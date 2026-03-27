# NodePortでクラスタ外からPodに接続する

テーマカラー: k8s (#4F8FFF)
中心メッセージ: NodePortは全Nodeに同じポートを開け、クラスタ外からPodに到達できる唯一の手段

## スライド構成

1. [type-title] NodePortでクラスタ外からPodに接続する
2. [type-section] Section 01 - NodePortの仕組み
3. [type-message] ClusterIPだけでは外部からアクセスできない
4. [type-compare] ClusterIP vs NodePort — 内部通信 vs 外部公開
5. [type-message-rev] NodePortは全Nodeに30000-32767番ポートを開ける
6. [type-code] NodePort Service マニフェストとminikube ipでの確認
7. [type-summary] まとめ — 3つのポイント

## スコープ

- 対象チャプター: kubernetes-foundation/chapter-09.md
- 選択した技術要素: 全テーマ（NodePort・クラスタ外公開・minikube ip・curl確認）
