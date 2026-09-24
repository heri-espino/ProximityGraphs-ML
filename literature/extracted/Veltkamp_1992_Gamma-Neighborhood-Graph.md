---
id: "Veltkamp_1992_Gamma-Neighborhood-Graph"
source_pdf: "../pdf/Veltkamp_1992_Gamma-Neighborhood-Graph.pdf"
source_filename: "Veltkamp_1992_Gamma-Neighborhood-Graph.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "excellent"
extraction_score: 108.0
visual_assets: "disabled"
references_file: "../references/Veltkamp_1992_Gamma-Neighborhood-Graph.references.md"
---

<!-- p:1 -->

## The γ-neighborhood graph

####### Remco C. Veltkamp 米

Centre for Mathematics and Computer Science (CWI), Department of Interactive Systems, Kruislaan 413, 1098 SJ Amsterdam, Netherlands

Communicated by Selim Akl Submitted 8 November 1990 Accepted 1 November 1991

####### Abstract

Veltkamp, R.C., The γ-neighborhood graph, Computational Geometry: Theory and Applications 1 (1992) 227-246.

This paper presents a novel two-parameter geometric graph, the γ-neighborhood graph. This graph unifies a number of geometric graphs such as the convex hull, the Delaunay triangulation, and in 2D also the Gabriel graph and the circle-based β-skeleton, into a continuous spectrum of geometric graphs that ranges from the void to the complete graph. The two parameters provide for a great flexibility in the analysis of a set of sites. For specific ranges of the parameters, the corresponding graph can be efficiently constructed.

Keywords. Computational geometry; neighborhood graph; Delaunay triangulation; Hamilton cycle.

## 1. Introduction

In the computational geometry discipline, old and new geometric techniques are brought together and unified. An example of this is the development in geometric graphs. A major unifying effect in computational geometry was brought about by the Delaunay triangulation [3-4], and its dual Voronoi diagram [23]. Old geometric graphs such as the convex hull and the Euclidean minimum spanning tree, and new, parameterized graphs such as the α-shape [7] and the β-skeleton [9] are intimately related to the Delaunay triangulation. An even more general graph is presented in this paper: the γ-neighborhood graph. It is a two-parameter graph, unifying the Delaunay triangulation, convex hull and the β-skeleton into a continuous spectrum of geometric graphs ranging from the void to the complete graph.

Correspondence to: R.C. Veltkamp, Centre for Mathematics and Computer Science (CWI), Department of Interactive Systems, Kruislaan 413, 1098 SD Amsterdam, Netherlands.

* This research was done while the author was working at Leiden University, Netherlands.


<!-- p:2 -->


In [9] it is said that a geometric graph describes the internal shape of a set of sites, when it connects essential neighbors among the essential sites. The external shape is described when the graph connects essential neighbors among the essential extreme sites. In which way sites or pairs of sites are essential is determined by the definition of the graph or, when appropriate, the neighborhood. It will be shown that the γ-neighborhood graph can describe the internal, as well as the external shape.

Before the γ-neighborhood graph is introduced in Section 3, the next section gives an introductory overview of geometric graphs and some relations between them. Section 4 gives some examples of the γ-neighborhood graph for specific choices of the parameters. Section 5 deals with the computation of the γ-neighborhood graph, and the resulting computational complexities. Section 6 finally, shortly explains how the graph is used in computational morphology, specifically in finding an external shape of a set of sites.

## 2. Overview of geometric graphs

Some of the graphs mentioned in this section are truly proximity or neighborhood graphs. Such graphs join two sites by an edge when a certain neighborhood is empty. The neighborhood is called empty if no sites lie in its interior, except when an entire half-space is involved: a half-space with its boundary through x1, . . . , xk, is called empty if no sites lie in the open half-space; sites may lie on the boundary of the half-space except inside or on the (k – 1)D polygon through x1, ... , xk. For example in 2D, a half-plane through x, and x2 is empty if the open half-plane is empty, and no sites lie on the line segment between x, and x2 (but sites may lie on the boundary of the half-plane outside that segment). A sphere of infinite radius is also considered a half-space.

In the following, all distances are Euclidean distances, k denotes the dimension of the embedding space, S denotes the set of sites, and N the number of sites.

### 2.1. Defnitions

Closest pairs (CP). The closest pairs of a set of sites are the pairs of sites that have the smallest distance to each other, among all pairs. Note that there can be more than one closest pair. CP is disconnected, except for N = 2, or when all sites are equidistant.

