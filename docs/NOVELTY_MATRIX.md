# Novelty Matrix — Paper 1

**Working title:** *Empty-Region Proximity Graphs on Manifolds: Local Limits and Intrinsic Dimension*  
**Status:** first-pass novelty audit, 2026-09-24  
**Purpose:** separate what is already known from what Paper 1 must genuinely contribute.

> **Important:** this document is a research audit, not a claim of priority.  
> "Potentially novel" means that the current core-literature audit has not found the same result in the same form. A final priority claim requires a broader citation search before submission.

---

## 1. Proposed object of study

Let

\[
\mathcal M^m\subset\mathbb R^D
\]

be a smooth \(m\)-dimensional manifold and let

\[
X_1,\ldots,X_n\stackrel{iid}{\sim} f\,d\operatorname{vol}_{\mathcal M}.
\]

For an admissible fixed-template / similarity-copy empty-region rule \(T\), retain the edge \(x_i x_j\) when

\[
S_T(x_i,x_j)\cap
\bigl(X_n\setminus\{x_i,x_j\}\bigr)=\varnothing.
\]

The Euclidean prior work motivates an intrinsic-dimensional template constant

\[
a_{m,T},
\]

and the candidate manifold theory is

\[
T
\longrightarrow
a_{m,T}
\longrightarrow
\text{tangent-space Poisson ERG}
\longrightarrow
\text{degree and edge-length laws}
\longrightarrow
\text{intrinsic-dimension inference}.
\]

The novelty question is **not** whether any one arrow exists somewhere in the literature. Several do. The question is whether the entire ERG-specific chain, with explicit fixed-template constants and statistical consequences, has already been developed on manifolds.

---

## 2. Legend

| Symbol | Meaning |
|---|---|
| **Yes** | The paper directly treats this ingredient. |
| **Partial** | Closely related, but not the same object/result. |
| **No** | Not a target/result of the paper, based on the present audit. |
| **Enabler** | Provides general machinery that may make one of our results a specialization/corollary rather than a new general theorem. |
| **High risk** | Strong overlap; our claim must be distinguished explicitly. |
| **Medium risk** | Related method/result, but a meaningful ERG-specific gap remains. |
| **Low risk** | Background or supporting machinery rather than direct overlap. |

---

# 3. Core novelty matrix

## 3.1 Empty-region and stochastic-geometry foundations

