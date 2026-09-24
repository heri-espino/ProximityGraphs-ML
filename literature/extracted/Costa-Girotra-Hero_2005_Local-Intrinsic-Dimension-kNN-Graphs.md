---
id: "Costa-Girotra-Hero_2005_Local-Intrinsic-Dimension-kNN-Graphs"
source_pdf: "../pdf/Costa-Girotra-Hero_2005_Local-Intrinsic-Dimension-kNN-Graphs.pdf"
source_filename: "Costa-Girotra-Hero_2005_Local-Intrinsic-Dimension-kNN-Graphs.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "excellent"
extraction_score: 108.0
visual_assets: "disabled"
---

<!-- p:1 -->

## Estimating Local Intrinsic Dimension with k -Nearest Neighbor Graphs

Jose A. Costa, Abhishek Girotra and Alfred O. Hero III Department of Electrical Engineering and Computer Science University of Michigan, Ann Arbor, MI 48109 Emails: { jcosta, agirotra, hero } @umich.edu

Abstract -Many high-dimensional data sets of practical interest exhibit a varying complexity in different parts of the data space. This is the case, for example, of databases of images containing many samples of a few textures of different complexity. Such phenomena can be modeled by assuming that the data lies on a collection of manifolds with different intrinsic dimensionalities. In this extended abstract, we introduce a method to estimate the local dimensionality associated with each point in a data set, without any prior information about the manifolds, their quantity and their sampling distributions. The proposed method uses a global dimensionality estimator based on k - nearest neighbor ( k -NN) graphs, together with an algorithm for computing neighborhoods in the data with similar topological properties.

Index Terms -Manifold learning, Intrinsic dimension, Nearest neighbor graph.

## I. INTRODUCTION

Continuing technological advances in both sensing and media storage capabilities are enabling the development of systems that generate massive amounts of new types of data and information. Today's medical information systems or video surveillance applications, for example, are producing signals that are high-dimensional in their nature and thus appear to be very complex. However, such signals often contain fundamental features that are concentrated on lower dimensional subsets - curves, surfaces or, more generally, lower-dimensional manifolds - thus permitting substantial dimension reduction with little or no loss of content information. In the recent past, this subject has received substantial attention from researchers in machine learning, computer vision and statistics, leading to the introduction of several manifold learning algorithms (see webpage [1] for an extensive list of references).

Playing a central role in the analysis of high-dimensional data is its intrinsic dimensionality , given by the the dimension of the manifold supporting the data. Intuitively, this quantity describes how many 'degrees of freedom' are necessary to describe the data set. When the intrinsic dimension is assumed constant over the data set, several algorithms have been proposed recently to estimate it directly from only a finite sampling of the manifold. These range from fractal dimension [2], estimating packing numbers [3], entropic graphs [4], [5] or maximum likelihood approach [6]. However, in several

This research was partially supported by NSF contract CCR-0325571.

problems of practical interest, data will exhibit varying dimensionality across the observed data set. For example, in the protein docking problem [7], the degrees of freedom associated with the allowed movements of the reacting molecules will change during the reaction time.

In this paper, we introduce a method to estimate the local dimensionality associated with each point in a data set. If the data set is sampled from a union of disjoint manifolds, with possible different intrinsic dimensionalities, then the algorithm estimates, for each sample point, the dimension of the local manifold where it is supported. The proposed method uses a previously introduced global dimensionality estimator [5] based on k -nearest neighbor ( k -NN) graphs, together with an algorithm for computing neighborhoods in the data with similar topological properties.

## II. THE k -NEAREST NEIGHBOR GRAPH AND GLOBAL DIMENSION ESTIMATION

Let Y n = { Y 1 , . . . , Y n } be n independent and identically distributed (i.i.d.) random vectors with values in a compact subset of R d . The ( 1 -)nearest neighbor of Y i in Y n is given by

$$\arg \min _ { Y \in \mathcal { Y } _ { n } \ \{ Y _ { i } \} } | Y - Y _ { i } | \ ,$$

