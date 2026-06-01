# Trader Performance vs Market Sentiment

## Methodology

Bitcoin Fear & Greed Index data was merged with Hyperliquid trader transaction data using trading dates. After cleaning and preprocessing the datasets, several performance and behavioral metrics were engineered, including Closed PnL, win rate, trade frequency, average trade size, and trading direction. Exploratory analysis and trader segmentation were then performed to identify relationships between market sentiment and trading outcomes.

## Key Findings

1. Extreme Greed periods generated the highest average profitability (67.89) and highest win rate (46.49%).

2. Fear periods generated the highest trading activity and largest average position sizes, indicating increased risk-taking behavior during uncertain market conditions.

3. Infrequent traders achieved substantially higher average profitability than frequent traders, suggesting that trade quality may be more important than trade quantity.

4. Consistent winners achieved significantly higher win rates while maintaining much smaller average position sizes, indicating the importance of disciplined risk management.

5. A Welch's t-test found no statistically significant difference between Fear and Greed profitability (p = 0.323), suggesting that trader behavior and risk management may have a stronger impact than sentiment alone.

## Strategy Recommendations

1. Reduce leverage and position sizes during Fear periods to limit downside risk.

2. Prioritize high-conviction trades over excessive trading activity.

3. Adopt disciplined position sizing strategies similar to those used by consistent winning traders.

These findings suggest that successful trading is influenced not only by market sentiment but also by trading discipline, position sizing, and selective participation.
