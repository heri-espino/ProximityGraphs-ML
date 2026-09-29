---
id: "Alvarez-Vizoso-Kirby-Peterson_2020_Manifold-Curvature-Integral-Invariant"
source_pdf: "../pdf/Alvarez-Vizoso-Kirby-Peterson_2020_Manifold-Curvature-Integral-Invariant.pdf"
source_filename: "Alvarez-Vizoso-Kirby-Peterson_2020_Manifold-Curvature-Integral-Invariant.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "good"
extraction_score: 90.0
visual_assets: "disabled"
references_file: "../references/Alvarez-Vizoso-Kirby-Peterson_2020_Manifold-Curvature-Integral-Invariant.references.md"
---

<!-- p:1 -->

Contents lists available at ScienceDirect

### Linear Algebra and its Applications

www.elsevier.com/locate/laa

## Manifold curvature learning from hypersurface integral invariants

Javier Álvarez-Vizoso a , ∗ , Michael Kirby b , Chris Peterson b

- a Max-Planck-Institut für Sonnensystemforschung, Justus-von-Liebig-Weg 3, 37077 Göttingen, Germany
- b Department of Mathematics, Colorado State University, 841 Oval Drive, Fort Collins, CO 80523, USA

##### a r t i c l e i n f o

##### a b s t r a c t

Article history:

Received 20 September 2019 Accepted 13 May 2020 Available online 21 May 2020 Submitted by P. Semrl

MSC: 53B99 55A07 62H25

Keywords: Riemann curvature tensor Principal component analysis Local eigenvalue decomposition Manifold learning Integral invariants obtained from Principal Component Analysis on a small kernel domain of a submanifold encode important geometric information classically defined in differentialgeometric terms. We generalize to hypersurfaces in any dimension major results known for surfaces in space, which in turn yield a method to estimate the extrinsic and intrinsic curvature tensor of an embedded Riemannian submanifold of general codimension. In particular, integral invariants are defined by the volume, barycenter, and the EVD of the covariance matrix of the domain. We obtain the asymptotic expansion of such invariants for a spherical volume component delimited by a hypersurface and for the hypersurface patch created by ball intersections, showing that the eigenvalues and eigenvectors can be used as multi-scale estimators of the principal curvatures and principal directions. This approach may be interpreted as performing statistical analysis on the underlying point-set of a submanifold in order to obtain geometric descriptors at scale with potential applications to Manifold Learning and Geometry Processing of point clouds. © 2020 The Author(s). Published by Elsevier Inc. This is an open access article under the CC BY-NC-ND license

