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
If you are performing analytics on the data, set up the storage account as an Azure Data Lake Storage Gen2 account by setting the Hierarchical Namespace option to Enabled.

![Enable lake ](https://github.com/spawnmarvel/azure-data-engineering/blob/main/images/hier-namespace.jpg)



#### Introduction to Azure Synapse Analytics




## Build data analytics solutions using Azure Synapse serverless SQL pools

## Perform data engineering with Azure Synapse Apache Spark Pools

## Work with Data Warehouses using Azure Synapse Analytics

## Transfer and transform data with Azure Synapse Analytics pipelines

## Work with Hybrid Transactional and Analytical Processing Solutions using Azure Synapse Analytics

## Implement a Data Streaming Solution with Azure Stream Analytics

## Govern data across an enterprise

## Data engineering with Azure Databricks

