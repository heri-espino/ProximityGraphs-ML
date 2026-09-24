---
id: "Farahmand_2007_Manifold-Adaptive-Dimension-Estimation"
source_pdf: "../pdf/Farahmand_2007_Manifold-Adaptive-Dimension-Estimation.pdf"
source_filename: "Farahmand_2007_Manifold-Adaptive-Dimension-Estimation.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "full-page-ocr"
extraction_quality: "excellent"
extraction_score: 108.0
visual_assets: "disabled"
references_file: "../references/Farahmand_2007_Manifold-Adaptive-Dimension-Estimation.references.md"
---

<!-- p:1 -->

## Manifold-Adaptive Dimension Estimation

Amir massoud Farahmand Csaba Szepesvári AMIR@CS.UALBERTA.CA SZEPESVA@CS.UALBERTA.CA

Department of Computing Science, University of Alberta, Edmonton, AB T6G 2E8 Canada

Jean-Yves Audibert AUDIBERT@CERMICS.ENPC.FR

CERTIS - Ecole des Ponts, 19, rue Alfred Nobel - Cité Descartes, 77455 Marne-la-Vallée France

#### Abstract

larity is present in the data.

Intuitively, learning should be easier when the data points lie on a low-dimensional submanifold of the input space. Recently there has been a growing interest in algorithms that aim to exploit such geometrical properties of the data. Oftentimes these algorithms require estimating the dimension of the manifold first. In this paper we propose an algorithm for dimension estimation and study its finite-sample behaviour. The algorithm estimates the dimension locally around the data points using nearest neighbor techniques and then combines these local estimates. We show that the rate of convergence of the resulting estimate is independent of the dimension of the input space and hence the algorithm is "manifold-adaptive". Thus, when the manifold supporting the data is low dimensional, the algorithm can be exponentially more efficient than its counterparts that are not exploiting this property. Our computer experiments confirm the obtained theoretical results.

## 1. Introduction

The curse of dimensionality in machine learning refers to the tendency of learning algorithms working in highdimensional spaces to use resources (time, space, samples) that scale exponentially with the dimensionality of the space. Since most practical problems involve high-dimensional spaces, it is of uttermost importance to identify algorithms that are capable of avoiding this exponential blow-up, exploiting when additional regu- One such regularity that has attracted much attention lately is when the samples lie in a low-dimensional submanifold of the possibly high-dimensional input space. Consider for example the case when the data points are images taken of a scene or object, from different angles. Although the images may contain millions of pixels, they all lie on a manifold of low dimensionality, such as 3. Another example is when the input data is enriched by adding a huge number of feature components computed from the original input components in the hope that these additional features will help some learning algorithm (generalized linear models or the "kernel trick" implement this idea).

Manifold learning research aims at finding algorithms that require less data (i.e., are more data efficient) when the data happens to be supported on a lowdimensional submanifold of the input-space. We call a learning algorithm manifold-adaptive when its samplecomplexity depends on the intrinsic dimension of the manifold only.1 A classical problem in pattern recognition is the estimation of the dimension of the data manifold. Dimension estimation is interesting on its own, but it is also very useful as the estimate can be fed into manifold-aware supervised learning algorithms that need to know the dimension to work efficiently (e.g., Hein 2006; Gine and Koltchinskii 2007).

In this paper we propose an algorithm for estimating the unknown dimension of a manifold from samples and prove that it is manifold-adaptive. The new algorithm belongs to the family of nearest-neighbor methods. Such methods have been considered since the late 70s. Pettis et al. (1979) suggested to average distances to k-nearest neighbors for various values of k and use the obtained values to find the dimension using an iterative method.2 Another more recent method is due to Levina and Bickel (2005) who suggested an algorithm based on a Poisson approximation to the process obtained by counting the number of neighbors of a point in its neighborhood. In a somewhat heuristic manner they argued for the asymptotic consistency of this method. Grassberger and Procaccia (1983) suggested to estimate the dimension based on the so-called correlation dimension, while Hein and Audibert (2005) suggested a method based on the asymptotics of a smoothed version of the correlation dimension estimate. Despite the large number of works and long history, to our best knowledge no previous rigorous theoretical work has been done on the finite-sample behavior of dimension-estimation algorithms, let alone their manifold adaptivity.

Appearing in Proceedings of the 24th International Conference on Machine Learning, Corvallis, OR, 2007. Copyright 2007 by the author(s)/owner(s).

1Of course, the sample-complexity may and will typically depend on the properties of the manifold and thus the embedding.


<!-- p:2 -->


the ball B(x, r), while the other approach is to calculate the radius of the smallest x-centered ball that encloses some fixed number of points. Either way, one ends up with an estimate of both ln(P (Xi ∈ B(x, r))) and ln(r). Taking multiple measurements, we may get an estimate of d by fitting a line through these measurements, by treating η as a constant. Because η cannot be considered constant when r is large (due to the uneven sampling distribution or the curvature of the manifold), one should ideally work at small scales (small r). On the other hand, when r is too small then the measurements' variance will be high. A good estimator must thus find a good balance between the bias and the variance, making the estimation of the intrinsic dimension a non-trivial problem.

## 2. Algorithm

The core component of our algorithm estimates the dimensionality of the manifold in a small neighborhood of a selected point. This point is then varied and results of the local estimates are combined to give the final estimate.

The local estimate is constructed as follows: Collect the observed data points into Dn = [X1, . . . , Xn]. We shall assume that Xi is an i.i.d. sample that comes from a distribution supported on the manifold M. Define η(x, r) by

$$\mathbb { P } \left ( X _ { i } \in B ( x , r ) \right ) = \eta ( x , r ) r ^ { d } , \quad ( 1 ) \quad \begin{matrix} X ^ { ( k ) } \\ \\ \left \| X ^ { 0 } \right \| \end{matrix}$$

or

