# Zillow's Home Value Prediction (Zestimate) #
This repository hosts code for my entry to [Zillow's Home Value Prediction competition](https://www.kaggle.com/c/zillow-prize-1). 

## Description ##
In this competition, participants develop algorithms that make indirect predictions about the future sale prices of homes. Training data includes a list of real estate properties with their characteristics (square footage, number of bedrooms, etc.), as well as their sale transactions. The predictive target is log error, defined as logerror=log(Zestimate)−log(SalePrice), which is recorded in the transactions training data. However, the training data does not include Zestimates or sale prices. 

I constructed basic features (physically nearest neighbors house values, tax-related information) before fitting CatBoost regression models. I also fit LightGBM regression models but generally their performances are worse than CatBoost. Cross-validation was used to pick the hyperparameters. 

## Requirements ##
`Python` 3, `CatBoost`. 