# Novelty Matrix — Paper 1

**Revised framing:** *Curvature Corrections for Empty-Region Proximity Graphs on Manifolds*  
**Status:** revised after direct comparison with the prior Unit-Region paper, 2026-09-24.

> This file is a novelty audit, not a final priority claim.

## 1. Central correction to the project

The previous framing was too close to

Espino_2026_Unit-Region-Factorization-Empty-Region-Graphs.pdf.

That earlier work already develops the flat-space chain

\[
T
\longrightarrow
a_{d,T}
\longrightarrow
\text{Poisson void probability}
\longrightarrow
\text{degree / incident-edge laws}.
\]

A new paper whose main change is only

\[
d\longrightarrow m
\]

for manifold-supported samples risks being a specialization of the previous framework combined with existing tangent-space Poisson theory.

Therefore

\[
\boxed{
\operatorname{vol}_{\mathcal M}(S_T\cap\mathcal M)
=
a_{m,T}r^m+o(r^m)
}
\]

is now classified as **baseline / enabling**, not headline novelty.

The revised target is

\[
\boxed{
\text{How does nonzero curvature / ambient orientation perturb the flat unit-region law?}
}
\]

## 2. Matrix of overlap and remaining gap

| Literature / prior work | Flat template law | Manifold tangent limit | Curvature / \(II_x\) correction to ERG exclusion volume | Perturbed ERG degree / edge-length laws | Uses ERG residuals to infer geometry | Implication |
|---|---:|---:|---:|---:|---:|---|
| Gabriel & Sokal / Matula & Sokal | Special-case Gabriel geometry | No | No | Classical Gabriel properties | No | Historical background |
| Toussaint / RNG literature | Special-case proximity geometry | No | No | Structural properties | No | Historical background |
| Devroye (1988) | Euclidean empty-region expected-size asymptotics | No | No | Euclidean expected edge counts | No | Flat probabilistic predecessor |
| Cardinal et al. (2009) | General ERG abstraction | No | No | Structural ERG properties | No | Terminology / graph-class predecessor |
| Penrose & Yukich (2001) | Generic Euclidean stabilizing scores | No | No ERG-specific curvature term | LLN / CLT machinery | No | Enabling probability machinery |
| **Espino (2026), Unit-Region Factorization** | **Yes — explicit \(a_{d,T}\)** | No | **No** | **Yes — flat degree / Palm incident-edge laws** | No | **Direct prior work; first-order reuse is not enough** |
| Penrose & Yukich (2013) | Generic local scores | **Yes — tangent-space Poisson principle** | No explicit ERG/template correction | Generic LLN / variance / CLT | No | **Makes first-order tangent limit non-novel as a principle** |
| Brito–Quiroz–Yukich | No ERG template constant | Manifold setting | No | Graph statistics for dimension | Dimension, not curvature | Rules out generic graph-based dimension novelty |
| Levina–Bickel | No | Local Poisson approximation | No | NN-distance law | Dimension | Rules out generic local-Poisson dimension novelty |
| Costa–Hero | No ERG template constant | Manifold setting | No | Graph-length scaling | Dimension / entropy | Rules out generic graph-length dimension novelty |
| IAN (Dyballa–Zucker) | Gabriel specifically | Manifold-learning setting | No explicit differential-geometric correction | Gabriel degree used for dimension | Dimension / neighborhoods | Rules out \(2^m\) as novelty |
| Aamari–Levrard | No ERG | Tangent / curvature theory | Geometric tools, not ERG correction | No | Curvature estimation by other methods | Enabler for our expansion |
| Niyogi–Smale–Weinberger | No ERG | Manifold / reach sampling | No ERG correction | No | Topology | Geometric assumptions/background |
| **Proposed Paper 1** | Reuses flat \(a_{d,T}\) as null model | Reuses tangent limit as baseline | **Target: explicit template-dependent first non-flat correction** | **Target: propagate correction into ERG statistics** | **Target: determine what local geometry is identifiable** | **Main candidate novelty** |

## 3. Claims we should not make

Paper 1 should not claim novelty for:

- empty-region graphs as a class;
- fixed-template factorization in Euclidean space;
- tangent-space Poisson limits on manifolds;
- graph-based intrinsic-dimension estimation;
- local Poisson nearest-neighbor dimension estimation;
- dimension estimation from graph lengths;
- Gabriel degree \(\approx2^m\).

Those are prior art or direct consequences of prior work.

## 4. Baseline theorem versus real target

### Baseline

For \(r=\|x-y\|\to0\),

\[
\operatorname{vol}_{\mathcal M}
(S_T(x,y)\cap\mathcal M)
=
a_T(T_x\mathcal M,u)r^m+o(r^m).
\]

