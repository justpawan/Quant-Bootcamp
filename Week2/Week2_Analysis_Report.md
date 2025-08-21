# Week 2 Analysis Report: Probability, Statistics & Portfolio Optimization

## 1. Data Acquisition

- Selected 10 major US stocks (AAPL, MSFT, AMZN, GOOGL, META, TSLA, NVDA, JPM, V, JNJ/UNH/XOM).
- Downloaded 5 years of daily adjusted close prices using `yfinance`.

## 2. Return & Risk Calculation

- **Daily Returns:** Calculated percentage change in closing prices.
- **Annualized Return & Volatility:** Scaled daily mean and standard deviation to annual figures (252 trading days).

## 3. Portfolio Statistics

- **Random Portfolio Weights:** Generated random weights summing to 1.
- **Expected Portfolio Return:** Weighted sum of mean returns.
- **Portfolio Volatility:** Computed using the covariance matrix and weights.

## 4. Visualization

- **Risk-Return Scatter Plot:** Plotted annualized return vs. volatility for each stock and the random portfolio.
- **Correlation Heatmap:** Used seaborn to visualize the correlation matrix of stock returns.
- **Efficient Frontier:** Simulated 5000 random portfolios, plotted return vs. volatility, colored by Sharpe ratio, and highlighted the maximum Sharpe portfolio.

## 5. Key Insights

- Diversification reduces portfolio risk compared to individual stocks.
- Correlation analysis helps identify diversification opportunities.
- The efficient frontier illustrates the trade-off between risk and return and helps identify optimal portfolios.

## 6. Next Steps

- Explore more advanced optimization (e.g., constraints, risk-free asset).
- Analyze the impact of changing the stock universe.
- Introduce additional risk metrics (e.g., Value at Risk, Conditional VaR).

---

*See the Jupyter notebooks for code, outputs, and visualizations.*
