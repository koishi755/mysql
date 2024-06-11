# 1 初期パスワードの変更

以下のコマンドを実行し、初期パスワードを確認します。

```
grep password /var/log/mysqld.log
```

<br>

以下のコマンドを実行して初期設定を行います。この際パスワードを変更を求められます。

```
mysql_secure_installation
```


<br>


# 別の方法のパスワード変更



MySQLに接続します。

```
mysql -uroot -p
```

<br>


```
use mysql
```


```
ALTER USER 'root'@'localhost' identified BY 'hoge';
```

```
flush privileges;
```



