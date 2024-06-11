# 1 ユーザー作成

以下のコマンドを実行し、新規ユーザを作成します。

```
CREATE USER <ユーザー名> IDENTIFIED BY '<パスワード>';
```

<br>


実行例

```
CREATE USER testuser1 IDENTIFIED BY 'Init123-';
```


<br>

# 2 権限の付与

以下のコマンドを実行し、権限を付与します。

```
GRANT ALL ON '<DB名>'.'<テーブル名>' TO '<ユーザー名>'@'<ホスト名>';
```

<br>

以下はtestUserに全ての権限を与える

```
GRANT ALL ON *.* TO testuser1;
```

# 3 ユーザー情報の変更



```
ALTER USER 'ユーザー'@'%'  IDENTIFIED WITH mysql_native_password BY 'パスワード';
```


```
flush privileges;
```

```
show grants for 'ユーザー名'@'ホスト名';
```
