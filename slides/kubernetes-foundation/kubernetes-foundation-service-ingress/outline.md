# KubernetesアプリをServiceとIngressで外部公開する
テーマカラー: k8s (#4F8FFF)
中心メッセージ: ServiceとIngressの2段構えで、PodをL4負荷分散→L7ルーティングで安全に外部公開できる

## スライド構成
1. [type-title]       KubernetesアプリをServiceとIngressで外部公開する
2. [type-summary]     Key Takeaway（ヘッドライン＋図＋3ポイント）
3. [type-message]     PodのIPが変わる問題をServiceが解決する
4. [type-message-rev] Serviceの4種類と使い分け
5. [type-diagram]     NodePortからIngressへ: 外部公開の進化
6. [type-message]     IngressがL7でマイクロサービスを振り分ける
7. [type-compare]     Service Type使い分け基準
8. [type-summary]     まとめ3カード

## スコープ
- 対象チャプター: cloud-pratica/content/chapters/kubernetes-foundation/chapter-08.md, chapter-09.md, chapter-10.md
- 選択した技術要素: Service (ClusterIP / Headless / NodePort / LoadBalancer) · Ingress · Ingress Controller
