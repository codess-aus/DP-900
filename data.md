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

Examples of **Batch Processing**:
* Employee payroll processing and generating payroll checks
* Setting inventory stocking levels based on seasonal sales volume

Data for batch processing is collected over time, often from different data sources, and it is processed as a dataset that includes a range of rows or all rows in the dataset.

* Batch processing is designed to handle processing of large datasets.

* There is typically a long latency between data collection and data processing.

A batch process used to analyze customer activity could include data from different databases and from text documents in different formats. Data gathering often requires extensive transformation, and the data must then be written to a data store before analysis.

Batch processing must be used if the data is to be subjected to detailed analysis to generate visuals and reports.


Examples of **Stream Processing**: 
* Reporting the number of users and bandwidth user for an online game
* Identifying detected manufacturing errors to automatically reject failing parts

Stream processing is designed for real-time or near real-time data processing, often as a data load process with minimal processing. Data must be able to stream out as quickly as it streams in for processing. Data is either processed as it is generated or in micro-batches of a very few rows with latency of no more than a few milliseconds.

Streaming could involve collecting data from multiple Internet of Things (IOT) sensors and writing them to Table storage.

Stream processing is set up where changes to the data are kept to a minimum to optimize performance.

For data used for transaction processing that requires immediate, consistent postings, stream processing should be used. This is because of a concern about latency. For example, you might insert a time stamp on each incoming entry or make minor formatting changes to the data.

Examples of streaming data include:
* A financial institution tracks changes in the *stock market* in real time, computes value-at-risk, and automatically rebalances portfolios based on stock price movements.
* An *online gaming* company collects real-time data about player-game interactions, and feeds the data into its gaming platform. It then analyzes the data in real time, offers incentives and dynamic experiences to engage its players.
* A real-estate website that tracks a subset of data from consumers’ mobile devices, and makes *real-time property recommendations* of properties to visit based on their geo-location.

Data with similar content can be processed from multiple sources by both batch and stream processing. One primary difference is that batch processing can involve a wider variety of sources, including on premises sources, whereas stream processing would receive data from streaming sources only, and it would most likely be with similar data. 

With both batch and stream processing, the data that is processed can include large quantities of data.

Differences between batch and streaming data:

* Data Scope: Batch processing can process all the data in the dataset. Stream processing typically only has access to the most recent data received, or within a rolling time window (the last 30 seconds, for example).

* Data Size: Batch processing is suitable for handling large datasets efficiently. Stream processing is intended for individual records or micro batches consisting of few records.

* Performance: The latency for batch processing is typically a few hours. Stream processing typically occurs immediately, with latency in the order of seconds or milliseconds. Latency is the time taken for the data to be received and processed.

* Analysis: You typically use batch processing for performing complex analytics. Stream processing is used for simple response functions, aggregates, or calculations such as rolling averages.

The main characteristics of a **Relational Database** are:

* All data is tabular. Entities are modeled as tables, each instance of an entity is a row in the table, and each property is defined as a column.

* All rows in the same table have the same set of columns.

* A table can contain any number of rows.

* A primary use of relational databases is to handle transaction processing

Examples:
* Inventory management
* Order management
* Reporting database
* Accounting

* Records are frequently created and updated.
* Multiple operations have to be completed in a single transaction.
* Relationships are enforced using database constraints.
* Indexes are used to optimize query performance.
* Data is highly normalized.
* Database schemas are required and enforced.
* Many-to-many relationships between data entities in the database.
* Constraints are defined in the schema and imposed on any data in the database.
* Data requires high integrity. Indexes and relationships need to be maintained accurately.
* Data requires strong consistency. Transactions operate in a way that ensures all data are 100% consistent for all users and processes.
* Size of individual data entries is small to medium-sized.

* A primary key uniquely identifies each row in a table. No two rows can share the same primary key. 
* The primary key is a unique value assigned to a row. 
* Even if all of the other columnar information is the same two rows, the primary key value makes each row unique.

* A foreign key references rows in another, related table. For each value in the foreign key column, there should be a row with the same value in the corresponding primary key column in the other table.
* When setting up relationships between tables through the use of foreign keys, each foreign key value must have a corresponding value in a primary key.

A relational database restructures the data into a fixed format that is designed to answer specific queries. When data needs to be ingested very quickly, or the query is unknown and unconstrained, a relational database can be less suitable than a non-relational database.

**Non-relational databases** are highly suitable for the following scenarios:

* IoT and telematics. These systems typically ingest large amounts of data in frequent bursts of activity. Non-relational databases can store this information very quickly. The data can then be used by analytics services such as Azure Machine Learning, Azure HDInsight, and Microsoft Power BI. Additionally, you can process the data in real-time using Azure Functions that are triggered as data arrives in the database.

* Retail and marketing. Microsoft uses CosmosDB for its own ecommerce platforms that run as part of Windows Store and Xbox Live. It's also used in the retail industry for storing catalog data and for event sourcing in order processing pipelines.

* Gaming. The database tier is a crucial component of gaming applications. Modern games perform graphical processing on mobile/console clients, but rely on the cloud to deliver customized and personalized content like in-game stats, social media integration, and high-score leaderboards. Games often require single-millisecond latencies for reads and write to provide an engaging in-game experience. A game database needs to be fast and be able to handle massive spikes in request rates during new game launches and feature updates.

* Web and mobile applications. A non-relational database such as Azure Cosmos DB is commonly used within web and mobile applications, and is well suited for modeling social interactions, integrating with third-party services, and for building rich personalized experiences. The Cosmos DB SDKs (software development kits) can be used to build rich iOS and Android applications using the popular Xamarin framework.