where | Y - Y i | is the usual Euclidean ( L 2 ) distance in R d between vector Y and Y i . For general integer k ≥ 1 , the k -nearest neighbor of a point is defined in a similar way. The k -NN graph puts an edge between each point in Y n and its k -nearest neighbors. Let N k,i = N k,i ( Y n ) be the set of k - nearest neighbors of Y i in Y n . The total edge length of the k -NN graph is defined as:

$$L _ { \gamma , k } ( \mathcal { Y } _ { n } ) = \sum _ { i = 1 } ^ { n } \sum _ { Y \in \mathcal { N } _ { k , i } } | Y - Y _ { i } | ^ { \gamma } \ ,$$

where γ &gt; 0 is a power weighting constant.

For many data sets of interest, the random vectors Y n are constrained to lie on a m -dimensional Riemannian submanifold M of R d ( m &lt; d ). A Riemann manifold has an associated metric g [8], which endows M with both a notion of distance via geodesics and also a measure μ g via the differential volume element. Under this framework, the asymptotic behavior of (1) is given by the following theorem [5]:


<!-- p:2 -->


Theorem 1: Let ( M , g ) be a compact Riemann m - dimensional submanifold of R d . Suppose Y 1 , . . . , Y n are i.i.d. random vectors of M with bounded density f relative to μ g . Assume m ≥ 2 , 1 ≤ γ &lt; m and define α = ( m - γ ) /m . Then, with probability 1 ,

