## Describe how to work with non-relational data on Azure (25-30%)
### Describe non-relational data workloads
* describe the characteristics of non-relational data
* describe the types of non-relational and NoSQL data
* recommend the correct data store
* determine when to use non-relational data
### Describe non-relational data offerings on Azure
* identify Azure data services for non-relational workloads
* describe Azure Cosmos DB APIs
* describe Azure Table storage
* describe Azure Blob storage
* describe Azure File storage
### Identify basic management tasks for non-relational data
* describe provisioning and deployment of non-relational data services
* describe method for deployment including the Azure portal, Azure Resource Manager templates, Azure PowerShell, and the Azure command-line interface (CLI)
* identify data security components (e.g., firewall, authentication, encryption)
* identify basic connectivity issues (e.g., accessing from on-premises, access with Azure VNets, access from Internet, authentication, firewalls)
* identify management tools for non-relational data

Each document in a **document** database typically contains all data for a single entity. 

The data contained in the document can vary between documents. 

Each document is identified by a unique key used to identify the document and each document is written or retrieved as a single block.

Documents in a document database do not use the same data schema for all documents. 

The schema is defined internally in the document, and each individual document can have a different schema. 

This allows for easy support of denormalized data and variations between entities. 

Documents in a document database do not support relationships enforced between documents. 

Document databases do not provide a way to establish relationships between documents. Document databases and graph databases are examples of non-relational data stores.

Document databases store data in JSON or XML format and do not require all documents to have the same structure.

A **key/value** data store functions essentially as a large hash table and is optimized for fast data writes. 

Each data row is referenced by a single key value. The only operations
supported are simple query, insert, and delete operations. 

Data updates require the application to rewrite the data for the entire value. Queries can be run by a key or a range of keys.

You should use a key-value non-relational data store to maintain user preferences for your company's application. Key-value stores are highly optimized for simple searches like user preferences. A Key-value store associates each data value with a key which can be used to access the data.

Azure File storage is not the recommended storage solution for key/value storage implementation. Microsoft recommends Azure Cosmos DB Core (SQL) API for new key/value requirements. Key/value storage is also supported by Azure Table storage and Cosmos DB Table API.

A **column-family** data store is similar to a relational data store in that data is organized as rows and columns, but the columns are divided into column families that can store multiple values in a single column. A row does not necessarily have a value in each column family. 

Columns within a column family are physically stored in the same file.

You should use the Cassandra API to store columnar data. This API is compatible with Apache Cassandra databases, which are column-family databases used to store columnar data consisting of row identifiers and a group of information stored in a column. Each group of information is stored in independent data structures named keyspaces.

You should use the Cassandra API when moving column-family format data to the cloud to support an existing application. Microsoft suggests limiting the use of the **Cassandra API to supporting existing data**, such as when **moving data to the cloud**. The Cassandra API is specifically designed to support **column-family data**.

A **table** data Store uses a row and column data format with the data
somewhat normalized but the same schema is not enforced across all rows. 

Each row can have a different number of columns. 

In Azure Table store, data is organized based on a partition key and a row key. The partition key identifies the partition in which the data is stored, and the row uniquely identifies the row within the partition.

Table storage is used for storing structured, non-relational data.

A **graph** data store is designed to support extensive, complex 
relationships between entities. This helps to make it easier to perform complex relation analysis. 
* Document databases and graph databases are examples of non-relational data stores.
* Graph databases store information in the form of edges and nodes. They are used to represent complex relationships such as social interactivity.

You should use the **Gremlin API** to store **graph data**. This API is compatible with Gremlin, which is a graph database that stores nodes and edges used for complex relationships among entities.


You do not need to define a schema on non-relational data. A non-relational database does not require you to configure a schema. It focuses on storing the data as it is rather than manipulating the data in tables and columns like in a relational database.

You can use non-relational data to store data that has a highly variable structure.

You can store entities with different structures in a non-relational data store, for example, a customer in an e-commerce platform could have multiple contact numbers or addresses, while another customer could have only one contact number. Non-relational data provides you this flexibility.

You can use indexing with non-relational data in a similar way to an index in a relational database. Some non-relational databases, such as Cosmos DB, support indexing in the fields of a stored entity, in a similar way a relational database does.

Document databases and graph databases are examples of non-relational data stores.

The Azure database for MariaDg and SQL databases are examples relational databases. Relational databases store information in the form of tables, which you can connect through relationships. Relational databases are used for highly structured data.

