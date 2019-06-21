# buildまでの手順
Dockerfileをvue, nginxごとに作成し、ルートにあるdocker-composeで紐付け。
そのあとはvueのコンテナに入り、以下のコマンドでwebpackなどなどインストール。
## ローカル
docker-compose build
docker-compose up
docker-compose ps # コンテナ名確認。
docker exec -it vue_docker_vue_1 sh #ログイン
## ホスト内部(/app内で以下のコマンド)
### 最初の一回
/app # vue init webpack (data/www以下にwebpackの諸々が生成)
/app # npm install (モジュールのインストール)
/app # npm run build  (data/www/distディレクトリが生成。ここにvueのwelcome pageができる。localhost:9000でアクセス。)

##次回以降
docker-compose up
のみでおっけー
