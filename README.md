# FTSE 100 Stock Ranking Model

This project analyses companies in the **FTSE 100 index** and builds a simple quantitative model to rank stocks based on **return and risk metrics**.

The goal is to identify companies that offer the strongest **risk-adjusted performance** using historica; price data.

The project demonstrates how financial data can be collected, transformed, and analysed using Python.

---

## Methodology

The analysis is carried out in three stages.

### 1. Data Collection

Historical stock price data for FTSE 100 companies is collected using the **Yahoo Finance API** through the `yfinance` Python library.

The dataset contains **adjusted closing prices** for each company starting from 2023.

Key steps:

- Retrieve price data for FTSE 100 tickers  
- Clean and structure the dataset  
- Store the dataset for further analysis  

---

### 2. Return and Risk Analysis

The raw price data is transformed into key financial performance metrics.

Two core measures are calculated:

**Total Return**

Measures overall price growth over the time period.

**Volatility**

Measures the standard deviation of daily returns and serves as a proxy for risk.

Higher volatility indicates greater uncertainty in stock performance.

---

### 3. Stock Ranking Model

Stocks are ranked using a **composite scoring model** based on:

- Total Return (higher is better)
- Volatility (lower is better)

Each metric is standardised using **z-scores**, and the final ranking score is calculated as: 

score = return_zscore - volatility_zscore

Stocks with **high returns and lower volatility** receive the highest rankings.
