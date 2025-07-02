# Value at Risk Backtesting

Implements methods to VaR backtesting including:

- Likelihood ratio framework of Christoffersen (1998)
- Dynamic Quantile Test of Engle and Manganelli (2004)

Input:
- actual, an array of actual returns
- forecast, an array of VaR forecasts
- alpha, the confidence level for which we have calculated our VaR forecasts

#### More about Christoffersen (1998) Likelihood Ratio Test
- Checks the assumption of unconditional coverage and independence