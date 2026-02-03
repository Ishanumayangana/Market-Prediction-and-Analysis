# 📈 Market Prediction and Analysis  

An end-to-end machine learning project to **predict stock market movements**, analyze technical indicators, and compare investment strategies.  
This project demonstrates how machine learning can enhance financial decision-making by integrating **advanced feature engineering, multi-model backtesting, trading signals, and comprehensive performance analysis**.

## 🔍 Project Overview  

The goal of this project is to build predictive models for the **S&P 500 index**, evaluate their accuracy using multiple metrics, and test their effectiveness against a traditional **Buy-and-Hold strategy**.  

### Key Steps:
1. **Data Collection** – Historical S&P 500 data via Yahoo Finance API  
2. **Feature Engineering** – 48 advanced features including technical indicators  
3. **Model Training** – Multiple ML models with hyperparameter tuning  
4. **Backtesting** – Walk-forward validation with configurable parameters  
5. **Trading Simulation** – Strategy vs Buy-and-Hold performance comparison  
6. **Visualization** – Comprehensive charts and model interpretability  

---

## ✨ Features  

### 📊 Data & Preprocessing
- Historical S&P 500 data from 1990 to present  
- Automated data loading with CSV caching  
- Missing value handling and data normalization  

### 🔧 Advanced Feature Engineering (48 Features)
| Category | Features |
|----------|----------|
| **Rolling Statistics** | Close Ratio, Volume Ratio, Volatility, Trend (7 horizons: 2, 5, 10, 20, 60, 250, 1000 days) |
| **RSI** | RSI_7, RSI_14, RSI_21 (Relative Strength Index) |
| **MACD** | MACD Line, Signal Line, Histogram |
| **Bollinger Bands** | BB Width, BB Position |
| **Volatility** | ATR (Average True Range), ATR Ratio |
| **Momentum** | 5, 10, 20-day Price Momentum |
| **Price Patterns** | Gap, Intraday Range, Body Size, Upper/Lower Shadows |
| **Moving Averages** | SMA Crossovers (5/20, 50/200), Price Above SMA200 |

### 🤖 Machine Learning Models
- **Random Forest Classifier** – Ensemble of 200 decision trees  
- **Gradient Boosting Classifier** – Sequential boosting with 100 estimators  
- Probability threshold optimization for precision improvement  

### 🔁 Backtesting Framework
- Walk-forward validation (start: 2500 days, step: 250 days)  
- Configurable probability thresholds  
- Out-of-sample performance evaluation  

### 📈 Comprehensive Evaluation
- **Classification Metrics**: Precision, Recall, F1-Score, Accuracy  
- **ROC Curve** with AUC scores for model comparison  
- **Confusion Matrix** visualization  
- **Rolling Accuracy** over time  
- **Feature Importance** analysis (Top 20 features)  

### 💹 Trading Simulation
- Buy & Hold vs ML Strategy comparison  
- Cumulative returns visualization  
- Sharpe Ratio (annualized)  
- Maximum Drawdown analysis  

---

## 📊 Results Summary

| Model | Precision | Recall | F1-Score | Accuracy |
|-------|-----------|--------|----------|----------|
| **Random Forest** | 55.79% | 36.31% | 43.99% | 49.45% |
| Gradient Boosting | 54.90% | 41.29% | 47.13% | 49.37% |

### Top 5 Most Important Features:
1. `Close_Ratio_2` – 2-day price ratio  
2. `Volatility_1000` – Long-term volatility  
3. `Close_Ratio_5` – 5-day price ratio  
4. `RSI_7` – 7-day Relative Strength Index  
5. `Lower_Shadow` – Candlestick lower shadow  

---

## ⚙️ Technologies Used  

- **Python 3.10+** 🐍  
- **Pandas, NumPy** – Data manipulation & numerical computing  
- **Matplotlib, Seaborn** – Data visualization  
- **Scikit-learn** – Machine learning models & evaluation metrics  
- **yfinance** – Yahoo Finance API for stock data  

### Technical Indicators Implemented:
- RSI (Relative Strength Index)  
- MACD (Moving Average Convergence Divergence)  
- Bollinger Bands  
- ATR (Average True Range)  
- SMA Crossovers (5/20, 50/200)  
- Price Momentum  
- Candlestick Patterns  