$$\lim _ { n \to \infty } \frac { L _ { \gamma , k } ( \mathcal { Y } _ { n } ) } { \tilde { n } ^ { ( d ^ { \prime } - \gamma ) / d ^ { \prime } } } = & & \sigma ^ { ( 2 ) } \\ \left \{ \begin{array} { c } \infty \\ \beta _ { m , \gamma , k } \int _ { \mathcal { M } } f ^ { \alpha } ( y ) \, \mu _ { g } ( d y ) , & d ^ { \prime } = m \\ 0 , & d ^ { \prime } > m \end{array} , \\ \text {where } \beta _ { m } \sim \tilde { s } \, \alpha \, c o n s t a n t \, i n d e p e n d e n t \, o f \, f \, \ a n d \, ( \mathcal { M } , q ) , \, \ F i g . \, 1 .$$

where β m,γ,k is a constant independent of f and ( M , g ) . Furthermore, the mean length E [ L γ,k ( Y n )] /n α converges to the same limit.

Theorem 1 provides the basis for developing a consistent estimator of the intrinsic dimensionality m of data set Y n . On the one hand, the growth rate of the length functional is strongly dependent on m . In particular, the only way to obtain a nonzero finite limit in (2) is by normalizing the length functional by the right power α of n , i.e., α = ( m - γ ) /m when d ′ = m . On the other hand, that nonzero finite limit is determined by the intrinsic R ́ enyi α -entropy of the multivariate density f on M :

$$H _ { \alpha } ^ { ( \mathcal { M } , g ) } ( f ) = \frac { 1 } { 1 - \alpha } \log \int _ { M } f ^ { \alpha } ( y ) \, \mu _ { g } ( d y ) \ . \quad ( 3 ) \quad \text {Rieman} \quad \\$$

These observations motivate the following estimator for m . Define l n = log L γ,k ( Y n ) . According to (2), l n has the following approximation

$$l _ { n } = a \, \log n + b + \epsilon _ { n } \ , & & ( 4 ) \, \log \, \frac { ( 4 ) } { 3 }$$

where

$$a & = ( m - \gamma ) / m \ , & \text {on the} \\ b & = \log \beta _ { m , \gamma , k } + \gamma / m \ H _ { \alpha } ^ { ( \mathcal { M } , g ) } ( f ) \ , & \text {sample}$$

and ǫ n is an error residual that goes to zero w.p. 1 as n →∞ . Using the additive model (4), a simple nonparametric least squares strategy based on subsampling from the population Y n of points in M can be adopted. Specifically, let p 1 , . . . , p Q , 1 ≤ p 1 &lt; ...,&lt; p Q ≤ n , be Q integers and let N be an integer that satisfies N/n = ρ for some fixed ρ ∈ (0 , 1] . For each value of p ∈ { p 1 , . . . , p Q } randomly draw N bootstrap datasets Y j p , j = 1 , . . . , N , with replacement, where the p data points within each Y j p are chosen from the entire data set Y n independently. From these samples compute the empirical mean of the k -NN length functionals  ̄ L p = N - 1 ∑ N j =1 L γ,k ( Y j p ) . Defining  ̄ l = [log  ̄ L p 1 , . . . , log  ̄ L p 1 ] T , write down the linear vector model

$$\bar { l } = A \left [ \begin{array} { c } a \\ b \end{array} \right ] + \epsilon$$

where

$$A = \left [ \begin{array} { c c c } \log p _ { 1 } & \dots & \log p _ { Q } \\ 1 & \dots & 1 \end{array} \right ] ^ { T } .$$

Now, taking a method-of-moments (MOM) approach, in which (6) is used to solve for the linear least squares (LLS) estimates

Fig. 1. Building local neighborhoods. From left to right: start with point y i ; fi nd its 3 -NN points; for each of the NN points just found, compute their 3 -NN points.

ˆ a, ˆ b of a, b , ˆ m and ˆ H can be determined by inversion of the relations (5). After making a simple large n approximation, this approach yields the following estimates:

$$\hat { m } & = \text {round} \{ \gamma / ( 1 - \hat { a } ) \} \\ \hat { H } _ { \hat { \alpha } } ^ { ( \mathcal { M } , g ) } & = \frac { \hat { m } } { \gamma } \left ( \hat { b } - \log \beta _ { \hat { n } , \gamma , k } \right ) \, .$$

III. L OCAL I NTRINSIC D IMENSION E STIMATION

Let {M 1 , . . . , M P } be a collection of disjoint compact Riemann submanifolds of R d and define M = ∪ P j =1 M j . Each manifold M j has unknown intrinsic dimension m j ≥ 2 , which may be different from manifold to manifold. Let f i be the density (with respect to μ g i ) of the samples on each manifold.

Given a set of n samples Y n ∈ M , the goal is to estimate the local dimension associated with each sample Y i , i.e., the dimension of manifold M j where Y i lies. Of course, this has to be accomplished without any prior knowledge on the number of different manifolds, intrinsic dimensions, sampling distribution or segmentation of the data. If the segmentation of the data set according to local manifolds was known in advance, then repeated applications of Theorem 1 to each manifold segment would yield consistent estimates for each point. However, such information is not available and local neighborhoods with similar geometric structure have to be automatically determined from the data. We propose the following general algorithm (see Figure 1):

$$\ f o r \ i = 1 \ t o \ n \ d o$$

1. Grow a local k -NN graph for y i : a) initialize N = { y i } , b) for all y ∈ N compute the set of its k -nearest neighbors, N k, y ( Y n ) . N ← ∪ y ∈N N k, y ( Y n ) ; c) goto b) until stopping criterion is met.
2. Apply the estimation algorithm described in Section II to the graph built in step 1, and obtain a local dimension estimate ˆ m ( y i ) .

end .

The challenging part of the algorithm described above is the selection of a criterion that stops the growing of the local k -NN graph. On the one hand, the graph should be small enough so that only the geometry of the local manifold where sample point y i lies is captured by the graph. On the other hand, the graph should include enough samples so that the asymptotic regime described by Theorem 1 is valid, resulting in statistically consistent estimates. Any stopping rule should take into account this tradeoff between local geometry and asymptotic consistency. We propose an heuristic rule based on the geometric and asymptotic properties of k -NN graphs.


<!-- p:3 -->


