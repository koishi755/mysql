# 1 設定の流れ
## 1-1 設定ファイル

```
vim /etc/my.cnf
```

<br>

# 1-2 クライアントオプション

以下のように記述します。このオプションでは、MySQL接続時、DBを指定しないかった場合、Test_mydatabaseにデフォルトで接続されます。

```
# /etc/my.cnf

[client]
database=Test_mydatabase
```

<br>

# 1-3

MySQLを再起動し、設定を反映させます。

```
systemctl restart mysqld
```
