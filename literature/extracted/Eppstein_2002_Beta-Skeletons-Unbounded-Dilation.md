---
id: "Eppstein_2002_Beta-Skeletons-Unbounded-Dilation"
source_pdf: "../pdf/Eppstein_2002_Beta-Skeletons-Unbounded-Dilation.pdf"
source_filename: "Eppstein_2002_Beta-Skeletons-Unbounded-Dilation.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "excellent"
extraction_score: 108.0
visual_assets: "disabled"
references_file: "../references/Eppstein_2002_Beta-Skeletons-Unbounded-Dilation.references.md"
---

<!-- p:1 -->

##### Abstract

A fractal construction shows that, for any β &gt; 0, the β -skeleton of a point set can have arbitrarily large dilation. In particular this applies to the Gabriel graph.  2001 Elsevier Science B.V. All rights reserved.

Keywords: Geometric graphs; Beta-skeleton; Gabriel graph; Dilation; Fractal

## 1. Introduction

Anumber of authors have studied questions of the dilation of various geometric graphs, defined as the maximum ratio between shortest path length and Euclidean distance.

Das and Joseph [5] showed that these constant dilation bounds hold for a wide variety of planar graph construction algorithms, satisfying the following two simple conditions:

For instance, Chew [3] showed that the rectilinear Delaunay triangulation has dilation at most √ 10 and that by placing points around the unit circle, one could find examples for which the Euclidean Delaunay triangulation has dilation arbitrarily close to π/ 2. In the journal version of his paper [4], Chew added a further result, that the graph obtained by Delaunay triangulation for a convex distance function based on an equilateral triangle has dilation at most 2. Chew's conjecture that the Euclidean Delaunay dilation was constant was proved by Dobkin et al. [6], who showed that the Delaunay triangulation has dilation at most φπ where φ is the golden ratio ( 1 + √ 5 )/ 2. Keil and Gutwin [10] further improved this bound to 2 π 3cos (π/ 6 ) ≈ 2 . 42.

E-mail address: eppstein@ics.uci.edu (D. Eppstein).

1 Work supported in part by NSF grant CCR-9258355 and by matching funds from Xerox Corp. Thanks to Marshall Bern for suggesting the problem of β -skeleton dilation.

Computational Geometry 23 (2002) 43-52

### Computational Geometry

Theory and Applications

www.elsevier.com/locate/comgeo

## Beta-skeletons have unbounded dilation

###### David Eppstein 1

Department of Information and Computer Science, University of California, Irvine, CA 92697-3425, USA

Received 4 December 2000; received in revised form 15 March 2001; accepted 12 June 2001

Communicated by D. Dobkin


<!-- p:2 -->


Fig. 1. (a) Diamond property: one of two isosceles triangles on edge is empty. (b) Graph violating good polygon property: ratio of diagonal to boundary path is high.

- Diamond property . There is some angle α &lt; π , such that for any edge e in a graph constructed by the algorithm, one of the two isosceles triangles with e as a base and with apex angle α contains no other site. This property gets its name because the two triangles together form a diamond shape, depicted in Fig. 1(a).
- Good polygon property. There is some constant d such that for each face f of a graph constructed by the algorithm, and any two sites u , v that are visible to each other across the face, one of the two paths around f from u to v has dilation at most d . Fig. 1(b) depicts a graph violating the good polygon property.

Intuitively, if one tries to connect two vertices by a path in a graph that passes near the straight line segment between the two, there are two natural types of obstacle one encounters. The line segment one is following may cross an edge of the graph, or a face of the graph; in either case the path must go around these obstacles. The two properties above imply that neither type of detour can force the dilation of the pair of vertices to be high.

For a survey of further results on dilation, see [7]. Our interest here is in another geometric graph, the β - skeletons [11,13], which have been of recent interest for their use in finding edges guaranteed to take part in the minimum weight triangulation [2,9,14,15] and in curve reconstruction [1]. As a special case, β = 1 gives the Gabriel graph , a subgraph of the Delaunay triangulation and the relative neighborhood graph, and a supergraph of the minimum spanning tree. These graphs have a definition (given below) closely related to Das and Joseph's diamond property. The value β is a parameter that can be taken arbitrarily close to zero; for any point set, as β approaches zero, more and more edges are added to the β - skeleton until eventually one forms the complete graph. Therefore it seems reasonable to guess that, for sufficiently small β , the β -skeleton should have bounded dilation. Such a result would also fit well with Kirkpatrick and Radke's motivation for introducing β -skeletons in the study of 'empirical networks': problems such as modeling the probability of the existence of a road between cities [11].

