# Kubernetesの運用監視 — Probe・HPA・ログ
テーマカラー: k8s (#4F8FFF)
中心メッセージ: Probe・requests/limits・HPA・ログ収集の4本柱でKubernetesアプリを自律回復・自動スケールする

## スライド構成
1. [type-title]       Kubernetesの運用監視 — Probe・HPA・ログ
2. [type-summary]     Key Takeaway（ヘッドライン＋図＋3ポイント）
3. [type-message]     Probeの3種類がコンテナの健全性を保つ
4. [type-message-rev] requests/limitsでリソースを安全に管理する
5. [type-diagram]     Metrics Server → HPA → スケールアウトの流れ
6. [type-message]     kubectl logsとsternでログを調査する
7. [type-compare]     Readiness/Liveness/Startup Probe の使い分け
8. [type-summary]     まとめ3カード

## スコープ
- 対象チャプター: cloud-pratica/content/chapters/kubernetes-foundation/chapter-11.md
- 選択した技術要素: Probe (Readiness/Liveness/Startup) · requests/limits · Metrics Server · HPA · ログ収集 (stern/Fluentd)