NoSQL (non-relational) databases generally fall into four categories: key-value stores, document databases, column family databases, and graph databases.

The focus of a **key-value store is** the ability to *read and write data very quickly*. Search capabilities are secondary. A key-value store is an excellent choice for data ingestion, when a large volume of data arrives as a continual stream and must be stored immediately.

**Azure Table** storage is an example of a **key-value store**. Cosmos DB also implements a key-value store using the Table API.




**Normalization** is the process that is used to split an entity into multiple tables. This helps to minimize data duplication through the use of related tables. For example, an online order might need to include customer information and information about the items ordered. Rather than putting all of this information in the order you can have foreign keys pointing to the detail customer and detail item information in other tables.

Relational databases are commonly used in ecommerce systems, but one of the major use cases for using relational databases is Online Transaction Processing (OLTP). 

**OLTP applications** are focused on transaction-oriented tasks that process a very large number of transactions per minute. Relational databases are well suited for OLTP applications because they naturally support insert, update, and delete operations. A relational database can often be tuned to make these operations fast. Also, the nature of SQL makes it easy for users to perform ad-hoc queries over data.

Examples of OLTP applications that use relational databases are:

* Banking solutions
* Online retail applications
* Flight reservation systems
* Many online purchasing applications.

**ETL** stands for *Extract, Transform, and Load*. The raw data is retrieved and transformed before being saved. The extract, transform, and load steps can be performed as a continuous pipeline of operations. It is suitable for systems that only require simple models, with little dependency between items. For example, this type of process is often used for basic data cleaning tasks, deduplicating data, and reformatting the contents of individual fields.

**ELT** is an abbreviation of *Extract, Load, and Transform*. The process differs from ETL in that the data is stored before being transformed. The data processing engine can take an iterative approach, retrieving and processing the data from storage, before writing the transformed data and models back to storage. ELT is more suitable for constructing complex models that depend on multiple items in the database, often using periodic batch processing.

**Azure Data Factory**: A cloud-based data integration service that allows you to create data-driven workflows for orchestrating data movement and transforming data at scale. 

Using Azure Data Factory, you can create and schedule data-driven workflows (called pipelines) that can ingest data from disparate data stores. 

You can build complex ETL processes that transform data visually with data flows, or by using compute services such as Azure HDInsight Hadoop, Azure Databricks, and Azure SQL Database.

<p><img align="center" src="https://github.com/msandfor/DP-900/blob/main/assets/2-etl-vs-elt.png" alt="ETL v ELT"></p>
<p align="center"></p>

A **transactional database** must adhere to the **ACID** (Atomicity, Consistency, Isolation, Durability) properties to ensure that the database remains consistent while processing transactions.

**Atomicity** guarantees that each transaction is treated as a single unit, which *either succeeds completely, or fails completely*. If any of the statements constituting a transaction fails to complete, the entire transaction fails and the database is left unchanged. An atomic system must guarantee atomicity in each and every situation, including power failures, errors, and crashes.

**Consistency** ensures that a transaction can only take the data in the database from one valid state to another. A consistent database should never lose or create data in a manner that can't be accounted for. In the bank transfer example described earlier, if you *add funds to an account, there must be a corresponding deduction of funds somewhere*, or a record that describes where the funds have come from if they have been received externally. You can't suddenly create (or lose) money.

**Isolation** ensures that concurrent execution of transactions leaves the database in the same state that would have been obtained if the transactions were executed sequentially. *A concurrent process can't see the data in an inconsistent state* (for example, the funds have been deducted from one account, but not yet credited to another.)

**Durability** guarantees that once a transaction has been committed, it will remain committed even if there's a system failure such as a power outage or crash.

**Analytical workloads** are typically read-only systems that store vast volumes of historical data or business metrics, such as *sales performance and inventory levels*. Analytical workloads are used for data analysis and decision making. Analytics are generated by aggregating the facts presented by the raw data into summaries, trends, and other kinds of “Business information.”

Analytics can be based on a snapshot of the data at a given point in time, or a series of snapshots. People who are higher up in the hierarchy of the company usually don't require all the details of every transaction. They want the bigger picture.

An example of analytical information is a *report on monthly sales*. As the head of sales department, you may not need to see all daily transactions that took place (transactional information), but you definitely would like a monthly sales report to identify trends and to make decisions (analytical information).

There are three key job roles that deal with data in most organizations:

* **Database Administrators** manage databases, assigning permissions to users, storing backup copies of data and restore data in case of any failures.
* **Data Engineers** are vital in working with data, applying data cleaning routines, identifying business rules, and turning data into useful information.
* **Data Analysts** explore and analyze data to create visualizations and charts to enable organizations to make informed decisions.

Most database management systems provide their own set of tools to assist with database administration. 
For example:
* SQL Server Database Administrators use SQL Server Management Studio for most of their day-to-day database maintenance activities. 
* pgAdmin for PostgreSQL systems, 
* MySQL Workbench for MySQL. 

There are also a number of *cross-platform database administration tools* available. One example is **Azure Data Studio**

**Azure Data Studio** provides a graphical user interface for managing many different database systems. It currently provides connections to on-premises SQL Server databases, Azure SQL Database, PostgreSQL, Azure SQL Data Warehouse, and SQL Server Big Data Clusters, amongst others.

**SQL Server Management Studio** provides a graphical interface, enabling you to query data, perform general database administration tasks, and generate scripts for automating database maintenance and support operations.

Azure SQL database provides database services in Azure. It's similar to SQL Server, except that it runs in the cloud. *You can manage Azure SQL database using Azure portal.*

Typical configuration tasks such as increasing the database size, creating a new database, and deleting an existing database are done using the Azure portal.