Nearest neighbors graph (NNG). In the nearest neighbor graph, each site is connected to the site that is nearest. Since all the pairs of sites that are each others nearest neighbor contain the pairs with the smallest distance of all, CP ⊆ NNG. In general NNG is disconnected.


<!-- p:3 -->


Euclidean minimum spanning tree (EMST). This graph is connected and has no cycles. EMST is spanning in the sense that it connects all sites, and minimum with respect to the sum of all Euclidean distances between connected sites. In EMST, each site is connected to its nearest neighbor, and thus NNG ⊆ EMST. NNG actually is a minimum spanning forest, so in the special case that it is connected, it coincides with EMST.

Infinite strip graph (∞-SG). Two sites x and y are connected if and only if the infinite strip bounded by two parallel planes through x and y, that are perpendicular to x - y, is empty. The EMST must also connect such a pair of sites in order to be connected, except when two strips coincide for different pairs of sites. So in nondegenerate cases ∞-SG ⊆ EMST.

Sphere of influence graph (SIG). The SIG is introduced by Toussaint [20]. For each site x, let rx be the distance to the closest site. The sphere of influence graph connects two sites x and y, if and only if the spheres with radii rx and ry, and centered at x and y respectively, intersect in more than one point. Clearly, each site is connected to its nearest neighbor, so that NNG ⊆ SIG.

Relative neighborhood graph (RNG). Two sites x and x; are defined to be relatively close if

$$d ( x _ { i } , x _ { j } ) \leq \max \{ d ( x _ { i } , x _ { l } ) , d ( x _ { j } , x _ { l } ) \} , \ \text { for all } l \neq i , j .$$

For arbitrary x1, d(xi, xj) ≤max{d(xi, x1), d(xj, x1)}, if x1 does not lie in the interior of the intersection of the two spheres centered at x, and x, and with radius d(x,, xj). The intersection is called the relative neighborhood, and two sites are relative neighbors, if their relative neighborhood is empty. The RNG connects all relative neighbors. In the original definition by [10], the ≤'is replaced by a &lt;', ] onnn eon  eonon eoo saon oo e o tno and corresponds to the notion of 'empty neighborhood'. It is shown in [19] that EMST⊆RNG.

Gabriel graph (GG). The Gabriel neighborhood (named after [8]) of two sites x and y is the smallest sphere through x and y, which has radius d(x, y)/2. Because the Gabriel neighborhood is contained in the relative neighborhood, it is empty when the latter is empty, and therefore RNG ⊆ GG.

Convex hull (CH). The convex hull of a set of sites is the smallest polytope containing all the sites. Indeed this polytope is convex. The CH connects k sites with each other if a half-space with its boundary through these sites is empty in the sense stated at the beginning of this section. As a result, if k + 1 sites on the CH lie in a plane, the faces are kept (k – 1)-simplicial (a simplex or k-simplex is the k-dimensional analogue of the triangle in the plane and the tetrahedron in 3D, having k + 1 vertices).


<!-- p:4 -->


Delaunay triangulation (DT). In [23], a partitioning of space into simplices L is defined, which is therefore called an L-subdivision or L-partition. A definition of the L-subdivision given by Delaunay [3-4], defines a simplex to be part of the L-subdivision if the sphere through its vertices, which are some sites from S, contains no other sites. The L-subdivision is therefore called Delaunay triangulation, or sometimes closest point Delaunay triangulation. In three-dimensional space, we can call this a Delaunay tetrahedralization, although in general k-space this subdivision is still called a triangulation.

In the case that more than k + 1 sites lie on a sphere, connecting all these sites with each other would generate overlapping simplices. Instead, the DT arbitrarily connects sites to generate non-overlapping simplices that fill the space enclosed by the convex hull of these sites. A degenerate Delaunay triangulation is therefore not unique.

Clearly, an empty sphere passes through the end-points of each edge in a Delaunay triangulation. Conversely, if an empty sphere passes through two sites, then there is a largest possible empty sphere through these two sites. This sphere either passes through k - 1 other sites, or through k – 2 other sites and has an infinite radius. In the latter case, the 'sphere' is a half-space, and the two end-points lie on the convex hull. In both cases the two sites form an edge in the Delaunay triangulation. It follows immediately that CH ⊆ DT and GG ⊆ DT.

