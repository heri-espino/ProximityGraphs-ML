---
id: "Devroye_1988_Expected-Size-Computational-Geometry-Graphs"
source_pdf: "../pdf/Devroye_1988_Expected-Size-Computational-Geometry-Graphs.pdf"
source_filename: "Devroye_1988_Expected-Size-Computational-Geometry-Graphs.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "full-page-ocr"
extraction_quality: "excellent"
extraction_score: 98.0
visual_assets: "disabled"
references_file: "../references/Devroye_1988_Expected-Size-Computational-Geometry-Graphs.references.md"
---

<!-- p:1 -->

### THE EXPECTED SIZE OF SOME GRAPHS IN COMPUTATIONAL GEOMETRY

### L. DEVROYE

School of Computer Science, McGill University, Montreal, Quebec H3A 2K6, Canada

(Received 18 August 1987)

Communicated by E. Y. Rodin

Abstract—We consider n independent points with a common but arbitrary density f in Ra. Two points (X,, X) are joined by an edge when a certain set S(X, X,) does not contain any other data points. The expected number E(N) of edges in the graph depends upon n, f and the definition of S. Examples include rectangles, spheres and loons; these lead to the graph of all dominance pairs, the Gabriel graph and the relative neighborhood graph, respectively. Other graphs covered by our analysis include the nearest ne   l      et  t  o er bounds that do not depend upon f (and are hence useful in all applications involving these graphs, since we usually do not know f ). For sparse graphs, exact asymptotic constants are obtained for È(N) that are valid for all densities.

## 1. INTRODUCTION

We consider a sample X, . . . , X of independent points with a common but arbitrary density f in Ra. These points form the vertices of a graph. Two points (X, Xj) are joined by an edge when a certain set S(X, X) does not contain any other data points. The definition of S is not affected by the other points. The number of edges in the graph is N. In this paper we seek relationships between E(N) and S, n and f. To save space, we will call all graphs created in this manner proximity graphs, even though this term could be misleading in some cases.

## Example 1

Direct dominance pairs. When S(X, Xj) is the rectangle with X and X, as vertices, X and X, are said to define a direct dominance pair. The problem of determining whether a pair is a dominance pair has applications in rectangle enclosure problems [1, 2]. Algorithms for reporting all direct dominance pairs are given in Gutting et al. [3]. Klein [4] has shown that the expected number of dir dns   da     s dat     n do n logd − 1n/(d − 1)!

#### Example 2

Gabriel graph. The Gabriel graph [5] is obtained when S is the sphere centered at (X, + Xj), with X, and X, at opposite poles. It has been used extensively in geographic variation analyses in biology (for a list of references, see Matula and Sokal [6]). Algorithms for finding the Gabriel graph in R2 are discussed in Matula and Sokal [6]. It is also shown there that for the uniform distribution in square, E(N) ~ 2n. We will see that for all densities, lim inf E(N)/n ≥ 2a-1 and that for most densities, E(N) ~ 2a − 1n. ■

#### Example 3

The relative neighborhood graph. The RNG, or relative neighborhood graph, is obtained by joining all pairs whose loon is empty, where the loon defined by a pair is the intersection of two spheres of equal radius, each having one point as center and the other point on its surface [7, 8]. It is a subgraph of the Gabriel graph. Supowit [9] has obtained an O(n log(n)) algorithm for finding the RNG in two dimensions. We will see that for all densities, E(N)/n ≥ Cd + o(1), where Ca is a constant depending upon d only (C2 is about 1.27). ■


<!-- p:2 -->


#### Example 4

The Delaunay triangulation. In the Delaunay triangulation, two points are joined by an edge if they are Delaunay triangulation neighbors, i.e. when some sphere with the two points on its surface and center somewhere on the hyperplane that forms the locus of all points at equal distance from both points is empty, i.e. contains no other points. Delaunay triangulations are ubiquitous in computational geometry [10], yet it is still unclear how E(N) is related to f. We know of course that N ≤ 3n — 6. Unfortunately, the Delaunay triangulation is not a special case of the kinds of graphs studied here, because the definition of S involves more than two points. However, since the Gabriel graph is a subgraph of the Delaunay triangulation, it is easy to see that the lower bounds derived for the Gabriel graph are applicable to the Delaunay triangulation as well. In particular, E(N)/n ≥ (2a− 1 + °(1)).

For a general discussion of proximity graphs and their applications, we refer to the survey papers by Toussaint [7, 8, 11]. For example, in Toussaint [7, 8], it is shown that the minimal spanning tree is a subgraph of the RNG, which is a subgraph of the Gabriel graph, which in turn is a subgraph of the Delaunay triangulation.

#### Example 5

Infinite strip graph. As an example of a more exotic graph, consider the graph formed when S(X,, Xj) is the infinite strip defined by two parallel hyperplanes through X, and X, that are perpendicular to X,— X,. This graph contains all dominance pairs as a subgraph, and cannot th   s o    s   a   se osed upon a decision that is not "local", it cannot truly be called a proximity graph. For the same reason, the expected time analysis requires a different collection of tools. Its properties will be studied elsewhere.

#### Example 6

Nearest neighbor graph. Consider the graph obtained by connecting each point with its nearest neighbor. The nearest neighbor graph is a subgraph of the Euclidean minimum spanning tree, and plays a role in closest point problems [10, pp. 180–181]. It is obvious that we have between n/2 and n edges in such a graph. We will prove that for all densities, E(N)/n →0.689 ... .

#### Example 7

The sphere of influence graph. For each X, in the plane, let C, be the circle centered at X, with the nearest neighbor of X, on its surface. If C, and C, have a nonempty intersection, X, and X, are connected. The corresponding graph is known as the sphere on influence graph. Avis and Horton [12] have studied the sphere of influence graph, and have shown that it has at most 29 n edges. They also report that El-Gindy has pointed out that it can be found in O(n log(n)) time by an algorithm of Bentley and Ottmann [13]. Unfortunately, there seems to be no inclusion property between any of the graphs discussed so far and the sphere of influence graph, which can often have several connected components. Also, the result of this paper do not apply directly to these graphs.

## 2. A USEFUL INEQUALITY

Most of the results in this paper are simple corollaries of an inequality provided in Theorem 1. That is why we forge directly ahead into a rather technical section. Some restrictions have to be put on S.

