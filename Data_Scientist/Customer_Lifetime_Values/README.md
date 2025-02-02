# **Customer Lifetime Value (CLV) Prediction**

## 📘 Overview  
The **Customer Lifetime Value (CLV)** project aims to estimate the total revenue a business can expect from a customer throughout their relationship. Understanding CLV helps businesses optimize marketing strategies, customer retention efforts, and personalized promotions.  

## 🎯 Objective  
The goal of this project is to use **probabilistic modeling techniques** to estimate the lifetime value of each customer based on purchasing behavior.  

## 🧑‍💻 Approach  

### **Data Preprocessing**  
- Handled **missing values** to ensure data quality.  
- Extracted **RFA Metrics** (Recency, Frequency, and Age) for customer behavior analysis:  
  - **Recency (R)**: The number of days between a customer's first and most recent purchase.  
  - **Frequency (F)**: The number of distinct purchase days a customer has made transactions.  
  - **Age (T)**: The time difference (in days) between the first purchase and the last recorded transaction.  

### **Model Training & Prediction**  
- Applied **BetaGeoFitter** to predict **customer retention probability**.  
- Used **GammaGammaFitter** to estimate **expected monetary value per customer**.  
- Evaluated customer lifetime value using **Pareto/NBD and BG/NBD models**.  
- Visualized customer purchasing behavior using **Lifetimes** library.  
- Tracked model training and performance using **MLflow**.  

---

## 🔧 Technologies Used  

- **Python**: Programming language for data analysis and machine learning.  
- **Pandas & NumPy**: For data manipulation and feature engineering.  
- **Matplotlib & Seaborn**: For data visualization.  
- **Lifetimes**: For customer transaction modeling (BetaGeoFitter, GammaGammaFitter, Pareto/NBD model).  
- **MLflow**: For experiment tracking and model version control.  
- **PySpark**: For large-scale data processing.  