| Work | Data / geometry | Empty-region or fixed-template class | Manifold support | Tangent-Poisson principle | Degree / edge-count law | Edge-length law | Intrinsic-dimension inference | Role for Paper 1 | Novelty risk |
|---|---|---|---|---|---|---|---|---|---|
| **Gabriel & Sokal (1969)**, *A New Statistical Approach to Geographic Variation Analysis* | Planar geographic point sets | Gabriel criterion | No | No | No general stochastic degree theorem | No | No | Origin/statistical motivation for Gabriel graph | Low |
| **Matula & Sokal (1980)**, *Properties of Gabriel Graphs...* | Planar Gabriel graphs | Gabriel only | No | No | Structural/edge-density properties; average planar behavior is studied | No ERG radial law | No | Classical Gabriel properties; prevents us from presenting basic Gabriel density facts as new | Low–medium |
| **Toussaint (1980)**, *The Relative Neighbourhood Graph...* | Finite planar point sets | RNG | No | No | Structural inclusions/algorithms | No stochastic radial law | No | Definition and classical RNG structure | Low |
| **Jaromczyk & Toussaint (1992)**, *Relative Neighborhood Graphs and Their Relatives* | Euclidean proximity graphs | RNG and related families | No | No | Surveys graph size/properties | Not our probabilistic law | No | Historical/structural survey | Low |
| **Devroye (1988)**, *The Expected Size of Some Graphs in Computational Geometry* | \(n\) i.i.d. points with arbitrary density in \(\mathbb R^d\) | **Yes:** edge iff a set \(S(X_i,X_j)\) is empty; includes Gabriel, RNG, NN | **No** | No | **Yes:** asymptotic bounds and exact constants for expected edge count of sparse graphs, density-independent in important cases | No explicit Palm fixed-template edge-length distribution | No | **Closest Euclidean probabilistic predecessor** | **High** |
| **Cardinal, Collette & Langerman (2009)**, *Empty Region Graphs* | Finite point sets in the plane | **Yes:** explicit ERG framework with region as graph parameter | No | No | Structural conditions for bounded degree and other graph properties | No stochastic edge-length law | No | Establishes ERG terminology and general region-based abstraction | **High for definitions; low for manifold probability** |
| **Penrose & Yukich (2001)**, *Weak Laws in Geometric Probability* | Binomial point processes in \(\mathbb R^d\), possibly nonuniform | General stabilizing geometric functionals; examples include MST, \(k\)-NN, Voronoi, sphere-of-influence | No | Flat-space local Poisson machinery | **Yes:** LLNs for graph statistics including weighted edge length, degree counts, components | Weighted total edge length, not our fixed-template incident-edge law | No | General LLN machinery; an ERG LLN may be an instantiation if stabilization is verified | **High as enabling machinery** |
| **Penrose & Yukich (2001)**, *Central Limit Theorems for Some Graphs in Computational Geometry* | Homogeneous Poisson / uniform binomial point sets in expanding Euclidean regions | General stabilizing graph functionals | No | Flat-space stabilization | CLTs for graph functionals | Total graph functionals | No | CLT machinery if Paper 1 pursues asymptotic normality | Medium |
| **Espino (2026)**, *Unit-Region Factorization for Empty-Region Proximity Graphs* | Homogeneous Poisson geometry in flat \(\mathbb R^d\) | **Yes:** fixed-template / similarity-copy empty-region class | **No** | Flat Poisson only | **Yes:** mean Palm degree / edge intensity governed by \(a_{d,T}\) | **Yes:** Palm incident-edge radial intensity and normalized edge-length law; order-\(k\) variants | No manifold estimator | **Direct foundation of Paper 1; must be reused, not repackaged as new** | Internal prior work |
| **Espino (2026)**, *Stepping-Stone Diversion Neighborhoods...* | Euclidean \(\mathbb R^d\) | Specific stepping-stone template family | No | No | Supplies template volume constants | Geometry/volume rather than manifold statistics | No | Source of nontrivial \(a_{d,T}\) examples | Low |

### Main conclusion from this block

The following are **already occupied**:

\[
\text{empty-region graph abstraction},
\qquad
\text{Euclidean expected-size laws},
\qquad
\text{general stabilization LLN/CLT machinery},
\qquad
\text{flat fixed-template }a_{d,T}\text{ laws}.
\]

Paper 1 therefore cannot be sold as "a new general class of empty-region graphs" or "a new stochastic theory of proximity graphs in Euclidean space."

The natural gap is the **manifold-supported fixed-template specialization with explicit constants and explicit local probability laws**.

---

## 3.2 Manifold limit theory and intrinsic-dimension estimation

