# Reconciliation with the source study

| # | Source prints | This repository | Effect |
|---|---|---|---|
| R1 | "Return" = ln Pₜ / ln Pₜ₋₁ (sheet TSLN) | log return ln(Pₜ/Pₜ₋₁) | 8/12 betas > 1 instead of 0/12 |
| R2 | "Alpha" 0.02–0.60, α+β=1 for all banks | α −4.5…+4.9 bps/day, all insignificant | printed alpha is 1 − β |
| R3 | σ_M = 0.20%/day; entries like 0.0000045 labelled "%" | σ_M = 1.42%/day; entries are daily variances | absolute risk understated ≈ 7× |
| R4 | VIB highest, VCB lowest return | table: STB highest (1.000102), TCB lowest (1.000003) | text does not match table |
| R5 | "Philippine and Vietnamese markets"; order TCB, STB, VIB, EIB, TPB, VPB | table order TCB, STB, VPB, CTG, MBB; recomputed STB, TCB, CTG, MBB, VPB | wording from another study |
| R6 | TPB t(β)=0.028768; STB p(α)=0.000 with t(α)=0.80 | t(β)=25.6; p(α)≈0.43 | print errors |
| R7 | "Jarque–Bera > α ⇒ cannot reject H0", H0/H1 swapped | all p < 0.001, normality rejected | wording only |
| R8 | 0.7 correlation rule among "independent" variables | one regressor; residual LM = 997 | replace argument |
| R9 | GMM listed as method | OLS only in chapter 3 | drop GMM |
| R10 | covariances "near 0" ⇒ no linear relation | scale of log ratio ≈ 0.002 | do not infer from magnitude |
