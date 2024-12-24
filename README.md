# Machine Learning Project: Car Price Prediction

## Project Overview
This project involves predicting car prices using various machine learning algorithms. The dataset contains features such as car specifications and prices. The objective is to build a model that accurately predicts car prices and provides insights into the most important features influencing the price.

## Dataset
The dataset used in this project is `CarPrice_Assignment.csv`. It contains 205 rows and 26 columns, with the following key attributes:
- **car_ID**: Unique identifier for each car.
- **CarName**: Name of the car.
- **fueltype**, **aspiration**, **carbody**, etc.: Various categorical features.
- **wheelbase**, **carlength**, **carwidth**, etc.: Numerical features related to car dimensions.
- **price**: Target variable to predict.

### Data Cleaning
1. **Missing Values:** No missing values were detected.
2. **Duplicates:** No duplicate rows were found.
3. **Outlier Detection:**
   - Outliers were identified using the IQR method for numerical features.
   - Outliers were capped to reduce their impact on the model.

### Data Transformation
1. **Encoding:**
   - Label encoding was applied to ordinal categorical variables.
   - One-hot encoding was used for nominal categorical variables.
2. **Scaling:**
   - StandardScaler was applied to numerical features for normalization.
3. **Feature Selection:**
   - SelectKBest and recursive feature elimination (RFE) were used to select the top 20 features.

## Exploratory Data Analysis
1. **Descriptive Statistics:**
   - Mean, median, standard deviation, skewness, and kurtosis were calculated for numerical features.
2. **Visualizations:**
   - Histogram and KDE plots for distributions.
   - Box plots for outlier analysis.
   - Correlation heatmap to identify relationships between features.

## Machine Learning Models
The following algorithms were implemented and evaluated:
1. **Linear Regression**
2. **Decision Tree Regressor**
3. **Random Forest Regressor**
4. **Gradient Boosting Regressor**
5. **Support Vector Regressor (SVR)**

### Model Evaluation Metrics
- Mean Squared Error (MSE)
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R-squared (R²)

### Results
| Model                     | MSE          | MAE        | RMSE        | R²         |
|---------------------------|--------------|------------|-------------|------------|
| Linear Regression         | 9,542,248    | 2,009.76   | 3,089.05    | 0.8791     |
| Decision Tree Regressor   | 15,189,540   | 2,558.71   | 3,897.38    | 0.8076     |
| Random Forest Regressor   | 17,056,590   | 2,498.79   | 4,129.96    | 0.7839     |
| Gradient Boosting Regressor | 21,235,200 | 2,517.97   | 4,608.17    | 0.7310     |
| Support Vector Regressor  | 86,708,560   | 5,695.91   | 9,311.74    | -0.0984    |

### Best Model
The best-performing model was **Linear Regression**, with the highest R² score of 0.8791.

## Feature Importance
The feature importances were analyzed using the coefficients of the linear regression model. The top 10 features influencing car prices include:
1. **fueltype_diesel**
2. **wheelbase_95.7**
3. **drivewheel_rwd**
4. **drivewheel_fwd**
5. **wheelbase_93.3**

A bar chart was plotted to visualize the top 10 feature importances.

## Conclusion
1. **Key Insights:**
   - Fuel type, drive wheel, and dimensions (e.g., wheelbase) significantly impact car prices.
2. **Model Performance:**
   - Linear Regression provided the best balance of simplicity and accuracy.


## Visualizations
- **Price Distribution:** Histogram showing the distribution of car prices.
- **Correlation Heatmap:** Visual representation of feature correlations.
- **Feature Importance Bar Chart:** Top 10 features impacting the price.


