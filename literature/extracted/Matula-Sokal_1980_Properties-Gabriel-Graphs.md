---
id: "Matula-Sokal_1980_Properties-Gabriel-Graphs"
source_pdf: "../pdf/Matula-Sokal_1980_Properties-Gabriel-Graphs.pdf"
source_filename: "Matula-Sokal_1980_Properties-Gabriel-Graphs.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "excellent"
extraction_score: 108.0
visual_assets: "disabled"
references_file: "../references/Matula-Sokal_1980_Properties-Gabriel-Graphs.references.md"
---

<!-- p:1 -->

David W. Matula and Robert R. Sokal*

Properties of Gabriel Graphs Relevant to Geographic Variation Research and the Clustering of Points in the Plane

## 1. INTRODUCTION AND SUMMARY

In geographic variation analysis in biology, one or more variables are commonly mapped ono a set of points in the plane, such points representing sampling station localities or areal unit centroids. The variables may be interval (morphometric variables, population densities, gene frequencies), ordinal (ranks), or -oner   oie  se Ss Ssas Sse nca tion of the methods of statistical geography to other disciplines. Many of the techniques for analyzing such variables require the construction of a geographicconnectivity network or graph among the sampling station localities. In such geographic-connectivity graphs, one connects by lines those pairs of points thought in some geographic sense to represent adjacent localities. Thus the pattern of geographic variation of a variable is evaluated with regard to the interconnectedness of the sampling station localities for which the variable has been measured. These geographic-connectivity graphs play an important role in numerous applications, three of which might be singled out here.

1. An approach to the regionalization problem defines regions as statistically homogeneous and geographically connected areas [6]. In such problems, tohi  oh eh i sohi ohi hie connectivity graph among the localities. Some other approaches to the regionalization problem (e.g., [5, 15, 20, 33]) employ geographic-connectivity graphs as well.
2. In many tests for randomness of geographic variation patterns [18, 22, 27 ], a connection matrix is essential to formulating a null hypothesis of random variation patterns.
3. Application of the technique of spatial autocorrelation [4, 12, 13, 26, 31, 32] usually requires formulation of a geographic-cónnectivity graph for localities.

*This study was supported in part by Grant No. DEB 77-04824 from the National Science Foundation. This article appears as Contribution No. 338, Graduate Program in Ecology and Evolution, State University of Ñew York at Stony Brook.

David W. Matula is professor of computer science, Southern Methodist University. Robert R. Sokal is professor of ecology and evolution, State University of New York at Stony Brook.

0016-7363/80/0780-0205$00.50/0©1980 Ohio State University Press GEOGRAPHICAL ANALYSIS, vol. 12, no. 3 (July 1980) Submitted 6/79. Revised version accepted 10/79.


<!-- p:2 -->


Various criteria have been proposed for constructing geographic-connectivity graphs [34]. Gabriel connectivity is defined in [6]: "Any two localities [points in the plane] A,B, are said to be contiguous iff all other localities are outside the A-B circle, that is, the circle on whose circumference A and B are at opposite points. In other words, two localities A and B are contiguous, unless there exists some other locality C such that in the triangle ABC the angle subtended at C is of 90° or more." The Gabriel connectivity criterion is alternatively characterized (using Euclidean distance) by the least squares adjacency criterion where locality A is adjacent to locality B iff the square of the distance between A and B is less than the sum of the squares of the distances to any other locality C. The least sn sg       ig  sens distances in higher dimensions, arbitrary distances, or numerical proximity functions, but these interesting directions are beyond the scope of the geographicconnectivity issues addressed in this paper.

In section 3 we discuss the planarity and faces (see [9, p. 102]) of a Gabriel graph diagram. Planarity establishes that the two conditions required by Gabriel and Sokal [6] for geographic contiguity are satisfied by the lines determined in the Gabriel graph. Specifically, (i) if A,B are adjacent, then there exists a continuous band of other points in the plane (not sampled) from A to B, and (ii) if there are two distinct pairs of points A,B and C, D each of which is geographically contiguous, the band joining A and B has no point in common with the band joining C and D. This second requirement is necessary to avoid the intersection of two mutually exclusive connected sets that should belong to two separate regions. The appropriateness of the planarity condition for geographical studies makes the Gabriel graph a more desirable extension of single linkage than other natural linkage adding extensions such as k-linkage (k-nearest neighbors) [17, 19], where the likelihood of nonplanarity may introduce unwarranted mathematical and geographical complexity. The uniqueness of the Gabriel graph also makes it preferable to other methods of connecting localities such as triangulation, where a very large number of distinct solutions is possible [2]. Also, the specific Delaunay triangulation can contain long lines opposite the obtuse angles darr y u  r p sr ra r r pok

Two other frequently used criteria for generating geographic-connectivity ras    e rs rs     soe sgne linkage or nearest neighbor method of cluster analysis [25, pp. 216–22]) and the Thiessen (Voronoi) diagram with its dual the Delaunay triangulation [1]. The shortest spanning tree is an important first-order geographic-connectivity graph. In most applications, however, a greater degree of interconnectedness for localities to receive input from and contribute output to adjacent localities is desired in the geographic-connectivity graph. In section 2 we prove that the Gabriel graph (more generally the least squares adjacency graph) must contain the edges of any shortest spanning tree, so the Gabriel connectivity criterion is an appropriate extension of the single-linkage criterion that avoids the possible lack of uniqueness inherent in determining a shortest spanning tree. The observation that the Gabriel graph is a subgraph of the Delaunay triangulation [11] is utilized to provide yet another characterization of Gabriel graphs, which provides for efficient computation of the Gabriel graph from the Delaunay triangulation. Shamos and Hoey [24] have shown that the Thiessen diagram (and Delaunay triangulation) on n points can be determined in computation time no greater than some constant times n log n, so we conclude that Gabriel graphs may be efficiently utilized even in cases of relatively large point sets.

diagrams.

Gabriel graphs have been employed in geographic variation studies in biology

