# SQLAlchemy

Object-relational-mapping is the idea of being able to write queries using the object-oriented paradigm of your preferred programming language. So, ORMs (object relational mappers) are basically libraries that try to implement this functionality in your choice of programming language. Examples are : [SQLAlchemy](https://www.sqlalchemy.org/),[Django ORM](https://www.fullstackpython.com/django-orm.html)
   - why are ORMs cool: 
     - You get to write in the language you are already using anyway.
     - Abstraction : It abstracts away the database system so that switching from MySQL to PostgreSQL for example, becomes easy.
     - Depending on the ORM you get a lot of advanced features such as support for transactions, connection pooling, migrations(schema), seeds, streams, etc
     - Optimization: Many of the queries you write will perform better than if you wrote them yourself.
   - what problems to ORMs solve?
     - ORM implementation classes know how to write vendor-specific SQL, so you don't have to.
     - (From DevOps perspective)Deployment: Pushing the app that can roll out its own database schema from its own code is a modern approach when everything including infrastructure should be a code.
     - Schema migrations : 
Schema migrations, for example when you need to add a new column to an existing table in your database, are not technically part of ORMs. However, since ORMs typically lead to a hands-off approach to the database, libraries to perform schema migrations often go hand-in-hand with ORM usage on web application projects. You can for example, automate migrations for SQLAlchemy based changes in database using [Alembic](https://alembic.sqlalchemy.org/en/latest/).

## How to use 

Code example:
 ```python
import os
 
from sqlalchemy import Column, DateTime, String, Integer, ForeignKey, func
from sqlalchemy.orm import relationship, backref
from sqlalchemy.ext.declarative import declarative_base

Base = declarative_base()
class Department(Base):
    __tablename__ = 'department'
    id = Column(Integer, primary_key=True)
    name = Column(String)
    
class Employee(Base):
    __tablename__ = 'employee'
    id = Column(Integer, primary_key=True)
    name = Column(String)
    hired_on = Column(DateTime, default=func.now())
    
db_name = 'alembic_sample.sqlite'
if os.path.exists(db_name):
    os.remove(db_name)
 
from sqlalchemy import create_engine
engine = create_engine('sqlite:///' + db_name)
 
from sqlalchemy.orm import sessionmaker
session = sessionmaker()
session.configure(bind=engine)
Base.metadata.create_all(engine)
```

## Resources 

- [Basic tutorial from tutorialspoint](https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_introduction.htm)
    - This tutorial gives simple examples for using SQLAlchemy for queries,joins deletes etc. and then mentions how to declare tables in class format , creating sessions and adding objects etc.
- [SQLAlchemy official docs](https://docs.sqlalchemy.org/en/13/orm/tutorial.html) with SQLAlchemy tutorial mentioning basic details like Querying , join , sessions etc.
- [This article](https://www.fullstackpython.com/sqlalchemy.html) mentions all the resources related to using SQLAlchemy with other application frameworks like Flask.


## Pain Points 
SQLAlchemy is an open source library which still has some bugs and upgrades with alembic tend to have restrictions about which schema changes can be done with that.

