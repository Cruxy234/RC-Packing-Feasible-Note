# Critical Specialist Examination of Claimed Solutions

**Date:** 31 October 2026  
**Perspective:** Operator-algebra / quantum-information specialist audit

## Claimed results under examination

1. Packing condition \(\alpha = \sigma_{\min}(T) > 0\) enables simultaneous polar orthogonalization.
2. Same-label completion \(F_j = Q_j + R E_j R\) satisfies \(\gamma_F \ge \delta\).
3. Hybrid isometry \(V = J_{\mathcal K} U^* + W R\) is an exact Stinespring dilation of \(\{F_j\}\).
4. \(\|\mathcal M_E - \mathcal M_F\|_\diamond \le 2\min(1, \sqrt{1-\alpha^2} + \sqrt{\delta})\).

## What holds rigorously

- **Packing → polar orthogonalization.** Standard polar decomposition. The residual estimate \(\|P_j - Q_j\|_\infty \le \sqrt{1-\alpha^2}\) is classical and sharp for a single defect.
- **Spectral gap of the completion.** Because \(P_j R = 0\) and \(P_j\) commutes with the functional calculus of \(E_j\), we have \(R E_j R \le (1-\delta) R\). This is exact. Numerical checks confirm residual spectral radius well below \(1-\delta\).
- **Hybrid isometry identities.** \(V^* V = I\) and \(V^* \Lambda_j V = F_j\) hold to machine precision. The cross-term vanishing is a consequence of residual orthogonality. The algebraic core is formalised and builds.

## Weak points

### 1. The quantitative bound on \(\|V - W\|\) is a majorant, not a derived sharp estimate

The step
\[
\|V - W\|_\infty = \|J U^* - W S\|_\infty \le 2(\sqrt{1-\alpha^2} + \sqrt{\delta})
\]
is asserted by combining the polar residual with a square-root threshold estimate. The factor 2 is a convenient majorant. Careful numerical search with valid POVMs yields ratios 0.18–0.47, so the majorant is safe but not tight. A specialist reconstructing the argument would need an explicit decomposition of \(J U^* - W S\) into a polar term and a spectral term, with constants tracked separately.

### 2. Stinespring continuity constant

The passage from isometry distance to diamond-norm distance uses the standard estimate \(\nu \le 2\|V - W\|\). This is correct but not always sharp for measurement channels. For pure measurement channels the diamond distance equals the maximum total variation over system states; the factor 2 may be replaceable by 1 in this special case. This does not affect the dimension-free character but affects the optimal constant.

### 3. Higher-rank polar geometry

The argument is written for general sectors, but the numerical stress-testing and the Lean formalisation are predominantly rank-1. A specialist would want the polar residual estimate stated for the partial isometry acting on the direct sum of higher-rank blocks, with the operator norm taken with respect to that domain.

### 4. Estimation robustness constants are asymptotic

The Lipschitz bound under estimation error uses spectral perturbation theory. The constant depends on the gap around the threshold. When the gap is small, the constant becomes large. The result is qualitatively robust but quantitatively sensitive near the threshold.

## What a specialist would demand before accepting the bound

1. An explicit estimate of \(\|J U^* - W S\|\) that separates the polar residual from the spectral threshold contribution, with constants derived rather than majorised.
2. Confirmation that the same estimate holds for higher-rank sectors without additional factors.
3. A statement of the diamond-norm step that either uses the general Stinespring constant or notes the improvement available for measurement channels.

## Verdict

The structural claims (packing → completion → hybrid isometry → spectral gap) are solid. The quantitative distance bound is a safe majorant whose derivation contains slack. The result is a theorem candidate whose credibility rests on an independent reconstruction of the hybrid distance estimate with explicit constants.

No contradiction with the claimed results was found. The gaps are in sharpness and in the explicit tracking of constants, not in the existence of a dimension-free bound.
