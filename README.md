# Big-Mart-Sales-Prediction

# Problem Statement
The data scientists at BigMart have collected 2013 sales data for 1559 products across 10 stores in different cities. Also, certain attributes of each product and store have been defined.

The aim is to build a predictive model and find out the sales of each product at a particular store. Using this model, BigMart will try to understand the properties of products and stores which play a key role in increasing sales.

Please note that the data may have missing values as some stores might not report all the data due to technical glitches. Hence, it will be required to treat them accordingly.

# Data Description
Data We have train (8523) and test (5681) data set, train data set has both input and output variable(s). You need to predict the sales for test data set.

Variable : Description

Item_Identifier : Unique product ID

Item_Weight : Weight of product

Item_Fat_Content : Whether the product is low fat or not

Item_Visibility : The % of total display area of all products in a store allocated to the particular product

Item_Type : The category to which the product belongs

Item_MRP : Maximum Retail Price (list price) of the product

Outlet_Identifier : Unique store ID

Outlet_Establishment_Year : The year in which store was established

Outlet_Size : The size of the store in terms of ground area covered

Outlet_Location_Type : The type of city in which the store is located

Outlet_Type : Whether the outlet is just a grocery store or some sort of supermarket

Item_Outlet_Sales : Sales of the product in the particulat store. This is the outcome variable to be predicted.


# Aproach to our Problem and Observations:
1) First we check for missing data. There are missing values and some categorical variables have repeated values. So data cleaning is      required. 
2) Then we check the normality of the data. For multiple linearregression, one of the assumptions is that the Actual values should be      normal.
3) We analyse the data through boxplots, scatter plots to see the descriptive analysis. Theseprobes could tell us whether some columns/feature are having an effect on the output variables or not. We can use them feature selection.
4) We tried various methods for Feature Extraction, then selected the ones which help the model achieve an approximate bias-variance tradeoff. 
5) OLS models have to be built for checking multi-collinearity, heteroskedaticity and other important assumptions for building a succesful multiple linear regression.
6) We then train and test our models through various regression algorithms.

# Conclusion:
*The Most Significant Results* 
- **We get the an error of 1158 after using Gradient Boosting Rgegressor algorithm**
- **We get the an error of 1170 after using Random Forest Rgegressor algorithm**
- **We get the an error of 1153 after using Xtreme Gradient Boosting algorithm and Hyperparamter Tuning**
