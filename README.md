# S&P 500 One-Day Prediction using Gold, Oil, Bond and Technical Indicators

This repository is a group project for 2301458 Applied Deep Learning, Chulalongkorn University.
This project's architecture is based on a [research paper](https://link.springer.com/article/10.1007/s00521-024-10303-1). Unlike the original paper, we achieve comparable performance using only Gold, Oil and Bond signals instead of news headlines.

A live demo is available at the [UpOrDown](https://github.com/Smith8bit/UpOrDown) repository, or visit our [demo website](https://upordown.streamlit.app/) built with Streamlit. The website will be updated for 90 days before we stop maintaining it.

## Model Architecture

The model is a 2-layer LSTM with a residual feed-forward network, trained on 60-day sliding window sequences.

### Input Features
**S&P 500 technical indicators**
- Trend: SMA and EMA distance from price (5/10/20/50/200-day), EMA crossovers, MACD, PSAR
- Momentum: RSI, Stochastic RSI, CMF, MFI
- Volatility: Bollinger Bands (high/low/percent/width bands), rolling volatility
- Volume: Volume ratio (relative to 20-day average)
- Returns: Daily, 5/10/20-day returns, Open/High/Low percentage changes

**Cross-asset signals**
- Gold: daily return, RSI
- Crude Oil: daily return, RSI, volume ratio
- US 10-Year Treasury Bond: daily return, yield level, RSI

### Dataset
S&P 500 daily data from 2000 to 2026 (~6,000 trading days), merged with gold, oil and bond data. Split chronologically into train, validation and test sets.
## Results
*Data period: 2022-06-17 to 2026-04-21*

### Model Performance
Overall Accuracy: 53.05%

| Class | Precision | Recall | F1-Score |
|---|---|---|---|
| Downward (0) | 0.48 | 0.51 | 0.50 |
| Upward (1) | 0.57 | 0.55 | 0.56 |

### One-Day Ahead Predictive Performance During the 2026 Energy Crisis

| | 60 Days | 90 Days | 120 Days |
|---|---|---|---|
| Our Model | +21.40% | +24.93% | +13.41% |
| S&P 500 | +0.03% | +3.30% | +7.30% |