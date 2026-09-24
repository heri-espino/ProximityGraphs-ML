---
id: "Watanabe_2008_Proximity-Graphs-Transportation-Networks"
source_pdf: "../pdf/Watanabe_2008_Proximity-Graphs-Transportation-Networks.pdf"
source_filename: "Watanabe_2008_Proximity-Graphs-Transportation-Networks.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "excellent"
extraction_score: 108.0
visual_assets: "disabled"
references_file: "../references/Watanabe_2008_Proximity-Graphs-Transportation-Networks.references.md"
---

<!-- p:1 -->

## Evaluating the Configuration and the Travel Efficiency on Proximity Graphs as Transportation Networks

Daisuke Watanabe

Faculty of Marine Technology, Tokyo University of Marine Science and Technology, 2-1-6, Etchujima, Koto-ku, Tokyo 135-8533, Japan E-mail address: daisuke@kaiyodai.ac.jp

(Received May 31, 2008; Accepted October 27, 2008)

In this paper, we treat proximity graphs as theoretical road networks and evaluate the configuration and the travel efficiency on proximity graphs. We analyze the configuration of proximity graphs in terms of the length of graph edge and the efficiecy of travel on the graphs to compare with the property of ideal road network pattern. In conclusion, network distance on the relative neighborhood graph which is a kind of proximity graph is similar to rectilinear distance in terms of edge length and travel distance, but is different in terms of ratio to Euclidean distance.

Key words: Transportation Network, Proximity Graph, Computational Geometry, Geometric Probability

## 1. Introduction

Transportation networks consist of several kind of transportation systems like road, railway, liner, airline and so on. Especially, road network makes a skeleton of city or region and there is no same pattern in the world. There is a few grid pattern as theoretical road networks in urban planning. Network consists of line data which is made with nodes and edges, and the efficiency of network depends on the configuration of network.

Okabe et al. (2000) introduces the theory of computational geometry to construct geometric graphs. The geometric graphs defined on the basis of proximity relations are called 'proximity graphs'. The proximity graphs have many applications in engineering, particularly to morphological problems, and are recently developed in the field of computational morphology like spatial and cluster analysis, computer vision, pattern recognition and computational perception. When it is given a set of points on the plane, it is desired to find some structure among the points in the form of edges connecting a subset of the pairs of points. Watanabe (2005) analyzes the road network pattern of major cities in Japan using proximity graphs and find that the edges of the relative neighborhood graph include most of the grid road.

In this paper, we treat proximity graphs as the ideal road networks and evaluate the configuration and the travel efficiency on proximity graphs. In the next section, we define the notations and introduce the proximity graphs and some graphs related to them. In Sec. 3, we analyze the configuration of proximity graphs in terms of the length of graph edge. It hasn't been reported that the estimation of edge length of all proximity graphs, so we estimate the length and number of edges using the theory of the geometric probability. In Sec. 4, we analyze the efficiecy of travel on the graphs to compare with some routing system of ideal road network pattern.

## 2. Mathematical Preliminaries

In graph theory, a graph is a set of objects called points, nodes, or vertices connected by links called lines or edges.

A geometric graph G = ( P , E ) consists of the set of points given by P = { p 1 , . . . pn } and the set of edges given by E = { e 1 , . . . em } . Let S be area of arbitrary region, d ( pi , pj ) be Euclidean distance between pi and pj . The total number of points is | P | = n and the total number of edges is | E | = m . The density of points is ρ = n / S .

The proximity Graphs are developed by several academic field and contain following graphs.

We call generally connected geometric graph as PG and denote it by G PG = ( P , E PG ) . We call directed graph if the two directions are counted as being distinct edge, and not undirected graph . A subgraph of G is denoted by G ′ = ( P ′ , E ′ ) if and only if G ′ satisfies following conditions: P ⊆ P ′ and E ⊆ E ′ .

Reciprocal Pairs (RP) is obtained by joining two points pi , pj of P with an edge if and only if pi is the nearest to pj and vice versa. The edge is originally direct graph, but we treat it as undirected graph and denote it G RP = ( P , E RP ) .

