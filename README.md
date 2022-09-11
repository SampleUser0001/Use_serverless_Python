# Use_serverless_Python
serverlessを使ってみる

## 初期化

``` bash
sls create --template aws-python3 --name Use_serverless_Python --path app
```

## デプロイ

``` bash
sls deploy -v
```

## 実行

``` bash
# 関数名serverless.yml-functionsの下に紐付いている値を設定する。
function_name=hoge
input_filepath=event.json
sls invoke --function ${function_name} -p ${input_filepath}
```

## 削除

``` bash
sls remove -v
```