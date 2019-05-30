# ASP .Net Coreテスト用プロジェクト

## 導入

- .Net Core SDKのインストール
  - [.Net Core SDK](https://dotnet.microsoft.com/download)

- ASP .Net Core用プロジェクトの作成(React + Redux)

  ```command
  dotnet new reactredux
  ```

- 動作確認
  - vscodeでプロジェクトを開き、デバッグ実行
  - アクセスしてHello, World!!が表示されればOK

    ```url
    https://localhost:5001/
    ```

- db

  - dbコンテナ作成

    ```dbコンテナ作成
    docker-compose up -d --build
    ```

  - db確認

    ```db確認
    docker-compose exec my-db psql -U dev
    psql (9.6.13)
    "help" でヘルプを表示します.

    dev=# \d
            リレーションの一覧
    スキーマ |  名前  |    型    | 所有者
    ----------+--------+----------+--------
    public   | sample | テーブル | dev
    (1 行)
    ```

  - dbコンテナ削除

    ```dbコンテナ削除
    docker-compose down
    ```

  - dbコンテナ削除(ボリュームも一緒に)

    ```dbコンテナ削除
    docker-compose down -v
    ```

  - dbについて
    - postgresqlは/docker-entrypoint-initdb.dディレクトリに*.sql, *.sql.gz, or *.shのファイルを配置するとコンテナ起動時に勝手に実行してくれるようだ。DBの初期化処理(テーブル作成等)をこのタイミングでするのが良さそう。

## やることリスト(順不同)

- ~~DB構築(Postgresql)~~
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

## 参考

[.NET Coreでサービスを作ってデスクトップアプリで利用してみる](https://qiita.com/shimura_atsushi/items/7321b023c3e837f16552)  
[Docker PostgreSQLイメージを利用する](https://qiita.com/kimullaa/items/70eaec61c02d2513e76c)