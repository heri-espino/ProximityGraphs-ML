---
id: "Toussaint_1980_Relative-Neighborhood-Graph"
source_pdf: "../pdf/Toussaint_1980_Relative-Neighborhood-Graph.pdf"
source_filename: "Toussaint_1980_Relative-Neighborhood-Graph.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "excellent"
extraction_score: 106.0
visual_assets: "disabled"
references_file: "../references/Toussaint_1980_Relative-Neighborhood-Graph.references.md"
---

<!-- p:1 -->

## THE RELATIVE NEIGHBOURHOOD GRAPH OF A FINITE PLANAR SET

GODFRIED T. TOUSSAINT School of Computer Science, McGill University, Montreal, Canada

(Received 21 September 1979)

Abstract – The relative neighbourhood graph (RNG) of a set of n points on the plane is defined. The ability of the RNG to extract a perceptually meaningful structure from the set of points is briefly discussed and compared to that of two other graph structures: the minimal spanning tree (MST) and the Delaunay (Voronoi) triangulation (DT). It is shown that the RNG is a superset of the MST and a subset of the DT. Two algorithms for obtaining the RNG of n points on the plane are presented. One algorithm runs in O(n2) time and the other runs in O(n3) time but works also for the d-dimensional case. Finally, several open problems concerning the RNG in several areas such as geometric complexity, computational perception, and geometric probability, are outlined.

Dil onlionln s ino r ion Dot patterns Computational perception Pattern recognition Algorithms Geometric complexity Geometric probability

CR Categories: 3.36 3.63 5.25 5.32 5.5

## 1. INTRODUCTION

In many problems in pattern recognition, such as clustering(1) and computational approaches to perception,(2) one is given a set of points on the plane and it is desired to find some structure among the points in the form of edges connecting a subset of the pairs of points. In the clustering problem we would like to have an algorithm that joins two points if the two points belong to the same cluster of points.(1) In computational perception we would like an algorithm to join pairs of points such that the final graph obtained is perceptually meaningful in some sense.(2)

Two graphs that we will be concerned with in this paper are the minimal spanning tree (MST) and the Delaunay triangulation (DT). In the minimal spanning tree of a set of points P edges are formed by joining pairs of points to form a tree that spans P such that the sum of the Euclidean edge lengths is less than the sum for any other spanning tree. As an example consider the set of points on the plane in Fig. 1(a). The MST of that set is given in Fig. 1(b). Observation of Fig. 1(b) suggests that the MST is a form of 'skeleton' of the data points. In addition, there is evidence that it has perceptual significance,(1.2) and it has been used extensively as a tool for cluster ánalysis.(1.16)

points can be triangulated in many different ways. Two triangulations of the set of points given in Fig. 1(a) are illustrated in Figs 1(c) and (d). Triangulations have received a lot of attention in the past and have many areas of application.(3) The triangulation we are concerned with here is the Delaunay triangulation, or alternatively the locally equiangular triangulation.(4) To define the Delaunay triangulation we first introduce a structure known as the Voronoi diagram(5) (also Dirichlet tessellation).

Let P = {P1, P2, ... , Pn} denote n distinct points on the plane. The Voronoi diagram partitions the plane into disjoint regions or tiles (also Thiessen polygons) such that the tile of p is the set T defined by

$$T _ { i } = \{ x \colon d ( x , p _ { i } ) < d ( x , p _ { j } ) \ \text { for all } j \neq i \} ,$$

where d denotes Euclidean distance. The Voronoi diagram finds wide application in various fields such as geography(6) and has been used to find elegant and efficient algorithms for many problems in computational geometry by Shamos and Hoey.(7) The Voronoi diagram for the set of points of Fig. 1(a) is given in Fig. 1(e). The Delaunay triangulation is now easily explained. Two points p and p are joined by an edge if, and only if, their corresponding tiles T and T, share a side. If this operation is carried out on the Voronoi diagram of Fig. 1(e) one obtains the Delaunay triangulation illustrated in Fig. 1(f).

