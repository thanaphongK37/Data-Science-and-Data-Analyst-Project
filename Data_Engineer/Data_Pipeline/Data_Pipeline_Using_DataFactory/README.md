# **Data Pipeline ELT to Data Lake**  


## 🎯 Objective  
The objective of this project is to centralize data from multiple sources into a unified Data Lake using an ELT (Extract, Load, Transform) approach with Azure Data Factory. This enables efficient data transformation and the creation of structured data models, making it easier for data analysis, business intelligence, and supporting various operational use cases. By consolidating data in one place, teams can streamline workflows, improve accessibility, and enhance decision-making with high-quality, well-structured data.

 ## 📌 Table of Contents  
1. [Get Latest Data Table in Data Lake](#1-get-latest-data-table-in-data-lake)  
2. [Setup Data Source Connection](#2-setup-data-source-connection)  
3. [Create Schema, Sink, and Data Pipeline](#3-create-schema-sink-and-data-pipeline)  
4. [Upsert New Dataset](#4-upsert-new-dataset)  
5. [Insert Log to Table](#5-insert-log-to-table)  

--

## 1. Get Latest Data Table in Data Lake  
The first step is to create a **Databricks Notebook** to retrieve the **latest timestamp** of the target table. This timestamp helps track the last update for incremental data extraction.  


![ชื่อรูปภาพ](https://github.com/thanaphongK37/Data-Science-and-Data-Analyst-Project/blob/main/Data_Engineer/Data_Pipeline/Data_Pipeline_Using_DataFactory/LastUpdateTable.png)

### Process:  
1. Retrieve the **latest timestamp** from the target table.  
2. Insert this timestamp as a log entry into a **temporary table** in **Azure Storage**.  
3. Create a **lookup tool** to fetch the extracted **timestamp** parameter for further processing.  

---

## 2. Setup Data Source Connection  
Once the latest data timestamp is retrieved, the next step is to set up a **Linked Service** in **Azure Data Factory** to establish connections to various data sources.  
![ชื่อรูปภาพ](https://github.com/thanaphongK37/Data-Science-and-Data-Analyst-Project/blob/main/Data_Engineer/Data_Pipeline/Data_Pipeline_Using_DataFactory/Connection%20LinkedService.png)

Supported data sources include:  
- **Azure Storage**  
- **SQL Server**  
- **MongoDB**  
- **Amazon RDS**  
- **APIs and external data sources**  

This setup ensures seamless data ingestion from various platforms.  

---

## 3. Create Schema, Sink, and Data Pipeline  
The data pipeline is built using **Azure Data Factory Activities** and follows these steps:  

### Process:  
1. **Connect to Data Source** using the configured **Linked Service**.  ![ชื่อรูปภาพ](https://github.com/thanaphongK37/Data-Science-and-Data-Analyst-Project/blob/main/Data_Engineer/Data_Pipeline/Data_Pipeline_Using_DataFactory/Activity%20Sink.png)
2. **Import Schema**: Define the required columns (Note: If the schema is too large, manual adjustments may be needed). ![ชื่อรูปภาพ](https://github.com/thanaphongK37/Data-Science-and-Data-Analyst-Project/blob/main/Data_Engineer/Data_Pipeline/Data_Pipeline_Using_DataFactory/Schema.png) 
3. **Configure Data Sink**: Choose the destination format and storage location, such as:  
   - **Azure Blob Storage**  
   - **Delta Lake**  
   - **ORC, Parquet, or JSON file formats**  ![ชื่อรูปภาพ](https://github.com/thanaphongK37/Data-Science-and-Data-Analyst-Project/blob/main/Data_Engineer/Data_Pipeline/Data_Pipeline_Using_DataFactory/Activity%20Sink.png) 

📌 When the pipeline runs, it extracts only the data **from the last recorded timestamp to the current execution time** and stores it in **Blob Storage**.  

---

## 4. Upsert New Dataset  
📌 **(Updating new data in Data Lake)**  
![ชื่อรูปภาพ](https://github.com/thanaphongK37/Data-Science-and-Data-Analyst-Project/blob/main/Data_Engineer/Data_Pipeline/Data_Pipeline_Using_DataFactory/UpsertData.png)

After data ingestion, **Databricks** is used to **upsert new records** into the target table based on the **Primary Key**. This ensures that only new and modified records are inserted while maintaining data consistency.  

---

## 5. Insert Log to Table  
Once the data update is completed, the **pipeline logs the process execution status** into a monitoring table. This log is essential for **tracking pipeline performance** and identifying potential failures.  
![ชื่อรูปภาพ](https://github.com/thanaphongK37/Data-Science-and-Data-Analyst-Project/blob/main/Data_Engineer/Data_Pipeline/Data_Pipeline_Using_DataFactory/InsertLog.png)

---

## 📌 Additional Notes  
To display a **Data Pipeline Diagram**, use the following Markdown syntax:  