Nearest Neighborhood Graph (NNG) is obtained by joining two points pi , pj of P with an edge if and only if pi is the nearest to pj . The edge is originally direct graph, but we treat it as undirected graph and denote it G NNG = ( P , E NNG ) .

Relative Neighborhood Graph (RNG) is obtained by joining two points pi , pj of P with an edge if and only if lune does not contain any other points of P in its interior. The lune is defined as the intersection of the two discs centered at pi and pj . We denote it G RNG = ( P , E RNG ) .

Delaunay Triangle (DT) is obtained by joining tree points of P with an edge if and only if triangle does not

Gabriel Graph (GG) is obtained by joining two points pi , pj of P with an edge if and only if the circle with the diameter pi , pj does not contain any other points of P in its interior. We denote it G GG = ( P , E GG ) .


<!-- p:2 -->

GG

DT

Fig. 1. Proximity graphs on same random points.

contain any other points of P in its interior. We denote it G DT = ( P , E DT ) . DT is dual graph of Voronoi diagram.

$$\mu _ { \text {rp} } & = \frac { 1 } { 2 } \sqrt { \frac { \pi } { \rho ( 4 \pi / 3 + \sqrt { 3 } / 2 ) } } \simeq \frac { 0 . 3 9 4 1 7 8 } { \sqrt { \rho } } , \\ \sigma _ { \text {rp} } ^ { 2 } & = \frac { 4 - \pi } { 4 \rho ( 4 \pi / 3 + \sqrt { 3 } / 2 ) } . \\ \text {The result of NNG is obtained by Clark and Evans (1954)}$$

The result of NNG is obtained by Clark and Evans (1954) as follows:

$$f _ { N G } ( l ) = 2 \rho \pi l e ^ { - \rho \pi l ^ { 2 } } ,$$

Minimum Spanning Tree (MST) is not proximity graph because MST needs to be global optimum, but related with proximity graphs. MST is defined as the tree which the sum of the Euclidean length of all the edges attains the minimum over all trees. The number of edges is m MST = n - 1 because there is no circuit. We denote it G MST = ( P , E MST ) .

$$\mu _ { N G } = \frac { 1 } { 2 \sqrt { \rho } } = \frac { 0 . 5 } { \sqrt { \rho } } , \ \sigma _ { N G } ^ { 2 } = \frac { 4 - \pi } { 4 \rho \pi } .$$

The result of GG is obtained by Møller (1994) as follows:

$$f _ { G G } ( l ) = \frac { 1 } { 2 } \rho \pi l e ^ { - \frac { 1 } { 4 } \rho \pi l ^ { 2 } } ,$$

$$\mu _ { G G } = \frac { 1 } { \sqrt { \rho } } , \ \sigma _ { G G } ^ { 2 } = \frac { 4 - \pi } { \pi \rho } .$$

The result of DT is obtained by Collins (1968) and Miles (1970) as follows:

$$f _ { D T } ( l ) = \frac { \pi \rho l } { 3 } \left \{ \sqrt { \rho } l e ^ { - \frac { 1 } { 4 } \pi \rho l ^ { 2 } } + E r f c \left ( \frac { 1 } { 2 } \sqrt { \pi \rho } l \right ) \right \} ,$$

$$\mu _ { \mathrm D T } = \frac { 3 2 } { 9 \pi \sqrt { \rho } } , \ \sigma _ { \mathrm D T } ^ { 2 } = \frac { 5 } { \pi \rho } - \frac { 1 0 2 4 } { 8 1 \pi ^ { 2 } \rho }$$

where Erfc is the complementary error function.

### 3.2 Estimation of the length of graph edges of RNG and MST

The result of RNG is not obtained and we derive using geomeric probability. At first, we derive the nearest neighbor distance with restricted search region. It has been established that the probability of finding exactly x points in an arbitrary area is given by the Poisson probability law. Let

$$( 4 )$$

