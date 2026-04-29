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
## Overview
This project repository is used to store and manage files for analyzing hospital patients data.
It supports collaboration using Git and GitHub.

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
- Model Selection

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




