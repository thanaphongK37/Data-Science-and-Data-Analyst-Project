# **Recommendation System**

## 📘 Overview  
The **Recommendation System** project focuses on building a recommendation engine that suggests relevant products or services to users based on text-based similarity and classification models.  

## 🎯 Objective  
The goal of this project is to develop a recommendation system using **TF-IDF (Term Frequency-Inverse Document Frequency)** and **machine learning models** to provide personalized suggestions.  

## 🧑‍💻 Approach  

### **Exploratory Data Analysis (EDA)**  
- Used **word_tokenize** from `pythainlp` to tokenize and clean text data for better matching of words.  

### **Feature Selection**  
- Used **TF-IDF Vectorizer** (`TfidfVectorizer`) to transform text into numerical feature vectors.  
- Applied **cosine similarity** and **linear kernel** to measure the similarity between different text inputs.  

### **Model Training & Prediction**  
- Trained a **Random Forest Classifier** and **Gradient Boosted Trees (GBTClassifier)** for classification tasks.  
- Tracked experiments using **MLflow**.  
- Evaluated model performance using **MulticlassClassificationEvaluator**.  

---

## 🔧 Technologies Used  

- **Python**: Programming language for data analysis and machine learning.  
- **Pandas & NumPy**: For data manipulation and preprocessing.  
- **Matplotlib & Seaborn**: For data visualization.  
- **PySpark**: For handling large-scale data processing and ML model training.  
- **TfidfVectorizer**: For transforming text data into numerical vectors.  
- **scikit-learn**: For cosine similarity calculation and classification models.  
- **MLflow**: For experiment tracking and model version control.  
- **PyThaiNLP**: For Thai text tokenization.  