15384632, 1980, 3, Downloaded from https://onlinelibrary.wiley.com/doi/10.1111/j.1538-4632.1980.tb00031.x by Cochrane Mexico, Wiley Online Library on [02/06/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License by numerous authors [3, 10, 16, 23, 28, 29, 30, 31, 32, 35]. In the biological models studied (typically gene flow), the interconnections produced from Gabriel graphs of the sampling station points appear to make intuitive sense to biologists. In other geographic models, where the flow of materials and information is not limited to special transportation channels, the Gabriel criterion should also be appealing. Figure 1 shows a Gabriel graph diagram on fifty-three locations in the eastern United States utilized in a geographic variation study of aphid stem mother data [22]. The Gabriel graph has eighty edges (denoting contiguous pairs of sampling stations) on the fifty-three vertices (sampling station points in the plane) and seems to provide sufficient but not excessive interconnections for the analysis of the morphometric variation in these data.


<!-- p:3 -->


In section 4 we investigate those frequently encountered graphs that can and cannot be realized as Gabriel graphs by the appropriate location of vertices in the plane. Of considerable interest is the result that no four vertices can ever be mutually pairwise adjacent in any Gabriel graph—a more restrictive result than

A planar graph diagram such as the resulting Gabriel graph diagram of Figure 1 divides the plane into disjoint faces each surrounded by the edges of a cycle of the graph. Note in Figure 1 that some faces are triangular, some are bounded by n-cycles with large n, and some faces are nonconvex. In section 3 we also investigate the alteration in the faces of a Gabriel graph diagram caused by the deletion or insertion of other vertices (sampling station localities) from or into the plane.

Fic. 1. A Gabriel Graph on Fifty-Three Sampling Station Locations in the Eastern United States. The numbers at the vertices of the graph are code numbers for the 53 localities [22, 31].

15384632, 1980, 3, Downloaded from https://onlinelibrary.wiley.com/doi/10.1111/j.1538-4632.1980.tb00031.x by Cochrane Mexico, Wiley Online Library on [02/06/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License in general planar graphs where four but not five vertices may be mutually pairwise adjacent. Also, we show that no two vertices can each be adjacent to the same set of three other vertices in a Gabriel graph.


<!-- p:4 -->


If the Gabriel graph provides an adequate model for representation of information exchange, such as gene flow among localities, then it becomes of interest to develop some measure of complexity of the network. Thus, among localities distributed linearly along a straight shoreline, minimum connectivity will result and the number of edges will be n-1 for n vertices. Many of the well-known measures of connectivity (e.g., [14]) require knowledge of the maximum number of edges possible in the graph. In examples from population biology, such measures would be quite useful in permitting tests of the variability of characters and gene frequencies related to the interconnectedness of their patterns. In section 5 we investigate the density of edges in Gabriel graphs and the resulting average face boundary sizes. For any n, it is shown that a maximally edge-dense Gabriel graph exists with at most two or three fewer edges than that of a maximal planar graph, and in the Gabriel graph diagram, all interior faces are bounded by 3cycles so that the graph is fully triangulated except for the exterior infinite face which is separated by a 5- or 6-cycle from the finite interior faces. For the "average" case where n vertices are placed uniformly randomly in the unit square, we show that each interior vertex will be expected to have about four other vertices adjacent to it in the Gabriel graph diagram on those vertices. It is further noted that the average face boundary size will be near four in the Gabriel graph diagram, in contrast to the average of three for Delaunay or other triangulations on the same vertex locations.

## 2. GABRIEL GRAPHS, SHORTEST SPANNING TREES, AND DELAUNAY TRIANGULATIONS

V denotes a finite nonvoid set of vertices. The proximity of vertices of V is assumed to be given by the distance matrix D = [daB] on V, where D is any nonnegative real symmetric matrix with dAB = 0 iff A = B. The vertices A, B ε V, A ≠ B are least squares adjacent forming the edge AB iff

$$d _ { A B } ^ { 2 } < d _ { A C } \, ^ { 2 } \, + \, d _ { C B } \, ^ { 2 } \, \text {for all } C \, \varepsilon \ V , \, C \neq A , \, C \neq B \ .$$

The vertices and pairs of least squares adjacent vertices (edges) determine the least squares adjacency graph G(V). Furthermore, if V is a set of points in the plane and dAB denotes Euclidean distance, then G(V) is a Gabriel graph [6].

A spanning tree on the vertex set V is a tree (i.e, a connected graph without cycles) covering all vertices of V. For a general vertex set V and distance matrix D, a shortest spanning tree, T(V), has the sum of distances dAB over all edges AB of the spanning tree T(V), a minimum over all spanning trees on V. Ties in the sums of distances may allow more than one shortest spanning tree on V; however, there is always à unique least squares adjacency graph on V, which we now show includes all shortest spanning trees.

THEOREM 1. Given a distance matrix D on the vertex set V, every shortest spanning tree T(V) is contained as a subgraph of the least squares adjacency graph G(V).

Proof. Let T(V) be a shortest spanning tree on V, and assume edge AB of T(V) is not in G(V). Deletion of AB from T(V) yields two subtrees, TA containing A

15384632, 1980, 3, Downloaded from https://onlinelibrary.wiley.com/doi/10.1111/j.1538-4632.1980.tb00031.x by Cochrane Mexico, Wiley Online Library on [02/06/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License and TB containing B, where each vertex of V is in either TA or TB. Since AB is not an edge of G(V), from (1) there must exist a point C ε V, C ≠ A, C ≠ B, such that dAC &lt; dAB and dCB &lt; dAB. Now if C is in TA, then TA and TB and edge CB form a spanning tree on V with sum of distances less than that of T(V), a contradiction. A similar contradiction arises if C is in TB, so AB must be an edge of G(V), and the theorem follows.


<!-- p:5 -->


It should be emphasized that theorem 1 pertains to arbitrary distance matrices and not just planar Euclidean distances. Since the shortest spanning tree has been shown to characterize the single linkage (nearest neighbor) cluster method [7, 21], theorem 1 is of general interest as an extension of single linkage cluster analysis. For all further results we shall assume that V is a set of points in the plane, D is Euclidean distance, and G(V) is a Gabriel graph.