| Work | Manifold-supported data | Graph / local statistic | Local Poisson idea | Explicit ERG template constant \(a_{m,T}\) | Degree law used for \(m\) | Edge/distance law used for \(m\) | Consistency / CLT / rates | Direct implication for our novelty | Risk |
|---|---:|---|---:|---:|---:|---:|---|---|---|
| **Penrose & Yukich (2013)**, *Limit Theory for Point Processes in Manifolds* | **Yes**, \(m\)-dimensional \(C^1\) submanifolds of \(\mathbb R^d\) | General local score \(\xi(y,\mathcal Y)\) | **Yes — central theorem:** limits are controlled by homogeneous Poisson processes on tangent \(m\)-planes | No ERG-specific \(a_{m,T}\) theory | Not an ERG degree formula | Treats NN-based dimension estimator and other local statistics | **LLN, variance asymptotics, CLT** under locality/continuity/moment conditions | **The tangent-Poisson principle itself is NOT novel.** Our work must verify ERG hypotheses and extract new explicit ERG formulas | **Very high / Enabler** |
| **Brito, Quiroz & Yukich (2002)**, *Graph-Theoretic Procedures for Dimension Identification* | Euclidean dimension-identification setting | Average "reach" in \(k\)-NN graph | Probabilistic local geometry | No | Graph statistic, but not ERG degree | \(k\)-NN reach | Theoretical dimension-identification guarantees | "Use a graph statistic to infer dimension" is already old | High |
| **Brito, Quiroz & Yukich (2013)**, *Intrinsic Dimension Identification via Graph-Theoretic Methods* | **Yes**, \(m\)-dimensional \(C^1\) submanifold of \(\mathbb R^d\) | \(k\)-NN reach, common-neighbor statistic, MST squared-degree statistic | Stabilization | No | Uses graph topology/statistics, but not fixed-template ERG mean degree | NN graph structure rather than ERG incident-edge law | **Consistency and CLTs** for two graph-theoretic ID procedures on manifolds | "Graph-theoretic intrinsic dimension estimator with consistency/CLT" is not novel | **Very high** |
| **Levina & Bickel (2004)**, *Maximum Likelihood Estimation of Intrinsic Dimension* | Motivated by lower-dimensional manifold structure | Distances to close nearest neighbors | **Yes:** local Poisson-process approximation | No | No | **Yes:** NN-distance likelihood | Approximate bias/variance; later manifold LLN/CLT theory supplied by Penrose–Yukich | "Poisson local distances reveal \(m\)" is not novel | **Very high** |
| **Costa & Hero (2004)**, *Geodesic Entropic Graphs for Dimension and Entropy Estimation in Manifold Learning* | **Yes**, unknown smooth manifold | Entropic graphs; focus on geodesic MST | Geometric-probability asymptotics | No ERG unit-region factor | No | **Yes:** total graph-length scaling with sample size | **Asymptotically consistent** dimension/entropy estimator | "Graph edge lengths estimate manifold dimension" is not novel | **Very high** |
| **Costa, Girotra & Hero (2005)**, *Estimating Local Intrinsic Dimension with k-NN Graphs* | **Yes**, allows regions / collections with varying local dimension | \(k\)-NN graph | Local geometric scaling | No | No | \(k\)-NN graph length / neighborhood-based | Local ID methodology | Local dimension from graph neighborhoods is already established | High |
| **Giesen & Wagner (2004)**, *Shape, Dimension and Intrinsic Metric from Samples of Manifolds* | **Yes** | Adaptive neighborhood graph | Deterministic/local manifold geometry | No | No stochastic universal degree law | No ERG Palm law | Geometric reconstruction/dimension/intrinsic metric guarantees | Proximity-like adaptive graphs on manifolds already exist; our novelty must be probabilistic/template-specific | Medium |
| **Farahmand, Szepesvári & Audibert (2007)**, *Manifold-Adaptive Dimension Estimation* | **Yes** | Local distance/dimension procedure | Local sampling behavior | No | No | Local distances | **Finite-sample behavior** studied | Another established ID baseline; limits novelty of "new manifold ID estimator" alone | Medium–high |
| **Facco et al. (2017)**, *Estimating the Intrinsic Dimension... by Minimal Neighborhood Information* | **Yes / manifold motivation** | First- and second-NN distances (TwoNN) | Local uniform-density approximation | No | No | **Yes:** ratio of first/second NN distances; density effects largely cancel | Exact under ideal uniform assumptions; empirically robust/general consistency claims | Density-canceling distance ratios are not novel as a principle | High |
| **Kim, Rinaldo & Wasserman (2019)**, *Minimax Rates for Estimating the Dimension of a Manifold* | **Yes**, well-behaved manifolds | Includes TSP-length-based testing/estimation arguments | Not ERG-specific | No | No | Global geometric length enters upper bounds | **Minimax upper/lower rates** | Any estimator claim should be contextualized against statistical difficulty/rates | Medium |
| **Aamari & Levrard (2019)**, *Nonasymptotic Rates for Manifold, Tangent Space and Curvature Estimation* | **Yes** | Local polynomial geometric estimators | Local tangent approximation | No | No | No ERG law | Optimal/nonasymptotic rates for tangent, curvature, manifold estimation | Supplies geometric control for our volume lemma / possible curvature correction | Low / Enabler |
| **Niyogi, Smale & Weinberger (2008)**, *Finding the Homology of Submanifolds...* | **Yes** | Union-of-balls / sampling geometry | No ERG tangent-Poisson law | No | No | No | Sampling bounds in terms of condition number/reach-like geometry | Source for geometric regularity assumptions; topology itself is out of Paper 1 | Low |
| **Dyballa & Zucker (2023)**, *IAN* | **Yes**, potentially nonuniform/non-pure manifold data | **Starts from the Gabriel graph**, then adaptively sparsifies/weights | Heuristic/geometric local-volume reasoning | No general ERG \(a_{m,T}\) theory | **Yes:** explicitly observes Gabriel degree \(\approx 2^d\), largely density-independent, and uses dimensionality information | Not an explicit ERG Palm edge-length distribution | Algorithmic experiments / manifold-learning applications, not our proposed fixed-template asymptotic theorem | **Gabriel degree \(\approx2^m\) as a dimension idea is NOT new** | **Very high** |

