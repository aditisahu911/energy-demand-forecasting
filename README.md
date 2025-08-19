# Time Series Forecasting with ARIMA: Electricity Load and Solar Generation Analysis

## Overview

This repository contains the complete workflow for analyzing and forecasting electricity load (`IT_load_new`) and solar generation (`IT_solar_generation`) time series data for the year 2016 using ARIMA models.

The project implements key preprocessing steps, stationarity testing, model building, evaluation, and visualization to provide actionable forecasting insights.

---

## Dataset

The dataset records hourly observations throughout 2016:

| Column Name        | Description                                           |
| ------------------ | ----------------------------------------------------|
| `utc_timestamp`    | Timestamp for each hourly observation                 |
| `IT_load_new`      | Electric load values                                  |
| `IT_solar_generation` | Solar power generation values                       |

---

## Project Structure

- `app.py` — Main Python script containing data processing, modeling, and plotting workflows  
- Model files (`clf.pkl`, `tfidf.pkl`, `encoder.pkl`) — Supporting model assets, included if applicable  
- `requirements.txt` — Project dependencies for easy environment setup  
- Dataset CSV — The time series data file, included or referenced as needed  
- Jupyter notebooks (optional) — For interactive experimentation and exploratory analysis  

---

## Methodology

1. **Data Loading & Visualization:** Time series plots to identify temporal patterns and signal characteristics.  
2. **Missing Value Imputation:** Forward filling to ensure continuous data series.  
3. **Stationarity Testing:** Augmented Dickey-Fuller (ADF) applied to confirm stationarity before modeling.  
4. **Parameter Selection:** Autocorrelation (ACF) and Partial Autocorrelation (PACF) plots guide choices of ARIMA parameters `p` and `q`.  
5. **Model Fitting & Forecasting:** ARIMA fitted on 80% training data; performance evaluated on 20% test data.  
6. **Evaluation:** Root Mean Squared Error (RMSE) quantifies prediction accuracy; predictions are also visually compared with actual values.  

---

## Key Results

- The ARIMA(2,0,2) model achieved an RMSE of approximately **7,715** for electricity load forecasting.  
- The same ARIMA configuration produced an RMSE of around **2,486** for solar generation.  
- Visualizations confirm that the ARIMA models capture the primary temporal structure of both series, despite some residual variability.

---

## Installation

To set up the environment and run the project locally, execute:

`pip install -r requirements.txt`


The script will process the data, fit ARIMA models, and produce plots comparing actual vs. predicted values for both load and solar generation.

---

## Future Work

- Incorporate exogenous variables and seasonal components to enhance model accuracy  
- Explore advanced forecasting techniques such as SARIMA, Prophet, or LSTM architectures  
- Conduct hyperparameter tuning and cross-validation for robust model selection  

---

## Contact

For questions or collaboration inquiries, please reach out at aditisahu24@iitk.ac.in.

---

*This project merges rigorous data analysis with effective visualization to support electric power forecasting and planning.*

