---
id: "Alvarez-Vizoso-Kirby-Peterson_2018_Covariance-Integral-Invariants-Embedded-Manifold"
source_pdf: "../pdf/Alvarez-Vizoso-Kirby-Peterson_2018_Covariance-Integral-Invariants-Embedded-Manifold.pdf"
source_filename: "Alvarez-Vizoso-Kirby-Peterson_2018_Covariance-Integral-Invariants-Embedded-Manifold.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "excellent"
extraction_score: 100.0
visual_assets: "disabled"
references_file: "../references/Alvarez-Vizoso-Kirby-Peterson_2018_Covariance-Integral-Invariants-Embedded-Manifold.references.md"
---

<!-- p:1 -->

## INTEGRAL INVARIANTS FROM COVARIANCE ANALYSIS OF EMBEDDED RIEMANNIAN MANIFOLDS

JAVIER ÁLVAREZ-VIZOSO, MICHAEL KIRBY, AND CHRIS PETERSON

Abstract. Principal Component Analysis can be performed over small domains of an embedded Riemannian manifold in order to relate the covariance analysis of the underlying point set with the local extrinsic and intrinsic curvature. We show that the volume of domains on a submanifold of general codimension, determined by the intersection with higher-dimensional cylinders and balls in the ambient space, have asymptotic expansions in terms of the mean and scalar curvatures. Moreover, we propose a generalization of the classical third fundamental form to general submanifolds and prove that the eigenvalue decomposition of the covariance matrices of the domains have asymptotic expansions with scale that contain the curvature information encoded by the traces of this tensor. In the case of hypersurfaces, this covariance analysis recovers the principal curvatures and principal directions, which can be used as descriptors at scale to build up estimators of the second fundamental form, and thus the Riemann tensor, of general submanifolds.

#### Contents

| 1.                                                                                                                                                             | Introduction . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                               | . . . . . . . . . . . . . . . . . . . . . . 1   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| 2.                                                                                                                                                             | PCA Integral Invariants of Riemannian Submanifolds. . . . . . . . . .                                                                                          | . . . . . . . . . . . . . . . . . . . . . . 3   |
| 3.                                                                                                                                                             | Third Fundamental Form of a Riemannian Submanifold . . . . . . .                                                                                               | . . . . . . . . . . . . . . . . . . . . . . 5   |
| 4.                                                                                                                                                             | Cylindrical Covariance Analysis . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                                                  | . . . . . . . . . . . . . . . . . . . . . . 10  |
| 5.                                                                                                                                                             | Spherical Covariance Analysis . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                                                | . . . . . . . . . . . . . . . . . . . . . . 17  |
| 6.                                                                                                                                                             | Curvature Descriptors . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                                        | . . . . . . . . . . . . . . . . . . . . . . 22  |
| 7.                                                                                                                                                             | Conclusions . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .                                              | . . . . . . . . . . . . . . . . . . . . . . 25  |
| Appendix A. Integration of Monomials over Spheres. . . . . . . . . . . . . . . . . . . . . . .                                                                 | Appendix A. Integration of Monomials over Spheres. . . . . . . . . . . . . . . . . . . . . . .                                                                 | . . . . . . . . . . . . . 26                    |
| References . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . | References . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . | . . . . 27                                      |

## 1. Introduction

Local integral invariants based on Principal Component Analysis have been introduced in the literature as theoretical tools to perform Manifold Learning and Geometry Processing of lowdimensional submanifolds, like curves and surfaces in space. Curvature descriptors obtained in this way serve as feature and shape estimators at scale whose numerical implementation takes advantage of the benefits of employing integrals instead of differentials when only a discrete sample of points is available. Integral invariants provide a theoretical link between the statistical covariance analysis of the underlying point-set of a domain and the differential-geometric invariants at

Date : April 30, 2018.


<!-- p:2 -->


a point of the domain inside the manifold. In particular, intersecting the submanifold with a ball in the ambient space cuts out a subdomain whose covariance matrix has an eigenvalue decomposition that asymptotically expands with the scale of the ball. The geometric interpretation of this analysis lies in the fact that the first and second terms of the eigenvalue series encode the curvature information of the submanifold at the center of the ball.

Integral invariants have been introduced and used in Computer Graphics and Geometry Processing by [11], [6, 7], [9, 10], [21, 22]. The integral invariant viewpoint via Principal Component Analysis has been introduced and studied theoretically and numerically [1], [4], [9,10], [15], [22], [35], with a focus on curves and surface, in order to process discrete samples of points to determine features and detect shapes at scale, and study stability with respect to noise [19], [28,29]. Voronoibased covariance matrices have been also been of interest, [23,24]. The eigenvalue decomposition of covariance matrices of spherical intersection domains was also introduced by [5], [31, 32], in order to obtain local adaptive Galerkin bases for the invariant manifold of large-dimensional dynamical systems. For curves, the Frenet-Serret frame is recovered in the scale limit, and ratios of the covariance matrix eigenvalues provide descriptors at scale of the generalized curvatures [2], but the tools needed to study the curve case are significantly different due to the fact that one-dimensional submanifolds have only extrinsic curvature.

In the present work we generalize to embedded Riemannian manifolds of general codimension the recent study of PCA integral invariants of hypersurfaces [3], that followed the theoretical study of surfaces in [29], with the purpose of obtaining analogous asymptotic formulas between eigenvalues of covariance matrices and curvature, as it was found for curves in [2]. We shall also introduce a generalization to general codimension of the third fundamental form in order to encapsulate all the curvature information hidden in the covariance analysis. Our main result shows how the eigenvalue decomposition of the covariance of cylindrical and spherical intersection domains has the first two orders of the asymptotic expansion given in terms of the dimension, and the extrinsic and intrinsic curvature encoded in the traces of the third fundamental form, with limit eigenvectors playing the role of generalized principal directions.

Geodesic balls inside manifolds have asymptotic series for their intrinsic volume given as corrections to the Euclidean ball completely determined by intrinsic scalar curvature invariants [14]. In our case, the domains of integration depend on the embedding of the submanifold so the extrinsic curvature will play a crucial role in the volume corrections, as in [16]. Normal coordinates via the exponential map are naturally used to do geometric measurements needed for probability and statistics from an intrinsic perspective inside Riemannian manifolds, e.g. [26,27]. The generalized definition of integral invariants makes use of the exponential map in the ambient manifold to make measurements over the underlying point-set of a submanifold.

The structure of the paper is as follows: in section §2 we propose a general definition of integral invariants in the context of general Riemannian submanifolds by use of the exponential map, along with the two types of kernel domains on which we will perform the PCA. In section §3, the study of the geometry of submanifolds via the second fundamental form is briefly reviewed and the classical third fundamental form is generalized to submanifolds of general codimension. In section §4 we compute the volume, barycenter and covariance matrix of a cylindrical domain inside an embedded submanifold; in particular, we show that the scaling of the eigenvalues of the covariance matrix singles out the tangent and normal spaces of the manifold at the point by the span of the corresponding limit eigenvectors, and how the next-to-leading order term in the asymptotic series of the eigenvalues is determined by the eigenvalues of the tangent and normal traces of the third fundamental form. In section §5 an analogous analysis is carried out for the domain determined by the intersection of a ball in ambient space with the manifold, which introduces considerable correction terms with respect to the previous case. This leads to an eigenvalue decomposition of the covariance matrix with tangent part given in terms of the Weingarten operator corresponding to the mean curvature vector. Finally, in section §6 we obtain the limit ratios of the eigenvalues in terms of this curvature information, and invert the asymptotic series to get descriptors at scale for the case of hypersurfaces, where the second and third fundamental forms are completely given by the principal curvatures and principal directions.


<!-- p:3 -->


These results show how Principal Component Analysis can be carried out on a general embedded Riemannian submanifold to probe its local geometry. It establishes the relationship between the statistical covariance analysis of the underlying point-set of the manifold and the classical differential-geometric curvature via the third fundamental form. Applying the integral invariant approach to hypersurfaces provides a method to build multi-scale descriptors of curvature also for the case of general codimension.

## 2. PCA Integral Invariants of Riemannian Submanifolds

In our context, integral invariants are local integrals over domains of a submanifold determined by intersection with objects in the ambient space, like spheres. Two such integrals are the volume of the domain and the point in the ambient manifold that represents the center of mass of the region. A more interesting object is the covariance matrix obtained by integrating the relative covariance of the degrees of freedom of the points in the domain, i.e., the products of the coordinates of the points with respect to a chosen frame. In order to get a frame independent integral invariant, one takes the eigenvalue decomposition of the covariance matrix. Since the kernel domains have a natural scale, e.g., the radius of the sphere, it is useful to think of them as a matrix-valued function of scale at every point. Therefore, these integral invariants correspond to eigenvalues and eigenvectors that can be interpreted respectively as a set of scalar and framevalued functions of scale at every point. The study of covariance matrices in order to obtain adapted frames of general submanifols was studied for example in [5] and [31, 32], whereas the integral invariant approach was developed in detail to extract the curvature information of surfaces in space in [29].

In order to do this type of Principal Component Analysis on a general Riemannian submanifold and generalize local integral invariants, definitions using Cartesian coordinates must naturally be promoted to Riemann normal coordinates [8], [25]. If the n -dimensional submanifold M p n q sits inside an ambient Riemannian manifold p N p n ` k q , g q , the curves in N that generalize the axis used in R n ` k are the geodesic curves γ v p t q and these always exist and are unique locally at any point p P N and direction v . Given an orthonormal frame in T p M ' N p M , the geodesics tangent to each of the vectors will trace out generalized coordinate axis in N that, through the exponential map will uniquely specify any point in a local neighborhood around p . Assuming N is geodesically complete to simplify the exposition, the exponential map collects all geodesics starting at p by mapping straight lines through the origin in T p N - R n ` k to geodesics through p :


<!-- p:4 -->


$$\exp _ { p } \colon T _ { p } \mathcal { M } \to \mathcal { N } \quad \text {such that} \quad \exp _ { p } ( t v ) = \gamma _ { t v } ( 1 ) = \gamma _ { v } ( t ) .$$

At any point p there is a neighborhood r U of 0 in T p N where exp is a diffeomorphism onto a neighborhood U of p in N . From this, for star-shaped r U , there is also a unique geodesic γ p t q connecting p and any other point q P U such that the tangent γ 1 p 0 q ' exp  ́ 1 p p q q . Moreover, the arclength of γ between the two points, i.e. the distance d p p, q q between them determined by the metric g , is the length of the tangent vector representation through this map, d p p, q q ' } exp  ́ 1 p p q q} . These normal neighborhoods allow the parametrization of points using the geodesic distances tangent to a given frame t e μ u n ` k μ ' 1 at p . The injectivity radius r p is the radius of the largest ball B 0 p ε q in T p N where exp is a diffeomorphism, so B p p r p q ' exp p p B 0 p r p qq is the largest ball in N created by radial geodesics of the same length around p where normal coordinates are well-defined. In fact r p ą 0 always. Since our main theorems 4.5 and 5.5 are asymptotic results with scale, in a general Riemannian manifold one could always use normal coordinates to study domains of submanifolds small enough so that they can be mapped to Euclidean space, thus, we propose the following general definition of PCA integral invariants in a general Riemannian manifold.

Definition 2.1. Let D be a measurable domain in a Riemannian manifold p N , g q such that D Ă B p p r p q for some point p P N , The integral invariants associated to the moments of order 0, 1 and 2 of the geodesic coordinate functions of the points of D with respect to p are: the volume

the barycenter

$$V ( D ) = \int _ { D } 1 \, d V o l ,$$

$$s ( D ) = \frac { 1 } { V ( D ) } \int _ { D } [ \exp _ { p } ^ { - 1 } ( q ) ] \, d V o l , \\ \intertext { d e c o m p o s i t i o n } \, \text {decomposition of the covariance matrix} \colon \, &$$

and the eigenvalue decomposition of the covariance matrix:

$$\text {Time decomposition of the covariance matrix} \colon & \\ & C ( D ) = \int _ { D } [ \exp _ { p } ^ { - 1 } ( q ) ] \otimes [ \exp _ { p } ^ { - 1 } ( q ) ] \, d V o l . \\ & \text {measure on } D \text { restriction of the measure of } \sqrt { \ } N \text { induced by the metric } a \text { and the}$$

Here dVol is the measure on D , restriction of the measure of N induced by the metric g , and the tensor product is to be understood as the outer product of the components of the exp  ́ 1 map in a chosen orthonormal basis of T p N . The reference point of the covariance matrix is often chosen to be the barycenter exp p p s q instead of p .

The two types of domains that we shall study are regions in a submanifold M Ă N determined by the intersection with a ball and a cylinder. Using the exponential map one can define such intersections by mapping Euclidean balls and higher-dimensional cylinders in T p N to their geodesic generalizations in the ambient manifold N .

Definition 2.2. The spherical component of radius ε ď r p , at a point p of a submanifold M of a Riemannian manifold N is the domain given by:

$$D _ { p } ( \varepsilon ) \colon = \mathcal { M } \cap \{ q \in \mathcal { N } \colon \| \exp _ { p } ^ { - 1 } ( q ) \| \leqslant \varepsilon \leqslant r _ { p } \} .$$


<!-- p:5 -->


An element V in the Grassmannian Gr p m,n ` k q is an m -dimensional linear subspace of R n ` k . Fixing a point and m -dimensional ball inside V , the standard three dimensional cylinder over the xy -plane can be generalized to an V -cylinder by taking all points in the ambient space that project down onto the ball inside V .

Definition 2.3. The cylindrical component of radius ε ď r p , at a point p of a submanifold M of a Riemannian manifold N over the m -plane V P Gr p m,n ` k q , is the V -cylinder intersection:

$$C y l _ { p } ( \varepsilon , \mathbb { V } ) & \colon = \mathcal { M } \cap \{ q \in \mathcal { N } \colon \| \text {proj} _ { j } ( \exp _ { p } ^ { - 1 } ( q ) ) \| \leqslant \varepsilon \leqslant r _ { p } \} , \\ \\$$

where proj V p ̈q is the orthogonal projection onto V as a linear subspace of T p N . We shall write Cyl p p ε q when V ' T p M is assumed.

We will compute these integral invariants for embedded submanifolds in Euclidean ambient space, N ' R n ` k , where exp  ́ 1 p p q q ' q  ́ p as vectors and the tensor product recovers the common definition of PCA integral invariants studied in the literature. The points q P D are then parametrized by a vector X such that the barycenter is the center of mass

and the the covariance matrix can be interpreted as analogous to a moment of inertia matrix, which for the cylindrical component shall be taken with respect to the center p , following the convention and motivation of [32],

$$\text {vector} \ X \text { such that the barycenter is the center of mass} \\ s ( D ) = \frac { 1 } { V ( D ) } \int _ { D } \ X \, d V o l , \\ \text {matrix} \, \text {can be interpreted as analogous to a moment of inertia matrix} .$$

