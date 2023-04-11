
# MySQL Install On WSL

## commands

[source](https://zhuanlan.zhihu.com/p/166444726)

### install
```
sudo apt-get install mysql-server
```

### start
```
sudo service mysql start
```

### login
```
mysql -u root -p
```

### open skip-grant-tables firstly
```
sudo vim /etc/mysql/mysql.conf.d/mysqld.cnf
```





