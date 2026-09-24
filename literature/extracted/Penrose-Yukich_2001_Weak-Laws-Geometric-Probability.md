---
id: "Penrose-Yukich_2001_Weak-Laws-Geometric-Probability"
source_pdf: "../pdf/Penrose-Yukich_2001_Weak-Laws-Geometric-Probability.pdf"
source_filename: "Penrose-Yukich_2001_Weak-Laws-Geometric-Probability.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "excellent"
extraction_score: 100.0
visual_assets: "disabled"
references_file: "../references/Penrose-Yukich_2001_Weak-Laws-Geometric-Probability.references.md"
---

<!-- p:1 -->

## Weak laws in geometric probability

Mathew D. Penrose and J. E. Yukich 1

University of Durham and Lehigh University

July 2001

###### Abstract

Using a coupling argument, we establish a general weak law of large numbers for functionals of binomial point processes in d -dimensional space, with a limit that depends explicitly on the (possibly non-uniform) density of the point process. The general result is applied to the minimal spanning tree, the k -nearest neighbors graph, the Voronoi graph, and the sphere of influence graph. Functionals of interest include total edge length with arbitrary weighting, number of vertices of specifed degree, and number of components. We also obtain weak laws for functionals of marked point processes, including statistics of Boolean models.

## 1 Introduction

Establishing laws of large numbers (LLN) for functionals of random Euclidean point sets is of considerable interest. When the point set forms the vertex set of a graph, functionals of interest include total edge length with arbitrary weighting, number of edges, and number of components. Relevant graphs include those in computational geometry, such as the minimal spanning tree, the k -nearest neighbors graph, Voronoi graph, and sphere of influence graph (these graphs are formally defined in Section 2.3). When the random Euclidean point set is a marked point set, then functionals of interest include those arising in the stochastic geometry of Boolean models.

For many functionals, subadditivity works well as a basic tool; see [27] and [29] for surveys. This is the case with power-weighted edge length functionals. For example, if G ( n, f ) is the minimal spanning tree (MST) on n i.i.d. random d -vectors with common density f on R d , and if | e | denotes the length of the edge e , then the following asymptotics hold for the sum ∑ e ∈ G ( n,f ) | e | α of the power-weighted edge lengths:

Department of Mathematical Sciences, University of Durham, South Road, Durham DH1 3LE, England: m athew.penrose@durham.ac.uk

Department of Mathematics, Lehigh University, Bethlehem PA 18015, USA: j oseph.yukich@lehigh.edu

1 Research supported in part by NSA grant MDA904-01-1-0029


<!-- p:2 -->


Theorem 1.1 If either (i) 1 ≤ α &lt; d, ∫ R d f ( x ) ( d - α ) /d dx &lt; ∞ , and ∫ R d | x | r f ( x ) dx &lt; ∞ for some r &gt; d/ ( d - α ) or (ii) α ≥ d and f has support on [0 , 1] d , and is bounded away from zero, then as n →∞

$$n ^ { ( \alpha - d ) / d } \sum _ { e \in G ( n , f ) } | e | ^ { \alpha } \rightarrow C ( \alpha , d ) \int _ { \mathbb { R } ^ { d } } f ( x ) ^ { ( d - \alpha ) / d } d x \ a . s . , \quad \ \ ( 1 . 1 )$$

where C ( α, d ) is a positive constant.

For a proof see [29] for case (i) and see [30] for case (ii).

However, many functionals are not amenable to subadditive methods. For example, if the edge lengths | e | in a Euclidean graph G are weighted by a general function φ , giving a sum of the form ∑ e ∈ G φ ( | e | ), then subadditive methods break down, and the LLN behavior is much less well understood. Functionals involving the Voronoi, Delaunay, and sphere of influence graphs are also generally not amenable to subadditive methods. Functionals of marked point processes are usually not subadditive either. Moreover, even when subadditive methods are applicable, they provide little information on the numerical values of limiting constants such as C ( α, d ) appearing in (1.1).

An alternative approach is the so-called 'objective method'. Steele [27] coined this term for a philosophy whereby, loosely speaking, one uses the locally Poisson nature of a binomial point process to describe the limiting behavior of functionals on finite point sets in terms of related functionals defined on infinite Poisson point sets. Aldous and Steele [1] used this idea to analyze certain functionals associated with the MST on uniform points, but one might expect it to be applicable to any functional, including those defined over non-uniform point samples, consisting of contributions which are locally determined in some sense. As noted in [1, 27], making formal sense of this intuition is not always quite so simple as one might imagine.

In an attempt to formulate in general terms the idea of locally determined contributions, Penrose and Yukich [23, 24] introduce a concept of 'stabilizing' functionals and essentially use the objective method to establish a strong law of large numbers (Theorem 3.2 of [24]) for stabilizing functionals on uniform point sets in R d . Jimenez and Yukich [15] obtain sufficient conditions yielding laws of large numbers for sums involving general edge weights and non-uniform point sets, but their conditions are rather strong and are limited to increasing functions φ .

The goal of this paper is to use the objective method to provide relatively simple conditions guaranteeing a general weak LLN for stabilizing functionals on possibly non-uniform point samples of size n . We illustrate the diverse applications of the general LLN by obtaining weak laws for functionals of spatial point processes in computational geometry as well as functionals of marked point processes, including those arising in packing processes and the stochastic geometry of Boolean models.

Many stabilizing functionals are defined in terms of graphs G which are themselves stabilizing, i.e., locally determined in a sense to be made precise below; stabilizing graphs include the MST, k -nearest neighbor, Voronoi, and sphere of influence graph. Given a stabilizing graph G , the theory applies to functionals such as the number of leaves, the number of components, and the sum of weighted edge lengths ∑ e ∈ G φ ( | e | ). In these graphs, edges are between 'nearby' points, and since the density of points grows in proportion to n , the typical distance between nearby points can be thought of as decreasing in proportion to n - 1 /d . Therefore we consider sums of the form ∑ e ∈ G φ ( n 1 /d | e | ), establishing weak LLN behavior. The limiting constants are defined explicitly in terms of φ , the density f , and certain graphs on Poisson processes, thereby providing extra information on the value of limiting constants such as that arising in (1.1) that is not given by subadditive methods alone, even in the classic case when φ is the identity function.


<!-- p:3 -->


## 2 Main Results

### 2.1 Terminology

In Section 2.2 we shall formulate a collection of general LLN results. Before doing so we need some terminology.

Given X ⊂ R d and a positive scalar a , let a X := { ax : x ∈ X} . Given y ∈ R d set y + X := { y + x : x ∈ X} . For x ∈ R d , let | x | be its Euclidean modulus and for r &gt; 0, let B ( x ; r ) denote the Euclidean ball { y ∈ R d : | y - x | ≤ r } . Let 0 denote the origin of R d .

Suppose ξ ( x ; X ) is a measurable R + -valued function defined for all pairs ( x, X ), where X ⊂ R d and x is an element of X . We assume that X is locally finite, i.e., contains only finitely many points in any bounded region. Suppose ξ is translation invariant, i.e. ξ ( y + x ; y + X ) = ξ ( y ; X ) for all y ∈ R d and all x, X . Then ξ induces a translation-invariant functional H ξ defined on finite point sets X ⊂ R d by

$$H _ { \xi } ( \mathcal { X } ) \coloneqq \sum _ { x \in \mathcal { X } } \xi ( x ; \mathcal { X } ) .$$

Functionals admitting the representation (2.1) include the total edge length, the total number of edges, the total number of components, and total number of vertices of fixed degree of Euclidean graphs. Later on, in cases with x / ∈ X it will be useful to abbreviate the notation ξ ( x ; X ∪ { x } ) to ξ ( x ; X ).

We probe the behavior of the functional H ξ by inserting an extra point into its domain. For 'typical' point sets X , it is conceivable that the contribution ξ ( x ; X ) is not affected by changes in X which are far from x . We formalize this notion as follows. For any locally finite point set S ⊂ R d , and any integer m ∈ N define

$$\bar { \xi } ( \mathcal { S } ; m ) \coloneqq \sup _ { n \in \mathbb { N } } ( \text {ess} \sup _ { m , n } \{ \xi ( 0 ; ( \mathcal { S } \cap B ( 0 ; m ) ) \cup \mathcal { A } ) \} )$$

and

$$\underline { \xi } ( \mathcal { S } ; m ) \coloneqq \inf _ { n \in \mathbb { N } } ( e s s \inf _ { m , n } \{ \xi ( 0 ; ( \mathcal { S } \cap B ( 0 ; m ) ) \cup \mathcal { A } ) \} ) ,$$


<!-- p:4 -->


where ess sup m,n (respectively ess inf m,n ) is essential supremum (infimum), with respect to Lebesgue measure on R dn , over sets A ⊂ R d \ B ( 0 ; m ) of cardinality n . Define ξ ∞ ( S ), called the limit of ξ on S , by

$$\xi _ { \infty } ( \mathcal { S } ) \colon = \lim _ { m \to \infty } \overline { \xi } ( \mathcal { S } ; m ) .$$

We shall say the functional ξ stabilizes on S if

$$\lim _ { m \to \infty } \bar { \xi } ( \mathcal { S } ; m ) = \lim _ { m \to \infty } \underline { \xi } ( \mathcal { S } ; m ) = \xi _ { \infty } ( \mathcal { S } ) .$$

