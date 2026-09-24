---
id: "Costa-Hero_2004_Geodesic-Entropic-Graphs-Manifold-Dimension"
source_pdf: "../pdf/Costa-Hero_2004_Geodesic-Entropic-Graphs-Manifold-Dimension.pdf"
source_filename: "Costa-Hero_2004_Geodesic-Entropic-Graphs-Manifold-Dimension.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "excellent"
extraction_score: 108.0
visual_assets: "disabled"
references_file: "../references/Costa-Hero_2004_Geodesic-Entropic-Graphs-Manifold-Dimension.references.md"
---

<!-- p:1 -->

## Geodesic Entropic Graphs for Dimension and Entropy Estimation in Manifold Learning

Jose A. Costa , Student Member, IEEE, and Alfred O. Hero , Fellow, IEEE

AbstractIn the manifold learning problem, one seeks to discover a smooth low dimensional surface, i.e., a manifold embedded in a higher dimensional linear vector space, based on a set of measured sample points on the surface. In this paper, we consider the closely related problem of estimating the manifold's intrinsic dimension and the intrinsic entropy of the sample points. Specifically, we view the sample points as realizations of an unknown multivariate density supported on an unknown smooth manifold. Weintroduce a novel geometric approach based on entropic graph methods. Although the theory presented applies to this general class of graphs, we focus on the geodesic-minimal-spanning-tree (GMST) to obtaining asymptotically consistent estimates of the manifold dimension and the Rényi -entropy of the sample density on the manifold. The GMST approach is striking in its simplicity and does not require reconstruction of the manifold or estimation of the multivariate density of the samples. The GMST method simply constructs a minimal spanning tree (MST) sequence using a geodesic edge matrix and uses the overall lengths of the MSTs to simultaneously estimate manifold dimension and entropy. We illustrate the GMST approach on standard synthetic manifolds as well as on real data sets consisting of images of faces.

Index TermsConformal embedding, intrinsic dimension, intrinsic entropy, manifold learning, minimal spanning tree, nonlinear dimensionality reduction.

## I. INTRODUCTION

C ONSIDER a class of natural occurring signals, e.g., recorded speech, audio, images, or videos. Such signals typically have high extrinsic dimension, e.g., as characterized by the number of pixels in an image or the number of time samples in an audio waveform. However, most natural signals have smooth and regular structure, e.g., piecewise smoothness, that permits substantial dimension reduction with little or no loss of content information.To support this fact, one needs only consider the success of image, video, and audio compression algorithms, e.g., MP3, JPEG, and MPEG, or the widespread use of efficient computational geometry methods for rendering smooth three-dimensional (3-D) shapes.

Auseful representation of a regular signal class is to model it as a set of vectors that are constrained to a smooth low-dimensional manifold embedded in a high-dimensional vector space. This manifold may in some cases be a linear, i.e., Euclidean,

Manuscript received July 15, 2003; revised December 23, 2003. This work was supported in part by the National Science Foundation under Grant CCR032557 and by the the National Institutes of Health Cancer Institute under Grant 1PO1 CA87634-01. The associate editor coordinating the review of this manuscript and approving it for publication was Dr. Mario A. T. Figueiredo.

The authors are with the Department of Electrical Engineering and Computer Science, University of Michigan, Ann Arbor, MI 48109-2122 USA (e-mail: jcosta@umich.edu; hero@eecs.umich.edu).

Digital Object Identifier 10.1109/TSP.2004.831130

subspace, but in general, it is a nonlinear curved surface. A problem of substantial recent interest in machine learning, computer vision, signal processing, and statistics is the determination of the so-called intrinsic dimension of the manifold and the reconstruction of the manifold from a set of samples from the signal class [1]-[7]. This problem falls in the area of manifold learning , which is concerned with discovering low-dimensional structure in high-dimensional data.

When the samples are drawn from a large population of signals, one can interpret them as realizations from a multivariate distribution supported on the manifold. As this distribution is singular in the higher dimensional embedding space, it has zero entropy, as defined by the standard Lebesgue integral over the embedding space. However, when defined as a Lebesgue integral restricted to the lower dimensional manifold, the entropy can be finite. This finite intrinsic entropy can be useful for exploring data compression over the manifold or, as suggested in [8], clustering of multiple subpopulations on the manifold. The question that we address in this paper is the following: How do wesimultaneously estimate the intrinsic dimension and intrinsic entropy on the manifold given a set of random sample points? Wepresent a novel geometric probability approach to this question, which is based on entropic graph methods developed by us and reported in [8]-[10].

Techniques for manifold learning can be classified into three categories: linear methods, local methods, and global methods. Linear methods include principal components analysis (PCA) [11] and classical multidimensional scaling (MDS) [12]. They are based on analyzing the eigenstructure of empirical covariance matrices and can be reliably applied only when the manifold is a linear subspace. Local methods include linear local imbedding (LLE) [2], locally linear projections (LLP) [13], Laplacian eigenmaps [14], and Hessian eigenmaps [3]. They are based on local approximation of the geometry of the manifold and are computationally simple to implement. Global approaches include isometric feature mapping (ISOMAP) [1] and coformal ISOMAP (C-ISOMAP) [15]. They preserve the manifold geometry at all scales and have better stability than local methods when the number of manifold samples is limited.

With regard to estimation of the intrinsic dimension , several methods have been proposed [11], [16]. Most of these methods are based on linear projection techniques: A linear map is explicitly constructed, and dimension is estimated by applying principal component analysis (PCA), factor analysis, or MDS to analyze the eigenstructure of the data. These methods rely on the assumption that only a small number of the eigenvalues of the (processed) data covariance will be significant. Linear methods tend to overestimate as they do not account for nonlinearities in the data. Both nonlinear PCA [4] methods and the ISOMAP circumvent this problem, but they still rely on possibly unreliable and costly eigenstructure estimates. Other methods have been proposed based on local geometric techniques, e.g., estimation of local neighborhoods [6] or fractal dimension [17] and estimating packing numbers [5] of the manifold.


