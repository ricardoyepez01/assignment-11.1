# Project Documentation

## Introduction

This is a Practical Application Assignment for the Professional Certification in Machine Learning and Artificial Intelligence program at UC Berkeley Executive Education

A dataset from kaggle was used. The original dataset contained information on 3 million used cars sales but for this purpose the dataset was limited to the information on 426K cars to ensure speed of processing.

## Objective

The goal is to understand what factors make a car more or less expensive. As a result of the analysis, clear recommendations should be provided to the client ( a used car dealership ) as to what consumers value in a used car.

## Procedure

The CRISP-DM model was thoroughly followed:

1. Business Understanding

* The objective is to identify how the different features of a used car ( independent variables ) affect the price ( dependent variable )
* Since the dependent variable is continuous, meaning the price value can be any number, this is considered a Regression analysis
* Also, given there is a specific well-known dependent variable, this is will be a Supervised learning process
* Lastly, as the ultimate goal is to maximize the price, this ML exercise is Exploitative in nature

2. Data Understanding

* Every feature (column) in the dataset was carefully evaluated for adequacy and correctness
* Identified categorical and numerical features
* Features were deemed necessary, appropriate, insufficient, inadequate or irrelevant
* Selected a subset of features for use in modeling
 
3. Data Preparation

* Removed unselected features
* Converted and aggregated some features
* Removed incomplete indexes for features deemed critical
* Filled in missing data for other features
* Transformed data accordingly using:
  * Logarithm Base 10
  * CardinalEncoding
  * OneHotEncoding
  * Scaling

4. Modeling

* The following models were used:
  * Linear Regression
  * Ridge Regression
  * Lasso Regression
* Created Pipelines to include Polynomial Feature Engineering preprocessing
* Performed Grid Search for hyperparameter tuning
* Performed Permutation Feature Importance with each model
* Performed Recursive Feature Elimination and Sequential Feature Selection for Linear and Ridge Regression

5. Evaluation

* Model performance was evaluated and compared between modules using:
  * R2 score
  * Root Mean Square Error
  * Mean Absolute Error
* Identified best performing model with the corresponding hyperparameters
* Reviewed findings from best model to elaborate final business recommendations

6. Deployment

* Included customer report with a brief explanation of the process and findings
* Provided recommendations base on those findings

## Conclusions

The following is a brief report shared with the customer:

  ### Overview
  
  The intent of this project is to analyze data from past sales of used cars in order to identify the different characteristics in a vehicle that influence the sale price so available and future inventory can be managed to improve sales and consequently increase revenue
  
  ### Description
  
  The sales data was procured from a well-known internet source (Kaggle) and it contains a large amount of historical transaction records with vehicle information like:
  
  * Sale Price
  * Model Year
  * Make and Model
  * Condition
  * Engine size and Fuel Type
  * Odometer
  * Status of the Title
  * Transmission
  * VIN
  * Drivetrain
  * Size
  * Type of Vehicle
  * Color
  * Registration State
  
  The available data was evaluated and processed to ensure accuracy and then analyzed through different Artificial Intelligence models that can identify the factors that influence the most the sale price.
  
  ### Conclusions
  
  After thorough simulation and careful evaluation of the modeling process, the following characteristics were deemed critical in driving the sale price:
  
  * Age
  * Odometer
  * Type
  * Condition
  
  As these findings may be expected, it is important to note that historical data analysis seems to reinforce those notions. Additionally, the following characteristics also have considerable influence, to a lesser degree:
  
  * Title
  * Fuel Type
  * Transmission
  * Brand
  
  ### Recommendations
  
  Based on these findings, the following recommendations may help improve inventory management:
  
  * Maintain an updated fleet. Although the occasional vintage or restored vehicle may generate a high revenue transaction, most higher price sales should be driven by newer vehicles
  * Low milage seems to be preferred and pay for by customers. Lease returns with limited milage by contract and second cars should be great options
  * Pickups, trucks, and sedans appear to have higher sale prices
  * As always, a vehicle in mint condition should apprise at a much higher price. Single owner or owners with no family or pets are desirable options to source these type of cars for resale
  * Additionally, characteristics like a clean Title, European brands, and Automatic transmission seem to sale at a higher price
  * Ultimately, this AI modeling process can be used to more accurately set pricing to existing car inventory based on market conditions and desired features  

  ### Considerations
  
  Despite the best effort to prepare and analyze the data within project's time frame, further work should be done to improve this process in order to gain further insight and more detailed recommendations on how to best manage vehicle inventory.
