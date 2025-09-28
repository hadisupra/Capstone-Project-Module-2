# Capstone-Project-Module-2
Prediction California House Price using Regression Linier


[Sumber data California house price]
<img width="254" height="199" alt="image" src="https://github.com/user-attachments/assets/ea77a2bc-d073-4bcd-95db-e5021e753666" />

(https://www.kaggle.com/datasets/camnugent/california-housing-prices/data)

### **Contents**

Data berasal dari hasil sensus tahun 1990 untuk districts California.
Setiap baris merepresentasikan district/block group dengan dengan informasi data rumah dan demografi yang sudah di kumpulkan.
Data yang di provide belum cukup bersih sehingga di perlukan conditioning data sebelumnya :
Columns yang terdapat pada dataset adalah sebagai berikut

| Column               |
|-----------------------|
| `longitude`          |
| `latitude`           |
| `housing_median_age` |
| `total_rooms`        |
| `total_bedrooms`     |
| `population`         |
| `households`         |
| `median_income`      |
| `ocean_proximity`    |
| `median_house_value` |

****
Dari dataset yang di provide kita akan mencoba memprediksi harga rumah di california, berikut ini main step yang akan di lakukan:

Main Points of Your California Housing Project
1. Dataset & Preparation
  Used the California Housing dataset (1990 Census), each row representing a district/block group with housing and demographic info.
  Columns included: longitude, latitude, housing median age, rooms, bedrooms, population, households, median income, ocean proximity, and median house     value.
  Performed data cleaning & conditioning: handled missing values, scaled features, and encoded categorical variables.

2. Exploratory Data Analysis (EDA)
  Found median income to be the strongest predictor of house prices.
  Location effects: coastal and bay areas had higher values, inland properties were cheapest.
  Target variable (median_house_value) was right‑skewed and capped at $500,001, limiting prediction accuracy for high‑end houses.
  Created visualizations: distributions, correlations, and maps showing geographic price patterns.

3. Model Benchmarking
  Tested multiple regression models:
  Linear Regression → weak baseline, high error.
  KNN & Decision Tree → moderate results, unstable.
  Random Forest & XGBoost → strong performers.
  Metrics used: RMSE, MAE, MAPE for fair comparison.

4. A/B Testing & Model Selection
  Directly compared Random Forest vs XGBoost on the same test set.
  XGBoost consistently outperformed Random Forest, with lower RMSE, MAE, and MAPE.
  Conducted hyperparameter tuning (learning rate, depth, estimators, subsample, etc.), further improving XGBoost’s performance.

5. Neural Network Experiment
  Built a feed‑forward neural network with scaled inputs.
  It learned patterns but did not outperform XGBoost, confirming that tree ensembles are better suited for this tabular dataset.
  Valuable as an exploration of deep learning, but not the final choice.

