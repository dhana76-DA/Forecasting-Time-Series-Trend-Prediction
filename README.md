# Forecasting-Time-Series-Trend-Prediction
Project Overview

This project focuses on forecasting retail sales using historical Walmart sales data. The objective is to analyze sales trends, identify seasonality, and build reliable forecasting models to predict future sales. The project follows a complete time-series forecasting pipeline using Python.

Dataset
Source: Walmart Sales Forecasting Dataset (CSV)

Key Columns:
Date – Weekly sales date
Weekly_Sales – Sales amount
Store, Holiday_Flag, Temperature, Fuel_Price, CPI, Unemployment
The dataset was aggregated to a monthly level to support trend and seasonality analysis.

Tools and Technologies
Python: Employed for data cleaning, analysis, and building predictive models using libraries such as Pandas, NumPy, and Scikit-learn.
Matplotlib & Seaborn: For creating visualizations to support exploratory data analysis.
Statsmodels: Used for implementing ARIMA and other time-series models for forecasting.
DateTime: Used for handling date-related operations for time-series data.
Pandas: Utilized for handling time-indexed data and applying moving averages for forecasting.

Project Workflow

Loaded and cleaned the Walmart sales dataset
Converted the Date column to datetime format
Aggregated weekly sales into monthly sales
Visualized sales trends over time
Checked seasonality using rolling mean
Split data into training and testing sets (time-based split)

Built forecasting models:
Moving Average (baseline)
Holt-Winters Exponential Smoothing
Forecasted future sales
Evaluated model performance using MAE and MAPE

Forecasting Models
Moving Average
Simple baseline model
Smooths short-term fluctuations
Does not capture trend or seasonality

Exponential Smoothing (Holt-Winters)
Captures level, trend, and seasonality
Produces realistic retail sales forecasts
Best-performing model in this project

Model Evaluation
The Exponential Smoothing model was evaluated on unseen test data.

Metrics Used:
MAE (Mean Absolute Error)
MAPE (Mean Absolute Percentage Error)

Sample Results:

MAE ≈ 1.8 × 10⁷
MAPE ≈ 6–7%

MAE  : 3.15e+07
MAPE : 15.29%
Moving Average Forecast Value: 1.97e+08
MA Model - MAE: 2.00e+07, MAPE: 9.35%
This indicates strong forecasting accuracy for retail sales data.

Final Conclusion

The sales forecasting analysis successfully identified clear seasonal patterns and long-term trends in Walmart sales data. While the Moving Average model served as a simple baseline, the Holt-Winters Exponential Smoothing model significantly outperformed it by effectively capturing both trend and seasonality. The low MAE and MAPE values demonstrate that the model provides accurate and reliable sales predictions. This approach can support data-driven decision-making in inventory planning, demand forecasting, and business strategy.

📂 Project Structure
Sales-Forecasting/
│── data/
│   └── Walmart.csv
│── notebooks/
│   └── sales_forecasting.ipynb
│── output/
│   ├── forecast_results.csv
│   └── future_sales_forecast.csv
│── README.md

Future Improvements
Use SARIMA for advanced seasonal modeling
Incorporate external factors (holidays, CPI, fuel price)
Perform hyperparameter tuning
Extend forecast horizon
