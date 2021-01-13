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

Each document in a document database typically contains all data for a single entity. 

The data contained in the document can vary between documents. 

Each document is identified by a unique key used to identify the document and each document is written or retrieved as a single block.

Documents in a document database do not use the same data schema for all documents. 

The schema is defined internally in the document, and each individual document can have a different schema. 

This allows for easy support of denormalized data and variations between entities. 

Documents in a document database do not support relationships enforced between documents. 

Document databases do not provide a way to establish relationships between documents.

A **key/value** data store functions essentially as a large hash table and is optimized for fast data writes. 

Each data row is referenced by a single key value. The only operations
supported are simple query, insert, and delete operations. 

Data updates require the application to rewrite the data for the entire value. Queries can be run by a key or a range of keys.

A **column-family** data store is similar to a relational data store in that data is organized as rows and columns, but the columns are divided into column families that can store multiple values in a single column. A row does not necessarily have a value in each column family. 

Columns within a column family are physically stored in the same file.

A **table** data Store uses a row and column data format with the data
somewhat normalized but the same schema is not enforced across all rows. 

Each row can have a different number of columns. 

In Azure Table store, data is organized based on a partition key and a row key. The partition key identifies the partition in which the data is stored, and the row uniquely identifies the row within the partition.

A **graph** data store is designed to support extensive, complex 
relationships between entities. This helps to make it easier to perform complex relation analysis.

You do not need to define a schema on non-relational data. A non-relational database does not require you to configure a schema. It focuses on storing the data as it is rather than manipulating the data in tables and columns like in a relational database.

You can use non-relational data to store data that has a highly variable structure. 

You can store entities with different structures in a non-relational data store, for example, a customer in an e-commerce platform could have multiple contact numbers or addresses, while another customer could have only one contact number. Non-relational data provides you this flexibility.

You can use indexing with non-relational data in a similar way to an index in a relational database. Some non-relational databases, such as Cosmos DB, support indexing in the fields of a stored entity, in a similar way a relational database does. 