# One-page summary

**Question.** How much of each bank stock's variance is market (VN30) risk, and does a single-index model support optimal portfolio selection?

**Data.** 12 bank stocks and VN30, daily closes, 2 Jan 2020 – 19 Jul 2024.

**Finding 1.** The source's "return" is ln Pₜ/ln Pₜ₋₁; on true log returns 8 of 12 betas exceed 1 and σ_M is 1.42%/day (×7).

**Finding 2.** Residuals are cross-correlated (LM 996.8, df 66); a sector factor helps but does not remove it.

**Finding 3.** Betas shift across subperiods; EGP (Sharpe 0.55) does not beat equal weight (0.89) or VN30 (0.98) out of sample, and the difference is not significant.

**Implication.** Check variable definitions before interpreting; use a multi-factor/sector structure for covariance of Vietnamese bank stocks.
