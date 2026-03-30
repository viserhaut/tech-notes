# KubernetesでDBを永続化する
テーマカラー: k8s (#4F8FFF)
中心メッセージ: StatefulSet・PV/PVC・Secretの3本柱でDBをKubernetesで安全に永続化できる

## スライド構成
1. [type-title]       KubernetesでDBを永続化する
2. [type-summary]     Key Takeaway（ヘッドライン＋図＋3ポイント）
3. [type-message]     Deploymentではデータが消える理由
4. [type-message-rev] StatefulSetがPodとストレージを1対1で紐づける
5. [type-diagram]     PVC → PV → ストレージの動的プロビジョニング
6. [type-message]     SecretでDB認証情報を安全に管理する
7. [type-compare]     Deployment vs StatefulSet 使い分け
8. [type-summary]     まとめ：3つのポイント

## スコープ
- 対象チャプター: cloud-pratica/content/chapters/kubernetes-foundation/chapter-04.md
- 選択した技術要素: StatefulSet・PV/PVC・Secret・Headless Service
