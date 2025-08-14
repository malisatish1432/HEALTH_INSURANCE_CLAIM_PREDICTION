# 🏥 Health Insurance Claim Prediction

**💡 Predicting claim amounts using advanced machine learning regression models**

---

## 🔍 Overview
This project aims to predict **medical claim amounts** for health insurance policyholders based on demographic, lifestyle, and medical attributes.  
Accurate claim prediction helps insurance providers:
- Set **fair premiums** for customers  
- Detect **fraudulent or excessive claims**  
- Improve **risk management**  
- Design **better policies & benefits**

---

## 📊 Problem Statement
- **Goal:** Predict the amount of a claim (numeric) filed by a policyholder  
- **Type:** Regression Problem  
- **Target Variable:** `Claim`

---

## 📁 Dataset
- **Name:** Health Insurance Claim Dataset  
- **Source:** *Kaggle*  
- **Dataset Shape:** ~ *(15000,13)*  

**Features:**
- **Age** – Age of the policyholder (numeric)  
- **Sex** – Gender (categorical)  
- **Weight** – Weight in kilograms (numeric)  
- **BMI** – Body Mass Index (numeric)  
- **Hereditary Diseases** – Known hereditary conditions (categorical)  
- **Number of Dependents** – Number of dependents covered (numeric)  
- **Smoker** – Smoker status (binary: 1 = yes, 0 = no)  
- **City** – City of residence (categorical)  
- **Blood Pressure** – Blood pressure level (numeric)  
- **Diabetes** – Has diabetes (binary: 1 = yes, 0 = no)  
- **Regular Exercise** – Exercises regularly (binary)  
- **Job Title** – Occupation (categorical)  
- **Claim** – **Target:** Amount claimed (numeric)  

---

## 🧪 Workflow

### 1️⃣ Data Understanding
- Loaded dataset using **pandas**  
- Previewed data with `.head()`, `.info()`, `.describe()`  
- Checked for **missing values**, **duplicates**, and **data types**

### 2️⃣ Data Cleaning & Preprocessing
- Median imputation for missing values (`Age`, `BMI`)  
- Encoding of categorical features (`Sex`, `City`, `Hereditary Diseases`, `Job Title`)  
- Outlier removal using **IQR method**  
- Feature scaling with **StandardScaler**

### 3️⃣ Exploratory Data Analysis (EDA)
- Histograms & boxplots for numeric features  
- Countplots for categorical variables  
- Correlation heatmap for relationships with claim amount

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
- **✅ Random Forest Regressor (Best performer)**  
- Gradient Boosting Regressor  
- XGBoost Regressor

### 7️⃣ Model Evaluation
Metrics used:
- **R² Score**
- **Mean Absolute Error (MAE)**
- **Mean Squared Error (MSE)**
- **Root Mean Squared Error (RMSE)**

📌 **Best Model:** Random Forest Regressor  
📌 **R² Score:** *0.96*  
📌 **RMSE:** *2289.23*  

### 8️⃣ Hyperparameter Tuning
- Tuned **Random Forest** parameters with **GridSearchCV**

### 9️⃣ Feature Importance
- Top predictors:
  - **BMI**
  - **Age**
  - **Blood Pressure**
  - **Smoker status**

---

## 📈 Insights
- **BMI, Age, and Smoking status** significantly influence claim amounts  
- High BMI & smoking habits are linked to **higher claim costs**  
- Healthy lifestyle choices (exercise, no smoking) reduce predicted claims

---

## ⚠️ Limitations
- Small dataset — may not generalize to all populations  
- Missing health/lifestyle variables (diet, stress, etc.)  
- Potential bias from **self-reported data**

---

## 🚀 Future Work
- Add external health/lifestyle datasets  
- Implement **stacked ensemble models** for higher accuracy  
- Deploy using **Streamlit** / **Flask** for real-time predictions

---

## 🛠 Tools & Libraries
- **Python**
- **pandas**, **numpy**
- **scikit-learn**
- **matplotlib**, **seaborn**
- **XGBoost**

---

## 📜 Conclusion
This project demonstrates how **machine learning regression** can effectively estimate health insurance claim amounts based on demographic and lifestyle factors.  
By leveraging **Random Forest Regressor** with proper preprocessing, feature engineering, and hyperparameter tuning, we achieved strong predictive performance.  
Such models can help insurance companies:
- Reduce **financial risks**
- Improve **premium pricing strategies**
- Promote **healthier lifestyle incentives**

---

## 👤 Author
**Mali Satish**  
*🎓 Machine Learning Enthusiast | Data Science Student @ BHU*
