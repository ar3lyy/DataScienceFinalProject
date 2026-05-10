# Rainfall Occurrence Prediction

This project predicts rainfall occurrence in New Brunswick, New Jersey using historical weather data. The goal is to classify whether a day was rainy or non-rainy based on weather variables such as temperature, humidity, wind speed, wind gusts, dew point, and atmospheric pressure.

## Project Overview

We combined weather data from two sources:

- **Open-Meteo**: hourly weather data, including temperature, humidity, rainfall, wind speed, wind gusts, and dew point
- **Meteostat**: daily weather data, used mainly for atmospheric pressure

The hourly Open-Meteo data was aggregated into daily values and merged with Meteostat data by date. Rainfall was converted into a binary target variable:

- `0` = No Rain
- `1` = Rain

A logistic regression model was trained to classify rainfall occurrence.

## Files

- `RainPredictionModel.ipynb` — main notebook containing data cleaning, EDA, model training, and evaluation
- `open-meteo.csv` — Open-Meteo weather dataset
- `meteostat.csv` — Meteostat weather dataset
- `README.md` — project description

## Methods Used

- Data cleaning and preprocessing with Pandas
- Exploratory data analysis with Matplotlib and Seaborn
- Logistic Regression with Scikit-Learn
- Evaluation using accuracy, precision, recall, F1-score, log loss, ROC-AUC, and confusion matrix

## Results

The logistic regression model achieved strong performance on the test set:

- Accuracy: 0.8649
- Precision: 0.8333
- Recall: 0.7692
- F1-score: 0.8000
- ROC-AUC: 0.91

The results showed that moisture-related variables, especially relative humidity and dew point, were important for distinguishing rainy days from non-rainy days.

## Limitations

This model classifies rainfall occurrence using same-day weather variables. It does not predict exact rainfall amount or serve as a full future weather forecasting system. The dataset also focuses only on New Brunswick, New Jersey and does not include winter weather conditions.

## Tools

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
