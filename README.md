# Big-Mart-Sales-Prediction

# Problem Statement
The data scientists at BigMart have collected 2013 sales data for 1559 products across 10 stores in different cities. Also, certain attributes of each product and store have been defined.

The aim is to build a predictive model and find out the sales of each product at a particular store. Using this model, BigMart will try to understand the properties of products and stores which play a key role in increasing sales.

Please note that the data may have missing values as some stores might not report all the data due to technical glitches. Hence, it will be required to treat them accordingly.

# My Performance - 300 rank out of 36657 participants. (As of 12.07.20)
# The lowest rmse was 1128.19, my model's rmse was 1148.30.

https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/#LeaderBoard


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


# Aproach to our Problem:
1) Check for missing data and the data types - categorical or numerical -  present in the dataset 
2) Check the normality of the data. For multiple linear regression, one of the assumptions is that the Actual values should be normal.
3) We analyse the data through boxplots, scatter plots to see the descriptive analysis. These probes could tell us whether some columns/feature are     having an effect on the output variables or not. We can use them feature selection.
4) Treating the missing data. 
5) Multivariate Analysis and then Feature Extraction.
6) OLS models have to be built for checking multi-collinearity, heteroskedaticity and other important assumptions for building a succesful multiple linear regression.
7) Prediction using various Regression Algorithms. The most important aspects are the prediction score and the rmse error.

# Observations:
**Algorithm,	RMSE Error
1)Polynomial Regression -	Very High Error**

**2)Linear Regression -	1155.952**

**3)Random Forest -	1150**

**4)XGBoost	- 1152.94**

**5)Gradient Boosting -	1155**

**6)SVM	- 1167**

**7)Linear SVM -	1167.27**

**8)NuSVM	- 1164**

**9)Ada Boost	- 1157**

**10)KNN	- 1154**

**11)Bagging Regressor -	1157**

**12)Lasso Lars IC	- 1180**

Final Obseravtions: 
1) The model was transformed before training and testing. When the input was transformed for non-linearity as well, so that gave us our best result.

2) Boxplots and groupby functions were used to decide on the significant variables for categorical variables
   While heatmaps, scatterplots were used for deciding on numerical variables.

2) When more features are introduced through feature extraction and feature transformation, accuracy increases but rmse error increases or doesnt get affected.

3) Item_MRP and Item_Outlet_Type are our most significant features.

4) Rmse gets affected due to high multicolinearity amonsgt varibles. But if those variables are dropped which show high multicollinearity, the accuracy is compromised.

5) Outlier removal didn't help with the model because they reduce the variance, and then the model underperformed.

6) It seems that the highest accuarcy possible is 68-69%. Any removal of insignificant variable results the model being underfit.

7) The model where all the varibles were taken into account, the results were overall better.

8) Ensemble Methods performed the best. Random Forest Regressor gave us the best model - with or without the insignificant features.


# Conclusion:
Random Forest performed the best with the lowest RMSE of 1148-1150.
A random forest is a meta estimator that fits a number of decision trees on various sub-samples of the dataset and uses averaging to improve the predictive accuracy and control over-fitting. It is a voting type algorithm, that builds multiple trees from the same dataset, and uses voting to decide on the best output on adequate variance and bias from those multiple models. It is a bootstrap model

# Interesting findings:
1) Supermarket Type 1 had the most sales because it sold the most variety in every Item_Type. 