Complete Graph (CG) is obtained by joining two points pi , pj of P with an edge if each pair of points has an edge connecting them, and denote it by G CG = ( P , E CG ) . The number of edges is m CG = n ( n - 1 )/ 2 because there are pairs of all nodes.

Each proximity graph and its related graphs have following relation: E RP ⊆ E NNG ⊆ E MST ⊆ E RNG ⊆ E GG ⊆ E DT ⊆ E CG. Figure 1 shows these proximity graphs constructed with random 100 points.

## 3. Evaluation of Graph Configuration

### 3.1 The length of graph edges with random points in previous works

It has been reported that the estimation of edge length of RP, NNG, GG and DT, but that of RNG and MST are unknown. We estimate those approximately using geometric probability.

We assume a random pattern with theoretical density of points ρ per unit area. Poisson probability law are used to obtain the probability density function of distance from an arbitrary locus to the nearest points. The random variable is denoted by l and a particular value of this distance variable is indicated by L . Let the probability density function of l be f ( l ) , the expectation be μ and the variance be σ 2 .

The result of RP is obtained by Pickard (1982) as follows:

$$f _ { \text {RP} } ( l ) = 2 \left ( \frac { 4 } { 3 } \pi + \frac { \sqrt { 3 } } { 2 } \right ) \rho l e ^ { - \left ( \frac { 4 } { 3 } \pi + \frac { \sqrt { 3 } } { 2 } \right ) \rho l ^ { 2 } } , \quad ( 1 ) \quad \text {bor disk} , \quad \text {lihed}$$


<!-- p:3 -->


Fig. 2. Search region for RNG.

the arbitrary region with area A , and assume region contains an average of ρ points per unit area. The probability that this region contains exactly x points is

$$\Pr ( x , A ) = \frac { ( \rho A ) ^ { x } } { x ! } e ^ { - \rho A } .$$

The probability of finding no points in a region with area A is obtained from Eq. (5) by putting x = 0. That probability is

$$\Pr ( 0 , A ) = e ^ { - \rho A } . \\$$

The region must contain at least one point on condition that the distance to the nearest point in the region L is less than l . So, the probability that the distance of two points is less than l is equal to the probability of finding at least one point in the region. That probabiltiy is

$$F ( l ) & = 1 - \Pr ( 0 , A ) . \\ \\$$

F ( l ) is accumulation of probabilistic density function, so f ( l ) is obtained by differentiation with respect to l as follows:

$$f ( l ) & = - \frac { d \Pr ( 0 , A ) } { d l } \\ & = - \frac { d } { d l } e ^ { - \rho A } . & ( 8 ) \quad \text {tim} u \\ \intertext { f o r } \intertext { b y i n j o i n g t w i t h e r s }$$

RNG is obtained by joining two points pi , pj of P with an edge if and only if lune does not contain any other points of P in its interior. As this lune is the gray region of RNG in Fig. 2, the area of this lune is ( 2 π/ 3 - √ 3 / 2 ) l 2 . We replace ( 2 π/ 3 - √ 3 / 2 ) by ω which doesn't contain the terms of l . So, we substitute ω l 2 for A and Eq. (8) is

$$f ( l ) & = - \frac { \text {d} } { d l } e ^ { - \rho \omega l ^ { 2 } } \\ & = 2 \rho \omega l e ^ { - \rho \omega l ^ { 2 } } . \\ \text {known to be} & \quad \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \$$

Laplacian is known to be

$$\int _ { 0 } ^ { \infty } x ^ { b - 1 } e ^ { - a x ^ { c } } d x & = \frac { \Gamma ( b / c ) } { c a ^ { b / c } } , & \text { (10) } & \text { is } A \\ \text { expectation of distance of two points is } & \text { } & \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \$$

and the expectation of distance of two points is

