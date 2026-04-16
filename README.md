# Trader Performance vs Market Sentiment Analysis

## Objective
The project analyzes how market sentiment emotions (Fear vs Greed) influences trader behavior and performance. The goal is to uncover patterns and derive actionable trading strategies based on observed trends.

---

##  Datasets

### 1. Bitcoin Market Sentiment Dataset
- Columns include `date`, `classification` (Fear / Greed / Neutral)

### 2. Historical Trader Data (Hyperliquid)
- Columns include
  - `Size Tokens`
  - `Size USD`
  - `Side` (BUY/SELL)
  - `Timestamp IST`
  - `Start Position`
  - `Direction` (Buy/Sell)
  - `Closed PnL`
  - `Transaction`
  - `Order ID`
  - `Crossed` (TRUE/FALSE)
  - `Fee`
  - `Trade ID`
  - `Timestamp`

---

##  Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/trader-performance-vs-market-sentiment.git
cd trader-performance-vs-market-sentiment
```

### 2. Install Dependencies
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### 3. Run the Notebook
```bash
jupyter notebook notebooks/Trader_Performance_vs_Market_Sentiment.ipynb
```

---

##  How to Run

1. Open `Trader Performance vs Market Sentiment.ipynb`
2. Run all cells sequentially
3. View charts and insights directly in the notebook

---

##  Methodology

### Data Cleaning
- Checked for missing values and duplicates
- Converted timestamps to datetime format
- Standardized date formats

### Data Integration
- Merged trader data with sentiment data on a daily basis

### Feature Engineering
- Daily Profit & Loss (PnL)
- Trade frequency
- Average position size
- Win rate
- Long/short ratio

### Segmentation
- Frequent vs infrequent traders
- Consistent vs volatile traders

### Analysis
- Compared performance across Fear and Greed periods
- Evaluated behavioral changes under different sentiments

---

## 📊 Key Insights

### 🔹 1. PnL Behavior and Volatility
- 'Fear' periods exhibit higher variability in PnL, with lower median returns but higher average PnL driven by extreme positive outliers, indicating a high-risk, high-reward environment.
- In contrast, 'Greed' periods show more stable and consistent returns, with higher median PnL and lower dispersion.
- The maximum daily PnL is significantly higher during 'Fear', reinforcing the presence of occasional large gains.

### 🔹 2. Trading Activity Patterns
- Trading activity is higher during 'Fear' periods, with an increased average number of trades per day, suggesting that traders react more actively to volatile market conditions.
- During 'Greed' periods, trade frequency decreases, indicating a tendency to hold positions longer in more stable environments.
- Higher trade frequency is positively associated with improved PnL, suggesting that active participation may enhance profitability in volatile regimes.

### 🔹 3. Trade Size and Profitability
- Position size (trade size in USD) shows little to no correlation with PnL, indicating that larger trades do not necessarily result in higher profits.
- Trade size and trade frequency appear largely independent, suggesting that traders are not simultaneously increasing both exposure and activity.

### 🔹 4. Market Sentiment Distribution
- 'Greed' sentiment dominates the dataset, accounting for approximately 59% of observations, while 'Fear' represents around 41%, indicating that favorable market conditions are more frequent.

### 🔹 5. Trade Direction Neutrality
- The distribution of BUY (long) and SELL (short) trades is nearly balanced (~50/50), suggesting that overall performance is not driven by directional market bias.

### 🔹 6. Drawdown Characteristics
- Although average drawdowns are similar across sentiments, 'Fear' periods exhibit deeper and more frequent drawdowns, indicating higher downside risk and less stable performance.

##  Strategy Recommendations

### 1. Trade Filtering During Fear Markets
During Fear periods, traders should reduce trade frequency and focus only on high-confidence trades to avoid unnecessary losses.

### 2. Performance-Based Position Allocation
Position sizes should be adjusted based on trader consistency. Consistent traders can increase exposure during Greed periods, while volatile traders should reduce activity during Fear periods.

---

##  Outputs

- Visualizations comparing Fear vs Greed performance
- Behavioral analysis of trading patterns

---


```
