# KubernetesでPostgres DBを構築する

テーマカラー: k8s (#4F8FFF)
中心メッセージ: DBの永続化はStatefulSet・PV・Secretの3本柱で成り立つ。Serviceで名前解決して安定アクセスを実現する

## スライド構成

1. [type-title] KubernetesでPostgres DBを構築する
2. [type-section] Section 01 - なぜStatefulSetが必要か
3. [type-message] DeploymentではなくStatefulSetを使う理由
4. [type-compare] 静的プロビジョニング vs 動的プロビジョニング
5. [type-section] Section 02 - SecretとServiceで完成させる
6. [type-message-rev] Secretは「ゆるい秘匿」、本番はSecretsManager+ESOへ
7. [type-message] ServiceのないPodは再起動でIPが変わる
8. [type-compare] ClusterIP vs Headless Service
9. [type-code] StatefulSet + Secret + Headless Service マニフェスト抜粋
10. [type-summary] まとめ — 3つのポイント

## スコープ

- 対象チャプター: kubernetes-foundation/chapter-04.md
- 選択した技術要素: 全テーマ（StatefulSet・PV/PVC・Secret・Service Headless）
