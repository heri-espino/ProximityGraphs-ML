# Literature Manual — Results, Sources, and Reuse Map

**Project:** ProximityGraphs-ML  
**Last updated:** 2026-09-24  
**Purpose:** provide a working mathematical manual extracted from the literature corpus. It records the results that matter for this project, where they come from, what assumptions they use, and how they may be reused.

> This document is a research guide, not a replacement for the original papers. Before citing a theorem formally, check its exact theorem number, hypotheses, notation, and version in the corresponding PDF.

---

# 0. Quick lookup: if we need X, read Y

| Need | Primary source in literature/pdf | What it gives |
|---|---|---|
| Definition/history of Gabriel graph | Gabriel-Sokal_1969_Statistical-Geographic-Variation.pdf | Diameter-ball empty-region rule and original statistical/geographical motivation |
| Classical Gabriel properties | Matula-Sokal_1980_Properties-Gabriel-Graphs.pdf | Planarity/basic structural results; planar expected-size antecedents |
| Definition/history of RNG | Toussaint_1980_Relative-Neighborhood-Graph.pdf | Empty lune rule for the relative neighborhood graph |
| Relations among MST/RNG/GG/Delaunay | Devroye_1988_Expected-Size-Computational-Geometry-Graphs.pdf; Jaromczyk-Toussaint_1992_Relative-Neighborhood-Graphs-Relatives.pdf | Classical inclusion chain and proximity-graph background |
| General Empty Region Graph abstraction | Cardinal_2009_Empty-Region-Graphs.pdf | ERG model, region as graph parameter, tight-region conditions for graph properties |
| Expected size of empty-region graphs under arbitrary density | Devroye_1988_Expected-Size-Computational-Geometry-Graphs.pdf | Density-robust asymptotic expected edge counts; explicit GG/RNG constants |
| Flat fixed-template Poisson laws | Espino_2026_Unit-Region-Factorization-Empty-Region-Graphs.pdf | \(a_K\), void probability, Palm incident-edge law, mean degree, normalized length law |
| Stepping-stone template constants | Espino_2026_Stepping-Stone-Diversion-Neighborhoods.pdf | \(a_{d,\alpha}\), 1-D volume integral, monotonicity, Gabriel/RNG limiting cases |
| Palm / Mecke / Slivnyak tools | Last-Penrose_2017_Lectures-Poisson-Process.pdf | Campbell-Mecke, Palm distributions, Mecke-Slivnyak theorem |
| LLN for stabilizing geometric graph functionals | Penrose-Yukich_2001_Weak-Laws-Geometric-Probability.pdf | General weak laws under stabilization, including edge length and degree statistics |
| CLT for stabilizing geometric graphs | Penrose-Yukich_2001_CLT-Computational-Geometry-Graphs.pdf | Asymptotic normality framework for graph functionals |
| Tangent-space Poisson limits on manifolds | Penrose-Yukich_2013_Limit-Theory-Point-Processes-Manifolds.pdf | LLN, variance asymptotics, CLT; local limit controlled by PPP on tangent \(m\)-planes |
| NN Poisson intrinsic-dimension MLE | Levina-Bickel_2004_Maximum-Likelihood-Intrinsic-Dimension.pdf | Local Poisson model and explicit nearest-neighbor MLE |
| TwoNN density-cancelling estimator | Facco_2017_TwoNN-Intrinsic-Dimension.pdf | Ratio \(R_2/R_1\) has Pareto law under local homogeneity |
| Graph-theoretic dimension estimators | Brito-Quiroz-Yukich_2002_Graph-Theoretic-Dimension-Identification.pdf; Brito-Quiroz-Yukich_2013_Intrinsic-Dimension-Graph-Theoretic-Methods.pdf | \(k\)-NN reach/common-neighbor/MST statistics; consistency and CLTs on manifolds |
| Graph-length dimension estimation | Costa-Hero_2004_Geodesic-Entropic-Graphs-Manifold-Dimension.pdf | GMST/geodesic graph length scaling identifies intrinsic dimension and Rényi entropy |
| Local dimension from \(k\)-NN graphs | Costa-Girotra-Hero_2005_Local-Intrinsic-Dimension-kNN-Graphs.pdf | Local intrinsic dimension on heterogeneous/manifold mixtures |
| Gabriel degree centering / density invariance | Devroye_1988_Expected-Size-Computational-Geometry-Graphs.pdf | Primary probabilistic source for the asymptotic \(2^d\) Gabriel mean-degree constant and its density robustness |
| Gabriel neighborhoods on manifolds | Dyballa-Zucker_2023_IAN-Manifold-Learning-Dimension.pdf | Reuses/interprets Gabriel degree behavior in manifold-learning neighborhoods; not the primary source of the \(2^d\) density-invariance result |
| Gabriel curvature-resolution observation | Dyballa-Zucker_2023_IAN-Manifold-Learning-Dimension.pdf | Explicit curvature threshold based on Gabriel geometry and sample spacing |
| Tangent/curvature estimation rates | Aamari-Levrard_2019_Manifold-Tangent-Curvature-Estimation.pdf | Nonasymptotic/minimax results for tangent spaces and second fundamental form |
| Reach/sampling assumptions | Niyogi-Smale-Weinberger_2008_Homology-Submanifolds-Random-Samples.pdf | Condition number/reach-style control, sampling complexity, noisy samples |
| Dimension/intrinsic metric from adaptive graph | Giesen-Wagner_2004_Shape-Dimension-Intrinsic-Metric-Manifolds.pdf | Adaptive neighborhood graph, dimension recovery, geodesic-distance approximation |
| Statistical difficulty of dimension estimation | Kim-Rinaldo-Wasserman_2019_Minimax-Rates-Manifold-Dimension.pdf | Minimax upper/lower rates; TSP-based upper-bound construction |
| Hyperspherical cap formulas | Li_2010_Hyperspherical-Cap-Area-Volume.pdf | Closed formulas useful for ball/lune/template intersections |

