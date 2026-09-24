---
id: "Aldous-Shun_2011_Connected-Spatial-Networks-Route-Length"
source_pdf: "../pdf/Aldous-Shun_2011_Connected-Spatial-Networks-Route-Length.pdf"
source_filename: "Aldous-Shun_2011_Connected-Spatial-Networks-Route-Length.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "full-page-ocr"
extraction_quality: "excellent"
extraction_score: 108.0
visual_assets: "disabled"
references_file: "../references/Aldous-Shun_2011_Connected-Spatial-Networks-Route-Length.references.md"
---

<!-- p:1 -->

## Connected Spatial Networks over Random Points and a Route-Length Statistic

David J. Aldous and Julian Shun

Abstract. We review mathematically tractable models for connected networks on random points in the plane, emphasizing the class of proximity graphs which deserves to be better known to applied probabilists and statisticians. We introduce and motivate a particular statistic R measuring shortness of routes in a network. We illustrate, via Monte Carlo in part, the trade-off between normalized network length and R in a one-parameter family of proximity graphs. How close this family comes to the optimal trade-off over all possible networks remains an intriguing open question.

The paper is a write-up of a talk developed by the first author during 2007-2009.

Key words and phrases: Proximity graph, random graph, spatial network, geometric graph.

## 1. INTRODUCTION

The topic called random networks or complex networks has attracted huge attention over the last 20 years. Much of this work focuses on examples such as social networks or WWW links, in which edges are not closely constrained by two-dimensional geometry. In contrast, in a spatial network not only are vertices and edges situated in two-dimensional space, but also it is actual distances, rather than number of edges, that are of interest. To be concrete, we visualize idealized inter-city road networks, and a feature of interest is the (minimum) route length

David J. Aldous is Professor, Department of Statistics, University of California, 367 Evans Hall # 3860, Berkeley, California 94720, USA (e-mail: aldous@stat.berkeley.edu; URL: www.stat.berkeley.edu/users/aldous). Julian Shun is Graduate Student, Machine Learning Department, Carnegie Mellon University, 5000 Forbes Avenue, Pittsburgh, Pennsylvania 15213, USA (e-mail: julianshun@gmail.com).

This is an electronic reprint of the original article published by the Institute of Mathematical Statistics in Statistical Science, 2010, Vol. 25, No. 3, 275–288. This reprint differs from the original in pagination and typographic detail.

between two given cities. Because we work only in two dimensions, the word spatial may be misleading, but equally the word planar would be misleading because we do not require networks to be planar graphs (if edges cross, then a junction is created).

Our major purpose is to draw the attention of readers from the applied probability and statistics communities to a particular class of spatial network models. Recall that the most studied network model, the random geometric graph [40] reviewed in Section 2.1, does not permit both connectivity and bounded normalized length in the n → ∞ limit. An attractive alternative is the class of proximity graphs, reviewed in Section 2.3, which in the deterministic case have been studied within computational geometry. These graphs are always connected. Proximity graphs on random points have been studied in only a few papers, but are potentially interesting for many puron t to, o ot oat te hs topic of this paper (see Section 6.5). One could also imagine constructions which depend on points having specifically the Poisson point process distribution, and one novel such network, which we name the Hammersley network, is described in Section 2.5.

Visualizing idealized road networks, it is natural to take total network length as the "cost" of a network, but what is the corresponding "benefit"? Primarily we are interested in having short route lengths. Choosing an appropriate statistic to meaFinally, recall this is a nontechnical account. Our sure the latter turns out to be rather subtle, and purpose is to elaborate verbally the ideas outlined the (only) technical innovation of this paper is the above; some technical aspects will be pursued elseintroduction (Section 3.2) and motivation of a spe- where. cific statistic R for measuring the effectiveness of a network in providing short routes.


<!-- p:2 -->


In the theory of spatial networks over random points, it is a challenge to quantify the trade-off between network length [precisely, the normalized length L defined at (2)] and route length efficiency statistics such as R. Our particular statistic R is not amenable to explicit calculation even in comparatively tractable models, but in Section 4 we present the results from Monte Carlo simulations. In particular, Figure 7 shows the trade-off for the particular β-skeleton family of proximity graphs.

Given a normalized network length L, for any realization of cities there is some network of normalized length L which minimizes R. As indicated in Section 5, by general abstract mathematical arguments, there must exist a deterministic function Ropt(L) giving (in the "number of cities → ∞" limit under the random model) the minimum value of R over all possible networks of normalized length L. An intriguing open question is as follows:

how close are the values Rβ-skel(L) from the β-skeleton proximity graphs to the optimum values Ropt(L)?

## 2. MODELS FOR CONNECTED SPATIAL NETWORKS

There are several conceptually different ways of defining networks on random points in the plane. To be concrete, we call the points cities; to be consistent about language, we regard xi as the position of city i and represent network edges as line segments (xi, xj).

First (Sections 2.1–2.3) are schemes which use deterministic rules to define edges for an arbitrary deterministic configuration of cities; then one just applies these rules to a random configuration. Second, one can have random rules for edges in a deterministic configuration (e.g., the probability of an edge between cities i and j is a function of Euclidean distance d(xi, xj), as in popular small worlds models [39]), and again apply to a random configuration. Third, and more subtly, one can have constructions that depend on the randomness model for city positions—Section 2.5 provides a novel example.