$$\text {and motivation of } [ 3 , ] , \\ C ( C y _ { 1 } ( \varepsilon ) ) = \int _ { C y _ { 1 } ( \varepsilon ) } ( X - p ) \otimes ( X - p ) \, d V o l , \\ \intertext { t h e q n a l $ o r $ m e n t } \, \text {with} \, \underset { p } { \, } \, \underset { ( 1 ) } { \, } \, \underset { ( 2 ) } { \, } \, \underset { ( 3 ) } { \, } \, \underset { ( 4 ) } { \, } \, \underset { ( 5 ) } { \, } \, \underset { ( 6 ) } { \, } \, \underset { ( 7 ) } { \, } \, \underset { ( 8 ) } { \, } \, \underset { ( 9 ) } { \, } \, \underset { ( 1 ) } { \, } \, \underset { ( 2 ) } { \, } \, \underset { ( 3 ) } { \, } \, \underset { ( 4 ) } { \, } \, \underset { ( 5 ) } { \, } \, \underset { ( 6 ) } { \, } \, \underset { ( 7 ) } { \, } \, \underset { ( 8 ) } { \, } \, \underset { ( 9 ) } { \, } \, \underset { ( 1 ) } { \, } \, \underset { ( 2 ) } { \, } \, \underset { ( 3 ) } { \, } \, \underset { ( 4 ) } { \, } \, \underset { ( 5 ) } { \, } \, \underset { ( 6 ) } { \, } \, \underset { ( 7 ) } { \, } \, \underset { ( 8 ) } { \, } \, \underset { ( 9 ) } { \, } \, \underset { ( 1 ) } { \, } \, \underset { ( 2 ) } { \, } \, \underset { ( 3 ) } { \, } \, \underset { ( 4 ) } { \, } \, \underset { ( 5 ) } { \, } \, \underset { ( 6 ) } { \, } \, \underset { ( 7 ) } { \, } \, \underset { ( 8 ) } { \, } \, \underset { ( 9 ) } { \, } \, \underset { ( 1 ) } { \, } \, \underset { ( 2 ) } { \, } \, \underset { ( 3 ) } { \, } \, \underset { ( 4 ) } { \, } \, \underset { ( 5 ) } { \, } \, \underset { ( 6 ) } { \, } \, \underset { ( 7 ) } { \, } \, \underset { ( 8 ) } { \, } \, \underset { ( 9 ) } { \, } \, \underset { ( 1 ) } { \, } \, \underset { ( 2 ) } { \, } \, \underset { ( 3 ) } { \, } \, \underset { ( 4 ) } { \, } \, \underset { ( 5 ) } { \, } \, \underset { ( 6 ) } { \, } \, \underset { ( 7 ) } { \, } \, \underset { ( 8 ) } { \, } \, \underset { ( 9 ) } { \, } \, \underset { ( 1 ) } { \, } \, \underset { ( 2 ) } { \, } \, \underset { ( 3 ) } { \, } \, \underset { ( 4 ) } { \, } \, \underset { ( 5 ) } { \, } \, \underset { ( 6 ) } { \, } \, \underset { ( 7 ) } { \, } \, \underset { ( 8 ) } { \, } \, \underset { ( 9 ) } { \, } \, \underset { ( 1 ) } { \, } \, \underset { ( 2 ) } { \, } \, \underset { ( 3 ) } { \, } \, \underset { ( 4 ) } { \, } \, \underset { ( 5 ) } { \, } \, \underset { ( 6 ) } { \, } \, \underset { ( 7 ) } { \, } \, \underset { ( 8 ) } { \, } \, \underset { ( 9 ) } { \, } \, \underset { ( 1 ) } { \, } \, \underset { ( 2 ) } { \, } \, \underset { ( 3 ) } { \, } \, \underset { ( 4 ) } { \, } \, \underset { ( 5 ) } { \, } \, \underset { ( 6 ) } { \, } \, \underset { ( 7 ) } { \, } \, \underset { ( 8 ) } { \, } \, \underset { ( 9 ) } { \, } \, \underset { ( 1 ) } { \, } \, \underset { ( 2 ) } { \, } \, \underset { ( 3 ) } { \, } \, \underset { ( 4 ) } { \, } \, \underset { ( 5 ) } { \, } \, \underset { ( 6 ) } { \, } \, \underset { ( 7 ) } { \, } \, \underset { ( 8 ) } { \, } \, \underset { ( 9 ) } { \, } \, \underset { ( 1 ) } { \, } \, \underset { ( 2 ) } { \, } \, \underset { ( 3 ) } { \, } \, \underset { ( 4 ) } { \, } \, \underset { ( 5 ) } { \, } \, \underset { ( 6 ) } { \, } \, \underset { ( 7 ) } { \, } \, \underset { ( 8 ) } { \, } \, \underset { ( 9 ) } { \, } \, \underset { ( 1 ) } { \, } \, \underset { ( 2 ) } { \, } \, \underset { ( 3 ) } { \, } \, \underset { ( 4 ) } { \, } \, \underset { ( 5 ) } { \, } \, \underset { ( 6 ) } { \, } \, \underset { ( 7 ) } { \, } \, \underset { ( 8 ) } { \, } \, \underset { ( 9 ) } { \, } \, \underset { ( 1 ) } { \, } \, \underset { ( 2 ) } { \, } \, \underset { ( 3 ) } { \, } \, \underset { ( 4 ) } { \, } \, \underset { ( 5 ) } { \, } \, \underset { ( 6 ) } { \, } \, \underset { ( 7 ) } { \, } \, \underset { ( 8 ) } { \, } \, \underset { ( 9 ) } { \, } \, \underset { ( 1 ) } { \, } \, \underset { ( 2 ) } { \, } \, \underset { ( 3 ) } { \, } \, \underset { ( 4 ) } { \, } \, \underset { ( 5 ) } { \, } \, \underset { ( 6 ) } { \, } \, \underset { ( 7 ) } { \, } \, \underset { ( 8 ) } { \, } \, \underset { ( 9 ) } { \, } \, \underset { ( 1 ) } { \, } \, \underset { ( 2 ) } { \, } \, \underset { ($$

whereas for the spherical component the covariance matrix shall be taken with respect to the barycenter following [29],

$$\text {center following } [ 2 ] , \\ C ( D _ { p } ( \varepsilon ) ) = \int _ { D _ { p } ( \varepsilon ) } ( X - s ( D _ { p } ( \varepsilon ) ) ) \otimes ( X - s ( D _ { p } ( \varepsilon ) ) ) \, d V o l . \\ \intertext { t h o i n t h o l i v s of g o n o r al i t y t h o s o f d o f i n t i o n s c o l d v a h o w h o o n o r m a l i z o d b y t h o v i l o m u o p e f t h o }$$

Without loss of generality, these definitions could have been normalized by the volume of the domain to make the integral measure become a probability density and thus make the matrices actual statistical covariances.

## 3. Third Fundamental Form of a Riemannian Submanifold

For a complete analysis of the the geometry of Riemannian submanifolds see [8], [17], [25], [33]. Let p M , g q be an n -dimensional manifold isometrically embedded in an p n ` k q -dimensional Riemannian manifold p N , g q , and let ∇ , ∇ be the respective Levi-Civita connections. We shall write g p ̈ ,  ̈q ' x  ̈ ,  ̈ y , classically called the fi rst fundamental form of M in N . Then, at any point p P M and for any vector y P T p M , and vector field X P Γ p T M q , the metric connection of M is the projection of the metric connection of N : ∇ y X ' p ∇ y X q J , where p  ̈ q J : T p N Ñ T p M . The second fundamental form II of M in N is defined to be the normal projection of the ambient covariant derivative when acting on vectors fields tangent to M , i.e., denoting p  ̈ q K : T p N Ñ N p M ,

$$\Pi ( x , y ) = ( \overline { \nabla } _ { y } X ) ^ { \perp } , \quad i . e . , \quad \overline { \nabla } _ { y } X = \nabla _ { y } X + \Pi ( x , y ) ,$$


<!-- p:6 -->


for all x , y P T p M , and X P Γ p T M q such that X | p ' x . It is a symmetric bilinear form on the tangent space at every point taking values in the normal space, II : T p M b T p M Ñ N p M . Fixing a normal vector n P N p M , the scalar-valued bilinear form x II p x , y q , n y has a corresponding selfadjoint map p S n P End p T p M q , called the Weingarten map at n , such that: x II p x , y q , n y ' x p S n x , y y ' x x , p S n y y . (3.2) Fixing orthonormal bases t e μ u n μ ' 1 of T p M , and t n j u k j ' 1 of N p M , the components of the second fundamental form at point p are:

$$\text {II} ( e _ { \mu } , e _ { \nu } ) & = \sum _ { j = 1 } ^ { k } \Pi ^ { j } ( e _ { \mu } , e _ { \nu } ) n _ { j } = \sum _ { j = 1 } ^ { k } \langle \text {II} ( e _ { \mu } , e _ { \nu } ) , \, n _ { j } \rangle \, n _ { j } = \sum _ { j = 1 } ^ { k } \langle \hat { S } _ { j } \, e _ { \mu } , \, e _ { \nu } \rangle \, n _ { j } . \\ \text {The geometric meaning of II lies in the fact that the Weigartzen map measures the tangential}$$

The geometric meaning of II lies in the fact that the Weingarten map measures the tangential rate of change of normal vectors to M when moving in tangent directions, cf. [8, Eq. II.2.4]:

p S n x '  ́p ∇ x N q J , for any N P Γ p N M q such that N | p ' n . From this, [25, Ch. 4, Cor. 9, 10], II p x , x q is to be interpreted as the curve acceleration in N of a geodesic inside M at p with tangent velocity x . Therefore, II naturally measures the extrinsic curvature of the embedding since it represents the forced curving of the straightest lines in M due to the curving of M itself in N .

The inverse function theorem and [17, Ch. VII, Ex. 3.3] establish the following lemma, of fundamental importance for the computations in the proofs of the present work.

Lemma 3.1. Let M be an n -dimensional submanifold of an p n ` k q -dimensional Riemannian manifold p N , g q , with the induced metric g | M . For any point p P M and orthonormal basis t e μ u n μ ' 1 of T p M , it is possible to choose normal coordinates p y 1 , . . . , y n ` k q in N such that the coordinate tangent vectors at the origin Y 1 , . . . , Y n coincide with t e μ u n μ ' 1 , and Y n ` 1 , . . . , Y n ` k are an orthonormal basis t n j u k j ' 1 of N p M . Moreover, M is locally given by a graph manifold y 1 ' x 1 , . . . , y n ' x n , y n ` 1 ' f 1 p x q , . . . , y n ` k ' f k p x q , such that the components of the second fundamental form at p can be written as:

$$f \ p \ c a n d { \sigma } { \sigma } = & \sum _ { j = 1 } ^ { k } \left [ \frac { \partial ^ { 2 } f ^ { j } } { \partial x ^ { \mu } \partial x ^ { \nu } } ( 0 ) \right ] n _ { j } . \\ \intertext { f l a t r a c $ o r $ I I $ for any o r t h o n $ o r $ m a l $ t a n $ e r $ }$$

The invariance of the trace of II for any orthonormal tangent frame t e μ u n μ ' 1 leads to the definition of the mean curvature vector:

$$H = \sum _ { \mu = 1 } ^ { n } \text {I} ( e _ { \mu } , e _ { \mu } ) = \sum _ { j = 1 } ^ { k } H ^ { j } n _ { j } , \quad \text {where } H ^ { j } = \sum _ { \mu = 1 } ^ { n } \text {I} ^ { j } ( e _ { \mu } , e _ { \mu } ) . \\ \intertext { The study of the intrinsic geometry of ( M _ { \ } a ) dependants only on the metric and is given in terms }$$

The study of the intrinsic geometry of p M , g q depends only on the metric and is given in terms of the Riemann curvature tensor:

$$R ( x , y ) z = ( \nabla _ { x } \nabla _ { y } - \nabla _ { y } \nabla _ { x } - \nabla _ { [ x , y ] } ) Z ,$$

for any x , y , z P T p M and Z P Γ p T M q such that Z | p ' z . This fundamental tensor equivalently measures the integrability of parallel transport, geodesic deviation and local flatness. Its traces yield the Ricci tensor and the scalar curvature , R ' ř μ R ic p e μ , e μ q . Here, p R P End p T p M q is the Ricci operator associated to the Ricci tensor with respect to the metric.


<!-- p:7 -->


$$\mathcal { R } i c ( x , y ) = \sum _ { \mu = 1 } ^ { n } \langle R ( e _ { \mu } , x ) y , e _ { \mu } \rangle = \langle \hat { \mathcal { R } } \, x , y \rangle , \\ \intertext { w r v a t u r e , } \mathcal { R } \, = \, \sum _ { \mu } \mathcal { R } i c ( e _ { \mu } , e _ { \mu } ) . \quad \text {Here, } \hat { \mathcal { R } } \in \text {End} ( T _ { p } \mathcal { M } ) \text { is the }$$

Gauß Theorema Egregium establishes that the intrinsic curvature of surfaces is a particular combination of products of the components of the second fundamental form. This generalizes to higher dimension to

Theorem 3.2 (Gauß equation) . The Riemann curvature tensor of a submanifold M is related to the curvature R of the ambient manifold N via

$$\langle R ( x , y ) z , w \rangle = \langle \overline { R } ( x , y ) z , \, w \rangle + \langle \mathbb { I } ( x , w ) , \, \mathbb { I } ( y , z ) \rangle - \langle \mathbb { I } ( x , z ) , \, \mathbb { I } ( y , w ) \rangle$$

for all x , y , z , w P T p M .

In classical differential geometry, [13], [34], the third fundamental form is the natural object to construct out of scalar products after the first fundamental form, I p x , y q ' x x , y y , and the second fundamental form II p x , y q ' x Sx , y y , so it is defined for hypersurfaces, e.g. [20], as

p p p However, it does not provide new information since it is completely determined by Gauß equation 3.2, e.g., in Euclidean space [17]:

$$\text {ar} \text { products after the first fundamental form, } & \text {II} ( x , y ) = \langle \hat { S } \, x , y \rangle , \, \text {so it is defined for hypersus} \\ & \text {II} ( x , y ) = \langle \hat { S } \, x , \, \hat { S } \, y \rangle = \langle \hat { S } ^ { 2 } x , y \rangle . \\$$

x p S 2 x , y y ' H x p Sx , y y  ́ R ic p x , y q , (3.7) or, in terms of the Ricci operator, p S 2 ' H p S  ́ p R . For a manifold M of higher codimension k , there are k linearly independent normal vectors at every point and, as mentioned before, the generalized second fundamental form takes values in the normal bundle precisely to reflect this structure in terms of the corresponding Weingarten operators at every normal vector. Therefore, the natural generalization of x Sx , Sy y to this context is

p p Definition 3.3. The third fundamental form of a Riemannian submanifold M Ă N is the fourthrank tensor III P p T p M  ̊ q 2 b N p M  ̊ b N p M , given at every point p P M by

$$\langle \, \text {II} ( x , y ) \, n , \, m \, \rangle \colon = \langle \, \hat { S } _ { m } \, x \, , \, \hat { S } _ { n } \, y \, \rangle . \\ M , \, \text {and} \, n , m \in N _ { p } \mathcal { M } .$$

for any x , y P T p M , and n , m P N p M .

At any specific point, and because the Weingarten maps are self-adjoint, the linear operator III p x , y q P End p N p M q is written as the following linear combination, when a particular orthonormal basis t n j u k j ' 1 of the normal space is fixed and η j ' g p ̈ , n j q is the dual basis:

$$\Pi ( x , y ) = \sum _ { i , j = 1 } ^ { k } \langle \hat { S } _ { i } \hat { S } _ { j } \, x , y \rangle \, \eta ^ { i } \otimes n _ { j } .$$


<!-- p:8 -->


This is due to the linearlity of the map n ÞÑ S n : N p M Ñ End p T p M q ; if n ' ř j n j n j then

for all x , y P T p M .

$$\text {This is due to the linearity of the map } n & \mapsto \hat { S } _ { n } \colon N _ { p } \mathcal { M } \to \text {End} ( T _ { p } \mathcal { M } ) ; \text {if } n = \sum _ { j } n ^ { j } n _ { j } \text { then} \\ & \langle \hat { S } _ { n } \, x , y \rangle = \langle \text {II} ( x , y ) , n \rangle = \sum _ { j = 1 } ^ { k } n ^ { j } \langle \text {II} ( x , y ) , \, n _ { j } \rangle = \langle \left ( \sum _ { j = 1 } ^ { k } n ^ { j } \hat { S } _ { j } \right ) x , y \rangle , \\ \text {for all } x , y \in T _ { p } \mathcal { M } . \\ \text {Let us define the tangent trace of a tensor } A \in ( T _ { M } \mathcal { * } ) ^ { 2 } \otimes N _ { j } M ^ { * } \otimes N _ { j } M \text { as the operator sum }$$

Let us define the tangent trace of a tensor A P p T p M  ̊ q 2 b N p M  ̊ b N p M as the operator sum of the evaluations at an orthonormal basis t e μ u n μ ' 1 of T p M :

And let the normal trace of such a tensor be

$$t r _ { \| } A \coloneqq \sum _ { \mu = 1 } ^ { n } A ( e _ { \mu } , e _ { \mu } ) \in E \text {End} ( N _ { p } \mathcal { M } ) , \\ \intertext { a l $ t r $ c a t r $ o f $ s u c h $ a t e n $ b e }$$

$$\ t r _ { \perp } A \colon = \sum _ { j = 1 } ^ { k } \langle \, \text {III} ( \cdot , \cdot ) \, n _ { j } , \, n _ { j } \, \rangle \in ( T _ { p } \mathcal { M } ^ { * } ) ^ { 2 } , \\ \text {formal basis} \, \{ n _ { j } \} ^ { k } _ { \cdot } \, \text {, of } N \, M \, \text { These tensors are well-defined since the sums are}$$

for any orthonormal basis t n j u k j ' 1 of N p M . These tensors are well-defined since the sums are independent of the orthonormal basis chosen.

Lemma 3.4. At any point p P M , for any x , y P T p M , and n , m P N p M , the normal trace of the third fundamental form is

$$\text {tr} \perp \Pi ( x , y ) = \sum _ { j = 1 } ^ { k } \langle \widehat { S } _ { j } ^ { 2 } \, x , y \rangle = \langle \, ( \widehat { S } _ { H } - \widehat { \mathcal { R } } + \overline { \mathcal { R } } ) \, x , y \, \rangle , \\ \widehat { \mathcal { R } } \ a n d \ \overline { \mathcal { R } } \ a r e \ t h e \ R i c c i \ o p e r a t i o r s \ o f \ \mathcal { M } \ a n d \ \mathcal { N } \ r e s p e c t i v e l y . \ \ln \ p a r t i c u l a r , \ t h e \ s u m \ o f$$

where p R and R are the Ricci operators of M and N respectively. In particular, the sum of squares of the Weingarten operators p S j , for an orthonormal basis t n j u k j ' 1 of N p M , is independent of the basis. The tangent trace of the third fundamental form is a linear operator on N p M whose components with respect to the metric are the Frobenius inner products of the corresponding Weingarten operators:

The total trace is

$$\langle \left ( t r _ { \| } \Pi I \right ) n , m \rangle & = t r \left ( \widehat { S } _ { n } \widehat { S } _ { m } \right ) . \\ \\ t r \Pi I & = t r _ { \perp } t r \| \Pi I = \| H \| ^ { 2 } - \mathcal { R } + \overline { \mathcal { R } } .$$

$$\ t r \, \Pi \, I I = \ t r \, _ { \perp } \, \text {tr} \, _ { \| } \, \Pi \, I = \| H \| ^ { 2 } - \mathcal { R } + \overline { \mathcal { R } } .$$

Proof. The normal trace biliniar form has components

$$P r o f . \ \L The \text {normal trace bilinear form has components} \\ \text {tr} \_ \Pi I ( e _ { \mu } , e _ { \nu } ) & = \sum _ { j = 1 } ^ { k } \langle \hat { S } _ { j } \, e _ { \mu } , \hat { S } _ { j } \, e _ { \nu } \rangle = \sum _ { j = 1 } ^ { k } \sum _ { \alpha = 1 } ^ { m } \langle \hat { S } _ { j } e _ { \alpha } , e _ { \mu } \rangle \langle \hat { S } _ { j } e _ { \alpha } , e _ { \nu } \rangle \\ & = \sum _ { j = 1 } ^ { k } \sum _ { \Pi ^ { j } ( e _ { \alpha } , e _ { \mu } ) \Pi ^ { j } ( e _ { \alpha } , e _ { \nu } ) } = \sum _ { \alpha = 1 } ^ { n } \langle \Pi ( e _ { \alpha } , e _ { \mu } ) , \Pi ( e _ { \alpha } , e _ { \nu } ) \rangle , \quad ( 3 . 1 5 ) \\ \text {that using Gau} \, \text {equation lead to the corresponding linear operator with respect to the metric}$$

that using Gauß equation lead to the corresponding linear operator with respect to the metric:

$$\text {that using Gaufl$ equation lead to the corresponding linear operator with respect to the metric} \\ \text {tr} \perp \text {II} ( e _ { \mu } , e _ { \nu } ) = \sum _ { \alpha = 1 } ^ { n } \langle \Pi ( e _ { \alpha } , e _ { \alpha } ) , \Pi ( e _ { \nu } , e _ { \mu } ) \rangle + \sum _ { \alpha = 1 } ^ { n } \langle \overline { R } ( e _ { \alpha } , e _ { \nu } ) e _ { \mu } , e _ { \alpha } \rangle - \sum _ { \alpha = 1 } ^ { n } \langle R ( e _ { \alpha } , e _ { \nu } ) e _ { \mu } , e _ { \alpha } \rangle \\ = \langle \Pi ( e _ { \mu } , e _ { \nu } ) , H \rangle + \overline { \mathcal { K } } i c ( e _ { \mu } , e _ { \nu } ) - \mathcal { R } i c ( e _ { \mu } , e _ { \nu } ) \\ = \langle \hat { \mathcal { S } } H e _ { \mu } , e _ { \nu } \rangle + \langle \overline { \mathcal { R } } e _ { \mu } , e _ { \nu } \rangle - \langle \hat { \mathcal { R } } e _ { \mu } , e _ { \nu } \rangle .$$


<!-- p:9 -->


This is the generalization of the operator of the classical third fundamental form, equation 3.7:

$$\sum _ { j = 1 } ^ { k } \widehat { S } _ { j } ^ { 2 } = \widehat { S } _ { H } - \widehat { \mathcal { R } } + \overline { \mathcal { R } } .$$

The tangent trace is trivial by definition of trace of a linear operator with respect to the metric and the self-adjointness of the Weingarten operators:

$$\langle ( \text {tr} \, \| \Pi ) \, n , m \rangle & = \sum _ { \mu = 1 } ^ { n } \langle \, \hat { S } _ { n } \hat { S } _ { n } \, e _ { \mu } , e _ { \mu } \, \rangle = ( \hat { S } _ { m } , \hat { S } _ { n } ) _ { F } . \\ \intertext { t h o r t h o n o r m a l $ b a s i s $ t h i s t e n $ r i s t h e l i n e c b i n a }$$

In a fixed orthonormal basis this tensor is the linear combination

$$t r \left \| \Pi \right \| = \sum _ { i , j = 1 } ^ { k } \sum _ { \mu = 1 } ^ { n } \langle \hat { S } _ { i } \hat { S } _ { j } \, e _ { \mu } \, , e _ { \mu } \rangle \, \eta ^ { i } \otimes n _ { j } = \sum _ { i , j = 1 } ^ { k } \, t r \left ( \hat { S } _ { i } \, \hat { S } _ { j } \right ) \, \eta ^ { i } \otimes n _ { j } , \\ \text {nose components can be expressed in terms of the second fundamental form as}$$

whose components can be expressed in terms of the second fundamental form as

$$\text {tr} \left ( \hat { S } _ { i } \hat { S } _ { j } \right ) = \sum _ { \mu , \nu = 1 } ^ { n } \langle \hat { S } _ { i } \, e _ { \mu } , e _ { \nu } \times \hat { S } _ { j } \, e _ { \mu } , e _ { \nu } \rangle = \sum _ { \mu , \nu = 1 } ^ { n } \, I ^ { i } ( e _ { \mu } , e _ { \nu } ) I ^ { j } ( e _ { \mu } , e _ { \nu } ) . \\ \text {Taking the total trace of II is analogous to the complete contraction of the Riemann curvature}$$

Taking the total trace of III is analogous to the complete contraction of the Riemann curvature tensor indices to obtain the scalar curvature:

$$\text {tr} \, \Pi \, = \, & \, \text {tr} \, \| \text {tr} \, \Pi \, \| \, = \, \sum _ { \mu = 1 } ^ { n } \langle \, \langle \hat { S } _ { H } - \hat { \mathcal { R } } + \overline { \mathcal { R } } ) e _ { \mu } \, , e _ { \mu } \rangle = \, \text {tr} \, \hat { S } _ { H } - \text {tr} \, \hat { \mathcal { R } } + \text {tr} \, \overline { \mathcal { R } } \\ & \, = \, \sum _ { \mu = 1 } ^ { n } \, \text {tr} \, \Pi \, \| \text {e} ( e _ { \mu } , e _ { \mu } ) = \sum _ { \alpha , \beta } ^ { n } \, \| \text {I} ( e _ { o } , e _ { \beta } ) \| ^ { 2 } , \\$$

where tr p S H ' ř n μ ' 1 x II p e μ , e μ q , H y ' } H } 2 , and the traces of the Ricci operators are by definition the scalar curvatures. □

Equations 3.16 and 3.15 will be recognized inside the elements of the tangent and normal matrix blocks in our covariance matrices to express its eigenvalues in terms of the third fundamental form.

The asymmetry of the components of the third fundamental form operator III p x , y q encodes the curvature information of the connection defined on the normal bundle N M by p ∇ x N q K , for any x P T p M , N P Γ p N M q , where an analog to Gauß equation holds.

Lemma 3.5 (Ricci equation) . The Riemann curvature of the induced normal connection, R K , satisfies:

$$\langle R _ { \perp } ( x , y ) n , m \rangle = \langle \overline { R } ( x , y ) n , m \rangle + \langle \coprod ( x , y ) n , m \rangle - \langle \coprod ( x , y ) m , n \rangle ,$$

for all x , y P T p M , and n , m P N p M , at any point p P M .


<!-- p:10 -->


Proof. Writing the classical equation [8, Ex. II.11] in terms of Weingarten maps leads to

$$\sum _ { \mu = 1 } ^ { n }$$

for any orthonormal basis t e μ u μ ' 1 of T p M .

$$\langle \, \overline { R } ( x , y ) n , m \rangle - \langle R _ { \perp } ( x , y ) n , m \rangle & = \sum _ { \mu = 1 } ^ { n } \left [ \, \langle \, \mathbb { I } ( e _ { \mu } , x ) , n \rangle \langle \, \mathbb { I } ( e _ { \mu } , y ) , m \rangle + \\ & \quad - \langle \, \mathbb { I } ( e _ { \mu } , y ) , n \rangle \langle \, \mathbb { I } ( e _ { \mu } , x ) , m \rangle \, \right ] \\ = \sum _ { \mu = 1 } ^ { n } \langle \, \hat { S } _ { n } \, x , e _ { \mu } \rangle \langle \, \hat { S } _ { m } \, y , e _ { \mu } \rangle - \langle \, \hat { S } _ { n } \, y , e _ { \mu } \rangle \langle \, \hat { S } _ { m } \, x , e _ { \mu } \rangle = \langle \, \hat { S } _ { n } \, x , \hat { S } _ { m } \, y \rangle - \langle \, \hat { S } _ { n } \, y , \hat { S } _ { m } \, x \rangle . \\ \intertext { f o r a n t h o r $ n $ o r $ \mu $ } \Box$$

## 4. Cylindrical Covariance Analysis

In this section we compute the integral invariants of the cylindrical domain around a point on an n -dimensional submanifold M of R n ` k . In the case the cylinder is not normal to the manifold at the point, we can only establish the leading order terms, but that is sufficient in the generic case to be able to detect the tangent space of the manifold by the scaling behaviour of the eigenvalues of the covariance matrix. Once the cylinder is fixed to be normal to this tangent space, the integral invariants can be computed to next-to-leading order to see how they encode the geometric information of the third fundamental form.

We shall always work in a neighborhood U Ă R n ` k of p P M , sufficiently small so that U X M is given by a graph representation r x 1 , . . . , x n , f 1 p x q , . . . , f k p x qs T over its tangent space, i.e., 0 represents p , x ' r x 1 , . . . , x n s T P T p M , and ∇ f j p 0 q ' 0 , so that the manifold is approximated at p by its osculating paraboloids.

Lemma 4.1. The first fundamental form components of a graph manifold M Ă R n ` k , parametrized by r x 1 , . . . , x n , f 1 p x q , . . . , f k p x qs T P T p M ' N p M - R n ` k , are:

$$g _ { \mu \nu } ( x ) = \delta _ { \mu \nu } + \sum _ { j = 1 } ^ { k } \frac { \partial f ^ { j } } { \partial x ^ { \mu } } \frac { \partial f ^ { j } } { \partial x ^ { \nu } } . \\ \intertext { n . m . i n t h e s e c o r d i n g a t e s $ j $ a i v e n $ b y }$$

The induced measure on M in these coordinates is given by

$$T h e \, \text {unduced metause on } \mathcal { M } \, \text { in these coordinates is given by} \\ d V o l = \sqrt { \det g ( x ) } \, d ^ { n } x = \left ( 1 + \frac { 1 } { 2 } \sum _ { j = 1 } ^ { k } \sum _ { \alpha = 1 } ^ { n } \left [ \sum _ { \beta = 1 } ^ { n } \left ( \frac { \partial ^ { 2 } f ^ { j } } { \partial x ^ { \alpha } \partial x ^ { \beta } } ( 0 ) \right ) x ^ { \beta } \right ] ^ { 2 } + \mathcal { O } ( x ^ { 3 } ) \right ) d ^ { n } x . \quad ( 4 . 2 ) \\ P r o f . \, T h e \, \text {tangent space in these coordinates is spanned by the vectors}$$

Proof. The tangent space in these coordinates is spanned by the vectors

$$X _ { \mu } = \frac { \partial } { \partial x ^ { \mu } } [ x ^ { 1 } , \dots , x ^ { n } , f ^ { 1 } ( x ) , \dots , f ^ { k } ( x ) ] ^ { T } = [ 0 , \dots , 1 , \dots , 0 , \frac { \partial f ^ { 1 } } { \partial x ^ { \mu } } , \dots , \frac { \partial f ^ { k } } { \partial x ^ { \mu } } ] ^ { T } , \\ \text {for } \mu \, = \, 1 _ { \infty } , \, n _ { \ } \text {which yields the canonical orthogonal basis at } \, n _ { \ } \text {since } \nabla f ^ { j } ( 0 ) \, = \, 0 .$$

for μ ' 1 , . . . , n , which yields the canonical orthonormal basis at p since ∇ f j p 0 q ' 0 . The induced metric tensor is then

$$g _ { \mu \nu } ( x ) = \langle \, X _ { \mu } , \, X _ { \nu } \, \rangle = \delta _ { \mu \nu } + \sum _ { j = 1 } ^ { k } \frac { \partial f ^ { j } } { \partial x ^ { \mu } } \frac { \partial f ^ { j } } { \partial x ^ { \nu } } . \\ \intertext { t h o t h o f i ( r ) h a v o T y l o r o n p a n s i o n s t o r t i n g a t o r d o r $ 2 i $ }$$

From this, recalling that the f j p x q have Taylor expansions starting at order 2 in these coordinates, the matrix of the metric components is of the form r g s ' Id n `r h s , where the correction matrix r h s ' r ř j B μ f j B ν f j s is small because we are in a neighborhood of 0 with ∇ f j p 0 q ' 0 . Let for every j ' 1 , . . . , k , then


<!-- p:11 -->


$$f ^ { j } ( x ) & = \frac { 1 } { 2 } \sum _ { \alpha , \beta = 1 } ^ { n } \left ( \frac { \partial ^ { 2 } f ^ { j } } { \partial x ^ { \alpha } \partial x ^ { \beta } } ( 0 ) \right ) x ^ { \alpha } x ^ { \beta } + \mathcal { O } ( x ^ { 3 } ) , \\$$

$$\frac { \partial f ^ { j } } { \partial x ^ { \mu } } & = \sum _ { \beta = 1 } ^ { n } \left ( \frac { \partial ^ { 2 } f ^ { j } } { \partial x ^ { \beta } \partial x ^ { \mu } } ( 0 ) \right ) x ^ { \beta } + \mathcal { O } ( x ^ { 2 } ) . \\ \intertext { r m o f a B i e r m a n i p a n d i s g i v e n b y . }$$

$$\varepsilon , \text { Lem. } 1 9 ] , \text { whose lowest order approximation is } \det g \approx 1 + \text { tr} h , \text { so } \sqrt { \det g } \approx 1 + \frac { \frac { } { 2 } \text { tr} h , \text { 1.e.,} } { 2 } \\ \sqrt { \det g ( x ) } = 1 + \frac { 1 } { 2 } \sum _ { \alpha = 1 } ^ { n } \sum _ { j = 1 } ^ { k } \left ( \frac { \partial f ^ { j } } { \partial x ^ { \alpha } } \right ) ^ { 2 } + \dots = 1 + \frac { 1 } { 2 } \sum _ { \alpha = 1 } ^ { n } \sum _ { j = 1 } ^ { k } \left [ \sum _ { \beta = 1 } ^ { n } \left ( \frac { \partial ^ { 2 } f ^ { j } } { \partial x ^ { \beta } \partial x ^ { \mu } } ( 0 ) \right ) x ^ { \beta } \right ] ^ { 2 } + \mathcal { O } ( x ^ { 3 } ) .$$

In the rest of this paper we shall abbreviate second derivatives at the origin by

$$\kappa _ { \alpha \beta } ^ { j } = \kappa _ { \beta \alpha } ^ { j } \colon = \frac { \partial ^ { 2 } f ^ { j } } { \partial x ^ { \alpha } \partial x ^ { \beta } } ( 0 ) , \\ \text {hypersurface principal curvatures, } \text {w}$$

motivated by the notation of hypersurface principal curvatures, which are the eigenvalues of the local Hessian of the defining function. We can now compute the Taylor expansion of the integral invariants in the chosen coordinates, and then relate the terms to the curvature differential invariants which are always combinations of second derivatives.

Theorem 4.2. The n -dimensional volume of the cylindrical component for a generic V P Gr p n, n ` k q , such that V K X T p M ' t 0 u , is to leading order the volume of the ellipsoid of intersection between the V -cylinder and T p M :

$$V ( C y l _ { p } ( \varepsilon , \mathbb { V } ) ) = V _ { n } ( 1 ) \prod _ { \mu = 1 } ^ { n } \ell _ { \mu } + \mathcal { O } ( \varepsilon ^ { n + 1 } ) , \\ \intertext { t h e p r i n c i p a l s e m i - a x e s o f t h e e l l i p s o i d } W h e n d \mathbb { V } = T _ { n } \mathcal { M } _ { \ } t h e v o l u m e \ i s$$

$$\ e l e \ e l l e \ p r i c { \L p a l \, \sinh e x } { \sigma } \ e l l e \ e l l p s o l d . \ \ w h e n \ \varnothing = I _ { p } \mathcal { M } , \, \ w h e \ v o l a m e \ i s \\ V ( C y l _ { p } ( \varepsilon ) ) = V _ { n } ( \varepsilon ) \left [ 1 + \frac { \varepsilon ^ { 2 } } { 2 ( n + 2 ) } \ t r \Pi I I + \mathcal { O } ( \varepsilon ^ { 4 } ) \right ] \\ = \| H \| ^ { 2 } - \mathcal { R }$$

where l μ are the the principal semi-axes of the ellipsoid. When V ' T p M , the volume is

where tr III ' } H } 2  ́ R .

Proof. To compute the leading term of V p Cyl p p ε, V qq we can approximate M near p by its tangent space, such that, fixing local coordinates with a basis for T p M ' N p M , a point is specified by X ' r x , 0 s T , with x P T p M , 0 P N p M . Since V K X T p M ' t 0 u , we have T p M ' V K ' R n ` k , and of course V ' V K ' R n ` k . Let t e μ u n μ ' 1 be an orthornomal basis of T p M , and t u α u n α ' 1 Yt v j u k j ' 1 an orthonormal basis of V ' V K , then the elements of the former are a linear combination of the latter, so there are matrices A,B such that:

$$e _ { \mu } = \sum _ { \alpha = 1 } ^ { n } A _ { \mu } ^ { \alpha } u _ { \alpha } + \sum _ { j = 1 } ^ { k } B _ { \mu } ^ { j } v _ { j } .$$

The natural volume form of a Riemannian manifold is given by ? det g dx 1 ^ ̈ ̈ ̈ ^ dx n , [25, Ch. 7, Lem. 19], whose lowest order approximation is det g « 1 ` tr h , so ? det g « 1 ` 1 2 tr h , i.e.,

□


<!-- p:12 -->


We need to find the region } proj V p X q} ď ε , and since X ' ř μ x μ e μ , when X P T p M , the projection is

hence, the domain of integration in x in this approximation is

$$\proj _ { \mathbb { W } } ( X ) = \sum _ { \alpha = 1 } ^ { n } \langle X , u _ { \alpha } \rangle \, u _ { \alpha } = \sum _ { \alpha = 1 } ^ { n } \sum _ { \mu = 1 } ^ { n } x ^ { \mu } A _ { \mu } ^ { \alpha } u _ { \alpha } , \\ \text { again of integration in } x \text { in this approximation is}$$

$$\left | \text {proj} _ { \mathbb { V } } ( X ) \right | ^ { 2 } & = \sum _ { \alpha = 1 } ^ { n } \left ( \sum _ { \mu = 1 } ^ { n } x ^ { \mu } \, A _ { \mu } ^ { \alpha } \right ) ^ { 2 } \leqslant \varepsilon ^ { 2 } . \\ \text {mutation that can be written as}$$

This is a quadratic equation that can be written as

$$\ a \text { quadratic equation that can be written as} \\ \sum _ { \mu , \nu } ^ { n } x ^ { \mu } \left [ \sum _ { \alpha = 1 } ^ { n } A _ { \mu } ^ { \alpha } A _ { \nu } ^ { \alpha } \right ] x ^ { \nu } = x ^ { T } [ A \cdot A ^ { T } ] x = y ^ { T } \cdot y = \| y \| ^ { 2 } \leqslant \varepsilon ^ { 2 } , \\ = A _ { T } x \, \text { The matrix } [ A \cdot A ^ { T } ] \text { is positive definite} \, \text { so } i s \text { clearly nonnegative}$$

where y ' A T x . The matrix r A  ̈ A T s is positive definite since it is clearly nonnegative, and if x P ker A T for nonzero x , then proj V p X q ' 0 , thus X P V K , which contradicts X P T p M under our assumption V K X T p M ' t 0 u . Therefore, the cylindrical domain is an n -dimensional ellipsoid in the tangent space at p , whose volume is given in terms of its principal semi-axes:

$$V ( C _ { Y } l _ { p } ( \varepsilon , \mathbb { V } ) ) = \frac { \pi ^ { n / 2 } } { \Gamma ( \frac { n } { 2 } + 1 ) } \prod _ { \mu = 1 } ^ { n } \ell _ { \mu } + \mathcal { O } ( \varepsilon ^ { n + 1 } ) . \\ \intertext { t h e l o c a l g r a p h b a n p r a x i m a t i o n o f A M o v e r T A M v e l d s }$$

When V ' T p M , the local graph approximation of M over T p M yields

$$\ p r o j _ { T _ { p } , \mathcal { M } } ( X ) = \| p r o j _ { T _ { p } , \mathcal { M } } ( [ x , f ^ { 1 } ( x ) , \dots , f ^ { k } ( x ) ] ^ { T } ) \| = \| x \| \leqslant \varepsilon ,$$

$$\text { thus, we are integrating } \sqrt { d e g ( x ) } \, \text { over the ball } B _ { p } ^ { ( n ) } ( \varepsilon ) & \subset T _ { p } \mathcal { M } , \text { which can be computed using} \\ \text { the integrals in the appendix: } \\ V ( C y _ { p } ( \varepsilon ) ) & = \int _ { \mathbb { S } ^ { n - 1 } } d \mathbb { S } \int _ { 0 } ^ { \varepsilon } \rho ^ { n - 1 } \left ( 1 + \frac { 1 } { 2 } \sum _ { i = 1 } ^ { k } \sum _ { \alpha = 1 } ^ { n } \left [ \sum _ { \beta = 1 } ^ { n } \kappa _ { \alpha \beta } ^ { i } \rho \overline { x } ^ { \beta } \right ] ^ { 2 } + \mathcal { O } ( x ^ { 3 } ) \right ) d \rho \\ & = V _ { n } ( \varepsilon ) + \frac { \varepsilon ^ { n + 2 } } { 2 ( n + 2 ) } \sum _ { i = 1 } ^ { k } \sum _ { \alpha = 1 } ^ { n } \sum _ { \beta , \gamma } \kappa _ { \alpha \beta } ^ { i } \kappa _ { \gamma } \int _ { \mathbb { S } ^ { n - 1 } } \overline { x } ^ { \beta } \overline { x } ^ { \gamma } \, d S + \mathcal { O } ( \varepsilon ^ { n + 4 } ) \\ & = V _ { n } ( \varepsilon ) + \frac { C _ { 2 } \varepsilon ^ { n + 2 } } { 2 ( n + 2 ) } \sum _ { i = 1 } ^ { k } \sum _ { \alpha , \beta } ( \kappa _ { \alpha \beta } ^ { i } ) ^ { 2 } + \mathcal { O } ( \varepsilon ^ { n + 4 } ) \\ & = V _ { n } ( \varepsilon ) + \frac { V _ { n } ( \varepsilon ) \varepsilon ^ { 2 } } { 2 ( n + 2 ) } \sum _ { \alpha , \beta } ^ { n } \langle \Pi ( e _ { \alpha } , e _ { \beta } ) , \Pi ( e _ { \alpha } , e _ { \beta } ) \rangle + \mathcal { O } ( \varepsilon ^ { n + 4 } ) . \\ \text {Here the spherical integral is only nonzero when } \beta & = \gamma , \text { and the last term is the component} \\ \text {expression of equation } 3 . 1 . 4 . . & \prod _ { \alpha = 1 } ^ { \alpha } \partial _ { \alpha } \prod _ { \beta = 1 } ^ { \alpha } \partial _ { \beta }$$

thus, we are integrating a det g p x q over the ball B p n q p p ε q Ă T p M , which can be computed using the integrals in the appendix:

Here the spherical integral is only nonzero when β ' γ , and the last term is the component expression of equation 3.14. □

Proposition 4.3. The barycenter of the cylindrical component, for V as in the previous theorem, is

$$s ( C y l _ { p } ( \varepsilon , \mathbb { W } ) ) = 0 + \mathcal { O } ( \varepsilon ^ { 2 } ) .$$


<!-- p:13 -->


In the case V ' T p M , the barycenter is:

$$s ( C y l _ { p } ( \varepsilon ) ) = [ \, 0 , \, \frac { \varepsilon ^ { 2 } } { 2 ( n + 2 ) } \, H \, ] ^ { T } + \mathcal { O } ( \varepsilon ^ { 4 } ) . \\ \\$$

Proof. For generic V , approximating the manifold again by its tangent space, X ' r x , 0 ` O p ε 2 qs T , the normal component does not contribute until order two and the tangent component also vanishes at order 1 in ε . When V ' T p M , we saw that the integration domain reduces to a ball. The integrals of the tangent components x μ weighed by ? det g are of order O p ε n ` 4 q , since the first terms in the expansion have odd powers in the coordinates. On the other hand the normal components integrate as:

$$\begin{array} { c } \text {components integrate as:} \\ \\ V [ s ] ^ { j } = \int _ { \S ^ { n - 1 } } d \mathbb { S } \int _ { 0 } ^ { \Xi } f ^ { j } \sqrt { \det g } \rho ^ { n - 1 } d \rho = \int _ { \mathbb { S } ^ { n - 1 } } d \mathbb { S } \int _ { 0 } ^ { \Xi } \rho ^ { n - 1 } \left ( \frac { 1 } { 2 } \sum _ { \alpha , \beta } ^ { n } \kappa _ { \alpha \beta } ^ { j } \rho ^ { 2 } \overline { x } ^ { \alpha } \overline { x } ^ { \beta } + \mathcal { O } ( x ^ { 3 } ) \right ) d \rho \\ = \frac { \varepsilon ^ { n + 2 } } { 2 ( n + 2 ) } \sum _ { \alpha , \beta = 1 } ^ { n } \kappa _ { \alpha \beta } ^ { j } \int _ { \S ^ { n - 1 } } \overline { x } ^ { 0 } \overline { x } ^ { \beta } d \mathbb { S } + \mathcal { O } ( \varepsilon ^ { n + 4 } ) = \frac { C _ { \varepsilon } \varepsilon ^ { n + 2 } } { 2 ( n + 2 ) } \, H ^ { j } + \mathcal { O } ( \varepsilon ^ { n + 4 } ) , \\ \intertext { D i v iing by V = V ( C y _ { 1 } ( \varepsilon ) ) \text { cancels } C _ { 2 } \varepsilon ^ { n } = V _ { n } ( \varepsilon ) \text { to leading order.} } \Box$$

Dividing by V ' V p Cyl p p ε qq cancels C 2 ε n ' V n p ε q to leading order.

□

In order to study the eigenvalue decomposition of the covariance matrix we need to establish how to determine the limit eigenvectors and the first two terms of the series expansion of the eigenvalues, so that computing the integrals in an arbitrary orthonormal basis produces blocks identifiable in terms of the coordinate expressions of the second and third fundamental forms in that basis. An analogous result to the matrix expansion in [3] generalizes to higher codimension.

Lemma 4.4. Let C p ε q be an p n ` k qˆp n ` k q real symmetric matrix depending on a real parameter ε with convergent series expansion in a neighborhood of 0 such that:

$$C ( \varepsilon ) = \varepsilon ^ { 2 } \left ( \frac { a \, I d _ { n } \, | \, 0 _ { n \times k } } { 0 _ { k \times n } \, | \, 0 _ { k \times k } } \right ) + \varepsilon ^ { 4 } \left ( \frac { A _ { n \times n } \, | \, B _ { n \times k } } { B _ { k \times n } \, | \, \Gamma _ { k \times k } } \right ) + \mathcal { O } ( \varepsilon ^ { 5 } ) ,$$

where a ‰ 0 , and the blocks A , B , Γ are not completely zero. Let r V s J , r V s K denote the first n and last k components of a vector in R n ` k . Then the series of eigenvectors of C p ε q form an orthonormal basis of R n ` k that converges for ε Ñ 0 . The first n eigenvalues are λ μ p ε q ' aε 2 ` λ p 4 q μ ε 4 ` O p ε 5 q , where λ p 4 q μ and the corresponding limit eigenvectors t V p 0 q μ u n μ ' 1 satisfy the eigenvalue decomposition of A :

$$( \lambda _ { \mu } ^ { ( 4 ) } \, \text {Id} _ { n } - A ) \left [ V _ { \mu } ^ { ( 0 ) } \right ] _ { \top } = 0 _ { n \times 1 } , \quad \left [ V _ { \mu } ^ { ( 0 ) } \right ] _ { \perp } = 0 _ { k \times 1 } .$$

The last k eigenvalues are λ j p ε q ' λ p 4 q j ε 4 ` O p ε 5 q , where λ p 4 q j and the corresponding limit eigenvectors t V p 0 q j u n ` k j ' n ` 1 satisfy the eigenvalue decomposition of Γ :

$$( \lambda _ { j } ^ { ( 4 ) } \, \text {Id} _ { k } - \Gamma ) \, [ V _ { j } ^ { ( 0 ) } ] _ { \perp } = 0 _ { n \times 1 } , \quad [ V _ { j } ^ { ( 0 ) } ] _ { \top } = 0 _ { n \times 1 } .$$

Therefore, the fourth-order term of the eigenvalues is given by the eigenvalues of the blocks A and Γ , with the respective eigenvectors as the limit eigenvectors of C p ε q for ε Ñ 0 .


<!-- p:14 -->


Proof. The eigenvalue decomposition C p ε q V p ε q ' λ p ε q V p ε q can be written as a convergent series expansion in ε within a neighborhood of 0 for all Hermitian matrices of converging power series elements [30]:

$$\text {elements} \, [ 3 ] & \colon \\ & [ \, \varepsilon ^ { 2 } \left ( \frac { a \, I d _ { n } \, | \, 0 _ { n \times k } } { 0 _ { k \times n } \, | \, 0 _ { k \times k } } \right ) + \varepsilon ^ { 4 } \left ( \frac { A _ { n \times n } \, | \, B _ { n \times k } } { B _ { k \times n } \, | \, \Gamma _ { k \times k } } \right ) + \mathcal { O } ( \varepsilon ^ { 5 } ) \, ] \cdot [ V ^ { ( 0 ) } + V ^ { ( 1 ) } \varepsilon + V ^ { ( 2 ) } \varepsilon ^ { 2 } + \dots ] = \\ & = ( \lambda ^ { ( 1 ) } \varepsilon ^ { 1 } + \lambda ^ { ( 2 ) } \varepsilon ^ { 2 } + \lambda ^ { ( 3 ) } \varepsilon ^ { 3 } + \lambda ^ { ( 4 ) } \varepsilon ^ { 4 } + \dots ) [ V ^ { ( 0 ) } + V ^ { ( 1 ) } \varepsilon + V ^ { ( 2 ) } \varepsilon ^ { 2 } + \dots ] . \\ \intertext { The zero matrix C ( 0 ) is the limit $ \varepsilon \to 0 $ , with $\lambda ( 0 ) = \lambda ^ { ( 0 ) } = 0 $ as a totally degenerate }$$

The zero matrix C p 0 q is the limit when ε Ñ 0 , with λ p 0 q ' λ p 0 q ' 0 as a totally degenerate eigenvalue of multiplicity p n ` k q . By [30, ch. I, Th. 1], for ε ą 0 , this eigenvalue branches out into p n ` k q eigenvalues λ i p ε q with p n ` k q orthonormal eigenvectors V i p ε q , all convergent in a neighborhood of 0 . Thus, the vectors V p 0 q i ' lim ε Ñ 0 V i p ε q are a unique orthonormal basis of R n ` k that is completely determined by the perturbation matrix.

The eigenvalue difference between C p ε q and its full diagonalization is bounded by the matrix norm difference between them, which implies λ p 1 q ' λ p 3 q ' 0 , and also λ p 2 q i ' a , for i ' 1 , . . . , n , and λ p 2 q i ' 0 , for i ' n ` 1 , . . . , n ` k , since C p ε q is already diagonal up to that order. One can obtain the relations satisfied by λ p 4 q and V p 0 q equating order by order. At second order, λ p 2 q i ' a is nonzero for i ' 1 , . . . , n , hence

$$\left [ \left ( \frac { a \, \text {Id} _ { n } \, | \, 0 _ { n \times k } } { 0 _ { k \times n } \, | \, 0 _ { k \times k } } \right ) - \lambda _ { i } ^ { ( 2 ) } \, \text {Id} _ { n + k } \right ] V _ { i } ^ { ( 0 ) } & = \left ( \frac { 0 _ { n \times n } \, | \, \ 0 _ { n \times k } } { 0 _ { k \times n } \, | \, - a \, \text {Id} _ { k } } \right ) \, V _ { i } ^ { ( 0 ) } = 0 \\$$

implies that r V p 0 q μ s K ' 0 k ˆ 1 , for the limit of the first n eigenvectors. At fourth order we have

$$\ m a t h s c r { K } _ { 1 } ( \mu ^ { 2 } , \mu ^ { 1 } ) & = \ m a t h s c r { K } _ { 1 } ( 1 , 0 ) \ m a t h s c r { K } _ { 1 } ( 0 , 0 ) \ m a t h s c r { K } _ { 1 } ( 0 , 0 ) \\ [ \lambda _ { i } ^ { ( 4 ) } \, I d _ { n + k } - \left ( \frac { A _ { n \times n } \left | \, B _ { n \times k } \right ) } { B _ { k \times n } \left | \, \Gamma _ { k \times k } \right ) } \right ) V _ { i } ^ { ( 0 ) } = [ \left ( \frac { a \, I d _ { n } \left | \, 0 _ { n \times k } \right ) } { 0 _ { k \times n } \left | \, 0 _ { k \times k } \right ) } \right ) - \lambda _ { i } ^ { ( 2 ) } \, I d _ { n + k } ] \, V _ { i } ^ { ( 2 ) } ,$$

