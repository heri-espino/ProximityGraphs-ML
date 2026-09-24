---
id: "Giesen-Wagner_2004_Shape-Dimension-Intrinsic-Metric-Manifolds"
source_pdf: "../pdf/Giesen-Wagner_2004_Shape-Dimension-Intrinsic-Metric-Manifolds.pdf"
source_filename: "Giesen-Wagner_2004_Shape-Dimension-Intrinsic-Metric-Manifolds.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "full-page-ocr"
extraction_quality: "excellent"
extraction_score: 100.0
visual_assets: "disabled"
references_file: "../references/Giesen-Wagner_2004_Shape-Dimension-Intrinsic-Metric-Manifolds.references.md"
---

<!-- p:1 -->

Discrete Comput Geom 32:245–267 (2004) DOI: 10.1007/s00454-004-1120-8

Geometry

Discrete &amp; Computational

© 2004 Springer-Verlag New York, LLC

### Shape Dimension and Intrinsic Metric from Samples of Manifolds*

Joachim Giesen and Uli Wagner

Institut für Theoretische Informatik, ETH Zürich, CH-8092 Zürich, Switzerland {giesen,uli}@inf.ethz.ch

Abstract. We introduce the adaptive neighborhood graph as a data structure for modeling a smooth manifold M embedded in some Euclidean space Rd. We assume that M is known to us only through a finite sample P ⊂ M, as is often the case in applications. The adaptive neighborhood graph is a geometric graph on P. Its complexity is at most min{2o(k)n, n2}, where n = |P| and k = dim M, as opposed to the n[d/2] complexity of the Delaunay triangulation, which is often used to model manifolds. We prove that we can correctly infer the connected components and the dimension of M from the adaptive neighborhood graph provided a certain standard sampling condition is fulfilled. The running time of the dimension detection algorithm is d2o(kτlog k) for each connected component of M. If the dimension is considered constant, this is a constant-time operation, and the adaptive neighborhood graph is of linear size. Moreover, the exponential dependence of the constants is only on the intrinsic dimension k, not on the ambient dimension d. This is of particular interest if the co-dimension is high, i.e., if k is much smaller than d, as is the case in many applications. The adaptive neighborhood graph also allows us to approximate the geodesic distances between the points in P.

## 1. Introduction

Manifold learning is the problem of computing a model of a k-dimensional manifold M embedded in d-dimensional Euclidean space Rd only from a finite set P of sample points. Often k is very small compared with d.

The manifold learning problem was identified as one of the most important and challenging problems in computational topology during an NSF founded workshop on computational topology [7]. The importance of the problem can be stressed by its many applications, e.g., in speech recognition, weather forecasting, and economic prediction.

* The first author was partially supported by the Swiss National Science Foundation under the project "Non-linear manifold learning".


<!-- p:2 -->


The term manifold learning was introduced in 1995 in the context of speech understanding [9], [10]. However, the problem also appeared in research on neural networks [17] and in mathematical psychology [19]. In all these areas heuristics were developed to address the problem, but so far no theoretical correctness guarantees could be proven.

Special cases of the manifold learning problem in low dimensions received a lot of attention in recent years. Most prominent is the surface reconstruction problem where P is sampled from a two-dimensional manifold embedded in three-dimensional space. The surface reconstruction problem as described here is also special in the sense that the co-dimension of the problem, i.e., d — k, is one. Some of the proposed algorithms for curve and surface reconstruction [2]–[4], [1 1] come with the guarantee that the computed model is a manifold homeomorphic and geometrically close to the unknown manifold M provided some sampling condition is fulfilled. These algorithms are called provably correct. Almost all known provably correct algorithms for surface reconstruction use the three-dimensional Delaunay triangulation or the Voronoi diagram of the sample points as a basic data structure. Unfortunately the time to compute the Delaunay triangulation or the Voronoi diagram in dimension d is of the order n[d/2] in the worst case, where n = |P| is the number of sample points.

o es- st e  xs ot  eit , st at ses or and recently it was shown [6], [13] that for points that are ""nicely distributed" on a smooth surface in R3, the Delaunay triangulation has complexity much lower than n2 (see [13] for an excellent survey of the different ways to specify "nice" and of related work). Observe, however, that exponential growth in the co-dimension is inevitable: As the simplest example, consider k mutually orthogonal unit circles centered at the origin in R2k. Even if we take n/ k evenly spaced points on each of the circles, the complexity of the Delaunay triangulation will be Ω(nk). Because of this exponential growth of the running time, the use of the Delaunay triangulation is prohibitive for high co-dimensions.

Even though the provably correct algorithms for curve and surface reconstruction cannot be adapted directly for use in higher dimensions, many of the ideas developed for their correctness proofs can. Especially interesting are the sampling conditions used in the proofs. Amenta and Bern [2] introduced the notion of an ε-sample, which can be defined in arbitrary dimensions and allows for non-uniform sampling. Later, the ε-sampling condition was specialized in [12] and [14] to the so-called (ε,δ)-sampling condition. We review these sampling conditions in Section 2, and then work with the (ε, δ)-sampling condition.

In this paper we introduce the adaptive neighborhood graph. The adaptive neighborhood graph is a geometric graph on the sample P and can be computed in time O(n2), wit   o ood     s l p   d ie manifold M in the following sense:

- (1) If the sample P satisfies an (ε, δ)-sampling condition, then the adaptive neighborhood graph has the same connectivity as the manifold M, i.e., the points in P that are connected by a path in M are also connected by a path in the adaptive neighborhood graph and vice versa.
- (2) Under the sae sampling condition we can correctly infer the dimension k of M in time d20(k7 log k) for each connected component. If the dimension is considered


<!-- p:3 -->


