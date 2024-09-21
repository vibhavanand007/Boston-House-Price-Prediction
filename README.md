### End to End project

Boston House Pricing Prediction --[Linear Regression]
[Live Link](https://boston-house-price-prediction-b1nh.onrender.com)

Create a new environment

```
conda create -p venv python==3.11.7 -y
```
1. Data Exploration and Preparation
You loaded the Boston Housing dataset and checked its structure, confirming that there are 506 rows and 13 features, with the target being the 'Price' (house prices).
You created a Pandas DataFrame, checked for missing values, and reviewed basic statistics of the data using df.describe().
The dataset includes features like CRIM (crime rate), RM (number of rooms), LSTAT (percentage of lower-status population), and others.

2. Exploratory Data Analysis (EDA)
You calculated correlations between features, observing that RM (average number of rooms) has a strong positive correlation with house prices, while LSTAT has a strong negative correlation.
Visualizations using scatter plots and seaborn's pairplot provided insights into relationships between individual features and house prices.
You visualized residuals (the difference between predicted and actual values) and explored their distribution, indicating areas where model predictions may not align with actual values.

3. Model Training and Evaluation
You split the data into training and test sets, standardized the features using StandardScaler, and trained a Linear Regression model, achieving an R² score of approximately 0.669.
You also used Ridge Regression with GridSearchCV for hyperparameter tuning, finding that an alpha of 1 was optimal. The model achieved similar R² scores to Linear Regression.
You then applied Lasso Regression with RandomizedSearchCV, tuning the alpha hyperparameter using log-spaced values.

4. Hyperparameter Tuning
Ridge Regression: GridSearchCV tested various values of alpha and returned the best alpha as 1.
Lasso Regression: RandomizedSearchCV with log-spaced alpha values explored the regularization strength.



Next Steps for Model Improvement:

Feature Engineering: Consider feature interactions, transformations, or polynomial features to capture more complex relationships.

Ensemble Methods: Try models like Random Forest, Gradient Boosting, or XGBoost to improve performance and account for non-linearities.

Cross-Validation: Use cross-validation scores to get a more robust estimate of model performance beyond train-test splits.
