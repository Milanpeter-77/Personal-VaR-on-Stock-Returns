# Value at Risk (VaR) Computing on Stock Returns

This repository provides a comprehensive exploration of Value at Risk (VaR), a widely-used metric in financial risk management. The project demonstrates various methodologies for estimating VaR using Python and historical stock return data, fetched via Yahoo Finance.

## Overview

VaR quantifies the maximum potential loss of an asset, portfolio, or investment over a specific time period, given a confidence level. It helps investors and institutions assess risk exposure and implement effective risk management strategies. 

The repository covers the following VaR computation methods:
- **Historical Method**: Non-parametric, based on past returns.
- **Variance-Covariance Method**: Parametric, assumes returns follow a normal distribution.
- **Monte Carlo Simulation**: Generates synthetic return paths to simulate potential future scenarios.

## Features
- Fetches historical stock data from Yahoo Finance using `yfinance`.
- Implements VaR calculations with multiple methods.
- Visualizes stock return distributions with interactive plots.
- Compares the results across methods, discussing assumptions and differences.


## Methodology

### Data Preparation
Historical stock prices are retrieved using Yahoo Finance. The script calculates daily returns based on the closing prices.

### VaR Methods
1. **Historical Method**:
   - Orders past returns.
   - Identifies the percentile corresponding to the confidence level.
2. **Variance-Covariance Method**:
   - Assumes returns follow a normal distribution.
   - Utilizes the mean and standard deviation to calculate VaR.
3. **Monte Carlo Simulation**:
   - Generates synthetic returns based on historical mean and standard deviation.
   - Sorts simulated returns to determine the VaR.

### Visualization
The distribution of daily returns is visualized with:
- A histogram of actual returns.
- An overlay of the normal distribution curve.
- Highlights of the VaR threshold.

### Sample Output
- Historical Method VaR: `2.66%`
- Variance-Covariance VaR: `2.66%`
- Monte Carlo VaR: `2.76%`

These results illustrate the strengths and limitations of each method, especially in capturing tail risk.

## Insights
- The **Historical Method** reflects past behavior but may miss extreme events.
- The **Variance-Covariance Method** simplifies computation but assumes normality, potentially underestimating risk.
- The **Monte Carlo Method** incorporates randomness and extreme scenarios, yielding a higher VaR in some cases.
