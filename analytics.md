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


<p><img align="center" src="https://github.com/msandfor/DP-900/blob/main/assets/DW.PNG" alt="Data Warehouse"></p>
<p align="center"></p>

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
OLTP is used for transactional workloads, such as:
* Performing e-commerce transactions
* Tracking inventory management systems

<p><img align="center" src="https://github.com/msandfor/DP-900/blob/main/assets/olap-data-pipeline.png" alt="OLAP"></p>
<p align="center"></p>

**OLAP**
An application to perform data mining on historic data collected from multiple relational and non-relational sources is an example of an OLAP workload.
* OLAP applications often manipulate data based on complex queries. Data mining queries are complex multidimensional queries that are designed to discover insights from the data that are not immediately apparent.
* An application to provide loosely normalized data to support report generation is an example of an OLAP workload. Companies will often maintain live data for transactional processing and a separate copy of historic data for analysis and report generation. This prevents analytic processing from interfering with the performance during transactional processing.
* Online analytical processing (OLAP) systems are designed to perform complex analysis and provide business intelligence. 
OLAP is used for analytical workloads, such as:
* Generating complex ad-hoc reports that include several aggregations 
* Performing big data analysis on NoSQL database Online transaction processing (OLTP) systems are designed to perform business transactions as they occur.
 
<p><img align="center" src="https://github.com/msandfor/DP-900/blob/main/assets/star-schema-example1.png" alt="Star Schema"></p>
<p align="center"></p>

**Star schema** is a mature modeling approach widely adopted by relational data warehouses. It requires modelers to classify their model tables as either dimension or fact.

Dimension tables describe business entities—the things you model. Entities can include products, people, places, and concepts including time itself. The most consistent table you'll find in a star schema is a date dimension table. A dimension table contains a key column (or columns) that acts as a unique identifier, and descriptive columns.

Fact tables store observations or events, and can be sales orders, stock balances, exchange rates, temperatures, etc. A fact table contains dimension key columns that relate to dimension tables, and numeric measure columns. The dimension key columns determine the dimensionality of a fact table, while the dimension key values determine the granularity of a fact table. For example, consider a fact table designed to store sale targets that has two dimension key columns Date and ProductKey. It's easy to understand that the table has two dimensions. The granularity, however, can't be determined without considering the dimension key values. In this example, consider that the values stored in the Date column are the first day of each month. In this case, the granularity is at month-product level.

Generally, dimension tables contain a relatively small number of rows. Fact tables, on the other hand, can contain a very large number of rows and continue to grow over time.

A **snowflake** dimension is a set of normalized tables for a single business entity. For example, Adventure Works classifies products by category and subcategory. Categories are assigned to subcategories, and products are in turn assigned to subcategories. In the Adventure Works relational data warehouse, the product dimension is normalized and stored in three related tables: DimProductCategory, DimProductSubcategory, and DimProduct.

Processing data as it arrives is called streaming. Buffering and processing the data in groups is called batch processing.

An example of **batch processing** is the way that votes are typically counted in elections. The votes are not entered when they are cast, but are all entered together at one time in a batch.

Advantages of batch processing include:

Large volumes of data can be processed at a convenient time.
It can be scheduled to run at a time when computers or systems might otherwise be idle, such as overnight, or during off-peak hours.
Disadvantages of batch processing include:

The time delay between ingesting the data and getting the results.
All of a batch job's input data must be ready before a batch can be processed. This means data must be carefully checked. Problems with data, errors, and program crashes that occur during batch jobs bring the whole process to a halt. The input data must be carefully checked before the job can be run again. Even minor data errors, such as typographical errors in dates, can prevent a batch job from running.
An example of an effective use of batch processing would be a connection to a mainframe system. Vast amounts of data need to be transferred into a data analysis system and the data is not real-time. An example of ineffective batch-processing would be to transfer small amounts of real-time data, such as a financial stock-ticker.