---

# 1. Core proximity-graph geometry

## 1.1 Gabriel graph

**Source:** Gabriel-Sokal_1969_Statistical-Geographic-Variation.pdf

For points \(p,q\in\mathbb R^d\), the Gabriel edge criterion is

\[
pq\in E_{\mathrm{GG}}
\iff
B\!\left(\frac{p+q}{2},\frac{\|p-q\|}{2}\right)
\cap (X\setminus\{p,q\})
=
\varnothing.
\]

The forbidden region is the ball having \(pq\) as diameter.

### Why it matters here

The Gabriel template is the cleanest first test for the manifold-curvature paper because:

- its ambient forbidden region is a Euclidean ball;
- it is isotropic;
- the tangent section is again a ball;
- symmetry makes cancellation of odd terms plausible;
- its flat expected degree has an explicit \(2^d\) law.

---

## 1.2 Relative neighborhood graph (RNG)

**Source:** Toussaint_1980_Relative-Neighborhood-Graph.pdf

For \(r=\|p-q\|\),

\[
pq\in E_{\mathrm{RNG}}
\iff
B(p,r)\cap B(q,r)
\]

contains no other sample point.

Equivalently, the forbidden region is the intersection of the two equal-radius balls centered at the endpoints: the lune.

Classically,

\[
\mathrm{MST}
\subseteq
\mathrm{RNG}
\subseteq
\mathrm{GG}
\subseteq
\mathrm{Delaunay}
\]

under the standard Euclidean definitions/general-position conventions.

**Useful sources:** Devroye (1988), Jaromczyk–Toussaint (1992).

### Why it matters here

The RNG gives a second highly symmetric but non-ball template. Comparing its manifold correction against Gabriel will tell us whether the curvature coefficient is universal or strongly template-dependent.

---

## 1.3 Empty Region Graphs (ERG)

**Source:** Cardinal_2009_Empty-Region-Graphs.pdf

Cardinal, Collette and Langerman formalize a family where an edge is determined by emptiness of a region associated to the pair:

\[
pq\in E
\iff
S(p,q)\cap(X\setminus\{p,q\})=\varnothing.
\]

Their main emphasis is structural. They give conditions on the defining region that imply properties such as:

