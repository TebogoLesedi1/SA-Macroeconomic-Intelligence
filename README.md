# SA Macroeconomic Intelligence
### Inflation, Monetary Policy & Exchange Rate Analysis

## Overview

SA Macroeconomic Intelligence is a data engineering and economic research project focused on analysing the relationship between inflation, monetary policy and exchange rate movements in South Africa.

The project aims to investigate how changes in the South African Consumer Price Index (CPI), the South African Reserve Bank's (SARB) repo rate and the ZAR/USD exchange rate interact over time.

Using historical macroeconomic data, the project will develop an end-to-end data pipeline, perform exploratory and econometric analysis, build inflation forecasting models and present findings through an interactive Power BI dashboard.

Microsoft Fabric will be used as the primary data platform for data ingestion, transformation, storage and analytical processing.

## Research Objective

To investigate the relationship between South African inflation, interest rates and exchange rate movements, and evaluate whether these economic indicators can improve short-term inflation forecasting.

### Research Questions

1. How has South African headline inflation evolved over time?
2. What relationship exists between rand depreciation and changes in inflation?
3. How have changes in the SARB repo rate coincided with inflation movements?
4. Are there observable lagged relationships between exchange rate movements, interest rates and inflation?
5. Can exchange rate and interest rate variables improve inflation forecasts compared with historical inflation alone?

## Data Sources

The project will use publicly available macroeconomic data from official and recognised sources.

| Dataset | Source | Key Variables |
|---|---|---|
| Consumer Price Index (CPI) | Statistics South Africa | CPI index, headline inflation, monthly inflation |
| Repo Rate | South African Reserve Bank | Historical policy interest rate |
| Exchange Rate | FRED / South African Reserve Bank | ZAR/USD exchange rate |

**Initial analysis period:** January 2000 to the latest complete month available across the selected datasets.

Additional macroeconomic indicators may be incorporated as the project develops.

## Technology Stack

| Area | Technologies |
|---|---|
| Data Platform | Microsoft Fabric |
| Data Ingestion | Fabric Data Factory |
| Data Storage | OneLake, Fabric Lakehouse |
| Data Transformation | Python, SQL, PySpark |
| Data Engineering | ETL/ELT, Medallion Architecture |
| Data Analysis | Python, Pandas, NumPy |
| Econometric Analysis | Statsmodels, SciPy |
| Machine Learning | Scikit-learn, XGBoost |
| Data Visualisation | Power BI |
| Version Control | Git, GitHub |

## Data Architecture

The project will follow a Medallion Architecture.

### Bronze Layer
- Ingest raw CPI, repo rate and exchange rate datasets.
- Preserve source files and original observations.
- Maintain source and ingestion metadata.

### Silver Layer
- Clean and standardise datasets.
- Convert dates into a consistent monthly format.
- Handle missing values and duplicates.
- Validate data types, units and observations.
- Align the different economic indicators.

### Gold Layer
- Develop curated analytical datasets.
- Create monthly macroeconomic fact tables.
- Calculate inflation rates and exchange rate percentage changes where required.
- Generate lagged variables and rolling averages.
- Prepare datasets for econometric analysis and Power BI.

## Analytical Approach

### 1. Exploratory Data Analysis
- Analyse historical CPI and inflation trends.
- Examine repo rate movements.
- Investigate ZAR/USD exchange rate movements.
- Calculate correlation coefficients.
- Examine relationships across different economic periods.

### 2. Econometric Analysis
- Analyse lagged relationships between economic indicators.
- Investigate the relationship between rand depreciation and inflation.
- Examine inflation and repo rate movements.
- Compare economic trends across selected periods.

### 3. Inflation Forecasting

The forecasting component will evaluate whether incorporating additional economic variables improves short-term inflation predictions.

Planned model comparisons:

- Model A: Historical inflation variables.
- Model B: Historical inflation and exchange rate variables.
- Model C: Historical inflation, exchange rate and repo rate variables.

Models will be evaluated using chronological training and testing periods, with performance compared against a baseline forecast.

Evaluation metrics:
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)

### 4. Power BI Dashboard

The dashboard will communicate the findings through four analytical areas:

- **Economic Overview:** Headline inflation, CPI trends and repo rate movements.
- **Exchange Rate Analysis:** Rand movements and their relationship with inflation.
- **Monetary Policy Analysis:** Repo rate changes and inflation trends.
- **Inflation Forecasting:** Forecast results, model comparisons and evaluation metrics.

## Repository Structure

```text
sa-macroeconomic-intelligence/
│
├── data/
│   ├── raw/
│   ├── processed/
│   └── gold/
│
├── notebooks/
│   ├── 01_data_quality.ipynb
│   ├── 02_exploratory_analysis.ipynb
│   ├── 03_econometric_analysis.ipynb
│   └── 04_inflation_forecasting.ipynb
│
├── src/
│   ├── extract.py
│   ├── transform.py
│   └── validate.py
│
├── sql/
│   └── analytical_schema.sql
│
├── fabric/
│   └── README.md
│
├── dashboard/
│
├── reports/
│
├── tests/
│
├── requirements.txt
└── README.md
```

## Project Status

**Status: In Development**

| Component | Status |
|---|---|
| Project definition and research questions | Defined |
| CPI data acquisition | In progress |
| Repo rate data acquisition | Planned |
| Exchange rate data acquisition | Planned |
| Fabric Lakehouse implementation | Planned |
| Data transformation pipeline | Planned |
| Exploratory and econometric analysis | Planned |
| Inflation forecasting | Planned |
| Power BI dashboard | Planned |

## Research Limitations

- Correlation does not establish causation.
- Exchange rate movements and interest rate decisions may influence one another through multiple economic channels.
- Economic shocks and external factors may affect inflation independently of the selected variables.
- Forecasting performance will depend on data quality, model selection and the historical evaluation period.

## Data Attribution

Macroeconomic data will be attributed to the original data providers.

Statistics South Africa retains copyright over its statistical publications. Where its data are used, the source will be acknowledged and any derived analysis will be identified as the result of independent processing.

## Project Purpose

This project combines data engineering, economic analysis and predictive modelling to explore South Africa's macroeconomic environment.

It aims to demonstrate how modern data platforms and analytical techniques can be applied to real-world economic research.


