# House-Price-Analysis-and-Prediction 

## Project Overview

This project is the capstone for the IBM Data Analysis course.
In this assignment, I act as a Data Analyst at a Real Estate Investment Trust (REIT) planning to invest in residential real estate. The goal is to analyze housing data and predict market prices based on key property features such as square footage, number of bedrooms, number of bathrooms, and number of floors using different LinearRegression models, Ridge Regression and Polynomial Features.

## Dataset
*	Source: King County (Seattle area) house sales dataset
*	Time Period: May 2014 – May 2015
*	Original Dataset: Kaggle – House Sales Prediction [(here)](https://www.kaggle.com/datasets/harlfoxem/housesalesprediction). 
*	License: Creative Commons Zero (CC0 1.0 – Public Domain) [(here)](https://creativecommons.org/publicdomain/zero/1.0/.).
*	Note: The dataset was slightly modified for this course

## Tools & Environment
*	Python
*	JupyterLab (Skills Network Labs – Cloud Environment)
*	Libraries: pandas, numpy, seaborn, matplotlib, scikit-learn

## Project Workflow
1. Data Wrangling
*	Imported required libraries and dataset
*	Removed unnecessary features using drop()
*	Handled missing values:
	Replaced missing values in bathrooms and bedrooms with column means

2. Exploratory Data Analysis (EDA)
* Used corr() to identify features most correlated with price
* Visual analysis using seaborn:
	* regplot: Identified sqft_above as positively correlated with price
	* boxplot: Found that waterfront properties have higher prices compared to non-waterfront homes

3. Model Development
*	Simple Linear Regression (SLR)
	Feature: sqft_living
	R² score: 0.49
*	Multiple Linear Regression (MLR)
	Used multiple relevant features
	R² score: 0.65
*	Polynomial Regression with Pipeline
	Pipeline included:
	StandardScaler
	PolynomialFeatures
	LinearRegression
Improved R^2 and model performance compared to basic linear models without polynomial features.

4. Model Evaluation and Refinement
*	Train/Test Split
	85% training / 15% testing
*	Ridge Regression
	Regularization parameter (alpha): 0.1
	Test R² score: 0.64
*	Polynomial Ridge Regression (2nd Order)
	Applied polynomial transformation to train and test data
	Ridge regression with alpha = 0.1
	Test R² score improved to 0.70
*	Model Validation
	Distribution plot shows strong alignment between actual prices and predicted prices

![Q11](https://github.com/user-attachments/assets/0e676d1c-ccd1-4ece-85c7-bbecc5abba41)


## Key Takeaways

*	Feature engineering and regularization significantly improve prediction accuracy
*  Square footage is strong predictor of house prices
*  Polynomial Ridge Regression provided the best overall performance
*	Waterfront view and square footage are strong predictors of house prices
*	Polynomial Ridge Regression provided the best overall performance
