# IITI-SOC-22
Problem Statement: Supply Chain Forecasting<br />

Technical Report
Supply Chain Forecasting



Summary:

Techstacks - language used: Python
Pandas and Matplotlib: DataCleaning, Exploratory Data Analysis 
Sklearn, DecisionTreeRegressor:  for forecasting 
PowerBI: Dashboarding

We took sales data from Kaggle and analyzed it using matplotlib graphs. Our approach for forecasting was to see the Trend in the graph and then detrend it, which gave us the data containing seasonality and other residuals. For seasonality, we used feature engineering and extracted features that can cover weekly, monthly, and annual and used Decision Tree Regression to predict the sales. 

Dashboarding- 
Used PowerBI for dashboarding, which included YearWise Sales. You have an option to check sales of every store, which will provide us the store number who is performing the best and the worst. There is a bar chart to show sales in different months to give an idea about seasonality. The whole dashboard is very interactive. A simple line chart to give you an idea about the trend of the total sales.
It contains two pages, other page will consist of the forecasted data in the form of graphs and some insights regarding the data.





The dashboard created, we can easily navigate through the years, months, stores and items and can have a quick overview of the sales and its distribution.



Overall Flow(with Technical details):

Data Cleaning- Used pandas to delete some unwanted rows and created a date/Time index with intervals of 1 day.
Data consisted of a store and item feature. We started with extracting the data of a particular store and item and then forecasted the sales for that particular item of a particular store.
Trend Determination- After looking at the regular line graph of different stores and items, we found out that there is almost a linear trend. Then, using DeterministicProcess, we created trend features and generated a prediction using linear Regression based on order 1 trend and then detrended the data, which gave us the residuals.




Seasonality: Residual consisted of Seasonal and cyclic patterns. We decided to predict seasonal patterns and leave cyclic patterns as they were not very dominant.
For that, we made some extra features of Month Number(Year seasonality), Day of the week(Weekly Seasonality), and Week of a year. For predicting seasonality, we used DecissionTree Regression which used our created feature and gave us a good prediction of seasonality. Then we added the trend prediction and the prediction from DecissionTree Regression to get the final prediction.




