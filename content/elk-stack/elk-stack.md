# ELK Stack
"ELK" is the acronym for three open source projects: 
- Elasticsearch, Logstash, and Kibana. Elasticsearch is a search and analytics engine. 
- Logstash is a server‑side data processing pipeline that ingests data from multiple sources simultaneously, transforms it, and then sends it to a "stash" like Elasticsearch. 
- Kibana lets users visualize data with charts and graphs in Elasticsearch. 

## Overview
The ELK stack consists of Elasticsearch, Logstash, and Kibana. Although they've all been built to work exceptionally well together, each one is an individual project run by the open-source company Elastic—which itself began as an enterprise search platform vendor. It has now become a full-service analytics software company, mainly because of the success of the ELK stack. Wide adoption of Elasticsearch for analytics has been the main driver of its popularity.

### Elasticsearch
Elasticsearch is a juggernaut solution for your data extraction problems. A single developer can use it to find the high-value needles underneath all of your data haystacks, so you can put your team of data scientists to work on another project. Consider these benefits:

#### Real-time data and real-time analytics
The ELK stack gives you the power of real-time data insights, with the ability to perform super-fast data extractions from virtually all structured or unstructured data sources. Real-time extraction, and real-time analytics. Elasticsearch is the engine that gives you both the power and the speed.

#### Scalable, high-availability, multi-tenant
With Elasticsearch, you can start small and expand it along with your business growth when you are ready. It is built to scale horizontally out of the box. As you need more capacity, simply add another node and let the cluster reorganize itself to accommodate and exploit the extra hardware. Elasticsearch clusters are resilient, since they automatically detect and remove node failures. You can set up multiple indices and query each of them independently or in combination.

#### Full text search
Under the hood, Elasticsearch uses Lucene to provide the most powerful full-text search capabilities available in any open-source product. The search features come with multi-language support, an extensive query language, geolocation support, context-sensitive suggestions, and autocompletion.

#### Document orientation
You can store complex, real-world entities in Elasticsearch as structured JSON documents. All fields have a default index, and you can use all the indices in a single query to get precise results in the blink of an eye.

### Logstash
Logstash is a tool for log data intake, processing, and output. This includes virtually any type of logs that you manage: system logs, webserver logs, error logs, and app logs. As administrators, we know how much time can be spent normalizing data from disparate data sources. We know, for example, how significantly Apache logs differ from NGINX logs.

#### Fast track over ETL
Rather than normalizing with time-sucking ETL (Extract, Transform, and Load), we recommend that you switch over to the fast track. Instead, you could spend much less time training Logstash to normalize the data, getting Elasticsearch to process the data, and then visualize it with Kibana. With Logstash, it's super easy to take all those logs and store them in one centralized location. The only prerequisite is a Java 8 runtime, and it takes just two commands to get Logstash up and running.

#### Powerful feature set
Using Elasticsearch as a backend datastore and Kibana as a frontend dashboard, Logstash will serve as the workhorse for storage, querying and analysis of your logs. Since it has an arsenal of ready-made inputs, filters, codecs, and outputs, you can grab hold of a very powerful feature-set with a very little effort on your part.

### Kibana
Kibana is your log-data dashboard. Get a better grip on your large data stores with point-and-click pie charts, bar graphs, trendlines, maps and scatter plots. You can visualize trends and patterns for data that would otherwise be extremely tedious to read and interpret. Eventually, each business line can make practical use of your data collection as you help them customize their dashboards. Save it, share it, and link your data visualizations for quick and smart communication.


## How to use 

The various components in the ELK Stack were designed to interact and play nicely with each other without too much extra configuration. However, how you end up designing the stack greatly differs on your environment and use case.

For a small-sized development environment, the classic architecture will look as follows:

![](assets/elk-stack.png "ELK Stack for small scale")

However, for handling more complex pipelines built for handling large amounts of data in production, additional components are likely to be added into your logging architecture, for resiliency (Kafka, RabbitMQ, Redis) and security (nginx):

![](assets/elk-stack1.png "ELK Stack for large scale")

## Resources 
- Elastic Stack Official Website - https://www.elastic.co/elastic-stack
- New Elastic Stack - https://www.elastic.co/blog/whats-new-in-elastic-stack-7-8-0-release
- Documentation Reference - https://qbox.io/blog/welcome-to-the-elk-stack-elasticsearch-logstash-kibana


## Installation

Follow the guide [here](https://logz.io/learn/complete-guide-elk-stack/#installing-elk) to install and configure the ELK Stack.

## Pain Points 
### The Challenge of Disparate Log Data -

#### No Consistency
The variety of systems and absence of standards means that it's difficult to be a jack-of-all trades.

- Logging is different for each app, system, or device.
- Specific knowledge is necessary for interpreting various types of logs.
- Variation in format makes it challenging to search.

#### No centralization
Simply put, log data is everywhere:

- Logs in many locations on various servers.
- Many locations of various logs on each server.
- SSH + GREP doesn’t scale or reach in multi-tenant and distributed environments.

#### Accessibility of Log Data
Much of the data is difficult to locate and manage. Although some of the log data may be highly valuable, many admins face these steep challenges:

- Access to data is often difficult.
- A high level of expertise is required to mine data.
- Logs can be difficult to find.
- Immense size of Log Data.

The ELK stack can help you address each of these challenges, and more. ELK is best for time-series data, --  anything with a time stamp such as you'll find in most web server logs, transaction logs, and stock data listings. To be intelligible, these logs usually need substantial clean-up.
