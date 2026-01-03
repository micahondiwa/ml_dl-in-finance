# Value at Risk Backtesting

Implements methods to VaR backtesting including:

- Likelihood ratio framework of Christoffersen (1998)
- Dynamic Quantile Test of Engle and Manganelli (2004)
  
Inputs:
- actual, an array of actual returns
- forecast, an array of VaR forecasts
- alpha, the confidence level for which we have calculated our VaR forecasts

#### More about Christoffersen (1998) Likelihood Ratio Test
- Checks the assumption of unconditional coverage and independence

1. The unconditional coverage hypothesis is that the probability of VaR is in fact ```1-alpha```. where alpha is the confidence level for which we have estimated the VaR. If the actual exceedance rate is higher or lower than ```1-alpha```, then the model underestimates or overestimates the true level of risk. 

2. The independence hypothesis asserts that VaR exceedances must be distributed independently. Whether an exceedance occurred on day t should not provide any information about whether an exceedance occurs on day t+1. There should be no "clusteriing" of exceedances (even if the overall number or rate of exceedances still approximates the expected ```1-alpha```).

### More about - Dynamic Quantile Test of Engle and Manganelli (2004)

- Also tests for independence but using a different approach: 
First, they fit a linear regression equation model to the historical exceedance. If the null hypothesis that all the coefficients in the linear regression equation are in fact zero us not rejected using a chi-square test, then newer exceedances are indeed independent of the previous ones. 
