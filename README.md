# ⛏️ Mining Process Quality Prediction using Machine Learning

Predicting **Silica Concentrate (%)** in a mineral flotation process using **Machine Learning** to improve process quality, operational efficiency, and production monitoring.

> **Project Notebook:**
> [Mining Process Quality Prediction Notebook](https://github.com/Sanjayduduka45/Mining-Process-Quality-Prediction-using-Machine-Learning/blob/main/mining.ipynb?utm_source=chatgpt.com)

---

# 📖 Overview

Mineral flotation is one of the most critical stages in the mining industry, where process parameters directly influence the quality of the final concentrate. Small variations in operating conditions such as air flow, pulp density, reagent flow, and feed composition can significantly affect the percentage of silica in the concentrate.

This project develops a **Machine Learning regression model** capable of predicting **% Silica Concentrate** from real-time flotation process measurements. The notebook demonstrates an end-to-end machine learning workflow including data cleaning, exploratory data analysis (EDA), outlier analysis, feature selection, model training, evaluation, and interpretation.

---

# 🎯 Problem Statement

The goal is to accurately predict the **% Silica Concentrate** produced during the flotation process using operational sensor data.

Accurate predictions help:

* Improve concentrate quality
* Monitor plant performance
* Reduce process variability
* Support data-driven operational decisions
* Increase production efficiency

---

# 📂 Dataset Information

| Property        | Value                    |
| --------------- | ------------------------ |
| Domain          | Mining Process           |
| Problem Type    | Supervised Regression    |
| Dataset Size    | 50,000 Records           |
| Features        | 24 Columns               |
| Target Variable | **% Silica Concentrate** |

---

# ⚙️ Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-Learn
* XGBoost
* LightGBM
* CatBoost

---

# 📊 Project Workflow

```
Mining Process Dataset
          │
          ▼
Data Inspection
          │
          ▼
Data Cleaning
          │
          ▼
Exploratory Data Analysis
          │
          ▼
Duplicate Removal
          │
          ▼
Missing Value Analysis
          │
          ▼
Outlier Detection (IQR)
          │
          ▼
Feature Selection
          │
          ▼
Train-Test Split
          │
          ▼
XGBoost Regression Model
          │
          ▼
Prediction
          │
          ▼
Performance Evaluation
          │
          ▼
Feature Importance Analysis
```

---

# 🔍 Exploratory Data Analysis

The notebook includes comprehensive exploratory analysis before model development.

### Dataset Inspection

* Dataset shape
* Feature names
* Data types
* Statistical summary

### Data Quality Checks

* Duplicate record detection
* Duplicate removal
* Missing value analysis
* Removal of unnecessary Date column

### Target Variable Analysis

* Distribution Plot
* Kernel Density Estimation (KDE)
* Box Plot

### Outlier Analysis

Outliers were detected using the **Interquartile Range (IQR)** method.

The percentage of outliers was calculated for every numerical feature to understand process variability before model training.

---

# 🛠 Data Preprocessing

The preprocessing pipeline consists of:

* Removing duplicate records
* Removing the Date feature
* Selecting numerical process variables
* Feature selection
* Train-Test Split (80% Training / 20% Testing)

### Dataset Split

| Dataset  | Samples |
| -------- | ------- |
| Training | 39,999  |
| Testing  | 10,000  |

---

# 🎯 Target Variable

```
% Silica Concentrate
```

---

# 🤖 Machine Learning Model

The final regression model used is:

## XGBoost Regressor

### Hyperparameters

```python
XGBRegressor(
    n_estimators=200,
    learning_rate=0.03,
    max_depth=8,
    subsample=0.8,
    colsample_bytree=0.8,
    random_state=42
)
```

---

# 📈 Model Performance

The trained model achieved the following performance:

| Metric                             | Score      |
| ---------------------------------- | ---------- |
| **R² Score**                       | **0.9344** |
| **Mean Absolute Error (MAE)**      | **0.1912** |
| **Root Mean Squared Error (RMSE)** | **0.3001** |

### Interpretation

* Explains approximately **93.4%** of the variance in silica concentrate.
* Low MAE indicates small prediction errors.
* Low RMSE demonstrates strong regression performance.
* Predicted values closely follow actual observations.

---

# 📊 Model Visualizations

The notebook contains multiple visualizations, including:

* Distribution of Silica Concentrate
* Box Plot for Outlier Analysis
* Actual vs Predicted Scatter Plot
* Top 10 Feature Importance
* Outlier Percentage Analysis

These visualizations help understand data distribution, model behavior, and the influence of process variables.

---

# ⭐ Top 10 Important Features

Based on XGBoost Feature Importance:

| Rank | Feature                      |
| ---- | ---------------------------- |
| 1    | % Silica Feed                |
| 2    | % Iron Feed                  |
| 3    | Flotation Column 03 Air Flow |
| 4    | Flotation Column 02 Level    |
| 5    | Flotation Column 02 Air Flow |
| 6    | Flotation Column 01 Level    |
| 7    | Ore Pulp Density             |
| 8    | Ore Pulp pH                  |
| 9    | Flotation Column 03 Level    |
| 10   | Amina Flow                   |

These variables contribute the most to predicting silica concentrate in the flotation process.

---

# 📁 Project Structure

```
Mining-Process-Quality-Prediction-using-Machine-Learning
│
├── mining.ipynb
├── README.md
└── MiningProcess_Flotation_Plant_Database.csv
```

---

# 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/Sanjayduduka45/Mining-Process-Quality-Prediction-using-Machine-Learning.git
```

### 2. Navigate to the project

```bash
cd Mining-Process-Quality-Prediction-using-Machine-Learning
```

### 3. Install dependencies

```bash
pip install numpy pandas matplotlib seaborn scikit-learn xgboost lightgbm catboost
```

### 4. Open the notebook

```bash
jupyter notebook mining.ipynb
```

---

# 📌 Key Highlights

* Complete End-to-End Machine Learning Pipeline
* Real-world Industrial Mining Dataset
* Comprehensive Exploratory Data Analysis
* Outlier Detection using IQR
* Data Cleaning and Preprocessing
* XGBoost Regression Model
* Feature Importance Analysis
* Actual vs Predicted Performance Visualization
* Well-structured and reproducible notebook

---

# 🔮 Future Enhancements

* Hyperparameter Optimization using RandomizedSearchCV
* Cross-Validation for improved generalization
* SHAP Explainability for model interpretation
* Model Serialization using Pickle/Joblib
* Streamlit Web Application
* FastAPI Deployment
* Docker Containerization
* MLOps Pipeline with CI/CD

---

# 👨‍💻 Author

**Sanjay Duduka**

**B.Tech – Computer Science & Engineering**

Machine Learning • Data Science • Python

**GitHub Repository:**
[Mining Process Quality Prediction Repository](https://github.com/Sanjayduduka45/Mining-Process-Quality-Prediction-using-Machine-Learning?utm_source=chatgpt.com)

**Project Notebook:**
[View mining.ipynb](https://github.com/Sanjayduduka45/Mining-Process-Quality-Prediction-using-Machine-Learning/blob/main/mining.ipynb?utm_source=chatgpt.com)

---

## ⭐ If you found this project useful, consider giving the repository a **Star** on GitHub!