- planarity;
- connectivity;
- triangle-freeness;
- cycle-freeness;
- bipartiteness;
- bounded degree.

They formulate these through **tight regions**: maximal/minimal region constraints associated with monotone graph properties.

### Terminology consequence

Use **Empty Region Graph (ERG)** as the established umbrella term. Our narrower fixed-template, similarity-copy, or future tangent-stable class must be presented as a subclass/structural condition.

---

# 2. Euclidean stochastic laws we inherit

## 2.1 Devroye's arbitrary-density empty-region asymptotics

**Source:** Devroye_1988_Expected-Size-Computational-Geometry-Graphs.pdf

Model:

\[
X_1,\dots,X_n\stackrel{iid}{\sim}f
\qquad\text{in }\mathbb R^d,
\]

with an edge if \(S(X_i,X_j)\) contains no other sample points.

Devroye proves density-robust asymptotic bounds for the expected number of edges, and exact asymptotic constants for sparse cases under suitable regularity.

### Gabriel result

For Gabriel, the unit forbidden-ball volume for an edge of length \(r\) is

\[
\frac{\kappa_d}{2^d}r^d.
\]

At almost every interior point \(x\),

\[
E[\deg(X_i)\mid X_i=x]
\longrightarrow
2^d.
\]

Thus the expected edge count has leading scale

\[
E|E_n|
\sim
2^{d-1}n
\]

for broad classes of densities; in the plane this gives the classical asymptotic \(2n\).

### RNG result in \(d=2\)

For the planar RNG, Devroye computes the lune constant and obtains asymptotic local degree

\[
2.557530243\ldots
\]

at almost every \(x\), with universal lower edge-count constant

\[
E|E_n|
\ge
(1.2787651215\ldots+o(1))n
\]

for arbitrary density.

### Key lesson

The cancellation of sampling density in expected local degree is not new. Our question is how curvature perturbs these flat constants.

---

## 2.2 Unit-region factorization

**Source:** Espino_2026_Unit-Region-Factorization-Empty-Region-Graphs.pdf

This is the direct flat-space predecessor.

For a similarity-copy empty region,

\[
\operatorname{Vol}_d S_K(p,q)
=
a_K r^d,
\qquad
r=\|p-q\|,
\]

where \(a_K\) is the normalized unit-region volume constant.

Let \(\mathcal P_\rho\) be a homogeneous Poisson process in \(\mathbb R^d\).

### Exact void probability

\[
P(p\sim q\mid r)
=
\exp(-\rho a_Kr^d).
\]

### Palm radial incidence intensity

Under the Palm distribution at the origin, the expected number of accepted neighbors in \([r,r+dr]\) is

\[
\rho\,d\kappa_d\,r^{d-1}
e^{-\rho a_Kr^d}\,dr.
\]

### Mean Palm degree

\[
E^0[D]
=
\frac{\kappa_d}{a_K}.
\]

For Gabriel,

\[
a_{\mathrm{GG}}
=
\frac{\kappa_d}{2^d},
\qquad
E^0[D_{\mathrm{GG}}]
=
2^d.
\]

### Normalized Palm incident-edge length

If \(R\) is sampled according to the normalized Palm incident-edge intensity,

\[
f_R(r)
=
d\rho a_Kr^{d-1}e^{-\rho a_Kr^d},
\]

hence

\[
\boxed{
\rho a_K R^d\sim\operatorname{Exp}(1).
}
\]

Its moments are

\[
E[R^q]
=
(\rho a_K)^{-q/d}
\Gamma\!\left(1+\frac qd\right).
\]

### Order-\(k\) extension

If acceptance means at most \(k-1\) points in the forbidden region and

\[
t=\rho a_Kr^d,
\]

then

\[
P(\text{accept}\mid r)
=
e^{-t}
\sum_{j=0}^{k-1}\frac{t^j}{j!},
\]

with

\[
E^0[D_k]
=
k\frac{\kappa_d}{a_K}.
\]

### Current-paper warning

These are inherited flat results. The manifold paper should use them as a null model rather than present them as new.

