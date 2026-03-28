# Probe でコンテナの異常を自動検知する
テーマカラー: k8s (#4F8FFF)
中心メッセージ: 3種のProbeを正しく使い分けることで、障害時のユーザー影響をゼロに近づけ自動復旧を実現する

## スライド構成
1. [type-title]   Probe でコンテナの異常を自動検知する
2. [type-summary] Key Takeaway（3種の役割図＋ポイント3点）
3. [type-message] Probeなしでは障害がユーザーに直撃する
4. [type-message-rev] 3種のProbeが別々のレイヤーを守る
5. [type-compare] Readiness vs Liveness vs Startup 比較表
6. [type-code]    Probe設定マニフェスト例
7. [type-diagram] Pod起動〜障害〜復旧のフロー
8. [type-summary] 本番Probe設計3原則

## スコープ
- 対象チャプター: cloud-pratica/content/chapters/kubernetes-foundation/chapter-11.md
- 選択した技術要素: Readiness Probe / Liveness Probe / Startup Probe
