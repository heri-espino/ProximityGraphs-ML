---
id: "Hirsch_2019_Lower-Large-Deviations-Geometric-Functionals"
source_pdf: "../pdf/Hirsch_2019_Lower-Large-Deviations-Geometric-Functionals.pdf"
source_filename: "Hirsch_2019_Lower-Large-Deviations-Geometric-Functionals.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "excellent"
extraction_score: 100.0
visual_assets: "disabled"
references_file: "../references/Hirsch_2019_Lower-Large-Deviations-Geometric-Functionals.references.md"
---

<!-- p:1 -->

## LOWER LARGE DEVIATIONS FOR GEOMETRIC FUNCTIONALS

CHRISTIAN HIRSCH, BENEDIKT JAHNEL, AND ANDR  ́ AS T  ́ OBI  ́ AS

Abstract. This work develops a methodology for analyzing large-deviation lower tails associated with geometric functionals computed on a homogeneous Poisson point process. The technique applies to characteristics expressed in terms of stabilizing score functions exhibiting suitable monotonicity properties. We apply our results to clique counts in the random geometric graph, intrinsic volumes of Poisson-Voronoi cells, as well as power-weighted edge lengths in the random geometric, k -nearest neighbor and relative neighborhood graph.

## 1. Introduction and main results

Considering the field of random graphs, there is a subtle difference in the understanding between upper and lower tails in a large-deviation regime. For instance, when considering the triangle count in the Erd ̋ os-R ́ enyi graph, the probability of observing atypically few triangles is described accurately via very general Poisson-approximation results [Jan90, JW16]. On the other hand, the probability of having too many triangles requires a substantially more specialized and refined analysis [Cha12].

This begs the question whether a similar dichotomy also arises in the large-deviation analysis of functionals that are of geometric rather than combinatorial nature. For instance, Figure 1.1 shows a typical realization of the random geometric graph in comparison to a realization with an atypically small number of edges. In geometric probability, elaborate results are available for large and moderate deviations of geometric functionals exhibiting a similar behavior in the upper and the lower tails [SY01, SY05, ERS15]. However, they prominently do not cover the edge count in the random geometric graph, whose upper tails have been understood only recently [CH14].

In the present work, we provide three general results, Theorems 1.1, 1.2 and 1.3, tailored to studying large-deviation lower tails of geometric functionals. For the proofs, we resort to a method inspired by the idea of sprinkling [ACC + 83]. We perform small changes in those parts of the domain where the underlying point process exhibits highly pathological configurations. After this procedure, we can compare the resulting functionals to approximations that are then amenable to the point-process based large-deviation theory from [GZ93] or [SY01, SY05]. Among the examples covered by our method are clique counts in the random geometric graph, inner volumes of Poisson-Voronoi cells and power-weighted edge lengths in the random geometric, k -nearest neighbor and relative neighborhood graph.

In the rest of this section, we set up the notation and state the main results. Then, Section 2 illustrates those results through the examples. Finally, Section 3 contains the proofs.

We study functionals on a homogeneous Poisson point process X = { X i } i ≥ 1 ⊂ R d with intensity 1, whose distribution on the space N of locally-finite configurations will be denoted by P . Following the framework of [SY01], these functionals are realized as averages of scores associated to the points of X . More precisely, a score function

$$\xi \colon \mathbb { R } ^ { d } \times \mathbb { N } \to [ 0 , \infty )$$

is any bounded measurable function. To simplify notation, we shift the coordinate system to the considered point and write ξ ( X - X i ) = ξ ( X i , X ). In this notation φ ↦→ ξ ( φ ) acts on configurations φ ∈ N o , the family of locally-finite point configurations with a distinguished node at the origin o ∈ R d .

2010 Mathematics Subject Classification. 60K35; 60F10; 82C22.

Key words and phrases. Large deviations; lower tails; stabilizing functionals; random geometric graph; k - nearest neighbor graph; relative neighborhood graph; Voronoi tessellation; clique count.


<!-- p:2 -->


Figure 1.1. Typical realization of the random geometric graph (left) next to a realization having fewer than 75% of the expected number of edges (right).

We then consider lower tails of functionals of the form

$$H _ { n } = H _ { n } ^ { \xi } ( X ) = \frac { 1 } { n ^ { d } } \sum _ { X _ { i } \in X \cap Q _ { n } } \xi ( X - X _ { i } ) ,$$

i.e., averages of the score function over all points in the box Q n = [ - n/ 2 , n/ 2] d of side length n ≥ 1 centered at the origin.

In a first step, we derive upper bounds for the lower tail probabilities. To that end, we work with approximating score functions ξ r that are r -dependent for some r &gt; 0. That is, ξ r ( φ ) = ξ r ( φ ∩ B r ) for every φ ∈ N o , where B r denotes the Euclidean ball of radius r centered at the origin.

To state the main results, we resort to the entropy-based formulation of the large-deviation rate function. We write

$$h ( \mathbb { Q } ) = \lim _ { n \uparrow \infty } \frac { 1 } { n ^ { d } } \int d \mathbb { Q } _ { n } \log \frac { d \mathbb { Q } _ { n } } { d \mathbb { P } _ { n } } \\$$

for the specific relative entropy of a stationary point process Q , where Q n and P n denote the restrictions of Q and P to the box Q n , respectively. If Q n is not absolutely continuous with respect to the restricted Poisson point process, we adhere to the convention that the above integral is infinite. Further, Q o [ ξ ] is the expectation of ξ with respect to the Palm version Q o of Q , see [GZ93] for details. Here is our first main theorem.

