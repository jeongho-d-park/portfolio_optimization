# Portfolio Optimization with Modern Portfolio Theory

A practical implementation of portfolio optimization using the Markowitz mean-variance model.  
This project demonstrates how to build and visualize efficient portfolios using historical stock data from 2020 to 2024.

---

## 🚀 Project Overview

This repository contains:
- ✅ Historical price data retrieval via `yfinance`
- ✅ Calculation of daily returns, mean returns, and covariance matrix
- ✅ Implementation of minimum variance portfolio optimization using `scipy.optimize`
- ✅ Random portfolio simulations to visualize the efficient frontier
- ✅ Integration of risk-free rate (IRX) to compute Sharpe ratios in portfolio optimization
- ✅ Integration of risk-free rate (from FRED) to compute Sharpe ratios in the past years

---

## 📈 Data

- **Assets**: AAPL, MSFT, JNJ, JPM, PG, XOM, TSLA  
- **Date Range**: 2020-01-01 ~ 2024-12-31  
- **Risk-Free Rate Source**: 3-Month Treasury Bill, retrieved using Yahoo Finance (`^IRX`)
- **Risk-Free Rate Source**: 3-Month Treasury Bill (FRED: `TB3MS`)

---

## 🧮 Methodology

1. Download historical adjusted close prices using `yfinance`
2. Compute daily returns and covariance matrix
3. Optimize for the minimum variance portfolio with constraints:
   - Total weights sum to 1
   - No short selling (weights between 0 and 1)
4. Simulate 5,000 random portfolios to visualize the efficient frontier
5. Compare optimized portfolios to randomly generated ones

---

## 📊 Results

The following plot shows 5,000 randomly simulated portfolios, with the optimized minimum-variance portfolio highlighted.

![Efficient Frontier](https://github.com/jeongho-d-park/portfolio_optimization/raw/main/output.png)

- Minimum Variance Portfolio:
AAPL	0.0991
MSFT	0.2869
JNJ	    0.0054
JPM	    0.0648
PG	    0.2860
XOM	    0.0896
TSLA	0.1682

---

## 📦 Libraries Used

- Python 3.x
- `yfinance`
- `numpy`, `pandas`
- `matplotlib`, `seaborn`
- `scipy.optimize`
- `pandas_datareader` (for FRED data)

---

## 📁 Folder Structure
├── PfOpt.ipynb # Main Jupyter Notebook for portfolio optimization ├── README.md # Project overview and documentation ├── output.png # Result figure └── .gitattributes # Git settings for text encoding and line endings
