# Prime Number Prediction Project


## Project Overview
This project leverages machine learning techniques to predict prime numbers using a dataset that comprises the first million prime numbers. Utilising a RandomForestRegressor, the aim is to develop a predictive model capable of estimating the nth prime number with high precision. 

## Table of Contents
- [Dataset](#dataset)
- [Feature Engineering](#feature-engineering)
- [Model Training](#model-training)
- [Model Evaluation](#model-evaluation)

## Dataset
The dataset includes the first million prime numbers and features the following columns:
- `Rank`: The index of the prime number.
- `Num`: The prime number itself.
- `Interval`: The gap to the previous prime number.

## Feature Engineering
We introduced several advanced features to enhance the model's ability to predict prime numbers:
- `Log_Interval`: Logarithmic transformation of the 'Interval' to normalise its distribution.
- `Rolling_Mean_Interval`: Rolling mean of the intervals over a predefined window to capture local average trends.
- `EMA_Interval`: Exponential moving average of intervals to smooth out fluctuations and highlight longer-term trends.

## Model Training
The model was trained using the RandomForestRegressor algorithm from the scikit-learn library. The key parameters configured for the RandomForestRegressor included:
- `n_estimators`: 100
- `random_state`: 42

## Model Evaluation
The performance of the model was assessed using the following metrics:
- **Mean Squared Error (MSE)**: 248.07094757261518
- **R² Score**: 0.9999999982703944

These results indicate that the model is exceptionally accurate, capturing nearly all the variability in the data around its mean.
