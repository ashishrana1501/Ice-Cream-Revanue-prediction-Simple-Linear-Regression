# Ice-Cream-Revanue-prediction-Simple-Linear-Regression
This notebook contain Prediction of Revenue of Ice-cream using Linear Regression and Decision Tree Regression Algorithm. 
- **Algorithms Used**
- **1} Linear Regression**
- **2} Decision Tree Regression**
 
- The Dataset Contain 2 variable Tempreture which is a independent Variable and Revanue as dependent Variable.
- Independent variable(Temperature) is of float data type where as dependent variable(Revenue) are of integer data type.
- The Dataset consist of 499 observation and there are no missing value present in this perticular dataset.

- **The Correlation matrix using heatmap**
 ![image](https://user-images.githubusercontent.com/86904142/169841414-1560c023-4097-417c-8c79-4445b8435173.png)

- **Checking Assumption of Linear Regression**
- **1} Linearity**
- Linear regression needs the relationship between the independent and dependent variables to be linear. Let's use a pair plot to check the relation of independent variables with the Sales variable
 ![image](https://user-images.githubusercontent.com/86904142/169842009-878caafa-89f5-462e-97ba-4bff2c447150.png)
- From Scatter Plot We can observe that there is a positive linear correlation between Temperature and Revenue.

- **regression line**
 ![image](https://user-images.githubusercontent.com/86904142/169842400-39abe8b3-aafe-411f-9145-86551633ae49.png)
- **Actual and Predicted Value**
 ![image](https://user-images.githubusercontent.com/86904142/169842508-a6e7f947-fca8-414f-b429-67c5e3bd53ec.png)
- **Normality Condition**
- **Residuals:-** Residuals as we know are the differences between the true value and the predicted value. One of the assumptions of linear regression is that the mean of the residuals should be zero. So let's find out.
- **Mean of Residuals =** 3.929301328753354e-14
- **The mean of the residuals is so small that we can consider it zero.**
- **Check for Homoscedasticity :-** Homoscedasticity means that the residuals have equal or almost equal variance across the regression line. By plotting the error terms with predicted terms we can check that there should not be any pattern in the error terms.
 ![image](https://user-images.githubusercontent.com/86904142/169843207-6e7c59d4-45ba-4fab-804e-ce9b22793183.png)
- From the scatter plot it is clear that there is no specific patters forming. So we can say homoscedasticity is present.
- **Goldfeld Quandt Test**

- **Checking heteroscedasticity : Using Goldfeld Quandt we test for heteroscedasticity.**

 - **Null Hypothesis:** Error terms are homoscedastic

 - **Alternative Hypothesis:** Error terms are heteroscedastic.
 - [('F statistic', 1.194064380988825), ('p-value', 0.10590221974044298)]
 - Since p value is greater than 0.05 in Goldfeld Quandt Test. Therefore, we do not reject Null hypothesis. Hnece, we Conclude that error terms are homoscedastic.
 - **No autocorrelation of residuals**
 - When the residuals are autocorrelated, it means that the current value is dependent of the previous (historic) values and that there is a definite unexplained pattern in the Y variable that shows up in the error terms. Though it is more evident in time series data.

- In plain terms autocorrelation takes place when there's a pattern in the rows of the data. This is usual in time series data as there is a pattern of time for eg. Week of the day effect which is a very famous pattern seen in stock markets where people tend to buy stocks more towards the beginning of weekends and tend to sell more on Mondays. There's been great study about this phenomenon and it is still a matter of research as to what actual factors cause this trend.

- There should not be autocorrelation in the data so the error terms should not form any pattern.
 ![image](https://user-images.githubusercontent.com/86904142/169843643-15a213b0-958a-460f-92ca-fa8cc08f5690.png)

- **Checking for autocorrelation To ensure the absence of autocorrelation we use Ljungbox test.**

 - **Null Hypothesis:** Autocorrelation is absent.

- **Alternative Hypothesis:** Autocorrelation is present.
- **Since p value(0.19018819503193227) is greater than 0.05 we do not reject the null hypothesis that error terms are not autocorrelated.**

- **No perfect multicollinearity:-** In regression, multicollinearity refers to the extent to which independent variables are correlated. Multicollinearity affects the coefficients and p-values, but it does not influence the predictions, precision of the predictions, and the goodness-of-fit statistics. If your primary goal is to make predictions, and you don’t need to understand the role of each independent variable, you don’t need to reduce severe multicollinearity.
 ![image](https://user-images.githubusercontent.com/86904142/169844047-7ede48c0-7b41-4b45-99d2-c3e264534c7d.png)
- **R-Square:** 0.9837324255882576
- **Mean Absolute Error:** 18.303213530102894
- **Mean Square Error:** 528.2150684519343
- **Root Mean Square Error:** 22.98292993619252
- **Mean Absolute Percenatge Error:** 0.07437058453356943

- **Decision Tree Algorithm**
- **Mean Absolute Error:** 18.303213530102894
- **Mean Square Error:** 528.2150684519343
- **Root Mean Square Error:** 22.98292993619252
- **Mean Absolute Percenatge Error:** 0.07437058453356943
