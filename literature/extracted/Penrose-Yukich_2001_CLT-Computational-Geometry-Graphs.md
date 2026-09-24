---
id: "Penrose-Yukich_2001_CLT-Computational-Geometry-Graphs"
source_pdf: "../pdf/Penrose-Yukich_2001_CLT-Computational-Geometry-Graphs.pdf"
source_filename: "Penrose-Yukich_2001_CLT-Computational-Geometry-Graphs.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "excellent"
extraction_score: 100.0
visual_assets: "disabled"
references_file: "../references/Penrose-Yukich_2001_CLT-Computational-Geometry-Graphs.references.md"
---

<!-- p:1 -->

## CENTRAL LIMIT THEOREMS FOR SOME GRAPHS IN COMPUTATIONAL GEOMETRY

By Mathew D. Penrose and J. E. Yukich 1

University of Durham and Lehigh University

Let lparenOSCASB Bn rparenOSCASB be an increasing sequence of regions in d -dimensional space with volume n and with union Ropen d . We prove a general central limit theorem for functionals of point sets, obtained either by restricting a homogeneous Poisson process to Bn , or by by taking n uniformly distributed points in Bn . The sets Bn could be all cubes but a more general class of regions Bn is considered. Using this general result we obtain central limit theorems for specific functionals such as total edge length and number of components, defined in terms of graphs such as the k -nearest neighbors graph, the sphere of influence graph and the Voronoi graph.

1. Introduction. The purpose of this paper is to develop a general methodology to establish central limit theorems (CLTs) for functionals of graphs in computational geometry. Functionals of interest include total edge length, total number of edges, total number of components and total number of vertices of fixed degree. Graphs of interest include the k -nearest neighbors graph, the Voronoi and Delaunay tessellations, the sphere of influence graph, the Gabriel graph and the relative neighbor graph. These graphs are formally defined later on. In each case, the graph or its dual graph (as with the Voronoi graph) is constructed as follows: given a finite vertex set in Ropen d commaorid ≥ 1, undirected edges are drawn from each vertex to various nearby vertices, the choice of edges to include being determined by the local point configuration according to some specified rule. Sometimes such graphs are called proximity graphs ; see [3] for a precise definition.

Our graphs are random in the sense that the vertex set is a random point set in Ropen d commaorid ≥ 1. We establish CLTs for two related types of random point sets: the homogeneous Poisson point process on a large region or 'window' of Ropen d and the point set consisting of a large independent sample of nonrandom sample size from the uniform distribution on such a region. By scaling, these often yield a CLT for Poisson processes of high intensity on a fixed set such as the unit cube lbrackOSCASB 0 commaori 1 rbrackOSCASB d , or for large independent samples of nonrandom size from the uniform distribution on a fixed set. As a by-product, we also prove the convergence of the (scaled) variance of our functionals of interest.

One of our more interesting new results is a CLT for the total number of components of the k -nearest neighbors graph, either on a Poisson process or on a sample of nonrandom size, and likewise for the sphere of influence graph.

Received November 1999; revised June 2000.

1 Supported in part by NSA Grant MDA904-97-1-0053.

AMS 2000 subject classifications . Primary 60F05; secondary 60D05.

Key words and phrases . Central limit theorems, computational geometry, k -nearest neighbors graph, sphere of influence graph, Voronoi graph.


<!-- p:2 -->


We also establish CLTs for the total edge length of the k -nearest neighbors graph on a sample of nonrandom size, and likewise for the sphere of influence graph and the Voronoi graph. These latter results add to existing results for their Poisson counterparts [1, 8, 10]. We believe that the CLTs established here, particularly those for nonrandom sample sizes, may have uses in the statistical analysis of data and may lead to useful tests for clustering. All of our CLTs follow from a general CLT which can be viewed as an attempt to capture the essence of the martingale method developed by Kesten and Lee [11], and extended by Lee [12, 13], in their deep study of the random Euclidean minimal spanning tree. The martingale method is developed into a general CLT for functionals of lattice-indexed white noise in [19]. Using the method of [19], we find a general CLT for functionals of graphs over Poisson point sets. To obtain CLTs on nonrandom sample sizes, we de-Poissonize by using a coupling lemma and some key ideas of Kesten and Lee [11]. An important earlier paper developing general CLTs of this type is that of Avram and Bertsimas [1], and a brief comparison is in order. First, the martingale method used here achieves CLTs for some functionals for which it is not apparent how to use the dependency graph method of [1]. Second, our method yields convergence of variances, an issue not addressed in [1]. Third, nonrandom sample sizes are considered here, but not in [1]. Fourth, we prove CLTs for functionals of point sets defined on rather general regions, not just on cubes of volume n . On the other hand, the method of [1], where applicable, can yield error bounds providing useful information about the rate of convergence, which is not given by our method. Specific graphs of interest are defined in terms of distances between points. , throughout, but our results should

We use the Euclidean norm, denoted vertSHT · vertSHT carry through to other norms. Let us now define the graphs of main interest.

k -nearest neighbors graph. The k -nearest neighbors graph on a point set Xscript ⊂ Ropen d is obtained by including lbraceOSCASB xcommaoriy rbraceOSCASB as an edge whenever y is one of the k nearest neighbors of x and/or x is one of the k nearest neighbors of y . If the k th nearest neighbor of x is not well defined (i.e., if there is a 'tie' in the ordering of interpoint distances involving x ), use the lexicographic ordering as a 'tie-breaker' to determine the k nearest neighbors. Such a tie has zero probability for the random point sets under consideration here. The k -nearest neighbors graph is an example of a dependent random connection model in percolation theory (see [16, 7]). This graph is also used in clustering methods in statistics and computer science. See [8, 21, 23] for additional applications

and references.

Sphere of influence graph. Given a point set Xscript ⊂ Ropen d , the sphere of influence graph (SIG) is constructed as follows: for each x ∈ Xscript , let Sscript x denote the closed ball centered at x with radius equal to the distance between x and its nearest neighbor in Xscript . This ball is often called the sphere of influence of x . The sphere of influence graph puts an edge between x and y if and only if the balls Sscript x and Sscript y overlap.


<!-- p:3 -->


In the language of continuum percolation [16], much as the k -nearest neighbors graph can be viewed as a dependent random connection model, the sphere of influence graph can be viewed as a dependent Boolean model. The sphere of influence graph is used in pattern recognition and computer science and we refer to the survey [17] for details. One of our new results is 'uniqueness of the infinite component' for the SIG on a homogeneous Poisson process on Ropen d , a result which is required for one of our CLTs. This adds to known uniqueness results for other graphs [16, 9].

Voronoi tessellations. Given a point set Xscript ⊂ Ropen d and x ∈ Xscript , consider the locus of points closer to x than to any other point. This set of points is the intersection of half planes and is a convex polyhedral cell. The cells partition Ropen d into a convex net which is variously called the Voronoi tessellation, Voronoi graph, Voronoi diagram or Dirichlet tessellation of Ropen d . Voronoi tessellations have numerous applications and are used to model natural phenomena in astrophysics, cell biology, crystallography, geology, metallography and other applied fields. See the encyclopedic work, [18], for details and a thorough treatment of the many applications.

This paper is organized as follows. Sections 2-5 contain the general results and their proofs, and Sections 6-9 contain applications to particular functionals of particular graphs.

Notational conventions: c denotes a generic finite positive constant whose value may change from line to line. For any set Xscript ⊂ Ropen d and any y ∈ Ropen d , we denote by Xscript - y the translated set lbraceOSCASB x - y colonori x ∈ Xscript rbraceOSCASB , and likewise set Xscript + y = lbraceOSCASB x + y colonori x ∈ Xscript rbraceOSCASB . Also, if a &gt; 0, we let a Xscript denote the set lbraceOSCASB ax colonori x ∈ Xscript rbraceOSCASB . For x ∈ Ropen d and r &gt; 0, let Br lparenOSCASB x rparenOSCASB denote the Euclidean ball centered at x and with radius r , and let Qr lparenOSCASB x rparenOSCASB denote the corresponding l ∞ ball (a cube); that is, Qr lparenOSCASB x rparenOSCASB = lbrackOSCASBrcommaorir rbrackOSCASB d + x . For F ⊂ Ropen d let vertSHT F vertSHT denote the Lebesgue measure of the set F , let ∂F denote the intersection of the closure of F with that of its complement and for r &gt; 0, set ∂rF = ∪ x ∈ ∂F Q r lparenOSCASB x rparenOSCASB , the r -neighborhood of the boundary of F . Let diam lparenOSCASB F rparenOSCASB = sup lbraceOSCASBvertSHT x - y vertSHTcolonori xcommaoriy ∈ F rbraceOSCASB , and let card lparenOSCASB F rparenOSCASB denote its cardinality (when finite).

Let Dscript -→ denote convergence in distribution, let P -→ denote convergence in probability and let Nscript lparenOSCASB μcommaoriσ 2 rparenOSCASB denote a normally distributed random variable with mean μ and variance σ 2 .

2. A general central limit theorem. Let d ≥ 1. Throughout the rest of this paper, λ &gt; 0 is a constant and lparenOSCASB Bn rparenOSCASB n ≥ 1 denotes a sequence of bounded Borel subsets ('regions' or 'windows') of Ropen d , satisfying the following conditions. First, vertSHT Bn vertSHT = n/λ for all n ; second, Bn tends to Ropen d , by which we mean ∪ n ≥ 1 ∩ m ≥ n Bm = Ropen d ; third, lim n →∞lparenOSCASBvertSHT ∂rBn vertSHT /n rparenOSCASB = 0 for all r &gt; 0 (the vanishing relative boundary condition) and fourth, there exists a constant β 1 such that diam lparenOSCASB Bn rparenOSCASB ≤ β 1 n β 1 for all n (the polynomial boundedness condition on Bn ). Subject to these conditions, the choice of lparenOSCASB Bn rparenOSCASB n ≥ 1 is arbitrary.

Let U 1 commaorin commaoriU 2 commaorin commaori periodori periodori periodori be independent identically distributed uniform variables on Bn . Let Uscript mcommaorin = lbraceOSCASB U 1 commaorin commaori periodori periodori periodori commaori Umcommaori n rbraceOSCASB (a binomial point process) and let Pscript n be a homogeneous Poisson process on Bn of intensity λ . Also, let B 0 be a fixed bounded Borel set in Ropen d satisfying vertSHT B 0 vertSHT = 1 and vertSHT ∂B 0 vertSHT = 0 (for example, the unit cube), and let Xscript n = lbraceOSCASB X 1 commaori periodori periodori periodori commaoriXn rbraceOSCASB , where X 1 commaoriX 2 commaoriX 3 commaori periodori periodori periodori are independent and uniformly distributed on B 0 . All of our results refer to the point processes Pscript n , Uscript ncommaorin and Xscript n , defined in this way.


<!-- p:4 -->


Let H be a real-valued functional defined for all finite subsets of Ropen d . Assume that H is translation-invariant, meaning that H lparenOSCASB Xscript + y rparenOSCASB = H lparenOSCASB Xscript rparenOSCASB for all Xscript ⊂ Ropen d and all y ∈ Ropen d . We derive central limit theorems for H lparenOSCASB Pscript n rparenOSCASB commaoriH lparenOSCASB Uscript ncommaorin rparenOSCASB and H lparenOSCASB Xscript n rparenOSCASB .

In the proof of our results, we shall need to consider translates of the regions Bn . With this in mind, let Bscript be the collection of all regions A ⊂ Ropen d of the form A = lbraceOSCASB Bn + x colonori x ∈ Ropen d commaorin ≥ 1 rbraceOSCASB . Likewise, let Bscript 0 be the collection of all regions of the form A = aB 0 + x with a ≥ 1 and x ∈ Ropen d .

The conditions on H for our central limit theorems are defined in terms of the 'add one cost,' by which we mean the increment in H caused by inserting a point at the origin into a finite point set Xscript ⊂ Ropen d , formally given by

Let Pscript be a homogeneous Poisson process of intensity λ on Ropen d . Our first condition on H develops a notion of stabilization having its origins in [12, 13].

$$\Delta ( \mathcal { X } ) \colon = H ( \mathcal { X } \cup \{ 0 \} ) - H ( \mathcal { X } ) . \\$$

Definition 2.1. The functional H is strongly stabilizing if there exist a.s. finite random variables S (a radius of stabilization of H ) and Delta1 lparenOSCASB∞rparenOSCASB such that with probability 1, Delta1 lparenOSCASBlparenOSCASB Pscript ∩ BS lparenOSCASB 0 rparenOSCASBrparenOSCASB∪ Ascript rparenOSCASB = Delta1 lparenOSCASB∞rparenOSCASB for all finite Ascript ⊂ lparenOSCASB Ropen d \ BS lparenOSCASB 0 rparenOSCASBrparenOSCASB .

Thus, S is a radius of stabilization if the add one cost for Pscript is unaffected by changes in the configuration outside the ball BS lparenOSCASB 0 rparenOSCASB .

Given A ∈ Bscript , let Uscript mcommaoriA be a point process consisting of m independent uniform variables on A . Our second condition on H is a uniform bound on the fourth moments of the add one cost for this point process. Our third condition is a mild uniform bound on the size of H .

Definition 2.2. The functional H satisfies the uniform bounded moments condition on Bscript if

$$\sup _ { A \in \mathcal { B } \colon 0 \in A \ m \in [ \lambda | A | / 2 , 3 \lambda | A | / 2 ] } \{ \mathbb { E } [ \Delta ( \mathcal { W } _ { m , \, A } ) ^ { 4 } ] \} < \infty .$$

Definition 2.3. The functional H is polynomially bounded if there exists a constant β 2 such that for all finite sets Xscript ⊂ Ropen d ,

$$| H ( \mathcal { X } ) | \leq \beta _ { 2 } ( \text {diam} ( \mathcal { X } ) + \text {card} ( \mathcal { X } ) ) ^ { \beta _ { 2 } } .$$

The following result is basic to this paper.

Theorem 2.1. Suppose that H is strongly stabilizing, satisfies the uniform bounded moments condition on Bscript , and is polynomially bounded. Then there exist constants σ 2 commaori τ 2 , with 0 ≤ τ 2 ≤ σ 2 , such that as n →∞ ,


<!-- p:5 -->


$$n ^ { - 1 } \text {Var} ( H ( \mathcal { P } _ { n } ) ) \to \sigma ^ { 2 } \\$$

and

$$n ^ { - 1 / 2 } ( H ( \mathcal { P } _ { n } ) - \mathbb { E } H ( \mathcal { P } _ { n } ) ) \stackrel { \mathcal { I } } { \longrightarrow } & \mathcal { W } ( 0 , \sigma ^ { 2 } ) , \\$$

while

$$n ^ { - 1 } \text {Var} ( H ( \mathcal { W } _ { n , n } ) ) \to \tau ^ { 2 } \\$$

and

$$n ^ { - 1 / 2 } ( H ( \mathcal { U } _ { n , n } ) - \mathbb { E } H ( \mathcal { U } _ { n , n } ) ) \stackrel { \mathcal { G } } { \longrightarrow } \mathcal { V } ( 0 , \tau ^ { 2 } ) . \\$$

lparenOSCASB Bn rparenOSCASB . If the distribution of Delta1 lparenOSCASB∞rparenOSCASB is nondegenerate, then τ 2 &gt; 0 , and hence also 2

Also, given λcommaoriσ 2 and τ 2 are independent of the choice of

σ &gt; 0 .

The proof of Theorem 2.1 will show that τ 2 = σ 2 - lparenOSCASB Ɛ Delta1 lparenOSCASB∞rparenOSCASBrparenOSCASB 2 . In most of our examples Ɛ Delta1 lparenOSCASB∞rparenOSCASB will be strictly positive because adding a point tends to increase the value of the functional and thus τ 2 will be strictly less than σ 2 . In other words, Poissonization contributes extra randomness which shows up in the limiting variance.

In Theorem 2.1 the condition vertSHT Bn vertSHT= n/λ can be relaxed to

The proof under this weaker condition is essentially unchanged. Also, the polynomial boundedness condition can be weakened to (2.6) and (2.7) below, and the first two limits (2.1) and (2.2) remain true under somewhat weaker forms of the moments and stabilization conditions (Theorem 3.1 below).

$$\lim \sup _ { n \to \infty } n ^ { - 1 / 2 } | ( n - \lambda | B _ { n } | ) | < \infty . \\$$

To deduce CLTs for functionals H on the point process Xscript n of independent uniform points in B 0 , we require one further scaling property for H . Given γ ∈ Ropen , we shall say H is homogeneous of order γ if for all Xscript ⊂ Ropen d on which H is defined, and all a ∈ Ropen ,

$$H ( a \mathcal { X } ) & = a ^ { \gamma } H ( \mathcal { X } ) . \\$$

If H satisfies homogeneity, it is easy to deduce from the above theorems a CLT for homogeneous Poisson processes of high intensity, or for a large sample of nonrandom size from the uniform distribution, on B 0 . We just state such a result for the sample Xscript n of large nonrandom size on B 0 .

Corollary 2.1. Suppose H is strongly stabilizing, satisfies the uniform bounded moments condition on Bscript 0 , is polynomially bounded and is homogeneous of order γ . Then with τ 2 the constant given in the case λ = 1 of Theorem 2 periodori 1 , n lparenOSCASB 2 γ/d rparenOSCASB1 Var H lparenOSCASB Xscript n rparenOSCASB→ τ 2 , and

$$n ^ { ( \gamma / d ) - 1 / 2 } ( H ( \mathcal { X } _ { n } ) - \mathbb { E } H ( \mathcal { X } _ { n } ) ) \stackrel { \mathcal { I } } { \longrightarrow } \mathcal { N } ( 0 , \tau ^ { 2 } ) .$$


<!-- p:6 -->


Corollary 2.1 is easily proved by assuming the origin lies in the interior of B 0 (if not, consider a suitable translate), taking Bn = n 1 /d B 0 , applying Theorem 2.1 and using homogeneity of H .

If H is homogeneous, the general case of Theorem 2.1 follows from the special case λ = 1. All of the specific functionals considered in detail here will be homogeneous for some γ , so we consider only the case λ = 1 for these examples. For examples where H is not homogeneous, see the last example in Section 9 and also [20].

Kesten and Lee [11] essentially showed that the total edge length of the power-weighted Euclidean minimal spanning tree satisfies all the conditions of Theorem 2.1 and Corollary 2.1. In this way they proved a nontrivial CLT for one of the archetypical problems of combinatorial optimization. The second half of this paper shows that various functionals of proximity graphs also satisfy the conditions of Theorem 2.1. Some of these applications involve some intricate work. In a related paper [20], we generalize Theorem 2.1 to functionals of marked point processes and thus central limit theorems for sphere packing and related problems.

A long-standing open problem is to find convergence of the variance, and a CLT, for the length of the optimal traveling salesman tour on Xscript n (or on a Poissonized point process). Other open problems of this kind concern the total length of the minimal matching on random points and the total length of the Steiner tree on random points. Our results show that one possible approach involves showing strong stabilization for these functionals. Although a proof of stabilization remains elusive, we believe that the approach here might be useful in attacking such problems.

In many of our applications, the following condition on Bscript will be used for checking the bounded moments condition. Let us say Bscript is regular if there exists δ &gt; 0 such that for all r ∈ lbrackOSCASB 1 commaori ∞rparenOSCASB , whenever A ∈ Bscript and xcommaoriy ∈ A with vertSHT x - y vertSHT = r , we have

$$| B _ { r / 4 } ( x ) \cap A | \geq \delta r ^ { \delta } .$$

By a box we shall mean a set B ⊂ Ropen d of the form ∏ d i = 1 lbrackOSCASB ai commaori bi rbrackOSCASB , with bi ≥ ai + 1 for each i . It is not hard to show that the collection of all boxes is regular, and therefore in applications that require regularity, taking the sets Bn to be all boxes is sufficient to ensure that Bscript is regular. Incidentally, if the sets Bn are all boxes then the vanishing boundary and polynomial boundedness conditions for Bn follow automatically from the assumptions that Bn → Ropen d and vertSHT Bn vertSHT = n/λ .

The next three sections are devoted to the proofs of our main results. The proofs make heavy use of the uniform fourth moment condition. It is likely that this can be replaced by a 2 + ε moment condition, but since the weaker

If instead of boxes, Bscript is a set of balls or ellipsoids, then again it is regular. It can be seen that a sufficient condition on B 0 for Bscript 0 to be regular is that B 0 has a reasonably smooth boundary in the sense that r - d vertSHT Br lparenOSCASB x rparenOSCASB ∩ B 0 vertSHT is bounded away from zero, uniformly over x ∈ B 0 and r ∈ lparenOSCASB 0 commaori 1 rbrackOSCASB .


