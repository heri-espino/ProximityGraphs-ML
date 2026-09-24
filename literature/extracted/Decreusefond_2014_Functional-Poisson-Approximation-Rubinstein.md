---
id: "Decreusefond_2014_Functional-Poisson-Approximation-Rubinstein"
source_pdf: "../pdf/Decreusefond_2014_Functional-Poisson-Approximation-Rubinstein.pdf"
source_filename: "Decreusefond_2014_Functional-Poisson-Approximation-Rubinstein.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "full-page-ocr"
extraction_quality: "excellent"
extraction_score: 100.0
visual_assets: "disabled"
references_file: "../references/Decreusefond_2014_Functional-Poisson-Approximation-Rubinstein.references.md"
---

<!-- p:1 -->

HAL

open science

### Functional Poisson approximation in Rubinstein distance

Laurent Decreusefond, Matthias Schülte, Christoph Thäle

####### V To cite this version:

Laurent Decreusefond, Matthias Schülte, Christoph Thäle. Functional Poisson approximation in Rubinstein distance. 2014. &lt;hal-01010967v1&gt;

##### HAL Id: hal-01010967 https://hal.science/hal-01010967v1

Preprint submitted on 21 Jun 2014 (v1), last revised 24 Feb 2015 (v2)

HAL is a multi-disciplinary open access archive L'archive ouverte pluridisciplinaire HAL, est desfor the deposit and dissemination of scientific re- tinée au dépôt et à la diffusion de documents sciensearch documents, whether they are published or not. tifiques de niveau recherche, publiés ou non, émanant The documents may come from teaching and research des établissements d'enseignement et de recherche institutions in France or abroad, or from public or pri- français ou étrangers, des laboratoires publics ou vate research centers. privés.

Autorisation

HAL


<!-- p:2 -->


## Functional Poisson approximation in Rubinstein distance

##### Laurent Decreusefond, Matthias Schulte†and Christoph Thäle‡

####### Abstract

A Poisson or a binomial process on an abstract state space and a symmetric function f acting on k-tuples of its points are considered. They induce a point process on the target space of f. The main result is a functional limit theorem which provides an upper bound for an optimal transportation distance between the image process and a Poisson process on the target space. The technical background are a version of Stein's method for Poisson process approximation, a Glauber dynamic representation for the Poisson process and the Malliavin formalism. As applications of the main result, error bounds for approximations of U-statistics by Poisson, compound Poisson and stable random variables are derived and examples from stochastic geometry are investigated.

Keywords. Binomial process, configuration space, functional limit theorem, Glauber dynamic, Malliavin formalism, Poisson process, Rubinstein distance, Stein's method, stochastic geometry, U-statistics. MSC2010. Primary 60F17, 60G55; Secondary 60D05, 60E07, 60H07.

## 1 Introduction

The arguably most prominent functional limit theorem is Donsker's invariance principle. It asserts that the distribution of a linear interpolation between the points of a suitably re-scaled random walk converges to the Wiener measure on the space of continuous functions on R+, the non-negative real half-line (see e.g. [24, Corollary 16.7]). Besides the Wiener process, there is another fundamental stochastic process, which plays an important rôle in many branches of probability theory and its applications, namely the Poisson process. However, functional limit theorems involving the Poisson process have found much less attention in the literature. The aim of this paper is to provide a quantitative version of a functional limit theorem for Poisson processes and to derive from it error bounds for the probabilistic approximation of U-statistics by a Poisson, a compound Poisson or a stable random variable. We demonstrate the versatility of our results by applying these bounds to functionals of random geometric graphs, distance-power statistics, non-intersecting flat processes and random polytopes.

Let us informally describe the set-up of this paper, precise definitions and statements follow in Section 3. Let (X, X) and (Y, ) be two measurable spaces (satisfying some mild regularity assumptions, see below), let K1 be a probability measure on X and fix an integer k ≥ 1. Moreover, for each n ∈ N let fn : dom fn → Y be a symmetric mapping whose domain dom fn is a symmetric subset of Xk. Next, consider a collection βn = {X1, . . . , Xn} of n ≥ k i.i.d. random elements X1, . . . , Xn of X with distribution K1. We apply for each n ≥ k, fn to every k-tuple of distinct elements of βn. This induces a point process ξn on Y of the form

= us

1

∑

δfn(x,..,,x),

k!

uf ≠ y3(x.x))

*Telecom ParisTech, Rue Barrault 46, F-75634 Paris cedex 13, France. E-mail: laurent.decreusefond@telecom-

paristech.fr measure concentrated on y ∈ Y. The intensity measure Ln of ξn is given by

†Karlsruhe Institute of Technology, Department of Mathematics, Institute of Stochastics, D-76128 Karlsruhe, Germany. E-mail: matthias.schulte@kit.edu

‡Ruhr University Bochum, Faculty of Mathematics, NA 3/68, D-44780 Bochum, Germany. E-mail: christoph.thaele@rub.de


<!-- p:3 -->


$$L _ { n } ( A ) = E \xi _ { n } ( A ) = \frac { ( n ) _ { k } } { k ! } \int _ { \text {dom} \ f _ { n } } 1 ( f _ { n } ( x _ { 1 } , \dots , x _ { k } ) \in A ) \, K _ { 1 } ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \, , \quad A \in \mathcal { Y } \, ,$$

where (n)k is the descending factorial. Our main result, Theorem 3.1 below, provides an upper bound for the Rubinstein distance dR(ξn, ζ) between ξn and a Poisson process ζ on Y with finite intensity measure M. Here, the Rubinstein distance is a variant of an optimal transportation distance, which measures the closeness between two point processes or, more precisely, their distributions. In particular, we show that ξn converges in Rubinstein distance and, thus, in distribution to ζ if

$$d _ { T V } ( L _ { n } , M ) \rightarrow 0 \quad \text {and} \quad \mathbf E _ { n } ( \mathbb { Y } ) ^ { 2 } \rightarrow M ( \mathbb { Y } ) ^ { 2 } + M ( \mathbb { Y } ) \, , \quad \text {as} \quad n \rightarrow \infty \, ,$$

where dTv(·, ·) denotes the total variation distance of measures on Y. More precisely, the upper bound for the Rubinstein distance only depends on dTv(Ln, M) and the first two moments of ξn(Y). This is a functional version of the famous results by Arratia, Chen, Goldstein and Gordon [1, 14] that "two moments suffice for Poisson approximation".

Besides of the binomial process βn of n independent and identically distributed points, we also allow the input process to be a Poisson process on X with a σ-finite intensity measure. In some instances, an underlying Poisson process is more natural and sometimes even unavoidable, especially if the underlying point process on X is supposed to have infinitely many points. To exploit this flexibility, we consider both set-ups in parallel.

Poisson process approximation has been studied by several authors by means of Stein's method, but to the best of our knowledge this is the first paper, where the Rubinstein distance is investigated. The works of Barbour [2], Barbour and Brown [4] and the last chapter of the monograph [8] of Barbour, Holst and Janson concern Poisson process approximation in the total variation distance. But since the total variation distance is not suitable for all problems and since the so-called ,Stein magic factors" do not get small if Ln(Y) is large (in contrast to classical Poisson approximation), one often uses weaker notions of distance. Starting with the work of Barbour and Brown [4] and Barbour, Holst and Janson [8], this has been done by Brown, Chen, Schuhmacher, Weinberg and Xia [11, 12, 13, 15, 38, 39, 40]. Our work goes in the opposite direction since the Rubinstein distance between point processes is stronger than the total variation distance in the sense that convergence in Rubinstein distance implies convergence in total variation distance, but not vice versa. Roughly speaking and in a transferred sense, the Rubinstein distance is related to the total variation distances between point processes as the Wasserstein distance is related to the total variation distance for integer-valued random variables. Since its test functions are allowed to take values different from zero and one, the Rubinstein distance is more sensitive to the behaviour and the geometry of the compared point processes than the total variation distance.

Besides the notion of distance and its connection to the theory of optimal transportation, the other main ingredient of our approach is a functional version of Stein's method for Poisson process approximation. It relies on a Glauber dynamic representation for Poisson processes and the Malliavin formalism. More precisely, we use an integration-by-parts argument on the target space and then a commutation relation between the discrete gradient on that space and the semi-group associated with the Glauber dynamic. This way we avoid the explicit computation and investigation of a solution of the Stein equation. We would like to highlight that our approach is generic and depends only on the underlying random structure (here, a binomial or a Poisson process) and not on a very specific model so that extensions to other probabilistic frameworks (such as Gaussian random measures or Rademacher sequences) should also be possible. However, they are beyond the scope of this paper and will be treated elsewhere.

To demonstrate the versatility of our new functional limit theorem, we consider probabilistic approximations of U-statistics over binomial or Poisson input processes. In a first regime, we consider the Poisson approximation of U-statistics and provide an error bound for the Wasserstein distance. Our result improves and extends earlier works of Barbour and Eagleson [7], and Peccati [31]. The second regime concerns compound Poisson approximation of U-statistics in total variation distance. Here, we do not impose any conditions on the nature of the compound Poisson distribution, which is allowed to be discrete or continuous. In contrast, previous results for the compound Poisson approximation via Stein's method only deal with the discrete case, see, for example, the work of Barbour, Chen and Loh [5], the survey [6] of Barbour and Chryssaphinou and especially the paper [21] of Eichelsbacher and Roos, who consider U-statistics over a binomial input process. In this light, we generalize the results of [21] to a larger class of limiting distributions and also to the case of an underlying Poisson process. In a third regime, we use our functional limit theorem to investigate probabilistic approximations of U-statistics by α-stable random variables with 0 &lt; α &lt; 1 and to derive explicit error bounds for the Kolmogorov distance. In the previous work [17], Dabrowski, Dehling, Mikosch and Sharipov also obtained α-stable limits for U-statistics from point process convergence results. However, their technique does not allow any conclusion about a rate of convergence.


<!-- p:4 -->


Finally, we apply our general result to problems arising in stochastic geometry. Random geometric graphs are one of the fundamental models of spatial stochastics, see [33], for example. We derive limit theorems for several U-statistics of random geometric graphs, where the limiting distributions are Poisson or compound Poisson, and show a new point process limit theorem for the midpoints of short edges. As further examples, we consider distance-power statistics with α-stable limit distributions, midpoints between non-intersecting Poisson m-flats which are close together and the diameter of random polytopes with vertices on the sphere.

In a natural way our paper continues the line of research on point process convergence initiated by the second and the third author in [41, 42], where the proofs are based on the main result of [31] and the underlying point process has to be Poisson. In contrast to these previous works our technique also allows to deal with an underlying binomial process and delivers in both cases bounds for the Rubinstein distance. Furthermore, the bounds derived here also improve the rates of convergence of some of the scalar limit theorems from [41, 42]. Our findings also complement the works [19] and [20] of the first author with Joulin and Savy concerning the Rubinstein distance on configuration spaces and related notions.

This paper is organised as follows. Before we present our main result for Poisson process convergence in Section 3, we recall in Section 2 some necessary notation and results about point processes and also summarize some facts from convex geometry which are important for our examples from stochastic geometry. The proof of our main result in Section 6 is prepared by a brief discussion of the underlying Stein principle in Section 4 and the Glauber dynamic, a key step in our argument, in Section 5. Section 7 is devoted to applications of our functional limit theorem to probabilistic approximations of U-statistics and to problems from stochastic geometry.

## 2 Preliminaries

In the present section we introduce some basic notions and notation, which are used in the text. Throughout (Ω, F, P) will be an abstract probability space, which is rich enough to carry all the ts  w d c ct e e   n

2.1 Configuration spaces. Let (Y, Y) be a lcscH space, that is, Y is a topological space with countable base such that every point in Y has a compact neighbourhood and such that any two points of Y can be separated by disjoint neighbourhoods. Such a space is separable and completely metrizable. Here,  denotes the Borel σ-field with respect to the topology of Y. By Ny we denote the space of σ-finite counting measures (i.e., point configurations) on Y, whereas NY stands for the set of all finite counting measures on Y. By a slight abuse of notation we will write y ∈ ω if y ∈ Y is charged by the measure ω and also use the set-notation ω1 ⊂ ω2 to indicate that ω1 is a sub-configuration of ω2 (with a similar meaning we also understand ω2 \ω1). Let Ny be the σ-field on Ny generated by the mappings

$$\psi _ { A } \colon N _ { Y } \to \mathbb { N } _ { 0 } \cup \{ \infty \} \, , \, \omega \mapsto \omega ( A ) \, , \quad A \in \mathcal { Y } \, ,$$

where N0 := N ∪ {0} is the set of natural numbers including zero. We notice that Ny is the Borel


<!-- p:5 -->


σ-field for the vague topology on Ny, which is generated by the mappings

$$e _ { g } \colon N _ { \mathbb { Y } } \rightarrow [ 0 , \infty ) , \, \omega \mapsto \int g \, d \omega \, ,$$

where g ≥ 0 is a continuous function on Y with compact support, see Theorem A2.3 in [24]. We supply Ny with the corresponding trace σ-field. A point process (or random counting measure) μ is a random element in Ny. It follows from [37, Lemma 3.1.3] that a point process μ can almost surely be represented as

$$\mu = \sum _ { i = 1 } ^ { \mu ( \mathbb { Y } ) } \delta _ { x _ { i } } \text { \ with \ } x _ { i } \in \mathbb { Y } , \ \ 1 \leq i \leq \mu ( \mathbb { Y } ) \in \mathbb { N } _ { 0 } \cup \{ + \infty \} ,$$

where δy stands for the unit mass Dirac measure concentrated at y ∈ Y. Thus, we may interpret μ also as a random collection of points, taking into account potential multiplicities.

2.2 Poisson processes. Let M be a σ-finite measure on Y and let Mk stand for its k-fold product measure. By a Poisson process on Y with intensity measure M, we understand a point process ζ with the properties that i) for any B ∈  the random variable ζ(B) is Poisson distributed with mean M(B) and that ii) ζ is independently scattered, i.e., for any n ∈ N and disjoint B1, . . . , Bn ∈ y the random variables ζ(B1), ... , ζ(Bn) are independent. We notice that if M is a finite measure, ζ charges almost surely only a finite number of points in Y, whose total number follows a Poisson distribution with mean M(Y). We will write Pζ for the distribution of ζ on Ny. In this paper we will speak about a homogeneous Poisson process on a set A ∈ B(Rd), where B(Rd) is the Borel σ-field on Rd, if the intensity measure is a multiple of the restriction of the Lebesgue measure to A. Also, if d = 1, a homogeneous Poisson process ζ on [0, ∞) can be thought of as a piecewise deterministic (pure jump) stochastic process in continuous time, starting at zero and having jumps of size one and i.i.d. exponentially distributed waiting times between the jumps. The points of discontinuity of this random process are the jump times of ζ.

One of our main tools to deal with Poisson functionals (by this we mean real-valued random variables depending only on a Poisson process) is the multivariate Mecke formula [37, Corollary 3.2.3]. It says that for any integer k ≥ 1 and any measurable and non-negative f : Yk × NY → R,

$$( 2 . 1 ) \quad \text {E} \sum _ { ( y _ { 1 } , \dots , y _ { k } ) \in \zeta ^ { k } _ { \neq } } f ( y _ { 1 } , \dots , y _ { k } , \zeta ) = \int _ { \gamma ^ { k } } \text {E} f ( y _ { 1 } , \dots , y _ { k } , \zeta + \delta _ { y _ { 1 } } + \dots + \delta _ { y _ { k } } ) \, \text {M} ^ { k } \left ( \text {d} ( y _ { 1 } , \dots , y _ { k } ) \right ) ,$$

where ζk is the collection of all k-tuples of distinct points charged by ζ. If the point process ζ is simple (i.e., if ζ({y}) ∈ {0, 1} almost surely for any y ∈ Y), ζk can be written as

$$\zeta _ { \neq } ^ { k } = \{ ( y _ { 1 } , \dots , y _ { k } ) \in \mathbb { Y } ^ { k } \colon y _ { i } \neq y _ { j } \in \zeta \text { for } i \neq j , \ i , j = 1 , \dots , k \} \, ,$$

while in the non-simple case distinct points can have the same location. We remark that (2.1) with k = 1 is even a characterizing property of the Poisson process ζ, cf. Theorem 3.2.5 of [37].

2.3 Binomial processes. Let M1 be a probability measure on Y. A binomial process with intensity measure M := nM1, n ∈ N, is a collection of n random points, distributed independently according to the measure M1. This process also arises by conditioning a Poisson process with intensity measure M on having exactly n points. In this paper we shall denote the random counting measure induced by points charged by βn. Then, the counterpart to the multivariate Mecke formula (2.1) for a binomial process reads as follows:

$$\intertext { f o r s e s $ d x $ a n d $ E $ f o r s e s } E \sum _ { ( 2 . 2 ) } f ( x _ { 1 } , \dots , x _ { k } , \beta _ { n } ) & \\ & = ( n ) _ { k } \int _ { \mathbb { Y } ^ { k } } E f ( y _ { 1 } , \dots , y _ { k } , \beta _ { n - k } + \delta _ { y _ { 1 } } + \dots + \delta _ { y _ { k } } ) \, M _ { \lceil } ^ { k } ( d ( y _ { 1 } , \dots , y _ { k } ) ) \, ,$$


<!-- p:6 -->


where (n)k := n(n − 1) · · · (n − k + 1) is the descending factorial and f is a real-valued non-negative measurable function on Yk × Ny. This can easily be seen directly and is also a special case of the Georgii-Nguyen-Zessin formula, for which we refer to [18, Proposition 15.5.II].

2.4 Probability distances. In order to compare two real-valued random variables Y1 and Y2 (or more precisely their distributions) and to measure their closeness, we use several probability distances in this paper. The Kolmogorov distance of Y1 and Y2 is given by

$$d _ { K } ( Y _ { 1 } , Y _ { 2 } ) \colon = \sup _ { z \in \mathbb { R } } | P ( Y _ { 1 } \leq z ) - P ( Y _ { 2 } \leq z ) | \, ,$$

while the total variation distance is

$$d _ { T V } ( Y _ { 1 } , Y _ { 2 } ) \colon = \sup _ { A \in \mathcal { B } ( \mathbb { R } ) } | P ( Y _ { 1 } \in A ) - P ( Y _ { 2 } \in A ) | \, ,$$

where, recall, B(R) stands for the Borel σ-field on R. If Y1 and Y2 are integer-valued random variables, we can re-write their total variation distance as

$$d _ { T V } ( Y _ { 1 } , Y _ { 2 } ) = \frac { 1 } { 2 } \sum _ { k \in \mathbb { Z } } | \mathbf P ( Y _ { 1 } = k ) - \mathbf P ( Y _ { 2 } = k ) | \, .$$

Let us denote by Lip(1) the set of all functions h : R → R whose Lipschitz constant is at most one and define the Wasserstein distance of two real-valued random variables Y1 and Y2 by

$$d _ { W } ( Y _ { 1 } , Y _ { 2 } ) \coloneqq \sup _ { h \in L i p ( 1 ) } | E h ( Y _ { 1 } ) - E h ( Y _ { 2 } ) | \, .$$