$$\ln ( \mathbb { P } \left ( X _ { i } \in B ( x , r ) \right ) ) = \ln ( \eta ( x , r ) ) + d \ln ( r ) , \quad ( 2 ) \quad \text {neigh} \quad \sigma _ { 0 } \colon$$

where B(x, r) ⊂ RD is a ball around the point x ∈ M in the Euclidean space RD. Our main assumption in the paper will be that in a small neighborhood of 0 the function η(x, ·) is slowly varying (the assumptions on η will be made precise later). This is obviously satisfied in the commonly studied simple case when the distribution of the data on the manifold is uniform and the manifold satisfies standard regularity assumption such as those considered by Hein et al. (2006).

There are two ways of using Equation (2) for estimating the dimension d. Both rely on the observation that this equation is linear in d. One approach is to fix a radius and count the number of data points within In this paper we study an algorithm in which we fix the "scale" by fixing the number of neighbors, k: the dimension is estimated from the distance to the kth nearest neighbor. In the other approach, i.e., when a scale h = hn is selected, the typical requirement is that hdn → ∞, or hn = Ω(n−1/d). Given that d is unknown this suggests to choose hn = Cn−1/D. This choice, however, is too conservative and would not lead to a dimension adaptive procedure.3 On the other hand, for the consistency of k-nearest neighbor procedures one typically requires only kn/n → 0 and kn → ∞ (these conditions are independent of d). Therefore we prefer nearest-neighbor based techniques for this task.

2Due to the lack of space, we cannot attempt to give a full review of existing work on dimension estimation. The interested reader may consult the papers of Kegl (2002) and Hein and Audibert (2005) which contain many further pointers.

In order to be more specific about the method, let X(k)(x) be the reordering of the data such that = y xoj sp[o||x − (x)(τ+x)X|| &gt; ||x − (x)(x)X|| 1, 2, . . . , n − 1 (ties are broken randomly). Here  · ∥ denotes the l2-norm of RD. Hence, X(1)(x) is the nearest neighbor of x in Dn, X(2) is the 2nd nearest neighbor, etc. Let p(k)(x) = ∥X(k)(x) − x|| be the distance to the kth nearest neighbor of x. In our theoretical analysis, for the sake of proofs simplicity, we use the following simple estimation method: Take k &gt; 2. Denoting η(x, r) ≈ η0, from (2) we have

$$\ln ( k / n ) \ & \approx \ \ln ( \eta _ { 0 } ) + d \ln ( \hat { r } ^ { ( k ) } ( x ) ) , \\ \ln ( k / ( 2 n ) ) \ & \approx \ \ln ( \eta _ { 0 } ) + d \ln ( \hat { r } ^ { ( \lceil k / 2 \rceil ) } ( x ) ) ,$$

since if n is big, P (X0 ∈ B(x, p(k)(x))) should be close to k/n. Reordering the above equations for d, we get

$$\hat { d } ( x ) = \frac { \ln 2 } { \ln ( \hat { r } ^ { ( k ) } ( x ) / \hat { r } ^ { ( | k / 2 | ) } ( x ) ) } .$$

When a center is selected from data, this point is naturally removed when calculating the point's nearest neighbors. With a slight abuse of notation, the estimate when selecting center Xi is also denoted by â(Xi).

3Of course, other options, such as using splitting or cross-validation to select h are also possible. We leave it for future work to study such algorithms.


<!-- p:3 -->


When used at a single random data point, the variance of the estimate will be high and due to k  n the available data is used in a highly inefficient manner. One idea is to compute the estimate at all data points and combine the results. The simplest method is to use averaging:

$$\hat { d } _ { a v g } = \left [ \frac { \sum _ { i = 1 } ^ { n } ( \hat { d } ( X _ { i } ) \wedge D ) } { n } \right ] . \quad \quad ( 4 ) \quad \quad \ A s$$

Here a ∧ b = min(a, b) and [x] denotes the rounded value of x (recall that the estimated dimension is a positive integer number smaller than or equal to D). Another option is to let the estimates vote:

$$\hat { d } _ { v o t e } = \arg \max _ { d ^ { \prime } \in \mathbb { N } ^ { + } } \, \sum _ { i = 1 } ^ { n } \mathbb { I } _ { \{ \hat { d } ( X _ { i } ) = d ^ { \prime } \} } . \quad \text { } \quad ( 5 ) \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { } \quad \text { }$$

Here N+ stands for the set of positive integers.

## 3. Main Results

The purpose of this section is to show that the procedure described in the previous section is manifoldadaptive. Let ηmin = infx∈M η(x, 0). In what follows we will assume that the following holds:

Assumption 1. (1) The constant ηmin is positive. (2) For any point x ∈ M, η(x, r) as a function of r is continuous and differentiable at any r &gt; 0 and rightdifferentiable at r = 0. (3) There exists a positive number B′, such that for any (x, r) ∈ M × [0, ro), |prη(x, r)| ≤ B'η(x, r).4(4) There exist r0 &gt; 0 and ∂ B &gt; 0 such that η satisfies |η(x, r) − η(x, 0)| ≤ Bη(x, 0)r, where (x, r) ∈ M × [0, r0) is arbitrary.

Since ηmin &gt; 0, the manifold has to be bounded. Thus the first condition on the partial derivative of η implies the second relative Lipschitzness condition when η satisfies some additional smoothness assumptions. Assumption 1 is not very restrictive: All it says is that the sampling distribution should be wellbehaving in the sense that it should not change too fast. This assumption is satisfied e.g. if η is uniform on M and if M is sufficiently regular. Define η(x, r) = min{η(x, r′) |0 ≤ r′ ≤ r}. From the above assumption, it is easy to see that η(x, r) ≥ η(x, 0)(1 − Br) holds for any 0 ≤ r &lt; r0 &lt; 1 and x ∈ M.

The following theorem is the main result of the paper: Theorem 1. Consider the estimate â(X1). Then under Assumption 1 provided that n ≥ ck2d, with probability at least 1 − δ

4For r = 0 we take the right-sided derivative of η here.

$$\text {i} a n c e \quad | \hat { d } ( X _ { 1 } ) - d | \leq \mathbb { E } \left [ C ( X _ { 1 } ) \right ] d \left ( B \left ( \frac { k } { n } \right ) ^ { \frac { 1 } { a } } + \sqrt { \frac { \ln ( 4 / \delta ) } { k } } \right ) , \\ \text {ninner} . \\ \text {points} \quad \text {where } C ( x ) = C ^ { \prime } ( ( n _ { \min } ) ^ { - \frac { 1 } { a } } \wedge n ( x _ { 0 } ) ^ { - \frac { 1 } { a } } ( \frac { 1 } { a } + 2 \frac { 1 } { a } ) ) + C ^ { \prime \prime }$$

where C(x) = C′((ηmin)−a ∧ η(x, 0)−a (− + 2a)) + C′ and where C′ and C" are universal constants that do not depend on d, D, k, n, δ and the distribution of X1.

As promised, the proposed method is manifoldadaptive: the estimate's convergence rate only depends on the intrinsic dimension of the manifold and not the embedding space dimension RD.

The first term of (6) bounds the bias of the estimate. By making k small, the bias can be held small. However, a small k makes the second term, which bounds the variance, large. The choice of k that optimizes the bound is k = n2/(2+d) , giving rise to the rate n−1/(2+d). Since d is not available, we may e.g. choose k = n1/2 giving the rate O(n−^1).

Since d is discrete valued when the upper bound of the left-hand-side of (6) becomes smaller than 1/2, then by rounding the estimate, â(X1), we get d. This gives rise to the following corollary:

Corollary 2. Assume that the conditions of Theorem 1 are satisfied and k/n &lt; (2Bcd)−d, where c = E [C(X1)]. Then

$$\begin{array} { r l } { i g h t - } & \mathbb { P } \left ( [ \hat { d } ( X _ { 1 } ) ] \neq d \right ) \leq 4 \exp \left ( - k \left ( \frac { 1 } { 2 c d } - B \left ( \frac { k } { n } \right ) ^ { \frac { 1 } { n } } \right ) ^ { 2 } \right ) . } \\ { , r _ { 0 } ) , } \\ { a n d } \\ { | \right ] \, \leq } \end{array}$$