Theorem 1.1 (Upper bound) . Let a &gt; 0 and assume the score function ξ to be the pointwise increasing limit of a family { ξ r } r ≥ 1 of r -dependent score functions. Then,

$$\lim _ { n \uparrow \infty } \sup _ { n ^ { d } } \frac { 1 } { n ^ { d } } \log \mathbb { P } ( H _ { n } \leq a ) \leq - \inf _ { \mathbb { Q } \colon \mathbb { Q } ^ { o } [ \xi ] \leq a } h ( \mathbb { Q } ) .$$

For the lower bound, we give two sets of conditions. The first deals with score functions ξ that are increasing in the sense that ξ ( φ ) ≤ ξ ( ψ ) for every φ ⊂ ψ . This applies for instance to clique counts and power-weighted edge lengths in the random geometric graph.

Theorem 1.2 (Lower bound for bounded-range scores) . Let a &gt; 0 and assume the score function ξ to be increasing and r -dependent for some r &gt; 0 . Moreover, assume that for every b &gt; 0 there exists M = M ( b ) &gt; 0 such that ξ ( φ ) ≤ M whenever # φ &lt; b . Then,


<!-- p:3 -->


$$\liminf _ { n \uparrow \infty } \frac { 1 } { n ^ { d } } \log \mathbb { P } ( H _ { n } < a ) \geq - \inf _ { \mathbb { Q } \colon \mathbb { Q } ^ { o } [ \xi ] < a } h ( \mathbb { Q } ) .$$

However, many score functions are neither r -dependent nor increasing, or not even monotone. A prime example is the sum of power-weighted edge lengths in the k -nearest neighbor graph, see Section 2. Still, this example and many other score functions are stabilizing, R -bounded and weakly decreasing in the following sense.

First, a score function ξ is stabilizing if there exists a P o -almost surely finite measurable stabilization radius R : N o → [0 , ∞ ], such that { R ( X ) ≤ r } is measurable with respect to X ∩ B r for every r ≥ 0 and

$$\mathbb { P } ^ { o } ( \xi ( X ) = \xi ( X \cap B _ { R ( X ) } ) ) = 1 .$$

In words, ξ ( X ) does not depend on the configuration outside the ball B R ( X ) . We call R decreasing if R ( φ ∪ { x } ) ≤ R ( φ ) for all φ ∈ N o and x ∈ R d .

Second, ξ is R -bounded if for every δ &gt; 0 and sufficiently large M = M ( δ ) ≥ 1,

$$\mathbb { P } ^ { o } ( \{ R ( X ) \leq M \} \cap \{ \xi ( X ) \geq \delta M ^ { d } \} ) = 0 .$$

Loosely speaking, the score function is negligible compared to the d th power of the stabilization radius.

Third, ξ is weakly decreasing if