which in the present case, i ' 1 , . . . , n , makes the right-hand side become 0 for the first n rows. On the other hand, r V p 0 q i s K ' 0 k ˆ 1 makes B not contribute in the left-hand side, hence the first n rows lead to the equation:

$$( \lambda _ { i } ^ { ( 4 ) } \, I d _ { n } - A ) \, [ V _ { i } ^ { ( 0 ) } ] _ { \top } = 0 _ { n \times 1 } .$$

When i ' n ` 1 , . . . , n ` k , an analogous argument using λ p 2 q i ' 0 , leads to r V p 0 q i s J ' 0 n ˆ 1 , and in turn to:

$$( \lambda _ { i } ^ { ( 4 ) } \, I d _ { n } - \Gamma ) \left [ V _ { i } ^ { ( 0 ) } \right ] _ { \perp } & = 0 _ { k \times 1 } . \\$$

Since the limit eigenvectors are an orthonormal basis they cannot be zero and, therefore, the previous equations establish λ p 4 q i and the nonzero components of r V p 0 q i s as the eigenvalue decomposition of A and Γ , which always has a solution due to being symmetric matrices. □

The previous lemma is a fundamental step to establish the main theorem of this and the next section.

Theorem 4.5. For V P Gr p n, n ` k q such that V K X T p M ' t 0 u , i.e. for non-normal transversality, and when Cyl p p ε, V q is finite, the covariance matrix C p p ε, V q has as limit eigenvectors spanning T p M those corresponding to the first n eigenvalues, which scale as ε 2 . The other k eigenvalues scaling at higher order have limit eigenvectors that span N p M :


<!-- p:15 -->


$$\lambda _ { \mu } ( C y _ { p } ( \varepsilon , \mathbb { V } ) ) & = \frac { \varepsilon ^ { 2 } } { n + 2 } \ell _ { \mu } ^ { 2 } \, V _ { n } ( 1 ) \prod _ { \alpha = 1 } ^ { n } \ell _ { \alpha } + \, \mathcal { O } ( \varepsilon ^ { n + 3 } ) , \quad \mu = 1 , \dots , n , \\ \lambda _ { j } ( C y _ { n } ( \varepsilon , \mathbb { V } ) ) & = 0 + \mathcal { O } ( \varepsilon ^ { n + 3 } ) , \quad j = n + 1 , \dots , n + k ,$$

$$\lambda _ { j } ( C y l _ { p } ( \varepsilon , \mathbb { V } ) ) = 0 + \mathcal { O } ( \varepsilon ^ { n + 3 } ) , & & j = n + 1 , \dots , n + k ,$$

where l μ are the principal lengths of the ellipsoid in 4.2. When V ' T p M , let λ l r ̈s denote taking the l -th eigenvalue of a linear operator at p , or of its associated bilinar form with respect to the metric. Then the eigenvalues of the covariance matrix of the cylindrical component are:

$$\lambda _ { \mu } ( C y l _ { p } ( \varepsilon ) ) & = V _ { n } ( \varepsilon ) \left [ \frac { \varepsilon ^ { 2 } } { n + 2 } + \frac { \varepsilon ^ { 4 } } { 2 ( n + 2 ) ( n + 4 ) } \lambda _ { \mu } [ ( t r \Pi I ) \, I d _ { n } + 2 \, t r _ { \perp } \Pi I ] + \, O ( \varepsilon ^ { 6 } ) \right ] \\ \\ \lambda _ { \mu } ( C y l _ { p } ( \varepsilon ) ) & = V _ { n } ( \varepsilon ) \left [ \frac { \varepsilon ^ { 4 } } { n + 2 } \right ] \cdot \Gamma _ { \mu } \left [ \Gamma _ { \mu } \Pi ^ { 2 } I \right ] \Gamma _ { n } \Gamma _ { \mu } \left [ 6 \Gamma _ { \mu } \Gamma _ { n } \Gamma _ { \mu } \right ] \Phi ( \varepsilon ^ { 6 } ) \right ]$$

$$\mu ( n ) p ( n ) & = n ^ { ( n + 2 ) ( n + 2 ) ( n + 4 ) } \mu [ ( \mu ( n ) ) ^ { 2 } - 2 ( n + 2 ) ( n + 4 ) ] ^ { 2 } - ( 1 ) ^ { 2 } ] \\ \lambda _ { j } ( C y _ { 1 } ( \varepsilon ) ) & = V _ { n } ( \varepsilon ) \left [ \frac { \varepsilon ^ { 4 } } { 4 ( n + 2 ) ( n + 4 ) } \lambda _ { j } [ H \otimes H + 2 \text {tr} _ { \| } \Pi \Pi ] + \mathcal { O } ( \varepsilon ^ { 6 } ) \right ] \\ \\ f _ { n } ( u _ { 1 } ) & = 1 - 2 ( n + 1 ) .$$

for all μ ' 1 , . . . , n , and j ' n ` 1 , . . . , n ` k . Moreover, the corresponding first n eigenvectors converge to the principal directions of the operator tr K III ' p S H  ́ p R , and the last k eigenvectors to those of H b H ` 2tr ‖ III .