All these probability distances have the property that they imply convergence in distribution, meaning that for a sequence (Yn)n∈N of random variables convergence in distribution to another random variable Y is implied by

$$\text {d} \mathbf I ( Y _ { n } , Y ) \to 0 \quad \text {as} \quad n \to \infty \, , \quad \text {for some } \mathbf I \in \{ K , \text {TV} , W \} \, .$$

Moreover, for integer-valued random variables Y1 and Y2 let us mention the general inequality

$$d _ { K } ( Y _ { 1 } , Y _ { 2 } ) \leq d _ { T V } ( Y _ { 1 } , Y _ { 2 } ) \leq d _ { W } ( Y _ { 1 } , Y _ { 2 } ) \, ,$$

which directly follows from the definitions of the involved probability distances and the fact that Yi and Y2 are concentrated on the integers. Note that (2.4) does not remain valid for general real-valued random variables.

2.5 Rubinstein distance. We define the total variation distance between two measures ν1 and ν2 onY by

$$d _ { T V } ( \nu _ { 1 } , \nu _ { 2 } ) \colon = \sup _ { \nu _ { 1 } ( A ) , \nu _ { 2 } ( A ) < \infty } | \nu _ { 1 } ( A ) - \nu _ { 2 } ( A ) | \, ,$$

a notion which should not be confused with the total variation distance between random variables introduced above. Note that dTv(ν1, ν2) can in principle take any value in [0, ∞].

We say that a map h : NY → R is 1-Lipschitz if

$$| h ( \omega _ { 1 } ) - h ( \omega _ { 2 } ) | \leq d _ { T V } ( \omega _ { 1 } , \omega _ { 2 } ) \quad \text {for all } \omega _ { 1 } , \omega _ { 2 } \in N _ { \mathbb { Y } } \, ,$$

and denote by L1 the set of all these maps which are measurable.

The Rubinstein distance (also called Rubinstein-Kantorovich distance, Monge-Kantorovich distance or Wasserstein distance) between two probability measures Q1 and Q2 on Ny is defined as the optimal transportation cost

$$d _ { R } ( Q _ { 1 } , Q _ { 2 } ) \coloneqq \inf _ { C \in \Sigma ( Q _ { 1 } , Q _ { 2 } ) } \int _ { N _ { Y } \times N _ { Y } } d _ { T V } ( \omega _ { 1 } , \omega _ { 2 } ) \, C ( d ( \omega _ { 1 } , \omega _ { 2 } ) )$$


<!-- p:7 -->


for the cost function dTv(· , ·), where Σ(Q1, Q2) denotes the set of probability measures on Ny × NY with first marginal Q1 and second marginal Q2 (i.e., couplings of Q1 and Q2). According to the last part of the Kantorovich duality stated in [44, Theorem 1.3] there is at least one coupling C ∈ Σ(Q1, Q2) for which the infimum in (2.5) is attained, and the Kantorovich-Rubinstein theorem [44, Theorem 1.14] says that this minimum equals

$$d _ { R } ( Q _ { 1 } , Q _ { 2 } ) = \sup \left | \int _ { N _ { Y } } h ( \omega ) \, Q _ { 1 } ( d \omega ) - \int _ { N _ { Y } } h ( \omega ) \, Q _ { 2 } ( d \omega ) \right | ,$$

where the supremum is over all h ∈ L1 that are integrable with respect to Q1 and Q2. Theorem 7.3 in [44] ensures that (2.5), or equivalently (2.6), defines a metric on the space of (Borel) probability measures on Ny and also on the subspace Ny.

By abuse of notation we will also write dR(ζn, ζ) instead of dR(Qn, Q) if the point process ζn on Y has distribution Qn for any n ≥ 1 and the point process ζ on Y has distribution Q. Note that the integrability condition in (2.6) is automatically fulfilled for all h ∈ L1 if Eζn(Y) &lt; ∞ and Eζ(Y) &lt; ∞.

The following result ensures that convergence of point processes in Rubinstein distance implies convergence in distribution.

Proposition 2.1. Assume that (ζn)n∈N is a sequence of point processes on Y and that ζ is another point process on Y such that dR(ζn, ζ) → 0, as n → ∞. Then ζn converges in distribution to ζ, as n →∞.

Proof. The structure of the vague topology on Ny implies that it is necessary and sufficient to prove that for any continuous g : Y → R with compact support, the random variables ∫ g dζn converge in distribution to ∫ g dζ, see [24, Theorem 16.16]. By (2.3), it is sufficient to show that for all Borel sets B ⊂ R, we have that

$$E e _ { g , B } ( \zeta _ { n } ) \rightarrow E e _ { g , B } ( \zeta ) \, , \quad \text {as} \quad n \rightarrow \infty \, ,$$

where eg,B : Ny → R, ω → 1(∫ g dω ∈ B). To show this, we notice that for each g and B as above the mapping eg,B belong to L1, whence

and the result follows.

$$| \mathbf E e _ { g , B } ( \zeta _ { n } ) - \mathbf E e _ { g , B } ( \zeta ) | & \leq \mathbf d _ { \mathbf R } ( \zeta _ { n } , \zeta ) \\ \Box$$

An alternative distance to measure the closeness of two point processes ζ1 and ζ2 on Y is the total variation distance

$$d _ { T V } ( \zeta _ { 1 } , \zeta _ { 2 } ) \colon = \sup _ { A \in \mathcal { N } _ { \mathbb { Y } } } | \mathbf P ( \zeta _ { 1 } \in A ) - \mathbf P ( \zeta _ { 2 } \in A ) | .$$

$$d _ { T V } ( \zeta _ { 1 } , \zeta _ { 2 } ) = \sup _ { A \in \mathcal { N } _ { Y } } | E 1 ( \zeta _ { 1 } \in A ) - E 1 ( \zeta _ { 2 } \in A ) |$$

and noting that the mapping ζ → 1(ζ ∈ A) from NY to R belongs to L1, we see that dTv(ζ1, ζ2) ≤ dR(ζ1, ζ2). The following example shows that convergence in Rubinstein distance is strictly finer than convergence in total variation distance.

Example 2.2. Let ζ be a Poisson process on Y with finite intensity measure M. Let (Xi)i∈N be a sequence of independent random elements in Y with distribution M(Y)−1M(·) and let Z be a Bernoulli random variable such that P(Z = 1) = p for some p ∈ (0, 1). Moreover, assume that ζ, (Xi)i∈N and Z are independent. Now, we consider the point process

$$\zeta _ { n , p } \colon = \zeta + 1 ( Z = 1 ) \sum _ { i = 1 } ^ { n } \delta _ { X _ { i } } \, . \\$$

Since ζ and ζn,p coincide on an event with probability 1 − p, we have that dTv(ζ, ζn,p) ≤ p. By taking h(μ) = μ(Y) as a test function in (2.6), we deduce that dR(ζ, ζn,p) ≥ np. Taking pn = 1/√n for p shows that

$$d _ { T V } ( \zeta , \zeta _ { n , p _ { n } } ) \to 0 \ \text { and } \ \text {d} _ { R } ( \zeta , \zeta _ { n , p _ { n } } ) \to \infty \, , \quad \text {as} \ \ n \to \infty \, ,$$

so that (ζn,pn)n∈N converges to ζ in total variation distance but not in Rubinstein distance.

Re-writing this as In the previous example the Rubinstein distance is stronger affected by the rare event that ζ ≠ ζn,pn than the total variation distance since the class of test functions is larger and contains functions taking also values different from zero and one. As already mentioned in the introduction, one can say that the difference between the Rubinstein distance and the total variation distance for point processes is similar to the difference between the Wasserstein and the total variation distance for integer-valued random variables. As particular example we cite the work [10], where Poisson approximation of random variables with respect to the Wasserstein distance has been considered, extending previous results for the total variation distance, see also Section 7.1 below.


<!-- p:8 -->


2.6 A discrete gradient. For a counting measure ω ∈ Ny and a measurable function h : NY → R let us introduce the discrete gradient in direction y ∈ Y by

$$D _ { y } h ( \omega ) \colon = h ( \omega + \delta _ { y } ) - h ( \omega ) \, ,$$

where, recall, δy is the unit-mass Dirac measure charging y ∈ Y. In our notation we often suppress the dependence of Dyh(ω) on the underlying counting measure ω and write Dyh. Clearly, if h ∈ L1, it holds that |Dyh| ≤ 1 for all y ∈ Y.

2.7 Geometric preparations. For our applications in Section 7, we need some facts from convex geometry. The Euclidean norm in Rd is denoted by ∥ ·∥. The Euclidean distance between two sets K1, K2 ⊂ Rd is given by

$$\text {dist} ( K _ { 1 } , K _ { 2 } ) = \inf \{ \| x _ { 1 } - x _ { 2 } \| \colon x _ { 1 } \in K _ { 1 } , x _ { 2 } \in K _ { 2 } \} \, .$$

If K1 = {x} with x ∈ Rd, we write dist(x, K2) instead of dist({x}, K2). For a measurable set K ⊂ Rd, we write vol(K) for the volume (i.e., d-dimensional Lebesgue measure) of K. For the volume of the unit ball Bd = {x ∈ Rd : ∥x∥ ≤ 1} in Rd, we introduce the abbreviation κd := vol(Bd). More generally, Bd(x, r) will denote the closed d-dimensional ball of radius r &gt; 0 centred at x ∈ Rd and we write Bd(r) instead of Bd(0, r) for short. For r ≥ 0, the Minkowski sum Kr = K + rBd of K and rBd is the so-called r-parallel set of K. In particular, if K is a convex set with non-empty interior, Steiner's formula (see e.g. [37, Equation (14.5)]) says that the volume vol(Kr) is a polynomial of degree d in r. Formally,

$$\text {vol} ( K _ { r } ) = \sum _ { i = 0 } ^ { d } \kappa _ { d - i } \, V _ { i } ( K ) \, r ^ { d - i } \, .$$

The coefficients V0(K), . . . , Vd(K) are the so-called intrinsic volumes of K, especially V0(K) = 1 whenever K ≠ Ø, V1(K) is a constant multiple of the mean width of K, Vd–1(K) is half of the surface area of K (if K is the closure of its interior) and Vd(K) = vol(K), cf. [37, Chapter 14.2].

by Am the space of m-dimensional affine subspaces of Rd. For L, M ∈ Gm let [L, M] be the subspace m determinant of L and M, that is the 2m-volume of a parallelepiped spanned by two orthonormal bases in L and in M. In one of our examples, we will also deal with the integrated subspace determinant and for this reason we recall that

$$\int _ { \mathbb { G } _ { m } ^ { d } } \int _ { \mathbb { G } _ { m } ^ { d } } [ L , M ] \, d L \, d M = \frac { \binom { d - m } { m } } { \binom { d } { m } } \frac { \kappa _ { d - m } ^ { 2 } } { \kappa _ { d } \kappa _ { d - 2 m } }$$

from [23, Lemma 4.4]. Here, dL and dM indicate integration with respect to the unique Haar probability measure on Gd m

## 3 Main results

### 3.1 General estimate

Let (Y, Y) be a lcscH space and let us fix another lcscH space (X, X). We adopt the notation introduced in Section 2 and denote by Nx the space of σ-finite counting measures on X.


<!-- p:9 -->


Let μ be a point process on X with a σ-finite intensity measure K(·) := Eμ(·). Fix an integer k ≥ 1 and let f : dom f → Y be a symmetric and measurable function, where dom f is a symmetric subset of Xk, i.e., if (x1, . , xk) ∈ dom f, then (xσ(1), . . . , xσ(k)) ∈ dom f for all permutations σ of {1, . . . , k}. We now apply f to all k-tuples of distinct points of μ contained in dom f to form a point process ξ, i.e.,

$$\xi \coloneqq \frac { 1 } { k ! } \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { \neq } ^ { k } \cap \text {dom} } \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } \, .$$

Since f is symmetric, every f(x1, . .. , xk) also appears for the k! permutations of the argument (x1, . . . , xk). However, for each subset {x1, . . . , xk } ⊂ μ of distinct points of μ we assign to f (x1, . . , xk) only multiplicity one as can be seen from the above definition of ξ. But ξ might still have points of multiplicity greater than one if there are different combinations of k points in X that are mapped under f to the same point in Y. The intensity measure of ξ is denoted by L and is given by

$$L ( A ) = E \xi ( A ) = E \sum _ { y \in \xi } 1 ( y \in A ) = \frac { 1 } { k ! } \, E \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { \neq } ^ { k } \cap \text {dom} } 1 ( f ( x _ { 1 } , \dots , x _ { k } ) \in A ) \, , \quad A \in \mathcal { Y } \, .$$

In what follows, we consider for μ two different types of point processes, namely Poisson processes and binomial processes. By η we denote a Poisson process on X with a σ-finite intensity measure K. By βn we denote a binomial process of n ∈ N points in X, which are independent and identically distributed in X according to a probability measure K1 on X. Such a binomial process βn has intensity measure K := nK1. Now the multivariate Mecke formula (2.1) and its binomial analogue (2.2) imply that the intensity measure L of ξ is given by

$$L ( A ) = \frac { 1 } { k ! } \int _ { \text {dom} } 1 ( f ( x _ { 1 } , \dots , x _ { k } ) \in A ) \, \text {K} ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \, , \quad A \in \mathcal { Y } \, ,$$

in the Poisson case and by

$$L ( A ) = \frac { ( n ) _ { k } } { k ! } \int _ { \text {dom} } 1 ( f ( x _ { 1 } , \dots , x _ { k } ) \in A ) \, K _ { 1 } ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \, , \quad A \in \mathcal { Y } \, ,$$

if we start with a binomial process (to deal with both cases simultanously we use the same notation for both set-ups). Let us finally introduce r(dom f) for k ≥ 2 by

$$1 \leq \ell \leq k - 1 \int _ { 0 }$$

and, for k = 1, put r(dom f) := 0. Moreover, we use the convention that (n − k)k/(n)k := 0 if n &lt; k. We can now state our main result, a functional limit theorem, which provides a bound on the Rubinstein distance between ξ and a suitable Poisson process on Y.

Theorem 3.1. Let ζ be a Poisson process on Y with finite intensity measure M. If ξ is induced by the Poisson process η, then

$$d _ { R } ( \xi , \zeta ) & \leq d _ { T V } ( L , M ) + 2 \left ( E \xi ( \mathbb { Y } ) ^ { 2 } - E \xi ( \mathbb { Y } ) - ( E \xi ( \mathbb { Y } ) ) ^ { 2 } \right ) \\ & \leq d _ { T V } ( L , M ) + \frac { 2 ^ { k + 1 } } { k ! } r ( \text {dom} \, f ) \, .$$

If otherwise ξ is derived from the binomial process βn, then

$$d _ { R } ( \xi , \zeta ) & \leq d _ { T V } ( L , M ) + 2 \left ( E _ { \xi } ( \mathbb { Y } ) ^ { 2 } - E _ { \xi } ( \mathbb { Y } ) - \frac { ( n - k ) _ { k } } { ( n ) _ { k } } ( E _ { \xi } ( \mathbb { Y } ) ) ^ { 2 } \right ) + \frac { 6 ^ { k } k ! } { n } \left ( E _ { \xi } ( \mathbb { Y } ) \right ) ^ { 2 } \\ & \leq d _ { T V } ( L , M ) + \frac { 2 ^ { k + 1 } } { k ! } r ( \text {dom} \, f ) + \frac { 6 ^ { k } k ! } { n } \, L ( \mathbb { Y } ) ^ { 2 } \, .$$


<!-- p:10 -->


- Remark 3.2. (i) If the underlying point process is a binomial process βn with n points and if n &lt; k, the point process ξ is empty with probability one and L ≡ 0. In this case, dR(ξ, ζ) ≤ Eζ(Y) = dTv(L, M) and the bound on dR (ξ, ζ) is trivially valid. For this reason, no further restriction on n is necessary.
- (ii) In the Poisson case, it can happen that L(Y) = ∞. In this case, we have dTv(L, M) = ∞ and the bound (3.3) is trivial. Hence, Theorem 3.1 is only of interest if L(Y) &lt; ∞, which is equivalent to Kk(dom f) &lt; ∞, a condition which ensures that ξ is almost surely finite.
- (iii) Taking M = L in the Poisson case in Theorem 3.1 shows that

$$d _ { R } ( \xi , \zeta ) \leq 2 ( E \xi ( \mathbb { Y } ) ^ { 2 } - E \xi ( \mathbb { Y } ) - ( E \xi ( \mathbb { Y } ) ) ^ { 2 } ) \leq \frac { 2 ^ { k + 1 } } { k ! } r ( \text {dom} \, f ) \, .$$

In particular, if k = 1, this gives dR(ξ, ζ) = 0, which in view of Proposition 2.1 implies that ξ is a Poisson process. This is consistent with the well known mapping theorem for Poisson processes, for which we refer to [25, Chapter 2.3].

- (iv) If X = Y and f : X → X is the identity, Theorem 3.1 yields that, for Poisson processes ξ and ζ with finite intensity measures L and M, respectively,

$$d _ { R } ( \xi , \zeta ) \leq d _ { T V } ( L , M ) \, .$$

In other words, the Rubinstein distance between two Poisson processes is bounded by the total variation distance of their intensity measures. For a similar estimate in a more restricted set-up we refer to [20, Proposition 4.1].

### 3.2 The Euclidean case

In this subsection we shall apply our general estimate of Theorem 3.1 to the important situation that the target space Y is Rd endowed with the standard Borel σ-field B(Rd). This is tailored towards some of our applications in Section 7 and is similar to the set-up in [41, 42]. We let (X, X) be a lcscH space and let (ηt)t≥1 be a family of Poisson processes in X with intensity measures Kt = tK, t ≥ 1, where K is a fixed σ-finite measure. By (βt)t≥1 we denote a family of binomial processes such that βt = β[t] and β[t] is a process of [t] points chosen independently according to a fixed probability measure K1. In this situation we use the notation Kt := [t]K. We write (μt)t≥1 in the sequel to indicate either (ηt)t≥1 or (βt)t≥1.

For a fixed integer k ≥ 1 we consider symmetric and measurable functions ft : Xk → Rd, t ≥ 1. We are interested in the behaviour of the derived point processes

$$\xi _ { t } \coloneqq \frac { 1 } { k ! } \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { t , \neq } ^ { k } } \delta _ { f _ { t } ( x _ { 1 } , \dots , x _ { k } ) } \, , \quad t \geq 1 \, .$$

For this reason, we consider the re-scaled point processes

$$t ^ { \gamma } \bullet \xi _ { t } \colon = \frac { 1 } { k ! } \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { t , \neq } ^ { k } } \delta _ { t ^ { \gamma } f _ { t } } ( x _ { 1 } )$$

where γ ∈ R is a suitable constant. In order to compare tγ · ξt with a Poisson process, we need to introduce the following notation. The intensity measure Lt of the re-scaled point process tγ · ξt is given by

