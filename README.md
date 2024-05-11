library(MASS)
library(ISLR2)
data(Boston) #importing Data
 dim(Boston)  
[1] 506 13 , 506 observations, 13lm.zn variables. #knowing how many predictors and observations Boston has.

#fitting linear regression for each predictor

1- lm.zn <- lm(crime ~ zn, data = Boston)
summary(lm.zn)
Call:
lm(formula = crim ~ zn, data = Boston)
Residuals:
 Min 1Q Median 3Q Max
-4.429 -4.222 -2.620 1.250 84.523
Coefficients:
 Estimate Std. Error t value Pr(>|t|)
(Intercept) 4.45369 0.41722 10.675 < 2e-16 ***
zn -0.07393 0.01609 -4.594 5.51e-06 ***
---
Signif. codes: 0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 8.435 on 504 degrees of freedom
Multiple R-squared: 0.04019, Adjusted R-squared: 0.03828
F-statistic: 21.1 on 1 and 504 DF, p-value: 5.506e-06
#(significant since p-value < 0.05 and R2 ≈ 4%)

2- lm.indus <- lm(crim ~ indus, data = Boston)
summary(lm.indus)
Call:
lm(formula = crim ~ indus, data = Boston)
Residuals:
 Min 1Q Median 3Q Max
-11.972 -2.698 -0.736 0.712 81.813
Coefficients:
 Estimate Std. Error t value Pr(>|t|)
(Intercept) -2.06374 0.66723 -3.093 0.00209 **
indus 0.50978 0.05102 9.991 < 2e-16 ***
---
Signif. codes: 0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 7.866 on 504 degrees of freedom
Multiple R-squared: 0.1653, Adjusted R-squared: 0.1637
F-statistic: 99.82 on 1 and 504 DF, p-value: < 2.2e-16
#(significant since p-value < 0.05 and R2 ≈ 16.5%)

3- lm.chas <- lm(crim ~ chas, data = Boston)
 summary(lm.chas)
Call:
lm(formula = crim ~ chas, data = Boston)
Residuals:
 Min 1Q Median 3Q Max
-3.738 -3.661 -3.435 0.018 85.232
Coefficients:
 Estimate Std. Error t value Pr(>|t|)
(Intercept) 3.7444 0.3961 9.453 <2e-16 ***
chas -1.8928 1.5061 -1.257 0.209
---
Signif. codes: 0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 8.597 on 504 degrees of freedom
Multiple R-squared: 0.003124, Adjusted R-squared: 0.001146
F-statistic: 1.579 on 1 and 504 DF, p-value: 0.20
#(not significant since p-value > 0.05 and R2 ≈ 0.31%)

4- > lm.nox <- lm(crim ~ nox, data = Boston)
> summary(lm.nox)
Call:
lm(formula = crim ~ nox, data = Boston)
Residuals:
 Min 1Q Median 3Q Max
-12.371 -2.738 -0.974 0.559 81.728
Coefficients:
 Estimate Std. Error t value Pr(>|t|)
(Intercept) -13.720 1.699 -8.073 5.08e-15 ***
nox 31.249 2.999 10.419 < 2e-16 ***
---
Signif. codes: 0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 7.81 on 504 degrees of freedom
Multiple R-squared: 0.1772, Adjusted R-squared: 0.1756
F-statistic: 108.6 on 1 and 504 DF, p-value: < 2.2e-16
#(significant since p-value < 0.05 and R2 ≈ 17.7%)

5- > lm.rm <- lm(crim ~ rm, data = Boston)
 > summary(lm.rm)
Call:
lm(formula = crim ~ rm, data = Boston)
Residuals:
 Min 1Q Median 3Q Max
-6.604 -3.952 -2.654 0.989 87.197
Coefficients:
 Estimate Std. Error t value Pr(>|t|)
(Intercept) 20.482 3.365 6.088 2.27e-09 ***
rm -2.684 0.532 -5.045 6.35e-07 ***
---
Signif. codes: 0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 8.401 on 504 degrees of freedom
Multiple R-squared: 0.04807, Adjusted R-squared: 0.04618
F-statistic: 25.45 on 1 and 504 DF, p-value: 6.347e-07
#(significant since p-value < 0.05 and R2 ≈ 4.8%)