<!-- p:2 -->


We propose a geodesic-minimal-spanning-tree (GMST) method that jointly estimates both the intrinsic dimension and intrinsic entropy on the manifold. The method is implemented as follows. First, a complete geodesic graph between all pairs of data samples is constructed, as in ISOMAP or C-ISOMAP. Then, aminimalspanninggraph(theGMST)isobtainedbypruningthe complete geodesic graph down to a subgraph that still connects all points but has minimum total geodesic length. The intrinsic dimension and intrinsic entropy are then estimated from the GMST length functional using a simple linear least squares (LLS) and method-of-moments (MOM) procedure.

The GMST method falls in the category of global approaches to manifold learning, but it differs significantly from the aforementioned methods. First, it has a different scope. Indeed, unlike ISOMAP and C-ISOMAP, the GMST method provides a statistically consistent estimate of the intrinsic entropy in addition to the intrinsic dimension of the manifold. To the best of our knowledge, no other such technique has been proposed for learning manifold dimension. Second, unlike local methods that work on chunks of data in local neighborhoods, GMST works on resampled data distributed over the global data set. Third, the GMST method is simple and elegant: It estimates intrinsic entropy and dimension by detecting the rate of increase of a graph as a function of the number of its resampled vertices.

The aims of this paper are limited to introducing GMST as a novel method for estimating manifold dimension and entropy of the samples. As in work of others on dimension estimation [5], [17], here, we do not consider the issue of reconstruction of the complete manifold. Similarly to these authors, we believe that dimension estimation and entropy estimation for nonlinear data are of interest in their own right. We also do not consider the effect of additive noise or outliers on the performance of GMST. Finally, the consistency results of GMST reported here are limited to domain manifoldsdefinedbysomesmoothunknownmapping.TheextensionofGMSTmethodologytogeneraltargetmanifolds, e.g., those defined by implicit level set embeddings [18], [19], is a worthwhile topic for future investigation.

What follows is a brief outline of the paper. We review some necessary background on the mathematics of domain manifolds in Section II. In Section III, we review the asymptotic theory of entropic graphs and obtain several new results required for their extension to embedded manifolds. In Section IV, we define the general GMST algorithm. Finally, in Section V, we test the GMST algorithm on standard synthetic manifolds and on a real data set consisting of human faces from different subjects.

## II. GEOMETRIC BACKGROUND

### A. Three-Dimensional Example

To illustrate ideas, consider a two-dimensional (2-D) surface embedded in 3-D Euclidean space called the embedding space.

Let be a set of points (samples) in a subset of the plane. Naturally, the shortest path between any pair of these points is given by the straight line in connecting them, with corresponding distance given by its Euclidean length . Now, let be used as a parameterization space to describe a curved surface in via a mapping . Surfaces defined in this explicit manner are called domain or parameterized manifolds, and they inherit the topological dimension, which is equal to 2 in this case, of the parameterization space. When is nonlinear, the shortest path on between points and is a curve on the surface called the geodesic curve. In this paper, we will primarily consider domain manifolds defined by conformal mappings . Such conformal embeddings have the property that the angles between tangent vectors to the surface are identical to angles between corresponding vectors in the parameterization space, possibly up to a smoothly varying local scale factor. This property guarantees that regardless of how the mapping 'deforms' onto , the geodesic distances in are closely related to the Euclidean distances in . When this smooth surface representation holds, there exist algorithms, e.g., ISOMAP and C-ISOMAP [1], [15], which can be used to estimate the Euclidean distances between points in from estimates of the geodesic distances between points in . If a certain type of minimal spanning graph is constructed using these estimates, well-established results in geometrical probability [8], [20] allow us to develop simple estimates of both entropy and dimension of the points distributed on the surface.

### B. Differential Geometry Setting

In the following, we recall some facts from differential geometry needed to formalize and generalize the ideas just described. We will consider smooth manifolds embedded in . For the general theory, we refer the reader to any standard book in differential geometry (for example, [21]-[23]). An -dimensional smooth manifold is a set such that each of its points has a neighborhood that can be parameterized by an open set of through a local change of coordinates. Intuitively, this means that although is a (hyper) surface in , it can be locally identified with .

Let be a mapping between two manifolds , . Let be a curve in . The tangent map assigns each tangent vector to at point and the tangent vector to at point such that if is the initial velocity of in , then is the initial velocity of the curve in . For example, if , where is an open set of , then , where , , is the Jacobian matrix associated with at point .

The length of a smooth curve is defined as . The geodesic distance between points , is the length of the shortest (piecewise) smooth curve between the two points

$$d _ { \mathcal { M } } ( y _ { 0 } , y _ { 1 } ) = \inf _ { \Gamma } \{ \ell ( \Gamma ) \colon \Gamma ( 0 ) = y _ { 0 } , \Gamma ( 1 ) = y _ { 1 } \} .$$

We can now define the following types of embeddings.


<!-- p:3 -->


Definition 1: is called a conformal mapping if is a diffeomorphism (i.e., is differentiable, bijective with differentiable inverse ) and, at each point , preserves the angles between tangent vectors, i.e.,

$$( d \varphi _ { X } v ) ^ { T } \left ( d \varphi _ { X } w \right ) = c ( x ) v ^ { T } w \quad \quad ( 1 ) ^ { \alpha - \text {ent} }$$

for all vectors and that are tangent to at , and is a scaling factor that varies smoothly with . If for all , , then is said to be a (global) isometry. In this case, the length of tangent vectors is also preserved in addition to the angles between them.

If there is an open set [21], then the diffeomorphism is a conformal mapping iff , where is the identity matrix. In this case, the geodesic distance in can be computed as follows. Any smooth curve can be represented as , where is a smooth curve in . Then, the length of the curve is given by

