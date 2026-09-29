---
id: "Hayashi-Nomoto-Suzuki_2026_Curvature-Corrections-Random-Geometric-Graphs"
source_pdf: "../pdf/Hayashi-Nomoto-Suzuki_2026_Curvature-Corrections-Random-Geometric-Graphs.pdf"
source_filename: "Hayashi-Nomoto-Suzuki_2026_Curvature-Corrections-Random-Geometric-Graphs.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "good"
extraction_score: 90.0
visual_assets: "disabled"
references_file: "../references/Hayashi-Nomoto-Suzuki_2026_Curvature-Corrections-Random-Geometric-Graphs.references.md"
---

<!-- p:1 -->

## Boundary-Moment Universality and Curvature Corrections in Random Geometric Graphs on Riemannian Manifolds

Taro Hayashi ∗ 1 , Subaru Nomoto † 1 , and Ryoichi Suzuki ‡ 2

1 Department of Mathematical Sciences, College of Science and Engineering, Ritsumeikan University, 1-1-1 Noji-higashi, Kusatsu, Shiga 525-8577, Japan.

2 Department of Business Economics, School of Management, Tokyo University of Science,

1-11-2 Fujimi, Chiyoda, Tokyo 102-0071, Japan.

##### Abstract

Let ( M,g ) be a smooth, closed, connected d -dimensional Riemannian manifold, and let X 1 , . . . , X n be i.i.d. with common law f d vol g , where f ∈ C 4 ( M ) is strictly positive. We derive a uniform intrinsic second-order expansion for symmetric three-vertex edgeindicator statistics supported on connected configurations, including the induced-path and triangle kernels. The second-order term separates density variation, normal-coordinate Jacobians, and the curvature-induced motion of the internal-chord boundary. Within this three-vertex connected symmetric class, a universal boundary-moment identity reduces the kernel-dependent contribution to a common intrinsic functional involving ∫ M f ∥ grad f ∥ 2 g d vol g and ∫ M f 3 Scal g d vol g . For the normalized path-triangle contrast, the Euclidean leading term cancels. We construct a consistent estimator of this intrinsic functional and, in a denser bandwidth regime, we prove an exact-expectation-centered rootn central limit theorem via the first Hoeffding projection. For uniform sampling on a closed surface, the estimator consistently recovers the Euler characteristic. We also study the threshold radius at which the maximum degree of a binomial random geometric graph first reaches two. Using the active-triple intensity expansion and a dependency-graph Poisson approximation, we obtain the ordern - 3 /d correction to the log-survival law for d &gt; 6.

Keywords. Random geometric graphs; Riemannian manifolds; scalar curvature; geometric U -statistics; degree-two maximum-degree threshold.

MSC 2020. Primary 60D05; Secondary 05C80, 53C21, 60G55, 62G20.

## 1 Introduction

Random geometric graphs encode local metric information through pairwise distance constraints [16]. At scales r ↓ 0, a neighborhood of a point on a smooth Riemannian manifold is approximately Euclidean, so the leading behavior of many local graph statistics is curvature-insensitive. We ask how intrinsic geometry first enters second-order expansions of symmetric three-vertex statistics supported on connected configurations and how those corrections propagate to the degree-two maximum-degree threshold.

∗ Corresponding author. E-mail: haya4taro@gmail.com . ORCID: 0009-0005-0145-8042

‡ E-mail: rsuzukimath@gmail.com . ORCID: 0000-0001-9979-1882

† E-mail: snomoto@fc.ritsumei.ac.jp . ORCID: 0009-0009-0701-8370


<!-- p:2 -->


Write [ n ] := { 1 , . . . , n } . Let G n ( r ) be the graph on the sample points { X 1 , . . . , X n } in which two vertices are adjacent when their geodesic distance is at most r , and let ∆( G ) denote the maximum degree of a graph G . Define

$$S _ { 2 , n } \colon = \inf \{ r > 0 \colon \Delta ( G _ { n } ( r ) ) \geq 2 \} .$$

$$r _ { 2 , n } ( t ) \colon = t n ^ { - 3 / ( 2 d ) } ,$$

because the expected number of three-point degree-two witnesses is then of order one; equivalently, n 3 r 2 ,n ( t ) 2 d = t 2 d . For d &gt; 6, Theorem 3.8 gives the ordern - 3 /d intrinsic correction to the survival law. The main new geometric input is the curvature-induced motion of the discontinuous internaledge constraint.

### 1.1 Relation to existing threshold and manifold expansions

Classical Poisson limits for short-distance U -statistics and minimum interpoint distances go back to [13,21]; general geometric order-statistic and Poisson-approximation frameworks include [8,19]. A recent preprint by Otsuka [15] proves the leading fixedk threshold law in Euclidean space and a compound-Poisson limit for the point process of degreek vertices. For k = 2, the feasible graphs are P 3 and K 3 , and Otsuka's total Euclidean intensity is

$$\mu _ { d , 2 } ^ { O } = A _ { 2 } ( d ) \int _ { \mathbb { R } ^ { d } } f ^ { 3 } \, d x .$$

Thus his leading survival law agrees exactly with the tangent-space leading term obtained below. The two Poisson descriptions concern different observables: Otsuka counts degree-two vertices, so a triangle contributes three vertices, whereas our active-triple count assigns unit weight to each P 3 or K 3 cluster. Our contribution is the next-order curvature correction on a closed Riemannian manifold.

First-order tangent-space limit theory for stabilizing point-process functionals on manifolds was developed by Penrose and Yukich [17]; related manifold models include [2,4,14]. Subgraph counts and their Poisson and normal limits in Euclidean random geometric graphs are classical [16, Chapter 3]. For our shrinking-radius kernels, we use the exact Hoeffding decomposition [20, Chapter 5] and verify projection dominance directly from geometric overlap bounds.

There is also a distinct literature on recovering continuum curvature from finite metric or graph data. Hickok and Blumberg [12] estimate scalar curvature from metric-ball volumes, while [9,22] study consistency of Ollivier-Ricci curvature on random geometric graphs or data clouds. Our target is instead the integrated density-curvature functional G 3 ( f ; g ) obtained from two global motif counts; under uniform sampling on a closed surface, Gauss-Bonnet converts it into the Euler characteristic. Scalar-curvature corrections for small geodesic balls are classical [10], and related corrections occur in Riemannian Poisson-Voronoi geometry [5]. The new technical issue here is the curvature-induced motion of a discontinuous internal-distance boundary.

### 1.2 Contributions and scope

The main geometric result, Theorem 3.2, is a second-order expectation expansion for any symmetric function of the three edge indicators that vanishes on graphs with at most one edge. This class is precisely the two-dimensional span of the induced-path and triangle kernels. The proof yields a stronger uniform anchored expansion, which is also used in the threshold analysis.

The central structural result is Proposition 3.1: the Jacobian and moving-boundary coefficients are linked, and every admissible weight h in this three-vertex class satisfies

$$\mathcal { B } _ { \mathfrak { h } } ( d ) = \frac { d - 1 } { 2 } M _ { \mathfrak { h } } ( d ) .$$

The natural sparse scale is We prove this boundary-moment identity by a distributional divergence argument in the displacement variable.


<!-- p:3 -->


Here and throughout, grad h denotes the Riemannian gradient of a smooth function h . Define

$$\mathcal { G } _ { 3 } ( f ; g ) \coloneqq \int _ { M } f \| \text { grad } f \| _ { g } ^ { 2 } \, d \text {vol} _ { g } + \frac { 1 } { 6 } \int _ { M } f ^ { 3 } \, \text {Scalar} _ { g } \, d \text {vol} _ { g } .$$

Theorem 3.2 gives, for every admissible kernel,

$$\mathbb { E } U _ { \mathfrak { h } } ( r ) = \left ( \begin{matrix} n \\ 3 \end{matrix} \right ) r ^ { 2 d } \left [ J _ { \mathfrak { h } } ( d ) \int _ { M } f ^ { 3 } \, d v \text {ol} _ { g } - \frac { 3 M _ { \mathfrak { h } } ( d ) } { 2 d } r ^ { 2 } \mathcal { G } _ { 3 } ( f ; g ) + o ( r ^ { 2 } ) \right ] .$$

The scalar-curvature coefficient combines the normal-coordinate Jacobian contribution - M h / (3 d ) with the moving-boundary contribution + M h / (12 d ). The latter is a one-sided shape derivative of a discontinuous graph-induced kernel and is invisible in the Euclidean tangent law.

For the active-triple kernel, J h 2 ( d ) / 6 = A 2 ( d ) and M h 2 ( d ) / (4 d ) = C 2 ( d ). The normalized induced-path minus triangle contrast cancels the orderr 2 d Euclidean term and yields an estimator of G 3 ( f ; g ). Theorem 3.4 gives variance bounds and consistency, while Theorem 3.5 gives, in a denser bandwidth regime, a rootn central limit theorem centered at the exact expectation. Without a quantitative higher-order bias expansion, we do not claim a target-centered central limit theorem. Under uniform sampling on a closed surface, Corollary 3.7 gives consistent recovery of the Euler characteristic.

For the degree-two threshold, Theorem 3.8 gives the ordern - 3 /d intrinsic correction to the log-survival law for d &gt; 6. Its proof represents the survival event as a zero-count event for active triples and uses a dependency-graph Chen-Stein bound to transfer the expectation expansion to the zero-count law. The restriction d &gt; 6 ensures that the probabilistic approximation error is smaller than the geometric r 2 correction. We do not treat manifolds with boundary or the critical dimension d = 6, and we do not claim a general theorem for higher-degree thresholds.

To the best of our knowledge, the one-sided moving-boundary coefficient, the boundarymoment identity, and the zero-mass path-triangle estimator of G 3 ( f ; g ) have not previously been derived.

Section 2 introduces the setting and Section 3 states the main results. Sections 4-6 develop the geometric, threshold, and statistical arguments. The appendices contain auxiliary computations and trace details.

## 2 Setting and notation

Throughout, ( M,g ) is a smooth, closed, connected d -dimensional Riemannian manifold. Let d g be the geodesic distance and d vol g the Riemannian volume measure, and write

$$V o l _ { g } ( M ) \colon = \int _ { M } d v o l _ { g } .$$

$$X _ { 1 } , \dots , X _ { n } \stackrel { i . i . d . } { \sim } f \, d v o l _ { g } , \quad f \in C ^ { 4 } ( M ) , \ \ f > 0 , \ \ \int _ { M } f \, d v o l _ { g } = 1 .$$

Let

For a smooth function φ on M , our Laplacian convention is

$$\Delta _ { g } \varphi = \text {div} _ { g } ( \text {grad} \varphi ) .$$

Since M is closed, integration by parts gives

$$\int _ { M } f \Delta _ { g } f \, d v o l _ { g } = - \int _ { M } \| \text {grad} \, f \| _ { g } ^ { 2 } \, d v o l _ { g } .$$


<!-- p:4 -->


Let ∇ be the Levi-Civita connection with respect to g . Our curvature convention is

$$R ( u , v ) w \coloneqq \nabla _ { u } \nabla _ { v } w - \nabla _ { v } \nabla _ { u } w - \nabla _ { [ u , v ] } w , \quad R _ { x } ( u , v , w , z ) \coloneqq \langle R _ { x } ( u , v ) z , w \rangle _ { g } .$$

Thus R x ( u, v, u, v ) = ⟨ R x ( u, v ) v, u ⟩ g , and the unit sphere has sectional curvature +1.

Let ω d be the Euclidean volume of the unit ball in R d , and let dσ denote the standard unnormalized surface measure on S d - 1 , so that σ ( S d - 1 ) = dω d . Let

$$\iota \colon = \text {in} ( M , g ) > 0 .$$

Compactness also gives a uniform strong-convexity radius ρ c &gt; 0: every ball B g ( x, ρ c ) is strongly geodesically convex. Put

$$r _ { * } \colon = \min \{ \iota / 1 0 , \rho _ { c } / 4 \} .$$

For a compact set K ⊂ R d × R d , define

$$R _ { K } \colon = \sup _ { ( z , w ) \in K } \max \{ | z | , | z - w | \} , \quad r _ { K } \colon = \min \left \{ r _ { * } , \frac { \iota } { 2 ( 1 + R _ { K } ) } , \frac { \rho _ { c } } { 2 ( 1 + R _ { K } ) } \right \} .$$

For a compactly supported cutoff χ , we write R χ and r χ for the same quantities with K = supp χ . Every local statement below uses the corresponding support-dependent radius. For x ∈ M , let

$$\mathcal { F } _ { x } \colon = \{ \tau \, \colon \mathbb { R } ^ { d } \to T _ { x } M \, \colon \tau \, \text { is an orthogonal isometric} \} , \quad \mathcal { F } ( M ) \, \colon = \{ ( x , \tau ) \, \colon x \in M , \, \tau \in \mathcal { F } _ { x } \} .$$

The orthonormal frame bundle F ( M ) is compact. We use the notation

$$\exp _ { x , \tau } ( z ) \colon = \exp _ { x } ( \tau z ) , \quad R _ { x , \tau } ( u , v , w , z ) \colon = R _ { x } ( \tau u , \tau v , \tau w , \tau z ) .$$

All estimates on fixed Euclidean compact sets are uniform in ( x, τ ) ∈ F ( M ). The kernels used below are simultaneously O ( d )-invariant, so the resulting integrals are independent of the choice of frame.

Local tangent variables are always defined by

$$z _ { i } = r ^ { - 1 } \exp _ { x } ^ { - 1 } ( x _ { i } )$$

inside the injectivity ball of x ; thus exp - 1 x is used only locally.

We write O ( · ) and o ( · ) uniformly in the base point x ∈ M ; when a parameter t appears in the threshold scale, all asymptotics are uniform for t in compact subsets of [0 , ∞ ). Constants denoted by C may change from line to line and depend on M,g,f,d and on the fixed compact range of t , but never on n or r .

The hypotheses f ∈ C 4 ( M ) and f &gt; 0 are standing assumptions adopted to keep a single set of conditions throughout the paper; we do not optimize the regularity or positivity assumptions theorem by theorem. The C 4 condition justifies the uniform normal-coordinate expansions used below. Compactness and positivity imply that the sampling density is bounded above and below away from zero, so no tail or support-boundary localization issue arises. All zero-count probability expansions are understood on compact t -ranges, including t = 0. At t = 0 the relevant cluster count is zero almost surely, because the sampling law is nonatomic. The displayed formulas are interpreted using this endpoint convention and uniformity in t .

## 3 Main results

The proofs of the statements in this section are deferred to the subsequent sections. After each main statement, we indicate where it is established.


<!-- p:5 -->


### 3.1 Path and triangle graph functionals

Fix λ P , λ K ∈ R and define

$$\mathfrak { h } ( a , b , c ) \colon = \lambda _ { P } ( a b + a c + b c ) + ( \lambda _ { K } - 3 \lambda _ { P } ) a b c , \quad ( a , b , c ) \in \{ 0 , 1 \} ^ { 3 } .$$

Thus h assigns weight λ P to a three-vertex path P 3 , weight λ K to a triangle K 3 , and weight 0 to every disconnected three-vertex graph. In particular, h is symmetric in its three arguments and

$$\mathfrak { h } ( a , b , c ) = 0 \quad \text {whenever } a + b + c \leq 1 .$$

We refer to such a weight as an admissible symmetric weight.

Let ( [ n ] 3 ) be the family of all three-element subsets { i, j, k } ⊂ [ n ]. For α = { i, j, k } ∈ ( [ n ] 3 ) , with i &lt; j &lt; k , put

$$\xi _ { \alpha , \mathfrak { h } } ( r ) = \mathfrak { h } \left ( 1 \{ d _ { g } ( X _ { i } , X _ { j } ) \leq r \} , 1 _ { \{ d _ { g } ( X _ { i } , X _ { k } ) \leq r \} } , 1 _ { \{ d _ { g } ( X _ { j } , X _ { k } ) \leq r \} } \right ) , \quad U _ { \mathfrak { h } } ( r ) = \sum _ { \alpha \in \left ( \begin{smallmatrix} n \\ 3 \end{smallmatrix} \right ) } \xi _ { \alpha , \mathfrak { h } } ( r ) .$$

For z 1 , z 2 ∈ R d , define

$$H _ { \mathfrak { h } } ( z _ { 1 } , z _ { 2 } ) = \mathfrak { h } ( 1 _ { \{ | z _ { 1 } | \leq 1 \} } , 1 _ { \{ | z _ { 2 } | \leq 1 \} } , 1 _ { \{ | z _ { 1 } - z _ { 2 } | \leq 1 \} } ) \, , \\ \ell _ { \mathfrak { h } } ( a , b ) = \mathfrak { h } ( a , b , 1 ) - \mathfrak { h } ( a , b , 0 ) , \\ \widetilde { L } _ { \mathfrak { h } } ( z _ { 1 } , z _ { 2 } ) = \ell _ { \mathfrak { h } } ( 1 _ { \{ | z _ { 1 } | \leq 1 \} } , 1 _ { \{ | z _ { 2 } | \leq 1 \} } ) \, , \quad L _ { \mathfrak { h } } ( z , w ) \colon = \widetilde { L } _ { \mathfrak { h } } ( z , z - w ) . \\ \widetilde { L } _ { \mathfrak { h } } ( z _ { 1 } , z _ { 2 } ) = \underline { \ell } _ { \mathfrak { h } } ( 1 _ { \{ | z _ { 1 } | \leq 1 \} } , 1 _ { \{ | z _ { 2 } | \leq 1 \} } ) \, ,$$

Thus  ̃ L h takes two endpoint variables, whereas L h takes an endpoint and a displacement. The connected-support assumption makes the following moments finite:

$$J _ { \mathfrak { h } } ( d ) = \int _ { ( \mathbb { R } ^ { d } ) ^ { 2 } } H _ { \mathfrak { h } } ( z _ { 1 } , z _ { 2 } ) \, d z _ { 1 } \, d z _ { 2 } , \quad M _ { \mathfrak { h } } ( d ) = \int _ { ( \mathbb { R } ^ { d } ) ^ { 2 } } H _ { \mathfrak { h } } ( z _ { 1 } , z _ { 2 } ) | z _ { 1 } | ^ { 2 } \, d z _ { 1 } \, d z _ { 2 } .$$

By symmetry in z 1 and z 2 , equivalently,

$$M _ { \mathfrak { h } } ( d ) = \frac { 1 } { 2 } \int _ { ( \mathbb { R } ^ { d } ) ^ { 2 } } H _ { \mathfrak { h } } ( z _ { 1 } , z _ { 2 } ) \left ( | z _ { 1 } | ^ { 2 } + | z _ { 2 } | ^ { 2 } \right ) d z _ { 1 } \, d z _ { 2 } .$$

$$\mathcal { B } _ { \mathfrak { h } } ( d ) = \int _ { S ^ { d - 1 } } \int _ { \mathbb { R } ^ { d } } L _ { \mathfrak { h } } ( z , w ) \left ( | z | ^ { 2 } - ( z \cdot w ) ^ { 2 } \right ) d z \, d \sigma ( w ) .$$

Proposition 3.1. For every admissible symmetric weight h and every d ≥ 2 ,

$$\mathcal { B } _ { \mathfrak { h } } ( d ) = \frac { d - 1 } { 2 } M _ { \mathfrak { h } } ( d ) .$$

The proof is given in Section 4, following Lemma 4.8. There the identity is obtained from the BV jump formula by a distributional divergence argument in the displacement variable.

Define

$$\mathcal { G } _ { 3 } ( f ; g ) & \coloneqq \int _ { M } f \| \text { grad } f \| _ { g } ^ { 2 } \, d \text {vol} _ { g } + \frac { 1 } { 6 } \int _ { M } f ^ { 3 } \, \text {Scalar} _ { g } \, d \text {vol} _ { g } . \\$$

The next theorem records the common intrinsic functional for all admissible weights, including signed linear combinations.

Theorem 3.2. Assume d ≥ 2 and the standing hypotheses on ( M,g,f ) . For every admissible symmetric weight h and every n ≥ 3 , as r ↓ 0 ,

$$\mathbb { E } U _ { \mathfrak { h } } ( r ) = \left ( \begin{matrix} n \\ 3 \end{matrix} \right ) r ^ { 2 d } \left [ J _ { \mathfrak { h } } ( d ) \int _ { M } f ^ { 3 } \, d v \text {ol} _ { g } - \frac { 3 M _ { \mathfrak { h } } ( d ) } { 2 d } r ^ { 2 } \mathcal { G } _ { 3 } ( f ; g ) + o ( r ^ { 2 } ) \right ] .$$

The remainder in the bracket is independent of n , so the expansion also holds along arbitrary integer sequences n = n ( r ) ≥ 3 .

For d ≥ 2, The proof is given in Subsection 5.2. There we first establish the stronger uniform anchored expansion in Proposition 5.2; integrating that expansion over the anchor point yields Theorem 3.2. Remark 3.3 . Proposition 3.1 reduces all second-order kernel dependence to the two Euclidean moments J h ( d ) and M h ( d ).


<!-- p:6 -->


### 3.2 Statistical estimation from the path-triangle contrast

For the induced path and triangle, set

$$\mathfrak { h } _ { P _ { 3 } } ( a , b , c ) \colon = 1 _ { \{ a + b + c = 2 \} } , \quad \mathfrak { h } _ { K _ { 3 } } ( a , b , c ) \colon = 1 _ { \{ a + b + c = 3 \} } .$$

For G ∈ { P 3 , K 3 } , write

$$H _ { G } ( z _ { 1 } , z _ { 2 } ) \coloneqq H _ { \mathfrak { h } _ { G } } ( z _ { 1 } , z _ { 2 } ) , \quad J _ { G } ( d ) \coloneqq J _ { \mathfrak { h } _ { G } } ( d ) , \quad M _ { G } ( d ) \coloneqq M _ { \mathfrak { h } _ { G } } ( d ) .$$

Define the normalized contrast kernel and statistic by

$$\mathfrak { c } _ { d } \colon = \frac { \mathfrak { h } _ { P _ { 3 } } } { J _ { P _ { 3 } } ( d ) } - \frac { \mathfrak { h } _ { K _ { 3 } } } { J _ { K _ { 3 } } ( d ) } , \quad C _ { n } ( r ) \colon = U _ { \mathfrak { c } _ { d } } ( r ) .$$

$$C _ { n } ( r ) = \frac { U _ { P _ { 3 } } ( r ) } { J _ { P _ { 3 } } ( d ) } - \frac { U _ { K _ { 3 } } ( r ) } { J _ { K _ { 3 } } ( d ) } .$$

$$D _ { d } \colon = \frac { M _ { P _ { 3 } } ( d ) } { J _ { P _ { 3 } } ( d ) } - \frac { M _ { K _ { 3 } } ( d ) } { J _ { K _ { 3 } } ( d ) } , \quad \gamma _ { d } \colon = \frac { 3 D _ { d } } { 2 d } .$$

Thus

Define