**Azure Blob** is the only Azure storage option that supports access tiers. The default is the Hot tier, which is designed for frequently accessed data. The Cool tier is optimized for data that will be stored for at least 30 days. The Cool tier has lower storage cost than the Hot tier but higher costs for early access. The Archive tier is designed for data that is rarely accessed and will remain in storage for at least 180 days. Access to Archive tier data requires the data to be rehydrated to a Hot or Cool tier. This can mean a latency of several hours. Access tier support requires Data Lake Storage Gen2.

Azure Blob also supports two performance tiers. The Standard performance tier provides for high performance using hard disk-based storage media. The Premium performance provides greater throughput than the Standard tier and uses solid state drive (SSD) media. The Standard and Premium tiers are also supported for other storage options including Azure File storage and Azure SQL Database.

Azure Table and Azure File do not support access tiers. Access tiers is a feature supported through Cosmos DB. Azure Table and Azure File are distinct storage types and are not implemented through Cosmos DB APIs.

File storage provides file storage with shared access, similar to a file server.

You can create a premium Azure File storage account in a FileStorage storage account only. You can create a standard File storage account only in a GPv2 account.

You can configure a premium Azure File storage account for LRS and, in select regions, for ZRS. A standard file storage account supports GRS, but not a premium storage account.

You can use a premium Azure File storage account to replace or supplement traditional on-premises file shares. This is true for both standard and premium storage accounts. This includes scenarios where application data is moved to the cloud but applications continue to run on-premises.

Microsoft recommends that any new data project created from scratch uses the **Core (SQL) API**. This includes applications with **key/value data**. This type of application is also supported by the Table API, but the Core (SQL) API is recommended as the best solution because it provides improved indexing and a richer query experience.

When creating a new application that analyzes detailed relationship information for non-relational data you should use the Gremlin API. This is one of the few cases where the Core (SQL) API is not recommended as the best solution. **Graph Database -> Gremlin API**

When moving application data to the cloud that uses semi-structured documents to store data, you should use the Core (SQL) API. The Core (SQL) API gives you the ability to create, query, and update data 
documents.

Azure File storage supports direct mounting by Windows, macOS, and Linux. This includes support for concurrent access from the cloud and on-premises. Azure File storage can be used to supplement or replace on-premises file server shares.

Azure File storage does not allow you to select the underlying hardware and operating system. Azure File storage is implemented as a serverless file service in which you have neither direct access to, or administrative responsibilities for, the underlying architecture. The one infrastructure choice you can make is between hard disk (ADD) standard file shares and solid-state disk (SSD) premium file shares.

Azure File storage does not support redundancy across multiple regions by default. Standard file shares support locally-redundant storage (CRS) by default with options for zone redundant storage (ZRS), geo-
redundant storage (CRS), and geo-zone-redundant storage (GZRS). 

Replication across multiple regions is supported as an option, but not as a default setting. The large file share feature and premium file shares support LRS and ZRS only.

**Cosmos DB Table API** supports multi-master replication across multiple regions. This means that you can set it up to let any region accept writes, Global distribution is a turnkey feature of Cosmos DB Table API. Table storage is limited to one primary image that can accept writes and can have one read-only replica in a different region.

Cosmos DB Table API supports manual and automatic failovers. Failure can be initiated from any redundant region and at any time.

Cosmos DB Table API automatically creates secondary indexes without any index management requirements.

An Azure Cosmos account is topmost in the resource hierarchy. You must have this before you can create an Azure Cosmos DB database instance. You can then create API-specific containers, such as tables, collections, or graphs. 

You create items, the entities for which you are storing data, inside a container. Examples include documents, nodes, edges, or rows.

Azure Cosmos Account -> Database -> Container -> Item

**Azure Table API** does not let you initiate failover.

Each row in a table can have a different number of columns in both Azure Cosmos DB and Azure Table storage. This is a defining feature of Table storage.

Data is organized and distributed by partition keys and row keys. This is the only indexing on Azure Table storage.

You can use the Table API to store key/value data organized as rows and columns, forming a table in which the number of columns may vary according to each row. This API is compatible with Azure Table storage.

You should use the **MongoDB API** to store JSON documents. This API is compatible with MongoDB, which is a document database that stores semi-structured data in JSON format. A document usually contains all data from an entity, and each document can have different fields Of data.