$$\ell ( \Gamma ) & = \int _ { 0 } ^ { 1 } \left | \frac { d } { d t } \varphi ( \gamma ( t ) ) \right | d t = \int _ { 0 } ^ { 1 } | J _ { \varphi } ( \gamma ( t ) ) \dot { \gamma } ( t ) | d t \\ & = \int _ { 0 } ^ { 1 } \sqrt { c ( \gamma ( t ) ) } | \dot { \gamma } ( t ) | d t .$$

As in , the shortest path between any two points is given by the straight line that connects them, and minimizes over all smooth curves with start and end points at and , respectively. Therefore, if is constant, i.e., for all , the geodesic distance between and is

$$d _ { \mathcal { M } } ( \varphi ( x _ { 0 } ) , \varphi ( x _ { 1 } ) ) = \sqrt { c } | x _ { 0 } - x _ { 1 } | . \quad ( 2 ) \sum _ { \substack { ( 2 ) \\ ( 2 ) } } \text {Let}$$

When , i.e., is an isometry, the geodesic distance in and the Euclidean distance in the parameterization space are the same. If , there is a global expansion (contraction) in the distances between points.

It is evident from the above discussion that geodesic distances carry strong information about a nonlinear domain manifold such as . However, their computation requires the knowledge of the analytical form of via and its Jacobian. Our goal is to learn the entropy of nonlinear data on a domain manifold together with its intrinsic dimension, given only the data set of samples in the embedding space , and without knowledge of its embedding function .

## III. ENTROPIC GRAPH ESTIMATORS ON EMBEDDED MANIFOLDS

Let be independent identically distributed (i.i.d.) random vectors in a compact subset of , with multivariate Lebesgue density , which we will also call random vertices. Define the distance matrix as the matrix of edge weights (w.r.t. a specified metric). A spanning graph over is defined as the pair , where , and is a subset of all graph edges connecting pairs of vertices in , with weights given by . When is computed from pairwise Euclidean distances, is called a Euclidean spanning graph.

It has long been known [24] that, when suitably normalized, the sum of the edge weights of certain minimal Euclidean spanning graphs over converges with probability 1 (w.p. 1) to the limit , where the integral is interpreted in the sense of Lebesgue, and . This a.s. limit is the integral factor in what we will call the extrinsic Rényi -entropy of the multivariate Lebesgue density :

$$H _ { \alpha } ^ { \mathbb { R } ^ { d } } ( f ) = \frac { 1 } { 1 - \alpha } \log \int _ { \mathbb { R } ^ { d } } f ^ { \alpha } ( y ) d y .$$

In the limit, when , we obtain the usual Shannon entropy . Graph constructions that converge to the integral in the limit (3) were called continuous quasiadditive (Euclidean) graphs in [20] and entropic (Euclidean) graphs in [8]. See the monographs by Steele [25] and Yukich [20] for an excellent introduction to the theory of such random Euclidean graphs. Relevant details for these results are given in Section III-A.

The -entropy has proved to be an important quantity in signal processing, where its applications range from vector quantization [26], [27] to pattern matching [28] and image registration [8], [29]. The -entropy parameterizes the Chernoff exponent governing the minimum probability of error [30], making it an important quantity in detection and classification problems. Like the Shannon entropy, the -entropy also has an operational characterization in terms of source coding rates. In [31], it was shown that the -entropy of a source determines the achievable block-code rates in the sense that the probability of block decoding error converges to zero at an exponential rate with rate constant .

### A. Beardwood-Halton-Hammersley Theorem in

Let be a set of points in . A minimal Euclidean graph spanning is defined as the graph spanning having minimal overall length

$$L _ { \gamma } ^ { \mathbb { R } ^ { d } } ( \mathcal { Y } _ { n } ) = \min _ { T \in \mathcal { T } } \sum _ { e \in T } | e | ^ { \gamma } .$$

Here, the sum is over all edges (e.g., , ) in the graph , is the Euclidean length of , and is called the edge exponent or power-weighting constant . For example, when is the set of spanning trees over , one obtains the MST. A minimal Euclidean graph is continuous quasiadditive when it satisfies several technical conditions specified in [20] (also see [9]). Continuous quasiadditive Euclidean graphs include the minimal spanning tree (MST), the -nearest neighbors graph ( -NNG), the minimal matching graph (MMG), the traveling salesman problem (TSP), and their power-weighted variants. While all of the results in this paper apply to this larger class of minimal graphs, we specialize to the MST for concreteness.

Aremarkable result in geometric probability was established by Beardwood, Halton, and Hammersley (BHH) [24].

BHH Theorem [20], [25]: Let be an i.i.d. set of random variables taking values in a compact subset of having common probability distribution . Let this distribution have the decomposition , where is the Lebesgue continuous component, and is the singular component. The Lebesgue continuous component has a Lebesgue density (no singular component) denoted , . Let be the length of the MST spanning , and assume that and that . Then, w.p. 1


<!-- p:4 -->


$$\lim _ { n \to \infty } \frac { L _ { \gamma } ^ { \mathbb { R } ^ { d } } ( y _ { n } ) } { n ^ { \alpha } } = \beta _ { d } \int _ { \mathbb { R } ^ { d } } f ^ { \alpha } ( y ) d y \quad ( 5 ) \quad \stackrel { B H H } { \text {the} } B H$$

where , and is a constant not depending on the distribution . Furthermore, the mean length converges to the same limit.

The limit on the right side of (5) in the BHH theorem is zero when the distribution has no Lebesgue continuous component, i.e., when . On the other hand, when has no singular component, i.e., , a consequence of the BHH Theorem is that

$$\hat { H } _ { \alpha } ^ { \mathbb { R } ^ { d } } ( \mathcal { Y } _ { n } ) \stackrel { \text {def} } { = } \frac { d } { \gamma } \left [ \log \frac { L _ { \gamma } ^ { \mathbb { R } ^ { d } } ( \mathcal { Y } _ { n } ) } { n ^ { ( d - \gamma ) / d } } - \log \beta _ { d } \right ] \quad ( 6 ) \quad \text {and} \quad \text {if}$$