---

# 3. Stepping-stone templates

**Source:** Espino_2026_Stepping-Stone-Diversion-Neighborhoods.pdf

For parameter \(\alpha\),

\[
S_\alpha(p,q)
=
\left\{
z:
\|z-p\|^\alpha+\|z-q\|^\alpha
\le
\|p-q\|^\alpha
\right\}.
\]

The paper derives a normalized one-dimensional integral for

\[
a_{d,\alpha}
=
\frac{\operatorname{Vol}_d(S_\alpha(p,q))}
{\|p-q\|^d}.
\]

Anchor cases:

- \(\alpha=1\): degenerate segment / zero \(d\)-volume;
- \(\alpha=2\): Gabriel diameter ball;
- \(\alpha\to\infty\): relative-neighborhood lune.

The region/volume varies monotonically with the parameter and the paper establishes graph inclusions/connectivity consequences.

### Why it matters now

This gives a continuous family of possible curvature sensors:

\[
\alpha
\mapsto
b_{d,\alpha}(II_x,u).
\]

---

# 4. Poisson / Palm toolbox

## 4.1 Campbell-Mecke

**Primary source:** Last-Penrose_2017_Lectures-Poisson-Process.pdf

For a Poisson process \(\eta\) with intensity measure \(\lambda\),

\[
E\left[
\sum_{x\in\eta}
h(x,\eta)
\right]
=
\int
E\left[
h(x,\eta+\delta_x)
\right]
\lambda(dx).
\]

Use it for expected degree, edge count, incidence measures, pair sums, and order-\(k\) variants.

## 4.2 Slivnyak / Palm principle

For a homogeneous Poisson process, conditioning on a point at the origin leaves the rest of the process Poisson with the same law. The Palm configuration is the original process plus the distinguished point.

This is the correct interpretation of a "typical Poisson vertex."

## 4.3 Void probability

For measurable \(A\),

\[
P(\eta(A)=0)
=
e^{-\lambda(A)}.
\]

For homogeneous intensity \(\rho\),

\[
P(\eta(A)=0)
=
e^{-\rho\operatorname{Vol}(A)}.
\]

This is the exact bridge

\[
\text{forbidden-region geometry}
\longrightarrow
\text{edge probability}.
\]

---

# 5. Stabilization and geometric probability

## 5.1 Weak laws

**Source:** Penrose-Yukich_2001_Weak-Laws-Geometric-Probability.pdf

They prove a general weak law for stabilizing functionals of binomial point processes with possibly nonuniform density.

Applications include MST, \(k\)-NN, Voronoi and sphere-of-influence graphs. Functionals include weighted total edge length, numbers of vertices of specified degree, and numbers of components.

Schematic form:

\[
H_n
=
\sum_{i=1}^n
\xi(X_i,X_n),
\]

and, under stabilization/moment/regularity assumptions,

\[
\frac{H_n}{n}
\to
\int
E[\xi_\infty(\mathcal P_{f(x)})]f(x)\,dx.
\]

This is schematic; consult the original theorem for exact scaling and hypotheses.

### Use here

Do not re-prove a generic LLN if the ERG score satisfies the existing stabilization assumptions.

## 5.2 Central limit theorem

**Source:** Penrose-Yukich_2001_CLT-Computational-Geometry-Graphs.pdf

For suitable stabilizing graph functionals,

\[
\frac{H_n-EH_n}{\sqrt n}
\Rightarrow
N(0,\sigma^2)
\]

in the usual linear-variance regime.

Potential later use: asymptotic normality for curvature-sensitive ERG statistics.

---

# 6. Manifold local-limit theory

## 6.1 Penrose-Yukich manifold theorem

**Source:** Penrose-Yukich_2013_Limit-Theory-Point-Processes-Manifolds.pdf

Let \(Y_i\) be i.i.d. on an \(m\)-dimensional manifold

\[
\mathcal M\subset\mathbb R^d.
\]

They study rescaled local-score sums

\[
\sum_{i=1}^n
\xi
\left(
n^{1/m}Y_i,
\{n^{1/m}Y_j\}_{j=1}^n
\right).
\]

