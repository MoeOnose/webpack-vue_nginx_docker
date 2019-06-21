# 参考記事
https://qiita.com/akashixi/items/2ebe9404c64a8854b4e5

# buildまでの手順
Dockerfileをvue, nginxごとに作成し、ルートにあるdocker-composeで紐付け。
そのあとはvueのコンテナに入り、以下のコマンドでwebpackなどなどインストール。
## ローカル
docker-compose build
docker-compose up
docker-compose ps # コンテナ名確認。
docker exec -it vue_docker_vue_1 sh #ログイン
## ホスト内部(/app内で以下のコマンド)
/app # vue init webpack
/app # npm install  
/app # npm run build