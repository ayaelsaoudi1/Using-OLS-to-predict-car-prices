# Car Price Prediction using Linear Regression

This repository contains a Jupyter Notebook demonstrating the application of linear regression to predict car prices using a dataset of 4,345 car records. The dataset includes various features like brand, mileage, engine volume, and more, which were preprocessed and analyzed to develop a predictive model.  

---

## Dataset
The dataset used in this project includes the following columns:
- **Brand**: The manufacturer of the car.
- **Price**: The target variable (car price).
- **Body**: The type of car body (e.g., sedan, SUV).
- **Mileage**: The mileage of the car.
- **EngineV**: Engine volume.
- **Engine Type**: The type of engine (e.g., petrol, diesel).
- **Registration**: Whether the car is registered.
- **Year**: The year the car was manufactured.
- **Model**: The specific model of the car (excluded from the analysis).

---

## Preprocessing
1. **Handling Missing Values**:
   - Removed missing values as they represented less than 5% of the dataset.
2. **Feature Exclusion**:
   - Excluded the `Model` feature because it can be determined from other features like `Brand`, `Year`, and `EngineV`.
3. **Outlier Removal**:
   - Removed outliers by analyzing the Probability Distribution Functions (PDF) of the features.
4. **Target Transformation**:
   - Applied a log transformation on `Price` to ensure a linear relationship with the features.
5. **Multicollinearity Check**:
   - Used Variance Inflation Factor (VIF) to check and address high correlation between variables.
6. **Categorical Variables**:
   - Converted categorical variables into dummy variables and checked their correlation using VIF.

---

## Model Development
1. **Model Selection**:
   - Linear Regression was selected as the model.
2. **Data Splitting**:
   - Split the data into training (80%) and testing (20%) sets.
3. **Residual Analysis**:
   - The residuals' PDF was normal, but some observations had much higher predicted prices compared to actual ones.

---

## Model Performance
- **Training Set**:
  - For higher prices, predictions closely followed the observed values.
  - For lower prices, predictions were scattered, indicating lower accuracy.
- **Test Set**:
  - Minimum difference: **0.06%**.
  - Maximum difference: **512%** (off mark).
  - Most predictions were relatively close to observed values (as shown by percentiles).

---

## Limitations
The model is not outstanding, and the following issues were observed:
- Poor prediction accuracy for lower-priced cars.
- Outliers significantly impacted the model's performance.

---

## How to Improve the Model
1. Use a different set of variables to better capture price determinants.
2. Remove a larger portion of outliers to improve prediction accuracy.
3. Experiment with different types of transformations on features and the target variable.
4. Explore advanced regression techniques or other machine learning algorithms.

---