is an asymptotically unbiased and strongly consistent estimator of the extrinsic -entropy defined in (3). For a discussion about the role of the constant in the proposed estimators, see Section IV.

### B. Generalization of BHH Theorem to Embedded Manifolds

If the vertices are constrained to lie on a smooth compact -dimensional manifold , the distribution of is singular with respect to Lebesgue measure and, as previously mentioned, the limit (5) in the BHH Theorem is zero. However, as shown below, if is defined by an isometric embedding from the parameterization space , if has a density on , and if the geodesic estimation step of ISOMAP is used to approximate geodesic distances, then the length of an MST constructed from the geodesic edge lengths can be made to converge, after suitable normalization and transformation, to the intrinsic -entropy on , which is defined by

$$H _ { \alpha } ^ { \mathcal { M } } ( f ) = \frac { m } { \gamma } \log \int _ { \mathcal { M } } f ^ { \alpha } ( y ) \mu _ { \mathcal { M } } ( d y ) \quad ( 7 ) \quad \text {the int}$$

where denotes the differential volume element over .

More generally, assume that is embedded in through the diffeomorphism . As lives in , let be the Euclidean minimal graph spanning and having length function according to (4). We have the following extension of the BHH Theorem.

Theorem 1: Let be a smooth compact -dimensional manifold embedded in through the diffeomorphism , . Assume and . Suppose that are i.i.d. random vectors on having common density with respect to Lebesgue measure on . Then, the length functional of the MST

spanning satisfies (8), shown at the bottom of the page, w.p. 1, where . Furthermore, the mean converges to the same limit.

Proof: This theorem is a simple consequence of (5) in the BHH Theorem and properties of integrals over manifolds. By the BHH Theorem, w.p. 1

$$g \text { on the } L _ { \gamma } ^ { \mathbb { R } ^ { m } } ( \mathcal { X } _ { n } ) = n ^ { ( m - \gamma ) / m } \beta _ { m } \int _ { \mathbb { R } ^ { m } } f _ { X } ^ { \alpha } ( x ) d x + o ( n ^ { ( m - \gamma ) / m } ) \ ( 9 )$$

where is the density of . Therefore, the limits claimed in (8) for and are obvious. For , (9) implies

$$\lim _ { n \to \infty } \frac { L _ { \gamma } ^ { R ^ { m } } ( \mathcal { X } _ { n } ) } { n ^ { ( m - \gamma ) / m } } = \beta _ { m } \int _ { \mathbb { R } ^ { m } } f _ { X } ^ { \alpha } ( x ) d x$$

and it remains to be shown that this limit is identical to the limit asserted in (8).

For an integrable function defined on a domain manifold defined by the diffeomorphism , the integral of over satisfies the relation [22]

$$\int _ { \mathcal { M } } F ( y ) \mu _ { \mathcal { M } } ( d y ) = \int _ { \mathbb { R } ^ { m } } F ( \varphi ( x ) ) g ( x ) d x \quad ( 1 1 )$$

where is the Riemannian metric associated with . Specializing to the indicator function of a small volume centered at a point , (11) implies the following relation between volume elements in and : . Furthermore, specializing to , it is clear from (11) that . Therefore

$$\int _ { \mathbb { R } ^ { m } } f _ { X } ^ { \alpha } ( x ) d x & = \int _ { \mathbb { R } ^ { m } } ( f ( \varphi ( x ) ) g ( x ) ) ^ { \alpha } d x \\ & = \int _ { \mathbb { R } ^ { m } } f ^ { \alpha } ( \varphi ( x ) ) g ^ { \alpha - 1 } ( x ) g ( x ) d x \\$$

which, after the change of variable , is equivalent to the integral in the limit (8). ■

### C. Estimating Geodesic Distances

If is an isometric or conformal embedding, then it has been shown that for sufficiently dense sampling over , i.e., for large , the ISOMAP or the C-ISOMAP algorithm summarized in Table I will approximate the matrix of pairwise Euclidean distances between points in the domain space without explicit knowledge of . This estimate is computed from an Euclidean graph connecting all local neighborhoods of data points in . Specifically, in the isometric case, ISOMAP proceeds as follows. Two methods, called the -rule and the -rule [1], are available for constructing . The first method connects each point to all points within some fixed radius , and the other connects

$$\lim _ { n \to \infty } \frac { L _ { \gamma } ^ { R ^ { n } } ( \varphi ^ { - 1 } ( \mathcal { Y } _ { n } ) ) } { n ^ { ( d ^ { \prime } - \gamma ) / d ^ { \prime } } } = \begin{cases} \infty , & d ^ { \prime } < m \\ \beta _ { m } \int _ { \mathcal { M } } \left [ \det \left ( J _ { \varphi } ^ { T } J _ { \varphi } \right ) \right ] ^ { ( \alpha - 1 / 2 ) } f ^ { \alpha } ( y ) \mu _ { M } ( d y ) , & d ^ { \prime } = m \\ 0 , & d ^ { \prime } > m . \end{cases}$$


<!-- p:5 -->


TABLE I

DISTANCE ESTIMATION STEPS OF ISOMAP/C-ISOMAP ALGORITHMS TO RECONSTRUCT EUCLIDEAN DISTANCES BETWEEN 88 ON THE EMBEDDING PARAMETERIZATION SPACE FROM POINTS 89 OVER THE EMBEDDED MANIFOLD

Step 1. Determine a Euclidean neighborhood graph G of the observed data 'n according to the €-rule or the k-rule as defined in ISOMAP [32].

Step 2. For isometric embeddings compute the edge matrix E of the ISOMAP graph [1] and for conformal imbeddings compute the edge matrix ε of the C-ISOMAP graph [15]. The (i, j) entry of this symmetric matrix is the sum of the lengths of the edges in G along the shortest path between the pair of vertices (Yi, Yj) where the edge lengths between neighboring points Y11, Y2 in G are defined as Euclidean distance |Y1-Y2| in the case of ISOMAP or |Y1-Y2|/√M(1)M(2) in the case of C-ISOMAP where M(i) is the mean distance of Yi to its immediate nearest neighbors.

