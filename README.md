# Flight Fare Prediction

## Overview

This project aims to predict flight fares based on various features of flights. The dataset includes information about the airline, source and destination cities, journey date, departure and arrival times, and more. The goal is to build a predictive model to estimate flight prices using machine learning algorithms.

## Dataset

The dataset contains the following columns:

- `Total_Stops`: Number of stops in the flight
- `Price`: The target variable (flight fare)
- `Journey_day`: Day of the journey
- `Journey_month`: Month of the journey
- `Dep_hour`: Hour of departure
- `Dep_min`: Minute of departure
- `Arrival_hour`: Hour of arrival
- `Arrival_min`: Minute of arrival
- `Duration_hours`: Duration of the flight in hours
- `Duration_mins`: Duration of the flight in minutes
- `Airline_*`: One-hot encoded columns for various airlines
- `Source_*`: One-hot encoded columns for source cities
- `Destination_*`: One-hot encoded columns for destination cities

## Data Preprocessing

1. **Data Cleaning**: Dropped columns that are not needed for modeling.
2. **Feature Encoding**: Converted categorical variables into one-hot encoded columns.
3. **Feature Selection**: Used `ExtraTreesRegressor` to determine feature importance.

## Exploratory Data Analysis

- Visualized correlations between features using a heatmap.

## Models and Evaluation

### Models

1. **Linear Regression**: Basic model to predict flight prices.
2. **Decision Tree Regressor**: Non-linear model for regression.
3. **Random Forest Regressor**: Ensemble model for regression.
4. **Gradient Boosting Regressor**: Boosted ensemble model for regression.
5. **XGBoost Regressor**: Advanced gradient boosting model for regression.

### Model Performance

- **Linear Regression**: R² score = 0.6196
- **Decision Tree Regressor**: R² score = 0.7239
- **Random Forest Regressor**: R² score = 0.7964
- **Gradient Boosting Regressor**: R² score = 0.7859
- **XGBoost Regressor**: R² score = 0.8460
- **Cross-Validation Score**: 0.8471
- **Mean Absolute Error**: 1126.70

## Hyperparameter Tuning

Performed hyperparameter tuning for the XGBoost Regressor using `RandomizedSearchCV`:

- **Best Parameters**:
  - `n_estimators`: 150
  - `max_depth`: 6
  - `learning_rate`: 0.2

- **Optimized Model Performance**: R² score = 0.8492

## Installation

To run this project, you need to have the following Python libraries installed:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `xgboost`


