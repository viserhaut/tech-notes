# IngressでL7ルーティングを実現する

テーマカラー: k8s (#4F8FFF)
中心メッセージ: IngressはALB相当のL7ルーティング。Ingress Controllerがルーティングを実行する

## スライド構成

1. [type-title] IngressでL7ルーティングを実現する
2. [type-section] Section 01 - IngressとIngress Controller
3. [type-message] NodePort/LoadBalancerの限界 — マイクロサービスが増えるたびにLBが増える
4. [type-compare] LoadBalancer vs Ingress — NLB vs ALB相当
5. [type-message-rev] Ingress Controllerがリクエストをルーティングする
6. [type-code] Ingress マニフェストとパスルーティング設定
7. [type-diagram] Client → Ingress Controller → Service → Pod フロー
8. [type-summary] まとめ — 3つのポイント

## スコープ

- 対象チャプター: kubernetes-foundation/chapter-10.md
- 選択した技術要素: 全テーマ（Ingress・Ingress Controller・L7ルーティング・LoadBalancer比較）
