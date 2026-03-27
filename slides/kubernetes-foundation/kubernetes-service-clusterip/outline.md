# ClusterIPでPodへの安定アクセスを実現する

テーマカラー: k8s (#4F8FFF)
中心メッセージ: PodのIPは再起動で変わる。ClusterIPが仮想IPとロードバランシングでこれを解決する

## スライド構成

1. [type-title] ClusterIPでPodへの安定アクセスを実現する
2. [type-section] Section 01 - なぜServiceが必要か
3. [type-message] PodのIPは再起動で変わる — Serviceで解決
4. [type-diagram] Client → ClusterIP → Pod ロードバランシング図
5. [type-section] Section 02 - ClusterIPの仕組み
6. [type-message-rev] kube-proxyがiptablesルールを管理する
7. [type-code] ClusterIP Service マニフェストとcurlでの確認
8. [type-summary] まとめ — 3つのポイント

## スコープ

- 対象チャプター: kubernetes-foundation/chapter-08.md
- 選択した技術要素: 全テーマ（Service ClusterIP・Pod安定アクセス・kube-proxy・curl確認）