We work throughout with reference to Euclidean distance d(x, y) on the plane, even though many models could be defined with reference to other metro  b     on n hold, for the MST).

In Sections 2.1–2.3 we have an arbitrary configuration x = {xi} of city positions, and a deterministic rule for defining the edge-set E. Usually in graph theory one imagines a finite configuration, but note that everything makes sense for locally finite configurations too. Where helpful, we assume "general position," so that intercity distances d(xi, xj) are all distinct.

As discussed in Section 5.3, at first sight it looks easy to design heuristic algorithms for networks which should improve over the β-skeletons, for example, 2.1 The Geometric Graph by introducing Steiner points, but in practice we have not succeeded in doing so.

This paper focuses on the random model for city positions because it seems the natural setting for theoretical study. As a complement, in [10] we give empirical data for the values of (L, R) for certain real-world networks (on the 20 largest cities, in each of 10 US States). In [8] we give analytic results and bounds on the trade-off between L and the mathematically more tractable stretch statistic Rmax at (4), in both worst-case and random-case settings for city positions. Let us also point out a (perhaps) nonobvious insight discussed in Section 3.3: in designing networks to be efficient in the sense of providing short routes, the main difficulty is providing short routes between city-pairs at a specific distance (2–3 standardized units) apart, rather than between pairs at a large distance apart.

For the geometric graph one fixes 0 &lt; c &lt; ∞ and defines

$$( x _ { i } , x _ { j } ) \in \mathcal { E } \quad \text {if} \ \ d ( x _ { i } , x _ { j } ) \leq c .$$

For the K-neighbor graph one fixes K ≥ 1 and defines

(xi, xj) ∈ E iff xi is one of the K closest neighbors of xj, or xj is one of the K closest neighbors of xi.


<!-- p:3 -->


- A moment's thought shows these graphs are in gen- · Gabriel graph. There does not exist a city inside the disc whose diameter is the line segment from xi to xj.

eral not connected, so we turn to models which are "by construction" connected. We remark that the connectivity threshold cn in the finite n-vertex model · Delaunay triangulation [23]. There exists some of the random geometric graph has been studied in disc, with xi and xj on its boundary, so that no detail—see Chapter 13 of [40]. city is inside the disc.

### 2.2 A Nested Sequence of Connected Graphs

The material here and in the next section was developed in graph theory with a view toward algorithmic applications in computational geometry and pattern recognition. The 1992 survey [28] gives the history of the subject and 116 citations. But everything we need is immediate from the (careful choice of) definitions. On our arbitrary configuration x we can define four graphs whose edge-sets are nested as follows:

MST ⊆ relative n'hood ⊆ Gabriel ⊆ Delaunay.

(1)

Here are the definitions (for MST and Delaunay, it is easy to check these are equivalent to more familiar definitions). In each case, we write the criterion for an edge (xi, xj) to be present:

- Minimum spanning tree (MST) [24]. There does not exist a sequence i = k0, k1, . . . , km = j of cities such that

$$\max ( d ( x _ { k _ { 0 } } , x _ { k _ { 1 } } ) , d ( x _ { k _ { 1 } } , x _ { k _ { 2 } } ) , \dots , d ( x _ { k _ { m - 1 } } , x _ { k _ { m } } ) ) & \quad \overset { ( i i i ) } { \underset { \alpha i s } { \max } } , \\ < d ( x _ { i } , x _ { j } ) . & \quad \text {flectice}$$

The inclusions (1) are immediate from these definitions. Because the MST (for a finite configuration) is connected, all these graphs are connected.

Figure 1 illustrates the relative neighborhood and Gabriel graphs. Figures for the MST and the Delaunay triangulation can be found online at http://www. spss.com/research/wilkinson/Applets/edges.html.

Constructions such as the relative neighborhood and Gabriel graphs have become known loosely as proximity graphs in [28] and subsequent literature, and we next take the opportunity to turn an implicit definition in the literature into an explicit definition.

### 2.3 Proximity Graphs

Write v\_ and v+ for the points (−1, 0) and (1, 0). The lune is the intersection of the open discs of radii 1 centered at v\_ and v+. So v\_ and v+ are not in the lune but are on its boundary. Define a template A to be a subset of R2 such that:

- (i) A is a subset of the lune.
- (ii) A contains the open line segment (v\_, v+).
- (iii) A is invariant under the "reflection in the yaxis" map Reflectx(x1, x2) = (−x1, x2) and the "reflection in the x-axis" map Reflecty(x1, x2) = (x1,
- Relative neighborhood graph. There does not exist a city k such that

$$\max ( d ( x _ { i } , x _ { k } ) , d ( x _ { k } , x _ { j } ) ) < d ( x _ { i } , x _ { j } ) .$$

- (iv) A is open.

−x2).

For arbitrary points x, y in R2, define A(x, y) to be the image of A under the natural transformation (translation, rotation and scaling) that takes 2.5 The Hammersley Network (v−, v+) to (x, y).

FIG. 1. The relative neighborhood graph (left) and Gabriel graph (right) on different realizations of 500 random points.

<!-- p:4 -->


