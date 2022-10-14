# MechaCar_Statistical_Analysis

## Linear Regression to Predict MPG
The MechaCar dataset contains a sample size of 50 prototypes measuring the miles per gallon across multiple variables. The linear regression was calculated using R in RStudio.
## Linear Regression
R script was applied to the dataset on several variables to get the following coefficients.
![image](linear_regression.jpg)

## Summary of Linear Regression Model
A summary of the linear regresion, as displayed int below image, provides with the quality of the dataset.Also, in first glance it can be said that the dataset fits in the normal parameters wherien the min and max are approximately -19.47 and 18.58. Median is approximately -0.07.


![image](summary_statistics.jpg)

Coming to the delverable questions,

### Q.Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

Considering a 95% level of confidence ie p level should be alpha= 0.05 level of significance to verify statistically significance.

**Coefficients:**
**mpg: 0 < 0.05 ; Statistically significant ; non random amount of variance**

**Vehicle length: 0 < 0.05 ; Statistically significant ; non random amount of variance**

**Vehicle weight: 0.08 > 0.05 ;Not Statistically significant ; random amount of variance**

**Spoiler angle: 0.31 > 0.05 ; Not Statistically significant ; random amount of variance**

**Ground clearance : 0 > 0.05 ; Statistically significant ; non-random amount of variance**

**AWD : 0.19 > 0.05 ; NOt Statistically signficant ; random amount of variance**

To summarise, vehicle length and ground clearance variables record non-random variance as applied to mpg. 

### Q.Is the slope of the linear model considered to be zero? Why or why not?

Converting from scientific notation, all of the slopes of the variables are shown to be non-zero even though some are close to zero:
Coefficients:
vehicle length: 6.267
vehicle weight: .001
spoiler angle: .069
ground clearance: 3.546
AWD: -3.411

The multiple linear regression formula for mpg = -.01 + 6.267(vehicle length)+.001(vehicle weight)+.069(spoiler angle)+3.546(ground clearance)-3.411(AWD), which results in a non-zero slope.

### Q.Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

R-squared = 0.7149 which showcases that the dataset is an effective dataset. But R squared is not the only parameter for consideration. There may be other variables impacting to the variation in mpg.

## Summary Statistics of Suspension Coils
Below is the summary statistics of all of the manufacturing lots. The mean is 1498.78 for this sample and the population mean was determined to be 1500.

![image2](Total_summary.jpg)

Summary by Manufacturing Lot Number
The means of the lot numbers are similar to the population mean and the sample mean.

![image3](lot_summary.jpg)

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?
The variance for the total manufacturing lot is 62 < 100, which is within the expected design specifications of staying under 100 PSI. However, when reviewing the data by Lot number, Lot 3 is a large contributing factor to the variance being high. Lot 3 shows a variance of 170 > 100 and does not meet the design specifications. Lot 1 and Lot 2 have significantly lower variance, 1 and 7 respectively.

## T-Tests on Suspension Coils
T-test for all Lots
All Manufacturing Lots: p-value = .6028, alpha = .05
.60 > .05, which means the total manufacturing lot is not statistically significant from the normal distribution and normality can be assumed. The mean falls within the 95% confidence interval.

![image4](t_test_alllots.jpg)

## T-test for Lot 1
Lot 1: p-value = 1, alpha = .05
1 > .05, which means Lot 1 is not statistically significant from the normal distribution and normality can be assumed. The mean falls within the 95% confidence interval.

![image5](t_test_lot1.jpg)

## T-test for Lot 2
Lot 2: p-value = .6072, alpha = .05

0.60 > .05, which means Lot 2 is not statistically significant from the normal distribution and normality can be assumed. The mean falls within the 95% confidence interval.

![image6](t_test_lot2.jpg)

## T-test for Lot 3
Lot 3: p-value = .04168, alpha = .05
.04 < .05, which means it is statistically significant from the normal distribution and normality cannot be assumed. However, the mean falls within the 95% confidence interval.

![image7](t_test_lot3.jpg)


The overall manufacturing, Lot 1, and Lot 2 display a normal distribution. Therefore, there is not sufficient evidence to reject the null hypothesis, which shows the two means are statistically similar.


## Study Design: MechaCar vs Competition

When comparing MechaCar to its competitor’s other metrics that could be of interest to a consumer could include cost, car color, city fuel efficiency, highway fuel efficiency, horsepower, maintenance cost, or safety rating.

* What metric or metrics are you going to test?
The next metrics to test should be the safety rating, horsepower, and highway fuel efficiency, which address some safety concerns of consumers.

* What is the null hypothesis or alternative hypothesis?
The null hypothesis is that the mean of the safety rating is zero. The alternative hypothesis is that the mean of the safety rating is not zero.

* What statistical test would you use to test the hypothesis? And why?
Using a multiple linear regression statistical summary would show how the variables impact the safety ratings for MechaCar and their competitors.

* What data is needed to run the statistical test?
A random sample of n > 30 for MechaCar and their competitor, would need to be collected including the safety ratings, highway fuel efficiency, and horsepower plus running the data through RStudio.