<!-- p:7 -->


condition does not seem to increase the range of applications considered here, we have used the fourth moment condition for technical ease. Our CLTs also hold if the deterministic polynomial boundedness conditions on H and Bn are replaced by the weaker moment bounds

$$\max ( \mathbb { E } [ H ( \mathcal { U } _ { n , \, n } ) ^ { 4 } ] , \mathbb { E } [ H ( \mathcal { P } _ { n } ) ^ { 4 } ] ) \leq \beta _ { 3 } n ^ { \beta _ { 3 } } \\$$

and for all A ∈ Bscript ,

We will actually use only these weaker conditions in the proofs.

$$E [ \Delta ( \mathcal { P } \cap A ) ^ { 8 } ] & \leq \beta _ { 4 } | A | ^ { \beta _ { 4 } } . \\ \\ \intertext { s u r } E [ \Delta ( \mathcal { P } \cap A ) ^ { 8 } ] & \leq \beta _ { 4 } | A | ^ { \beta _ { 4 } } .$$

3. Proof of CLT: the Poisson case. In this section we prove a CLT for H lparenOSCASB Pscript n rparenOSCASB only, under somewhat different conditions than those of Theorem 2.1. These conditions are in fact weaker (see Lemma 4.1) and thus we actually establish (2.1) and (2.2).

Definition 3.1. The functional H is weakly stabilizing on Bscript if there is a random variable Delta1 lparenOSCASB∞rparenOSCASB such that Delta1 lparenOSCASB Pscript ∩ A rparenOSCASB a periodori s periodori -→ Delta1 lparenOSCASB∞rparenOSCASB as A → Ropen d through Bscript , by which we mean that for any Bscript -valued sequence lparenOSCASB An rparenOSCASB n ≥ 1 that tends to Ropen d , Delta1 lparenOSCASB Pscript ∩ An rparenOSCASB→ Delta1 lparenOSCASB∞rparenOSCASB as n →∞ , almost surely.

Observe that strong stabilization implies weak stabilization on Bscript . In fact, for all specific examples considered in this paper, strong stabilization holds. We retain the distinction, first to emphasize which properties are used in the proofs, and second, to allow for the possibility that in some cases not considered here (see, e.g., [19]), it may be possible to prove weak stabilization but not strong stabilization.

As shown in Section 4, the following moments condition is weaker than the uniform moments condition. It is all we need in the Poisson setting.

Definition 3.2. The functional H satisfies the Poisson bounded moments condition on Bscript if

$$\sup _ { A \in \mathcal { O } \colon \, 0 \in A } \{ \mathbb { E } [ \Delta ( \mathcal { P } \cap A ) ^ { 4 } ] \} < \infty .$$

Theorem 3.1. Suppose that H is weakly stabilizing on Bscript and satisfies the Poisson bounded moments condition on Bscript . Then there exists σ 2 ≥ 0 such that as n → ∞ , n - 1 Var lparenOSCASB H lparenOSCASB Pscript n rparenOSCASBrparenOSCASB → σ 2 and n - 1 / 2 lparenOSCASB H lparenOSCASB Pscript n rparenOSCASB - Ɛ H lparenOSCASB Pscript n rparenOSCASBrparenOSCASB Dscript -→ Nscript lparenOSCASB 0 commaoriσ 2 rparenOSCASB periodori

Theorem 3.1 still holds if in Definition 3.1, almost sure convergence is relaxed to convergence in probability. The proof under this weaker condition is essentially the same as that given, but entails some extra subsequence arguments.

The first step toward a proof of Theorem 3.1 is to show that the conditions in Definitions 3.1 and 3.2 imply alternative stabilization and moment conditions, referring to the modification of the homogeneous Poisson process Pscript by replacing those Poisson points lying in a unit cube with an independent Poisson process on that unit cube, rather than inserting a single point. Formally, this modification is defined as follows.


<!-- p:8 -->


Let Pscript ′ be an independent copy of the Poisson process Pscript . For x ∈ Zopen d , set

$$\mathcal { P } ^ { \prime \prime } ( x ) = ( \mathcal { P } \rangle Q _ { 1 / 2 } ( x ) ) \cup ( \mathcal { P } ^ { \prime } \cap Q _ { 1 / 2 } ( x ) ) .$$

Then, given a translation-invariant functional H of point sets in Ropen d , define

$$\Delta _ { x } ( A ) \coloneqq H ( \mathcal { P } ^ { \prime \prime } ( x ) \cap A ) - H ( \mathcal { P } \cap A ) .$$

Lemma 3.1. Suppose H is weakly stabilizing on Bscript . Then for all x ∈ Zopen d , there is a random variable Delta1 x lparenOSCASB∞rparenOSCASB such that for all x ∈ Zopen d ,

$$\Delta _ { x } ( A ) \stackrel { a . s . } { \longrightarrow } \Delta _ { x } ( \infty ) \ \text { as } A \to \mathbb { R } ^ { d } \ \ t h r o u g h \ \mathcal { B } .$$

Moreover, if H satisfies the Poisson bounded moments condition on Bscript , then

$$\sup _ { A \in \mathcal { B } , \ x \in \mathbb { Z } ^ { d } } \mathbb { E } [ ( \Delta _ { x } ( A ) ) ^ { 4 } ] < \infty .$$

Proof. Set C 0 = Q 1 / 2 lparenOSCASB 0 rparenOSCASB . To prove (3.2), by translation-invariance it suffices to consider the case x = 0, and therefore suffices to prove that the variables H lparenOSCASB Pscript ∩ A rparenOSCASBH lparenOSCASB Pscript ∩ A \ C 0 rparenOSCASB converge almost surely as A → Ropen d through Bscript .

The number N of points of Pscript in C 0 is a Poisson variable with parameter λ . Let V 1 commaoriV 2 commaori periodori periodori periodori commaoriVN be the points of Pscript ∩ C 0 , taken in an order chosen uniformly at random from the N ! possibilities. Then, provided C 0 ⊆ A ,

where

