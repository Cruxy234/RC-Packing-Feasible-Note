# Lean Formalisation Status

**Date:** 31 October 2026  
**Build:** Successful (`lake build RCProof.Hybrid`)

## What is formalised

- `hybrid_is_isometry`: If the cross terms vanish and the two summands are partial isometries with complementary domain supports, their sum is an isometry.
- `implements_completion`: The implementation identity is recorded as a hypothesis (definitional).

## What remains open for full end-to-end formalisation

- The geometric fact that the residual subspace is orthogonal to the near-unit sectors (so the cross term vanishes).
- The polar residual estimate controlling `||V - W||`.
- The spectral-gap argument for `gamma_F >= delta`.
- The Stinespring continuity step from isometry distance to diamond-norm distance.
- Composition with Record-Margin Stability.

## Status

The algebraic core of the hybrid isometry is formalised and builds. The remaining steps are analytic/geometric and require additional Mathlib infrastructure or longer formalisation effort. This is a verified partial formalisation, not a complete end-to-end proof.
