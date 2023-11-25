# AdvancedRegressionAssignment
Housing Prices Prediction Assignment
> #### Problem Statement:
A US-based housing company named Surprise Housing has decided to enter the Australian market. The company uses data analytics to purchase houses at a price below their actual values and flip them on at a higher price. For the same purpose, the company has collected a data set from the sale of houses in Australia. The data is provided in the CSV file.

The company is looking at prospective properties to buy to enter the market. We are required to build a regression model using regularisation in order to predict the actual value of the prospective properties and decide whether to invest in them or not.


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
<!--* [Acknowledgements](#acknowledgements)-->

<!-- You can include any other section that is pertinent to your problem -->

## General Information
**The company wants to know:**
- Which variables are significant in predicting the price of a house, and
- How well those variables describe the price of a house.
- Also, determine the optimal value of lambda for ridge and lasso regression

**Our objecties:**
- We are required to model the price of houses with the available independent variables. This model will then be used by the management to understand how exactly the prices vary with the variables. They can accordingly manipulate the strategy of the firm and concentrate on areas that will yield high returns. Further, the model will be a good way for management to understand the pricing dynamics of a new market.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions

**Final Observations from our model:**
1. We have imported the data and had a quick look at the data
2. Few predictor variables have missing values, they are identified and handled appropriately.
3. Data cleaning is performed to drop unnecessary columns, to convert columns to correct data types and to detect the outliers and handle them appropriately.
4. We have visually inspected the data by splitting it into categorical and numeric variables to get more insights / to identify visible patterns in the data
5. We did data pre-processing such as splitting the data into train and test data sets, encoding categorical variables and to perform scaling on numerical features to get stable & uniform coefficients
6. As part of model building, we first built the model using plain linear regression and then applied regularization using Ridge and Lasso to avoid overfitting of the data
    - Used cross validation to identify the optimal value of alpha for which Ridge / Lasso regularization gives best results.
    - Optimal value of alpha turned out to be `6` and `0.0004` for Ridge and Lasso respectively.
    - Lasso model gave slightly better test results and it also have used less number of predictor variables.
    - So we decided to pick the Lasso as final model.
7. Then we validated the basic assumptions of linear regression and evaluated our final model on the test data.
8. We got train r2 score of 0.865 and test r2 score of 0.873 using our final model
9. **Top 5 significant predictor variables as per our final model are `GrLivArea`, `OverallQual`,`TotalBsmtSF`,`GarageCars` and `OverallCond`**

## Technologies Used
- Pandas
- Matplotlib
- Seaborn
- sklearn

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

<!--
## Acknowledgements
Give credit here.
- This project was inspired by...
- References if any...
- This project was based on [this tutorial](https://www.example.com).
-->

## Contact
Created by [@naga-shanmukha]
