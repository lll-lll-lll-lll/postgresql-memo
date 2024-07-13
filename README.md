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
