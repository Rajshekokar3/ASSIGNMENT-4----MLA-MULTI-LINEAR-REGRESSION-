# Multiple Linear Regression: Toyota Corolla Price Prediction
Welcome to the Toyota Corolla Price Prediction project! This repository contains a comprehensive analysis to predict the price of Toyota Corolla cars using multiple linear regression (MLR). The dataset includes various attributes of the car, such as age, mileage, and specifications, which are used to build and evaluate predictive models.

# Objective
The primary goal of this project is to develop and evaluate multiple linear regression models to predict the price of Toyota Corolla cars and apply regularization techniques (Lasso and Ridge) to improve the model’s performance.

# Dataset Description
The dataset includes the following variables:

Variable	Description
Age	Age of the car in years
KM	Accumulated kilometers on the odometer
FuelType	Fuel type (Petrol, Diesel, CNG)
HP	Horsepower
Automatic	Transmission type (Yes=1, No=0)
CC	Cylinder volume in cubic centimeters
Doors	Number of doors
Weight	Weight of the car in kilograms
Quarterly_Tax	Quarterly tax paid in Euros
Price	Offer price in Euros (target variable)


# Tools and Libraries
# This project uses Python and the following libraries:

Data Manipulation: pandas, numpy
Data Visualization: matplotlib, seaborn
Modeling and Evaluation: scikit-learn, statsmodels


# Project Workflow
1. Exploratory Data Analysis (EDA)
Conducted a thorough analysis to understand the dataset structure.
Summary statistics (mean, median, standard deviation) were calculated for all variables.
Visualizations included:
Histograms for variable distributions.
Correlation heatmaps to identify relationships between variables.
Boxplots to detect outliers.
Data preprocessing steps:
Handled missing values and standardized numerical variables.
Converted categorical variables (e.g., FuelType, Doors) into dummy variables.
Detected and treated outliers using appropriate techniques.
2. Data Splitting
Split the dataset into:
Training Set: 80% of the data for model training.
Testing Set: 20% of the data for evaluation.
3. Multiple Linear Regression Models


# Built three different models for comparison:

Model 1: Baseline MLR
Included all variables in the dataset.
Interpreted coefficients to assess the influence of each feature on the price.
Model 2: Feature Selection
Performed feature selection using correlation analysis and stepwise regression.
Removed redundant or insignificant variables to simplify the model.
Model 3: Interaction Terms
Explored interaction effects between significant variables (e.g., Age × KM).
For all models, regression assumptions were validated:

Linearity
Homoscedasticity
Multicollinearity (checked using Variance Inflation Factor - VIF)
Normality of residuals
4. Model Evaluation
Evaluated the performance of all models using the testing dataset.
Metrics used:
R-squared: Proportion of variance explained by the model.
Mean Squared Error (MSE): Measures average squared error.
Mean Absolute Error (MAE): Measures average absolute error.
5. Regularization Techniques
Applied Lasso Regression and Ridge Regression to address overfitting and multicollinearity:
Lasso adds L1 regularization to shrink less significant coefficients to zero.
Ridge adds L2 regularization to minimize coefficient magnitude without eliminating features.
Optimized hyperparameters (e.g., alpha) using cross-validation.


# Key Findings
Age and KM are the most significant predictors of car price, with older cars and higher mileage associated with lower prices.
Weight and FuelType also influence price, with heavier cars and diesel fuel types generally having higher prices.
Regularization techniques (Lasso and Ridge) improved model generalizability by reducing overfitting.
