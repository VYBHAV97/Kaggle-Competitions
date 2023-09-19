# Predict CO2 Emissions in Rwanda

The objective of this challenge is to create machine learning models that use open-source emissions data (from Sentinel-5P satellite observations) to predict carbon emissions.

Approximately 497 unique locations were selected from multiple areas in Rwanda, with a distribution around farm lands, cities and power plants. The data for this is split by time; the years 2019 - 2021 are included in the training data, and the task is to predict the CO2 emissions data for 2022 through November.

## Table of Contents
- [Features](#features)
- [Dataset](#dataset)
- [Model Training](#model-training)
- [Results](#results)
 
## Features
Seven main features were extracted weekly from Sentinel-5P from January 2019 to November 2022. Each feature (Sulphur Dioxide, Carbon Monoxide, etc) contain sub features such as column_number_density which is the vertical column density at ground level, calculated using the DOAS technique. You can read more about each feature in the below links, including how they are measured and variable definitions. You are given the values of these features in the test set and your goal to predict CO2 emissions using time information as well as these features.

Sulphur Dioxide - https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S5P_NRTI_L3_SO2?hl=en
Carbon Monoxide - https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S5P_NRTI_L3_CO?hl=en
Nitrogen Dioxide - https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S5P_NRTI_L3_NO2?hl=en
Formaldehyde - https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S5P_NRTI_L3_HCHO?hl=en
UV Aerosol Index - https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S5P_NRTI_L3_AER_AI?hl=en
Ozone - https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S5P_NRTI_L3_O3?hl=en
Cloud - https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S5P_OFFL_L3_CLOUD?hl=en

## Dataset

The dataset used for training the machine learning model is sourced from https://www.kaggle.com/competitions/playground-series-s3e20/data. 

## Model Training

The machine learning model is trained using a supervised learning algorithm, such random forest, to predict the CO2 emission based on the input features. The dataset is split into training and testing sets to evaluate the model's performance.

## Results

The trained model achieved a RMSE of 22.4 in predicting CO2 emission. Improved the RMSE score by using Stacked Ensemble Learning technique with RMSE of 9.2 on train data.








