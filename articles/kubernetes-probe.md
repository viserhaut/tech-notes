---
title: "【Kubernetes】Pod のヘルスチェック — 3 種類の Probe の役割と使い分け"
emoji: "🔍"
type: "tech"
topics: ["kubernetes", "cloudnative", "container"]
published: false
---

## TL;DR

**Overview**
- Probe は **Startup / Readiness / Liveness** の3種類。それぞれ「起動完了待ち」「トラフィック制御」「プロセス死活」と役割が異なる
- ECS のヘルスチェック2軸（生死・トラフィック）に「起動中か起動失敗か」の軸を加えて3種類に分割している

**Points**
- **Startup Probe** は起動時間が不定なアプリ（Java 等）に使う。`initialDelaySeconds` より柔軟で、起動が早ければ即座に次フェーズへ移行できる
- 本番では **Readiness + Liveness をセットで設定**する。Liveness の `initialDelaySeconds` は Readiness より長く設定し、起動直後の誤再起動を防ぐ

**Tips**
- **Liveness に外部依存（DB など）を含めない**。DB 障害時に全 Pod が再起動してカスケード障害になる
- **Readiness の失敗は Pod を維持したまま Service から除外するだけ**。Liveness と混同して過剰に再起動させないようにする

![Kubernetes の 3 種類の Probe](/images/kubernetes-probe.png)

## 3 種類の Probe が必要な理由

- **ECS のヘルスチェックは「生きているか」「トラフィックを流すか」の2軸だった**
  - Kubernetes はそこに「起動中か起動失敗か」を区別する軸を追加し、3種類に分割している

| Probe | 失敗時の動作 | ECS の対応機能 |
|-------|-------------|----------------|
| Startup | コンテナ再起動（猶予あり） | コンテナ依存関係設定 |
| Readiness | Service から除外（Pod は維持） | ALB ターゲットグループ ヘルスチェック |
| Liveness | コンテナ強制再起動 | タスク定義のコンテナ HealthCheck |

## Startup Probe が解決する問題

- **起動完了タイミングが読めないアプリ**（Java 等）では、Liveness Probe が起動中に動いて誤判定し、永遠に再起動ループに陥る
  - Startup Probe はその間、Liveness と Readiness をブロックする
- **`initialDelaySeconds` を大きく設定するより柔軟**
  - `initialDelaySeconds: 300` は常に300秒待つ
  - Startup Probe なら10秒で起動が終われば即座に次のフェーズへ、遅れても最大300秒待てる

```yaml
startupProbe:
  httpGet:
    path: /api/health
    port: 8080
  failureThreshold: 30  # 最大 30 回 = 300秒の猶予
  periodSeconds: 10
```

## Readiness と Liveness の使い分け

- **Readiness Probe** ——「トラフィックを受けてよいか」の判断
  - 失敗しても Pod は生き続け、Service から外れるだけ
  - ゼロダウンタイムデプロイや DB 接続待ちに有効
  - 新しい Pod が Readiness を通過するまで古い Pod が残るため、切り替え時の 502 を防げる
- **Liveness Probe** ——「プロセスが回復不能な状態でないか」の検知
  - 失敗するとコンテナが強制再起動される
  - ハングアップやメモリリークの自動回復に使う
- **Liveness に外部依存（DB など）を入れてはいけない**
  - DB が一時的に落ちると全 Pod が再起動し、復旧後にアクセスが集中してカスケード障害になる
  - Liveness はプロセス自体の死活のみを確認する

## 本番設定の例

```yaml
livenessProbe:
  httpGet:
    path: /api/health
    port: 8080
  initialDelaySeconds: 15  # Readiness より長くする。起動直後の一時的な重さで再起動ループに入らないよう猶予を持たせる
  periodSeconds: 10        # 10秒ごとにチェック
  failureThreshold: 3      # 3回連続失敗（=30秒）で再起動。瞬間的なエラーで即再起動しないよう余裕を持たせる

readinessProbe:
  httpGet:
    path: /api/health
    port: 8080
  initialDelaySeconds: 5   # 起動後すぐチェック開始。早めに Service に組み込む
  periodSeconds: 10
  failureThreshold: 3      # 3回連続失敗で Service から除外。Pod は生存したまま
```
