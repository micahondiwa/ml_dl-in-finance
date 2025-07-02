# Value at Risk Backtesting

Implements methods to VaR backtesting including:

- Likelihood ratio framework of Christofersen (1998)
- Dynamic Quantile Test of Engle and Manganelli (2004)

Input:
- actual, an array of actual returns
- forecast, an array of VaR forecasts
- alpha, the confidence level for which we have calculated our VaR forecasts
