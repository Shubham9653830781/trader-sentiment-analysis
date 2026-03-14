# Round-0 Assignment Submission – Primetrade.ai Data Science Internship

# Trader Performance vs Market Sentiment Analysis

## Overview
This project analyzes the relationship between **Bitcoin market sentiment (Fear/Greed)** and **trader behavior and performance** using historical trading data from the Hyperliquid platform.

The goal is to identify patterns in trader activity during different market sentiment conditions and derive insights that could inform more effective trading strategies.

This project was completed as part of the **Round-0 Data Science / Analytics Intern assignment for Primetrade.ai**.

---

# Dataset Description

## 1. Bitcoin Market Sentiment Dataset
This dataset contains the **Fear & Greed Index**, which measures overall market sentiment.

Columns:
- `timestamp` – Unix timestamp of sentiment value
- `value` – Numerical sentiment score
- `classification` – Market sentiment label (Fear / Greed)
- `date` – Date of sentiment measurement

---

## 2. Historical Trader Data (Hyperliquid)
This dataset contains detailed trading activity for multiple accounts.

Columns include:
- `Account` – Trader account ID
- `Coin` – Traded asset
- `Execution Price` – Trade execution price
- `Size Tokens` – Trade size in tokens
- `Size USD` – Trade size in USD
- `Side` – Buy / Sell
- `Closed PnL` – Profit or loss from the trade
- `Timestamp` – Trade timestamp
- `Start Position` – Position before trade
- `Direction` – Trade direction
- `Fee` – Trading fee
- `Transaction Hash` – Transaction identifier
- `Trade ID` – Trade identifier

Total trades analyzed: **211k+ trades**

---

# Project Workflow

## 1. Data Preparation
Steps performed:

- Loaded both datasets using **Pandas**
- Checked dataset dimensions
- Verified missing values
- Removed duplicate records
- Converted timestamps into datetime format
- Aggregated trading data at a **daily level**
- Merged sentiment data with trading records using date alignment

---

## 2. Feature Engineering
Key metrics created:

- **Daily PnL per trader**
- **Win rate per trader**
- **Average trade size**
- **Trades per day**
- **Long vs Short ratio**
- **Trader activity segments**

---

## 3. Trader Segmentation
To better understand trader behavior, traders were segmented into:

### High Frequency vs Low Frequency Traders
Based on number of trades executed.

### Consistent Winners vs Inconsistent Traders
Based on cumulative PnL.

### Large Position vs Small Position Traders
Based on trade size distribution.

---

# Analysis

The analysis focused on answering the following questions:

### 1. Does trader performance differ between Fear and Greed markets?

Average PnL was compared between sentiment regimes to observe how trader profitability changes under different market conditions.

---

### 2. Do traders change behavior based on sentiment?

Behavioral changes analyzed:

- Trade frequency
- Position size
- Long vs Short bias

---

### 3. How do different trader segments behave?

Segment performance was analyzed to determine which types of traders perform better under varying sentiment conditions.

---

# Key Insights

### Insight 1
Trading activity increases during **Greed periods**, suggesting traders become more confident and active when markets are bullish.

### Insight 2
Large position traders experience **higher PnL volatility during Fear markets**, indicating increased risk exposure during uncertain market conditions.

### Insight 3
High-frequency traders show **more consistent profitability**, likely due to faster reaction to market sentiment changes.

---

# Strategy Recommendations

### Strategy 1 – Risk Reduction in Fear Markets
Reduce position sizes and leverage during **Fear sentiment periods** to mitigate downside risk.

---

### Strategy 2 – Momentum Strategy in Greed Markets
During **Greed sentiment periods**, traders can increase trade frequency to capitalize on bullish momentum.

---

### Strategy 3 – Segment-Based Trading
Low-frequency traders should avoid trading during high volatility fear markets due to increased loss probability.

---

# Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

# Project Structure

trader-sentiment-analysis
│
├── data
│ ├── fear_greed_index.csv
│ └── historical_data.csv
│
├── analysis.ipynb
├── README.md
└── requirements.txt


---

# How to Run the Project

1. Clone the repository
git clone https://github.com/yourusername/trader-sentiment-analysis

2. Install dependencies
pip install -r requirements.txt

3. Run the analysis notebook
analysis.ipynb	


---

# Future Improvements

- Build predictive models for trader profitability
- Cluster traders into behavioral archetypes
- Develop an interactive Streamlit dashboard
- Perform risk-adjusted performance analysis

---

# Author

Shubham  
Chemical Engineering, IIT (BHU) Varanasi  
Data Science & Machine Learning Enthusiast