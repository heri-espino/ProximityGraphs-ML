---
id: "Brito-Quiroz-Yukich_2002_Graph-Theoretic-Dimension-Identification"
source_pdf: "../pdf/Brito-Quiroz-Yukich_2002_Graph-Theoretic-Dimension-Identification.pdf"
source_filename: "Brito-Quiroz-Yukich_2002_Graph-Theoretic-Dimension-Identification.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "excellent"
extraction_score: 100.0
visual_assets: "disabled"
references_file: "../references/Brito-Quiroz-Yukich_2002_Graph-Theoretic-Dimension-Identification.references.md"
---

<!-- p:1 -->

## Graph-Theoretic Procedures for Dimension Identification

María R. Brito and Adolfo J. Quiroz

Universidad Simón Bolivar, Caracas, Venezuela

and

J. E. Yukich 1

Lehigh University

Received September 17, 1999; published online November 13, 2001

We consider the problem of identifying the dimension in which a sample of data points lives, when only their interpoint distances are known. We study as a random variable the average ''reach'' of vertices in the k -nearest-neighbors graph associated to the interpoint distance matrix, and we show how this variable can be used to accurately (from a probabilistic viewpoint) identify the unknown dimension at low computational cost. We discuss results that serve as the theoretical foundation for the methodology proposed. We illustrate how our method can help in dimension reduction procedures. © 2001 Elsevier Science (USA)

AMS subject classifications: 60F15; 62H30; 65C60.

Key words and phrases: proximity data; multidimensional scaling; k -nearestneighbors graph; dimensionality reduction.

## 1. INTRODUCTION

Data consisting of an n×n matrix D of distances between individuals are usually referred to as dissimilarity or proximity data (see, for example, Chapter 3 in Krzanowski, 1996). This type of data arises in psychometric and several other contexts of applied statistics and usually the analyst is interested in finding a Euclidean representation of the data set, that is, a dimension d and a set of n points in R d , such that the Euclidean interpoint distances between the points are close to the entries in D . This problem is known as Multidimensional Scaling (MDS), (see Kruskal and Wish, 1978) and has received a good amount of attention in the literature (see Groenen, 1997).

1 Research supported in part by NSA Grant MDA904-97-1-0053.

<!-- p:2 -->


We will consider a graph theoretic tool that can be useful for the first step of the MDS problem, that is, the identification of an appropriate dimension d \ 1 where the data can be represented. Existing methods for the problem considered here mainly include the following. (i) Studying the eigenvalues of the ''centered inner product matrix'' associated to the classical solution of MDS (see section 14.2 in Mardia, Kent and Bibby, 1979). This approach is relatively expensive from the computational viewpoint, involving the eigenvalue decomposition of an n×n matrix associated to D . (ii) Minimization of Kruskal's STRESS function (Kruskal, 1964). This is even more computationally intensive than method (i), requiring the solution of the non-metric MDS problem for several values of the dimension. (iii) Statistical Inference based on maximum likelihood estimation (Ramsay, 1982). This approach has the advantage of offering statistical statements on the parameter of interest. Still, it can present numerical problems (see comment on page 294 of Ramsay, 1982) and its robustness, with respect to the model assumed, of i.i.d. lognormal errors added to the underlying interpoint distances, has not been established.

For the method discussed here, we show in Section 3 that it is asymptotically universal, in the sense that if the dissimilarity data correspond to the interpoint distances for an i.i.d. sample from some continuous density f , then, asymptotically, the correct dimension will be identified with high probability, regardless of the particular continuous density f .

In what follows we will assume that we are in the context of Theorem 3, that is, we have a matrix corresponding to the Euclidean interpoint distances for an i.i.d. sample X 1 , ..., X n coming from some probability distribution P on R d , d \ 1 , having (an unknown) continuous density f , and we want to estimate d . Our methodology does not provide classical statistical statements on the dimension, such as estimation intervals or sets of maximum a posteriori probability (although we can estimate probabilities of missclasification). Nevertheless, the output of our procedure can be useful as a relatively inexpensive initial guess, when the user wants to employ a different methodology to decide on the appropriate dimension.

Suppose the n×n matrix D=(d ij ) contains the (Euclidean) interpoint distances corresponding to the sample X 1 , ..., X n . We will assume throughout this paper that the interpoint distances are distinct. We will consider the k -nearest-neighbors graph, G k , which can be built from D , and which is defined here for the reader's convenience, although it has been frequently used in the statistical literature, mostly in clustering applications (see, for example, Brito, Chavez, Quiroz and Yukich (1997) and references therein). The definitions of basic graph-theoretic concepts such as node, vertex, edge, path, and degree are omitted and found e.g. in the classic text of Harary (1969). In G k the vertices are the (in our case unobserved) sample points, X 1 , ..., X n , and an edge joins vertices X i and X j , if either X j is one of the k nearest neighbors of X i , that is, if d ij is one of the k smallest values (excluding d ii =0 ) on the i -th row of D , or X i is one of the k nearest neighbors of X j .


<!-- p:3 -->


Our intuition is that, as the dimension increases, the vertices in G k become more ''interconnected'' (since there are more directions in which one can look for neighbors), and an appropriate measure of ''interconnectedness,'' should give useful information on the dimension of the data. Such a measure is the average reach , which we define next.

Let V be a finite or countable infinite subset of R d and let G=G k (V) be the k -nearest-neighbors graph over the vertex set V . For vertices x and y in V , say that y can be reached in j steps from x , if there exists a path v 0 , v 1 , ..., v j in G , with v 0 =x and v j =y . The reach in j steps of vertex x ¥ V , r j, k (x, V) , is the total number of vertices that can be reached from x , in j steps or less using edges of G , that is

r j, k (x, V)= card {y ¥ V : y ] x, y is reached in l steps from x; l [ j}, (1)

where ''card'' denotes the cardinality of a set. For a finite subset U of V , let

$$r _ { j , k } ( U , V ) = \sum _ { x \in U } r _ { j , k } ( x , V ) .$$

When V is finite, we can compute r j, k (V, V) and this will be denoted r j, k (V) , while the average reach in j steps in G , r  ̄ j, k (V) , is defined as

$$\bar { r } _ { j , k } ( V ) = \sum _ { x \in V } r _ { j , k } ( x , V ) / \text {card} \, V .$$

