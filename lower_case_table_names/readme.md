# 1 データベースのバックアップを取得

特定のDBのバックアップを取得。

```
mysqldump -u root -p Test_mydatabase > Test_mydatabase.sql
```

<br>


または以下のように全てのDBを取得。


```
mysqldump -u root -p --all-databases > mysql-all-backup.sql
```


<br>

# 2 /var/lib/mysqlのバックアップ

MySQLのライブラリを削除

```
mv /var/lib/mysql /var/tmp/mysql
```

<br>

ログの削除

```
rm -f /var/log/mysqld.log
```

<br>

新しいログを作成

```
touch /var/log/mysqld.log
```


<br>

権限の付与

```
chown mysql:mysql /var/log/mysqld.log
``` 

<br>

設定ファイルの編集


```
vim /etc/my.cnf
```

<br>

lower_case_table_names=1 を追加します。

```
# /etc/my.cnf
datadir=/var/lib/mysql
socket=/var/lib/mysql/mysql.sock

log-error=/var/log/mysqld.log
pid-file=/var/run/mysqld/mysqld.pid

lower_case_table_names=1 # <-- 追記
```


# 3 MySQLの初期化


```
mysqld --defaults-file=/etc/my.cnf --initialize --user=mysql --console
```

ファイルが作成されているか確認


```
ls -l /var/lib/mysql
```


```
systemctl restart mysqld
```


```
show variables where variable_name='lower_case_table_names';
```


# 4 データベースの復元

特定のDBの復元

```
mysql -u root -p Test_mydatabase < Test_mydatabase.sql
```


<br>

全て復元

```
mysql -u root -p < mysql-all-backup.sql
```



