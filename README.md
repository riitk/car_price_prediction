# car_price_prediction
Car Price Prediction Using ML

# Car Price Prediction using Machine Learning

## Overview
This project aims to predict the selling price of cars using various features of car listings. The dataset used contains information about the car's name, manufacturing year, kilometers driven, fuel type, seller type, transmission type, and ownership details.

## Dataset
The dataset used for this project can be found on Kaggle and contains 4340 rows with the following columns:

- `name`: The name of the car.
- `year`: The year the car was manufactured.
- `selling_price`: The selling price of the car.
- `km_driven`: The total kilometers driven by the car.
- `fuel`: The type of fuel used by the car (Diesel, Petrol, CNG, LPG).
- `seller_type`: The type of seller (Individual, Dealer, Trustmark Dealer).
- `transmission`: The type of transmission (Manual, Automatic).
- `owner`: The ownership status (First Owner, Second Owner, etc.).

## Data Preprocessing
1. **Basic Analysis**: Checked for null values, dataset shape, and descriptive statistics using `df.info()` and `df.describe()`.
2. **Feature Extraction**: Extracted the company name from the `name` column using a lambda function.
3. **Data Visualization**: 
   - Plotted various graphs (countplot, barplot, histplot) to understand relationships between columns.
   - Used heatmaps and correlation matrices.
4. **Outlier Removal**:
   - Removed the row for the electric car due to its low count.
   - Removed outliers in `selling_price` and `km_driven`.
5. **Encoding Categorical Variables**:
   - `transmission`: Manual (0), Automatic (1)
   - `seller_type`: Individual (0), Dealer (1), Trustmark Dealer (2)
   - `fuel`: Diesel (0), Petrol (1), CNG (2), LPG (2)
6. **Creating Dummy Variables**:
   - For `year` and `name` columns, converted them into dummy variables and dropped the original columns.

## Model Training
Performed train-test split and used two models for training:
1. **Linear Regression**
2. **Lasso Regression**

## Model Evaluation
Evaluated models using:
- **Mean Squared Error (MSE)**
- **R-squared (R²) Score**
- **Root Mean Squared Error (RMSE)**

### Results
- **Linear Regression**: R² Score = 0.7171
- **Lasso Regression**: R² Score = 0.7171

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/riitk/car-price-prediction.git
   cd car-price-prediction
