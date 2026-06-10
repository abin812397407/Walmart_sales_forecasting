# Walmart Sales Forecasting Using Machine Learning

A machine learning project that forecasts Walmart weekly sales using historical retail data, time-series feature engineering, and ensemble learning techniques. The project compares Random Forest and XGBoost models, with XGBoost achieving the best forecasting performance.

---

##  Project Overview

Accurate sales forecasting is critical for inventory management, workforce planning, budgeting, and strategic decision-making in the retail industry.

This project develops a forecasting system that predicts Walmart's weekly sales using:

- Historical sales data
- Economic indicators
- Time-series features
- Ensemble machine learning algorithms

The project follows a complete end-to-end machine learning workflow from data preprocessing to model evaluation and forecasting.

---

##  Objectives

- Forecast Walmart weekly sales accurately.
- Analyze the impact of economic and seasonal factors on sales.
- Compare machine learning algorithms for forecasting performance.
- Generate actionable business insights from historical sales data.

---

##  Dataset

The dataset contains Walmart weekly sales data along with several external factors affecting demand.

### Features

| Feature | Description |
|----------|-------------|
| Store | Store identification number |
| Date | Weekly sales date |
| Weekly_Sales | Weekly sales revenue |
| Holiday_Flag | Indicates holiday week |
| Temperature | Average temperature |
| Fuel_Price | Fuel price index |
| CPI | Consumer Price Index |
| Unemployment | Unemployment rate |

---

##  Feature Engineering

To improve forecasting performance, several time-series features were created.

### Lag Features

- `lag_1` → Sales from previous week
- `lag_4` → Sales from 4 weeks ago
- `lag_12` → Sales from 12 weeks ago

### Rolling Statistics

- `rolling_mean_4` → Average sales of the previous 4 weeks

### Date Features

- Month
- Year
- Week of Year

These features help the model capture seasonality, trends, and temporal dependencies.

---

##  Machine Learning Models

### Random Forest Regressor

- Ensemble learning algorithm
- Handles nonlinear relationships
- Robust to noise and outliers
- Strong baseline forecasting model

### XGBoost Regressor

- Gradient boosting framework
- Learns from previous prediction errors
- Handles complex feature interactions
- Provides superior forecasting accuracy

---

 📊 Model Performance

### Random Forest

| Metric | Score |
|----------|----------|
| MAE | 85,218.70 |
| RMSE | 161,563.27 |
| R² Score | 0.9085 |

### XGBoost

| Metric | Score |
|----------|----------|
| MAE | 73,834.34 |
| RMSE | 102,769.69 |
| R² Score | 0.9630 |

### 🏆 Best Model

**XGBoost** achieved the highest predictive performance with:

- Lowest MAE
- Lowest RMSE
- Highest R² Score

Therefore, XGBoost was selected as the final forecasting model.

---

## 📈 Example Forecast

### Random Forest

```text
Predicted Sales: 768,606.65
Actual Sales:    760,281.43
```

### XGBoost

```text
Predicted Sales: 699,217.31
Actual Sales:    760,281.43
```

Although Random Forest was closer for this individual prediction, XGBoost delivered better overall performance across the complete test dataset.

---

##  Visualizations

The project includes:

- Actual vs Predicted Sales
- Random Forest Forecast Plot
- XGBoost Forecast Plot
- Model Comparison Visualization
- Feature Importance Analysis
- Residual Analysis
- Error Distribution Histogram

---

##  Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- XGBoost
- Jupyter Notebook

---

##  Project Workflow

1. Data Loading
2. Data Cleaning
3. Feature Engineering
4. Lag Feature Creation
5. Train-Test Split
6. Random Forest Training
7. XGBoost Training
8. Model Evaluation
9. Model Comparison
10. Visualization
11. Sales Forecasting

---

##  Future Improvements

- Hyperparameter Tuning
- LSTM-based Deep Learning Forecasting
- Real-Time Sales Prediction Dashboard
- Model Deployment using Flask or FastAPI
- Automated Forecasting Pipeline

---

## 👨‍💻 Author

**Abin Mathew**

Computer Science Student | Machine Learning & Data Analytics Enthusiast

Interested in Machine Learning, Data Science, Predictive Analytics, and Artificial Intelligence.

---

## 📄 License

This project is intended for educational, research, and portfolio purposes.