(http://creativecommons.org/licenses/by-nc-nd/4.0/).

* Corresponding author. E-mail addresses: javizoso@alumni.colostate.edu (J. Álvarez-Vizoso), kirby@math.colostate.edu (M. Kirby), peterson@math.colostate.edu (C. Peterson).

0024-3795/©

2020

The Author(s).

[Published by Elsevier Inc.](http://creativecommons.org/licenses/by-nc-nd/4.0/)

This is an open access article under the CC

(http://creativecommons.org/licenses/by-nc-nd/4.0/).

<!-- p:2 -->


### 1. Introduction

Manifold learning has as its prime goal the local characterization and reconstruction of manifold geometry from the study of the underlying point set, usually embedded as a submanifold in an ambient space, typically Euclidean. To obtain theoretical results that can serve as tools for this endeavor, it is assumed that the complete continuous point set is known so that local statistical invariants on given domains can be shown to be related to the relevant local geometry, whereas in practice only a fi nite cloud of points, probably with noise, is available. In geometry processing, the development of these methods provides us with descriptors that serve as geometry estimators, guide a possible reconstruction, or provide feature detectors. The integral invariant point of view attempts to overcome some of the difficulties of computational geometry when facing the task of extracting information that is classically defined as a differential invariant, like curvature, since its discrete version reduces to, e.g., sums instead of fi nite differences. The multi-scale behavior and averaging nature of these invariants is also of importance in applications and their possible stability and robustness with respect to noise.

Series expansion of the volume of small geodesic balls within a manifold [1], and volumes cut out by a hypersurface inside a ball of the ambient space [2], have been shown to be given in terms of the manifold curvature scalar invariants. In order to obtain local adaptive Galerkin bases for large-dimensional dynamical systems, the eigenvalue decomposition of covariance matrices of spherical intersection domains on the invariant manifold was introduced in [3], [4,5] to provide estimates of the dimension of the manifold and a suitable decomposition of phase space at every point. In the case of curves, the Frenet-Serret apparatus is recovered with explicit formulas at scale to obtain descriptors of the generalized curvatures in terms of the eigenvalues of the covariance matrix [6]. Integral invariants were already introduced and employed in geometry processing applications by [7], [8,9], [10,11], [12,13]. Local principal component analysis of this type has been studied primarily for the case of curves and surface in 2D and 3D in [10,11], [13], [14], [15], [16], [17], as a means to determine relevant local geometric information while maintaining stability with respect to noise [18], [19,20], e.g., for feature and shape detection using point clouds or meshes in computer graphics. Voronoi-based feature estimation [21,22] has also taken advantage of the PCA covariance matrix approach. Those methods study embedded manifolds whereas intrinsic probability and statistical analysis using geometric measurements inside a Riemannian manifold have also been developed [23,24] and could be used to do covariance analysis of submanifolds embedded in curved ambient spaces.

The complementary side of this framework is the study of fi nite point clouds and how their discrete PCA covariance matrices converge with the number of points to the exact analytical result of the smooth case, as studied in our work. Methods using geometric measure theory and harmonic analysis have been developed [25,26], [27,28] in order to study noisy samples from probability distributions supported on submanifolds of a highdimensional Euclidean space [29]. In these works, ranges of scales are determined, taking into account curvature, for the covariance matrices to be most informative and close to the noisy empirical matrices. The approach of [29] is complemented by ours in the sense that we obtain explicitly the next to leading order terms of the eigenvalue expansion for the complete smooth data set providing the direct theoretical link between curvature and covariance. Since [29] develops an explicit algorithm for the estimation of the dimension of the manifold, a natural next step would be to expand these multiscale methods in order to apply them to our main theorems and thus to estimate curvature from noisy point clouds. Our descriptor algorithm to estimate the Riemann curvature provides the theoretical result to fulfill this task in practice.


<!-- p:3 -->


In this paper we follow and generalize the major theoretical results of [20] for surfaces in space to hypersurfaces in any dimension, which in turn allows for the extension of their approach to obtain descriptors of the extrinsic and intrinsic curvature at a given scale for any Riemannian submanifold of general codimension in Euclidean space. Future work will show how the analysis for the ball intersection patch case further extends to general codimension, [30,31], establishing the connection between the generalized third fundamental form and the integral invariants, i.e. between local Riemannian geometry and local covariance integrals.

The structure of the paper is as follows: In section 2, PCA integral invariants and geometric descriptors are introduced to show how the study of hypersurfaces is sufficient to study the curvature of Riemannian submanifolds of any dimension by applying the analysis to k hypersurface projections (where k is the codimension of the submanifold). In section 3, an explicit toy example of the correspondence between the differentialgeometric curvature and the integral invariant covariance is detailed. In section 4, these integral invariants are analytically computed for a volume region delimited by a hypersurface inside a ball; the asymptotic expansions of the invariants with respect to the scale of the ball are shown to be given in terms of the principal curvatures and the dimension, and the eigenvectors of the covariance matrix are shown to converge in the limit to the principal directions. In section 5, the analogous analysis is carried out for the integral invariants of the hypersurface patch cut out by the ball. In section 6, we see how these asymptotic formulas can be inverted to yield geometric descriptors at scale of the principal curvatures and principal directions for hypersurfaces, thus establishing concrete formulas to use in our fi nal algorithm for curvature descriptors of Riemannian submanifolds. The notation and technical results needed for all computations are summarized in appendix A.

### 2. Integral invariants and descriptors

Our approach generalizes the theoretical part of the seminal work [20] with a focus on the analytical expansion of integral invariants to get descriptors of manifold curvature in any dimension. The local integral invariants considered are integrals over small kernel domains determined by balls and the hypersurface. In particular, we will focus on the Principal Component Analysis of a ( n +1)-dimensional region delimited by the hypersurface inside a ball centered at a point on the hypersurface, and the n -dimensional patch on the submanifold cut out by such a ball. In general, one can define invariants for a measurable domain by computing the moments of the coordinates of the points inside, which leads us to Definition 2.1. Let D be a measurable domain in R n , the integral invariants associated to the moments of order 0, 1 and 2 of the coordinate functions of the points of D are: the volume


<!-- p:4 -->


$$V ( D ) = \mathbb { E } [ 1 \cdot \chi _ { D } ( X ) ] = \int _ { D } 1 \, d V o l , & & ( 1 )$$

$$s ( D ) = \mathbb { E } [ X \cdot \chi _ { D } ( X ) ] = \frac { 1 } { V ( D ) } \int _ { D } X \, d V o l ,$$

and the eigenvalue decomposition of the covariance matrix

$$C ( D ) = \mathbb { E } [ ( X - s ( D ) ) \otimes ( X - s ( D ) ) ^ { T } \cdot \chi _ { D } ( X ) ] = \int _ { D } ( X - s ( D ) ) \otimes ( X - s ( D ) ) ^ { T } \ d V o l .$$

Here dVol is the measure on D induced by restriction of the Euclidean measure, and the tensor product is to be understood as the outer product of the components in a chosen basis. E represents taking the expectation value over all possible X in their domain, i.e. R n , and χ D is the characteristic function of the set D (i.e., 1 if and only if X ∈ D , zero otherwise).

An integral invariant descriptor F ( D ) of some feature F of a measurable domain D is any expression for F completely given in terms of V ( D ) , s ( D ), the eigenvalue decomposition of C ( D ) or other integral invariants. If the domain D is determined by a region of a hypersurface S , the main geometric descriptors are any principal curvature estimators κ μ ( D ) of κ μ ( p ), and principal and normal direction estimators e μ ( D ) , N ( D ) of e μ ( p ) , N ( p ), for some known point p ∈ S . If the domain D is determined by a region of an embedded manifold M , the main geometric descriptor is any second fundamental form estimator, II ( D ) of II p , for some known point p ∈ M . Since our domain D of interest will possess a natural scale ε determined by the size of the ball that shall define it, we shall talk about descriptors at scale . Moreover, throughout all the paper we consider ε to be small enough so that we can approximate the hypersurface S by the local graph representation of its osculating quadric at p , which is sufficient to obtain the leading terms of the asymptotic expansions with scale of the integral invariants.

These descriptors become valuable tools to perform manifold learning, feature detection and shape estimation when only partial knowledge of the complete set of points is

the barycenter known or when noise is present. In this regard, [19,20,17] carried out experimental and theoretical analysis of the stability of these and other descriptors in the case of curves and surfaces in R 3 , reporting for example that the invariants of the spherical component domain are more robust with respect to noise than the patch region ones. It is to be expected that the same stability behavior holds in the hypersurface case due to the sensitivity to small changes of an n -dimensional patch compared to an ( n +1)-dimensional volume of which the perturbed patch is only part of its boundary.


<!-- p:5 -->


When the asymptotic expansions with respect to scale of hypersurface integral invariants are available to high enough order, curvature information can be extracted by truncating the series and inverting the relations in order to obtain a computable multiscale estimator of the actual curvatures. In particular, the eigenvalues of the covariance matrix will provide such a descriptor for the principal curvatures of a smooth hypersurface, κ μ ( D ), and its eigenvectors { e μ ( D ) } n μ =1 , and e n +1 ( D ), will do the same for the normal direction. In order to produce analogous descriptors for an embedded Riemannian manifold of higher codimension, we just need to apply the procedure to the k hypersurfaces created by projecting the manifold down to ( n + 1) linear subspaces determined by its tangent space and each of the normal directions.

Lemma 2.2. Let M ⊂ R n + k be an n -dimensional embedded Riemannian manifold, and fix an orthonormal basis { e μ } n μ =1 of the tangent space T p M , and an orthonormal basis { N j } k j =1 of the normal space N p M at p ∈ M . Consider a ball B ( n + k ) p ( ε ) for small enough ε &gt; 0 , such that the projections of M ∩ B ( n + k ) p ( ε ) onto the linear subspaces T p M ⊕ 〈 N i 〉 , for all i = 1 , . . . , k , are smooth hypersurfaces S i . Then, if κ ( i ) μ ( D ) , { e ( i ) μ ( D ) } n μ =1 are descriptors of the principal curvatures and principal directions at p for each of the hypersurfaces S i , then the second fundamental form of M at p has a descriptor:

$$\mathbb { I } _ { p } ( D ) ( e _ { \mu } , e _ { \nu } ) = \sum _ { i = 1 } ^ { k } [ V _ { i } ( D ) K _ { i } ( D ) V ( D ) _ { i } ^ { T } ] _ { \mu \nu } \ N _ { i } \, , \quad \mu , \nu = 1 , \dots , n , \quad ( 4 )$$

where [ V i ( D )] are the matrices whose columns are the components of { e ( i ) μ ( D ) } n μ =1 in the chosen basis { e μ } n μ =1 , and [ K i ( D )] is the diagonal matrix of principal curvature estimators. In turn, the Riemann curvature tensor of M at p acquires a descriptor:

$$\langle R ( D ) ( e _ { \mu } , e _ { \nu } ) e _ { \alpha } , e _ { \beta } \rangle = \sum _ { i = 1 } ^ { k } \left ( \left [ V _ { i } K _ { i } V _ { i } ^ { T } \right ] _ { \mu \beta } [ V _ { i } K _ { i } V _ { i } ^ { T } ] _ { \nu \alpha } - [ V _ { i } K _ { i } V _ { i } ^ { T } ] _ { \mu \alpha } [ V _ { i } K _ { i } V _ { i } ^ { T } ] _ { \nu \beta } \right ) .$$

In fact, the matrices [ V i ( D ) K i ( D ) V T i ( D )] are a descriptor of the local Hessian of S j at p .

Proof. By the implicit function theorem, there is a neighborhood of U p ⊂ T p M such that the manifold can be locally given by a graph x ↦→ ( x , f 1 ( x ) , . . . , f k ( x )), where x ∈ U p , p corresponds to 0 , and ∇ f i ( 0 ) = 0 . From this, the projection hypersurfaces S i are just ( x , f i ( x )) within the linear subspace T p M ⊕ 〈 N i 〉 , for i = 1 , . . . , k . It can be shown


<!-- p:6 -->


[32, vol. II ex. 3.3.] that the second fundamental form of M at p is precisely the linear combination of the second fundamental forms of each of the hypersurface projections weighed by the corresponding normal vector, i.e.,

$$\Pi _ { p } ( e _ { \mu } , e _ { \nu } ) = \sum _ { i = 1 } ^ { k } \left [ \frac { \partial ^ { 2 } f _ { i } } { \partial x _ { \mu } \partial x _ { \nu } } ( p ) \right ] N _ { i } \\$$

Analyzing each of those hypersurfaces in T p M ⊕ 〈 N i 〉 ∼ = R n +1 , to obtain descriptors κ ( i ) μ ( D ), { e ( i ) μ ( D ) } n μ =1 for every i , we obtain precisely a descriptor of the eigenvalue decomposition of each Hessian, i.e., Hess f i | p ( D ) = [ V i ( D ) K i ( D ) V ( D ) T i ] is an estimator of the second fundamental form of S i at p in the original basis. Applying Gauß equation

$$\langle R ( e _ { \mu } , e _ { \nu } ) e _ { \alpha } , e _ { \beta } \rangle = \langle \mathbb { I } ( e _ { \mu } , e _ { \beta } ) , \mathbb { I } ( e _ { \nu } , e _ { \alpha } ) \rangle - \langle \mathbb { I } ( e _ { \mu } , e _ { \alpha } ) , \mathbb { I } ( e _ { \nu } , e _ { \beta } ) \rangle$$

yields a corresponding descriptor for the Riemann tensor.

Box

A concrete application of this result in a toy computation is presented in the next section. We summarize the steps for the applicability of these ideas for arbitrary embedded Riemannian manifolds in the following algorithm.

- Algorithm 1 Curvature descriptors from ball intersections. Input: Point-set M ⊂ R n + k , point p ∈ M , radius ε &gt; 0 Output: 2nd fundamental form descriptor II p ( ε ), Riemann tensor descriptor R μναβ ( ε ) at p if current basis is not known to split T p M ⊕ N p M into a tangent and normal basis then - Find the eigenvectors { e μ } n μ =1 ∪ { N i } k i =1 of E [( X - p ) ⊗ ( X - p ) T · χ Bp ( ε ) ∩M ( X )] {Dimension n and split basis are determined by different scaling of eigenvalues, cf. [5]} - Update the basis to the normalized eigenvector basis end if for i = 1 to n do - Project M to a hypersurface S i in the linear subspace 〈{ e μ } n i =1 , N i 〉 ∼ = R n +1 ⊂ R n + k - Determine region D i := V + p ( ε ) (cf. Lemma 4.2) or D p ( ε ) (cf. section 5) of this S i - Compute the induced volume V ( D i ) = E [1 · χ Di ( X )] - Compute the barycenter s ( D i ) = E [ X · χ Di ( X )] /V ( D i ) - Compute the eigenvectors { e ( i ) μ ( ε ) } n i =1 ∪ N i ( ε ), and eigenvalues { λ ( i ) μ ( ε ) } n +1 μ =1 of the covariance matrix C ( D i ) = E [( X - s ( D i )) ⊗ ( X - s ( D i )) T · χ Di ( X )] - Obtain the principal curvatures κ ( i ) μ ( ε ) from λ ( i ) μ ( ε ) using Corollary 6.1 or Corollary 6.2 - Set V i to the matrix whose columns are { e ( i ) μ ( ε ) } n i =1 - Set K i to the diagonal matrix of { κ ( i ) μ ( ε ) } n μ =1 - Determine the Hessian matrix descriptor at p of S i by II ( i ) p ( ε ) = [ V i · K i · V T i ] end for - Obtain the 2nd fundamental form estimator: II p ( ε )( e μ , e ν ) = ∑ k i =1 [ II ( i ) p ( ε )] μν N i ( ε ) - Obtain the Riemann curvature tensor estimator: R μναβ ( ε ) = 〈 R ( ε )( e μ , e ν ) e α , e β 〉 = ∑ k i =1 ( [ II ( i ) p ( ε )] μβ [ II ( i ) p ( ε )] να - [ II ( i ) p ( ε )] μα [ II ( i ) p ( ε )] νβ )

### 3. Example of the covariance-curvature correspondence

Let us study a simple analytic toy example to understand the integral invariant approach to differential geometry. The classical approach follows [33]. Let M ⊂ R 4 be an embedded smooth surface such that around a point p ∈ M it has a local graph expression in a neighborhood U p given to second order by its osculating quadric M (2) p (indeed, note that curvature is fully determined by this second order truncation, but our general analysis will take into account the errors from the full series):


<!-- p:7 -->


$$\mathcal { M } _ { p } ^ { ( 2 ) } = \{ ( x , y , f _ { 1 } , f _ { 2 } ) \in \mathbb { R } ^ { 4 } \ | \ f _ { 1 } ( x , y ) = - \frac { 1 } { 2 } x ^ { 2 } - 3 x y - \frac { 1 } { 2 } y ^ { 2 } , f _ { 2 } ( x , y ) = \frac { 9 } { 4 } x ^ { 2 } + \frac { \sqrt { 3 } } { 2 } x y + \frac { 7 } { 4 } y ^ { 2 } \} .$$

This can always be done for arbitrary dimension and we can think of f i ( x ) as the leading order truncation of the Taylor expansions of the local graph functions of M over T p M , with x as coordinates of this tangent space. Given an orthonormal tangent basis { e μ } n μ =1 and normal basis { N i } k i =1 , the extrinsic curvature of M at p is encoded by the second fundamental form, determined by the Hessians II ( i ) p of f i ( x ) as seen in the previous section. Thus, for this example it can be written as the following quadratic form with values in the normal space N p M , for any a , b ∈ T p M :

$$\Pi _ { p } ( a , b ) = \sum _ { i = 1 } ^ { 2 } I _ { p } ^ { ( i ) } ( a , b ) N _ { i } = \left ( a ^ { T } \cdot \left [ \begin{smallmatrix} - 1 & - 3 \\ - 3 & - 1 \end{smallmatrix} \right ] \cdot b \right ) \, N _ { 1 } + \left ( a ^ { T } \cdot \left [ \begin{smallmatrix} \frac { 9 } { 2 } & \frac { \sqrt { 3 } } { 2 } \\ \frac { \frac { 9 } { 2 } } { 2 } & \frac { \frac { \sqrt { 3 } } { 2 } } { 2 } \end{smallmatrix} \right ] \cdot b \right ) \, N _ { 2 } . \\ \\ \text {The mean curvature vector is then } H \, = \, \text {tr} \, U \, \mathbb { I } \, U \, - \, H \, \mathbb { N } _ { + } \, + \, H \, \mathbb { N } _ { - } = - 2 N _ { + } + 8 N _ { - } \, s _ { 0 }$$

The mean curvature vector is then H p = tr II p = H 1 N 1 + H 2 N 2 = - 2 N 1 +8 N 2 , so we can consider || H p || = 2 √ 17 ≈ 8 . 2462112512 a scalar characterization of the extrinsic curvature at p . The (intrinsic) Riemann curvature tensor for a surface, even embedded in higher dimension, has only 1 independent component, the Gaußian curvature R 1221 = 7. We can see this by computing the curvature operators at p in our orthonormal tangent basis using eq. (7) in eq. (6):

$$R _ { p } ( e _ { 1 } , e _ { 2 } ) = - R _ { p } ( e _ { 2 } , e _ { 1 } ) = \begin{bmatrix} 0 & - 7 \\ 7 & 0 \end{bmatrix} , \quad R _ { p } ( e _ { 1 } , e _ { 1 } ) = R _ { p } ( e _ { 2 } , e _ { 2 } ) = \begin{bmatrix} 0 & 0 \\ 0 & 0 \end{bmatrix} .$$

From the integral invariant point of view, the aim is to obtain the same information by completely different means: using the eigenvalue decomposition of the covariance matrix of domains determined by the underlying point-set of M around p , i.e. instead of employing (covariant) derivatives on M , the same information is hidden within the asymptotics of integrals over local domains. Conceptually this signifies that we need only know the measure function over a domain within M , i.e. a means to evaluate expectation values E [ · · · χ D ( X )], which is equivalent to knowing only one volume element function, e.g. √ det g ( x ) d n x in local coordinates, instead of the ( n + k ) embedding functions X ( x ), or the n ( n + 1) / 2 components of the metric tensor g μν = 〈 ∂ X ∂x μ , ∂ X ∂x ν 〉 . Therefore the

The Ricci operator is R ic p = [ 7 0 0 7 ] , so the scalar curvature is R p = tr R ic p = 14, again the only independent intrinsic invariant (same as R 1221 upon normalization by dim M , a convention which we do not follow here). These computations yield the classical geometric invariants determined by the differential structure of M around p .


<!-- p:8 -->


integral invariant approach furnishes in principle a dictionary between covariance and curvature that requires less actual knowledge about the parametrization focusing on the underlying point-set, thus providing a more adequate methodology when only a discrete point cloud sample is available.

In our toy example we can analytically show this correspondence to high precision since the embedding functions are known and the integral invariants of eq. (1), eq. (2) and eq. (3) can be expressed explicitly and computed numerically. Since there are two normal directions there are no canonical principal directions and principal curvatures for a surface in R 4 , but one such set for each normal direction. Choosing N 1 and N 2 , the principal directions and curvatures are just the eigenvalue decomposition of the Hessian matrices in eq. (7). Therefore, we can consider the projected local (hyper)surfaces S i given by the graphs ( x , f i ( x )) in the linear subspaces T p M ⊕〈 N i 〉 , with corresponding principal directions { e ( i ) μ ( p ) } n μ =1 and principal curvatures { κ ( i ) μ ( p ) } n μ =1 , for i = 1 . . . k , here k = 2. This yields two local surfaces in two R 3 subspaces of R 4 , with principal directions and principal curvatures given by the eigenvalue decomposition of each [ ∂ 2 f i ∂x μ ∂x ν (0) ] :

$$\kappa _ { 1 } ^ { ( 1 ) } ( p ) & = 2 , \, e _ { 1 } ^ { ( 1 ) } ( p ) = \frac { 1 } { \sqrt { 2 } } ( - 1 , 1 , 0 ) ^ { T } \quad \text {and} \quad \kappa _ { 2 } ^ { ( 1 ) } ( p ) = - 4 , \, e _ { 2 } ^ { ( 1 ) } ( p ) = \frac { 1 } { \sqrt { 2 } } ( 1 , 1 , 0 ) ^ { T } , \, ( 9 ) \\ \kappa _ { 1 } ^ { ( 2 ) } ( p ) & = 3 , \, e _ { 1 } ^ { ( 2 ) } ( p ) = ( \frac { - 1 } { 2 } , \, \frac { \sqrt { 3 } } { 2 } , 0 ) ^ { T } \quad \text {and} \quad \kappa _ { 2 } ^ { ( 2 ) } ( p ) = 5 , \, e _ { 2 } ^ { ( 2 ) } ( p ) = ( \frac { \sqrt { 3 } } { 2 } , \, \frac { 1 } { 2 } , 0 ) ^ { T } . \quad ( 1 0 )$$

Determining these for each S i from integral invariants makes it possible to recover the Hessian matrices and hence the full second fundamental form II p of M , and the Riemann tensor thereafter. As domain D i for our descriptors we shall use the intersection regions B ( n +1) p ( ε ) ∩ S i , which cuts out a patch domain in S i around p using the ambient space ball of radius ε &gt; 0, see Fig. 1a and section 5. The moments of inertia of the shaded region in the fi gure yield approximations at scale ε to the principal and normal directions and the principal curvatures at p . In our example D i = { ( x, y, z ) ∈ T p M ⊕〈 N i 〉 | z = f i ( x, y ) , x 2 + y 2 + f i ( x, y ) 2 ≤ ε 2 } . These regions are well-defined for ε small enough which is sufficient to establish the asymptotic behavior of the integral invariants with the scale of the domain, as developed in the sections below, so that the covariancecurvature correspondence is well-defined in the limit to provide curvature estimators in the general case when the local graph expression of the manifold is of course unknown and the domain may be bigger. In that case the D i are known only as point-sets and the expectation values can only be computed numerically. According to our results in section 5, the volumes and barycenters to leading order are:

$$V o l ( D _ { 1 } ) = \pi \varepsilon ^ { 2 } ( 1 + \frac { 9 } { 8 } \varepsilon ^ { 2 } + \dots ) , \quad V o l ( D _ { 2 } ) = \pi \varepsilon ^ { 2 } ( 1 + \frac { 1 } { 8 } \varepsilon ^ { 2 } + \dots ) , \\ s ( D _ { 1 } ) = ( 0 , 0 , \frac { - \varepsilon ^ { 2 } } { 4 } + \dots ) ^ { T } , \quad s ( D _ { 2 } ) = ( 0 , 0 , \varepsilon ^ { 2 } + \dots ) ^ { T } .$$


<!-- p:9 -->


8.44

Fig. 1. (a) The covariance EVD of domains determined by ball intersections at scale provide descriptors that approximate the principal and normal directions and principal curvatures of a hypersurface at a generic point. (b) In general codimension, this covariance analysis for projection hypersurfaces of the embedded manifold can be used to estimate the 2nd fundamental form and Riemann tensor. The simple example of the text shows the asymptotic convergence to the exact value of extrinsic and intrinsic curvature ( || H || and R 1212 resp.)

More importantly, the covariance matrices in this example have the following analytical form:

$$C ( D _ { i } ) & = \mathbb { E } [ ( X - s ( D _ { i } ) ) \otimes ( X - s ( D _ { i } ) ) ^ { T } \cdot \chi _ { D } ( X ) ] \\ & = \int _ { x ^ { 2 } + y ^ { 2 } + f _ { 2 } ^ { 2 } \leq e ^ { 2 } } \left [ \begin{array} { c c } x ^ { 2 } & x y & x ( f _ { i } - \frac { H _ { i } e ^ { 2 } } { 8 } ) \\ y x & y ^ { 2 } & y ( f _ { i } - \frac { H _ { i } e ^ { 2 } } { 8 } ) \\ x ( f _ { i } - \frac { H _ { i } e ^ { 2 } } { 8 } ) & y ( f _ { i } - \frac { H _ { i } e ^ { 2 } } { 8 } ) & ( f _ { i } - \frac { H _ { i } e ^ { 2 } } { 8 } ) ^ { 2 } \end{array} \right ] \sqrt { \det g _ { i } ( x , y ) } \, d x d y , \\ \intertext { w h e r e t h e i n d u c $ o n $ $ s _ { i } $ a r e }$$

$$\text {where the included volume elements on } & _ { i } \, a r e . \\ & d V o l _ { 1 } = \sqrt { \det g _ { 1 } ( x , y ) } \, d x d y = \sqrt { 1 + 1 0 x ^ { 2 } + 1 2 x y + 1 0 y ^ { 2 } } \, d x d y , \\ & d V o l _ { 2 } = \sqrt { \det g _ { 2 } ( x , y ) } \, d x d y = \sqrt { 1 + 2 1 x ^ { 2 } + 8 \sqrt { 3 } x y + 1 3 y ^ { 2 } } \, d x d y . \\ \text {For instance, for } & \varepsilon = 0 . 0 1 \, \text {numerical integration yields} .$$

where the induced volume elements on S i are:

For instance, for ε = 0 . 01 numerical integration yields:

$$C ( D _ { 1 } ) = \left [ \begin{matrix} 7 . 8 5 4 4 3 9 2 0 3 9 \cdot 1 0 ^ { - 9 } & - 3 . 9 2 8 9 7 3 3 0 4 \cdot 1 0 ^ { - 1 3 } & - 1 . 6 5 0 5 3 8 6 2 9 \cdot 1 0 ^ { - 4 9 } \\ - 3 . 9 2 8 9 7 3 3 0 4 \cdot 1 0 ^ { - 1 3 } & 7 . 8 5 4 4 3 9 2 0 3 9 \cdot 1 0 ^ { - 9 } & - 3 . 2 3 4 5 7 0 7 4 5 8 \cdot 1 0 ^ { - 4 9 } \\ - 1 . 6 5 0 5 3 8 6 2 9 \cdot 1 0 ^ { - 4 9 } & - 3 . 2 3 4 5 7 0 7 4 5 8 \cdot 1 0 ^ { - 4 9 } & 1 . 2 4 3 1 7 5 7 5 9 \cdot 1 0 ^ { - 1 2 } \end{matrix} \right ] ,$$

From Theorem 5.4 below their respective eigenvectors approximate the principal and normal directions of S i at this scale, and the corresponding eigenvalues serve as input for the formulas of Corollary 6.2 to estimate the principal curvatures as well:

$$C ( D _ { 1 } ) & = \left [ \begin{array} { c c c c } 7 . 8 5 4 4 3 9 2 0 3 9 \cdot 1 0 ^ { - 9 } & - 3 . 9 2 8 9 7 3 3 3 0 4 \cdot 1 0 ^ { - 1 3 } & - 1 . 6 5 0 5 3 8 6 2 9 \cdot 1 0 ^ { - 4 9 } \\ - 3 . 0 2 8 9 7 3 3 3 0 4 \cdot 1 0 ^ { - 1 3 } & 7 . 8 5 4 4 3 9 2 0 3 9 \cdot 1 0 ^ { - 9 } & - 3 . 2 3 4 5 7 0 7 4 5 8 \cdot 1 0 ^ { - 4 9 } \\ - 1 . 6 5 0 5 3 8 6 2 9 \cdot 1 0 ^ { - 4 9 } & - 3 . 2 3 4 5 7 0 7 4 5 8 \cdot 1 0 ^ { - 4 9 } & 1 . 2 3 1 7 5 7 5 5 9 \cdot 1 0 ^ { - 1 2 } \\ & & \\ C ( D _ { 2 } ) & = \left [ \begin{array} { c c c c } 7 . 8 5 1 6 9 0 6 3 7 4 \cdot 1 0 ^ { - 9 } & - 4 . 5 4 7 3 9 0 3 3 7 \cdot 1 0 ^ { - 1 3 } & 9 . 9 3 9 1 9 2 4 5 2 6 \cdot 1 0 ^ { - 5 0 } \\ - 4 . 5 3 4 7 3 9 0 3 3 7 \cdot 1 0 ^ { - 1 3 } & 7 . 8 5 2 2 1 4 2 6 4 0 \cdot 1 0 ^ { - 9 } & 5 . 3 7 2 5 5 4 5 0 9 6 \cdot 1 0 ^ { - 4 9 } \\ 9 . 9 3 9 1 9 2 4 5 2 6 \cdot 1 0 ^ { - 5 0 } & 5 . 3 7 2 5 5 4 5 0 9 6 \cdot 1 0 ^ { - 4 9 } & 1 . 1 7 6 9 5 7 0 5 4 4 \cdot 1 0 ^ { - 1 2 } \\ & & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ & \\ &$$


<!-- p:10 -->


$$\kappa _ { 1 } ^ { ( 1 ) } ( \varepsilon ) & = 1 . 9 9 4 7 , \quad e _ { 1 } ^ { ( 1 ) } ( \varepsilon ) = ( - 0 . 7 0 7 1 0 6 7 8 1 2 , \, 0 . 7 0 7 1 0 6 7 8 1 2 , \, - 3 . 2 3 8 \cdot 1 0 ^ { - 4 1 } ) ^ { T } \\ \kappa _ { 2 } ^ { ( 1 ) } ( \varepsilon ) & = - 3 . 9 9 3 0 6 , \quad e _ { 2 } ^ { ( 1 ) } ( \varepsilon ) = ( 0 . 7 0 7 1 0 6 7 8 1 2 , \, 0 . 7 0 7 1 0 6 7 8 1 2 , \, 2 . 7 5 0 \cdot 1 0 ^ { - 4 1 } ) ^ { T } \\ \kappa _ { 1 } ^ { ( 2 ) } ( \varepsilon ) & = 2 . 9 9 8 4 5 , \quad e _ { 1 } ^ { ( 2 ) } ( \varepsilon ) = ( - 0 . 5 0 0 0 0 0 0 0 , \, - 0 . 8 6 6 0 2 5 4 0 3 8 , \, 5 . 0 9 7 \cdot 1 0 ^ { - 3 5 } ) ^ { T } \\ \kappa _ { 2 } ^ { ( 2 ) } ( \varepsilon ) & = 4 . 9 9 8 2 , \quad e _ { 2 } ^ { ( 2 ) } ( \varepsilon ) = ( 0 . 8 6 6 0 2 5 4 0 3 8 , \, 0 . 5 0 0 0 0 0 0 0 , \, 3 . 6 9 \cdot 1 0 ^ { - 3 5 } ) ^ { T } \\ \intertext { Compare , these  descriptive  values  at  scale  5  -  0 . 01  with  the  exact  analytical  values }$$

Compare these descriptive values at scale ε = 0 . 01 with the exact analytical values of eq. (9) and eq. (10). Now, since these are supposed to be as well the eigenvalue decomposition of the Hessian matrices of f i , we have essentially achieved an integral reconstruction of the second fundamental form of M at p , at scale ε = 0 . 01:

$$\Pi _ { p } ( \varepsilon ) = \left [ \begin{matrix} - 0 . 9 9 1 7 9 8 5 9 9 & - 2 . 9 3 8 7 8 5 0 2 1 \\ - 2 . 9 3 8 7 8 5 0 2 1 & - 0 . 9 9 1 7 9 8 5 9 9 \end{matrix} \right ] N _ { 1 } + \left [ \begin{matrix} 4 . 4 9 8 2 6 4 4 8 8 1 & 0 . 8 6 5 9 2 1 0 7 5 6 \\ 0 . 8 6 5 9 2 1 0 7 5 6 & 3 . 4 9 8 3 8 4 9 5 5 8 \end{matrix} \right ] N _ { 2 } ,$$

so || H p ( ε ) || = 8 . 2425629448. Therefore the procedure yields an estimation of the Riemann curvature tensor:

$$R _ { p } ( \varepsilon ) ( e _ { 1 } , e _ { 2 } ) = - R _ { p } ( \varepsilon ) ( e _ { 2 } , e _ { 1 } ) = \begin{bmatrix} 0 & - 7 . 0 2 1 8 9 3 4 1 \\ 7 . 0 2 1 8 9 3 4 1 & 0 \end{bmatrix} ,$$

to be compared with the exact tensors of eq. (7) and eq. (8).

By repeating this procedure at different scales ε one can clearly see the convergence of the covariance-curvature correspondence in this example, cf. Fig. 1b. The steps followed here generalize to any dimension and are summarized in Algorithm 1. In the rest of the paper we develop the technical machinery needed to establish the validity, formulae and algorithm of this asymptotic correspondence, providing the theoretical foundation of this methodology for practical applications in manifold learning.

### 4. Hypersurface spherical component integral invariants

The following domain is introduced in [2] to study the relation between the mean curvature of hypersurfaces and the volume of sections of balls (we reserve their notation B + p ( ε ) for the half-ball).

Definition 4.1. Let S be a smooth hypersurface in R n +1 with a locally chosen normal vector fi eld N : S → R n +1 . Let B ( n +1) p ( ε ) be a ball of radius ε &gt; 0 centered at a point p ∈ S , for small enough ε the hypersurface always separates this ball into two connected components. Define the region V + p ( ε ) to be that component such that N ( p ) is oriented towards its interior.

All the methods and results of [20] for surfaces using this domain generalize because to approximate integrals of functions over this type of region in R 3 , the formula developed in their work makes use of the hypersurface approximations of [2], valid in any dimension.


<!-- p:11 -->


Note we start to use the notation from the appendix. Also, in the rest of the paper we shall say that a smooth function f ( x ) has order O ( x n ) if its local power series around x = 0 begins at order n , i.e., the n th-order derivative at x = 0 is nonzero whereas all the lower order derivatives are zero at that point; this generalizes to functions of several variables by referring to its fi rst nonzero higher-order partial derivative at the center of the expansion.

Lemma 4.2. Let f : R n +1 → R be a function of order O ( ρ k z l ) in cylindrical coordinates X = ( x , z ) = ( ρ x , z ) , x ∈ S n - 1 , let S be a graph hypersurface given by the function z ( x ) whose normal at the origin points in the positive z -axis, and V + p ( ε ) the spherical component delimited by this S , then

$$\int _ { V _ { p } ^ { + } ( \varepsilon ) } f ( X ) d V & = \int _ { B _ { p } ^ { + } ( \varepsilon ) } f ( X ) d V o l - \int _ { B _ { p } ^ { + } ( \varepsilon ) } \left [ \sum _ { z = 0 } ^ { z = \frac { 1 } { 2 } \sum _ { \mu = 1 } ^ { n } \kappa _ { \mu } x _ { \mu } ^ { 2 } } f ( x , z ) \, d z \right ] d ^ { n } x + \mathcal { O } ( \varepsilon ^ { k + 2 l + n + 3 } ) \\ \intertext { w h e r e } \intertext { w h e r e } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext { s u c h t a r g a l } \intertext$$

where the half-ball B + p ( ε ) consists of the points of B n +1 p ( ε ) such that z ≥ 0 .

Proof. We approximate z ( x ) by its osculating quadric at the origin, 1 2 ∑ n μ =1 κ μ x 2 μ , and remove from the complete half-ball integral of f ( X ) its contribution from below the paraboloid. The exact integration domain is determined by the sphere intersection with the hypersurface, {‖ x ‖ 2 + z ( x ) 2 ≤ ε 2 } , and what can be computed exactly is the integral over the cylinder { ρ ≤ ε } , so that for every x ∈ B ( n ) p ( ε ) ⊂ T p S , we can remove the contribution of ∫ z 0 f ( x , z ) dz . Then:

$$\int _ { V _ { r } ^ { + } ( \varepsilon ) } f ( X ) d V & \approx \int _ { B _ { p } ^ { n } ( \varepsilon ) } f ( X ) d V - \int _ { B _ { p } ^ { n } ( \varepsilon ) } \left [ \int _ { z = 0 } ^ { z ( \varepsilon ) } f ( x , z ( x ) ) \, d z \right ] d ^ { n } x . \\ \intertext { W e n d to f i n d t e r o r y i n t h i s a p r o x i m a t i o n . T h e v u m e i n t h e i n t e r o d } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n d t o f t h e r d o w t h e f t a r i d e r o w t h e s t a t i o n } \intertext { W e n $$

We need to fi nd the order of the error in this approximation. The volume in the second integral extends outside the ball that defines V + p ( ε ), which is inscribed in the cylinder, and thus the integral below the hypersurface is subtracting an extra contribution from the region Ω, that lies outside the sphere but inside the cylinder and is bounded by the hypersurface. Thus

$$\int _ { \Omega } f ( X ) d V o l \ \leq \ \max _ { X \in \Omega } | f ( X ) | \cdot V o l ( \Omega ) .$$

Since z ( ρ x ) ∼ O ( ρ 2 ), then max X ∈ Ω | f ( X ) | ∼ O ( ρ k ( ρ 2 ) l ). To bound the volume of Ω, notice ρ is bounded by ε from the cylinder and by approximately ε - Cε 3 from the intersection of the sphere with the hypersurface, for some constant C (cf. Lemma 5.1 below or the estimation in [2]). This maximum thickness O ( ε 3 ) is added up for every point of the base sphere, whose area is ∼ O ( ε n - 1 ). Now, the maximum height in the z direction of Ω is of order O ( ε 2 ) because it is given by the intersection of the cylinder with the hypersurface. Therefore, Vol(Ω) ∼ O ( ε 2 ε n - 1 ε 3 ) ∼ O ( ε n +4 ). The total error of this approximation is then O ( ε k +2 l + n +4 ). Finally, the graph function z ( x ) is to be approximated as a quadric, truncating the terms O ( ρ 3 ) from its Taylor series. This makes a new error in the second integral of our formula, given by the integral over the region in between the quadric and the actual hypersurface, which has height given by the O ( ρ 3 ) Therefore, the integral we are neglecting by this truncation makes an error


<!-- p:12 -->


$$\int _ { \S ^ { n - 1 } } \, \overset { \rho = \varepsilon } { \int } \mathcal { O } ( \rho ^ { k } ( \rho ^ { 2 } ) ^ { l } ) \mathcal { O } ( \rho ^ { 3 } ) \rho ^ { n - 1 } d \rho \, d \mathbb { S } \sim \mathcal { O } ( \varepsilon ^ { k + 2 l + n + 3 } )$$

which is the leading order of the two errors studied for the original integral.

Box

This type of approximations were used by [2] to obtain the fi rst integral invariant.

Proposition 4.3 (Hulin and Troyanov). The volume of the spherical component cut by a hypersurface has the asymptotic expansion, with the mean curvature H p appearing to second order:

$$V ( V _ { p } ^ { + } ( \varepsilon ) ) = \frac { V _ { n + 1 } ( \varepsilon ) } { 2 } - \frac { \varepsilon ^ { 2 } \, V _ { n } ( \varepsilon ) } { 2 ( n + 2 ) } H _ { p } + \mathcal { O } ( \varepsilon ^ { n + 3 } ) .$$

Proposition 4.4. The barycenter of the spherical component is of the form:

$$s ( V _ { p } ^ { + } ( \varepsilon ) ) = [ 0 , \dots , 0 , \ 2 \frac { V _ { n } ( \varepsilon ) } { V _ { n + 1 } ( \varepsilon ) } \frac { \varepsilon ^ { 2 } } { n + 2 } \left ( 1 + \frac { V _ { n } ( \varepsilon ) } { V _ { n + 1 } ( \varepsilon ) } \frac { \varepsilon ^ { 2 } } { n + 2 } H _ { p } \right ) ] ^ { T } \ + \mathcal { O } ( \varepsilon ^ { 3 } ) .$$

Proof. Notice that ∫ V + p ( ε ) x dVol = O ( ε n +4 ) because applying Lemma 4.2, ∫ B + p ( ε ) x d n x dz is zero, and the second integral is of monomials of odd degree. Then the normal component

$$[ V ( V _ { p } ^ { + } ( \varepsilon ) ) s ( V _ { p } ^ { + } ( \varepsilon ) ) ] _ { z } & = \int _ { \ B _ { p } ^ { + } ( \varepsilon ) } \ z \, d ^ { n } x \, d z - \int _ { \frac { 2 } { \ } } \frac { 1 } { \left [ \sum _ { \mu = 1 } ^ { n } \kappa _ { \mu } x _ { \mu } ^ { 2 } \right ] ^ { 2 } } d ^ { 2 } x + \mathcal { O } ( \varepsilon ^ { n + 4 } ) \\ & = D _ { 1 } ^ { ( n + 1 ) } + \mathcal { O } ( \varepsilon ^ { n + 4 } )$$

where we have discarded the second integral since its order is O ( D ( n ) 4 ) = O ( D ( n ) 22 ) ∼ O ( ε n +4 ), which leaves the same order O ( ε 3 ) as the error after dividing by the volume. The fi nal expression follows from inverting the volume formula and using D ( n +1) 1 from the appendix. Box Theorem 4.5. The covariance matrix C ( V + p ( ε )) has eigenvalues with the following series expansion, for all μ = 1 , . . . , n :


<!-- p:13 -->


$$\lambda _ { \mu } ( V _ { p } ^ { + } ( \varepsilon ) ) = V _ { n + 1 } ( \varepsilon ) \frac { \varepsilon ^ { 2 } } { 2 ( n + 3 ) } - V _ { n } ( \varepsilon ) \frac { \varepsilon ^ { 4 } } { 2 ( n + 2 ) ( n + 4 ) } ( 2 \kappa _ { \mu } ( p ) + H _ { p } ) + \mathcal { O } ( \varepsilon ^ { n + 5 } ) ,$$

ε

2

n

+3)

.

(15)

ε

)) =

V

n

+1

+

O

(

ε

)

ε

(

2(

n

+5

)

Moreover, in the limit ε → 0 + , when the principal curvatures are different, the corresponding eigenvectors e μ ( V + p ( ε )) converge linearly to the principal directions of S at p , and e n +1 ( V + p ( ε )) converges quadratically to the hypersurface normal vector N at p .

Proof. Working in the basis formed by the principal directions and the normal vector of the hypersurface at the fi xed point p , we shall compute the entries of the covariance matrix and see that it is diagonal to all orders smaller than O ( ε n +5 ), precisely the error we get in the diagonal elements, therefore the eigenvalues coincide with those diagonal terms up to that error since differences between eigenvalues of symmetric matrices are bounded by the matrix norm metric. The covariance matrix splits into the fi rst two terms of

$$C ( V _ { p } ^ { + } ( \varepsilon ) ) = & \int _ { V _ { p } ^ { + } ( \varepsilon ) } X \otimes X ^ { T } \, d V o l - \int _ { V _ { p } ^ { + } ( \varepsilon ) } X \otimes s ^ { T } \, d V o l - \int _ { V _ { p } ^ { + } ( \varepsilon ) } s \otimes X ^ { T } \, d V o l + \int _ { V _ { p } ^ { + } ( \varepsilon ) } s \otimes s ^ { T } \, d V o l , \\$$

because the last three terms become the same upon integration. To compute the term left we can use the expression for V s from the proof of the barycenter formula to get:

$$\int _ { V _ { p } ^ { + } ( \varepsilon ) } s \otimes s ^ { T } \, d V o l = V ( V _ { p } ^ { + } ( \varepsilon ) ) s \otimes s ^ { T } = \left [ \frac { \mathcal { O } ( \varepsilon ^ { n + 7 } ) _ { n \times n } } { \mathcal { O } ( \varepsilon ^ { n + 5 } ) _ { 1 \times n } } \Big | V ( V _ { p } ^ { + } ( \varepsilon ) ) s _ { z } ^ { 2 } \right ]$$

where V ( V + p ( ε )) s 2 z = [ D ( n +1) 1 ] 2 V ( V + p ( ε )) + O ( ε n +5 ). The other contribution to the last matrix entry is

$$e n t r y \, i s & & \int _ { V _ { p } ^ { + } ( \varepsilon ) } z ^ { 2 } \, d V o l = \int _ { B _ { p } ^ { + } ( \varepsilon ) } z ^ { 2 } \, d ^ { n } x \, d z - \frac { 1 } { 2 4 } \, \int \, \left [ \sum _ { \mu = 1 } ^ { n } \kappa _ { \mu } x _ { \mu } ^ { 2 } \right ] ^ { 3 } d ^ { n } x + \mathcal { O } ( \varepsilon ^ { n + 7 } ) \\ & & = \frac { D _ { 2 } ^ { n + 1 } } { 2 } + \mathcal { O } ( \varepsilon ^ { n + 6 } ) ,$$

in which we have neglected the second integral for being of higher order than the barycenter matrix error, whose subtraction yields the stated result for the normal eigenvalue. Notice that the other elements in the last column and row of the complete covariance matrix

V


n

(

ε

)

n

+1

2

ε

)

(

ε

4

n

+2)

V

ε

)

V

n

(

n

+1

ε

)

(

ε

2

n

+2

(

)

λ

n

+1

V

(

+

p

(

-

2

(

2

1 +

H

p


<!-- p:14 -->


are O ( ε n +5 ) since the remaining contributions come from ∫ V + p ( ε ) x μ z dVol ∼ O ( ε n +6 ), and its approximation formula has all monomials with odd powers in x .

̸

Now, we compute the tangent coordinates block. This can be done at once for any μ, ν = 1 , . . . , n , noticing that when μ = ν , the integrals of Lemma 4.2 are of monomials of odd degree in tangent coordinates so the off-diagonal elements are O ( ε n +5 ), (we use that D 4 = 3 D 22 ):

̸

$$t h a t \ D _ { 4 } & = 3 D _ { 2 2 } ) \colon \\ & \int _ { X _ { \mu } ^ { + } } x _ { \mu } ^ { 2 } \, d \text {Vol} = \int _ { B _ { \mu } ^ { + } ( \varepsilon ) } x _ { \mu } ^ { 2 } \, d ^ { n } x \, d z - \int _ { B _ { \mu } ^ { n } ( \varepsilon ) } x _ { \mu } ^ { 2 } \left ( \frac { 1 } { 2 } \sum _ { \alpha = 1 } ^ { n } \kappa _ { \alpha } x _ { \alpha } ^ { 2 } \right ) \, d ^ { n } x + \mathcal { O } ( \varepsilon ^ { n + 5 } ) \\ & = \frac { D _ { 2 } ^ { ( n + 1 ) } } { 2 } - \frac { D _ { 4 } ^ { ( n ) } } { 2 } \kappa _ { \mu } - \frac { D _ { 2 2 } ^ { ( n ) } } { 2 } \sum _ { \alpha \neq \mu } \kappa _ { \alpha } + \mathcal { O } ( \varepsilon ^ { n + 5 } ) \\ & = \frac { D _ { 2 } ^ { ( n + 1 ) } } { 2 } - \frac { D _ { 2 2 } ^ { ( n ) } } { 2 } ( 2 \kappa _ { \mu } + H _ { p } ) + \mathcal { O } ( \varepsilon ^ { n + 5 } ) . \\ \text {The perturbation theory of Hermitian matrices [34], [35] shows the convergence of}$$

̸

The perturbation theory of Hermitian matrices [34], [35] shows the convergence of the eigenvectors to the principal directions in the case of no multiplicity: truncating C ( V + p ( ε )) to order lower than O ( ε n +5 ), that is precisely the order of the perturbation with respect to the exact diagonalized matrix. Fixing an eigenvalue λ μ ( V + p ( ε )) with μ = n +1, the minimum difference to the other eigenvalues is of order ∼ ε n +4 ( κ μ - κ ν ), whereas for the last eigenvalue its distance to all the others is already at leading order ∼ ε n +3 . Therefore, from the sin θ theorem [34], the perturbation O ( ε n +5 ) changes the eigenvectors { e μ ( V + p ( ε )) } n μ =1 with respect to the principal directions as O ( ε n +5 ) / O ( ε n +4 ( κ μ - κ ν )) ∼ ε κ μ - κ ν , and changes the eigenvector e n +1 ( V + p ( ε )) with respect to the normal as O ( ε n +5 ) / O ( ε n +3 ) ∼ ε 2 , i.e., in the limit ε → 0 + the eigenvectors of C ( V + p ( ε )) get a vanishing correction with respect to the principal directions. Box

Therefore, we may write the covariance matrix as:

$$I n c e r o , & \text { we may write the covariance matrix as} . \\ & C ( V _ { p } ^ { + } ( \varepsilon ) ) = \frac { V _ { n + 1 } ( \varepsilon ) \varepsilon ^ { 2 } } { 2 ( n + 3 ) } \text { Id} _ { n + 1 } \text { } - \frac { V _ { n } ( \varepsilon ) \varepsilon ^ { 4 } } { ( n + 2 ) ( n + 4 ) } \left ( \frac { \widehat { S } + \frac { H } { 2 } \text {Id} _ { n } } { 0 _ { 1 \times n } } \right | _ { \overline { V } _ { n + 1 } ( \varepsilon ) ( n + 2 ) } ^ { 0 _ { n \times 1 } } \right ) \\ & + \mathcal { O } ( \varepsilon ^ { n + 5 } ) , \\$$

where the Weingarten operator ̂ S at p is diag( κ 1 ( p ) , . . . , κ n ( p )) in our basis.

### 5. Hypersurface patch integral invariants

Now, we shall compute the asymptotic expansions of the integral invariants of the hypersurface patch cut out by a ball centered at p and radius ε &gt; 0, i.e. over the domain D p ( ε ) = S ∩ B n +1 p ( ε ). Since a parametrization of the region is needed to perform the integrals locally, we need to fi nd local parametric equations of the boundary ∂ ( S ∩


<!-- p:15 -->


B n +1 p ( ε )) to high enough order in ε so that we can expand asymptotically the integral invariants in terms of the geometric information of the hypersurface at the point. The strategy of [20], hinted in [2], obtaining a cylindrical coordinate approximation for the boundary radius of the patch, works in general dimension as follows.

Lemma 5.1. In cylindrical coordinates ( ρ, φ 1 , . . . , φ n - 1 , z ) over the tangent space T p S , fixing the basis to the principal directions and the normal vector of S at p , the parametric equations of a point X = ( ρx 1 , . . . , ρx n , z ) T in ∂D p ( ε ) = S ∩ S n p ( ε ) , are

$$r ( \overline { x } ) & \colon = \rho ( \overline { x } _ { 1 } , \dots , \overline { x } _ { n } ) = \varepsilon - \frac { 1 } { 8 } \kappa ^ { 2 } ( \overline { x } ) \varepsilon ^ { 3 } + \mathcal { O } ( \varepsilon ^ { 4 } ) , \quad z ( \overline { x } _ { 1 } , \dots , \overline { x } _ { n } ) = \frac { 1 } { 2 } \kappa ^ { 2 } ( \overline { x } ) \varepsilon ^ { 2 } + \mathcal { O } ( \varepsilon ^ { 3 } ) , \\ \\ \\$$

where x 1 , . . . , x n are the coordinates of points on S n - 1 ⊂ T p S , and κ ( x ) = κ ( x 1 , . . . , x n ) = ∑ n μ =1 κ μ x 2 μ is the normal curvature of S at p cut by a normal plane in the direction of x .

Proof. In this coordinate system the expansion of the function that locally defines S is z ( x ) = 1 2 ∑ n μ =1 κ μ x 2 μ + O ( x 3 ) = 1 2 κ ( x ) ρ 2 + O ( ρ 3 ) since x μ = ρx μ , and because II p is diagonal in our basis with x a unit vector, the curve curvature cut by a normal plane is by Euler's formula κ ( x ) = II p ( x , x ) = ∑ n μ =1 κ μ x 2 μ . Now, a point X = ( ρx 1 , . . . , ρx n , z ) T in S ∩ S n p ( ε ) satisfies the equation of the sphere ρ 2 + z 2 = ε 2 . Substituting the expansion of z ( x ) above, we obtain 1 4 κ ( x ) 2 ρ 4 + ρ 2 - ε 2 + O ( ρ 5 ) = 0, which up to order 4 is a biquadratic equation in ρ whose positive solution is the following and leads to the mentioned approximation:

$$\rho ^ { 2 } = \frac { 2 } { \kappa ( \overline { x } ) ^ { 2 } } \left ( - 1 + \sqrt { 1 + \kappa ( \overline { x } ) ^ { 2 } \varepsilon ^ { 2 } } \right ) = \varepsilon ^ { 2 } - \frac { 1 } { 4 } \kappa ( \overline { x } ) ^ { 2 } \varepsilon ^ { 4 } + \mathcal { O } ( \varepsilon ^ { 6 } ) , \\ \intertext { a n d } \text {by outtring } \sigma \, \underset { \sigma } { a n d } \, \text {common factor } \, \sigma ^ { 2 } \, \underset { \sigma } { \text { and } } \, \text {toling} \, \text {the } \, \text {acguoro } \, \text {root} \, \text { the } \, \text {approximet} \, \text {in}$$

then by extracting a common factor ε 2 and taking the square root, the approximation expression follows. Box

The volume or mass of the domain can be expressed as a correction to the volume of the n -ball in terms of the extrinsic mean curvature H p and intrinsic curvature R p of S at the point, as it depends on the embedding. This compares to the case of the volume of a geodesic ball domain inside a manifold [1], which exhibits a correction only dependent on the intrinsic scalar curvature R p .

Proposition 5.2. The n -dimensional area of the hypersurface patch expands as

$$V ( D _ { p } ( \varepsilon ) ) = V _ { n } ( \varepsilon ) \left [ 1 + \frac { \varepsilon ^ { 2 } } { 8 ( n + 2 ) } ( H _ { p } ^ { 2 } - 2 \mathcal { R } _ { p } ) + \mathcal { O } ( \varepsilon ^ { 3 } ) \right ] .$$

Proof. Computing the induced metric tensor using Lemma 5.1, the volume around p becomes


<!-- p:16 -->


$$d V o l | _ { D _ { p } ( \varepsilon ) } = \sqrt { \det g ( x ) } \, d x _ { 1 } \cdots d x _ { n } = \left [ 1 + \frac { 1 } { 2 } \sum _ { \mu = 1 } ^ { n } \kappa _ { \mu } ^ { 2 } x _ { \mu } ^ { 2 } + \mathcal { O } ( x ^ { 3 } ) \right ] d x _ { 1 } \cdots d x _ { n } ,$$

since ‖∇ z ( x ) ‖ 2 can be considered small for small enough ε &gt; 0, because in our coordinates ∇ z ( 0 ) = 0. With this and the cylindrical measure, eq. (A.1), the integration becomes

$$b \text { becomes} \\ V ( D _ { p } ( \varepsilon ) ) & = \int _ { \mathbb { S } ^ { n } B ^ { n + 1 } ( \varepsilon ) } d V o l = \int _ { \mathbb { S } ^ { n - 1 } } d \mathbb { S } \, \int _ { 0 } ^ { \pi ( \mathbb { X } ) } \left [ 1 + \frac { 1 } { 2 } \sum _ { \mu = 1 } ^ { n } \kappa _ { \mu } ^ { 2 } \rho ^ { \frac { 2 } { x } } _ { x } + \mathcal { O } ( \rho ^ { 3 } ) \right ] \rho ^ { n - 1 } \, d \rho \\ & = \int _ { \mathbb { S } } d \mathbb { S } \left [ \frac { 1 } { n } ( \varepsilon - \frac { \kappa ( \overline { x } ) ^ { 2 } \varepsilon ^ { 3 } } { 8 } + \mathcal { O } ( \varepsilon ^ { 4 } ) ) ^ { n } \right ] \\ & \quad s s ^ { n - 1 } \\ & \quad + \frac { 1 } { 2 } \sum _ { \mu = 1 } ^ { n } \kappa _ { \mu } ^ { 2 } \overline { x } _ { \mu } ^ { 2 } ( \varepsilon - \frac { \kappa ( \overline { x } ) ^ { 2 } \varepsilon ^ { 3 } } { 8 } + \mathcal { O } ( \varepsilon ^ { 4 } ) ) ^ { n + 2 } + \mathcal { O } ( \varepsilon ^ { n + 4 } ) \right ] \\ \intertext { a t h e r g i n t a g r u p o t h e w t h o r d u a n d y r a d i u s . $ E p a n d i m o n i a l $ s e r i n d }$$

after integrating over ρ up to the boundary radius. Expanding the binomial series and the square of the normal curvature, all the remaining integrals are in Theorem A.4, leading to

$$\text {leading to} \\ V ( D _ { p } ( \varepsilon ) ) = V _ { n } ( \varepsilon ) - \frac { \varepsilon ^ { n + 2 } } { 8 } \int d \mathbb { S } \left [ \sum _ { \mu = 1 } ^ { n } \kappa _ { \mu } ^ { 2 } \overline { x } _ { \mu } ^ { 4 } + 2 \sum _ { \mu < \nu } ^ { n } \kappa _ { \mu } \kappa _ { \nu } \overline { x } _ { \mu } ^ { 2 } \overline { x } _ { \nu } ^ { 2 } \right ] + \frac { C _ { 2 } \varepsilon ^ { n + 2 } } { 2 ( n + 2 ) } \sum _ { \mu = 1 } ^ { n } \kappa _ { \mu } ^ { 2 } \\ + \mathcal { O } ( \varepsilon ^ { n + 3 } ) \\ = V _ { n } ( \varepsilon ) + \frac { \varepsilon ^ { n + 2 } } { n + 2 } \left [ \left ( \frac { C _ { 2 } } { 2 } - \frac { n + 2 } { 8 } C _ { 4 } \right ) \sum _ { \mu = 1 } ^ { n } \kappa _ { \mu } ^ { 2 } - C _ { 2 2 } \frac { n + 2 } { 8 } 2 \sum _ { \mu < \nu } ^ { n } \kappa _ { \mu } \kappa _ { \nu } \right ] \\ + \mathcal { O } ( \varepsilon ^ { n + 3 } ) , \\ \intertext { w h e r e the f i n a l e x p r e s i g n o w i n p o r e c o n g i n z i g h e n a n d s c a l r a c u r v a t u r e }$$

where the fi nal expression is obtained upon recognizing the mean and scalar curvature in terms of the principal curvatures, and using the relations among the coefficients from the appendix. Box

The center of mass in this case turns out to deviate, to leading order in ε , only in the normal direction with respect to the center of the ball.

Proposition 5.3. The barycenter of the patch region has coordinates in the principal basis with respect to p given by

$$s ( D _ { p } ( \varepsilon ) ) = [ \mathcal { O } ( \varepsilon ^ { 4 } ) , \dots , \mathcal { O } ( \varepsilon ^ { 4 } ) , \, \frac { \varepsilon ^ { 2 } } { 2 ( n + 2 ) } H _ { p } + \mathcal { O } ( \varepsilon ^ { 3 } ) \, ] ^ { T } .$$


<!-- p:17 -->


Proof. When integrating any tangent component x α of X , only factors with an odd power in some components are produced because the computable terms (see previous proof) now contain products x α x 2 μ , x α x 4 μ and x α x 2 μ x 2 ν , which always have an odd power factor regardless of the subindices combination. Therefore the fi rst n components of V ( D p ( ε )) s ( D p ( ε )) are of order O ( ε n +4 ), coming from the error inside r ( x ) n +1 after integrating radially the fi rst term x α ρ n - 1 dρ . The normal component of X integrates as

$$& \int _ { S ^ { n + 1 } } z \, d \text {Vol} = \int _ { \real } d S \, \int _ { 0 } ^ { \real } \left [ \frac { r ^ { \chi } } { 2 } ( \kappa ^ { ( \overline { \chi } ) } \rho ^ { 2 } + \mathcal { O } ( \rho ^ { 3 } ) ) \right ] \left [ 1 + \frac { 1 } { 2 } \sum _ { \mu = 1 } ^ { n } \kappa ^ { 2 } _ { \mu } \rho ^ { 2 } _ { \mu } + \mathcal { O } ( \rho ^ { 3 } ) \right ] \rho ^ { n - 1 } \, d \rho \\ & = \int _ { S ^ { n - 1 } } d S \left [ \frac { \kappa ( \overline { \chi } ) } { 2 ( n + 2 ) } ( \varepsilon - \frac { \kappa ( \overline { \chi } ) ^ { 2 } } { 8 } \varepsilon ^ { 3 } + \mathcal { O } ( \varepsilon ^ { 4 } ) ) ^ { n + 2 } + \mathcal { O } ( \varepsilon ^ { n + 3 } ) \right ] = C _ { 2 } \frac { \varepsilon ^ { n + 2 } } { 2 ( n + 2 ) } \, H _ { p } + \mathcal { O } ( \varepsilon ^ { n + 3 } ) . \\ & \quad \text {This is a following line} \, n \, \text {th} \, \omega \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \, \exp ( \chi ) \,$$

Then normalizing by the volume to lowest order cancels the coefficient C 2 ε n . Box

Finally, the study of the covariance matrix of the patch domain shows a behavior similar to the spherical component, but where the next-to-leading order contribution to the eigenvalues includes only products of principal curvatures and no linear terms on them.

Theorem 5.4. The covariance matrix C ( D p ( ε )) has n eigenvalues that scale like ε n +2 as

$$\lambda _ { \mu } ( D _ { p } ( \varepsilon ) ) = V _ { n } ( \varepsilon ) \left [ \frac { \varepsilon ^ { 2 } } { n + 2 } + \frac { \varepsilon ^ { 4 } } { 8 ( n + 2 ) ( n + 4 ) } ( H _ { p } ^ { 2 } - 2 \mathcal { R } _ { p } - 4 H _ { p } \kappa _ { \mu } ( p ) ) \right ] + \mathcal { O } ( \varepsilon ^ { n + 5 } ) ,$$

for all μ = 1 , . . . , n , and one eigenvalue scaling as ε n +4 with leading term

$$\lambda _ { n + 1 } ( D _ { p } ( \varepsilon ) ) = V _ { n } ( \varepsilon ) \frac { \varepsilon ^ { 4 } } { 2 ( n + 2 ) ( n + 4 ) } \left ( \frac { n + 1 } { n + 2 } H _ { p } ^ { 2 } - \mathcal { R } _ { p } \right ) + \mathcal { O } ( \varepsilon ^ { n + 5 } ) .$$

Moreover, in the limit ε → 0 + , if the principal curvatures at p are all different, the eigenvectors e μ ( D p ( ε )) corresponding to the fi rst n eigenvalues converge to the principal directions of S at p , and the last eigenvector e n +1 ( D p ( ε )) converges to the hypersurface normal vector N ( p ) .

Proof. We need to evaluate ∫ D p ( ε ) X ( x ) ⊗ X ( x ) T √ det g d n x and V ( D p ( ε )) s ( D p ( ε )) ⊗ s ( D p ( ε )) T . The latter can be obtained from the previous proof:

$$[ \mathcal { O } ( \varepsilon ^ { n + 4 } ) , \dots , \mathcal { O } ( \varepsilon ^ { n + 4 } ) , \, \frac { C _ { 2 } \varepsilon ^ { n + 2 } } { 2 ( n + 2 ) } H _ { p } + \mathcal { O } ( \varepsilon ^ { n + 3 } ) ] ^ { T } \\ \otimes [ \mathcal { O } ( \varepsilon ^ { 4 } ) , \dots , \mathcal { O } ( \varepsilon ^ { 4 } ) , \frac { \varepsilon ^ { 2 } } { 2 ( n + 2 ) } H _ { p } + \mathcal { O } ( \varepsilon ^ { 3 } ) ] ,$$


<!-- p:18 -->


resulting in all entries of the n × n block being O ( ε n +8 ), the fi rst n elements of the last column and last row being O ( ε n +6 ), and the last element of the matrix becoming

$$[ V ( D _ { p } ( \varepsilon ) ) s ( D _ { p } ( \varepsilon ) ) \otimes s ( D _ { p } ( \varepsilon ) ) ^ { T } ] _ { ( n + 1 ) , ( n + 1 ) } = \frac { V _ { n } ( \varepsilon ) \, \varepsilon ^ { 4 } } { 4 ( n + 2 ) ^ { 2 } } H _ { p } ^ { 2 } + \mathcal { O } ( \varepsilon ^ { n + 5 } ) ,$$

(we already disregarded the term of O ( ε n +6 ) that can be computed for this matrix entry because, as shown below, the other contributing term in that position has error O ( ε n +5 )).

Now, the rest of the covariance matrix requires the longest computations so far. The entries of X ( x ) ⊗ X ( x ) T are of three types: x μ x ν , x μ z ( x ) and z ( x ) 2 . The fi rst n entries of the last column and last row, x μ z ( x ), contribute at order O ( ε n +4 ). This implies that the matrix may not decompose at order O ( ε n +4 ) as direct sum of a 'tangent' n × n block, the integrals of [ x μ x ν ], and a 'normal' 1 × 1 block, the integral of z ( x ) 2 . Hence, the argument in the proof of Theorem 4.5 to equate the diagonal elements of this expansion with that of the actual eigenvalues cannot be made here, since there are off-diagonal error elements at the same order as the diagonal approximation. Nevertheless, one can show, cf. [30], how these do not affect the eigenvalues at the order we are interested in by writing the eigenvalue-eigenvector equation as a series expansion order-by-order, which is always possible and converges for Hermitian matrices of converging power series elements [36], such as our C ( D p ( ε )):

$$& [ \ a \varepsilon ^ { 2 } \left ( \frac { \text {Id} _ { n } } { 0 _ { 1 \times n } } \Big | _ { 0 } \frac { 0 _ { n \times 1 } } { 0 } \right ) + b \varepsilon ^ { 4 } \left ( \frac { A _ { n \times n } } { B _ { 1 \times n } } \Big | _ { \ C } \frac { B _ { n \times 1 } } { \ C } \right ) + \mathcal { O } ( \varepsilon ^ { 5 } ) \Big ] [ V ^ { ( 0 ) } + V ^ { ( 1 ) } \varepsilon + V ^ { ( 2 ) } \varepsilon ^ { 2 } + \dots ] = \\ & = ( \lambda ^ { ( 1 ) } \varepsilon ^ { 1 } + \lambda ^ { ( 2 ) } \varepsilon ^ { 2 } + \lambda ^ { ( 3 ) } \varepsilon ^ { 3 } + \lambda ^ { ( 4 ) } \varepsilon ^ { 4 } + \dots ) [ V ^ { ( 0 ) } + V ^ { ( 1 ) } \varepsilon + V ^ { ( 2 ) } \varepsilon ^ { 2 } + \dots ] .$$

Therefore, expanding the components of C ( D p ( ε )) shall yield exactly the actual eigenvalues to order O ( ε n +4 ). The last matrix element expands the integrals into the following terms

$$\text {terms} \\ \int _ { \mathcal { S } \cap B ^ { n + 1 } _ { p } ( \varepsilon ) } \frac { 1 } { 4 } \left [ \sum _ { \alpha = 1 } ^ { n } \kappa _ { \alpha } ^ { 2 } \int \frac { \overline { x } _ { \alpha } ^ { 4 } } { x _ { \alpha } ^ { 4 } } \, d \mathbb { S } + 2 \sum _ { \alpha < \beta } ^ { n } \kappa _ { \alpha } \kappa _ { \beta } \int \frac { \overline { x } _ { \alpha } ^ { 2 } \overline { x } _ { \beta } ^ { 2 } } { x _ { \alpha } ^ { 2 } \overline { x } _ { \beta } ^ { 2 } } \, d \mathbb { S } \right ] \frac { \varepsilon ^ { n + 4 } } { n + 4 } + \mathcal { O } ( \varepsilon ^ { n + 5 } ) \\ = \frac { \varepsilon ^ { n + 4 } } { 4 ( n + 4 ) } \left [ C _ { 4 } ( H _ { p } ^ { 2 } - \mathcal { R } _ { p } ) + C _ { 2 2 } \mathcal { R } _ { p } \right ] + \mathcal { O } ( \varepsilon ^ { n + 5 } ) , \\ \intertext { w h e r o f s u b r a t i c g h e t s } \text {where} \quad \text {the barycenter matrix contribution, the last eigenvalue becomes}$$

whereof subtracting the barycenter matrix contribution, the last eigenvalue becomes

$$\lambda _ { n + 1 } ( p , \varepsilon ) = \frac { C _ { 2 } \varepsilon ^ { n + 4 } } { 4 ( n + 2 ) ( n + 4 ) } \left [ 3 H _ { p } ^ { 2 } - 2 \mathcal { R } _ { p } \right ] - \frac { C _ { 2 } \varepsilon ^ { n + 4 } } { 4 ( n + 2 ) ^ { 2 } } H _ { p } ^ { 2 } + \mathcal { O } ( \varepsilon ^ { n + 5 } ) . \\ \\ \intertext { T h o \cdots t e r n o n t " " b l o c k e w t r i o n v e b o o m u n t o o d \, i s u m t e n o w o u c l y f o r e w a u v - 1 }$$

The 'tangent' block entries can be computed simultaneously for any μ, ν = 1 , . . . , n :


<!-- p:19 -->


̸


$$J . \ A l w e z \cdot V i z o s o e \, t a l . \, / \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \$$

̸


where the δ μν appears because the monomials get an odd power if μ = ν . Now, the different integrals inside the indexed sums result in different constants depending on the different monomials that the terms x 2 μ x 4 α and x 2 μ x 2 α x 2 β can combine into, and after some algebraic manipulations the above integral is equal to

̸

$$\L a g b r a i { \text { manipulations the above integral is equal to} } \\ C _ { 2 } \frac { \varepsilon ^ { n + 2 } } { n + 2 } \delta _ { \mu \nu } + \frac { \varepsilon ^ { n + 4 } } { n + 4 } \delta _ { \mu \nu } \left [ ( \frac { C _ { 4 } } { 2 } - \frac { n + 4 } { 8 } C _ { 6 } ) \kappa _ { \mu } ^ { 2 } + ( \frac { C _ { 2 2 } } { 2 } - \frac { n + 4 } { 8 } C _ { 2 4 } ) \sum _ { \alpha \neq \mu } \kappa _ { \alpha } ^ { 2 } \\ - \frac { n + 4 } { 8 } ( 2 C _ { 2 4 } \sum _ { \alpha \neq \mu } \kappa _ { \mu } \kappa _ { \alpha } + C _ { 2 2 } \sum _ { \alpha \neq \beta } \kappa _ { \alpha \beta } ) \, + \mathcal { O } ( \varepsilon ^ { n + 5 } ) . \\ \\ \text {Notice that the summations in the last equation are all over indices that must be different} \\ \text {from } \omega \subsetneq \omega \subsetneq \omega \text { and subtract the corresponding missing terms to those sums as long}$$

̸

Notice that the summations in the last equation are all over indices that must be different from μ , so we can add and subtract the corresponding missing terms to those sums as long as we subtract them in the correct place. Doing this, and using the crucial relationships between the constants from the appendix, each of the different terms under the big braces simplify to:

̸

$$\text {lifty to:} \\ & ( \frac { C _ { 4 } } { 2 } - \frac { n + 4 } { 8 } C _ { 6 } - \frac { C _ { 2 2 } } { 2 } + \frac { n + 4 } { 8 } C _ { 2 4 } ) \kappa _ { \mu } ^ { 2 } = - \frac { C _ { 2 } } { 2 ( n + 2 ) } \kappa _ { \mu } ^ { 2 } ( p ) , \\ & ( \frac { C _ { 2 2 } } { 2 } - \frac { n + 4 } { 8 } C _ { 2 4 } ) \sum _ { \alpha = 1 } ^ { n } \kappa _ { \alpha } ^ { 2 } = \frac { C _ { 2 } } { 8 ( n + 2 ) } ( H _ { p } ^ { 2 } - \mathcal { R } _ { p } ) , \\ & - \frac { n + 4 } { 8 } ( ( 2 C _ { 2 4 } - 2 C _ { 2 2 2 } ) \sum _ { \alpha \neq \mu } ^ { n } \kappa _ { \mu } \kappa _ { \alpha } + 2 C _ { 2 2 2 } \sum _ { \alpha < \beta } ^ { n } \kappa _ { \alpha } \kappa _ { \beta } ) \\ & = - \frac { C _ { 2 } } { 2 ( n + 2 ) } R _ { \mu \mu } ( p ) + \frac { C _ { 2 } } { 8 ( n + 2 ) } \mathcal { R } _ { p } , \\ \text {lling that the diagonal components of the Ricci tensor for hypersurfaces are } R _ { \mu } ( \sigma )$$

̸

recalling that the diagonal components of the Ricci tensor for hypersurfaces are R μμ ( p ) = ∑ n α = μ κ α ( p ) κ μ ( p ), and the scalar curvature is R p = 2 ∑ n μ&lt;ν κ μ ( p ) κ ν ( p ). Finally, these add up into the expression


<!-- p:20 -->


$$\int x _ { \mu } x _ { \nu } d V & = \delta _ { \mu \nu } V _ { n } ( \varepsilon ) \left [ \frac { \varepsilon ^ { 2 } } { n + 2 } + \frac { \varepsilon ^ { 4 } } { 8 ( n + 2 ) ( n + 4 ) } ( H _ { p } ^ { 2 } - 2 \mathcal { R } _ { p } - 4 \kappa _ { \mu } ^ { 2 } - 4 R _ { \mu \mu } ) \right ] \\ & + \mathcal { O } ( \varepsilon ^ { n + 5 } ) ,$$

and since κ 2 μ ( p ) + R μμ ( p ) = κ μ ( p ) H p the stated formula for the tangent eigenvalues follows from the diagonal of this block. Therefore, we can write C ( D + p ( ε )) =

$$\frac { V _ { n } ( \varepsilon ) \, \varepsilon ^ { 2 } } { n + 2 } \left ( \frac { \text {Id} _ { n } } { 0 _ { 1 \times n } } \left | \, 0 _ { n \times 1 } \right ) + \frac { V _ { n } ( \varepsilon ) \, \varepsilon ^ { 4 } } { 2 ( n + 2 ) ( n + 4 ) } \left ( \frac { \frac { H ^ { 2 } - 2 \mathcal { R } } { 4 } \text {Id} _ { n } - H _ { p } \, \widehat { S } } { A _ { 1 \times n } } \right | \, \frac { A _ { n \times 1 } } { \frac { n + 1 } { n + 2 } H _ { p } ^ { 2 } - \mathcal { R } _ { p } } \right ) + \mathcal { O } ( \varepsilon ^ { n + 5 } ) , \\ \\ + \, \text {W} \colon \quad + \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \quad \cdot \$$

so the Weingarten operator appears inside the covariance matrix in this case as well.

### 6. Multi-scale curvature descriptors

By solving the second term in the expansion from our integral invariants, we can extract the curvature information they encode and write it in terms of the volume and eigenvalues at a fi xed scale. This means that these local statistical measurements of the underlying point set can be employed to reconstruct or estimate its differential geometry, e.g., from a discrete sample cloud of points. These estimators can be used in geometry processing to ignore details below a given scale and act as feature detectors.

Employing the asymptotic expressions of section 4, we invert the relations and solve for the principal curvatures.

Corollary 6.1. Abbreviating the integral invariants of the spherical component as λ μ ( p, ε ) ≡ λ μ ( V + p ( ε )) , V p ( ε ) ≡ V ( V + p ( ε )) , then the corresponding descriptors of the principal curvatures, at scale ε &gt; 0 and point p ∈ S , are given by

̸

$$\kappa _ { \mu } ( V _ { p } ^ { + } ( \varepsilon ) ) = \frac { n + 4 } { \varepsilon ^ { 4 } V _ { n } ( \varepsilon ) } \left [ \frac { \varepsilon ^ { 2 } V _ { n + 1 } ( \varepsilon ) } { n + 3 } - ( n + 1 ) \lambda _ { \mu } ( p , \varepsilon ) + \sum _ { \alpha \neq \mu } ^ { n } \lambda _ { \alpha } ( p , \varepsilon ) \right ] , \quad ( 2 1 ) \\ \intertext { o r e q u i v a l e n t l y , u s i n g t h e m e a n c u r v a t u r e $ H , b y $ }$$

or equivalently, using the mean curvature H , by

$$H ( V _ { p } ^ { + } ( \varepsilon ) ) & = \frac { ( n + 2 ) V _ { n + 1 } ( \varepsilon ) } { \varepsilon ^ { 2 } V _ { n } ( \varepsilon ) } \left ( 1 - 2 \, \frac { V _ { p } ( \varepsilon ) } { V _ { n + 1 } ( \varepsilon ) } \right ) , \\ & \quad ( n \, \downarrow \, 2 ) ( n \, \downarrow \, 4 ) \, \left ( c ^ { 2 } V _ { n } ( \varepsilon ) \right ) \, ,$$

$$\varepsilon ^ { 4 } v _ { n } ( \varepsilon ) \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { }$$

with corresponding errors | H p - H ( V + p ( ε )) | ≤ O ( ε ) , and | κ μ ( p ) - κ μ ( V + p ( ε )) | ≤ O ( ε ) , for any μ = 1 , . . . , n . The eigenvectors e μ ( V + p ( ε )) and e n +1 ( V + p ( ε )) are descriptors of the principal and normal directions respectively.

Box Proof. Let us define the coefficients a = ε 2 V n +1 ( ε ) 2( n +3) , b = - ε 4 V n ( ε ) 2( n +2)( n +4) , then the tangent eigenvalues from eq. (14) solve the principal curvatures


<!-- p:21 -->


$$\kappa _ { \mu } = \frac { \lambda _ { \mu } - a } { 2 b } - \frac { 1 } { 2 } H _ { p } + \mathcal { O } ( \varepsilon ) .$$

Fixing one μ = 1 , . . . , n , and subtracting any two such equations with μ = α results in

$$\kappa _ { \alpha } = \frac { \lambda _ { \alpha } - \lambda _ { \mu } } { 2 b } + \kappa _ { \mu } + \mathcal { O } ( \varepsilon ) ,$$

and inserting this into the definition of H yields

̸


$$\kappa _ { \mu } ( V _ { p } ^ { + } ( \varepsilon ) ) & = \frac { \lambda _ { \mu } - a } { b ( n + 2 ) } - \sum _ { \alpha \neq \mu } ^ { n } \frac { \lambda _ { \alpha } - \lambda _ { \mu } } { 2 b ( n + 2 ) } = \frac { 1 } { 2 b ( n + 2 ) } \left ( - 2 a + ( n + 1 ) \lambda _ { \mu } - \sum _ { \alpha \neq \mu } ^ { n } \lambda _ { \alpha } \right ) . \\ \\ \text {The truncation error is given by the order of } \mathcal { O } ( \varepsilon ^ { n + 5 } ) / b \sim \mathcal { O } ( \varepsilon ) \text {, Alternatively, one can}$$

The truncation error is given by the order of O ( ε n +5 ) /b ∼ O ( ε ). Alternatively, one can solve the Hulin-Troyanov relation, eq. (12), to obtain a descriptor of H p , and then use this in the expression of κ μ in terms of λ μ and H above. Box

An analogous inversion process can be carried out with the series expansions of section 5.

Corollary 6.2. Denoting by λ ( p, ε ) ≡ λ ( D p ( ε )) , V p ( ε ) ≡ V ( D p ( ε )) the integral invariants of the hypersurface patch domain, then the corresponding curvature descriptors at scale ε &gt; 0 and point p ∈ S , for any μ = 1 , . . . , n , are

$$\mathcal { R } ( D _ { p } ^ { + } ( \varepsilon ) ) = 2 ( n + 2 ) ^ { 2 } ( n + 4 ) \frac { \lambda _ { n + 1 } ( p , \varepsilon ) } { n \varepsilon ^ { 4 } V _ { n } ( \varepsilon ) } - \frac { 8 ( n + 1 ) ( n + 2 ) } { n \varepsilon ^ { 2 } } \left ( \frac { V _ { p } ( \varepsilon ) } { V _ { n } ( \varepsilon ) } - 1 \right ) \quad ( 2 4 )$$

$$\bar { V } \quad \bar { V } _ { n } ( \varepsilon ) = \frac { 2 ( n + 2 ) } { \varepsilon ^ { 2 } H ( D _ { p } ^ { + } ( \varepsilon ) ) } \left [ \frac { V _ { p } ( \varepsilon ) } { V _ { n } ( \varepsilon ) } + \frac { n + 4 } { \varepsilon ^ { 2 } } \left ( \frac { \varepsilon ^ { 2 } } { n + 2 } - \frac { \lambda _ { \mu } ( p , \varepsilon ) } { V _ { n } ( \varepsilon ) } \right ) - 1 \right ] ,$$

$$H ( D _ { p } ^ { + } ( \varepsilon ) ) = ( \pm ) \sqrt { 4 ( n + 2 ) ^ { 2 } ( n + 4 ) \frac { \lambda _ { n + 1 } ( p , \varepsilon ) } { n \varepsilon ^ { 4 } V _ { n } ( \varepsilon ) } } + \frac { 8 ( n + 2 ) ^ { 2 } } { n \varepsilon ^ { 2 } } \left ( 1 - \frac { V _ { p } ( \varepsilon ) } { V _ { n } ( \varepsilon ) } \right ) , \quad ( 2 5 ) \\$$

where the overall sign can be chosen by fi xing a normal orientation from

$$( \pm ) = s g n \langle e _ { n + 1 } ( D _ { p } ( \varepsilon ) ) , \, s ( D _ { p } ( \varepsilon ) ) \rangle .$$

The eigenvectors e μ ( D p ( ε )) and e n +1 ( D p ( ε )) are descriptors of the principal and normal directions respectively. The corresponding errors are | H 2 p - H ( D p ( ε )) 2 | ≤ O ( ε ) , |R p - R ( D p ( ε )) | ≤ O ( ε ) , and | κ 2 μ ( p ) - κ μ ( D p ( ε )) 2 | ≤ O ( ε ) .

̸


<!-- p:22 -->


Proof. By solving the second term in eq. (17) and eq. (20), let us define coefficients

$$A = \frac { 8 ( n + 2 ) } { \varepsilon ^ { 2 } } \left ( \frac { V _ { p } ( \varepsilon ) } { V _ { n } ( \varepsilon ) } - 1 \right ) + \mathcal { O } ( \varepsilon ) , \quad B = 2 ( n + 2 ) ( n + 4 ) \frac { \lambda _ { n + 1 } ( p , \varepsilon ) } { \varepsilon ^ { 4 } V _ { n } ( \varepsilon ) } + \mathcal { O } ( \varepsilon ) ,$$

so that we have the system of equations A = H 2 p - 2 R p , B = n +1 n +2 H 2 p - R p , whose solution is

$$\mathcal { R } _ { p } = \frac { 1 } { n } ( ( n + 2 ) B - ( n + 1 ) A ) , \ \ H _ { p } ^ { 2 } = \frac { ( n + 2 ) } { n } ( 2 B - A ) .$$

We can approximate the normal direction and orientation by using e n +1 ( p, ε ), and since the barycenter eq. (18) has normal component with leading order in terms of H p , their mutual projection can serve to fi x the orientation and overall relative sign of all the principal curvatures. The principal curvatures themselves are then solved from eq. (19) substituting the value of H p above, resulting in κ μ = 1 ( A Γ μ ), where

4 H p -

$$\Gamma _ { \mu } = \frac { 8 ( n + 2 ) ( n + 4 ) } { \varepsilon ^ { 4 } } \left ( \frac { \lambda _ { \mu } ( p , \varepsilon ) } { V _ { n } ( \varepsilon ) } - \frac { \varepsilon ^ { 2 } } { n + 2 } \right ) + \mathcal { O } ( \varepsilon ) .$$

The errors follow straightforwardly by the truncation of A, B, Γ μ . Box

In the spirit of the limit formula obtained in [6] for regular curves in R n , relating ratios of the covariance eigenvalues to the Frenet-Serret curvatures, we also state here analogous expressions for hypersurfaces using the ratios of the covariance eigenvalues, whose proofs are straightforward.

Corollary 6.3. Let p ∈ S and consider the spherical component invariants. Then for any μ, ν = 1 , . . . , n , the fi rst n eigenvalues, λ μ ( p, ε ) ≡ λ μ ( V + p ( ε )) , of the covariance matrix C ( V + p ( ε )) satisfy the following limit ratio:

$$\lim _ { \varepsilon \to 0 ^ { + } } \frac { V _ { n + 1 } ^ { 2 } ( \varepsilon ) } { V _ { n } ( \varepsilon ) } \frac { \lambda _ { \mu } ( p , \varepsilon ) - \lambda _ { \nu } ( p , \varepsilon ) } { \lambda _ { \mu } ( p , \varepsilon ) \lambda _ { \nu } ( p , \varepsilon ) } = \frac { 4 ( n + 3 ) ^ { 2 } } { ( n + 2 ) ( n + 4 ) } [ \kappa _ { \nu } ( p ) - \kappa _ { \mu } ( p ) ] .$$

Corollary 6.4. Let p ∈ S and consider the hypersurface patch invariants. Then for any μ, ν = 1 , . . . , n , the fi rst n eigenvalues, λ μ ( p, ε ) ≡ λ μ ( D p ( ε )) , of the covariance matrix C ( D p ( ε )) satisfy the following limit ratio:

$$\lim _ { \varepsilon \to 0 ^ { + } } V _ { n } ( \varepsilon ) \frac { \lambda _ { \mu } ( p , \varepsilon ) - \lambda _ { \nu } ( p , \varepsilon ) } { \lambda _ { \mu } ( p , \varepsilon ) \lambda _ { \nu } ( p , \varepsilon ) } = \frac { n + 2 } { 2 ( n + 4 ) } [ \kappa _ { \nu } ( p ) - \kappa _ { \mu } ( p ) ] H _ { p } ,$$

and the last eigenvalue satisfies:


<!-- p:23 -->


$$\lim _ { \varepsilon \to 0 ^ { + } } V _ { n } ( \varepsilon ) \frac { \lambda _ { n + 1 } ( p , \varepsilon ) } { \lambda _ { \mu } ( p , \varepsilon ) \lambda _ { \nu } ( p , \varepsilon ) } = \frac { n + 2 } { 2 ( n + 4 ) } \left [ \frac { n + 1 } { n + 2 } H _ { p } ^ { 2 } - \mathcal { R } _ { p } \right ] .$$

These ratios can be used as well to define descriptors solving for the curvature variables aided by the volume descriptor, like in the preceding corollaries.

### 7. Conclusions

In this paper we have generalized major PCA methods and results known for surfaces in space to establish the asymptotic relationship between integral invariants and the principal curvatures and principal directions of hypersurfaces of any dimension, which furnishes a method to obtain geometric descriptors at any given scale using the eigenvalue decomposition of the covariance matrix. We have seen that these methods are sufficient to provide also estimators of the Riemann curvature tensor of embedded submanifolds of higher-codimension, using its hypersurface projections onto the linear subspaces in ambient space spanned by the tangent space and each of the normal vectors from an orthonormal basis. These results establish a theoretical foundation for the implementation of the computational integral invariant approach to study the geometry of point clouds of high dimensionality, which should be a helpful tool for manifold learning and geometry processing.

#### Declaration of competing interest

The authors declare that they have no known competing fi nancial interests or personal relationships that could have appeared to influence the work reported in this paper.

### Acknowledgements

We would like to thank Louis Scharf for very helpful discussions during the writing of this paper. This paper is based on research partially supported by the National Science Foundation under Grants No. DMS-1513633, and DMS-1322508.

### Appendix A. Integration of monomials over spheres

Let x = ( x 1 , . . . , x n ) ∈ R n , and denote the sphere and ball of radius ε in R n by:

$$\mathbb { S } ^ { n - 1 } ( \varepsilon ) = \{ x \in \mathbb { R } ^ { n } \colon \| x \| = \varepsilon \} , \ \ B ^ { n } ( \varepsilon ) = \{ x \in \mathbb { R } ^ { n } \colon \| x \| \leq \varepsilon \} ,$$

where we set S n - 1 = S n - 1 (1). Using generalized spherical coordinates ( r, φ 1 , . . . , φ n - 1 ), where r = ‖ x ‖ , x μ = x μ /r ∈ S n - 1 , i.e.,

$$\bar { x } _ { 1 } = \cos \phi _ { 1 } , \dots , \ \bar { x } _ { n - 1 } = \sin \phi _ { 1 } \cdots \sin \phi _ { n - 2 } \cos \phi _ { n - 1 } , \ \bar { x } _ { n } = \sin \phi _ { 1 } \cdots \sin \phi _ { n - 2 } \sin \phi _ { n - 1 } ,$$


<!-- p:24 -->


the Euclidean measure over the unit sphere and ball of any radius can be written as

$$d \mathbb { S } ^ { n - 1 } = d \phi _ { n - 1 } \prod _ { \mu = 1 } ^ { n - 2 } \sin ^ { n - 1 - \mu } ( \phi _ { \mu } ) d \phi _ { \mu } , \quad d ^ { n } B = d x _ { 1 } \cdots d x _ { n } = r ^ { n - 1 } d r \ d \mathbb { S } ^ { n - 1 } .$$

Definition A.1. For any integers α 1 , . . . , α n ∈ { 0 , 1 , 2 , . . . } , the integrals of the monomials x α 1 1 · · · x α n n over the unit sphere and the ball of radius ε are denoted by:

$$C _ { \alpha _ { 1 } \dots \alpha _ { n } } ^ { ( n ) } = \int _ { \mathbb { S } ^ { n - 1 } } \, x _ { 1 } ^ { \alpha _ { 1 } } \cdots x _ { n } ^ { \alpha _ { n } } \, d \mathbb { S } ^ { n - 1 } , \quad D _ { \alpha _ { 1 } \dots \alpha _ { n } } ^ { ( n ) } = \int _ { B ^ { n } ( \varepsilon ) } \, x _ { 1 } ^ { \alpha _ { 1 } } \cdots x _ { n } ^ { \alpha _ { n } } \, d ^ { n } B . \quad ( A . 2 )$$

These can be computed directly in spherical coordinates by collecting factors and separating the integrals into a product of integrals of powers of sines and cosines which can be given in terms of the Beta function, that then telescopes and simplifies; other shorter proof uses the usual exponential trick, see for example [37], resulting in the following formula.

Theorem A.2. Denoting β μ = 1 2 ( α μ +1) , the values of the integrals eq. (A.2) over spheres are

$$C _ { \alpha _ { 1 } \dots \alpha _ { n } } ^ { ( n ) } = \begin{cases} 0 , & \text {if some $\alpha_{\mu}$ is odd,} \\ 2 \frac { \Gamma ( \beta _ { 1 } ) \Gamma ( \beta _ { 2 } ) \cdots \Gamma ( \beta _ { n } ) } { \Gamma ( \beta _ { 1 } + \beta _ { 2 } + \cdots + \beta _ { n } ) } , & \text {if all $\alpha_{\mu}$ are even,} \end{cases}$$

and the integrals over balls become

$$D _ { \alpha _ { 1 } \dots \alpha _ { n } } ^ { ( n ) } = \frac { \varepsilon ^ { n + ( \alpha _ { 1 } + \cdots + \alpha _ { n } ) } } { n + ( \alpha _ { 1 } + \cdots + \alpha _ { n } ) } \, C _ { \alpha _ { 1 } \dots \alpha _ { n } } ^ { ( n ) } .$$

Notice that the values of the integrals of these monomials only depend on the combination of powers, not on which particular coordinates have those powers. Using these formulas we compute the relevant integrals that are needed for our work.

Remark A.3. Unless integrals over spheres of different dimension appear in the same expression, we shall abbreviate and omit the superscript ( n ) to be understood from the context.

Example A.4. Using the factorial property of the gamma function, Γ( z + 1) = z Γ( z ), and the value Γ( 1 2 ) = √ π , the integrals of monomials of even powers of order 2, 4 and 6, have the following relations (shortening d S n - 1 as d S ):

$$C _ { 2 } = \int _ { \S ^ { n - 1 } } \, x _ { 1 } ^ { 2 } \, d \mathbb { S } = 2 \frac { \Gamma ( \frac { 3 } { 2 } ) \Gamma ( \frac { 1 } { 2 } ) ^ { n - 1 } } { \Gamma ( \frac { 3 } { 2 } + \frac { n - 1 } { 2 } ) } = \frac { \pi ^ { n / 2 } } { \Gamma ( \frac { n } { 2 } + 1 ) } , \quad C _ { 2 2 } = \int _ { \S ^ { n - 1 } } \, x _ { 1 } ^ { 2 } x _ { 2 } ^ { 2 } \, d \mathbb { S } = \frac { C _ { 2 } } { n + 2 } ,$$


<!-- p:25 -->


$$C _ { 4 } = \int _ { \mathbb { S } ^ { n - 1 } } \, x _ { 1 } ^ { 4 } \, d \mathbb { S } = \frac { 3 \, C _ { 2 } } { n + 2 } = 3 \, C _ { 2 2 } , \quad C _ { 2 2 2 } = \int _ { \mathbb { S } ^ { n - 1 } } \, x _ { 1 } ^ { 2 } x _ { 2 } ^ { 2 } \, x _ { 3 } ^ { 2 } \, d \mathbb { S } = \frac { C _ { 2 } } { ( n + 2 ) ( n + 4 ) } ,$$

$$\S ^ { n - 1 } _ { n } & = \S ^ { n - 1 } _ { n } \\ C _ { 2 4 } & = \int _ { \S ^ { n - 1 } } x _ { 1 } ^ { 2 } x _ { 2 } ^ { 4 } \, d \S = \frac { 3 \, C _ { 2 } } { ( n + 2 ) ( n + 4 ) } = 3 \, C _ { 2 2 2 } , \, C _ { 6 } = \int _ { \S ^ { n - 1 } } \, x _ { 1 } ^ { 6 } \, d \S = \frac { 1 5 \, C _ { 2 } } { ( n + 2 ) ( n + 4 ) } .$$

The value of C 2 is related to the n -dimensional volume of the ball of radius ε , and the ( n - 1)-dimensional area of the unit sphere by V n ( ε ) = Vol( B n ( ε )) = ε n C 2 , and S n - 1 = Area( S n - 1 ) = n C 2 . The integrals over balls needed in our work are:

$$D _ { 2 } = \int _ { B ^ { n } ( \varepsilon ) } \, x _ { 1 } ^ { 2 } \ d x _ { 1 } \cdots d x _ { n } = \frac { \varepsilon ^ { n + 2 } } { n + 2 } C _ { 2 } = \frac { \varepsilon ^ { 2 } } { n + 2 } V _ { n } ( \varepsilon ) ,$$

$$B ^ { n } ( \varepsilon ) \\ D _ { 2 2 } = \int _ { B ^ { n } ( \varepsilon ) } x _ { 1 } ^ { 2 } x _ { 2 } ^ { 2 } \ d x _ { 1 } \cdots d x _ { n } = \frac { \varepsilon ^ { n + 4 } } { ( n + 2 ) ( n + 4 ) } C _ { 2 } = \frac { \varepsilon ^ { 4 } } { ( n + 2 ) ( n + 4 ) } V _ { n } ( \varepsilon ) ,$$

$$B ^ { n } ( \varepsilon ) & \\ D _ { 4 } = \int _ { B ^ { n } ( \varepsilon ) } x _ { 1 } ^ { 4 } \ d x _ { 1 } \cdots d x _ { n } = \frac { 3 \, \varepsilon ^ { n + 4 } } { ( n + 2 ) ( n + 4 ) } C _ { 2 } = \frac { 3 \, \varepsilon ^ { 4 } } { ( n + 2 ) ( n + 4 ) } V _ { n } ( \varepsilon ) .$$

̸

We also need the integral of monomials over half-balls B + ( ε ) (without loss of generality we can consider the half-ball is defined by x 1 ≥ 0). If all the α i are even then nothing changes in the proof of Theorem A.2 except that now we integrate over half the domain and an extra factor of 1 2 is needed. If any α i is odd for i = 1, the integration over those variables is still carried out over the same domain so the overall integral is still 0. However, if α 1 is odd the corresponding integral of that coordinate does not cancel out, and the main formula still holds with β 1 = 1 but without the factor of 2.

Example A.5. Using the formula in the mentioned adjusted form, we define and compute

$$D _ { 1 } ^ { ( n ) } = \int _ { B ^ { + } ( \varepsilon ) } \, x _ { 1 } \ d x _ { 1 } \cdots d x _ { n } = \frac { \varepsilon ^ { n + 1 } \, \pi ^ { \frac { n - 1 } { 2 } } } { 2 \Gamma ( \frac { n + 3 } { 2 } ) } ,$$

which gives the constant needed in our main text D ( n +1) 1 = ∫ B + ( ε ) x 1 dx 1 · · · dx n +1 =

ε 2 n +2 V n ( ε ). When integrating ∫ B + ( ε ) x 2 1 dVol, we shall just write D 2 2 to be consistent with our notation.
