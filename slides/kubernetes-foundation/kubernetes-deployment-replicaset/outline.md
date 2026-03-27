# DeploymentでAPIサーバーを安定稼働させる

テーマカラー: k8s (#4F8FFF)
中心メッセージ: DeploymentはECSサービス相当。ReplicaSetを裏で管理しロールバックも可能にする

## スライド構成

1. [type-title] DeploymentでAPIサーバーを安定稼働させる
2. [type-section] Section 01 - DeploymentとReplicaSet
3. [type-message] DeploymentはECSサービスに相当するPod管理リソース
4. [type-compare] ReplicaSet直接操作 vs Deployment — なぜDeploymentを使うか
5. [type-section] Section 02 - ConfigMap・SecretとAPI構築
6. [type-message-rev] ConfigMap + SecretでAPIの環境変数を外部注入
7. [type-code] Deployment + ConfigMap + Secret マニフェスト
8. [type-message] ロールアウトとロールバック — kubectl rollout
9. [type-summary] まとめ — 3つのポイント

## スコープ

- 対象チャプター: kubernetes-foundation/chapter-07.md
- 選択した技術要素: 全テーマ（Deployment・ReplicaSet・ConfigMap・Secret・ロールアウト）