---

# 4. Claims Paper 1 must NOT make

The current literature audit rules out the following broad novelty claims.

### 4.1 "We introduce empty-region graphs"

No. Cardinal et al. formalize **Empty Region Graphs**, and classical Gabriel/RNG work predates that terminology.

### 4.2 "We show proximity graphs can be used on manifolds"

Too broad. Giesen–Wagner, IAN, \(k\)-NN graph methods, entropic graphs, and many manifold-learning constructions already use geometric graphs on manifold-supported samples.

### 4.3 "We discover that local statistics on a manifold converge to tangent-space Poisson statistics"

No. This is essentially the organizing principle of Penrose–Yukich (2013) for a broad class of local scores.

### 4.4 "We estimate intrinsic dimension from graph statistics"

No. Brito–Quiroz–Yukich (2002, 2013) do this explicitly, including consistency and CLTs on manifolds.

### 4.5 "We estimate intrinsic dimension from local Poisson neighbor distances"

No. Levina–Bickel is a canonical predecessor, with later rigorous manifold limit theory in Penrose–Yukich.

### 4.6 "We estimate intrinsic dimension from graph edge lengths"

No. Costa–Hero use entropic graph / GMST length scaling to obtain asymptotically consistent manifold-dimension estimates.

### 4.7 "Gabriel degree is approximately \(2^m\) and can reveal intrinsic dimension"

Not as a standalone novelty claim. IAN explicitly studies this behavior and reports that Gabriel degree is approximately centered at \(2^d\) and largely insensitive to sampling density in its settings. The flat stochastic constant is also consistent with the earlier Euclidean Gabriel expected-size literature.

---

# 5. What still appears to be open / potentially novel

The strongest remaining contribution is **not** a generic dimension estimator. It is an explicit **fixed-template ERG theory on manifolds**.

## Candidate contribution A — manifold unit-region factorization

For an admissible template \(T\), prove a uniform local expansion of the form

\[
\boxed{
\operatorname{vol}_{\mathcal M}
\bigl(S_T(x,y)\cap\mathcal M\bigr)
=
a_{m,T}\,\|x-y\|^m
+
o(\|x-y\|^m)
}
\]

as \(y\to x\), with \(a_{m,T}\) equal to the same intrinsic-dimensional unit-region constant obtained by applying the normalized template in \(T_x\mathcal M\simeq\mathbb R^m\).

