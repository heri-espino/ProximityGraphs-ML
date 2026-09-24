---
id: "Teng_1998_Combinatorial-Geometric-Graphs"
source_pdf: "../pdf/Teng_1998_Combinatorial-Geometric-Graphs.pdf"
source_filename: "Teng_1998_Combinatorial-Geometric-Graphs.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "excellent"
extraction_score: 108.0
visual_assets: "disabled"
references_file: "../references/Teng_1998_Combinatorial-Geometric-Graphs.references.md"
---

<!-- p:1 -->

###### Abstract

As a special case of our main result, we show that for all L &gt; 0, each k-nearest neighbor graph in d dimensions excludes Kh as a depth L minor if h = Ω(Ld). More generally, we prove that the overlap graphs dhnto   trd ato  t ( st  t  i  ton of Plotkin, Rao and Smith (1994), our result implies that overlap graphs have "good" cut-covers, answering an open question of Kaklamanis, Krizanc and Rao (1993). Consequently, overlap graphs can be emulated on hypercube graphs with a constant factor of slow-down and on butterfly graphs with a factor of O(log* n) sow   ns e e s se ons son dueo dn stt r, n-on "well-conditioned" meshes and image processing on k-nearest neighbor graphs, can be performed on hypercubic parallel machines with a linear speed-up. Our result, in conjunction with a result of Plotkin, Rao and Smith, also yields a combinatorial proof that overlap graphs have separators of sublinear size. We also show that with high probability, the Delaunay diagram, the relative neighborhood graph, and the k-nearest neighbor graph of a random point set exclude Kh as a depth L minor if h = Ω(Ld/2 log n). © 1998 Elsevier Science B.V.

## 1. Introduction

Many applications, such as finite element and finite difference methods, image processing, and pattern recognition, use graphs that are defined geometrically [5,7,17,18,24,27]. These graphs usually satisfy certain geometric conditions [3,21,22,25,29]. Thus, we can study some combinatorial properties of these graphs via our knowledge in computational geometry in order to develop efficient algorithms.

Motivated by this observation, Miller et al. [17,18] proposed a class of geometric graphs, called overlap graphs. The class of overlap graphs has a simple geometrical definition (see Section 2). It contains all "well-conditioned" finite element and finite difference meshes in both two and three dimensions [17,18]. It also contains k-nearest neighbor graphs and planar graphs [19,27]. Using conformal mapping and analytical geometric arguments, Miller et al. [18] showed that a d-dimensional overlap

'Supported by an NSF CAREER award. Part of this work was done at Department of Mathematics and Lab. for Computer Science Massachusetts Institute of Technology, Cambridge, MA 02139, where the research was supported in part by AFOSR F49620-92-J-0125 and Darpa N00014-92-J-1799.

Computational Geometry 9 (8661) 277-287

## Combinatorial aspects of geometric graphs

Shang-Hua Teng

Department of Computer Science, University of Minnesota, Minneapolis, MN 55455, USA Received 4 December 1995; revised 29 March 1996


<!-- p:2 -->


graph has a separator of size O(n–1/d). Their result generalizes the planar separator theorem of Lipton and Tarjan [15] to geometric domains and has been used in parallel scientific computing [10,11] and parallel computational geometry [8,9,27]. Recently, Spielman and Teng [26] showed that the application of this geometric separator algorithm to planar graphs finds a separator of size 1.84√n, reducing the constant term in the Lipton-Tarjan's separator theorem. It is an interesting problem to find a combinatorial characterization of overlap graphs and a combinatorial proof to their small separator theorem.

In this paper, we show that overlap graphs exclude "shallow" minors. See Section 2 for the definition of the depth of a minor as introduced by Plotkin et al. [23]. In particular, we show that for all L, each overlap graph in d dimensions excludes Kh as a depth L minor for h = Ω(Ld). In conjunction with the construction in [23], this yields the first combinatorial proof of a weaker version of the small separator theorem for overlap graphs. An important consequence of our shallow minor result is that overlap graphs have "good" cut-covers, solving an open question of Kaklamanis et al. [12]. Consequently, this implies that overlap graphs can be emulated by hypercube graphs at a cost of a constant factor slow-down and by butterfly graphs with a factor of O(log* n) slow-down. Therefore, computations based on overlap graphs, such as finite element and finite difference methods and image processing on k-nearest neighbor graphs, can be performed on hypercubic parallel machine with a linear speed-up.

Our work is motivated by the result of Plotkin et al. [23] who introduced the concept of shallow minor and also showed that a special subclass of overlap graphs, the simplicial graphs with bounded aspect ratio in d dimensions (Miller and Thurston [20]), exclude Kh as a depth L minor when h = Ω(Ld). Our result generalizes their results to the class of all overlap graphs which includes k-nearest neighbor graphs.

We obtain a Mader-like result for overlap graphs. A classical result of Mader [6] states that if a graph G does not have a minor isomorphic to Kh, then no minor of G has average degree Ω(h log h). We show that for all L, any depth L minor of an overlap graph in d dimensions has average degree bounded from above by O(Ld).

We also consider some probabilistic properties of certain classes of random geometric graphs. We show that, with high probability, the Delaunay diagram, the relative neighborhood graph, and the k-nearest neighbor graph of a random point set excludes Kh as a depth L minor if h = Ω(Ld/2 log n).

## 2. Overlap graphs and shallow minors

s  -  p  o  {     . } =     on set, {B1, . . . , Bn }, of closed balls such that (1) Bi is centered at pi and (2) no point p ∈ Rd is strictly interior to more than k balls from B.

We will use the following notation. For each positive real α, if B is a ball of radius r in Rd, then α· B denotes the ball with the same center as B but radius αr.

Let Γ = {B1, . .. , Bn} be a k-ply neighborhood system. The intersection graph of Γ is the undirected graph with vertices V = {1, . . . , n} and edges E = {(Bi, Bj): (Bi ∩ Bj) ≠ 0}.

Let α ≥ 1. The α-overlap graph of Γ is the undirected graph with vertices V = {1, . . . , n} and edges


<!-- p:3 -->


$$E = \left \{ ( B _ { i } , B _ { j } ) \colon \left ( B _ { i } \cap ( \alpha \cdot B _ { j } ) \neq \emptyset \right ) \text { and } \left ( ( \alpha \cdot B _ { i } ) \cap B _ { j } \neq \emptyset \right ) \right \} .$$

Clearly, when α = 1, an overlap graph becomes the intersection graph of the k-ply neighborhood system.

We remark that overlap graphs include k-NNGs, well-shaped finite element and finite difference meshes, and planar graphs [18].

We now define the k-nearest neighbor graph [24]. Let P = {p1, . . . , pn} be a set of points in Rd. The nearest neighbor of pi is a point pj, j ≠ i, with minimum Euclidean distance from pi. To make the nearest neighbor unique, we choose the point pj with maximum index in case of ties and denoted it by nn(pi). Similarly, for any integer k &gt; 0, let nnk(pi) be the set of k nearest neighbors of pi in P (again, use indices to break ties). The k-nearest neighbor graph of P, denoted by k-NNG(P), is the directed graph (P, E) where E = {(pi, pj) | pj ∈ nnk(pi)}.

We now give the definition of shallow minors as introduced in [23]. Suppose G is an undirected graph. Let G1, G2,..., Gn be h disjoint connected subgraphs of G. The minor defined by G1, G2, . . . , Gh is a graph H whose vertex set is {1, . . . , h} and whose edge set contains exactly all those pairs (i, j): 1 ≤ i, j ≤ h such that there is an edge in G that connects a vertex of Gi to a vertex of Gj. Clearly, H can be obtained from a subgraph of G by contraction. The depth of such an H-minor is the maximum diameter of G1, . . . , Gh.

## 3. A combinatorial lemma of geometric graphs

In this section, we show that the intersection graph and the α-overlap graph of a k-ply neighborhood system exclude Kh as a depth L minor whenever h &gt; k(4L + 1)d and h &gt; k(4αL + 1)d, respectively.

### 3.1. Shallow minors of intersection graphs

First, we prove a geometric lemma about neighborhood systems.

Lemma 3.1. Suppose {B1, . . . , Bn} is a k-ply neighborhood system in Rd. For each d-dimensional ball B with radius r, for all constant β &gt; 0,

$$| \{ i \colon B _ { i } \cap B \neq \emptyset \, a n d \, r _ { i } \geqslant \beta r \} | \leqslant ( 1 + 2 \beta ) ^ { d } \beta ^ { - d } k ,$$

where ri is the radius of Bi.

Proof. Let p be the center of B. Let B′ = (1 + β) · B.

We distinguish two types of balls that intersect B. The first class contains those balls whose centers are in B' and the second class contains those whose centers are in the exterior of B'.

For the first class, we can shrink each ball to a concentric one of radius βr. The shrinking operation maintains the k-ply condition of the resulting neighborhood system. So, without loss of generality, we assume that all balls in the first class have radius βr.

Now, let Bi be a ball of the second class of radius ri and center pi. Let qi be the common point of the boundary of B′ and the line passing through ppi. Let B′ be a ball centered at qi of radius βr. Clearly B′ is completely contained in Bi because Bi intersects B. Replacing Bi by B′ still satisfies the k-ply condition. So, without loss of generality, we assume all balls of the second class have the properties that their centers are on the boundary of B' and their radii are equal to βr.


<!-- p:4 -->


Therefore, all balls that intersect B are completely contained in (1 + 2β) · B. Suppose there are m of them, by the volume bound we have

$$m v _ { d } ( \beta r ) ^ { d } \leqslant k v _ { d } ( 1 + 2 \beta ) ^ { d } r ^ { d } ,$$

where vd is the volume of a unit d-dimensional ball, implying m ≤ k(1 + 2β)d /βd. □

Theorem 3.2. Suppose Γ is a k-ply neighborhood system and G is the intersection graph of Γ. Then for all L, G excludes Kh as a depth L minor for h &gt; k(4L + 1)d.

Proof. Suppose G has a Kh minor of depth L. Then there are h sets of balls, I1, . . . , Ih ⊂ Γ such that

- (1) For each i, the intersection graph of Γi is connected and its diameter is at most L.
- (2) For each pair i, j, there is a ball in Γi that intersects a ball in Γj.

Now, let Bi be the ball in Γi of the largest radius. Without loss of generality, let B1 be the ball of the smallest radius among {B1, . . . , Bh }. Assume that the radius of B1 is r.

Because the diameter of the intersection graph of Γi is at most L and B1 is the ball of the largest radius of Γ1, all balls of Γ1 are completely contained in the ball B′ = (2L + 1) · B1.

Therefore, for all i &gt; 1, there is a ball from Γi that intersects B'.

We claim that for each i &gt; 1, there is a ball in Γi of radius at least r that intersects B′′ = (4L – 1)· B1. Here is the argument. Note first that the diameter of the intersection graph of Γ is at most L and there is a ball from Γi that intersects B'. If that ball has radius at least r, then we are done with Γ. If not, as we increase the radius of B' by 2r, we will include the ball completely and meet balls from the next level. We repeat the argument. We terminate in less than L + 1 iterations, since we must meet either Bi (which has radius of at least r) or some other balls in Γi that have radius at least r.

Notice that the radius of B′′ is (4L − 1)r. With β = 1/(4L − 1), using Lemma 3.1, we have h ≤ (1 + 2β)dβ−dk = (4L + 1)dk. □

### 3.2. Shallow minors of overlap graphs

Theorem 3.3. Suppose Γ is a k-ply neighborhood system and G is the α-overlap graph of Γ. Then for all L, G excludes Kh as a depth L minor for h = k(4αd L + 1)d.

Proof. The proof is similar to that of Theorem 3.2. Suppose G has a Kh minor with depth L. Then there are h sets of balls, Γ1 , . . . , Γh ⊂ Γ such that (1) for each i, the α-overlap graph of Γi is connected and its diameter is at most L, and (2) for each pair i, j, there exist Ui in Γi and Uj in Γj such that Ui ∩ (α · Uj) ≠∅ and (α · Ui) ∩Uj ≠∅.

Because the diameter of the α-overlap graph of Γi is at most L and B1 is the ball of the largest radius of Γ1, all balls of Γ1 are completely contained in the ball B′ = (2αL + 1) · B1.

Now, let Bi be the ball in Γi of the largest radius. Without loss of generality, let B1 be the ball of the smallest radius among {B1, . .. , Bh }. Assume that the radius of B1 is r.

Therefore, for all i &gt; 1, there is a ball Uj from Γi and a U ∈ Γ1 such that α · U intersects Uj. We claim that for each i &gt; 1, there is a ball in Γi of radius at least r that intersect B" (4αL - 1) · B1. The argument is very similar to that for the intersection graph.

=


<!-- p:5 -->


Notice that the radius of B′′ is (4αL − 1)r. With β = 1/(4αL – 1), using Lemma 3.1, we have h ≤ (1 + 2β)dβ−dk = (4αL)dk.

## 4. Random geometric graphs

In this section, we show that if P is a "random" point set of n points in d dimensions, then with probability approaching to 1, various types of geometric graphs, such as the Delaunay diagram, the k-nearest neighbor graph (k ≤ Θ(log n)), the α-overlap graph, and the relative neighborhood graph of P exclude Kh as a depth L minor when h = Ω((L)d/2 log n). Such result can also be generalized to random point sets on the surface of unit d-sphere in Rd+1.

Formally, we use the homogeneous Poisson point process of intensity one as our probabilistic model. This standard model is characterized by the property that the number of points in a region is a random variable that depends only on the d-dimensional volume of the region [4,13,16,28]. In this model,

- The probability of exactly k points appearing in any region of volume V is e−VVk/k!.
- The conditional distribution of points in any region given that exactly k points fall in the region is uniform.

We denote the probability of an event by Prob[ · ].

### 4.1. Shallow minors for uniform neighborhood systems

Let β ≥ 1 a constant. A k-ply {B1, . .. , Bn} is β-uniform if for all i, j, ri ≤ βrj, where ri is a radius of Bi for all 1 ≤ i ≤ n.

Lemma 4.1. Suppose Γ is a β-uniform k-ply neighborhood system and G is the intersection graph of Γ. Then for all L, G excludes Kh as a depth L minor for h &gt; k(4βL + 1)d/2.

Proof. Let Γ1 , . . . , Γh ⊂ Γ be defined as in the proof of Theorem 3.2.

We first note that there are at least Θ(h2/k) balls in the union of Γi's. This follows from the observation that the intersection graph of a k-neighborhood system of size n has at most O(kn) edges [27] and there are at least h2 edges in the intersection graph of I ∪.· ·∪Γh because they define a Kh-minor.

Then the argument is similar to that in the proof of Theorem 3.2. Let B be the smallest ball in p( + )         ∩     ( + )  s giving h ≤ O(kLd/2). □

Theorem 4.2. With high probability, for all L, a random k-NNG excludes Kh as a depth L minor for h = Ω(Ld/2 max(k, log n)).

The basic idea is to show that with high probability there is a constant β that the k-NNG of a random point set is a subgraph of the intersection graph of a β-uniform neighborhood system. We use is s o- os o o ao os e oms  o oos o Lemma 4.3. There are constants c, c1 &lt; c2 depending only on d such that with high probability (e.g., 1 – 1/n), the radius of all balls in a (clog n)-nearest neighbor graph of a random point set P is between c1(log1/d n) and c2(log1/dn).


<!-- p:6 -->


Proof. Teng and Yao [28] gave a proof of this lemma for d = 2. Their proof can be directly extended to higher dimension. For completeness, we present here such a high-dimension extension.

Let k = clog n for a constant c to be specified. Let vd be the volume of the unit d-dimensional ball. (t      dd     d l   (t  l  ) =  l the number of points of P contained in B(r). Let rk be the radius of k-nearest neighbor ball of p.

$$P r & > r ] = \text {Prob} [ | B ( r ) | < k ] = \text {e} ^ { - \lambda k } \sum _ { j < k } \frac { ( \lambda k ) ^ { j } } { j ! } . \\$$

If λ &gt; 1, then the terms in the summation strictly increase with j, hence

$$\text {Prob} [ r _ { k } > r ] < k e ^ { - \lambda k } \, \frac { ( \lambda k ) ^ { k } } { k ! } \leqslant k ( \lambda e ) ^ { k } e ^ { - \lambda k } = k ( \lambda e ^ { - ( \lambda - 1 ) } ) ^ { k } .$$

Therefore, there is a constant c2 such that Prob[rk &gt; c2 log1/d n] ≤ 1/n2. So with probability at least 1 – 1/n, the radius of all k-nearest neighbor ball is at most c2 log1/d n.

For a lower bound on rk, we have

$$\text {Prob} [ r _ { k } < r ] & = \text {Prob} \left [ \right ] B ( r ) | > k \right ] = e ^ { - \lambda k } \sum _ { j > k } \frac { ( \lambda k ) ^ { j } } { j ! } . \\$$