Although the probability of error decays exponentially fast, the result is only valid (just like the previous result) when the number of samples is large. The exponential behavior of this condition in d is because the algorithm uses estimates of balls volume of radii r and r/2 with small r: In d dimensions, if we have less than (1/r)d uniform random points in a unit cube centered around the origin, the expected number of points in the ball B(0, r) is smaller than one. Thus we need at least (2/r)d &gt; 2d points if we want to have at least one point inside the radius r/2 ball. Also the factor (1/d) is the result of the unevenness of the data distribution.

Now, let us consider the global estimates davg and âvote. Using McDiarmid's version of the HoeffdingAzuma inequality (McDiarmid, 1989; Hoeffding, 1963; Azuma, 1967) and a counting argument relying on the covering of the manifold by cones (essentially adopting the argument of Stone (1977) to manifolds) and under very weak assumptions on the manifold both estimates can be shown to enjoy exponentially fast rates5 . In particular, for some universal constants c, c', c" &gt; 0, we have


<!-- p:4 -->


$$\mathbb { P } \left ( \hat { d } _ { v o t e } \neq d \right ) \ \leq \ e ^ { - \frac { c ^ { \prime } n } { ( c ^ { d } k ) ^ { 2 } } } , \quad ( 8 ) \quad \text {Lem}$$

$$\mathbb { P } \left ( \hat { d } _ { a v g } \neq d \right ) \ \leq \ e ^ { - \frac { c ^ { \prime \prime } n } { ( D c ^ { d } k ) ^ { 2 } } } .$$

From these bounds we can conclude that voting should be preferred since in the case of the averaging bound the rate of convergence depends on D (though only in a very mild, polynomial way). However, our experimental results seems to suggest that the estimate for the averaging method is probably too conservative aoe o oe r  ou   t aet least for the particular dataset and choice of parameters that we considered.

Due to the lack of space the proof of this statement is deferred to the full version of this paper, but the proof of Theorem 1 which is the key to this proof as well is given in the next section.

## 4. Proofs

Theorem 1 is proven in a series of lemmas. First, let us remark that due to the independence of samples, it suffices to show the result for any deterministically selected point x ∈ M. Hence, in what follows we will consider this case. For the sake of brevity we shall suppress the dependence on x in the rest of this section.

Let p = k/n. By the triangle inequality,

$$| d - \hat { d } | \leq | d - d ( p ) | + | d ( p ) - \hat { d } | . \quad ( 1 0 ) \quad \text {Lem} .$$

Here d(p) is defined by

$$d ( p ) = \frac { \ln 2 } { \ln ( r _ { p } / r _ { p / 2 } ) } .$$

By (2), if η(x, rp) = η(x, rp/2) were hold true then d(p) = d would hold. Hence, the source of the error |d − d(p)| is the change in η in the neighborhood of x. By Assumption 1 on η, we can make this error controllable.

The following statement follows by elementary considerations (the proofs of these lemmas are given in the appendix):

Lemma 1. |d − d(p)| ≤ C Bdrp provided that rp &lt; (0.2/B) ∧ r0. Here C ≤ 8 is a universal constant.

It is easy to see that rp ≤ (ηmin)−1/d(k/n)1/d. When the density is non-uniform this estimate might be very conservative. We prefer a bound that depends on the properties of the density in the vicinity of x. Using the observation stated after Assumption 1, we get the following result:

5Bounded curvatures and that the manifold is not selfapproaching are the main assumptions.

