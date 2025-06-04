---

# 📊 Clean Merge of Economic Indicators for Better GDP Insights Using ML & DL Techniques

This project focuses on merging and modeling economic indicators from multiple global datasets to enhance GDP forecasting. Using both Random Forest and ARIMA models, it analyzes data for the top 20 global economies, exploring both linear and nonlinear dependencies among key economic factors.

---

## 📝 Abstract

Global economic instability, inflation, and fluctuating indicators like unemployment, energy use, and exports make GDP forecasting complex but crucial. This project builds machine learning and deep learning pipelines that clean, merge, and analyze large economic datasets to make more reliable GDP predictions. These predictions can support decision-making for governments, investors, and policy makers.

---

## 🛠️ Tech Stack

Language: Python

Libraries: Pandas, NumPy, Matplotlib, Plotly, Scikit-learn 

Machine Learning Model: RandomForestRegressor

Deep Learning Model: Statsmodels (ARIMA)

---

## 📂 Dataset Information

Source: World Bank Open Data: https://data.worldbank.org/

Indicators Used:
-  GDP (Current US$)
-  CPI (Consumer Price Index)
-  Energy Use (kg of oil equivalent per capita)
-  Exports (% of GDP)
-  Government Spending
-  Oil Rents
-  Unemployment (% of labor force)

Scope: Top 20 Powerful Economies (Country-Year level data)

---

## 🔁 Data Processing Pipeline

Cleaning:
-  Missing numerical values filled with zero
-  Placeholder values for missing text (e.g., "null")
-  Column name standardization
-  Year alignment across dataset

Merging:
-  Based on shared keys: Country, Year
-  Final dataset is a wide table with all indicators per country-year pair

EDA (Exploratory Data Analysis):
-  GDP Trends (Line Charts)
-  Correlation Heatmaps
-  Distribution Histograms
-  GDP vs. Export Scatter Plots

---

## 🤖 ML Model: Random Forest Regressor

Training:
-  Trained to predict GDP using all economic indicators as inputs

Hyperparameters:
-  n_estimators, max_depth (tuned for performance)

Evaluation:
-  MAE, MSE, RMSE for all countries
-  Feature importance plots

Results:
-  Best results for France, Netherlands, Japan
-  Struggles with scale for China, USA (high errors)

---

## 📉 DL Model: ARIMA

Scope: Time-series only

Used For:
-  CPI Forecasting
-  Energy Use & Oil Rents

Training:
-  Fitted using historical trends with ARIMA from statsmodels

Evaluation:
-  MAE, MSE, RMSE
-  Lower performance than RF on complex indicators

---

## ✅ Forecast Outputs (2023–2028)

Random Forest Predictions:
GDP: ✅
CPI: ✅
Unemployment: ✅
Exports: ✅
Energy Use: ❌
Oil Rents: ❌

ARIMA Predictions:
Energy Use: ✅
Oil Rents: ✅

---

## 📊 Model Comparison

In this project, both Random Forest and ARIMA models were employed to predict GDP and related economic indicators. Random Forest demonstrated superior performance in capturing complex, non-linear relationships among multiple variables, making it well-suited for multi-variate economic forecasting. It consistently produced lower error metrics such as MAE, MSE, and RMSE across most countries, especially in stable economies like France and Japan.

On the other hand, ARIMA excelled in forecasting single-variable time-series data such as CPI and energy usage, particularly when trends were smooth and historical patterns were consistent. However, ARIMA struggled with dynamic and volatile economies due to its limited capacity to handle multiple predictors or abrupt non-linear shifts in data. Compared to Random Forest, ARIMA's accuracy was lower and its error metrics were higher, particularly for countries with irregular economic trends like India and Brazil.

Overall, Random Forest was more effective for comprehensive GDP prediction using multiple indicators, whereas ARIMA served better in simpler, trend-focused tasks. The choice of model should be aligned with the data structure and forecasting complexity.

---

## 🔮 Future Scope

-  Integrate additional socio-economic factors (like inflation rate, interest rates)
-  Real-time economic dashboards
-  Deploy as a forecasting web application
-  Country-wise risk indicator engine

--- 