each point to all its -nearest neighbors. The graph defining the connectivity of these local neighborhoods is then used to approximate the geodesic distance between any pair of points as the shortest path through that connects them. Finally, this results in a distance matrix whose entry is the geodesic distance estimate for the th pair of points. The geodesic distance estimation algorithm just described is motivated by the fact that locally, a smooth manifold is well 'approximated' by a linear hyperplane, and so, geodesic distances between neighboring points are close to their Euclidean distances. For faraway points, the geodesic distance is estimated by summing the sequence of such local approximations over the shortest path through the graph .

Thus, if one uses these distances to construct an MST, its length function will approximate , and we can invoke Theorem 1 to characterize its asymptotic convergence properties. As the estimated distances will use information about the geodesic distances between pairs of points , this graph will be called a geodesic MST (GMST).

More specifically, denote by the matrix of estimated pairwise distances between points and in and by the estimated length of the corresponding edge . Define the GMST as the minimal graph over whose length is

$$\hat { L } _ { \gamma } ^ { \mathcal { M } } ( \mathcal { Y } _ { n } ) = \min _ { T \in \mathcal { T } } \sum _ { e \in T } \hat { d } ^ { \gamma } ( e ) . \quad \quad ( 1 2 ) \quad \quad \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \$$

The following is the principal theoretical result of this paper and is a simple consequence of Theorem 1.

Corollary 1: Let be a smooth compact -dimensional manifold embedded in through the diffeomorphism . Let and . Suppose that are i.i.d. random vectors on with common density w.r.t. Lebesgue measure on . If the entries of matrix satisfy

$$\text {points} \quad \max _ { \substack { i \leq i , j \leq n \\ \text {denotes} } } \left | \frac { \hat { d } _ { i j } } { \left | \varphi ^ { - 1 } ( Y _ { i } ) - \varphi ^ { - 1 } ( Y _ { j } ) \right | } - 1 \right | \rightarrow 0 \text { as } n \rightarrow \infty \ \ ( 1 3 )$$

w.p. 1, then the length functional of the GMST satisfies equation (14), shown at the bottom of the page w.p. 1, where and . Furthermore, the mean converges to the same limit.

The sufficient condition (13) of Corollary 1 simply states that the pairwise Euclidean distances between points in should be uniformly well approximated by the entries of matrix . Constructions of that satisfy (13) will be discussed in Section III-C1

Proof of Corollary 1: Write as

$$\hat { L } _ { \gamma } ^ { \mathcal { M } } ( \mathcal { Y } _ { n } ) = \min _ { T \in T } \sum _ { e \in T } \left [ \frac { \hat { d } ( e ) } { | e | } \right ] ^ { \gamma } | e | ^ { \gamma } .$$

The uniform convergence expressed by (13) implies that

$$\hat { L } _ { \gamma } ^ { \mathcal { M } } ( \mathcal { Y } _ { n } ) = ( 1 + o ( 1 ) ) ^ { \gamma } L _ { \gamma } ^ { \mathbb { R } ^ { m } } ( \varphi ^ { - 1 } ( \mathcal { Y } _ { n } ) ) .$$

Applying Theorem 1 and identifying , , and provides the desired result. ■

If , as the parameter is increased from 2 to , the limit (14) in Corollary 1 transitions from infinity to a finite limit and finally to zero over three consecutive steps , , and . As indexes the rate constant of the length functional , this abrupt transition suggests that the intrinsic dimension and the intrinsic entropy might be easily estimated by investigating the growth rate of the GMSTs length functional. This observation is the basis for the estimation algorithm introduced in Section IV.

$$\lim _ { n \to \infty } \frac { \hat { L } _ { \gamma } ^ { \mathcal { M } } ( \mathcal { Y } _ { n } ) } { n ^ { ( d ^ { \prime } - \gamma ) / d ^ { \prime } } } = \begin{cases} \infty , & d ^ { \prime } < m \\ \beta _ { m } \int _ { \mathcal { M } } f ^ { \infty } ( \mathbf y ) g ^ { - ( \gamma / m ) } ( \varphi ^ { - 1 } ( \mathbf y ) ) \mu _ { \mathcal { M } } ( d \mathbf y ) , & d ^ { \prime } = m \\ 0 , & d ^ { \prime } > m \end{cases}$$


<!-- p:6 -->


We now specialize Corollary 1 to the following cases of interest.

1) Isometric Embeddings: In the case that defines an isometric embedding, the geodesic estimation step of ISOMAP is asymptotically able to recover the true Euclidean distances between the points in , and satisfies (13) [32]. Furthermore, . Thus, using ISOMAP to construct , limit (14) holds with the limit replaced by

$$\beta _ { m } \int _ { \mathcal { M } } f ^ { \alpha } ( y ) \mu _ { \mathcal { M } } ( d y ) .$$

Furthermore, converges w.p. 1 to the intrinsic entropy (7).

If defines an isometric embedding with contraction or expansion, the geodesic estimation step of the ISOMAP algorithm is able to recover the true Euclidean distances between points in only up to an unknown scaling constant [cf. (2)]. As , limit (14) holds with the limit replaced by

$$\beta _ { m } c ^ { 1 - \gamma / 2 } \int _ { \mathcal { M } } f ^ { \alpha } ( y ) \mu _ { \mathcal { M } } ( d y ) .$$

Now, the entropy estimator defined above converges w.p. 1 up to an unknown additive constant to the intrinsic entropy (7). We point out that in many signal processing applications (e.g., image registration), a constant bias on the entropy estimate does not pose a problem since an estimate of the relative magnitude of the entropy functional is all that is required.

2) Nonisometric Embeddings Defined by Conformal Mappings: In the case that is a general (nonisometric) conformal mapping, it was stated in [33], without proof, that the C-ISOMAP algorithm is once again able to recover the true Euclidean distances between points in . Furthermore, . Thus, when is the length of the geodesic MST constructed on the distance matrix generated by the C-ISOMAP algorithm, we expect the limit (14) to hold with the limit replaced by