For λ &lt; 1, the terms in the summation decrease faster than a geometric series with ratio λ, hence

$$\text {Prob} [ r _ { k } < r ] \leqslant \frac { 1 } { 1 - \lambda } e ^ { - \lambda k } \, \frac { ( \lambda k ) ^ { k } } { k ! } \leqslant \frac { 1 } { 1 - \lambda } ( \lambda e ^ { 1 - \lambda } ) ^ { k } .$$

Therefore, there is a constant c1 such that Prob[rk &lt; c1 log1/d n] ≤ 1/n2. So with probability at least 1 — 1/n, the radius of all k-nearest neighbor ball is at least c1 log1/d n. □

In [28], Teng and Yao showed that with high probability, all edges in the Delaunay diagram of a random points are "short", and hence contained in the Θ(log n)-NNG. The following corollary is a direct consequence of Lemma 4.3.

Corollary 4.4. There exists a constant c depending only on d such that with high probability (e.g., 1 – 1/n), Delaunay diagram is a subgraph of the (clog n)-nearest neighbor graph of a set P of random points.

We now prove Theorem 4.2. We first note that the property of excluding shallow minor is closed under the subgraph operation.

Proof of Theorem 4.2. By Lemma 4.3, there exist a pair of constants c1 and c2 such that with high probability, the radii of ali k-nearest neighbor balls are between c1(log1/d n) and c2(log1/d n). This implies that with high probability, the resulting neighborhood system is β-uniform for β = c2/c1. The theorem then follows from Lemma 4.1.


