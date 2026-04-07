# Rossmann Store Sales Prediction: Time Series Forecasting

## 📌 Project Overview
Rossmann operates over 3,000 drug stores in 7 European countries. This project focuses on predicting the daily sales for 1,115 stores up to six weeks in advance. Accurate forecasting allows store managers to optimize inventory, manage staff schedules, and increase overall operational efficiency.

## 📊 Business Problem
Currently, Rossmann store managers predict sales based on their unique circumstances, leading to varied accuracy. The goal of this project is to build a robust Machine Learning model that automates this process using historical data, considering factors like:
* Promotions and Seasonality
* Competition distance and opening dates
* State and School holidays
* Store types and assortment levels

## 🛠️ Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-learn, XGBoost, Matplotlib, Seaborn
* **Environment:** Jupyter Notebook / Google Colab

## 🧪 Data Description
The dataset contains historical sales data for 1,115 Rossmann stores. Key features include:
* **Store:** Unique ID for each store.
* **Sales:** The turnover for any given day (Target Variable).
* **Customers:** Number of customers on a given day.
* **Promo:** Indicates if a store is running a promotion.
* **StateHoliday/SchoolHoliday:** Indicates closures due to holidays.

## 🚀 Key Implementation Steps
1.  **Data Cleaning:** Handled missing values in `CompetitionDistance` and other store-related features.
2.  **Feature Engineering:** * Extracted `Year`, `Month`, `Day`, and `WeekOfYear` from date columns.
    * Encoded categorical variables like `StoreType` and `Assortment`.
    * Mapped holiday types to numerical values.
3.  **Preprocessing:** Filtered out days where stores were closed or had zero sales to avoid biasing the model.
4.  **Modeling:** Implemented an **XGBoost Regressor** with log-transformed target variables to handle skewed sales data and improve RMSPE.

## 📈 Results
The model was evaluated using **Root Mean Square Percentage Error (RMSPE)**, ensuring that the prediction error is minimized relative to the actual sales volume.

## 🏁 Conclusion
This project demonstrates how data-driven forecasting can replace manual estimations. By leveraging gradient boosting techniques, we can provide Rossmann with a scalable solution to predict sales trends with high precision.