$$\beta _ { m } \int _ { \mathcal { M } } f ^ { \alpha } ( y ) c ^ { - \gamma / 2 } ( \varphi ^ { - 1 } ( y ) ) \mu _ { \mathcal { M } } ( d y ) .$$

In this case, would converge a.s. to the weighted intrinsic entropy

$$\frac { 1 } { 1 - \alpha } \log \int _ { \mathcal { M } } f ^ { \alpha } ( y ) c ^ { - \gamma / 2 } ( \varphi ^ { - 1 } ( y ) ) \mu _ { \mathcal { M } } ( y ) .$$

The weighted -entropy is a 'version' of the standard unweighted -entropy , which is 'tilted' by the space-varying volume element of . This unknown weighting makes it impossible to estimate the intrinsic unweighted -entropy. However, as can be seen from the discussion in Section IV, as the growth rate exponent of the GMST length depends on , we can still perform dimension estimation in this case.

3) Nonconformal Diffeomorphic Embeddings: When defines a general diffeomorphic embedding, an extension of the C-ISOMAPalgorithmthat can probably learn the Euclidean distances between the points in the parametrization space is needed in order to apply Corollary 1. To the best of our knowledge, such an extension of C-ISOMAP does not yet exist.

## IV. GMST ALGORITHM

Now that we have characterized the asymptotic limit (14) of the length functional of the GMST, we here apply this theory to jointly estimate entropy and dimension. The key is to notice that the growth rate of the length functional is strongly dependent on the intrinsic dimension , whereas the constant in the convergent limit is equal to the intrinsic -entropy. We use this strong growth dependence as a motivation for a simple estimator of . Throughout, we assume that the geodesic minimal graph length is determined from a distance matrix that satisfies the assumption of Corollary 1, e.g., obtained using ISOMAP or C-ISOMAP. We also assume that . This guarantees that has a nonzero finite convergent limit for . Next, define . According to (14), has the following approximation:

$$l _ { n } = a \log n + b + \epsilon _ { n }$$

where

$$a & = \frac { ( m - \gamma ) } { m } \\ b & = \log \beta _ { m } + \frac { \gamma } { m } H _ { \alpha } ^ { \mathcal { M } } ( f ) \\$$

, and is an error residual that goes to zero w.p. 1 as .

The additive model (15) could be the basis for many different methods for estimation of and . For example, we could invoke a central limit theorem on the MST length functional [34] to motivate a Gaussian approximate to and apply maximum likelihood principles. However, in this paper, we adopt a simpler nonparametric least squares strategy that is based on resampling from the population of available points in . The proposed algorithm is summarized in Table II. Specifically, let , , and be integers, and let be an integer that satisfies for some fixed . For each value of , randomly draw bootstrap data sets , with replacement, where the data points within each are chosen from the entire data set independently. From these samples, compute the empirical mean of the GMST length functionals . Defining and motivated by (15), we write down the linear model T

$$\bar { l } = A \left [ _ { b } ^ { a } \right ] + \epsilon$$

where

$$A = \begin{bmatrix} \log p _ { 1 } & \dots & \log p _ { Q } \\ & 1 & \dots & 1 \end{bmatrix} ^ { T } .$$

Expressing and explicitly as functions of and via (16), the dimension and entropy quantities could be estimated using a combination of nonlinear least squares (NLLS) and integer programming. Instead, we take a simpler MOM approach in which we use (17) to solve for the linear least squares (LLS) estimates nn   r     n e g using ISOMAP or C-ISOMAP method.


<!-- p:7 -->


TABLE II GMST RESAMPLING ALGORITHM FOR ESTIMATING INTRINSIC DIMENSION 109 AND INTRINSIC ENTROPY 72

```
-------------------------------------
Initialize: Using entire database of signals {}, construct geodesic distance matrix \dM

using ISOMAP or C-ISOMAP method.

Select parameters: M > 0, N > 0, Q > 0 and pi < ... < pq < n


m = 0,  H = 0;

for M' = 1, ..., M

    for p = p1, ...,PQ

        L = 0;

        for N' = 1, ..., N

            Randomly select a subset of p signals \yj from \yj;

            Compute geodesic MST length L, over \yj, and from \D_M;

            L = L + L*pj;

        end for

        Compute sample average geodesic MST length;

        \E[L^(My)] = L/N;

    end for

    Estimate dimension \m$_M' and \a-entropy \H_M' from \{ \E[ \L^{M}(\yj,)]^p=n, \via LLS/NLS;

    \m = \pi + \m_M^^j',   \H = \H + \H^M^j';

    end for

    \hat = \pi / M,   \hat = \H/M

    -------------------------------------

a, b of a, followed by inversion of (16). After making a simple     \E[

```

, of , followed by inversion of (16). After making a simple large approximation, this approach yields the following estimates:

$$\hat { m } = \text {round} \left \{ \frac { \gamma } { ( 1 - \hat { a } ) } \right \} \\ \hat { H } _ { \alpha } ^ { ( \mathcal { M } , g ) } = \frac { \hat { m } } { \gamma } \left ( \hat { b } - \log \beta _ { \dot { m } } \right ) . \\ \text {lyouh, that the low of logrho, numpho, and Theorem}$$

It is easily shown that the law of large numbers and Theorem 1 imply that these estimators are consistent as , . We omit the details.

By running the algorithm times independently over the population , one obtains estimates that can be averaged to obtain final regularized dimension and entropy estimators and . The role of parameter , together with parameter , is to provide a tradeoff between the bias and variance performance of the estimators for finite . The two cases of interest (considered in Section V) are and . In the first case, the smoothing is performed on the GMST length functional values before dimension and entropy are estimated, resulting in low variance but possibly high bias. In the second case, the smoothing is performed directly on the dimension and entropy estimates, resulting in higher variance but less bias.

