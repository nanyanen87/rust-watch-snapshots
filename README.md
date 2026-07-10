# rust-watch-snapshots

[rust-watch](https://github.com/nanyanen87) (個人用のRustサーバー定点観測) のリモートコレクター。

- GitHub Actions が5分間隔で BattleMetrics API からスナップショットを取得(トークン+身元入りUA)
- スナップショットは AES-256-CBC で暗号化してコミット(`snapshots/*.json.gz.enc`)。
  復号鍵はこのリポジトリには含まれない
- 観測サーバー: Rustoria EU East Long (今ワイプ周期限定の一時運用)
