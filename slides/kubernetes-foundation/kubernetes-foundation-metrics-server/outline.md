# Metrics Serverでリソース監視の基盤を作る
テーマカラー: k8s (#4F8FFF)
中心メッセージ: Metrics Serverはクラスタ全体のリソース可視化とオートスケーリングの土台となる

## スライド構成
1. [type-title] Metrics Serverでリソース監視の基盤を作る
2. [type-section] なぜMetrics Serverが必要か
3. [type-message] kubectl topが使えないのはメトリクス収集基盤がないから
4. [type-message-rev] Metrics Serverがノード全体のメトリクスを集約する
5. [type-compare] EKS vs GKE — Metrics Serverの扱いの違い
6. [type-code] Minikubeへの導入とkubectl topの実行
7. [type-diagram] cAdvisor → Metrics Server → kubectl top / HPA の全体像
8. [type-summary] Metrics Server導入の3ステップ

## スコープ
- 対象チャプター: cloud-pratica/content/chapters/kubernetes-foundation/chapter-11.md
- 選択した技術要素: Metrics Server
