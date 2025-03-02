# **Data Model** - Optimizing Data for Analytics and Insights

## 📘 Overview
The **Data Model** project focuses on transforming raw data ingested into **Delta Lake** into structured, organized datasets that can be easily accessed and analyzed by the **Data Science**, **Data Analyst**, and **Support** teams. The structured data is stored in a **Data Warehouse** to allow fast and efficient data querying, enabling teams to derive insights and create visualizations more effectively.

![ชื่อรูปภาพ](https://github.com/thanaphongK37/Data-Science-and-Data-Analyst-Project/blob/main/Data_Engineer/Data_Model/Diagram%20data%20Model.png)


## 🎯 Objective
The goal of this project is to build a **Data Model** that:
- **Data Warehouse**: Organizes the data into a **Data Warehouse**, where different models are stored and structured to facilitate easier querying and faster processing.
- **Optimized for Performance**: Ensures that data is easily accessible for **Data Science**, **Data Analyst**, and **Support** teams, making the querying and reporting process much faster, which is crucial for timely decision-making.

## 🔧 Technologies Used
- **Azure Databricks**: For processing and transforming data.
- **Delta Lake**: For storing raw and processed data in a scalable and reliable format.
- **SQL Server**: For structured data storage.
- **Azure Data Factory**: For orchestration of the ETL pipeline.
- **Data Warehouse**: Used for storing optimized data models.

## Data Modelling
![ชื่อรูปภาพ](https://github.com/thanaphongK37/Data-Science-and-Data-Analyst-Project/blob/main/Data_Engineer/Data_Model/datamodel%20diagram.png)


## 🛠️ Process

1. **Create Delta Table**:
   - Create table Schema follow Unity Catalog
   -  ![ชื่อรูปภาพ](https://github.com/thanaphongK37/Data-Science-and-Data-Analyst-Project/blob/main/Data_Engineer/Data_Model/Create_delta_table.png)
  
3. **Tranfrom data**:
   - Create a script for transforming data into a Data Warehouse for use in Data Science and Data Analytics projects, enabling Machine Learning or Visualization tasks.
   - ![ชื่อรูปภาพ](https://github.com/thanaphongK37/Data-Science-and-Data-Analyst-Project/blob/main/Data_Engineer/Data_Model/update_data_to_datamodel.png)
   

4. **Support for Downstream Use**:
   - The **Data Warehouse** makes it easier for **Support teams** to pull data for customer service, billing inquiries, and troubleshooting.
   - The data is structured to ensure that it is easy to access without having to go through raw data, saving time and effort.

---

## 📊 Key Metrics
- **Data Load Time**: Time taken to load data into the Data Warehouse from **Delta Lake**.
- **Query Performance**: Speed and efficiency of queries performed on the **Data Warehouse**.
- **Data Accuracy**: The correctness and completeness of the data after it has been processed and loaded into the Data Warehouse.

---

## 🔧 Tools and Libraries
- **Azure Databricks**: For transforming data and running processing jobs.
- **Delta Lake**: For storing raw and processed data.
- **Azure Data Factory**: For orchestrating the ETL pipeline and managing data flow.
- **SQL Server**: For storing structured data in the **Data Warehouse**.
- **Data Warehouse**: For storing and organizing transformed data models for easy access.

---

## 🚀 Future Improvements
- **Data Quality Monitoring**: Implement automated checks to ensure data quality throughout the ETL process.
- **Real-Time Data Ingestion**: Develop capabilities for real-time data processing and analysis.
- **Advanced Data Models**: Explore and build more advanced data models to support more complex analytics use cases.

---

By creating a structured and optimized **Data Model**, this project aims to streamline the process of data retrieval, making it easier and faster for teams to perform analytics and derive insights from the data, ultimately driving better business decision-making.