For a set of points V in the plane, drawing straight lines between least squares adjacent points in the plane yields the Gabriel graph diagram for G(V), as illustrated'in the example of Figure 1. In general, Gabriel graphs have interesting properties derived from geometrical considerations pertaining to planar Euclidean distance, which are intuitively evident in the Gabriel graph diagram. The following lemma is straightforward from elementary geometrical arguments and provides two important properties of Gabriel graphs.

LEMMA 1 [6]. The following are equivalent definitions for Gabriel graphs. (i) AB is an edge of the Gabriel graph G iff the circle with diameter arc AB contains no other vertex of Vin its interior or on its boundary; (ii) AB is an edge of the Gabriel graph G iff the angle ACB is acute for every C ε V, C ≠ A, C ≠ B.

Given a set of vertices V in the plane, the region containing all points of the plane as close as, or closer to, a given vertex A of V than to any other vertex of V is the Thiessen polygon for A. The set of Thiessen polygons for all vertices of V is the Thiessen (or Voronoi) diagram. The Thiessen diagram is a planar map, and its geometric dual [9, p. 113] is known as the Delaunay triangulation (see [1] for a recent survey of the origins of these diagrams). The Delaunay triangulation is a planar graph diagram, which generally (but not always) has all interior regions bounded by triangles.

Howe [11] has noted that the Gabriel graph is a subgraph of the Delaunay triangulation, and that observation is utilized to provide the following additional characterization of Gabriel graphs.

LEMMA 2 [11]. The Gabriel graph on a vertex set V is a subgraph of the Delaunay triangulation for V. Furthermore, the edge AB of the Delaunay triangulation is an edge of the Gabriel graph iff the straight line joining A to B intersects the boundary line segment common to the Thiessen polygons for A and B at a point other than the endpoints of that boundary line segment .

Proof. For A, B ε V, suppose the midpoint of the straight line between A and B has no other vertices of V as close as A and B. Then a segment of the perpendicular bisector of AB, extending on both .sides of the midpoint of AB, must form part of the boundary of the Thiessen polygons for A and B, and conversely. Hence the lemma.

Shamos and Hoey [24] have utilized a recursive computational geometry procedure to show that the Thiessen diagram can be computed in time bounded by a constant times n log n for any number n of vertices in the plane. From lemma 2

15384632, 1980, 3, Downloaded from https://onlinelibrary.wiley.com/doi/10.1111/j.1538-4632.1980.tb00031.x by Cochrane Mexico, Wiley Online Library on [02/06/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License it is then evident that Gabriel graphs can be computed with similar efficiency so that they may be utilized in applications with relatively large numbers of vertices.


<!-- p:6 -->


## 3. PLANARITY AND FACES OF GABRIEL GRAPH DIAGRAMS

Note that any graph that may be embedded in the plane such that distinct edges do not intersect except at vertices is termed a planar graph, whereas a particular embedding is separately termed a graph diagram (or plane graph, see [9, p. 102]). The important observation that any Gabriel graph is a planar graph was noted without proof by Gabriel and Sokal [6], and the result also follows from the fact that a Gabriel graph is a subgraph of the Delaunay triangulation [11]. We include an alternative direct proof.

THEOREM 2. A Gabriel graph is a planar graph.

Proof. Assume the lines AB and CD of a Grabriel graph diagram intersect at an interior point (see Fig. 2). The sum of the angles ACB, CBD, BDA, and DAC must equal 360°, so at least one of them, say ACB, must be at least 90°. But then AB is not an edge of the Gabriel graph by lemma 1. This contradiction establishes the fact that any Gabriel graph is a planar graph.

FIG. 2. Proof that a Gabriel Graph Is a Planar Graph

A cyclic sequence of edges such as AB, BC, CD, DE, EA, where successive edges are incident to distinct common vertices, forms a cycle of a graph. If repetition of edges is allowed, the sequence is a closed walk. Note that every cycle in the Gabriel graph diagram will bound some finite interior region of the plane. The innermost regions bounded by cycles without interior chords, along with the infinite exterior region, will effectively form a partition of the plane into faces. Formally, an interior face of a Gabriel graph diagram is a finite continuous region of the plane bounded by the vertices and edges of a cycle (or closed walk) of the graph and having no vertices or edges in its interior. It follows from Euler's l   s  l  (nm   s lr oon Caq  s        r en

Number Interior Faces = Number Edges – Number Vertices + 1 . (2)

The Gabriel graph diagram of Figure 1 has 80 edges, 53 vertices and 80 – 53 + 1 = 28 interior faces, 10 of which are bounded by 3-cycles, with the largest face boundary being a 13-cycle. Faces of a Gabriel graph diagram can have boundary n-cycles with arbitrarily large n, and a face may be nonconvex when n ≥ 6. Although any particular n-cycle of a Gabriel graph may or may not bound an individual face of the diagram, the 3- and 4-cycles of a Gabriel graph have an important property that limits the faces in their interior.

THEOREM 3. Any Gabriel graph diagram for the Gabriel graph G can have no vertex interior to any 3-cycle or 4-cycle of G.

Proof. For n = 3 or 4, let A1, A2, . . ., A be the vertices of an n-cycle of the

15384632, 1980, 3, Downloaded from https://onlinelibrary.wiley.com/doi/10.1111/j.1538-4632.1980.tb00031.x by Cochrane Mexico, Wiley Online Library on [02/06/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License Gabriel graph G. Suppose a Gabriel graph diagram for G contains another vertex B in the interior of this n-cycle. Add the lines AB to the diagram for 1 ≤ i ≤ n, a =      =  )   + ( ) t t  ) or 4, one of these angles is at least 90°. By lemma 1, this contradicts the fact that the edges of the boundary cycle are in the Gabriel graph. Thus there can be no vertices of G interior to any 3- or 4-cycle in the diagram.