Because the sphere through the vertices of a simplex in the DT is empty, the ela , sa    ls   ss   slsk ay neighborhood'.

α-Shape. The notion of a parameterized generalized disc is introduced in [7]. A generalized disc of radius 1/α is defined as a disc of radius 1/α if α&gt;0, the complement of a disc of radius 1/(− α) if α &lt; 0, and a half-space if α = 0. For an arbitrary real α and a set S of sites in the plane, the α-hull of S is defined as the intersection of all closed generalized discs of radius 1/α that contain all the sites of S. Replacing circular arcs on the boundary of the α-hull by straight edges gives the α-shape. This definition is easily generalized to higher dimensions, replacing discs by spheres, and straight edges by flat triangles. The α-shape is a subgraph of the closest point Delaunay triangulation, if α ≥ 0, and a subgraph of the so-called furthest point Delaunay triangulation if α ≤0. The 0-shape coincides with the convex hull.

β-Skeleton. The β-skeleton is a planar parameterized graph, introduced in a lune-based and a circle-based variant [9]. The following definition is a slightly modified version of the original, in order to normalize the parameter to lie :    s  o - -e o  e  ee

(1) the intersection of two circles of radius d(x, y)/2(1 + β) that pass through x and y, if β ∈[−1,0],


<!-- p:5 -->


- (2) the intersection of two circles of radius d(x, y)/2(1 - β) centered at the points x + (y − x)β/2 and y + (x − y)β/2, if β ∈ [0, 1].

The circle-based β-neighborhood for two sites x and y is:

- (1) the intersection of two circles of radius d(x, y)/2(1 + β) that pass through x and y, if β ∈ [−1, 0].
- (2) the union of two circles of radius d/(x, y)/2(1 − β), that pass through x and y, if β ∈ [0, 1].

The β-skeleton connects those sites whose β-neighborhood is empty. When β = 0, both the lune-based and the circle-based neighborhood coincide with the Gabriel neighborhood. Both β-neighborhoods contain the Gabriel neighborhood when β &lt;0, so that the corresponding skeletons are contained in the GG. When β = 1/2 the lune-based β-neighborhood reduces to the relative neighborhood. When β = 1, the lune-based skeleton reduces to x-SG, and the circle-based skeleton to the void graph. For β = -1, both skeletons reduce to the complete graph if no three sites are collinear. The spectrum of β-neighborhoods for the whole range of the parameter is illustrated in Fig. 1. The generalization of the lune-based β-neighborhood to higher dimensions is straightforward. Nothing is said in [9] about a higher dimensional circle-based β-neighborhood. The lune-based β-skeleton is used for the analysis of empirical networks.

The convex hull and its parameterized generalization, the α-shape, describe aspects of the external structure of a set of sites. All other geometric graphs mentioned here describe different aspects of the internal structure. The inclusion relations between all these graphs are depicted in Fig. 2.

### 2.2. Computational complexities

Table 1 lists the time complexities to compute the graphs, and the references where these results can be found.

Fig. 1. Overview of the spectrum of planar β-neighborhoods.

<!-- p:6 -->


Fig. 2. Dependencies between geometric graphs. α represents the α-shape, β, the lune-based, β. the circle-based β-skeleton, and γ the γ-graph. The void and the complete graph are omitted. Graph 1 ←graph 2 denotes graph 1 ⊆ graph 2, and graph 1  graph 2 indicates that the parameterized graph 1 reduces to graph 2 for specific parameter values.

I do not know a reference for the complexity the ∞-SG. But since ∞-SG ⊆ EMST, one can examine each of the N – 1 edges in the EMST, and check if any site lies in the infinite strip. This check takes O(N) time, giving a total of O(N2).

The higher dimensional SIG can be constructed after computing the NNG, by examining each of the O(N2) pairs of sites in constant time, yielding O(N2) total time. The higher dimensional GG can be constructed by taking all O(N2) pairs of sites, and examining each neighborhood for inclusion of all N – 2 other sites. This results in O(N3) time.

The planar lune-based β-skeleton (denoted by β, in Table 1) is a subgraph of the GG when β≥0. Examining all the O(N) edges of the GG takes O(N) time per edge, giving a total of O(N2). The planar circle-based β-skeleton (βc) is also a subgraph of the GG when β≥0. Checking whether the Delaunay neighborhood of each edge in the GG contains the circle-based β-neighborhood takes constant time, giving order O(N log N). The O(N3) time applies to the case β &lt; 0, and results from a brute force algorithm, just as the O(N3) for the higher dimensional lune-based β-skeleton (remember that the circle-based β-skeleton has no direct higher dimensional analogue).

