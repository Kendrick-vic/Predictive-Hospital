# Hospital Admission Forecasting using SARIMA Forecasting Model
We are building a data analyst solution to forecast hospital resources allocation, addressing real-world challenges such as overcrowding, bed shortage, and inefficient staff utilization through data driven insights and interactive dashboard. 

# Problem Statement
Healthcare systems generate large amounts of data daily, including patient admissions and bed usage.
Many hospitals still rely on reactive decisions instead of data-driven planning.
This often leads to overcrowding, resource shortages, or underutilization.
Poor planning can reduce the quality of patient care.
Forecasting hospital data helps predict future demand.
It allows better allocation of staff, beds, and medical resources.
It is especially important during peak periods like disease outbreaks.
Accurate forecasts improve hospital efficiency and operations.
They also support better patient outcomes and service delivery.
This project uses historical data to provide predictive insights for better decision-making.

## Project Overview

This project uses SARIMA time-series modeling to forecast daily hospital admissions.
Accurate forecasting helps hospitals plan staffing, manage bed occupancy, and improve resource allocation.

## Objectives
- To forecast daily hospital admissions using time-series analysis (SARIMA)
- Clean and organize hospital data
- Generate insights for decision-making

## Dataset
**Souce:** Synthetic dataset created for time-series forecasting practice

**Access:** [View dataset](https://docs.google.com/spreadsheets/d/1F8YbWkqpu282zeTUmYgBTCQgeovWWVho/edit?usp=drive_link&ouid=101342511537791973894&rtpof=true&sd=true)

Number of records: 91

Variables:
- date: Daily timestamp of hospital records
- daily_admissions: Number of patients admitted per day
- daily_discharges: Number of patients discharged per day
- bed_occupancy: Total occupied hospital beds
- is_holiday: Indicator for public holidays (1 = Yes, 0 = No)

## Methodology
- Data cleaning
- Stationarity test(ADF)
- ACF/PACF
- Model Selection: SARIMA


</> Markdown
## **KEY INSIGHTS AND RESULTS**
## Data & Pattern Insights
- The dataset contains daily hospital records over a 3-month period.
- A clear weekly pattern (7-day cycle) was observed in hospital admissions.
- Admissions tend to fluctuate based on weekday vs weekend effects, indicating strong seasonality.
## Stationarity Findings
- Augmented Dickey-Fuller (ADF) test showed the original series is stationary (p < 0.05).
- Therefore, no non-seasonal differencing was required (d = 0).
- Seasonal differencing at lag 7 was applied to remove weekly seasonality.
- The seasonally differenced series was confirmed stationary (p < 0.05), hence D = 1.
## ACF & PACF Analysis
- ACF and PACF plots showed no strong significant spikes outside the confidence intervals.
- This indicates weak autoregressive (AR) and moving average (MA) components.
- Both seasonal and non-seasonal lag effects were minimal.
## Model Selection
- Based on stationarity tests and ACF/PACF analysis, a SARIMA model was selected.
- Final model used: SARIMA (1,0,1)(1,1,1,7)
- The model accounts for:
  - No trend differencing (d = 0)
  - Weekly seasonality (s = 7)
  - Seasonal differencing (D = 1)
## Forecasting Results
- The model successfully captured weekly seasonal patterns in hospital admissions.
- Forecasts showed stable and predictable short-term trends.
- The model is suitable for predicting hospital admissions over a 14-day horizon.
## Pratical Implications
- Hospitals can use the model to anticipate daily patient inflow.
- Helps in staff scheduling and resource allocation.
- Supports better planning for bed occupancy and patient management.
## Model Summary
- Model Type: SARIMA
- Order: (1, 0, 1)
- Seasonal Order: (1, 1, 1, 7)
- Forecast Horizon: 14 days


## Folder Structure
- data/ : Contains raw and processed datasets
- notebooks/ : Analysis notebooks
- scripts/ : Data cleaning and automation scripts
- docs/ : Project documentation

## Tools and Technologies
- Git and GitHub
- Excel / Python (as applicable)

## Collaboration Guidelines
- All changes should be committed with clear commit messages
- Pull requests should be used for major changes




