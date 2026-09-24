---
id: "Decreusefond_2016_Functional-Poisson-Approximation-KR-U-Statistics"
source_pdf: "../pdf/Decreusefond_2016_Functional-Poisson-Approximation-KR-U-Statistics.pdf"
source_filename: "Decreusefond_2016_Functional-Poisson-Approximation-KR-U-Statistics.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "excellent"
extraction_score: 100.0
visual_assets: "disabled"
references_file: "../references/Decreusefond_2016_Functional-Poisson-Approximation-KR-U-Statistics.references.md"
---

<!-- p:1 -->

2016, Vol. 44, No. 3, 2147-2197

c

©

#### FUNCTIONAL POISSON APPROXIMATION IN KANTOROVICH-RUBINSTEIN DISTANCE WITH APPLICATIONS TO U-STATISTICS AND STOCHASTIC GEOMETRY

By Laurent Decreusefond 1 , 2 3

Matthias Schulte and Christoph Th ̈ ale

Telecom ParisTech, Karlsruhe Institute of Technology and Ruhr University Bochum

A Poisson or a binomial process on an abstract state space and a symmetric function f acting on k -tuples of its points are considered. They induce a point process on the target space of f . The main result is a functional limit theorem which provides an upper bound for an optimal transportation distance between the image process and a Poisson process on the target space. The technical background are a version of Stein's method for Poisson process approximation, a Glauber dynamics representation for the Poisson process and the Malliavin formalism. As applications of the main result, error bounds for approximations of U-statistics by Poisson, compound Poisson and stable random variables are derived, and examples from stochastic geometry are investigated.

## Introduction. The arguably most prominent functional limit theorem is Donsker's invariance principle. It asserts that the distribution of a linear interpolation between the points of a suitably re-scaled random walk converges to the Wiener measure on the space of continuous functions on R + , the nonnegative real half-line; see, for example, [24], Corollary 16.7. Besides the Wiener process, there is another fundamental stochastic process, which plays an important role in many branches of probability theory and

Received June 2014; revised March 2015.

1 Supported in part by ANR Masterie.

2 Supported by the German Research Foundation (DFG) through the research unit 'Geometry and Physics of Spatial Random Systems' Grant HU 1874/3-1.

3 Supported by the German research foundation (DFG) via SFB-TR 12.

AMS 2000 subject classifications. Primary 60F17, 60G55; secondary 60D05, 60E07, 60H07.

Key words and phrases. Binomial process, configuration space, functional limit theorem, Glauber dynamics, Kantorovich-Rubinstein distance, Malliavin formalism, Poisson process, Stein's method, stochastic geometry, U-statistics.

This is an electronic reprint of the original article published by the Institute of Mathematical Statistics in The Annals of Probability , 2016, Vol. 44, No. 3, 2147-2197. This reprint differs from the original in pagination and typographic detail.


<!-- p:2 -->


its applications, namely the Poisson process. However, functional limit theorems involving the Poisson process have found much less attention in the literature. The aim of this paper is to provide a quantitative version of a functional limit theorem for Poisson processes and to derive from it error bounds for the probabilistic approximation of U-statistics by a Poisson, a compound Poisson or a stable random variable. We demonstrate the versatility of our results by applying these bounds to functionals of random geometric graphs, distance-power statistics, nonintersecting flat processes and random polytopes.

Let us informally describe the set-up of this paper; precise definitions and statements follow in Section 3. Let ( X , X ) and ( Y , Y ) be two measurable spaces (satisfying some mild regularity assumptions, see below), let K 1 be a probability measure on X and fix an integer k ≥ 1. Moreover, for each n ∈ N let f n : dom f n → Y be a symmetric mapping whose domain dom f n is a symmetric subset of X k . Next, consider a collection β n = { X 1 , . . . , X n } of n ≥ k i.i.d. random elements X 1 , . . . , X n of X with distribution K 1 . We apply for each n ≥ k , f n to every k -tuple of distinct elements of β n . This induces a point process ξ n on Y of the form

$$\xi _ { n } = \frac { 1 } { k ! } \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \beta _ { n , \neq } ^ { k } \cap \text {dom} \ f _ { n } } \delta _ { f _ { n } ( x _ { 1 } , \dots , x _ { k } ) } ,$$

̸


The motivation for studying the point processes ξ n as defined above comes from the theory of U-statistics and from a class of extreme value problems arising in stochastic geometry. At first, if dom f n = X k and Y = R , the points of ξ n can be regarded as the summands of the U-statistic

̸

where β k n, = = { ( x 1 , . . . , x k ) ∈ β k n : x j = x j , i = j, i, j =1 , . . . , k } and δ y stands for the unit mass Dirac measure concentrated at y ∈ Y .

$$S _ { n } = \frac { 1 } { k ! } \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \beta _ { n , \neq } ^ { k } } f _ { n } ( x _ { 1 } , \dots , x _ { k } ) .$$

̸

These objects play a prominent role in large parts of probability theory and mathematical statistics, and an analysis of the point process of summands is helpful for the understanding of their (asymptotic) properties. On the other hand, in several problems arising in stochastic geometry, one is interested in extreme values of the type

$$\min _ { ( x _ { 1 } , \dots , x _ { k } ) \in \beta _ { n , \neq } ^ { k } } f _ { n } ( x _ { 1 } , \dots , x _ { k } )$$

̸

in case that dom f n = X k and Y =[0 , ∞ ). Clearly, this minimum is the distance from the origin to the first point of the point process ξ n . For these reasons, a study of the point processes ξ n unifies both mentioned problems.


<!-- p:3 -->


The intensity measure L n of ξ n is given by

$$T h e i n t i s y \, & \, \text {measure } L _ { n } \, \text { of } \xi _ { n } \, \text { is given by} \\ L _ { n } ( A ) = E \xi _ { n } ( A ) = \frac { ( n ) _ { k } } { k ! } \int _ { \text {dom} f _ { n } } 1 ( f _ { n } ( x _ { 1 } , \dots , x _ { k } ) \in A ) K _ { 1 } ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) , \\ & \, A \in \mathcal { Y } , \\ \text {where } ( n ) _ { k } \, \text { is the descending factorial. Our main result, Theorem 3.1 below,}$$

where ( n ) k is the descending factorial. Our main result, Theorem 3.1 below, provides an upper bound for the Kantorovich-Rubinstein distance d KR ( ξ n , ζ ) between ξ n and a Poisson process ζ on Y with finite intensity measure M . Here, the Kantorovich-Rubinstein distance is a variant of an optimal transportation distance, which measures the closeness between two point processes or, more precisely, their distributions. In particular, we show that ξ n converges in Kantorovich-Rubinstein distance, and thus in distribution to ζ if

$$d _ { T V } ( L _ { n } , M ) \to 0 \quad \text {and} \quad \mathbf E _ { n } ( \mathbb { V } ) ^ { 2 } \to \mathbf M ( \mathbb { V } ) ^ { 2 } + \mathbf M ( \mathbb { V } ) \quad \text {as } n \to \infty , \\ \\ 1 \quad 1 \quad ( \begin{matrix} 0 & 0 & 0 \quad \text {and} \quad \mathbf E _ { n } ( \mathbb { V } ) ^ { 2 } \to \mathbf M ( \mathbb { V } ) ^ { 2 } + \mathbf M ( \mathbb { V } ) \\ 0 & 0 & 0 & 0 \quad \text {and} \quad \mathbf E _ { n } ( \mathbb { V } ) ^ { 2 } \to \mathbf M ( \mathbb { V } ) \quad \text {as } n \to \infty , \\ \end{matrix}$$

where d TV ( · , · ) denotes the total variation distance of measures on Y . More precisely, the upper bound for the Kantorovich-Rubinstein distance only depends on d TV ( L n , M ) and the first two moments of ξ n ( Y ). This is a functional version of the famous results by Arratia, Goldstein and Gordon [1], and Chen [14] that 'two moments suffice for Poisson approximation.'

Besides the binomial process β n of n independent and identically distributed points, we also allow the input process to be a Poisson process on X with a σ -finite intensity measure. In some instances, an underlying Poisson process is more natural and sometimes even unavoidable, especially if the underlying point process on X is supposed to have infinitely many points. To exploit this flexibility, we consider both set-ups in parallel.

Poisson process approximation has been studied by several authors by means of Stein's method, but to the best of our knowledge this is the first paper where the Kantorovich-Rubinstein distance is investigated. The works of Barbour [2], Barbour and Brown [4] and the last chapter of the monograph [8] of Barbour, Holst and Janson concern Poisson process approximation in the total variation distance. But since the total variation distance is not suitable for all problems and since the so-called Stein magic factors do not get small if L n ( Y ) is large (in contrast to classical Poisson approximation), one often uses weaker notions of distance. Starting with the work of Barbour and Brown [4] and Barbour, Holst and Janson [8], this has been done by Brown, Chen, Schuhmacher, Weinberg and Xia [11-13, 15, 39, 40, 42]. Our work goes in the opposite direction since the Kantorovich-Rubinstein distance between point processes is stronger than the total variation distance in the sense that convergence in Kantorovich-Rubinstein distance implies convergence in total variation distance, but not vice versa. Roughly speaking and in a transferred sense, the Kantorovich-Rubinstein distance is related to the total variation distance between point processes as the Wasserstein distance is related to the total variation distance for integer-valued random variables. Since its test functions are allowed to take values other than zero and one, the Kantorovich-Rubinstein distance is more sensitive to the behavior and the geometry of the compared point processes than the total variation distance. Let us further remark that in the recent paper [41], Schuhmacher and Stucki consider the total variation distance between two Gibbs processes. This includes Poisson process approximation as a special case. However, the approximated point processes of the present paper do not, in general, satisfy the technical conditions assumed in [41] since they are not necessarily hereditary.


<!-- p:4 -->


Besides the notion of distance and its connection to the theory of optimal transportation, the other main ingredient of our approach is a functional version of Stein's method for Poisson process approximation. It relies on a Glauber dynamics representation for Poisson processes and the Malliavin formalism. More precisely, we use an integration-by-parts argument on the target space and then a commutation relation between the discrete gradient on that space and the semi-group associated with the Glauber dynamics. This way we avoid the explicit computation and investigation of a solution of the Stein equation. We would like to highlight that our approach is generic and depends only on the underlying random structure (here, a binomial or a Poisson process) and not on a very specific model so that extensions to other probabilistic frameworks (such as Gaussian random measures or Rademacher sequences) should also be possible. However, they are beyond the scope of this paper and will be treated elsewhere.

To demonstrate the versatility of our new functional limit theorem, we consider probabilistic approximations of U-statistics over binomial or Poisson input processes. In a first regime, we consider the Poisson approximation of U-statistics and provide an error bound for the Wasserstein distance. Our result improves and extends earlier works of Barbour and Eagleson [7] and Peccati [32]. The second regime concerns compound Poisson approximation of U-statistics in total variation distance. Here, we do not impose any conditions on the nature of the compound Poisson distribution, which is allowed to be discrete or continuous. In contrast, previous results for the compound Poisson approximation via Stein's method only deal with the discrete case; see, for example, the work of Barbour, Chen and Loh [5], the survey [6] of Barbour and Chryssaphinou and especially the paper [21] of Eichelsbacher and Roos, who consider U-statistics over a binomial input process. In this light, we generalize the results of [21] to a larger class of limiting distributions and also to the case of an underlying Poisson process. In a third regime, we use our functional limit theorem to investigate probabilistic approximations of U-statistics by α -stable random variables with 0 &lt; α &lt; 1 and to derive explicit error bounds for the Kolmogorov distance. In their previous work [17], Dabrowski et al. also obtained α -stable limits for U-statistics from point process convergence results. However, their technique does not allow any conclusion about a rate of convergence.


<!-- p:5 -->


Finally, we apply our general result to problems arising in stochastic geometry. Random geometric graphs are one of the fundamental models of spatial stochastics; see [34], for example. We derive limit theorems for several U-statistics of random geometric graphs, where the limiting distributions are Poisson or compound Poisson, and show a new point process limit theorem for the midpoints of short edges. As further examples, we consider distance-power statistics with α -stable limit distributions, midpoints between nonintersecting Poisson m -flats which are close together and the diameter of random polytopes with vertices on the sphere.

In a natural way our paper continues the line of research on point process convergence and extreme values initiated by the second and the third author in [43, 44], where the proofs are based on the main result of [32] and the underlying point process has to be Poisson. In contrast to these previous works our technique also allows us to deal with an underlying binomial process and delivers in both cases bounds for the Kantorovich-Rubinstein distance. Furthermore, the bounds derived here improve the rates of convergence of some of the scalar limit theorems from [43, 44]. Our findings also complement the works [19] and [20] of the first author with Joulin and Savy, concerning the Kantorovich-Rubinstein distance on configuration spaces and related notions.

This paper is organized as follows. Before we present our main result for Poisson process convergence in Section 3, we recall in Section 2 some necessary notation and results about point processes and also summarize some facts from convex geometry which are important for our examples from stochastic geometry. The proof of our main result in Section 6 is prepared by a brief discussion of the underlying Stein principle in Section 4 and the Glauber dynamics, a key step in our argument, in Section 5. Section 7 is devoted to applications of our functional limit theorem to probabilistic approximations of U-statistics and to problems from stochastic geometry.

## Preliminaries. In the present section we introduce some basic notions and notation, which are used in the text. Throughout, (Ω , F , P ) will be an abstract probability space, which is rich enough to carry all the random objects we deal with. Expectation with respect to P is denoted by E .
### Configuration spaces. Let ( Y , Y ) be a lcscH space; that is, Y is a topological space with countable base such that every point in Y has a compact neighborhood and such that any two points of Y can be separated by disjoint neighborhoods. Such a space is separable and completely metrizable. Here, Y denotes the Borel σ -field generated by the topology of Y . By N Y we


<!-- p:6 -->


denote the space of σ -finite counting measures (i.e., point configurations) on Y , whereas  ̃ N Y and ̂ N Y stand for the sets of all locally finite (i.e., bounded on all relatively compact sets) and finite counting measures on Y , respectively. By a slight abuse of notation we will write y ∈ ω if y ∈ Y is charged by the measure ω and also use the set-notation ω 1 ⊂ ω 2 to indicate that ω 1 is a sub-configuration of ω 2 (with a similar meaning we also understand ω 2 \ ω 1 ). Let N Y be the σ -field on N Y generated by the mappings

$$\psi _ { A } \colon N _ { \mathbb { Y } } \to \mathbb { N } _ { 0 } \cup \{ \infty \} , & & \omega \mapsto \omega ( A ) , A \in \mathcal { Y } , \\ \intertext { b y } \mathbb { N } _ { A } + ( o ) \ \colon & & - 1 + 1 , \quad 0 \leq c + 1 , \quad 0 \leq i + 1 , \quad i + 1 \colon \quad 0 \leq i + 1 ,$$

where N 0 := N ∪{ 0 } is the set of natural numbers including zero. We equip  ̃ N Y and ̂ N Y with the corresponding trace σ -fields of N Y . The σ -field of  ̃ N Y is then the Borel σ -field for the vague topology on  ̃ N Y , which is generated by the mappings

where g ≥ 0 is a continuous function on Y with compact support, and the space  ̃ N Y equipped with the vague topology becomes a Polish space; see Theorem A2.3 in [24]. A point process (or random counting measure) μ is a random element in N Y . By a locally finite point process and a finite point process, we mean random elements in  ̃ N Y and ̂ N Y , respectively. It follows from [38], Lemma 3.1.3, that a point process μ can almost surely be represented as

$$g s & & \\ & e _ { g } \colon \widetilde { N } _ { \mathbb { W } } \rightarrow [ 0 , \infty ) , & \quad \omega \mapsto \int _ { \mathbb { Y } } g \, d \omega , \\ & a \, \text {continuous function on } \mathbb { Y } \text { with compact sur }$$

$$\mu = \sum _ { i = 1 } ^ { \mu ( \mathbb { Y } ) } \delta _ { x _ { i } } \quad \text {with } x _ { i } \in \mathbb { Y } , i \in \mathbb { N } \text { and } \mu ( \mathbb { Y } ) \in \mathbb { N } _ { 0 } \cup \{ \infty \} , \\$$

where δ y stands for the unit mass Dirac measure concentrated at y ∈ Y . Thus we may interpret μ also as a random collection of points, taking into account potential multiplicities.

2.2. Poisson processes. Let M be a σ -finite measure on Y , and let M k stand for its k -fold product measure. By a Poisson process on Y with intensity measure M , we understand a point process ζ with the properties that: (i) for any B ∈ Y , the random variable ζ ( B ) is Poisson distributed with mean M ( B ) and (ii) ζ is independently scattered; that is, for any n ∈ N and disjoint B 1 , . . . , B n ∈Y the random variables ζ ( B 1 ) , . . . , ζ ( B n ) are independent. We notice that if M is a finite measure, ζ charges almost surely only a finite number of points in Y , whose total number follows a Poisson distribution with mean M ( Y ). We will write P ζ for the distribution of ζ on N Y . In this paper we will speak about a homogeneous Poisson process on a set A ∈ B ( R d ), where B ( R d ) is the Borel σ -field on R d , if the intensity measure is a multiple of the restriction of the Lebesgue measure to A .


<!-- p:7 -->


Also, if d =1, a homogeneous Poisson process ζ on [0 , ∞ ) can be thought of as a piecewise deterministic (pure jump) stochastic process in continuous time, starting at zero and having jumps of size one and i.i.d. exponentially distributed waiting times between the jumps. The points of discontinuity of this random process are the jump times of ζ .

One of our main tools to deal with Poisson functionals (by these we mean real-valued random variables depending only on a Poisson process) is the multivariate Mecke formula [38], Corollary 3.2.3, which says that for any integer k ≥ 1 and any measurable and nonnegative f : Y k × N Y → R ,

̸

$$integer & \geq 1 \text { and any measurable and nonnegative } f \colon \mathbb { Y } ^ { k } \times \mathbb { N } _ { \mathbb { Y } } \to \mathbb { R } , \\ & \quad \sum _ { ( y _ { 1 } , \dots , y _ { k } ) \in \mathcal { K } } f ( y _ { 1 } , \dots , y _ { k } , \zeta ) \\ & \quad ( 2 . 1 ) \\ & = \int _ { \mathbb { Y } ^ { k } } E f ( y _ { 1 } , \dots , y _ { k } , \zeta + \delta _ { y _ { 1 } } + \dots + \delta _ { y _ { k } } ) M ^ { k } ( d ( y _ { 1 } , \dots , y _ { k } ) ) , \\ \intertext { w h e r e } & \text { } \zeta \text { is the collection of all } k \text { tuples of distinct points charged by } \zeta \text { .}$$

̸

where ζ k = is the collection of all k -tuples of distinct points charged by ζ . If the point process ζ is simple [i.e., if ζ ( { y } ) ∈ { 0 , 1 } almost surely for any y ∈ Y ], ζ k = can be written as

̸

while in the nonsimple case distinct points can have the same location. We remark that (2.1) with k =1 is even a characterizing property of the Poisson process ζ ; cf. Theorem 3.2.5 of [38].

̸

$$\zeta _ { \neq } ^ { k } = \{ ( y _ { 1 } , \dots , y _ { k } ) \in \mathbb { Y } ^ { k } \colon y _ { i } \neq y _ { j } \in \zeta \text { for } i \neq j , i , j = 1 , \dots , k \} , \\ \ m u i _ { j } \colon _ { i j } \ t h a r p s a r i m { 1 } _ { k } \colon _ { j } \ s p a r s a t i m { t } _ { k } \colon _ { j } \ s p a r s a t i m { 1 } _ { k } \colon _ { j } \ s p a r s a t i m { 1 } _ { k } .$$

̸

$$b i n o m i a l { p r e s } & \text {reads as follows:} \\ & \text {E} \quad \sum _ { ( y _ { 1 } , \dots , y _ { k } ) \in \beta _ { n } ^ { k } , } f ( y _ { 1 } , \dots , y _ { k } , \beta _ { n } ) \\ & ( 2 . 2 ) \\ & = ( n ) _ { k } \int _ { \mathbb { Y } ^ { k } } E f ( y _ { 1 } , \dots , y _ { k } , \beta _ { n - k } + \delta _ { y _ { 1 } } + \cdots + \delta _ { y _ { k } } ) M _ { 1 } ^ { k } ( d ( y _ { 1 } , \dots , y _ { k } ) ) , \\ & \text {where } ( n ) _ { k } \coloneqq n ( n - 1 ) \cdots ( n - k + 1 ) \text { is the descending factorial and } f \text { is a }$$

̸


2.3. Binomial processes. Let M 1 be a probability measure on Y . A binomial process with intensity measure M := n M 1 , n ∈ N, is a collection of n random points, distributed independently according to the measure M 1 . This process also arises by conditioning a Poisson process with intensity measure M on having exactly n points. In this paper we shall denote the random counting measure induced by such a binomial process by β n . We also write β k n, = to indicate the collection of all k -tuples of distinct points charged by β n . Then the counterpart to the multivariate Mecke formula (2.1) for a binomial process reads as follows:

̸

where ( n ) k := n ( n - 1) · · · ( n - k +1) is the descending factorial and f is a real-valued nonnegative measurable function on Y k × N Y . This can easily be seen directly and is also a special case of the Georgii-Nguyen-Zessin formula, for which we refer to [18], Proposition 15.5.II.


<!-- p:8 -->


2.4. Probability distances. In order to compare two real-valued random variables Y 1 and Y 2 (or more precisely their distributions) and to measure their closeness, we use several probability distances in this paper. The Kolmogorov distance of Y 1 and Y 2 is given by

$$d _ { K } ( Y _ { 1 } , Y _ { 2 } ) \colon = \sup _ { z \in \mathbb { R } } | P ( Y _ { 1 } \leq z ) - P ( Y _ { 2 } \leq z ) | ,$$

while the total variation distance is

$$d _ { T V } ( Y _ { 1 } , Y _ { 2 } ) \colon = \sup _ { A \in \mathcal { B } ( \mathbb { R } ) } | P ( Y _ { 1 } \in A ) - P ( Y _ { 2 } \in A ) | ,$$

where, recall, B ( R ) stands for the Borel σ -field on R . If Y 1 and Y 2 are integervalued random variables, we can re-write their total variation distance as

$$d _ { T V } ( Y _ { 1 } , Y _ { 2 } ) = \frac { 1 } { 2 } \sum _ { k \in \mathbb { Z } } | P ( Y _ { 1 } = k ) - P ( Y _ { 2 } = k ) | .$$

Let us denote by Lip(1) the set of all functions h : R → R whose Lipschitz constant is at most one and define the Wasserstein distance of two realvalued random variables Y 1 and Y 2 by

$$d _ { W } ( Y _ { 1 } , Y _ { 2 } ) \coloneqq \sup _ { h \in L i p ( 1 ) } | E h ( Y _ { 1 } ) - E h ( Y _ { 2 } ) | .$$

These probability distances all have the property that they imply convergence in distribution, meaning that for a sequence ( Y n ) n ∈ N of random variables convergence in distribution to another random variable Y is implied by

- d I ( Y n , Y ) → 0 as n →∞ , for some I ∈{ K , TV , W } . (2.3)

Moreover, for integer-valued random variables Y 1 and Y 2 , let us mention the general inequality

$$d _ { K } ( Y _ { 1 } , Y _ { 2 } ) & \leq d _ { T V } ( Y _ { 1 } , Y _ { 2 } ) \leq d _ { V } ( Y _ { 1 } , Y _ { 2 } ) , \\ \intertext { ( 2 . 4 ) } 1 \colon 1 \colon & \quad 1 \cdot 1 \cdot 1 \cdot 1 \cdot 1 \cdot 1 \cdot 1 \cdot 1 \cdot 1 \cdot 1 \cdot 1 \cdot 1 \cdot 1 \cdot 1 \cdot 1 \cdot 1 \cdot 1 \cdot 1 \cdot 1 \cdot 1 \cdot 1 \cdot 1$$

which directly follows from the definitions of the involved probability distances and the fact that Y 1 and Y 2 are concentrated on the integers. Note that (2.4) does not remain valid for general real-valued random variables.

2.5. Kantorovich-Rubinstein distance. We define the total variation distance between two measures ν 1 and ν 2 on Y by

$$d _ { T V } ( \nu _ { 1 } , \nu _ { 2 } ) \colon = \sup _ { \substack { A \in \mathcal { Y } \\ \nu _ { 1 } ( A ) , \nu _ { 2 } ( A ) < \infty } } | \nu _ { 1 } ( A ) - \nu _ { 2 } ( A ) | ,$$

a notion that should not be confused with the total variation distance between random variables introduced above. Note that d TV ( ν 1 , ν 2 ) can in principle take any value in [0 , ∞ ].


<!-- p:9 -->


We say that a map h :  ̃ N Y → R is 1-Lipschitz if | h ( ω 1 ) - h ( ω 2 ) | ≤ d TV ( ω 1 , ω 2 ) for all ω 1 , ω 2 ∈  ̃ N Y , and denote by L 1 the set of all these maps which are measurable.

The Kantorovich-Rubinstein distance between two probability measures Q 1 and Q 2 on N Y is defined as the optimal transportation cost

$$Q _ { 1 } \text { and } Q _ { 2 } \text { on } N _ { \mathbb { Y } } \text { is defined as the optimal transportation cost } \\ ( 2 . 5 ) \quad \text {d} _ { K R } ( Q _ { 1 } , Q _ { 2 } ) \coloneqq \inf _ { C \in \Sigma ( Q _ { 1 } , Q _ { 2 } ) } \int _ { N _ { Y } \times N _ { Y } } d _ { T V } ( \omega _ { 1 } , \omega _ { 2 } ) C ( d ( \omega _ { 1 } , \omega _ { 2 } ) )$$

for the cost function d TV ( · , · ), where Σ( Q 1 , Q 2 ) denotes the set of probability measures on N Y × N Y with first marginal Q 1 and the second marginal Q 2 (i.e., couplings of Q 1 and Q 2 ). If Q 1 and Q 2 are concentrated on  ̃ N Y , there is at least one coupling C ∈ Σ( Q 1 , Q 2 ) for which the infimum in (2.5) is attained according to [46], Theorem 4.1, and the Kantorovich duality theorem [46], Theorem 5.10, says that this minimum equals

where the supremum is over all h ∈ L 1 that are integrable with respect to Q 1 and Q 2 .

$$[ 6 ] , \, \text {Theorem 5.10, says that this minimum equals} \\ ( 2 . 6 ) \quad \text {dkR} ( Q _ { 1 } , Q _ { 2 } ) = \sup \Big | \int _ { \widetilde { N } _ { Y } } h ( \omega ) Q _ { 1 } ( d \omega ) - \int _ { \widetilde { N } _ { Y } } h ( \omega ) Q _ { 2 } ( d \omega ) \Big | , \\ \text {where the supremum is over all } h \in \mathcal { L } _ { 1 } \text { that are integrable with respect to } Q _ { 1 } \text { and } Q _ { 2 } .$$

By abuse of notation we will also write d KR ( ζ n , ζ ) instead of d KR ( Q n , Q ) if the point process ζ n on Y has distribution Q n for any n ≥ 1 and the point process ζ on Y has distribution Q . Note that the integrability condition in (2.6) is automatically fulfilled for all h ∈ L 1 if E ζ n ( Y ) &lt; ∞ and E ζ ( Y ) &lt; ∞ . The Kantorovich-Rubinstein distance is also called Wasserstein distance, Monge-Kantorovich distance or Rubinstein distance. For a detailed discussion of the terminology we refer to the bibliographic notes of Chapter 6 in [46].

The following result ensures that convergence of locally finite point processes in Kantorovich-Rubinstein distance implies convergence in distribution.

Proposition 2.1. Assume that ( ζ n ) n ∈ N is a sequence of locally finite point processes on Y and that ζ is another locally finite point process on Y such that d KR ( ζ n , ζ ) → 0 , as n →∞ . Then ζ n converges in distribution to ζ , as n →∞ .

Proof. The structure of the vague topology on  ̃ N Y implies that it is necessary and sufficient to prove that for any continuous g : Y → R with compact support, the random variables ∫ g d ζ n converge in distribution to ∫ g d ζ ; see [24], Theorem 16.16. By (2.3), it is sufficient to show that for all Borel sets B ⊂ R , we have that

$$\mathbf E e _ { g , B } ( \zeta _ { n } ) \rightarrow \mathbf E e _ { g , B } ( \zeta ) \quad \text {as $n\to\infty$,}$$


<!-- p:10 -->


where e g,B :  ̃ N Y → R , ω ↦→ 1 ( ∫ g d ω ∈ B ). To show this, we notice that for each g and B as above the mapping e g,B belong to L 1 , whence

$$| E e _ { g , B } ( \zeta _ { n } ) - E e _ { g , B } ( \zeta ) | \leq d _ { K R } ( \zeta _ { n } , \zeta ) , \\$$

and the result follows. □

An alternative distance to measure the closeness of two point processes ζ 1 and ζ 2 on Y is the total variation distance

$$d _ { T V } ( \zeta _ { 1 } , \zeta _ { 2 } ) \colon = \sup _ { A \in \mathcal { N } _ { Y } } | \mathbf P ( \zeta _ { 1 } \in A ) - \mathbf P ( \zeta _ { 2 } \in A ) | .$$

It is always dominated by the Kantorovich-Rubinstein distance since

$$It is always dominated by the Kantorovich Rubinstein distance since \\ d _ { T V } ( \zeta _ { 1 } , \zeta _ { 2 } ) & = \sup _ { A \in \mathcal { N } _ { Y } } \inf _ { C \in \Sigma ( \zeta _ { 1 } , \zeta _ { 2 } ) } \int _ { N _ { Y } \times N _ { Y } } 1 ( \omega _ { 1 } \in A ) - 1 ( \omega _ { 2 } \in A ) C ( d ( \omega _ { 1 } , \omega _ { 2 } ) ) \Big | \\ & \leq \inf _ { C \in \Sigma ( \zeta _ { 1 } , \zeta _ { 2 } ) } \int _ { N _ { Y } \times N _ { Y } } d _ { T V } ( \omega _ { 1 } , \omega _ { 2 } ) C ( d ( \omega _ { 1 } , \omega _ { 2 } ) ) = d _ { K R } ( \zeta _ { 1 } , \zeta _ { 2 } ) . \\ \intertext { The following example shows that convergence in Kantorovich Rubinstein }$$

The following example shows that convergence in Kantorovich-Rubinstein distance is strictly finer than convergence in total variation distance.

Example 2.2. Let ζ be a Poisson process on Y with finite intensity measure M . Let ( X i ) i ∈ N be a sequence of independent random elements in Y with distribution M ( Y ) - 1 M ( · ) and let Z be a Bernoulli random variable such that P ( Z =1) = p for some p ∈ (0 , 1). Moreover, assume that ζ , ( X i ) i ∈ N and Z are independent. Now we consider the point process

$$\zeta _ { n , p } \coloneqq \zeta + 1 ( Z = 1 ) \sum _ { i = 1 } ^ { n } \delta _ { X _ { i } } .$$

Since ζ and ζ n,p coincide on an event with probability 1 - p , we have that d TV ( ζ, ζ n,p ) ≤ p . By taking h ( μ ) = μ ( Y ) as a test function in (2.6), we deduce that d KR ( ζ, ζ n,p ) ≥ np . Taking p n =1 / √ n for p shows that

$$d _ { T V } ( \zeta , \zeta _ { n , p _ { n } } ) \to 0 \quad \text {and} \quad \text {d} _ { K R } ( \zeta , \zeta _ { n , p _ { n } } ) \to \infty \quad \text {as } n \to \infty , \\ + 1 \, \underset { n } { ( \ast } \, ( \zeta _ { n , p _ { n } } ) \, \to 0 \quad \text {and} \quad \text {d} _ { K R } ( \zeta , \zeta _ { n , p _ { n } } ) \to \infty \\$$

so that ( ζ n,p n ) n ∈ N converges to ζ in total variation distance but not in Kantorovich-Rubinstein distance.

̸

In the previous example the Kantorovich-Rubinstein distance is more strongly affected by the rare event that ζ = ζ n,p n than the total variation distance, since the class of test functions is larger and contains functions taking also values different from zero and one. As already mentioned in the Introduction, one can say that the difference between the KantorovichRubinstein distance and the total variation distance for point processes is similar to the difference between the Wasserstein and the total variation distance for integer-valued random variables. As particular example we cite the work of Barbour and Xia [10], where Poisson approximation of random variables with respect to the Wasserstein distance has been considered, extending previous results for the total variation distance; see also Section 7.1 below.


<!-- p:11 -->


2.6. A discrete gradient. For a counting measure ω ∈  ̃ N Y and a measurable function h :  ̃ N Y → R , let us introduce the discrete gradient in direction y ∈ Y by

$$D _ { y } h ( \omega ) \colon = h ( \omega + \delta _ { y } ) - h ( \omega ) , \\ \quad \ \ s _ { y } \cdot \dot { \omega } _ { y } = \dot { \omega } ( \omega ) - \dot { h } ( \omega ) ,$$

where we recall that δ y is the unit-mass Dirac measure charging y ∈ Y . In our notation we often suppress the dependence of D y h ( ω ) on the underlying counting measure ω and write D y h . Clearly, if h ∈ L 1 , it holds that | D y h | ≤ 1 for all y ∈ Y .

2.7. Geometric preparations. For our applications in Section 7, we need some facts from convex geometry. The Euclidean norm in R d is denoted by ‖ · ‖ . The Euclidean distance between two sets A 1 , A 2 ⊂ R d is given by

$$\text {dist} ( A _ { 1 } , A _ { 2 } ) = \inf \{ \| x _ { 1 } - x _ { 2 } \| \colon x _ { 1 } \in A _ { 1 } , x _ { 2 } \in A _ { 2 } \} . \\ \{ \ \cdot \, \cdot \, \cdot \, \cdot \, \pi \mathbb { d } \quad \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \, \cdot \,$$

If A 1 = { x } with x ∈ R d , we write dist( x, A 2 ) instead of dist( { x } , A 2 ). For a measurable set K ⊂ R d , we write vol( K ) for the volume (i.e., d -dimensional Lebesgue measure) of K . For the volume of the unit ball B d = { x ∈ R d : ‖ x ‖ ≤ 1 } in R d , we introduce the abbreviation κ d := vol( B d ). More generally, B d ( x, r ) will denote the closed d -dimensional ball of radius r &gt; 0 centered at x ∈ R d , and we write B d ( r ) instead of B d (0 , r ) for short. For r ≥ 0, the Minkowski sum K r = K + rB d of K and rB d is the so-called r -parallel set of K . In particular, if K is a convex set with nonempty interior, Steiner's formula (see, e.g., [38], equation (14.5)) says that the volume vol( K r ) is a polynomial of degree d in r . Formally,

$$( 2 . 7 ) & & \text {vol} ( K _ { r } ) = \sum _ { i = 0 } ^ { d } \kappa _ { d - i } V _ { i } ( K ) r ^ { d - i } .$$

̸

For 1 ≤ m ≤ d - 1, we denote in this paper by G d m the space of m - dimensional linear subspaces and by A d m the space of m -dimensional affine subspaces of R d . For L,M ∈ G d m let [ L,M ] be the subspace determinant of

The coefficients V 0 ( K ) , . . . , V d ( K ) are the so-called intrinsic volumes of K , especially V 0 ( K ) = 1 whenever K = ∅ , V 1 ( K ) is a constant multiple of the mean width of K , V d - 1 ( K ) is half of the surface area of K (if K is the closure of its interior) and V d ( K ) = vol( K ); cf. [38], Chapter 14.2.


<!-- p:12 -->


L and M , that is, the 2 m -volume of a parallelepiped spanned by two orthonormal bases in L and in M . In one of our examples, we will also deal with the integrated subspace determinant, and for this reason we recall that

$$& \text {with the integrated subspace determined, and for this reason we recorr} \\ & ( 2 . 8 ) & \int _ { \mathbb { G } _ { m } ^ { d } } \int _ { \mathbb { G } _ { m } ^ { d } } [ L , M ] \, d L \, d M = \frac { \binom { d - m } { m } } { \binom { d } { m } } \frac { \kappa _ { d - m } ^ { 2 } } { \kappa _ { d } \kappa _ { d - 2 m } } \\ & \text {from [23], Lemma 4.4. Here, } d L \text { and } d M \text { indicate integration with }$$

from [23], Lemma 4.4. Here, d L and d M indicate integration with respect to the unique Haar probability measure on G d m .

## 3. Main results.

3.1. General estimate. Let ( Y , Y ) be a lcscH space, and let us fix another lcscH space ( X , X ). We adopt the notation introduced in Section 2 and denote by N X the space of σ -finite counting measures on X .

Let μ be a point process on X with a σ -finite intensity measure K ( · ) := E μ ( · ). Fix an integer k ≥ 1, and let f : dom f → Y be a symmetric and measurable function, where dom f is a symmetric subset of X k ; that is, if ( x 1 , . . . , x k ) ∈ dom f , then ( x σ (1) , . . . , x σ ( k ) ) ∈ dom f for all permutations σ of { 1 , . . . , k } . We now apply f to all k -tuples of distinct points of μ contained in dom f to form a point process ξ , that is,

$$\xi \colon = \frac { 1 } { k ! } \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { \nmid } ^ { k } \cap \text {dom} } \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } .$$

̸

Since f is symmetric, every f ( x 1 , . . . , x k ) also appears for the k ! permutations of the argument ( x 1 , . . . , x k ). However, for each subset { x 1 , . . . , x k } ⊂ μ of distinct points of μ , we assign to f ( x 1 , . . . , x k ) only multiplicity one as can be seen from the above definition of ξ . However, ξ might still have points of multiplicity greater than one if there are different combinations of k points in X that are mapped under f to the same point in Y . The intensity measure of ξ is denoted by L and is given by

$$0 & \text { of } \xi \text { is denoted by } L \text { and is given by } \\ & L ( A ) = E \xi ( A ) = E \sum _ { y \in \xi } 1 ( y \in A ) \\ & = \frac { 1 } { k ! } E \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { \neq } ^ { k } \cap \text {dom} f } 1 ( f ( x _ { 1 } , \dots , x _ { k } ) \in A ) , \quad A \in \mathcal { Y } . \\ & \text {In what follows, we consider for } \mu \text { two different types of point processes}$$