<!-- p:7 -->


Corollary 4.5. With very high probability, for all L, the Delaunay diagram and the relative neighborhood graph of a random point exclude Kh as a depth L minor whenever h = Ω(Ld/2 log n).

Proof. It follows from Corollary 4.4 and Theorem 4.2.

## 5. Average degree of shallow minors in geometric graphs

A classical result of Mader [6] states: There is a constant c such that if a graph G does not have a       n  fo   n  s  e constant c.

What would be a Mader-like result for shallow minors? The first quess may be: If a graph G does not have a depth L minor isomorphic to the h-clique, then all depth L minors of G have average degree bounded from above by a polynomial in h and L. Unfortunately, this is not true. For example,2 take a complete n by n bipartite graph; clearly the average degree of this graph is n. But it does not have a depth 0 minor isomorphic to K3.

We now show that a "stronger version" of Mader-like result does exist for our geometric graphs.

Theorem 5.1. Suppose G is the intersection graph of a k-ply neighborhood system Γ in Rd and H is a depth L minor of G. Then the average degree of H is bounded from above by O(kLd).

Proof. Suppose H has m vertices {h1, .. . , hm}. Because H is a depth L minor of G, there are m disjoint subsets Γ1, ... , Γm of I that define H where Γi corresponds to hi. Let Bi be the ball of the largest radius of Γi. Let ri be the radius of Bi. Without loss of generality, we assume that r1 ≤ r2 ≤ ·.. ≤ rm. Direct each edge of H from its lower indexed vertex to its higher indexed vertex. We claim that the outdegree of the resulting directed graph is bounded by O(kLd). The theorem then follows. The proof to the claim above is similar to that of Theorem 3.2.