<!-- p:7 -->


CoROLLARY 3.1. For any Gabriel graph diagram, every 3-cycle and every chordless 4-cycle determines an interior face.

Proof. Any 3-cycle or 4-cycle of the Gabriel graph diagram bounds some finite interior region of the plane. This region cannot contain any vertices of the graph by theorem 3, and no edges if the cycle is also without chords, and therefore is

an interior face of the diagram.

It is apparent that the deletion or insertion of a vertex in a Gabriel graph diagram will alter the composition of faces in the neighborhood of the specific vertex. Investigation of vertex deletion and insertion provides considerable insight into the nature of the faces of a Gabriel graph diagram. The following result

shows the stability obtained on deletion of all vertices "outside a face.'

LEMMA 3. Let VC V be the vertices of a cycle that bounds an interior face F

of the plane in a Gabriel graph diagram for G(V). Then the Gabriel graph diagram for G(VF), determined solely by the vertices of VF, has F as an interior face, and if F is convex, this is the only interior face.

Proof. Each pair of vertices of VF that are adjacent in the Gabriel graph diagram for G(V) will be adjacent in the diagram for G(VF). Thus the boundary cycle u      (          obp in G(VF) that was not in G(V). Then some vertex C ε V− VF must fall in or on the circle with diameter arc AB. Assume AB is an interior chord bisecting the region F. Then C must be outside of F, and the triangular region formed by A, B, and C cannot contain another vertex DεVF for then AB could not be an edge of G(VF). Thus some edge A1A2 of the boundary cycle of F must intersect both th               cts the fact that A1A2 is an edge of G(V). Hence AB cannot be an interior chord bisecting F in G(VF), so F is also an interior face of G(VF) and is clearly the only face when F is convex.

There is no comparable stability result for the faces of a Gabriel graph regarding insertion of vertices as may be inferred from the sequence of Gabriel graph diagrams generated by successive vertex insertions in Figure 3. Note that the interior face in 3a is unrelated to the interior faces in 3b, 3c, 3d, and 3e. Finally note that vertex insertion can change more than the closest neighboring faces as seen in 3e, where the final vertex insertion yields a graph with no interior faces. If edges rather than faces are more pertinent to a particular application of Gabriel graphs, then an interpretation yielding a measure of edge stability under vertex insertion is relevant. Specifically, if the vertex C is inserted into the Gabriel graph diagram for G(V), then clearly (i) all inserted edges of G(V∪{C}) are incident to C; and (ii) the edge AB of G(V) is deleted iff dCA2 + dCB2 ≤ dAB2. Localization of the effect of edge deletion is implicit from (ii), in that if d* is the maximum distance for any edge of G(V), then any edge AB deleted in forming G(V∪{C}) must have had both vertices A and B strictly within the circle of radius d* about C. Reinspection of the succession of Gabriel graphs of Figure 3, utilizing these observations relevant to edge insertion and deletion, provides a

15384632, 1980, 3, Downloaded from https://onlinelibrary.wiley.com/doi/10.1111/j.1538-4632.1980.tb00031.x by Cochrane Mexico, Wiley Online Library on [02/06/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License better understanding of the extent to which the phenomena exhibited may cause difficulties in applications.


<!-- p:8 -->


FiG. 3. Gabriel Graphs Determined after Successive Vertex Insertions. The initial vertices 1, 2, 3 in figure 3a are augmented by 4, 5, 6, and 7 in figures 3b through 3e respectively. Each insertion changes the resulting Gabriel graph as shown.

## 4. SOME SPECIAL GABRIEL GRAPHS AND FORBIDDEN SUBGRAPHS

A graph G = (V,E) is defined abstractly by a vertex set V and an edge set E. The graph G = (V,E) is then a Gabriel graph if there exists an embedding of the vertex set V in the plane so that the edges of E are precisely the vertex pairs that satisfy the least squares adjacency criteria given by inequality (1). To understand the general structure of Gabriel graphs without specific reference to the actual embedding of the vertices V in the plane, it is instructive to catalogue those frequently encountered graphs that can and cannot arise as Gabriel graphs or as subgraphs of Gabriel graphs.

For n ≥ 3, the Gabriel graph determined by. placing n points uniformly spaced around the circumference of a circle in the plane is readily determined to be the graph Cn, composed of a single n-cycle, which proves the following.

LEMMA 4. The cycle Cn is a Gabriel graph for all n ≥ 3.

A graph Wn on n ≥ 4 vertices composed of a cycle C-1 and an additional vertex adjacent to all vertices of the cycle, is termed a wheel (see Fig. 4).

LEMMA 5. The wheel Wn is a Gabriel graph iff n ≥ 6.

Proof. If Wn is a Gabriel graph, then by Euler's formula (2) it must have n – 1 interior faces. For n = 4, the four 3-cycles. of W4 would all have to bound interior faces of a Gabriel graph diagram by corollary 3.1, a contradiction, so W4 is

FIC. 4. The Wheels W4 and W7

15384632, 1980, 3, Downloaded from https://onlinelibrary.wiley.com/doi/10.1111/j.1538-4632.1980.tb00031.x by Cochrane Mexico, Wiley Online Library on [02/06/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License not a Gabriel graph. For n = 5, the four 3-cycles and one chordless 4-cycle of W5 would all have to bound interior faces of a Gabriel graph diagram by corollary 3.1, a contradiction, so W5 is not a Gabriel graph. For n ≥ 6, Wn is shown to be a Gabriel graph as follows. Locate n - 1 points uniformly spaced on the circumference of a circle, and place another point at the center of the circle, as shown for n = 7 in Figure 4b. The resulting Gabriel graph diagram is then a diagram of Wn.


<!-- p:9 -->


It is not generally true that every subgraph of a Gabriel graph is a Gabriel graph, since deletion of vertices in a Gabriel graph diagram may allow more of taa  se   s t  t sag s ton. However, the deleted vertices cannot nullify the adjacency of remaining pairs of vertices that were adjacent in the original diagram. This proves the following result, useful in a later theorem.

LEMMA 6. Let G′ = (V',E') be any subgraph of the Gabriel graph G = (V,E). Then there exists a Gabriel graph G* = (V',E*) on V' with *3C.3.

A graph Kn on n ≥ 1 vertices having all possible edges is a complete graph.

LEMMA 7. The complete graph K is a Gabriel graph only for n = 1, 2, and 3.

Proof. The complete graphs K1 = · , K2 =  , and K3= △ are clearly Gabriel graphs. By lemma 6, if Kn is a Gabriel graph for any n ≥ 4, then K4 is also a Gabriel graph. But K4 is identical as a graph to the wheel W4 shown in Figure 4a, and by lemma 5 is not a Gabriel graph. This contradiction establishes that K is not a Gabriel graph for any n ≥ 4.

A complete bipartite graph Km,n has vertex set V = A∪B, A∩B = ∅, where A contains m vertices, B contains n vertices, and each of the mn edges of Km,n joins a unique vertex of A with a unique vertex of B. Note that a complete bipartite graph has every vertex in part A adjacent to every vertex in part B (and no edge between any two vertices of A or between any two vertices of B), and is not to be confused with a complete graph, where every pair of vertices is adjacent.

LEMMA 8. The only complete bipartite Gabriel graphs are K1,n for 1 ≤ n ≤ 4 and K2,2.

p  =   =   =  =  lt   nd K2,2 = are clearly Gabriel graphs. Now assume Ki,j is a Ġabriel graph for some i ≥ 2, j ≥ 3. By Euler's formula, a Gabriel graph diagram of ·Kij must have ij − (i+j) + 1 interior faces. Now there are i(i − 1)/2 × j(j − 1)/2 distinct ways of choosing 2 members of the i-vertex set and 2 members of the j-vertex set, each choice yielding a chordless 4-cycle of Ki which must bound an interior face in any Gabriel graph diagram of Kij by corollary 3.1. Since i ≥ 2, j ≥ 3, then

$$i \left ( i - 1 \right ) / 2 \times j ( j - 1 ) / 2 > \left \langle i - 1 \right \rangle \left ( j - 1 \right ) = i j - \left \langle i + j \right \rangle + 1 ,$$

a contradiction. Hence Kij is not a Gabriel graph for i ≥ 2, j ≥ 3.

Assume a Gabriel graph diagram exists for K1,n with vertex a adjacent to all n ≥ 5 vertices of B = {b1,b2, . . .,bn}. Assume the vertices of B are labeled in the order encountered by a ray rotating 360° around the origin point a in the

15384632, 1980, 3, Downloaded from https://onlinelibrary.wiley.com/doi/10.1111/j.1538-4632.1980.tb00031.x by Cochrane Mexico, Wiley Online Library on [02/06/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License plane (see Fig. 5). The order must be strict since no two vertices of B could both be on the same ray from a and each be least squares adjacent to a. For n ≥ 5 at least one angle, say angle (biabi+ 1), is strictly less than 90°. Also angle (abibi+ 1) ah   s  a   a s l l (   th diameter bb+1 is contained in the union of the circles with diameters abi and ab+1 and the area in the wedge between the rays abi and ab+1. Since no other point of V falls in this area, bi and b+1 are least squares adjacent by lemma 1, a contradiction. Thus K1,n is not a Gabriel graph for n ≥ 5.


<!-- p:10 -->


Kuratowski's famous characterization theorem (see [9, p. 109]) states that a graph is planar iff it has no subgraph homeomorphic to K5 or K3,3. The definition of homeomorphic subsumes the notion of isomorphic, so a planar graph can have no subgraph of the type K5 or K3,3. Although we cannot fashion a characterization theorem for Gabriel graphs using the concept of "homeomorphic," we prove the following showing that Gabriel graphs are more restrictive than general planar graphs regarding complete subgraphs and complete bipartite subgraphs.

THEOREM 4. A Gabriel graph has no subgraph isomorphic to K4 or K2,3.

Proof. Lemmas 6 and 7 imply that K4 cannot be a subgraph of any Gabriel graph. Suppose a Gabriel graph G′ has vertices a1,a2, b1,b2, b3, with ai adjacent to bj for 1 ≤ i ≤ 2, 1 ≤ j ≤ 3. In the Gabriel graph diagram, at least two points of {b1,b2, b3} must be on the same side of the ray through a1a2 as shown in Figure 6. Now bi, cannot be in triangle a1a2bi, since either angle a1bi bi, or angle bibi,a2 would be ≥ 90°, and similarly bi2 cannot be in triangle a1azbi, so the dotted line bibi, must fall outside both triangles. But then the four points a1,a2,bi,bi have a convex hull which is a quadrilateral and the diagonals cross over. But the diagonals are edges of G' and cannot cross over. This contradiction establishes that K2,3 cannot be a subgraph of any Gabriel graph.

FIG. 5. Proof that K1,n Is Not a Gabriel Graph for n ≥ 5

FIG. 6. Proof that K2,3 Cannot Be a Subgraph of Any Gabriel Graph

n   l  o i t s n s   ly pairwise adjacent in any Gabriel graph; and (ii) no two vertices may each be adjacent to the same set of three other vertices in any Gabriel graph.

It was noted in theorem 1 that the Gabriel graph G(V) will contain all shortest spanning trees on the vertex set V. To better understand the similarities and distinctions between the utilization of shortest spanning trees and Gabriel graphs in applications, it is instructive to determine properties associated with the case where the methods yield the same result, i.e., where the Gabriel graph is identical to a unique shortest spanning tree.

THEOREM 5. Any tree of maximum degree 3 is a Gabriel graph.

Proof. Consider the tree diagram formed recursively as follows. Three edges emanate from the root vertex r at 120° angles to each other and extend a unit distance to three other vertices u,v,w, termed the first generation vertices. At

15384632, 1980, 3, Downloaded from https://onlinelibrary.wiley.com/doi/10.1111/j.1538-4632.1980.tb00031.x by Cochrane Mexico, Wiley Online Library on [02/06/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License the end of each path from the root to an nth generation vertex, n ≥ 1, two new edges, each one with one-sixth the length of the previous edge, are joined at angles 120° with the previous edge and they lead to (n + 1)th generation vertices. This construction is shown through the third generation in Figure 7. The construction assures that further generations will yield vertices restricted to the Gr  ra x xl y  b  i y s sr albr. through v, cannot be adjacent to r, since angle (rvx) &gt; 90°. Any two vertices x,y of the tree, reachable in different directions from r, cannot be adjacent, since angle (xry) &gt; 90°. By the similarity of construction of the other generations, the Gabriel graph for such a positioning of vertices through n generations will be a tree where vertices of generation 0 through n-1 have degree three and vertices at the nth generation level are the terminal vertices of degree unity.


<!-- p:11 -->


FIG. 7. A Tree with all Nonterminal Vertices of Degree Three that Is a Gabriel Graph.

Our previous arguments also confirm that deletion of branches of the tree formed by this construction cannot result in any remaining pair of vertices becoming least squares adjacent that were not previously adjacent. Thus every subtree of each such nth generation tree is a Gabriel graph for all n. Since any tree with all vertices of degree at most 3 is a subtree of such a tree for some generation, the theorem is obtained.

Although a tree such as K1,4 =  with a vertex of degree 4 can be a Gabriel graph, it appears that no tree withtwo adjacent vertices of degree 4 or with a vertex of degree greater than or equal to 5 can be a Gabriel graph. We prove a slightly weaker result.

THEOREM 6. Any tree having a vertex of degree greater than or equal to six is not a Gabriel graph.

Proof. Let V be a set of vertex points in the plane such that the Gabriel graph

15384632, 1980, 3, Downloaded from https://onlinelibrary.wiley.com/doi/10.1111/j.1538-4632.1980.tb00031.x by Cochrane Mexico, Wiley Online Library on [02/06/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License G(V) is a tree with r e V having a degree of at least six. Then in the Gabriel graph diagram for G(V), the vertex r must have two vertices x,y ∈ V, both adjacent to r with d(r,x) ≤ d(r,y) where angle (xry) ≤ 60°. Since the sides of any triangle have lengths proportional to the size of the opposite angles, it follows that d(x,y) ≤ d(r,y).


<!-- p:12 -->


By theorem 1, G(V) must contain all shortest spanning trees for the distance matrix D on V. Since G(V) is itself a tree, it is the unique shortest spanning tree. But the tree formed from G(V) by deleting edge ry and adding edge xy has a sum of distances no greater than that of G(V), a contradiction. Hence no tree having a vertex of degree greater than or equal to six can be a Gabriel graph.

## 5. EDGE DENSITY OF GABRIEL GRAPHS

A Gabriel graph must have enough edges to contain a spanning tree but can have no greater edge density than any planar graph. From well-known properties of trees and planar graphs [9], any Gabriel graph on n vertices must have an edge-to-vertex ratio of no less than 1 – (1/n) and no greater than 3.

The edge-to-vertex ratio is also directly related to the average size of the face boundaries for a Gabriel graph. Letting a = (Number Edges/Number Vertices), with the average size of all face boundaries including the exterior face given by b = [2 (Number Edges)/Number Faces], it follows from Euler's formula (see (2) and increment by unity to count the exterior face) that

The edge-to-vertex ratio is significant for the storage requirements implicit in computerized clustering and regionalization procedures. A problem involving 5,000 localities in a geographical study would require 12.5 million entries to store just one-half of the symmetric distance matrix and therefore be intractable even on a large computer. However, there are no more than 15,000 least squares adjacent pairs of localities for such a problem. If the relevant information for the geographical problem can be associated with the 5,000 localities and the (at most) 15,000 pairs of adjacent localities in an appropriate data structure, then storage of the data becomes feasible in typical computer memories.

$$b = \frac { 2 a } { ( a \, - \, 1 \, + \, \sqrt { 2 / N u m b e r \ V e r t i c e s } ) } \ .$$

$$\frac { ( 3 ) } { \text {tices} ] } \cdot$$

It then follows from (3) that when the edge-to-vertex ratio is near the lower limit of 1 - (1/Number Vertices), the face boundary size is large as in the case of a -sn e ae e e ae se ae --e  e e e s ary size is near four, and if the edge-to-vertex ratio is near the upper limit of three, then the average face boundary is near three, so the graph is nearly triangulated.

Gabriel graph diagrams realizing close to the extremes of edge density variation can be achieved by certain regular placements of points in the plane. A sequence of colinear points, such as in Figure 8a, yields a Gabriel graph that is a simple path and, thus, achieves the minimum edge-to-vertex ratio for Gabriel graphs. A path may also be obtained if the points are nearly colinear as, for example, the Gabriel graph on vertices {1,48,40,3,50,4,47} of Figure 1. Placing points at the Cartesian grid points of an n × n square in the plane yields a Gabriel graph with 2n (n + 1) edges, (n + 1)2 vertices and n2 square interior faces as shown for n = 4 in Figure 8b. The edge-to-vertex ratio is near two and the face boundary size averages near four in this case. Placing points at triangular grid points in the plane bounded by a hexagon with n points on each side yields a

15384632, 1980, 3, Downloaded from https://onlinelibrary.wiley.com/doi/10.1111/j.1538-4632.1980.tb00031.x by Cochrane Mexico, Wiley Online Library on [02/06/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License Gabriel graph with 9n2 – 15n + 6 edges, 3n2 –3n + 1 vertices, and 6(n – 1)2 triangular interior faces, as shown for n = 4 in Figure 8c. The edge-to-vertex ratio is 3 -[(6n − 3)/(3n2— 3n + 1)] in this case, which approaches asymptotically the maximum edge-to-vertex ratio of three. The boundaries are alì 3-cycles except for the exterior face. Furthermore, since hexagons are the regular polygons that allow the greatest amount of packing into an area [8], this suggests that certain regular Gabriel graph diagrams are potentially efficient in filling space.


<!-- p:13 -->


D

b

FıG. 8. Several Gabriel Graph Diagrams Resulting from Regular Vertex Spacings in the Plane

A measure of planar network structure given in [8, p. 32; 14] and used by Gabriel and Sokal [6] is defined for any connected planar graph G with at least three vertices by

$$\alpha ( G ) = \frac { \text {Number Edges } - \text {Number Vertices } + 1 } { 2 \left ( \text {Number Vertices} \right ) - 5 } \, .$$

From Euler's polyhedron formula it is recognized that this ratio is simply the number of interior faces divided by the maximum number of interior faces in a planar connected graph on as many vertices. Thus we term this ratio the planar face density α(G) for any planar graph G with at least three vertices, and note the alternative formula

$$\alpha ( G ) = \frac { \text {Number Interior Faces in a Diagram of $G$ on $n$ Vertices} } { \max { \text {Maximum Number Interior Faces in Any Planar Graph on $n$ Vertices} } } \ . \ ( 5 )$$

Note that 0 ≤ α(G) ≤ 1, with α = 0 for G a tree, and α = 1 if G is a fully triangulated planar graph on n vertices for any n ≥ 3. For the Gabriel graphs of Figure 8a, 8b, and 8c, note that α = 0, α = 16/45, and α = 54/69, respectively.

It is of interest to investigate the structure of those Gabriel graphs that achieve maximum edge density (and corresponding maximum α (G) from (4)) for a specific number of vertices, n, including small values of n where the asymptotic results are not instructive. A maximal planar graph on n vertices is defined [9] as a planar graph to which no edge can be added without losing planarity. Similarly, let a maximal Gabriel graph on n vertices be a Gabriel graph with a maximum number of edges for n vertices. Maximal planar graphs for n = 1, 2, and 3 are K1 = ·, K2 =, and K3 = △ respectively, and these are also maximal Gabriel graphs. For n = 4 the maximal Grabiel graph  has one less edge than the maximal planar graph K4 =  . For n ≥ 5, a maximal planar graph has 3n - 6 edges [9, p. 104]. It is now shown that a maximal Gabriel graph always has at least two less but no more than three less edges than a maximal planar graph for any n ≥ 5, hence α(G) can be arbitrarily close, but not equal, to unity for appropriately large n.

15384632, 1980, 3, Downloaded from https://onlinelibrary.wiley.com/doi/10.1111/j.1538-4632.1980.tb00031.x by Cochrane Mexico, Wiley Online Library on [02/06/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License THEOREM 7. A maximal Gabriel graph has exactly 3n-8 edges for n = 5m + 1 for any m ≥ 1, and either 3n-8 or 3n-9 edges for all n ≥ 5.


<!-- p:14 -->


Proof. We first show that every Gabriel graph has at most 3n-8 edges for n ≥ 5. Let C be the cycle (or closed walk) bounding the exterior face in the Gabriel graph diagram for a maximal Gabriel graph G(V) on n ≥ 5 vertices. If C has a length of 3 or 4, it would have to be a cycle containing other vertices in its interior, contrary to theorem 3. Thus C must have a length of at least 5, so at least two edges can be added to the exterior face and maintain planarity of the n   t s Ss   t n Sa u S  s us Strs Gabriel graph on n ≥ 5 vertices can have at most 3n-8 edges.

We now show that this bound is tight when n = 5m + 1 for m ≥ 1. Let Vn be a set of vertex points in the plane composed of an origin point and m = (n − 1)/5 sets of five equally spaced points on the boundaries of concentric circles, each circle having fve times the diameter of the preceding one, where the successive 5-point sets are 36° out of phase with their predecessors. It is readily verified that G(Vn) has 3n-8 edges, as seen for n = 11 in Figure 9.

FIG. 9. A Maximal Gabriel Graph on 11 Vertices Having (3 × 11) – 8 = 25 Edges and Planar Face Density α = 15/17 = 0.88.

For m ≥ 2, deleting 1 ≤ k ≤ 4 successive points of V5m +1 on the outermost circle yields V*⊂V5m+1 where G(V*) has n=5m+1−k vertices and 3n−9 edges. Finally, for n = 5 note that deleting one outer vertex point from V6 yields a vertex set V' where G(V') has 7 = 3n-8 edges, completing the theorem.