$$\text {expectation of distance of two points is} & & \text {RNG} \\ \mu = \int _ { 0 } ^ { \infty } l f ( l ) d l & & \text {and (} \\ = 2 \rho \omega \int _ { 0 } ^ { \infty } l ^ { 2 } e ^ { - \rho \omega l ^ { 2 } } d l & & \text {and (} \\ = 2 \rho \omega \frac { \Gamma ( 3 / 2 ) } { 2 ( \rho \omega ) ^ { 3 / 2 } } & & \\ = \frac { 1 } { 2 } \sqrt { \frac { \pi } { \rho \omega } } . & & ( 1 1 )$$

Fig. 3. Search region for MST.

The variance is

$$\text {since is} \\ \sigma ^ { 2 } & = \int _ { 0 } ^ { \infty } ( l - \mu ) ^ { 2 } f ( l ) d l \\ & = \int _ { 0 } ^ { \infty } l ^ { 2 } f ( l ) d l - \mu ^ { 2 } \\ & = \frac { 1 } { \rho \omega } - \frac { \pi } { 4 \rho \omega } \\ & = \frac { 4 - \pi } { 4 \rho \omega } . \\$$

After substituting ω by ( 2 π/ 3 - √ 3 / 2 ) in Eqs. (9), (11) and (12), we obtain f ( l ) , μ and σ as follows:

$$( 1 2 ) , \, & \text {we obtain } f ( l ) , \, \mu \text { and } \sigma \text { as follows:} \\ & f _ { \text {rng} } ( l ) = 2 \left ( \frac { 2 } { 3 } \pi - \frac { \sqrt { 3 } } { 2 } \right ) \rho \text {e} ^ { - \left ( \frac { 2 } { 3 } \pi - \frac { \sqrt { 3 } } { 2 } \right ) \rho l ^ { 2 } } , \quad ( 1 3 ) \\ & \mu _ { \text {rng} } = \frac { 1 } { 2 } \sqrt { \frac { \pi } { \rho ( 2 \pi / 3 - \sqrt { 3 } / 2 ) } } \, \frac { 0 . 7 9 9 6 1 4 } { \sqrt { \rho } } , \\ & \sigma _ { \text {rng} } ^ { 2 } = \frac { 4 - \pi } { 4 ( 2 \pi / 3 - \sqrt { 3 } / 2 ) \rho } . \\ & \text {The estimation of length of MST which needs global op-}$$

The estimation of length of MST which needs global optimum is more difficult than that of proximity graphs that can be constructed only with local information. Therefore, wemust think an approximated method using nearest neighbor distance. The construction principle of MST is approximated as the set of unisolated edges because MST is a tree which doesn't have isolated edge. We can think that MST is approximately obtained by joining two points pi , pj of P with an edge if and only if crescent does not contain any other points of P in its interior. This crescent is defined as the conplements of the two discs centered at pi and pk which is assumed as connected point of MST. We can connect pi and pj even if pi is the closest point from pi because we limit the search region within this crescent. As this crescent is the gray region in Fig. 3, the area of this crescent is A = (π/ 3 + √ 3 / 2 ) l 2 . We replace (π/ 3 + √ 3 / 2 ) by ω which doesn't contain the terms of l as same manner of RNG. After substituting ω by (π/ 3 + √ 3 / 2 ) in Eq. (9), (11) and (12), we obtain f ( l ) , μ and σ as follows:

$$and ( 1 2 ) , & \text { we obtain } f ( l ) , \mu \text { and or as follows:} \\ & f _ { \text {mst} } ( l ) = 2 \left ( \frac { \pi } { 3 } + \frac { \sqrt { 3 } } { 2 } \right ) \rho l e ^ { - \left ( \frac { \pi } { 3 } + \frac { \sqrt { 3 } } { 2 } \right ) \rho l ^ { 2 } } , \\ & \mu _ { \text {mst} } = \frac { 1 } { 2 } \sqrt { \frac { \pi } { \rho ( \pi / 3 + \sqrt { 3 } / 2 ) } } \simeq \frac { 0 . 6 4 0 7 1 1 } { \sqrt { \rho } } , \\ & \sigma _ { \text {mst} } ^ { 2 } = \frac { 4 - \pi } { 4 ( \pi / 3 + \sqrt { 3 } / 2 ) \rho } .$$


<!-- p:4 -->


Fig. 4. PDF of edge length of proximity graphs.

Fig. 5. Proximity graphs with regular points.

We compare the expectation of length with estimations in former researches. As lower bound, Furuyama (2003) estimated μ L MST = 0 . 64 / √ ρ from the component percentages of nearest neighbor links using numerical result. As upper bound, Robert (1968) estimated μ U MST = 0 . 707 / √ ρ . The expectation of length μ MST which is derived by this crescent is very close to the lower bound derived by Furuyama and our approximation using the nearest neighbor distance with the restricted search region within crescent is similar to the lower bound of MST.

Figure 4 shows the probabilistic density functions with ρ =1. As the search region become smaller from RP to DT, the length of edges become longer because the number of connectable points increase. As the distribution of edge length shifts to the right from RP to DT, the expectation and the variance also become larger. Especially, the functions of RNGandMSTwhich are derived in this section lie between that of NNG and GG.

### 3.3 Comparison with the length of graph edges with regular points

Figure 5 shows the proximity graphs with regular points of triangular lattice, square lattice and hexagonal lattice. If the node is degenerated, we include the edges. As you can see, RNG can construct typical grid road network on each lattice.

In the region which contain n points in area S , we can easily calculate the total number and length of edges if we don't consider the condition of the boundary. Table 1 shows the total number of edges, and Table 2 shows the total length of edges By deviding total length of edges by total number of edges, we get the average length of edge. From the result of random point in previous section, Table 3 shows the result of the average length of graph edges in both regular point and random point. Figure 6 shows the numerical result of Table 3 with ρ = 1. On random point, the average length of edge gets longer from RP to DT, and is less than that of regular lattice except DT. On triangle lattice and square lattice, the average length of edges hardly changes from RP to DT. On hexagonal lattice, the average length of edges hardly changes from RP to RNG, but get longer from GG to DT.

Table 1. Total number of graph edges of regular lattice.

|     | Triangle   | Square   | Hexagon   |
|-----|------------|----------|-----------|
| RP  | 1 2 n      | 1 2 n    | 1 2 n     |
| NNG | n          | n        | n         |
| MST | n - 1      | n - 1    | n - 1     |
| RNG | 3 n        | 2 n      | 3 2 n     |
| GG  |            | 3 n      | 2 n       |
| DT  |            |          | 3 n       |

Fig. 6. Average length of graph edges.

## 4. Evaluation of Travel Efficiency on Graphs 4.1 Model description

In this section, we analyze the efficiecy of travel on the graphs to compare with some routing system of ideal road network pattern. Most of transportation model treat discrete network or continuous plane. On continuous plane, there are several kind of theoretical distance like Euclidean distance and rectilinear distance. We call the set of edges network when the edges have attribution like distance.

We assume a random pattern with theoretical density of points ρ per unit area. There are n demand points in rectangular region whose side is a and area is S = a 2 . The trip demand uniformly and independently distributed between two points and the total of trips is n ( n - 1 ) .

Types of distance are Euclidean distance u , rectilinear distance r and network distance d , and 'the travel distance' and 'the ratio to Euclidean distance' are compared.

The distance of two point between pi = ( xi , yi ) and pj = ( x j , yj ) of Euclidean distance u and rectilinear distance r are respectively defined as follows:


<!-- p:5 -->


Table 2. Total length of graph edges of regular lattice.

|     | Triangle                | Square          | Hexagon                   |
|-----|-------------------------|-----------------|---------------------------|
| RP  | 1 2 1 √ 2 √ 3 √ nS      | 1 2 √ nS        | 1 √ 3 √ 3 √ nS            |
| NNG | √ 2 √ 3 √ nS            | √ nS            | 2 √ 3 √ 3 √ nS            |
| MST | ( n - 1 ) √ 2 √ 3 √ S n | ( n - 1 ) √ S n | ( n - 1 ) 2 √ 3 √ 3 √ S n |
| RNG | 3 √ 2 √ 3 √ nS          | 2 √ nS          | √ 3 √ 3 √ nS              |
| GG  |                         | (2+ √ 2 ) √ nS  | 5 √ 3 √ 3 √ nS            |
| DT  |                         |                 | 5 + 2 √ 3 √ 3 √ 3 √ nS    |

Table 3. Average length of graph edges.

|     | Triangle            | Square          | Hexagon                 | Random                         |
|-----|---------------------|-----------------|-------------------------|--------------------------------|
| RP  | √ 2 √ 3 √ S n √ S n | 2 √ 3 √ 3 √ S n |                         | 1 2 √ π 4 π/ 3 + √ 3 / 2 √ S n |
| NNG | √ 2 √ 3 √ S n √ S n | 2 √ 3 √ 3 √ S n |                         | 1 2 √ S n                      |
| MST | √ 2 √ 3 √ S n √ S n | 2 √ 3 √ 3 √ S n |                         | 1 2 √ π π/ 3 + √ 3 / 2 √ S n   |
| RNG | √ 2 √ 3 √ S n √ S n | 2 √ 3 √ 3 √ S n |                         | 1 2 √ π 2 π/ 3 - √ 3 / 2 √ S n |
| GG  | √ 2 √ 3 √ S n √ S n | 2 + √ 2 3 √ S n | 5 2 √ 3 √ 3 √ S n       | √ S n                          |
| DT  | √ 2 √ 3 √ S n √ S n | 2 + √ 2 3 √ S n | 5 + 2 √ 3 3 √ 3 √ 3 S n | 32 9 π S n                     |

$$u \stackrel { d e f } { = } & \sqrt { ( x _ { i } - x _ { j } ) ^ { 2 } + ( y _ { i } - y _ { j } ) ^ { 2 } } , \\ r \stackrel { d e f } { = } & \left | x _ { i } - x _ { j } \right | + \left | y _ { i } - y _ { j } \right | .$$

$$r \stackrel { d e f } { = } | x _ { i } - x _ { j } | + | y _ { i } - y _ { j } | .$$

Network distance is the distance on the shortest path using the Dijkstra's algorithm. Each trip travel on undirected graph G = ( P , E ) which is proximity graph and we treat RNG, GG and DT for network because they are connected graph.

### 4.2 Comparison with travel distance

Distance distribution is the probabilistic density function f ( l ) of distance l . The probabilistic density function fU ( u ) of Euclidean distance u is derived by Ghosh (1951) in rectangular region as follows:

$$\text {angular region as follows} & & \frac { 1 } { \sqrt { 2 } } \text { } \frac { \text {Network} } { \sqrt { 2 } } \text { } \frac { 1 } { \sqrt { 2 } } \text { } \frac { \text {Network} } { \sqrt { 2 } a } \text { } \frac { 1 } { 2 a ^ { 2 } } \text { } \frac { 2 u } { a ^ { 2 } } + u ^ { 2 } ) , & & ( 0 \leq u \leq a ) \\ & = \begin{cases} \frac { 2 u } { a ^ { 4 } } \left \{ 2 a ^ { 2 } \left ( \arcsin \frac { a } { u } - \arccos \frac { a } { u } \right ) & & \text {The pointer} \end{cases} & & \text {tance} \, r \text { } \text {in} \\ & + 4 a \sqrt { u ^ { 2 } - a ^ { 2 } } - ( u ^ { 2 } + 2 a ^ { 2 } ) \right \} , \, ( a < u \leq \sqrt { 2 } a ) & & \text {as follow} \\ & ( 1 7 ) & & f _ { R } ( r )$$

and the expectation of Euclidean distance is

$$\mu _ { U } & = \left \{ \frac { 1 } { 1 5 } ( 2 + \sqrt { 2 } ) + \frac { 1 } { 3 } \log ( 1 + \sqrt { 2 } ) \right \} a \\ & \simeq 0 . 5 2 1 a .$$

√


Table 4. Average distance.

|                         |   Average distance |
|-------------------------|--------------------|
| Euclidean distance      |              0.521 |
| Rectilinear distance    |              0.667 |
| Network distance on RNG |              0.668 |
| Network distance on GG  |              0.583 |
| Network distance on DT  |              0.551 |

Table 5. The ratio of each distance to Euclidean distance.

|                         |   Maximum |   Average |    RF |
|-------------------------|-----------|-----------|-------|
| Rectilinear distance    |     1.414 |     1.274 | 1.279 |
| Network distance on RNG |     4.143 |     1.293 | 1.280 |
| Network distance on GG  |     1.987 |     1.121 | 1.116 |
| Network distance on DT  |     1.402 |     1.058 | 1.056 |

The probabilistic density function fR ( r ) of rectiliner distance r is derived by Fairthorne (1963) in rectangular region as follows:

$$\leq \sqrt { 2 } a ) \\ ( 1 7 ) & & f _ { R } ( r ) = \begin{cases} \frac { 2 r } { a ^ { 4 } } \left ( \frac { r ^ { 2 } } { 3 } - 2 a r + 2 a ^ { 2 } \right ) , & ( 0 \leq r \leq a ) \\ \frac { 2 } { 3 a ^ { 4 } } ( 2 a - r ) ^ { 3 } , & ( a < r \leq 2 a ) \end{cases} \\ \text {and the expectation of rectilinear distance is}$$

