# Forecasting Average Length of Stay (ALOS) in U.S. Hospitals Using Seasonal Indexing and Linear Regression.
---
## Overview:
The primary aim of this project is to analyze the Average Length of Stay (ALOS) in hospitals and forecast future trends. By leveraging the historical data of inpatient days and hospital discharges, this project seeks to understand trends in ALOS data to investigate the effect of seasonal diseases like flu, respiratory illness, etc; and finally to forecast the future ALOS values. This analysis will help in making informed decisions regarding capacity planning, resource allocation, and operational efficiency in healthcare settings.

Extrcated two datasets from Federal Reserve Economic Data ([FRED](https://fred.stlouisfed.org/)) website:

- __Total Inpatient Days for Hospitals__ (2005–2022)
- __Total Discharges for Hospitals__ (2005–2022)

The ALOS is derived from these datasets by calculating the ratio of inpatient days to discharges for each time period. 

ALOS = Total Inpatient Days/Total Discharges

In this project, we have utilized two dataset, which contains historical Total Inpatient Days and Total Discharges data obtained from Quarterly Services Survey of US hospitals over theyears. The dataset includes metrics such as:

- __date:-__	Starting dates of the quarter
- __Value:-__	Total Inpatient Days (Total Inpatient Days for Hospitals) / Total Discharges (Total Discharges for Hospitals)

## Methods
The project employs time series analysis techniques, including:

- __Seasonal Indexing:__ To identify seasonal patterns in ALOS data.
- __Linear Regression:__ To forecast ALOS for the next four quarters (2023).

## Tools
- __Programming Language:__ Python
- __Libraries:__ NumPy, Pandas, Matplotlib, Statsmodels, Scikit-learn
- __Environment:__ Jupyter Notebook

The project will deliver a robust and scalable forecasting model capable of predicting average ALOS for the next four quarters. This model will uncover seasonal trends in ALOS in US hospitals, particularly during peak periods (e.g., Q1 and Q4) driven by seasonal diseases like influenza, RSV, common cold, etc. The forecasted result will further help in capacity planning, resource allocation, and revenue management, helping hospitals improve operational efficiency and patient care delivery.