$$\mathbb { P } ( \# \{ y \in X \colon \xi ( X \cup \{ o \} - y ) > \xi ( X - y ) \} \leq k ) = 1$$

holds for some k ≥ 1. In words, for all but at most k points of a configuration, adding a new point to the configuration decreases the score function value of the point.

Finally, we need to ensure that sprinkling a sparse configuration of Poisson points yields control on the stabilization radii of the points in a box. More precisely, we assume that the stabilization radius is regular in the following sense. Let X + ,M denote a Poisson point process with intensity M - d that is independent of X . Then, we assume that there exists K 0 &gt; 0 with the following property. For every δ &gt; 0 there exist M 0 = M 0 ( δ ) ≥ 1 and n 0 = n 0 ( δ ) ≥ 1 such that for all M ≥ M 0 and n ≥ n 0 ,

$$\mathbb { P } ( \{ X ^ { + , M } ( Q _ { n } ) \leq K _ { 0 } ( n / M ) ^ { d } \} \cap E _ { n } ^ { M , + } | X ) \geq \exp ( - \delta n ^ { d } )$$

holds almost surely. Here, for φ ∈ N and any measurable subset A ⊂ R d , we write φ ( A ) = # { x ∈ φ : x ∈ A } for the number of points of φ contained in A , and

$$E _ { n } ^ { M , + } = \max _ { X _ { i } \in ( X \cup X ^ { + , M } ) \cap Q _ { n } } R ( ( X \cup X ^ { + , M } ) - X _ { i } ) \leq M$$

denotes the event that after the sprinkling, the stabilization radii of all points in Q n are at most M . Here is the corresponding main result.

Theorem 1.3 (Lower bound for stabilizing scores) . Let a &gt; 0 and ξ be a weakly-decreasing R -bounded score function with a decreasing and regular radius of stabilization. Then, (1.3) remains true.

## 2. Examples

In this section, we discuss how to apply the results announced in Section 1 to a variety of examples arising in geometric probability. More precisely, Sections 2.1, 2.2 and 2.3 are devoted to characteristics for the random geometric graph, the Voronoi tessellation, k -nearest neighbor graphs and relative neighborhood graphs, respectively.


<!-- p:4 -->


### Clique counts and power-weighted edge lengths in random geometric graphs. As a first simple application of our results, consider the set

̸

$$C _ { k } ( \varphi ) = C _ { k , t } ( \varphi ) = \{ \{ x _ { 1 } , \dots , x _ { k } \} \subset \varphi \colon x _ { 1 } = o \text { and } | x _ { i } - x _ { j } | < t \text { for all } i \neq j \}$$

of k -cliques associated to the origin in the geometric graph on φ ∈ N o with connectivity radius t &gt; 0. Then, for k ≥ 2 and α ≥ 0, the score functions

$$\xi _ { k } ( \varphi ) = \frac { 1 } { k } \# C _ { k } ( \varphi ) \quad \text {and} \quad \xi _ { \alpha } ^ { \prime } ( \varphi ) = \frac { 1 } { 2 } \sum _ { x \in \varphi \colon | x | < t } | x | ^ { \alpha }$$

count the number of k -cliques containing the origin and the power-weighted edge lengths at the origin, respectively. Note that ξ k and ξ ′ α are t -dependent and increasing. Additionally, if # φ &lt; b , then ξ k ( φ ) ≤ k - 1 b k - 1 and ξ ′ α ( φ ) ≤ t α b . Hence Theorems 1.1 and 1.2 are applicable.

Further examples arise in the context of topological data analysis. More precisely, the number of k -cliques containing the origin is precisely the number of k -simplices of the Vietoris-Rips complex containing the origin. Similar arguments also apply to the ˇ Cech complex, the second central simplicial complex in topological data analysis. We refer the reader to [BCY18, Section 2.5] for precise definitions and further properties.

2.2. Intrinsic volumes of Voronoi cells. Recall the definition of the Voronoi cell at the origin of a locally-finite configuration φ ∈ N o , i.e.,

$$C _ { o } ( \varphi ) = \{ x \in \mathbb { R } ^ { d } \colon | x | \leq \inf _ { y \in \varphi } | x - y | \} .$$

Recall that since C o ( φ ) is a convex body, its intrinsic volumes v 0 ( C o ) , v 1 ( C o ) , . . . , v d ( C o ) can be computed. They are key characteristics of a convex set, e.g., v 1 , v d - 1 and v d are proportional to the mean width, the surface area and the volume, respectively. We refer the reader to [SW08, Section 14.2] for a precise definition and further properties. In particular, considering v 1 in dimension d = 2, the associated characteristic n d H n becomes the total edge length of the Voronoi graph, so that we obtain a link to the setting studied in [SY05, Section 2.4.1]. Due to the intricate geometry, deriving a full large deviation principle even for a strictly concave function of the edge length was only achieved for a Poisson point process that is restricted to a lattice instead of living in the entire Euclidean space. This example illustrates that even in situations where understanding the large-deviation upper tails requires a delicate geometric analysis, the lower tails may be more accessible.

More precisely, consider the score functions

$$\xi _ { k } ( \varphi ) = v _ { k } ( C _ { o } ( \varphi ) )$$

and note that ξ r k ( φ ) = v k ( C o ( φ ) ∩ B r ) is a 4 r -dependent, pointwise increasing approximation of ξ k ( φ ). Hence, the upper bound of Theorem 1.1 applies.

For the lower bound, the conditions of Theorem 1.3 can be satisfied using the following definitions. The radius of stabilization is described in [Pen07, Section 6.3]: Take any collection { S i } i ∈ I of cones with apex at the origin and angular radius π/ 12 whose union covers R d , where I = I ( d ) ∈ N . Let S + i denote the cone that has the same apex and symmetry hyperplane as S i and has the larger angular radius π/ 6. Then, we define the stabilization radius

$$R ( \varphi ) = 2 \max _ { i \in I } \min _ { x \in \varphi \cap S _ { i } ^ { + } } | x | ,$$

as twice the radius at which the origin has a neighbor in every extended cone. In particular, both R and ξ k are decreasing. Since C o ( φ ) ⊂ B R ( φ ) , we deduce that

$$\xi _ { k } ( \varphi ) \leq v _ { k } ( B _ { R ( \varphi ) } ) = R ( \varphi ) ^ { k } v _ { k } ( B _ { 1 } ) .$$

In particular, ξ k is R -bounded for k &lt; d . Finally, we define for a suitable constant L = L ( d ) ≥ 1 the event

$$A _ { n } ^ { M } = \{ X ^ { + , M } ( Q _ { M / L } ( z ) ) = 1 \text { for all } z \in ( M / L ) \mathbb { Z } ^ { d } \cap Q _ { 2 n } \}$$


<!-- p:5 -->


that X + ,M has precisely one point in each sub-box from an M/L -partition of the box Q 2 n . It follows from the definition of R that the event E M, + n occurs whenever A M n occurs, provided that L is chosen sufficiently large. Moreover, setting K 0 = (2 L ) d , we deduce that X + ,M ( Q n ) ≤ K 0 ( n/M ) d under A M n . Hence, it remains to establish the asserted lower bound on the probability P ( A M n ). Fixing δ &gt; 0 and invoking the independence property of the Poisson point process yields that

$$\mathbb { P } ( A _ { n } ^ { M } ) = \mathbb { P } ( X ^ { + , M } ( Q _ { M / L } ) = 1 ) ^ { ( 2 n L / M ) ^ { d } } = e ^ { - ( 2 n / M ) ^ { d } } L ^ { - ( 2 n L / M ) ^ { d } } \geq e ^ { - \delta n ^ { d } } ,$$

provided that M = M ( δ ) is sufficiently large. Summarizing the above findings, we deduce that Theorem 1.3 can be applied to get the lower bound on the rate function.

- 2.3. Power-weighted edge counts in k -nearest neighbor graphs and relative neighborhood graphs. Finally, we elucidate how to apply Theorem 1.3 to the power-weighted edge count of two central graphs in computational geometry, namely the k -nearest neighbor graph and the relative neighborhood graph. As we shall see, in contrast to the Voronoi example presented in Section 2.2, we encounter here score functions that are weakly decreasing but not decreasing. A full large deviation principle for the total edge length of the k -nearest neighbor graph is described in [SY05, Section 2.3], and we believe that the proof should extend to power-weighted edge lengths with a power strictly less than d . Nevertheless, we apply here our approach towards the large-deviation lower tails as it can be directly adapted to the bidirectional k -nearest neighbor graph, the relative neighborhood graph and possibly further graphs.

In the undirected k -nearest neighbor graph , ξ expresses the powers of distances between any point and the origin, such that at least one of them belongs to the set of k nearest neighbors of the other one. To be more precise,

$$\Re _ { k } ( \varphi ) = \inf \{ r > 0 \colon \varphi ( B _ { r } ) \geq k + 1 \}$$

defines the k -nearest neighbor radius of o in φ ∈ N o . Then, for some α ≥ 0, the score function corresponding to the sum of power-weighted edge lengths of the k -nearest neighbor graph is defined via

$$\xi _ { k , \alpha } ( \varphi ) = \frac { 1 } { 2 } \sum _ { x \in \varphi \colon | x | \leq \Re _ { k } ( \varphi ) \vee \Re _ { k } ( \varphi - x ) } | x | ^ { \alpha } .$$

In particular, we recover the number of edges by setting α = 0. As noted in [Pen07, Section 6.3], to construct a radius of stabilization we can proceed as in (2.1) except for replacing min x ∈ φ ∩ S + i | x | by the distance of the k th closest point from the origin in φ ∩ S + i . Hence, ξ k,α becomes stabilizing with a decreasing stabilization radius. In the same vein, a minor adaptation of the arguments in Section 2.2 yield the regularity and R -boundedness for α &lt; d .

In order to apply Theorem 1.3 for the lower bound, it remains to verify the following.

Lemma 2.1. ξ k,α is weakly decreasing.

Proof. Let us call φ ∈ N nonequidistant if for all y, z, v, w ∈ φ , | y - z | = | v - w | &gt; 0 implies { y, z } = { v, w } . First note that for any x ∈ R d , under P , almost all configurations φ ∪ { x } are nonequidistant. We claim that for any nonequidistant configuration φ ∪ { x } , we have for all but at most k points y ∈ φ that

$$\xi _ { k } ( \varphi \cup \{ x \} - y ) \leq \xi _ { k } ( \varphi - y ) .$$

Indeed, for y ∈ φ , let us define the set of k nearest neighbors of y in φ as follows

$$k N N ( \varphi , y ) = \left ( B _ { \Re _ { k } ( \varphi - y ) } ( y ) \cap \varphi \right ) \ \{ y \} .$$

Now, if y ∈ k NN( φ ∪{ x } , x ), then possibly ξ k ( φ ∪{ x }- y ) &gt; ξ k ( φ - y ). We claim that else (2.4) holds. Indeed, if y / ∈ k NN( φ ∪ { x } , x ), then there are two possibilities. If x ∈ k NN( φ ∪ { x } , y ), then x replaced precisely one neighbor z of y and is closer to y than z . More precisely, note that | x - y | ≤ R k ( φ ∪ { x } - y ) ≤ R k ( φ - y ). Hence, there exists z ∈ k NN( φ, y ) such that | z - y | = R k ( φ - y ) and z / ∈ k NN( φ ∪{ x } , y ), the neighbor of y that is replaced by x . Additionally, for any w ∈ k NN( φ, y ) \ { z } also w ∈ k NN( φ ∪ { x } , y ). Further, also for any v ∈ φ such that y ∈ k NN( φ ∪ { x } , v ) we have y ∈ k NN( φ, v ). Hence,


<!-- p:6 -->


$$\xi _ { k } ( \varphi \cup \{ x \} - y ) - \xi _ { k } ( \varphi - y ) \leq | x - y | ^ { \alpha } - | z - y | ^ { \alpha } \leq 0 ,$$

which is (2.4). The other possibility is that x / ∈ k NN( φ ∪ { x } , y ). Then the addition of x can only remove edges that were present due to the fact that some other point had y as a neighbor. In this case, ξ ( φ ∪ { x } - y ) = ξ ( φ - y ) unless there exists z ∈ φ such that y ∈ k NN( φ, z ) but y / ∈ k NN( φ ∪ { x } , z ), which must be due to the property that x ∈ k NN( φ ∪ { x } , z ). So again, the addition of x can only remove such an edge and hence again (2.4) holds for y . □

Note that the approach presented above also applies to further graphs studied in computational geometry. The most immediate adaptation concerns the bidirectional k -nearest neighbor graph , see [BB13], where in the definition of the score function, we replace R k ( φ ) ∨ R k ( φ - x ) by R k ( φ ) ∧ R k ( φ - x ). Not only can we take the same radius of stabilization, but also Lemma 2.1 remains valid. As a third example, we showcase the relative neighborhood graph . Here, for α ≥ 0 and φ ∈ N o the score function is given by

$$\xi _ { R N } ( \varphi ) = \frac { 1 } { 2 } \sum _ { x \in \varphi \colon \varphi \cap B _ { | x | } ( o ) \cap B _ { | x | } ( x ) = \emptyset } | x | ^ { \alpha } .$$

The relative neighborhood graph is a sub-graph of the Delaunay tessellation, and in fact we can reuse the radius of stabilization from Section 2.2. Finally, proving the analog of Lemma 2.1 reduces to the observation that the degree of every node in the relative neighborhood graph is bounded by a constant K = K ( d ), see [JT92, Section IV]. What remains to be verified is that ξ RN is weakly decreasing.

Lemma 2.2. ξ RN is weakly decreasing.

Proof. We claim that for any nonequidistant configuration φ ∪ { x } with φ ∈ N , for all but at most K points y ∈ φ ,

$$\xi _ { R N } ( \varphi \cup \{ x \} - y ) \leq \xi _ { R N } ( \varphi - y )$$

holds. Indeed, for y ∈ φ , let us define the set of relative neighbors of y in φ as follows

$$R N ( \varphi , y ) \colon = \{ z \in \varphi \ \{ y \} \colon \varphi \cap B _ { | z - y | } ( y ) \cap B _ { | z - y | } ( z ) = \emptyset \} ,$$

and note that z ∈ RN( φ, y ) if and only if y ∈ RN( φ, z ). In particular, #RN( φ, y ) ≤ K for any y ∈ φ . So, if y ∈ RN( φ ∪ { x } , x ), then possibly ξ RN ( φ ∪ { x } - y ) &gt; ξ RN ( φ - y ). But if y / ∈ RN( φ ∪ { x } , x ), then

as asserted.

$$\xi _ { R N } ( \varphi \cup \{ x \} - y ) - \xi _ { R N } ( \varphi - y ) \\ = \frac { 1 } { 2 } \sum _ { z \in \varphi - y } | z - y | ^ { \alpha } \left ( \mathbb { 1 } \{ z \in R N ( \varphi \cup \{ x \} , y ) \} - \mathbb { 1 } \{ z \in R N ( \varphi , y ) \} \right ) \leq 0 , \\ \intertext { s a s s e r t e d . }$$

## 3. Proofs

In this section we provide the proofs of the main theorems.

3.1. Proof of Theorem 1.1. The proof of the upper bound relies on the level-3 large deviation principle for the Poisson point process from [GZ93, Theorem 3.1].

Proof of Theorem 1.1. Replacing ξ r by ξ r ∧ r if necessary, we may assume that ξ r is bounded above by r . Then, ξ r is a bounded local observable, so that by the contraction principle [DZ98, Theorem 4.2.10] and [GZ93, Theorem 3.1],

$$\lim _ { n \uparrow \infty } \sup _ { n ^ { d } } \frac { 1 } { n ^ { d } } \log \mathbb { P } ( H _ { n } \leq a ) \leq \lim _ { n \uparrow \infty } \sup _ { n } \frac { 1 } { n ^ { d } } \log \mathbb { P } ( H _ { n } ^ { \xi ^ { r } } \leq a ) \leq - \inf _ { \mathbb { Q } \colon \mathbb { Q } ^ { r } [ \xi ^ { r } ] \leq a } h ( \mathbb { Q } ) .$$

□


<!-- p:7 -->


Hence, it suffices to show that

-

$$- \lim _ { r \uparrow \infty } \inf _ { \mathbb { Q } \colon \mathbb { Q } ^ { o } [ \xi ^ { r } ] \leq a } h ( \mathbb { Q } ) \leq - \inf _ { \mathbb { Q } \colon \mathbb { Q } ^ { o } [ \xi ] \leq a } h ( \mathbb { Q } ) .$$

Let { Q k } k ≥ 1 be a family of stationary point processes such that Q o k [ ξ k ] ≤ a and

$$\lim _ { k \uparrow \infty } h ( \mathbb { Q } _ { k } ) = \lim _ { r \uparrow \infty } \inf _ { \mathbb { Q } \colon \mathbb { Q } ^ { o } [ \xi ^ { r } ] \leq a } h ( \mathbb { Q } ) .$$

Let Q ∗ be a subsequential limit of { Q k } k ≥ 1 . To simplify the presentation, we may assume Q ∗ to be the limit of { Q k } k ≥ 1 . Then, by monotone convergence,

$$\mathbb { Q } _ { * } ^ { o } [ \xi ] \leq \lim _ { r \uparrow \infty } \mathbb { Q } _ { * } ^ { o } [ \xi ^ { r } ] = \lim _ { r \uparrow \infty } \lim _ { k \uparrow \infty } \mathbb { Q } _ { k } ^ { o } [ \xi ^ { r } ] \leq \lim _ { k \uparrow \infty } \sup _ { k } \mathbb { Q } _ { k } ^ { o } [ \xi ^ { k } ] \leq a .$$

Since the specific relative entropy h is lower semicontinuous, we arrive at

$$\liminf _ { k \uparrow \infty } h ( \mathbb { Q } _ { k } ) \geq h ( \mathbb { Q } _ { * } ) \geq \inf _ { \mathbb { Q } \colon \mathbb { Q } ^ { o } [ \xi ] \leq a } h ( \mathbb { Q } ) ,$$

as asserted.

□

3.2. Proof of Theorem 1.2. To prove Theorem 1.2, we consider the truncation ξ M = ξ ∧ M of the original increasing and r -dependent score function ξ at a large threshold M &gt; 1 and write H n M = H ξ M n . In comparison to the arguments in Section 3.1, the proof of the lower bound is more involved, since we can no longer replace P ( H n ≤ a ) by P ( H n M ≤ a ). Instead, we rely on a sprinkling approach. For this method to work, we need that the total number of points in pathological areas is small with high probability. More precisely, we say that a point X i ∈ X is b -dense if X ( Q r ( X i )) &gt; b and write

$$N _ { b , n } = N _ { b , n } ( X ) = \# \{ X _ { i } \in X \cap Q _ { n } \, \colon \, X _ { i } \text { is dense} \}$$

for the total number of b -dense points in Q n . Then, b -dense points are indeed rare.

Lemma 3.1 (Rareness of b -dense points) . Let δ &gt; 0 . Then,

$$\lim _ { b \uparrow \infty } \sup _ { n \uparrow \infty } \sup _ { n \uparrow \infty } \frac { 1 } { n ^ { d } } \log \mathbb { P } ( N _ { b , n } > \delta n ^ { d } ) = - \infty .$$

In the second step, we remove all b -dense points through the coupling. That is, we let X - ,ε be an independent thinning of X with survival probability 1 - ε . Furthermore, we let X + ,ε be an independent Poisson point process with intensity ε &gt; 0. Then, the coupled process

$$X ^ { \varepsilon } = X ^ { - , \varepsilon } \cup X ^ { + , \varepsilon }$$

is again a Poisson point process with intensity 1. Now, let

$$E _ { b , n } = \{ X ^ { + , \varepsilon } \cap Q _ { n } = \emptyset \} \cap \{ X ^ { - , \varepsilon } \cap Q _ { n } \text { has no } b \text {-dense points} \}$$

be the event that X + ,ε has no points in Q n and that X - ,ε does not contain any b -dense points in Q n .

Lemma 3.2 (Removal of b -dense points) . Let b, n, ε &gt; 0 . Then, P -almost surely,

$$\mathbb { P } ( E _ { b , n } | X ) \geq \exp ( - \varepsilon n ^ { d } + N _ { b , n } \log ( \varepsilon ) ) .$$

Before showing Lemmas 3.1 and 3.2, we illustrate how they enter the proof of (1.3).

Proof of Theorem 1.2. Let M &gt; 0. Then, by [GZ93, Theorem 3.1],

$$\liminf _ { n \uparrow \infty } \frac { 1 } { n ^ { d } } \log \mathbb { P } ( H _ { n } ^ { M } < a ) \geq - \inf _ { \mathbb { Q } \colon \mathbb { Q } ^ { o } [ \xi ^ { M } ] < a } h ( \mathbb { Q } ) \geq - \inf _ { \mathbb { Q } \colon \mathbb { Q } ^ { o } [ \xi ] < a } h ( \mathbb { Q } ) .$$

Hence, it remains to show that

$$\liminf _ { n \uparrow \infty } \frac { 1 } { n ^ { d } } \log \mathbb { P } ( H _ { n } < a ) \geq \liminf _ { M \uparrow \infty } \liminf _ { n \uparrow \infty } \frac { 1 } { n ^ { d } } \log \mathbb { P } ( H _ { n } ^ { M } < a ) .$$


<!-- p:8 -->


Let b, δ, ε &gt; 0 be arbitrary. Now, since ξ is increasing,

$$& \mathbb { P } ( H _ { n } < a ) = \mathbb { P } ( H _ { n } ( X ^ { \varepsilon } ) < a ) \geq \mathbb { P } ( \{ H _ { n } ^ { M ( b ) } < a \} \cap E _ { b , n } ) = \mathbb { E } [ \mathbb { I } \{ H _ { n } ^ { M ( b ) } < a \} \mathbb { P } [ E _ { b , n } \, | \, X ] ] . \\ & \text {Thus, by Lemma 3.2,} \\ & \mathbb { P } ( H _ { n } < a ) > \exp ( - \varepsilon n ^ { d } ) \mathbb { E } [ \mathbb { I } \{ H _ { n } ^ { M ( b ) } < a \} \xi ^ { N _ { b , n } } ]$$

Since X and X ε share the same distribution, Lemma 3.1 allows us to choose b = b ( δ ) &gt; 0 sufficiently large such that

$$\mathbb { P } ( H _ { n } < a ) & \geq \exp ( - \varepsilon n ^ { d } ) \mathbb { E } [ 1 \{ H _ { n } ^ { M ( b ) } < a \} \varepsilon ^ { N _ { b , n } } ] \\ & \geq \exp \left ( ( \delta \log ( \varepsilon ) - \varepsilon ) n ^ { d } \right ) \mathbb { P } ( H _ { n } ^ { M ( b ) } < a ) - \mathbb { P } ( N _ { b , n } > \delta n ^ { d } ) . \\ \text {Once } X \text { and } X ^ { \varepsilon } \text { share the same distribution} . \ \text {Lemma } 3 . 1 \text { allows us to choose } b = h ( \delta ) \geq$$

$$\liminf _ { n \uparrow \infty } \frac { 1 } { n ^ { d } } \log \mathbb { P } ( H _ { n } < a ) \geq \delta \log ( \varepsilon ) - \varepsilon + \liminf _ { n \uparrow \infty } \frac { 1 } { n ^ { d } } \log \mathbb { P } ( H _ { n } ^ { M ( b ) } < a ) .$$

Hence, sending ε ↓ 0, δ ↓ 0, and b ↑ ∞ concludes the proof of (3.1).

□

Proof of Lemma 3.1. Consider a subdivision of Q n , for sufficiently large n ≥ 1, into sub-boxes Q a ( z i ) = z i + Q a of side length a &gt; r where z i ∈ a Z d . Let N i = X ( Q a ( z i )) be the number of points in the i th sub-box and N ′ i = X ( Q 3 a ( z i )) be the number of points the i th sub-box plus its adjacent sub-boxes. Then, N b,n ≤ N ′′ b,n , where

$$N _ { b , n } ^ { \prime \prime } = \sum _ { i \in a \mathbb { Z } ^ { d } \cap Q _ { n } } N _ { i } \mathbb { I } \{ N _ { i } ^ { \prime } > b \} , \\ \text {Markov inequality} , \text { for all } t > 0 ,$$

so that by the exponential Markov inequality, for all t &gt; 0,

$$\log \mathbb { P } ( N _ { b , n } > \delta n ^ { d } ) \leq \log \mathbb { P } ( N _ { b , n } ^ { \prime \prime } > \delta n ^ { d } ) \leq - \delta t n ^ { d } + \log \mathbb { E } [ \exp ( t N _ { b , n } ^ { \prime \prime } ) ] .$$

Since the random variables N i ✶ { N ′ i &gt; b } and N j ✶ { N ′ j &gt; b } are independent whenever ‖ z i - z j ‖ ∞ ≥ 3, we have 3 d regular sub-grids of a Z d containing independent random variables N i ✶ { N ′ i &gt; b } . Thus, using H ̈ older's inequality, independence and the dominated convergence theorem, we arrive at

□

$$\lim _ { b \uparrow \infty } & \sup \lim s _ { n \uparrow \infty } \frac { 1 } { n ^ { d } } \log \mathbb { E } [ \exp ( t N _ { b , n } ^ { \prime \prime } ) ] \leq \frac { 1 } { ( 3 a ) ^ { d } } \lim s u p \log \mathbb { E } [ \exp ( 3 ^ { d } t N _ { o } \mathbb { 1 } \{ N _ { o } ^ { \prime } > b \} ) ] = \frac { 1 } { ( 3 a ) ^ { d } } . \\ \text {Since } & t > 0 \text { was arbitrary, we conclude the proof.} & \square$$

Proof of Lemma 3.2. First, since X + ,ε and X - ,ε are independent, it suffices to compute

$$\mathbb { P } ( X ^ { + , \varepsilon } \cap Q _ { n } = \emptyset \, | \, X ) \quad \text { and } \quad \mathbb { P } ( X ^ { - , \varepsilon } \cap Q _ { n } \ h a s \ n o \ b { \text {dense points} } \ | \, X )$$

separately. The void probabilities for a Poisson point process give that

$$\mathbb { P } ( X ^ { + , \varepsilon } \cap Q _ { n } = \emptyset \, | \, X ) = \exp ( - \varepsilon n ^ { d } ) .$$

Next, since X - ,ε is an independent thinning of X with probability ε , we arrive at

$$\mathbb { P } ( X ^ { - , \varepsilon } \cap Q _ { n } \text { has no } b { \text {-dense points} } | X ) \geq \varepsilon ^ { N _ { b , n } } ,$$

- [ ] as asserted. □

### Proof of Theorem 1.3. In order to prove the lower bound for stabilizing score functions, we use sprinkling to regularize sub-regions that are not sufficiently stabilized. Let us define the approximation

$$\xi ^ { \delta , M } ( \varphi ) = \xi ( \varphi \cap Q _ { M } ) \wedge \delta M ^ { d }$$

and write H δ,M n = H ξ δ,M n .

Similarly as before, we consider a coupling construction. Now, we let X - ,M denote an independent thinning of X with survival probability 1 - M - d and X + ,M an independent Poisson point process with intensity M - d . Then,

$$X ^ { M } = X ^ { - , M } \cup X ^ { + , M }$$

defines a unit-intensity Poisson point process.


<!-- p:9 -->


In this coupling, we consider events in which the sprinkling X + ,M adds points wherever necessary to reduce the stabilization radius. More precisely, let

$$E _ { n } ^ { M } = \{ X ^ { - , M } \cap Q _ { n } = X \cap Q _ { n } \} \cap \{ X ^ { + , M } ( Q _ { n } ) \leq K _ { 0 } ( n / M ) ^ { d } \} \cap E _ { n } ^ { M , + } .$$

As we shall prove below, the events E n M occur with a high probability.

Lemma 3.3 (Sprinkling regularizes with high probability) . Let δ &gt; 0 and n ≥ M ≥ 1 sufficiently large. Then, under the assumptions of Theorem 1.3, P -almost surely,

$$\mathbb { P } ( E _ { n } ^ { M } | X ) \geq \exp \left ( X ( Q _ { n } ) \log ( 1 - M ^ { - d } ) - \delta n ^ { d } \right ) .$$

Proof. Indeed, for given X , the event { X - ,M ∩ Q n = X ∩ Q n } has probability (1 - M - d ) X ( Q n ) and is independent of the event { X + ,M ( Q n ) ≤ K 0 ( n/M ) d } ∩ E M, + n , which has probability at least exp( - δn d ). □

Now, we conclude the proof of Theorem 1.3.

Proof of Theorem 1.3. Let δ &gt; 0 and M = M ( δ ) &gt; 1 sufficiently large. Then, by R -boundedness,

$$\mathbb { P } ( H _ { n } < a ) = \mathbb { P } ( H _ { n } ( X ^ { M } ) < a ) \geq \mathbb { P } ( \{ H _ { n } ^ { \delta , M } ( X ^ { M } ) < a \} \cap E _ { n } ^ { M } ) .$$

Moreover, under the event E n M ,

$$H _ { n } ^ { \delta , M } ( X ^ { M } ) & = \frac { 1 } { n ^ { d } } \sum _ { X _ { i } \in X ^ { + } , M \cap Q _ { r } } \xi ^ { \delta , M } ( X ^ { M } - X _ { i } ) + \frac { 1 } { n ^ { d } } \sum _ { X _ { i } \in X \cap Q _ { n } } \xi ^ { \delta , M } ( X ^ { M } - X _ { i } ) \\ & \leq K _ { 0 } \delta + H _ { n } ^ { \delta , M } ( X ) + \frac { 1 } { n ^ { d } } \sum _ { X _ { i } \in X \cap Q _ { n } } \left ( \xi ^ { \delta , M } ( X ^ { M } - X _ { i } ) - \xi ^ { \delta , M } ( X - X _ { i } ) \right ) .$$

Let us write X M, 0 = X and X M,j +1 = X M,j ∪{ X + ,M j } where { X + ,M j } 1 ≤ j ≤ N ( M ) is an arbitrary ordering of X + ,M . Then, since ξ is weakly decreasing,

$$\text {ordering of } X ^ { + , M } . \text { Then, since } \xi \text { is weakly decreasing} , \\ \sum _ { X _ { i } \in X \cap Q _ { n } } ( \xi ^ { \delta , M } ( X ^ { M } - X _ { i } ) - \xi ^ { \delta , M } ( X - X _ { i } ) ) \\ = \sum _ { X _ { i } \in X \cap Q _ { n } } \sum _ { j < N ( M ) } ( \xi ^ { \delta , M } ( X ^ { M , j } - X _ { i } ) - \xi ^ { \delta , M } ( X ^ { M , j - 1 } - X _ { i } ) ) \\ \leq \delta M ^ { d } \sum _ { j \leq N ( M ) } \sum _ { X _ { i } \in X \cap Q _ { n } } \mathbb { 1 } \{ \xi ^ { \delta , M } ( X ^ { M , j } - X _ { i } ) > \xi ^ { \delta , M } ( X ^ { M , j - 1 } - X _ { i } ) \} \\ \leq k \delta M ^ { d } N ( M ) . \\ \text {Further note that } N ( M ) < K _ { 0 } ( n / M ) ^ { d } , \text { and thus we arrive at }$$

Further note that N ( M ) ≤ K 0 ( n/M ) d , and thus we arrive at

$$\mathbb { P } ( H _ { n } ( X ^ { M } ) < a ) \geq \mathbb { P } ( \{ H _ { n } ^ { \delta , M } ( X ^ { M } ) < a \} \cap E _ { n } ^ { M } ) \geq \mathbb { P } ( \{ H _ { n } ^ { \delta , M } ( X ) < a - 2 k K _ { 0 } \delta \} \cap E _ { n } ^ { M } ) .$$

Now, by conditioning on X and applying Lemma 3.3 for sufficiently large n ≥ M ≥

Moreover, for any c &gt; 0,

$$\mathbb { E } [ \mathbb { 1 } \{ H _ { n } ^ { \delta , M } ( X ) < a - 2 k K _ { 0 } \delta \} \exp \left ( X ( Q _ { n } ) \log ( 1 - M ^ { - d } ) \right ) ] \\ \geq \exp \left ( c n ^ { d } \log ( 1 - M ^ { - d } ) \right ) \mathbb { P } ( \{ H _ { n } ^ { \delta , M } ( X ) < a - 2 k K _ { 0 } \delta \} \cap \{ X ( Q _ { n } ) < c n ^ { d } \} ) , \\ \text {where for the first factor} .$$

n n n n 1,

$$\mathbb { P } ( H _ { n } ( X ^ { M } ) < a ) & \geq \mathbb { E } \left [ \mathbb { 1 } \{ H _ { n } ^ { \delta , M } ( X ) < a - 2 k K _ { 0 } \delta \} \mathbb { P } ( E _ { n } ^ { M } \ | X ) \right ] \\ & \geq \mathbb { E } \left [ \mathbb { 1 } \{ H _ { n } ^ { \delta , M } ( X ) < a - 2 k K _ { 0 } \delta \} \exp \left ( X ( Q _ { n } ) \log ( 1 - M ^ { - d } ) \right ) \right ] \exp ( - \delta n ^ { d } ) . \\ \text {Moreover, for any } c & > 0 , \\ \mathbb { E } \left [ \mathbb { 1 } \{ H _ { n } ^ { \delta , M } ( X ) < a - 2 k K _ { 0 } \delta \} \exp \left ( X ( Q _ { n } ) \log ( 1 - M ^ { - d } ) \right ) \right ]$$

where for the first factor,

$$\liminf _ { M \uparrow \infty } \frac { 1 } { n ^ { d } } \log \left ( \exp \left ( c n ^ { d } \log ( 1 - M ^ { - d } ) \right ) \right ) = \liminf _ { M \uparrow \infty } c \log ( 1 - M ^ { - d } ) = 0 .$$


<!-- p:10 -->


Now, for the second factor,

$$\mathbb { P } ( \{ H _ { n } ^ { \delta , M } ( X ) < a - 2 k K _ { 0 } \delta \} \cap \{ X ( Q _ { n } ) < c n ^ { d } \} ) & \geq \mathbb { P } ( H _ { n } ^ { \delta , M } ( X ) < a - 2 k K _ { 0 } \delta ) \\ & - \mathbb { P } ( X ( Q _ { n } ) \geq c n ^ { d } ) ,$$

where for large c the second summand plays no role in the large deviations. Applying [GZ93, Theorem 3.1] on the local bounded observable ξ δ,M yields that

$$\liminf _ { n \uparrow \infty } \frac { 1 } { n ^ { d } } \log \mathbb { P } ( H _ { n } ^ { \delta , M } ( X ) < a - 2 k K _ { 0 } \delta ) \geq - \inf _ { \mathbb { Q } \colon \mathbb { Q } ^ { o } [ \xi ^ { \delta , M } ] < a - 2 k K _ { 0 } \delta } h ( \mathbb { Q } ) .$$

Finally, if Q o [ ξ ] &lt; a , then lim sup M ↑∞ Q o [ ξ δ,M ] &lt; a - 2 kK 0 δ for a sufficiently small δ &gt; 0, so that

$$\liminf _ { M \uparrow \infty } \left ( - \inf _ { \mathbb { Q } \colon \mathbb { Q } ^ { o } [ \xi ^ { \delta , M } ] < a - 2 k K _ { 0 } \delta } h ( \mathbb { Q } ) \right ) \geq - \inf _ { \mathbb { Q } \colon \mathbb { Q } ^ { o } [ \xi ] < a } h ( \mathbb { Q } ) ,$$
