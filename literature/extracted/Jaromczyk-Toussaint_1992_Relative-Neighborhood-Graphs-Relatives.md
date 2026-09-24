---
id: "Jaromczyk-Toussaint_1992_Relative-Neighborhood-Graphs-Relatives"
source_pdf: "../pdf/Jaromczyk-Toussaint_1992_Relative-Neighborhood-Graphs-Relatives.pdf"
source_filename: "Jaromczyk-Toussaint_1992_Relative-Neighborhood-Graphs-Relatives.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "excellent"
extraction_score: 108.0
visual_assets: "disabled"
---

<!-- p:1 -->

## Relative Neighborhood d Graphs and Their Relatives

JERZY W. JAROMCZYK AND GODFRIED T. TOUSSAINT

Invited Paper

This is a survey of results on neighborhood graphs. The paper discusses properties, bounds on the size, algorithms, and variants of the neighborhood graphs. Numerous applications including computational morphology, spatial analysis, pattern classification, and data bases for computer vision are described. A rich bibliography of the subject concludes the paper.

Keywords—Computational geometry, computational morphology, geometric graphs, neighborhood graphs, spatial analysis.

## I. INTRODUCTION

aa , Rdaed   asstd sa  e Neighborhood Graph of a Finite Planar Set" [1] appeared in print. This anniversary provides a good opportunity to review the results obtained so far and the current state of research on neighborhood graphs.

The relative neighborhood graph of a finite set of points V, RNG(V), is a prominent representative of the family of graphs which are defined using some concept of neighborliness. For points in a real space Ra the relative neighborhood graph of V is a graph with vertex set V and set of edges RNG(V) which are exactly those pairs (p, q) of points for which δ(p, q) ≤ max veV\{p,q} {δ(p, v), δ(q, v)}, where δ denotes the distance between p and q. Fig. 1 illustrates a set of points and their relative neighborhood graph.

In fact, during this time the original notion of neighborhood has been generalized in several directions and all of these graphs are now jointly referred to as proximity graphs [2]. So much interest has been spawned in this area that in December 1989 an entire conference on proximity graphs took place in Las Cruces, New Mexico [3].

The main objective of this paper is to summarize efforts of the last ten years of research on concepts which emerged while studying relative neighborhood graphs.

From a mathematical and algorithmic point of view, neighborhood graphs fall under the scope of computational

Manuscript received January 21, 1990; revised April 16, 1992.

G. T. Toussaint is with the School of Computer Science, McGill

J. W. Jaromczyk is with the Department of Computer Science, University of Kentucky, Lexington, KY 40506–0027.

University, 3480 University Street, Montreal, Quebec, Canada H3A 2A7.

IEEE Log Number 9204424.

.


Fig. 1. A point set and its RNG.

geometry. More particularly, since they are concerned with extracting the shape and structure of points sets, from an application perspective, they form an indispensable tool of computational morphology. Neighborhood graphs serve as tools in disciplines where shape and structure are vital. These include visual perception, computer vision and pattern recognition, geography and cartography, and biology, to list a few; for further examples refer to the section on applications and the bibliography, which includes numerous references.

There is, however, much beyond purely practical applications which makes neighborhood graphs attractive objects of study. We will demonstrate both practical and theoretical aspects in further sections, where we discuss algorithms, properties, and applications.

## II. DEFINITIONS

We will start with a definition of neighborhood graph in a quite general form. This will later enable us to introduce specialized versions more uniformly. Although our later discussion mainly pertains to R2 and R3 the definition is valid in any dimension.

Let V be a set of points in Rd. Each (unordered) pair of points (p, q) ∈ V × V is associated with a neighborhood Up,q C Rd. Let P be a property defined on U = {Up,q : (p, q) ∈ V × V}. A neighborhood graph Gu,p(V, E) defined by the property P is a graph with the set of vertices

~- V and the set of edges E such that (p, q) ∈ E if and only if Up,q has property P. If (p, q) is an edge, denoted later simply by pq, then we say that q is a neighbor of p (and vice versa). For some neighborhood graphs it is more natural to associate neighborhoods with points rather than with pairs of points.

<!-- p:2 -->


Technically, it is convenient to differentiate between the graph and its geometric realization, which is called a neighborhood skeleton. The neighborhood skeleton of V is obtained by connecting, with straight line segments, thoii o  o os ois d s od ing neighborhood graph. We will use both terms alternatively without, we hope, any confusion. It is worth noting that the term neighborhood graph is also used, with a different and unrelated meaning, in graph theory; see [4].

The neighborhood of an edge is usually defined using the concept of distance. In this paper, we will use the metrics Lp, 1 &lt; p &lt; ∞, L1, and L∞ to measure the distance δ(x, y) between points x = (x...,xd) and y = (y1, ..,yd) in Rd. The distance in the metric Lp is defined as δp(x, y) = Σd=1|xi − yi}1/p. In L1 and L∞ the distance is defined by δ1(x, y) = Σd=1|xi − yi|, and δ∞(x, y) = max1≤i≤d|xi − yi respectively. Some concepts and results presented in the paper hold for more general metrics. The distance δ(p, q) will be also called the length of pq. Furthermore, B(x, r) denotes an open sphere centered at x with radius r, i.e., B(x, r) = {y : δ(x, y) &lt; r}. A closed sphere is defined as B(x, r) = {y : δ(x, y)≤r}. In R2 both a sphere and its boundary will be called, without any confusion, a circle.

Below we will define, within this framework, relative neighborhood graphs, Gabriel graphs, and β skeletons. Many interesting variants will be given in Section VI. We begin with an alternative definition of the RNG.

#### A. Relative Neighborhood Graphs

Let Λp,q = B(p, δ(p, q))∩B(q, δ(p, q)); Λp,q is called a lune. The relative neighborhood graph of V, the RNG(V), is a neighborhood graph with the set of edges defined as follows:

$$( p , q ) \in E \text { if and only if } \Lambda _ { p , q } \cap V = \emptyset . \quad ( 1 ) \quad \text {A} \ \{ \begin{matrix} 1 \end{matrix} \}$$

Note that the above definition is equivalent to one given in the introduction.

As a historical digression, let us mention that lunes, as intersections of circles, have been the object of intense study since the times of ancient Greeks. In contrast to a circle (which cannot be squared with a straight edge and compass) Hippocrates of Chios (circa 440 B.C.) showed that certain types of lunes could be squared [5]. Furthermore, the type of lune used in the RNG, traditionally referred to as the Vesica Piscis, was used with symbolism as a basic design element in the floor plans of gothic cathedrals [6].

It is immediate that an edge pq is in the RNG(V) if there is no triangle ∆pqv, v∈V\{p, q}, with pq the strictly longest edge. In Euclidean spaces, relative neighborhood graphs can be equivalently defined by means of angles; we will return to this issue in Section V.

I

Note that if we change slightly the definition of the neighborhood by using the intersection of closed spheres (rather than their interiors) we obtain a different class of graphs. In fact such a class was defined by Lankford [7] in 1969 and historically relative neighborhood graphs could be viewed as a modification of this class (see [1]). As we will point out in later sections this modification leads to different geometric properties.

#### B. Gabriel Graphs

The neighborhood, called a diameter sphere, is defined 2 V, GG(V), is a neighborhood graph with the set of edges as a  sphere: = B ( y l The  Gabriel  graph  of

$$( p , q ) \in E \text { if and only if } \Gamma _ { p , q } \cap V = \emptyset . \quad ( 2 )$$

In the Euclidean space, pq is an edge in GG(V) if there is no triangle ∆pqv, v ∈ V\{p, q}, with ∠pvq &gt; Yet another equivalent definition is that

$$\begin{array} { r l } { x , g } & { \quad } & { R ^ { d } . } & { p q \in G G ( V ) } \\ { ) } & { = } & { p q \in G G ( V ) } \\ { d by } & { \quad } & { i f \, \delta _ { 2 } ( p , q ) \leq \min \left \{ \sqrt { \delta _ { 2 } ^ { 2 } ( p , s ) + \delta _ { 2 } ^ { 2 } ( s , q ) } \ \colon s \in V \ \right \} . } \\ { x _ { i } - } & { \quad } & { ( 3 ) } \\ { n \, g } & { \quad } & { C _ { i } \cdot \cdot \cdot } \end{array} \, ,$$

Gabriel graphs were introduced by Gabriel and Sokal [8] in a context of geographic variation analysis.

#### C. β Skeletons

Kirkpatrick and Radke [9] defined a parameterized family of neighborhood graphs called β skeletons. The neighborhood Up,g(β) is defined, for any fixed β(1≤β &lt; ∞), as the intersection of two spheres:

$$U _ { p , q } ( \beta ) & = B \left ( \left ( 1 - \frac { \beta } { 2 } \right ) p + \frac { \beta } { 2 } q , \frac { \beta } { 2 } \delta ( p , q ) \right ) \cap \\ B \left ( \left ( 1 - \frac { \beta } { 2 } \right ) q + \frac { \beta } { 2 } p , \frac { \beta } { 2 } \delta ( p , q ) \right ) . \\ \text { (June-based) } \beta \text { skeleton of } V , \, G _ { \ell } ( V ) , \text { is a neighbor-}$$

The (lune-based) β skeleton of V, Gβ(V), is a neighborhood graph with the set of edges defined as follows:

$$( p , q ) \in E \text { if and only if } U _ { p , q } ( \beta ) \cap V = \emptyset .$$

A useful feature of this parametrized family is its monotonicity with respect to β, i.e. Gβ1(V)CGβ2(V) for β1 &gt; β2. It is easy to see that β skeletons contain both relative neighborhood and Gabriel graphs as special cases. Specifically, the RNG(V) = G2(V) and GG(V) = G1(V). In fact, as we will see in Section V, it is possible to design a uniform algorithm for the whole spectrum of β skeletons for 1 ≤ β ≤ 2.

The β skeletons have interesting applications to the analysis of interpoint linkages in empirical networks. Kirkdatss sse  us ts  k ed sng examples of road and airline networks. In particular, a comparison of links in an empirical network with the set of edges in the computed β skeletons for various values of β helps to detect significant patterns.

Lune-based β skeletons can be also defined for 0 &lt; β &lt; 1. To this end, the neighborhood of (p, q) is defined as the intersection of two spheres of radius δ(p, q)/2β which

I


<!-- p:3 -->


Fig. 2. DT(V) with four lunes and the RNG(V).

contain p and q in their boundaries. In fact this extension leads to so-called circle-based β skeletons. For β ≥ 1, the neighborhood Up,g of (p, q) is defined as the union of two spheres of radius β × δ(p, q)/2 passing through p, q. The points p, q are connected with an edge if the neighborhood is empty. The circle-based β skeleton for β ≥ 1 can be constructed in O(nlogn) time; see [9].

## III. PROPERTIES

