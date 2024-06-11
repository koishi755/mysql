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

```
systemctl start mysqld
```

```
systemctl status mysqld
```

```
systemctl enable mysqld
```

