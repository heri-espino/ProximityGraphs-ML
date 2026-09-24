# TODO — Paper 1

This is the operational checklist for the current paper. Items are ordered by dependency, not by perceived difficulty.

## P0 — Literature and novelty audit

- [x] Normalize literature filenames.
- [x] Document the paper scope and theorem targets.
- [ ] Identify the two unresolved PDFs currently named with `Unknown_nd_...`.
- [x] Remove literature clearly unrelated to Paper 1; retain mathematically plausible peripheral sources until the novelty audit.
- [x] Acquire and normalize the core manifold/intrinsic-dimension papers listed in `literature/README.md`.
- [ ] Read Devroye (1988) completely and extract assumptions, theorem statements, proof machinery, and constants.
- [ ] Read Cardinal et al. (2009) and map their empty-region-graph formalism against our fixed-template class.
- [ ] Read Penrose–Yukich's manifold limit theory and identify the exact theorem/hypotheses reusable here.
- [ ] Read the graph-based intrinsic-dimension literature, especially Brito–Quiroz–Yukich and Levina–Bickel.
- [ ] Read IAN (Dyballa–Zucker) carefully for what is already claimed/used about Gabriel degree and dimension.
- [x] Build `docs/NOVELTY_MATRIX.md`: map the closest papers against ERG class, manifold support, tangent-Poisson limits, degree/length laws, dimension inference, and asymptotic theory.
- [x] Write a provisional defensible novelty statement after the first-pass matrix; re-check priority before submission.

## P1 — Formal model

- [ ] Define the sampling model
  \[
  X_1,\ldots,X_n\stackrel{iid}{\sim} f\,d\mathrm{vol}_{\mathcal M},
  \qquad \mathcal M^m\subset\mathbb R^D.
  \]
- [ ] Decide the minimum smoothness assumptions on \(\mathcal M\) (start with compact \(C^2\), no boundary, positive reach).
- [ ] Decide regularity assumptions on \(f\) (start with continuous/Lipschitz and bounded away from \(0\) and \(\infty\)).
- [ ] Define the admissible template class precisely: measurability, similarity equivariance, endpoint symmetry if needed, finite positive unit volume, regular boundary, and any stabilization condition.
- [ ] Define the graph using the ambient Euclidean metric; record where geodesic distance enters only asymptotically.
- [ ] Define the intrinsic \(m\)-dimensional template constant \(a_{m,T}\).
- [ ] Compute/check \(a_{m,T}\) for Gabriel, RNG, and stepping-stone/beta-skeleton examples.

## P2 — Flat Poisson baseline

- [ ] Re-derive the Euclidean homogeneous Poisson edge-void probability from first principles.
- [ ] Re-derive Palm incident-edge radial intensity carefully.
- [ ] Separate three non-equivalent random edge notions: Palm incident edge, uniformly sampled global edge, and nearest eligible edge.
- [ ] Derive degree expectation and graph-size expectation under the exact template hypotheses.
- [ ] Derive all edge-length moment formulas that are genuinely valid for the chosen edge notion.
- [ ] Verify which claims are already in the submitted Unit-Region paper and cite/reuse rather than duplicate.

## P3 — Manifold local limit

- [ ] Prove the local volume lemma
  \[
  \mathrm{vol}_{\mathcal M}(S_T(x,y)\cap\mathcal M)
  =a_{m,T}r^m+o(r^m)
  \]
  uniformly under clearly stated conditions.
- [ ] Determine whether a useful \(O(r^{m+2})\) curvature correction is accessible; treat as optional unless it falls out cleanly.
- [ ] Prove or invoke the rescaled tangent-space point-process limit.
- [ ] Verify stabilization / locality hypotheses for the ERG score.
- [ ] Prove the local graph/tangent-Poisson limit.
- [ ] Derive the scaled edge-probability limit
  \[
  P(x\sim y)\to \exp[-f(x)a_{m,T}t^m],
  \qquad r_n=t n^{-1/m}.
  \]
- [ ] Derive degree convergence and the expected-edge LLN.
- [ ] Decide whether a CLT follows with acceptable additional work; keep it a stretch goal.

## P4 — Intrinsic-dimension inference

- [ ] Define a degree-based estimator \(\widehat m_{\deg}\) where the template constant is invertible in \(m\).
- [ ] For Gabriel, investigate the estimator suggested by \(E[D]\approx 2^m\), but do not claim novelty for the identity itself.
- [ ] Define an edge-length survival / Weibull-slope estimator.
- [ ] Investigate density-free moment-ratio estimators, e.g.
  \[
  \frac{E[R^2]}{E[R]^2}
  =\frac{\Gamma(1+2/m)}{\Gamma(1+1/m)^2}
  \]
  only after confirming the underlying edge law for the precise random-edge definition.
- [ ] Prove consistency for at least one estimator.
- [ ] If feasible, derive asymptotic normality / variance.
- [ ] Investigate whether \(m\) and local density \(f(x)\) can be separated using degree + length information.

## P5 — Simulations

- [ ] Implement reproducible generators for \(S^1\), \(S^2\), tori, Swiss roll, and higher-dimensional spheres/manifolds.
- [ ] Vary intrinsic dimension \(m\), ambient dimension \(D\), sample size \(n\), density \(f\), and curvature/reach.
- [ ] Validate degree constants for multiple templates.
- [ ] Create the key data-collapse experiment for normalized edge lengths.
- [ ] Test density invariance of degree at first order and density scaling of edge lengths.
- [ ] Compare intrinsic-dimension estimators against Levina–Bickel MLE, TwoNN, local PCA/eigenvalue methods, and relevant graph-based baselines.
- [ ] Measure bias, RMSE, rounded-dimension accuracy, and sensitivity to \(n,D,f,\) and curvature.
- [ ] Run template ablations (Gabriel vs RNG vs stepping-stone/beta-skeleton).
- [ ] Treat boundary and off-manifold noise as robustness experiments, not as core theorem assumptions.

## P6 — Manuscript

- [ ] Draft only after the novelty matrix and the first theorem chain are stable.
- [ ] Introduction: problem, gap, contribution, relation to Euclidean ERG theory and manifold point-process limits.
- [ ] Definitions and template class.
- [ ] Tangent-space limit theorem.
- [ ] Degree / edge-length consequences.
- [ ] Intrinsic-dimension estimators.
- [ ] Simulations.
- [ ] Limitations and future work.
- [ ] Append long technical proofs rather than overloading the main narrative.

## Explicitly out of scope for Paper 1

Do not expand Paper 1 into:

- persistent homology;
- Čech or Vietoris–Rips theory;
- topological reconstruction guarantees;
- Laplace–Beltrami / graph-Laplacian convergence;
- spectral manifold learning;
- UMAP/Isomap replacements;
- order-\(k_n\) ERG continuum operators.

Those are candidate follow-up papers after the local stochastic theory is settled.