The explicit Euclidean moment formulas proved later imply D d &gt; 0 and γ d &gt; 0 for every d ≥ 2; see Lemma 5.4. Since J c d ( d ) = 0 and M c d ( d ) = D d , Theorem 3.2 gives

$$\mathbb { E } C _ { n } ( r ) = - \gamma _ { d } \binom { n } { 3 } r ^ { 2 d + 2 } \mathcal { G } _ { 3 } ( f ; g ) + o \left ( n ^ { 3 } r ^ { 2 d + 2 } \right ) .$$

$$\widehat { \mathcal { G } } _ { 3 , n } ( r ) \colon = - \frac { C _ { n } ( r ) } { \gamma _ { d } \binom { n } { 3 } r ^ { 2 d + 2 } } .$$

Define

Theorem 3.4. There are C &lt; ∞ and r 0 &gt; 0 such that, for n ≥ 3 and 0 &lt; r &lt; r 0 ,

$$\text {Var} \, C _ { n } ( r ) \leq C \left ( n ^ { 3 } r ^ { 2 d } + n ^ { 4 } r ^ { 3 d } + n ^ { 5 } r ^ { 4 d + 4 } \right ) .$$

$$\text {Var} \, \widehat { \mathcal { G } } _ { 3 , n } ( r ) \leq C \left ( \frac { 1 } { n ^ { 3 } r ^ { 2 d + 4 } } + \frac { 1 } { n ^ { 2 } r ^ { d + 4 } } + \frac { 1 } { n } \right ) .$$

$$n ^ { 3 } r _ { n } ^ { 2 d + 4 } \rightarrow \infty , \quad n ^ { 2 } r _ { n } ^ { d + 4 } \rightarrow \infty .$$

$$\widehat { \mathcal { G } } _ { 3 , n } ( r _ { n } ) \stackrel { \mathbb { P } } { \rightarrow } \mathcal { G } _ { 3 } ( f ; g ) .$$

For clarity in the proof section, an equivalent reformulation of Theorem 3.4 is restated as Theorem 6.2 in Section 6. That theorem is proved there, and hence Theorem 3.4 follows from it.

To state the projection-dominant limit, put

$$q _ { f } ( x ) \coloneqq \frac { 1 } { 2 d } \| \text {grad} \, f ( x ) \| _ { g } ^ { 2 } + \frac { 1 } { d } f ( x ) \Delta _ { g } f ( x ) - \frac { 1 } { 4 d } f ( x ) ^ { 2 } \, \text {scal} _ { g } ( x ) ,$$

Consequently,

Let r n ↓ 0 and assume

Then and Integration by parts gives


<!-- p:7 -->


$$\int _ { M } q _ { f } f \, d v o l _ { g } = - \frac { 3 } { 2 d } \mathcal { G } _ { 3 } ( f ; g ) , \quad \int _ { M } \psi _ { f } f \, d v o l _ { g } = 0 .$$

Theorem 3.5. Let r n ↓ 0 and suppose

$$n r _ { n } ^ { d + 4 } \rightarrow \infty .$$

$$\sqrt { n } \left ( \widehat { \mathcal { G } } _ { 3 , n } ( r _ { n } ) - \mathbb { E } \widehat { \mathcal { G } } _ { 3 , n } ( r _ { n } ) \right ) \stackrel { \mathcal { D } } { \rightarrow } N ( 0 , \sigma _ { f } ^ { 2 } ) ,$$

$$\sigma _ { f } ^ { 2 } \colon = 4 d ^ { 2 } \int _ { M } \psi _ { f } ( x ) ^ { 2 } f ( x ) \, d v o l _ { g } ( x ) .$$

Then

where

The limit is understood as degenerate when σ 2 f = 0 .

For clarity in the proof section, an equivalent reformulation of Theorem 3.5 is restated as Theorem 6.3 in Section 6. That theorem is proved there, and hence Theorem 3.5 follows from it. Remark 3.6 . The central limit theorem is centered at the exact expectation. Since the second-

order expansion provides no quantitative rate for

$$\mathbb { E } \mathcal { G } _ { 3 , n } ( r _ { n } ) - \mathcal { G } _ { 3 } ( f ; g ) ,$$

we do not claim a target-centered central limit theorem or confidence intervals for G 3 ( f ; g ).

Corollary 3.7. Assume d = 2 and f ≡ V - 1 , where V := Vol g ( M ) . Then

$$J _ { P _ { 3 } } ( 2 ) = M _ { P _ { 3 } } ( 2 ) = \frac { 9 \sqrt { 3 } \pi } { 4 } , \quad J _ { K _ { 3 } } ( 2 ) = \frac { \pi ( 4 \pi - 3 \sqrt { 3 } ) } { 4 } , \quad \gamma _ { 2 } = \frac { \pi } { 4 \pi - 3 \sqrt { 3 } } .$$

Let

$$\widehat { F } _ { 3 , n } ( r ) \colon = \frac { U _ { K _ { 3 } } ( r ) } { \left ( ^ { n } _ { 3 } \right ) r ^ { 4 } J _ { K _ { 3 } } ( 2 ) } , \quad \widehat { V } _ { n } ( r ) \colon = \begin{cases} \widehat { F } _ { 3 , n } ( r ) ^ { - 1 / 2 } , & \widehat { F } _ { 3 , n } ( r ) > 0 , \\ 1 , & \widehat { F } _ { 3 , n } ( r ) = 0 . \end{cases}$$

Define

$$\widehat { \chi } _ { n } ( r ) \coloneqq \frac { 3 } { 2 \pi } \widehat { V } _ { n } ( r ) ^ { 3 } \widehat { \mathcal { G } } _ { 3 , n } ( r ) = - \frac { 3 ( 4 \pi - 3 \sqrt { 3 } ) } { 2 \pi ^ { 2 } } \frac { \widehat { V } _ { n } ( r ) ^ { 3 } C _ { n } ( r ) } { \binom { n } { 3 } r ^ { 6 } } .$$

If r n ↓ 0 satisfies

then

$$\psi _ { f } ( x ) \coloneqq q _ { f } ( x ) + \frac { 3 } { 2 d } \mathcal { G } _ { 3 } ( f ; g ) .$$

$$n ^ { 2 } r _ { n } ^ { 6 } \rightarrow \infty ,$$

$$\widehat { V } _ { n } ( r _ { n } ) \stackrel { \mathbb { P } } { \rightarrow } V , \quad \widehat { \chi } _ { n } ( r _ { n } ) \stackrel { \mathbb { P } } { \rightarrow } \chi ( M ) .$$

Consequently, since χ ( M ) is integer-valued, rounding ̂ χ n ( r n ) to the nearest integer recovers χ ( M ) with probability tending to one.

For clarity in the proof section, an equivalent reformulation of Corollary 3.7 is restated as Corollary 6.5 in Section 6. That corollary is proved there, and hence Corollary 3.7 follows from it.


<!-- p:8 -->


### 3.3 Degree-two threshold: k = 2

For z 1 , z 2 ∈ R d , define

$$a = 1 _ { \{ | z _ { 1 } | \leq 1 \} } , \quad b = 1 _ { \{ | z _ { 2 } | \leq 1 \} } , \quad c = 1 _ { \{ | z _ { 1 } - z _ { 2 } | \leq 1 \} } .$$

$$\mathfrak { h } _ { 2 } ( a , b , c ) \colon = 1 _ { \{ a + b + c \geq 2 \} } .$$

The indicator that the three-point configuration { 0 , z 1 , z 2 } has maximum degree at least 2 is

$$H _ { 2 } ( z _ { 1 } , z _ { 2 } ) = \mathfrak { h } _ { 2 } ( a , b , c ) = a b + a c + b c - 2 a b c .$$

Define the Euclidean constants

$$A _ { 2 } ( d ) \coloneqq \frac { 1 } { 6 } \int _ { ( \mathbb { R } ^ { d } ) ^ { 2 } } H _ { 2 } ( z _ { 1 } , z _ { 2 } ) \, d z _ { 1 } \, d z _ { 2 } , \quad C _ { 2 } ( d ) \coloneqq \frac { 1 } { 4 d } \int _ { ( \mathbb { R } ^ { d } ) ^ { 2 } } H _ { 2 } ( z _ { 1 } , z _ { 2 } ) | z _ { 1 } | ^ { 2 } \, d z _ { 1 } \, d z _ { 2 } .$$

Both are positive. Explicit lens-volume and one-dimensional formulas are given in Section 5 and Appendix A.

Theorem 3.8. Under the standing assumptions, assume d &gt; 6 and define r 2 ,n ( t ) := tn - 3 / (2 d ) . Then, as n →∞ , for every T &lt; ∞ , uniformly for 0 ≤ t ≤ T ,

$$\log \mathbb { P } \{ S _ { 2 , n } > r _ { 2 , n } ( t ) \} & = - \ A _ { 2 } ( d ) t ^ { 2 d } \int _ { M } f ^ { 3 } \, d v _ { g } \\ & + C _ { 2 } ( d ) t ^ { 2 d + 2 } n ^ { - 3 / d } \left \{ \begin{array} { c } \int _ { M } f \| \text {grad} \, f \| _ { g } ^ { 2 } \, d v _ { g } \\ + \frac { 1 } { 6 } \int _ { M } f ^ { 3 } \, \text {Scal} _ { g } \, d v _ { g } \end{array} \right \} + o ( n ^ { - 3 / d } ) . \\ \intertext { T h o r \, \text {proof is completed in Section 5.  M o r is  presently  Proposition  5. 8 gives the  o r r e s p o n d i n g } }$$

The proof is completed in Section 5. More precisely, Proposition 5.8 gives the corresponding zero-count expansion for the active-triple count N 2 ( r ), and Theorem 3.8 follows from that proposition together with the identity

$$\{ S _ { 2 , n } > r \} = \{ N _ { 2 } ( r ) = 0 \} .$$

Corollary 3.9. Under the hypotheses of Theorem 3.8, if f ≡ Vol g ( M ) - 1 , then, for every T &lt; ∞ , uniformly for 0 ≤ t ≤ T ,

$$\log \mathbb { P } \{ S _ { 2 , n } > t n ^ { - 3 / ( 2 d ) } \} = - \frac { A _ { 2 } ( d ) t ^ { 2 d } } { \text {Vol} _ { g } ( M ) ^ { 2 } } + \frac { C _ { 2 } ( d ) t ^ { 2 d + 2 } } { 6 \text {Vol} _ { g } ( M ) ^ { 3 } } \left ( \int _ { M } \text {Scalar } d \text {vol} _ { g } \right ) n ^ { - 3 / d } + o ( n ^ { - 3 / d } ) .$$

This corollary follows immediately from Theorem 3.8 by taking f ≡ Vol g ( M ) - 1 . Indeed,

$$\text {grad} \, f = 0 , \quad \int _ { M } f ^ { 3 } \, d \text {vol} _ { g } = \text {Vol} _ { g } ( M ) ^ { - 2 } ,$$

$$\int _ { M } f ^ { 3 } \, S c a l _ { g } \ d v o l _ { g } = V o l _ { g } ( M ) ^ { - 3 } \int _ { M } S c a l _ { g } \ d v o l _ { g } .$$

and

Remark 3.10 (Why d &gt; 6) . The geometric correction is of order n - 3 /d , whereas the largest dependency-graph error is O ( n - 1 / 2 ). Thus d &gt; 6 ensures n - 1 / 2 = o ( n - 3 /d ).

Define


<!-- p:9 -->


## 4 Preliminaries

### 4.1 Chord expansion and boundary variation

Let F ( M ) denote the orthonormal frame bundle of M . Thus an element ( x, τ ) ∈ F ( M ) consists of a point x ∈ M and a linear isometry

$$\tau \colon \mathbb { R } ^ { d } \longrightarrow T _ { x } M .$$

$$\exp _ { x , \tau } ( u ) \colon = \exp _ { x } ( \tau u ) ,$$

and pull back the curvature tensor to R d by setting

$$R _ { x , \tau } ( a , b , c , d ) \coloneqq R _ { x } ( \tau a , \tau b , \tau c , \tau d ) .$$

Since M is closed, the frame bundle F ( M ) is compact.

Define the rescaled two-point squared-distance function by

$$\Phi _ { r , x , \tau } ( z , w ) \colon = r ^ { - 2 } d _ { g } ( \exp _ { x , \tau } ( r z ) , \exp _ { x , \tau } ( r ( z - w ) ) ) ^ { 2 } \, .$$

In Euclidean space, this function is exactly | w | 2 . We first identify the exact fourth-order curvature correction and only then use Taylor's theorem to control the remainder. This distinction is important because the moving-boundary coefficient depends on the precise quartic curvature term.

All derivatives with respect to the variables u, v, z, w ∈ R d are ordinary Euclidean Fr ́ echet derivatives. For a linear map A : R m → R n , we denote its operator norm by

$$\| A \| \colon = \sup _ { | \xi | = 1 } | A \xi | ,$$

where | · | denotes the standard Euclidean norm.

Lemma 4.1. Let K ⊂ R d × R d be compact. There exist constants r K &gt; 0 and C K &gt; 0 and a family of functions R r,x,τ , continuously differentiable in the w variable, such that, for 0 &lt; r &lt; r K , ( x, τ ) ∈ F ( M ) , and ( z, w ) ∈ K , one has

$$\Phi _ { r , x , \tau } ( z , w ) = | w | ^ { 2 } - \frac { r ^ { 2 } } { 3 } R _ { x , \tau } ( z , w , z , w ) + r ^ { 3 } \mathcal { R } _ { r , x , \tau } ( z , w ) ,$$

We write

and

$$\sup _ { 0 < r < r _ { K } , \ ( x , \tau ) \in \mathcal { F } ( M ) } ( | \mathcal { R } _ { r , x , \tau } ( z , w ) | + \| D _ { w } \mathcal { R } _ { r , x , \tau } ( z , w ) \| ) \leq C _ { K } .$$

Proof. For a continuous map f : [0 , 1] → R d , we define ∥ f ∥ C 0 ([0 , 1]) := sup 0 ≤ t ≤ 1 | f ( t ) | . For f ∈ C 1 ([0 , 1]; R d ), we set ∥ f ∥ C 1 ([0 , 1]) := ∥ f ∥ C 0 ([0 , 1]) + ∥  ̇ f ∥ C 0 ([0 , 1]) .

For each ( x, τ ) ∈ F ( M ), we use the normal coordinates induced by τ and set

$$D _ { x , \tau } ( u , v ) \colon = d _ { g } ( \exp _ { x , \tau } ( u ) , \exp _ { x , \tau } ( v ) ) ^ { 2 } \, .$$

Since M is closed, its convexity radius is positive. Hence there exists s 0 &gt; 0 such that, for every ( x, τ ) ∈ F ( M ) and every u, v ∈ R d satisfying | u | + | v | &lt; s 0 , the points exp x,τ ( u ) and exp x,τ ( v ) lie in a common strongly convex normal neighborhood. In particular, the minimizing geodesic between them is unique, and D x,τ ( u, v ) depends smoothly on ( x, τ, u, v ) in this region. Fix 0 &lt; s 1 &lt; s 0 and restrict to the compact parameter set

$$\{ ( x , \tau , u , v ) \, \colon ( x , \tau ) \in \mathcal { F } ( M ) , \quad | u | + | v | \leq s _ { 1 } \} \, .$$


<!-- p:10 -->


Since this parameter set is compact, all derivatives of D x,τ ( u, v ) needed below are uniformly bounded on it.

We first identify the fourth-order jet of D x,τ . The standard normal-coordinate metric expansion (see, for example, [6,11,18]) gives, under our curvature convention,

$$g _ { y } ( a , b ) = \langle a , b \rangle - \frac { 1 } { 3 } R _ { x , \tau } ( a , y , b , y ) + O ( | y | ^ { 3 } | a | | b | ) ,$$

uniformly in ( x, τ ). Let q = v - u , let λ ( t ) = u + tq , and let γ be the coordinate representation of the minimizing geodesic from u to v , affinely parametrized on [0 , 1]. The normal-coordinate metric is uniformly equivalent to the Euclidean metric on the restricted parameter set. Since γ is minimizing and has constant speed,

$$| \gamma ^ { \prime } ( t ) | _ { g _ { \gamma ( t ) } } = d _ { g } ( \exp _ { x , \tau } ( u ) , \exp _ { x , \tau } ( v ) ) \leq | u | + | v | = \colon s .$$

The uniform equivalence of the two metrics therefore gives ∥ γ ′ ∥ C 0 ([0 , 1]) = O ( s ). Since γ ( t ) = u + ∫ t 0 γ ′ ( r ) dr , we also have ∥ γ ∥ C 0 ([0 , 1]) = O ( s ). Hence

$$\| \gamma \| _ { C ^ { 1 } ( [ 0 , 1 ] ) } = O ( s ) .$$

In normal coordinates, the Christoffel symbols satisfy Γ( y ) = O ( | y | ) uniformly in ( x, τ ) The geodesic equation gives | γ ′′ ( t ) | ≤ C | γ ( t ) | | γ ′ ( t ) | 2 = O ( s 3 ), and hence

$$\| \gamma ^ { \prime \prime } \| _ { C ^ { 0 } ( [ 0 , 1 ] ) } = O ( s ^ { 3 } ) .$$

We set h := γ - λ . Since λ ′′ = 0, we have h ′′ = γ ′′ and h (0) = h (1) = 0. Using the endpoint conditions and integrating twice, one obtains

$$\| h \| _ { C ^ { 1 } ( [ 0 , 1 ] ) } \leq C \| h ^ { \prime \prime } \| _ { C ^ { 0 } ( [ 0 , 1 ] ) } .$$

$$\| h \| _ { C ^ { 1 } ( [ 0 , 1 ] ) } = \| \gamma - \lambda \| _ { C ^ { 1 } ( [ 0 , 1 ] ) } = O ( s ^ { 3 } ) .$$

Since γ is a minimizing geodesic affinely parametrized on [0 , 1], it has constant speed, and its energy equals the square of its length. Therefore,

$$D _ { x , \tau } ( u , v ) = \int _ { 0 } ^ { 1 } g _ { \gamma ( t ) } \left ( \gamma ^ { \prime } ( t ) , \gamma ^ { \prime } ( t ) \right ) \, d t .$$

Applying (4.1) with y = γ ( t ) and a = b = γ ′ ( t ), we obtain

$$g _ { \gamma ( t ) } ( \gamma ^ { \prime } ( t ) , \gamma ^ { \prime } ( t ) ) = | \gamma ^ { \prime } ( t ) | ^ { 2 } - \frac { 1 } { 3 } R _ { x , \tau } ( \gamma ^ { \prime } ( t ) , \gamma ( t ) , \gamma ^ { \prime } ( t ) , \gamma ( t ) ) + O ( | \gamma ( t ) | ^ { 3 } | \gamma ^ { \prime } ( t ) | ^ { 2 } ) \, .$$

Since ∥ γ ∥ C 1 ([0 , 1]) = O ( s ), the remainder term is uniformly O ( s 5 ). Hence

$$D _ { x , \tau } ( u , v ) = \int _ { 0 } ^ { 1 } | \gamma ^ { \prime } ( t ) | ^ { 2 } \, d t - \frac { 1 } { 3 } \int _ { 0 } ^ { 1 } R _ { x , \tau } ( \gamma ^ { \prime } ( t ) , \gamma ( t ) , \gamma ^ { \prime } ( t ) , \gamma ( t ) ) \, d t + O ( s ^ { 5 } ) .$$

Since γ = λ + h and γ ′ = q + h ′ ,

$$\int _ { 0 } ^ { 1 } | \gamma ^ { \prime } ( t ) | ^ { 2 } \, d t & = \int _ { 0 } ^ { 1 } | q + h ^ { \prime } ( t ) | ^ { 2 } \, d t \\ & = | q | ^ { 2 } + 2 \int _ { 0 } ^ { 1 } \langle q , h ^ { \prime } ( t ) \rangle \, d t + \int _ { 0 } ^ { 1 } | h ^ { \prime } ( t ) | ^ { 2 } \, d t .$$

Consequently, The middle term vanishes because ∫ 1 0 ⟨ q, h ′ ( t ) ⟩ dt = ⟨ q, h (1) - h (0) ⟩ = 0. Moreover, since ∥ h ∥ C 1 ([0 , 1]) = O ( s 3 ), we have ∫ 1 0 | h ′ ( t ) | 2 dt = O ( s 6 ). Therefore


<!-- p:11 -->


$$\int _ { 0 } ^ { 1 } | \gamma ^ { \prime } ( t ) | ^ { 2 } \, d t = | q | ^ { 2 } + O ( s ^ { 6 } ) .$$

By multilinearity,

$$R _ { x , \tau } ( \gamma ^ { \prime } , \gamma , \gamma ^ { \prime } , \gamma ) - R _ { x , \tau } ( q , \lambda , q , \lambda ) & = R _ { x , \tau } ( \gamma ^ { \prime } - q , \gamma , \gamma ^ { \prime } , \gamma ) + R _ { x , \tau } ( q , \gamma - \lambda , \gamma ^ { \prime } , \gamma ) \\ & + R _ { x , \tau } ( q , \lambda , \gamma ^ { \prime } - q , \gamma ) + R _ { x , \tau } ( q , \lambda , q , \gamma - \lambda ) .$$

Since the curvature tensor is uniformly bounded,

$$| q | = O ( s ) , \quad \| \lambda \| _ { C ^ { 0 } ( [ 0 , 1 ] ) } = O ( s ) , \quad \| \gamma \| _ { C ^ { 1 } ( [ 0 , 1 ] ) } = O ( s ) ,$$

and

$$\| \gamma - \lambda \| _ { C ^ { 1 } ( [ 0 , 1 ] ) } = \| h \| _ { C ^ { 1 } ( [ 0 , 1 ] ) } = O ( s ^ { 3 } ) ,$$

each term on the right-hand side is O ( s 6 ), uniformly in t ∈ [0 , 1]. Hence

$$R _ { x , \tau } ( \gamma ^ { \prime } , \gamma , \gamma ^ { \prime } , \gamma ) = R _ { x , \tau } ( q , \lambda , q , \lambda ) + O ( s ^ { 6 } ) .$$

Substituting these two estimates into the preceding expansion of D x,τ ( u, v ) gives

$$D _ { x , \tau } ( u , v ) = | q | ^ { 2 } - \frac { 1 } { 3 } \int _ { 0 } ^ { 1 } R _ { x , \tau } ( q , \lambda ( t ) , q , \lambda ( t ) ) \, d t + O ( s ^ { 5 } ) .$$

Since λ ( t ) = u + tq , the skew symmetries of the curvature tensor imply

$$R _ { x , \tau } ( q , \lambda ( t ) , q , \lambda ( t ) ) = R _ { x , \tau } ( q , u , q , u ) .$$

Moreover, since q = v - u ,

$$R _ { x , \tau } ( q , u , q , u ) = R _ { x , \tau } ( u , v , u , v ) .$$

Therefore,