$$\mu _ { R } & = \frac { 2 } { 3 } a \\ & \simeq 0 . 6 6 7 a .$$


<!-- p:6 -->


Fig. 7. Distance distribution on RNG.

Fig. 8. Distance distribution on GG.

Fig. 9. Distance distribution on DT.

We test ten numerical patterns of n = 1000 and a = 10 6 , and compare those numerical results with theoretical results. Table 4 shows the result of average distance. Distance distribution of RNG, GG and DT is respectively shown in Figs. 7, 8 and 9. The sign of reverse-triangle on axis indicate average distance  ̄ d in each figure. Solid lines indicate distance distributions of Euclidean distance and rectilinear distance, and vertical lines on axis indicate average of them. Average distance μ U of Euclidean distance is shorter than μ R of rectiliear distance.

From Fig. 7, form of distribution of RNG is close to that of rectilinear distance. From Table 4, average of RNG is also close to that of rectilinear distance.

From Fig. 8, form of distribution of GG is intermediate of that of Euclidean distance and rectilinear distance. From Table 4, average of GG is also intermediate of that of Euclidean distance and rectilinear distance.

From Fig. 9, form of distribution of DT is close to that of Euclidean distance. From Table 4, average of DT is also close to that of Euclidean distance.

h

k

Fig. 10. Ratio distribution of RNG.

