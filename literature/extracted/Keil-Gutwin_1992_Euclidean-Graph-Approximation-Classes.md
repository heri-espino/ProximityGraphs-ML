---
id: "Keil-Gutwin_1992_Euclidean-Graph-Approximation-Classes"
source_pdf: "../pdf/Keil-Gutwin_1992_Euclidean-Graph-Approximation-Classes.pdf"
source_filename: "Keil-Gutwin_1992_Euclidean-Graph-Approximation-Classes.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "excellent"
extraction_score: 98.0
visual_assets: "disabled"
references_file: "../references/Keil-Gutwin_1992_Euclidean-Graph-Approximation-Classes.references.md"
---

<!-- p:1 -->

## Classes of Graphs Which Approximate the Complete Euclidean Graph

### J. Mark Keil and Carl A. Gutwin

Department of Computational Science, University of Saskatchewan, Saskatoon, Canada S7N 0W0

Abstract. Let S be a set of N points in the Euclidean plane, and let d(p, q) be the Euclidean distance between points p and q in S. Let G(S) be a Euclidean graph based on S and let G(p, q) be the length of the shortest path in G(S) between p and q. We say a Euclidean graph G(S) t-approximates the complete Euclidean graph if, for every p, q ε S, G(p, q)/d(p, q) ≤ t. In this paper we present two classes of graphs which closely epp  a  ud sr th dad u u  udte Delaunay triangulation of S, DT(S). We show that DT(S) (2π/(3 cos(π/6)) ≈ 2.42)- approximates the complete Euclidean graph. Secondly, we define θ(S), the e  s  (o o eo    - -) ((1/cos θ)(1/(1 - tan θ)))-approximates the complete Euclidean graph.

## 1. Introduction

Let S be a set of N points in the Euclidean plane. Then a Euclidean graph Go  ts o t ts  o to tat oord  s  t tnd the weight of an edge is equal to the straightline Euclidean distance between the points it connects [7]. Euclidean graphs have been used as a modeling tool; for example, in circuit layout [7]. They also arise indirectly in the solution to geometric problems such as motion planning [2].

