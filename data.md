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


Data with similar content can be processed from multiple sources by both batch and stream processing. One primary difference is that batch processing can involve a wider variety of sources, including on premises sources, whereas stream processing would receive data from streaming sources only, and it would most likely be with similar data. 

With both batch and stream processing, the data that is processed can include large quantities of data.

The main characteristics of a **Relational Database** are:

* All data is tabular. Entities are modeled as tables, each instance of an entity is a row in the table, and each property is defined as a column.

* All rows in the same table have the same set of columns.

* A table can contain any number of rows.

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