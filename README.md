# my-swagger-template

Swagger UI／Swagger API mock を使用するためのテンプレートです。<br>

# Swagger の使用方法

## 使用手順

### 使用手順 1：docker-compose.yml が存在するフォルダへ移動

コマンドプロンプトを開き、docker-compose.yml が存在するフォルダへ移動する。<br>
`cd ~/specs`

### 使用手順 2：モジュール等のインストール

npm を使用してパッケージをインストールする。<br>
`npm ci`　<br>

### 使用手順 3：コンテナ作成＆アプリ起動

npm を用いてサーバを起動する。gulp 処理を実行。<br>
※ swagger.yaml を自動更新するため<br>
`npm start` <br>

<br>
新しいコマンドプロンプトを開き、docker-compose.yml が存在するコンテナに移動し、Docker コンテナを立ち上げる。<br>
<br>

`cd ~/swagger-template` <br>

` docker-compose up -d`　<br>
⇒ Docker コンテナが 2 つ起動していることを確認する。<br>

### 使用手順 4：サーバに接続する

ブラウザ等を経由してサーバに接続する。<br>

| サービス         | URL                               |
| ---------------- | --------------------------------- |
| Swagger UI       | http://localhost:50000/           |
| Swagger API mock | http://localhost:50001/users など |
