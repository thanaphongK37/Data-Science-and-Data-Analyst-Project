# **Data Engineering** - Scalable Data Pipeline

## 📘 Overview
Collaborated with a **Data Engineering** project focuses on building a scalable and efficient **data pipeline** to process and transform data from various sources into **Delta Lake** for storage and further processing. This pipeline supports a range of data sources, including **Azure Storage Tables**, **SQL Server**, **MongoDB**, and various **APIs**. The aim is to streamline data ingestion, improve cost efficiency, and ensure that data is available in an optimal format for analysis and machine learning.

![Data Diagram](https://github.com/thanaphongK37/Data-Science-and-Data-Analyst-Project/blob/main/Data_Engineer/Data_Pipeline/Diagramdata%20pipeline.png)

## 🎯 Objective
The main objectives of this project include:
- **Ingest data from multiple sources** (Azure Storage Tables, SQL Server, MongoDB, APIs) into **Delta Lake**.
- **Optimize data ingestion costs** by leveraging an **incremental data loading strategy**, reducing the amount of data transferred and thus cutting down the ingestion cost by over 50%.
- Use **Z-Order Tables** to further optimize data storage and access. This technique helps organize the data efficiently, reducing the need for expensive data scans and speeding up query performance.
- Ensure data **quality, consistency, and timeliness** for downstream processes.
- Create a **monitoring and alerting dashboard** to track the pipeline's performance and provide timely notifications for failures or issues.

---


## 🔧 Technologies Used
- **Azure Data Factory**: For orchestrating the data pipeline and managing data movement between sources and Delta Lake.
- **Azure Databricks**: For data transformation, processing, and optimization within the pipeline.
- **Delta Lake**: For storing the processed data in a reliable and scalable format.
- **SQL Server**: For one of the data sources.
- **MongoDB**: Another source for unstructured data.
- **Azure Storage Tables**: A source for structured data.
- **API Integration**: For ingesting external data.

## 🛠️ Process

1. **Data Ingestion**:
   - The data is ingested from various sources including **SQL Server**, **MongoDB**, **Azure Storage Tables**, and **APIs**.
   - To minimize costs and optimize performance, an **incremental loading strategy** is used instead of the previous full-table copy method.
   - By utilizing the incremental method, only new or updated data is transferred, reducing the load time and size of data to be ingested into **Delta Lake**.
   - This change has led to a **cost reduction of over 50%** in data ingestion.

2. **Z-Order Table Optimization**:
   - To further improve data retrieval performance and reduce costs associated with large table scans, **Z-Order Tables** are used in **Delta Lake**.
   - Z-ordering organizes the data on disk in a way that co-locates related data, reducing the number of file scans and thus improving query performance and reducing storage costs.
   - This technique ensures that queries on frequently accessed data can be executed faster and more efficiently, lowering operational overhead.

3. **Data Transformation (ELT)**:
   - Once the data is ingested into **Delta Lake**, the pipeline processes and transforms it using **Azure Databricks**.
   - The data is cleaned, validated, and structured in a way that makes it ready for downstream analytics and machine learning.

4. **Monitoring & Logging**:
   - A **log collection system** is implemented to monitor the success or failure of each pipeline task.
   - These logs are integrated into a **monitoring dashboard** that provides insights into the pipeline's performance.
   - **Alert notifications** are triggered in case of any pipeline failures, ensuring that the team is alerted in real-time and can take appropriate actions.

5. **Cost Optimization**:
   - By implementing **incremental data loading** and **Z-Order Table** optimization in **Delta Lake**, significant savings are achieved on cloud storage and processing costs.
   - The team continuously monitors the pipeline's efficiency to ensure that the cost remains minimized without compromising data quality or performance.

---

## 📊 Key Metrics
- **Data Ingestion Time**: Time taken to ingest data from each source to Delta Lake.
- **Cost Savings**: Reduction in cost from using incremental loading and Z-Order optimization.
- **Pipeline Success Rate**: The percentage of successful pipeline executions.
- **Alert Notifications**: Number of times alerts were triggered based on failure events.

---

## 🔧 Tools and Libraries
- **Azure Data Factory**: Orchestrating data movement and transformation.
- **Azure Databricks**: For data transformation and processing.
- **Delta Lake**: For storing and managing large-scale data.
- **SQL Server**: Source for structured data.
- **MongoDB**: Source for unstructured data.
- **Azure Storage Tables**: Source for structured data.
- **API Integration**: For pulling in external data.

---

## 🚀 Future Improvements
- **Scalability**: Further optimizations in data processing to handle larger datasets.
- **Advanced Analytics**: Integration of more advanced analytics models into the pipeline.
- **Automated Failure Detection**: Improving the alerting system to detect more nuanced pipeline issues.

---

By implementing the above process and tools, the data pipeline aims to ensure a streamlined, cost-efficient, and reliable data flow from source systems to the data lake, making it ready for analysis and decision-making processes.
