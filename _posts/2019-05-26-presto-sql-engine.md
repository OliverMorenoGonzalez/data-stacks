# One SQL to rule them all.

We are going to talk about Apache Presto and Presto version from Starburstdata.
This tutorial is a friendly introduction, without too much deep tech terms later I will prepare a large version.

Apache Presto is a SQL Engine, It is use for queries across different data sources, high performance queries over gigabytes and petabytes of data.It is ideal for Big Data.

Presto was designed to handle data warehousing and analytics: data analysis, aggregating large amounts of data and producing reports. These workloads are often classified as Online Analytical Processing (OLAP).

Presto was not designed to handle Online Transaction Processing (OLTP).

I am going to use the Presto version from Starburstdata because its Docker Image is perfect, fast configuration and start playing around with Presto.

# Advantages of Presto:

1) SQL over any data source using connectors avalaible (there are a lot) or creating connectors. There isn't more need for different SQL implementation. 
"One SQL to rule them all."

2) Separation of Storage and Compute. This allow easily scale base in your analytics need, saving tons of money.

3) Deploy anywhere, on clouds, local or virtualized environments.

4) SQL with new operations (extended) and create with performance philosophy first.

5) Easy to install and debug.

6) High security and It is possible configure it.

Next tutorial: Architecture.
