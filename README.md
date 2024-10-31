Election 2024 Forecast

Overview

This repository contains the R Markdown notebook, data, and code used for predicting the outcome of the 2024 United States Presidential Election. The project utilizes public health, demographic, and historical election data to make predictions using a variety of machine learning models. The goal is to predict the margin of victory for each state, with a focus on identifying trends in key swing states that could influence the final election outcome.

Project Contents

Election_2024_Forecast.Rmd: The main R Markdown notebook, which includes the following steps:

Data Preprocessing: Reading, transforming, and imputing missing data.

Modeling: Creating linear, logistic, and random forest models to predict election results.

Feature Engineering: Creating and evaluating interaction terms.

Model Evaluation: Assessing model performance through cross-validation and statistical measures.

Swing State Analysis: Analyzing key predictors, such as vaccine uptake, mail-in ballots, and migration rates, across swing states over time.

model_data_outlier_remove.csv: The dataset used for training the models, including historical data and predictors such as vaccine uptake, domestic migration rate, and mail-in ballot requests.

predict_data.csv: The dataset used for predicting election results based on the trained models.

predict_data_with_predictions_2.csv: The output file that contains predictions for each state, generated from the models.

combined_data.csv: A dataset combining historical data with predicted values for additional analysis.

Data Sources

The following data sources were used in this analysis:



MIT Election Lab -https://electionlab.mit.edu/data#data


UF Election Lab https://data.cdc.gov/Vaccinations/Cumulative-Percentage-of-Adults-18-Years-and-Older/hm35-qkiu/about_data


Voter turnout statistics 

CDC https://data.cdc.gov/Vaccinations/Cumulative-Percentage-of-Adults-18-Years-and-Older/hm35-qkiu/about_data
https://www.cdc.gov/covidvaxview/interactive/adults.html
https://data.cdc.gov/Vaccinations/COVID-19-Vaccinations-in-the-United-States-Jurisdi/unsk-b7fc/about_data
https://www.cdc.gov/covidvaxview/weekly-dashboard/vaccine-administration-coverage-jurisdiction.html
Five Thirty Eight https://github.com/fivethirtyeight/election-results/blob/main/election_results_senate.csv
Census- Population Migration https://www.census.gov/newsroom/press-kits/2023/national-state-population-estimates.html
NCHS- State Population Health Statistics https://www.cdc.gov/nchs/data_access/VitalStatsOnline.htm


Model Descriptions

The following models were used to train and predict election results:

Linear Regression: Trained with cross-validation to estimate the Democratic margin of victory in each state.

Logistic Regression (Elastic Net Regularization): Utilizes key predictors to classify states as either a win or loss for the Democratic party.

Random Forest: Uses ensemble learning to estimate margin of victory based on multiple predictors.

Analysis of Swing States

The analysis focuses on six key swing states: Arizona, Nevada, Wisconsin, Georgia, North Carolina, and Pennsylvania. Key indicators such as vaccine uptake, mail-in ballot requests, and domestic migration rate were tracked over time to gain insights into potential shifts in voter sentiment.

Instructions for Running the Notebook

Install Required Packages: Use the install.packages() function to install the required R packages.

Run the Notebook: The notebook can be run in RStudio by opening Election_2024_Forecast.Rmd.

View Outputs: The model predictions are saved to predict_data_with_predictions_2.csv and the combined dataset to combined_data.csv.

How to Use the Repository

This repository is designed for researchers, data scientists, and anyone interested in election forecasting using data-driven methods. You can:

Reproduce the analysis by running the R Markdown file.

Use the datasets to explore further and build upon the analysis.

Modify the code to adapt to other election forecasting needs.

Data Notes and Assumptions

Vaccine Uptake Data: Imputed missing values for a few states to ensure coverage.

Mail-in Voting Data: Used historical averages where current year data was unavailable.

Outliers: Removed states like Washington, D.C., and Alaska for certain years to avoid skewing the model.

Predictor Variables: Predictors include demographic, health, and election-related data points aimed at estimating public support for the Democratic party.
