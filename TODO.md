# TODO — Paper 1

This checklist reflects the **revised curvature-focused framing**.

## P0 — Literature / novelty

- [x] Normalize literature filenames.
- [x] Curate clearly unrelated literature.
- [x] Acquire the core manifold / intrinsic-dimension papers.
- [x] Build docs/NOVELTY_MATRIX.md.
- [x] Recognize that a first-order \(d\to m\) extension is too close to the prior Unit-Region paper.
- [x] Reframe Paper 1 around non-flat geometric corrections.
- [ ] Do a final targeted prior-art search for curvature-sensitive proximity-graph asymptotics before submission.

## P1 — Ambient template geometry

- [ ] Write the exact ambient-space definition of \(S_T(x,y)\subset\mathbb R^D\).
- [ ] Separate template coordinates, edge direction \(u\), tangent plane \(T_x\mathcal M\), and ambient orientation.
- [ ] Define the normalized tangent-section coefficient
  \[
  a_T(T_x\mathcal M,u).
  \]
- [ ] Characterize sufficient conditions for
  \[
  a_T(T_x\mathcal M,u)=a_{m,T}.
  \]
- [ ] Determine whether tangent-stable / dimensionally stable is useful terminology or whether existing terminology should be used.
- [ ] Work out Gabriel explicitly as the first sanity check.
- [ ] Work out RNG and stepping-stone / beta-skeleton examples.

## P2 — Local differential geometry

- [ ] Fix the manifold regularity needed for a second-order expansion (\(C^2\), \(C^3\), positive reach, etc.).
- [ ] Put \(\mathcal M\) in a local Monge chart:
  \[
  z\mapsto x+z+\frac12 II_x(z,z)+O(\|z\|^3).
  \]
- [ ] Expand the induced \(m\)-dimensional volume element.
- [ ] Expand the moving boundary of \(S_T(x,y)\cap\mathcal M\).
- [ ] Prove the leading tangent-section term
  \[
  \operatorname{vol}_{\mathcal M}(S_T\cap\mathcal M)
  =
  a_T(T_x\mathcal M,u)r^m+o(r^m).
  \]
- [ ] Determine the **first nonzero correction order**: \(r^{m+1}\) versus \(r^{m+2}\).
- [ ] Identify symmetry conditions that force odd-order terms to vanish.
- [ ] Express the first correction coefficient \(b_T(x,u)\) in terms of \(II_x\), \(u\), and template moments.
- [ ] Derive a quantitative remainder bound if feasible.

## P3 — Probabilistic consequences

- [ ] Insert the geometric expansion into the local binomial / Poisson void probability.
- [ ] Derive the first curvature correction to
  \[
  P(x\sim y\mid x,y).
  \]
- [ ] Re-derive Palm incident-edge statistics using the perturbed geometry.
- [ ] Compute curvature-induced bias in local expected degree.
- [ ] Compute curvature-induced bias in incident-edge moments / quantiles.
- [ ] Investigate directional statistics relative to principal curvature directions.
- [ ] Use Penrose–Yukich only for generic tangent/local-score limit machinery where appropriate.

## P4 — Inverse geometry / inference

- [ ] Test whether the flat law separates \(m\) and \(f(x)\) at leading order.
- [ ] Define curvature-sensitive residuals after subtracting the flat null.
- [ ] Determine which contraction(s) of \(II_x\) are identifiable from an isotropic template.
- [ ] Determine whether anisotropic / directional templates recover more curvature information.
- [ ] Investigate consistency of a curvature estimator only after identifiability is established.
- [ ] Compare templates as geometric sensors: bias, variance, orientation sensitivity.

## P5 — Simulations

- [ ] Implement flat null controls.
- [ ] Simulate circles / spheres with varying radius.
- [ ] Simulate cylinders.
- [ ] Simulate tori and evaluate points with different principal curvatures.
- [ ] Simulate quadratic patches / paraboloids / saddles with known \(II_x\).
- [ ] Vary \(n,m,D,f\), curvature magnitude, curvature sign, and template.
- [ ] Numerically verify the predicted correction order in \(r\).
- [ ] Plot normalized residuals against the theoretical \(b_T(x,u)\).
- [ ] Compare Gabriel, RNG, and stepping-stone curvature sensitivity.
- [ ] Add off-manifold noise only as a later robustness experiment.

## P6 — Manuscript criterion

The paper is **not** ready if it only proves

\[
a_{m,T}r^m+o(r^m)
\]

plus an intrinsic-dimension estimator.

Minimum target:

- [ ] tangent-section theorem;
- [ ] first non-flat correction with geometric interpretation;
- [ ] at least one explicit curvature / orientation effect on an ERG statistic;
- [ ] controlled simulations validating the correction;
- [ ] clear distinction from the prior Unit-Region paper.

## Explicitly out of scope

- persistent homology;
- Čech / Vietoris–Rips;
- topological reconstruction;
- Laplace–Beltrami / graph-Laplacian convergence;
- spectral embeddings;
- UMAP/Isomap replacement;
- order-\(k_n\) continuum operators.
