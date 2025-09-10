# Forecasting Average Length of Stay (ALOS) in U.S. Hospitals.
---
## Overview:
The primary goal of this project is to develop a robust time series forecasting model to predict the ALOS for patients in US hospitals. ALOS is a critical Key Performance Indicator (KPI) in healthcare, calculated as the average number of days a patient remains admitted to a hospital.

By accurately forecasting ALOS, one can:

* Enhance Operational Efficiency: Help hospital administrators anticipate patient flow, optimize bed capacity, manage staffing levels, and improve resource allocation (e.g., medical supplies, room cleaning schedules)

* Improve Financial Planning: ALOS is directly tied to healthcare costs and reimbursement models. Forecasting allows for better budget forecasting and financial risk management

* Support Strategic Decision-Making: Provide data-driven insights into trends and seasonal patterns in patient stays, which can inform long-term strategic plans and policy decisions at institutional and regional levels

* Identify Anomalies: The model can serve as a baseline to detect unexpected shifts in ALOS, potentially flagging issues like new disease outbreaks, changes in treatment protocols, or administrative bottlenecks

This analysis leverages two pivotal datasets extracted from the ([FRED](https://fred.stlouisfed.org/)) website using the FRED API:

Dataset 1: ([Total Discharges for Hospitals](https://fred.stlouisfed.org/series/DISC622ALLEST176QNSA))

* Description: This time series data records the total number of patients discharged from US hospitals. A discharge occurs whenever a patient is released, transferred to another facility, or passes away.

* Significance: This metric represents the total volume of patient turnover and is a direct measure of hospital throughput.

Dataset 2: ([Total Inpatient Days for Hospitals](https://fred.stlouisfed.org/series/INPAT622ALLEST176QNSA))

* Description: This time series data records the sum of all days spent by all patients in the hospital during a given period. For example, if 5 patients each stay 4 days, the total inpatient days for that period would be 20.

* Significance: This metric captures the total utilization or "bed-day" consumption of hospital resources.

$ALOS = \frac{\text{total_inpatient_days}}{\text{total_discharge}}$

The formula for ALOS is $ALOS = \frac{\text{total_inpatient_days}}{\text{total_discharge}}$
The formula for ALOS is: ALOS = total_inpatient_days / total_discharge
The formula for ALOS is: ALOS = total_inpatient_days ÷ total_discharge




## Methods
The project employs various time series analysis techniques, including:

- __Data Extraction:__ Fetch 'Total Discharges' and 'Total Inpatient Days' dataset from FRED using the FRED API
- __Data Cleaning & Transformation:__ Format and clean raw data for analysis, and merge datasets to compute ALOS
- __Train-Test Split:__ Separate data into training and testing periods
- __Time Series EDA:__ Visualize ALOS trends and assess seasonality, use statistical tests and plots to evaluate time series stability, and apply transformations to make the data stationary
- __Model Selection:__ Choose model parameters based on ACF/PACF plots
- __Model Training & Evaluation__ Fit the model to the training data, predict ALOS for the upcoming quarters, and visualize results and assess prediction accuracy using error metrics.


## Tools
- __Programming Language:__ Python
- __Libraries:__ NumPy, Pandas, Seaborn, Matplotlib, Statsmodels
- __Environment:__ Google Colab
