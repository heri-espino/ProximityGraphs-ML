---
id: "Brito-Quiroz-Yukich_2013_Intrinsic-Dimension-Graph-Theoretic-Methods"
source_pdf: "../pdf/Brito-Quiroz-Yukich_2013_Intrinsic-Dimension-Graph-Theoretic-Methods.pdf"
source_filename: "Brito-Quiroz-Yukich_2013_Intrinsic-Dimension-Graph-Theoretic-Methods.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "excellent"
extraction_score: 100.0
visual_assets: "disabled"
references_file: "../references/Brito-Quiroz-Yukich_2013_Intrinsic-Dimension-Graph-Theoretic-Methods.references.md"
---

<!-- p:1 -->

Contents lists available at SciVerse ScienceDirect

## Journal of Multivariate Analysis

[journal homepage: www.elsevier.com/locate/jmva](http://www.elsevier.com/locate/jmva)

## Intrinsic dimension identification via graph-theoretic methods

M.R. Brito a,c , A.J. Quiroz b,c, ∗ , J.E. Yukich d

a Dpto. de Matemáticas Puras y Aplicadas, Universidad Simón Bolivar, Venezuela

b Dpto. de Cómputo Científico y Estadística, Universidad Simón Bolivar, Venezuela

c Dpto. de Matemáticas, Universidad de Los Andes, Colombia

d Department of Mathematics, Lehigh University, USA

###### a r t i c l e i n f o

Article history: Received 18 August 2011

Available online 11 January 2013

AMS subject classifications: primary 62H99 60D05 secondary 62G99

Keywords:

Graph theoretical methods Stabilization methods Dimensionality reduction

### 1. Introduction

In the statistical analysis of complex data sets, it is frequently the case that data points are represented in a high dimensional Euclidean space, R d , but the data actually live in an m -dimensional manifold, with m ≪ d . This is the case, for instance, when one takes a set of digital images of the same subject. Thinking of black and white images, for simplicity, each image is coded by a very high dimensional vector, in which each coordinate represents the light intensity in a pixel, and the number of pixels may be 400 × 600 or more. Still, if we represent each image by the point in R 3 from where it was taken, knowledge of this three dimensional representation will be enough for understanding and classification of the set of pictures. Actually, in this example, depending on how the pictures are taken, the value of m could be 1, 2 or 3. Similar situations arise in other image analysis applications, in the analysis of text and of genetic data, and in most cases, the value of m might not be as obvious as in our example. Several authors in the artificial intelligence literature have argued about the convenience of having methods to find automatically, whenever possible, a low-dimensional manifold representation of high dimensional data [2,3,7,25,27,28,30].

Methods for the representation of high dimensional data in a lower dimensional manifold are termed manifold projection methods . Two popular such methods are Isomap, of Tenenbaum, de Silva and Langford [30] and the Locally Linear Embedding method of Roweis and Saul [25]. In these references, it is suggested that the intrinsic dimension of the data can be ''guessed'' by observing the decrease in error (in the approximate representation) as the value of m varies, as was traditionally done in

∗ Corresponding author at: Dpto. de Matemáticas, Universidad de Los Andes, Carrera 1, Nro. 18A-10, edificio H, Bogotá, Colombia. E-mail addresses: aj.quiroz1079@uniandes.edu.co, ajquiroz@gmail.com (A.J. Quiroz).

##### a b s t r a c t

Three graph theoretical statistics are considered for the problem of estimating the intrinsic dimension of a data set. The first is the ''reach'' statistic, r j , k , proposed in Brito et al. (2002) [4] for the problem of identification of Euclidean dimension. The second, Mn , is the sample average of squared degrees in the minimum spanning tree of the data, while the third statistic, U k n , is based on counting the number of common neighbors among the k - nearest, for each pair of sample points { Xi , Xj } , i &lt; j ≤ n . For the first and third of these statistics, central limit theorems are proved under general assumptions, for data living in an m -dimensional C 1 submanifold of R d , and in this setting, we establish the consistency of intrinsic dimension identification procedures based on r j , k and U k n . For Mn , asymptotic results are provided whenever data live in an affine subspace of Euclidean space. The graph theoretical methods proposed are compared, via simulations, with a host of recently proposed nearest neighbor alternatives.

© 2013 Elsevier Inc. All rights reserved.

<!-- p:2 -->


the context of Multidimensional Scaling. A more precise initial estimation of m , of low computational cost, can be of great help in the application of manifold projection methods.

In the present article, as in [22], it will be understood that though data are given in R d , they actually live in an m - dimensional, C 1 submanifold M of R d , m ≤ d , endowed with the subset topology, and that the goal is the estimation of the dimension m from an i.i.d. sample.

Various nearest-neighbor methods attempting to estimate the value of m have appeared recently in the statistical and artificial intelligence literature. Some of the ideas behind these methods can be traced to Pettis et al. [23] and Grassberger and Procaccia [11]. With the brief description of these methods we start introducing notation that will be used throughout. Let X n := { Xi } n i = 1 denote the i.i.d. sample. The dimension estimator of Grassberger and Procaccia [11] is based on the U -statistic which computes the fraction of data pairs, Xi , Xj satisfying ∥ Xi - Xj ∥ &lt; r , for positive r . Secondly, let Dk ( Xi ) := Dk ( Xi , X n ) be the distance from the sample point Xi to its k -th nearest neighbor in the sample. Denoting Dk the sample average of these distances, for each k in a given range, the nearest neighbor dimension estimator of Pettis et al. [23] is based on plotting log ( Dk ) against log ( k ) and estimating the slope of the plot. Thirdly, Kegl [14] suggests using sample estimators of the packing number corresponding to the dimension where the data live, an idea motivated on the fast variation of packing numbers with dimension. The difficulty with this approach is that precise estimation of the packing number is, computationally, a very hard problem, and in practice one has to work with rather crude approximations.

Neither of these three methods provides a direct estimation of intrinsic dimension m , but rather its value must be deduced indirectly, from the slope of a line, for instance. Levina and Bickel [17], on the other hand, propose a ''maximum likelihood'' estimator of intrinsic dimension, arguing that, asymptotically, the expected value of the statistic

$$\hat { m } _ { k } ( X _ { i } ) \colon = \left [ \frac { 1 } { k - 2 } \sum _ { j = 1 } ^ { k - 1 } \log \frac { D _ { k } ( X _ { i } ) } { D _ { j } ( X _ { i } ) } \right ] ^ { - 1 }$$

is the intrinsic dimension of the data. Thus, one expects that the average over the sample, namely mk := n - 1  n i = 1 ˆ mk ( Xi ) , is an asymptotically unbiased estimator of the intrinsic dimension. If k ≥ 4 and if the data have a density which is bounded away from zero and infinity on a subset of a C 1 submanifold of R d , m ≤ d , then Theorem 2.1 in [22] establishes that mk converges in probability to the intrinsic dimension m , as the sample size n tends to infinity. (If k ≥ 11 then mk converges a.s., as n → ∞ , to the intrinsic dimension.) Theorem 4.3 in [3] establishes a central limit theorem for mk as n → ∞ , for data in an affine subspace of R d , whereas for data belonging to a manifold, Theorem 2.1 in [22] establishes a central limit theorem for mk , conditioned on nearest neighbor distances being not too large. Levina and Bickel carry out comparisons of their procedure against the correlation dimension estimator of Grassberger and Procaccia [11] and the nearest-neighbor estimator of Pettis et al. [23], and conclude that mk has a better performance.

Costa, Girotra and Hero [5] propose a method based on the total (power) length of the k -nearest-neighbor graph, namely

$$L _ { \gamma , k } \coloneqq L _ { \gamma , k } ( X _ { n } ) = \sum _ { i = 1 } ^ { n } \sum _ { j = 1 } ^ { k } D _ { j } ( X _ { i } ) ^ { \gamma } ,$$

where γ is a power weighting constant. The use of (2) is justified by the following law of large numbers (Theorem 1 in [5]). Assume that the data sample lives in an m -dimensional compact Riemannian submanifold M , of R d , and is obtained from a continuous distribution on M with density f bounded away from zero and infinity. Let g be the Riemannian metric defined on M and let μ g be the associated volume measure. If 1 ≤ γ ≤ m , m ≥ 2, and d ′ is any positive integer, then, almost surely,

$$\lim _ { n \to \infty } \frac { L _ { \gamma , k } } { n ^ { d ^ { \prime } - \gamma / d ^ { \prime } } } = \begin{cases} \infty & \text {if } d ^ { \prime } < m \\ \beta _ { m , \gamma , k } \int _ { \mathcal { F } ^ { \mu } ( x ) d \mu _ { g } ( x ) } & \text {if } d ^ { \prime } = m \\ 0 & \text {if } d ^ { \prime } > m \end{cases}$$

where α = ( m - γ)/ m and β m ,γ , k is a constant not depending on f , M or g

.

From the above law of large numbers, [5] proposes a consistent bootstrap procedure for the estimation of m : Let p 1 , . . . , pQ be integers in ( 0 , n ) and N a fixed fraction of n . For each l in 1 , . . . , Q , produce N samples of size pl , say X j p l , for j = 1 , . . . , N , by resampling with replacement from the original sample X n . Fix l for the moment. For each bootstrap sample X j p l , compute L γ, k ( X j p l ) . Average the N values obtained to get Lpl , and let l p l = ln Lpl . After this calculus has been done for each l , adjust the model

$$\bar { l } _ { p _ { I } } = a \, \ln p _ { I } + b + \epsilon _ { I }$$

by ordinary least squares. If ˆ a stands for the estimator of a in the model above, then ˆ m = round (γ /( 1 - ˆ a )) is a consistent (as n goes to infinity) estimator of m (see [5] for more details).

Farahmand, Szepesvári and Audibert [7] present a direct estimate of m , based on nearest neighbor distances. Given r ∈ ( 0 , ∞ ) and x ∈ R d , let Br ( x ) denote the ball in R d of radius r and center x . Define η( x , r ) by

$$P [ X _ { i } \in B _ { r } ( x ) ] = \colon \eta ( x , r ) r ^ { m } .$$


<!-- p:3 -->


For small r , η( x , r ) is an approximation to the data density at x ∈ M . For i ≤ n , let

$$\hat { m } ( X _ { i } ) \coloneqq \frac { \ln 2 } { \ln ( D _ { k } ( X _ { i } ) / D _ { | k | 2 } ( X _ { i } ) ) } \quad \text {and} \quad \hat { m } \coloneqq \text {round} \left ( \frac { 1 } { n } \sum _ { i = 1 } ^ { n } ( \hat { m } ( X _ { i } ) \wedge d ) \right ) ,$$

where a ∧ b := min ( a , b ) . Under differentiability assumptions on the function η and regularity assumptions on M , exponential bounds for the probability that ˆ m , in (4), differs from m , for large enough n , are given in [7]. In particular, under those assumptions, this estimator is consistent in probability for the dimension m .

Recently, Sricharan, Raich, and Hero [28] have proposed another direct procedure for estimation of m , using ideas related to k -nearest neighbors density estimators. Partition the sample X n into two disjoint sets, say Y and Z of respective sizes N and M . For each Yi ∈ Y , let Rk ( Yi ) denote the distance from Yi to its k -th nearest neighbor in Z . For a positive γ , let

$$T _ { k } ( X _ { n } ) \colon = \frac { \gamma } { N } \sum _ { i = 1 } ^ { N } \log R _ { k } ( Y _ { i } ) .$$

The ''improved'' estimator for m proposed in [28] is

$$\hat { m } \coloneqq \frac { \gamma \left ( \log ( k _ { 2 } - 1 ) - \log ( k _ { 1 } - 1 ) \right ) } { T _ { k _ { 2 } } ( X _ { n } ) - T _ { k _ { 1 } } ( X _ { n } ) }$$

for k 1 &lt; k 2. Although no theoretical results are given in [28] for the estimator (5), approximate formulas for the bias and variance and a central limit theorem are stated for an associated estimator and it is argued that the behavior, in terms of variance, of the improved version should be better than that of the associated statistic. Also, in [28] optimal criteria are obtained for the choice of M , N , k 1 and k 2 in (5), but these criteria are of limited practical application since the formulas obtained for the parameters depend on some unknown constants, including the dimension m to be estimated.

In the following section we present the graph theoretical methods for intrinsic dimension identification to be discussed here. Section 3 includes results of a Monte Carlo performance comparison of the graph theoretical methods with the k - nearest neighbor methods of [5,7,17,28], described above. Section 4 provides some theoretical results that support the methods introduced here, including central limit theorems for the ''reach'' statistic and the ''mutual neighbors'' statistic of Section 2, assuming that the data live in a C 1 manifold.

### 2. Graph theoretical methods

Since the series of papers of Friedman and Rafsky [8-10] it has been clear that graph theoretic methods offer a natural way of dealing with non-parametric statistics in the multivariate setting. The article [24] gives a brief account of the different applications of graph theoretic methods on a variety of statistical problems, including the two-sample problem, outlier identification and clustering, among others. In this reference, or in any classical book on Graph Theory (for instance, Harary, [12]) the reader can find the graph theoretic definitions required in what follows. Penrose and Yukich [19-22] as well as [31] explain some of the main mathematical ideas that validate, asymptotically, these sorts of methods.

Starting from a d -dimensional data set X n , or more precisely, from the corresponding interpoint distances, different graphs can be built that establish connections (edges) between nearby sample points. Examples include the k -nearestneighbor graph, Gk , the minimum spanning tree graph and the sphere of influence graph, which are three types of ''proximity graphs''; see Aldous and Shun [1]. For a description of the first two, the reader can look in the references of Friedman and Rafsky [8-10], while the sphere of influence graph, has been studied in [19]. Once a proximity graph H has been constructed from a data sample, we may abstract from the data and look at statistics which are functions only of graph theoretic properties of H , such as vertex degrees, vertex eccentricities, length of paths between vertices, diameter of the graph, and so on. Procedures based on these types of statistics are what we call graph theoretic methods. Since the estimators of intrinsic dimension of [5,7,17,28] require for their computation the actual values of the nearest neighbor distances, they do not fall in the graph theoretic category. The main advantages of using graph theoretic methods are, in our opinion:

- (i) Low computational cost. Most of the graphs considered in these methods and the statistics calculated from them can be computed at a sub-quadratic cost, with respect to the sample size. See [8] and references therein.
- (ii) Robustness. The construction of the graphs does not require exact knowledge of the interpoint distance. Only the ordering among these distances is required. Thus, for data coming from a continuous distribution, there is an ε &gt; 0 such that statistics based on these graphs are invariant if the data is perturbed by a noise component of Euclidean norm less than ε . Small amounts of noise will thus not affect the analysis in an important manner, unless a significant fraction of distance comparisons is altered.
- (iii) Availability of theory. A number of theoretical tools exist for the study of properties of graph theoretic statistics, including methods for proving laws of large numbers, central limit theorems and consistency of the corresponding parameter estimators. See [19,22,31]. In many important problems, the graph theoretic procedures turn out to be asymptotically non-parametric.


<!-- p:4 -->

degree

Fig. 1. Average degree frequencies in MST.

In the context of Multidimensional Scaling, Brito, Quiroz and Yukich [4] propose a graph theoretical method for identifying the Euclidean dimension of a data set. The method is based on the ''reach'' of data in the k -nearest neighbor graph, defined as follows. Recall that in the k -nearest-neighbor graph, Gk := Gk ( X n ) the vertex set is the sample X n . For x , y ∈ X n , x ̸= y and j a fixed positive natural number, say that y can be reached in j steps from x , if there exists a path v 0 , v 1 , . . . , v j in Gk with v 0 = x and v j = y . The reach in j steps of vertex x ∈ X n , r j , k ( x , X n ) , is the total number of vertices that can be reached from x in j steps or less in Gk . The statistics considered in [4] is the average reach in j steps of points in Gk , namely

$$\bar { r } _ { j , k } ( x _ { n } ) \colon = \frac { 1 } { n } \sum _ { x \in x _ { n } } r _ { j , k } ( x , x _ { n } ) .$$

The intuition for considering the statistic r j , k ( X n ) is that, as the dimension increases, there are more directions in which a given sample point can find neighbors and, therefore, the amount of points reached in j steps in Gk , should increase with dimension. For data living in Euclidean space, a law of large numbers for r j , k ( X n ) is established in [4]. This result is extended here to data living in a C 1 submanifold of R d and, in this context, a central limit theorem for r j , k ( X n ) is given as well (see Remark(ii) following Theorem 1 in Section 4). This leads to a consistency result for an estimator of intrinsic dimension based on r j , k ( X n ) (Theorem 4).

To introduce a second estimator of intrinsic dimension, let Tn := Tn ( X n ) be the minimum spanning tree (MST) associated to the sample X n . Let deg ( Xi ) := deg Tn ( X n ) ( Xi ) denote the degree of node Xi in Tn , that is, the number of Xj 's, j ̸= i , such that { Xi , Xj } is an edge of Tn . Steele, Shepp and Eddy [29] showed that for data obtained from a continuous distribution on R d , the fraction of nodes with a given degree, j , in Tn , converges almost surely to a limit depending only on j and d . Fig. 1 shows the average fractions of nodes with each given degree up to 7, for MSTs in dimension 2-8 for samples of size n = 1000 from the Uniform distribution on the unit cube. For each dimension, the averages are computed over 50 samples. We see, in this figure, that the degree distribution in the MST is monotonically changing with dimension: As the dimension increases, the number of leaves (nodes of degree 1) is increasing, as is the fraction of nodes with large degree (degree ≥ 4). Recall that the average degree in a tree is a constant, depending only in the number of vertices. On the other hand, that the fraction of nodes with large degree increases with dimension, suggests that the average of a power greater than 1 of the node degrees in the MST might capture the difference between dimensions. We are thus motivated to consider the following estimator of intrinsic dimension:

$$M _ { n } \coloneqq M ( X _ { n } ) \coloneqq \frac { 1 } { n } \sum _ { i = 1 } ^ { n } ( \deg ( X _ { i } ) ) ^ { 2 } . \\$$

Fig. 2 shows average values of Mn for different dimensions, up to 12. For each dimension, the average is obtained from a set of 100 Mn values computed on independent samples of size n = 1000 from the d -dimensional Uniform distribution. It is clear that the mean of this random variable behaves monotonically with dimension in the range considered.


<!-- p:5 -->


Fig. 2. Average Mn as function of dimension.

Mutual neighbor and neighbor sharing probabilities are studied by Schilling [26] in connection with test statistics for the multivariate two-sample problem. Schilling shows that these probabilities, for samples from continuous distributions, converge to limits that do not depend on the particular density producing the sample. In particular, the limits of mutual neighbor probabilities (for samples from continuous distributions in Euclidean space) depend only on the dimension of the support of the data. This fact motivates our third estimator of dimension identification, defined as follows.

The sphere of influence graph, studied, for instance, in [19], is a proximity graph defined as follows: For each sample point, Xi , consider the closed ball B ρ( i )( Xi ) with center Xi and radius ρ( i ) equal to the distance between Xi and its nearest neighbor in the sample. The sphere of influence graph S 1 := S 1 ( X n ) has the sample X n as its vertex set, and an edge exists between Xi and Xj iff the corresponding nearest neighbor balls intersect, that is, iff ∥ Xi - Xj ∥ ≤ ρ( i ) + ρ( j ) . We shall consider a generalization of the sphere of influence graph, as follows. Let Sk , called the k -sphere of influence graph, be defined in the same way as S 1 but instead of ρ( i ) , we shall use ρ k ( i ) , defined as the distance between Xi and its k -th nearest neighbor in the sample. That is, an edge exists between Xi and Xj in Sk if ∥ Xi - Xj ∥ ≤ ρ k ( i ) + ρ k ( j ) . This is a way of enriching the sphere of influence graph, by adjoining more edges to it. We define a third graph theoretical intrinsic dimension statistic in the context of Sk . Let Ni , j denote the number of sample points, other than Xi and Xj , in the intersection B ρ k ( i )( Xi ) ∩ B ρ k ( j )( Xj ) . Ni , j is the number of neighbors, among the k -nearest, that the points Xi and Xj share. A similar intuition to the one motivating the consideration of r j , k , leads us to consider the statistic

$$U _ { n } ^ { k } \coloneqq U ^ { k } ( X _ { n } ) \coloneqq \frac { 1 } { n } \sum _ { i < j } N _ { i , j } .$$

The intuition is that, as the dimension grows, every point is more likely to be closer to any other point in the sample, in terms of length of the connecting path in Gk , and thus, the expected number of neighbors shared by a given pair of data points, should grow with dimension. Although (7) suggests that the computation of U k n has quadratic complexity in the sample size, it turns out to be easy to compute, once the k -th nearest neighbor graph has been created, with computational complexity O ( nk ) , as follows. Suppose we have a n × k table that contains the identities (indices), for each i ≤ n , of the k nearest neighbors of Xi in the sample. One pass through this table is enough to compute, for each Xi , the random variable

ck ( Xi , X n ) := card { j ≤ n : Xi is one of the k nearest neighbors of Xj in the sample X n } .

Since each sample point Xl , 1 ≤ l ≤ n , appears in a total of  c k ( X l , X n ) 2  summands Ni , j , we get that U k n in (7) can be computed as

$$U ^ { k } ( X _ { n } ) = \frac { 1 } { n } \sum _ { i = 1 } ^ { n } \left ( \begin{pmatrix} c _ { k } ( X _ { i } , X _ { n } ) \\ 2 \end{pmatrix} .$$

It follows that the computational complexity of U k n is the same as that of constructing the k -th nearest neighbor graph, which is less than quadratic, according to Friedman and Rafsky [8].


<!-- p:6 -->


Fig. 3. Average U 1 n as function of dimension.

Fig. 3 shows the averages of U 1 n := U 1 n ( X n ) values, for dimensions 2-12. As in Fig. 2, for each dimension, the U 1 n are computed on 100 samples of size n = 1000, from the Uniform distribution on the d -dimensional unit cube. Again, we see a clear tendency of the statistic U 1 n ( · ) to grow nearly linearly with dimension, suggesting that it might be appropriate for the identification of intrinsic dimension. For values of k larger than 2, (experiments not included here) a similar behavior of U k n ( X n ) is observed, as a function of dimension.

Figs. 2 and 3 and the results in [4] suggest that, at least for a relevant set of dimensions, a linear dependence can be established between all the graph theoretical statistics presented above and the underlying data dimension. In each case, one could find a linear formula to predict the dimension from the value of the graph theoretical statistic. We shall not pursue this line of research, since it would not take into consideration the variability that each graph theoretical statistic presents in each dimension, but only the average value of the statistics in the different dimension. To take advantage of all the information obtained from simulations, including estimated means and variances, and the information provided by theoretical results (Section 4) regarding the asymptotic Gaussian distribution of the statistics, it seems more sensible to employ a Bayesian decision theoretic procedure, described below, since it is known to converge to the smallest possible error rate based on a given statistic (see Chapter 2 in [6]). A drawback of our approach is the need to estimate parameters of the distribution of the statistic to be used, but this is a one-time cost, since simulations can be performed for the Uniform distribution on the d -dimensional unit cube and, by the asymptotic theory, the parameters estimated will be approximately valid for any data distribution satisfying the assumptions of the results in Section 4. Another possible objection to our proposed methodology is the reliance on asymptotic results, but this is essentially true of all the methods currently available for this problem. For instance, the statistic of Levina and Bickel [17] is known to be biased for small sample size, but asymptotically unbiased, and its use can be justified by the existence of a strong law of large numbers (Theorem 2.1 in [22]). Similarly the method of Costa, Girotra and Hero [5] is supported by a strong law of large numbers for the total length statistic L γ, k ( X n ) . Perhaps the one exception to this dependence on asymptotics is the method of Farahmand, Szepesvári and Audibert [7], in which bounds for the probability of error in the estimation of m are provided for finite n , although the values of n required for the bounds to be valid depend on constants that are not known.

We shall now describe the setup for the approximate Bayesian estimators to be used with each of the three graph theoretic statistics described above (the reach statistic, r j , k , the average of squared degrees in the MST, Mn , and the mutual neighbors statistic, U k n ). In the context of manifolds we prove central limit theorems only for the first and third of these statistics, though we shall assume that a Gaussian approximation is valid for all of them. In the remainder of this section, Sn := Sn ( X n ) denotes any of these graph theoretic statistics. When the data live in an m -dimensional C 1 submanifold of R d , we assume that Sn ( X n ) converges in L 2 to a limit, μ( m ) , that does not depend on the particular density producing the sample, but only on m . Weassume further that

$$n \, V a r ( S _ { n } ( X _ { n } ) ) \to \sigma ^ { 2 } ( m ) , \ \ a s \, n \to \infty ,$$

for a positive constant σ 2 ( m ) depending only on m . Finally, we assume that

$$\sqrt { n } ( S _ { n } ( X _ { n } ) ) - \mathbb { E } ( S _ { n } ( X _ { n } ) ) \stackrel { \mathfrak { D } } { \longrightarrow } Z ,$$


<!-- p:7 -->


Table 1 Estimated parameters for graph theoretic statistics, n = 1000.

|   Dimension |   r 2 , 4 -  ̃ μ d |   r 2 , 4 -  ̃ σ d / √ n |   M n -  ̃ μ d |   M n -  ̃ σ d / √ n |   U 1 n -  ̃ μ d |   U 1 n -  ̃ σ d / √ n |
|-------------|-------------------|-------------------------|---------------|---------------------|-----------------|-----------------------|
|           2 |             12.58 |                   0.161 |         4.452 |              0.0172 |           0.319 |                0.0176 |
|           3 |             15.02 |                   0.202 |         4.637 |              0.0219 |           0.360 |                0.0235 |
|           4 |             17.01 |                   0.249 |         4.758 |              0.0303 |           0.392 |                0.0233 |
|           5 |             18.75 |                   0.273 |         4.860 |              0.0341 |           0.425 |                0.0251 |
|           6 |             20.27 |                   0.312 |         4.940 |              0.0434 |           0.452 |                0.0275 |
|           7 |             21.76 |                   0.334 |         5.010 |              0.0429 |           0.489 |                0.0310 |
|           8 |             23.14 |                   0.346 |         5.081 |              0.0405 |           0.529 |                0.0303 |
|           9 |             24.48 |                   0.398 |         5.155 |              0.0472 |           0.571 |                0.0342 |
|          10 |             25.65 |                   0.404 |         5.220 |              0.0504 |           0.608 |                0.0419 |
|          11 |             26.98 |                   0.399 |         5.302 |              0.0633 |           0.645 |                0.0452 |
|          12 |             28.13 |                   0.487 |         5.371 |              0.0648 |           0.690 |                0.0459 |

for a Gaussian random variable Z with mean 0 and variance σ 2 ( m ) . At least in the case of r j , k and U k n these assumptions are supported by the results in Section 4. We consider a finite set F of candidate values for the intrinsic dimension m . For each dimension j in F , we produce, by simulation, L samples of size n (large) from the Uniform distribution on the unit j -cube. For each sample generated, the statistic Sn is computed, and from the L values produced, we obtain the natural estimators  ̃ μ j and  ̃ σ 2 ( j ) of the parameters μ j and σ 2 ( j ) , for each j in F . In the Monte Carlo experiments used for parameter estimation and described in Section 3, we used F = { 2 , 3 , . . . , 12 } , n = 1000 and L = 100 for each statistic.

Suppose now a new data sample, of size n ′ , assumed to live in an m -dimensional submanifold of R d is presented and the value of m for these data is to be estimated. Based on the simulation results, the density of Sn ( X n ) in dimension j , evaluated at s ∈ R , is approximated as  ̃ f j ( s ) , the Gaussian density with mean  ̃ μ j and variance  ̃ σ 2 ( j )/ n ′ . Then, we compute the value of the graph theoretic statistic on the new data set, Sn ′ . Elementary Bayesian Decision Theory tells us that, assuming equal a priori probabilities for all the dimensions in F , the a posteriori probabilities, P [ j | Sn ′ ] corresponding to the dimensions considered, are

$$P [ j \ | \ S _ { n ^ { \prime } } ] = \frac { \tilde { f } _ { j } ( S _ { n ^ { \prime } } ) } { \sum _ { l \in F } \tilde { f } _ { l } ( S _ { n ^ { \prime } } ) } \quad \text {for} \, j \in F .$$

Choosing the value of j that maximizes (11) as the estimator of intrinsic dimension, corresponds to employing an approximation to the Bayesian Classifier, which is the best possible procedure based on Sn ′ (see Chapter 2 in [6], for instance). Still, since the intrinsic dimension is a numerical (non categorical) variable, it seems sensible to combine the information in the a posteriori probabilities and to use, as an estimator, the a posteriori expected value of the intrinsic dimension, given by

$$\tilde { m } \coloneqq \text {round} \left ( \frac { \sum _ { j \in F } ( S _ { j } ( S _ { n ^ { \prime } } ) } { \sum _ { j \in F } \tilde { \{ S _ { j } ( S _ { n ^ { \prime } } ) \} } \right ) .$$

Formula (12) is the one we shall use for our graph-theoretic estimation of intrinsic dimension; a proof of consistency of this method, valid when Sn is r j , k or U k n , is given in Theorem 4.

### 3. Monte Carlo evaluation of procedures for intrinsic dimension identification

The simulations described in the present section were carried out on a laptop computer using the statistical language R. We report first the result of the Monte Carlo experiments carried out for parameter estimation for the graph theoretic statistics r j , k , Mn , and U k n . For the reach statistic r j , k , the parameters were set to k = 4 and j = 2, while for U k n we worked with k = 1 (the statistic Mn does not require choice of parameters). For each statistic and each dimension j in F = { 2 , 3 , . . . , 12 } , M = 100 samples of size n = 1000 were generated from the Uniform distribution on the j -dimensional unit cube. For each sample, the statistic considered is computed, and from the M values available the sample mean is used as the estimator  ̃ μ j of the mean, while, if s 2 denotes the sample variance of the statistic values observed,  ̃ σ 2 ( j ) = n s 2 is used as estimator of σ 2 ( j ) in (9). Table 1 presents the results of this estimation for the three graph theoretical statistics. The numbers in columns  ̃ μ d , for Mn and U 1 n , are the ones plotted in Figs. 2 and 3. We can see in the  ̃ μ d values, for the three statistics in this table, a nearly linear growth of the means. On the other hand, the curse of dimensionality manifests itself, in Table 1, in that the standard deviations of the statistics tend to grow with dimension, making it more difficult to distinguish between consecutive dimensions when they are larger.

To evaluate the performance of the graph theoretic methods proposed, a Monte Carlo comparison was carried out, in which we included the recently developed nearest-neighbor methods described in Section 1 and a set of manifolds with dimensions m varying from 2 to 9, most of which have appeared in similar studies in the literature:


<!-- p:8 -->


Table 2 Estimated MSE for Costa et al. estimator.

| Data set   |   n = 250 | n = 250   |   n = 500 | n = 500   |   n = 1000 | n = 1000   |
|------------|-----------|-----------|-----------|-----------|------------|------------|
| S 3        |      0.62 | (1)       |     0.665 | (1)       |      0.659 | (1)        |
| S 6        |     7.311 | (9)       |     7.096 | (9)       |       6.97 | (9)        |
| S 9        |    25.703 | (25)      |    24.298 | (25)      |     24.205 | (25)       |
| P 3        |      0.62 | (1)       |     1.001 | (1)       |       0.85 | (1)        |
| P 6        |    13.838 | (16)      |    11.445 | (9.467)   |     10.032 | (9)        |
| P 9        |     46.98 | (49)      |    40.186 | (37.733)  |     35.147 | (36)       |
| Swiss Roll |     0.059 | (0)       |     0.053 | (0)       |      0.047 | (0)        |
| Möbius     |     0.043 | (0)       |     0.099 | (0)       |      0.147 | (0)        |

Table 3 Estimated MSE for Farahmand et al. estimator.

| Data set   |   n = 250 | n = 250   |   n = 500 | n = 500   |   n = 1000 | n = 1000   |
|------------|-----------|-----------|-----------|-----------|------------|------------|
| S 3        |     0.298 | (0.5)     |     0.287 | (0.567)   |      0.286 | (0.633)    |
| S 6        |     0.331 | (0.5)     |      0.35 | (0.667)   |      0.566 | (1)        |
| S 9        |     0.085 | (0.067)   |     0.098 | (0.1)     |      0.105 | (0.1)      |
| P 3        |     0.298 | (0.5)     |     0.048 | (0)       |      0.086 | (0)        |
| P 6        |     1.904 | (1.5)     |     0.871 | (1)       |      0.311 | (0.733)    |
| P 9        |    16.041 | (16.3)    |      8.97 | (9)       |      5.245 | (4.167)    |
| Swiss Roll |     1.025 | (1)       |     1.017 | (1)       |      0.722 | (1)        |
| Möbius     |     0.624 | (1)       |     0.224 | (0.333)   |      0.122 | (0)        |

- (i) Möbius band data (as considered in [7]). This is a 2-dimensional manifold data set produced as follows: For U ∼ Unif ( - 1 / 2 , 1 / 2 ) and V ∼ Unif ( 0 , 2 π) , let the coordinates of X ∈ R 3 begivenby X 1 = ( 1 + U cos ( 5 V )) cos ( V ), X 2 = ( 1 + U cos ( 5 V )) sin ( V ) and X 3 = U sin ( 5 V ) .
- (ii) The ''Swiss Roll'' data, introduced in Tenenbaum, de Silva and Langford [30] and considered in several other articles, is another 2-dimensional manifold data set that is obtained by generating first a bivariate mixture of Gaussian sample, and then ''twisting'' the sample into R 3 by applying the following transformation to each bivariate datum ( Z 1 , Z 2 ) : X 1 = Z 1 cos ( Z 1 ), X 2 = Z 2 and X 3 = Z 1 sin ( Z 1 ) .
- (iii) Uniform data in the unit sphere S m . This data was generated for m = 3 , 6 and 9.
- (iv) Random data in an m -dimensional paraboloid, P m . These data points fall in the manifold

$$x _ { m + 1 } = x _ { 1 } ^ { 2 } +$$

$$x _ { m + 1 } = x _ { 1 } ^ { 2 } + \dots + x _ { m } ^ { 2 }$$

and are obtained by generating first ( X 1 , . . . , Xm ) ∈ R m with the Multivariate Burr distribution with parameter α = 1 (see [13, Chapter 9]). This means that, for i ≤ m , Xi = ( 1 + Ei / E 0 ) - 1 , where E 0 , E 1 , . . . , Em are i.i.d. exp(1) variables. After the coordinates ( X 1 , . . . , Xm ) are generated, Xm + 1 is computed according to (13). These data were generated for m = 3 , 6 and 9. The idea in considering the paraboloid data is to have, in the larger dimensions considered, an example with non-constant curvature, in contrast to the unit sphere data.

As in [7], after generating the manifold samples just described, redundant coordinates were added to the data by adding the coordinates sin ( Xi ) and X 2 i , for each coordinate Xi . In this manner, although the data actually live in a manifold of dimension m , the dimension identification procedures shall be implemented with data in R 3 ( m + 1 ) .

The nearest neighbor methods considered in this comparison, with their parameters, are the following:

LB: The statistic of Levina and Bickel, (1), with k = 5.

CGH: Costa, Girotra and Hero's method, with γ = 1 , k = 5, Q = 3 , p 1 = ⌈ n / 4 ⌉ , p 2 = ⌈ n / 2 ⌉ , p 3 = n and N = 0 . 1 n . See the explanation of the parameters in the lines following (2).

FSA: The estimator of Farahmand, Szepesvári and Audibert, (4), with k = 10.

SRH: Sricharan, Raich and Hero's estimator, (5), with k 1 = 5 , k 2 = 10 , N = ⌊ n / 5 ⌋ and M = n - N .

These nearest neighbor methods are compared to the approximate Bayesian classifiers corresponding to the graph theoretic procedures proposed here. The Bayesian classifiers are set up with the estimated mean and variance values given in Table 1 and the choice of parameters made for that table. For comparison purposes, for each method of classification, each data type, each value of the intrinsic dimension, m , and each sample size, n = 250 , 500 and 1000, 30 samples were generated and presented to the dimension estimator. For each estimator, the final value is obtained by rounding, to the next integer, a value produced by the estimator formula.

Tables 2-8 present the mean squared errors (MSEs) for the different estimators, before and after rounding. The value in parenthesis is the MSE for the rounded (integer) value of the estimator. In these MSE tables, we observe the following: The estimator of Costa, Girotra and Hero (CGH) presents a very good behavior in identification of dimension 2, in which case the MSE for the rounded value of the estimator is 0 for both 2-dimensional data distributions and all sample sizes, but its performance deteriorates rapidly with increasing dimension, and for m = 9 the estimator presents a bias of about


<!-- p:9 -->


Table 4 Estimated MSE for Levina-Bickel estimator.

| Data set   |   n = 250 | n = 250   |   n = 500 | n = 500   |   n = 1000 | n = 1000   |
|------------|-----------|-----------|-----------|-----------|------------|------------|
| S 3        |     0.016 | (0)       |     0.009 | (0)       |      0.007 | (0)        |
| S 6        |     0.115 | (0.133)   |      0.09 | (0.033)   |      0.037 | (0)        |
| S 9        |     1.056 | (1.067)   |     0.612 | (0.767)   |      0.468 | (0.767)    |
| P 3        |     0.016 | (0)       |     0.033 | (0)       |      0.021 | (0)        |
| P 6        |     2.362 | (2.8)     |     1.634 | (1)       |      1.101 | (1)        |
| P 9        |    13.007 | (13.433)  |     9.019 | (8.833)   |      6.681 | (7.667)    |
| Swiss Roll |     0.277 | (0.533)   |     0.261 | (0.333)   |      0.285 | (0.367)    |
| Möbius     |     0.009 | (0)       |     0.004 | (0)       |      0.002 | (0)        |

Table 5 Estimated MSE for Sricharan et al. estimator.

| Data set   |   n = 250 |          |   n = 500 |          |   n = 1000 |          |
|------------|-----------|----------|-----------|----------|------------|----------|
| S 3        |     0.112 | (0.167)  |     0.096 | (0.1)    |      0.071 | (0)      |
| S 6        |     0.154 | (0.233)  |      0.19 | (0.333)  |       0.15 | (0.167)  |
| S 9        |     0.401 | (0.567)  |     0.286 | (0.367)  |      0.164 | (0.133)  |
| P 3        |     0.112 | (0.167)  |     0.037 | (0.033)  |      0.012 | (0)      |
| P 6        |     5.317 | (4.967)  |     2.987 | (3.3)    |      1.592 | (1.3)    |
| P 9        |    29.097 | (28.733) |    18.592 | (18.167) |     11.464 | (10.867) |
| Swiss Roll |     0.184 | (0.3)    |     0.144 | (0.167)  |      0.123 | (0.033)  |
| Möbius     |     0.297 | (0.5)    |     0.095 | (0.067)  |      0.039 | (0)      |

Table 6 Estimated MSE for reach estimator, r 2 , 4 .

| Data set   |   n = 250 | n = 250   |   n = 500 | n = 500   |   n = 1000 | n = 1000   |
|------------|-----------|-----------|-----------|-----------|------------|------------|
| S 3        |     0.003 | (0)       |     0.009 | (0.033)   |          0 | (0)        |
| S 6        |     0.672 | (0.867)   |     0.454 | (0.633)   |      0.036 | (0.033)    |
| S 9        |     6.558 | (6.667)   |     4.049 | (4)       |      3.722 | (4)        |
| P 3        |     0.003 | (0)       |         0 | (0)       |          0 | (0)        |
| P 6        |     3.734 | (3.767)   |     1.075 | (1.1)     |      0.122 | (0.2)      |
| P 9        |    26.792 | (26.467)  |    13.906 | (14.367)  |      4.324 | (4.333)    |
| Swiss Roll |      0.31 | (0.333)   |     0.166 | (0.2)     |      0.064 | (0.067)    |
| Möbius     |     0.098 | (0.133)   |         0 | (0)       |          0 | (0)        |

Table 7 Estimated MSE for estimator Mn .

| Data set   |   n = 250 | n = 250   |   n = 500 | n = 500   |   n = 1000 | n = 1000   |
|------------|-----------|-----------|-----------|-----------|------------|------------|
| S 3        |     0.186 | (0.267)   |     0.015 | (0.033)   |      0.001 | (0)        |
| S 6        |     2.284 | (2.333)   |     1.323 | (1.4)     |      0.801 | (0.967)    |
| S 9        |    12.571 | (12.767)  |     9.827 | (10.2)    |      7.577 | (8.367)    |
| P 3        |     0.186 | (0.267)   |     0.014 | (0)       |          0 | (0)        |
| P 6        |     1.107 | (1.167)   |     0.435 | (0.6)     |      0.388 | (0.467)    |
| P 9        |     5.393 | (5.567)   |       1.2 | (1.467)   |      0.542 | (0.567)    |
| Swiss Roll |     0.078 | (0.1)     |     0.042 | (0.067)   |          0 | (0)        |
| Möbius     |     0.186 | (0.2)     |         0 | (0)       |          0 | (0)        |

Table 8 Estimated MSE for mutual neighbors estimator, U 1 .

| Data set   |   n = 250 |         |   n = 500 |          |   n = 1000 |         |
|------------|-----------|---------|-----------|----------|------------|---------|
| S 3        |     0.709 | (0.667) |     0.128 | (0.167)  |      0.164 | (0.2)   |
| S 6        |     2.388 | (2.4)   |     2.231 | (2.033)  |      1.728 | (1.8)   |
| S 9        |    10.005 | (9.967) |    11.877 | (12.067) |     10.906 | (10.8)  |
| P 3        |     0.709 | (0.667) |     0.371 | (0.367)  |      0.235 | (0.333) |
| P 6        |      1.09 | (1.067) |     0.579 | (0.633)  |      0.365 | (0.567) |
| P 9        |     4.293 | (4.733) |     3.185 | (3.4)    |      2.717 | (2.433) |
| Swiss Roll |     1.104 | (1.233) |     0.461 | (0.5)    |      0.146 | (0.167) |
| Möbius     |     1.398 | (1.5)   |     0.241 | (0.333)  |      0.058 | (0.1)   |

n

5 units for the sphere data and even more bias for the paraboloid data. This, together with the fact that this estimator is, computationally, by far the most expensive of all considered here, due to the intensive resampling required, makes it very difficult to recommend its use. The FSA estimator has a very good performance for the unit sphere data, even for the larger value of m , while its performance deteriorates with dimension for the P m data, reaching a standard error of about 4 units for the P 9 data for n = 250, although we observe, as well, that this performance tends to improve with sample size. The FSA estimator is not as good on the 2-dimensional distributions considered, presenting an error of about one unit on the Swiss Roll data for all sample sizes. For the distributions considered, the LB estimator has, in general, a similar performance to FSA, being superior for the S 3 and Möbius band data, for which LB is practically perfect, and being inferior to FSA for the S 9 data. The estimator of Sricharan et al. presents a behavior similar to those of the FSA and LB statistics, with a tendency to perform slightly below (with a larger MSE) the LB statistic across the table. The reach statistic, for the 2-dimensional manifolds, performs fairly well, better than FSA and SRH, and similar to LB. With respect to S m and P m , r j , k does well for m = 3, but its performance deteriorates with growing m , reaching a standard error of about 2.5 units for S 9 and of about 5 units for P 9 for sample size n = 250, but we observe that these errors tend to improve rapidly with sample size in both cases ( S 9 and P 9). For the 2-dimensional manifolds, the Mn estimator displays a good behavior, being better than FSA and SRH and similar in mean squared error to LB and r j , k . For the unit sphere data, Mn performance is inferior to that of all the nearest neighbor methods (except CGH), while for the P m data, Mn displays consistently, the smallest errors of all the methods considered, suggesting that it might be a very good method in the case of non-constant curvature manifolds. The Mutual Neighbor method, for the 2-dimensional manifolds, displays a better behavior than the FSA statistic, but is inferior to the other nearest neighbor methods, although U k n 's performance improves rapidly with sample size in this case. For S m and P m , U k n 's offers a behavior similar to that of Mn , being inferior to the nearest neighbor methods (except CGH) for the unit sphere data, while being clearly better than those methods for the paraboloid data.


<!-- p:10 -->


A conclusion that can be extracted from this comparison is that no clear winner emerges. It would appear that the graph theoretic methods could have a certain edge in the case of manifolds of non-constant curvature.

### 4. Limit theory for dimension estimators

In this section, we establish weak laws of large numbers, variance asymptotics, and central limit theorems for the statistics Mn and U k n , k ∈ N , as n → ∞ . The corresponding theory for r j , k follows the pattern of that for U k n , as explained in the remarks after Theorem 1. To obtain the limit theory for U k n , we shall slightly extend some of the general results of Penrose and Yukich [22].

#### 4.1. Statement of results

For all x ∈ R d , k = 1 , 2 , . . . and all locally finite point sets X ⊂ R d , we put as in Section 1

ck ( x , X ) := card { y ∈ X : x is one of the k nearest neighbors of y in X } .

Let

$$\zeta _ { k } ( x , x ) \coloneqq \begin{pmatrix} c _ { k } ( x , x ) \\ 2 \end{pmatrix} .$$

Recalling that X n := { Xi } n i = 1 , we have U k n = n - 1  n i = 1 ζ k ( Xi , X n ) .

As in [22], let M := M ( m , d ) be the class of all m -dimensional C 1 submanifolds of R d which are also closed subsets of R d . Given M ∈ M , let P c ( M ) denote the class of probability density functions κ on M whose support K (κ) is a compact C 1 submanifold-with-boundary of M , and which are bounded away from zero and infinity on their support.

Let H denote a homogeneous rate one Poisson point process on R m . Say that a functional ξ defined on pairs ( x , X ) , with x ∈ R m and X locally finite in R m , is translation invariant if ξ( x , X ) = ξ( x + y , X + y ) for all y ∈ R m . Letting 0 denote a point at the origin of R m , we put, for all m ∈ N ,

$$V ^ { \xi } ( m ) \colon = \mathbb { E } [ \xi ( 0 , \mathcal { H } ) ^ { 2 } ] + \int _ { \mathbb { R } ^ { m } } [ \mathbb { E } \xi ( 0 , \mathcal { H } \cup \{ z \} ) \xi ( z , \mathcal { H } \cup \{ 0 \} ) - ( \mathbb { E } \xi ( 0 , \mathcal { H } ) ) ^ { 2 } ] d z$$

and

$$\Delta ^ { \xi } ( m ) \colon = \mathbb { E } \xi ( 0 , \mathcal { H } ) + \int _ { \mathbb { R } ^ { m } } \mathbb { E } [ \xi ( 0 , \mathcal { H } \cup \{ z \} ) - \xi ( 0 , \mathcal { H } ) ] d z .$$

For all κ ∈ P c ( M ) and ξ we define

$$\sigma ^ { 2 } ( \xi , \kappa ) \coloneqq \int _ { \mathcal { M } } V ^ { \xi } ( \kappa ( x ) ) \kappa ( x ) d x - \left ( \int _ { \mathcal { M } } \Delta ^ { \xi } ( \kappa ( x ) ) \kappa ( x ) d x \right ) ^ { 2 } ,$$

provided that both integrals in (17) exist and are finite. Put

$$\sigma ^ { 2 } ( \xi ) \colon = V ^ { \xi } ( m ) - ( \Delta ^ { \xi } ( m ) ) ^ { 2 } .$$


<!-- p:11 -->


The scalar V ξ ( m ) may be interpreted as the mean pair correlation function for the functional ξ on homogeneous Poisson points H whereas we may view ∆ ξ ( m ) as an expected ''add-one cost''.

We have the following limit theory for the dimension estimator U k n ; N ( 0 , σ 2 ) denotes a mean zero normal random variable with variance σ 2 .

Theorem 1. Let M ∈ M and let κ ∈ P c ( M ) . If Xi , i ≥ 1 , are i.i.d. with density κ , then, for all k ∈ N , we have in L 2 and almost surely,

$$\lim _ { n \to \infty } U _ { n } ^ { k } = \mathbb { E } _ { k } ( 0 , \mathcal { H } ) .$$

If, additionally, κ is a.e. continuous, then

$$\lim _ { n \to \infty } n \, V a r [ U _ { n } ^ { k } ] \coloneqq \sigma ^ { 2 } ( \zeta _ { k } ) \colon = V ^ { \zeta _ { k } } ( m ) - ( \Delta ^ { \zeta _ { k } } ( m ) ) ^ { 2 } ,$$

and as n →∞ ,

$$n ^ { 1 / 2 } ( U _ { n } ^ { k } - \mathbb { E } U _ { n } ^ { k } ) \stackrel { \mathcal { D } } { \longrightarrow } N ( 0 , \sigma ^ { 2 } ( \zeta _ { k } ) ) .$$

Remarks. (i) The limits in (18) and (19) are independent of the density κ of the underlying point set. (ii) The proof of Theorem 1 shows that the statistic r j , k also satisfies the limit theory of Theorem 1, with ζ k replaced by the functional

r j , k ( x , X ) := card { y ∈ X : y ̸= x , y is reached in l steps from x ; l ≤ j } .

(iii) Positivity of σ 2 (ζ k ) and σ 2 ( r j , k ) follows as in the proof of the last part of Theorem 2.1 of [19].

For all x ∈ R d and all locally finite point sets X ⊂ R d , define the functional

$$\varphi ( x , \mathcal { X } ) \coloneqq \left ( \deg _ { M S T ( x ) } \right ) ^ { 2 } ,$$

where we recall that deg MST ( X ) ( x ) denotes the degree of the node x in the graph of the minimal spanning tree on X . We have Mn := M ( X n ) := n - 1  n i = 1 φ( Xi , X n ) .

Theorem 2. Assume that Xi , i ≥ 1 , have density κ on R m . Then in L 2

$$\lim _ { n \to \infty } M _ { n } = \mathbb { E } \varphi ( 0 , \mathcal { H } ) .$$

If the density κ is uniform on [- 1 , 1 ] m then there is a σ 2 ( m ) , such that

$$\lim _ { n \to \infty } n \, V a r [ M _ { n } ] = o ^ { 2 } ( m )$$

and, as n →∞ ,

$$n ^ { 1 / 2 } ( M _ { n } - \mathbb { E } M _ { n } ) \stackrel { \varnothing } { \longrightarrow } N ( 0 , \sigma ^ { 2 } ( m ) ) .$$

Remark. If M ∈ M and κ ∈ P c ( M ) , then no limiting theory is currently available for Mn , but we conjecture that the limit theory of Theorem 1 applies to Mn , with ζ k replaced by φ . The method of proof shows that Theorem 2 also holds if the data X n belongs to any affine subspace of R d .

#### 4.2. A general result

Wefirst slightly extend some general results of [22]. This goes as follows. For all r ∈ ( 0 , ∞ ) and x ∈ R d , let Br ( x ) be the Euclidean ball of radius r centered at x . Let F ⊂ R l , l ∈ N , be a locally finite set. For all x ∈ R l , j ∈ N , we let N j ( x , F ) be the set of points in F having x as one of their j nearest neighbors in { x } ∪ F . Let nj ( x , F ) be the maximum of the distances between x and the elements of N j ( x , F ) , i.e.,

$$n _ { j } ( x , F ) \colon = \max \{ | x - w | \, \colon w \in \mathcal { N } _ { j } ( x , F ) \} .$$

If N j ( x , F ) = ∅ , then put nj ( x , F ) := diam ( F ) .

Given k ∈ N , let Ξ( k ) be the class of translation and rotation invariant functionals ξ such that (i) for all x , X with card ( X \ { x } ) ≥ k , we have

$$\xi ( x , \mathcal { X } ) = \xi ( x , \mathcal { X } \cap B _ { n _ { k } ( x , \mathcal { X } ) } ( x ) )$$


<!-- p:12 -->


and (ii) for all n , Lebesgue-almost every ( x 1 , . . . , xn ) ∈ ( R m ) n (with R m embedded in R d ) is at a continuity point of the mapping from ( R d ) n → R , given by

$$( x _ { 1 } , \dots , x _ { n } ) \mapsto \xi ( 0 , \{ x _ { 1 } , \dots , x _ { n } \} ) .$$

The functional ζ k , defined at (14), belongs to the class Ξ( k ) . Indeed, the continuity criteria (ii) hold when the points ( x 1 , . . . , xn ) have distinct interpoint distances.

Next, for x ∈ R l and j ∈ { 0 , 1 , 2 , . . . } , let Nj ( x , F ) be the Euclidean distance between x and its j th nearest neighbor in F \ { x } , i.e.

$$N _ { j } ( x , F ) \coloneqq \inf \{ r \geq 0 \colon \text {card} ( F \cap B _ { r } ( x ) \ \{ x \} ) \geq j \}$$

with the infimum of the empty set taken to be +∞ . In particular, N 0 ( x , F ) = 0. Given k ∈ Z , let Ξ 0 ( k ) be the class of translation and rotation invariant functionals, ξ , such that (i) for all x , X with card ( X \ { x } ) ≥ k , we have

$$\xi ( x , \mathcal { X } ) = \xi ( x , \mathcal { X } \cap B _ { N _ { k } ( x , \mathcal { X } ) } ( x ) )$$

and (ii) for all n , Lebesgue-almost every ( x 1 , . . . , xn ) ∈ ( R m ) n (with R m embedded in R d ) is at a continuity point of the mapping from ( R d ) n → R , given by

$$( x _ { 1 } , \dots , x _ { n } ) \mapsto \xi ( 0 , \{ x _ { 1 } , \dots , x _ { n } \} ) .$$

When ξ ∈ Ξ 0 ( k ), M ∈ M , and κ ∈ P c ( M ) , then under moment conditions on ξ , [22] establishes weak laws of large numbers, variance asymptotics, and central limit theorems for

$$H _ { n } ^ { \xi } ( X _ { n } ) \colon = \sum _ { i = 1 } ^ { n } \xi _ { n } ( X _ { i } , X _ { n } ) ,$$

where ξ n ( x , X ) := ξ( n 1 / d x , n 1 / d X ) .

Here we shall show that if ξ ∈ Ξ( k ) , then a similar limit theory holds for H ξ n ( X n ) . Given i = 1 , 2 , 3, recall that S i is the collection of all subsets of K (κ) of cardinality at most i , including the empty set. Consider the following moment conditions on ξ :

$$\sup _ { n } \mathbb { E } | \xi _ { n } ( X _ { 1 } , X _ { n } ) | ^ { p } < \infty ,$$

$$\sup _ { n \geq 1 , x \in \mathcal { K } ( x ) , A \in \mathfrak { s } _ { 3 } \left ( n / 2 \right ) \leq \ell \leq ( 3 n / 2 ) } \mathbb { E } | \xi _ { n } ( x , X _ { \ell } \cup \mathcal { A } ) | ^ { p } \, < \infty$$

and

$$\sup _ { \lambda \geq 1 , x \in \mathcal { K } ( x ) , A \in \mathcal { S } _ { 1 } } \mathbb { E } | \xi _ { \lambda } ( x , \mathcal { P } _ { \lambda } \cup \mathcal { A } ) | ^ { p } < \infty .$$

Theorem 3 ( Limit Theory for H ξ n ( X n ), ξ ∈ Ξ( k ) ) . Let M ∈ M , κ ∈ P c ( M ), k ∈ N , and put q = 1 or q = 2 . Let ξ ∈ Ξ( k ) and suppose there exists p &gt; q such that (26) holds. Then as n →∞ we have L q convergence

$$n ^ { - 1 } H _ { n } ^ { \xi } ( X _ { n } ) \rightarrow \int _ { \mathcal { M } } \mathbb { E } [ \xi ( 0 , \mathcal { H } _ { \kappa ( x ) } ) ] \kappa ( x ) d x .$$

If also (27) holds for some p &gt; 5 , then (29) holds a.s. If, additionally, κ is a.e. continuous, and if ξ satisfies (27) and (28) for some p &gt; 2 , then σ 2 (ξ, κ) &lt; ∞ and

$$\lim _ { n \to \infty } n ^ { - 1 } \, V a r [ H ^ { \xi } ( X _ { n } ) ] = \sigma ^ { 2 } ( \xi , \kappa )$$

and as n →∞ ,

$$n ^ { - 1 / 2 } ( H _ { n } ^ { \xi } ( \mathcal { X } _ { n } ) - \mathbb { E } H _ { n } ^ { \xi } ( \mathcal { X } _ { n } ) ) \stackrel { \mathcal { D } } { \longrightarrow } N ( 0 , \sigma ^ { 2 } ( \xi , \kappa ) ) .$$

Remark. Wesay that ξ is homogeneous of order zero if, for all scalars a &gt; 0, we have ξ( x , X ) = ξ( ax , a X ) . In this case the constants in Theorem 3 simplify, since

$$\int _ { \mathcal { M } } \mathbb { E } [ \xi ( 0 , \mathcal { H } _ { \kappa ( x ) } ) ] \kappa ( x ) d x = \mathbb { E } [ \xi ( 0 , \mathcal { H } _ { 1 } ) ]$$

and σ 2 (ξ, κ) := σ 2 (ξ) := V ξ ( m ) - (∆ ξ ( m )) 2 . The functionals ζ k and φ are both homogeneous of order zero.


<!-- p:13 -->


Proof of Theorem 3. We first recall a definition (see Definition 5.1 in [22]). Recall that if ξ is continuous if for any linear F : R m → R d of full rank, for almost all z ∈ R m both F ( H ) and F ( H ∪{ z } ) lie a.s. at continuity points of ξ( 0 , · ) with respect to the topology T d in [22]. We first give some definitions, following closely [22]. Assume M ∈ M and κ ∈ P ( M ) are given, and recall K := K (κ) . Suppose k ∈ N is given, along with the density κ . For x ∈ K and locally finite X ⊂ K define

$$R _ { \lambda } ( x , \mathcal { X } ) \colon = \begin{cases} n _ { k } ( \lambda ^ { 1 / m } x , \lambda ^ { 1 / m } \mathcal { X } ) & \text {if card} ( \mathcal { X } \ \{ x \} ) \geq k \\ \lambda ^ { 1 / m } \text { diam} ( \mathcal { K } ) & \text {otherwise.} \end{cases}$$

Then R := R λ( x , X ) is a radius of stabilization for any ξ ∈ Ξ( k ) , in the following sense: for all finite A ⊂ ( K \ B λ - 1 / m R ( x )) , we have

$$\xi _ { \lambda } \left ( x , ( x \cap B _ { \lambda ^ { - 1 / m } _ { R } } ( x ) ) \cup \mathcal { A } \right ) = \xi _ { \lambda } \left ( x , \mathcal { X } \cap B _ { \lambda ^ { - 1 / m } _ { R } } ( x ) \right ) .$$

Recall that X n := { Xi } n i = 1 and for λ ∈ [ 1 , ∞ ) , let P λ denote the Poisson point process on M having intensity density λκ( · ) , that is E P λ( dx ) = λκ( x ) dx . Given ε &gt; 0 and t &gt; 0, we define the tail probabilities for R λ denoted by τ( t ) and τε ( t ) , for Poisson input P λ and binomial input X n , respectively, as follows:

$$\tau ( t ) \coloneqq & \sup _ { \lambda \geq 1 } \sup _ { x \in \mathcal { X } } P [ R _ { \lambda } ( x , \mathcal { P } _ { \lambda } ) > t ] \\ \tau _ { \epsilon } ( t ) \coloneqq & \sup _ { \lambda \geq 1 , n \in \mathbb { N } ( ( 1 - \epsilon ) \lambda , ( 1 + \epsilon ) \lambda ) , \ \mathcal { A } \in \mathcal { B } _ { 2 } } \ \text {ess} \sup _ { x \in \mathcal { X } } P [ R _ { \lambda } ( x , \mathcal { X } _ { n } \cup \mathcal { A } ) > t ]$$

where the ess sup denotes essential supremum with respect to the measure κ( x ) dx .

Definition 1. Given k , we say that all ξ ∈ Ξ( k ) are exponentially stabilizing for κ if lim sup t →∞ t - 1 log τ( t ) &lt; 0 . We say that all ξ ∈ Ξ( k ) are binomially exponentially stabilizing for κ if there exists ε &gt; 0 such that lim sup t →∞ t - 1 log τε ( t ) &lt; 0 .

To prove Theorem 3, by the remark at the end of Section 6 of [22], it suffices to show that ξ ∈ Ξ( k ) is continuous, exponentially stabilizing, and binomially exponentially stabilizing. We prove continuity by following verbatim the proof of Lemma 6.1 in [22], replacing Nk ( 0 , F ( H )) in that proof by nk ( 0 , F ( H )) .

We now show that ξ is exponentially stabilizing and binomially exponentially stabilizing in the sense of Definition 1. Let C 0 1 , . . . , C 0 J be a finite collection of open cones in R d , each with vertex at the origin and angular radius π/ 6, so that R d \ { 0 } = ∪ J j = 1 C 0 j . For 1 ≤ j ≤ J , let Cj be the translate of C 0 j with its vertex at x . Put Kj := Cj ∩ M .

Elementary geometry shows that if card ( Kj ∩ Bt ( x ) ∩ P λ) ≥ k + 1 for all 1 ≤ j ≤ J , then points outside Bt ( x ) will not affect the value of ξ( x , P λ) . Let T λ( x , P λ) be the minimum ρ such that each Kj ∩ B λ - 1 / m ρ ( x ) contains at least k + 1 points from P λ , that is

$$T _ { \lambda } ( x , \mathcal { P } _ { \lambda } ) \coloneqq \begin{cases} \inf \{ \rho > 0 \colon \text { card} ( K _ { j } \cap B _ { \lambda ^ { - 1 / m } \rho } ( x ) \cap \mathcal { P } _ { \lambda } ) \geq k + 1 \} & \text { if } \text { card} ( K _ { j } \cap \mathcal { P } _ { \lambda } ) > k \\ \lambda ^ { 1 / m } \text { dice} ( \mathcal { K } ) & \text { otherwise.} \end{cases}$$

Then R λ( x , P λ) ≤ T λ( x , P λ) and so T λ( x , P λ) is a radius of stabilization for ξ . Also, T λ( x , P λ) exceeds t only when there is a j , 1 ≤ j ≤ J , such that

$$c a r d ( K _ { j } \cap B _ { \lambda ^ { - 1 / m _ { t } } } ( x ) \cap \mathcal { P } _ { \lambda } ) \leq k .$$

The number of points in Kj ∩ B λ - 1 / m t ( x ) ∩ P λ is Poisson distributed with parameter b ( t ) := b ( t , x , λ) equal to the λκ measure of B λ - 1 / m t ( x ) ∩ M . By Lemma 4.3 in [22], there is a constant C 1 ∈ ( 0 , ∞ ) such that, uniformly in λ ∈ [ 1 , ∞ ), x ∈ K , and t ∈ ( 0 , λ 1 / m diam ( K )) , we have b ( t ) ≥ C - 1 1 t m .

By bounds for the Poisson distribution (e.g. Lemma 1.2 of [18]), there is a constant C 2 ∈ ( 0 , ∞ ) such that for t ∈ ( 0 , λ 1 / m diam ( K )) we have uniformly in j that

$$P [ \text {card} ( K _ { j } \cap B _ { \lambda ^ { - 1 / m } t } ( x ) \cap \mathcal { P } _ { \lambda } ) \leq k ] = P [ \text {Pois} ( b ( t ) ) \leq k ] \leq k C _ { 2 } \exp ( - C _ { 2 } ^ { - 1 } t ^ { m } ) .$$

Thus for t ∈ ( 0 , λ 1 / m diam ( K )) we have

$$P [ T _ { \lambda } ( x , \mathcal { P } _ { \lambda } ) > t ] \leq C _ { 3 } ( k ) \exp ( - C _ { 2 } ^ { - 1 } t ^ { m } ) .$$

For t ∈ (λ 1 / m diam ( K ), ∞ ) this also holds since P [ T λ( x , P λ) &gt; t ] = 0in this case. This shows that ξ stabilizes exponentially fast on Poisson input. Modifications of these arguments give that ξ stabilizes exponentially fast on binomial input. This completes the proof of Theorem 3. □

#### 4.3. Proof of Theorem 1

Weshall deduce Theorem 1 from Theorem 3. Since U k n = n - 1  n i = 1 ζ k ( Xi , { Xi } n i = 1 ) , it suffices to show that ζ k satisfies the conditions of Theorem 3.

Note that ζ k ∈ Ξ( k ) and so it only remains to show that ζ k satisfies the moment conditions of Theorem 3. However this follows since ζ k is deterministically bounded. Indeed, a given point in R d is the nearest neighbor of at most a finite number of other points in R d (see Lemma 8.4 of [31]). For all k ∈ N there is thus a constant Ck such that, for all x , X we have ck ( x , X ) ≤ Ck , that is ζ k ( · , · ) ≤ C 2 k / 2 . Applying Theorem 3 and recalling that ζ k is homogeneous of order zero, we obtain Theorem 1 as desired. □


<!-- p:14 -->


#### 4.4. Proof of Theorem 2

The limit (22) is an immediate consequence of the boundedness of φ (as noted on pp. 811-812 of Steele, Shepp and Eddy [29]), the fact that φ is stabilizing as shown in Lemma 2.1 of [20], the general weak law of large numbers for sums of stabilizing functionals, as given by Theorem 2.1 of [20], and the fact that φ( x , X ) is homogeneous of order zero, and thus (30) applies.

To prove (23) and (24), we proceed as follows. The proof of (24) follows from Lee [16] or [19]. We provide the details as follows. Consider the functional

$$H ^ { \varphi } ( \mathcal { X } ) \colon = \sum _ { x \in \mathcal { X } } \varphi ( x , \mathcal { X } ) .$$

It will suffice to show that H φ satisfies the conditions of Corollary 2.1 of [19]. Since φ is bounded it follows that H φ ( X ) ≤ C card ( X ) and, therefore, H φ is polynomially bounded, that is to say there exists a constant β ∈ ( 0 , ∞ ) such that, for all finite sets X ⊂ R d , we have

$$H ^ { \varphi } ( \mathcal { X } ) \leq \beta ( \text {diam} ( \mathcal { X } ) + \text {card} ( \mathcal { X } ) ) ^ { \beta } .$$

Put ∆( X ) := H φ ( X ∪ { 0 } ) - H φ ( X ) . If H λ denotes a homogeneous Poisson point process of intensity λ on R d , then there exist a.s. finite random variables S and ∆( ∞ ) such that, with probability one,

$$\Delta ( \mathcal { H } _ { \lambda } \cap B _ { S } ( 0 ) \cup \mathcal { A } ) = \Delta ( \infty )$$

for all finite A ⊂ R d \ BS ( 0 ) . This condition, known as strong stabilization of H φ (cf. Definition 2.1 of [19]), follows from Kesten and Lee [15] and Lee [16]. Actually Kesten and Lee [15] show that the above condition holds if H MST ( X ) is the total edge length of the minimal spanning tree on X , but the random variable S which works for H MST will also work for H φ .

Finally, if X m is the point process consisting of m i.i.d. uniform random variables on [- 1 , 1 ] d , then straightforward modifications of Kesten and Lee [15] as well as Lee [16] show that

$$\sup _ { n \ m \in [ \lambda / 2 , 3 \lambda / 2 ] } \mathbb { E } [ \Delta ( X _ { m } ) ^ { 4 } ] < \infty ,$$

and so H φ satisfies the uniform bounded moment condition of [19]. Thus, H φ satisfies all of the conditions of Corollary 2.1 in [19] and so (23) and (24) follow. □

#### 4.5. Consistency of a dimension identification procedure

To prove that the procedures for intrinsic dimension identification based on r j , k and U k n are consistent, we assume that the limiting constants in the corresponding LLNs are different, for different dimensions in the range considered. Actually, our simulations support the hypothesis that these constants are increasing with dimension. As in Section 2, let Sn := Sn ( X n ) represent one of our statistics, r j , k or U k n , or another graph theoretic statistic satisfying the same conditions. Let X n denote an i.i.d. data set obtained from a density κ with support on an m -dimensional compact submanifold-with-boundary of R d and assume that κ is bounded away from zero and infinity on its support. Assume that, for this kind of data Sn satisfies a SLLN: Sn → μ( m ) in L 2 , and almost surely, where the limit depends only on m , and the μ( m ) values are different for the different m ∈ F , F being a finite set. Assume, as well, that conditions (9) and (10) of Section 2 hold. Suppose that the parameter estimation for the approximate Bayesian dimension identification procedure based on Sn , is made as described in Section 2, using L samples of size n from the Uniform distribution on the unit cube for each j ∈ F and that the value of the graph theoretic statistic, Sn ′ is computed on a new data set X n ′ that satisfies the conditions for manifold data given above. Then, we have the following.

Theorem 4. Let m ∗ and  ̃ mdenote, respectively, the actual intrinsic dimension of X n ′ and its estimator, as given by (12) . Under the conditions stated above,  ̃ m -→ m ∗ , almost surely, as L , n , n ′ →∞ .

Proof of Theorem 4. In view of formula (12), it suffices to show that, for each j ∈ F , j ̸= m ∗ ,

$$\frac { \tilde { f } _ { j } ( S _ { n ^ { \prime } } ) } { \tilde { f } _ { m ^ { * } } ( S _ { n ^ { \prime } } ) } \to 0 , \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \$$

Now, for each dimension j ∈ F , the estimator,  ̃ μ( j ) , is converging a.s. to E ( Sn ) for j -dimensional unit cube data, as L →∞ . Then, using the L 2 convergence of Sn to μ( j ) , we have that  ̃ μ( j ) → μ( j ) , a.s., as L , n →∞ . On the other hand, both  ̃ σ 2 ( j ) and


<!-- p:15 -->


 ̃ σ 2 ( m ∗ ) are a.s. consistent for their estimated parameters, as n , L →∞ and then, the ratio  ̃ σ 2 ( j )/  ̃ σ 2 ( m ∗ ) will almost surely, be bounded away from zero and ∞ for large L and n . Applying the definition of  ̃ f j , we have

$$\frac { \tilde { f } _ { j } ( S _ { n ^ { \prime } } ) } { \tilde { f } _ { m ^ { * } } ( S _ { n ^ { \prime } } ) } = \frac { \tilde { \sigma } ( m ^ { * } ) } { \tilde { \sigma } ( j ) } \exp \left ( \frac { n ^ { \prime } } { 2 } \left [ \frac { ( S _ { n ^ { \prime } } - \tilde { \mu } ( m ^ { * } ) ) ^ { 2 } } { \tilde { \sigma } ^ { 2 } ( m ^ { * } ) } - \frac { ( S _ { n ^ { \prime } } - \tilde { \mu } ( j ) ) ^ { 2 } } { \tilde { \sigma } ^ { 2 } ( j ) } \right ] \right ) .$$

Using both the L 2 and almost sure convergence to the mean, we have that Sn ′ -  ̃ μ( m ∗ ) goes to zero, almost surely, as n , n ′ , L go to ∞ , while Sn ′ -  ̃ μ( j ) converges, almost surely, to a non-zero limit. It follows that the exponent in (32) diverges to -∞ , almost surely, establishing the result. □

Remarks. The hypotheses of Theorem 4 are met by both r j , k and U k n , and the result is valid for the procedures based on these statistics. The fact that n and n ′ do not need to be equal for the consistency of the procedure, partially answers the comment of Levina and Bickel [17] regarding the need of a different calibration for every sample size. It is clear, from the proof just given, that the rounding in formula (12) does not affect the consistency of the estimator. That is, Theorem 4 holds whether or not we use rounding in (12).

### Acknowledgment

The research of the third author was supported in part by NSF grant DMS-1106619.
