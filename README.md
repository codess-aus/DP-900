# DP-900 Microsoft Azure Data Fundamentals

## Describe core data concepts (15-20%)
### Describe types of core data workloads
* describe batch data
* describe streaming data
* describe the difference between batch and streaming data
* describe the characteristics of relational data

### Describe data analytics core concepts
* describe data visualization (e.g., visualization, reporting, business intelligence (BI))
* describe basic chart types such as bar charts and pie charts
* describe analytics techniques (e.g., descriptive, diagnostic, predictive, prescriptive, cognitive)
* describe ELT and ETL processing
* describe the concepts of data processing

## Describe how to work with relational data on Azure (25-30%)
### Describe relational data workloads
* identify the right data offering for a relational workload
* describe relational data structures (e.g., tables, index, views)

### Describe relational Azure data services
* describe and compare PaaS, IaaS, and SaaS solutions
* describe Azure SQL database services including Azure SQL Database, Azure SQL

### Managed Instance, and SQL Server on Azure Virtual Machine
* describe Azure Synapse Analytics
* describe Azure Database for PostgreSQL, Azure Database for MariaDB, and Azure Database for MySQL

### Identify basic management tasks for relational data
* describe provisioning and deployment of relational data services
* describe method for deployment including the Azure portal, Azure Resource Manager templates, Azure PowerShell, and the Azure command-line interface (CLI)
* identify data security components (e.g., firewall, authentication)
* identify basic connectivity issues (e.g., accessing from on-premises, access with Azure VNets, access from Internet, authentication, firewalls)
* identify query tools (e.g., Azure Data Studio, SQL Server Management Studio, sqlcmd
utility, etc.)
Describe query techniques for data using SQL language
* compare Data Definition Language (DDL) versus Data Manipulation Language (DML)
* query relational data in Azure SQL Database, Azure Database for PostgreSQL, and Azure Database for MySQL

## Describe how to work with non-relational data on Azure (25-30%)
### Describe non-relational data workloads
* describe the characteristics of non-relational data
* describe the types of non-relational and NoSQL data
* recommend the correct data store
* determine when to use non-relational data

### Describe non-relational data offerings on Azure
* identify Azure data services for non-relational workloads
* describe Azure Cosmos DB APIs
* describe Azure Table storage
* describe Azure Blob storage
* describe Azure File storage

### Identify basic management tasks for non-relational data
* describe provisioning and deployment of non-relational data services
* describe method for deployment including the Azure portal, Azure Resource Manager templates, Azure PowerShell, and the Azure command-line interface (CLI)
* identify data security components (e.g., firewall, authentication, encryption)
* identify basic connectivity issues (e.g., accessing from on-premises, access with Azure VNets, access from Internet, authentication, firewalls)
* identify management tools for non-relational data

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

# Learning Path:

