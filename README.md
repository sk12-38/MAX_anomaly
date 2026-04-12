# MAX Anomaly Strategy

## Overview
This project implements a behavioral-finance-based equity strategy using the MAX anomaly in the Korean stock market.

## Motivation
Investors tend to prefer lottery-like stocks with extreme upside potential. This preference can lead to overpricing and lower subsequent returns. This project attempts to exploit that mispricing.

## Methodology
1. Estimate stock residuals using the Fama-French 3-factor model
2. Compute MAX5 using the top 5 residual returns over the recent 21 trading days
3. Rank stocks by MAX5
4. Construct a Low-MAX equal-weighted portfolio with monthly rebalancing

## Investment Rules
- Universe: KOSPI, KOSDAQ
- Rebalancing: Monthly
- Weighting: Equal-weighted
- Liquidity filter: bottom 10% excluded by 60-day average trading value
- Strategy type: Long-only

## Files
- `notebooks/Residual_MAX_FF3.ipynb`: residual-based signal construction
- `reports/proposal.pdf`: project proposal slides
- `reports/reports/Team_02 운용보고서 (25년 11월)pdf`: monthly operation report
- `reports/reports/Team_02 운용보고서 (25년 12월)pdf`: monthly operation report
- `reports/reports/Team_02 운용보고서 (26년 01월)pdf`: monthly operation report

## Reports
- [Investment Proposal](./reports/Team_02_투자제안서.pdf)
- [Monthly Report 2025-11](./reports/Team_02_운용보고서_(2025-11).pdf)
- [Monthly Report 2025-12](./reports/Team_02_운용보고서_(2025-12).pdf)
- [Monthly Report 2026-01](./reports/Team_02_운용보고서_(2026-01).pdf)
