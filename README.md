#  Health Insurance Claim Prediction

## 🏥 Project Overview :
### 🔸 This project predicts the medical claim amount a policyholder might request using machine learning regression   models.
### 🔸 The dataset contains demographic, health, and insurance-related details.
### 🔸The goal is to help insurance companies estimate claim costs accurately to improve pricing strategies, detect potential fraud, and ensure financial stability.
## 🎯 Why It Matters :
### 🔸Price premiums fairly for customers.
### 🔸Detect overuse or fraudulent claims.
### 🔸Plan reserves & reduce financial risks.
### 🔸Improve healthcare benefits and policy efficiency.
### 🔸Keep insurance affordable while maintaining profitability.
## 📊 Dataset Summary :
### 🔸Target Variable:
#### 🔸 claim (numeric) → amount of money claimed by the policyholder.
### 🔸Features include:
#### 🔸Demographic: Age, Sex, Number of Dependents.
#### 🔸Health: Weight, BMI, Hereditary Diseases, Chronic Diseases, Height.
#### 🔸Insurance-related: Insurance Plan, Previous Claims, Employment Status.
# 🛠 Approach :
### 🔸1. Data Preprocessing :
#### 🔸Handling missing values with SimpleImputer.
#### 🔸Encoding categorical variables using OneHotEncoder & LabelEncoder.
#### 🔸Feature scaling with StandardScaler.
#### 🔸Removing multicollinearity using Variance Inflation Factor (VIF).
### 🔸2. Model Training & Comparison :
#### 🔸 Linear Regression
#### 🔸Ridge & Lasso Regression
#### 🔸ElasticNet Regression
#### 🔸Random Forest Regressor (Best Performer)
### 🔸3. Evaluation Metrics :
#### 🔸Mean Squared Error (MSE)
#### 🔸Mean Absolute Error (MAE)
#### 🔸R² Score
# 🚀 Results :
### 🔸Model	R² Score	MAE	MSE
### 🔸Random Forest	0.93	120.5	28045
### 🔸Ridge Regression	0.88	155.2	39012
### 🔸Linear Regression	0.86	162.8	42567
### 🔸📌 Random Forest Regressor was chosen as the final model due to its highest accuracy and lowest error.
# 📈 Visualizations :
### 🔸Feature Correlation Heatmap
### 🔸Actual vs Predicted Claims Plot
### 🔸Residual Error Distribution
### 🔸Feature Importance (Random Forest)
# 🖥 Tech Stack :
### 🔸Python: Pandas, NumPy, Scikit-learn, Statsmodels, Matplotlib, Seaborn
### 🔸Environment: Jupyter Notebook
# 📜 Conclusion :
### 🔸Using Random Forest Regressor, we achieved an R² Score of 0.93 with a low MAE, making it effective for predicting claim amounts.
### 🔸This approach can help insurance companies reduce risk, improve pricing models, and detect anomalies in claims processing.