Similarly, we have Theorem 5.2.

Theorem 5.2. Suppose G is the α-overlap graph of a k-ply neighborhood system in Rd and H is a depth L minor of G. Then the average degree of H is bounded from above by O(k(αL)d).

Using a similar argument, we can also show that, with very high probability, for all L, the average degree of any depth L minor of a random k-NNG is bounded above by O(Ld/2 max(k, log n)). Moreover, the Delaunay diagram and the relative neighborhood graph of a random set of points in Rd have no depth L minor of average degree more than Ω(Ld/2 log n).

## 6. Applications

Our shallow minor results make it possible to apply some known combinatorial construction to overlap graphs. In particular, we can use the algorithm of Plotkin et al. [23] to decompose overlap graphs and k-NNGs for a linear or almost linear speed-up emulation of overlap graphs on hypercubes and butterflies, respectively. Such emulations can be used to design efficient parallel finite element and finite difference algorithms and parallel computational geometry algorithms for k-NNG related problems.

2 Given by Yuan Ma of Department of Mathematics, MIT.


<!-- p:8 -->


### 6.1. Cut-cover for overlap graphs and k-NNG

Suppose G = (V, E, w) is a node weighted undirected graph where w is the weight function. For each vertex u ∈ V let Nt(u) be the set of all vertices in V that are within (combinatorial) distance t from u. A t-neighborhood cover of G, as defined by Awerbuch and Peleg [1] is a set of (possible overlapping) subsets {S1, . .. , Sk } of G such that for all u ∈ V, there exists an i, such that Nt(u) ⊆ Si.