Proof. For generic V the manifold is again approximated by its tangent space as X ' r x , 0 s T , which produces no contribution to the normal block at leading order O p ε n ` 2 q . Choosing the tangent orthonormal basis to be aligned with the principal axis of the ellipsoid, and changing variables so that x μ ' y μ l μ , the tangent block becomes an integration over a ball:

$$\text {Variables so that } x ^ { \prime \prime } = y ^ { \ell - \ell _ { \mu } } , \, \text {the tangent block becomes an integration over a ball} . \\ [ C ( C y _ { p } ( \varepsilon , \mathbb { V } ) ) ] ^ { \mu \nu } = \int _ { x ^ { T } A . A ^ { T } x \leqslant \varepsilon ^ { 2 } } x ^ { \mu } x ^ { \nu } \, d x = \int _ { \sum _ { y ^ { 2 } } y _ { \mu } ^ { 2 } y ^ { \ell } \ell _ { \mu } \ell _ { \nu } } \prod _ { \alpha = 1 } ^ { n } \ell _ { \alpha } \, d ^ { n } y \\ = \delta _ { \mu \nu } \frac { \varepsilon ^ { n + 2 } } { n + 2 } \ell _ { \mu } \ell _ { \nu } V _ { n } ( 1 ) \prod _ { \alpha = 1 } ^ { n } \ell _ { \alpha } + \mathcal { O } ( \varepsilon ^ { n + 3 } ) . \\ \text {Thus, the covariance matrix leading term is proportional to diag( \ell _ { n } ^ { 2 } , \dots , \ell _ { n } ^ { 2 } , 0 , \dots , 0 ), which has}$$

Thus, the covariance matrix leading term is proportional to diag p l 2 1 , . . . , l 2 n , 0 , . . . , 0 q , which has limit eigenvectors corresponding to the first n eigenvalues spanning T p M , and the other k eigenvectors spanning N p M , by an straightforward extension to lemma 4.4 at order ε 2 .

For V ' T p M , we shall compute the integrals of the matrix blocks r x μ x ν s n μ,ν ' 1 , and r f i f j s k i, j ' 1 , so the next-to-leading order elements of those blocks will suffice to obtain the eigenvalues and limit eigenvectors by the results of the previous lemma. The tangent block is:

