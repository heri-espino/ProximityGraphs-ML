# Research Roadmap — Empty-Region Proximity Graphs on Manifolds

## 1. Research objective

Let
[
mathcal M^m\subset\mathbb R^D
]
be an unknown smooth (m)-dimensional manifold and let
[
X_1,ldots,X_n\stackrel{iid}{\sim} f,d\mathrm{vol}_{\mathcal M}.
]

For a fixed-template empty-region rule (T), an edge (x_i x_j) is retained when its associated region (S_T(x_i,x_j)) contains no other sample point.

The working thesis is that, at the (n^{-1/m}) spatial scale, the graph near a point (x\inmathcal M) should be governed by a homogeneous Poisson process on the tangent space (T_xmathcal M\simeq\mathbb R^m). If true under a useful template class, the same unit-region constant that controls the Euclidean graph should control local manifold degree and edge-length laws after replacing ambient dimension by intrinsic dimension.

This is a research hypothesis until proved.

## 2. Why the paper exists

Several ingredients already exist separately:

1. Euclidean empty-region/proximity-graph theory gives exact or asymptotic graph-size and degree results.
2. Stabilizing geometric probability provides LLNs/CLTs for local graph functionals.
3. Point-process limit theory on manifolds reduces many local statistics to Poisson processes on tangent spaces.
4. Graph statistics and nearest-neighbor distances are already used for intrinsic-dimension estimation.
5. Gabriel graphs have already appeared in manifold-learning algorithms.

Therefore the paper must **not** claim that proximity graphs, Gabriel graphs, or graph-based dimension inference are new.

The potential contribution is their synthesis into one explicit fixed-template ERG theory on manifolds:
[
T
\longrightarrow
a_{m,T}
\longrightarrow
\text{tangent-space Poisson ERG}
\longrightarrow
(D,R)
\longrightarrow
m.
]

## 3. Core definitions to settle

### Sampling model

Initial theorem setting:

- compact (C^2) manifold (mathcal M^m\subset\mathbb R^D);
- no boundary;
- positive reach (	au>0);
- density (f) continuous or Lipschitz;
- (0<f_{\min}\le f(x)\le f_{\max}<\infty).

These assumptions should be weakened only when a proof gives a clear reason.

### Template class

The admissible template (T) should support a similarity-copy representation of the candidate exclusion region, schematically
[
S_T(x,y)=x+rR_u T
]
after fixing a normalized endpoint configuration, with (r=|x-y|) and orientation (u).

Candidate assumptions:

- Borel measurability;
- translation equivariance;
- rotation equivariance or a controlled orientation rule;
- homogeneous scaling;
- finite positive (m)-volume;
- endpoint symmetry when the graph is undirected;
- boundary regularity sufficient for manifold-volume approximation;
- locality/stabilization sufficient for geometric-probability limit theory.

The exact minimal class is a research deliverable, not a naming exercise.

## 4. Theorem chain

### Target A — local manifold-volume lemma

For (y\to x) with (r=|x-y|),
[
\mathrm{vol}_{\mathcal M}(S_T(x,y)\cap\mathcal M)
=
a_{m,T}r^m+o(r^m).
]

Optional second-order target:
[
\mathrm{vol}_{\mathcal M}(S_T(x,y)\cap\mathcal M)
=
a_{m,T}r^m+b_T(x,u)r^{m+2}+o(r^{m+2}),
]
where (b_T) may encode the second fundamental form / curvature.

### Target B — tangent-space graph limit

After rescaling by (n^{1/m}) around (x), the local ERG should converge to the corresponding ERG of a homogeneous Poisson process of intensity (f(x)) on (T_xmathcal M).

Symbolically,
[
G_T(X_n)\stackrel{\mathrm{loc}}{\Longrightarrow}
G_T(\mathcal P_{f(x)}\subset T_x\mathcal M).
]

### Target C — scaled edge law

At (r_n=t n^{-1/m}),
[
P(x\sim y)
\to
\exp[-f(x)a_{m,T}t^m]
]
under the precise conditioning used by the theorem.