There is a quite separate recent literature in theDEFINITION. Given a template A and a locally oretical probability [26, 27] defining structures such finite set V of vertices, the associated proximity graph as trees and matchings directly on the infinite PoisG has edges defined by, for each x, y ∈ V, son point process. In this spirit, we observe that the (x, y) is an edge of G iff A(x, y) contains Hammersley process studied in [6] can be used to no vertex of V. define a new network on the infinite Poisson point From the definitions: process, which we name the Hammersley network. This network is designed to have the feature that · if A is the lune, then G is the relative neighboreach vertex has exactly 4 edges, in directions NE hood graph; (between North and East), NW, SE and SW. The · if A is the disc centered at the origin with radius conceptual difference from the networks in the previ1/2, then G is the Gabriel graph. ous section is that there is not such a simple "local" But the MST and Delaunay triangulation are not criterion for whether a potential edge (xi, xj) is in instances of proximity graphs. the network. And edges cross, creating junctions.

Note that replacing A by a subset A' can only For a picturesque description, imagine one-eyed introduce extra edges. It follows from (1) that the frogs sitting on an infinitely long, thin log, each beproximity graph is always connected. The Gabriel ing able to see only the part of the log to their left graph is planar. But if A is not a superset of the disc before the next frog. At random times and positions centered at the origin with radius 1/2, then G might (precisely, as a space-time Poisson point process of not be a subgraph of the Delaunay triangulation, rate 1) a fly lands on the log, at which instant the and in this case edges may cross, so G is not planar (unique) frog which can see it jumps left to the fly's (e.g., if the vertex-set is the four corners of a square, position and eats it. This defines a continuous time then the diagonals would be edges). Markov process (the Hammersley process) whose states are the configurations of positions of all the frogs. There is a stationary version of the process in which, at each time, the positions of the frogs form a Poisson (rate 1) point process on the line.

For a given configuration x, there is a collection of proximity graphs indexed by the template A, so by choosing a monotone one-parameter family of templates, one gets a monotone one-parameter family of graphs, analogous to the one-parameter family Gc of geometric graphs. Here is a popular choice [30] in which β = 1 gives the Gabriel graph and β = 2 gives the relative neighborhood graph.

DEFINITION (The β-skeleton family). (i) For 0 &lt; β &lt; 1 let Aβ be the intersection of the two open discs of radius (2β)−1 passing through v\_ and v+.

(ii) For 1 ≤ β ≤ 2 let Aβ be the intersection of Reinterpreting the time axis as a second space the two open discs of radius β/2 centered at (±(β − axis, and introducing compass directions, that part 1)/2,0). of the trajectory becomes a North edge followed by 2.4 Networks Based on Powers of Edge-Lengths a West edge. Now replace these two edges by a single North-West straight edge. Doing this procedure for It is not hard to think of other ways to define oneeach frog and each pair of successive jumps, we obparameter families of networks. Here is one scheme tain a collection of NW paths, that is, a network in used in, for example, [38]. Fix 1 ≤ p &lt; ∞. Given a which each city (the reinterpreted space-time ranconfiguration x, and a route (sequence of vertices) dom points) has an edge to the NW and an edge x0, x1, . . . , xk, say, the cost of the route is the sum of pth powers of the step lengths. Now say that a pair to the SE. Finally, we repeat the construction with (x, y) is an edge of the network Gp if the cheapest the same realization of the space-time Poisson point route from x to y is the one-step route. As p inprocess but with frogs jumping rightward instead of creases from 1 to ∞, these networks decrease from leftward. This yields a network on the infinite Poisthe complete graph to the MST. Moreover, for p ≥ 2 son point process, which we name the Hammersley the network Gp is a subgraph of the Gabriel graph. network. See Figure 3.

Now consider the space-time trajectories of all the frogs, drawn with time increasing upward on the page. See Figure 2. For each frog, the part of the trajectory between the completions of two successive jumps consists of an upward edge (the frog remains in place as time increases) followed by a leftward edge (the frog jumps left).


<!-- p:5 -->


REMARKs. (a) To draw the Hammersley network randomization has effect only near the boundary of the square.

on random points in a finite square, one needs external randomization to give the initial (time 0) frog positions, in fact, two independent randomizations for the leftward and the rightward processes. So to be pedantic, one gets a random network over the given realization of cities. However, one can deduce from the theoretical results in [6] that the external

5

4

3

2

t

-1

-3

0

3

4

x

FIG. 2. Space-time trajectories in Hammersley's process.

FIG. 3. The Hammersley network on 2500 random points.

- (b) The property that each vertex has exactly 4 edges, in directions NE (between North and East), NW, SE and SW, is immediate from the construction. Note, however, that while adjacent NW spacetime trajectories in Figure 2 do not cross, the corresponding diagonal roads in the Hammersley network may cross, so it is not a planar graph, though this has only negligible effect on route lengths.
- (c) Intuition, confirmed by Figure 7 later, says that the Hammersley network is not very efficient as a road network. It serves to demonstrate that there do exist random networks other than the familiar ones, and provides an instance where imposing deterministic constraints (the four edges, in this case) on a random network makes it much less efficient. How general a phenomenon is this?

### 2.6 Normalized Length

The notion of normalized network length L is most easily visualized in the setting of an infinite deterministic network which is "regular" in the sense of consisting of a repeated pattern. First choose the unit of length so that cities have an average density of one per unit area. Then define