### Why this looks genuinely useful

Penrose–Yukich gives a general tangent-space limit principle, but it does not supply an ERG-specific factorization of the exclusion-region volume into an explicit template constant.

The result becomes much stronger if we can prove a uniform error bound, for example

\[
O\!\left(\frac{r^{m+2}}{\tau^2}\right)
\]

under positive reach / curvature control, or derive an explicit second-order curvature term

\[
a_{m,T}r^m+b_T(x,u)r^{m+2}+o(r^{m+2}).
\]

**Novelty assessment:** **strong candidate**, especially with a quantitative or second-order result.

---

## Candidate contribution B — explicit local ERG void law on a manifold

At the natural scale

\[
r_n=t\,n^{-1/m},
\]

derive

\[
\boxed{
\Pr(x\sim y\mid x,y)
\longrightarrow
\exp\!\left[-f(x)a_{m,T}t^m\right]
}
\]

under a precise conditioning regime.

This is more explicit than merely stating "the local process looks Poisson": it identifies exactly how **template geometry, intrinsic dimension, local density, and edge scale** interact.

However, if the proof is only "apply Penrose–Yukich," the contribution will look thin. It should be derived from the ERG-specific volume lemma and then integrated into the more general local-score framework.

**Novelty assessment:** **moderate by itself; strong as part of the full ERG factorization theorem.**

---

## Candidate contribution C — universal manifold degree constant for a template family

For the Palm/local limiting ERG, derive conditions under which

\[
\boxed{
\mathbb E[D_n(x)]
\longrightarrow
c_{m,T}
=
\frac{\kappa_m}{a_{m,T}}
}
\]

independently of \(f(x)\) at first order.

For Gabriel,

\[
c_{m,\mathrm{GG}}=2^m.
\]

The Gabriel special case alone is not enough because IAN already exploits approximately \(2^m\). The potentially new statement is the **entire fixed-template family**, with a rigorous manifold asymptotic and explicit \(a_{m,T}\).

**Novelty assessment:** **moderate–strong for the general ERG family; weak if presented only for Gabriel.**

---

## Candidate contribution D — manifold Palm incident-edge law

For a precisely defined **Palm incidence** (not an arbitrary "random edge"), seek

\[
\boxed{
nf(x)a_{m,T}R^m
\Rightarrow
\operatorname{Exp}(1)
}
\]

and therefore a Weibull-type radial law whose shape is \(m\).

This would be the manifold extension of the flat fixed-template incident-edge law.

Important distinction:

- candidate-pair edge probability;
- Palm incidence sampled according to incident-edge intensity;
- uniformly chosen edge from the finite graph;
- choose a vertex first and then choose uniformly among its incident edges;

are **not automatically the same distribution**.

The theorem must state exactly which object converges.

**Novelty assessment:** **strong candidate if no ERG-manifold version is found in the final search.**

---

## Candidate contribution E — joint degree/length separation of \(m\) and \(f(x)\)

The most interesting statistical angle may not be "another dimension estimator."

If

\[
\mathbb E[D\mid x]\approx c_{m,T}
\]

is first-order density-free, while

\[
R\sim
\text{scale determined by }
[nf(x)a_{m,T}]^{-1/m},
\]

then ERG topology and geometry may separate:

\[
\boxed{
\text{degree}
\;\rightsquigarrow\;
m,
\qquad
\text{edge lengths}
\;\rightsquigarrow\;
f(x)
}
\]

after \(m\) is estimated.

A joint estimator or identifiability theorem for

\[
(m,f(x))
\]

using **two observables from the same parameter-free ERG** would distinguish the work more clearly from existing NN-distance estimators.

**Novelty assessment:** **potentially strong**, but currently conjectural.

---

## Candidate contribution F — template-dependent statistical efficiency

Because different empty-region templates have different \(a_{m,T}\), sparsity, angular geometry, and sensitivity to curvature, one can ask whether

