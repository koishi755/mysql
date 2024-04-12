# アカウントの作成

```
CREATE USER '<ユーザー名>'@'<ホスト名>'
  IDENTIFIED BY '<パスワード>';
GRANT ALL
  ON <DB名>.<テーブル名>
  TO '<ユーザー名>'@'<ホスト名>'
  WITH GRANT OPTION;
```

```
CREATE USER 'testser'@'%'
  IDENTIFIED BY 'password';
GRANT ALL
  ON *.*
  TO 'testser'@'%'
  WITH GRANT OPTION;
```
