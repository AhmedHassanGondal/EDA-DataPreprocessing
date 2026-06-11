# ⚡ Electricity Demand & Weather — EDA and Data Preprocessing

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=python&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=power-bi&logoColor=black)

A robust **data preprocessing and exploratory data analysis** pipeline that
merges raw **electricity demand** and **weather** data, cleans and engineers it,
explores the relationships between weather and demand, and trains a baseline
demand model. Built with a `rich` console UI for readable, step-by-step output.

## 🔧 Pipeline

1. **Load & merge** — reads many raw electricity-demand and weather JSON files
   (with encoding fallbacks and empty-file handling) and merges them on
   timestamp.
2. **Clean** — handles missing values, types, and outliers to produce a tidy
   analysis table.
3. **Explore (EDA)** — distributions, time trends, and a **correlation matrix**
   between weather variables and demand.
4. **Model (baseline)** — a `LinearRegression` demand model with an
   RMSE / R² evaluation.
5. **Report** — exports processed data, summary statistics, and a Power BI
   dashboard.

## 📦 What's included

```
eda-data-preprocessing/
├── robust_data_preprocessing.py            # The end-to-end pipeline
├── electricity_demand_analysis.ipynb       # Notebook walkthrough of the EDA
├── processed_electricity_weather_data.csv  # Cleaned, merged output
├── correlation_matrix.csv                  # Weather ↔ demand correlations
├── summary_statistics.csv                  # Descriptive statistics
└── Power_Bi Charts.pbix                     # Power BI dashboard
```

> **Note on data:** the processed outputs above are included so you can inspect
> the results directly. The raw `electricity_raw_data/` and `weather_raw_data/`
> JSON folders are external inputs — update the `base_path` at the top of
> `robust_data_preprocessing.py` to point at your local copy before re-running
> the full pipeline from scratch.

## 🚀 Run it

```bash
pip install pandas numpy matplotlib seaborn scikit-learn rich

python robust_data_preprocessing.py
# or open electricity_demand_analysis.ipynb in Jupyter
```

## 🧰 Tech stack

Python · pandas · NumPy · scikit-learn · Matplotlib · Seaborn · rich · Power BI