- a constant, then this is a constant-time operation, and, moreover, the exponential dependence of the constants is only on k and not on d. This improves a result of Dey et al. [12] who gave a dimension detection algorithm which is provably correct under the same sampling condition and is based on the d-dimensional Delaunay triangulation, i.e., requires time Θ(n[a/21) in the worst case. Dey et al. also provide an example that the sampling condition cannot be weakened essentially.
- (3) The geodesic distance between two sample points on M can be approximated by the length of the shortest path that connects them in the adaptive neighborhood -rx   tt s td   a s at o  ao oxi mate geodesic distances. This also improves an early result: Tenenbaum et al. [19] suggest two different graphs models: either they connect two points if they are at a distance of no more than some global threshold, or they use a fixed number of nearest neighbors around each point. The disadvantage of the first method is that it requires a much stricter sampling condition (globally uniform samples). The second graph, on the other hand, does not automatically adapt to the dimension of M. While for various input models (such as (ε, δ)-samples reviewed below, or uniform random sample points), one can show that there is a number m, depending on the model and the intrinsic dimension k, such that considering the m nearest neighbors works well for that model and that k, this number would have to be a parameter of the algorithm, to be interactively adjusted by the user for each particular input.

## 2. Sampling and the Adaptive Neighborhood Graph

Let M = {M1 , . . . , Mm } be a collection of disjoint, smooth (C2 would be enough), compact, and connected manifolds embedded in Rd and let M = Ui=1 Mi be the underlying topological space of M. We do not assume that all the manifolds M ∈ M have the same dimension, but we assume that all the manifolds M have dimension larger than zero. Note that we assume our manifolds to have no boundary.

For p ∈ M, we denote by TpM the tangent space of M at p, and by NpM the space of normals. The tangent space Tp M is the set of tangent vectors at p of all smooth curves in M passing through p. If the dimension of M is k, then Tp M is a k-flat containing p. The space of normals NpM is the orthogonal complement of TpM. (We picture both spaces to be anchored at p.)

If we are to infer any useful information about M from a finite sample P ⊂ M, the sample has to fulfill some sampling condition. Following [2] we base the sampling condition on the medial axis of M.

Medial Axis and Local Feature Size. A d-dimensional ball B is called a medial ball of M if int(B) ∩ M = ∅ and |bd(B) ∩ M| ≥ 2, i.e., B does not contain any point of M in its interior but at least two points of M in its boundary. The medial axis of M is the closure of the set of all medial ball centers.

The local feature size is the function f: M → R that assigns to x ∈ M its distance to the medial axis. The following observation was made in [2].


<!-- p:4 -->


Lemma 1. The feature size f: M → R satisfies:

- (i) f(x) ≤ f(y) + ∥x − y∥.
- (ii) If ∥x − y∥ ≤ εf (x) with ε &lt; 1, then

$$\| x - y \| \leq \frac { \varepsilon } { 1 - \varepsilon } f ( y ) .$$

In what follows, we assume that f (x) &lt; ∞ for all x ∈ M. Observe that it follows from smoothness that f (x) &gt; 0.

Most algorithms learning properties of M from a sampling P are based on the assumption that P is a uniform sample. This assumption is quite strict. It means that the sampling density is globally determined by the smallest feature exhibited by M. We use the feature size to define less restrictive sampling conditions.

Sampling Conditions. Let ε &gt; 0. A finite sample P ⊂ M is called an ε-sample if

$$\forall x \in M , \ \exists p \in P , \quad \| x - p \| \leq \varepsilon f ( x ) .$$

An ε-sample P is called an (ε, δ)-sample or tight ε-sample if it satisfies the additional condition

$$\forall p , q \in P , \quad \| p - q \| \geq \delta f ( p )$$

for some δ, 0 &lt; δ &lt; ε.

The ε-sampling condition was introduced by Amenta et al. in the context of curve and surface reconstruction [2]. The tight ε-sampling condition was introduced by Dey et al. for dimension detection from samples [12] and by Funke and Ramos for fast surface reconstruction [14].

The fundamental data structure that we use later is the adaptive neighborhood graph.

Adaptive Neighborhood Graph. For a constant c &gt; 1 we define the c-neighborhood Nc(p) of a sample point p ∈ P as follows:

$$N _ { c } ( p ) = \left \{ q \in P - \{ p \} \ \colon \| p - q \| \leq c \min _ { q ^ { \prime } \in P - \{ p \} } \| p - q ^ { \prime } \| \right \} .$$

The adaptive neighborhood graph Gc(P) is the geometric graph with vertex set P where two vertices p, q ∈ P are connected by a straight edge if either q ∈ Nc(P) or p ∈ Nc(q).

## 3. Connectivity

In this section we show that for a suitable choice of c and all sufficiently small ε, δ &gt; 0 such that the ratio δ/ε is at least some suitable constant, the adaptive neighborhood graph G(P) of any (ε, δ)-sample P of M has essentially the same connectivity as M. That is, two points in P are connected by a path in M if and only if they lie in the same connected component of Gc(P).


<!-- p:5 -->


We start by proving an upper bound on the distance of a sample point from its nearest neighbor in the set of sample points. Moreover, we establish an upper bound on the length of restricted Delaunay edges. The Delaunay triangulation of P restricted to M is the dual complex of the restricted Voronoi diagram of P. That is, the convex hull of sample points p1, . . . , Pk ∈ P belongs to the restricted Delaunay triangulation iff the intersection M ∩ ∩k=1 Vpi is non-empty, where Vp := {x ∈ Rd : ∥x − p∥ = minq∈P ∥x − q∥} is the Voronoi cell of a sample point p.

Lemma 2. Let P be an ε-sample of M with ε &lt; 1. Then the following hold:

- (i) The distance between p ∈ P and its nearest neighbor in P\{p} is at most (2ε/(1 − ε))f(p).
- (ii) If p, q ∈ P and if pq is an edge of the restricted Delaunay triangulation, then ∥p − q∥ ≤ (2ε/(1 − ε)) min{ f (p), f (q)}.

Proof. Let Vp be the Voronoi cell of p. We first show that the boundary of Vp must have a non-empty intersection with the component M of M containing p.

Otherwise, M has to be completely contained in the interior of Vp and p is the only sample point on M. By compactness, there exists a point x ∈ Mi whose distance to p is maximal. Observe that the tangent space Tx M must be orthogonal to the segment xp, else a suitable small perturbation would produce a point even farther away from p. Thus, there exists a ball B of radius f (x) that is tangent to x and whose center lies on the ray from x through p. The interior of B contains no point from M, in particular, the distance from p to x is at least the diameter of B, i.e., ∥x — p∥ ≥ 2 f (x). Thus, if p is the only sample point on M, then S is not an ε-sample.

Thus, we can assume that Vp contains a point y ∈ M in its boundary. From ∥y — p∥ ≤ εf (y) and the property of the local feature size stated in Lemma 1(ii) we conclude that

$$\| y - p \| \leq \frac { \varepsilon } { 1 - \varepsilon } f ( p ) .$$

Since y is contained in the boundary of Vp there must exist another point q ∈ P\{p} such that y is also contained in the boundary of the Voronoi cell Vq. We have

$$\| p - y \| = \| q - y \| \geq \frac { \| p - q \| } { 2 }$$

$$\| p - q \| \leq 2 \| p - y \| \leq \frac { 2 \varepsilon } { 1 - \varepsilon } f ( p ) .$$

Hence p has a neighbor in P\{p} within distance at most (2ε/(1 − ε)) f (p). This proves the first claim. Note that the edge pq is a restricted Delaunay edge. In general we have for any restricted Delaunay edge pq that the common intersection of M with the Voronoi regions Vp and Vq is not empty. Thus we can use the same calculations as above to prove also the second claim. □

and thus Corollary 1. Let P be an (ε, δ)-sample of M. If pq with p, q ∈ P is an edge in the Delaunay triangulation of P restricted to M, then


<!-- p:6 -->


$$p \in N _ { c } ( q ) \quad a n d \quad q \in N _ { c } ( p ) , \quad p r o v i d e d \quad c \geq \frac { 2 \varepsilon } { ( 1 - \varepsilon ) \delta } .$$

Proof. Lemma 2(ii) together with the δ-condition satisfied by P gives

$$2 ( \tt n ) \log \text {cylinder with the $0$-condition satisfied by $1$-gives} \\ \| p - q \| & \leq \frac { 2 \varepsilon } { 1 - \varepsilon } f ( p ) \\ & \leq \frac { 2 \varepsilon } { ( 1 - \varepsilon ) \, \delta } \min _ { p ^ { \prime } \in P - \{ p \} } \| p - p ^ { \prime } \| \\ & \leq c \cdot \min _ { p ^ { \prime } \in P - \{ p \} } \| p - p ^ { \prime } \| .$$

That shows q ∈ Nc(p). Analogously it follows that p ∈ Nc(q).

□

Now we will show that the adaptive neighborhood graph cannot connect sample points from different connected components of M.

Lemma 3. Let P be an ε-sample of M. The adaptive neighborhood graph Gc(P) contains no edge that connects different connected components of M provided ε &lt; 1 and c &lt; (1 − ε)/2ε.

Proof. Let p, q ∈ P be two sample points that are sampled from two different connected components of M. That is, the line segment pq connects two disjoint connected components of M. Assume p ∈ Mi ∈ M and consider the following continuous function on the pq:

$$g \colon p q \to \mathbb { R } , \, x \mapsto \text {dist} ( x , M _ { i } ) - \text {dist} ( x , M \rangle M _ { i } ) .$$

By construction we have g(p) &lt; 0 and g(q) &gt; 0. The continuity of g implies that there exists at least one point x' ∈ pq with g(x′) = 0. The point x′ has to be a point of the medial axis of M. Hence we have

$$f ( p ) , f ( q ) \leq \| p - q \| .$$

Let p′ be the nearest neighbor of p in P\{p}. From our assumption on c and Lemma 2(i) we get

$$c \| p - p ^ { \prime } \| \leq \frac { 2 c \varepsilon } { 1 - \varepsilon } f ( p ) < f ( p ) \leq \| p - q \| .$$

By an analogous reasoning we also have, for the nearest neighbor q′ of q in P\{q},

$$c \| q - q ^ { \prime } \| \leq \frac { 2 c \varepsilon } { 1 - \varepsilon } f ( q ) < f ( q ) \leq \| p - q \| .$$

That is, the line segment pq cannot be an edge of any adaptive neighborhood graph Gc(P) for ε &lt; 1 and c &lt; (1 − ε)/2ε. □


<!-- p:7 -->


Now we are ready to prove that the adaptive neighborhood graph has to be connected for each subset of sample points that belong to one connected component of M.

Lemma 4. Let P be an (ε, δ)-sample of M and let Gc[P ∩ M] be the subgraph of the adaptive neighborhood graph Gc(P) induced by P ∩ M. The graph Gc[P ∩ M] is connected for every connected component Mi ∈ M of M provided ε &lt; 1 and

$$\frac { 2 \varepsilon } { ( 1 - \varepsilon ) \delta } \leq c \leq \frac { 1 - \varepsilon } { 2 \varepsilon } .$$

Proof. The restricted Delaunay graph on P is the intersection graph of the restricted Voronoi cells of the points in P. Let G be the induced subgraph on P∩M of the restricted Delaunay graph. It suffices to show that G is connected. The proof then follows from Corollary 1.

Let G' be a connected component of G and assume that G′ ≠ G. Let P′ ⊂ P be the vertex set of G' and let F be the set of all Voronoi facets shared by Voronoi cells of points from P' and P\P'. By construction the set F is not empty and the intersection

$$\bigcup _ { f \in \mathcal { F } } f \cap M _ { i }$$

cannot be empty either since the collection of all Voronoi cells of points in P' do not cover the whole of M. That is, there exists a point x ∈ M that is contained in the intersection Vp ∩ Vq where Vp is the Voronoi cell of a point p ∈ P' and Vq is the Voronoi cell of a point q ∈ P\P'. We know from Lemma 3 that q has to be a sample point of M, i.e., a vertex in the complement of G' in G. Hence the straight edge pq has to be a restricted Delaunay edge connecting a vertex p in G' with a vertex q in the complement of G' in G. That is a contradiction. □

We summarize our findings in the following theorem.

Theorem 1. Let P be an (ε, δ)-sample of M. The adaptive neighborhood graph Gc(P) has the same connectivity as M, provided ε &lt; 1 and

$$\frac { 2 \varepsilon } { ( 1 - \varepsilon ) \delta } \leq c \leq \frac { 1 - \varepsilon } { 2 \varepsilon } .$$

That is, two points p, q ∈ P are connected by a path in M if and only if they are connected by a path in Gc(P).

Note that the assumptions stated in the theorem are fulfilled if δ/ε is bounded from below by a suitable constant ρo &gt; 0 and ε is sufficiently small. For example ε ≤ 1 will do.

## 4. Dimension Detection

In this section we present an algorithm which detects the local dimension of M at a sample point p, i.e., the dimension of the component of M that contains p. In contrast to reconstruction of the connectivity, dimension detection is a local task. We exploit this fact by considering only the set Nc(p) instead of all neighbors of p in the adaptive neighborhood graph.


<!-- p:8 -->


Here is a rough outline of our strategy: First we show that for a suitable choice of c and all sufficiently small ε, δ &gt; 0 such that δ/ε is bounded from below by a suitable constant, the following holds:

If P is an (ε, δ)-sample from M and if p ∈ P, then, on the one hand, all points q ∈ Nc(P) lie very close to the tangent space TpM of M at p, while, on the other hand, for any affine subspace L through p with dim L &lt; dimp M, there is some q ∈ Nc(P) that is quite far away from L.

These findings give rise to an algorithm to determine the dimension of the manifold Mi ∈ M that contains p: Starting with l = 1, we apply an algorithm by Har-Peled and Varadarajan [15] to compute a 1.99-approximation L of the best-fit l-dimensional affine subspace through p for the set Nc(P). We will see that for all suitable samples, the distance

$$\max _ { q \in N _ { c } ( P ) } \inf _ { x \in L } \| x - q \|$$

is larger than some threshold if l &lt; k and it is at most 1.99/2 times this threshold if l ≥ k. Hence, the smallest l for which the maximum of the distances from L is smaller than the threshold gives us the dimension of the manifold Mi ∈ M that contains p.

We now make our strategy precise through a series of lemmas.

Lemma 5. Let p ∈ M and u ∈ NpM, ∥u∥ = 1. Then the ball B of radius f (p) centered at p + f (p)u does not contain any points from M in its interior.

Proof. For ρ &gt; 0, consider the ball Bρ of radius ρ centered at p + ρu. We have Bρ ⊆ Bρ′ whenever ρ ≤ ρ′, and since the balls Bρ are tangent to M at p they do not contain points from M in their interior if ρ is sufficiently small. Let r := sup{ρ &gt; 0 : int Bρ ∩ M = ∅}. Then intB, ∩ M = ∅, and there is a point q ∈ M such that q ∈ bdB, and q ∈ intBρ for every ρ &gt; r. In particular, q ≠ p, so the center m of B, belongs to the medial axis, and hence r = ∥m − p∥ ≥ f (p). □

Lemma 6 (Small Angle Lemma). Let p ∈ M and consider q ∈ M with ∥p − q∥ = t f (p), 0 &lt; t &lt; 1. Then for every non-zero normal vector u ∈ NpM, the distance from q to the hyperplane p + u− satisfies

$$\text {dist} ( q , p + u ^ { \perp } ) \leq \frac { t ^ { 2 } } { 2 } f ( p ) .$$

In other words, the angle α between the segment pq and the tangent space TpM satisfies

$$\sin \alpha \leq \frac { t } { 2 } .$$

Proof. If q ∈ p + u−, we are done. Otherwise, there is a unique d-dimensional ball B which is tangent to p + u− at p and contains q on its boundary. Let m and r be the center


<!-- p:9 -->

B

m

b

q

u⊥

a

p

Fig. 1. The component of q − p in any normal direction is small.

and the radius of B, respectively (if ∥u∥ = 1 and (q − p, u〉 &gt; 0, then m = p + ru). We have r ≥ f (p) (else q would be contained in the interior of the ball B′ of radius f (p) centered at p + f (p)(u/∥u∥), contradicting Lemma 5). Let a be the orthogonal projection of q onto p + u+, and let b := 1(p + q). Observe that the triangles pqa and mpb are similar (see Fig. 1), whence

$$\frac { \| q - a \| } { \| p - q \| } = \frac { \| p - q \| / 2 } { r } .$$

Therefore, ∥q − a∥ = t2 f (p)2 /2r ≤ (t2/2) f (p), as desired. Finally, for the last part of the assertion, either q ∈ TpM, in which case α = 0, or we can let a be the orthogonal p −  = n  () d      o id □

The previous lemma states that if we start from p ∈ M and move by at most t f (p) on the manifold, then there is a point on the tangent space that is very close, namely, at distance at most t2 f (p). We now consider the reverse of this statement: If we start from a point p ∈ M and move by a sufficiently small amount t in direction of a unit tangent vector v ∈ TpM, then there exists a point q ∈ M very close to p + tv, namely, ∥p + tv − q∥ = O(t2). The following lemma specifies "sufficiently close" and the implicit constant in terms of the local feature size.

Lemma 7 (Close Point Lemma). Let p ∈ M and v ∈ TpM, ∥v∥ = 1. For 0 &lt; t &lt; 1, let a(t) := p + t f (p) · v, and let q(t) be the point on M closest to a(t) (which is unique since ∥p − a(t)∥ &lt; f (p)). If t ≤ t0 for some absolute constant t0 (t0 = works, for 4 instance), then

$$\| a ( t ) - q ( t ) \| < 2 t ^ { 2 } f ( p ) .$$

We note that the constant factor of 2 for t2 in (2) is somewhat arbitrary, any other constant strictly greater than will do if we adjust t0 accordingly. 2

Proof. We proceed in two steps. We first prove that by general principles, (2) holds if t is sufficiently small, without being able to specify what exactly "sufficiently small" means. In the second step we show that if t ≤ t0 violates (2), then so does t′ := t /(1 + t).


<!-- p:10 -->


Therefore, if there existed some violator t ≤ t0, there would in fact be a whole sequence t, t′, t′′, t′", . . . of violators. Moreover, this sequence would converge to 0 (if t ≤ 1/n, then t′ ≤ 1/(n + 1)), eventually leading to a contradiction to what we proved in the first step.

1. Consider the geodesic γ through p on M in direction v. We assume that γ is parametrized by arc length and such that γ (0) = p. It follows that γ(0) = v and that j(0) ⊥ v. Moreover, since γ is a geodesic, ¿(0) ⊥ w for all tangent vectors w ∈ TpM which are themselves orthogonal to v, see [16]. Therefore, γ (0) ∈ NpM.

By Taylor's formula, we have

$$\gamma ( s ) = \underbrace { \gamma ( 0 ) + s } _ { p } \dot { \gamma } ( 0 ) + \frac { s ^ { 2 } } { 2 } \ddot { \gamma } ( 0 ) + r ( s ) ,$$

where ∥r(s)∥/s2 → 0 (but we do not know how fast) as s → 0. It follows that ∥j (0)∥ ≤ 1/f (p), otherwise for sufficiently small s, γ(s) ∈ M would contradict Lemma 6 (applied with u = γ (0) and t = s/ f (p)). Hence, if we choose t so small that( ( () f t &gt; l() ft).t ten

$$\| a ( t ) - q ( t ) \| \leq \| p + t f ( p ) \cdot v - \gamma ( t f ( p ) ) \| < 2 t ^ { 2 } f ( p ) ,$$

which completes the first step.

2. Assume then that t ≤ t0 violates (2). We want to show that t′ := t/(1 + t) is a violator as well. Without loss of generality, we may assume that f (p) = 1. For simplicity, we write a := a(t), q := q(t), and a′ := a(t′). Observe that since q is the point on M closest to a, the (non-zero) vector a − q is orthogonal to Tq M, and so is the unit vector u := (a − q)/∥a − q∥. Therefore, for any r ≤ f (q), the as t   ot  o +  =:     st   on its interior. Thus, in order to prove that t′ is again a violator, it is enough to show that for a suitable r to be specified below, the distance from a' to the boundary of B is at least 2(t′)2, i.e.,

$$\| a ^ { \prime } - m \| ^ { 2 } \leq ( r - 2 ( t ^ { \prime } ) ^ { 2 } ) ^ { 2 } .$$

∥ b − p| =  ə    · s (n  − p〉 =:  p 〈n  − d〉 =: x 1 ∥ p − a∥ = t (and also y ≥ 2t2, since t is a violator). Thus, as a first estimate, we get∥ p − q∥ ≤ ∥p − a∥ + ∥a − q∥ ≤ 2t, and so f(q) ≥ 1 − 2t.

Since u is orthogonal to Tq M and ∥p − q∥ ≤ 2t ≤ 1 − 2t ≤ f (q), we can apply Lemma 6 and conclude

$$| x | \leq \frac { \| p - q \| ^ { 2 } } { 2 f ( q ) } .$$

Observe that the projection of q – p onto u+, which is the same as the projection of a − p, has length √t2 − (y − x)2. Therefore,

$$\| p - q \| ^ { 2 } = x ^ { 2 } + t ^ { 2 } - ( y - x ) ^ { 2 } ,$$


<!-- p:11 -->


Fig. 2. t′ is again a violator.

B

√t2 − (y − x)2

m

a

a′

r

y

q

p

hence x ≤ (t2 − y2 + 2xy)/2 f (q), i.e., x(1 − y/ f (q)) ≤ (t2 − y2)/2 f (q). Since y ≤ t &lt; f (q), it follows that

$$x \leq \frac { t ^ { 2 } - y ^ { 2 } } { 2 f ( q ) - 2 y } .$$

This is at most y/2 because yf (q) ≥ 2t2(1 − 2t) ≥ t2 for t ≤ 1. Together with (6), x ≤ y/2 implies ∥p − q∥ ≤ t, so in fact f (q) ≥ 1 − t. Therefore, we can set

$$r \colon = 1 - t .$$

It remains to verify (4). By definition of t′, we have t — t′ = tt′, so we can write a′ − m = a − m − tt′v = a − m − t′(a − p). Therefore, by decomposing a′ − m into its components in direction u and in u+, respectively, we obtain

$$\| a ^ { \prime } - m \| ^ { 2 } & = ( r - y + t ^ { \prime } ( y - x ) ) ^ { 2 } + ( t ^ { \prime } ) ^ { 2 } ( t ^ { 2 } - ( y - x ) ^ { 2 } ) \\ & = r ^ { 2 } - 2 r y + y ^ { 2 } + 2 t ^ { \prime } ( r - y ) ( y - x ) + t ^ { 2 } ( t ^ { \prime } ) ^ { 2 } .$$

Thus, in order to show (4), we have to prove

$$F ( x , y , t , r ) \colon = 2 r y - 4 r ( t ^ { \prime } ) ^ { 2 } - y ^ { 2 } - 2 t ^ { \prime } ( r - y ) ( y - x ) \\ \geq \, t ^ { 2 } ( t ^ { \prime } ) ^ { 2 } - 4 ( t ^ { \prime } ) ^ { 4 } .$$

Observe that (d /dx) F (x, y, t, r) = 2t′(r − y) ≥ 0, so we can substitute any lower bound for x without increasing F. By (5), we have

$$x \geq - \frac { t ^ { 2 } - y ^ { 2 } } { 2 f ( q ) + 2 y } \geq - \frac { t ^ { 2 } - y ^ { 2 } } { 2 ( 1 - t ) + 2 y } \geq - \frac { y } { 3 } ,$$

since t ≤  and y ≥ 2t2, by assumption. Therefore, F (x, y, t, r) ≥ F(−y/3, y, t, r) = 2ry − 4r (t′)2 − y2 −2t′(r − y)(3y). Moreover, (d/dy) F(−y/3, y, t, r) =


<!-- p:12 -->


2r )   1   s  (,1 − )( − ) &lt; ( − 1), −  − e we can also replace y by the lower bound 2t2 and obtain

$$\text {can also replace } y & \text { by the lower bound } 2 t ^ { 2 } \text { and obtain} \\ F ( x , y , t , r ) & \geq F ( - \frac { 2 } { 3 } t ^ { 2 } , 2 t ^ { 2 } , t , r ) \\ & = 4 r t ^ { 2 } - 4 r ( t ^ { \prime } ) ^ { 2 } - 4 t ^ { 4 } - \frac { 1 6 } { 3 } t ^ { \prime } ( r - 2 t ^ { 2 } ) t ^ { 2 } \\ & = \frac { 4 \, t ^ { 3 } ( 2 - 6 t - t ^ { 2 } + t ^ { 3 } ) } { 3 } \\ & \geq \frac { t ^ { 4 } } { ( 1 + t ) ^ { 2 } } - 4 \frac { t ^ { 4 } } { ( 1 + t ) ^ { 4 } } , \\ \text {desired, provided that}$$

as desired, provided that

$$\frac { 1 } { 3 } ( 8 + t - 5 0 t ^ { 2 } - 3 1 t ^ { 3 } + 4 t ^ { 4 } + 4 t ^ { 5 } ) \geq 0 ,$$

which is the case for 0 ≤ t ≤ 0.3712.

Note that we can apply the Small Angle Lemma to all q ∈ Nc(p) if we choose t = 2c · ε/(1 — ε). That is, the lemma essentially states that the tangent space TpM is a k = dim(TM)-flat that approximates Nc(p) very well. We will now show there are no lower-dimensional flats that well approximate Nc(p).

Lemma 8 (Large Angle Lemma). Let p be a sample point in Mi ∈ M and assume dim(Mi) = k. There are absolute constants ε0 &gt; 0, ρ0 &lt; 1, and c &gt; 1 satisfying

$$\arcsin \left ( \left ( \frac { c \rho _ { 0 } ( \rho _ { 0 } - 2 c \varepsilon _ { 0 } ) } { ( \rho _ { 0 } ^ { 2 } + 2 c ^ { 2 } \varepsilon _ { 0 } ) ( \rho _ { 0 } - c \varepsilon _ { 0 } ) } - 1 \right ) ^ { - 1 } \right ) < \frac { \pi } { 4 }$$

such that the following holds for every l-dimensional flat L through p with l &lt; k:

Let P be an (ε, δ)-sample of M with ε0 ≥ ε &gt; δ ≥ ρ0ε &gt; 0. Then the largest angle between L and any edge pq, q ∈ Nc(p), is bounded from below by

$$\beta _ { 0 } \colon = \frac { \pi } { 4 } - \arcsin \left ( \left ( \frac { c \rho _ { 0 } ( \rho _ { 0 } - 2 c \varepsilon _ { 0 } ) } { ( \rho _ { 0 } ^ { 2 } + 2 c ^ { 2 } \varepsilon _ { 0 } ) ( \rho _ { 0 } - c \varepsilon _ { 0 } ) } - 1 \right ) ^ { - 1 } \right ) ^ { - 1 }$$

Proof. We start the proof with a general construction. Let v be a unit vector in TpM and let x be the following point in Tp M:

$$x \colon = p + \left ( \frac { c \varepsilon } { \rho _ { 0 } } - \frac { \rho _ { 0 } - c \varepsilon } { \rho _ { 0 } - 2 c \varepsilon } \varepsilon - \frac { 2 c ^ { 2 } \varepsilon ^ { 2 } } { \rho _ { 0 } ^ { 2 } } \right ) f ( p ) \cdot v . \\$$

From Lemma 7 we know that there exists a point q ∈ M such that

$$\| x - q \| \leq 2 \left ( \frac { c \varepsilon } { \rho _ { 0 } } - \frac { \rho _ { 0 } - c \varepsilon } { \rho _ { 0 } - 2 c \varepsilon } \varepsilon - \frac { 2 c ^ { 2 } \varepsilon ^ { 2 } } { \rho _ { 0 } ^ { 2 } } \right ) ^ { 2 } f ( p ) \leq \frac { 2 c ^ { 2 } \varepsilon ^ { 2 } } { \rho _ { 0 } ^ { 2 } } f ( p ) .$$

This implies

$$\| p - q \| \leq \| p - x \| + \| x - q \| \leq \frac { c \varepsilon } { \rho _ { 0 } } f ( p ) .$$


<!-- p:13 -->


From the sampling condition we get that there exists a point p' ∈ P such that

$$\| q - p ^ { \prime } \| \leq \varepsilon f ( q ) \leq \frac { \varepsilon } { 1 - ( c \varepsilon / \rho _ { 0 } ) / ( 1 - c \varepsilon / \rho _ { 0 } ) } f ( p ) = \frac { \rho _ { 0 } - c \varepsilon } { \rho _ { 0 } - 2 c \varepsilon } \varepsilon f ( p ) .$$

Therefore,

$$\| x - p ^ { \prime } \| \leq \left ( \frac { \rho _ { 0 } - c \varepsilon } { \rho _ { 0 } - 2 c \varepsilon } \varepsilon + \frac { 2 c ^ { 2 } \varepsilon ^ { 2 } } { \rho _ { 0 } ^ { 2 } } \right ) f ( p ) ,$$

which in turn provides us with

$$\| p - p ^ { \prime } \| \leq \| p - x \| + \| x - p ^ { \prime } \| \leq \frac { c \varepsilon } { \rho _ { 0 } } f ( p ) \leq c \delta f ( p ) .$$

That is, p' ∈ Nc(p). We get for the inner angle α of the triangle xpp' at p that

$$T h a t i s , \, p ^ { \prime } \in N _ { c } ( p ) . \, We get for the inner angle \alpha \, of the triangle x p p ^ { \prime } \, a t \, p \, t a t \\ \sin \alpha \, \leq \, \frac { \| x - p ^ { \prime } \| } { | x - p \| } \leq \frac { ( ( \rho _ { 0 } - c \varepsilon ) / ( \rho _ { 0 } - 2 c \varepsilon ) ) \varepsilon + 2 c ^ { 2 } \varepsilon ^ { 2 } / \rho _ { 0 } ^ { 2 } } { c \varepsilon / \rho _ { 0 } - ( ( \rho _ { 0 } - c \varepsilon ) / ( \rho _ { 0 } - 2 c \varepsilon ) ) \varepsilon - 2 c ^ { 2 } \varepsilon ^ { 2 } / \rho _ { 0 } ^ { 2 } } \\ = \left ( \frac { c \rho _ { 0 } ( \rho _ { 0 } - 2 c \varepsilon ) } { \rho _ { 0 } ^ { 2 } ( \rho _ { 0 } - c \varepsilon ) + 2 c ^ { 2 } \varepsilon ( \rho _ { 0 } - 2 c \varepsilon ) } - 1 \right ) ^ { - 1 } \\ \leq \, \left ( \frac { c \rho _ { 0 } ( \rho _ { 0 } - 2 c \varepsilon ) } { ( \rho _ { 0 } ^ { 2 } + 2 c ^ { 2 } \varepsilon ) ( \rho _ { 0 } - c \varepsilon ) } - 1 \right ) ^ { - 1 } \\ \leq \, \left ( \frac { c \rho _ { 0 } ( \rho _ { 0 } - 2 c \varepsilon _ { 0 } ) } { ( \rho _ { 0 } ^ { 2 } + 2 c ^ { 2 } \varepsilon _ { 0 } ) ( \rho _ { 0 } - c \varepsilon _ { 0 } ) } - 1 \right ) ^ { - 1 } . \\ \text {Note that this bound on sin $\alpha$ goes to $\rho_{0}/(c - \rho _ { 0})$ as $\varepsilon_{0}$ goes to 0.}$$

Note that this bound on sin α goes to ρo/(c − ρ0) as ε0 goes to 0.

Now we are prepared to prove the lemma. We distinguish two cases. Either there exists a point y ∈ L such that the vector w := y — p makes an angle β larger than π /4 with its projection on TpM or all such vectors make an angle less than or equal to π/4 with their projection on TpM.

In the first case let π(w) be the unit vector in the direction of the projection of w on TpM. If we set v in the above calculations to be π(w), then the inner angle φ of the triangle ypp' at p can be bounded from below by using the triangle inequality for angles as follows:

$$\varphi \geq \beta - \alpha > \frac { \pi } { 4 } - \alpha .$$

In the second case let L' be the projection of L onto TpM. Since l &lt; k we find a unit vector v in TpM that is orthogonal to L'. With this vector v we find as above p' ∈ P. Let y ≠ p be some point in L and let y' be its projection on TpM. Let β be the smaller of the two angles made by y − p and y' – p. From our assumption we have β ≤ π/4. We can bound the inner angle φ of the triangle ypp' at p from below by using the triangle inequality for angles twice:

$$\varphi \geq \frac { \pi } { 2 } - \beta - \alpha \geq \frac { \pi } { 4 } - \alpha .$$

This proves our claim.

□


<!-- p:14 -->


We summarize:

Theorem 2. There are absolute constants ε0 &gt; 0, ρ0 &gt; 1, and c ≥ 1 such that for all :splo guol1of ə1 0 &lt; 30d  8 &lt; 3 &lt; 03

Suppose P is an (ε, δ)-sample from M and p ∈ P with dimp M = k (i.e., p ∈ M with dim Mi = k). Then

1. the maximal angle α between the tangent space TpM and any edge pq, q ∈ Nc(p), satisfies sin α ≤ cε/(1 − ε), but
2. for any affine subspace L through p of dimension dim L &lt; k, there is a point q ∈ Nc(p) such that the angle β between pq and L is at least βo, as defined in Lemma 8.

That is, α &lt;&lt; β if ε0 is sufficiently small.

We use Theorem 2 to devise an algorithm for dimension detection. The running time of the algorithm will depend on the size of Nc(p), so we make a brief detour to bound the latter.

Lemma 9. Suppose that ε, δ, and P are as in Theorem 2. Assume that

$$\frac { 2 c ^ { 2 } \varepsilon _ { 0 } } { ( 1 - \varepsilon _ { 0 } ) ( 1 - ( 2 c + 1 ) \varepsilon _ { 0 } ) } < \rho _ { 0 } .$$

$$| N _ { c } ( p ) | = 2 ^ { O ( k ) } ,$$

where k = dimp M, with the constant of proportionality depending on ε0, ρo, and c.

Proof. From Lemma 2 we know that any point q ∈ Nc(p) has distance at most (2cε/(1 − ε)) f (p) from p. We set

$$\eta \coloneqq \frac { 2 c \varepsilon } { 1 - \varepsilon } \quad \text {and} \quad \eta _ { 0 } \coloneqq \frac { 2 c \varepsilon _ { 0 } } { 1 - \varepsilon _ { 0 } } .$$

Observe that η ≤ ηo. Our assumption guarantees that we have that δf(q) ≥ δ(1 − η) f (p) &gt; (η/2) f (p) ≥ dist(q, TpM), so the d-dimensional ball of radius δf (q) centered at q ∈ Nc(p) intersects TpM in a k-dimensional ball centered at the projection of q onto TpM. By Pythagoras' Theorem, the squared radius of that k-dimensional ball is

$$\delta ^ { 2 } f ( q ) ^ { 2 } - d ( q , T _ { p } M ) ^ { 2 } & \geq \delta ^ { 2 } ( 1 - \eta ) ^ { 2 } f ( p ) ^ { 2 } - \eta ^ { 4 } f ( p ) / 4 \\ & = ( \delta ^ { 2 } ( 1 - \eta ) ^ { 2 } - \eta ^ { 4 } / 4 ) f ( p ) ^ { 2 } = \colon r ^ { 2 } .$$

Therefore, by our sampling condition, the k-dimensional balls of radius r centered at the projections of the points from Nc(p) onto TpM are disjoint, and they are all contained in the k-dimensional ball of radius ηf (p) + r centered at p. Since r &lt; δf (p) ≤

Then, for p ∈ P,


<!-- p:15 -->


(2ε/(1 − ε)) f (p), we have ηf (p) + r ≤ (2(c + 1)ε/(1 − ε)) f (p), and so |Nc(p)| is at most

$$f ( 1 - \varepsilon ) ) f ( p ) , & \text { we have } \eta f ( p ) + r \leq ( 2 ( c + 1 ) \varepsilon / ( 1 - \varepsilon ) ) f ( p ) , \text { and so } | N _ { c } ( p ) | \text { is } \\ & \frac { ( \eta f ( p ) + r ) ^ { k } } { r ^ { k } } \leq \left ( \frac { 1 6 ( c + 1 ) ^ { 2 } \varepsilon ^ { 2 } / ( 1 - \varepsilon ) ^ { 2 } } { 4 \delta ^ { 2 } ( 1 - \eta ) ^ { 2 } - \eta ^ { 4 } } \right ) ^ { k / 2 } \\ & \leq \left ( \frac { 1 6 ( c + 1 ) ^ { 2 } \varepsilon ^ { 2 } / ( 1 - \varepsilon ) ^ { 2 } } { 4 \varepsilon ^ { 2 } ( 1 - \eta ) ^ { 2 } \rho _ { 0 } ^ { 2 } - \eta ^ { 4 } } \right ) ^ { k / 2 } \\ & = \left ( \frac { 4 ( c + 1 ) ^ { 2 } / ( 1 - \varepsilon ) ^ { 2 } } { ( 1 - \eta ) ^ { 2 } \rho _ { 0 } ^ { 2 } - 4 c ^ { 4 } \varepsilon ^ { 2 } / ( 1 - \varepsilon ) ^ { 4 } } \right ) ^ { k / 2 } \\ & \leq \left ( \frac { 4 ( c + 1 ) ^ { 2 } / ( 1 - \varepsilon _ { 0 } ) ^ { 2 } } { ( 1 - \eta _ { 0 } ) ^ { 2 } \rho _ { 0 } ^ { 2 } - 4 c ^ { 4 } \varepsilon _ { 0 } ^ { 2 } / ( 1 - \varepsilon _ { 0 } ) ^ { 4 } } \right ) ^ { k / 2 } \\ & = 2 ^ { O ( k ) } .$$

For dimension detection we use, with ξ = 0.99 say, the following result of Har-Peled and Varadarajan [15]: Let U ⊂ Rd be a finite set of points. Then, for 0 &lt; ξ &lt; 1 and any integer 0 ≤ l ≤ d − 1, one can compute a (1 + ξ)-approximation L for the best-fit l-dimensional linear subspace for U in time

$$d | U | ^ { O ( l ^ { 6 } / \xi ^ { 5 } \log ( l / \xi ) ) } .$$

That is, one can compute an l-dimensional linear subspace L such that

$$\max _ { u \in I I } \text {dist} ( u , L ) \leq ( 1 + \xi ) \min _ { I ^ { \prime } } \max _ { u \in I I } \text {dist} ( u , L ^ { \prime } ) ,$$

where dist denotes the orthogonal distance and the minimum is taken over all l-dimensional linear subspaces L' (i.e., l-flats which contain the origin).

Theorem 3. There are constants ε0, ρ0, and c such that, for ε0 &gt; ε &gt; δ ≥ ρ0ε &gt; 0, the following holds:

Suppose we are given a finite set P of n points in Rd and we are guaranteed that it is an (ε, δ)-sample for M. Then, for each p ∈ P, if we have precomputed Nc(p), the local dimension k = dimp M at p can be computed in time

$$d 2 ^ { O ( k ^ { 7 } \log k ) } .$$

The actual computation of the neighborhoods Nc(p) can be trivially done in linear time for a single point, and hence in time O(n2) for the entire point set (for high codimensions, this will still be much faster than computing the Delaunay triangulation). It seems natural, at least if the ambient dimension d is considered fixed, to try to speed up this computation by using approximate proximity data structures as in, for instance, [5], but we do not pursue this issue further in this paper.

Proof. Choose ε0, ρo, and c according to Theorem 2 such that

$$\frac { c \varepsilon _ { 0 } } { 1 - \varepsilon _ { 0 } } \leq \frac { \sin \beta _ { 0 } } { 2 } .$$


<!-- p:16 -->


To compute the local dimension at p ∈ P, we proceed as follows:

1. Compute Nc(p) and re-normalize its elements to obtain a set of unit vectors

$$U = U _ { c } ( p ) = \left \{ \frac { q - p } { \| q - p \| } \colon q \in N _ { c } ( p ) \right \} \subset \mathbb { R } ^ { d } .$$

2. Starting with l = 1, compute a 1.99-approximation L for the best-fit l-dimensional linear subspace for U. Stop and output dimp M = l as soon as

$$\max _ { u \in U } \text {dist} ( u , L ) \leq \frac { 1 . 9 9 } { 2 } \sin ( \beta _ { 0 } ) .$$

The correctness of this algorithm is immediate from Theorem 2, and the running time follows from (7) and the fact that |Nc(p)| ≤ 20(k), as proved in Lemma 9. □

## 5. Approximation of Geodesic Distances

For x, y ∈ M, we denote by dist (x, y) the geodesic distance between x and y in M. If p and q lie in different connected components of M, then this distance is set to be ∞; otherwise it is defined as the infimum of the lengths L(γ) over all rectifiable continuous curves γ: [0, 1] → M connecting p and q, i.e., γ (0) = p and γ(1) = q. Recall that subdivisions 0 = t0 &lt; t1 &lt; · . . &lt; tN = 1 of the parameter interval, and that γ is called rectifiable if L(γ) &lt; ∞.

Since each connected component Mi of M is a smooth compact manifold, for any two points p, q ∈ Mi there exists a shortest geodesic γ connecting p and q such that L(γ) = distM(p, q).

Further, if G is the adaptive neighborhood graph for P and p, q ∈ P, let distG(p, q) be shortest-path distance between p and q in the geometric graph G, i.e., the minimum

For suitable values of the constants c, ρo, and ε0, the distances in the adaptive neighborhood graph are good approximations for the geodesic distances. This is made precise in Theorems 4 and 5 following. It follows that by applying Dijkstra's algorithm to the adaptive neighborhood graph Gc(P), we can very efficiently approximate geodesic distances in M.

Since we know from Theorem 1 that G and M have the same connected components, it suffices to consider the case that M is connected, and we assume so throughout this section.

Theorem 4. There are constants c, ρ, and ε0 such that, for ε0 ≥ ε &gt; δ ≥ ρ0ε &gt; 0, the following holds:

If G is the c-adaptive neighborhood graph for an (ε, δ)-sample P from M, then for all p, q ∈ P,

$$\text {dist} _ { M } ( p , q ) \leq ( 1 + O ( \varepsilon ^ { 2 } ) ) \text {dist} _ { G } ( p , q )$$

as ε → 0.


<!-- p:17 -->


Fig. 3. Estimating the diameter of B'\int B.

m

6

z

α

a

B


p

The proof of the theorem proceeds in a somewhat roundabout way. We first establish the following technical lemma:

Lemma 10. Let a, a' ∈ Rd, and let p and p' be the points of M closest to a and a', respectively. Assume that ∥a − a′∥ ≤ ∥p − a∥ ≤ f (p)/2. Then

$$\| p - p ^ { \prime } \| \leq \frac { 2 f ( p ) } { f ( p ) - \| p - a \| } \| a - a ^ { \prime } \| \leq 4 \| a - a ^ { \prime } \| .$$

Proof. Since p is the point in M closest to a, we have a — p ∈ NpM. We may assume that p ≠ a, otherwise the assertion of the lemma is trivial.

Consider then the ball B of radius f (p) centered at m := p + f (p) · (p − a)/∥ p − a∥. This ball is tangent to M at p, and M does not intersect the interior int B.

Moreover, let B' be the ball of radius ∥a' — p∥ centered at a', see Fig. 3. Since p' is the point of M that is closest to a', we have p' ∈ B'\int B.

Now we estimate the diameter of B'\intB. Let b := 2a' — p be the point antipodal to p in B'. We claim that b ∈ B.

Suppose we had already shown this. The boundaries of B and B' intersect in a (d — 2)-dimensional sphere S. Let x be the center of that sphere. Since b ∈ B, the point in B'\int B that is farthest from p is the point y := 2x − p that is antipodal to p in S. Hence, ∥p − p′∥ ≤ ∥p − y∥ = 2∥p − x∥|, and∥p − x∥/∥p − m∥ = ∥z − a∥/∥a − m|, where z is the orthogonal projection of a onto the line through m and a'. This establishes the lemma because ∥p − m∥ = f (p) and ∥z − a∥ ≤ ∥a — a'∥|, so it suffices to prove the claim.

In order to see that b ∈ B, first observe that our assumption ∥a — a′∥ ≤ ∥p — a∥ ≤ f (p)/2 implies that a' is contained in the ball B′′ with diameter ∥m — p∥ through m and p, see Fig. 4. Therefore, by Thales' theorem, the angle α = ∠pa'm is at least π/2. It follows that the angle β = ∠ma′b = π − α satisfies β ≤ α.

Finally, by the Cosine Theorem, we have

$$\| b - m \| ^ { 2 } = \| b - a ^ { \prime } \| ^ { 2 } + \| m - a ^ { \prime } \| ^ { 2 } - 2 \| b - a ^ { \prime } \| \cdot \| m - a ^ { \prime } \| \cos \beta$$


<!-- p:18 -->


and

$$\| p - m \| ^ { 2 } = \| m - a ^ { \prime } \| ^ { 2 } + \| p - a ^ { \prime } \| ^ { 2 } - 2 \| m - a ^ { \prime } \| \cdot \| p - a ^ { \prime } \| \cos \alpha .$$

$$\text {Since} \, \| b - a ^ { \prime } \| & = \| p - a ^ { \prime } \| \text { and } \alpha \geq \beta , \text { we conclude } \| b - m \| \leq \| p - m \| = f ( p ) , \text {i.e.,} \\ b \in B . & & \square$$

We also need the following result due to Schmidt [18] (see also [1] for a more general version).

Theorem (Schmidt). Let γ: [0, L] → Rd be a C2 curve without self-intersections. We assume that γ is parametrized by arclength, i.e., that ∥γ(t)∥ = 1 for all t. In particular, L is the length of γ, and L = L(γ) = ∫ν ∥γ (t)∥ dt. If the total curvature C(γ) = ∫ν ∥ (t)∥ dt is less than π, then the distance ∥γ (0) − γ(L)∥ between the two endpoints of γ is at least L(γ) · cos(C(γ)/2).

Proof of Theorem 4. We assume that ε, δ, and c satisfy the assumptions of Theorem 1. p d  ( =   d s p  = d    .  d = d J i.e., distc(p, q) = ∑i=1 Pi − Pi−1ll, then distm(p, q) ≤ ∑i=1 distm(Pi, Pi−1), so it suffices to prove the theorem for the case that p and q are adjacent in G.

By Lemma 2, we can write ∥p − q∥ = ηf (p), with η ≤ 2cε/(1 − ε). We assume that ε and c are chosen so that η &lt; 1 and 4η/(1 − 4η) &lt; π.

We define β: [0, 1] → M as follows: For t ∈ [0, 1], let a(t) := p + t (q − p), and let β(t) be the point in M closest to a(t) (which is unique since ∥a(t) − p∥ &lt; f (p)). It is not hard to verify that this defines indeed a continuous curve (we will not need any stronger smoothness properties of β). Further, we have ∥β(t) − p∥ ≤ 2ηf (p), hence f (β(t)) ≥ (1 − 2η) f (p) for all t. Now, consider a subdivision 0 = t0 &lt; t1 &lt; · · · &lt; tN = 1 of the interval [0, 1]. If the subdivision is sufficiently fine, then any two consecutive points

As a first step, we show that there exists a curve β in M connecting p and q such that L(β) ≤ 4∥p − q∥.

m

B′′

b

a

B

p

Fig. 4. Proving that b ∈ B.


<!-- p:19 -->


a(ti), a(t–1) satisfy the assumptions of Lemma 10. Therefore,

$$\sum _ { i = 1 } ^ { N } \| \beta ( t _ { i } ) - \beta ( t _ { i - 1 } ) \| \leq 4 \sum _ { i = 1 } ^ { N } \| a ( t _ { i } ) - a ( t _ { i - 1 } ) \| = 4 \| p - q \| ,$$

and since this holds for all subdivisions, we conclude that L(β) ≤ 4∥ p − q∥.

Now, let γ be a shortest geodesic connecting p and q in M. We assume that γ is parametrized by arc length. We write L(γ) = xηf (p), and our aim is to show that x = 1 + O(ε2). As a first estimate, we have L(γ) ≤ L(β) ≤ 4∥ p − q∥, i.e., x ≤ 4. In particular, ∥γ (t) − p∥ ≤ 4∥p − q∥ = 4ηf (p) for all t ∈ [0, L(γ)].

It follows that f (γ (t)) ≥ (1 − 4η) f (p) for all t. Hence, ∥ (t)∥ ≤ 1/(1 − 4η) f (p), as we saw in the proof of the Close Point Lemma (Lemma 7), and therefore

$$C ( \gamma ) = \int _ { 0 } ^ { L ( \gamma ) } \| \ddot { \gamma } ( t ) \| \, d t \leq \frac { L ( \gamma ) } { ( 1 - 4 \eta ) f ( p ) } = \frac { x \eta } { 1 - 4 \eta } < \pi .$$

We can now apply Schmidt's theorem, which yields

$$\text {we can show apyiscum s t h eom} , \text {when} \, y \text { yields} \\ \eta f ( p ) = \| p - q \| \geq L ( \gamma ) \cos \left ( \frac { C ( \gamma ) } { 2 } \right ) \geq x \eta f ( p ) \left ( 1 - O \left ( \left ( \frac { x \eta } { 2 ( 1 - 4 \eta ) } \right ) ^ { 2 } \right ) \right ) , \\ \\ \dot { x } _ { \mu } \cdot x _ { \mu } ( t ) = 1 _ { 0 } \, O ( x ^ { 2 } ) \cdot x _ { \mu } \cdot x _ { \mu } \cdot y _ { \mu } = 0 , \quad 0 \, y _ { \mu } \cdot x _ { \mu } \cdot y _ { \mu } = 0 ,$$

since cos(t) = 1 − O(t2) for small t. We also know that x ≤ 4, so it follows that 1 ≥ x(1 − O(η2)), hence x = 1 + O(η2) = 1 + O(ε2), as desired. □

Thus, we obtain better and better upper estimates for the geodesic distances as the sample becomes denser. On the other hand, for a lower bound, we can only guarantee a constant depending on c:

Theorem 5. Fix ρ0. For all c ≥ 1, there exists ε0 such that for all ε0 ≥ ε &gt; δ ≥ ρ0ε &gt; 0, we have

$$\text {dist} _ { G } ( p , q ) \leq \left ( 1 + O \left ( \frac { 1 } { c } \right ) \right ) \text {dist} _ { M } ( p , q )$$

for all p, q ∈ P.

Proof. Let γ be a geodesic of length distm (p, q) connecting p and q. For every point x ∈ γ let q (x) be the point in P closest to x. We set

$$\eta \coloneqq \frac { 1 } { \rho _ { 0 } ( 1 - \varepsilon ) } .$$

We construct a finite sequence of points p = x1, x2, . .. on γ. We set mi := max {f (q (xi−1)), f (q (xxi))} for i &gt; 1. Let x2 be the point on γ farthest from x1 = p = q (x1) in the order along γ such that

$$\text {dist} _ { M } ( x _ { 1 } , x _ { 2 } ) = ( c - \eta ) \rho _ { 0 } \varepsilon m _ { 2 } .$$


<!-- p:20 -->


If such a point x2 does not exist, then

$$\| p - q \| & \leq ( c - \eta ) \rho _ { 0 } \varepsilon \max \{ f ( p ) , f ( q ) \} \\ & \leq c \rho _ { 0 } \varepsilon \max \{ f ( p ) , f ( q ) \} \\ & \leq c \delta \max \{ f ( p ) , f ( q ) \} .$$

Thus pq is an edge of Gc(P) and the claim follows immediately. Otherwise we have from the sampling condition

$$\| x _ { 2 } - q ( x _ { 2 } ) \| \leq \varepsilon f ( x _ { 2 } ) \quad \text {thus} \quad \| x _ { 2 } - q ( x _ { 2 } ) \| \leq \frac { \varepsilon } { 1 - \varepsilon } \, f ( q ( x _ { 2 } ) ) .$$

We derive

$$\| x _ { 1 } - q ( x _ { 2 } ) \| & \leq \| x _ { 1 } - x _ { 2 } \| + \| x _ { 2 } - q ( x _ { 2 } ) \| \\ & \leq d i s t _ { M } ( x _ { 1 } , x _ { 2 } ) + \frac { \varepsilon } { 1 - \varepsilon } \, f ( q ( x _ { 2 } ) ) \\ & = ( c - \eta ) \rho _ { 0 } \varepsilon m _ { 2 } + \frac { \varepsilon } { 1 - \varepsilon } \, f ( q ( x _ { 2 } ) ) \\ & \leq ( c - \eta ) \rho _ { 0 } \varepsilon m _ { 2 } + \frac { \varepsilon } { 1 - \varepsilon } m _ { 2 } \\ & \leq \left ( c - \eta + \frac { 1 } { \rho _ { 0 } ( 1 - \varepsilon ) } \right ) \rho _ { 0 } \varepsilon m _ { 2 } \\ & = c \rho _ { 0 } \varepsilon m _ { 2 } \leq c \delta m _ { 2 } . \\ q ( x _ { 2 } ) \text { is an edge of } G _ { c } ( P ) , \text { that is we can approximate dist} _ { M } ( x )$$

Hence x1q(x2) is an edge of Gc(P). That is we can approximate distM(x1, x2) by ∥x1 − q(x2)∥ in Gc(P). We get for the approximation quality

$$\frac { \| x _ { 1 } - q ( x _ { 2 } ) \| } { \text {dist} _ { M } ( x _ { 1 } , x _ { 2 } ) } & \leq \frac { c \rho _ { 0 } \varepsilon m _ { 2 } } { ( c - \eta ) \rho _ { 0 } \varepsilon m _ { 2 } } = \frac { c } { c - \eta } \\ & = 1 + \frac { \eta } { c - \eta } = 1 + O \left ( \frac { 1 } { c } \right ) .$$

We proceed on γ by choosing x3 to be the point on γ farthest from x2 such that

$$\text {dist} _ { M } ( x _ { 2 } , x _ { 3 } ) = ( c - 2 \eta ) \rho _ { 0 } \varepsilon \max \{ f ( q ( x _ { 2 } ) ) , \, f ( q ( x _ { 3 } ) ) \} .$$

If such a point does not exist, then we stop with x2. Otherwise we get from a calculation similar to the one above that q (x2)q (x3) is an edge in Gc(P). That is, we can approximate distm (x2, x3) by∥q (x2) − q(x3)∥ in Gc(P). We get for the approximation quality

$$\frac { \| q ( x _ { 2 } ) - q ( x _ { 3 } ) \| } { \text {dist} _ { M } ( x _ { 2 } , x _ { 3 } ) } \leq 1 + \frac { 2 \eta } { c - 2 \eta } = 1 + O \left ( \frac { 1 } { c } \right ) .$$

We continue this construction with x4, X5, . . . . Since γ has finite length this sequence has to be finite. Let x be the last point of the sequence. We have


<!-- p:21 -->


$$\text {dist} _ { M } ( x _ { n } , q ) < ( c - 2 \eta ) \rho _ { 0 } \varepsilon \max \{ f ( q ( x _ { n } ) ) , f ( q ) \} .$$

By continuity we can find c/2 &lt; c′ ≤ c and a sequence p = y1, . . . , yn, yn+1 = q constructed the same way as the sequence p = x1, . . . , x only replacing c by c′ such that for all i = 1, . . . , n it holds that

distM(yi, yi+1) &lt; (c′ − 2η)ρ0ε max{f (q(yi)), f (q(yi+1))}.

The length of the path q (y1)q (y2) · · · q(yn+1) in Gc(P) approximates the length of γ up to a factor of 1 + O(1/c′) = 1 + O(1/c). □

Here is an example that shows that the dependence on c of the previous estimate is unavoidable, i.e., that the lower estimate of the geodesic distance in terms of the graph distance need not become better as the density of the sample increases.

For the sake of concreteness, let c = 4 and ρ0 = 1. Let M consist of two large parallel squares at distance 2 in 3-space; to compactify the example, we join the boundaries of the squares by four half-cylinders of radius 1 (for the sides) and four quarter-spheres for radius 1 (for the corners). Thus, f (x) = 1 for all x ∈ M.

For ε &gt; 0, consider a regular hexagonal grid of edge length δ = ε/2 embedded on the flat portion of M (one grid on each of the squares, but we only work with one copy), and let the sample P consist of the subset of the vertices of the grid as shown in Fig. 5, extended to a uniform sample on the non-flat parts of M in your favorite fashion.

For the points p and q indicated, we have distm(p, q) = 6δ and distG (p, q) = 2√138 for all δ = ε/2 &gt; 0.

Fig. 5. A hexagonal grid with the neighborhood of p and the shortest path from p to q.

<!-- p:22 -->


## 6. Conclusion

We have shown that the adaptive neighborhood graph can replace the Delaunay triangulation for some tasks in sample-based modeling. That is important since the Delaunay triangulation is prohibitive to compute in high dimensions. With the adaptive neighborhood graph it becomes feasible to provably correctly solve problems as inferring the dimension and connectivity of a manifold from a sample even if the ambient dimension is very high.

The (ε, δ)-sampling condition is quite strict and it is reasonable to assume that it is hardly ever met in practice. Nevertheless, a combination of the adaptive neighborhood graph with the k nearest neighbor approach, i.e., building the neighborhood graph on k nearest neighbors instead of just the nearest neighbor, should remove on practical data sets, e.g., locally uniform random samples, the disadvantages of both approaches when applied alone (too strict sampling condition for the neighborhood graph and nonadaptivity to the dimension of the k nearest neighbors).

We are quite confident that the adaptive neighborhood graph will be useful even for the more general problem of manifold reconstruction.
