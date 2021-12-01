
# SQLAlchemy Alembic

## commands

[reference](https://zhuanlan.zhihu.com/p/90106173)

[reference](https://www.cnblogs.com/blackmatrix/p/6236573.html)

[official](https://alembic.sqlalchemy.org/en/latest/tutorial.html)

### install
```
pip install alembic
```

### init
```
alembic init alembic
```

### create one revision
```
alembic revision -m "first create script"
```

### migration
```
alembic upgrade head：将数据库升级到最新版本。
alembic downgrade base：将数据库降级到最初版本。
alembic upgrade <version>：将数据库升级到指定版本。
alembic downgrade <version>：将数据库降级到指定版本。
alembic upgrade +2：相对升级，将数据库升级到当前版本后的两个版本。
alembic downgrade -2：相对降级，将数据库降级到当前版本前的两个版本。
```

### migration offline
```
alembic upgrade <version> --sql > migration.sql

alembic downgrade head:base --sql

alembic upgrade base:head --sql

```