̸

In what follows, we consider for μ two different types of point processes, namely Poisson processes and binomial processes. By η we denote a Poisson process on X with a σ -finite intensity measure K . By β n we denote a binomial process of n ∈ N points in X , which are independent and identically distributed in X according to a probability measure K 1 on X . Such a binomial process β n has intensity measure K := n K 1 . Now the multivariate Mecke formula (2.1) and its binomial analogue (2.2) imply that the intensity measure L of ξ is given by


<!-- p:13 -->


$$\L l a c { \L l a c { \L l a c { \L l a c { \L l a c { \L l a c { \L l a c { x } } } } } } } { \L l a c { \L l a c { x } } } & \text {given by} \\ ( 3 . 1 ) & \ \L l ( A ) = \frac { 1 } { k ! } \int _ { \text {dom} } 1 ( f ( x _ { 1 } , \dots , x _ { k } ) \in A ) K ^ { k } ( \text {d} ( x _ { 1 } , \dots , x _ { k } ) ) , \quad A \in \mathcal { Y } ,$$

in the Poisson case and by

$$& \quad \text {in} \, \ A ( x _ { 0 } \subsetneq \partial x _ { 0 } \subsetneq \partial y ) \\ & \quad ( 3 . 2 ) \, \ L ( A ) = \frac { ( n ) _ { k } } { k ! } \int _ { \text {dom} } 1 ( f ( x _ { 1 } , \dots , x _ { k } ) \in A ) K _ { 1 } ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) , \quad A \in \mathcal { Y } ,$$

if we start with a binomial process. (To deal with both cases simultaneously we use the same notation for both set-ups.) Let us finally introduce r (dom f ) for k ≥ 2 by

$$r ( \dom f ) \\ \vdots = \max _ { 1 \leq \ell \leq k - 1 } \int _ { \mathbb { X } ^ { \ell } } \left ( \int _ { \mathbb { X } ^ { k - \ell } } 1 ( ( x _ { 1 } , \dots , x _ { k } ) \in \text {dom} \, f ) K ^ { k - \ell } ( d ( x _ { \ell + 1 } , \dots , x _ { k } ) ) \right ) ^ { 2 } \\ \times K ^ { \ell } ( d ( x _ { 1 } , \dots , x _ { \ell } ) ) , \\ \intertext { a n d , for $ k = 1 , \, p u t \, r ( \text {dom} \, f ) \colon = 0 . \, M o r e v o r , \, w e u s e \, the c o n v e n t i o n \, t h a r r e d }$$

and, for k = 1, put r (dom f ) := 0. Moreover, we use the convention that ( n - k ) k / ( n ) k := 0 if n &lt; k .

We can now state our main result, a functional limit theorem, which provides a bound on the Kantorovich-Rubinstein distance between ξ and a suitable Poisson process on Y .

Theorem 3.1. Let ζ be a Poisson process on Y with finite intensity measure M . If ξ is induced by the Poisson process η , then

$$d _ { K R } ( \xi , \zeta ) & \leq d _ { T V } ( L , M ) + 2 ( E \xi ( \mathbb { Y } ) ^ { 2 } - E \xi ( \mathbb { Y } ) - ( E \xi ( \mathbb { Y } ) ) ^ { 2 } ) \\ & \leq d _ { T V } ( L , M ) + \frac { 2 ^ { k + 1 } } { k ! } r ( \text {dom} \, f ) .$$

If otherwise ξ is derived from the binomial process β n , then

$$If \text {otherwise} \, \xi \text { is derived from the binomial process } \beta _ { n } , \text { then} \\ \text {d} _ { \text {KR} } ( \xi , \zeta ) \leq d _ { \text {TV} } ( L , M ) + 2 \left ( E \xi ( \mathbb { Y } ) ^ { 2 } - E \xi ( \mathbb { Y } ) - \frac { ( n - k ) _ { k } } { ( n ) _ { k } } ( E \xi ( \mathbb { Y } ) ) ^ { 2 } \right ) \\ + \frac { 6 ^ { k } k ! } { n } ( E \xi ( \mathbb { Y } ) ) ^ { 2 } \\ \leq d _ { \text {TV} } ( L , M ) + \frac { 2 ^ { k + 1 } } { k ! } r ( \text {dom} \, f ) + \frac { 6 ^ { k } k ! } { n } L ( \mathbb { Y } ) ^ { 2 } .$$


<!-- p:14 -->


Remark 3.2. (i) If the underlying point process is a binomial process β n with n points and if n &lt; k , the point process ξ is empty with probability one and L ≡ 0. In this case, d KR ( ξ, ζ ) ≤ E ζ ( Y ) = d TV ( L , M ), and the bound on d KR ( ξ, ζ ) is trivially valid. For this reason, no further restriction on n is necessary.

(ii) In the Poisson case, it can happen that L ( Y ) = ∞ . In this case, we have d TV ( L , M ) = ∞ , and the bound (3.3) is trivial. Hence Theorem 3.1 is only of interest if L ( Y ) &lt; ∞ , which is equivalent to K k (dom f ) &lt; ∞ , a condition which ensures that ξ is almost surely finite.

- (iii) Taking M = L in the Poisson case in Theorem 3.1 shows that

$$d _ { K R } ( \xi , \zeta ) & \leq 2 ( E \xi ( \mathbb { Y } ) ^ { 2 } - E \xi ( \mathbb { Y } ) - ( E \xi ( \mathbb { Y } ) ) ^ { 2 } ) \leq \frac { 2 ^ { k + 1 } } { k ! } r ( \text {dom} \, f ) . \\$$

In particular, if k = 1, this gives d KR ( ξ, ζ ) = 0, which in view of Proposition 2.1 implies that ξ is a Poisson process. This is consistent with the well-known mapping theorem for Poisson processes, for which we refer to [25], Chapter 2.3.

(iv) If X = Y and f : X → X is the identity, Theorem 3.1 yields that, for Poisson processes ξ and ζ with finite intensity measures L and M , respectively,

### d KR ( ξ, ζ ) ≤ d TV ( L , M ) .

In other words, the Kantorovich-Rubinstein distance between two Poisson processes is bounded by the total variation distance of their intensity measures. For a similar estimate in a more restricted set-up we refer to [20], Proposition 4.1.

3.2. The Euclidean case. In this subsection we shall apply our general estimate of Theorem 3.1 to the important situation that the target space Y is R d endowed with the standard Borel σ -field B ( R d ). This is tailored toward some of our applications in Section 7 and is similar to the set-up in [43, 44]. We let ( X , X ) be a lcscH space and let ( η t ) t ≥ 1 be a family of Poisson processes in X with intensity measures K t = t K , t ≥ 1, where K is a fixed σ -finite measure. By ( β t ) t ≥ 1 we denote a family of binomial processes such that β t = β ⌈ t ⌉ , and β ⌈ t ⌉ is a process of ⌈ t ⌉ points chosen independently according to a fixed probability measure K 1 . In this situation we use the notation K t := ⌈ t ⌉ K . We write ( μ t ) t ≥ 1 in the sequel to indicate either ( η t ) t ≥ 1 or ( β t ) t ≥ 1 .

For a fixed integer k ≥ 1 we consider symmetric and measurable functions f t : X k → R d , t ≥ 1. We are interested in the behavior of the derived point processes

$$\xi _ { t } \coloneqq \frac { 1 } { k ! } \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { t , \neq } ^ { k } } \delta _ { f _ { t } ( x _ { 1 } , \dots , x _ { k } ) } , \quad t \geq 1 .$$

̸


<!-- p:15 -->


For this reason, we consider the re-scaled point processes

$$t ^ { \gamma } \bullet \xi _ { t } \colon = \frac { 1 } { k ! } \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { t , \neq } ^ { k } } \delta _ { t ^ { \gamma } f _ { t } ( x _ { 1 } , \dots , x _ { k } ) } , \quad t \geq 1 ,$$

̸

where γ ∈ R is a suitable constant. In order to compare t γ · ξ t with a Poisson process, we need to introduce the following notation. The intensity measure L t of the re-scaled point process t γ · ξ t is given by

̸

$$L _ { t } ( B ) \coloneqq \frac { 1 } { k ! } E \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { t , \neq } ^ { k } } 1 ( f _ { t } ( x _ { 1 } , \dots , x _ { k } ) \in t ^ { - \gamma } B ) , \quad B \in \mathcal { B } ( \mathbb { R } ^ { d } ) .$$

For B ∈B ( R d ) let r t ( B ) be given by r t ( B ) := 0 for k =1 and

