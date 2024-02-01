
# MySQL Commands

## commands

[Official](https://dev.mysql.com/doc/refman/8.0/en/tutorial.html)

[W3C](https://www.w3schools.com/mysql/mysql_sql.asp)

[Cheatsheet](https://devhints.io/mysql)


### Connect
```
mysql -h host -u user -p
```

### user management
```
SELECT user, host, plugin FROM mysql.user;


create user 'test_u'@'%' identified by 'kkSWhEpMVZ1xfaebJsRS';
CREATE USER 'percona'@'localhost' IDENTIFIED BY RANDOM PASSWORD;


grant select,insert,delete,update on db_test.* to 'test_u'@'%' ;


ALTER USER 'root'@'localhost' IDENTIFIED BY 'new_password';
ALTER USER 'root'@'localhost' IDENTIFIED BY RANDOM PASSWORD;

DROP USER 'jack'@'localhost';
```

### delete foreign key
```
show create table table_name


ALTER TABLE tb_emp9 DROP FOREIGN KEY fk_emp_dept;
```


