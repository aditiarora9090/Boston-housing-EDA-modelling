# Boston Housing - EDA and Modelling
![](https://cdn10.bostonmagazine.com/wp-content/uploads/sites/2/2022/06/housing-costs-story.jpg)
## About the dataset
The Boston Housing Dataset is a derived from information collected by the U.S. Census Service concerning housing in the area of  [Boston MA](http://www.cs.toronto.edu/~delve/data/boston/bostonDetail.html). The following describes the dataset columns:

-   CRIM - per capita crime rate by town
-   ZN - proportion of residential land zoned for lots over 25,000 sq.ft.
-   INDUS - proportion of non-retail business acres per town.
-   CHAS - Charles River dummy variable (1 if tract bounds river; 0 otherwise)
-   NOX - nitric oxides concentration (parts per 10 million)
-   RM - average number of rooms per dwelling
-   AGE - proportion of owner-occupied units built prior to 1940
-   DIS - weighted distances to five Boston employment centres
-   RAD - index of accessibility to radial highways
-   TAX - full-value property-tax rate per  $10,000
-   PTRATIO - pupil-teacher ratio by town
-   B - 1000(Bk - 0.63)^2 where Bk is the proportion of blacks by town
-   LSTAT - % lower status of the population
-   MEDV - Median value of owner-occupied homes in  $1000's


## Exploratory Data Analysis

I have done Exploratory Data Analysis on this dataset which helped me gain the following insights:
- The price (medv) of the houses is normally distributed with a few outliers.
- RM (average number of rooms per dwelling) has a strong positive correlation with MEDV(Median value of owner-occupied homes in $1000's) i.e 0.7 whereas LSTAT (% lower status of the population) has a high negative correlation with MEDV i.e -0.74.
- Prices of houses closer to charles river are found to be higher in general with higher value of 1st quartile, median and 3rd quartile. Even the minimum and maximum values are higher if the house is located in close vicinity of charles river.
- 24 is the most common index of accessibility to radial highways.
- There is a negative correlation between the percentage of low status population and the number of owner pre occupied homes.
- Maximum spread of units further away from charles river is priced between 15-25 million USD.
-There are more neighborhoods with fewer rooms per dwelling than with more rooms per dwelling.


## Modelling - Multiple Linear Regression

For the modelling part, the following steps were followed:

1. Looking at the statistics
2. Data-Preprocessing (label encoding not required as all the variables are numeric)
3. Splitting the dataset into training and testing
4. Fitting the multiple linear regression model
5. Checking the training accuracy 
6. Checking the testing accuracy
  > **Training accuracy:  67.17%**
  > **Testing Accuracy:  43.60%**

## Creating a python function

At last, I created a python function that takes these values(training row for eg.) as input and predicts a price.


