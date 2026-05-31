# スライドブリーフ: kubectl は"型"で覚える — 動詞＋リソース＋詳細の構文パターン

## メタ情報

- **コース**: kubernetes-foundation
- **スラッグ**: kubectl-command-patterns
- **出力ディレクトリ**: slides/kubernetes-foundation/kubectl-command-patterns/
- **テーマカラー**: k8s (#4F8FFF)
- **元チャプター**: content/chapters/kubernetes-foundation/chapter-02.md
- **スライド枚数**: 8枚

## 中心メッセージ

kubectl は無数のコマンドの集合ではなく、「動詞＋リソース＋詳細」という1つの構文パターンに集約される。
この型を理解すれば、コマンドを丸暗記しなくても都度調べず正しく叩けるようになる。
AWS CLI の `aws <サービス> <アクション>` と同じ「サブコマンド体系」の発想で習得できる。

## 対象読者

- AWS（特に ECS / AWS CLI）の実務経験があるエンジニア
- これから kubectl を触り始める段階
- コマンドを暗記ではなく「構文の型」として体系的に掴みたい

## スライド構成

| # | タイプ | タイトル | 要点 |
|---|--------|----------|------|
| 1 | type-title | kubectl は"型"で覚える | 動詞＋リソース＋詳細の一文構文 |
| 2 | type-summary | Key Takeaway | 構文の型・動詞は7つ・AWS CLI と同じ発想 |
| 3 | type-message | コマンドの丸暗記は早晩行き詰まる | 操作ごとに検索する非効率 |
| 4 | type-message-rev | kubectl は1つの構文パターンに集約される | 動詞＋リソース＋名前＋オプションの分解 |
| 5 | type-diagram | 動詞は「役割」で4グループに整理できる | 観察 / 作成・適用 / 削除 / 操作 |
| 6 | type-code | 実コマンド例で型を体に染み込ませる | get / describe / apply / exec の実例 |
| 7 | type-compare | kubectl の型は AWS CLI / docker と地続き | サブコマンド体系の対比 |
| 8 | type-summary | まとめ | 型で覚える・動詞7つ・複数形と -f |

## デザイン指示

- AWS CLI / docker との対比を随所に入れる（対象読者が AWS エンジニアのため）
- 図解は SVG インライン、ダークテーマ（#0B0E14 背景）
- 矢印は orthogonal routing（polyline・辺中央・先端は辺を超えない）、ラベルと重ねない
- 1スライド1メッセージ、箇条書きは3項目以内
- 図解はフロー一辺倒にせず、構文分解図（スライド4）＋役割グルーピング図（スライド5）を混在させる
- 絵文字・アイコンは使わない

## 備考

- chapter-02 は kubectl・Minikube・Pod/Node・Deployment を含む大型チャプターだが、
  タスク指定「kubectl パターン」に従い kubectl の構文体系のみにスコープを絞った。
- Minikube 導入・Pod/Node 概念・Deployment は別デッキ（別タスク）の領域とする。
</content>
