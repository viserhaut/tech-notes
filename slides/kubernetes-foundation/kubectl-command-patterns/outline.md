# kubectl は"型"で覚える

テーマカラー: k8s
中心メッセージ: kubectl は「動詞＋リソース＋詳細」という1つの構文パターンを覚えれば、コマンドを丸暗記せずに大半の操作ができる。AWS CLI のサブコマンド体系と同じ発想で習得できる。

## スライド構成

1. [type-title]       表紙: kubectl は"型"で覚える
2. [type-summary]     Key Takeaway: 構文の型・動詞は7つ・AWS CLI と同じ発想
3. [type-message]     課題: コマンドを丸暗記しようとすると詰む（左テキスト/右図解）
4. [type-message-rev] 解決: kubectl は1つの構文パターンに集約される（左構文分解図/右テキスト）
5. [type-diagram]     動詞は「役割」で4グループに整理できる（観察/作成/削除/操作）
6. [type-code]        実コマンド例で型を体に染み込ませる（コード＋注釈）
7. [type-compare]     kubectl の型は AWS CLI / docker と地続き（比較表・AWS対比）
8. [type-summary]     まとめ: 型を覚える・動詞7つ・複数形と -f

## スコープ

- 対象チャプター: content/chapters/kubernetes-foundation/chapter-02.md
- 選択した技術要素: kubectl の基本構文パターン（動詞＋リソース＋詳細の型）
  ※ chapter-02 は kubectl / Minikube / Pod・Node / Deployment を含むが、タスク指定「kubectl パターン」に従い
    kubectl のコマンド体系（型）にスコープを絞る。Minikube・Pod/Node・Deployment は別デッキの領域とする。

## リファレンス

- slides/kubernetes-foundation/chapter-01/index.html（同コース・イントロ階層・8枚・Claude Code 単独生成）
- slides/kubernetes-foundation/job-cronjob-deployment/（同コース・Claude Design 生成・7枚・AWS 対比頻出）
</content>
</invoke>