In this paper, we show that this is surprisingly not the case. For any β , we find point sets for which the β -skeleton has arbitrarily high dilation. Our construction uses fractal curves closely related to the Koch snowflake. We show that the point set can be chosen in such a way that the β -skeleton forms a path with this fractal shape; the fact that the curve has a fractal dimension greater than one then implies that the graph shortest path between its endpoints has unbounded length.


<!-- p:3 -->


## 2. Beta-skeletons

The β -skeleton [11,13] of a set of points is a graph, defined to contain exactly those edges ab such that no point c forms an angle acb greater than sin - 1 1 /β (if β &gt; 1) or π - sin - 1 β (if β &lt; 1).

Equivalently, if β &gt; 1, the β -skeleton can be defined in terms of the union U of two circles, each having ab as a chord and having diameter β d(a,b) . Edge ab is included in this graph exactly when U contains no points other than a and b .

If β = 1, an edge ab is included in the β -skeleton exactly when the circle having ab as diameter contains no points other than a and b . The 1-skeleton is also known as the Gabriel graph [8].

If 0 &lt;β &lt; 1, there is a similar definition in terms of the intersection I of two circles, each having ab as a chord and having diameter d(a,b)/β . Edge ab is included in the β -skeleton exactly when I contains no points other than a and b .

Fig. 2 depicts these regions for β = √ 2 (union of circles), β = 1 (single circle), and β = 1 / √ 2 (intersection of circles).

As noted above, β -skeletons were originally introduced for analyzing empirical networks. Gabriel graphs and β -skeletons have many other applications in computational morphology (combinatorial methods of representating shapes). Gabriel graphs can also be used to construct minimum spanning trees, since the gabriel graph contains the MST as a subgraph. More recently, various researchers have shown that β -skeletons (for certain values of β &gt; 1) form subgraphs of the minimum weight triangulation [2,9,15].

Su and Chang [12] have described a generalization of Gabriel graphs, the k -Gabriel graphs, in which an edge is present if its diameter circle contains at most k - 1 other points. One can similarly generalize β -skeletons to k - β -skeletons. Our results can be made to hold as well for these generalizations as for the original graph classes.

## 3. Fractals and dilation

Our construction showing that beta-skeletons have unbounded dilation consists of a fractal curve with a recursive definition similar to that of a Koch snowflake. For a given angle θ &lt; π/ 2 define the polygonal path P(θ, 1 ) , by following a path of five equal-length line segments: one horizontal, one at angle θ to the horizontal, a second horizontal, a segment at angle - θ to the horizontal, and a third horizontal.

Fig. 2. Empty regions for √ 2-skeleton, Gabriel graph, and 1 / √ 2-skeleton.

<!-- p:4 -->


Fig. 3. Fractal curves P(π/ 4 , k) for k = 1 , 2 , 3.

Wethen more generally define the graph P(θ,k) to be a path of 5 k line segments, formed by replacing the five segments of P(θ, 1 ) with congruent copies of P(θ,k - 1 ) , scaled so that the two endpoints of the path are at distance one from each other. Fig. 3 shows three levels of this construction. In the drawing of Fig. 3, the orientations of the five copies of P(θ,k - 1 ) alternate along the overall path, so that the horizontal copies are in the same orientation as the overall path and the other two copies are close to upside-down, but this choice of orientation is not essential to our construction.

Note that, if we denote the length of P(θ,k) by lk = lk(θ) , then l 1 &gt; 1 and lk = l k 1 .

Lemma 1. P(θ,k) is contained within a diamond shape having the endpoints of the path as its diagonal, and with angle θ at those two corners of the diamond.

Proof. This follows by induction, as shown in Fig. 4, since the five such diamonds containing the five copies of P(θ,k - 1 ) fi t within the larger diamond defined by the lemma. ✷

Lemma 2. If θ ⩽ ( sin - 1 β)/ 2 and β ⩽ 1 , then P(θ,k) is the β -skeleton of its vertices.

Proof. We show that, if a and b are non-adjacent vertices in the path, then there is some c forming an angle of at least π - sin - 1 β . We can assume that a and b are in different copies of P(θ,k - 1 ) , since otherwise the result would hold by induction. But no matter where one places two points in different copies of the small diamonds containing the copies of P(θ,k - 1 ) (depicted in Fig. 4), we can choose one of the three interior vertices of P(θ, 1 ) as the third point c forming an angle acb ⩾ π - 2 θ . The result follows from the assumed inequality relating θ to β . Thus, the β -skeleton can contain no edges other than those of P(θ,k) .