$$\text {For $B\in\mathbb{B}(\mathbb{X}^{d})$ let $r_{t}(B)$ be given by $r_{t}(B)$ := 0 for $k\equiv 1$ and} \\ r _ { t } ( B ) \colon = \max _ { 1 \leq \ell \leq k - 1 } \int _ { \mathbb { X } ^ { \ell } } \left ( \int _ { \mathbb { X } ^ { \ell } } 1 ( f _ { t } ( x _ { 1 } , \dots , x _ { k } ) \in t ^ { - \gamma } B ) K _ { t } ^ { k - \ell } ( d ( x _ { \ell + 1 } , \dots , x _ { k } ) ) \right ) ^ { 2 } \\ \times K _ { t } ^ { \ell } ( d ( x _ { 1 } , \dots , x _ { \ell } ) ) \\ \intertext { f o r $ k > 2$ . F u r t h e r m o r e . for a measure $ V \in \mathbb { R } ^ { d } $ and $ B \in \mathcal { B } ( \mathbb { R } ^ { d } ) $ l e t $ | R | _ { B } \text { be the}$$

for k ≥ 2. Furthermore, for a measure ν on R d and B ∈B ( R d ) let ν | B be the restriction of ν to B .

Corollary 3.3. Let ζ be a Poisson process on R d with intensity measure M , and let B ∈ B ( R d ) be such that M ( B ) &lt; ∞ . If ξ t is induced by a Poisson process η t with t ≥ 1 , then

$$d _ { K R } ( ( t ^ { \gamma } \bullet \xi _ { t } ) | _ { B } , \zeta | _ { B } ) \\ \leq d _ { T V } ( L _ { t } | _ { B } , M | _ { B } ) + 2 ( E _ { \xi _ { t } } ( t ^ { - \gamma } B ) ^ { 2 } - E _ { \xi _ { t } } ( t ^ { - \gamma } B ) - ( E _ { \xi _ { t } } ( t ^ { - \gamma } B ) ) ^ { 2 } ) \\ \leq d _ { T V } ( L _ { t } | _ { B } , M | _ { B } ) + \frac { 2 ^ { k + 1 } } { k ! } r _ { t } ( B ) . \\ \intertext { f . e . is induced by a h i n o m i a l p r o c e s } \intertext { s . a . } \intertext { i . e . } \intertext { s . a . } \intertext { t h e r e } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . } \intertext { s . a . } \intertext { e f . }$$

If ξ t is induced by a binomial process β t with t ≥ 1 , then

$$If \xi _ { t } \text { is induced by a binomial process } \beta _ { t } \text { with } t \geq 1 , \text { then} \\ \text {d} \kappa ( ( t ^ { \gamma } \bullet \xi _ { t } ) | _ { B } , \zeta | _ { B } ) \\ \leq d _ { T V } ( L _ { t } | _ { B } , M | _ { B } ) \\ + 2 \left ( E \xi _ { t } ( t ^ { - \gamma } B ) ^ { 2 } - E \xi _ { t } ( t ^ { - \gamma } B ) - \frac { ( | t | - k ) _ { k } } { ( | t | ) _ { k } } ( E \xi _ { t } ( t ^ { - \gamma } B ) ) ^ { 2 } \right ) \\ + \frac { k ^ { k } ! } { t } ( E \xi _ { t } ( t ^ { - \gamma } B ) ) ^ { 2 } \\ \leq d _ { T V } ( L _ { t } | _ { B } , M | _ { B } ) + \frac { 2 ^ { k + 1 } } { k ! } r _ { t } ( B ) + \frac { 6 ^ { k } k ! } { t } L _ { t } ( B ) ^ { 2 } .$$


<!-- p:16 -->


Proof. This is a direct consequence of Theorem 3.1 with t γ · ξ t | B instead of ξ and ζ | B instead of ζ there. □

In view of limit theorems, the most natural choice for M is to take M as the strong limit of the measures L t , as t →∞ . That is,

$$M ( B ) & = \lim _ { t \to \infty } L _ { t } ( B ) \quad \text {for all $B\in\mathcal{B}(\mathbb{R}^{d})$} . \\$$

However, we emphasize that this does not necessarily imply that d TV ( L t , M ) → 0, as t →∞ , even though this is true for our applications presented below.

Remark 3.4. (i) The upper bounds in Corollary 3.3 are not uniform in the sense that they depend on the set B . This was to be expected since the re-scaled point processes t γ · ξ t can be finite for any t ≥ 1, while a realization of ζ can charge an infinite number of points (compare with our applications in Section 7). This is the reason for introducing the restriction to the set B , which allows us to compare t γ · ξ t | B with ζ | B using the KantorovichRubinstein distance.

(ii) To allow for an easier comparison with the previous paper [43], we remark that ibidem the Poisson case for d =1 is considered. Moreover, the intensity measure M there is concentrated on the positive real half-axis and has the form

$$\text { form } & & M ( B ) = a b \int _ { B } 1 ( u \geq 0 ) u ^ { b - 1 } \, d u , & B \in \mathcal { B } ( \mathbb { R } ) , \\ & & \text { } \\$$

for some constants a, b &gt; 0. In this case, the Poisson process ζ is a so-called Weibull process since the distance from the origin to the closest point of ζ is Weibull distributed with distribution function u ↦→ (1 - exp( - au b )) 1 ( u &gt; 0). We remark that this form of M was tailored to the applications in [43]; a more general version is stated without proof in [44].

(iii) Note that r t ( B ) is dominated by k ! L t ( B )ˆ r t ( B ), where ˆ r t ( B ) is defined as

$$\hat { r } _ { t } ( B ) \colon = \max _ { \substack { 1 \leq \ell \leq k - 1 , \\ ( x _ { 1 } , \dots , x _ { \ell } ) \in \mathbb { X } ^ { \ell } } } K _ { t } ^ { k - \ell } ( \{ ( y _ { 1 } , \dots , y _ { k - \ell } ) \in \mathbb { X } ^ { k - \ell } \colon \\$$

for B ∈B ( R d ). A quantity similar to ˆ r t ( B ) has also played a prominent role in the previous study [43]. In many applications a bound for ˆ r t ( B ) is already sufficient in order to apply Corollary 3.3. However, there are situations for which ˆ r t ( B ) is an increasing function in t , while r t ( B ) tends to zero, as t →∞ . This way [43], Theorem 1.1, in which ˆ r t instead of r t appears, is not applicable in such cases, as is erroneously done in Sections 2.5 and 2.6 ibidem. However, in these specific cases it is readily checked that r t behaves nicely, implying that the results there are correct.

$$( B ) \colon = \max _ { 1 \leq \ell \leq k - 1 , } \ K _ { t } ^ { k - \ell } ( \{ ( y _ { 1 } , \dots , y _ { k - \ell } ) \in \mathbb { X } ^ { k - \ell } \colon \\ ( x _ { 1 } , \dots , x _ { \ell } ) \in \mathbb { X } ^ { \ell } \\ f _ { t } ( x _ { 1 } , \dots , x _ { \ell } , y _ { 1 } , \dots , y _ { k - \ell } ) \in t ^ { - \gamma } B \} ) \\ B ( \mathbb { R } ^ { d } ) . \ A \text { quantity similar to } \hat { r } _ { t } ( B ) \text { has also played a prominent role}$$


<!-- p:17 -->


4. A general Stein principle. This section is devoted to a more informal discussion about the method of bounding the Kantorovich-Rubinstein distance between point processes using a Stein principle. This approach is the key argument of our proof of Theorem 3.1 in Section 6. Recall that the aim is to provide an upper bound for the Kantorovich-Rubinstein distance between a Poisson process ζ on a space Y with finite intensity measure M and a second point process ξ on Y , which in turn is derived from another point process μ on a space X by a transformation.

The first part of Stein's method consists of characterizing the target object, here the Poisson process ζ . The method is to consider a functional operator L which, at a formal level, satisfies for a finite point process ν the identity

$$& \quad \text {E} [ L F ( \nu ) ] = 0 \quad \text {for a large class of functions } F \colon \widehat { N } _ { \mathbb { Y } } \rightarrow \mathbb { R } \\ & \text {if and only if } \nu \text { is a Poisson process with intensity measure } M . \text { It is usually }$$

if and only if ν is a Poisson process with intensity measure M . It is usually not difficult to construct such an operator for a given target object. What may become challenging, especially in infinite dimensions (compare with [3, 16, 45]), will be to prove that the target object is the unique solution of (4.1). In our case, uniqueness follows from the theory of spatial birth-death processes; see [35].

The second step of Stein's method is to solve the so-called Stein equation,

$$& ( 4 . 2 ) & L F ( \omega ) = \mathbf E h ( \zeta ) - h ( \omega ) , \quad \omega \in \widehat { N } _ { \mathbb { Y } } , \\ & \text {for a certain class of test functions} \ h \colon \widehat { N } _ { \mathbb { Y } } \to \mathbb { R } . \ \text {This means that} \ w$$

A prominent way to do this is to use the so-called generator approach; see the survey article [36] and the references cited therein. The underlying idea is to interpret L as infinitesimal generator of a Markov process with the distribution of ζ as its invariant distribution, whence L satisfies (4.1). If ( P s ) s ≥ 0 is the semi-group associated with this Markov process, one can show that

for a certain class of test functions h : ̂ N Y → R . This means that we have to compute a solution F h for a given test function h and to evaluate LF h ( ω ).

$$\text {show that} & & L F _ { h } ( \omega ) = \int _ { 0 } ^ { \infty } L P _ { s } h ( \omega ) \, d s , \quad \omega \in \widehat { N } _ { \mathbb { Y } } . \\ & & \text {In order to compare the point process } \xi \text { with } \zeta , \text { we put } \omega = \xi \text { a}$$

In order to compare the point process ξ with ζ , we put ω = ξ and take expectations in (4.2) and (4.3). This leads to

$$E h ( \zeta ) - E h ( \xi ) = E L F _ { h } = E \int _ { 0 } ^ { \infty } L P _ { s } h ( \xi ) \, d s .$$

In the subsequent section, we will derive this identity rigorously. In the context of our main result, the point process ξ is induced by an underlying point process μ on another space X . More formally we have that ξ = T ( μ ), where T is a suitable transformation, that is, a mapping from N X to ̂ N Y . Hence we will have to compute


<!-- p:18 -->


$$\begin{matrix} \text {compute} \\ E \int _ { 0 } ^ { \infty } L P _ { s } h ( T ( \mu ) ) \, \text {d} s . \\ \end{matrix}$$

This expression is bounded in Section 6 by exploiting the special structure of the transformation T and the fact that μ is a Poisson or binomial process.

5. Glauber dynamics for the Poisson process. We now specialize the general scheme outlined in Section 4 to our particular situation. Although the approach is similar to [4], Section 2, for example, we prefer to carry out the details here since we consider a different class of test functions, namely Lipschitz functions instead of bounded functions. We assume the same set-up as for Theorem 3.1; that is, ζ is a Poisson process on a lcscH space Y with a finite intensity measure M and distribution P ζ . We now construct a Glauber dynamics for P ζ , that is a continuous-time Markov process ( G ( s )) s ≥ 0 with state space ̂ N Y and P ζ as its stationary (i.e., invariant) distribution; see [35]. Its generator L is given by

̂ where h : ̂ N Y → R is a measurable and bounded function. According to our notational convention, L may be re-written as

$$I s \, \text {generator} \, L \, \text {is given by} \\ L h ( \omega ) \colon = \int _ { \mathbb { Y } } h ( \omega + \delta _ { y } ) - h ( \omega ) M ( d y ) + \int _ { \mathbb { Y } } h ( \omega - \delta _ { y } ) - h ( \omega ) \omega ( d y ) , \\ ( 5 . 1 ) \\ \omega \in \widehat { N } _ { Y } , \\ \text {where} \, h \colon \widehat { N } _ { Y } \to \mathbb { R } \, \text { is a measurable and bounded function.  According to our}$$

$$\text {notational convention, } L \text { may be re-written as} \\ L h ( \omega ) = \int _ { \mathbb { Y } } h ( \omega + \delta _ { y } ) - h ( \omega ) \text {M} ( d y ) + \sum _ { y \in \omega } ( h ( \omega - \delta _ { y } ) - h ( \omega ) ) .$$

Note that Lh ( ω ) is well defined for all h ∈ L 1 and ω ∈ ̂ N Y since the Lipschitz property implies that the integrands in (5.1) are bounded by one. Moreover, we notice that the operator L uniquely determines the process ( G ( s )) s ≥ 0 , which has P ζ as its unique invariant distribution; see [18], Proposition 10.4.VII, or [35].

The Markov process ( G ( s )) s ≥ 0 is a spatial birth-death process in continuous time whose dynamics can be described as follows. If at time s , the system is in state ω s , each particle charged by ω s dies at rate 1, and a new particle is born at y with rate M (d y ). Alternatively, imagine a homogeneous Poisson process ζ b on R + with intensity M ( Y ). The jump times of ζ b determine the birth times of the particles in ζ . At each jump of ζ b a new particle is born and is placed in Y according to the distribution M ( · ) / M ( Y ), independently of the current configuration. Moreover, each particle has a lifetime which is exponentially distributed with parameter 1, independent of the past and of the rest of the configuration; see again [35].


<!-- p:19 -->


The semi-group ( P s ) s ≥ 0 associated with the Markov process ( G ( s )) s ≥ 0 is defined as

$$& P _ { s } h ( \omega ) = E [ h ( G ( s ) ) | G ( 0 ) = \omega ] , \quad \omega \in \widehat { N } _ { Y } , h \colon \widetilde { N } _ { \mathbb { Y } } \rightarrow \mathbb { R } . \\ & \text {For } h \in \mathcal { L } _ { 1 } \text { and } \omega \in \widehat { N } _ { \mathbb { Y } } \text { the conditional expectation is always well defined}$$

For h ∈ L 1 and ω ∈ ̂ N Y the conditional expectation is always well defined since

$$| P _ { s } h ( \omega ) | & = | E [ h ( G ( s ) ) | G ( 0 ) = \omega ] | \\ & \leq E [ | h ( G ( s ) ) - h ( \omega ) | | G ( 0 ) = \omega ] + | h ( \omega ) | \\ & \leq E [ d _ { T V } ( G ( s ) , \omega ) | G ( 0 ) = \omega ] + | h ( \omega ) | \\ & \leq E \zeta _ { b } ( [ 0 , s ] ) + \omega ( \mathbb { Y } ) + | h ( \omega ) | < \infty , \\ \text {re} \ \zeta _ { b } \text { is the homogeneous Poisson process from the description of}$$

where ζ b is the homogeneous Poisson process from the description of the birth-death dynamics above. Below we will need the following lemmas about the process ( G ( s )) s ≥ 0 and its semi-group ( P s ) s ≥ 0 . The first one provides a commutation relation between the discrete gradient and the semi-group.

Lemma 5.1. For any s ≥ 0 , ω ∈ ̂ N Y , y ∈ Y and h ∈ L 1 , D y P s h ( ω ) = e - s P s ( D y h )( ω ) .

Proof. To construct a sample path of ( G ( s )) s ≥ 0 , given the initial configuration G (0) = ω + δ y , we have to add the independent particle y to a realization of ( G ( s )) s ≥ 0 starting from the initial configuration ω . These two realizations will be identical after the particle y has died. Thus, denoting by l ( y ) the lifetime of y and using (5.2), we can write

$$D _ { y } P _ { s } h ( \omega ) & = \mathbf E [ h ( G ( s ) ) | G ( 0 ) = \omega + \delta _ { y } ] - \mathbf E [ h ( G ( s ) ) | G ( 0 ) = \omega ] \\ & = \mathbf E [ ( h ( G ( s ) + \delta _ { y } ) - h ( G ( s ) ) ) 1 ( \ell ( y ) \geq s ) | G ( 0 ) = \omega ] . \\$$

Since l ( y ) is independent of everything else and is exponentially distributed with mean one, we can continue with

$$D _ { y } P _ { s } h ( \omega ) & = \mathbf E [ 1 ( \ell ( y ) \geq s ) ] \mathbf E [ ( h ( G ( s ) + \delta _ { y } ) - h ( G ( s ) ) ) | G ( 0 ) = \omega ] \\ & = e ^ { - s } P _ { s } ( D _ { y } h ) ( \omega ) ,$$

where we have used (5.2) again. This completes the proof. □

Lemma 5.2. Let ω 1 , ω 2 ∈ ̂ N Y with ω 2 ⊂ ω 1 . If h ∈ L 1 and s ≥ 0 , then E [ h ( G ( s )) G (0) = ω ] E [ h ( G ( s )) G (0) = ω ] ( ω ω )( Y ) e - s .

$$| E [ h ( G ( s ) ) | G ( 0 ) = \omega _ { 1 } ] - E [ h ( G ( s ) ) | G ( 0 ) = \omega _ { 2 } ] | \leq ( \omega _ { 1 } \, \wedge \, \omega _ { 2 } ) ( \mathbb { Y } ) e ^ { - s } .$$


<!-- p:20 -->


Proof. Recall that each particle y of the initial configuration G (0) has an exponentially distributed lifetime l ( y ) with mean one. Thus since h ∈ L 1 , it holds that

$$it \text { holds that} \\ | E [ h ( G ( s ) ) | G ( 0 ) = \omega _ { 1 } ] - E [ h ( G ( s ) ) | G ( 0 ) = \omega _ { 2 } ] | \\ & \leq E \left [ \left | h \left ( G ( s ) + \sum _ { y \in \omega _ { 1 } \omega _ { 2 } } 1 ( \ell ( y ) \geq s ) \delta _ { y } \right ) - h ( G ( s ) ) \right | \left | G ( 0 ) = \omega _ { 2 } \right ] \\ & \leq E \left [ d _ { T V } \left ( G ( s ) + \sum _ { y \in \omega _ { 1 } \omega _ { 2 } } 1 ( \ell ( y ) \geq s ) \delta _ { y } , G ( s ) \right ) \right | G ( 0 ) = \omega _ { 2 } \right ] \\ & \leq E \sum _ { y \in \omega _ { 1 } \omega _ { 2 } } 1 ( \ell ( y ) \geq s ) \\ & = ( \omega _ { 1 } \, \omega _ { 2 } ) ( \Upsilon ) e ^ { - s } , \\ \text {which proves the claim.} \quad \square$$

which proves the claim. □

Lemma 5.3. For any ω ∈ N Y and h ∈ L 1 ,

$$F o r \ a n y \ \omega \in \widehat { N } _ { \mathbb { Y } } \ a n d \ h \in \mathcal { L } _ { 1 } , \\ \lim _ { s \to \infty } P _ { s } h ( \omega ) = E h ( \zeta ) = \int h \, d P _ { \zeta } .$$

Proof. We notice first that the expectation on the right-hand side is well defined since h ∈ L 1 implies that

$$E | h ( \zeta ) | & \leq E | h ( \zeta ) - h ( \varnothing ) | + | h ( \varnothing ) | \leq E d _ { T V } ( \zeta , \varnothing ) + | h ( \varnothing ) | \leq E \zeta ( \mathbb { Y } ) + | h ( \varnothing ) | \\ & = M ( \mathbb { Y } ) + | h ( \varnothing ) | , \\ \intertext { e x t . } \ w h o r o w \ \varnothing \text { stands for the 0-counting  measure} \, \ m o r u r o p n d o n s \ t o \, the o p n t y$$

where ∅ stands for the counting measure that corresponds to the empty point configuration.

From Lemma 5.2 with ω 1 = ω and ω 2 = ∅ , we have that

$$| E [ h ( G ( s ) ) | G ( 0 ) = \omega ] - E [ h ( G ( s ) ) | G ( 0 ) = \varnothing ] | \leq \omega ( \mathbb { Y } ) e ^ { - s } . \\$$

The number of particles of G ( s ) starting from the empty configuration follows the evolution of an M / M / ∞ queue with arrival (birth) rate M ( Y ) and service (death) rate 1, and thus is Poisson distributed with parameter (1 - e - s ) M ( Y ). Since the position of each of the particles is independent of everything else, G ( s ) has the same distribution as a Poisson process on Y with intensity measure (1 - e - s ) M . Since ζ has the same distribution as the superposition of two independent Poisson processes with intensity measures (1 - e - s ) M and e - s M , respectively, we obtain that

$$| \mathbf E [ h ( G ( s ) ) | G ( 0 ) = \varnothing ] - \mathbf E h ( \zeta ) | \leq c ^ { - s } \mathbf M ( \mathbb { Y } ) .$$


<!-- p:21 -->


Combining (5.3) and (5.4) and letting s →∞ completes the proof. □

The next lemma, which can be seen as an integration by parts formula, is the key for the proof of Theorem 3.1 given in Section 6 below.

$$L E M M A \ 5 . 4 . \quad & \text {If } h \in \mathcal { L } _ { 1 } \ \ a n d \ \omega \in \widehat { N } _ { \mathbb { Y } } , \ \ t h e n \\ ( 5 . 5 ) & & \text {Eh} ( \zeta ) - h ( \omega ) = \int _ { 0 } ^ { \infty } L P _ { s } h ( \omega ) \, d s .$$

Proof. For an arbitrary h ∈ L 1 we define h n : N Y → R , n ∈ N by

Clearly, each of the functions h n is bounded and belongs to L 1 . Thus the forward-backward equation stated as Theorem 12.22 in [24] implies that

$$\text {For an arbitrary } h \in \mathcal { L } _ { 1 } \text { we define } h _ { n } \colon \widehat { N } _ { \mathbb { Y } } \to \mathbb { R } , \, n , \\ h _ { n } ( \omega ) = \begin{cases} n , & h ( \omega ) > n , \\ h ( \omega ) , & - n \leq h ( \omega ) \leq n , \end{cases} \\ \text { of the functions } h _ { n } \text { is bounded and belongs to
sward equation stated as Theorem 1.2.22 in [24] in}$$

$$\text { for wait-back wait equation state} \, & \text {a} \, \text { s} \, \text {e} \, \text { in } 1 2 . 2 \, \text { in } [ 2 4 ] \text { in } \text {pimes} \text { in } \text {a} \, \text {s} \, \text {e} \, \text { } \\ & \text { (5.6)} & P _ { t } h _ { n } ( \omega ) - h _ { n } ( \omega ) = \int _ { 0 } ^ { t } L P _ { s } h _ { n } ( \omega ) \, d s , \quad t \geq 0 .$$

By construction, we have h n ( ω ) → h ( ω ), as n →∞ . The dominated convergence theorem implies that P s h n ( ω ) → P s h ( ω ) and LP s h n ( ω ) → LP s h ( ω ), as n →∞ , for all s ≥ 0. By (5.1) and Lemma 5.1, we have that, for g = h or g = h n and s ≥ 0,

$$g & = h _ { n } \text { and } s \geq 0 , \\ & \quad | L P _ { s } g ( \omega ) | \leq \int _ { \mathbb { Y } } e ^ { - s } | P _ { s } ( D _ { y } g ) ( \omega ) | M ( d y ) \\ & \quad + \int _ { \mathbb { Y } } e ^ { - s } | P _ { s } ( D _ { y } g ) ( \omega - \delta _ { y } ) | \omega ( d y ) \\ & \leq e ^ { - s } ( M ( \mathbb { Y } ) + \omega ( \mathbb { Y } ) ) . \\ \intertext { \text {In the last step we used the fact that } | P _ { s } ( D _ { y } g ) | \leq 1 . \text { Now, a further a }$$

In the last step we used the fact that | P s ( D y g ) | ≤ 1. Now, a further application of the dominated convergence theorem shows that

$$\text {In or the lemma of concrete inference shows that} \\ \lim _ { n \to \infty } \int _ { 0 } ^ { t } L P _ { s } h _ { n } ( \omega ) \, d s & = \int _ { 0 } ^ { t } L P _ { s } h ( \omega ) \, d s , \quad t \geq 0 , \\$$

so that, letting n →∞ in (5.6), yields

$$5 0 \text { that} , & 1 6 \text { coming } h ^ { 2 } / \infty \text { in } ( 0 . 6 ) , \, y \text {1cds} \\ & ( 5 . 8 ) & P _ { t } h ( \omega ) - h ( \omega ) = \int _ { 0 } ^ { t } L P _ { s } h ( \omega ) \, \text {d} s , \quad t \geq 0 . \\$$

Because of (5.7) and the dominated convergence theorem, the right-hand side of (5.8) converges to the right-hand side of (5.5), as t →∞ . Together with Lemma 5.3 for the left-hand side, this completes the proof. □


<!-- p:22 -->


Remark 5.5. The operator L and the associated semi-group ( P s ) s ≥ 0 on the Poisson space can be also defined via the Wiener-Itˆ o chaos expansion, which we recall now for completeness. We still denote by ζ a Poisson process with intensity measure M on a lcscH space Y . A crucial property of ζ is that any square integrable functional F ∈ L 2 ( P ζ ) of ζ can be written as

$$F = E F + \sum _ { n = 1 } ^ { \infty } I _ { n } ( f _ { n } )$$

with

$$f _ { n } ( y _ { 1 } , \dots , y _ { n } ) = \frac { 1 } { n ! } \text {E} D _ { y _ { 1 } , \dots , y _ { n } } ^ { n } F ( \zeta ) , \quad y _ { 1 } , \dots , y _ { n } \in \mathbb { Y } , n \geq 1 ,$$

where D n := D ◦ D n - 1 with D 1 := D is the n th iteration of the discrete gradient D introduced in Section 2, and where I n ( f n ) stands for the n -fold Wiener-Itˆ o integral of the square integrable and symmetric function f n with respect to the signed random measure ζ - M . Moreover, the series in (5.9) converges in L 2 ( P ζ ) and is called the Wiener-Itˆ o chaos expansion of F ; we refer to [29] for further details. We can now define the Ornstein-Uhlenbeck generator L on the Poisson space by

$$L F = - \sum _ { n = 1 } ^ { \infty } n I _ { n } ( f _ { n } ) ,$$

whenever F belongs to dom L ; that is, F is such that ∑ ∞ n =1 n 2 n ! ‖ f n ‖ 2 L 2 ( M n ) &lt; ∞ , where ‖· ‖ L 2 ( M n ) stands for the usual norm in L 2 ( M n ). We remark that LF can equivalently be written as in (5.1) as a consequence of identity (3.19) in [29] and of the relation stated in [33], Lemma 2.11, between the discrete gradient, the Ornstein-Uhlenbeck generator and the so-called Skorohodintegral on the Poisson space, another operator, which is not needed in the sequel. In [28] the relation between the inverse of the Ornstein-Uhlenbeck generator and the associated semi-group is investigated. The semi-group ( P s ) s ≥ 0 can be written in terms of the Wiener-Itˆ o chaos expansion as

$$P _ { s } F = E F + \sum _ { n = 1 } ^ { \infty } e ^ { - n s } I _ { n } ( f _ { n } ) , \quad s \geq 0 ,$$

where F ∈ dom L is assumed to have a chaotic expansion as in (5.9); see, for example, [28], equation (3.13). Lemma 5.1 is a special case of [28], Lemma 3.1, and Lemmas 5.2, 5.3 and 5.4 can also be derived via the approach sketched in this remark. However, we prefer to give proofs not relying on Wiener-Itˆ o chaos expansions rather than on trajectorial properties.


<!-- p:23 -->


Remark 5.6. In [41] a spatial birth-death process is constructed whose invariant distribution is a Gibbs process. This includes the birth-death process in the present paper as a special case, and the generator in [41] is a generalization of the generator in (5.1). However, the results in [41] do not cover the results of this section since only the test functions for the total variation distance are considered, while we use Lipschitz functions, which are needed for the Kantorovich-Rubinstein distance.

6. Proof of Theorem 3.1. Before going into the details of the proof of Theorem 3.1, we explain the strategy informally in case of an underlying Poisson process η . Applying the multivariate Mecke formula (2.1) in equation (6.4) below, we are lead to estimate the integral with respect to K k of

$$E [ F ( \xi ( \eta + \delta _ { x _ { 1 } } + \cdots + \delta _ { x _ { k } } ) - \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) - F ( \xi ( \eta + \delta _ { x _ { 1 } } + \cdots + \delta _ { x _ { k } } ) ) ] , \\ ( 6 . 1 ) & & x _ { 1 } , \dots , x _ { k } \in \mathbb { X } , \\ & & \\ & & w h \ F \colon \widehat { N } _ { x } \to \mathbb { R } \text { being a certain point process functional and where we write }$$

̸

with F : ̂ N Y → R being a certain point process functional and where we write ξ ( μ ) instead of ξ to underpin the dependence of ξ on the underlying point configuration μ . The difficulty comes from the fact that adding δ x 1 + · · · + δ x k to the Poisson process η amounts not only to adding δ f ( x 1 ,...,x k ) to ξ ( η ) but also all atoms of the form f ( x i 1 , . . . , x i l ,  ̃ x l +1 , . . . ,  ̃ x k ) with l ∈ { 1 , . . . , k } , pairwise different indices i 1 , . . . , i l ∈{ 1 , . . . , k } and ( ̃ x l +1 , . . . ,  ̃ x k ) ∈ η k - l = . We denote by ˆ ξ ( x 1 , . . . , x k , η ) the collection of these extra atoms. The difference in (6.1) is now decomposed as

$$m \left ( 0 . 1 \right ) & \text {is now composed as} \\ E [ ( F ( \xi ( \eta ) + \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \eta ) ) - F ( \xi ( \eta ) ) ) \\ ( 6 . 2 ) \quad & + ( F ( \xi ( \eta ) ) - F ( \xi ( \eta ) + \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) ) \\ & + ( F ( \xi ( \eta ) + \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) - F ( \xi ( \eta ) + \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \eta ) + \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) ) ] . \\ \text {The middle term in } ( 6 . 2 ) \text { contributes to the total variation distance of the}$$

The middle term in (6.2) contributes to the total variation distance of the intensity measures in (3.3) in Theorem 3.1. Since F is Lipschitz, the expectation and the integral with respect to x 1 , . . . , x k of the first and the third term in (6.2) are bounded (up to a constant) by

$$E \int _ { \mathbb { X } ^ { k } } \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \eta ) ( \mathbb { Y } ) K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) ,$$

