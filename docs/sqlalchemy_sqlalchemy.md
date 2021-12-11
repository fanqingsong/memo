
# SQLAlchemy SQLAlchemy

## Comparision 

[comparison with others](https://medium.com/pragmatech/orm-for-python-b63cfbc39e7f)

[comparison with others](https://www.pythoncentral.io/sqlalchemy-vs-orms/)

## Reference

[Session](https://docs.sqlalchemy.org/en/14/orm/session_api.html?highlight=session#sqlalchemy.orm.Session)

[Relation](https://docs.sqlalchemy.org/en/14/orm/relationships.html)

[Column](https://docs.sqlalchemy.org/en/14/core/metadata.html?highlight=column#sqlalchemy.schema.Column)

[DATA TYPE](https://docs.sqlalchemy.org/en/14/core/type_basics.html#generic-types)


## DATABASE URL

[official](https://docs.sqlalchemy.org/en/14/core/engines.html#database-urls)

### SCHEMA
```
dialect+driver://username:password@host:port/database
```

### MySQL
```
# default
engine = create_engine('mysql://scott:tiger@localhost/foo')

# mysqlclient (a maintained fork of MySQL-Python)
engine = create_engine('mysql+mysqldb://scott:tiger@localhost/foo')

# PyMySQL
engine = create_engine('mysql+pymysql://scott:tiger@localhost/foo')
```

### sqlite
```
# Unix/Mac - 4 initial slashes in total
engine = create_engine('sqlite:////absolute/path/to/foo.db')

# Windows
engine = create_engine('sqlite:///C:\\path\\to\\foo.db')

# Windows alternative using raw string
engine = create_engine(r'sqlite:///C:\path\to\foo.db')

# memory
engine = create_engine('sqlite://')
```
