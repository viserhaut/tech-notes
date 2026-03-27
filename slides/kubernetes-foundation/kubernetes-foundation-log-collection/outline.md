# Kubernetesのログ収集を理解して障害調査力を上げる
テーマカラー: k8s (#4F8FFF)
中心メッセージ: Kubernetesのログは標準出力がノードに集約される仕組みを理解し、適切なツールで調査する

## スライド構成
1. [type-title] Kubernetesのログ収集を理解して障害調査力を上げる
2. [type-section] ログはどこに集まるのか
3. [type-message] Pod単位のログ確認ではマイクロサービスの調査が追いつかない
4. [type-message-rev] kubeletが標準出力をノード内に自動収集している
5. [type-compare] kubectl logs vs stern vs Fluentd — ツール選択の判断基準
6. [type-code] sternによる複数Podの横断ログ確認
7. [type-diagram] stdout → kubelet → Node → 外部ログ基盤の全体フロー
8. [type-summary] ログ調査スキルの3段階

## スコープ
- 対象チャプター: cloud-pratica/content/chapters/kubernetes-foundation/chapter-11.md
- 選択した技術要素: ログ収集 (kubectl logs / stern / Fluentd)
