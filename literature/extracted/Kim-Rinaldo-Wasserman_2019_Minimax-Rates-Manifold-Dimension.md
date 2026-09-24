---
id: "Kim-Rinaldo-Wasserman_2019_Minimax-Rates-Manifold-Dimension"
source_pdf: "../pdf/Kim-Rinaldo-Wasserman_2019_Minimax-Rates-Manifold-Dimension.pdf"
source_filename: "Kim-Rinaldo-Wasserman_2019_Minimax-Rates-Manifold-Dimension.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "full-page-ocr"
extraction_quality: "excellent"
extraction_score: 100.0
visual_assets: "disabled"
references_file: "../references/Kim-Rinaldo-Wasserman_2019_Minimax-Rates-Manifold-Dimension.references.md"
---

<!-- p:1 -->

## MINIMAX RATES FOR ESTIMATING THE DIMENSION OF A MANIFOLD

Jisu Kim,* Alessandro Rinaldo,† and Larry Wasserman‡

ABSTRACT. Many algorithms in machine learning and computational geometry require, as input, the intrinsic dimension of the manifold that supports the probability distribution of the data. This parameter is rarely known and therefore has to be estimated. We characterize the statistical difficulty of this problem by deriving upper and lower bounds on the minimax rate for estimating the dimension. First, we consider the problem of testing the hypothesis that the support of the data-generating probability distribution is a well-behaved manifold of intrinsic dimension d1 versus the alternative that it is of dimension d2, with d1 &lt; d2. With an i.i.d. sample of size n, we provide an upper bound on the probability of choosing the wrong dimension of O (n−(d2/d1−1-e)n), where € is an arbitrarily small positive number. The proof is based on bounding the length of the traveling salesman path through the data points. We also demonstrate a lower bound of Ω (n−(2d2-2d1+€)n), by applying Le Cam's lemma with a specific set of d1-dimensional probability distributions. We then extend these results to get minimax rates for estimating the dimension of well-behaved manifolds. We obtain an upper bound of order O (n−(−−1−€)n) and a lower bound of order Ω (n−(2+€)n), where m is the embedding dimension.

## 1 Introduction

Suppose that X1, ..., Xn is an i.i.d. sample from a distribution P whose support is an unknown, well-behaved, manifold M of dimension d in Rm, where 1 ≤ d ≤ m. Manifold learning refers broadly to a suite of techniques from statistics and machine learning aimed at estimating M or some of its features based on the data.

Manifold learning procedures are widely used in high dimensional data analysis, mainly to alleviate the curse of dimensionality. Such algorithms map the data to a new, lower dimensional coordinate system [Bellman, 1961, Lee and Verleysen, 2007a, Hastie et al.,

*Carnegie Mellon University, jisuk1@andrew. cmu. edu, supported by Samsung Scholarship and partially supported by NSF CAREER Grant DMS 1149677.

‡Carnegie Mellon University, larry@stat.cmu.edu

† Carnegie Mellon University, arinaldo@cmu.edu, partially supported by NSF CAREER Grant DMS 1149677.

<!-- p:2 -->


2009], with little loss in accuracy. Manifold learning can greatly reduce the dimensionality of the data.

Most manifold learning techniques require, as input, the intrinsic dimension of the manifold. However, this quantity is almost never known in advance and therefore has to be estimated from the data.

Various intrinsic dimension estimators have been proposed and analyzed; [see, e.g., Lee and Verleysen, 2007b, Koltchinskii, 2000, Kégl, 2003, Levina et al., 2004, Hein and Audibert, 2005, Raginsky and Lazebnik, 2005, Little et al., 2009, 2011, Sricharan et al., 2010, Rozza et al., 2012, Camastra and Staiano, 2016]. However, characterizing the intrinsic statistical hardness of estimating the dimension remains an open problem.

The traditional way of measuring the difficulty of a statistical problem is to bound its minimax risk, which in the present setting is loosely described as the worst possible statistical performance of an optimal dimension estimator. Formally, given a class of probability distribution P, the minimax risk Rn = Rn(P) is defined as

$$R _ { n } = \inf _ { \widehat { d } _ { n } } \sup _ { P \in \mathcal { P } } \mathbb { E } _ { P } \left [ 1 ( \widehat { d } _ { n } \ne d ( P ) ) \right ] .$$

In Equation (1.1), d(P) is the dimension of the support of P, Ep denotes the expectation with respect to the distribution P, 1(·) is the indicator function, and the infimum is over all estimators (measurable functions of the data) dn = dn(X1, . . . , Xn) of the dimension d(P). The risk EP[1(dn ≠ d(P))] of a dimension estimator dn is the probability that dn differs from the true dimension d(P) of the support of the data generating distribution P. The minimax risk Rn(P), which is a function of both the sample size n and the class P, quantifies the intrinsic hardness of the dimension estimation problem, in the sense that any dimension estimator cannot have a risk smaller than Rn uniformly over every P ∈ P.

The purpose of this paper is to obtain upper and lower bounds on the minimax risk Rn in (1.1). We impose several regularity conditions on the set of manifolds supporting the distribution in the class P, in order to make the problem analytically tractable and also to avoid pathological cases, such as space-filling manifolds. We first assume that the manifold supporting the data generating distribution P has two possible dimensions, d1 and d2. This assumption is then relaxed to any dimension d(P) between 1 and the embedding dimension m. Our main result is the following theorem. See Section 2 for the definition of the class P of probability distributions supported on well-behaved manifolds in Rm.

Theorem 1. The minimax risk Rn in (1.1) satisfies, an ≤ Rn ≤ bn, where

$$a _ { n } = ( C _ { K _ { I } } ^ { ( 1 7 ) } ) ^ { n } \min \{ \tau _ { \ell } ^ { - 4 } n ^ { - 2 } , 1 \} ^ { n } , \\$$

$$b _ { n } = ( C _ { K _ { 1 } , K _ { p } , K _ { v } , m } ^ { ( 1 5 ) } ) ^ { n } \max \left \{ 1 , \tau _ { g } ^ { - ( m ^ { 2 } - m ) n } \right \} n ^ { - \frac { n } { m - 1 } } ,$$

and the constants τl, τg, γ(17) and C(15) depend on P and are deined in Section 5. KI K1,Kp,Kv,m We now make a few remarks about the previous theorem.

<!-- p:3 -->


- Since the dimension d(P) is a discrete quantity, the minimax rate Rn in (1.1) is superexponential in sample size. This result seems at odds with the exponential rate obtained by [Koltchinskii, 2000, Proposition 2.1]. These different rates are due to different model assumptions. In [Koltchinskii, 2000] the data generating distribution is the convolution of a probability distribution supported on a manifold with a noise distribution supported on a set of full dimension m. In contrast, here we assume that the data are generated from a probability distribution supported on a manifold. Under our noiseless model, distributions supported on manifolds with different dimension are more easily distinguishable, hence the minimax rate Rn converges to 0 faster than under the model with noise assumed by [Koltchinskii, 2000].
- The key quantities that appear in the lower bound (1.2) and the upper bound (1.3) are the global reach τg and the local reach τe of the manifold, which are defined in Section 2. These reach parameters can be roughly thought as the inverse of the usual notion of curvature [see, e.g. Federer, 1959], and they affect the performance of any dimension estimator: a manifold with low reach may appear more space-filling than a manifold of the same dimension but with higher reach, thus making the task of resolving the dimension harder. Indeed, our analysis shows formally that the minimax risk Rn in (1.1) decreases in the values of the reaches. Given their crucial role, we have attempted to make the dependence of the minimax risk Rn on both τg and τe as explicit as possible.
- There is a gap between the lower bound (1.2) and the upper bound (1.3). Nonetheless, as far as we are aware, these are the most precise bounds on Rn that are available.

This paper is organized as follows. In Section 2, we formulate and discuss regularity conditions on distributions and their supporting manifolds. In Section 3, we provide an upper bound on the minimax rate by considering the traveling salesman path through the points. In Section 4, we derive a lower bound on the minimax rate by applying Le Cam's lemma with a specific set of d1-dimensional and d2-dimensional probability distributions. In Section 5, we extend our upper bound and lower bound for the case where the intrinsic dimension varies from 1 to m.

## 2 Definitions and Regularity Conditions

In this section, we define the set P of probability distributions that we consider in bounding the minimax risk Rn in (1.1). Such distributions are supported on manifolds whose dimension d is between 1 and m, where m is the dimension of the embedding space. In particular, we require that the supporting manifolds have a uniform lower bound on their reach parameters τg and τl. The resulting class of distributions is denoted by

<!-- p:4 -->


$$\mathcal { P } = \bigcup _ { d = 1 } ^ { m } \mathcal { P } _ { \tau _ { g } , \tau _ { \ell } , K _ { I } , K _ { v } , K _ { p } } .$$

are not interested in the details may skip the rest of the section. All the proofs for this section are in Section A.

### 2.1 Notation and Basic Definitions

For the reader's convenience, we provide a list of the notation used throughout the paper in Table 1.

We now briefly review some notations from differential geometry. For a more detailed treatment, we refer the reader to standard textbooks on this topic [see, e.g., Lee, 2000, 2003, Petersen, 2006, do Carmo, 1992]. A topological manifold of dimension d is a topological space M and a family of homeomorphisms φα : Uα ⊂ Rd → Vα ⊂ M from an open subset of Rd to an open subset of M such that Uφα(Uα) = M. A topological space α M is considered to be a d-dimensional manifold if there exists a family of homeomorphisms φα : Uα ⊂ Rd → Vα ⊂ M such that (M, {φα}α) is a manifold. If M is a d-dimensional manifold, such d is unique and is called the dimension of a manifold. If, for any pair α, β,

with φα(Uα) ∩φβ(Uβ) ≠ ∅, φ−1 0 φα : Uα ∩Uβ → Uα∩Uβ is Ck, then M is a Ck-manifold.

We assume that the topological manifold M is embedded in Rm, i.e. M ⊂ Rm, and the metric is inherited from the metric of Rm. For a topological manifold M ⊂ Rm and for any p, q ∈ M, a path joining p to q is a map γ : [a, b] → M for some a, b ∈ R such that γ(a) = p, γ(b) = q. The length of the curve γ is defined as Length(γ) = ∫a |γ′(t)|2dt. A topological manifold M is equipped with the distance distM : M × M → R as distM (p, q) = inf Length(γ). A path γ : [a, b] → M is a geodesic if for all t, t′ ∈ [a, b], γ: path joining p and q

distM(γ(t), γ(t′)) = |t − t′|.

Let TpM denote the tangent space to M at p. Given p ∈ M, there exist a set 0 ∈ ε ⊂ Tp(M) and a mapping expp : ε ⊂ TpM → M such that t → expp(tv), t ∈ (−1, 1), is the unique geodesic of M which, at t = 0, passes through p with velocity v, for all v ∈ ε. The map expp : ε ⊂ TpM → M is called the exponential map on p.

One of the key conditions that we impose in Section 2.3 is about the reach.

Definition 1. For a compact d-dimensional topological manifold M ⊂ Rm (with boundary), the reach of M, τ(M), is defined as the largest value of r &gt; 0 such that each x ∈ Rm with distRm (x, M) &lt; r has a unique projection πM(x) on M, i.e.

<!-- p:5 -->


Table 1: Table of notations and definitions.

| Notation                                                                                                                                                                                                                                                                    | Definition                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1( · ) d , d 1 , d 2 ̂ d n dist A ( · , · ) dist A, &#124;&#124;·&#124;&#124; ( · , · ) exp p ( · ) l ( · , · ) n m p , q vol A ( · ) B A ( x, r ) C a 1 ,...,a k I K I , K v , K p M P R n S n T T p M X 1 , . . . , X n M P γ π A ( · ) σ τ ( M ) τ g τ l ω d Π n 1 : n 2 | indicator function. dimension of a manifold. dimension estimator. distance function on the set A . distance function on the set A induced by the norm &#124;&#124; · &#124;&#124; . exponential map on point p ∈ M . loss function. size of the sample. dimension of the embedding space. points on the manifold M . volume function of A . open ball with center x and radius r , { y ∈ A : dist A ( y,x ) < r } . constant that depends only on a 1 , . . . , a k . cube [ - K I , K I ] m . fixed constants for regular conditions; see Definition 2. manifold. data generating probability distribution. minimax risk inf ̂ d n sup P ∈P E P [ 1 ( ̂ d n = d ( P ) )] ; see (1.1), (2.5), and (2.6). permutation group on { 1 , . . . , n } . subset of I n ⊂ ( R d ) n , used in Section 4. tangent space of a manifold M at p . sample points. set of manifolds; see Definition 2. set of distributions; see Definition 2. path on a manifold M . projection function onto a closed set A . permutation. reach of a manifold M ; see Definition 1 and Lemma 2. lower bound for global reach; see Definition 2. lower bound for local reach; see Definition 2. volume of the unit ball in R d , π d 2 Γ ( d 2 +1 ) . coordinate projection map: Π n 1 : n 2 ( x 1 , . . . , x d ) = ( x n 1 , . . . , x n d ) . |

$$\tau ( M ) \coloneqq \sup \{ r \colon \forall x \in \mathbb { R } ^ { m } \text { with } d i s t _ { \mathbb { R } ^ { m } } ( x , M ) < r , \\ \exists ! \pi _ { M } ( x ) \in M \ s . t . \ \| x - \pi _ { M } ( x ) \| _ { 2 } = \inf _ { y \in M } \| x - y \| _ { 2 } \} .$$

<!-- p:6 -->

τ(M)

M


x

πM(x)

τ(M)


x

(b) reach τ(M) in Lemma 2.

(a) reach τ(M) in Definition 1.

Figure 2.1: For a manifold M, there are several equivalent definitions for reach τ(M) in Definition 1. (a) The reach τ(M) is the supremum value of r such that for all x ∈ Rm with distRm (x, M) &lt; r has unique projection πM(x) to M, as in (2.2). (b) The reach τ(M) is the maximum radius of a ball that you can roll over the manifold M, as in (2.3).

See [Federer, 1959] for further details. The reach τ(M) can be also considered as one kind of curvature, and can be understood as an inverse of other usual curvatures. See Figure 2.1(a) for the illustration of Definition 1. There are several equivalent ways to define the reach τ(M) in (2.2) for the manifold M. The reach τ(M) is the maximum radius of a ball that can be rolled freely over the manifold M, as in Lemma 2. See Figure 2.1(b) for the illustration of Lemma 2.

Lemma 2. For a manifold M ⊂ Rm,

$$\tau ( M ) = \sup \{ r \colon \forall x \in M , \, \forall y \in \mathbb { R } ^ { m } \text { with } y - x \perp T _ { x } M \ a n d \ \| y - x \| _ { 2 } = r , \\ B _ { \mathbb { R } ^ { m } } ( y , r ) \cap M = \emptyset \} .$$

$$P r o o f \ o f \ L e m m a \ 2 \ \left [ \text {See Federal, 1959, Theorem 4.18} \right ] . & & \square$$

### 2.2 Minimax Theory

The minimax rate is the risk of an estimator that performs best in the worst case, as a function of the sample size [see, e.g. Tsybakov, 2008]. Let P be a collection of probability distributions over the same sample space X and let θ : P → Θ be a function over P taking values in some space Θ, the parameter space. We can think of θ(P) as the feature of interest of the probability distribution P, such as its mean, or, as in our case, the dimension of its support. For the fixed sample size n, suppose X = (X1, . . . , Xn) is an i.i.d. (independent and identically distributed) sample drawn from a fixed probability distribution P ∈ P. Thus X takes values in the n-fold product space χn = X × · · · × X and is distributed as P(n), the n-fold product measure. An estimator θn : Rn → Θ is any measurable function that maps the observation X into the parameter space Θ. Let l : Θ × Θ → R be a loss function, a non-negative bounded function that measures how different two parameters are. Then for a fixed estimator θn and a fixed distribution P, the risk of θn is defined as

<!-- p:7 -->


$$\mathbb { E } _ { P ^ { ( n ) } } \left [ \ell \left ( \widehat { \theta } _ { n } ( X ) , \theta ( P ) \right ) \right ] .$$

Then for a fixed estimator θn, its maximum risk is the supremum of its risk over every distribution P ∈ P, that is,

$$\sup _ { P \in \mathcal { P } } \mathbb { E } _ { P ^ { ( n ) } } \left [ \ell \left ( \widehat { \theta } _ { n } ( X ) , \theta ( P ) \right ) \right ] .$$

The minimax risk associated with P, θ, l and n is the maximal risk of any estimator that performs the best under the worst possible choice of P. Formally, the minimax risk is

$$R _ { n } = \inf _ { \widehat { \theta } _ { n } } \sup _ { P \in \mathcal { P } } \mathbb { E } _ { P ^ { ( n ) } } \left [ \ell \left ( \widehat { \theta } _ { n } ( X ) , \theta ( P ) \right ) \right ] .$$

The minimax risk Rn in (2.5) is often viewed as a function of the sample size n, in which case any positive sequence ψn such that limn→∞ Rn/ψn remains bounded away from 0 and ∞ is called a minimax rate. Notice that minimax rates are unique up to constants and lower order terms.

To define a meaningful minimax risk, it is essential to have some constraint on the set of distributions P in (2.4) and (2.5). If P is too large, then the minimax rate Rn in (2.5) will not converge to 0 as n goes to ∞: this means that the problem is statistically ill-posed. If P is too small, the minimax estimator depends too much on the specific distributions in P and is not a useful measure of a statistical difficulty.

Determining the value of the minimax risk Rn in (2.5) for a given problem requires two separate calculations: an upper bound on Rn and a lower bound. In order to derive an upper bound, one analyzes the asymptotic risk of a specific estimator θn. Lower bounds are instead usually computed by measuring the difficulty of a multiple hypothesis testing problem that entails identifying finitely many distributions in P that are maximally difficult to discriminate [see, e.g. Tsybakov, 2008, Section 2.2].

For the dimension estimation problem, we obtain an upper bound on Rn by analyzing the performance of an estimator based on the length of the traveling salesman problem, as described in Section 3. On the other hand, the calculation of the lower bound presents non-trivial technical difficulties, because probability distributions supported on manifolds of different dimensions are singular with respect to each other, and therefore trivially discriminable. In order to overcome such an issue, we resort to constructing mixtures of mutually singular distributions. We detail this construction in Section 4.

<!-- p:8 -->


Figure 2.2: A manifold M is assumed to be contained inside the cube I = [−K1, K1]m, for some K1 &gt; 0. See Definition 2.

2KI

W

There is a gap between the lower and upper bounds we derive on the minimax risk, as it is often the case in such calculations. Nonetheless, the derivation of the bounds is of use in understanding the difficulty of the dimension estimation problem.

### 2.3 Regularity conditions on the Distributions and their Supporting Manifolds

In our analysis we require various regularity conditions on the class P of probability distributions appearing in the minimax risk (1.1). Most of these conditions are of a geometric nature and concern the properties of the manifolds supporting the probability distributions in P. Altogether, our assumptions rule out manifolds that are so complicated to make the dimension estimation problem unsolvable and, therefore, guarantee that the minimax risk Rn in (2.5) converges to 0 as n goes to ∞. Such regularity assumptions are quite mild, and in fact allow for virtually all types of manifolds usually encountered in manifold learning problems.

Our first assumption is that the probability distributions in P are supported over manifold contained inside a compact set, which, without loss of generality, we take to be the cube I := [−K1, K1]m, for some KI &gt; 0. See Figure 2.2.

Second, to exclude manifolds that are arbitrarily complicated in the sense of having unbounded curvatures or of being nearly self intersecting, we assume that the reach is uniformly bounded from below. More precisely, we will constrain both the global reach and the local reach as follows. Fix τg, τe ∈ (0, ∞] with τg ≤ τl. The global reach condition for a manifold M is that the usual reach τ(M) in (2.2) is lower bounded by τg as in Figure 2.3(a), and the local reach condition is that M can be covered by small patches whose reaches are lower bounded by τe, as in Figure 2.3(b). (See Definition 2 below for more details.)

<!-- p:9 -->


Figure 2.3: A manifold M with (a) global reach at least τg, or (b) local reach at least τe. See Definition 2.

πUx(y)

x

Tg

Ux

M

x

y

τg

(a) global reach condition

(b) local reach condition

Third, we assume that the data are generated from a distribution P supported on a manifold M having a density with respect to the (restriction of the) Hausdorff measure on M bounded from above by some positive constant Kp.

For manifolds without boundary, the above conditions suffice for our analysis. However, to deal with manifolds with boundary, we need further assumptions, namely local geodesic completeness and essential dimension. A manifold M is said to be complete if any geodesic can be extended arbitrarily farther, i.e. for any geodesic path γ : [a, b] → M, there exists a geodesic γ : R → M that satisfies γl[a,b] = γ. [see, e.g., Lee, 2000, 2003, Petersen, 2006, do Carmo, 1992]. Accordingly, we define a manifold M to be locally (geodesically) complete, if any two points inside a geodesic ball of small enough radius in the interior of M can be joined by a geodesic whose image also lies on the interior of M.

Fifth, we assume the manifold M is of essential dimension d, in volume sense. If we fix any point p in the d-dimensional manifold M, then the volume of a ball of radius r grows in order of rd when r is small. By extending this, fix Kv ∈ (0, 2−m], and we say that the manifold M is of essential volume dimension d, if the volume of a geodesic ball of radius r around any point in M is lower bounded by Kvrdωd, for some positive constant Kv and all r small enough.

<!-- p:10 -->


We are now ready to formally define the class P of probability distributions that we will consider in our analysis of the minimax problem (1.1).

