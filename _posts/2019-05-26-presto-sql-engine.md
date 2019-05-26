# One SQL to rule them all.

We are going to talk about Apache Presto and Presto version from Starburstdata.
This tutorial is a friendly introduction, without too much deep tech terms later I will prepare a large version.

Apache Presto is a SQL Engine, It is use for queries across different data sources, high performance queries over gigabytes and petabytes of data.It is ideal for Big Data.

Presto was designed to handle data warehousing and analytics: data analysis, aggregating large amounts of data and producing reports. These workloads are often classified as Online Analytical Processing (OLAP).

Presto was not designed to handle Online Transaction Processing (OLTP).

I am going to use the Presto version from Starburstdata because its Docker Image is perfect, fast configuration and start playing around with Presto.

## Advantages of Presto:

1) SQL over any data source using connectors avalaible (there are a lot) or creating connectors. There isn't more need for different SQL implementation. 
"One SQL to rule them all."

2) Separation of Storage and Compute. This allow easily scale base in your analytics need, saving tons of money.

3) Deploy anywhere, on clouds, local or virtualized environments.

4) SQL with new operations (extended) and create with performance philosophy first.

5) Easy to install and debug.

6) High security and It is possible configure it.

# Architecture Apche Presto SQL Engine.

In Presto you have one coordinator (the brain) and multiple workers for query processing.

The coordinator accept SQL statements from client and parse, plan and schedule how SQL statement are going to be processed when It is done workers come into action.

Workers read data from data sources and finally combine them into one process which is return to client.

Presto have a metadata API (one component of Coordinator) to understand the relations from your data sources (How Data is been store in each source) and translate it to use the data, after this is done the rest of execution is agnostic to your data source.

## More advantages of Apache Presto:

1) Community driven open source project.

2) Huge community, It is used by a lot of huge companies, so there are experts or users out there you can reach, in some cases companies have share his knowledge to improve Apache Presto.

3) No vendor lock-in.

4) High performance ANSI SQL enine.

Next tutorial: Hands on Presto and practise