For τ ∈ (0 , ∞ ), let P τ be a homogeneous Poisson point process of intensity τ on R d . We are interested particularly in functionals that stabilize almost surely on P τ . Note that with probability 1, ξ ( P τ ; m ) is nonincreasing in m and ξ ( P τ ; m ) is nondecreasing in m , so they both converge. Stabilization means they converge to the same limit, almost surely. The present formulation of stabilization is weaker than that of [24]. Any functional ξ ( x ; X ) which depends only on the points of X within a fixed distance of x is stabilizing on P τ .

We are interested in functionals on spatial point processes involving nonuniform points, defined as follows. Let X 1 , X 2 , . . . be i.i.d. d -dimensional random variables with common density f , which is fixed but arbitrary. Define the induced binomial point processes

$$\mathcal { X } _ { n } \colon = \mathcal { X } _ { n } ( f ) \colon = \{ X _ { 1 } , \dots , X _ { n } \} , \quad n \in \mathbb { N } .$$

Our general limit theory is not for H ξ ( X n ), but for H ξ n ( X n ), where we define

$$\xi _ { n } ( x ; \mathcal { X } ) \colon = \xi ( n ^ { 1 / d } x ; n ^ { 1 / d } \mathcal { X } ) .$$

To obtain a LLN for H ξ n ( X n ) we use the following approach. By coupling n 1 /d X n to a Poisson process of varying intensity, we show that the local behavior of ξ ( n 1 /d X 1 ; n 1 /d X n ) is approximated by the local behavior of the coupled Poisson process. If the functional ξ stabilizes on homogeneous Poisson point processes, then a conditioning argument shows distributional convergence of ξ ( n 1 /d X i ; n 1 /d X n ) for each X i ∈ X n . Under appropriate moment conditions on ξ , this gives a weak LLN for H ξ n . This formalizes the intuitive notion that the limiting behavior of H ξ n on finite sets is related to the behavior of ξ ∞ on the infinite set P τ .

Many of the applications that we consider are concerned with functionals of graphs of the form G = G ( X ) defined for each locally finite point set X ⊂ R d , where either G ( X ) or (in the case of the Voronoi graph) its planar dual has vertex set X .

We shall say G is translation invariant if translation by y is a graph isomorphism from G ( X ) to G ( y + X ) for all y ∈ R d and all locally finite point sets X . We shall say G is scale invariant if scalar multiplication by a induces a graph isomorphism from G ( X ) to G ( a X ) for all X and all a &gt; 0.

It is useful to have a notion of stabilization for these graphs. Given G , and given a vertex x ∈ X , let E ( x ; G ( X )) be the set of edges of G ( X ) incident to x


<!-- p:5 -->


(or for the Voronoi graph, the set of edges whose planar duals are incident to x ). Let P τ, 0 := P τ ∪ { 0 } . We shall say that G stabilizes on P τ if there exists a random but almost surely finite variable R such that

$$\mathcal { E } ( 0 ; G ( \mathcal { P } _ { \tau , 0 } ) ) = \mathcal { E } ( 0 ; G ( \mathcal { P } _ { \tau , 0 } \cap B ( 0 ; R ) ) \cup \mathcal { A } )$$

for all finite A ⊂ R d \ B ( 0 ; R ).

Stabilization of the graph G says that the local behavior of the graph in a bounded region is unaffected by points beyond a finite (but random) distance from that region. As we shall see, the minimal spanning tree and the k -nearest neighbors, Voronoi, Delaunay, and sphere of influence graphs are all stabilizing on P τ , τ ∈ (0 , ∞ ).

### 2.2 General LLN results

The following theorem places the objective method in a general context, shows that the asymptotic behavior of H ξ n ( X n ) is sensitive to the underlying density f , and explicitly identifies the asymptotic constants in terms of f and the limit functional ξ ∞ . It will be proved in Section 3.

Theorem 2.1 (General LLN) Suppose q = 1 or q = 2 . Suppose ξ is almost surely stabilizing on P τ , with limit ξ ∞ ( P τ ) , for all τ ∈ (0 , ∞ ) . If ξ satisfies the moments condition

$$\sup _ { n \in \mathbb { N } } E [ \xi ( n ^ { 1 / d } X _ { 1 } ; n ^ { 1 / d } \mathcal { X } _ { n } ) ^ { p } ] < \infty ,$$

for some p &gt; q , then as n →∞ ,

$$n ^ { - 1 } H _ { \xi _ { n } } ( \mathcal { X } _ { n } ) \rightarrow \int _ { \mathbb { R } ^ { d } } E [ \xi _ { \infty } ( \mathcal { P } _ { f ( x ) } ) ] f ( x ) d x \quad \text {in} \ L ^ { q } .$$

Obviously, for there to be any possibility at all for the mean of the left side of (2.6) to converge to a finite limit, the moments condition (2.5) must hold for p = 1. In this sense, when q = 1, the moments condition (2.5) is close to being the best possible.

A simplification arises in the case where there is a constant γ &gt; 0 such that ξ satisfies the relation

$$\xi ( a x ; a \mathcal { X } ) = a ^ { \gamma } \xi ( x ; \mathcal { X } )$$

for all positive scalars a and all finite point sets X and x ∈ X . In this case we say ξ is homogeneous of order γ . Homogeneity of order γ implies that ξ n ( x ; X ) = n γ/d ξ ( x ; X ). Moreover, almost sure stabilization on P 1 with limit ξ ∞ ( P 1 ), together with homogeneity of order γ , implies stabilization on P τ with limit τ - γ/d ξ ∞ ( P 1 ), for any τ &gt; 0. Therefore the L q limit in (2.6) simplifies to

$$E [ \xi _ { \infty } ( \mathcal { P } _ { 1 } ) ] \int _ { \mathbb { R } ^ { d } } f ( x ) ^ { ( d - \gamma ) / d } d x .$$


<!-- p:6 -->


Even simpler is the special case where the function ξ is scale invariant , i.e., is homogeneous of order 0. In this case the expresion (2.7) simplifies to E [ ξ ∞ ( P 1 )], and the large n behavior of scale invariant functionals is not sensitive to the density of the underlying point set.

Theorem 2.1 admits the following extension to functionals defined on marked point sets. Let ( K , F K , P K ) be a probability space. A marked point set is a subset of R d × K , to be denoted  ̃ X where X is an (unmarked) subset of R d and the tilde indicates that each element x of X carries a mark in K (and with its mark, is denoted  ̃ x ). In this context, a functional ξ ( ̃ x ;  ̃ X ) is said to be translation invariant if for all y ∈ R d , and for any element  ̃ x of any marked point set  ̃ X , we have ξ ( τ y ( ̃ x ); τ y (  ̃ X )) = ξ ( ̃ x ;  ̃ X ) where τ y is the translation operator sending any element ( x, t ) ∈ R d ×K to ( y + x, t ) (i.e., leaving the mark unchanged).

In the random setting, assume the marks are i.i.d. with distribution P K . We are interested in the cases where X is the point process X n or P τ ; in both cases assume the mark values are independent of the set X . We say that ξ stabilizes on the marked Poisson point process  ̃ P τ if (2.2) holds with S replaced by  ̃ P τ .

If ξ is translation invariant and almost surely stabilizing on  ̃ P τ , with limit ξ ∞ (  ̃ P τ ) , τ ∈ (0 , ∞ ), and if ξ satisfies the moments condition (2.5) for some p &gt; q , then as n → ∞ , we obtain a version of (2.6) for marked processes, namely,

$$n ^ { - 1 } H _ { \xi _ { n } } ( \tilde { \mathcal { X } } _ { n } ) \rightarrow \int _ { \mathbb { R } ^ { d } } E [ \xi _ { \infty } ( \tilde { \mathcal { P } } _ { f ( x ) } ) ] f ( x ) d x \quad \text {in} \ L ^ { q } .$$

In applications of (2.8), it will be clear that we are considering marked point processes and for simplicity we will thus suppress mention of the tilde.

Many applications of Theorem 2.1 are defined in terms of functionals of graphs arising in computational geometry. Suppose the graph G := G ( X ) is defined for all locally finite X . Given G , functionals such as total length, number of edges, or number of edges less than some specified length are of interest. These and other functionals may be interpreted as a total of φ -weighted edge lengths, i.e., as a sum

$$L _ { \phi } ^ { G } ( \mathcal { X } ) \coloneqq \sum _ { e \in G ( \mathcal { X } ) } \phi ( | e | ) ,$$

with φ : [0 , ∞ ] → [0 , ∞ ) a specified function. Also of interest are the number of components, which we denote K G ( X ), and, for any specified finite connected unlabeled graph Γ, the number of vertices x ∈ X for which G ( X ) contains a subgraph isomorphic to Γ with a vertex at x , which we denote V G Γ ( X ). Let σ G be the order of the component (i.e., the number of vertices in the component) containing the origin of G ( P 1 , 0 ), and let E Γ be the event that G ( P 1 , 0 ) contains a subgraph isomorphic to Γ with a vertex at the origin.

Note that both K G ( X ) and V G Γ ( X ), as well as L G φ ( X ) in the case φ ≡ 1 (the total number of edges) are scale invariant functionals of X .

The following general result, proved in Section 3, is a consequence of Theorem 2.1.


<!-- p:7 -->


Theorem 2.2 Suppose G is translation and scale invariant and stabilizes on P 1 . Then

$$n ^ { - 1 } K ^ { G } ( \mathcal { X } _ { n } ) \rightarrow E [ \sigma _ { G } ^ { - 1 } ] \ i n \ L ^ { 2 }$$

and for any finite connected graph Γ ,