Suppose C ⊆ V is a subset of V, by G/C we denote the graph (V − C, E ∩ (V − C) × (V − C)).

The balanced cut-cover, defined by Kaklamanis et al. [12], combines the notion of t-neighborhood covers and small separators. Formally, for 0 &lt; β &lt; 1, s,t, ε ∈ R+, a β-balanced (t, s,ε) cut-cover of G is a set C ⊆ V and a t-neighborhood cover {S1,...,Si} of G/C such that

- (1) |C| ≤ s;
- (3) maxi=1 w(Si) ≤ βw(V).
- (2) Σi=1 ω(Si) ≤ (1 + ε)w(V); and

A q-color β-balanced (t, s, ε) cut-cover of an n node graph G = (V, E) where nodes are colored with q colors is a set C and a t-neighborhood cover {S1, . . . , St } of G/C that is a β-balanced (t, s, ε) cut-cover of G for every weight function defined by an indicator function for the q colors of G, ignoring other colors.

Kaklamanis, Krizanc and Rao showed that planar graphs and graphs with bounded forbidden minors have good cut-covers and posed an open question of whether intersection graphs and overlap graphs ao-ad,, rs.

The following theorem follows from Theorem 3.3 and the construction of Plotkin et al. [23]. The time complexity for finding such a cut-cover is O(kαdn2/L).