The k -NN graph satisfies certain geometric properties, like subadditivity and superadditivity [9], which imply that the graph can be approximately computed in a greedy fashion in the following way. First partition R d into a finite number of disjoint sets. Then, build a k -NN graph on the samples that fall on each disjoint set and compute its total edge length functional. Summing all contributions from each total edge length functional provides a good approximation for the global value of the functional, as long as the number of samples falling on each individual partition set is significant. According to [10], the number of samples that minimizes upper bounds on the convergence rate of (2) to its asymptotic limit is roughly of order O ( n 1 /d ) . According to this result, a simple stopping rule can then be to grow the local k -NN graph until it incorporates a total of O ( n 1 /d ) sample points.

We are currently studying other stopping rules based on adaptive neighborhood graphs [11] that have provable geometric properties.

## IV. R ELATED M ETHODS

The local dimension estimation method proposed here is conceptually related to the estimation of the following functional of the density of the sample points:

$$\log \int _ { B ( y _ { 0 } , r ) } g ( f ( y ) ) \, \mu ( d y ) \ , \quad \ \ \ ( 8 ) \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \$$

where g is a strictly increasing function and B ( y 0 , r ) is the ball of radius r centered at y 0 . Under suitable regularity conditions on f and g , using the mean value theorem results in:

$$\log \int _ { B ( y _ { 0 } , r ) } g ( f ( y ) ) \, \mu ( d y ) = m y _ { 0 } \, \log r + c + o ( 1 ) \ , \quad ( 9 ) \quad \text {where} \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \$$

where c is a constant depending on f, g and the volume of the unit sphere and o (1) → 0 when r → 0 . Compare equation (9) to equation (4). By choosing different functions g and radii r one can develop new estimators for the local dimensionality m y 0 .

For example, by choosing g ( u ) = 1 , then functional (8) can be estimated by the number of points falling into B ( y 0 , r ) . This is the motivation behind correlation dimension methods [3], [12]. If r is chosen adaptively according to the distance from y 0 to its k -nearest neighbor, T k ( y 0 ) , then (8) is given by k/n , the proportion of samples within a radius T k ( y 0 ) of y 0 . This is the starting point for earlier methods for estimating intrinsic dimension based on k -NN distances [13].

Fig. 2. Estimating the local dimension of the Swiss roll and the sphere. The estimated local dimension was 2 for the black points and 3 for the blue points.

In [6], a similar approach is followed, but the (binomial) number of points falling in B ( y 0 , T k ( y 0 )) is approximated by a Poisson process, for samples uniformly distributed over the manifold. Then the intrinsic dimension is estimated by maximum likelihood, resulting in the following local estimate:

$$\hat { m } y _ { _ { 0 } } = \frac { 1 } { k - 1 } \sum _ { j = 1 } ^ { k - 1 } \log \frac { T _ { k } ( y _ { _ { 0 } } ) } { T _ { j } ( y _ { _ { 0 } } ) } \ .$$

### V. S IMULATIONS

We now illustrate the application of the proposed method on collections of synthetic manifolds of known dimension. We compare it to the maximum likelihood (MLE) method proposed in [6] for dimension estimation.

We first start with simple low-dimensional manifolds embedded in R 3 for the purpose of visualization. Figure 2 shows the results of applying the proposed algorithm to a threedimensional data set composed of two manifolds. This set consists of 200 hundred points sampled uniformly on the 2 - dimensional 'Swiss roll' and 300 points sampled uniformly on the 3 -dimensional sphere. The black points have an estimated local dimension of 2 , while the blue points have an estimated local dimension of 3 . Figure 3 shows the histogram of the local dimension estimates. As it can be seen, almost all points were labeled with the correct dimension, except for a few that live close to the intersection of both manifolds.

