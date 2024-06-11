# 1 識別子の大文字と小文字の区別


MySQLのデータストアの削除

```
cp -rp /var/lib/mysql /var/tmp/mysql
```

```
rm -rf /var/lib/mysql
```

```
rm -f /var/log/mysqld.log
```


```
touch /var/log/mysqld.log
```

```
chown mysql:mysql /var/log/mysqld.log
``` 




```
vim /etc/my.cnf
```


```
# /etc/my.cnf
datadir=/var/lib/mysql
socket=/var/lib/mysql/mysql.sock

log-error=/var/log/mysqld.log
pid-file=/var/run/mysqld/mysqld.pid

lower_case_table_names=1 # <-- 追記
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
systemctl restart mysqld
```


```
show variables where variable_name='lower_case_table_names';
```