- (2) L = average network length per unit area,
2. Δ = average degree (number of incident edges) (3) of cities.

Figure 4 shows the values of L and Δ for some simple "repeated pattern" networks. Though not directly relevant to our study of the random model, we find Figure 4 helpful for two reasons: as intuition for the interpretation of the different numerical values of L, and because we can make very loose analogies (Section 6.6) between particular networks on random points and particular deterministic networks.

## 3. NORMALIZED LENGTH AND ROUTE-LENGTH EFFICIENCY

### 3.1 The Random Model

For the remainder of the paper we work with "the random model" for city positions. The finite model assumes n random vertices (cities) distributed independently and uniformly in a square of area n. The infinite model assumes the Poisson point process of rate 1 (per unit area) in the plane. The quantities L, Δ above and R below that we discuss may be in- Euclidean distance between the cities. So l(i, j) ≥ d(i, j), and we write


<!-- p:6 -->


FIG. 4. Variant square, triangular and hexagonal lattices. Drawn so that the density of cities is the same in each diagram, and ordered by value of L.

L = 1.25

Δ = 2.5

L = 1.32 Δ = 3

L = 1.50

Δ = 3

Punctured lattice

L = 1.61 Δ = 3

L = 2.00 Δ = 4

L = 2.71

Δ = 5

Square lattice

L = 2.83 Δ = 4

L = 3.22 Δ = 6

L = 3.41

∆ = 6

Diagonal lattice

Triangular lattice

$$r ( i , j ) = \frac { \ell ( i , j ) } { d ( i , j ) } -$$

so that "r(i, j) = 0.2" means that route length is 20% longer than straight line distance. With n cities we get u such numbers r(i, j); what is a reasonable way to combine these into a single statistic? Two natural possibilities are as follows:

$$\begin{array} { c c c } t ^ { \prime } & \text {is} & R _ { \max } \colon = \max _ { j \neq i } r ( i , j ) , \\ \text {for} & & \\ \text {even} & ( 4 ) & \\ & \text {for} & R _ { a v e } \colon = a v e _ { ( i , j ) } \, r ( i , j ) , \end{array}$$

terpreted as exact values in the infinite model or as n → ∞ limits in the finite model; see Section 5. We use the word normalized as a reminder of the "density 1" convention—we choose the normalized unit of distance to make cities have average density 1 per unit area. After this normalization, L is the average network length per unit area.

### 3.2 The Route-Length Efficiency Statistic R

In designing a network, it is natural to regard total length as a "cost". The corresponding "benefit" is having short routes between cities. Write l(i, j) for the route length (length of shortest path) between cities i and j in a given network, and d(i,j) for where ave(i,j) denotes average over all distinct pairs (i,j). The statistic Rmax has been studied in the context of the design of geometric spanner networks [37] where it is called the stretch. However, being an "extremal" statistic Rmax seems unsatisfactory as a descriptor of real world networks—for instance, it seems unreasonable to characterize the UK rail network as inefficient simply because there is no very direct route between Oxford and Cambridge.


<!-- p:7 -->


FIG. 5. Efficient or inefficient? Rave would judge this network efficient in the n → ∞ limit.

品

The statistic Rave has a more subtle drawback. Consider a network consisting of:

- the minimum-length connected network (Steiner tree) on given cities;
- and a superimposed sparse collection of randomly oriented lines (a Poisson line process [45]).

See Figure 5. By choosing the density of lines to be sufficiently low, one can make the normalized network length be arbitrarily close to the minimum needed for connectivity. But it is easy to show (see [7] for careful analysis and a stronger result) that one can construct such networks so that Rave → 0 as n → ∞. Of course no one would build a road network looking like Figure 5 to link cities, because there are many pairs of nearby cities with only very indirect routes between them. The disadvantage of Rave as a descriptive statistic is that (for large n) most citypairs are far apart, so the fact that a given network has a small value of Rave says nothing about route lengths between nearby cities.

We propose a statistic R which is intermediate between Rave and Rmax. First consider (see discussion below for details)

$$\rho ( d ) \coloneqq & \text {mean value of } r ( i , j ) \text { over} \\ & \text {city-pairs with } d ( i , j ) = d$$

and then define

$$R \colon = \max _ { 0 \leq d < \infty } \rho ( d ) .$$

In words, R = 0.2 means that on every scale of distance, route lengths are on average at most 20% longer than straight line distance.

On an intuitive level, R provides a sensible and interpretable way to compare efficiency of different networks in providing short routes. On a technical level, we see two advantages and one disadvantage of using R instead of Rave:

Advantage 1. Using R to measure efficiency, there is a meaningful n → ∞ limit for the network length/ efficiency trade-off [the function Ropt(L) discussed in Section 5], and so, in particular, it makes sense to compare the values of R for networks with different n.

Advantage 2. A more realistic model for traffic would posit that volume of traffic between two cities varies as a power-law d−γ of distance d, so that in calculating Rave it would be more realistic to weight by d−γ. This means that the optimal network, when using Rave as optimality criterion, would depend on γ. Use of R finesses this issue; the value of γ does not affect R. A related issue is that volume of traffic between two cities should depend on their populations. Intuitively, incorporating random population sizes should make the optimal R smaller because the network designer can create shorter routes between larger cities. We see this effect in data [10]; R calculated via population-weighting is typically slightly smaller. But we have not tried theoretical study.

