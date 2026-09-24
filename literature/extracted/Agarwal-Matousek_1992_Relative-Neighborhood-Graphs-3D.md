---
id: "Agarwal-Matousek_1992_Relative-Neighborhood-Graphs-3D"
source_pdf: "../pdf/Agarwal-Matousek_1992_Relative-Neighborhood-Graphs-3D.pdf"
source_filename: "Agarwal-Matousek_1992_Relative-Neighborhood-Graphs-3D.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "excellent"
extraction_score: 100.0
visual_assets: "disabled"
references_file: "../references/Agarwal-Matousek_1992_Relative-Neighborhood-Graphs-3D.references.md"
---

<!-- p:1 -->

## Relative neighborhood graphs in three dimensions*

### Pankaj K. Agarwal

Computer Science Department, Duke University, Durham, NC 27706, USA

#### Jiří Matoušek

Department of Applied Mathematics, Charles University, Praha, Czechoslovakia

Communicated by Herbert Edelsbrunner Submitted 1 May 1991 Accepted 23 September 1991

Abstract

Agarwal, P.K. and J. Matoušek, Relative neighborhood graphs in three dimensions, Computational Geometry: Theory and Applications 2 (1992) 1–14.

The relative neighborhood graph (RNG) of a set S of n points in Ra is a graph (S, E), where d &gt; {(z  (z d}     z d          ( d) show that in R3, RNG(S) has O(n4/3) edges. We present a randomized algorithm that constructs RNG(S) in expected time O(n3/2+e) assuming that the points of S are in general position. If the points of S are arbitrary, the expected running time is O(n7/4+ε). These algorithms can be made deterministic without affecting their asymptotic running time.

Keywords. Pattern matching; geometric graphs; arrangements; random sampling; closest pairs.

## 1. Introduction

Let S be a set of n points in Ra. The relative neighborhood graph of S, denoted RNG(S), is a graph (S, E), where a pair of points (p, q) ∈ E if and only if

$$d ( p , q ) \leqslant \max _ { p ^ { \prime } \in S - \{ p , q \} } \{ d ( p , p ^ { \prime } ) , d ( q , p ^ { \prime } ) .$$

Here d(.,.) is the Euclidean distance. In other words, (p, q) is an edge of RNG(S) if the interior of the lune of p and q, defined as the set of points

$$\lambda ( p , q ) = \{ z \, \Big | \, d ( p , z ) \leqslant d ( p , q ) \text { and } d ( q , z ) \leqslant d ( p , q ) \} ,$$

does not contain any point of S.

* Work by the first author was supported by National Science Foundation Grant CCR-91-06514. Part of this work was done while the second author was visiting School of Mathematics, Georgia Institute of Technology, Atlanta.

0925-7721/92/$05.00 © 1992—Elsevier Science Publishers B.V. All rights reserved

1


<!-- p:2 -->


Relative neighborhood graphs were originally introduced by Toussaint [23], and have applications in pattern recognition. See [12,15, 17,19-21,24] for variants and generalizations of relative neighborhood graphs.

It is well known that RNG(S) is a subgraph of Delaunay triangulation of S, therefore RNG(S) is a planar graph in R2. But, for d≥3, Delaunay triangulation can have Ω(n2) edges in the worst case, so an interesting question is t t t t st  t  s t t  t   t o  dd a  =  r r   r   a (r O(n3/2β(n)) has been proved by Jaromczyk and Kowaluk [14], where β(n) is an extremely slowly growing function. In this paper we improve the upper bound to O(n43) by reducing it to counting the number of bi-chromatic closest pairs. Note that if we assume points in Ra to be in general position, that is, only O(1) points lie on a (d – 1)-sphere, then RNG(S) has only linear number of edges; see e.g. [22].

Like minimum spanning tree, a common approach for computing RNG(S) is—first construct a graph G that contains all edges of RNG(S) and then throw away the edges of G that do not appear in RNG(S). In R2, Delaunay triangulation can be used as G, and therefore RNG(S) can be computed in O(n log n) time [22, 16, 25]. But for d = 3, one has to use some other graph if one wants to construct it in subquadratic time, because, as mentioned above, Delaunay triangulation can have quadratic number of edges. The previously best known algorithm for constructing RNG(S) in R3 is by Jaromczyk and Kowaluk, on oo n e on o     e o ol oh running time can be improved to O(n2) [13, 22].

In this paper, we present a randomized algorithm whose expected running time a n  ods  on    ntr  r   ( san be extended to higher dimensions too. If the points in S are arbitrary, then RNG(S) can be computed in R2 in expected time O(n7/4+ε) by modifying the previous algorithm. Both of these algorithms can be made deterministic without affecting their asymptotic time complexity.

We extend our algorithms to compute k-relative neighborhood graphs. k-RNG(S) has an edge (p, q) if the interior of λ(p, q) contains less than k points of S.

This paper is organized as follows. In Section 2 we prove the upper bound on RNG in R3. Section 3 gives the main algorithm. We generalize our algorithm to arbitrary set of points in Section 4, and to k-relative neighborhood graphs in Section 5. We conclude with some final remarks in Section 6.

## 2. Complexity of RNG

In this section we show that RNG(S) of a set S of n points in R3 has O(n4/3)

'Throughout this paper, ε denotes an arbitrarily small positive constant, and the constant of proportionality in the time complexity tends to ∞ as ε ↓0.


<!-- p:3 -->


edges. In order to prove the bound, we need to define a few notation, some of which are borrowed from [1]. Throughout this section we shall not distinguish between points and vectors. Given a unit vector u ∈ Ra and an angle α, let

Cone(u, α) = {x ∈ R3 |∠(x, u) ≤ α},

$$\angle ( x , u ) = \arccos \frac { x ^ { \top } u } { \| x \| \cdot \| u \| } \, .$$

Let P, Q be two sets of points. The pair (P, Q) is called well separated if there are a point z ∈ R3 and a unit vector u, such that P⊂z + Cone(-u, α) and Q ⊂ z + Cone(u, α) for some α &lt; π/6 (see Fig. 1). The edges of RNG(P ∪ Q) of the form (p, q) ∈ P × Q will be referred to as cross edges. A point q ∈ Q is called a bi-chromatic closest neighbor of p ∈ P if d(p, q) = minq'eQ d(p, q′), a pair (p, q) ∈ P× Q is called a bi-chromatic closest pair if d(p, q) = minp'eP, q'∈Q d(p', q′), and a pair (p, q) is called a symmetric bi-chromatic closest neighbor pair if q is a bi-chromatic closest neighbor of p and vice-versa.

Lemma 2.1. Let P, Q be a well separated pair of set of points in Ra. Then RNG(P ∪ Q) has a cross edge (p, q) if and only if (p, q) is bi-chromatic closest neighbor pair.

Proof. Let (p, q) be a bi-chromatic closest neighbor pair. Then the ball Bp (resp. Bq) of radius d(p, q) around p (resp. q) does not contain any point of P (resp. Q) in its interior. Consequently, lune λ(p, q) = Bp ∩ Bq does not contain any point of P ∪ Q in its interior. Therefore, (p, q) is an edge in RNG(P ∪ Q).

For the only if' part, assume, in order to obtain a contradiction, that q is not a bi-chromatic closest neighbor of p and (p, q) ∈ RNG(P ∪ Q), i.e., there is a point q′∈ Q such that d(p, q′) &lt; d(p, q) and q′ does not lie in the interior of λ(p, q).

Let h be the plane passing through p, q and q'. Let s be the intersection point of h and the boundary of λ(p, q) such that d(p, q) = d(q, s) = d(p, s) and that s and q′ lie on the same side of the line supporting pq (see Fig. 2). Let ρ1 (resp. ρ2) denote the ray emanating from p and passing through q (resp. s). The angle of the wedge formed by ρ1 and ρ2 is π/3, as △spq is an equilateral triangle. Since

Fig. 1. A well separated pair of sets.

where


<!-- p:4 -->


4

Fig. 2. Triangle spq.

q′ λ(p, q) and d(p, q) &gt; d(p, q′), it is easily seen that q′ cannot lie in this wedge, therefore ∠qpq'≥π/3. But that is impossible, because ∠qpq′≤ 2α &lt; π/3. Hence, q is a bi-chromatic closest neighbor of p.

Similarly one can prove that p is a bi-chromatic closest neighbor of q.

Lemma 2.2. Let P, Q be a well separated pair of set of points in R3. Then RNG(P ∪ Q) has O(m2/3n2/3 + m + n) cross edges, where m = |P| and n = |Q|.

Proof. Let G be the subgraph of RNG(P ∪ Q) induced by its cross edges. Let G1, . .. , G, denote the nontrivial connected components of G, and let (P, Qi) denote the vertices of G. We claim that each edge (p, q) in (Pi, Q) connects a bi-chromatic closest pair of P; an Q. Suppose the contrary, i.e., there are a bi-chromatic closest pair (p'q') of (Pi, Q) and an edge (p, q) in G, such that d(p, q) &gt; d(p', q′). Since G, is a connected graph, one of the following two conditions should hold: (i) there is a vertex z ∈ P ∪ Q, such that two of the edges incident to z have different lengths, or (ii) length of all edges of G, is d(p, q). But (i) violates Lemma 2.1 for z and (ii) violates the same lemma for p'. Hence, all the edges of G connect bi-chromatic closest pairs of (P, Q).

Edelsbrunner and Sharir [11] have proved that the number of bi-chromatic closest pairs between a set of a points and another set of b points in R3 is O(a2/3b2/3 + a + b). Thus, the number of edges in G, is O(m23n2/3 + mi + ni), where mi = P|, ni = |Q|. Summing it over all connected components of G, we obtain the desired bound.

The argument of Lemma 2.2 also implies the following.

Corollary 2.3. The number of symmetric bi-chromatic closest neighbor pairs between a set of m points and another set of n points in ®3 is O(m2/3n2/3 + m + n).


<!-- p:5 -->


To prove the main result of this section, we need a procedure that decomposes S ⊂ Ra into a family

$$\mathcal { F } = \{ ( P _ { 1 } , Q _ { 1 } ) , ( P _ { 2 } , Q _ { 2 } ) , \dots , ( P _ { s } , Q _ { s } ) \}$$

of well-separated pairs with the following properties:

(1) Σi=1 ({Pi| + |Qi{) = O(n logd−1 n), and

(2) for every pair p, q ∈ S, there is an i ≤s such that p ∈ P and q ∈ Q.

The second condition ensures that every edge of RNG(S) appears as a cross edge in at least one of RNG(P ∪ Q). Agarwal et al. [1] have given a procedure to construct such a family of pairs of sets in Ra. For the sake of completeness, we shall describe it briefly here.

A basis B = {b1, . . . , bd} of Rd is called narrow if there exist a unit vector u and an angle α &lt; π/3 such that

$$c o n ( B ) = \left \{ \sum _ { i = 1 } ^ { d } \lambda _ { i } b _ { i } \, | \, \lambda _ { i } \geqslant 0 , \forall i \} \subseteq C o n e ( u , \, \alpha ) .$$

Let F be a family of t = O(1) narrow bases such that ∪B∈(cone(B) ∪ cone(-B)) = Rd. Yao [26] has shown that for every dimension d one can compute such a family of narrow bases in O(1) time. For each B ∈ F, we compute a set of well-separated pairs of subsets of S. Let (x, ... , xd) be the coordinates of a point of x in basis B, i.e., x = x1b1 + x2b2 + · · · + xdbd. Here is the outline of the algorithm. Initially k = d and P = Q = S.

We repeat the above procedure for all B ∈ F. It has been shown in [1] that the ( os as s s a    s ord Let Ek(m + n) denote the number of cross-edges in the pairs of sets returned by the algorithm Pairing(k, P, Q) (see Fig. 3) with |P| = m, |Q| = n, then

$$E _ { k } ( m + n ) \leqslant 2 E _ { k } \left ( \frac { m + n } { 2 } \right ) + E _ { k - 1 } ( m + n )$$

Algorithm: Pairing (k, P, Q)

if k = 0 and P, Q ≠ ∅ then

output (P, Q)

end if

if k ≥ 1 then

medk := median of the kth coordinate of P ∪ Q

P1 = { p ∈ P | Pk ≤ medk}, Pr = { p ∈ P | pk &gt; medk}

Q1 = {p ∈ Q | pk ≤ medk}, Qr = {p ∈ Q | pk &gt; medk}

Pairing (k, P1, Qt), Pairing (k, Pr, Qr)

Pairing (k − 1, P1, Qr)

end if

Fig. 3. Computing the family of well separated pairs.


<!-- p:6 -->


and, by Lemma 2.2, E0(m + n) = O(m2/3n2/3 + m + n). The solution of the above recurrence is easily seen to be O(m2/3n2/3 + (m + n)logk(m + n)). Initially P = Q = S and t = O(1), therefore we can conclude the following.

Theorem 2.4. Given a set S of n points in R3, RNG(S) has O(n43) edges.

Remark 2.5. (i) It is easy to show that a lower bound on the number of bi-chromatic closest pairs will yield a similar lower bound on the size of relative neighborhood graphs.

- (ii) If we assume that the points of S are in general position, that is, no d + 2 points lie on a (d – 1)-sphere, the size of RNG(S) is obviously linear (see e.g. [22]).

## 3. Computing RNG: points in general position

In this section we assume that the point of S ⊂ R3 are in general position—no five points lie on a sphere. This condition implies that every point of S has only constant number of closest neighbors. RNG(S) is constructed in the following three steps.

- I. Compute the family F of well separated pairs of subsets of S, as described above.
- II. For each pair (P, Q) ∈ F, compute a bi-chromatic closest neighbors of each z ∈ P ∪Q. Let Ep,Q ⊂ P× Q be the set of edges (p, q) such that p is the bi-chromatic closest neighbor of q and vice-versa, and let E = ∪p.Q Ep,Q

III. Throw away the edges of E that are not the edges of RNG(S).

Steps I and II can be accomplished together by replacing the first step of Pairing(k, P, Q) with

$$\text {if } k = 0 \text { and } P , Q \neq \emptyset \text { then }$$

Compute the bi-chromatic closest neighbors of z ∈ P ∪ Q

By our assumptions on points being in general position, each point in P U Q has only constant number of bi-chromatic closest neighbors, therefore they can be computed either in time O((mVn + nVm)log(m + n)) using Voronoi diagrams, or in randomized expected time

$$O ( m ^ { 2 / 3 } n ^ { 2 / 3 } \log ^ { 4 / 3 } m + m \log ^ { 2 } n + n \log ^ { 2 } n )$$

using a more sophisticated algorithm of Agarwal et al [3] (this algorithm extends also to higher dimensions). For our purposes, the first algorithm is sufficient. Analyzing in the same way as in the previous section, one can show that Steps I and II require O(n3/2 log n) time.


<!-- p:7 -->


Re  (h    l         l ot contain a point of S. We thus need to solve the following problem. Given a set L of n lunes and a set S of m points, determine the empty lunes of L, i.e., the lunes that do not contain any point of S.

We present an algorithm based on the random sampling technique. As in most of the other random-sampling based algorithms, we first describe an algorithm that works well when n &gt; m, and then describe another algorithm, which uses the previous algorithm as a subroutine, and is efficient for all ranges of m and n.

First algorithm: The first algorithm constructs a two-level data structure, in time O(m2+ε), on S so that, for a query lune, one can determine in O(log2 n) time whether it contains any points of S in its interior. This gives an O(m3+e+ n log2 n) algorithm for filtering out the RNG edges from E. The running time can s o  ss ε  s  n  (3   + 3 a ≤[n1/3] and running the above algorithm for each subset of S separately. The data structure is based on the partitioning scheme of Chazelle et al [6]. We shall only sketch the main idea; the details can be found in the original paper.

Let S* be the set of planes dual to the points of S and let r be a suitable constant. We compute a set T of simplices with disjoint interiors, which cover the whole space and each of which intersects at most m/r planes of S*. It is known that we can find such a collection of size O(r3) in expected linear time [5]. (One can find such a collection of size O(r3log3r) by a straightforward random sampling.) For each simplex τ ∈ T, let Sν ⊆ S* denote the set of at most m/r planes intersecting the interior of τ. We recursively construct the structure on S* and store it at τ. We also store two secondary structures at τ. Let Uτ (resp. L) denote the set of points dual to the planes of S* that lie above (resp. below) τ. We preprocess U into a data structure, so that, for a query point, we can quickly determine its closest neighbor in U. Clarkson [7] has shown that a set of t points in Ra can be preprocessed in time O(tld/2+δ]), so that one can answer a closest neighbor query in O(logt) time. Therefore U can be processed in time O(|Uτ|2+δ) into a data structure that supports O(log m) time closest neighbor queries. We construct a similar structure for L. Following the same analysis as in [6], one can show that the overall time and space required by this data structure is O(m3+ ε), for any ε &gt; 0.

Let λ(p, q) be a query lune, and let hpq be the perpendicular bisector of p and q. Without loss of generality we can assume that p lies below hpq. We search the primary structure with hpq, point dual to hpq, starting from the root. We first locate the simplex t ∈ T containing the point h*q. We recursively search through the primary substructure stored at τ to determine whether any point of S, lies in the lune. Since all planes of U‡ lie above τ, and therefore above hpq, λ(p, q) contains a point of U if and only if the ball B of radius d(p, q), centered at p, contains a point of U. In other words int(λ(p, q)) ∩ Uτ ≠∅ if and only if the distance between p and its closest neighbor in Uτ is less than d(p, q). We can therefore determine, in O(log m) time, whether the interior of λ(p, q) contains a point of Uτ using the secondary structure stored at τ. Similarly, one can determine whether any point of L, lies inside λ(p, q). Since the query procedure visits O(log m) nodes of the primary structure, the total query time is O(log2 m) as required. Hence, we can conclude the following.


<!-- p:8 -->


Lemma 3.1. Given a set S of m points in R3 and a collection L of n lunes, one can determine the subset of lunes that do not contain any point of S in time O(mn2/3+ε + n1+ε).

Remark 3.2. Given a fixed k = O(1), the algorithm can be modified to determine the subset of lunes that contain less than k points of S in their interior, as follows: At each node of the primary structure, we preprocess U in such a way so that instead of just deciding the emptiness of B, we can decide whether the interior of the ball B contains at most k points of U and, if yes, we can also count the number of points of Uτ that lie in B. To this end, we preprocess U into a data structure of size O(Uτ 2+ε), so that k closest neighbors of a query point can be determined in O(k log m) time; see [2]. One constructs a similar data structure for L. We leave it for the reader to verify that with these data structures, one can determine in time O(log2 m + k log m) whether a lune contains ≥k points. The overall running time is easily seen to be O(mn2/3+ ε + n1+ε).

Second algorithm: Next, we describe the second algorithm for computing the subset of empty lunes of L. The algorithm consists of the following steps.

1. If m &lt; n1/3, then solve the problem using the previous algorithm. Otherwise, do the following.
2. Randomly choose a subset € ⊆ L of r lunes, where r is a sufficiently large constant.
3. Construct the arrangement of spheres bounding the lunes of € and decompose the arrangement into O(r3β(r)) constant size cells, where β(r) is an extremely slowly growing function. Let (€) denote the resulting subdivision.
4. For each cell τ, determine the set L of lunes whose boundaries intersect τ, and the set S ⊆ S of points that lie inside τ.
5. If S ≠Ø for some τ, then, for all lunes λ that contain τ, conclude that λ is not empty. Discard these lunes from all L.
6. If τ is a 3-dimensional cell, solve the problem recursively for L, S. If τ is a 2-dimensional cell, again solve the problem recursively using a 2-dimensional variant of the algorithm.
7. If τ is a 1-dimensional cell, we can easily determine all lunes of L that do not contain any point of S in their interior: Sort the points of S, along τ and, for each lune λ ∈ L, determine whether int(λ) ∩ τ contains any point of S. The second step can be easily done by a straight-forward binary search.
8. Output a lune λ, if none of the subproblems found a point inside λ.


<!-- p:9 -->


-Cla  snd a ai ta  hn    sno ment of r spheres into O(r3β(r)) constant size cells in time O(r3β(r)log r). Therefore Step 3 can be accomplished in time O(r3β(r)log r) time. Since r= O(1), Sr, L for all cells can be computed in linear time. Finally, the sultd (    n ms   l om-  smne Therefore, if T(m, n) denotes the maximum expected running time of the algorithm for m points and n lunes, we obtain the following recurrence

$$\arg \intertext { a n g h o n l i n f o r $ m $ p o n s $ i n d $ n $ l u n e s , $ w $ o b t a n l e $ i n o w i n g $ r e c u l r e $ e } T ( m , n ) = \begin{cases} O ( n ^ { 1 + \varepsilon } ) & \text {if $m \leqslant n^{\prime} $} , \\ O ( ( m + n ) \log n ) + \sum _ { \tau \in \mathcal { M } ( \varepsilon ) } T ( m _ { \tau } , n _ { \tau } ) & \text {if $m > n^{\prime} $} \end{cases}$$

wha   t s a  [l  su    e l ieles

$$E \left [ \sum _ { \tau \in \mathcal { A } ( \mathcal { C } ) } n _ { \tau } \right ] = O ( n r ^ { 2 } \beta ( r ) )$$

$$E \left [ \sum _ { \tau \in \mathcal { A } ( \mathcal { C } ) } m _ { \tau } n _ { \tau } ^ { 2 / 3 } \right ] = O \left ( m \frac { n ^ { 2 / 3 } } { r ^ { 2 / 3 } } \right ) .$$

It is known that the solution of the above recurrence is O(m3/4+ εn3/4 + n1+ε + m log2 n); see [1] for a proof. Hence, we obtain the following theorem.

Theorem 3.3. Given a set S of m points in R3 and a set L of n lunes, one can compute, in randomized expected time O(m3/4+ εn3/4 + n1+ε + m log2 n), the lunes of L that do not contain any point of S in their interior.

Remark 3.4. As earlier, we can modify this algorithm to determine, in randomized expected time O(m3/4n3/4+εn1+ε), the lunes of L that contain less than k points of S in their interior.

Going back to the problem of computing RNG(S), since we have n points and O(n) lunes, the above theorem immediately implies the following theorem.

Theorem 3.5. Given a set S of n points in R3 in general position, one can compute its relative neighborhood graph by a randomized algorithm, whose expected running time is O(n3/2+ ε).

Remark 3.6. A r-element subset € with properties needed in Step 2 of the above algorithm can be computed deterministically in time O(n) by an algorithm of [18], which implies that RNG(S) can be computed deterministically within the same time bound as mentioned in the above theorem.

The algorithm for computing the set of empty lunes can be extended to higher dimensions as in [1, 3]. The result is that in Ra, one can find the lunes that do not

and contain any points of S in time


<!-- p:10 -->


$$O ( m ^ { d / ( d + 1 ) } n ^ { d / ( d + 1 ) + \varepsilon } + m \log ^ { 2 } n + n ^ { 1 + \varepsilon } ) ,$$

which yields

Theorem 3.7. Given a set S of n points in Rd in general position, one can compute RNG(S) in time O(n2(1−1/(d+1))+ε).

## 4. Computing RNG: the general case

If the points of S are not in general position, a point can have several closest neighbors. Consequently, we cannot afford to compute all bi-chromatic closest neighbors for each point z ∈ P ∪ Q. Instead we compute all symmetric bi-chromatic closest neighbor pairs of (P, Q) by replacing step II of the previous algorithm with the following step.

II'. For each pair (P, Q) ∈ F do the following:

II'.a For each point z ∈ P∪ Q, compute the distance between z and its bi-chromatic closest neighbor; let δz denote this distance.

II'.b For each p ∈ P, determine the points q ∈ Q such that d(p, q) = δp and δq = δp. Let Ep.o denote the resulting set of pairs, i.e.,

$$E _ { P , Q } = \{ ( p , q ) \in P \times Q \, | \, d ( p , q ) = \delta _ { q } = \delta _ { p } \} .$$

In view of Lemma 2.1, RNG(S) is a subgraph of G = (S, ∪(P.Q)∈ Ep,Q). By Corollary 2.3, G has only O(n43) edges. After having computed G, we can use the same algorithm as earlier to prune the edges of G that are not in RNG(S). Since there are O(n43) lunes and n points, by Theorem 3.3, step III will require O(n7/4+ ε) time.

Going back to step II', δ2 for every z ∈ P ∪ Q can be computed in time O(n3/2 log n) as earlier. So we only have to show how to compute the set Ep,o assuming that we know the value of δ2 for all z ∈ P ∪ Q.

Let Qβ = {q ∈ Q | δq = β}. We process each of Qβ a follows. We map Qβ to a st         =        pd  o the hyperplane

$$\varphi ( q ) \colon x _ { 4 } = 2 q _ { 1 } x _ { 1 } + 2 q _ { 2 } x _ { 2 } + 2 q _ { 3 } x _ { 3 } - ( q _ { 1 } ^ { 2 } + q _ { 2 } ^ { 2 } + q _ { 3 } ^ { 2 } ) .$$

We process the upper envelope of φ(Qβ), in time O(m2+ε), so that, for a query point ξ, one can determine all k hyperplanes of φ(Qβ) containing ξ in time O(log n + k). This can be easily done by modifying the algorithm of Clarkson [7].

For every point p ∈ P, we first determine whether the set Qs is empty. If not, we report the points q ∈ Qs, for which  ̄ = (p1, P2, P3, p2 + p2 + p3 − δ2) lies on the hyperplane φ(q). Since d(p, q) ≥ δp, for all q ∈ Qs, none of the hyperplanes of φ(Qs) lie above ē, i.e., ē lies in the upper envelope of Qδ,. Therefore, we can report all k points q with d(p, q) = δp, in time O(log n + k), using the above structure. Let K be the total number of points returned by the above procedure, then the total running time is O(m2+ε + n log m + K). This can be improved to O(mn1/2+ ε + n1+ε + K) using the batching technique similar to the one used in the first algorithm of the previous section. By Corollary 2.3, K = O(m2/3n2/3 + m + n). Consequently, Ep.Q can be computed in time O(mn1/2+εn1+ε). Repeating this procedure over all pairs (P, Q) ∈ F, we obtain the graph G, in time O(n3/2+ ε). Hence, we can conclude Theorem 4.1. Given a set S of arbitrary n points in R3, we can construct RNG(S) in time O(n74+ε).


<!-- p:11 -->


Remark 4.2. (i) The time required to construct the graph G can be further improved to O(n4/3+ε) by using the random sampling technique as for step III in the previous section, but for our purpose this algorithm is good enough.

(ii) If the upper bound on the number of bi-chromatic closest pairs between two sets of points, with n points in each set, can be improved to τ, one can compute RNG(S) in time O(τ3/4 n3/4+ ).

## 5. k-Relative neighborhood graphs

The k-relative neighborhood graph of S, denoted k-RNG(S), is a generalization of RNG(S). In particular, (p, q) is an edge of k-RNG(S) if λ(p, q) contains less than k points of S. For k = O(1), Chang et al [4] have proposed an O(n2) algorithm to compute k-RNG(S) in R2, which has been improved by Su and Chang to O(n5/3 log n) [21]. It is known that Euclidean bottleneck matching problem, i.e., given a set S of points find an Euclidean matching that minimizes sh s  e  - s  s    s her Euclidean bottleneck problems can also be reduced to computing k-relative neighborhood graphs.

In this section we present efficient algorithms for computing the k-relative neighborhood graph of a set of points. Let us begin by an easy consequence of Theorem 2.4.

Theorem 3.5. Given a set S of n points in R2 (resp. R3), the k-RNG(S) has O(nk) (resp. O(n4/3k2/3)) edges.

Proof. The proof is based on a method due to Clarkson [9]. Rather than explaining the general theory from which the result directly follows, we just give the specific application. Let Mk denote the number of edges of k-RNG(S). Choose a random r-element subset R ⊆ S, where r = [n/k] and each r-element subset of S is chosen with equal probability. Let Pp,q denote the probability that an edge (p, q) ∈ k-RNG(S) is an edge of RNG(R). An edge (p, q) of k-RNG(S) will be an edge of RNG(R) if the following two conditions are satisfied.


<!-- p:12 -->


- (i) Both p, q are chosen into R, and
- (ii) none of the (at most k) points of S∩ λ(p, q) belong to R.

Therefore

$$\mathbf P _ { p , q } \geqslant \begin{pmatrix} n - k - 2 \\ r - 2 \end{pmatrix} \Big / \begin{pmatrix} n \\ \binom { n } { r } \geqslant \frac { c } { k ^ { 2 } } \, , \end{pmatrix}$$

wh e ns    nt    s   us

$$E [ | R N G ( R ) | ] \geqslant \sum _ { ( p , q ) \in k \cdot R N G ( S ) } \mathbf P _ { p , q } \geqslant \frac { c } { k ^ { 2 } } \, M _ { k } .$$

But RNG(R) can have only O(r43) edges in R3 (cf. Theorem 2.4), which implies Mk = O(n4/3k2/3).

A similar argument shows that Mk = O(nk) in R2. □

In this section, we obtain efficient algorithms for computing k-RNG(S), for k = O(1), by modifying the algorithms described in the previous sections. We shall describe only the main idea.

For a point p, let Φk(p, Q) ⊆ Q denote the set of points q such that d(p, q) is less than or equal to the distance between p and its kth closest neighbor in Q. Following the same argument as in Lemma 2.1, one can show that if P, Q are well separated, then k-RNG(P ∪ Q) has a cross edge (p, q) only if q ∈ Φk(p, Q) and p ∈ Φk(q, p). Hence, we can modify the algorihtm of Section 3 as follows.

- I. Compute the family F of well separated pairs of subsets of S, as described above.
- II. For each pair (P, Q) ∈ F, compute Φk(p, Q), for every p ∈ P, and Φk(q, P), for every q ∈ Q. Let Ep.ρ⊂ P× Q be the set of edges (p, q) such that p ∈ Φk(q, P) and vice-versa. Let G = (S, ∪(P,Q)∈ Ep.Q).
- III. Throw away an edge (p, q) of G if λ(p, q) contains ≥k points of S.

Aasinr s  r r r  r assng (n ≤s ≤n2), one can compute Φk(p, Q), in time O(n1+ε/√s) [2]. Setting st     '( ) d   sd  s  +  + ε = s O(m2/3n2/3+ ε + m + n) (recall that k = O(1)). Thus, the total time spent in steps I and II is O(n4/3+ ε). Finally in view of Remark 3.4, the edges of G that are not in k-RNG(S) can be determined in time O(n3/2+ε). Hence, if points of S are in general position, k-RNG(S) can be computed in time O(n3/2+ ε). As in Section 3, the same algorithm can compute k-RNG(S) in Ra in time O(n2(1−1/(d+1))+ε).


<!-- p:13 -->


Using Theorem 5.1, and an appropriate modification of the algorithm of Section 4, we can compute k-RNG(S) in time O(n43+ ε) (resp. O(n7/4+ ε)) for d = 2 (resp. d = 3).

Hence, we can conclude the following theorem.

Theorem 5.2. Given a set S of n points in Ro in general position and a fixed constant k, one can compute k-RNG(S) in time O(n2(1−1/(d+1))+ε). If points of S are arbitrary, k-RNG(S) can be computed in time O(n4/3+ ε) (resp. O(n7/4+ ε)) for d = 2 (resp. d = 3).

## 6. Conclusion

In this paper, we describe efficient algorithms for computing relative neighborhood graphs and k-relative neighborhood graphs in Ra. Our algorithms work for larger values of k too, but analysis of the running time becomes complicated. Moreover, in most of the applications k is some fixed constant.

-  nr  i n n d     b chromatic closest pairs between a set of m points and another set of n points in R3?"
