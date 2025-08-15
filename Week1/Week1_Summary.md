# Week 1: Python for Finance Basics - S&P 500 Analysis

## Overview

This document summarizes the Week 1 notebook analysis of S&P 500 historical data using Python for quantitative finance. The analysis demonstrates fundamental data science techniques applied to financial markets.

## Project Structure

- **Notebook**: `Week1_PythonBasics_S&P500.ipynb`
- **Data Source**: Yahoo Finance (^GSPC symbol)
- **Time Period**: January 1, 2020 to January 1, 2025
- **Analysis Type**: Historical price and return analysis

## Libraries and Dependencies

The project uses the following Python libraries:

```python
import pandas
import yfinance as yf
import matplotlib.pyplot as plt
```

### Installation Requirements

```bash
pip install pandas numpy matplotlib scipy yfinance
```

## Data Analysis Components

### 1. Data Acquisition

Downloaded S&P 500 historical data using yfinance:

```python
sp500 = yf.download("^GSPC", start="2020-01-01", end="2025-01-01",
                    auto_adjust=True, progress=False)
```

### 2. Data Exploration

Basic data inspection included:

- First 5 rows examination (`head()`)
- Data structure analysis (`info()`)
- Descriptive statistics (`describe()`)

### 3. Calculated Metrics

#### Daily Returns

```python
sp500['DailyReturn'] = sp500['Close'].pct_change()
```

#### Rolling Statistics (20-day window)

```python
sp500['rollingMean'] = sp500['Close'].rolling(window=20).mean()
sp500['rollingStd'] = sp500['Close'].rolling(window=20).std()
```

#### Short-term Indicators (3-day window)

- `sliceOpen`: 3-day rolling average of opening prices
- `sliceHigh`: 3-day rolling average of high prices
- `sliceLow`: 3-day rolling average of low prices
- `sliceVolume`: 3-day rolling average of volume
- `sliceDailyReturn`: 3-day rolling average of daily returns

#### Extreme Value Tracking

- `topReturn`: Maximum return in 3-day rolling window
- `bottomReturn`: Minimum return in 3-day rolling window

## Visualizations Created

### 1. Complete Rolling Averages Chart

- **Size**: 14x7 figure
- **Content**: All calculated rolling metrics
- **Features**: Comprehensive time series view

### 2. Daily Returns Plot

- **Focus**: S&P 500 daily return patterns
- **Size**: 12x6 figure
- **Purpose**: Volatility and trend analysis

### 3. Returns Distribution Histogram

- **Type**: Histogram with 50 bins
- **Size**: 10x5 figure
- **Analysis**: Distribution shape and outliers

### 4. Price with Volatility Bands

- **Components**:
  - Daily returns line
  - 20-day rolling mean
  - Volatility bands (±1 standard deviation)
- **Features**: Shaded volatility region with transparency

## Key Learning Outcomes

### Technical Skills

1. **Data Import**: Yahoo Finance API integration
2. **Data Processing**: Pandas DataFrame manipulation
3. **Statistical Analysis**: Rolling window calculations
4. **Visualization**: Multiple chart types with matplotlib

### Financial Concepts

1. **Return Calculations**: Daily percentage changes
2. **Moving Averages**: Trend identification techniques
3. **Volatility Measurement**: Standard deviation analysis
4. **Risk Assessment**: Distribution and extreme value analysis

## Code Execution Summary

All notebook cells executed successfully in sequence:

1. **Cell 1**: Library installation comments and shebang
2. **Cell 2**: Library imports
3. **Cell 3**: Data download
4. **Cell 4**: Data exploration with output
5. **Cell 5**: Metric calculations
6. **Cell 6**: Multiple visualizations with image outputs

## Files Generated

- Main analysis notebook with executed code
- Various plots and visualizations
- Calculated financial indicators and metrics

## Next Steps

This foundational analysis sets up for more advanced topics:

- Additional technical indicators
- Portfolio analysis
- Risk management techniques
- Backtesting frameworks
- Machine learning applications

---

*Generated from Week1_PythonBasics_S&P500.ipynb*  
*Analysis Date: August 15, 2025*