$$\lim i t e g e n v e c t o r s \, b y \, b e r s \, \left ( \begin{array} { c c c } \lim i t e g e n v e c t o r s \, b y & \text {the previous lemma. The tangent block is:} \\ \\ [ C ( C y _ { p } ( \varepsilon ) ) ] ^ { \mu \nu } & = \int _ { B ^ { ( n ) } ( \varepsilon ) } x ^ { \mu } x ^ { \nu } \sqrt { \det g ( x ) } \, d ^ { n } x \\ \\ \\ [ \int _ { \mathbb { S } ^ { n - 1 } } d \int _ { 0 } ^ { \varepsilon } \rho ^ { n + 1 } \overline { x } ^ { \mu } \overline { x } ^ { \nu } \left ( 1 + \frac { k } { 2 } \sum _ { i = 1 } ^ { n } \sum _ { \alpha = 1 } \left [ \sum _ { \beta = 1 } ^ { n } \kappa _ { \alpha \beta } ^ { j } \rho ^ { \varepsilon } \overline { x } ^ { \beta } \right ] ^ { 2 } + \mathcal { O } ( x ^ { 3 } ) \right ) \rho ^ { d o } \\ \\ [ \varepsilon ^ { n + 2 } ] & = \frac { \varepsilon ^ { n + 2 } } { n + 2 } \int _ { \mathbb { S } ^ { n - 1 } } \overline { x } ^ { \mu } \overline { x } ^ { \nu } d \mathbb { S } + \frac { \varepsilon ^ { n + 4 } } { 2 ( n + 4 ) } \sum _ { i = 1 } ^ { k } \sum _ { \alpha = 1 , \beta , \gamma } \kappa _ { \alpha \beta } \kappa _ { \alpha \gamma } ^ { i } \int _ { \mathbb { S } ^ { n - 1 } } \overline { x } ^ { \mu } \overline { x } ^ { \nu } \overline { x } ^ { \gamma } d \mathbb { S } + \mathcal { O } ( \varepsilon ^ { n + 6 } ) ,$$


<!-- p:16 -->


and the last integral is only nonzero for the following combination of indices using the notation in the appendix

This simplifies the sums using the relationship between C 4 , C 22 and C 2 , and writing p 1  ́ δ μν q to enforce μ ‰ ν in the last two terms of C 22 :

$$& \text {in the appendix} \\ & \quad \int _ { \mathbb { S } ^ { n - 1 } } \overline { x } ^ { \mu } \overline { x } ^ { \nu } \overline { x } ^ { \gamma } \, d \mathbb { S } = C _ { 4 } ( \overline { \mu \nu \beta \gamma } ) + C _ { 2 2 } \left [ ( \overline { \mu \nu \beta \gamma } ) + ( \overline { \mu \nu \beta \gamma } ) + ( \overline { \mu \nu \beta \gamma } ) \right ] . \\ & \text {This simplifies the sums using the relationship between } C _ { 4 } , C _ { 2 2 } \text { and } C _ { 2 } , \text { and writing } ( 1 - \delta _ { \mu \nu } ) \text { to }$$

$$& \text {This simplifies the sums using the relationship between } C _ { 4 } , C _ { 2 2 } \text { and } C _ { 2 } , \text { and writing } ( 1 - \delta _ { \mu \nu } ) \text { to } \\ & \text {enforce } \mu \neq \nu \text { in the last two terms of } C _ { 2 2 } \\ & \quad \frac { \delta _ { \mu } C _ { 2 } n ^ { + 2 } } { n + 2 } + \frac { C _ { 2 } n ^ { + 4 } } { 2 ( n + 2 ) ( n + 4 ) } \sum _ { i = 1 } ^ { k } \left [ 3 \delta _ { \mu \nu } \sum _ { \alpha = 1 } ^ { n } ( \kappa _ { \alpha \mu } ^ { i } ) ^ { 2 } + \delta _ { \mu \nu } \sum _ { \alpha , \beta \neq \mu } ^ { n } ( \kappa _ { \alpha \beta } ^ { i } ) ^ { 2 } + 2 ( 1 - \delta _ { \mu \nu } ) \sum _ { \alpha = 1 } ^ { n } k _ { \alpha \mu } ^ { i } \kappa _ { \alpha \nu } \right ] + \dots \\ & = V _ { n } ( \varepsilon ) \frac { \varepsilon ^ { 2 } } { n + 2 } \delta _ { \mu \nu } + \frac { V _ { n } ( \varepsilon ) \varepsilon ^ { 4 } } { 2 ( n + 2 ) ( n + 4 ) } \left [ \delta _ { \mu \nu } \sum _ { i = 1 , \alpha , \beta } ^ { k } \sum _ { \substack { i = 1 , \alpha , \beta \\ i = 1 } } ^ { n } ( k _ { \alpha \mu } ^ { i } \sum _ { \alpha = 1 } ^ { n } \sum _ { \substack { i = 2 \\ i = 1 } } ^ { k } \sum _ { \alpha \mu } ^ { n } k _ { \alpha \mu } ^ { i } \kappa _ { \alpha \nu } \right ] + \mathcal { O } ( \varepsilon ^ { n + 0 } ) \\ & = \frac { V _ { n } ( \varepsilon ) ^ { 2 } } { n + 2 } \delta _ { \mu \nu } + \frac { V _ { n } ( \varepsilon ) \varepsilon ^ { 4 } } { 2 ( n + 2 ) ( n + 4 ) } \left ( \delta _ { \mu \nu } \sum _ { \alpha , \beta } ^ { n } \| \Pi ( e _ { \alpha } , e _ { \beta } ) \| ^ { 2 } + 2 \sum _ { \alpha = 1 } ^ { n } \langle \Pi ( e _ { \alpha } , e _ { \mu } ) , \Pi ( e _ { \alpha } , e _ { \nu } ) \rangle \right ) + \mathcal { O } ( \varepsilon ^ { n + 6 } ) . \\ & \text {The component expression of equations } 3 . 1 5 \text { and } 3 . 1 7 \text { identify this block matrix at order } \mathcal { O } ( \varepsilon ^ { n + 4 } ) \\ & \text {as the matrix elements of the operator } \left [ ( \text {tr} _ { 1 } \Pi _ { 1 } \Pi _ { n } ) I _ { n } + 2 \text {tr} _ { 1 } \Pi _ { 1 } \Pi _ { n } \right ] \text { in our chosen orthogonal}$$

We perform now the integration of the normal block, which truncated to leading order yields:

The component expression of equations 3.15 and 3.17 identify this block matrix at order O p ε n ` 4 q as the matrix elements of the operator rp tr ‖ tr K III q Id n ` 2tr K III s in our chosen orthonormal basis, whose eigenvalues are then by lemma 4.4 the next-to-leading order contribution to the first n eigenvalues of C p Cyl p p ε qq , and whose eigenvectors are the limit eigenvectors of C p Cyl p p ε qq .

$$\text {we perform how the integration of the normal block, which truncated to leading order yields.} \\ [ C ( C y l _ { p } ( \varepsilon ) ) ] ^ { i j } = \int _ { B ^ { ( n ) } ( \varepsilon ) } f ^ { i } ( x ) f ^ { j } ( x ) d ^ { n } x + \dots = \int _ { \varsigma ^ { n - 1 } } d \mathbb { S } \int _ { 0 } ^ { \varepsilon } \frac { \rho ^ { n + 3 } } { 4 } d \rho \sum _ { \alpha , \beta , \gamma , \delta } ^ { n } \sum _ { \kappa _ { \alpha \beta } \kappa _ { \gamma \delta } ^ { j } = \overline { x } ^ { \alpha } \overline { x } ^ { \beta } \overline { x } ^ { \gamma } \overline { x } ^ { \delta } } + \mathcal { O } ( \varepsilon ^ { n + 6 } ) \\ \text {where the angular integral is only nonzero in the same cases as in equation 4.11 above, but}$$

$$with \text { the indices related accordingly.  This again simplifies every summation by matching the
 combination of indices and using the relations among the constants: } \\ [ C ( C y l _ { p } ( \varepsilon ) ) ] ^ { i j } = \frac { \varepsilon ^ { n + 4 } } { 4 ( n + 4 ) } \left [ C _ { \alpha } \sum _ { \alpha = 1 } ^ { n } \kappa _ { \alpha \kappa } ^ { i } \kappa _ { \alpha } + C _ { 2 2 } \left ( \sum _ { \alpha , \gamma } \kappa _ { \alpha \gamma } ^ { i } \gamma + 2 \sum _ { \alpha , \beta } \kappa _ { \beta \alpha } ^ { i } \beta _ { \alpha } \right ) \right ] + \mathcal { O } ( \varepsilon ^ { n + 6 } ) \\ = \frac { C _ { 2 } \varepsilon ^ { n + 4 } } { 4 ( n + 2 ) ( n + 4 ) } \left [ 3 \sum _ { \alpha = 1 } ^ { n } I ^ { i } ( e _ { \alpha } , e _ { i } ) I ^ { j } ( e _ { i } , e _ { \alpha } ) + \sum _ { \alpha , \gamma } I ^ { i } ( e _ { \alpha } , e _ { i } ) I ^ { j } ( e _ { i } , e _ { \alpha } ) + \\ + 2 \sum _ { \alpha , \beta } I ^ { i } ( e _ { \alpha } , e _ { \beta } ) I ^ { j } ( e _ { \alpha } , e _ { \beta } ) \right ] + \mathcal { O } ( \varepsilon ^ { n + 6 } ) , \\ \intertext { in which the first sum precisely completes the elements missing from the other two } = \frac { V _ { n } ( \varepsilon ) \varepsilon ^ { 2 } } { V _ { n } ( \varepsilon ) \varepsilon ^ { 2 } } = \left [ \left ( \sum _ { \alpha } I ^ { i } \psi ( e _ { \alpha } , e _ { i } ) \right ) \left ( \sum _ { \alpha } I ^ { j } \psi ( e _ { \alpha } , e _ { i } ) \right ) + 2 \sum _ { \alpha } I ^ { i } \psi ( e _ { \alpha } , e _ { i } ) I ^ { j } ( e _ { \alpha } , e _ { i } ) \right ] + \mathcal { O } ( \varepsilon ^ { n + 6 } )$$

where the angular integral is only nonzero in the same cases as in equation 4.11 above, but with the indices relabeled accordingly. This again simplifies every summation by matching the combination of indices and using the relations among the constants:

in which the first sum precisely completes the elements missing from the other two

$$& \quad \text {in which the first sum precisely completes the elements missing from the other two} \\ & = \frac { V _ { n } ( \varepsilon ) \varepsilon ^ { 2 } } { 4 ( n + 2 ) ( n + 4 ) } \left [ \left ( \sum _ { \alpha = 1 } ^ { n } \Pi ^ { i } ( e _ { \alpha } , e _ { \alpha } ) \right ) \left ( \sum _ { \gamma = 1 } ^ { n } \mathbb { I } ^ { j } ( e _ { \gamma } , e _ { \gamma } ) \right ) + 2 \sum _ { \alpha , \beta } ^ { n } \mathbb { I } ^ { i } ( e _ { \alpha } , e _ { \beta } ) \mathbb { I } ^ { j } ( e _ { \alpha } , e _ { \beta } ) \right ] + \mathcal { O } ( \varepsilon ^ { n + 6 } ) .$$


<!-- p:17 -->


In this last expression we clearly identify the components r H b H s ij , and those of 2tr ‖ III using the definition of H and equation 3.16. □

We shall see below that the spherical covariance matrix has the same normal eigenvalues, to leading order, as the cylindrical case above. In [31,32] these were expressed as an average of the squares of the curvatures of curves inside the manifold M . Therefore, our previous computation provides an explicit formula for this interpretation of the normal eigenvalues.

Corollary 4.6. Let M be an n -dimensional submanifold of Euclidean space R n ` k , then the first generalized curvatures κ p γ, x , n j q of curves γ Ă M passing through p with tangent vector x and principal normal vectors any of the eigenvectors n j , j ' 1 , . . . , k , of r H b H ` 2tr ‖ III s , integrate to:

In particular:

$$t o & \colon \\ & \frac { 1 } { V _ { n } ( \varepsilon ) } \int _ { B ^ { ( n ) } ( \varepsilon ) } \kappa ^ { 2 } ( \gamma , x , n _ { j } ) \, d ^ { n } x = \frac { \varepsilon ^ { 4 } } { ( n + 2 ) ( n + 4 ) } \lambda _ { j } [ H \otimes H + 2 \text {tr} \, | | \Pi | | . \\ I n \ p a r t i c u l a r { \colon }$$

$$\sum _ { j = 1 } ^ { k } \frac { 1 } { V _ { n } ( \varepsilon ) } \int _ { B ^ { ( n ) } ( \varepsilon ) } \kappa ^ { 2 } ( \gamma , x , n _ { j } ) \, d ^ { n } x & = \frac { 3 \| H \| ^ { 2 } - 2 \mathcal { R } } { ( n + 2 ) ( n + 4 ) } \varepsilon ^ { 4 } .$$

## 5. Spherical Covariance Analysis

The difference between the cylindrical and spherical intersection domains for a graph manifold lies in the irregular projection onto the tangent space: by definition the cylinder is the extension in the normal directions of the ball B p n q p p ε q Ă T p M , so the points of the graph manifold satisfy } proj T p M pr x , f p x qs T q} ' } x } ď ε , and thus the integration region is a perfect ball. However, in the spherical case the domain of integration is } x } 2 `} f p x q} 2 ď ε 2 , which is nontrivial and in general cannot be parametrized exactly. One can nevertheless apply the same procedure as done originally in [29] and [3] to find the leading order corrections to the ball domain.

Lemma 5.1. For ε ą 0 small enough so that M is a graph manifold over T p M , using cylindrical coordinates, the radial parametric equation of a point X ' r ρx 1 , . . . , ρx n , f 1 p ρ x q , . . . , f k p ρ x qs T in B D p p ε q ' M X S n p p ε q , is

$$r ( \overline { x } ) \coloneqq \rho ( \overline { x } _ { 1 } , \dots , \overline { x } _ { n } ) = \varepsilon - \frac { K ( \overline { x } ) ^ { 2 } } { 8 } \varepsilon ^ { 3 } + \mathcal { O } ( \varepsilon ^ { 4 } ) ,$$

where x P S n  ́ 1 Ă T p M , and

$$K ( \overline { x } ) ^ { 2 } \colon = \| I ( \overline { x } , \overline { x } ) \| ^ { 2 } = \sum _ { i = 1 } ^ { k } \sum _ { \alpha , \beta } ^ { n } \sum _ { \gamma , \delta } ^ { n } \kappa _ { \alpha \beta } ^ { i } \kappa _ { \gamma \delta } ^ { i } \overline { x } ^ { \alpha } \overline { x } ^ { \beta } \overline { x } ^ { \gamma } \overline { x } ^ { \delta } \\ \intertext { a r e f t h e a m b i e n t s p a c e l e r a t i o n $ o f $ a a d e s i c s $ c u r v e $ o f $ M $ w i t h $ t a n g e n $ t \overline { r } $ a t $ n }$$

is the square of the ambient space acceleration of a geodesic curve of M with tangent x at p .

Proof. A point of the spherical boundary satisfies } x } 2 ` ř k i ' 1 p f i p x qq 2 ' ε 2 . Since } x } 2 ' ρ 2 , and f i p x q ' 1 2 ř n α,β κ i αβ x α x β ` O p x 3 q , it is immediate that

$$\beta ^ { k } _ { \alpha \beta } x ^ { l } & \ x ^ { l } + O ( x ^ { l } ) , \, l \text { is infinite that} \\ \rho ^ { 2 } + \frac { 1 } { 4 } \rho ^ { 4 } \sum _ { i = 1 } ^ { k } \left ( \sum _ { \alpha , \beta } ^ { n } \kappa _ { \alpha \beta } ^ { i } \overline { x } ^ { \alpha } \overline { x } ^ { \beta } \right ) ^ { 2 } - \varepsilon ^ { 2 } = \mathcal { O } ( \rho ^ { 5 } ) .$$


<!-- p:18 -->


Defining K p x q 2 as the coefficient of ρ 4 4 , we can solve the equation to order four to get

whose square root yields the result. Note that the actual error may be of order four because this could contribute at order fie upon squaring the expression, which is the order neglected in the original equation. In our chosen orthonormal basis at p , we have that II p x , x q ' ř k i ' 1  ́ ř n α,β κ i αβ x α x β  ̄ n i , and this is precisely the ambient space acceleration of a geodesic of M , cf. [25, ch. 4, Cor. 10]. □

$$\rho ^ { 2 } & = \frac { 2 } { K ( \overline { x } ) ^ { 2 } } \left ( - 1 + \sqrt { 1 + K ( \overline { x } ) ^ { 2 } \varepsilon ^ { 2 } } \right ) = \varepsilon ^ { 2 } - \frac { 1 } { 4 } K ( \overline { x } ) ^ { 2 } \varepsilon ^ { 4 } + \mathcal { O } ( \varepsilon ^ { 6 } ) , \\ \intertext { e s q u a r e \, r o t \, y e l d s \, t h e \, r e s l u t . \, \ N o t e \, t h a t \, t h e \, a t u a l \, e r r o w \, y a m y \, b e \, o f \, o r d e \, f o u r }$$

Proposition 5.2. The n -dimensional volume of the spherical component is

$$\text {position} \ 5 . 2 . \ 1 h e ^ { - \alpha } \text {m/s} \text {on} \ v o m e \ 0 \text {j} \text { the sphemic call} \text { component} \ i s \\ V ( D _ { p } ( \varepsilon ) ) = V _ { n } ( \varepsilon ) \left [ 1 + \frac { \varepsilon ^ { 2 } } { 8 ( n + 2 ) } \ \left ( 2 \text {tr} \text {II} - \| H \| ^ { 2 } \right ) + \mathcal { O } ( \varepsilon ^ { 3 } ) \right ] \\ \text {re} \ 2 \text {tr} \text {II} \, U = \| H \| ^ { 2 } = \| H \| ^ { 2 } - 2 \mathcal { R }$$

where 2tr III  ́} H } 2 ' } H } 2  ́ 2 R .

Proof. In contrast to the proof of the cylindrical domain, the radial integration introduces new angular corrections due to r p x q :

the second integral is the same to leading order as in the cylindrical case, hence

$$\text {angular corrections due to } r ( \overline { x } ) & \colon \\ & V ( D _ { p } ( \varepsilon ) ) = \int _ { \mathbb { S } ^ { n - 1 } } d \mathbb { S } \int _ { 0 } ^ { \overline { x } ( \overline { x } ) } \rho ^ { n - 1 } \sqrt { \det g ( \rho \overline { x } ) } \, d \rho \\ & = \int _ { \mathbb { S } ^ { n - 1 } } \frac { r ( \overline { x } ) ^ { n } } { n } d \mathbb { S } + \int _ { \mathbb { S } ^ { n - 1 } } \frac { r ( \overline { x } ) ^ { n + 2 } } { 2 ( n + 2 ) } \sum _ { i = 1 } ^ { k } \sum _ { \alpha , \beta , \gamma } \kappa _ { \alpha \beta } \kappa _ { \gamma \alpha } ^ { i } \overline { x } ^ { \beta } \overline { x } ^ { \gamma } \, d \mathbb { S } + \mathcal { O } ( \varepsilon ^ { n + 3 } ) , \\ \intertext { the second integral is the same to leading order as in the cylindrical case, hence }$$

$$the \text { second integral is the same to leading order as in the cylindrical case, hence} \\ = \int _ { \mathbb { S } ^ { n - 1 } } d \mathbb { S } \frac { \varepsilon ^ { n } } { n } \left [ 1 - n \frac { K ( \bar { x } ) ^ { 2 } } { 8 } \varepsilon ^ { 2 } + \mathcal { O } ( \varepsilon ^ { 3 } ) \right ] + \frac { V _ { n } ( \varepsilon ) \, \varepsilon ^ { 2 } } { 2 ( n + 2 ) } \text {tr} \, \Pi \, I + \mathcal { O } ( \varepsilon ^ { n + 3 } ) \\ = V _ { n } ( \varepsilon ) - \frac { \varepsilon ^ { n + 2 } } { 8 } \sum _ { i = 1 } ^ { n } \sum _ { \alpha , \beta } \kappa _ { \alpha \beta } ^ { i } \kappa _ { \delta } ^ { i } \int _ { \mathbb { S } ^ { n - 1 } } \overline { x } ^ { \alpha } \overline { x } ^ { \gamma } \overline { x } ^ { \gamma } \, d \mathbb { S } + \frac { V _ { n } ( \varepsilon ) \, \varepsilon ^ { 2 } } { 2 ( n + 2 ) } \text {tr} \, \Pi \, I + \mathcal { O } ( \varepsilon ^ { n + 3 } ) , \\ \text {where the integral is only nonzero as in equation 4.11, so}$$

$$& \text {where the integral is only nonzero as in equation 4.11, so} \\ & = V _ { n } ( \varepsilon ) - \frac { C _ { 2 } \varepsilon + n ^ { 2 } } { 8 ( n + 2 ) } \sum _ { i = 1 } ^ { k } \left [ 3 \sum _ { \substack { n = 1 \\ \alpha = 1 } } ^ { n } ( \kappa _ { \alpha \alpha } ^ { i } ) ^ { 2 } + \sum _ { \substack { \alpha , \gamma \\ \alpha \neq \gamma } } ^ { n } \kappa _ { \alpha \alpha } ^ { i } \kappa _ { \gamma \gamma } ^ { i } + 2 \sum _ { \substack { \alpha , \beta \\ \alpha , \beta } } ^ { n } ( \kappa _ { \alpha \beta } ^ { i } ) ^ { 2 } \right ] + \frac { V _ { n } ( \varepsilon ) \, \varepsilon ^ { 2 } } { 2 ( n + 2 ) } \text {tr} \, I I I + \mathcal { O } ( \varepsilon ^ { n + 3 } ) \\ & = V _ { n } ( \varepsilon ) \left [ 1 + \frac { \varepsilon ^ { 2 } } { 8 ( n + 2 ) } \left ( 4 \text {tr} \, I I I - \sum _ { i = 1 } ^ { k } \sum _ { \alpha , \gamma } ^ { n } \kappa _ { \alpha \alpha } ^ { i } \kappa _ { \gamma } - 2 \sum _ { i = 1 } ^ { k } \sum _ { \alpha , \beta } ^ { n } ( \kappa _ { \alpha \beta } ^ { i } ) ^ { 2 } \right ) + \mathcal { O } ( \varepsilon ^ { 3 } ) \right ] \\ & \text {Now, the first set of sums in the braces is } \langle \sum _ { \alpha } I I ( e _ { \alpha } , e _ { \alpha } ) , \sum _ { \gamma } I I ( e _ { \gamma } , e _ { \gamma } ) \rangle = \| H \| ^ { 2 } , \text { and the second} \\ & \text {set is tr} \, I I I .$$

