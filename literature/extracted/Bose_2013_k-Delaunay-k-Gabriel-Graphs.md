---
id: "Bose_2013_k-Delaunay-k-Gabriel-Graphs"
source_pdf: "../pdf/Bose_2013_k-Delaunay-k-Gabriel-Graphs.pdf"
source_filename: "Bose_2013_k-Delaunay-k-Gabriel-Graphs.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "full-page-ocr"
extraction_quality: "excellent"
extraction_score: 98.0
visual_assets: "disabled"
references_file: "../references/Bose_2013_k-Delaunay-k-Gabriel-Graphs.references.md"
---

<!-- p:1 -->

ELSEVIER

Contents lists available at SciVerse ScienceDirect

## Computational Geometry: Theory and Applications

www.elsevier.com/locate/comgeo

## sors -rk e -  sordk hs

Prosenjit Bose a, Sébastien Collette b,1,2, Ferran Hurtado c,3,4 Matias Korman c,4,5 b,1,6, Vera Sacristán c,3,4, Maria Saumelld,*,3,7 Stefan Langerman

a School of Computer Science, Carleton University, Ottawa, Canada

Departament de Matemàtica Aplicada II, Universitat Politècnica de Catalunya, Barcelona, Spain

b Computer Science Department, Université Libre de Bruxelles, Brussels, Belgium

d Department of Applied Mathematics, Charles University, Prague, Czech Republic

## ARTICLE INFO

###### A BST R ACT

Article history:

Received 30 January 2011 Accepted 26 April 2012 Available online 30 April 2012 Communicated by Stephane Durocher

Keywords:

Proximity graphs Geometric graphs

## 1. Introduction

Let S be a set of n points in the plane in general position (no three are collinear and no four are concyclic). A proximity graph on S is a geometric graph where two points are adjacent if they satisfy some specific proximity criterion. Proximity graphs have been widely studied due to their theoretical interest and to their applications in situations where it is necessary to extract the "shape" of a set of points (see [16] for a survey).

Adjacency in many proximity graphs is defined in terms of an empty region associated to any pair of points. To provide more flexibility the definition of the graphs can be relaxed to allow up to k points to lie in the neighborhood region. This gives rise to higher order proximity graphs. In this paper we deal with two such graphs.

We consider the k-Delaunay graph of S (denoted k-DG(S)), where a straight-line segment connects points pi, pj ∈ S if there exists a circle C(pi, pj) through pi and pj with at most k points of S in its interior. The standard Delaunay triangulation corresponds to 0-DG(S) and will be denoted by DT(S).

* Corresponding author.

E-mail addresses: jit@scs.carleton.ca (P. Bose), secollet@ulb.ac.be (S. Collette), ferran.hurtado@upc.edu (F. Hurtado), matias.korman@upc.edu (M. Korman),

slanger@ulb.ac.be (S. Langerman), vera.sacristan@upc.edu (V. Sacristán), maria.saumell.m@gmail.com (M. Saumell).

Supported by A.R.C. and F.N.R.S.

Chargé de recherches du F.R.S.-FNRS.

3 Partially supported by projects MTM2009-07242 and Gen. Cat. DGR 2009SGR1040.

4 Partially supported by the ESF EUROCORES programme EuroGIGA, CRP ComPoSe: MICINN Project EUI-EURC-2011-4306, for Spain.

Supported by the Secretary for Universities and Research of the Ministry of Economy and Knowledge of the Government of Catalonia and the European

6 Maître de recherches du F.R.S.-FNRS.

Union.

Supported by GraDR EUROGIGA project No. GIG/11/E023.

We consider two classes of higher order proximity graphs defined on a set of points in the plane, namely, the k-Delaunay graph and the k-Gabriel graph. We give bounds on the following combinatorial and geometric properties of these graphs: spanning ratio, diameter, connectivity, chromatic number, and minimum number of layers necessary to partition the edges of the graphs so that no two edges of the same layer cross.

Computational

Cery

©2012 Elsevier B.V. All rights reserved.


<!-- p:2 -->


Table 1 Worst-case possible values for the studied properties. SR, D, κ, X, and θc denote the spanning ratio, diameter, connectivity, chromatic number, and constrained geometric thickness, respectively. The results hold for specific ranges of k; see the complete statements throughout the paper.

