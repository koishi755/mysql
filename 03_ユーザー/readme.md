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

# 2 ユーザー権限

## 2-1 権限の付与
以下のコマンドを実行し、権限を付与します。

```
GRANT ALL ON '<DB名>'.'<テーブル名>' TO '<ユーザー名>'@'<ホスト名>';
```

<br>

以下はtestUserに全ての権限を与える

```
GRANT ALL ON *.* TO testuser1;
```

<br>

## 2-2 ユーザー権限の確認

全ユーザーのリストを取得

```
SELECT User, Host FROM mysql.user;
```


ユーザー情報の確認

```
show grants for 'ユーザー名'@'ホスト名';
```



# 3 ユーザー情報の変更

パスワードの変更

```
ALTER USER 'ユーザー'@'%'  IDENTIFIED WITH mysql_native_password BY 'パスワード';
```

<br>

権限の付与などを即時更新

```
flush privileges;
```

<br>