where the integral is only nonzero as in equation 4.11, so

Now, the first set of sums in the braces is x ř α II p e α , e α q , ř γ II p e γ , e γ q y ' } H } 2 , and the second set is tr III . □

Remark 5.3 . Notice that it is not known the dependence of the error generated by the irregular radius r p x q , O p ε n ` 3 q in the previous proof, and whether it cancels at that order upon spherical integration, so the spherical component invariants may have error terms at lower order than the cylindrical ones.


<!-- p:19 -->


Proposition 5.4. The barycenter of the spherical component is to leading order the same as for the cylindrical component:

$$s ( D _ { p } ( \varepsilon ) ) = [ \, 0 , \, \frac { \varepsilon ^ { 2 } } { 2 ( n + 2 ) } \, H \, ] ^ { T } + \mathcal { O } ( \varepsilon ^ { 4 } ) . \\ \\ + \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf f \colon \mathbf f \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \colon \mathbf i \$$

Proof. The new contributions from r p x q to the cylindrical computations are at least of the same order, O p ε 4 q , as the overall error. □

The covariance integral invariants for the spherical domain were obtained for hypersurfaces in [3] by performing the computations in the basis of principal and normal directions. In arbitrary codimension, the different osculating paraboloids of f i p x q , i ' 1 , . . . , k , cannot be diagonalized simultaneously to a common basis in general. The amount of terms and simplifications needed in this general case is of much higher complexity than for hypersurfaces but, nevertheless, an analogous result for the eigenvalue decomposition obtains.

Theorem 5.5. Let λ l r ̈s denote taking the l -th eigenvalue of a linear operator at p , or of its associated bilinar form with respect to the metric. Then the eigenvalues of the covariance matrix of the spherical component are:

$$\sigma \, \text {the spherical curvature} \, \sigma \, \text {neq} \, \sigma \, \text { here} \colon \\ \lambda _ { \mu } ( D _ { p } ( \varepsilon ) ) = V _ { n } ( \varepsilon ) \left [ \frac { \varepsilon ^ { 2 } } { n + 2 } + \frac { \varepsilon ^ { 4 } } { 8 ( n + 2 ) ( n + 4 ) } \lambda _ { \mu } [ ( 2 \, \text {tr} \, \Pi \, \text {I} - \| H \| ^ { 2 } ) I d _ { n } - 4 \hat { S } _ { H } ] + \mathcal { O } ( \varepsilon ^ { 5 } ) \right ] \\ \lambda _ { j } ( D _ { p } ( \varepsilon ) ) = V _ { n } ( \varepsilon ) \left [ \frac { \varepsilon ^ { 4 } } { 2 ( n + 2 ) ( n + 4 ) } \lambda _ { j } [ \text {tr} \, \Pi \, \text {I} - \frac { 1 } { n + 2 } H \otimes H ] + \mathcal { O } ( \varepsilon ^ { 6 } ) \right ]$$

$$\mu ( \rho ( \tau ) ) = & \left [ n + 2 \left ^ { n } \, 8 ( n + 2 ) ( n + 4 ) \right ^ { \mu } \rho ( \tau ) \right ] ^ { n } \| \tau \| ^ { n } + \mu ^ { 2 } H \right ] ^ { 2 } \\ \lambda _ { j } ( D _ { p } ( \varepsilon ) ) = & \, V _ { n } ( \varepsilon ) \left [ \frac { \varepsilon ^ { 4 } } { 2 ( n + 2 ) ( n + 4 ) } \lambda _ { j } [ \tt r \, \Pi \left \| \Pi - \frac { 1 } { n + 2 } H \otimes H \right ] + \mathcal { O } ( \varepsilon ^ { 6 } ) \right ] \\ & \quad \ \ f o r \, \ a l l \, u = 1 \quad n \, p \, \ e n d \, j \, \frac { n } { n } \, p \, n + 1 \quad n \, p \, k \, \ u o r w a r r \, \ t h e \, o r m o n p e n d i n g \, f r o t \, n \, \ e q i n e w a r t o r e \\$$

for all μ ' 1 , . . . , n , and j ' n ` 1 , . . . , n ` k . Moreover, the corresponding first n eigenvectors converge to the principal directions of the Weingarten operator at H , i.e., p S H , and the last k eigenvectors to those of r tr ‖ III  ́ 1 n ` 2 H b H s .

Proof. From lemma 4.4 again, only the tangent and normal blocks need to be computed. Now, however, the covariance matrix is taken with respect to the barycenter, so there is an extra matrix contribution from the tensor product,

$$\text {from the tensor} \ p d u c { t } , \\ C ( D _ { p } ( \varepsilon ) ) = \int _ { D _ { p } ( \varepsilon ) } X \otimes X \ d V o l - \int _ { D _ { p } ( \varepsilon ) } X \otimes s \ d V o l , \\$$

because the other two products cancel each other upon integration. From the proof of the barycenter formula, this integral is to leading order:

$$\text {barycenter formula, this integral is to leading order:} \\ \int _ { D _ { p } ( \varepsilon ) } X \otimes d V o l = V ( D _ { p } ( \varepsilon ) ) s \otimes s = \left ( \frac { \mathcal { O } ( \varepsilon ^ { n + 8 } ) _ { n \times n } \, | \, \mathcal { O } ( \varepsilon ^ { n + 6 } ) _ { n \times k } } { \mathcal { O } ( \varepsilon ^ { n + 6 } ) _ { k \times n } \, | \, \frac { V _ { n } ( \varepsilon ) e ^ { 4 } } { 4 ( n + 2 ) ^ { 2 } } H \otimes H } \right ) \\ \text {There is no difference in the normal block computations of this covariance matrix and the cylin-}$$

There is no difference in the normal block computations of this covariance matrix and the cylindrical case proved before, since the corrections coming from r p x q are O p ε n ` 6 q . Thus, subtracting the barycenter contribution:

$$\frac { V _ { n } ( \varepsilon ) \varepsilon ^ { 4 } } { 4 ( n + 2 ) ( n + 4 ) } ( H \otimes H + 2 \, t r \, \| \Pi H ) - \frac { V _ { n } ( \varepsilon ) \varepsilon ^ { 4 } } { 4 ( n + 2 ) ^ { 2 } } H \otimes H = \frac { V _ { n } ( \varepsilon ) \varepsilon ^ { 4 } } { 2 ( n + 2 ) ( n + 4 ) } ( \, t r \, \| \Pi H - \frac { 1 } { n + 2 } H \otimes H ) .$$


<!-- p:20 -->


For the tangent block, the number of correction terms due to the spherical domain irregularities with respect to the cylindrical case makes a substantial contribution at O p ε n ` 4 q :

$$\text {with respect to the cylindrical case makes a substantial contribution at } \mathcal { O } ( \varepsilon ^ { n + 4 } ) \colon \\ [ C ( D _ { \rho } ( \varepsilon ) ) ] ^ { \mu \nu } & = \int _ { \mathbb { S } ^ { n - 1 } } d \int _ { 0 } ^ { r ( \bar { x } ) } \rho ^ { n + 1 } \overline { x } ^ { \mu } \overline { x } ^ { \nu } \left ( 1 + \frac { 1 } { 2 } \sum _ { i = 1 } ^ { k } \sum _ { \alpha = 1 } ^ { n } \left [ \sum _ { \beta } \kappa _ { \alpha \beta } ^ { i } \rho \overline { x } ^ { \beta } \right ] ^ { 2 } + \mathcal { O } ( x ^ { 3 } ) \right ) d \rho \\ & = \frac { \varepsilon ^ { n + 2 } } { n + 2 } \left [ \delta _ { \mu } C _ { 2 } - ( n + 2 ) \int _ { \mathbb { S } ^ { n - 1 } } \overline { x } ^ { \mu \nu } \frac { K ( \bar { x } ) ^ { 2 } } { 8 } \frac { d \varepsilon } { 8 } d \mathbb { S } + \mathcal { O } ( \varepsilon ^ { 3 } ) \right ] \\ & \quad + \frac { \varepsilon ^ { n + 4 } } { 2 ( n + 4 ) } \sum _ { i = 1 } ^ { k } \sum _ { \alpha , \beta , \gamma } \kappa _ { \alpha \beta } ^ { i } \kappa _ { \gamma } ^ { i } \int _ { \mathbb { S } ^ { n - 1 } } \overline { x } ^ { \mu \nu } \overline { x } ^ { \beta \overline { x } } \overline { x } ^ { \alpha \overline { s } } + \dots \\ & = \delta _ { \mu \nu } \frac { V _ { n } ( \varepsilon ) \varepsilon ^ { 2 } } { n + 2 } + \frac { \varepsilon ^ { n + 4 } } { 2 ( n + 4 ) } \sum _ { i = 1 } ^ { k } \sum _ { \alpha = 1 , \beta , \gamma } \kappa _ { \alpha \beta } ^ { i } \kappa _ { \gamma } ^ { i } C _ { ( \mu \beta ) \gamma } ) - \frac { n + 4 } { 4 } \sum _ { \alpha , \beta , \gamma , \delta } ^ { n } \sum _ { \gamma , \delta } \kappa _ { \alpha \beta } ^ { i } \kappa _ { \gamma } ^ { i } C _ { ( \mu \alpha \beta , \gamma \delta ) } \right ] + \mathcal { O } ( \varepsilon ^ { n + 5 } ) , \\ & \quad \text {where we have made use of equation } 5 . 2 , \text { and written } C _ { ( \alpha \beta , \dots ) } \text { for the integral over } \mathbb { S } ^ { n - 1 } \text { of the } \text {monomial product } \overline { x } ^ { \alpha } \overline { x } ^ { \beta } \dots ( \text {notice here the indices are not exponents but coordinate compo-}$$

where we have made use of equation 5.2, and written C p αβ... q for the integral over S n  ́ 1 of the monomial product x α x β . . . , (notice here the indices are not exponents but coordinate components). The first summation simplifies again with equation 4.11 to yield the cylindrical tangent block, but the other set of sums comprises the 31 spherical integrals of all possible monomials of degree six:

$$C _ { ( \mu \nu \alpha \beta \gamma \delta ) } = \int _ { \mathbb { S } ^ { n - 1 } } \overline { x } ^ { \mu } \overline { x } ^ { \nu } \overline { x } ^ { \alpha } \overline { x } ^ { \beta } \overline { x } ^ { \gamma } \overline { x } ^ { \delta } d \mathbb { S } = C _ { 6 } ( \overline { \mu \nu \alpha \beta \gamma \delta } ) +$$

$$J _ { \mathbb { S } ^ { n - 1 } } \\ + C _ { 2 4 } \left [ \, ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + \dots \\ ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) \right ] \\ \\ + C _ { 2 2 2 } \left [ \, ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + \dots \\ ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) + ( \mu \nu \alpha \beta \gamma \delta ) \right ] \\ \\ \text {Each of these contractions are only nonzero when the connected indices are equal, and at the
$$

Each of these contractions are only nonzero when the connected indices are equal, and at the same time different from the indices of the other connected groups, for instance:

$$\sum _ { \alpha , \beta } \sum _ { \gamma , \delta } ^ { n } \kappa _ { \alpha \beta } ^ { i } \kappa _ { \gamma \beta } ^ { i } ( \mu \nu \alpha \beta \gamma \delta ) = \delta _ { \mu \nu } \sum _ { \alpha \neq \mu } \sum _ { \gamma \neq \mu } \sum _ { \gamma \neq \alpha } ^ { n } \kappa _ { \alpha \alpha } ^ { i } \kappa _ { \gamma \gamma } ^ { i } .$$

Matching all the indices in this way for each of the terms just found, and taking into account the relation of C 6 , C 24 and C 222 to C 2 in the appendix, we take out a common factor C 2 4 p n ` 2 q , and abbreviate the sum notation to produce all the terms of order O p ε n ` 4 q :


<!-- p:21 -->


$$\ a b r { v i t a n t o r } & \, t o \, \prod u c a n t a l l t e r s \, o f \, \text {EMBBD} \, \Pi _ { \mu } \Pi _ { \nu } \Pi _ { \mu } \Pi _ { \nu } \Pi _ { \mu } \\ & \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \, \quad \$$

$$\ a b r { \text {validate the sum notation to produce an the terms of order } ( \varepsilon ^ { n } ) ^ { n } } \colon \\ [ C ( D _ { p } ( \varepsilon ) ) ] ^ { \mu \nu } = \frac { \delta _ { \mu \nu } V _ { n } ( \varepsilon ) \varepsilon ^ { 2 } } { n + 2 } + \frac { C _ { 2 } \varepsilon ^ { n + 4 } } { 8 ( n + 2 ) ( n + 4 ) } \sum _ { i } \left [ 4 \delta _ { \mu \nu } \sum _ { \alpha , \beta } ( \kappa _ { \alpha \beta } ^ { i } ) ^ { 2 } + 8 \delta _ { \mu \nu } \sum _ { \alpha } \kappa _ { \alpha \mu } ^ { i } \kappa _ { \alpha \nu } + 1 2 \delta _ { \mu \nu } \sum _ { \alpha } ( \kappa _ { \alpha \nu } ^ { i } ) ^ { 2 } } \\$$

Many of the resulting summations are the same after relabeling and using κ i αβ ' κ i βα , so they can be gathered into common factors:

$$\text {Many of the resulting summations are the same after relabeling and using $\kappa_{\alpha}\equiv \kappa_{\beta}$, so they} \\ \text {can be gathered into common factors:} \\ \\ [ C ( D _ { p } ( \varepsilon ) ) ] ^ { \mu \nu } & = \delta _ { \mu \nu } \frac { V _ { ( \varepsilon ) \varepsilon } } { n + 2 } + \frac { V _ { ( \varepsilon ) \varepsilon } } { 8 ( n + 2 ) ( n + 4 ) } \sum \left [ 4 \delta _ { \mu \nu } \sum ( \kappa _ { \alpha \beta } ^ { i } ) ^ { 2 } + 8 \sum _ { \alpha } \kappa _ { \alpha \mu } ^ { i } \kappa _ { \alpha \nu } - 1 5 \delta _ { \mu \nu } ( \kappa _ { \nu \nu } ^ { i } ) ^ { 2 } \\ & - 3 \delta _ { \mu \nu } \sum ( \kappa _ { \alpha \rho } ^ { i } ) ^ { 2 } - 1 2 ( 1 - \delta _ { \mu \nu } ) ^ { i } \kappa _ { \mu \nu } ^ { i } + \kappa _ { \mu \nu } ^ { i } - 6 \delta _ { \mu \nu } \sum \kappa _ { \alpha \rho } ^ { i } \kappa _ { \nu - 1 } ^ { i } - 1 2 \delta _ { \mu \nu } \sum ( \kappa _ { \alpha \nu } ^ { i } ) ^ { 2 } \\ & - \delta _ { \mu \nu } \sum _ { \alpha \neq \mu \neq \alpha , \mu } \kappa _ { \alpha \kappa } ^ { i } \kappa _ { \gamma \gamma } - 2 \delta _ { \mu \nu } \sum _ { \alpha \neq \mu \neq \alpha , \mu } ( \kappa _ { \alpha \beta } ^ { i } ) ^ { 2 } - ( 1 - \delta _ { \mu \nu } ) \left ( 4 \kappa _ { \mu \nu } ^ { i } \sum _ { \alpha \neq \mu , \nu } \kappa _ { \alpha \alpha } ^ { i } + 8 \sum _ { \alpha \neq \mu , \nu } \kappa _ { \alpha \mu } ^ { i } \kappa _ { \nu \alpha } \right ) \right ] \\ \text {for which regrouping terms and completing some sums will clarify the simplifications below,} \\ & \quad V ( c ) ^ { 2 } \sum ( c ) ^ { 2 } - \left [ \gamma ( c ) ^ { 4 } - \left [ \gamma - \left [ \alpha - \alpha ^ { 2 } \right ] - \left [ \gamma - \left [ \alpha - \alpha ^ { 2 } \right ] \right ] - \left [ \gamma - \left [ \alpha - \alpha ^ { 2 } \right ] \right ] - \left [ \gamma - \left [ \alpha - \alpha ^ { 2 } \right ] \right ] \right ] \right ] \\$$

for which regrouping terms and completing some sums will clarify the simplifications below,

$$& \quad \text {for which regrouping terms and completing some sums will clearly the simplifications below,} \\ & \quad = \delta _ { \mu \nu } \frac { V _ { ( \varepsilon ) } \varepsilon ^ { 2 } } { n + 2 } + \frac { V _ { ( n ) } \varepsilon ^ { 4 } } { 8 ( n + 2 ) ( n + 4 ) } \sum _ { i } \left [ 8 \sum _ { \alpha } \kappa _ { \alpha \mu \alpha \nu } ^ { i } - 1 2 \kappa _ { \mu \nu } ^ { i } ( \kappa _ { \mu \mu } ^ { i } + \kappa _ { \nu \nu } ^ { i } ) - 4 \kappa _ { \mu \nu } ^ { i } \sum _ { \alpha \neq \mu } \kappa _ { \alpha \alpha } ^ { i } \\ & \quad - 8 \sum _ { \alpha \neq \mu , \nu } \kappa _ { \alpha \mu \nu } ^ { i } \kappa _ { \nu \alpha } ^ { i } + \delta _ { \mu \nu } \left \{ 4 \sum _ { \alpha , \beta } ( \kappa _ { \alpha \alpha } ^ { i } ) ^ { 2 } - 3 \sum _ { \alpha \neq \mu } ( \kappa _ { \alpha \alpha } ^ { i } ) ^ { 2 } + 2 1 ( \kappa _ { \mu \mu } ^ { i } ) ^ { 2 } - 2 \kappa _ { \mu \mu } ^ { i } \sum _ { \alpha \neq \mu } \kappa _ { \alpha \alpha } ^ { i } - 1 2 \sum ( \kappa _ { \alpha \mu } ^ { i } ) ^ { 2 } \\ & \quad - \sum _ { \alpha \neq \mu \gamma \neq \alpha , \mu } \kappa _ { \alpha \alpha } ^ { i } \kappa _ { \gamma \gamma } ^ { i } - 2 \sum _ { \alpha \neq \mu \neq \alpha , \mu } ( \kappa _ { \alpha \beta } ^ { i } ) ^ { 2 } + 8 \sum _ { \alpha \neq \mu } ( \kappa _ { \alpha \mu } ^ { i } ) ^ { 2 } \left \} \right ] + \mathcal { O } ( \varepsilon ^ { n + 5 } ) . \\ & \quad \text {Some terms inside the curly braces complement the missing elements of other summations:} \\ & \quad 2 1 ( \kappa _ { \mu \mu } ^ { i } ) ^ { 2 } - 2 \kappa _ { \mu \mu } \sum _ { \kappa _ { \alpha \alpha } ^ { i } } \kappa _ { \alpha \alpha } ^ { i } - 1 2 \sum ( \kappa _ { \alpha \mu } ^ { i } ) ^ { 2 } + 8 \sum _ { \alpha \neq \mu } ( \kappa _ { \alpha \mu } ^ { i } ) ^ { 2 } = 1 5 ( \kappa _ { \mu \mu } ^ { i } ) ^ { 2 } - 2 \kappa _ { \mu \mu } ^ { i } \sum _ { \kappa _ { \alpha \alpha } ^ { i } } \kappa _ { \alpha \mu } ^ { i } - 4 \sum ( \kappa _ { \alpha \mu } ^ { i } ) ^ { 2 } ,$$

$$2 1 ( \kappa _ { \mu \mu } ^ { i } ) ^ { 2 } - 2 \kappa _ { \mu \mu } ^ { i } \sum _ { \alpha \neq \mu } \kappa _ { \alpha \alpha } ^ { i } - 1 2 \sum _ { \alpha } ( \kappa _ { \alpha \mu } ^ { i } ) ^ { 2 } + 8 \sum _ { \alpha \neq \mu } ( \kappa _ { \alpha \mu } ^ { i } ) ^ { 2 } = 1 5 ( \kappa _ { \mu \mu } ^ { i } ) ^ { 2 } - 2 \kappa _ { \mu \mu } ^ { i } \sum _ { \alpha } \kappa _ { \alpha \alpha } ^ { i } - 4 \sum _ { \alpha } ( \kappa _ { \alpha \mu } ^ { i } ) ^ { 2 } ,$$


<!-- p:22 -->


and

Now, notice that this last type of double sum decomposes as follows

$$& \text {and} \\ & \quad - 3 \sum _ { \alpha \neq \mu } ( \kappa _ { \alpha \alpha } ^ { i } ) ^ { 2 } - \sum _ { \alpha \neq \mu } \sum _ { \gamma \neq \alpha , \mu } \kappa _ { \alpha \alpha } ^ { i } \kappa _ { \gamma \gamma } ^ { i } - 2 \sum _ { \alpha \neq \mu } \sum _ { \beta \neq \alpha , \mu } ( \kappa _ { \alpha \beta } ^ { i } ) ^ { 2 } = - \sum _ { \alpha , \gamma \neq \mu } \kappa _ { \alpha \alpha } ^ { i } \kappa _ { \gamma \gamma } ^ { i } - 2 \sum _ { \alpha , \beta \neq \mu } ( \kappa _ { \alpha \beta } ^ { i } ) ^ { 2 } . \\ & \quad \text {Now notice that this last type of double sum decomposes as follows}$$

$$\text {notice that this last type of double sum decomposes as follows} \\ & - \sum _ { \alpha , \gamma \neq \mu } [ \cdot ] _ { \alpha \gamma } = - \sum _ { \alpha , \gamma } [ \cdot ] _ { \alpha \gamma } + \sum _ { \substack { \gamma = \mu \\ \gamma = \mu } } [ \cdot ] _ { \alpha \gamma } + \sum _ { \substack { \alpha = \mu \\ \gamma = \mu } } [ \cdot ] _ { \alpha \gamma } - [ \cdot ] _ { \mu \mu } , \\$$

therefore, the right hand side of the previous two equations complement each other:

$$- 8 \sum _ { \alpha \neq \mu , \nu } \kappa _ { \alpha \mu } ^ { i } \kappa _ { \nu \alpha } ^ { i } + \delta _ { \mu \nu } \left \{ 4 \sum _ { \alpha , \beta } ( \kappa _ { \alpha \beta } ^ { i } ) ^ { 2 } + 1 2 ( \kappa _ { \mu \mu } ^ { i } ) ^ { 2 } - \sum _ { \alpha , \gamma } \kappa _ { \alpha \alpha } ^ { i } \kappa _ { \gamma \gamma } ^ { i } - 2 \sum _ { \alpha , \beta } ( \kappa _ { \alpha \beta } ^ { i } ) ^ { 2 } \right \} \right ] + \mathcal { O } ( \varepsilon ^ { n + 5 } ) . \\ \intertext { To simplify further, use 12 ( \kappa _ { \mu \mu } ^ { i } ) ^ { 2 } \, to \, complete the \text {remaining sums and cancel terms} \colon }$$