$$n ^ { - 1 } V _ { \Gamma } ^ { G } ( \mathcal { X } _ { n } ) \to P [ E _ { \Gamma } ] \ i n \ L ^ { 2 } .$$

Moreover, if q = 1 or q = 2 and φ : [0 , ∞ ] → [0 , ∞ ) is a specified function with

$$\sup _ { n \in \mathbb { N } } E \left [ \left ( \sum _ { e \in \mathcal { E } ( X _ { 1 } ; G ( \mathcal { X } _ { n } ) ) } \phi ( n ^ { 1 / d } | e | ) \right ) ^ { p } \right ] < \infty$$

for some p &gt; q , then

$$n ^ { - 1 } L _ { \phi } ^ { G } ( n ^ { 1 / d } \mathcal { X } _ { n } ) \rightarrow \frac { 1 } { 2 } \int _ { \mathbb { R } ^ { d } } E \sum _ { e \in \mathcal { E } ( 0 ; G ( \mathcal { P } _ { 1 , 0 } ) ) } \phi \left ( \frac { | e | } { f ( x ) ^ { 1 / d } } \right ) f ( x ) d x \quad \text {in} \ L ^ { q } . \ ( 2 . 1 3 )$$

The conclusions of Theorems 2.1 and 2.2 can be strengthened in more than one way. If, for example, q &gt; 2 is an integer, and if ξ satisfies the moments condition (2.5) for some p &gt; q , then a modification of the coupling arguments given in Section 3 yields convergence in L q . Moreover, for many functionals, convergence of the means E [ n - 1 H ξ n ( X n ) ] , as given by Theorems 2.1 and 2.2, implies almost sure and even complete convergence using concentration inequalities involving either isoperimetric methods or sums of martingale differences; we will not pursue this but refer to [15, 24, 29] for details. We will also not seek to establish rates of convergence in our general results.

##### Remarks .

- (a) In the special case where φ ( x ) = x α (i.e., power-weighted edges), the lefthand side of (2.13) equals n ( α - d ) /d L G φ ( X n ), while the right-hand side of (2.13) simplifies to C G ( d, α ) ∫ R d f ( x ) ( d - α ) /d dx , with C G ( d, α ) := 1 2 E ∑ e φ ( | e | ), the sum being over all e ∈ E ( 0 ; G ( P 1 , 0 )). This provides extra information about, for example, the limiting constant in (1.1).
- (b) The stabilizing hypothesis of Theorem 2.1 can be weakened to one requiring that ξ be almost surely stabilizing on P f ( x ) , with limit ξ ∞ ( P f ( x ) ), for almost all x in the support of the density f . These weakened hypotheses are used in Theorem 2.7 below. The moments condition (2.5) is not always easy to check, but is obviously true for any p when the functional ξ is uniformly bounded. In Section 2.3 we shall verify the moments condition (2.12) for various graphs.
- (c) Even without the moments condition (2.5), the stabilization assumption in Theorem 2.1 is enough to guarantee that the right side of (2.6) is a lower bound for lim inf E [ n - 1 H ξ n ( X n )]; this is proved by following the proof of Lemma 3.2 below and applying Fatou's Lemma. Likewise, even without the moments condition (2.12), a weaker version of (2.13) holds in which the right hand side


<!-- p:8 -->


is a lower bound for the liminf of the expectation of the left hand side. With the moments condition (2.5) (respectively, (2.12)) the integral on the right hand side of (2.6) (respectively, (2.13)) is finite.

- (d) Limit laws such as (2.10) and (2.11) for scale invariant functionals are of interest in multi-dimensional scaling [5]. In this context, given the matrix of interpoint distances between pairs of points in a data set X , one seeks to identify the dimension in which a data set lives. To identify the underlying dimension, it is useful to study scale invariant functionals of the interpoint distances, since these are precisely the functionals whose asymptotics are sensitive only to the dimension of the support of the distribution of the data points and not on the underlying density. This approach to dimension identification may be relatively inexpensive from a computational point of view [6].
- (e) Without further conditions on ξ and H ξ n , we are unable to obtain asymptotics for H ξ n over point sets consisting of random d -vectors having a law with a singular component.
- (f) Suppose the conditions of Theorem 2.1 are satisfied with q = 2. Since ξ 2 is almost surely stabilizing on P τ , with limit ξ 2 ∞ ( P τ ), and since ξ 2 satisfies the moments condition (2.5) for some p &gt; 1, it follows that the sample variance of { ξ n ( X i ; X n ) , 1 ≤ i ≤ n } , namely the quantity

$$\underline { \sum _ { i = 1 } ^ { n } ( \xi _ { n } ( X _ { i } ; \mathcal { X } _ { n } ) ) - n ^ { - 1 } \sum _ { i = 1 } ^ { n } \xi _ { n } ( X _ { i } ; \mathcal { X } _ { n } ) ) ^ { 2 } }$$

converges in L 1 to Var( ξ ∞ ( P f ( X 1 ) )) .

- (g) The limit (2.11) says, loosely speaking, that the number of vertices of G ( X n ) satisfying any property determined by the local graph structure within a bounded graph distance exhibits LLN behavior. For example, it yields a LLN for the proportionate number of vertices of any fixed degree, among other things.
- (h) A version of Theorem 2.2 also holds for directed graphs. In this context the limit (2.13) holds without the factor of 1 / 2 and with E ( x ; G ( X )) defined to be the set of edges going into x .

### 2.3 Applications

The applications of Theorems 2.1 and 2.2 range from the treatment of functionals in computational geometry to the statistics of Boolean models as well as to an analysis of packing processes. The following discussion is not meant to be an exhaustive treatment of applications, but is merely meant to indicate the variety of uses of the main theorems.

- (a) Minimal spanning tree . Given a locally finite set X ⊂ R d , d ≥ 2, let MST( X ) be the graph with vertex set x obtained by including each edge e := { x, y } for which there is no path in X from x to y consisting of links which are all shorter than e . If X is finite with distinct inter-point distances, then MST( X ) is the minimal spanning tree on X , i.e. the connected graph with vertex set X of minimal total edge length; see Alexander [2]. If X is infinite, then


<!-- p:9 -->


MST( X ) is the so-called minimal spanning forest on X [2]. Clearly MST( X ) is translation and scale invariant.

The following theorem considerably expands upon Theorem 1.1. We say that φ has polynomial growth of order a &lt; ∞ if φ ( x ) ≤ C (1 + x a ).

Theorem 2.3 Let G ( X ) = MST( X ) . Then (2.11) holds for any finite connected Γ . Also, (2.13) holds with q = 2 if either (i) φ is bounded, or (ii) φ has polynomial growth of order a &lt; ∞ , the support of f is a convex polyhedron and f is bounded away from infinity and zero on its support, and (2.13) holds with q = 1 if (iii) φ has polynomial growth of order a &lt; d and ∫ R d | x | r f ( x ) dx &lt; ∞ , for some r &gt; max { ad/ ( d - a ) , d/ ( d - a ) } , and ∫ R d f ( x ) ( d - a ) /d dx &lt; ∞ .

Special cases of Theorem 2.3 include an L 2 version of Theorem 1.1 (take φ to be a power function) and the L 2 LLN for the empirical distribution function of rescaled edge lengths in the MST, first obtained by Penrose [21] (take φ ( x ) := 1 [0 ,t ] ( x )). For uniformly distributed points, Bezuidenhout et al. [4] obtained an almost sure version of the latter result. The first part (2.11) of the conclusion in Theorem 2.3 yields an L 2 version of the results of [28] and Theorem 5.2.2 of [27], concerning the number of vertices of fixed degree.

Proof of Theorem 2.3. The set of edges of MST( P 1 , 0 ) incident to the origin is unaffected by any additions or deletions of points outside a ball of random but almost surely finite radius, i.e. G ( X ) = MST( X ) is stabilizing on P 1 . This follows from the definition of MST( X ) and the simultaneous uniqueness of percolation clusters (Alexander [3]), and the almost sure existence of a 'blocking set' of Poisson points lying in some annulus surrounding the origin and precluding the possibility of any edge from the origin to the exterior of that annulus. For more details see Lee [16].

Theorem 2.2 then gives us (2.11). To prove (2.13) it remains only to verify the moments condition (2.12). Note first that points in the MST have a degree which is uniformly bounded by some finite constant C ( d ) (Lemma 4 of [1]). Hence under condition (i), i.e. if φ is bounded, then ∑ e ∈E ( x ; G ( X )) φ ( | e | ) is also bounded for any point set X and x ∈ X , and thus (2.12) is clearly satisfied, showing that (2.13) holds in this case.

The uniform bound on vertex degrees implies that for any p &gt; 1, there is a second constant C ( p, d ) such that for any X and any x ∈ X ,

$$\left ( \sum _ { e \in \mathcal { E } ( x ; G ( \mathcal { X } ) ) } \phi ( n ^ { 1 / d } | e | ) \right ) ^ { p } & \leq C ( p , d ) \sum _ { e \in \mathcal { E } ( x ; G ( \mathcal { X } ) ) } \phi ^ { p } ( n ^ { 1 / d } | e | ) . \\ \text {Suppose condition} \left ( \text {ij} \text { holds } i \text { e. } \phi \text { has polynomial growth of order } a < \infty \right )$$

Suppose condition (ii) holds, i.e. φ has polynomial growth of order a &lt; ∞ and the support of f is a convex polyhedron with the restriction of f to its support bounded away from zero and infinity. Then by the uniform bound on vertex degrees, the right hand side of (2.14) is bounded by a constant plus a constant multiple of

