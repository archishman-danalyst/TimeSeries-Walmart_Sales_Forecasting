# TimeSeries-Walmart_Sales_Forecasting
# 🛒 Walmart Sales Forecasting (Time Series Project)

## 📌 Overview

This project focuses on analyzing Walmart's historical sales data and building a time series forecasting model to predict future weekly sales for multiple stores. The primary goal is to help optimize inventory management by aligning supply with demand.

---

## 🎯 Problem Statement

Retail stores across multiple locations are facing challenges in managing inventory efficiently. The objective is to:

* Analyze historical weekly sales data
* Identify key factors affecting sales
* Detect patterns such as seasonality and trends
* Build predictive models to forecast sales for the next 12 weeks

---

## 📊 Dataset Description

The dataset contains **6435 rows and 8 columns**:

| Feature      | Description                              |
| ------------ | ---------------------------------------- |
| Store        | Store number                             |
| Date         | Week of sales                            |
| Weekly_Sales | Sales for the given store in that week   |
| Holiday_Flag | Indicates holiday week (1 = Yes, 0 = No) |
| Temperature  | Temperature on the day                   |
| Fuel_Price   | Regional fuel price                      |
| CPI          | Consumer Price Index                     |
| Unemployment | Unemployment rate                        |

---

## 🔍 Exploratory Data Analysis (EDA)

### Key Steps:

* Converted `Date` column to datetime format
* Checked for missing values and handled appropriately
* Identified and treated outliers using statistical methods
* Performed correlation analysis

### Key Insights:

* Sales vary significantly across stores
* Holiday weeks show noticeable spikes in sales
* Some stores show consistent growth trends while others fluctuate

---

## 📈 Business Insights

### 1. Impact of Unemployment on Sales

* Negative correlation observed between unemployment rate and sales
* Certain stores are more sensitive to economic conditions

### 2. Seasonality Trends

* Strong seasonal patterns observed
* Sales peak during holiday seasons (e.g., Thanksgiving, Christmas)

### 3. Temperature Effect

* Mild influence on sales
* Extreme weather conditions show slight impact

### 4. CPI Influence

* CPI shows moderate correlation with sales
* Inflation impacts purchasing power and hence sales

### 5. Top Performing Stores

* Identified based on highest average weekly sales
* Consistent performance across multiple weeks

### 6. Worst Performing Stores

* Stores with lowest average sales identified
* Significant gap between best and worst performers

---

## 🧠 Modeling Approach

### Models Used:

* ARIMA (AutoRegressive Integrated Moving Average)
* SARIMA (Seasonal ARIMA)
* Prophet (optional improvement)

### Steps:

1. Stationarity check using ADF test
2. Differencing to remove trends
3. Model parameter tuning (p, d, q)
4. Model training and validation
5. Performance evaluation using RMSE and MAE

---

## 🔮 Forecasting Results

* Generated forecasts for the next **12 weeks** for each store
* SARIMA performed best due to seasonality handling
* Forecasts show realistic seasonal fluctuations

---

## 📉 Model Evaluation Metrics

| Metric | Description             |
| ------ | ----------------------- |
| MAE    | Mean Absolute Error     |
| RMSE   | Root Mean Squared Error |

Lower values indicate better model performance.

---

## 🛠️ Tech Stack

* Python
* Pandas, NumPy
* Matplotlib, Seaborn
* Statsmodels
* Google Colab

---

## 🚀 Future Improvements

* Incorporate external factors like promotions and events
* Use advanced models like LSTM (Deep Learning)
* Build a real-time dashboard for monitoring

---

## 📁 Project Structure

```
├── data/
│   └── walmart.csv
├── notebooks/
│   └── analysis.ipynb
├── models/
├── outputs/
│   └── forecasts.csv
├── README.md
```

---

## ✅ Conclusion

This project demonstrates how time series analysis can be effectively used to forecast retail sales and improve inventory planning. By understanding patterns and key influencing factors, businesses can make data-driven decisions and reduce operational inefficiencies.