Conversely, if ab is an edge of P(θ,k) for θ &lt; π/ 2, then the diameter circle of ab is empty and ab is also an edge of the β -skeleton. ✷


<!-- p:5 -->


Fig. 4. Fractal curve is contained in a diamond.

For instance, the graphs P(π/ 4 , k) depicted in Fig. 3 are Gabriel graphs of their vertices. A more careful analysis shows that larger values of θ can still result in a β -skeleton: if the orientations of the copies of P(θ,k - 1 ) that form P(θ,k) are chosen carefully, P(θ,k) is contained in only half the diamond of Lemma 1, and angle acb in the proof above can be shown to be ⩾ π - 3 θ/ 2.

Theorem 1. For any β &gt; 0 there is a c &gt; 0 such that β -skeletons of n -point sets have dilation Omega1 (n c ) .

Proof. We have seen that we can choose a θ such that the graphs P(θ,k) are β -skeletons. Since the endpoints of the path are at distance one from each other, the dilation of P(θ,k) is lk = l k 1 . Each such graph has n = 5 k + 1 vertices and dilation l k 1 = n log 5 l 1 - o ( 1 ) . Since l 1 &gt; 1, log 5 l 1 &gt; 0. ✷

## 4. Upper bounds

Wehave shown a lower bound of Omega1 (n c ) for the dilation of β -skeletons, where c is a constant depending on β , and approaching zero as β approaches zero. This behavior of having length a fractional power of n is characteristic of fractal curves; is it inherent in β -skeletons or an artifact of our fractal construction? We now show the former by proving an upper bound on dilation of the same form.

To do this, we define an algorithm for finding short paths in β -skeletons. As a first start towards such an algorithm, we use the following simple recursion: to find a path from s to t , test whether edge st exists in the β -skeleton. If so, use that edge as path. If not, some r forms a large angle srt ; concatenate the results of recursively finding paths from s to r and r to t .

For β ⩽ 1, sr and rt are shorter than st , so this algorithm always terminates; we assume throughout the rest of the section that β ⩽ 1. We can represent the path it finds as a tree of triangles (Fig. 5), all having an angle of at least π - sin - 1 β . The tree is rooted at triangle srt , with left subtree formed by the recursive call to find a path from s to r and right subtree formed by the recursive call to find a path from r to t . The hypotenuse of each triangle in this tree is equal to one of the two shorter sides of its parent. Note that the triangles may overlap geometrically, or even coincide - we will later describe a procedure for pruning the path found by this procedure to eliminate repeated nodes, while still allowing the tree structure of the triangles to be used in analyzing the path's length. For any similarly defined tree of triangles, we define the boundary length of the tree to be the following formula:

$$| T | = \text {dist} ( s , t ) + \sum _ { \Delta \in T } ( \text {pern} ( \Delta ) - 2 \cdot \text {hypotense} ( \Delta ) ) .$$


<!-- p:6 -->


Fig. 5. Tree of triangles formed by recursive path-finding procedure, and the corresponding abstract tree.

In other words, we sum the lengths of all the short sides of the triangles, and subtract the lengths of all non-root hypotenuses. If the tree forms a non-self-intersecting polygon, such as the one shown in the figure, this is distance from s to t 'the long way' around the polygon's perimeter. We also define an apex of a leaf triangle in such a tree to be the triangle vertex nonadjacent to the leaf's parent, and an apex of the tree to be any apex of any of its leaves.

Lemma 3. For the tree defined by the algorithm above, | T | is the length of the path constructed by the algorithm.

Proof. This can be shown by induction using the fact that the path from s to t is formed by concatenating the paths from s to r and r to t . ✷

Our bound will depend on the number of leaves in the tree produced above. However, this number may be very large, larger than n , because the same vertex of our input point set may be involved in triangles in many unrelated parts of the tree. Our first step is to prune the tree to produce one that still corresponds in a sense to a path in the β -skeleton, but with a good bound on the number of leaves.

Lemma 4. For any β ⩽ 1 , we can find a tree like the one described above, with at most 2 n leaves, for which | T | is at least as large as the length of some path in the β -skeleton from s to t .

Proof. Define a 'leaf vertex' to be the vertex opposite the hypotenuse of a leaf triangle in T . We prune the tree one step at a time until each vertex appears at most twice as a leaf vertex, while maintaining a path in the β -skeleton corresponding to the pruned tree. As we progress, we maintain the invariant that the path we find has as its edges a subsequence of the edges occurring in the leaf triangles of T , so that the path length will always be bounded by | T | . Further, we maintain invariant that this subsequence includes all apexes of T .