$$n ^ { a p / d } \max _ { e \in \mathcal { E } ( x ; G ( \mathcal { X } ) ) } | e | ^ { a p } .$$


<!-- p:10 -->


Lemma 2.1 of [30] shows that

$$E [ \max \{ | e | ^ { a p } \colon e \in \mathcal { E } ( X _ { 1 } ; G ( \mathcal { X } _ { n } ) ) \} ] = O ( n ^ { - a p / d } )$$

and therefore the left side of (2.12) is uniformly bounded by a constant. Therefore, under condition (ii), the conclusion (2.13) (with q = 2) holds.

Finally consider case (iii). Put ξ n ( x ; X ) := ∑ e ∈E ( x,G ( X )) φ ( n 1 /d | e | ). If φ has polynomial growth of order a then by exchangeability and (2.14),

$$\pi$$

$$E [ ( \xi _ { n } ( X _ { 1 } ; \mathcal { X } _ { n } ) ) ^ { p } ] & = n ^ { - 1 } E \sum _ { i = 1 } ^ { n } ( \xi _ { n } ( X _ { i } ; \mathcal { X } _ { n } ) ) ^ { p } \\ & \leq C ( p , d ) n ^ { - 1 } E \sum _ { i = 1 } ^ { n } \sum _ { e \in \mathcal { E } ( X _ { i } ; G ( \mathcal { X } _ { n } ) ) } \phi ^ { p } ( n ^ { 1 / d } | e | ) \\ & = 2 C ( p , d ) n ^ { - 1 } E \sum _ { e \in G ( X _ { n } ) } \phi ^ { p } ( n ^ { 1 / d } | e | ) \\ & \leq C _ { 1 } ( p , d ) + C _ { 2 } ( p , d ) n ^ { ( a p - d ) / d } E \sum _ { e \in G ( \mathcal { X } _ { n } ) } | e | ^ { a p } . \\ \intertext { W e n o w b o und the r i g h t h a n d s i d e o f ( 2 . 1 6 ) . $ L e t $ L ^ { a p } ( \mathcal { X } ) \colon = \sum _ { e \in G ( \mathcal { X } ) } | e | ^ { a p } } \intertext { W e n o w b o und the r i g h t h a n d s i d e o f ( 2 . 1 6 ) . $ L e t $ L ^ { a p } ( \mathcal { X } ) \colon = \sum _ { e \in G ( \mathcal { X } ) } | e | ^ { a p } }$$

We now bound the right hand side of (2.16). Let L ap ( X ) := ∑ e ∈ G ( X ) | e | ap and for all k ≥ 1, let A k denote the annular shell centered around the origin of R d with inner radius 2 k and outer radius 2 k +1 (Let A 0 be the ball centered at the origin with radius 2). Note that, as in (7.21) of [29],

$$L ^ { a p } ( \mathcal { X } _ { n } ) \leq \sum _ { 0 \leq k \leq s ( n ) } L ^ { a p } ( \mathcal { X } _ { n } \cap A _ { k } ) + C ( p ) \max _ { 1 \leq i \leq n } | X _ { i } | ^ { a p } ,$$

where s ( n ) is the largest k such that A k ∩ X n is not empty. We need to show, after taking expectations and dividing by n ( d - ap ) /d , that the two terms on the right are bounded uniformly in n . By Jensen's inequality and the growth bounds L ap ( X ) ≤ C (diam X ) ap (card( X )) ( d - ap ) /d (see Lemma 3.3 of [29]), the first term is upper bounded by

$$C \sum _ { k \geq 1 } 2 ^ { k a p } ( P [ X _ { 1 } \in A _ { k } ] ) ^ { ( d - a p ) / d }$$

which is finite by the integrability hypothesis (see p. 85 of [21]). The second term is bounded by

$$C ( p ) \int _ { 0 } ^ { \infty } P \left [ \max _ { 1 \leq i \leq n } | X _ { 1 } | ^ { a p } \geq t m ^ { ( d - a p ) / d } \right ] d t \\$$

$$\leq n C ( p ) \int _ { 0 } ^ { \infty } P \left [ | X _ { 1 } | ^ { a p d / ( d - a p ) } \geq t ^ { d / ( d - a p ) } n \right ] d t .$$

By Markov's inequality together with the moment condition ∫ R d | x | r f ( x ) dx &lt; ∞ , for some r &gt; ad/ ( d - a ), this last integral is finite. Thus under condition


<!-- p:11 -->


(iii), we can choose p &gt; 1 so that (2.16) is uniformly bounded, and hence the moments condition (2.12) is satisfied, showing the validity of the conclusion under condition (iii).

(b) k -nearest neighbors graphs . Let k be a positive integer. Given a locally finite point set X ⊂ R d , the k -nearest neighbors (undirected) graph on X , denoted NG( X ), is the graph with vertex set X obtained by including { x, y } as an edge whenever y is one of the k nearest neighbors of x and/or x is one of the k nearest neighbors of y . The k -nearest neighbors (directed) graph on X , denoted NG ′ ( X ), is the graph with vertex set X obtained by placing an edge between each point and its k nearest neighbors. If the k -th nearest neighbor of x is not well-defined (i.e., if there is a 'tie' in the ordering of interpoint distances involving x ), use the lexicographic ordering as a 'tie-breaker' to determine the k nearest neighbors. Such a tie has zero probability for the random point sets under consideration here.

It is clear that the k -nearest neighbors graphs are translation and scale invariant. The following generalizes and extends the asymptotics for the sum of power-weighted edge lengths by McGivney [18], Yukich (Theorem 8.3 of [29]), and Jimenez and Yukich [15], who limit attention to continuous densities and increasing φ . It also extends Theorem 2 of Eppstein, Paterson and Yao [8], who prove convergence of the mean number of components for uniform samples.

Theorem 2.4 Let G ( X ) denote either NG( X ) or NG ′ ( X ) . Then (2.10) and (2.11) hold. Moreover, (2.13) holds, with q = 2 , if either (i) φ is bounded, or (ii) φ has polynomial growth of order a &lt; ∞ , the support of f is a convex polyhedron and f is bounded away from infinity and zero. Finally the directed graph version of (2.13) holds for NG ′ ( X ) with q = 1 if φ has polynomial growth of order a &lt; d , ∫ R d f ( x ) ( d - a ) /d dx &lt; ∞ , and ∫ R d | x | r f ( x ) dx &lt; ∞ for some r &gt; d/ ( d - a ) .

Proof. We apply Theorem 2.2. As shown in Lemma 6.1 of [23] (even though the definition of stabilization there is slightly different), the set of edges incident to the origin in NG( P 1 , 0 ) is unaffected by the addition or removal of points outside a ball of random but almost surely finite radius, i.e. the graph G ( X ) = NG( X ) is stabilizing on P 1 . Similar arguments show that NG ′ ( X ) is stabilizing on P 1 . Therefore Theorem 2.2 yields (2.10) and (2.11) for NG( X ) and NG ′ ( X ).

To prove (2.13) it remains only to verify the moments condition (2.12). This condition is checked, under any of the conditions (i), (ii), or (iii), in very much the same manner as for the MST of Theorem 2.3. The existence of a uniform bound on the degree of vertices in the nearest neighbors graph is Lemma 8.4 of [29]. Under condition (iii), we note that since NG ′ is subadditive without any error term, the last term in (2.17) is not needed, eliminating the need for the condition r &gt; ad/ ( d - a ).

Henze [12] considers the fraction of points in X n which are the nearest neighbors of exactly j other points; he also considers the fraction of points in X n that are the l th nearest neighbors to their own k th nearest neighbor. He shows that the limits of these fractions converge to explicit but rather complicated limiting constants. A directed-graph version of (2.11) in Theorem 2.2 yields Henze's results and shows that one can interpret his limiting constants in terms of a functional evaluated at a point in the origin of the homogeneous Poisson point process.


<!-- p:12 -->


(c) Voronoi and Delaunay graphs . Given a locally finite set X ⊂ R d , and given x ∈ X , the locus of points closer to x than to any other point ∈ X is called the Voronoi cell centered at x . The graph on vertex set X in which each pair of adjacent cell centers is connected by an edge is called the Delaunay graph on X ; if d = 2, then the planar dual graph consisting of all boundaries of Voronoi cells is called Voronoi graph generated by X . Edges of the Voronoi graph can be finite or infinite. Let DEL( X ) (respectively VOR( X )) denote the collection of edges in the Delaunay graph (respectively, the Voronoi graph) on X . The Voronoi and Delaunay graphs are clearly scale and translation invariant.

Theorem 2.5 Let d = 2 and let G ( X ) = VOR( X ) . Then (2.11) holds. Also, if φ has polynomial growth with φ ( ∞ ) = 0 , and if the support of f is a convex polygonal region and if f is bounded away from infinity and zero on its support, then (2.13) holds with q = 2 .

This result adds to McGivney and Yukich [19] and Jimenez and Yukich [15], who require continuous f and functions φ which are either power functions or increasing. If φ is the identity and the support of f is the unit square, then the right hand side of (2.13) simply reduces to 2 ∫ [0 , 1] 2 f ( x ) 1 / 2 dx (see Theorem 1.2 of [19]).

Proof. Once again we apply Theorem 2.2. As in [23], we can verify G ( X ) is stabilizing, i.e., the Voronoi cell centered at the origin for P 1 , 0 is unaffected by changes beyond a random but almost surely finite distance from of the origin. Let E ( X ; VOR( X )) denote the edges of the cell around X 1 in VOR( X n ). Concerning the moments condition (2.12), a modification of Lemma 8.1 of [23] shows that under the prescribed conditions on f and its support,

