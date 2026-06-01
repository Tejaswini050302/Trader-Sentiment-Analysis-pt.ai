# Trader Performance vs Market Sentiment Analysis

## Overview

This project analyzes the relationship between Bitcoin market sentiment (Fear & Greed Index) and trader behavior/performance on Hyperliquid.

The objective is to identify how market sentiment influences:

* Trader profitability (PnL)
* Win rates
* Trading activity
* Position sizing behavior
* Long/Short preferences

The analysis also segments traders into different groups and proposes actionable trading strategies based on the findings.

---

## Dataset

### 1. Bitcoin Fear & Greed Index

Contains daily market sentiment classifications:

* Extreme Fear
* Fear
* Neutral
* Greed
* Extreme Greed

### 2. Hyperliquid Historical Trader Data

Contains trader-level transaction information including:

* Account
* Symbol
* Side
* Execution Price
* Size
* Closed PnL
* Leverage
* Timestamp
* Position Information

---

## Methodology

### Data Preparation

* Loaded both datasets
* Checked missing values and duplicates
* Standardized timestamps
* Extracted trading dates
* Merged sentiment and trading datasets at the daily level

### Feature Engineering

Created the following metrics:

* Win/Loss Indicator
* Daily PnL
* Win Rate
* Trade Count
* Average Trade Size
* Long/Short Bias

### Exploratory Analysis

Analyzed:

* Profitability across sentiment regimes
* Win rate differences
* Trading activity differences
* Position sizing behavior
* Directional trading preferences

### Trader Segmentation

Segmented traders into:

* Frequent vs Infrequent Traders
* Consistent Winners vs Inconsistent Traders
* K-Means Behavioral Clusters

### Statistical Testing

Performed Welch's T-Test to evaluate whether profitability differs significantly between Fear and Greed market conditions.

---

## Key Findings

### 1. Extreme Greed Produced the Highest Profitability

Extreme Greed periods generated the highest average trader profitability and the highest win rate.

### 2. Traders Took Larger Risks During Fear

Average trade sizes were highest during Fear periods despite lower profitability.

### 3. Fear Generated the Highest Trading Activity

Traders were most active during Fear periods, suggesting increased participation during volatile markets.

### 4. Trade Quality Outperformed Trade Quantity

Infrequent traders achieved higher average profitability than frequent traders.

### 5. Consistent Winners Used Smaller Position Sizes

Consistent winners maintained significantly smaller average position sizes while achieving much higher win rates.

### 6. Sentiment Alone Was Not Statistically Significant

Welch's T-Test produced a p-value greater than 0.05, indicating that profitability differences between Fear and Greed periods were not statistically significant.

---

## Strategy Recommendations

### Strategy 1

Reduce leverage and position sizes during Fear periods to limit downside risk.

### Strategy 2

Prioritize high-conviction trades rather than increasing trade frequency.

### Strategy 3

Adopt disciplined position sizing practices similar to those used by consistent winning traders.

---

## Repository Contents

```text
.
├── Notebook.ipynb
├── notebook.py
├── README.md
├── Report.md
```

---

## Running the Analysis

Install required packages:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn scipy
```

Run the script:

```bash
python notebook.py
```

---

## Note

A Python script version (`notebook.py`) is included for easy execution and reproducibility.

If GitHub's notebook renderer is unable to display `Notebook.ipynb`, the complete analysis can still be reviewed and executed using the Python script.

---

## Author

Tejaswini Singh

