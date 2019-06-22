
## ローカル

```
docker-compose build
docker-compose up
docker-compose ps # コンテナ名確認。
docker exec -it (vue用のコンテナ名) sh #ログイン
```

## ホスト内部(/app内で以下のコマンド)
もしくはdocker-compose —rm run (サービス名: vue) コマンド 
### 最初の一回
```
/app # vue init webpack 
```
data/www以下にwebpackの諸々が生成 webpack+vue-louder( Vue コンポーネントをプレーンな JavaScript モジュールに変換する webpack の loader)のセット

以下yarnではなくnpm選択
```
/app # npm install 
```
モジュールのインストール
data/www/distディレクトリが生成。
webpackを通してコンパイルされた生成物がここにできる(vueのwelcome page)localhost:9000でアクセス。

・コーディングはsrc以下
・変更したら npm run script
・プリコンパイルみたいに圧縮してコンパイルってしたものがdist以下に入る(localhostで表示するもの)

##次回以降 docker-compose up のみでおっけ
