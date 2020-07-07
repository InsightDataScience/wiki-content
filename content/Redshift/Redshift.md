# What is Amazon Redshift?
Amazon Redshift is a cloud-based data warehouse designed for large scale data sets. It was created to take on a lot of the issues previous data warehouses had and drastically improve on them. It does this with specific design decisions such as being columnar focused, having the ability to scale horizontally across multiple nodes, and massively parallel processing. Each of these specific design decisions has allowed AWS to develop a data storage system that operates very differently from your traditional RDBMS.

# High-Level Architecture
### Column-oriented database
As opposed to traditional database management systems, Redshift stores data by column. By partitioning data column-wise each time, you can retrieve a value, which also implies that a single value per partition reduces the load from the hard disk — thus resulting in faster speeds for massive amounts of data. In addition, with Redshift there’s also the concept of compression.
By compressing columns that are the same value it further improves the I/O because all the data is the same data type per column. This does require the developer to set the correct compression type per the data type.
### Redshift clustering
Every redshift cluster comprises of multiple machines which store a fraction of the data. These machines work in parallel, saving data so we can work upon it efficiently. Here, Redshift has some compute nodes that are managed by leader nodes to manage data distribution and query execution among the computing nodes. With this fraction dataset assigned to each node, Redshift performs efficiently. This also makes it horizontally scalable. Larger organizations can even use Redshift to operate with data in petabytes and beyond.
### Massive Parallel Processing (MPP)
In order to process data faster, Redshift employees the use of multiple compute nodes which allows the work to be broken up across nodes (depending on distribution), which can improve performance. This allows the Redshift architecture to offer maximum processing in minimum time.

<p align="center"> <img src="assets/AmazonRedshift.png" width="800" height="500"> </p>

## How to use 
Outline common uses of this topic, focusing on real life deployments and explames. Link to articles and videos to provide more information. 

Bonus points for making it Insight specific.


## Resources 
- Medium article: Building a Data Warehouse on Amazon Redshift [Link](https://medium.com/better-programming/building-a-data-warehouse-on-amazon-redshift-49a620a5392f)


## Pain Points 
- Identify current problems and paint points surround this topic / tool. What problems are people looking to solve around or with this topic/tool?
- 