$$\text {therefor, the right hand side of the previous two equations complement each other:} \\ [ C ( D _ { p } ( \varepsilon ) ) ] ^ { \mu \nu } = \frac { \delta _ { \mu \nu } V _ { n } ( \varepsilon ) \varepsilon ^ { 2 } } { n + 2 } + \frac { V _ { n } ( \varepsilon ) \varepsilon ^ { 4 } } { 8 ( n + 2 ) ( n + 4 ) } \sum _ { i } \left [ 8 \sum _ { \alpha } \kappa _ { \alpha } ^ { i } \kappa _ { \alpha \nu } ^ { i } - 1 2 \kappa _ { \mu \nu } ^ { i } ( \kappa _ { \mu \mu } ^ { i } + \kappa _ { \nu \nu } ) - 4 \kappa _ { \mu \nu } ^ { i } \sum _ { \alpha \neq \mu , \nu } \kappa _ { \alpha } ^ { i } \\ - 8 \sum _ { \alpha \neq \mu , \nu } \kappa _ { \alpha \mu } \kappa _ { \alpha } ^ { i } + \delta _ { \mu \nu } \left \{ 4 \sum _ { \alpha , \beta } ( \kappa _ { \alpha \beta } ^ { i } ) ^ { 2 } + 1 2 ( \kappa _ { \mu \mu } ^ { i } ) ^ { 2 } - \sum _ { \alpha , \gamma } \kappa _ { \alpha \gamma } \kappa _ { \gamma } ^ { i } - 2 \sum _ { \alpha , \beta } ( \kappa _ { \alpha \beta } ^ { i } ) ^ { 2 } \right \} \right ] + \mathcal { O } ( \varepsilon ^ { n + 5 } ) .$$

To simplify further, use 12 p κ i μμ q 2 to complete the remaining sums and cancel terms:

and

$$8 \sum _ { \alpha } \kappa _ { \alpha \mu } ^ { i } \kappa _ { \nu \alpha } ^ { i } - 8 \kappa _ { \mu \nu } ^ { i } ( \kappa _ { \mu \mu } ^ { i } + \kappa _ { \nu \nu } ^ { i } ) - 8 \sum _ { \alpha \neq \mu , \nu } \kappa _ { \alpha \mu } ^ { i } \kappa _ { \nu \alpha } ^ { i } + 8 ( \kappa _ { \mu \mu } ^ { i } ) ^ { 2 } \delta _ { \mu \nu } = 0 ,$$

$$- 4 \kappa _ { \mu \nu } ^ { i } ( \kappa _ { \mu \mu } ^ { i } + \kappa _ { \nu \nu } ^ { i } ) - 4 \kappa _ { \mu \nu } ^ { i } \sum _ { \alpha \neq \mu , \nu } \kappa _ { \alpha \alpha } ^ { i } + 4 ( \kappa _ { \mu \mu } ^ { i } ) ^ { 2 } \delta _ { \mu \nu } = - 4 \kappa _ { \mu \nu } ^ { i } \sum _ { \alpha } \kappa _ { \alpha \alpha } ^ { i } . \\ \text {ally, all these computations lead us to the simple expression:}$$

$$F \text { finally, all these computations lead us to the simple expression} \\ [ C ( D _ { p } ( \varepsilon ) ) ] ^ { \mu \nu } = \frac { \delta _ { \mu \nu } V _ { n } ( \varepsilon ) \varepsilon ^ { 2 } } { n + 2 } + \frac { V _ { n } ( \varepsilon ) \varepsilon ^ { 4 } } { 8 ( n + 2 ) ( n + 4 ) } \sum _ { i } \left [ \delta _ { \mu \nu } \left \{ 2 \sum _ { \alpha , \beta } ( \kappa _ { \alpha \beta } ^ { i } ) ^ { 2 } - ( H ^ { i } ) ^ { 2 } \right \} - 4 \kappa _ { \mu \nu } ^ { i } H ^ { i } \right ] + \mathcal { O } ( \varepsilon ^ { n + 5 } ) \\ \text {where} \\ \sum _ { \kappa _ { \mu \nu } H ^ { i } } K _ { \mu \nu } H ^ { i } \leq \langle \mathbb { I } ( e _ { \mu } , e _ { \nu } ) , H \rangle = \langle \widehat { S } _ { H } e _ { \mu } , e _ { \nu } \rangle ,$$

Finally, all these computations lead us to the simple expression:

and

$$\sum _ { i } \kappa _ { \mu \nu } ^ { i } H ^ { i } & = \langle \text {II} ( e _ { \mu } , e _ { \nu } ) , \, H \rangle = \langle \, \hat { S } _ { H } \, e _ { \mu } , \, e _ { \nu } \, \rangle , \\ \\ \sum _ { i } \varsigma _ { \sigma } \sum _ { \substack { ( i , j ) ? 2 \\ ( i , j ) = 0 } } \langle \, \text {II} ( e _ { \mu } , e _ { \nu } ) , \, H \rangle & = \langle \, \hat { S } _ { H } \, e _ { \mu } , \, e _ { \nu } \, \rangle ,$$

identify the covariance tangent block to be the matrix of the Weingarten operator at the mean curvature, plus a constant, in the orthonormal basis chosen. □

$$\sum _ { i } ( 2 \sum _ { \alpha , \beta } ( \kappa _ { \alpha \beta } ^ { i } ) ^ { 2 } - ( H ^ { i } ) ^ { 2 } ) = 2 \, t r \, \Pi I - \| H \| ^ { 2 } , \\ \text {since tangent block to be the matrix of the Weigarten open}$$

## 6. Curvature Descriptors

Curvature descriptors in terms of the covariance eigenvalues were introduced in [29] for surfaces and in [3] for hypersurfaces. Alimit formula for the ratio of the eigenvalues was found for curves [2] to establish a direct relationship between the local covariance analysis of a domain containing the point p and the Frenet-Serret curvature information at p , which in the case of curves completely determines the curve locally up to rigid motion [18, Th. 2.13]. The two main theorems of the present work generalize this type of result to general submanifolds by directly taking the limits of the covariance matrix eigenvalues.


<!-- p:23 -->


Corollary 6.1. Writing λ μ p p, ε q for the tangent eigenvalues of the cylindrical covariance matrix C p Cyl p p ε qq , they satisfy the asymptotic ratio

$$\lim _ { \varepsilon \to 0 } V _ { n } ( \varepsilon ) \frac { \lambda _ { \mu } ( p , \varepsilon ) - \lambda _ { \nu } ( p , \varepsilon ) } { \lambda _ { \mu } ( p , \varepsilon ) \lambda _ { \nu } ( p , \varepsilon ) } = \frac { n + 2 } { n + 4 } \left ( \, \lambda _ { \mu } [ t r _ { \perp } \Pi I ] - \lambda _ { \nu } [ t r _ { \perp } \Pi I ] \, \right ) ,$$

and the normal eigenvalues satisfy

$$\lim _ { \varepsilon \to 0 } \frac { V _ { n } ( \varepsilon ) } { \lambda _ { \mu } ( p , \varepsilon ) \lambda _ { \nu } ( p , \varepsilon ) } \sum _ { j = n + 1 } ^ { n + k } \lambda _ { j } ( p , \varepsilon ) & = \frac { n + 2 } { 4 ( n + 4 ) } \left ( \| H \| ^ { 2 } + 2 \text {tr} \Pi \Pi \right ) , \\ \\$$

for any μ, ν ' 1 , . . . , n . Let r λ μ p p, ε q denote the eigenvalues in the case of the spherical domain covariance matrix, C p p D p p ε qq , then the corresponding limits are

and

$$& \lim _ { \varepsilon \to 0 } V _ { n } ( \varepsilon ) \frac { \widetilde { \lambda } _ { \mu } ( p , \varepsilon ) - \widetilde { \lambda } _ { \nu } ( p , \varepsilon ) } { \widetilde { \lambda } _ { \mu } ( p , \varepsilon ) \widetilde { \lambda } _ { \nu } ( p , \varepsilon ) } = \frac { n + 2 } { 2 ( n + 4 ) } \left ( \widetilde { \lambda } _ { \nu } [ \hat { S } _ { H } ] - \widetilde { \lambda } _ { \mu } [ \hat { S } _ { H } ] \right ) , \\ d & \intertext { d } V _ { n } ( \varepsilon ) & \sum _ { \substack { n + k \\ \widetilde { \lambda } _ { n } ^ { + } } } V _ { n } ( \varepsilon ) \sum _ { \substack { n + k \\ \widetilde { \lambda } _ { n } ^ { + } } } \widetilde { \sum } _ { \widetilde { \lambda } _ { n } ^ { + } } ( p , \varepsilon ) - \sum _ { \widetilde { \lambda } _ { n } ^ { + } } \left ( \widetilde { S } _ { \nu } [ \hat { S } _ { H } ] - \widetilde { \lambda } _ { \mu } [ \hat { S } _ { H } ] \right ) ,$$

Now we focus on smooth hypersurfaces in R n ` 1 . Theorems 4.5 and 5.5 provide formulas to extract curvature estimators at scale from the eigenvalues of the covariance matrices. Doing this analysis on a hypersurface furnishes descriptors at scale of the principal curvatures, and the principal and normal directions. As explained in [3], for an embedded Riemannian manifold M Ă R n ` k , of general codimension k , it can always be projected down locally to k hypersurfaces by choosing k linearly independent orthogonal directions n j of its normal space, and project the points to the linear subspace T p M 'x n j y . Approximations of the principal curvatures and directions of these hypersurfaces are sufficient to build an estimator of the second fundamental form of the original manifold and, by Gauß equation 3.2, get in turn a descriptor of its Riemann curvature tensor.

$$& \text {and} & & V _ { n } ( \varepsilon ) & \sum _ { \varepsilon \to 0 } \frac { v _ { n } ( \varepsilon ) } { \lambda _ { \mu } ( p , \varepsilon ) \lambda _ { \nu } ( p , \varepsilon ) } \sum _ { j = n + 1 } ^ { n + k } \tilde { \lambda } _ { j } ( p , \varepsilon ) = \frac { n + 2 } { 2 ( n + 4 ) } \left ( \text {tr} \mathbb { I } \mathbb { I } - \frac { 1 } { n + 2 } \right ) H \| ^ { 2 } \right ) . \\ & \text {Now we focus on smooth hypersurfaces in } \mathbb { R } ^ { n + 1 } . \text { Theorems } 4 . 5 \text { and } 5 . 5 \text { provide formulas to } \\ & \text {extract curvature estimators at scale from the eigenvalues of the covariance matrices.  Doing}$$

Example 6.2. For a smooth hypersurface S , there is only one unit normal vector n at every point p P S , up to orientation. Choosing t e μ u n μ ' 1 as the orthonormal basis of the tangent space given by the principal directions at p , the components of the third fundamental form are:

The tangent trace components are

$$\langle \Pi ( e _ { \mu } , e _ { \nu } ) n , n \rangle = \langle \hat { S } e _ { \mu } , \hat { S } e _ { \nu } \rangle = \langle \hat { S } ^ { 2 } e _ { \mu } , e _ { \nu } \rangle = \kappa _ { \mu } ^ { 2 } \delta _ { \mu \nu } = \text {tr} \, \Pi ( e _ { \mu } , e _ { \nu } ) . \\ \intertext { t h e t a n g t r a c h o n e s a r }$$

$$\langle \, \text {tr} \, \| \Pi \, n , \, n \, \rangle = \text {tr} \, ( \widehat { S } ^ { 2 } ) = \sum _ { \mu = 1 } ^ { n } \kappa _ { \mu } ^ { 2 } = H ^ { 2 } - \mathcal { R } , \\ \intertext { s t h e t a l t r a c , t r \, I I I = \sum _ { \mu = 1 } ^ { n } \kappa _ { \mu } ^ { 2 } = H ^ { 2 } - \mathcal { R } . }$$