Disadvantage. The statistic R is tailored to the infinite model, in which it makes sense to consider two cities at exactly distance d apart (then the other city positions form a Poisson point process). For finite n we need to discretize. For the empirical data in [10], where n = 20, we average over intervals of width 1 unit (recall the unit of distance is taken such that the density of cities is 1 per unit area), that is, for d = 1, 2, . . . , 5, we calculate


<!-- p:8 -->


(d) := mean value of r(i, j) over city-pairs

$$( 6 ) & & \text {with } d - \frac { 1 } { 2 } < d ( i , j ) < d + \frac { 1 } { 2 } , \\ \tilde { R } & \colon = \max _ { 1 \leq d < \infty } \tilde { \rho } ( d )$$

n    r o Y  o   u u shorter intervals. Thus, there is, in principle, a certain fuzziness to the notion of R for finite networks, and, in particular, it is not clear how to assign a value of R to regular networks such as those in Figure 4. But in practice, for networks we have studied on real-world data and on random points, this is not a problem, as explained next.

### 3.3 Characteristic Shape of the Function ρ(d)

For the connected networks on random points (excluding the Hammersley network) we are discussing, the function ρ(d) has a characteristic shape (see Figure 6) attaining its maximum between 2 and 3 and slowly decreasing thereafter. We suspect that "this characteristic shape holds for any reasonable model," but we do not know how to turn that phrase into a precise conjecture. Note that "smoothness near the maximum" implies that any calculated value R at (6) is quite insensitive to the choice of discretization.

a value of 0.21 at d = 5. This arises from the particular structure (from each city there is one road in each quadrant) resembling the deterministic "diagonal lattice" of Figure 4, in which the route between some nearby pairs will be via two diagonal roads and a junction.

## 4. LENGTH-EFFICIENCY TRADE-OFF FOR TRACTABLE NETWORKS

Recall that our overall theme is the trade-off between network length and route-length efficiency, and that in this paper we focus on n → ∞ limits in the random model and the particular statistics L and R.

The models described in Section 2 are "tractable" in the specific sense that one can find exact analytic formulas for normalized length L. Unfortunately R is not amenable to analytic calculation, and we resort to Monte Carlo simulation to obtain values for R. Table 1 and Figure 7 show the values of (L, R) in the models. We explain below how the values of L are calculated.

Notes on Table 1. (a) Values of R from our simulations with n = 2500.

(b) Value of L for MST from Monte Carlo [19]. In principle, one can calculate arbitrarily close bounds [11], but apparently this has never been carried out. Of course, Δ = 2 for any tree.

| Network               |     L |  ̄ ∆    | R    |
|-----------------------|-------|--------|------|
| Minimum spanning tree | 0.633 | 2      | ∞    |
| Relative n'hood       |  1.02 | 2 . 56 | 0.38 |
| Gabriel               |     2 | 4      | 0.15 |
| Hammersley            |  3.25 | 4      | 0.35 |
| Delaunay              |  3.40 | 6      | 0.07 |

This characteristic shape has a common-sense interpretation. Any efficient network will tend to place (c) The Gabriel graph and the relative neighborroads directly between unusually close city-pairs, hood graph fit the assumptions of Lemma 1 with implying that ρ(d) should be small for d &lt; 1. For c = π/4 and c = 2π √3 respectively, and their ta3 4 large d the presence of multiple alternate routes ble entries for L and Δ are obtained from Lemma helps prevent ρ(d) from growing. At distance 2 − 3 1, as are the values for β-skeletons in Figure 7. from a typical city i there will be about π32 − π22 ≈ (d) For the Hammersley network, every degree 16 other cities j. For some of these j there will be equals 4, so L = 2 × (mean edge-length). It follows cities k near the straight line from i to j, so the from theory [6] that a typical edge, say, NE from network designer can create roads from i to k to j. (x, y), goes to a city at position (x +ξx, y + ξy), where The difficulty arises where there is no such intermediate city k: including a direct road (xi, xj) will TABLE 1 increase L, but not including it will increase ρ(d) for Statistics of tractable networks on random points 2 &lt; d &lt; 3.

Thus, Figure 6 offers a minor insight into spatial network design: that it is city pairs at normalized distance 2 - 3 specifically that enforce the constraints on efficient network design.

The characteristic shape—at least, the flatness over 2 ≤ d ≤ 5—is also visible in the real-world data [10].

For the Hammersley network, the graph of ρ(d) is quite different; ρ(d) increases to a maximum of 0.35 around d = 0.8 and then decreases more steeply to Notes: Integer values are exact. Recall L is normalized length (2), ∆ is average degree (3) and R is our route-length statistic (5).


<!-- p:9 -->


FIG. 6. The function ρ(d) for three theoretical networks on random cities. Irregularities are Monte Carlo random variation.

0.4

o


Relative n'hood

o

0.3

o

ρ(d)

o

0.2

o

Gabriel

o

0.1-

Delaunay

o


1

2

3

4

5

Normalized distance d

