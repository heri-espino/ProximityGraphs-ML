---
id: "Bose-Smid_2013_Plane-Geometric-Spanners-Survey"
source_pdf: "../pdf/Bose-Smid_2013_Plane-Geometric-Spanners-Survey.pdf"
source_filename: "Bose-Smid_2013_Plane-Geometric-Spanners-Survey.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "full-page-ocr"
extraction_quality: "excellent"
extraction_score: 108.0
visual_assets: "disabled"
references_file: "../references/Bose-Smid_2013_Plane-Geometric-Spanners-Survey.references.md"
---

<!-- p:1 -->

ELSEVIER

Contents lists available at SciVerse ScienceDirect

## Computational Geometry: Theory and Applications

www.elsevier.com/locate/comgeo

## On plane geometric spanners: A survey and open problems ¥

Prosenjit Bose *, Michiel Smid

School of Computer Science, Carleton University, Ottawa, Ontario, K1S 5B6, Canada

ARTICLE INFO

##### ABSTRACT

Article history:

Available online 23 April 2013 Communicated by S. Langerman

Keywords: Spanners Plane graphs Delaunay triangulations Dilation

### 1. Introduction

Given a weighted graph G = (V, E) and a real number t ≥ 1, a t-spanner of G is a spanning subgraph G′ with the property that for every edge xy in G, there exists a path between x and y in G' whose weight is no more than t times td  t  s -s de h s -s st   t  s dts G and the parameter t represents the approximation ratio. The smallest t for which G' is a t-spanner of G is called the spanning ratio of the graph G'. In the literature, the terms stretch factor is also used.

Spanners have been studied in many different settings. The various settings depend on the type of underlying graph G, on the way weights are assigned to edges in G, on the specific value of the spanning ratio t, and on the function used to measure the weight of a shortest path. We concentrate on the setting where the underlying graph is geometric. In this context, a geometric graph is a weighted graph whose vertex set is a set of points in R2 and whose edge set consists of line segments joining two vertices. The edges are weighted by the Euclidean distance between their endpoints. Given a geometric graph G = (V, E), a t-spanner of G is a spanning subgraph G' with the property that for every edge xy ∈ G, there is a path from x to y in G′ such that the sum of the weights of the edges in this path is no more than t times d(x, y), where d(x, y) denotes the Euclidean distance between x and y. In the literature, the main focus has been on the case where the underlying graph is the complete geometric graph. We review this case as well as other variants.

There is a vast literature on different methods for constructing t-spanners with various properties in this geometric setting (see [52] for a comprehensive survey of the area). Aside from trying to build a spanner that has small spanning ratio, additional properties of the spanners are desirable. Typical goals in this area include the construction of t-spanners that also have few edges, bounded degree, fault tolerance, and low weight, to name a few. Notice that some of these properties actually oppose each other. For example, a graph with few edges or bounded degree cannot have a high faulttolerance. Therefore, one needs to balance the various properties.

Our goal in this survey is to review results related to the following problem: Given a finite set P of points in R2, construct a plane t-spanner of the complete geometric graph with vertex set P, for some constant t ≥ 1. We also explore the setting where the underlying graph is not the complete graph but some other type of graph such as the unit-disk

☆ The authors are supported by the Natural Science and Engineering Research Council of Canada.

* Corresponding author. E-mail addresses: jit@scs.carleton.ca (P. Bose), michiel@scs.carleton.ca (M. Smid).

Given a weighted graph G = (V, E) and a real number t ≥ 1, a t-spanner of G is a spanning subgraph G′ with the property that for every edge xy in G, there exists a path between x and y in G' whose weight is no more than t times the weight of the edge xy. We review results and present open problems on different variants of the problem of constructing plane geometric t-spanners.

Crown Copyright © 2013 Published by Elsevier B.V. All rights reserved.

Computational

Geametry

CrossMark


<!-- p:2 -->


Fig. 1. Tilted equilateral triangle and L1-metric diamond.

Tilted equilateral triangle

L1-metric diamond

graph or the visibility graph of a set of line segments. Finally, we touch on plane spanners with bounded spanning ratio. In addition to surveying various results related to the construction of plane t-spanners, we also mention several open problems in the area and provide some proof sketches of a few results so that the reader may get a flavour of the different techniques used in this area.

In the rest of this paper, we say that a graph is a spanner if it is a t-spanner for some constant t.

### 2. Plane spanners

In what follows, unless specified otherwise, we assume that the underlying graph is the complete geometric graph. We let P be a finite set of points in the plane. The following is the central question addressed in this section: Given the point set P, is it always possible to construct a plane spanner? What constraints does planarity place on the spanning ratio?

#### 2.1. Upper and lower bounds

In his seminal paper, Chew [24] was the first to study the question of determining whether it is possible to construct a plane spanner. First, he observed that requiring planarity does indeed impose a lower bound on the spanning ratio. Consider four points placed at the four corners of a square. Every plane geometric graph embedded on those 4 points has a spanning ratio of at least √2. This was the best known lower bound on the spanning ratio until Mulzer [50] showed that every triangulation of a regular 21-gon has spanning ratio at least √2.005367532 ≈ 1.41611. This leads us to our first open problem:

