# **Data Pipeline ELT to Data Lake Using Databricks**  

## 📖 Table of Contents  
1. [Objective](#1-objective)  
2. [Setup Databricks Cluster](#2-setup-databricks-cluster)  
3. [Data Ingestion from Azure Storage](#3-data-ingestion-from-azure-storage)  
4. [Data Transformation using Spark](#4-data-transformation-using-spark)  
5. [Upsert Data to Data Lake](#5-upsert-data-to-data-lake)  

---

## 1. Objective  
This data pipeline is designed to **sync data every 15 minutes** from **Azure Storage** to **Data Lake**. The reason for using **Databricks** over **Azure Data Factory** is its **faster execution time** for high-frequency tasks. While **Azure Data Factory** may take longer to run and incur higher costs, **Databricks** can scale the cluster size down to keep costs lower while providing more flexibility and faster processing.

The concept is to **load historical data** from the **Data Source** for the past **hour** to prevent data loss. The data is then stored in a **temporary table** using **Spark** for further processing. After that, the data will be **upserted** into the main table in the **Data Lake**.

---

## 2. Setup Databricks Cluster  
To get started, you first need to create a **Databricks Cluster** in your Azure environment. The cluster will be responsible for executing the Spark jobs, and since the data sync is done at a high frequency (every 15 minutes), it's important to scale the cluster appropriately to optimize for both **performance** and **costs**.
![ชื่อรูปภาพ](https://github.com/thanaphongK37/Data-Science-and-Data-Analyst-Project/blob/main/Data_Engineer/Data_Pipeline/Data_Pipeline_Using_Databrick/cluster.png)

### Steps:  
1. Navigate to the **Azure Databricks workspace**.  
2. Create a new **cluster** and configure it based on the expected workload.  
3. Set the cluster to **auto-scaling** to manage resource allocation dynamically during the execution.  

---

## 3. Data Ingestion from Azure Storage  
The data ingestion process involves retrieving the data from **Azure Storage** (Blob Storage or Azure Data Lake Store) and loading it into **Databricks**. This is done every 15 minutes to keep the data synced.

 **Step 1**: This Import Library and defind Config for get SASKey From Connect Azure Storage

![ชื่อรูปภาพ](https://github.com/thanaphongK37/Data-Science-and-Data-Analyst-Project/blob/main/Data_Engineer/Data_Pipeline/Data_Pipeline_Using_Databrick/import_lib1.png)

 **Step 2**: Initial pagekage and Define Functions Used:

1. **get_dataframe_from_table_storage** → Retrieves data from Azure Table Storage and converts it into a Spark DataFrame.
2. **transform_value** → Transforms values into the correct format, such as converting datetime and EntityProperty types.
3. **get_data_from_table_storage** → Queries data from Azure Table Storage and applies transform_value to process the retrieved records.get_data_from_table_storage → ใช้ query ข้อมูลจาก Azure Table Storage และเรียกใช้ transform_value 

![ชื่อรูปภาพ](https://github.com/thanaphongK37/Data-Science-and-Data-Analyst-Project/blob/main/Data_Engineer/Data_Pipeline/Data_Pipeline_Using_Databrick/config.png)

![ชื่อรูปภาพ](https://github.com/thanaphongK37/Data-Science-and-Data-Analyst-Project/blob/main/Data_Engineer/Data_Pipeline/Data_Pipeline_Using_Databrick/define_func1.png)
### Process:  
1. **Extract Data**: Use the **Databricks notebook** to extract data from Azure Storage for the past **hour** based on the timestamp parameter.
2. **Incremental Loading**: By using an **incremental loading strategy**, the pipeline will fetch only the new or updated data since the last run, which prevents overloading the system.
3. **Store Temporarily**: The data is initially stored in a **temporary table** using **Spark**.

---

## 4. Data Transformation using Spark  
After the data is ingested, **Spark** is used for data transformation. Spark allows you to perform complex data processing tasks efficiently, which is why it's chosen over other services for this pipeline.
![ชื่อรูปภาพ](https://github.com/thanaphongK37/Data-Science-and-Data-Analyst-Project/blob/main/Data_Engineer/Data_Pipeline/Data_Pipeline_Using_Databrick/spark.png)

### Process:  
1. **While loop**: Used Loop because Run Start cluster All time
2. **Transform the Data**: Perform necessary transformations, such as changing data types or formatting the data.
3. **Load to Temp Table**: After transformation, load the data into a temporary table to be processed in the next step.

---

## 5. Upsert Data to Data Lake  
Once the data is transformed, the next step is to **upsert** the data into the main table in **Data Lake**. This is done to ensure that only the latest data is present in the main table and that no duplicate or outdated records exist.
![ชื่อรูปภาพ](https://github.com/thanaphongK37/Data-Science-and-Data-Analyst-Project/blob/main/Data_Engineer/Data_Pipeline/Data_Pipeline_Using_Databrick/upsert.png)

### Process:  
1. **Define Primary Key**: The upsert process is based on the primary key for each record in the data table.
2. **Merge Data**: Use Spark to merge the data into the main table. Only new or updated records will be inserted, ensuring data consistency.
3. **Store in Data Lake**: After the upsert process, the data is stored in the **Data Lake** in the appropriate format (e.g., **Parquet** or **Delta Lake**).

---

### Process:  
1. **Log Data**: Insert logs into a **monitoring table** that tracks the status of each pipeline run.
2. **Error Handling**: Implement error handling mechanisms, such as retries and alert notifications, to ensure that failures are detected and resolved quickly.

---

With the above setup, this **ELT pipeline** will efficiently handle data ingestion, transformation, and upsert into the **Data Lake** while optimizing for **costs** and **performance**.
