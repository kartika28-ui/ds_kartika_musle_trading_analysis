### ds_kartika_musle_trading_analysis
# Trading Behavior vs. Market Sentiment Analysis

This analysis explores the relationship between trader behavior and market sentiment in cryptocurrency markets, using:

Hyperliquid historical trade data (executions, PnL, volumes)
Bitcoin Fear & Greed Index (market sentiment indicators)

## Key Insights

| Market Sentiment | Avg Profit/Trade | Win Rate | Risk Level |
|------------------|------------------|----------|------------|
| Extreme Fear     | +$142.50         | 58%      | High       |
| Greed            | +$89.20          | 62%      | Medium     |
| Neutral          | +$210.80         | 71%      | Low        |



## 1. Main Insight: Profitability vs Risk

<img src="https://github.com/kartika28-ui/ds_kartika_musle_trading_analysis/blob/main/profitability-vs-risk.png" alt="Form Input UI" width="700"/>

Neutral markets offer safest returns (left), while Extreme Fear periods show high-risk/high-reward opportunities (right). Greed phases attract more trades but with diminishing returns.

## 2. Behavioral Pattern: Trading Volume

<img src= "https://github.com/kartika28-ui/ds_kartika_musle_trading_analysis/blob/main/trading-volume.png" alt="Form Input UI" width="700"/>

Heatmap shows traders are most active during Greed periods (top row), but Extreme Fear spikes (red blips) correlate with short-term opportunities.

## 3. Technical Highlight: Date Parsing

> **Problem Solved**:  
> - Handled mixed date formats (DD/MM vs MM/DD) in raw data  
> - Automatically detected IST timestamps when present  
> - Added fail-safe with `dayfirst=True` for European-style dates  
> - Extracted clean date-only column for merging  