A triangulation is more difficult to define formally. A set P, of points in the plane, is triangulated by a subset, T, of the straight line segments whose endpoints are in In this paper we investigate a graph which we call P, if T is a maximal subset such that the line segments the relative neighbourhood graph (RNG) of a finite in T intersect only at their end points. Intuitively, planar set. It is based on the notion of relatively close edges are formed such that as many triangles as neighbours defined by Lankford'8) and has not repossible are created without crossing lines. A set of ceived any attention in the literature on computational


<!-- p:2 -->


·


e·

·


(a) A set of points on the plane.

(b) Minimal spanning tree of points in (a).

(c)

(d)

(e) Voronoi diagram of points in (a).

(f) Delaunay triangulation of points in (a). Fig. 1.

geometry or pattern recognition. The RNG is defined in section 2 and its ability to extract perceptually relevant structures from sets of points is compared to that of the MST and the DT. In section 3 the RNG is related to both the MST and the DT. Two algorithms for finding the RNG, of n points on the plane, are given in section 4. One algorithm runs in O(n3) time while the other requires O(n2) time. Finally, some open problems are discussed in section 5.

## 2. THE RELATIVE NEIGHBOURHOOD GRAPH

Consider again a set P of n distinct points on the plane: P = {P1, P2,..., Pn}. There are many possible ways of defining whether or not two points p and p  are neighbours of each other. Several definitions are considered.(1.2.8.15) Lankford(8 defines two points p and pj as being relatively close' if d(pi,Pj) ≤ max[d(pi, Pk), d(pj, Pk)] for all k = 1, ..., n, k ≠i, j.

(a) A set of points.

(b) Relative neighbourhood graph of points in (a). Fig. 2.

·


<!-- p:3 -->


Actually, Lankford uses &lt;'rather than '≤'in his definition. The difference is essentially that with this minor modification, in a degenerate situation such as three points lying equidistant from each other, all three points are considered relative neighbours of each other, whereas with only &lt;'in the definition none of the three points are relative neighbours of each other. Intuitively, the definition states that two points are relative neighbours if they are at least as close to each other as they are to any other point. The relative neighbourhood graph is obtained by connecting an edge between points p and pj for all i, j = 1, . . . , n, i ≠j if, and only if, p and p, are relative neighbours. Figure 2 illustrates a set of points and its RNG.

It is interesting to compare the perceptual relevance of the RNG to that of the MST and the DT. To this end consider a set of points for which the MST extracts a perceptually relevant structure. Such a set and its MST are illustrated in Fig. 3. Clearly the DT of the set of points of Fig. 3(a) fails as a perceptually meaningful

(a) A set of points on the plane.

(b) Minimal spanning tree of points in (a). Fig. 3. (b) Minimal spanning tree of points in (a). Fig. 3.

●

·


(a) Set of points on the plane.

(b) Delaunay triangulation of points in (a). Fig. 4.

structure. However, we can find sets of points where the reverse is true. Figure 4(a) shows a set of points with its DT in Fig. 4(b). In this case the DT appears to be more perceptually relevant than the MST. However, the RNG works well in both cases: in Fig. 3 the RNG agrees with the MST, and in Fig. 4 the RNG agrees with the DT. It is further possible to find very simple and basic sets of points where both the MST and the DT fail to extract the perceptually relevant structure. A strong case, in fact, for the RNG is a set of four points arranged in a square or rectangular fashion as in Fig. 5(a). Perceptually, the set of points immediately suggests a rectangle.(9)Here both the MST [Fig. 5(b)] and the DT [Fig. 5(c)] fail and only the RNG yields the rectangle. This suggests that the RNG may have more perceptual significance than the MST considered in,(1) at least for arbitrary sets of points. That this is not always the case can be shown by constructing a set of points that have important symbolic meaning such as those in Fig. 6(a) which clearly indicate the letter G'. The MST [Fig. 6(b)] yields a G' but the RNG [Fig. 6(c)] does not. In short, the RNG is more adaptive to the data in the sense that it imposes less structure than either the MST or the DT.

Figures 7, 8, and 9 illustrate further sets of points and their RNGs. Unlike the set of points in Fig. 2 which consists of points in a somewhat arbitrary position, the points in Figs 7, 8, and 9 are more symmetrically arranged. As a result many more tri-


<!-- p:4 -->


·


(a) A set of four points on the plane.

(b) Minimal spanning tree of points in (a).

-

"

(c) Delaunay triangulation of points in (a).

(d) Relative neighbourhood graph of points in (a). Fig. 5.

(a) Set of points on the plane.

@''

(b) Minimal spanning tree of points in (a).

(c) Relative neighbourhood graph of points in (a). Fig. 6.

angles and squares appear. Recall from Figs 3 and 4 that the RNG sometimes behaves like an MST and at other times like a DT. These figures, in particular Fig. 2, suggest that the RNG is a structure 'lying somewhere in between'the MST and the DT. In the next section we show, in fact, that the RNG is a superset of the MST and a subset of the DT.

## 3. TWO THEOREMS CONCERNING THE RNG

Theorem 1. The relative neighbourhood graph is a superset of the minimal spanning tree.

Proof. Consider two points a and b as in Fig. 10. Let R denote the interior of the intersection of the two circles with centres at a and b and let B denote the boundary of R. Let c be a third point in a nondegenerate position, i.e., c ∉ B. (If c lies in B, d(a, b) = d(c, b) or d(c, a) and the MST is non-unique.) Thus c must lie either in R or in Ř, the complement of R  B. If c ∈ R then d(a, c) &lt; d(a, b) and d(b, c) &lt; đ(a, b), and it follows that ab∉ MST. Thus a necessary but not a sufficient condition for ab∈ MST is that all other points lie in R. However, this is a necessary and sufficient condition for ab∈ RNG. Therefore, MST ∈ RNG. Q.E.D.


<!-- p:5 -->


Theorem 2. The relative neighbourhood graph is a subset of the Delaunay triangulation.

Proof. Consider again two arbitrary points a and b from a finite set of points as in Fig. 10. We must show that if ab ∈ RNG then ab ∈ DT. Assume that ab ∈ RNG. It follows from the definition that no other points lie in R. We now ask under what conditions the tiles T. and T of the Voronoi diagram do not share a side. Consider two additional points, say c and d, that lie somewhere on B as in Fig. 11, where the Voronoi diagram is indicated with dashed lines. Observe that the Voronoi lines associated with ca and ad are the perpendicular bisectors of the lines joining ca and ad, respectively. Furthermore, since a, c, and d all lie on a circle with its center at b, it follows that no matter how close c and d are to a, Te and T will always share a side of non-zero length. Furthermore, if either c or d lie in R, the length of the shared side of T. and T6 will tend to increase. Therefore, when no other points lie in R the

(a)

Fig. 8.

tiles T and T always share a side. Therefore ab ∈ DT. Q.E.D.

Let Ne denote the number of edges contained in the RNG of n points on the plane.

Corollary. The number of edges in the RNG of n points on the plane is bounded by n − 1 ≤ Ne ≤ 3n − 6, and is thus O(n).

Proof. By definition, the MST contains n – 1 edges. Since the MST is a subset of the RNG (Theorem 1) it follows that Ne ≥ n — 1, where the equality holds when RNG = MST. It has been shown that a graph without crossings can contain at most 3n — 6 edges and that this bound is achieved when all faces of the graph are triangles.(17) Therefore the DT contains at most 3n – 6 edges. Since the RNG is a subset of the DT (Theorem 2) it follows that N. ≤ 3n —6 where the equality holds when RNG = DT. Thus0(n) ≤ Ne ≤ 0(n) and we have Ne = 0(n).

## 4. TWO ALGORITHMS FOR FINDING THE RNG

Let n points be given by their Cartesian coordinates


<!-- p:6 -->

(a)

(b)

Fig. 9.

P1(x1, y1), P2(x2, y2), . . . , Pn(x, yn). It is required to find their RNG. In this section we give two algorithms for finding the RNG. The first, RNG–1, is the obvious and naïve algorithm which has a complexity of O(n3). The second, RNG–2, uses knowledge from Theorem 2 and has a complexity of O(n2).

### Algorithm RNG—1

Step 1. Compute the distance between all pairs of points d(pi, Pj) i, j = 1, . . . , n, i ≠j.

Sep al (   o o  ol  ax = max{d(pk, Pi), d(Pk, Pj)} for k= 1, ... , n, k≠i, k≠j. Step 3. For each pair of points (p, Pj) search for a

I

Fig. 10.

Fig. 11.

value of dkmax that is smaller than d(p, Pj). If such a point is not found, an edge is formed between p and pj.

Step 1 of this algorithm requires O(n2) operations to yield O(n2) pairs. Furthermore, for each of these pairs steps 2 and 3 each require O(n) operations. Hence the overall complexity of this algorithm is O(n3).

### Algorithm RNG–2

Step 1. Compute the Voronoi diagram of the set of points.

Step 2. Obtain the Delaunay triangulation from the Voronoi diagram.

Step 3. For each pair of points (p, Pj), associated with an edge of the DT, compute dmax = max{d(Pk, Pi), d(pk, Pj)} for k= 1, . .. , n, k≠i, k≠j.

Step 4. Same as Step 3 of algorithm RNG–1, with edges of the DT only.

It is clear that the reason why algorithm RNG-2 requires O(n2) running time is that for each of the O(n) edges of the DT, O(n) points are tested for proximity. It follows that if for each edge of the DT only a small fraction of the points were tested for proximity the algorithm should run faster. Such a modification of algorithm RNG-2 is possible using the cell' or 'bin' approach.(18) First, the region in which the n points lie is divided into a√n×√n grid of n bins and each point is placed' in a bin using the floor function. Thus each bin has a pointer to a list of its points. Each edge of the DT now specifies a small group of cells, as a function of the edge length, which in turn identifies the points to be tested. It is conjectured that for some 'nice' distributions of the points this modification of algorithm RNG–2 will run in O(n) expected time.

The Voronoi diagram (Step 1) can be computed in O(n log n) worst-case running time.(7) Since there are O(n) edges in the Voronoi diagram(") and each yields an edge in its dual, the DT, Step 2 requires O(n) operations. In Step 3, for each pair of points considered, O(n) ope sd (  s p pi  se be investigated this step runs in O(n2) time. Since Step 4 is O(n2) the algorithm's complexity is dominated by Steps 3 and 4 and is thus of O(n2).

An idea that also comes to mind for restricting the number of points tested for each edge of the DT is to test only those points that are Delaunay neighbours of the two vertices of the edge being considered. It is also conjectured that for some 'nice' distributions this algorithm will run in O(n) expected time. Unfortunately the algorithm does not always work. It is easy for the reader to construct an example with five points to convince himself that this algorithm does not yield the RNG. Nevertheless, it can be considered as an approximate algorithm for the RNG.


<!-- p:7 -->


## 5. OPEN PROBLEMS AND CONCLUDING REMARKS

One of the main goals of this paper is to introduce the RNG to the literature on pattern recognition, perception, and computational geometry, and to point out that the RNG opens a host of problems in several areas of research. In this section we will outline some of the more interesting open problems concerning the RNG.

(a) Non-Euclidean case. In this paper we assumed that the weight, associated with an edge of the complete graph of the set of points, was equal to the Euclidean distance between the vertex points of the edge. In general the weights could take on arbitrary values and we would then have a non-Euclidean RNG. Algorithm 1 would still work in this case and thus we have an O(n3) algorithm for the non-Euclidean RNG. It remains an open problem whether we can do better than this.

(b) d-Dimensional case. In this paper only the twodimensional problem was considered. It is clear that algorithm 1 generalizes to the d-dimensional case. Thus we have an O(n3) algorithm for arbitrary fixed dimensions. It is an open question whether we can do better than this in three and higher dimensions.

- (e) In this paper the RNG was related to two other graph structures: the MST and the DT. It would be interesting to find relationships between the RNG and other graph structures such as the minimum weight triangulation and those considered in(2) and(8).
- (f) Another ciass of problems relates to the statistical properties of the RNG. Such problems include: what is the expected number of circuits in the RNG of n points when the n points are randomly chosen from a given distribution? What is the expected area of the largest circuit? What is the expected length of the RNG? Theorem 1 partially answers the last question with the help of existing results for the MST. Let E{MST} and E{RNG} denote the expected length of the MST and RNG, respectively. Gilbert(13) and Roberts14) showed that for n points distributed according to a Poisson process in the unit square, in the limit as n → x, E{MST} = k√n where 0.5 ≤ k ≤ 0.707. From Theorem 1 it follows that E[RNG} ≥ E{MST} and therefore for the Poisson process above E{RNG} ≥ k√n.

(g) The RNG also opens new problems in geometrical probability. In general, if n points are generated randomly according to a given distribution, we can ask

PR 12:4D

what is the probability that a certain event occurs in the RNG of the points. For example, let n = 4. In this case the RNG can assume only a few easily recognizable classes of forms illustrated in Fig. 12: the 'toad', the 'starfish', the'wiggly snake', the 'convex snake', and last and least the degenerate 'kite' (degenerate because this form only occurs when the sides joining the tail have equal length which happens with probability zero.) Are there more 'toads' than 'starfish'?

(h) A final open problem has to do with the (c) Is there an O(n log n) algorithm? Alternatively, relevance of the RNG to the perceptual process. find a lower bound on the problem. Section II suggests that the RNG is a powerful model (d) Several techniques have been found recently for of low-level visual processes involved in the perception making algorithms run in linear expected time.(õ–12) of certain dot patterns. It would be interesting to Can such algorithms be found for the RNG problem? compare the RNG to other structures such as those used in(1) and(2) and to determine its limits as a model of human perceptual mechanisms.

##### SUMMARY

The problem of extracting the perceptually meaningful structure from a dot pattern or finite set of points on the plane is considered. Two relevant graphtheoretical structures are reviewed: the minimal spanning tree (MST) and the Delaunay (Voronoi) triangulation (DT), and their limitations for solving the above problem are illustrated with examples. A graph, termed the relative neighbourhood graph (RNG), based on the notion of relative neighbours proposed by Lankford in a geographical context, is proposed as an improvement to the MST in solving the problem of extracting the perceptually relevant structure from a dot pattern . It is shown that the RNG is a supergraph of the MST and a subgraph of the DT. Two algorithms for obtaining the RNG of n points on the plane are presented. One algorithm runs in O(n2) time and the other runs in O(n3) time but works also for the ddimensional case. Furthermore, a modification is proposed that should make the algorithms run much faster on average, and it is conjectured that for n points drawn randomly and independently from a uniform distribution in the unit square the latter algorithm will run in O(n) time. Finally, several open problems concerning the RNG in several areas such as geometric complexity, computational perception, and geometric probability, are outlined.


<!-- p:8 -->


Acknowledgements – The author is indebted to David Avis and Duncan McCallum for several helpful discussions during the course of this research. Ernesto Correa obtained some of the figures using a CalComp plotter. I am also grateful to Luc Devroye for reading a preliminary version of this paper and for his helpful comments.
