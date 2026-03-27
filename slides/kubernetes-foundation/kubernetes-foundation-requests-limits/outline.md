# requests / limitsでリソース暴走を防ぐ
テーマカラー: k8s (#4F8FFF)
中心メッセージ: requestsとlimitsを正しく設定することで、ノード障害とリソース暴走を防ぐ

## スライド構成
1. [type-title] requests / limitsでリソース暴走を防ぐ
2. [type-section] リソース制限が必要な理由
3. [type-message] 設定なしではノード過剰配置とOOM Killが発生する
4. [type-message-rev] requestsで予約しlimitsで制限する2段階の仕組み
5. [type-compare] requests vs limits — 役割・使われ方・未設定リスクの比較
6. [type-code] resources設定の実践マニフェスト
7. [type-diagram] スケジューリングからOOM Killまでのリソース制御フロー
8. [type-summary] 本番運用でのリソース設計3原則

## スコープ
- 対象チャプター: cloud-pratica/content/chapters/kubernetes-foundation/chapter-11.md
- 選択した技術要素: requests / limits