which in turn is bounded by E ξ ( Y ) 2 - E ξ ( Y ) - ( E ξ ( Y )) 2 and r (dom f ). This effect contributes to the second term of the bounds in Theorem 3.1. For k =1, only the middle term in (6.2) is present. This explains why, for k =1, the Kantorovich-Rubinstein distance between the transformation of a Poisson process (which is again a Poisson process) and a second Poisson process is bounded by the total variation distance of the intensity measures, and the second term in (3.3) in Theorem 3.1 vanishes.


<!-- p:24 -->


Throughout this section we use the same notation as in Section 3.1. Moreover, let [ k ] be shorthand for { 1 , . . . , k } . For x =( x 1 , . . . , x k ) ∈ X k , I = { i 1 , . . . , i | I | } ⊂ [ k ] and z =( z 1 , . . . , z k -| I | ) ∈ X k -| I | , let ( x I , z ) = ( x i 1 , . . . , x i | I | , z 1 , . . . , z k -| I | ). We prepare the proof of Theorem 3.1 with the following lemma.

Lemma 6.1. Let the assumptions of Theorem 3.1 prevail. If ξ is induced by a Poisson process, then

$$b y _ { \ } a \ P o i s s o n \ p r o c e s s , \ t h e n \\ \\ E \xi ( \mathbb { Y } ) ^ { 2 } = \frac { 1 } { k ! } \sum _ { I \subset [ k ] } \frac { 1 } { ( k - | I | ) ! } \int _ { \mathbb { X } ^ { k } } \int _ { \mathbb { Y } ^ { k - | I | } } 1 ( ( x _ { 1 } , \dots , x _ { k } ) \in \hom f ) \\ \times 1 ( ( x _ { I } , z ) \in \hom f ) K ^ { k - | I | } ( d z ) \\ \times K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) . \\ \\ \intertext { I f \xi \ i s \ d e r i v e d \ f o r m \ a \ b i n o m i a l \ p r o c e s \ o f \ n \ p o i n t s , \ t h e n }$$

If ξ is derived from a binomial process of n points, then

$$I f \, \xi \, \text { is derived from a binomial process of $n$ points, then} \\ \\ E \xi ( \mathbb { Y } ) ^ { 2 } = \frac { 1 } { k ! } \sum _ { I \subset [ k ] } \frac { ( n ) _ { 2 k - | I | } } { ( k - | I | ) ! } \int _ { \mathbb { Z } ^ { k } } \int _ { \mathbb { Z } ^ { k - | I | } } 1 ( ( x _ { 1 } , \dots , x _ { k } ) \in \text {dom} \, f ) \\ \times 1 ( ( x _ { I } , z ) \in \text {dom} \, f ) K _ { 1 } ^ { k - | I | } ( d z ) \\ \times K _ { 1 } ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) . \\$$

Proof. We have that

$$P R O F . \quad & \text {We have that} \\ \xi ( \mathbb { Y } ) ^ { 2 } = \frac { 1 } { ( k ! ) ^ { 2 } } \left ( \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { \neq } ^ { k } } 1 ( ( x _ { 1 } , \dots , x _ { k } ) \in \text {dom} f ) \right ) ^ { 2 } \\ = \frac { 1 } { ( k ! ) ^ { 2 } } \sum _ { I \subset [ k ] } \sum _ { ( x _ { 1 } , \dots , x _ { k } , z ) \in \mu _ { \neq } ^ { k - 1 } } \frac { k ! } { ( k - | I | ) ! } 1 ( ( x _ { 1 } , \dots , x _ { k } ) \in \text {dom} f ) \\ & \times 1 ( ( x _ { I } , z ) \in \text {dom} f ) , \\ \text {where we have used that two points occurring in different sums can be either} \\ \text {equal or distinguish and that dom f is symmetric. Now the multivariate Mooko}$$

̸

where we have used that two points occurring in different sums can be either equal or distinct and that dom f is symmetric. Now the multivariate Mecke (2.1) and its binomial analogue (2.2) complete the proof. □

Proof of Theorem 3.1. Throughout this proof we write ξ ( η ) and ξ ( β n ) to emphasize the dependence of ξ on the underlying point process. Whenever we do not need special properties of η or β n , we write ξ ( μ ) with the dummy variable μ standing for either η or β n . As discussed in Remark 3.2(ii), we can assume for the Poisson case that L ( Y ) &lt; ∞ and

̸


<!-- p:25 -->


hence that ξ ( η ) is almost surely finite since (3.3) is obviously true otherwise. For an underlying binomial process it is sufficient to consider only the case n ≥ k since, otherwise, the statement is obviously true as explained in Remark 3.2(i).

$$& \text {Remark } 3 . 2 ( 1 ) . \\ & \text {Lemma } 5 . 4 \text { says that for } h \in \mathcal { L } _ { 1 } \text { and } \omega \in \widehat { N } _ { \mathbb { Y } } , \\ & ( 6 . 3 ) & \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { }$$

The Stein-type identity (6.3) is the starting point for our proof. Combining (6.3) with the representation of the generator L in (5.1), choosing ω = ξ ( μ ) and taking expectations results in the following:

$$\left ( 6 . 3 \right ) & \text { with the representation of the generator } L \text { in } ( 5 . 1 ) , \text { choosing } \omega = \xi ( \mu ) \\ \text { and taking } & \text {expectations results in the following:} \\ & \text {Eh( \zeta) - E h( \xi ( \mu ) ) = E \int _ { 0 } ^ { \infty } L P _ { s } h ( \xi ( \mu ) ) \, d s } \\ & \quad = E \int _ { 0 } ^ { \infty } \int _ { \mathbb { Y } } ( P _ { s } h ( \xi ( \mu ) + \delta _ { y } ) - P _ { s } h ( \xi ( \mu ) ) ) M ( d y ) \, d s \\ & \quad + E \int _ { 0 } ^ { \infty } \sum _ { y \in \xi ( \mu ) } \left ( P _ { s } h ( \xi ( \mu ) - \delta _ { y } ) - P _ { s } h ( \xi ( \mu ) ) \right ) d s . \\ \text {Let us denote the first and the second term on the right-hand side by } T _ { 1 , \mu }$$

Let us denote the first and the second term on the right-hand side by T 1 ,μ and T 2 ,μ , respectively. By Fubini's theorem and the definition of ξ ( μ ), we obtain that

̸

$$\text {obtain that} \\ T _ { 2 , \mu } = \frac { 1 } { k ! } \int _ { 0 } ^ { \infty } E \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { \neq } ^ { k } \cap d o m \ f } ( P _ { s } h ( \xi ( \mu ) - \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) - P _ { s } h ( \xi ( \mu ) ) ) \, d s . \\$$

By the multivariate Mecke formula (2.1) and its analogue (2.2) for binomial processes, we see that

and

$$p r o c h s e s , & \, w e \, s e e \, t a t \\ & \, T _ { 2 , \eta } = \frac { 1 } { k ! } \int _ { 0 } ^ { \infty } \int _ { \text {dom} } E [ P _ { s } h ( \xi ( \eta + \delta _ { x _ { 1 } } + \cdots + \delta _ { x _ { k } } ) - \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) \\ & \, - P _ { s } h ( \xi ( \eta + \delta _ { x _ { 1 } } + \cdots + \delta _ { x _ { k } } ) ) ] \\ & \quad \times K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \, d s \\ \text {and} & \,$$

$$\text { and } & \quad T _ { 2 , \beta _ { n } } = \frac { ( n ) _ { k } } { k ! } \int _ { 0 } ^ { \infty } \int _ { \text {dom} } E [ P _ { s } h ( \xi ( \beta _ { n - k } + \delta _ { x _ { 1 } } + \cdots + \delta _ { x _ { k } } ) - \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) \\ & \quad \times K _ { 1 } ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \, d s . \\ \text {Let us write $\hat{ \xi}(x_{1},\dots,x_{k},\mu) \, for the point process }$$

Let us write ˆ ξ ( x 1 , . . . , x k , μ ) for the point process

̸

$$\text {Let} \ \text {us white $\zeta(\ x_{1},\dots,x_{k},\mu)$ for the
                    $k$-subset of process} \\ \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \mu ) \coloneqq \sum _ { \partial \neq I \subset \zeta [ k ] , z \in \mu _ { \neq } ^ { k - | I | } } \frac { 1 } { ( k - | I | ) ! } 1 ( ( x _ { I } , z ) \in \text {dom} \ f ) \delta _ { f ( x _ { I } , z ) }$$

̸


<!-- p:26 -->


on Y , where ⊊ denotes proper set-inclusion and where the notation ( x I , z ) has been introduced before Lemma 6.1 above. Then

$$on \, \mathbb { Y } , \, \text {where $\zeta$ denotes proper set-inclusion and where the notation (x_{I}, z)\,} \\ \text {has been introduced before Lemma 6.1 above. Then} \\ T _ { 2 , \eta } = \frac { 1 } { k ! } \int _ { 0 } ^ { \infty } \int _ { \text {dom} } E [ P _ { s } h ( \xi ( \eta ) + \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \eta ) ) \\ & - P _ { s } h ( \xi ( \eta ) + \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \eta ) + \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) ] \\ & \times K ^ { \ast } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \, d s \\ = - \frac { 1 } { k ! } \int _ { 0 } ^ { \infty } \int _ { \text {dom} f } E [ P _ { s } h ( \xi ( \eta ) + \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) - P _ { s } h ( \xi ( \eta ) ) ] \\ & \times K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \, d s \\ + \frac { 1 } { k ! } \int _ { 0 } ^ { \infty } \int _ { \text {dom} f } E [ P _ { s } h ( \xi ( \eta ) + \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \eta ) ) \\ & - P _ { s } h ( \xi ( \eta ) ) + P _ { s } h ( \xi ( \eta ) + \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) \\ & - P _ { s } h ( \xi ( \eta ) + \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \eta ) + \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) ] \\ \times K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \, d s \\ = \hat { T _ { 2 , \eta } } + R _ { \eta } \\ \text {and} \\ & ( n ) _ { k } , \, \int _ { \infty } ^ { \infty } \int _ { \mathbb { L } } \hat { \hat { \ } } \\$$

and

$$\colon = & \hat { T } _ { 2 , \eta } + R _ { \eta } \\ \text {and} \\ T _ { 2 , \beta _ { n } } = \frac { ( n ) _ { k } } { k ! } \int _ { 0 } ^ { \infty } \int _ { \text {dom} } E [ P _ { S } h ( \xi ( \beta _ { n - k } ) + \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \beta _ { n - k } ) ) \\ & - P _ { S } h ( \xi ( \beta _ { n - k } ) + \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \beta _ { n - k } ) + \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) ] \\ & \times K _ { 1 } ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) d s \\ = & - \frac { ( n ) _ { k } } { k ! } \int _ { 0 } ^ { \infty } \int _ { \text {dom} } E [ P _ { S } h ( \xi ( \beta _ { n - k } ) + \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) - P _ { S } h ( \xi ( \beta _ { n - k } ) ) ] \\ & \times K _ { 1 } ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) d s \\ & + \frac { ( n ) _ { k } } { k ! } \int _ { 0 } ^ { \infty } \int _ { \text {dom} } E [ P _ { S } h ( \xi ( \beta _ { n - k } ) + \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \beta _ { n - k } ) ) \\ & - P _ { S } h ( \xi ( \beta _ { n - k } ) ) + P _ { S } h ( \xi ( \beta _ { n - k } ) + \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) \\ & + \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) ] \\ = & \hat { T } _ { 2 , \beta _ { n } } + R _ { \beta _ { n } } .$$


<!-- p:27 -->


Together with (6.4) and the formulas for L in (3.1) and (3.2), we see that

and

$$E h ( \zeta ) - E h ( \xi ( \beta _ { n } ) ) \\ = \int _ { 0 } ^ { \infty } \int _ { \mathbb { Y } } E [ D _ { y } P _ { s } h ( \xi ( \beta _ { n } ) ) ] ( M - L ) ( d y ) \, d s \\ + \int _ { 0 } ^ { \infty } \int _ { \mathbb { Y } } E [ D _ { y } P _ { s } h ( \xi ( \beta _ { n } ) ) ] - E [ D _ { y } P _ { s } h ( \xi ( \beta _ { n - k } ) ) ] L ( d y ) \, d s + R _ { \beta _ { n } } . \\ \text {We now determine the remainder terms } R _ { n } \text { and } R _ { \beta _ { n } } \text { . For } ( x _ { 1 } , \dots , x _ { k } ) \in \text {dom } f$$

We now determine the remainder terms R η and R β n . For ( x 1 , . . . , x k ) ∈ dom f let us define  ̃ h x 1 ,...,x k : ̂ N Y → R by

We can then rewrite R η and R β n as

$$\widetilde { h } _ { x _ { 1 } , \dots , x _ { k } } ( \mu ) = \frac { 1 } { 2 } ( h ( \mu ) - h ( \mu + \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) ) . \\ \text {then rewrite } R _ { \eta } \text { and } R _ { \beta _ { n } } \text { as }$$

$$We can then rewrite R _ { \eta } \, and \, R _ { \beta _ { n } } \, as \\ R _ { \eta } = \frac { 2 } { k ! } \int _ { 0 } ^ { \infty } \int _ { \text {dom} f } \mathbf E [ P _ { s } \widetilde { h } _ { x _ { 1 } , \dots , x _ { k } } ( \xi ( \eta ) + \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \eta ) ) - P _ { s } \widetilde { h } _ { x _ { 1 } , \dots , x _ { k } } ( \xi ( \eta ) ) ] \\ \times K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \, d s \\ \intertext { a n d }$$

and

$$\text { and } & & R _ { \beta _ { n } } = \frac { 2 ( n ) _ { k } } { k ! } \int _ { 0 } ^ { \infty } \int _ { \text {dom} f } E [ P _ { s } \widetilde { h } _ { x _ { 1 } , \dots , x _ { k } } ( \xi ( \beta _ { n - k } ) + \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \beta _ { n - k } ) ) \\ & & \quad - P _ { s } \widetilde { h } _ { x _ { 1 } , \dots , x _ { k } } ( \xi ( \beta _ { n - k } ) ) ] \\ & & \quad \times K _ { 1 } ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \, d s .$$

Because of  ̃ h x 1 ,...,x k ∈ L 1 , we obtain by the definition of the semi-group ( P s ) s ≥ 0 in (5.2) and Lemma 5.2 that

$$\times K _ { 1 } ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \, d s . \\$$

$$( P _ { s } ) _ { s \geq 0 } \, \text { in } ( 5 . 2 ) \, \text { and } \text { Lemma } 5 . 2 \, \text { that } \\ | R _ { \eta } | \leq \frac { 2 } { k ! } \int _ { 0 } ^ { \infty } \int _ { \text {dom} } e ^ { - s } \hat { E } \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \eta ) ( \mathbb { Y } ) K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \, d s \\ = \frac { 2 } { k ! } \int _ { \text {dom} } \hat { E } \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \eta ) ( \mathbb { Y } ) K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \\ \text {and}$$

and

$$\text { and } & & | R _ { \beta _ { n } } | \leq \frac { 2 ( n ) _ { k } } { k ! } \int _ { 0 } ^ { \infty } \int _ { \text {dom} } e ^ { - s } \mathbf E \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \beta _ { n - k } ) ( \mathbb { Y } ) K _ { 1 } ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \, d s \\ & \leq \frac { 2 ( n ) _ { k } } { k ! } \int _ { \text {dom} } E \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \beta _ { n - k } ) ( \mathbb { Y } ) K _ { 1 } ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) .$$

$$\log \text {ether with } ( 6 . 4 ) \text { and the formulas for } L \text { in } ( 3 . 1 ) \text { and } ( 3 . 2 ) , \text { we see that} \\ E h ( \zeta ) - E h ( \xi ( \eta ) ) = \int _ { 0 } ^ { \infty } \int _ { \mathbb { Y } } E [ D _ { y } P _ { s } h ( \xi ( \eta ) ) ] ( M - L ) ( d y ) \, d s + R _ { \eta } \\$$


<!-- p:28 -->


Now, from the Mecke formula (2.1) and its analogue (2.2) for binomial processes, it follows that

̸


, . . . , x

1

x

=

E

=

∅

̸

=

I

∅

̸

k

=

, β

I

⊊

n

-

k

[

k

]

,z

∈

)(

β

1

I

-|

∑

̸

Y

)

k

-|

I

|

n

=

-

k,

̸

∑

⊊

[

k

]

X

k

)!

|

1

