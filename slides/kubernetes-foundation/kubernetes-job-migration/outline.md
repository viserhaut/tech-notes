# JobでDBマイグレーションを単発実行する

テーマカラー: k8s (#4F8FFF)
中心メッセージ: Jobは「単発実行」の仕組み。minikube image loadでイメージを持ち込み、DBマイグレーションをJobで安全に実行できる

## スライド構成

1. [type-title] JobでDBマイグレーションを単発実行する
2. [type-section] Section 01 - Jobとは何か
3. [type-message] Jobは「一度きりの実行」リソース、ECSのrun-taskに相当
4. [type-compare] Deployment / Job / CronJob — 用途の違い
5. [type-section] Section 02 - Minikubeでイメージを持ち込む
6. [type-message-rev] minikube image loadでローカルイメージをMinikubeに転送
7. [type-code] Jobマニフェストの読み方（restartPolicy / backoffLimit）
8. [type-message] 再実行はdelete→apply、CI/CDへの組み込み
9. [type-summary] まとめ — 3つのポイント

## スコープ

- 対象チャプター: kubernetes-foundation/chapter-05.md
- 選択した技術要素: 全テーマ（Job・minikube image load・DBマイグレーション実行・CI/CD）
