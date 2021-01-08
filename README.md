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
| [SQL Server Integration Services](https://docs.microsoft.com/en-us/sql/integration-services/sql-server-integration-services?view=sql-server-ver15) |  |  |
| [SSIS and Data Sources](https://social.technet.microsoft.com/wiki/contents/articles/1947.ssis-and-data-sources.aspx) |  |  |
| [What is Azure Data Factory?](https://docs.microsoft.com/en-us/azure/data-factory/introduction) |  |  |
| [Copy activity in Azure Data Factory](https://docs.microsoft.com/en-us/azure/data-factory/copy-activity-overview) |  |  |
| [Find the analytics product you need](https://azure.microsoft.com/en-us/product-categories/analytics/) |  |  |
| [Load data into Azure Data Lake Storage Gen2 with Azure Data Factory](https://docs.microsoft.com/en-us/azure/data-factory/load-azure-data-lake-storage-gen2) |  |  |
| [Introduction to Azure Data Lake Storage Gen2](https://docs.microsoft.com/en-us/azure/storage/blobs/data-lake-storage-introduction) |  |  |
| [What is Azure SQL Database?](https://docs.microsoft.com/en-us/azure/azure-sql/database/sql-database-paas-overview) |  |  |
| [What is dedicated SQL pool (formerly SQL DW) in Azure Synapse Analytics?](https://docs.microsoft.com/en-us/azure/synapse-analytics/sql-data-warehouse/sql-data-warehouse-overview-what-is) |  |  |
| [FOUR TYPES OF BUSINESS ANALYTICS TO KNOW](https://www.analyticsinsight.net/four-types-of-business-analytics-to-know/) |  |  |
| [Explore data analytics](https://docs.microsoft.com/en-us/learn/modules/explore-concepts-of-data-analytics/4-explore) |  |  |
| [Explore data visualization](https://docs.microsoft.com/en-us/learn/modules/explore-concepts-of-data-analytics/3-explore-data-visualization) |  |  |
| [Visualization types in Power BI](https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-types-for-reports-and-q-and-a) |  |  |
| [Tips and tricks for creating reports in Power BI Desktop](https://docs.microsoft.com/en-us/power-bi/create-reports/desktop-tips-and-tricks-for-creating-reports) |  |  |
| [Visual types in Power BI](https://docs.microsoft.com/en-us/power-bi/consumer/end-user-visual-type) |  |  |
| [Features of the key influencers visual](https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-influencers) |  |  |
| [Scatter charts, bubble charts, and dot plot charts in Power BI](https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-scatter) |  |  |
| [Overview of data analysis](https://docs.microsoft.com/en-us/learn/modules/data-analytics-microsoft/2-data-analysis) |  |  |

<p><img align="center" src="https://github.com/msandfor/DP-900/blob/main/assets/analytics.jpg" alt="Analytics"></p>
<p align="center"></p>

<p><img align="center" src="https://github.com/msandfor/DP-900/blob/main/assets/four-types-business-analytics.png" alt="4 types of business analytics"></p>
<p align="center"></p>


<p><img align="center" src="https://github.com/msandfor/DP-900/blob/main/assets/2-data-process.png" alt="Data Processing"></p>
<p align="center"></p>

<p><img align="center" src="https://github.com/msandfor/DP-900/blob/main/assets/copy-activity.png" alt="Data Factory"></p>
<p align="center"></p>


## Describe how to work with relational data on Azure (25-30%)

| Reference | Objective | Item |
|-----|-----|-----|
| [Clustered and Nonclustered Indexes Described](https://docs.microsoft.com/en-us/sql/relational-databases/indexes/clustered-and-nonclustered-indexes-described?view=sql-server-ver15) |  |  |
| [Primary and Foreign Key Constraints](https://docs.microsoft.com/en-us/sql/relational-databases/tables/primary-and-foreign-key-constraints?view=sql-server-ver15&viewFallbackFrom=sql-server-ver1) |  |  |
| [Views](https://docs.microsoft.com/en-us/sql/relational-databases/views/views?view=sql-server-ver15) |  |  |
| [Understand data store models](https://docs.microsoft.com/en-us/azure/architecture/guide/technology-choices/data-store-overview) |  |  |
| [What is Azure Table storage ?](https://docs.microsoft.com/en-us/azure/storage/tables/table-storage-overview) |  |  |
| [Explore relational data structures](https://docs.microsoft.com/en-us/learn/modules/describe-concepts-of-relational-data/3-explore-structures) |  |  |
| [Heaps (Tables without Clustered Indexes)](https://docs.microsoft.com/en-us/sql/relational-databases/indexes/heaps-tables-without-clustered-indexes?view=sql-server-ver15) |  |  |
| [Explore the characteristics of relational data](https://docs.microsoft.com/en-us/learn/modules/describe-concepts-of-relational-data/2-explore-characteristics) |  |  |
| [Identify types of data and data storage](https://docs.microsoft.com/en-us/learn/modules/explore-core-data-concepts/3-identify-types-storage) |  |  |
| [Relational vs. NoSQL data](https://docs.microsoft.com/en-us/dotnet/architecture/cloud-native/relational-vs-nosql-data) |  |  |
| [Describe types of non-relational and NoSQL databases](https://docs.microsoft.com/en-us/learn/modules/explore-concepts-of-non-relational-data/4-describe-types-nosql-databases) |  |  |
| [Understand data store models](https://docs.microsoft.com/en-us/azure/architecture/guide/technology-choices/data-store-overview) |  |  |
| [Azure SQL Database](https://docs.microsoft.com/en-us/learn/modules/explore-relational-data-offerings/4-azure-sql-database) |  |  |
| [Explore Azure Synapse Analytics](https://docs.microsoft.com/en-us/learn/modules/explore-data-storage-processing-azure/3-explore-azure-synapse-analytics) |  |  |
| [Explore Azure Cosmos DB](https://docs.microsoft.com/en-us/learn/modules/explore-non-relational-data-offerings-azure/5-explore-azure-cosmos-database) |  |  |
| [What is SQL Server on Azure Virtual Machines (Windows)](https://docs.microsoft.com/en-us/azure/azure-sql/virtual-machines/windows/sql-server-on-azure-vm-iaas-what-is-overview) |  |  |
| [What is Azure SQL Database?](https://docs.microsoft.com/en-us/azure/azure-sql/database/sql-database-paas-overview) |  |  |
| [SQL Server on Azure virtual machines](https://docs.microsoft.com/en-us/learn/modules/explore-relational-data-offerings/3-sql-server-azure-virtual-machines) |  |  |
| [Explore relational Azure data services](https://docs.microsoft.com/en-us/learn/modules/explore-relational-data-offerings/2-azure-data-services) |  |  |
| [Features comparison: Azure SQL Database and Azure SQL Managed Instance](https://docs.microsoft.com/en-us/azure/azure-sql/database/features-comparison) |  |  |
| [What is Azure SQL Managed Instance?](https://docs.microsoft.com/en-us/azure/azure-sql/managed-instance/sql-managed-instance-paas-overview) |  |  |
| [What is Azure Database for PostgreSQL?](https://docs.microsoft.com/en-us/azure/postgresql/overview) |  |  |
| [Configure TLS connectivity in Azure Database for PostgreSQL - Single Server](https://docs.microsoft.com/en-us/azure/postgresql/concepts-ssl-connection-security) |  |  |
| [Configure TLS in Azure Database for PostgreSQL - Hyperscale (Citus)](https://docs.microsoft.com/en-us/azure/postgresql/concepts-hyperscale-ssl-connection-security) |  |  |
| [Use Azure Active Directory for authenticating with PostgreSQL](https://docs.microsoft.com/en-us/azure/postgresql/concepts-aad-authentication) |  |  |
| [Dedicated SQL pool (formerly SQL DW) architecture in Azure Synapse Analytics](https://docs.microsoft.com/en-us/azure/synapse-analytics/sql-data-warehouse/massively-parallel-processing-mpp-architecture) |  |  |
| [What is SaaS?](https://azure.microsoft.com/en-us/overview/what-is-saas/) |  |  |
| [SQL Server database migration to Azure SQL Database](https://docs.microsoft.com/en-us/azure/azure-sql/database/migrate-to-database-from-sql-server) |  |  |
| [Azure SQL Database Managed Instance](https://docs.microsoft.com/en-us/learn/modules/explore-relational-data-offerings/5-azure-sql-database-managed-instance) |  |  |
| [PostgreSQL, MariaDB, and MySQL](https://docs.microsoft.com/en-us/learn/modules/explore-relational-data-offerings/6-postgresql-mariadb-mysql) |  |  |
| [What is Azure SQL?](https://docs.microsoft.com/en-us/azure/azure-sql/azure-sql-iaas-vs-paas-what-is-overview) |  |  |
| [Connectivity architecture for Azure SQL Managed Instance](https://docs.microsoft.com/en-us/azure/azure-sql/managed-instance/connectivity-architecture-overview) |  |  |
| [Use Azure SQL Managed Instance securely with public endpoints](https://docs.microsoft.com/en-us/azure/azure-sql/managed-instance/public-endpoint-overview) |  |  |
| [Quickstart: Configure a point-to-site connection to Azure SQL Managed Instance from on-premises](https://docs.microsoft.com/en-us/azure/azure-sql/managed-instance/point-to-site-p2s-configure) |  |  |
| [Tutorial: Secure a database in Azure SQL Database](https://docs.microsoft.com/en-us/azure/azure-sql/database/secure-database-tutorial) |  |  |
| [Azure SQL Database and Azure SQL Managed Instance connect and query articles](https://docs.microsoft.com/en-us/azure/azure-sql/database/connect-query-content-reference-guide) |  |  |
| [Configure Always Encrypted by using Azure Key Vault](https://docs.microsoft.com/en-us/azure/azure-sql/database/always-encrypted-azure-key-vault-configure?tabs=azure-powershell) |  |  |
| [Dynamic Data Masking](https://docs.microsoft.com/en-us/sql/relational-databases/security/dynamic-data-masking?view=sql-server-ver15) |  |  |
| [Transparent data encryption for SQL Database, SQL Managed Instance, and Azure Synapse Analytics](https://docs.microsoft.com/en-us/azure/azure-sql/database/transparent-data-encryption-tde-overview?view=sql-server-ver15&tabs=azure-portal) |  |  |
| [What is Azure Data Studio?](https://docs.microsoft.com/en-us/sql/azure-data-studio/what-is-azure-data-studio?view=sql-server-ver15) |  |  |
| [Quickstart: Use Azure Data Studio to connect and query Azure SQL database](https://docs.microsoft.com/en-us/sql/azure-data-studio/quickstart-sql-database?view=sql-server-ver15) |  |  |
| [Quickstart: Use Azure Data Studio to connect and query PostgreSQL](https://docs.microsoft.com/en-us/sql/azure-data-studio/quickstart-postgres?view=sql-server-ver15) |  |  |
| [Connect to Synapse SQL with SQL Server Management Studio (SSMS)](https://docs.microsoft.com/en-us/azure/synapse-analytics/sql/get-started-ssms) |  |  |
| [Quickstart: Azure Database for MariaDB: Use MySQL Workbench to connect and query data](https://docs.microsoft.com/en-us/azure/mariadb/connect-workbench) |  |  |
| [Quickstart: Create a server-level firewall rule using the Azure portal](https://docs.microsoft.com/en-us/azure/azure-sql/database/firewall-create-server-level-portal-quickstart) |  |  |
| [What is Azure role-based access control (Azure RBAC)?](https://docs.microsoft.com/en-us/azure/role-based-access-control/overview) |  |  |
| [Manage storage account access keys](https://docs.microsoft.com/en-us/azure/storage/common/storage-account-keys-manage?tabs=azure-portal) |  |  |
| [Use Azure Active Directory authentication](https://docs.microsoft.com/en-us/azure/azure-sql/database/authentication-aad-overview) |  |  |
| [Microsoft identity platform access tokens](https://docs.microsoft.com/en-us/azure/active-directory/develop/access-tokens) |  |  |
| [What is SQL Server Management Studio (SSMS)?](https://docs.microsoft.com/en-us/sql/ssms/sql-server-management-studio-ssms?view=sql-server-ver15) |  |  |
| [What is Azure Data Studio?](https://docs.microsoft.com/en-us/sql/azure-data-studio/what-is-azure-data-studio?view=sql-server-ver15) |  |  |
| [Use Jupyter Notebooks in Azure Data Studio](https://docs.microsoft.com/en-us/sql/azure-data-studio/notebooks/notebooks-guidance?view=sql-server-ver15) |  |  |
| [SQL Server Data Tools](https://docs.microsoft.com/en-us/sql/ssdt/sql-server-data-tools?view=sql-server-ver15) |  |  |
| []() |  |  |
| []() |  |  |

The following two applications are best suited to batch processing: 
Employee payroll processing and generating payroll checks 
• Setting inventory stocking levels based on seasonal sales volume 
Data for batch processing is collected over time, often from different data sources, and it is processed as a 
dataset that includes a range of rows or all rows in the dataset. Batch processing is designed to handle 
processing of large datasets. There is typically a long latency between data collection and data processing. 
The following two applications are best suited to stream processing: 
• Reporting the number of users and bandwidth user for an online game 
• Identifying detected manufacturing errors to automatically reject failing parts 
Stream processing is designed for real-time or near real-time data processing, often as a data load process 
with minimal processing. Data must be able to stream out as quickly as it streams in for processing. Data is 
either processed as it is generated or in micro-batches of a very few rows with latency of no more than a 
few milliseconds. 