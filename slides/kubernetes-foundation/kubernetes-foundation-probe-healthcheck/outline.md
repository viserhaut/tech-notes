# Kubernetes Probe でヘルスチェックを自動化する
テーマカラー: k8s (#4F8FFF)
中心メッセージ: Probeは3種を正しく使い分けることで、障害時のユーザー影響を最小化し自動復旧を実現する

## スライド構成
1. [type-title] Kubernetes Probe でヘルスチェックを自動化する
2. [type-section] Probeが解決する問題
3. [type-message] Probeなしではコンテナ障害がユーザーに直撃する
4. [type-message-rev] 3種のProbeがそれぞれ異なるレイヤーを守る
5. [type-compare] Readiness vs Liveness vs Startup — 判断基準の比較
6. [type-code] Probe設定の実践マニフェスト
7. [type-diagram] Probe判定フローと Pod ライフサイクル
8. [type-summary] 本番運用でのProbe設計3原則

## スコープ
- 対象チャプター: cloud-pratica/content/chapters/kubernetes-foundation/chapter-11.md
- 選択した技術要素: Readiness Probe / Liveness Probe / Startup Probe