Lemma 2. Assume that Brp &lt; (0.5 ∧ r0). Then

$$r _ { p } \leq ( ( \eta _ { \min } ) ^ { - \frac { 1 } { d } } \wedge \eta ( x , 0 ) ^ { - \frac { 1 } { d } } \left ( \frac { 1 } { 2 } + 2 ^ { \frac { 1 } { d } } \right ) ) \left ( \frac { k } { n } \right ) ^ { \frac { 1 } { d } } .$$

Chaining the inequalities of Lemma 1 and Lemma 2 we get that |d − d(p)| ≤ CdBrp ≤ C((ηmin)−a ∧ η(x, 0)−a (− + 2a))Bd (k) 11d

The second term of (10), |d(p) − d|, is bounded by relating it to the relative errors of estimating rp by p(k) (and rp/2 by τ([k/2])).

Lemma 3. If d(p)′ is defined by d(p)′ ln(2)/ln(r′/rp/2) for some positive quantities rp and rp/2 then for

$$\alpha = \max \left ( \left | \frac { r _ { p } ^ { \prime } } { r _ { p } } - 1 \right | , \left | \frac { r _ { p / 2 } ^ { \prime } } { r _ { p / 2 } } - 1 \right | \right ) , \\ | d ( p ) - d ( p ) ^ { \prime } | \leq C d ^ { 2 } \alpha \\ \text {provided that } \alpha \leq c / d \, \text {and} \, r _ { p } \leq ( 0 \, 2 \, / \, R ) \, \triangle r _ { 0 } \, \text {where} \, c$$

provided that α ≤ c/d and rp &lt; (0.2/B) ∧ r0, where c is a fxed universal constant.

Again, the proof of this lemma uses elementary analysis. By this lemma, in order to get a bound on |d(p) − â|, we need to analyze the relative error of estimating rp by p(k). We get the following lemma by using Assumption 1.

Lemma 4. Assume that rp &lt; (4B′)−1 ∧ r0 and α ≤ 1/(4(d + 1)). Then

$$\mathbb { P } \left ( \hat { r } ^ { ( k ) } \leq r _ { p } ( 1 - \alpha ) \right ) \leq \exp ( - C _ { 1 } k \alpha ^ { 2 } ( d - \frac { 1 } { 4 } ) ^ { 2 } ) \ \ ( 1 3 )$$

$$\mathbb { P } \left ( \hat { r } ^ { ( k ) } \geq r _ { p } ( 1 + \alpha ) \right ) \leq \exp ( - C _ { 2 } k \alpha ^ { 2 } ( d - \frac { 1 } { 4 } ) ^ { 2 } ) \ \ ( 1 4 )$$

$$\begin{array} { r l } & { e \text { then } } & { w h e r e \text { } C _ { 1 } = \frac { 3 } { 8 } ( 1 - \frac { d - 2 } { 4 ( d + 1 ) } ) ( 1 - \frac { 3 } { 1 6 ( d + 1 ) } ) , \, C _ { 2 } = \frac { 3 e } { 8 } \frac { 1 / 4 } { 1 - } ( 1 - } \\ & { e o d o f } & { \frac { 1 } { 8 ( d + 1 ) } ) ( 1 - \frac { 1 } { 1 6 ( d + 1 ) ( d - 1 / 4 ) } ) ^ { 2 } . } \end{array}$$

The proof of this lemma relies on Bernstein's inequality. According to these bounds, with probability at least 1 − δ,

$$\max \left \{ \left | \frac { \hat { r } ^ { ( k ) } } { r _ { p } } - 1 \right | , \left | \frac { \hat { r } ^ { ( \lceil k / 2 \rceil ) } } { r _ { p / 2 } } - 1 \right | \right \} \leq C _ { 3 } \frac { 1 } { d } \sqrt { \frac { \ln ( 4 / \delta ) } { k } }$$

with a suitable universal constant C3. Hence,

$$| d - \hat { d } | \leq C ( x ) d \left ( B \left ( \frac { k } { n } \right ) ^ { \frac { 1 } { d } } + \sqrt { \frac { \ln ( 4 / \delta ) } { k } } \right )$$

holds with probability at least 1 −δ, which proves Theorem 1.


<!-- p:5 -->


art  ot    e   s rs  t s  r  ss t rsest is for the averaging method, while those in parentheses are for the voting method.