(

f

(

1

-|

I

|

k

-|

I

|

k

)

I

(

n

(

k

)!

-|

|

k

∫

Together with Lemma 6.1, we obtain

̸

$$\text {Together with Lemma 6.1, we obtain} \\ | R _ { \eta } | \leq \frac { 2 } { k ! } \int _ { \mathbb { K } ^ { k } } \sum _ { \varnothing \neq I \subseteq [ k ] } \frac { 1 } { ( k - | I | ) ! } \int _ { \mathbb { K } ^ { k - | I | } } 1 ( ( x _ { 1 } , \dots , x _ { k } ) \in \text {dom} \, f ) \\ \times 1 ( ( x _ { 1 } , z ) \in \text {dom} \, f ) K ^ { k - | I | } ( d z ) \\ \times K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \\ = 2 ( E \xi ( \mathbb { Y } ) ^ { 2 } - L ( \mathbb { Y } ) - L ( \mathbb { Y } ) ^ { 2 } ) = 2 ( E \xi ( \mathbb { Y } ) ^ { 2 } - E \xi ( \mathbb { Y } ) - ( E \xi ( \mathbb { Y } ) ) ^ { 2 } ) \\ \text {and}$$

and

$$\text { and } \\ | R _ { \beta n } | \leq \frac { 2 } { k ! } \int _ { \mathbb { X } ^ { k } } \sum _ { \varnothing \in I \subset [ k ] } \frac { ( n ) _ { k } ( n - k ) _ { k - | I | } } { ( k - | I | ) ! } \int _ { \mathbb { X } ^ { k - | I | } } 1 ( ( x _ { 1 } , \dots , x _ { k } ) \in \text {dom} \, f ) \\ \times 1 ( ( x _ { I } , z ) \in \text {dom} \, f ) K _ { 1 } ^ { k - | I | } ( d z ) \\ ( 6 . 7 ) \\ = 2 \left ( 1 E \xi ( \mathbb { Y } ) ^ { 2 } - L ( \mathbb { Y } ) - \frac { ( n - k ) _ { k } } { ( n ) _ { k } } L ( \mathbb { Y } ) ^ { 2 } \right ) \\ = 2 \left ( 1 E \xi ( \mathbb { Y } ) ^ { 2 } - E \xi ( \mathbb { Y } ) - \frac { ( n - k ) _ { k } } { ( n ) _ { k } } ( E \xi ( \mathbb { Y } ) ) ^ { 2 } \right ) .$$

((

x


I

, z

)

I

, z

)

∈

-

$$cresseses , & \text { if follows that} \\ & \quad E \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \eta ) ( \mathbb { Y } ) \\ & = E \sum _ { \substack { & & \langle k - | I | | ) ! \\ & \geqslant I \subsetneq [ k ] , z \in \eta _ { \neq } ^ { k - | I | } } } \frac { 1 } { ( k - | I | ) ! } 1 ( f ( x _ { I } , z ) \in \text { dom } f ) \\ & = \sum _ { \emptyset \neq I \subset [ k ] } \frac { 1 } { ( k - | I | ) ! } \int _ { \mathbb { X } ^ { k - | I | } } 1 ( ( x _ { I } , z ) \in \text { dom } f ) K ^ { k - | I | } ( d z ) \\ \text {and}$$

and

(6.5)

E

ˆ

ξ

(

̸

(

∈

dom

f

)

dom

f

)

K

k

-|

I

|

1

(d

z

)

.


<!-- p:29 -->


The inequalities in (6.6) and (6.7) together with the definition of r (dom f ) imply that

$$| R _ { \eta } | \leq \frac { 2 ^ { k + 1 } } { k ! } r ( \text {dom} \, f ) \quad \text {and} \quad | R _ { \beta _ { n } } | \leq \frac { 2 ^ { k + 1 } } { k ! } r ( \text {dom} \, f ) .$$

Next, it follows from Lemma 5.2 that for s ≥ 0,

$$| E D _ { y } P _ { s } h ( \xi ( \mu ) ) | \leq E [ | P _ { s } h ( \xi ( \mu ) + \delta _ { y } ) - P _ { s } h ( \xi ( \mu ) ) | ] \leq e ^ { - \mathfrak s } . \\$$

For y 1 , y 2 ∈ Y and  ̃ ξ ∈  ̃ N Y we have d TV (  ̃ ξ + δ y 1 ,  ̃ ξ + δ y 2 ) ≤ 1 so that h ∈ L 1 leads to

$$| D _ { y _ { 1 } } h ( \tilde { \xi } ) - D _ { y _ { 2 } } h ( \tilde { \xi } ) | & = | h ( \tilde { \xi } + \delta _ { y _ { 1 } } ) - h ( \tilde { \xi } + \delta _ { y _ { 2 } } ) | \leq 1 . \\ \vdots & \vdots 1 .$$

Together with Lemma 5.1, we obtain that

$$| \text {ED} _ { y _ { 1 } } P _ { s } h ( \xi ( \mu ) ) - \text {ED} _ { y _ { 2 } } P _ { s } h ( \xi ( \mu ) ) | \\ = e ^ { - s } | \text {E} P _ { s } ( D _ { y _ { 1 } } h - D _ { y _ { 2 } } h ) ( \xi ( \mu ) ) | \leq e ^ { - s } \\ \text {for all } y _ { 1 } \cup y _ { 2 } \in \mathbb { Y } \text { and } s > 0 \text { The estimates in } ( 6 9 ) \text { and } ( 6 1 0 ) \text { show that }$$

for all y 1 , y 2 ∈ Y and s ≥ 0. The estimates in (6.9) and (6.10) show that

$$\text { for all } y _ { 1 } , y _ { 2 } \in \mathbb { Y } \text { and } s \geq 0 . \text { The estimates in } ( 6 . 9 ) \text { and } ( 6 . 1 0 ) \text { show that } \\ | \int _ { 0 } ^ { \infty } \int _ { \mathbb { Y } } E [ D _ { y } P _ { s } h ( \xi ( \mu ) ) ] ( M - L ) ( d y ) \, d s \Big | \leq d _ { T V } ( M , L ) \int _ { 0 } ^ { \infty } \, e ^ { - s } \, d s \\ \leq d _ { T V } ( M , L ) . \\$$

Combining (6.6) and (6.8) with (6.11) completes the proof of the Poisson case.

When considering a binomial process, we additionally need to take care of the term

$$\int _ { 0 } ^ { \infty } \int _ { \mathbb { Y } } E [ D _ { y } P _ { s } h ( \xi ( \beta _ { n } ) ) ] - E [ D _ { y } P _ { s } h ( \xi ( \beta _ { n - k } ) ) ] L ( d y ) \, d s .$$

For this, we use Lemma 5.1, the fact that 1 2 D y h ∈ L 1 whenever h ∈ L 1 and Lemma 5.2 to obtain that

$$\text {Lemma 5.2 to obtain that} \\ | E [ D _ { y } P _ { h } s ( \xi ( \beta _ { n } ) ) ] - E [ D _ { y } P _ { s } h ( \xi ( \beta _ { n - k } ) ) ] | \\ \leq \int _ { \mathbb { X } ^ { k } } | E [ D _ { y } P _ { s } h ( \xi ( \beta _ { n - k } + \delta _ { x _ { 1 } } + \cdots + \delta _ { x _ { k } } ) ) ] - E [ D _ { y } P _ { s } h ( \xi ( \beta _ { n - k } ) ) ] | \\ \times K _ { 1 } ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \\ = \int _ { \mathbb { X } ^ { k } } e ^ { - s } | E [ P _ { s } ( D _ { y } h ) ( \xi ( \beta _ { n - k } ) + \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \beta _ { n - k } ) + \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) \\ & - P _ { s } ( D _ { y } h ) ( \xi ( \beta _ { n - k } ) ) | \\ \times K _ { 1 } ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) )$$


<!-- p:30 -->


$$L \colon & \ D E C { R E S E F O N , M . S C H U L E } \ A N \colon C \colon T H A L E \\ & \leq \frac { 1 } { n ^ { k } } \int _ { \mathbb { X } ^ { k } } 2 e ^ { - 2 s } ( \hat { E } \hat { \xi } ( x _ { 1 } , \dots , x _ { k } , \beta _ { n - k } ) ( \mathbb { Y } ) + 1 ( ( x _ { 1 } , \dots , x _ { k } ) \in \text {dom} \, f ) ) \\ & \quad \times K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) \\ \text {for any } s \geq 0 . \text { It follows from } ( 6 . 5 ) \text { and } ( n - k ) _ { k - | I | } \leq n ^ { k - | I | } \text { that}$$

for any s ≥ 0. It follows from (6.5) and ( n - k ) k -| I | ≤ n k -| I | that

̸


$$\times K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) & \\ \quad \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \$$

Now, (3.2) implies that

$$N o w , ( 3 . 2 ) \lim i t s { \tt i a r t } \\ \int _ { \mathbb { X } ^ { k } } 1 ( ( x _ { 1 } , \dots , x _ { k } ) \in \text {dom} \, f ) \mathbf K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) = \frac { k ! n ^ { k } } { ( n ) _ { k } } \mathbf L ( \mathbb { Y } ) \leq k ! e ^ { k } E \xi ( \mathbb { Y } ) ,$$

where we have used that n k / ( n ) k ≤ k k /k ! ≤ e k for n ≥ k . Hence, using that 2 k e k ≤ 6 k , we find

$$2 ^ { k } e ^ { k } & \leq 6 ^ { k } , \, w e \, \text {find} \\ & \int _ { 0 } ^ { \infty } \int _ { \mathbb { Y } } | E [ D _ { Y } P _ { s } h ( \xi ( \beta _ { n } ) ) ] - E [ D _ { Y } P _ { s } h ( \xi ( \beta _ { n - k } ) ) ] | L ( d y ) \, d s \leq 6 ^ { k } k ! \frac { L ( \mathbb { Y } ) ^ { 2 } } { n } \\ & = 6 ^ { k } k ! \frac { ( E \xi ( \mathbb { Y } ) ) ^ { 2 } } { n } . \\ \intertext { Together with } ( 6 . 7 ) , ( 6 . 8 ) \, \text {and} \, ( 6 . 1 1 ) \, \text {this completes the proof in the binomial}$$

Together with (6.7), (6.8) and (6.11) this completes the proof in the binomial case. □

Remark 6.2. Bounds for the total variation distance between ξ and ζ that are similar to the bounds for the Kantorovich-Rubinstein distance in Theorem 3.1 can be deduced from Theorem 2.6 in [4]. This result implies that

$$\text {that} & & d _ { \text {rv} } ( \xi ( \eta ) , \zeta ) \leq 2 d _ { \text {TV} } ( L , M ) \\ & & + \frac { 2 } { k ! } \int _ { \text {dom} } E d _ { \text {TV} } ( \xi ( \eta ) , \xi ( \eta + \delta _ { x _ { 1 } } + \cdots + \delta _ { x _ { k } } ) - \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) \\ & & \times K ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) )$$


<!-- p:31 -->


and

$$\text { and } & & \text {d} _ { \text {TV} } ( \xi ( \beta _ { n } ) , \zeta ) \\ & \leq 2 d _ { \text {TV} } ( L , M ) \\ & + \frac { 2 ( n ) _ { k } } { k ! } \int _ { \text {dom} } \text {E} _ { \text {TV} } ( \xi ( \beta _ { n } ) , \xi ( \beta _ { n - k } + \delta _ { x _ { 1 } } + \dots + \delta _ { x _ { k } } ) - \delta _ { f ( x _ { 1 } , \dots , x _ { k } ) } ) \\ & \quad \times K _ { 1 } ^ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) . \\ \text {Since the integrands are bounded by } & & \hat { \rho }$$

Since the integrands are bounded by

E ˆ ξ ( x 1 , . . . , x k , η )( Y ) and E ˆ ξ ( x 1 , . . . , x k , β n - k )( Y )+ E d TV ( ξ ( β n ) , ξ ( β n - k )) , respectively, the integrals on the right-hand sides can be controlled as in the proof of Theorem 3.1 above.

## 7. Applications.

7.1. Poisson approximation of U-statistics. In this subsection we present a first application of Theorem 3.1 to U-statistics of Poisson or binomial processes. Let ( X , X ) and ( Y , Y ) be two lcscH spaces, and let for some fixed integer k ≥ 1, f t : X k → Y , t ≥ 1, be symmetric measurable functions. Furthermore, for a σ -finite measure K and a probability measure K 1 on X , we denote by η t a Poisson process with intensity measure K t := t K , t ≥ 1, and by β t , t ≥ 1, a binomial process of ⌈ t ⌉ points with intensity measure K t := ⌈ t ⌉ K 1 , respectively. If μ t is either η t or β t and if B is a measurable subset of Y , we define the U-statistics

$$\text { subset of } & \mathbb { I } , \, \text { we determine the } \text { 0-statistics} \\ & S _ { t } ( B ) \coloneqq \frac { 1 } { k ! } \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { t , \neq } ^ { k } } 1 ( f _ { t } ( x _ { 1 } , \dots , x _ { k } ) \in B ) , \quad t \geq 1 ,$$

̸

$$x _ { k } ) \in B . \, \text {To compare $S_{t}(B)$ with a Poisson random variable, we define} \\ r _ { t } ( B ) \colon = \max _ { 1 \leq \ell \leq k - 1 } \int _ { \mathbb { X } ^ { k - \ell } } \left ( \int _ { \mathbb { X } ^ { k - \ell } } 1 ( f _ { t } ( x _ { 1 } , \dots , x _ { k } ) \in B ) K _ { t } ^ { k - \ell } ( d ( x _ { \ell + 1 } , \dots , x _ { k } ) ) \right ) ^ { 2 } \\ \times K _ { t } ^ { \ell } ( d ( x _ { 1 } , \dots , x _ { \ell } ) ) \\ \text {if $k > 1$ and $r_{t}(B)$ := 0 if $k = 1$} .$$

̸

which count the number of k -tuples ( x 1 , . . . , x k ) ∈ μ k t, = for which f t ( x 1 , . . . , x k ) ∈ B . To compare S t ( B ) with a Poisson random variable, we define

if k &gt; 1 and r t ( B ) := 0 if k =1.

Theorem 7.1. Let B ∈ Y , and let Z be a Poisson distributed random variable with mean λ ∈ [0 , ∞ ) . Suppose that E S t ( B ) 2 &lt; ∞ . If S t ( B ) is induced by a Poisson process η t with t ≥ 1 , then

$$d w ( S _ { t } ( B ) , Z ) & \leq | E S _ { t } ( B ) - \lambda | + 2 ( E S _ { t } ( B ) ^ { 2 } - E S _ { t } ( B ) - ( E S _ { t } ( B ) ) ^ { 2 } ) \\ & \leq | E S _ { t } ( B ) - \lambda | + \frac { 2 ^ { k + 1 } } { k ! } r _ { t } ( B ) .$$


<!-- p:32 -->


If S t ( B ) is induced by a binomial process β t with t ≥ 1 , then

$$I f \, S _ { t } ( B ) \, \text { is induced by a binomial process } \beta _ { t } \text { with } t \geq 1 , \text { then} \\ \text {d} w ( S _ { t } ( B ) , Z ) \\ \leq | E S _ { t } ( B ) - \lambda | + 2 \left ( E S _ { t } ( B ) ^ { 2 } - E S _ { t } ( B ) - \frac { ( \lceil t \rceil - k ) _ { k } } { ( \lceil t \rceil ) _ { k } } ( E S _ { t } ( B ) ) ^ { 2 } \right ) \\ + \frac { k ! } { t } ( E S _ { t } ( B ) ) ^ { 2 } \\ \leq | E S _ { t } ( B ) - \lambda | + \frac { 2 ^ { k + 1 } } { k ! } r _ { t } ( B ) + \frac { 6 ^ { k } k ! } { t } ( E S _ { t } ( B ) ) ^ { 2 } . \\ \text {Proof.} \quad \text {We define the point processes}$$

Proof. We define the point processes

$$\xi _ { t } \coloneqq \frac { 1 } { k ! } \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { t , \neq } ^ { k } } \delta _ { f _ { t } ( x _ { 1 } , \dots , x _ { k } ) } , \quad t \geq 1 ,$$

̸

and denote their intensity measures by L t , t ≥ 1. By construction, S t ( B ) and ξ t ( B ) follow the same distribution. We notice that for any fixed h ∈ Lip(1) (recall that these are all h : R → R whose Lipschitz constant is at most one) and B ∈Y the mapping ω ↦→ h ( ω ( B )) from  ̃ N Y to R satisfies

and thus belongs to L 1 . Consequently, if ζ t is a Poisson process on Y with intensity measure L t , the definition of the Wasserstein distance and (2.6) yield

$$| h ( \omega _ { 1 } ( B ) ) - h ( \omega _ { 2 } ( B ) ) | & \leq | \omega _ { 1 } ( B ) - \omega _ { 2 } ( B ) | \leq d _ { T V } ( \omega _ { 1 } , \omega _ { 2 } ) , \quad \omega _ { 1 } , \omega _ { 2 } \in \widetilde { N } _ { \mathbb { Y } } , \\ \text {and thus belongs to } \mathcal { L } _ { 1 } . \text { Consequently, if } \zeta _ { t } \text { is a Poisson process on } \mathbb { Y } \text { with } \\ \intertext { t h u s b e l { o n g s } t h u s c r { L } _ { 1 } . \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { }$$

$$\mathbb { I }$$

$$d w ( S _ { t } ( B ) , \zeta _ { t } ( B ) ) & = d w ( \xi _ { t } ( B ) , \zeta _ { t } ( B ) ) = \sup _ { h \in \text {Lip} ( 1 ) } | \text {E} h ( \xi _ { t } ( B ) ) - \text {E} h ( \zeta _ { t } ( B ) ) | \\ & \leq \sup _ { g \in \mathcal { L } _ { 1 } } | \text {E} g ( \xi _ { t } | _ { B } ) - \text {E} g ( \zeta _ { t } | _ { B } ) | = d _ { \text {KR} } ( \xi _ { t } | _ { B } , \zeta _ { t } | _ { B } ) .$$

Now Theorem 3.1 and the observation that L t ( B ) = E S t ( B ) imply the result for the choice λ = E S t ( B ). The general case follows from the triangle inequality for the Wasserstein distance and the fact that the Wasserstein distance between a Poisson random variable with mean E S t ( B ) and another Poisson random variable with mean λ is bounded by | E S t ( B ) - λ | . □

We emphasize that Theorem 7.1 deals with Poisson approximation in Wasserstein distance. As already stated in (2.4), this is stronger than approximation in total variation distance, which is usually considered in the literature; see [10] for the only exception we are aware of. This is possible thanks to our functional limit Theorem 3.1, which deals with the KantorovichRubinstein distance rather than the total variation distance for point processes.


<!-- p:33 -->


The Poisson approximation in total variation distance of U-statistics over binomial input was considered in [7]. If we assume that E S t ( B ) = λ for t ≥ 1 for the binomial case in Theorem 7.1, we obtain up to a constant, which may depend on λ , the same bound as in [7], Theorem 2, for the total variation distance.

In [32], an abstract bound for the Poisson approximation of Poisson functionals (i.e., random variables depending on a Poisson process) is derived, which is also applicable to U-statistics over Poisson input. Our Theorem 7.1 yields better rates of convergence for this special class of Poisson functionals. In fact, the bound in [43], Proposition 4.1, which is derived from [32], involves the square root of ˆ r t ( B ) [see Remark 3.4(iii)], while in the bound for the Poisson case in Theorem 7.1 only ˆ r t ( B ) enters.

To illustrate the use of Theorem 7.1 let us consider a particular example, which will recur also in the following subsections. Let K ⊂ R d ( d ≥ 1) be a compact convex set with volume one. For t ≥ 1 let η t be a homogeneous Poisson process in K of intensity t , and denote by β t a binomial process in K with ⌈ t ⌉ points distributed according to the uniform distribution on K . For a family ( θ t ) t ≥ 1 of positive real numbers let us construct the random geometric graph with vertex set μ t , where μ t is η t or β t , by drawing an edge between two distinct vertices y 1 and y 2 whenever their Euclidean distance ‖ y 1 - y 2 ‖ is bounded by θ t . These random graphs are the natural geometric counterparts to the classical Erd ̈ os-R ́ enyi models for combinatorial random graphs. For background material we refer the reader to the monograph [34] and also to the recent paper [37] as well as the references cited therein.

For the random geometric graph introduced above, let E t be the number of edges. Note that E t is a U-statistic of the form

̸

$$E _ { t } = \frac { 1 } { 2 } \sum _ { ( y _ { 1 } , y _ { 2 } ) \in \mu _ { t , \neq } ^ { 2 } } 1 ( \| y _ { 1 } - y _ { 2 } \| \leq \theta _ { t } ) .$$

The multivariate Mecke formula (2.1) and a computation using spherical coordinates show that E t has expectation t 2 ( κ d θ d t + O ( θ d +1 t )) / 2 in the Poisson case, as θ t → 0. For an underlying binomial process the expected number of edges is ⌈ t ⌉ ( ⌈ t ⌉ - 1)( κ d θ d t + O ( θ d +1 t )) / 2, as θ t → 0. If the expectation of E t converges to a constant, as t →∞ , E t can be well approximated by a Poisson random variable. In contrast to [32], Theorem 5.1, whose proof involves various nontrivial computations, we can deduce a corresponding approximation result from Theorem 7.1; the proof is postponed to Section 7.4.

Corollary 7.2. Assume that lim t →∞ t 2 θ d t = λ ∈ [0 , ∞ ) , and let Z be a Poisson distributed random variable with mean κ d λ/ 2 . Then there is a constant c &gt; 0 only depending on the space dimension d , the set K and sup t ≥ 1 t 2 θ d t such that

$$d _ { W } ( E _ { t } , Z ) \leq c ( | t ^ { 2 } \theta _ { t } ^ { d } - \lambda | + t ^ { - \min \{ 2 / d , 1 \} } ) , \quad t \geq 1 .$$


<!-- p:34 -->


Remark 7.3. Using the classical Chen-Stein method for Poisson approximation, Theorem 3.4 in [34] delivers a version of Corollary 7.2 with the same rate of convergence in the total variation distance in case of an underlying binomial process. For the Poisson case, Theorem 3.12(iii) in [26] is a qualitative version of Corollary 7.2, which has been established by the method of moments, and Theorem 5.1 in [32] adds a total variation bound. Corollary 7.2 extends these results to a stronger probability metric and at the same time improves the rates of convergence in [32]. Namely, for space dimensions d ∈ { 1 , 2 } , Corollary 7.2 yields an upper bound of order | t 2 θ d t - λ | + t - 1 (for the Wasserstein distance), while Theorem 5.1 in [32] delivers an upper bound of order | t 2 θ d t - λ | + t - 1 / 2 (for the total variation distance).

7.2. Compound Poisson approximation of U-statistics. As in the previous subsection, we denote by μ t , t ≥ 1, a Poisson process η t or a binomial process β t on a lcscH space X . For k ∈ N and measurable functions h t : X k → R , t ≥ 1, we consider the family of U-statistics

̸

$$S _ { t } \coloneqq \frac { 1 } { k ! } \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { t , \neq } ^ { k } } h _ { t } ( x _ { 1 } , \dots , x _ { k } ) , \quad t \geq 1 .$$

̸

$$a \, \max ( \, \dot { C } \, \text {constant} \, \gamma \, \subset \, \mathbb { K } \, \text {and} \, t \geq 1 , \, \ w C \, \text {cnn} \\ L _ { t } ( A ) \colon = \frac { 1 } { k ! } \, \text {E} \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { t , \neq } ^ { k } } 1 ( h _ { t } ( x _ { 1 } , \dots , x _ { k } ) \in t ^ { - \gamma } A \, \wedge \, \{ 0 \} ) , \quad A \in \mathcal { B } ( \mathbb { R } ) ,$$