The histogram of local dimension estimates obtained by the MLE method is also shown is Figure 3, where it can be observed to have a slightly better performance. This is due to the fact that that the MLE approach relies on an approximation of a binomial process by a Poisson process. This approximation converges at a rate of order O ( n - 1 ) , as opposed to a much slower rate of order roughly O ( n - 1 /d ) for the graph based methods. As such, for higher dimensions, the MLE method will tend to outperform the proposed method. However, this comes at a cost, as the fast convergence rate of the MLE method is only valid for the case of sample points uniformly distributed over the manifold. When the density of the samples departs from a uniform distribution on the manifold, the effective convergence rate may be less than order O ( n - 1 ) , as it will be slowed down by the variations of the distribution. This phenomenon can be observed in Figure 4 that shows the histogram of dimension estimates for a 6 - dimensional hyper-sphere sampled according to a Bingham distribution [14], whose density with respect to the Lebesgue measure on the hyper-shere is


<!-- p:4 -->


Fig. 3. Histogram of local dimension estimated for the Swiss roll + Sphere data set.

Fig. 4. Histogram of local dimension estimated for the non-uniform 6 -D hyper-sphere.

$$f ( y ) \, \alpha \, \exp \{ y ^ { T } \, K y \} \, ,$$

where K is a symmetric matrix.

Figure 5 shows similar results to the ones described previously for a data set consisting of a 3 -dimensional sphere and the 2 -dimensional S curve in R 3 . As it can be seen, all points were labeled with the correct dimension.

### A. Complexity Segmentation

We now apply the proposed method to a synthetic image database. The goal is to classify images according to their complexity, i.e., the intrinsic dimensionality of the model used to generate them. In our simplified experiment, we generated gray scale 3 × 3 pixel images according to the following model. For a d -dimensional database, choose d seed pixels that will be generated independently from each other. The remaining pixels are generated according to a linear or nonlinear function of the seed pixels. For example, Figure

Fig. 5. Estimating the local dimension of the S curve and the sphere. The estimated local dimension was 2 for the black points and 3 for the blue points.

7(a) shows a 2 -D database where the first two columns of each image are linearly dependent on the seed pixel located at the uppper rightmost corner, while the last column is a linear function of the upper leftmost corner pixel. If I ij is the intensity of pixel ij , then the model is:

$$\{ I _ { i j } \} = \left [ \begin{array} { c c c } 1 & c _ { 1 2 } & 1 \\ c _ { 2 1 } & c _ { 2 2 } & c _ { 2 3 } \\ c _ { 3 1 } & c _ { 3 2 } & c _ { 3 3 } \end{array} \right ] \cdot \left [ \begin{array} { c c c } I _ { 1 1 } & 0 & 0 \\ 0 & I _ { 1 1 } & 0 \\ 0 & 0 & I _ { 1 3 } \end{array} \right ] \ ,$$

,

where I 11 and I 13 are the independent random seeds and c ij are fixed coefficients. Figure 7(b) shows a 3 -D database, where each column is generated independently, according to:

$$\{ I _ { i j } \} = \left [ \begin{array} { c c c c } 1 & 1 & 1 \\ d _ { 2 1 } & d _ { 2 2 } & d _ { 2 3 } \\ d _ { 3 1 } & d _ { 3 2 } & d _ { 3 3 } \end{array} \right ] \cdot \left [ \begin{array} { c c c c } I _ { 1 1 } & 0 & 0 \\ 0 & I _ { 1 2 } & 0 \\ 0 & 0 & I _ { 1 3 } \end{array} \right ] \ ,$$

for fixed coefficients d ij and independent random seeds I 11 , I 12 and I 13 . The aim of these models is to simulate databases that contain images/textures with different patterns or edges, for example, which are inherently of different intrinsic dimensionality, and thus complexity.

Figure 7 shows the histograms resulting from applying the discussed methods to a database consisting of merging 400 samples of 2 -D images with 400 samples of 3 -D images. Unlike the MLE method, the proposed method succeeds at finding the right proportion of samples from each dimensionality. However, regarding classification rates, i.e, the number of samples whose dimensionality was correctly estimated, both methods behave similarly, with rates of correct classifications around 75% .

## VI. C ONCLUSIONS

We have introduced a new method to estimate intrinsic local dimensionality associated with each data sample. This represents the first attempt towards developing a robust nonparametric method that will be able to segment a data set into regions of different complexities. This complexities can be a product of, for example, different textures, number of edges, etc, that impose nonlinear constraints on the data set. Several issues have to be addressed before achieving this goal.