$$\text { by } & & L _ { t } ( B ) \coloneqq \frac { 1 } { k ! } \text { } E \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { t , \neq } ^ { k } } 1 ( f _ { t } ( x _ { 1 } , \dots , x _ { k } ) \in t ^ { - \gamma } B ) \, , \quad B \in \mathcal { B } ( \mathbb { R } ^ { d } ) \, . \\ B \subset \mathcal { K } ( \mathbb { P } ( d ) \, \bmod t _ { * } \, ( B ) \, h _ { \colon } & \, \min i t s _ { k = 0 } ( B ) \, , \quad 0 \, f _ { k } \, h _ { k } \, , \, 1 \, \text { and } \\$$

r  =  ( =: ()   ( ()  (p)   nd

$$r _ { t } ( B ) \colon = \max _ { 1 < \ell < k - 1 } \left | \max _ { v \in B } \left | \max _ { v \in B } \right | \right |$$

for k ≥ 2. Furthermore, for a measure ν on Rd and B ∈ B(Rd) let ν|B be the restriction of ν to B.


<!-- p:11 -->


Corollary 3.3. Let ζ be a Poisson process on Rd with intensity measure M and let B ∈ B(Rd) be such that M(B) &lt; ∞. If ξt is induced by a Poisson process ηt with t ≥ 1, then

$$d _ { R } ( ( t ^ { \gamma } \bullet \xi _ { t } ) | _ { B } , \zeta | _ { B } ) & \leq d _ { T V } ( \L _ { t } | _ { B } , M | _ { B } ) + 2 ( E \xi _ { t } ( t ^ { - \gamma } B ) ^ { 2 } - E \xi _ { t } ( t ^ { - \gamma } B ) - ( E \xi _ { t } ( t ^ { - \gamma } B ) ) ^ { 2 } ) \\ & \leq d _ { T V } ( \L _ { t } | _ { B } , M | _ { B } ) + \frac { 2 ^ { k + 1 } } { k ! } r _ { t } ( B ) \, .$$

If ξt is induced by a binomial process βt with t ≥ 1, then

$$If \xi _ { t } \text { is induced by a binomial process } \beta _ { t } \text { with } t \geq 1 , \text { then} \\ d _ { \Gamma } ( ( t ^ { \gamma } \bullet \xi _ { t } ) | _ { B } , \zeta | _ { B } ) & \leq d _ { T V } ( L _ { t } | _ { B } , M | _ { B } ) + 2 \left ( E _ { \xi _ { t } } ( t ^ { - \gamma } B ) ^ { 2 } - E _ { \xi _ { t } } ( t ^ { - \gamma } B ) - \frac { ( [ t ] - k ) _ { k } } { ( [ t ] ) _ { k } } ( E _ { \xi _ { t } } ( t ^ { - \gamma } B ) ) ^ { 2 } \right ) \\ & + \frac { 6 ^ { k ! } k } { t } ( E _ { \xi _ { t } } ( t ^ { - \gamma } B ) ) ^ { 2 } \\ & \leq d _ { T V } ( L _ { t } | _ { B } , M | _ { B } ) + \frac { 2 ^ { k + 1 } } { k ! } r _ { t } ( B ) + \frac { 6 ^ { k ! } k } { t } L _ { t } ( B ) ^ { 2 } \, . \\ \intertext { P o r f . $ \text { This is a direct consequence of Theorem 3.1$ with } t \ncong \xi _ { t } | _ { B } $ }$$

Proof. This is a direct consequence of Theorem 3.1 with tγ · ξt|B instead of ξ and ζ|B instead of ζ there. □

In view of limit theorems, the most natural choice for M is to take M as the strong limit of the measures Lt, as t → ∞. That is,

$$M ( B ) = \lim _ { t \to \infty } L _ { t } ( B ) \quad \text {for all $B\in\mathcal{B}(\mathbb{R}^{d})$} .$$

However, we emphasize that this does not necessarily imply that dTv(Lt, M) → 0, as t → ∞, even though this is true for our applications presented below.

- Remark 3.4. (i) The upper bounds in Corollary 3.3 are not uniform in the sense that they depend on the set B. This was to be expected since the re-scaled point processes tγ · ξt can be finite for any t ≥ 1, while a realization of ζ can charge an infinite number of points (compare with our applications in Section 7). This is the reason for introducing the restriction to the set B, which allows us to compare tγ · ξt|B with ζ|B using the Rubinstein distance.
- (ii) To allow for an easier comparison with the previous paper [41], we remark that ibidem the Poisson case for d = 1 is considered. Moreover, the intensity measure M there is concentrated on the positive real half-axis and has the form

$$M ( B ) = a \, b \int _ { B } 1 ( u \geq 0 ) \, u ^ { b - 1 } \, d u \, , \quad B \in \mathcal { B } ( \mathbb { R } ) \, ,$$

for some constants a, b &gt; 0. In this case, the Poisson process ζ is a so-called Weibull process since the distance from the origin to the closest point of ζ is Weibull distributed with distribution function u → (1 − exp(−a ub)) 1(u &gt; 0). We remark that this form of M was tailored to the applications in [41], a more general version is stated without proof in [42].

- (iii) Note that rt(B) is dominated by Lt(B)^t(B), where τt(B) is defined as

$$\hat { r } _ { t } ( B ) \coloneqq \max _ { \substack { 1 \leq \ell \leq k - 1 , \\ ( x _ { 1 } , \dots , x _ { \ell } ) \in \mathbb { K } ^ { \ell } } } K _ { t } ^ { k - \ell } ( \{ ( y _ { 1 } , \dots , y _ { k - \ell } ) \in \mathbb { K } ^ { k - \ell } \colon f _ { t } ( x _ { 1 } , \dots , x _ { \ell } , y _ { 1 } , \dots , y _ { k - \ell } ) \in t ^ { - \gamma } B \} )$$

for B ∈ B(Rd). A quantity similar to ît(B) has also played a prominent rôle in the previous study [41]. In many applications a bound for ît(B) is already sufficient in order to apply Corollary 3.3. However, there are situations for which t(B) is an increasing function in t, while rt(B) tends to zero, as t → ∞. This way, [41, Theorem 1.1], in which ît instead of rt appears, is not applicable in such cases as erroneously done in Sections 2.5 and 2.6 ibidem. However, in these specific cases it is readily checked that rt behaves nicely, implying that the results there are correct.


<!-- p:12 -->


## 4 A general Stein principle

This section is devoted to a more informal discussion about the method of bounding the Rubinstein distance between point processes using a Stein principle. This approach is the key argument of our proof of Theorem 3.1 in Section 6. Recall that the aim is to provide an upper bound for the Rubinstein distance between a Poisson process ζ on a space Y with finite intensity measure M and a second point process ξ on Y, which in turn is derived from another point process μ on a space X by a transformation.

The first part of Stein's method consists in characterizing the target object, here the Poisson process ζ. The way is to consider a functional operator L which, at a formal level, satisfies for a finite point process ν the identity

$$\mathbf E [ L F ( \nu ) ] = 0 \quad \text {for a large class of functions} \ F \colon \widehat { N } _ { \mathbb { Y } } \to \mathbb { R }$$

if and only if ν is a Poisson process with intensity measure M. It is usually not difficult to construct such an operator for a given target object. What may become challenging, especially in infinite dimensions (compare with [3, 16, 43]), is to prove that the target object is the unique solution of (4.1). In our case, uniqueness follows from the theory of spatial birth-death processes, see [34].

The second step of Stein's method is to solve the so-called Stein equation

$$L F ( \omega ) = \mathbf E h ( \zeta ) - h ( \omega ) \, , \quad \omega \in \widehat { N } _ { \mathbb { Y } } \, ,$$

for a certain class of test functions h : NY → R. This means that we have to compute a solution Fh for a given test function h and to evaluate LFh(ω).

A prominent method to do this is the so-called generator approach (see the survey article [35] and the references cited therein). The underlying idea is to interpret L as infinitesimal generator of a Markov process with the distribution of ζ as its invariant distribution, whence L satisfies (4.1). If (Ps)s≥0 is the semi-group associated with this Markov process, one can show that

$$L F _ { h } ( \omega ) = \int _ { 0 } ^ { \infty } L P _ { s } h ( \omega ) \, \mathrm d s \, , \quad \omega \in \widehat { N } _ { \mathbb { Y } } \, .$$

In order to compare the point process ξ with ζ, we put ω = ξ and take expectations in (4.2) and (4.3). This leads to

$$E h ( \zeta ) - E h ( \xi ) = E L F _ { h } = \mathbf E \, \int _ { 0 } ^ { \infty } L P _ { s } h ( \xi ) \, d s \, .$$

To derive this identity rigorously is the content of the subsequent section. In the context of our main result, the point process ξ is induced by an underlying point process μ on another space X. More, formally we have that ξ = T(μ), where T is a suitable transformation, i.e., a mapping from Nx to Ny. Hence, we will have to compute

$$\mathbf E \int _ { 0 } ^ { \infty } L P _ { s } h ( T ( \mu ) ) \, d s \, . \\$$

This expression is bounded in Section 6 by exploiting the special structure of the transformation T and the fact that μ is a Poisson or binomial process.

## 5 Glauber dynamic for the Poisson process

We now specialize the general scheme outlined in Section 4 to our particular situation. Although the approach is similar to [4, Section 2], for example, we prefer to carry out the details here since we consider a different class of test functions, namely Lipschitz functions instead of bounded functions. We assume the same set-up as for Theorem 3.1, that is, ζ is a Poisson process on a lcscH space Y with a finite intensity measure M and distribution Pζ. We now construct a Glauber dynamic for Pζ, that is a continuous-time Markov process (G(s))s≥0 with state space Ñy and Pζ as its stationary (i.e., invariant) distribution, see [34]. Its generator L is given by

$$L h ( \omega ) \coloneqq \int _ { \mathbb { Y } } h ( \omega + \delta _ { y } ) - h ( \omega ) \, \mathbf M ( d y ) + \int _ { \mathbb { Y } } h ( \omega - \delta _ { y } ) - h ( \omega ) \, \omega ( d y ) \, , \quad \omega \in \widehat { N } _ { \mathbb { Y } } \, ,$$


<!-- p:13 -->


where h : Ny → R is a measurable and bounded function. According to our notational convention, L may be re-written as

$$L h ( \omega ) = \int _ { \mathbb { Y } } h ( \omega + \delta _ { y } ) - h ( \omega ) \, M ( d y ) + \sum _ { y \in \omega } h ( \omega - \delta _ { y } ) - h ( \omega ) \, .$$

Note that Lh(ω) is well-defined for all h ∈ L1 and ω ∈ NY, since the Lipschitz property implies that the integrands in (5.1) are bounded by one. Moreover, we notice that the operator L uniquely determines the process (G(s))s≥0, which has Pζ as its unique invariant distribution, see [18, Proposition 10.4.VII] or [34].

The Markov process (G(s))s≥0 is a spatial birth-death process in continuous time whose dynamic can be described as follows. If at time s, the system is in state ωs, each particle charged by ωs dies at rate 1 and a new particle is born at y with rate M(dy). Alternatively, imagine a homogeneous Poisson process ζb on R+ with intensity M(Y). The jump times of ζb determine the birth times of the particles in ζ. At each jump of ζb a new particle is born and is placed in Y according to the distribution M(·)/M(Y), independently of the current configuration. Moreover, each particle has a lifetime which is exponentially distributed with parameter 1, independent of the past and of the rest of the configuration, see again [34].

The semi-group (Ps)s≥0 associated with the Markov process (G(s))s≥0 is defined as

$$P _ { s } h ( \omega ) = \mathbf E [ \, h ( G ( s ) ) \, | \, G ( 0 ) = \omega \, ] \, , \quad \omega \in \widehat { N } _ { \mathbb { Y } } \, , \quad h \, \colon \widehat { N } _ { \mathbb { Y } } \rightarrow \mathbb { R } \, .$$

For h ∈ L1 and ω ∈ ÑY the conditional expectation is always well defined, since

$$| P _ { s } h ( \omega ) | & = | E [ h ( G ( s ) ) \, | \, G ( 0 ) = \omega ] | \\ & \leq E [ \, | \, h ( G ( s ) ) - h ( \omega ) \, | \, | \, G ( 0 ) = \omega \, ] + | h ( \omega ) | \\ & \leq E [ d _ { T V } ( G ( s ) , \omega ) \, | \, G ( 0 ) = \omega ] + | h ( \omega ) | \\ & \leq E \zeta _ { b } ( [ 0 , s ] ) + \omega ( \mathbb { Y } ) + | h ( \omega ) | < \infty \, ,$$

where ζb is the homogeneous Poisson process from the description of the birth-death dynamic above. Below we will need the following lemmas about the process (G(s))s≥0 and its semi-group (Ps)s≥0. The first one provides a commutation relation between the discrete gradient and the semi-group.

Lemma 5.1. For any s ≥ 0, ω ∈ ÑY, y ∈ Y and h ∈ L1,

$$D _ { y } P _ { s } h ( \omega ) = e ^ { - s } \, P _ { s } ( D _ { y } h ) ( \omega ) \, .$$

Proof. To construct a sample path of (G(s))s≥0, given the initial configuration G(0) = ω + δy, we have to add the independent particle y to a realization of (G(s))s≥0 starting from the initial configuration ω. These two realizations will be identical after the particle y has died. Thus, denoting by l(y) the lifetime of y and using (5.2), we can write

$$\begin{array} { r l } { D _ { y } P _ { s } h ( \omega ) } & { = } & { \mathbf E [ h ( G ( s ) ) \, | \, G ( 0 ) = \omega + \delta _ { y } ] - \mathbf E [ h ( G ( s ) ) \, | \, G ( 0 ) = \omega ] } \\ & { = } & { \mathbf E [ ( h ( G ( s ) + \delta _ { y } ) - h ( G ( s ) ) ) \, 1 ( \ell ( y ) \geq s ) \, | \, G ( 0 ) = \omega ] \, . } \end{array}$$

Since l(y) is independent of everything else and is exponentially distributed with mean one, we can continue with

$$D _ { y } P _ { s } h ( \omega ) = \mathbf E [ 1 ( \ell ( y ) \geq s ) ] \, \mathbf E [ ( h ( G ( s ) + \delta _ { y } ) - h ( G ( s ) ) ) \, | \, G ( 0 ) = \omega ] = e ^ { - s } \, P _ { s } ( D _ { y } h ) ( \omega ) \, ,$$

where we have used (5.2) again. This completes the proof.

□

Lemma 5.2. Let ω1, ω2 ∈ ÑY with ω2 ⊂ ω1. If h ∈ L1 and s ≥ 0, then

$$\left | E [ h ( G ( s ) ) \, | \, G ( 0 ) = \omega _ { 1 } ] - E [ h ( G ( s ) ) \, | \, G ( 0 ) = \omega _ { 2 } ] \right | \leq ( \omega _ { 1 } \, \omega _ { 2 } ) ( \mathbb { Y } ) \, e ^ { - s } \, .$$


<!-- p:14 -->


Proof. Recall that each particle y of the initial configuration G(0) has an exponentially distributed lifetime l(y) with mean one. Thus, since h ∈ L1, it holds that

$$\text {e} ( y ) \text { with mean one.  Thus, since $h\in\mathcal{Z}_{1}$, it holds that } \\ | E [ h ( G ( s ) ) | \, | G ( 0 ) = \omega _ { 1 } ] - E [ h ( G ( s ) ) | \, G ( 0 ) = \omega _ { 2 } ] | \\ & \leq E [ | h ( G ( s ) + \sum _ { y \in \omega _ { 1 } \ \omega _ { 2 } } 1 ( \ell ( y ) \geq s ) \delta _ { y } ) - h ( G ( s ) ) | \, | G ( 0 ) = \omega _ { 2 } ] \\ & \leq E [ d _ { T Y } ( G ( s ) + \sum _ { y \in \omega _ { 1 } \ \omega _ { 2 } } 1 ( \ell ( y ) \geq s ) \delta _ { y } , G ( s ) ) | \, G ( 0 ) = \omega _ { 2 } ] \\ & \leq E \sum _ { y \in \omega _ { 1 } \ \omega _ { 2 } } 1 ( \ell ( y ) \geq s ) \\ & = ( \omega _ { 1 } \, \langle \, \omega _ { 2 } \rangle ( \mathbb { Y } ) \, e ^ { - s } \, , \\ \intertext { c h o r v e s the claim. }$$

which proves the claim.

Lemma 5.3. For any ω ∈ ÑY and h ∈ L1,

$$\lim _ { s \to \infty } P _ { s } h ( \omega ) = E h ( \zeta ) = \int h \, d P _ { \zeta } \, .$$

Proof. We notice first that the expectation on the right-hand side is well defined since h ∈ L1 implies that

$$\mathbf E | h ( \zeta ) | \leq \mathbf E | h ( \zeta ) - h ( \emptyset ) | + | h ( \emptyset ) | \leq \mathbf E d _ { \text {TV} } ( \zeta , \emptyset ) + | h ( \emptyset ) | \leq \mathbf E \zeta ( \mathbb { Y } ) + | h ( \emptyset ) | = \text {M} ( \mathbb { Y } ) + | h ( \emptyset ) | \, ,$$

where Ø stands for the counting measure that corresponds to the empty point configuration.

From Lemma 5.2 with ω1 = ω and ω2 = ∅ we have that

$$\left | E \left [ h ( G ( s ) ) \, | \, G ( 0 ) = \omega \right ] - \mathbf E \left [ h ( G ( s ) ) \, | \, G ( 0 ) = \emptyset \right ] \right | \leq \omega ( \mathbb { Y } ) \, e ^ { - s } \, .$$

The number of particles of G(s) starting from the empty configuration follows the evolution of an M/M/∞ queue with arrival (birth) rate M(Y) and service (death) rate 1, and thus is Poisson distributed with parameter (1 − e−8)M(Y). Since the position of each of the particles is independent of everything else, G(s) has the same distribution as a Poisson process on Y with intensity measure (1 - e−8)M. Since ζ has the same distribution as the superposition of two independent Poisson processes with intensity measures (1 − e−s)M and e−sM, respectively, we obtain that

$$| \mathbf E [ h ( G ( s ) ) \, | \, G ( 0 ) = \emptyset ] - \mathbf E h ( \zeta ) | \leq e ^ { - s } \mathbf M ( \mathbb { Y } ) \, .$$

Combining (5.3) and (5.4) and letting s → ∞ concludes the proof.

□

The next lemma, which can be seen as an integration by parts formula, is the key for the proof of Theorem 3.1 given in Section 6 below.

Lemma 5.4. If h ∈ L1 and ω ∈ NY, then

$$E h ( \zeta ) - h ( \omega ) = \int _ { 0 } ^ { \infty } L P _ { s } h ( \omega ) \, \dot { c }$$

$$\intertext {  } L P _ { s } h ( \omega ) \, d s \, .$$

Proof. For an arbitrary h ∈ L1 we define hn : NY → R, n ∈ N, by

$$h _ { n } ( \omega ) = \begin{cases} n & \colon h ( \omega ) > n \\ h ( \omega ) & \colon - n \leq h ( \omega ) \leq n \\ - n & \colon h ( \omega ) < - n \, . \end{cases}$$

□


<!-- p:15 -->


Clearly, each of the functions hn is bounded and belongs to L1. Since hn is bounded, the forwardbackward equation stated as Theorem 12.22 in [24] implies that

$$P _ { t } h _ { n } ( \omega ) - h _ { n } ( \omega ) = \int _ { 0 } ^ { t } L P _ { s } h _ { n } ( \omega ) \, d s \, , \ \ t \geq 0 \, .$$

By construction, we have hn(ω) → h(ω), as n → ∞. The dominated convergence theorem implies h  ()  0  s  d ∞ ←   () ← () d  ()d ← () d1 na 5.1, we have that, for g = h or g = hn and s ≥ 0,

$$| L P _ { s } g ( \omega ) | & \leq \int _ { \mathbb { Y } } e ^ { - s } | P _ { s } ( D _ { y } g ) ( \omega ) | \, \text {M} ( d y ) + \int _ { \mathbb { Y } } e ^ { - s } | P _ { s } ( D _ { y } g ) ( \omega - \delta _ { y } ) | \, \omega ( d y ) \\ & \leq e ^ { - s } ( \text {M} ( \mathbb { Y } ) + \omega ( \mathbb { Y } ) ) \, .$$

In the last step we used the fact that |Ps(Dyg)| ≤ 1. Now, a further application of the dominated convergence theorem shows that

$$\lim _ { n \to \infty } \int _ { 0 } ^ { t } L P _ { s } h _ { n } ( \omega ) \, \mathrm d s = \int _ { 0 } ^ { t } L P _ { s } h ( \omega ) \, \mathrm d s \, , \quad t \geq 0 \, ,$$

so that, letting n → ∞ in (5.6), yields

$$P _ { t } h ( \omega ) - h ( \omega ) = \int _ { 0 } ^ { t } L P _ { s } h ( \omega ) \, d s \, , \quad t \geq 0 \, .$$

Because of (5.7) and the dominated convergence theorem, the right-hand side of (5.8) converges to the right-hand side of (5.5), as t → ∞. Together with Lemma 5.3 for the left-hand side, this concludes the proof. □

Remark 5.5. The operator L and the associated semi-group (Ps)s≥0 on the Poisson space can be also defined via the Wiener-Itô chaos expansion, which we recall now for completeness. We still denote by ζ a Poisson process with intensity measure M on a lcscH space Y. A crucial property of ζ is that any square integrable functional F ∈ L2(Pζ) of ζ can be written as

$$F = \mathbf E F + \sum _ { n = 1 } ^ { \infty } I _ { n } ( f _ { n } )$$

with

$$f _ { n } ( y _ { 1 } , \dots , y _ { n } ) = \frac { 1 } { n ! } \, \mathbf E D _ { y _ { 1 } , \dots , y _ { n } } ^ { n } \, F ( \zeta ) \, , \quad y _ { 1 } , \dots , y _ { n } \in \mathbb { Y } \, , \quad n \geq 1 \, ,$$

where Dn := D  Dn-1 with D1 := D is the n-th iteration of the discrete gradient D introduced in Section 2, and where In(fn) stands for the n-fold Wiener-Itô integral of the square integrable and symmetric function fn with respect to the signed random measure ζ —M. Moreover, the series in (5.9) converges in L2(Pζ) and is called the Wiener-Itô chaos expansion of F (we refer to [28] for further details). We can now define the Ornstein-Uhlenbeck generator L on the Poisson space by

$$L F = - \sum _ { n = 1 } ^ { \infty } n I _ { n } ( f _ { n } ) \, ,$$

whenever F belongs to dom L, i.e., F is such that Σn=1 n2 n! n∥ž2(Mn) &lt; ∞, where ∥· ∥z2(Mn) stands for the usual norm in L2(Mn). We remark that LF can equivalently be written as in (5.1) as a consequence of identity (3.19) in [28] and of the relation stated in [32, Lemma 2.11] between the discrete gradient, the Ornstein-Uhlenbeck generator and the so-called Skorohod-integral on the Poisson space, another operator, which is not needed in the sequel. In [27] the relation between the inverse of the Ornstein-Uhlenbeck generator and the associated semi-group is investigated. The semi-group (Ps)s≥0 can be written in terms of the Wiener-Itô chaos expansion as


<!-- p:16 -->


$$P _ { s } F = \text {EF} + \sum _ { n = 1 } ^ { \infty } e ^ { - n s } I _ { n } ( f _ { n } ) \, , \quad s \geq 0 \, , \\$$

ht    s (  s s t  t  st s    t ton (3.13)]). Lemma 5.1 is a special case of [27, Lemma 3.1] and Lemma 5.2, Lemma 5.3 and Lemma 5.4 can also be derived via the approach sketched in this remark. However, we preferred to give proofs wrod r o ans r res ro e- o rr te

## 6 Proof of Theorem 3.1

Before going into the details of the proof of Theorem 3.1, we explain the strategy informally in case of an underlying Poisson process η. Applying the multivariate Mecke formula (2.1) in Equation (6.4) below, we are lead to estimate the integral with respect to Kk of

$$( 6 . 1 ) \quad \mathbf E \left [ F ( \xi ( \eta + \delta _ { x _ { 1 } } + \dots + \delta _ { x _ { k } } ) - \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) - F ( \xi ( \eta + \delta _ { x _ { 1 } } + \dots + \delta _ { x _ { k } } ) ) \right ] , \quad x _ { 1 } , \dots , x _ { k } \in \mathbb { X } ,$$

with F : NY → R being a certain point process functional and where we write ξ(μ) instead of ξ to underpin the dependence of ξ on the underlying point configuration μ. The difficulty comes from the fact that adding δx1 + . .. + δxk to the Poisson process η, amounts not only in adding δf(x1,.,.xk) to ξ(η) but also all atoms of the form f (xi1, . . . , xie, xe+1, . . . , xk) with l ∈ {1, . . . , k}, pairwise different of these extra atoms. The difference in (6.1) is now decomposed as

$$E [ ( F ( \xi ( \eta ) + \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \eta ) ) - F ( \xi ( \eta ) ) ) + ( F ( \xi ( \eta ) ) - F ( \xi ( \eta ) + \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) ) \\ + \left ( F ( \xi ( \eta ) + \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) - F ( \xi ( \eta ) + \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \eta ) + \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) \right ) ] \, . \\ \intertext { E [ ( F ( \xi ( \eta ) + \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \eta ) ) - F ( \xi ( \eta ) ) ) + ( F ( \xi ( \eta ) ) - F ( \xi ( \eta ) + \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) ) ) ] \, .$$

