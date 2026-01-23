# 🚲 Bike Sharing Demand Prediction

## Objective
Predict how many bicycles will arrive at a given station in the next 60 minutes. This project compares the performance of **Zero-Inflated Regression models** with and without the inclusion of weather data.

## Project Structure
The analysis is split into two Jupyter notebooks:

1.  **`Bike_Sharing_Demand_With_Weather.ipynb`**
    * Includes weather features (Temperature, Visibility, Wind Speed, Rain, etc.).
    * Merges trip data with station and weather datasets.
2.  **`Bike_Sharing_Demand_Without_Weather.ipynb`**
    * Baseline model relying solely on historical trip and station data.
    * Excludes weather-related features to isolate their impact on prediction accuracy.

## Data Sources
* **Trips Data**: Historical trip records (filtered for 2021).
* **Stations Data**: Metadata including station names and regions.
* **Weather Data**: Hourly weather metrics (used in the "With Weather" analysis).

## Methodology
* **Data Cleaning**: handling missing values, merging datasets, and filtering for relevant trips (e.g., duration ≤ 90 mins, distance ≤ 10km).
* **EDA**: Analyzing busiest times, route categories, passholder types, and station hotspots.
* **Modeling**: Implementation of **Zero-Inflated Regressors** (via `sklego`) to handle the excess zeros in demand data.
    * **Base Models Tested**: Decision Trees, Random Forest, Extra Trees, Gradient Boosting, AdaBoost, XGBoost, LightGBM, and CatBoost.

## Requirements
* Python 3.x
* pandas
* numpy
* matplotlib & seaborn
* scikit-learn
* scikit-lego
* xgboost
* lightgbm
* catboost
