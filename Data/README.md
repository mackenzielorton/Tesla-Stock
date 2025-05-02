# Data Directory

This folder contains all the datasets used in our analysis, organized into **raw** and **processed** subfolders.

---

## 📂 raw

The **raw** folder holds the original, unmodified source files:

- **`tesla_stock_data_2000_2025.csv`**  
  Daily Tesla price and volume data (Open, High, Low, Close, Volume) downloaded from Kaggle.  
- **`monthly_inflation.csv`**  
  Monthly U.S. inflation rates (percent change) scraped from the BEA website.

> **Note:** These files are the unaltered inputs to our pipeline. Do not edit them directly—any cleaning or transformation happens in the processing step below.

---

## 📂 processed

The **processed** folder contains cleaned, merged, and feature-engineered datasets ready for analysis:

- **`tesla_rev_eps.csv`**  
  - **Date** (YYYY-MM-DD)  
  - **Close / High / Low / Open** (USD)  
  - **Volume** (shares)  
  - **Value** (quarterly inflation %)  
  - **Quarter** (1–4) derived from Date  
  - **Return** (daily % change in Close)  
  - **EPS** (quarterly earnings per share, USD)  
  - **Revenue** (quarterly revenue, millions USD)