\[
T
\mapsto
\operatorname{Bias}_T(\widehat m),
\quad
\operatorname{Var}_T(\widehat m),
\quad
\operatorname{MSE}_T(\widehat m)
\]

has a systematic structure.

A particularly interesting hypothesis is a tradeoff:

\[
\text{more local / restrictive template}
\Rightarrow
\text{smaller curvature bias but larger sampling variance}.
\]

That would turn "we can use Gabriel/RNG/stepping-stone" into a real statistical theory of **template choice**.

**Novelty assessment:** **potentially strong and clearly differentiating**, if theory accompanies simulations.

---

# 6. The Penrose–Yukich issue: what is and is not ours

This is the most important positioning point.

Penrose–Yukich (2013) considers statistics

\[
\sum_{i=1}^n
\xi\!\left(
n^{1/m}Y_i,
\{n^{1/m}Y_j\}_{j=1}^n
\right)
\]

for local functionals \(\xi\), and proves LLNs, variance asymptotics, and CLTs under locality/continuity/moment assumptions. Their limiting behavior is controlled by homogeneous Poisson processes on the \(m\)-dimensional tangent hyperplanes.

Therefore:

### Not ours

\[
\boxed{
\text{local manifold functional}
\to
\text{tangent-space homogeneous Poisson functional}
}
\]

as a general principle.

### What can still be ours

1. Show that the **fixed-template ERG score** satisfies the required regularity/stabilization conditions.
2. Prove the **template-specific manifold-volume lemma**.
3. Identify the limiting functional explicitly in terms of \(a_{m,T}\).
4. Derive closed-form degree / incidence-length laws unavailable from the generic theorem alone.
5. Convert those explicit laws into ERG-specific statistical inference.
6. Quantify curvature / reach corrections if possible.

A paper that only says "Penrose–Yukich applies to Gabriel/RNG" is probably too incremental.

A paper that proves a reusable **ERG manifold factorization theorem** and then uses Penrose–Yukich to obtain global limit theory is substantially better positioned.

---

# 7. Highest-overlap papers and the exact distinction we need

| Prior work | What a referee may say | Required response in Paper 1 |
|---|---|---|
| **Devroye (1988)** | "Empty-set graphs with density-free asymptotic constants already exist." | Correct. Devroye is Euclidean. We extend a structured fixed-template class to manifold-supported data and identify intrinsic-dimensional tangent constants and local laws. |
| **Penrose–Yukich (2013)** | "Tangent Poisson limits on manifolds are already a general theorem." | Correct. We do not claim that principle. We establish ERG admissibility, explicit exclusion-volume factorization, and closed-form ERG consequences. |
| **Brito–Quiroz–Yukich (2013)** | "Consistent graph-theoretic manifold dimension estimators with CLTs already exist." | Correct. Our estimator is secondary; the primary object is the fixed-template ERG law. Any estimator must exploit the explicit template structure or offer a distinct property. |
| **Levina–Bickel (2004)** | "Local Poisson distance laws for estimating \(m\) are standard." | Correct. Our distances are not arbitrary NN radii: they are retained ERG incidences whose law is governed by a template exclusion constant. |
| **Costa–Hero (2004)** | "Graph lengths already estimate manifold dimension consistently." | Correct. They use global entropic/GMST length scaling. We study local empty-region incidence laws and template constants. |
| **IAN (2023)** | "Gabriel degree already tracks dimension and is density-adaptive." | Correct. We must not sell \(2^m\) as new. We seek a rigorous general-template asymptotic and possibly joint degree/length inference. |
| **Facco et al. (TwoNN)** | "Density cancellation using local distance ratios is already known." | Correct. A moment-ratio estimator alone is not a sufficient novelty claim; its value must come from the ERG law/template family or joint inference. |

---

# 8. Revised theorem stack for Paper 1

The current roadmap should be interpreted in the following order.