| Data set    | n=50    | n=100     | n=500     | n=1000    | n=5000    |
|-------------|---------|-----------|-----------|-----------|-----------|
| S 1         | 98 (99) | 100 (100) | 100 (100) | 100 (100) | 100 (100) |
| S 3         | 75 (19) | 95 (20)   | 100 (15)  | 100 (19)  | 100 (62)  |
| S 5         | 33 (5)  | 50 (10)   | 100 (9)   | 98 (2)    | 100 (0)   |
| S 7         | 18 (2)  | 17 (3)    | 57 (1)    | 54 (1)    | 100 (0)   |
| Sinusoid    | 92 (98) | 100 (100) | 100 (100) | 100 (100) | 100 (100) |
| 10-M ̈ obius | 69 (47) | 13 (74)   | 100 (98)  | 100 (99)  | 100 (100) |
| Swiss roll  | 62 (71) | 49 (91)   | 88 (96)   | 100 (100  | 100 (100) |

## 5. Experimental Results

The purpose of this section is to provide some experimental evidence on the performance of our algorithm. We investigated the influence of the following factors: (i) number of samples (n), (ii) the manifold's dimension (d) (iii) the embedding space's dimensionality (D), (iv) the number of centers used when combining the local estimates (m)6, (v) the number of neighbors (k), and (vi) the noise level. Due to the lack of space here we only present results for (i)−(iii). The other results will be given in the longer version of this paper, here we remark only that according to our experience the algorithm's performance degrades gracefully when noise, not respecting the manifold is added to the data. Noise is the Achilles heel of manifold-aware algorithms as it changes the support of the sampling distribution. We leave it for future work to study the behaviour of manifold-aware algorithms in the presence of noise.

The default setting of the parameters are m = n/2 and k = [2 ln n]. These parameter settings were used in all the experiments.7 Except for the real-world dataset, we performed the measurements by repeating the calculations 100 times, for 100 different randomizations of the datasets considered. We report average errors and the percentages when a correct estimate was obtained.

The datasets used were essentially identical to those used by Hein and Audibert (2005), i.e., they include some standard datasets such as spheres of various dimensionality and some high-curvature datasets for which dimension estimation is quite challenging.

6In the theoretical analysis we assumed that m = n (see Equations (4) and (5)). However, one can also select datapoints participating in the computation in a random fashion (by sampling data points uniformly with replacement). The hope is that an equivalently good estimate can be obtained by less work.

7Note that according to the theory developed this choice of k is inferior to e.g. k = n1/2. However, k = O(ln n) yields much less computation and was therefore preferred in the experiments.

In the case of shperes the data points are sampled uniformly from a d-dimensional sphere Sd embedded in Rd+1. The sinusoid dataset is a one dimensional oscillating sinusoid on the circle in R3. The data points come from the manifold M = (sint (she ({( ' l 3 n ((nt)is (n)s'(n) h)} samples are obtained by drawing random points uniformly at random in the interval [0,2π). The 10Möbius strip is a two dimensional submanifold in R3, created by twisting a two dimensional rectangle 10 times. Data points are obtained by sampling points (U, V) uniformly on [−1, 1] × [0, 2π) and returning x1(U, V) = (1 + U cos(5V))cos(V), x2(U, V) = U2 sin(5V). We used two other datasets: "Swiss roll" and the ISOMAP Face datset. The Swiss roll is a two dimensional manifold embedded in R3 (Levina and Bickel, 2005). ISOMAP Face consists of 698 64 × 64 images (256 gray levels) of a face sculpture (Tenenbaum et al., 2000). For this dataset we obtained an estimate of four when using davg, while we got an estimate of 3 when using dvote. Earlier results by others suggest that the intrinsic dimensionality is 3.

Results for the different artificial datasets when the number of data points (n) is varied are given in Table 1. As expected, the number of samples required for an accurate estimate increases with the intrinsic dimension of the manifold. We can conclude that (at least for the parameter settings considered) the averaging method performs better than the voting method. In particular, voting seems to have troubles when the number of datapoints is small or the intrinsic dimension is higher. Therefore in what follows we consider only the averaging method. Overall the performance seems comparable to those reported by Hein and Audibert (2005).

Figure 1 shows the average absolute error measured as the number of samples for S4 and S8. It turns out that the error behave roughly as O(n−c/d) with c = 2.4.


<!-- p:6 -->


Figure 1. Average absolute error of the dimension estimate for different sample sizes for S4 and S8. Note the logarithmic scales. The straight lines show lines fitted to the measured curves.

S4

8S

Mean Absolute Dimension Estimation Error

10°

101

10^{2

10{3

104

Number of Samples

One crucial property of our bounds is that they do not depend (explicitly) on the dimension of the embedding space RD. In order to test this we picked the 10-Möbius dataset and added additional dimensions ("features") to it by using two functions, φ1 and φ2.8 The results for the original manifold and M1, M2 are shown in Figure 2. We see that the behavior of the error-curves is almost identical in all three cases9.

This figure reinforces us in that, as predicted by the theory, the embedding dimension has essentially no effect on the quality of estimates.

## 6. Conclusions

In this paper, we introduced an algorithm for estimating the intrinsic dimension of a manifold, and analyzed its finite-sample convergence properties. We showed that the method is manifold-adaptive: the convergence behavior of the method is determined by the dimension of the manifold, and not the dimension of the embedding space. In addition to the theoretical analysis, we examined our method on several test problems. It was shown that the performance of the method is compara- Number of Samples ble to other works. As for future work, it would be interesting to prove manifold-adaptivity results for other learning problems, such as regression or classification. Another interesting open question is if manifold learning can succeed at all in the presence of noise.

8In particular, we let φ1 : R3 → R6 defined by φ1(x) = (x, sin(x)), and φ2 : R3 → R12 defined by φ2(x) = (x, sin(x), x2, x3). Clearly, Mj = {φj(x) |x ∈ M} has the same dimensionality as M (j = 1, 2), but the extrinsic dimensionality of the data points, Xi = φ1(Xi), Xi = φ2(Xi) is increased.

10°

X (D = 3)

X (D = 6)

X"(D = 12)

Mean Absolute Dimension Estimation Errors

10^{1

10

100

1000

10000 20000

Figure 2. The effect of extrinsic dimension on the mean absolute dimension estimation error for 10-Möbius problem. For more information see the text.

#### Acknowledgments

Csaba Szepesvári greatly acknowledges the support received through the Alberta Ingenuity Center for Machine Learning (AICML) and the Computer and Automation Research Institute of the Hungarian Academy of Sciences.

### A. Proof of Lemma 1

We will need the following result that we state without a proof :

$$\begin{array} { r l } & { \text {nowed} } & { \quad \text {1} } \\ & { \text {regence} } & { \quad \text {Proposition } 5 . \ I f \ x < 1 \ t h e n \ 2 x \leq \ln ( ( 1 + x ) / ( 1 - \text {epsilon} ) ) \leq 0 } \\ & { \text {version} } & { \quad x ) \leq \frac { 2 x } { ( 1 - x ) ( 1 + x ) } . } \end{array}$$

We need to prove the following: Let p &gt; 0 and assume that rp ≤ 0.2/B. Then for d(p) = ln(2)/ ln(rp/rp/2), |d − d(p)| ≤ CdBrp, where C ≤ 8.

Proof. Let r1 = rp, r2 = rp/2 and η1 = η(x, rp), η2 = η(x, rp/2). Note that d = (ln(2)+1n(η1/η2))/ ln(r1/r2). Hence |d − d(p)| = ln(η1/η2)/ln(r1/r2) and thus we plan to upper bound the numerator and lower bound the denominator.

Let η0 = η(x, 0). By Assumption 1, η1/η2 ≥ η0(1 − Br1)/(η0(1 + Br2)) ≥ (1 − Br1)/(1 + Br1). Similarly,

9The differences in the case of the points (Xi') can probably be explained by the additional curvature introduced by the non-linear functions.


<!-- p:7 -->


η1/η2 ≤ (1 + Br1)/(1 − Br1). Since by assumption Br1 ≤ 0.2, taking logarithms and using the upper bound in Proposition 5 we get

$$| \ln ( \eta _ { 1 } / \eta _ { 2 } ) | \leq \frac { 2 B r _ { 1 } } { ( 1 - B r _ { 1 } ) ( 1 + B r _ { 1 } ) } . \quad ( 1 5 ) \quad \begin{matrix} 2 / \ln \\ \frac { 2 \ln ( 1 + B r _ { 1 } ) } { \left ( 1 - B r _ { 1 } \right ) ( 1 + B r _ { 1 } ) } . \quad ( 1 5 ) \\ \end{matrix} \quad \begin{matrix} 2 \ln ( 1 + B r _ { 1 } ) \\ \frac { 2 \ln ( 1 + B r _ { 1 } ) } { \left ( 1 + B r _ { 1 } \right ) } . \quad ( 1 5 ) \\ \end{matrix}$$

Now, using the identities p = η1r1, p/2 = η2r2 we get (r1/r2)d = 2 η2/η1 ≥ 2(1 − Br1)/(1 + Br1). Taking logarithms and using the lower bound in Proposition 5 we get d ln(r1/r2) ≥ ln 2 − 2Br1/((1 − Br1)(1 + Br1)). Combining the inequalities obtained gives |d − d(p)| ≤ 2dBr1/((1 − Br1)(1 + Br1) ln 2 − 2Br1). Using the assumption r1 = rp ≤ 0.2/B allows us to lower bound the denominator here by a constant, yielding the final result. □

### B. Proof of Lemma 2

Proof. Since p = k/n = η(x,rp)rd, rp (η(x, rp))−a (k/n)a ≤ (n(x, rp))−a (k/n)a ≤ (η(x, 0)(1 − Brp))−a (k/n)a, where we have used that Brp &lt; 1. Using the elementary ins  x+1 + 1  p/1−-(x − 1) ds for 0 ≤ x ≤ 0.5 and assuming that Brp ≤ 0.5 we get rp ≤ (k/n)aη(x, 0)−a(1 + 21+a)Brp ≤ (k/n)aη(x, 0)−a(1 + 21+a)/2. Also, from rp = (η(x, rp))−a (k/n)a we get rp ≤ (ηmin)−a (k/n)a. Combining this with the previous inequality for rp gives the result. □

### C. Proof of Lemma 3

p/2 1). The lemma states Let α = max -1 rp rp/2 that |d(p) − d(p)′| ≤ Cd2α provided that rp ≤ 0.2/B and α &lt; 0.5.

rp/2 1 + α and ≥ 1 − α. Hence, since by assumption rp/2 ·((x − 1)/( + 1))I (2)I/1 = (d)a − ,(d)a 1 &gt; p Using Proposition 5, we thus get e(p)' − e(p) = 2/ 1n(2) α/((1 + α)(1 − α). Since (1 + α)(1 − α) is decreasing in α, we may upper bound the right-hand side by Cα with an appropriate positive constant C, thus finishing the proof. □

### D. Proof of Lemma 4

Introduce λ(x, r) = P (X1 ∈ B(x, r)). Since x is fixed, in what follows for the sake of brevity we will drop x from the arguments of λ. Similarly, we drop x from η(x, r). We need the following properties of λ:

Proposition 6. Let r &gt; 0, 0 ≤ ε &lt; r, 0 ≤ α &lt; 1. The following inequalities hold for λ:

$$\lambda ( r ) - \lambda ( r - \epsilon ) \ \geq \ \eta ( r ) ( 1 - B ^ { \prime } \epsilon ) ( r - \epsilon ) ^ { d - 1 } ( d - B ^ { \prime } r ) \epsilon , \\ = \intertext { r _ { p } } < \sum _ { \substack { 1 \\ 2 } } ( 1 )$$

$$\begin{array} { r l r } { \frac { 1 } { d } } & { \leq } & { \lambda ( r + \epsilon ) - \lambda ( r ) \, \geq \, \eta ( r ) ( 1 - B ^ { \prime } \epsilon ) r ^ { d - 1 } ( d - B ^ { \prime } ( r + \epsilon ) ) \epsilon , } \\ { h a v e } & & { ( 1 8 ) } \\ { r y i n - } & & { ( 1 ) ( 1 - ( 1 + \eta ) ) \, \geq \, 0 \, ( 1 ) ( 1 - ( 1 + D ^ { \prime } \eta ^ { \prime } ) ( 1 + \eta ^ { \prime } D ^ { \prime } ) ) } \end{array}$$

$$\lambda ( r ( 1 - \alpha ) ) \ \geq \ \lambda ( r ) ( 1 - \alpha ( 1 + B ^ { \prime } \alpha r ) ( d + B ^ { \prime } r ) ) , \\ 0 . 5 \\$$

$$\lambda ( r - \epsilon ) \ \leq \ \eta ( r ) ( 1 + B ^ { \prime } \epsilon ) ( r - \epsilon ) ^ { d } , \quad ( 2 0 )$$

$$\lambda ( r + \epsilon ) \ \leq \ \eta ( r ) ( 1 + B ^ { \prime } \epsilon ) ( r + \epsilon ) ^ { d } . \quad ( 2 1 )$$

Proof. Note that (18) follows immediately from (17). Inequalities (20),(21) follow directly from λ(r) = η(r)rd and Assumption 1. Hence, it remains to prove (17) and (19). Let us start with (17).

Since η is differentiable, λ(r) = η(r)rd is differentiable, too. Further, λ′(r) = η′(r)rd + η(r)drd−1 and hence using Assumption 1, η(r)rd−1(d − B′r) ≤ λ′(r) ≤ η(r)rd−1(d + B′r).

Proof. Let e(p) = 1/d(p), e(p)' = 1/d(p)′. Let ∈ = |d(p) − d(p)′|, γ = |e(p) − e(p)′|. Then ∈ = |d(p) − d(p)'| = e(p) e(p), = d(p)d(p)' γ ≤ d(p)(d(p) + e)γ. Ordering this for €, provided that γd(p) &lt; 1 we get that ε ≤ γd(p)2/(1 − γd(p)). Since by Lemma 1, d(p) ≤ d + CdBrp, assuming that dγ(1 + Brp) &lt; 1 we may further bound € by

$$\epsilon \leq \gamma d ^ { 2 } \frac { ( 1 + C B r _ { p } ) ^ { 2 } } { 1 - \gamma d ( 1 + C B r _ { p } ) } .$$

Hence it suffices to show that γ ≤ Cα since then for α sufficiently small the denominator can be bounded from below with a positive constant and the whole expression will be bounded by O(d2α) as promised.

By the definition of e(p) and e(p)′, e(p)′ − e(p) 1/ 1n(2) ln(( p/2 )). By the definition of α, rp V rp (rp/2 rp Let 0 &lt; a, b, v = a ∧ b, u = a ∨ b. Since by assumption λ is differentiable in (v, u) and continuous on [v, u], by the Mean-Value Theorem, λ(a) − λ(b) = λ′(ξ)(a − b) where ξ is some number in (v, u). Using the bound derived for λ′, with the choice a = r, b = r − ∈ we get λ(r) − λ(r − €) = λ′(ξ)∈ ≥ η(ξ)ξd−1(d − B′ξ) for some ξ ∈ (r − €, r). Using η(ξ) ≥ η(r)(1 − B′€) which holds by Assumption 1, we get λ(r) − λ(r − €) ≥ η(r)(1 − B′€)(r − ∈)d−1(d − B′r), which proves (17).

Let us show (19). Let ε = αr. By Taylor's theorem there exists ξ ∈ (r − ∈, r), such that λ(r − €) = λ(r) − λ′(ξ)∈. Hence, λ(r − ∈) ≥ λ(r) − η(ξ)ξd−1(d + B′ξ)∈ ≥ λ(r) − η(r)(1 + B′€)rd−1(d + B′r)αr = λ(r)(1 − α(1 + B′αr)(d + B′r)), where we have used the bound on λ′ and Assumption 1. □

Now, let us prove Lemma 4.


<!-- p:8 -->


Proof. Let r′ &lt; rp be some positive number. Then

$$1 \, 6 0 j \colon L C 1 _ { p } & < I _ { p } \ B C B { \text {66} } . \, 1 \, 1 6 \, 0 \, 1 \, 1 \, 0 \, 1 \, \frac { 1 } { 2 } \, \text {we have} \, \frac { B ^ { \prime } r _ { p } \alpha ) r _ { p } ^ { 2 } } { 2 } \\ & \mathbb { P } \left ( \hat { r } ^ { ( k ) } \leq r _ { p } ^ { \prime } \right ) = \mathbb { P } \left ( \sum _ { i = 1 } ^ { n } \mathbb { I } _ { \{ X _ { i } \in B ( x , r _ { p } ^ { \prime } ) \} } \geq k \right ) & \text {is upper} \\ & = \mathbb { P } \left ( \frac { 1 } { n } \sum _ { i = 1 } ^ { n } \mathbb { I } _ { \{ X _ { i } \in B ( x , r _ { p } ^ { \prime } ) \} } - \lambda ( r _ { p } ^ { \prime } ) \geq k / n - \lambda ( r _ { p } ^ { \prime } ) \right ) & \quad 1 ) ) ^ { 4 ( d + 1 ) } \\ & \leq \exp \left ( - \frac { n } { 2 } F ( \lambda ( r _ { p } ) , \lambda ( r _ { p } ^ { \prime } ) ) \right ) , & \quad ( 2 2 ) & \text {pont} \ e q \\ & \text {where} \ F ( \lambda _ { 1 } , \lambda _ { 2 } ) = ( \lambda _ { 1 } - \lambda _ { 2 } ) ^ { 2 } / ( \lambda _ { 2 } ( 1 - \lambda _ { 2 } ) + \frac { 1 } { 2 } ( \lambda _ { 1 } - \lambda _ { 2 } ) ) ,$$

where F (λ1, λ2) = (λ1 − λ2)2/(λ2(1 − λ2) + 1 (λ1 − λ2)). The last inequality in (22) follows from Bernstein's inequality thanks to k/n − λ(rp) = p − λ(rp) = λ(rp) − λ(rp) &gt; 0 and Var [I{x1∈B(x,r)}] = λ(r)(1 − λ(r)). Similarly, if rp &gt; rp then

$$\mathbb { P } \left ( \hat { r } ^ { ( k ) } \geq r _ { p } ^ { \prime } \right ) \leq \exp \left ( - \frac { n } { 2 } \, F ( \lambda ( r _ { p } ^ { \prime } ) , \lambda ( r _ { p } ) ) \right ) . \quad ( 2 3 )$$

Choose r′ = rp(1 − α). Then (22) gives an upper bound on P (p(k) ≤ rp(1 − α)). We further bound this by lower bounding the numerator of F(λ(rp), λ(rp)) and upper bounding its denominator. For the (d,t) − (d,)   (2r) s   I n(rp)(1− B'αrp)rd−1(1−α)d−1(d− B'rp)rpα = α(1− α)d−1rpdη(rp)(1 − B′αrp)(d − B′rp). The first term in the denominator is upper bounded by λ(rp) (since 1 − λ(rp) ≤ 1). We now show that the second term can be bounded from above by λ(rp) thanks to the assumptions α ≤ 1/(4(d + 1)) and B′rp ≤ 1. Indeed, by (19) of Proposition 6, λ(rp(1−α)) ≥ λ(rp)(1−α(1+ B′αrp)(d + B′rp)) ≥ 1/2λ(rp), where the last inequality follows since (1 + B′αrp)(d + B′rp) ≤ 2(d + 1). Hence, the denominator can be upper bounded by 4/3λ(rp). Now using (20), this can be further upper bounded by 4/3η(rp)(1 + B′rpα)(rp(1 − α))d. Combining these bounds gives

$$\text {ing these bounds gives} \\ \frac { n } { 2 } F ( \lambda ( r _ { p } ) , \lambda ( r _ { p } ^ { \prime } ) ) & \geq \\ \frac { 3 n } { 8 } \frac { \alpha ^ { 2 } ( 1 - \alpha ) ^ { 2 d } } { \eta ( r _ { p } ) ( 1 + B ^ { \prime } r _ { p } \alpha ) ( r _ { p } ) ^ { 2 } ( d - B ^ { \prime } r _ { p } ) ^ { 2 } } \\ & = \frac { 3 n } { 8 } \, \frac { \alpha ^ { 2 } ( 1 - \alpha ) ^ { d } \, ^ { 2 } ( r _ { p } ) ^ { d } ( r _ { p } ) ( 1 - B ^ { \prime } \alpha r _ { p } ) ^ { 2 } ( d - B ^ { \prime } r _ { p } ) ^ { 2 } } { ( 1 + B ^ { \prime } r _ { p } \alpha ) } \\ & \geq \frac { 3 k } { 8 } \alpha ^ { 2 } ( 1 - \alpha ) ^ { d - 2 } ( 1 - 3 B ^ { \prime } \alpha r _ { p } ) ( d - B ^ { \prime } r _ { p } ) ^ { 2 } \\ & \geq \frac { 3 k } { 8 } \alpha ^ { 2 } ( 1 - ( d - 2 ) \alpha ) ( 1 - 3 B ^ { \prime } \alpha r _ { p } ) ( d - B ^ { \prime } r _ { p } ) ^ { 2 } \\ & \geq \frac { 3 k } { 8 } \alpha ^ { 2 } ( 1 - ( d - 2 ) \alpha ) ( 1 - \frac { 3 } { 1 6 ( d + 1 ) } ) ( d - \frac { 1 } { 4 } ) ^ { 2 } \\ \text {where to get the first inequality we used (1 - x ) / (1 + \text { } P e } }$$

where to get the first inequality we used (1 − x)/(1 + (x − 1)(x − 1) 0 &lt; x 1   x − 1  (x (1 − 3x), and η(rp)rd = p = k/n, which holds thanks to the definition of rp. In the last inequality we used the assumption B′rp &lt; 1/4 and α &lt; 1/(4(d+ 1)). This finishes the proof of the bound of (13).

For bounding P (p(k) ≥ rp(1 + α)) we start with (23). Again, we lower bound the numerator. This time, we use (18) to get λ(rp(1 + α)) − λ(rp) ≥ η(rp)(1 − B′rpα)rd(d−B′(rp(1+α)))α. The denominator of (23) is upper bounded by 4/3λ(rp(1 + α)) ≤ 4/3η(rp)(1 + B'rpα)(rp(1+α))d ≤ 4/3η(rp)(1+B'rpα)rde1/4, which follows by (21) and since (1 + α)d ≤ (1 + 1/(4(d + 1)))(d+1)×(d+1) ≤ el/(4+1/d) ≤ e1/4. Hence, the exponent of (23), n/2F(λ(rp), λ(rp)), is bounded from below by

$$\begin{array} { r l } & { 0 . } \\ & { 0 ^ { s } } & { \frac { 3 n } { 8 } \frac { ( \eta ( r _ { p } ) ( 1 - B ^ { \prime } r _ { p } \alpha ) r _ { p } ^ { d } ( d - B ^ { \prime } ( r _ { p } ( 1 + \alpha ) ) ) \alpha ) ^ { 2 } } { \eta ( r _ { p } ) ( 1 + B ^ { \prime } r _ { p } \alpha ) r _ { p } ^ { d } } } \\ & { \geq } & { \frac { 3 n e ^ { 1 / 4 } } { 8 } \frac { \alpha ^ { 2 } \eta ( r _ { p } ) r _ { p } ^ { d } ( 1 - B ^ { \prime } r _ { p } \alpha ) ( d - B ^ { \prime } ( r _ { p } ( 1 + \alpha ) ) ) ^ { 2 } } { ( 1 + B ^ { \prime } r _ { p } \alpha ) } } \\ & { \geq } & { \frac { 3 k e ^ { 1 / 4 } } { 8 } \alpha ^ { 2 } ( 1 - \frac { 1 } { 8 ( d + 1 ) } ) ( d - \frac { 1 } { 4 } - \frac { 1 } { 1 6 ( d + 1 ) } ) ) ^ { 2 } , } \\ & { 3 ) } & { w h o r o w o w i n v o c d ( 1 - \alpha ) \langle ( 1 + \alpha ) > 1 } & { 2 \alpha - k / r - } \end{array}$$

where we again used (1 − x)/(1 + x) ≥ 1 − 2x, k/n = η(rp)rd, B'rp ≤ 1/4, α ≤ 1/(4(d + 1)). This finishes the proof of (14). □