The paper must be exact about the difference between candidate-pair edge probability and the distribution of a randomly selected retained edge.

### Target D — degree law

At minimum,
[
E[D_n(x)]\to c_{m,T}.
]

For an isotropic similarity-copy template, investigate when
[
c_{m,T}=\frac{\kappa_m}{a_{m,T}},
qquad
\kappa_m=\frac{\pi^{m/2}}{\Gamma(m/2+1)}.
]

For the Gabriel template this reduces to the known Euclidean constant (2^m); the new contribution must be the manifold-limit framework and subsequent inference, not that identity.

### Target E — graph-size LLN

Seek
[
\frac{|E_n|}{n}\to\frac{c_{m,T}}2
]
in probability or almost surely under the chosen assumptions.

### Target F — intrinsic-dimension consistency

Construct at least one estimator (widehat m_n) from ERG observables and prove
[
widehat m_n\xrightarrow{P}m.
]

Asymptotic normality is desirable but not required for the minimal paper.

## 5. Statistical routes

### Degree route

If (m\mapsto c_{m,T}) is injective,
[
widehat m_{\deg}=c_T^{-1}(\bar D).
]

Gabriel provides the motivating special case
[
widehat m\approx\log_2 \bar D.
]

This identity has prior literature; our task is to determine a rigorous estimator, finite-sample behavior, and whether other templates offer better bias/variance tradeoffs.

### Edge-length route

The Euclidean fixed-template theory suggests a Weibull-type scaling. On a manifold the candidate local law is
[
nf(x)a_{m,T}R^m
\Rightarrow
\operatorname{Exp}(1),
]
for a carefully defined local edge-length variable (R).

Possible estimators:

- survival-slope / Weibull-plot estimator;
- moment-ratio estimator;
- likelihood estimator using local edge lengths;
- joint degree-length estimator separating (m) from (f(x)).

Every formula must be tied to the exact random-edge sampling scheme.

## 6. Simulation program

### Geometries

Use manifolds with known intrinsic dimension and controlled geometry:

- circles and spheres;
- flat / embedded tori;
- Swiss roll as a standard nontrivial embedding;
- higher-dimensional spheres;
- optionally products of spheres for richer curvature patterns.

### Factors

Vary:

- intrinsic dimension (m);
- ambient dimension (D);
- sample size (n);
- sampling density (f);
- reach / curvature;
- template (T).

### Main diagnostic figures

1. Local manifold-to-tangent-space schematic.
2. Theory vs empirical mean degree across (m) and templates.
3. Normalized edge-length data collapse.
4. Density invariance of degree vs density dependence of lengths.
5. Intrinsic-dimension RMSE vs (n).
6. Template bias/variance comparison.
7. Robustness to curvature, boundary, and small off-manifold noise.

### Signature data-collapse test

The most important empirical falsification test is whether
[
Z=nf(x)a_{m,T}R^m
]
collapses toward (operatorname{Exp}(1)) across different (n), (m), densities, and templates after using the correct edge notion.

If this fails systematically, revisit the theoretical object before adding more experiments.

## 7. Minimum publishable theorem package

The paper is not ready merely because simulations look good. A minimal coherent package is:

1. local tangent-space ERG limit;
2. local edge-probability / edge-length consequence;
3. degree expectation or distributional limit;
4. global edge-count LLN;
5. consistency of at least one intrinsic-dimension estimator.

A CLT, curvature correction, local-density estimator, or nonasymptotic error bound would strengthen the paper but is not required at the outset.

## 8. Follow-up papers, not Paper 1

### Possible Paper 2 — topology

Use ERG/RNG/Gabriel structure to reduce or calibrate topological constructions, persistent-homology birth scales, or topological reconstruction.

### Possible Paper 3 — manifold operators

Introduce order-(k_n) empty-region graphs with (k_n\to\infty) and (k_n/n\to0), then study graph-Laplacian convergence toward a differential operator such as the Laplace–Beltrami operator.

Do not let these directions dilute Paper 1 before its local stochastic theory is complete.