Relative neighborhood graphs are related to other prominent geometric structures such as minimum spanning trees (M ST) and Delaunay triangulations (DT). The Delaunay triangulation of a set V is defined as the dual graph of the Voronoi diagram of V which is a decomposition of Rd into n cells, n being the number of points in V. A point x is in the cell associated with v ∈ V if for all w∈V\{v}, δ(x, v) &lt; δ(x, w). Two points in the DT(V) are connected with an edge if the boundaries of their Voronoi cells intersect. For definitions and properties of the MST and the DT see for example [10]–[12].

Toussaint showed that in the Euclidean plane M ST(V)⊂ RNG(V)⊂DT(V). This implies, in particular, that the RNG is connected. Fig. 2 illustrates the Delaunay triangulation of a point set and nonempty lunes for those of its edges which are not in the RNG.

These inclusions can be generalized to other metrics and higher dimensions. A crucial step in this direction was made by O'Rourke [13]. Studying the RNG in the L1 metric, he noticed that the dual graph of the Voronoi diagram is not necessarily a supergraph of the RNG in L1 and L∞. Instead, he proposed a definition of the DT directly in terms of the points V. Two points in V are connected by an edge in the DT if there exists a sphere (with respect to the metric at hand) such that its boundary contains these points and no point of V is in the interior of this sphere. This definition is equivalent to the traditional one for the metric Lp in R2 space (see [13] and [14]). Here, for the sake of uniqueness of the DT, a general position of points is assumed. In our context we say that points are in a general position in Rd if no d + 1 of them are coplanar (lie on a common d – 1 flat) and no d + 2 of them are cospherical (cocircular) with respect to the given metric. In some cases it will be possible to relax the general position assumption.

This definition of the DT allows extension of the result of Toussaint [1] that the RNG of a subgraph of the DT to all of the metrics Lp, L1, and L∞ and to an arbitrary dimension; see [13].

Similar relationships hold for β graphs in Lp. More specifically, for R2 and Lp we have MST(V)⊂Gβ(V)⊂ DT(V)(1 ≤ β ≤ 2) (see [15] for Lp and [9] for L2). In particular, the relation holds for Gabriel graphs; see also Matula and Sokal [16].

As we will see in further sections, the fact that the DT is a supergraph of the RNG (and β graphs) turns out to be very useful in designing efficient algorithms for neighborhood graphs.

## IV. SIZE OF NEIGHBORHOOD GRAPHS

It is both interesting and important to know lower and upper bounds for the number of edges in the RNG(V). The results of the previous section give immediate bounds in two-dimensional space. Since the MST is a subgraph of the RNG and the RNG is a subgraph of the DT', we have ((|  (((  )(| t ! Expressing this in terms of n = V we have in Lp that n − 1 ≤ |RNG(V)| ≤ 3n − 6. The upper bound follows from the planarity of the DT(V). Note that a similar argument works for β graphs as well. A more detailed analysis gives the tighter bounds of 3n – 8 for the GG (see [16]) and 3n − 10, n ≤ 8, for the RNG (see Urquhart [17]) in the Euclidean plane. The bounds for the RNG and the GG are tight for an infinite number of n. In the metrics L1 and L∞ the RNG can have Θ(n2) edges; an example has been given by Katajainen [18].

Consider now the case of Euclidean Ra space. As higher dimensional spaces are easier to discuss, we will begin with d ≥ 4. A discussion on the three-dimensional case will be deferred.

The first interesting observation is that the relative neighborhood graphs can be dense in Rd, d &gt; 3. The maximum number of edges of the relative neighborhood graph of n points in Rd, d ≥ 4, is Ω(n2).

Consider a set V in R4 that contains an even number of points with n/2 points of the form (a, b, 0, 0), where a2 + b2 = 1, and n/2 points of the form (0, 0, c, d), where c2 + d2 = 1. Each pair of points from different groups forms an edge of the RNG(V); this shows that the size of the RNG can be Ω(n2). Note that the points are not in general position. By embedding the set V into Rd we obtain this quadratic bound for any d ≥ 4. Clearly, the same Ω(n2) bound holds for all β graphs. The above construction, based on Lenz's example, is standard and has been used by many authors for various spatial graphs.

The problem of estimating the sizes of the RGN and the GG in three-dimensional space is much more interesting. Let us start with the RNG; again we focus on Euclidean space. The following result was the first subquadratic upper bound on the size of the RNG (see [19]): the maximum number of edges of the relative neighborhood graph of n points in d ≥ 3 dimensions is O(n3/2+€) for each ε &gt; 0.


<!-- p:4 -->


of bichromatic closest neighbor pairs would improve the upper bound on the RNG.

This result can be established using upper bounds on the size of unit distance graphs. The unit distance graph of V is a graph with two points connected by an edge if they are in a particular, say, one unit, distance. Recent results by Clarkson et al. [20] show that the size of the unit distance graph of an n point set is bounded by cn3/2+€, where € &gt; 0 is an arbitrary small real number. In fact, they give this bound in a stronger form of O(n3/2(λ6(n)/n)1/4), where λ6 is related to the complexity of Davenport-Schinzel sequences. For more discussion on the size of unit distance graphs in Euclidean spaces, see also Chung [21].

To derive an upper bound, decompose the RNG into subgraphs of edges of the same length. For each subgraph an upper bound can be established based on the results of the size of unit distance graphs. Furthermore, the number of different lengths of edges in the RNG(V) which are adjacent to any vertex is bounded by a constant independent of V. Hence each vertex participates in a constant number of subgraphs and an upper bound of O(n3/2+€) for the total number of edges in the RNG follows. Clearly, any improvement on the upper bound on the size of unit graphs automatically improves the upper bound on the RNG.

As a remark in passing let us mention that subgraphs of the RNG of edges of the same length have other interesting properties. For example the interior of a pyramid spanned by three edges of such a subgraph that share a common endpoint has an empty intersection with the remaining edges of this subgraph. We call this a nonpenetration property.

Agarwal and Matoušek [22] proved an upper bound of O(n4/3) using bichromatic closest neighbor pairs and an interesting technique of computing a "small" family of well-separated pairs which include all edges in the RNG [23]. Let P,Q be two point sets. We say that points p∈P, q∈Q form a bichromatic closest neighbor pair if δ(p, q) = minxeP,y∈Qδ(x, y). Furthermore, we say that P and Q are well separated if there exists a pair of cones C, C' with a common apex, a common axis, and the angle at the apex less than π/3, such that Q⊂C and P⊂C′. The following holds [22]: if P, Q are well separated in Rd, then RNG(P∪Q) has an edge pq, p∈P, q∈Q if and only if (p, q) is a bichromatic closest neighbor pair. Based on the result of Edelsbrunner and Sharir [24], the number of edges in the RNG(P∪Q) in R3, with P and Q well || = || = ud( +  + ε//)  ms) Next, it is possible to cover V⊂R3 by a family of wellseparated pairs (P1, Q1), · · . , (Ps, Qs) with two properties: (i) for each p, q∈V, there is (Pi, Qi) with p∈Pi, q∈Qi; (ii) Σi=1|Pi| + |Qi| = O(nlog2n). Each edge in the RNG connects a pair of bichromatic neighbors in some wellseparated pair of this family. Hence counting the number of bichromatic neighbor pairs in all of the well-separated pairs gives an upper bound on the size of the RNG. Concluding: the maximum number of edges of the relative neighborhood graph of n points in R3 is O(n4/3).

Again, any improvement in the upper bound on the size We do not know about any nontrivial lower bound on the size of the RNG in R3. For the special case of point sets that do not allow equal distances between pairs of points, it is easy to show that the size of the RNG is linear. This observation also applies to point sets for which the number of equidistant neighbors for each vertex is bounded by a common constant; in particular it holds for points in general position. A geometric fact worth noting is that the degree of each vertex of the RNG, if no isosceles triangles are formed, is bounded by a constant. This is also true for Lp, 1 &lt; p &lt; ∞ (see for example [25]). Therefore |RNĠ(V)|≤c|V| for point sets in Rd that do not allow equal distances between pairs of points. Alternatively, the size of relative neighborhood graphs defined by closed lunes is linear.

#### A. Size of Gabriel Graphs

As we remember, Gabriel graphs are supergraphs of relative neighborhood graphs. It appears that Gabriel graphs can have substantially more edges than the RNG already in R3. There are point sets in R3 whose Gabriel graphs have Ω(n2) edges (see [26] and [27]). Therefore the following results holds: the maximum number of edges of the Gabriel graph of n points in d≥3 dimensions is Ω(n2).

An example in [27] gives a point set V which consists of two groups of n/2 points located on two circles. These circles are placed in two orthogonal planes and they pass through each other's center. The points are located close to these centers; this distance can be precisely specified. A construction which uses parabolas, and therefore avoids many cocircular points, was provided in [26]. Consider 2n points on two parabolas; n of them on x = 1 − z2 /4, y = 0 at z = 0 ± €, ±2€ · .· and the remaining n points on the parabola x = y2 /4 − 1, z = 0, at y = 0, ±e, ±2e, · · ., where € is a sufficiently small positive number. Each of the points is extremal on the convex hull of this set of points. With a small perturbation of the points we can preserve density of the GG while placing the points in general position.

Interestingly, for any sęt of n points P in d≥3 dimensions there is a set Q of O(√nlogd-1n) points so that the Gabriel graph of PUQ has at most O(n3/2logd−1n) edges (see [27]). Thus by adding extra points we can reduce the size of certain Gabriel graphs substantially; furthermore this set of points can be effectively found.

#### B. Expected Values for Proximity Graphs