The most appropriate use case for **Azure Synapse Analytics** is to perform very complex queries and aggregations on a large amount of relational data. 
* You can provision Synapse SQL pools to quickly execute complex queries across multiple computer nodes thanks to the Synapse SQL massively parallel processing (MPP) architecture. 
* Azure Synapse Analytics models and serves data. 
* You can load relational data ingested from Azure Data Factory in Azure Synapse Analytics using Synapse SQL pool, and also read unstructured data stored in Azure Data Lake Storage using Polybase. 
* Combining both relational and unstructured data, you can perform complex analytics and serve data for later stages.

The most appropriate use case for **Power Bl** is to create dashboards and data visualizations from tabular data.
Power BI visualizes data. You can build interactive reports and dashboards with Power Bl, allowing business users to analyze this data and deliver insights throughout your organization.

The most appropriate use case for **Azure Data Lake Storage** is to store massive amounts of unstructured data in a hierarchical structure.
* Azure Data Lake Storage stores raw data. You can store raw, unstructured data, such as text files, logs, and images, to be processed quickly at later stages.
* Azure Data Lake Storage Gen2 is built on top of Azure Blob storage, combining the features of the previous generation of Azure Data Lake Storage with Azure Blob storage.
* Azure Data Lake Storage is capable of storing a large amount of data in a cost-effective way. 
* Azure Data Lake Storage can store large amounts of data, like hundreds of terabytes and more, and you only pay for what you use. 
* You can reduce the storage cost even more by using features such as storage lifecycle to archive or move data that is not used frequently to cheaper storage tiers.
* Azure Data Lake Storage enables hierarchical namespace compatible with Hadoop Distributed File System (HDFS). 
* Azure Data Lake Storage provides a layer to access Azure Blob Storage data as an HDFS storage, including support to organize files in directories and subdirectories, allowing you to quickly examine large quantities of data.

The most appropriate use case for Azure SQL Database is to serve as data storage for online transactional processing (OLTP) workloads.

**Azure HDlnsight** is a big data processing service used to provision and manage a cluster of open-source analytics solutions such as Apache Spark, Hadoop, and Kafka.

**Azure Databricks** is a complete platform for big data processing, streaming, and machine learning optimized for the Microsoft Azure cloud services platform and built on top of Apache Spark.
* Azure Databricks can process batch and streaming processing workloads. You can also perform real-time data processing and event streaming from Azure Event Hubs with Azure Databricks.
* Azure Databricks provides an interactive workspace for exploration and data visualization.
* Azure Databricks provides a workspace for collaboration between data scientists, data engineers, and business analysts.
* You can run notebooks in R, Python, Scala, or SQL, and interact with the data very quickly.

**Azure Data Factory** ingests data from the source. You can ingest data from both relational data and non-structured data from multiple sources with Azure Data Factory.


**Azure Analysis Services** is a service used to build multidimensional or tabular models used by online analytical processing (OLAP) queries. You can combine data from multiple sources, like Azure Synapse Analytics, Azure Data Lake Store, Azure Cosmos DB, and others to build the tabular models.

You should use PolyBase. PolyBase is a feature present in SQL Server and Azure Synapse Analytics capable of reading data from Hadoop Distributed File System (HDFS)•compatible storage by using T-SQL queries. You can create an external table with an external data source to map the parquet format stored in Azure Data Lake Storage.You can query this external table with T-SQL and join it to other tables.

While you can read data from Azure Data Lake Storage parquet files, you cannot use T-SQL queries to read this data in Azure Data Factory.

Azure Databricks and Azure HDlnsight: These services are capable of reading data from Azure Data Lake Storage by using notebooks.

Azure Data Factory can load data from Azure Blob Storage, Azure Data Lake Storage, Azure Cosmos DB, and Azure Synapse Analytics. You can even load data from services outside Azure, such as Amazon 53.

Azure Data Factory can export data to Azure Data Lake Storage, Azure Synapse Analytics, and many other destinations, such as Azure SQL Database, Azure Blob Storage, and Azure Cosmos DB.