Open Problem 1. What is the best lower bound on the spanning ratio of plane geometric graphs? Specifically, is there a t &gt; √2.005367532 and a point set P, such that every triangulation of P has spanning ratio at least t?

#### 2.2. Variants of Delaunay graphs

All of the known methods for constructing plane constant spanners of a point set are related to various types of Delaunay graphs. The L1-metric Delaunay graph of P is the plane graph that is constructed in the following way. Two points x, y ∈ P form an edge of the Delaunay graph provided there is a point in R2 such that x and y are its nearest neighbours in the L1 metric (see [53] for a comprehensive review of Delaunay Graphs and Voronoi Diagrams). Note that the unit circle in the L1 metric is a diamond (a unit square tilted by 45 degrees); see Fig. 1. The planarity of this graph is only ensured provided that no 4 points lie on the boundary of a tilted square. Chew [24] showed that the L1-metric Delaunay graph is a √10-spanner of the complete Euclidean geometric graph. Note that the L∞-metric Delaunay graph has an axis parallel square as its unit circle. Thus, the L1 Delaunay graph of a point set is identical to the L∞ Delaunay graph of the same point set rotated by 45 degrees. Therefore, Chew's result implies that the L∞ Delaunay graph is a √10-spanner. Recently, Bonichon et al. [7] showed that the L1 and L∞Delaunay graph is a √4 + 2√2-spanner and that this is tight in the worst case.

Given a set of points P, the Yao∞ (P) is defined as follows. Two points x, y ∈ P form an edge of Yaoœ (P) provided there is an axis parallel square with x as a vertex of the square, y on the boundary of the square and no other points of P in the interior of the square. Notice that the Yao% (P) graph is a subgraph of the L∞ Delaunay graph on P. The Yaox (P) was shown to be an 8√2-spanner [12].

In the journal version of [24], Chew [26] improved the result by showing that one can construct a plane graph whose spanning ratio is at most 2. He proved that a Delaunay graph built using a convex distance function defined by an equilateral triangle having one vertical side, as opposed to the L1-metric diamond or L∞-metric square, has a spanning ratio of 2 and that this bound is tight in the worst case. He refers to these equilateral triangles as tilted equilateral-triangles (see Fig. 1). The tilted equilateral-triangle Delaunay graph of a planar point set P is constructed in the following manner. Two points x, y ∈ P share an edge provided that there exists a tilted equilateral triangle with x and y on its boundary and no points of P in its interior. Using the results of Bonichon et al. [5], a simple inductive proof of the spanning ratio of 2 with applications to routing was given [15].


<!-- p:3 -->


Fig. 2. One-sided Voronoi path from x to y shown in bold.

●

x

●

A natural question that Chew [26] posed is whether or not the standard (i.e., Euclidean) Delaunay triangulation is a spanner. By placing the points on the boundary of a circle, Chew noticed that the spanning ratio of the Delaunay triangulation can be at least π/2 – € for any € &gt; 0; see Fig. 3(a). This led him to conjecture that not only is the standard Delaunay triangulation a spanner but that its spanning ratio is strictly less than 2. This conjecture was recently settled by Xia [57] who showed that the Delaunay triangulation has a spanning ratio of at most 1.998.

The first to show that the standard Delaunay triangulation of a point set is indeed a spanner were Dobkin et al. [30]. They showed that the spanning ratio of the Delaunay triangulation is at most (1 + √5)π/2 ≈ 5.08.

Almost all of the proofs in the literature are constructive. We give the reader a flavour of how some of these proofs proceed by highlighting one of the cases in Dobkin et al.'s proof. Let DT(P) be the standard Delaunay triangulation of P and Vor(P) the Voronoi diagram of P. It is well-known that DT(P) and Vor(P) are duals of each other. Given two points o     s 'o  o o     on      d      on a horizontal line, unit distance apart, with x to the left of y. Let Pvor(P)(x, y) = [x = p1, p2, . . . , pk = y] be the sequence of sites of Vor(P) whose cells intersect the segment xy ordered from x to y. We call Pvor(P) (x, y) a Voronoi path. By the duality relation between Delaunay triangulations and the Voronoi diagram, this path consists of Delaunay edges. The Voronoi path is called one-sided provided that all of the sites lie in one closed half-plane defined by the line containing xy. See Fig. 2 for an example. Denote by cj the intersection point of the segment xy with the Voronoi edge separating the cells of pj and pj+1. Notice that by construction the circle centred at cj with radius cjPj, denoted C(cj, pj), has pj and pj+1 on its boundary and is empty of all other points of P. Furthermore, the arc of C(cj, pj) defined clockwise from pj to pj+1 is longer than the segment pjp j+1. Therefore, when Pvor(P) (x, y) is a one-sided Voronoi path, its length is bounded by half the boundary of the union of the circles C(cj, pj), j = 1, ... , k — 1. Since the boundary of the union of these circles has length at most π, the length of Pvor(P)(x, y) is at most π/2. When the Voronoi path is not one-sided, its spanning ratio can be unbounded. In this case, Dobkin et al. showed how to construct a path with spanning ratio at most (1 + √5)π /2. The argument in this case is slightly more involved.