6- > lm.age <- lm(crim ~ age, data = Boston)
> summary(lm.age)
Call:
lm(formula = crim ~ age, data = Boston)
Residuals:
 Min 1Q Median 3Q Max
-6.789 -4.257 -1.230 1.527 82.849
Coefficients:
 Estimate Std. Error t value Pr(>|t|)
(Intercept) -3.77791 0.94398 -4.002 7.22e-05 ***
age 0.10779 0.01274 8.463 2.85e-16 ***
---
Signif. codes: 0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 8.057 on 504 degrees of freedom
Multiple R-squared: 0.1244, Adjusted R-squared: 0.1227
F-statistic: 71.62 on 1 and 504 DF, p-value: 2.855e-16
#(significant since p-value < 0.05 and R2 ≈ 12.44%)

7- > lm.dis <- lm(crim ~ dis, data = Boston)
> summary(lm.dis)
Call:
lm(formula = crim ~ dis, data = Boston)
Residuals:
 Min 1Q Median 3Q Max
-6.708 -4.134 -1.527 1.516 81.674
Coefficients:
 Estimate Std. Error t value Pr(>|t|)
(Intercept) 9.4993 0.7304 13.006 <2e-16 ***
dis -1.5509 0.1683 -9.213 <2e-16 ***
---
Signif. codes: 0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 7.965 on 504 degrees of freedom
Multiple R-squared: 0.1441, Adjusted R-squared: 0.1425
F-statistic: 84.89 on 1 and 504 DF, p-value: < 2.2e-16
#(significant since p-value < 0.05 and R2 ≈ 14.41%)

8-> lm.rad <- lm(crim ~ rad, data = Boston)
> summary(lm.rad)
Call:
lm(formula = crim ~ rad, data = Boston)
Residuals:
 Min 1Q Median 3Q Max
-10.164 -1.381 -0.141 0.660 76.433
Coefficients:
 Estimate Std. Error t value Pr(>|t|)
(Intercept) -2.28716 0.44348 -5.157 3.61e-07 ***
rad 0.61791 0.03433 17.998 < 2e-16 ***
---
Signif. codes: 0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 6.718 on 504 degrees of freedom
Multiple R-squared: 0.3913, Adjusted R-squared: 0.39
F-statistic: 323.9 on 1 and 504 DF, p-value: < 2.2e-16
#(significant since p-value < 0.05 and R2 ≈ 39.13%)

9-> lm.tax <- lm(crim ~ tax, data = Boston)
> summary(lm.tax)
Call:
lm(formula = crim ~ tax, data = Boston)
Residuals:
 Min 1Q Median 3Q Max
-12.513 -2.738 -0.194 1.065 77.696
Coefficients:
 Estimate Std. Error t value Pr(>|t|)
(Intercept) -8.528369 0.815809 -10.45 <2e-16 ***
tax 0.029742 0.001847 16.10 <2e-16 ***
---
Signif. codes: 0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 6.997 on 504 degrees of freedom
Multiple R-squared: 0.3396, Adjusted R-squared: 0.3383
F-statistic: 259.2 on 1 and 504 DF, p-value: < 2.2e-16
#(significant since p-value < 0.05 and R2 ≈ 33.96%)

10-> lm.ptratio <- lm(crim ~ ptratio, data = Boston)
> summary(lm.ptratio)
Call:
lm(formula = crim ~ ptratio, data = Boston)
Residuals:
 Min 1Q Median 3Q Max
-7.654 -3.985 -1.912 1.825 83.353
Coefficients:
 Estimate Std. Error t value Pr(>|t|)
(Intercept) -17.6469 3.1473 -5.607 3.40e-08 ***
ptratio 1.1520 0.1694 6.801 2.94e-11 ***
---
Signif. codes: 0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 8.24 on 504 degrees of freedom
Multiple R-squared: 0.08407, Adjusted R-squared: 0.08225
F-statistic: 46.26 on 1 and 504 DF, p-value: 2.943e-11
#(significant since p-value < 0.05 and R2 ≈ 8.4%)