and

Since the sum runs also over all permutations of a fixed ( x 1 , . . . , x k ) ∈ μ k t, = , we assume without loss of generality that h t is symmetric for any t ≥ 1. For a fixed constant γ ∈ R and t ≥ 1, we define

̸

$$\text { and } \\ r _ { t } \colon = \max _ { 1 \leq \ell \leq k - 1 } \int _ { \mathbb { X } ^ { \ell } } \left ( \int _ { \mathbb { X } ^ { k - \ell } } 1 ( h _ { t } ( x _ { 1 } , \dots , x _ { k } ) \neq 0 ) K _ { t } ^ { k - \ell } ( d ( x _ { \ell + 1 } , \dots , x _ { k } ) ) \right ) ^ { 2 } \\ \times K _ { t } ^ { \ell } ( d ( x _ { 1 } , \dots , x _ { \ell } ) ) \\ \text { for } k \geq 2 , \text { and } \, \text { put } r _ { t } \colon = 0 \text { if } k = 1 . \text { The following result compares the U-}$$

̸

for k ≥ 2, and put r t := 0 if k = 1. The following result compares the Ustatistic S t with a compound Poisson random variable. Most of the existing literature is based on a direct use of Stein's method, but only for discrete compound Poisson random variables. This approach is technically sophisticated and also needs, in general, certain monotonicity assumptions. Moreover, there are even situations in which the solution of the so-called Stein equation cannot be controlled appropriately, and hence in which Stein's method is of little use; see [9]. Being a consequence of the functional limit theorem (Theorem 3.1), our approach circumvents such technicalities and also allows us to deal with compound Poisson random variables having a discrete or continuous distribution.


<!-- p:35 -->


Theorem 7.4. Let ζ be a Poisson process on R with a finite intensity measure M , let Z := ∑ x ∈ ζ x and let γ ∈ R . Then

$$d _ { T V } ( t ^ { \gamma } S _ { t } , Z ) \leq d _ { T V } ( L _ { t } , M ) + \frac { 2 ^ { k + 1 } } { k ! } r _ { t } , \quad t \geq 1 \\$$

if in the definition of S t a Poisson process η t is used, and

$$d _ { T V } ( t ^ { \gamma } S _ { t } , Z ) \leq d _ { T V } ( L _ { t } , M ) + \frac { 2 ^ { k + 1 } } { k ! } r _ { t } + \frac { 6 ^ { k } k ! } { t } L _ { t } ( \mathbb { R } ) ^ { 2 } , \quad t \geq 1 \\$$

if the underlying point process is a binomial process β t .

Proof. We consider the point processes

̸

$$t ^ { \gamma } \bullet \xi _ { t } \coloneqq \frac { 1 } { k ! } \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { t , \neq } ^ { k } } 1 ( h _ { t } ( x _ { 1 } , \dots , x _ { k } ) \neq 0 ) \delta _ { t ^ { \gamma } h _ { t } ( x _ { 1 } , \dots , x _ { k } ) } , \quad t \geq 1 .$$

̸

It follows from the definition of the total variation distance and (2.6) that

since the maps ω → 1 ( ∑ x ∈ ω x ∈ A ) belong to L 1 . Now Theorem 3.1 implies that

$$It \text { follows from the definition of the total variation distance and (2.6) that} \\ d _ { T V } ( t ^ { \gamma } S _ { t } , Z ) & = \sup _ { A \in \mathcal { B } ( \mathbb { R } ) } \left | E 1 \left ( \sum _ { x \in \mathcal { T } ^ { \gamma } \xi _ { t } } x \in A \right ) - E 1 \left ( \sum _ { x \in \mathcal { C } } x \in A \right ) \right | \leq \text {dkR} ( t ^ { \gamma } \bullet _ { \xi _ { t } , \zeta } ) \\ \text {since the maps } \omega \to 1 ( \sum _ { x \in \omega } x \in A ) \text { belong to } \mathcal { L } _ { 1 } . \text { Now Theorem } 3 . 1 \text { implies}$$

$$d _ { K R } ( t ^ { \gamma } \bullet \xi _ { t } , \zeta ) \leq d _ { T V } ( L _ { t } , M ) + \frac { 2 ^ { k + 1 } } { k ! } r _ { t } , \quad t \geq 1 ,$$

and

$$d _ { K R } ( t ^ { \gamma } \bullet \xi _ { t } , \zeta ) \leq d _ { T V } ( L _ { t } , M ) + \frac { 2 ^ { k + 1 } } { k ! } r _ { t } + \frac { 6 ^ { k } k ! } { t } L _ { t } ( \mathbb { R } ) ^ { 2 } , \quad t \geq 1 , \\$$

for the Poisson and the binomial case, respectively. This completes the proof. □

Remark 7.5. A compound Poisson random variable Z can alternatively be written as Z = ∑ N i =1 X i , where N is a Poisson distributed random variable and ( X i ) i ∈ N is a sequence of independent and identically distributed random variables such that N and ( X i ) i ∈ N are independent. However, the representation of Z in terms of the Poisson process ζ fits better into our general framework.

For the compound-Poisson approximation of U-statistics in the binomial case, a bound similar to that in Theorem 7.4 is derived in [21], Section 3.6. However, in that paper h t is required to take values in the nonnegative integers, whereas we do not need to impose such a condition. In addition, we are not aware of any analogous result for an underlying Poisson process.


<!-- p:36 -->


As an application of Theorem 7.4 we consider general edge-length functionals of the random geometric graph introduced in the course of the previous subsection. Fix a parameter b ∈ R , and define

̸

$$L _ { t } ^ { ( b ) } \coloneqq \frac { 1 } { 2 } \sum _ { ( x _ { 1 } , x _ { 2 } ) \in \mu _ { t , \neq } ^ { 2 } } 1 ( \text {dist} ( x _ { 1 } , x _ { 2 } ) \leq \theta _ { t } ) \text { dist} ( x _ { 1 } , x _ { 2 } ) ^ { b } , \quad t \geq 1 ,$$

where μ t stands either for a Poisson process η t or a binomial process β t . In particular, L (0) t is the number of edges in the random geometric graph, and L (1) t is its total edge length. As in Section 7.1, we consider the situation where the distance parameters ( θ t ) t ≥ 1 are chosen in such a way that the expected number of edges converges to a constant, as t →∞ . Recall that in Corollary 7.2 the number of edges L (0) t has been approximated by a Poisson random variable. For general exponents b we approximate L ( b ) t by a suitable compound Poisson random variable. The proof of the next result is postponed to Section 7.4 below.

Corollary 7.6. Fix b ∈ R , and assume that lim t →∞ t 2 θ d t = λ ∈ [0 , ∞ ) . Define Z := ∑ N i =1 ‖ X i ‖ b , where N is a Poisson distributed random variable with mean κ d λ/ 2 and ( X i ) i ∈ N are independent and uniformly distributed points in B d ( λ 1 /d ) , which are independent of N . Then there is a constant c &gt; 0 only depending on the space dimension d , the set K and sup t ≥ 1 t 2 θ d t such that

$$d _ { T V } ( t ^ { 2 b / d } L _ { t } ^ { ( b ) } , Z ) \leq c ( | t ^ { 2 } \theta _ { t } ^ { d } - \lambda | + t ^ { - \min \{ 2 / d , 1 \} } ) , \quad t \geq 1 .$$

Remark 7.7. Corollary 7.6 without a rate of convergence has been derived in [37], Theorem 3.5, by combining a point process convergence result with the continuous mapping theorem. Thanks to Theorem 7.4 we are able to add a rate of convergence for the total variation distance.

7.3. Approximation of U-statistics by α -stable random variables. Let us denote by μ t , t ≥ 1, a Poisson process η t or a binomial process β t as in the previous subsections. For fixed k ∈ N and measurable functions h t : X k → R , t ≥ 1, let

̸

$$S _ { t } \coloneqq \frac { 1 } { k ! } \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { t , \neq } ^ { k } } h _ { t } ( x _ { 1 } , \dots , x _ { k } ) , \quad t \geq 1 .$$

Here, we can and will assume without loss of generality that h t is symmetric for any t ≥ 1. We are interested in the limiting behavior of these U-statistics in situations where their summands are heavy tailed, and approximate S t by an α -stable random variable Z . Recall that this means that for any n ∈ N


<!-- p:37 -->


there are independent copies Z 1 , . . . , Z n of Z satisfying the distributional equality n - 1 /α ( Z 1 + · · · + Z n ) D = Z . We fix α ∈ (0 , 1) and γ ∈ R and apply our functional limit theorem to the point processes

̸

$$t ^ { \gamma } \bullet \xi _ { t } \coloneqq \frac { 1 } { k ! } \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { t , \neq } ^ { k } } 1 ( h _ { t } ( x _ { 1 } , \dots , x _ { k } ) \neq 0 ) \delta _ { s i g n ( h _ { t } ( x _ { 1 } , \dots , x _ { k } ) ) ^ { t \gamma } | h _ { t } ( x _ { 1 } , \dots , x _ { k } ) | ^ { - \alpha } } ,$$

$$=$$

$$t \geq 1 , \\ \\ \intertext { t \geq 1 , } \intertext { a . b . } \intertext { o r } \intertext { a } \intertext { b } \intertext { a } \intertext { b }$$

̸

on R , where sign( a ) = 1 ( a ≥ 0) - 1 ( a &lt; 0). If μ t is a binomial process, the convergence of the U-statistic S t to an α -stable random variable was considered in [17] without giving rates of convergence. Thanks to our quantitative bound for the Kantorovich-Rubinstein distance in Theorem 3.1, we are in the position to add a rate of convergence for the Kolmogorov distance. The statement of our result is prepared by introducing some notation. For A ∈B ( R ) and t ≥ 1, we define

̸

$$\sum _ { x _ { 1 } , \dots , x _ { k } ) \in \mu _ { t , \neq } ^ { k } } 1 ( h _ { t } ( x _ { 1 } , \dots , x _ { k } ) \neq 0 ) \\ \times 1 ( \text {sign} ( h _ { t } ( x _ { 1 } , \dots , x _ { k } ) ) | h _ { t } ( x _ { 1 } , \dots , x _ { k } ) | ^ { - \alpha } \in t ^ { - \gamma } A ) , \\ \intertext { t e n s i t y } \text {density measure of } t ^ { \gamma } \bullet \xi _ { t } , \text { and }$$

$$L _ { t } ( A ) \coloneqq \frac { 1 } { k ! } E \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { t , \neq } ^ { k } } 1 ( h _ { t } ( x _ { 1 } , \dots , x _ { k } ) \neq 0 )$$

̸

which is the intensity measure of t γ · ξ t , and

̸

$$\text { which is the intensity measure of } t ^ { \gamma } \bullet \xi _ { t } , \text { and } \\ r _ { t } ( A ) \coloneqq \max _ { 1 \leq \ell \leq k - 1 } \int _ { X ^ { \ell } } \left ( \int _ { \mathbb { X } ^ { k - \ell } } 1 ( h _ { t } ( x _ { 1 } , \dots , x _ { k } ) \neq 0 ) \\ \times 1 ( \text {sign} ( h _ { t } ( x _ { 1 } , \dots , x _ { k } ) ) | h _ { t } ( x _ { 1 } , \dots , x _ { k } ) | ^ { - \alpha } \in t ^ { - \gamma } A ) \\ \times K _ { t } ^ { k - \ell } ( d ( x _ { \ell + 1 } , \dots , x _ { k } ) ) \right ) ^ { 2 } \\ \times K _ { t } ^ { \ell } ( d ( x _ { 1 } , \dots , x _ { \ell } ) ) \\ \text { if } k > 2 \text { and } r _ { t } ( A ) \coloneqq 0 \text { if } k = 1 \text { The following result contains a quantitative }$$

if k ≥ 2 and r t ( A ) := 0 if k =1. The following result contains a quantitative bound for the approximation of U-statistics by an α -stable random variable with α ∈ (0 , 1).

$$\times K _ { t } ^ { \ell } ( d ( x _ { 1 } , \dots , x _ { \ell } ) ) \\ = 0 \text { if } l _ { 0 } = 1 \ T h o \ f o l l o r { x } { i }$$

Theorem 7.8. Let α ∈ (0 , 1) , and let M be either the Lebesgue measure on R or its restriction to R + . Define Z := ∑ x ∈ ζ sign( x ) | x | - 1 /α , where ζ is a Poisson process with intensity measure M . Assume that there are a constant γ ∈ R and functions g 1 , g 2 , g 3 : R 2 + → R + such that, for any a &gt; 0 and t ≥ 1 ,

and

$$d _ { T V } ( L _ { t } | _ { [ - a , a ] } , M | _ { [ - a , a ] } ) & \leq g _ { 1 } ( a , t ) , \quad r _ { t } ( [ - a , a ] ) \leq g _ { 2 } ( a , t ) \\$$

$$\frac { t ^ { - \gamma / \alpha } } { k ! } E \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { t , \neq } ^ { k } } 1 ( | h _ { t } ( x _ { 1 } , \dots , x _ { k } ) | < t ^ { \gamma / \alpha } a ^ { - 1 / \alpha } ) | h _ { t } ( x _ { 1 } , \dots , x _ { k } ) |$$

̸


<!-- p:38 -->


$$( 7 . 2 ) & & \leq g _ { 3 } ( a , t ) . \\ T h _ { 2 } & \, t h _ { 2 } \, a _ { 2 } \, i _ { 2 } = \frac { 1 } { 2 } \, t h _ { 2 }$$

Then there is a constant C &gt; 0 only depending on α and k such that

$$d _ { K } ( t ^ { - \gamma / \alpha } S _ { t } , Z ) \leq C g ( t ) , \quad t \geq 1 ,$$

$$w h e r e & & \text {where} \\ g ( t ) \coloneqq & \begin{cases} \inf \max \{ a ^ { 1 / 2 - 1 / ( 2 \alpha ) } , g _ { 1 } ( a , t ) , g _ { 2 } ( a , t ) , \sqrt { g _ { 3 } ( a , t ) } \} , & \mu _ { t } = \eta _ { t } , \\ \inf \max \{ a ^ { 1 / 2 - 1 / ( 2 \alpha ) } , g _ { 1 } ( a , t ) , g _ { 2 } ( a , t ) , \sqrt { g _ { 3 } ( a , t ) } , a ^ { 2 } / t \} , & \mu _ { t } = \beta _ { t } . \end{cases} \\ \text {Proof.} & \text { For } a > 0 \text { we define the random variables}$$

where

Proof. For a &gt; 0 we define the random variables

$$S _ { t , a } \colon = \frac { 1 } { k ! } \sum _ { ( x _ { 1 } , \dots , x _ { k } ) \in \mu _ { t , \neq } ^ { k } } 1 ( | h _ { t } ( x _ { 1 } , \dots , x _ { k } ) | \geq t ^ { \gamma / \alpha } a ^ { - 1 / \alpha } ) h _ { t } ( x _ { 1 } , \dots , x _ { k } ) , \quad t \geq 1 ,$$

and

̸

$$Z _ { a } \colon = \sum _ { x \in \zeta } 1 ( | x | \leq a ) \, \text {sign} ( x ) | x | ^ { - 1 / \alpha } .$$

Then, for any a &gt; 0 and ε &gt; 0, we find that

$$T h e n , \, & \text { for any } a > 0 \text { and } \varepsilon > 0 , \, \text { we find that} \\ & \text { } d _ { K } ( t ^ { - \gamma / \alpha } S _ { t } , Z ) \\ & \leq P ( t ^ { - \gamma / \alpha } | S _ { t } - S _ { t , a } | \geq \varepsilon ) + \text {d} _ { K } ( t ^ { - \gamma / \alpha } S _ { t , a } , Z ) \\ & \quad + \sup _ { z \in \mathbb { R } } | P ( Z \leq z ) - P ( Z \leq z + \varepsilon ) | \\ & \leq P ( t ^ { - \gamma / \alpha } | S _ { t } - S _ { t , a } | \geq \varepsilon ) + \text {P} ( | Z - Z _ { a } | \geq \varepsilon ) + \text {d} _ { K } ( t ^ { - \gamma / \alpha } S _ { t , a } , Z _ { a } ) \\ & \quad + 2 \sup _ { z \in \mathbb { R } } | P ( Z \leq z ) - P ( Z \leq z + \varepsilon ) | . \\ & \text {Combining Markov's inequality with the multivariate Mcke formula} \, ( 2 . 1 )$$

Combining Markov's inequality with the multivariate Mecke formula (2.1) and assumption (7.2), we obtain that, for all ε &gt; 0,

and

$$P ( | Z - Z _ { \alpha } | \geq \varepsilon ) \leq \frac { 2 } { \varepsilon } \int _ { a } ^ { \infty } x ^ { - 1 / \alpha } \, d x = \frac { 2 a ^ { 1 - 1 / \alpha } } { ( 1 / \alpha - 1 ) \varepsilon }$$

$$P ( t ^ { - \gamma / \alpha } | S _ { t } - S _ { t , a } | \geq \varepsilon ) \leq \frac { g _ { 3 } ( a , t ) } { \varepsilon } .$$

As α -stable random variable, Z has a bounded density; see [47], page 13. Hence there is a constant C α &gt; 0 only depending on α such that

$$\sup _ { z \in \mathbb { R } } | P ( Z \leq z ) - P ( Z \leq z + \varepsilon ) | \leq C _ { \alpha } \varepsilon , \quad \varepsilon \geq 0 .$$


<!-- p:39 -->


It follows from the definition of the Kolmogorov distance and (2.6) that

$$It \text { follows from the definition of the Kolmogorov distance and (2.6) that} \\ d _ { K } ( t ^ { - \gamma / \alpha } S _ { t , a } , Z _ { a } ) = \sup _ { z \in \mathbb { R } } \left | P \left ( \sum _ { x \in t ^ { \gamma } \bullet \xi _ { t } } 1 ( x \in [ - a , a ] ) \text {sign} ( x ) | x | ^ { - 1 / \alpha } \leq z \right ) \right | \\ - P \left ( \sum _ { x \in \zeta } 1 ( x \in [ - a , a ] ) \text {sign} ( x ) | x | ^ { - 1 / \alpha } \leq z \right ) \right | \\ \leq d _ { K R } ( t ^ { \gamma } \bullet \xi _ { t } | _ { [ - a , a ] } , \zeta | _ { [ - a , a ] } ) . \\ \text {Now we consider the Poisson case and the binomial case separately. For an}$$

Now we consider the Poisson case and the binomial case separately. For an underlying Poisson process, Theorem 3.1 and the assumptions in (7.1) show that

$$d _ { K R } ( t ^ { \gamma } \bullet \xi _ { t } | _ { [ - a , a ] } , \zeta | _ { [ - a , a ] } ) \leq g _ { 1 } ( a , t ) + \frac { 2 ^ { k + 1 } } { k ! } g _ { 2 } ( a , t ) , \quad t \geq 1 .$$

Combining this with the previous estimates, we see that

$$d _ { K } ( t ^ { - \gamma / \alpha } S _ { t } , Z ) & \leq \frac { 2 a ^ { 1 - 1 / \alpha } } { ( 1 / \alpha - 1 ) \varepsilon } + \frac { g _ { 3 } ( a , t ) } { \varepsilon } + 2 C _ { \alpha } \varepsilon + g _ { 1 } ( a , t ) + \frac { 2 ^ { k + 1 } } { k ! } g _ { 2 } ( a , t ) . \\$$

Thus choosing ε = √ max { a 1 - 1 /α , g 3 ( a, t ) } yields the assertion. For the binomial case, Theorem 3.1 and the assumptions in (7.1) imply that

$$d _ { K } ( S _ { t , a } , Z _ { a } ) & \leq \frac { 2 a ^ { 1 - 1 / \alpha } } { ( 1 / \alpha - 1 ) \varepsilon } + \frac { g _ { 3 } ( a , t ) } { \varepsilon } + 2 C _ { \alpha } \varepsilon + g _ { 1 } ( a , t ) \\ & + \frac { 2 ^ { k + 1 } } { k ! } g _ { 2 } ( a , t ) + \frac { 6 ^ { k } k ! } { t } ( 8 a ^ { 2 } + 2 g _ { 1 } ( a , t ) ^ { 2 } ) , \\$$

where we have used that L t ([ - a, a ]) 2 ≤ (2 a + g 1 ( a, t )) 2 ≤ 8 a 2 + 2 g 1 ( a, t ) 2 . Now the same choice for ε as in the Poisson case and the fact that the Kolmogorov distance is bounded by one complete the proof. □

Remark 7.9. For all choices of α ∈ (0 , 2] there are α -stable random variables, and one can think of U-statistics converging to such variables. For α ∈ (1 , 2] and the binomial case this problem was considered in [17, 22, 30]. A technique similar to that used in the proof of Theorem 7.8 should also be applicable if α ∈ (1 , 2]. In this case the limiting random variable is given by Z := lim a →∞ Z a - E Z a , whence an additional centering is necessary. In order to derive bounds similar to those of Theorem 7.8, one has to control the distance between Z and Z a , which might be difficult to tackle. We would like to mention that the bounds derived in [22] also involve a quantity similar to d K ( Z,Z a ).


<!-- p:40 -->


To give an application of Theorem 7.8, let us consider the following distance-power statistics, which are closely related to the edge functionals of random geometric graphs considered above. Let for some d ≥ 1, K ⊂ R d be a compact convex set with volume one, and let K be the restriction of the Lebesgue measure to K . Let η t be a Poisson process in K with intensity measure K t = t K , t ≥ 1, and let β t , t ≥ 1 be a binomial process of ⌈ t ⌉ points, which are independent and uniformly distributed in K . Our aim is to investigate the limiting behavior of the U-statistics

$$S _ { t } \coloneqq \frac { 1 } { 2 } \sum _ { ( x _ { 1 } , x _ { 2 } ) \in \mu _ { t , \neq } ^ { k } } \text {dist} ( x _ { 1 } , x _ { 2 } ) ^ { - \tau } , \quad t \geq 1 ,$$

̸

where τ &gt; 0 and μ t stands for η t or β t . The following result, whose proof will be given in Section 7.4 below, deals with the case τ &gt; d .

Corollary 7.10. Let τ &gt; d , let ζ be a homogeneous Poisson process on R + with intensity one and let Z := ( κ d / 2) τ/d ∑ x ∈ ζ x - τ/d . Then there is a constant C &gt; 0 only depending on K , τ and d such that

with

$$d _ { K } ( t ^ { - 2 \tau / d } S _ { t } , Z ) \leq C t ^ { \varrho } , \quad t \geq 1 ,$$

$$\varrho \coloneqq \inf _ { u > 0 } \max \left \{ \frac { 1 } { 2 } u - \frac { \tau } { 2 d } u , 2 u - 1 , u + \frac { 1 } { d } u - \frac { 2 } { d } \right \} .$$

Example 7.11. To have a more specific example, take τ =2 d in Corollary 7.6, in which case ̺ has the form

$$\text {which case $\varrho$ has the form} \\ \varrho = \inf _ { u > 0 } \max \left \{ - \frac { u } { 2 } , 2 u - 1 , u + \frac { u - 2 } { d } \right \} .$$

For d ∈ { 1 , 2 } the infimum is attained at u = 2 5 , giving that ̺ = - 1 5 . For d ≥ 3, the infimum is attained at u = 4 3 d +2 so that ̺ = - 2 3 d +2 in this case. Thus

where the 1 / 2-stable random variable Z is of the form Z = c d ∑ x ∈ ζ x - 2 for a unit-intensity homogeneous Poisson process ζ on R + and with c d = κ 2 d / 4. The distribution of Z can be characterized more explicitly. Namely, applying [24], Lemma 12.2(i), we see that for all t ∈ R ,

$$d _ { K } ( t ^ { - 4 } S _ { t } , Z ) \leq \begin{cases} C t ^ { - 1 / 5 } , & d \in \{ 1 , 2 \} , \\ C t ^ { - 2 / ( 3 d + 2 ) } , & d \geq 3 , \end{cases} \\ \intertext { t h e 1 / 2 - s t a b l e r a n d o m u r i a b l e Z i s o f t h e f o r m Z = c _ { d } \sum _ { c _ { i } = c _ { j } } }$$

$$[ 2 ] , \, \text {Lemma 12.2} ( i ) , \, \text {we see that for all } t \in \mathbb { R } , \\ \quad \text {Eexp} ( i t Z ) = \text {Eexp} \left ( i t c _ { d } \sum _ { x \in \zeta } x ^ { - 2 } \right ) = \exp \left ( \int _ { 0 } ^ { \infty } ( e ^ { i t c _ { d } x ^ { - 2 } } - 1 ) \, d x \right ) \\ = \exp ( - \sqrt { - i t \pi c _ { d } } ) ,$$


<!-- p:41 -->


where i is the imaginary unit. This is the characteristic function of a centred L ́ evy distribution with scale parameter πc d / 2. Thus Z has density x ↦→ 1 2 √ c d /x 3 exp( - πc d / (4 x )) 1 ( x &gt; 0).

Remark 7.12. Note that if τ &lt; d/ 2, then S t satisfies a central limit theorem as shown in Theorem 3.1 of [37]. Moreover, the choice d/ 2 ≤ τ ≤ d corresponds to the situation α ∈ [1 , 2], to which Remark 7.9 applies.

7.4. Random geometric graphs. Let K ⊂ R d ( d ≥ 1) be a compact convex set with volume one. For t ≥ 1 let μ t either be a homogeneous Poisson process η t of intensity t ≥ 1 in K or a binomial process β t of ⌈ t ⌉ independent and uniformly distributed points in K , and let ( θ t ) t ≥ 1 be a family of positive real numbers. Based on this data we construct a random geometric graph as explained in Section 7.1. In contrast to Corollaries 7.2 and 7.6, where lim t →∞ t 2 θ d t = λ ∈ [0 , ∞ ), we assume at first that lim t →∞ t 2 θ d t = ∞ and are interested in the point process ξ t,a on K defined by

$$\xi _ { t , a } \colon = \frac { 1 } { 2 } \sum _ { ( x , y ) \in \mu _ { t , \neq } ^ { 2 } } 1 ( \| x - y \| \leq \min \{ \theta _ { t } , t ^ { - 2 / d } a \} ) \delta _ { ( x + y ) / 2 }$$

̸

for some a &gt; 0. In other words, ξ t,a charges the collection of all midpoints of edges of the random geometric graph whose length does not exceed t - 2 /d a .

Theorem 7.13. Let a &gt; 0 , let ζ be a Poisson process on K with intensity measure κ d 2 a d vol | K and let ξ t,a be constructed from a Poisson process η t or a binomial process β t with t ≥ 1 . Also suppose that lim t →∞ t 2 θ d t = ∞ . Then t 0 := sup { t ≥ 1: t 2 θ d t &lt;a d } ∪ { 1 } &lt; ∞ , and there is a constant C &gt; 0 only depending on a , d and K such that

$$d _ { K R } ( \xi _ { t , a } , \zeta ) \leq C t ^ { - \min \{ 2 / d , 1 \} } , \quad t > t _ { 0 } .$$

The rest of this subsection is devoted to the proofs of Theorem 7.13 as well as Corollaries 7.2, 7.6 and 7.10. We prepare with the following lemma. In order to deal with the Poisson and the binomial case in parallel, we define χ ( t ) = t 2 and  ̃ χ ( t ) = t 3 if μ t = η t and χ ( t ) = ⌈ t ⌉ ( ⌈ t ⌉ - 1) and  ̃ χ ( t ) = ( ⌈ t ⌉ ) 3 if μ t = β t .

Lemma 7.14. There is a constant C K &gt; 0 only depending on d and K such that

̸

$$\left | \frac { 1 } { 2 } E \sum _ { ( x , y ) \in \mu _ { t , \neq } ^ { 2 } } 1 ( ( x + y ) / 2 \in B , \| x - y \| \in \tilde { A } )$$


<!-- p:42 -->


$$L . \, \text {DECREUSE} \, \text {ND} , \, \text {M. SCHUULETE} \, \text {AN} \, \text {C. THALE} \\ & - \frac { \kappa _ { d } } { 2 } \, v o l ( B ) t ^ { 2 } d \int _ { 0 } ^ { \infty } 1 ( r \in \tilde { A } ) r ^ { d - 1 } \, d r \Big | \\ & \leq 2 C _ { K } \kappa _ { d } t ^ { 2 } ( \tilde { a } ^ { d + 1 } + \tilde { a } ^ { 2 d } ) + \frac { \kappa _ { d } } { 2 } t \tilde { a } ^ { d } \\ \intertext { f o r $ all $ B o r e l $ sets $ B \subset K $ a n d $ \tilde { A } \subset [ 0 , \tilde { a } ] $ w i t h $ \tilde { a } > 0 $ }$$

for all Borel sets B ⊂ K and  ̃ A ⊂ [0 ,  ̃ a ] with  ̃ a &gt; 0 . Moreover,

for all Borel sets B ⊂ K and u ≥ 0 .

$$& \quad \text {for all Borel sets } B \subset K \ \text { and } A \subset [ 0 , a ] \ \text { with } a > 0 . \ \text { Moreover} , \\ & \quad ( 7 . 4 ) \quad \widetilde { \chi } ( t ) \int _ { K } \left ( \int _ { K } 1 ( ( x + y ) / 2 \in B , \| x - y \| \leq u ) \, d x \right ) ^ { 2 } \text {d} y \leq 8 t ^ { 3 } \kappa _ { d } ^ { 2 } u ^ { 2 d } \\ & \quad \text {for all Borel sets } B \subset K \ \text { and } u \geq 0 .$$

Proof. By the multivariate Mecke formula (2.1) for the Poisson process and its analogue (2.2) for the binomial case, we obtain that

̸

$$P O F . \quad & \text {By the multivariate Mcke formula (2.1) for the Poisson process} \\ \text {and its analogue (2.2) for the binomial case, we obtain that} \\ \frac { 1 } { 2 } E \sum _ { ( x , y ) \in \mu _ { k } ^ { 2 } , \neq } 1 ( ( x + y ) / 2 \in B , \| x - y \| \in \tilde { A } ) \\ = & \frac { \chi ( t ) } { 2 } \int _ { K } \int _ { K } 1 ( ( x + y ) / 2 \in B , \| x - y \| \in \tilde { A } ) \, d x \, d y \\ = & \frac { \chi ( t ) } { 2 } \int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { R } ^ { d } } 1 ( ( x + y ) / 2 \in B , \| x - y \| \in \tilde { A } ) \, d x \, d y \\ & - \frac { \chi ( t ) } { 2 } \int _ { ( \mathbb { R } ^ { d } ) ^ { 2 } \langle K ^ { 2 } } 1 ( ( x + y ) / 2 \in B , \| x - y \| \in \tilde { A } ) \, d ( x , y ) . \\ \text {To the first term in the last expression we apply the change of variables} \\ u = & \, x - y \, v = ( x + y ) / 2 \, \text {which has Jacobian one and spherical coordinates}$$

