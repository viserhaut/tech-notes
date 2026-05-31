# なぜ Kubernetes が必要なのか

テーマカラー: k8s (#4F8FFF)
中心メッセージ: コンテナ単体運用の限界を、Kubernetes は宣言的モデルと調整ループで自動的に埋める

## スライド構成

1. [type-title] なぜ Kubernetes が必要なのか
2. [type-summary] Key Takeaway（オーケストレーション必須・宣言的・自動運用）
3. [type-message] コンテナ単体では本番が回らない（手動運用の限界）
4. [type-message-rev] 宣言的モデルが手順を肩代わりする（命令的 vs 宣言的）
5. [type-diagram] 調整ループが差分を埋め続ける（Reconciliation Loop）
6. [type-diagram] クラスタは「頭脳」と「実行」に分かれる（Control Plane / Data Plane）
7. [type-compare] 運用タスクは手動から自動へ（復旧・スケール・更新・配置）
8. [type-summary] まとめ（オーケストレーション必須・宣言的＋調整ループ・ポータビリティ）

## スコープ

- 対象チャプター: content/chapters/kubernetes-foundation/chapter-01.md
- 選択した技術要素: チャプター全体（1.1 コンテナ単体の限界 〜 1.5 学ぶ意義）

## リファレンス（Step 0.5 で参照した品質基準）

- slides/kubernetes-foundation/aws-engineer-intro/（同主題・7枚、density の主基準）
- slides/kubernetes-foundation/service-ingress-architecture/（図解パターンの補助）

## リファレンス比較メモ

- 目標枚数 7枚 → 本デッキ 8枚（チャプターが5節と厚いため +1、許容 ±1 内）
- type 分布: title1 / summary2 / message1 / message-rev1 / diagram2 / compare1（フロー図偏重を回避し loop 図＋階層図を混在）
- 各 message スライド: lead 1文 + 箇条書き 3点（リファレンス準拠）
- AWS 対比: slide5（ECS Service Scheduler）・slide6（EKS / EC2・Fargate）・slide7（ECS Service Auto Scaling）に分散挿入
