# Prediction-of-an-individual-income-of-a-cencus-tract
This repository will predict the individual income of a census tract based on the household income and incarceration rate

# Background Information
From my first mini project, I explored the relationship between parents' income and the incarceration rate in Baltimore, MD and Washington, DC. And based on my analysis, it was true that lower income parents (childrens' financial circumstance) lead to a higher incarceration rate of their children in both areas. Now, I wanted to explore how the high incarceration rate and the low household income (also represents children's financial circumstance along with parents income) together would affect the children's future individual income specifically in Washington, DC (Baltimore, MD had a small number of data). Like cycle of poverty, if it is true that one ends up earning a lower income after jail, one would have a higher possibiilty of raising their children under lower household income, then this would again lead to higher chance for one's future children to be incarcerated. Not only exploring the relationship among the incarceration rate, individual income, and household income, I wanted to see if both incarceration rate and household income are significant enough for predicting the individual income in each census tract and to see whether the linear relationships are postiive or negative: Do high incarceration rate and low household income lead to low individual income in Washington, DC?

# Business Question
Can we predict individual income in Washington, DC (using census tracts) based on one's incarceration rate and household income?

# Original Data
[Individual income in Washington, DC] https://github.com/michellesykim/Prediction-of-an-individual-income-of-a-cencus-tract/blob/master/DC-indiv%20income.csv

[Incarceration rate in Washington, DC] https://github.com/michellesykim/Prediction-of-an-individual-income-of-a-cencus-tract/commit/33f4ad7eccd3a02c1db6ff70b029b2f6175a131f

[Household income in Washington, DC] https://github.com/michellesykim/Prediction-of-an-individual-income-of-a-cencus-tract/blob/master/DC-Household%20income.csv

# Analysis
![alt text](https://github.com/michellesykim/Prediction-of-an-individual-income-of-a-cencus-tract/blob/master/Screen%20Shot%202020-09-30%20at%209.35.50%20PM.png)

R^2 value tells us how well the linear regression line predicts the outcome data. Here, the R^2 value is approximately 0.94, which means 94% of the individual income data (dependent variable) in Washington, DC can be explained by the incarceration rate and household income (independent variables of the linear regression line).

Next, standard error measures the spread of the data around the linear regression line. Here, the standard error value is about 1716.58, which means approximately 68% of the predictions for individual income (independent variable) are accurate within one standard error ($1,716.58) and 95% of the individual income prediction is accurate within two standard errors ($3,433.16).

![alt text](https://github.com/michellesykim/Prediction-of-an-individual-income-of-a-cencus-tract/blob/master/Screen%20Shot%202020-09-30%20at%209.55.24%20PM.png)

Coefficients (least squares estimates) give the best fitting estimate of the multiple regression line. Here, the the multiple regression line is **Individual income = 12,507.04 - 22,326.22*Incarceration rate + 0.467*Household income.** Generally, according to the data, the incarceration data usually ranges from 0 to 0.1078, thus it makes more sense to have an increase of 0.001 or so, then if there is an increase of 0.001, the individual income will decrease by $223.3. Also, when there is an increase of $1,000 in household income, the individual income would increase by $467. And the coefficient of the intercept (12,507.04) is theoratically the expected mean value of individual income when all the dependent variables are zero. Thus, in total, if the incarceration rate increased by 0.001% and the household income increased by $1000, this will result an individual income of $12,750.74.

P-value is the probability that the null hypothesis is true, and it helps you to whether your independent variables are significant in predicting the dependent variable. If p-values is less than 0.05, it is considered to be significant in predicting the y-value. Here, both incarceration rate and household income have a p-values lower than 0.05. Thus, both independent variables are significant in predicting the individual income but especially, household income has a lower p-value so it is more significant in predicting the outcome.


Significance F value indicates the probability that none of the independent variables matter. Thus, here, F value of 1.1777E-109 means there’s almost no case where household income and incarceration rate (independent variables) are not important for predicting the individual income.

![alt text](https://github.com/michellesykim/Prediction-of-an-individual-income-of-a-cencus-tract/blob/master/Screen%20Shot%202020-09-30%20at%2010.00.06%20PM.png)

Correlation (unit-free measure) between two variables is the strength of the linear relationship between dependent variable one and two. Here, the correlation between the individual income and the household income is 0.97, which shows a strong positive linear relationship. Also, the correlation between the individual income and incarceration rate is -0.76 which also shows a negative linear relationship between the two variables. Looking at the absolute values of the two correlations, individual income has a stronger linear relationship with household income. 






