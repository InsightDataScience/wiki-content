# What is Amazon Redshift?
Amazon Redshift is a cloud-based relational database system built on PostgreSQL principles. It’s optimized for performing online analytical processing (“OLAP”) queries efficiently over petabytes of data. The query handling efficiency is achieved through the combination of:
- highly parallel processing
- a columnar database design
- data compression of columns

# Architecture
The heart of each Redshift deployment is a cluster. Each cluster has a leader node and one or more compute nodes, all connected by high speed links. A leader node is the interface to your business intelligence application. It offers standard PostgreSQL JDBC/ODBC interfaces for queries and responses. It serves as the traffic cop directing queries from customer applications to the appropriate compute nodes, and manages the results returned. It also distributes ingested data into the compute nodes to build your databases.

<p align="center"> <img src="assets/AmazonRedshift.png"> </p>

The Dense Compute (DC) nodes are meant for speed of query execution, with less storage, and is best for high performance activities. It is implemented with SSD drives. The Dense Storage (DS) nodes are for storing and querying big data, using typical hard disk drives.

## How to use 
Outline common uses of this topic, focusing on real life deployments and explames. Link to articles and videos to provide more information. 

Bonus points for making it Insight specific.


## Resources 
- Medium article: Amazon Redshift: Data Warehousing for the Masses [Link](https://medium.com/intermix-io/amazon-redshift-data-warehousing-for-the-masses-ea1642dc63ea)


## Pain Points 
- Identify current problems and paint points surround this topic / tool. What problems are people looking to solve around or with this topic/tool?
- 