In graph theory there are two popular connectivity measures that are quite often intimately related to the edge density, which leads us to note the following observation.

The vertex-connectivity (edge-connectivity) of a graph is the minimum number of vertices (edges) whose removal either disconnects the graph or leaves the trivial graph (single vertex graph K1 =·). A planar graph has vertexconnectivity, edge-connectivity, and a minimum degree, all of value of at most five [9, pp. 43, 104]. The Gabriel graph of Figure 10 has a vertex-connectivity of 5, edge-connectivity of 5, and a minimum degree of 5, showing these upper bounds on connectivity can be achieved by a planar graph that is a Gabriel graph. Utilizing Menger's theorem [9, pp. 47–49], we may conclude that every

15384632, 1980, 3, Downloaded from https://onlinelibrary.wiley.com/doi/10.1111/j.1538-4632.1980.tb00031.x by Cochrane Mexico, Wiley Online Library on [02/06/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License pair of vertices of Figure 10 then has 5 disjoint paths joining those vertices, which provides considerably greater interconnection capability than the single path always obtained with the shortest spanning tree.


<!-- p:15 -->


FiG. 10. A Maximal Gabriel Graph on 21 Vertices with Vertex-Connectivity, Edge-Connectivity, and Minimum Degreę All Equal to Five.

Returning to the investigation of edge density, note that the examples of minimum and maximum edge-to-vertex ratios in Gabriel graphs in Figures 8a and 9 utilized very special vertex location patterns. The Gabriel graph of Figure 1 resulting from an actual application has edge density sufficiently different from either of these extremes. "In order to understand typical or "average" behavior of the edge-to-vertex ratio, it is of value to consider the properties of the Gabriel graphs generated by the uniform random placement of n vertices in the unit square. It is to be expected that the vertices forming the boundary of the exterior face will have somewhat different properties than those interior to the Gabriel graph diagram. The following theorem addresses a particular vertex v removed from the boundary of the unit square. We show for sufficiently large n, making it then probable that v is not on the boundary of the exterior face of the resulting Ga  at se   e t t Da e ast squares adjacent to v approaches four.

