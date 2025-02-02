# **Fraud Detection**

## 📘 Overview  
This **Fraud Detection** project is developed in collaboration with the **Data Scientist Team Lead**. The goal is to build fraud detection mechanisms by analyzing identity patterns and transaction behaviors, focusing on **Identity Fullname Verification** and **Redeem Scoring** metrics.  

## 🎯 Objective  
The primary objectives of this project are:  
1. **Identity Fullname Verification**: Detect potential fraudulent identities by analyzing name structures.  
2. **Redeem Scoring**: Evaluate and score redemption behavior to identify suspicious activities.  

---

## 🧑‍💻 Approach  

### **1️⃣ Identity Fullname Verification**  
- Explored multiple techniques for **language detection**, **phonetic similarity**, and **named entity recognition (NER)**.  
- Tested different models such as:  
  - **Rule-based methods** using `pythainlp` for tokenization, soundex (`lk82`), pronunciation analysis, and spell checking.  
  - **Machine learning models** like `RandomForestClassifier` and `LogisticRegression`.  
  - **Deep learning models** such as `AutoTokenizer` and `AutoModelForTokenClassification` from `transformers`, which yielded the best performance.  

### **2️⃣ Redeem Scoring (RDM)**
Developed **multiple scoring metrics** to evaluate customer redemption behavior:  

#### **📌 Redeem Timing (RDM_Timing)**  
- **Published Date - Redeem Date (RDM_TimingPublished)**: Measures the time gap between coupon publication and redemption.  
- **Closest Redeem (RDM_TimingCloset)**: Detects if a user redeems multiple coupons in quick succession.  
- **Latest Redeem (Recency) (RDM_TimingLatest)**: Tracks the most recent redemption activity.  

#### **📌 Redeem Distribution (RDM_Distribution)**  
- **By Campaign Type (RDM_DistributionByCampaignType)**: Analyzes redemption trends across different campaign types.  
- **By Period (Time/Hr) (RDM_DistributionPeriod)**: Identifies peak redemption times.  

#### **📌 Redeem Frequency (RDM_Frequency)**  
- **By Period (Days) (RDM_FrequencyByDays)**: Evaluates how frequently a user redeems over time.  
- **By Times (Times) (RDM_FrequencyByTimes)**: Measures total redemption count per user.  

**📊 Current Status**  
- **Identity Fullname Verification**: Model trained and evaluated.  
- **Redeem Scoring**: Metrics are being monitored via dashboards. Model training is yet to begin.  

---

## 🔧 Technologies Used  

- **Python**: Core programming language.  
- **Pandas & NumPy**: For data preprocessing and analysis.  
- **PyThaiNLP**: For Thai language processing, tokenization, phonetics, and spell checking.  
- **Langdetect & Langid**: For language detection.  
- **Transformers (Hugging Face)**: For deep learning-based name recognition.  
- **Scikit-learn**: For traditional machine learning models.  
- **PySpark**: For large-scale data processing.  

