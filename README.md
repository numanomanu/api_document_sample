# api spec
## spec
- node_version: v8.1.2
- yarn v1.3.2

## install

```
$ cd /path/to/this/
$ yarn
```

## 書き方
- [api blue print](https://apiblueprint.org/) の形式で書いてください。
- 書き終わったら以下のコマンドを実行し、 index.html を生成してください。

```
$ yarn run build
$ open index.html
```

## mock サーバーの立ち上げ
mock server を立ち上げることで、 api サーバーが完成する前に、json のやりとりができます。

```
$ yarn run dev_server
```

localhost:3002 番にサーバーが立ち上がるように設定しています。

### リクエスト例

```
POST: /items
curl -H "Content-Type: application/json" -X POST -d '{"title":"カバン"}' http://localhost:3002/items/

GET: /items
curl -H "Content-Type: application/json" -X GET http://localhost:3002/items

PUT: /items/1
curl -H "Content-Type: application/json" -X PUT -d '{"title": "綺麗なカバン"}' http://localhost:3002/items/1
```


## 参考資料
- [aglioとdrakovでAPI仕様書とMockを生成する手順](http://takemikami.com/2017/01/05/agliodrakovAPIMock.html)
