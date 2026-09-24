---
id: "Ceyhan_2010_Proximity-Regions-Higher-Dimensions"
source_pdf: "../pdf/Ceyhan_2010_Proximity-Regions-Higher-Dimensions.pdf"
source_filename: "Ceyhan_2010_Proximity-Regions-Higher-Dimensions.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "full-page-ocr"
extraction_quality: "excellent"
extraction_score: 100.0
visual_assets: "disabled"
references_file: "../references/Ceyhan_2010_Proximity-Regions-Higher-Dimensions.references.md"
---

<!-- p:1 -->

ELSEVIER

Computational

Ceometry

Contents lists available at ScienceDirect

## Computational Geometry: Theory and Applications

www.elsevier.com/locate/comgeo

## Exx do o r donr -n r xsons

####### Elvan Ceyhan *

Department of Mathematics, Koç University, 34450 Sariyer, Istanbul, Turkey

## ARTICLE INFO

###### ABSTRACT

Article history: Received 11 March 2009 Accepted 25 May 2010 Available online 27 May 2010

Communicated by R. Fleischer

Keywords:

Class cover catch digraph (CCCD)

Delaunay triangulation

Proximity map Proximity catch digraph Random graph Relative density Triangle center

## 1. Introduction

Classification and clustering have received considerable attention in the statistics and probability literature. In recent years, a new classification approach which is based on the proximity maps that incorporate the relative positions of data points from various classes has been developed. Proximity maps and the associated (di)graphs are used in disciplines where shape and structure are crucial. Examples include computer vision (dot patterns), image analysis, pattern recognition (prototype selection), geography and cartography, visual perception, biology, etc. Proximity graphs were first introduced by Toussaint [25], who called them relative neighborhood graphs. From a mathematical and algorithmic point of view, proximity graphs fall under the category of computational geometry.

A general definition of proximity graphs is as follows: Let V be any finite or infinite set of points in Rd where d is a positive integer. Each (unordered) pair of points p, q ∈ V is associated with a neighborhood N(p, q) ⊆ Rd. Let  be a property defined on X = {Ω(p, q): p, q ∈ V}. A proximity (or neighborhood) graph Gn,p (V, E) defined by the property  is a graph with the vertex set V and the edge set E such that pq ∈ E iff M(p, q) satisfies property . Examples of the most commonly used proximity graphs are the Delaunay tessellation, the boundary of the convex hull, the Gabriel graph, the rlt s     dr ule  ulds t   Sss ul an r  eor example, the relative neighborhood graph of V RNG(V), is a prominent representative of the family of graphs which are defined by some sort of neighborliness. The graph RNG(V) has vertex set V and edge set which are exactly the pairs pq of points for which p ≠ q and d(p, q) ≤ minν∈v max(d(p, v), d(q, ν)). That is, pq is an edge of RNG(V) iff Lune(p, q) does

* Tel.: +90 (212)3381845, fax: +90 (212)3381559. E-mail address: elceyhan@ku.edu.tr.

Proximity regions (and maps) are defined based on the relative allocation of points from two or more classes in an area of interest and are used to construct random graphs called proximity catch digraphs (PCDs) which have applications in various fields. The simplest of such maps is the spherical proximity map which gave rise to class cover catch digraph (CCCD) and was applied to pattern classification. In this article, we note some appealing properties of the spherical proximity map in compact intervals on the real line, thereby introduce the mechanism and guidelines for defining new proximity maps in higher dimensions. For non-spherical PCDs, Delaunay tessellation (triangulation in the real plane) is used to partition the region of interest in higher dimensions. We also introduce the auxiliary tools used for the construction of the new proximity maps, as well as some related concepts that will be used in the investigation and comparison of these maps and the resulting PCDs. We provide the distribution of graph invariants, namely, domination number and relative density, of the PCDs and characterize the geometry invariance of the distribution of these graph invariants for uniform data and provide some newly defined proximity maps in higher dimensions as illustrative examples.

© 2010 Elsevier B.V. All rights reserved.


<!-- p:2 -->


not contain any other points of V, where Lune(p, q) is defined as the intersection of two balls centered at p and q each with radius d(p, q). See, e.g., [14] and [2] for more detail.

A digraph is a directed graph, i.e., a graph with directed edges from one vertex to another based on a binary relation. Then the arc from vertex p to vertex q is denoted by the ordered pair (p, q) ∈ V × V. For example, the nearest neighbor (di)graph in [20] is a proximity digraph. The nearest neighbor digraph, denoted as NND(V), has the vertex set V and (p, q) is t      t t         n   n       )

