# S&P One-Day Prediction using Gold, Oil and Bond + Technical Indicators
This repositry is a group work for 2301458 Applied Deep Learning, Chulalongkorn University.

This project's architecture is based on a [research paper](https://link.springer.com/article/10.1007/s00521-024-10303-1). But we believe that we can achieve the same performance by just using Gold, Oil and Bond instead of relying on news headlines.

Project's demo can be found in [UpOrDown](https://github.com/Smith8bit/UpOrDown) repositry, or visit our [demo website](https://upordown.streamlit.app/) built using streamlit, The website will be updating for 90 days before we stop maintaining it.

## Results
*Data period: 2022-06-17 — 2026-04-21*
### Model Performance
Overall Accuracy: 53.05%
| Class Performance | Precision | Recall | F1-Score |
|---|---|---|---|
| Downward Direction (0) | 0.48 | 0.51 | 0.50 |
| Upward Direction (1) | 0.57 | 0.55 | 0.56 |

## One-Day Ahead Predictive Performance During the 2026 Energy Crisis

| Performance | 60 Days | 90 Days | 120 Days |
|---|---|---|---|
| Our Model | +21.40% | +24.93% | +13.41% |
| S&P500 | +0.03% | +3.30% | +7.30% |