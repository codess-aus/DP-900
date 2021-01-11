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

<p><img align="center" src="https://github.com/msandfor/DP-900/blob/main/assets/2-relations.png" alt="Realtional Databases"></p>
<p align="center"></p>

The main characteristics of a **Relational Database** are:

* All data is tabular. Entities are modeled as tables, each instance of an entity is a row in the table, and each property is defined as a column.

* All rows in the same table have the same set of columns.

* A table can contain any number of rows.

* A primary key uniquely identifies each row in a table. No two rows can share the same primary key.

* A foreign key references rows in another, related table. For each value in the foreign key column, there should be a row with the same value in the corresponding primary key column in the other table.

