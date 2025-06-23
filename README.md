# 🔴 Project: Clustering-Based-Portfolio-Optimization
This project is a collaborative academic exploration into portfolio optimization using clustering techniques. We aimed to investigate whether unsupervised learning models can enhance traditional momentum-based trading strategies. All strategies are backtested and evaluated based on risk-adjusted metrics.

## 📊 Performance Evaluation
| Strategy   | Monthly Sharpe | Annualized Sharpe | Max Drawdown | Final Portfolio Value | Total Return (%) |
|------------|----------------|-------------------|---------------|------------------------|-------------------|
| Strategy 1 | 0.176          | 0.608             | -35.46%       | $3,833,699             | **+283.37%**      |
| Strategy 2 | 0.275          | 0.954             | -22.40%       | $9,150,980.48          | **+815.10%**      |

## 📘 Strategy Breakdown

### 📌 Strategy 1 — CAPM-Based Selection with GMVP Allocation
> This strategy focuses on selecting stocks using CAPM parameters and allocating capital using Global Minimum Variance Portfolio (GMVP) weights.

- **Stock Selection**:
  - Stocks were selected monthly based on CAPM alpha and beta values.
  - Only stocks with \( 0 < \beta < 1 \) were considered, favoring moderately responsive stocks.
- **Portfolio Formation**:
  - Each month, 5 stocks were selected and their historical returns were collected.
  - GMVP weights were calculated using the inverse of the covariance matrix to minimize portfolio variance.
- **Capital Allocation**:
  - Monthly returns were computed using weighted combinations of selected stocks.
  - Capital was reallocated monthly based on these selections and weights.
- **Performance Evaluation**:
  - Final capital grew from $1,000,000 to **$3,833,699**, a **+283.37%** return.
  - Monthly Sharpe: **0.176**, Annualized Sharpe: **0.608**, Max Drawdown: **-35.46%**

---

### 📌 Strategy 2 — KMeans Clustering with CAPM Refinement
> This enhanced strategy integrates KMeans clustering to group stocks by return features and then applies CAPM-based filtering within clusters.

- **Clustering**:
  - Stocks were grouped monthly using **KMeans** (with 5 clusters) on return-based feature matrices.
  - Each cluster was analyzed independently for stock characteristics.
- **Refined Selection**:
  - From each cluster, stocks with the best CAPM profiles (positive alpha, beta between 0 and 1) were chosen.
  - A total of 5 stocks were selected monthly from across clusters.
- **Portfolio Formation & Allocation**:
  - GMVP weights were computed as in Strategy 1 for diversification.
  - Monthly rebalancing was performed based on cluster-informed selections.
- **Performance Evaluation**:
  - Final capital grew from $1,000,000 to **$9,150,980**, a **+815.10%** return.
  - Monthly Sharpe: **0.275**, Annualized Sharpe: **0.954**, Max Drawdown: **-22.40%**



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
