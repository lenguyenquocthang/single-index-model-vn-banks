# Systematic Risk of Vietnamese Bank Stocks: Single-Index Model vs VN30, 2020–2024

Sharpe's single-index model (SIM) for **12 listed bank stocks against VN30 (2 Jan 2020 – 19 Jul 2024, 1,134 daily returns)**, with HAC inference, residual-dependence tests, subperiod stability and an out-of-sample test of the Elton–Gruber–Padberg (EGP) portfolio. Part of my [quant portfolio](https://github.com/lenguyenquocthang/quant-portfolio).

**Pages:** [Landing](https://lenguyenquocthang.github.io/single-index-model-vn-banks/) · [Scroll presentation](https://lenguyenquocthang.github.io/single-index-model-vn-banks/presentation/) · [Research report](https://lenguyenquocthang.github.io/single-index-model-vn-banks/report/)

## Model

$$r_{it}=\alpha_i+\beta_i\,r_{Mt}+\varepsilon_{it},\qquad \sigma_i^2=\beta_i^2\sigma_M^2+\sigma_{\varepsilon i}^2,\qquad r_{it}=\ln\frac{P_{it}}{P_{i,t-1}}$$

Betas by OLS with Newey–West (5 lags) standard errors; Dimson ($t\pm1$) and Blume ($\tfrac23\beta+\tfrac13$) adjustments; Breusch–Pagan $LM=T\sum_{i<j}\hat\rho_{ij}^2\sim\chi^2(66)$ for residual cross-correlation; two-index model with an orthogonalised other-banks factor; EGP trained to 2022, tested 2023–Jul 2024 with a block bootstrap for the Sharpe difference.

## Main findings
| Item | Result |
|---|---|
| Sample | 12 bank stocks, 1,134 daily log returns; ADF rejects a unit root in returns, JB rejects normality for all series |
| Betas | 8 of 12 exceed 1 (STB 1.39, TCB 1.29, CTG/MBB 1.25, VPB 1.23, BID 1.14, HDB/TPB 1.04) |
| Risk split | $\sigma_M=1.42\%$/day; $R^2$ ranges from 0.11 (EIB) to 0.67 (MBB) |
| Alpha | −4.5 to +4.9 bps/day, none significant ($\lvert t\rvert<1$) |
| Residuals | $LM=996.8$, $p\approx10^{-166}$: SIM independence rejected; sector factor significant for 10/12 banks and cuts $LM$ to 425 |
| Stability | Betas move across 2020–21, 2022, 2023–24 (e.g. VIB 0.47 → 1.18 → 1.05) |
| EGP out of sample | Sharpe 0.55 vs 0.89 (equal weight) and 0.98 (VN30); difference CI [−1.16, 0.51] contains 0 |

## Limitations
All 12 stocks are VN30 members (large-cap selection) and VN30 contains these banks, so betas carry a mechanical component. Prices are used as supplied. The out-of-sample window is 18 months. Statistical associations only, not investment advice. The report appendix and `ERRATA.md` reconcile these results with the tables printed in the source study.

## Repository
| Path | Content |
|---|---|
| `presentation/` | Scroll presentation (VI/EN, light/dark) |
| `report/` | Research report (VI/EN) with data reconciliation appendix |
| `data/` | Daily closing prices of 12 banks and VN30, plus the series printed in the source |
| `reestimation/` | Python code and results (JSON, figures) |
| `ERRATA.md`, `SUMMARY.md` | Reconciliation with the source study; one-page summary |

```bash
cd reestimation && pip install -r requirements.txt
python run.py --data ../data/prices_12_bank_stocks_vn30.xlsx --out results
python make_figures.py
```

Academic analysis, not investment advice.
