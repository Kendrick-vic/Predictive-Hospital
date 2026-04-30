# 🏥 Hospital Admissions Forecasting using SARIMA

## 📌 Problem Statement

Hospitals experience fluctuating patient admissions, making it difficult to efficiently allocate resources such as staff, beds, and medical supplies.
Without accurate forecasting, this can lead to **overcrowding, staff shortages, or underutilization of resources**.

This project addresses the problem by using time-series forecasting to **predict future hospital admissions**, enabling better planning and decision-making.

---

## 📖 Project Overview

This project applies the **SARIMA (Seasonal ARIMA)** model to forecast daily hospital admissions using historical data.
The goal is to identify patterns, especially **seasonality**, and generate reliable short-term forecasts.

---

## 🎯 Objective

* Analyze historical hospital admission data
* Identify trends and seasonal patterns
* Build a SARIMA model for forecasting
* Generate accurate short-term predictions

---

## 📊 Dataset

**Source:** Simulated dataset for time-series forecasting practice
**Access:** [View dataset](https://docs.google.com/spreadsheets/d/1F8YbWkqpu282zeTUmYgBTCQgeovWWVho/edit?usp=drive_link&ouid=101342511537791973894&rtpof=true&sd=true)

**Number of records:** 91

**Variables:**

* `date`: Daily timestamp of hospital records
* `daily_admissions`: Number of patients admitted per day
* `daily_discharges`: Number of patients discharged per day
* `bed_occupancy`: Total occupied hospital beds
* `is_holiday`: Indicator for public holidays (1 = Yes, 0 = No)

The dataset represents daily hospital activity over a 3-month period.

---

## 🛠️ Methodology

### 1. Data Preprocessing

* Converted `date` column to datetime format
* Set date as index for time-series analysis
* Ensured consistent daily frequency

---

### 2. Stationarity Testing

* Applied **Augmented Dickey-Fuller (ADF) test**
* Result: Series is **non-seasonally stationary**
* Therefore:

  * `d = 0`

---

### 3. Seasonal Analysis

* Identified **weekly seasonality (s = 7)**
* Applied seasonal differencing
* ADF test confirmed stationarity
* Therefore:

  * `D = 1`

---

### 4. ACF & PACF Analysis

* Used ACF and PACF plots to identify model parameters
* Observed weak AR and MA components
* Selected low-order parameters to avoid overfitting

---

### 5. Model Building

Final SARIMA model:

```python
SARIMA (1, 0, 1)(1, 1, 1, 7)
```

This model captures:

* Short-term dependencies
* Weekly seasonal patterns

---

## 📈 Forecast Results

The model was used to forecast hospital admissions for the next 14 days.

![Forecast Plot](Downloads/forecast.png)
---

## 📉 Model Performance

*(Update after evaluation)*

* MAE: 14.5 
* RMSE: 19.20
The model’s predictions deviate from actual values by an average of approximately 14–15 patients per day. The higher RMSE indicates the presence of occasional larger prediction errors, which is expected due to fluctuations in hospital demand.

---

## 🔍 Key Insights

* Strong **weekly seasonality** observed
* Admissions follow predictable weekday/weekend patterns
* Data required **seasonal differencing**, not trend differencing
* SARIMA effectively captured repeating admission cycles

---

## 🏥 Practical Implications

* Enables hospitals to **anticipate patient inflow**
* Supports **better staff scheduling**
* Improves **bed occupancy management**
* Helps reduce **overcrowding risks**

---

## ⚙️ Tools & Libraries

* Python
* pandas
* numpy
* matplotlib
* statsmodels

---

## ▶️ How to Run the Project

```bash
git clone https://github.com/Kendrick-vic/Predictive-Hospital.git
cd Predictive-Hospital
pip install -r requirements.txt
jupyter notebook
```

---

## 🚀 Future Improvements

* Incorporate external variables (e.g., holidays, weather)
* Compare with machine learning models (LSTM, XGBoost)
* Deploy as a web-based forecasting dashboard

---

## 👤 Author

Victor Ola
