## INTRODUCTION 

## TOOL  USED 

Microsoft SQL

## THE WHOLE IDEA OF LINEAR REGRESSION
 Y = bO + b1*x
 where Y is dependent variable
       bo is intercept(value of y when x is 0)
       b1 is slope (rate of change)
       x is the independent variable 

## TASK 

### VIEWING THE DATASET

### IDENTIFYING DEPENDENT AND INDEPENDENT VARIABLE
The first thing to do in linear Regression, is to identify the independent and the dependent variable. 
in this data set, the year is the independent variable while per capita income is the dependent variable.

### CHECKING FOR CORRELATION BETWEEN THE DEPENDENT AND INDEPENDENT VARIABLE

There are two was to do this.

1) use of a sccattered plot


![Alt Text](https://github.com/Mario-Gozie/Canada-GDP-Prediction-Simple-Linear-Regression/blob/main/images/The_Scattered_Plot.png)


From this scattered plot, there is a positive correlation between year and per capita income

2) calculating the pearson correlation coefficient using the CORREL() function in excel


![Alt Text](https://github.com/Mario-Gozie/Canada-GDP-Prediction-Simple-Linear-Regression/blob/main/images/Peason_Corretion.png)


when a correlation coefficient is close +1 or -1 we say there is a strong correlation between variables where when it has a negetive sign, it shows negative correlation and when positive it shows possitive correlation.

As we can see here, the correlation coefficient of the two variables could be rounded to  0.94 which is positive and very close to one. That shows a strong correlation between Year and per capita income.

in otherwords, as the year increses, Per capita income increases.


### CALCULATING MEANS/AVERAGE

The mean year and that of per capita income was done using the average function in excel 

![Alt Text]()


### CALCULATING FOR SLOPE

This is known as the rate of change i.e it is the value of Y(dependent variable) for a single change in X(independent variable)
The slope is given by the product of (X-Xmean)(Y-Ymean)/(X-Xmean)^2

1) calculating for (X-Xmean),(Y-Ymean) and (X-Xmean)^2

![Alt Text]()

2) Applying the above formula (X-Xmean)(Y-Ymean)/(X-Xmean)^2 to get the slope

![Alt Text]()

_Alternatively the slope can be calculated using the Slope function in Exel which takes the range of the Y variable and that of the X varible and gives you the output._


![Alt Text]()


### CALCULATING INTERCEPT

Having gotten the the slopes and mean(X) and Mean(Y) I had to calculate for the intercept since it is a constant.

in making the intercept the subject of the equation, I got `b0 = Ymean - Xmean*b1`

![Alt Text]()


Alternatively, there is an intercept function that can calculate the intercept of the two variables which needs the the the dependent(Y) and independent(X) variable

![Alt Text]()

### CALCULATING FOR R^2

R^2 tells us how well a regression model can predict the dependable variable. when it is it ranges from 0 to 1 when it is close to 1, it means it is a good model and when it equals 1, it means 100% of the actual values can be explained by a model.
R^2 is calculated by dividing the squared of the distance between predicted Y variable and the mean of the Y variable by the squared of the difference between the actual Y variable and its mean.
Another way to see this is that it is the ratio of sum of squares of Regression to sum of squares of the total.

 Formula = (Ypredicted-Ymean)^2 / (Y-Ymean)^2 

1) calculating for (Ypredicted-Ymean)^2  and (Y-Ymean)^2

![Alt Text]()

2) calculating for R^2

![Alt Text]()

Interestingly, R^2 is the same as squaring the pearson correlation coefficient. which also mean that the square root of R^2 will give you the pearson correlation.


![Alt Text]()

## REGRESSION WITH EXCEL DATA ANALYSIS TOOL PACK

Earlier I said that this project will be done manually and with the data anlysis tool pack. my reason for doing it is this way is to explain the concept behind linear regression.
lets me now use the excel data analytics tool pack plug in wjhich makes these calculations easy and quick.

To use Analysis tool for Regression, you can see the data analytics tools on the right of the data section in the excel ribbon and choose Regression.


![Alt Text]()

The result from using the analytics tool has 3 main sections.

a) The Regression statistics pane,
b) The Anova Pane,
c) The Coefficient pane

I will focus on the most important values

### The Regression Statistics Pane

![Alt Text]()

* here we have the Multiple R which is the same as the Peason correlataion coefficient.
its value is 0.943883954 and that corresponds with the pearson correlation coefficient I calculated earlier manually. once again, this shows a strong relationship between X variable and Y variable.

* We have the R^2 in this pane too which is known as the coeffiecient of determination
its value is 0.890916918 and it corresponds with the R^2 I calculated earlier.

* the number of observations is 48 which is clear.

### The Anova Pane


![Alt Text]()

Looking at the sum of squares column, we have the sum of squares for Regression, sum of squares for the Residual and sum of squares for Total.
Remember that R^2 is sum of squares of the Regression divided by sum of squres for Total.  if we compute this, we will have our corresponding R^2

## The coefficient Pane 

![Alt Text]()

Here we have intercept which is the value of the dependent variable when the independent variable is 0 which is -1632210.758

There is the slope for the relationship which is 828.4650752

we also have a Pvalue which is 2.79524E-23


NB in Linear Regression Analysis, we are doing hypothesis testing. where the **Null Hypothesis** is that there is no relationship between the two variables and the **Alternate Hypothesis** is that there is a relationship. if Pvalue is less or equal than the significant value which is usually 0.05
we Reject the Null Hyposthesis** if its greater than the significant value, we **fail to Reject the Null Hypothesis.**

SUMMARY AND INSIGHT

So far after my analysis, I found the intercept correlation coefficient of the relationship between Year and per capita income to be 0.943883954 (Multiple R) and I can say thath the two variables are strongly correlated because the correlation coefficient is very close to 1.
I calculated the intercept and slope which are -1632210.758 and 828.4650752 respectively. With these two values, I developed a Regression equation for Prediction which is **Y = -1632210.758 + 828.4650752*X**. But how good will this equation be for prediction? well, to know how good, I calculated for the coefficient of determination(R^2) which gave me a value of 0.890916918.
if the value of R^2 is converted to percentage, we will have 89.09%. This simply means that the model can account for 89.09%  of the values for the Y variable while other factors can account for the variations. That I must say is a good fit because its very close to 100% so I would say I have a good model. 

 