The expected size of Gabriel graphs and relative neighborhood graphs in Euclidean Rd space for various set distributions has been studied, among other graphs, by Devroye [28]. He showed that for all densities lim inf E(|GG(V)|)/|V|≥2d−1(E(γ) being the expected value of a given random variable γ). Furthermore, for most densities E(|GG(V)|) ∼ 2d−1|V|. This result extends a similar result by Matula and Sokal [16], who demonstrated that for points l ~ ( uin     r For relative neighborhood graphs the expected size is estimated by E(|RNG(V)|)/|V|≥Cd + o(1), where Cd is a constant that depends only on d. In particular, for d = 2 the expected number of edges in the RNG(V) is at least (1.27 + o(1))|V|.


<!-- p:5 -->


Several results concerning the expected values for the RNG and the GG, as well as many other geometric graphs, in the unit density Poisson probabilistic model were given in [26].

Let us mention that considerable work has also been done on computing expected values of properties such as the expected length, perimeter, and area of a triangle in the DT. These issues are well covered in Getis and Boots [29]; see also [30].

#### V. ALGORITHMS

A variety of algorithms have been proposed for the RNG in the literature. They are based on ideas developed independently by several researchers. From a retrospective we can identify techniques which are common to several approaches.

A paradigm used in most of the algorithms is a refinement approach. It fits to a framework of filtering (for a general treatment and development of this technique and its application to many fundamental geometric problems see Chazelle [31]). Applications of filtering for the RNG have been described by Katajainen [32].

are contained in the query region. A typical query region can be a sphere, a lune, a simplex, a halfspace, or a box.

The point location or range-search approach is a natural implication of the way neighborhood graphs are defined; a search of the neighborhood of an edge gives complete information as to whether this edge has to be eliminated. The power of this approach for constructing the RNG was recognized by O'Rourke [13]. He employed an efficient data structure for range queries to construct the RNG in the L∞ (for arbitrary dimension) and L1 metrics. The point location approach was also taken by Toussaint, Bhattacharya, and Poulsen [35] to obtain a practically efficient algorithm for computing the Gabriel graph in all dimensions.

As we will see, the difficulty of the RNG problem will depend on whether the given points are in general position. Recall that in our context we say that points are in general position in Rd if no (d + 1) of them belong to a common (d – 1) flat and no (d + 2) of them are cospherical (cocircular) with respect to a given metric.

#### A. Two-Dimensional Space

A straightforward approach to constructing the RNG is to check, for each edge and point, whether this point is in the neighborhood of the edge. The cost of such a procedure is obviously Θ(n3) but this this approach does work for any metric or dimension. (In fact, it works for any neighborhoods for which a membership test costs O(1).)

In this approach the RNG is built in stages (usually two) where a sequence of supergraphs with the RNG as a final graph is constructed. Each supergraph is obtained from the previous one by eliminating edges which cannot belong to the RNG. This elimination, called also a pruning, is either based directly on the definition or uses geometric properties of relative neighborhood graphs.

In fact, common to many algorithms for neighborhood graphs is a general method called the region approach (see [33] for various applications). The main idea of the region approach is to divide space in such a way that each point is associated with a finite number of simple regions and the search for the neighbors of the point in these regions reduces to simple queries. One of the most important general references here is Yao's paper [34], which presents subquadratic algorithms for various proximity problems in Rd, e.g., general geographic neighbors which are particularly useful in algorithms for neighborhood graphs. In addition, the paper illustrates another powerful technique, balancing, i.e., how to trade preprocessing and query costs to minimize the overall processing time.

Often such a process applies other fundamental algorithms, as well as nontrivial data structures and general algorithm design techniques.

Not surprisingly, particularly useful for constructing neighborhood graphs are point location and range searching algorithms. Point location consists in identifying the region, in a partition of the geometric space, where the query point is located. Range search is a problem of counting or retrieving all points from a given collection of points which One can immediately reduce this complexity by a factor of n recalling that the Delaunay triangulation (which has O(n) edges) is a supergraph of the relative neighborhood graph of a given point set; this observation led to the first O(n2) algorithm for the RNG [1].

Clearly the DT(V) is not the only supergraph that can be effectively utilized for constructing the RNG. A family of such graphs can be obtained using a general approach of frames and narrow regions (see Yao [34] and Gabow, Bentley, and Tarjan [33]). A region associated with a point v is narrow if for p, s∈V that belong to this region we have δ(p, s) &lt; max{δ(v, p), δ(v, s)}. Such regions can be obtained, for example, by dividing the space around a given point p into equal sections by eight lines passing through p. In particular, Katajainen [18] used octant neighbors as a supergraph of the RNG. An octant (geographic) neighbor of p in a region r(p) associated with p is a point of V\{p} in r(p) which is closest to p. The octant neighbor graph is obtained by connecting each point of V with its geographic neighbors in all regions. Since an octant neighbor graph can be decomposed into eight planar graphs, its size is linear (in Lp, 1 &lt; p &lt; ∞). Phasing out edges from this graph by testing them against each point leads to an O(n2) algorithm.

Using octant neighbors and a range query algorithm, e.g. [31], [33] [36] for rectangles (intersections of spheres in L1 and L∞), Katajainen [18] derived an O(nlogn + m) output sensitive algorithm for the RNG in L1 and L∞, m being the output size. To achieve a linear space the range searching is organized accordingly to the batching technique described in [37].


<!-- p:6 -->


7

For further results regarding geographic neighbors or the angle restricted nearest neighbor see also [38] and [39].

Probably the simplest way to divide the plane into regions is to use a square grid. The cell technique (see Bentley, Weide, and Yao [40]), which leads to a fast expected time algorithm for many closest point problems, has been used by Katajainen, Nevalainen, and Teuhola [41], [42] (see also [43]) to design a linear expected time algorithm for the RNG in a Euclidean plane. They show that the expected time is linear for the points (in a unit square) generated by a homogeneous Poisson process. Note that the floor function is essential in applying the cell technique.

More Elaborate Elimination Techniques: The first O(nlogn) algorithm for the RNG in L2 was developed by Supowit [44]. Supowit was able to organize the elimination of edges from the DT(V) in O(nlogn) time, matching the cost of building the DT(V). The elimination uses the sweep line technique (see, e.g., [10] and [11]; the sweeping is done in six directions (multiples of π). Assume that we sweep from right to left in the direction parallel to a line l. A sweep status structure T maintains active points (at the beginning T is empty); E is set to the DT(V). During the sweep any encountered point p∈V is inserted into T. Then, for edges e with the left point p (in the order of increasing n u  ud  rk    ut h sat the horizontal line passing through v intersects e, we check if v eliminates e. If e is eliminated then e is removed from E; otherwise v is deleted and the plane is swept further. The above process, repeated in the six directions, is able to extract all edges of the DT(V) which do not belong to the RNG(V) and can be implemented to take O(nlogn) time. This gives an O(nlogn) algorithm, which is optimal. In fact Supowit demonstrated a simple linear time reduction of sorting to the RNG in one-dimensional Euclidean space; the reduction is also valid in Lp.

Using a similar approach, Lee [45] has designed an O(nlogn) time algorithm to construct the RNG in L1 and L∞ metrics. The starting graph is again the Delaunay triangulation, and the assumption that no four points in V are cocircular (in the sense of L1) is essential.

Construction of the GG in the Euclidean plane is simpler. The first optimal O(nlogn) algorithm was given by Matula and Sokal [16], where applications to geographic variation research and clustering were discussed. The algorithm is based on an observation that the Gabriel graph of V contains those edges in the DT(V) which do not intersect their dual Voronoi edges: see Fig. 3. Since the Voronoi diagram and DT(V) can be constructed in O(nlogn) time, the bound follows. Clearly, the method can be extended to Ra.

Another elimination strategy for the RNG has been proposed in [25] and later improved and extended by Jaromczyk, Kowaluk, and Yao [15]. This strategy is based on an interesting structure of edges in the DT(V) that do not belong to the RNG(V). Pick a triangle ∆ in the DT(V) and one of its vertices v. Then check if v eliminates the opposite edge of ∆; call this edge e. If yes, then analyze if any two edges of the triangle adjacent to ∆ along the edge e are eliminated by v. Continue this process until no edge is eliminated by v; the obtained sequence of edges will be called an elimination path of v; see Fig. 4. This process does not necessarily detect all edges eliminated by v. Yet one can prove that each edge not in the RNG belongs to the elimination path for some point in V. If one continues constructing elimination paths for other points it will be noticed that paths that happen to coincide will never split apart. They grow into elimination trees (this term is slightly misleading since some elimination paths can have a cycle). This follows from an observation that if a point eliminates an edge of a triangle, then it may eliminate only the strictly longer of the two remaining edges of this triangle. This special structure allows an efficient elimination of edges not in the RNG. The elimination paths and elimination trees are built to form a so-called elimination forest, which carries all the information about the RNG. A union-find structure is helpful [46].

Fig. 3. DT(V), the Voronoi diagram of V, and GG(V).

Fig. 4. DT(V) and lunes showing an elimination path.

We can think about this construction as a sweeping guided by the shape of the DT(V) rather than by the coordinate system. This sweeping can be accomplished in time O(n) using the Gabow and Tarjan [46] implementation for a special case of union-find structure. If we are willing to sacrifice the linear time of this phase to gain simplicity, we can use another efficient and simultaneously very simple, almost linear, implementation for union-find such as a height ranking with path compression (see [47]).

It is interesting to note that the order of constructing elimination paths and composing them into an elimination forest is irrelevant. In general, different orders will lead to different elimination forests; nevertheless all edges not in the RNG will always be eliminated. An elimination forest is an important structure and can be useful in other algorithms.


<!-- p:7 -->


Recently, Hwang [48] used the idea of elimination paths to construct the RNG in a divide and conquer fashion. Elimination forests are carried over through the levels of recursion.

In view of linear expected time algorithms to construct the DT(V) for some distributions of points (see [32], [49], [40], and [50]), the idea of elimination forests and the results of [15] give a simple O(n) expected time algorithm for β-graphs.

We start with the set of all edges adjacent to the vertex v. A currently shortest edge e is found and all edges of the length equal to e are stored. Next all edges longer than e that form with e an angle less than are discarded; clearly they do not belong to the RNG. For the remaining (longer than e) edges the same process is repeated until no edges are left. At this moment edges of the same length are grouped into orbits. Clearly, by the construction, the number of orbits associated with v is not larger than (2π)/(x) = 6.

We will finish this section with a simple algorithm to illustrate the use of the point location method in the elimination phase. This algorithm finds, for a planar point set, all edges in the RNG that are adjacent to a given vertex v. As we will see in the next section, the algorithm has a natural generalization to three-dimensional space.

Not all edges in the orbits have to be in the RNG and the next phase will discard them. A helpful geometric fact is that if the angle between two adjacent edges e and w (w a shorter edge) is smaller than αw = arccos(2 |w| ) then e 2|e does not belong to the RNG; |e| is fixed for a given orbit. In other words, if for e there is a shorter edge w such that e is contained in the angular section (cone) with the axis w and the angle equal to 2αw, then e is not in the RNG. In this case e is the longest edge in the triangle spanned by e and w. Fig. 5 illustrates this elimination. The edges on the orbit which intersect the perpendicular bisector of e are not in the RNG; each of them forms with w an angle less than αw.

Now the problem reduces to the location of e in the union of angular sectors determined by all edges that are adjacent and shorter than e. After sorting the edges with respect to angles, such a union can be found in a linear time. In fact, edges in all orbits can be sorted in an O(n2) rather than O(n2logn) time. To this end observe that the order of the sn o  ons nd    n s oesn O(n2) time (see [51]). A simple binary search determines in O(logn) steps whether e belongs to this union. Since there are at most six orbits for a given point and at most n edges, the total time to identify all edges in the RNG that are adjacent to a given point v is O(nlogn). Clearly, the same result can be obtained using the Delaunay diagram. We will see in further sections that the above ideas can be extended to the three-dimensional Euclidean case.

In R2 the edge location in the union of angular sectors, or equivalently a point location in the union of arcs, can be accomplished faster, in time proportional to n (as suggested by one of the referees.) Observe that each angle of elimination 2αw &gt; 2π and the corresponding arc occupy 3 at least one third of a circle. Let a, b, c be equidistant points on the circle. We can group the arcs with respect to which of a, b, c they contain (ties can be resolved arbitrarily). The union of arcs in each group can be determined by finding the extremal arc endpoints in time proportional to the number of arcs. Now each point can be located in the union of the arcs in a constant time. Consequently, all edges in the RNG which are adjacent to a given point can be found in an O(n) time.

Fig 5. An orbit and its edges eliminated by u.

For completeness, observe that this result yields immediately an O(n2) algorithm for the RNG in a Euclidean real plane. It is also possible to show that the total number of edges in all the orbits is subquadratic.

We will finish this section by mentioning two special cases.

Supowit [44] considered the RNG problem for convex polygons and he provided an optimal O(n) time algorithm. Note that the same result can be established by combining a linear time construction of Delaunay triangulation for points forming a convex hull presented by Aggarwal et al. [52] with a linear time algorithm for constructing the RNG from the DT [15].

A linear time algorithm for computing the RNG of unimodal polygons, not necessarily convex, was designed by Olariu [53].

#### B. Three-Dimensional Space

A straightforward approach gives an O(n3) time algorithm for the RNG in three dimensions (see [1]).

In a manner similar to the two-dimensional case this time complexity can be reduced by constructing a "small" supergraph of the RNG.The first such construction was given by Supowit [44] for Euclidean spaces. The space around each point of v∈V is partitioned into a number of narrow regions. Recall that a region is narrow if for p, s∈V that belong to the region of v we have δ(p, s) &lt; max{δ(v, p), δ(v, s)}. The number of regions is independent of n. For points in general position, based on such a partition, it is easy to construct a linear size supergraph of the RNG in O(n2) time. Note that it can be also done in o(n2) time using the technique of Yao [34]. Specifically, the only candidate for the RNG in a given region is the edge joining v with the point in this region closest to v (the geographic neighbor). Because of the assumption about general position, in each region there is only a bounded (by a constant) number of such points. Note that the original assumption in [44] is that there are no isosceles triangles formed by the points in a given set. The algorithm works also if the number of equal length edges adjacent to each vertex is bounded by a common constant; in particular it holds for points in general position. A straightforward elimination of edges from this graph yields the RNG in total time O(n2). By virtue of the results obtained by Yao [34] and by Gabow, Bentley, and Tarjan [33], Supowit's algorithm extends to Lp metrics.


<!-- p:8 -->


geographical nearest neighbor graph is used as a departure point. Recall that the GNG is a linear size supergraph of the RNG (see [44]), and it can be constructed in O(n2−a(d)(logn)1-a(d)) (see [34]). The next stage, an elimination, uses an arrangement of (d + 1)-dimensional hyperplanes. The hyperplanes are the images, in the inverse transformation, of those spheres which bound lunes generated by the edges of the GNG. Next the algorithm identifies lunes which contain a point from V. By wellknow properties of the inverse transformation, the point I  n s ees  cn   oens translated into a location problem in the corresponding arrangement of hyperplanes in Rd+1. Su and Chang used an algorithm from Dodge [55] and the balancing technique typpt os tns ons ops optins ion queries.

Elaborating on the above ideas and using balancing, Smith [26] showed how the time complexity can be reduced to O(n23/12logn); general position is assumed.

A similar method can be used for constructing the Gabriel graph of V in Euclidean spaces. A useful observation here is that pr  GG(V) if there is q such that ∠pqr &gt; π/2. Starting with the shortest edge pq adjacent to p, we e    s   s    s iterated for all currently shortest noneliminated edges until no more edges adjacent to p are eliminated. The edges, E, which remain after such elimination are in the GG; the cost associated with each edge in E is proportional to n. It gives an O(|En) algorithm for the GG in the Euclidean Ra space. The cost of the algorithm is Ω(n2) since the GG is connected and has at least n – 1 edges. The algorithm does not depend on general position of input points. A variant of this algorithm is presented in [26].

Using another approach, Jaromczyk and Kowaluk [25] demonstrated a simple O(n2) algorithm for points in general position in Lp (the original assumption was a lack of isosceles triangles). For each point p, from the set of edges adjacent to p.we remove iteratively the currently shortest edge pq and eliminate all edges pr such that δ(p, r) &gt; δ(q, r). Each such pr is the longest edge in the triangle ∆pqr and therefore is not in the RNG. The RNG is the collection of edges which survive such a test, i.e., are never eliminated in this process. When this process terminates the number of edges adjacent to p is bounded by a constant, provided that there are no two equal distances between points of V (or their number is bounded by a constant). This follows from the fact that neither of pw, pq∈RNG(V) is the longest edge in the triangle ∆pwą and the angle opposite to the longest edge is greater than some constant c(d, Lp)×n. Hence the overall cost of the algorithm is O(c(d, Lp)n2).

A subquadratic algorithm for the RNG of points in dDSin  n  O  sa Sdes ng [54]. The algorithm constructs the RNG(V) of an n point set in a Euclidean d-dimensional space (d being fixed) in time O(n2−a(d)(logn)1−a(d)), where a(d) = 2−(d+1). The points are assumed to be in general position. The Using faster existing algorithms for the nearest neighbor search in three-dimensional spaces they obtained an O(n29/15logn) time algorithm to construct the RNG of points in R3 (recall that general position is assumed).

Extending the idea of elimination based on angles between edges, Jaromczyk and Kowaluk [19] demonstrated an O(n2logn) time algorithm for arbitrary point sets in three-dimensional Euclidean space. The algorithm finds for each vertex v all edges of the RNG adjacent to v. As in the two-dimensional case, orbits of edges of the same length are formed (see the previous subsection). The number of orbits for each vertex is bounded by a constant independent of n. This constant is equal to the maximum number of segments with a common endpoint which form angles not less than

The orbits associated with v contain all edges in the RNG adjacent to v. However, they can also include extra edges. The size of the graph determined by the union of the orbits for all the vertices is O(n3/2+€); see [19] or Section IV. A straightforward elimination leads to an O(n5/2+€) algorithm. We can capitalize, however, on a special form of orbits and perform this elimination faster.

Recall that if the angle between two adjacent edges e and does not belong to the RNG. This fact, which' we have used to derive a two-dimensional algorithm, can be utilized in this situation as follows. Consider an orbit of v and let e belong to this orbit. For each edge w with an endpoint v which is shorter than e, take an open cone of revolution with its axis containing w and the angle at its apex equal the union of such cones (with v added). w  (w a  shorter edge)  is  smaller  than  arccos( #), then  e to 2 x arccos( Clearly, e is not in  the RNG if  e  is in

Alternatively, we can use spherical cups obtained by intersecting the cones with the boundary of the sphere B(v, le|) and locate the endpoint of e in the union of these cups. A suitable stereographic projection transforms the problem to a point location in the union of (open) circles. To solve this problem, we can use Voronoi diagrams in Laguerre geometry [56] or power diagrams [57]. After O(nlogn) preprocessing such a location can be done in O(logn) time per point. Hence for each vertex v the cost of eliminating extra edges from orbits is O(nlogn), which gives in total O(n2logn) time.


<!-- p:9 -->


Table 1 The Relative Neighborhood Graphs—Summary of Results

| Dimension   | Metric   | Complexity   | Reference       | Remarks          |
|-------------|----------|--------------|-----------------|------------------|
| R2          | L P      | n2           | PI, [411, ~ 3 1 | [41] in L2       |
| R2          | L P      | n log n      | P I             | in L2            |
| R2          | L P      | n            | ~ 5 1           | when DT is given |
| R2          | Lm, L1   | I n2 log n I | 1131 I          |                  |
| R2          | Lm, L1   | I n log n I  | [451 I          | general position |
|             | L2       |              |                 |                  |
|             | L2       | I n2 log n I | (191 I          |                  |
|             | L2       | n29/15 log n | P I             | general position |
|             | L2       | ,7/4+€       | [221            |                  |
|             | L2       | ,3/2+        | [221            | general position |
|             | L C C    | I n2 log n I | ~ 3 1 1         | general position |
|             | L C C    | n(1og n)'    | [261            | n(logn)d-' in Rd |

Katajainen and Nevalainen [58] designed a simple algorithm based on Urquhart [59]. The algorithm works in d-dimensional spaces and the metrics L1, Lp, L∞. Interestingly, its time complexity analysis uses the region approach. In particular, they showed that in R2 the running time is bounded by O(n5/2). Using the methods of [19], we cat  a  t tt  t  time complexity for arbitrary point sets in three-dimensional Euclidean space.

It is also possible (see [22]) to construct the RNG(V) in R3 in time O(n7/4+€), € &gt; 0, for arbitrary point sets.

In the L∞ metric the elimination phase can be based on fast point queries in d - rectangles (intersections of spheres in L∞). In particular, in Rd the RNG can be constructed in O(n(logn)d-1) time; a general position of points is assumed (see [61]).

The results discussed in this section for the RNG are summarized in Table 1, where "big-O" notion is omitted.

## VI. VARIANTS AND SPECIAL CASES

The concept of relative neighborhood as a method to define graphs can be extended and modified in numerous directions. Usually modifications regard either elimination rules or the shape of a neighborhood. This section will discuss some of the interesting variants. The first group of modifications pertains to the relaxation of elimination rules.

#### A. k-Relative Neighborhood Graphs

Let Λp,q = B(p, δ(p, q)) ∩ B(q, δ(p, q)); i.e., Λp,q is a lune. The edges of the k-relative neighborhood graph of V, k – RNG(V), are defined as follows:

$$( p , q ) \in E \text { if and only if the cardinality of } \\ \Lambda _ { p , q } \cap V \text { is less than } k .$$

Clearly, the 1 − RNG(V) is the RNG(V); see Fig. 6. Properties and applications of k – RNG(V) in Euclidean two-dimensional spaces are discussed in [62]. In general, k – RNG graphs in R2 can contain intersecting edges yet their size is linear with respect to kn.

A simple probabilistic argument showing that the size of the k − RNG in R3 is O(k2/3n4/3) was given in [22].

Noticeable progress in three-dimensional and higher dia ay     a ds es Matoušek [22]. In the first step a family of well-separated pairs of subsets of V is constructed (see Section IV for the definitions of the well-separated pairs and bichromatic neighbors). This family has a property that each RNG edge connects some bichromatic closest neighbors in a separated pair of the family. Therefore, computation of all bichromatic closest neighbors for all the points in all the separated pairs gives a supergraph of the RNG. To eliminate from this supergraph edges which are not in the RNG(V), an algorithm for a fast point location in an arrangement of lunes is designed. It uses a data structure based on the partitioning scheme of Chazelle et al. [60] and an arrangement of spheres based on the work of Clarkson et al. [61]. If points are in general position then: for a set V of n points in R3 the RNG(V) can be computed r py      f (   n general position the RNG(V) can be constructed in time O(n2(1−a+1+e).


<!-- p:10 -->


Fig. 6. RNG and 2 - RNG.

Consider a subset R ⊂ V of r = [x 」 points; each subset chosen with equal probability. A pair of points p, q which form an edge in the k - RNG(V) are also an edge in the RNG(R) if p, q ∈ R and ∆p,q ∪ V is empty. The probability of such an event is at least

Therefore, the expected size of the RNG(R) is bounded by Ω(M/k2), where M is the size of the k − RNG(V). However, in R3 the size of the RNG of an r = [n/k] element set is O(r4/3) (see Section IV). Hence M = O(k2/3n4/3).

$$\begin{array} { c } \text {probability of such an event is at least} \\ \\ \left ( \begin{matrix} n - k - 2 \\ r - 2 \end{matrix} \right ) / \left ( \begin{matrix} n \\ r \end{matrix} \right ) = \Omega ( 1 / k ^ { 2 } ) . \\ \end{array}$$

Clearly, a similar argument can be used for other kneighborhood graphs. For example a bound of O(kn) can be established for the k – RNG in R2. Let us note that the same bound was also proved in [62] based on the size of the k-geographic neighbors graph.

An O(n5/3logn) algorithm to construct the k − RNG, for a fixed k, has been presented in [62]. The algorithm has a traditional organization and works in two stages. At first the k − GNG(V), the k-geographical neighborhood graph of V, is constructed. The k – GNG is a generalization of the geographical neighborhood graph and is defined as follows. Let W be a narrow region. A point p ∈ V ∩ W is a kth nearest geographical neighbor of v in W if there are exactly k - 1 points of V in W which are closer to v than p. The k – GNG is obtained by connecting points with their first through kth nearest geographical neighbors. The k-geographical neighborhood graph is a supergraph of the k - RNG and it can have at most 18kn edges (see [62]). The construction of the k – GNG is modeled on an algorithm for the geographicał neighborhood graph presented in [34].

In the second stage the lunes determined by edges in the k—GNG are preprocessed for supporting fast point location queries. Using the balancing technique it is possible to preprocess lunes and perform all n point locations in the lunes, in order to eliminate edges which have at least k neighbors, in time not exceeding the cost spent on constructing k – GNG.

Recently, Agarwal and Matoušek [22] showed that the k – RNG of a set of n points in Rd in general position, where k is a fixed constant, can be computed in time (n i   o      -ion then the k − RNG can be computed in time O(n4/3+€) for points in Rd, and in time O(n7/4+€) for points in R3.

In Chang et al. [63] the k — RNG is studied in an interesting context of bottleneck Hamiltonian cycles. For an application of the k — RNG to Euclidean bottleneck matching and biconnected edge subgraphs, see [64] and [113].

A minmax (bottleneck) Hamiltonian cycle of a graph is a Hamiltonian cycle which minimizes the length of its longest edge over all Hamiltonian cycles of this graph. Consider a complete graph induced by a set V of points in a Euclidean plane. Such a graph has a minmax Hamiltonian cycle which is contained in the 20 – RNG(V) (see [63]). In fact, there is a transformation which after a finite number of steps produces, from any given minmax Hamiltonian cycle, a minmax Hamiltonian cycle which is a subgraph of the 20– RNG. Correctness of the transformation is based on an interesting observation related to narrow regions. Consider a set S of points contained in cone(v, ), ∠(σ, ) &lt; α and t the apex of the cone. Assume that for all points p, q ∈ S the following properties hold, r &gt; 0 : δ(t, p) ≥ r, δ(p, q) ≥ r, δ(p, q) ≥ δ(t, p) − r, and δ(p, q) ≥ δ(t, q) − r. Then there exists a constant c depending only on α such that |S| &lt; c (see [63]).

Now consider a minmax Hamiltonian cycle H and its longest edge pq not in the k − RNG. (The value of k can s  : (   =  ds n the k – RNG(V), the lune Λp,g contains at least k points, t1, · · · , tm , of V. If any pair ti, t j is connected by an edge in H, then we can replace pq by a sequence pti, titj, tjq; the new cycle is again a minmax Hamiltonian cycle. Otherwise, let w be a direct predecessor of ti in H; assume that H has a counterclockwise orientation. If k is large enough, then by virtue of the above observation on the narrow regions there are two points wi, wj that satisfy at least one of the following conditions:

- a) δ(q, wi) &lt; δ(p, q), or
- b) δ(wi, ωj) &lt; δ(p, q), or
- c) δ(wi, wj) &lt; δ(wi, ti) or δ(wi, wj) &lt; δ(wj, tj).

In each case the edge pq can be replaced by other edges without increasing the length of the longest edge. For example, in case (b) the edges pq, witi, wjtj can be substituted with pti, titj, wjq. Moreover, each application of this transformation replaces a longest edge not in the k - RNG by some shorter edges. Hence, after a finite number of steps we obtain a minmax Hamiltonian cycle which is a subgraph of the k – RNG.

A related and important problem of constructing a minmax length triangulation, i.e., a triangulation which minimizes the longest edge, has been studied by Edelsbrunner h y  t     a ont set V in R2 has a minmax length triangulation which is a supergraph of the RNG(V). The lemma suggests that construction of a minmax length triangulation can start from the RNG(V). It leads immediately to a cubic time construction when existing dynamic programming l (  nm l und  ud also provides the first polynomial time algorithm for this problem. Furthermore, as demonstrated in [65], an even faster quadratic time algorithm can be developed. The algorithm works for a general class of metrics.

#### B. k-Gabriel Graphs

In a similar fashion k-Gabriel graphs can be introduced B( +q, (p,9); i.e. Γp,q is a (see [67]). Let Γp,q = 1 2 diameter sphere. The edges of the k-Gabriel graph of V, the k – GG(V), are defined as follows:


<!-- p:11 -->


$$( p , q ) \in E \text { if and only if the cardinality of } \\ \Gamma _ { p , q } \cap V \text { is less than } k . \\ \text {Properties of the above} \text { and applications to bounded}$$

Properties of these graphs and applications to bottleneck biconnected graphs, and Eulidean bottleneck matchings are discussed in [67], where an O(k2nlogn) time construction for the k – GG in R2 is presented.

#### C. Constrained Relative Neighborhood

Graphs and Gabriel Graphs

An interesting extension of relative neighborhood graphs has been investigated by Su and Chang [68]. Let V be a set of n points in a plane and T be a set of nonintersecting line segments with their endpoints in V. Clearly, the number of segments in T is of order O(n). We say that two points in V are visible if their connecting line segment does not intersect any edge in T.

The constrained relative neighborhood graph of V U T, CRNG(V ∪ T), is defined as a graph with vertices V and the set of edges E such that (p, q) ∈ E if and only if:

### 1) (p, q) ∈ T, or

2) p, q are visible and Λp,q does not contain points in V which are visible from both p and q.

Figure 7 illustrates a polygon T, the RNG(V) of its vertices, and its CRNG. Interestingly, a special case of the CRNG, where T' forms a simple polygon, was introduced much earlier in [69]. Because of its applications to pattern recognition we will discuss this special case separately.

It appears that CRNG(V ∪ T) is a subgraph of the constrained Delaunay triangulation of V and T (see [68]). The constrained Delaunay triangulation of V and T, CDT(V, T), contains all segments in T. In addition, it includes all edges (p, q) such that p, q are visible and there is a sphere with its boundary containing p, q which does not contain points of V visible from both p and q. The CDT(V, T) can be constructed in O(nlogn) time (see [12]). Using a process similar to Supowit's sweep, it is possible to eliminate edges from CDT(V, T)\CRNG(V∪ T) in O(nlogn) time.

Constrained Gabriel graphs, CGG, are defined in an analogous fashion. They can be obtained from the CDT in O(n) time. To this end it is sufficient to consider obtuse and right angle triangles in the CDT. After eliminating from these triangles the longest edges which are not in T we obtain the desired CGG [68].

Fig. 7. A polygon, the RNG of its vertices, and its CRNG.

hood graphs discussed earlier in this section. Let P be a simple polygon and V be its set of vertices. We set the neighborhood Up,q to be the lune Λp,q·

The relative neighborhood decomposition of P, RND(P), is defined as a set of these edges pq which are diagonals of P, and if v ∈ Λp,q then at least one of pv, qv intersects the boundary of P.

The concept of the RN D has been introduced by Toussaint [70]. Intuitively, we can think that an edge of P is an opaque barrier. A point can have an impact on the segment pq only if no barrier separates them.

The RND can be used to decompose simple polygons into perceptually meaningful components and is thus useful in pattern recognition.

ElGindy and Toussaint [69] discussed properties and several algorithms for the RND as well as the Gabriel decomposition, which is defined analogously. In particular, they show that the RN D(P) is a planar graph and that it can be constructed in time O(n2) (n being the number of edges in P).

The RND can be viewed as a special case of a constrained relative neighborhood graph. Based on algorithms for the CRNG, it can be constructed in time O(nlogn).

#### E. The Rectangular Influence Graph

Ichino and Sklansky [71] defined the rectangular influence graph, RIG(V), assuming as the neighborhood Up,q of points p, q the smallest coordinate oriented rectangle containing these points. They showed that the RIG(V) is a supergraph of GG(V) and therefore also a supergraph of the RNG(V) in Lp. However, in general, the rectangular influence graph is not a subgraph of the DT.

In addition, variants such as an interclass RIG and mutual neighborhood graphs were introduced. In our terminology, the mutual neighborhood graph can be viewed as a graph defined over two point sets V1 and V2. The mutual graph MNG(Vi|V2) has edges for these pairs of points in V1, which neighborhood does not contain points from V2.

Clearly, the whole concept can be extended to β graphs. Furthermore, using the elimination forest structure of [15], the constrained β graph (1 ≤ β ≤ 2) can be constructed in an O(n) time.

Several applications of the RIG, the interclass RIG, and the MNG are presented in [71]. In particular, it is argued that these graphs are useful in the design of piecewiselinear classifiers and in clustering methods applicable to mixed feature variables.

#### D. Relative Neighborhood Decomposition of a Simple Polygon

The relative neighborhood decomposition of a simple polygon is connected to the constrained relative neighbor- In this context we also mention direct dominance pairs, which are applicable to the rectangle enclosure problem. Algorithms for reporting all direct dominance pairs are given in the work by Gutting, Nurmi, and Ottman [72].


<!-- p:12 -->


#### F. Other Graphs

There is a large family of neighborhood graphs that we have not mentioned here.

This family includes such important and interesting graphs as the sphere of influence graph, introduced by Toussaint [73] and α graphs introduced by Edelsbrunner, Kirkpatrick, and Seidel [74]. Both graphs are useful in dot pattern and shape analysis [75]. They also have several interesting graph-theory properties [76], [73], [74]. We expand on these graphs in Section VII.

Several variants of β graphs are discussed in [9]. The ideas in [9] can be generalized and expanded on in various directions. Some discussion of possible generalizations, in particular with an eye toward applications, is given in [75].

A recent paper by Veltkamp [77] proposes a parametrized family of γ-neighborhood graphs. The γ graph can be reduced to the circle based β skeleton, to the DT, or to the convex hull for specific parameter values.

An interesting variant of a digital geometry version of the RNG applied to computer vision is given in the work by Toriwaki and Yokoi [78]. Planar neighborhood graphs without cycles are discussed in [114].

## VII. APPLICATIONS

We have already touched briefly on some applications as different neighborhood graphs were introduced. In this section we consider applications in more detail. We will discuss graphs and structures which are related to the RNG as members of the same family belonging to computational morphology.

#### A. Morphology and Computer Vision

1) Dot Patterns: The central problem in computer vision begins with a gray-level intensity array of a visual pattern or scene and culminates with a description of the scene. This description is a marriage of the intensity array itself (the bottom-up or data-driven information) and the objective for which it is viewed (the top-down or conceptually-driven information). Considerable attention has been devoted to low-level vision, i.e., the aspect dealing with the analysis of the intensity array up to the level of figure-background separation. The main purpose of analyzing an intensity array at this level is to form a low-level description that is independent of any final conceptually-driven description. Marr [79] has called such a description a primal sketch of the intensity array. One class of patterns or scenes which had been studied extensively is the so-called dot pattern.

When dots in the plane have a finite diameter so that they are visible, and when they are fairly densely distributed in some region in the plane, then a human observer is quick to perceive the "shape" of such a set. These sets are usually referred to as dot patterns or dot figures. A polygonal description of the boundary of the shape is referred to as the shape hull of a dot pattern, where the vertices are given as the coordinates of the dot centers.

There are two versions of the shape hull problem. In one there are no "holes" in the dot pattern and the dot pattern is "simply connected"; hence the shape hull is a simple polygon. On the other hand, in the more difficult o aoes ,, e o, o aoa exist. To add to this difficulty, in some instances illusory contours are perceived between "disconnected" components as illustrated by Kennedy and Ware [80]. For more details and early approaches see Toussaint [81] and Medek [82].

In addition to describing the shape or structure of a set of points by its shape-hull or external shape we may also use the skeleton or internal shape. An early step in this direction was taken by Zahn [83] with the minimal spanning tree. More recent approaches have used the RNG [71].

Most of the early approaches suffer from various deficiencies such as computational inefficiency or dependence on too many parameters which must be fine-tuned in order to obtain satisfactory performance for the task at hand.

A very elegant definition for the external shape of a set of points was put forward by Edelsbrunner, Kirkpatrick, and Seiel atd  td l l l ton of convex hulls that they call α hulls. The α hull of a point set is based on the notion of generalized disks in the plane. For a real number α a generalized disk of radius is a (standard) disk of radius 1 if α &gt; 0. If α &lt; 0 it is the 1 α complement of a disk of radius 1. It is half-plane for α = 0.

The α hull of a point set S is defined to be the intersection of all closed generalized disks of radius 1 that contain all the points of S. The convex hull of S is exactly the 0 hull. The family of α hulls includes a spectrum of enclosing regions of S.

A combinatorial variant of the α hull defined in [74] is called the α shape. It can be viewed as the boundary of the α hull with curved edges replaced by straight edges. Unlike the family of α hulls, the family of distinct α shapes has only a finite number of members. They provide a spectrum of progressively more detailed descriptions of the external shape of a given point set; they can be calculated in O(nlogn) time for n point sets. For more details see [74] and [11].

Note that the idea of α hulls is closely related to the notions of opening and closing sets, found in mathematical morphology (see [84]–[86]). The two-dimensional α shapes are connected to the dot patterns (see [87] and [88]) and to the circle diagrams utilized in cluster analysis (see [89]). An extension of α shapes to R3 and an O(n2) algorithm that constructs for n points a representation of the α shapes for all values of α have been presented by Edelsbrunner and Mücke [90]. The shape hulls are also used in muscle fiber analysis [115]. A digital α-hull introduced by Saito et al. [116] was used for shape feature analysis.

A new methodology for describing the internal shape of point sets was outlined by Kirkpatrick and Radke [9], where the notion of β graphs was introduced.

Another simple and elegant method for extracting the shape of a dot pattern is due to Rosenberg and Langridge [91]. The algorithm is free of parameter tuning. It is limited, however, to single objects; its computational complexity is O(n4).

-e  rouddt t oars  oupat a upssaa ture the essence of the primal sketch for dot patterns of arbitrary complexity. It seems that the graph, which is called the sphere-of-influence graph, suffers from none of the drawbacks of the previous methods. It delivers either the "internal" structure in the form of a "skeleton" or the "external" structure in the form of a "shape-hull" as a function of what the data look like (see Fig. 8). Secondly, it can be applied to a scene of disconnected objects and it works without tuning of parameters. In addition, the graph affords a graph-theory explanation of certain visual illusions, such as the Mueller-Lyer illusion.


<!-- p:13 -->


Fig. 8. The sphere-of-influence graph.

Let V = {p1, · ·· , Pn} be a finite set of points in the plane. For each point p ∈ V, let rp be the closest distance to any other point in the set, and let Cp be the circle of radius rp centered at p. The sphere of influence graph is a graph on V with an edge between points p, q if and only if the circles Cp, Cq intersect in at least two places. The sphere of influence graph has at most cn edges, where c is a constant (see [76]). This constant is not greater than 17; for a discussion of this issue see [76] and [92], as well as [93] and [94]. It implies, as was observed by ElGindy, that the algorithm of Bentley and Ottman [95] for reporting intersections can be used to find the sphere of influence graph in O(nlogn) time. This is optimal in the decision tree model (see [76]).

A general family of graphs related to the sphere-ofinfluence graph, although based on a slightly different definition and with a different purpose, has been studied in [92] and [96].

Guibas, Pach, and Sharir [97] have recently generalized the sphere-of-influence graph to kth sphere of influence. Given a set V of n points in Rd, the kth sphere of influence of a point x ∈ V is the smallest closed ball centered at x and containing more than k points of V (including x). The case k = 1 gives the standard sphere of influence. The kth sphere-of-influence graph Gk(V) of V is a graph whose vertices are the points of V, and two points are connected by an edge if their kth spheres of influence intersect. They show, extending results for the first sphere-of-influence graph from [76] and [92], that there is a constant cd &gt; 0 depending only on d such that the number of edges in Gk(v) is at most cdkn. They also give an algorithm that computes the kth sphere-of-influence graph in time O(n2− 1+(a+2)/] +€ + knlog2n) for any ∈ &gt; 0.

Even for k = 1 the sphere-of-influence graph need be neither connected nor planar. In [98] trees that are sphereof-influence graphs are characterized. The geometric notion of the sphere of influence has also been modified to a graph theory sense by Harary et al. [99].

2) Texture Discrimination: There are many computer vision problems where the patterns are neither dot patterns nos aitr s i raets rrs u atr s lns in satellite image analyses of the earth.

Toriwaki and Yokoi [78] have applied the RNG and the GG to the problem of discriminating between different textures.

3) Monotonic Search Networks: A graph embedded in the plane is called monotone if for every pair of vertices p, q t  s  = - =     uat δ(vi, q) &gt; δ(vi+1, q) for i = 1, · · . , k − 1.

A useful property of monotone graphs is that the distance can be used to guide efficient traversal of the graph. Dearholt et al. [100] have used a monotone graph called the monotonic search network as the underlying structure for an associative data base for computer vision. Kurup [101] showed that the Delaunay triangulation is a monotone graph which in general is not true for the GG, the RNG, and the minimum spanning tree. He observed, however, that the RNG can be extended to a monotone graph, which is minimal in some sense, and consequently it can be used as a base for monotonic search networks [102], which find application in the design of data bases for computer vision.

#### B. Geographic Analysis

Underlying the study of geographic analysis is spatial analysis [29] the field of study which examines the spatial structure and association of phenomena. This is a large and well-established area of geography. The RNG and other proximity graphs may revolutionize the manner in which the spatial analysts do their work. For a survey of applications of neighborhood graphs to spatial analysis the reader is referred to the work by Radke [75].

#### C. Pattern Classification

In the nonparametric classification problem, a set of n feature vectors is available. It is taken from a collected data set: {X, Θ} = {(X1, Θ1), ..., (Xn, Θn)}, where Xi and Θi denote the feature vector of the ith object and the class label of this object, respectively. One of several powerful classification techniques is the so-called nearestneighborhood rule (NN rule) [103], [104]. Let Y be a new object (vector feature) to be classified. The NN rule classified Y as belonging to class Θk, where Xk ∈ {Xi, · · · , Xn} is the feature vector closest to Y.

In the past some practitioners avoided using the NN rue a  e e   e o store all data {X, Θ}. Both of these problems have been eradicated with techniques from computational geometry. Various methods exist for finding nearest neighbors including an optimal O(nlogn) algorithm [105]. For other approaches see also [106] and [107]. Furthermore, not all


<!-- p:14 -->


r

the "training" data {X, Θ} are required to be stored. Methods have been developed [35] to edit redundant members of {X, Θ} in order to obtain a relatively small subset of {X, Θ} that implements exactly the same decision rule as using all of {X, Θ}. Such methods depend heavily on the use of Voronoi diagrams and proximity graphs such as the RNG and the Gabriel graph [35].

Let us finish with a few further applications of the RNG. Lee [108] applied the RNG to computing shortest rectilinear paths; it is an element of a design problem in VLSI. In Lefkovitch [109] the RNG are used in cluster analysis in ecology. Finally, in [110] and [111] the RNG found an application in comparing dissimilarity matrices.

## VIII. CONCLUSION

We have reviewed in this paper results and algorithms for neighborhood graphs. Although we have focused on the relative neighborhood graphs the other members of this rich family of graphs have been discussed as well.

Many interesting questions remain open. Among them there is a problem of tight bounds for the number of edges of the RNG in R3. The best established upper bound is superlinear. On the other hand only a trivial linear lower bound is known. In this context it would be interesting to develop optimal or output sensitive algorithms for the three-dimensional RNG as well as the GG. Also, threedimensional β skeletons deserve more research. Another area which needs further study is the question of recognition of proximity graphs, i.e., given a class of proximity graphs and a graph G, determine if G belongs to this class. The known results concern the Delaunay triangulation [112] and f-factors of point sets in the plane [92].

In view of the widespread applications of neighborhood graphs to computational morphology, geographical analysis, and pattern analysis, the design of robust algorithms and implementations for the neighborhood graphs is a challenging problem.

####### ACKNOWLEDGMENT

The authors would like to thank the anonymous referees, whose valuable remarks were essential in improving the presentation of our paper. The first author would like also to thank K. Senn for her professional help in locating many of the references.

####### REFERENCES

- [1] G. T. Toussaint, "The relative neighborhood graph of a finite planar set," Pattern Recognition, vol. 12, pp. 261–268, 1980.
- [3] D. W. Dearholt and F. Harary, Eds., Proceedings of the First Workshop on Proximity Graphs. Computing Research Laboratory, New Mexico State University, 1991. Memoranda in Computer and Cognitive Science MCCS-91–224.
- [2] G. T. Toussaint, "Some unsolved problems on proximity graphs," in Proceedings of the First Workshop on Proximity Graphs (New Mexico State University, Las Cruces), 1991.
- [4] J. W. Boland, R.C. Brigham, and R. D. Dutton, "The difference between a neighborhood graph and a wheel," Congressus Numerantium, vol. 58, pp. 151–156, 1987.
- [5] W. Dunham, Journey Through Genius: The Great Theorems of Mathematics. New York: Wiley, 1990.
- [6] R. Lawror, Sacred Geometry: Philosophy and Practice. London: Thames and Hudson, 1982.
- [8] K. R. Gabriel and R. R. Sokal, "A new statistical approach to geographic variation analysis," Systematic Zoology, vol. 18, pp. 259–278, 1969.
- [7] P. M. Lankford, "Regionalization: Theory and alternative algorithms," Geogr. Annals, vol. 1, pp. 196–212, 1969.
- [9] D. G. Kirkpatrick and J. D. Radke, "A framework for computational morphology," in Computational Geometry, G. Toussaint, Ed, North-Holland, 1985, pp. 217–248.
- [11] H. Edelsbrunner, Algorithms in Combinatorial Geometry. New York: Springer-Verlag, 1987.
- [10] F. Preparata and M. I. Shamos, Computational Geometry - Introduction. New York: Springer-Verlag, 1986.
- [12] F. Aurenhammer, "Voronoi diagrams — A survey of fundamenIl o Ss Su S us Su Su v) pp. 345–406, 1991.
- [14] D. T. Lee, "Two dimensional Voronoi diagram in the l1 -metric," J. Ass. Comput. Mach., vol. 27, pp. 604–618, 1980. ~
- [13] J. O'Rourke, "Computing the relative neighborhood graph in the l1 and l metrics," Pattern Recognition, pp. 45–55, 1982.
- [15] J. W. Jaromczyk, M. Kowaluk, and F. Yao, "An optimal algorithm for constructing β-skeletons in lp metric," SÍAM J. Comput., to be published.
- [17] R. B. Úrquhart, "Some properties of the planar Euclidean relative neighborhood graph," Pattern Recognition Lett., pp. 317–322, 1983.
- [16] D. W. Matula and R. R. Sokal, "Properties of Gabriel graphs relevant to geographical variation research and the clustering of points in the plane," Geographical Analysis, vol. 12, pp. 205–222, 1984.
18. an   d n , tin  1it neighborhood graphs in the lp metric," Computing, vol. 40, pp. 147–161, 1988.
- [20] K.'L. Clarkson, H. Edeísbrunner L. J. Guibas, M. Sharir, and E. Welzl. "Combinatorial complexity bounds for arrangements of curves and surfaces," Discrete and Computational Geometry, vol. 5, pp. 99–160, 1990.
- [19] J. W. Jaromczyk and M. Kowaluk, "Constructing the relative neighborhood graph in 3-dimensional Euclidean space, Discrete Applied Math., vol. 31, pp. 181–192, 1991.
- [21] F. R. K. Chung, "Sphere-and-point incidence relations in high uimots ns us   s ns uost neighbor pairs," Discrete and Computational Geometry, vol. 4, pp. 183–190, 1989.
- [23] P. Agarwal, H. Edelsbrunner, O. Schwarzkopf, and E. Welzl. "Euclidean minimum spanning trees and bichromatic closest pairs" in Proc. 6th ACM Symp. Computational Geometry, 1990, pp. 203–210.
- [22] P. K. Agarwal and J. Matoušek, "Relative neighborhood graphs in three dimensions," in Proc. 3rd Annual ÁCM-SIAM Symp. Discrete Algorithms, 1992, pp. 58–67; also in Computational Geometry: Theory and Applications, to be published.
- [24] H. Edelsbrunner and M. Sharir, "A hyperplane incidence problem with applications to counting distances," in Proc. Int. Symp. Algorithms, LNCS 450, 1990, pp. 419–428.
- [26] W. D. Smith, "Studies in computational geometry motivated by mesh generation," Ph.D. thesis, Princeton University, 1989.
- [25] J. W. Jaromczyk and M. Kowaluk, "A note on relative neighborhood graphs,"in Proc. 3rd Ann. Symp. Computational Geometry (Waterloo, Canada), June 8–10, 1987, pp. 233-241.
- [27] B. Chazelle et al., "Slimming down by adding; Selecting heavily covered points," in Proc. 6th Ann. Symp. Computational Geometry, 1990, pp. 116–127.
- [29] A. Getis and B. N. Boots, Models and Spatial Process. Cambridge, U.K.: Cambridge University Press, 1978.
- [28] L. Devróye, "The expected size of some graphs in computational geometry," Computers and Mathematics with Applications, vol. 15, pp. 53–64, 1988.
- [30] R. E. Miles, "On the homogenous planar poisson point process," Mathematical Bioscences, vol. 6, pp. 85–127, 1970.
- [32] J. Katajainen, "Bucketing and filtering in computational geometry," Ph.D. thesis, University of Turku, Finland, 1987. (Available as Report A46.)
- [31] B. M. Chazelle, "Filtering search: A new approach to query answering," SIAM J. Comput., vol. 15, pp. 703–724, 1986.
- [33] H. N. Gabow, J. L. Bentley, and R. E. Tarjan, "Scaling and related techniques for geometry problems," in Proc. 16th Ann. ACM Symp. Theory of Computing, 1984, pp. 135–143.


<!-- p:15 -->


- [34] A. C.-C. Yao, "On constructing minimum spanning trees in kdimensional spaces and related problems,"SIAM J. Comput., vol. 11, pp. 721–736, 1982.
- [36] D. É. Willard, "New data structures for orthogonal range queries," SIAM J. Comput., vol. 14, pp. 232–253, 1985.
- [35] G. T. Toussaint, B. K. Bhattacharya, and R. S. Poulsen, "The application of Voronoi diagrams to non-parametric decision rules," in Proc. Computer Science and Statistics: 16 Symp. Interface (Atlanta), Mar. 14–16 1984.
- [37] . Edeisbrunner and M. H. Overmars, "Batched dynamic solutions to decomposable searching problems," J. Algorithms, vol. 6, pp. 515–542, 1985.
- [39] Y. C. Wee, "On the angle restricted nearest neighbor problem," Tech. Rep. 89–8, Dept. Comp. Sci., University at Albany, 1989.
- [38] L. J. Guibas and J. Stolfi, "On computing all north-east nearest neighbors in the l1 metric," Inform. Process. Lett., vol. 17, pp. 219–223, 1983.
- [40] J. L. Bentley, B. W. Weide, and A. C. Yao, ""Optimal expected-time algorithms for closest point problems," ACM Trans. Math. Software, pp. 563–580, 1980.
- [42] J. Katajainen, O. Nevalainen, and J. Teuhola, "A linear expectedtime algorithm for computing planar relative neighborhood graphs," Inform. Process. Lett., vol. 25, pp. 77–86, 1987.
- [41] J. Katajainen and'O. Nevalainen, "Computing relative neighborhood graphs in the plane," Pattern Recognition, vol. 19, pp. 221–228, 1986.
- [43] G. T. Toussaint and R. Menard, "Fast algorithms for computing the planar relative neighborhood graph," in Proc. 5th Symp. Operations Research, 1980, pp. 425-428.
- [45] D. T. Lee, "Relative neighborhood graphs in the l1-metric," Pattern Recognition, vol. 18, pp. 327–332, 1985.
- [44] K. J. Supowit, "The relative neighborhood graph, with an application to minimum spanning trees," J. Assoc. Comput. Mach., vol. 30, pp. 428–448, 1983.
- [46] H. N. Gabow and R. E. Tarjan, "A linear-time algorithm for a special case of disjoint set union,"J. Computer and System Sciences, vol. 30, pp. 209–221, 1985.
- [61] K. L.Clarkson, H. Edelsbrunner, L. J. Guibas, M. Sharir, and E. Welzl, "Combinatorial complexity bounds for arrangements of curves and surfaces," in Proc. 29th Ann. Symp. Foundations of Computer Science, 1989, pp. 568–579.
- [63] M. S. Chang, C. Y. Tang, and R. C. T. Lee "20-relative neighborhood graphs are Hamiltonian," in Proc. Int. Symp. SIGAL '90, Aug. 1990, pp. 53–65.
- [62] T.-H. Su and R.-Ch. Chang, "Computing the k-relative neighborhood graphs in Euclidean plane," Pattern Recognition, vol. 24, pp. 231–239, 1991.
- [64] M. Chang, C. Tang, and R. Lee, "Solving the Euclidean bottleneck matching problem by k-relative neighborhood graph," Algorithmica, 1991.
- [66] G. T. Klinscek, "Minimal triangulations of polygonal domains,' Annals Discrete Math., pp. 121–123, 1980.
- [65] H. Edelsbrunner and T. S. Tan, "A quadratic time algorithm for the minmax length triangulation," Tech. Rep., Dept. of Comp. Sci., University of Illinois at Urbana Champaign, Feb. 1991.
20. J   - ,  -   - [e applications," in Proc. Int. Symp., SIGAL '90, Aug. 1990, pp. 66-75.
- [69] H. A. ElGindy and G. T. Toussaint, "Computing the relative neighborhood decomposition of a simple polygon," Computational Morphology, pp. 53–70, 1988.
- [68] T.-H. Su and R.-Ch. Chang, "Computing the constrained relative neighborhood graphs and constrained Gabriel graphs in Euclidean plane," Pattern Recognition, vol 24, pp. 221–230, 1991.
- [70] G. T. Toussaint, "Decomposing a simple polygon with the relative neighborhood graph," in Proc. Allerton Conf., Oct. 1980, pp. 20–28.
- [71] M. Ichino and J. Sklansky, "The relative neighborhood graph for mixed feature variables," Pattern Recognition, vol. 18, pp. 161–167, 1985.
- [72] R. H. Gutting, O. Nurmi, and T. Ottmann, "The direct dominance problem," in Proc. First Ann. ACM Symp. Computational Geometry, 1985, pp. 81–88.
- [48] N.-F. Hwang, "Divide and conquer algorithm for RNG," B/T, vol. 30, pp. 196–206, 1990.
- [47] R. E. Tarjan, Data Structures and Network Algorithms. Philadelphia, PA: SIAM, 1983.
- [49] R. Dwyer, "Average-case analysis of algorithms for convex hulls and Voronoi diagrams," Ph.D. thesis, Carnegie-Mellon University, 1988.
- [51] M. H. Overmars and E. Welzl, "New methods for computing visibility graphs," in Proc. Fourth Ann. Symp. Comp. Geometry, 1988, pp. 164–171.
30. putational Morphology, G. T. Toussaint, Ed. North-Holland, 1988, pp. 229–260. [73]  G. T. Toussaint, 'A graph-theoretical  primal sketch,' in Com-
- [75] J. D. Radke, "On the shape of a set of points," in Computational Morphology, G. T. Toussaint, Ed. North-Holland, 1988, pPp. 105–136.
- [74] H. Edelsbrunner, D. Kirkpatrick, and R. Seidel, "On the shape of a set of points in the plane," IEEE Trans. Inform. Theory, vol. 29, pp. 551–559, 1983.
- [76] D. Avis and J. Horton, "Remarks on the sphere of influence graph," in Discrete Geometry and Convexity, J. E. Goodman et al., Eds. New York Academy of Sciences, 1985, pp. 323–327.
- [50] A. Maus, "Delaunay triangulation and the convex hull of points in expected linear time," B/T, vol. 24, pp. 151–163, 1984.
- [52] A. Aggarwal, L. J. Guibas, J. Saxe, and P. W. Shor, "A linear time algorithm for computing the Voronoi diagram of a convex polygon," in Proc. 19th Ann. ACM Symp. Theory of Computing, 1987, pp. 39–45.
- [54] T.-H. Su and R.-Ch. Chang, "On constructing relative neighboronnn s e- unn  na n vol. 46, pp. 121–130, 1991.
37. ir Ii  i r-ir i , iin  [1thn rng and mst of unimodal polygons,"Inform. Process. Lett., vol. 31, pp. 243–248, 1989.
- [55] C. W. Dodge. Euclidean Geometry and Transformations. Reading, MA: Addison-Wesley, 1972.
- [57] F. Aurenhammer, "Improved algorithms for discs and balls using power diagrams," J. Algorithms, vol. 9, pp. 151–161, 1988.
- [56] H. Imai, M. Iri, and K. Murota, "Voronoi diagram in the Laguerre geometry and its applications," SIAM J. Čomput., vol. 14, pp. 93–105, 1985.
- [58] J. Katajainen and O. Nevalainen, "An almost naive algorithm for finding relative neighborhood graphs in lp metrics," Informatique Theoretique et Applications, vol. 21, pp. 199–215, 1987.
- [60] B. Chazelle, M. Sharir, and E. Welzl, "Quasi-optimal upper bounds for simplex range searching and new zone theorem," in Proc. 6th AĆM Symp. Computational Geometry, 1990, pp. 23-33.
- [59] R. B. Urquhart, "Algorithms for computation of relative neighborhood graph," Electron. Lett., vol. 14, no. 14, pp. 556–557, 1980.
- [78] J. I. Toriwaki and S. Yokoi, "Voronoi and related neighbors on digitized two dimensional space with application to texture analysis," in Computational Morphology, G. T. Toussaint, Ed. North-Holland, 1988, pp. 207–228.
- [77] R. C. Veltkamp. "The γ-neighborhood graph," Tech. Rep., Centre for Mathematics and Computer Science, July 1990.
46. i oi sti   id i, in  o sophical Trans. Royal Soc. London, vol. 275, no. 945, pp. 483–524, 1976.
- [81] G. T. Toussaint, "Pattern recognition and geometric complexity," in Proc. 5th Int. Conf. Pattern Recognition (Miami Beach), Dec. 1980, pp. 1324–1347.
- [80] J. M. Kennedy and C. Ware, "Illusory contours can arise in dot figures," Perception, pp. 191–194, 1978.
- [82] V. Medek, On the boundary of a finite set of points in the plane," Computer Graphics and Image Processing, vol. 15, pp. 93–99, 1981.
- [84] G. Matheron, Random Sets and Integral Geometry. New York: Wiley, 1975.
- [83] C. T. Zahn, "Graph-theoretical methods for detecting and describing gestalt clusters," IEEE Trans. Comput., vol. 20, pp. 68–86, 1971.
- [85] J. Serra, Image Analysis and Mathematical Morphology. New York: Academic Press, 1982.
- [87] J. Fairfield, "Čontoured shape generation: Forms that people see in dot patterns," in Proc. IEEE Conf. Cybernetics and Society,
- [86] G. T. Toussaint, "Computational geometry and morphology," in Proc. First Int. Symp. Science and Form (Tsukuba, Japan), Nov. 1985, pp. 395–403.


<!-- p:16 -->


1979, pp. 60–64.

- [89] W. W. Moss, "Some new analytic and graphic approaches to numerical taxonomy, with an example from dermanyssidae (acari)," Systematic Zoology, vol. 16, pp. 177–207, 1967.

I

- [113] M. Chang, C. Tang, and R. Lee, "Solving the Euclidean bottleneck biconnected edge subgraph problem by 2-relative neighborhood graph," Discrete and Applied Mathematics, vol. 39, pp. 1–12, 1992.
- [115] F. Pernus, "The Delaunay triangulation and the shape hull as tools in muscle fiber analysis," Pattern Recognition Lett., vol. 8, pp. 197–202, 1988.
- [114] B. Sendov, "Planar neighborhood graphs without cycles," Comptes rendus de l'Academie Bulgare des sciences, vol. 44, no. 4, pp. 23–25, 1991.
- [88] J. Fairfield, "Segmenting dot patterns by Voronoi diagram concavity," IEEÈ Trans. Pattern Anal. Machine Intell., pp. 104–110, 1983.
- [90] H. Edelsbrunner and E. P. Mücke, "Three-dimensional alpha shapes," manuscript, 1992.
- [92] H. Edelsbrunner, Ġ. Rote, and E. Weizl, "Testing the necklace condition for shortest tours and optimal factors in the plane,' Theoretical Computer Science, vol. 66, pp. 157–180, 1989.
- [91] B. Rosenberg andD. J. Langridge, "A computational view of perception," Perception, pp. 415–424, 1973.
- [93] E. R. Reinferberg, "A problem on circles," Math. Gaz., vol. 32, pp. 290–292, 1948.
- [95] J. Bentley and T. Ottman, "Algorithms for reporting and counting geometric intersections," IÉEE Trans. Comput., vol. 28, pp. 643–647, 1979.
10. qt ns a , m d a amad  m] a lemma of Besicovitch," Amer. Math. Monthly, vol. 58, pp. 306–314, 1951.
- [96] G. Rote, "Two solvable cases of the traveling salesman problem," Ph.D. thesis, Technische Universitat Graz, Austria, 1988.
- [98] M. S. Jacobson, M. J. Lipman, and F. R. McMorris, "Trees that are sphere-of-influence graphs," Tech. Rep., University of Louisville, 1989.
- [116] T. Saito, J.-I. Toriwaki, and S. Yokoi, "Properties of extended digital α-hull with applications to shape feature analysis of a figure set," Forma, vol. 6, pp. 9–25, 1991.

Jerzy W. Jaromczyk received the Ph.D. in compter science in 1984 from Warsaw University, Poland.

Currently he is an associate professor in the Department of Computer Science at the University of Kentucky in Lexington. His research interests include algorithm design and applications.

Dr. Jaromczyk is a member of the Association for Computing Machinery and the European Association for Theoretical Computer Science.

- [97] L Guibas, J. Pach, and M. Sharir, "Generalized sphere-ofinfluence graphs in higher dimensions," manuscript, Tel-Aviv University, 1992.
- [99] F. Harary, M. S. Jacobson, M. J. Lipman, and F. R. McMorris, "Sphere-of-influence graphs defined on prescribed graph," manuscript, University of Louisville, 1990.
3. -utss  a    a  ai  at ties with applications in computer vision," Ph.D. thesis, New Mexico State University, June 1991.
- [100] D. W. Dearholt, N. Gonzales, H. Kirpekar, "Associative network databases for computer vision," in Proc. 21st Asilomar Conf. Signals, Systems, and Computers, 1987, pp. 859–864.
- [102] D. W. Dearholt, N. Ġonzales, and G. Kurup, "Monotonic search networks for computer vision databases," in Proc. 22nd Asilomar Conf. Signals," Systems, and Computers, 1988, pp. 548–553.
- [104] L. P. Devroye, "On the inequality of Cover and Hart in nearest neighbor discrimination," IEEE Trans. Pattern Anal. Machine Intell., vol. 3, pp. 75–78, 1981.
- [103] T. M. Cover and P. E. Hart, "Nearest neighbor pattern classification," IEEE Trans. Inform. Theory, vol. 13, pp. 21–27, 1967.
- [105] P. M. Vaidya, "An O(n log n) algorithm for the all-nearestneighbors problem," Discrete and Computational Geometry, pp. 101–115, 1989.
- [107] D. T. Lee and F. P. Preparata, "Location of a point in a planar subdivision and its applications," SIAM J. Comput., pp.594–606, 1977.
10. I , y    ih      hm] for finding best matches in logarithmic expected time," ACM Trans. Math. Software, vol. 3, pp. 209–226, 1977.
- [108] D. T. Lee, "Rectangle proximity graphs and rectilinear shortest path problems," in Proc. First Workshop Proximity Graphs. Memoranda in Computer and Cognitive Science MCĆS-91–224, Computing Research Laboratory, New Mexico State University, Las Cruces, 1991, pp. 57-87.
- [110] L. P. Lefkovitch, "Further nonparametric tests for comparing dissimilarity matrices based on the relative neighborhood graph," Mathematical Biosciences, vol. 73, pp. 71–88, 1985.
- [109] L. P. Lefkovitch, "Species associations and conditional clustering; clustering with or without pairwise resemblances, in Developments in Numerical Ecology (NATO ASI Series, vol. G14), P. Legendre and L. Legendre, Eds. New York: SpringerVerlag, 1987, pp. 309–331.
14. dissimilarity matrices, a general measure of biogeographical distance, and their applications, Amer. Natur., vol. 123, pp. 484–499, 1984.
- [112] P. F. Ash and E. D. Bolker, "Recognizing Dirichlet tessellations," Geometria Dedicata, vol. 19, pp. 175–206, 1985.

Godfried T. Toussaint received the B.Sc. degree from the Univesity of Tulsa, Tulsa, OK, and the M.A.Sc. and Ph.D. degrees from the University of British Columbia, Vancouver, B.C., Canada, in 1968, 1970, and 1972, respectively, all in electrical engineering.

Since 1972 he has been with the School of Computer Science at McGill University, teaching and doing research in the areas of information theory, pattern recognition, and computational geometry. During the summers of 1975

and 1977 he was a Visiting Scholar at the Information Systems Laboratory, Stanford University. The sabbatical year 1980-81 he spent as a Visiting Scientist at the Applied Mathematics Research Center of the University of Montreal. During the spring of 1986 he was a Visiting Scholar at the Courant Institute of Mathematical Sciences, at New York University. During the fall of 1988 he was a British Columbia Advanced Systems Institute Fellow at Simon Fraser University. In the spring of 1989 he was a Visiting Professor in the Mathematics Department at the University of West Indies, Cave Hill, Barbados, and during the summer of 1989 he was a Visiting Scientist in the Department of Mathematics and Computer Science at the University of Amsterdam.

Dr. Toussaint is a former council member of the North American Branch of the Classification Society and a former associate editor of the IEEE TRANSACTIONS ON INFORMATION THEORY and of the IEEE TRANSACTIONS ON PATTERN ANALYSIS AND MACHINGE INTELLIGENCE. Presently he is an associate editor of the Plenum Press Series on Advanced Applications in Pattern Recognition and associate editor of the journals Pattern Recognition, Computational Geometry: Theory and Applications, The International Journal of Computational Geometry and Applications, and The Visual Computer. He is also on the editorial boards of the journals Discrete &amp; Computational Geometry and Forma and on the advisory board of the IEEE TRANSACTIONS ON PATTERN ANALYSIS AND MACHINE INTELLIGENCE. He is a member of several learned societies, including the Pattern Recognition Society and the New York Academy of Sciences. He is the editor of two books published by North Holland: Computational Geometry (1985) and Computational Morphology (1988), and he served as guest editor of a special issue of The Visual Computer on computational geometry (May 1988). In 1978 he was the recipient of the Pattern Recognition Society's Best Paper of the Year Award and in 1985 he was awarded a Killam Fellowship by the Canada Council to carry out a two-year research project on the movable separability of sets.

1
