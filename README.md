# postgresql-memo
postgresqlに関する適当なメモ


データベースクラスタの初期化
https://www.postgresql.jp/docs/9.4/app-initdb.html
ディレクトリの親の権限がrootだと実行できないので、ユーザを変更して実行できるようにするためのコマンド
```sh
mkdir -p /usr/local/pgsql/data
chown -R myuser:myuser /usr/local/pgsql
su - myuser
/usr/lib/postgresql/16/bin/initdb -D /usr/local/pgsql/data
```


## バキューム処理についてまとめる
VACUUM処理は更新削処理の実行後に不要なデータを削除機能

なぜ不要なデータを削除する必要があるのか。
そもそも更新削除なら物理的にデータを更新削除すればこの処理は必要ではないのではないのか？
この疑問の答えはpostgresqlのアーキテクチャを理解すると納得する。



参考
https://gihyo.jp/dev/feature/01/dex_postgresql/0002
https://devcenter.heroku.com/ja/articles/postgresql-concurrency
