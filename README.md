# azure-data-engineering
Stuff about azure data engineering

## Microsoft Certified: Azure Data Engineer Associate DP-203: Data Engineering on Microsoft Azure

https://learn.microsoft.com/en-us/certifications/azure-data-engineer/


## Practice Assessments for Microsoft Certifications

https://learn.microsoft.com/en-us/certifications/practice-assessments-for-microsoft-certifications#availability

## Study guide

https://learn.microsoft.com/en-us/certifications/resources/study-guides/DP-203


Skills measured
* Design and implement data storage (15–20%)
* Develop data processing (40–45%)
* Secure, monitor, and optimize data storage and data processing (30–35%)

## dp-203-azure-data-engineer/Instructions/Labs/

https://github.com/MicrosoftLearning/dp-203-azure-data-engineer/tree/master/Instructions/Labs

## MS Learn

https://learn.microsoft.com/en-us/certifications/azure-data-engineer/

## Get started with data engineering on Azure

#### Introduction to data enginering in Azure

Types of data
* Structured, table based, relation, or flat file csv
* Semi-structured, JSON
* Unstructured, pdf, word and images

Data integration
* Data Integration involves establishing links between operational and analytical services and data sources to enable secure, reliable access to data across multiple systems. 

Data transformation
* Operational data usually needs to be transformed into suitable structure and format for analysis, often as part of an extract, transform, and load (ETL) process; though increasingly a variation in which you extract, load, and transform (ELT)

Data consolidation
* Data consolidation is the process of combining data that has been extracted from multiple data sources into a consistent structure - usually to support analytics and reporting.

Common languages
* SQL, Python, others

#### Important data engineering concepts

Operational and analytical data
* Operational data is usually transactional data that is generated and stored by applications, often in a relational or non-relational database. 
* Analytical data is data that has been optimized for analysis and reporting, often in a data warehouse.

Streaming data
* Streaming data refers to perpetual sources of data that generate data values in real-time, often relating to specific events.

Data pipelines
* Data pipelines are used to orchestrate activities that transfer and transform data.

Data lakes
* A data lake is a storage repository that holds large amounts of data in native, raw formats.
* The idea with a data lake is to store everything in its original, untransformed state. This approach differs from a traditional data warehouse, which transforms and processes the data at the time of ingestion.

Data warehouses
* A data warehouse is a centralized repository of integrated data from one or more disparate sources.

Apache Spark
* Apache Spark is a parallel processing framework that takes advantage of in-memory processing and a distributed file storage. It's a common open-source software (OSS) tool for big data scenarios.


#### Data engineering in Microsoft Azure

