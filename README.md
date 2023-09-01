# Endogeneity and Instrumental Variables

Endogeneity is a concept primarily used in the field of econometrics, which is a branch of economics that focuses on statistical methods to analyze and test economic theories. 

Endogeneity refers to a situation in which a variable is influenced by other variables within a system, making it difficult to determine the true cause-and-effect relationship between the variables. In other words, endogeneity occurs when the value of a variable is not determined solely by its own characteristics but is also affected by the values of other variables in the system.

Endogeneity can pose a challenge in statistical analysis and research, especially when trying to establish causal relationships between variables. If endogeneity is not properly accounted for, it can lead to biased or incorrect estimates of the relationships between variables.

### Instrumental variables

Instrumental variables (IVs) are used to address the issue of endogeneity in regression analysis. Endogeneity refers to the situation where there is a correlation between the independent variable(s) and the error term in a regression model, leading to biased and inconsistent parameter estimates. Instrumental variables provide a solution to this problem by introducing external variables, the instruments, that are correlated with the endogenous variables but are not directly related to the dependent variable.

Here's a step-by-step explanation of how instrumental variables work to address endogeneity:

1. **Identify the Endogenous Variable**: First, identify the variable(s) in your regression model that might be endogenous. These are the variables that are potentially affected by the error term and therefore violate the assumption of exogeneity.
2. **Identify the Instrument(s)**: Find one or more instrumental variables that are correlated with the endogenous variable of interest but are not directly related to the dependent variable. The instruments should meet the relevance criterion, which means they need to have a statistically significant relationship with the endogenous variable.
3. **Test for Exogeneity**: Make sure that the instrumental variables satisfy the exogeneity criterion, meaning they should not be correlated with the error term in the regression equation. This can sometimes be challenging to confirm, but it's a crucial assumption for valid instrumental variables.
4. **Estimation**: Run a two-stage least squares (2SLS) regression analysis. In the first stage, regress the endogenous variable(s) on the instrumental variable(s) to obtain predicted values for the endogenous variable(s). These predicted values are essentially the part of the endogenous variable that is unrelated to the error term. In the second stage, regress the dependent variable on the predicted values from the first stage (which are the "cleaned" endogenous variables) along with any other relevant control variables.
5. **Interpretation**: The coefficient estimate for the cleaned endogenous variable(s) from the second-stage regression provides an estimate of the causal relationship between the endogenous variable(s) and the dependent variable, without the bias introduced by endogeneity.

while estimating coefficients , we need causality estimations rather than correlation estimates. That is one of the main reasons why we do two step regression rather than OLS.

### Hausman test

The Hausman test can also be used to test for endogeneity in econometric models. Endogeneity refers to a situation where one or more of the independent variables in a regression model are correlated with the error term, leading to biased and inconsistent parameter estimates.

Here's how the Hausman test can be used to test for endogeneity:

1. **Run the OLS Regression:** Estimate the model using ordinary least squares, obtaining the OLS coefficient estimates.
2. **Run the IV Regression:** Estimate the same model using instrumental variables. This method aims to eliminate the endogeneity bias. Instrumental variables are chosen so that they are correlated with the endogenous variable but are not correlated with the error term.
3. **Calculate the Difference:** Calculate the difference between the OLS coefficient estimates and the IV coefficient estimates for each independent variable.
4. **Calculate the Covariance Matrix:** Calculate the covariance matrix of the differences in coefficient estimates.
5. **Perform the Hausman Test:** Perform a chi-squared test on the differences in coefficient estimates using the covariance matrix. The test statistic follows a chi-squared distribution with degrees of freedom equal to the number of endogenous variables.

**If the p-value from the chi-squared test is small (typically below a chosen significance level like 0.05), it suggests that the null hypothesis of no systematic difference between the OLS and IV coefficient estimates should be rejected. In this case, there is evidence of endogeneity, indicating that the OLS estimates are biased and inconsistent.**

**If the p-value is high, it suggests that there is not enough evidence to reject the null hypothesis, indicating that the OLS estimates may be consistent and unbiased, and endogeneity might not be a major concern.**


![Logo](![image](https://github.com/Anshumaan031/endogeneity-for-econometrics-/assets/67821036/cbb5a3c6-59dc-4fda-93be-2e46fd2a3f2a)
)



## Documentations

[Endogeneity](https://www.sciencedirect.com/topics/psychology/endogeneity) 

[Python](https://www.python.org/doc/)

[statsmodels](https://www.statsmodels.org/stable/index.html)

[linearmodels](https://bashtage.github.io/linearmodels/)

## Authors

- [@Anshumaan - <anshuphukan031@gmail.com>](https://github.com/Anshumaan031)
