# 🕵️‍♀️ Chicago Domestic Crime Analysis (2018–2022)

This project explores patterns of **domestic violence crimes** in the city of Chicago from 2018 to 2022 using publicly available crime data. The main objective is to understand the evolution of domestic crimes, identify key temporal and spatial trends, and predict crime levels for 2023 using statistical modeling.

---

## 👥 Authors
Project by:

* Miguel Balderrama

* Joaquín Miguel

* María Victoria D’Ercole

Universidad Nacional de San Martín (UNSAM) | Introduction to Data Science — June 2023 


---

## 🎯 Objective

To evaluate the dynamics of domestic violence crimes in Chicago, analyzing trends, seasonality, and location-based insights, and to develop a predictive model for estimating domestic crime levels in 2023. The project aims to support awareness, policymaking, and community safety efforts.

---

## 📂 Project Structure

- `PRESENTACION_ICD_-_Balderrama__Miguel__DErcole_2.pdf`: Full project presentation (in Spanish).
- Notebook: Data processing and modeling code (to be included).
- Data source: [Chicago Crimes Dataset (Kaggle)](https://www.kaggle.com/datasets/utkarshx27/crimes-2001-to-present)

---

## 🧰 Tools & Technologies

- **R Programming**: Data cleaning, manipulation, and modeling
- **ggplot2 / Base R Plots**: Visualizations
- **Polynomial Regression**: Forecast modeling
- **Public data APIs**: Climate data and demographic background

---

## 🗂 Dataset Summary

**Source**: [City of Chicago Data Portal](https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-Present/ijzp-q8t2)

- **Rows analyzed**: 1,188,896 (filtered from original dataset)
- **Time range**: 2018 to 2022
- **Focus**: Only domestic-related crimes (`Domestic = TRUE`)

### Key Variables Used:
- `Date`
- `Primary.Type`
- `Location.Description`
- `Arrest`
- `Community.Area`
- `Year`

### Engineered Variables:
- `month`, `week`, `day_of_week`, `hour` (from parsed `Date` column)

---

## 🔍 Analysis Overview

### 🔸 General Trends
- Domestic crimes remained relatively stable from 2018 to 2022.
- Annually: ~40,000 to ~45,000 cases.
- **Assault** is the most frequent domestic-related crime.

### 🔸 Arrests
- A **downward trend** in arrest rates for domestic incidents over time.

### 🔸 Temporal Insights
- Higher crime frequency on **weekends**.
- **Midnight** is the peak hour for incidents.
- Seasonal increase during **summer months**, decrease in **winter**.

### 🔸 Spatial Analysis
- Common locations: **Street**, **residence**, **apartment**, **sidewalk**, and **storefront**.
- Certain **community areas** show disproportionately high incident rates.

---

## 📈 Predictive Modeling (2023)

## Best Model:
cant_crimen ~ poly(month_year, 2) * season + Arrest
R-squared: 0.97
P-value: 2.2e-06
Residual Standard Error: 0.2

## Forecast:
* Projected domestic crime cases for 2023: ~45,036
* Predicted +6% increase from 2022
* ±20% margin of error

## 📚 Key Findings
* Domestic crime levels are stable but high.
* Seasonal behavior is evident: peaks in summer, lows in winter.
* Assault dominates domestic crime types.
* Crime is most frequent at midnight and weekends.
* Spatial patterns reveal hotspots in specific neighborhoods.

## 🔭 Future Work
* Evaluate other model types (e.g., ARIMA, Random Forest, XGBoost).
* Explore socioeconomic correlations (e.g., income, education level).
* Add weather and external variables to improve forecasts.
* Develop a web-based dashboard or Shiny app for visualization.



---
## References
📊 Chicago Crime Data (City Portal)

🌡️ WeatherSpark: Chicago Climate Averages

🏥 Chicago Health Atlas

📰 BBC News – Crime in Chicago

