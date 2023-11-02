# 環境構築

dockerをダウンロード

あとは以下を実行
```
# イメージの作成
docker compose build
# データベースの作成
docker-compose run --rm web rails db:create
# マイグレート
docker-compose run --rm web rails db:migrate
```

新しくアプリを作るとき
```
docker-compose run web rails new . --force --database=postgresql
```

サーバーの立て方
```
docker compose up -d
```

サーバの削除
```
docker compose down
```