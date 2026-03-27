# Probe・HPA・ログで本番運用を安全にする

テーマカラー: k8s (#4F8FFF)
中心メッセージ: Probe・HPA・ログの3本柱でKubernetesの可観測性を確立する

## スライド構成

1. [type-title] Probe・HPA・ログで本番運用を安全にする
2. [type-section] Section 01 - リソース管理とオートスケール
3. [type-message] requests/limitsでスケジューリングと実行制御を分離する
4. [type-compare] requests vs limits — 予約 vs 上限
5. [type-message-rev] HPAがMetrics Serverのメトリクスで自動スケール
6. [type-section] Section 02 - 可観測性とProbe
7. [type-compare] Readiness / Liveness / Startup — 3種のProbeの使い分け
8. [type-message] sternで複数PodのログをリアルタイムTail
9. [type-summary] まとめ — 3つのポイント

## スコープ

- 対象チャプター: kubernetes-foundation/chapter-11.md
- 選択した技術要素: 全テーマ（requests/limits・HPA・Probe・ログ収集・Metrics Server）
