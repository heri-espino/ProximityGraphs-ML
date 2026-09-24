# AI Handoff — ProximityGraphs-ML

**Last updated:** 2026-09-24  
**Project:** Paper 1 — differential-geometric corrections to empty-region proximity graphs  
**Repository:** heri-espino/ProximityGraphs-ML

## Critical framing change

Do **not** continue the old framing "extend Unit-Region Factorization from \(d\) to intrinsic dimension \(m\) and build an intrinsic-dimension estimator."

That is now considered too close to the user's previous paper:

Espino_2026_Unit-Region-Factorization-Empty-Region-Graphs.pdf

The earlier paper already has the flat-space chain

\[
T
\to
a_{d,T}
\to
\text{Poisson void law}
\to
\text{degree / incident-edge laws}.
\]

A new paper whose main result is only

\[
d\rightsquigarrow m
\]

via tangent-space Poisson limits would be too incremental, especially because Penrose–Yukich already provides general tangent-space limit theory for local manifold functionals.

## Revised paper question

The project now asks:

\[
\boxed{
\text{How does differential geometry perturb the flat unit-region laws?}
}
\]

For a manifold

\[
\mathcal M^m\subset\mathbb R^D
\]

and ambient exclusion region \(S_T(x,y)\), the first-order tangent approximation

\[
\operatorname{vol}_{\mathcal M}(S_T(x,y)\cap\mathcal M)
=
a_{m,T}r^m+o(r^m)
\]

is a **baseline lemma**, not the intended headline result.

The main target is a first non-flat expansion

\[
\operatorname{vol}_{\mathcal M}(S_T(x,y)\cap\mathcal M)
=
a_T(T_x\mathcal M,u)r^m
+
b_T(x,u)r^{m+q}
+
o(r^{m+q}),
\]

where the correction order \(q\) must be derived rather than assumed.

The coefficient should encode local geometry through objects such as the second fundamental form \(II_x\), edge direction \(u\), tangent orientation, codimension, and template geometry.

## Key structural question

The exclusion region is constructed in ambient space, so the leading object is a tangent section:

\[
S_T(x,y)\cap T_x\mathcal M.
\]

Do not assume automatically that its normalized \(m\)-volume is the same universal \(a_{m,T}\).

Define / investigate

\[
a_T(T_x\mathcal M,u)
\]

and characterize templates for which

\[
a_T(T_x\mathcal M,u)=a_{m,T}
\]

independently of orientation and direction.

This tangent-stability question may itself be an important structural contribution.

## Role of intrinsic dimension

Intrinsic dimension is now secondary.

Known literature already covers graph-theoretic intrinsic-dimension estimation, local Poisson nearest-neighbor estimators, graph edge-length estimators, Gabriel degree as a dimensionality signal, and tangent-space Poisson limits.

The new paper should use the flat \(m\)-dimensional laws as a null model and study deviations caused by curvature.

A stronger inverse-geometric target is

\[
\text{leading exponent}\to m,\qquad
\text{scale}\to f(x),\qquad
\text{second-order residual}\to\text{curvature}.
\]

This is a research target, not a proved claim.

## Current strongest candidate theorem

1. Tangent-section expansion:
   \[
   \operatorname{vol}_{\mathcal M}(S_T\cap\mathcal M)
   =
   a_T(T_x\mathcal M,u)r^m+o(r^m).
   \]

2. First non-flat correction:
   \[
   =
   a_T(T_x\mathcal M,u)r^m
   +
   b_T(x,u)r^{m+q}
   +
   o(r^{m+q}),
   \]
   with \(q\) determined by symmetry.

3. Translate \(b_T\) into perturbed edge probabilities and local graph statistics.

4. Investigate identifiability / estimation of curvature information from ERG residuals.

## Literature manual

**literature/MANUAL.md** is now the primary entry point to the literature corpus. It maps the important formulas/theorems to source PDFs and records what is reusable versus already occupied prior art. Read it before starting a proof, then open the cited original PDFs for exact hypotheses.

## Immediate next work

Do **geometry first**, statistics second.

1. Formalize the ambient template construction.
2. Work in a local chart / Monge patch:
   \[
   z\mapsto
   x+z+\frac12 II_x(z,z)+O(\|z\|^3).
   \]
3. Intersect the scaled exclusion region with this graph.
4. Expand the induced \(m\)-volume element and moving boundary.
5. Determine whether the first correction is \(r^{m+1}\) or \(r^{m+2}\).
6. Identify symmetry conditions that cancel odd terms.
7. Compute the coefficient explicitly for Gabriel first.
8. Then test RNG and stepping-stone templates.
9. Only after that return to Penrose/Palm consequences.

## What has been completed

- Literature corpus assembled and normalized.
- First-pass novelty matrix completed.
- The overlap with the previous Unit-Region paper was explicitly recognized.
- Project framing revised toward curvature/orientation corrections.
- Core intrinsic-dimension literature is present.
- Repo documentation treats tangent-Poisson and \(d\to m\) as background/baseline.

## What is not done

- No formal ambient-template class.
- No tangent-section theorem.
- No curvature expansion.
- No proof of the order of the first correction.
- No curvature-sensitive ERG statistic.
- No simulation code for curvature experiments.
- No paper draft.

## Referee test

If the paper can still be summarized as

> "Take the previous unit-region theory, replace \(d\) by \(m\), and invoke Penrose–Yukich,"

then the project is not ready.

The desired summary is instead:

> "Use the flat unit-region theory as a null model and derive how embedded-manifold geometry changes empty-region volumes and proximity-graph statistics."

## Conventions for future agents

- Never present \(a_{m,T}r^m+o(r^m)\) alone as the main novelty.
- Never present Gabriel \(E[D]\approx2^m\) as new.
- Use Penrose–Yukich as enabling machinery, not as a theorem to rediscover.
- Separate inherited flat-space results from genuinely new manifold corrections.
- Distinguish ambient dimension \(D\), intrinsic dimension \(m\), tangent orientation, and edge direction.
- Check carefully whether an \(r^{m+1}\) term appears before assuming the correction is \(r^{m+2}\).
- Treat curvature estimation as a target only after the expansion is mathematically established.