Definition 2. Fix τg, τl ∈ (0, ∞], KI ∈ [1, ∞), Kv ∈ (0, 2−m], with τg ≤ τl. Let Md be the set of compact d-dimensional manifolds M such that: τg,Te,K1,Kv

- (1) M ⊂ I := [−K1, K1]m ⊂ Rm;
- (2) M is of global reach at least τg, i.e. τ(M) ≥ τg, and M is of local reach at least τe, i.e. for all p ∈ M, there exists a neighborhood Up in M such that τ(Up) ≥ τe;
- (3) M is locally (geodesically) complete (with respect to τg): for all p ∈ int(M) and for all q1, q2 ∈ BM(p, 2√3τg), there exists a geodesic γ joining q1 and q2 whose image lies on intM;
- (4) M is of essential volume dimension d (with respect to Kv and τg): if for all p ∈ M and for all r ≤ √3τg, volM(BM(p, r)) ≥ Kvrdωd.

Let P = Pd be the set of Borel probability distributions P such that: Tg,Te,K1,Kv,Kp

- (5) P is supported on a d-dimensional manifold M ∈ Md τg,Te,K1,Kv;
- (6) P is absolutely continuous with respect to the restriction volM of the d-dimensional Hausdorff measure on the supporting manifold M and such that supx∈M dvo dP (x) ≤ Kp.

For every P ∈ Pd 9,τe,K1,Kv,Kp, denote the dimension of its distribution as d(P).

Remark 1. For manifolds without boundary, the local completeness condition and the essential volume dimension condition in Definition 2 always hold. The Hopf Rinow Theorem [see, e.g. Petersen, 2006, Theorem 16] implies that any compact closed manifold without boundary is geodesic complete, which implies it is locally complete in the sense of (3) in Definition 2. Also, [Niyogi et al., 2008, Lemma 5.3] implies that, for a d-dimensional manifold M and all 0 &lt; r ≤ 2τ(M),

$$\ v o l _ { M } ( B _ { M } ( p , r ) ) \geq r ^ { d } \left ( 1 - \left ( \frac { r } { 2 \tau ( M ) } \right ) ^ { 2 } \right ) ^ { \frac { d } { 2 } } \omega _ { d } ,$$

for all p ∈ M. Hence, when, for fixed τg &gt; 0, a d-dimensional manifold M (without boundary) satisfies τ(M) ≥ τg, then for any 0 &lt; r ≤ √3τg, volM(BM(p, r)) ≥ 2−drdωd, so the essential volume dimension condition is satisfied.

<!-- p:11 -->


Remark 2. The notion of the local reach τe in Definition 2 is less standard than the global reach τg, which is the usual definition of the reach in [see, e.g. Federer, 1959]. The local reach condition is only used in getting the lower bound of the minimax rate Rn in Section 4, while the global reach condition is used in both Section 3 and Section 4. In fact, the reach of the manifold is determined either by a bottleneck structure or an area of high curvature, as in [Aamari et al., 2017, Theorem 3.4]. And the global reach condition is imposing regularities on both cases, while the local reach condition is imposing regularities only on the latter case, i.e. on the local curvature. Setting the local reach τe equal to the global reach τg reduces to the model that has conditions only on the usual reach.

The regularity conditions in Definition 2 imply further constraints on both the distributions in P and their supporting manifolds, in Lemma 3, 4, and 5. Such properties are exploited in Section 3 and 4. The proofs for Lemma 3, 4, and 5 are in Appendix A.

Lemma 3. Fix τg ∈ (0, ∞], and let M be a d-dimensional manifold with global reach ≥ τg. For r ∈ (0, τg), let Mr := {x ∈ Rm : distRm,(x, M) &lt; r} be an r-neighborhood of M in Rm. Then, the volume of M is upper bounded as

$$v o l _ { M } ( M ) \leq \frac { m ! } { d ! } r ^ { d - m } v o l _ { \mathbb { R } ^ { m } } ( M _ { r } ) .$$

Further, fx τl ∈ (0, ∞], K1 ∈ [1, ∞), Kv ∈ (0, 2−m], with τg ≤ τl, and suppose M ∈ Md 1 g,τe,K1,Kv· Then the volume of M is upper bounded as

$$\ v o l _ { M } ( M ) \leq C _ { K _ { I } , m } ^ { ( 3 ) } \max \left \{ 1 , \tau _ { g } ^ { d - m } \right \} ,$$

where is a constant depending only on K1 and m. K1,m

Lemma 4. Fix τg, τl ∈ (0, ∞], K1 ∈ [1, ∞), Kv ∈ (0, 2−m], with τg ≤ τl. Let M ∈ . . ., BM (pN, r), with

$$N \leq \left \lfloor \frac { 2 ^ { d } v o l ( M ) } { K _ { v } r ^ { d } \omega _ { d } } \right \rfloor \, .$$

Lemma 5. Fix τg, τl ∈ (0, ∞], K1 ∈ [1, ∞), Kv ∈ (0, 2−m], with τg ≤ τl. Let M ∈ Md and let exppk : Ek ⊂ Rm → M be an exponential map, where Ek is the τg,Te,K1,Kv domain of the exponential map exppk and TpkM is identified with Rd. For all v, w ∈ Ek, let Rk := max{||v||, ||ω||}. Then

$$\| \exp _ { p _ { k } } ( w ) - \exp _ { p _ { k } } ( w ) \| _ { \mathbb { R } ^ { m } } \leq \frac { \sinh ( \sqrt { 2 } R _ { k } / \tau _ { \ell } ) } { \sqrt { 2 } R _ { k } / \tau _ { \ell } } \| v - w \| _ { \mathbb { R } ^ { d } } .$$

<!-- p:12 -->


Under these regularity conditions, the minimax risk Rn is defined as

$$R _ { n } = \inf _ { \widehat { d } _ { n } } \sup _ { P \in \mathcal { P } } \mathbb { E } _ { P ^ { ( n ) } } \left [ 1 \left ( \widehat { d } _ { n } ( X ) \neq d ( P ) \right ) \right ] ,$$

where in Section 3 and 4 we fix d1, d2 ∈ N with 1 ≤ d1 &lt; d2 ≤ m and define

$$\mathcal { P } = \mathcal { P } _ { \tau _ { g } , \tau _ { \ell } , K _ { I } , K _ { v } , K _ { p } } \bigcup \mathcal { P } _ { \tau _ { g } , \tau _ { \ell } , K _ { I } , K _ { v } , K _ { p } } ^ { d _ { 1 } } ,$$

and in Section 5 we set instead

$$\mathcal { P } = \bigcup _ { d = 1 } ^ { m } \mathcal { P } _ { \tau _ { g } , \tau _ { \ell } , K _ { I } , K _ { v } , K _ { p } } .$$

In (2.6), λn is any dimension estimator based on data X = (X1, . . , Xn), and the loss function l(·, ·) is 0 − 1 loss, so for all x, y ∈ R, l(x, y) = 1(x ≠ y).

## 3 Upper Bound for Choosing Between Two Dimensions

In this section we provide an upper bound on the minimax rate Rn in (2.6) when d(P) can only take two known values. Fix d1, d2 ∈ N with 1 ≤ d1 &lt; d2 ≤ m, and assume that the data are generated from a distribution P ∈ P such that either d(P) = d1 or d(P) = d2 as in (2.7). In this case, the minimax risk quantifies the statistical hardness of the hypothesis testing problem of deciding whether the data originate from a d1 or d2-dimensional distribution. In Section 5 we will relax this assumption and allow for the intrinsic dimension d(P) to be any integer between 1 and m as in (2.8). All the proofs for this section are in Section B.

Our strategy to derive an upper bound on Rn is to choose a particular estimator dn and then derive a uniform upper bound on its risk over the class P in (2.7), i.e. an upper bound for the quantity

$$\sup _ { P \in \mathcal { P } } \mathbb { E } _ { P ^ { ( n ) } } \left [ 1 \left ( \widehat { d } _ { n } ( X ) \neq d ( P ) \right ) \right ] ,$$

where P(n) denotes the n-fold product of P. This will in turn yield an upper bound on the minimax risk Rn, since

$$R _ { n } = \inf _ { \widehat { d } _ { n } } \sup _ { P \in \mathcal { P } } \mathbb { E } _ { P ^ { ( n ) } } \left [ 1 \left ( \widehat { d } _ { n } ( X ) \neq d ( P ) \right ) \right ] \leq \sup _ { P \in \mathcal { P } } \mathbb { E } _ { P ^ { ( n ) } } \left [ 1 \left ( \widehat { d } _ { n } ( X ) \neq d ( P ) \right ) \right ] .$$

Naturally, choosing an appropriate estimator is critical to get a sharp bound. In Section 3.1, we define our dimension estimator dn and analyze its risk. From that analysis, we derive an upper bound on the minimax risk Rn in (2.6) in Section 3.2.

<!-- p:13 -->


### 3.1 Dimension Estimator and its Analysis

Our dimension estimator dn is based on the d1-squared length of the TSP (Traveling Salesman Path) generated by the data. The d1-squared length of the TSP generated by the data is the minimal d1-squared length of all possible paths passing through each sample point Xi once, which is

$$\min _ { \sigma \in S _ { n } } \left \{ \sum _ { i = 1 } ^ { n - 1 } \| X _ { \sigma ( i + 1 ) } - X _ { \sigma ( i ) } \| _ { \mathbb { R } ^ { m } } ^ { d _ { 1 } } \right \} .$$

Then, λn = d1 if and only if the d1-squared length of the TSP is below a certain threshold; that is

$$\widehat { d } _ { n } ( X ) \coloneqq \begin{cases} d _ { 1 } , & i f \ \min \left \{ \sum _ { i = 1 } ^ { n - 1 } \| X _ { \sigma ( i + 1 ) } - X _ { \sigma ( i ) } \| _ { \mathbb { R } ^ { m } } ^ { d _ { 1 } } \right \} \leq C _ { K _ { 1 } , K _ { v } , m } ^ { ( 7 ) } \max \left \{ 1 , \tau _ { g } ^ { d _ { 1 } - m } \right \} , \\ d _ { 2 } , & \text {otherwise} . \end{cases}$$

γ(7) where is a constant to be defined later. K1,Kv,m

We begin our analysis of the estimator dn with Lemma 6, which shows that λn d2 −1)n makes an error with probability of order O n (d1 if the correct dimension is d2. Specifically, we demonstrate that, for any pòsitive value L, the d1-squared length of a n-1 piecewise linear path from X1 to Xn, ∑∥Xi+1 − Xil ldm, is upper bounded by L with a d1 i=1 d2 −1)n very small probability of order O n d1 as in (3.5). Hence the d1-squared length o     o  o  o e d  o

Lemma 6. Fix τg, τl ∈ (0, ∞], K1 ∈ [1, ∞), Kv ∈ (0, 2−m], Kp ∈ [(2K1)m, ∞), d1, d2 ∈ N, with τg ≤ τe and 1 ≤ d1 &lt; d2 ≤ m. Let X1, . .., Xn ∼ P ∈ Pd2 τg,Te,K1,Kv,Kp Then for all L &gt; 0,

$$P ^ { ( n ) } \left [ \sum _ { i = 1 } ^ { n - 1 } \| X _ { i + 1 } - X _ { i } \| _ { \mathbb { R } ^ { m } } ^ { d _ { 1 } } \leq L \right ] \leq \frac { \left ( C _ { K _ { 1 } , K _ { p } , m } ^ { ( 6 ) } \right ) ^ { n - 1 } L ^ { \frac { d _ { 2 } } { d _ { 1 } } ( n - 1 ) } \max \left \{ 1 , \tau _ { g } ^ { ( d _ { 2 } - m ) ( n - 1 ) } \right \} } { ( n - 1 ) ^ { \left ( \frac { d _ { 2 } } { d _ { 1 } } - 1 \right ) ( n - 1 ) } ( n - 1 ) ! } ,$$

where ~(6) is a constant depending only on K1, Kp, and m. K1,Kp,m

Proof of Lemma 6. in Appendix B.

Next, Lemma 7 shows that the estimator ∂n in (3.4) is always correct when the intrinsic dimension is d1, as in (3.6). Specifically, the d1-squared length of the TSP path Xσ(1)

<!-- p:14 -->

Xσ(n)

Xσ(3)

Yn-1

●

Xσ(2)

Y2

Yn−2

Xσ(n−1)

M

Y1

Xσ(n−2)

∑Yi ≤ volM(M)

Figure 3.1: When the manifold is a curve, the length of the TSP path n−1 min Σ∥Xσ(i+1) − Xσ(i)lRm  in (3.3) is upper bounded by the length of the curve σ∈Sn (i=1 volM(M).

~(7) in (3.3) is bounded by some positive threshold C i: (  d      :rs     =   ) upper bounded by the length of curve volM(M), as in Figure 3.1. This fact, combined n max {1, τ1−m }, yields the result. In K1,m ~(7) γ(3) can be set as K1,Kv,m K1,Kv,m K1,m

When d1 &gt; 1, Lemma 7 is proved using Lemma 3, 4 and 5, along with the Hölder continuity of a d1-dimensional space-filling curve [Steele, 1997, Buchin, 2008].

Lemma 7. Fix τg, τl ∈ (0, ∞], KI ∈ [1, ∞), Kv ∈ (0, 2−m], d1 ∈ N, with τg ≤ τl. Let M ∈ Md1 1τg,Te,Kp,Kv and X1, . . . , Xn ∈ M. Then

$$\min _ { \sigma \in S _ { n } } \sum _ { i = 1 } ^ { n - 1 } \| X _ { \sigma ( i + 1 ) } - X _ { \sigma ( i ) } \| _ { \mathbb { R } ^ { m } } ^ { d _ { 1 } } \leq C _ { K _ { 1 } , K _ { v } , m } ^ { ( 7 ) } \max \left \{ 1 , \tau _ { g } ^ { d _ { 1 } - m } \right \} ,$$

where C(7) is a constant depending only on K1, Kv, and m. K1,Kv,m

$$P r o o f \ o f \ L e m m a \ 7 . \ \text { in Appendix B.}$$

Proposition 8 below is the main result of this subsection and follows directly from Lemma 6 and Lemma 7 above. Indeed, when the intrinsic dimension is d2, the risk of (d−1)n) our estimator dn, is of order O n (d1 by Lemma 6 and the union bound. On the other hand, when the intrinsic dimension is d1, the risk of our estimator dn is 0, because of Lemma 7.

<!-- p:15 -->


Proposition 8. Fix τg, τl ∈ (0, ∞], KI ∈ [1, ∞), Kv ∈ (0, 2−m], Kp ∈ [(2K1)m, ∞), d1, d2 ∈ N, with τg ≤ τl and 1 ≤ d1 &lt; d2 ≤ m. Let dn be in (3.4). Then either for d = d1 or d = d2,

$$0 r \, d = d _ { 2 } , \\ \sup _ { P \in \mathcal { P } _ { \tau _ { g } , \tau _ { \ell } , K _ { 1 } , K _ { v } , K _ { p } } } \mathbb { E } _ { P ( n ) } \left [ \ell \left ( \widehat { d } _ { n } , d ( P ) \right ) \right ] \\ \leq 1 ( d = d _ { 2 } ) \left ( C _ { K _ { 1 } , K _ { p } , K _ { v } , m } ^ { ( 8 ) } \right ) ^ { n } \max \left \{ 1 , \tau _ { g } ^ { - \left ( \frac { d _ { 2 } } { d _ { 1 } } m + m - 2 d _ { 2 } \right ) n } \right \} n ^ { - \left ( \frac { d _ { 2 } } { d _ { 1 } } - 1 \right ) n } ,$$

where ~(8) K1,Kp,Kv,m ∈ (0, ∞) is a constant depending only on K1, Kp, Kv, and m.

Proof of Proposition 8. in Appendix B.

As described so far, the convergence analysis of our dimension estimator is probable. This is enough for our purpose, which is to quantify the statistical difficulties, in particular the minimax rate, of the dimension estimation problem. However, our dn in (3.4) is not completely data-driven but depends on the model parameters τg, K1, and Kv. Hence the model on which our convergence analysis is valid depends on the model parameters. When it comes to applying our dimension estimator dn to real data, we need to estimate the constant ~(7) K1,Kv,m' Proofs of Lemma 6 and 7 suggest that overestimating CK1,Kv,m ~(7) by ~(7) some constant factor doesn't deteriorate the convergence rate, so the constants C K1,Kv,m and τg can be replaced by any consistent estimators. Still, we have the difficulty of tuning γ(7) K1,Kv,m and τg. Also, the constant C K1,Kv,m is tuned to work for the worst case, so the practical performance of our dimension estimator is questionable.

### 3.2 Minimax Upper Bound

As noted at the beginning of Section 3, the maximum risk of our estimator dn in (3.1) serves as an upper bound on the minimax risk Rn in (2.6). Since we assume that the intrinsic dimension is either d1 or d2, Proposition 8 yields that the maximum risk of our estimator d2 −1)n λn is of order O n Lp This also serves as an upper bound of the minimax risk Rn, as in Proposition 9.

Proposition 9. Fix τg, τl ∈ (0, ∞], KI ∈ [1, ∞), Kv ∈ (0, 2−m], Kp ∈ [(2K1)m, ∞), d1, d2 ∈ N, with τg ≤ τl and 1 ≤ d1 &lt; d2 ≤ m. Then