k

Fig. 11. Ratio distribution of GG.

h

k

Fig. 12. Ratio distribution of DT.

### 4.3 Comparison with the ratio to Euclidean distance

The ratio of rectilinar distance r to Euclidean distance u is denoted by h , and is defined as follows:

$$& \quad h = \frac { r } { u } \\ & \quad \text {is} \quad = \frac { | x _ { i } - x _ { j } | + | y _ { i } - y _ { j } | } { \sqrt { ( x _ { i } - x _ { j } ) ^ { 2 } + ( y _ { i } - y _ { j } ) ^ { 2 } } } \quad ( 1 \leq r \leq \sqrt { 2 } ) . \ ( 1 9 ) \\ & \quad \text {the probability density function } \ f _ { H } ( h ) \ \text {is derived by}$$

The probabilistic density function fH ( h ) is derived by Tanaka et al. (2007) in rectangular region as follows:

$$f _ { H } ( h ) = \frac { 8 ( h + 3 \sqrt { 2 - h ^ { 2 } } ) } { 3 ( h + \sqrt { 2 - h ^ { 2 } } ) ^ { 3 } \sqrt { 2 - h ^ { 2 } } }$$


<!-- p:7 -->


and the expectation of ratio is

$$\text {and the expectation of ratio is} \\ \mu _ { H } & = \int _ { 1 } ^ { \sqrt { 2 } } h f _ { H } ( h ) d h \\ & = \frac { 1 } { 3 } \left \{ 5 \log ( 1 + \sqrt { 2 } ) + \sqrt { 2 } ( 1 - \sqrt { 2 } ) \right \} \\ & \simeq 1 . 2 7 4 . \\ \text {The ratio of network distance } d _ { i j } & \text { to Euclidean distance}$$

