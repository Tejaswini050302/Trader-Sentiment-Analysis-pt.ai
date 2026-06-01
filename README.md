# Trader Performance vs Market Sentiment Analysis

## Overview

This project investigates the relationship between Bitcoin market sentiment and trader performance on Hyperliquid.

The objective is to determine whether different market sentiment conditions (Fear, Greed, Extreme Fear, Extreme Greed, and Neutral) influence:

- Trader profitability (PnL)
- Win rates
- Trading activity
- Position sizing behavior
- Long/Short preferences

The project combines Bitcoin Fear & Greed Index data with Hyperliquid historical trader data to uncover actionable trading insights.

---

## Datasets

### 1. Bitcoin Fear & Greed Index

Contains daily market sentiment classifications:

- Extreme Fear
- Fear
- Neutral
- Greed
- Extreme Greed

### 2. Hyperliquid Historical Trader Data

Contains trader-level transaction information including:

- Account
- Symbol
- Side
- Execution Price
- Size
- Closed PnL
- Leverage
- Timestamp
- Position Information

---

## Project Structure

```text
Trader-Sentiment-Analysis-pt.ai
│
├── Notebook.ipynb
├── notebook.py
├── README.md
├── Report.md
├── PnL_distribution.png
├── k-mean_clusterplot.png
├── long vs short bias.png
├── market sentiment distribution.png
├── trade count.png
├── trade size by sentiment.png
└── win_rate.png
```

---

## Methodology

### Data Preparation

- Loaded both datasets
- Checked for missing values and duplicates
- Converted timestamps to datetime format
- Extracted daily dates
- Merged sentiment and trading data using date

### Feature Engineering

Created the following metrics:

- Win/Loss Indicator
- Daily PnL
- Win Rate
- Trade Count
- Average Trade Size
- Long/Short Bias

### Exploratory Data Analysis

Performed analysis on:

- Profitability by sentiment
- Win rates by sentiment
- Trade counts by sentiment
- Position sizes by sentiment
- Trading direction distribution

### Trader Segmentation

Created trader segments:

- Frequent vs Infrequent Traders
- Consistent Winners vs Inconsistent Traders
- K-Means Behavioral Clusters

### Statistical Testing

Performed Welch's T-Test to compare profitability between Fear and Greed market conditions.

---

## Key Findings

### Extreme Greed Generated Highest Profitability

Extreme Greed periods produced the highest average trader profitability and win rates.

### Fear Produced Highest Trading Activity

Fear periods recorded the largest number of trades, indicating increased participation during uncertain market conditions.

### Traders Took Larger Positions During Fear

Average trade sizes were largest during Fear periods, suggesting increased risk-taking behavior.

### Infrequent Traders Outperformed Frequent Traders

Infrequent traders achieved higher average profitability despite lower trading activity.

### Consistent Winners Used Smaller Positions

Consistent winners maintained significantly smaller average position sizes while achieving much higher win rates.

### Sentiment Alone Was Not Statistically Significant

Welch's T-Test resulted in a p-value greater than 0.05, suggesting that profitability differences between Fear and Greed periods were not statistically significant.

---

## Visualizations Included

- Market Sentiment Distribution
- Profitability Distribution
- Win Rate by Sentiment
- Trade Count by Sentiment
- Trade Size by Sentiment
- Long vs Short Bias
- K-Means Trader Clusters

---

## Setup

### Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scipy scikit-learn
```

### Required Libraries

- pandas
- numpy
- matplotlib
- seaborn
- scipy
- scikit-learn

---

## How to Run

### Option 1: Jupyter Notebook

Open:

```text
Notebook.ipynb
```

Run all cells sequentially.

---

### Option 2: Python Script

Execute:

```bash
python notebook.py
```

The script performs:

1. Data loading
2. Data cleaning
3. Feature engineering
4. Exploratory data analysis
5. Trader segmentation
6. Statistical testing
7. Chart generation

---

## Results

The analysis indicates that trader behavior, risk management, and position sizing have a stronger relationship with profitability than sentiment alone.

The findings suggest that disciplined position sizing and selective trading outperform excessive trading activity.

---

## Report

A detailed summary of the methodology, exploratory analysis, findings, and strategy recommendations is available in:

```text
Report.md
```

---

## Author

Tejaswini Singh