$$\sup _ { n \in \mathbb { N } } E \left [ \left ( \sum _ { e \in \mathcal { E } ( X _ { 1 } ; V O R ( \mathcal { X } _ { n } ) ) } ( n ^ { 1 / d } | e | ) ^ { a } \right ) ^ { p } \right ] < \infty \\$$

for all a &gt; 0 and p &gt; 2. A modification of the proof of Lemma 2.6 of [19] (pp. 286-87) shows that the cardinality of E ( X 1 ; VOR( X n )) has a finite p th moment for all p &gt; 2. Combining this with (2.20) thus shows that for all φ with polynomial growth

$$\sup _ { n \in \mathbb { N } } E \left [ \left ( \sum _ { e \in \mathcal { E } ( X _ { 1 } ; V O R ( \mathcal { X } _ { n } ) ) } \phi ( n ^ { 1 / d } | e | ) \right ) ^ { p } \right ] < \infty$$


<!-- p:13 -->


for all p &gt; 2. Thus (2.12) holds and the conclusion (2.13) follows.

A similar result to Theorem 2.5 holds if G ( X ) is taken to be the Delaunay graph and E ( x ; DEL( X )) denotes the edges in DEL( X ) incident to x . In this case the conclusion (2.11) yields a LLN for the number of vertices of the Delaunay graph of fixed degree m , for any m = 3 , 4 , 5 , ... . Since this quantity is the same as the total number of cells in the Voronoi graph on X n which are m -gons, this adds to results of Hayen and Quine [11] who determine the proportion of triangles in the Voronoi graph on P 1 .

Finally, for each t &gt; 0 consider the case where ξ ( x ; X ) equals 1 or 0 according to whether the area of the Voronoi cell around x is bounded by t or not. This is one case where it is natural to use Theorem 2.1 rather than Theorem 2.2, and that result yields a LLN for H ξ n ( X n ) := ∑ n i =1 ξ ( n 1 /d X i ; n 1 /d X n ), i.e., a LLN for the empirical distribution function of the rescaled areas of the Voronoi diagram on X n .

(d) Sphere of influence graph . Given a locally finite set X ⊂ R d , the sphere of influence graph SIG( X ) is a graph with vertex set X , constructed as follows: for each x ∈ X let B x be a ball around x with radius equal to min y ∈X\{ x } {| y - x |} . Then B x is called the sphere of influence of x . Draw an edge between x and y iff the balls B x and B y overlap. The collection of such edges is the sphere of influence graph (SIG) on X . It is clearly translation and scale invariant.

The following LLN is apparently new, even for the identity function φ ( x ) = x . In the case φ ( x ) ≡ 1 it extends a result of F ̈ uredi [9] on the mean number of edges of the SIG on uniform point sets (F ̈ uredi identified the limiting constant in this case).

Theorem 2.6 Let G ( X ) = SIG( X ) . Then (2.10) and (2.11) both hold. If φ has polynomial growth and if the support of f is a convex polyhedron and if f is bounded away from infinity and zero on its support, then (2.13) holds with q = 2 .

Proof. We apply Theorem 2.2. As in [23], we can check that the edges incident to the origin in SIG( P 1 , 0 ) are unaffected by changes beyond a random but almost surely finite distance of the origin, i.e. the graph G ( X ) = SIG( X ) is stabilizing. Concerning the moments condition (2.12), the arguments of [23] (Theorem 7.2) show that for any a &gt; 0 , p &gt; 1 , we have under the prescribed conditions on f ,

$$\sup _ { n \in \mathbb { N } } E \left [ \left ( \sum _ { e \in \mathcal { E } ( X _ { 1 } ; S I G ( \mathcal { X } _ { n } ) ) } ( n ^ { 1 / d } | e | ) ^ { a } \right ) ^ { p } \right ] & < \infty . \\ \text {prever, since the third moment of the degree of vertices in the SIG on } \mathcal { X } _ { n }$$

Moreover, since the third moment of the degree of vertices in the SIG on X n is uniformly bounded over all vertices (see e.g. pp. 142-43 of [13]) we obtain for any φ with polynomial growth

$$\text { with polyhom group } & \text { } g \text { on } \mathbb { N } \\ & \sup _ { n \in \mathbb { N } } E \left [ \left ( \sum _ { e \in \mathcal { E } ( X _ { 1 } ; \text {SIG} ( \mathcal { X } _ { n } ) ) } \phi ( n ^ { 1 / d } | e | ) \right ) ^ { p } \right ] < \infty .$$


<!-- p:14 -->


##### Thus (2 . 12) holds.

- (e) Proximity graphs. Devroye [7] defines a proximity graph on X to be one in which each { x, y } is included as an edge if a specified set S ( x, y ) is empty. If S ( x, y ) is the ball with opposite poles at x, y , then the associated proximity graph is the Gabriel graph . If S ( x, y ) is the intersection of B ( x ; | y - x | ) and B ( y ; | y - x | ) then it is the relative neighborhood graph . For a survey of applications of proximity graphs such as these, and also of the sphere of influence graph, see Jaromczyk and Toussaint [14].

Both the Gabriel graph and the relative neighborhood graph are translation and scale invariant, and stabilize on P 1 , and also satisfy (2.12), subject to conditions on φ and f similar to those already given for the sphere of influence graph; see remarks in [23], Section 9. Therefore Theorem 2.2 yields information about these graphs, adding to results in Devroye [7] on the expected number of edges. Numerical estimates for values of mean edge length and mean degree of various proximity graphs over homogeneous Poisson point sets are given by Smith (chapter III.C of [26]).

- (f) Boolean models. As already indicated, Theorem 2.1 extends to marked processes via the limit (2.8). An example of application is to Boolean models, whose importance in stochastic geometry and spatial statistics can be seen from e.g. Hall [10] and Molchanov [20]. Let μ S be a shape distribution , that is, a probability distribution on the space S of all compact sets in R d . For measuretheoretic details see Matheron [17], page 27. Assume that μ S is concentrated on connected sets contained in B ( 0 ; K ) for some fixed finite K (i.e., uniformly bounded connected sets). On a suitable probability space let ( S i , i ≥ 1) be a family of random closed sets each with distribution μ S , independent of each other and of ( X 1 , X 2 , . . . ) (as usual, X 1 , X 2 , . . . are i.i.d. d -vectors with common density f ). Let Ξ n := ∪ n i =1 ( X i + n - 1 /d S i ). We refer to X i + n - 1 /d S i as a random shape centered at X i . The random set Ξ n is a scale-changed Boolean model in the sense of Hall [10], pages 141 and 233.

A connected component of Ξ n is often called a clump . A clump of order k is one which comprises precisely k random shapes. Let U k (Ξ n ) be the number of clumps of order k and let U (Ξ n ) := ∑ k U k (Ξ n ), the total number of clumps. Let V (Ξ n ) denote the total volume of the set Ξ n . In the case d = 2, we consider the total curvature functional of the set Ξ n (the product of 2 π and the Euler characteristic of Ξ n ; see Hall ([10], Ch. 4.3)), which we shall denote W (Ξ n ).

Another statistic of interest is the off-line packing functional for the collection X i + n - 1 /d S i , 1 ≤ i ≤ n . This functional, denoted by M (Ξ n ), is the maximal number of non-intersecting random shapes in the collection X i + n - 1 /d S i , 1 ≤ i ≤ n . Additional statistics associated with Boolean models are found in Molchanov [20], for example.

Let Ξ ∞ ,λ be the infinite Boolean model ∪ X ∈P λ ( X + S X ), where P λ is a homogeneous Poisson process of intensity λ on R d , each point carrying an independent S -valued mark S X with distribution μ S . Let λ c := λ c ( d, μ S ) denote the continuum percolation threshold, i.e., let λ c be the supremum of the set of values of λ such that Ξ ∞ ,λ almost surely has no infinite connected component (note λ c = ∞ if d = 1).


<!-- p:15 -->


Theorem 2.7 (i) There exist constants u k, ∞ ( k ∈ N ) and u ∞ (dependent on μ S ), such that n - 1 U k (Ξ n ) → u k, ∞ in L 2 (for each k ∈ N ) and such that n - 1 U (Ξ n ) → u ∞ in L 2 .

(ii) There exists a constant v ∞ (dependent on μ S ) such that V (Ξ n ) → v ∞ in L 2 .

(iii) If d = 2 and the measure μ S is concentrated on convex sets, then there exists a constant w ∞ (dependent on μ S ) such that W (Ξ n ) converges in L 2 to w ∞ .

(iv) If sup x ∈ R d f ( x ) &lt; λ c , then there is a constant m ∞ such that n - 1 M (Ξ n ) converges in L 2 to m ∞ .

Part (i) of this result adds to existing results in the literature such as Hall's result ([10], Theorem 4.7) on the number of clumps of order 1, especially since we do not restrict attention to a uniform underlying density f for the points X i . As usual, the value of the limiting constant u ∞ is of the form ∫ E [ ξ ∞ ( P f ( x ) )] f ( x ) dx, where ξ ( x ; X ) is described in the proof below.

Part (ii) shows that the volume functional satisfies a weak LLN over nonuniform point sets, adding to results of Hall ([10], Ch. 3.4) involving the vacancy functional of Ξ n . Part (iii) is a weak LLN for the total curvature functional over non-uniform samples, and also adds to results of Hall ([10], Ch. 4.3)).