Fig.1showsagraphicalillustrationofthesmoothingstepofthe algorithm.Theleftpanelshows resampledGMSTlengths, labeled ' ' and ' ,' along with their average, labeled ' ' for GMSTs built on randomly chosen vertices. For , a linear least squares fit to the average GMST trajectory is used to compute the dimension estimate . For , dimension estimates and are computed from subtrajectories and , forming a histogram from which a final estimate can be computed.

Fig. 1. Computing the dimension estimators by averaging over the length functional values, i.e., 40 7759 78 41 61 4049 59 78 41 (dashed line) or by averaging over the dimension estimates, i.e., 40 7759 78 41 61 40 7759 4941 (solid lines).

A word about determination of the sequence of constants is in order. First of all, in the large regime for which the above estimates were derived, is not required for the dimension estimator. is the limit of the normalized length functional of the Euclidean MST for a uniform distribution on the unit cube . Closed-form expressions are not available, but several approximations and bounds can be used in various regimes of [20], [35]. For example, one could use the large approximation of Bertsimas and van Ryzin [36]: . Another strategy, which is adopted in this paper, is to determine by simulation of the Euclidean MST length on the -dimensional cube for uniform random samples.

Before turning to applications, we briefly discuss computational issues. For samples, computing the MST scales as , for which we have implemented Kruskal's algorithm [29]. On the other hand, the geodesic distances needed to


<!-- p:8 -->

(a)

Fig. 2. 83 -shaped surface manifold and corresponding GMST 40 107 61 5541 graph on 400 sample points.

compute the GMST require operations using Dijkstra's algorithm multiple times. Thus, like ISOMAP, the GMST has overall computational complexity.

### V. APPLICATIONS

We illustrate the performance of the GMST algorithm on manifolds of known dimension as well as on a real data set consisting of face images. In all the simulations, we fixed the parameters and . We also used the -rule method, as described in Table I, to estimate geodesic lengths. With regard to intrinsic dimension estimation, we compare our algorithm to ISOMAP. In ISOMAP, similarly to PCA, intrinsic dimension is usually estimated by detecting changes in the residual fitting errors as a function of subspace dimension.

### A. -Shaped Surface

The first manifold considered is the standard 2-D -shaped surface [2] embedded in (see Fig. 2). Fig. 3 shows the evolution of the average GMST length as a function of the number

50

Fig. 3. GMST dimension estimation for 40 7759 78 41 61 4049 59 78 41 . (a) Plot of the average GMST length 22 76 for the 83 -shaped manifold as a function of the number of samples. (b) Log-log plot of (a). (c) Blowup of the last ten points in (b) and its linear least squares fit. The estimated slope is 94 97 61 48 58 52575554 , which implies 94 109 61 50 . ( 107 61 55 , 77 61 49 , 78 61 53 ).

of samples for a random set of i.i.d. points uniformly distributed on the surface.

To compare the dimension estimation performance of the GMST method to ISOMAP, we ran a Monte Carlo simulation. For each of several sample sizes, 30 independent sets of i.i.d. random vectors uniformly distributed on the surface were generated. We then counted the number of times that the intrinsic dimension was correctly estimated. To automatically estimate dimension with ISOMAP, we follow a standard PCA order estimation procedure. Specifically, we graph the residual variance of the MDS fit as a function of the PCA dimension and try to detect the 'elbow' at which residuals cease to decrease 'significantly' as estimated dimension increases [1]. The elbow detector is implemented by a simple minimum angle threshold rule. Table III shows the results of this experiment. As it can


<!-- p:9 -->


TABLE III NUMBER OF CORRECT ISOMAP AND GMST DIMENSION ESTIMATES OVER 30 TRIALS AS A FUNCTION OF THE NUMBER OF SAMPLES FOR THE 83 -SHAPED MANIFOLD 40 107 61 5541

| n                           |   200 |   400 |   600 |
|-----------------------------|-------|-------|-------|
| ISOMAP                      |    23 |    29 |    30 |
| GMST (M = 1, N = 5, Q = 10) |    29 |    30 |    30 |

5

Fig. 4. Histogram of GMST entropy estimates over 30 trials of 600 samples uniformly distributed on the 83 -shaped manifold ( 107 61 55 , 77 61 49 , 78 61 53 , 81 61 4948 ). True entropy ('true') was computed analytically from the area of the 83 curve supporting the uniform distribution of manifold samples.

be observed, the GMST algorithm outperforms ISOMAP in terms of dimension estimation error rates for small sample sizes. Fig. 4 shows the histogram of the entropy estimates for the same experiment.

### B. Hyperplanes

Next, we investigated linear -dimensional hyperplanes in for which PCA methods are designed. We consider hyperplanes of the form . Table IV shows the results of running a Monte Carlo simulation under the same conditions as in Section V-B. When (i.e., least squares applied to the average length functional values), the GMST method showed a tendency to underestimate the correct dimension at smaller sample sizes. However, by taking instead (i.e., averaging of least squares dimension estimates), this negative bias was eliminated, and the GMST performed as well as the ISOMAP, which was observed to correctly predict the dimension for all sample sizes investigated.

Of course, as expected, the number of samples required to achieve the same level of accuracy increases with the manifold dimension. This is the usual curse of dimensionality phenomenon: As the dimension increases, more samples are needed for the asymptotic regime in (14) to settle in and validate the limit in Corollary 1.

TABLE IV NUMBER OF CORRECT GMST DIMENSION ESTIMATES OVER 30 TRIALS AS A FUNCTION OF THE NUMBER OF SAMPLES FOR HYPERPLANES 40 107 61 5341

