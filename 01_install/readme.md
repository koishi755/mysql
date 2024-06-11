[2.5.1 MySQL Yum リポジトリを使用して MySQL を Linux にインストールする](https://dev.mysql.com/doc/refman/8.0/ja/linux-installation-yum-repo.html)

[MySQL Community Downloads](https://dev.mysql.com/downloads/repo/yum/)


# 1 MySQL Yum リポジトリの追加

MySQL Yum リポジトリをダウンロードします。

```
wget https://dev.mysql.com/get/mysql80-community-release-el7-10.noarch.rpm
```

<br>

MySQL Yum リポジトリをシステムのリポジトリリストに追加します。<br>


```
yum localinstall mysql80-community-release-el7-10.noarch.rpm
```

<br>

インストールできるバージョンなどを確認します。

```
yum info mysql-community-server
```

<br>

MySQLをインストールします。

```
yum install -y mysql-community-server
```

<br>

インストール後、バージョンを確認します。

```
mysqld --version
```

<br>


MySQLをスタートします。

```
systemctl start mysqld
```

<br>

MySQLが起動しているか確認します。

```
systemctl status mysqld
```

<br>

サーバー起動時にMySQLが起動するよう設定します。<br>


```
systemctl enable mysqld
```

[02_初期設定](https://github.com/koishi755/mysql/blob/main/02_%E5%88%9D%E6%9C%9F%E8%A8%AD%E5%AE%9A/readme.md)
