# UPI Transaction Pattern Analyser

End-to-end payment analytics pipeline — churn scoring, fraud detection & interactive dashboard

## Problem statement
India processes 16+ billion UPI transactions monthly (RBI, 2024). Understanding spending patterns, identifying at-risk users, and flagging suspicious activity is critical for any fintech or payment platform. This project builds a production-grade analytics pipeline on 10,000 synthetic UPI transactions calibrated against real RBI payment data.

## Key findings

| Finding | Metric |
|---|---|
| At-risk + churned users | 221 of 500 (44%) |
| Revenue at risk | ₹38.95 lakh |
| Top fraud flag | Amount anomaly (220+ transactions) |
| Highest fraud-risk category | Transport & Utilities |
| Android dominance | 71.8% of all transactions |

## Tech stack
Python · pandas · numpy · Faker · matplotlib · seaborn · plotly · scikit-learn · Jupyter

## Notebooks
| Notebook | Description |
|---|---|
| 01.data generation | 10,000 synthetic UPI transactions (lognormal distribution) |
| 02.cleaning Eda | Feature engineering — hour, day, amount buckets |
| 03.pattern analysis | Heatmap, weekly trend, city tier, device analysis |
| 04.churn rfm | RFM segmentation — Champions, Loyal, At Risk, Churned |
| 05.fraud flags | 3-layer fraud heuristics — Z-score, velocity, off-hours |

## How to run
```bash
git clone https://github.com/Udayshaka/upi-transaction-analyser
cd upi-transaction-analyser
pip install pandas numpy faker matplotlib seaborn plotly scikit-learn jupyter
jupyter notebook
```
Run notebooks in order: 01 → 02 → 03 → 04 → 05

## Limitations & future work
- Synthetic data — real UPI data requires NPCI partnership
- Fraud: ML approach (Isolation Forest) would replace rule-based heuristics
- Churn: survival analysis (Cox Proportional Hazards) for time-to-churn curves

## Data sources
- Synthetic data calibrated against RBI Payment System Indicators FY2024
- NPCI UPI Ecosystem Statistics (monthly)

*Built by Udayshaka | Data Analyst portfolio project | 2025*
