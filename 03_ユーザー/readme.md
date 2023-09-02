# ユーザー作成

```
CREATE USER <ユーザー名> IDENTIFIED BY '<パスワード>';
```

<br>

# 権限の付与

```
GRANT ALL ON '<DB名>'.'<テーブル名>' TO '<ユーザー名>'@'<ホスト名>';
```

<br>

以下はtestUserに全ての権限を与える

```
GRANT ALL ON *.* TO testUser;
```


```
ALTER USER 'ユーザー'@'%'  IDENTIFIED WITH mysql_native_password BY 'パスワード';
```


```
flush privileges;
```

```
show grants for 'ユーザー名'@'ホスト名';
```