FIG. 7. The normalized network length L and the route-length efficiency statistic R for certain networks on random points. The o show the beta-skeleton family, with RN the relative neighborhood graph and G the Gabriel graph. The · are special models: △ shows the Delaunay triangulation, □ shows the network G2 from Section 2.4 and  shows the Hammersley network.

0.4

RN

o

0.3

O

R

o


0.2

o

OG

0.1

1

2

3

Normalized network length L

ξx and ξy are independent with Exponential(1) dis- the minimum-length triangulation. Our simulation tribution. So mean edge-length equals results in Figure 6 for ρ(d) for the Delaunay tri(7) ∞ ∞J √x2 + y2e−x−y dx dy ≈ 1.62. angulation are roughly consistent with a simulation result in [13] saying that ρ(65) ≈ 0.05.

(e) For any triangulation, Δ = 6 in the infinite 4.1 A Simple Calculation for Proximity Graphs model. For the Delaunay triangulation, L = ES where S is the perimeter length of a typical cell, and it is known ([35], page 113) that ES = 32 . Note [33] Let us give an example of an elementary calcula3π that the Delaunay triangulation is in general not tion for proximity graphs over random points.


<!-- p:10 -->


LEMMA 1. For a proximity graph with template A on the Poisson point process,

$$L = \frac { \pi ^ { 3 / 2 } } { 4 c ^ { 3 / 2 } } ,$$

$$\bar { \Delta } = \frac { \pi } { c } ,$$

where c = area(A).

PRoOF. Take a typical city at position x0. For a city x at distance s the chance that (x0,x) is an edge equals exp(−cs2) and so

$$\text {edge equals} \exp ( - c s ) & \text { and } s 0 \\ \text {mean-degree} & = \int _ { 0 } ^ { \infty } \exp ( - c s ^ { 2 } ) 2 \pi s \, d s , \\ L & = \frac { 1 } { 2 } \int _ { 0 } ^ { \infty } s \exp ( - c s ^ { 2 } ) 2 \pi s \, d s .$$

$$L = \frac { 1 } { 2 } \int _ { 0 } ^ { \infty } s \exp ( - c s ^ { 2 } ) 2 \pi s \, d s .$$

Evaluating the integrals gives (8) and (9). □

One can derive similar integral formulas for other "local" characteristics, for example, mean density of triangles and moments of vertex degree. See [18, 20, 21, 34] for a variety of such generalizations and specializations.

### 4.2 Other Tractable Networks

We do not know any other ways of defining networks on random points which are both "natural" and are tractable in the sense that one can find exact analytic formulas for L. In particular, we know no tractable way of defining networks with deliberate junctions as in Figure 8. Note also that, while it is easy to make ad hoc modifications to the geometric graph to ensure connectivity, these destroy tractability. On the other hand, one can construct "unnatural" networks (see, e.g., [8]) designed to permit calculation of L.

## 5. OPTIMAL NETWORKS AND N → ∞ LIMITS

### 5.1 Tractable Models

As mentioned earlier, the quantities L, ∆, R we discuss may be interpreted as exact values in the infinite model or as n → ∞ limits in the finite model. To elaborate briefly, in a realization of the finite model (n cities distributed independently and uniformly in a square of area n), a network in Table 1 has a normalized length Ln = n−1 × (network length) and an average degree ∆n which are random variables, but there is convergence (in probability and in expectation)

$$( 1 0 ) \quad L _ { n } \rightarrow L , \quad \bar { \Delta } _ { n } \rightarrow \bar { \Delta } \quad \text {as } n \rightarrow \infty$$

FIG. 8. An ad hoc modification of the relative neighborhood graph, introducing junctions.

to limit constants definable in terms of the analogous network on the infinite model (rate 1 Poisson point process on the infinite plane). For the proximity graphs or Delaunay triangulation, the network definition applies directly to the infinite model and proof of (10) is straightforward. For the Hammersley network, (10) is implicit in [6], and for the MST detailed arguments can be found in [9, 43].

### 5.2 Optimal Networks

We now turn to consideration of optimal networks. Given a configuration x of n cities in the area-n square, and a value of L which is greater than n−1 × (length of Steiner tree), one can define a number

$$\begin{array} { r l } & { \text {the ge-} } \\ & { d o r y } & { R _ { n } ( x , L ) = \min \, o f \, \tilde { R } \, o r \, a l l \, n t w i r k s } \\ & { \text {construct} } & { ( 1 1 ) } \\ & { t o p e r - } & { o n \, x \, w i t h \, n o r m a l i z e d \, l e g h t \leq L , } \end{array}$$

where Ř is the discretized version (6) calculated using intervals of some suitable length δn. Applying this to a random configuration X in the finite model gives, for each L, a random variable

$$\Xi _ { n } ( L ) \colon = R _ { n } ( X , L ) .$$

One intuitively expects convergence to some deterministic limit

$$\inf _ { \substack { \text {unit} - \\ \text {d unit-} } } \quad ( 1 2 ) \quad \Xi _ { n } ( L ) \to R _ { \text {oppt} } ( L ) \quad \text {say, as } n \to \infty .$$