Subsequently, Keil and Gutwin [42] showed that the spanning ratio of the Delaunay triangulation is at most 4π√3/9 ≈ 2.42. Their proof is inductive and also relies heavily on the empty circle property of Delaunay triangulations. Cui et al. [27] then improved the upper bound on the spanning ratio for points in convex position. They showed that when points are in convex position, the upper bound on the spanning ratio is at most the root of some function bounded above by 2.33. Finally, Xia [57] showed an upper bound of 1.998.

pn n  ¿ n    ns   on enn   s   ln d smaller upper bound on the spanning ratio for points in convex position?

When considering the above problems, one also needs to consider the issue of lower bounds. Chew [26] conjectured that the worst-case spanning ratio of the Delaunay triangulation is π/2 and showed that by placing points on the boundary of a circle, one can approach this bound. The fact that one-sided Voronoi paths also have a spanning ratio of at most π/2 led many to believe that π /2 was the correct bound. Surprisingly, it was shown recently that the worst-case spanning ratio of the Delaunay triangulation is actually greater than π /2 [14]. There exists a set of points in convex position for which the spanning ratio of the Delaunay triangulation is at least 1.581. See Fig. 3(b). The lower bound can be slightly improved to 1.5846 if points do not need to be in convex position. Moreover, it is shown that the lower bound on the spanning ratio of the Delaunay triangulation is essentially the same for random point sets. The lower bound when points are not in convex position has been further improved to 1.5932 [58].


<!-- p:4 -->


Fig. 3. (a) Construction providing a lower bound of π /2 – € on the spanning ratio. (b) Construction providing lower bound of 1.581. The basic construction consists of two unit semicircles separated by a fixed distance that is optimized to maximize the spanning ratio. The shortest path from p to p' in the Delaunay triangulation has spanning ratio at least 1.581.

(a)

(b)

Open Problem 3. What is the best lower bound on the worst-case spanning ratio of the Delaunay triangulation? Can one construct a point set such that the spanning ratio of its Delaunay triangulation is strictly greater than 1.5932? For points in convex position, can one construct a point set such that the spanning ratio is strictly greater than 1.581?

Although all of the known upper bounds on the spanning ratio of planar graphs are obtained using some variant of the Delaunay graph, the following question still remains open.

Open Problem 4. What is the best upper bound on the spanning ratio of a plane graph? The best that is currently known is an upper bound of 1.998.

#### 2.3. Minimum spanning ratio

One question that comes to mind when contemplating the above problem is how to compute, for a given point set, the plane graph with minimum spanning ratio. The complexity of the problem is unknown, however, there is strong evidence to suggest that the problem is NP-hard. Recently, Klein and Kutz [45] showed that computing, when given a point set and ni ns       -        -      a ae even computing the spanning tree with minimum spanning ratio of a given point set is an NP-hard problem. However, their pdrns n  s ns  n ns    ng   srn   s s nng ratio need not be plane. This leads to the following two open problems:

Open Problem 5. Is computing the plane graph of minimum spanning ratio for a given point set an NP-hard problem?

Open Problem 6. Is computing the plane spanning tree of minimum spanning ratio for a given point set an NP-hard problem?

#### 2.4. α-diamond spanners

The empty circle property is the key property of Delaunay triangulations that is exploited to prove the upper and lower bounds on the spanning ratio. However, there does not seem to be anything particularly special about circles. One can view the empty circle property as each edge of the triangulation having an empty buffer region on one side of the edge. In other words, each edge of the triangulation has a fixed proportional amount of space on one of its sides that is guaranteed to be empty of points. Das and Joseph [29] formalized this notion in the following way.

Definition 1. Given a point set P and two points x, y ∈ P, the segment xy has the α-diamond property provided that at least one of the two isosceles triangles with base xy and base angle α does not contain any point of P. Note that the apices of the isosceles triangles need not be points of P. See Fig. 4.

A plane graph has the α-diamond property when every edge of the graph has the α-diamond property for some fixed α. Moreover, a plane graph has the d-good polygon property if for every visible pair of vertices a, b on a face f, the shortest distance from a to b around the boundary of f is at most d times the Euclidean distance between a and b. Two vertices a, b form a visible pair provided that the segment ab does not intersect the exterior of the face. Das and Joseph showed that an α-diamond plane graph with the d-good polygon property has a spanning ratio of at most 8dπ2/(α2 sin2(α/4)). This was slightly improved to 8d(π − α)2/(α2 sin2(α/4)) [19]. Notice that when the value of d is 1, then a plane graph with the α-diamond property must be a triangulation. Das and Joseph showed that certain special types of triangulations possess the α-diamond property for fixed values of α. The empty circle property implies that Delaunay triangulations have the α-diamond property for α = π /4. Das and Joseph also proved that the minimum weight triangulation and the greedy triangulation each have the α-diamond property with α = π/8. The minimum weight triangulation of a point set is defined as the triangulation whose sum of the lengths of its edges is minimum over all possible triangulations of the given point set. It was recently shown that computing such triangulations is NP-hard [51]. The greedy triangulation is one that is constructed in the following way. Starting with just the vertices, edges are added in non-decreasing order\_as long as planarity is not violated. Drysdale et al. [31] improved the value of α for greedy triangulations to arctan(1/√5). Bose et al. [19] subsequently improved this to π /6.