11- > lm.lstat <- lm(crim ~ lstat, data = Boston)
> summary(lm.lstat)
Call:
lm(formula = crim ~ lstat, data = Boston)
Residuals:
 Min 1Q Median 3Q Max
-13.925 -2.822 -0.664 1.079 82.862
Coefficients:
 Estimate Std. Error t value Pr(>|t|)
(Intercept) -3.33054 0.69376 -4.801 2.09e-06 ***
lstat 0.54880 0.04776 11.491 < 2e-16 ***
---
Signif. codes: 0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 7.664 on 504 degrees of freedom
Multiple R-squared: 0.2076, Adjusted R-squared: 0.206
F-statistic: 132 on 1 and 504 DF, p-value: < 2.2e-16
#(significant since p-value < 0.05 and R2 ≈ 20.8%)

12- > lm.medv <- lm(crim ~ medv, data = Boston)
> summary(lm.medv)
Call:
lm(formula = crim ~ medv, data = Boston)
Residuals:
 Min 1Q Median 3Q Max
-9.071 -4.022 -2.343 1.298 80.957
Coefficients:
 Estimate Std. Error t value Pr(>|t|)
(Intercept) 11.79654 0.93419 12.63 <2e-16 ***
medv -0.36316 0.03839 -9.46 <2e-16 ***
---
Signif. codes: 0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 7.934 on 504 degrees of freedom
Multiple R-squared: 0.1508, Adjusted R-squared: 0.1491
F-statistic: 89.49 on 1 and 504 DF, p-value: < 2.2e-16
#(significant since p-value < 0.05 and R2 ≈ 15.8%)

#Full predictors fit

> lm.crime <- lm(crim ~ ., data = Boston)
> summary(lm.crime)
lm(formula = crim ~ ., data = Boston)
Residuals:
 Min 1Q Median 3Q Max
-8.534 -2.248 -0.348 1.087 73.923
Coefficients:
 Estimate Std. Error t value Pr(>|t|)
(Intercept) 13.7783938 7.0818258 1.946 0.052271 .
zn 0.0457100 0.0187903 2.433 0.015344 *
indus -0.0583501 0.0836351 -0.698 0.485709
chas -0.8253776 1.1833963 -0.697 0.485841
nox -9.9575865 5.2898242 -1.882 0.060370 .
rm 0.6289107 0.6070924 1.036 0.300738
age -0.0008483 0.0179482 -0.047 0.962323
dis -1.0122467 0.2824676 -3.584 0.000373 ***
rad 0.6124653 0.0875358 6.997 8.59e-12 ***
tax -0.0037756 0.0051723 -0.730 0.465757
ptratio -0.3040728 0.1863598 -1.632 0.103393
lstat 0.1388006 0.0757213 1.833 0.067398 .
medv -0.2200564 0.0598240 -3.678 0.000261 ***
---
Signif. codes: 0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 6.46 on 493 degrees of freedom
Multiple R-squared: 0.4493, Adjusted R-squared: 0.4359
F-statistic: 33.52 on 12 and 493 DF, p-value: < 2.2e-16
#(rad, dis, medv, and zn are statistically significant their since p-value < 0.05)
#(indus, chas, nox, rm, age, tax, ptratio and lstat are not statistically significant their
since p-value > 0.05)


#evidence of quadratic association between any of the predictors and the response

- lm.zn2 <- lm(crim ~ zn + I(zn^2), data = Boston)
> summary(lm.zn2)
Call:
lm(formula = crim ~ zn + I(zn^2), data = Boston)
Residuals:
 Min 1Q Median 3Q Max
-4.760 -4.553 -1.491 0.821 84.191
Coefficients:
 Estimate Std. Error t value Pr(>|t|)
(Intercept) 4.7853138 0.4302223 11.123 < 2e-16 ***
zn -0.2159497 0.0521941 -4.137 4.12e-05 ***
I(zn^2) 0.0019080 0.0006676 2.858 0.00444 **
---
Signif. codes: 0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 8.376 on 503 degrees of freedom
Multiple R-squared: 0.05553, Adjusted R-squared: 0.05177
F-statistic: 14.79 on 2 and 503 DF, p-value: 5.757e-07
#( there is a quadradic association between the response and the predictor sin
ce p-value<0.05)

