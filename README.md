# ASP .Net Coreテスト用プロジェクト

## 導入

- .Net Core SDKのインストール
  - [.Net Core SDK](https://dotnet.microsoft.com/download)

- ASP .Net Core用プロジェクトの作成

  ```command
  dotnet new webapi -n myServer
  ```

- 動作確認
  - vscodeでプロジェクトを開き、デバッグ実行
  - アクセスしてデータが表示されればOK

    ```url
    https://localhost:5001/api/values
    ```

## やることリスト(順不同)

- DB構築(Postgresql)
- モデルクラス作成
- Docker化
- Viewの作成(cshtml?)
- SPA化(React)

## 構成

- Server
  - ASP .Net Core
- Client
  - React(将来的には+Redux)
  - Typescript
- DB
  - Postgresql