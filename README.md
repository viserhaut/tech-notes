# tech-notes

Zenn に公開する技術記事のソースリポジトリ。

## 構成

```
articles/      Zenn 記事（*.md）— ファイル名がそのまま記事 URL のスラッグになる
images/        記事内の画像（PNG）
books/         Zenn 本（未使用）
```

## 命名規則

記事ファイル名はカテゴリ-トピックで構成する。

```
kubernetes-probe.md
aws-iam-policy.md
terraform-import-workflow.md
```

## 記事の公開フロー

1. `published: false` のまま push → Zenn 下書きとして同期
2. Zenn ダッシュボードでプレビュー確認
3. `published: true` に変更して push → 公開

## ローカルプレビュー

```bash
npx zenn preview   # http://localhost:8000
```
