# my-swagger-template

Swagger UI／Swagger API mock を使用するためのテンプレートプロジェクト<br>

## FEATURE

- swaggerui を用いた API 仕様書作成
- stoplight/prism:4 を用いた API スタブ作成
- yaml ファイルを用いたソースコード共通化
  - components/base-data: GET するデータを基準に共通化
  - components/error-response: HTTP レスポンスのエラーコンテンツを共通化
- gulpfile を用いた共通コードの自動統合

## HOW TO USE

### 1 ターミナルを開き、docker-compose.yml が存在するフォルダへ移動

ターミナルを開き、docker-compose.yml が存在するフォルダへ移動<br>
`cd ~/specs`

### 2 npm パッケージのインストール

下記コマンドを実行<br>
`npm ci`

### 3 swagger.yaml を自動更新するための gulpfile の実行

下記コマンドを実行<br>
`npm start`

### 4 Docker Desktop を起動

ローカルにて Docker Desktop を起動する。<br>
左下の Docker マークの色が青背景の白抜きになっていることを確認する。

### 5 新規のターミナルを開き、docker-compose.yml が存在するフォルダへ移動

新規のターミナルを開き、docker-compose.yml が存在するフォルダへ移動<br>
`cd ~/specs`

### 6 Docker コンテナを起動する

` docker-compose up -d`　<br>
⇒ Docker Desktop にて、Docker コンテナが 2 つ起動していることを確認する。<br>

### 7 サーバに接続する

ブラウザ等を経由してサーバに接続する。<br>

| サービス         | URL                               |
| ---------------- | --------------------------------- |
| Swagger UI       | http://localhost:50000/           |
| Swagger API mock | http://localhost:50001/users など |
