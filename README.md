## GitHub Actions iOS CD Template

iOSアプリのTestFlight配信のActionsのテンプレート、ExportOptions.plistのテンプレートです。

### Actionsの機能

`deliver.yaml` は、以下の処理を自動で行う GitHub Actions ワークフローです

- iOS アプリのビルドからTestFlightの配信までを行う。
- Push通知のEntitlementを埋め込む。
- このワークフローは `workflow_dispatch` トリガーで実行され、GitHub Actions 画面から手動で起動します。

### GitHub Actionsのsecretsを登録

App Store Connect にデプロイするために、以下の3つの GitHub Secrets をリポジトリに設定してください。

| Secret名                          | 内容                                                                 |
|----------------------------------|----------------------------------------------------------------------|
| `APP_STORE_CONNECT_API_KEY`      | App Store Connect APIの秘密鍵（`.p8`ファイルの中身をそのまま貼り付け） |
| `APP_STORE_CONNECT_API_KEY_ID`   | 秘密鍵に対応する「キーID」                                          |
| `APP_STORE_CONNECT_API_KEY_ISSUER_ID` | APIキー発行元の「Issuer ID」                                     |

Ref: 
https://developer.apple.com/jp/help/app-store-connect/get-started/app-store-connect-api/
