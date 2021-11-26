# Ames_House_Price_Prediction_Using_Model_Pipelines

The goal of this project was to predict the price of a home in Ames, Iowa, based on certain characteristics of the building. This was carried out using basic algorithms such as Linear Regression and Random Forest. This problem is a regression problem.

# About the data
The dataset, downloaded from [Kaggle](https://www.kaggle.com/c/house-prices-advanced-regression-techniques), contained information on 2919 houses in Ames. This was divided into train set [1460 rows, 81 columns] and test set [1459 rows, 80 columns], consisting of 36 numeric variables, 44 categorical variables and a numeric label (present in the train set). The features centred around location of the building, characteristics of the building itself, year of construction or renovation.

## Exploratory Analysis
This is a continuation of an earlier project, where exploratory data analysis was conducted and can be found [here](https://github.com/adeyinkaoresanya/Ames-House_Price-Regression-Model/blob/main/Ames_HousePrice_prediction_EDA_FeatureEngineering.ipynb)

## Building Pipelines for Preprocessing and Modelling

Due to the fact that the dataset contained a lot of missing values and categorical variables, custom transformers  were built and integrated with existing Scikit-Learn pipeline for building the models. These transformer classes were built on top of Scikit-Learn base classes, BaseEstimator and TransformerMixin.

## Model Evaluation

XGBRegressor took a longer time to train than GradientBoostingRegressor due to the number of estimators, however, the inference time is 31% faster than GradientBoostingRegressor with a better RMSE score. 

![alt text](https://github.com/adeyinkaoresanya/Ames_House_Price_Prediction_Using_Model_Pipelines/blob/main/Images/Pipe_models_table.PNG "models table")


On the contrary, MLPRegressor model performed poorly than the other two, with a RMSE score of 1.780.


![alt text](https://github.com/adeyinkaoresanya/Ames_House_Price_Prediction_Using_Model_Pipelines/blob/main/Images/pipe_MLP_table.PNG "models table2")

## Conclusion
The model built with XGBoost met the requirement of the project and a leaderboard score of 0.128 was achieved.