$$D _ { x , \tau } ( u , v ) = | u - v | ^ { 2 } - \frac { 1 } { 3 } R _ { x , \tau } ( u , v , u , v ) + O ( s ^ { 5 } ) .$$

$$E _ { x , \tau } ( u , v ) \colon = D _ { x , \tau } ( u , v ) - | u - v | ^ { 2 } + \frac { 1 } { 3 } R _ { x , \tau } ( u , v , u , v ) .$$

Set

Since E x,τ ( u, v ) = O ( s 5 ), all derivatives of E x,τ at (0 , 0) of total order at most four vanish. The fifth derivatives of E x,τ are uniformly bounded on the compact restricted parameter set. Taylor's theorem with integral remainder, applied also after one differentiation, therefore yields uniformly on this compact subdomain

$$| E _ { x , \tau } ( u , v ) | \leq C s ^ { 5 } , \quad | D _ { ( u , v ) } E _ { x , \tau } ( u , v ) | \leq C s ^ { 4 } .$$

For ( z, w ) in a fixed compact set K , we set u = rz and v = r ( z - w ). Then

$$s = r | z | + r | z - w | = O _ { K } ( r ) , \quad | u - v | ^ { 2 } = r ^ { 2 } | w | ^ { 2 } .$$

By the symmetries of the curvature tensor,

$$R _ { x , \tau } ( u , v , u , v ) & = r ^ { 4 } R _ { x , \tau } ( z , z - w , z , z - w ) \\ & = r ^ { 4 } R _ { x , \tau } ( z , w , z , w ) .$$


<!-- p:12 -->


Hence

Define

$$\mathcal { R } _ { r , x , \tau } ( z , w ) \colon = r ^ { - 5 } E _ { x , \tau } ( r z , r ( z - w ) ) .$$

Then Φ r,x,τ ( z, w ) = | w | 2 - r 2 3 R x,τ ( z, w, z, w ) + r 3 R r,x,τ ( z, w ), and |R r,x,τ ( z, w ) | ≤ C K . By the chain rule,

$$D _ { w } \mathcal { R } _ { r , x , \tau } ( z , w ) = - r ^ { - 4 } D _ { v } E _ { x , \tau } ( r z , r ( z - w ) ) .$$

Since | D ( u,v ) E x,τ ( u, v ) | ≤ Cs 4 , we have

$$\| D _ { v } E _ { x , \tau } ( r z , r ( z - w ) ) \| \leq C _ { K } r ^ { 4 } .$$

Therefore, ∥ D w R r,x,τ ( z, w ) ∥ ≤ C K . This proves the lemma.

Corollary 4.2. Let L ⊂ R d × S d - 1 be compact and let ρ range over a fixed compact neighborhood [1 - ε, 1 + ε ] of 1 . Then, uniformly in ( x, τ ) ∈ F ( M ) , ( z, θ ) ∈ L , and ρ ,

$$\partial _ { \rho } \Phi _ { r , x , \tau } ( z , \rho \theta ) = 2 \rho - \frac { 2 r ^ { 2 } } { 3 } \rho R _ { x , \tau } ( z , \theta , z , \theta ) + O ( r ^ { 3 } ) .$$

Consequently, for all sufficiently small r , the equation Φ r,x,τ ( z, ρθ ) = 1 has a unique solution ρ r,x,τ ( z, θ ) near ρ = 1 , and

$$\rho _ { r , x , \tau } ( z , \theta ) = 1 + \frac { r ^ { 2 } } { 6 } R _ { x , \tau } ( z , \theta , z , \theta ) + O ( r ^ { 3 } ) ,$$

uniformly in ( x, τ ) ∈ F ( M ) and ( z, θ ) ∈ L .

Proof. Apply Lemma 4.1 to the compact set

$$K _ { L , \varepsilon } \colon = \{ ( z , \rho \theta ) \, \colon ( z , \theta ) \in L , \ \rho \in [ 1 - \varepsilon , 1 + \varepsilon ] \} \, .$$

Since R x,τ ( z, ρθ, z, ρθ ) = ρ 2 R x,τ ( z, θ, z, θ ), we have

$$\Phi _ { r , x , \tau } ( z , \rho \theta ) = \rho ^ { 2 } - \frac { r ^ { 2 } } { 3 } \rho ^ { 2 } R _ { x , \tau } ( z , \theta , z , \theta ) + r ^ { 3 } \mathcal { R } _ { r , x , \tau } ( z , \rho \theta ) .$$

Differentiating with respect to ρ gives

$$\partial _ { \rho } \Phi _ { r , x , \tau } ( z , \rho \theta ) = 2 \rho - \frac { 2 r ^ { 2 } } { 3 } \rho R _ { x , \tau } ( z , \theta , z , \theta ) + r ^ { 3 } \mathbf D _ { w } \mathcal { R } _ { r , x , \tau } ( z , \rho \theta ) [ \theta ] .$$

Since | θ | = 1 and D w R r,x,τ is uniformly bounded, the last term is O ( r 3 ). Thus

$$\partial _ { \rho } \Phi _ { r , x , \tau } ( z , \rho \theta ) = 2 \rho - \frac { 2 r ^ { 2 } } { 3 } \rho R _ { x , \tau } ( z , \theta , z , \theta ) + O ( r ^ { 3 } ) .$$

$$F _ { r , x , \tau , z , \theta } ( \rho ) \colon = \Phi _ { r , x , \tau } ( z , \rho \theta ) - 1 .$$

On [1 - ε, 1 + ε ], we have ∂ ρ F r,x,τ,z,θ ( ρ ) = 2 ρ + O ( r 2 ). Thus, after decreasing r if necessary,

$$\partial _ { \rho } F _ { r , x , \tau , z , \theta } ( \rho ) \geq 1 ,$$

uniformly in the remaining parameters. Hence F r,x,τ,z,θ is strictly increasing. Set

$$A _ { x , \tau } ( z , \theta ) \colon = R _ { x , \tau } ( z , \theta , z , \theta ) .$$

Finally, set

$$\Phi _ { r , x , \tau } ( z , w ) = | w | ^ { 2 } - \frac { r ^ { 2 } } { 3 } R _ { x , \tau } ( z , w , z , w ) + r ^ { - 2 } E _ { x , \tau } ( r z , r ( z - w ) ) .$$


<!-- p:13 -->


Since F ( M ) × L is compact, there exists A L &gt; 0 such that

$$| A _ { x , \tau } ( z , \theta ) | \leq A _ { L } .$$

Choose B &gt; 0 sufficiently large. Since F r,x,τ,z,θ ( ρ ) = ρ 2 - 1 - r 2 3 ρ 2 A x,τ ( z, θ ) + O ( r 3 ), we obtain, for sufficiently small r ,

$$F _ { r , x , \tau , z , \theta } ( 1 - B r ^ { 2 } ) < 0 , \quad F _ { r , x , \tau , z , \theta } ( 1 + B r ^ { 2 } ) > 0 .$$

The intermediate value theorem therefore gives a root

$$\rho _ { r , x , \tau } ( z , \theta ) \in ( 1 - B r ^ { 2 } , 1 + B r ^ { 2 } ) ,$$

and strict monotonicity shows that this root is unique. Hence

$$| \rho _ { r , x , \tau } ( z , \theta ) - 1 | \leq B r ^ { 2 }$$

uniformly in ( x, τ ) ∈ F ( M ) and ( z, θ ) ∈ L . In particular, ρ r,x,τ ( z, θ ) = 1 + O ( r 2 ), where the O ( r 2 ) term is uniform in these parameters. We write

$$\rho _ { r , x , \tau } ( z , \theta ) = 1 + \delta .$$

Then δ = O ( r 2 ) uniformly in the same parameters, and substitution into Φ r,x,τ ( z, ρθ ) = 1 gives

$$2 \delta - \frac { r ^ { 2 } } { 3 } R _ { x , \tau } ( z , \theta , z , \theta ) + O \left ( \delta ^ { 2 } + r ^ { 2 } | \delta | + r ^ { 3 } \right ) = 0 .$$

Since δ 2 + r 2 | δ | = O ( r 4 ), we conclude that

$$2 \delta - \frac { r ^ { 2 } } { 3 } R _ { x , \tau } ( z , \theta , z , \theta ) + O ( r ^ { 3 } ) = 0 .$$

$$\delta = \frac { r ^ { 2 } } { 6 } R _ { x , \tau } ( z , \theta , z , \theta ) + O ( r ^ { 3 } ) ,$$

and hence ρ r,x,τ ( z, θ ) = 1 + r 2 6 R x,τ ( z, θ, z, θ ) + O ( r 3

).

For the remainder of this subsection, for each x choose any τ ∈ F x and suppress τ from the notation. The resulting statements are independent of this choice and remain uniform over ( x, τ ) ∈ F ( M ).

The Ricci and scalar traces in the next lemma use the convention fixed in Section 2:

$$R i c _ { R } ( w , w ) = \sum _ { i } R ( e _ { i } , w , e _ { i } , w ) , \quad \text {Scalar} ( R ) = \sum _ { i } R i c _ { R } ( e _ { i } , e _ { i } ) .$$

Lemma 4.3. Let ψ : R d × S d - 1 → R be bounded, measurable, compactly supported in the first variable, and invariant under simultaneous rotations:

$$\psi ( O z , O w ) = \psi ( z , w ) , \quad O \in O ( d ) .$$

Then, for d ≥ 2 and every algebraic curvature tensor R on R d ,

$$\int _ { S ^ { d - 1 } } \int _ { \mathbb { R } ^ { d } } \psi ( z , w ) R ( z , w , z , w ) \, d z \, d \sigma ( w ) = \frac { \text {Scale} ( R ) } { d ( d - 1 ) } \int _ { S ^ { d - 1 } } \int _ { \mathbb { R } ^ { d } } \psi ( z , w ) \left ( | z | ^ { 2 } - ( z \cdot w ) ^ { 2 } \right ) d z \, d \sigma ( w ) .$$

Therefore, Proof. Fix w ∈ S d - 1 and write


<!-- p:14 -->


$$z = s w + u , \quad s = z \cdot w , \quad u \in w ^ { \perp } .$$

By the alternating symmetries of R ,

$$R ( z , w , z , w ) = R ( u , w , u , w ) , \quad | z | ^ { 2 } - ( z \cdot w ) ^ { 2 } = | u | ^ { 2 } .$$

For fixed w , simultaneous rotational invariance implies that the restriction of ψ ( sw + u, w ) to w ⊥ is radial in u . Using the Euclidean identification R d ≃ ( R d ) ∗ , we regard u ⊗ u as the rank-one endomorphism

$$v \longmapsto \langle u , v \rangle u .$$

The resulting tensor integral is invariant under every orthogonal transformation fixing w , and hence it is a scalar multiple of Π w ⊥ . Taking its trace determines the scalar and gives

$$\int _ { \mathbb { R } } \int _ { w ^ { \perp } } \psi ( s w + u , w ) u \otimes u \, d u \, d s = \frac { A ( w ) } { d - 1 } \, \Pi _ { w ^ { \perp } } ,$$

where Π w ⊥ is the orthogonal projection onto w ⊥ and

$$A ( w ) \colon = \int _ { \mathbb { R } } \int _ { w ^ { \perp } } \psi ( s w + u , w ) | u | ^ { 2 } \, d u \, d s .$$

Simultaneous rotational invariance implies that A ( w ) is independent of w . Denote its common value by A . Choose an orthonormal basis

$$e _ { 1 } = w , e _ { 2 } , \dots , e _ { d } , \quad e _ { 2 } , \dots , e _ { d } \in w ^ { \perp } .$$

Contracting the preceding tensor identity with

$$( v _ { 1 } , v _ { 2 } ) \longmapsto R ( v _ { 1 } , w , v _ { 2 } , w ) ,$$

$$\int _ { \mathbb { R } ^ { d } } \psi ( z , w ) R ( z , w , z , w ) \, d z & = \frac { A } { d - 1 } \sum _ { \alpha = 2 } ^ { d } R ( e _ { \alpha } , w , e _ { \alpha } , w ) \\ & = \frac { A } { d - 1 } \, R i c _ { R } ( w , w ) .$$

The last equality follows from e 1 = w and R ( w,w,w,w ) = 0. Integrating over S d - 1 and using

$$\int _ { S ^ { d - 1 } } R i c _ { R } ( w , w ) \, d \sigma ( w ) = \frac { \sigma ( S ^ { d - 1 } ) } { d } \, S c a l ( R ) = \omega _ { d } \, S c a l ( R )$$

gives

$$\int _ { S ^ { d - 1 } } \int _ { \mathbb { R } ^ { d } } \psi ( z , w ) R ( z , w , z , w ) \, d z \, d \sigma ( w ) = \frac { A \omega _ { d } } { d - 1 } \, S c a l ( R ) .$$

On the other hand,

we obtain

$$\int _ { S ^ { d - 1 } } \int _ { \mathbb { R } ^ { d } } \psi ( z , w ) ( | z | ^ { 2 } - ( z \cdot w ) ^ { 2 } ) \, d z \, d \sigma ( w ) = d \omega _ { d } A .$$

Combining the last two displays yields the stated coefficient 1 / ( d ( d - 1)).


<!-- p:15 -->


Let d prod denote the distance induced by the product metric on R d × S d - 1 . For p ∈ R d × S d - 1 and A ⊂ R d × S d - 1 , we write

$$\text {dist} _ { \text {prod} } ( p , A ) \colon = \inf _ { q \in A } d _ { \text {prod} } ( p , q ) .$$

Define

$$T _ { 1 } \coloneqq \{ ( z , \theta ) \in \mathbb { R } ^ { d } \times S ^ { d - 1 } \colon | z | = 1 \} , \quad T _ { 2 } \coloneqq \{ ( z , \theta ) \in \mathbb { R } ^ { d } \times S ^ { d - 1 } \colon | z - \theta | = 1 \} .$$

In the definition of T 2 , both z and θ are regarded as vectors in the same Euclidean space R d . The defining functions F 1 ( z, θ ) = | z | 2 - 1 and F 2 ( z, θ ) = | z - θ | 2 - 1 have nonzero differentials on their zero sets. At an intersection point, | z | = | z - θ | = 1 implies z · θ = 1 / 2. The S d - 1 - tangent component of dF 2 is - 2( z - ( z · θ ) θ ), which is nonzero there, whereas the corresponding component of dF 1 vanishes. Thus the hypersurfaces meet transversely.

For a compact set K ⊂ R d × S d - 1 and a measurable set A ⊂ R d × S d - 1 , we write

$$\text {meas} _ { K } ( A ) \colon = \int _ { A \cap K } d z \, d \sigma ( \theta ) .$$

Lemma 4.4. Assume d ≥ 2 , and let K ⊂ R d × S d - 1 be compact. Then there exist constants C K &lt; ∞ and η K &gt; 0 such that

$$\text {meas} _ { K } \left \{ p \in \mathbb { R } ^ { d } \times S ^ { d - 1 } \colon \text {dist} _ { \text {prod} } ( p , T _ { 1 } \cup T _ { 2 } ) < \eta \right \} \leq C _ { K } \eta , \quad 0 < \eta < \eta _ { K } .$$

Proof. Since T 1 and T 2 are compact smooth embedded hypersurfaces, the tubular neighborhood theorem implies that, for each i = 1 , 2, there exist constants C K,i &lt; ∞ and η i &gt; 0 such that

$$\text {meas} _ { K } \left \{ p \colon \text {dist} _ { \text {prod} } ( p , T _ { i } ) < \eta \right \} \leq C _ { K , i } \eta , \quad 0 < \eta < \eta _ { i } .$$

Since dist prod ( p, T 1 ∪ T 2 ) = min { dist prod ( p, T 1 ) , dist prod ( p, T 2 ) } ,

$$\{ p \colon \text {dist} _ { \text {prod} } ( p , T _ { 1 } \cup T _ { 2 } ) < \eta \} = \bigcup _ { i = 1 } ^ { 2 } \{ p \colon \text {dist} _ { \text {prod} } ( p , T _ { i } ) < \eta \} \, .$$

Set

$$\eta _ { K } \colon = \min \{ \eta _ { 1 } , \eta _ { 2 } \} .$$

Then, for 0 &lt; η &lt; η K , the subadditivity of meas K gives

$$\text {meas} _ { K } \{ p \colon \text {dist} _ { \text {prod} } ( p , T _ { 1 } \cup T _ { 2 } ) & < \eta \} \\ & \leq \sum _ { i = 1 } ^ { 2 } \text {meas} _ { K } \{ p \colon \text {dist} _ { \text {prod} } ( p , T _ { i } ) < \eta \} \\ & \leq ( C _ { K , 1 } + C _ { K , 2 } ) \eta .$$

Thus the result follows with

$$C _ { K } \colon = C _ { K , 1 } + C _ { K , 2 } .$$

For ( x, τ ) ∈ F ( M ), r &gt; 0, and z, w ∈ R d , we put

$$c _ { r , x , \tau } ^ { l o c } ( z , w ) \colon = 1 _ { \{ \Phi _ { r , x , \tau } ( z , w ) \leq 1 \} } , \quad c ( w ) \colon = 1 _ { \{ | w | \leq 1 \} } .$$


<!-- p:16 -->


Lemma 4.5. Let χ ∈ C ∞ c ( R d × R d ) be fixed. There exist constants 0 &lt; r 0 ≤ r χ and 0 &lt; K 0 &lt; ∞ , depending only on χ and ( M,g ) , such that, for every ( x, τ ) ∈ F ( M ) and 0 &lt; r &lt; r 0 ,

̸

$$c _ { r , x , \tau } ^ { l o c } ( z , w ) \ne c ( w ) \quad \Longrightarrow \quad | | w | - 1 | \leq K _ { 0 } r ^ { 2 }$$

̸

for all ( z, w ) ∈ supp χ .

Proof. The two indicators agree when w = 0. For w = 0, write w = ρθ with θ ∈ S d - 1 . By Lemma 4.1, uniformly in ( x, τ ) and on supp χ ,

$$\Phi _ { r , x , \tau } ( z , \rho \theta ) = \rho ^ { 2 } - \frac { r ^ { 2 } } { 3 } \rho ^ { 2 } R _ { x , \tau } ( z , \theta , z , \theta ) + O ( r ^ { 3 } ) .$$

On the compact support of χ , after decreasing r 0 if necessary, the entire perturbation satisfies | Φ r,x,τ ( z, ρθ ) - ρ 2 | ≤ Cr 2 . Suppose that | ρ 2 - 1 | &gt; 2 Cr 2 . If ρ 2 - 1 &gt; 2 Cr 2 , then

$$\Phi _ { r , x , \tau } ( z , \rho \theta ) - 1 & = ( \rho ^ { 2 } - 1 ) + \left ( \Phi _ { r , x , \tau } ( z , \rho \theta ) - \rho ^ { 2 } \right ) \\ & \geq ( \rho ^ { 2 } - 1 ) - \left | \Phi _ { r , x , \tau } ( z , \rho \theta ) - \rho ^ { 2 } \right | \\ & > 2 C r ^ { 2 } - C r ^ { 2 } \\ & > 0 .$$

Thus both Φ r,x,τ ( z, ρθ ) and ρ 2 are greater than one. Similarly, if ρ 2 - 1 &lt; - 2 Cr 2 , then

$$\Phi _ { r , x , \tau } ( z , \rho \theta ) - 1 & \leq ( \rho ^ { 2 } - 1 ) + \left | \Phi _ { r , x , \tau } ( z , \rho \theta ) - \rho ^ { 2 } \right | \\ & < - 2 C r ^ { 2 } + C r ^ { 2 } \\ & < 0 .$$

Thus both Φ r,x,τ ( z, ρθ ) and ρ 2 are less than one. Consequently, whenever | ρ 2 - 1 | &gt; 2 Cr 2 , the quantities

$$\Phi _ { r , x , \tau } ( z , \rho \theta ) - 1 \quad \text {and} \quad \rho ^ { 2 } - 1$$

have the same sign, and hence the two indicators agree. Therefore, if the two indicators differ, then

$$| \rho ^ { 2 } - 1 | \leq 2 C r ^ { 2 } .$$

Since ρ ≥ 0, we have | ρ 2 - 1 | = | ρ - 1 | ( ρ +1) ≥ | ρ - 1 | . It follows that

$$| | w | - 1 | = | \rho - 1 | \leq 2 C r ^ { 2 } .$$

Thus the assertion holds with K 0 := 2 C .

Let

$$B \colon = \{ z \in \mathbb { R } ^ { d } \colon | z | \leq 1 \} , \quad a ( z ) \colon = 1 _ { B } ( z ) , \quad b ( z , w ) \colon = 1 _ { B } ( z - w ) .$$

For a function l : { 0 , 1 } 2 → R , put

$$L _ { \ell } ( z , w ) \colon = \ell ( a ( z ) , b ( z , w ) ) , \quad \| \ell \| _ { \infty } \colon = \max _ { ( \alpha , \beta ) \in \{ 0 , 1 \} ^ { 2 } } | \ell ( \alpha , \beta ) | .$$

If l (0 , 0) = 0, then

In particular, for θ ∈ S d - 1 ,

$$L _ { \ell } ( z , \theta ) \neq 0 \quad \Longrightarrow \quad | z | \leq 2 , \quad | z - \theta | \leq 2 .$$

̸

$$L _ { \ell } ( z , w ) \neq 0 \quad \Longrightarrow \quad z \in B \cup ( w + B ) .$$

̸


<!-- p:17 -->


For χ ∈ C ∞ c ( R d × R d ), we set

$$I _ { r , x , \tau } ^ { \ell , \chi } \colon = \int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { R } ^ { d } } \chi ( z , w ) L _ { \ell } ( z , w ) \left ( c _ { r , x , \tau } ^ { l o c } ( z , w ) - c ( w ) \right ) d w \, d z$$

and

$$J _ { x , \tau } ^ { \ell } \colon = \int _ { S ^ { d - 1 } } \int _ { \mathbb { R } ^ { d } } L _ { \ell } ( z , \theta ) R _ { x , \tau } ( z , \theta , z , \theta ) \, d z \, d \sigma ( \theta ) .$$

Lemma 4.6. Assume d ≥ 2 . Let l : { 0 , 1 } 2 → R satisfy l (0 , 0) = 0 . Let χ ∈ C ∞ c ( R d × R d ) satisfy 0 ≤ χ ≤ 1 and suppose that χ = 1 on a neighborhood of

$$\mathcal { S } _ { * } \colon = \{ ( z , \theta ) \in \mathbb { R } ^ { d } \times S ^ { d - 1 } \colon | z | \leq 2 , \ | z - \theta | \leq 2 \} .$$

Then there exists r χ &gt; 0 such that, for every L &lt; ∞ ,

$$\sup _ { ( x , \tau ) \in \mathcal { J } ( M ) } \frac { 1 } { r ^ { 2 } } \left | I _ { r , x , \tau } ^ { \ell , \chi } - \frac { r ^ { 2 } } { 6 } J _ { x , \tau } ^ { \ell } \right | \longrightarrow 0 \quad ( r \downarrow 0 ) .$$

