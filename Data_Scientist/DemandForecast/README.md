# 📌 Demand Forecast Planning Product

## 📖 Project Overview
This project focuses on **demand forecasting** for product manufacturing planning. The goal is to predict the quantity of products that should be produced based on the sales coverage over an **8-month period**. The model utilizes historical sales data and product attributes, along with external economic indicators, to improve prediction accuracy.

---

## 📊 Data Description
The dataset consists of multiple features related to product sales and external economic factors:

### 🛒 1. **Historical Sales Data**
✅ Sales data of each SKU from the first day of sale  
✅ Aggregated monthly sales over different time periods  
✅ **Target variable:** `SO_QTY_8M` (8-month sales quantity)  

### 📦 2. **Product Information**
✅ Product Category  
✅ Product Type and Attributes  

### 🌍 3. **External Economic Indicators**
✅ **Consumer Price Index (CPI)** – Measures the average change in prices paid by consumers  
✅ **Employment Rate** – The number of employed individuals in different professions  
✅ **Unemployment Rate** – The percentage of unemployed individuals by month and year  
✅ **Retail Sales Index** – Measures the overall retail sales performance  

---

## 🛠 Feature Engineering
Several transformations and additional features were created to enhance model performance:
- 📌 Time-based sales aggregation (e.g., rolling window sales, lag features)
- 📌 Categorical encoding for product categories
- 📌 Scaling and normalization for numerical features
- 📌 Feature interactions between product attributes and external indicators

---

## 🤖 Model Training & Evaluation
A machine learning model was trained to predict **SO_QTY_8M** using **XGBoost**. The dataset was split into training and validation sets to evaluate performance.

### 📌 **Model Performance Metrics:**
- **📈 Explained Variance Score (R²):** `0.848`
- **📉 Mean Absolute Error (MAE):** `75.98`
- **📊 Median Absolute Error (MedAE):** `40.43`

---

## 📊 Results 
The model's prediction performance was evaluated by comparing actual vs. predicted sales:

  ![ชื่อรูปภาพ](https://github.com/thanaphongK37/Data-Science-and-Data-Analyst-Project/blob/main/Data_Scientist/DemandForecast/Distribution.png)  
📌 First Image: The performance metrics of the XGBoost model show an R² of 0.848, which indicates that the model explains a substantial portion of the variance. However, the MAE of 75.98 suggests that there is still room for improvement in minimizing absolute prediction errors.


 ![ชื่อรูปภาพ](https://github.com/thanaphongK37/Data-Science-and-Data-Analyst-Project/blob/main/Data_Scientist/DemandForecast/Evaluate%20Model.png)  
  ![ชื่อรูปภาพ](https://github.com/thanaphongK37/Data-Science-and-Data-Analyst-Project/blob/main/Data_Scientist/DemandForecast/Evaluate%20Model2.png)  
📌 Second Image: The scatter plot of Predicted vs. Actual sales shows a generally positive correlation, but there is still some deviation for higher values. This might suggest that the model underestimates high-demand products or overestimates low-demand products. Further fine-tuning, such as adjusting feature selection or hyperparameter optimization, could improve accuracy.

---

## 🎯 Conclusion
✅ The model demonstrates **high predictive power** (R² = 0.848), indicating a strong ability to forecast demand.  
✅ **External economic indicators** contributed significantly to improving accuracy.  
✅ Future improvements could include **deep learning approaches** or incorporating **real-time market trends**.  

---



---

✨ **Author:** Tanapong ketsin  