To the first term in the last expression we apply the change of variables u = x - y , v =( x + y ) / 2, which has Jacobian one, and spherical coordinates to see that

$$- \ y , \ v = ( x + y ) / 2 , \text { which has Jacobian one, and spherical coordinate} \\ \text { that } & & \frac { \chi ( t ) } { 2 } \int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { R } ^ { d } } 1 ( ( x + y ) / 2 \in B , \| x - y \| \in \tilde { A } ) \, d x \, d y \\ & = \frac { \chi ( t ) } { 2 } \int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { R } ^ { d } } 1 ( v \in B , \| u \| \in \tilde { A } ) \, d u \, d v \\ & = \frac { \chi ( t ) } { 2 } \, v o l ( B ) d \kappa _ { d } \int _ { 0 } ^ { \infty } 1 ( r \in \tilde { A } ) r ^ { d - 1 } \, d r .$$

A straightforward compuatation shows that

For the second term we have, independently of B , the upper bound

$$\text {the second term we have, independently of } B , \text { the upper bound} \\ \frac { \chi ( t ) } { 2 } \int _ { ( \mathbb { R } ^ { d } ) ^ { \kappa } \ K ^ { 2 } } 1 ( ( x + y ) / 2 \in B , \| x - y \| \in \tilde { A } ) \, d ( x , y ) \\ \leq 2 t ^ { 2 } \, v o l ( \{ x \in \mathbb { R } ^ { d } \ \ K \colon \text {dist} ( x , K ) \leq \tilde { a } \} ) \kappa _ { d } \tilde { a } ^ { d } .$$

$$\text {straightforward computation shows that} \\ \left | ( t ^ { 2 } - \chi ( t ) ) \, v o l ( B ) \frac { \kappa _ { d } } { 2 } d \int _ { 0 } ^ { \infty } 1 ( r \in \tilde { A } ) r ^ { d - 1 } \, d r \right | \leq \frac { \kappa _ { d } } { 2 } t \tilde { a } ^ { d } . \\ \text {or the second term we have, independently of } B , \, the upper bound} \\ \gamma ( t ) \, \lceil \, \iota \, \rceil$$


<!-- p:43 -->


From Steiner's formula (2.7) it follows that there is a constant C K &gt; 0 only depending on d and K such that

$$\ v o l ( \{ x \in \mathbb { R } ^ { d } \ \vee \ K \colon \text {dist} ( x , K ) \leq \tilde { a } \} ) \leq C _ { K } ( \tilde { a } + \tilde { a } ^ { d } ) . \\ \intertext { v o l } \sin v o l \, \ t h o o \, \ e c t i m o t o { \ t h o o } \, \ v i o l d a \ t h o \, \ f r c t \, \ b o w d \, \ O n \ t h o \, \ e t h o r \, h o n$$

$$h a v & & \widetilde { \chi } ( t ) \int _ { K } \left ( \int _ { K } 1 ( ( x + y ) / 2 \in B , \| x - y \| \leq u ) \, d x \right ) ^ { 2 } d y \leq 8 t ^ { 3 } \int _ { K } ( \kappa _ { d } u ^ { d } ) ^ { 2 } \, d y \\ & & = 8 t ^ { 3 } \kappa _ { d } ^ { 2 } u ^ { 2 d } ,$$

Combining these estimates yields the first bound. On the other hand, we have

which is the second bound. □

Proof of Theorem 7.13. Due to our assumption that lim t →∞ t 2 θ d t = ∞ , we have that t 0 := sup { t ≥ 1: t 2 θ d t &lt;a d } ∪ { 1 } &lt; ∞ . Note that min { θ t , t - 2 /d a } = t - 2 /d a for t &gt; t 0 . We denote by L t,a the intensity measure of ξ t,a . For t &gt; t 0 the choice  ̃ A =[0 , min { θ t , t - 2 /d a } ] = [0 , t - 2 /d a ] in (7.3) leads to

$$& > t _ { 0 } \text { the choice } \tilde { A } = [ 0 , \min \{ \theta _ { t } , t ^ { - 2 / d } a \} ] = [ 0 , t ^ { - 2 / d } a ] \text { in } ( 7 . 3 ) \text { leads to } \\ & \quad \left | L _ { t , a } ( B ) - \frac { \kappa _ { d } } { 2 } \text { vol} ( B ) t ^ { 2 } ( t ^ { - 2 / d } a ) ^ { d } \right | \\ & \quad \leq 2 C _ { K } \kappa _ { d } t ^ { 2 } ( t ^ { - 2 - 2 / d } a ^ { d + 1 } + t ^ { - 4 } a ^ { 2 d } ) + \frac { \kappa _ { d } } { 2 } t ^ { - 1 } a ^ { d } \\ & \text {at} \, d _ { T Y } ( \text {I} _ { t _ { 0 } } - \frac { \kappa _ { d } } { 2 } a ^ { d } \text {vol} | _ { K } ) < C _ { 1 } t ^ { - \min \{ 2 / d , 1 \} } \text { for } t > t _ { 0 } \text { with } a \text { constant } C$$

so that d TV ( L t,a , κ d 2 a d vol | K ) ≤ C 1 t - min { 2 /d, 1 } for t &gt; t 0 with a constant C 1 &gt; 0 only depending on a , d and K . Moreover, there is a constant C 2 &gt; 0 only depending on a , d and K such that L t,a ( K ) ≤ C 2 for all t &gt; t 0 . Inequality (7.4) implies that for t &gt; t 0 ,

$$( 7 . 4 ) \text { implies that for } t > t _ { 0 } , \\ \widetilde { \chi } ( t ) \int _ { K } \left ( \int _ { K } 1 ( \| x - y \| \leq \min \{ \theta _ { t } , t ^ { - 2 / d } a \} ) \, d x \right ) ^ { 2 } d y & \leq 8 t ^ { 3 } \kappa _ { d } ^ { 2 } ( t ^ { - 2 / d } a ) ^ { 2 d } \\ & = 8 \kappa _ { d } ^ { 2 } a ^ { 2 d } t ^ { - 1 } .$$

Now, application of Theorem 3.1 completes the proof. □

Proof of Corollary 7.2. The choice B = K and  ̃ A =[0 , θ t ] in (7.3) leads to

$$\text { Proof of COROLLARY 7.2.} \quad & \text { leads to} \\ \left | E _ { t } - \frac { \kappa _ { d } } { 2 } \lambda \right | \leq \left | \frac { \kappa _ { d } } { 2 } \lambda - \frac { \kappa _ { d } } { 2 } t ^ { 2 } \theta _ { t } ^ { d } \right | + \left | E _ { t } - \frac { \kappa _ { d } } { 2 } t ^ { 2 } \theta _ { t } ^ { d } \right | \\ & \leq \frac { \kappa _ { d } } { 2 } | \lambda - t ^ { 2 } \theta _ { t } ^ { d } | + 2 C _ { K } \kappa _ { d } t ^ { 2 } ( \theta _ { t } ^ { d + 1 } + \theta _ { t } ^ { 2 d } ) + \frac { \kappa _ { d } } { 2 } t \theta _ { t } ^ { d } \\ & \leq \frac { \kappa _ { d } } { 2 } | \lambda - t ^ { 2 } \theta _ { t } ^ { d } | + 2 C _ { K } \kappa _ { d } \left ( \frac { ( \sup _ { t \geq 1 } t ^ { 2 } \theta _ { t } ^ { d } ) ^ { 1 + 1 / d } } { t ^ { 2 / d } } + \frac { ( \sup _ { t \geq 1 } t ^ { 2 } \theta _ { t } ^ { d } ) ^ { 2 } } { t ^ { 2 } } \right ) \\ & + \frac { \kappa _ { d } } { 2 } \frac { \sup _ { t \geq 1 } t ^ { 2 } \theta _ { t } ^ { d } } { t }$$


<!-- p:44 -->


for t ≥ 1, which also implies that E E t is bounded by a constant only depending on d , K and sup t ≥ 1 t 2 θ d t for t ≥ 1. It follows from (7.4) that

$$\text {pending on } d , \, K \text { and } \sup _ { t \geq 1 } t ^ { \theta _ { t } ^ { 2 } } \text { for } t \geq 1 . \, \text {it follows from } ( 1 . 4 ) \text { that} \\ \widetilde { \chi } ( t ) \int _ { K } \left ( \int _ { K } 1 ( \| x - y \| \leq \theta _ { t } ) \, d x \right ) ^ { 2 } d y \leq 8 t ^ { 3 } \kappa _ { d } ^ { 2 } \theta _ { t } ^ { 2 d } \leq 8 \kappa _ { d } ^ { 2 } \frac { ( \sup _ { t \geq 1 } t ^ { 2 } \theta _ { t } ^ { d } ) ^ { 2 } } { t } . \\ \text {Now, the assertion is a consequence of Theorem 7.1. } \ \Box$$

̸

$$\text {we define } A ^ { 1 / b } & \colon = \{ a ^ { 1 / b } \colon a \in A \ \{ 0 \} \} . \text { Hence we have that} \\ L _ { t } ( A ) & \colon = \frac { 1 } { k ! } E \sum _ { ( x , y ) \in \mu _ { t , \neq } ^ { 2 } } 1 ( \| x - y \| \leq \theta _ { t } , \| x - y \| ^ { b } \in t ^ { - 2 b / d } A \ \{ 0 \} ) \\ & = \frac { 1 } { k ! } E \sum _ { ( x , y ) \in \mu _ { t , \neq } ^ { 2 } } 1 ( \| x - y \| \in t ^ { - 2 / d } A ^ { 1 / b } \cap [ 0 , \theta _ { t } ] ) . \\ \text {Moreover, we define}$$

Moreover, we define

$$M ( A ) \colon = \frac { \kappa _ { d } } { 2 } d \int _ { 0 } ^ { \lambda ^ { 1 / d } } 1 ( r \in A ^ { 1 / b } ) r ^ { d - 1 } \, d r , \quad A \in \mathcal { B } ( \mathbb { R } ) .$$

For a Borel set A ⊂ [0 , ∞ ), inequality (7.3) with B = K and  ̃ A = t - 2 /d A 1 /b ∩ [0 , θ t ] implies that

$$For a B orel set A \subset [ 0 , \infty ) , \text { inequality } ( 7 . 3 ) \text { with } B = K \text { and } A = t ^ { - 2 / d } A ^ { 1 / b } \cap \\ [ 0 , \theta _ { t } ] \text { implies that } \\ | L _ { t } ( A ) - M ( A ) | \\ \leq \left | \frac { \kappa _ { d } } { 2 } t ^ { 2 } d \int _ { 0 } ^ { \infty } 1 ( r \in t ^ { - 2 / d } A ^ { 1 / b } \cap [ 0 , \theta _ { t } ] ) r ^ { d - 1 } \, d r \\ \\ - \frac { \kappa _ { d } } { 2 } d \int _ { 0 } ^ { \lambda / 1 / d } 1 ( r \in A ^ { 1 / b } ) r ^ { d - 1 } \, d r \right | \\ + 2 C _ { K } \kappa _ { d } t ^ { 2 } ( \theta _ { t } ^ { d + 1 } + \theta _ { t } ^ { 2 d } ) + \frac { \kappa _ { d } } { 2 } t \theta _ { t } ^ { d } \\ \leq \frac { \kappa _ { d } } { 2 } | \lambda - t ^ { 2 } \theta _ { t } ^ { d } | + 2 C _ { K } \kappa _ { d } \left ( \frac { ( \sup _ { t \geq 1 } t ^ { 2 } \theta _ { t } ^ { d } ) ^ { 1 + 1 / d } } { t ^ { 2 / d } } + \frac { ( \sup _ { t \geq 1 } t ^ { 2 } \theta _ { t } ^ { d } ) ^ { 2 } } { t ^ { 2 } } \right ) \\ + \frac { \kappa _ { d } } { 2 } \frac { \sup _ { t \geq 1 } t ^ { 2 } \theta _ { t } ^ { d } } { t } . \\ \text {Hence there are constants } C _ { 1 } , C _ { 2 } > 0 \text { only depending on } d , \, K \text { and } \sup _ { t \geq 1 } t ^ { 2 } \theta _ { t } ^ { d } \\ \text {such that } d _ { T v } ( L _ { t } , M ) \leq C _ { 1 } t ^ { - \min \{ 2 / d , 1 \} } \text { for } t \geq 1 \text { and } L _ { t } ( \mathbb { R } ) \leq C _ { 2 } \text { for } t \geq 1 . \, I t$$

Hence there are constants C 1 , C 2 &gt; 0 only depending on d , K and sup t ≥ 1 t 2 θ d t such that d TV ( L t , M ) ≤ C 1 t - min { 2 /d, 1 } for t ≥ 1 and L t ( R ) ≤ C 2 for t ≥ 1. It follows from (7.4) that

$$\text {follows from } ( \cdot . 4 ) \text { that} \\ \widetilde { \chi } ( t ) \int _ { K } \left ( \int _ { K } 1 ( \| x - y \| \leq \theta _ { t } ) \, d x \right ) ^ { 2 } d y \leq 8 t ^ { 3 } \kappa _ { d } ^ { 2 } \theta _ { t } ^ { 2 d } \leq 8 \kappa _ { d } ^ { 2 } \frac { ( \sup _ { t \geq 1 } t ^ { 2 } \theta _ { t } ^ { d } ) ^ { 2 } } { t } .$$

Proof of Corollary 7.6. We assume that b =0 in the following since for b =0 the assertion follows from Corollary 7.2. For a Borel set A ⊂ [0 , ∞ ) we define A 1 /b := { a 1 /b : a ∈ A \ { 0 }} . Hence we have that

̸


<!-- p:45 -->


Now, application of Theorem 7.4 completes the proof. □

Proof of Corollary 7.10. In the following, we check that the assumptions of Theorem 7.8 are satisfied with h t ( x, y ) = (2 /κ d ) τ/d ‖ x - y ‖ - τ with α = d/τ and γ =2. For a Borel set A ⊂ [0 , ∞ ) and t ≥ 1 we have that

̸

$$t h \ \alpha & = d / \tau \ \text { and } \gamma = 2 . \text { For a Borel set } A \subset [ 0 , \infty ) \ \text { and } t \geq 1 \ \text { we have that} \\ L _ { t } ( A ) & \colon = \frac { 1 } { 2 } E \sum _ { ( x , y ) \in \mu _ { t , \neq } ^ { 2 } } 1 ( \kappa _ { d } | | x - y | | ^ { d } / 2 \in t ^ { - 2 } A ) \\ & = \frac { 1 } { 2 } E \sum _ { ( x , y ) \in \mu _ { t , \neq } ^ { 2 } } 1 ( | | x - y | | \in ( 2 / \kappa _ { d } ) ^ { 1 / d } t ^ { - 2 / d } A ^ { 1 / d } ) \\ & = \frac { 1 } { 2 } E \sum _ { ( x , y ) \in \mu _ { t , \neq } ^ { 2 } } 1 ( | | x - y | | \in ( 2 / \kappa _ { d } ) ^ { 1 / d } t ^ { - 2 / d } A ^ { 1 / d } ) \\$$

̸

with A 1 /d := { x 1 /d : x ∈ A } . In the following let M be the restriction of the Lebesgue measure to R + , and let a &gt; 0. Since

