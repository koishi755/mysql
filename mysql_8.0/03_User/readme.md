# アカウントの作成


アカウント作成

```
CREATE USER '<ユーザー名>'@'<ホスト名>' IDENTIFIED BY '<パスワード>';
```

<br>

権限付与

```
GRANT ALL ON <DB名>.<テーブル名> TO '<ユーザー名>'@'<ホスト名>' WITH GRANT OPTION;
```

<br>


実行例
```
CREATE USER 'testuser'@'%' IDENTIFIED BY 'password';
```

```
GRANT ALL ON *.* TO 'testuser'@'%' WITH GRANT OPTION;
```