| Hyper-plane dimension   | Q         | M         | N         | n - 600     | n - 800     | n - 1000    |
|-------------------------|-----------|-----------|-----------|-------------|-------------|-------------|
|                         | 2 10      | 1 5       | 5 1       | 30 30       | 30 30       | 30 30       |
|                         | 10 10     | 1 5 1 5   | 5 1 5 1   | 24 25 24 25 | 24 26 24 26 | 27 27 27 27 |
|                         | 3 15 3 15 | 1 10 1 10 | 10 1 10 1 | 30 30 30 30 | 30 30 30 30 | 30 30 30 30 |
|                         | 15 15     | 1 10 1 10 | 10 1 10 1 | 24 27 24 27 | 25 28 25 28 | 26 28 26 28 |
|                         | 4 20 4 20 | 1 10 1 10 | 10 1 10 1 | 25 29 25 29 | 28 29 28 29 | 29 30 29 30 |

Fig. 5. Samples from ISOMAP face database [1].

### C. ISOMAP Face Database

Weapplied our method to a high-dimensional synthetic image data set. For this purpose, we used the ISOMAP face database [1]. This set consists of 698 images of the same face generated by varying three different parameters: vertical and horizontal pose and lighting direction. Each image has 64 64 pixels with 256 gray levels, normalized between 0 and 1 (Fig. 5). For processing, we embedded each image in the 4096-dimensional Euclidean space using the common lexicographic order. We applied the algorithm 30 times over the data set with the histogram of the dimension estimates displayed in Fig. 6. The estimated intrinsic dimension oscillates between 3 and 4, which, as in [5], deviates from the 'informal' intrinsic dimension of 3 estimated by ISOMAP with thresholding. The estimated entropy was 21.8 bits, with a standard deviation of 0.5. Note that as is close to one for the estimated values of , the estimate of -entropy is expected to be close to the Shannon entropy. This estimate suggests that one could, in theory, compress the ISOMAP face database with little loss, using at most bits/pixel.

### D. Yale Face Database B

Finally, we applied the GMST method to a real data set and, consequently, of unknown manifold structure, intrinsic dimension, and intrinsic entropy. We chose the set of 256 gray-level


<!-- p:10 -->


30

Fig. 6. GMST intrinsic dimension estimate histogram for the ISOMAP face database. (Left) 107 61 54 , 77 61 49 , 78 61 4948 , 81 61 4953 . (Right) 107 61 54 , 77 61 4948 , 78 61 49 , 81 61 4953 .

Fig. 7. Samples from Yale face database B [37].

images of several individuals taken from the Yale Face Database B [37]. This is a publicly available database 1 containing a number of portfolios of face images under 585 different viewing conditions for each subject (see Fig. 7). Each portfolio consists of nine poses and 65 illumination conditions (including ambient lighting) for each subject. The images were taken against a fixed background, which we did not bother to segment out. This is justified since any fixed structures throughout the images would not change the intrinsic dimension or the intrinsic entropy of the dataset. We randomly selected four individuals from this data base and subsampled each person's face images down to a 64 64 pixel image. Similarly to the ISOMAP face data set, we normalized the pixel values between 0 and 1.

Fig. 8. GMST real-valued intrinsic dimension estimates and histogram for face 2 in the Yale face database B ( 107 61 55 , 77 61 49 78 61 4948 , 81 61 5048 ).

Fig. 9. ISOMAP 40 107 61 5541 residual variance for face 2 in the Yale face database B.

Fig. 8 displays the results of running 30 trials of the algorithm using face 2. The first panel shows the real-valued estimates of the intrinsic dimension, i.e., estimates obtained before the rounding operation in (18). Any value that falls in between the dashed lines will then be rounded to the integer at the midpoint. The second panel of Fig. 8 shows the histogram for these rounded estimates over the 30 generated trials. The intrinsic dimension estimate is between 5 and 6. Fig. 9 shows the corresponding residual variance plots used by ISOMAP to estimate intrinsic dimension. From these plots, it is not obvious how to determine the 'elbow' at which the residuals cease to decrease 'significantly' with added dimensions. This illustrates one of the major drawbacks of ISOMAP (and other spectralbased methods like PCA) as an intrinsic dimension estimator, as it relies on a specific eigenstructure that may not exist in real data. The simple minimum angle threshold rule on ISOMAP produced estimates between 3 and 6. Table V summarizes the results of the GMST method for the four faces. The intrinsic entropy estimates expressed in log base 2 were between 24.9 and


<!-- p:11 -->


TABLE V GMST DIMENSION ESTIMATES 94 109 AND ENTROPY ESTIMATES 94 72 FOR FOUR FACES IN THE YALE FACE DATABASE B

|          |   Facel |      |   Face3 |   Face 4 |
|----------|---------|------|---------|----------|
| m        |       6 |    6 |       7 |        7 |
| H (bits) |    24.9 | 26.4 |    25.8 |     28.0 |

28 bits. Similarly to the ISOMAP face database, as is close to one, these values suggest that the portfolio of a person's face image could be accurately compressed using at most bits/pixel.

## VI. CONCLUSION

We have introduced a novel method for intrinsic dimension and entropy estimation based on the growth rate of the geodesic total edge length functional of entropic graphs. The proposed method has two main advantages. First, it is global in the sense that the MST is constructed over the entire set and thus avoids local linearizations. Second, it does not require reconstructing the manifold or estimating the multivariate density of the samples. We validated the new method by testing it on synthetic manifolds of known dimension and on high dimensional real data sets.

One drawback of GMST, or any other dimension estimator based on ISOMAP geodesic fitting to data, is the restriction to isometric embeddings. We are currently working on extending Theorem 1 and Corollary 1 to general (nonisometric) Riemann manifolds, thus avoiding any assumptions about global embeddings and eliminating the effect of the Jacobian on the intrinsic entropy. We are also studying the use of entropic graphs that bypass the complex step of geodesic estimation. In particular, in [38], we consider -nearest neighbor graphs due to their low complexity and local properties. Future work includes the characterization of the statistics in the linear model (15), optimization of the bias/variance tradeoff parameters of the GMST algorithm, and the study of the effect of additive noise on the manifold samples.

### ACKNOWLEDGMENT

The authors acknowledge and thank the creators of Yale Face Database B for making their face image data publicly available. The authors would also like to thank H. Neemuchwala and A. Almal for their help in acquiring and processing these face images.