The middle term in (6.2) contributes to the total variation distance of the intensity measures in (3.3) in Theorem 3.1. Since F is Lipschitz, the expectation and the integral with respect to x1, . . . , xk of the first and the third term in (6.2) are bounded (up to a constant) by

$$E \int \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \eta ) ( \mathbb { Y } ) \, K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \, ,$$

which in turn is bounded by Eξ(Y)2 − Eξ(Y) − (Eξ(Y))2 and r(dom f). This effect contributes to the second term of the bounds in Theorem 3.1. For k = 1, only the middle term in (6.2) is present. This explains, why for k = 1 the Rubinstein distance between the transformation of a Poisson process (which is again a Poisson process) and a second Poisson process is bounded by the total variation distance of the intensity measures and the second term in (3.3) in Theorem 3.1 vanishes.

Throughout this section we use the same notation as in Subsection 3.1. Moreover, let [k] be shorthand for {1, . . , k }. For x = (x1, . . . , xk) ∈ Xk, I = {i1, . . . , i|1|} ⊂ [k] and z = (z1, . . . , k−|1|) ∈ Xk−||, let (x1, z) = (xi, . . ,xi|1|, 1, . . ., k−||). We prepare the proof of Theorem 3.1 with the following lemma.

Lemma 6.1. Let the assumptions of Theorem 3.1 prevail. If ξ is induced by a Poisson process, then

$$E \xi ( \mathbb { Y } ) ^ { 2 } = \frac { 1 } { k ! } \sum _ { I \subset [ k ] } \frac { 1 } { ( k - | I | ) ! }$$

$$\mathbf E _ { \xi } ( \mathbb { Y } ) ^ { 2 } & = \frac { 1 } { k } \sum _ { I \subset [ k ] } \frac { 1 } { ( k - | I | ) ! } \int _ { \mathbb { X } ^ { k } } \int _ { \mathbb { X } ^ { k - | I | } } 1 ( ( x _ { 1 } , \dots , x _ { k } ) \in \text {dom} \, f ) \\ & \quad \times 1 ( ( x _ { I } , z ) \in \text {dom} \, f ) \, K ^ { k - | I | } ( d z ) \, K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \, .$$

If ξ is derived from a binomial process of n points, then

$$\mathfrak { E } _ { \xi ( \Psi ) ^ { 2 } } = \frac { 1 } { k ! } \sum _ { I \subset [ k ] } \frac { ( n ) _ { 2 k - | I | } } { ( k - | I | ) ! } \int _ { \mathbb { X } ^ { k } } \int _ { \mathbb { X } ^ { k - | I | } } \mathbf 1 ( ( x _ { 1 } , \dots , x _ { k } ) \in \text {dom} \, f ) \\ \times \mathbf 1 ( ( x _ { I } , z ) \in \text {dom} \, f ) \, K _ { 1 } ^ { k - | I | } ( d z ) \, K _ { 1 } ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \, .$$


<!-- p:17 -->


Proof. We have that

$$P r o f . \ \ We \ have \text {that} \quad \\ \xi ( \Upsilon ) ^ { 2 } = \frac { 1 } { ( k ! ) ^ { 2 } } \left ( \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { k } ^ { \neq } } 1 ( ( x _ { 1 } , \dots , x _ { k } ) \in \text {dom} \, f ) \right ) ^ { 2 } \\ = \frac { 1 } { ( k ! ) ^ { 2 } } \sum _ { I \subset [ k ] } \sum _ { ( x _ { 1 } , \dots , x _ { k } , z ) \in \mu _ { k } ^ { 2 - | I | } } \frac { k ! } { ( k - | I | ) ! } 1 ( ( x _ { 1 } , \dots , x _ { k } ) \in \text {dom} \, f ) 1 ( ( x _ { 1 } , z ) \in \text {dom} \, f ) , \\ \intertext { w h e v . \ } \text {where} \, \text {we have used that two points occurring in different sums can be either equal or distinct and}$$

where we have used that two points occurring in different sums can be either equal or distinct and that dom f is symmetric. Now the multivariate Mecke (2.1) and its binomial analogue (2.2) conclude the proof. □

Proof of Theorem 3.1. Throughout this proof we write ξ(η) and ξ(βn) to emphasize the dependence of ξ on the underlying point process. Whenever we do not need special properties of η or βn, we write ξ(μ) with the dummy variable μ standing for either η or βn. As discussed in Remark 3.2 (ii), we can assume for the Poisson case that L(Y) &lt; ∞ and, hence, that ξ(η) is almost surely finite since (3.3) is obviously true otherwise. For an underlying binomial process it is sufficient to consider only the case n ≥ k since, otherwise, the statement is obviously true as explained in Remark 3.2 (i).

Lemma 5.4 says that, for h ∈ L1 and ω ∈ ÑY,

$$E h ( \zeta ) - h ( \omega ) = \int _ { 0 } ^ { \infty } L P _ { s } h ( \omega ) \, d s \, .$$

The Stein-type identity (6.3) is the starting point for our proof. Combining (6.3) with the representation of the generator L in (5.1), choosing ω = ξ(μ) and taking expectations results into

$$\text {ation of the generator } L \text { in } ( 5 . 1 ) , \text { choosing } \omega = \xi ( \mu ) \text { and taking expectations results into
 } \\ \text {Eh} ( \zeta ) - \text {Eh} ( \xi ( \mu ) ) & = E \int _ { 0 } ^ { \infty } L P _ { s } h ( \xi ( \mu ) ) \, d s \\ & = E \int _ { 0 } ^ { \infty } \int _ { Y } \left ( P _ { s } h ( \xi ( \mu ) + \delta _ { y } ) - P _ { s } h ( \xi ( \mu ) ) \right ) M ( d y ) \, d s \\ & + E \int _ { 0 } ^ { \infty } \sum _ { y \in \xi ( \mu ) } \left ( P _ { s } h ( \xi ( \mu ) - \delta _ { y } ) - P _ { s } h ( \xi ( \mu ) ) \right ) d s \, . \\ \intertext { L e t u s d e n o t e h i s t r i n g t a n d t h e i n t e r m o n t h e r g h e d s y b i s y } \text {By}$$

Let us denote the first and the second term on the right-hand side by T1,μ and T2,μ, respectively. By Fubini's theorem and the definition of ξ(μ), we obtain that

$$T _ { 2 , \mu } = \frac { 1 } { k ! } \int _ { 0 } ^ { \infty } \mathbf E \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { \neq } ^ { k } \cap \text {dom} } \left ( P _ { s } h ( \xi ( \mu ) - \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) - P _ { s } h ( \xi ( \mu ) ) \right ) \mathrm d s \, .$$

By the multivariate Mecke formula (2.1) and its analogue (2.2) for binomial processes, we see that

$$T _ { 2 , \eta } = \frac { 1 } { k ! } \int _ { 0 } ^ { \infty } \int _ { d o m \, f } \mathbf E \left [ P _ { s } h ( \xi ( \eta + \delta _ { x _ { 1 } } + \dots + \delta _ { x _ { k } } ) - \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) \right ) \\ & - P _ { s } h ( \xi ( \eta + \delta _ { x _ { 1 } } + \dots + \delta _ { x _ { k } } ) ) \right ] \mathbf K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \, d s$$

$$T _ { 2 , \beta _ { n } } = \frac { ( n ) _ { k } } { k ! } \int _ { 0 } ^ { \infty } \int _ { \text {dom} } E [ P _ { s } h ( \xi ( \beta _ { n - k } + \delta _ { x _ { 1 } } + \dots + \delta _ { x _ { k } } ) - \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) \\ & - P _ { s } h ( \xi ( \beta _ { n - k } + \delta _ { x _ { 1 } } + \dots + \delta _ { x _ { k } } ) ) ] \, \mathbf K _ { 1 } ^ { k } ( \text {d} ( x _ { 1 } , \dots , x _ { k } ) ) \, \text {ds} .$$

Let us write ξ(x1, . . . , xk, μ) for the point process

$$\hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \mu ) \colon = \sum _ { \emptyset \neq I \subseteq [ k ] , \, z \in \mu _ { \neq } ^ { k - 1 / I } } \frac { 1 } { ( k - | I | ) ! } \, 1 ( ( x _ { I } , z ) \in \text {dom} \, f ) \, \delta _ { f ( x _ { I } , z ) }$$


<!-- p:18 -->


on Y, where ¢ denotes proper set-inclusion and where the notation (x1, z) has been introduced before Lemma 6.1 above. Then

$$\text {Lemma 6.1 above. Then} \\ T _ { 2 , \eta } = \frac { 1 } { k ! } \int _ { 0 } ^ { \infty } \int _ { \text {dom} f } E [ P _ { s } h ( \xi ( \eta ) + \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \eta ) ) \\ - P _ { s } h ( \xi ( \eta ) + \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \eta ) + \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) ] \, K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \, d s \\ = - \frac { 1 } { k ! } \int _ { 0 } ^ { \infty } \int _ { \text {dom} f } E [ P _ { s } h ( \xi ( \eta ) + \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) - P _ { s } h ( \xi ( \eta ) ) ] \, K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \, d s \\ + \frac { 1 } { k ! } \int _ { 0 } ^ { \infty } \int _ { \text {dom} f } E [ P _ { s } h ( \xi ( \eta ) + \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \eta ) ) - P _ { s } h ( \xi ( \eta ) ) + P _ { s } h ( \xi ( \eta ) + \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) ) \\ - P _ { s } h ( \xi ( \eta ) + \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \eta ) + \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) ] \, K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \, d s \\ = \hat { T } _ { 2 , \eta } + R _ { \eta } \\ \text {and}$$

$$\text { and } \\ T _ { 2 , \beta _ { n } } & = \frac { ( n ) _ { k } } { k ! } \int _ { 0 } ^ { \infty } \int _ { \text {dom} } E [ P _ { s } h ( \xi ( \beta _ { n - k } ) + \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \beta _ { n - k } ) ) \\ & = - \frac { ( n ) _ { k } } { k ! } \int _ { 0 } ^ { \infty } \int _ { \text {dom} } E [ P _ { s } h ( \xi ( \beta _ { n - k } ) + \delta _ { f } ( x _ { 1 } , \dots , x _ { k } , \beta _ { n - k } ) + \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) ] \, K _ { 1 } ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \, d s \\ & + \frac { ( n ) _ { k } } { k ! } \int _ { 0 } ^ { \infty } \int _ { \text {dom} } E [ P _ { s } h ( \xi ( \beta _ { n - k } ) + \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \beta _ { n - k } ) ) - P _ { s } h ( \xi ( \beta _ { n - k } ) ) \\ & + P _ { s } h ( \xi ( \beta _ { n - k } ) + \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) \\ & = \hat { T } _ { 2 , \beta _ { n } } + R _ { \beta _ { n } } \, . \\ \text {Together with } ( 6 . 4 ) \text { and the formulas for } L \text { in } ( 3 . 1 ) \text { and } ( 3 . 2 ) , \text { we see that }$$

Together with (6.4) and the formulas for L in (3.1) and (3.2), we see that

$$E h ( \zeta ) - E h ( \xi ( \eta ) ) = \int _ { 0 } ^ { \infty } \int _ { \mathbb { Y } } \mathbf E [ D _ { y } P _ { s } h ( \xi ( \eta ) ) ] \, \left ( \mathbf M - \mathbf L \right ) ( \mathbf d y ) \, \mathrm d s + R _ { \eta }$$

and

$$\text {E} h ( \zeta ) - \text {E} h ( \xi ( \beta _ { n } ) ) & = \int _ { 0 } ^ { \infty } \int _ { Y } \text {E} [ D _ { y } P _ { s } h ( \xi ( \beta _ { n } ) ) ] \left ( \text {M} - \text {L} \right ) ( \text {d} y ) \, \text {ds} \\ & \quad + \int _ { 0 } ^ { \infty } \int _ { Y } \text {E} [ D _ { y } P _ { s } h ( \xi ( \beta _ { n } ) ) ] - \text {E} [ D _ { y } P _ { s } h ( \xi ( \beta _ { n - k } ) ) ] \left \lfloor \text {d} y \right \rfloor \, \text {ds} + R _ { \beta _ { n } } \, .$$

We now determine the remainder terms Rη and Rβn. For (x1, . . .,xk) ∈ dom f let us define hx,..xk : NY → R by

$$\widetilde { h } _ { x _ { 1 } , \dots , x _ { k } } ( \mu ) = \frac { 1 } { 2 } \left ( h ( \mu ) - h ( \mu + \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) \right ) \, .$$

We can then re-write Rη and Rβn as

