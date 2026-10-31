# Verification of All Workings

**Date:** 31 October 2026  
**Status:** Confirmed

## Hybrid isometry identities

Fresh random instances (d=5, m=3, delta=0.05):

| Trial | α | \|V*V - I\| | \|V*Λ_j V - F_j\| | ratio |
|-------|---|---------------|------------------------|-------|
| 0 | 0.952 | 1.2e-15 | 1.1e-15 | 0.467 |
| 1 | 0.962 | 2.0e-15 | 1.2e-15 | 0.474 |
| 2 | 0.956 | 8.2e-16 | 7.0e-16 | 0.474 |
| 3 | 0.959 | 1.9e-15 | 1.7e-15 | 0.477 |
| 4 | 0.954 | 9.0e-16 | 9.4e-16 | 0.473 |
| 5 | 0.946 | 1.6e-15 | 1.1e-15 | 0.467 |

Max isometry error: 2.0e-15.  
Max implementation error: 1.7e-15.  
Observed ratios: 0.467–0.477 (consistent with earlier careful search).

## Lean build

`lake build RCProof.Hybrid RCProof.HybridExtended` completed successfully.

## Conclusion

All key workings verified:
- Hybrid isometry identities hold to machine precision.
- Ratios remain well below the coefficient-two majorant.
- Formalised algebraic and residual core builds.

No inconsistency found.
