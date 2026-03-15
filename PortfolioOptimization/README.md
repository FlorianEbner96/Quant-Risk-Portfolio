# 02 · Portfolio Optimization — Efficient Frontier & Risk Parity

## Overview

A complete **Modern Portfolio Theory (MPT)** implementation covering four portfolio construction strategies used in institutional asset management, with performance backtesting and risk attribution.

## Methods

| Strategy | Objective | Key Insight |
|----------|-----------|-------------|
| **Minimum Variance** | Minimise portfolio volatility | Relies only on covariance matrix — robust to return estimation error |
| **Maximum Sharpe Ratio** | Maximise risk-adjusted return | Tangency portfolio; optimal for all investors per Tobin separation theorem |
| **Equal Weight** | 1/N allocation | Naive benchmark; surprisingly competitive in practice |
| **Risk Parity** | Equal risk contribution per asset | Bridgewater approach; avoids return forecasting entirely |

## Key Visualisations

- **Efficient Frontier** coloured by Sharpe Ratio with Capital Market Line
- **Weight allocation** comparison across all four strategies
- **Cumulative performance & drawdown** backtest (5-year simulated history)
- **Risk contribution** decomposition — shows how Risk Parity differs from others

## Theoretical Background

- Markowitz (1952) mean-variance framework
- SLSQP constrained optimisation (long-only, weights sum to 1)
- Tobin separation theorem and the Capital Market Line
- Risk contribution: $TRC_i = w_i \cdot (Σw)_i / σ_p$
- Calmar Ratio: annualised return / |Max Drawdown|

## References

- Markowitz, H. (1952). *Portfolio Selection*. Journal of Finance.
- Black, F. & Litterman, R. (1992). *Global Portfolio Optimization*. Financial Analysts Journal.
- Michaud, R. (1989). *The Markowitz Optimization Enigma*. Financial Analysts Journal.
