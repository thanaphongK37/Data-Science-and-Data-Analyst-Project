# **Churn Prediction**

## 📘 Overview  
The **Churn Prediction** project focuses on identifying customers who are likely to stop using a service. By leveraging **machine learning models**, businesses can proactively engage with at-risk customers to improve retention.  

## 🎯 Objective  
The objective of this project is to build a predictive model that estimates the likelihood of customer churn based on various behavioral and transactional features.  

## 🧑‍💻 Approach  

### **Feature Engineering**  
- Created features based on customer insights, including:  
  - **Age group** segmentation  
  - **Number of active days**  
  - **Purchase history**  
  - **Redemption history**  

### **Exploratory Data Analysis (EDA)**  
- Analyzed customer survival rates using **Kaplan-Meier Estimator**.  
- Calculated **Confidence Interval (95%)** to estimate how long customers remain active before churning.  
- Visualized feature correlation and trends using **Seaborn** and **Matplotlib**.  

### **Data Preprocessing**  
- Applied **Label Encoding** for categorical features.  
- Performed **Principal Component Analysis (PCA)** for dimensionality reduction.  

### **Model Training & Prediction**  
- Used **XGBoost** as the primary classification model.  
- Applied **K-Fold Cross Validation** to evaluate model performance.  
- Tracked experiments and model performance using **MLflow**.  

---

## 🔧 Technologies Used  

- **Python**: Programming language for data analysis and machine learning.  
- **Pandas & NumPy**: For data manipulation and feature engineering.  
- **Matplotlib & Seaborn**: For data visualization.  
- **Lifelines**: For survival analysis (Kaplan-Meier Estimator, Cox Proportional Hazards Model).  
- **XGBoost**: For churn classification modeling.  
- **scikit-learn**: For feature correlation analysis, PCA, and model evaluation.  
- **MLflow**: For experiment tracking and model version control.  
- **PySpark**: For large-scale data processing.  