## Theorem A — geometric ERG manifold lemma

Establish the local exclusion-volume factorization

\[
\operatorname{vol}_{\mathcal M}
(S_T(x,y)\cap\mathcal M)
=
a_{m,T}r^m(1+o(1)).
\]

This should be proved directly and uniformly enough to support the stochastic limits.

**This is the most important theorem to make genuinely ours.**

## Theorem B — local pair/void asymptotics

For \(r_n=t n^{-1/m}\),

\[
\Pr(x\sim y\mid x,y)
\to
e^{-f(x)a_{m,T}t^m}.
\]

This should follow transparently from Theorem A plus binomial/Poisson local asymptotics.

## Theorem C — ERG local-score / Palm limit

Define an ERG score \(\xi_T\) and prove that its rescaled local law converges to the corresponding ERG score on a homogeneous Poisson process in \(T_x\mathcal M\).

Use Penrose–Yukich rather than reproving general stabilization theory whenever its hypotheses fit.

## Corollary D — explicit degree law

Derive

\[
E[D_n(x)]\to \frac{\kappa_m}{a_{m,T}}
\]

under the exact isotropy/similarity assumptions required.

## Corollary E — explicit incident-edge law

For the precisely defined Palm incidence,

\[
nf(x)a_{m,T}R^m
\Rightarrow \operatorname{Exp}(1).
\]

Derive moment identities only for that exact sampling scheme.

## Theorem F — statistical inference

Prove consistency of at least one ERG-specific estimator of \(m\).

A stronger version would jointly identify \(m\) and local \(f(x)\), or establish a template-dependent bias/variance comparison.

## Optional Theorem G — second order / curvature

If tractable,

\[
\operatorname{vol}_{\mathcal M}(S_T\cap\mathcal M)
=
a_{m,T}r^m
+
b_T(x,u)r^{m+2}
+
o(r^{m+2}).
\]

This could materially raise the mathematical contribution because it gives finite-sample bias structure rather than only a first-order tangent approximation.

---

# 9. Provisional novelty statement

A defensible **working** statement is:

> We study similarity-generated empty-region proximity graphs on random samples supported by a smooth manifold. Rather than introducing a new graph family or a new tangent-space Poisson principle, we derive an explicit fixed-template manifold factorization: locally, the exclusion geometry is governed by an intrinsic-dimensional unit-region constant \(a_{m,T}\). This yields explicit template-dependent void, degree, and Palm incident-edge laws on tangent spaces, and provides a basis for intrinsic-dimension and local-density inference from parameter-free proximity graphs.

Do **not** yet write "for the first time" or "the first theory" in the manuscript.

A stronger final statement becomes possible if the final search confirms that no prior paper derives the same fixed-template manifold ERG laws.

---

# 10. What would make the paper too weak

Paper 1 is at risk of being incremental if the final contribution is only:

1. apply Penrose–Yukich to the Gabriel graph;
2. recover \(E[D]\approx 2^m\);
3. define \(\widehat m=\log_2 \bar D\);
4. show simulations.

IAN already places Gabriel degree and dimension in the manifold-learning literature, while graph-based ID estimators with asymptotic theory already exist.

Likewise, a paper consisting only of a Weibull-slope dimension estimator would face Levina–Bickel, Costa–Hero, TwoNN, and graph-theoretic ID literature.

The paper becomes substantially more distinctive if it contains:

\[
\boxed{
\text{general template class}
+
\text{manifold unit-region theorem}
+
\text{explicit ERG laws}
+
\text{nontrivial statistical consequence}
}
\]

and especially if one of the following is achieved:

- quantitative curvature/reach error;
- joint \(m\) and \(f(x)\) inference;
- template efficiency/bias–variance theory;
- a general consistency/CLT statement specialized to the ERG family with explicit variance structure.

---

# 11. Literature roles for the manuscript

## Must cite in the main theoretical narrative

