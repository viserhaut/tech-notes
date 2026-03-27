# CronJobとConfigMapでバッチ処理を構成する

テーマカラー: k8s (#4F8FFF)
中心メッセージ: CronJobはEventBridge+ECSのJobs相当。ConfigMapで設定を外部注入してバッチ処理を構成する

## スライド構成

1. [type-title] CronJobとConfigMapでバッチ処理を構成する
2. [type-section] Section 01 - CronJobとConfigMap
3. [type-message] CronJobはEventBridge Scheduler + ECS Jobの相当
4. [type-compare] Job vs CronJob — 手動実行 vs スケジュール実行
5. [type-message-rev] ConfigMapで設定を外部注入する
6. [type-section] Section 02 - バッチ実行と永続化確認
7. [type-diagram] CronJob → Job → Pod 実行フロー
8. [type-code] CronJob + ConfigMap マニフェスト
9. [type-summary] まとめ — 3つのポイント

## スコープ

- 対象チャプター: kubernetes-foundation/chapter-06.md
- 選択した技術要素: 全テーマ（CronJob・ConfigMap・バッチ実行・StatefulSet永続化確認）
