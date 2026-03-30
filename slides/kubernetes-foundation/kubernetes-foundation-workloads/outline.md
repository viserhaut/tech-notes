# Kubernetesコアワークロード入門
テーマカラー: k8s (#4F8FFF)
中心メッセージ: PodからDeployment・Job・CronJobまで、Kubernetesの主要ワークロードを一覧で理解する

## スライド構成
1. [type-title]       Kubernetesコアワークロード入門
2. [type-summary]     Key Takeaway（ヘッドライン＋図＋3ポイント）
3. [type-message]     PodはKubernetesの最小実行単位
4. [type-message-rev] DeploymentがPodを自動復旧・スケールする
5. [type-diagram]     Deployment → ReplicaSet → Pod の階層構造
6. [type-message]     Jobは単発・CronJobは定期実行を担う
7. [type-message-rev] ConfigMapで設定をPodに外部注入する
8. [type-compare]     ワークロード種別の使い分け早見表
9. [type-summary]     まとめ：3つのポイント

## スコープ
- 対象チャプター: cloud-pratica/content/chapters/kubernetes-foundation/chapter-02.md, chapter-05.md, chapter-06.md
- 選択した技術要素: Pod・Deployment・ReplicaSet・Job・CronJob・ConfigMap
