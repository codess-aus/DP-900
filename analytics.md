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