Table 1 Upper bounds time complexity

|             | 2D - upper bound   | 2D - reference   | kD - upper bound   | kD - reference   |
|-------------|--------------------|------------------|--------------------|------------------|
| CP          | O(N log N)         | 111              | O(N log N)         | [II              |
| NNG         | O(N log N)         | 111              | O(N(log N)k_')     | [II              |
| EMST m-SG   | O(N log N) O(N*)   | [I71             | O(N*) O(N')        | [151             |
| SIG         | O(N log N)         | WI               | OW')               |                  |
| RNG         | O(N log N)         | [181             | O(N')              | 1191             |
| GG          | O(N log N)         | [121             | O(N')              |                  |
| DT          | O(N log N)         | [111             | ,+ [k/Z] O(N )     | PI + 1161        |
| CH          | O(N log N)         | [I41             | O(Nt(k+')'21)      | [161             |
| o-Shape     | O(N log N)         | [71              | O(N'+ tail1 )      | 171              |
| p,-Skeleton | O(N'), O(N')       | [91              | O(N')              |                  |
| P,-Skeleton | O(N log N), O(N')  | 191              |                    |                  |


<!-- p:7 -->


## 3. The γ-neighborhood graph

The γ-neighborhood graph is defined for arbitrary dimension k. In the following we will use 'γ-graph', 'γ(γo, γ1)-graph', or simply 'γ(γo, γt)' and similar expressions, to denote the appropriate neighborhood graph.

In the definition of the γ-graph we use the following notation: for k≥2, r(x1, . . . , xk) denotes the radius of the smallest sphere through sites x1, . . . , xk in kD space. Thus for k = 2, r(x1, x2) equals d(x1, x2)/2.

The neighborhood graph γ(γo, γ1) is defined for −1 ≤ γo, γ1 ≤ 1, and |γo| ≤ lγıl. In kD space, the graph connects sites x1, ... , xk pairwise (k(k - 1)/2 edges) if an empty neighborhood N(γo, γ1) is associated with these sites, that is defined by two kD spheres through x, . . . , xk in the following way:

- (1) the spheres have radii

$$r ( x _ { 1 } , \dots , x _ { k } ) / ( 1 - | \gamma _ { 0 } | ) \ \text { and } \ r ( x _ { 1 } , \dots , x _ { k } ) / ( 1 - | \gamma _ { 1 } | ) ,$$

- (2) if γoγ1 &lt;0, the centers of the spheres lie on the same side of the plane through x1, . . . , xk; if γoγ1 &gt; 0, the centers lie on both sides of that plane.
- (3) if γ1 ≤0, we take the intersection of the two spheres; if γ1 ≥0, we take the union.

Noo oio      e d   a not  nd that the graph connects x1, . . . , xk, as soon as one neighborhood is empty. Note surts   i ta     =      s ta tres coincide, their common center lies in the plane through x1,..., xk, and the intersection equals the union.

For k = 2 the definition involves two sites and two circles, and r(x, x2) is scaled by factors 1/(1 - |γol) and 1/(1 - |γ1)|. The planar γ(γo, γ1) reduces to well-known geometric graphs for special values of γo and γ1:

- γ0 = γ1 = 0. The resulting neighborhood N(0, 0) is the smallest circle through x1 and x2, which is the Gabriel neighborhood. γ(0, 0) is the Gabriel graph.
- γ0 = γ1 = 1. The union of the two half-planes gives the entire plane. If no three sites are collinear, γ(1, 1) is a void graph.
- ynts s   -y   o s o   =  =  . x1 and x2. If no three sites are collinear, then γ(−1, -1) is the complete graph.
- γ0 = −1, γ1 = 1 and γ0 = 1, γ1 = −1. In both cases the two half-planes lie on the same side of the line through x, and x2. They therefore coincide (more generally, γ(γo, -γo) = γ(− γo, γo)). The neighborhood is empty if all other sites


<!-- p:8 -->


lie on one side of the line through x1 and x2, or on the line, but outside the segment from x1 to x2. That occurs only if x1 and x2 lie on the convex hull. Therefore, γ(-1, 1) and γ(1, -1) are the convex hull of the set of sites.

· γo = γ1. The graph γ(γo, γo) reduces to the circle-based β-neighborhood graph.

The relation of the planar γ-graph with other geometric graphs is depicted in Fig. 2. Fig. 3 gives a graphical overview of the whole spectrum of planar neighborhoods.

In 3D space, the definition of the neighborhood involves three sites and two spheres, and r(x1, x2, x3) is scaled by factors 1/(1 − |γol) and 1/(1 − |γ1l). Because the Gabriel neighborhood is the smallest sphere through two sites, whereas the kD N(0, 0) involves k sites, these neighborhoods do not coincide for k &gt;2. Further, it is not clear how to relate the higher dimensional N(γo, γo) to the circle-based β-neighborhood, since Kirkpatrick and Radke [9] do not tell how to generalize it to higher dimensions. Generalization of the lune-based neighborhood is straightforward, involving two sites in any dimension. The kD complete and the void graph however, result from the γ-graph if no k + 1 or more sites lie in a (k - 1)D plane. The convex hull equals γ(−1, 1) and γ(1, −1) in any dimension. Again, γ(γo, − γo) = γ(− γo, γo).

Fig. 3. Overview of the spectrum of planar γ(γo, γ1)-neighborhoods, −1 ≤ γo, γ1 ≤ 1, and −1 ≤ γ0/γ ≤ 1 (rectangles denote half-spaces).

<!-- p:9 -->


So far we have considered fixed values of the γ-parameters. We can also look at the largest values of the γ-parameters, for which the corresponding neighborhood is still empty. That is the value for which the sphere touches a (k + 1)th site, or is either 1 or -1 if there is no such site. We define γ([γo, γı], [γ2, γ3]) to be the graph connecting sites x1, ... , xk with each other, if the largest γ-parameter values for which the corresponding neighborhood is still empty, lie in [γo, γ1] and [γ2, γ3] respectively.

The γ([−1, 1], [0, 1])-graph connects sites x, . . . , xk in kD space if there are two spheres through these sites, of arbitrary radius, such that the union is empty. This is exactly a definition of the Delaunay triangulation, if no more than k + 1 sites are cospherical. If there are more than k + 1 cospherical sites, γ([-1, 1], [0, 1]) connects them all, whereas the Delaunay triangulation arbitrarily connects k sites, as long as the resulting (k – 1)D faces do not intersect.

The γ-graph describes the internal structure of a set of sites. But it also describes aspects of the external structure. For example, the γ(-1, 1)-graph reduces to the convex hull. Also, the next section gives an example in which special γ-parameter values give a clear external structure, and Section 6 will show how it is used to find a boundary through all sites.

This capability of external structure description somewhat contrasts to the lunebased β-skeleton. In this graph, the neighborhood is located between the two sites. The resulting graph therefore emphasizes connections between sites, which makes it suitable for network analysis. In the γ-graph, the spheres are located aside the k involved sites. Especially when the neighborhood is the union of these spheres, the γ-graph is more like (a part of) a tesselation.

## 4. Examples

The types of graphs that result from specific choices of the parameters is most clearly demonstrated with planar graphs. Figs. 4, 5, and 6 show planar γ-graphs on the same set of 20 sites.

Fig. 4 shows a sequence of γ([−1, 1], [γo, 1]-graphs. For γo = 1, this yields the convex hull. Lowering γo introduces more and more edges in the graph, until for γo=0 the graph coincides with the Delaunay triangulation. When γo gets negative, edges cross each other. For γo = –1, the graph would be complete (not shown).


<!-- p:10 -->


Fig. 4. Planar γ-graphs on the same set of sites, containing more and more edges.

The graphs in Fig. 5 all coincide with a circle-based β-skeleton. The neighborhoods N(0.2, 0.2), N(0.1, 0.1), N(0, 0), and N(−0.2, −0.2) get smaller and smaller. The emptiness requirement gets less restrictive, so that more pairs of sites are considered as neighbors. The γ(0, 0)-graph equals the Gabriel graph.

Fig. 6 depicts graphs that result when only intersections of circles are allowed as neighborhood. The graph γ([−1, 1], [−1, 0]) connects all pairs of sites that have no empty circle through themselves. It is the complement of the Delaunay triangulation. In γ[−ł, ł], {−1, 0]), the intersections are forced to have a certain atttoi s o  ( -1]  - n oo   aons. The edges now join sites only when there is another site close to the edge. In γ([-1, 1], [-1, -0.9]) the neighborhoods are so thin, that only sites are connected if there is another site almost on the edge.

Fig. 7 shows a set of sites similar to the one used in [7] to illustrate the α-shape. The γ(-0.15,0.3)-graph turns out to give a clear boundary, although also internal sites are connected. The α-shape, designed to give the boundary of a cluster of sites, yields a single inner and outer contour. However, the two γ-parameters give more freedom for finding some external structure than the single parameter β-skeleton (see [9] for a β-skeleton on the set of sites from [7]). Fig. 8 at last, shows projections of two stereo-pairs of 3D γ-graphs on the same set of 30 sites. The 3D γ(0, 0)-graph connects three sites with each other if the smallest sphere through these sites is empty. Note that in 3D, this differs from the Gabriel graph, which connects two sites if the smallest sphere through these sites is empty. The picture of the γ(0, 0)-graph only slightly differs from a typical 3D Delaunay triangulation. This is because the triangles that belong to the γ(0, 0) but not to the Delaunay triangulation, can have edges that are also edges of other triangles in the γ(0, 0). All edges of a triangle can thus be displayed, while the triangle does not belong the graph. In this example, the Delaunay triangulation consists of 257 triangles (constituting 248 tetrahedra), and the γ(0, 0) of only 150 triangles.


<!-- p:11 -->


iel- e ne ss o s s e o e- ed o eeos   ins

<!-- p:12 -->


Fig. 6. A sequence of planar γ-graphs on the same set of sites. The neighborhoods consist of the intersection of circles.

Fig. 7. The γ-graph describing an external structure on the planar set of sites after [7].

<!-- p:13 -->


Fig. 8. Two stereo-pairs of perspectively projected 3D γ-graphs.

This lt st dit ss s sp s d-t l  t es are connected to each other, if at all.

## 5. Complexity issues

The following three lemmas tell how γ-graphs are related to each other. They give cues how to construct an arbitrary γ-graph. The two subsequent theorems tell how efficiently they can be computed.

Lemma 1. γ(γo, γ1) = γ([γo, 1], [γ1, 1] if γ1 ≥ 0.

Proof. If γ1≥0, the neighborhood is defined by the union of two spheres. That neighborhood is contained in all neighborhoods that are the union of two larger or equally sized spheres, see Fig. 9. So when N(γo, γı) is empty, the largest parameter values for which the neighborhood is still empty are not less than γo and γ1 respectively. Thus γ(γo, γ1) ⊆([γo, 1], [γ1, 1]). Conversely, look at the pair of sites having parameter values for which the largest neighborhood is still empty, and which are not less than γo and γ1 respectively. They also have an empty N(γo, γ1) so γ(γo, γ1) ∃ γ([γo, 1], [γ1, 1]. □


<!-- p:14 -->


Fig. 9. Shaded area denotes neighborhoods that contain N(γo, γ1).

Lemma 2. γ(γo, γ1) = γ([γo, 1], [γ1, 1]) ∪ γ([γ1, 1], [|γol, 1]) if γ1 ≤ 0.

Proof. If γ1≤0, the neighborhood is the intersection of two spheres. That neighborhood is contained in all neighborhoods that are the intersection or union of spheres defined by parameters larger than γo and γ1. But N(γ2, -γ2) equals N(− γ2, γ2), specifically for γ1 ≤ γ2 ≤ γo. N(γo, γ1) is therefore also contained in all neighborhoods that are the union of spheres defined by parameters larger than γ1 and |γol respectively, see Fig. 10. So when N(γo, γ1) is empty, the largest parameter values for which the neighborhood is still empty, are not less than γo and γ1, or γ1 and |γol. Thus γ(γo, γ1) ⊆ γ([γo, 1], [γ1, 1]) ∪ γ([γ1, 1], {γol, 1]). Conversely, look at the pairs of sites having parameter values for which the largest neighborhood is still empty, and which are not less than γo and γ1 or γı and |γol. They also have an empty neighborhood defined by γo and γ1, so γ(γo, γ1) ⇒ γ([γo, 1], [γ1, 1]) ∪ γ(γ1, 1], [γol, 1]).

Lemma 3. γ([γo, γ1], [γ2, γ3]) ⊆ γ([γ4, γs], [γ6, γ7]) if [γo, γ1]⊆[γ4, γ5] and [γ2, γ3]⊆[γ6, γ7].

Proof. Consider the pairs of sites joined by an edge in γ([γo, γı], [γ2, γ3]). Their largest γ-parameters defining an empty neighborhood lie in [γo, γı] and [γ2, γ3].


<!-- p:15 -->


Fig. 10. Shaded area denotes neighborhoods that contain N(γo, γ1).

Then they certainly lie in [γ4, γs}⇒[γo, γ1] and [γ6, γ7]⇒[γ2, γ3]. So all these sites are also joined by an edge in γ([γ4, γs], [γ6, γ7]), and thus γ([γo, γ1], ([] ( ]

Lemmas 1, 2, and 3 are illustrated in Fig. 11. According to Lemma 1, γ(, ν) = γ(, 1], [2, 1]) (say G1), and likewise γ(−1, ‡) is equal to γ([−4, 1], [1, 1]) (G2). Lemma 2 says that γ(0, −‡) = γ([0, 1], [−1, 1]) ∪ γ([−1, 1], [0, 1]) (G3), and γ(0, −) = γ([0, 1], [−1, 1]) ∪ γ([−1, 1], [0, 1]) (G4). And Lemma 3 says G1 ⊆ G2 ⊆ G3⊆ G4, as illustrated in the figure.

Theorem 1. Any k-dimensional γ-graph can be computed in O(Nk+1) time.

Proof. A brute force algorithm takes all the () possible combination of k sites, and checks whether any of the N – k other sites lie in the neighborhood defined by the γ-parameters. This amounts to O((N − k)(λ)) = O(Nk+1) time. □

Theorem 2. For nondegenerate sets of sites, the planar γ([γo, γ1], [γ2, γ3]) can be computed in O(N log N) time, and the k-dimensional one in O(N1+[k/2]) time, provided that [γo, γ1] ⊆ [−1, 1] and [γ2, γ3] ⊆ [0, 1].

Proof. When [γo, γ1]⊆[−1, 1] and [γ2, γ3] ⊆ [0, 1], γ([γo, γ1], [γ2, γ3]) is a subgraph of γ([−1, 1], [0, 1]) according to Lemma 3. When the position of the sites is nondegenerate, γ([-1, 1], [0, 1]) is the Delaunay triangulation. After coa t v v  c  ta t tc  ch (k – 1)-simplex lie in the allowable range in constant time. The upper bounds to compute the Delaunay triangulation thus carry over to the γ-graph. These are O(N log N) for 2D, and O(N1+ [k/2]) for kD (see Section 2). □


<!-- p:16 -->


Fig. 11. Four γ-graphs on the same set of 30 sites. γ(1, ν) ⊆ γ(−‡, ‡) ⊆ γ(0, −1) ⊆ γ(0, −1).

For the Delaunay triangulation, O(N log N) is optimal. Whether this is optimal for the γ-graph, depends on the parameter values. It is clearly not optimal when the γ-graph reduces to the void graph.

Both O(N log N) and O(N1+[k/2]) only apply to nondegenerate cases. Because in the degenerate case that all sites lie on a k-dimensional sphere, the size of the output is already O((x)) = O(Nk).

## 6. Application

The γ-graph can be used to (re)construct a boundary of a set of sites [21, 22]. The sites are thought to be measured from the surface of a 2-dimensional or


<!-- p:17 -->


3-dimensional object. The problem is to find a simple closed polygon or polyhedron passing through all the sites. This is also called a Hamilton polygon or Hamilton polyhedron.

In order to find a Hamilton polygon or polyhedron, we take γ([-1, 1], [0, 1]), axu  i  t oy ss oro y ss tex hull). We go on shrinking the hull, until all vertices are included in the boundary. However, by removing a simplex we may not introduce an isolated vertex, dangling boundary segments, or a self-intersecting boundary. The following short description for the planar case indicates the way simplices are selected for deletion.

A value is associated to all current boundary edges, based on the γ-values of the boundary segments. We keep the sign of the γ-values of the boundary edges consistent with the following rule: if -1 ≤ γ &lt;0, the center of the associated circle lies on the side of the boundary segment that is outside the current boundary, and if 0 &lt; γ ≤ 1, the center lies on the side of the boundary segment that is inside the current boundary. The selection of the triangle to be removed is based on the attempt to, informally speaking, change slightly the shape of the current boundary, relative to the size of the triangle. Formally, we choose the triangle with the largest interior angle at the vertex opposite to the boundary edge.

Let us call the radius of the circle through the vertices of the triangle that we consider, R, the γ-value of the boundary edge corresponding to that triangle, γ, and the two vertices on the boundary, x, and x2. We abbreviate r(x1, x2) to r. If γ ≥0, the angle φ at the interior vertex increases when r/R increases. If γ ≤ 0, φ increases when 2 -r/R increases. The exact relation is given by the sine rule: r/R = sin φ. By definition, r/R equals 1 − {γ}, which is 1 − γ for a nonnegative γ. Similarly, 2 − r/R expands to 1 + |γ|, which equals 1 − γ for a nonpositive γ. This results in the following selection rule:

among all removable triangles, delete the one whose boundary edge has the largest value for 1 - γ (or equivalently, the smallest value for γ).

A more detailed description, including the 3-dimensional case, is given in [21, 22]. The method described so far does not always succeed. In the first place, the shrinking operation can get locked, although the initial graph does contain a Hamilton polygon. This happens when there are no more removable edges, and not all vertices are included yet in the boundary. Secondly, there exist nondegenerate non-Hamiltonian Delaunay triangulations [6], and thus γ([–1, 1], [0, 1])-graphs. Therefore methods based on shrinking from the Delaunay triangulation do not guarantee success.

In both cases, the solution is to shrink from a γ([-1, 1], [γo, 1])-graph, for some γo&lt; 0. Such a graph contains more edges. The extra triangles will have smaller interior angles at the vertex opposite to the boundary edge, than overlapping triangles from γ([–1, 1], [0, 1]). They offer more choice in selecting a boundary edge for deletion. For a γo small enough, γ([-1, 1], [γo, 1]) will be -a sn (-−-−) =(−-1  - rs a ) a0o tains a Hamilton polygon), and locking of the shrinking process will not occur.


<!-- p:18 -->


Fig. 12. Planar non-Hamiltonian Delaunay triangulation (after [6]), and three Hamiltonian γ-graphs.

Fig. 12 shows a Delaunay triangulation from [6], that contains no boundary through all the sites. The three other γ-graphs make it feasible to find such a boundary.

## 7. Conclusions

In this paper we have introduced the γ-neighborhood graph. The γ-graph describes the internal structure of a set of sites. It has been shown briefly that it can also be used to find the external structure, specifically a simple boundary through all sites. The inclusion hierarchy CP ⊆ NNG ⊆ MST ⊆ RNG ⊆ GG ⊆ DT has been extended: DT ⊆ γ-graph. The γ-graph provides for a general framework in describing neighborhood graphs. It unifies the convex hull, the Delaunay triangulation, and in 2D also the Gabriel graph and the circle-based β-skeleton, into a continuous spectrum ranging from the void to the complete graph.

The neighborhood N(γo, γ1) is defined only for γo, γ1 ∈ [−1, 1], and |γol ≤ |γı|. For k sites and specific parameters γo and γ1, there can be two neighborhoods, since the spheres can be interchanged. The sites are connected if at least one of the two neighborhoods is empty. We could also use the parameters |γol ≥ |γı| and completely specify the position of the spheres, for example γo specifies 'the left', ao e e       t    ds l ,  no need to specify a preference for one direction.


<!-- p:19 -->


I have shown that the γ([γo, γı], [γ2, γ3]) can be constructed efficiently if it is a subgraph of the Delaunay triangulation, that is, when [γo, γ1] ⊆[−1, 1], and [γ2, γ3] ⊆ [0, 1], and the Delaunay triangulation is nondegenerate. Programs have been developed that construct the γ-graphs. They have been written in the programming language C, on a UNIX workstation. All the example graphs in this paper have been generated by these programs.

There are several directions for further research. The most urgent is the development of output sensitive algorithms. Of course for γ &lt;0, the worst case size of the γ-graph is O(N3), but an algorithm having a time complexity that depends on the size of the output can probably do better than O(N3). Also for γ &gt;0 an output sensitive algorithm can be profitable, since the size of the γ-graph may be sub-linear in N.

Little is known from stochastic geometry about probabilistic properties of geometric graphs (some results are known about the DT [13], the GG, and the RNG [5]). Insight in the expected number of edges in the γ-graph may lead to the development of efficient algorithms for the average case.

A final research suggestion is the construction of γ-graphs on sets of weighted sites.
