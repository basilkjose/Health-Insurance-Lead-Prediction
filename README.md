# Health Insurance Lead Prediction

## Table of Content
* [Overview](#overview)
* [Dataset](#dataset)
* [Evaluation Metric](#evaluation_metric)
* [Feature Engineering](#feature_engineering)
* [Modeling](#modeling)
* [To Do](#to-do)

## Overview

Your Client FinMan is a financial services company that provides various financial services like loan, investment funds, insurance etc. to its customers. FinMan wishes to cross-sell health insurance to the existing customers who may or may not hold insurance policies with the company. The company recommend health insurance to it's customers based on their profile once these customers land on the website. Customers might browse the recommended health insurance policy and consequently fill up a form to apply. When these customers fill-up the form, their Response towards the policy is considered positive and they are classified as a lead.

Once these leads are acquired, the sales advisors approach them to convert and thus the company can sell proposed health insurance to these leads in a more efficient manner.Now the company needs your help in building a model to predict whether the person will be interested in their proposed Health plan/policy

## Dataset

The dataset contains following information.
   * Demographics (city, age, region etc.)
   * Information regarding holding policies of the customer
   * Recommended Policy Informatio   
    
The following are features in the dataset.
1) **ID** - Unique id.
2) **City_Code** - Code for the city of users.
3) **Region_Code** - Code for the region of the users.
4) **Accomodation_Type** - Customer owns/rents the house.
5) **Reco_Insurance_Type** - Joint or individual type for the recommended insurance.
6) **Upper_Age** - Maximium age of the customer.
7) **Lower_Age** - Minimium age of the customer.
8) **Is_Spouse** - If the customer is married or not.
9) **Health Indicator** - Encoded values for health of the customer.
10) **Holding_Policy_Duration** - Duration in year of holding policy.
11) **Holding_Policy_Type** - Type of holding policy.
12) **Reco_Policy_Cat** - Encoded values of recommended health insurance.
13) **Reco_Policy_Premium** - Annual premium(INR) for the recommended health insurance.

## Evaluation_Metric
It is a binary class classification problem.
Models are evaluated on the area under the ROC curve(**AUC VALUE**) between the predicted probability and the observed target.

## Feature_Engineering
Since most of the features are categorical we can easily derive some type of features.In categorical features we can easily derive following type of features
* **Frequency Encoding features** - Frequency Encoding for each categories in categorical features
* **Interaction Features** - Combining 2 categorical features and performing frequency encoding
* **Aggregate Features** - Grouping categorical features and applying aggregate function such as mean,std,nunique,max,min,sum..

## Modeling

We mainly used two types of boosting techniques for modeling.
* [XGBoost Classifier](https://xgboost.readthedocs.io/en/latest/python/python_api.html)
* [CatBoost Classifier](https://catboost.ai/)

## TO DO
* Done bit more feature engineering, like feature binning.
* Done more hyper parameter tuning for modeling.