The analogous result for Rmax will be proved carefully in [8], and the same "superadditivity" argument could be used to prove (12). See [43, 44, 47] for general background to such results. The point is that we do not have any explicit description of the optimal [i.e., attaining the minimum in (11)] networks in the finite or infinite models, so it seems very chal- between distant cities to be roughly proportional to lenging to prove the natural stronger supposition graph distance (number of edges), which is a more that the finite optimal networks themselves converge relevant quantity in some contexts. However, when oe en ec e  o c -oe ce nnn  one uns e o cn timal network for which the value R = Ropt(L) is or partially replacing route length by graph distance attained. leads to quite different optimal networks [1, 22]. For some other cost/benefit functionals leading to yet 5.3 The Curve Ropt(L) different optimal networks see [2, 14].


<!-- p:11 -->


Every possible network on the infinite Poisson point process defines a pair (L, R), and the curve R = Ropt (L) can be defied equivalently as the lower boundary of the set of possible values of (L, R). There is no reason to believe that proximity graphs are exactly optimal, and, indeed, Figure 7 shows that the Delaunay triangulation is slightly more efficient than the corresponding β-skeleton. But our attempts to do better by ad hoc constructions (e.g., by introducing degree-3 junctions—see Figure 8 for an example) have been unsuccessful. And, indeed, the fact that the two special models in Figure 7 lie close to the β-skeleton curve lends credence to the idea that this curve is almost optimal. We therefore speculate that the function Ropt looks something like the curve in Figure 9, which we now discuss.

### 6.2 Rigorous Proof of Finite R in Random Proximity Graphs

Table 1 presented the Monte Carlo numerical value ≈0.38 of R for the relative neighborhood graph on random points. From a rigorous viewpoint, the assertion that a random network has R &lt; ∞ is essentially the assertion that ρ(d) = O(d) as d → ∞. This is often nontrivial to prove. A general sufficient condition for this property, which applies to the relative neighborhood graph (and hence all proximity graphs), is proved in [3]. The related fact that the limit limd→∞ρ(d)/d exists is proved in [4].

### 6.3 Real-World Trade-Off Between Network Length and Route-Length Efficiency

