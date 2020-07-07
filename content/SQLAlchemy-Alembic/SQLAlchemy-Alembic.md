SQLAlchemy and Alembic

What are ORMs and why are they cool?
What specific challenges do they solve (ie migrations)?
How does Alembic work?

# SQLAlchemy
- What are ORMs and why are they cool?

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
   

 
![](https://www.fullstackpython.com/img/visuals/orm-examples.png)

Write an introduction for the topic you are covering. Think about what information does a user need to know to understand the fundamentals of the topic. Diagrams and flowcharts are a plus. 


## How to use 
- Installation : for pyhon ,it is [pip install SQLAlchemy](https://pypi.org/project/SQLAlchemy/)
>>> from sqlalchemy import create_engine

>>> engine = create_engine('sqlite:///:memory:', echo=True)


## Resources 


- [Basic tutorial from tutorialspoint](https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_introduction.htm)
    - This tutorial gives simple examples for using SQLAlchemy for queries,joins deletes etc. and then mentions how to declare tables in class format , creating sessions and adding objects etc.


## Pain Points 
Identify current problems and paint points surround this topic / tool. What problems are people looking to solve around or with this topic/tool?

Example:
- **Something painful about this topic**
This is really annoying when it happens.  The reason for it is people need to write better code.  In order to get around it, write better code.