Moreover,

$$\int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { R } ^ { d } } \chi ( z , w ) | L _ { \ell } ( z , w ) | \left | c _ { r , x , \tau } ^ { \text {loc} } ( z , w ) - c ( w ) \right | \, d w \, d z \leq C _ { \chi } \| \ell \| _ { \infty } r ^ { 2 }$$

for all 0 &lt; r &lt; r χ , uniformly in ( x, τ ) ∈ F ( M ) . For sufficiently small r , both integrals are independent of the choice of χ among cutoffs satisfying the above condition.

Proof. The condition l (0 , 0) = 0 implies that, on | w | = 1, the support of L l lies in S ∗ . We regard S ∗ as a compact subset of R d × R d via S d - 1 ⊂ R d . Since χ = 1 on an open neighborhood of S ∗ , there exists δ χ &gt; 0 such that χ = 1 on the δ χ -neighborhood of S ∗ in R d × R d .

Step 1: shell localization and the cutoff margin. By Lemma 4.5, the difference c loc r,x,τ - c is supported in

$$1 - K _ { 0 } r ^ { 2 } \leq | w | \leq 1 + K _ { 0 } r ^ { 2 } .$$

Write w = ρθ . If L l ( z, w ) = 0, then either | z | ≤ 1 or | z - w | ≤ 1. In the first case ( z, θ ) ∈ S ∗ , and hence

$$\text {dist} _ { \mathbb { R } ^ { 2 d } } \left ( ( z , \rho \theta ) , \mathcal { S } _ { * } \right ) \leq | \rho - 1 | .$$

In the second case, we put z ∗ := z +(1 - ρ ) θ . Then | z ∗ - θ | = | z - w | ≤ 1 and | z ∗ | ≤ 2. Thus ( z ∗ , θ ) ∈ S ∗ . Therefore

$$\text {dist} _ { \mathbb { R } ^ { 2 d } } \left ( ( z , \rho \theta ) , \mathcal { S } _ { * } \right ) & \leq | ( z , \rho \theta ) - ( z _ { * } , \theta ) | \\ & = \sqrt { 2 } \, | \rho - 1 | .$$

$$\text {dist} _ { \mathbb { R } ^ { 2 d } } \left ( ( z , \rho \theta ) , S _ { * } \right ) \leq \sqrt { 2 } \, K _ { 0 } r ^ { 2 } .$$

Thus, in either case,

After decreasing r 0 so that √ 2 K 0 r 2 0 &lt; δ χ , the cutoff is one on every nonzero shell contribution. Step 2: fixed reference traces. Let K be a fixed compact set containing all ( z, θ ) for which ( z, ρθ ) belongs to supp χ and | ρ - 1 | ≤ 2 K 0 r 2 0 . At ρ = 1, the reference discontinuity traces are

$$T _ { 1 } = \{ ( z , \theta ) \colon | z | = 1 \} , \quad T _ { 2 } = T _ { 2 , 1 } = \{ ( z , \theta ) \colon | z - \theta | = 1 \} .$$

For general ρ , the second discontinuity surface is T 2 ,ρ := { ( z, θ ) : | z - ρθ | = 1 } ; thus T 2 is used only as a fixed reference trace. By Lemma 4.4,

$$\ m e a s _ { K } \{ \text {dist} _ { \text {prod} } \left ( ( z , \theta ) , T _ { 1 } \cup T _ { 2 } \right ) < \eta \} \leq C \eta , \quad 0 < \eta < \min \{ 1 , \eta _ { K } \} .$$

Define

̸

$$G _ { \eta } \coloneqq \{ ( z , \theta ) \in K \colon \text {dist} _ { \text {prod} } \left ( ( z , \theta ) , T _ { 1 } \cup T _ { 2 } \right ) \geq \eta \} \, .$$


<!-- p:18 -->


Step 3: constancy on the good set.

For ( z, θ ) ∈ G η , we have

$$\text {dist} _ { \text {prod} } \left ( ( z , \theta ) , T _ { 2 } \right ) \geq \eta .$$

To obtain an upper bound for the same distance, observe that

$$\text {dist} _ { \text {prod} } ( ( z , \theta ) , T _ { 2 } ) \leq | | z - \theta | - 1 | .$$

$$z ^ { \prime } \colon = \theta + \frac { z - \theta } { | z - \theta | } .$$

satisfies

Hence the indicator

uniformly.

Polar Fubini and the uniqueness of this crossing give, for every ( z, θ ) ∈ G η , the exact signed identity

$$\int _ { 0 } ^ { \infty } \chi ( z , \rho \theta ) L _ { \ell } ( z , \rho \theta ) \left ( 1 _ { \{ \Phi _ { r , x } , \tau ( z , \rho \theta ) \leq 1 \} } - 1 _ { \{ \rho \leq 1 \} } \right ) \rho ^ { d - 1 } d \rho \\ = \int _ { 1 } ^ { \rho _ { r , \tau } ( z , \rho \theta ) } \chi ( z , \rho \theta ) L _ { \ell } ( z , \rho \theta ) \rho ^ { d - 1 } d \rho .$$

̸

Indeed, if z = θ , set

Then ( z ′ , θ ) ∈ T 2 , and hence

$$\text {dist} _ { \text {prod} } ( ( z , \theta ) , T _ { 2 } ) & \leq \text {dist} _ { \text {prod} } ( ( z , \theta ) , ( z ^ { \prime } , \theta ) ) \\ & = | z - z ^ { \prime } | \\ & = | | z - \theta | - 1 | .$$

If z = θ , choose any e ∈ S d - 1 and put z ′ = θ + e ; the same inequality follows. Therefore,

$$| | z - \theta | - 1 | \geq \eta .$$

For fixed η &gt; 0, after decreasing r if necessary so that 2 K 0 r 2 ≤ η/ 2, every

$$1 - 2 K _ { 0 } r ^ { 2 } \leq \rho \leq 1 + 2 K _ { 0 } r ^ { 2 }$$

$$| | z - \rho \theta | - 1 | & \geq | | z - \theta | - 1 | - | \rho - 1 | \\ & \geq \eta - 2 K _ { 0 } r ^ { 2 } \geq \frac { \eta } { 2 } .$$

$$b ( z , \rho \theta ) = 1 _ { \{ | z - \rho \theta | \leq 1 \} }$$

does not change as ρ varies over this interval. Since a ( z ) = 1 {| z |≤ 1 } is independent of ρ , it follows that

$$L _ { \ell } ( z , \rho \theta ) = L _ { \ell } ( z , \theta )$$

throughout the enlarged radial interval.

Step 4: the exact signed shell identity. Consider the enlarged radial interval

$$1 - 2 K _ { 0 } r ^ { 2 } \leq \rho \leq 1 + 2 K _ { 0 } r ^ { 2 } .$$

At either endpoint, | ρ - 1 | &gt; K 0 r 2 , so Lemma 4.5 forces agreement of the Euclidean and Riemannian indicators. At the lower endpoint both equal one, and at the upper endpoint both equal zero. Moreover,

$$\partial _ { \rho } \Phi _ { r , x , \tau } ( z , \rho \theta ) = 2 \rho + O ( r ^ { 2 } ) \geq 1$$

throughout the interval for small r . Thus there is exactly one crossing, and Corollary 4.2 gives

$$\rho _ { r , x , \tau } ( z , \theta ) = 1 + \frac { r ^ { 2 } } { 6 } R _ { x , \tau } ( z , \theta , z , \theta ) + O ( r ^ { 3 } )$$


<!-- p:19 -->


The right-hand side is interpreted as a signed integral when ρ r,x,τ &lt; 1. By the cutoff margin from Step 1 and the constancy from Step 3, it equals

$$L _ { \ell } ( z , \theta ) \frac { \rho _ { r , x , \tau } ( z , \theta ) ^ { d } - 1 } { d } = \frac { r ^ { 2 } } { 6 } L _ { \ell } ( z , \theta ) R _ { x , \tau } ( z , \theta , z , \theta ) + O ( \| \ell \| _ { \infty } r ^ { 3 } )$$

uniformly on G η .

Step 5: uniform control of the bad set and the order of limits. Set

$$B _ { \eta } \colon = K \, \bigcup G _ { \eta } .$$

Let E r,x,τ,η denote the contribution from B η to the full shell integral, minus r 2 / 6 times the contribution from B η to the limiting surface integral. The bad-set shell contribution is bounded by C ∥ l ∥ ∞ ηr 2 : the shell has thickness O ( r 2 ) and the bad set has measure O ( η ). Bounded curvature gives the same bound for the omitted part of the limiting surface integral. Consequently, for every L &lt; ∞ ,

$$\lim \sup _ { r \downarrow 0 } \sup _ { ( x , \tau ) \in \mathcal { F } ( M ) \ \| \ell \| _ { \infty } \leq L } r ^ { - 2 } | \mathcal { E } _ { r , x , \tau , \eta } | \leq C L \eta .$$

For fixed η , the good-set calculation based on (4.2) has an integrated remainder O ( Lr 3 ). We first let r ↓ 0 and subsequently let η ↓ 0. This proves the asserted o ( r 2 ) formula uniformly over bounded families of l . Step 1 also shows that, for sufficiently small r , the integral is independent of the admissible cutoff.

Remark 4.7 . The boundary calculation in Lemma 4.6 does not rely on a general transfer principle for discontinuous weights. Such a principle would in general require specifying the appropriate one-sided trace at the moving boundary. In the present graph-induced setting, however,

$$H _ { r , x } ^ { l o c } - H _ { \mathfrak { h } } = L _ { \mathfrak { h } } ( z _ { 1 } , z _ { 1 } - z _ { 2 } ) ( c _ { r , x } ^ { l o c } - c ) ,$$

and the coefficient L h depends only on the two fixed anchor-edge indicators, not on the moving indicator c . Consequently, its discontinuities lie only on fixed trace hypersurfaces. After removing an η -neighborhood of these hypersurfaces, L h is locally constant across the moving shell, so the usual shell calculation applies. The omitted contribution is O ( η ) by Lemma 4.4. Letting first r ↓ 0 and then η ↓ 0 yields the desired boundary formula without any ambiguity concerning one-sided traces.

### 4.2 The boundary-moment identity

We extend h to [0 , 1] 3 by the multilinear polynomial

$$\bar { \mathfrak { h } } ( s _ { 1 } , s _ { 2 } , s _ { 3 } ) \colon = \lambda _ { P } ( s _ { 1 } s _ { 2 } + s _ { 1 } s _ { 3 } + s _ { 2 } s _ { 3 } ) + ( \lambda _ { K } - 3 \lambda _ { P } ) s _ { 1 } s _ { 2 } s _ { 3 } .$$

Thus h is the unique multilinear extension of h , and

$$\bar { \mathfrak { h } } ( a , b , c ) = \mathfrak { h } ( a , b , c ) \quad \text {for } ( a , b , c ) \in \{ 0 , 1 \} ^ { 3 } .$$

We write BV c ( R 2 d ) for the space of functions of bounded variation on R 2 d with compact support. For u ∈ BV c ( R 2 d ) we split the gradient measure as Du = ( D z u, D w u ), so that D w u is the R d -valued Radon measure formed by the last d components of Du . Throughout, H d - 1 denotes the ( d - 1)-dimensional Hausdorff measure on R d ; in particular σ = H d - 1 ⌊ S d - 1 .

Lemma 4.8. Assume d ≥ 2 . Use the displacement coordinates z = z 1 and w = z 1 - z 2 . We set a = 1 {| z |≤ 1 } , b = 1 {| z - w |≤ 1 } , c = 1 {| w |≤ 1 } , and ̂ H h ( z, w ) := h ( a, b, c ) . Then

$$\widehat { H } _ { \mathfrak { h } } \in B V _ { c } ( \mathbb { R } ^ { 2 d } )$$


<!-- p:20 -->


holds. Moreover, for every φ ∈ C 1 c ( R 2 d ; R d ) , we have

$$\int _ { \mathbb { R } ^ { 2 d } } \varphi \cdot d D _ { w } \widehat { H } _ { \mathfrak { h } } & = \int _ { \mathbb { R } ^ { d } } \int _ { \{ | z - w | = 1 \} } \Delta _ { \mathfrak { h } } \mathfrak { h } ( a , c ) \, \varphi ( z , w ) \cdot ( z - w ) \, d \mathcal { H } ^ { d - 1 } ( w ) \, d z \\ & - \int _ { \mathbb { R } ^ { d } } \int _ { S ^ { d - 1 } } \Delta _ { \mathfrak { h } } \mathfrak { h } ( a , b ) \, \varphi ( z , w ) \cdot w \, d \sigma ( w ) \, d z ,$$

where

and

̸

Fix z = 0. As functions of w ,

and Gauss-Green gives

$$D _ { w } b = ( z - w ) \, \mathcal { H } ^ { d - 1 } \lfloor \{ | z - w | = 1 \} , \quad D _ { w } c = - w \, \mathcal { H } ^ { d - 1 } \lfloor S ^ { d - 1 } .$$

Moreover,

$$\mathcal { H } ^ { d - 1 } ( \partial B ( z , 1 ) \cap S ^ { d - 1 } ) = 0 .$$

Hence the BV product rule yields

Since a is constant in w ,

$$D _ { w } \left [ \widehat { H } _ { \mathfrak { h } } ( z , \cdot ) \right ] & = \lambda _ { P } a ( D _ { w } b + D _ { w } c ) + \{ \lambda _ { P } + ( \lambda _ { K } - 3 \lambda _ { P } ) a \} ( c \, D _ { w } b + b \, D _ { w } c ) \\ & = \Delta _ { \mathfrak { h } } ( a , c ) \, D _ { w } b + \Delta _ { c } \mathfrak { h } ( a , b ) \, D _ { w } c .$$

̸

This holds for every z = 0.

Now let φ ∈ C 1 c ( R 2 d ; R d ). By the definition of D w and Fubini,

$$\int _ { \mathbb { R } ^ { 2 d } } \varphi \cdot d D _ { w } \widehat { H } _ { \mathfrak { h } } = \int _ { \mathbb { R } ^ { d } } \left ( \int _ { \mathbb { R } ^ { d } } \varphi ( z , \cdot ) \cdot d D _ { w } [ \widehat { H } _ { \mathfrak { h } } ( z , \cdot ) ] \right ) d z .$$

The exceptional slice z = 0 is dz -null. Substituting the preceding formula and the expressions for D w b, D w c gives (4.3).

Finally, the two measures are concentrated on

$$\Sigma _ { b } = \{ | z - w | = 1 \} , \quad \Sigma _ { c } = \{ | w | = 1 \} .$$

For every z = 0 their intersections in the w -slice are H d - 1 -null; hence

$$\Sigma _ { b } \cap \Sigma _ { c }$$

is null for both measures, so the two measures are mutually singular. Since their sum is D w ̂ H h , which vanishes on R 2 d \ supp ̂ H h , mutual singularity implies that each measure vanishes there separately.

̸

$$\Delta _ { b } \mathfrak { h } ( a , c ) & \colon = \mathfrak { h } ( a , 1 , c ) - \mathfrak { h } ( a , 0 , c ) \\ & = \lambda _ { P } ( a + c ) + ( \lambda _ { K } - 3 \lambda _ { P } ) a c ,$$

$$\Delta _ { c } \mathfrak { h } ( a , b ) & \colon = \mathfrak { h } ( a , b , 1 ) - \mathfrak { h } ( a , b , 0 ) \\ & = \lambda _ { P } ( a + b ) + ( \lambda _ { K } - 3 \lambda _ { P } ) a b .$$

The two measures on the right-hand side of (4.3) are mutually singular; consequently, each of them is supported in supp ̂ H h .

Proof. By the definition of h , ̂ H h = λ P ( ab + ac + bc )+( λ K - 3 λ P ) abc . The functions ab, ac, bc, abc are indicators of bounded convex sets in R 2 d , hence belong to BV c ( R 2 d ). Therefore

$$\widehat { H } _ { \mathfrak { h } } \in B V _ { c } ( \mathbb { R } ^ { 2 d } ) .$$

$$b = 1 _ { B ( z , 1 ) } , \quad c = 1 _ { B ( 0 , 1 ) } ,$$

$$D _ { w } ( b c ) = c \, D _ { w } b + b \, D _ { w } c .$$


<!-- p:21 -->


Note that, by the symmetry of h , ∆ b h = ∆ c h = l h ; the two symbols merely indicate which internal chord is moving.

Proof of Proposition 3.1. Use the displacement coordinates z = z 1 and w = z 1 - z 2 , and let ̂ H h be as in Lemma 4.8. Since ̂ H h ( z, w ) = H h ( z, z - w ), the measure-preserving change of variables ( z 1 , z 2 ) = ( z, z - w ) gives

$$M _ { \mathfrak { h } } ( d ) = \int _ { \mathbb { R } ^ { 2 d } } \widehat { H } _ { \mathfrak { h } } ( z , w ) | z | ^ { 2 } \, d z \, d w .$$

$$V ( z , w ) \colon = | z | ^ { 2 } w - ( z \cdot w ) z .$$

$$d i v _ { w } \, V = d | z | ^ { 2 } - | z | ^ { 2 } = ( d - 1 ) | z | ^ { 2 } .$$

Choose χ ∈ C 1 c ( R 2 d ) such that χ = 1 on a neighborhood of supp ̂ H h . The distributional product rule gives

$$d i v _ { w } ( V \widehat { H } _ { \mathfrak { h } } ) = \widehat { H } _ { \mathfrak { h } } \, d i v _ { w } \, V + V \cdot D _ { w } \widehat { H } _ { \mathfrak { h } } .$$

Testing this identity against χ , and using that ∇ w χ = 0 on supp ̂ H h , we obtain

$$0 = \int _ { \mathbb { R } ^ { 2 d } } \widehat { H } _ { \mathfrak { h } } ( z , w ) \, d i v _ { w } \, V ( z , w ) \, d z \, d w + \int _ { \mathbb { R } ^ { 2 d } } V ( z , w ) \cdot d D _ { w } \widehat { H } _ { \mathfrak { h } } ( z , w ) .$$

Since M h ( d ) = ∫ R 2 d ̂ H h ( z, w ) | z | 2 dz dw , the first term is

$$( d - 1 ) M _ { \mathfrak { h } } ( d ) .$$

We next evaluate the second term using Lemma 4.8. Since the measure D w ̂ H h is supported where χ = 1, we may apply the lemma with φ = χV and obtain

$$\int _ { \mathbb { R } ^ { 2 d } } V \cdot d D _ { w } \widehat { H } _ { \mathfrak { h } } & = \int _ { \mathbb { R } ^ { d } } \int _ { \{ | z - w | = 1 \} } \Delta _ { \mathfrak { h } } ( a , c ) \, V ( z , w ) \cdot ( z - w ) \, d \mathcal { H } ^ { d - 1 } ( w ) \, d z \\ & - \int _ { \mathbb { R } ^ { d } } \int _ { S ^ { d - 1 } } \Delta _ { \mathfrak { h } } ( a , b ) \, V ( z , w ) \cdot w \, d \sigma ( w ) \, d z .$$

Define

$$I _ { b } \colon = \int _ { \mathbb { R } ^ { d } } \int _ { \{ | z - w | = 1 \} } \Delta _ { b } \mathfrak { h } ( a , c ) \, V ( z , w ) \cdot ( z - w ) \, d \mathcal { H } ^ { d - 1 } ( w ) \, d z .$$

On | w | = 1,

and

Define

Then

Consequently,

$$\Delta _ { c } \mathfrak { h } ( a , b ) = \mathfrak { h } ( a , b , 1 ) - \mathfrak { h } ( a , b , 0 ) = L _ { \mathfrak { h } } ( z , w ) ,$$

$$V ( z , w ) \cdot w = | z | ^ { 2 } | w | ^ { 2 } - ( z \cdot w ) ^ { 2 } = | z | ^ { 2 } - ( z \cdot w ) ^ { 2 } .$$

Hence, by the definition of B h ( d ),

$$\int _ { \mathbb { R } ^ { 2 d } } V \cdot d D _ { w } \widehat { H } _ { \mathfrak { h } } = I _ { b } - \mathcal { B } _ { \mathfrak { h } } ( d ) .$$

$$0 = ( d - 1 ) M _ { \mathfrak { h } } ( d ) + I _ { b } - \mathcal { B } _ { \mathfrak { h } } ( d ) .$$

It remains to compute I b . Parameterize the hypersurface {| z - w | = 1 } by

$$u = z - w \in S ^ { d - 1 } , \quad w = z - u .$$


<!-- p:22 -->


Then

$$I _ { b } = \int _ { S ^ { d - 1 } } \int _ { \mathbb { R } ^ { d } } \Delta _ { b } \mathfrak { h } ( a , c ) \, V ( z , z - u ) \cdot u \, d z \, d \sigma ( u ) .$$

Apply the measure-preserving change of variables

$$( z , u ) \mapsto ( z ^ { \prime } , w ^ { \prime } ) = ( - z , - u ) .$$

$$a = 1 _ { \{ | z ^ { \prime } | \leq 1 \} } , \quad c = 1 _ { \{ | z - u | \leq 1 \} } = 1 _ { \{ | z ^ { \prime } - w ^ { \prime } | \leq 1 \} } .$$

$$\Delta _ { b } \mathfrak { h } ( a , c ) & = \mathfrak { h } ( a , 1 , c ) - \mathfrak { h } ( a , 0 , c ) \\ & = \mathfrak { h } ( a , c , 1 ) - \mathfrak { h } ( a , c , 0 ) \\ & = L _ { \mathfrak { h } } ( z ^ { \prime } , w ^ { \prime } ) .$$

Under this change,

By symmetry of h ,

Moreover, since | u | = 1,

$$V ( z , z - u ) \cdot u & = | z | ^ { 2 } ( z - u ) \cdot u - \left ( z \cdot ( z - u ) \right ) ( z \cdot u ) \\ & = | z | ^ { 2 } ( z \cdot u - 1 ) - \left ( | z | ^ { 2 } - z \cdot u \right ) ( z \cdot u ) \\ & = - | z | ^ { 2 } + ( z \cdot u ) ^ { 2 } \\ & = - ( | z ^ { \prime } | ^ { 2 } - ( z ^ { \prime } \cdot w ^ { \prime } ) ^ { 2 } ) .$$

$$I _ { b } = - \mathcal { B } _ { \mathfrak { h } } ( d ) .$$

Substituting this into (4.4) gives 0 = ( d - 1) M h ( d ) - 2 B h ( d ), and hence B h ( d ) = d - 1 2 M h ( d ).

### 4.3 Dependency-graph Poisson approximation and zero-count transfer

We use Theorem 1 of Arratia-Goldstein-Gordon [1]; see also [3]. The following lemma records our total-variation convention and the simplification b 3 = 0 furnished by a dependency graph.