THEOREM 8. Let G be the Gabriel graph formed on n ≥ 3 vertices that are placed in a uniformly random manner on the unit square. Let a particular point v of G be at distance α &gt; 0 from the closest boundary of the unit square. Then the expected degree of v in G, denoted E(deg(v)), satisfies

$$4 - 4 \left ( 1 - \frac { \pi \alpha ^ { 2 } } { 4 } \right ) ^ { n - 1 } \leqslant E ( \deg ( v ) ) \leqslant 4 + 8 \left ( 1 - \frac { \pi \alpha ^ { 2 } } { 8 } \right ) ^ { n - 1 } ,$$

so for any α &gt; 0,

$$\lim _ { n \to \infty } E ( \deg ( v ) ) \, = \, 4 \, .$$

Proof. Given a vertex v with closest distance α to the boundary of the unit square, we first determine the probability that another particular vertex w is

15384632, 1980, 3, Downloaded from https://onlinelibrary.wiley.com/doi/10.1111/j.1538-4632.1980.tb00031.x by Cochrane Mexico, Wiley Online Library on [02/06/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License least squares adjacent to v. For d(v,w) = x ≤ α, note that the probability density that w lies at distance x from v is 2πx dx. Then the probability that all other n − 2 vertices lie outside the circle with diameter arc vw is [1 − (πx2/4)]n−2 so


