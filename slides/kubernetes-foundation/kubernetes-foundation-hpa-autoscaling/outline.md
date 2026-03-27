# HPAでPodの自動スケーリングを実現する
テーマカラー: k8s (#4F8FFF)
中心メッセージ: HPAはrequestsベースのメトリクスでPod数を自動調整し、負荷変動に対応する

## スライド構成
1. [type-title] HPAでPodの自動スケーリングを実現する
2. [type-section] なぜ自動スケーリングが必要か
3. [type-message] 手動スケーリングでは負荷急増に対応できない
4. [type-message-rev] HPAがメトリクスを監視してPod数を自動調整する
5. [type-compare] ECSオートスケーリング vs HPA — 設定構造の比較
6. [type-code] HPA マニフェストとスケーリングポリシー
7. [type-diagram] Metrics Server → HPA → Deployment のスケーリングフロー
8. [type-summary] HPA設計の3つのポイント

## スコープ
- 対象チャプター: cloud-pratica/content/chapters/kubernetes-foundation/chapter-11.md
- 選択した技術要素: HPA (Horizontal Pod Autoscaler)
