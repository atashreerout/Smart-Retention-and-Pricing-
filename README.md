# 🤖 Machine Learning Projects: Customer Churn Prediction & Airbnb Price Prediction

This repository contains two end-to-end machine learning projects:
1. **Customer Churn Prediction (Classification)**
2. **Airbnb Price Prediction (Regression)**

Both projects involve complete workflows including data cleaning, preprocessing, feature engineering, model development, evaluation, and interpretation. The objective is to build predictive models that support real-world business decisions.

---

# 📌 Project 1 — Customer Churn Prediction (Classification)

## 🔍 Objective
To develop a machine learning model that predicts whether a customer will churn based on demographics, account details, and service usage patterns. This allows businesses to proactively target at-risk customers and improve retention.

---

## 📂 Dataset Summary
**Dataset:** Customer_data  
**Target Variable:** `Churn` (Yes/No)

Key features include:
- Customer demographics (Gender, SeniorCitizen, Dependents)
- Account features (Contract type, Billing method, Tenure)
- MonthlyCharges, TotalCharges
- Internet, Phone, and Streaming service details

---

## 🛠️ Workflow

### **1️⃣ Data Exploration & Cleaning**
- Identified missing values and replaced invalid entries  
- Converted categorical values to standardized formats  
- Transformed `TotalCharges` to numeric  
- Removed irrelevant columns like `customerID`  

### **2️⃣ Preprocessing**
- Used **OneHotEncoder** for categorical variables  
- Used **StandardScaler** for numerical variables  
- Built a **pipeline** to automate preprocessing steps  
- Ensured reproducibility by saving the preprocessing pipeline  

### **3️⃣ Model Development**
Trained multiple models using **GridSearchCV** with cross-validation:
- Logistic Regression  
- Random Forest  
- Gradient Boosting  
- XGBoost  

**Evaluation Metric:** F1 Score (to balance precision & recall)

### **4️⃣ Best Model**
- **Logistic Regression** achieved the best performance  
- **Test Accuracy:** ~0.80  
- **F1 Score:** ~0.59  

### **5️⃣ Key Insights**
- Customers with:
  - Short tenure  
  - Month-to-month contract  
  - No online security or tech support  
  are more likely to churn.

### **6️⃣ Recommendations**
- Offer incentives to convert customers to long-term contracts  
- Improve online security & tech support services  
- Target customers with high churn-probability scores  

### **7️⃣ New Customer Prediction**
The final pipeline predicts:
- Whether a new customer will churn (0/1)  
- Probability of churn (%)  

---

# 📌 Project 2 — Airbnb Listing Price Prediction (Regression)

## 🔍 Objective
To build a regression model that predicts Airbnb listing prices based on listing characteristics such as property type, amenities, location, reviews, and host behavior.

---

## 📂 Dataset Summary
Contains 29 features including:
- Property type, room type  
- Number of reviews  
- Amenities  
- Host details  
- Latitude/Longitude  
- Availability metrics  

---

## 🛠️ Workflow

### **1️⃣ Data Cleaning & Feature Engineering**
- Handled missing values using median/mode imputation  
- Standardized text fields and removed irrelevant columns  
- Added new engineered features:
  - **Number of amenities**
  - **Host response rate**
  - **Neighborhood popularity**
  - **Host seniority (days since host_since)**
  - **Host total listings count**

### **2️⃣ Train/Validation/Test Split**
- Train: 60%  
- Validation: 20%  
- Test: 20%  

### **3️⃣ Model Development**
Trained and compared:
- Linear Regression  
- Random Forest Regressor  
- XGBoost Regressor (best)  

### **4️⃣ Best Model — Tuned XGBoost**
Hyperparameters:
- learning_rate: 0.05  
- max_depth: 7  
- n_estimators: 400  
- subsample: 0.8  

### **Performance**
- **Test RMSE (log space): 0.3854**  
- **Test R²: 0.7109**

### **5️⃣ Insights**
Most influential features:
- Neighborhood popularity  
- Property type & room type  
- Number of reviews  
- Host seniority  
- Amenities  

### **6️⃣ Recommendations**
- Offer more amenities to improve pricing potential  
- Encourage guests to leave reviews  
- Optimize pricing based on neighborhood trends  

---



