# 01 · Monte Carlo Value at Risk & Expected Shortfall

## Overview

A complete **market risk measurement framework** implementing Monte Carlo-based Value at Risk (VaR) and Conditional Value at Risk (CVaR / Expected Shortfall) for a multi-asset equity portfolio --> directly aligned with **Basel III / FRTB** regulatory requirements.

## Methods

| Component | Description |
|-----------|-------------|
| **Monte Carlo Engine** | 10,000 correlated scenarios via Cholesky decomposition of the covariance matrix |
| **VaR (95%, 99%)** | Quantile-based maximum loss at given confidence levels |
| **CVaR / ES (97.5%)** | Basel III Expected Shortfall — average loss in the worst 2.5% of scenarios |
| **Component VaR** | Risk attribution by asset using the delta-normal decomposition |
| **Kupiec POF Backtest** | χ² likelihood ratio test validating model accuracy against historical breaches |
| **Multi-Day Scaling** | Square-root-of-time rule for regulatory capital horizons (1, 5, 10, 20 days) |

## Key Results (5-Asset Portfolio, €1M)

- 1-Day VaR (99%): computed from 10,000 simulated P&L scenarios
- Expected Shortfall (97.5%): always exceeds VaR — captures tail severity
- Kupiec test: statistical validation at 5% significance level

## Regulatory Context

- **Basel II:** VaR at 99%, 10-day horizon as standard market risk capital metric
- **Basel III / FRTB:** ES at 97.5% replaces VaR as primary metric; stricter backtesting requirements

## References

- Jorion, P. (2007). *Value at Risk* (3rd ed.). McGraw-Hill.
- Basel Committee on Banking Supervision (2019). *Minimum Capital Requirements for Market Risk*.
- Kupiec, P. (1995). *Techniques for Verifying the Accuracy of Risk Measurement Models*. Journal of Derivatives.