| Gabriel graphs                                                                                                                                                                                                                                                                                                             | Delaunay graphs                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Θ( √ n k ) ⩽ max &#124; S &#124;= n SR ( k - GG ( S )) ∈ O ( √ n ) ⌈ n - 1 k + 1 ⌉ ⩽ max &#124; S &#124;= n D ( k - GG ( S )) ⩽ n - 2 k + 1 + 1 min &#124; S &#124;= n k ( k - GG ( S )) = k + 1 3 ( k + 1 ) ⩽ max &#124; S &#124;= n χ( k - GG ( S )) ⩽ 6 ( k + 1 3 ⩽ max &#124; S &#124;= n θ c ( 1- GG ( S )) ⩽ 4 3 k 2 | 1 . 5931 ⩽ max &#124; S &#124;= n SR ( k - DG ( S )) ⩽ 1 . 998 ⌊ n 2 ( k + 1 ) ⌋ ⩽ max &#124; S &#124;= n D ( k - DG ( S )) ⩽ n - 2 2 ( k + 1 ) min &#124; S &#124;= n k ( k - DG ( S )) = 2 ( k + 1 ) |
|                                                                                                                                                                                                                                                                                                                            | + 1                                                                                                                                                                                                    |
| )                                                                                                                                                                                                                                                                                                                          | 4 ( k + 1 ) ⩽ max &#124; S &#124;= n χ( k - DG ( S )) ⩽ 6 ( k + 1 )                                                                                                                                    |
|                                                                                                                                                                                                                                                                                                                            | 3 ⩽ max &#124; S &#124;= n θ c ( 1- DG ( S )) ⩽ 4                                                                                                                                                      |
| 2 ⩽ max S n θ c ( k - GG ( S )) ⩽ 18 k 3 k                                                                                                                                                                                                                                                                                 | 3 k 2 ⩽ max S n θ c ( k - DG ( S )) ⩽ 18 k 2 3 k                                                                                                                                                       |

