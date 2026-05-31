# スライドブリーフ: なぜ Kubernetes が必要なのか

## メタ情報

- **コース**: kubernetes-foundation
- **スラッグ**: why-kubernetes-orchestration
- **出力ディレクトリ**: slides/kubernetes-foundation/chapter-01/（タスク handoff_note 指定）
- **テーマカラー**: k8s (#4F8FFF)
- **元チャプター**: content/chapters/kubernetes-foundation/chapter-01.md
- **スライド枚数**: 8枚

## 中心メッセージ

コンテナ単体では本番運用が回らない。Kubernetes は「望ましい状態の宣言」と「調整ループ」で、障害復旧・スケール・更新を自動化する。AWS エンジニアは ECS の知識を踏み台にして概念を対応づけられる。

## 対象読者

- AWS（特に ECS）でコンテナ運用の経験があるエンジニア
- これから Kubernetes を学び始める段階
- 宣言的モデル・調整ループ・コントロールプレーン/データプレーンの全体像を掴みたい

## スライド構成

| # | タイプ | タイトル | 要点 |
|---|--------|----------|------|
| 1 | type-title | なぜ Kubernetes が必要なのか | コンテナオーケストレーションの本質 |
| 2 | type-summary | Key Takeaway | オーケストレーション必須・宣言的・自動運用 |
| 3 | type-message | コンテナ単体では本番が回らない | 手動運用は止まる |
| 4 | type-message-rev | 宣言的モデルが手順を肩代わりする | 命令的 vs 宣言的 |
| 5 | type-diagram | 調整ループが差分を埋め続ける | desired/current の差分を自動修正 |
| 6 | type-diagram | クラスタは「頭脳」と「実行」に分かれる | Control Plane / Data Plane |
| 7 | type-compare | 運用タスクは手動から自動へ | 復旧・スケール・更新・配置 |
| 8 | type-summary | まとめ | オーケストレーション必須・宣言的＋調整ループ・ポータビリティ |

## デザイン指示

- ECS / EKS との対比を随所に入れる（対象読者が AWS エンジニアのため）
- 図解は SVG インライン、ダークテーマ（#0B0E14 背景）
- 矢印は orthogonal routing（polyline・辺中央・先端は辺を超えない）、ラベルと重ねない
- 1スライド1メッセージ、箇条書きは3項目以内
- 図解はフロー一辺倒にせず、調整ループ図＋階層（アーキテクチャ）図を混在させる

## 備考

- 第1章全体のイントロダクションとして使用（次章以降の Pod / Deployment 詳細への導入）
- 既存の slides/kubernetes-foundation/aws-engineer-intro/（Claude Design 生成）と同主題。
  本デッキは Claude Code 単独生成版で、品質比較（検証）用に chapter-01/ ディレクトリへ分離出力した。