#### Definition of a regular set

In the halfplane {(u, v):u ∈ R, v ≥ 0}, we consider a fixed bounded set T (T stands for "target set"). T is symmetric about u = 1/2. A regular set S is any set for which membership can be determined based upon some T, according to the procedure explained below. To determine whether z ∈ S(x, y), we rotate and translate the space rigidly so that x coincides with the origin, and y coincides with (∥ x — y ∥, 0, 0, 0, . . . , 0). Then we shrink the space by a factor  x — y ∥ (shrinking by λ means that w gets mapped to λw). Finally, we rotate around the first axis such that the transformed z ends up in the positive halfplane (i.e. its second coordinate is nonnegative, and all coordinates from the third up are zero). The new location of z after these three operations should fall in T. Note that because of the symmetry in T, z ∈ S(x, y) if, and only if, z ∈ S(y, x).


<!-- p:3 -->


It is easy to see that if z ∈ S(x, y) for some regular set S, than all the points at the same distance of the line xy, and with the same projection on that line are also in S(x, y); in other words, we have rotational symmetry about xy. Examples include the loon defining the RNG, and the sphere defining the Gabriel graph.

The Gabriel graph, the RNG and the nearest neighbor graph are based on regular sets. The analysis of the direct dominance graph will be carried out elsewhere. The thrust of Theorem 1 is that the expected number of edges in a proximity graph based upon a regular set is virtually independent of f; the only factor truly influencing this expected number if the volume of S(x, y) when ∥ x — y  = 1. It is curious that all such S's with the same volume, regardless of their shape, give rise to the same expected number of edges, asymptotically speaking.

#### Theorem 1

Let N be the number of edges in a graph defined on the basis of a regular set S defined on the basis of a target set T. Then, for any density f,

$$\liminf _ { n \to \infty } \frac { E ( N ) } { n } \geqslant \frac { V _ { d } } { 2 \lambda ( T ) } ,$$

where Va is the volume of the unit sphere in Ra, and λ(T) is the d-dimensional volume of the d-dimensional set obtained by rotating T about the first axis [equivalently, it is the volume of S(x, y) when∥x − y∥ = 1].

Furthermore, for almost all x,

$$\lim _ { \eta \to \infty } E ( N ( X _ { 1 } ) | X _ { 1 } = x ) = \frac { V _ { d } } { \lambda ( T ) } ,$$

where N(X1) is the number of neighbors of X.

#### Proof of Theorem 1

We let N(X) be the number of neighbors of X, and observe that

$$N = \frac { 1 } { 2 } \sum _ { i = 1 } ^ { n } N ( X _ { i } ) .$$

Assume that for almost all x, (with respect to f),

$$\liminf _ { n \to \infty } E ( N ( x _ { 1 } ) ) \geqslant \frac { V _ { d } } { \lambda ( T ) } ,$$

where N(x) refers to the sample X2,. .. , X. Then, applying Fatou's lemma,