$$R _ { \eta } = \frac { 2 } { k ! } \int _ { 0 } ^ { \infty } \int _ { \text {dom} \ f } E [ P _ { s } \widetilde { h } _ { x _ { 1 } , \dots , x _ { k } } ( \xi ( \eta ) + \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \eta ) ) - P _ { s } \widetilde { h } _ { x _ { 1 } , \dots , x _ { k } } ( \xi ( \eta ) ) ] \ K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \, d s$$

and

$$R _ { \beta _ { n } } = \frac { 2 ( n ) _ { k } } { k ! } \int _ { 0 } ^ { \infty } \int _ { d \text {om} } E [ P _ { s } \widetilde { h } _ { x _ { 1 } , \dots , x _ { k } } ( \xi ( \beta _ { n - k } ) + \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \beta _ { n - k } ) ) \\ & - P _ { s } \widetilde { h } _ { x _ { 1 } , \dots , x _ { k } } ( \xi ( \beta _ { n - k } ) ) ] \, \mathbf K _ { 1 } ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \, d s \, .$$


<!-- p:19 -->


Because of ħx1,..xk ∈ L1, we obtain by the definition of the semi-group (Ps)s≥0 in (5.2) and Lemma 5.2 that

$$| R _ { \eta } | & \leq \frac { 2 } { k ! } \int _ { 0 } ^ { \infty } \int _ { d o m \, f } e ^ { - s } \, \mathbf E \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \eta ) ( \mathbb { Y } ) \, K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \, d s \\ & = \frac { 2 } { k ! } \int _ { d o m \, f } \mathbf E \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \eta ) ( \mathbb { Y } ) \, K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) )$$

pp

$$| R _ { \beta _ { n } } | & \leq \frac { 2 ( n ) _ { k } } { k ! } \int _ { 0 } ^ { \infty } \int _ { d \text { dom } f } e ^ { - s } \, \mathbf E \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \beta _ { n - k } ) ( \mathbb { Y } ) \, K _ { 1 } ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \, d s \\ & \leq \frac { 2 ( n ) _ { k } } { k ! } \int _ { d \text { dom } f } E \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \beta _ { n - k } ) ( \mathbb { Y } ) \, K _ { 1 } ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \, .$$

Now, from the Mecke formula (2.1) and its analogue (2.2) for binomial processes it follows that

$$E \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \eta ) ( \Upsilon ) & = E \sum _ { \emptyset \neq I \subseteq [ k ] , \, z \in \eta _ { z } ^ { k - | I | } } \frac { 1 } { ( k - | I | ) ! } \, 1 ( f ( x _ { I } , z ) \in \dim f ) \\ & = \sum _ { \emptyset \neq I \subseteq [ k ] } \frac { 1 } { ( k - | I | ) ! } \int _ { \mathbb { X } ^ { k - | I | } } 1 ( ( x _ { I } , z ) \in \dim f ) \, K ^ { k - | I | } ( d z )$$

pup

$$\text { and } & & E \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \beta _ { n - k } ) ( \mathbb { Y } ) = E \sum _ { \emptyset \in I \subseteq [ k ] , \, z \in \beta ^ { k - | I | } _ { n - k , \# } } \frac { 1 } { ( \frac { 1 } { k - | I | ) ! } \, 1 ( f ( x _ { 1 } , z ) \in \text {dom} \, f ) \\ & & = \sum _ { 0 \not \in I \subseteq [ k ] } \frac { ( n - k ) _ { k - | I | } } { ( k - | I | ) ! } \int _ { X ^ { k - | I | } } 1 ( ( x _ { I } , z ) \in \text {dom} \, f ) \, K _ { 1 } ^ { k - | I | } ( d z ) .$$

Together with Lemma 6.1, we obtain

$$| R _ { \eta } | & \leq \frac { 2 } { k ! } \int _ { \mathbb { X } ^ { k } } \sum _ { 0 \neq I \subseteq [ k ] } \frac { 1 } { ( k - | I | ) ! } \int _ { \mathbb { X } ^ { k - | I | } } 1 ( ( x _ { 1 } , \dots , x _ { k } ) \in \text {dom} \, f ) \\ & = 2 ( E \xi ( \mathbb { Y } ) ^ { 2 } - L ( \mathbb { Y } ) - L ( \mathbb { Y } ) ^ { 2 } ) = 2 ( E \xi ( \mathbb { Y } ) ^ { 2 } - E \xi ( \mathbb { Y } ) - ( E \xi ( \mathbb { Y } ) ) ^ { 2 } )$$

and

$$\text { and } & & | R _ { \beta _ { n } } | \leq \frac { 2 } { k ! } \int _ { \mathbb { X } ^ { k } } \sum _ { \emptyset \leq I \subseteq [ k ] } \frac { ( n ) _ { k } ( n - k ) _ { k - | I | } } { ( k - | I | ) ! } \int _ { \mathbb { X } ^ { k - | I | } } 1 ( ( x _ { 1 } , \dots , x _ { k } ) \in \text { dom } f ) \\ & & \quad \times 1 ( ( ( x _ { r } , z ) \in \text { dom } f ) K _ { 1 } ^ { k - | I | } ( d z ) K _ { 1 } ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \\ & = 2 ( \mathbb { E } ( \mathbb { Y } ) ^ { 2 } - L ( \mathbb { Y } ) - \frac { ( n - k ) _ { k } } { ( n ) _ { k } } L ( \mathbb { Y } ) ^ { 2 } ) = 2 ( \mathbb { E } ( \mathbb { Y } ) ^ { 2 } - \mathbb { E } ( \mathbb { Y } ) - \frac { ( n - k ) _ { k } } { ( n ) _ { k } } ( \mathbb { E } \xi ( \mathbb { Y } ) ) ^ { 2 } ) \, . \\ \intertext { The inequalities in ( 6 . 6 ) and ( 6 . 7 ) together with the definition of r ( \text { dom } f ) \, \text { imply that} }$$

The inequalities in (6.6) and (6.7) together with the definition of r(dom f) imply that

$$| R _ { \eta } | \leq \frac { 2 ^ { k + 1 } } { k ! } r ( \text {dom} \, f ) \quad \text {and} \quad | R _ { \beta _ { n } } | \leq \frac { 2 ^ { k + 1 } } { k ! } r ( \text {dom} \, f ) \, .$$

It follows from Lemma 5.2 that, for s ≥ 0,

$$| \mathbf E D _ { y } P _ { s } h ( \xi ( \mu ) ) | \leq \mathbf E [ \, | P _ { s } h ( \xi ( \mu ) + \delta _ { y } ) - P _ { s } h ( \xi ( \mu ) ) | \leq e ^ { - s } \, .$$


<!-- p:20 -->


For y1, y2 ∈ Y and ξ ∈ NY we have dTv(ξ + δy1, ξ + δy2) ≤ 1 so that h ∈ L1 leads to

$$| D _ { y _ { 1 } } h ( \tilde { \xi } ) - D _ { y _ { 2 } } h ( \tilde { \xi } ) | = | h ( \tilde { \xi } + \delta _ { y _ { 1 } } ) - h ( \tilde { \xi } + \delta _ { y _ { 2 } } ) | \leq 1 \, .$$

Together with Lemma 5.1, we obtain that

$$| E D _ { y _ { 1 } } P _ { s } h ( \xi ( \mu ) ) - E D _ { y _ { 2 } } P _ { s } h ( \xi ( \mu ) ) | = e ^ { - s } | E P _ { s } ( D _ { y _ { 1 } } h - D _ { y _ { 2 } } h ) ( \xi ( \mu ) ) | \leq e ^ { - s }$$

for all y1, y2 ∈ Y and s ≥ 0. The estimates in (6.9) and (6.10) show that

$$\left | \int _ { 0 } ^ { \infty } \int _ { \mathbb { Y } } \mathbf E \left [ D _ { y } P _ { s } h ( \xi ( \mu ) ) \right ] ( \mathbf M - \mathbf L ) ( d y ) \, d s \right | \leq d _ { T V } ( \mathbf M , \mathbf L ) \int _ { 0 } ^ { \infty } e ^ { - s } \, d s \leq d _ { T V } ( \mathbf M , \mathbf L ) \, .$$

Combining (6.6) and (6.8) with (6.11) completes the proof of the Poisson case.

When considering a binomial process, we additionally need to take care of the term

$$\int _ { 0 } ^ { \infty } \int _ { \mathbb { W } } \mathbf E \left [ D _ { y } P _ { s } h ( \xi ( \beta _ { n } ) ) \right ] - \mathbf E \left [ D _ { y } P _ { s } h ( \xi ( \beta _ { n - k } ) ) \right ] \text {L} ( d y ) \, d s \, .$$

For this, we use Lemma 5.1, the fact that Dyh ∈ L1 whenever h ∈ L1 and Lemma 5.2 to obtain that

$$\text {that} \\ & \quad | \mathbf E [ D _ { y } P _ { s } h ( \xi ( \beta _ { n } ) ) ] - \mathbf E [ D _ { y } P _ { s } h ( \xi ( \beta _ { n - k } ) ) ] \, | \\ & \leq \int _ { \mathbb { X } ^ { k } } | \mathbf E [ D _ { y } P _ { s } h ( \xi ( \beta _ { n - k } + \delta _ { x _ { 1 } } + \dots + \delta _ { x _ { k } } ) ) ] - \mathbf E [ D _ { y } P _ { s } h ( \xi ( \beta _ { n - k } ) ) ] \, | \, K _ { 1 } ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \\ & \quad - \int _ { \mathbb { X } ^ { k } } e ^ { - s } | \mathbf E [ P _ { s } ( D _ { y } h ) ( \xi ( \beta _ { n - k } ) + \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \beta _ { n - k } ) + \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) - P _ { s } ( D _ { y } h ) ( \xi ( \beta _ { n - k } ) ) ] | \\ & \leq \frac { 1 } { n ^ { k } } \int _ { \mathbb { X } ^ { k } } 2 e ^ { - 2 s } \left ( E \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \beta _ { n - k } ) ( \Psi ) + 1 ( ( x _ { 1 } , \dots , x _ { k } ) \in \text {dom} \, f ) \right ) K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \\ \intertext { \text {for any } s > 0 . \text { It follows from } ( 6 . 5 ) \text { and } ( n - k ) _ { k - 1 } | _ { l } < n ^ { k - | l | } \text { that} }$$

o0t |1|−  ||−( − )  () os   0  s  t

$$for any s \geq 0. \, It follows from \, ( 6 . 5 ) \, and \, ( n - k ) _ { k - | I | } \leq n ^ { k - | I | } \, \text { that} \\ \frac { 1 } { n ^ { k } } \int _ { \mathbb { X } ^ { k } } \mathbf E \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \beta _ { n - k } ) ( \mathbb { Y } ) \, \mathbf K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \\ \leq \frac { 1 } { n ^ { k } } \int _ { \mathbb { X } ^ { k } } \sum _ { \emptyset \in \mathbb { J } [ \mathcal { S } ] } \frac { 1 } { ( k - | I | ) ! } \int _ { \mathbb { X } ^ { k - | I | } } 1 ( ( x _ { 1 } , z ) \in \text { dom } f ) \, \mathbf K ^ { k - | I | } ( d z ) \, \mathbf K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \\ = \frac { 1 } { n ^ { k } } \sum _ { 0 \not = I \subset [ k ] } \frac { 1 } { ( k - | I | ) ! } \int _ { \mathbb { X } ^ { k } } 1 ( ( x _ { 1 } , \dots , x _ { k } ) \in \text { dom } f ) \, \mathbf K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \, \mathbf K ( \mathbb { X } ) ^ { | k | - | I | } \\ \leq \frac { ( 2 ^ { k } - 2 ) } { n } \int _ { \mathbb { X } ^ { k } } 1 ( ( x _ { 1 } , \dots , x _ { k } ) \in \text { dom } f ) \, \mathbf K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) . \\ \text { Now } ( 3 . 2 ) \, \text { implies that}$$

Now (3.2) implies that

$$\int _ { \mathbb { K } ^ { k } } 1 ( ( x _ { 1 } , \dots , x _ { k } ) \in \text {dom} \, f ) \, \mathbf K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) = \frac { k ! \, n ^ { k } } { ( n ) _ { k } } \text {L} ( \mathbb { Y } ) \leq k ! e ^ { k } \text {e} ( \mathbb { Y } ) \, ,$$

where we have used that nk/(n)k ≤ kk/k! ≤ ek for n ≥ k. Hence, using that 2kek ≤ 6k, we find

$$\int _ { 0 } ^ { \infty } \int _ { \mathbb { Y } } | \mathbf E [ D _ { y } P _ { s } h ( \xi ( \beta _ { n } ) ) ] - \mathbf E [ D _ { y } P _ { s } h ( \xi ( \beta _ { n - k } ) ) ] | \, \text {L} ( d y ) \, d s \leq 6 ^ { k } k ! \, \frac { \text {L} ( \mathbb { Y } ) ^ { 2 } } { n } = 6 ^ { k } k ! \, \frac { ( \mathbf E \xi ( \mathbb { Y } ) ) ^ { 2 } } { n } \, .$$

Together with (6.7), (6.8) and (6.11) this concludes the proof in the binomial case.


<!-- p:21 -->


Remark 6.2. Bounds for the total variation distance between ξ and ζ that are similar to the bounds for the Rubinstein distance in Theorem 3.1 can be also deduced from Theorem 2.6 in [4]. This result implies that

$$d _ { T V } ( \xi ( \eta ) , \zeta ) & \leq 2 d _ { T V } ( L , M ) \\ & + \frac { 2 } { k ! } \int _ { d o m \, f } \text {Ed} _ { T V } ( \xi ( \eta ) , \xi ( \eta + \delta _ { x _ { 1 } } + \dots + \delta _ { x _ { k } } ) - \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) \, K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \\$$

and

$$\text {d} _ { \text {TV} } ( \xi ( \beta _ { n } ) , \zeta ) & \leq 2 d _ { \text {TV} } ( L , M ) \\ & + \frac { 2 ( n ) _ { k } } { k ! } \int _ { \text {dom} } E d _ { \text {TV} } ( \xi ( \beta _ { n } ) , \xi ( \beta _ { n - k } + \delta _ { x _ { 1 } } + \dots + \delta _ { x _ { k } } ) - \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) \, K _ { 1 } ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \, .$$

Since the integrands are bounded by

$$\mathbf E \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \eta ) ( \mathbb { Y } ) \quad \text {and} \quad \mathbf E \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \beta _ { n - k } ) ( \mathbb { Y } ) + \mathbf E d _ { T V } ( \xi ( \beta _ { n } ) , \xi ( \beta _ { n - k } ) ) \, ,$$

respectively, the integrals on the right-hand sides can be controlled as in the proof of Theorem 3.1 above.

## 7 Applications

### 7.1 Poisson approximation of U-statistics

In this subsection we present a first application of Theorem 3.1 to U-statistics of Poisson or binomial processes. Let (X, χ) and (Y, ) be two lcscH spaces and let for some fixed integer k ≥ 1, ft : Xk → Y, t ≥ 1, be symmetric measurable functions. Furthermore, for a σ-finite measure K and a probability measure K1 on X we denote by ηt a Poisson process with intensity measure Kt := tK, t ≥ 1, and by βt, t ≥ 1, a binomial process of [t] points with intensity measure Kt := [t]K1, respectively. If μt is either ηt or βt and if B is a measurable subset of Y, we define the U-statistics

$$S _ { t } ( B ) \coloneqq \frac { 1 } { k ! } \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { t , \neq } ^ { k } } 1 ( f _ { t } ( x _ { 1 } , \dots , x _ { k } ) \in B ) \, , \quad t \geq 1 \, ,$$

which count the number of k-tuples (x, . . , xk) ∈ μk,≠ for which ft(x1, . . . ,xk) ∈ B. To compare St(B) with a Poisson random variable we define

$$r _ { t } ( B ) \colon = \max _ { 1 \leq \ell \leq k - 1 } \int _ { \mathbb { X } ^ { \ell } } \left ( \int _ { \mathbb { X } ^ { k - \ell } } \mathbf 1 ( f _ { t } ( x _ { 1 } , \dots , x _ { k } ) \in B ) \mathbf K _ { t } ^ { k - \ell } ( \mathbf d ( x _ { \ell + 1 } , \dots , x _ { k } ) ) \right ) ^ { 2 } \mathbf K _ { t } ^ { \ell } ( \mathbf d ( x _ { 1 } , \dots , x _ { \ell } ) )$$

if k &gt; 1 and rt(B) := 0 if k = 1.

Theorem 7.1. Let B ∈  and let Z be a Poisson distributed random variable with mean λ ∈ [0, ∞). Suppose that ESt(B)2 &lt; ∞. If St(B) is induced by a Poisson process ηt with t ≥ 1, then

$$d _ { W } ( S _ { t } ( B ) , Z ) & \leq | E S _ { t } ( B ) - \lambda | + 2 ( E S _ { t } ( B ) ^ { 2 } - E S _ { t } ( B ) - ( E S _ { t } ( B ) ) ^ { 2 } ) \\ & \leq | E S _ { t } ( B ) - \lambda | + \frac { 2 ^ { k + 1 } } { k ! } \, r _ { t } ( B ) \, .$$

If St(B) is induced by a binomial process βt with t ≥ 1, then

$$\mathbf d w ( S _ { t } ( B ) , Z ) & \leq | \mathbf E S _ { t } ( B ) - \lambda | + 2 \left ( \mathbf E S _ { t } ( B ) ^ { 2 } - \mathbf E S _ { t } ( B ) - \frac { ( \lceil t \rceil - k ) _ { k } } { ( \lceil t \rceil ) _ { k } } ( \mathbf E S _ { t } ( B ) ) ^ { 2 } \right ) + \frac { 6 ^ { k } k ! } { t } \left ( \mathbf E S _ { t } ( B ) \right ) ^ { 2 } \\ & \leq | \mathbf E S _ { t } ( B ) - \lambda | + \frac { 2 ^ { k + 1 } } { k ! } \ r t _ { t } ( B ) + \frac { 6 ^ { k } k ! } { t } \left ( \mathbf E S _ { t } ( B ) \right ) ^ { 2 } .$$


<!-- p:22 -->


Proof. We define the point processes

$$\xi _ { t } \coloneqq \frac { 1 } { k ! } \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { t , \neq } ^ { k } } \delta _ { f _ { t } ( x _ { 1 } , \dots , x _ { k } ) } \, , \quad t \geq 1 \, .$$

and denote their intensity measures by Lt, t ≥ 1. By construction, St(B) and ξt(B) follow the same distribution. We notice that for any fixed h ∈ Lip(1) (recall that these are all h : R → R whose Lipschitz constant is at most one) and B ∈  the mapping ω → h(ω(B)) from NY to R satisfies

$$| h ( \omega _ { 1 } ( B ) ) - h ( \omega _ { 2 } ( B ) ) | \leq | \omega _ { 1 } ( B ) - \omega _ { 2 } ( B ) | \leq d _ { T V } ( \omega _ { 1 } , \omega _ { 2 } ) , \quad \omega _ { 1 } , \omega _ { 2 } \in N _ { \mathbb { Y } } \, ,$$

and, thus, belongs to L1. Consequently, if ζt is a Poisson process on Y with intensity measure Lt, the definitions of the Wasserstein distance and of the Rubinstein distance yield

