

[MySQL Community Downloads](https://dev.mysql.com/downloads/repo/yum/)

```
wget https://dev.mysql.com/get/mysql80-community-release-el7-10.noarch.rpm
```


```
yum localinstall mysql80-community-release-el7-10.noarch.rpm
```


```
yum info mysql-community-server
```

```
yum install -y mysql-community-server
```

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