Suppose some vertex v appears two or more times as an apex of T , and that there is at least one other leaf of T occurring between the first and last occurrences of T . Then we prune T by removing all subtrees descending from the path between the first and last appearance of v (occurring between the two appearences in tree order), and we shorten the corresponding path by removing the portion of it between these two appearances of v . This clearly preserves the invariants described above. Fig. 6 depicts this pruning process.


<!-- p:7 -->


Fig. 6. Pruning the tree of triangles: removal of leaves between repeated apexes, and simplification of the corresponding path.

Fig. 7. Making single-leaf tree longer: subdivide triangles, increase angles, add children.

Since each step reduces the number of leaves in the tree, we must eventually terminate, at which point each vertex can appear at most twice as an apex. ✷

We use induction on the number of leaves to prove bounds on | T | . The following lemma forms the base case.

Lemma 5. Let T be a tree of triangles, all having an angle of at least θ &gt; π/ 2 opposite the edge connecting to the parent in the tree, with exactly one leaf triangle, and scaled so that the hypotenuse of the root triangle has length 1 . Then | T | ⩽ - 1 / cos θ .

Proof. Since | T | does not depend on the ordering of tree nodes, we can assume without loss of generality that each node's child is on the left. For any such tree, we can increase | T | by performing a sequence of the following steps: (1) If any triangle has an angle greater than θ , change it to one having an angle exactly equal to θ , without changing any other triangle shapes. (2) If any triangle has a ratio of right to left side lengths less than some value C , split it into two triangles by adding a vertex on the right side. (3) Add a child to the leaf of T . These steps are depicted in Fig. 7.


<!-- p:8 -->


Fig. 8. Logarithmic spiral formed by keeping fixed angle to destination point.

The result of this sequence of transformations is the concatenation of many triangles with angles equal to θ , very short left sides, and right sides with length close to that of the hypotenuse. In the limit we get a curve from s to t formed by moving in a direction forming an angle π - θ to t , namely the logarithmic spiral (Fig. 8). Integrating the distance traveled on this spiral against the amount by which the distance to t is reduced shows that it has the length formula claimed in the lemma. Since we reach this limit by a monotonically increasing sequence of tree lengths, starting with any finite one-leaf tree, any finite tree must have length less than this limit. ✷

More generally, we have the following result.

Lemma 6. Let T be a tree of triangles, all having an angle of at least θ &gt; π/ 2 opposite the edge connecting to the parent in the tree, with k leaf triangles, and scaled so that the hypotenuse of the root triangle has length 1 . Then | T | ⩽ ( - 1 / cos θ) 1 +⌊ log 2 k ⌋ .

Proof. We prove the result by induction on k ; Lemma 5 forms the base case. If there is more than one leaf in T , form a smaller tree T ′ by removing from T each path from a leaf to the nearest ancestor with more than one child. These paths are disjoint, and each such removal replaces a subtree with one leaf by the edge at the root of the subtree, so using Lemma 5 again shows that | T | ⩽ -| T ′ | / cos θ . Each leaf in T ′ has two leaf descendants in T , so the number of leaves in T is at most k/ 2 and the result follows. ✷

This, finally, provides a bound on β -skeleton dilation.

Theorem 2. For β &lt; √ 3 / 2 ≈ 0 . 866025 , any β -skeleton has dilation O (n c ) , where c &lt; 1 is a constant depending on β and going to zero in the limit as β goes to zero.

Proof. We have seen (Lemma 4) that we can connect any pair of vertices in the skeleton by a path with length bounded by | T | , where T is a tree of triangles in which all angles are at least π - sin - 1 β , and where T has at most 2 n leaves. By Lemma 6, the length of such a tree is at most


<!-- p:9 -->


Fig. 9. Exponent in the bound of Theorem 2, as a function of β .

$$( - 1 / \cos ( \pi - \sin ^ { - 1 } \beta ) ) ^ { 1 + \lfloor \log _ { 2 } 2 n \rfloor } & = O ( n ^ { \log _ { 2 } \frac { - 1 } { \cos ( \pi - \sin ^ { - 1 } \beta ) } } ) = O ( n ^ { - \frac { 1 } { 2 } \log _ { 2 } ( 1 - \beta ^ { 2 } ) } ) , \\ \text {which has the form specified in the statement of the theorem} \quad \square$$

Fig. 9 shows the growth of the exponent c as a function of β . For √ 3 / 2 ⩽ β ⩽ 1, the theorem does not give the best bounds; a bound of n - 1 on dilation can be proven using the fact that the skeleton contains the minimum spanning tree.

which has the form specified in the statement of the theorem. ✷