- Gabriel & Sokal (1969)
- Toussaint (1980)
- Devroye (1988)
- Cardinal, Collette & Langerman (2009)
- Penrose & Yukich (2001, weak laws)
- Penrose & Yukich (2013, manifold limit theory)
- Espino (2026), *Unit-Region Factorization...*

## Must cite in the intrinsic-dimension positioning

- Brito, Quiroz & Yukich (2002)
- Brito, Quiroz & Yukich (2013)
- Levina & Bickel (2004)
- Costa & Hero (2004)
- Facco et al. (2017)
- Dyballa & Zucker (2023)
- Kim, Rinaldo & Wasserman (2019)

## Geometric assumptions / proof support

- Niyogi, Smale & Weinberger (2008)
- Aamari & Levrard (2019)
- Giesen & Wagner (2004)

## Secondary / possible comparison sources

- Farahmand, Szepesvári & Audibert (2007)
- Costa, Girotra & Hero (2005)
- Matula & Sokal (1980)
- Jaromczyk & Toussaint (1992)
- relevant beta/gamma/stepping-stone references already in \`literature/pdf/\`

---

# 12. Verified bibliographic anchors

These are the main external anchors used in this first-pass audit.

| Work | DOI / bibliographic anchor |
|---|---|
| Devroye (1988) | 10.1016/0898-1221(88)90071-5 |
| Cardinal et al. (2009) | 10.1016/j.comgeo.2008.09.003 |
| Penrose & Yukich (2001), CLT | 10.1214/aoap/1015345393 |
| Penrose & Yukich (2013) | 10.1214/12-AAP897 |
| Brito et al. (2013) | 10.1016/j.jmva.2012.12.007 |
| Costa & Hero (2004) | 10.1109/TSP.2004.831130 |
| Costa, Girotra & Hero (2005) | 10.1109/SSP.2005.1628631 |
| Giesen & Wagner (2004) | 10.1007/s00454-004-1120-8 |
| Farahmand et al. (2007) | 10.1145/1273496.1273530 |
| Facco et al. (2017) | 10.1038/s41598-017-11873-y |
| Aamari & Levrard (2019) | 10.1214/18-AOS1685 |
| Kim, Rinaldo & Wasserman (2019) | 10.20382/jocg.v10i1a3 |
| Dyballa & Zucker (2023) | 10.1162/neco_a_01566 |

---

# 13. Immediate research decision

The novelty audit changes the emphasis of Paper 1.

### Old framing

\[
\text{proximity graphs}
\to
\text{intrinsic dimension estimator}.
\]

This is too close to existing literature.

### Revised framing

\[
\boxed{
\text{Euclidean fixed-template ERG factorization}
\to
\text{manifold exclusion-volume factorization}
\to
\text{explicit tangent ERG laws}
\to
\text{statistical consequences}
}
\]

Intrinsic-dimension estimation remains important, but it should be presented as a **consequence/application of the new stochastic-geometric theory**, not as the sole reason the paper exists.

---

# 14. Next actions after this matrix

1. **Formalize the admissible template class.**
2. Prove the local manifold-volume lemma before writing an estimator.
3. Check whether that lemma needs \(C^2\), positive reach, or weaker regularity.
4. Write the ERG local score \(\xi_T\) explicitly and verify Penrose–Yukich hypotheses.
5. Re-derive the flat Palm incidence law carefully so there is no ambiguity about what "random edge" means.
6. Derive degree and length consequences on the manifold.
7. Only then choose the intrinsic-dimension estimator.
8. Run a second, broader prior-art search focused specifically on:
   - "empty region graph manifold";
   - "Gabriel graph manifold asymptotic degree";
   - "relative neighborhood graph manifold stochastic";
   - "Palm edge length manifold geometric graph";
   - "stabilizing proximity graph manifold";
   - "empty ball / lune graph intrinsic dimension".
9. Before submission, convert this file from a first-pass audit into a citation-complete related-work table.

