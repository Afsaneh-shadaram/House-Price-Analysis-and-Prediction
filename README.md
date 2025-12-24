## House-Price-Analysis-and-Prediction 

# Project Overview

This project is the capstone for the IBM Data Analysis course.
In this assignment, I act as a Data Analyst at a Real Estate Investment Trust (REIT) planning to invest in residential real estate. The goal is to analyze housing data and predict market prices based on key property features such as square footage, number of bedrooms, number of bathrooms, and number of floors.

# Dataset
•	Source: King County (Seattle area) house sales dataset
•	Time Period: May 2014 – May 2015
•	Original Dataset: Kaggle – House Sales Prediction <https://www.kaggle.com/datasets/harlfoxem/housesalesprediction> (here)
•	License: Creative Commons Zero (CC0 1.0 – Public Domain) <https://creativecommons.org/publicdomain/zero/1.0/.> (here)
•	Note: The dataset was slightly modified for this course

# Tools & Environment
•	Python
•	JupyterLab (Skills Network Labs – Cloud Environment)
•	Libraries: pandas, numpy, seaborn, matplotlib, scikit-learn

# Project Workflow
1. Data Wrangling
•	Imported required libraries and dataset
•	Removed unnecessary features using drop()
•	Handled missing values:
o	Replaced missing values in bathrooms and bedrooms with column means

2. Exploratory Data Analysis (EDA)
•	Used corr() to identify features most correlated with price
•	Visual analysis using seaborn:
o	regplot: Identified sqft_above as positively correlated with price
o	boxplot: Found that waterfront properties have higher prices compared to non-waterfront homes

3. Model Development
•	Simple Linear Regression (SLR)
o	Feature: sqft_living
o	R² score: 0.49
•	Multiple Linear Regression (MLR)
o	Used multiple relevant features
o	R² score: 0.65
•	Polynomial Regression with Pipeline
o	Pipeline included:
	StandardScaler
	PolynomialFeatures
	LinearRegression
Improved R^2 and model performance compared to basic linear models without polynomial features.

4. Model Evaluation and Refinement
•	Train/Test Split
o	85% training / 15% testing
•	Ridge Regression
o	Regularization parameter (alpha): 0.1
o	Test R² score: 0.64
•	Polynomial Ridge Regression (2nd Order)
o	Applied polynomial transformation to train and test data
o	Ridge regression with alpha = 0.1
o	Test R² score improved to 0.70
•	Model Validation
o	Distribution plot shows strong alignment between actual prices and predicted prices

# Key Takeaways

•	Feature engineering and regularization significantly improve prediction accuracy
• Waterfront view and square footage are strong predictors of house prices
• Polynomial Ridge Regression provided the best overall performance
•	Waterfront view and square footage are strong predictors of house prices
•	Polynomial Ridge Regression provided the best overall performance
