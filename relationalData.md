## Describe how to work with relational data on Azure (25-30%)
### Describe relational data workloads
* identify the right data offering for a relational workload
* describe relational data structures (e.g., tables, index, views)
### Describe relational Azure data services
* describe and compare PaaS, IaaS, and SaaS solutions
* describe Azure SQL database services including Azure SQL Database, Azure SQL
### Managed Instance, and SQL Server on Azure Virtual Machine
* describe Azure Synapse Analytics
* describe Azure Database for PostgreSQL, Azure Database for MariaDB, and Azure Database for MySQL
### Identify basic management tasks for relational data
* describe provisioning and deployment of relational data services
* describe method for deployment including the Azure portal, Azure Resource Manager templates, Azure PowerShell, and the Azure command-line interface (CLI)
* identify data security components (e.g., firewall, authentication)
* identify basic connectivity issues (e.g., accessing from on-premises, access with Azure VNets, access from Internet, authentication, firewalls)
* identify query tools (e.g., Azure Data Studio, SQL Server Management Studio, sqlcmd
utility, etc.)
Describe query techniques for data using SQL language
* compare Data Definition Language (DDL) versus Data Manipulation Language (DML)
* query relational data in Azure SQL Database, Azure Database for PostgreSQL, and Azure Database for MySQL



The SQL language has four basic types of commands.

**Data Manipulation Language DML commands** are used to *manipulate rows* in a table. They include:
* DELETE
* INSERT
* SELECT
* UPDATE

**Data Definition Language (DDL) commands** are used to *create, modify, and delete database objects*. They include:
* ALTER
* CREATE
* DROP
* RENAME

**Data Control Language (DCL) commands** are for *access control* and permission management. They include:
* DENY
* GRANT
* REVOKE

**Transaction Control Language (TCL) commands** are used to *manage and control transactions*. They include:
* BEGIN TRAN
* COMMIT TRAN
* ROLLBACK

A **key/value data store**:
* A key/value data store functions essentially as a large hash table and is optimized for fast data writes.
* Each data row is referenced by a single key value.
* The only operations supported are simple query, insert, and delete operations.
* Data updates require the application to rewrite the data for the entire value.
* Queries can be run by a key or a range of keys.

**A column-family (columnar) data store**: 
* A column-family data store is similar to a relational data store in that data is organized as rows and columns, but the columns are divided into column families that can store multiple values in a single column.
* A row does not necessarily have a value in each column family. 
* Columns within a column family are physically stored in the same file.
* A column-family data store is similar to a relational data store in that data is organized as rows and columns, but the columns are divided into column families that can store multiple values in a single column. 
* Columns within a column family are physically stored in the same file.
* Data is denormalized and relationships are not defined between entities.

**A Table Data Store**: 
* A table data store uses a row and column data format with the data somewhat normalized but the same schema is not enforced across all rows.
* Each row can have a different number of columns.
* In Azure Table store, data is organized based on a partition key and a row key.
* The partition key identifies the partition in which the data is stored, and the row uniquely identifies the row within the partition.
* You would use a table data store for denormalized data that is stored in a row/column structure with a variable number of columns per row. 
* Table storage can be used for unstructured data, semi-structured data, or a mix of data types. 
* This type of data is supported through Azure Table storage or an Azure Cosmos DB database.

**A Graph Data Store**: 
* A graph data store is designed to support extensive, complex relationships between entities. This helps to make it easier to perform complex relation analysis.
* Made up of entities and relationships that are referred to as nodes and edges.
* You can have multiple relationships between entities, including hierarchical relationships.
* A graph data store is designed to support extensive, complex relationships between entities. This helps to make it easier to perform complex relation analysis.


**A Document Store**:
* A document store supports semi-structured documents.
* Each document is identified as a single key, and the data schema is defined internally in each document named fields and values.
* The schema and content can vary between documents.
* Each document typically contains the data for a single entity.
* Relationships are not defined between documents.
* Semi-structured data with each entity providing its own field definitions is a description of document-type data, and therefore a document store is your best choice. 
* Documents are written and retrieved as complete documents. The embedded field definitions make it possible to query documents in order to retrieve field values. 
* You would typically use an Azure Cosmos DB storage solution.

**An object store** is used to store unstructured data, such as audio or video files, and it does not provide for relationship analysis.
* For large audio and video files that are used as the source for streaming content, you should choose an object data store. 
* Files of this type are unstructured, non-relational data. The typical storage solution for this type of file is an object store, such as Azure Blob storage.

