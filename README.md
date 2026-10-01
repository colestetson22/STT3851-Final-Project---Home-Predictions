# King County Housing Price Prediction

## Project Overview

This project was completed as part of my coursework at Appalachian State University using **RStudio**. The goal was to develop a regression model to predict residential housing prices using the **2014–2015 King County Housing dataset** from Kaggle.

For the project, my professor split the dataset into two portions. I was given one portion with known sale prices to analyze, modify, and use for model development. The final model was then used to predict housing prices for the remaining portion of the data.

## Data Preparation & Feature Engineering

I began the analysis by exploring the original variables and preparing the data for modeling. Rather than using only the variables in their original form, I modified existing features and created new variables that could better represent characteristics affecting housing prices.

This stage included:

- Exploring the distributions and relationships between variables
- Transforming and modifying existing variables
- Creating new features from the available housing data
- Preparing categorical and numerical variables for regression
- Identifying variables that could improve prediction performance

## Model Development

After preparing the data, I built and compared three regression approaches:

- **Ordinary Least Squares (OLS) Regression**
- **Lasso Regression**
- **Ridge Regression**

I evaluated the models based on their ability to predict housing prices on unseen data. Lasso and Ridge regression were explored as regularized alternatives to OLS, allowing me to examine whether controlling coefficient size could improve predictive performance.

After comparing the models, I selected **Ridge Regression** as my final model because it produced the best results for this dataset.

## Final Prediction

The final Ridge model was trained using the provided training data and then applied to the held-out portion of the King County dataset to generate predicted housing prices.

## Skills Demonstrated

- R / RStudio
- Data cleaning and preprocessing
- Exploratory data analysis
- Feature engineering
- Ordinary Least Squares regression
- Lasso regression
- Ridge regression
- Regularization
- Model comparison and evaluation
- Predictive modeling

## Dataset

The project uses the **2014–2015 King County House Sales dataset** from Kaggle. The dataset contains information about residential properties in King County, Washington, including housing characteristics, location information, and sale prices.

## Purpose

The purpose of this project was to gain experience with the full predictive modeling process—from exploring and modifying raw data to engineering features, comparing regression techniques, selecting a final model, and using that model to make predictions on unseen data.