$$d w ( S _ { t } ( B ) , \zeta _ { t } ( B ) ) & = d w ( \xi _ { t } ( B ) , \zeta _ { t } ( B ) ) = \sup _ { h \in \text {Lip} ( 1 ) } | \text {E} h ( \xi _ { t } ( B ) ) - \text {E} h ( \zeta _ { t } ( B ) ) | \\ & \leq \sup _ { g \in \mathcal { L } _ { 1 } } \left | \text {E} g ( \xi _ { t } | B ) - \text {E} g ( \zeta _ { t } | B ) \right | = d r ( \xi _ { t } | B , \zeta _ { t } | B ) \, .$$

Now Theorem 3.1 and the observation that Lt(B) = ESt(B) imply the result for the choice λ = ESt(B). The general case follows from the triangle inequality for the Wasserstein distance and the fact that the Wasserstein distance between a Poisson random variable with mean ESt(B) and another Poisson random variable with mean λ is bounded by |ESt(B) − λ|. □

We emphasize that Theorem 7.1 deals with Poisson approximation in Wasserstein distance. As already stated in (2.4), this is stronger than approximation in total variation distance, which is usually considered in the literature (see [10] for the only exception we are aware of). This is possible thanks to our functional limit Theorem 3.1, which deals with the Rubinstein distance rather than the total variation distance for point processes.

The Poisson approximation in total variation distance of U-statistics over binomial input was considered in [7]. If we assume that ESt(B) = λ for t ≥ 1 for the binomial case in Theorem 7.1, we obtain up to a constant, which may depend on λ, the same bound as in [7, Theorem 2] for the total variation distance.

In [31], an abstract bound for the Poisson approximation of Poisson functionals (i.e., random variables depending on a Poisson process) is derived, which is also applicable to U-statistics over Poisson input. Our Theorem 7.1 yields better rates of convergence for this special class of Poisson functionals. In fact, the bound in [41, Proposition 4.1], which is derived from [31], involves the square root of t(B) (see Remark 3.4 (iii)), while in the bound for the Poisson case in Theorem 7.1 only τt(B) enters.

To illustrate the use of Theorem 7.1 let us consider a particular example, which will recur also in the following subsections. Let K ⊂ Rd (d ≥ 1) be a compact convex set with volume one. For t ≥ 1 let ηt be a homogeneous Poisson process in K of intensity t ≥ 1 and denote by βt a binomial process in K with [t] points distributed according to the uniform distribution on K. For a family (θt)t≥1 of positive real numbers let us construct the random geometric graph with vertex set μt, where μt is ηt or βt, by drawing an edge between two distinct vertices y1 and y2 whenever their Euclidean distance ∥y1 − y2∥ is bounded by θt. These random graphs are the natural geometric counterparts to the classical Erdös-Rényi models for combinatorial random graphs. For background material we refer the reader to the monograph [33] and also to the recent paper [36] as well as the references cited therein.

For the random geometric graph introduced above let Et be the number of edges. Note that Et is a U-statistic of the form

$$E _ { t } = \frac { 1 } { 2 } \sum _ { ( y _ { 1 } , y _ { 2 } ) \in \mu _ { t , \neq } ^ { 2 } } 1 ( \| y _ { 1 } - y _ { 2 } \| \leq \theta _ { t } ) \, . \\$$

The multivariate Mecke formula (2.1) and a computation using spherical coordinates show that Et has expectation t2(κdθd + O(θd+1))/2 in the Poisson case, as θt → 0. For an underlying binomial process the expected number of edges is [t]([t] − 1)(κdθd + O(θd+1))/2, as θt → 0. If the expectation of Et converges to a constant, as t → ∞, Et can be well approximated by a Poisson random variable. In contrast to [31, Theorem 5.1], whose proof involves various non-trivial computations, we can deduce a corresponding approximation result from Theorem 7.1, the proof is postponed to Subsection 7.4.


<!-- p:23 -->


Corollary 7.2. Assume that lim t2θt = λ ∈ [0, ∞) and let Z be a Poisson distributed random variable ∞←7 with mean κdλ/2. Then there is a constant c &gt; 0 only depending on the space dimension d, the set K and supt≥1 t2θt such that

$$d _ { W } ( E _ { t } , Z ) \leq c \left ( | t ^ { 2 } \theta _ { t } ^ { d } - \lambda | + t ^ { - \min \{ 2 / d , 1 \} } \right ) , \quad t \geq 1 \, .$$

Remark 7.3. As mentioned before, Corollary 7.2 extends the results for the random geometric graph from [31] not only to a stronger distance and to a binomial point process, but also improves the at    r o  od }   ooss ods dr o  der |t2θd − λ| + t−1 (for the Wasserstein distance), while Theorem 5.1 in [31] delivers an upper bound of order |t2θd − λ| + t−1/2 (for the total variation distance).

### 7.2 Compound Poisson approximation of U-statistics

As in the previous subsection, we denote by μt, t ≥ 1, a Poisson process ηt or a binomial process βt on a lcscH space X. For k ∈ N and measurable functions ht : Xk → R, t ≥ 1, we consider the family of U-statistics

$$S _ { t } \colon = \frac { 1 } { k ! }$$

of generality that ht is symmetric for any t ≥ 1. For a fixed constant γ ∈ R and t ≥ 1, we define

$$L _ { t } ( A ) \colon = \frac { 1 } { k ! } E \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { t , \neq } ^ { k } } 1 ( h _ { t } \langle \frac { x _ { 1 } } { x _ { t , \neq } } \rangle$$

and

$$r _ { t } \coloneqq \max _ { 1 \leq \ell \leq k - 1 } \int _ { \mathbb { X } ^ { \ell } } \left ( \int _ { \mathbb { X } ^ { k - \ell } } 1 ( h _ { t } ( x _ { 1 } , \dots , x _ { k } ) \neq 0 ) \, K _ { t } ^ { k - \ell } ( d ( x _ { \ell + 1 } , \dots , x _ { k } ) ) \right ) ^ { 2 } K _ { t } ^ { \ell } ( d ( x _ { 1 } , \dots , x _ { \ell } ) )$$

for k &gt; 1, and put rt := 0 if k = 1. The following result compares the U-statistic St with a compound Poisson random variable. Most of the previous literature is based on a direct use of Stein's method, poeo o s e te t  oo o o o o and also needs in general certain monotonicity assumptions. Moreover, there are situations in which the solution of the so-called Stein equation cannot be controlled appropriately, and hence in which Stein's method is of little use, see [9]. Being a consequence of the functional limit theorem (Theorem 3.1), our approach circumvents such technicalities and also allows us to deal with compound Poisson random variables having a discrete or continuous distribution.

Theorem 7.4. Let ζ be a Poisson process on R with a finite intensity measure M, let Z := Σx∈ζ x and let γ ∈ R. Then

$$d _ { T V } ( t ^ { \gamma } S _ { t } , Z ) & \leq d _ { T V } ( L _ { t } , M ) + \frac { 2 ^ { k + 1 } } { k ! } r _ { t } \, , \quad t \geq 1 \, , \\$$

if in the definition of St a Poisson process ηt is used, and

$$d _ { T V } ( t ^ { \gamma } S _ { t } , Z ) \leq d _ { T V } ( L _ { t } , M ) + \frac { 2 ^ { k + 1 } } { k ! } r _ { t } + \frac { 6 ^ { k } k ! } { t } \, L _ { t } ( \mathbb { R } ) ^ { 2 } \, , \quad t \geq 1 \, ,$$

if the underlying point process is a binomial process βt.


<!-- p:24 -->


Proof. We consider the point processes

$$t ^ { \gamma } \bullet \xi _ { t } \coloneqq \frac { 1 } { k ! } \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { t , \neq } ^ { k } } 1 ( h _ { t } ( x _ { 1 } , \dots , x _ { k } ) \neq 0 ) \, \delta _ { t ^ { \gamma } h _ { t } ( x _ { 1 } , \dots , x _ { k } ) } \, , \ \ t \geq 1 \, .$$

It follows from the definitions of the total variation and the Rubinstein distance that

$$d _ { T V } ( t ^ { \gamma } S _ { t } , Z ) = \sup _ { A \in \mathcal { B } ( \mathbb { R } ) } \left | E 1 \left ( \sum _ { x \in t ^ { \gamma } \bullet \xi _ { t } } x \in A \right ) - E 1 \left ( \sum _ { x \in \zeta } x \in A \right ) \right | \leq d _ { R } ( t ^ { \gamma } \bullet \xi _ { t } , \zeta )$$

since the maps ω → 1(Σx∈ω x ∈ A) belong to L1. Now Corollary 3.3 with B = R implies that

$$d _ { R } ( t ^ { \gamma } \bullet \xi _ { t } , \zeta ) \leq d _ { T V } ( L _ { t } , M ) + \frac { 2 ^ { k + 1 } } { k ! } r _ { t } \, , \quad t \geq 1 \, ,$$

$$d _ { R } ( t ^ { \gamma } \bullet \xi _ { t } , \zeta ) \leq d _ { T V } ( L _ { t } , \mathbf M ) + \frac { 2 ^ { k + 1 } } { k ! } r _ { t } + \frac { 6 ^ { k } k ! } { t } \, \mathbf L _ { t } ( \mathbb { R } ) ^ { 2 } \, , \quad t \geq 1 \, , \\$$

and

for the Poisson and the binomial case, respectively. This concludes the proof.

□

where N is a Poisson distributed random variable and (Xi)i∈N is a sequence of independent and identically distributed random variables such that N and (Xi)i∈N are independent. However, the representation of Z in terms of the Poisson process ζ fits better into our general framework.

For the compound-Poisson approximation of U-statistics in the binomial case a similar bound as n  t   t  eed e  ot  o       n the non-negative integers, whereas we do not need to impose such a condition. In addition, we are not aware of any analogous result for an underlying Poisson process.

As an application of Theorem 7.4 we consider general edge-length functionals of the random geometric graph introduced in the course of the previous subsection. Fix a parameter b ∈ R and define

$$L _ { t } ^ { ( b ) } \colon = \frac { 1 } { 2 } \sum _ { ( x _ { 1 } , x _ { 2 } ) \in \mu _ { t , \neq } ^ { 2 } } 1 ( \text {dist} ( x _ { 1 } , x _ { 2 } ) \leq \theta _ { t } ) \text { dist} ( x _ { 1 } , x _ { 2 } ) ^ { b } \, , \quad t \geq 1 \, ,$$

7.1, we consider the situation that the distance parameters (θt)t≥1 are chosen in such a way that the expected number of edges converges to a constant, as t → ∞. Recall that in Corollary 7.2 the number of edges L) hs been approximated in this case by a Poisson random variable. For general exponents is postponed to Subsection 7.4 below.

Corollary 7.6. Fix b ∈ R and assume that lim t2θd = λ ∈ [0, ∞). Define Z := Σi=1 ∥Xib, where N t→∞ is a Poisson distributed random variable with mean κdλ/2 and (Xi)i∈N are independent and uniformly distributed points in Bd(λ1/d), which are independent of N. Then, there is a constant c &gt; 0 only depending on the space dimension d, the set K and supt≥1t2θd such that

$$d _ { \text {TV} } ( t ^ { 2 b / d } L _ { t } ^ { ( b ) } , Z ) \leq c \left ( | t ^ { 2 } \theta _ { t } ^ { d } - \lambda | + t ^ { - \min \{ 2 / d , 1 \} } \right ) , \quad t \geq 1 \, .$$

Remark 7.7. Corollary 7.6 without a rate of convergence has been derived in [36, Theorem 3.5] by combining a point process convergence result with the continuous mapping theorem. Thanks to Theorem 7.4 we were able to add a rate of convergence for the total variation distance.


<!-- p:25 -->


### 7.3 Approximation of U-statistics by α-stable random variables

Let us denote by μt, t ≥ 1, a Poisson process ηt or a binomial process βt as in the previous subsections. For fixed k ∈ N and measurable functions ht : Xk → R, t ≥ 1, let

$$S _ { t } \coloneqq \frac { 1 } { k ! } \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { t , \neq } ^ { k } } h _ { t } ( x _ { 1 } , \dots , x _ { k } ) \, , \quad t \geq 1 \, .$$

Here, we can and will assume without loss of generality that ht is symmetric for any t ≥ 1. We are interested in the limiting behaviour of these U-statistics in situations, where their summands are heavy tailed, and approximate St by an α-stable random variable Z. Recall that this means that for any n ∈ N there are independent copies Z1, ..., Zn of Z satisfying the distributional equality n−1/α(Z1 + . . . + Zn)  Z. We fix α ∈ (0, 1) and γ ∈ R and apply our functional limit theorem to the point processes

$$t ^ { \gamma } \bullet \xi _ { t } \coloneqq \frac { 1 } { k ! } \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { t , \neq } ^ { k } } 1 ( h _ { t } ( x _ { 1 } , \dots , x _ { k } ) \neq 0 ) \, \delta _ { \text {sign} ( h _ { t } ( x _ { 1 } , \dots , x _ { k } ) ) } t ^ { \gamma } | h _ { t } ( x _ { 1 } , \dots , x _ { k } ) | ^ { - \alpha } \, , \quad t \geq 1 \, ,$$

on R, where sign(a) = 1(a ≥ 0) − 1(a &lt; 0). If μt is a binomial process, the convergence of the U-statistic St to an α-stable random variable has been considered in [17] without giving rates of convergence. Thanks to our quantitative bound for the Rubinstein distance in Theorem 3.1 we are in the position to add a rate of convergence for the Kolmogorov distance. The statement of our result is prepared by introducing some notation. For A ∈ B(R) and t ≥ 1 we define

$$L _ { t } ( A ) & \colon = \frac { 1 } { k ! } E \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { t , \neq } ^ { k } } 1 ( h _ { t } ( x _ { 1 } , \dots , x _ { k } ) \neq 0 ) \, 1 ( \text {sign} ( h _ { t } ( x _ { 1 } , \dots , x _ { k } ) ) \, | h _ { t } ( x _ { 1 } , \dots , x _ { k } ) | ^ { - \alpha } \in t ^ { - \gamma } A ) \, , \\$$

which is the intensity measure of tγ · ξt, and

$$r _ { t } ( A ) \coloneqq \max _ { 1 \leq \ell \leq k - 1 } \int _ { \mathbb { X } ^ { \ell } } \left ( \int _ { \mathbb { X } ^ { k - \ell } } 1 ( h _ { t } ( x _ { 1 } , \dots , x _ { k } ) \neq 0 ) \, 1 ( \text {sign} ( h _ { t } ( x _ { 1 } , \dots , x _ { k } ) ) \, | h _ { t } ( x _ { 1 } , \dots , x _ { k } ) | ^ { - \alpha } \in t ^ { - \gamma } A ) \\ \\ K _ { t } ^ { k - \ell } ( d ( x _ { \ell + 1 } , \dots , x _ { k } ) ) \right ) ^ { 2 } K _ { t } ^ { \ell } ( d ( x _ { 1 } , \dots , x _ { \ell } ) )$$

if k ≥ 2 and rt(A) := 0 if k = 1. The following result contains a quantitative bound for the approximation of U-statistics by an α-stable random variable with α ∈ (0, 1).

Theorem 7.8. Let α ∈ (0, 1) and let M be either the Lebesgue measure on R and or its restriction to R+. Define Z := Σx∈ζ sign(x) |x|−1/α, where ζ is a Poisson process with intensity measure M. Assume that there are a constant γ ∈ R and functions g1, g2, g3 : R2 → R+ such that, for any a &gt; 0 and t ≥ 1,

$$d _ { T V } ( L _ { t } | _ { [ - a , a ] } , M | _ { [ - a , a ] } ) \leq g _ { 1 } ( a , t ) \, , \quad r _ { t } ( [ - a , a ] ) \leq g _ { 2 } ( a , t )$$

and

$$\frac { t ^ { - \gamma / \alpha } } { k ! } E \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { t , \neq } ^ { k } } 1 ( | h _ { t } ( x _ { 1 } , \dots , x _ { k } ) | < t ^ { \gamma / \alpha } a ^ { - 1 / \alpha } ) \, | h _ { t } ( x _ { 1 } , \dots , x _ { k } ) | \leq g _ { 3 } ( a , t ) \, .$$

Then there is a constant C &gt; 0 only depending on α and k such that

$$d _ { K } ( t ^ { - \gamma / \alpha } S _ { t } , Z ) \leq C g ( t ) \, , \ \ t \geq 1 \, ,$$

$$g ( t ) \colon = \begin{cases} \inf _ { a > 0 } \max \{ a ^ { 1 / 2 - 1 / ( 2 \alpha ) } , g _ { 1 } ( a , t ) , g _ { 2 } ( a , t ) , \sqrt { g _ { 3 } ( a , t ) } \} & \colon \mu _ { t } = \eta _ { t } \\ \inf _ { a > 0 } \max \{ a ^ { 1 / 2 - 1 / ( 2 \alpha ) } , g _ { 1 } ( a , t ) , g _ { 2 } ( a , t ) , \sqrt { g _ { 3 } ( a , t ) } , a ^ { 2 } / t \} & \colon \mu _ { t } = \beta _ { t } \, . \end{cases}$$

where Proof. For a &gt; 0 we define the random variables


<!-- p:26 -->


$$S _ { t , a } \colon = \frac { 1 } { k ! } \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { t , \neq } ^ { k } } 1 ( | h _ { t } ( x _ { 1 } , \dots , x _ { k } ) | \geq t ^ { \gamma / \alpha } a ^ { - 1 / \alpha } ) \, h _ { t } ( x _ { 1 } , \dots , x _ { k } ) \, , \ \ t \geq 1 \, ,$$

and

$$Z _ { a } \colon = & \sum _ { x \in \zeta } 1 ( | x | \leq a ) \, \text { sign} ( x ) \, | x | ^ { - 1 / \alpha } \, . \\$$

Then, for any a &gt; 0 and ε &gt; 0, we find that

$$d _ { K } ( t ^ { - \gamma / \alpha } S _ { t } , Z ) & \leq P ( t ^ { - \gamma / \alpha } | S _ { t } - S _ { t , a } | \geq \varepsilon ) + d _ { K } ( t ^ { - \gamma / \alpha } S _ { t , a } , Z ) + \sup _ { z \in \mathbb { R } } | P ( Z \leq z ) - P ( Z \leq z + \varepsilon ) | \\ & \leq P ( t ^ { - \gamma / \alpha } | S _ { t } - S _ { t , a } | \geq \varepsilon ) + P ( | Z - Z _ { a } | \geq \varepsilon ) + d _ { K } ( t ^ { - \gamma / \alpha } S _ { t , a } , Z _ { a } ) \\ & \quad + 2 \sup _ { z \in \mathbb { R } } | P ( Z \leq z ) - P ( Z \leq z + \varepsilon ) | .$$

Combining Markov's inequality with the multivariate Mecke formula (2.1) and assumption (7.2), we obtain that, for all ε &gt; 0,

