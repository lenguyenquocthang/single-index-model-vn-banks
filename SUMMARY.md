# One-page summary

**Question.** How much of each bank stock's variance is market (VN30) risk, and does a single-index model support optimal portfolio selection?

**Data.** 12 bank stocks and VN30, daily closes, 2 Jan 2020 – 19 Jul 2024 (1,134 log returns).

**Finding 1.** 8 of 12 banks have beta above 1 (STB 1.39, TCB 1.29, CTG/MBB 1.25, VPB 1.23); ACB, EIB, VCB and VIB sit below 1. $R^2$ ranges from 0.11 to 0.67.

**Finding 2.** Residuals are cross-correlated (LM 996.8, df 66); a sector factor helps (LM 425) but does not remove the dependence.

**Finding 3.** Betas shift across subperiods; EGP (Sharpe 0.55) does not beat equal weight (0.89) or VN30 (0.98) out of sample, and the difference is not significant.

**Implication.** Use a sector-factor structure for the covariance of Vietnamese bank stocks and re-estimate betas by period.