W    sk s ts -t  ei (      - t s o s if the closed disk centered at the midpoint of the segment pipj with both pi and pj on its boundary contains at most k points from S different from pi, p j. The standard Gabriel graph corresponds to 0-GG(S) and will be denoted by GG(S).

The combinatorial and geometric properties of these graphs have been widely studied for the case k = 0 (see [16]). Howe    n   ns         n    w  o ed in O (k2n logn) time, and that the k-Gabriel graph can be used to obtain fast algorithms for the Euclidean bottleneck biconnected edge subgraph problem and for the Euclidean bottleneck matching problem. The structure of the set of triangulations -thn n  n  s  s    s  -   s    m u ber of edges of this graph, and a use of k-DG(S) in a coloring problem with applications to cellular networks. Finally, the number of crossings in these graphs is discussed in [3].

In this paper we investigate other properties of these graphs. The first property we consider is the spanning ratio, a parameter capturing to what extent traveling along a graph is much longer compared to traveling along the plane (the formal definition is given below). Our goal is to study the relationship between k and the spanning ratio. For k = 0, the spanning ratio of several proximity graphs has been studied in the literature. In particular, it has been shown the spanning ratio of the Gabriel graph might be as bad as Θ(√n) [6]. On the other hand, it is known that the spanning ratio of the Delaunay triangulation of any set of points in the plane is constant, but determining the exact value of the spanning ratio of this graph remains a challenging open problem [7,11,17,24,25].

We also study three graph theoretical properties of k-DG(S) and k-GG(S). These properties are the diameter, which can be seen as a combinatorial counterpart to the spanning ratio, the connectivity and the chromatic number. In the three cases the bounds we provide are tight (up to multiplicative constants).

Finally, we deal with a variation of the notion of geometric thickness. The geometric thickness of a graph G is the mino s            -  s  t s s G into layers such that no two edges of the same layer cross. The study of the geometric thickness finds applications in problems such as representing nonplanar graphs so that their complexity is minimized, or designing printed circuit boards, where connections that cross must lie in distinct layers [10]. In some cases one might not have the freedom of choosing the drawing of the graph because it is fixed or forced to satisfy additional restrictions. This motivates the use of a distinct parameter defined as follows. The constrained geometric thickness of a geometric graph G (i.e., a fixed straight-line drawing of a graph in the plane) is the smallest number of layers necessary to partition the edges of G into layers in such a way that no two edges of the same layer cross. The concept of constrained geometric thickness has appeared before in the literature, and in particular it is known that it can be tested in O(n logn) time whether the constrained geometric thickness of a geometric graph is 2 [12]. In this reference the constrained geometric thickness of a geometric graph is called "thickness of a drawing of a graph", but in the current paper we prefer to use our notation because we see the proximity graphs not as abstract graphs, but as geometric graphs.

We give bounds on the constrained geometric thickness of the graphs k-DG(S) and k-GG(S). Notice that the algorithmic question of testing whether the constrained geometric thickness of a geometric graph is at most some given value k, for k &gt; 2, is NP-complete [12]. The fact that, when it comes to the constrained geometric thickness, the embedding of the graph is fixed appears to be a natural restriction when dealing with these graphs, since in this case the position of the vertices and the adjacencies have a geometric meaning that is not preserved if vertices are allowed to move around.

From a theoretical point of view, determining the constrained geometric thickness of k-DG(S) and k-GG(S) is a particular ca   r    :(     se  ned a    at most λ pairwise crossing edges, can the edges of G be colored with f (λ) colors such that crossing edges receive distinct cl      ss   s  s  s  t        ¿ pairwise crossing edges and we give a quadratic upper bound on the number of colors required.

From a more practical point of view, DT(S) and GG(S) satisfy some properties that make them interesting in the context of routing in wireless networks [8,19]. Finding ways to extract plane layers from k-DG(S) or k-GG(S) may have applications in this setting.

### Our results are summarized in Table 1.

For all k ≥ 0, the following relations hold: (i) k-DG(S) ⊆ (k + 1)-DG(S), (ii) k-GG(S) ⊆ (k + 1)-GG(S), (iii) k-GG(S) ⊆ k-DG(S).


<!-- p:3 -->


## 2. Spanning ratio

Let G be a geometric graph on S and P = {p1p2··· pl} be a path in G. We define the geometric length of P as ∑-1 ∑i=1 |pipi+1|, where |pipj| is the Euclidean distance between pi and pj. The geometric distance between points pi, p j ∈ S, denoted by dg(pi, pj), is the minimum over the geometric length of all paths in G connecting pi and p j. The spanning ratio of G is defined as

$$S R ( G ) = \max _ { p _ { i } \neq p _ { j } \in S } \frac { d _ { g } ( p _ { i } , p _ { j } ) } { | p _ { i } p _ { j } | } .$$

The spanning ratio of DT(S) is not greater than 1.998 [24]. Since k-DG(S) is a supergraph of DT(S), we have:

Corollary 1. For any set S of n points in the plane, SR(k-DG(S)) ≤ 1.998.

The number of edges of k-Delaunay graphs grows with k. Consequently, it would be reasonable to believe that the spas      a  r s  s    a   s naws somehow the opposite, i.e., that in the worst case the spanning ratio of k-DG is not smaller than the spanning ratio of the Delaunay triangulation.

hnns     n     &lt;  n   u +    n    n  t      s n   ch that SR(k-DG(S')) ≥ SR(DT(S)) − ε.

Proof. Consider the Delaunay triangulation of S. Since S is in general position, the combinatorial structure of the graph does not change when moving each point in S at most ε', for sufficiently small values of ε' &gt; 0. The supremum of the values of ε'satisfying this property is called the tolerance of DT(S) and is denoted by tol(DT(S)) [2].

Let i, j be a pair of indices such that

$$S R ( D T ( S ) ) = \frac { d _ { g } ( p _ { i } , p _ { j } ) } { | p _ { i } p _ { j } | } .$$

Given ε &gt; 0, for each pl ∈ S, define pl,0 = pl and place k new points pl,1, Pl,2, . . . , pl,k at distance from pl,0 less than ε′ = min{tol(DT(S)), |pipj|ε } and in general position. If n' &gt; (k + 1)n, add extra points far from the set S. Let S′ be the 2(k+1)n resulting set of points. In the following lines we prove that SR(k-DG(S')) is almost as large as SR(DT(S)).

Suppose that pl and pm are not adjacent in DT(S), and let ν, t be two integers such that 0 ≤ ν, t ≤ k. We next argue that, in this case, pl,v and pm,t are not adjacent in k-DG(S'). Consider a circle C through pl,v and pm,t. We want to see that C contains at least k + 1 points of S' in its interior. In the Delaunay triangulation of the set of points formed by pl,v and pm,t, together with {pr,o}r≠l,m, the points pl,v and pm,t are not connected, since this triangulation has the same combinatorial structure as DT(S) by the choice of ε'. Hence, C contains at least one point of the group {pr,0}r≠l,m. Analogously, C contains at least one point of the group {pr,τ }r≠l,m for all τ ∈ {1, . .. , k}. Consequently, C contains at least k + 1 points of S′ in its interior.

Let Plo, v0 = Pi,0, Plh, vh = p j,0, and Plo, v0 l1, v1 · Plh, νh be the shortest path from pi,0 to pj,0 in k-DG(S'). By the triangle inequality, |plr,νr Plr+1,vr+1| ≥ |plr Plr+1| − 2ε′, for any r ≤ h − 1. Therefore, in k-DG(S′),

$$d _ { g } ( p _ { i , 0 } , p _ { j , 0 } ) & = | p _ { l _ { 0 } , v _ { 0 } } p _ { l _ { 1 } , v _ { 1 } } | + | p _ { l _ { 1 } , v _ { 1 } } p _ { l _ { 2 } , v _ { 2 } } | + \dots + | p _ { l _ { h - 1 } , v _ { h - 1 } } p _ { l _ { h } , v _ { h } } | \\ & \geqslant | p _ { l _ { 0 } } p _ { l _ { 1 } } | + | p _ { l _ { 1 } } p _ { l _ { 2 } } | + \dots + | p _ { l _ { h - 1 } } p _ { l _ { h } } | - 2 \varepsilon ^ { \prime } h .$$

Notice that h ≤ (k + 1)n. Let r ∈ {0, 1, . . ., h − 1}. Since plr, vr Plr+1, r+1 is an edge of k-DG(S'), we have that either pl, = Plr+1 or Pl Plr+1 is an edge of DT(S). Therefore pl0 Pl1 Pl2 · ·· Plh\_1Plh is a walk in DT(S) connecting pi to pj. Thus |pl0 Pl1| + |pl1 Pl2| + · · + |plh−1 Plh| ≥ dg (pi, p j). Combining these facts,

$$d _ { g } ( p _ { i , 0 } , p _ { j , 0 } ) & \geqslant d _ { g } ( p _ { i } , p _ { j } ) - 2 \varepsilon ^ { \prime } ( k + 1 ) n \geqslant d _ { g } ( p _ { i } , p _ { j } ) - | p _ { i } p _ { j } | \varepsilon . \\ \text {Finally,}$$

$$S R ( k { \text {-DG} } ( S ^ { \prime } ) ) \geqslant \frac { d _ { g } ( p _ { i , 0 } , p _ { j , 0 } ) } { | p _ { i , 0 } p _ { j , 0 } | } \geqslant S R ( D T ( S ) ) - \varepsilon . \quad \Box$$

Corollary 2. For any k ≥ 1 and any sufficiently large value of n, there exist sets of n points in the plane whose k-Delaunay graphs have spanning ratio larger than 1.5931.


<!-- p:4 -->


Fig. 1. Left: Gabriel graph tower construction of 8 points. Right: A sequential triangulation.

Proof. It suffices to consider the Delaunay triangulation described in [25] having spanning ratio at least 1.5932. Then we apply Theorem 1 with ε = 10−4. □

If k ≥ n/2 – 1, the graph k-DG(S) is the complete graph, so it has spanning ratio 1. If k is just one unit smaller, the spanning ratio of k-DG(S) might be almost √2:

Remark 1. For any n ≥ 5 and ε &gt; 0, there exist sets of n points in the plane whose (lμ」 – 2)-Delaunay graphs have spanning ratio larger than √2 — ε.

Such a point set S can be constructed by placing two points p1 and p2 at distance 2, and two groups of [n/2] – 1 and [n/2] – 1 points at distinct sides of the segment p1p2 such that all points q in these groups are at distance approximately √2 from both p1 and p2, and satisfy ∠p1qp2 &gt; π/2. The points p1 and p2 are not adjacent in (ln」 − 2)-DG(S). Let us finally consider k-Gabriel graphs. The situation in this case is different because for k = o(n) these graphs do not

have constant spanning ratio:

Theorem 2. For any set S of n points in the plane and k ≤ n — 2, the spanning ratio of k-GG(S) is O (√n). There exist sets of n points in the plane whose k-Gabriel graphs have spanning ratio Θ(k).

rie es -   or  ot  s rds ot ats rs  s   o  o  o os at most

As for the second part, consider the Gabriel graph tower construction in [6] with [k+1 n 1 points, which has spanning ratio Θ(k). (See Fig. 1, left.) Notice that all non-Gabriel edges are precluded by points lying in the interior of the closed disks associated to these edges. Consequently, for sufficiently small values of ε'&gt; 0, each point can be moved at most ε' without changing the combinatorial structure of the graph. Now, proceeding as in the proof of Theorem 1, we obtain a point set whose k-Gabriel graph has spanning ratio Θ(√k). □

## 3. Diameter and connectivity

We define the combinatorial length of a path P on a geometric graph G as the number of its edges. The combinatorial distance between points pi, pj ∈ S, denoted by dc(pi, pj), is the minimum over the combinatorial length of all paths in G connecting pi and pj. The diameter of G, denoted by D(G), is defined as the maximum over the combinatorial distance of all pairs of points in S.

The connectivity κ(G) of a graph G = (V, E) is the size of the smallest subset V′⊆ V such that the induced subgraph G[V \ V′] is disconnected.

In this section we determine the diameter and the connectivity of the k-Delaunay graph and the k-Gabriel graph. For any graph, these parameters are related in the following way:

Lemma 1. (See [23].) If G is a graph on n vertices with connectivity κ(G) ≥ 1 and diameter D(G) ≥ 1, then n ≥ κ(G)(D(G) − 1) − 2.

We derive lower bounds for the connectivity of k-DG(S) and k-GG(S). Combining these bounds with Lemma 1, we obtain upper bounds for the diameter of these graphs. We start with k-Delaunay graphs.

Thd         ( +   -  - n   n  t e d    s    ane hh  y  y   s Proof. Let S' be a minimal subset of S such that k-DG(S) \ S' is disconnected. Let S1, ..., Sm be the vertex sets of the connected components of k-DG(S) \ S′. If m = 1, then k-DG(S) is the complete graph and κ(k-DG(S)) = n − 1 ≥ 2(k + 1), for k ≤ [n/2] – 2. Otherwise we distinguish two cases.


<!-- p:5 -->


Fig. 2. The two cases in the proof of Theorem 3.

l

C1

CH(S2)

rj


C1

rl

qi

●

C2

qt

●

qi

CH(S1)

qi

We first consider the case where m = 2 and the two components can be separated by a horizontal line. We denote by q1, q2, ... the vertices in S1 and by r1, r2, ... the vertices in S2. Suppose that the common tangent l of CH(S1) and CH(S2) leaving these polygons to its right passes through qi and rj. (See Fig. 2, left.) Then there exists a circle C1 through qi and rj that does not contain any point from S to the right of the segment qrj. Since qi and rj belong to distinct components of k-DG(S) \ S′, (qi, rj) is not an edge of either k-DG(S) \ S′ or k-DG(S). Therefore every circle through qi and rj contains at least k + 1 points of S in its interior. In particular, C1 contains k + 1 such points, none of which can be in S \ S' by construction. Hence C1 contains k + 1 points of S′, and all of these points are to the left of l. If S1 = {qi} and S2 = {rj}, w h  ot   ot     t  ot s  t       h  hs circle contains at least k + 1 points of S', and these points are different from the ones in C1 because they are to the right of l. Thus |S'| ≥ 2(k + 1). Otherwise we can assume that |S2| ≥ 2, and we consider a circle C2 tangent to l at qi growing towards the right of l until it contains a point r on its boundary. If C2 does not contain any point from S1 in its interior, we define C2 = C2. Otherwise, let C2 be the largest circle tangent to C2 at ri not containing any point from S1 in its interior. Notice that C2 does not contain any point from S2 in its interior and contains some point qt on its boundary. Since r and qt belong to distinct components of k-DG(S) \ S′, C2 contains at least k + 1 points of S'. These points are distinct from the points in C1 because they are to the right of l, which yields that |S′| ≥ 2(k + 1).

In the second case there exists a vertex qi ∈ S \ S' such that each of the two open half-spaces separated by the horizontal io   o  o   t n  \  o  o t   t oos of generality, we assume qi ∈ S1. Let C1 be the smallest circle that has qi at the south pole and includes a point rj of a dins         d '  i     \ (    in C1 keeping the tangency on rj until it contains exactly one point qι ∈ U1. Let C1 be the circle we obtain. Since the vertices rj and qi belong to distinct components, C′ contains at least k + 1 points from S'. By repeating the same idea with circles that have qi as the north pole we obtain a circle C2 containing at least k + 1 points from S', and whose interior is disjoint from the interior of C1. Therefore, |S′| ≥ 2(k + 1).

It remains to prove the second part of the claim. We consider a set of sequential triangulation. A sequential triangulation can be constructed iteratively as follows: p1, p2, and p3 form a triangle and, for i ≥ 4, pi is adjacent to pi–1 and pi-2 (see Fig. 1, right for an example). These triangulations can be disconnected by removing two points. As in Theorem 1, each point (except possibly one) can be replaced by k + 1 points so that, in the k-Delaunay graph of the new point set, any two points can only be adjacent if they belong to the same cluster or their original points were adjacent. The k-Delaunay graph of this point set has connectivity at most 2(k + 1), because it can be disconnected by removing two clusters of k + 1 points corresponding to two points whose removal disconnects the original sequential triangulation. By the first part of the theorem, the connectivity of this k-Delaunay graph is exactly 2(k + 1).

Corollary 3. Let S be a set of n points in the plane and k ≤ [n/2] − 2. Then D(k-DG(S)) ≤ n-2 + 1. There exist sets of n points in 2(k+1) the plane whose k-Delaunay graphs have diameter greater than or equal to  2(k+1]. n

Po o o  n ot e s t    t    o     omna

In general, the k-Gabriel graph has fewer edges than the k-Delaunay graph, so its connectivity is usually smaller:

Theorem 4. For any set S of n points in the plane and k ≤ n — 2, κ(k-GG(S)) ≥ k + 1. There exist sets of n points in the plane whose k-Gabriel graphs have connectivity k + 1.


<!-- p:6 -->


Proof. Let S′ be a minimal subset of S with the property that k-GG(S) \ S′ is disconnected. If |S′| = n — 1, then k-GG(S) is the complete graph and κ(k-GG(S)) = n − 1 ≥ k + 1, for k ≤ n − 2. Otherwise, k-GG(S) \ S′ contains at least two connected components; let pi and pj be the pair of vertices at disjoint components of k-GG(S) \ S′ such that their distance in the plane is minimal. That is, any other pair of vertices pl, pm ∈ S \ S' such that |pipm| &lt; |pipj| are in the same connected component of k-GG(S) \ S′.

Finally, we describe a point set showing that this bound is tight. Let S = {p1, ... , pn} be a set of n points sorted by x coordinate in an infinitesimally perturbed horizontal line. Then k-GG(S) contains the edge (pi, pj) if and only if |i — j| ≤ k + 1. Thus removing p2, p3, . . . , Pk+2 disconnects p1 from the rest of the graph. □

Since pi and pj belong to distinct components of k-GG(S) \ S′, the edge (pi, pj) is not present in k-GG(S). Therefore, the closed disk centered at the midpoint of the segment pipj with both pi and pj on its boundary contains at least k + 1 points from S different from pi, pj. Let pι be one of these points; notice that pl does not belong to S \ S': otherwise we would have a contradiction with the definition of pi and pj (since both |pipi| &lt; |pipj| and |pipj| &lt; |pipj| hold, and pl a +   l n      t n   ost.

Corollary 4. For any set S of n points in the plane and k ≤ n − 2, D(k-GG(S)) ≤ n−2 + 1. There exist sets of n points in the plane k+1

Proof. The upper bound follows from Theorem 4 and Lemma 1. As for the second part of the statement, in the example of Theorem 4, dc(p1, pn) = [k+11

## 4. Chromatic number

A j-coloring of a graph G = (V, E) is a mapping f : V → {1, 2, . . . , j} such that f (v) ≠ f (w) for every edge (ν, w) of G. The chromatic number of G, denoted by X (G), is the minimum j such that G is j-colorable.

+   (- )  (-   -       n d    s    1)

P r      + ( +  -  +   o  (r    t  na vertex of degree at most 6k + 5. Observe that, if (pi, pj) is an edge of k-DG(S), this edge is also present in k-DG(S  {pt}) for any pl ∈ S (pι ≠ pi, pj). Thus, if k-DG(S)  S′ is an induced subgraph of k-DG(S) on n' vertices, then it is a subgraph of ( + (   - (           rs applying the minimum degree greedy algorithm [9]. □

Next we describe a point set whose k-Gabriel graph has high chromatic number:

Proposition 1. For any n ≥ 3 and k ≤ n-3 , there exist sets of n points in the plane whose k-Gabriel graphs have chromatic number at 3 least 3k + 3.

Prot t  i     itd  (ol  i  t a    t    gte. PQ denotes the arc of the circle centered at R with endpoints P, Q, and Q R and RP are defined analogously. The set S consists of the following 3k + 3 points: a group of k + 1 points p1, p2, .. . , pk+1 on PQ and close to P, k + 1 points q1, q2, , qk+1 on Q R and close to Q, and k + 1 points r1, r2, . . . , rk+1 on RP and close to R. There is a way to choose the exact positions of these points so that, for every x, y ∈ S, the closed disk centered at the midpoint of x, y with both x and y on its boundary contains at most k + 2 points from S (see [4] for details). Thus, for every x, y ∈ S, the edge (x, y) belongs to k-GG(S). Then k-GG(S) is a clique and has chromatic number 3k + 3.

ans  s sd  s           s s    i ig a position and k-GG remains the complete graph. Since in the original construction all edges belong to k-GG(S), we only need to show that none of these edges disappear from the graph after perturbing S. This is indeed the case because the region associated to every edge (the diametral disk containing at most k additional points from S) is closed, so points that are outside the disk in the original construction remain outside the new disk if the points are infinitesimally perturbed. Additionally, notice that, if the given n is greater than 3k + 3, it suffices to add to S additional points far from p1, P2, . . . , Pk+1, q1, q2, . . . , qk+1, and r1, r2, ... , rk+1, so that the initial adjacencies are preserved. □

For k-Delaunay graphs we provide a better construction:

Proposition 2. For any n ≥ 4 and k ≤ n-4 , there exist sets of n points in the plane whose k-Delaunay graphs have chromatic number 4 at least 4k + 4.

Proof. Let S be the point set in Fig. 3 (right). The points P, Q, R, form an equilateral triangle, U is the midpoint of R and Q, and T is a point on the vertical line through R such that |RT| = |RP|. The set S consists of k + 1 points p1, P2, . . . , Pk+1


<!-- p:7 -->


Fig. 3. Point sets of Propositions 1 and 2 for k = 3.

T

ti's

rk+1 R

r1

R

q1

U

P

qk+1

pk+1

Q

pi's

Q

p1

P

qi's

o        d  +         +        +        s  1 on Q R very close to R, and k + 1 points t1, t2, . . . , tk+1 on TU very close to T.

This construction was originally described in [15], where the authors showed that, for every pair of points in S, there ei  o ss      a  n       pds and its chromatic number is 4k + 4. Notice that the construction can be perturbed to avoid that three or more points are collinear. □

## 5. Constrained geometric thickness

Let us recall that, given a geometric graph G, the constrained geometric thickness of G, denoted by θc(G), is defined as the minimum number of layers necessary to partition the edges of G so that no two edges of the same layer cross. Since GG(S) and DT(S) are plane, the constrained geometric thickness of these graphs is 1. In this section we give bounds on θc(k-DG(S)) and θc(k-GG(S)), for k ≥ 1. We also tighten these bounds for the particular case k = 1. This extra effort is motivated by the fact that order-1 proximity graphs (together with order-0 proximity graphs) are the most commonly used in applications [1,13,20,21].

### 5.1. Constrained geometric thickness of k-DG(S) and k-GG(S)

Let us introduce some definitions and recall some properties of k-DG(S).

Edges of DT(S) are said to have order 0. The edges of order k ≥ 1 are those belonging to k-DG(S), but not to (k − 1)-DG(S).

Let (pi, p j) be an edge of order k. Then (pi, p j) is an edge in DT(S  {pl,1, Pl,2, . . . , Pl,k}) for some {pl,1, . . . , Pl,k} ∈ S. We will say that (pi, pj) is generated by {pl,1, . . . , pl,k}. It holds that: (i) (pi, pj) is generated by {pl,1, . .. , Pl,k} if and only if there exists a circle through pi and pj whose interior contains pl,1, ... , Pl,k and no other point in S; (ii) if (pi, pj) is generated by {pl,1, . . . , Pl,k}, then (pl,ν, pi) and (pl,ν, p j) are edges in (k − 1)-DG(S) for all ν ∈ {1, . . . , k}.

In order to prove Theorem 6 we use the following well-known geometric fact:

Observation 1. Let (pi, p j) and (pl, pm) be two crossing edges. Either every circle through pi and pj contains pl or pm, or every circle through pl and pm contains pi or p j.

$$\text {Theorem} \, 6 . \, \text {For any set} \, S \, \text {of points in the plane and} \, k \leq \lceil n / 2 \rceil - 1 , \, \theta _ { c } ( k - \text {DG} ( S ) ) \leq \frac { \chi ^ { 2 } ( ( k - 1 ) - \text {DG} ( S ) ) + \chi ( ( k - 1 ) - \text {DG} ( S ) ) } { 2 } .$$

Proof. Consider a χ((k - 1)-DG(S))-vertex coloring f of (k - 1)-DG(S). We use f to construct a

interior. Then pl is connected to pi and pj in the graph (s − 1)-DG(S) ⊆ (k − 1)-DG(S). Therefore f (pl) ≠ f (pi), f (pj). □

(()(-(−))X+((S)(-(I−))X) -coloring of the edges of k-DG(S) such that within each color class no two edges cross. This 2 {  f ( f}    (      (-     ( d d s :      () Let us prove that no two edges of the same color cross. Suppose that (pi, pj) and (pi, pm) are two crossing edges in k-DG(S), where (pi, p j) has order s and (pl, pm) has order t, with 0 ≤ s, t ≤ k. By Observation 1, either C(pi, pj) contains pl or pm, or C(pl, pm) contains pi or pj. Without loss of generality, let us assume that the circle C(pi, pj) contains pl in its

$$\text {Corollary} \, 5 . \text { For any set } S \text { of } n \text { points in the plane } a n d \, k \leq \lceil n / 2 \rceil - 1 , \theta _ { c } ( k \text { - } \text {GG} ( S ) ) \leq \theta _ { c } ( k \text { - } \text {DG} ( S ) ) \leqslant 1 8 k ^ { 2 } + 3 k .$$

We point out that the proof of Theorem 6 is constructive, that is, it describes a method to decompose k-DG(S) and k-GG(S) into at most 18k2 + 3k plane layers. This decomposition might nevertheless be non-optimal.

I    o o s   d -s  ot       der of magnitude:

Proposition 3. For any n ≥ 3 and k ≤ n-3 , there exists a set S of n points in the plane such that θc(k-DG(S)) ≥ θc(k-GG(S)) ≥ 3k 3 2


<!-- p:8 -->


Proof. Consider the point set in the proof of Proposition 1. We rename the points as s1, S2, ..., S3k+3 (this is also the counterclockwise sequence along the convex hull of the point set). The edges (s1, S[ 3k+5 ), (s2, S 3k+7 ), . . . , (s 3k+3 , s2| 3k+3) belong to the k-Gabriel graph and are pairwise crossing. Therefore the thickness of the graph is at least 3k+3 」. □ 2

We tend to believe that our worst-case lower bounds on the constrained geometric thickness of the k-Delaunay and Gabriel graphs are closer to the true values than our upper bounds. The following proposition might give some evidence in this direction.

Pro ss et  + t t   (   e t e d       t  dges.

Proof. Suppose that the graph k-DG(S) contains l pairwise crossing edges. We consider the complete graph H having these d              o   o  :       n Observation 1, every edge of H is oriented. Furthermore, if a vertex (pi, p j) of H has in-degree d, then C(pi, pj) contains at least d points, since the d edges oriented to (pi, pj) are pairwise crossing, which implies that they do not have endpoints in common. Thus every vertex in H has in-degree at most k. Counting the edges of H, we have that () ≤ lk. Consequently, l≤2k + 1. □

### 5.2. Constrained geometric thickness of 1-DG(S) and 1-GG(S)

In this subsection we improve to 4 the upper bound θc(1-DG(S)) ≤ 21 given by Corollary 5. First we make some observations on the structure of 1-DG(S).

Let (pi, pj) be an edge of order 1. Then (pi, pj) is an edge in DT(S  pl) for a certain pl ∈ S. We will say that (pi, pj) is generated by pl. Observe that: (i) (pi, pj) is generated by pι if and only if there exists a circle through pi and pj whose interior contains pi and no other point in S; (ii) every edge of order 1 is generated by at most one point on each side of t   (    ( d)  ( d  '    (  d) i (

Aeoss ti  s    t tt s  ot ' s s e

Corollary 6. Let (pi, p j), (pl, Pm) be two crossing edges in 1-DG(S). If both edges have order 1, then one of them can only be generated ynd        (     or  (         i     t m.

We now prove the main result of this subsection:

Theorem 7. For any set S of n points in the plane, 2 ≤ θc(1-DG(S)) ≤ χ (DT(S)) ≤ 4.

Proof. The graph DT(S) is maximal planar, hence each edge of order 1 crosses at least one edge in DT(S). Since the number of edges of order 1 is strictly greater than zero [1], at least two layers are needed.

Next we prove that each color class is plane.

We now prove the upper bound. Let f be a χ (DT(S))-coloring of the vertices of DT(S). We define a χ (DT(S))-coloring of the edges of 1-DG(S) as follows. Let (pi, pj) be an edge of 1-DG(S). If (pi, pj) has order 1 and is generated by pl, we assign it the color f (pι) (if (pi, p j) is generated by two points of distinct colors, we arbitrarily assign one of the two colors). I( f  ( f    i     (n

Spp        r     s  o r  )    )  rodts by the endpoints of the other. Let us assume that this is the case of edge (pi, pj). Then (pi, pj) has color f (pl) or f (pm). Since the points generating (pl, pm) are connected to both pl and pm in DT(S), their color is different from f(pl) and f (pm). Consequently, (pt, pm) is assigned a color different from f (pl) and f (pm).

Suppose that (pi, p j) and (pl, pm) are two crossing edges, where (pi, pj) has order 1 and (pl, pm) has order 0. The color of (pl, pm) is different from f (pl) and f (pm). By Corollary 6, (pi, pj) can only be generated by pl and pm. Hence its color is f (pl) or f (pm). □

Corollary 7. For any set S of n points in the plane, θc(1-GG(S)) ≤ χ (DT(S)).

We now give a worst-case lower bound on the constrained geometric thickness of 1-DG(S) and 1-GG(S):

Proposition 5. For any n ≥ 6, there exists a set S of n points in the plane such that θc(1-DG(S)) ≥ θc(1-GG(S)) ≥ 3.

Proof. Fig. 4 shows a set of 6 points whose 1-Gabriel graph contains three pairwise intersecting edges. Thus its constrained d   t   s e          u ss


<!-- p:9 -->


## 6. Final remarks

We have studied several properties of two fundamental higher order proximity graphs. As for open problems, a natural one is to close the gaps between the lower and upper bounds on the spanning ratio of k-Gabriel graphs and on the constrained geometric thickness of k-Gabriel and k-Delaunay graphs. In both cases we are inclined to think that the lower bounds are closer to the true values.

## Acknowledgements

This research was initiated during the second UPC-ULB workshop on Computational Geometry. We thank participants Greg Aloupis, Victor A. Campos, Jean Cardinal, and Perouz Taslakian. We also thank Jorge Urrutia and David R. Wood for helpful comments and suggestions.
