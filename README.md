# Bike-Sharing-Demand-Forecasting-with-Machine-Learning
Built a machine learning regression model to forecast bike rental demand based on time, weather, and  seasonal variables. Helped optimize inventory and resource planning for bike-sharing companies. 
# 🚲 Bike Sharing Demand Forecasting with Machine Learning

## 📘 Problem Statement

A bike-sharing company aims to forecast daily rental demand using historical data to:

* Optimize the number of bikes made available each day
* Avoid both shortages and surplus inventory
* Improve staff planning and dock utilization

The goal is to build a machine learning regression model using variables related to **time**, **season**, and **weather** to predict how many bikes will be rented on any given day.

## ✅ Solution Summary

We built a **Multiple Linear Regression** model to forecast the daily number of bike rentals (`cnt`) using historical data from 2018 and 2019.

### 📈 Model Performance

* **R² Score**: **0.835** (83.5% of rental variation explained)

## 🔢 Forecasted Demand Examples

Using the trained model, we predicted demand under future weather and time conditions:

| Scenario | Season | Temp (°C) | Weather           | Day Type | Predicted Rentals |
| -------- | ------ | --------- | ----------------- | -------- | ----------------- |
| 1        | Summer | 28        | Clear             | Weekday  | **6245**          |
| 2        | Winter | 22        | Mist\_Cloudy      | Weekday  | **6029**          |
| 3        | Spring | 15        | Light\_Rain\_Snow | Weekend  | **1559**          |

These results help determine how many bikes should be available on different types of days.

## 📊 Key Visualizations & Interpretations

### 1. Residual Plot

* Residuals are centered around 0 and normally distributed → model predictions are unbiased.

### 2. Top Positive Features

* Features like `yr`, `temp`, `season_Summer`, and `mnth_Sep` **increase** demand

### 3. Top Negative Features

* Features like `weathersit_Light_Rain_Snow`, high `hum`, `windspeed`, and `season_Winter` **decrease** demand

## 📊 Operational Impact

| Forecast Use      | Example Impact                        |
| ----------------- | ------------------------------------- |
| Bike Allocation   | Stock 6000+ bikes on high-demand days |
| Staff Scheduling  | Add support on summer weekdays        |
| Maintenance Plans | Use low-demand days for servicing     |

## ⚙️ Workflow Summary

1. Data Cleaning & Feature Engineering
2. One-Hot Encoding for Categorical Features
3. Train-Test Split and Model Training
4. Forecasting and Evaluation
5. Visualizations and Interpretation

## 📁 Files

* `Bike_Sharing_Regression_Model_.ipynb` — Notebook with complete code, outputs, and plots
* `day.csv` — Dataset with 2018–2019 daily rental data




