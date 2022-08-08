Introduction
* The MechaCar prototypes were produced using multiple design specifications to identify ideal vehicle performance. Multiple metrics, such as vehicle length, vehicle weight, spoiler angle
* drive train, and ground clearance, were collected for each vehicle. Design a linear model that predicts the mpg of MechaCar prototypes using several variables from the MechaCar_mpg.csv file.
* Then interprete the multiple linear regression results. 
* Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
* Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
* Run t-tests to determine if the manufacturing lots are statistically different from the mean population
* Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you�ll write a summary 
* Interpretation of the findings.

* Deliverable 1: 
* Linear Regression to Predict MPG
* Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset? 
* On this dataset, which is predicting miles per gallons, the result shows that the probability that each variables/coefficients helps to contributes a non-random amount of variance to the
* model, the length of the vehicle traveled and the clearance would not be enough to provide a statistical result of variance needed for the model.
* Is the slope of the linear model considered to be zero? Why or why not?
* Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

Answers
Multiple linear regression is a statistical model that extends the scope and flexibility of a simple linear regression model. Instead of using a single independent variable to account for all variability observed in the dependent variable, a multiple linear regression uses multiple independent variables to account for parts of the total variance observed in the dependent variable. In actuality, a multiple linear regression is a simple linear regression in disguise—all of the assumptions, hypotheses, and outputs are the same. The only difference between multiple linear regression and simple linear regression is how we will evaluate the outputs.

From the csv dataset run to predict the linear regression of MPG, variables/coefficients like Vehicle weight, spoiler angle and AWD provide a non-random amount to the variable to predict the MPG values in the dataset therefore, the main variable that has the amount of random variance to affect the linear regression prediction of MPG are the vehicle length and ground clearance based on the result derived from the module of the dataset output. 
The slope of the linear regression model is not zero because the p-value of the dataset run is less than 0.05.
One sample t - test
data subset(suspension_Coil,) Call:
lm(formula = mpg ~ vehicle_length + vehicle_weight + spoiler_angle + 
    ground_clearance + AWD, data = MechaCar)

Coefficients:
     (Intercept)    vehicle_length    vehicle_weight     spoiler_angle  ground_clearance               AWD  
      -1.040e+02         6.267e+00         1.245e-03         6.877e-02         3.546e+00        -3.411e+00
* Deliverable 2: Summary Statistics on Suspension Coils

> summary(lm(mpg ~ vehicle_length + vehicle_weight + spoiler_angle + ground_clearance + AWD,data= MechaCar))



* No, the slope is not considered to be zero because the p-value on this data is less than 0.05. The p-value of the linear model is one of the factors that would determine the slope of the linear model

Call:
lm(formula = mpg ~ vehicle_length + vehicle_weight + spoiler_angle + 
    ground_clearance + AWD, data = MechaCar)

Residuals:
     Min       1Q   Median       3Q      Max 
-19.4701  -4.4994  -0.0692   5.4433  18.5849 
Coefficients:
                   Estimate Std. Error t value Pr(>|t|)    
(Intercept)      -1.040e+02  1.585e+01  -6.559 5.08e-08 ***
vehicle_length    6.267e+00  6.553e-01   9.563 2.60e-12 ***
vehicle_weight    1.245e-03  6.890e-04   1.807   0.0776 .  
spoiler_angle     6.877e-02  6.653e-02   1.034   0.3069    
ground_clearance  3.546e+00  5.412e-01   6.551 5.21e-08 ***
AWD              -3.411e+00  2.535e+00  -1.346   0.1852    
---
Sign if codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 8.774 on 44 degrees of freedom
Multiple R-squared:  0.7149,	Adjusted R-squared:  0.6825 
F-statistic: 22.07 on 5 and 44 DF,  p-value: 5.35e-11


* Deliverable 3: T-Test on Suspension Coils

df = 49 p-value t = -2.0916
mean of x = 1496.431, 1499.849 are sample extimates
On T-Test p-value for sample one lot 3 the P-value is 0.04168 and there is a 95 percent confidence interval. the true mean is not equal to 1500

 t.test(Suspension_Coil$PSI,mu = 1500)

	One Sample t-test

data:  Suspension_Coil$PSI
t = -1.8931, df = 149, p-value = 0.06028
alternative hypothesis: true mean is not equal to 1500
95 percent confidence interval:
 1497.507 1500.053
sample estimates:
mean of x 
  1498.78 

t.test(subset(Suspension_Coil,Manufacturing_Lot=="Lot1")$PSI,mu = 1500)

	One Sample t-test

data:  subset(Suspension_Coil, Manufacturing_Lot == "Lot1")$PSI
t = 0, df = 49, p-value = 1
alternative hypothesis: true mean is not equal to 1500
95 percent confidence interval:
 1499.719 1500.281
sample estimates:
mean of x 
     1500 


* Deliverable 4: Design a Study Comparing the MechaCar to the Competition





