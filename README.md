# 🔴 Project: Clustering-Based-Portfolio-Optimization
This project is a collaborative academic exploration into portfolio optimization using clustering techniques. We aimed to investigate whether unsupervised learning models can enhance traditional momentum-based trading strategies. All strategies are backtested and evaluated based on risk-adjusted metrics.

## 📊 Results Summary
| Strategy   | Monthly Sharpe | Annualized Sharpe | Max Drawdown | Final Portfolio Value | Total Return (%) |
|------------|----------------|-------------------|---------------|------------------------|-------------------|
| Strategy 1 | 0.176          | 0.608             | -35.46%       | $3,833,699             | **+283.37%**      |
| Strategy 2 | 0.275          | 0.954             | -22.40%       | $9,150,980.48          | **+815.10%**      |


## 💡 Objective
To build two alternative investment strategies using clustering models that:
  - Identify meaningful patterns in financial time series
  - Segment stocks into groups based on performance or volatility features
  - Optimize portfolio allocation based on grouped momentum signals

## 📂 Project Notebook
- Project_2_Clustering_Portfolio.ipynb contains the full research pipeline
- Data preprocessing
- Clustering (KMeans, possibly others)
- Portfolio construction & weight allocation
- Performance evaluation

## ⚙️ Tools & Libraries Used
- Python (pandas, NumPy, matplotlib, sklearn, yfinance)
- Algorithms: K Means Clustering
- Portfolio Evaluation: Sharpe Ratio, Maximum Drawdown, CAGR

## 🧠 What We Learned
- Applying unsupervised learning techniques like KMeans can reveal hidden structure in stock behavior.
- Momentum signals can be amplified or filtered through cluster-based stock selection.
- Portfolio construction benefits from risk-aware rebalancing rules post-clustering.
- Evaluation must account for both returns and risk (e.g., using Sharpe and drawdown).