Under weak spatial dependence/stabilization, continuity and moment conditions they establish:

- weak laws;
- variance asymptotics;
- central limit theorems.

### Central geometric result

The limit is controlled by \(\xi\) evaluated on a homogeneous Poisson process on the \(m\)-dimensional tangent hyperplane at the sample point.

Symbolically,

\[
\text{local sample near }y
\Longrightarrow
\mathcal P_{f(y)}
\text{ on }T_y\mathcal M.
\]

### Novelty consequence

The first-order principle

\[
\text{manifold locally}
\to
\text{flat tangent-space PPP}
\]

is established prior art. Our paper must quantify the departure from this flat tangent limit.

---

# 7. Intrinsic-dimension estimators already occupied

## 7.1 Levina-Bickel MLE

**Source:** Levina-Bickel_2004_Maximum-Likelihood-Intrinsic-Dimension.pdf

Let \(T_j(x)\) be the distance from \(x\) to its \(j\)-th nearest neighbor. Locally approximate the point process as homogeneous Poisson.

The radial counting rate is

\[
\lambda(t)
=
f(x)\kappa_m\,m\,t^{m-1}.
\]

The local \(k\)-neighbor MLE is

\[
\boxed{
\widehat m_k(x)
=
\left[
\frac{1}{k-1}
\sum_{j=1}^{k-1}
\log\frac{T_k(x)}{T_j(x)}
\right]^{-1}.
}
\]

A \(k-2\) normalization is discussed as a first-order bias correction.

### Implication

Using local Poisson distance scaling to estimate \(m\) is established prior art.

---

## 7.2 TwoNN

**Source:** Facco_2017_TwoNN-Intrinsic-Dimension.pdf

Let

\[
\mu=\frac{R_2}{R_1}\ge1.
\]

Under local homogeneous Poisson sampling in intrinsic dimension \(m\),

\[
\boxed{
p(\mu)
=
m\mu^{-m-1},
\qquad \mu\ge1.
}
\]

Thus

\[
\log\mu\sim\operatorname{Exp}(m),
\]

and under the idealized independent-ratio likelihood,

\[
\widehat m
=
\left(
\frac1n\sum_i\log\mu_i
\right)^{-1}.
\]

### Implication

Density cancellation through local distance ratios is already a known principle.

---

## 7.3 Brito-Quiroz-Yukich

**Sources:** Brito-Quiroz-Yukich_2002_Graph-Theoretic-Dimension-Identification.pdf and Brito-Quiroz-Yukich_2013_Intrinsic-Dimension-Graph-Theoretic-Methods.pdf

The 2002 paper uses the average reach of vertices in a \(k\)-NN graph to identify dimension from interpoint distances.

The 2013 paper studies:

1. \(k\)-NN reach;
2. average squared degree in the MST;
3. common-neighbor counts in the \(k\)-NN graph.

For data on an \(m\)-dimensional \(C^1\) submanifold, they prove CLTs for the reach/common-neighbor statistics under general assumptions and consistency of the corresponding dimension-identification procedures.

### Implication

Graph-theoretic intrinsic dimension with consistency/CLTs on manifolds is already established.

---

## 7.4 Costa-Hero geodesic entropic graphs

**Source:** Costa-Hero_2004_Geodesic-Entropic-Graphs-Manifold-Dimension.pdf

For a smooth compact \(m\)-dimensional manifold and graph-length power \(\gamma\), geodesic MST length has leading growth

\[
n^{(m-\gamma)/m}.
\]

Their regression model is

\[
\boxed{
\log L_n
=
a\log n+b+\varepsilon_n,
\qquad
a=\frac{m-\gamma}{m},
}
\]

with asymptotically vanishing residual.

Thus

\[
m=\frac{\gamma}{1-a}.
\]

They construct asymptotically consistent estimators of intrinsic dimension and intrinsic Rényi entropy.

### Implication

Estimating dimension from graph-length scaling is prior art.

---

## 7.5 Costa-Girotra-Hero

**Source:** Costa-Girotra-Hero_2005_Local-Intrinsic-Dimension-kNN-Graphs.pdf

