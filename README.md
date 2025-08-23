# 🏥 Health Insurance Claim Prediction  

💡 *Predicting claim amounts using advanced machine learning regression models*  
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)]()
[![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange)]()
[![XGBoost](https://img.shields.io/badge/XGBoost-Regressor-red)]()
[![License](https://img.shields.io/badge/License-MIT-green.svg)]()
[![LightGBM](https://img.shields.io/badge/LightGBM-Regressor-lightgreen)]()
[![Random Forest](https://img.shields.io/badge/RandomForest-Regression-yellowgreen)]()


---

## 🧭 Table of Contents
- [Overview](#-overview)
- [Problem Statement](#-problem-statement)
- [Dataset](#-dataset)
- [Workflow](#-workflow)
- [Model Performance](#-model-performance)
- [Visualizations](#-visualizations)
- [Insights](#-insights)
- [Limitations](#-limitations)
- [Future Work](#-future-work)
- [Tools & Libraries](#-tools--libraries)
- [Conclusion](#-conclusion)
- [Author](#-author)

---

## 🔍 Overview  
This project predicts **medical claim amounts** for health insurance policyholders using demographic, lifestyle, and medical attributes.  
Accurate claim predictions help insurance providers:  
- Set **fair premiums**  
- Detect **fraudulent or excessive claims**  
- Improve **risk management**  
- Design **better policies & benefits**  

---

## 📊 Problem Statement  
- **Goal:** Predict the amount of a claim filed by a policyholder  
- **Type:** Regression Problem  
- **Target Variable:** `Claim` (numeric)  

---

## 📁 Dataset  
- **Name:** Health Insurance Claim Dataset  
- **Source:** Kaggle  
- **Shape:** *(15000, 13)*  

**Features:**  
| Feature                | Type        | Description |
|------------------------|-------------|-------------|
| Age                    | Numeric     | Age of policyholder |
| Sex                    | Categorical | Gender |
| Weight                 | Numeric     | Weight (kg) |
| BMI                    | Numeric     | Body Mass Index |
| Hereditary Diseases    | Categorical | Known hereditary conditions |
| Number of Dependents   | Numeric     | Dependents covered |
| Smoker                 | Binary      | Smoker status (1=yes, 0=no) |
| City                   | Categorical | City of residence |
| Blood Pressure         | Numeric     | Blood pressure level |
| Diabetes               | Binary      | Diabetes status |
| Regular Exercise       | Binary      | Regular exercise (1=yes, 0=no) |
| Job Title              | Categorical | Occupation |
| Claim (Target)         | Numeric     | Amount claimed |

---

## 🧪 Workflow  

### 1️⃣ Data Understanding  
- Loaded dataset with **pandas**  
- Checked missing values, duplicates, and data types  

### 2️⃣ Data Cleaning & Preprocessing  
- Median imputation for missing values (`Age`, `BMI`)  
- Categorical encoding (Sex, City, Hereditary Diseases, Job Title)  
- Outlier removal (**IQR method**)  
- Feature scaling (**StandardScaler**)  

### 3️⃣ Exploratory Data Analysis (EDA)  
- Histograms & boxplots for numeric features  
- Countplots for categorical variables  
- Correlation heatmap for relationships with `Claim`  

### 4️⃣ Feature Engineering  
- BMI categories *(Underweight, Healthy, Overweight, Obese)*  
- Grouped cities into tiers *(optional)*  
- Dropped redundant/uninformative columns  

### 5️⃣ Data Splitting  
- **80% Train / 20% Test** split  

### 6️⃣ Model Training  
Tested multiple regression algorithms:  
- Linear Regression  
- Decision Tree Regressor  
- Random Forest Regressor  
- Gradient Boosting Regressor  
- XGBoost Regressor  

---

## 📊 Model Performance (Regression)

| Model                |   MSE        |   RMSE   |   MAE   |   R²   | Adjusted R² | CV R² Score |
|-----------------------|--------------|----------|---------|--------|-------------|-------------|
| Linear Regression     | 6.10e+07     | 7811.03  | 6051.21 | 0.148  | 0.1399      | 0.7619      |
| Ridge Regression      | 6.10e+07     | 7810.87  | 6051.44 | 0.148  | 0.1400      | 0.7620      |
| Lasso Regression      | 6.10e+07     | 7811.05  | 6051.45 | 0.148  | 0.1399      | 0.7620      |
| **Random Forest** ✅   | **8.28e+06** | **2876.96** | **1300.60** | **0.884** | **0.8833**  | **0.9605** |
| XGBoost Regressor     | 9.83e+06     | 3135.79  | 1799.90 | 0.863  | 0.8614      | 0.9594      |

### ✅ Best Model: Random Forest
- Lowest error values (MSE, RMSE, MAE)  
- Highest R² (0.884), Adjusted R² (0.8833)  
- Excellent generalization (CV R² Score = 0.9605)  

🔥 **Key Predictors:** BMI, Age, Blood Pressure, Smoker status  

---

## 📈 Insights  
- **BMI, Age, and Smoking status** strongly influence claim amounts  
- Higher BMI & smoking habits → **higher claim costs**  
- Healthy lifestyle choices → **lower predicted claims**  

---

## ⚠️ Limitations  
- Small dataset — may not generalize well  
- Missing lifestyle variables (diet, stress)  
- Possible bias from self-reported data  

---

## 🚀 Future Work  
- Integrate additional health/lifestyle datasets  
- Implement **stacked ensemble models** for better accuracy  
- Deploy via **Streamlit** or **Flask**  

---

## 🛠 Tools & Libraries  
- Python  
- pandas, numpy  
- scikit-learn  
- matplotlib, seaborn  
- XGBoost  

---

## 📜 Conclusion  
This project shows that **machine learning regression** can effectively predict health insurance claim amounts.  
Using **Random Forest Regressor** with preprocessing, feature engineering, and tuning, we achieved an **R² of 0.96** and **RMSE 2876.96**.  
Such models can help insurers:  
- Reduce **financial risks**  
- Improve **premium pricing strategies**  
- Promote **healthier lifestyle incentives**  

---

## 👤 Author  
**Mali Satish**  
🎓 *Machine Learning Enthusiast | Data Science Student @ BHU*  

