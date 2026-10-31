# RC Packing-Feasible Note & Measurement Quality Certificate

Contribution toward the open packing-feasible moving-POVM problem in [christophergardner-star/RC-Discovery](https://github.com/christophergardner-star/RC-Discovery), extended into a dimension-free **Measurement Quality Certificate (MQC)**.

## Contents

| File | Description |
|------|-------------|
| `theory/packing_feasible_moving_povm.md` | Packing condition, rank-1 theorem, higher-rank extension, literature differentiation |
| `theory/measurement_quality_certificate.md` | MQC draft (estimation sketch, FT/foundations corollaries) |
| `theory/MQC_complete_status.md` | Items 1–4: sharp $C_{\mathrm{proj}}=1$, sample complexity, surface-code illustration, verification audit |
| `theory/items_5_7_complete.md` | **Items 5–7:** global diamond constant, higher-rank analytic bounds, paper-ready abstract + Lean core |

## Headline results

1. **Packing condition.** $\sigma_{\min}(T)>0$ is necessary and sufficient (up to constants) for quantitative rounding to a repeatable measurement.
2. **Sharp geometric constant.** $\max_j\|E_j-F_j\|_\infty \le \delta+(1-\alpha)$ for both rank-1 and higher rank.
3. **MQC.** $\|\Phi-\Pi\|_\diamond\le C(\delta+(1-\alpha)+\sqrt{\eta/(\kappa\alpha)})$ with working $C=6$, conservative $C=8$.
4. **FT illustration.** Certificate is informative against a ~1% threshold gap; poor packing is rejected.
5. **Higher rank.** Same $1-\alpha$ bound lifts via polar factor of the synthesis matrix.
6. **Lean obligations.** Core linear-algebra statements isolated for Mathlib formalisation.

## Verification status

Self-audited geometric core and constants; external peer review and full Lean proofs still required.

## Note on repository location

Under Cruxy234 because the GitHub integration lacks write access to `christophergardner-star/RC-Discovery`. Copy or PR when access is available.