<!-- p:5 -->


Fig. 4. Segment xy has the α-diamond property and segment ab does not.

α

b

y

x

a

Fig. 5. The proximity regions for various values of β.

β = 0

I &gt; g &gt; 0

β = 1

β&gt;1

β = ∞

x•

•y

x

y

x

y

x

h

x•

y

Open Problem 7. Can the spanning ratio for plane graphs with the α-diamond property and the d-good polygon property b¿ s ( -   s    ds   s  a 'd ¿ (

Open Problem 8. Is the α-value for greedy triangulations greater than π /6?

Open Problem 9. Is the α-value for minimum weight triangulations greater than π /8?

#### 2.5. Convex Delaunay spanners

Chew [24,26] showed that the Delaunay graph constructed using two different convex distance functions (based on the diamond and the tilted equilateral triangle) results in a spanner of the complete Euclidean graph. This begs the question vh  rds   sr ot h  r  u  r   o  rhg complete Euclidean graph. Bose et al. [10] answered this in the affirmative by showing that the Delaunay graph constructed using any convex distance function results in a spanner of the complete Euclidean graph where the spanning ratio depends on the shape of the compact convex set used to define the distance function.

#### 2.6. Proximity-based plane spanners

We already noted that it is the empty region property of Delaunay graphs that makes them spanners. The above generalizations show that the type of empty region around each edge is not particularly important but simply the fact that an empty region exists. This leads to questions such as whether or not other kinds of geometric proximity graphs are spanners. A geometric graph is a proximity graph when some sort of an empty region property defines the edges of the graph. Many proximity graphs are non-plane or disconnected. One well-known class of proximity graphs is the β-skeletons [43]. A β-skeleton of a set P of points in the plane, denoted BSkELβ(P), is a proximity graph where the proximity region for two points x, y ∈ P is a function of β (see Fig. 5):

1. For β = 0, the proximity region is the line segment xy.
2. For 0 &lt; β &lt; 1, the proximity region is the intersection of the two disks of radius d(x, y)/(2β) passing through both x and y.


<!-- p:6 -->


- 3od                ond       n ts ·(2/g − 1) + x(2/g) p(2/g) + x(2/g − 1)
4. For β = ∞, the proximity region is the infinite strip perpendicular to the line segment xy.

The edge xy is in the β-skeleton of P if the proximity region of xy does not contain any other points of P. Notice hilt t t i ie i it it in ser   it  f ri t  i i tnt same value of β if the proximity regions are constructed with open rather than closed disks. When the proximity region is constructed with an open disk, it is referred to as the open β-skeleton, otherwise, it is referred to as the closed β-skeleton. For the range 0 ≤ β &lt; 1, the β-skeleton is not necessarily plane and for the range β &gt; 2, the β-skeleton is not necessarily connected. The range of interest for plane connected graphs is β ∈ [1, 2]. The extreme values in this range define some well-known families of plane connected proximity graphs. The Relative Neighbourhood Graph (RNG), which is also the open 2-skeleton, was first defined as a geometric graph where two vertices x, y are adjacent provided that there is no third vertex z in the graph with the property that max(d(x, z), d(y, z)) &lt; d(x, y). The Gabriel Graph (GG), which is the closed 1-skeleton, was first defined as a geometric graph where two vertices x, y are adjacent provided that there is no third vertex z in the graph with the property that d(x, z)2 + d(z, y)2 ≤ d(x, y)2. It is well-known that RNG(P) ⊆ GG(P) ⊆ DT(P). See Jaromczyk and Toussaint [38] for a survey of various proximity graphs.

Bo s         s -   ds  s  i  s [   hat the spanning ratio can be at least (1/2 — o(1))√n and is always at most n — 1. They also showed that Gabriel graphs have a spanning ratio of at most 4π√2n — 4/3 and exhibited a family of point sets where the Gabriel graph has a spanning ratio of at least 2√n/3 thereby showing that the bound is Θ(√n). They proved that the spanning ratio of the RNG is at most o    ss  t o    o t    u unit square, they showed that the spanning ratio for the Gabriel graph and all β-skeletons with β ∈ [1, 2] tends to infinity in probability as √logn/log logn. Wang et al. [55], subsequently, showed that the spanning ratio of Gabriel graphs is at most √n — 1 and that there exist point sets where this ratio is achieved. For β ∈ [1, 2], they provide an upper bound on the spanning ratio that depends on β, specifically, (n − 1)γ where γ = 1 − log2(√2/β).

Open Problem 10. For the range β ∈ [1, 2], is there a stronger lower bound of the spanning ratio that depends on β?

'   =   (     d    d  e tight? It is tight for the GG, where β = 1 and RNG, where β = 2.

In the range β ∈ [0, 1], the resulting β-skeletons are not necessarily plane. For example, the 0-skeleton is the complete graph. However, recently, Bose et al. [8] studied the spanning properties of the family of graphs RGGβ(P) := BSkELβ(P) ∩ D  t       ted     d     e and plane, hence the name Relaxed Gabriel graphs for this family. They showed upper and lower bounds on the spanning ratio for BSKELβ(P) that depend on β ∈ [0, 1]. The upper bound on the spanning ratio of RGGβ(P) is O (nγ), where γ = ratio of RGGβ(P) is Ω(nγ), with γ = 1 − 1 (log(1 + √ 2

Open Problem 12. Are these upper and lower bounds tight?

#### 2.7. Bounded-degree plane spanners

Another question that comes to mind is whether or not it is possible to build a plane spanner with bounded degree. All of the above plane spanners can have unbounded degree.

Bose et al. [17] were the first to show the existence of a plane t-spanner (for some constant t), whose maximum vertex degree is bounded by a constant. To be more precise, they showed that the Delaunay triangulation of any set P of points in the plane contains a subgraph, which is a t-spanner for P, where t = 4π (π + 1)√3/9, and whose maximum degree is at og :  s       r   n  'n  o 9 =     +        ed the degree bound to 17 and generalized the result to α-diamond triangulations (i.e. they showed that every α-diamond triangulation contains a subgraph that is a plane bounded-degree spanner). Kanj and Perkovic [39] showed how to compute a plane spanner of maximum degree 14 that is a subgraph of the Delaunay triangulation. A breakthrough in this area came with the paper by Bonichon et al. [6]. They presented a simple and elegant method for constructing a plane 6-spanner with maximum degree 6. Their algorithm is based on the Delaunay triangulation where the empty region is an equilateral tsi o ot t      sa s   at  ns  s s es rr      s s  ' n  s   s     n n spanner with maximum degree 7 that is a subgraph of the standard Delaunay triangulation and a strong plane spanner w    l  e  e   dns    s e  e ul n s  s    t  n                s     dh edges in this path is no more than t times d(x, y) and every edge on this path has length at most d(x, y).


<!-- p:7 -->


Open Problem 13. What is the smallest maximum degree that can be achieved for plane spanners that are subgraphs of the standard Delaunay triangulation?

Open Problem 14. What is the smallest maximum degree that can be achieved for plane spanners?

If one does not insist on having a plane spanner, then it is possible to construct a spanner with maximum degree 3 [28]. - s s  t       r  at s ss t  vt t    s n bounded spanning ratio. As such, the more interesting question becomes whether the planarity constraint actually imposes a higher lower bound on the maximum degree. Thus, we have the following open problem:

oo o  n n n  o  r rr  o      o re that is greater than 3? That is, can we show the following: For every real number t &gt; 1, there exists a set P of points, such that every plane degree-3 spanning graph of P has spanning ratio greater than t.

### 3. Low weight plane spanners

The weight of a graph is the sum of the weights of its edges. A lower bound on the weight of a connected graph is t    wt (  s  st e     s s    s     thg minimum spanning tree. As such, one objective in this area is to build plane spanners that have constant spanning ratio and Iou  s   uuds          d l   o  or whose spanning ratio is at most 1 + € times that of G and whose weight is at most O(1) times the weight of the minimum sp v ds n   p   s (        dns Lnl d  u      a t    ndd r  n  t s [ sippt that is a t-spanner for t = (r − 1)4π√3/9 and whose total weight is at most 1 + 2/(r — 2) times the weight of a minimum spanning tree. Subsequently, Kanj et al. [40] showed how this method can be generalized to build bounded degree plane spanners. They showed that for any integer constant k ≥ 14 and r &gt; 2, one can build a plane t-spanner with maximum degree k, where t = (r − 1)(4π√3/9)/(1 + 2π (k cos(π /k))) and whose total weight is at most 1 + 2/(r − 2) times the weight of the minimum spanning tree.

Open Problem 16. Are these bounds tight?

### 4. (1 + €)-plane Steiner spanners

As we have seen in Section 2.1, there exist point sets that do not admit a plane spanner with spanning ratio arbitrarily close to 1. Let P be a set of n points in the plane. In this section, we consider plane Steiner spanners, which are plane graphs whose vertex sets contain P. Vertices that do not belong to P are called Steiner points. It turns out that by allowing r ds  a      g n       s      s  o defined only in terms of point-pairs in the set P.

We give a sketch of the construction, which is due to Arikati et al. [2]. The starting point is to consider the plane Steiner spanner problem in the L1 metric. Thus, we want to construct a plane graph, whose vertex set contains P, such that any two points x and y of P are connected by a path whose L1 length is at most 1 + ∈ times the L1 distance between x and y.

A box is defined to be an axes-parallel rectangle whose longest side is at most twice as long as its shortest side. A doughnut is defined to be the set-theoretic difference B \ B' of two boxes B and B', where B' is contained in B; see Fig. 6. We put the following additional restriction on any doughnut: For any edge e' of the inner box B', consider the corresponding edge e of the outer box B; for example, if e' is the top edge of B', then e is the top edge of B. We require that the distance between e and e' is either zero or at least the length of e'.

Let C be a square that contains all points of P. Using an algorithm of Arya et al. [3], we can compute, in O(n logn) time, a subdivision of C into O (n) cells, such that each cell is either a box or a doughnut. Moreover, each box contains at most one point of P, whereas each doughnut is empty of points. Notice that the edges of this subdivision define a graph. We augment this graph in the following way.

Consider a box B in the subdivision and let l be the length of its shortest side. On each side of B, we place O(1/€) Steiner points such that successive Steiner points have distance ∈l. Then we connect these Steiner points by a grid; see Fig. 7. If B contains a point, say p, of P, then we also add horizontal and vertical rays from p to the edges of B. By tuirt  in t  o st  stns r   t    ns ig t  cg doughnut B \ B', we do a similar construction, one for the outer box B and one for the inner box B', as illustrated in Fig. 7. Again, this results in a plane graph inside B \ B′ consisting of O(1/€2) vertices.


<!-- p:8 -->

B

≥ eh

B′

ev

≥ e′

eh

≥ e′

Fig. 6. The doughnut B \ B'.

p

Fig. 7. Adding Steiner points to boxes and doughnuts.

Since the number of cells in the subdivision is O (n), we obtain a plane graph whose vertex set contains P and that has O (n/€2) Steiner points. Let x and y be two points of P, and consider the Manhattan path M (with two segments) between t   +  i  s       d     t s t  o s    es the length of M. Thus, our graph is a plane Steiner (1 + O (€))-spanner of the point set P for the L1 metric.

T            d-((    r   bin rotating the X- and Y-axes by angles of i∈, for 0 ≤ i &lt; 2π /€. For each coordinate system, we construct the plane Steiner spanner for the L1 metric corresponding to that system. By overlaying all these graphs, Arikati et al. [2] show that we obtain a plane graph with O (n/€4) Steiner points. Since for any two points x and y in P, there is a coordinate system such that the L1 distance (in this system) is within a factor of O (€) of the Euclidean distance between x and y, this gives indeed a plane Steiner (1 + O (€))-spanner of P. By replacing ∈ by δ€, for some small constant δ, we obtain a plane Steiner (1 + €)-spanner of P.

#### Open Problem 17. Can the dependence on € in the solution sketched above be improved?

We finally mention that Arikati et al. [2] showed that these results can be generalized to the case when we are given a set P of n points and a collection of polygonal obstacles (none of which contains any point of P) of total complexity O (n). For this case, we obtain a plane graph with O (n/€4) Steiner points such that the following is true: For any two points ins     t             d    t     st obstacle-avoiding path between x and y. Maheshwari et al. [49] have given a slightly simplified version of this construction which, in fact, is efficient even in external memory.

### 5. Dilation

In Section 4, we considered Steiner spanners for a given set P of points in the plane. When measuring the spanning ratio of such a spanner, we considered only pairs of points in P, i.e., we did not consider the spanning ratio for pairs x, y, where x or y is a Steiner point. In this section, we do take these pairs into account.

For any geometric graph G, we denote its spanning ratio by SP(G). Let P be a (finite or infinite) set of points in the plane. The dilation of P is defined to be the infimum of SP(G), over all plane graphs G = (V, E) for which P ⊆ V and V \ P is finite.

In Fig. 8, triangulations with spanning ratio 1 are given; the two figures on the left constitute infinite families, whereas t-i   i   i s s  s       s    i eti angulations with spanning ratio 1. Notice that any finite point set P that is contained in the vertex set of one of these triangulations has dilation 1. Klein and Kutz [44] have shown that the dilation of every other point set is strictly larger than 1.


<!-- p:9 -->


Fig. 8. All triangulations with spanning ratio 1.

Eb s t      d  s (  ss d  t dbs t   e -son is larger than 1.00157. They have also shown that the dilation of every finite point set is less than 1.1247.

Open Problem 18. What is the smallest value of t such that every finite set of points in the plane has dilation at most t? It is known that 1.00157 ≤ t ≤ 1.1247.

It turns out that even for small point sets, it is very difficult to determine their dilation:

Open Problem 19. What is the dilation of the vertices of a regular 5-gon? It is known that this dilation is at most 1.02046; see [34].

We now turn to the so-called geometric dilation. Consider a plane geometric graph and let x and y be two distinct points "on" G, i.e., each of x and y is either a vertex or in the interior of some edge. Let SPG(x, y) be the ratio of the shortest-path distance between x and y in G to the Euclidean distance d(x, y). The geometric dilation of G is defined to be the supremum of SPG(x, y) over all such pairs x, y. For example, consider a triangle T and let α be its largest acute angle. If we consider T to be a graph whose vertex set consists of the three vertices of T, then the spanning ratio of T is equal to 1. On the other hand, the geometric dilation of T is at least 1/ sin(α/2), which is at least 2.

The geometric dilation of a finite set P of points in the plane is defined to be the infimum of the geometric dilations of all finite plane graphs whose vertex sets contain P.

As opposed to the dilation of the vertex set of the regular n-gon Pn, its geometric dilation has been determined by Ebbers-Baumann et al. [33]: The geometric dilations of P3 and P4 are 2/√3 and √2, respectively. For n ≥ 5, the geometric dilation of Pn is equal to π/2.

In Dumitrescu et al. [32], it is shown that the geometric dilation of every finite point set is less than 1.678. Furthermore, they showed that the geometric dilation of the vertices of the 19 × 19 grid is larger than (1 + 10−11)π /2.

Open Problem 20. What is the smallest value of t such that every finite set of points in the plane has geometric dilation at most t? It is known that (1 + 10−11)π /2 ≤t ≤ 1.678.

### 6. Variants

In the previous sections, the underlying graph has been the complete geometric graph. We now review some results when the underlying graph is not necessarily the complete geometric graph but a subgraph. We explore two different settings: one where the underlying graph is the visibility graph of a set of line segments and the other where the underlying graph is the unit-disk graph. We begin with the former.

#### 6.1. Constrained setting

Before we can review the results in the constrained setting, we need to outline precisely what is meant by the constrained setting. Let P be a set of points in the plane and let L be a set of non-crossing line segments whose endpoints are in P. Two line segments intersect properly if they share a common interior point. Two points x and y of P are visible with respect to L provided the segment xy does not properly intersect any segment of L. The visibility graph of P constrained to L, denoted Vis(P, L), is the geometric graph whose vertex set is P and whose edge set contains L as well as one edge for each visible pair of vertices (see Fig. 9). All edges, including the constrained edges, are weighted by their length. A spanning subgraph of Vis(P, L) whose edge set contains L is a geometric graph constrained to L. In such a graph, the elements of L are referred to as the constrained edges, whereas all other edges are referred to as unconstrained edges or visibility edges.


<!-- p:10 -->


Fig. 9. The visibility graph Vis(P, L) where segments of L are shown in bold.

Fig. 10. The edge e has the visible α-diamond property.

a(e)

△(e)

α


e

α

●

The underlying graph in this subsection is Vis(P, L). Thus, a constrained geometric graph G(P, L) is a constrained t-spanner of Vis(P, L) provided that for every edge xy in Vis(P, L), the length of the shortest path between x and y in G(P, L) is at most t times the Euclidean distance between x and y. Note that if G(P, L) is a constrained t-spanner, then for every pair x, y of points in P (not just visible edges), the shortest path from x to y in G(P, L) is at most t times the shortest path from x to y in Vis(P, L). The fundamental question to address here is: Given Vis(P, L), does there always exist a plane constrained spanner G(P, L) of Vis(P, L)?

Chew [24,26] mentioned that his technique (see in Section 2.1) can be extended to the constrained setting. Karavelas [41] noted that the proof in Dobkin et al. [30] can also be extended to the constrained setting, thereby asserting that the Constrained Delaunay triangulation, denoted CDT(P, L), is a (1 + √5)π /2-spanner of Vis(P, L). The constrained Delaunay triangulation was independently introduced by Chew [25] and Wang and Schubert [54]. It is a generalization of the standard Delaunay triangulation. Two visible points x, y ∈ P form an edge in CDT(P, L) provided that there exists a disk with x and y on its boundary that does not contain any point z ∈ P that is visible to both x and y. Subsequently, Bose and Keil [18] proved that the spanning ratio of the CDT(P, L) is at most 4π√3/9. If one replaces an empty disk with an empty equilateral triangle in the definition of CDT(P, L), one gets a generalization of the empty equilateral triangle Delaunay graph used by Chew [26]. Recently, Bose et al. [16] showed that the constrained empty equilateral triangle Delaunay graph is a 2-spanner. They also showed how to construct a plane 6-spanner of Vis(P, L) with maximum degree 6 + c, where c is the maximum number of segments incident to a vertex.

Bonr td  os entd   d  n sd o s  td oe    opd G(P, L) is said to have the visible α-diamond property if, for every unconstrained edge e in the graph, at least one of the two isosceles triangles, with e as the base and base angle α, does not contain any points of P visible to the endpoints of e. Refer to Fig. 10. Furthermore, G(P, L) has the d-good polygon property if for every visible pair of vertices a and b on a face f, the shortest distance from a to b around the boundary of f is at most d times the Euclidean distance between a and b. Bose et al. [19] generalized the results on α-diamond spanners in the following way: Given fixed α ∈ (0, π /2) and d ≥ 1, if a constrained plane graph G(P, L) has both the visible α-diamond property and the d-good polygon property, then its spanning ratio is at most 8(π−α)2d α2 sin2(α/4)

Open Problem 21. Essentially, all of the questions that are open in the unconstrained setting are also open in the constrained setting since the constrained setting is a generalization of the unconstrained one.

#### 6.2. Unit-disk graphs

Given a set P of points in the plane, the unit-disk graph, denoted UDG(P), is the geometric graph whose vertex set is P with two vertices being joined by an edge provided the length of the edge is at most a specified unit. There has been much interest in studying spanners of UDG(P) in the wireless network community since these graphs are often used to model wireless adhoc networks (see [4] for an overview of the area).

The question to address in this area is: Does there always exist a plane spanner of the unit-disk graph? Before answering this question, we first highlight a connection between strong spanners and spanners of the unit-disk graph. Recall that given a geometric graph G, a t-spanner G′ of G is strong if for every edge xy ∈ G, there is a path from x to y in G′ such that the su  s  d s     (  s  as s o s d s s       ost d(x, y). It is the latter property that distinguishes a spanner from a strong spanner. Note that any method for constructing a plane strong spanner of the complete geometric graph becomes a technique for constructing a plane spanner of the unitdisk graph. That is, if a graph G is a plane strong spanner of the complete geometric graph, then G ∩ UDG is a plane strong spanner of UDG, provided UDG is connected.


<!-- p:11 -->


o r     s n S  o  n  ns o rn  rne o   ng proving that the Delaunay triangulation is a strong 4π√3/9-spanner. They showed that the proof by Keil and Gutwin [42] can be generalized to show that the Delaunay triangulation is indeed a strong spanner. This implies that DT(P) ∩ UDG(P) is dl  d n o-  on  n t s  e on ' n   ds d e where the maximum degree is at most 17.

The algorithms to obtain the above results are all centralized. This means that the algorithm is aware of the whole graph. Since there is interest in studying these spanners in the wireless network community, it should be noted that centralized algorithms are undesirable in that setting. In the wireless network setting, the challenge is to compute these spanners in a local manner. A wireless ad hoc network consists of a set P of n wireless nodes in the plane. Each wireless node u ∈ P can only communicate directly with nodes that are within its communication range. If we assume that this range is equal to one unit for each node, then one can see how the unit-disk graph UDG(P) models a wireless ad hoc network. We now describe what it means for an algorithm to be local in this setting.

In the wireless setting, it is assumed that UDG(P) is connected and that each node knows its position and the position of ali  sn i o  o  ou oo  r  n on on  ii the nodes. For simplicity, a message is often defined as the x-coordinate and y-coordinate of a point since that is the content om  s m  o  s  n  s mss  s ss  tho metric used to measure the performance of different construction algorithms is the total number of messages broadcast as a function of the number of nodes. The construction algorithm is usually synchronized and a communication round is defined as the period between the sending of a message and the complete processing of the message on the receiver side. For any positive integer k, let Nk(v) = {w | there is a path in UDG(P) between ν and w with at most k edges}. If every node ν can compute the value of any computable function with domain Nk(v) by an algorithm, we define this algorithm to be a k-local algorithm. For example, let DT(P) be a function that returns the Delaunay triangulation of P, then the localized algorithm where each node v runs DT(N2(v)) is a 2-local algorithm. Computing Nk(v) is typically more expensive than computing Nk-1(v) in a localized environment, therefore, it is desirable to design k-local algorithms with the smallest k as possible.

Let UDEL(P) be the intersection between the unit-disk graph and the Delaunay triangulation of P. Gao et al. [36] proposed a localized algorithm to build a plane graph called the restricted Delaunay graph (RDG), which is a supergraph o    at s     n  s           l  g n t               s  i t      o       n      a   (  td total message complexity of their algorithm is O (n2).

In [47], Li et al. defined a k-localized Delaunay triangle as a triangle ∆uvw whose interior of the circumcircle disk l tha  sa t d  s (d l   '  -   s  n o al Gabriel edges with length at most one and the edges of all k-localized Delaunay triangles. They showed that LDel(k)(P) is a supergraph of UDEL(P) and plane if k ≥ 2. They also defined PLDel(P) as the plane graph obtained by removing intersecting edges, which do not belong to LDel(2)(P), from LDel(1)(P). Notice that PLDel(P) is a subgraph of LDel(1)(P), a supergraph of LDel(2)(P) and also a t-spanner of UDG(P) for t = 4π√3 9

t l   l l    l l   -  d o   l  en as     s      s nt   n   s   ss a sei l- os  d       o o     o  o s  ca lq o s  o   o o  o     o n bounded by 11n. Bose et al. [11] improved the work of Araújo et al. [1] by presenting an efficient 2-local algorithm to compute PLDel(P). Their algorithm needs one communication round and the message complexity can be bounded by 5n.

¿dl  es  r  p  r ne  r r  o oe n o r o dr

Wang and Li [56] presented a 3-local algorithm that computes a plane spanner of UDG(P) with degree bound 23. The communication cost of their algorithm is O (n). Very recently, Kanj et al. [40] presented, for any given k ≥ 14 and λ &gt; 2, an L(8/π)(λ + 1)2」-local algorithm that constructs a plane spanner of UDG(P) with degree bound k. Both of these two algorithms are based on the construction of the 2-localized Delaunay graph LDei(2)(P). Although LDel(2)(P) could be constructed with communication cost O (n) [56] by using the result of [22], the constant in the O(n) bound could be several hundred.