Lemma 4.9. Let I be finite, and let ( ξ i ) i ∈ I be Bernoulli random variables with dependency graph ( I, ∼ ) , meaning that whenever A,B ⊂ I are disjoint and no edge joins a vertex of A to a vertex of B , the families ( ξ i ) i ∈ A and ( ξ j ) j ∈ B are independent. Put

$$p _ { i } = \mathbb { E } \xi _ { i } , \quad W = \sum _ { i \in I } \xi _ { i } , \quad \lambda = \mathbb { E } W ,$$

and let N ( i ) := { i } ∪ { j : j ∼ i } . Define

$$b _ { 1 } \colon = \sum _ { i \in I } \sum _ { j \in N ( i ) } p _ { i } p _ { j } , \quad b _ { 2 } \colon = \sum _ { i \in I } \sum _ { \substack { j \in N ( i ) \\ j \neq i } } \mathbb { E } [ \xi _ { i } \xi _ { j } ] .$$

Therefore

With the convention

$$d _ { \text {TV} } ( \mu , \nu ) \colon = \sup _ { A \subseteq \mathbb { Z } \geq 0 } | \mu ( A ) - \nu ( A ) | ,$$

$$d _ { T V } ( \mathcal { L } ( W ) , \text {Po} ( \lambda ) ) \leq \frac { 1 - e ^ { - \lambda } } { \lambda } ( b _ { 1 } + b _ { 2 } ) \leq ( 1 \wedge \lambda ^ { - 1 } ) ( b _ { 1 } + b _ { 2 } ) ,$$

one has

where the factor is interpreted as 1 when λ = 0 .

The next elementary consequence transfers a Poisson approximation to the zero-count probability. This is the form needed later for the survival event of the degree-two threshold.

̸


<!-- p:23 -->


Lemma 4.10. Let W n be nonnegative integer-valued random variables and put λ n := E W n . Suppose that ( λ n ) is uniformly bounded and that

$$d _ { T V } \left ( \mathcal { L } ( W _ { n } ) , \text {Po} ( \lambda _ { n } ) \right ) \leq C \varepsilon _ { n } .$$

$$\mathbb { P } \{ W _ { n } = 0 \} = e ^ { - \lambda _ { n } } + O ( \varepsilon _ { n } ) .$$

Moreover, suppose that a n ↓ 0 , ε n = o ( a n ) , and λ n = λ 0 + λ 1 a n + o ( a n ) . Then

$$\log \mathbb { P } \{ W _ { n } = 0 \} = - \lambda _ { 0 } - \lambda _ { 1 } a _ { n } + o ( a _ { n } ) .$$

The logarithmic conclusion is uniform on a parameter set K whenever the total-variation bound, the upper bound on λ n , and the expansion of λ n are all uniform on K .

Proof. By the definition of total variation,

$$\left | \mathbb { P } \{ W _ { n } = 0 \} - e ^ { - \lambda _ { n } } \right | \leq C \varepsilon _ { n } .$$

Since ( λ n ) is uniformly bounded, there is c &gt; 0 such that

$$e ^ { - \lambda _ { n } } \geq c$$

$$\mathbb { P } \{ W _ { n } = 0 \} = e ^ { - \lambda _ { n } } \left ( 1 + O ( \varepsilon _ { n } ) \right ) .$$

For the second assertion, ε n = o ( a n ) and a n ↓ 0 imply ε n → 0. Therefore

$$\log \mathbb { P } \{ W _ { n } = 0 \} & = - \lambda _ { n } + \log ( 1 + O ( \varepsilon _ { n } ) ) \\ & = - \lambda _ { n } + O ( \varepsilon _ { n } ) \\ & = - \lambda _ { 0 } - \lambda _ { 1 } a _ { n } + o ( a _ { n } ) .$$

The same argument is uniform on K under the stated uniform assumptions.

## 5 Path-triangle expansion and proof of the k = 2 theorem

### 5.1 Euclidean moment identities

Let

$$L _ { d } ( s ) \colon = 2 \omega _ { d - 1 } \int _ { s / 2 } ^ { 1 } ( 1 - u ^ { 2 } ) ^ { ( d - 1 ) / 2 } \, d u , \quad 0 \leq s \leq 2 ,$$

the volume of the intersection of two Euclidean unit balls whose centers are a distance s apart, and define

$$T _ { 0 } ( d ) \colon = d \omega _ { d } \int _ { 0 } ^ { 1 } s ^ { d - 1 } L _ { d } ( s ) \, d s , \quad T _ { 2 } ( d ) \colon = d \omega _ { d } \int _ { 0 } ^ { 1 } s ^ { d + 1 } L _ { d } ( s ) \, d s . \\$$

For related geometric results on intersections of geodesic balls, see [7]. In this notation,

$$A _ { 2 } ( d ) = \frac { 1 } { 2 } \omega _ { d } ^ { 2 } - \frac { 1 } { 3 } T _ { 0 } ( d ) , \quad C _ { 2 } ( d ) = \frac { 1 } { 4 d } \left ( \frac { 4 d } { d + 2 } \omega _ { d } ^ { 2 } - 2 T _ { 2 } ( d ) \right ) .$$

The positive one-dimensional representation of C 2 ( d ) is proved in Appendix A.

For later use, write

Then

for all n . Hence

$$M _ { 2 } ( d ) \colon = \int _ { ( \mathbb { R } ^ { d } ) ^ { 2 } } H _ { 2 } ( z _ { 1 } , z _ { 2 } ) | z _ { 1 } | ^ { 2 } \, d z _ { 1 } \, d z _ { 2 } .$$

Thus, by the definition of C 2 ( d ),

$$M _ { 2 } ( d ) = 4 d \, C _ { 2 } ( d ) .$$

We now record the tensor identities used in the three-point expansion. They hold for every admissible symmetric three-vertex weight.


<!-- p:24 -->


Lemma 5.1. Let h be an admissible symmetric weight. Then

$$\int _ { ( \mathbb { R } ^ { d } ) ^ { 2 } } H _ { \mathfrak { h } } ( z _ { 1 } , z _ { 2 } ) \, z _ { 1 } \otimes z _ { 1 } \, d z _ { 1 } \, d z _ { 2 } = \frac { M _ { \mathfrak { h } } ( d ) } { d } I _ { d } ,$$

$$\int _ { ( \mathbb { R } ^ { d } ) ^ { 2 } } H _ { \mathfrak { h } } ( z _ { 1 } , z _ { 2 } ) \, z _ { 1 } \otimes z _ { 2 } \, d z _ { 1 } \, d z _ { 2 } = \frac { M _ { \mathfrak { h } } ( d ) } { 2 d } I _ { d } .$$

and

Consequently, for every symmetric bilinear form Q on R d ,

$$\int _ { ( \mathbb { R } ^ { d } ) ^ { 2 } } H _ { \mathfrak { h } } ( z _ { 1 } , z _ { 2 } ) \{ Q ( z _ { 1 } , z _ { 1 } ) + Q ( z _ { 2 } , z _ { 2 } ) \} \, d z _ { 1 } \, d z _ { 2 } = \frac { 2 M _ { \mathfrak { h } } ( d ) } { d } \, \text {tr} \, Q .$$

Proof. Throughout the proof, all unqualified integrals are over ( R d ) 2 with respect to dz 1 dz 2 . The kernel H h is invariant under simultaneous orthogonal transformations and under relabeling of the three points 0 , z 1 , z 2 . In particular, the measure-preserving transformations

$$( z _ { 1 } , z _ { 2 } ) \longmapsto ( z _ { 2 } , z _ { 1 } ) , \quad ( z _ { 1 } , z _ { 2 } ) \longmapsto ( - z _ { 1 } , z _ { 2 } - z _ { 1 } )$$

permute the three edge indicators. Hence

$$\int H _ { \mathfrak { h } } | z _ { 1 } | ^ { 2 } = \int H _ { \mathfrak { h } } | z _ { 2 } | ^ { 2 } = \int H _ { \mathfrak { h } } | z _ { 1 } - z _ { 2 } | ^ { 2 } = M _ { \mathfrak { h } } ( d ) .$$

Since | z 1 - z 2 | 2 = | z 1 | 2 + | z 2 | 2 - 2 z 1 · z 2 , we obtain

$$\int H _ { \mathfrak { h } } z _ { 1 } \cdot z _ { 2 } = \frac { 1 } { 2 } M _ { \mathfrak { h } } ( d ) .$$

$$T _ { 1 1 } \colon = \int H _ { \mathfrak { h } } z _ { 1 } \otimes z _ { 1 } , \quad T _ { 1 2 } \colon = \int H _ { \mathfrak { h } } z _ { 1 } \otimes z _ { 2 } .$$

Set

For every R ∈ O ( d ), simultaneous orthogonal invariance gives

$$H _ { \mathfrak { h } } ( R u _ { 1 } , R u _ { 2 } ) = H _ { \mathfrak { h } } ( u _ { 1 } , u _ { 2 } ) .$$

$$| \det R | = 1 ,$$

so the change of variables

preserves Lebesgue measure. Hence

$$u \, \text { measure.} \, \text { Hence} \\ T _ { 1 1 } & = \int H _ { \mathfrak { h } } ( R u _ { 1 } , R u _ { 2 } ) ( R u _ { 1 } ) \otimes ( R u _ { 1 } ) \, d u _ { 1 } \, d u _ { 2 } \\ & = \int H _ { \mathfrak { h } } ( u _ { 1 } , u _ { 2 } ) ( R u _ { 1 } ) \otimes ( R u _ { 1 } ) \, d u _ { 1 } \, d u _ { 2 } \\ & = R \left ( \int H _ { \mathfrak { h } } ( u _ { 1 } , u _ { 2 } ) u _ { 1 } \otimes u _ { 1 } \, d u _ { 1 } \, d u _ { 2 } \right ) R ^ { \top } \\ & = R T _ { 1 1 } R ^ { T } .$$

$$T _ { 1 2 } & = \int H _ { \mathfrak { h } } ( R u _ { 1 } , R u _ { 2 } ) ( R u _ { 1 } ) \otimes ( R u _ { 2 } ) \, d u _ { 1 } \, d u _ { 2 } \\ & = R \left ( \int H _ { \mathfrak { h } } ( u _ { 1 } , u _ { 2 } ) u _ { 1 } \otimes u _ { 2 } \, d u _ { 1 } \, d u _ { 2 } \right ) R ^ { T } \\ & = R T _ { 1 2 } R ^ { T } .$$

Moreover, since R is orthogonal,

Similarly,

$$( z _ { 1 } , z _ { 2 } ) = ( R u _ { 1 } , R u _ { 2 } )$$


<!-- p:25 -->


Hence both T 11 and T 12 commute with every orthogonal transformation. Therefore there exist α, β ∈ R such that

$$T _ { 1 1 } = \alpha I _ { d } , \quad T _ { 1 2 } = \beta I _ { d } .$$

Taking traces and using

$$t r ( u \otimes v ) = u \cdot v ,$$

we obtain

Thus

$$d \alpha = \int H _ { \mathfrak { h } } | z _ { 1 } | ^ { 2 } = M _ { \mathfrak { h } } ( d ) , \quad d \beta = \int H _ { \mathfrak { h } } z _ { 1 } \cdot z _ { 2 } = \frac { 1 } { 2 } M _ { \mathfrak { h } } ( d ) .$$

$$T _ { 1 1 } = \frac { M _ { \mathfrak { h } } ( d ) } { d } I _ { d } , \quad T _ { 1 2 } = \frac { M _ { \mathfrak { h } } ( d ) } { 2 d } I _ { d } . \\$$

Finally, contracting the first identity with Q gives

$$\int H _ { \mathfrak { h } } Q ( z _ { 1 } , z _ { 1 } ) = \frac { M _ { \mathfrak { h } } ( d ) } { d } \, t r \, Q .$$

By the symmetry under ( z 1 , z 2 ) ↦→ ( z 2 , z 1 ), the same formula holds with z 1 replaced by z 2 . Adding the two identities yields

$$\int H _ { \mathfrak { h } } \{ Q ( z _ { 1 } , z _ { 1 } ) + Q ( z _ { 2 } , z _ { 2 } ) \} = \frac { 2 M _ { \mathfrak { h } } ( d ) } { d } \, t r \, Q .$$

### 5.2 Proof and specializations of the path-triangle expansion

We first prove a stronger anchored form of Theorem 3.2. Its integrated consequence, written in normalized form below, recovers the expansion in that theorem and provides the uniform remainder needed later.

For x ∈ M and 0 &lt; r &lt; r ∗ , define the normalized anchored integral

$$\mathcal { I } _ { \mathfrak { h } } ( r , x ) \coloneqq r ^ { - 2 d } f ( x ) \int _ { M ^ { 2 } } \mathfrak { h } \left ( 1 _ { \{ d _ { g } ( x , y ) \leq r \} } , 1 _ { \{ d _ { g } ( x , z ) \leq r \} } , 1 _ { \{ d _ { g } ( y , z ) \leq r \} } \right ) f ( y ) f ( z ) \, d v o l _ { g } ( y ) \, d v o l _ { g } ( z ) .$$

Proposition 5.2. Assume d ≥ 2 and the standing hypotheses on ( M,g,f ) . There exists r 0 &gt; 0 such that, for every 0 ≤ H &lt; ∞ , there is a nondecreasing function

$$\omega _ { H } \colon [ 0 , r _ { 0 } ] \longrightarrow [ 0 , \infty ) , \quad \omega _ { H } ( s ) \longrightarrow 0 \quad a s \ s \downarrow 0 ,$$

for which

$$\mathcal { I } _ { \mathfrak { h } } ( r , x ) & = J _ { \mathfrak { h } } ( d ) f ( x ) ^ { 3 } \\ & + \frac { M _ { \mathfrak { h } } ( d ) } { d } r ^ { 2 } \left \{ \frac { 1 } { 2 } f ( x ) \| \text { grad } f ( x ) \| _ { g } ^ { 2 } + f ( x ) ^ { 2 } \Delta _ { g } f ( x ) - \frac { 1 } { 4 } f ( x ) ^ { 3 } \text { Scaler} _ { g } ( x ) \right \} + \text {Rem} _ { \mathfrak { h } } ( r , x ) ,$$

where

$$\left | R e m _ { \mathfrak { h } } ( r , x ) \right | \leq r ^ { 2 } \omega _ { H } ( r )$$

for every x ∈ M , every 0 &lt; r ≤ r 0 , and every admissible symmetric weight h satisfying ∥ h ∥ ∞ ≤ H .

Consequently, for every n ≥ 3 , uniformly over such h ,

$$\frac { \mathbb { E } U _ { h } ( r ) } { \binom { n } { 3 } r ^ { 2 d } } & = J _ { h } ( d ) \int _ { M } f ^ { 3 } \, d v o l _ { g } \\ & - \frac { 3 M _ { h } ( d ) } { 2 d } r ^ { 2 } \left \{ \int _ { M } f \| \text { grad } f \| _ { g } ^ { 2 } \, d v o l _ { g } + \frac { 1 } { 6 } \int _ { M } f ^ { 3 } \, S c a l _ { g } \, d v o l _ { g } \right \} + o _ { H } ( r ^ { 2 } ) ,$$

where the remainder is independent of n .


<!-- p:26 -->


Proof. Fix the first labeled point as the anchor x and choose τ ∈ F x . A nonzero h -weight requires at least two of the three possible edges, because h vanishes on configurations with at most one edge. Hence every contributing three-vertex graph is either a path or a triangle and has graph diameter at most two. Since every graph edge has geodesic length at most r , the triangle inequality shows that each of the other two vertices lies in B g ( x, 2 r ).

Choose r 0 &gt; 0 so small that

$$2 r _ { 0 } < \min \{ \iota , \rho _ { c } \} .$$

Then, for 0 &lt; r ≤ r 0 , the other two points of every contributing configuration have unique representations exp x,τ ( rz 1 ) and exp x,τ ( rz 2 ) with | z 1 | ≤ 2 and | z 2 | ≤ 2.

Set

and

$$c _ { r , x , \tau } ^ { l o c } = \mathbf 1 _ { \{ d _ { g } ( \exp _ { x , \tau } ( r z _ { 1 } ) , \exp _ { x , \tau } ( r z _ { 2 } ) ) \leq r \} } , \quad H _ { r , x , \tau } ^ { l o c } = \mathbf h ( a , b , c _ { r , x , \tau } ^ { l o c } ) .$$

The two anchor-edge indicators are exact, since

$$d _ { g } ( x , \exp _ { x , \tau } ( r z _ { i } ) ) = r | z _ { i } | .$$

$$a = 1 _ { \{ | z _ { 1 } | \leq 1 \} } , \quad b = 1 _ { \{ | z _ { 2 } | \leq 1 \} } , \quad c = 1 _ { \{ | z _ { 1 } - z _ { 2 } | \leq 1 \} } ,$$

For a Boolean variable c ,

$$\mathfrak { h } ( a , b , c ) = \mathfrak { h } ( a , b , 0 ) + \left [ \mathfrak { h } ( a , b , 1 ) - \mathfrak { h } ( a , b , 0 ) \right ] c .$$

$$H _ { r , x , \tau } ^ { l o c } - H _ { \mathfrak { h } } & = \widetilde { L } _ { \mathfrak { h } } ( z _ { 1 } , z _ { 2 } ) \left ( c _ { r , x , \tau } ^ { l o c } - c \right ) \\ & = L _ { \mathfrak { h } } ( z _ { 1 } , z _ { 1 } - z _ { 2 } ) \left ( c _ { r , x , \tau } ^ { l o c } - c \right ) .$$

Therefore

The same graph-distance argument gives

̸


$$H _ { \mathfrak { h } } ( z _ { 1 } , z _ { 2 } ) \neq 0 \quad \text {or} \quad H _ { r , x , \tau } ^ { l o c } ( z _ { 1 } , z _ { 2 } ) \neq 0 \quad \Longrightarrow \quad | z _ { 1 } | \leq 2 , \quad | z _ { 2 } | \leq 2 .$$

Moreover,

$$\ell _ { \mathfrak { h } } ( 0 , 0 ) = \mathfrak { h } ( 0 , 0 , 1 ) - \mathfrak { h } ( 0 , 0 , 0 ) = 0 ,$$

so L h satisfies the hypothesis of Lemma 4.6.

Choose an O ( d )-invariant cutoff

$$\chi \in C _ { c } ^ { \infty } ( \mathbb { R } ^ { d } \times \mathbb { R } ^ { d } )$$

that equals one on a neighborhood of

$$\mathcal { K } _ { * } \colon = \{ ( z , w ) \, \colon | z | \leq 2 , \ | z - w | \leq 2 \} .$$

After decreasing r 0 , if necessary, assume

$$r _ { 0 } \leq r _ { \chi } .$$

Thus multiplication by χ ( z 1 , z 1 - z 2 ), followed by extension by zero outside the local normalcoordinate domain, does not change the anchored integral.

Let j x,τ ( v ) denote the normal-coordinate volume density:

$$d v o l _ { g } ( \exp _ { x , \tau } ( v ) ) = j _ { x , \tau } ( v ) \, d v .$$

The change of variables y = exp x,τ ( rz 1 ) and z = exp x,τ ( rz 2 ) gives

$$\mathcal { I } _ { \mathfrak { h } } ( r , x ) = \int _ { ( \mathbb { R } ^ { d } ) ^ { 2 } } \chi ( z _ { 1 } , z _ { 1 } - z _ { 2 } ) H _ { r , x , \tau } ^ { l o c } ( z _ { 1 } , z _ { 2 } ) F _ { r , x , \tau } ( z _ { 1 } , z _ { 2 } ) \, d z _ { 1 } \, d z _ { 2 } ,$$


<!-- p:27 -->


where

$$F _ { r , x , \tau } \coloneqq f ( x ) f ( \exp _ { x , \tau } ( r z _ { 1 } ) ) f ( \exp _ { x , \tau } ( r z _ { 2 } ) ) j _ { x , \tau } ( r z _ { 1 } ) j _ { x , \tau } ( r z _ { 2 } ) .$$

Since χ = 1 on supp H h ,

Hence

$$\mathcal { I } _ { \mathfrak { h } } ( r , x ) & = \int _ { ( \mathbb { R } ^ { d } ) ^ { 2 } } H _ { \mathfrak { h } } ( z _ { 1 } , z _ { 2 } ) F _ { r , x , \tau } ( z _ { 1 } , z _ { 2 } ) \, d z _ { 1 } \, d z _ { 2 } \\ & + \int _ { ( \mathbb { R } ^ { d } ) ^ { 2 } } \chi ( z _ { 1 } , z _ { 1 } - z _ { 2 } ) ( H _ { r , x , \tau } ^ { l o c } ( z _ { 1 } , z _ { 2 } ) - H _ { \mathfrak { h } } ( z _ { 1 } , z _ { 2 } ) ) F _ { r , x , \tau } ( z _ { 1 } , z _ { 2 } ) \, d z _ { 1 } \, d z _ { 2 } .$$

We treat these two terms separately. The first term accounts for the Taylor expansion of the density and the normal-coordinate volume density, while the second is the boundary contribution coming from the curvature-induced displacement of the internal-edge condition.

In the following expansion, all tensors are evaluated at x and pulled back by τ , and we write f = f ( x ). For i = 1 , 2, consider the radial geodesic

$$\gamma _ { i } ( t ) \colon = \exp _ { x , \tau } ( t z _ { i } ) .$$

$$\gamma _ { i } ( 0 ) = x , \quad \dot { \gamma } _ { i } ( 0 ) = \tau z _ { i } , \quad \nabla _ { \dot { \gamma } _ { i } } \dot { \gamma } _ { i } = 0 ,$$

Taylor's formula along γ i gives

$$f ( \exp _ { x , \tau } ( r z _ { i } ) ) = f + r \, d f ( z _ { i } ) + \frac { r ^ { 2 } } { 2 } \nabla ^ { 2 } f ( z _ { i } , z _ { i } ) + O ( r ^ { 3 } ) .$$

Moreover, the normal-coordinate volume density satisfies

$$j _ { x , \tau } ( r z _ { i } ) = 1 - \frac { r ^ { 2 } } { 6 } \, \text {Ric} ( z _ { i } , z _ { i } ) + O ( r ^ { 3 } ) .$$

Hence, uniformly on the fixed compact set involved,

$$f _ { r , x , \tau } = f ^ { 3 } + r f ^ { 2 } \{ d f ( z _ { 1 } ) + d f ( z _ { 2 } ) \} \\ + r ^ { 2 } \left \lceil f \, d f ( z _ { 1 } ) d f ( z _ { 2 } ) + \frac { f ^ { 2 } } { 2 } \{ \nabla ^ { 2 } f ( z _ { 1 } , z _ { 1 } ) + \nabla ^ { 2 } f ( z _ { 2 } , z _ { 2 } ) \} \right \rceil \\ - \frac { f ^ { 3 } } { 6 } \{ R i c ( z _ { 1 } , z _ { 1 } ) + R i c ( z _ { 2 } , z _ { 2 } ) \} \right ] + O ( r ^ { 3 } ) .$$