![Data Engineering in Azure ](https://github.com/spawnmarvel/azure-data-engineering/blob/main/images/data-eng-azure.jpg)

The core Azure technologies used to implement data engineering workloads include:
* Azure Synapse Analytics
* Azure Data Lake Storage Gen2
* Azure Stream Analytics
* Azure Data Factory
* Azure Databricks

#### Introduction to Azure Data Lake Storage Gen2

#### Understand Azure Data Lake Storage Gen2

A data lake is a repository of data that is stored in its natural format, usually as blobs or files.
* Azure Data Lake Storage combines a file system with a storage platform to help you quickly identify insights into your data. Data Lake Storage builds on Azure Blob storage capabilities to optimize it specifically for analytics workloads. 
* Data Lake Storage Gen2 as the basis for both real-time and batch solutions.

Hadoop compatible access
* A benefit of Data Lake Storage is that you can treat the data as if it's stored in a Hadoop Distributed File System. With this feature, you can store the data in one place and access it through compute technologies including Azure Databricks, Azure HDInsight, and Azure Synapse Analytics without moving the data between environments. 
* The data engineer also has the ability to use storage mechanisms such as the parquet format, which is highly compressed and performs well across multiple platforms using an internal columnar storage.


Security
* Data Lake Storage supports access control lists (ACLs) and Portable Operating System Interface (POSIX) permissions that don't inherit the permissions of the parent directory. 
* In fact, you can set permissions at a directory level or file level for the data stored within the data lake, providing a much more secure storage system.

Performance
* Azure Data Lake Storage organizes the stored data into a hierarchy of directories and subdirectories, much like a file system, for easier navigation. As a result, data processing requires less computational resources, reducing both the time and cost.

Data redundancy
* Data Lake Storage takes advantage of the Azure Blob replication models, LRS or GRS

Enable Azure Data Lake Storage Gen2 in Azure Storage

#### Enable Azure Data Lake Storage Gen2 in Azure Storage

Select the option to Enable hierarchical namespace in the Advanced page when creating the storage account in the Azure portal:

![Enable lake ](https://github.com/spawnmarvel/azure-data-engineering/blob/main/images/enable-lake.jpg)

Or Data Lake Gen2 upgrade wizard in the Azure portal page.

Compare Azure Data Lake Store to Azure Blob storage

In Azure Blob storage, you can store large amounts of unstructured ("object") data in a flat namespace within a blob container.
* If you want to store data without performing analysis on the data, set the Hierarchical Namespace option to Disabled to set up the storage account as an Azure Blob storage account. 
* If you are performing analytics on the data, set up the storage account as an Azure Data Lake Storage Gen2 account by setting the Hierarchical Namespace option to Enabled.

![Enable lake ](https://github.com/spawnmarvel/azure-data-engineering/blob/main/images/hier-namespace.jpg)


#### Understand the stages for processing big data

There are four stages for processing big data solutions that are common to all architectures:
1. Ingest - The ingestion phase identifies the technology and processes that are used to acquire the source data.
2. Store - The store phase identifies where the ingested data should be placed. Azure Data Lake Storage Gen2 provides a secure and scalable storage solution that is compatible with commonly used big data processing technologies.
3. Prep and train - The prep and train phase identifies the technologies that are used to perform data preparation and model training and scoring for machine learning solutions. 
4. Model and serve - Finally, the model and serve phase involves the technologies that will present the data to users.



#### Introduction to Azure Synapse Analytics

What is Azure Synapse Analytics
* Descriptive analytics, which answers the question “What is happening in my business?”
* Diagnostic analytics, which deals with answering the question “Why is it happening?”.
* Predictive analytics, which enables you to answer the question “What is likely to happen in the future based on previous trends and patterns?”
* Prescriptive analytics, which enables autonomous decision making based on real-time or near real-time analysis of data, using predictive analytics.


How Azure Synapse Analytics works

Creating and using an Azure Synapse Analytics workspace
* A Synapse Analytics workspace defines an instance of the Synapse Analytics service in which you can manage the services and data resources needed for your analytics solution.

Working with files in a data lake
* One of the core resources in a Synapse Analytics workspace is a data lake, in which data files can be stored and processed at scale. A workspace typically has a default data lake, which is implemented as a linked service to an Azure Data Lake Storage Gen2 container.

Ingesting and transforming data with pipelines
*  Data is extracted from multiple operational sources and transferred to a central data lake or data warehouse for analysis. 
* Azure Synapse Analytics includes built-in support for creating, running, and managing pipelines that orchestrate the activities necessary to retrieve data from a range of sources, transform the data as required, and load the resulting transformed data into an analytical store.

NOTE!

Pipelines in Azure Synapse Analytics are based on the same underlying technology as Azure Data Factory.

Querying and manipulating data with SQL
* Azure Synapse Analytics supports SQL-based data querying and manipulation through two kinds of SQL pool
* * A built-in serverless pool that is optimized for using relational SQL semantics to query file-based data in a data lake.
* * Custom dedicated SQL pools that host relational data warehouses.

You can use the built-in serverless pool for cost-effective analysis and processing of file data in the data lake [...]

![sql lake ](https://github.com/spawnmarvel/azure-data-engineering/blob/main/images/SQL-DATA.jpg)

Processing and analyzing data with Apache Spark
* Apache Spark is an open source platform for big data analytics. Spark performs distributed processing of files in a data lake by running jobs that can be implemented using any of a range of supported programming languages. 

Exploring data with Data Explorer
* Azure Synapse Data Explorer is a data processing engine in Azure Synapse Analytics that is based on the Azure Data Explorer service. 
* Kusto, KQL

Integrating with other Azure data services
* Azure Synapse Link enables near-realtime synchronization between operational data in Azure Cosmos DB, Azure SQL Database, SQL Server, and Microsoft Power Platform
* Microsoft Power BI
* Azure Machine Learning

When to use Azure Synapse Analytics
* Large-scale data warehousing, 
* Advanced analytics, 
* Data exploration and discovery, The serverless SQL pool functionality provided by Azure Synapse Analytics enables Data Analysts, Data Engineers and Data Scientist alike to explore the data within your data estate. This capability supports data discovery, diagnostic analytics, and exploratory data analysis.
* Real time analytics
* Data integration, Azure Synapse Pipelines enables you to ingest, prepare, model and serve the data to be used by downstream systems.
* Integrated analytics




## Build data analytics solutions using Azure Synapse serverless SQL pools

Use Azure Synapse serverless SQL pool to query files in a data lake

https://learn.microsoft.com/en-us/training/modules/query-data-lake-using-azure-synapse-serverless-sql-pools/


## Perform data engineering with Azure Synapse Apache Spark Pools

## Work with Data Warehouses using Azure Synapse Analytics

## Transfer and transform data with Azure Synapse Analytics pipelines

## Work with Hybrid Transactional and Analytical Processing Solutions using Azure Synapse Analytics

## Implement a Data Streaming Solution with Azure Stream Analytics

## Govern data across an enterprise

## Data engineering with Azure Databricks

