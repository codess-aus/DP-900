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