lm.indus <- lm(crim ~ indus +I(indus^2), data = Boston)
> summary(lm.indus)

Call:
lm(formula = crim ~ indus + I(indus^2), data = Boston)
Residuals:
 Min 1Q Median 3Q Max
-7.530 -3.769 -1.069 1.354 81.462
Coefficients:
 Estimate Std. Error t value Pr(>|t|)
(Intercept) -4.849269 1.109293 -4.371 1.50e-05 ***
indus 1.189715 0.223173 5.331 1.48e-07 ***
I(indus^2) -0.027993 0.008949 -3.128 0.00186 **
---
Signif. codes: 0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 7.799 on 503 degrees of freedom
Multiple R-squared: 0.1812, Adjusted R-squared: 0.178
F-statistic: 55.67 on 2 and 503 DF, p-value: < 2.2e-16

#( there is a quadradic association between the response and the predictor sin
ce p-value<0.05)

 lm.chas2 <- lm(crim ~ chas + I(chas^2), data = Boston)
> summary(lm.chas2)
Call:
lm(formula = crim ~ chas + I(chas^2), data = Boston)
Residuals:
 Min 1Q Median 3Q Max
-3.738 -3.661 -3.435 0.018 85.232
Coefficients: (1 not defined because of singularities)
 Estimate Std. Error t value Pr(>|t|)
(Intercept) 3.7444 0.3961 9.453 <2e-16 ***
chas -1.8928 1.5061 -1.257 0.209
I(chas^2) NA NA NA NA
---
Signif. codes: 0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 8.597 on 504 degrees of freedom
Multiple R-squared: 0.003124, Adjusted R-squared: 0.001146
F-statistic: 1.579 on 1 and 504 DF, p-value: 0.2094
#( there is no a quadradic association between the response and the predictor
since p-value> 0)

lm.nox2 <- lm(crim ~ nox + I(nox^2), data = Boston)
> summary(lm.nox2)
Call:
lm(formula = crim ~ nox + I(nox^2), data = Boston)
Residuals:
 Min 1Q Median 3Q Max
-7.512 -3.394 -1.467 1.444 80.946
Coefficients:
 Estimate Std. Error t value Pr(>|t|)
(Intercept) -41.325 7.572 -5.457 7.6e-08 ***
nox 127.877 26.016 4.915 1.2e-06 ***
I(nox^2) -80.958 21.655 -3.738 0.000206 ***
---
Signif. codes: 0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 7.711 on 503 degrees of freedom
Multiple R-squared: 0.1995, Adjusted R-squared: 0.1963
F-statistic: 62.66 on 2 and 503 DF, p-value: < 2.2e-16
#( there is a quadradic association between the response and the predictor sin
ce p-value<0.05)

> lm.rm2 <- lm(crim ~ rm + I(rm^2), data = Boston)
> summary(lm.rm2)
Call:
lm(formula = crim ~ rm + I(rm^2), data = Boston)
Residuals:
 Min 1Q Median 3Q Max
-15.962 -3.528 -2.142 -0.237 87.470
Coefficients:
 Estimate Std. Error t value Pr(>|t|)
(Intercept) 71.3257 16.2718 4.383 1.42e-05 ***
rm -18.7078 5.0469 -3.707 0.000233 ***
I(rm^2) 1.2468 0.3906 3.192 0.001499 **
---
Signif. codes: 0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 8.325 on 503 degrees of freedom
Multiple R-squared: 0.06697, Adjusted R-squared: 0.06326
F-statistic: 18.05 on 2 and 503 DF, p-value: 2.681e-08
#( there is a quadradic association between the response and the predictor si
nce p-value<0.05)


lm.age2 <- lm(crim ~ age + I(age^2), data = Boston)
> summary(lm.age2)
Call:
lm(formula = crim ~ age + I(age^2), data = Boston)
Residuals:
 Min 1Q Median 3Q Max
-8.650 -3.484 -0.394 0.663 82.476
Coefficients:
 Estimate Std. Error t value Pr(>|t|)