$$2 \subset & \cap , \text { with } \mathcal { I } _ { g } \subseteq \mathcal { I } _ { \ell } \text { and } \mathbb { I } \subseteq \mathcal { I } _ { 1 } \text { < } \mathcal { A } _ { 2 } \subseteq \mathbb { I } . \\ & \inf _ { \substack { \widehat { d } _ { n } \, P \in \mathcal { P } _ { 1 } \cup \mathcal { P } _ { 2 } \\ & \leq \left ( C _ { K _ { 1 } , K _ { p } , K _ { v } , m } ^ { ( 8 ) } \right ) ^ { n } \max \left \{ 1 , \mathcal { I } _ { g } ^ { - \left ( \frac { d _ { 2 } } { d _ { 1 } } m + m - 2 d _ { 2 } \right ) n } \right \} n - \left ( \frac { d _ { 2 } } { d _ { 1 } } - 1 \right ) n ,$$

<!-- p:16 -->


γ(8) where is from Proposition 8 and K1,Kp,Kv,m

$$\mathcal { P } _ { 1 } = \mathcal { P } _ { \tau _ { g } , \tau _ { \ell } , K _ { I } , K _ { v } , K _ { p } } , \quad \mathcal { P } _ { 2 } = \mathcal { P } _ { \tau _ { g } , \tau _ { \ell } , K _ { I } , K _ { v } , K _ { p } } .$$

Proof of Proposition 9. in Appendix B.

## 4 Lower Bound for Choosing Between Two Dimensions

The goal of this section is to derive a lower bound for the minimax rate Rn. As in Section 3, we fix d1, d2 ∈ N with 1 ≤ d1 &lt; d2 ≤ m, and assume that the intrinsic dimension of data is either d1 or d2 as in (2.7). This assumption is relaxed in Section 5. All the proofs for this section are in Section C.

Our strategy is to find a subset T ⊂ In ⊂ (Rd)n and two sets of distributions Pd1 and Pd2 2 with dimensions d1 and d2, such that Pd1 and Pd2 satisfy the regularity conditions as     r   .  . ) =   t distinguish whether the underlying distribution is from Pd1 1 or Pd2.

After constructing T, Pd1 and P2, we derive the lower bound using the following result, known as Le Cam's lemma.

Lemma 10. (Le Cam's Lemma) Let P be a set of probability measures on (Ω, F), and P1, P2 ⊂ P be such that for all P ∈ Pi, θ(P) = θi for i = 1, 2. For any Qi ∈ co(Pi), where co(Pi) is the convex hull of Pi, let qi be the density of Qi with respect to a measure ν. Then

$$\inf _ { \widehat { \theta } } \sup _ { P \in \mathcal { P } } \mathbb { E } _ { P } [ \ell ( \widehat { \theta } , \theta ( P ) ) ] \geq \frac { \ell ( \theta _ { 1 } , \theta _ { 2 } ) } { 2 } \int [ q _ { 1 } ( x ) \wedge q _ { 2 } ( x ) ] d \nu ( x ) .$$

Proof of Lemma 10. [See Yu, 1997, Chapter 29.2, Lemma 1].

In above Le Cam's lemma, considering the convex hull of distributions co(Pi) is critical for getting the nontrivial lower bound. Suppose we are using the basic version of Le Cam's lemma where the convex hull is not considered, i.e. Qi ∈ Pi. Then for two distributions Q1 and Q2 respectively from our d1 and d2 dimensional model pd1 τg,τl,K1,Kv,Kp and Pd2 Pτ9,τt,K1,Kv,Kp, Q1 and Q2 are singular to each other; i.e. q1(x) ∧ q2(x) = 0 for all x. Hence no matter which subset P1 and P2 we choose with d(P1) = d1 and d(P2) = d2, the lower bound in (4.1) will be always 0. This trivial bound can be improved by considering the convex hull of distributions co(Pi) in Le Cam's lemma.

Our construction for T, Pd1 , l1, and Pd2 is based on mimicking a space-filling curve. 2 Intuitively, this gives the lower bound since it is difficult to differentiate a space-filling curve and a higher dimensional cube. In detail, we set

<!-- p:17 -->


$$\mathcal { P } _ { 1 } ^ { d _ { 1 } } & = \{ \text {distributions supported on} \\ & a \text { space-filling-curve like } d _ { 1 } \text {dimensional manifold} \} ,$$

and

$$\mathcal { P } _ { 2 } ^ { d _ { 2 } } = \{ \text {uniform distributions on } [ - K _ { I } , K _ { I } ] ^ { d _ { 2 } } \} .$$

To apply Le Cam's lemma, we construct a set T ⊂ In so that, whenever X = (X1, . . . , Xn) ∈ T, we cannot distinguish whether X is from Pd1 in (4.2) or P12 in (4.3). Then, for an appropriately chosen distribution Q1 in the convex hull of Pd1 with density q1 with respect to Lebesgue measure λ on the cube [−K1, K1]d2, and a density q2 from the class Pd2, 2, ∫T[q1(x) ∧ q2(x)]dλ(x) is a lower bound on the minimax rate Rn in (2.6). Indeed, from Le Cam's Lemma 10, we have that

$$\inf _ { \hat { \theta } } \sup _ { \mathcal { P } } \mathbb { E } _ { P } [ \ell ( \theta , \theta ( P ) ) ] & \geq \frac { 1 } { 2 } \int [ q _ { 1 } ( x ) \wedge q _ { 2 } ( x ) ] d \lambda ( x ) \\ & \geq \frac { 1 } { 2 } \int _ { T } [ q _ { 1 } ( x ) \wedge q _ { 2 } ( x ) ] d \lambda ( x ) .$$

For constructing the class Pd1 in (4.2), it will be sufficient to consider the case d1 = 1. In fact, Lemma 11 states that the regularity conditions in Definition 2 are still preserved when the manifold M is a Cartesian product with a cube [−K1, K1]∆d, as in Figure 4.1. Hence for constructing a d-dimensional "space-filling" manifold, we first construct a 1dimensional space-filling curve satisfying the required regularity conditions, and then we form a Cartesian product with a cube of dimension d − 1, which becomes a d-dimensional manifold satisfying the same regularity conditions by Lemma 11.

Lemma 11. Fix τg, τl ∈ (0, ∞], K1 ∈ [1, ∞), Kv ∈ (0, 2−m], d, ∆d ∈ N, with τg ≤ τl and be a d-dimensional manifold of global reach ≥ τg, local reach ≥ τe, which is embedded in Rm−∆d. Then

$$M \times [ - K _ { I } , K _ { I } ] ^ { \Delta d } \in \mathcal { M } _ { \tau _ { g } , \tau _ { \ell } , K _ { I } , K _ { v } } ^ { d + \Delta d } ,$$

which is embedded in Rm.

Proof of Lemma 11. in Appendix C.

The precise construction of Pd1 in (4.2) and T is detailed in Lemma 12. As in Figure 4.2, we construct Ti's that are cylinder sets aligned as a zigzag in [−K1, K1]d2, and n n then T is constructed as T = Sn ∏Ti, where the permutation group Sn acts on ∏Ti as a i=1 i=1 coo       x n     o o  old M ∈ Md1 that passes through x1, . ., xn. The class P1 in (4.2) is finally defined Tg,Te,K1,Kv as the set of distributions that are supported on such a manifold.

<!-- p:18 -->


Figure 4.1: The regularity conditions in Definition 2 are still preserved under the Cartesian product with a cube [−K1, K]∆d. Detailed explanations are in Figure C.1.

2KI

M

M × [−K1, KI]∆d

Figure 4.2: This figure illustrates the case where d1 = 1 and d2 = 2. (a) shows how Ti's are aligned in a zigzag. (b) shows for given x1 ∈ T1, . . . , xn ∈ Tn(represented as blue points), how a manifold with regularity conditions(represented as a red curve) passes through x1, . . . , xn. Detailed constructions in Figure C.2.

2KI

T1

T2

x1

●

x2

T1

T2

Te

T4

T3

x4

●

x3

2KI

T5

T6

x5

x6

T8

T7

x8

x7

(a) alignment of Ti

(b) manifold passing through xi's

<!-- p:19 -->


Lemma 12. Fix τe ∈ (0, ∞], K1 ∈ [1, ∞), d1, d2 ∈ N, with 1 ≤ d1 ≤ d2, and suppose τl &lt; K1. Then there exist T1, . . . , Tn ⊂ [−K1, K1]d2 such that:

- (1) The Ti's are distinct.

(2) For each Ti, there exists an isometry Φi such that

$$T _ { i } = \Phi _ { i } \left ( [ - K _ { I } , K _ { I } ] ^ { d _ { 1 } - 1 } \times [ 0 , a ] \times B _ { \mathbb { R } ^ { d _ { 2 } - d _ { 1 } } } ( 0 , w ) \right ) ,$$

$$w h e r e \, c = \left \lceil \frac { K _ { I } + \tau _ { \ell } } { 2 \tau _ { \ell } } \right \rceil , \, a = \frac { K _ { I } - \tau _ { \ell } } { ( d _ { 2 } - d _ { 1 } + \frac { 1 } { 2 } ) \left | \frac { n } { d _ { 2 } - d _ { 1 } } \right | } , \, a n d \, w = \min \left \{ \tau _ { \ell } , \, \frac { ( d _ { 2 } - d _ { 1 } ) ^ { 2 } ( K _ { I } - \tau _ { \ell } ) ^ { 2 } } { 2 \tau _ { \ell } ( d _ { 2 } - d _ { 1 } + \frac { 1 } { 2 } ) \left ( \left \lceil \frac { n } { d _ { 2 } - d _ { 1 } } \right \rceil + 1 \right ) ^ { 2 } } \right \} .$$

(3)There exists M : (BRd2−d1 (0, w))n → Md1,1 one-to-one such that for each τg,Te,K1,Kv yi ∈ BRd2−d1 (0, w), 1 ≤ i ≤ n, M (y1, · · . , yn)∩Ti = Φi([− K1, K1]d1−1 × [0, a] × {yi}). Hence

Proof of Lemma 12. in Appendix C.

Next we show that whenever x = (x1, . . . , xn) ∈ T, it is difficult to tell whether the data e         t d  d  tnd  d ne n dt q2 be the density function of the uniform distribution on [−K1, K1]d2, then from (4.4), we t  (x(x  (x ]f q  s    t os such that q1(x) ≥ Cq2(x) for every x ∈ T with C &lt; 1, then q1(x) ∧ q2(x) ≥ Cq2(x), so that C ∫T q2(x) can serve as a lower bound of the minimax rate. Such existence of Q1 and the inequality q1(x) ≥ Cq2(x) is shown in Claim 13.

n Claim 13. Let T = Sn ∏Ti where the Ti's are from Lemma 12. Let Q2 be the uniform i=1 distribution on [−K1, K1]d2, and let Pd1 be as in (4.2). Then there exists Q1 ∈ co(Pd1) satisfying that for all x ∈ intT, there exists rx &gt; 0 such that for all r &lt; rx,

$$Q _ { 1 } \left ( \prod _ { i = 1 } ^ { n } B _ { \| \cdot \| _ { \mathbb { R } ^ { d _ { 2 } } , \infty } ( x _ { i } , r ) } \right ) \geq 2 ^ { - n } Q _ { 2 } \left ( \prod _ { i = 1 } ^ { n } B _ { \| \cdot \| _ { \mathbb { R } ^ { d _ { 2 } } , \infty } ( x _ { i } , r ) } \right ) .$$

Proof of Claim 13. in Appendix C.

The following lower bound is then a consequence of Le Cam's lemma, Lemma 12, and the previous claim.

<!-- p:20 -->


Proposition 14. Fix τg, τl ∈ (0, ∞], KI ∈ [1, ∞), Kv ∈ (0, 2−m], Kp ∈ [(2K1)m, ∞), d1, d2 ∈ N, with τg ≤ τe and 1 ≤ d1 &lt; d2 ≤ m, and suppose that τl &lt; K1. Then

$$& \inf \sup \mathbb { E } _ { P ( n ) } [ \ell ( \widehat { d } _ { n } , d ( P ) ) ] \\ & \quad \geq \left ( C _ { d _ { 1 } , d _ { 2 } , K _ { I } } ^ { ( 1 4 ) } \right ) ^ { n } \min \left \{ \tau _ { \ell } ^ { - 2 ( d _ { 2 } - d _ { 1 } + 1 ) } n ^ { - 2 } , 1 \right \} ^ { ( d _ { 2 } - d _ { 1 } ) n } ,$$

γ(14) where ∈ (0, ∞) is a constant depending only on d1, d2, and K1 and d1,d2,K1

$$\mathcal { Q } = \mathcal { P } _ { \tau _ { g } , \tau _ { \ell } , K _ { I } , K _ { v } , K _ { p } } ^ { d _ { 1 } } \bigcup \mathcal { P } _ { \tau _ { g } , \tau _ { \ell } , K _ { I } , K _ { v } , K _ { p } } ^ { d _ { 2 } } .$$

Proof of Proposition 14. in Appendix C.

## 5 Upper Bound and Lower Bound for the General Case

Now we generalize our results to allow the intrinsic dimension d to be any integer between m 1 and m. Thus the model is P = U pd as in (2.8). For the upper bound, we Tg,Te,K1,Kv,Kp d=1 extend the dimension estimator dn in (3.4) and compute its maximum risk. And for the lower bound, we simply use the lower bound derived in Section 4 with d1 = 1 and d2 = 2. All the proofs for this section are in Section D.

For the model P in (2.8), our dimension estimator dn estimates the dimension as the smallest integer 1 ≤ d ≤ m that the d-squared length of the TSP is below a certain threshold, i.e. (3.6) holds; that is,

$$\widehat { d } _ { n } ( X ) \coloneqq & \min \{ d \in [ 1 , m ] \colon \\ & \min _ { \sigma \in S _ { n } } \left \{ \sum _ { i = 1 } ^ { n - 1 } \| X _ { \sigma ( i + 1 ) } - X _ { \sigma ( i ) } \| _ { \mathbb { R } ^ { m } } \right \} \leq C _ { K _ { I } , K _ { v } , m } ^ { ( T ) } \max \left \{ 1 , \tau _ { g } ^ { d - m } \right \} \right \} . \\ \intertext { A s a g e r a l z e d \, r o s t i m e s $ \, $ } & \quad \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext { \intertext {$$

As a generalized result of Proposition 8, Proposition 15 gives an upper bound for the risk of our estimator dn in (5.1). When the intrinsic dimension is d, our estimator dn makes an error with probability of order O (n−a−1n)

Proposition 15. Fix τg, τe ∈ (0, ∞], K1 ∈ [1, ∞), Kv ∈ (0, 2−m], Kp ∈ [(2K1)m, ∞), with Tg m (T    n    1:

$$\gamma _ { \ell } \cdot \ B c t { a } _ { n } \ B c t { h } & ( 0 . 1 ) \cdot 1 ^ { n } \ B c t { h } . \\ & \sup _ { P \in \mathcal { P } ^ { d } _ { \tau _ { g } , \tau _ { \ell } , K _ { 1 } , K _ { v } , K _ { p } } } \mathbb { E } _ { P ^ { ( n ) } } \left [ \ell \left ( \widehat { d } _ { n } , d ( P ) \right ) \right ] \\ & \leq 1 ( d > 1 ) \left ( C _ { K _ { 1 } , K _ { p } , K _ { v } , M } ^ { ( 1 5 ) } \right ) ^ { n } \max \left \{ 1 , \tau _ { g } ^ { - ( d m + m - 2 d ) n } \right \} n ^ { - \frac { 1 } { d - 1 } n } ,$$

□


<!-- p:21 -->


where K1,Kp,Kv,m ∈ (0, ∞) is a constant depending only on K1, Kp, Kv, and m. γ(15)

- [ ] Proof of Proposition 15. in Appendix D.

Then similarly to Section 3.2, the maximum risk of our estimator dn in (5.1) serves as an upper bound on the minimax risk Rn in (2.6). The maximum of the upper bound in Proposition 15 over d ranging from 1 to m should serve as the upper bound for the maximum risk, hence we get the upper bound of the minimax risk Rn in Proposition 16 as a generalized result of Proposition 9.

Proposition 16. Fix τg, τl ∈ (0, ∞], K1 ∈ [1, ∞), Kv ∈ (0, 2−m], Kp ∈ [(2K1)m, ∞), with τg ≤ τl. Then:

$$\inf _ { \widehat { d } _ { n } } \sup _ { P \in \mathcal { P } } \mathbb { E } _ { P ^ { ( n ) } } \left [ \ell \left ( \widehat { d } _ { n } , d ( P ) \right ) \right ] \leq \left ( C _ { K _ { I } , K _ { P } , K _ { v } , m } ^ { ( 1 5 ) } \right ) ^ { n } \max \left \{ 1 , \tau _ { g } ^ { - ( m ^ { 2 } - m ) n } \right \} n ^ { - \frac { 1 } { m - 1 } n } ,$$

γ(15) where is from Proposition 15. K1,Kp,Kv,m

$$P r o o f \ o f \ P r o p o s i t i o n \ 1 6 . \ \text { in Appendix } D .$$

Proposition 17 provides a lower bound for the minimax rate Rn in (2.6), in multidimensions. It can be viewed of a generalization for the binary dimension case in Proposition 14.

Proposition 17. Fix τg, τe ∈ (0, ∞], KI ∈ [1, ∞), Kv ∈ (0, 2−m], Kp ∈ [(2K1)m, ∞), with τg ≤ τl, and suppose that τl &lt; K1. Then,

$$\inf _ { \widehat { d } _ { n } } \sup _ { P \in \mathcal { P } } \mathbb { E } _ { P ^ { ( n ) } } [ \ell ( \widehat { d } _ { n } , d ( P ) ) ] \geq \left ( C _ { K _ { I } } ^ { ( 1 7 ) } \right ) ^ { n } \min \left \{ \tau _ { \ell } ^ { - 4 } n ^ { - 2 } , 1 \right \} ^ { n }$$

γ(17) where ∈ (0, ∞) is a constant depending only on K1. KI

Proof of Proposition 17. in Appendix D.

## 6 Conclusion

On a logarithmic scale, the leading terms of the lower and upper bounds for the minimax rate Rn in (2.6) have the form

−nclog τ

for some constant c, where τ is the global reach for the upper bound and the local reach for the lower bound. This shows that the difficulty of the problem of estimating the dimension goes to 0 rapidly with sample size, in a way that depends on the curvature of the manifold.

<!-- p:22 -->


There are several open problems. The first is to tighten the bounds so that the upper and lower bounds match. Second, it should be possible to extend the analysis to allow noise. With enough noise, the minimax rate should eventually become the same as the rate in [Koltchinskii, 2000]. Finally, it would be interesting to get very precise bounds on the many dimension estimators that appear in the literature and compare these bounds to the minimax bounds.

## A Proofs for Section 2

Lemma 3. Fix τg ∈ (0,∞], and let M be a d-dimensional manifold with global reach ≥ τg. For r ∈ (0, τg), let Mr := {x ∈ Rm : distRm,(x, M) &lt; r} be an r-neighborhood of M in Rm. Then, the volume of M is upper bounded as

$$v o l _ { M } ( M ) \leq \frac { m ! } { d ! } r ^ { d - m } v o l _ { \mathbb { R } ^ { m } } ( M _ { r } ) .$$

Further, fix τl ∈ (0, ∞], K1 ∈ [1, ∞), Kv ∈ (0, 2−m], with τg ≤ τl, and suppose M ∈ Md Then the volume of M is upper bounded as 1τg,τe,K1,Kv·

$$\ v o l _ { M } ( M ) \leq C _ { K _ { I } , m } ^ { ( 3 ) } \max \left \{ 1 , \tau _ { g } ^ { d - m } \right \} ,$$

where is a constant depending only on KI and m. K1,m

Proof of Lemma 3. Suppose {A1, . . . , Al} is a disjoint cover of M, i.e. measurable subsets of M such that Ai ∩ Aj = ∅, ∪ Ai = M, and each Ai is equipped with a chart map i=1 φ(i) : Ui ⊂ Rd → Ai. Such a triangulation is always possible. For each Ai, define M(i) {x ∈ Rm : πM(x) ∈ Ai, distRm,11(x, M) ≤ r} so that each Ai is a projection of M(i) on M, as in Figure A.1. Since ∥x|2 ≤ ∥x∥1 fo all x ∈ Rm, Ui=1 M(i) ⊂ Mr holds, and hence

$$\sum _ { i = 1 } ^ { l } v o l _ { \mathbb { R } ^ { m } } ( M _ { r } ^ { ( i ) } ) \leq v o l _ { \mathbb { R } ^ { m } } ( M _ { r } ) .$$

<!-- p:26 -->


Fix i ∈ {1, . . . , l}. Then for each u ∈ Ui, there exists a linear isometry R(i)(u) : Rm−d → (Tφ(i)(u)M)−, which can be identified as an m × (m − d) matrix with jth column being R(i,j)(), so that M(i) can be parametrized as ψ(i : Ui × BRm−,-1(1, r) → M(i) withh

$$\psi ^ { ( i ) } ( u , t ) = \varphi ^ { ( i ) } ( u ) + R ^ { ( i ) } ( u ) t = \varphi ^ { ( i ) } ( u ) + \sum _ { j = 1 } ^ { m - d } t _ { j } R ^ { ( i , j ) } ( u ) .$$

Then, because R(i) is an isometry,

$$R ^ { ( i ) } ( u ) ^ { \top } R ^ { ( i ) } ( u ) = I _ { m - d } .$$

Let ψ(i) ,(i) ∂ψ(i) ∂ψ(i) ∂ψ(i) ∈ Rm×d be the partial derivative of ψ(i) with respect ∂u ∂u1 ∂ud to u and let ψ(i (i) ∂ψ(i) be the partial derivative of ψ(i) with respect to t. Define φu (i) and R(i,j) similarly. Then, since R(i) is an isometry, image(R(i)(u)) = (Tφ(i)(u)M)− holds, and hence

$$R ^ { ( i ) } ( u ) ^ { \top } \varphi _ { u } ^ { ( i ) } ( u ) = 0 .$$

Also by differentiating (A.5), for all j,

$$R _ { u } ^ { ( i , j ) } ( u ) ^ { \top } R ^ { ( i ) } ( u ) = 0 .$$

Also by differentiating (A.4), we get

$$\psi _ { u } ^ { ( i ) } ( u , t ) = \varphi _ { u } ^ { ( i ) } ( u ) + \sum _ { j = 1 } ^ { m - d } t _ { j } R _ { u } ^ { ( i , j ) } ( u ) ,$$

$$\psi _ { t } ^ { ( i ) } ( u , t ) = R ^ { ( i ) } ( u ) .$$

and

Hence by multiplying (A.8) and (A.9), and by applying (A.5), (A.6), and (A.7), we get

$$\psi _ { t } ^ { ( i ) } ( u , t ) ^ { \top } \psi _ { u } ^ { ( i ) } ( u , t ) = R ^ { ( i ) } ( u ) ^ { \top } \varphi _ { u } ^ { ( i ) } ( u ) + R ^ { ( i ) } ( u ) ^ { \top } R _ { u } ^ { ( i ) } ( u ) t = 0 ,$$

and

Now let's consider ψ(i)(u, t) ̄ψ(i)(u,t). From (A.7) and image(R(i)(u)) = (Tφ(i)(u) M)⊥, column space generated by Ri,j)(u) is contained in Tφ(i)(u)M, i.e.

$$\psi _ { t } ^ { ( i ) } ( u , t ) ^ { \top } \psi _ { t } ^ { ( i ) } ( u , t ) = R ^ { ( i ) } ( u ) ^ { \top } R ^ { ( i ) } ( u ) = I _ { m - d } . \\$$

$$\left \langle R _ { u } ^ { ( i , j ) } ( u ) \right \rangle \subset T _ { \varphi ^ { ( i ) } ( u ) } ( M ) = s p a n ( \varphi _ { u } ^ { ( i ) } ( u ) ) .$$

<!-- p:27 -->


Therefore, there exists Λ(i,j)(u) : d × d matrix such that

$$R _ { u } ^ { ( i , j ) } ( u ) = \varphi _ { u } ^ { ( i ) } ( u ) \Lambda ^ { ( i , j ) } ( u ) .$$

Then by applying this to (A.8),

$$\psi _ { u } ^ { ( i ) } ( u , t ) = \varphi _ { u } ^ { ( i ) } ( u ) \left ( I + \sum _ { j = 1 } ^ { m - d } t _ { j } \Lambda ^ { ( i , j ) } ( u ) \right ) .$$

Now M en of global  g implies ( ) (u, ) is f ull rank fo allt BRm−4,1–r reea, g). m−d From (A.12), this implies I + Σ tjΛ(i,j)(u) is invertible for all t ∈ BRm−d,1 (0, τg), and j=1 this implies all singular values of Λ(i,j)(u) are bounded by 1. . Hence for all v ∈ Rd, Tg

$$\left | v ^ { \top } \Lambda ^ { ( i , j ) } ( u ) v \right | \leq \frac { \| v \| _ { 2 } ^ { 2 } } { \tau _ { g } } ,$$

and accordingly,

$$\left | v ^ { \top } \left ( I + \sum _ { j = 1 } ^ { m - d } t _ { j } \Lambda ^ { ( i , j ) } ( u ) \right ) v \right | & \geq \| v \| _ { 2 } ^ { 2 } - \sum _ { j = 1 } ^ { m - d } | t _ { j } | \left | v ^ { \top } \Lambda ^ { ( i , j ) } ( u ) v \right | \\ & \geq \left ( 1 - \frac { \| t \| _ { 1 } } { \tau _ { g } } \right ) \| v \| _ { 2 } ^ { 2 } .$$

m−d Hence any singular value σ of I + Σ tjΛ(i,j) (u) satisfies |σ| ≥ 1 − ||t||1 . And since ∥|t||1 ≤ τg, j=1 Tg

$$\left | I + \sum _ { j = 1 } ^ { m - d } t _ { j } \Lambda ^ { ( i , j ) } ( u ) \right | \geq \left ( 1 - \frac { \| t \| _ { 1 } } { \tau _ { g } } \right ) ^ { d } .$$

(u, t)− ψ(i) (u, t) is lower bounded as

$$\left | \psi _ { u } ^ { ( i ) } ( u , t ) ^ { \top } \psi _ { u } ^ { ( i ) } ( u , t ) \right | & = \left | I + \sum _ { j = 1 } ^ { m - d } t _ { j } \Lambda ^ { ( i , j ) } ( u ) \right | ^ { 2 } \left | \varphi _ { u } ^ { ( i ) } ( u ) ^ { \top } \varphi _ { u } ^ { ( i ) } ( u ) \right | \\ & \geq \left ( 1 - \frac { \| t \| _ { 1 } } { \tau _ { g } } \right ) ^ { 2 d } \left | \varphi _ { u } ^ { ( i ) } ( u ) ^ { \top } \varphi _ { u } ^ { ( i ) } ( u ) \right | .$$

<!-- p:28 -->


Now, let gij (Mr) be the Riemannian metric tensor of Mr, and g(M (M) be the Riemannian metric tensor of M. Then from (A.10), (A.11), and (A.13), the determinant of Riemannian metric tensor gij (Mr) is lower bounded by

$$& \text {or } g _ { i j } ^ { ( M _ { r } ) } \text { is lower bounded by } \\ & \quad | \det ( g _ { i j } ^ { ( M _ { r } ) } ) | = \left | \left ( \psi _ { u } ^ { ( i ) } ( u , t ) \ \psi _ { t } ^ { ( i ) } ( u , t ) \right ) ^ { \top } \left ( \psi _ { u } ^ { ( i ) } ( u , t ) \ \psi _ { t } ^ { ( i ) } ( u , t ) \right ) \right | \\ & \quad = \left | \begin{array} { c } \psi _ { u } ^ { ( i ) } ( u , t ) ^ { \top } \psi _ { u } ^ { ( i ) } ( u , t ) & \psi _ { u } ^ { ( i ) } ( u , t ) ^ { \top } \psi _ { t } ^ { ( i ) } ( u , t ) \\ \psi _ { u } ^ { ( i ) } ( u , t ) ^ { \top } \psi _ { t } ^ { ( i ) } ( u , t ) & \psi _ { t } ^ { ( i ) } ( u , t ) ^ { \top } \psi _ { t } ^ { ( i ) } ( u , t ) \end{array} \right | \\ & \quad = \left | \begin{array} { c } \psi _ { u } ^ { ( i ) } ( u , t ) ^ { \top } \psi _ { u } ^ { ( i ) } ( u , t ) & \end{array} \right | \\ & \quad \geq \left ( 1 - \frac { \| t \| _ { 1 } } { \tau _ { g } } \right ) ^ { 2 d } \left | \varphi _ { u } ^ { ( i ) } ( u ) ^ { \top } \varphi _ { u } ^ { ( i ) } ( u ) \right | \\ & \quad = \left ( 1 - \frac { \| t \| _ { 1 } } { \tau _ { g } } \right ) ^ { 2 d } | \det ( g _ { i j } ^ { ( M ) } ) | . \\$$

And from this, the volume of M(i) is lower bounded as

$$And from this, the volume of M _ { r } ^ { ( i ) } \, is lower bounded as \\ & \quad v o l _ { \mathbb { R } ^ { m } } ( M _ { r } ^ { ( i ) } ) = \int _ { U _ { i } \times B _ { r } ^ { m , \dots , | | ( 0 , r ) } } \sqrt { | \det ( g _ { i j } ^ { ( M _ { r } ) } ) | } d u t \\ & \geq \int _ { U _ { i } \times B _ { r } ^ { m , \dots , | | ( 0 , r ) } } ( 1 - \| t \| _ { 1 } \kappa _ { g } ) ^ { d } \sqrt { | \det ( g _ { i j } ^ { ( M ) } ) | } d t d u \\ & = v o l ( U _ { i } ) \int _ { 0 } ^ { r } \int _ { t _ { 1 } + \dots + t _ { m - d - 1 } s } \left ( 1 - \frac { s } { \tau _ { g } } \right ) ^ { d } d t _ { 1 } \cdots d t _ { m - d - 1 } d s \\ & = \frac { 1 } { ( m - d - 1 ) ! } v o l ( U _ { i } ) \int _ { 0 } ^ { r } s ^ { m - d - 1 } \left ( 1 - \frac { s } { \tau _ { g } } \right ) ^ { d } d s \\ & = \frac { 1 } { ( m - d - 1 ) ! } r ^ { m - d } v o l ( U _ { i } ) \int _ { 0 } ^ { 1 } u ^ { m - d - 1 } \left ( 1 - \frac { r } { \tau _ { q } } u \right ) ^ { d } d u \\ & \geq \frac { 1 } { ( m - d - 1 ) ! } r ^ { m - d } v o l ( U _ { i } ) \int _ { 0 } ^ { 1 } u ^ { m - d - 1 } ( 1 - u ) ^ { d } d u \\ & = \frac { d ! } { m ! } r ^ { m - d } v o l ( U _ { i } ) . \\ \intertext { B a p p l y } By applying ( A . 1 ) to ( A . 3 ) , we can lower bound the volume of M _ { r } as$$

By applying (A.14) to (A.3), we can lower bound the volume of Mr as

$$v o l _ { \mathbb { R } ^ { m } } ( M _ { r } ) & \geq \frac { d ! } { m ! } r ^ { m - d } \sum _ { i = 1 } ^ { l } v o l ( U _ { i } ) \\ & = \frac { d ! } { m ! } r ^ { m - d } v o l _ { M } ( M ) ,$$

<!-- p:29 -->


hence rewriting this gives (A.1) as

$$v o l _ { M } ( M ) \leq \frac { m ! } { d ! } r ^ { d - m } v o l _ { \mathbb { R } ^ { m } } ( M _ { r } ) .$$

With r = min{τg, K1}, Mr is contained in min{τg, K1}- neighborhood of I, hence

$$\ v o l _ { \mathbb { R } ^ { m } } ( M _ { r } ) \leq 2 ^ { m } ( K _ { I } + \min \{ \tau _ { g } , K _ { I } \} ) ^ { m } \leq 2 ^ { 2 m } K _ { I } ^ { m } .$$

By combining (A.15) and (A.16), we get the desired upper bound of volM(M) in (A.2) as

$$1 5 ) \text { and } ( A . 1 6 ) , \text { we get the desired upper bound of } & \text { or } v o l _ { \mathbb { R } ^ { m } } \\ & \ v o l _ { M } ( M ) \leq \frac { m ! } { d ! } r ^ { d - m } v o l _ { \mathbb { R } ^ { m } } ( M _ { r } ) \\ & \leq \frac { m ! } { d ! } 2 ^ { 2 m } K _ { I } ^ { m } \min \{ \tau _ { g } , K _ { I } \} ^ { d - m } \\ & \leq C _ { K _ { I } , m } ^ { ( 3 ) } \max \left \{ 1 , \tau _ { g } ^ { d - m } \right \} ,$$

where γ(3) := m!22m Kp is a constant depending only on KI and m. K1,m

Lemma 4. Fix τg, τl ∈ (0, ∞], K1 ∈ [1, ∞), Kv ∈ (0, 2−m], with τg ≤ τl. Let M ∈ and r ∈ (0, 2√3τg]. Then M can be covered by N radius r balls BM(p1, r), . . ., BM (pN, r), with

$$N \leq \left \lfloor \frac { 2 ^ { d } v o l ( M ) } { K _ { v } r ^ { d } \omega _ { d } } \right \rfloor .$$

Proof of Lemma 4. We follow the strategy in [Ma and Fu, 2011, 4.3.1. Lemma 3].

Consider a maximal family of disjoint balls {BM (p1, γ), . . , BM(pN, γ) }, i.e. BM (pi, −) ∩ BM(pj, 2) = ∅ for i ≠ j and for all q ∈ M, there exists i ∈ [1, N] such that BM(q, ν) ∩ BM (pi, ν) ≠ ∅. Then ∥q − pil2 &lt; r holds, so {BM (p1, r), . . . , BM (pN, r)} covers M. Now, note that BM(pi, γ)'s are disjoint, and hence

$$\sum _ { i = 1 } ^ { N } v o l ( B _ { M } ( p _ { i } , \frac { r } { 2 } ) ) \leq v o l ( M ) .$$

Then since 2 ≤ √3τg, the condition (4) in Definition 2 implies vol(BM (pi, γ)) ≥ Kv2−drdωd for all i, hence applying this to (A.18) yields

$$N \leq \frac { 2 ^ { d } v o l ( M ) } { K _ { v } r ^ { d } \omega _ { d } } ,$$

hence M can be covered by N radius r balls with N satisfying (A.17).

<!-- p:30 -->


Lemma 18. (Toponogov comparison theorem, 1959) Let (M, g) be a complete Riemannian manifold with sectional curvature≥ κ, and let Sκ be a surface of constant Gaussian curvature κ. Given any geodesic triangle with vertices p, q, r ∈ M forming an angle α at q, consider a (comparison) triangle with vertices p, q, r ∈ Sκ such that distsk (p, ā) = distM (p, q), distsk(r, q) = distM(r, q), and ∠pqr = ∠pqr. Then

$$d i s t _ { M } ( \bar { p } , \bar { r } ) \leq d i s t _ { S _ { \kappa } } ( p , r ) .$$

Proof of Lemma 18. [See Petersen, 2006, Theorem 79, p.339]. Note that for a manifold with boundary, the complete Riemannian manifold condition can be relaxed to requiring the existence of a geodesic path joining p and q whose image lies on intM. □

Lemma 19. (Hyperbolic law of cosines) Let H\_κ2 be a hyperbolic plane whose Gaussian curvature is −κ2. Then given a hyperbolic triangle ABC with angles α, β, γ, and side lengths BC = a, CA = b, and AB = c, the following holds:

cosh(κα) = cosh(κb) cosh(κc) − sinh(κb) sinh(κc) cos α.

Proof of Lemma 19. [See Bridson and Häfliger, 1999, 2.13 The Law of Cosines in Mn, κ, p.24]. □

Claim 20. Let λ ∈ [0, 1] and a, b ∈ [0, ∞). Then

$$\frac { \cosh ^ { - 1 } ( ( 1 - \lambda ) \cosh a + \lambda \cosh b ) } { \sqrt { ( 1 - \lambda ) a ^ { 2 } + \lambda b ^ { 2 } } } \leq \frac { \sinh \left ( \max \{ a , b \} / 2 \right ) } { \max \{ a , b \} / 2 } .$$

Proof of Claim 20. Without loss of generality, assume a ≤ b. Consider two functions F, G : [0, ∞)2 × [0, 1] → R defined as F(a, b, λ) = f−1((1 − λ)f(a) + λf(b)) and G(a, b, λ) = g−1((1 − λ)g(a) + λg(b)), for 0 ≤ a ≤ b, λ ∈ [0, 1], f(t) = cosh t, and g(t) = t2. Applying Toponogov comparison theorem in Lemma 18 to (A.25) in the proof of Lemma 5 with r1 = a+b , r2 = b-a 2, α = arccos(√λ) ∈ [0, 7] implies 2 2

$$F ( a , b , \lambda ) \geq G ( a , b , \lambda ) ,$$

and f and g being strictly increasing function implies a ≤ G(a, b, λ) ≤ F(a, b, λ) ≤ b. Also differentiating the log fraction ∂ log F(a,b,λ) gives ∂a (G)a))

$$\text {differentiating the log fraction } \frac { \frac { \partial } { \partial a } \log \frac { 1 } { G ( a , b , \lambda ) } \text { gives} \\ \frac { \partial } { \partial a } \log \frac { F ( a , b , \lambda ) } { G ( a , b , \lambda ) } & = \frac { ( 1 - \lambda ) f ^ { \prime } ( a ) } { f ^ { \prime } ( F ( a , b , \lambda ) ) F ( a , b , \lambda ) } - \frac { ( 1 - \lambda ) g ^ { \prime } ( a ) } { g ^ { \prime } ( G ( a , b , \lambda ) ) G ( a , b , \lambda ) } \\ & = \frac { 1 - \lambda } { F ( a , b , \lambda ) } \exp \left ( - \int _ { a } ^ { F ( a , b , \lambda ) } ( \log f ^ { \prime } ) ^ { \prime } ( t ) d t \right ) \\ & - \frac { 1 - \lambda } { G ( a , b , \lambda ) } \exp \left ( - \int _ { a } ^ { G ( a , b , \lambda ) } ( \log g ^ { \prime } ) ^ { \prime } ( t ) d t \right ) .$$

<!-- p:31 -->


Then applying (log f′)'(t) = coth t &gt; 1-t = (log g′)′(t) for t &gt; 0 and F(a, b, λ) ≥ G(a, b, λ) to (A.20) implies

$$\frac { 0 } { 0 } < 0 ,$$

and hence

$$0 < \forall a < b , \ \frac { \partial } { \partial a } \log \frac { F ( a , b , \lambda ) } { G ( a , b , \lambda ) } < 0 , \\ \frac { F ( a , b , \lambda ) } { G ( a , b , \lambda ) } \leq \frac { F ( 0 , b , \lambda ) } { G ( 0 , b , \lambda ) } . \\ \intertext { G r o f m h i s , w e g e t }$$

By expanding F and G from this, we get

$$\begin{array} { r l } & { \frac { \cosh ^ { - 1 } ( ( 1 - \lambda ) \cosh a + \lambda \cosh b ) } { \sqrt { ( 1 - \lambda ) a ^ { 2 } + \lambda b ^ { 2 } } } \leq \frac { \cosh ^ { - 1 } ( \lambda \cosh b + ( 1 - \lambda ) ) } { \sqrt { \lambda b ^ { 2 } } } } \\ & { = \frac { \cosh ^ { - 1 } ( 1 + 2 \lambda \sinh ^ { 2 } \left ( \frac { b } { 2 } \right ) ) } { b \sqrt { \lambda } } } \\ & { \leq \frac { 2 \sinh \left ( \frac { b } { 2 } \right ) } { b } , } \\ & { \text {here the last line is coming from 1+ } r < \cosh \sqrt { 2 } x \Longrightarrow \cosh ^ { - 1 } ( 1 + x ) < \sqrt { 2 } x \text { for all } x > 2 . } \end{array}$$

0  x  s x  (x + 1 − ←= x   x +  s   s   −0n Hence we get (A.19).

Lemma 5. Fix τg, τl ∈ (0, ∞], K1 ∈ [1, ∞), Kv ∈ (0, 2−m], with τg ≤ τl. Let M ∈ and let exppk : Ek ⊂ Rm → M be an exponential map, where Ek is the domain of the exponential map exppk and TpkM is identified with Rd. For all v, w ∈ Ek, let Rk := max{|v||, ||w||}. Then

$$\| \exp _ { p _ { k } } ( v ) - \exp _ { p _ { k } } ( w ) \| _ { \mathbb { R } ^ { m } } \leq \frac { \sinh ( \sqrt { 2 } R _ { k } / \tau _ { \ell } ) } { \sqrt { 2 } R _ { k } / \tau _ { \ell } } \| v - w \| _ { \mathbb { R } ^ { d } } .$$

=: ,  () ddxə = z e (a) dxə = I t   fo food √2||v|| and r2 := √2||w|| τe Te so that distM(pk, q1) = √2r1 and distM (pk, 92) = Te r2, and let α := ∠q1pkq2 ∈ [0, x] so √2 that ∠q1pkq2 = 2α, as in Figure A.2(a). Then

$$\| v - w \| _ { \mathbb { R } ^ { d } } & = \frac { \tau _ { \ell } } { \sqrt { 2 } } \sqrt { r _ { 1 } ^ { 2 } + r _ { 2 } ^ { 2 } - 2 r _ { 1 } r _ { 2 } \cos 2 \alpha } \\ & = \frac { \tau _ { \ell } } { \sqrt { 2 } } \sqrt { ( r _ { 1 } + r _ { 2 } ) ^ { 2 } \sin ^ { 2 } \alpha + ( r _ { 1 } - r _ { 2 } ) ^ { 2 } \cos ^ { 2 } \alpha } .$$

Let κl := 1 H\_2κ2 be a surface of constant sectional curvature −2κ2, and let pk, ā1, ā2 ∈ H\_2κi Te 2( ̄k,  ̄1) = distM(pk,q1), distH\_2κ2( ̄k, ā2) = distM(pk, 92),

<!-- p:32 -->

q2

√2

Te

r2

distM(q1, q2)

2α

pk

\_2

Te

r1

q1

√2

Te

r2

distH\_2κk2(ā1, ā2)

2α

pk

√2

Tl

r1

M

(a) triangle △pkq1q2 in M

ā2

H\_2κ2

(b) comparison triangle △pkā1ā2 in H−2κ2

Figure A.2: (a) A triangle △pkq1q2 in M formed by pk, q1, q2, and (b) its comparison triangle △pkā1ā2 in H22κl

and ∠ ̄1pkā2 = ∠q1pkq2, so that △pk ̄1ā2 becomes a comparison triangle of pkq1q2, as in Figure A.2(b). Then since (sectional curvature of M) ≥ -2κ2 by [Aamari et al., 2017, Proposition A.1 (iii)], from the Toponogov comparison theorem in Lemma 18,

$$d i s t _ { H _ { - 2 \kappa _ { \ell } ^ { 2 } } } ( \bar { q } _ { 1 } , \bar { q } _ { 2 } ) .$$

Also, by applying the hyperbolic law of cosines in Lemma 19 to the comparison triangle △pkā1 ̄2 in Figure A.2(a),

$$\cosh \left ( \frac { \sqrt { 2 } } { \tau _ { \ell } } d i s t _ { H - 2 r _ { \ell } ^ { 2 } } ( \bar { q } _ { 1 } , \bar { q } _ { 2 } ) \right ) & = \cosh r _ { 1 } \cosh r _ { 2 } - \sinh r _ { 1 } \sinh r _ { 2 } \cos 2 \alpha \\ & = ( \sin ^ { 2 } \alpha ) \cosh ( r _ { 1 } + r _ { 2 } ) + ( \cos ^ { 2 } \alpha ) \cosh ( r _ { 1 } - r _ { 2 } ) . \quad ( A . 2 4 )$$

distH ( ̄ā1,ā2) From (A.22) and (A.24), we can expand the fraction of the distances ||v−w∥|Rd as

$$\frac { d i s t _ { H _ { - 2 \kappa } ^ { 2 } } ( \bar { q } _ { 1 } , \bar { q } _ { 2 } ) } { \| v - w \| _ { \mathbb { R } ^ { d } } } = \frac { \cosh ^ { - 1 } \left ( \sin ^ { 2 } \alpha \cosh ( r _ { 1 } + r _ { 2 } ) + \cos ^ { 2 } \alpha \cosh ( r _ { 1 } - r _ { 2 } ) \right ) } { \sqrt { ( \sin ^ { 2 } \alpha ) ( r _ { 1 } + r _ { 2 } ) ^ { 2 } + ( \cos ^ { 2 } \alpha ) ( r _ { 1 } - r _ { 2 } ) ^ { 2 } } } .$$

distH (ā1 ,ā2) Then we can upper bound the fraction of the distances by plugging in a = ∥|v−w∥|Rd |r1 − r2|, b = r1 + r2, λ = sin2 α to Claim 20 as

$$\frac { \cosh ^ { - 1 } \left ( \sin ^ { 2 } \alpha \cosh ( r _ { 1 } + r _ { 2 } ) + \cos ^ { 2 } \alpha \cosh ( r _ { 1 } - r _ { 2 } ) \right ) } { \sqrt { ( \sin ^ { 2 } \alpha ) ( r _ { 1 } + r _ { 2 } ) ^ { 2 } + ( \cos ^ { 2 } \alpha ) ( r _ { 1 } - r _ { 2 } ) ^ { 2 } } } \leq \frac { \sinh \left ( \frac { r _ { 1 } + r _ { 2 } } { 2 } \right ) } { ( r _ { 1 } + r _ { 2 } ) / 2 } .$$

<!-- p:33 -->


Then since t → sinh t is an increasing function of t and r1+r2 ≤ √2Rk/τe, so t 2

$$\frac { \sinh \left ( \frac { r _ { 1 } + r _ { 2 } } { 2 } \right ) } { ( r _ { 1 } + r _ { 2 } ) / 2 } & \leq \frac { \sinh ( \sqrt { 2 } R _ { k } / \tau _ { \ell } ) } { \sqrt { 2 } R _ { k } / \tau _ { \ell } } .$$

Combining (A.25), (A.26), and (A.27), we have an upper bound of the fraction of the distH (ā1,ā2) distances ∥|v−w∥|Rd as

$$\frac { d i s t _ { H _ { - 2 \kappa _ { \ell } ^ { 2 } } } ( \bar { q } _ { 1 } , \bar { q } _ { 2 } ) } { \| v - w \| _ { \mathbb { R } ^ { d } } } & \leq \frac { \sinh ( \sqrt { 2 } R _ { k } / \tau _ { \ell } ) } { \sqrt { 2 } R _ { k } / \tau _ { \ell } } .$$

And finally, combining (A.23) and (A.28), we get the desired upper bound of ∥ exppk(v) − exppk(ω)∥Rm in (A.21) as

$$\| \exp _ { p _ { k } } ( w ) - \exp _ { p _ { k } } ( w ) \| _ { \mathbb { R } ^ { m } } & \leq d i s t _ { M } ( q _ { 1 } , q _ { 2 } ) \\ & \leq d i s t _ { H _ { - 2 \kappa _ { \ell } ^ { 2 } } } ( \bar { q } _ { 1 } , \bar { q } _ { 2 } ) \\ & \leq \frac { \sinh ( \sqrt { 2 } R _ { k } / \tau _ { \ell } ) } { \sqrt { 2 } R _ { k } / \tau _ { \ell } } \| v - w \| _ { \mathbb { R } ^ { d } } .$$

## B Proofs for Section 3

Claim 21. Fix τg, τe ∈ (0, ∞], K1 ∈ [1, ∞), Kv ∈ (0, 2−m], Kp ∈ [(2K1)m, ∞), d1, d2 ∈ N, Then for all y∈ [0, ∞),

$$\left \{ 1 , \tau _ { g } ^ { d _ { 2 } - m } \right \} y ^ { \frac { d _ { 2 } } { d _ { 1 } } } , \quad ( B . 1 )$$

γ(21) where K1,Kp,m is a constant depending only on K1, Kp, and m.

Proof of Claim 21. Let pxn be the pdf of Xn. Then the conditional cdf of |Xn − Xn−1|dim d1 given X1, . . . , Xn-1 is upper bounded by the volume of a ball in the manifold M as

$$X _ { 1 } , \dots , X _ { n - 1 } & \text { is upper bounded by the volume of a ball in the manifold } M \text { as } \\ & P ^ { ( n ) } \left ( \left | | X _ { n } - X _ { n - 1 } | | _ { \mathbb { R } ^ { m } } ^ { d _ { 1 } } \leq y | X _ { 1 } , \dots , X _ { n - 1 } \right ) \\ & = P ^ { ( n ) } \left ( X _ { n } \in B _ { \mathbb { R } ^ { m } } \left ( X _ { n - 1 } , y ^ { \frac { 1 } { d _ { 1 } } } \right ) | \ X _ { 1 } , \dots , X _ { n - 1 } \right ) \\ & = \int _ { M \cap \left ( B _ { \mathbb { R } ^ { m } } \left ( X _ { n - 1 } , y ^ { \frac { 1 } { d _ { 1 } } } \right ) \right ) } ^ { \frac { 1 } { d _ { 1 } } } p _ { X _ { n } } \left ( x _ { n } \right ) d v o l _ { M } ( x _ { n } ) \\ & \leq K _ { p } v o l _ { M } \left ( M \cap B \left ( X _ { n - 1 } , y ^ { \frac { 1 } { d _ { 1 } } } \right ) \right ) ,$$

<!-- p:34 -->


where the last inequality is coming from the condition (6) in Definition 2. And by applying Lemma 3, volM (M ∩B (Xn−1, ydi) can be further bounded as

$$& \text {Lemma 3, volVol} \left ( M \cap B \left ( X _ { n - 1 } , y ^ { \frac { d _ { 1 } } { y ^ { 1 } } } \right ) \right ) \text { can be further bounded as} \\ & \quad v o l _ { M } \left ( M \cap B \left ( X _ { n - 1 } , y ^ { \frac { \frac { d _ { 1 } } { y ^ { 1 } } } { d _ { 1 } } } \right ) \right ) \\ & \leq \frac { m ! } { d _ { 2 } ! } \min \left \{ y ^ { \frac { 1 } { d _ { 1 } } } , \tau _ { g } \right \} ^ { d _ { 2 } - m } \ v o l _ { \mathbb { R } ^ { m } } \left ( B \left ( X _ { n - 1 } , y ^ { \frac { 1 } { d _ { 1 } } } + \min \left \{ y ^ { \frac { 1 } { d _ { 1 } } } , \tau _ { g } \right \} \right ) \right ) \text { (Lemma 3)} \\ & = \frac { m ! } { d _ { 2 } ! } \omega _ { m } \left ( y ^ { \frac { d _ { 2 } } { d _ { 1 } } } 2 ^ { m } 1 ( y ^ { \frac { 1 } { d _ { 1 } } } \leq \tau _ { g } ) + y ^ { \frac { d _ { 2 } } { d _ { 1 } } } \left ( \frac { \tau _ { g } } { y ^ { \frac { \frac { d _ { 2 } } { d _ { 1 } } } { y ^ { 1 } } } } \right ) ^ { d _ { 2 } - m } \left ( 1 + \left ( \frac { \tau _ { g } } { y ^ { \frac { d _ { 1 } } { d _ { 1 } } } } \right ) ^ { m } \right ) ^ { \frac { 1 } { ( y ^ { d _ { 1 } } + \tau _ { g } ) } } / \\ & \leq \frac { m ! } { d _ { 2 } ! } \omega _ { m } 2 ^ { m } \left ( y ^ { \frac { d _ { 2 } } { d _ { 1 } } } 1 ( y ^ { \frac { 1 } { d _ { 1 } } } \leq \tau _ { g } ) + y ^ { \frac { d _ { 2 } } { d _ { 1 } } } \left ( \frac { \tau _ { g } } { ( 2 K _ { I } \sqrt { m } ) ^ { \frac { 1 } { d _ { 1 } } } } \right ) ^ { d _ { 2 } - m } 1 ( y ^ { \frac { \frac { 1 } { d _ { 1 } } } { d _ { 1 } } } > \tau _ { g } ) \right ) \\ & \leq C _ { K _ { I } , m } ^ { ( 2 1 , 1 ) } \max \left \{ 1 , \tau _ { g } ^ { d _ { 2 } - m } \right \} \frac { d _ { 2 } ^ { \frac { 2 } { d _ { 1 } } } } { y ^ { \frac { d _ { 1 } } { d _ { 1 } } } } , \\ & \text {where } C _ { K _ { I } , m } ^ { ( 2 1 , 1 ) } = m ! \omega _ { m } 2 ^ { m } \left ( 2 K _ { I } \sqrt { m } \right ) ^ { m } . \text { By applying} \left ( B . 2 \right ) \text { and } ( B . 3 ) , \text { we get the upper bound}$$

where C γ(21,1) = m!ωm2m (2K1√m)m. By applying (B.2) and (B.3), we get the upper bound K1,m on the conditional cdf of |Xn − Xn−1| d1 given X1, . . . , Xn−1 in (B.1) as |Rm

$$P ^ { ( n ) } \left ( \| X _ { n } - X _ { n - 1 } \| _ { \mathbb { R } ^ { m } } ^ { d _ { 1 } } & \leq y | X _ { 1 } , \dots , X _ { n - 1 } \right ) \leq K _ { p } C _ { K _ { 1 } , m } ^ { ( 2 1 , 1 ) } \max \left \{ 1 , \tau _ { g } ^ { d _ { 2 } - m } \right \} y ^ { \frac { d _ { 2 } } { d _ { 1 } } } \\ & \leq C _ { K _ { 1 } , K _ { p } , m } ^ { ( 2 1 ) } \max \left \{ 1 , \tau _ { g } ^ { d _ { 2 } - m } \right \} y ^ { \frac { d _ { 2 } } { d _ { 1 } } } , \quad ( B . 4 )$$

where γ(21) y(21,1) = m!Kpωm2m (2K1√m)m is a constant depending only on K1,Kp,m K1,m K1, Kp, and m.

□

Lemma 6. Fix τg, τe ∈ (0, ∞], KI ∈ [1, ∞), Kv ∈ (0, 2−m], Kp ∈ [(2K1)m, ∞), d1, d2 ∈ N, with τg ≤ Te and 1 ≤ d1 &lt; d2 ≤ m. Let X1,. .., Xn ∼ P ∈ Pd2 Then for all τg,Te,K1,Kv,Kp L &gt; 0,

$$P ^ { ( n ) } \left [ \sum _ { i = 1 } ^ { n - 1 } \| X _ { i + 1 } - X _ { i } \| _ { \mathbb { R } ^ { m } } ^ { d _ { 1 } } \leq L \right ] \leq \frac { \left ( C _ { K _ { 1 } , K _ { p } , m } ^ { ( 6 ) } \right ) ^ { n - 1 } L ^ { \frac { d _ { 2 } } { d _ { 1 } } ( n - 1 ) } \max \left \{ 1 , \tau _ { g } ^ { ( d _ { 2 } - m ) ( n - 1 ) } \right \} } { ( n - 1 ) ^ { \left ( \frac { d _ { 2 } } { d _ { 1 } } - 1 \right ) ( n - 1 ) } ( n - 1 ) ! } , \ ( B . 5 )$$

where γ(6) is a constant depending only on K1, Kp, and m. K1,Kp,m

Proof of Lemma 6. Let Yi := ∥Xi+1 − Xi| 1d1 i = 1, . . . , n − 1, and let p(n) be the ∑Yi =1

<!-- p:35 -->


n−2 cumulative distribution function of ΣYi. Then from Claim 21, probability of the d1i=1 squared length of the path being bounded by L, P(n) ∑ Yi ≤ L , is upper bounded as i=1

×

$$P ^ { ( n ) } & \left ( \sum _ { i = 1 } ^ { n - 1 } Y _ { i } \leq L \right ) \\ & = \int _ { 0 } ^ { L } P ^ { ( n ) } \left ( Y _ { n - 1 } \leq y _ { n - 1 } | \sum _ { i = 1 } ^ { n - 2 } Y _ { i } = L - y _ { n - 1 } \right ) d P _ { n - 2 } ^ { ( n ) } \left ( L - y _ { n - 1 } \right ) \\ & \leq C _ { K _ { 1 } , K _ { p } , m } ^ { ( 2 1 ) } \max \left \{ 1 , \tau _ { g } ^ { d _ { 2 } - m } \right \} \int _ { 0 } ^ { L } \frac { d _ { 1 } ^ { 2 } } { y _ { n - 1 } ^ { 1 } } d P _ { n - 2 } ^ { ( n ) } \left ( L - y _ { n - 1 } \right ) \left ( \text {Claim } 2 1 \right ) \\ & = C _ { K _ { 1 } , K _ { p } , m } ^ { ( 2 1 ) } \max \left \{ 1 , \tau _ { g } ^ { d _ { 2 } - m } \right \} \\ & \times \left ( \left [ - y _ { n - 1 } ^ { \frac { 2 } { d _ { 1 } } } P \left ( \sum _ { i = 1 } ^ { n - 2 } Y _ { i } \leq L - y _ { n - 1 } \right ) \right ] ^ { L } + \int _ { 0 } ^ { L } P \left ( \sum _ { i = 1 } ^ { n - 2 } Y _ { i } \leq L - y _ { n - 1 } \right ) d ^ { \left ( \frac { d _ { 2 } } { d _ { 1 } } \right ) } \right ) \\ & = C _ { K _ { 1 } , K _ { p } , m } ^ { ( 2 1 ) } \max \left \{ 1 , \tau _ { g } ^ { d _ { 2 } - m } \right \} \int _ { 0 } ^ { L } P \left ( \sum _ { i = 1 } ^ { n - 2 } Y _ { i } \leq L - y _ { n - 1 } \right ) \frac { d _ { 2 } - \frac { \frac { d _ { 2 } - d _ { 1 } } { d _ { 1 } } } { d _ { 1 } y _ { n - 1 } } d y _ { n - 1 } .$$

n−1 By repeating this argument, we get an upper bound of P(n) ∑ Yi ≤ L as i=1

$$P ^ { ( n ) } \left ( \sum _ { i = 1 } ^ { n - 1 } Y _ { i } \leq L \right ) \leq \left ( \frac { d _ { 2 } } { d _ { 1 } } C _ { K _ { 1 } , K _ { p } , m } ^ { ( 2 1 ) } \max \left \{ 1 , \tau _ { g } ^ { d _ { 2 } - m } \right \} \right ) ^ { n - 1 } \int _ { \sum _ { i = 1 } ^ { n - 1 } y _ { i } \leq L } \prod _ { i = 1 } ^ { n - 1 } y _ { i } ^ { \frac { d _ { 2 } - d _ { 1 } } { d _ { 1 } } } d y .$$

n−1 Hence we get a further upper bound of P(n) ∑∥|Xi+1 − Xi|| d1 in (B.5) with apRm i=1

<!-- p:36 -->


plying the AM-GM inequality as

$$& \frac { \sum _ { i = 1 } ^ { n - 1 } ( x _ { i + 1 } - x _ { i } \| _ { \mathbb { R } ^ { m } } d _ { 1 } \leq L ) } { \leq \left ( \frac { d _ { 2 } } { d _ { 1 } } c _ { K _ { 1 } , K _ { p } , m } \max \left \{ 1 , \tau _ { g } ^ { d _ { 2 } - m } \right \} \right ) ^ { n - 1 } _ { \sum _ { i = 1 } ^ { d _ { 1 } } y _ { i } \leq L } \frac { \prod _ { i = 1 } ^ { n - 1 } \frac { d _ { 2 } - d _ { 1 } } { d _ { i } } } { \sum _ { i = 1 } ^ { d _ { 1 } } y _ { i } \leq L } \\ & \leq \left ( C _ { K _ { 1 } , K _ { p } , m } ^ { ( 6 ) } \right ) ^ { n - 1 } L ^ { \frac { d _ { 2 } } { d _ { 1 } } ( n - 1 ) } \max \left \{ 1 , \tau _ { g } ^ { ( d _ { 2 } - m ) ( n - 1 ) } \right \} \\ & \quad \times \int _ { \sum _ { i = 1 } ^ { n - 1 } \left ( \frac { n - 1 } { n - 1 } y _ { i } \right ) } ^ { ( d _ { 2 } - n - 1 ) } d y _ { n - 1 } \cdots d y _ { 1 } \left ( b y \ A M - G M \text { inequality} \right ) \\ & = \frac { \left ( C _ { K _ { 1 } , K _ { p } , m } ^ { ( 6 ) } \right ) ^ { n - 1 } L ^ { \frac { d _ { 2 } } { d _ { 1 } } ( n - 1 ) } \max \left \{ 1 , \tau _ { g } ^ { ( d _ { 2 } - m ) ( n - 1 ) } \right \} } { \left ( n - 1 \right ) ^ { \left ( \frac { d _ { 2 } } { d _ { 1 } } - 1 \right ) ( n - 1 ) } } \\ & \quad \times \int _ { 0 } ^ { 1 } \int _ { \sum _ { i = 2 } ^ { n - 2 } y _ { i } \leq z } ^ { \frac { ( d _ { 2 } - d ) ( n - 1 ) } { d _ { 1 } } } d y _ { n - 2 } \cdots d y _ { 1 } d z \\ & = \frac { \left ( C _ { K _ { 1 } , K _ { p } , m } ^ { ( 6 ) } \right ) ^ { n - 1 } L ^ { \frac { d _ { 2 } } { d _ { 1 } } ( n - 1 ) } \max \left \{ 1 , \tau _ { g } ^ { ( d _ { 2 } - m ) ( n - 1 ) } \right \} } { \left ( n - 1 \right ) ^ { \left ( \frac { d _ { 2 } - 1 } { d _ { 1 } } \right ) ( n - 1 ) } ( n - 2 ) ! } \int _ { 0 } ^ { 1 } z ^ { \frac { d _ { 2 } ( n - 1 ) } { d _ { 1 } } - 1 } d z \\ & \leq \frac { \left ( C _ { K _ { 1 } , K _ { p } , m } ^ { ( 6 ) } \right ) ^ { n - 1 } L ^ { \frac { d _ { 2 } } { d _ { 1 } } ( n - 1 ) } \max \left \{ 1 , \tau _ { g } ^ { ( d _ { 2 } - m ) ( n - 1 ) } \right \} } { \left ( n - 1 \right ) ^ { \left ( \frac { d _ { 2 } - 1 } { d _ { 1 } } \right ) ( n - 1 ) } ( n - 1 ) ! } , \\ & \quad \text {where } C _ { K _ { 1 } , K _ { p } , m } ^ { ( 6 ) } = m C _ { K _ { 1 } , K _ { p } , m } ^ { ( 2 1 ) } \text { is a constant depending only on } K _ { 1 } , K _ { p } , \text { and } m . \\$$

γ(6) γ(21) where K1,Kp,m = mC K1,Kp,m is a constant depending only on K1, Kp, and m.

Lemma 22. (Space-filling curve) There exists a surjective map ψd : [0, 1] → [0, 1]d which is Hölder continuous of order 1/d, i.e.

$$0 \leq \forall s , t \leq 1 , \ \| \psi _ { d } ( s ) - \psi _ { d } ( t ) \| _ { \mathbb { R } ^ { d } } \leq 2 \sqrt { d + 3 } | s - t | ^ { 1 / d } .$$

Such a map is called a space-illing curve.

- [ ] Proof of Lemma 22. [See Buchin, 2008, Chapter 2.1.6]. □

Lemma 7. Fix τg, τe ∈ (0, ∞], KI ∈ [1, ∞), Kν ∈ (0, 2−m], d1 ∈ N, with τg ≤ τl. Let p and X1, . . . , Xn ∈ M. Then Tg,Te,Kp,Kv

<!-- p:37 -->


$$\min _ { \sigma \in S _ { n } } \sum _ { i = 1 } ^ { n - 1 } \| X _ { \sigma ( i + 1 ) } - X _ { \sigma ( i ) } \| _ { \mathbb { R } ^ { m } } ^ { d _ { 1 } } \leq C _ { K _ { I } , K _ { v } , m } ^ { ( 7 ) } \max \left \{ 1 , \tau _ { g } ^ { d _ { 1 } - m } \right \} ,$$

where ~(7) is a constant depending only on K1, Kv, and m. K1,Kv,m

Proof of Lemma 7. When d1 = 1, the length of TSP path is bounded by the length of the curve volM(M) as in Figure 3.1, and Lemma 3 implies volM(M) ≤ C γ(3) max {1, τ1−m} , K1,m hence (2)) K1,Kv,m can be set as ~(7) K1,Kv,m ~(3) K1,m, as described before.

Consider d1 &gt; 1, and let r := 2√3τg. By scaling the space-filling curve in Lemma 22, there exists a surjective map ψd1 : [0, 1] → [−r, r]d1 and ψm : [0, 1] → [−K1, K1]m that satisfies

$$0 \leq \forall s , t \leq 1 , \, \| \psi _ { d _ { 1 } } ( s ) - \psi _ { d _ { 1 } } ( t ) \| _ { \mathbb { R } ^ { d _ { 1 } } } \leq 4 r \sqrt { d _ { 1 } + 3 } | s - t | ^ { 1 / d _ { 1 } }$$

$$0 \leq \forall s , t \leq 1 , \, \| \psi _ { m } ( s ) - \psi _ { m } ( t ) \| _ { \mathbb { R } ^ { m } } \leq 4 K _ { I } \sqrt { m + 3 } | s - t | ^ { 1 / m }$$

Now, from Lemma 4, M can be covered by N balls of radius r, denoted by

$$B _ { M } ( p _ { 1 } , r ) , \dots , B _ { M } ( p _ { N } , r ) ,$$

2d1 volM(M) with N ≤ Since ψm : [0, 1] → [−K1, K1]m in (B.9) is surjective, we can find Kvrd1ωd1 a right inverse Ψm : [−K1, K1]m → [0, 1] that satisfies ψm(Ψm(p)) = p, i.e.

$$[ 0 , 1 ] \Longleftrightarrow [ - K _ { I } , K _ { I } ] ^ { m } .$$

Reindex pk with respect to Ψm so that

$$\Psi _ { m } ( p _ { 1 } ) < \dots < \Psi _ { m } ( p _ { N } ) .$$

) BM (pk, r), since dM(pk, p) &lt; r, the condition (3) in Definition 2 implies that we can find φk(p) ∈ BRd1 (0, r) such that exppk(φk(p)) = p. So this shows

$$B _ { M } ( p _ { k } , r ) \subset \exp _ { p _ { k } } \left ( B _ { \mathbb { R } ^ { d _ { 1 } } } ( 0 , r ) \right ) .$$

Now consider the composition of the exponential map exppk and ψd1 in (B.8), exppk ψd1 : [0, 1] → M. Then

$$B _ { M } ( p _ { k } , r ) \subset \exp _ { p _ { k } } \left ( B _ { \mathbb { R } ^ { d _ { 1 } } } ( 0 , r ) \right ) \subset \exp _ { p _ { k } } \left ( [ - r , r ] ^ { d _ { 1 } } \right ) = \exp _ { p _ { k } } \circ \psi _ { d _ { 1 } } \left ( [ 0 , 1 ] \right ) ,$$

<!-- p:38 -->


where the last equality is from that ψd1 in (B.8) is surjective. So exppk oψd1 : [0, 1] → M Ss t  ] ← (   :    t   os (  t   es (exppk oψd1)(Ψk(p)) = p, i.e.

$$[ 0 , 1 ] \Longleftrightarrow \underbrace { [ - r , r ] } _ { \Psi _ { k } } \xrightarrow { \exp _ { p _ { k } } } M \supset B _ { M } ( p _ { k } , r ) .$$

Then, reindex X1, . . . , Xn with respect to Ψm and Ψk as {Xk,j}1≤k≤N, 1≤j≤nk, where Xk,1, . . . , Xk,nk ∈ BM(pk, r) and

$$\Psi _ { k } ( X _ { k , 1 } ) < \dots < \Psi _ { k } ( X _ { k , n _ { k } } ) .$$

Let σ ∈ Sn be the corresponding order of index, so that the d1-squared length of the path n−1 ∑∥Xσ(i+1) − Xσ(i)∥|km d1 is factorized as i=1

$$\sum _ { i = 1 } ^ { n - 1 } \| X _ { \sigma ( i + 1 ) } - X _ { \sigma ( i ) } \| _ { \mathbb { R } ^ { m } } ^ { d _ { 1 } } = \sum _ { k = 1 } ^ { N } \sum _ { j = 1 } ^ { n _ { k } - 1 } \| X _ { k , j + 1 } - X _ { k , j } \| _ { \mathbb { R } ^ { m } } ^ { d _ { 1 } } + \sum _ { k = 1 } ^ { N - 1 } \| X _ { k + 1 , 1 } - X _ { k , n _ { k } } \| _ { \mathbb { R } ^ { m } } ^ { d _ { 1 } } .$$

N nk−1 First, consider the first term Σ Σ ∥Xk,j+1 − Xk,jllkm in (B.15). For all 1 ≤ k ≤ N, by k=1 j=1 nk−1 applying Lemma 5, Σ ∥|Xk,j+1 − Xk,j|im is upper bounded as j=1

$$& \text {applying lemma 5} , \ \sum _ { j = 1 } ^ { \ n _ { k } - 1 } \| X _ { k , j + 1 } - X _ { k , j } \| _ { \mathbb { R } ^ { m } } ^ { d _ { 1 } } \text { is upper bounded as} \\ & \quad \sum _ { j = 1 } ^ { \ n _ { k } - 1 } \| X _ { k , j + 1 } - X _ { k , j } \| _ { \mathbb { R } ^ { m } } ^ { d _ { 1 } } \\ & \leq \sum _ { j = 1 } ^ { \ n _ { k } - 1 } \| ( \exp _ { p _ { k } } \circ \psi _ { d _ { 1 } } ) ( \Psi _ { k } ( X _ { k , j + 1 } ) ) - ( \exp _ { p _ { k } } \circ \psi _ { d _ { 1 } } ) ( \Psi _ { k } ( X _ { k , j } ) ) \| _ { \mathbb { R } ^ { m } } ^ { d _ { 1 } } \text { (from } ( B . 1 3 ) ) \\ & \leq \left ( \frac { \sinh ( \sqrt { 2 } / r / \tau _ { \ell } ) } { \sqrt { 2 } r / \tau _ { \ell } } \right ) ^ { d _ { 1 } } \sum _ { j = 1 } ^ { \ n _ { k } - 1 } \| \psi _ { d _ { 1 } } ( \Psi _ { k } ( X _ { k , j + 1 } ) ) - \psi _ { d _ { 1 } } ( \Psi _ { k } ( X _ { k , j } ) ) \| _ { \mathbb { R } ^ { d _ { 1 } } } ^ { d _ { 1 } } \text { (Lemma 5)} \\ & \leq \left ( \frac { 2 \sqrt { ( d _ { 1 } + 3 ) \sinh ( \sqrt { 2 } r / \tau _ { \ell } ) } } { r / \tau _ { \ell } } \right ) ^ { d _ { 1 } } \sum _ { j = 1 } ^ { \ n _ { k } - 1 } | \Psi _ { k } ( X _ { k , j + 1 } ) - \Psi _ { k } ( X _ { k , j } ) | \text { (from } ( B . 8 ) ) \\ & \leq \left ( \frac { 2 \sqrt { ( d _ { 1 } + 3 ) \sinh ( \sqrt { 2 } r / \tau _ { \ell } ) } } { r / \tau _ { \ell } } \right ) ^ { d _ { 1 } } r ^ { d _ { 1 } } \text { (from } ( B . 1 4 ) ) .$$

<!-- p:39 -->


Then, by applying the fact that r = 2√3τg ≤ 2√3τe and that t → sinh t is an increasing t function on t ≥ 0 to this, we have an upper bound of ∑ ∥|Xk,j+1 − Xk,jl|k as nk−1 d1 j=1

$$\sum _ { j = 1 } ^ { n _ { k } - 1 } \| X _ { k , j + 1 } - X _ { k , j } \| _ { \mathbb { R } ^ { m } } ^ { d _ { 1 } } \leq \left ( \frac { \sqrt { 2 ( d _ { 1 } + 3 ) \sinh 2 \sqrt { 6 } } } { \sqrt { 3 } } \right ) ^ { d _ { 1 } } r ^ { d _ { 1 } } .$$

N-1 And then, the second term Σ∥Xk+1,1 − Xk,nk∥dim d1 in (B.15) is upper bounded as k=1

$$k = 1 \\ \sum _ { k = 1 } ^ { N - 1 } \| X _ { k + 1 , 1 } - X _ { k , n _ { k } , \| \mathbb { R } ^ { m } } \| _ { \mathbb { R } ^ { m } } ^ { d _ { 1 } } \\ \leq 3 ^ { d _ { 1 } - 1 } \sum _ { k = 1 } ^ { N - 1 } \left ( \| X _ { k + 1 , 1 } - p _ { k + 1 } \| _ { \mathbb { R } ^ { m } } ^ { d _ { 1 } } + \| p _ { k + 1 } - p _ { k } \| _ { \mathbb { R } ^ { m } } ^ { d _ { 1 } } + \| p _ { k } - X _ { k , n _ { k } , \| \mathbb { R } ^ { m } } \| _ { \mathbb { R } ^ { m } } \right ) \\ \leq 2 \cdot 3 ^ { d _ { 1 } - 1 } ( N - 1 ) r ^ { d _ { 1 } } + 3 ^ { d _ { 1 } - 1 } \sum _ { k = 1 } ^ { N - 1 } \| \psi _ { m } ( \Psi _ { m } ( p _ { k + 1 } ) ) - \psi _ { m } ( \Psi _ { m } ( p _ { k } ) ) \| _ { \mathbb { R } ^ { d _ { 1 } } } ^ { d _ { 1 } } \pmod { ( B . 1 1 ) } \\ < 3 ^ { d _ { 1 } } ( N - 1 ) r ^ { d _ { 1 } } + 2 \cdot 3 ^ { d _ { 1 } } \sqrt { m + 3 K _ { I } } \sum _ { k = 1 } ^ { N - 1 } | \Psi _ { m } ( p _ { k + 1 } ) - \Psi _ { m } ( p _ { k } ) | ^ { \frac { d _ { 1 } } { m } } \pmod { ( B . 9 ) } \\ \leq 3 ^ { d _ { 1 } } ( N - 1 ) r ^ { d _ { 1 } } + \\ 2 \cdot 3 ^ { d _ { 1 } } \sqrt { m + 3 K _ { I } } \left ( \sum _ { k = 1 } ^ { N - 1 } | \Psi _ { m } ( p _ { k + 1 } ) - \Psi _ { m } ( p _ { k } ) | ^ { \frac { d _ { 1 } } { m } } \sum _ { i = 1 } ^ { N - 1 } \left ( \sum _ { k = 1 } ^ { m - d _ { 1 } } \right ) \\ ( using Hodler's inequlatiy ) \\ \leq 3 ^ { d _ { 1 } } ( N - 1 ) r ^ { d _ { 1 } } + 2 \cdot 3 ^ { d _ { 1 } } \sqrt { m + 3 K _ { I } } ( N - 1 ) ^ { 1 - \frac { d _ { 1 } } { m } } \pmod { ( B . 1 2 ) } .$$

n−1 Hence, by plugging in (B.16) and (B.17) to (B.15), ∑ ∥Xσ(i+1) −Xσ(i)lldm is upper bounded d1 i=1

<!-- p:40 -->


$$& \frac { \text {Journal of Computational Geometry} } { \ } \\ & \quad \text {as} \\ & \quad \sum _ { i = 1 } ^ { n - 1 } \| X _ { \sigma ( i + 1 ) } - X _ { \sigma ( i ) } \| _ { \mathbb { R } ^ { m } } ^ { d _ { 1 } } \\ & \quad < \left ( \left ( \frac { \sqrt { 2 ( d _ { 1 } + 3 ) \sinh 2 \sqrt { 6 } } } \right ) ^ { d _ { 1 } } + 3 ^ { d _ { 1 } } \right ) r ^ { d _ { 1 } } N + 2 \cdot 3 ^ { d _ { 1 } } \sqrt { m + 3 } K _ { I } N ^ { 1 - \frac { d _ { 1 } } { m } } \\ & \quad < \frac { ( 2 \sqrt { d _ { 1 } + 3 } \sinh 2 \sqrt { 6 } ) ^ { d _ { 1 } } + 6 ^ { d _ { 1 } } } { K _ { v } \omega _ { d _ { 1 } } } v o l _ { M } ( M ) + \frac { 2 \cdot 3 ^ { \frac { d _ { 1 } } { 2 } } \sqrt { m + 3 } K _ { I } } { ( K _ { v } \omega _ { d _ { 1 } } ) ^ { 1 - \frac { d _ { 1 } } { m } } \tau _ { g } } \tau _ { g } ^ { d _ { 1 } - 1 } ( \text {vol} _ { M } ( M ) ) ^ { 1 - \frac { d _ { 1 } } { m } } \\ & \quad \leq \frac { ( 2 ( \sinh 2 \sqrt { 6 } ) \sqrt { m + 3 } ) ^ { d _ { 1 } } 2 K _ { I } } { \min \{ 1 , K _ { v } \omega _ { d _ { 1 } } \} } \times \\ & \quad \left ( C _ { K _ { I } , m } ^ { ( 3 ) } \max \left \{ 1 , \tau _ { g } ^ { d _ { 1 } - m } \right \} + \tau _ { g } ^ { \frac { d _ { 1 } ( \frac { d _ { 1 } - 1 } { m } ) } { m } } \left ( C _ { K _ { I } , m } ^ { ( 3 ) } \max \left \{ 1 , \tau _ { g } ^ { d _ { 1 } - m } \right \} \right ) ^ { 1 - \frac { d _ { 1 } } { m } } \right ) \text { (from lemma 3)} \\ & \quad \leq C _ { K _ { I } , k _ { v , m } } ^ { ( 7 ) } \max \left \{ 1 , \tau _ { g } ^ { d _ { 1 } - m } \right \} , \\ & \quad \text {with some constant } C _ { K _ { I } , K _ { v } , m } ^ { ( 7 ) } \text { which depends only on } m , \, K _ { v } , \text { and } K _ { I } . \text { Hence we have the } \\ & \quad \text {same upon bound for } \min \{ 1 , \tau _ { Y } \, \sum _ { \substack { Y _ { I } , \, U _ { I } , \, U _ { V } \, \text {swell, as} \, \text {in} \, ( R 7 ) \\ \square } } \prod _ { \substack { U _ { I } , \, U _ { V } \, \text {swell} \, ( R 7 ) \\ \square } }$$

(7) with some constant K1,Kv,m which depends only on m, Kv, and K1. Hence we have the same upper bound for min ∑∥Xσ(i+1) − Xσ(i)ldm a n−1 d1 as well, as in (B.7). □ σ∈Sni=1

'(∞'(1)]   [-)   (∞]   [∞0)  1 1 x, 8 )) d1, d2 ∈ N, with τg ≤ τe and 1 ≤ d1 &lt; d2 ≤ m. Let dn be in (3.4). Then either for d = d1 or d = d2,

$$& \sup _ { P \in \mathcal { P } _ { \tau _ { g } , \tau _ { k } , K _ { v } , K _ { p } } } \mathbb { E } _ { P ^ { ( n ) } } \left ( \ell \left ( \widehat { d } _ { n } , d ( P ) \right ) \right ] \\ & \leq 1 ( d = d _ { 2 } ) \left ( C _ { K _ { 1 } , K _ { p } , K _ { v , m } } ^ { ( 8 ) } \right ) ^ { n } \max \left \{ 1 , \tau _ { g } ^ { - \left ( \frac { d _ { 2 } } { d _ { 1 } } + m + 2 d _ { 2 } \right ) n } \right \} n \left \{ \frac { - \left ( \frac { d _ { 2 } } { d _ { 1 } } - 1 \right ) n } { n ^ { - \left ( \frac { d _ { 2 } } { d _ { 1 } } - 1 \right ) n } , } \quad ( B . 1 8 )$$

where K1,Kp,Kv,m (8) ∈ (0, ∞) is a constant depending only on K1, Kp, Kv, and m.

Proof of Proposition 8. Consider first the case d = d1. Then for all P ∈ Pd1 and Tg,Te,K1,Kv,Kp X1, . . . , Xn ∼ P, by Lemma 7,

$$\min _ { \sigma \in S _ { n } } \left \{ \sum _ { i = 1 } ^ { n - 1 } \| X _ { \sigma ( i + 1 ) } - X _ { \sigma ( i ) } \| _ { \mathbb { R } ^ { m } } ^ { d _ { 1 } } \right \} \leq C _ { K _ { I } , K _ { v } , m } ^ { ( 7 ) } \max \left \{ 1 , \tau _ { g } ^ { d _ { 1 } - m } \right \} ,$$

<!-- p:41 -->


hence λn in (3.4) always satisfies dn(X) = d1 = d(P), i.e. the risk of dn satisfies

$$P ^ { ( n ) } \left [ \widehat { d } _ { n } ( X _ { 1 } , \dots , X _ { n } ) = d _ { 2 } \right ] = 0 .$$

For the case when d = d2, for all P ∈ Pd2 P9,τe,K1,Kv,Kp, the risk of n in (3.4) is upper bounded as

$$& \text {For the case when } d = d _ { 2 } , \text { for all } P \in \mathcal { P } _ { \tau , \tau , K _ { 1 } , K _ { v } , K _ { p } } ^ { d _ { 2 } } , \text { the risk of } \widehat { d } _ { m } \text { in } ( 3 . 4 ) \text { is upper bounded} \\ & \quad \text {as} \\ & \quad P ^ { ( n ) } \left [ \widehat { d } _ { n } ( X _ { 1 } , \dots , X _ { n } ) = d _ { 1 } \right ] \\ & \quad = P \left [ \bigcup _ { \sigma \in S _ { n } } \sum _ { i = 1 } ^ { n - 1 } | X _ { \sigma ( i + 1 ) } - X _ { \sigma ( i ) } | \leq C _ { K _ { 1 } , K _ { v } , m } ^ { ( 7 ) } \max \left \{ 1 , \tau _ { g } ^ { d _ { 1 } - m } \right \} \right ] \\ & \quad \leq \sum _ { \sigma \in S _ { n } } P \left [ \sum _ { \substack { i = 1 \\ i = 1 } } ^ { n - 1 } | X _ { \sigma ( i + 1 ) } - X _ { \sigma ( i ) } | \leq C _ { K _ { 1 } , K _ { v } , m } ^ { ( 7 ) } \max \left \{ 1 , \tau _ { g } ^ { d _ { 1 } - m } \right \} \right ] \\ & = n ! P \left [ \sum _ { i = 1 } ^ { n - 1 } | X _ { i + 1 } - X _ { i } | \leq C _ { K _ { 1 } , K _ { v } , m } ^ { ( 7 ) } \max \left \{ 1 , \tau _ { g } ^ { d _ { 1 } - m } \right \} \right ] \\ & = n \left ( C _ { K _ { 1 } , K _ { p } , m } ^ { ( 6 ) } \right ) ^ { n - 1 } \left ( C _ { K _ { 1 } , K _ { v } , m } ^ { ( 7 ) } \max \left \{ 1 , \tau _ { g } ^ { d _ { 1 } - m } \right \} \right ) ^ { \frac { d _ { 2 } ( n - 1 ) } { 4 } } \max \left \{ 1 , \tau _ { g } ^ { ( d _ { 2 } - m ) ( n - 1 ) } \right \} \\ & = \frac { ( n - 1 ) ^ { ( \frac { d _ { 2 } } { 4 } - 1 ) ( n - 1 ) } } { ( n - 1 ) ^ { ( \frac { d _ { 2 } } { 4 } - 1 ) ( n - 1 ) } } \\ & \text {where the last line is implied by Lemma 6. Theorefore, by combining (B.19) and (B.20), the
 & r i s k \text { is upper bounded as in } ( B . 18 ) , \text { as}$$

where the last line is implied by Lemma 6. Therefore, by combining (B.19) and (B.20), the risk is upper bounded as in (B.18), as

$$\text {risk is upper bounded as in (B.18), as} \\ \sup _ { P \in \mathcal { P } _ { \gamma , \tau _ { 1 } , K _ { 1 } , K _ { v } , K _ { p } } } \mathbb { E } _ { P ( n ) } \left [ \ell \left ( \widehat { d } _ { n } , d ( P ) \right ) \right ] \\ n \left ( C _ { K _ { 1 } , K _ { p } , m } ^ { ( 6 ) } \left ( C _ { K _ { 1 } , K _ { v } , m } ^ { ( 7 ) } \right ) ^ { \frac { d _ { 2 } } { d _ { 1 } } } \right ) ^ { n - 1 } \max \left \{ 1 , \tau _ { g } ^ { - \left ( \frac { d _ { 2 } } { d _ { 1 } } m + m - 2 d _ { 2 } \right ) ( n - 1 ) } \right \} \\ \leq 1 ( d = d _ { 2 } ) \frac { ( n - 1 ) ^ { \left ( \frac { d _ { 2 } } { d _ { 1 } } - 1 \right ) ( n - 1 ) } } { ( n - 1 ) ^ { \left ( \frac { d _ { 2 } } { d _ { 1 } } - 1 \right ) ( n - 1 ) } } \\ \leq 1 ( d = d _ { 2 } ) \left ( C _ { K _ { 1 } , K _ { p } , K _ { v } , m } ^ { ( 8 ) } \right ) ^ { n } \max \left \{ 1 , \tau _ { g } ^ { - \left ( \frac { d _ { 2 } } { d _ { 1 } } m + m - 2 d _ { 2 } \right ) n } \right \} n ^ { - \left ( \frac { d _ { 2 } } { d _ { 1 } } - 1 \right ) n } , \\ \text {for some } C _ { K _ { 1 } , K _ { p } , K _ { v } , m } ^ { ( 8 ) } \quad \text {that depends only on } K _ { 1 } , K _ { p } , K _ { v } \text { and } m ,$$

for some γ(8) that depends only on K1, Kp, Kv, and m.

K1,Kp,Kv,m

Proposition 9. Fix τg, τe ∈ (0, ∞], KI ∈ [1, ∞), Kv ∈ (0, 2−m], Kp ∈ [(2K1)m, ∞), d1, d2 ∈ N, with τg ≤ τl and 1 ≤ d1 &lt; d2 ≤ m. Then

$$1 , \, d _ { 2 } \in \mathbb { N } , \, \text {with } & \, 1 _ { g } \supset \mathcal { I } _ { \ell } \ a n d \ 1 \supset a _ { 1 } < a _ { 2 } \leq m . \ \text {In} \ h e n \\ & \inf _ { \widetilde { d } _ { n } \ P \in \mathcal { P } _ { 1 } \cup \mathcal { P } _ { 2 } } \mathbb { E } _ { P ^ { ( n ) } } \left [ \ell \left ( \widehat { d } _ { n } , d ( P ) \right ) \right ] \\ & \leq \left ( C _ { K _ { 1 } , K _ { 2 } , K _ { v } , m } ^ { ( 8 ) } \right ) ^ { n } \max \left \{ 1 , \tau _ { g } + \frac { - \left ( \frac { d _ { 2 } } { d _ { 1 } } m + m - 2 d _ { 2 } \right ) n } { \tau _ { g } } \right \} n ^ { - \left ( \frac { d _ { 2 } } { d _ { 1 } } - 1 \right ) n } ,$$

<!-- p:42 -->


γ(8) where K1,Kp,Kv,m is from Proposition 8 and

$$\mathcal { P } _ { 1 } = \mathcal { P } _ { \tau _ { g } , \tau _ { \ell } , K _ { I } , K _ { v } , K _ { p } } , \quad \mathcal { P } _ { 2 } = \mathcal { P } _ { \tau _ { g } , \tau _ { \ell } , K _ { I } , K _ { v } , K _ { p } } .$$

Proof of Proposition 9. Applying Proposition 8 to (3.2) yields

$$\ f o f \, P r o p o s i t i o n & \ 9 . \ \ A p l y i n g \, P r o p o s i t i o n \ 8 \ t o \ ( 3 . 2 ) \ y i e l d s \\ & \inf _ { \widehat { d } _ { n } \ P \in \mathcal { P } _ { \tau _ { g } , \tau _ { \ell } , K _ { I } , K _ { v } , K _ { p } } \cup \mathcal { P } _ { \tau _ { g } , \tau _ { \ell } , K _ { I } , K _ { v } , K _ { p } } } \ \mathbb { E } _ { P ^ { ( n ) } } \left [ \ell \left ( \widehat { d } _ { n } , d ( P ) \right ) \right ] \\ & \leq \sup _ { P \in \mathcal { P } _ { \tau _ { g } , \tau _ { \ell } , K _ { I } , K _ { v } , K _ { p } } \cup \mathcal { P } _ { \tau _ { g } , \tau _ { \ell } , K _ { I } , K _ { v } , K _ { p } } } \ \mathbb { E } _ { P ^ { ( n ) } } \left [ \ell \left ( \widehat { d } _ { n } , d ( P ) \right ) \right ] \\ & \leq \left ( C _ { K _ { I } , K _ { p } , K _ { v } , m } ^ { ( 8 ) } \right ) ^ { n } \max \left \{ 1 , \tau _ { g } \left \} n \left \{ \frac { d _ { 2 } } { d _ { 1 } } \frac { d _ { m + m - 2 d _ { 2 } } } { d _ { 1 } } n \right \} n \right \} n \left ( \frac { d _ { 2 } } { d _ { 1 } } - 1 \right ) n .$$

Hence the minimax rate Rn in (2.6) is upper bounded as in (B.21).

## C Proofs for Section 4

Lemma 11. Fix τg, τe ∈ (0, ∞], K1 ∈ [1, ∞), Kv ∈ (0, 2−m], d, ∆d ∈ N, with τg ≤ τe and be a d-dimensional manifold of global reach ≥ τg, local reach ≥ τe, which is embedded in Rm−∆d. Then

$$M \times [ - K _ { I } , K _ { I } ] ^ { \Delta d } \in \mathcal { M } _ { \tau _ { g } , \tau _ { \ell } , K _ { I } , K _ { v } } ^ { d + \Delta d } ,$$

which is embedded in Rm.

Proof of Lemma 11. For showing (C.1), we need to show 4 conditions in Definition 2. The other conditions are rather obvious and the critical condition is (2), i.e. the global reach condition and the local reach condition. Showing the local reach condition is almost identical to showing the global reach condition, so we will focus on the global reach condition. From the definition of the global reach in Definition 1, we need to show that for all x ∈ Rm with distRm(x, M × [−K1, K1]∆d) &lt; τg, x has the unique closest point πM×[−K1,K1]∆d(x) on M × [−K1, K1].

Let x ∈ Rm be satisfying distRm(x, M × [−K1, K1]∆d) &lt; τg, and let y ∈ M × [−K1, K1]∆d. Then the distance between x and y can be factorized as their distance on first m − ∆d coordinates and last ∆d coordinates,

$$d i s t _ { \mathbb { R } ^ { m } } \left ( x , y \right ) \\ & = \sqrt { d i s t _ { \mathbb { R } ^ { m - \Delta d } } \left ( \Pi _ { 1 ; m - \Delta d } ( x ) , \Pi _ { 1 ; m - \Delta d } ( y ) \right ) ^ { 2 } + d i s t _ { \mathbb { R } ^ { \Delta d } } \left ( \Pi _ { ( m - \Delta d + 1 ) ; m } ( x ) , \Pi _ { ( m - \Delta d + 1 ) ; m } ( y ) \right ) ^ { 2 } } .$$

<!-- p:43 -->


For the first term in (C.2), note that the projection map Π1:m-∆d : Rm → Rm-∆d is a contraction, i.e. for all x, y ∈ Rm, distRm−∆d(I1:m−∆d(x), III1:m−∆d(y)) ≤ distRm(x, y) holds, so II1:m−∆d(x) is also within a τg-neighborhood of M = II1:m−∆d(M × [−K1, K1]∆d), i.e.

$$d i s t _ { \mathbb { R } ^ { m - \Delta d } } \left ( \Pi _ { 1 \colon m - \Delta d } ( x ) , \, M \right ) & = d i s t _ { \mathbb { R } ^ { m - \Delta d } } \left ( \Pi _ { 1 \colon m - \Delta d } ( x ) , \, \Pi _ { 1 \colon m - \Delta d } ( M \times [ - K _ { I } , K _ { I } ] ^ { \Delta d } ) \right ) \\ & \leq d i s t _ { \mathbb { R } ^ { m } } ( x , \, M \times [ - K _ { I } , K _ { I } ] ^ { \Delta d } ) < \tau _ { g } .$$

Hence from the definition of the global reach in Definition 1, πM (I1:m−∆d(x)) ∈ M uniquely exists. And from Π1:m−∆d(y) ∈ M, the distance between I1:m−∆d(x) and I1:m−∆d (y) is lower bounded by the distance between II1:m-∆d(x) and M, i.e.

$$d i s t _ { \mathbb { R } ^ { m - \Delta d } } \left ( \Pi _ { 1 \colon m - \Delta d } ( x ) , \Pi _ { 1 \colon m - \Delta d } ( y ) \right ) & \geq d i s t _ { \mathbb { R } ^ { m - \Delta d } } \left ( \Pi _ { 1 \colon m - \Delta d } ( x ) , \pi _ { M } \left ( \Pi _ { 1 \colon m - \Delta d } ( x ) \right ) \right ) \\ & = d i s t _ { \mathbb { R } ^ { m - \Delta d } } \left ( \Pi _ { 1 \colon m - \Delta d } ( x ) , M \right ) ,$$

and the equality holds if and only if II1:m−∆d (y) = πM (II1:m−∆d(x)).

The second term in (C.2) is trivially lower bounded by 0, i.e.

$$d i s t _ { \mathbb { R } ^ { \Delta d } } \left ( \Pi _ { ( m - \Delta d + 1 ) \colon m } ( x ) , \, \Pi _ { ( m - \Delta d + 1 ) \colon m } ( y ) \right ) \geq 0 ,$$

and the equality holds if and only if II(m−∆d+1):m(x) = II(m−∆d+1):m(y).

Hence by applying (C.3) and (C.4) to (C.2), distRm (x, y) is lower bounded by the distance between I1:m-∆d(x) and M, i.e.

$$d i s t _ { \mathbb { R } ^ { m } } \left ( x , y \right ) \\ = \sqrt { d i s t _ { \mathbb { R } ^ { m - d } } \left ( \Pi _ { 1 \colon m - \Delta d } ( x ) , \Pi _ { 1 \colon m - \Delta d } ( y ) \right ) ^ { 2 } + d i s t _ { \mathbb { R } ^ { \Delta d } } \left ( \Pi _ { ( m - \Delta d + 1 ) \colon m } ( x ) , \Pi _ { ( m - \Delta d + 1 ) \colon m } ( y ) \right ) ^ { 2 } } \\ \geq d i s t _ { \mathbb { R } ^ { m - \Delta d } } \left ( \Pi _ { 1 \colon m - \Delta d } ( x ) , M \right ) ,$$

and the equality holds if and only if I1:m−∆d (y) = πM (I1:m−∆d(x)) and II(m−∆d+1):m(x) = I(m−∆d+1):m(y), i.e. when y = (πM (I1:m−∆d(x)) , II(m−∆d+1):m(x)). Hence x has the unique closest point πM×[−K1,K1]∆d(x) on M × [−K1, K1] as

$$\pi _ { M \times [ - K _ { I } , K _ { I } ] ^ { \Delta d } } ( x ) = \left ( \pi _ { M } \left ( \Pi _ { 1 \colon m - \Delta d } ( x ) \right ) , \, \Pi _ { ( m - \Delta d + 1 ) \colon m } ( x ) \right ) ,$$

as in Figure C.1.

Lemma 12. Fix τe ∈ (0, ∞], K1 ∈ [1, ∞), d1, d2 ∈ N, with 1 ≤ d1 ≤ d2, and suppose τl &lt; K1. Then there exist T1, · · · , Tn ⊂ [−K1, K1]d2 such that:

- (1) The Ti's are distinct.
- (2) For each Ti, there exists an isometry Φi such that

$$T _ { i } = \Phi _ { i } \left ( [ - K _ { I } , K _ { I } ] ^ { d _ { 1 } - 1 } \times [ 0 , a ] \times B _ { \mathbb { R } ^ { d _ { 2 } - d _ { 1 } } } ( 0 , w ) \right ) ,$$

<!-- p:44 -->


Figure C.1: πM×[−K1,K1]∆d(x) satisfies Π1:m−∆d (πM×[−K1,K1]∆d(x)) = πM (I1:m−∆d(x)).

I1:m−∆d(x)

πM×[−Ky,K1]∆d(x)

2KI

I1:m−∆d (yM×[−K1,K1]∆d(x)) = πM (I1:m−∆d(x))

M

where c = 1+11 2τe (d2−d1+1) KI-τe cd2−d1 n and w = min Tl, 2τe(d2−d1+1)2([ (d2−d1)2(K1−τe)2 cd2−d1 n +1) (3)There exists M : (BRd2-d1(0, w))n → Md, one-to-one such that for each yi ∈ τg,τe,K1,Kv BRd2−d1 (0, w), 1 ≤ i ≤ n, M (y1, . . . , yn) ∩ Ti = Φi([−K1, K1]d1−1 × [0, a] × {yi}). Hence for any x1 ∈ T1, . .,xn ∈ Tn, M {−d1+1): 2 2Φ−1(xi)}1≤i≤n) passes through x1, . . . , xn.

Proof of Lemma 12. By Lemma 11, we only need to show the case for d1 = 1. This is since for d1 &gt; 1 case, we can build the set of manifolds in Md1 1 9,πe,K1,Kv by forming a Cartesian product of the manifold with the cube as in Lemma 11.

$$\product \text { of the mainfold with the cube as in Lemma 11.} \\ \text { Let } b = \frac { 2 ( d _ { 2 } - d _ { 1 } ) ( K _ { 1 } - \tau _ { \ell } ) } { ( d _ { 2 } - d _ { 1 } + \frac { 1 } { 2 } ) \left ( \left [ \frac { n } { d _ { 2 } - d _ { 1 } } \right ] + 1 \right ) } , \text { so that} \\ b \geq 2 \sqrt { 2 w \tau _ { \ell } } \quad \text {and} \quad 2 \tau _ { \ell } + \left \lfloor \frac { n } { c ^ { 2 } d - d _ { 1 } } \right \rfloor a + \left ( \left \lfloor \frac { n } { c ^ { 2 } d - d _ { 1 } } \right \rfloor + 1 \right ) b = 2 K _ { 1 } . \\$$

With such values of a, b, and w, align Ti, Ri, and Ai in a zigzag way, as in Figure C.2(a).

Then from the definition of Ti, (1) the Ti's are distinct and (2) for each Ti, there exists an isometry Φi such that Ti = Φi ([−K1, K1]d1−1 × [0, a] × BRd2−d1 (0, w)) . There exists an isometry Ψi such that Ri = Ψi ([−K1, K1]d1−1 × [0, b] × BRd2−d1 (0, w)) as well. Hence the conditions (1) and (2) are satisfied.

We are left to define M that satisfies the condition (3). Now define a map from a

set of points to a set of manifolds M : (BRd2-d1 (0, w))n → Md1, τg,Te,K1,Kv as follows. For each 4 (∪ Ai) U(UTi) U(U Ri). yi ∈ BRd2−d1 (0, wω), 1 ≤ i ≤ n, ∪ Ai ⊂ M (y1, . . . , yn) ⊂ i=1 The intersection of M (y1, . . . , yn) and Ti is a line segment Φi([− K1, K1]d1−1 × [0, a] × {yi}), as in Figure C.2(b). Our goal is to make M (y1, . . . , yn) be C1 and piecewise C2.

<!-- p:45 -->

2KI

w

R1

T1

R2

T2

R3

A1

a

b

Te

R6

T4

R5

T3

R4

A2

2KI

R7

T5

R8

T6

R9

A3

R12

T8

R11

T7

R10

x1

x2

T1

T2

x4

x3

x5

x6

x8

x7

(a) alignment of Ti, Ri, and Ai

(b) manifold passing through Xi's See Figure C.3 for the construction of the intersection of M(y1, . . . , yn) and Ri. i=1 i=1 ∂Ri are already determined. " By translation and rotation if necessary, for all p, q with −w ≤ q ≤ p ≤ w, we need to find a C2 curve with reach ≥ τe that starts from (0, p) ∈ R2, ends at (b, q) ∈ R2, and the velocities at both endpoints are parallel to (1, 0) ∈ R2, as in Figure C.3(a).

Figure C.2: This figure illustrates the case where d1 = 1 and d2 = 2. (a) shows how Ti, Ri, and Ai's are aligned in a zigzag. (b) shows for given x1 ∈ T1, . . . , xn ∈ Tn (represented as x1, . . . , xn

<!-- p:46 -->


Figure C.3: (a) We need to find a C2 curve with local reach ≥ τe that starts from (0, p) ∈ R2, ends at (b, q), and the velocities at both endpoints are parallel to (1, 0). (b) C1 and C2 are arcs of circles of radius Rl, and C3 is the cotangent segment of two circles.

个

M(y)

(0, p)

C1

(0, p)

Ri

C3

(b, q + τe)

Tl

&gt;

t0

(0, p − τe)

(b, q)

M(y)

C2

(b, q)

(a)

(b)

Let

$$t _ { 0 } = \cos ^ { - 1 } \left ( \frac { 2 \tau _ { \ell } \left ( 2 \tau _ { \ell } - ( p - q ) \right ) + b \sqrt { b ^ { 2 } - ( p - q ) \left ( 4 \tau _ { \ell } - ( p - q ) \right ) } } { b ^ { 2 } + ( 2 \tau _ { \ell } - ( p - q ) ) ^ { 2 } } \right ) ,$$

and let

$$C _ { 1 } = \{ ( 0 , p - \tau _ { \ell } ) + \tau _ { \ell } \left ( \sin t , \cos t \right ) \ | \ 0 \leq t \leq t _ { 0 } \} \, .$$

Then C1 is an arc of a circle of which center is (0, p − τe), and starts at (0, p) when t = 0 and ends at (τe sin t0, p − τe(1 − cos t0)) when t = t0. Also, the normalized velocities of C1 at endpoints are

$$( 1 , 0 ) \ a t \ ( 0 , p ) , \quad ( \cos t _ { 0 } , - \sin t _ { 0 } ) \ a t \ ( \tau _ { \ell } \sin t _ { 0 } , \ p - \tau _ { \ell } ( 1 - \cos t _ { 0 } ) ) .$$

Similarly, let

$$C _ { 2 } = \{ ( b , q + \tau _ { \ell } ) - \tau _ { \ell } \left ( \sin t , \cos t \right ) \ | \ 0 \leq t \leq t _ { 0 } \} \, .$$

Then C2 is an arc of a circle of whose center is (b, q + τe), and starts at (b, q) when t = 0 and ends at (b − τe sin t0, q + τe (1 − cos t0)) when t = t0. Also, the normalized velocities of C2 at endpoints are

<!-- p:47 -->


$$( - 1 , 0 ) \ a t \ ( b , q ) , \quad ( - \cos t _ { 0 } , \sin t _ { 0 } ) \ a t \ ( b - \tau _ { \ell } \sin t _ { 0 } , \ q + \tau _ { \ell } \left ( 1 - \cos t _ { 0 } \right ) ) .$$

Let

$$C _ { 3 } & = \left \{ ( 1 - s ) \left ( \tau _ { \ell } \sin t _ { 0 } , \ p - \tau _ { \ell } ( 1 - \cos t _ { 0 } ) \right ) + s \left ( b - \tau _ { \ell } \sin t _ { 0 } , \ q + \tau _ { \ell } \left ( 1 - \cos t _ { 0 } \right ) \right ) \\ & \quad | \ 0 \leq s \leq 1 \right \} ,$$

so that C3 is a segment joining (τe sin t0, p − τe(1 − cos t0)) (when s = 0) and (b−τe sin t0, q+ τe(1 − cos t0)) (when s = 1). Also, its velocity vector is

$$( b - \tau _ { \ell } \sin t _ { 0 } , \ q + \tau _ { \ell } \left ( 1 - \cos t _ { 0 } \right ) ) \ \text {for all } s \in [ 0 , 1 ] .$$

Then from definition of t0 in (C.6),

$$\cos t _ { 0 } \left ( q - p + 2 \tau _ { \ell } \left ( 1 - \cos t _ { 0 } \right ) \right ) + \sin t _ { 0 } \left ( b - 2 \tau _ { \ell } \sin t _ { 0 } \right ) = 0 ,$$

and this implies that (b − 2τe sin t0, q − p + 2τe (1 − cos t0)) is parallel to (cos t0, − sin t0). Hence the velocity vector of C3 in (C.9) is parallel to the velocity vector of C1 in (C.7) at (τe sin t0, p − τe(1 − cos t0)) and the velocity vector of C2 in (C.8) at (b − τe sin t0, q + τe(1 − cos t0)), i.e. C3 is cotangent to both C1 and C2. See Figure C.3(b).

Now we check whether is of global reach ≥ τe, which implies both global reach ≥ τg and local reach ≥ τe since τg ≤ τe. From [Aamari et al., 2017, Theorem 3.4], the reach τ(M) of a manifold M is realized in either the global case or the local case, where the global case refers to that there exist two points q1, q2 ∈ M with B(91+92, τ(M)) ∩ M = 2 ∅, and the local case refers to that there exists an arc-length parametrized geodesic γ such that|γ′′(0)|2 = 1 . Now from the construction, any q1, q2 ∈ M (y1, . . . , yn) with τ(M)· B(q1+q2, 2, τ)∩M (y1, . . . , yn) = ∅ can only happen when τ ≥ τe, so it suffices to check whether 2 any arc-length parametrized geodesics γ satisfies |γ"(0)||2 ≤ 1 And this is satisfied since Tl M(y1, . . . , yn) is piecewise either a straight line segment or an arc of a circle of radius τe. Hence M (y1, . . . , yn) is of global reach ≥ τe. □

n Claim 13. Let T = Sn ∏Ti where the Ti's are from Lemma 12. Let Q2 be the uniform i=1 distribution on [−K1, K1]d2, and let Pd1 be as in (4.2). Then there exists Q1 ∈ co(Pd1)

satisfying that for all x ∈ intT, there exists rx &gt; 0 such that for all r &lt; rx,

$$Q _ { 1 } \left ( \prod _ { i = 1 } ^ { n } B _ { \| \cdot \| _ { R ^ { d _ { 2 } } , \infty } } ( x _ { i } , r ) \right ) \geq 2 ^ { - n } Q _ { 2 } \left ( \prod _ { i = 1 } ^ { n } B _ { \| \cdot \| _ { \mathbb { R } ^ { d _ { 2 } } , \infty } } ( x _ { i } , r ) \right ) .$$

<!-- p:48 -->


Proof of Claim 13. Let Q1 be from (C.15) in Proposition 14. By symmetry, we can assume n that x ∈ ∏ Ti, i.e. x1 ∈ T1, . . . , xn ∈ Tn. Choose rx small enough so that B(x, rx) ⊂ intT. i=1 Then for all r &lt; rx, from the definition of Q1 in (C.15),

$$Q _ { 1 } \left ( \prod _ { i = 1 } ^ { n } B _ { \| \cdot \| _ { \mathbb { R } ^ { d _ { 2 } , \infty } } ( x _ { i } , r ) } \right ) & = \int _ { \mathcal { P } _ { 1 } } P ^ { ( n ) } \left ( \prod _ { i = 1 } ^ { n } B _ { \| \cdot \| _ { \mathbb { R } ^ { d _ { 2 } , \infty } } ( x _ { i } , r ) } \right ) d \mu _ { 1 } ( P ) \\ & = \int _ { C ^ { n } } \Phi ( y ) ^ { ( n ) } \left ( \prod _ { i = 1 } ^ { n } B _ { \| \cdot \| _ { \mathbb { R } ^ { d _ { 2 } , \infty } } ( x _ { i } , r ) } \right ) \lambda c ( y ) \\ & = \int _ { C ^ { n } } \prod _ { i = 1 } ^ { n } \lambda _ { \mathcal { M } ( y ) } \left ( B _ { \| \cdot \| _ { \mathbb { R } ^ { d _ { 2 } , \infty } } ( x _ { i } , r ) } \right ) \lambda _ { C ^ { n } } ( y ) .$$

Then from the condition (3) in Lemma 12, M (y) ∩ Ti = Φi ([−K1, K1]d1−1 × [0, a] × {yi}) holds, hence

$$\mathcal { M } ( y ) \cap B _ { \| \cdot _ { r } d _ { 2 } } ( x _ { i } , r ) \\ \begin{cases} = \Phi _ { i } \left ( B _ { \| \cdot _ { r } d _ { 1 } } \left ( \Pi _ { 1 \colon d _ { 1 } } ( \Phi _ { i } ^ { - 1 } ( x _ { i } ) ) , \ r \right ) \times \{ y _ { i } \} \right ) , & \text {if } \| y _ { i } - \Pi _ { ( d _ { 1 } + 1 ) \colon d _ { 2 } } ( \Phi _ { i } ^ { - 1 } ( x _ { i } ) ) \| _ { \mathbb { R } ^ { d _ { 2 } - d _ { 1 } } } < r , \\ \supset \emptyset , & \text {otherwise.} \end{cases}$$

And hence the volume of M (y) ∩ B1d2, (xi, r) can be lower bounded as

$$\lambda _ { \mathcal { A } ( y ) } \left ( B _ { \| \cdot \| _ { \mathbb { R } ^ { d _ { 2 } } , \infty } } ( x _ { i } , r ) \right ) \geq \frac { r ^ { d _ { 1 } } } { 2 K _ { I } ^ { d _ { 1 } - 1 } a n } I \left ( \left \| y _ { i } - \Pi _ { ( d _ { 1 } + 1 ) \cdot d _ { 2 } } ( \Phi _ { i } ^ { - 1 } ( x _ { i } ) ) \right \| _ { \mathbb { R } ^ { d _ { 2 } - d _ { 1 } , \infty } } < r \right ) .$$

<!-- p:49 -->


By applying this to (C.11), Q1 II B1d2,0 n (xi, r)) can be lower bounded as i=1

$$By applying this to ( C . 1 1 ) , Q _ { 1 } & \left ( \prod _ { i = 1 } ^ { n } B _ { \| _ { \mathbb { R } ^ { 2 } , \infty } } ( x _ { i } , r ) \right ) \, \text { can be lower bounded as} \\ Q _ { 1 } & \left ( \prod _ { i = 1 } ^ { n } B _ { \| _ { \mathbb { R } ^ { 2 } , \infty } } ( x _ { i } , r ) \right ) \\ & \geq \int \prod _ { C ^ { n } } ^ { n } \frac { r ^ { d _ { 1 } } - 1 } { 2 K _ { i } ^ { d _ { 1 } - 1 } a n } I \left ( \| y _ { i } - \Pi _ { ( d _ { 1 } + 1 ) ; d _ { 2 } } ( \Phi _ { i } ^ { - 1 } ( x _ { i } ) ) \| _ { \mathbb { R } ^ { d _ { 2 } - d _ { 1 } } , \infty } < r \right ) \lambda _ { C ^ { n } } ( y ) \\ & = \frac { r ^ { d _ { n } } } { 2 ^ { n } K _ { I } ^ { ( d _ { 1 } - 1 ) ^ { n } } ( a n ) ^ { n } } \prod _ { C } ^ { n } I \left ( \| y _ { i } - \Pi _ { ( d _ { 1 } + 1 ) ; d _ { 2 } } ( \Phi _ { i } ^ { - 1 } ( x _ { i } ) ) \| _ { \mathbb { R } ^ { d _ { 2 } - d _ { 1 } } , \infty } < r \right ) \lambda _ { C } ( y _ { i } ) \\ & = \frac { r ^ { d _ { n } } } { 2 ^ { n } K _ { I } ^ { ( d _ { 1 } - 1 ) ^ { n } } ( a n ) ^ { n } } \left ( \frac { ( 2 r ) ^ { d _ { 2 } - d _ { 1 } } } { w ^ { d _ { 2 } - d _ { 1 } } \omega _ { d _ { 2 } - d _ { 1 } } } \right ) ^ { n } \\ & = \frac { ( 2 d _ { 2 } - d _ { 1 } - 1 ) n } { K _ { I } ^ { ( d _ { 1 } - 1 ) n } w ^ { ( d _ { 2 } - d _ { 1 } ) n } ( a n ) ^ { n } \omega _ { d _ { 2 } - d _ { 1 } } ^ { n } } \\ & \geq \frac { 2 ^ { ( d _ { 2 } - d _ { 1 } - 1 ) n } r ^ { d _ { 2 } n } } { K _ { I } ^ { d _ { 2 } n } \omega _ { d _ { 2 } - d _ { 1 } } ^ { n } } , \\ \intertext { where the last ineqequality uses an } & \intertext { where the last ineqequality uses an } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext { a n } & \intertext {$$

where the last inequality uses an ≤ cd2-d1 K1 ≤ Kd2−d1+1 and w ≤ τl. d2−d1 τe

On the other hand, Q2 I B1-Rd2, n (xi, r) 2r d2n rd2n 2KI i=1 (C.12), we get (C.10) as

$$Q _ { 1 } \left ( \prod _ { i = 1 } ^ { n } B _ { \| \cdot \| _ { \mathbb { R } ^ { d _ { 2 } , \infty } } ( x _ { i } , r ) } \right ) & \geq \frac { 2 ^ { ( d _ { 2 } - d _ { 1 } - 1 ) n } } { \omega _ { d _ { 2 } - d _ { 1 } } ^ { n } } Q _ { 2 } \left ( \prod _ { i = 1 } ^ { n } B _ { \| \cdot \| _ { \mathbb { R } ^ { d _ { 2 } , \infty } } ( x _ { i } , r ) } \right ) \\ & \geq 2 ^ { - n } Q _ { 2 } \left ( \prod _ { i = 1 } ^ { n } B _ { \| \cdot \| _ { \mathbb { R } ^ { d _ { 2 } , \infty } } ( x _ { i } , r ) } \right ) .$$

Proposition 14. Fix τg, τe ∈ (0, ∞], KI ∈ [1, ∞), Kv ∈ (0, 2−m], Kp ∈ [(2KI)m, ∞), d1, d2 ∈ N, with τg ≤ τl and 1 ≤ d1 &lt; d2 ≤ m, and suppose that τl &lt; K1. Then

$$& \inf _ { \widehat { d } _ { n } } \sup _ { P \in \mathcal { Q } } \mathbb { E } _ { P ^ { ( n ) } } [ \ell ( \widehat { d } _ { n } , d ( P ) ) ] \\ & \quad \geq \left ( C _ { d _ { 1 } , d _ { 2 } , k _ { I } } ^ { ( 1 4 ) } \right ) ^ { n } \min \left \{ \tau _ { \ell } ^ { - 2 ( d _ { 2 } - d _ { 1 } + 1 ) } n ^ { - 2 } , 1 \right \} ^ { ( d _ { 2 } - d _ { 1 } ) n } ,$$

<!-- p:50 -->


where C(14) ∈ (0, ∞) is a constant depending only on d1, d2, and KI and d1,d2,K1

$$\mathcal { Q } = \mathcal { P } _ { \tau _ { \ell } , \tau _ { \ell } } ^ { d _ { 1 } }$$

Proof of Proposition 14. Let J = [−K1, K1]d2. Let Sn be the permutation group, and Sn Q Jn by coordinate change, i.e. σ ∈ Sn, x ∈ Jn, σx := (xσ(1), . . , xσ(n)). For any set A ⊂ Jn, let SnA := {σx ∈ Jn : σ ∈ Sn, x ∈ A}.

n n Let Ti be Ti's from Lemma 12. Let T := Sn ΠTi, and V := U Ti = II1:d2(T). i=1 i=1 Intuitively, T is the set of points x = (x1, . . . , xn) where xi lies on one of the Tj.

Let C = BRd2-d1 (0, w) where w is from Lemma 12, and precisely define a set of d1-dimensional distribution P1 in (4.2) and a set of d2-dimensional distribution P2 in (4.3) as

P1 = {P ∈ Pd1 Tg,Te,K1,Kv,Kp : : there exists M ∈ M (Cn) such that P is uniform on M},

$$\mathcal { P } _ { 2 } = \{ \lambda _ { J } \} \subset \mathcal { P } _ { \tau _ { g } , \tau _ { \ell } , K _ { I } , K _ { v } , K _ { p } } .$$

Define a map Φ : Cn → P1 by Φ(y1, . . . , yn) = λM (y1,.,n) , .e. the uniform measure on M(y1, . . . , yn). Impose a topology and probability measure structure on P1 by the pushforward topology and the uniform measure on Cn, i.e. P′ ⊂ P1 is open if and only if Φ−1(P′) is open in Cn, P′ ⊂ P1 is measurable if and only if Φ−1(P′) ∈ B(Cn), and μ1(P′) = λCn(Φ−1(P′)).

Define a probability measure Q1, Q2 on (Jn, B(Jn)) by

$$Q _ { 1 } ( A ) \coloneqq \int _ { \mathcal { P } _ { 1 } } P ^ { ( n ) } ( A ) d \mu _ { 1 } ( P ) \quad \text { and } \quad Q _ { 2 } = \lambda _ { J ^ { n } } .$$

Fix P ∈ P1, let x = Φ−1(P). Then P(n)(A) = λ(n)( )(A) is a measurable function of x and M (x) Φ is a homeomorphism. Hence, p(n)(A) is measurable function and Q1(A) is well defined. Define ν = Q1 + λJ. Then Q1, Q2  ν, so there exist densities q1 = dQ1 = zb dQ2 with dν, dν respect to ν.

Then by applying Le Cam's Lemma (Lemma 10) with θ(P) = d(P), P1 and P2 from (C.14), and Q1 and Q2 in (C.15), the minimax rate inf sup EP l(λn, d(P)) can dn P∈P1∪P2 be lower bounded as

$$\text {be lower bounded as} \\ \inf _ { \widehat { d } _ { n } } \sup _ { P \in \mathcal { P } _ { 1 } \cup \mathcal { P } _ { 2 } } \mathbb { E } _ { P } \left [ \ell ( \widehat { d } _ { n } , d ( P ) ) \right ] & \geq \frac { \ell ( d _ { 1 } , d _ { 2 } ) } { 2 } \int _ { J ^ { n } } q _ { 1 } ( x ) \wedge q _ { 2 } ( x ) d \nu ( x ) \\ & = \frac { 1 } { 2 } \int _ { J ^ { n } } q _ { 1 } ( x ) \wedge q _ { 2 } ( x ) d \nu ( x ) .$$

<!-- p:51 -->


Then from Claim 13, for all x ∈ intT, there exists rx &gt; 0 s.t. for all r &lt; rx,

$$Q _ { 1 } \left ( \prod _ { i = 1 } ^ { n } B _ { \| \cdot \| _ { R ^ { d _ { 2 } } , \infty } } ( x _ { i } , r ) \right ) \geq 2 ^ { - n } Q _ { 2 } \left ( \prod _ { i = 1 } ^ { n } B _ { \| \cdot \| _ { R ^ { d _ { 2 } } , \infty } } ( x _ { i } , r ) \right ) .$$

Hence q1(x) is lower bounded by q2(x) whenever x ∈ intT as

$$q _ { 1 } ( x ) \geq 2 ^ { - n } q _ { 2 } ( x ) \text { if } x \in i n t { T } ,$$

and q1(x) ∧ q2(x) is correspondingly lower bounded by q2(x) as

$$q _ { 1 } ( x ) \wedge q _ { 2 } ( x ) \geq 2 ^ { - n } q _ { 2 } ( x ) 1 ( x \in i n t T ) .$$

Hence the integration of q1(x) ∧ q2(x) over T is lower bounded as

$$\frac { 1 } { 2 } \int _ { T } q _ { 1 } ( x ) \wedge q _ { 2 } ( x ) d \nu ( x ) \geq 2 ^ { - n - 1 } \lambda _ { J ^ { n } } ( T ) .$$

Then from a = (d2−d1+1) KI-τe Ip−p n and w = min Tl, 2τe(d2−d1+1)2([ (d2−d1)2(KI−τe)2 cd2−d1 n ]+1) 2 λJn(T) can be lower bounded as

$$c a n \, b e l o w \, b o u n d e d \, a s & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & &$$

C(14,1) for some constant that depends only on d1, d2, and K1. Hence by combining d1,d2,KI (C.16), (C.17), and (C.18), the minimax rate iņf sup Ep [e(∂n, d(P))] can be lower λn P∈P1UP2 bounded as

$$\inf _ { \substack { \widehat { d } _ { n } , P \in \mathcal { P } _ { 1 } \cup \mathcal { P } _ { 2 } } } \sup _ { \mathbb { E } _ { P } } \mathbb { E } _ { P } \left [ \ell ( \widehat { d } _ { n } , d ( P ) ) \right ] \geq \left ( C _ { d _ { 1 } , d _ { 2 } , K _ { I } } ^ { ( 1 4 ) } \right ) ^ { n } \min \left \{ \tau _ { \ell } ^ { - 2 ( d _ { 2 } - d _ { 1 } + 1 ) } n ^ { - 2 } , 1 \right \} ^ { ( d _ { 2 } - d _ { 1 } ) n } ,$$

for some constant (14) that depends only on d1, d2, and K1. Then since P1 ⊂ d1,d2,KI Pd1 and P2 ⊂ Pd2 P9,τe,K1,Kv2Kp, the minimax rate Rn in (2.6) can be lower bounded τg,Te,K1,Kv,Kp by the minimax rate inf sup Ep [l(λn, d(P))], i.e. dn P∈P1UP2

$$\inf _ { \widehat { d } _ { n } } \sup _ { P \in \mathcal { P } _ { \tau _ { g } , \tau _ { \ell } , K _ { I } , K _ { v } , K _ { p } } \cup \mathcal { P } _ { \tau _ { g } , \tau _ { \ell } , K _ { I } , K _ { v } , K _ { p } } } \mathbb { E } _ { P } [ \ell ( \widehat { d } _ { n } , d ( P ) ) ] \geq \inf _ { \widehat { d } _ { n } } \sup _ { P \in \mathcal { P } _ { 1 } \cup \mathcal { P } _ { 2 } } \mathbb { E } _ { P } [ \ell ( \widehat { d } _ { n } , d ( P ) ) ] ,$$

which completes the proof of showing (C.13).

<!-- p:52 -->


## D Proofs For Section 5

Proposition 15. Fix τg, τl ∈ (0, ∞], K1 ∈ [1, ∞), Kv ∈ (0, 2−m], Kp ∈ [(2K1)m, ∞), with τg ≤ τe. Let dn be in (5.1). Then:

$$& \sup _ { P \in \mathcal { P } _ { \gamma , \tau _ { l } , K _ { 1 } , K _ { v } , K _ { p } } } \mathbb { E } _ { P ^ { ( n ) } } \left [ \ell \left ( \widehat { d } _ { n } , d ( P ) \right ) \right ] \\ & \leq 1 ( d > 1 ) \left ( C _ { K _ { 1 } , K _ { p } , K _ { v } , m } ^ { ( 1 5 ) } \right ) ^ { n } \max \left \{ 1 , \tau _ { g } ^ { - ( d m + m - 2 d ) n } \right \} n ^ { - \frac { 1 } { d - 1 } n } ,$$

where K1,Kp,Kv,m ∈ (0, ∞) is a constant depending only on K1, Kp, Kv, and m. γ(15)

Proof of Proposition 15. Note that for all P ∈ Pd and X1, . . . , Xn ∼ P, by Tg,Te,K1,Kv,Kp Lemma 7,

$$\min _ { \sigma \in S _ { n } } \left \{ \sum _ { i = 1 } ^ { n - 1 } \| X _ { \sigma ( i + 1 ) } - X _ { \sigma ( i ) } \| _ { \mathbb { R } ^ { m } } ^ { d } \right \} \leq C _ { K _ { I } , K _ { v } , m } ^ { ( 7 ) } \max \left \{ 1 , \tau _ { g } ^ { d - m } \right \} ,$$

hence dn in (5.1) always satisfies

$$\widehat { d } _ { n } ( X ) \leq d = d ( P ) .$$

Hence when d = 1, the risk of n is 0. When d &gt; 1, from (D.2) and Proposition 9, the risk of dn in (5.1) is upper bounded as

$$H e nce when d = 1 , the risk of d , n , is 0 . \text { When } d > 1 , \text { from } ( D . 2 ) \text { and } \text { Proposition } 9 , \text { the risk} \\ \text { of } \widehat { d } _ { n } \text { in } ( 5 . 1 ) \text { is upper bounded as} \\ P ^ { ( n ) } \left [ \widehat { d } _ { n } ( X _ { 1 } , \cdots , X _ { n } ) \neq d \right ] \\ = P ^ { ( n ) } \left [ \max \left \{ k \in [ 1 , m ] \colon \min \left \{ \sum _ { i = 1 } ^ { n - 1 } \| X _ { \sigma ( i + 1 ) } - X _ { \sigma ( i ) } \| _ { \mathbb { R } ^ { m } } ^ { k } \right \} \leq C _ { K _ { 1 } , K _ { \nu } , m } ^ { ( 7 ) } \max \left \{ 1 , \tau _ { g } ^ { k - m } \right \} \right \} \\ < d \right ] ( \text {from } ( D . 2 ) ) \\ \leq \sum _ { k = 1 } ^ { d - 1 } P ^ { ( n ) } \left [ \min \left \{ \sum _ { i = 1 } ^ { n - 1 } \| X _ { \sigma ( i + 1 ) } - X _ { \sigma ( i ) } \| _ { \mathbb { R } ^ { m } } ^ { k } \right \} \leq C _ { K _ { 1 } , K _ { \nu } , m } ^ { ( 7 ) } \max \left \{ 1 , \tau _ { g } ^ { k - m } \right \} \right ] \\ \leq \sum _ { k = 1 } ^ { d - 1 } \left ( C _ { K _ { 1 } , K _ { \nu } , k _ { m } } ^ { ( 8 ) } \right ) ^ { n } \max \left \{ 1 , \tau _ { g } ^ { - \frac { ( \frac { d } { k } + m - 2 d ) n } { k } } \right \} n ^ { - \frac { ( \frac { d } { k } - 1 ) n } { ( \frac { d } { k } - 1 ) ^ { n } } } \left ( \text {Proposition} \right ) \\ \leq \left ( C _ { K _ { 1 } , K _ { \nu } , k _ { m } } ^ { ( 1 5 ) } \right ) ^ { n } \max \left \{ 1 , \tau _ { g } ^ { - ( d m + m - 2 d ) n } \right \} n ^ { - \frac { 1 } { d } n } ,$$

<!-- p:53 -->


where γ(15) K1,Kp,Kv,m = mC γ(8) K1,Kp,Kv,m is a constant depending only on K1, Kp, Kv, and m. Therefore, the risk is upper bounded as in (D.1), as

$$& \sup _ { P \in \mathcal { P } ^ { d } _ { \tau _ { g } , K _ { l } , K _ { v } , K _ { p } } } \mathbb { E } _ { P ^ { ( n ) } } \left [ \ell \left ( \widehat { d } _ { n } , d ( P ) \right ) \right ] \\ & \leq 1 ( d > 1 ) \left ( C _ { K _ { l } , K _ { p } , K _ { v } , m } ^ { ( 1 5 ) } \right ) ^ { n } \max \left \{ 1 , \tau _ { g } ^ { - ( d m + m - 2 d ) n } \right \} n ^ { - \frac { 1 } { d - 1 } n } .$$

Proposition 16. Fix τg, τe ∈ (0, ∞], KI ∈ [1, ∞), Kv ∈ (0, 2−m], Kp ∈ [(2KI)m, ∞), with τg ≤ τl. Then:

$$\inf _ { \widehat { d } _ { n } } \sup _ { P \in \mathcal { P } } \mathbb { E } _ { P ^ { ( n ) } } \left [ \ell \left ( \widehat { d } _ { n } , d ( P ) \right ) \right ] \leq \left ( C _ { K _ { 1 } , K _ { p } , K _ { v } , m } ^ { ( 1 5 ) } \right ) ^ { n } \max \left \{ 1 , \tau _ { g } ^ { - ( m ^ { 2 } - m ) n } \right \} n ^ { - \frac { 1 } { m - 1 } n } , \quad ( D . 3 )$$

(15) where K1,Kp,Kv,m is from Proposition 15.

Proof of Proposition 16. Note that (3.2) still holds when P is as in (2.8). Hence applying Proposition 15 to (3.2) yields

$$\inf \sup & \mathbb { E } _ { P ( n ) } \left [ \ell \left ( \widehat { d } _ { n } , d ( P ) \right ) \right ] \\ & \leq \max _ { 1 \leq d \leq n } \left \{ \sup _ { P \in \mathcal { P } _ { \tau _ { g } , \tau _ { \ell } , K _ { I } , K _ { v } , K _ { p } } } \mathbb { E } _ { P ^ { ( n ) } } \left [ \ell \left ( \widehat { d } _ { n } , d ( P ) \right ) \right ] \right \} \\ & \leq \left ( C _ { K _ { I } , K _ { p } , K _ { v } , m } ^ { ( 1 5 ) } \right ) ^ { n } \max \left \{ 1 , \tau _ { g } ^ { - ( m ^ { 2 } - m ) n } \right \} n ^ { - \frac { 1 } { m - 1 } } .$$

Hence the minimax rate Rn in (2.6) is upper bounded as in (D.3).

Proposition 17. Fix τg, τe ∈ (0, ∞], KI ∈ [1, ∞), Kv ∈ (0, 2−m], Kp ∈ [(2K1)m, ∞), with τg ≤ τl and suppose that τl &lt; K1. Then,

$$\inf _ { \substack { \widehat { d } _ { n } , \, P \in \mathcal { P } } } \mathbb { E } _ { P ^ { ( n ) } } \left [ \ell ( \widehat { d } _ { n } , d ( P ) ) \right ] \geq \left ( C _ { K _ { 1 } } ^ { ( 1 7 ) } \right ) ^ { n } \min \left \{ \tau _ { \ell } ^ { - 4 } n ^ { - 2 } , 1 \right \} ^ { n }$$

where (17) ∈ (0, ∞) is a constant depending only on K1. KI

<!-- p:54 -->


Proof of Proposition 17. For any d1 and d2, from Proposition 14,

$$\inf _ { \widehat { d } _ { n } } & \sup _ { P \in \mathcal { P } } \mathbb { E } _ { P ( n ) } [ \ell ( \widehat { d } _ { n } , d ( P ) ) ] \\ & \geq \inf _ { \widehat { d } _ { n } } \quad \sup \quad \mathbb { E } _ { P ^ { ( n ) } } [ \ell ( \widehat { d } _ { n } , d ( P ) ) ] \\ & \geq \left ( C _ { d _ { 1 } , d _ { 2 } , K _ { I } } ^ { ( 1 4 ) } \right ) ^ { n } \min \left \{ \tau _ { \ell } ^ { - 2 ( d _ { 2 } - d _ { 1 } + 1 ) } n ^ { - 2 } , 1 \right \} ^ { ( d _ { 2 } - d _ { 1 } ) n }$$

Hence by plugging in d1 = 1 and d2 = 2, the minimax rate Rn in (2.6) is lower bounded as in (D.3), as

$$\text { in } ( D . 3 ) , \text { as } & & \inf _ { \widehat { d } _ { n } } \sup _ { P \in \mathcal { P } } \mathbb { E } _ { P ^ { ( n ) } } [ \ell ( \widehat { d } _ { n } , d ( P ) ) ] \geq \left ( C _ { K _ { I } } ^ { ( 1 7 ) } \right ) ^ { n } \min \left \{ \tau _ { \ell } ^ { - 4 } n ^ { - 2 } , 1 \right \} ^ { n } \\ \text { with } C _ { K _ { I } } ^ { ( 1 7 ) } = C _ { d _ { 1 } = 1 , d _ { 2 } = 2 , K _ { I } } ^ { ( 1 4 ) } \cdot &$$
