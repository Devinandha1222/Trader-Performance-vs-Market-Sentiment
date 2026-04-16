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

## Key Insights

### 🔹 1. Performance Patterns
- Traders achieve higher average profitability during Greed periods
- However, Greed periods also show increased variability, indicating higher volatility in outcomes

### 🔹 2. Behavioral Changes
- Trading activity increases significantly during Greed, reflecting higher market confidence
- During Fear periods, traders become more cautious, leading to reduced trade frequency

### 🔹 3. Risk & Consistency
- Performance during Fear periods is less stable, with greater fluctuations in PnL
- Volatile traders experience larger losses during Fear, while consistent traders maintain relatively stable outcomes

### 🔹 4. Market Sentiment Impact
- Market sentiment has a clear influence on both trader behavior and performance
- Greed encourages aggressive participation, while Fear leads to conservative decision-making

---

##  Strategy Recommendations

### 1. Trade Filtering During Fear Markets
During Fear periods, traders should reduce trade frequency and focus only on high-confidence trades to avoid unnecessary losses.

### 2. Performance-Based Position Allocation
Position sizes should be adjusted based on trader consistency. Consistent traders can increase exposure during Greed periods, while volatile traders should reduce activity during Fear periods.

---

##  Outputs

- Visualizations comparing Fear vs Greed performance
- Behavioral analysis of trading patterns
- Segment-based insights

---

##  Project Structure

```
trader-sentiment-analysis/
│
├── data/
│   ├── fear_greed_index.csv
│   └── historical_data.csv
├── notebooks/
│   └── Trader_Performance_vs_Market_Sentiment.ipynb
├── outputs/
│   ├── charts/
│   └── tables/
└── README.md
```
