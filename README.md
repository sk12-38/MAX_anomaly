# MAX Anomaly Strategy

## 한국어

이 저장소는 한국 주식시장에서 나타나는 MAX anomaly를 활용한 행동재무 기반 주식 전략 프로젝트입니다. 투자자가 극단적인 상승 가능성을 가진 복권형 주식을 선호하면서 발생할 수 있는 과대평가와 이후 낮은 수익률을 이용하는 전략을 실험합니다.

### 개요

- 분석 대상: KOSPI, KOSDAQ 종목
- 핵심 신호: 최근 21거래일 잔차수익률 중 상위 5개를 활용한 `MAX5`
- 포트폴리오: Low-MAX 동일가중 포트폴리오
- 리밸런싱: 월간 리밸런싱
- 유동성 필터: 60일 평균 거래대금 하위 10% 제외
- 전략 유형: Long-only 및 long-short

### 방법론

1. Fama-French 3요인 모형으로 개별 종목 잔차수익률을 추정합니다.
2. 최근 21거래일 잔차수익률 중 상위 5개를 이용해 `MAX5`를 계산합니다.
3. 종목을 `MAX5` 기준으로 정렬합니다.
4. MAX 값이 낮은 종목으로 동일가중 포트폴리오를 구성합니다.

### 주요 파일

- `notebooks/Residual_MAX_FF3.ipynb`: 잔차 기반 MAX 신호 구성 노트북
- `reports/Team_02_투자제안서.pdf`: 투자 제안서
- `reports/Team_02_운용보고서_(2025-11).pdf`: 2025년 11월 운용 보고서
- `reports/Team_02_운용보고서_(2025-12).pdf`: 2025년 12월 운용 보고서
- `reports/Team_02_운용보고서_(2026-01).pdf`: 2026년 1월 운용 보고서
- `reports/Team_02_운용보고서_(2026-02).pdf`: 2026년 2월 운용 보고서
- `reports/Team_02_운용보고서_(2026-03).pdf`: 2026년 3월 운용 보고서

## English

This repository implements a behavioral-finance-based equity strategy using the MAX anomaly in the Korean stock market. The project studies whether investors' preference for lottery-like stocks can create overpricing and lower subsequent returns, then tests a strategy designed to exploit that mispricing.

### Overview

- Universe: KOSPI and KOSDAQ stocks
- Main signal: `MAX5`, based on the top 5 residual returns over the recent 21 trading days
- Portfolio: Low-MAX equal-weighted portfolio
- Rebalancing: Monthly
- Liquidity filter: Excludes the bottom 10% by 60-day average trading value
- Strategy type: Long-only and long-short

### Methodology

1. Estimate stock residual returns using the Fama-French 3-factor model.
2. Compute `MAX5` from the top 5 residual returns over the recent 21 trading days.
3. Rank stocks by `MAX5`.
4. Construct an equal-weighted portfolio using low-MAX stocks.

### Main Files

- `notebooks/Residual_MAX_FF3.ipynb`: Residual-based MAX signal construction notebook
- `reports/Team_02_투자제안서.pdf`: Investment proposal
- `reports/Team_02_운용보고서_(2025-11).pdf`: Monthly operation report for 2025-11
- `reports/Team_02_운용보고서_(2025-12).pdf`: Monthly operation report for 2025-12
- `reports/Team_02_운용보고서_(2026-01).pdf`: Monthly operation report for 2026-01