For the remainder of the proof, unqualified integrals are over ( R d ) 2 with respect to dz 1 dz 2 , and we suppress the argument d in J h ( d ), M h ( d ), and B h ( d ).

The linear term vanishes under

$$( z _ { 1 } , z _ { 2 } ) \longmapsto ( - z _ { 1 } , - z _ { 2 } ) .$$

$$\int H _ { \mathfrak { h } } z _ { 1 } \otimes z _ { 1 } = \frac { M _ { \mathfrak { h } } } { d } I _ { d } , \quad \int H _ { \mathfrak { h } } z _ { 1 } \otimes z _ { 2 } = \frac { M _ { \mathfrak { h } } } { 2 d } I _ { d } .$$

By symmetry, the same first identity holds with z 2 in place of z 1 . Therefore

$$\int H _ { \mathfrak { h } } d f ( z _ { 1 } ) d f ( z _ { 2 } ) = \frac { M _ { \mathfrak { h } } } { 2 d } \| \text { grad } f ( x ) \| _ { g } ^ { 2 } ,$$

Since

By Lemma 5.1,

$$\chi H _ { r , x , \tau } ^ { l o c } = H _ { \mathfrak { h } } + \chi ( H _ { r , x , \tau } ^ { l o c } - H _ { \mathfrak { h } } ) .$$


<!-- p:28 -->


and

Together with

this gives

$$\int H _ { \mathfrak { h } } F _ { r , x , \tau } & = J _ { \mathfrak { h } } f ( x ) ^ { 3 } \\ & + r ^ { 2 } \left \{ \frac { M _ { \mathfrak { h } } } { 2 d } f ( x ) \| \text { grad } f ( x ) \| _ { g } ^ { 2 } + \frac { M _ { \mathfrak { h } } } { d } f ( x ) ^ { 2 } \Delta _ { g } f ( x ) - \frac { M _ { \mathfrak { h } } } { 3 d } f ( x ) ^ { 3 } \text {scal} _ { g } ( x ) \right \} + O _ { H } ( r ^ { 3 } ) .$$

We now turn to the second term in the above decomposition. Using

$$H _ { r , x , \tau } ^ { l o c } - H _ { \mathfrak { h } } = L _ { \mathfrak { h } } ( z _ { 1 } , z _ { 1 } - z _ { 2 } ) \left ( c _ { r , x , \tau } ^ { l o c } - c \right ) ,$$

it is equal to

$$\int _ { ( \mathbb { R } ^ { d } ) ^ { 2 } } \chi ( z _ { 1 } , z _ { 1 } - z _ { 2 } ) L _ { \mathfrak { h } } ( z _ { 1 } , z _ { 1 } - z _ { 2 } ) ( c _ { r , x , \tau } ^ { \text {loc} } - c ) F _ { r , x , \tau } ( z _ { 1 } , z _ { 2 } ) \, d z _ { 1 } \, d z _ { 2 } .$$

On the support of χ ,

$$F _ { r , x , \tau } ( z _ { 1 } , z _ { 2 } ) = f ( x ) ^ { 3 } + O ( r )$$

uniformly in x and τ . On the other hand, the absolute estimate in Lemma 4.6 gives

$$\int _ { ( \mathbb { R } ^ { d } ) ^ { 2 } } \chi ( z _ { 1 } , z _ { 1 } - z _ { 2 } ) | L _ { \mathfrak { h } } ( z _ { 1 } , z _ { 1 } - z _ { 2 } ) | | c _ { r , x , \tau } ^ { l o c } - c | \, d z _ { 1 } \, d z _ { 2 } = O _ { H } ( r ^ { 2 } ) .$$

Hence replacing F r,x,τ by f ( x ) 3 in the boundary term incurs only an O H ( r 3 ) error. Thus

$$\int _ { ( \mathbb { R } ^ { d } ) ^ { 2 } } \chi ( z _ { 1 } , z _ { 1 } - z _ { 2 } ) & ( H ^ { l o c } _ { r , x , \tau } ( z _ { 1 } , z _ { 2 } ) - H _ { \mathfrak { h } } ( z _ { 1 } , z _ { 2 } ) ) F _ { r , x , \tau } ( z _ { 1 } , z _ { 2 } ) \, d z _ { 1 } \, d z _ { 2 } \\ & = f ( x ) ^ { 3 } \int _ { ( \mathbb { R } ^ { d } ) ^ { 2 } } \chi ( z _ { 1 } , z _ { 1 } - z _ { 2 } ) L _ { \mathfrak { h } } ( z _ { 1 } , z _ { 1 } - z _ { 2 } ) ( c _ { r , x , \tau } ^ { l o c } - c ) \, d z _ { 1 } \, d z _ { 2 } + O _ { H } ( r ^ { 3 } ) .$$

Now make the linear change of variables

$$z = z _ { 1 } , \quad w = z _ { 1 } - z _ { 2 } .$$

Its Jacobian has absolute value one. Lemma 4.6 therefore gives

$$\int _ { ( \mathbb { R } ^ { d } ) ^ { 2 } } \chi ( z _ { 1 } , z _ { 1 } - z _ { 2 } ) ( H _ { r , x , \tau } ^ { l o c } ( z _ { 1 } , z _ { 2 } ) - H _ { \mathfrak { h } } ( z _ { 1 } , z _ { 2 } ) ) F _ { r , x , \tau } ( z _ { 1 } , z _ { 2 } ) \, d z _ { 1 } \, d z _ { 2 } \\ = \frac { r ^ { 2 } f ( x ) ^ { 3 } } { 6 } \int _ { S ^ { d - 1 } } \int _ { \mathbb { R } ^ { d } } L _ { \mathfrak { h } } ( z , w ) R _ { x , \tau } ( z , w , z , w ) \, d z \, d \sigma ( w ) + o _ { H } ( r ^ { 2 } ) .$$

By Lemma 4.3,

$$\int _ { S ^ { d - 1 } } \int _ { \mathbb { R } ^ { d } } L _ { \mathfrak { h } } ( z , w ) R _ { x , \tau } ( z , w , z , w ) \, d z \, d \sigma ( w ) = \frac { \mathcal { B } _ { \mathfrak { h } } } { d ( d - 1 ) } \, \text {Scalar} _ { g } ( x ) ,$$

$$=$$

$$\int H _ { \mathfrak { h } } \{ \nabla ^ { 2 } f ( z _ { 1 } , z _ { 1 } ) + \nabla ^ { 2 } f ( z _ { 2 } , z _ { 2 } ) \} & = \frac { 2 M _ { \mathfrak { h } } } { d } \Delta _ { g } f ( x ) , \\ \int H _ { \mathfrak { h } } \{ R i c ( z _ { 1 } , z _ { 1 } ) + R i c ( z _ { 2 } , z _ { 2 } ) \} & = \frac { 2 M _ { \mathfrak { h } } } { d } \, S c a l _ { g } ( x ) . \\ \int H _ { \mathfrak { h } } & = J _ { \mathfrak { h } } ,$$


<!-- p:29 -->


while Proposition 3.1 gives

we obtain

$$\mathcal { I } _ { h } ( r , x ) & = J _ { h } f ( x ) ^ { 3 } \\ & \quad + r ^ { 2 } \left [ \frac { M _ { h } } { 2 d } f ( x ) \| \text { grad } f ( x ) \| _ { g } ^ { 2 } + \frac { M _ { h } } { d } f ( x ) ^ { 2 } \Delta _ { g } f ( x ) - \frac { M _ { h } } { 4 d } f ( x ) ^ { 3 } \text { Scal} _ { g } ( x ) \right ] \\ & \quad + \text {Rem} _ { h } ( r , x ) ,$$

with

Using

together with

$$\mathcal { B } _ { \mathfrak { h } } = \frac { d - 1 } { 2 } M _ { \mathfrak { h } } .$$

Hence the second term in the decomposition, namely the boundary contribution, is

$$\frac { r ^ { 2 } M _ { 0 } } { 1 2 d } f ( x ) ^ { 3 } \, S c a l _ { g } ( x ) + o _ { H } ( r ^ { 2 } ) .$$

Combining the two scalar-curvature contributions,

-

$$- \frac { M _ { \mathfrak { h } } } { 3 d } + \frac { M _ { \mathfrak { h } } } { 1 2 d } = - \frac { M _ { \mathfrak { h } } } { 4 d } ,$$

$$R e m _ { \mathfrak { h } } ( r , x ) = o _ { H } ( r ^ { 2 } )$$

uniformly in x ∈ M and in admissible h satisfying ∥ h ∥ ∞ ≤ H . Indeed, the Taylor remainders above are uniform on the fixed compact coordinate set, the boundary replacement error is O H ( r 3 ), and Lemma 4.6 is uniform for bounded l h . Since

$$\| \ell _ { \mathfrak { h } } \| _ { \infty } \leq 2 \| \mathfrak { h } \| _ { \infty } ,$$

all of these estimates are uniform over ∥ h ∥ ∞ ≤ H .

Define

and, for 0 &lt; s ≤ r 0 ,

$$\omega _ { H } ( 0 ) \colon = 0 ,$$

$$\omega _ { H } ( s ) \colon = \sup _ { 0 < r \leq s } \sup _ { x \in M } \sup _ { \mathfrak { h } \text {admissible} } \frac { | \text {Rem} _ { \mathfrak { h } } ( r , x ) | } { r ^ { 2 } } .$$

Then ω H is nondecreasing,

and

Finally, exchangeability gives

$$\mathbb { E } U _ { \mathfrak { h } } ( r ) = \binom { n } { 3 } r ^ { 2 d } \int _ { M } \mathcal { I } _ { \mathfrak { h } } ( r , x ) \, d v o l _ { g } ( x ) .$$

$$\int _ { M } f ^ { 2 } \Delta _ { g } f \, d v o l _ { g } = - 2 \int _ { M } f \| \, \text {grad} \, f \| _ { g } ^ { 2 } \, d v o l _ { g } ,$$

$$\frac { M _ { \mathfrak { h } } } { 2 d } - \frac { 2 M _ { \mathfrak { h } } } { d } = - \frac { 3 M _ { \mathfrak { h } } } { 2 d } , \quad - \frac { M _ { \mathfrak { h } } } { 4 d } = - \frac { 3 M _ { \mathfrak { h } } } { 2 d } \cdot \frac { 1 } { 6 } ,$$

$$\omega _ { H } ( s ) \longrightarrow 0 \quad \text {as } s \downarrow 0 ,$$

$$| \text {Rem} _ { \mathfrak { h } } ( r , x ) | \leq r ^ { 2 } \omega _ { H } ( r ) .$$

$$=$$


<!-- p:30 -->


yields

$$\frac { \mathbb { E } U _ { \mathfrak { h } } ( r ) } { \binom { n } { 3 } r ^ { 2 d } } = J _ { \mathfrak { h } } \int _ { M } f ^ { 3 } \, d v o l _ { g } \\ - \frac { 3 M _ { \mathfrak { h } } } { 2 d } r ^ { 2 } \left \{ \int _ { M } f \| \text { grad } f \| _ { g } ^ { 2 } \, d v o l _ { g } + \frac { 1 } { 6 } \int _ { M } f ^ { 3 } \, \text {scal} _ { g } \, d v o l _ { g } \right \} + o _ { H } ( r ^ { 2 } ) .$$

Moreover,

and

$$\left | \int _ { M } R e m _ { \mathfrak { h } } ( r , x ) \, d v o l _ { g } ( x ) \right | \leq V o l _ { g } ( M ) r ^ { 2 } \omega _ { H } ( r ) ,$$

so the remainder is independent of n .

Theorem 3.2 follows directly from Proposition 5.2 by taking H ≥ ∥ h ∥ ∞ and integrating the anchored expansion over x ∈ M . The remainder is independent of n , so the conclusion continues to hold along arbitrary integer sequences n = n ( r ) ≥ 3.

Corollary 5.3. The Euclidean moments of the induced-path and triangle kernels are given in Table 1. Applying Theorem 3.2 to these two kernels gives the corresponding expansions for their expected graph counts. Moreover,

$$J _ { P _ { 3 } } ( d ) + J _ { K _ { 3 } } ( d ) = 6 A _ { 2 } ( d ) , \quad M _ { P _ { 3 } } ( d ) + M _ { K _ { 3 } } ( d ) = M _ { 2 } ( d ) .$$

Table 1: Euclidean zeroth and second moments for the induced-path and triangle kernels.

| Kernel   | J G ( d )               | M G ( d )                    |
|----------|-------------------------|------------------------------|
| P 3      | 3 { ω 2 d - T 0 ( d ) } | 4 d d +2 ω 2 d - 3 T 2 ( d ) |
| K 3      | T 0 ( d )               | T 2 ( d )                    |

Proof. For the triangle kernel,

$$J _ { K _ { 3 } } ( d ) = \int _ { ( \mathbb { R } ^ { d } ) ^ { 2 } } a b c \, d z _ { 1 } \, d z _ { 2 } = T _ { 0 } ( d ) ,$$

$$M _ { K _ { 3 } } ( d ) = \int _ { ( \mathbb { R } ^ { d } ) ^ { 2 } } a b c | z _ { 1 } | ^ { 2 } \, d z _ { 1 } \, d z _ { 2 } = T _ { 2 } ( d ) .$$

For the induced-path kernel,

h P 3 = ab (1 - c ) + ac (1 - b ) + bc (1 - a ) = ab + ac + bc - 3 abc.

Since each of the three two-edge regions has volume ω 2 d ,

$$J _ { P _ { 3 } } ( d ) = 3 \omega _ { d } ^ { 2 } - 3 T _ { 0 } ( d ) .$$

For the second moment,

$$\int _ { ( \mathbb { R } ^ { d } ) ^ { 2 } } a b | z _ { 1 } | ^ { 2 } \, d z _ { 1 } \, d z _ { 2 } = \int _ { ( \mathbb { R } ^ { d } ) ^ { 2 } } a c | z _ { 1 } | ^ { 2 } \, d z _ { 1 } \, d z _ { 2 } = \frac { d } { d + 2 } \omega _ { d } ^ { 2 } .$$

For the remaining term, the change of variables u = z 2 and v = z 1 - z 2 gives

$$\int _ { ( \mathbb { R } ^ { d } ) ^ { 2 } } b c | z _ { 1 } | ^ { 2 } \, d z _ { 1 } \, d z _ { 2 } & = \int _ { B ( 0 , 1 ) ^ { 2 } } | u + v | ^ { 2 } \, d u \, d v \\ & = \frac { 2 d } { d + 2 } \omega _ { d } ^ { 2 } ,$$


<!-- p:31 -->


where the mixed term vanishes by symmetry. Hence

$$M _ { P _ { 3 } } ( d ) = \frac { 4 d } { d + 2 } \omega _ { d } ^ { 2 } - 3 T _ { 2 } ( d ) .$$

$$\mathfrak { h } _ { 2 } = \mathfrak { h } _ { P _ { 3 } } + \mathfrak { h } _ { K _ { 3 } } ,$$

so additivity of the Euclidean moments gives

$$J _ { P _ { 3 } } ( d ) + J _ { K _ { 3 } } ( d ) = J _ { \mathfrak { h } _ { 2 } } ( d ) = 6 A _ { 2 } ( d ) ,$$

$$M _ { P _ { 3 } } ( d ) + M _ { K _ { 3 } } ( d ) = M _ { \mathfrak { h } _ { 2 } } ( d ) = M _ { 2 } ( d ) .$$

Lemma 5.4. For every d ≥ 2 ,

$$D _ { d } > 0 , \quad \gamma _ { d } > 0 .$$

Proof. By Table 1,

$$D _ { d } = \frac { \omega _ { d } ^ { 2 } } { 3 \{ \omega _ { d } ^ { 2 } - T _ { 0 } ( d ) \} T _ { 0 } ( d ) } \left \{ \frac { 4 d } { d + 2 } T _ { 0 } ( d ) - 3 T _ { 2 } ( d ) \right \} .$$

The denominator is positive because both the triangle and induced-path regions have positive Euclidean measure. Let μ d be the probability measure on [0 , 1] given by

$$\mu _ { d } ( d s ) \colon = d s ^ { d - 1 } \, d s .$$

Since s ↦→ s 2 is strictly increasing and s ↦→ L d ( s ) is strictly decreasing, Chebyshev's integral inequality for oppositely ordered functions gives

$$\frac { T _ { 2 } ( d ) } { T _ { 0 } ( d ) } = \frac { \int _ { 0 } ^ { 1 } s ^ { 2 } L _ { d } ( s ) \, d \mu _ { d } ( s ) } { \int _ { 0 } ^ { 1 } L _ { d } ( s ) \, d \mu _ { d } ( s ) } < \int _ { 0 } ^ { 1 } s ^ { 2 } \, d \mu _ { d } ( s ) = \frac { d } { d + 2 } .$$

Consequently,

$$\frac { 4 d } { d + 2 } T _ { 0 } ( d ) - 3 T _ { 2 } ( d ) > \frac { d } { d + 2 } T _ { 0 } ( d ) > 0 ,$$

and the assertion follows.

For α ∈ ( [ n ] 3 ) and r ≥ 0, let

$$\eta _ { \alpha } ( r ) \colon = 1 _ { \{ \Delta ( G _ { n } ( r ) [ \alpha ] ) \geq 2 \} } , \quad N _ { 2 } ( r ) \colon = \sum _ { \alpha \in \left ( \begin{matrix} n \\ 3 \end{matrix} \right ) } \eta _ { \alpha } ( r ) ,$$

where G n ( r )[ α ] is the graph induced by the vertices indexed by α . Then

$$\{ S _ { 2 , n } > r \} = \{ N _ { 2 } ( r ) = 0 \} .$$

Finally,

and

Corollary 5.5. As r ↓ 0 ,

$$\mathbb { E } N _ { 2 } ( r ) & = \begin{pmatrix} n \\ 3 \end{pmatrix} r ^ { 2 d } \left [ 6 A _ { 2 } ( d ) \int _ { M } f ^ { 3 } \, d v o l _ { g } \\ & - 6 C _ { 2 } ( d ) r ^ { 2 } \left \{ \int _ { M } f \| \text { grad } f \| _ { g } ^ { 2 } \, d v o l _ { g } + \frac { 1 } { 6 } \int _ { M } f ^ { 3 } \, \text { Scalar} _ { g } \, d v o l _ { g } \right \} + o ( r ^ { 2 } ) \right ] .$$


<!-- p:32 -->


Equivalently,

$$\mathbb { E } N _ { 2 } ( r ) & = n ^ { 3 } r ^ { 2 d } \left [ A _ { 2 } ( d ) \int _ { M } f ^ { 3 } \, d v o l _ { g } \\ & - C _ { 2 } ( d ) r ^ { 2 } \left \{ \int _ { M } f \| \text {grad} \, f \| _ { g } ^ { 2 } \, d v o l _ { g } + \frac { 1 } { 6 } \int _ { M } f ^ { 3 } \, S c a l _ { g } \, d v o l _ { g } \right \} + o ( r ^ { 2 } ) \right ] \\ & + O ( n ^ { 2 } r ^ { 2 d } ) .$$

Proof. Since h 2 = h P 3 + h K 3 , Corollary 5.3 gives

$$J _ { \mathfrak { h } _ { 2 } } ( d ) = 6 A _ { 2 } ( d ) , \quad M _ { \mathfrak { h } _ { 2 } } ( d ) = M _ { 2 } ( d ) = 4 d C _ { 2 } ( d ) .$$

Applying Theorem 3.2 to h 2 ( a, b, c ) = 1 { a + b + c ≥ 2 } gives the first formula. The second follows from ( n 3 ) = n 3 6 + O ( n 2 ).

### 5.3 Poisson approximation

Let I n := ( [ n ] 3 ) be the family of all three-element subsets of [ n ]. For α = { i, j, k } ∈ I n , recall that

$$\eta _ { \alpha } ( r ) \colon = 1 _ { \{ \Delta ( G _ { n } ( r ) [ \alpha ] ) \geq 2 \} } ,$$

where G n ( r )[ α ] is the subgraph of G n ( r ) induced by the vertices indexed by α . Thus

$$\eta _ { \alpha } ( r ) = 1$$

if and only if their induced graph is either a path P 3 or a triangle K 3 . In particular,

$$N _ { 2 } ( r ) = \sum _ { \alpha \in \mathcal { I } _ { n } } \eta _ { \alpha } ( r ) .$$

To obtain a Poisson approximation for N 2 ( r ), we need to control the dependence between two active-triple indicators η α ( r ) and η β ( r ). If α ∩ β = ∅ , the two indicators depend on disjoint sets of sample points and hence are independent. Thus only the cases

$$| \alpha \cap \beta | = 1 \quad \text { and } \quad | \alpha \cap \beta | = 2$$

require estimates. The following lemma provides the needed overlap bounds.

Lemma 5.6. There exists C &lt; ∞ such that, for all sufficiently small r and all α, β ∈ I n ,

$$\mathbb { P } ( \eta _ { \alpha } ( r ) = 1 ) \leq C r ^ { 2 d } ,$$

$$\mathbb { P } ( \eta _ { \alpha } ( r ) \eta _ { \beta } ( r ) = 1 ) \leq C r ^ { 4 d } \quad ( | \alpha \cap \beta | = 1 ) ,$$

$$\mathbb { P } ( \eta _ { \alpha } ( r ) \eta _ { \beta } ( r ) = 1 ) \leq C r ^ { 3 d } \quad ( | \alpha \cap \beta | = 2 ) .$$

Proof. Since M is compact and f is bounded, there is a constant C such that

$$\mathbb { P } \{ X _ { j } \in B _ { g } ( y , 2 r ) \} \leq C r ^ { d }$$

and

uniformly in y ∈ M and small r .

For one active triple, at least one vertex has degree two. Taking a union over the at most three possible choices of this center, fix one such choice and condition on the location y of the center. The two remaining points must both lie in B g ( y, r ). Since they are conditionally independent, P { both remaining points lie in B g ( y, r ) | y } ≤ Cr 2 d .


<!-- p:33 -->


After summing over the at most three possible centers and enlarging C , we obtain

$$\mathbb { P } ( \eta _ { \alpha } ( r ) = 1 ) \leq C r ^ { 2 d } .$$

Suppose | α ∩ β | = 1, and condition on the common vertex X i . If both triples are active, each induced three-vertex graph is connected and has graph diameter at most two. Hence each of the four non-common vertices is within geodesic distance at most 2 r of X i . Thus all four non-common vertices lie in B g ( X i , 2 r ). Conditioning on X i and using their conditional independence gives

$$\mathbb { P } ( \eta _ { \alpha } ( r ) \eta _ { \beta } ( r ) = 1 ) \leq C r ^ { 4 d } .$$

Suppose | α ∩ β | = 2, and condition on one of the shared vertices. If both triples are active, each induced three-vertex graph is connected and has graph diameter at most two. Hence the other shared vertex and the two non-shared vertices are all within geodesic distance at most 2 r of the chosen shared vertex. Conditioning on that vertex and using the independence of the other three points gives

