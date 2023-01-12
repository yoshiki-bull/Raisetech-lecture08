# 第8回課題
## DockerによるMySQLの構築を初めて行うひとのためのガイドプロジェクト
- 「docker -v」コマンドでDockerのバージョンが確認できる。
- イメージからコンテナはすでに出来上がっている状態。
- イメージは「Dockerfile」や「docker-compose.ymlファイル」で作成する。
- 「SQL文」において「;」はコマンドの終わりを意味する。
-  composeの場合、dockerイメージの作成・取得からdocker runまでをまとめて実行する。
-  「カラム」がキーワードのように見受けられた。
-  「select」コマンドでできることが多そうだった。

## hands-onの流れ
  1.__「docker compose up -d」__---コンテナの起動。    
  2.__「docker ps」__---コンテナの状態を確認。  
  3.__「docker compose exec db mysql  -uroot -p」__---MySQL(データベース)にログイン。  
  4.__「show databases;」__---データベースの一覧を確認。  
  5.__「use movie_list;」__---操作対象のデータベースを切り替える。  
  6.__「show tables;」__---テーブルの一覧を表示。  
  7.__「select * from movies;」__---moviesテーブルのレコードを確認。  
  8.__「insert into movies (name, director) values ("name(カラム)に入れるデータ", "director(カラム)に入れるデータ");」__  
  →指定したテーブルのカラムにデータを挿入。  
  9.__「select * from movies;」__---レコードの挿入結果を確認。  
  10.__「exit」__---MySQLからログアウト。  
  11.__「docker compose down」__---起動したDockerコンテナを停止。  
  12.__「docker ps」__---コンテナの状態を確認。