In most of what follows, V will be the i.i.d. sample X 1 , ..., X n associated to the distance matrix D and, in this case we simply write r  ̄ j, k for r  ̄ j, k (X 1 , ..., X n ) . We will explore the use of the variables r  ̄ j, k , for different values of k and j , as dimension discriminators. In what follows, we will sometimes refer to these variables as reach variables. It is, perhaps, convenient to remark that reach variables are (i) completely computable from the distance matrix D and (ii) actually, very easy to compute, using standard algorithms of low complexity for the traversal of graphs (see, for example, Biggs, 1990). In the next section, we present the result of a MonteCarlo experiment, designed to validate the intuition that r  ̄ j, k is, in expectation, an increasing function of the dimension of the data associated to a distance matrix D . We also present a simple procedure, based on one of the variables r  ̄ j, k , for assigning a dimension, between 2 and 5, to a given distance matrix and we comment on its accuracy. This procedure can be presented as a binary decision tree, and is built using a simplified version of the CART methodology (Breiman, Friedman, Olshen, Stone, 1984). We also discuss the use of the variables considered in the context of reduction of dimensionality. In Section 3, we present a theorem which states that, for i.i.d. data having a continuous density, r  ̄ j, k converges, as the sample size grows, to a constant which represents the average number of points reachable from an arbitrary point adjoined to a homogeneous Poisson process of unit intensity on R d . Section 3 also establishes the asymptotic normality of the reach statistic in the setting of uniformly distributed random variables.


<!-- p:4 -->


## 2. USING r  ̄ j, k IN DIMENSION DISCRIMINATION

### 2.1. Using Reach Variables in Decision Trees for Dimension Discrimination

We will describe first a MonteCarlo experiment designed to validate the intuition mentioned in the previous section, in the sense that, as the dimension d grows, the graph G k (for each fixed k ) becomes more interconnected and this fact should be reflected on the values of the variables r  ̄ j, k . All the simulations described here were programmed in Fortran language and run on a Pentium PC. For each combination of j ¥ {1, 2, 3} , k ¥ {1, ..., 5} and each dimension d ¥ {2, 3, 4, 5} , we generate 100 samples of size n=100 from the standard Gaussian distribution on R d , and compute for each sample the statistics r  ̄ j, k . The values of the statistic obtained for each triple (j, k, d) are used to estimate the corresponding mean and standard deviation, and these estimates are reported in Tables I, II and III. Some quantiles of r  ̄ j, k were also estimated from these runs and, although they are not displayed for reasons of space, they are available from the authors. We observe in these tables that, for each choice of the pair (j, k) there is a tendency of the mean value of r  ̄ j, k to increase with dimension, and this tendency becomes stronger for larger values of j and k . Denote by m  ̃ (k, j, d) and s  ̃ (k, j, d) the estimates reported in Tables I-III. One way to predict the potential of a reach variable, r  ̄ j, k , as dimension discriminator (suggested by parametric discriminant analysis), is to compute the indices

$$i ( j , k , d ) = \frac { | \tilde { \mu } ( k , j , d + 1 ) - \tilde { \mu } ( k , j , d ) | } { \tilde { \sigma } ( k , j , d ) \wedge \tilde { \sigma } ( k , j , d + 1 ) } \quad \text {for } \ d = 2 , 3 , 4$$

and i(j, k)= min d i(j, k, d) . Larger values of i(j, k) suggest a better ability of the corresponding variable to identify dimensions in the range considered. When i(j, k) is computed from our mean and standard deviation estimates, we obtain the values shown in Table IV. A clear tendency of i(j, k) to increase with both j and k is observed, suggesting that larger values of both parameters should be preferred for our application. Choosing j=1 , which corresponds to looking at the average degree of vertices in G k , clearly seems like a poor choice for dimension discrimination.


<!-- p:5 -->


TABLE I Estimated Mean and Standard Deviation for r  ̄ 1, k , n=100

|   k |   dim=2 |   dim=2 |   dim=3 |   dim=3 |   dim=4 |   dim=4 |   dim=5 |   dim=5 |
|-----|---------|---------|---------|---------|---------|---------|---------|---------|
|   1 |    1.41 |    .050 |    1.46 |    .046 |    1.50 |    .045 |    1.53 |    .050 |
|   2 |    2.67 |    .056 |    2.78 |    .071 |    2.88 |    .070 |    2.93 |    .088 |
|   3 |    3.91 |    .085 |    4.08 |    .087 |    4.22 |    .097 |    4.33 |    .098 |
|   4 |    5.13 |    .100 |    5.38 |    .112 |    5.54 |    .127 |    5.68 |    .127 |
|   5 |    6.38 |    .128 |    6.70 |    .131 |    6.90 |    .139 |    7.04 |    .147 |

TABLE II Estimated Mean and Standard Deviation for r  ̄ 2, k , n=100

|   k |   dim=2 |   dim=2 |   dim=3 |   dim=3 |   dim=4 |   dim=4 |   dim=5 |   dim=5 |
|-----|---------|---------|---------|---------|---------|---------|---------|---------|
|   1 |    2.29 |    .148 |    2.53 |    .185 |    2.72 |    .210 |    2.89 |    .224 |
|   2 |    5.42 |    .346 |    6.34 |    .377 |    7.17 |    .394 |    7.95 |    .497 |
|   3 |    8.89 |    .451 |    10.8 |    .554 |    12.8 |    .696 |    14.2 |    .827 |
|   4 |    12.5 |    .606 |    16.0 |    .784 |    18.6 |    .826 |    21.1 |    1.11 |
|   5 |    16.3 |    .675 |    20.8 |    .999 |    24.6 |    1.16 |    28.0 |    1.32 |

TABLE III Estimated Mean and Standard Deviation for r  ̄ 3, k , n=100

|   k |   dim=2 |   dim=2 |   dim=3 |   dim=3 |   dim=4 |   dim=4 |   dim=5 |   dim=5 |
|-----|---------|---------|---------|---------|---------|---------|---------|---------|
|   1 |    2.73 |    .253 |    3.16 |    .326 |    3.50 |    .386 |    3.77 |    .433 |
|   2 |    8.24 |    .775 |    10.8 |    1.04 |    13.1 |    1.25 |    15.7 |    1.47 |
|   3 |    15.1 |    1.06 |    21.5 |    1.72 |    27.1 |    2.08 |    32.5 |    2.74 |
|   4 |    22.1 |    1.43 |    32.8 |    2.35 |    41.7 |    2.73 |    49.6 |    3.59 |
|   5 |    29.5 |    1.72 |    43.6 |    2.25 |    55.0 |    3.28 |    65.0 |    3.05 |

