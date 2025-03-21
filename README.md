# Telcho_Churn
# Telco Customer Churn Prediction

## Project Overview
This project aims to develop a machine learning model to predict customer churn in a fictional telecom company. The dataset contains information about 7,043 customers receiving phone and internet services in California. The goal is to identify patterns that indicate whether a customer is likely to leave the company.

## Dataset Information
The dataset consists of **21 variables** and **7,043 observations**. Each row represents a unique customer, and the features include demographic details, account information, and services subscribed.

### **Key Features:**
- **CustomerID**: Unique identifier for each customer
- **Demographics**: Gender, SeniorCitizen, Partner, Dependents
- **Services**: PhoneService, MultipleLines, InternetService, OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, StreamingTV, StreamingMovies
- **Account Information**: Contract type, PaperlessBilling, PaymentMethod, MonthlyCharges, TotalCharges
- **Target Variable**: **Churn** (whether the customer left the service: Yes/No)

## Tasks and Methodology

### **1. Exploratory Data Analysis (EDA)**
- Identify numerical and categorical variables.
- Handle type mismatches and analyze feature distributions.
- Examine relationships between categorical variables and the target variable.
- Detect and handle outliers.
- Check for missing values and apply necessary treatments.

### **2. Feature Engineering**
- Handle missing and outlier values appropriately.
- Create new meaningful features, such as:
  - Engaged customers based on contract type.
  - Customers with no protection services.
  - Monthly contract customers who are young.
  - Total number of services subscribed.
  - Auto-payment flag.
- Apply **Label Encoding** for binary categorical variables.
- Perform **One-Hot Encoding** for multi-class categorical variables.
- Standardize numerical features if necessary.

### **3. Modeling**
- Train multiple classification models:
  - Logistic Regression (LR)
  - K-Nearest Neighbors (KNN)
  - Decision Tree (CART)
  - Random Forest (RF)
  - XGBoost (XGB)
  - LightGBM
  - CatBoost
- Evaluate models using **10-fold Cross-Validation** on:
  - Accuracy
  - F1 Score
  - ROC-AUC
  - Precision
  - Recall
- Select the top 4 models based on performance.
- Perform **Hyperparameter Tuning** for selected models and retrain them.

## Results & Next Steps
- Compare model performances and interpret results.
- Deploy the best-performing model.
- Explore feature importance and further optimize.
- Potential integration with a real-time churn prediction system.

## Requirements
- Python 3.x
- Libraries: `pandas`, `numpy`, `sklearn`, `xgboost`, `lightgbm`, `catboost`

## How to Run the Project
1. Install dependencies:
   ```bash
   pip install pandas numpy scikit-learn xgboost lightgbm catboost
   ```
2. Load the dataset into a Pandas DataFrame.
3. Run the feature engineering script.
4. Train and evaluate models.
5. Analyze and interpret results.

---

This project provides a structured approach to churn prediction and can be extended for real-world business applications.