In part (iii), the constant w ∞ is again of the form ∫ E [ ξ ∞ ( P f ( x ) )] f ( x ) dx, and if μ S is isotropic, there exist analytic formulae for E [ ξ ∞ ( P λ )]; see (2.14) of [20], or (4.28) of [10].

Concerning part (iv), the off-line packing functional can be shown to be subadditive, and methods based on this fact show that a weak LLN also holds, at least for the uniform distribution on a cube of volume 1 /λ , even in the supercritical case λ ≥ λ c .

Sketch of proof of Theorem 2.7. Define the rescaled Boolean model Ξ ′ n by

$$\Xi _ { n } ^ { \prime } \colon = n ^ { 1 / d } \Xi _ { n } = \cup _ { i = 1 } ^ { n } ( n ^ { 1 / d } X _ { i } + S _ { i } ) .$$

Let the mark space be S with mark distribution μ S .

(i) Given a marked point set X ⊂ R d with marks S x , x ∈ X , let ξ ( x ; X ) be the reciprocal of the order of the clump of ∪ y ∈X ( y + S y ) containing x + S x . Then H ξ ( X ) is the total number of clumps of ∪ y ∈X ( y + S y ); hence

$$H _ { \xi _ { n } } ( \mathcal { X } _ { n } ) = U ( \Xi _ { n } ^ { \prime } ) = U ( \Xi _ { n } ) .$$

Stabilization of ξ follows from the fact that μ S is concentrated on uniformly bounded sets. The moments condition (2.5) follows from the uniform bound ξ ( x ; X ) ≤ 1. Therefore the LLN for U (Ξ n ) follows from (2.8). The LLN for U k (Ξ n ) is proved similarly.

(ii) This time let ξ ( x ; X ) be the volume of the intersection of ∪ y ∈X S y with the Voronoi cell around x for X . Then

$$H _ { \xi _ { n } } ( \mathcal { X } _ { n } ) = U ( \Xi _ { n } ^ { \prime } ) = n U ( \Xi _ { n } ) .$$


<!-- p:16 -->


Since μ S is concentrated on sets contained in B ( 0 ; K ), for any x ∈ X , the intersection of ∪ y ∈X S y with the Voronoi cell around x is contained in B ( x ; 2 K ), since any point lying outside B ( x ; 2 K ) but in ∪ y ∈X S y must be closer to some point y ∈ X \ { x } than it is to x . Both the stabilization and the moments conditions in the marked point process version of Theorem 2.1 hold as a consequence of this, and (2.8) yields the LLN for V (Ξ n ).

(iii) This time let ξ ( x ; X ) be the contribution of the random set S x to the total curvature of the union ∪ y ∈X Ξ y . This gives us H ξ ( X n ) = W (Ξ n ). By convexity, ξ ( x ; X ) is uniformly bounded, which gives us the moments condition (2.5).

By the assumption of uniform boundedness of the random sets, if S 0 is an independent random shape inserted at the origin, changes outside B ( 0 ; 2 K ) do not affect the contribution of S 0 to the total curvature. Thus, for all τ , ξ is almost surely stabilizing on P τ . This enables us to deduce the stabilization condition in the marked point process version of Theorem 2.1, and, we therefore deduce the LLN behavior.

- (iv) Let ξ ( x ; X ) be either 1 or 0, depending upon whether or not x + S x is included in the maximal subset of non-intersecting shapes. If there are several such maximal subsets, choose one in an arbitrary deterministic but translationinvariant manner. Then H ξ ( X ) is the maximal number of disjoint shapes and H ξ n ( X n ) = M (Ξ ′ n ). Since ξ ≤ 1, this gives the moments condition (2.5).
- If f &lt; λ c , then there is almost surely no infinite cluster in P f ( x ) , for we are in the subcritical phase of continuum percolation. Since there is no infinite cluster, inserting a random shape at the origin thus almost surely changes the order of only finite clusters and thus the packing functional M stabilizes.
- (g) Packing processes . Consider the following prototypical random sequential packing model. Let B n, 1 , B n, 2 ..., B n,n be a sequence of d -dimensional balls of volume n - 1 whose centers are independent random d -vectors with common probability density function f : R d → [0 , ∞ ). Let the first ball B n, 1 be packed , and recursively for i = 2 , 3 , . . . , n , let the i -th ball B n,i be packed iff B n,i does not overlap any ball in B n, 1 , ..., B n,i - 1 which has already been packed. If not packed, the i -th ball is discarded. Let N f ( n ) be the number of packed balls, out of the first n to arrive. This is sometimes called 'on-line packing', in contrast with the off-line scheme described earlier.

We may use our general result (2.8) for marked processes to obtain LLN for random sequential packing, as follows.

For any finite point set X ⊂ R d , assume the points have marks which are independent and uniformly distributed over [0 , 1]. Assume unit volume balls centered at the points of X arrive sequentially in an order determined by the associated marks, and assume as before that each ball is packed or discarded according to whether or not it overlaps a previously packed ball. Let ξ ( x ; X ) be either 1 or 0 depending on whether the ball centered at x is packed or discarded. Then with the binomial point process X n defined at (2.3), and ξ n defined at (2.4), it can be seen that H ξ n ( X n ) has the same distribution as N f ( n ). Following [24], we can show that ξ is almost surely stabilizing on P τ , τ ∈ (0 , ∞ ), with limit


<!-- p:17 -->


ξ ∞ . Since ξ is bounded it satisfies the moments condition (2.5) and therefore using the limit (2.8) we get the following LLN for N f ( n ).

Theorem 2.8 Let f : R d → [0 , ∞ ) be an arbitrary density. As n →∞ ,

$$n ^ { - 1 } N _ { f } ( n ) \to \int _ { \mathbb { R } ^ { d } } E [ \xi _ { \infty } ( \mathcal { P } _ { f ( x ) } ) ] f ( x ) d x \quad \text {in} \ L ^ { 2 } .$$

This result represents a finite input version of Theorem 5.1 of Penrose [22], but with a more general class of densities f .

Theorem 2.8 extends to more general versions of the prototypical packing model. For example, by following the general stabilization analysis of [24], we can develop asymptotics in the finite input setting for the number of packed balls in the following general models: (i) models with balls replaced by particles of random size/shape/charge, (ii) time dependent, dynamic models, (iii) cooperative sequential adsorption models, and (iv) ballistic deposition models. In each case, we obtain a LLN for the number of packed balls, from among the first n to arrive, when the distribution of the balls has a density f : R d → [0 , ∞ ). See [24] for a discussion of these models and for laws of large numbers in the special case where the particless arrive uniformly at random over R d .

(h) Combinatorial optimization . Both the shortest traveling salesman tour and the minimal matching are translation and scale invariant graphs on finite point sets. However, it is not known whether their definition can be extended to infinite sets in a manner that makes them stabilizing, and therefore we are at present unable to apply Theorem 2.1 or 2.2 in these cases.

## 3 Proofs

The proof of Theorem 2.1 centers around suitably coupling a version of the binomial process X n to a Cox process, that is, a Poisson process whose intensity measure is itself random. We do this as follows. On a suitable probability space suppose we have, independently, a d -dimensional variable X with density f , and a homogeneous Poisson processes P of rate 1 on R d × [0 , ∞ ).

Define coupled point processes P ( n ), X ′ n - 1 , and H n and a random variable ζ n , all in terms of P and X , as follows. Let P ( n ) be the image of the restriction of P to the set

$$\{ ( x , t ) \in \mathbb { R } ^ { d } \times [ 0 \ , \infty ) \colon t \leq n f ( x ) \} ,$$

under the projection ( x, t ) ↦→ x . Then P ( n ) is a Poisson process in R d with intensity function nf ( · ), consisting of N ( n ) random points with common density f . Discard ( N ( n ) - ( n - 1)) + of these points, chosen at random, and add ( n - 1 - N ( n )) + extra independent points with common density f . The resulting set of points is denoted X ′ n - 1 , and has the same distribution as X n - 1 defined earlier.


<!-- p:18 -->


To define H n , let P n be the restriction of P to the set

$$\{ ( x , t ) \colon t \leq n f ( X ) \} .$$

Let H n be the image of the point set P n under the mapping

$$( x , t ) \mapsto n ^ { 1 / d } ( x - X ) .$$

Given X = x , the point process P n is a homogeneous Poisson process of intensity 1 on R d × [0 , nf ( x )], and therefore, given X = x , H n is a homogeneous Poisson process on R d of intensity f ( x ). Define ζ n to be the limit ξ ∞ ( H n ).

Then H n is a Cox process, where the randomness of the intensity measure comes from the value of f ( X ). Note that the distribution of H n , and hence that of ζ n , does not depend on n .

Lemma 3.1 Given K &gt; 0 , we have

$$\lim _ { n \to \infty } P [ n ^ { 1 / d } ( \mathcal { X } _ { n - 1 } ^ { \prime } - X ) \cap B ( 0 ; K ) = \mathcal { H } _ { n } \cap B ( 0 ; K ) ] = 1 .$$

Proof. Suppose X lies at a Lebesgue point of f (see e.g. [25]). Given X = x , the expected number of points of P in B ( x ; Kn - 1 /d ) × [0 , ∞ ) that contribute to H n but not to P ( n ) is

$$n \int _ { B ( x ; K n \ 1 / d ) } ( f ( x ) - f ( y ) ) ^ { + } d y$$

