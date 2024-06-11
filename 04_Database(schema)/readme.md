# 1 Database(スキーマ)とは？

スキーマ<br>
　MySQLにおいて、「スキーマ」という用語はデータベース全体の構造や設計を指します。スキーマにはテーブル、ビュー、インデックス、ストアドプロシージャ、トリガーなどが含まれます。また、MySQLの一部のドキュメントやGUIツールでは、データベースそのものを指して「スキーマ」という用語を使用することもあります。

<br>

# 2 Databaseの作成

## 2-1 現在存在するDatabase一覧を取得

```
SHOW DATABASES;
```

<br>

## 2-2 新規Databaseの作成

以下のSQLを実行し、Databaseを作成します。

```
CREATE DATABASE <Database名>;
```

<br>


実行例

```
CREATE DATABASE Test_mydatabase;
```

<br>

※Database名は大文字と小文字を区別しているようです。



# 3 データベースの移動

現在のデータベースの確認

```
SELECT DATABASE();
```

<br>

以下のコマンドを実行し、データベースを移動します。

```
Use <Database名>;
```

<br>


実行例


