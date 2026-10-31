# RC Packing-Feasible Note & Measurement Quality Certificate

Contribution toward the open packing-feasible moving-POVM problem in [christophergardner-star/RC-Discovery](https://github.com/christophergardner-star/RC-Discovery), extended into a dimension-free **Measurement Quality Certificate (MQC)**.

## Contents

| File | Description |
|------|-------------|
| `theory/packing_feasible_moving_povm.md` | Packing condition, rank-1 theorem, higher-rank extension, literature differentiation |
| `theory/measurement_quality_certificate.md` | Earlier MQC draft (constants, estimation sketch, FT/foundations corollaries) |
| `theory/MQC_complete_status.md` | **Complete status on items 1–4**: sharp analytic $C_{\mathrm{proj}}=1$, sample-complexity protocols, surface-code-style numerical illustration, verification audit |

## Headline results

1. **Packing condition.** $\sigma_{\min}(T)>0$ (synthesis operator of near-unit sectors) is necessary and sufficient (up to constants) for quantitative rounding of a POVM to a nearby repeatable measurement.
2. **Sharp constant.** $\max_j\|E_j-F_j\|_\infty \le \delta+(1-\alpha)$ (analytic, phase-aligned polar factor).
3. **MQC.** Dimension-free diamond-norm certificate from $(\eta,\kappa,\alpha,\delta)$.
4. **FT illustration.** Against a ~1% surface-code-style threshold, the certificate is informative: only ultra-high packing quality yields $\varepsilon$ comparable to the threshold gap; poor packing is rejected.

## Verification status

Self-audited geometric core; external peer review and full Lean formalisation still required.

## Note on repository location

This repository is under Cruxy234 because the GitHub integration used for the work does not have write access to `christophergardner-star/RC-Discovery`. The notes can be copied or submitted as a PR once access is available.