Extends graph-based dimension estimation to local/heterogeneous settings, including collections of manifolds with differing intrinsic dimensionalities.

### Implication

Local graph-based dimension estimation is not enough as a novelty claim.

---

## 7.6 Farahmand-Szepesvári-Audibert

**Source:** Farahmand_2007_Manifold-Adaptive-Dimension-Estimation.pdf

Nearest-neighbor dimension estimator with finite-sample analysis and emphasis on manifold-adaptive behavior, meaning sample complexity tied to intrinsic rather than ambient dimension.

---

## 7.7 Kim-Rinaldo-Wasserman

**Source:** Kim-Rinaldo-Wasserman_2019_Minimax-Rates-Manifold-Dimension.pdf

They derive minimax upper and lower bounds for estimating manifold dimension. Their upper-bound construction uses bounds on the traveling-salesman path through the sample.

### Implication

If dimension estimation reappears later, consistency alone is a weak statistical endpoint.

---

# 8. Gabriel graphs on manifolds: IAN is especially important

## 8.1 Scale-free neighborhoods

**Source:** Dyballa-Zucker_2023_IAN-Manifold-Learning-Dimension.pdf

IAN begins with a Gabriel graph because it avoids a fixed global radius or fixed \(k\), and provides locally adaptive neighborhoods. It then iteratively sparsifies/reweights the graph to reconcile discrete and continuous local-volume estimates.

## 8.2 Degree and local dimension: Devroye first, IAN later

The asymptotic Gabriel mean-degree constant and its robustness to the sampling density are **not an IAN result in origin**.

Devroye (1988) is the primary probabilistic source. For broad classes of i.i.d. densities in \(\mathbb R^d\), the Gabriel expected edge count has leading term

\[
E|E_n|
\sim
2^{d-1}n,
\]

which yields the asymptotic mean degree

\[
\boxed{
\frac{2E|E_n|}{n}
\to
2^d.
}
\]

The important point is that the leading constant is independent of the particular density \(f\) under the stated asymptotic conditions.

IAN later **reuses and interprets** this Gabriel behavior in a manifold-learning setting, reporting local degree behavior approximately centered near

\[
2^{d_i}
\]

for local intrinsic dimension \(d_i\), and using this as a scale-free dimensionality signal.

### Genealogy to cite

\[
\boxed{
\text{Devroye (1988): probabilistic }2^d\text{ centering / density robustness}
}
\]

\[
\boxed{
\text{IAN (2023): manifold-learning interpretation and algorithmic use}
}
\]

Do not cite IAN as the primary source for the density-invariance or \(2^d\) asymptotic constant.

### Technical caution

Keep separate:

- global expected mean degree;
- conditional local degree \(E[D\mid X=x]\);
- empirical finite-sample degree at a manifold point.

The exact hypotheses for each statement must be checked in the source before the manuscript equates them.

### Implication

Using \(m\approx\log_2\deg\) is not new, and the density robustness of the leading Gabriel degree constant belongs historically to the Euclidean stochastic-geometry literature rather than to IAN.

## 8.3 Curvature-resolution result

This is crucial for our revised paper.

IAN studies when Gabriel connectivity can represent a curved arc without incorrectly closing a chord.

For chord/diameter \(D\), it obtains a maximum geodesic curvature

\[
\boxed{
\kappa_{\max}
=
\frac{2}{D}.
}
\]

For uniform sampling with arc spacing \(T\),

\[
\boxed{
\kappa_{\max}(T)
=
\frac{\pi}{2T}.
}
\]

IAN interprets this as a curvature/reach resolution limitation of Gabriel neighborhoods.

### What remains different from our target

IAN gives a geometric validity/resolution threshold. It does not derive an asymptotic expansion of the form

\[
\operatorname{vol}_{\mathcal M}
(S_T(x,y)\cap\mathcal M)
=
a_{m,T}r^m+
b_T(II_x,u)r^{m+q}
+\cdots
\]

nor propagate such a coefficient into explicit perturbations of Palm degree or incident-edge distributions.

### Referee warning