$$\mathbf P ( | Z - Z _ { a } | \geq \varepsilon ) \leq \frac { 2 } { \varepsilon } \int _ { a } ^ { \infty } x ^ { - 1 / \alpha } \, d x = \frac { 2 a ^ { 1 - 1 / \alpha } } { ( 1 / \alpha - 1 ) \varepsilon } \quad \text {and} \quad \mathbf P ( t ^ { - \gamma / \alpha } | S _ { t } - S _ { t , a } | \geq \varepsilon ) \leq \frac { g _ { 3 } ( a , t ) } { \varepsilon } \, .$$

As α-stable random variable, Z has a bounded density, see [45, page 13]. Hence, there is a constant Cα &gt; 0 only depending on α such that

$$\sup _ { z \in \mathbb { R } } | P ( Z \leq z ) - P ( Z \leq z + \varepsilon ) | \leq C _ { \alpha } \varepsilon \, , \quad \varepsilon \geq 0 \, .$$

It follows from the definitions of the Kolmogorov and the Rubinstein distance that

$$\mathbf d _ { \mathbf K } ( t ^ { - \gamma / \alpha } S _ { t , a } , Z _ { a } ) & = \sup _ { z \in \mathbb { R } } \left | \mathbf P \left ( \sum _ { x \in t ^ { \gamma } \xi _ { t } } 1 ( x \in [ - a , a ] ) \text { sign} ( x ) \, | x | ^ { - 1 / \alpha } \leq z \right ) \\ & - \mathbf P \left ( \sum _ { x \in \zeta } 1 ( x \in [ - a , a ] ) \text { sign} ( x ) \, | x | ^ { - 1 / \alpha } \leq z \right ) \right | \\ & < \mathbf d _ { \mathbf R } ( t ^ { \gamma } \, \xi _ { t } | _ { [ - a , a ] } ; \zeta | _ { [ - a , a ] } ) .$$

$$\leq d _ { \text {R} } ( t ^ { \gamma } \bullet \xi _ { t } | _ { [ - a , a ] } , \zeta | _ { [ - a , a ] } ) \, .$$

Now, we consider the Poisson case and the binomial case separately. For an underlying Poisson process, Theorem 3.1 and the assumptions in (7.1) show that

$$d _ { R } ( t ^ { \gamma } \bullet \xi _ { t } | _ { [ - a , a ] } , \zeta | _ { [ - a , a ] } ) \leq g _ { 1 } ( a , t ) + \frac { 2 ^ { k + 1 } } { k ! } g _ { 2 } ( a , t ) \, , \quad t \geq 1 \, .$$

Combining this with the previous estimates, we see that

$$\mathbf d _ { K } ( t ^ { - \gamma / \alpha } S _ { t } , Z ) \leq \frac { 2 a ^ { 1 - 1 / \alpha } } { ( 1 / \alpha - 1 ) \varepsilon } + \frac { g _ { 3 } ( a , t ) } { \varepsilon } + 2 C _ { \alpha \varepsilon } + g _ { 1 } ( a , t ) + \frac { 2 ^ { k + 1 } } { k ! } g _ { 2 } ( a , t ) \, .$$

Thus, choosing ε = √max{a1−1/α, g3(a, t)} yields the assertion. For the binomial case, Theorem 3.1 and the assumptions in (7.1) imply that

$$d _ { K } ( S _ { t , a } , Z _ { a } ) \leq & \frac { 2 a ^ { 1 - 1 / \alpha } } { ( 1 / \alpha - 1 ) \varepsilon } + \frac { g _ { 3 } ( a , t ) } { \varepsilon } + 2 C _ { \alpha \varepsilon } + g _ { 1 } ( a , t ) + \frac { 2 ^ { k + 1 } } { k ! } g _ { 2 } ( a , t ) + \frac { 6 ^ { k } k ! } { t } ( 8 a ^ { 2 } + 2 g _ { 1 } ( a , t ) ^ { 2 } ) \, ,$$

where we have used that Lt([−a, a])2 ≤ (2a + g1(a, t))2 ≤ 8a2 + 2g1(a, t)2. Now, the same choice for ε as in the Poisson case and the fact that the Kolmogorov distance is bounded by one conclude the proof. □


<!-- p:27 -->


Remark 7.9. For all choices of α ∈ (0, 2] there are α-stable random variables and one can think of U-statistics converging to such variables. For α ∈ (1, 2] and the binomial case this problem has been considered in [17, 22, 29]. A similar technique as that used in the proof of Theorem 7.8 should also be applicable if α ∈ (1, 2]. In this case the limiting random variable is given by Z := lima→∞ Za − EZa, whence an additional centring is necessary. In order to derive bounds similar to that of Theorem 7.8, one has to control the distance between Z and Za, which might be difficult to tackle. We would like to mention that the bounds derived in [22] also involve a quantity similar to dk(Z, Za).

To give an application of Theorem 7.8, let us consider the following distance-power statistics, which are closely related to the edge functionals of random geometric graphs considered above. Let for some d ≥ 1, K ⊂ Rd be a compact convex set with volume one and let K be the restriction of the Lebesgue measure to K. Let ηt be a Poisson process in K with intensity measure Kt = tK, t ≥ 1, and let βt, t ≥ 1, be a binomial process of [t] points, which are independent and uniformly distributed in K. Our aim is to investigate the limiting behaviour of the U-statistics

$$S _ { t } \coloneqq \frac { 1 } { 2 } \sum _ { ( x _ { 1 } , x _ { 2 } ) \in \mu _ { t , \neq } ^ { k } } \text {dist} ( x _ { 1 } , x _ { 2 } ) ^ { - \tau } \, , \quad t \geq 1 \, ,$$

where τ &gt; 0 and μt stands for ηt or βt. The following result, whose proof will be given in Subsection 7.4 below, deals with the case τ &gt; d.

Corollary 7.10. Let τ &gt; d, let ζ be a homogeneous Poisson process on R+ with intensity one and let Z := (κd/2)τ/d Σx∈ζ x−τ/d. Then there is a constant C &gt; 0 only depending on K, τ and d such that

$$d _ { K } ( t ^ { - 2 \tau / d } S _ { t } , Z ) \leq C \, t ^ { \varrho } \, , \ \ t \geq 1 \, ,$$

$$\varrho \coloneqq \inf _ { u > 0 } \max \left \{ \frac { 1 } { 2 } u - \frac { \tau } { 2 d } u , 2 u - 1 , u + \frac { 1 } { d } u - \frac { 2 } { d } \right \} .$$

with

Example 7.11. To have a more specific example, take τ = 2d in Corollary 7.6, in which case ρ has the form

$$\varrho = \inf _ { u > 0 } \max \left \{ - \, \frac { u } { 2 } , 2 u - 1 , u + \frac { u - 2 } { d } \right \} .$$

For d ∈ {1, 2} the infimum is attained at u = For d ≥ 3, the infimum is attained at u = 3d+2 4 so that ρ = 3d+2 2 in this case. Thus,

$$d _ { K } ( t ^ { - 4 } S _ { t } , Z ) \leq \begin{cases} C t ^ { - 1 / 5 } & \colon d \in \{ 1 , 2 \} \\ C t ^ { - 2 / ( 3 d + 2 ) } & \colon d \geq 3 \, , \end{cases}$$

where the 1/2-stable random variable Z is of the form Z = cd Σx∈ζ x−2 for a unit-intensity homogeneous Poisson process ζ on R+ and with cd = κ2/4. The distribution of Z can be characterized more explicitly. Namely, applying [24, Lemma 12.2 (i)] we see that, for all t ∈ R,

$$\underline { x \in \zeta }$$

where i is the imaginary unit. This is the characteristic function of a centred Lévy distribution with scale parameter πcd/2. Thus, Z has density x → 1 √cd/x3 exp(−πcd/(4x)) 1(x &gt; 0).

Remark 7.12. Note that if τ &lt; d/2, then St satisfies a central limit theorem as shown in Theorem 3.1 of [36]. Moreover, the choice d/2 ≤ τ ≤ d corresponds to the situation α ∈ [1, 2], to which Remark 7.9 applies.


<!-- p:28 -->


### 7.4 Random geometric graphs

Let K ⊂ Rd (d ≥ 1) be a compact convex set with volume one. For t ≥ 1 let μt be either a homogeneous Poisson process ηt of intensity t ≥ 1 in K or a binomial process βt of [t] independent and uniformly distributed points in K and let (θt)t≥1 be a family of positive real numbers. Based on this data we construct a random geometric graph as explained in Section 7.1. In contrast to Corollary 7.2 and Corollary 7.6, where lim t2θd = λ ∈ [0, ∞), we assume here that lim t2θd = ∞. In this section we t→∞ t→∞ are interested in the point process ξt,a on K defined by

$$\xi _ { t , a } \coloneqq \frac { 1 } { 2 } \sum _ { ( x , y ) \in \mu _ { t , \neq } ^ { 2 } } 1 ( \| x - y \| \leq \min \{ \theta _ { t } , t ^ { - 2 / d } a \} ) \, \delta _ { ( x + y ) / 2 }$$

for some a &gt; 0. In other words, ξt,a charges the collection of all midpoints of edges of the random geometric graph whose length does not exceed t−2/da. Due to our assumption that lim t2θd = ∞, t→∞ we have that t0 := sup{t ≥ 1 : t2θd &lt; ad} ∪ {1} &lt; ∞. Note that min{θt, t−2/da} = t−2/da for t ≥ t0. We denote by Lt,a the intensity measure of ξt,a. To deal with the Poisson and the binomial case in parallel let χ(t) := t2 for μt = ηt and χ(t) := [t]([t] − 1) for μt = βt. For sets B ∈ B(Rd) with B ⊂ K and for t ≥ t0, Lt,a is of the form

$$\text { and for } t \geq t _ { 0 } , \, L _ { t , a } \text { is of the form } \\ L _ { t , a } ( B ) = \frac { \chi ( t ) } { 2 } \int _ { K } \int _ { K } 1 ( ( x + y ) / 2 \in B , \, \| x - y \| \leq t ^ { - 2 / d } a ) \, d x \, d y \\ = \frac { \chi ( t ) } { 2 } \int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { R } ^ { d } } 1 ( ( x + y ) / 2 \in B , \, \| x - y \| \leq t ^ { - 2 / d } a ) \, d x \, d y \\ - \frac { \chi ( t ) } { 2 } \int _ { ( \mathbb { R } ^ { d } ) ^ { 2 } \langle K ^ { 2 } } 1 ( ( x + y ) / 2 \in B , \, \| x - y \| \leq t ^ { - 2 / d } a ) \, d ( x , y ) \, , \\ \intertext { where in the first line we have used the multivariate M e c k e f l u m a \, ( 2 . 1 ) for the Poisson process and }$$

where in the first line we have used the multivariate Mecke formula (2.1) for the Poisson process and ts t d  sd t t e t t   s  t o ( n sne of variables u = x − y, v = (x + y)/2, which has Jacobian one, to see that

$$= x - y , \, v & = ( x + y ) / 2 , \, \text {which has Jacobian one, to see that} \\ & \frac { \chi ( t ) } { 2 } \int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { R } ^ { d } } 1 ( ( x + y ) / 2 \in B , \| x - y \| \leq t ^ { - 2 / d } a ) \, d x \, d y \\ & = \frac { \chi ( t ) } { 2 } \int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { R } ^ { d } } 1 ( v \in B , \| u \| \leq t ^ { - 2 / d } a ) \, d u \, d v \\ & = \frac { \chi ( t ) } { 2 } \kappa _ { d } ( t ^ { - 2 / d } a ) ^ { d } \, v o l ( B ) \\ & = \frac { \kappa _ { d } } { 2 } \frac { \chi ( t ) } { t ^ { 2 } } \, a ^ { d } \, v o l ( B ) \, . \\ \intertext { c a n c y ( t ) / t ^ { 2 } = 1 , w h e r e a s } | \chi ( t ) / t ^ { 2 } - 1 | \leq 1 / t \, i n t h e b i n o m i a l c u s e . \, F o r t h e n d a n t h e d o w s$$

In the Poisson case χ(t)/t2 = 1, whereas |χ(t)/t2 − 1| ≤ 1/t in the binomial case. For the second term we have, independently of B, the upper bound

$$\begin{array} { r l } & { \frac { \chi ( t ) } { 2 } \int _ { ( \mathbb { R } ^ { d } ) ^ { 2 } \langle K ^ { 2 } } 1 ( ( x + y ) / 2 \in B , \| x - y \| \leq t ^ { - 2 / d } a ) \, d ( x , y ) } \\ & { \leq \chi ( t ) \, v o l \{ ( x \in \mathbb { R } ^ { d } \ \langle K \colon d i s t ( x , K ) \leq t ^ { - 2 / d } a \} ) \, \kappa _ { d } \, ( t ^ { - 2 / d } a ) ^ { d } } \\ & { \leq 2 \, v o l \{ ( x \in \mathbb { R } ^ { d } \ \langle K \colon d i s t ( x , K ) \leq t ^ { - 2 / d } a \} ) \, \kappa _ { d } \, a ^ { d } . } \end{array}$$

From Steiner's formula (2.7) it follows that there is a constant cK,a &gt; 0 only depending on a, d and K such that

$$\ v o l ( \{ x \in \mathbb { R } ^ { d } \ \ K \colon \text {dist} ( x , K ) \leq t ^ { - 2 / d } a \} ) \leq c _ { K , a } \, t ^ { - 2 / d }$$

for all t ≥ t0. Altogether, we see that there is a constant c1 &gt; 0 depending only on a, d and K such that for all t ≥ t0 we have

$$d _ { T V } \left ( L _ { t , a } , \frac { \kappa _ { d } } { 2 } \, a ^ { d } \, v o l | _ { K } \right ) \leq c _ { 1 } \, t ^ { - \min \{ 2 / d , 1 \} } \, ,$$


<!-- p:29 -->


where vol|K stands for the restriction of Lebesgue measure to K. Finally, for Borel sets B ⊂ K we have to bound

$$r _ { t , a } ( B ) = \widetilde { \chi } ( t ) \int _ { K } \left ( \int _ { K } 1 ( ( x + y ) / 2 \in B , \| x - y \| \leq \min \{ \theta _ { t } , t ^ { - 2 / d } a \} ) \, d x \right ) ^ { 2 } d y \, ,$$

where χ(t) := t3 in the Poisson case and χ(t) := ([t])3 in the binomial case. For t ≥ t0 this can be estimated from above by

$$r _ { t , a } ( B ) \leq 8 t ^ { 3 } \int _ { K } \left ( \kappa _ { d } ( t ^ { - 2 / d } a ) ^ { d } \right ) ^ { 2 } \text {d} y = 8 t ^ { 3 } \kappa _ { d } ^ { 2 } ( t ^ { - 2 / d } a ) ^ { 2 d } = 8 \kappa _ { d } ^ { 2 } a ^ { 2 d } t ^ { - 1 } .$$

Hence, there is a constant c2 &gt; 0 only depending on a and d such that rt,a(B) ≤ c2 t−1 for all B ∈ B(Rd) with B ⊂ K and t ≥ t0. We can now conclude the following from Theorem 3.1.

Theorem 7.13. Let a &gt; 0, let ζ be a Poisson process on K with intensity measure Kd ad vol|K and 2 let ξt,a be constructed from a Poisson process ηt or a binomial process βt with t ≥ 1. Also suppose that lim t2θ = ∞. Then t0 := sup{t ≥ 1 : t2θd &lt; ad} ∪ {1} &lt; ∞ and there is a constant C &gt; 0 only t→∞ depending on a, d and K such that

$$d _ { R } ( \xi _ { t , a } , \zeta ) \leq C \, t ^ { - \min \{ 2 / d , 1 \} } \, , \quad t \geq t _ { 0 } \, .$$

The remaining part of this section is devoted to the postponed proofs of the results in Subsections 7.1, 7.2 and 7.3.

Proof of Corollary 7.2 and Corollary 7.6. Let us define

$$t ^ { 2 / d } \bullet \xi _ { t } \coloneqq \frac { 1 } { 2 } \sum _ { ( x _ { 1 } , x _ { 2 } ) \in \mu _ { t , \neq } ^ { 2 } } 1 ( \text {dist} ( x _ { 1 } , x _ { 2 } ) \leq \theta _ { t } ) \, \delta _ { t ^ { 2 / d } \text {dist} ( x _ { 1 } , x _ { 2 } ) } \, , \quad t \geq 1 \, .$$

The intensity measure Lt of t2/d · ξt is given by

$$L _ { t } ( A ) = \frac { \chi ( t ) } { 2 } \int _ { K } \int _ { K } 1 ( \text {dist} ( x _ { 1 } , x _ { 2 } ) \in t ^ { - 2 / d } A \cap [ 0 , \theta _ { t } ] ) \, d x _ { 1 } \, d x _ { 2 } \, , \quad A \in \mathcal { B } ( \mathbb { R } ) \, , \quad t \geq 1 \, ,$$

with χ(t) as above. The arguments leading to Theorem 7.13 also show that

$$M ( A ) \coloneqq \lim _ { t \to \infty } L _ { t } ( A ) = \lim _ { t \to \infty } \frac { d \kappa _ { d } } { 2 } \int _ { A } 1 ( r \leq t ^ { 2 / d } \theta _ { t } ) \, r ^ { d - 1 } \, d r \, , \quad A \in \mathcal { B } ( \mathbb { R } ) \, ,$$

and, for any a &gt; 0 and t ≥ 0,

$$d _ { t } ( \dot { M } | _ { [ 0 , a ] } , L _ { t } | _ { [ 0 , a ] } ) & \leq \left | \frac { \kappa _ { d } } { 2 } \min \{ a , t ^ { 2 / d } \theta _ { t } \} ^ { d } - \lim _ { t \to \infty } \frac { \kappa _ { d } } { 2 } \min \{ a , t ^ { 2 / d } \theta _ { t } \} ^ { d } \right | \\ & + \left | \frac { \kappa _ { d } } { 2 } \min \{ a , t ^ { 2 / d } \theta _ { t } \} ^ { d } - \frac { \kappa _ { d } \chi ( t ) } { 2 t ^ { 2 } } \min \{ a , t ^ { 2 / d } \theta _ { t } \} ^ { d } \right | \\ & + C _ { K } \kappa _ { d } \min \{ a , t ^ { 2 } \theta _ { t } ^ { d } \} \left ( \min \{ t ^ { - 2 / d } a , \theta _ { t } \} + \min \{ t ^ { - 2 / d } a , \theta _ { t } \} ^ { d } \right ) ,$$

where CK &gt; 0 is a constant only depending on the set K. Moreover, we have, with χ(t) as above,

$$r _ { t } ( [ 0 , a ] ) & \colon = \widetilde { \chi } ( t ) \int _ { K } \left ( \int _ { K } \mathbf 1 ( \| x _ { 1 } - x _ { 2 } \| \leq \min \{ t ^ { - 2 / d } a , \theta _ { t } \} ) \, d x _ { 1 } \right ) ^ { 2 } d x _ { 2 } \\ & \leq 8 t ^ { 3 } \kappa _ { d } ^ { 2 } \min \{ t ^ { - 2 / d } a , \theta _ { t } \} ^ { 2 d } .$$