| Course | Length | Notes |
|-----|-----|----------|
| [Azure Data Fundamentals: Explore core data concepts](https://docs.microsoft.com/en-us/learn/paths/azure-data-fundamentals-explore-core-data-concepts/) | 1 hr 39 min | identify and describe core data concepts such as relational, non-relational, big data, and analytics, and explore how this technology is implemented with Microsoft Azure. You will explore the roles, tasks, and responsibilities in the world of data |
| [Azure Data Fundamentals: Explore relational data in Azure](https://docs.microsoft.com/en-us/learn/paths/azure-data-fundamentals-explore-relational-data/) | 1 hr 27 min | explore relational data offerings, provisioning and deploying relational databases, and querying relational data through cloud data solutions with Microsoft Azure |
| [Azure Data Fundamentals: Explore non-relational data in Azure](https://docs.microsoft.com/en-us/learn/paths/azure-data-fundamentals-explore-non-relational-data/) | 2 hr 24 min | explore non-relational data offerings, provisioning and deploying non-relational databases, and non-relational data stores with Microsoft Azure |
| [Azure Data Fundamentals: Explore modern data warehouse analytics in Azure](https://docs.microsoft.com/en-us/learn/paths/azure-data-fundamentals-explore-data-warehouse-analytics/)| 1 hr 51 min | explore the processing options available for building data analytics solutions in Azure. You will explore Azure Synapse Analytics, Azure Databricks, and Azure HDInsight |

## Describe core data concepts (15-20%):

<p><img align="center" src="https://github.com/msandfor/DP-900/blob/main/assets/big-data-logical.svg" alt="Big Data Architecture"></p>
<p align="center"></p>

| Reference | Objective | Item |
|-----|-----|-----|
| [Describe the difference between batch and streaming data](https://docs.microsoft.com/en-us/learn/modules/explore-core-data-concepts/4-describe-difference) | types of core data workloads | describe the difference between batch and streaming data |
| [Choosing a batch processing technology in Azure](https://docs.microsoft.com/en-us/azure/architecture/data-guide/technology-choices/batch-processing) | types of core data workloads | describe the difference between batch and streaming data |
| [Choosing a stream processing technology in Azure](https://docs.microsoft.com/en-us/azure/architecture/data-guide/technology-choices/stream-processing) | types of core data workloads | describe the difference between batch and streaming data |
| [Real Time vs Batch Processing vs Stream Processing](https://www.bmc.com/blogs/batch-processing-stream-processing-real-time/) | types of core data workloads | describe the difference between batch and streaming data |
| [Big Data Battle : Batch Processing vs Stream Processing](https://medium.com/@gowthamy/big-data-battle-batch-processing-vs-stream-processing-5d94600d8103) | types of core data workloads | describe the difference between batch and streaming data |
| [What Is Data Consistency?](https://www.easytechjunkie.com/what-is-data-consistency.htm) | types of core data workloads | describe the difference between batch and streaming data |
| [Explore the characteristics of relational data](https://docs.microsoft.com/en-us/learn/modules/describe-concepts-of-relational-data/2-explore-characteristics) | types of core data workloads | describe the characteristics of relational data |
| [Relational vs. NoSQL data](https://docs.microsoft.com/en-us/dotnet/architecture/cloud-native/relational-vs-nosql-data) | types of core data workloads | describe the characteristics of relational data |
| [Relational Data Model](https://binaryterms.com/relational-data-model.html) | types of core data workloads | describe the characteristics of relational data |
| [Big data architecture style](https://docs.microsoft.com/en-us/azure/architecture/guide/architecture-styles/big-data) | types of core data workloads | describe the characteristics of relational data |
| [Identify types of data and data storage](https://docs.microsoft.com/en-us/learn/modules/explore-core-data-concepts/3-identify-types-storage) | types of core data workloads | describe the characteristics of relational data |
| [Description of the database normalization basics](https://docs.microsoft.com/en-us/office/troubleshoot/access/database-normalization-description) | types of core data workloads | describe the characteristics of relational data |
| [Clustered and Nonclustered Indexes Described](https://docs.microsoft.com/en-us/sql/relational-databases/indexes/clustered-and-nonclustered-indexes-described?view=sql-server-ver15) | types of core data workloads | describe the characteristics of relational data |
| [Explore the characteristics of relational data](https://docs.microsoft.com/en-us/learn/modules/describe-concepts-of-relational-data/2-explore-characteristics) | types of core data workloads | describe the characteristics of relational data |
| [Understand data store models](https://docs.microsoft.com/en-us/azure/architecture/guide/technology-choices/data-store-overview) | types of core data workloads | describe the characteristics of relational data |
| [Databases](https://docs.microsoft.com/en-us/sql/relational-databases/databases/databases?view=sql-server-ver15) | types of core data workloads | describe the characteristics of relational data |
| [Explore data analytics](https://docs.microsoft.com/en-us/learn/modules/explore-concepts-of-data-analytics/4-explore) | Describe data analytics core concepts | describe analytics techniques |
| [Describe, diagnose, and predict with IoT Analytics](https://azure.microsoft.com/en-us/blog/answering-whats-happening-whys-happening-and-what-will-happen-with-iot-analytics/) | Describe data analytics core concepts | describe analytics techniques |
| [Descriptive, predictive, and prescriptive analytics: How are they different?](https://www.zdnet.com/article/descriptive-predictive-and-prescriptive-analytics-how-are-they-different/) | Describe data analytics core concepts | describe analytics techniques |
| [Explore data visualization](https://docs.microsoft.com/en-us/learn/modules/explore-concepts-of-data-analytics/3-explore-data-visualization) | Describe data analytics core concepts | describe data visualization |
| [Describe data ingestion and processing](https://docs.microsoft.com/en-us/learn/modules/explore-concepts-of-data-analytics/2-describe-data-ingestion-process) | Describe data analytics core concepts | describe the concepts of data processing |
| [Extract, transform, and load (ETL)](https://docs.microsoft.com/en-us/azure/architecture/data-guide/relational-data/etl) | Describe data analytics core concepts | describe the concepts of data processing |



<p><img align="center" src="https://github.com/msandfor/DP-900/blob/main/assets/analytics.jpg" alt="Analytics"></p>
<p align="center"></p>


