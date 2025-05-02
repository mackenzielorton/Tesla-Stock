# Tesla-Stock
BAIS3250 Data Wrangling Final Project

**Description**  
This repo contains all the scaffolding for our final data‐wrangling project on Tesla stock and macro indicators. It illustrates folder structure, a sample data dictionary, and pointers to key notebooks and datasets.

## Table of Contents  
1. [Folder Structure](#folder-structure)  
2. [Data Sources](#data-sources)  
3. [How to Run](#how-to-run)  
4. [Notebooks](#notebooks)  
5. [Data Dictionary](#data-dictionary)  
6. [Links](#links)

### Folder Structure  
| Folder              | Description                                                        |
|---------------------|--------------------------------------------------------------------|
| `Data/Raw/`         | Original downloaded data files (unchanged)                         |
| `Data/Processed/`   | Cleaned and merged data ready for analysis                         |
| `Notebooks/`        | Jupyter notebooks for EDA, modeling, and reporting                 |


### Data Sources  
- **Tesla daily prices:** Kaggle (tesla_stock.csv)  
- **Inflation (Value):** BEA API  
- **EPS & Revenue:** Macrotrends  

### How to Run  
1. `pip install -r requirements.txt`  
2. Place CSVs in `data/raw/`  
3. In `notebooks/01_data_wrangling.ipynb`, run cells to clean, merge, and save to `data/processed/merged_data.csv`.

### Notebooks  
| Notebook                       | Description                                   |
|--------------------------------|-----------------------------------------------|
| `01_data_wrangling.ipynb`      | Ingest, clean, merge raw data into final DF   |
| `02_EDA_and_Visualizations.ipynb` | Univariate & bivariate analyses                |

### Links  
- Raw dataset download: [Kaggle Tesla Stock](https://www.kaggle.com/…/tesla-stock-data)  
- BEA inflation API: https://apps.bea.gov/…  

### Data Dictionary  
Please see [data_dictionary.md](data_dictionary.md) for column definitions.