that coincides with the total trace, tr III ' ř n μ ' 1 κ 2 μ ' H 2  ́ R . The limit eigenvectors of either C p Cyl p p ε qq or C p D p p ε qq yield a local adapted orthonormal frame x e 1 , . . . , e n y ' x n y of R n ` 1 that precisely singles out the tangent and normal spaces at every generic point. If the principal curvatures at p are of different absolute value, this basis exactly points in the principal and normal directions. The tangent eigenvalues of the cylindrical covariance matrix C p Cyl p p ε qq satisfy


<!-- p:24 -->


$$\lim _ { \varepsilon \to 0 } V _ { n } ( \varepsilon ) \frac { \lambda _ { \mu } ( p , \varepsilon ) - \lambda _ { \nu } ( p , \varepsilon ) } { \lambda _ { \mu } ( p , \varepsilon ) \lambda _ { \nu } ( p , \varepsilon ) } = \frac { n + 2 } { n + 4 } ( \kappa _ { \mu } ^ { 2 } ( p ) - \kappa _ { \nu } ^ { 2 } ( p ) \, ) , \\ \intertext { n o r m o l $ i g o n v u l o $ h a s }$$

and the normal eigenvalue has

$$\lim _ { \varepsilon \to 0 } V _ { n } ( \varepsilon ) \frac { \lambda _ { n + 1 } ( p , \varepsilon ) } { \lambda _ { \mu } ( p , \varepsilon ) \lambda _ { \nu } ( p , \varepsilon ) } = \frac { n + 2 } { 4 ( n + 4 ) } \left ( \, 3 H ^ { 2 } ( p ) - 2 \mathcal { R } ( p ) \, \right ) , \\ y \, \mu , \nu = 1 , \dots , n . \, \text { For the spherical covariance matrix } C ( D _ { p } ( \varepsilon ) ) , \, \text { the limits are }$$

for any μ, ν ' 1 , . . . , n . For the spherical covariance matrix C p D p p ε qq , the limits are

and

$$\lim _ { \varepsilon \to 0 } V _ { n } ( \varepsilon ) \frac { \tilde { \lambda } _ { \mu } ( p , \varepsilon ) - \tilde { \lambda } _ { \nu } ( p , \varepsilon ) } { \tilde { \lambda } _ { \mu } ( p , \varepsilon ) \tilde { \lambda } _ { \nu } ( p , \varepsilon ) } & = \frac { n + 2 } { 2 ( n + 4 ) } [ \kappa _ { \nu } ( p ) - \kappa _ { \mu } ( p ) ] H ( p ) , \\ \intertext { l i m V ( \varepsilon ) } \lim _ { \varepsilon \to 0 } V _ { n } ( \varepsilon ) \frac { \tilde { \lambda } _ { n + 1 } ( p , \varepsilon ) } { \tilde { \lambda } _ { \mu } ( p , \varepsilon ) \tilde { \lambda } _ { \nu } ( p , \varepsilon ) } & = \frac { n + 2 } { 2 } \left [ \frac { n + 1 } { n } H ^ { 2 } ( n ) - \mathcal { R } ( n ) \right ]$$

r r The known terms of the series expansion of the eigenvalue decomposition of the covariance matrices can be inverted to extract the curvature descriptors upon truncations of the series. In the spherical case, one recovers the results and descriptors already obtained in [3].

$$\lim _ { \varepsilon \to 0 } V _ { n } ( \varepsilon ) \frac { \widetilde { \lambda } _ { n + 1 } ( p , \varepsilon ) } { \widetilde { \lambda } _ { \mu } ( p , \varepsilon ) \widetilde { \lambda } _ { \nu } ( p , \varepsilon ) } = \frac { n + 2 } { 2 ( n + 4 ) } \left [ \frac { n + 1 } { n + 2 } H ^ { 2 } ( p ) - \mathcal { R } ( p ) \right ] . \\ \intertext { h e n k o n n e r s o f t h e s i n c o u s i p a n d e c o mposi t i o n o f t h e c o v a r i a n c e }$$

Corollary 6.3. Let us write λ p p, ε q ' λ p D p p ε qq , V p p ε q ' V p D p p ε qq for the integral invariants of a spherical domain on a hypersurface S , then the corresponding curvature descriptors at scale ε ą 0 and point p P S , for any μ ' 1 , . . . , n , are:

$$H ( D _ { p } ^ { + } ( \varepsilon ) ) = ( \pm ) \sqrt { 4 ( n + 2 ) ^ { 2 } ( n + 4 ) \frac { \lambda _ { n + 1 } ( p , \varepsilon ) } { n \varepsilon ^ { 4 } V _ { n } ( \varepsilon ) } } + \frac { 8 ( n + 2 ) ^ { 2 } } { n \varepsilon ^ { 2 } } \left ( 1 - \frac { V _ { p } ( \varepsilon ) } { V _ { n } ( \varepsilon ) } \right ) ,$$

$$\varepsilon & > 0 \ a n d \ p o i n t { p \in \mathcal { S } , \, \int o r \ a n g \ \mu = 1 , \dots , n , \, \ a r d e } { \colon } \\ \mathcal { R } ( D _ { p } ^ { + } ( \varepsilon ) ) & = 2 ( n + 2 ) ^ { 2 } ( n + 4 ) \frac { \lambda _ { n + 1 } ( p , \varepsilon ) } { n \, \varepsilon ^ { 4 } \, V _ { n } ( \varepsilon ) } - \frac { 8 ( n + 1 ) ( n + 2 ) } { n \, \varepsilon ^ { 2 } } \left ( \frac { V _ { p } ( \varepsilon ) } { V _ { n } ( \varepsilon ) } - 1 \right )$$

$$\kappa _ { \mu } ( D _ { p } ^ { + } ( \varepsilon ) ) & = \frac { 2 ( n + 2 ) } { \varepsilon ^ { 2 } H ( D _ { p } ^ { + } ( \varepsilon ) ) } \left [ \frac { V _ { p } ( \varepsilon ) } { V _ { n } ( \varepsilon ) } + \frac { n + 4 } { \varepsilon ^ { 2 } } \left ( \frac { \varepsilon ^ { 2 } } { n + 2 } - \frac { \lambda _ { \mu } ( p , \varepsilon ) } { V _ { n } ( \varepsilon ) } \right ) - 1 \right ] , \\ \intertext { w h e r e } \intertext { s i t h e v e r a l l s i g a n h e c h o s e n b w i f r i n g a n g r a n r o m a l l o r i e n t a t i o n p r e m }$$

where the overall sign can be chosen by fixing a normal orientation from

$$( \pm ) = s g n \langle e _ { n + 1 } ( D _ { p } ( \varepsilon ) ) , \, s ( D _ { p } ( \varepsilon ) ) \rangle .$$

The eigenvectors e μ p D p p ε qq and e n ` 1 p D p p ε qq are descriptors of the principal and normal directions respectively. The errors are:

$$| H ^ { 2 } ( p ) - H ^ { 2 } ( D _ { p } ( \varepsilon ) ) | & \leqslant \mathcal { O } ( \varepsilon ) , \quad | \mathcal { R } ( p ) - \mathcal { R } ( D _ { p } ( \varepsilon ) ) | \leqslant \mathcal { O } ( \varepsilon ) , \quad | \kappa _ { \mu } ^ { 2 } ( p ) - \kappa _ { \mu } ^ { 2 } ( D _ { p } ( \varepsilon ) ) | \leqslant \mathcal { O } ( \varepsilon ) .$$

The cylindrical domain descriptors may determine in general the squares of the principal curvatures with better truncation error than their spherical domain counterparts.

Corollary 6.4. Denote λ p p, ε q ' λ p Cyl p p ε qq , V p p ε q ' V p Cyl p p ε qq the integral invariants of a cylindrical domain on a hypersurface S , then the corresponding curvature descriptors at scale


<!-- p:25 -->


ε ą 0 and point p P S , for any μ ' 1 , . . . , n , are:

$$H ( C y _ { p } 1 _ { \varepsilon } ( \varepsilon ) ) = ( \pm ) \sqrt { \frac { 2 ( n + 2 ) } { \varepsilon ^ { 2 } } \left [ \frac { 2 ( n + 4 ) } { \varepsilon ^ { 2 } } \frac { \lambda _ { n + 1 } ( p , \varepsilon ) } { V _ { n } ( \varepsilon ) } + 2 \left ( 1 - \frac { V _ { p } ( \varepsilon ) } { V _ { n } ( \varepsilon ) } \right ) \right ] } ,$$

$$\varepsilon & > 0 \ a n d \ p o n t \ p \in \mathcal { S } , \text { for } a n y \ \mu = 1 , \dots , n , \ \ a r e \colon \\ & \mathcal { R } ( C y _ { p } 1 _ { \varepsilon } ( \varepsilon ) ) = \frac { 2 ( n + 2 ) } { \varepsilon ^ { 2 } } \left [ \frac { 2 ( n + 4 ) } { \varepsilon ^ { 2 } } \frac { \lambda _ { n + 1 } ( p , \varepsilon ) } { V _ { n } ( \varepsilon ) } + 3 \left ( 1 - \frac { V _ { p } ( \varepsilon ) } { V _ { n } ( \varepsilon ) } \right ) \right ]$$

$$\kappa _ { \mu } ^ { 2 } ( C _ { Y } l _ { p } ( \varepsilon ) ) = \frac { n + 2 } { \varepsilon ^ { 2 } } \left [ \frac { n + 4 } { \varepsilon ^ { 2 } } \left ( \frac { \lambda _ { \mu } ( p , \varepsilon ) } { V _ { n } ( \varepsilon ) } - \frac { \varepsilon ^ { 2 } } { n + 2 } \right ) - \frac { V _ { p } ( \varepsilon ) } { V _ { n } ( \varepsilon ) } + 1 \right ] , \\ \intertext { w h e r e t h e o v e r a l l s i q n \ c a n b e \ c h o s e n \ b y \ f i x i n g a \ n o r m a l \ o r i e n t a t i o n \ f r o m }$$

where the overall sign can be chosen by fixing a normal orientation from

$$( \pm ) & = s g n \langle e _ { n + 1 } ( C y l _ { p } ( \varepsilon ) ) , \, s ( C y l _ { p } ( \varepsilon ) ) \rangle . \\$$

The eigenvectors e μ p Cyl p p ε qq and e n ` 1 p Cyl p p ε qq are descriptors of the principal and normal directions respectively. The truncation errors are:

$$| H ^ { 2 } ( p ) - H ^ { 2 } ( C y _ { p } ( \varepsilon ) ) | \leqslant \mathcal { O } ( \varepsilon ^ { 2 } ) , \, | \mathcal { R } ( p ) - \mathcal { R } ( C y _ { p } ( \varepsilon ) ) | \leqslant \mathcal { O } ( \varepsilon ^ { 2 } ) , \, | \kappa _ { \mu } ^ { 2 } ( p ) - \kappa _ { \mu } ^ { 2 } ( C y _ { p } ( \varepsilon ) ) | \leqslant \mathcal { O } ( \varepsilon ^ { 2 } ) .$$

Proof. Solving for the next-to-leading order term in the volume formula 4.4, and for the normal eigenvalue in equation 4.10, we get a system of two equations H 2  ́ R ' A p ε q , 3 H 2  ́ 2 R ' B p ε q , whose solution is H 2 ' B  ́ 2 A and R ' B  ́ 3 A , where

Finally, solving for κ 2 μ from the tangent eigenvalue equation 4.9, and using A p ε q ' ř α κ 2 α , the last formula obtains. □

$$\text {whose solution is } H ^ { 2 } & = B - 2 A \text { and } \mathcal { K } = B - 3 A , \text { where } \\ A ( \varepsilon ) & = \frac { 2 ( n + 2 ) } { \varepsilon ^ { 2 } } \left ( \frac { V _ { p } ( \varepsilon ) } { V _ { n } ( \varepsilon ) } - 1 \right ) + \mathcal { O } ( \varepsilon ^ { 2 } ) , \quad B ( \varepsilon ) = \frac { 4 ( n + 2 ) ( n + 4 ) } { \varepsilon ^ { 4 } } \frac { \lambda _ { n + 1 } ( p , \varepsilon ) } { V _ { n } ( \varepsilon ) } + \mathcal { O } ( \varepsilon ^ { 2 } ) . \\ \text {Finally, solving for } \kappa ^ { 2 } \text { from the tangent, eigenvalue equation } 4 \, 9 \text { and using } A ( \varepsilon ) = \sum _ { \kappa ^ { 2 } } \kappa ^ { 2 } \text { the }$$

The spherical descriptors can be used to determine the relative signs of the principal curvatures, and the cylindrical descriptors can be used to estimate with higher precision the absolute value of the principal curvatures.

## 7. Conclusions

We have used the exponential map to propose a generalization of the multi-scale integral invariants determined by performing Principal Component Analysis in small regions of n -dimensional submanifolds inside a general p n ` k q -dimensional Riemannian manifold. The kernel domains studied for Riemannian manifolds embedded in Euclidean space were determined by the manifold intersection with higher-dimensional cylinders and balls in the ambient space. The volume of these regions expands with scale as the volume of the n -dimensional ball plus second order corrections proportional to the mean curvature and scalar curvature of the submanifold at the center point. We have also introduced a generalization of the classical third fundamental form to any codimension and showed how it relates to the Weingarten and Ricci operators and the Ricci equation. Then, the covariance analysis of the region point-set was found to have eigenvalues encoding curvature in terms of the third fundamental form; in particular, the first n eigenvalues are related to those of the normal trace of the third fundamental form operator and the corresponding eigenvectors converge to its principal directions, whereas the last k eigenvalues and eigenvectors are related to the tangent trace of this tensor. In the case of the spherical domain the tangent eigenvalues and eigenvectors of the covariance matrix are related to the Weingarten operator at the mean curvature vector. For hypersurfaces, these eigenvalues provide a method to estimate the principal curvatures and principal directions, furnishing descriptors for general submanifolds via the analysis of their independent hypersurface projections. These results show how local integral invariants relate to the same geometric information traditionally characterized by differential-geometric invariants.


<!-- p:26 -->


## Appendix A. Integration of Monomials over Spheres

Let x ' r x 1 , . . . , x n s T P R n , and denote unit the sphere and ball of radius ε in R n by:

$$\mathbb { S } ^ { n - 1 } & = \{ x \in \mathbb { R } ^ { n } \colon \| x \| = 1 \} , \quad B ^ { n } ( \varepsilon ) = \{ x \in \mathbb { R } ^ { n } \colon \| x \| \leqslant \varepsilon \} . \\ \\$$

General spherical coordinates p r, φ 1 , . . . , φ n  ́ 1 q are given by r ' } x } , where x μ : ' x μ { r P S n  ́ 1 .

Definition A.1. For any integers p 1 , . . . , p n P t 0 , 1 , 2 , . . . u , the integrals of the monomials p x 1 q p 1  ̈  ̈  ̈ p x n q p n over the unit sphere and the ball of radius ε are denoted by:

$$( x ^ { n } ) ^ { p _ { 1 } } \dots ( x ^ { n } ) ^ { p _ { n } } \text { over the unit sphere and the ball of radius } \varepsilon \text { are denoted by:} \\ C _ { p _ { 1 } \dots p _ { n } } ^ { ( n ) } = \int _ { \mathbb { S } ^ { n - 1 } } ( x ^ { 1 } ) ^ { p _ { 1 } } \dots ( x ^ { n } ) ^ { p _ { n } } \, d \mathbb { S } ^ { n - 1 } , \quad D _ { p _ { 1 } \dots p _ { n } } ^ { ( n ) } = \int _ { B ^ { n } ( \varepsilon ) } ( x ^ { 1 } ) ^ { p _ { 1 } } \dots ( x ^ { n } ) ^ { p _ { n } } \, d ^ { n } B . \quad ( A . 1 ) \\ \intertext { w h o w } \intertext { o w h e d } \int _ { \mathbb { S } ^ { n - 1 } } ( x ^ { n } ) ^ { p _ { 1 } } \dots ( x ^ { n } ) ^ { p _ { n } } \, d \mathbb { S } ^ { n } - d ^ { 1 } \intertext { o w h e d } \intertext { s u p }$$

where d S n  ́ 1 is the Euclidean measure on the sphere and d n B ' dx 1  ̈  ̈  ̈ dx n ' r n  ́ 1 dr d S n  ́ 1 .

The following formula is crucial to the computations of the present paper, cf. [12].

Theorem A.2. Let b i ' 1 2 p p i ` 1 q , then the values of the integrals A.1 over spheres are

and the integrals over balls become

$$\text {rem. A.2.} & \text { Let } b _ { i } = \frac { 1 } { 2 } ( p _ { i } + 1 ) , \text { then the values of the integrals } A . 1 \text { over spaces are} \\ & C _ { p _ { 1 } \dots p _ { n } } ^ { ( n ) } = \begin{cases} 0 , & \text {if some } p _ { i } \text { is odd,} \\ 2 \frac { \Gamma ( b _ { 1 } ) \Gamma ( b _ { 2 } ) \cdots \Gamma ( b _ { n } ) } { \Gamma ( b _ { 1 } + b _ { 2 } + \cdots + b _ { n } ) } , & \text {if all } p _ { i } \text { are even,} \end{cases} ( A . 2 ) \\ \intertext { i n t e g r a l s } \text { over balls become} & \quad \intertext { D ( n ) } & \sum ^ { n + p _ { 1 } + \cdots + p _ { n } } C ( n ) & \intertext { ( A . 2 ) }$$

$$D _ { p _ { 1 } \dots p _ { n } } ^ { ( n ) } = \frac { \varepsilon ^ { n + p _ { 1 } + \dots + p _ { n } } } { n + p _ { 1 } + \dots + p _ { n } } \ C _ { p _ { 1 } \dots p _ { n } } ^ { ( n ) } . \\ \text {vea shall need the relations among integers of monomials of even powers} .$$

Example A.3. We shall need the relations among integrals of monomials of even powers:

$$D _ { p _ { 1 } \dots p _ { n } } ^ { ( n ) } & = \frac { C _ { p _ { 1 } \dots p _ { n } } ^ { ( n ) } } { n + p _ { 1 } + \cdots + p _ { n } } \, C _ { p _ { 1 } \dots p _ { n } } ^ { ( n ) } . \\ A . 3 . \, \text { We shall need the relations among integrals of monomials of even power} \\ C _ { 2 } & = \int _ { \mathbb { S } ^ { n - 1 } } ( x ^ { 1 } ) ^ { 2 } \, d \mathbb { S } = 2 \frac { \Gamma ( \frac { 3 } { 2 } ) \Gamma ( \frac { 1 } { 2 } ) ^ { n - 1 } } { \Gamma ( \frac { 3 } { 2 } + \frac { n - 1 } { 2 } ) } = \frac { \pi ^ { n / 2 } } { \Gamma ( \frac { n } { 2 } + 1 ) } , \\ C _ { 2 2 } & = \int _ { \mathbb { S } ^ { n - 1 } } ( x ^ { 1 } ) ^ { 2 } ( x ^ { 2 } ) ^ { 2 } \, d \mathbb { S } = \frac { 1 } { n + 2 } \, C _ { 2 } , \\ C _ { 4 } & = \int _ { \mathbb { S } ^ { n - 1 } } ( x ^ { 1 } ) ^ { 4 } \, d \mathbb { S } = \frac { 3 } { n + 2 } \, C _ { 2 } = 3 \, C _ { 2 2 } , \\ C _ { 2 2 2 } & = \int _ { \mathbb { S } ^ { n - 1 } } ( x ^ { 1 } ) ^ { 2 } ( x ^ { 2 } ) ^ { 2 } ( x ^ { 3 } ) ^ { 2 } \, d \mathbb { S } = \frac { 1 } { ( n + 2 ) ( n + 4 ) } \, C _ { 2 } , \\ C _ { 2 4 } & = \int _ { \mathbb { S } ^ { n - 1 } } ( x ^ { 1 } ) ^ { 2 } ( x ^ { 2 } ) ^ { 4 } \, d \mathbb { S } = \frac { 3 } { ( n + 2 ) ( n + 4 ) } \, C _ { 2 } = 3 \, C _ { 2 2 2 } , \\ C _ { 6 } & = \int _ { \mathbb { S } ^ { n - 1 } } ( x ^ { 1 } ) ^ { 6 } \, d \mathbb { S } = \frac { 1 5 } { ( n + 2 ) ( n + 4 ) } \, C _ { 2 } = 1 5 \, C _ { 2 2 2 } .$$


<!-- p:27 -->


The volume of a ball of radius ε , and the area of the unit sphere satisfy:

$$V _ { n } ( \varepsilon ) = V o l ( B ^ { n } ( \varepsilon ) ) = \varepsilon ^ { n } \, C _ { 2 } , \quad S _ { n - 1 } = A r e a ( \mathbb { S } ^ { n - 1 } ) = n \, C _ { 2 } .$$

The integral of a general combination of coordinates depends on the superindices involved, which must not be confused with exponents. For instance

is the general value of the integral of any product of 4 coordinates, that can be all equal to produce C 4 , or be a couple of different pairs to result in C 22 . We introduce the following notation:

$$\text {which must not be confused with exponents. For instance} \\ \int _ { \mathbb { S } ^ { n - 1 } } \overline { x } ^ { \mu } \overline { x } ^ { \nu } \overline { x } ^ { \beta } \overline { x } ^ { \gamma } \, d \mathbb { S } = C _ { 4 } ( \overline { \mu \nu \beta \gamma } ) + C _ { 2 2 } \left [ ( \overline { \mu \nu \beta \gamma } ) + ( \overline { \mu \nu \beta \gamma } ) + ( \overline { \mu \nu \beta \gamma } ) \right ] \\ \text {the general value of the integral of any product of 4 coordinates, that can be all equal to produce}$$

$$( \overset { \prod } { \mu \nu } \beta \gamma ) = \delta _ { \mu \nu } \, \delta _ { \beta \gamma } \delta _ { \mu \beta } , \\$$

so that the symbol is 1 only when the connected superindices are equal and the nonconnected superindices are different, and 0 otherwise, and where ✁ δ μβ : ' p 1  ́ δ μβ q is the negation of the Kronecker delta, i.e., nonzero only if μ ‰ β . An example of order 6 is

$$( \underbrace { \mu \nu \alpha \beta \gamma \delta } } _ { \underbrace { \mu \gamma } } ) = \delta _ { \mu \gamma } \, \delta _ { \nu \delta } \, \delta _ { \alpha \beta } \, \delta _ { \mu \nu } \, \delta _ { \mu \alpha } \, \delta _ { \nu \alpha } .$$

## Acknowledgments

We would like to thank Louis Scharf for very helpful discussions. J.Á.V. would like to thank Miguel Dovale Álvarez for many useful discussions during the writing of this paper.
