# tech-notes

Zenn に公開する技術記事のソースリポジトリ。

## 構成

```
articles/      Zenn 記事（*.md）— ファイル名がそのまま記事 URL のスラッグになる
images/        記事内の画像（PNG）
books/         Zenn 本（未使用）
slides/        スライド出力（Git 管理外 — SpeakerDeck に手動アップ）
  [course]/
    chapter-XX.drawio     1枚図解（speakerdeck-slide スキル生成）
    chapter-XX.pdf        1枚図解 PDF（SpeakerDeck 用）
    [slug].html           複数枚デッキ HTML（slide-deck スキル生成）
    [slug].pdf            複数枚デッキ PDF（SpeakerDeck 用）
```

### slides/ の使い分け

| スキル | 出力 | 用途 |
|--------|------|------|
| `/speakerdeck-slide` | `chapter-XX.drawio` / `.pdf` + `images/[slug].png` | 1枚図解（Zenn 記事に埋め込む PNG） |
| `/slide-deck` | `[slug].html` / `.pdf` + `images/[slug]-ogp.png` | 複数枚プレゼンデッキ（OGP サムネイル付き） |

## 命名規則

記事・スライドのスラッグはカテゴリ-トピックで構成する。コース名・章番号は含めない。

```
kubernetes-probe.md
aws-iam-policy.md
terraform-import-workflow.md
```

スライドも同じスラッグを使う（例: `kubernetes-probe.html`, `kubernetes-probe-ogp.png`）。

## 公開フロー

### 1枚図解（speakerdeck-slide → zenn-article）

1. `/speakerdeck-slide` で `.drawio` + `images/[slug].png` を生成
2. draw.io CLI / VS Code で PDF エクスポート
3. SpeakerDeck に PDF をアップロード → スライド ID を取得
4. `/zenn-article` で記事を生成（図解 PNG + SpeakerDeck 埋め込み）
5. `published: false` のまま push → Zenn 下書き確認
6. `published: true` に変更して push → 公開

### 複数枚デッキ（slide-deck → zenn-article）

1. `/slide-deck` で `[slug].html` + `[slug].pdf` + `[slug]-ogp.png` を生成
2. SpeakerDeck に PDF をアップロード → スライド ID を取得
3. `/zenn-article` で記事を生成（OGP PNG + SpeakerDeck 埋め込み）
4. `published: false` のまま push → Zenn 下書き確認
5. `published: true` に変更して push → 公開

## ローカルプレビュー

```bash
npx zenn preview   # http://localhost:8000
```