<!-- p:16 -->


$$\text {Prob} \{ w \text { is an edge and } d ( v , w ) \leq \alpha \} & = \int ^ { \alpha } \left ( 1 - \frac { \pi x ^ { 2 } } { 4 } \right ) ^ { n - 2 } 2 \pi x \, d x \\ & = \frac { 4 } { n - 1 } \left ( 1 - \left ( 1 - \frac { \pi \alpha ^ { 2 } } { 4 } \right ) ^ { n - 1 } \right ) .$$

Since E(deg(v)) = (n − 1) Prob {vw is an edge}, the lower bound of (6) is obtained. For the upper bound in (6) we need an upper bound on Prob {vw is an edge, d(v,w) &gt; α}. For x &gt; α, at least one-half of the circle with diameter arc vw falls in the unit square, and since x &lt; √2,

$$\text {Prob} \left \{ w \text { is an edge and } d ( v , w ) > \alpha \right \} & < \int _ { \alpha } ^ { \vee _ { 2 } } \left ( 1 - \frac { \pi x ^ { 2 } } { 8 } \right ) ^ { n - 2 } 2 \pi x \, d x \\ & < \frac { 8 } { n - 1 } \left ( 1 - \frac { \pi \alpha ^ { 2 } } { 8 } \right ) ^ { n - 1 } ,$$

