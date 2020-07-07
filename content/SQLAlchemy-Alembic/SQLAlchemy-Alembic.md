SQLAlchemy and Alembic

What are ORMs and why are they cool?
What specific challenges do they solve (ie migrations)?
How does Alembic work?

# SQLAlchemy
- What are ORMs and why are they cool?

Object-relational-mapping is the idea of being able to write queries using the object-oriented paradigm of your preferred programming language. So, ORMs (object relational mappers) are basically libraries that try to implement this functionality in your choice of programming language.
   - why are ORMs cool: 
     - You get to write in the language you are already using anyway.
     - Abstraction : It abstracts away the database system so that switching from MySQL to PostgreSQL for example, becomes easy.
     - Depending on the ORM you get a lot of advanced features such as support for transactions, connection pooling, migrations(schema), seeds, streams, etc
     - Optimization: Many of the queries you write will perform better than if you wrote them yourself.
   - what problems to ORMs solve?
     - ORM implementation classes know how to write vendor-specific SQL, so you don't have to.
     - (From DevOps perspective)Deployment: Pushing the app that can roll out its own database schema from its own code is a modern approach when everything including infrastructure should be a code.
     -Schema migrations : 
Schema migrations, for example when you need to add a new column to an existing table in your database, are not technically part of ORMs. However, since ORMs typically lead to a hands-off approach to the database, libraries to perform schema migrations often go hand-in-hand with ORM usage on web application projects.
   

Duplicate this page when creating a new wiki entry. 
![](https://www.fullstackpython.com/img/visuals/orm-examples.png)

Write an introduction for the topic you are covering. Think about what information does a user need to know to understand the fundamentals of the topic. Diagrams and flowcharts are a plus. 


## How to use 
Outline common uses of this topic, focusing on real life deployments and examples. Link to articles and videos to provide more information.

Bonus points for making it Insight specific.


## Resources 
- Everyone has to start somewhere, provide a short blurb for ANY turorials you found helpful, link to the tutorial, and any connected Codebases. 
- Youtube videos, Important documentation, etc.
- Please don't include out of date / bad resources.  This should be a best of list with

Example:
- [Some really awesome tutorial](https://towardsdatascience.com/getting-started-with-apache-airflow-df1aa77d7b1b)
    - This tutorial is about XYZ...


## Pain Points 
Identify current problems and paint points surround this topic / tool. What problems are people looking to solve around or with this topic/tool?

Example:
- **Something painful about this topic**
This is really annoying when it happens.  The reason for it is people need to write better code.  In order to get around it, write better code.



