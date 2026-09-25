# sales-procurement-forecasting-ml
Sales and procurement Forecasting using machine learning and python,developed during my tata motors internship
# 📊 Sales & Procurement Forecasting using Machine Learning

A machine learning-based sales and procurement forecasting project developed during my internship at Tata Motors.

## 📌 Project Overview

Forecasting helps organizations predict future demand using historical data. Accurate forecasting can support procurement planning, reduce the risk of overstocking or understocking, and improve cost management.

This project analyzes procurement data from **2022–2024** and uses it to forecast demand for **2025**.

Two forecasting approaches were evaluated:

- Prophet – Time Series Forecasting
- XGBoost – Machine Learning Regression

## 🎯 Business Problem

Monthly material purchase amounts fluctuate, making future procurement requirements difficult to estimate.

The project focuses on:

- Fluctuating monthly demand
- Overstocking and understocking risks
- Procurement cost implications
- Challenges associated with manual monthly tracking

## 📊 Dataset

The project uses historical procurement data.

| Category | Details |
|---|---|
| Training Data | 2022–2024 |
| Testing Data | 2025 |
| Main Fields | Amount Value, Month, Amount in LC |
| Preprocessing | Data cleaning and missing-value handling |

> The original company dataset is not included in this repository due to data confidentiality.

## 🤖 Forecasting Models

### 1. Prophet

Prophet was used as a time-series forecasting model with yearly seasonality.

The model was trained using historical data from 2022–2024 and evaluated against 2025 data.

### 2. XGBoost

XGBoost was used as a machine-learning regression model.

Time-based and lag features were created, including:

- Year
- Month number
- Lag 1
- Lag 2
- Lag 3
- Lag 6
- Rolling mean features

The model was trained on historical data and tested using 2025 observations.

## 📏 Model Evaluation

The models were evaluated using:

- MAE – Mean Absolute Error
- RMSE – Root Mean Squared Error
- MAPE – Mean Absolute Percentage Error

### Results

| Model | MAE | RMSE | MAPE |
|---|---:|---:|---:|
| Prophet | ≈ 61 | ≈ 73 | ≈ 54% |
| XGBoost | ≈ 16 | ≈ 24 | ≈ 18% |

Based on the reported evaluation results, XGBoost produced lower error values than Prophet on the 2025 test data.

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Prophet
- XGBoost
- Scikit-learn
- Excel

## 🔄 Project Workflow

```text
Historical Procurement Data
          ↓
     Data Cleaning
          ↓
   Data Preprocessing
          ↓
   ┌───────────────┐
   ↓               ↓
 Prophet         XGBoost
   ↓               ↓
 Forecast        Forecast
   ↓               ↓
   └───────┬───────┘
           ↓
    Model Evaluation
           ↓
      Compare Results
           ↓
    Forecasting Insights
