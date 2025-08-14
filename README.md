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
## 🚀 Regression Results  

| Model                 | MSE           | RMSE        | MAE         | R²       | Adjusted R² |
|-----------------------|--------------:|------------:|------------:|---------:|------------:|
| Linear Regression     | 61012230.0    | 7811.03     | 6051.21     | 0.1478   | 0.1399      |
| Ridge Regression      | 61009670.0    | 7810.87     | 6051.44     | 0.1478   | 0.1400      |
| Lasso Regression      | 61012560.0    | 7811.05     | 6051.45     | 0.1478   | 0.1399      |
| ElasticNet Regression | 60669980.0    | 7789.09     | 6063.14     | 0.1526   | 0.1448      |
| Random Forest         | **8276888.0** | **2876.96** | **1300.60** | **0.8844*| **0.8833**|
| XGBoost Regressor     | 9833185.0     | 3135.79     | 1799.90     | 0.8626   | 0.8614      |

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
### 🔸Using Random Forest Regressor, we achieved an R² Score of 0.8844 with a low MAE, making it effective for predicting claim amounts.
### 🔸This approach can help insurance companies reduce risk, improve pricing models, and detect anomalies in claims processing.