which tends to zero because x is a Lebesgue point of f . The expected number of points of P in B ( x ; Kn - 1 /d ) × [0 , ∞ ) that contribute to P ( n ) but not to H n is

̸

$$n \int _ { B ( x ; K n \ \ 1 / d ) } ( f ( y ) - f ( x ) ) ^ { + } d y$$

which also tends to zero for the same reason. Finally the probability that P ( n ) ∩ B ( x ; Kn - 1 /d ) = X ′ n - 1 ∩ B ( x ; Kn - 1 /d ) tends to zero as n → ∞ , since | N ( n ) - ( n - 1) | is o ( n ) in probability. Integrating over possible values of X and using Dominated Convergence, we obtain (3.1).

Lemma 3.2 Suppose that ξ is almost surely stabilizing on P τ , with limit ξ ∞ ( P τ ) , for all τ ∈ (0 , ∞ ) , and ξ satisfies the moments condition (2.5) for some p &gt; 1 . Then

$$\lim _ { n \to \infty } E [ n ^ { - 1 } H _ { \xi _ { n } } ( \mathcal { X } _ { n } ) ] = \int _ { \mathbb { R } ^ { d } } E [ \xi _ { \infty } ( \mathcal { P } _ { f ( x ) } ) ] f ( x ) d x .$$

Proof. Let ε &gt; 0. Then since

$$\xi _ { n } ( X ; \mathcal { X } _ { n - 1 } ^ { \prime } ) = \xi ( 0 ; n ^ { 1 / d } ( \mathcal { X } _ { n - 1 } ^ { \prime } - X ) ) ,$$


<!-- p:19 -->


for any K ∈ N we have

$$P [ | \xi _ { n } ( X ; \mathcal { X } _ { n - 1 } ^ { \prime } ) - \zeta _ { n } | > \varepsilon ]$$

̸

$$\leq P [ n ^ { 1 / d } ( \mathcal { X } _ { n - 1 } ^ { \prime } - X ) \cap B ( 0 ; K ) \neq \mathcal { H } _ { n } \cap B ( 0 ; K ) ]$$

$$+ P [ \bar { \xi } ( \mathcal { H } _ { n } ; K ) - \underline { \xi } ( \mathcal { H } _ { n } ; K ) > \varepsilon ] .$$

By the stabilization assumption, we can choose K &gt; 0 so that (3.4) is less than ε/ 2, and then by Lemma 3.1, the expression (3.3) is also less than ε/ 2 for n large. Since ζ n have the same distribution for all n , it follows that

$$\xi _ { n } ( X ; \mathcal { X } _ { n - 1 } ^ { \prime } ) \xrightarrow { \mathcal { D } } \zeta _ { 1 } .$$

Since the bounded p -th moments condition (2.5) is assumed to hold for some p &gt; 1, the variables ξ n ( X ; X ′ n - 1 ) are uniformly integrable, and hence their expectations converge to that of ζ 1 . By conditioning on X , we obtain

$$E [ \zeta _ { 1 } ] = \int _ { \mathbb { R } ^ { d } } E [ \xi _ { \infty } ( \mathcal { P } _ { f ( x ) } ) ] f ( x ) d x \coloneqq \mu ,$$

which is the right hand side of (3.2). Since E [ H ξ n ( X n )] = nE [ ξ n ( X ; X ′ n - 1 )], this gives us (3.2).

Next we consider E [ ξ n ( X 1 ; X n ) ξ n ( X 2 ; X n )], and use a refinement of the coupling argument. Assume on a suitable probability space that we have, independently, two d -dimensional variables X and Y with density f , and two homogeneous Poisson proceses P , Q , both of unit intensity on R d × [0 , ∞ ).

Define coupled point processes X ′ n - 2 (a binomial process) and H X n , H Y n (both Cox processes) and variables ζ X n and ζ Y n , all in terms of P , Q , X, and Y , as follows. Let X ′ n - 2 be obtained just as X ′ n - 1 was before, i.e. let P ( n ) be the image of the restriction of P to the set { ( x, t ) ∈ R d × [0 ∞ ) : t ≤ nf ( x ) } , under the projection ( x, t ) ↦→ x , and let N ( n ) be the number of points of P ( n ). Discard ( N ( n ) - ( n - 2)) + of the points of P ( n ), chosen at random, and add ( n - 2 - N ( n )) + extra independent points with common density f . The resulting set of points is denoted X ′ n - 2 and has the same distribution as X n - 2 .

Let F X be the half-space of points in R d closer to X than to Y , and let F Y be the half-space of points in R d closer to Y than to X . Construct H X n as follows. Let P n X be the restriction of P to the set F X × [0 , nf ( X )]; let Q n X be the restriction of Q to the set F Y × [0 , nf ( X )]. Let H X n be the image of the point process P n X ∪ Q n X under the mapping

$$( x , t ) \mapsto n ^ { 1 / d } ( x - X ) .$$

Given X = x , the point process P n X ∪ Q n X is a homogeneous Poisson process of intensity 1 on R d × [0 , nf ( x )]. Hence, given X = x , H X n is a homogeneous Poisson process on R d of intensity f ( x ); let ζ X n be the associated limit ξ ∞ ( H X n ).

Construct H Y n in the following analogous manner. Let P n Y be the restriction of P to the set F Y × [0 , nf ( Y )]; let Q n Y be the restriction of Q to the set F X × [0 , nf ( Y )]. Let H Y n be the image of the point process P n Y ∪ Q n Y under the mapping


<!-- p:20 -->


$$( x , t ) \mapsto n ^ { 1 / d } ( x - Y ) .$$

By an argument similar to that used for H X n , the point process H Y n , given Y = y , is a homogeneous Poisson process on R d of intensity f ( y ); we set ζ Y n := ξ ∞ ( H Y n ).

We can now prove the following result, which is the case q = 2 of Theorem 2.1.

Proposition 3.1 If ξ is almost surely stabilizing on P τ , with limit ξ ∞ ( P τ ) , for all τ ∈ (0 , ∞ ) and if ξ satisfies the moments condition (2.5) for some p &gt; 2 , then as n →∞ ,

$$n ^ { - 1 } H _ { \xi _ { n } } ( \mathcal { X } _ { n } ) \rightarrow \int _ { \mathbb { R } ^ { d } } E [ \xi _ { \infty } ( \mathcal { P } _ { f ( x ) } ) ] f ( x ) d x \quad \text {in} \ L ^ { 2 } .$$

Proof. For any K &gt; 0, we have

$$\lim _ { n \to \infty } P [ n ^ { 1 / d } ( ( \mathcal { X } ^ { \prime } _ { n - 2 } \cup \{ Y \} ) - X ) \cap B ( 0 ; K ) = \mathcal { H } ^ { X } _ { n } \cap B ( 0 ; K ) ] = 1 ;$$

$$\lim _ { n \to \infty } P [ n ^ { 1 / d } ( ( \mathcal { X } _ { n - 2 } ^ { \prime } \cup \{ X \} ) - Y ) \cap B ( 0 ; K ) = \mathcal { H } _ { n } ^ { Y } \cap B ( 0 ; K ) ] = 1 .$$

The proof of these facts is just the same as that of (3.1) using the additional observation that

$$\lim _ { n \to \infty } P [ B ( X ; K n ^ { - 1 / d } ) \subset F _ { X } ] = \lim _ { n \to \infty } P [ B ( Y ; K n ^ { - 1 / d } ) \subset F _ { Y } ] = 1 .$$

Note that H X n and H Y n are independent identically distributed Cox processes. Independence follows by conditioning on the values of X,Y ; given these the point processes H X n and H Y n are constructed from Poisson processes on disjoint regions of space. Therefore, for each n , the variables ζ X n and ζ Y n are independent. Also the joint distribution of ζ X n , ζ Y n is independent of n .

Since by translation invariance

$$\xi _ { n } ( X ; \mathcal { X } ^ { \prime } _ { n - 2 } \cup \{ X , Y \} ) = \xi ( 0 ; n ^ { 1 / d } ( ( \mathcal { X } ^ { \prime } _ { n - 2 } \cup \{ Y \} ) - X ) ) ,$$

and

$$\xi _ { n } ( Y ; \mathcal { X } _ { n - 2 } ^ { \prime } \cup \{ X , Y \} ) = \xi ( 0 ; n ^ { 1 / d } ( ( \mathcal { X } _ { n - 2 } ^ { \prime } \cup \{ X \} ) - Y ) ) ,$$

it follows from (3.8) and (3.9), by a similar argument to that which yielded (3.5), that as n →∞ ,

$$\xi _ { n } ( X ; \mathcal { X } _ { n - 2 } ^ { \prime } \cup \{ X , Y \} ) \xi _ { n } ( Y ; \mathcal { X } _ { n - 2 } ^ { \prime } \cup \{ X , Y \} ) \stackrel { \mathcal { D } } { \longrightarrow } \zeta _ { 1 } ^ { X } \zeta _ { 1 } ^ { Y } ,$$

and hence

$$\xi _ { n } ( X _ { 1 } ; \mathcal { X } _ { n } ) \xi _ { n } ( X _ { 2 } ; \mathcal { X } _ { n } ) \xrightarrow { \mathcal { D } } \zeta _ { 1 } ^ { X } \zeta _ { 1 } ^ { Y } .$$


<!-- p:21 -->


By assumption, the bounded p -th moments condition (2.5) holds for some p &gt; 2. Then by Cauchy-Schwarz,

