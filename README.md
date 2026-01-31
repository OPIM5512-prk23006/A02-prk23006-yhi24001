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

## ✂️ Train–Test Split
Train size: 80%, Test size: 20%, Random state: 42
Target variable separated before splitting. 

## ⚙️Data Preprocessing
Feature Scaling
Different scaling strategies were applied using a ColumnTransformer:
StandardScaler applied to:
- MedInc
- HouseAge
- AveRooms
- AveBedrms
- Population
- AveOccup

No scaling (passthrough):
-Latitude
-Longitude
This ensures numerical stability for the neural network while preserving geographic features.
 
## 🧠 Model: MLP Regressor
A Multi-Layer Perceptron Regressor was trained with the following configuration:
Hidden layers: (16, 8)
Learning rate: 0.01
Max iterations: 1000
Early stopping: Enabled
Random state: 67
The model was trained on scaled training data and evaluated on both training and test sets.

## 📈 Model Evaluation
Metrics Used
Root Mean Squared Error (RMSE)
Mean Absolute Error (MAE) 

Results (Test Set)
 -RMSE: 0.76
 -MAE: 0.56

The model struggles with outliers, particularly at higher house values, which is visible in the prediction scatter plots.

## 📉 Visualization
Actual vs Predicted plots for:
Training data
Test data

These plots highlight:
-Reasonable fit for mid-range values
-Underprediction for high-value houses
-Increased error variance in the test set

## 🧪 Observations & Limitations
-Neural networks are sensitive to outliers in regression tasks
-Target variable was not transformed (e.g., log-scale), which may impact performance
-Model capacity may be insufficient for capturing extreme price variations

## 🛠️ Tech Stack
-Python
-NumPy
-Pandas
-Matplotlib & Seaborn
-Scikit-learn

## 📌 Conclusion
This project demonstrates an end-to-end regression workflow using neural networks on tabular data. While the MLP model captures general trends, handling outliers and improving robustness remains a key challenge.
