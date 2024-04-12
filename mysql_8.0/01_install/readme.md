# 1 MySQL Yum リポジトリの追加


RHEL7ベース

```
wget https://dev.mysql.com/get/mysql80-community-release-el7-11.noarch.rpm
```

<br>

```
yum localinstall mysql80-community-release-el7-11.noarch.rpm
```

<br>

MySQL Yum リポジトリが正常に追加されたことを確認

```
yum repolist enabled | grep "mysql.*-community.*"
```

<br>


# 2 リリースシリーズの選択

MySQL Yum リポジトリを使用する場合、デフォルトで最新の GA シリーズ (現在の MySQL 8.0) がインストール用に選択されます。次のコマンドでMySQL Yum リポジトリ内のすべてのサブリポジトリを表示できます。


```
yum repolist all | grep mysql
```

<br>

# 3 デフォルトの MySQL モジュールの無効化

 RHEL8 や Oracle Linux 8 などの EL8-based システムには、デフォルトで有効になっている MySQL モジュールが含まれています。 このモジュールを無効にしないかぎり、MySQL リポジトリによって提供されるパッケージがマスクされます。 含まれているモジュールを無効にして MySQL リポジトリパッケージを表示するには、次のコマンドを使用します (dnf 対応システムの場合は、コマンドの yum を dnf に置き換えます)

 
```
yum module disable mysql
```


# 4 MySQL のインストール



```
yum install mysql-community-server
```


# 5 MySQL Server の起動

```
systemctl start mysqld
```

```
systemctl status mysqld
```

```
systemctl enable mysqld
```

<br>


## 5-1 初期パスワードの確認

```
grep 'temporary password' /var/log/mysqld.log
```


## 5-2 ログイン

```
mysql -uroot -p
```

## 5-3 初期パスワードの変更

```
ALTER USER 'root'@'localhost' IDENTIFIED BY 'MyNewPass4!';
```