The ratio of network distance dij to Euclidean distance uij between point i and j is denoted by k , and is defined as follows:

$$\sum _ { k = \frac { i = 1 } { n ( n - 1 ) / 2 } } ^ { n } \sum _ { \substack { i = 1 + 1 \\ n ( n - 1 ) / 2 } } ^ { n } \frac { d _ { i j } } { u _ { i j } } . \quad \text {where} \quad \begin{matrix} \text {graph} \\ \text {pattern} \\ \text {and} \end{matrix}$$

Route Factor (RF) is defined as the ratio of Average distance of network distance to Average distance of Euclidean distance by Vaughan (1987), and is derived as follows:

$$\text {distance by Vauhgan (1987/), and is derived as follows:} \\ \quad R F _ { R } = \frac { \mu _ { R } } { \mu _ { U } } \\ = \frac { \frac { 2 } { 3 } a } { \left \{ \frac { 1 } { 1 5 } ( 2 + \sqrt { 2 } ) + \frac { 1 } { 3 } \log ( 1 + \sqrt { 2 } ) \right \} a } \\ \simeq 1 . 2 7 9 . \\ R F _ { R } \text { is different from } \mu _ { H } , \text { but result is numerically similar}$$

RF R is different from μ H , but result is numerically similar. RF of network distance on graph is