Letting a → ∞ we see that the measure M is finite. A short compuatation yields that Lt(R+) ≤ κdt2θd. Now Theorem 7.1 and Theorem 7.4 imply Corollary 7.2 and Corollary 7.6, respectively. □


<!-- p:30 -->


Proof of Corollary 7.10. In the set-up around the random geometric graphs as above, we put θt = ∞ and consider the transformed process

$$t ^ { 2 } \bullet \widehat { \xi } _ { t } = \sum _ { x \in t ^ { 2 / d } \bullet \xi _ { t } } \delta _ { \kappa _ { d } x ^ { d } / 2 } \, .$$

The intensity measure Lt of t2 · ξt converges to the restriction of the Lebesgue measure to R+. By using the transformation x → κdxd/2 again, we see that bounds similar to (7.3) and (7.4) hold for t2 · ξt if a is replaced by (2a/κd)1/d on the right-hand sides. Hence, for γ = 2 and α = d/τ, the assumptions in (7.1) are satisfied with

$$g _ { 1 } ( a , t ) = \hat { C } _ { 1 } \, a ( t ^ { - 2 / d } a ^ { 1 / d } + t ^ { - 2 } a + t ^ { - 1 } ) \quad \text {and} \quad g _ { 2 } ( a , t ) = \hat { C } _ { 2 } \, t ^ { - 1 } a ^ { 2 } \, ,$$

where 1 &gt; 0 and 2 &gt; 0 are constants depending only on K and d. Because of

$$C _ { 1 } & > 0 \text { and } C _ { 2 } > 0 \text { are constants depending only on } K \text { and } d . \text { Because of } \\ & \frac { t ^ { - 2 \tau / d } } { 2 } E \sum _ { ( x _ { 1 } , x _ { 2 } ) \in \mu _ { t , \neq } ^ { 2 } } 1 ( \text {dist} ( x _ { 1 } , x _ { 2 } ) ^ { - \tau } \leq t ^ { 2 \tau / d } a ^ { - \tau / d } ) \text { dist} ( x _ { 1 } , x _ { 2 } ) ^ { - \tau } \\ & \leq d \kappa _ { d } t ^ { 2 - 2 \tau / d } \int _ { t ^ { - 2 / d } a ^ { 1 / d } } r ^ { - \tau } r ^ { d - 1 } \, d r \\ & = \frac { d \kappa _ { d } } { \tau - d } a ^ { 1 - \tau / d } \, , \\ \intertext { c h o n } ( 7 \, 2 ) \, \text { holds with } a ( \tau ) = \frac { d \kappa _ { d } } { \sigma } a ^ { 1 - \tau / d } \, T h u s \, \text { Corollary } 7 \, 1 0 \, f o l w s \, \text { from Theorem}$$

1q 82 m o om 1 eo m 1/1-1condition (7.2) holds with g3(a, t) = p−⊥ choosing a = tu with u &gt; 0. □

### 7.5 Proximity of Poisson flats

Let us fix a space dimension d ≥ 2 and a dimension parameter m ≥ 1 such that m &lt; d/2. Recall that with the property that two independent random with distribution Q are almost surely in general position, meaning that the dimension of the linear hull of L and M is 2m with probability one. Note that this is satisfied, for m cf. [37, Theorem 4.4.5 (c)]. The measure Q induces a translation-invariant measure Kt on Ad via m

$$\int _ { \mathbb { A } _ { m } ^ { d } } g ( E ) \, \mathbf K _ { t } ( d E ) = t \int _ { \mathbb { G } _ { m } ^ { d } } \int _ { E _ { 0 } ^ { \perp } } g ( E _ { 0 } + x ) \, \text {vol} _ { E _ { 0 } ^ { \perp } } ( d x ) \, \mathbb { Q } ( d E _ { 0 } ) \, ,$$

where t ≥ 1 is an intensity parameter, g ≥ 0 is a measurable function on Am and volE⊥ denotes the Lebesgue measure on E, the orthogonal complement of E0. We use the convention K := K1 and can re-write Kt as Kt = tK. We now consider a Poisson process ηt with intensity measure Kt. This is what is usually called a Poisson m-flat process in stochastic geometry [37, Chapter 4.4]. One particular problem for such m-flat processes is to describe the mutual arrangement of the flats in space. Since m &lt; d/2, any two different flats E, F of ηt do not intersect each other with probability one. Thus, they have a well defined distance dist(E, F) and we denote by m(E, F) the midpoint of the almost surely uniquely determined line segment realizing this distance (the perpendicular of E and F). We are interested here in the point process of the midpoints m(E, F) such that the flats E, F are close together and m(E, F) is in a compact convex set K ⊂ Rd of volume 0 &lt; vol(K) &lt; ∞. To the best of our knowledge, Theorem 7.14 is the first result describing its asymptotic behaviour, as t → ∞. To do so, we define for t ≥ 1 and a &gt; 0, ξt,a on K by

$$\xi _ { t , a } \colon = \frac { 1 } { 2 } \sum _ { ( E , F ) \in \eta _ { t , \neq } ^ { 2 } } \delta _ { m ( E , F ) } \, 1 ( \text {dist} ( E , F ) \leq a t ^ { - 2 / ( d - 2 m ) } , \, m ( E , F ) \in K ) \, .$$


<!-- p:31 -->


The intensity measure Lt,a(B) of ξt,a for a Borel set B ⊂ K is given by

$$L _ { t , a } ( B ) = \frac { t ^ { 2 } } { 2 } \int _ { \mathbb { A } _ { m } ^ { d } } \int _ { \mathbb { A } _ { m } ^ { d } } 1 ( m ( E , F ) \in B , \text {dist} ( E , F ) \leq a t ^ { - 2 / ( d - 2 m ) } ) \text {K} ( \text {d} E ) \text {K} ( \text {d} F )$$

due to the multivariate Mecke formula (2.1). It follows from [42, Theorem 1] that

$$L _ { t , a } ( B ) = \frac { t ^ { 2 } } { 2 } \kappa _ { d - 2 m } ( a t ^ { - 2 / ( d - 2 m ) } ) ^ { d - 2 m } V _ { d } ( B ) \int _ { \mathbb { G } _ { k } ^ { d } } \int _ { \mathbb { G } _ { k } ^ { d } } [ M , L ] \, \mathbb { Q } ( d L ) \, \mathbb { Q } ( d M ) \, ,$$

(it is readily checked that the identity there extends from compact convex sets to general Borel sets). This leads to

Now, putting

$$\mathcal { C } \coloneqq \frac { \kappa _ { d - 2 m } } { 2 } \, \int _ { \mathbb { G } _ { m } ^ { d } } \int _ { \mathbb { G } _ { m } ^ { d } } [ L , M ] \, \mathbb { Q } ( \mathbf d L ) \, \mathbb { Q } ( \mathbf d M ) \, ,$$

we see that

$$d _ { T V } \left ( L _ { t , a } , \mathcal { C } \, a ^ { d - 2 m } \, v o l | _ { K } \right ) = 0 \, ,$$

where vol|K stands for the restriction of the Lebesgue measure on Rd to K. Moreover, the proof of [42, Theorem 3] shows that there is a constant  &gt; 0 only depending on a, d, m, Q and K such that ft(B) ≤ Č t−1 uniformly for all Borel sets B ⊂ K. From this we conclude that rt(B) ≤ Lt,a(B) t(B) ≤ ê Lt,a(B) t−1 and in view of Theorem 3.1 the following result for the midpoint process ξt,a.

Theorem 7.14. Let a &gt; 0 and let ζ be a Poisson process with intensity measure C ad−2m vol|K, where C is as at (7.6). Then there is a constant C &gt; 0 depending on a, d, m, Q and K such that

$$d _ { R } ( \xi _ { t , a } , \zeta ) \leq C \, t ^ { - 1 } , \ \ t \geq 1 \, .$$

Reon r r      (  s t rn (  rm

$$\mathcal { C } = \frac { 1 } { 2 } \frac { \binom { d - m } { m } } { \binom { d } { m } } \frac { \kappa _ { d - m } ^ { 2 } } { \kappa _ { d } }$$

(or, equivalently, if the m-flat process is stationary and isotropic, see [37]).

- (ii) As opposed to our previous applications, we do not consider a binomial counterpart to Theorem 7.14. The reason for that is that there is no normalization, which would turn the measure K1 defined at (7.5) into a probability measure.
- (iii) Theorem 7.14 extends Theorem 7.13 from m = 0 (which has been excluded here for technical reasons) to arbitrary m satisfying m &lt; d/2. However, due to the slightly different set-ups (an underlying point process on the compact set K vs. a point process on the non-compact space Am), there are boundary effects in the context of Theorem 7.13, implying that the total variation distance dTv(Lt,a, M) is not identically zero there. These boundary effects are not present for m ≥ 1, which eventually leads to the rate O(t−1) for the Rubinstein distance in this case.

$$L _ { t , a } ( B ) = \frac { \kappa _ { d - 2 m } } { 2 } \, v o l ( B ) \, a ^ { d - 2 m } \, \int _ { \mathbb { G } _ { m } ^ { d } } \int _ { \mathbb { G } _ { m } ^ { d } } [ L , M ] \, \mathbb { Q } ( d L ) \, \mathbb { Q } ( d M ) \, .$$


<!-- p:32 -->


Figure 1: Illustration of the argument used in the derivation of Theorem 7.16

2-s

r

y

1

●

1

-y

Bd(−y, r)

### 7.6 Random polytopes with vertices on the sphere

Let Sd-1 be the unit sphere of dimension d − 1 (d ≥ 2). Let μt be a Poisson process ηt on Sd-1 whose intensity measure is a constant multiple t ≥ 1 of the normalized spherical Lebesgue measure or a binomial process βt of [t] independent and uniformly chosen points on Sd-1. The convex hull conv(μt) of μt is a random polytope with vertices on Sd-1 and we denote by Dt the diameter of conv(μt), that is,

$$D _ { t } \coloneqq \max _ { ( x , y ) \in \mu _ { t , \neq } ^ { 2 } } \| x - y \| \, . \\$$

More generally, define the point process of all reversed interpoint distances by

$$\xi _ { t } = \frac { 1 } { 2 } \sum _ { ( x , y ) \in \mu _ { t , \neq } ^ { 2 } } \delta _ { 2 - \| x - y \| } \, .$$

Clearly, Dt is then two minus the distance from the origin to the closest point of ξt. We define

$$L _ { t } ( A ) \colon = \frac { 1 } { 2 } \, E \sum _ { ( x , y ) \in \mu _ { t , \neq } ^ { 2 } } 1 ( t ^ { 4 / ( d - 1 ) } ( 2 - \| x - y \| ) \in A ) , \quad A \subset \mathbb { R } _ { + } \quad B o r e l .$$

Let χ(t) := t2 in the Poisson case and χ(t) := [t]([t] − 1) in the binomial case. Applying the Mecke formula (2.1) or its analogue (2.2) for binomial processes, respectively, we see that

$$L _ { t } ( [ 0 , a ] ) = \frac { \chi ( t ) } { 2 ( d \kappa _ { d } ) ^ { 2 } } \int _ { \mathbb { S } ^ { d - 1 } } \int _ { \mathbb { S } ^ { d - 1 } } 1 ( \| x - y \| \geq 2 - a t ^ { - 4 / ( d - 1 ) } ) \, \mathcal { H } ^ { d - 1 } ( d x ) \, \mathcal { H } ^ { d - 1 } ( d y ) \, ,$$

where dκd is the surface area of Sd−1 and Hd-1 stands for the (d − 1)-dimensional Hausdorff measure. For fixed y ∈ Sd-1, the indicator function is one if and only if the point x is contained in a certain spherical cap Sd−1 ∩ Bd(−y, r) centred at the antipodal point -y of y, whose radius r has to be determined. For this, we refer to Figure 1 and notice that (2 − s)2 + r2 = 4 so that r = √4s − s2. Hence, the (d − 1)-dimensional volume of Sd−1 ∩ Bd(−y, r) is given by

$$( d - 1 ) \kappa _ { d - 1 } \int _ { 0 } ^ { 2 s - s ^ { 2 } / 2 } ( 2 h - h ^ { 2 } ) ^ { ( d - 3 ) / 2 } \, d h \, ,$$

independently of y. Using the substitution h = 2ut−4/(d−1) − u2t−8/(d−1) /2 this means that

$$\text {Im} ( \text {pcnclnly} \, \mathfrak { r } \, g . \, \text {Cos} \, \mathfrak { r } \, \text {Subsection} \, h = 2 u t ^ { 2 } \, \cdots \, \cdots \, 2 \, \text {hams} \, \text {that} \, \\ \text {L} _ { t } ( [ 0 , a ] ) & = \frac { \chi ( t ) } { 2 d \kappa _ { d } } \left ( d - 1 \right ) \kappa _ { d - 1 } \int _ { 0 } ^ { 2 a t ^ { - 4 ( d - 1 ) } - a ^ { 2 } t ^ { - 8 / ( d - 1 ) / 2 } } ( 2 h - h ^ { 2 } ) ^ { ( d - 3 ) / 2 } \, d h \\ & = \frac { \chi ( t ) } { 2 d \kappa _ { d } } \left ( d - 1 \right ) \kappa _ { d - 1 } \int _ { 0 } ^ { 4 u t ^ { - 4 / ( d - 1 ) } - u ^ { 2 } t ^ { - 8 / ( d - 1 ) } - ( 2 u t ^ { - 4 / ( d - 1 ) } - u ^ { 2 } t ^ { - 8 / ( d - 1 ) / 2 } ) ^ { ( d - 3 ) / 2 } } \\ & \quad \times ( 2 t ^ { - 4 / ( d - 1 ) } - u t ^ { - 8 / ( d - 1 ) } ) \, d u$$


<!-- p:33 -->


$$= \frac { 1 } { 2 d \kappa _ { d } } \, \frac { \chi ( t ) } { t ^ { 2 } } \left ( d - 1 \right ) \kappa _ { d - 1 } \int _ { 0 } ^ { a } \left ( 4 u - u ^ { 2 } t ^ { - 4 / ( d - 1 ) } - t ^ { - 4 / ( d - 1 ) } ( 2 u - u ^ { 2 } t ^ { - 4 / ( d - 1 ) } / 2 ) ^ { 2 } \right ) ^ { ( d - 3 ) / 2 } \\ \times ( 2 - u t ^ { - 4 / ( d - 1 ) } ) \, d u \, .$$

Hence, we have for any Borel set A ⊂ R+ that

$$L _ { t } ( A ) & = \frac { ( d - 1 ) \kappa _ { d - 1 } } { 2 d \kappa _ { d } } \, \frac { \chi ( t ) } { t ^ { 2 } } \int _ { A } \left ( 4 u - u ^ { 2 } t ^ { - 4 / ( d - 1 ) } - t ^ { - 4 / ( d - 1 ) } ( 2 u - u ^ { 2 } t ^ { - 4 / ( d - 1 ) } / 2 ) ^ { 2 } \right ) ^ { ( d - 3 ) / 2 } \\ & \quad \times ( 2 - u t ^ { - 4 / ( d - 1 ) } ) \, d u \, .$$

The measure Lt converges, as t → ∞ and in the strong sense, to a measure M on R+ given by

$$M ( A ) \coloneqq \frac { d - 1 } { d \kappa _ { d } } \kappa _ { d - 1 } 2 ^ { d - 3 } \int _ { A } u ^ { ( d - 3 ) / 2 } \, d u \, , \quad A \subset \mathbb { R } _ { + } \quad B o r e l \, .$$

Moreover, for any bounded Borel set B ⊂ R+ there is a constant c1,B &gt; 0 only depending on B and the space dimension d such that

$$d _ { T V } ( L _ { t } | _ { B } , M | _ { B } ) \leq c _ { 1 , B } t ^ { - \min \{ 4 / ( d - 1 ) , 1 \} } , \quad t \geq 1 \, .$$

Here we have used that |χ(t)/t2 − 1| ≤ t−1 for t ≥ 1. Let χ(t) := t in the Poisson case and χ(t) := [t] in the binomial case. The same arguments as above also show that

$$\hat { r } _ { t } ( B ) = \sup _ { x \in \mathbb { S } ^ { d - 1 } } \frac { \widetilde { \chi } ( t ) } { d \kappa _ { d } } \int _ { \mathbb { S } ^ { d - 1 } } 1 ( 2 - \| x - y \| \in t ^ { - 4 / ( d - 1 ) } B ) \, \mathcal { H } ^ { d - 1 } ( d y ) \leq c _ { 2 , B } \, t ^ { - 1 }$$

with a constant c2,B &gt; 0 only depending on B and d so that rt(B) ≤ Lt(B) t(B) ≤ c2,B Lt(B) t−1. Applying Corollary 3.3 we conclude the following result.

Theorem 7.16. Let ζ be a Poisson process on R+ with intensity measure given by (7.7) and let ξt be derived from a Poisson process ηt or a binomial process βt on Sd-1. Then, for any bounded Borel set B ⊂ R+ there is a constant CB,d &gt; 0 only depending on B and d such that

$$d _ { \mathbf R } ( ( t ^ { 4 / ( d - 1 ) } \bullet \xi _ { t } ) | _ { B } , \zeta | _ { B } ) \leq C _ { B , d } \, t ^ { - \min \{ 4 / ( d - 1 ) , 1 \} } , \ \ t \geq 1 \, .$$

In particular, for the diameter Dt of the random polytope, constructed from a Poisson process ηt or a binomial process βt, we have

$$| \mathbf P ( t ^ { 4 / ( d - 1 ) } ( 2 - D _ { t } ) > a ) - e ^ { - \frac { 1 } { d \kappa _ { d } } \kappa _ { d - 1 } 2 ^ { d - 2 } a ^ { ( d - 1 ) / 2 } } | \leq C _ { a , d } t ^ { - \min \{ 4 / ( d - 1 ) , 1 \} } , \ \ t \geq 1 ,$$

with a constant Ca,d &gt; 0 only depending on a &gt; 0 and d.

Remark 7.17. The limiting distribution for the diameter is also derived in [30, Theorem 5.2] and [26, Theorem 3.1], where the latter one allows the underlying random points to have distributions different from the uniform distribution. While the result in [30] does not give any rates of convergence, in [26, Theorem 3.1] it has erroneously been claimed that the rate of convergence for Dt to its limiting Weibull random variable is of order t-1. However, in our notation the rate of convergence stated in (2.5) in [26] concerns only the difference to a Weibull random variable with parameter Lt([0, a]) and not to a Weibull random variable with parameter M([0, a]) as stated by the authors. For the difference to a Weibull random variable with parameter Lt([0, a]) our result also yields a rate of order t−1 since dTv(Lt|[0,a], Lt|[0,a]) = 0 in this case.

###### Acknowledgements

This research has been initiated during the Oberwolfach mini-workshop "Stochastic Analysis for Poisson Point Processes". All support is gratefully acknowledged.

LD has partially been supported by ANR Masterie. MS has been funded by the German Research Foundation (DFG) through the research unit "Geometry and Physics of Spatial Random Systems" n (u o     ns  s n -  r  n SFB-TR 12.


<!-- p:34 -->
