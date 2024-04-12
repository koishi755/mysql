# アカウントの作成

```
CREATE USER 'testser'@'%'
  IDENTIFIED BY 'password';
GRANT ALL
  ON *.*
  TO 'testser'@'%'
  WITH GRANT OPTION;
```