$$\mathbb { P } ( \eta _ { \alpha } ( r ) \eta _ { \beta } ( r ) = 1 ) \leq C r ^ { 3 d } .$$

Proposition 5.7. For every fixed T &lt; ∞ , setting r 2 ,n ( t ) = tn - 3 / (2 d ) , one has, as n →∞ ,

$$d _ { T V } \left ( \mathcal { L } ( N _ { 2 } ( r _ { 2 , n } ( t ) ) ) , \text {Po} ( \mathbb { E } N _ { 2 } ( r _ { 2 , n } ( t ) ) ) \right ) = O ( n ^ { - 1 / 2 } )$$

uniformly for 0 ≤ t ≤ T .

Proof. Let I n := ( [ n ] 3 ) and use the indicators η α ( r ) defined in Section 3. Use the dependency graph in which α and β are adjacent iff α ∩ β = ∅ and α = β . Since η α ( r ) depends only on ( X i ) i ∈ α , disjoint triples give independent indicators. Hence this is a dependency graph. Lemma 4.9 gives

̸


$$d _ { T V } \left ( \mathcal { L } ( N _ { 2 } ( r ) ) , P o ( \mathbb { E } N _ { 2 } ( r ) ) \right ) \leq C \left ( \sum _ { \alpha } \sum _ { \beta \sim \alpha } \mathbb { E } [ \eta _ { \alpha } \eta _ { \beta } ] + \sum _ { \alpha } \sum _ { \beta \in N ( \alpha ) } \mathbb { E } \eta _ { \alpha } \mathbb { E } \eta _ { \beta } \right ) .$$

There are O ( n 5 ) ordered pairs of triples sharing exactly one vertex and O ( n 4 ) ordered pairs sharing exactly two vertices. By Lemma 5.6,

$$\sum _ { \alpha } \sum _ { \beta \sim \alpha } \mathbb { E } [ \eta _ { \alpha } \eta _ { \beta } ] \leq C ( n ^ { 5 } r ^ { 4 d } + n ^ { 4 } r ^ { 3 d } ) .$$

For the product-of-marginals term, separate the self term from the neighboring term. Since |I n | = O ( n 3 ) and E η α ≤ Cr 2 d ,

$$\sum _ { \alpha } ( \mathbb { E } \eta _ { \alpha } ) ^ { 2 } \leq C n ^ { 3 } r ^ { 4 d } .$$

̸

The number of ordered neighboring pairs with α = β is O ( n 5 ), and therefore

̸

$$\sum _ { \alpha } \sum _ { \substack { \beta \in N ( \alpha ) \\ b e t a \neq \alpha } } \mathbb { E } \eta _ { \alpha } \, \mathbb { E } \eta _ { \beta } \leq C n ^ { 5 } r ^ { 4 d } .$$

Thus the full product-of-marginals term is bounded by C ( n 3 r 4 d + n 5 r 4 d ), which is O ( n 5 r 4 d ) when r = tn - 3 / (2 d ) with t ∈ [0 , T ]. Therefore

$$d _ { T V } ( \mathcal { L } ( N _ { 2 } ( r ) ) , \text {Po} ( \mathbb { E } N _ { 2 } ( r ) ) ) \leq C ( n ^ { 4 } r ^ { 3 d } + n ^ { 5 } r ^ { 4 d } ) .$$


<!-- p:34 -->


For r = r 2 ,n ( t ) = tn - 3 / (2 d ) and 0 ≤ t ≤ T , we have

$$n ^ { 4 } r ^ { 3 d } + n ^ { 5 } r ^ { 4 d } = t ^ { 3 d } n ^ { - 1 / 2 } + t ^ { 4 d } n ^ { - 1 } = O _ { T } ( n ^ { - 1 / 2 } ) .$$

Proposition 5.8. Under the standing assumptions, assume d &gt; 6 , and set

$$r _ { 2 , n } ( t ) \colon = t n ^ { - 3 / ( 2 d ) } .$$

Then, as n →∞ , for every T &lt; ∞ , uniformly for 0 ≤ t ≤ T ,

$$\log \mathbb { P } \{ N _ { 2 } ( r _ { 2 , n } ( t ) ) = 0 \} & = - \ A _ { 2 } ( d ) t ^ { 2 d } \int _ { M } f ^ { 3 } \, d v \log \\ & + C _ { 2 } ( d ) t ^ { 2 d + 2 } n ^ { - 3 / d } \left \{ \int _ { M } f \| \text { grad } f \| _ { g } ^ { 2 } \, d v \log _ { g } + \frac { 1 } { 6 } \int _ { M } f ^ { 3 } \, S c a l _ { g } \, d v o l _ { g } \right \} \\ & + o ( n ^ { - 3 / d } ) .$$

Proof. We combine Corollary 5.5, Proposition 5.7, and Lemma 4.10.

For the active-triple weight h 2 , let ω := ω 1 be the nondecreasing modulus supplied by Proposition 5.2. Since ∥ h 2 ∥ ∞ = 1,

$$\sup _ { 0 \leq t \leq T } t ^ { 2 d + 2 } \omega ( t n ^ { - 3 / ( 2 d ) } ) \leq T ^ { 2 d + 2 } \omega ( T n ^ { - 3 / ( 2 d ) } ) \longrightarrow 0 .$$

Thus the remainder in Corollary 5.5 is uniform for 0 ≤ t ≤ T .

Substituting r = r 2 ,n ( t ) = tn - 3 / (2 d ) into Corollary 5.5 gives

$$\mathbb { E } N _ { 2 } ( r _ { 2 , n } ( t ) ) & = A _ { 2 } ( d ) t ^ { 2 d } \int _ { M } f ^ { 3 } \, d v \text {ol} _ { g } \\ & - C _ { 2 } ( d ) t ^ { 2 d + 2 } n ^ { - 3 / d } \left \{ \int _ { M } f \| \text { grad } f \| _ { g } ^ { 2 } \, d v \text {ol} _ { g } + \frac { 1 } { 6 } \int _ { M } f ^ { 3 } \, \text {scal} _ { g } \, d v \text {ol} _ { g } \right \} \\ & + o ( n ^ { - 3 / d } ) + O _ { T } ( n ^ { - 1 } ) ,$$

uniformly for 0 ≤ t ≤ T . Here the O T ( n - 1 ) term is the finite-size correction arising from

$$\left ( \begin{matrix} n \\ 3 \end{matrix} \right ) = \frac { n ^ { 3 } } { 6 } + O ( n ^ { 2 } ) .$$

Since d &gt; 6, we have n - 1 = o ( n - 3 /d ) and n - 1 / 2 = o ( n - 3 /d ). Thus O T ( n - 1 ) term may be absorbed into the o ( n - 3 /d ) remainder.

For convenience, define

and

Then

$$\lambda _ { 0 } ( t ) \colon = A _ { 2 } ( d ) t ^ { 2 d } \int _ { M } f ^ { 3 } \, d v o l _ { g }$$

$$\lambda _ { 1 } ( t ) \colon = - C _ { 2 } ( d ) t ^ { 2 d + 2 } \left \{ \int _ { M } f \| \text {grad} \, f \| _ { g } ^ { 2 } \, d \text {vol} _ { g } + \frac { 1 } { 6 } \int _ { M } f ^ { 3 } \, \text {Scalar} _ { g } \, d \text {vol} _ { g } \right \} .$$

$$\sup _ { 0 \leq t \leq T } \left | \mathbb { E } N _ { 2 } ( r _ { 2 , n } ( t ) ) - \lambda _ { 0 } ( t ) - \lambda _ { 1 } ( t ) n ^ { - 3 / d } \right | = o ( n ^ { - 3 / d } ) .$$

On the other hand, Proposition 5.7 gives

$$\sup _ { 0 \leq t \leq T } d _ { T V } ( \mathcal { L } ( N _ { 2 } ( r _ { 2 , n } ( t ) ) ) , \text {Po} ( \mathbb { E } N _ { 2 } ( r _ { 2 , n } ( t ) ) ) ) = O ( n ^ { - 1 / 2 } ) = o ( n ^ { - 3 / d } ) .$$


<!-- p:35 -->


The expectation expansion also shows that

$$\sup _ { n } \sup _ { 0 \leq t \leq T } \mathbb { E } N _ { 2 } ( r _ { 2 , n } ( t ) ) < \infty .$$

Hence Lemma 4.10 applies uniformly on [0 , T ]. For 0 &lt; t ≤ T , it follows that

$$\log \mathbb { P } \{ N _ { 2 } ( r _ { 2 , n } ( t ) ) = 0 \} = - \lambda _ { 0 } ( t ) - \lambda _ { 1 } ( t ) n ^ { - 3 / d } + o ( n ^ { - 3 / d } ) .$$

Substituting the definitions of λ 0 and λ 1 gives

$$\log \mathbb { P } \{ N _ { 2 } ( r _ { 2 , n } ( t ) ) = 0 \} & = - \ A _ { 2 } ( d ) t ^ { 2 d } \int _ { M } f ^ { 3 } \, d v o l _ { g } \\ & + C _ { 2 } ( d ) t ^ { 2 d + 2 } n ^ { - 3 / } \left \{ \int _ { M } f \| \text { grad } f \| _ { g } ^ { 2 } \, d v o l _ { g } + \frac { 1 } { 6 } \int _ { M } f ^ { 3 } \, S c a l _ { g } \, d v o l _ { g } \right \} \\ & + o ( n ^ { - 3 / } ) .$$

The remainder is uniform for 0 &lt; t ≤ T . At t = 0,

$$r _ { 2 , n } ( 0 ) = 0$$

and N 2 (0) = 0 almost surely under the continuous sampling law, so

$$\log \mathbb { P } \{ N _ { 2 } ( 0 ) = 0 \} = 0 .$$

The displayed expansion is therefore exact at t = 0 as well. This proves the assertion uniformly on [0 , T ].

Theorem 3.8 now follows immediately from Proposition 5.8 and the identity

$$\{ S _ { 2 , n } > r \} = \{ N _ { 2 } ( r ) = 0 \} .$$

## 6 Statistical estimation from path-triangle contrasts

This section proves Theorems 3.4 and 3.5, and Corollary 3.7. For each n , we use the exact Hoeffding decomposition of the order-three U -statistic with radius r n ; see, for example, [20, Chapter 5]. The point specific to the present problem is that the normalization J - 1 P 3 versus J - 1 K 3 cancels the leading one-point projection.

### 6.1 Overlap bounds

For a fixed admissible weight h , write

$$\xi _ { \alpha } = \xi _ { \alpha , \mathfrak { h } } ( r ) , \quad U = U _ { \mathfrak { h } } ( r ) .$$

Writing ξ h ,r ( x, y, z ) for the corresponding symmetric three-point kernel, define

$$m _ { \natural , r } ( x ) & \colon = \mathbb { E } \left [ \xi _ { \{ 1 , 2 , 3 \} , \mathfrak { h } } ( r ) \, | \, X _ { 1 } = x \right ] \\ & = \int _ { M } \int _ { M } \xi _ { \natural , r } ( x , y , z ) f ( y ) f ( z ) \, d v o l _ { g } ( y ) \, d v o l _ { g } ( z ) .$$

$$\theta _ { \mathfrak { h } , r } \colon = \mathbb { E } \xi _ { \{ 1 , 2 , 3 \} , \mathfrak { h } } ( r ) ,$$

and let h 1 ,r , h 2 ,r , and h 3 ,r denote the canonical Hoeffding projections of the symmetric three-point kernel. Explicitly,

$$h _ { 1 , r } ( x ) = m _ { \mathfrak { h } , r } ( x ) - \theta _ { \mathfrak { h } , r } ,$$

Let and, writing We write


<!-- p:36 -->


$$R _ { \mathfrak { h } , n } ( r ) \coloneqq ( n - 2 ) \sum _ { 1 \leq i < j \leq n } h _ { 2 , r } ( X _ { i } , X _ { j } ) + \sum _ { 1 \leq i < j < k \leq n } h _ { 3 , r } ( X _ { i } , X _ { j } , X _ { k } )$$

for the remainder after removing the first Hoeffding projection. The canonical components are mutually orthogonal in L 2 .

For random variables Y and Z , we use the conventions

$$\text {Var} ( Y ) \colon = \mathbb { E } \left [ ( Y - \mathbb { E } Y ) ^ { 2 } \right ] = \mathbb { E } [ Y ^ { 2 } ] - ( \mathbb { E } Y ) ^ { 2 }$$

and

$$C o v ( Y , Z ) \colon = \mathbb { E } [ ( Y - \mathbb { E } Y ) ( Z - \mathbb { E } Z ) ] = \mathbb { E } [ Y Z ] - \mathbb { E } [ Y ] \mathbb { E } [ Z ] .$$

In particular, since

we have

$$g _ { 2 , r } ( x , y ) & \colon = \mathbb { E } [ \xi _ { \{ 1 , 2 , 3 \} , r } ( r ) \ | \ X _ { 1 } = x , X _ { 2 } = y ] , \\ h _ { 2 , r } ( x , y ) & = g _ { 2 , r } ( x , y ) - \theta _ { \mathfrak { h } , r } - h _ { 1 , r } ( x ) - h _ { 1 , r } ( y ) .$$

The third projection is defined by

$$h _ { 3 , r } ( x , y , z ) & = \xi _ { \mathfrak { h } , r } ( x , y , z ) - \theta _ { \mathfrak { h } , r } \\ & - h _ { 1 , r } ( x ) - h _ { 1 , r } ( y ) - h _ { 1 , r } ( z ) \\ & - h _ { 2 , r } ( x , y ) - h _ { 2 , r } ( x , z ) - h _ { 2 , r } ( y , z ) .$$

$$U = \sum _ { \alpha \in \left ( \begin{matrix} [ n ] \\ 3 \end{matrix} \right ) } \xi _ { \alpha } ,$$

$$\text {Var} \, U = \sum _ { \alpha , \beta \in \left ( \begin{smallmatrix} n \\ 3 \end{smallmatrix} \right ) } \text {Cov} ( \xi _ { \alpha } , \xi _ { \beta } ) .$$

The following lemma bounds these covariance contributions according to the overlap size | α ∩ β | .

Lemma 6.1. For each fixed admissible h , there are C &lt; ∞ and r 0 &gt; 0 such that, for n ≥ 3 and 0 &lt; r &lt; r 0 ,

$$\text {Var} \, U _ { \mathfrak { h } } ( r ) \leq C \left ( n ^ { 3 } r ^ { 2 d } + n ^ { 4 } r ^ { 3 d } + n ^ { 5 } r ^ { 4 d } \right ) .$$

If J h ( d ) = 0 , then the last term improves to

$$\text {Var} \, U _ { \mathfrak { h } } ( r ) \leq C \left ( n ^ { 3 } r ^ { 2 d } + n ^ { 4 } r ^ { 3 d } + n ^ { 5 } r ^ { 4 d + 4 } \right ) .$$

Moreover, after removing the first Hoeffding projection, the remainder R h ,n ( r ) satisfies

$$\text {Var} \, R _ { \mathfrak { h } , n } ( r ) \leq C \left ( n ^ { 3 } r ^ { 2 d } + n ^ { 4 } r ^ { 3 d } \right ) .$$

Proof. Since U = ∑ α ∈ ( [ n ] 3 ) ξ α , we have

$$\text {Var} \, U = \sum _ { \alpha , \beta \in ( \real ^ { [ n ] } _ { 3 } ) } \text {Cov} ( \xi _ { \alpha } , \xi _ { \beta } ) .$$

We bound the summands according to the overlap size | α ∩ β | . Since h is fixed, the corresponding kernel is uniformly bounded. We also use throughout the uniform small-ball estimate

$$\sup _ { x \in M } \mathbb { P } \{ X _ { 1 } \in B _ { g } ( x , c r ) \} = O ( r ^ { d } )$$


<!-- p:37 -->


for each fixed c &gt; 0.

If α ∩ β = ∅ , then ξ α and ξ β are independent, and hence their covariance is zero.

̸

Suppose first that α = β . By connected support, after choosing one of the three sample points as an anchor, the other two lie in its geodesic 2 r -ball whenever ξ α = 0. Hence

̸

$$\mathbb { P } \{ \xi _ { \alpha } \neq 0 \} = O ( r ^ { 2 d } ) ,$$

and boundedness of the kernel gives

$$V a r ( \xi _ { \alpha } ) \leq \mathbb { E } \xi _ { \alpha } ^ { 2 } = O ( r ^ { 2 d } ) .$$

There are ( n 3 ) = O ( n 3 ) such pairs.

Suppose next that | α ∩ β | = 2. If both kernel values are nonzero, the two shared points are at distance at most 2 r , and, conditional on the shared points, each of the two remaining points lies in a union of a bounded number of geodesic balls of radius 2 r . Therefore

$$\mathbb { E } | \xi _ { \alpha } \xi _ { \beta } | = O ( r ^ { 3 d } ) .$$

Moreover, the preceding one-kernel support bound gives E | ξ α | = O ( r 2 d ), and hence

$$| \, C o v ( \xi _ { \alpha } , \xi _ { \beta } ) | & \leq \mathbb { E } | \xi _ { \alpha } \xi _ { \beta } | + | \mathbb { E } \xi _ { \alpha } | \, | \mathbb { E } \xi _ { \beta } | \\ & = O ( r ^ { 3 d } ) .$$

There are O ( n 4 ) ordered pairs of this type.

If | α ∩ β | = 1, relabel the common sample point as X 1 . Conditional on X 1 , the two kernel values are independent, so

$$\mathbb { E } [ \xi _ { \alpha } \xi _ { \beta } \, | \, X _ { 1 } ] = \mathbb { E } [ \xi _ { \alpha } \, | \, X _ { 1 } ] \mathbb { E } [ \xi _ { \beta } \, | \, X _ { 1 } ] = m _ { \mathfrak { h } , r } ( X _ { 1 } ) ^ { 2 } .$$

$$C o v ( \xi _ { \alpha } , \xi _ { \beta } ) = V a r ( m _ { \mathfrak { h } , r } ( X _ { 1 } ) ) .$$

By definition of the normalized anchored integral,

$$m _ { \mathfrak { h } , r } ( x ) = \frac { r ^ { 2 d } } { f ( x ) } \mathcal { I } _ { \mathfrak { h } } ( r , x ) .$$

Since f is bounded below away from zero, the anchored expansion in Proposition 5.2 yields, uniformly in x ,

$$m _ { \mathfrak { h } , r } ( x ) = O ( r ^ { 2 d } ) , \quad \ V a r ( m _ { \mathfrak { h } , r } ( X _ { 1 } ) ) = O ( r ^ { 4 d } ) .$$

There are O ( n 5 ) ordered pairs sharing one index. Combining the four overlap cases proves (6.1). If J h ( d ) = 0, the leading anchored term vanishes and the same expansion gives

$$\sup _ { x \in M } | m _ { \mathfrak { h } , r } ( x ) | = O ( r ^ { 2 d + 2 } ) , \quad \text {Var} ( m _ { \mathfrak { h } , r } ( X _ { 1 } ) ) = O ( r ^ { 4 d + 4 } ) ,$$

which proves (6.2).

Set

$$R _ { \delta , n } ( r ) = ( n - 2 ) \sum _ { 1 \leq i < j \leq n } h _ { 2 , r } ( X _ { i } , X _ { j } ) + \sum _ { 1 \leq i < j < k \leq n } h _ { 3 , r } ( X _ { i } , X _ { j } , X _ { k } ) ,$$

and the two canonical sums are orthogonal.

Let

Consequently,

$$g _ { 2 , r } ( x , y ) \colon = \mathbb { E } [ \xi _ { \{ 1 , 2 , 3 \} , r } ( r ) \ | \ X _ { 1 } = x , X _ { 2 } = y ] .$$

The projection property gives

$$\mathbb { E } h _ { 2 , r } ( X _ { 1 } , X _ { 2 } ) ^ { 2 } \leq \mathbb { E } g _ { 2 , r } ( X _ { 1 } , X _ { 2 } ) ^ { 2 } .$$


<!-- p:38 -->


By connected support, g 2 ,r ( x, y ) = 0 when d g ( x, y ) &gt; 2 r . When d g ( x, y ) ≤ 2 r , the third point must lie in a union of a bounded number of geodesic 2 r -balls, and hence

$$| g _ { 2 , r } ( x , y ) | = O ( r ^ { d } )$$

$$\mathbb { E } g _ { 2 , r } ( X _ { 1 } , X _ { 2 } ) ^ { 2 } & \leq C r ^ { 2 d } \, \mathbb { P } \{ d _ { g } ( X _ { 1 } , X _ { 2 } ) \leq 2 r \} \\ & = O ( r ^ { 3 d } ) ,$$

$$\mathbb { E } h _ { 2 , r } ^ { 2 } = O ( r ^ { 3 d } ) .$$

Similarly, by the projection property and the first support estimate,

$$\mathbb { E } h _ { 3 , r } ^ { 2 } \leq \mathbb { E } \xi _ { \{ 1 , 2 , 3 \} , \mathfrak { h } } ( r ) ^ { 2 } = O ( r ^ { 2 d } ) .$$

The exact variance formula for canonical Hoeffding components now gives

$$\text {Var} \, R _ { \mathfrak { h } , n } ( r ) = \binom { n } { 2 } ( n - 2 ) ^ { 2 } \mathbb { E } h _ { 2 , r } ^ { 2 } + \binom { n } { 3 } \mathbb { E } h _ { 3 , r } ^ { 2 } \leq C \{ n ^ { 4 } r ^ { 3 d } + n ^ { 3 } r ^ { 2 d } \} ,$$

which is (6.3).

Define the path-triangle contrast weight by

$$\mathfrak { c } _ { d } \colon = \frac { \mathfrak { h } _ { P _ { 3 } } } { J _ { P _ { 3 } } ( d ) } - \frac { \mathfrak { h } _ { K _ { 3 } } } { J _ { K _ { 3 } } ( d ) } ,$$

$$C _ { n } ( r ) \colon = U _ { \mathfrak { c } _ { d } } ( r ) = \frac { U _ { P _ { 3 } } ( r ) } { J _ { P _ { 3 } } ( d ) } - \frac { U _ { K _ { 3 } } ( r ) } { J _ { K _ { 3 } } ( d ) } .$$

and set

Since J h ( d ) is linear in h ,

$$J _ { \mathfrak { c } _ { d } } ( d ) = \frac { J _ { P _ { 3 } } ( d ) } { J _ { P _ { 3 } } ( d ) } - \frac { J _ { K _ { 3 } } ( d ) } { J _ { K _ { 3 } } ( d ) } = 0 .$$

We normalize the contrast by

uniformly. Therefore

and thus

$$\widehat { \mathcal { G } } _ { 3 , n } ( r ) \colon = - \frac { C _ { n } ( r ) } { \gamma _ { d } \binom { n } { 3 } r ^ { 2 d + 2 } } .$$

For clarity, we restate Theorem 3.4 in the following equivalent form.