(Intercept) 3.3100066 1.7550195 1.886 0.0599 .
age -0.2012862 0.0662371 -3.039 0.0025 **
I(age^2) 0.0025680 0.0005405 4.751 2.64e-06 ***
---
Signif. codes: 0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 7.89 on 503 degrees of freedom
Multiple R-squared: 0.162, Adjusted R-squared: 0.1587
F-statistic: 48.63 on 2 and 503 DF, p-value: < 2.2e-16
#( there is a quadradic association between the response and the predictor sin
ce p-value<0.05)


 lm.dis2 <- lm(crim ~ dis + I(dis^2), data = Boston)
> summary(lm.dis2)
Call:
lm(formula = crim ~ dis + I(dis^2), data = Boston)
Residuals:
 Min 1Q Median 3Q Max
-12.896 -3.721 -0.229 1.736 78.724
Coefficients:
 Estimate Std. Error t value Pr(>|t|)
(Intercept) 17.96831 1.33179 13.492 < 2e-16 ***
dis -6.11277 0.63286 -9.659 < 2e-16 ***
I(dis^2) 0.46971 0.06305 7.450 4.09e-13 ***
---
Signif. codes: 0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 7.567 on 503 degrees of freedom
Multiple R-squared: 0.2292, Adjusted R-squared: 0.2261
F-statistic: 74.79 on 2 and 503 DF, p-value: < 2.2e-16
#( there is a quadradic association between the response and the predictor si
ce p-value<0.05)

 lm.rad2 <- lm(crim ~ rad + I(rad^2), data = Boston)
> summary(lm.rad2)

Call:
lm(formula = crim ~ rad + I(rad^2), data = Boston)
Residuals:
 Min 1Q Median 3Q Max
-10.373 -0.408 -0.243 0.039 76.224
Coefficients:
 Estimate Std. Error t value Pr(>|t|)
(Intercept) 0.57387 1.17805 0.487 0.62637
rad -0.18796 0.30959 -0.607 0.54404
I(rad^2) 0.02897 0.01106 2.619 0.00909 **
---
Signif. codes: 0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 6.679 on 503 degrees of freedom
Multiple R-squared: 0.3994, Adjusted R-squared: 0.3971
F-statistic: 167.3 on 2 and 503 DF, p-value: < 2.2e-16

#(there is a quadradic association between the response and the predictor sinc
e p-value<0.05)


lm.tax2 <- lm(crim ~ tax + I(tax^2), data = Boston)
> summary(lm.tax2)
Call:
lm(formula = crim ~ tax + I(tax^2), data = Boston)
Residuals:
 Min 1Q Median 3Q Max
-14.810 -1.085 -0.011 0.256 76.982
Coefficients:
 Estimate Std. Error t value Pr(>|t|)
(Intercept) 5.934e+00 3.192e+00 1.859 0.06361 .
tax -4.318e-02 1.569e-02 -2.753 0.00612 **
I(tax^2) 7.850e-05 1.677e-05 4.680 3.69e-06 ***
---
Signif. codes: 0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 6.856 on 503 degrees of freedom
Multiple R-squared: 0.3672, Adjusted R-squared: 0.3647
F-statistic: 145.9 on 2 and 503 DF, p-value: < 2.2e-16
#( there is a quadradic association between the response and the predictor sin
ce p-value<0.05)

lm.ptratio2 <- lm(crim ~ ptratio + I(ptratio^2), data = Boston)
> summary(lm.ptratio2)
Call:
lm(formula = crim ~ ptratio + I(ptratio^2), data = Boston)
Residuals:
 Min 1Q Median 3Q Max
-10.850 -3.204 -1.225 0.235 83.038
Coefficients:
 Estimate Std. Error t value Pr(>|t|)
(Intercept) 51.67955 23.08535 2.239 0.02562 *
ptratio -6.87098 2.65239 -2.590 0.00986 **
I(ptratio^2) 0.22805 0.07524 3.031 0.00256 **
---
Signif. codes: 0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 8.174 on 503 degrees of freedom
Multiple R-squared: 0.1005, Adjusted R-squared: 0.09692
F-statistic: 28.1 on 2 and 503 DF, p-value: 2.702e-12
#( there is a quadradic association between the response and the predictor sin
ce p-value<0.05)

