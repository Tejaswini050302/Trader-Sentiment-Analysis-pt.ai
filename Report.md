# Trader Performance vs Market Sentiment

## Objective

The objective of this project was to analyze the relationship between Bitcoin market sentiment (Fear & Greed Index) and trader behavior on Hyperliquid. The analysis aimed to determine whether market sentiment influences trader profitability, win rates, trading activity, and risk-taking behavior.

---

## Methodology

Two datasets were used:

1. Bitcoin Fear & Greed Index
2. Hyperliquid Historical Trader Data

The datasets were cleaned, checked for missing values and duplicates, and merged using daily dates. Several features were engineered, including:

* Win/Loss Indicator
* Daily Profit & Loss (PnL)
* Win Rate
* Trade Count
* Average Trade Size
* Long/Short Bias

Trader segmentation and statistical testing were subsequently performed to identify behavioral patterns.

---

## Exploratory Data Analysis (EDA)

### Profitability by Market Sentiment

Average profitability varied across sentiment regimes:

| Sentiment     | Average PnL |
| ------------- | ----------- |
| Extreme Greed | 67.89       |
| Fear          | 54.29       |
| Greed         | 42.74       |
| Extreme Fear  | 34.54       |
| Neutral       | 34.31       |

Extreme Greed produced the highest profitability, suggesting traders benefited from strong bullish market momentum.

### Win Rate Analysis

| Sentiment     | Win Rate |
| ------------- | -------- |
| Extreme Greed | 46.49%   |
| Fear          | 42.08%   |
| Neutral       | 39.70%   |
| Greed         | 38.48%   |
| Extreme Fear  | 37.06%   |

Trading success rates were highest during Extreme Greed periods and lowest during Extreme Fear periods.

### Trade Size Analysis

| Sentiment     | Average Trade Size (USD) |
| ------------- | ------------------------ |
| Fear          | 7,816                    |
| Greed         | 5,737                    |
| Extreme Fear  | 5,350                    |
| Neutral       | 4,783                    |
| Extreme Greed | 3,112                    |

Interestingly, traders used the largest position sizes during Fear periods despite lower profitability.

### Trading Activity

Fear periods recorded the highest trading activity with 61,837 trades, indicating increased market participation during uncertain conditions.

### Statistical Testing

A Welch's T-Test was conducted to compare profitability during Fear and Greed periods.

* T-statistic: -0.988
* P-value: 0.323

Since the p-value exceeds 0.05, the difference in profitability between Fear and Greed periods was not statistically significant.

---

## Trader Segmentation

### Frequent vs Infrequent Traders

| Segment            | Avg PnL | Win Rate |
| ------------------ | ------- | -------- |
| Frequent Traders   | 57.58   | 41.36%   |
| Infrequent Traders | 137.80  | 39.26%   |

Infrequent traders generated substantially higher profitability despite slightly lower win rates.

### Consistent Winners vs Inconsistent Traders

| Segment              | Avg PnL | Win Rate | Avg Trade Size |
| -------------------- | ------- | -------- | -------------- |
| Consistent Winners   | 106.51  | 69.20%   | 2,334          |
| Inconsistent Traders | 97.10   | 38.38%   | 6,253          |

Consistent winners achieved significantly higher win rates while maintaining smaller position sizes.

### Behavioral Clustering

K-Means clustering identified three trader groups:

* High-profit, high-position-size traders
* High-frequency traders with moderate profitability
* Lower-frequency traders with lower profitability

These clusters demonstrate that trading behavior varies considerably across market participants.

---

## Key Findings

1. Extreme Greed periods generated the highest average profitability and win rates.

2. Fear periods encouraged larger position sizes and higher trading activity.

3. Infrequent traders achieved higher profitability than frequent traders, indicating that trade quality may be more important than trade quantity.

4. Consistent winners used smaller position sizes while maintaining substantially higher win rates.

5. Market sentiment alone was not a statistically significant predictor of profitability.

---

## Strategy Recommendations

### Strategy 1: Reduce Risk During Fear Periods

Since traders tended to increase position sizes during Fear periods without corresponding profitability improvements, reducing leverage and exposure may help preserve capital.

### Strategy 2: Focus on High-Conviction Trades

The superior performance of infrequent traders suggests that selective participation may outperform excessive trading activity.

### Strategy 3: Adopt Disciplined Position Sizing

Consistent winners used significantly smaller average trade sizes, indicating that controlled risk management contributes to long-term success.

---

## Conclusion

The analysis suggests that trader success is influenced not only by market sentiment but also by behavioral factors such as trade frequency, position sizing, and risk management discipline. While Extreme Greed periods produced stronger overall performance, sentiment alone was not sufficient to explain profitability differences. Traders who controlled risk and avoided excessive trading generally achieved better outcomes.
