# 1 Tableとは？

テーブル<br>
　テーブルは、データベース内にデータを保存するための構造です。テーブルは行と列から構成され、各行がデータのレコードを表し、各列がデータのフィールド（属性）を表します。例えば、ユーザー情報を格納する users というテーブルは以下のように定義されます。

<br>

# 2 Tableの作成

まず、テーブルを作成したいデータベースに移動します。

```
Use Test_mydatabase;
```


テーブルは以下のようなSQLを実行し作成します。

```
CREATE TABLE <テーブル名> (
    <カラム名１> <カラム１のタイプ>,
    <カラム名２> <カラム２のタイプ>,
    ...
);
```

<br>

実行例

```
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(50) NOT NULL,
    email VARCHAR(100) NOT NULL
);
```

