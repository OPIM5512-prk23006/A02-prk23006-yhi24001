# A02-prk23006-yhi24001
Ping Pong Assignment
Authors: Pranaydeep Khare, Arijita Pani
----
## 🏠California Housing Price Prediction using MLP Regressor

This project builds and evaluates a Neural Network regression model (MLPRegressor) to predict median house values in California using the well-known California Housing dataset from scikit-learn. The workflow covers data loading, exploratory data analysis (EDA), preprocessing, model training, and evaluation, with a focus on understanding model performance and limitations (especially with outliers).

## 📊 Dataset
Source: sklearn.datasets.fetch_california_housing
Target Variable: MedHouseVal
Features:
MedInc – Median income
HouseAge – Median house age
AveRooms – Average number of rooms
AveBedrms – Average number of bedrooms
Population – Block population
AveOccup – Average household occupancy
Latitude
Longitude
MedHouseVal-Median house valuation

## 🔍 Exploratory Data Analysis (EDA)
Histograms plotted for all input features (excluding target)
Helps to visualize:
 -Feature distributions
 -Skewness and presence of outliers
 -Scale differences between variables

#✂️ Train–Test Split
Train size: 80%

Test size: 20%

Random state: 42

Target variable separated before splitting. 
 