Theorem 6.2. There exist constants C &lt; ∞ and r 0 &gt; 0 such that, for every n ≥ 3 and 0 &lt; r &lt; r 0 , the path-triangle contrast satisfies

$$\text {Var} \, C _ { n } ( r ) \leq C \left ( n ^ { 3 } r ^ { 2 d } + n ^ { 4 } r ^ { 3 d } + n ^ { 5 } r ^ { 4 d + 4 } \right ) .$$

Accordingly, its normalized estimator obeys

$$\text {Var} \, \widehat { \mathcal { G } } _ { 3 , n } ( r ) \leq C \left ( \frac { 1 } { n ^ { 3 } r ^ { 2 d + 4 } } + \frac { 1 } { n ^ { 2 } r ^ { d + 4 } } + \frac { 1 } { n } \right ) .$$

Now let r n ↓ 0 . If the bandwidth sequence satisfies

$$n ^ { 3 } r _ { n } ^ { 2 d + 4 } \longrightarrow \infty , \quad n ^ { 2 } r _ { n } ^ { d + 4 } \longrightarrow \infty ,$$

then the normalized contrast consistently estimates the intrinsic functional:

$$\widehat { \mathcal { G } } _ { 3 , n } ( r _ { n } ) \stackrel { \mathbb { P } } { \rightarrow } \mathcal { G } _ { 3 } ( f ; g ) .$$


<!-- p:39 -->


Proof. Apply Lemma 6.1 to c d ; its Euclidean mass is zero. This gives (3.3).

By the definition

which is (3.4).

$$B _ { Y } \left ( 3 . 1 \right ) , \\ \mathbb { E } \widehat { \mathcal { G } } _ { 3 , n } ( r _ { n } ) \longrightarrow \mathcal { G } _ { 3 } ( f ; g ) .$$

$$\widehat { \mathcal { G } } _ { 3 , n } ( r ) = - \frac { C _ { n } ( r ) } { \gamma _ { d } \binom { n } { 3 } r ^ { 2 d + 2 } } ,$$

we have

$$\text {Var} \, \widehat { \mathcal { G } } _ { 3 , n } ( r ) = \frac { \text {Var} \, C _ { n } ( r ) } { \gamma _ { d } ^ { 2 } \left ( ^ { n } _ { 3 } \right ) ^ { 2 } r ^ { 4 d + 4 } } .$$

Since ( n 3 ) ≍ n 3 for n ≥ 3, (3.3) yields

$$\text {Var} \, \widehat { \mathcal { G } } _ { 3 , n } ( r ) \leq C \left ( \frac { 1 } { n ^ { 3 } r ^ { 2 d + 4 } } + \frac { 1 } { n ^ { 2 } r ^ { d + 4 } } + \frac { 1 } { n } \right ) ,$$

$$\mathbb { E } \mathcal { G } _ { 3 , n } ( r _ { n } ) \longrightarrow \mathcal { G } _ { 3 } ( f ; g ) .$$

Furthermore, the right-hand side of (3.4) tends to zero under (3.5). Chebyshev's inequality completes the proof.

### 6.2 The H ́ ajek-projection-dominant limit

Let

uniformly in x .

For clarity, we record the following equivalent reformulation of Theorem 3.5, emphasizing the rootn fl uctuation of the normalized contrast around its exact expectation.

Theorem 6.3. Let r n ↓ 0 and assume that

$$n r _ { n } ^ { d + 4 } \longrightarrow \infty .$$

Then the exact-expectation-centered normalized path-triangle contrast has the rootn limit

$$\sqrt { n } \left ( \widehat { \mathcal { G } } _ { 3 , n } ( r _ { n } ) - \mathbb { E } \widehat { \mathcal { G } } _ { 3 , n } ( r _ { n } ) \right ) \stackrel { \mathcal { D } } { \longrightarrow } N ( 0 , \sigma _ { f } ^ { 2 } ) ,$$

$$\sigma _ { f } ^ { 2 } = 4 d ^ { 2 } \int _ { M } \psi _ { f } ( x ) ^ { 2 } f ( x ) \, d v o l _ { g } ( x ) .$$

where

The limiting normal distribution is understood to be degenerate at zero when σ 2 f = 0 .

$$\theta _ { r } \colon = \mathbb { E } \xi _ { \{ 1 , 2 , 3 \} , \mathfrak { c } _ { d } } ( r ) , \quad h _ { 1 , r } ( x ) \colon = m _ { \mathfrak { c } _ { d } , r } ( x ) - \theta _ { r } .$$

The Hoeffding decomposition for the unnormalized order-three statistic is

$$C _ { n } ( r ) - \mathbb { E } C _ { n } ( r ) = \left ( \begin{matrix} n - 1 \\ 2 \end{matrix} \right ) \sum _ { i = 1 } ^ { n } h _ { 1 , r } ( X _ { i } ) + R _ { n } ( r ) ,$$

where R n ( r ) is orthogonal to the first projection.

Since

$$m _ { c _ { d } , r } ( x ) = \frac { r ^ { 2 d } } { f ( x ) } \mathcal { I } _ { c _ { d } } ( r , x )$$

and J c d ( d ) = 0, the pointwise expansion in Proposition 5.2 gives, uniformly in x ∈ M ,

$$\frac { m _ { \text {c} , r } ( x ) } { D _ { d } r ^ { 2 d + 2 } } = q _ { f } ( x ) + o ( 1 ) .$$

Integrating against f d vol g and using (3.1) gives

$$\frac { h _ { 1 , r } ( x ) } { D _ { d } r ^ { 2 d + 2 } } = \psi _ { f } ( x ) + o ( 1 )$$


<!-- p:40 -->


Proof. Since

Then

and hence

$$\frac { \binom { n - 1 } { 2 } } { \binom { n } { 3 } } = \frac { 3 } { n } , \quad \frac { 3 D _ { d } } { \gamma _ { d } } = 2 d ,$$

the first term in (6.7) contributes

-

$$- \frac { 2 d } { n } \sum _ { i = 1 } ^ { n } \psi _ { f } ( X _ { i } ) + o _ { L ^ { 2 } } ( n ^ { - 1 / 2 } )$$

to ̂ G 3 ,n ( r ) - E ̂ G 3 ,n ( r ). Indeed, the uniform remainder in (6.9) has centered L 2 norm tending to zero. Because ψ f is bounded on the compact manifold and the centered remainder is uniformly o (1) in L 2 ( f d vol g ), the triangular array differs in L 2 from the fixed i.i.d. sum - 2 dn - 1 ∑ n i =1 ψ f ( X i ). The ordinary i.i.d. central limit theorem therefore gives the normal limit with variance (3.10).

It remains to check that the higher Hoeffding terms are negligible. By (6.3),

$$n \ V a r \left ( \frac { R _ { n } ( r _ { n } ) } { \gamma _ { d } \left ( ^ { n } _ { 3 } \right ) r _ { n } ^ { 2 d + 2 } } \right ) \\ & \leq C \left ( \frac { 1 } { n ^ { 2 } r _ { n } ^ { 2 d + 4 } } + \frac { 1 } { n r _ { n } ^ { d + 4 } } \right ) \longrightarrow 0 .$$

For the first term, note that

because

This proves (3.9).

Remark 6.4 (Degeneracy under uniform sampling) . Suppose f ≡ V - 1 , where V = Vol g ( M ), and put

$$\overline { S c a l } _ { g } \colon = \frac { 1 } { V } \int _ { M } S c a l _ { g } \ d v o l _ { g } .$$

$$\psi _ { f } ( x ) = \frac { \overline { S c a l } _ { g } - S c a l _ { g } ( x ) } { 4 d V ^ { 2 } }$$

$$\sigma _ { f } ^ { 2 } = \frac { 1 } { 4 V ^ { 5 } } \int _ { M } \left ( S c a l _ { g } - \overline { S c a l } _ { g } \right ) ^ { 2 } d v o l _ { g } .$$

Thus the rootn limit is nondegenerate exactly when the scalar curvature is not constant. In particular, for constant-curvature surfaces the theorem still holds, but its limit at the rootn scale is degenerate; the consistency statement in Corollary 3.7 is unaffected. This also shows that the rootn fl uctuation around the exact mean records spatial variation of scalar curvature, rather than the Euler characteristic itself.

### 6.3 Surface Euler characteristic

Throughout this subsection, assume d = 2 and uniform sampling,

$$f \equiv V ^ { - 1 } , \quad V \colon = V o l _ { g } ( M ) .$$

By Table 1 and the elementary lens integrals,

$$J _ { P _ { 3 } } ( 2 ) = M _ { P _ { 3 } } ( 2 ) = \frac { 9 \sqrt { 3 } \pi } { 4 } , \quad J _ { K _ { 3 } } ( 2 ) = \frac { \pi ( 4 \pi - 3 \sqrt { 3 } ) } { 4 } ,$$

$$n ^ { 2 } r _ { n } ^ { 2 d + 4 } = ( n r _ { n } ^ { d } ) ( n r _ { n } ^ { d + 4 } ) \longrightarrow \infty ,$$

$$n r _ { n } ^ { d } = ( n r _ { n } ^ { d + 4 } ) r _ { n } ^ { - 4 } \longrightarrow \infty .$$


<!-- p:41 -->


and

Define the triangle-based estimator

$$\widehat { F } _ { 3 , n } ( r ) \colon = \frac { U _ { K _ { 3 } } ( r ) } { \binom { n } { 3 } r ^ { 4 } J _ { K _ { 3 } } ( 2 ) }$$

and the corresponding volume estimator

$$\widehat { V } _ { n } ( r ) \colon = \begin{cases} \widehat { F } _ { 3 , n } ( r ) ^ { - 1 / 2 } , & \widehat { F } _ { 3 , n } ( r ) > 0 , \\ 1 , & \widehat { F } _ { 3 , n } ( r ) = 0 . \end{cases}$$

$$\widehat { \chi } _ { n } ( r ) \colon = \frac { 3 } { 2 \pi } \widehat { V } _ { n } ( r ) ^ { 3 } \widehat { \mathcal { G } } _ { 3 , n } ( r ) = - \frac { 3 ( 4 \pi - 3 \sqrt { 3 } ) } { 2 \pi ^ { 2 } } \frac { \widehat { V } _ { n } ( r ) ^ { 3 } C _ { n } ( r ) } { \left ( \begin{matrix} n \\ 3 \end{matrix} \right ) r ^ { 6 } } .$$

$$\mathcal { E } _ { a l l } \coloneqq \{ 2 , 1 , 0 , - 1 , - 2 , \dots \} ,$$

and define

with deterministic tie-breaking.

For clarity, we record the following equivalent reformulation of Corollary 3.7.

Corollary 6.5. Let r n ↓ 0 and assume that

$$n ^ { 2 } r _ { n } ^ { 6 } \longrightarrow \infty .$$

$$\widehat { V } _ { n } ( r _ { n } ) \stackrel { \mathbb { P } } { \rightarrow } V , \quad \widehat { \chi } _ { n } ( r _ { n } ) \stackrel { \mathbb { P } } { \rightarrow } \chi ( M ) .$$

$$\mathbb { P } \{ \widehat { \chi } _ { n } ^ { a l l } ( r _ { n } ) = \chi ( M ) \} \longrightarrow 1 .$$

Thus projection onto the admissible Euler characteristics gives exact recovery with probability tending to one.

Proof. The values of J P 3 (2) and J K 3 (2) follow from Table 1 and the elementary lens integrals

$$T _ { 0 } ( 2 ) = \frac { \pi ( 4 \pi - 3 \sqrt { 3 } ) } { 4 } , \quad T _ { 2 } ( 2 ) = \frac { \pi ( 8 \pi - 9 \sqrt { 3 } ) } { 1 2 } .$$

$$^ { \circ }$$

Indeed, since ω 2 = π ,

$$J _ { P _ { 3 } } ( 2 ) & = 3 ( \pi ^ { 2 } - T _ { 0 } ( 2 ) ) = \frac { 9 \sqrt { 3 } \pi } { 4 } , \\ M _ { P _ { 3 } } ( 2 ) & = 2 \pi ^ { 2 } - 3 T _ { 2 } ( 2 ) = \frac { 9 \sqrt { 3 } \pi } { 4 } ,$$

while

Hence

$$J _ { K _ { 3 } } ( 2 ) = T _ { 0 } ( 2 ) = \frac { \pi ( 4 \pi - 3 \sqrt { 3 } ) } { 4 } , \quad M _ { K _ { 3 } } ( 2 ) = T _ { 2 } ( 2 ) = \frac { \pi ( 8 \pi - 9 \sqrt { 3 } ) } { 1 2 } .$$

$$D _ { 2 } & = \frac { M _ { P _ { 3 } } ( 2 ) } { J _ { P _ { 3 } } ( 2 ) } - \frac { M _ { K _ { 3 } } ( 2 ) } { J _ { K _ { 3 } } ( 2 ) } \\ & = 1 - \frac { 8 \pi - 9 \sqrt { 3 } } { 3 ( 4 \pi - 3 \sqrt { 3 } ) } = \frac { 4 \pi } { 3 ( 4 \pi - 3 \sqrt { 3 } ) } .$$

$$^ { - }$$

Define also

Finally, let

Then

Moreover,

$$\gamma _ { 2 } = \frac { \pi } { 4 \pi - 3 \sqrt { 3 } } .$$

$$\widehat { \chi } _ { n } ^ { a l l } ( r ) \in \arg \min _ { k \in \mathcal { E } _ { a l l } } | \widehat { \chi } _ { n } ( r ) - k | ,$$


<!-- p:42 -->


Therefore

Since f ≡ V - 1 , we have

Therefore,

$$\gamma _ { 2 } = \frac { 3 D _ { 2 } } { 4 } = \frac { \pi } { 4 \pi - 3 \sqrt { 3 } } .$$

$$\int _ { M } f ^ { 3 } \, d v o l _ { g } = V ^ { - 2 } , \quad \text {grad} \, f = 0 .$$

Hence the triangle expectation expansion gives

$$\mathbb { E } \widehat { F } _ { 3 , n } ( r ) = V ^ { - 2 } + O ( r ^ { 2 } ) .$$

Since d = 2, Lemma 6.1, applied to the triangle kernel, gives

$$\ V a r { U } _ { K _ { 3 } } ( r ) \leq C \left ( n ^ { 3 } r ^ { 4 } + n ^ { 4 } r ^ { 6 } + n ^ { 5 } r ^ { 8 } \right ) .$$

$$\text {Var} \, \widehat { F } _ { 3 , n } ( r ) & \leq C \frac { n ^ { 3 } r ^ { 4 } + n ^ { 4 } r ^ { 6 } + n ^ { 5 } r ^ { 8 } } { \left ( 3 \right ) ^ { n } r ^ { 8 } } \\ & \leq C \left ( \frac { 1 } { n ^ { 3 } r ^ { 4 } } + \frac { 1 } { n ^ { 2 } r ^ { 2 } } + \frac { 1 } { n } \right ) , \\$$

where we used ( n 3 ) ≍ n 3 and absorbed the fixed positive constant J K 3 (2) - 2 into C . Condition (3.12) implies nr 2 n →∞ , and therefore

$$n ^ { 3 } r _ { n } ^ { 4 } \rightarrow \infty , \quad n ^ { 2 } r _ { n } ^ { 2 } \rightarrow \infty , \quad n ^ { 3 } r _ { n } ^ { 8 } = ( n ^ { 2 } r _ { n } ^ { 6 } ) ( n r _ { n } ^ { 2 } ) \rightarrow \infty .$$

Since E ̂ F 3 ,n ( r n ) → V - 2 and Var ̂ F 3 ,n ( r n ) → 0, we have

$$\widehat { F } _ { 3 , n } ( r _ { n } ) \stackrel { \mathbb { P } } { \rightarrow } V ^ { - 2 } .$$

The continuous mapping theorem then yields

$$\widehat { V } _ { n } ( r _ { n } ) \stackrel { \mathbb { P } } { \rightarrow } V .$$

The two conditions of Theorem 3.4 also hold for d = 2, so

$$\widehat { \mathcal { G } } _ { 3 , n } ( r _ { n } ) \stackrel { \mathbb { P } } { \rightarrow } \mathcal { G } _ { 3 } ( f ; g ) .$$

Since G 3 ( f ; g ) = 2 πχ ( M ) 3 V 3 , Slutsky's theorem gives

$$\widehat { \chi } _ { n } ( r _ { n } ) \stackrel { \mathbb { P } } { \rightarrow } \chi ( M ) .$$

The Euler characteristics of closed connected surfaces belong to E all , and distinct values in E all are separated by distance one. Therefore, consistency of ̂ χ n ( r n ) implies

$$\mathbb { P } \{ \widehat { \chi } _ { n } ^ { \text {all} } = \chi ( M ) \} \longrightarrow 1 .$$

<!-- p:43 -->


## 7 Discussion and limitations

The path-triangle contrast identifies the intrinsic functional

$$\mathcal { G } _ { 3 } ( f ; g ) = \int _ { M } f \| \text { grad } f \| _ { g } ^ { 2 } \, d \text {vol} _ { g } + \frac { 1 } { 6 } \int _ { M } f ^ { 3 } \, \text {scal} _ { g } \, \text { d} \text {vol} _ { g } .$$

Under uniform sampling on a closed surface, Gauss-Bonnet reduces the second-order geometric term to a multiple of χ ( M ), leading to the estimator in Corollary 3.7. In general, however, path and triangle counts alone do not separate the density-gradient and scalar-curvature contributions.

The expectation expansion gives an o (1) normalized bias, which is sufficient for consistency, whereas the central limit theorem is centered at the exact expectation. A target-centered limit theorem, studentization, or confidence intervals would require sharper bias and variance estimates.

The restriction d &gt; 6 in the degree-two threshold theorem comes from the separation between the overlap error O ( n - 1 / 2 ) and the geometric correction n - 3 /d . At d = 6, determining the next term would require a more refined connected-cluster or factorial-cumulant analysis.

Finally, the boundaryless assumption avoids orderr boundary corrections. The argument also exploits the special structure of connected three-vertex kernels; for k ≥ 3, several moving internal-chord boundaries appear, and the present two-parameter reduction need not persist.

## A One-dimensional reduction of the k = 2 constants

Assume d ≥ 2 throughout this appendix. This appendix gives the elementary one-dimensional calculation underlying the positive representation of C 2 ( d ). Equivalently, since M 2 ( d ) = 4 dC 2 ( d ), put

$$J _ { d } = \int _ { 0 } ^ { 1 / 2 } ( 1 - x ^ { 2 } ) ^ { ( d + 1 ) / 2 } \, d x .$$

We prove the manifestly positive representation

$$M _ { 2 } ( d ) = \frac { 8 d \omega _ { d } \omega _ { d - 1 } } { d + 1 } J _ { d } .$$

$$M _ { 2 } ( d ) = \frac { 4 d } { d + 2 } \omega _ { d } ^ { 2 } - 2 d \omega _ { d } \int _ { 0 } ^ { 1 } s ^ { d + 1 } L _ { d } ( s ) \, d s .$$

$$L _ { d } ( s ) = 2 \omega _ { d - 1 } \int _ { s / 2 } ^ { 1 } h ( u ) \, d u , \quad h ( u ) = ( 1 - u ^ { 2 } ) ^ { ( d - 1 ) / 2 } .$$

Recall that

Also recall that

Fubini-Tonelli theorem implies that

$$\int _ { 0 } ^ { 1 } s ^ { d + 1 } L _ { d } ( s ) \, d s & = 2 \omega _ { d - 1 } \int _ { 0 } ^ { 1 } s ^ { d + 1 } \int _ { s / 2 } ^ { 1 } h ( u ) \, d u \, d s \\ & = \frac { 2 \omega _ { d - 1 } } { d + 2 } \left [ \int _ { 0 } ^ { 1 / 2 } ( 2 u ) ^ { d + 2 } h ( u ) \, d u + \int _ { 1 / 2 } ^ { 1 } h ( u ) \, d u \right ] .$$

Let

$$I _ { 0 } = \int _ { 0 } ^ { 1 / 2 } h ( u ) \, d u , \quad I _ { 1 } = \int _ { 1 / 2 } ^ { 1 } h ( u ) \, d u , \quad I _ { 2 } = \int _ { 0 } ^ { 1 / 2 } u ^ { d + 2 } h ( u ) \, d u .$$

Since ω d = 2 ω d - 1 ( I 0 + I 1 ), the expression for M 2 ( d ) becomes

$$M _ { 2 } ( d ) = \frac { 4 d \omega _ { d } \omega _ { d - 1 } } { d + 2 } \left ( 2 I _ { 0 } + I _ { 1 } - 2 ^ { d + 2 } I _ { 2 } \right ) .$$


<!-- p:44 -->


It remains to identify the bracket. The substitutions u = cos θ and y = sin( θ/ 2) give

$$I _ { 1 } = \int _ { 0 } ^ { \pi / 3 } \sin ^ { d } \theta \, d \theta = 2 ^ { d + 1 } \int _ { 0 } ^ { 1 / 2 } y ^ { d } h ( y ) \, d y .$$

$$P _ { d } = \int _ { 0 } ^ { 1 / 2 } u ^ { d } h ( u ) \, d u , \quad F _ { d } = \frac { 1 } { 2 } \left ( \frac { 3 } { 4 } \right ) ^ { ( d + 1 ) / 2 } .$$

Let

Integrating

$$\frac { d } { d u } \left ( u ^ { d + 1 } ( 1 - u ^ { 2 } ) ^ { ( d + 1 ) / 2 } \right ) = ( d + 1 ) u ^ { d } ( 1 - u ^ { 2 } ) ^ { ( d + 1 ) / 2 } - ( d + 1 ) u ^ { d + 2 } h ( u )$$

over [0 , 1 / 2] gives

$$P _ { d } - 2 I _ { 2 } = \frac { 2 ^ { - d } F _ { d } } { d + 1 } .$$

Thus

$$I _ { 1 } - 2 ^ { d + 2 } I _ { 2 } = 2 ^ { d + 1 } ( P _ { d } - 2 I _ { 2 } ) = \frac { 2 F _ { d } } { d + 1 } .$$

On the other hand, integrating

$$\frac { d } { d u } \left ( u ( 1 - u ^ { 2 } ) ^ { ( d + 1 ) / 2 } \right ) = ( 1 - u ^ { 2 } ) ^ { ( d + 1 ) / 2 } - ( d + 1 ) u ^ { 2 } h ( u )$$

over [0 , 1 / 2] yields

$$F _ { d } = ( d + 2 ) J _ { d } - ( d + 1 ) I _ { 0 } .$$

Consequently, we have

and hence

holds.

### Statements and Declarations

Funding. This work was supported by the Japan Society for the Promotion of Science (JSPS) KAKENHI Grant Number 23K12507.

Competing interests. The authors declare that they have no competing interests.

Author contributions. All authors contributed to the conception of the study, the mathematical analysis, and the preparation of the manuscript. All authors read and approved the final manuscript.

Data availability. No datasets were generated or analysed during the current study.