$$\text {Lebesgue measure to } \mathbb { R } _ { + } , & \text { and let } a > 0 . \text { Since} \\ \frac { \kappa _ { d } } { 2 } t ^ { 2 } d \int _ { 0 } ^ { \infty } 1 ( r \in ( 2 / \kappa _ { d } ) ^ { 1 / d } t ^ { - 2 / d } ( A \cap [ 0 , a ] ) ^ { 1 / d } ) r ^ { d - 1 } \, d r \\ & = \frac { \kappa _ { d } } { 2 } t ^ { 2 } \int _ { 0 } ^ { \infty } 1 ( u \in ( 2 / \kappa _ { d } ) t ^ { - 2 } ( A \cap [ 0 , a ] ) ) \, d u = \int _ { 0 } ^ { \infty } 1 ( u \in A \cap [ 0 , a ] ) \, d u \\ & = M | _ { [ 0 , a ] } ( A ) , \\ \text {application of } ( 7 . 3 ) \text { with } B = K \text { and } \hat { A } = ( 2 / \kappa _ { d } ) ^ { 1 / d } t ^ { - 2 / d } ( A \cap [ 0 , a ] ) ^ { 1 / d } \text { yields}$$

application of (7.3) with B = K and  ̃ A =(2 /κ d ) 1 /d t - 2 /d ( A ∩ [0 , a ]) 1 /d yields that

$$| L _ { t } | _ { [ 0 , a ] } ( A ) - M | _ { [ 0 , a ] } ( A ) | \leq 2 C _ { K } \kappa _ { d } t ^ { 2 } ( c _ { a } ^ { d + 1 } t ^ { - 2 - 2 / d } + c _ { a } ^ { 2 d } t ^ { - 4 } ) + \frac { \kappa _ { d } } { 2 } t ^ { - 1 } c _ { a } ^ { d }$$

with c a =(2 a/κ d ) 1 /d . Consequently, there is a constant C 1 &gt; 0 only depending on d and K such that

d TV ( L t | [0 ,a ] , M | [0 ,a ] ) ≤ C 1 ( a 1+1 /d t - 2 /d + a 2 t - 2 + at - 1 ) =: g 1 ( a, t ) , t ≥ 1 . It follows from (7.4) that

$$It follows from ( 7 . 4 ) \text { that} \\ \widetilde { \chi } ( t ) \int _ { K } \left ( \int _ { K } 1 ( \kappa _ { d } \| x - y \| ^ { d } / 2 \leq t ^ { - 2 } a ) \, d x \right ) ^ { 2 } d y \\ = \widetilde { \chi } ( t ) \int _ { K } \left ( \int _ { K } 1 ( \| x - y \| \leq ( 2 / \kappa _ { d } ) ^ { 1 / d } t ^ { - 2 / d } a ^ { 1 / d } ) \, d x \right ) \, d y \\ \leq 8 t ^ { 3 } \kappa _ { d } ^ { 2 } ( 2 / \kappa _ { d } ) ^ { 2 } t ^ { - 4 } a ^ { 2 } = 3 2 t ^ { - 1 } a ^ { 2 } = \colon g _ { 2 } ( a , t ) . \\ \text {Moreover, we have that}$$

Moreover, we have that

$$\frac { t ^ { - 2 \tau / d } } { 2 } \text {E} \sum _ { ( x , y ) \in \mu _ { t , \neq } ^ { 2 } } 1 ( ( 2 / \kappa _ { d } ) ^ { \tau / d } \| x - y \| ^ { - \tau } \leq t ^ { 2 \tau / d } a ^ { - \tau / d } ) ( 2 / \kappa _ { d } ) ^ { \tau / d } \| x - y \| ^ { - \tau }$$

̸


<!-- p:46 -->


$$L . \, \text {DECUSEFUNOD, $M. SCHULTE AND C. THÁLE$} \\ \leq d \kappa _ { d } ( 2 / \kappa _ { d } ) ^ { \tau / d } t ^ { 2 - 2 \tau / d } \int _ { ( \kappa _ { d } / 2 ) ^ { 1 / d } t ^ { - 2 / d } a ^ { 1 / d } } r ^ { - \tau } r ^ { d - 1 } \, d r \\ = \frac { d \kappa _ { d } } { \tau - d } ( \kappa _ { d } / 2 ) ^ { 1 - 2 \tau / d } a ^ { 1 - \tau / d } = \colon g _ { 3 } ( a , t ) . \\ \text {Now, Theorem 7.8 completes the proof. } \Box$$

Now, Theorem 7.8 completes the proof. □

7.5. Proximity of Poisson flats. For a space dimension d ≥ 2 and a dimension parameter m ≥ 1 satisfying m&lt;d/ 2, we investigate the mutual arrangement of the flats of a Poisson m -flat process, that is, a Poisson process on the space of m -dimensional affine subspaces of R d , which are called m -flats. In order to define such a Poisson m -flat process in a rigorous way, recall that G d m and A d m stand for the space of m -dimensional linear and m -dimensional affine subspaces of R d , respectively. Let Q be a probability measure on G d m with the property that two independent random subspaces L,M ∈ G d m with distribution Q are almost surely in general position, meaning that the dimension of the linear hull of L and M is 2 m with probability one. Note that this is satisfied, for example, if Q is absolutely continuous with respect to the unique Haar probability measure on G d m ; cf. [38], Theorem 4.4.5(c). The measure Q induces a translation-invariant measure K t on A d m via

$$\mathbb { A } _ { m } ^ { \mathbb { A } _ { m } ^ { \sigma } \ v i a } \\ ( 7 . 5 ) \quad \int _ { \mathbb { A } _ { m } ^ { d } } g ( E ) \mathbf K _ { t } ( d E ) = t \int _ { \mathbb { G } _ { m } ^ { d } } \int _ { E _ { 0 } ^ { \perp } } g ( E _ { 0 } + x ) \, \text {vol} _ { E _ { 0 } ^ { \perp } } ( d x ) \mathbb { Q } ( d E _ { 0 } ) ,$$

where t ≥ 1 is an intensity parameter, g ≥ 0 is a measurable function on A d m and vol E ⊥ 0 denotes the Lebesgue measure on E ⊥ 0 , the orthogonal complement of E 0 . We use the convention K := K 1 and can re-write K t as K t = t K . We now consider a Poisson process η t with intensity measure K t . This is what is usually called a Poisson m -flat process in stochastic geometry [38], Chapter 4.4. One particular problem for such m -flat processes is to describe the mutual arrangement of the flats in space. Since m&lt;d/ 2, any two different flats E,F of η t do not intersect each other with probability one. Thus they have a well-defined distance dist( E,F ), and we denote by m ( E,F ) the midpoint of the almost surely uniquely determined line segment realizing this distance (the perpendicular of E and F ). We are interested here in the point process of the midpoints m ( E,F ) such that the flats E,F are close together, and m ( E,F ) is in a compact convex set K ⊂ R d of volume 0 &lt; vol( K ) &lt; ∞ . To the best of our knowledge, Theorem 7.15 is the first result describing its asymptotic behavior, as t →∞ . To do so, we define for t ≥ 1 and a &gt; 0, ξ t,a on K by

$$\xi _ { t , a } \colon = \frac { 1 } { 2 } \sum _ { ( E , F ) \in \eta _ { t , \neq } ^ { 2 } } \delta _ { m ( E , F ) } 1 ( \text {dist} ( E , F ) \leq a t ^ { - 2 / ( d - 2 m ) } , m ( E , F ) \in K ) .$$

̸


<!-- p:47 -->


The intensity measure L t,a ( B ) of ξ t,a for a Borel set B ⊂ K is given by

$$1 \, \text {Inc} \, ( E ) \, \overset { 2 } { \ A _ { m } ^ { d } } \, \overset { 2 } { \ A _ { l } ^ { d } } ( E ) \, \overset { 2 } { \ A _ { l , d } ^ { d } } \, \overset { 2 } { \ A _ { l , d } ^ { d } } \, \overset { 2 } { \ A _ { m } ^ { d } } \, \overset { 2 } { \ A _ { m } ^ { d } }$$

due to the multivariate Mecke formula (2.1). It follows from [44], Theorem 1 (it is readily checked that the identity there extends from compact convex sets to general Borel sets) that

$$S C 3 \log C I G C A T ^ { 2 } S C 3 ) \, \text { that} \\ L _ { t , a } ( B ) = \frac { t ^ { 2 } } { 2 } \kappa _ { d - 2 m } ( a t ^ { - 2 / ( d - 2 m ) } ) ^ { d - 2 m } \, \text {vol} ( B ) \int _ { \mathbb { G } _ { k } ^ { d } } \int _ { \mathbb { G } _ { k } ^ { d } } [ M , L ] \mathbb { Q } ( d L ) \mathbb { Q } ( d M ) ,$$

where [ M,L ] stands for the subspace determinant of M and L introduced in Section 2. This leads to

$$\text {in Section 2. The} \text { leads to} \\ L _ { t , a } ( B ) = \frac { \kappa _ { d - 2 m } } { 2 } \text {vol} ( B ) a ^ { d - 2 m } \int _ { \mathbb { G } _ { m } ^ { d } } \int _ { \mathbb { G } _ { m } ^ { d } } [ L , M ] \mathbb { Q } ( \text {d} L ) \mathbb { Q } ( \text {d} M ) .$$

Now, putting

$$Now & , \, \text {putting} \\ & ( 7 . 6 ) & \mathcal { C } \coloneqq \frac { \kappa _ { d - 2 m } } { 2 } \int _ { \mathbb { G } _ { m } ^ { d } } \int _ { \mathbb { G } _ { m } ^ { d } } [ L , M ] \mathbb { Q } ( d L ) \mathbb { Q } ( d M ) ,$$

we see that

where vol | K stands for the restriction of the Lebesgue measure on R d to K . Moreover, the proof of [44], Theorem 3, shows that there is a constant ˆ C &gt; 0 only depending on a , d , m , Q and K such that

$$d _ { T V } ( L _ { t , a } , \mathcal { C } a ^ { d - 2 m } v o l | _ { K } ) = 0 , \\ r _ { 1 } + 1 = 0 ,$$

$$\text {only depending on } a , a , m , \mathbb { Q } \text { and } \mathbb { A } \text { such that} \\ \hat { r } _ { t } \colon = \sup _ { E \in A _ { m } ^ { d } } \ t \int _ { \mathbb { A } _ { m } ^ { d } } 1 ( m ( E , F ) \in K , \text {dist} ( E , F ) \leq a t ^ { - 2 / ( d - 2 m ) } ) \mathbb { K } ( d F ) \leq \hat { C } t ^ { - 1 } .$$

From this we conclude that

$$From this we conclude that \\ r _ { t } \coloneqq t ^ { 3 } \int _ { \mathbb { A } _ { m } ^ { d } } \left ( \int _ { \mathbb { A } _ { m } ^ { d } } 1 ( m ( E , F ) \in K , \text {dist} ( E , F ) \leq a t ^ { - 2 / ( d - 2 m ) } ) K ( d E ) \right ) ^ { 2 } K ( d F ) \\ \leq 2 \hat { C } L _ { t , a } ( K ) t ^ { - 1 } \\ \text {and in view of Theorem 3.1 the following result for the midpoint process}$$

and in view of Theorem 3.1 the following result for the midpoint process ξ t,a .

Theorem 7.15. Let a &gt; 0 , and let ζ be a Poisson process with intensity measure C a d - 2 m vol | K , where C is as at (7.6). Then there is a constant C &gt; 0 depending on a , d , m , Q and K such that

$$d _ { K R } ( \xi _ { t , a } , \zeta ) \leq C t ^ { - 1 } , \quad t \geq 1 .$$


<!-- p:48 -->


Remark 7.16. (i) Note that because of (2.8), the constant C takes the particularly appealing form

$$\mathcal { C } = \frac { 1 } { 2 } \frac { \binom { d - m } { m } } { \binom { d } { m } } \frac { \kappa _ { d - m } ^ { 2 } } { \kappa _ { d } } \\ \text {ar probability measure on}$$

- if Q is the invariant Haar probability measure on G d m (or, equivalently, if the m -flat process is stationary and isotropic; see [38]).
- (ii) As opposed to our previous applications, we do not consider a binomial counterpart to Theorem 7.15. The reason for that is that there is no normalization, which would turn the measure K 1 defined at (7.5) into a probability measure.
- (iii) Theorem 7.15 extends Theorem 7.13 from m = 0 (which has been excluded here for technical reasons) to arbitrary m satisfying m&lt;d/ 2. However, due to the slightly different set-ups (an underlying point process on the compact set K vs. a point process on the noncompact space A d m ), there are boundary effects in the context of Theorem 7.13, implying that the total variation distance d TV ( L t,a , M ) is not identically zero there. These boundary effects are not present for m ≥ 1, which eventually leads to the rate O ( t - 1 ) for the Kantorovich-Rubinstein distance in this case.
### Random polytopes with vertices on the sphere. Let S d - 1 be the unit sphere of dimension d - 1 ( d ≥ 2). Let μ t be a Poisson process η t on S d - 1 whose intensity measure is a constant multiple t ≥ 1 of the normalized spherical Lebesgue measure or a binomial process β t of ⌈ t ⌉ independent and uniformly chosen points on S d - 1 . The convex hull conv( μ t ) of μ t is a random polytope with vertices on S d - 1 , and we denote by D t the diameter of conv( μ t ), that is,

$$D _ { t } \colon = \max _ { ( x , y ) \in \mu _ { t , \neq } ^ { 2 } } \| x - y \| .$$

̸

More generally, define the point process of all reversed interpoint distances by

$$\xi _ { t } = \frac { 1 } { 2 } \sum _ { ( x , y ) \in \mu _ { t , \neq } ^ { 2 } } \delta _ { 2 - \| x - y \| } .$$

̸

Clearly, D t is then two minus the distance from the origin to the closest point of ξ t . We define

$$L _ { t } ( A ) \coloneqq \frac { 1 } { 2 } \mathbf E \sum _ { ( x , y ) \in \mu _ { t , \neq } ^ { 2 } } 1 ( t ^ { 4 / ( d - 1 ) } ( 2 - \| x - y \| ) \in A ) , \quad A \subset \mathbb { R } _ { + } \ B o r e l .$$

̸


<!-- p:49 -->


Fig. 1. Illustration of the argument used in the derivation of Theorem 7.17.

Let χ ( t ) := t 2 in the Poisson case and χ ( t ) := ⌈ t ⌉ ( ⌈ t ⌉ - 1) in the binomial case. Applying the Mecke formula (2.1) or its analogue (2.2) for binomial processes, respectively, we see that

L ([0 , a

$$L _ { t } ( [ 0 , a ] ) \\ = \frac { \chi ( t ) } { 2 ( d \kappa _ { d } ) ^ { 2 } } \int _ { \mathbb { S } ^ { d - 1 } } \int _ { \mathbb { S } ^ { d - 1 } } 1 ( \| x - y \| \geq 2 - a t ^ { - 4 / ( d - 1 ) } ) \mathcal { H } ^ { d - 1 } ( d x ) \mathcal { H } ^ { d - 1 } ( d y ) , \\$$

where dκ d is the surface area of S d - 1 and H d - 1 stands for the ( d - 1)- dimensional Hausdorff measure. For fixed y ∈ S d - 1 , the indicator function is one if and only if the point x is contained in a certain spherical cap S d - 1 ∩ B d ( - y, r ) centered at the antipodal point - y of y , whose radius r has to be determined. For this, we refer to Figure 1 and notice that (2 - s ) 2 + r 2 =4 so that r = √ 4 s - s 2 . Hence the ( d - 1)-dimensional volume of S d - 1 ∩ B d ( - y, r ) is given by

$$( d - 1 ) \kappa _ { d - 1 } \int _ { 0 } ^ { 2 s - s ^ { 2 } / 2 } ( 2 h - h ^ { 2 } ) ^ { ( d - 3 ) / 2 } \, d h ,$$

independently of y . Using the substitution h =2 ut - 4 / ( d - 1) - u 2 t - 8 / ( d - 1) / 2, this means that

$$\text { independently of } y . \text { Using the substitution } h = 2 u t ^ { - 4 / ( d - 1 ) } - u 2 t ^ { - 8 / ( d - 1 ) / 2 } , \\ \text { this means that } & \quad \chi ( t ) \\ L _ { t } ( [ 0 , a ] ) = \frac { \chi ( t ) } { 2 d \kappa _ { d } } ( d - 1 ) \kappa _ { d - 1 } \int _ { 0 } ^ { 2 a t ^ { - 4 / ( d - 1 ) } - a ^ { 2 } t ^ { - 8 / ( d - 1 ) / 2 } } ( 2 h - h ^ { 2 } ) ^ { ( d - 3 ) / 2 } \, d h \\ & = \frac { \chi ( t ) } { 2 d \kappa _ { d } } ( d - 1 ) \kappa _ { d - 1 } \int _ { 0 } ^ { a } ( 4 u t ^ { - 4 / ( d - 1 ) } - u ^ { 2 } t ^ { - 8 / ( d - 1 ) } \\ & - ( 2 u t ^ { - 4 / ( d - 1 ) } - u ^ { 2 } t ^ { - 8 / ( d - 1 ) / 2 } ) ^ { ( d - 3 ) / 2 } \\ & \times ( 2 t ^ { - 4 / ( d - 1 ) } - u t ^ { - 8 / ( d - 1 ) } ) \, d u \\ = \frac { 1 } { 2 d \kappa _ { d } } \frac { \chi ( t ) } { t ^ { 2 } } ( d - 1 ) \kappa _ { d - 1 } \\ & \times \int _ { 0 } ^ { a } ( 4 u - u ^ { 2 } t ^ { - 4 / ( d - 1 ) } - t ^ { - 4 / ( d - 1 ) } ( 2 u - u ^ { 2 } t ^ { - 4 / ( d - 1 ) / 2 } ) ^ { ( d - 3 ) / 2 }$$


<!-- p:50 -->


$$\times ( 2 - u t ^ { - 4 / ( d - 1 ) } ) \, d u . \\$$

Hence we have for any Borel set A ⊂ R + that

$$\text {Hence we have for any Borel set } A \subset \mathbb { R } + \text { that} \\ L _ { t } ( A ) = \frac { ( d - 1 ) \kappa _ { d - 1 } } { 2 d \kappa _ { d } } \frac { \chi ( t ) } { t ^ { 2 } } \\ \times \int _ { A } ( 4 u - u ^ { 2 } t ^ { - 4 / ( d - 1 ) } - t ^ { - 4 / ( d - 1 ) } ( 2 u - u ^ { 2 } t ^ { - 4 / ( d - 1 ) } / 2 ) ^ { 2 } ) ^ { ( d - 3 ) / 2 } \\ \times ( 2 - u t ^ { - 4 / ( d - 1 ) } ) \, d u . \\ \text {The measure } L _ { t } \text { converges, as } t \to \infty \text { and in the strong sense, to a measure}$$

The measure L t converges, as t →∞ and in the strong sense, to a measure M on R + given by

$$M \text { on } \mathbb { W } + \text {given by} \\ ( 7 . 7 ) \quad M ( A ) \colon = \frac { d - 1 } { d \kappa _ { d } } \kappa _ { d - 1 } 2 ^ { d - 3 } \int _ { A } u ^ { ( d - 3 ) / 2 } \, d u , \quad A \subset \mathbb { R } _ { + } \text { Borel} .$$

Moreover, for any bounded Borel set B ⊂ R + there is a constant c 1 ,B &gt; 0 only depending on B and the space dimension d such that

$$d _ { T V } ( L _ { t } | _ { B } , M | _ { B } ) & \leq c _ { 1 , B } t ^ { - \min \{ 4 / ( d - 1 ) , 1 \} } , \quad t \geq 1 . \\ \\ t _ { B } & \quad , \quad t _ { B } = 1 + ( 1 - ( 2 ) - 2 ) ( 2 - 1 ) + 1 - ( 2 ) - 2 + 1 - 1 - ( 2 ) - 2 + 1 .$$

$$\text {above also show that} \\ \hat { r } _ { t } ( B ) \colon = \sup _ { x \in \mathbb { S } ^ { d - 1 } } \frac { \widetilde { \chi } ( t ) } { d \kappa _ { d } } \int _ { \mathbb { S } ^ { d - 1 } } 1 ( 2 - \| x - y \| \in t ^ { - 4 / ( d - 1 ) } B ) \mathcal { H } ^ { d - 1 } ( d y ) \leq c _ { 2 , B } t ^ { - 1 } \\ \text {with } a \text { constant } a _ { s } \mapsto 0 \text { only } d \text { depending on } B \text { and } d \text { so that } 2 \P ( B ) \hat { r } ( B ) <$$

Here, we have used that | χ ( t ) /t 2 - 1 | ≤ t - 1 for t ≥ 1. Let  ̃ χ ( t ) := t in the Poisson case and  ̃ χ ( t ) := ⌈ t ⌉ in the binomial case. The same arguments as above also show that

with a constant c 2 ,B &gt; 0 only depending on B and d so that 2 L t ( B )ˆ r t ( B ) ≤ 2 c 2 ,B L t ( B ) t - 1 . Combining Corollary 3.3 and Remark 3.4(iii), we conclude the following result.

Theorem 7.17. Let ζ be a Poisson process on R + with intensity measure given by (7.7), and let ξ t be derived from a Poisson process η t or a binomial process β t on S d - 1 . Then, for any bounded Borel set B ⊂ R + there is a constant C B,d &gt; 0 only depending on B and d such that

$$d _ { K R } ( ( t ^ { 4 / ( d - 1 ) } \bullet \xi _ { t } ) | _ { B } , \zeta | _ { B } ) & \leq C _ { B , d } t ^ { - \min \{ 4 / ( d - 1 ) , 1 \} } , \quad t \geq 1 . \\ \intertext { d _ { K R } ( ( t ^ { 4 / ( d - 1 ) } \bullet \xi _ { t } ) | _ { B } , \zeta | _ { B } ) & \leq C _ { B , d } t ^ { - \min \{ 4 / ( d - 1 ) , 1 \} } , \quad t \geq 1 .$$

In particular, for the diameter D t of the random polytope, constructed from a Poisson process η t or a binomial process β t , we have

$$| \mathbf P ( t ^ { 4 / ( d - 1 ) } ( 2 - D _ { t } ) > a ) - e ^ { - ( 1 / ( d \kappa _ { d } ) ) \kappa _ { d - 1 } } 2 ^ { d - 2 } a ^ { ( d - 1 ) / 2 } | \leq C _ { a , d } t ^ { - \min \{ 4 / ( d - 1 ) , 1 \} } , \\ t \geq 1 , \\ \intertext { w i t h a c o n s t a n g t }$$

with a constant C a,d &gt; 0 only depending on a &gt; 0 and d .


<!-- p:51 -->


Remark 7.18. The limiting distribution for the diameter is also derived in [31], Theorem 5.2, and [27], Theorem 3.1, where the latter allows the underlying random points to have distributions different from the uniform distribution. While the result in [31] does not give any rates of convergence, in [27], Theorem 3.1, it has erroneously been claimed that the rate of convergence for D t to its limiting Weibull random variable is of order t - 1 . However, in our notation the rate of convergence stated in (2.5) in [27] concerns only the difference to a Weibull random variable with parameter L t ([0 , a ]) and not to a Weibull random variable with parameter M ([0 , a ]) as stated by the authors. For the difference to a Weibull random variable with parameter L t ([0 , a ]), our result also yields a rate of order t - 1 since d TV ( L t | [0 ,a ] , L t | [0 ,a ] ) = 0 in this case.

Acknowledgments. We would like to thank an anonymous referee for valuable hints and comments, which helped us to improve the text.

This research was initiated during the Oberwolfach mini-workshop 'Stochastic Analysis for Poisson Point Processes.' All support is gratefully acknowledged.