$$\liminf _ { n \to \infty } \frac { E ( N ) } { n } = \liminf _ { n \to \infty } \left \{ \frac { E ( N ( x _ { 1 } ) ) f ( x _ { 1 } ) } { 2 n } \, d x _ { 1 }$$

$$\liminf _ { n \to \infty } \frac { E ( N ) } { n } & = \liminf _ { n \to \infty } \int \frac { E ( N ( x _ { 1 } ) ) f ( x _ { 1 } ) } { 2 n } \, d x _ { 1 } \\ & \geq \int \liminf _ { n \to \infty } \frac { E ( N ( x _ { 1 } ) ) f ( x _ { 1 } ) } { 2 } \, d x _ { 1 } \\ & = \frac { V _ { d } } { 2 \lambda ( T ) } .$$

Thus, we need only show the pointwise result. We will use the symbol μ(·) to denote the probability measure of a set, i.e. the integral of f over the set in question. Also, λ(·) denotes Lebesgue measure, the € is an arbitrary small positive number.


<!-- p:4 -->


We observe that

$$E ( N ( x _ { 1 } ) ) = ( n - 1 ) \int ( 1 - \mu ( S ( x _ { 1 } , x _ { 2 } ) ) ) ^ { n - 2 } f ( x _ { 2 } ) \, d x _ { 2 }$$

$$\geqslant ( n - 1 ) \int _ { 1 . x _ { 2 } - x _ { 1 } | \leqslant \delta } ( 1 - ( 1 + \epsilon ) f ( x _ { 1 } ) \lambda ( S ( x _ { 1 } , x _ { 2 } ) ) ) ^ { n - 2 } f ( x _ { 2 } ) \, d x _ { 2 } ,$$

$$\left | \frac { \mu ( S ( x _ { 1 } , x _ { 2 } ) ) } { \lambda ( S ( x _ { 1 } , x _ { 2 } ) ) } - f ( x _ { 1 } ) \right | \leqslant \epsilon f ( x _ { 1 } )$$

$$\left | \frac { \mu ( B ( x _ { 1 } , x _ { 2 } ) ) } { \lambda ( B ( x _ { 1 } , x _ { 2 } ) ) } - f ( x _ { 1 } ) \right | \leqslant \epsilon f ( x _ { 1 } ) ,$$

for all x2 — x1  &lt; δ, where B(x1, x2) is the ball of radius ∥x2 — x1  centered at x1 . The fact that this can be done is a consequence of the fixed structure of S (S can only be translated, rotated and shrunk uniformly in all directions), the boundedness of S, and the Lebesgue density theorem [14, pp. 108–109]. It should be noted that δ depends upon x. A point x, with f (x1) &gt; 0 and δ &gt; 0 for every € &gt;0 will be called a Lebesgue point. The Lebesgue density theorem states that almost all points (with respect to f) are Lebesgue points. We assume that x, is a Lebesgue point.

Next, we introduce the nonincreasing funtion

$$\Psi ( r ) \triangle q ( 1 - ( 1 + \epsilon ) \lambda ( T ) f ( x _ { 1 } ) r ^ { \phi } ) ^ { n - 2 } \, I _ { r \lesssim \delta } ,$$

where r &gt; 0. We note that the volume of S(x, y) is λ(T) times  x — y ∥ d. Thus, the lower bound for E(N(x1)) is

$$r & > 0 . \text { We note that the volume of } S ( x , y ) \text { is } \lambda ( T ) \text { times } \| x - y \| ^ { - } . \text { Thus, the lower bound } E ( x _ { 1 } ) \text { is } \\ E ( N ( x _ { 1 } ) ) & \text { is } \\ & ( n - 1 ) \int _ { 1 ^ { x _ { 2 } - x _ { 1 } | | \delta } } ( 1 - ( 1 + \epsilon ) f ( x _ { 1 } ) \lambda ( T ) \| x _ { 1 } - x _ { 2 } \| ^ { d } ) ^ { n - 2 } f ( x _ { 2 } ) \, d x _ { 2 } \\ & = ( n - 1 ) E ( \Psi ( \| X _ { 2 } - x _ { 1 } \| ) ) \\ & = ( n - 1 ) \int _ { 0 } ^ { 1 } P ( \Psi ( \| X _ { 2 } - x _ { 1 } \| ) > t ) \, d t \\ & = ( n - 1 ) \int _ { 0 } ^ { 1 } P ( \Psi ( \| X _ { 2 } - x _ { 1 } \| ) > t ) \\ & = ( n - 1 ) \int _ { 0 } ^ { 1 } \left ( \int _ { x _ { 2 } ; \mathbb { P } ^ { ( 1 | x _ { 2 } - x _ { 1 } | | \ell ) } } f ( x _ { 2 } ) \, d x _ { 2 } \right ) d t \\ & = ( n - 1 ) \int _ { 0 } ^ { 1 } \left ( \int _ { x _ { 2 } ; \mathbb { P } ^ { ( 1 | x _ { 2 } - x _ { 1 } | | \ell ) } } f ( x _ { 2 } ) \, d x _ { 2 } \right ) d t \\ & \geq ( n - 1 ) \int _ { r \colon 0 < r < 1 ; \Psi ^ { - 1 } ( x ) \delta } ( 1 - \epsilon ) V _ { d } ( \Psi ^ { - 1 } ( t ) ) ^ { d } f ( x _ { 1 } ) \, d t \\ \intertext { w e c o n s a g a i n p l a g e d s u n t i o n } \text {the one used in the definition of } \Psi \text { . We note that }$$

where we once again applied the Lebesgue density theorem; the δ &gt; 0 introduced here is the same as the one used in the definition of Ψ. We note that

$$( \Psi ^ { - 1 } ( t ) ) ^ { d } \, \Rightarrow \, \frac { 1 - t ^ { 1 / ( n - 2 ) } } { ( 1 + \epsilon ) \lambda ( T ) f ( x _ { 1 } ) } ,$$

when t ≥(1 - (1 + €)λ(T)f (x1)δd)-2. Resubstitution of this in the last expression gives us yet another lower bound (because we integrate over fewer t's):

$$( n - 1 ) \int _ { t \colon > t \gtrsim \xi } ( 1 - \epsilon ) V _ { d } f ( x _ { 1 } ) \frac { 1 - t ^ { 1 / ( \tilde { n } - 2 ) } } { ( 1 + \epsilon ) \lambda ( T ) f ( x _ { 1 } ) } d t$$

where δ &gt; 0 is so small that

and


<!-- p:5 -->


$$Geometrical graphs \\ ( \text {where $\xi\triangleleft(1-\left(1+ \epsilon\right)\lambda(T)\ f(x_{1})\delta^{n-2})$} ) \\ = ( n - 1 ) \frac { 1 - \epsilon } { 1 + \epsilon } \frac { V _ { a } } { \lambda ( T ) } \int _ { t \colon 1 > \gamma \xi } ( 1 - t ^ { 1 / ( n - 2 ) } ) \, d t \\ \\ \geq ( n - 1 ) \frac { 1 - \epsilon } { 1 + \epsilon } \frac { V _ { d } } { \lambda ( T ) } \left ( \frac { 1 } { n - 1 } - \xi \right ) \\ = ( 1 + o ( 1 ) ) \frac { 1 - \epsilon } { 1 + \epsilon } \frac { V _ { a } } { \lambda ( T ) } , \\ \text {calling that $\epsilon$ was arbitrary, this conccludes the proof of the lower}$$

because ξ↓0. Recalling that € was arbitrary, this concludes the proof of the lower bound for E(N), and for the lower bound for E(N(x)) at all Lebesgue points x.

What follows is simply an upper bound for E(N(x)) at Lebesgue points x. We observe that

$$E ( N ( x _ { 1 } ) ) & \leqslant ( n - 1 ) \int \exp [ - \left ( n - 2 \right ) \mu ( S ( x _ { 1 } , x _ { 2 } ) ) ] f ( x _ { 2 } ) \, d x _ { 2 } \\ & \leqslant ( n - 1 ) \int _ { | x _ { 2 } - x _ { 1 } | \leqslant \delta } \exp [ - \left ( n - 2 \right ) \mu ( S ( x _ { 1 } , x _ { 2 } ) ) ] f ( x _ { 2 } ) \, d x _ { 2 } \\ & + ( n - 1 ) \int _ { | x _ { 2 } - x _ { 1 } | > \delta } \exp [ - \left ( n - 2 \right ) \mu ( S ( x _ { 1 } , x _ { 2 } ) ) ] f ( x _ { 2 } ) \, d x _ { 2 } , \\ \intertext { s l e f } \beta \, > 0 \, \text { is as defined above. Thus}$$

where δ &gt; 0 is as defined above. Thus,

$$\text {where } & \ > 0 \text { is as defined above.} \ \text {Thus} , \\ & E ( N ( x _ { 1 } ) ) \leq ( n - 1 ) \int _ { | x _ { 2 } - x _ { 1 } | \leq \delta } \exp [ - ( n - 2 ) \lambda ( T ) f ( x _ { 1 } ) ( 1 - \epsilon ) \| x _ { 2 } - x _ { 1 } \| ^ { \dagger } ] f ( x _ { 2 } ) \, d x _ { 2 } \\ & \quad + ( n - 1 ) \int _ { | x _ { 2 } - x _ { 1 } | > \delta } \exp [ - ( n - 2 ) \lambda ( T ) f ( x _ { 1 } ) ( 1 - \epsilon ) \| x _ { 2 } - x _ { 1 } \| ^ { \dagger } ] f ( x _ { 2 } ) \, d x _ { 2 } \\ & \leqslant n \int _ { | x _ { 2 } - x _ { 1 } | \leq \delta } \exp [ - ( n - 2 ) \lambda ( T ) f ( x _ { 1 } ) ( 1 - \epsilon ) \| x _ { 2 } - x _ { 1 } \| ^ { \dagger } ] f ( x _ { 2 } ) \, d x _ { 2 } \\ & \quad + n \exp [ - ( n - 2 ) \lambda ( T ) f ( x _ { 1 } ) ( 1 - \epsilon ) \delta ^ { \delta } ] . \\ \text {The second term in the upper bound is o(1). The first term is handled as in the lower bound. It}$$

The second term in the upper bound is o(1). The first term is handled as in the lower bound. It can be written as

$$n \, E ( \Psi ( \| X _ { 2 } - x _ { 1 } \| ) ) \\ ( \text {where} \Psi ( r ) \triangle I _ { r , s \delta } \exp [ - \left ( n - 2 \right ) \lambda ( T ) f ( x _ { 1 } ) ( 1 - \epsilon ) r ^ { d } ] ) \\ = n \int _ { 0 } ^ { 1 } P ( \Psi ( \| X _ { 2 } - x _ { 1 } \| ) > t ) \, d t \\ = n \int _ { 0 } ^ { 1 } \int _ { x _ { 2 } \cdot \mathbb { P } ( | x _ { 2 } - x _ { 1 } | ) > t } f ( x _ { 2 } ) \, d x _ { 2 } \, d t$$

$$\int _ { 0 } ^ { 0 } \int _ { x _ { 2 } \colon \mathcal { P } ( | x _ { 2 } - x _ { 1 } | | ) > t } ^ { 0 }$$


<!-- p:6 -->


$$= n \int _ { 0 } ^ { 1 } \int _ { x _ { 2 } \colon i x _ { 2 } - x _ { 1 } \, \| \, \varsigma \, \varphi ^ { - 1 } ( t ) } f ( x _ { 2 } ) \, d x _ { 2 } \, d t$$

$$& \int _ { 0 } \int _ { x _ { 2 } \colon | x _ { 2 } - x _ { 1 } | ^ { 2 } \subset \varphi ^ { - 1 } ( n ) } \int _ { 0 } \int _ { x _ { 2 } \colon | x _ { 2 } - x _ { 1 } | ^ { 2 } \subset \varphi ^ { - 1 } ( n ) } \\ \leqslant & n \int _ { \mathbb { m } { P } ^ { - 1 } ( t ) > \delta } d t \ + n \int _ { \mathbb { m } { T } ^ { 0 } < t < 1 ; \, \gamma - 1 ( n ) < \delta } \int _ { x _ { 2 } \colon | x _ { 2 } - x _ { 1 } | ^ { 2 } \subset \varphi ^ { - 1 } ( t ) } ( 1 + \epsilon ) f ( x _ { 1 } ) \, d x \\ = & n \, \Psi ( \delta ) + n \int _ { t \colon \mathbb { m } { P } ( \delta ) \leqslant t < 1 } ( 1 + \epsilon ) \, f ( x _ { 1 } ) \, V _ { d } [ \Psi ^ { - 1 } ( t ) ] ^ { 4 } \, d t \\ = & o ( 1 ) + n \int _ { \Psi ( \delta ) } \log \left ( \frac { 1 } { t } \right ) \, d t \, \frac { 1 + \epsilon } { 1 - \epsilon } \frac { V _ { d } } { ( n - 2 ) \lambda ( T ) } \\ = & o ( 1 ) + n \left [ 1 - \Psi ( \delta ) + \Psi ( \delta ) \log ( \Psi ( \delta ) ) \right ] \frac { 1 + \epsilon } { 1 - \epsilon } \frac { V _ { d } } { ( n - 2 ) \lambda ( T ) } \\ = & o ( 1 ) + ( 1 + o ( 1 ) ) \frac { 1 + \epsilon } { 1 - \epsilon } \frac { V _ { d } } { \lambda ( T ) } , \\ \text {since } n \, \Psi ( \delta ) \to 0 . \text { This concludes the proof of Theorem 1.}$$

$$& = n \int _ { 0 } ^ { 1 } \int _ { x _ { 2 } \colon | x _ { 2 } - x _ { 1 } | \leq \xi ^ { - 1 } ( n ) } f ( x _ { 2 } ) \, d x _ { 2 } \, d t \\ & \leqslant n \int _ { \cdot \cdot \cdot } \int _ { - ( n ) > \delta } d t \, + n \int _ { \cdot \cdot \cdot < t < \cdot \, 1 ; \, \Psi ^ { - 1 } ( n ) \leq \delta } \int _ { x _ { 2 } \colon | x _ { 2 } - x _ { 1 } | \leq \xi ^ { - 1 } ( n ) } ( 1 + \epsilon ) f ( x _ { 1 } ) \, d x _ { 2 } \, d t \\$$

$$) \overbrace { 1 - \epsilon } ^ { ( ) } \overline { \lambda ( T ) } ,$$

since n Ψ(δ) →0. This concludes the proof of Theorem 1.

## 3. DISCUSSION OF THEOREM 1

It is noteworthy that the lower bound depends upon the volume induced by T only. It is applicable to all densities f.

Perhaps equally interesting is the fact that for almost all x, conditional on X, = x, the expected number of neighbors of X, is Va/λ(T) + o(1). This is due to the fact that locally, every density, no matter how pathological, is "almost" uniform in a small neighborhood of almost all points. Hence, since the decision to include an edge or not is virtually always based upon the points in a small neighborhood of the candidate vertices, the expected degree of each vertex is roughly as for the uniform density.

One should not conclude from Theorem 1 that all the properties of N or N(X) are distribution-free. Indeed, the rate of convergence of the various quantities in Theorem 1 to their asymptotic values depends very much on f. Thus, it is certainly not possible to argue as follows:

$$\lim _ { n \to \infty } \sup \frac { E ( N ) } { n } \leq \int \frac { 1 } { 2 } \lim _ { n \to \infty } \sup E ( ( N ( X _ { 1 } ) | X _ { 1 } = x ) f ( x ) \, d x = \frac { V _ { d } } { 2 \lambda ( T ) } ,$$

by Theorem 1. One can bring the limit supremum under the integral only under certain conditions. One such condition is that the integrand, a function of n and x here, can be uniformly bounded from above in n by an integrable function. The lower bound of Theorem 1 can be attained however for some distributions, as we will see below.

It is known that planar graphs cannot have more than 3n -6 edges. Thus, results like Theorem 1 can be used to prove possible nonplanarity of certain graphs; indeed, if E(N) ≥(α + o(1))n for some α &gt; 3 and all densities, it is easy to see that the proximity graph defined by that particular S must have some configuration for which it cannot possibly be planar.

## 4. THE GABRIEL GRAPH

For the Gabriel graph, λ(T) = Vd/2d. Thus, we conclude that

$$\liminf _ { n \to \infty } \frac { E ( N ) } { n } \geqslant 2 ^ { d - 1 } ,$$

for all f. In addition, at almost all x, E(N(X,)|X, = x) tends to 2a. This generalizes some results of Matula and Sokal [6]. They have shown that the Gabriel graph in the plane is planar and has at most 3n - 8 edges. They also showed that the expected number of edges is asymptotic to 2n for the uniform distribution on the unit square. We will see in Theorem 3 that the latter result remains valid for nearly all densities of interest to users.


<!-- p:7 -->


## 5. THE RELATIVE NEIGHBORHOOD GRAPH

Since the loon defining the RNG contains the set S defining the Gabriel graph, it is clear that the RNG is contained in the Gabriel graph. To obtain exact information on how E(N) varies with n, we need to compute the area of the unit loon generated by T with some care. We have, for d = 2,

$$= \frac { 2 } { \pi } \left ( \frac { \pi } { 3 } - \frac { 3 ^ { 1 / 2 } } { 4 } \right )$$

$$= \frac { 2 } { 3 } - \frac { 3 ^ { 1 / 2 } } { 2 \pi } = 0 . 3 9 1 0 0 2 2 1 9 0 \dots$$

$$\frac { \lambda ( T ) } { V _ { 2 } } = \frac { 2 } { \pi } \left ( \frac { \pi } { 3 } - \frac { 3 ^ { 1 / 2 } } { 4 } \right ) \\ = \frac { 2 } { 3 } - \frac { 3 ^ { 1 / 2 } } { 2 \pi } = \\ d g r e e \, a t \, a l m o s t \, a l l$$

Therefore, the expected degree at almost all x is 2.557530243 ·. · + o(1). Also, the expected number of edges is at least n(1.2787651215 ··· + o(1)) for any density.

$$\lambda ( T ) = \int _ { 0 } ^ { 3 ^ { 1 / 2 } / 2 } 2 ( ( 1 - r ^ { 2 } ) ^ { 1 / 2 } - \frac { 1 } { 2 } ) \, d ( V _ { d } r ^ { d } ) ,$$

$$\frac { V _ { d } } { \lambda ( T ) } = \frac { 1 } { \int _ { 0 } ^ { 3 ^ { 1 / 2 } / 2 } 2 ( ( 1 - r ^ { 2 } ) ^ { 1 / 2 } - \frac { 1 } { 2 } ) \, d r ^ { d - 1 } \, d r } \\$$

for the asymptotic degree at almost all x.

## 6. THE NEAREST NEIGHBOR GRAPH

Let S(x, y) be the union of the spheres of radius x — y | centered at x and y, respectively. If S(x, y) contains no data points, then x and y are each other's nearest neighbors, hence they o t e s   t  e t ot r  e     t minus the area of the loon of the RNG, i.e.

$$\frac { \lambda ( T ) } { V _ { 2 } } = \frac { 4 } { 3 } + \frac { 3 ^ { 1 / 2 } } { 2 \pi } = 1 . 6 0 8 9 9 7 7 8 0 9 \dots \, .$$

Thus, if E(N) is the expected number of double edges,

$$\liminf _ { n \to \infty } \frac { E ( N ) } { n } \geqslant \frac { 1 } { \frac { 8 } { 3 } + \frac { 3 ^ { 1 / 2 } } { \pi } } \, .$$

Since the number of edges in the nearest neighbor graph is n minus the number of double edges, we have, for all densities f,

$$\text {we have, for all densities} \, f , \\ \lim _ { n \to \infty } \frac { E \left ( n u m b o r \, e d g e s \, i n e r s e n t \, n e r b o r \, g r a p h \right ) } { n } & \leqslant \frac { \frac { 5 } { 3 } + \frac { 3 ^ { \prime } 2 } { \pi } } { 8 } \\ & = \frac { 5 \pi + 2 7 ^ { \prime 2 } } { 8 \pi + 2 7 ^ { \prime 2 } } \\ & = 0 . 6 8 9 2 4 7 5 5 1 6 \dots .$$

For d &gt; 2, we have

which yields the formula We will see below (Theorem 2) that for all densities, the expected number of edges in the nearest neighbor graph is (c + o(1))n, where c = 0.6892475516 .. . is the constant defined above.


<!-- p:8 -->


For uniform distributions in the plane (more precisely, homogeneous Poisson processes in the plane), many statistical properties of nearest neighbor graphs are well-known; for a tour of these results, one can consult Getis and Boots [15], where references to applications in geography and biology are given. For example, it is known that the probability that X, will form a reciprocal nearest neighbor pair with its nearest neighbor (i.e. X, is the nearest neighbor of its nearest neighbor) is asymptotic to

$$c \triangle q \frac { 6 \pi } { 8 \pi + 2 7 ^ { 1 / 2 } } = 0 . 6 2 1 5 \dots ,$$

see Refs [16–18]. This implies that the expected number of edges in the nearest neighbor graph is asymptotic to.

$$\left ( \frac { c } { 2 } + ( 1 - c ) \right ) n ,$$

where the first contribution comes from the double edges, and the second term from the single edges. We verify easily that

$$\frac { c } { 2 } + ( 1 - c ) = \frac { 5 \pi + 2 7 ^ { 1 / 2 } } { 8 \pi + 2 7 ^ { 1 / 2 } } .$$

This corresponds to what we found to be true for all densities.

## 7. DIRECTIONAL NEAREST NEIGHBOR GRAPHS

Flinchbaugh and Jones [19] studied the directional nearest neighbor graph in R2, obtained by connecting each point with its nearest neighbor in one of r fixed divisions. The divisions are obtained by positioning the origin at a point, and partitioning the space into infinite slices of a pie, each with angle 2π/r. The number of edges grows at most linearly in n, so that Theorem 3 below applies, but unfortunately, a crucial symmetry condition on S used by us is violated.

Nevertheless, we can get some idea of the expected number of edges in similar graphs obtained as follows: join X, and X, if in the cone of angle α centered at X, with X, on its bisector, X, is the nearest point to X.

Here too, we proceed first by computing the expected number of double edges. We note in passing that for α = 2π /3, every double edge corresponds to a RNG edge. For α ≤ 2π /3, the double edges define a supergraph of the RNG. A simple computation shows that in Theorems 1 and 3, which are both applicable here,

$$\lambda ( T ) = 2 \, \frac { \alpha } { 2 } - \frac { 1 } { 2 } \tan \left ( \frac { \alpha } { 2 } \right ) .$$

Hence, for all densities of Theorem 3, and 0 &lt; α ≤ 2π/3,

$$E ( N ) / n \rightarrow \frac { \pi } { 2 \alpha + \tan \left ( \frac { \alpha } { 2 } \right ) } \, . \\ \colon \, _ { 1 } \, \omega ^ { 1 } \colon \, _ { 2 } \, \omega ^ { 2 } \colon \, _ { 1 } \, \omega \, ( \frac { \alpha } { 2 } )$$

For the RNG (α = 2π /3), we obtain the limit value 1/(4/3 – 31/2/π) = 1.2787651215 . . . . Let us now consider a graph in which we associate with each edge one or two directions; an edge with two directions is said to be a double edge; and X, points to X, whenever X, is the nearest neighbor of X. Above, we have already counted the expected number of double edges. The total expected number of directions attached to edges is easily seen to be asymptotic to n × V2/λ(T), where T now stands for the cone of angle α, intersected with the unit circle. Thus, the expected number of directions is asymptotic to 2 n π/α. The expected number of edges is obtained by subtracting from this the expected number of double edges. This yields the result (valid for 0 &lt; α ≤ 2π/3)

$$\frac { E ( N ) } { n } \rightarrow \frac { 2 \pi } { \alpha } \left ( 1 - \frac { 1 } { 2 } \frac { 1 } { \left ( \frac { \alpha } { 2 } \right ) } \right ) ,$$


<!-- p:9 -->


which is valid for all densities of Theorem 3. It is interesting to observe that this limit varies as 8π/(5α) and α ↓0, so that by controlling α, we have in fact full control on the sparseness of the graph. For small α, these graphs cannot possibly be planar.

## 8. ASYMPTOTICS FOR GRAPHS WITH BOUNDED MAXIMAL DEGREE

We have hinted at the fact that the lower bound on E(N) given in Theorem 1 can be attained for some densities.

In some proximity graphs, the maximal degree of each vertex is bounded by a number depending upon d only; for example, for any value of d, is is known that the nearest neighbor graph has maximal vertex degree bounded by a constant C depending upon d only. For all such graphs, we have a very general property, valid for all densities (Theorem 2): the lower bound of Theorem 1 is attained for all densities.

In the next section, we will consider proximity graphs that are worst-case sparse, i.e. for any x1, . . . , x, the number of edges does not exceed Cn for some constant C. It suffices to note that this condition is satisfied for all planar graphs: hence, for d = 2, it holds for most of the graphs discussed above, including the RNG, the graph formed by double edges in the nearest neighbor graph, and the Gabriel graph. For worst-case sparse graphs, possibly having unbounded maximal vertex degree, the lower bound of Theorem 1 is attained under some (mild) conditions on the underlying distribution (Theorem 3).

Theorem 2

Consider a proximity graph based on a regular set S, and assume that the maximal vertex degree is bounded by a constant C depending upon d only. Then, for all densities,

$$\lim _ { n \to \infty } \frac { E ( N ) } { n } = \frac { V _ { d } } { 2 \lambda ( T ) } .$$

Proof of Theorem 2

For every €, δ &gt; 0, we can partition Ra into a set G,δ, and its complement, B,. The "G" stands for "good" and the "B" stands for "bad". G,s is the collection of all x for which

and

$$\text {ends for "bad" .} \, G _ { c , \delta } \text { is the collection of } \\ \left | \frac { \mu ( S ( x , y ) ) } { \lambda ( S ( x , y ) ) } - f ( x ) \right | \leqslant \epsilon f ( x ) \\ \\ \left | \frac { \mu ( B ( x , y ) ) } { \lambda ( B ( x , y ) ) } - f ( x ) \right | \leqslant \epsilon f ( x ) , \\ \text {where } B ( x , y ) \text { is the ball centered at } x$$

for all y with ∥x — y  &lt; δ, where B(x, y) is the ball centered at x with radius x — y ∥, and x ∥ ≤ 1/δ. By the Lebesgue density theorem, it is possible to find δ &lt; 0 depending upon €, such that μ(B,δ) &lt; €. We pick δ in this manner, and write G, and B, from here onwards.

What follows is simply an upper bound for E(NG).

The data points are partitioned into two sets, according to membership in G, or its complement. The number of edges N can be written as NG + Ns, where NG refers to the edges in which both vertices are in G. NB refers to the other edges. The expected number of Ns is bounded by CE(cardinality of B) (because every vertex has degree C in the worst case). This is Cnμ(B) ≤ Cn€. When divided by n, this is as small as desired by our choice of €.

We observe that

$$E ( N _ { G } ) ( n / 2 ) & \leqslant ( n - 1 ) \iint _ { x _ { 1 } , x _ { 2 } \in G _ { 1 } } \exp [ - \left ( n - 2 \right ) \mu ( S ( x _ { 1 } , x _ { 2 } ) ) ] f ( x _ { 1 } ) f ( x _ { 2 } ) \, d x _ { 2 } d x _ { 1 } \\ & \leqslant ( n - 1 ) \iint _ { x _ { 1 } , x _ { 2 } \in G _ { 1 } | x _ { 2 } - x _ { 1 } | \leqslant \delta } \exp [ - \left ( n - 2 \right ) \mu ( S ( x _ { 1 } , x _ { 2 } ) ) ] f ( x _ { 1 } ) f ( x _ { 2 } ) \, d x _ { 2 } d x _ { 1 }$$

$$\leqslant ( n - 1 ) \sum _ { x _ { 1 } , x _ { 2 } \in G _ { c } \colon | x _ { 2 } - x _ { 1 } | \ll \delta } \exp [ - ( n - 2 ) \mu ( S ( x _ { 1 } , x _ { 2 } ) ) ] f ( x _ { 1 } ) f ( x _ { 2 } ) \, d x _ { 2 } \, d x _ { 1 }$$


<!-- p:10 -->


$$\iint _ { \widehat { T } _ { i } , x _ { 2 } = 1 }$$

$$L \ D v e r \colon & & L \ D v e r \\ & + ( n - 1 ) \, \iint _ { x _ { 1 } , x _ { 2 } \in G , ( 1 , x _ { 2 } - x _ { 1 } | | ) \, \delta } \exp [ - ( n - 2 ) \mu ( S ( x _ { 1 } , x _ { 2 } ) ) ] f ( x _ { 1 } ) f ( x _ { 2 } ) \, d x _ { 2 } d x _ { 1 } . \\ & \leq ( n - 1 ) \, \iint _ { x _ { 1 } , x _ { 2 } \in G , ( 1 , x _ { 2 } - x _ { 1 } | | \, \delta } \exp [ - ( n - 2 ) \lambda ( T ) f ( x _ { 1 } ) ( 1 - \epsilon ) | | x _ { 2 } - x _ { 1 } | | ^ { 2 } ] f ( x _ { 1 } ) f ( x _ { 2 } ) d x _ { 2 } d x _ { 1 } \\ & + ( n - 1 ) \, \iint _ { x _ { 1 } , \epsilon , | x _ { 2 } - x _ { 1 } | | \, \delta } \exp [ - ( n - 2 ) \lambda ( T ) f ( x _ { 1 } ) ( 1 - \epsilon ) \delta ^ { \delta } ] f ( x _ { 1 } ) f ( x _ { 2 } ) d x _ { 2 } d x _ { 1 } \\ & \leq n \, \iint _ { x _ { 1 } , x _ { 2 } \in G , | x _ { 2 } - x _ { 1 } | | \, \delta } \exp [ - ( n - 2 ) \lambda ( T ) f ( x _ { 1 } ) ( 1 - \epsilon ) | | x _ { 2 } - x _ { 1 } | | ^ { 2 } ] f ( x _ { 1 } ) f ( x _ { 2 } ) d x _ { 2 } d x _ { 1 } \\ & + n \int _ { x _ { 1 } , \epsilon \in G } \exp [ - ( n - 2 ) \lambda ( T ) f ( x _ { 1 } ) ( 1 - \epsilon ) \delta ^ { \delta } ] f ( x _ { 1 } ) \, d x _ { 1 } . \\ \text {The second term in the upper bound is of } & ( 1 ) \, . \, \text {using the fact that} \\ \text {ne-} ^ { \prime \prime } & < 1 / ( \i u ) \, \text {for all } n \geq 1 \, \text { and all } \i u \geq 0 , \, \text {it is easy to see that the integral is uniformly bounded} \\ \intertext { s u n g a b l e } & \quad \, \text {in the upper bound} \, \text {and} \, \text {the fact that} \, G \text { vanishes outside a big square} .$$

The second term in the upper bound is o(1). This can be seen as follows: using the fact that ne−a ≤ 1/(eu) for all n ≥ 1 and all u &gt; 0, it is easy to see that the integrand is uniformly bounded in n by an integrable function (here we also need the fact that G, vanishes outside a big square). Furthermore, the integrand tends to zero with n for almost all x, , so that we can apply the Lebesgue dominated convergence theorem. The first term is handled as in the proof of the lower bound (see Theorem 1): it can be written as

$$\text {e} ^ { - \kappa } & \leq 1 / ( \text {e} ) \text { for } n \geq 1 \text { and all } u > 0 , \text { it is easy to see that the integral and is uniformly bounded} \\ \intertext { u n g r a m e , t h e i n g r a n d t e s to zero with n \text { for almost all } x , \text { so that we can apply the Lebesgue } } \text {dominated convergence theorem. The first term is handled as in the proof of the lower bound (see
Theorem 1): it can be written as } \\ & \int _ { G _ { n } } \left ( n \int _ { x _ { 2 } \in G _ { n } \times _ { x _ { 2 } } \times _ { | | } } \exp [ - ( n - 2 ) \lambda ( T ) f ( x _ { 1 } ) ( 1 - \epsilon ) \| x _ { 2 } - x _ { 1 } \| ^ { 4 } f ( x _ { 2 } ) d x _ { 2 } \right ) f ( x _ { 1 } ) d x _ { 1 } \\ & \triangle q \int _ { G _ { n } } \left ( \int _ { G _ { n } } \left ( E ( \Psi ( \| x _ { 2 } - x _ { 1 } \| ) / _ { \mathcal { I } } ( x _ { 2 } ) ) \right ) f ( x _ { 1 } ) d x _ { 1 } , \\ \intertext { w h e r e , for fixed } A \triangle q \{ x _ { 2 } \cdot x _ { 2 } \in G _ { n } , \| x _ { 2 } - x _ { 1 } \| \leq \delta \} . \\ \text {However, for fixed } x _ { 1 } \in G _ { n } , \\ E ( \Psi ( \| x _ { 2 } - x _ { 1 } \| ) / _ { \mathcal { I } } ( x _ { 2 } ) ) = n \int _ { 0 } ^ { 1 } P ( X _ { 2 } \in A , \Psi ( \| x _ { 2 } - x _ { 1 } \| ) > t ) \, d t \\ & = n \int _ { 0 } ^ { 1 } \int _ { \Omega _ { 1 } ( X _ { 2 } ) > 1 , 2 \in \mathcal { I } } f ( x _ { 2 } ) \, d x _ { 2 } d t \\ & = n \int _ { 0 } ^ { 1 } \int _ { \Omega _ { 1 } ( X _ { 2 } ) > 1 , 2 \in \mathcal { I } } f ( x _ { 2 } ) \, d x _ { 2 } d t \\ & = n \int _ { 0 } ^ { 1 } \int _ { \Omega _ { 1 } ( X _ { 2 } ) > 1 , 2 \in \mathcal { I } } f ( x _ { 2 } ) \, d x _ { 2 } d t \\ & \leq n \int _ { \Omega _ { 1 } ( X _ { 2 } ) > 1 } d t + n \int _ { \Omega _ { 1 } ( X _ { 2 } ) < 1 , 1 \in \mathcal { I } } \int _ { \Omega _ { 1 } ( X _ { 2 } ) \colon 1 \in \mathcal { I } } ( 1 + \epsilon ) f ( x _ { 1 } ) \, d x _ { 2 } d t \\ & ( x _ { 1 } \in G _ { n } ) \\ & = n \Psi ( \delta ) + n \int _ { \Omega _ { 1 } ( X _ { 2 } ) < 1 } ( 1 + \epsilon ) f ( x _ { 1 } ) \, V _ { \mathcal { I } } ( \Psi ^ { - 1 } ( t ) ) ^ { \prime } d t \\ & = n \Psi ( \delta ) + \int _ { \Gamma _ { 0 } ( \delta ) } ^ { 1 } \log \left ( \frac { 1 } { t } \right ) d t \frac { 1 + \epsilon } { 1 - \epsilon } \frac { V _ { \mathcal { I } } } { ( n - 2 ) \lambda ( T ) } \\$$


<!-- p:11 -->


or

#### Proof of Theorem 3

Let €, δ, G, and B, be as in the proof of Theorem 2. The data points are partitioned into two sets, according to membership in G, or its complement. The number of edges N can be partitioned into three collections, NGG (connecting vertices entirely within G ), N (connecting vertices entirely in B), and NBG (connecting vertices from G with vertices in B).

If we consider the proximity graph formed on the basis of the points in B, alone, then the expected number of edges [and thus E(Ns)] is bounded by CE(cardinality of B) because the proximity graph is worst-case sparse. This is Cnμ(B) ≤ Cne. When divided by n, this is as small as desired by our choice of €.

$$\leqslant n \, \Psi ( \delta ) + n \frac { 1 + \epsilon } { 1 - \epsilon } \frac { V _ { d } } { ( n - 2 ) \lambda ( T ) } .$$

We have seen above that

$$\int _ { G _ { c } } n \, \Psi ( \delta ) f ( x _ { 1 } ) \, d x _ { 1 } \to 0 \\$$

as n → ∞; hence the first term in the upper bound has an o(1) contribution to E(N)/n [note that uos s   x    ← (     s  t    x d in the upper bound does not depend upon x, so that we can conclude, by the arbitrary nature of €, that lim sup E(N)/n ≤ Va/(2 λ(T)). This, combined with the lower bound of Theorem 1, concludes the proof of Theorem 2. ■

## 9. ASYMPTOTICS FOR SPARSE GRAPHS

We now introduce a regularity condition for a density f. For every €,δ &gt; 0, let B, be the collection of all x ∈ Rd for which

$$\inf _ { y \colon | y - x | \leq \delta \ \ z \colon \in S ( x , y ) \ \ o r \ \ | z - x | \leq \delta } f ( z ) < ( 1 - \epsilon ) f ( x )$$

$$\sup _ { y \colon | y - x | \in \{ \delta \ \ z \colon z \in S ( x , y ) \ \text { or } | z - x | \leqslant \delta } f ( z ) > ( 1 + \epsilon ) f ( x ) .$$

We demand that the boundary of B, have zero Lebesgue measure, where the boundary of a set is defined as the closure of a set minus the set itself. The boundary of a closed set is obviously empty. Examples of sufficient conditions follow.

#### Example 8

Uniform density on a convex set. When f is the uniform density on a convex set C, and € is small enough B,&amp; consists of all the points in C that are within distance δ of the complement of C, and all the points of the complement of C that are within distance δ of C. This in turn is the difference of two nested convex sets. Its boundary has zero Lebesgue measure. ■

#### Example 9

The multivariate normal density. For the multivariate normal density, the argument is rather simple. In fact, the regularity condition is satisfied for most unimodal radially symmetric densities. ■

#### Theorem 3

Consider a proximity graph based on a regular set S, and assume that it is worst-case sparse. Then, for all densities satisfying the regularity condition given above,

$$\lim _ { n \to \infty } \frac { E ( N ) } { n } = \frac { V _ { d } } { 2 \, \lambda ( T ) } .$$


<!-- p:12 -->


E(NGc) is handled exactly as in the proof of Theorem 2 [it is called E(NG) there]. Using the notation of the proof of Theorem 2, we can conclude that

$$\lim \sup \frac { E ( N _ { G G } ) } { n } \leqslant \frac { ( 1 + \epsilon ) V _ { d } } { 2 ( 1 - \epsilon ) \lambda ( T ) } .$$

The     s nanl  s   o      sin the manner we handled the upper bound for E(Ng) in the proof of Theorem 2, provided that we replace everywhere the event X2∈ G, or the statement x2∈ G, by the corresponding event and statement involving B. Furthermore, when breaking up the integral with respect to dt into two pieces, we consider a breakpoint defined by the condition {t : Ψ − '(t) &gt; ρ} for some ρ ∈ (0, δ). It can be verified that we have

$$\frac { E ( N _ { B G } ) } { n / 2 } & \leqslant \phi ( 1 ) + \frac { ( 1 + \epsilon ) V _ { d } } { 2 ( 1 - \epsilon ) \lambda ( T ) } \int _ { x _ { 1 } \in G _ { c } , \| x _ { 2 } - x _ { 1 } \| < \rho \text { for some } x _ { 2 } \in B } f ( x _ { 1 } ) \, d x _ { 1 } . \\$$

We are done if we can prove that the integral in the last upper bound can be made as small as desired by our choice of ρ, for every fixed € and δ. This is precisely where the regularity condition comes into play. Indeed, the function f is integrable, and as ρ ↓0, the set over which we integrate shrinks down to a set of zero Lebesgue measure (because the closure of B, intersected with G has zero Lebesgue measure). Therefore, by the Lebesgue dominated convergence theorem, the integral can be made as small as desired by the choice of ρ. This, together with Theorem 1, concludes the proof of Theorem 3.

Acknowledgement—Research by the author was sponsored by NSERC Grant A3456 and by FCAC Grant EQ-1678.