<!-- p:5 -->


Fig. 6. Samples from image databases with different complexities.

Fig. 7. Histogram of local dimension estimated for the 2 -D and 3 -D image databases.

The key block behind a local dimensionality estimator is an algorithm that finds a local adjacency graph that connects points with similar geometric properties. We are currently studying adaptive neighborhood graphs that find local neighborhoods of points that lie on the same manifold. We are also implementing a two step procedure that uses the first complexity segmentation to construct new adjacency graphs using only the points classified with the same intrinsic dimension.

Another possible improvement to the performance of the algorithm is the development of a block resampling and bootstrap procedure that will account for the dependencies among resamplings when estimating the slope in equation (4). This method might also prove useful for extending the current methodology to non i.i.d. samples. Examples of such data sets include, among others, time series obtained from Internet traffic traces.

Also of interest are applications to streaming data problems. This will require developing algorithms to compute k -NN

graph neighborhoods recursively.

Finally, we are developing the asymptotic analysis necessary to guarantee the statistical consistency of the proposed method.

We remark that the problem of sampling a manifold with noise was not considered in this paper. That is a subject of future work.

##### R EFERENCES

- [1] 'Manifold learning resource page,' http://www.cse.msu.edu/  ̃lawhiu/manifold/ .
- [2] F. Camastra and A. Vinciarelli, 'Estimating the intrinsic dimension of data with a fractal-based method,' IEEE Trans. on Pattern Analysis and Machine Intelligence , vol. 24, no. 10, pp. 1404-1407, October 2002.
- [3] B. K ́ egl, 'Intrinsic dimension estimation using packing numbers,' in Neural Information Processing Systems: NIPS , Vancouver, CA, Dec. 2002.
- [4] J. A. Costa and A. O. Hero, 'Geodesic entropic graphs for dimension and entropy estimation in manifold learning,' IEEE Trans. on Signal Processing , vol. 52, no. 8, pp. 2210-2221, August 2004.
- [5] J. A. Costa and A. O. Hero, 'Entropic graphs for manifold learning,' in Proc. of IEEE Asilomar Conf. on Signals, Systems, and Computers , Pacifi c Grove, CA, November 2003.
- [6] E. Levina and P. Bickel, 'Maximum likelihood estimation of intrinsic dimension,' in Neural Information Processing Systems: NIPS , Vancouver, CA, Dec. 2004.
- [7] H. Edelsbrummer, M. Facello, and J. Liang, 'On the defi nition and the construction of pockets on macromolecules,' Discrete Applied Math. , vol. 88, pp. 83-102, 1998.
- [8] M. Carmo, Riemannian geometry , Birkh ̈ auser, Boston, 1992.
- [9] J. E. Yukich, Probability theory of classical Euclidean optimization problems , vol. 1675 of Lecture Notes in Mathematics , Springer-Verlag, Berlin, 1998.
- [10] A. Hero, J. Costa, and B. Ma, 'Convergence rates of minimal graphs with random vertices,' submitted to IEEE Trans. on Inform. Theory , 2003, www.eecs.umich.edu/ ̃hero/det\_est.html .
- [11] J. Giesen and U. Wagner, 'Shape dimension and intrinsic metric from samples of manifolds,' in Proceedings of the 19th Annual ACM Symposium on Computational Geometry , 2003.
- [12] P. Grassberger and I. Procaccia, 'Measuring the stangeness of strange attractors,' Physica D , vol. 9, pp. 189-208, 1983.
- [13] K. Pettis, T. Bailey, A. Jain, and R. Dubes, 'An intrinsic dimensionality estimator from near-neighbor information,' IEEE Trans. on Pattern Analysis and Machine Intelligence , vol. 1, no. 1, pp. 25-36, 1979.
- [14] G. S. Watson, Statistics on Spheres , John Wiley &amp; Sons, 1983.
