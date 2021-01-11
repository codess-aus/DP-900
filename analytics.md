## Describe an analytics workload on Azure (25-30%)
### Describe analytics workloads
* describe transactional workloads
* describe the difference between a transactional and an analytics workload
* describe the difference between batch and real time
* describe data warehousing workloads
* determine when a data warehouse solution is needed

### Describe the components of a modern data warehouse
* describe Azure data services for modern data warehousing such as Azure Data Lake, Azure Synapse Analytics, Azure Databricks, and Azure HDInsight
* describe modern data warehousing architecture and workload
Describe data ingestion and processing on Azure
* describe common practices for data loading
* describe the components of Azure Data Factory (e.g., pipeline, activities, etc.)
* describe data processing options (e.g., Azure HDInsight , Azure Databricks, Azure Synapse Analytics, Azure Data Factory)

### Describe data visualization in Microsoft Power BI
* describe the role of paginated reporting
* describe the role of interactive reports
* describe the role of dashboards
* describe the workflow in Power BI




Two common use cases for **Data Warehousing** are:
* You want to generate reports from historical data without impacting transactional processing.
* You want to provide a platform for data mining.

Data warehousing lets you consolidate data from multiple sources for analysis and reporting. Data stores are optimized for read operations with few, if any, writes performed on the data. There are typically no locking requirements in a data warehouse.

**OLTP** systems are used to record day-to-day business activities and interactions as they occur. This includes activities such as orders taken, services performed, and payments received or made. 
* In an OLTP system, data is highly normalized with the schema strongly enforced on write. 
* OLTP systems are usually structured around a relational data store supporting transactional applications. 
* An OLTP workload has heavy write requirements with minimal (in comparison) read requirements. 
* In an OLTP environment, changes made are rolled back automatically if a transaction is not completed so that no transaction is left in a partially completed state. This is known as atomicity and is a requirement for OLTP.
* An application to process hundreds of user purchases per minute, including updates to inventory on hand, is an example of an OLTP workload. 
* OLTP applications are optimized for write operations and entering and updating data across multiple, related tables. Partial changes made to data are rolled back automatically if a transaction is not completed, so that no transaction is left in a partially completed state.
* An application to support warehouse sales and shipping for physical warehouses and multiple international locations is an example of an OLTP application. 
* OLTP transactions can be distributed geographically and supported by one or more relational database. This scenario requires a solution that supports consistent and reliable data writes. 


**OLAP**
An application to perform data mining on historic data collected from multiple relational and non-relational sources is an example of an OLAP workload.
* OLAP applications often manipulate data based on complex queries. Data mining queries are complex multidimensional queries that are designed to discover insights from the data that are not immediately apparent.
* An application to provide loosely normalized data to support report generation is an example of an OLAP workload. Companies will often maintain live data for transactional processing and a separate copy of historic data for analysis and report generation. This prevents analytic processing from interfering with the performance during transactional processing.
 
<p><img align="center" src="https://github.com/msandfor/DP-900/blob/main/assets/star-schema-example1.png" alt="Star Schema"></p>
<p align="center"></p>

**Star schema** is a mature modeling approach widely adopted by relational data warehouses. It requires modelers to classify their model tables as either dimension or fact.

Dimension tables describe business entities—the things you model. Entities can include products, people, places, and concepts including time itself. The most consistent table you'll find in a star schema is a date dimension table. A dimension table contains a key column (or columns) that acts as a unique identifier, and descriptive columns.

Fact tables store observations or events, and can be sales orders, stock balances, exchange rates, temperatures, etc. A fact table contains dimension key columns that relate to dimension tables, and numeric measure columns. The dimension key columns determine the dimensionality of a fact table, while the dimension key values determine the granularity of a fact table. For example, consider a fact table designed to store sale targets that has two dimension key columns Date and ProductKey. It's easy to understand that the table has two dimensions. The granularity, however, can't be determined without considering the dimension key values. In this example, consider that the values stored in the Date column are the first day of each month. In this case, the granularity is at month-product level.

Generally, dimension tables contain a relatively small number of rows. Fact tables, on the other hand, can contain a very large number of rows and continue to grow over time.
