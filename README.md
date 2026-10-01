# King County Housing Price Prediction

## Project Overview

This project was completed as part of my coursework at Appalachian State University using **RStudio**. The goal was to develop a regression model to predict residential housing prices using the **2014–2015 King County Housing dataset**.

For the project, my professor divided the dataset into two portions. I was provided with one portion containing known sale prices to use for analysis and model development. The second portion did not include sale prices and was used to generate my final predictions.

## Data Exploration & Feature Engineering

I began by exploring the relationships between the available predictors and housing prices. I then modified existing variables and created new features that could better represent factors affecting housing prices.

Some of the feature engineering included:

- Creating house age and renovation age variables
- Applying log transformations to living area and lot size
- Creating a squared bathroom term to account for a possible nonlinear relationship
- Creating interactions between living area and construction grade
- Creating interactions between living area and view quality
- Creating bedroom-to-bathroom interactions
- Creating an interaction between house age and condition
- Comparing a home's living area to the living area of nearby homes

I also applied a **log transformation to sale price** after examining the initial OLS regression diagnostics.

## Model Development

I built and compared three regression approaches:

- **Ordinary Least Squares (OLS) Regression**
- **Lasso Regression**
- **Ridge Regression**

I divided the provided housing data into training and testing sets so that I could compare how well each model performed on held-out data. Model performance was evaluated using **Mean Squared Error (MSE)**.

For Lasso and Ridge regression, I used cross-validation to select the regularization parameter, lambda.

## Model Selection

After comparing the performance of the three approaches, I selected **Ridge Regression** as my final model.

The housing dataset contains several correlated predictors, particularly variables related to the size and characteristics of a home. Ridge regression allowed these predictors to remain in the model while shrinking their coefficients through regularization.

Based on my model testing, Ridge produced the best results and was selected to generate the final housing price predictions.

## Final Predictions

After selecting Ridge, I trained the final model using the available training data and used it to predict sale prices for the unseen portion of the dataset.

Because the model was trained using log-transformed sale prices, the predictions were transformed back into dollar values before being exported.

## Tools & Techniques

- R / RStudio
- `glmnet`
- `ggplot2`
- `corrplot`
- Data cleaning and preprocessing
- Exploratory data analysis
- Feature engineering
- Correlation analysis
- OLS regression
- Lasso regression
- Ridge regression
- Regularization
- Cross-validation
- Model evaluation using MSE
- Predictive modeling

## Data Source & Acknowledgment

The original data comes from the **2014–2015 King County Housing dataset**, available through Kaggle. For this project, the dataset was provided and divided into training and prediction sets by my professor at Appalachian State University as part of the course assignment.

All data preparation, feature engineering, model development, model comparison, and final predictions included in this repository were completed by me.

## What I Learned

This project gave me experience working through a complete predictive modeling process rather than simply fitting a single regression model. I explored and modified the original data, engineered new predictors, compared multiple regression approaches, tuned regularization parameters, evaluated models using held-out data, and used the final model to make predictions on unseen observations.

One of my main takeaways was seeing how **feature engineering, correlated predictors, and regularization can affect predictive performance**, as well as why different regression methods can perform differently on the same dataset.
