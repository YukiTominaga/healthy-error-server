# HEALTY-ERROR-SERVER 簡易仕様説明

## エンドポイント一覧
- /
- /health
- /unhealth

## 仕様
ルートパスへのリクエストは、200コードを返します。
`/unhealth`へのリクエストを送ると503コードを返すようになり、`/health`へリクエストを送ると再度200コードを返します。

## 初期状態
実行時環境変数 `HEALTHY` が "FALSE" または "false" の時は最初から503が返ってきます。

## リクエスト例
```
$ curl -i localhost:8080
HTTP/1.1 200 OK
Date: Wed, 18 Sep 2019 07:39:05 GMT
Content-Length: 24
Content-Type: text/plain; charset=utf-8

HostName is dcb52ea79e63
```
