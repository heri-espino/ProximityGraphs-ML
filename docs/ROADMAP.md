# Research Roadmap — Curvature Corrections for Empty-Region Proximity Graphs

## 1. Revised research objective

Let

\[
\mathcal M^m\subset\mathbb R^D
\]

be a smooth embedded manifold and let

\[
X_1,\ldots,X_n\stackrel{iid}{\sim}f\,d\operatorname{vol}_{\mathcal M}.
\]

For an ambient fixed-template empty-region rule \(T\), the edge \(x_i x_j\) is retained when its exclusion region \(S_T(x_i,x_j)\) contains no other sample point.

The earlier Euclidean unit-region theory gives the flat-space factorization

\[
\operatorname{Vol}_d(S_T(x,y))=a_{d,T}\|x-y\|^d.
\]

The new paper should not simply replace \(d\) by intrinsic dimension \(m\). The first-order tangent-space identity

\[
\operatorname{vol}_{\mathcal M}(S_T(x,y)\cap\mathcal M)
=
a_{m,T}r^m+o(r^m)
\]

is now considered the **baseline**.

The main goal is to characterize the departure from flatness:

\[
\boxed{
\operatorname{vol}_{\mathcal M}(S_T(x,y)\cap\mathcal M)
-
a_{m,T}r^m.
}
\]

We want to understand whether this deviation is controlled by the second fundamental form \(II_x\), edge direction \(u\), codimension, tangent orientation, local density derivatives, and template geometry.

The motivating interpretation is

\[
\boxed{
\text{flat ERG law}
+
\text{geometric perturbation}
=
\text{observable signature of manifold geometry}.
}
\]

## 2. Relation to the previous Unit-Region paper

The previous paper has the chain

\[
T
\longrightarrow
a_{d,T}
\longrightarrow
\text{Poisson void law}
\longrightarrow
\text{degree / incidence-length laws}.
\]

Paper 1 here should instead be organized as

\[
\boxed{
\text{flat unit-region law}
\longrightarrow
\text{tangent restriction}
\longrightarrow
\text{curvature/orientation correction}
\longrightarrow
\text{perturbed ERG statistics}.
}
\]

Therefore \(a_{m,T}r^m\) is a null model / first-order term. The main contribution is the first informative correction beyond that null model. Intrinsic-dimension inference is secondary. Merely recovering \(2^m\) for Gabriel is not a paper contribution.

## 3. Core geometric problem

### 3.1 Ambient template and tangent section

The exclusion region is constructed in ambient space:

\[
S_T(x,y)\subset\mathbb R^D.
\]

At small scales, the relevant flat object is the section induced on the tangent plane:

\[
S_T(x,y)\cap T_x\mathcal M.
\]

Define a tangent-section coefficient

\[
a_T(T_x\mathcal M,u)
=
\operatorname{vol}_m(
\text{normalized ambient template section in direction }u
).
\]

A major structural question is:

> For which ambient template classes is
> \[
> a_T(T_x\mathcal M,u)=a_{m,T}
> \]
> independent of tangent orientation and edge direction?

This suggests studying a class of templates stable under tangent restriction. Terminology should be frozen only after comparison with existing literature.

### 3.2 First-order theorem

Establish

\[
\operatorname{vol}_{\mathcal M}
(S_T(x,y)\cap\mathcal M)
=
a_T(T_x\mathcal M,u)r^m+o(r^m).
\]

For isotropic / tangent-stable templates this should reduce to

\[
a_{m,T}r^m+o(r^m).
\]

This theorem is necessary but not sufficient for the paper.

### 3.3 First non-flat correction

The principal target is an expansion

\[
\boxed{
\operatorname{vol}_{\mathcal M}
(S_T(x,y)\cap\mathcal M)
=
a_T(T_x\mathcal M,u)r^m
+
b_T(x,u)r^{m+q}
+
o(r^{m+q})
}
\]

where \(q\) must be derived.

If general templates produce an \(r^{m+1}\) term, characterize when symmetry cancels it. If symmetry forces \(q=2\), identify \(b_T(x,u)\) in terms of \(II_x\), \(u\), and template moments.

This is the theorem that would most clearly separate the paper from the earlier Euclidean framework.

## 4. Probability consequences

Once the geometric expansion is known,

\[
P(x\sim y\mid x,y)
\approx
\exp\left[
-nf(x)\operatorname{vol}_{\mathcal M}(S_T(x,y)\cap\mathcal M)
\right].
\]

Hence

