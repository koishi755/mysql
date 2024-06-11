# 1 識別子の大文字と小文字の区別


MySQLのデータストアの削除

```
cp /var/lib/mysql /var/tmp/mysql
```

```
rm -rf /var/lib/mysql
```

```
rm -f /var/log/mysql/mysqld.log
```


```
touch /var/log/mysql/mysqld.log
```

```
chown mysql:mysql /var/log/mysql/mysqld.log
```

```
vim /etc/my.cnf.d/mysql-server.cnf
```


```
# /etc/my.cnf.d/mysql-server.cnf
[mysqld]
lower_case_table_names=1
```


# 初期化


```
mysqld --defaults-file=/etc/my.cnf --initialize --user=mysql --console
```

ファイルが作成されているか確認


```
ls -l /var/lib/mysql
```


```
systemctl start mysqld
```