$$H ( \mathcal { P } \cap A ) - H ( \mathcal { P } \cap A \langle C _ { 0 } \rangle = \sum _ { i = 0 } ^ { N - 1 } \delta _ { i } ( A ) ,$$

$$\delta _ { i } ( A ) = H ( ( \mathcal { P } \cap A \langle C _ { 0 } \rangle \cup \{ V _ { 1 } , \dots , V _ { i + 1 } \} ) - H ( ( \mathcal { P } \cap A \langle C _ { 0 } \rangle \cup \{ V _ { 1 } , \dots , V _ { i } \} ) .$$

Since N is a.s. finite, it suffices to prove each δi lparenOSCASB A rparenOSCASB converges almost surely as A → Ropen d through Bscript . Let U be a uniform variable on C 0 , independent of Pscript . The distribution of the translated point process lparenOSCASBlbraceOSCASB V 1 commaori periodori periodori periodori commaoriVi rbraceOSCASB ∪lparenOSCASB Pscript \ C 0 rparenOSCASBrparenOSCASBVi + 1 is the same as the conditional distribution of the Poisson process Pscript given that the number of points of Pscript in C 0 - U is equal to i , an event of strictly positive probability. By assumption, this satisfies weak stabilization, which proves (3.2).

Next we prove (3.3) under the Poisson bounded moments assertion. If Q 1 / 2 lparenOSCASB x rparenOSCASB ∩ A = varnothing then Delta1 x lparenOSCASB A rparenOSCASB is zero, a.s. By translation-invariance it suffices to consider the case with x = 0, that is, to prove

$$\sup _ { A \in \mathcal { B } \colon C _ { 0 } \cap A \neq \emptyset } \mathbb { E } [ ( \Delta _ { 0 } ( A ) ) ^ { 4 } ] < \infty .$$


<!-- p:9 -->


Let N ′ be the number of points of Pscript in C 0 ∩ A ; in cases with C 0 ⊆ A this is the same as N . In general, N ′ has a Poisson distribution with mean μ colonori= λ vertSHT C 0 ∩ A vertSHT . Let V 1 commaori periodori periodori periodori commaoriVN ′ be the points of Pscript ∩ C 0 ∩ A , taken in random order. Then

$$H ( \mathcal { P } \cap A ) - H ( \mathcal { P } \cap A \langle C _ { 0 } \rangle ) & = \sum _ { i = 0 } ^ { N ^ { \prime } - 1 } \delta _ { i } ( A ) , \\ \intertext { ) i s d o f i n d o w e $ A $ l o s $ H ( \mathcal { W } ^ { \prime \prime } ( 0 ) \cap A ) $ }$$

where δi lparenOSCASB A rparenOSCASB is defined above. Also, H lparenOSCASB Pscript ′′ lparenOSCASB 0 rparenOSCASB∩ A rparenOSCASBH lparenOSCASB Pscript ′′ lparenOSCASB 0 rparenOSCASB∩ A \ C 0 rparenOSCASB has the same distribution as H lparenOSCASB Pscript ∩ A rparenOSCASBH lparenOSCASB Pscript ∩ A \ C 0 rparenOSCASB . Hence, it suffices to prove

$$\sup _ { A \in \mathcal { B } \colon C _ { 0 } \cap A \neq \emptyset } \left [ \left ( \sum _ { i = 0 } ^ { N ^ { \prime } - 1 } \delta _ { i } ( A ) \right ) ^ { 4 } \right ] < \infty . \\ = k l \text { Then writing simply } \delta _ { i } \text { for } \delta ( A ) \text { , we have }$$

Set pk = P lbrackOSCASB N ′ = k rbrackOSCASB . Then, writing simply δi for δi lparenOSCASB A rparenOSCASB , we have

$$\text {Set } \rho _ { k } = P [ N \stackrel { \prime } { = } k ] . \text { Then, with } \text { simply } \delta _ { i } \text { for } \delta _ { i } ( A ) , \text { we have} \\ \mathbb { E } \left [ \left ( \sum _ { i = 0 } ^ { N ^ { \prime } - 1 } \delta _ { i } \right ) ^ { 4 } \right ] = \sum _ { k = 1 } ^ { \infty } p _ { k } \mathbb { E } \left [ \left ( \delta _ { k - 2 } + \delta _ { k - 1 } + \sum _ { i = 0 } ^ { k - 3 } \delta _ { i } \right ) ^ { 4 } \right ] \\ \leq \sum _ { k = 1 } ^ { \infty } p _ { k } 3 ^ { 3 } \mathbb { E } \left ( \delta _ { k - 2 } ^ { 4 } + \delta _ { k - 1 } ^ { 4 } + ( k - 2 ) ^ { 3 } \sum _ { i = 0 } ^ { k - 3 } \delta _ { i } ^ { 4 } \right ) , \\ \text {where the last line is obtained using Cauchy-Schwarz, where we set } \delta _ { - 1 } =$$

where the last line is obtained using Cauchy-Schwarz, where we set δ - 1 = δ - 2 = 0 and where the summation ∑ k - 3 i = 0 is taken to be zero when k ≤ 2. Consider the final sum. Rearranging, we have

$$\sum _ { k = 3 } ^ { \infty } p _ { k } ( k - 2 ) ^ { 3 } \sum _ { i = 0 } ^ { k - 3 } \mathbb { E } \delta _ { i } ^ { 4 } & = \sum _ { i = 0 } ^ { \infty } q _ { i } \mathbb { E } \delta _ { i } ^ { 4 } , \\ ( k _ { 1 } , 2 ) _ { 3 } & = \prod _ { i = 0 } ^ { T ] _ { 1 } } T | _ { 2 } \prod _ { i = 0 } ^ { T }$$

$$& \frac { q _ { i } } { p _ { i } } = \sum _ { k \geq i + 3 } \frac { i ! \mu ^ { k - i } ( k - 2 ) ^ { 3 } } { k ! } \leq \sum _ { k \geq i + 3 } \frac { i ! \mu ^ { k - i } } { ( k - 3 ) ! } \\ & = \sum _ { j \geq 0 } \frac { \mu ^ { j + 3 } i ! } { ( i + j ) ! } \leq \mu ^ { 3 } \sum _ { j \geq 0 } \frac { \mu ^ { j } } { j ! } = \mu ^ { 3 } e ^ { \mu } .$$

with qi = ∑ k ≥ i + 3 lparenOSCASB k - 2 rparenOSCASB 3 pk . Then

$$= \sum _ { j \geq 0 } \frac { \mu ^ { j + 3 } i ! } { ( i + j ) ! } \leq \mu ^ { 3 } \sum _ { j \geq 0 } \frac { \mu ^ { j } } { j ! } \\$$

Hence, ∑ ∞ i = 0 qi Ɛ δ 4 i ≤ μ 3 e μ ∑ ∞ i = 0 pi Ɛ δ 4 i periodori Similarly, since pi + 2 /pi = μ 2 / lparenOSCASBlparenOSCASB i + 2 rparenOSCASBlparenOSCASB i + 1 rparenOSCASBrparenOSCASB ≤ μ 2 , we have

$$\sum _ { k = 2 } ^ { \infty } p _ { k } \mathbb { E } \delta _ { k - 2 } ^ { 4 } & = \sum _ { i = 0 } ^ { \infty } p _ { i + 2 } \mathbb { E } \delta _ { i } ^ { 4 } \leq \mu ^ { 2 } \sum _ { i = 0 } ^ { \infty } p _ { i } \mathbb { E } \delta _ { i } ^ { 4 } . \\ \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \$$

One obtains a similar bound (this time with a factor of μ ) in the case of Ɛ δ 4 k - 1 . Combining all these estimates in (3.5), and setting c lparenOSCASB μ rparenOSCASB = 27 lparenOSCASB μ 3 e μ + μ 2 + μ rparenOSCASB , we have


<!-- p:10 -->


$$\text {we have} \\ \mathbb { E } \left ( \left ( \sum _ { i = 0 } ^ { N ^ { \prime } - 1 } \delta _ { i } \right ) ^ { 4 } \right ) & \leq c ( \mu ) \sum _ { i = 0 } ^ { \infty } p _ { i } \mathbb { E } \delta _ { i } ^ { 4 } = c ( \mu ) \int _ { C _ { 0 } \cap A } \frac { d x } { | C _ { 0 } \cap A | } \sum _ { i = 0 } ^ { \infty } p _ { i } \mathbb { E } [ \delta _ { i } ^ { 4 } | V _ { i + 1 } = x ] \\ & = c ( \mu ) \int _ { C _ { 0 } \cap A } \frac { d x } { | C _ { 0 } \cap A | } \mathbb { E } \Delta ( \mathcal { P } \cap ( A - x ) ) ^ { 4 } . \\ \intertext { B y the P o i s s o n b o u d e n d e m o t i n d e c t i o n , a n d t h e f a t h \mu \leq \lambda , this is }$$

By the Poisson bounded moments condition, and the fact that μ ≤ λ , this is uniformly bounded, yielding (3.3). ✷

Proof of Theorem 3.1. The proof is similar to that of Theorem 2.1 of [19], adapted to the continuum. Note that Pscript n has the same distribution as Pscript ∩ Bn , so for this proof without loss of generality we assume Pscript n = Pscript ∩ Bn .

For x ∈ Zopen d , let Fscript x denote the σ -field generated by the points of Pscript in ∪ y ⪯ xQ 1 / 2 lparenOSCASB y rparenOSCASB , where y ⪯ x means y ∈ Zopen d and y precedes or equals x in the lexicographic ordering on Zopen d . In other words, Fscript x is the smallest σ -field, with respect to which the number of Poisson points in any bounded Borel subset of ∪ y ⪯ xQ 1 / 2 lparenOSCASB y rparenOSCASB is measurable.

Let B ′ n be the set of lattice points x ∈ Zopen d such that vertSHT Q 1 / 2 lparenOSCASB x rparenOSCASB ∩ Bn vertSHT ̸= varnothing . Let kn = card lparenOSCASB B ′ n rparenOSCASB ; then kn/n tends to λ - 1 because of the vanishing relative boundary condition and the fact that

$$B _ { n } \subseteq \bigcup _ { x \in B _ { n } ^ { \prime } } Q _ { 1 / 2 } ( x ) \subseteq B _ { n } \cup \partial _ { 1 } ( B _ { n } ) . \\ \text {tion } ( \mathcal { E } _ { n } , \mathcal { E } _ { 1 } ) \text { as follows: let } \mathcal { E } _ { n } \text { be the }$$

$$D _ { i } = \mathbb { E } [ H ( \mathcal { P } _ { n } ) | \mathcal { L } _ { i } ] - \mathbb { E } [ H ( \mathcal { P } _ { n } ) | \mathcal { L } _ { i - 1 } ] = \mathbb { E } [ \Delta _ { x _ { i } } ( B _ { n } ) | \mathcal { F } _ { x _ { i } } ] , \\$$

Define the filtration lparenOSCASB Gscript 0 commaori Gscript 1 commaori periodori periodori periodori commaori Gscript kn rparenOSCASB as follows: let Gscript 0 be the trivial σ -field, label the elements of B ′ n in lexicographic order as x 1 commaori periodori periodori periodori commaori xkn and let Gscript i = Fscript xi for 1 ≤ i ≤ kn . Then H lparenOSCASB Pscript n rparenOSCASBƐ H lparenOSCASB Pscript n rparenOSCASB = ∑ kn i = 1 Di where we set

with Delta1 xi lparenOSCASB Bn rparenOSCASB defined by (3.1). By orthogonality of martingale differences, Var lbrackOSCASB H lparenOSCASB Pscript n rparenOSCASBrbrackOSCASB = Ɛ ∑ kn i = 1 D 2 i periodori By this fact, along with a CLT for martingale differences (Theorem (2.3) of [15]), it suffices to prove the conditions

$$\text {references} \, ( \text {Theorem} \, ( 2 . 3 ) \, \text {or} \, [ 1 5 ] , \, \text {it suffices} \, \mathfrak { o } \, \text {prove the condition} \\ ( 3 . 7 ) & & \sup _ { n \geq 1 } \mathbb { E } \left [ \max _ { 1 \leq i \leq k _ { n } } \left ( k _ { n } ^ { - 1 / 2 } | D _ { i } | \right ) ^ { 2 } \right ] < \infty , \\$$

$$k _ { n } ^ { - 1 / 2 } \max _ { 1 \leq i \leq k _ { n } } | D _ { i } | \stackrel { P } { \longrightarrow } 0 , \\$$

and for some σ 2 ≥ 0,

$$k _ { n } ^ { - 1 } \sum _ { i = 1 } ^ { k _ { n } } D _ { i } ^ { 2 } \stackrel { L ^ { 1 } } { \longrightarrow } \lambda \sigma ^ { 2 } . \\ \intertext { The factor of } \lambda \text { is included in } ( 3 , 9 ) \text { to make } \sigma ^ { 2 } \text { consistent}$$

The factor of λ is included in (3.9) to make σ 2 consistently defined.


<!-- p:11 -->


Using the representation Di = Ɛ lbrackOSCASB Delta1 xi lparenOSCASB Bn rparenOSCASBvertSHT Fscript xi rbrackOSCASB we may easily check conditions (3.7) and (3.8). Indeed, by the conditional Jensen's inequality we have

$$k _ { n } ^ { - 1 } \mathbb { E } \left [ \max _ { i \leq k _ { n } } D _ { i } ^ { 2 } \right ] & \leq k _ { n } ^ { - 1 } \sum _ { i = 1 } ^ { k _ { n } } \mathbb { E } [ D _ { i } ^ { 2 } ] \leq k _ { n } ^ { - 1 } \sum _ { i = 1 } ^ { k _ { n } } \mathbb { E } [ \Delta _ { x _ { i } } ( B _ { n } ) ^ { 2 } ] , \\ \intertext { ch is uniformly bounded by the alternative bounded moments condition ( }$$

whichisuniformlyboundedbythealternativeboundedmomentscondition(3.3).

For the second condition (3.8), we use Boole's and Markov's inequalities to obtain

$$P \left [ \max _ { 1 \leq i \leq k _ { n } } | D _ { i } | \geq k _ { n } ^ { 1 / 2 } \varepsilon \right ] & < \sum _ { i = 1 } ^ { k _ { n } } \frac { \mathbb { E } [ D _ { i } ^ { 4 } ] } { k _ { n } ^ { 2 } \varepsilon ^ { 4 } } , \\ \intertext { s o r e , a g a i n b y ( 3 . 3 ) . }$$

which tends to zero, again by (3.3).

We now prove (3.9). By the alternative stabilization condition (3.2), for each x ∈ Zopen d the variables Delta1 x lparenOSCASB A rparenOSCASB converge almost surely to a limit, denoted Delta1 x lparenOSCASB∞rparenOSCASB , as A → Ropen d through Bscript . For x ∈ Zopen d and A ∈ Bscript , let

$$F _ { x } ( A ) = \mathbb { E } [ \Delta _ { x } ( A ) | \mathcal { F } _ { x } ] ; \quad F _ { x } = \mathbb { E } [ \Delta _ { x } ( \infty ) | \mathcal { F } _ { x } ] . \\ \quad \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \$$

Then lparenOSCASB Fxcommaori x ∈ Zopen d rparenOSCASB is a stationary family of random variables. Set σ 2 = Ɛ lbrackOSCASB F 2 0 rbrackOSCASB /λ . We claim that the pointwise ergodic theorem (see [4], Chapter 6) implies

$$m p r e s & & k _ { n } ^ { - 1 } \sum _ { x \in B _ { n } ^ { \prime } } F _ { x } ^ { 2 } \stackrel { L ^ { 1 } } { \longrightarrow } \lambda \sigma ^ { 2 } . \\ & & \intertext { ( 3 . 1 0 ) } \text {To prove this let } e _ { 1 } = ( 1 0 \intertext { ( 3 . 1 0 ) } \text {To prove this let } e _ { 2 } = ( 2 E ^ { d } \intertext { ( 3 . 1 0 ) } \text {To prove this let } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( 3 . 1 0 ) } \intertext { ( $$

$$\begin{array} { r l } & { ( B _ { n } ) _ { n \geq 1 } ^ { n \geq 1 } \text { as $var$ isometric relative bounded} y , \text { in } n _ { n } \to \infty ( k _ { n } / k _ { n } ) = 1 . \text { writing } \| \cdot \| _ { 1 } } \\ & { \text { for the $L^{1-norm of random variables, we have } } } \\ & { \left \| \begin{pmatrix} k _ { n } ^ { - 1 } \sum _ { x \in B _ { n } ^ { x } } F _ { x } ^ { 2 } \right ) - \lambda \sigma ^ { 2 } \right \| _ { 1 } \leq k _ { n } ^ { - 1 } \left \| \left ( \sum _ { x \in B _ { n } ^ { x } } F _ { x } ^ { 2 } \right ) - k _ { n } ^ { * } \lambda \sigma ^ { 2 } \right \| _ { 1 } } \\ & { ( 3 . 1 1 ) } & \\ & { + k _ { n } ^ { - 1 } \left \| \left ( \sum _ { x \in B _ { n } ^ { \wedge } \ \{ B _ { n } ^ { x } \} } F _ { x } ^ { 2 } \right ) - ( k _ { n } - k _ { n } ^ { * } ) \lambda \sigma ^ { 2 } \right \| _ { 1 } } \\ & { + } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad } & \\ & { \quad }$$

To prove this, let e 1 = lparenOSCASB 1 commaori 0 commaori periodori periodori periodori commaori 0 rparenOSCASB ∈ Zopen d . The variables Fne 1 , n ≥ 1, form an ergodic sequence because they take the form f lparenOSCASB T n lparenOSCASB V rparenOSCASBrparenOSCASB where T is a shift operator on an i.i.d. sequence V = lbraceOSCASB Vzcommaori z ∈ Zopen rbraceOSCASB . Given ε &gt; 0, by the ergodic theorem we can choose K &gt; 0 such that for all n ≥ K , the average of F 2 e 1 commaoriF 2 2 e 1 commaori periodori periodori periodori commaoriF 2 ne 1 is within an L 1 distance at most ε of λσ 2 . Divide B ′ n into one-dimensional intervals by which we mean maximal subsets of Bn of the form lparenOSCASB Zopen ∩ lbrackOSCASB acommaorib rbrackOSCASBrparenOSCASB ×lbraceOSCASB z 2 rbraceOSCASB ×··· × lbraceOSCASB zd rbraceOSCASB , with acommaori bcommaoriz 2 commaori periodori periodori periodori commaorizd in Zopen . Let B ∗ n be the union of constituent intervals of length at least K . Let k ∗ n = card lparenOSCASB B ∗ n rparenOSCASB . Since lparenOSCASB Bn rparenOSCASB n ≥ 1 has vanishing relative boundary, lim n →∞lparenOSCASB k ∗ n /kn rparenOSCASB = 1. Writing VertSHT · VertSHT 1 for the L 1 -norm of random variables, we have

∥ ∥ By the choice of K and translation-invariance, for each interval I of length at least K the average of F 2 z commaori z ∈ I , is within an L 1 -distance ε of Ɛ lbrackOSCASB F 2 0 rbrackOSCASB . Therefore the first term on the right-hand side of (3.11) is at most ε , while the second term tends to zero because lparenOSCASB k ∗ n /kn rparenOSCASB → 1. Therefore the left side of (3.11) is less than 2 ε for large n , and (3.10) follows.


<!-- p:12 -->


We need to show that Fx lparenOSCASB Bn rparenOSCASB 2 approximates to F 2 x . We consider x at the origin 0. For any A ∈ Bscript , by Cauchy-Schwarz,

By the definition of F 0 and the conditional Jensen's inequality,

$$\mathbb { E } [ | F _ { 0 } ( A ) ^ { 2 } - F _ { 0 } ^ { 2 } | ] & \leq ( \mathbb { E } [ ( F _ { 0 } ( A ) + F _ { 0 } ) ^ { 2 } ] ) ^ { 1 / 2 } ( \mathbb { E } [ ( F _ { 0 } ( A ) - F _ { 0 } ) ^ { 2 } ] ) ^ { 1 / 2 } . \\ \\ \mathbb { D } _ { 0 } ( 1 ) _ { 0 } \, \varrho _ { 0 } \cdots \varrho _ { 0 } & \colon _ { 0 } F _ { 0 } \\$$

$$\mathbb { E } [ ( F _ { 0 } ( A ) + F _ { 0 } ) ^ { 2 } ] & = \mathbb { E } [ ( \mathbb { E } [ \Delta _ { 0 } ( A ) + \Delta _ { 0 } ( \infty ) | \mathcal { F } _ { 0 } ] ) ^ { 2 } ] \\ & \leq \mathbb { E } [ \mathbb { E } [ ( \Delta _ { 0 } ( A ) + \Delta _ { 0 } ( \infty ) ) ^ { 2 } | \mathcal { F } _ { 0 } ] ] = \mathbb { E } [ ( \Delta _ { 0 } ( A ) + \Delta _ { 0 } ( \infty ) ) ^ { 2 } ] \\ \text {which is uniformly bounded by the alternative stabilization and bounded}$$

which is uniformly bounded by the alternative stabilization and bounded moments conditions (3.2) and (3.3). Similarly,

$$& \mathbb { E } [ ( F _ { 0 } ( A ) - F _ { 0 } ) ^ { 2 } ] \leq \mathbb { E } [ ( \Delta _ { 0 } ( A ) - \Delta _ { 0 } ( \infty ) ) ^ { 2 } ] . \\ & \\ & \mathbb { E } ( A _ { 0 } ) = 1 ( A _ { 0 } ) + 1 ; \quad 1 - A _ { 0 } = 1 , \quad 1 - A _ { 0 } = 1 , \quad 1 - A _ { 0 } = 1 ,$$

Returning to the given sequence lparenOSCASB Bn rparenOSCASB , let ε &gt; 0. By the vanishing relative boundary condition, we can choose Kn so that lim n →∞ Kn = ∞ and vertSHT ∂Kn lparenOSCASB Bn rparenOSCASBvertSHT ≤ εn for all n . Set B ′′ n = B ′ n \ ∂Kn Bn . Using the conclusion of the previous paragraph and translation-invariance, it is not hard to deduce that

By (3.2) and (3.3) this is also uniformly bounded. For any Bscript -valued sequence lparenOSCASB An rparenOSCASB n ≥ 1 tending to Ropen d , the sequence lparenOSCASB Delta1 0 lparenOSCASB An rparenOSCASBDelta1 0 lparenOSCASB∞rparenOSCASBrparenOSCASB 2 tends to 0 a.s. by (3.2), and is uniformly integrable by (3.3), and therefore (see [4], Chapter 4, Theorem 5.2) the expression (3.12) tends to zero so that Ɛ lbrackOSCASBvertSHT F 0 lparenOSCASB An rparenOSCASB 2 - F 2 0 vertSHTrbrackOSCASB→ 0.

$$\lim _ { n \to \infty } \sup _ { x \in B _ { n } ^ { \prime \prime } } \mathbb { E } [ | F _ { x } ( B _ { n } ) ^ { 2 } - F _ { x } ^ { 2 } | ] = 0 .$$

Using (3.13), the uniform boundedness of Ɛ lbrackOSCASBvertSHT Fx lparenOSCASB Bn rparenOSCASB 2 - F 2 x vertSHTrbrackOSCASB and the fact that ε can be taken arbitrarily small in the above argument, it is routine to deduce that

$$k _ { n } ^ { - 1 } \sum _ { x \in B _ { n } } \left ( F _ { x } ( B _ { n } ) ^ { 2 } - F _ { x } ^ { 2 } \right ) \stackrel { L ^ { 1 } } { \longrightarrow } 0 , \\ \intertext { \text {() remains true with } F \ \text { replaced by } F } \text {() remains true with } F \ \text { replaced by } F$$

and therefore (3.10) remains true with Fx replaced by Fx lparenOSCASB Bn rparenOSCASB ; that is, (3.9) holds and the proof of Theorem 2.1 is complete. ✷

4. ProofofCLT:thenon-Poissoncase. In this section we prove Theorem 2.1, subject to showing that the limiting variance τ 2 is nonzero. The first step is to show that the conditions of Theorem 2.1 imply those of Theorem 3.1, as follows.

Lemma 4.1. If H satisfies the uniform bounded moments condition and is polynomially bounded, then H satisfies the Poisson bounded moments condition.

Proof. Suppose A ∈ Bscript . Let N be the number of Poisson points in A . Then

$$\mathbb { E } \Delta ( \mathcal { P } \cap A ) ^ { 4 } = \sum _ { m = 0 } ^ { \infty } P [ N = m ] \mathbb { E } \Delta ( \mathcal { Q } _ { m , \, A } ) ^ { 4 } .$$


<!-- p:13 -->


Assumingtheuniformboundedmomentscondition,therestriction of the sum to those m with λ vertSHT A vertSHT / 2 ≤ m ≤ 3 λ vertSHT A vertSHT / 2isuniformlybounded.ByCauchy-Schwarz, the remainder of the sum is bounded by the square root of Ɛ lbrackOSCASB Delta1 lparenOSCASB Pscript ∩ A rparenOSCASB 8 rbrackOSCASB P lbrackOSCASBvertSHTlparenOSCASB N - λ vertSHT A vertSHTrparenOSCASBvertSHT &gt; vertSHT A vertSHT / 2 rbrackOSCASB . By (2.7), this too is uniformly bounded. ✷

It follows from Lemma 4.1 that if H satisfies the conditions of Theorem 2.1, then Theorem 3.1 applies and we have (2.1) and (2.2). To de-Poissonize these limits and obtain (2.3) and (2.4), we use a technique related to that used in [11] and [12]. We make the definition

$$R _ { m , n } = H ( \mathcal { W } _ { m + 1 , n } ) - H ( \mathcal { W } _ { m , n } ) ,$$

and use the following coupling lemma.

Lemma 4.2. Suppose H is strongly stabilizing. Let ε &gt; 0 . Then there exists δ &gt; 0 and n 0 ≥ 1 such that for all n ≥ n 0 and all mcommaorim ′ ∈ lbrackOSCASBlparenOSCASB 1 - δ rparenOSCASB ncommaori lparenOSCASB 1 + δ rparenOSCASB n rbrackOSCASB with m &lt; m ′ , there exists a coupled family of variables DcommaoriD ′ commaori RcommaoriR ′ with the following properties:

- (i) D and D ′ each have the same distribution as Delta1 lparenOSCASB∞rparenOSCASB .
- (iii) lparenOSCASB RcommaoriR ′ rparenOSCASB have the same joint distribution as lparenOSCASB Rmcommaori n commaoriRm ′ commaorin rparenOSCASB .
- (ii) D and D ′ are independent.
- (iv) P lbrackOSCASBlbraceOSCASB D ̸= R rbraceOSCASB ∪ lbraceOSCASB D ′ ̸= R ′ rbraceOSCASBrbrackOSCASB &lt; εperiodori

Proof. Suppose we are given n . On a suitable probability space, let Pscript and Pscript ′ be independent homogeneous Poisson processes on Ropen d of intensity λ ; let UcommaoriU ′ commaoriV 1 commaoriV 2 commaori periodori periodori periodori be independent variables uniformly distributed over Bn , independent of Pscript and Pscript ′ . The variables U and U ′ will play the role of Umcommaori n and Um ′ commaorin .

Let N denote the number of points of Pscript ′′ lying in Bn (a Poisson variable with mean n ). Choose an ordering on the points of Pscript ′′ lying in Bn , uniformly at random from all N ! possible such orderings. Use this ordering to list the points of Pscript ′′ in Bn as W 1 commaoriW 2 commaori periodori periodori periodori commaoriWN . Also, set WN + 1 = V 1 commaori WN + 2 = V 2 commaori WN + 3 = V 3 and so on.

Let Pscript ′′ be the point process consisting of those points of Pscript which lie closer to U than to U ′ (in the Euclidean norm), together with those points of Pscript ′ which lie closer to U ′ than to U . Clearly Pscript ′′ is a Poisson process of rate λ on Ropen d , and moreover it is independent of U and of U ′ .

Let R = H lparenOSCASBlbraceOSCASB W 1 commaori periodori periodori periodori commaori Wmcommaori U rbraceOSCASBrparenOSCASBH lparenOSCASBlbraceOSCASB W 1 commaori periodori periodori periodori commaoriWm rbraceOSCASBrparenOSCASB . Let R ′ = H lparenOSCASBlbraceOSCASB W 1 commaori periodori periodori periodori commaori Wm ′ - 1 commaori UcommaoriU ′ rbraceOSCASBrparenOSCASB - H lparenOSCASBlbraceOSCASB W 1 commaori periodori periodori periodori commaoriWm ′ - 1 commaoriU rbraceOSCASBrparenOSCASB . The variables Ucommaori U ′ commaoriW 1 commaoriW 2 commaori W 3 commaori periodori periodori periodori are independent uniformly distributed variables on Bn , and therefore the pairs lparenOSCASB RcommaoriR ′ rparenOSCASB and lparenOSCASB Rmcommaori n commaoriRm ′ commaorin rparenOSCASB have the same joint distribution as claimed.

Let  ̃ Pscript be the translated point process Pscript - U . Similarly, let  ̃ Pscript ′ = Pscript ′ - U ′ . Clearly,  ̃ Pscript and  ̃ Pscript ′ are independent Poisson processes of rate λ on Ropen d . Let ScommaoriS ′


<!-- p:14 -->


be radii of stabilization for Pscript and Pscript ′ , respectively, and define

Then D and D ′ are independent, and each have the same distribution as Delta1 lparenOSCASB∞rparenOSCASB .

$$\text {of stabilization for } \widetilde { \mathcal { P } } \text { and } \widetilde { \mathcal { P } } ^ { \prime } , \text { respectively, and define} \\ D = \Delta ( \widetilde { \mathcal { P } } \cup B _ { S } ( 0 ) ) ; \quad D ^ { \prime } = \Delta ( \widetilde { \mathcal { P } } ^ { \prime } \cup B _ { S } ( 0 ) ) . \\ \text {and } D ^ { \prime } \text { are independent, and each have the same distribution} \\ \text {ains to show that } ( D , D ^ { \prime } ) = ( R , R ^ { \prime } ) \text { with high probability.} \, C$$

Set δ = ε lparenOSCASB 2 K rparenOSCASB - d / lparenOSCASB 18 λ rparenOSCASB . We assume vertSHT m - n vertSHT ≤ δn and vertSHT m ′ - n vertSHT ≤ δn . For n large enough, except on an event (denoted E 1 ) of probability at most ε/ 9, we have vertSHT N - m vertSHT ≤ 2 δn = ε lparenOSCASB 2 K rparenOSCASB - d n/ lparenOSCASB 9 λ rparenOSCASB , and likewise vertSHT N - m ′ vertSHT ≤ ε lparenOSCASB 2 K rparenOSCASB - d n/ lparenOSCASB 9 λ rparenOSCASB .

It remains to show that lparenOSCASB DcommaoriD ′ rparenOSCASB = lparenOSCASB RcommaoriR ′ rparenOSCASB with high probability. Choose K such that P lbrackOSCASB S &gt; K rbrackOSCASB &lt; ε/ 9 and P lbrackOSCASB S ′ &gt; K rbrackOSCASB &lt; ε/ 9. Using the vanishing relative boundary condition, take n to be so large that except on an event (denoted E 0 ) of probability less than ε/ 9, the positions of U and U ′ are sufficiently far from ∂Bn and from each other, that the cubes QK lparenOSCASB U rparenOSCASB and QK lparenOSCASB U ′ rparenOSCASB are contained entirely within Bn and also are such that every point of QK lparenOSCASB U rparenOSCASB lies closer to U than to U ′ and every point of QK lparenOSCASB U ′ rparenOSCASB lies closer to U ′ than to U .

Let E be the event that the set of points of lbraceOSCASB W 1 commaori periodori periodori periodori commaoriWm rbraceOSCASB lying in QK lparenOSCASB U rparenOSCASB is not the same as the set of points of Pscript lying in QK lparenOSCASB U rparenOSCASB . This will happen either if one or more of the lparenOSCASB N - m rparenOSCASB + 'discarded' points of Pscript ′′ or one or more of the lparenOSCASB m - N rparenOSCASB + 'added' points of lbraceOSCASB V 1 commaoriV 2 commaori periodori periodori periodori rbraceOSCASB lies in QK lparenOSCASB U rparenOSCASB . For each added or discarded point, the probability of lying in QK lparenOSCASB U rparenOSCASB is at most lparenOSCASB 2 K rparenOSCASB d λ/n , and so the probability of E , given that E 1 does not occur, is less than ε/ 9. Similarly, with E ′ denoting the event that the set of points of lbraceOSCASB W 1 commaori periodori periodori periodori commaoriWm ′ rbraceOSCASB lying in QK lparenOSCASB U ′ rparenOSCASB is not the same as the set of points of Pscript ′ lying in QK lparenOSCASB U ′ rparenOSCASB , we have P lbrackOSCASB E ′ vertSHT E c 1 rbrackOSCASB ≤ ε/ 9.

Combining all these estimates, using the definition of the radius of (strong) stabilization for Pscript and Pscript ′ , and using Boole's inequality, we obtain for large enough n that

$$P [ ( D , D ^ { \prime } ) \neq ( R , R ^ { \prime } ) ] & \leq P [ E _ { 0 } ] + P [ E _ { 1 } ] + P [ S > K ] + P [ S ^ { \prime } > K ] \\ & + P [ E \rangle E _ { 1 } ] + P [ E ^ { \prime } \rangle E _ { 1 } ] \leq \varepsilon .$$

✷

Lemma 4.3. Suppose H is strongly stabilizing and satisfies the uniform bounded moments condition. Let lparenOSCASB h lparenOSCASB n rparenOSCASBrparenOSCASB n ≥ 1 be a sequence with h lparenOSCASB n rparenOSCASB /n → 0 as n →∞ . Then

$$\lim _ { n \to \infty } \sup _ { n - h ( n ) \leq m \leq n + h ( n ) } | \mathbb { E } R _ { m , \, n } - \mathbb { E } \Delta ( \infty ) | = 0 . \\$$

Also

$$\lim _ { n \to \infty } \sup _ { n - h ( n ) \leq m < m ^ { \prime } \leq n + h ( n ) } | \mathbb { E } R _ { m , \, n } R _ { m ^ { \prime } , \, n } - ( \mathbb { E } \Delta ( \infty ) ) ^ { 2 } | = 0 \\$$

and

$$\lim _ { n \to \infty } \sup _ { n - h ( n ) \leq m \leq n + h ( n ) } | \mathbb { E } R _ { m , \, n } ^ { 2 } | < \infty .$$

Proof. Let m be an arbitrary integer satisfying n - h lparenOSCASB n rparenOSCASB ≤ m ≤ n + h lparenOSCASB n rparenOSCASB . Let ε &gt; 0. Provided n is large enough, by Lemma 4.2 we can find coupled variables D and R , with D having the same distribution as Delta1 lparenOSCASB∞rparenOSCASB , with R having the same distribution as Rmcommaori n and with P lbrackOSCASB D ̸= R rbrackOSCASB &lt; ε . Then


<!-- p:15 -->


$$\mathbb { E } R _ { m , \, n } = \mathbb { E } R = \mathbb { E } [ D ] - \mathbb { E } [ D 1 \{ D \neq R \} ] + \mathbb { E } [ R 1 \{ D \neq R \} ] . \\$$

By Cauchy-Schwarz and the Poisson and uniform moments conditions, there is a constant c , independent of ε , such that vertSHT Ɛ lbrackOSCASB D 1 lbraceOSCASB D ̸= R rbraceOSCASBrbrackOSCASBvertSHT ≤ cε 1 / 2 and vertSHT Ɛ lbrackOSCASB R 1 lbraceOSCASB D ̸= R rbraceOSCASBrbrackOSCASBvertSHT ≤ cε 1 / 2 . Since ε is arbitrarily small, (4.2) follows. Moreover, the proof of (4.4) is very similar and is omitted.

Next we consider mcommaorim ′ with n - h lparenOSCASB n rparenOSCASB ≤ m&lt;m ′ ≤ n + h lparenOSCASB n rparenOSCASB . By Lemma 4.2 we can find coupled variables DcommaoriD ′ commaori RcommaoriR ′ such that D and D ′ are independent and each have the same distribution as Delta1 lparenOSCASB∞rparenOSCASB , lparenOSCASB RcommaoriR ′ rparenOSCASB have the same joint distribution as lparenOSCASB Rmcommaori n commaoriRm ′ commaorin rparenOSCASB , and P lbrackOSCASBlparenOSCASB DcommaoriD ′ rparenOSCASB ̸= lparenOSCASB RcommaoriR ′ rparenOSCASBrbrackOSCASB &lt; ε . Then

$$,$$

$$\mathbb { E } [ R R ^ { \prime } ] - \mathbb { E } [ D D ^ { \prime } ] & = \mathbb { E } [ R R ^ { \prime } 1 \{ ( D , D ^ { \prime } ) \neq ( R , R ^ { \prime } ) \} ] \\ & - \mathbb { E } [ D D ^ { \prime } 1 \{ ( D , D ^ { \prime } ) \neq ( R , R ^ { \prime } ) \} ] , \\ \intertext { w c o v a b y } \mathbb { C } \text {cov} \Omega \Omega \text { and } \mathbb { C } \text { is a projection } \text { moment and uniform} \text { condition}$$

and by Cauchy-Schwarz and the Poisson and uniform moment conditions, the right-hand side has modulus bounded by a constant multiple of ε 1 / 2 . Since ε is arbitrarily small, (4.3) follows. ✷

Proof of Theorem 2.1. We prove here the limits (2.3) and (2.4). We defer showing the strict positivity of τ 2 until the next section.

$$\mathbb { E } \left [ ( n ^ { - 1 / 2 } ( H _ { n } ^ { \prime } - H _ { n } - ( N _ { n } - n ) \alpha ) ) ^ { 2 } \right ] \to 0 . \\$$

Let Hn = H lparenOSCASB Uscript ncommaorin rparenOSCASB and H ′ n = H lparenOSCASB Pscript n rparenOSCASB . For this proof, assume Pscript n is coupled to Uscript ncommaorin by setting Pscript n = lbraceOSCASB U 1 commaorin commaoriU 2 commaorin commaori periodori periodori periodori commaori UNncommaori n rbraceOSCASB with Nn an independent Poisson variable with mean n . Let α = Ɛ Delta1 lparenOSCASB∞rparenOSCASB . The first step is to prove that as n →∞ ,

To prove this, note that the expectation in the left-hand side is equal to

$$To prove this, note that the expectation in the left-hand side is equal to \\ & \sum _ { ( 4 . 6 ) } \mathbb { E } \left [ n ^ { - 1 } ( H ( \mathcal { W } _ { m , n } ) - H ( \mathcal { W } _ { n , n } ) - ( m - n ) \alpha ) ^ { 2 } \right ] P [ N _ { n } = m ] \\ & + n ^ { - 1 } \mathbb { E } \left [ ( H _ { n } ^ { \prime } - H _ { n } - ( N _ { n } - n ) \alpha ) ^ { 2 } 1 \{ | N _ { n } - n | > n ^ { 3 / 4 } \} \right ] . \\ \intertext { L e t . }$$

Let ε &gt; 0. By (4.1) and Lemma 4.3, there exists c &gt; 0 such that for large enough n and all m with n ≤ m ≤ n + n 3 / 4 ,

$$\mathbb { E } [ ( H ( \mathcal { W } _ { m , n } ) - H ( \mathcal { W } _ { n , n } ) - ( m - n ) \alpha ) ^ { 2 } ] \\ = \mathbb { E } \left [ \left ( \sum _ { l = n } ^ { m - 1 } ( R _ { l , n } - \alpha ) \right ) ^ { 2 } \right ] \leq \varepsilon ( m - n ) ^ { 2 } + c ( m - n ) , \\ \text {are the bound comes from expanding out the double sum arising from} \, t$$

$$^ { 2 }$$

where the bound comes from expanding out the double sum arising from the expectation of the squared sum. A similar argument applies when n - n 3 / 4 ≤ m ≤ n , and hence the first term in (4.6) is bounded by

$$n ^ { - 1 } \mathbb { E } [ \varepsilon ( N _ { n } - n ) ^ { 2 } + c | N _ { n } - n | ] ,$$


<!-- p:16 -->


which is bounded by 2 ε for n large enough. By the estimate (2.6) and Cauchy-Schwarz, there is a constant β 5 such that the second term in (4.6) is bounded by β 5 n β 5 lparenOSCASB P lbrackOSCASBvertSHT Nn - n vertSHT &gt; n 3 / 4 rbrackOSCASBrparenOSCASB 1 / 2 , which tends to zero. This completes the proof of (4.5).

$$n ^ { - 1 / 2 } H _ { n } ^ { \prime } & = n ^ { - 1 / 2 } H _ { n } + n ^ { - 1 / 2 } ( N _ { n } - n ) \alpha + n ^ { - 1 / 2 } ( H _ { n } ^ { \prime } - H _ { n } - ( N _ { n } - n ) \alpha ) . \\ \\ I _ { n } + t _ { n } - \dot { a } _ { n } + t _ { n } - \dot { a } _ { n } + t _ { n } - t _ { n } \dot { a } _ { n } + t _ { n } \dot { a } _ { n } + t _ { n } - t _ { n } + t _ { n } - t _ { n } - t _ { n } - t _ { n } ( 4 \tilde { F } )$$

We prove convergence of n - 1 Var lparenOSCASB Hn rparenOSCASB . This follows from the identity

In the right-hand side, the third term has variance tending to zero by (4.5), while the second term has variance α 2 and is independent of the first term. It follows that with σ 2 given by Theorem 3.1,

$$\sigma ^ { 2 } & = \lim _ { n \to \infty } n ^ { - 1 } \, V a r ( H _ { n } ^ { \prime } ) = \lim _ { n \to \infty } ( n ^ { - 1 } \, V a r ( H _ { n } ) ) + \alpha ^ { 2 } , \\ \rho _ { n } & = 3 \, \substack { 2 & 1 - 1 \, W _ { n } \, ( H _ { n } ) \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n } ) \, 2 \\ 2 & 2 \, 1 - 1 \, W _ { n } \, ( H _ { n }$$

Theorem 3.1 tells us that n - 1 / 2 lparenOSCASB H ′ n - Ɛ H ′ n rparenOSCASB Dscript -→ Nscript lparenOSCASB 0 commaoriσ 2 rparenOSCASB periodori Combined with (4.5) this gives us

so that σ 2 ≥ α 2 and n - 1 Var lparenOSCASB Hn rparenOSCASB→ τ 2 , where we set τ 2 = σ 2 - α 2 . This gives us (2.3).

$$n ^ { - 1 / 2 } ( H _ { n } - \mathbb { E } H _ { n } ^ { \prime } + ( N _ { n } - n ) \alpha ) \stackrel { \mathcal { I } } { \longrightarrow } \mathcal { W } ( 0 , \sigma ^ { 2 } ) , \\ \quad - 1 / 2 ( N _ { n } - n ) \quad i n g h t s c r { E } ( N _ { n } - n ) + \epsilon _ { n } \epsilon _ { n } + \epsilon _ { n } \epsilon _ { n } + \epsilon _ { n } \epsilon _ { n } + \epsilon _ { n } \epsilon _ { n } + \epsilon _ { n } \epsilon _ { n }$$

and since n - 1 / 2 lparenOSCASB Nn - n rparenOSCASB α is independent of Hn and is asymptotically normal with mean zero and variance α 2 , it follows by considering characteristic functions that

$$n ^ { - 1 / 2 } ( H _ { n } - \mathbb { E } H _ { n } ^ { \prime } ) \xrightarrow { \mathcal { I } } \mathcal { N } ( 0 , \sigma ^ { 2 } - \alpha ^ { 2 } ) . \\ \\ D _ { n } ( 4 \tilde { \Sigma } ) + \tilde { \mathbf h } _ { n } \sigma + \tilde { \mathbf t } _ { n } \sigma _ { n } + \tilde { \mathbf f } _ { n } - 1 / 2 \epsilon ( U _ { n } ^ { \prime } ) \ \ U _ { n } ( \Omega U _ { n } ^ { \prime } ) \ ) + \mathbf t _ { n } \tilde { \mathbf d } _ { n } + \tilde { \mathbf t } _ { n }$$

By (4.5), the expectation of n - 1 / 2 lparenOSCASB H ′ n - Hn -lparenOSCASB Nn - n rparenOSCASB α rparenOSCASB tends to zero, so in (4.7) we can replace Ɛ H ′ n by Ɛ Hn , which gives us (2.4). Save for showing that τ 2 is strictly positive, this completes the proof of Theorem 2.1.

5. A lower bound for the limiting variance. In this section we complete the proof of Theorem 2.1 by showing that the limiting variance τ 2 of n - 1 / 2 H lparenOSCASB Uscript ncommaorin rparenOSCASB is nonzero whenever the distribution of Delta1 lparenOSCASB∞rparenOSCASB is nondegenerate. Set α = Ɛ lbrackOSCASB Delta1 lparenOSCASB∞rparenOSCASBrbrackOSCASB , and using nondegeneracy, take δ &gt; 0 such that

In the following we think of n as 'fixed' but large enough for various estimates to hold. We construct a martingale in a manner different from that in Section 3. Let Fscript 0 be the trivial σ -field, let Fscript i = σ lparenOSCASB U 1 commaorin commaori periodori periodori periodori commaori Uicommaori n rparenOSCASB and write Ɛ i for conditional expectation given Fscript i . Define martingale differences Di = Ɛ iH lparenOSCASB Uscript ncommaorin rparenOSCASBƐ i - 1 H lparenOSCASB Uscript ncommaorin rparenOSCASB periodori Then H lparenOSCASB Uscript ncommaorin rparenOSCASBƐ H lparenOSCASB Uscript ncommaorin rparenOSCASB = ∑ n i = 1 Di , and by orthogonality of martingale differences,

$$P [ \Delta ( \infty ) > \alpha + 4 \delta ] & > 4 \delta . \\ \vdots \, 1 & \quad c \quad \i c \quad v \, 1 \quad 1 \quad v \, 2 .$$

$$( 5 . 1 ) & & \text {Var } H ( \mathcal { W } _ { n , n } ) = \sum _ { i = 1 } ^ { n } E [ D _ { i } ^ { 2 } ] . \\ \text {We look for lower bounds for } E [ D _ { i } ^ { 2 } ] . \text { Given } i \, < \, m , \, \text {let} \, G _ { i }$$

We look for lower bounds for E lbrackOSCASB D 2 i rbrackOSCASB . Given i ≤ m , let Gicommaori m = H lparenOSCASB Uscript mcommaorin rparenOSCASB - H lparenOSCASB Uscript mcommaorin \lbraceOSCASB Uicommaori n rbraceOSCASBrparenOSCASB , the 'contribution of Uicommaori n to H lparenOSCASB Uscript mcommaorin rparenOSCASB '. Let  ̃ Gicommaori m = H lparenOSCASB Uscript m + 1 commaorin \ lbraceOSCASB Uicommaori n rbraceOSCASBrparenOSCASBH lparenOSCASB Uscript mcommaorin \lbraceOSCASB Uicommaori n rbraceOSCASBrparenOSCASB . Then Di = Ɛ i lbrackOSCASB Gicommaori n -  ̃ Gicommaori n rbrackOSCASB periodori We start by looking at Gicommaori n . We approximate it by Gicommaori i which is a good approximation when i is close to n . By the coupling lemma (Lemma 4.2), we can find ε 1 &gt; 0 such that if i &gt; lparenOSCASB 1 - ε 1 rparenOSCASB n and n is sufficiently large, then


<!-- p:17 -->


$$P [ G _ { i , i } > \alpha + 3 \delta ] > 3 \delta . \\$$

Let η &gt; 0 (to be given later on) and choose ε 2 ∈ lparenOSCASB 0 commaoriε 1 rparenOSCASB so that if i &gt; lparenOSCASB 1 - ε 2 rparenOSCASB n , then P lbrackOSCASB Gicommaorin ̸= Gicommaori i rbrackOSCASB &lt; η . Then for i &gt; n lparenOSCASB 1 - ε 2 rparenOSCASB ,

$$\mathbb { E } [ | G _ { i , n } - G _ { i , i } | ] & \leq \eta ^ { 1 / 2 } \mathbb { E } [ ( G _ { i , n } - G _ { i , i } ) ^ { 2 } ] ^ { 1 / 2 } \leq c \eta ^ { 1 / 2 } , \\ \\$$

by the uniform bounded moments assumption. Provided η is small enough, this is less than δ 2 . Then by Markov's inequality,

$$P [ \mathbb { E } _ { i } [ | G _ { i , \, n } - G _ { i , \, i } | ] > \delta ] \leq \delta ^ { - 1 } \mathbb { E } [ | G _ { i , \, n }$$

$$P [ \mathbb { E } _ { i } G _ { i , n } \geq \alpha + 2 \delta ] > 2 \delta . \\$$

$$P [ \mathbb { E } _ { i } [ | G _ { i , \, n } - G _ { i , \, i } ] > \delta ] \leq \delta ^ { - 1 } \mathbb { E } [ | G _ { i , \, n } - G _ { i , \, i } | ] \leq \delta . \\ \text {Since } \mathbb { E } _ { i } G _ { i , \, n } = G _ { i , \, i } + \mathbb { E } _ { i } [ G _ { i , \, n } - G _ { i , \, i } ] , \, i t \text { follows that} \\ P [ \mathbb { E } _ { i } G _ { i , \, n } \geq \alpha + 2 \delta ] > 2 \delta .$$

Define f colonori Ropen → Ropen by f lparenOSCASB x rparenOSCASB = 0 for x ≤ α + δ and f lparenOSCASB x rparenOSCASB = 1 for x ≥ α + 2 δ , interpolating linearly between α + δ and α + 2 δ . Set Yi = f lparenOSCASB Ɛ i Gicommaori n rparenOSCASB . Then (5.2) implies that

$$\mathbb { E } [ ( G _ { i , \, n } - \alpha ) Y _ { i } ] = \mathbb { E } [ Y _ { i } \mathbb { E } _ { i } ( G _ { i , \, n } - \alpha ) ] \geq 4 \delta ^ { 2 } .$$

Next consider Ɛ lbrackOSCASBlparenOSCASB  ̃ Gicommaori n - α rparenOSCASB Yi rbrackOSCASB , writing the second factor as the sum of f lparenOSCASB Gicommaorii rparenOSCASB and f lparenOSCASB Ɛ i Gicommaori n rparenOSCASB - f lparenOSCASB Gicommaori i rparenOSCASB . We claim that there exists ε 3 ∈ lparenOSCASB 0 commaoriε 2 rparenOSCASB such that provided n is sufficiently large and i &gt; lparenOSCASB 1 - ε 3 rparenOSCASB n ,

Ɛ lbrackOSCASBlparenOSCASB  ̃ Gicommaori n - α rparenOSCASB f lparenOSCASB Gicommaori i rparenOSCASBrbrackOSCASB ≤ δ 2 periodori (5.4) This is because the two factors  ̃ Gicommaori n - α and f lparenOSCASB Gicommaori i rparenOSCASB are almost independent and the first of them has mean close to zero. More formally, it is proved as follows. By the proof of our coupling lemma (Lemma 4.2), provided ε 3 is sufficiently small we can take coupled variables RcommaoriR ′ commaori DcommaoriD ′ such that D and D ′ are independent and each have the same distribution as Delta1 lparenOSCASB∞rparenOSCASB , such that R and R ′ have the same joint distribution as  ̃ Gicommaori n and Gicommaori i , and such that P lbrackOSCASBlparenOSCASB RcommaoriR ′ rparenOSCASB ̸= lparenOSCASB DcommaoriD ′ rparenOSCASBrbrackOSCASB is small. Then

$$\mathbb { E } [ ( \tilde { G } _ { i , n } - \alpha ) f ( G _ { i , i } ) ] & = \mathbb { E } [ ( R - \alpha ) f ( R ^ { \prime } ) ] \\ & = \mathbb { E } [ ( D - \alpha ) f ( D ^ { \prime } ) ] - \mathbb { E } [ ( D - \alpha ) f ( D ^ { \prime } ) 1 \{ ( R , R ^ { \prime } ) \neq ( D , D ^ { \prime } ) \} ] \\ & + \mathbb { E } [ ( R - \alpha ) f ( R ^ { \prime } ) 1 \{ ( R , R ^ { \prime } ) \neq ( D , D ^ { \prime } ) \} ] ; \\ \intertext { t h e f r i s t o f t h e r e t h e r s i n t h e r i g h s y c h a y - S h w a r z }$$

the first of the three terms in the right side is zero, while by Cauchy-Schwarz and the Poisson and uniform bounded moments conditions, the second and third terms are bounded by a constant times the square root of P lbrackOSCASBlparenOSCASB RcommaoriR ′ rparenOSCASB ̸= lparenOSCASB DcommaoriD ′ rparenOSCASBrbrackOSCASB . This is less than δ 2 for an appropriate choice of ε 3 , justifying the claim (5.4).


<!-- p:18 -->


Since f ′ is bounded, and Gicommaorii is Fscript i -measurable, there is a constant c such that

$$\text {that} \quad & | \mathbb { E } [ ( \widetilde { G } _ { i , \, n } - \alpha ) ( f ( \mathbb { E } _ { i } G _ { i , \, n } ) - f ( G _ { i , \, i } ) ) ] | \\ & \leq \mathbb { E } [ ( \widetilde { G } _ { i , \, n } - \alpha ) ^ { 1 / 2 } \mathbb { E } [ ( f ( \mathbb { E } _ { i } G _ { i , \, n } ) - f ( G _ { i , \, i } ) ) ^ { 2 } ] ^ { 1 / 2 } \leq c \mathbb { E } [ ( \mathbb { E } _ { i } G _ { i , \, n } - G _ { i , \, i } ) ^ { 2 } ] ^ { 1 / 2 } \\ & = c \mathbb { E } [ ( \mathbb { E } _ { i } G _ { i , \, n } - G _ { i , \, i } ) ^ { 2 } ] ^ { 1 / 2 } \leq c \mathbb { E } [ ( G _ { i , \, n } - G _ { i , \, i } ) ^ { 2 } ] ^ { 1 / 2 } . \\ \text {However,}$$

However,

$$\mathbb { E } [ ( G _ { i , \, n } - G _ { i , \, i } ) ^ { 2 } ] \leq \mathbb { E } [ ( G _ { i , \, n } - G _ { i , \, i } ) ^ { 4 } ] ^ { 1 / 2 } P [ G _ { i , \, n } \neq G _ { i , \, i } ] ^ { 1 / 2 } \leq c ^ { \prime } \, \eta ^ { 1 / 2 } , \\ \intertext { o n d r o w i d o d }$$

and provided η was well chosen it follows that

Combining this with (5.4), for n large, we have

$$Combining this with ( b . 4 ) , & \text { for } h \text { lag} c , \text { we have } \mathbb { E } [ ( \widetilde { G } _ { i , \, n } - \alpha ) Y _ { i } ] = \mathbb { E } [ ( \widetilde { G } _ { i , \, n } - \alpha ) f ( G _ { i , \, i } ) ] \\ \mathbb { E } [ ( \widetilde { G } _ { i , \, n } - \alpha ) Y _ { i } ] = & \mathbb { E } [ ( \widetilde { G } _ { i , \, n } - \alpha ) f ( G _ { i , \, i } ) ] \\ & + \mathbb { E } [ ( \widetilde { G } _ { i , \, n } - \alpha ) ( f ( \mathbb { E } _ { i } G _ { i , \, n } ) - f ( G _ { i , \, i } ) ) ] \leq 2 \delta ^ { 2 } . \\ \text {Combined with } ( 5 . 3 ) & \text { this implies that for large } n \text { and } i \geq ( 1 - \varepsilon _ { 3 } ) n , \, \text { we have } \\ & \mathbb { E } [ ( G _ { i , \, n } - \widetilde { G } _ { i , \, n } ) Y _ { i } ] > 2 \delta ^ { 2 } .$$

$$| \mathbb { E } [ ( \widetilde { G } _ { i , \, n } - \alpha ) ( f ( \mathbb { E } _ { i } G _ { i , \, n } ) - f ( G _ { i , \, i } ) ) ] | & \leq \delta ^ { 2 } . \\ \intertext { this w i t h s w i t h s } \widetilde { G } _ { \widetilde { G } } \quad \alpha ) Y \, \downarrow = \mathbb { F } [ ( \widetilde { G } _ { \widetilde { G } } \, \alpha ) f ( G _ { \widetilde { G } } ) ]$$

Combined with (5.3) this implies that for large n and i ≥ lparenOSCASB 1 - ε 3 rparenOSCASB n , we have

Ɛ lbrackOSCASBlparenOSCASB Gicommaori n -  ̃ Gicommaori n rparenOSCASB Yi rbrackOSCASB ≥ 2 δ 2 periodori Hence, using the fact that Yi is Fscript i -measurable and lies in the range lbrackOSCASB 0 commaori 1 rbrackOSCASB , we obtain

2 δ 2 ≤ Ɛ lbrackOSCASB Yi Ɛ i lparenOSCASB Gicommaori n -  ̃ Gicommaori n rparenOSCASBrbrackOSCASB ≤ Ɛ lbrackOSCASBvertSHT Ɛ i lparenOSCASB Gicommaori n -  ̃ Gicommaori n rparenOSCASBvertSHTrbrackOSCASB = Ɛ lbrackOSCASBvertSHT Di vertSHTrbrackOSCASB commaori and hence, Ɛ lbrackOSCASB D 2 i rbrackOSCASB ≥ Ɛ lbrackOSCASBvertSHT Di vertSHTrbrackOSCASB 2 ≥ 4 δ 4 . Thus, using (5.1), we have Var H lparenOSCASB Uscript ncommaorin rparenOSCASB ≥ lparenOSCASB ε 3 n - 1 rparenOSCASBlparenOSCASB 4 δ 4 rparenOSCASB commaori and therefore τ 2 &gt; 0 by (2.3).

6. The k -nearest neighbors graph. Fix k ∈ Nopen and d ≥ 1 and let NG lparenOSCASB Xscript rparenOSCASB denote the k -nearest neighbors graph on a point set Xscript ⊂ Ropen d . Here we show that the total edge length and the number of components of the k -nearest neighbors graph on points in Ropen d satisfy strong stabilization as well as the bounded moments conditions. Using similar methods one can show that other functionals, such as the number of vertices of a fixed degree in the k -nearest neighbors graph, the number of vertices which are the nearest neighbors of exactly k other points and the number of vertices which are the l th nearest neighbors to their own k th nearest neighbors all satisfy the central limit behavior of Theorem 2.1 and Corollary 2.1. We will leave the details of these other applications to the reader. Laws of large numbers for the latter two functionals have been obtained by Henze [9].

A variant of NG lparenOSCASB Xscript rparenOSCASB which has also been considered in the literature is the directed graph NG ′ lparenOSCASB Xscript rparenOSCASB , formed by inserting a directed edge lparenOSCASB xcommaoriy rparenOSCASB whenever y is one of the k nearest neighbors of x . Thus, for example, the total length of NG ′ lparenOSCASB Xscript rparenOSCASB counts some of the edges of NG lparenOSCASB Xscript rparenOSCASB twice. It should be possible to modify proofs of our CLTs for NG lparenOSCASB Xscript rparenOSCASB to give analogous CLTs for NG ′ lparenOSCASB Xscript rparenOSCASB .

Throughout this section we assume λ = 1.


<!-- p:19 -->


6 . 1 . Total edge length. In this section, H lparenOSCASB Xscript rparenOSCASB denotes the total edge length of NG lparenOSCASB Xscript rparenOSCASB . Bickel and Breiman [2] prove, among other things, a CLT for the total edge length of NG ′ lparenOSCASB Xscript n rparenOSCASB , in the case k = 1; Avram and Bertsimas [1] prove a CLT for the total edge length of NG ′ lparenOSCASB Pscript n rparenOSCASB , in the case where all the sets Bn are cubes, but do not address the convergence of the variance. The following CLT extends these results.

Theorem 6.1 (CLT for total edge length of the k -nearest neighbors graph). There exists σ 2 &gt; 0 such that provided Bscript is regular in the sense of (2.5), as n →∞ , n - 1 Var lparenOSCASB H lparenOSCASB Pscript n rparenOSCASBrparenOSCASB→ σ 2 and

Additionally, there exists τ 2 ∈ lparenOSCASB 0 commaoriσ 2 rbrackOSCASB such that as n →∞ , n - 1 Var lparenOSCASB H lparenOSCASB Uscript ncommaorin rparenOSCASBrparenOSCASB → τ 2 , and

$$( 6 . 1 ) & & n ^ { - 1 / 2 } ( H ( \mathcal { P } _ { n } ) - \mathbb { E } H ( \mathcal { P } _ { n } ) ) \xrightarrow { \mathcal { I } } \mathcal { W } ( 0 , \sigma ^ { 2 } ) . \\ & & \\ 0 & 1 & 0 .$$

$$n ^ { - 1 / 2 } ( H ( \mathcal { U } _ { n , n } ) - \mathbb { E } H ( \mathcal { U } _ { n , n } ) ) \stackrel { \mathcal { I } } { \longrightarrow } \mathcal { N } ( 0 , \tau ^ { 2 } ) . \\ \\$$

$$n ^ { ( 1 / d ) - 1 / 2 } ( H ( \mathcal { X } _ { n } ^ { r } ) - \mathbb { E } H ( \mathcal { X } _ { n } ^ { r } ) ) \stackrel { \mathcal { I } } { \rightarrow } \mathcal { N } ( 0 , \tau ^ { 2 } ) .$$

Moreover, if Bscript 0 is regular then n lparenOSCASB 2 /d rparenOSCASB1 Var H lparenOSCASB Xscript n rparenOSCASB→ τ 2 and

To prove Theorem 6.1 it suffices to verify the conditions of Theorem 2.1 and Corollary 2.1. We do this in the remainder of this section. Note first that H is homogeneous of order 1. Also, H is polynomially bounded because H lparenOSCASB Xscript rparenOSCASB ≤ k diam lparenOSCASB Xscript rparenOSCASB card lparenOSCASB Xscript rparenOSCASB periodori

### Lemma 6.1. H is strongly stabilizing.

Proof. For simplicity we prove strong stabilization in dimension two, but the argument is easily extended to higher dimensions by using cones instead of triangles (for d = 1, take intervals instead of triangles). For each t &gt; 0 construct six disjoint equilateral triangles Tj lparenOSCASB t rparenOSCASB commaori 1 ≤ j ≤ 6 commaori such that the origin is a vertex of each triangle, such that each triangle has edge length t and such that Tj lparenOSCASB t rparenOSCASB ⊂ Tj lparenOSCASB u rparenOSCASB whenever t &lt; u .

Inserting the origin lbraceOSCASB 0 rbraceOSCASB into a point set can cause the addition of some edges and the removal of others. We claim that given the configuration of Pscript in B 4 R lparenOSCASB 0 rparenOSCASB , the set of added edges or removed edges is insensitive to the addition or removal of points outside B 4 R lparenOSCASB 0 rparenOSCASB , and therefore 4 R is a radius of stabilization for H .

Given the homogeneous Poisson point process Pscript of unit intensity on Ropen 2 , let the random variable R be the minimum t such that each triangle Tj lparenOSCASB t rparenOSCASB commaori 1 ≤ j ≤ 6 commaori contains at least k + 1 points from Pscript . Then R is a.s. finite, since Tj lparenOSCASB∞rparenOSCASB colonori= ∪ t&gt; 0 Tj lparenOSCASB t rparenOSCASB contains infinitely many Poisson points a.s.

To prove the claim, note first that the k nearest neighbors of the origin all lie in ∪ 6 j = 1 Tj lparenOSCASB R rparenOSCASB . Moreover, if a point at x has the origin as one of its k nearest neighbors, then x must lie in one of the six triangles Tj lparenOSCASB R rparenOSCASB ; if not it would lie in some trapezoid Tj lparenOSCASB t rparenOSCASB\ Tj lparenOSCASB R rparenOSCASB , and there would be k points in Tj lparenOSCASB R rparenOSCASB lying closer to x than the origin does. Moreover, if x lies in Tj lparenOSCASB R rparenOSCASB then its k nearest neighbors lie within a distance R and are unaffected by changes outside B 2 R lparenOSCASB 0 rparenOSCASB . This shows that the set of added edges is insensitive to changes outside B 2 R lparenOSCASB 0 rparenOSCASB .


<!-- p:20 -->


Next consider removed edges. All edges removed as a result of the insertion of a point at the origin are of the form lbraceOSCASB xcommaoriy rbraceOSCASB with x having 0 as one of its k nearest neighbors and having y as its lparenOSCASB k + 1 rparenOSCASB st nearest neighbor. As already seen, x must lie in one of the sets Tj lparenOSCASB R rparenOSCASB , and vertSHT y - x vertSHT ≤ R so that y ∈ B 2 R lparenOSCASB 0 rparenOSCASB . Then the edge lbraceOSCASB xcommaoriy rbraceOSCASB is indeed removed unless x is one of the k nearest neighbors of y . However, y has at least k points within a distance 2 R of it, and so the decision on whether to remove edge lbraceOSCASB xcommaoriy rbraceOSCASB is unaffected by changes outside B 4 R lparenOSCASB 0 rparenOSCASB , points outside B 4 R lparenOSCASB 0 rparenOSCASB all lying at a distance greater than 2 R from y . This proves the claim. ✷

Lemma 6.2. If Bscript is regular, then H satisfies the uniform bounded moments condition on Bscript .

Proof. Let A ∈ Bscript with 0 ∈ A , and let vertSHT A vertSHT / 2 ≤ m ≤ 3 vertSHT A vertSHT / 2. Let the m independent random points comprising Uscript mcommaoriA be denoted V 1 commaori periodori periodori periodori commaoriVm . Let L lparenOSCASB 0 rparenOSCASB be the total length of the edges incident to 0 in NG lparenOSCASB Uscript mcommaoriA ∪ lbraceOSCASB 0 rbraceOSCASBrparenOSCASB ; this is an upper bound for Delta1 lparenOSCASB Uscript mcommaoriA rparenOSCASB + , the positive part of Delta1 lparenOSCASB Uscript mcommaoriA rparenOSCASB . Let L max be the maximum of these edge lengths, and let Deg lparenOSCASB 0 rparenOSCASB be the degree of the vertex at the origin. Then

$$L ( 0 ) ^ { 4 } \leq \deg ( 0 ) ^ { 4 } L _ { \max } ^ { 4 } \leq \sum _ { i = 1 } ^ { m } W _ { i } ^ { 4 } , \\$$

where Wi denotes the product of vertSHT Vi vertSHT with the number of points of Uscript mcommaoriA in B vertSHT Vi vertSHT lparenOSCASB 0 rparenOSCASB (including Vi itself ) times the indicator of the event that lbraceOSCASB 0 commaoriVi rbraceOSCASB is an edge. Therefore,

$$\mathbb { E } [ L ( 0 ) ^ { 4 } ] & \leq m \mathbb { E } [ W _ { 1 } ^ { 4 } ] = m \int _ { A } | u | ^ { 4 } \mathbb { E } [ ( N _ { u } + 1 ) ^ { 4 } 1 \{ E _ { u } \} ] \frac { d u } { | A | } , \\$$

where Nu is the number of points of Uscript m - 1 commaoriA in B vertSHT u vertSHT lparenOSCASB 0 rparenOSCASB and where Eu is the event that u is joined to 0 in the k -nearest neighbors graph on Uscript m - 1 commaoriA ∪lbraceOSCASB 0 commaoriu rbraceOSCASB . By Cauchy-Schwarz and the fact that m ≤ 2 vertSHT A vertSHT by assumption,

$$\mathbb { E } [ L ( 0 ) ^ { 4 } ] & \leq 2 \int _ { A } | u | ^ { 4 } ( \mathbb { E } [ ( N _ { u } + 1 ) ^ { 8 } ] ) ^ { 1 / 2 } P [ E _ { u } ] ^ { 1 / 2 } \, d u . \\$$

The mean of Nu is bounded by a constant times vertSHT u vertSHT d , so by a standard estimate on the binomial distribution, its eighth moment is bounded by a constant times vertSHT u vertSHT 8 d . Also, Eu happens only if the ball B vertSHT u vertSHT lparenOSCASB u rparenOSCASB has at most k - 1 points or B vertSHT u vertSHT lparenOSCASB 0 rparenOSCASB has at most k - 1 points. Let θ denote the volume of the unit ball.


<!-- p:21 -->


For vertSHT A vertSHT / 2 ≤ m ≤ 3 vertSHT A vertSHT / 2, and vertSHT u vertSHT ≥ 1, we have by regularity (2.5),

$$\leq c | u | ^ { d ( k - 1 ) } \exp ( - ( \delta / 4 ) | u | ^ { \delta } ) . \\$$

$$P [ E _ { u } ] & \leq 2 \sum _ { j = 0 } ^ { k - 1 } \binom { m - 1 } { j } \left ( \frac { \theta | u | ^ { d } } { | A | } \right ) ^ { j } \left ( 1 - \frac { \delta | u | ^ { \delta } } { | A | } \right ) ^ { m - 1 - j } \\ & < c | u | ^ { d ( k - 1 ) } \exp ( - ( \delta / 4 ) | u | ^ { \delta } ) .$$

This shows that E lbrackOSCASB L lparenOSCASB 0 rparenOSCASB 4 rbrackOSCASB is uniformly bounded by a constant times

which is finite. Hence Delta1 lparenOSCASB Uscript mcommaoriA rparenOSCASB + has a uniformly bounded fourth moment.

$$\int _ { \mathbb { R } ^ { d } } | u | ^ { 4 + 4 d + d ( k - 1 ) } \exp ( - ( \delta / 4 ) | u | ^ { \delta } ) \, d u , \\ . \text { Hence } \Delta ( \mathcal { W } _ { m , A } ) ^ { + } \text { has a uniformly bounded fourth}$$

Now consider the fourth moment of Delta1 lparenOSCASB Uscript mcommaoriA rparenOSCASB - . Write Vi → 0 if 0 is one of the k nearest neighbors of Vi in the point process Uscript mcommaoriA ∪lbraceOSCASB 0 rbraceOSCASB . Also, let Li be the total length of all edges incident to Vi in NG lparenOSCASB Uscript mcommaoriA rparenOSCASB . Then Delta1 lparenOSCASB Uscript mcommaoriA rparenOSCASB - is bounded by the total length of deleted edges, and so is at most ∑ m i = 1 Li 1 lbraceOSCASB Vi → 0 rbraceOSCASB . Since the number of nonzero terms in this sum is bounded by a geometric constant C lparenOSCASB dcommaorik rparenOSCASB (see [23], page 102), it follows that there is a constant c such that

$$( \Delta ( \mathcal { W } _ { m , \, A } ) ^ { - } ) ^ { 4 } \leq c \sum _ { i = 1 } ^ { m } L _ { i } ^ { 4 } 1 \{ V _ { i } \to 0 \} . \\ \text {ions and using Cauchy-Schwarz yields}$$

$$\text {taking expectations and using Cauchy-Schwarz yields} \\ \mathbb { E } [ ( \Delta ( \mathcal { U } _ { m , A } ) ^ { - } ) ^ { 4 } ] \leq & \ m c \int _ { A } ( \mathbb { E } L ( x ) ^ { 8 } ) ^ { 1 / 2 } P [ x \to 0 ] ^ { 1 / 2 } \left ( \frac { d x } { | A | } \right ) . \\ \text {here } L ( x ) \text { is the total length of edges incident to } x \text { in } \text { NG} ( \{ x \} \cup \mathcal { U } _ { m - 1 } }$$

Taking expectations and using Cauchy-Schwarz yields

Here L lparenOSCASB x rparenOSCASB is the total length of edges incident to x in NG lparenOSCASBlbraceOSCASB x rbraceOSCASB ∪ Uscript m - 1 commaoriA rparenOSCASB , which has a bounded eighth moment by a similar argument to the above proof that L lparenOSCASB 0 rparenOSCASB has bounded fourth moment. Also, by the same argument as for (6.4), there are constants ccommaoriδ such that P lbrackOSCASB x → 0 rbrackOSCASB ≤ c vertSHT x vertSHT d lparenOSCASB k - 1 rparenOSCASB exp lparenOSCASBδ vertSHT x vertSHT δ rparenOSCASB for all x ∈ A . Hence, E lbrackOSCASBlparenOSCASB Delta1 lparenOSCASB Uscript mcommaoriA rparenOSCASB - rparenOSCASB 4 rbrackOSCASB is bounded uniformly in Acommaorim . This demonstrates the uniform moments condition.

Lemma 6.3. The distribution of Delta1 lparenOSCASB∞rparenOSCASB is nondegenerate.

Proof. Let C 0 = Q 1 / 2 lparenOSCASB 0 rparenOSCASB , the unit cube centered at the origin. The annulus Qd + 1 lparenOSCASB 0 rparenOSCASB\ C 0 will be called the moat. Partition the annulus Qd + 2 lparenOSCASB 0 rparenOSCASB\ Qd + 1 lparenOSCASB 0 rparenOSCASB into a finite collection Ascript of unit cubes. Now define the following events. Let E 2 be the event that there are no points in Pscript in the moat and there are at least k + 1 points in each of the unit subcubes in Ascript . Let E 1 be the intersection of E 2 and the event that there are k points in C 0 ; let E 0 be the intersection of E 2 and the event that there are no points in C 0 . Then E 0 and E 1 have strictly positive probability.

Now we notice that if E 0 occurs, then adding the origin creates k new edges and has no other effect. It increases the total edge length by at least kW , where W = d + 1 / 2 is the width of the moat. If E 1 occurs, then before adding the origin there are k edges crossing the moat. Adding the origin destroys these edges and reduces the total edge length by at least k lparenOSCASB W - w rparenOSCASB , where w = √ d is the diameter of C 0 .


<!-- p:22 -->


Thus E 0 and E 1 are events with strictly positive probability which give rise to values of Delta1 lparenOSCASB∞rparenOSCASB which differ by at least k lparenOSCASB W - w rparenOSCASB , a fixed amount. This demonstrates the nondegeneracy of Delta1 lparenOSCASB∞rparenOSCASB . ✷

Thus, H satisfies the conditions for Theorem 2.1 and Corollary 2.1, so Theorem 6.1 is proved.

6 . 2 . Number of components. In this section we let H lparenOSCASB Xscript rparenOSCASB be the number of components in NG lparenOSCASB Xscript rparenOSCASB .

Theorem 6.2 (CLT for the number of components of the k -nearest neighbors graph). There exists σ 2 &gt; 0 such that as n →∞ commaorin - 1 Var lparenOSCASB H lparenOSCASB Pscript n rparenOSCASBrparenOSCASB→ σ 2 and

$$n ^ { - 1 / 2 } ( H ( \mathcal { P } _ { n } ) - \mathbb { E } H ( \mathcal { P } _ { n } ) ) \stackrel { \mathcal { D } } { \longrightarrow } \mathcal { W } ( 0 , \sigma ^ { 2 } ) .$$

Additionally, there exists τ 2 ∈ lparenOSCASB 0 commaoriσ 2 rbrackOSCASB such that as n →∞ , n - 1 Var lparenOSCASB H lparenOSCASB Uscript ncommaorin rparenOSCASBrparenOSCASB→ τ 2 and

$$n ^ { - 1 / 2 } ( H ( \mathcal { U } _ { n , n } ) - \mathbb { E } H ( \mathcal { U } _ { n , n } ) ) \stackrel { \mathcal { D } } { \longrightarrow } \mathcal { N } ( 0 , \tau ^ { 2 } ) .$$

$$A l s o , \, n ^ { - 1 } \, V a r ( H ( \mathcal { X } _ { n } ) ) \to \tau ^ { 2 } \, a n d$$

$$n ^ { - 1 / 2 } ( H ( \mathcal { X } _ { n } ) - \mathbb { E } H ( \mathcal { X } _ { n } ) ) \stackrel { \mathcal { I } } { \longrightarrow } \mathcal { W } ( 0 , \tau ^ { 2 } ) .$$

Note that in this theorem, there is no requirement that Bscript or Bscript 0 be regular. We prove it by showing that H satisfies the conditions of Theorem 2.1 and Corollary 2.1. First note that H is homogeneous of order 0, and H is polynomially bounded because H lparenOSCASB Xscript rparenOSCASB ≤ card lparenOSCASB Xscript rparenOSCASB .

The proof of strong stabilization is more involved than it was for the total length. In particular, it requires a result of [7] on 'uniqueness of the infinite cluster' for the k -nearest neighbors graph on the infinite Poisson process Pscript .

It is quite simple to see that H satisfies the uniform bounded moments condition. Recall first that the degree of the vertices of the k -nearest neighbors graph is uniformly bounded by some constant C lparenOSCASB dcommaorik rparenOSCASB [23]. Thus, inserting an extra point into a given set of points causes the addition of at most C lparenOSCASB dcommaorik rparenOSCASB edges and cannot decrease the number of components by more than C lparenOSCASB dcommaorik rparenOSCASB . Moreover, the number of edges removed due to the insertion of an extra point is at most one for each point having the inserted point as one of its k nearest neighbors, and therefore is also bounded by C lparenOSCASB dcommaorik rparenOSCASB . Each removed edge increases the number of components by at most one, so inserting a point cannot increase the number of components by more than C lparenOSCASB dcommaorik rparenOSCASB . This demonstrates the uniform moments condition, with no extra requirement on Bscript .


<!-- p:23 -->


Lemma 6.4. (a) With probability 1 , NG lparenOSCASB Pscript rparenOSCASB has at most one infinite component.

(b) With probability 1 , NG lparenOSCASB Pscript ∪ lbraceOSCASB 0 rbraceOSCASBrparenOSCASB has at most one infinite component.

Proof. Part (a) is Theorem 4.1 of [7]. For part (b), let Eε be the event that there is a single point of Pscript in Bε lparenOSCASB 0 rparenOSCASB . Let A be the event that there is at most one infinite component in NG lparenOSCASB Pscript rparenOSCASB . Then P lbrackOSCASB A vertSHT Eε rbrackOSCASB = 1 for all ε &gt; 0, by part (a). Letting ε tend to zero gives the result. ✷

We now want to show that H satisfies strong stabilization. As before, we prove this only for the case d = 2. We prepare for the proof of stabilization with one final lemma. Recall the definitions of the six triangles Tj lparenOSCASB t rparenOSCASB used in the proof of Lemma 6.1. For each point X of Pscript let R lparenOSCASB X rparenOSCASB be the minimum t such that each of the translated triangles Tj lparenOSCASB t rparenOSCASB+ Xcommaori 1 ≤ j ≤ 6 commaori contains at least k + 1 points (not counting X itself) of Pscript . The significance of R lparenOSCASB X rparenOSCASB is that changes in the configuration outside B 2 R lparenOSCASB X rparenOSCASB lparenOSCASB X rparenOSCASB cannot have any effect on the set of edges of the k -nearest neighbors graph incident to X . This is seen by a similar argument to the proof of Lemma 6.1.

Lemma 6.5. With probability 1, the values of R lparenOSCASB X rparenOSCASB are finite for all points X of Pscript .

Proof. It suffices to prove the result for all points X ∈ Pscript ∩ Q 1 / 2 lparenOSCASB 0 rparenOSCASB . By integrating out the respective positions of the points in Q 1 / 2 lparenOSCASB 0 rparenOSCASB , one sees that it suffices to prove that for any finite subset lbraceOSCASB x 1 commaori periodori periodori periodori commaorixm rbraceOSCASB of Q 1 / 2 lparenOSCASB 0 rparenOSCASB , the triangles Tj lparenOSCASB∞rparenOSCASB+ xi commaori 1 ≤ i ≤ mcommaori 1 ≤ j ≤ 6, all have infinitely many points of Pscript \ Q 1 / 2 lparenOSCASB 0 rparenOSCASB a.s. However, this is clearly true. ✷

Proposition 6.1. H satisfies strong stabilization and the distribution of Delta1 lparenOSCASB∞rparenOSCASB is nondegenerate.

Proof. The insertion of the origin causes the addition of certain edges and the deletion of other edges. As seen in the proof of Lemma 6.1, all such edges lie within B 2 R lparenOSCASB 0 rparenOSCASB and the set of added edges and the set of deleted edges are insensitive to changes outside B 4 R lparenOSCASB 0 rparenOSCASB . We need to prove that the effect of these additions and deletions on the number of components is insensitive to changes in the configuration outside a certain range.

Let Cscript be the set of components of NG lparenOSCASB Pscript rparenOSCASB that include one or more vertices lying in B 4 R lparenOSCASB 0 rparenOSCASB . At most one of these components is infinite, by Lemma 6.4. Choose a finite L 1 &gt; 4 R such that BL 1 lparenOSCASB 0 rparenOSCASB contains all the fi nite components in the collection Cscript . For every pair of points XcommaoriY of Pscript ∩ B 4 R lparenOSCASB 0 rparenOSCASB which lie in the infinite component of NG lparenOSCASB Pscript rparenOSCASB (if there is one), there is a path in NG lparenOSCASB Pscript rparenOSCASB connecting X to Y . Since there are a.s. only finitely many points of Pscript in B 4 R lparenOSCASB 0 rparenOSCASB , we can a.s. find a finite L 2 &gt; L 1 such that for every pair of points XcommaoriY in B 4 R lparenOSCASB 0 rparenOSCASB which are also in the infinite component of NG lparenOSCASB Pscript rparenOSCASB , there is a path from X to Y staying within the ball BL 2 lparenOSCASB 0 rparenOSCASB .


<!-- p:24 -->


The upshot of the above argument is that for every pair XcommaoriY of points of Pscript ∩ B 4 R lparenOSCASB 0 rparenOSCASB , either there is a path from X to Y in NG lparenOSCASB Pscript rparenOSCASB that stays within BL 2 lparenOSCASB 0 rparenOSCASB , or at least one member of lbraceOSCASB XcommaoriY rbraceOSCASB lies in a finite component of NG lparenOSCASB Pscript rparenOSCASB that is contained within BL 2 lparenOSCASB 0 rparenOSCASB and does not include the other member of lbraceOSCASB XcommaoriY rbraceOSCASB .

The number of Poisson points in BL 3 lparenOSCASB 0 rparenOSCASB is a.s. finite. By Lemma 6.5, the balls B 2 R lparenOSCASB X rparenOSCASB lparenOSCASB X rparenOSCASB commaori X ∈ Pscript ∩ BL 3 lparenOSCASB 0 rparenOSCASB commaori all have finite radius. Take a finite L 4 &gt; L 3 , large enough for BL 4 lparenOSCASB 0 rparenOSCASB to contain all of these balls. Our claim is that L 4 is a radius of stabilization for H . This is because changes outside BL 4 lparenOSCASB 0 rparenOSCASB do not create or destroy any edges having at least one endpoint within BL 3 lparenOSCASB 0 rparenOSCASB , and therefore do not affect the question of whether there is a path from X to Y , for all XcommaoriY in B 4 R lparenOSCASB 0 rparenOSCASB . Let us now explicitly justify the claim.

Using part (b) of Lemma 6.4, we can similarly a.s. find a finite L 3 &gt; L 2 , such that for every pair XcommaoriY of points of lparenOSCASB Pscript ∪lbraceOSCASB 0 rbraceOSCASBrparenOSCASB∩ B 4 R lparenOSCASB 0 rparenOSCASB , either there is a path from X to Y in NG lparenOSCASB Pscript ∪lbraceOSCASB 0 rbraceOSCASBrparenOSCASB that stays within BL 3 lparenOSCASB 0 rparenOSCASB , or at least one member of lbraceOSCASB XcommaoriY rbraceOSCASB lies in a finite component of NG lparenOSCASB Pscript ∪ lbraceOSCASB 0 rbraceOSCASBrparenOSCASB that is contained within BL 3 lparenOSCASB 0 rparenOSCASB and does not include the other member of lbraceOSCASB XcommaoriY rbraceOSCASB . Thus, whether there is a path from X to Y is determined entirely by edges involving points in BL 3 lparenOSCASB 0 rparenOSCASB .

Let e 1 commaori periodori periodori periodori commaori e i be the set of added edges as a result of the insertion of the origin. Let Cscript 1 be the set of components of NG lparenOSCASB Pscript rparenOSCASB in the collection Cscript which are connected to the origin by one or more of the edges e 1 commaori periodori periodori periodori commaori e i . Then, regardless of what happens outside BL 4 lparenOSCASB 0 rparenOSCASB , the increment in the number of components, due to the addition of a vertex at 0 and edges e 1 commaori periodori periodori periodori commaori e i , is equal to 1 - card lparenOSCASB Cscript 1 rparenOSCASB .

Let Cscript ′ be the set of components of NG lparenOSCASB Pscript ∪ lbraceOSCASB 0 rbraceOSCASBrparenOSCASB that include one or more vertices lying in B 4 R lparenOSCASB 0 rparenOSCASB . The edges f 1 commaori periodori periodori periodori commaorifj (which are not edges of this graph) induce an adjacency relation on the set Cscript ′ , two elements of Cscript ′ being deemed adjacent if one or more of the f 1 commaori periodori periodori periodori commaorifj connects them together. If ν 1 denotes the cardinality of Cscript ′ , and ν 2 denotes the number of components of the graph with vertex set Cscript ′ and adjacency as just described, then the increment in the number of components due to adding edges f 1 commaori periodori periodori periodori commaorifj is precisely equal to ν 2 - ν 1 .

Let f 1 commaori periodori periodori periodori commaorifj be the set of edges deleted as a result of the insertion of the origin. After deleting these edges, having previously added the edges e 1 commaori periodori periodori periodori commaori e i , one ends up with the k -nearest neighbors graph on the point set with lbraceOSCASB 0 rbraceOSCASB inserted. We consider instead the reverse process, in which we start with the k -nearest neighbors graph on the point set with lbraceOSCASB 0 rbraceOSCASB inserted, and then remove edges f 1 commaori periodori periodori periodori commaorifj .

Combining the above arguments, we see that the increment in the number of components, due to the insertion of lbraceOSCASB 0 rbraceOSCASB , is equal to 1 - card lparenOSCASB Cscript rparenOSCASB+ ν 1 - ν 2 , regardless of what happens outside BL 4 lparenOSCASB 0 rparenOSCASB . Thus we have established strong stabilization, and Delta1 lparenOSCASB∞rparenOSCASB = 1 - card lparenOSCASB Cscript rparenOSCASB+ ν 1 - ν 2 .

Finally, let us check the distribution of Delta1 lparenOSCASB∞rparenOSCASB . It suffices to consider the events E 0 and E 1 from Section 6.1 and to note that if E 0 occurs then there is no increase in the number of components, whereas if E 1 occurs then the number of components increases by at least one. This completes the proof of Proposition 6.1. ✷


<!-- p:25 -->


The total number of components in the k -nearest neighbors graph thus satisfies the conditions of Theorem 2.1 and Corollary 2.1, and Theorem 6.2 is proved.

7. The sphere of influence graph. Fix d ≥ 1 and let SIG lparenOSCASB Xscript rparenOSCASB denote the SIG on a finite point set Xscript ⊂ Ropen d . We show that the total number of edges, the total edge length, the number of vertices of fixed degree and the total number of components of the SIG on points in Ropen d all satisfy the CLT behavior of Theorem 2.1. Along the way we show uniqueness of the infinite component in the SIG on an infinite Poisson process, which is of interest in its own right.

Throughout this section we assume λ = 1.

7 . 1 . Total number of edges. In this section, let H lparenOSCASB Xscript rparenOSCASB denote the number of edges in SIG lparenOSCASB Xscript rparenOSCASB . F ̈ uredi [5] has shown that Ɛ H lparenOSCASB Xscript n rparenOSCASB /n converges to a limit as n →∞ . We show that H satisfies the following CLT. In this way we recover most of the results of [10], we show a de-Poissonized version of their central limit theorem and we show convergence of the variance of the total number of edges.

Theorem 7.1 (CLT for the number of edges in the SIG). Suppose Bscript is regular. There exists σ 2 &gt; 0 such that as n →∞ commaorin - 1 Var lparenOSCASB H lparenOSCASB Pscript n rparenOSCASBrparenOSCASB→ σ 2 and

$$n ^ { - 1 / 2 } ( H ( \mathcal { P } _ { n } ) - \mathbb { E } H ( \mathcal { P } _ { n } ) ) \xrightarrow { \mathcal { I } } \mathcal { W } ( 0 , \sigma ^ { 2 } ) . \\ \\$$

Additionally, there exists τ 2 ∈lparenOSCASB 0 commaoriσ 2 rbrackOSCASB such that as n →∞ commaori n - 1 Var lparenOSCASB H lparenOSCASB Uscript ncommaorin rparenOSCASBrparenOSCASB→ τ 2 and

$$n ^ { - 1 / 2 } ( H ( \mathcal { U } _ { n , n } ) - \mathbb { E } H ( \mathcal { U } _ { n , n } ) ) \stackrel { \mathcal { I } } { \longrightarrow } \mathcal { V } ( 0 , \tau ^ { 2 } ) . \\$$

Also, if Bscript 0 is regular, n - 1 Var lparenOSCASB H lparenOSCASB Xscript n rparenOSCASBrparenOSCASB→ τ 2 , and

$$n ^ { - 1 / 2 } ( H ( \mathcal { X } _ { n } ) - \mathbb { E } H ( \mathcal { X } _ { n } ) ) \stackrel { \mathcal { I } } { \longrightarrow } \mathcal { W } ( 0 , \tau ^ { 2 } ) .$$

We will prove this result by showing that H satisfies the conditions of Theorem 2.1. Since SIG lparenOSCASB Xscript rparenOSCASB is a subgraph of the complete graph on Xscript , it follows that H satisfies the growth bound H lparenOSCASB Xscript rparenOSCASB ≤ lparenOSCASB card lparenOSCASB Xscript rparenOSCASBrparenOSCASB 2 commaori and so is polynomially bounded. Also, H is homogeneous of order 0.

### Lemma 7.1. H is strongly stabilizing.

Proof. Inserting a point at the origin creates new edges incident to the origin and may remove edges between points, but cannot create any new edges between two old points. Edges which are removed have a vertex which has the origin as a nearest neighbor. We will show that there is a random ball centered at the origin such that the set of added edges is a.s. determined by what happens inside the ball and likewise for the set of removed edges.


<!-- p:26 -->


To see this, consider an infinite cone C with its vertex at the origin, subtending an angle of π/ 6 radians [for d = 1, take C to be the interval lparenOSCASB 0 commaori ∞rparenOSCASB ]. Let R be the distance from 0 to its closest neighbor in Pscript ∩ C , and let Y be the point in C \ B 6 R lparenOSCASB 0 rparenOSCASB closest to 0. Then Y exists a.s., because there are a.s. infinitely many Poisson points in C (but only finitely many in any bounded region).

Given x ∈ C \ B vertSHT Y vertSHT lparenOSCASB 0 rparenOSCASB let x ′ = lparenOSCASBvertSHT Y vertSHT / vertSHT x vertSHTrparenOSCASB x . By the triangle inequality and the fact that sin lparenOSCASB π/ 6 rparenOSCASB = 1 / 2,

$$| x - Y | \leq | x - x ^ { \prime } | + | x ^ { \prime } - Y | \leq ( | x | - | Y | ) + ( | Y | / 2 ) \leq | x | - 3 R .$$

Therefore, the sphere of influence of x does not reach the interior of B 3 R lparenOSCASB 0 rparenOSCASB . Hence, no points in C at a distance more than vertSHT Y vertSHT from the origin will be connected to 0. Therefore, the configuration of points outside B 3 vertSHT Y vertSHT lparenOSCASB 0 rparenOSCASB has no effect on the set of points in C connected to 0.

Now consider a finite number of cones C 1 commaori periodori periodori periodori commaoriCm congruent to C , each with a vertex at 0 and with union Ropen d . By the above, there is a.s. a finite random number S 1 , which is equal to the maximum of m identically distributed copies of 3 vertSHT Y vertSHT , such that adding or removing points further than S from 0 does not affect the set of added edges. This gives strong stabilization of H for added edges.

Now we show that H is strongly stabilizing for deleted edges. We will follow the cone argument described above. For 1 ≤ i ≤ m let xi be the closest Poisson point in Ci to the origin. The set of vertices having the origin as a nearest neighbor is a subset of lbraceOSCASB x 1 commaori periodori periodori periodori commaorixm rbraceOSCASB . Let R ′ i be the distance from 0 to its second nearest neighbor in the cone Ci and let R ′ = max lparenOSCASB R 1 commaori periodori periodori periodori commaoriRm rparenOSCASB . Note that for 1 ≤ i ≤ m , the sphere of influence of xi (before the addition of the origin) is contained in B 2 R ′ lparenOSCASB 0 rparenOSCASB .

Let Y ′ i be the point in Ci \ B 6 R ′ lparenOSCASB 0 rparenOSCASB closest to 0. By a similar argument to (7.4), for any point in Ci further out than Y ′ i the sphere of influence does not reach B 3 R ′ lparenOSCASB 0 rparenOSCASB , and so does not meet any of the spheres of influence of the points xjcommaori 1 ≤ j ≤ m . Thus, if we set S 2 = max1 ≤ i ≤ m vertSHT Y ′ i vertSHT , only edges involving points inside BS 2 lparenOSCASB 0 rparenOSCASB are possibly deleted as a result of inserting lbraceOSCASB 0 rbraceOSCASB , and moreover these points all lie within a distance at most S 2 + R ′ of the points xi , so their spheres of influence are unaffected by changes outside B 3 S 2 lparenOSCASB 0 rparenOSCASB . Therefore 3 S 2 serves as a radius of stabilization for deleted edges. Combined with the earlier argument for added edges, this shows that H is strongly stabilizing. ✷

Lemma 7.2. If Bscript is regular, then H satisfies the uniform bounded moments condition on Bscript .

Proof. The proof is quite similar to that of Lemma 6.2. Let A ∈ Bscript with 0 ∈ A , and assume vertSHT A vertSHT / 2 ≤ m ≤ 3 vertSHT A vertSHT / 2. Let the independent random points comprising Uscript mcommaoriA be denoted V 1 commaori periodori periodori periodori commaoriVm .


<!-- p:27 -->


Consider first the positive part Delta1 lparenOSCASB Uscript mcommaoriA rparenOSCASB + of Delta1 lparenOSCASB Uscript mcommaoriA rparenOSCASB . Let D lparenOSCASB 0 rparenOSCASB denote the degree of zero in SIG lparenOSCASB Uscript mcommaoriA ∪lbraceOSCASB 0 rbraceOSCASBrparenOSCASB . Inserting a point causes some of the existing spheres of influence to shrink and leaves the others unchanged and so does not create any new edges of the SIG except for those incident to the inserted point itself. Therefore Delta1 lparenOSCASB Uscript mcommaoriA rparenOSCASB + ≤ D lparenOSCASB 0 rparenOSCASB .

$$& \text {and} \ \text {inc} \ \text {in} \ \text {dec} \ \text {in} \ \text {u} \ \text {i} \ \text {s} \ \text {in} \ \text {d} \ \text {u} \ \text {c} \ \text {dec} \ \text {i} \ \text {c} \ \text {dec} \ \text {i} , \\ & \quad \text {etc} \quad \mathbb { E } [ D ( 0 ) ^ { 4 } ] \leq m \mathbb { E } [ W _ { 1 } ^ { 4 } ] = m \int _ { A } \mathbb { E } [ ( N _ { u } + 1 ) ^ { 4 } 1 \{ E _ { u } \} ] \frac { d u } { | A | } , \\ & \text {where } N _ { u } \text { is the number of points of } \mathcal { W } _ { m - 1 } \ A \text { in } B _ { | u | } ( 0 ) \text { and where } E _ { u } \text { is } t$$

Since one of the points Vi must be the furthest out from the origin among those adjacent to it in the SIG, we have D lparenOSCASB 0 rparenOSCASB 4 ≤ ∑ m i = 1 W 4 i commaori where Wi denotes the product of the number of points of Uscript mcommaoriA in B vertSHT Vi vertSHT lparenOSCASB 0 rparenOSCASB (including Vi itself), and the indicator of the event that lbraceOSCASB 0 commaoriVi rbraceOSCASB is an edge. Therefore,

where Nu is the number of points of Uscript m - 1 commaoriA in B vertSHT u vertSHT lparenOSCASB 0 rparenOSCASB and where Eu is the event that u is joined to 0 in the SIG on Uscript m - 1 commaoriA ∪lbraceOSCASB 0 commaoriu rbraceOSCASB . By Cauchy-Schwarz and the fact that m ≤ 2 vertSHT A vertSHT by assumption,

The eighth moment of Nu is bounded by a constant times vertSHT u vertSHT 8 d . Also, Eu happens only if the ball B vertSHT u vertSHT / 4 lparenOSCASB u rparenOSCASB contains no points or B vertSHT u vertSHT / 4 lparenOSCASB 0 rparenOSCASB contains no points. For vertSHT u vertSHT ≥ 1, regularity (2.5) yields

$$\text {act that } & \mathcal { M } \leq 2 | A | \text { by assumption} , \\ & \mathbb { E } [ D ( 0 ) ^ { 4 } ] \leq 2 \int _ { A } ( \mathbb { E } [ ( N _ { u } + 1 ) ^ { 8 } ] ) ^ { 1 / 2 } P [ E _ { u } ] ^ { 1 / 2 } \, d u . \\ \text {th moment of } & \ N _ { u } \text { is bounded by a constant times } | u | ^ { 8 d } .$$

$$P [ E _ { u } ] & \leq 2 \left ( 1 - \frac { ( \delta | u | / 4 ) ^ { \delta } } { | A | } \right ) ^ { n - 2 } \leq c \exp ( - ( \delta / 4 ^ { 1 + \delta } ) | u | ^ { \delta } ) . \\ \intertext { b m o n b i n g i n s } \text {bending these estimates gives us a uniform bound for the fourth m o n b i n g i n s}$$

Now consider the fourth moment of Delta1 lparenOSCASB Uscript mcommaoriA rparenOSCASB - . Write Vi → 0 if 0 is the nearest neighbor of Vi in the point process Uscript mcommaoriA ∪lbraceOSCASB 0 rbraceOSCASB , and let Di denote the degree of Vi in SIG lparenOSCASB Uscript mcommaoriA rparenOSCASB .

Combining these estimates gives us a uniform bound for the fourth moment of E lbrackOSCASB D lparenOSCASB 0 rparenOSCASB 4 rbrackOSCASB and hence for that of Delta1 lparenOSCASB Uscript mcommaoriA rparenOSCASB + .

Inserting a point at the origin causes the sphere of inference of Vi to shrink only if Vi → 0, and therefore causes the possible deletion of an existing edge lbraceOSCASB VicommaoriVj rbraceOSCASB of SIG lparenOSCASB Uscript mcommaoriA rparenOSCASB only if either Vi → 0 or Vj → 0 (or both). Therefore Delta1 lparenOSCASB Uscript mcommaoriA rparenOSCASB - ≤ ∑ m i = 1 Di 1 lbraceOSCASB Vi → 0 rbraceOSCASB periodori Since the number of nonzero terms in this sum is bounded by a geometric constant C lparenOSCASB dcommaorik rparenOSCASB ([23], page 102), it follows that there is a constant c such that lparenOSCASB Delta1 lparenOSCASB Uscript mcommaoriA rparenOSCASB - rparenOSCASB 4 ≤ c ∑ m i = 1 D 4 i 1 lbraceOSCASB Vi → 0 rbraceOSCASB periodori Taking expectations and using Cauchy-Schwarz yields

Here D lparenOSCASB x rparenOSCASB is degree of x in SIG lparenOSCASBlbraceOSCASB x rbraceOSCASB ∪ Uscript m - 1 commaoriA rparenOSCASB , which has a bounded eighth moment by a similar argument to the above proof that D lparenOSCASB 0 rparenOSCASB has bounded fourth moment. Also, by regularity, there are constants ccommaoriδ such that P lbrackOSCASB x → 0 rbrackOSCASB ≤ c exp lparenOSCASBδ vertSHT x vertSHT δ rparenOSCASB for all x ∈ A . Hence, E lbrackOSCASBlparenOSCASB Delta1 lparenOSCASB Uscript mcommaoriA rparenOSCASB - rparenOSCASB 4 rbrackOSCASB is bounded uniformly in A . This shows the uniform moments condition. ✷

$$\begin{array} { r } { \text {expectations and using Cauchy-Schwarz yields} } \\ { \mathbb { E } [ ( \Delta ( \mathcal { U } _ { m , \, A } ) ^ { - } ) ^ { 4 } ] \leq m c \int _ { A } ( \mathbb { E } D ( x ) ^ { 8 } ) ^ { 1 / 2 } P [ x \to 0 ] ^ { 1 / 2 } \left ( \frac { d x } { | A | } \right ) . } \\ { \text {here} \, D ( x ) \, is \, degree \, of \, x \, in \, S I G ( \{ x \} \cup \mathcal { U } _ { m - 1 } \, A ) , \, which \, has \, a \, bounded \, \text {eighth} } \end{array}$$

Lemma 7.3. The distribution of Delta1 lparenOSCASB∞rparenOSCASB is nondegenerate.


<!-- p:28 -->


Proof. We will use a construction similar to that used for the k -nearest neighbors graph. Let E 2 be the event that the moat is empty and that there are two points of Pscript in each of the unit subcubes in Ascript . Let E 0 be the intersection of E 2 and the event that there is no point of Pscript in C 0 . Let E 1 be the intersection of E 2 and the event that there is one point of Pscript in the ball B 1 / 10 lparenOSCASB 1 / 4 commaori 0 commaori periodori periodori periodori commaori 0 rparenOSCASB , and there are no other points in C 0 .

Each of E 0 and E 1 have positive probability. Inserting the origin when E 0 happens creates at least one additional edge across the moat and does not destroy any edges. Inserting the origin when E 1 happens creates a single new edge inside C 0 and destroys at least one edge across the moat. So the events E 0 and E 1 have strictly positive probability and give rise to values of Delta1 lparenOSCASB∞rparenOSCASB which differ by at least 1. This shows nondegeneracy of Delta1 lparenOSCASB∞rparenOSCASB . ✷

We have shown that H satisfies the conditions of Theorem 2.1 and Corollary 2.1. Together, these results give us Theorem 7.1.

7 . 2 . Total edge length. In this section, H lparenOSCASB Xscript rparenOSCASB denotes the total edge length of SIG lparenOSCASB Xscript rparenOSCASB .

Theorem 7.2 (CLT for the total edge length in the SIG). Suppose that Bscript is regular. Then there exists σ 2 &gt; 0 such that as n →∞ commaorin - 1 Var lparenOSCASB H lparenOSCASB Pscript n rparenOSCASBrparenOSCASB→ σ 2 and

$$n ^ { - 1 / 2 } ( H ( \mathcal { P } _ { n } ) - \mathbb { E } H ( \mathcal { P } _ { n } ) ) \stackrel { \mathcal { I } } { \longrightarrow } \mathcal { W } ( 0 , \sigma ^ { 2 } ) .$$

Additionally, there exists τ 2 ∈ lparenOSCASB 0 commaoriσ 2 rbrackOSCASB such that as n →∞ commaorin - 1 Var lparenOSCASB H lparenOSCASB Uscript ncommaorin rparenOSCASBrparenOSCASB→ τ 2 , and

$$n ^ { - 1 / 2 } ( H ( \mathcal { U } _ { n , n } ) - \mathbb { E } H ( \mathcal { U } _ { n , n } ) ) \stackrel { \mathcal { G } } { \longrightarrow } \mathcal { V } ( 0 , \tau ^ { 2 } ) .$$

Also, if Bscript 0 is regular, n lparenOSCASB 2 /d rparenOSCASB1 Var lparenOSCASB H lparenOSCASB Xscript n rparenOSCASBrparenOSCASB→ τ 2 , and

$$n ^ { ( 1 / d ) - 1 / 2 } ( H ( \mathcal { X } _ { n } ^ { r } ) - \mathbb { E } H ( \mathcal { X } _ { n } ^ { r } ) ) \stackrel { \mathcal { G } } { \longrightarrow } \mathcal { W } ( 0 , \tau ^ { 2 } ) .$$

Proof. We verify the conditions of Theorem 2.1 and Corollary 2.1. Notice first that H is homogeneous of order 1. Also, H is polynomially bounded since SIG lparenOSCASB Xscript rparenOSCASB is a subgraph of the complete graph on Xscript . Moreover, strong stabilization follows exactly as in the proof of Lemma 7.1.

If Bscript is regular, then H satisfies the uniform bounded moments condition on Bscript . The proof of this is virtually identical to that of Lemma 7.2, except that the degree D lparenOSCASB 0 rparenOSCASB in that argument should be replaced by the total length of edges incident to the origin, and similarly for the degrees Di and D lparenOSCASB x rparenOSCASB appearing later on in that proof. A factor of vertSHT Vi vertSHT needs to be introduced into the definition of the variable Wi , and consequently a factor of vertSHT u vertSHT 4 comes into the integral in (7.5), but this does not invalidate the subsequent argument.


<!-- p:29 -->


Finally, by using the same arguments as in Section 7.1 and noting that the event E 0 produces an increase of at least 1 in the total edge length of the SIG when the origin is added, while E 1 produces a reduction in the total edge length when the origin is added, we see that the distribution of Delta1 lparenOSCASB∞rparenOSCASB is nondegenerate. ✷

7 . 3 . Number of vertices of fixed degree. Let Hk lparenOSCASB Xscript rparenOSCASB denote the number of vertices of fixed degree k in SIG lparenOSCASB Xscript rparenOSCASB . We may modify the above methods to see that the number of vertices of a fixed degree is asymptotically normal. If d = 1, then all vertices have degree 1 commaori 2 or 3, a.s. If d ≥ 2 then all degrees are possible.

We assert that for each k ∈ Nopen (for d ≥ 2) and for k ∈ lbraceOSCASB 1 commaori 2 commaori 3 rbraceOSCASB (for d = 1), the distribution of Delta1 lparenOSCASB∞rparenOSCASB is nondegenerate. For simplicity we just consider d = 2. All arguments below may be easily extended to the case of general d ≥ 2. We leave the case d = 1 to the reader.

The arguments are similar for higher values of k . For example if k is even, then consider a variation of the above, where now we place k points x 1 commaori periodori periodori periodori commaorixk on vertSHT x vertSHT = 1 in such a way that there are k/ 2 pairs such that points within each pair are within ε of each other but at least 100 ε away from other points. Then consider balls Bε/ 10 lparenOSCASB xi rparenOSCASB commaori 1 ≤ i ≤ kcommaori and let E 0 be the intersection of E 2 and the event that there is exactly one point from the Poisson process in each ball. Let E 1 be the intersection of E 2 and the event that there is exactly one point from the Poisson process in each ball and one point in Bε/ 10 lparenOSCASB 0 rparenOSCASB . Then on E 0 commaoriHk increases by 1 if the origin is added whereas on E 1 commaoriHk decreases by 1 if the origin is added. When k is odd, then modify the above in the following way. Put all points xi commaori 1 ≤ i ≤ k - 1, on one hemisphere and put the point xk at the pole of the other hemisphere. Consider the analogues of E 0 and E 1 colonori E 0 is the intersection of E 2 and the event that there is one point in each ball Bε/ 10 lparenOSCASB xi rparenOSCASB commaori 1 ≤ i ≤ k and no point in the ball Bε/ 10 lparenOSCASB 0 rparenOSCASB whereas E 1 is the intersection of E 2 and the event that there is one point in each ball Bε/ 10 lparenOSCASB xi rparenOSCASB commaori 1 ≤ i ≤ k and one point in the ball Bε/ 10 lparenOSCASB 0 rparenOSCASB . Then inserting the origin on E 0 means that Hk increases by 1 (no vertices had degree k prior to the insertion of the origin), whereas inserting the origin on E 1 means that Hk

For k = 1 commaori 2 commaori we may argue as follows. Let E 2 be the event of the proof of Lemma 6.3. Choose points x 1 commaorix 2 on the unit circle vertSHT x vertSHT = 1 such that vertSHT x 1 - x 2 vertSHT = 1 / 2 periodori Let E 0 be the intersection of E 2 and the event that there is exactly one point in each of the balls B 1 / 100 lparenOSCASB xi rparenOSCASB commaori 1 ≤ i ≤ 2, and no other point inside Qd + 1 lparenOSCASB 0 rparenOSCASB . Notice that on E 0 the SIG does not put edges across the moat. Let E 1 be the intersection of E 2 and the event that there is exactly one point in each of the three balls B 1 / 100 lparenOSCASB xi rparenOSCASB commaori 1 ≤ i ≤ 2 and B 1 / 100 lparenOSCASB 0 rparenOSCASB and no other point inside Qd + 1 lparenOSCASB 0 rparenOSCASB . Notice that on E 0 the SIG does not put edges across the moat. When E 0 happens, notice that H 1 decreases by 2, and H 2 increases by 3. However, when E 1 happens, H 1 increases by 4 and H 2 decreases by 3. Since E 0 and E 1 each have positive probability, we see that Delta1 lparenOSCASB∞rparenOSCASB is nondegenerate for k = 1 commaori 2.


<!-- p:30 -->


decreases by 1 (since now no points have degree k ). So Delta1 lparenOSCASB∞rparenOSCASB is nondegenerate for all values of k .

7 . 4 . Uniqueness of the infinite component. To show strong stabilization for the number of components of the sphere of influence graph, we need a result on uniqueness of the infinite component, analogous to Lemma 6.4 in the case of the k -nearest neighbors graph.

Theorem 7.3. SIG lparenOSCASB Pscript rparenOSCASB has a.s. at most one infinite component.

For d = 1, a simple renewals argument shows that there is no infinite component. So we need only a proof for d ≥ 2. This runs mostly along the lines of the proof of Theorem 4.1 of [7]. The first step is analogous to Lemma 4.2 of [7].

Lemma 7.4. Let r &gt; 0 and let E lparenOSCASB r rparenOSCASB be the event that Br lparenOSCASB 0 rparenOSCASB is intersected by an infinite component C of SIG lparenOSCASB Pscript rparenOSCASB , such that if all edges intersecting Br lparenOSCASB 0 rparenOSCASB are removed from this component, three of the resulting components formed from C are infinite. Then P lbrackOSCASB E lparenOSCASB r rparenOSCASBrbrackOSCASB = 0 .

This can be proved by the same sort of standard argument used in the proof of Lemma 4.2 of [7]; see, for example, [16], page 67. Therefore we omit the argument here.

Lemma 7.5. SIG lparenOSCASB Pscript rparenOSCASB has a.s. at most two infinite components.

Proof. This lemma is analogous to Lemma 4.3 of [7]. Define the point process Pscript ′ 2 r as follows. Take Pscript ′ to be an independent copy of Pscript , and let Pscript ′ 2 r be the union of the point process lparenOSCASB Pscript ′ ∪ Pscript rparenOSCASB∩ B 2 r lparenOSCASB 0 rparenOSCASB , thinned by selecting each point randomly with probability 1 / 2, and the point process Pscript \ B 2 r lparenOSCASB 0 rparenOSCASB . Then Pscript ′ 2 r is a homogeneous Poisson process on Ropen d of unit intensity. A similarly constructed point process, there denoted X ′ 3 r , is used in [16].

Define the event

E ∗ lparenOSCASB r rparenOSCASB = lbraceOSCASB three infinite components of SIG lparenOSCASB Pscript rparenOSCASB intersect Br lparenOSCASB 0 rparenOSCASBrbraceOSCASB periodori

As in [7], the aim is to prove P lbrackOSCASB E ∗ lparenOSCASB r rparenOSCASBrbrackOSCASB = 0 by showing that given E ∗ lparenOSCASB r rparenOSCASB occurs, the conditional probability that the event E lparenOSCASB r rparenOSCASB occurs for Pscript ′ 2 r is nonzero, and then to appeal to Lemma 7.4.

Suppose E ∗ lparenOSCASB r rparenOSCASB occurs. Then there are three infinite components of SIG lparenOSCASB Pscript rparenOSCASB which intersect Br lparenOSCASB 0 rparenOSCASB ; call them C 1 commaoriC 2 commaoriC 3 . In proving Lemma 4.3 of [7], H ̈ aggstr ̈ om and Meester adopt a strategy of removing vertices from C 1 commaoriC 2 commaoriC 3 until they become connected for the k -nearest neighbors graph, k ≥ 2. In our setting, it is not clear that such a removal strategy works. Instead we adopt a strategy of adding points in Br lparenOSCASB 0 rparenOSCASB to connect together C 1 commaoriC 2 commaoriC 3 .

For i = 1 commaori 2 commaori 3 let C ∗ i be the union of the spheres of influence of the vertices of Ci . Then by definition, C ∗ 1 commaoriC ∗ 2 commaoriC ∗ 3 are disjoint connected subsets of Ropen d , all of them entering the set Br lparenOSCASB 0 rparenOSCASB . There may be other Poisson points too in Br lparenOSCASB 0 rparenOSCASB ; unlike in [7] we do not remove these other points.


<!-- p:31 -->


Given ε &gt; 0, let the ε -grid be the set ε Zopen d = lbraceOSCASB εz colonori z ∈ Zopen d rbraceOSCASB . By a path in the ε -grid connecting C 1 and C 2 we mean a nonempty finite sequence γ = lparenOSCASB z 1 commaoriz 2 commaori periodori periodori periodori commaorizm rparenOSCASB of elements of ε Zopen d , together with endpoints z 0 commaori zm + 1 also in ε Zopen d , such that lbraceOSCASB z 1 commaori periodori periodori periodori commaorizm rbraceOSCASB ⊂ Br lparenOSCASB 0 rparenOSCASB\ ∪ 3 i = 1 C ∗ i while z 0 ∈ C 1 and zm + 1 ∈ C 2 , such that for 1 ≤ i ≤ m + 1, ε - 1 zi and ε - 1 zi - 1 are nearest neighbors in the integer lattice Zopen d , and such that, moreover, none of the points zi in the path is within a distance less than 2 ε from any of the points of Pscript . Define paths connecting C 1 and C 3 or connecting C 2 and C 3 , similarly.

Let F lparenOSCASB rcommaori εcommaoriδ rparenOSCASB be the event that (i) E ∗ lparenOSCASB r rparenOSCASB occurs; (ii) there exist two paths γcommaoriγ ′ in the ε -grid which together connect up C 1 commaoriC 2 commaoriC 3 ; (iii) the union of the balls Bδε lparenOSCASB z rparenOSCASB commaori z ∈ γ ∪ γ ′ is contained in Br lparenOSCASB 0 rparenOSCASB\ ∪ 3 i = 1 C ∗ i and (iv) the balls of radius 4 δε centered at the endpoints of the paths γcommaoriγ ′ are each entirely contained in one of the sets C ∗ i .

Given that E ∗ lparenOSCASB r rparenOSCASB occurs, if ε is sufficiently small there will be two paths γcommaoriγ ′ , in the ε -grid, not necessarily disjoint, which together connect up C 1 , C 2 , C 3 . We now show that γcommaoriγ ′ each induce a path in SIG lparenOSCASB Pscript ′ 2 r rparenOSCASB which together connect up the clusters C 1 commaoriC 2 commaoriC 3 .

If P lbrackOSCASB E ∗ lparenOSCASB r rparenOSCASBrbrackOSCASB &gt; 0, there exists ε &gt; 0 and δ ∈ lparenOSCASB 0 commaori 1 / 6 rparenOSCASB such that P lbrackOSCASB F lparenOSCASB rcommaori εcommaori δ rparenOSCASBrbrackOSCASB &gt; 0. Choose such an ε and δ . If F lparenOSCASB rcommaori εcommaoriδ rparenOSCASB occurs, then there is a positive probability that (i) no points of lparenOSCASB Pscript ∪ Pscript ′ rparenOSCASB∩ Br lparenOSCASB 0 rparenOSCASB are discarded in the thinning process, (ii) a single point of Pscript ′ is placed in each of the balls Bδε lparenOSCASB z rparenOSCASB for each z ∈ γ ∪ γ ′ and (iii) no points are placed anywhere else by Pscript ′ . If this happens, then the added points have no effect on previous spheres of influence in C ∗ 1 commaoriC ∗ 2 commaoriC ∗ 3 , since they lie outside the old spheres of influence. On the other hand, given neighboring points zcommaoriz ′ in one of the paths, for any added points YcommaoriY ′ in Bδε lparenOSCASB z rparenOSCASB or Bδε lparenOSCASB z ′ rparenOSCASB , the sphere of influence of Y has radius at least ε lparenOSCASB 1 - 2 δ rparenOSCASB , and likewise for Y ′ , while vertSHT Y - Y ′ vertSHT ≤ ε lparenOSCASB 1 + 2 δ rparenOSCASB ; therefore the spheres of influence of Y and Y ′ overlap, and thus the paths γ and γ ′ each induce a corresponding path in SIG lparenOSCASB Pscript ′ 2 r rparenOSCASB . Finally, if z is in a path and w is an endpoint of the path adjacent to z , and if Y ∈ Bδε lparenOSCASB Z rparenOSCASB , then vertSHT Y - w vertSHT ≤ ε lparenOSCASB 1 + δ rparenOSCASB so the sphere of influence of Y goes within a distance 3 εδ of w , and therefore overlaps the cluster C ∗ i containing w . Thus the paths in SIG lparenOSCASB Pscript ′ 2 r rparenOSCASB , created by the added points, actually connect up the clusters C 1 commaoriC 2 commaoriC 3 as desired. Hence, if P lbrackOSCASB E ∗ lparenOSCASB r rparenOSCASBrbrackOSCASB &gt; 0, then P lbrackOSCASB E ′ lparenOSCASB r rparenOSCASBrbrackOSCASB &gt; 0, where E ′ lparenOSCASB r rparenOSCASB denotes the event that E lparenOSCASB r rparenOSCASB occurs for the point process Pscript ′ 2 r . This contradicts Lemma 7.4, so we must have P lbrackOSCASB E ∗ lparenOSCASB r rparenOSCASBrbrackOSCASB = 0. ✷

The proof of Theorem 7.3 is completed by similar results to Lemmas 4.4 and 4.5 of [7], except that where [7] uses a technique of removal of vertices, we use a method of adding vertices as in the proof of the preceding lemma, in such a way as to create paths connecting these spheres of influence. Since we always make sure we add vertices lying outside the spheres of influence of existing infinite components, the added vertices do not affect these existing infinite components, except to connect them together.


<!-- p:32 -->


- 7 . 5 . Number of components. In this section, we let H lparenOSCASB Xscript rparenOSCASB denote the number of components in SIG lparenOSCASB Xscript rparenOSCASB .

Theorem 7.4 (CLT for the number of components of the SIG). Suppose Bscript is regular. There exists σ 2 &gt; 0 such that as n →∞ commaorin - 1 Var lparenOSCASB H lparenOSCASB Pscript n rparenOSCASBrparenOSCASB→ σ 2 and

$$n ^ { - 1 / 2 } ( H ( \mathcal { P } _ { n } ) - \mathbb { E } H ( \mathcal { P } _ { n } ) ) \stackrel { \mathcal { I } } { \longrightarrow } \mathcal { W } ( 0 , \sigma ^ { 2 } ) .$$

Additionally, there exists τ 2 ∈ lparenOSCASB 0 commaoriσ 2 rbrackOSCASB such that as n →∞ , n - 1 Var lparenOSCASB H lparenOSCASB Uscript ncommaorin rparenOSCASBrparenOSCASB→ τ 2 , and

$$n ^ { - 1 / 2 } ( H ( \mathcal { U } _ { n , n } ) - \mathbb { E } H ( \mathcal { U } _ { n , n } ) ) \stackrel { \mathcal { I } } { \longrightarrow } \mathcal { V } ( 0 , \tau ^ { 2 } ) .$$

$$\ F i n a l l y , i f \, \mathcal { B } _ { 0 } \, \text {is regular there} \ n ^ { - 1 } \, \text {Var} ( H ( \mathcal { X } _ { n } ^ { \prime } ) ) \to \tau ^ { 2 } , \, a n d$$

$$n ^ { - 1 / 2 } ( H ( \mathcal { X } _ { n } ) - \mathbb { E } H ( \mathcal { X } _ { n } ) ) \stackrel { \mathcal { I } } { \longrightarrow } \mathcal { W } ( 0 , \tau ^ { 2 } ) .$$

Proof. It is clear that H lparenOSCASB Xscript rparenOSCASB ≤ card lparenOSCASB Xscript rparenOSCASB , so H is polynomially bounded. Also, H is homogeneous of order 0.

Let us prove the uniform bounded moments condition. Given a finite set Xscript , let M + lparenOSCASB Xscript rparenOSCASB , respectively M - lparenOSCASB Xscript rparenOSCASB , be the number of edges added to the SIG, respectively removed from the SIG, when lbraceOSCASB 0 rbraceOSCASB is added to the set Xscript . Since adding or removing an edge to a graph changes the number of components by at most 1,

$$| \Delta ( \mathcal { X } ) | \leq M ^ { + } ( \mathcal { X } ) + M ^ { - } ( \mathcal { X } ) + 1 .$$

By the proof of Lemma 7.2, both M + lparenOSCASB Uscript mcommaoriA rparenOSCASB and M - lparenOSCASB Uscript mcommaoriA rparenOSCASB have fourth moments bounded uniformly in A ∈ Bscript and in m ∈ lbrackOSCASBvertSHT A vertSHT / 2 commaori 3 vertSHT A vertSHT / 2 rbrackOSCASB . Thus by (7.12) we obtain the uniform bounded moments property.

The proof of strong stabilization proceeds in the same way as in the case of the number of components of the k -nearest neighbors graph (Proposition 6.1), this time using Theorem 7.3. Since the argument is almost the same as for Proposition 6.1, we omit it.

Together, the above remarks show that H satisfies the conditions for Theorem 2.1 and Corollary 2.1, so the result is proved. ✷

8. The Voronoi graph. In this section we assume throughout that d = 2 commaoriλ = 1, the sets Bn are all boxes and that B 0 = Q 1 / 2 lparenOSCASB 0 rparenOSCASB . We let Vor lparenOSCASB Xscript rparenOSCASB denote the Voronoi graph on a point set Xscript ⊂ Ropen 2 . We show that the total edge length of the Voronoi tessellation satisfies the central limit behavior of Theorem 2.1.
2. 8 . 1 . Total edge length. In this section, we let H lparenOSCASB Xscript rparenOSCASB denote the total edge length of all of the fi nite edges in Vor lparenOSCASB Xscript rparenOSCASB . The following CLT extends the results of [1] and [8] which restrict attention to Voronoi tessellations over Poisson samples. We also establish the convergence of the variance of H .


<!-- p:33 -->


Theorem 8.1 (CLT for the total edge length in the Voronoi graph). Suppose the sets Bn are all boxes. There exists σ 2 &gt; 0 such that as n → ∞ , n - 1 Var lparenOSCASB H lparenOSCASB Pscript n rparenOSCASBrparenOSCASB→ σ 2 and

Additionally, there exists τ 2 ∈ lparenOSCASB 0 commaoriσ 2 rbrackOSCASB such that as n →∞ , n - 1 Var lparenOSCASB H lparenOSCASB Uscript ncommaorin rparenOSCASBrparenOSCASB→ τ 2 and

$$n ^ { - 1 / 2 } ( H ( \mathcal { P } _ { n } ) - \mathbb { E } H ( \mathcal { P } _ { n } ) ) \stackrel { \mathcal { I } } { \longrightarrow } & \mathcal { W } ( 0 , \sigma ^ { 2 } ) . \\ \\ \intertext { s o n t r } 1 0 \cdot \sigma \colon \quad w i t h \quad & = \colon \dot { \sigma } \colon \quad 2 \cdot \sigma \colon \quad 2 ( \sigma ) = 1 w \quad ( 0 , \sigma ^ { 2 } ) .$$

$$n ^ { - 1 / 2 } ( H ( \mathcal { U } _ { n , n } ) - \mathbb { E } H ( \mathcal { U } _ { n , n } ) ) \stackrel { \mathcal { D } } { \longrightarrow } \mathcal { N } ( 0 , \tau ^ { 2 } ) . \\ \\$$

$$A l s o , i f \, B _ { 0 } = Q _ { 1 / 2 } ( 0 ) , n ^ { ( 2 / d ) - 1 } \, \text {Var} ( H ( \mathcal { L } _ { n } ^ { \prime } ) ) \to \tau ^ { 2 } \ a n d$$

$$n ^ { ( 1 / d ) - 1 / 2 } ( H ( \mathcal { X } _ { n } ^ { \cdot } ) - \mathbb { E } H ( \mathcal { X } _ { n } ^ { \cdot } ) ) \stackrel { \mathcal { I } } { \longrightarrow } \mathcal { W } ( 0 , \tau ^ { 2 } ) .$$

We prove Theorem 8.1 by showing that H satisfies the conditions of Theorem 2.1. Note that by Euler's formula, for any finite Xscript we have H lparenOSCASB Xscript rparenOSCASB ≤ 3diam lparenOSCASB Xscript rparenOSCASB card lparenOSCASB Xscript rparenOSCASB and thus the functional H is polynomially bounded. Also, H is clearly homogeneous of order 1.

It is easy to see that H is strongly stabilizing. We follow [14] closely and use a construction similar to that used for the k -nearest neighbors graph. Instead of constructing six equilateral triangles, we now construct twelve disjoint congruent isosceles triangles Tj lparenOSCASB t rparenOSCASB commaori 1 ≤ j ≤ 12, where the origin is a vertex of each triangle, where each triangle has two edges of length t , where Tj lparenOSCASB t rparenOSCASB ⊂ Tj lparenOSCASB u rparenOSCASB whenever t &lt; u , and where ∪ t&gt; 0 ∪ 12 j = 1 Tj lparenOSCASB t rparenOSCASB = Ropen 2 . Let S denote the minimum t such that each triangle Tj lparenOSCASB t rparenOSCASB commaori 1 ≤ j ≤ 12, contains at least one point from the Poisson point process.

Then the insertion of the origin into the Poisson point process does not affect the structure of the Voronoi diagram at distances farther than 3 S from the origin (see Section 4 of [14]). (The same is true for the Delaunay, relative neighbor and Gabriel graphs, which are defined in the next section.) As in Lemma 6.1, it is easy to see that the random variable S is a.s. finite, so H is strongly stabilizing.

Lemma 8.1. H satisfies the uniform bounded moments condition.

Proof. We will make heavy use of the estimates in [14]. From inequalities (4.7) and (4.9) of [14] we know that

$$| \Delta H ( \mathcal { X } ) | & \leq E ( 0 , \mathcal { X } ) + F ( 0 , \mathcal { X } ) , \\ | \Delta H ( \mathcal { X } ) | & \leq E ( 0 , \mathcal { X } ) + F ( 0 , \mathcal { X } ) , \\$$

$$\max ( \mathbb { E } [ E ( 0 , \mathcal { W } _ { m , \, B } ) ^ { 4 } ] , \mathbb { E } [ F ( 0 , \mathcal { W } _ { m , \, B } ) ^ { 4 } ] ) \leq c .$$

where E lparenOSCASB 0 commaori Xscript rparenOSCASB denotes the combined lengths of the bounded edges of the cell consisting of points closer to 0 than to any point of Xscript , and where F lparenOSCASB 0 commaori Xscript rparenOSCASB denotes the combined lengths of the intersections of the bounded edges in Vor lparenOSCASB Xscript rparenOSCASB with the interior of the Voronoi cell around 0 in Vor lparenOSCASBlbraceOSCASB 0 rbraceOSCASB ∪ Xscript rparenOSCASB . Thus it is enough to show that there exists a constant c such that for all boxes B and m ∈ lbrackOSCASBvertSHT B vertSHT / 2 commaori 3 vertSHT B vertSHT / 2 rbrackOSCASB , If we follow the arguments of [14] then we see that we need only show


<!-- p:34 -->


$$\mathbb { E } [ D ( 0 , \mathcal { W } _ { m , \, B } ) ^ { 4 } K ( 0 , \mathcal { W } _ { m , \, B } ) ^ { 4 } ] & \leq c , \\ \\ \mathbb { E } [ D ( 0 , \mathcal { O } _ { m , \, B } ) - 1 ] & \leq c ,$$

$$P [ S _ { j } > t ] & \leq ( 1 - c t / | B | ) ^ { m } \leq \exp ( - c t / 2 ) , \\ \intertext { t } P [ S _ { j } > t ] & \leq ( 1 - c t / | B | ) ^ { m } \leq \exp ( - c t / 2 ) ,$$

where D colonori= D lparenOSCASB 0 commaori Uscript mcommaoriB rparenOSCASB denotes the diameter of the intersection of B with the Voronoi cell around 0 in the Voronoi diagram on lbraceOSCASB 0 rbraceOSCASB ∪ Uscript mcommaoriB , and where K colonori= K lparenOSCASB 0 commaori Uscript mcommaoriB rparenOSCASB denotes the number of sides of the Voronoi cell around 0 in the Voronoi diagram on lbraceOSCASB 0 rbraceOSCASB ∪ Uscript mcommaoriB . For each t &gt; 0, construct twelve disjoint congruent isosceles triangles Tj lparenOSCASB t rparenOSCASB commaori 1 ≤ j ≤ 12, having union Ropen 2 , where the point 0 is a vertex of each triangle, where each triangle has two edges of length t and where Tj lparenOSCASB t rparenOSCASB ⊂ Tj lparenOSCASB u rparenOSCASB whenever 0 &lt; t &lt; u . For all 1 ≤ j ≤ 12, let Sj be the minimum t such that the triangle Tj lparenOSCASB t rparenOSCASB contains at least one point from Uscript mcommaoriB , if such a t exists, or to be the diameter of Tj lparenOSCASB t rparenOSCASB ∩ B , if not. Let S = max lparenOSCASB S 1 commaori periodori periodori periodori commaoriS 12 rparenOSCASB . As in [14], simple geometric considerations show that for all boxes B including those with 0 near the boundary of B , we have D ≤ 2 S . Note that there is a constant c such that for all B and m of interest,

and therefore the tail of the distribution of S decays exponentially, uniformly in B and m . Then using the arguments of Section 4 of [14], we can obtain (8.4). ✷

Lemma 8.2. The distribution of Delta1 lparenOSCASB∞rparenOSCASB is nondegenerate.

Proof. Consider the construction used in the proof of Lemma 6.3. Let E 2 be the event that there are no points of Pscript in the moat and there is at least one point in each of the subcubes in Ascript . Fix ε small ( &lt; 1 / 100). Choose points x 1 commaorix 2 commaorix 3 ∈ Ropen 2 forming an equilateral triangle of side length 1 / 2, centered at the origin. Consider the balls of radius ε centered at the points x 1 commaorix 2 commaorix 3 . Let A 0 be the intersection of E 2 and the event that there is exactly one point in each of the three balls and no other point in the central 'island' C 0 . Let A 1 be the intersection of E 2 and the event that there is exactly one point in each of the balls of radius εδ centered at the points δx 1 commaoriδx 2 commaoriδx 3 , where δ ∈ lparenOSCASB 0 commaori 1 rparenOSCASB will be chosen shortly, and no other point in the central island.

On the event A 0 , the insertion of the origin leads to three new edges, namely the edges of a (nearly equilateral) triangular cell T around the origin. It removes the parts of the three edges of the original Voronoi graph which intersect T . The difference between the sum of the lengths of the added edges and the sum of the lengths of the three removed edges exceeds some fixed positive number α [the reason is this: given an equilateral triangle T , and a point P inside it, the sum of the lengths of the three edges joining P to the vertices of T is strictly less than the perimeter of T since the length of each of the three edges is less than the common length of the side of T . If T is nearly equilateral (our case) this is still true].

On the other hand, on the event A 1 , the insertion of the origin cannot increase the total edge length by more than the total edge length of triangular cell around the origin, and this increase is bounded by a constant multiple of δ , which is less than α if δ is small enough. Thus if δ is small enough, the events A 0 and A 1 give rise to values of Delta1 lparenOSCASB∞rparenOSCASB which differ by at least some fixed amount. This shows the nondegeneracy of Delta1 lparenOSCASB∞rparenOSCASB . ✷


<!-- p:35 -->


Thus H satisfies all of the conditions of Theorem 2.1 and thus Theorem 8.1 is proved.

8 . 2 . Total number of edges and vertices. The above discussion also applies in part to other functionals of the Voronoi tessellation. For example, if H lparenOSCASB Xscript rparenOSCASB counts the number of edges in Vor lparenOSCASB Xscript rparenOSCASB , then it can be checked that H is strongly stabilizing, satisfies the uniform moment condition, is homogeneous of order 0 and therefore satisfies the conclusions of Corollary 2.1 with γ = 0. However, this is one instance where the limiting variance τ 2 is zero, and therefore the 'correct' scaling of the variance is not by n - 1 , so that our results are not so relevant in this case.

The reason for this degeneracy is as follows. All vertices of Vor lparenOSCASB Xscript n rparenOSCASB a.s. have degree 3 (see [21], Theorem 5.7). Therefore, if Vn denotes the number of vertices, En the number of edges and In the number of infinite edges, we have 3 Vn = 2 En - In . On the other hand, by Euler's formula, since the number of faces is n , we have Vn - En + n = 1 (it is not the usual Euler's formula because we are not counting the 'vertex at infinity'). Combining these two simultaneous equations, we obtain En = 3 n - 3 - Inperiodori Therefore Var lparenOSCASB En rparenOSCASB = Var lparenOSCASB In rparenOSCASB .

It would be interesting to know if there is a way of adapting our method to get nondegenerate CLTs for quantities such as the number of vertices in the convex hull, whose variances do not grow in proportion to n . See [1] for an adaptation of a method to the convex hull problem.

The value of In is equal to the number of points of Xscript n lying on the boundary of the convex hull of Xscript n , and therefore its variance is asymptotic to a constant times log n [6]. This shows that τ 2 = 0. Moreover, a similar discussion applies when H is the number of vertices of the Voronoi graph.

9. Other proximity graphs. The discussion in the preceding sections applies to other graphs in computational geometry and, at a minimum, covers the case when the sets Bn are all boxes and B 0 = Q 1 / 2 lparenOSCASB 0 rparenOSCASB . In the examples which follow, we see that functionals of such graphs (such as total edge length and total number of edges) satisfy strong stabilization, the uniform bounded moments condition and the nondegeneracy of Delta1 lparenOSCASB∞rparenOSCASB . Moreover, the proofs of these facts are nearly exact replicas of the proofs above and we leave the details to the reader. We now describe some of the graphs covered by the above discussion. See [3, 22] for more details on these and related proximity graphs.

Delaunay triangulation. The Delaunay triangulation of a point set Xscript ⊂ Ropen d is the graph which is dual to the Voronoi tessellation; it puts an edge between two points of Xscript if and only if these points are centers of adjacent Voronoi cells. The total edge length of the Delaunay triangulation satisfies a CLT analogous to Theorem 8.1. The Delaunay triangulation on n points has at most n lparenOSCASB n - 1 rparenOSCASB / 2


<!-- p:36 -->


edges and so the total edge length is polynomially bounded. The radius of stabilization for the total edge length of the Delaunay triangulation is the same as that for the Voronoi tessellation. By modifying Lemma 6.2 in a straightforward fashion, one can show that the total edge length of the Delaunay triangulation satisfies the fourth moment condition and in this way avoid the complications present in Lemma 8.1. When d = 2, the number of edges of the Delaunay triangulation is the same as the number of edges of the Voronoi tessellation, so the discussion in Section 8.2 applies. Gabriel graph. The Gabriel graph on a point set Xscript puts an edge between two points xcommaoriy of Xscript if the ball centered at lparenOSCASB x + y rparenOSCASB / 2 with x and y at opposite poles does not contain any other points in Xscript . The Gabriel graph is a subgraph of the Delaunay triangulation. Strong stabilization for the Gabriel graph can be established by an argument using cones or triangles in much the same way as for the k -nearest neighbors graph or the Voronoi graph. Fourth moments are handled as in Lemma 6.2. Relative neighborhood graph. The relative neighborhood graph on Xscript is formed by joining all pairs of points whose loon is empty, where the loon defined by a pair is the intersection of two spheres of equal radius, each having one point as center and the other point on its surface. The relative neighborhood graph is a subgraph of the Gabriel graph. Strong stabilization for the relative neighborhood graph can be established in much the same way as for the k -nearest neighbors graph or the Voronoi graph. Fourth moments are handled as in Lemma 6.2. Power weighted edges. Kesten and Lee [11] prove a central limit theorem for the total edge length of the minimal spanning tree on a random sample when the edges are power-weighted. All of the graphs described here admit versions with power weighted edges and it is trivial to show that the total edge length of such graphs satisfies all the conditions of our main theorems. Percolation. One simple way to obtain a graph on Xscript is to connect all pairs of points which are at most unit distance apart. One can obtain a (nonhomogeneous) functional H occ lparenOSCASB Xscript rparenOSCASB by counting the components of the resulting graph. This is equivalent to a basic model of continuum percolation [16], in which one takes balls of unit diameter around each point and counts the connected components of the union of the balls ( occupied clusters ). One can also consider the number H vac lparenOSCASB Xscript rparenOSCASB of vacant clusters , by which we mean components of the complement of the union of balls. Using results in [16] on uniqueness of the infinite cluster, both H occ and H vac can be shown to satisfy strong stabilization, and hence a CLT for the uniform sample Uscript ncommaorin . This adds to a result in [19] on CLTs for occupied and vacant cluster counts (in a more general setting) for Poisson samples.

Acknowledgment. MDP's work on this research started during a visit in April-June 1999 to the Fields Institute in Toronto, whose hospitality and support is much appreciated.


<!-- p:37 -->


CLTS IN COMPUTATIONAL GEOMETRY 1041