hdt  st t ¿(ot ot   t t Recall that our central theme is seeking to quannonincreasing. It is known [47] that there exists a tify the trade-off between normalized network length l Euclidean Steiner tree constant LsT representing the and route-length efficiency R. Figure 9 suggests that limit normalized Steiner tree length in the random for optimal networks the "law of diminishing remodel, and clearly Ropt(L) = ∞ for L &lt; LST. The turns" sets in around L = 2 (for comparison, this is facts the value of L corresponding to the square grid network), in that Ropt(L) decreases rapidly to around Ropt (L) &lt; ∞ for all L &gt; LST; 0.13 as L increases to 2 but decreases only slowly (13) as L increases further. This suggests a kind of "ecoRopt (L) → 0 as L → ∞ nomic prediction" for the lengths of real-world netare not trivial to prove rigorously, but follow from works which are perceived by users to be efficient in

the corresponding facts for Rmax proved in [8]. But providing short routes: we are unable to prove rigorously that Ropt(L) is strictly decreasing or that it is continuous.

## 6. FINAL REMARKS

### 6.1 Toy Models for Road Networks

the length of an efficient network linking n cities in a region of area A will be roughly 2√An.

Here the √An arises from undoing the normalization and the "2" is the value of L. Of course, this is

The idea of using proximity graphs as toy models rough: we mean "closer to 2 than to 1 or 3." for road networks has previously been noted [30] but 6.4 Other Results for the Random Network not investigated very thoroughly. It is an intuitively Models natural idea to a network designer: whether or not to place a direct road from city i to a nearby city j depends (partly) on whether some other city k is (MST, proximity graphs, Delaunay triangulation) in close to the line between them.

There is substantial literature on the networks the deterministic setting. In the random case, cenAs observed by a referee, for the kind of models tral limit theorems for total network length have studied in this paper we expect route length l(i, j) been studied in many models: for the MST in [29, 31,


<!-- p:12 -->


FIG. 9. Speculative shape for the curve Ropt(L), with o and · values from tractable networks in Figure 7.

0.4

0.3

o

R

o

0.2

o●

0.1

o

LST

1

2

3

Normalized network length L

32], and for the Delaunay triangulation, Voronoi tes- being natural models for road networks, proximity sellation, relative neighborhood and Gabriel graphs graphs might be useful in modeling communication in [12, 25, 42]. Large deviation estimates for tonetworks suffering line of sight interference. tal network length are given for the Gabriel graph At a more mathematical level, for questions such in [46], Section 11.4, and presumably could be exas spread-out percolation [41] or critical value of tended to other models. Otherwise the literature for contact processes [15], random proximity graphs with the random case is rather diffuse, with different fosmall A are an interesting alternative to the usual cuses for different networks. For instance, work on lattice- or random graph-based models. For instance, MSTs has focused on connections with critical continuum percolation [17]. For the relative neighborfor edge percolation on a random proximity graph hood graph and the Gabriel graph, [20] calculates ∆ with template A satisfies and [18] shows that, in the finite model, in a certain range the β-skeletons have

(14) Rmax grows as order √log n/log log n

degree in the Gabriel graph. As for the Delaunay triangulation, there has been surprisingly little followup to the seminal analysis by Miles [35] (various maximal statistics are studied in [16]), though the closely related Voronoi tessellation has been studied in more detail [36].

### 6.5 Speculative Applications of Random Proximity Graphs

Random proximity graphs seem an interesting object of study from many viewpoints, in particular, as an attractive alternative to random geometric graphs for modeling spatial networks that are connected by design. It is remarkable that results such as (14) are the only nonelementary results about them that we can find in the literature. As well as

(15) pA ∼π−1 area(A) as area(A) → 0

[the right side = 1/∆ from (9)] and that the critifor the contact process has the same asymptotics.

### 6.6 Analogies Between Deterministic and Random Networks

As mentioned earlier, we may make very loose analogies between particular networks on random points and particular deterministic networks in Figt       ait  li  t latter three cases:

Relative n'hood graph ↔ punctured lattice,

Gabriel graph ↔ square lattice,

Hammersley network ↔ diagonal lattice,

Delaunay triangulation ↔ triangular lattice.


<!-- p:13 -->


### 6.7 Scale Invariant Continuum Networks

Introducing the statistic R can be viewed as one [6] ALDOUS, D. J. and DIACONIS, P. (1995). Hammersley's approach to resolving the "paradox" from [7], disinteracting particle process and longest increasing cussed in Section 3.2, that the more natural statissubsequences. Probab. Theory Related Fields 103 tic Rave does not lead to realistic optimal networks 199–213. MR1355056 in the n → ∞ limit. This particular approach was [7] ALDOUS, D. J. and KENDALL, W. S. (2008). Shortlength routes in low-cost networks via Poisson prompted by visualizing real-world road networks— line patterns. Adv. in Appl. Probab. 40 1–21. cf. discussion in Section 3.3. Let us mention a matheMR2411811 matically more sophisticated alternative, under study [8] ALDous, D. J., BHAmIDI, S. and LANDo, T. (2010). as a work in progress [5]. Instead of a discrete PoisThe stretch-length tradeoff in geometric networks: son process of cities, we imagine a continuum limit. Worst-case and average-case study. To appear. That is, for each finite set (z1, . . . , zk) of points in the [9] ALDOUS, D. J. and STEELE, J. M. (1992). Asymptotics for Euclidean minimal spanning trees on random plane, there is a random network S(z1, . . . , zk) linkpoints. Probab. Theory Related Fields 92 247–258. ing the points, consistent as more points are added. MR1161188 Mathematically natural structural properties for the distribution of such a process are as follows:

- (i) translation and rotation invariance,
- (ii) scale invariance,

where the latter means that routes, as point-sets in R2, are invariant in distribution under Euclidean -caes (pp  t ts  t .itial ogous to (5), assumed finite, is a constant, which we can call R'. The analog L' of L is defined by

the expected length of the network on n uniform random points in the area-n square grows ∼ L'n as n → ∞.

In this setting we can study the optimal trade-off between L' and R', and the kind of "paradoxical" Figure 5 network cannot arise because it violates scale-invariance.

## ACKNOWLEDGMENTS

- [5] ALDoUs, D. J. (2010). Scale-invariant random spatial networks. To appear.
- [10] ALDOUS, D. J. and CHOI, A. (2009). A route-length efficiency statistic for road networks. Unpublished manuscript. Available at www.stat.berkeley.edu/ ~aldous/Spatial/paper.pdf.
- [11] AVRAM, F. and BERTSIMAS, D. (1992). The minimum spanning tree constant in geometric probability and under the independent model: A unified approach. Ann. Appl. Probab. 2 113–130. MR1143395
- [12] AVRAM, F. and BERTSIMAS, D. (1993). On central limit theorems in geometrical probability. Ann. Appl. Probab. 3 1033–1046. MR1241033
- [13] BACCELLI, F., TCHOUMATCHENKO, K. and ZUYEV, S. (2000). Markov paths on the Poisson-Delaunay graph with applications to routeing in mobile networks. Adv. in Appl. Probab. 32 1–18. MR1765174
- [14] BARTHÉLEMY, M. and FLAMMINI, A. (2006). Optimal traffic networks. J. Stat. Mech. Theory Exp. 2006 L07002.
- [15] BERGER, N., BORGS, C., CHAYES, J. T. and SABERI, A. (2005). On the spread of viruses on the internet. In Proceedings of the Sixteenth Annual ACM-SIAM Symposium on Discrete Algorithms 301–310 (electronic). ACM, New York. MR2298278
- [16] BERN, M., EPPSTEIN, D. and YAO, F. (1991). The expected extremes in a Delaunay triangulation. Internat. J. Comput. Geom. Appl. 1 79–91. MR1099499
- [17] BEZUIDENHOUT, C., GRIMMETT, G. and LÖFFLER, A. (1998). Percolation and minimal spanning trees. J. Stat. Phys. 92 1–34. MR1645627
- [18] BOSE, P., DEVROYE, L., EVANS, W. and KIRKPATRICK, D. (2006). On the spanning ratio of Gabriel graphs and β-skeletons. SIAM J. Discrete Math. 20 412427 (electronic). MR2257270
- [19] CORTINA-BORJA, M. and ROBINSON, T. (2000). Estimating the asymptotic constants of the total length of Euclidean minimal spanning trees with powerweighted edges. Statist. Probab. Lett. 47 125–128. MR1747099

Aldous's research supported by NSF Grant DMS0704159. We thank three anonymous referees for helpful comments.