For sufficiently isotropic / tangent-stable templates,

\[
a_T(T_x\mathcal M,u)=a_{m,T}.
\]

This is necessary, but by itself it is too close to "Unit-Region + tangent plane."

### Real target

Determine the first nonzero departure:

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

where \(q\) must be derived rather than assumed.

The central questions are:

1. Is \(q=1\) generically?
2. Under what symmetry conditions does the odd-order term vanish so that \(q=2\)?
3. Can \(b_T(x,u)\) be expressed through the second fundamental form \(II_x\)?
4. Which contractions of \(II_x\) are visible to isotropic templates?
5. Can directional or anisotropic templates recover more information?

## 5. Ambient-template / tangent-section novelty

A point missing from the old framing is that the exclusion region lives in ambient space:

\[
S_T(x,y)\subset\mathbb R^D.
\]

The leading coefficient should therefore be defined through a tangent section:

\[
a_T(T_x\mathcal M,u)
=
\operatorname{vol}_m(
\text{normalized ambient template section}
).
\]

It is a research question whether the template family is stable under tangent restriction:

\[
a_T(T_x\mathcal M,u)
=
a_{m,T}
\]

for all tangent orientations and edge directions.

A classification theorem for templates satisfying this property could itself be substantive.

## 6. Why curvature changes the stochastic laws

The local void probability is approximately

\[
P(x\sim y\mid x,y)
\approx
\exp\left[
-nf(x)
\operatorname{vol}_{\mathcal M}(S_T(x,y)\cap\mathcal M)
\right].
\]

If

\[
\operatorname{vol}_{\mathcal M}
=
a r^m + b r^{m+q}+o(r^{m+q}),
\]

then

\[
\log P(x\sim y\mid x,y)
=
-nf(x)a r^m
-
nf(x)b r^{m+q}
+
o(nr^{m+q}).
\]

Thus the flat Unit-Region theory supplies the null law, while manifold geometry appears as a structured perturbation.

That is the conceptual distinction from the previous paper.

## 7. Candidate new consequences

### A. Curvature-induced degree bias

Instead of merely proving

\[
E[D_n(x)]\to c_{m,T},
\]

derive the leading finite-\(n\) correction

\[
E[D_n(x)]
=
c_{m,T}
+
\text{curvature-dependent term}
+
o(\cdot).
\]

### B. Curvature-induced edge-length distortion

Start from the flat Palm incidence law and derive how its transformed Exponential / Weibull law is perturbed by curvature.

### C. Directional geometry

Study whether edge direction \(u\) relative to principal curvature directions changes the correction.

### D. Template comparison

Different templates may respond differently to the same \(II_x\), creating a statistical design problem

\[
T
\mapsto
\text{curvature sensitivity / variance / robustness}.
\]

### E. Inverse geometry

A stronger endpoint is

\[
\text{leading exponent}\to m,
\qquad
\text{scale}\to f(x),
\qquad
\text{second-order residual}\to II_x\text{-information}.
\]

## 8. Referee test

A referee should not be able to summarize the paper as:

> "Take the authors' previous unit-region theory, replace \(d\) by intrinsic dimension \(m\), and invoke Penrose–Yukich."

If that sentence remains accurate, the paper is not ready.

The intended summary is:

> "The paper uses the authors' flat unit-region theory as a null model and derives how embedded-manifold geometry changes empty-region volumes and therefore proximity-graph statistics, with explicit template-dependent curvature / orientation corrections."

That is the standard the project should meet.

## 9. Provisional novelty statement

> We study how the differential geometry of a smooth embedded manifold perturbs fixed-template empty-region proximity graphs. The flat Euclidean unit-region laws provide a local null model, while the manifold induces template- and direction-dependent corrections through tangent sections and curvature. The main objective is to derive the first non-flat term in the exclusion-region volume expansion and propagate it to explicit corrections in edge probabilities, degree, and incident-edge statistics, thereby determining what local geometric information can be recovered from proximity-graph observables.

Do not yet use "first" or priority language in the manuscript.

## 10. Immediate proof target

Work in local coordinates

\[
\Phi(z)
=
x
+
z
+
\frac12 II_x(z,z)
+
O(\|z\|^3),
\qquad
z\in T_x\mathcal M.
\]

Then analyze

\[
\Phi^{-1}(S_T(x,y))
\]

and the induced volume form.

The next concrete derivation should use the **Gabriel template**, because its ambient exclusion region is a ball and its symmetry makes it the cleanest case for determining:

- the true correction order;
- which curvature invariant appears;
- whether directional dependence survives;
- what part generalizes to arbitrary templates.