which then yields the upper bound in (6). Equation (7) follows immediately from (6).

The bounds in (6) are not the sharpest possible but they are adequate for reasonably large n. For example, (i) n = 500, α = 0.15, yields 3.999 ≤ E(deg(v)) ≤ 4.096; and (ii) n = 500, α = 0.20, yields 3.999 ≤ E(deg(v)) ≤ 4.003.

It is readily obtained that as the number of vertices increases, the average degree for a shortest spanning tree approaches two and the average degree of the Delaunay triangulation approaches six (since that graph is maximal planar, except for the exterior region, with probability one). Hence the average edge density of Gabriel graphs is about midway between that of two popular alternative approaches.

From theorem 8 we may then infer that an average interior vertex in a random Gabriel graph will have about four other vertices to which it is least squares adjacent, and by equation (3) the average face boundary size should then be near four. The average behavior is thus closer in edge density to the Cartesian grid of Figure 8b rather than the denser triangulation exhibited in Figure 8c.

## 6. CONCLUSIONS

Several of the properties described in this paper can be used for the computational and visual inspection of connectivity graphs to determine whether they are least squares connected in the plane, i.e., Gabriel-connected. Knowing that no vertices can be found within a three or four cycle and that n-cycles (n ≥ 3) and wheels Wn (n ≥ 6) are Gabriel-connected will help in this context. For those connectivity matrices that are minimally connected, i.e., a tree, it is useful to know that if the maximum degree of any vertex is 3, then appropriate placement of vertices in the plane will make that tree a Gabriel graph. Trees with vertices of degree ≥ 6 cannot be Gabriel graphs.

As sampling stations are deleted from a map on which a Gabriel graph has been drawn, it is useful to know both algorithmically and in terms of the model

15384632, 1980, 3, Downloaded from https://onlinelibrary.wiley.com/doi/10.1111/j.1538-4632.1980.tb00031.x by Cochrane Mexico, Wiley Online Library on [02/06/2026]. See the Terms and Conditions (https://onlinelibrary.wiley.com/terms-and-conditions) on Wiley Online Library for rules of use; OA articles are governed by the applicable Creative Commons License that earlier adjacencies between the points will be retained and that the residual edges can be embedded in a Gabriel graph. Since the maximum number of edges in a Gabriel graph is very close to the maximum of a planar graph, it is relatively quite densely connected, although connectivity networks at or near the maximum will require peculiar configurations of vertices unlikely to be achieved in real sampling situations. But on the average a Gabriel graph will be twice as edge dense as a spanning tree. If an actual sampling scheme of localities is relatively sparsely packed, then it will reflect a curious sampling pattern (e.g., linear transects, rings) or physical properties of the terrain being sampled, such as barriers which wilì result in peculiar edge-sparse structures. Thus low edge density can be used as a measure of the interconnectedness of the graph.


<!-- p:17 -->