$$\sup _ { n \in \mathbb { N } } E [ ( \xi _ { n } ( X _ { 1 } ; \mathcal { X } _ { n } ) \xi _ { n } ( X _ { 2 } ; \mathcal { X } _ { n } ) ) ^ { p / 2 } ] < \infty$$

and therefore the variables ξ n ( X 1 ; X n ) ξ n ( X 2 ; X n ), defined for each n ≥ 2, are uniformly integrable, so that the convergence (3.11) also holds in the sense of convergence of means, i.e.

$$\lim _ { n \to \infty } E [ \xi _ { n } ( X _ { 1 } ; \mathcal { X } _ { n } ) \xi _ { n } ( X _ { 2 } ; \mathcal { X } _ { n } ) ] = E [ \zeta _ { 1 } ^ { X } \zeta _ { 1 } ^ { Y } ] = \mu ^ { 2 } ,$$

with μ defined at (3.6) Here we have used independence of ζ X n and ζ Y n . To complete the proof, observe that

$$E [ ( n ^ { - 1 } H _ { \xi _ { n } } ( \mathcal { X } _ { n } ) ) ^ { 2 } ] = n ^ { - 1 } E [ \xi _ { n } ( X _ { 1 } ; \mathcal { X } _ { n } ) ^ { 2 } ] + ( 1 - \frac { 1 } { n } ) E [ \xi _ { n } ( X _ { 1 } ; \mathcal { X } _ { n } ) \xi _ { n } ( X _ { 2 } ; \mathcal { X } _ { n } ) ] ,$$

and in the right hand side the first term tends to zero by the bounded p -th moments condition, while the second term tends to μ 2 by (3.12). Therefore E [ n - 1 H ξ n ( X n )] → μ and E [( n - 1 H ξ n ( X n )) 2 ] → μ 2 , so that n - 1 H ξ n ( X n ) tends to μ in mean square.

Finally we prove L 1 convergence, i.e. the case q = 1 of Theorem 2.1, completing the proof of that result.

Proposition 3.2 If ξ is almost surely stabilizing on P τ , with limit ξ ∞ ( P τ ) , for all τ ∈ (0 , ∞ ) and if ξ satisfies the moments condition (2.5) for some p &gt; 1 , then as n →∞ ,

$$n ^ { - 1 } H _ { \xi _ { n } } ( \mathcal { X } _ { n } ) \rightarrow \int _ { \mathbb { R } ^ { d } } E [ \xi _ { \infty } ( \mathcal { P } _ { f ( x ) } ) ] f ( x ) d x \quad \text {in} \ L ^ { 1 } .$$

Proof. Given K &gt; 0, define the functional

$$\xi ^ { K } ( x , \mathcal { X } ) \colon = \min ( \xi ( x ; \mathcal { X } ) , K ) .$$

Then by the stabilization condition for ξ , the truncated functional ξ K also stabilizes on P τ with limit ξ K ∞ ( P τ ) := min( ξ ∞ ( P τ ) , K ); we leave the reader to verify this assertion. Since ξ K is uniformly bounded, by Proposition 3.1 and the fact that L 2 convergence implies L 1 convergence, we have

$$n ^ { - 1 } H _ { \xi _ { n } ^ { K } } ( \mathcal { X } _ { n } ) \rightarrow \int _ { \mathbb { R } ^ { d } } E [ \xi _ { \infty } ^ { K } ( \mathcal { P } _ { f ( x ) } ) ] f ( x ) d x \quad \text {in} \ L ^ { 1 } .$$

Moreover,

$$0 \leq E [ n ^ { - 1 } H _ { \xi _ { n } } ( \mathcal { X } ) - n ^ { - 1 } H _ { \xi _ { n } ^ { K } } ( \mathcal { X } ) ] \\ = E [ \xi ( n ^ { 1 / d } X _ { 1 } ; n ^ { 1 / d } \mathcal { X } _ { n } ) - \xi ^ { K } ( n ^ { 1 / d } X _ { 1 } ; n ^ { 1 / d } \mathcal { X } _ { n } ) ]$$


<!-- p:22 -->


which tends to zero as K →∞ , uniformly in n , because the assumed moments condition (2.5), p &gt; 1, implies uniform integrability of the family of variables ξ ( n 1 /d X 1 ; n 1 /d X n ) , n ≥ 1. Also, by monotone convergence the right hand side of (3.14) converges to the right side of (3.13) as K →∞ . Combining these facts, and taking K to infinity in (3.14), we obtain (3.13).

We now work towards a proof of Theorem 2.2. First we show that stabilization of the graph G as defined in Section 2.1 implies an apparently stronger form of the stabilizing property.

Lemma 3.3 Suppose the graph G ( X ) is translation invariant and stabilizes on P 1 . Then with probability 1, for all points X ∈ P 1 , 0 there exists R ( X ) &lt; ∞ such that the set of edges of G ( P 1 , 0 ) incident to X is unchanged if points are added and/or deleted outside B ( 0 ; R ( X )) .

Proof. Let us say that a point x in a locally finite set X is unstable for G ( X ) if there does not exist r &gt; 0 such that

$$\mathcal { E } ( x ; G ( \mathcal { X } ) ) = \mathcal { E } ( x ; G ( \mathcal { X } \cap B ( 0 ; r ) ) \cup \mathcal { A } )$$

for almost all finite A ⊂ R d \ B ( 0 ; r ).

Let t &gt; 1. By translation-invariance and the fact that the Poisson point process is its own Palm distribution, the mean number of points of P 1 in B ( 0 ; t ) that are unstable for G ( P 1 ) is equal to

$$\int _ { B ( 0 ; t ) } P [ x \text { is unstable for } \mathcal { P } _ { 1 } \cup \{ x \} ] d x$$

which is zero by the assumption that G stabilizes on P 1 . Therefore, since t can be arbitrarily large, with probability 1 the Poisson process P 1 has no unstable points.

A further application of Palm theory for Poisson processes shows that the mean number of pairs of distinct points X,Y of P 1 in B ( 0 ; t ) such that Y is an unstable point of P 1 , is equal to

$$\int _ { B ( 0 ; t ) } \int _ { B ( 0 ; t ) } P [ y \text { is unstable for } \mathcal { P } _ { 1 } \cup \{ x , y \} ] d x d y$$

and since the mean number of such pairs is zero, the above integral is zero, and therefore for almost all x in B ( 0 ; t ),

$$L e b \ \{ y \in B ( 0 ; t ) \colon P [ y \text { is unstable for } \mathcal { P } _ { 1 } \cup \{ x , y \} ] \} > 0 \} = 0 . \quad ( 3 . 1 5 )$$

Choose x 0 in B ( 0 ; 1), such that (3.15) holds with x = x 0 . Then the set of z in B ( - x 0 ; t ) such that

$$P [ z \text { is unstable for } \mathcal { P } _ { 1 } \cup \{ 0 , z \} ] > 0$$

has zero measure. Integrating over z ∈ B ( - x 0 ; t ) and using Palm theory yet again, we find that the mean number of Poisson points X ∈ P 1 in B ( - x 0 ; t )


<!-- p:23 -->


such that X is unstable for G ( P 1 ∪{ 0 } ) is zero. Since t can be arbitrarily large, this gives us the result.

Proof of Theorem 2.2. To prove (2.10) let ξ ( x ; X ) be the reciprocal of the order of the component containing x in G ( X ). If the component containing the origin in G ( P 1 , 0 ) is finite then by stabilization of G (Lemma 3.3) there exists R such that alterations to P 1 outside B ( 0 ; R ) will not cause any change in this component. If the component containing the origin in G ( P 1 , 0 ) is infinite then given ε &gt; 0 we can find a connected subgraph of G ( P 1 , 0 ) of order greater than ε - 1 ; then by Lemma 3.3 there exists R such that alterations to P 1 outside B ( 0 ; R ) will not cause any removal of edges in this subgraph, and hence the functional ξ stabilizes on P 1 with limit σ - 1 G . By scale invariance ξ also stabilizes on P τ with limit having the same mean as σ - 1 G . Since ξ ( x ; X ) is uniformly bounded by 1, the moments condition (2.5) is trivially satisfied and by Theorem 2.1 we have (2.10).

To prove (2.11) let ξ ( x ; X ) be equal to 1 if G ( X ) contains a subgraph isomorphic to Γ with a vertex at x , and to zero if not. This is bounded by 1, and by Lemma 3.3 ξ stabilizes on P 1 with limit equal to 1 if E G occurs and equal to 0 if not. Also ξ stabilizes on P τ with limit having the same distribution, and Theorem 2.1 applies to yield (2.11).

To prove (2.13), observe that the functional L G φ ( X ) = ∑ e ∈ G ( X ) φ ( | e | ) has the representation L G φ ( X ) = L ξ ( X ) with

$$\xi ( x ; \mathcal { X } ) = \frac { 1 } { 2 } \sum _ { e \in \mathcal { E } ( x ; G ( \mathcal { X } ) ) } \phi ( | e | ) .$$

If G is scale invariant, then G ( P τ ) has the same distribution as G ( τ - 1 /d P 1 ) and therefore ξ stabilizes on P τ with

$$E [ \xi _ { \infty } ( \mathcal { P } _ { \tau } ) ] = \frac { 1 } { 2 } E \sum _ { e \in \mathcal { E } ( 0 ; G ( \mathcal { P } _ { 1 , 0 } ) ) } \phi ( \tau ^ { - 1 / d } | e | ) .$$

Then (2.13) follows from Theorem 2.1.