\[
\log P(x\sim y\mid x,y)
=
-nf(x)a_T(T_x\mathcal M,u)r^m
-
nf(x)b_T(x,u)r^{m+q}
+\cdots.
\]

The goal is not merely to recover the tangent Poisson limit. Penrose–Yukich already supplies general tangent-space local limit machinery. We need the **explicit correction around that limit**.

## 5. Statistical / geometric consequences

### 5.1 Flat quantities as calibration

Use flat first-order quantities only as calibration:

\[
E[D\mid x]\approx c_{m,T},
\]

and incident-edge scale approximately

\[
[nf(x)a_{m,T}]^{-1/m}
\]

for tangent-stable templates.

### 5.2 Curvature-sensitive residuals

Investigate residual statistics such as

\[
\Delta_{\deg}(x)
=
E[D_n(x)]-c_{m,T},
\]

and transformed edge-length or void-probability residuals after subtracting the flat null.

Ask whether

\[
\Delta_{\deg}(x),\qquad
\Delta_R(x,u),\qquad
\Delta_{\text{void}}(x,u)
\]

encode contractions of \(II_x\), directional curvature, or reach.

### 5.3 Potential inverse problem

A stronger endpoint is

\[
\boxed{
\text{ERG local observables}
\Rightarrow
(m,\ f(x),\ \text{curvature information}).
}
\]

Conceptually:

\[
\text{leading exponent}\to m,
\]

\[
\text{leading scale}\to f(x),
\]

\[
\text{second-order / directional residual}\to\text{local curvature}.
\]

This is a target, not a current theorem.

## 6. Role of existing manifold limit theory

Penrose–Yukich (2013) is enabling machinery. It already supplies

\[
\text{local manifold score}
\to
\text{homogeneous Poisson score on }T_x\mathcal M.
\]

We should not re-prove or claim novelty for that principle.

Our contribution should be:

1. ERG-specific ambient-template geometry;
2. explicit tangent-section constants;
3. first non-flat departure from tangent geometry;
4. consequences for observable graph statistics.

If the final result is only "Penrose–Yukich applies to Gabriel/RNG," the project is too incremental.

## 7. Revised theorem stack

### Theorem A — tangent-section theorem

For an admissible ambient template \(T\),

\[
\operatorname{vol}_{\mathcal M}(S_T(x,y)\cap\mathcal M)
=
a_T(T_x\mathcal M,u)r^m+o(r^m).
\]

Characterize when

\[
a_T(T_x\mathcal M,u)=a_{m,T}.
\]

### Theorem B — curvature correction

Derive the first nonzero correction:

\[
a_T(T_x\mathcal M,u)r^m
+
b_T(x,u)r^{m+q}
+
o(r^{m+q}),
\]

with \(q\) determined by symmetry. Express \(b_T\) geometrically.

### Corollary C — perturbed void law

Translate Theorem B into a second-order asymptotic for edge probability.

### Corollary D — perturbed degree / edge-length statistics

Determine how curvature changes local expected degree, incident-edge radial intensity, moments / quantiles, and directional edge statistics.

### Theorem E — identifiability or estimation

If feasible, prove that one or more curvature quantities can be recovered from suitably normalized ERG observables.

This is preferable to making intrinsic dimension the headline estimator.

## 8. Simulation program

Use manifolds with analytically known geometry:

- flat manifolds as null controls;
- circles and spheres with varying radius;
- cylinders;
- tori with locations of different principal curvatures;
- paraboloids / quadratic patches;
- saddle surfaces.

Vary intrinsic dimension \(m\), ambient dimension \(D\), curvature magnitude/sign, direction relative to principal directions, template \(T\), density \(f\), and sample size \(n\).

Signature experiments should measure

\[
\frac{
\operatorname{vol}_{\mathcal M}(S_T\cap\mathcal M)-a_{m,T}r^m
}{
r^{m+q}
}
\]

against the predicted correction coefficient, then propagate the same correction into edge probability, degree bias, and edge-length residuals.

## 9. Minimum publishable package

The revised minimum is:

1. a nontrivial tangent-section theorem;
2. a first non-flat correction with geometric interpretation;
3. at least one explicit consequence for ERG probabilities/statistics;
4. simulations validating that correction across controlled manifolds/templates.

A paper that contains only the first-order tangent limit plus intrinsic-dimension estimation is no longer considered sufficient.

## 10. Out of scope

Still out of scope:

- persistent homology;
- Čech / Vietoris–Rips;
- topological reconstruction;
- graph-Laplacian / Laplace–Beltrami convergence;
- spectral manifold learning;
- UMAP/Isomap replacement;
- order-\(k_n\) continuum operators.