$$R F _ { D } = \frac { \sum _ { i = 1 } ^ { n } \sum _ { j = i + 1 } ^ { n } d _ { i j } } { \sum _ { i = 1 } ^ { n } \sum _ { j = i + 1 } ^ { n } u _ { i j } } . \quad \text { (22) } \quad \begin{matrix} \text {Firth} \\ \text {Ghosh} \end{matrix} \\ \text {shows the result of ratio to Euclidean distance} \quad \text { (22) } \quad \begin{matrix} \text {Ghosh} \end{matrix} \quad \text {rec} \quad \begin{matrix} \text {Fir} \\ \text {Miles} \end{matrix}$$

Table 5 shows the result of ratio to Euclidean distance of rectilinear distance and network distance of RNG, GG and DT. Average ratio is quite similar to RF of rectilinear distance and network distance on proximity graphs. In both average ratio and RF, rectiliear distance is quite similar to network distance on RNG. We can conclude that RNG have same character with grid road network from view of travel efficiency. In maximum of ratio, Euclidean distance is intermediate of network distance on GG and DT.

Ratio distribution of RNG, GG and DT is respectively shown in Figs. 10, 11 and 12. In each figure, sign of reverse-triangle on axis indicate average distance  ̄ h . Solid line indicate ratio distributions of rectilinear distance, and vertical line on axis indicate average of that.

The curve of rectilinear distance diverges at h = √ 2 and is not similar to that of proximity graphs. From the view of ratio to Euclidean distance, rectilinear distance and network distance on RNG have different character. The reason of this diffence seems to be related with the difference between the continuous plane and the discrete network.

## 5. Conclusion

In this paper, we treat these proximity graphs as the ideal road networks and evaluate the configuration of road networks and efficiency on them using proximity graphs. We analyze the configuration of proximity graphs in terms of the length of graph edge and the efficiecy of travel on the graphs to compare with the property of ideal road network pattern.

We estimate the length and the number of edges of RNG and MST using the theory of the geometric probability. The length of edge of RNG and MST lie between that of NNG and GG. The average length of edge on random points is less than that on regular lattice.

The network distance on RNG which is a kind of proximity graph is similar to rectilinear distance in terms of edge length and travel distance, but is different in terms of ratio to Euclidean distance.