lm.lstat2 <- lm(crim ~ lstat + I(lstat^2), data = Boston)
> summary(lm.lstat2)
Call:
lm(formula = crim ~ lstat + I(lstat^2), data = Boston)
Residuals:
 Min 1Q Median 3Q Max
-16.965 -2.365 -0.636 0.523 83.503
Coefficients:
 Estimate Std. Error t value Pr(>|t|)
(Intercept) -1.27531 1.20609 -1.057 0.2908
lstat 0.20674 0.17122 1.207 0.2278
I(lstat^2) 0.01077 0.00518 2.080 0.0381 *
---
Signif. codes: 0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 7.639 on 503 degrees of freedom
Multiple R-squared: 0.2143, Adjusted R-squared: 0.2112
F-statistic: 68.62 on 2 and 503 DF, p-value: < 2.2e-16
#( there is a quadradic association between the response and the predictor sin
ce p-value<0.05)


lm.medv2 <- lm(crim ~ medv + I(medv^2), data = Boston)
> summary(lm.medv2)
Call:
lm(formula = crim ~ medv + I(medv^2), data = Boston)
Residuals:
 Min 1Q Median 3Q Max
-18.802 -3.127 -0.593 2.031 75.204
Coefficients:
 Estimate Std. Error t value Pr(>|t|)
(Intercept) 31.969173 1.777610 17.98 <2e-16 ***
medv -2.071441 0.137980 -15.01 <2e-16 ***
I(medv^2) 0.030938 0.002425 12.76 <2e-16 ***
---
Signif. codes: 0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 6.903 on 503 degrees of freedom
Multiple R-squared: 0.3584, Adjusted R-squared: 0.3559
F-statistic: 140.5 on 2 and 503 DF, p-value: < 2.2e-16
#( there is a quadradic association between the response and the predictor sin
ce p-value<0.05)

#Logistic regression

a-
> crim_med = median(Boston$crim)
> Boston$crim_cat = (Boston$crim >= crim_med)
> crim_class = glm(crim_cat ~ . - crim, family = "binomial", data = Boston )
> summary(crim_class)
Call:
glm(formula = crim_cat ~ . - crim, family = "binomial", data = Boston)
Coefficients:
 Estimate Std. Error z value Pr(>|z|)
(Intercept) -38.832417 6.086280 -6.380 1.77e-10 ***
zn -0.086228 0.034090 -2.529 0.0114 *
indus -0.052438 0.042817 -1.225 0.2207
chas 0.619914 0.722150 0.858 0.3907
nox 47.913820 7.344213 6.524 6.84e-11 ***
rm -0.271941 0.676239 -0.402 0.6876
age 0.021474 0.012105 1.774 0.0761 .
dis 0.669991 0.214618 3.122 0.0018 **
rad 0.669240 0.151742 4.410 1.03e-05 ***
tax -0.006165 0.002622 -2.351 0.0187 *
ptratio 0.326433 0.116296 2.807 0.0050 **
lstat 0.053537 0.047105 1.137 0.2557
medv 0.147987 0.064347 2.300 0.0215 *
---
Signif. codes: 0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
(Dispersion parameter for binomial family taken to be 1)
 Null deviance: 701.46 on 505 degrees of freedom
Residual deviance: 218.75 on 493 degrees of freedom
AIC: 244.75
Number of Fisher Scoring iterations: 9
#bzn: The variable is statistically significant (p-value = 0.0114)
#nox: Highly significant (p-value = 6.84e-11),
#dis: Statistically significant (p-value = 0.0018)
#rad: Highly significant (p-value = 1.03e-05)
#tax: Statistically significant (p-value = 0.0187)
#ptratio: Statistically significant (p-value = 0.0050)
#medv: Statistically significant (p-value = 0.0215)
#indus, chas, rm, age, lstat: These variables are not statistically
#significant (their p-value > 0.05)
c-
> contrasts(Boston$crim_cat)
 TRUE
FALSE 0
TRUE 1
predicted_values = ifelse(predict(crim_class, type = "response")> 0.5, 1, 0)
> confusion_matrix = table(predicted_values, Boston$crim_cat)
> show(confusion_matrix)

predicted_values FALSE TRUE
 0 234 25
 1 19 228
> mean (predicted_values == Boston$crim_cat)
[1] 0.9130435
