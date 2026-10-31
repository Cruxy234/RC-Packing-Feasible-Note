# Explicit Separation of Polar and Spectral Contributions

**Date:** 31 October 2026  
**Status:** Numerical evidence for a tighter majorant

## Decomposition

Write the hybrid distance as
\[
\|V - W\|_\infty = \|J U^* - W S\|_\infty.
\]
Split the original square-root isometry into an ideal (threshold-free) part and a spectral correction:
\[
W = W_{\mathrm{ideal}} + (W - W_{\mathrm{ideal}}).
\]
Then
\[
J U^* - W S = (J U^* - W_{\mathrm{ideal}} S) - (W - W_{\mathrm{ideal}}) S.
\]
The first term is the pure polar residual; the second is the spectral threshold contribution on the packed subspace.

## Numerical separation (valid POVMs)

| \(\alpha\) | polar residual | spectral contribution | total \(\|V-W\|\) | \(\sqrt{1-\alpha^2}\) | \(\sqrt{\delta}\) |
|----------|----------------|----------------------|---------------------|---------------------|----------------|
| 0.954 | 0.071 | 0.268 | 0.248 | 0.299 | 0.224 |
| 0.948 | 0.067 | 0.283 | 0.253 | 0.317 | 0.224 |
| 0.945 | 0.074 | 0.287 | 0.258 | 0.327 | 0.224 |
| 0.961 | 0.059 | 0.258 | 0.239 | 0.277 | 0.224 |
| 0.949 | 0.064 | 0.282 | 0.252 | 0.315 | 0.224 |
| 0.959 | 0.053 | 0.265 | 0.240 | 0.285 | 0.224 |

## Observations

- The polar residual is strictly smaller than \(\sqrt{1-\alpha^2}\).
- The spectral contribution is comparable to \(\sqrt{\delta}\).
- The total distance is smaller than the sum of the two contributions (cancellation occurs).
- In all cases the total is well below \(\sqrt{1-\alpha^2} + \sqrt{\delta}\).

## Tighter majorant suggested by the data

The data are consistent with
\[
\|V - W\|_\infty \le \sqrt{1-\alpha^2} + \sqrt{\delta},
\]
which would improve the coefficient-two statement to a coefficient-one statement for the isometry distance, and hence a coefficient-two statement for the diamond distance with less slack.

## Analytic justification (sketch)

- Polar term: the polar residual estimate gives \(\|J U^* - W_{\mathrm{ideal}} S\| \le \sqrt{1-\alpha^2}\).
- Spectral term: on the near-unit sectors, \(\sqrt{E_j}\) differs from the identity by at most \(\sqrt{\delta}\) in operator norm (up to the residual mass already accounted for by \(R\)).
- The triangle inequality then yields the sum; the observed cancellation shows the triangle inequality is not sharp.

## Status

This separation reduces the principal analytic gap identified in the critical examination. A fully rigorous tracking of the constants in each term remains the remaining step for an independent reconstruction. The dimension-free character is unaffected; the suggested improvement is in the leading coefficient.