Azure Data Factory can run SQL Server Integration Service (SSIS) packages using the Execute SSIS Package activity, To use the Execute SSIS Package activity, you need to configure the Azure-SSIS
integration runtime (IR).

You use the **Power 81 Report Builder** to author and publish paginated reports. You create a paginated report by creating a report definition that specifies what data to retrieve, where to get it, and how to display it. The report is generated by the report processor when you run the report. You can preview the report in Report Builder before publishing it to the Power BI service.

**Power Bl Dashboard** is a single page on which your visualizations are posted as tiles on the dashboard to display information. A dashboard allows you to show important business metrics at a glance.

* Each report page displayed on a dashboard is based on a single dataset.

* An interactive report can be created from one dataset only. The reports can be created from the same dataset or a different dataset, but each report will be based on one dataset.

* Report pages are pinned to the dashboard from interactive reports.

* A dashboard can include pages pinned from multiple reports.

* Dashboard content is not limited to cloud data only. Content can include cloud and on-premises data. This gives you an easy way to compare data from various sources.

* One dashboard can be identified as your featured dashboard. After you declare a featured dashboard, this is the dashboard that will be displayed initially when you open the Power Bl service. You can change the featured dashboard at any time. 


The **Power Bl service** is a set of analysis and display tools that lets you create visuals based on your data. This includes Power Bl Desktop and Power Bl Dashboard.

**Power Bl Desktop** is used to create interactive reports, typically for publishing in Power Bl Dashboard.

You can include tiles as visualizations based on underlying data and along with standalone tiles, which can include:
* Text boxes
* Images
* Videos
* Streaming data
* Web content

The primary difference between these and other types of visualizations is that they do not link you to additional data or information. Tiles with underlying data include:
* Interactive reports
* Datasets
* Dashboards
* Excel worksheets
* Server Reporting Services (SSRS)
This is a partial list of the types of tiles supported.

**Power Bl apps** are used to create visualizations.

An app is a collection of ready-made visuals pre-arranged on reports and dashboards. Power Bl service includes several apps already defined for you. This includes apps available for various online services.

A report based on a single dataset generated using the Power BI Desktop as a collection of one or more pages of visuals is an interactive report. **An interactive report** will have one or more pages of visuals. Once the Power is published, the report pages can be used as tiles on a dashboard.

A unique combination of data pulled from various sources and used to create a visualization is referred to as a **dataset**. A dataset can include data from one or more databases, spreadsheets, flat files, and other sources, including both cloud-based and on-premises sources. Each unique combination is considered a different dataset.

**A tile** is a rectangular box that contains a single visual for use with a report or dashboard that supports user interaction. The visual can be custom content, content from a pre-defined app, or standalone tile content.

**A paginated report** is created in Power BI Report Builder from a report definition that specifies what data to retrieve, where to get it, and how to display it.

**A dashboard** is a single-page canvas to which you can pin tiles containing visualizations.

You should use **Power BI service** to create an app workspace and share its dashboard. Power BI service allows you to create an app workspace and share reports and dashboards. You can create a dashboard from reports in Power Bl service.

Power BI desktop allows you to create reports and publish them to an app workspace in Power BI service. 

You can create dashboards from reports.

You only need Power BI service to create a workspace and share its dashboard.

Power BI mobile app allows you to view reports and dashboard that are shared with you.

You should create a report on Power Bl Desktop. In a common workflow, you begin by connecting to data sources and building a report in Power Bl Desktop. 

You can also create reports on Power Bl service but with limited access to data sources.

Then, you should share a report on Power Bl service. You can publish and share reports on a Power Bl service workspace to make it available to end users.

Finally, you should view and interact with reports on Power Bl mobile. After a report is shared on Power Bl service, you can view and interact with this report using Power Bl mobile. You can use Power Bl service to interact and view reports with end users with desktop access only.

Power Bl mobile apps can only be used to view and interact with reports.

