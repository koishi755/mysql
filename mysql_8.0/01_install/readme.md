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

