# Notebook: `TeslaStock.ipynb`

## Overview  
`TeslaStock.ipynb` walks through the full data-wrangling and analysis pipeline for our Tesla project. Starting from raw price, inflation, EPS and revenue data, it produces a cleaned master DataFrame, explores key relationships, builds predictive models, and forecasts fundamentals.

---

## Contents

1. **Setup & Imports**  
   - Load libraries: pandas, NumPy, seaborn, matplotlib, statsmodels, scikit-learn, etc.  
   - Define helper utilities (e.g. quarter mapping).

2. **Data Ingestion**  
   - Read daily OHLCV (`raw/tesla_stock_data_2000_2025.csv`).  
   - Read monthly inflation (`raw/monthly_inflation.csv`).  
   - Read quarterly EPS & revenue (`raw/tesla_rev_eps.csv`).

3. **Cleaning & Parsing**  
   - Remove extraneous header rows.  
   - Convert `Date` columns to datetime.  
   - Cast numeric columns (`Close`, `High`, `Low`, `Open`, `Volume`) to floats/ints.

4. **Feature Engineering & Merge**  
   - Compute daily return (`Return = pct_change()` of Close).  
   - Extract `Year`, `Month`, map to `Quarter`.  
   - Join quarterly inflation, EPS, and revenue by year+quarter onto the daily data.

5. **Exploratory Data Analysis**  
   - **Descriptive statistics** (mean, median, standard deviation).  
   - **Univariate plots**: histograms and boxplots.  
   - **Bivariate plots**: scatter-with-regression for Price vs. EPS, Return vs. Inflation; correlation heatmap.  
   - **Hypothesis tests**: t-tests around policy events, ANOVA across quarters.

6. **Machine Learning**  
   - **Regression**: OLS, Ridge, Lasso to predict quarterly price/returns (report R²).  
   - **Classification**: Logistic Regression, Decision Tree, KNN, SVM to predict up/down moves (report accuracy & F₁).

7. **Time-Series Forecasting**  
   - Fit **ARIMA(1,1,1)** to quarterly EPS and Revenue.  
   - Plot historical series and 8-quarter forecasts.

8. **Conclusions & Next Steps**  
   - Summarize insights on volatility drivers and predictive power of fundamentals.  
   - Recommend further modeling or feature enhancements.

---
