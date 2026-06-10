# Walmart Sales Forecasting (Machine Learning)

## Project Overview

This project builds a **machine learning model to forecast Walmart weekly sales** using historical retail data.
The model uses **Random Forest Regression with time-series feature engineering** to capture temporal patterns, store-level differences, and economic indicators affecting sales.

The project demonstrates a **complete end-to-end ML workflow**, including:

* Data preprocessing
* Feature engineering
* Time-series forecasting
* Model training
* Performance evaluation
* Model interpretation
* Example prediction using the latest available data

---

## Dataset

The dataset contains Walmart weekly sales data along with additional features that influence demand.

Main columns include:

* Store
* Date
* Weekly_Sales
* Holiday_Flag
* Temperature
* Fuel_Price
* CPI
* Unemployment

These variables allow the model to learn **seasonal trends, economic influence, and store-level sales patterns**.

---

## Feature Engineering

To improve forecasting performance, several **time-series features** were created.

### Lag Features

* `lag_1` – sales from previous week
* `lag_4` – sales from 4 weeks ago
* `lag_12` – sales from 12 weeks ago

### Rolling Statistics

* `rolling_mean_4` – average sales of previous 4 weeks

### Date Features

* `month`
* `year`
* `week_of_year`

These features help the model learn **temporal dependencies in retail demand**.

---

## Machine Learning Model

The forecasting model used in this project is:

**Random Forest Regressor**

Reasons for choosing Random Forest:

* Handles nonlinear relationships well
* Robust to noisy data
* Works effectively for tabular datasets
* Captures complex interactions between features

Model configuration:

* `n_estimators = 400`
* `max_depth = None`
* `min_samples_leaf = 2`

---

## Model Evaluation

Model performance is evaluated using:

* **MAE (Mean Absolute Error)**
* **RMSE (Root Mean Squared Error)**
* **R² Score**

Additional diagnostics include:

* Actual vs Predicted scatter plot
* Residual analysis
* Error distribution
* Feature importance visualization

---

## Key Insights

Key observations from the trained model:

* Store identity is a strong predictor of sales.
* Economic indicators such as **CPI and unemployment** influence retail demand.
* Time-series lag features capture weekly sales patterns.
* Random Forest effectively models nonlinear retail behavior.

---

## Example Forecast

The project includes a final step demonstrating **how to use the trained model to predict future sales** using the latest available features.

Example output:

Predicted Sales: ~768,000
Actual Sales: ~760,000

This shows the model can produce **reasonable short-term forecasts**.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* Joblib

---

## Project Workflow

1. Data loading and inspection
2. Data cleaning and preprocessing
3. Feature engineering
4. Lag feature creation
5. Time-based train/test split
6. Random Forest model training
7. Model evaluation
8. Visualization and diagnostics
9. Feature importance analysis
10. Forecasting using latest data

---

## How to Run the Project

### Clone the repository

```bash
git clone https://github.com/abin812397407/Walmart_sales_forecasting.git
cd Walmart_sales_forecasting
```

### Install dependencies

```bash
pip install -r requirements.txt
```

### Run the script

```bash
python walmart_sales_forecasting.py
```

---

## Project Structure

```
walmart-sales-forecasting/
│
├── walmart_sales_forecasting.py
├── Walmart.csv
├── README.md
├── requirements.txt
└── .gitignore
```

---

## Future Improvements

Possible improvements to this project include:

* Using advanced models such as **XGBoost or LightGBM**
* Training **store-specific forecasting models**
* Adding promotional or event-based features
* Building an interactive dashboard for forecasting

---

## Author

Abin
Machine Learning & Data Science Enthusiast
