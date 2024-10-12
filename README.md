# Sunspot Count Forecasting
## Problem Statement
The number of sunspots on the Sun's surface varies annually, and the sun is most active during sunspot maximums. These maximums result in increased energy and radiation impacting Earth's environment, potentially causing disruptions to radio transmissions, power grids, and other technologies. Forecasting sunspot activity is crucial for managing these effects.

Using the monthly average sunspot data from 1749 to 2010, this project aims to build a model to forecast the monthly average sunspot count for the period from 2011 to 2020.

## Dataset
### Files
train.csv: This dataset contains monthly sunspot data from 1749 to 2010. It has two columns:
* Month: The date of the sunspot count in the format "MM-DD-YYYY".
* Avg_sunspot_count: The average monthly sunspot count.

test.csv: This file contains the months for the prediction period (from 2011 to 2020). The task is to predict the corresponding sunspot counts for these months.

sample_submission.csv: A sample file showing the required format for submission. It contains:
* Month: The date in "MM-DD-YYYY".
* Avg_sunspot_count: The predicted average sunspot count (example values provided).

Sun_Spot_Counting_Forecasting.csv: A python file created using a LightGBM model containing predictions for the train dataset.

## Features in the Dataset
Month: The month and year for which the average sunspot count is recorded or predicted.
Avg_sunspot_count: The average number of sunspots observed during the month (target variable).

## Requirements
Python 3.x
Libraries used:
pandas
numpy
scikit-learn
LightGBM (for model building)
matplotlib (for visualization)

## How to Run the Code
Clone this repository.

Install the required libraries by running:

bash
Copy code
pip install -r requirements.txt
Place the dataset files (train.csv, test.csv, sample_submission.csv, and lgbm_sunspot_forecast_submission-4669.csv) in the appropriate folder.

Use the provided code in a Jupyter Notebook or Python script to load, preprocess, and train the model on the train.csv data.

Predict the Avg_sunspot_count for the years 2011-2020 using the test.csv data.

Generate your submission in the format shown in sample_submission.csv.

## Model Overview
The model used for forecasting the sunspot count is based on the LightGBM algorithm, which is a gradient boosting framework. The following steps were performed:

Data Preprocessing: The dates were parsed and converted into suitable time-series formats, with potential feature engineering to extract month and year.
Model Training: The LightGBM model was trained using historical sunspot data from 1749 to 2010.
Prediction: The model was used to predict the average monthly sunspot count for the years 2011-2020.
Submission: The results were formatted according to the submission file format and evaluated against the actual sunspot counts.

## How to Generate Predictions
Load the train.csv file and preprocess the data.
Train the LightGBM model on the processed data.
Predict the Avg_sunspot_count for the months in test.csv.
Save the results in a CSV file similar to sample_submission.csv.

## Conclusion
This project demonstrates a time-series forecasting problem where historical sunspot data is used to predict future sunspot activity. By accurately predicting sunspot counts, we can prepare for potential disruptions caused by solar activity.