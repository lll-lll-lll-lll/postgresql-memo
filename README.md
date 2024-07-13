# postgresql-memo
postgresqlに関する適当なメモ


データベースクラスタの初期化
```sh
mkdir -p /usr/local/pgsql/data
chown -R myuser:myuser /usr/local/pgsql
su - myuser
/usr/lib/postgresql/16/bin/initdb -D /usr/local/pgsql/data
```
