# ProximityGraphs-ML

Research repository for **Paper 1** in a program connecting empty-region proximity graphs, stochastic geometry, and differential geometry.

## Working paper

**Tentative title:** *Curvature Corrections for Empty-Region Proximity Graphs on Manifolds*

Alternative working title: *How Empty-Region Proximity Graphs See Manifold Geometry*.

The paper is a continuation of the Euclidean unit-region framework, but it is **not** intended to be merely "Unit-Region Factorization with \(d\) replaced by intrinsic dimension \(m\)."

The flat-space theory provides the null model:

\[
\operatorname{Vol}(S_T(x,y))=a_{d,T}r^d.
\]

On a manifold \(\mathcal M^m\subset\mathbb R^D\), the first-order tangent approximation

\[
\operatorname{vol}_{\mathcal M}(S_T(x,y)\cap\mathcal M)
=
a_{m,T}r^m+o(r^m)
\]

is treated as a **baseline consequence**, not the main contribution.

The main research question is:

\[
\boxed{
\text{How do curvature, tangent orientation, codimension, and template geometry perturb the flat ERG laws?}
}
\]

The target is a second-order or otherwise first non-flat expansion such as

\[
\operatorname{vol}_{\mathcal M}(S_T(x,y)\cap\mathcal M)
=
a_T(T_x\mathcal M,u)r^m
+
b_T(x,u)r^{m+q}
+
o(r^{m+q}),
\]

where the correction order \(q\) must be derived rather than assumed and \(b_T(x,u)\) should encode local differential geometry.

## Current state

- Literature corpus assembled and normalized.
- First-pass novelty audit completed in docs/NOVELTY_MATRIX.md.
- The framing has been revised to avoid duplicating Espino (2026), Unit-Region Factorization.
- Tangent-space Poisson limits and intrinsic-dimension estimation are now treated as existing machinery / downstream consequences.
- The next mathematical task is to formalize ambient-template/tangent-section geometry and derive the first non-flat correction.
- **No new theorem in this repository is proved yet unless explicitly marked proved.**

## Start here

1. docs/AI_HANDOFF.md — current intellectual state and immediate next actions.
2. docs/NOVELTY_MATRIX.md — overlap with the earlier Unit-Region paper and the revised novelty target.
3. docs/ROADMAP.md — revised theorem program.
4. TODO.md — executable task list.
5. literature/README.md — literature inventory and naming convention.

## Paper-1 boundary

Paper 1 now targets:

- ambient-template restriction to tangent spaces;
- conditions under which the Euclidean unit-region constant survives as \(a_{m,T}\);
- first non-flat curvature / orientation corrections;
- consequences for ERG void probabilities, degree, and edge-length statistics;
- whether those deviations encode local differential geometry;
- simulations designed to measure the predicted curvature corrections.

Intrinsic-dimension estimation may appear as a **secondary corollary or diagnostic**, but it is no longer the paper's main novelty claim.

Paper 1 does **not** currently target persistent homology, Čech/Vietoris–Rips complexes, Laplace–Beltrami convergence, spectral embeddings, UMAP/Isomap replacements, or full topological reconstruction.

## Candidate graph families

Primary examples:

- Gabriel graph;
- relative neighborhood graph (RNG);
- beta-skeleton / stepping-stone families.

These examples should be used to understand how different template geometries respond to curvature and orientation, not merely to reproduce flat-space degree constants.