Theorem 6.1. Suppose G = (V, E) is an α-overlap graph of a k-neighborhood system in Rd. Then for all integers q, t and L &gt; 2qt, and q coloring functions on G, there is a set C ⊂ V and a t-neighborhood cover {S1, . . . , Sl} such that

$$t \text {-neighborhood cover} \ \{ S _ { 1 } , \dots , S _ { l } \} \ s u c h \ t h e r \\ | C | = O ( q ^ { 2 } \alpha ^ { d - 1 } k L ^ { 2 d - 1 } \log n ) , \\ \sum _ { i = 1 } ^ { l } w ( S _ { i } ) \leqslant ( 1 + 2 q t / L ) w ( V ) , \\ \max _ { i = 1 } ^ { l } w ( S _ { i } ) \leqslant ( 2 / 3 ) w ( V ) , \\ \text {with respect to each of the a colors function}$$

with respect to each of the q colors function w ignoring the other q – 1 colors.


<!-- p:9 -->


### 6.2. Fast emulations in hypercubes and butterflies

Our result that overlap graphs have "good" cut-cover yields an immediately application to parallel computation on hypercubic and butterfly networks, thanks to the result of Kaklamanis et al. [12].

Theorem 6.2. Bounded degree α-overlap graphs can be emulated on hypercube graphs with a constant factor slow down and on butterfly graphs with a factor of O(log* n) slow down.