TABLE IV Index i(j, k) , n=100

|   j |   k=1 |   k=2 |   k=3 |   k=4 |   k=5 |
|-----|-------|-------|-------|-------|-------|
|   1 |  0.67 |  0.56 |  1.13 |  1.03 |  0.93 |
|   2 |  0.76 |  1.56 |  1.72 |  2.26 |  2.55 |
|   3 |  0.61 |  1.77 |  1.97 |  2.22 |  3.06 |


<!-- p:6 -->


Now, we will describe a simple decision procedure for automatic dimension assignment, based on the variable r  ̄ 3, 4 . For illustrative purposes, we restrict ourselves to the problem of assigning a dimension in the set D ={2, 3, 4, 5} . Our procedure takes as input a distance matrix D and produces, as output, a probable dimension d in D . By the strong tendency of the variables considered to increase with dimension, the procedure takes the following simple form:

- Step 0. Three numbers (thresholds) z 2 &lt;z 3 &lt;z 4 have been chosen based on a training set , as described below. Let z 1 =0 and z 5 = . .
- Step 1. Compute r  ̄ 3, 4 from the given distance matrix D .
- Step 2. For i=1 to 4, do: if z i [ r  ̄ 3, 4 &lt;z i+1 , assign d the value i+1 .
- End.

For the selection of the thresholds z 2 , z 3 , and z 4 , a training set is required, that is, a set of examples for which the true answer (the dimension) is known. For this purpose, for each dimension d ¥ D , we considered three possible distributions: the d -dimensional standard Gaussian, the distribution with independent exp(1) coordinates, and the mixture distribution given by 0.5 N(0, I d )+0.5 N( m , I d ) , where I d is the identity matrix and m is the d -dimensional vector (3, 3, ..., 3) . For each d ¥ D , for each sample size n=300, 400, 500 and 600 , and for each of the three distributions, we generated 20 samples of size n from the given distribution, for a total of 960 samples. The two distributions different from the standard Gaussian are included to assess the effect of a different tail behavior and of the presence of clusters on the procedure considered. The thresholds are chosen by minimizing the empirical error over this training set, that is, by minimizing the number of classification errors of the procedure given above over the 960 training samples. Finally, the resulting procedure is evaluated by computing its classification error over a new and independent set of samples, the validation set , generated in the same way as the training set.

The results of the threshold selection and the evaluation of the dimension assignment procedures are given in Table V. In spite of its simplicity, being based on a single reach variable, and the fact that it is being evaluated on different distributions and sample sizes, the procedure identifies the right dimension with high probability, with a classification error of less than 6% on the validation set. The classification error obtained suggests that the data distribution has little effect on the value of the reach variables considered. Regarding the behavior of this type of procedure on nearly-degenerate data, see, however, the following subsection. One could try to improve the behavior of our procedure by building more complex classification trees, based on several reach variables and designed following the CART methodology. We do not pursue this approach, since the results obtained with our simple procedure based on a single variable are satisfactory.

TABLE V Dimension Assignment Procedure and Its Classification Error

| Variable used   |   z 2 |   z 3 |   z 4 |   Validation error |
|-----------------|-------|-------|-------|--------------------|
| r  ̄ 3, 4        | 27.18 | 38.06 | 49.70 |              0.056 |


<!-- p:7 -->


### 2.2. The Interplay between Near-Degeneracy of the Continuous Density and Sample Size

Even though r  ̄ j, k converges, as the sample size grows, to a limit which does not depend on the underlying continuous density, one could expect that, for a fixed sample size, the graph G k corresponding to a sample coming from a continuous density f on R d , with support lying in the vicinity of an affine subspace of dimension p ( p &lt; d ), would be very similar to the graph for the p -dimensional sample obtained by projection of the d -dimensional sample on the affine subspace. Thus, for nearly-degenerate densities, the dimension assignment procedures based on the reach variables, might be able to identify the dimension p of the affine subspace around which the data are concentrating.

In order to verify the behavior of our methodology on densities approaching singularity, we performed the following MonteCarlo experiment: 100 samples of size n=400 were generated from the 4-dimensional distribution N (0, A 2 ) , where the matrix A is of the form diag (1, 1, e , e ) . Then, each sample was assigned a dimension (in {2, 3, 4, 5} ), using the procedure based on r  ̄ 3, 4 given in Subsection 2.1, and the percentage of times each dimension was assigned was recorded. This was repeated for e =0.02, 0.1 , and 0.25. The experiment is repeated for n=600 , and the results are summarized in Table VI, where the numbers under the column d  ̃ =i give the fraction of samples that were assigned dimension i by our procedure in each case. We see that, in the case of more severe degeneracy of the continuous density ( e =0.02 ), all samples are classified as twodimensional, for both sample sizes considered, and, as the degree of degeneracy diminishes, the samples will tend to be classified first as threedimensional and then, as four-dimensional for the largest value of e . We observe that the effect of a larger sample size is to offset, to some extent, the degeneracy of the continuous density, resulting in more samples being classified in higher dimensions for e =0.1 and 0.25. In particular, for n=600 and e =.25 , all samples are (correctly) assigned dimension 4 by our procedure.

TABLE VI Dimension Assignment for Nearly Degenerate Data

|   Sample size |    e |   d  ̃=2 |   d  ̃=3 |   d  ̃=4 |   d  ̃=5 |
|---------------|------|---------|---------|---------|---------|
|           400 | 0.02 |    1.00 |    0.00 |    0.00 |    0.00 |
|           400 | 0.10 |    0.19 |    0.81 |    0.00 |    0.00 |
|           400 | 0.25 |    0.00 |    0.18 |    0.82 |    0.00 |
|           600 | 0.02 |    1.00 |    0.00 |    0.00 |    0.00 |
|           600 | 0.10 |    0.00 |    1.00 |    0.00 |    0.00 |
|           600 | 0.25 |    0.00 |    0.00 |    1.00 |    0.00 |


<!-- p:8 -->


## 3. ASYMPTOTIC BEHAVIOR OF THE REACH VARIABLES

### 3.1. Almost Sure Convergence of r  ̄ j, k

The main purpose of this section is to prove that when data come from a d -dimensional distribution having a continuous density f , (with respect to Lebesgue measure, as usual) then, for every fixed j and k ,

$$\bar { r } _ { j , k } \rightarrow \beta ( j , k , d ) , \quad a . s . , \text { as } n \rightarrow \infty ,$$

where the constant b (j, k, d) depends only on the three parameters indicated ( j, k, and d ) and not on the data density.

In what follows, P denotes a realization of the homogeneous Poisson point process on R d with unit intensity.

We will make use of the following lemmas, which we prove at the end of this section.

Lemma 1 (Boundedness of r j, k ( · ) ). For each pair of positive integers j , k and each dimension d , there exists a constant c = c (j, k, d) such that, for every countable V and x ¥ V , r j, k (x, V) [ c and r  ̄ j, k (V) [ c .

Lemma 2 (Deterministic smoothness of r j, k ( · ) ) . For all positive integers j , k and each dimension d , there exists a constant C=C(j, k, d) such that, for all finite sets U and V in R d ,

$$| r _ { j , k } ( V ) - r _ { j , k } ( V \cup U ) | \leqslant C ( j , k , d ) \cdot c a r d ( U ) .$$


<!-- p:9 -->


Lemma 3 (Stochastic smoothness of r j, k ( · ) ). Suppose the laws of X and Y are related by

$$\mathcal { L } ( Y ) = \rho \mathcal { L } ( X ) + ( 1 - \rho ) \, \mu ,$$

where m is a probability measure on R d and 0 &lt; r &lt;1 . If X 1 , ..., X n is a random sample from L (X) and if Y 1 , ..., Y n is a random sample from L (Y) , then

$$| \mathbb { E } r _ { j , k } ( \{ X _ { 1 } , \dots , X _ { n } \} ) - \mathbb { E } r _ { j , k } ( \{ Y _ { 1 } , \dots , Y _ { n } \} ) | \leqslant 2 \, C ( j , k , d ) ( n ( 1 - \rho ) ) ,$$

where the constant C(j, k, d) is the same as that in Lemma 2 .

Our last lemma is useful for handling boundary effects in the calculation of r  ̄ j, k for the points of P falling in a d -dimensional cube.

Lemma 4. Let U 1 , U 2 , ... be i.i.d. points, uniformly distributed in the cube C n =[0, n 1/d ] d ... R d . Let N(n) be a random variable with distribution Poisson( n ) and independent of the U i . When N(n) \ 1 , then for each i [ N(n) , let d i(j, k) ( P ) denote the largest distance from U i to one of the points reachable from it in j or less steps in G k ( P ) , and, when N(n) \ j+1 , define d i(j, k) ( P 5 C n ) similarly. Then, for each a &gt; 1 , there exists a positive constant o a = o a (j, k, d) such that if

$$A _ { n } = \{ 2 \max _ { i \leqslant N ( n ) } \left ( d _ { i ( j , k ) } ( \Pi ) \vee d _ { i ( j , k ) } ( \Pi \cap C _ { n } ) \right ) \leqslant \kappa _ { a } ( \log n ) ^ { 1 / d } \}$$

then for sufficiently large n ,

$$\Pr ( A _ { n } ^ { c } ) \leqslant n ^ { - a } .$$

As a first result, we establish the convergence of the mean of r  ̄ j, k over a uniformly distributed sample.

Theorem 1. Let U 1 , U 2 , ... be an i.i.d. sample from the uniform distribution on the unit cube [0, 1] d . Let b (j, k, d)= E r j, k ({0}, P 2 {0}) . Then

$$\mathbb { E } \bar { r } _ { j , k } ( \{ U _ { 1 } , \dots , U _ { n } \} ) \to \beta ( j , k , d ) , \quad a s \ \ n \to \infty .$$

Proof. If each point of the sample {U 1 , ..., U n } has all its coordinates multiplied by n 1/d , the reach of each point remains the same. Thus, in the following argument we will think of U 1 , U 2 , ..., as uniformly distributed on C n =[0, n 1/d ] d , and we will identify U 1 , ..., U N(n) with P 5 C n . Using Lemmas 1 and 2, we have E r j, k ({U 1 , ..., U N(n) })/nE r  ̄ j, k ({U 1 , ..., U n }) Q 0 , and it is also easy to see that E r j, k ({U 1 , ..., U N(n) })/nE r  ̄ j, k ({U 1 , ..., U N(n) }) Q 0 . Thus, by the triangle inequality we have


<!-- p:10 -->


$$\mathbb { E } \bar { r } _ { j , k } ( \{ U _ { 1 } , \dots , U _ { N ( n ) } \} ) - \mathbb { E } \bar { r } _ { j , k } ( \{ U _ { 1 } , \dots , U _ { n } \} ) \to 0 ,$$

as n goes to infinity.

We want to approximate r j, k ( P 5 C n ) by r j, k ( P 5 S n , P ) , where S n is a subset of C n to be defined shortly.

We will need to bound the change in total reach produced by removing the points of P outside C n from the graph G k ( P ) . When the points of P 5 C c n are removed (from P and the graph G k ( P ) ) some edges between P 5 C n and P 5 C c n are deleted. Some of these edges are replaced in the graph G k ( P 5 C n ) by new ones. If x ¥ P 5 C n has y ¥ P 5 C c n as one of its k nearest neighbors, the deleted edge {x, y} will be replaced by a new edge {x, x Œ } , for some x Œ ¥ P 5 C n in the graph G k ( P 5 C n ) . For z ¥ P 5 C n , the deletion of edge {x, y} or the addition of {x, x Œ } , can affect the reach in j steps of z , only if x is reachable in j or less steps from z in one of the graphs G k ( P ) or G k ( P 5 C n ) . It follows that, given the event A n of Lemma 4, a point z ¥ P 5 C n , at distance greater than l n = o a ( log n) 1/d from the boundary of C n , will have the same reach in the graphs G k ( P ) and G k ( P 5 C n ) .

Partition C n into the following two regions: the ''moat'' M n of points near the boundary, defined by

$$M _ { n } = \{ x \in C _ { n } \colon \text {for some } i \leqslant d , \, x _ { i } \leqslant l _ { n } \text { or } x _ { i } \geqslant n ^ { 1 / d } - l _ { n } \} ,$$

and the large, inner cube S n =C n 0 M n of side n 1/d -2l n .

Since r  ̄ j, k ({U 1 , ..., U N(n) })=N(n) -1 ; N(n) i=1 r j, k (U i , {U 1 , ..., U N(n) }) , we get:

$$\mathbb { E } \bar { r } _ { j , k } ( \{ U _ { 1 } , \dots , U _ { N ( n ) } \} ) = \mathbb { E } r _ { j , k } ( U _ { 1 } , \{ U _ { 1 } , \dots , U _ { N ( n ) } \} ) .$$

Next, we have

$$| \mathbb { E } r _ { j , k } ( U _ { 1 } , \{ U _ { 1 } , \dots , U _ { N ( n ) } \} ) - \mathbb { E } r _ { j , k } ( U _ { 1 } , \{ U _ { 1 } , \dots , U _ { N ( n ) } , U _ { N ( n ) + 1 } \} ) | \to 0 .$$

This may be seen by evaluating the difference

$$r _ { j , k } ( U _ { 1 } , \{ U _ { 1 } , \dots , U _ { N ( n ) } \} ) - r _ { j , k } ( U _ { 1 } , \{ U _ { 1 } , \dots , U _ { N ( n ) } , U _ { N ( n ) + 1 } \} )$$

over the sets E n and E c n , where E n =A c n 2 {||U N(n)+1 -U 1 | | [ l n } , and using the facts that the difference is uniformly bounded by a constant (Lemma 1), P(E n )=o(1) , and on E c n the difference is zero. Note that we can rewrite (8) as

$$| \mathbb { E } _ { j , k } ( U _ { 1 } , \{ U _ { 1 } , \dots , U _ { N ( n ) } \} ) - \mathbb { E } r _ { j , k } ( U _ { 0 } , \{ U _ { 0 } , U _ { 1 } , \dots , U _ { N ( n ) } \} ) | \rightarrow 0 ,$$


<!-- p:11 -->


where U 0 is uniformly distributed on C n and independent of the U i , i \ 1 . Next, note that

$$\mathbb { E } r _ { j , k } ( U _ { 0 } , \{ U _ { 0 } , U _ { 1 } , \dots , U _ { N ( n ) } \} ) = \mathbb { E } r _ { j , k } ( U _ { 0 } , \{ U _ { 0 } , U _ { 1 } , \dots , U _ { N ( n ) } \} ) \ 1 _ { A _ { n } } 1 _ { U _ { 0 } \in S _ { n } } + o ( 1 ) ,$$

since r j, k is bounded, P(A c n ) Q 0 , and P(U 0  ̈ S n ) Q 0 . Moreover, on the set A n 5 {U 0 ¥ S n } Lemma 4 implies that r j, k (U 0 , {U 0 , U 1 , ..., U N(n) }) coincides with r j, k (U 0 , U 0 2 P ) , and thus

$$\mathbb { E } r _ { j , k } ( U _ { 0 } , \{ U _ { 0 } , U _ { 1 } , \dots , U _ { N ( n ) } \} ) = \mathbb { E } r _ { j , k } ( U _ { 0 } , U _ { 0 } \cup I ) + o ( 1 ) .$$

By translation invariance we have

$$\mathbb { E } _ { r _ { j , k } } ( U _ { 0 } , U _ { 0 } \cup I T ) = \mathbb { E } _ { r _ { j , k } } ( U _ { 0 } - U _ { 0 } , U _ { 0 } \cup \Pi - U _ { 0 } ) = \mathbb { E } _ { r _ { j , k } } ( \{ 0 \} , \{ 0 \} \cup \Pi ) .$$

Combining these estimates with (7) and (8) we obtain Theorem 1.

Theorem 1 generalizes to arbitrary continuous densities, as follows.

Theorem 2. Let X 1 , X 2 , ... be an i.i.d. sample from a distribution on R d having continuous density f . Then

$$\mathbb { E } \bar { r } _ { j , k } ( \{ X _ { 1 } , \dots , X _ { n } \} ) \to \beta ( j , k , d ) , \quad a s \ \ n \to \infty ,$$

for the same constant b (j, k, d) of Theorem 1 .

Proof. Denote by F n the sample {X 1 , ..., X n } . Consider first the case in which f is a step density of the form

$$\phi = \sum _ { l = 1 } ^ { L } \, \alpha _ { i } \mathbb { 1 } _ { B _ { i } } ,$$

where the a i are positive numbers summing to 1 and the B i , 1 [ i [ L, are disjoint cubes. Partition each B i into an outer ''moat'' M i, n , and an inner cube S i, n , as we did with the cube C n of the previous proof. Choose the moats with thickness of the magnitude C( log n/n) 1/d , thin enough to have

$$\mathbb { E } \bar { r } _ { j , k } ( F _ { n } ) - \frac { 1 } { n } \sum _ { i = 1 } ^ { L } \, \mathbb { E } r _ { j , k } ( S _ { i , n } \cap F _ { n } , F _ { n } ) \to 0 , \quad \text {as} \quad n \to \infty$$

and

$$\frac { 1 } { n } \sum _ { i = 1 } ^ { L } \mathbb { E } r _ { j , k } ( S _ { i , n } \cap F _ { n } , B _ { i } \cap F _ { n } ) - \frac { 1 } { n } \sum _ { i = 1 } ^ { L } \mathbb { E } r _ { j , k } ( B _ { i } \cap F _ { n } ) \rightarrow 0 , \quad \text {as } n \rightarrow \infty \ ( 1 2 )$$


<!-- p:12 -->


but, sufficiently wide to guarantee that the event

$$D _ { n } = \{ \text {for some } i \leqslant L \colon r _ { j , k } ( S _ { i , n } \cap F _ { n } , F _ { n } ) \neq r _ { j , k } ( S _ { i , n } \cap F _ { n } , B _ { i } \cap F _ { n } ) \}$$

satisfies Pr (D n ) [ n -a , for some fixed a &gt; 1 , and n sufficiently large. Then the triangle inequality and (11) and (12) give

$$\mathbb { E } \bar { r } _ { j , k } ( F _ { n } ) = \sum _ { i = 1 } ^ { L } \, \mathbb { E } \left ( \, \frac { n _ { i } } { n } \, \bar { r } _ { j , k } ( B _ { i } \cap F _ { n } ) \right ) + o ( 1 ) ,$$

where n i = card {B i 5 F n } . For each i [ L , we have by Lemma 1

$$\mathbb { E } \left | \left ( \frac { n _ { i } } { n } - \alpha _ { i } \right ) \bar { r } _ { j , k } ( B _ { i } \cap F _ { n } ) \right | \leqslant \gamma \mathbb { E } \left | \frac { n _ { i } } { n } - \alpha _ { i } \right | \to 0 ,$$

as n Q . , since (n i /n)- a i goes to 0 in the L 1 -norm. Applying Theorem 1, we have, for each i ,

$$\mathbb { E } \bar { r } _ { j , k } ( B _ { i } \cap F _ { n } ) \rightarrow \beta ( j , k , d )$$

and, Theorem 2 follows, in the particular case considered, from (13) and (14).

For the general case, let L (X) be the probability law corresponding to the continuous density f . Then, for e &gt;0 we can write

$$\mathcal { L } ( X ) = ( 1 - \varepsilon ) \ \mathcal { L } ( Y ) + \varepsilon \mu ,$$

where the variable Y has a step density f of the form (10) and m is some probability measure. By the triangle inequality we have

$$| \mathbb { E } \bar { r } _ { j , k } ( X _ { 1 } , \dots , X _ { n } ) - \beta ( j , k , d ) | \\ \leq & | \mathbb { E } \bar { r } _ { j , k } ( X _ { 1 } , \dots , X _ { n } ) - \mathbb { E } \bar { r } _ { j , k } ( Y _ { 1 } , \dots , Y _ { n } ) | + | \mathbb { E } \bar { r } _ { j , k } ( Y _ { 1 } , \dots , Y _ { n } ) - \beta ( j , k , d ) | .$$

Letting n go to infinity, applying Lemma 3, using the case just proved for step densities, and letting e tend to zero concludes the proof of Theorem 2.

The a.s. convergence of r  ̄ j, k follows from the convergence of the mean given by Theorem 2:

Theorem 3. Let X 1 , X 2 , ... be an i.i.d. sample from a distribution on R d having continuous density f . Then

$$\bar { r } _ { j , k } ( \{ X _ { 1 } , \dots , X _ { n } \} ) \rightarrow \beta ( j , k , d ) , \quad a . s . \ a s \ \ n \rightarrow \infty .$$


<!-- p:13 -->


Proof. Denote by s (X 1 , ..., X j ) the smallest s -algebra making the variables X 1 , ..., X j measurable. In order to apply Azuma's inequality write, as usual,

$$r _ { j , k } ( \{ X _ { 1 } , \dots , X _ { n } \} ) - \mathbb { E } r _ { j , k } ( \{ X _ { 1 } , \dots , X _ { n } \} ) = \sum _ { i = 1 } ^ { n } \, d _ { i } ,$$

$$d _ { i } & = \mathbb { E } ( r _ { j , k } ( \{ X _ { 1 } , \dots , X _ { n } \} ) \, | \, \sigma ( X _ { 1 } , \dots , X _ { i } ) ) \\ & - \mathbb { E } ( r _ { j , k } ( \{ X _ { 1 } , \dots , X _ { n } \} ) \, | \, \sigma ( X _ { 1 } , \dots , X _ { i - 1 } ) ) \\ & = \mathbb { E } ( r _ { j , k } ( \{ X _ { 1 } , \dots , X _ { n } \} ) \, | \, \sigma ( X _ { 1 } , \dots , X _ { i } ) ) \\ & - \mathbb { E } ( r _ { j , k } ( \{ X _ { 1 } , \dots , X _ { i } ^ { \prime } , \dots , X _ { n } \} ) \, | \, \sigma ( X _ { 1 } , \dots , X _ { i } ) )$$

where X - 1 , ..., X - n are independent copies of X 1 , ..., X n . Now replacing X i by X - i changes the total reach by at most K=2C(j, k, d) (Lemma 2), showing that | |d i | | . [ K . Azuma's inequality tells us that there exists a C&gt;0 such that for all e &gt;0 we have

$$\Pr \left ( \left | \sum _ { i = 1 } ^ { n } d _ { i } \right | \geqslant \varepsilon \, n \right ) \leqslant \exp \left ( - \frac { C ( \varepsilon \, n ) ^ { 2 } } { \sum _ { i = 1 } ^ { n } \| d _ { i } \| _ { \infty } ^ { 2 } } \right )$$

$$\sum _ { n = 1 } ^ { \infty } \Pr \left ( \left | \sum _ { i = 1 } ^ { n } d _ { i } \right | \geqslant \varepsilon \, n \right ) < \infty .$$

The Borel-Cantelli Lemma gives the almost sure convergence.

Two comments should be made about the proof just given.

1. The above Borel-Cantelli argument gives the complete convergence of r  ̄ j, k ({X 1 , ..., X n }) to its asymptotic mean (recall that random variables W n converge completely to the constant C iff for all e &gt;0 we have ; . n=1 Pr(|W n -C| &gt; e ) &lt; . ). Complete convergence, which is stronger than a.s. convergence, tells us that Theorem 3 is valid for the two relevant models of interdependance between the sample of size n and the sample of size n+1 , namely, the incrementing model , in which the sample of size n+1 is obtained from the sample of size n by the addition of a new independent point, X n+1 , and the independent model , where the sample of size n is replaced by an entire new (and independent) sample to produce the sample of size n+1 . This gives the statistician some flexibility in the interpretation and application of Theorem 3.

with

and, therefore,


<!-- p:14 -->


2. Azuma's inequality (16), provides a fast (exponential) rate of concentration of r  ̄ j, k ({X 1 , ..., X n }) around its mean. On the other hand, our MonteCarlo experiments described above, strongly suggest that the constants b (j, k, d) increase with dimension. Provided the last fact holds, we can establish results on the large sample classification error probability for procedures based on r  ̄ j, k ({X 1 , ..., X n }) , as the one described in Subsection 2.1, or even simpler ones, as the following. As before, let D be the n×n distance matrix corresponding to an i.i.d. sample X 1 , ..., X n coming from a fixed but unknown distribution with a continuous density f on R d . Let D be a finite set of integers containing d . From D , we compute the average reach, r  ̄ j, k ({X 1 , ..., X n }) . For each d Œ ¥ D , we generate one sample of size n , say F n, d Œ , from the Unif ([0, 1] d Œ ) distribution, and compute the corresponding average reach, r  ̄ j, k (F n, d Œ ) . We estimate d by

$$\widetilde { d } = \arg \min _ { d ^ { \prime } \in \mathcal { D } } \, | \bar { r } _ { j , k } ( \{ X _ { 1 } , \dots , X _ { n } \} ) - \bar { r } _ { j , k } ( F _ { n , d ^ { \prime } } ) | .$$

Even though only one example is used from each dimension in D , we have the following result, whose proof is straightforward and omitted.

Proposition 1. If, for the values of j and k chosen, the constants b (j, k, d) are strictly increasing on D , then, there exists an integer n 0 (depending on the underlying continuous density f of the data X 1 , X 2 , ... ) such that, the probability of classification error, Pr (d  ̃ ] d) , for the procedure described in the previous paragraph, satisfies Pr (d  ̃ ] d) [ exp (-c n) , for some constant c &gt; 0 and n \ n 0 .

Our next result establishes the asymptotic normality of the reach statistic r  ̄ j, k , in the particular case of an i.i.d. sample from the uniform distribution on the unit cube [0, 1] d . We do not have an extension of Theorem 4 to nonuniform random variables.

Theorem 4. Let U 1 , U 2 , ... be i.i.d. points, uniformly distributed on the unit cube [0, 1] d . Then, there exists s 2 = s 2 (d, j, k) &gt; 0 such that, as n Q . ,

$$n ^ { - 1 } \ V a r \left ( ( r _ { j , k } ( \{ U _ { 1 } , \dots , U _ { n } \} ) ) \to \sigma ^ { 2 } \ a n d$$

$$n ^ { - 1 / 2 } [ r _ { j , k } ( \{ U _ { 1 } , \dots , U _ { n } \} ) - E r _ { j , k } ( \{ U _ { 1 } , \dots , U _ { n } \} ) ] \stackrel { \mathcal { L } } { \rightarrow } N ( 0 , \sigma ^ { 2 } ) .$$

The proof of Theorem 4 follows from a straightforward application of Theorem 2.1 of Penrose and Yukich (2001) to the reach statistic. Penrose and Yukich show that several functionals of the nearest neighbor graph (number of components, total Euclidean edge length) satisfy a CLT (see especially section 6 in this reference). These functionals all satisfy a ''strongly stabilizing'' condition as well as a uniformly bounded moments condition and polynomial growth condition (see Penrose and Yukich, 2001, for details) and thus a CLT. Using the approach given there, it is a simple matter to see that the reach statistic, in the uniform case, satisfies the same conditions and thus a CLT as well.


<!-- p:15 -->


### 3.2. Proofs of Lemmas

Proof of Lemma 1 . This lemma follows from the well-known fact that the vertices of G k (F) have bounded degree (see, for example, Lemma 8.4 of Yukich, 1998).

Proof of Lemma 2 . Let d be an upper bound for the largest possible degree in G k (E 2 F) ( d exists by Lemma 1). Let m= card (F) . When the vertices in F are removed from the graph G k (E 2 F) , the graph loses at most m d edges. Now, suppose that x ¥ E has y ¥ F as one of its k nearest neighbors in E 2 F . In the graph G k (E) that neighbor will be replaced by some x Œ ¥ E . Thus, going from G k (E 2 F) to G k (E) involves the removal of at most m d edges, which are replaced by at most m d new edges. Now, when an edge e is added to a graph G k (.) , it can ony affect the reach in j steps of those vertices that reach one of the vertices incident to e in j - 1 or less steps. It follows that, at most, c (j, k, d) vertices change their reach when a new edge is added (or removed) and, using again Lemma 1, each reach can change by at most c . Then, when going from G k (E 2 F) to G k (E) , the total reach changes by at most 2 m dc 2 .

Proof of Lemma 3 . Let

$$\{ W _ { 1 } , W _ { 2 } , \dots , W _ { n } \} = \{ X _ { 1 } , \dots , X _ { B ( n ) } , Z _ { B ( n ) + 1 } , \dots , Z _ { n } \} ,$$

where B(n) is a Bin (n, r ) random variable and the Z i are i.i.d. variables with distribution m . Denote by p a random permutation of the indices {1, ..., n} , independent of the W i . By hypothesis,

$$\{ Y _ { 1 } , Y _ { 2 } , \dots , Y _ { n } \} \stackrel { \mathcal { L } } { = } \{ W _ { \pi ( 1 ) } , W _ { \pi ( 2 ) } , \dots , W _ { \pi ( n ) } \} .$$

Then, by Lemma 2 and the triangle inequality

$$| E r _ { j , k } ( \{ X _ { 1 } , \dots , X _ { n } \} ) - E r _ { j , k } ( \{ Y _ { 1 } , \dots , Y _ { n } \} ) | \leqslant 2 C ( j , k , d ) ( n - B ( n ) ) ,$$

and the result follows by taking expectations of both sides.

Proof of Lemma 4 . By the triangle inequality, for every j \ 1 , we have

$$\max _ { i \leqslant N ( n ) } \, d _ { i ( j , k ) } ( \cdot ) \leqslant j \max _ { i \leqslant N ( n ) } \, d _ { i ( 1 , k ) } ( \cdot ) ,$$


<!-- p:16 -->


where the argument ( · ) represents either P or P 5 C n . Clearly, we also have

$$\max _ { i \leqslant N ( n ) } \, d _ { i ( 1 , k ) } ( \Pi ) \leqslant \max _ { i \leqslant N ( n ) } \, d _ { i ( 1 , k ) } ( \Pi \cap C _ { n } ) .$$

Thus, to prove (4) it suffices to show

$$\Pr ( \max _ { i \leq N ( n ) } d _ { i ( 1 , k ) } ( \Pi \cap C _ { n } ) > \kappa _ { a } ^ { \prime } ( \log n ) ^ { 1 / d } ) \leqslant n ^ { - a } ,$$

where o - a = o a /(2j) . For i [ N(n) , let

$$M _ { i } ( t ) = \text { card} \{ j \leqslant N ( n ) \colon j \neq i ; \| U _ { i } - U _ { j } \| \leqslant t \} .$$

Given N(n)=m and U i ( i [ N(n) ), the conditional distribution of M i (t) is Bin (m-1, p) , with p \ g d t d /(2 d n) , where g d denotes the volume of the unit ball in R d and the 2 d factor comes from considering the worst case, in which the point U i falls in a corner of C n . Since d i(1, k) ( P 5 C n ) &gt; t if and only if M i (t) &lt; k , it follows, by one of the Chernoff-Okamoto inequalities (Dudley, 1984, inequality 2.2.7) that

$$\Pr ( d _ { i ( 1 , k ) } ( \Pi \cap C _ { n } ) > t \, | \, N ( n ) = m , U _ { i } ) \leqslant \exp ( - ( m p - k ) ^ { 2 } / 2 m p q ) ,$$

for mp &gt; k . Choosing t= o - a log n and m \ n/2 , we have mp \ g d o - d a log n/2 d+1 . Since k is fixed, for large enough n , mp-k \ mp/2 and the upper bound (19) simplifies to

$$\Pr ( d _ { i ( 1 , k ) } ( \Pi \cap C _ { n } ) > t \, | \, N ( n ) = m , U _ { i } ) \leq \exp ( - m p / 8 ) ,$$

and, using inequality (9), Section 11.9, of Shorack and Wellner, 1986, we obtain

$$\Pr ( d _ { i ( 1 , k ) } ( \Pi \cap C _ { n } ) > \kappa _ { a } ^ { \prime } \log n ) & \leq \Pr ( N ( n ) < n / 2 ) + \sum _ { m \geq n / 2 } \frac { e ^ { - 1 } } { m ! } \, e ^ { - m p / 8 } \\ & \leq ( 2 / e ) ^ { n / 2 } + n ^ { - ( n d _ { a } ^ { r ^ { d } } / 2 ^ { d + 4 } ) } ,$$

which clearly implies (18) for an appropriate choice of o - a .

### 3.3. Estimation of the Limiting Constant

From the proof of Theorem 1 we get the following method for estimating b = b (j, k, d) , the limiting value of r  ̄ j, k : Let P n be a homogeneous Poisson process of intensity n . Then, clearly

$$\beta = \lim _ { n \to \infty } r _ { j , k } ( \Pi _ { n } \cap [ 0 , 1 ] ^ { d } , \Pi _ { n } ) / \, \text { card} ( \Pi _ { n } \cap [ 0 , 1 ] ^ { d } ) .$$


<!-- p:17 -->


TABLE VII Estimated Mean and Standard Deviation for r  ̄ 1, k , n=2000

|   k |   dim=2 |   dim=2 |   dim=3 |   dim=3 |   dim=4 |   dim=4 |   dim=5 |   dim=5 |
|-----|---------|---------|---------|---------|---------|---------|---------|---------|
|   1 |    1.38 |    .013 |    1.41 |    .014 |    1.48 |    .019 |    1.55 |    .021 |
|   2 |    2.58 |    .017 |    2.64 |    .020 |    2.78 |    .024 |    2.91 |    .032 |
|   3 |    3.73 |    .024 |    3.83 |    .026 |    4.03 |    .031 |    4.24 |    .038 |
|   4 |    4.85 |    .026 |    4.99 |    .032 |    5.28 |    .038 |    5.54 |    .048 |
|   5 |    5.96 |    .029 |    6.17 |    .035 |    6.50 |    .045 |    6.85 |    .053 |

In order to estimate the right hand side of (21) we simulate a homogeneous Poisson process of intensity a =2000 on the larger cube C Œ =[-0.1, 1.1] d and compute the average reach of the points of the process that fall in the unit cube, with respect to the graph G k ( P n 5 C Œ ) . This procedure is justified by the ''moat argument'' in Theorem 1. This simulation is repeated for 100 samples, for each combination of j ¥ {1, 2, 3} , k ¥ {1, ..., 5} and d ¥ {2, ..., 5} and we report, in Tables VII to IX the average and standard deviation for the 100 values computed in each case. Most of the estimated mean values in Tables VII-IX are very close to those presented in Tables I-III for n=100 , suggesting that the convergence in mean of r  ̄ j, k is very fast for these choices of parameters and dimension, except for the entries corresponding to j=3 , for which the ''limiting'' values appear to be larger than those observed for n=100 . The values of estimated standard deviations in Tables VII-IX are much smaller than those presented before for n=100 , resulting in significantly larger values for the indexes i(j, k) , indicating that, for very large samples, basically any reach variable in the range studied, will be a good dimension discriminator for the dimensions considered in our experiment.

TABLE VIII Estimated Mean and Standard Deviation for r  ̄ 2, k , n=2000

|   k |   dim=2 |   dim=2 |   dim=3 |   dim=3 |   dim=4 |   dim=4 |   dim=5 |   dim=5 |
|-----|---------|---------|---------|---------|---------|---------|---------|---------|
|   1 |    2.21 |    .040 |    2.38 |    .052 |    2.57 |    .065 |    2.71 |    .066 |
|   2 |    5.17 |    .082 |    5.95 |    .106 |    6.71 |    .119 |    7.37 |    .137 |
|   3 |    8.46 |    .132 |    10.3 |    .162 |    11.9 |    .177 |    13.4 |    .221 |
|   4 |    12.0 |    .147 |    15.0 |    .179 |    17.9 |    .246 |    20.4 |    .309 |
|   5 |    15.6 |    .163 |    20.2 |    .217 |    24.4 |    .273 |    28.2 |    .363 |


<!-- p:18 -->


TABLE IX Estimated Mean and Standard Deviation for r  ̄ 3, k , n=2000

|   k |   dim=2 |   dim=2 |   dim=3 |   dim=3 |   dim=4 |   dim=4 |   dim=5 |   dim=5 |
|-----|---------|---------|---------|---------|---------|---------|---------|---------|
|   1 |    2.58 |    .073 |    2.83 |    .087 |    3.11 |    .107 |    3.35 |    .108 |
|   2 |    7.72 |    .159 |    9.87 |    .261 |    11.9 |    .271 |    13.7 |    .371 |
|   3 |    14.6 |    .309 |    20.5 |    .482 |    26.2 |    .586 |    31.8 |    .719 |
|   4 |    22.4 |    .401 |    33.7 |    .608 |    44.8 |    .886 |    56.1 |    1.06 |
|   5 |    30.7 |    .444 |    48.5 |    .799 |    66.6 |    1.22 |    85.5 |    1.53 |
