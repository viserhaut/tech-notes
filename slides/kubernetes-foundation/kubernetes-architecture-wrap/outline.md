# KubernetesのService全種とアーキテクチャを俯瞰する

テーマカラー: k8s (#4F8FFF)
中心メッセージ: Service4種とK8sアーキテクチャを俯瞰してコースを締めくくる

## スライド構成

1. [type-title] KubernetesのService全種とアーキテクチャを俯瞰する
2. [type-section] Section 01 - Service 4種を使い分ける
3. [type-compare] ClusterIP / Headless / NodePort / LoadBalancer — 4種比較
4. [type-message] マイクロサービス増加でLoadBalancerは破綻する
5. [type-message-rev] IngressがLoadBalancerの代替になる理由
6. [type-section] Section 02 - Kubernetesアーキテクチャ
7. [type-diagram] Control Plane + Worker Node 全体構成図
8. [type-message] kubeletがPod仕様を実現し、kube-proxyがネットワークを制御
9. [type-summary] まとめ — コース振り返り3ポイント

## スコープ

- 対象チャプター: kubernetes-foundation/chapter-12.md
- 選択した技術要素: 全テーマ（Service4種・LoadBalancer vs Ingress・K8sアーキテクチャ）