Let d(p, q) be the Euclidean distance between points p and q and let G(p, q) be tut ut      dd u (  d u   u dph G(S) t-approximates the complete Euclidean graph if, for every p, q∈S, G(p, q)/d(p, q) ≤ t.

Approximating the complete Euclidean graph has potential application in the development of approximation algorithms or heuristics for problems that involve finding shortest distances in the plane [2], [4], [7]. The efficiency of the resulting algorithms would be dependent upon the number of edges in the approximating graph. For this reason, it is desirable to identify classes of graphs which closely approximate the complete Euclidean graph, yet contain only a linear number of edges.


<!-- p:2 -->


The first known result of this type concerns the graph of the Delaunay triangulation in the L1 metric, DT1. Chew [2] has shown that DT1(S) √10approximates the complete Euclidean graph, independent of S and N. Chew has also shown that the graph of the Delaunay triangulation based on an equilateral a e uae u  e ,,    ea Along similar lines Dobkin et al. [4] have shown that if DT(S) is the graph of the Delaunay triangulation with the Euclidean metric, DT(S) (((1 + √5)/2)π ≈ 5.08)- approximates the complete Euclidean graph, again independent of S and N. Chew [2] was able to exhibit an example for which the ratio, of the shortest distance in DT(S) to the Euclidean distance, approaches π/2 ≥ 1.57. Thus the Delaunay triangulation t-approximates the complete Euclidean graph, where the lowest possible value of t lies in the interval between 1.57 and 5.08. In Section 2 of this paper we show that the Delaunay triangulation indeed (2π/(3 cos(π/6)) ≈ 2.42)- approximates the complete Euclidean graph, independent of S and N.

The Delaunay triangulations are good candidates for approximating graphs, since they contain only a linear number of edges and can be computed from the point set in O(N log N) time [6]. In some applications, however, it may be that the Delaunay approximates are not sufficiently close. In Section 3 we define the c ts  o    toa  t s  s  so O(N log N) time. Each point in a θ-graph defines an edge to a near neighbor in up to k different directions, where θ = 2π/k, thus a θ-graph contains only a linear number of edges if k is a constant. In Section 4 we show that, for k &gt; 8, a θ-graph ((1/cos θ)(1/(1 - tan θ)))-approximates the complete Euclidean graph, again independent of both S and N.

It should be noted that a Euclidean graph which approximates the complete Euclidean graph is a specific example of a graph spanner. Peleg and Schaffer [5], define a t-spanner for a connected simple graph, G = (V, E), to be a subgraph G′ = (V, E') such that, for every u, v ∈ V, dist(u, v, G′)/dist(u, v, G) ≤ t where dist(u, v, H) denotes the distance from u to v in graph H. Graph spanners have applications in distributed systems and communications networks [5].

## 2. Delaunay Triangulation

In this section we consider how well the Delaunay triangulation approximates the complete Euclidean graph. We begin with some definitions. A Voronoi diagram of a set S of points in the plane is a partition of the plane into regions, each corresponding to a point in S, such that, for a point p ∈ S, every point within its corresponding region is closer to p than to any other point of S. By connecting two points of S with an edge if and only if their corresponding Voronoi regions share a boundary, then a Euclidean graph results which is known as the Delaunay triangulation of S. This Voronoi dual is in fact a triangulation under the standard assumption that no four points of S are cocircular [6]. Under this assumption, the Delaunay triangulation of S can be alternatively defined as the Euclidean graph formed by joining a pair of points p and q if and only if there exists a circle a s s   ad n  ot  a    as sor For the remainder of this section we consider the shortest path in DT(S) between two points p and q of S. Without loss of generality we assume that the line, L, through p and q is horizontal and that the x-coordinate of p is less than the x-coordinate of q. The following lemma gives us a bound on DT(p, q).


<!-- p:3 -->


Lemma 1. Let C be a circle whose boundary passes through p and q, with center O and radius r, and let θ be the upper angle pOq. If no point of S lies inside C below L, then DT(p, q) ≤ rθ (i.e., DT(p, q) ≤ the length of the upper arc of C from p to q).

Proof. If no point of S lies inside C, then DT(p, q) = d(p, q) ≤ rθ for any such circle C and we are done. Otherwise, let t be the point in S that lies inside C such that t lies on the boundary of the circle D, whose boundary passes through p and q such that no point in S lies inside D above the line L. Refer to Fig. 1(a) and (b). Let C1 be the circle, with radius r1, that passes through p and t, whose centre O1 lies on the segment pO, and let C2 be the circle, with radius r2, that passes through t and q, whose centre O2 lies on the segment Oq. Let a1 and a2 be the respective intersection points of the circles C1 and C2 with the interior of the segment pq. Note that Fig. 1(a) shows a situation where a2 is left of a1, while Fig. 1(b) shows a situation where a, is left of a2. Also let C33 be the circle, with radius r3, whose boundary passes through a1 and a2 and whose center, O3, lies at the intersection of the line through O, and a1 and the line through O2 and a2.

Using elementary geometry the following facts can be easily verified.

Fact 1. No point of S lies inside C1 below the line through p and t. Likewise, no point of S lies inside C2 below the line through t and q.

Fact 2. Triangles pOq, pO1a1, a2O2q, and a2 O3a1 are all similar isoceles triangles with two equal base angles which we call φ. Thus the upper angles pOq, pOa1, and a2O2q are all equal to θ. If a2 is left of a1, then the upper angle a2O3a1 is also equal to θ.

Fact 3.

$$\cos \varphi = \frac { d ( p , a _ { 1 } ) } { 2 r _ { 1 } } = \frac { d ( a _ { 2 } , q ) } { 2 r _ { 2 } } = \frac { d ( a _ { 2 } , a _ { 1 } ) } { 2 r _ { 3 } } = \frac { d ( p , q ) } { 2 r } .$$

To prove the lemma, consider transforming C downward into the circle C', with radius r' and center O', that passes through p and q and a third point z of S below L, maintaining the property that no point of S lies inside C' below L. If we let θ' be the upper angle pO'q, then clearly r'θ' ≤ rθ. Thus to prove the lemma for a circle C it suffices to prove it for the corresponding circle C'. If there is no such point z below L, then the segment pq forms part of the convex hull of S and DT(p, q) = d(p, q) ≤ rθ as required. Thus for the rest of the proof we assume that circle C has been transformed to pass through a third point z of S that lies below L.


<!-- p:4 -->


Fig. 1

<!-- p:5 -->


As there are only O(n3) possible transformed circles, we may proceed by induction on the rank of the angle θ in the transformed circle. As a base case consider the transformed circle, C, with the smallest possible angle θ. If circle C is not empty, then consider the circle C1, defined earlier, that passes through p and t. By Fact 1 we have that no point of S lies inside C, below the line n nu  a pO1t &lt; pO1a1 = θ. But this contradicts the assumption that C has the smallest possible interior upper angle θ, thus C must have been empty implying that DT(p, q) = d(p, q) ≤ rθ as required.

We may now consider a particular transformed circle C and assume that the lemma holds for all other circles with a smaller interior upper angle. By Fact 2, we have θ1 = pO1t &lt; pO1a1 = θ and θ2 = tO2q &lt; a2 O2q = θ. Thus Fact 1 and the inductive assumption imply that

$$D T ( p , q ) \leq D T ( p , t ) + D T ( t , q ) \leq r _ { 1 } \theta _ { 1 } + r _ { 2 } \theta _ { 2 } .$$

Let C3 be the region that lies inside C3 and above L. Let C12 be the region that lies inside C1 and C2 and above L. If a2 is left of a1, then C12 exists and properly contains C3. Since C3 and C12 are convex, we have L(C3) &lt; L(C12), where L(X) is the length of the boundary of convex body X [1, p. 42]. That is

$$L ( \bar { C } _ { 3 } ) = r _ { 3 } \theta + d ( a _ { 2 } , a _ { 1 } ) < L ( \bar { C } _ { 1 2 } ) = r _ { 1 } ( \theta - \theta _ { 1 } ) + r _ { 2 } ( \theta - \theta _ { 2 } ) + d ( a _ { 2 } , a _ { 1 } ) .$$

Then from (1)

$$\ D T ( p , q ) & \leq r _ { 1 } \theta _ { 1 } + r _ { 2 } \theta _ { 2 } = r _ { 1 } ( \theta - ( \theta - \theta _ { 1 } ) ) + r _ { 2 } ( \theta - ( \theta - \theta _ { 2 } ) ) \\ & = r _ { 1 } \theta + r _ { 2 } \theta - [ r _ { 1 } ( \theta - \theta _ { 1 } ) + r _ { 2 } ( \theta - \theta _ { 2 } ) ] < r _ { 1 } \theta + r _ { 2 } \theta - r _ { 3 } \theta \\ & = ( r _ { 1 } + r _ { 2 } - r _ { 3 } ) \theta$$

by (2), and Fact 3 implies that

$$D T ( p , q ) \leq ( r _ { 1 } + r _ { 2 } - r _ { 3 } ) \theta = \left ( \frac { d ( p , a _ { 1 } ) } { 2 \cos \varphi } + \frac { d ( a _ { 2 } , q ) } { 2 \cos \varphi } - \frac { d ( a _ { 2 } , a _ { 1 } ) } { 2 \cos \varphi } \right ) \theta = \frac { d ( p , q ) \theta } { 2 \cos \varphi } = r \theta .$$

If a2 is not left of a1, then from (1) we have

$$D \mathbf T ( p , q ) \leq r _ { 1 } \theta _ { 1 } + r _ { 2 } \theta _ { 2 } \leq r _ { 1 } \theta + r _ { 2 } \theta = ( r _ { 1 } + r _ { 2 } ) \theta$$

and Fact 3 implies that

$$D T ( p , q ) \leq ( r _ { 1 } + r _ { 2 } ) \theta = \left ( \frac { d ( p , a _ { 1 } ) } { 2 \cos \varphi } + \frac { d ( a _ { 2 } , q ) } { 2 \cos \varphi } \right ) \theta \leq \frac { d ( p , q ) \theta } { 2 \cos \varphi } = r \theta . \quad \square$$

We are now able to prove the main theorem of this section.


<!-- p:6 -->


Theorem 1. Given a set S of N points in the plane, for any two points p and q in S

$$\frac { \ D T ( p , q ) } { d ( p , q ) } \leq \frac { 2 \pi } { 3 \cos \left ( \frac { \pi } { 6 } \right ) } \approx 2 . 4 2 ,$$

independent of S and N.

Proof. Let C1 (C2) be the circle that passes through p and q with centre O (O2) above (below) L such that angles qpO, (qpO2) and pqO (pqO2) equal π/6. Let LUNE be the intersection of the interiors of C1and C2. See Fig. 2.

If no points of S lie inside LUNE, then C, is empty below L and the lemma implies that DT(p, q) ≤ r1θ1 where r1 is the radius of C1 and θ, is the upper angle pO1q. We have θ1 = 2π − (π − 2(π/6)) = π and also

$$r _ { 1 } = \frac { d ( p , q ) } { 2 \cos ( \pi / 6 ) } ,$$

$$D T ( p , q ) \leq \frac { 2 \pi } { 3 \cos ( \pi / 6 ) } \, d ( p , q )$$

thus

as required.

It remains to consider the case where there exists a point of S that lies inside LUNE. Without loss of generality we need only consider the set of points S' ⊆ S that lie inside LUNE and closer to p than q. Let € be the set of circles that pass through point p whose centers lie on the segment pO. Without loss of generality we may assume that there exists a point t of S' that does not lie below L, such that the intersection of LUNE and the circle C3 ∈ € that passes through t contains no point of S. Refer to Fig. 2. Let θ be the angle qpt and let φ be the angle pqt. Let c be the distance from t to the closest point t' on the line L. Let α be the upper angle pO3t and let r be the radius of C3.

We now proceed by induction on the rank of d(p, q) with respect to pairs of point a   =   s       o         d the segment pq forms part of the Delaunay triangulation of S [6].

As an inductive step consider the ith closest pair p and q and assume that for all closer pairs the theorem holds. We have

$$D T ( p , q ) \leq D T ( p , t ) + D T ( t , q ) .$$

Since C3 is empty below the line through p and t, Lemma 1 implies that DT(p, t) ≤ αr. From the inductive assumption we have

$$D T ( t , q ) \leq \frac { 2 \pi } { 3 \cos ( \pi / 6 ) } \, d ( t , q ) .$$


<!-- p:7 -->

Thus

$$D T ( p , q ) \leq \alpha r + \frac { 2 \pi d ( t , q ) } { 3 \cos ( \pi / 6 ) } .$$

Consider the case in which t lies on L. We have α = π and r = d(p, t)/(2 cos(π/6)) therefore from (3) we have

$$D T ( p , q ) \leq \frac { 2 \pi } { 3 \cos ( \pi / 6 ) } \left [ d ( p , t ) + d ( t , q ) \right ] = \frac { 2 \pi } { 3 \cos ( \pi / 6 ) } \, d ( p , q )$$

as required.


<!-- p:8 -->


It remains to consider the case where t lies above L. Using elementary geometry we have α = 2π - (π − 2(π/6 − θ)) = π - 2θ and, since d(p, t) = c/sin θ, using the sine law we have

$$r = \frac { c \sin ( \pi / 6 - \theta ) } { \sin ( \frac { 2 } { 3 } \pi + 2 \theta ) \sin \theta } = \frac { c } { 2 \sin ( \pi / 3 + \theta ) \sin \theta } .$$

Since d(t, q) = c/sin φ we can substitute into (3) to get

$$D T ( p , q ) \leq ( \frac { 2 \pi - \theta } { 3 } ) \frac { c } { \sin ( \pi / 3 + \theta ) \sin \theta } + \frac { 2 \pi c } { 3 \cos ( \pi / 6 ) \sin \varphi } .$$

Let a be the distance from p to t'' and let b be the distance from t' to q. Then

$$d ( p , q ) = a + b = \frac { c } { \tan \theta } + \frac { c } { \tan \varphi } ,$$

therefore

$$\text {truncate} \\ \frac { \text {DT} ( p , q ) } { d ( p , q ) } & \leq \frac { ( \i \pi - \theta ) / ( \sin ( \pi / 3 + \theta ) \sin \theta ) + 2 \pi / ( 3 \cos ( \pi / 6 ) \sin \varphi ) } { 1 / \tan \theta + 1 / \tan \varphi } \\ & = \left [ \frac { \sqrt { \pi } - \theta } { \sin ( \pi / 3 + \theta ) \sin \theta } + \frac { 2 \pi } { 3 \cos ( \pi / 6 ) \sin \varphi } \right ] \cos \theta \sin \varphi \\ & = ( \i \pi - \theta ) \, \frac { \sin \varphi } { \sin ( \pi / 3 + \theta ) \sin ( \varphi + \theta ) } + \frac { 2 \pi \sin \theta } { 3 \cos ( \pi / 6 ) \sin ( \varphi + \theta ) } = f ( \theta , \varphi ) .$$

Since t lies inside LUNE above L and closer to p than q we have φ &gt; 0, θ ≥ φ, and θ + φ &lt; π/3. With these contraints it can be shown that ∂f/∂θ ≠ 0 if θ ≥ π/10 and ∂f/∂φ ≠ 0 if θ ≤ π/10. We-thus have that f(θ, φ) achieves its maximum value on the boundary. There are three boundary conditions to check.

As φ approaches, 0, sin φ approaches 0 and sin(φ + θ) approaches sin(θ) thus

$$\lim _ { \varphi \to 0 } f ( \theta , \varphi ) = \frac { 2 \pi } { 3 \cos ( \pi / 6 ) } .$$

As φ approaches θ, f(θ, φ) approaches

$$g ( \theta ) & = \left ( \frac { 2 \pi } { 3 } - \theta \right ) \frac { \sin \theta } { \sin ( \pi / 3 + \theta ) \sin ( 2 \theta ) } + \frac { 2 \pi \sin \theta } { 3 \cos ( \pi / 6 ) \sin 2 \theta } \\ & = \frac { 2 \pi / 3 - \theta } { \sin ( \pi / 3 + \theta ) 2 \cos \theta } + \frac { \pi } { 3 \cos ( \pi / 6 ) \cos \theta } ,$$


<!-- p:9 -->


where 0 &lt; θ &lt; π/6. Using calculus it can be shown that g(θ) has one local minimum and no local maximum when 0 &lt; θ &lt; π/6, thus g(θ) must attain its maximum value as θ approaches either 0 or π/6:

$$\lim _ { \theta \to 0 } g ( \theta ) = \frac { \pi } { 3 \sin ( \pi / 3 ) } + \frac { \pi } { 3 \cos ( \pi / 6 ) } = \frac { 2 \pi } { 3 \cos ( \pi / 6 ) }$$

and

$$\lim _ { \theta \to \pi / 6 } g ( \theta ) = \frac { \pi } { 4 \cos ( \pi / 6 ) \sin ( \pi / 2 ) } + \frac { \pi } { 3 \cos ^ { 2 } ( \pi / 6 ) } \approx 2 . 3 0 .$$

As θ + φ approaches π/3, f(θ, φ) approaches

$$h ( \theta ) = \left ( \frac { 2 \pi } { 3 } - \theta \right ) \frac { \sin ( \pi / 3 - \theta ) } { \sin ( \pi / 3 + \theta ) \sin ( \pi / 3 ) } + \frac { 2 \pi \sin \theta } { 3 \cos ( \pi / 6 ) \sin ( \pi / 3 ) } ,$$

where π/6 &lt; θ &lt; π/3. It can be shown that ∂h/∂θ ≠ 0 when π/6 &lt; θ &lt; π/3, thus h(θ) attains its maximum value either as θ approaches π/6 or as θ approaches π/3:

$$\lim _ { \theta \to \pi / 6 } h ( \theta ) \approx 2 . 3 0$$

$$\lim _ { \theta \to \pi / 3 } h ( \theta ) = \frac { 2 \pi } { 3 \cos ( \pi / 6 ) } \, .$$

$$\frac { D T ( p , q ) } { d ( p , q ) } \leq \sum _ { 0 < \varphi \leq \theta < \pi / 3 \sim \varphi } f ( \theta , \varphi ) \leq \frac { 2 \pi } { 3 \cos ( \pi / 6 ) }$$

as required.

## 3. Fixed-Angle θ-Graph

Definition. Consider the shortest path from a point p to a point q in a Euclidean graph G. Let r be the intermediate vertex adjacent to p on this path. If the angle qpr is small we might suspect that G(p, q) is not much longer than d(p, q), whereas if angle qpr is large we might suspect a greater difference between G(p, q) and d(p, q). This intuition suggests that by defining a type of graph in which each point will be connected to a near neighbor in each of a variety of directions we may approximate the complete Euclidean graph.

and

Thus we have

[]


<!-- p:10 -->

Fig. 3

Given a set S of points in the plane we define the θ-graph, for θ = 2π/k, k an integer constant such that k &gt; 4, to be the Euclidean graph, θ(S), whose edges are defined as follows. From a point p ∈ S, with x-coordinate x(p) and y-coordinate y(p), draw k rays such that the rays form the angles 2π(i − 1)/k, i = 1, 2, ..., k, respectively with the positive x-axis. In Fig. 3, k = 6 and the rays from point p are drawn with dashed lines. These rays divide the plane into k regions and we let S(p), i = 1, 2, ..., k, be the points q ∈ S such that the angle φ between the ray pą and the positive x-axis is such that 2π(i — 1)/k ≤ φ &lt; 2πi/k. If S(p) is not empty, then p will be the source of a type 1 edge to a point r∈S1(p) such that x(t) = min{x(q)|q ∈ S(p)}. If there are several candidates for r, the type 1 edge from p will go to the point of minimum y coordinate. In general, let q' be the P( - r a   r    d     r r o. Then p will be the source of a type i edge destined to a point r if and only if r ∈ S(p), and for all other q ∈ S(p) either d(p, r') &lt; d(p, q') or d(p, r) = d(p, q′) and d(r, r') &lt; d(q, q'). Once the edges have been defined, the implied directions on the edges are ignored so that θ(S) is an undirected graph.

Note that a θ-graph differs from a geographic neighbor graph [9] in that a point will not necessarily be connected to its nearest neighbor in each region. Also the θ-graph is easier to compute. In the next section we present a simple O(N log N) plane sweep algorithm for constructing a θ-graph. Until recently the best algorithm -or   (  d  -  e     nt ly, Wee et al. [8] presented a complex O(N log N) divide-and-conquer algorithm for this problem.


<!-- p:11 -->


Algorithm. To construct the θ-graph for a given point set the algorithm makes use of a separate plane sweep for each of the k different types of edges.

Let us consider the plane sweep in which the type 1 edges are identified, as the other sweeps are performed similarly. During the performance of this plane sweep, three different orderings of the points are employed. These are the ordering by x-coordinate, the ordering by y-coordinate, and the γ ordering by the projections of the points onto the oriented line L through the origin at angle 2π/k + π/2 with the positive x-axis which is oriented by the ray from the origin at angle 2π/k +- π/2 wt t  t tw oi  i t st t t tio points have the same x-coordinate, the same y-coordinate, or the same projection onto the line L. Let γ(p) be the rank of point p in the γ ordering.

The point set is swept in decreasing order of y-coordinate. As the sweep progresses a table T of active points to which type 1 edges may be destined is maintained in γ order. When a point p is encountered on the sweep the following operations are performed:

1. Insert point p into table T.
2. d  n   n          .
3. Repeat Forever

If p has a successor r in T, then if x(r) &gt; x(p), then delete r from T else exit loop else exit loop

Proof of Correctness. Here we prove that the above algorithm correctly computes the type 1 edges in θ(S). The proof that the other edges are correctly determined is analogous. Again for simplicity we assume that no two points have the same x-coordinate, the same y-coordinate, or the same projection onto the line L.

We first note that the table T maintains the points in both γ order and reverse x order.

Lemma 2. Table T is maintained so that if s is the predecessor of t in T, then γ(s) &lt; γ(t) and x(s) &gt; x(t).

Proof. We proceed by induction on the number of points encountered by the sweep. When a point t is inserted into T it is placed in γ order. If successors of t are then deleted, the table will remain in correct γ order. It remains to show that correct reverse x order is maintained in the neighborhood of t. If s is the predecessor of t in T, then, since y(s) &gt; y(t), γ(s) &lt; γ(t), and θ = 2π/k ≤ π/2, we ha  e            (  s eas no successor in T or, for the successor r of t in T, x(r) &lt; x(t). □


<!-- p:12 -->


The next lemma shows that the points deleted in step 3 of the algorithm are not needed in further processing.

Lemma 3. If a point r is deleted in step 3 of the algorithm, immediately after the insertion of a point z, then r cannot be the destination of a type 1 edge whose source is a point u with y(u) &lt; y(z).

Proof. Since r is deleted by the insertion of point z, we know that y(r) &gt; y(z), γ(r) &gt; γ(z), and x(r) &gt; x(z). If a point u, with y(u) &lt; y(z), is to be the source of a type 1 edge destined to r we must have that γ(r) &lt; γ(u). But we have y(u) &lt; y(z), γ(z) &lt; γ(r) &lt; γ(u), and x(z) &lt; x(r), thus point z prevents the formation of a type 1 edge from u to r. □

The final lemma of this section shows that type 1 edges are being correctly reported.

Lemma 4. When p is inserted into table T, p has predecessor q in T if and only if p is the source of a type 1 edge to q in the θ-graph.

i n n (  ( n ( &gt; (     ss    mo) no point z exists in T when p is inserted, such that y(p) &lt; y(z), γ(z) &lt; γ(p), and x(z) &lt; x(q). It remains to show that no point r, that has been deleted from T, exists, such that γ(r) &lt; γ(p) and x(r) &lt; x(q). Assume, to the contrary, that there are points that have been deleted from T with γ rank less than γ(p) and x-coordinate less was caused by the insertion of a point w with y(p) &lt; y(w) &lt; y(r), γ(r) &gt; γ(w), and x(r) &gt; x(w). If γ(w) &lt; γ(q), then the insertion of w would have caused the deletion of q contradicting the fact that q is in T when p is inserted. If γ(w) &gt; γ(q), this contradicts the fact that q is the predecessor of p in T, since γ(p) &gt; γ(r) &gt; γ(w) &gt; γ(q).

If p is the source of a type 1 edge to q in the θ-graph, then by definition we from T before p was inserted. We thus have that when p is inserted into T, q exists a type 1 edge destined to q. If x(z) &gt; x(q), then either γ(q) &gt; γ(z) or y(z) &gt; y(q). In the former case, we have a contradiction to the assumption that z is the immediate predecessor of p in T. If y(z) &gt; y(q), then z would have been deleted when q was inserted since γ(z) &gt; γ(q), x(z) &gt; x(q), and T is maintained in both γ order and reverse x order. □

than x(q). Let r be such a point with minimum y-coordinate. The deletion of r have y(p) &lt; y(q) and γ(g) &lt; γ(p). Then, by Lemma 3, q could not have been deleted in T with γ(q) &lt; γ(p). If q is not the immediate predecessor of p, then some point z is such that y(p) &lt; y(z) and γ(z) &lt; γ(p). If x(z) &lt; x(q), then p is not the source of

We are now able to prove the main theorem of this section.

Theorem 2. The algorithm correctly computes the θ-graph for a set S of points in the plane in O(N log N) time, where θ = 2π/k and k is an integer constant such that k &gt; 4.


<!-- p:13 -->


Proof. The correctness of the algorithm follows from Lemma 4. To verify the timing note that if the table of active points T is maintained as a balanced binary tree (e.g., 2-3-tree), then the operations insert, delete, successor, and predecessor can be performed in O(log N) time. Thus each of the k plane sweeps can be performed in O(N log N) time. Since k is a constant, the total time required to form the θ-graph is O(N log N). []

## 4. The Bound for θ-Graphs

Given a set S of points in the plane and the θ-graph θ(S), for θ = 2π/k, k an integer constant such that k &gt; 8, the purpose of this section is to show that the graph θ(S) closely approximates the complete Euclidean graph. We must thus show that the ratio θ(p, q)/d(p, q) is bounded by a small constant for any pair of points p and q in S. The shortest path from p to q in the graph θ(S) will pass through m, 0ols o n o o  ng oli      t to θ(p, q)/d(p, q) with a function of m.

Lemma 5. If the shortest path from p to q in θ(S), for θ = 2π/k, k an integer constant sa s tas   ta   k t en

$$\frac { \theta ( p , q ) } { d ( p , q ) } \leq \frac { 1 } { \cos \theta } \left ( \frac { \tan ^ { m } \theta - 1 } { \tan \theta - 1 } \right ) + \tan ^ { m } \theta .$$

Proof. Let s, be the ith intermediate point on the path from p to q, 0 ≤ i ≤ m, so = p. Let θ'(p, q) be the length of the shortest path from p to q under the folowing restriction. If the origin is located at s and q is located so that the ray sq forms an angle φ with the x-axis where 2π(i — 1)/k ≤ φ &lt; 2πi/k, then the edge from s to si+ 1 in the path from p to q is of type i. Clearly, θ(p, q) ≤ θ'(p, q) thus the lemma will follow if we can prove the bound for θ'(p, q).

We proceed by induction on m. In the base case, m = 0, there are no intermediate points on the path from p to q and θ'(p, q) = d(p, q).

As an inductive assumption we assume that if there are m - 1 intermediate points on the shortest restricted path between two points p and q, then

$$\frac { \theta ^ { \prime } ( p , q ) } { d ( p , q ) } \leq \frac { 1 } { \cos \theta } \left ( \frac { \tan ^ { ( m - 1 ) } \theta - 1 } { \tan \theta - 1 } \right ) + \tan ^ { ( m - 1 ) } \, \theta .$$

As an inductive step we consider the case where there are m intermediate points on the shortest restricted path between p and q. Since there are m — 1 intermediate points on the shortest restricted path from s1 to q in θ(s), the inductive assumption implies that

$$\theta ( p , q ) \leq d ( p , s _ { 1 } ) + d ( s _ { 1 } , q ) \left [ \frac { 1 } { \cos \theta } \left ( \frac { \tan ^ { ( m - 1 ) } \theta - 1 } { \tan \theta - 1 } \right ) + \tan ^ { ( m - 1 ) } \theta \right ] .$$


<!-- p:14 -->


If we let θ"(p, q) equal the right-hand side of (*), the lemma will follow if we can prove the bound for θ"(p, q).

Let the origin be located at p. Without loss of generality let q be located so that the angle φ between the x-axis and the ray pq is such that 0 ≤ φ &lt; 2π/k. We also then have that s1 is located so that the angle α between the x-axis and the ray ps1 is such that 0 ≤ α &lt; 2π/k. To proceed further we need more information as to where q and s1 are located. The following claim allows us to restrict their locations.

Claim. The ratio θ′′(p, q)/d(p, q) can attain its maximum when q is located on the x-axis and s1 is located to maximize the angle α such that 0 ≤ α &lt; 2π/k.

Proof of the Claim. We show how q and s1 can be moved to their desired locations without decreasing the value of the ratio θ"(p, q)/d(p, q). If we move q and s1 so that the values of d(p, s1) and d(s1, q) do not decrease and the value of d(p, q) does not increase, then the value of the ratio θ′′(p, q)/d(p, q) will not decrease.

If s, and q are located such that angle α is less than angle φ, we then consider the polar coordinates of s1 and q, (α, rs) and (φ, rq) respectively. If we move q to location (α, rq) and s1 to the location (φ, rs), we preserve the values d(p, s1) = rs, d(s1, q) and d(p, q) = rq. We may thus hence forth assume that if φ is the angle bet  i-x t e t t s   d  t  st- t ete ps1, then α ≥ φ.

To complete the proof of the claim we need to show that we can move s1 so that the angle α approaches 2π/k, without decreasing the ratio θ′′(p, q)/d(p, q). To do this we move s, by increasing its y-coordinate as much as possible without violating the condition that α &lt; 2π/k. Since both p and q lie on the x-axis, this transformation will increase the values of d(p, s1) and d(s1, q), but will not affect the value of d(p, q). □

We now show how q can be moved to the x-axis. To do this we rotate the segment s1q about s1 until q lies on the x-axis. This transformation clearly preserves the values d(p, s1) and d(s1, q). That α ≥ φ ensures that the transformation does not increase the value of d(p, q).

The claim implies that in (*) 0 ≤ d(p, s1) &lt; d(p, q)/cos θ. Using elementary calculus it can be shown that θ"(p, q) will attain its maximum when s1 is located so that d(p, s1) is maximized. In this situation we have d(s1, q) = d(p, q) tan θ thus

$$\theta ^ { m } ( p , q ) \leq \frac { d ( p , q ) } { \cos \theta } + d ( p , \, q ) \, \tan \, \theta \left [ \frac { 1 } { \cos \theta } \left ( \sum _ { i = 0 } ^ { m - 2 } \tan ^ { i } \, \theta \right ) + \tan ^ { ( m - 1 ) } \, \theta \right ] .$$

Therefore the ratio

$$\frac { \theta ^ { \prime \prime } ( p , q ) } { d ( p , q ) } \leq \frac { 1 } { \cos \theta } \left ( \sum _ { i = 0 } ^ { m - 1 } \tan ^ { i } \theta \right ) + \tan ^ { m } \theta = \frac { 1 } { \cos \theta } \left ( \frac { \tan ^ { m } \theta - 1 } { \tan \theta - 1 } \right ) + \tan ^ { m } \theta$$

as required.

[]


<!-- p:15 -->


Note that since θ(p, q) may be strictly less than θ"(p, q), the above bound is not t s o   ot  l    os     t θ(p, q) = θ′′(p, q) for m &gt; 2.

The bound given by the lemma is strictly increasing with m. By taking the limit as m approaches infinity we have the following theorem.

Theorem 3. Given a set S of N points in the plane and the θ-graph θ(S), for θ = 2π/k, k an integer constant such that k &gt; 8, for any two points p and q in S

$$\frac { \theta ( p , q ) } { d ( p , q ) } \leq \frac { 1 } { \cos \theta } \left ( \frac { 1 } { 1 - \tan \theta } \right ) ,$$

independent of S and N.

Given θ = 2π/k, the following table illustrates the nature of the bound B = (1/cos θ)(1/(1 − tan θ)):

## 5. Concluding Remarks

We have shown that DT(S), the graph of the Delaunay triangulation of a point set S, (2π/(3 cos(π/6)) ≈ 2.42)-approximates the complete Euclidean graph, independent of S and N. The obvious open problem is to improve this bound.

We also introduced fixed-angle θ-graphs as a potential new tool in the investigation of problems involving shortest distances in the plane. For θ = 2π/k, k a constant such that k &gt; 8, we were able to develop an O(N log N)-time algorithm for the construction of θ(S) and we showed that θ(S) ((1/cos θ)(1/(1 – tan θ)))- approximates the complete Euclidean graph, independent of S and N. Note th     n o   o s  t o investigate θ-graphs for higher-dimensional point sets.

Neither θ-graphs nor Delaunay triangulations have bounded degree. Is there a graph with bounded degree which approximates the complete Euclidean graph?

### Acknowledgments

This work was supported by the Natural Science and Engineering Research Council of Canada. The authors wish to thank R. Coulman for producing the figures.


<!-- p:16 -->