Any curvature claim in our paper must explicitly distinguish itself from this IAN result.

---

# 9. Manifold geometry and reconstruction tools

## 9.1 Giesen-Wagner adaptive neighborhood graph

**Source:** Giesen-Wagner_2004_Shape-Dimension-Intrinsic-Metric-Manifolds.pdf

They introduce an adaptive neighborhood graph for a smooth manifold known only through a finite sample.

Under their sampling conditions:

- connected components and dimension can be correctly inferred;
- complexity depends exponentially on intrinsic dimension rather than ambient dimension;
- graph distances can approximate intrinsic/geodesic distances.

### Implication

Adaptive graph recovery of dimension/intrinsic metric is prior art.

---

## 9.2 Niyogi-Smale-Weinberger

**Source:** Niyogi-Smale-Weinberger_2008_Homology-Submanifolds-Random-Samples.pdf

They give high-probability sampling guarantees for recovering manifold homology from random samples, with bounds controlled by a condition number that limits curvature and nearness to self-intersection. They also treat noisy samples near the manifold.

### Use here

This is a standard justification for imposing a reach/condition-number lower bound so that local tangent approximations are geometrically meaningful.

---

## 9.3 Aamari-Levrard

**Source:** Aamari-Levrard_2019_Manifold-Tangent-Curvature-Estimation.pdf

They derive nonasymptotic rates and minimax lower bounds for estimating:

- the manifold;
- tangent spaces \(T_x\mathcal M\);
- the second fundamental form \(II_x\).

Their estimators use local polynomial approximations.

### Use here

Primary context for:

- local Monge expansions;
- assumptions controlling higher-order remainders;
- comparison if we later claim ERG-based curvature estimation.

---

# 10. Geometry formulas useful for template calculations

## 10.1 Unit ball constants

\[
\kappa_d
=
\frac{\pi^{d/2}}{\Gamma(d/2+1)},
\qquad
s_{d-1}=d\kappa_d.
\]

These constants enter the radial Palm integrals.

## 10.2 Hyperspherical caps

**Source:** Li_2010_Hyperspherical-Cap-Area-Volume.pdf

Provides concise formulas for areas/volumes of hyperspherical caps.

Potential use:

- ball-plane intersections;
- Gabriel local corrections;
- RNG lune decomposition;
- numerical checks of symbolic calculations.

---

# 11. Background sources retained for later

| Source | Possible use |
|---|---|
| Goldstein_2018_Normal-Bounds-Proximity-Region-Graphs.pdf | Quantitative normal approximation |
| Decreusefond_2014_Functional-Poisson-Approximation-Rubinstein.pdf | Functional Poisson approximation |
| Decreusefond_2016_Functional-Poisson-Approximation-KR-U-Statistics.pdf | Poisson approximation / U-statistics |
| Hirsch_2019_Lower-Large-Deviations-Geometric-Functionals.pdf | Large deviations |
| van-der-Vaart-Wellner_2023_Weak-Convergence-Empirical-Processes.pdf | Empirical-process arguments |
| Meester-Roy_1996_Continuum-Percolation.pdf | Connectivity/percolation regimes |
| Baccelli-Blaszczyszyn_2010_Stochastic-Geometry-Wireless-Networks-I.pdf | General Palm/stochastic geometry |
| Coupier_2019_Stochastic-Geometry-Modern-Research-Frontiers.pdf | Modern stochastic-geometry context |
| Duchemin-Castro_2022_Random-Geometric-Graphs-Developments.pdf | Random geometric graph survey |
| Devroye_2009_Maximum-Degree-Gabriel-Yao-Graphs.pdf | Maximum/extreme degree behavior |
| Bose_2013_k-Delaunay-k-Gabriel-Graphs.pdf | Higher-order Gabriel/Delaunay variants |
| Ceyhan_2010_Proximity-Regions-Higher-Dimensions.pdf | Higher-dimensional proximity regions |
| Veltkamp_1992_Gamma-Neighborhood-Graph.pdf | Parametric neighborhood families |
| Scholz_1996_Weibull-Plotting.pdf | Weibull diagnostics |