The emulation result can be applied to parallel finite element and finite difference computations and computational geometry problems that use k-NNGs.

For example, a natural condition for well-shaped meshes for the adaptive finite difference method is the density of the embedding [2,21]. Let G be an undirected graph and let π be an embedding of its nodes in Rd. We say π is an embedding of density α if the following inequality holds for all vertices v in G. Let u be the closest node to v. Let w be the farthest node from v that is connected to v by an edge. Then

$$\frac { \| \pi ( w ) - \pi ( v ) \| } { \| \pi ( u ) - \pi ( v ) \| } \leqslant \alpha .$$

In general, G is an α-density graph in Rd if there exists an embedding of G in Rd with density α. It can be easily shown that there is a ∆(α,d) depending only on α and d such that the maximum degree of an α-density graph is bounded by ∆(α, d).

Corollary 6.3. Density graphs and k-NNGs can be emulated on hypercube graphs with a factor of constant slow down and on butterfly graphs with a factor of O(log* n) slow down. Therefore, iterative methods for solving a finite difference system of a PDE (on a well-conditioned adaptive mesh) can be performed on a hypercubic parallel machine with a linear speed-up.

Recently, Leiserson et al. [14] showed that "good" cut-cover implies better out-of-core algorithms for iterative relaxation algorithms on the graphs. Our results can be used to extend their tools for solving adaptive finite difference systems.

## 7. Final remarks and open questions

In this paper, we show that certain classes of geometric graphs have some common combinatorial properties. Our results, to a certain degree, complement the work of Miller et al. [17,18] which can be viewed as an attempt to find a geometric characterization for a combinatorial property, namely, the existence of small separators. This paper tries, in some sense, to understand the combinatorial aspects of geometric graphs. The goal of such an understanding is for

- applying combinatorial construction to geometric graphs, and ·
- designing efficient combinatorial algorithms using our knowledge from (computational) geometry.

An open question is whether the Ω(Ld) bound can be reduced to Ω(Ld/2). We notice that by amortizing the steps and volume, we are able to reduce the exponent of L from d to d – 1. We conclude the paper by giving a simple argument to reduce the exponent of L from d to d – 0.5.


<!-- p:10 -->


In the proof of Theorem 3.2, we showed that for each i &gt; 1, there is a ball B in Γi of radius at least r that intersects B". We divide B′ into two classes: C1 contains balls which are less than D = L(d–0.5)/dr away from the center of B′′; C2 contains all other balls. By volume argument, there are at most O(Ld-0.5) number of balls in C1. We now show that the number of balls in Č2 is bounded by O(Ld-0.5). The distance between B′ and the center of B′′ is at least D, and at most 2L balls connecting B1 to B. The total volume of these ball is at least L0.5. Therefore, by volume argument, there are at most O(Ld/L0.5) balls in C2. Fine tuning this argument further reduces the exponent to d – 1. However, we conjecture that the correct value of the exponent is d/2.

##### Acknowledgments

I would like to thank Satish Rao for introducing me to the notion of shallow minors and his invaluable help. I thank Yuan Ma for his counterexample of Section 5, Dan Spielman for helpful discussion, and Frances Yao for all that I have learnt about random geometric graphs.