The proximity catch digraphs (PCDs) are based on the property  that is determined by the following mapping which is defined in a more general space than Rd. Let (Ω, M) be a measurable space. The proximity map N(·) is given by N : Ω → ®(Ω), where ®(Ω) is the power set of Ω, and the proximity region of x ∈ Ω, denoted as N(x), is the image of x ∈ Ω under N  t      \            t        td  tex set V = {p1, p2, . . . , pn} and the arc set A is defined as (pi, pj) ∈ A iff pj ∈ N(pi) for i ≠ j. Notice that D depends on the proximity map N(·); and if pj ∈ N(pi), then N(p) is said to catch p j. Hence the name proximity catch digraph. If arcs of the s)  os   dd   o  o    (s  (d  on)

In a digraph D = (V, A), a vertex ν ∈ V dominates itself and all vertices of the form {u: (v, u) ∈ A}. A dominating set SD for the digraph D is a subset of V such that each vertex ν ∈ V is dominated by a vertex in SD. A minimum dominating set S* is a dominating set of minimum cardinality and the domination number γ(D) is defined as γ(D) := |S*| where |·I denotes the set cardinality functional. Priebe et al. [21] introduced the class cover catch digraphs (CCCDs) and gave the exact and the asymptotic distribution of the domination number of the CCCD based on two data sets Xn and Ym both of which are random samples from uniform distribution on a compact interval in R. DeVinney et al. [12], Marchette and Pri       te      n '   rd  ted relatively good performance of CCCDs in classification. The methods employed involve data reduction (condensing) by using s s ng ss ns  s t s ng ms s ng se sns n mntn mn NP-hard problem – in particular, for CCCDs – (see [10]).

Although intuitively appealing and easy to extend to higher dimensions, the exact and the asymptotic distribution of the domination number of the CCCDs are not analytically tractable in multiple dimensions. As alternatives to CCCD, Ceyhan and Prt ra  d  ne d s     dt n r c  ned a parametrized family of PCDs called proportional-edge PCDs and used the domination number of this PCD with a fixed pda son o sestt o a   s o st tn an St  sio is the pattern in which points of one class tend to cluster together, i.e., form one-class clumps. On the other hand, association is the pattern in which the points of one class tend to occur more frequently around points from the other class. The relative (arc) density of the proportional-edge PCDs is also used for testing the spatial patterns in [8]. The parametrized version of t       nd   n s   s   s  s  to o  se   t      s         si    enn digraph. These new families (other than CCCDs) are applicable to pattern classification also and are designed to have better distributional and mathematical properties. Ceyhan and Priebe [6] derived the asymptotic distribution of the domination number of proportional-edge PCDs for uniform data for the entire range of the parameter. Ceyhan [3] discusses the use of the domination number of proportional-edge PCDs, whose asymptotic distribution was computed in [6] for testing spatial patterns. Domination number (relative density) approach is applicable for testing spatial patterns, since under segregation the domination number tends to be small (large), and under association it tends to be large (small). An extensive treatment of the PCDs based on Delaunay tessellations is available in [1].

In this article, we determine some appealing properties of the spherical proximity region (i.e., the proximity region associated with CCCD) for uniform data in R and use them in introducing the mechanism and guidelines for defining new p  t  n                ornd as do  oi ar do  ( on di donr o    dons we expect the new PCDs will behave in a similar fashion. Furthermore, we introduce some auxiliary tools used for the c n   o      o    's d    oon comparison of the proximity maps. Additionally, we discuss the conditions for the geometry invariance for uniform data in triangles. Although the proportional-edge and central similarity PCDs were introduced before, their comparison and assessment in terms of the appealing properties were not done. We also introduce two new PCD families.

Throughout the article, d(x, y), can be any distance in Rn. Furthermore, the distance between a point x and a set A is defined as d(x, A) := infy∈A d(x, y); and the distance between two sets A and B is defined as d(A, B) := inf(x,y)∈A×B d(x, y). We describe the data-random PCDs and the related concepts such as Voronoi diagram and Delaunay tessellation, provide tns s s rrin ng g g ns  ns s  rs g r r ans e e   en s  en   on  eo   en s    eoon 'nl  s o o  m o  o     n o    i oon and discussion and conclusions in Section 6. We also provide a list of the new concepts and their notation in Appendix A for quick reference.


<!-- p:3 -->


Fig. 1. Plotted are the class  points (circles) and class χ points {x0, x1, x2, x3} (solid squares). The proximity region Ny (x0) in general form for an x0 (left) and spherical proximity region (right) and the corresponding arcs from x0 to other points in {x0, x1, x2, x3}.

17


0.8


0.6


0

o

Ny(x0) = B(x0, r(x0))

0.4

Ny(xo)

0.4

x0

x2

x0

■ x2

0.2


o

■x3

o

x3

0

0.2

0.4

0.6

0.8

0

0.2

0.4

0.6

0.8

## 2. Data-random proximity catch digraphs and related concepts

In particular, the proximity regions are constructed using data sets from two classes, X and . Given Ym ⊆ Ω from class , the proximity map Ny(·) : Ω → ®(Ω) associates a proximity region Ny(x) ⊆ Ω with each point x ∈ Ω. The region Ny(x) is defined in terms of the relative position of x with respect to points from m. Two examples of Ny (x) are presented in Fig. 1, where the corresponding proximity region in the left has a general shape, while in the right it is spherical. If Xn = {X1, X2, . .. , Xn} is a set of Ω-valued random variables from class χ, then Ny(X) are random sets. If Xi are independent identically distributed (iid) and if different X induce different Ny(X) a.s., then Ny(X) are iid as well. The data-random PCD D − associated with Ny(·) − is defined with vertex set χn and arc set A by (X, Xj) ∈ A iff Xj ∈ Ny(X). See Fig. 1. Since this relationship is not symmetric, a digraph is used rather than a graph. The random digraph D depends s ()  :(()  ) = (  ( ) =: (  ( d        (d)  ) the probability of having an arc from X to Xj, hence is called arc probability for the PCD based on Ny.

Notice that the CCCDs are defined with (open) balls only, whereas PCDs are not based on a particular geometric shape or a functional form; that is, PCDs admit Ny(·) to be any type of region, e.g., circle (ball), arc slice, triangle, a convex or nonconvex polygon, etc. In this sense, the PCDs are defined in a more general setting compared to CCCDs.

The PCDs are closely related to the proximity graphs of [14] and might be considered as a special case of covering sets of [26] and intersection digraphs of [24]. This data-random proximity digraph is a vertex-random proximity digraph which is not of standard type (see, e.g., [13]). The randomness of the PCDs lies in the fact that the vertices are random with joint probability density function (pdf) fx,y, but arcs (X, Xj) are deterministic functions of the random variable Xj and the set Ny(X). For example, the CCCD of [21] can be viewed as an example of PCD with Ny(x) being the ball B(x, r(x)) centered at x with radius r(x), where r(x) := miny∈m d(x, y). The CCCD is the digraph of order n with vertex set Xn and an arc from X to Xj iff Xj ∈ B(X, r(X)). See Fig. 1 (right). That is, there is an arc from X to Xj iff there exists an open ball centered at X which is "pure" (or contains no elements) of Ym, and simultaneously contains (or "catches") point Xj.

### 2.1. The appealing properties of spherical proximity regions in R

Let m = {y1, y2, . . . , Ym} ⊂ R and Yi:m be the ith order statistic (i.e., ith smallest data point in Ym). Then the proximity map associated with CCCD is defined as the open ball Ns(x) := B(x, r(x)) for all x ∈ R \ m, where r(x) = miny∈m d(x, y) with d(x, y) being the Euclidean distance between x and y [21]. See, e.g., Fig. 2. For x ∈ Ym, define Ns(x) = {x}. Notice that Ns(x) is a sphere for x ∉ Ym in higher dimensions, hence the name spherical proximity map and the notation Ns. Furthermore, dependence on m is through r(x). Note that, this proximity map is based on the intervals Ii = (y(i–1):m, Yi:m) for i = 1, 2, . . . , (m + 1) with the additional notation that y0:m = −∞ and y(m+1):m = ∞.

The CCCDs in R have desirable properties such as the finite sample and asymptotic distributions of the domination number being available. In this section, we determine some appealing properties of the proximity map associated with cu  s   i s d n     s n    nr  dps in higher dimensions. Potentially these properties make the CCCD to behave so "nicely" in R and the more they are satisfied by the new PCDs in higher dimensions, the more likely the new PCDs to have similar behavior.


<!-- p:4 -->


Fig. 2. Depicted are class  points {y1, y2, y3} (solid squares) and class Xχ points {x0, x1, x2, X3, x4} (solid circles) on the real line. The spherical proximity regions for x0 and x3 and the corresponding arcs are also presented.

r(xo)

y1

x0

x1

x2

y2

εx

x4

y3

B(xo, r(xo))

iid For Xi ~ U(Ii), the uniform distribution on I, without loss of generality, we can assume Ii = (a, b) with a, b ∈ R and a &lt; b. Then the arc probability pa(Ns) = P(X2 ∈ Ns(X1)) = 1/2, since

$$(a+b)/22x1−a b b P(X2 ∈ Ns(X1)) = ∫∫(b−a)−2dx2dx1+ a a (a+b)/22x1−b$$

Observe that the arc probability is independent of a and b, hence the interval I. Below are some appealing properties of the proximity map Ns(x) in R (for m &gt; 1):

- P1: The region Ns(x) is well-defined for all x ∈ CH (m) = [y1:m, ym:m].
- P2: For all x ∈ CH(m), we have χ ∈ Ns(x).
- P3: The point x is at the center of Ns(x) for all x ∈ CH(m).
- P4: For x ∈ Ii ⊆ CH(m), Ns(x) and I are of the same type; i.e., they are both intervals.
- P5: For χ ∈ Ii ⊆ CH (m), Ns(x) mimics the shape of Ii; i.e., it is (geometrically) similar to Ii.
- P7: For χ ∈ Ii and y ∈ Ij with i ≠ j, Ns(x) and Ns(y) are disjoint regions.
- P6: For x ∈ I, Ns(x) is a proper subset of Ii for all x ∈ I \ {(y(i−1):m + yi:m)/2} (or almost everywhere in Ii).
- P8: The size (i.e., measure) of Ns(x) is continuous in x; that is, for each ε &gt; 0 there exists a δε &gt; 0 such that |Ns(y)| − |Ns(x)|| &lt; ε whenever |d(x, y)| &lt; δε.

P9: The arc probability pa(Ns) does not depend on the support interval for uniform data in R.

Notice that Ns satisfies the properties P1, P2, and P3 for all x ∈ R provided that m ≥ 1. Property P9 implies that not only the arc probability but also the distribution of the relative arc density and domination number do not depend on the support int (  s s st  r   s s ec t     aoor Ns in R, it suffices to work with U(0, 1) data, and in higher dimensions (in R2) we will be able to consider only uniform data in a standard d-dimensional polytope (an equilateral triangle) for PCDs based on proximity maps that satisfy P9.

Notice that Ns(·) satisfies only P1, P2, P3, and P8 in Rd with d &gt; 1. Properties P4 and P5 fail, since Ns(x) is a sphere for l            ((         -( + Ns(y) might overlap for x, y from two distinct cells (see Fig. 5), hence P7 is violated. The arc probability pa(Ns) depends on the support set Ti for d &gt; 1, so P9 is violated.

Suppose we partition the convex hull of Ym, CH(m) by Delaunay tessellation. Let Ti be the ith Delaunay cell in the Delaunay tessellation of m for i = 1, 2, . . . , J. See Fig. 3. Note that P4 and P5 are equivalent when d = 1 for x ∈ CH (m), since any two (compact) intervals in R are (geometrically) similar. For d &gt; 1, P5 implies P4 only, since, for example, for d = 2 a Delaunay tessellation is a triangulation and any two triangles are not necessarily similar, but similar triangles are always of the same type as they are triangles.

Let Ω, i ∈ {1, 2, ..., J} be a partition on Ω and μ be the associated measure on Ω. The appealing properties meno   s  s s  r  sds  a oo      its measure μ [2].

Pr     s       d         s  as domination number equal to 1. So the measure of set of such points is of interest for the domination number of the PCDs.

(x :   } =:            t

For example, for Ω = Ii  R, Rs(Ns) := {x ∈ Ii: Ns(x) = Ii} = {(y(i−1):m + yi:m)/2}, and for Ω = Ti ⊆ Rd, Rs(Ns) := {x ∈ Ti: Ns(x) = Ti}. Note that for χ ∈ Ii, λ(Ns(x)) ≤ λ(Ii) and λ(Ns(x)) = λ(Ii) iff χ ∈ Rs(Ns) where λ(·) is the Lebesgue me-    (     e s  s  -     ue measure. Note also that Rs(Ns) is not a random set, but I(X ∈ Rs(Ns)) is a random variable. The property P6 is equivalent to Rs(Ns) having zero R-Lebesgue measure. Moreover, the larger the superset region, the more likely the relative density to be larger. On the other hand, for x ∈ ∂(Ii) = {y(i−1):m, yi}, the proximity region Ns(x) = {x} which has zero R-Lebesgue measure. When Ny(x) has zero measure, there is no arc from x to other points a.s. This suggests the following concept.


<!-- p:5 -->

o

0.8

0.6

o


0.4

0.2

0

0.2

0.4

0.6

0.8

### Voronoi Diagram

10

o


8

o


9.6

o


40

02

O

00

0.0

0.2

0.4

0.6

0.8

1.0

### Delaunay Triangulation

Fig. 3. Depicted are 10 points generated iid U(0, 1) × (0, 1) from class  (top), the corresponding Voronoi diagram (bottom left) and the Delaunay triangulation (bottom right).

10

0.8

6.6

0.4

02

00

0.0

0.2

0.4

0.6

0.8

1.0

Definition 2.2. Let (Ω, μ) be a measurable space. The Λ0-region for any proximity map N(·) is defined to be Λ0(N) := {x ∈ Ω: μ(N(x)) = 0}.

For Ω = Rd, Λ0(Ns) := {x ∈ Rd: λ(Ns(x)) = 0} = m. The notation Λ0-region is suggested by the fact that Ns(x) has zero Lebesgue measure for x ∈ Λ0(Ns).

Given a set Xn of size n in [y1:m, Ym:m] \ m, P7 implies that the number of disconnected components in the PCD based on Ns(·) is at least the cardinality of {i ∈ [m + 1]: Xn ∩ Ii ≠ Ø}, which is the set of indices of the intervals that contain some point(s) from Xn where [m] := {0, 1, 2, . . . , m − 1}.

The proximity region Ns(x) can easily be extended to multiple dimensions and is well-defined for all x ∈ Rd provided ts  s       s  nt  i     r    r problem [10] and the distribution of the domination number is not analytically tractable [1]. This drawback has motivated the definition of new families of proximity maps in higher dimensions. Note that for d = 1, such problems do not exist.


<!-- p:6 -->

10

+


#

+


++

+

十


10

+

十

8

6

十

+


++

十十

+


x×

+

4

十

+

十

+


十


+


十

+++

+


十


+


6.6

十

4

十

+

十


+


十

+

++

十

+


十十

+

土

十

++

+

十十

+

02

0.4

+

十

+

十

+

#

十

+


十十

+


4

十

+


4

+

x

十十

+


+ +

#

+

十


+


x×x

+

44

++++

十

+


++

+

十

40

02

#

+


4

+


十

+


+++

#

十

+


××


+

++

+十

+

0.0

+


十

+

十

+ +

+

++

+

00

0.0

0.2

0.4

0.6

0.8

1.0

0.0

0.2

0.4

0.6

0.08

1.0

Fig. 4. A realization of 200 points from class X (pluses) and the Delaunay triangulation based on 10 points from class  (circles) in Fig. 3 (left). Out of these 200 class X points, only 77 are in the convex hull of class  points (right).

### 2.2. Voronoi diagrams and Delaunay tessellations

Our next goal is to extend the PCD concept to higher dimensions and investigate the properties of the associated PCDs. The spherical proximity map in R is based on the intervals Ii = (Y(i−1):m, Yi:m) for i = 1, .. . , (m + 1). This intervalization can be viewed as a tessellation, since it partitions CH(m). For d &gt; 1, a natural tessellation that partitions CH(m) is the Delaunay tessellation, where each Delaunay cell is a (d + 1)-simplex. In R, the cell that contains x is implicitly used to define the spherical proximity map. More specifically, our proximity maps will be based on the relative position of points from class X' with respect to the Delaunay tessellation of the points from class . See [19] for more on Delaunay tessellations.

By definition a Delaunay tessellation of a finite set of points, P, is the dual of the Voronoi diagram based on the same set. The tessellation yields a (unique) polytopization provided that no more than (d + 1) points in Rd are cospherical (i.e., no more than (d + 1) points lie on the boundary of a (hyper)sphere in Rd). Moreover, the circumsphere of each Delaunay polytope (i.e., the sphere that contains the vertices of the Delaunay polytope on its boundary) is pure from the set P; i.e., the interior of the circumsphere of the Delaunay polytope does not contain any points from P. The Delaunay tessellation partitions CH(P). In particular, in R2, the tessellation is a triangulation that yields triangles Ti, i = 1, 2, ..., J (see, e.g., [19]) provided that no more than three points are cocircular (i.e., no more than three points lie on the boundary of some circle in R2). See Fig. 3 for an example with m = 10 class  points iid from U((0, 1) × (0, 1)). In this article we adopt the convention that a triangle refers to the closed region bounded by its edges.

The Delaunay triangles are based on a given set of points Ym. The set Ym can be assumed to come from a Poisson point Pdros e       o  s     s s s t  s rton based on a finite data set from a Poisson point process Poisson Delaunay tessellation and denote it Dp. The associated Voronoi diagram is called the Poisson Voronoi diagram and is denoted by Vp. For more detail on the properties of Vp, see [19].

Let c and r be the circumcenter and circumradius, respectively, of a (d + 1)-dimensional Poisson Delaunay cell in Rd. Then the (d + 1) vertices of the cell are the points {c + ru} where {u} are the unit vectors for i = 0, 1, 2, ... , d. The ergodic id l   l   l ssl l         t      t odr ona   i n    t m    m   d    n  n arle e  [1  d s  d ri  ices.

The non-spherical PCDs (i.e., PCDs other than CCCDs) we will consider in this article, will be defined only for X' points inside the convex hull of  points, CH (m), while the CCCDs are well-defined for all X' points provided m ≥ 1. See Fig. 4 for iid an example with n = 200 class X points ~ U((0, 1) × (0, 1)), and the Delaunay triangulation based on the 10 class  points in Fig. 3. This is actually the main advantage of the CCCDs for multi-dimensional data; but CCCDs suffer from the mathematical intractability of the calculation of the graph invariants of interest. On the other hand, the non-spherical PCDs, although restricted to CH(m), have more tractable graph invariants, which is their main advantage. Moreover, these non-spherical PCDs might allow one to work in one Delaunay cell (triangle in R2) only, if the corresponding proximity regions satisfy properties P7 and P9. The distribution of the graph invariants for the points outside the convex hull should be somehow corrected. For example, Ceyhan [3] suggests a correction coefficient to adjust the domination number of the proportionaledge PCDs. Such a correction can be derived for the relative density as well. The CCCDs were used for classification purposes in [22], and the non-spherical PCDs can be used for the same purpose in a similar fashion. However, since non-spherical PCDs we will consider are only defined for X' points inside the convex hull, a different strategy is required for points outside the convex hull. For example, one can use the PCD approach for the points inside, and employ some other method such as nearest neighbor classification for the points outside, hence the resultant classifier will be kind of a hybrid classifier.


<!-- p:7 -->


Fig. 5. The spherical proximity regions for 20 of the 200 class X points (small triangles) depicted in Fig. 4 (left).

10

△


8

△

AA

△

又

△

△△

∆∆

8

△


△4

△


4

又

△


△△

6

△


4

A

△


△△

△∆

△

△△

40

A

△

△△

A

△


02

△


X


△


A

Δ

△


∆△

A

△∆

△


00

△


△∆

0.0

0.2

0.4

0.6

0.8

1.0

The calculations in the convex hull may also be used to approximate the results for more general proximity regions. Gon    n on   on   n t  n x  o n  i we restrict the proximity region Ny(x) to the Delaunay cell that contains x, denoted N'y(x), then we will have a region satisfying P7 and so will need to do the calculations for Delaunay cells only. Moreover, the PCD based on N'γ (x) will be a subdigraph of the PCD based on Ny(x). Hence the domination number (relative density) of the PCD based on Ny(x) will be stochastically smaller (larger) than the PCD based on N',(x). So the calculations for the PCD based on N',(x) will be informative about the general PCD we start with.

### 2.3. Transformations preserving uniformity on triangles in R2

The property P9, when satisfied by a proximity region, suggests that in higher dimensions the arc probability of the corresponding PCDs based on uniform data would be geometry invariant, i.e., would not depend on the geometry of the support set. The set Xn is assumed to be a set of iid uniform random variables on the convex hull of Ym; i.e., a random san           ' r  &lt;     o   'd l (   orm random variables on Ti for i ∈ {1, 2, ... , J}, where Ti is the ith Delaunay triangle and J is the total number of Delaunay triangles. The geometry invariance property will reduce the triangle T as much as possible while preserving uniformity and the probabilities related to PCDs will simplify in notation and calculations. Below, we present such a transformation that reduces a single triangle to the standard equilateral triangle Te = T((0, 0), (1, 0), (1/2, √3/2)).

The triangle T(3) can be carried into the first quadrant by a composition of transformations in such a way that the largest edge has unit length and lies on the x-axis, and the x-coordinate of the vertex nonadjacent to largest edge is less than 1/2. We call the resultant triangle the basic triangle and denote it as Tb where Tb = T((0, 0), (1, 0), (c1, c2)) with 0 &lt; c1 ≤ 1/2, and c2 &gt; 0 and (1 − c1)2 + c2 ≤ 1. See Fig. 7 (left). We will describe such transformations below: Let ei be tha     s          }         cale the triangle so that e3 is of unit length. Next translate y1 to (0, 0), and if necessary rotate the triangle so that y2 = (1, 0). If the y-coordinate of y3 is negative reflect the triangle around the x-axis, then if the x-coordinate of y3 is greater than 1/2, reflect it around x = 1/2, then the associated basic triangle Tb is obtained by a transformation denoted by φb which is a

iid Let 3 = {y1, y2, y3} ⊂ R2 be three non-collinear points and T(3) be the triangle with vertices y1, y2, y3. Let X U(T (3)) for i = 1, 2, . . . , n. The pdf of U(T (3)) is f (u) = A(T()3) 1 I(u ∈ T(3)), where A(·) is the area functional.


<!-- p:8 -->


(  -  se  i    id  t    t   (     t  i    hit

C2


1/2

C1

1/2

C1

composition of some of the rigid motion transformations (namely translation, rotation, and reflection) and scaling. Hence if iid T(3) is transformed into Tb, then T(3) is similar to Tb and φb(T (3)) = Tb. Thus the random variables Xi ~ U(T(3)) iid a       (   s           an assume T(3) to be the basic triangle. If c1 = 1/2 and c2 = √3/2, then Tb is an equilateral triangle; if c2 &lt; √c1 − c2, then Tb is an obtuse triangle; if c2 = √c1 − c2, t , then Tb is a right triangle; and if c2 &gt; Vc1 − c2, then Tb is an acute triangle. If c2 = 0, then the Tb reduces to the unit interval (0, 1). See Fig. 6 for the domain of (c1, c2) for Tb and the part of the domain

on which Tb is a non-acute triangle.

Ian.  s  -t s    a an     d   t r p   e. pa(Ny) does not change under rigid motion transformations and does not depend on the scale of the support triangle T (V3).

Pro     :   s (lt   t l : ' lt   t t s   orm iid iid data, the set probabilities are calculated as the ratio of the area of the set to the total area. So P(X ∈ S ⊆ T(3)) = A(S)/A(T(3)) and P(φb(X) ∈ φb(S) ⊆ φb(T(3))) = P(φb(X) ∈ φb(S) ⊆ Tb) = A(φb(S))/A(Tb) = [kA(S)]/[kA(T(3))] = A(S)/A(T(3)) where k is the scaling factor. Letting X = Xj and S = Ny(X), the desired result follows. □

Based on Lemma 2.3, without loss of generality, we can assume T(3) to be the basic triangle T for uniform data.

2.3.1. Transformation of T to Te

Let φe : (x, y) → (u, ν), where u(x, y) = x + 1-2c1 y and ν(x, y) = √3 y. Then y1 is mapped to (0, 0), y2 is mapped to √3 2c2 (1, 0), and y3 is mapped to (1/2, √3/2). See also Fig. 7. Note that the inverse transformation is φ−1(u, v) = (x(u, v), y(u, v)) where x(u, ν) = u − (1−2c1) ν and y(u, ν) = 2C2 u. Then the Jacobian is given by √3 √3

h s t  s   n n t  i ni at s is i i only describe the transformation that maps T(3) to the standard equilateral triangle, Te = T((0, 0), (1, 0), (1/2, √3/2)) for exploiting the symmetry in calculations using Te.

$$\sqrt { 3 } & & \sqrt { 3 } & & \sqrt { 3 } \\ J ( x , y ) = \left | \begin{array} { c c c } \frac { \partial x } { \partial u } & \frac { \partial x } { \partial v } \\ \frac { \partial y } { \partial u } & \frac { \partial y } { \partial v } \\ \end{array} \right | = \left | \begin{array} { c c c } 1 & \frac { 2 c _ { 1 } - 1 } { \sqrt { 3 } } \\ 1 & \frac { \sqrt { 3 } } { \sqrt { 3 } } \\ 0 & \frac { 2 c _ { 2 } } { \sqrt { 3 } } \\ \end{array} \right | = \frac { 2 c _ { 2 } } { \sqrt { 3 } } .$$

So fu,v (u, v) = fx,y (φ−1(u, v))|J| = 4 I((u, v) ∈ Te). Hence uniformity is preserved. √3

Theorem 2.4. The arc probability pa(Ny) of the PCD based on Ny for uniform data on Tb is geometry invariant iff A(φe(Ny (x))) = A(Nφe() (φe(x))) for all x ∈ Tb where Nφe() is based on φe(V3).

Proof. By Lemma 2.3, the PCD based on Ny for uniform data on T(3) is rigid-motion and scale invariant. So T(3) can be transformed to Tb preserving the uniformity of the data and the arc probability for the associated PCD. For uniform data, the set probabilities are calculated as the ratio of the area of the set to the total area. Suppose the arc probability is geometry invariant. Then pa(Ny) = P(X ∈ Ny(x)) = P(φe(X) ∈ Nφe()(φe(x))). But P(X ∈ Ny(x)) = A(Ny(x))/A(Tb) and P(φe(X) ∈ Nφe()(φe(x))) = A(Nφe()(φe(x)))/A(Te). Moreover A(Ny(x))/A(Tb) = A(φe(Ny(x)))/A(φe(Tb)) = A(φe(Ny(x)))/A(Te) since the Jacobian cancels out and φe(Tb) = Te. Hence A(Nφe()(φe(x)))/A(Te) = A(φe(Ny (x)))/A(Te) implies A(φe(Ny(x))) = A(Nφe() (φe(x))) for all x ∈ Tb. The converse can be proved similarly. □


<!-- p:9 -->


Fig. 7. The description of φe (x, y) for (x, y) ∈ Tb (left) and the equilateral triangle φe (Tb) = Te (right).

φe(y3)

N3 = (c1, c2)

y

φe(x, y)

(x, y)

y1 = (0, 0)

y2 = (1, 0)

φe(y1) = (0, 0)

φe(y2) = (1, 0)

x

u

Corollary 2.5. If φe (Ny (x)) = Nφe () (φe (x)) for all x ∈ Tb, then the arc probability pa(Ny) of the PCD based on Ny for uniform data on T is geometry invariant.

Proof. Let χ ∈ Tb. Then φe(Ny(x)) = Nφe()(φe(x)) implies A(φe(Ny(x))) = A(Nφe()(φe(x))). Hence the result follows by Theorem 2.4. □

### 2.4. Vertex and edge regions

The new proximity maps will be based on the Delaunay cell Ti that contains x. The region Ny(x) will also depend on the location of x in Ti with respect to the vertices or faces (edges in R2) of T. Hence for Ny (x) to be well-defined, the vertex or face of T associated with x should be uniquely determined. This will give rise to two new concepts: vertex regions and face regions (edge regions in R2).

#### 2.4.1. Triangle centers

Thn      r  s 'd d  n        e center. The trilinear coordinates of a point P with respect to T(3) are an ordered triple of numbers, which are proportional to the distances from P to the edges. Trilinear coordinates are denoted as (α : β : γ) and also are known as homogeneous coordinates or trilinears. By convention, the three vertices y1, y2, and y3 of T(3) are commonly written as (1 : 0 : 0), (0 :1 : 0), and (0 : 0 : 1), respectively (see [27]).

Definition 2.6. A triangle center is a point whose trilinear coordinates are defined in terms of the edge lengths and (inner) angles of a triangle. The function giving the coordinates (α : β : γ) is called the triangle center function.

Kimberling [15] enumerates 360 triangle centers, among which four have been widely known since the ancient times; namely, circumcenter (Mcc), incenter (M), center of mass or centroid (Mcm), and orthocenter (Mo).

The trilinear coordinates of the circumcenter Mcc are (cosθ1 : cos θ2 : cos θ3) where θ is the inner angle of T(3) at vertex yi for i ∈ {1, 2, 3}. The circumcenter of a triangle is in the interior, at the midpoint of the hypotenuse, or in the exterior of the triangle, if the triangle is acute, right, or obtuse, respectively. See Fig. 8 where an acute and an obtuse triangle are depicted. Using the pdf of an arbitrary angle of a triangle Ti from Poisson Delaunay triangulation Dp [18], we see that, P(Ti is a right triangle) = P(θ = π /2) = 0, hence P(Mcc is the midpoint of the hypotenuse) = 0. Furthermore,

$$\text { see that, } P ( T _ { i } ; i \text { is a right triangle} ) = P ( \theta = \pi / 2 ) = 0 , \text { hence } P ( M _ { C C } \text { is the midpoint of the hypotenuse} ) = 0 . \text { Furthermore} \\ P ( T _ { i } ; \text { an obtuse triangle} ) = P ( M _ { C C } \notin T _ { i } ) = P ( \theta _ { \max } > \pi / 2 ) = \int _ { \pi / 2 } ^ { \pi } f _ { 3 } ( x ) d x \\ = \frac { 3 f _ { s } ( \sqrt { 2 \pi } ) - f _ { C } ( \sqrt { 2 \pi } ) - 3 f _ { s } ( \sqrt { \frac { \pi } { 2 } } ) + f _ { C } ( \sqrt { \frac { \pi } { 2 } } ) } { \sqrt { 2 \pi } } \approx . 0 3 7 2 6 \\ \intertext { where } \intertext { where } \intertext { \text { } f _ { 3 } ( x ) \text { is the pdf of the maximum angle and its given by } }$$

where f3(x) is the pdf of the maximum angle and is given by

$$f _ { 3 } ( x ) & = \left [ \frac { 2 } { \pi } \left ( 3 x ( \sin 2 x ) - \cos 2 x + \cos 4 x - \pi \sin 2 x \right ) \right ] \left ( \pi / 3 < x < \pi / 2 \right ) \\ & + \left [ \frac { 1 } { \pi } \left ( 4 \pi ( \cos x ) ( \sin x ) + 3 \sin x ^ { 2 } - \cos x ^ { 2 } - 4 x ( \cos x ) ( \sin x ) + 1 \right ) \right ] \left ( \pi / 2 < x < \pi \right ) ,$$


<!-- p:10 -->

y3


0.2

0.6

M2

M3

-0.2

y1

0.2

0,4 M1O,6

0.8

1y2 12

0

0.4

M3

M2

cc

-02

0.2

Mcc


rCC

-0.4

y1

y2

-0.2

0.2

0.4

M0.6

0.8

1.2

-0.6

-0.2

-0.8

Fig. 8. The circumcircle, circumcenter Mcc, and circumradius rcc of an acute triangle (left) and an obtuse triangle (right). Mi is the midpoint of edge ei, for i = 1, 2, 3.

0.7

y3

F

y3

0.6


0.5


P2

0.4

P3

0.4

M3

M2

0.3


M1

MCM

0.2

rI

0.2

0.1


y1

0

0.2

0.6

0.8

1

y2

y1

0

0.2

0.4

M1

0.6

0.8

1

y2

0.4\_1

Fig. 9. The incircle, incenter M1, inradius r1 of a triangle (left) and the centroid or center of mass of a triangle (right). Pi is the point where the incircle is tangent to edge ei for i = 1, 2, 3.

fc (x) = ∫0 cos(πt2/2) dt, and fs(x) = ∫ Ssin(πt2/2) dt are the Fresnel cosine and sine functions, respectively. The coordinates cf-c1+c2 2C2

The incenter M1 and has trilinear coordinates (1 : 1 : 1). See Fig. 9 (left). The coordinates of M, for the basic triangle Tb are (x1, y1), where

$$c _ { 1 } - \sqrt { c _ { 1 } ^ { 2 } + c _ { 2 } ^ { 2 } } & & y _ { l } = \frac { c _ { 2 } } { 1 + \sqrt { c _ { 1 } ^ { 2 } + c _ { 2 } ^ { 2 } } + \sqrt { ( 1 - c _ { 1 } ) ^ { 2 } + c _ { 2 } ^ { 2 } } } , & y _ { l } = \frac { c _ { 2 } } { 1 + \sqrt { c _ { 1 } ^ { 2 } + c _ { 2 } ^ { 2 } } + \sqrt { ( 1 - c _ { 1 } ) ^ { 2 } + c _ { 2 } ^ { 2 } } } . \\ \text {Unlike the arrows} & \text {, } & y _ { l } = \frac { c _ { 2 } } { 1 + \sqrt { c _ { 1 } ^ { 2 } + c _ { 2 } ^ { 2 } } + \sqrt { ( 1 - c _ { 1 } ) ^ { 2 } + c _ { 2 } ^ { 2 } } } .$$

Unlike the circumcenter, the incenter is guaranteed to be inside the triangle.

The median line of a triangle is the line from one of its vertices to the midpoint of the opposite edge. The three median lines of any triangle intersect at the triangle's centroid (i.e., center of mass), denoted as Mcm. See Fig. 9 (right). It has trilinear coordinates (1/|e1|: 1/|e2| : 1/|e3|) or (cscθ1 : cscθ1 : cscθ1) where e denotes the edge opposite to the vertex yi for i ∈ {1, 2, 3}. The centroid is also guaranteed to be in the interior of the triangle. The coordinates of Mcm in the basic triangle are ((1 + c1)/3, c2/3).

Note that in an equilateral triangle, M1 = Mcc = Mo = Mcm (i.e., all the centers we have described coincide).

The intersection of the three altitudes of a triangle is called the orthocenter, Mo, which has trilinear coordinates (cos θ2 cos θ3 : cos θ1 cos θ3 : cos θ1 cos θ2). The orthocenter of a triangle is in the interior, at vertex y3, or in the exterior of the basic triangle, Tb, if T is acute, right, or obtuse, respectively. The functional form of Mo in the basic triangle is (c1, c1(1 − c1)/c2).


<!-- p:11 -->

F

y3

F

y3

0.6


0.5


RCM(y3)

RM(y3)

PCM

0.4

M2

M1

0.4

PCM/

1

2

0.3


MCM


0.2

RcM(y1)

RCM(y2)

0.2

Rm(y1)

RM(y2)

0.1


y1

y2

y1

y2

0.2

0.4M3

0.6

0.8

1

0

0.2

0.4

0.8

1

3

Fig. 10. The Mcm-vertex regions with median lines (left) and with orthogonal projections (right). PCM is the point where the orthogonal projection from Mcm crosses edge ei for i = 1, 2, 3.

#### 2.4.2. Vertex regions

Recall that for x ∈ T(3), Ns(x) = B(x, r(x)) where r(x) = miny∈y3 d(x, y). That is, r(x) = d(x, y) iff x ∈ Vc (y) ∩ T(3) for i ∈ {1, 2, 3}, where Vc(y) is the Voronoi cell generated by yi in the Voronoi diagram based on Y3. Notice that these cells partition the triangle T(3) and each Vc (y) ∩ T(3) is adjacent only to vertex yi and their intersection is the point M which is equidistant to the vertices. So M is in fact the circumcenter, Mcc, of T(3). To define new proximity regions based on some sort of distance or dissimilarity relative to the vertices Y3, we associate each point in T(3) to a vertex ot   e    t          ds   e   the vertex region based on the closest vertex, argminy∈y3 d(x, y). If two vertices were equidistant from x (i.e., argminy∈3 d(x, y) were not unique), x is arbitrarily assigned to a region of one of them. In fact, for Ns, by construction, it would not matter which vertex to pick when the vertices are equidistant to x, the region Ns(x) will be the same.

Definition 2.7. The connected regions that partition the triangle, T(3) (in the sense that the intersections of the regions have zero R2-Lebesgue measure) such that each region has one and only one vertex of T(3) on its boundary are called vertex regions.

This definition implies that there are three vertex regions. The vertex regions can be constructed starting with a point M ∈ R2\3. Join the point M to a point on each edge by a curve such that the resultant regions satisfy the above definition. Such regions are called M-vertex regions and we denote the vertex region associated with vertex y as Rm(y) for y ∈ 3. In ar   n  ng       s o  (   o    o  n t thought as being "closer" to y than to the other vertices.

It is reasonable to require that the area of the region Rm(y) gets larger as d(M, y) increases. Usually the curves will be taken to be lines or even the orthogonal projections to the edges. But these lines do not necessarily yield three vertex regions for M in the exterior of T(3). Unless stated otherwise, M-vertex regions will refer to regions constructed by joining M to the edges with straight line segments, henceforth.

We construct M-vertex regions by straight lines in the following two ways:

Method I: with the extensions of the line segments joining y to M: Let T(3)o denote the interior of the triangle T(3). M-vertex regions with M ∈ T(3)° can be constructed by using the extensions of the line segments joining y to M for each y ∈ 3. See Fig. 10 (left) with M = Mcm. The functional forms of RM (y) for i ∈ {1, 2, 3} with M = (m1, m2) and m1 &gt; c1 in the basic triangle, Tb, are provided in [2]. If x falls on the boundary of two M-vertex regions, then x is arbitrarily assigned to one of the M-vertex regions.

Method II: with the orthogonal projections from M to edges: In this method, we draw the orthogonal projections from M to the edges to obtain the vertex regions denoted as R (y). For instance see Fig. 10 (right) with M = Mcm. The functional fot  r ro  t nl   od o rt  t e    =      ono the edges does not necessarily fall on the boundary of T(Y3). For example, letting PM be the orthogonal projection of M to edge e2, it is easy to see that PM might fall outside T(3) which contradicts the definition of vertex regions. In fact PM M ∈ e2 iff c2(m2c2+c1m1) ≤ c2 iff c2(c2 − m2) + c1(c1 − m1) ≥ 0. By definition, Ro (y) and R (y) are identical. But, for c2+c2 M ∈ {Mcm, Mcc, M1}, RM (y) can have both versions.

We define and provide the explicit forms of Mcc-vertex regions, Mcm-vertex regions, and M-vertex regions in [2]. See also Fig. 11 for Mcc-vertex regions with Method II (i.e., with orthogonal projections) for acute and obtuse triangles; and Fig. 12 M-vertex regions with Methods I and II.


<!-- p:12 -->

F

y3

0.6

0.5

0.2

y3

0.4

M2

Rcc(y3)

M1

M2

M1

0.1

Rcc(y3)

0.3

y1

0.2

0.4

M30.6

0.8

1y2

O

0.2

Rcc(y1)

Rc(y2)

Mcc

-0.1

0.1

Rc(y1)

Rc(y2)

-0.2

y1

y2

0

0.2

0.4

M3

0.6

0.8

1

-0.3

Mcc

Fig. 11. The Mcc-vertex regions with orthogonal projections in an acute triangle (left) and in an obtuse triangle (right).

7

y3

7

y3

0.6


0.5


R1(y3)


0.4


0.3


MI


0.2

R1(y1)

R1(y2)

0.2

R1(y1)

R(y2)

0.1


y1

y2

y1

y2

0.2

0.4

0.6

0.8

1

0.2

0.4

0.6

0.8

1

Fig. 12. The M1-vertex regions with extension of the line segments joining the vertices (i.e., with Method I) to M, (left) and with orthogonal projections (i.e., with Method II) (right).

#### 2.4.3. Edge regions

The spherical proximity region seen earlier is constructed by using the vertex region based on the closest vertex, argminy∈y3 d(x, y). One can also use the closest edge, argmini∈{1,2,3} d(x, ei), in defining a proximity region, which suggests the concept of edge regions. While using the edge argmini∈{1,2,3) d(x, e), the triangle is again partitioned into three regions whose intersection is some point M with Euclidean distance to the edges d(M, e1) = d(M, e2) = d(M, e3), so M is in fact the incenter of T(3) and d(M, e) = r1 is the inradius.

Definition 2.8. The connected regions that partition the triangle, T(O3), in such a way that each region has one and only one edge of T(V3) on its boundary, are called edge regions.

Thin             t    a   sinn fact, one can describe the edge regions starting with M. Join the point M to the vertices by curves such that the resultant regions satisfy the above definition. Such regions are called M-edge regions and the edge region for edge e is denoted as Rm(e) for e ∈ {e1, e2, e3}. Unless stated otherwise, M-edge regions will refer to the regions constructed by joining M to the vertices by straight lines, henceforth. In particular, one can use a center of T(3) for the starting point M. See Fig. 13 for M-edge regions with M = Mcm and M = M1. One can also consider the points in Rm(e) to be "closer" to e than to the other edges. Furthermore, it is reasonable to require that the area of the region Rm(e) get larger as d(M, e) increases. In higher dimensions, the corresponding regions are called "face regions".

Below are the results about the geometry invariance of vertex- and edge-regions.

The functional forms of Rm(e) for i ∈ {1, 2, 3}, for M = (m1, m2) ∈ T(3)° and m1 &gt; c1 in the basic triangle are provided in [2]. If x falls on the boundary of two M-edge regions, then it is arbitrarily assigned to one of the M-edge regions. The center of mass edge regions (Mcm-edge regions) and other edge regions are described in detail in [2].


<!-- p:13 -->


Fig. 13. The M-edge regions with M = Mcm (left) and M = M1 (right).

y3

7F

y3

0.6


0.5


0.4


0.3

RcM(e2)

RcM(e1)

0.3

RI(e2)

R1(e1)

MI

MCM

0.2


RI(e3)

0.1

RcM(e3)

0.1

y1

y2

y1

y2

0

0.2

0.4

0.6

0.8

1

0.2

0.4

0.6

0.8

1

Definition 2.9. The M-edge regions are said to be geometry invariant if φe(RM(ei)) = Rφe(M)(φe(ei)) for i = 1, 2, 3 where φe is the transformation defined in Section 2.3.1. The M-vertex regions are said to be geometry invariant if φe(Rm(yi)) = Rφe(M)(φe (yi)) for i = 1, 2, 3.

As a corollary to Theorem 2.4, we obtain the following.

Corollary 2.10. Suppose Ny is based on geometry invariant edge or vertex regions. If the proximity regions are based on boundary of T (3) and parallel lines to edges, then geometry invariance of the arc probability for uniform data follows.

rot  ((  n = ((x  ts      e   s r n nek desired result holds by Corollary 2.5.

Corollary 2.11. If the edge or vertex regions are based on specific angles in Tb in the sense that they have specific (inner) angular values, then these regions are not geometry invariant. Similarly, if the proximity regions are based on specific angles in Tb then they are not geometry invariant either.

Proof. The transformation φe clearly does not preserve the angles in T. Hence the regions dependent on (inner) angles of Tb fail to be preserved. □

## 3. Families of proximity regions in Delaunay tessellations

tn   n os on  oo s nn    l on t  o   o    m. That is, Ω = CH (m) and Ωi = Ti with μ being the Lebesgue measure. Then the appealing properties for proximity regions in Section 2.1 can be extended to this special case also [2].

For illustrative purposes, we focus on R2, where a Delaunay tessellation is a triangulation, provided that no more than three points of Ym are cocircular. Let Xn be a random sample from F with support S(F) ⊆ T(3). The spherical proximity map is the first proximity map defined in the literature (see [12,17,22,23,11]) where Mcc-vertex regions with Method II wei '  i o- o i      r    i    wo families of proximity regions for which P4 and P5 will automatically hold, and introduce two new families of proximity regions.

### 3.1. Arc-slice proximity maps

Recall that for Ns(·), P7 is violated, since for any x ∈ Ti ⊂ Rd, B(x, r(x))  Ti, which implies that two proximity regions Ns(x) and Ns(y) might overlap for x and y in two distinct cells. See, e.g., Fig. 5. Such an overlap of the regions make the distribution of the domination number of the PCD associated with Ns(), if not impossible, hard to calculate. In order to avoid the overlap of regions B(x, r(x)) and B(y, r(y)) for x, y in different Delaunay cells, the balls are restricted to the corresponding cells, which leads to arc-slice proximity regions, NAs(x) := B(x, r(x)) ∩ Ti, where B(x, r(x)) is the closure of the ball B(x, r(x)). The closed ball is used in the definition of the arc-slice proximity map for consistency with the other proximity maps that will be defined on Delaunay cells. The arc-slice proximity map NAs(x) is well-defined only for points in CH (m), provided that m is in general position and m ≥ (d + 1) in Rd.

By construction, the Mcc-vertex regions with Method II are implicitly used, since x is in the Mcc-vertex region of y iff y = argminu∈ym d(x, u). To make this dependence explicit, we will use the notations NAs(·, Mc) and Rc(y) for the


<!-- p:14 -->

F

y3

0.6

0.5

0.4

M2

M1

0.3

0.2

0.1

y1

y2

0

0.2

0.4

M30.6

0.8

1

x

Fig. 14. The region NAs (x, MC) with an x ∈ Rcc (y2).

proximity region and the vertex region, respectively. See Fig. 14 for NAs(x, Mc) for an x ∈ Rc(y2). The properties P1, P2, P7 hold by definition. Notice that NAs (x, MC) ⊆ T(3) for all x ∈ T(3) and NAs (x, MC) = T(3) iff x = MCcc, since B(x, r(x)) ⊃ T(3) only when x = Mcc. Hence the superset region for arc-slice proximity maps with Mcc-vertex regions Id    tt  ottt  t,    :   tt, {tt} == t t c, i follows. Furthermore, P8 holds since the area A(NAs(x, Mc)) is a continuous function of r(x) = miny∈3 d(x, y) which is o t      s         d NAs(x, Mc) for a realization of 7 class X points in the one triangle case, and for the realization of 77 class X points in the multi-triangle case in Fig. 4 (right).

One can define arc-slice proximity regions with any type of M-vertex regions with Method II as

NAs (x, M−) := B(x, r(x)) ∩ T (3) where r(x) := d(x, y) for χ ∈ RM (y).

But for M ≠ Mcc, NAs(·, M↓) satisfies only P1, P2, and P7, property P6 fails to hold, since R(NAs, M) has positive area, and P8 fails, since the size of NAs(x, M−) is not continuous in x. See [2] for illustrations of R(NAs, M) with M = Mcm and M = MI.

The arc-slice proximity regions can also be defined with M-vertex regions constructed as in Method I (i.e., with the extensions of the line segments joining M to the vertices). Such proximity regions are denoted as NAs(x, M) as opposed to NAs(x, M|). The NAs(·, M) satisfies the same properties as NAs(·, M|), except property P8. That is, NAs(·, M) violates property P8 for all M.

In terms of the appealing properties in Section 2.1, NAs(·, Mc) is the most appealing proximity map in the family NAs := {NAs(·, M): M ∈ R2 \ 3} ∪ {NAs(·, M⊥): M ∈ R2 \ 3}. Moreover, Λ0(NAs, M) = 3 for all M ∈ R2 \ 3, since λ(NAs(χ, M)) = 0 iff χ ∈ Y3.

### 3.2. Proportional-edge proximity maps

The first type of triangular proximity map we will consider is the proportional-edge proximity map. For this proximity map, the asymptotic distribution of domination number and the relative density of the corresponding PCD has mathematical tractability. See [5,6,8].

For the expansion parameter r ∈ [1, ∞], define NpE(·, M) := N(·, M; r, 3) to be the proportional-edge proximity map with M-vertex regions obtained as in Method I as follows (see also Fig. 16 with M = Mcm and r = 2). For x ∈ T(3) \ 3, let v(x) ∈ 3 be the vertex whose region contains x; i.e., x ∈ Rm(v(x)). If x falls on the boundary of two M-vertex regions, v(x) arbitrarily assigned. Let e(x) be the edge of T(3) opposite v(x). Let l(v(x), x) be the line parallel to e(x) through x. Let d(v(x), l(v(x), x)) be the Euclidean distance from v(x) to l(v(x), x). For r ∈ [1, ∞), let lr(v(x), x) be the line parallel to e(x) such that

$$d ( v ( x ) , \ell _ { r } ( v ( x ) , x ) ) = r d ( v ( x ) , \ell ( v ( x ) , x ) ) \quad \text {and} \quad d ( \ell ( v ( x ) , x ) , \ell _ { r } ( v ( x ) , x ) ) < d ( v ( x ) , \ell _ { r } ( v ( x ) , x ) ) .$$

Let Tr(x) be the triangle similar to and with the same orientation as T(3) having v(x) as a vertex and lr(v(x), x) as the opposite edge. Then the proportional-edge proximity region NE(x, M) is defined to be Tr(x) ∩ T(3). Notice that l(v(x), x) divides the edges of Tr(x) (other than lr(v(x), x)) proportionally with the factor r. Hence the name proportional edge proximity map and the notation NPE(·, M).


<!-- p:15 -->

7

10

6.6

05

8

0.4

0.3

96

02

01

40

00

0.0

0.2

0.4

0.6

0.8

1.0

02

0

0.0

0.2

0.4

0.6

0.08

1.0

Fig. 15. A realization of 7 class X points (small triangles) generated iid U(T(3)) and the corresponding arcs for NAs (x, M) (left). The arcs for arc-slice PCDs with NAs (x, Mc) for the 77 class X points that lie in the CH (10) (right) where the same 10 in Fig. 4 is used.

Y3

l2(v(x), x)

e(x)

l(v(x), x)

Mc

x

di

y2

y1 = v(x)

da

Fig. 16. Construction of proximity region, N2E(x) (shaded region) for an x ∈ Rcm (y1) where d1 = d(v(x), l(v(x), x)) and d2 = d(v(x), l2(v(x), x)) = 2d(ν(x), l(ν(x), x)).

Notice that r ≥ 1 implies x ∈ NPE (x, M). Furthermore, limr→∞ NpE(x, M) = T(V3) for all ∈ T (3)\ 3, so NpE (x, M) := T(     l     l    {} =:       s  s   (2) (x, MCm) in the PE one triangle and the multi-triangle cases.

F ins  ssrl f wd -t -on t t st  t t l  sl iid T(3), implies that the special case in the construction of NpE — X falls on the boundary of two vertex regions — occurs with probability zero. For such an F, NpE(X, M) is a triangle a.s. The functional form of NE(x, M) for x = (x0, yo) ∈ Tb is given in the technical report by [2].

Of particular interest is NPE with any M and r ∈ {√2, 3/2, 2}. For r = √2, l(v(x), x) divides T√2(x) into two regions of equal area, hence N √2 is also referred to as double-area proximity map. See, e.g., Fig. 19 (left) for an illustration of PE N √2 (x, M−). For r = 2, l(v(x), x) divides the edges of T2(x) − other than lr(v(x), x) − into two segments of equal length, PE hence N2 VpE is also referred to as double-edge proximity map. Se, e.g., Fig. 19 (right) for an illustration of N (x, M−). The superset region is empty for r &lt; 3/2, has positive area for r &gt; 3/2; and is {Mcm} for r = 3/2. Therefore, r = 3/2 is the

The proportional-edge PCDs based on vertex regions constructed as in Method II are denoted as NpE(x, M−) and the corresponding superset region is denoted as R (NPE, M). See Fig. 18 for the superset region R+(N2E, M) with M ∈ {MCc, M}. On the other hand, the superset region for NPE(x, M) is denoted as Rs(NE, M).


<!-- p:16 -->

10

8

7

40

02

00

0.0

0.2

0.4

0.6

0.8

1.0

Fig. 17. The arcs for N=2 (x, Mcm) the 7 class X points in Fig. 15, and the arcs for N=2 (x, Mcm) for the 77 class X points that lie in the CH(10) where the same 10 in Fig. 4 is used.

7F

y3

7

y3

0.6


0.5


0.4


M

M1

M2

2

M1

0.3


0.2


0.1


y1

y2

y1

PIC

3

y2

0

0.2

0.4

M30.6

0.8

1

0.2

0.4

0.6

0.8

1

M3

F.     d    () (     '(     (    e    rom M1 crosses edge ei for i = 1, 2, 3.

threshold for NpE(·, Mcm) (and NpE(·, MCM)) to satisfy P6. Furthermore, r = 3/2 is the value at which the asymptotic dis a t  t-n     n  d   tn o   s

As for P3, for T2(x) ⊆ T(3) one can loosen the concept of center by treating the line l(v(x), x) as the edge-wise central line, so P3 is satisfied in this loose sense for r = 2. Notice that x is not the unique center in this sense, but a point on a central line. Let T(M1, M2, M3) be triangle whose vertices are the midpoints of the edges M for i = 1, 2, 3. Then for any x ∈

For NE(x, M), the properties P1, P2, P4, P5, and P7 follow by definition for all M and r. Furthermore P9 holds, since NPE(x, M) is geometry invariant for uniform data. Property P5 holds with similarity ratio of NE(x, M) to T(3): [min(d(v(x), e(x)), rd(v(x), l(v(x), x)))]/d(v(x), e(x)); that is, NpE(x, M) is similar to T(3) with the given ratio. P6 holds depending on the pair M and r. That is, there exists an ro := r0(M) so that NρE NE(x, M) satisfies P6 for all r ≤ r0(M), and fails to satisfy otherwise. Property P6 fails for all M when r = ∞, and P8 holds only when M = Mcm. With Mcm-vertex regions, for all r ∈ [1, ∞], the area A(NpE(x, Mcm)) is a continuous function of d(lr(v(x), x), v(x)) which is a continuous function of d(l(v(x), x), v(x)) which is a continuous function of x. Moreover, Λ0(NE, M) = 3 for all r ∈ [1, ∞] and M ∈ R2 \ 3, since the R2-Lebesgue measure λ(NpE(x, M)) = 0 iff x ∈ 3.

T(M1, M2, M3), N2E(x, M) = T(3), so T(M1, M2, M3) ⊆ Rs(N2E, M) where equality holds for M = MCM for all triangles. 2 For r = √2, one can loosen the concept of center by treating the line l(v(x), x) as the area-wise central line in N) (x, M), so PE (x, M) = T (Y3). We could PE

P3 is satisfied in this loose sense. Note that if x is close enough to M, it is possible to have N) also use M-vertex regions obtained by inner angle bisectors.


<!-- p:17 -->


Fig. 19. Shaded regions are double-area proximity region N /2 (x, M−) (left) and double-edge proximity region N2E(x, M−) (right) for an x ∈ R+ (y2).

y3


0.6


0.4


β

MI


0.2


x

β

x

0


y1

y2

y1

α


y2

0

0.2

0.4

0.6

0.8

1

0

0.2

0.4

0.6

0.8

1

0.7

y3

0.6

0.5

0.4

0.3

Mi

0.2

McC

0.1

y1

y2

0

0.6

1

0.2

0.4

0.8

Fig. 20. The hatched region is the triangle T' with r = √2.

The proximity region NE(x, M+) satisfies all the properties as NPE(x, M), except for properties P8 and P9. The property P8 fails as the continuity does not hold with orthogonal projections even for M = Mcm; and P9 fails since with orthogonal projections, the geometry invariance is violated.

In non-obtuse triangles, R(N2E, Mcc) = T(M1, M2, M3) (see Fig. 18 (left)). But, in obtuse triangles, R (N2E, Mcc) T(M1, M2, M3) and is a quadrilateral. The functional forms of the superset region, R(NpE, M), and T(M1, M2, M3) in Tb T(Y3) is an equilateral triangle. For N2E(·, McM) constructed using the median lines Rs(N2E, McM) = T(M1, M2, M3) and for NE(·, McM) constructed by the orthogonal projections, R(N2E, Mcm)  T(M1, M2, M3) with equality holding when T(3) is an equilateral triangle.

In T(3), drawing the lines q(r, x) such that d(yi, e) = rd(q(r, x), y) for i ∈ {1, 2, 3} yields a triangle, Tr, for r &lt; 3/2. See Fig. 20 for Tr with r = √2. The functional form of T′ in Tb is

$$\mathcal { T } ^ { r } & = T ( t _ { 1 } ( r ) , t _ { 2 } ( r ) , t _ { 3 } ( r ) ) \\ & \div T \left ( \left ( \frac { ( r - 1 ) ( 1 + c _ { 1 } ) } { r } , \frac { c _ { 2 } ( r - 1 ) } { r } \right ) , \left ( \frac { 2 - r + c _ { 1 } ( r - 1 ) } { r } , \frac { c _ { 2 } ( r - 1 ) } { r } \right ) , \left ( \frac { c _ { 1 } ( 2 - r ) + r - 1 } { r } , \frac { c _ { 2 } ( r - 2 ) } { r } \right ) \right ) .$$

There is a crucial difference between Tr and T(M1, M2, M3): T(M1, M2, M3) ⊆ Rs(NPE, M) for all M and r ≥ 2, but (Tr)o and Rs(NE, M) are disjoint regions for all M and r. So if M ∈ (Tr)o, then Rs(NpE, M) = ∅; if M ∈ ∂(T′), then Rs(NPE, M) = {M}; and if M ∉ Tr, then Rs(NPE, M) has positive area. Thus NPE(·, M) fails to satisfy P6 if M ∉ Tr. The same holds for NE(·, M–) also. The triangle Tr defined above plays a crucial role in the analysis of the distribution of the domination number of the proportional-edge PCD. In fact, it has been shown that for M ∈ {t1(r), t2(r), t3(r)}, there exists a specific value of r for which the asymptotic distribution of the domination number is non-degenerate [6]. The superset region Rs(NpE, M) will be important for both the domination number and the relative density of the corresponding PCDs.


<!-- p:18 -->


In non-acute triangles, Mcc ∉ T(3)° implies Mcc ∉ Tr (since T(3) ⊃ T'). Let Mcc = (xcc, ycc). For an acute basic triangle, if ycc &lt; c2(√2-2xcc) holds, then Mcc ∉ Tr=√2 (see Fig. 20). 2(1−c1)

##### Remark 3.1.

- ymin(r1, 2) , M). x ∈ Y3 or x ∈ Rs(N) PE
- "stochastically smaller than".

The same results hold for NPE(X, M−) also.

(·, Mcm) is the most appealing proximity map in the family NPE := {NpE(·, M): r ∈ [1, ∞], M ∈ R2 \ V3} ∪ {NPE(·, M−): r ∈ [1, ∞], M ∈ R2 \ 3}. It is also noteworthy that the asymptotic distribution of the domination number of the PCD based on N v3/2 (, Mcm) is non-degenerate. Since, in general, PE NpE(·, M) satisfies more of the properties compared to NpE(·, M+), we will use the former, henceforth.

#### 3.2.1. Extension of NE to higher dimensions

The extension to Rd for d &gt; 2 is straightforward. The extension with M = Mcm is given here, but the extension for general M is similar. Let d+1 = {y1, y2, . . . , Yd+1} be d+ 1 points that do not lie on the same (d — 1)-dimensional hyperplane. Dene    e    d s   s    ed      e s  es d(d + 1)/2 edges and d + 1 faces of dimension (d – 1). For r ∈ [1, ∞], define the proximity map as follows. Given a point x in (d+1), let v := argminy∈d+1 V(Qy(x)) where Qy(x) is the polytope with vertices being the d(d + 1)/2 midpoints of the edges, the vertex v and x and V(·) is the d-dimensional volume functional. That is, the vertex region for vertex v is the polytope with vertices given by v and the midpoints of the edges. Let v(x) be the vertex in whose region x falls. If x falls on the boundary of two vertex regions, v(x) is assigned arbitrarily. Let φ(x) be the face opposite to vertex v(x), and γ(v(x), x) be the hyperplane parallel to φ(x) which contains x. Let d(v(x), γ(v(x), x)) be the Euclidean distance from v(x) to γ(v(x), x). For r ∈ [1, ∞), let γ(v(x), x) be the hyperplane parallel to φ(x) such that

$$d ( v ( x ) , \Upsilon _ { r } ( v ( x ) , x ) ) = & r d ( v ( x ) , \Upsilon \left ( v ( x ) , x \right ) ) \quad \text {and} \quad d ( \Upsilon ( v ( x ) , x ) , \Upsilon _ { r } ( v ( x ) , x ) ) < d ( v ( x ) , \Upsilon _ { r } ( v ( x ) , x ) ) .$$

t  (      s    +         od    n +    =:   e  t    c)

### 3.3. Central similarity proximity maps

For the expansion parameter τ ∈ (0, 1], define Ns(·, M) to be the central similarity proximity map with M-edge regions as follows; see also Fig. 21 with M = Mcm. For x ∈ T(3) \ 3, let e(x) be the edge in whose region x falls; i.e., χ ∈ RM(e(x)). If x falls on the boundary of two edge regions, e(x) is assigned to x arbitrarily. For τ ∈ (0, 1], the central similarity proximity region Ns (x, M) is defined to be the triangle Tτ (x) with the following properties:

- (i) The triangle Tτ (x) has edges e (x) parallel to ei for i ∈ {1, 2, 3}, and for χ ∈ RM(e(x)), d(x, eτ (x)) = τd(x, e(x)) and d(e (x), e(x)) ≤ d(x, e(x)) where d(x, e(x)) is the Euclidean distance from x to e(x);
- (ii) The triangle Tτ (x) has the same orientation as and is similar to T(3);
- I(i              e    ()

Note that (i) implies the parametrization of the PCD, (ii) explains "similarity", and (iii) explains "central" in the name, central similarity proximity map. For τ = 0, we let Nτ=0 (x, M) := {x} for all x ∈ T(3). For x ∈ ∂(T (3)), we have Ncs (x, M) := {x} for all τ ∈ [0, 1].

By definition x ∈ Nτs (x, M) for all x ∈ T(V3). Furthermore, τ ≤ 1 implies that Ncs (x, M) ⊆ T(V3) for all x ∈ T(3) and M ∈ T(3)°. For all x ∈ T(3)° ∩ Rm(e(x)), the edges e (x) and e(x) are coincident iff τ = 1. See Fig. 22 for the arcs based

Notice that Xi~a F, with the additional assumption that the non-degenerate two-dimensional pdf f exists with support iid S(F) ⊆ T(Y3), implies that the special case in the construction of Ns(·) – X falls on the boundary of two edge regions – occurs with probability zero. Note that for such an F, Ns(X, M) is a triangle for τ &gt; 0 a.s. The central similarity proximity m     s         s      m are always inside the triangle, so they can be used in construction of the central similarity proximity map.


<!-- p:19 -->


(x, Mcm) (shaded region) where d2 = d(x, e3 (x)) = 1d(x, e(x)) and d1 = d(x, e(x)).

y3

e2

e1

MCM

ei(x)

e2(x)

d2

e3(x)

d1

y1

y2

e3 = e(x)

Fig. 22. A realization of 20 class X points (circles) generated iid U(T(3)) (left) and the corresponding arcs for N1 (x, Mcm) (right).

o

8

。。

o


0

&lt;

Fig. 23. The regions N[=1 (x, M) for an x ∈ RM (e3) (left); and Nτ=1 (x, M1) for an x ∈ RM1 (e3) (right).

y3


0.6


0.4


W

MI

0.2


x


0

y1

y2

0

y1

y2

0

0.2

0.4

0.6

0.8

1

0

0.2

0.4

0.6

0.8

1

With M = Mcm, for x ∈ Rcm(e), the similarity ratio of Ncs(x, Mcm) to T(3) is d(x, eτ(x))/d(Mcm, e). See Fig. 21 for d       =   d        = CS proximity regions Ns(x, M) are also described in detail in [2]. In general, for central similarity proximity regions with M-edge regions, the similarity ratio of Ns (x, M) to T(3) is d(x, e (x))/d(M, e(x)). See Fig. 23 (left) for Nτ=1(x, M) and (right) Nτ=1 (x, M1) with e(x) = e3. Notice that Ns(·, M) satisfies properties P1-P9. Furthermore, Λ0(Ns (·, M)) = ∂(T (3)) for all τ ∈ (0, 1] and Λ0(Nτ=0(·, M)) = T(3), since λ(Ncs(x)) = 0 iff x ∈ ei for i ∈ {1, 2, 3} or τ = 0.

Remark 3.3. For acute triangles we could use Mcc- or Mo-edge regions in central similarity proximity regions which will also satisfy properties P1-P9. But for obtuse triangles, P2 is not satisfied and edge regions are not defined in a natural manner.


<!-- p:20 -->


Remark 3.4. In the family Nξs := {Nτs (·, M): τ ∈ [0, 1], M ∈ T(3)°}, every Nτs (·, M) with τ ∈ [0, 1] satisfies all the properties in Section 2.1. Furthermore,

- For τ1 ≤ τ2, N1 (x, M) ⊆ Nτ2s( Ncs(x, M) for all ∈ T(3). For τ1 &lt; τ2, Ns (x, M) ⊆ N2 (x, M) with equality holding only for x ∈ ∂(T(3)).
- For t1 &lt; τ2, A(Nts (X, M)) ≤ST A(Ns(X, M)) for X from a continuous distribution on T(V3).
- The superset region Rs(Ncs, M) = ∅ for t ∈ [0, 1) and Rs(Nt=1, M) = {M}.

#### 3.3.1. Extension of Ns to higher dimensions

The extension of Nτs to Rd for d &gt; 2 is straightforward. The extension for M = Mcm is described, the extension for general M is similar. Let Yd+1 = {y1, y2, . . . , Yd+1} be d + 1 points that do not lie on the same (d − 1)-dimensional hyperplane. For τ ∈ (0, 1], define the central similarity proximity map as follows. Let φi be the face opposite vertex yi for c  +   +)  +     (  (     ( +    · } the d + 1 polytopes with vertices being the center of mass together with d vertices chosen from d + 1 vertices. For x ∈ S(d+1) \ d+1, let φ(x) be the face in whose region x falls; x ∈ R(φ(x)). If x falls on the boundary of two face regions, φ(x) is assigned arbitrarily. For τ ∈ (0, 1], the central similarity proximity region Ns (x, Mcm) = Sτ (x) is defined to be the simplex Sτ (x) with the following properties:

- (i) The region Sτ (x) has faces φμ (x) parallel to φi(x) for i ∈ {1, 2, . . . , (d + 1)}, and for χ ∈ Rcm(φ(x)), τd(x, φ(x)) = d(φ (x), x) where d(x, φ(x)) is the Euclidean distance from x to φ(x);
- (iii) The point x is the center of mass of Sτ (x), as Mcm is of &amp;(d+1). Note that τ &gt; 1 implies that x ∈ Nτs(x).
- (ii) The region Sτ (x) has the same orientation as and similar to S(d+1);

### 3.4. The behavior of proximity regions

Let N(·) be any proximity map defined on the measurable space Ω with measure μ, and let {xn}=1 be a sequence of points in Ω. We say N(xn) gets larger as n increases if N(xn) ⊆ N(xm) for m ≥ n, and N(xn) gets strictly larger if N(xn) ¢ N(xm) for m &gt; n.

In the following theorems we will assume Ω = R2 with μ being the R2-Lebesgue measure λ and M-vertex regions are defined with pointsM ∈ R2 \ 3.

h)  ) (  \ ( t           ) (     ·    tt) larger.

Proof. Let N(·) ∈ NAs. For x, y lying on a ray from y in RM (y) \ Rs(N, M), if d(x, y) ≤ d(y, y), then B(x, r(x)) ⊆ B(y, r(y)), which implies N(x) ⊆ N(y), hence N(x) gets larger as d(x, y) increases for x lying on a ray from y in Rm (y) \ Rs(N, M). The strict version follows similarly. If x, y ∈ RM (y) ∩ Rs(N, M), then N(x) = N(y) = T (3). □

Let l(y, x) be the line at x parallel to e(x) for x ∈ Rm (y) where e(x) is the edge opposite vertex y.

Theorem 3.6. For N(·) ∈ NPE, as d(l(y, x), y) (strictly) increases with x ∈ RM (y) \ Rs(N, M), N(x) gets (strictly) larger for r &lt; ∞.

Proof. Let N(·) ∈ NPE. For x, y ∈ RM(y) \ Rs(N, M), if d(l(y, x), y) ≤ d(l(y, y), y), then by definition N(x) ⊆ N(y), hence the s ∞ =    (  = ( = (x o (   (      is  n     nd x, y ∈ T (3) \ 3, N(x) = N(y) = T (3). □

Note that as d(l(y, x), y) increases for x ∈ Rm(y), d(l(y, x), M) decreases, provided that M ∈ T(3)° and M-vertex regions are convex.

Theorem 3.7. For N(·) ∈ Nτs with τ ∈ (0, 1], as d(x, e) (strictly) increases with x ∈ RM (e), the area A(Nτs (x, M)) (strictly) increases.

Proof. Let N(·) ∈ Nτs with τ ∈ (0, 1]. For x, y ∈ Rm(e) and τ ∈ (0, 1], if d(x, e) ≤ d(y, e) then the similarity ratio of N(y) to T(3) is larger than or equal to that of N(x), which in turn implies that A(N(x)) ≤ A(N(y)). The strict version follows similarly. □

Observe that the statement of Theorem 3.7 is about the area A(Ns(x, M)). We need further restrictions for Ns(x, M) to get larger.

Theorem 3.8. Let lm (y) be the line joining M and vertex y ∈ Y3 and let N(·) ∈ Nξs with τ ∈ (0, 1]. As d(x, lm (yj)) and d(x, lM (yk)) both (strictly) decrease for x ∈ Rm (el) where j, k, l are distinct, N(x) (strictly) increases.


<!-- p:21 -->


Fig. 24. The figure for x, y ∈ RM (e3) described in Theorem 3.8. Here d1 = d(x, lMc (y1)) and d2 = d(x, lMc (y2)).

y3

e2

e1

MCM

.y

d2

x

1p

y1

y2

ε3

Proof. Suppose, without loss of generality, that x, y ∈ Rm(e3). Consider the set

```
S ( e _ { 3 } , x ) \coloneqq \left \{ y \in R _ { M } ( e _ { 3 } ) \colon d ( y , \ell _ { M } ( y _ { 1 } ) ) \leqslant d ( x , \ell _ { M } ( y _ { 1 } ) ) \ \text { and } \ d ( y , \ell _ { M } ( y _ { 2 } ) ) \leqslant d ( x , \ell _ { M } ( y _ { 2 } ) ) \right \} ,
```

which is a parallelogram. See Fig. 24 for an example of S(e3, x) with M = Mcm and e = e3. Given x, for y ∈ S(e3, x), by construction, N(x) ⊆ N(y). Then the desired result follows for τ ∈ (0, 1]. Observe that if xn+1 is in S(e3, xn), then d(xn, lm (y1)) and d(xn, lm(y2)) both decrease. The strict version follows similarly. □

Remark 3.9. For Rs(Ny) with positive area, by definition, as x → y ∈ Rs(Ny), Ny(x) → T(3) and hence argsupx∈T(3) A(Ny(x)) ∈ Rs(Ny) with supx∈T(3) A(Ny (x)) = A(T(3)). Furthermore, the following also hold.

- Let N(·) ∈ NAs. Then as x → Mcc in a non-obtuse triangle T(3), we have N(x) → T(3) and

```
Remark   3.9.    For    &R s (N y)    with    positive    area,    by    definition,    as    x ->   y  =   \mathcal { R } s ( N y ),    N y ( x )  ->   T () \, \mathcal { Y } \, ( x \in \mathcal { Y } ) \, N ( x ) \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \, \mathop \rightarrow \,
```


<!-- p:22 -->


Although the comments in the above remark mostly follow by definition, they will be indicative of whether the asymptotic distribution of the domination number of the associated PCD is degenerate or not.

## 4. Relative density and domination number of PCDs

### 4.1. Relative density

The relative density of a digraph D = (V, A) of order |V| = n, denoted as ρ(D), is defined as

$$\rho ( D ) = \frac { | \mathcal { A } | } { n ( n - 1 ) }$$

where |·| denotes the cardinality of sets [13]. Thus ρ(D) represents the ratio of the number of arcs in the digraph D to the number of arcs in the complete symmetric digraph of order n, which is n(n – 1).

iid If X1, X2, . . . , Xn ~ F the relative density of the associated data-random PCD D, denoted as ρn for brevity, is a U-statistic,

$$\rho _ { n } = \frac { 1 } { n ( n - 1 ) } \sum _ { i < j } h _ { i j }$$

where

$$h _ { i j } = \{ ( X _ { i } , X _ { j } ) \in A \} + \{ ( X _ { j } , X _ { i } ) \in \mathcal { A } \} = \{ X _ { j } \in N _ { \mathcal { Y } } ( X _ { i } ) \} + \{ X _ { i } \in N _ { \mathcal { Y } } ( X _ { j } ) \} ,$$

where I(·) is the indicator function. Since the digraph is asymmetric, hij is defined as the number of arcs in D between vertices X and Xj, in order to produce a symmetric kernel with finite variance [16].

The random variable ρn depends on n and Ny explicitly and on F implicitly. The expectation E[ρn], however, is independent of n and depends on only F and Ny:

$$0 \leqslant E [ \rho _ { n } ] = \frac { 1 } { 2 } E [ h _ { 1 2 } ] \leqslant 1 \quad \text {for all $n\geqslant 2$} .$$

The variance Var[ρn] simplifies to

$$0 \leqslant & \text {Var} [ \rho _ { n } ] = \frac { 1 } { 2 n ( n - 1 ) } \text { Var} [ h _ { 1 2 } ] + \frac { n - 2 } { n ( n - 1 ) } \text { Cov} [ h _ { 1 2 } , h _ { 1 3 } ] \leqslant 1 / 4 .$$

A central limit theorem for U-statistics [16] yields

$$\sqrt { n } ( \rho _ { n } - \mathbf E [ \rho _ { n } ] ) \stackrel { \mathcal { L } } { \longrightarrow } \mathcal { N } ( 0 , \text {Conv} [ h _ { 1 2 } , h _ { 1 3 } ] )$$

provided Cov[h12, h13] &gt; 0. The asymptotic variance of ρn, Cov[h12, h13], depends on only F and Ny. Thus, we need determine only E[h12] and Cov[h12, h13] in order to obtain the normal approximation

$$\text {Var} [ \rho _ { n } ] = \mathcal { N } \left ( \frac { E [ h _ { 1 2 } ] } { 2 } , \frac { \text {Conv} [ h _ { 1 2 } , h _ { 1 3 } ] } { n } \right ) \quad \text {for large $n$} .$$

4.1.1. Asymptotic distribution of relative density of PCDs

By detailed geometric probability calculations, provided in [8] and [7] the mean and the asymptotic variance of the relative density of the proportional-edge and central similarity PCDs can explicitly be computed. The central limit theorem for U-statistics then establishes the asymptotic normality under the uniform null hypothesis. These results are summarized in the following theorems.

Theorem 4.1. Let ρn(Np) be the relative density of the proportional-edge PCD with parameter r and M = Mcm based on a random sample of Xn from U(T (3)) and pa(N E) be the corresponding arc probability, and ν(NpE) be the Cov(h12, h13). Then for r ∈ [1, ∞),

$$\frac { \sqrt { n } ( \rho _ { n } ( N _ { p _ { E } } ^ { r } ) - p _ { a } ( N _ { p _ { E } } ^ { r } ) ) } { \sqrt { \nu ( N _ { p _ { E } } ^ { r } ) } } \xrightarrow { \mathcal { L } } \mathcal { N } ( 0 , 1 )$$

where

$$\text {where} \\ p _ { a } ( N _ { p _ { E } } ^ { r } ) = \begin{cases} \frac { 3 7 } { 2 1 6 } r ^ { 2 } & \text {for } r \in [ 1 , 3 / 2 ) , \\ - \frac { 1 } { 8 } r ^ { 2 } + 4 - 8 r ^ { - 1 } + \frac { 9 } { 2 } r ^ { - 2 } & \text {for } r \in [ 3 / 2 , 2 ) , \\ 1 - \frac { 3 } { 2 } r ^ { - 2 } & \text {for } r \in [ 2 , \infty ) , \end{cases}$$


<!-- p:23 -->


and

$$v ( N _ { P _ { E } } ^ { r } ) & = v _ { 1 } ( r ) ( r \in [ 1 , 4 / 3 ) ) + v _ { 2 } ( r ) ( r \in [ 4 / 3 , 3 / 2 ) ) + v _ { 3 } ( r ) ( r \in [ 3 / 2 , 2 ) ) + v _ { 4 } ( r ) ( r \in [ 2 , \infty ] ) \\ \text {with} & \\$$

$$with & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & &$$

For r = ∞, ρn(NpE) is degenerate.

Theorem 4.2. Let ρn(Ns) be the relative density of the central similarity PCD with parameter τ and M = Mcm based on a random sample of Xχn from U(T (Ö3)) and pa(Ncs) be the corresponding arc probability, and ν(Nτs) be the Cov(h12, h13). Then for τ ∈ (0, 1], the relative density of the central similarity proximity digraph converges in law to the normal distribution; i.e., as n → ∞,

$$\text {the remaining details of the algorithm are provided in the paper} \, , & \, \arg a r p a m i t y \, \arg a r p a m i t y \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t y \, , \, \arg a r p a m i t y \, , \, \text {as} \, , \, \text {and} \, , \, \arg a r p a m i t$$

where

$$p _ { a } ( N _ { C S } ^ { \tau } ) = \tau ^ { 2 } / 6 \ \ a n d \quad \nu ( N _ { C S } ^ { \tau } ) = \frac { \tau ^ { 4 } ( 6 \tau ^ { 5 } - 3 \tau ^ { 4 } - 2 5 \tau ^ { 3 } + \tau ^ { 2 } + 4 9 \tau + 1 4 ) } { 4 5 ( \tau + 1 ) ( 2 \tau + 1 ) ( \tau + 2 ) } .$$

For τ = 0, ρn(Nτs) is degenerate for all n &gt; 1.

### 4.2. Domination number of the PCDs

In a digraph D = (V, A), recall that the domination number γ(D) is the cardinality of the minimum dominating set. If a minimum dominating set is of size one, we call it a dominating point. Note that for |V| = n &gt; 0, 1 ≤ γ (D) ≤ n, since V itself is always a dominating set.

#### 4.2.1. Asymptotic distribution of domination number of the PCDs

The domination number γn(r, M) of the PCD has the following asymptotic distribution [6]. As n → ∞,

Recall the triangle Tr defined in Eq. (1) (see also Fig. 20 for Tr with r = √2). Let γn(r, M) be the domination number of the PCD based on NE(, M) with Xn, a set of iid random variables from U(T(3)), with M-vertex regions.

$$\text {mixture} \, \lambda \, \gamma _ { n } ( r , M ) \stackrel { 2 } { \longrightarrow } & \begin{cases} 2 + \text {BER} ( 1 - \pi _ { r } ) & \text {for } r \in [ 1 , 3 / 2 ) \, \text {and } M \in \{ t _ { 1 } ( r ) , t _ { 2 } ( r ) , t _ { 3 } ( r ) \} , \\ 1 & \text {for } r > 3 / 2 \, \text {and } M \in T ( \mathcal { Y } _ { 3 } ) ^ { o } , \\ 3 & \text {for } r \in [ 1 , 3 / 2 ) \, \text {and } M \in \mathcal { T } ^ { r } \ \{ \{ t _ { 1 } ( r ) , t _ { 2 } ( r ) , t _ { 3 } ( r ) \} , \end{cases} \\$$

( ( }    (    d  ()     ( t))

$$\pi _ { r } = \bigset { \prod _ { 0 } ^ { \infty } \frac { \infty } { \int \int \frac { 6 4 r ^ { 2 } } { 9 ( r - 1 ) ^ { 2 } } w _ { 1 } w _ { 3 } \exp \left ( \frac { 4 r } { 3 ( r - 1 ) } ( w _ { 1 } ^ { 2 } + w _ { 3 } ^ { 2 } + 2 r ( r - 1 ) w _ { 1 } w _ { 3 } ) \right ) d w _ { 3 } w _ { 1 } . }$$

For example, for r = 5/4 and M ∈ {t1(r) = (3/10, √3/10), t2(r) = (7/10, √3/10), t3(r) = (1/2, 3√3/5)}, πr ≈ 0.6514. See -in    on   n            od  o  on degenerate case in (13), E[γn(r, M)] = 3 − πr and Var[γn(r, M)] = πr(1 − πr). For r = 3/2 and M = Mcm = (1/2, √3/6), we have πr ≈ 0.7413, which is computed differently from that in Eq. (14); see [5] for its computation.

The results in Theorem 2.4 and Corollaries 2.10 and 2.11 also hold for relative density and the domination number of PCDs based on Ny. That is, we have the following corollary.

The distribution of the domination number of Ns is still an open problem.

Corollary 4.3. Given any triangle T0 and Xn a random sample from U(To). Suppose the PCD, Do is defined in such a way that the ratio of the area of N(x) to the area of the triangle T。 is preserved under the uniformity preserving transformation, then the distributions of the relative density and the domination number of D。 are geometry invariant.


<!-- p:24 -->

0.8

0.6

11

0.4

0.2

0

1

1.1

1.2

1.3

1.4

1.5

r

Fig. 25. The probability πr = limn→∞ P(γn(r, M) = 2) given in Eq. (14) as a function of r for r ∈ [1, 3/2) and M ∈ {t1 (r), t2(r), t3 (r)}.

07F

y3


0.6


0.5

0.4


0.3

MCM

0.2


++

+++

4+****

φx

0.1

y1

+++++++++H

++4

y2

0

y1

c = 1/2

y2

0.2

0.4

0.6

0.8

1

x

0

0.2

0.4

0.6

0.8

1

Fig. 26. An example of directional-doubling proximity region with M = Mcm (left) and double-X proximity region with c = 1/2 (right).

## 5. Two new proximity maps

In this section, we introduce two new proximity maps and investigate their properties.

### 5.1. Directional-doubling proximity maps

it    n -n     t    n =          e) for i = 1, 2, 3. For z ∈ Rm(ei), directional-doubling proximity map is defined as

$$N _ { D D } ( z , M ) \colon = \left \{ u \in T _ { b } \colon d ( u , e _ { i } ) \leqslant 2 d ( z , e _ { i } ) \right \} .$$

See Fig. 26 (left) with M = Mcm. If z ∈ ei, then NDD(z, M) := ei. Notice that if z ∉ ei, then NDD(z, M) is a quadrilateral. Among the properties, P1 and P2 follow trivially. The line at z ∈ Rm (e) parallel to e divides the region into two pieces (half-way in the perpendicular direction to e) so P3 holds in this special sense. Properties P4 and P5 both fail, since NDD(z, M) is a quadrilateral. Property P6 holds if M ∈ T(M1, M2, M3); otherwise it fails, since Rs(NDD, M) will have positive area. Property P7 follows by definition. However, P8 holds only when M = Mcm.

Property P9 follows for NDD, since NDD(z, M) is constructed with the boundary of T(3) and parallel lines to the edges and by Corollary 2.10, geometry invariance for uniform data follows. That is, the distributions of relative density and the domination number of the corresponding PCD do not depend on the geometry of the triangle T(3). Hence, it suffices to compute them for the standard equilateral triangle only. Furthermore, we have Λ0(NDD) = ∂(T(3)), since NDD(x, M) has zero area iff x ∈ ∂(T(3)).


<!-- p:25 -->


Table 1

ds  = (    :6   =   :           s  :  :i      l.

The table for the six proximity region families we consider in Rd with d &gt; 1 with respect to the nine properties P1-P9 defined in Section 2.1. + (-): the property is (not) satisfied for all parameters of the corresponding proximity region. The symbol — with a numbered superscript means the property is satisfied only for some of the parameters. *: Ns(·) satisfies all the properties in R. **: The left (and right) column is for the\_proximity region that is a      =      s  o :  : o =     (d :  (   o  a     i as described on page 736; 3: holds for r ≤ ro(M) for r0 (M) described on page 736 only; 4: holds for M = Mcm only; 5 and 6: holds in the special sense

| Property   | Proximity regions   | Proximity regions   | Proximity regions   | Proximity regions    | Proximity regions    | Proximity regions           | Proximity regions   |
|------------|---------------------|---------------------|---------------------|----------------------|----------------------|-----------------------------|---------------------|
|            | N S ( · )           | ∗ N AS ( · ,        | M ) ∗∗              | N r P E ( · , M ) ∗∗ | N r P E ( · , M ) ∗∗ | N τ CS ( · , M ) N DD ( · , | M ) N DX ( · , c )  |
| P1         | +                   | +                   | +                   | +                    | + +                  |                             | +                   |
| P2         | +                   | +                   | +                   | +                    | +                    | + +                         | +                   |
| P3         | +                   | -                   | -                   | - 2                  | + - 2 +              | - 5                         | - 6                 |
| P4         | -                   | -                   | -                   | +                    | + +                  | -                           | -                   |
| P5         | -                   | -                   | -                   | +                    | + +                  | -                           | -                   |
| P6         | -                   | -                   | - 1                 | - 3                  | - 3 +                | - 7                         | - 8                 |
| P7         | -                   | +                   | +                   | +                    | + +                  | +                           | +                   |
| P8         | +                   | -                   | - 1                 | - 4                  | - +                  | - 4                         | - 9                 |
| P9         |                     |                     |                     |                      |                      |                             |                     |

### 5.2. Double-X proximity maps

Without loss of generality, we can assume that T(3) = Tb. Partition the triangle Tb using the vertical line at c ∈ (0, 1) as in Fig. 26 (right) with c = 1/2. Let R1(c) := {(x, y) ∈ Tb: χ &lt; c} and R2(c) := {(x, y) ∈ Tb: χ &gt; c}. If (x, y) ∈ Tb with x = c, assign (x, y) arbitrarily to one of R1(c) or R2(c). We define the double-X proximity map as follows. For z = (xo, yo) ∈ Tb \ {y1, y2}

$$N _ { D X } ( z , c ) \colon = \begin{cases} \{ ( x , y ) \in T _ { b } \colon x \leqslant 2 x _ { o } \} & \text {if } z \in R _ { 1 } ( c ) , \\ \{ ( x , y ) \in T _ { b } \colon 1 - x \leqslant 2 ( 1 - x _ { o } ) \} & \text {if } z \in R _ { 2 } ( c ) . \end{cases}$$

If z = (x0, yo) ∈ {y1, y2}, then NDx(z, c) := {z}. See also Fig. 26 (right). Notice that if z ∉ {y1, y2}, then NDD(z, M) is a right triangle or a quadrilateral. Among the properties, P1 and P2 follow trivially. The vertical line at z divides the region into two pieces (half-way along the x-coordinate), so P3 holds in this special sense. Properties P4 and P5 fail to hold, since NDx(z, c) may be a quadrilateral for some z ∈ Tb. Property P6 holds if c = 1/2, otherwise Rs(NDx, c) has positive area and P7 also follows by definition. However, P8 holds only when the regions R1(c) and R2(c) are constructed at a point where the vertical line divides the area into two equal pieces.

Property P10 fails, since NDx(z) is constructed with the boundary of Tb and a line with a specific angle (perpendicular to the largest edge). By Corollary 2.11, geometry invariance for uniform data does not hold. That is, the distributions of relative density and the domination number of the corresponding PCD depend on the geometry of the triangle T(3). Hence, it does not suffice to compute them for the standard equilateral triangle only, but instead one should compute them for each pair of (c1, c2). Moreover, Λ0(NDx) = {y1, y2}, since NDx(x, c) has zero area iff x ∈ {y1, y2}.

## 6. Discussion and conclusions

In this article, we discuss the construction of proximity catch digraphs (PCDs) based on two classes of points X' and in multiple dimensions. Let Xn and Ym be two samples from classes X and Y, respectively. PCDs are a special type of proximity graphs which have applications in various fields. The class cover catch digraph (CCCD) is the first type of P id ,  n (ss  d i as          or uniform data in R; in the sense that, the exact and asymptotic distribution of the domination number for CCCDs are available for uniform one-dimensional data. We determine some of the properties of the spherical proximity regions in R (called appealing properties), and use them as guidelines for defining PCDs in higher dimensions. We also characterize the geometry invariance for PCDs based on uniform data. Geometry invariance is important, since it facilitates the computation of quantities (such as relative density or domination number) related to PCDs.

We discuss four PCD families in literature and introduce two new PCD families in this article. We investigate these PCD families in terms of the appealing properties and geometry invariance for uniform data. See Table 1 for the proximity region families with respect to the appealing properties. We provide the asymptotic distribution of relative density and dn  od as     r n     o o n sis and statistical pattern classification. We have demonstrated that the more the properties are satisfied, the better and simpler the asymptotic distribution of relative density. Furthermore, the availability of the asymptotic distribution of domination number is highly correlated with the number of properties satisfied.

eh o  w d   r n  (   o s n as ssed on a particular geometric shape or a functional form; that is, the new proximity regions admit any type of region, e.g., circle (ball), arc slice, triangle, a convex or nonconvex polygon, etc. In this sense, the PCDs are defined in a more general setting compared to CCCD. Moreover, the new families of proximity maps we introduce will yield closed regions. Furthermore, the CCCDs based on balls use proximity regions which are defined by the obvious metric, while the PCDs do not suggest an obvious metric. One main advantage of CCCDs is that they are well defined for all X' points (regardless of they are in the convex hull of m, CH(m), or not) provided that m ≥ 1. On the other hand, the distribution of the domination number and relative density are not analytically tractable for data in Rd with d &gt; 1. All the non-spherical PCDs (i.e., PCDs other than CCCDs) we consider in this article are only well-defined for X points inside CH(m), but, nevertheless, the distributions of fng -rn ot sn nd ads r o rt o ons r ra or sns rn r s rer od -l  eiot ' e      eo e eion with the expansion parameter around 1 [7]. Among these two families, we recommend the proportional-edge PCDs with a parameter within 1.5–2. For large samples, the domination number of the proportional-edge PCD is more sensitive (i.e., more powerful) against the segregation and association alternatives, but for small samples the relative density is more appropriate since the convergence in distribution is faster for the relative density. For points outside the convex hull, a correction factor is introduced for the domination number by Ceyhan [3], a similar factor can be devised for the relative density as well.


<!-- p:26 -->


-i  t ' ( a   l il    s   'ti bution of the domination number. However, it turned out that they might be more useful for the geometry invariance of thnn i  a t e rl  ee   rii e    o ons satisfy all the properties, and their relative density has the simplest asymptotic distribution; but the distribution of their domination number is still an open problem. The investigation of the domination number of the arc-slice PCDs sheds some light on that of the spherical PCDs (i.e., CCCDs). By construction, for points in the convex hull, arc-slice PCD is a subdigraph of the CCCD (with the same vertices), hence the domination number of CCCDs is stochastically smaller than that of arc-slice PCDs. Since the upper bound for the arc-slice PCD for data in one triangle is three, for data in the convex hull, CCCDs domination number is bounded by three times the number of Delaunay triangles. Adding more  points outside the convex hull so that all X' points are inside the convex hull might provide an upper bound for the domination number of CCCDs as well, but then the applicability for spatial pattern analysis and classification may not be possible.

The mechanism to define the proximity maps (and regions) provided in this article can also be used for defining new pery r ie (ie  iy ies.

Most of the discussion in this article is for data in Rd with d ≤ 2. For higher dimensional data, the geometry invariance results hold as well, and the same properties will be satisfied (with perhaps minor modifications). Moreover, the behavior of the PCDs will be same as in Section 3.4. The asymptotic normality of the relative density for proportional-edge and central similarity PCDs also hold, and domination number of the proportional-edge PCD can be computed as in the two-dimensional case. For example, Ceyhan and Priebe [5] provide the domination number in R3. However, the calculations of the relative nneiy  o        '       e in very high dimensions, since for large d almost all the points will be outside the convex hull (with high probability). In tu s  l (   s is   s  t  id    s  tt in practice this becomes extremely crucial for the applicability of the PCD approach. Perhaps, either PCD approach could be employed after a dimension reduction technique is applied to the data set; or the data can be mapped to a lower dimension by multi-dimensional scaling, and then the PCD approach can be used.

## Acknowledgements

I would like to thank anonymous referees, whose constructive comments and suggestions greatly improved the presentaia # r r  i e,   t  s ra e  rd     ob.

## Appendix A

###### A.1. Symbols and notation used in the article

M(p, q): Neighborhood associated with (unordered) pair of points p, q ∈ V. See page 721.

G,  (V, E): Proximity (or neighborhood) graph. Šee page 721.

: The property that defines the edge set in Gm,p(V, E). See page 721.

RNG(V): Relative neighborhood graph for a set of points V ⊂ Rd. See page 721.

NND(V): Nearest neighbor digraph for a set of points V ⊂ Rd. See page 722.

N(·): Proximity map in the most general form defined as N : Ω → (Ω) in measurable space (Ω, M). See page 722.

D = (V, A): Digraph with vertex set V and arc set A. See page 722.

γ(D): Domination number for the digraph D. See page 722.

Ny(·): Proximity map based on two classes χn, m ⊆ Ω. Šee page 723.

γn(r, M): The domination number of the PCD based on NE with Xn. See page 743.

pa(Ny): The probability of having an arc from X to Xj, i.e., arc probability for the PCD based on Ny. See page 723.

pa(NE) and pa(Ns) are also the (asymptotic) means for the relative arc density for proportional-edge and central similarity PCDs. See Eqs. (9) and (12).

Ns(x): Spherical proximity map defined as the open ball B(x, r(x)) for all x ∈ R \ m, where r(x) = miny∈ym d(x, y). See page 723.


<!-- p:27 -->


CH(A): Convex hull of the set A. See page 724.

S   (  o    nn :2,.

T: ith Delaunay cell in the Delaunay tessellation of Ym in Rd. See page 724.

Ii: ith interval based on m in R. See page 726.

e d  ue -  e     .

Λ0(N): The Λ0-region for the proximity map N(·). See Definition 2.2 on page 725.

Dp: Delaunay tessellation based on a finite data set from a (Poisson) point process. See page 726.

Vp: Poisson Voronoi diagram associated with Dp. See page 726.

Te: The standard equilateral triangle T((0, 0), (1, 0), (1/2, √3/2)). See page 727.

T i  y7    } = C    y :(2.

φ: The transformation that maps any triangle to Tb. See page 727.

Tb: The basic triangle T((0, 0), (1, 0), (c1, c2)) with 0 &lt; c1 ≤ 1/2, and c2 &gt; 0 and (1 − c1)2 + c2 ≤ 1. See page 727.

φe: The transformation that maps Tb to Te. See page 728.

Mcc: The circumcenter of a triangle; M: the incenter of a triangle; Mcm: the centroid or center of mass of a triangle; and Mo: the orthocenter of a triangle. See page 729.

Vc(y): The Voronoi cell generated by y. See page 731.

R(y): The vertex region obtained by drawing the orthogonal projections to the edges (i.e., with Method II). See page 731.

Rm (y): The vertex region obtained by using the extensions of the line segments joining y to M (i.e., with Method I). See page 731.

Rm(e): The edge region for edge e. See page 732.

S(F): The support of a distribution F. See page 733.

NAs(x): Arc-slice proximity map. See page 733.

NPE(·, M): Proportional-edge proximity map with M-vertex regions. See page 734.

NAs: The family of arc-slice proximity regions with center M ∈ R2 \ 3 and vertex regions with Methods I and II. See page 734.

Tr(x): The triangle similar to and with the same orientation as T(Y3). See page 734.

(   {  }   i (  t =    s (         :) Vertices of Tr are t1(r), t2(r), and t3(r). See Fig. 20.

vertex regions with Methods I and II. See page 738.

S(d+1): The simplex formed by d + 1 points d+1 = {y1, y2, . . . , yYd+1} in Rd. See page 738.

(v(x), x): The hyperplane parallel to φ(x) which contains x where φ(x) be the face opposite to vertex v(x) in (d+1). See page 738.

Tτ (x): The defining triangle for Ns (x, M). See page 738.

Ns(·, M): Central similarity proximity map with M-edge regions. See page 738.

center M ∈ M ∈ T(Y3)0. See page 740.

ρ(D): Relative density for digraph D. See page 742.

ν(NE) and v(Ns): The (asymptotic) variances for the relative arc density for proportional-edge and central similarity PCDs. See Eq. (10) on page 743.

1 e   ( .  ( = (      :1.

NDD(·, M): Directional-doubling proximity map based on M-edge regions. See page 744.

y   -oe :(  5.