---

# 12. What the literature says our new paper must do

The corpus already supplies:

\[
\text{ERG definitions},
\]

\[
\text{flat expected-size laws},
\]

\[
\text{flat fixed-template Poisson/Palm laws},
\]

\[
\text{generic tangent-space Poisson limits},
\]

\[
\text{graph-based intrinsic-dimension estimators},
\]

and even a Gabriel-based curvature-resolution result.

Therefore the current paper should target

\[
\boxed{
\text{an explicit differential-geometric perturbation of an empty-region law}.
}
\]

Define

\[
V_T(x,u,r)
=
\operatorname{vol}_{\mathcal M}
\left(
S_T(x,x+ru+\cdots)\cap\mathcal M
\right).
\]

The desired expansion is

\[
V_T(x,u,r)
=
a_T(T_x\mathcal M,u)r^m
+
b_T(II_x,u)r^{m+q}
+
o(r^{m+q}).
\]

Then the void identity gives

\[
\log P(\text{edge}\mid x,u,r)
=
-\rho V_T(x,u,r),
\]

hence

\[
=
-\rho a_T r^m
-
\rho b_T r^{m+q}
+
o(r^{m+q}).
\]

The coefficient \(b_T\), and its consequences for degree/edge-length statistics, is the main gap suggested by this literature map.

---

# 13. Reading priority for the next proof

## Tier 1 — keep open while proving the first theorem

1. Espino_2026_Unit-Region-Factorization-Empty-Region-Graphs.pdf
2. Dyballa-Zucker_2023_IAN-Manifold-Learning-Dimension.pdf
3. Penrose-Yukich_2013_Limit-Theory-Point-Processes-Manifolds.pdf
4. Aamari-Levrard_2019_Manifold-Tangent-Curvature-Estimation.pdf
5. Last-Penrose_2017_Lectures-Poisson-Process.pdf
6. Li_2010_Hyperspherical-Cap-Area-Volume.pdf

## Tier 2 — positioning and consequences

7. Devroye_1988_Expected-Size-Computational-Geometry-Graphs.pdf
8. Cardinal_2009_Empty-Region-Graphs.pdf
9. Levina-Bickel_2004_Maximum-Likelihood-Intrinsic-Dimension.pdf
10. Facco_2017_TwoNN-Intrinsic-Dimension.pdf
11. Brito-Quiroz-Yukich_2013_Intrinsic-Dimension-Graph-Theoretic-Methods.pdf
12. Costa-Hero_2004_Geodesic-Entropic-Graphs-Manifold-Dimension.pdf

---

# 14. Terminology guardrails

- **Empty Region Graph (ERG):** established umbrella term.
- **fixed-template / similarity-copy:** narrower structural subclass from the prior Unit-Region work.
- **Palm incident-edge law:** use for the Palm incidence measure; do not call it simply a uniformly random finite-graph edge.
- **intrinsic dimension \(m\):** manifold dimension.
- **ambient dimension \(D\):** embedding-space dimension.
- **second fundamental form \(II_x\):** extrinsic curvature object.
- **reach:** geometric regularity/separation scale; not universally identical to a curvature radius.
- **tangent-space Poisson limit:** established Penrose-Yukich machinery.

---

# 15. Open literature questions

Before submission, verify specifically whether prior work already contains:

1. second-order curvature corrections to Gabriel/RNG empty-region probabilities on manifolds;
2. expansions of
   \[
   \operatorname{vol}_{\mathcal M}(B\cap\mathcal M)
   \]
   for edge-dependent off-center balls;
3. Palm degree expansions for geometric graphs on curved submanifolds;
4. curvature estimation from Gabriel/RNG degree or edge-length residuals;
5. anisotropic empty-region templates for identifying the second fundamental form.

Any such source should be added both here and to docs/NOVELTY_MATRIX.md.

---

# 16. Two unresolved PDFs

The corpus still contains:

- Unknown_nd_Unidentified-PDF.pdf
- Unknown_nd_Unidentified-Scanned-Article.pdf

They are excluded from this manual until identified. Do not attribute results to them by guesswork.
