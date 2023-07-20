以下のサイトからインストールするバージョンのrpmを探します。

[MySQL Product Archives](https://downloads.mysql.com/archives/community/)

<br>

今回はバージョン5.7.16をダウンロードします。

![](./img/01.png)

<br>

以下のコマンドを実行し、rpmをダウンロードします。

```
wget https://downloads.mysql.com/archives/get/p/23/file/mysql-community-server-5.7.16-1.el6.x86_64.rpm
```

<br>


```bash
rpm -qpl mysql-community-server-5.7.16-1.el6.x86_64.rpm
```

```
service mysqld start
```


```
grep 'temporary password' /var/log/mysqld.log
```
