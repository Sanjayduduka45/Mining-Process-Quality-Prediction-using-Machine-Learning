# Mining Process Quality Prediction using Machine Learning

## Overview

This project focuses on predicting **Silica Concentrate (%)** in a mining flotation plant using Machine Learning techniques. The dataset contains various process parameters such as ore characteristics, reagent flow rates, air flow measurements, and flotation column levels collected from a mineral processing plant.



---

## Problem Statement

In mining industries, maintaining the desired quality of concentrate is very important. Manual monitoring of process variables is difficult because a large number of parameters influence the final output.

The goal of this project is to develop a Machine Learning model that predicts **% Silica Concentrate** using flotation process measurements.

---

## Dataset Information

* Dataset: Mining Process Flotation Plant Database
* Records: 736,000+
* Features: 24 Process Variables
* Target Variable: `% Silica Concentrate`

### Sample Features

* % Iron Feed
* Starch Flow
* Amina Flow
* Ore Pulp Flow
* Ore Pulp pH
* Ore Pulp Density
* Flotation Column Air Flows
* Flotation Column Levels

---

## Project Workflow

### 1. Data Preprocessing

* Loaded dataset using Pandas
* Removed duplicate records
* Checked missing values
* Converted date column into datetime format

### 2. Feature Engineering

Extracted useful time-based features from date column:

* Month
* Day
* Hour
* Day of Week

### 3. Exploratory Data Analysis (EDA)

* Distribution Analysis
* Boxplots
* Correlation Analysis
* Outlier Detection

### 4. Feature Selection

Removed highly correlated features to reduce redundancy and improve model performance.

### 5. Model Building

The following regression models were trained and compared:

* Linear Regression
* Random Forest Regressor
* XGBoost Regressor
* LightGBM Regressor
* CatBoost Regressor

### 6. Hyperparameter Tuning

Performed RandomizedSearchCV on the best-performing model to improve prediction performance.

### 7. Model Interpretation

* Feature Importance Analysis
* SHAP Analysis
* Actual vs Predicted Comparison
* Residual Analysis

---

## Model Performance

| Model             | R² Score              |
| ----------------- | --------------------- |
| Linear Regression | Baseline              |
| Random Forest     | Best Performing Model |
| XGBoost           | Evaluated             |
| LightGBM          | Evaluated             |
| CatBoost          | Evaluated             |

Final Random Forest model achieved strong predictive performance on unseen test data.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* XGBoost
* LightGBM
* CatBoost
* SHAP
* Streamlit

---

## Project Structure

```text
Mining-Process-Quality-Prediction/

│
├── mining.ipynb
├── app.py
├── mining_quality_model.pkl
├── feature_names.pkl
├── requirements.txt
├── README.md
└── dataset/
```

---

## Streamlit Application

A simple Streamlit application was developed to allow users to manually enter process parameters and predict Silica Concentrate values using the trained model.

---

## Author

**Sanjay Duduka**

B.Tech Computer Science and Engineering

SR University, Warangal

GitHub: https://github.com/Sanjayduduka45

LinkedIn: https://www.linkedin.com/in/sanjayduduka/

---

## Conclusion

This project demonstrates the complete Machine Learning workflow from data preprocessing and feature engineering to model training, hyperparameter tuning, interpretation, and deployment. The developed model can assist mining industries in predicting silica concentrate levels and improving process efficiency through data-driven decision making.
