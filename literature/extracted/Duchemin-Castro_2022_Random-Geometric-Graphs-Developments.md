---
id: "Duchemin-Castro_2022_Random-Geometric-Graphs-Developments"
source_pdf: "../pdf/Duchemin-Castro_2022_Random-Geometric-Graphs-Developments.pdf"
source_filename: "Duchemin-Castro_2022_Random-Geometric-Graphs-Developments.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "excellent"
extraction_score: 100.0
visual_assets: "disabled"
references_file: "../references/Duchemin-Castro_2022_Random-Geometric-Graphs-Developments.references.md"
---

<!-- p:1 -->

## Random Geometric Graph: Some recent developments and perspectives

##### Quentin Duchemin and Yohann De Castro

Keywords Random Geometric Graphs Concentration inequality for U-statistics Random matrices Non-parametric estimation Spectral clustering Coupling Information inequalities

####### Abstract

The Random Geometric Graph (RGG) is a random graph model for network data with an underlying spatial representation. Geometry endows RGGs with a rich dependence structure and often leads to desirable properties of real-world networks such as the small-world phenomenon and clustering. Originally introduced to model wireless communication networks, RGGs are now very popular with applications ranging from network user profiling to protein-protein interactions in biology. RGGs are also of purely theoretical interest since the underlying geometry gives rise to challenging mathematical questions. Their resolutions involve results from probability, statistics, combinatorics or information theory, placing RGGs at the intersection of a large span of research communities. This paper surveys the recent developments in RGGs from the lens of high dimensional settings and non-parametric inference. We also explain how this model differs from classical community based random graph models and we review recent works that try to take the best of both worlds. As a by-product, we expose the scope of the mathematical tools used in the proofs.

## 1 Introduction

### 1.1 Random graph models

Graphs are nowadays widely used in applications to model real world complex systems. Since they are high dimensional objects, one needs to assume some structure on the data of interest to be able to efficiently extract information on the studied system. To this purpose, a large number of models of random graphs have been already introduced. The most simple one is the Erdös-Renyi model G ( n , p ) in which each edge between pairs of n nodes is present in the graph with some probability p 2 ( 0, 1 ) . One can also mention the scale-free network model of Barabasi and Albert (Barabási, 2009) or the small-world networks of Watts and Strogatz (Watts and Strogatz, 1998). We refer to Channarond (2015) for an introduction to the most famous random graph models. On real world problems, it appears that there often exist some relevant variables accounting for the heterogeneity of the observations. Most of the time, these explanatory variables are unknown and carry a precious information on the system studied. To deal with such cases, latent space models for network data emerged (see Smith et al. (2019)). Ones of the most studied latent models are the community based random graphs where each node is assumed to belong to one (or multiple) community while the connection probabilities between two nodes in the graph depend on their respective membership. The well-known Stochastic Block Model has received increasing attention in the recent years and we refer to Abbe (2018) for a nice introduction to this model and the statistical and algorithmic questions at stake. In the previous mentioned latent space models the intrinsic geometry of the problem is not taken into account. However, it is known that the underlying spatial structure of network is an important property since geometry affects drastically the topology of networks (see Barthélemy (2011) and Smith et al. (2019)). To deal with embedded complex systems, spatial random graph models have been studied such as the Random Geometric Graph (RGG). This paper surveys the recent developments in the theoretical analysis of RGGs through the prism of modern statistics and applications.


<!-- p:2 -->


The theoretical analysis of random graph models is interesting by itself since it often involves elegant and important information theoretic, combinatorial or probabilistic tools. In the following, we adopt this mindset trying to provide a faithful picture of the state of the art results on RGGs focusing mainly on high dimensional settings and non-parametric inference while underlining the main technical tools used in the proofs. We want to illustrate how the theory can impact real data applications. To this end, we will essentially be focused on the following questions:

- Detecting Geometry in RGGs. Nowadays real world problems often involve high-dimensional feature spaces. A first natural work is to identify the regimes where the geometry is lost in the dimension (see Eq.(1) for a formal definition). Several recent papers have made significant progress towards the resolution of this question that can be formalized as follows. Given a graph of n nodes, a latent geometry of dimension d = d ( n ) and edge density p = p ( n ) , for what triples ( n , d , p ) is the model indistinguishable from G ( n , p ) ?
- Non-parametric estimation in RGGs. By considering other rules for connecting latent points, the RGG model can be naturally extended to cover a larger class of networks. In such a framework, we will wonder what can be learned in an adaptive way from graphs with an underlying spatial structure. We will address non-parametric estimation in RGGs and its extension to growth model.
- Connections between RGGs and community based latent models. Until recently, community and geometric based random graph models have been mainly studied separately. Recent works try to investigate graph models that account for both cluster and spatial structures. We present some of them and we sketch interesting research directions for future works.

### 1.2 Brief historical overview of RGGs

The RGG model was first introduced by Gilbert (1961) to model the communications between radio stations. Gilbert's original model was defined as follows: pick points in R 2 according to a Poisson Point Process of intensity one and join two if their distance is less than some parameter r &gt; 0. The Gilbert model has been intensively studied and we refer to Walters (2011) for a nice survey of its properties including connectivity, giant component, coverage or chromatic number. The most closely related model is the Random Geometric Graph where n nodes are independently and identically distributed on the space. A lot of results are actually transferable from one model to the other as presented in (Penrose et al., 2003, Section 1.7). In this paper we will focus on the n points i.i.d. model which is formally defined in the next subsection (see Definition 1). The Random Geometric Graph model was extended to other latent spaces such as the hypercube [ 0, 1 ] d , the Euclidean sphere or compact Lie group Méliot (2019). A large body of literature has been devoted to studying the properties of low-dimensional Random Geometric Graphs Penrose et al. (2003), Dall and Christensen (2002), Bollobás (2001). RGGs have found applications in a very large span of fields. One can mention wireless networks Haenggi et al. (2009), Mao and Anderson (2012), gossip algorithms Wang and Lin (2014), consensus Estrada and Sheerin (2016), spread of a virus Preciado and Jadbabaie (2009), protein-protein interactions Higham et al. (2008), citation networks Xie et al. (2016). One can also cite an application to motion planning in Solovey et al. (2018), a problem which consists in finding a collision-free path for a robot in a workspace cluttered with static obstacles. The ubiquity of this random graph model to faithfully represent real world networks has motivated a great interest for its theoretical study .

### 1.3 Outline

In Section 2, we formally define the RGG and several variant models that will be useful for this article. In Sections 3, 4 and 5, we describe recent results related to high-dimensional statistic, non-parametric estimation and temporal prediction. Note that in these three sections, we will be working with the d - dimensional sphere S d 1 as latent space. S d 1 will be endowed with the Euclidean metric κ κ which is the norm induced by the inner product η , ι : ( x , y ) 2 S d 1 2 7! P d i = 1 x i y i . The choice of this latent space is motivated by both recent theoretical developments in this framework Bubeck et al. (2016), De Castro et al. (2020), Allen-Perkins (2018), Issartel et al. (2021) and by applications Pereda and Estrada (2019), Perry et al. (2020). We further discuss in Section 6 recent works that investigate the connections between community based random graph models and RGGs. Contrary to the previous sections, our goal is not to provide an exhaustive review of the literature in Section 6 but rather to shed light on some pioneering papers.


<!-- p:3 -->

Table 1: Outline of the paper. Models are defined in Section 2.

|   Section | Questions tackled                                   | Model                                               |
|-----------|-----------------------------------------------------|-----------------------------------------------------|
|         3 | Geometry detection                                  | RGG on S d 1                                        |
|         4 | Non-parametric estimation                           | TIRGG on S d 1                                      |
|         5 | Non-parametric estimation & Temporal prediction     | MRGG on S d 1                                       |
|         6 | Connections between community based models and RGGs | Connections between community based models and RGGs |

## 2 The Random Geometric Graph model and its variants

The questions that we tackle here can require some additional structure on the model. In this section, we define the variants of the RGG that will be useful for our purpose. Figure 2 shows the connections between these different models.

### 2.1 (Soft-) Random Geometric Graphs

Definition 1. (Random Geometric Graph: RGG)

Let ( Ξ , ) be a metric space, and m be a Borel probability measure on Ξ . Given a positive real number r &gt; 0 , the Random Geometric Graph with n 2 N νφ 0 γ points and level r &gt; 0 is the random graph G such that

- the n vertices X 1 , . . . , X n of G are chosen randomly in Ξ according to the probability measure m n on Ξ n .

6

- for any i , j 2 [ n ] with i = j, an edge between X i and X j is present in G if and only if ( X i , X j ) r.

We denote RGG ( n , m , ( Ξ , )) the distribution of such random graphs.

Motivated by wireless ad hoc networks, Soft-RGGs have been more recently introduced (see Penrose (2016)). In such models, we are given some function H : R + ! [ 0, 1 ] and two nodes at distance in the graph are connected with probability H ( ) .

Definition 2. (Soft Random Geometric Graph: Soft-RGG)

Let ( Ξ , ) be a metric space, m be a Borel probability measure on Ξ and consider some function H : R + ! [ 0, 1 ] . The Soft (or probabilistic) Random Geometric Graph with n 2 N νφ 0 γ points with connection function H is the random graph G such that

- the n vertices X 1 , . . . , X n of G are chosen randomly in Ξ according to the probability measure m n on Ξ n .

6

- for any i , j 2 [ n ] with i = j, we draw an edge between nodes X i and X j with probability H ( X i , X j ) .

We denote Soft-RGG ( n , m , ( Ξ , )) the distribution of such random graphs.

Note that the RGG model with level r &gt; 0 is a particular case of the Soft-RGG model where the connection function H is chosen as 7! 1 r . The obvious next special case to consider of Soft-RGG is the so-called percolated RGG introduced in Müller and Prałat (2015) which is obtained by retaining each edge of a RGG of level r &gt; 0 with probability p 2 ( 0, 1 ) (and discarding it with probability 1 p ). This reduces to consider the connection function H : 7! p 1 r . Particular common choices of connection function are the Reyleigh fading activation functions which take the form

Figure 1: Venn diagram of the different random graph models.


<!-- p:4 -->


$$H ^ { R a y l e i g h } ( \rho ) = \exp \left [ - \zeta \left ( \frac { \rho } { r } \right ) ^ { \eta } \right ] , \quad \zeta > 0 , \eta > 0 .$$

We refer to Dettmann and Georgiou (2016) and references therein for a nice overview of Soft-RGGs in particular the most classical connection functions and the question of connectivity in the resulting graphs.

### 2.2 Translation Invariant Random Geometric Graphs

One possible non-parametric generalization of the (Soft)-RGG model is given by the W random graph model (see for example Diaconis and Janson (2007)) based on the notion of graphon. In this model, given latent points x 1 , . . . , x n uniformly and independently sampled in [ 0, 1 ] , the probability to draw an edge between i and j is i , j : = W ( x i , x j ) where W is a symmetric function from [ 0, 1 ] 2 onto [ 0, 1 ] , referred to as a graphon. Hence, the adjacency matrix A of this graph satisfies

$$\forall i , j \in [ n ] , \ A _ { i , j } \sim B e r ( \Theta _ { i , j } ) ,$$

where for any p 2 [ 0, 1 ] , Ber ( p ) is the Bernoulli distribution with parameter p .

Remark. Let us point out that graphon models can also be defined by replacing the latent space [ 0, 1 ] by the Euclidean sphere S d 1 : = φ x 2 R d φ κ x κ 2 = 1 γ in which case latent points are sampled independently and uniformly on S d 1 .

This model has been widely studied in the literature (see Lovász (2012)) and it is now well-known that, by construction, graphons are defined on an equivalent class up to a measure preserving homomorphism . More precisely, two graphons U and W define the same probability distribution if and only if there exist measure preserving maps ' , : [ 0, 1 ] ! [ 0, 1 ] such that U ( ' ( x ) , ' ( y )) = W ( ( x ) , ( y )) almost everywhere. Hence it can be challenging to have a simple description from an observation given by sampled graph-since one has to deal with all possible composition of a bivariate function by any measure preserving homomorphism. Such difficulty arises in Wolfe and Olhede (2013) or in Klopp and Verzelen (2019) that use respectively Maximum Likelihood and least-square estimators to approximate the graphon W from the adjacency matrix A . In those works, the error measures are based on the so-called cut-distance that is defined as an infimum over all measure-preserving transformations. This statistical issue motivates the introduction of (Soft)-RGGs with latent metric spaces for which the distance is invariant by translation (or conjugation) of pairs of points. This natural assumption leads to consider that the latent space has some group structure, namely it is a compact Lie group or some compact symmetric space.

####### Definition 3. (Translation Invariant Random Geometric Graph: TIRGG)

Let ( S , ) be a compact Lie group with an invariant Riemannian metric normalized so that the range of equals [ 0, ] . Let m be the uniform probability measure on S and let us consider some map p : [ 1, 1 ] ! [ 0, 1 ] , called the envelope function. The Translation Invariant Random Geometric Graph with n 2 N νφ 0 γ points is the random graph G such that

- the n vertices X 1 , . . . , X n of G are chosen randomly in S according to the probability measure m n on S n .

6

- for any i , j 2 [ n ] with i = j, we draw an edge between nodes X i and X j with probability p cos ( X i , X j ) .

In Section 4, we present recent results regarding non-parametric estimation in the TIRGG model with S : = S d 1 the Euclidean sphere of dimension d from the observation of the adjacency matrix. A related question was addressed in Klopp and Verzelen (2019) where the authors derived sharp rates of convergence for the L 2 loss for the Stochastic Block Model (which belongs to the class of graphon models). Let us point out that a general approach to control the L 2 loss between the probability matrix and a eigenvalue-tresholded version of the adjacency matrix is the USVT method introduced by Chatterjee (2015), which was further investigated by Xu (2018). In Section 4, another line of work is presented to estimate the envelope function p where the difference between the adjacency matrix and the matrix of probabilities is controlled in operator norm. The cornerstone of the proof is the convergence of the spectrum of the matrix of probabilities towards the spectrum of some integral operator associated with the envelope function p . Based on the analysis of Koltchinskii and Giné (2000), the proof of this convergence includes in particular matrix Bernstein inequality from Tropp (2015) and concentration inequality for order 2 U-statistics with bounded kernels that was first studied by Arcones and Gine (1993) and remains an active field of research (see Giné et al. (2000), Houdré and Reynaud-Bouret (2002) or Joly and Lugosi (2016)).


<!-- p:5 -->


### 2.3 Markov Random Geometric Graphs

In the following, we will refer to growth models to denote random graph models in which a node is added at each new time step in the network and is connected to other vertices in the graph according to some probabilistic rule that needs to be specified. In the last decade, growth models for random graphs with a spatial structure have gained an increased interest. One can mention Jordan and Wade (2015), Papadopoulos et al. (2012) and Zuev et al. (2015) where geometric variants of the preferential attachment model are introduced with one new node entering the graph at each time step. More recently, Xie et al. (2015) and Xie and Rogers (2016) studied a growing variant of the RGG model. Note that in the latter works, the birth time of each node is used in the connection function while nodes are still sampled independently in R 2 . Still motivated by non-parametric estimation, the TIRGG model can be extended to a growth model by considering a Markovian sampling scheme of the latent positions. Considering a Markovian latent dynamic can be relevant to model customer behavior for item recommendation or to study bird migrations where animals have regular seasonal movement between breeding and wintering grounds (cf. Duchemin, 2022).

Definition 4. (Markov Random Geometric Graph: MRGG)

Let ( S , ) be a compact Lie group with an invariant Riemannian metric normalized so that the range of equals [ 0, ] . Let us consider some map p : [ 1, 1 ] ! [ 0, 1 ] , called the envelope function. The Markov Random Geometric Graph with n 2 N νφ 0 γ points is the random graph G such that

- the sequence of n vertices ( X 1 , . . . , X n ) of G is a Markov chain on S.

6

- for any i , j 2 [ n ] with i = j, we draw an edge between nodes X i and X j with probability p cos ( X i , X j ) .

In Section 5, we shed light on a recent work from Duchemin and De Castro (2022) that achieves non-parametric estimation in MRGGs on the Euclidean sphere of dimension d . The theoretical study of such graphs becomes more challenging because of the dependence induced by the latent Markovian dynamic. Proving the consistency of the non-parametric estimator of the envelope function p proposed in Section 5 requires in particular a new concentration inequality for U-statistics of order 2 of uniformly ergodic Markov chains. By solving link prediction problems, Duchemin and De Castro (2022) also reveal that MRGGs are convenient tools to extract temporal information on growing graphs with an underlying spatial structure.

### 2.4 Other model variants

Choice of the metric space. The Euclidean Sphere or the unit square in R d are the most studied latent spaces in the literature for RGGs. By the way, Allen-Perkins (2018) offers an interesting comparison of the different topological properties of RGGs working on one or the other of these two spaces. Nevertheless, one can find variants such as in Araya Valdivia (2020) where Euclidean Balls are considered. More recently, some researchers left the Euclidean case to consider negatively curved-i.e. hyperbolic-latent spaces. Random graphs with an hyperbolic latent space seem promising to faithfully model real world networks. Actually, Krioukov et al. (2010) showed that the RGG built on the hyperbolic geometry is a scale-free network, that is the proportion of node of degree k is of order k where is between 2 and 3. The scale-free property is found in the most part of real networks as highlighted by Xie et al. (2015).

Different degree distributions. It is now well-known that the average degree of nodes in random graph models is a key property for their statistical analysis. Let us highlight some important regimes in the random graph community that will be useful in this paper. The dense regime corresponds to the case where the expected normalized degree of the nodes ( i.e., degree divided by n ) is independent of the number of nodes in the graph. The other two important regimes are the relatively sparse and the sparse regimes where the average degree of nodes scales respectively as log ( n ) = n and 1 = n with the number of nodes n . A direct and important consequence of these definitions is that in the (relatively) sparse regime, the envelope function p from Definitions 3 and 4 depends on n while it remains independent of n in the dense regime. Similarly, in the (relatively) sparse regime, the radius threshold r from Definition 1 (resp. the connection function H from Definition 2) depend on n contrary to the dense regime.


<!-- p:6 -->


## 3 Detecting geometry in RGGs

To quote Bollobás (2001), "One of the main aims of the theory of random graphs is to determine when a given property is likely to appear." In this direction, several works tried to identify structure in networks through testing procedure, see for example Bresler and Nagaraj (2018), Ghoshdastidar et al. (2020) or Gao and Lafferty (2017). Regarding RGGs, most of the results have been established in the low dimensional regime d 3 Ostilli and Bianconi (2015), Penrose (2016), Penrose et al. (2003), Barthélemy (2011). Goel et al. (2005) proved in particular that all monotone graph properties (i.e. property preserved when adding edges to the graph) have a sharp threshold for RGGs that can be distinguished from the one of Erdös-Rényi random graphs in low-dimensions. However, applications of RGGs to cluster analysis and the interest in the statistics of high-dimensional data sets have motivated the community to investigate the properties of RGGs in the case where d !1 . If the ambitious problem of recognizing if a graph can be realized as a geometric graph is known to be NP-hard Breu and Kirkpatrick (1998), one can take a step back and wonder if a given RGG still carries some spatial information as d !1 or if geometry is lost in high-dimensions (see Eq.(1) for a formal definition), a problem known as geometry detection. In the following, we present some recent results related to geometry detection in RGGs with latent space the Euclidean sphere S d 1 and we highlight several interesting directions for future research.

Notations Given two sequences ( an ) n 2 N and ( bn ) n 2 N of positive numbers, we write an = Ο n ( bn ) or bn = n ( an ) if the sequence ( an = bn ) n 0 is bounded and we write an = on ( bn ) or bn = ! n ( an ) if an = bn ! n ! + 1 0. We further denote an = ( bn ) if an = Ο n ( bn ) and bn = Ο n ( an ) . In the following, we will denote G ( n , p , d ) the distribution of random graphs of size n where nodes X 1 , . . . , X n are sampled uniformly on S d 1 and where distinct vertices i 2 [ n ] and j 2 [ n ] are connected by an edge if and only if η X i , X j ι t p , d . The threshold value t p , d 2 [ 1, 1 ] is such that P η X 1 , X 2 ι t p , d = p . Note that G ( n , p , d ) is the distribution of RGGs on ( S d 1 , κ   κ ) sampling nodes uniformly with connection function H : t 7! 1 t π 2 2 t p , d . In the following, we will also use the notation G ( n , d , p ) to denote a graph sampled from this distribution. We also introduce some definitions of standard information theoretic tools with Definition 5.

Definition 5. Let us consider two probability measures P and Q defined on some measurable space ( E , Ε ) . The total variation distance between P and Q is given by

$$T V ( P , Q ) \colon = \sup _ { A \in \mathcal { E } } | P ( A ) - Q ( A ) | .$$

Assuming further that P Q and denoting dP = dQ the density of P with respect to Q,

- the 2 -divergence between P and Q is defined by

$$\chi ^ { 2 } ( P , Q ) \colon = \int _ { E } \left ( \frac { d P } { d Q } - 1 \right ) ^ { 2 } d Q .$$

- the Kullback-Leibler divergence between P and Q is defined by

$$K L ( P , Q ) \colon = \int _ { E } \log \left ( \frac { d P } { d Q } \right ) d P .$$

Considering that both p and d depend on n , we will say in this paper that geometry is lost if the distributions G ( n , p ) and G ( n , p , d ) are indistinguishable, namely if

$$T V ( G ( n , p ) , G ( n , p , d ) ) \to 0 \ \ \ \text {as} \ n \to \infty .$$


<!-- p:7 -->


### 3.1 Detecting geometry in the dense regime

Devroye et al. (2011) is the first to consider the case where d ! 1 in RGGs. In this paper, the authors proved that the number of cliques in the dense regime in G ( n , p , d ) is close to the one of G ( n , p ) provided d log n in the asymptotic d !1 . This work allowed them to show the convergence of the total variation (see Definition 5) between RGGs and Erdös-Renyi graphs as d !1 for fixed p and n . Bubeck et al. (2016) closed the question of geometry detection in RGGs in the dense regime showing that a phase transition occurs when d scales as n 3 as stated by Theorem 1.

Theorem 1. (Bubeck et al., 2016, Theorem 1)

- (i) Let p 2 ( 0, 1 ) be fixed, and assume that d = n 3 ! 0 . Then

$$T V ( G ( n , p ) , G ( n , p , d ) ) \to 1 \ \ a s \ n \to \infty .$$

- (ii) Furthermore, if d = n 3 !1 , then

$$\sup _ { p \in ( 0 , 1 ) } T W ( G ( n , p ) , G ( n , p , d ) ) \to 0 \ \ a s \ n \to \infty .$$

The proof of Theorem.1. ( i ) relies on a count of signed triangles in RGGs. Denoting A the adjacency matrix of the RGG, the number of triangles in A is Tr ( A 3 ) , while the total number of signed triangles is defined as

$$\tau ( G ( n , p , d ) ) \colon = \text {Tr} ( ( A - p ( J - I ) ) ^ { 3 } ) = \sum _ { \{ i , j , k \} \in \{ \real ^ { n } _ { 3 } \} } \left ( A _ { i , j } - p \right ) \left ( A _ { i , k } - p \right ) \left ( A _ { j , k } - p \right ) ,$$

where I is the identity matrix and J 2 R n n is the matrix with every entry equals to 1. The analogous quantity in Erdös Renyi graphs ( G ( n , p )) is defined similarly. Bubeck et al. (2016) showed that the variance of ( G ( n , p , d )) is of order n 3 while the one of the number of triangles is of order n 4 . This smaller variance for signed triangles is due to the cancellations introduced by the centering of the adjacency matrix. Lemma 1 provides the precise bounds obtained on the expectation and the variance of the statistic of signed triangles. Theorem.1. ( i ) follows from the lower-bounds (resp. the upper-bounds) on the expectations (resp. the variances) of ( G ( n , p )) and ( G ( n , p , d )) presented in Lemma 1.

Lemma 1. (Bubeck et al., 2016, Section 3.4) For any p 2 ( 0, 1 ) and any n , d 2 N νφ 0 γ it holds

$$\mathbb { E } [ \tau ( G ( n , p ) ) ] = 0 , \quad \mathbb { E } [ \tau ( G ( n , p , d ) ) ] \geq \left ( \begin{matrix} n \\ n \\ \sqrt { d } \end{matrix} \right ) \frac { C _ { p } } { \sqrt { d } } \\ \intertext { a n d } \max \{ V a r \left [ \tau ( G ( n , p ) ) \right ] , V a r \left [ \tau ( G ( n , p , d ) ) \right ] \} \leq n ^ { 3 } + \frac { 3 n ^ { 4 } } { d } ,$$

where C p &gt; 0 is a constant depending only on p.

Let us now give an overview of the proof of the indistinguishable part of Theorem 1. Bubeck et al. (2016) proved that in the dense regime, the phase transition for geometry detection occurs at the regime at which Wishart matrices becomes indistinguishable from GOEs (Gaussian Orthogonal Ensemble). In the following, we draw explicitly this link in the case p = 1 = 2.

An n n Wishart matrix with d degrees of freedom is a matrix of inner products of n d -dimensional Gaussian vectors denoted by W ( n , d ) while an n n GOE random matrix is a symmetric matrix with i.i.d. Gaussian entries on and above the diagonal denoted by M ( n ) . Let X be an n d matrix where the entries are i.i.d. standard normal random variables, and let W = W ( n , d ) = XX &gt; be the corresponding n n Wishart matrix. Then recalling that for X 1 Ν ( 0, I d ) a standard gaussian vector of dimension d , X 1 = κ X 1 κ 2 is uniformly distributed on the sphere S d 1 , we get that the n n matrix A defined by

6

$$\forall i , j \in [ n ] , \ A _ { i , j } = \left \{ \begin{array} { l l } { 1 } & { i f W _ { i , j } \geq 0 \, a n d \, i \neq j } \\ { 0 } & { o t h e r w i s e . } \end{array}$$

has the same distribution as the adjacency matrix of a graph sampled from G ( n , 1 = 2, d ) . We denote H the map that takes W to A . Analogously, one can prove that G ( n , 1 = 2 ) can be seen as a function of an n n GOE matrix. Let M ( n ) be a symmetric n n random matrix where the diagonal entries are i.i.d. normal random variables with mean zero and variance 2, and the entries above the diagonal are i.i.d.standard normal random variables, with the entries on and above the diagonal all independent. Then B = H ( M ( n )) is distributed as the adjacency matrix of G ( n , 1 = 2 ) . We then get


<!-- p:8 -->


$$\text {TV} ( G ( n , 1 / 2 , d ) , G ( n , 1 / 2 ) ) = \text {TV} ( H ( W ( n , d ) ) , H ( M ( n ) ) ) \leq \text {TV} ( W ( n , d ) ) , M ( n ) ) \, .$$

If a simple application of the multivariate Central Limit Theorem proves that the right hand side of (2) goes to zero as d !1 for fixed n , more work is necessary to address the case where d = d ( n ) = ! n ( n 3 ) and n !1 . The distributions of W ( n , d ) and M ( n ) are known and allow explicit computations leading to Theorem 2. This proof can be adapted for any p 2 ( 0, 1 ) leading to Theorem 1. ( ii ) from (2).

Theorem 2. (Bubeck et al., 2016, Theorem 7)

Define the random matrix ensembles W ( n , d ) and M ( n ) as above. If d = n 3 !1 , then

$$T V ( W ( n , d ) , M ( n ) ) \rightarrow 0 .$$

Extensions Considering R d as latent space endowed with the Euclidean metric, Bubeck and Ganguly (2015) extended Theorem 2 and proved an information theoretic phase transition. To give an overview of their result, let us consider the n n Wigner matrix Μ n with zeros on the diagonal and i.i.d. standard Gaussians above the diagonal. For some n d matrix X with i.i.d. entries from a distribution on R d that has mean zero and variance 1, we also consider the following rescaled Wishart matrix associated with X

$$\mathcal { W } _ { n , d } \colon = \frac { 1 } { \sqrt { d } } \left ( \mathbb { X } \mathbb { X } ^ { \top } - d i a g ( \mathbb { X } \mathbb { X } ^ { \top } ) \right ) ,$$

where the diagonal was removed. Using an high-dimensional entropic Central Limit Theorem, Bubeck and Ganguly (2015) proved Theorem 3 which implies that geometry is lost in RGG ( n , , ( R d , κ   κ )) as soon as d n 3 log 2 ( d ) provided that the measure is sufficiently smooth (namely log-concave) and the rate is tight up to logarithmic factors. We refer to Racz and Bubeck (2016) for a friendly presentation of this result. Note that the comparison between Wishart and GOE matrices also naturally arise when dealing with covariance matrices. For example, Theorem 2 was used in Brennan and Bresler (2019) to study the informational-computational tradeoff of sparse Pincipal Component Analysis.

Theorem 3. (Bubeck and Ganguly, 2015, Theorem 1)

If the distribution is log-concave and d n 3 log 2 ( d ) !1 , then TV ( Ω n , d , Μ n ) ! 0.

On the other hand, if has a finite fourth moment and d n 3 ! 0 , then TV ( Ω n , d , Μ n ) ! 1.

### 3.2 Failure to extend the proof techniques to the sparse regime

Bubeck et al. (2016) provided a result in the sparse regime where p = c n showing that one can distinguish between G ( n , c n ) and G ( n , c n , d ) as long as d log 3 n . The authors conjectured that this rate is tight for the sparse regime (see Conjecture 1).

Conjecture 1. (Bubeck et al., 2016, Conjecture 1)

Let c &gt; 0 be fixed, and assume that d = log 3 ( n ) !1 . Then

$$\text {TV} \left ( G \left ( n , \frac { c } { n } \right ) , G \left ( n , \frac { c } { n } , d \right ) \right ) \to 0 \ \ a s \ n \to \infty .$$

The testing procedure from Bubeck et al. (2016) to prove the distinguishability result in the sparse regime was based on a simple counting of triangles. Indeed, when p scales as 1 n , the signed triangle statistic does not give significantly more power than the triangle statistic which simply counts the number of triangles in the graph. Recently, Avrachenkov and Bobu (2020) provided interesting results that give credit to Conjecture 1. First, they proved that in the sparse regime, the clique number of G ( n , p , d ) is almost surely at most 3 under the condition d log 1 + " n for any " &gt; 0. This means that in the sparse regime, G ( n , p , d ) does not contain any complete subgraph larger than a triangle like Erdös-Renyi graphs. Hence it is hopeless to prove that Conjecture 1 is false considering the number of k -cliques for k 4. Nevertheless, one could believe that improving the work of Bubeck et al. (2016) by deriving sharper bounds on the number of 3-cliques (i.e. the number of triangles), it could possible to statistically distinguish between G ( n , p , d ) and G ( n , p ) in the sparse regime even for some d log 3 n . In a regime that can be made arbitrarily close to the sparse one, Avrachenkov and Bobu (2020) proved that this is impossible as stated by Theorem 4.


<!-- p:9 -->


Theorem 4. (Avrachenkov and Bobu, 2020, Theorem 5)

Let us suppose that d log 3 n and p = ( n ) = n with n m ( n ) n for some m &gt; 0 . Then the expected number of triangles-denoted E [ T ( n , p , d )] -in RGGs sampled from G ( n , p , d ) is of order n 3 p 3 , meaning that there exist two universal constants c , C &gt; 0 such that for n large enough it holds

$$c \binom { n } { 3 } p ^ { 3 } \leq \mathbb { E } [ T ( n , p , d ) ] \leq C \binom { n } { 3 } p ^ { 3 } .$$

In a nutshell, the work from Avrachenkov and Bobu (2020) suggests that a negative result regarding Conjecture 1 cannot be obtained using statistics based on clique numbers. This discussion naturally gives rise to the following more general question.

Given a random graph model with n nodes, latent geometry in dimension d = d ( n ) and edge

density p = p ( n ) , for what triples ( n , d , p ) is the model G ( n , p , d ) indistinguishable from G ( n , p ) ? ( Θ )

### 3.3 Towards the resolution of geometry detection

#### 3.3.1 A first improvement when d &gt; n

A recent work from Brennan et al. (2020) tackled the general problem ( Θ ) and proved Theorem 5.

Theorem 5. (Brennan et al., 2020, Theorem 2.4)

Suppose p = p ( n ) 2 ( 0, 1 = 2 ] satisfies that n 2 log n = Ο n ( p ) and

$$d \gg \min \left \{ p n ^ { 3 } \log p ^ { - 1 } \, , \, p ^ { 2 } n ^ { 7 / 2 } ( \log n ) ^ { 3 } \sqrt { \log p ^ { - 1 } } \right \} ,$$

where d also satisfies that d n log 4 n. Then

$$T V ( G ( n , p ) , G ( n , p , d ) ) \to 0 \ \ a s \ n \to \infty .$$

6

Remarks In the dense regime, Theorem 5 recovers the optimal guarantee from Theorem 1. In the sparse regime, Theorem 5 states that if d n 3 = 2 ( log n ) 7 = 2 , then geometry is lost in G ( n , c n , d ) (where c &gt; 0). This result improves the work from Bubeck et al. (2016). Nevertheless, regarding Conjecture 1, it remains a large gap between the rates log 3 n and n 3 = 2 ( log n ) 7 = 2 where nothing is known up to date. Let us sketch the main elements of the proof of Theorem 5. In the following we denote G = G ( n , p , d ) with set of edges E ( G ) and for any i , j 2 [ n ] , i = j , we denote G φ i , j γ the set of edges other than φ i , j γ in G . One first important step of their approach is the following tenzorization Lemma for the Kullback-Leibler divergence.

Lemma 2. (Kontorovich and Raginsky, 2017, Lemma 3.4)

Let us consider ( X , Β ) a measurable space with X a Polish space and Β its Borel -field. Consider some probability measure on the product space X k with = 1 2 k . Then for any other probability measure on X k it holds

$$K L ( \nu | | \mu ) \leq \sum _ { i = 1 } ^ { k } \mathbb { E } _ { x \sim \nu } \left [ K L ( \nu _ { i } ( \cdot | x _ { \sim i } ) | | \mu _ { i } ) \right ] , \\ d i s t r i b y t i o n \, o r m o n d i n g t o t h e i t h m a g r i a n g l o f e v a n d w k$$

where i is the probability distribution corresponding to the i-th marginal of and where x i : =( x 1 , . . . , x i 1 , x i + 1 , . . . , x k ) .

$$2 T V ( G ( n , p , d ) , G ( n , p ) ) ^ { 2 } & \leq K L ( G ( n , p , d ) | | G ( n , p ) ) \quad \text {from Pinsker's inequality} \\ & \leq \sum _ { 1 \leq i < j \leq n } \mathbb { E } [ K L ( \mathcal { L } ( \mathbf 1 _ { i , j } ) \in E ( | \sigma ( G _ { \sim ( i , j ) } ) | | B n ( p ) ) ] \quad \text {from Lemma 2} \\ & \leq \binom { n } { 2 } \times \mathbb { E } [ \chi ^ { 2 } ( \mathcal { L } ( \mathbb { 1 } _ { \epsilon _ { j } \in E ( G ) } | \sigma ( G _ { \sim \epsilon _ { j } } ) ) , B n ( p ) ) ] \\ & = \binom { n } { 2 } \times \mathbb { E } \left [ \frac { ( Q - p ) ^ { 2 } } { p ( 1 - p ) } \right ] ,$$


<!-- p:10 -->


where Q : = P e 0 2 E ( G ) φ G e 0 is a ( G e 0 ) -measurable random variable corresponding to the probability that a specific edge is included in the graph given the rest of the graph. The proof then consists in showing that with high probability, Q concentrates near p . To do so, they use a coupling argument that gives an alternative way to generate X 1 that provides a direct description of 1 e 0 2 E ( G ) in terms of the random variables introduced in the coupling. If this step may seem computationally involved, it is not conceptually difficult since it turns out to be a simple re-parametrization of the problem. An integration of this concentration result for Q implies that the convergence of Theorem 5 holds when d pn 3 log p 1 . To get the convergence result in the regime where d p 2 n 7 = 2 ( log n ) 3 p log p 1 which gives the improvement over Bubeck et al. (2016) in the sparse case one additional step of coupling is required. More precisely, they decompose E [( Q p ) 2 ] as E [( Q p ) ( Q p )] . The previous coupling argument gives a concentration inequality allowing to bound with high probability the first term φ Q p φ . It remains then to upper bound E [ φ Q p φ ] which relies on a simple observation given by the following proposition.

Proposition 1. (Brennan et al., 2020, Proposition 5.3) Let e 0 denote the marginal distribution of G restricted to all edges that are not e 0 , and let + e 0 denote the distribution of G conditioned on the event e 0 2 E ( G ) . It holds

$$\mathbb { E } [ | Q - p | ] = 2 p \times \text {TV} \left ( \nu _ { \sim e _ { 0 } } ^ { + } , \nu _ { \sim e _ { 0 } } \right ) .$$

The proof is then concluded by using another coupling argument between + e 0 and e 0 to upperbound the total variation distance involved in Eq.(3) and we give a sketch of proof in the following. Given latent positions X 1 , . . . , X n uniformly and independently sampled on S d 1 , we can consider without loss of generality that X 1 = ( 1, 0, . . . 0 ) . Denoting X 2 = ( X 2, j ) j 2 [ d ] and ' d the density of X 2,1 1 , one can define = r 1 2 1 X 2 2,1 and X + 2 : =( , X 2,2 , . . . , X 2, d ) where is a random variable in [ 1, 1 ] with density ' + d , p ( x ) = p 1 1 x t p , d ' d ( x ) . Denoting further G e 0 (resp. G + e 0 ) the RGG with threshold t p , d induced by the latent points ( X i ) i 2 [ n ] (resp. ( X 1 , X + 2 , X 3 , . . . , X n ) ) without the edge e 0 = φ 1, 2 γ , G e 0 (resp. G + e 0 ) is distributed as e 0 (resp. + e 0 ). Hence it holds,

6


$$\mathbb { E } [ | Q - p | ] & \leq 2 p \times T V \left ( \nu _ { \sim e _ { 0 } } ^ { + } , \nu _ { \sim e _ { 0 } } \right ) \leq 2 p \times \mathbb { P } ( G _ { \sim e _ { 0 } } \neq G _ { \sim e _ { 0 } } ^ { + } ) \leq 2 p \sum _ { i = 3 } ^ { n } \mathbb { P } \left ( 1 _ { ( X _ { z } , X _ { i } ) \geq t _ { \eta , d } } \neq 1 _ { ( X _ { z } ^ { + } , X _ { i } ) \geq t _ { \eta , d } } \right ) .$$

The proof is concluded using standard concentration arguments.

#### 3.3.2 Reaching the polylogarithmic regime

Very recently, Liu et al. (2021) came with novels ideas and improved upon the previous bounds for geometry detection by polynomial factors in the sparse regime. This significant breakthrough presented in Theorem 6 almost solves Conjecture 1.

Theorem 6. (Liu et al., 2021, Theorem 1.2) For any fixed constant c 1 , if d log 36 n, then

$$\text {TV} \left ( G \left ( n , \frac { c } { n } \right ) , G \left ( n , \frac { c } { n } , d \right ) \right ) \to 0 \ \ a s \ n \to \infty .$$

The authors do not limit their analysis to the sparse regime but also provide results holding for any regime interpolating between the sparse and the dense cases as shown with Theorem 7.

Theorem 7. (Liu et al., 2021, Theorem 1.1 and Lemma A.1)

- For any fixed constant c &gt; 0 , if c n &lt; p &lt; 1 2 and d p 2 n 3 , then

$$T V ( G ( n , p ) \, , G ( n , p , d ) ) \to 0 \ \ a s \ n \to \infty .$$

- If 1 n 2 p 1 for any fixed constant &gt; 0 , then as long as d ( nH ( p )) 3 ,

$$\text {TV} \left ( G \left ( n , \frac { c } { n } \right ) , G \left ( n , \frac { c } { n } , d \right ) \right ) \to 1 \ \ a s \ n \to \infty ,$$

where H ( p ) = p log 1 p +( 1 p ) log 1 1 p is the binary entropy function. This result can be achieved using the signed triangle statistic following an approach strictly analogous to Bubeck et al. (2016).

1 i.e. ' d is the density of a one-dimensional marginal of a uniform random point on S d 1 .


<!-- p:11 -->


Liu et al. (2021) extend the work from Bubeck et al. (2016) and prove that the signed statistic distinguishes between G ( n , p ) and G ( n , p , d ) not only in the sparse and dense cases but also for most p , as long as d ( nH ( p )) 3 . We provide in the Appendix A a synthetic description of the proofs of Theorems 6 and 7. Let us mention that the proofs rely on a new concentration result for the area of the intersection of a random sphere cap with an arbitrary subset of S d 1 , which is established using optimal transport maps and entropy-transport inequalities on the unit sphere. Liu et al. (2021) make use of this set-cap intersection concentration lemma for the theoretical analysis of the Belief Propagation algorithm.

### 3.4 Open problems and perspectives

The main results we have presented so far look as follows:

| Task                                                                                    | Current state of knowledge                                    | Ref.        |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------|-------------|
| Recognizing if a graph can be realized as a RGG                                         | NP-hard                                                       | 1998        |
| Testing between G ( n , p , d ) and G ( n , p ) in high-dimension for p 2 ( 0,1 ) fixed | 0 n 3 Polynomial time test Undistinguishable d                | 2016        |
| Testing between G ( n , c n , d ) and G ( n , c n ) in high-dimension for c > 0         | 0 log 3 n log 36 n Polynomial time test Undistinguishable ? d | 2016 & 2021 |

Figure 2: Phase-Diagram of the ( d , p ) regions where geometry detection (on the Euclidean sphere) is known to be information theoretically impossible or possible (in polynomial time). Note that the figure only presents a simplified illustration of the current state of knowledge for the problem of geometry detection on S d 1 since the true scales are not respected.

With new proof techniques based on combinatorial arguments, direct couplings and applications of information inequalities, Brennan et al. (2020) were the first to make a progress towards Conjecture 1. Nevertheless, their proof was heavily relying on a coupling step involving a De Finetti-type result that requires the dimension d to be larger than the number of points n . Liu et al. (2021) improved upon the previous bounds by polynomial factors with innovative proof arguments. In particular, their analysis makes use of the Belief Propagation algorithm and the cavity method, and relies on a new sharp estimate for the area of the intersection of a random sphere cap with an arbitrary subset of S d 1 . The proof of this new concentration result is an application of optimal transport maps and entropy-transport inequalities. Despite this recent progress, a large span of research directions remain open and we discuss some of them in the following.


<!-- p:12 -->


1. Closing the gaps for geometry detection on the Euclidean sphere S d 1 . Figure 2 shows that there are still important research directions to investigate to close the question of geometry detection regarding RGGs on S d 1 . First in the sparse regime, it would be desirable to finally know if Conjecture 1 is true, meaning that the phase transition occurs when the latent dimension is of the order of log 3 n . It could be fruitful to see if some steps in the approach from Liu et al. (2021) could be sharpened in order to get down to the threshold log 3 n . A question that seems even more challenging is to understand what happens in the regimes where p = p ( n ) 2 ( 1 n , 1 ) and d = d ( n ) 2 ([ H ( p ) n ] 3 , p 2 n 3 ) (corresponding to the white region on Figure 2). To tackle this question, one could try to extend the methods used in the sparse case by Liu et al. (2021) to denser cases. Another possible approach to close this gap would be to dig deeper into the connections between the Wishart and GOE ensembles. One research direction to possibly improve the existing impossibility results regarding geometry detection would be to avoid the use of the data-processing inequality in Eq.(2) which makes us lose the fact that we do not observe the matrices W ( n , d ) and M ( n ) themselves. To some extent, we would like to take into account that some information is lost by observing only the adjacency matrices. In a recent work, Brennan et al. (2021) made a first step in this direction. They study the total variation distance between the Wishart and GOE ensembles when some given mask is applied beforehand. They proved that the combinatorial structure of the revealed entries, viewed as the adjacency matrix of a graph G , drives the distance between the two distributions of interest. More precisely, they provide regimes for the latent dimension d based exclusively on the number of various small subgraphs in G , for which the total variation distance goes to either 0 or 1 as n !1 .

## 2.

- Let us mention that the signed triangle statistic has found applications beyond the scope of spatial networks. In Jin et al. (2019), the authors study community based random graphs (namely the Degree Corrected Mixed Membership model) and are interested in testing whether a graph has only In that way, they extend the signed triangle statistic to m -gon in the network for any m 3. Contrary to Bubeck et al. (2016), the average degree of each node is not known and the Degree Corrected Mixed Membership model allows degree heterogeneity. In Jin et al. (2019), the authors define the signal-to-noise ratio (SNR) using parameters of their model and they prove that a phase transition occurs, namely i ) when the SNR goes to + 1 , the Signed Polygon test is able to separate the alternative hypothesis from the null asymptotically, and ii ) when the SNR goes to 0 (and additional mild conditions), then the alternative hypothesis is inseparable from the null.
- How specific is the signed triangle statistic to RGGs? one community or multiple communities. They propose the Signed Polygon as a class of new tests.
3. How the phase transition phenomenon in geometry detection evolves when other latent spaces are considered?

This question is related to the robustness of the previous results with respect to the latent space. Inspired by Bubeck et al. (2016), Eldan and Mikulincer (2020) provided a generalization of Theorem 1 considering an ellipsoid rather than the sphere S d 1 as latent space. They proved that the phase transition also occurs at n 3 provided that we consider the appropriate notion of dimension which takes into account the anisotropy of the latent structure.

In Dall and Christensen (2002), the clustering coefficient of RGGs with nodes uniformly distributed on the hypercube shows systematic deviations from the Erdos-Rényi prediction.

4. What is inherent to the connection function?

Considering a fixed number of nodes, Erba et al. (2020) use a multivariate version of the central limit theorem to show that the joint probability of rescaled distances between nodes is normal-distributed as d ! 1 . They provide a way to compute the correlation matrix. This work allows them to evaluate the average number of M -cliques, i.e. of fully-connected subgraphs with M vertices, in high-dimensional RGGs and Soft-RGGs. They can prove that the infinite dimensional limit of the average number of M -cliques in Erdös-Rényi graphs is the same of the one obtained from for Soft-RGGs with a continuous activation function. On the contrary, they show that for classical RGGs, the average number of cliques does not converge to the Erdös-Rényi prediction. This paper leads to think that the behavior of local observables in Soft-RGGs can heavily depend on the connection function considered. The work from Erba et al. (2020) is one of the first to address the emerging questions concerning the high-dimensional fluctuations of some statistics in RGGs. If they focused on the number of M -cliques, one can also mention the recent work from Grygierek and Thäle (2020) that provide a central limit theorem for the edge counting statistic as the space dimension d tends to infinity . Their work shows that the Malliavin-Stein approach for Poisson functionals that was first introduced in stochastic geometry can also be used to deal with spatial random models in high dimensions.


<!-- p:13 -->


In a recent work, Liu and Racz (2021a) are interested in extending the previous mentioned results on geometry detection in RGGs to Soft RGGs with some specific connection functions. The authors consider the dense case where the average degree of each node scales with the size of the graph n and study geometry detection with graphs sampled from Soft-RGGs that interpolate between the standard RGG on the sphere S d 1 and the Erdös-Rényi random graph. Hence, the null hypothesis remains that the observed graph G is a sample from G ( n , p ) while the alternative becomes that the graph is the Soft-RGG where we draw an edge between nodes i and j with probability

$$( 1 - q ) p + q 1 _ { t _ { p , d } \leq \langle X _ { i } , X _ { j } \rangle } ,$$

where ( X i ) i 1 are randomly and independently sampled on S d 1 and where q 2 [ 0, 1 ] can be interpreted as the geometric strength of the model. Denoting the random graph model G ( n , p , d , q ) , one can easily notice that G ( n , p , d , 1 ) is the standard RGG on the Euclidean sphere S d 1 while G ( n , p , d , 0 ) reduces to the Erdös-Rényi random graph. Hence, by taking q = 1 in Theorem 8, we recover Theorem 1 from Bubeck et al. (2016). One can further notice that Theorem 8 depicts a polynomial dependency on q for geometry detection but when q &lt; 1 there is a gap between the upper and lower bounds as illustrated by Figure 3 taken from Liu and Racz (2021a). As stated in Liu and Racz (2021a), " [ ... ] a natural direction of future research is to consider [ geometry detection ] for other connection functions or underlying latent spaces, in order to understand how the dimension threshold for losing geometry depends on them."

Theorem 8. (Liu and Racz, 2021a, Theorem 1.1) 2 be fixed.

Let p ( 0, 1 )

- (i) If n 3 q 6 = d !1 , then TV ( G ( n , p ) , G ( n , p , d , q )) ! 1 as n !1 .
- (ii) If nq ! 0 or n 3 q 2 d ! 0

$$T V ( G ( n , p ) , G ( n , p , d , q ) ) \rightarrow 0$$

- = , then TV G n , p , G n , p , d , q ! 0 as n !1 .

Figure 3: Phase diagram for detecting geometry in the soft random geometric graph G ( n , p , d , q ) . Here d = n and q = n for some , &gt; 0.

The same authors in Liu and Racz (2021b) extend the model of the Soft-RGG by considering the latent space R d where the latent positions ( X i ) i 2 [ n ] are i.i.d. sampled with X 1 Ν ( 0, I d ) . Two different nodes i , j 2 [ n ] are connected with probability p ( η X i , X j ι ) where p is a monotone increasing connection function. More precisely, they consider a connection function p parametrized by i ) a cumulative distribution function F : R ! [ 0, 1 ] and ii ) a scalar r &gt; 0 and given by

$$\mathbf p \colon t \mapsto F \left ( \frac { t - \mu _ { p , d , r } } { r \sqrt { d } } \right ) ,$$

where p , d , r is determined by setting the edge density in the graph to be equal to p , namely E [ p ( η X 1 , X 2 ι )] = p . They work in the dense regime by considering that p 2 ( 0, 1 ) is independent of n . The parameter r encodes the flatness of the connection function and is typically a function of n . The authors prove phase transitions of detecting geometry in this framework in terms of


<!-- p:14 -->


- 5.

the dimension of the underlying geometric space d and the variance parameter r . The larger r , the smaller the dimension d at which the phase transition occurs. When r ! n !1 0, the connection function becomes an indicator function and the transition appears at d n 3 (recovering the result from Theorem 1 established for RGGs on the Euclidean Sphere).

- Suppose that we know that the latent variables are embedded in a Eucliden Sphere, can we estimate the dimension d from the observation of the graph?

When p = 1 = 2, Bubeck et al. (2016) obtained a bound on the difference of the expected number of signed triangles between consecutive dimensions leading to Theorem 9.

Theorem 9. (Bubeck et al., 2016, Theorem 5)

There exists a universal constant C &gt; 0 , such that for all integers n and d 1 &lt; d 2 , one has

$$T V ( G ( n , 1 / 2 , d _ { 1 } ) , G ( n , 1 / 2 , d _ { 2 } ) ) \geq 1 - C \left ( \frac { d _ { 1 } } { n } \right ) ^ { 2 } .$$

The bound provided by Theorem 9 is tight in the sense that when d n , G ( n , 1 = 2, d ) and G ( n , 1 = 2, d + 1 ) are indistiguishable as proved in Eldan (2015). More recently, Araya Valdivia and De Castro (2019) proposed a method to infer the latent dimension of a Soft-RGG on the Euclidean Sphere in the low dimensional setting. Their approach is proved to correctly recover the dimension d in the relatively sparse regime as soon as the connection function belongs to some Sobolev class and satisfies a spectral gap condition.

6. Extension to hypergraphs and information-theoretic / computational gaps.
2. Let us recall that a hypergraph is a generalization of a graph in which an edge can join any number of vertices. Extensions of RGGs to hypergraphs have already been proposed in the literature (see for example Lunagómez et al. (2017)). A nice research direction would consist in investigating the problem of geometry detection in these geometric representations of random hypergraphs. As already discussed, it has been conjectured that the problem of geometry detection in RGGs on S d 1 does not present a statistical-to-algorithmic gap meaning that whenever it is information theoretically possible to differ G ( n , p , d ) from G ( n , p ) , we can do it with a computational complexity polynomial in n (using the signed triangle statistic). Dealing with hypergraphs, one can legitimately think that statistical-to-algorithmic gaps could emerge. This intuition is based on the fact that most of the time, going from a matrix problem to a tensor problem brings extra challenges. One can take the example of principal component analysis of Gaussian k -tensors with a planted rank-one spike (cf. Ben Arous et al. (2020)). In this problem, we assume that we observe for any l 2 [ n ] ,

$$\Upsilon ^ { l } = \lambda u ^ { \otimes k } + W ^ { l } ,$$

where u 2 S d 1 is deterministic, 0 is the signal-to-noise ratio and where ( W l ) l 2 [ n ] are independent Gaussian k -tensor (we refer to Ben Arous et al. (2020) for further details). The goal is to infer the 'planted signal' or 'spike', u . In the matrix case (i.e. when k = 2), whenever the problem is information theoretically solvable, we can also recover the spike with a polynomial time algorithm (using for example a spectral method). If we look at the tensor version of this problem where k 3, there is a regime of signal-to-noise ratios for which it is information theoretically possible to recover the signal but for which there is no known algorithm to approximate it in polynomial time in n . This is a statistical-to-algorithmic gap and we refer to (Brennan and Bresler, 2020, Section 3.8) and references therein for more details.

7. Can we describe the properties of high dimensional RGGs in the regimes where TV ( G ( n , p ) , G ( n , p , d )) ! 1 as n !1 ? In the low dimensional case, RGGs have been extensively studied: their spectral or topological properties, chromatic number or clustering number are now well known (see e.g. Walters (2011); Penrose et al. (2003)). One of the first work studying the properties of high dimensional RGGs is Avrachenkov and Bobu (2020) where the authors are focused on the clique structure. These questions are essential to understand how good high dimensional RGGs are as models for the theory of network science.


<!-- p:15 -->


8. How to find a relevant latent space given a graph with an underlying geometric structure? As stated in Racz and Bubeck (2016), "Perhaps the ultimate goal is to find good representations of network data, and hence to faithfully embed the graph of interest into an appropriate metric space" . This task is known as manifold learning in the Machine learning community. Recently Smith et al. (2019) proved empirically that the eigenstructure of the Laplacian of the graph provides information on the curvature of the latent space. This is an interesting research direction to propose model selection procedure and infer a relevant latent space for a graph.

## 4 Non-parametric inference in RGGs

In this section, we are interested in non-parametric inference in TIRGGs (see Definition 3) on the Euclidean sphere S d 1 . The methods presented rely mainly on spectral properties of such random graphs. Note that spectral aspects in (Soft-)RGGs have been investigated for a long time (see for example Rai (2004)) and it is now well-known that the spectra of RGGs are very different from the one of other random graph models since the appearance of particular subgraphs give rise to multiple repeated eigenvalues (see Nyberg et al. (2015) and Blackwell et al. (2007)). Recent works took advantage of the information captured by the spectrum of RGGs to study topological properties such as Aguilar-Sánchez et al. (2020). In this section, we will see that random matrix theory is a powerful and convenient tool to study the spectral properties of RGGs as already highlighted by Dettmann et al. (2017).

### 4.1 Description of the model and notations

We consider a Soft-RGG on the Euclidean Sphere S d 1 endowed with the geodesic distance . We consider that the connection function H is of the form H : t 7! p ( cos ( t )) where p : [ 1, 1 ] ! [ 0, 1 ] is an unknown function that we want to estimate. This Soft-RGG belongs to the class of TIRGG has defined in Section 2 and corresponds to a graphon model where the graphon W is given by

$$\forall x , y \in \S ^ { d - 1 } , \ W ( x , y ) \coloneqq \mathbf p ( \langle x , y \rangle ) .$$

W viewed as an integral operator on square-integrable functions, is a compact convolution (on the left) operator

$$\mathbb { T } _ { W } \colon f \in L ^ { 2 } ( \S ^ { d - 1 } ) \mapsto \int _ { \S ^ { d - 1 } } W ( x , \cdot ) f ( x ) \sigma ( d x ) \in L ^ { 2 } ( \S ^ { d - 1 } ) ,$$

where is the Haar measure on S d 1 . The operator T W is Hilbert-Schmidt and it has a countable number of bounded real eigenvalues k with zero as only accumulation point. The eigenfunctions of T W have the remarkable property that they do not depend on p (see (Dai and Xu, 2013, Lemma 1.2.3)): they are given by the real Spherical Harmonics. We denote Η l the space of real Spherical Harmonics of degree l with dimension dl and with orthonormal basis ( Yl , j ) j 2 [ dl ] . We end up with the following spectral decomposition of the envelope function p

$$\forall x , y \in \mathbb { S } ^ { d - 1 } , \quad \mathbf p ( \langle x , y \rangle ) = \sum _ { l \geq 0 } p _ { l } ^ { * } \sum _ { j = 1 } ^ { d _ { l } } Y _ { l , j } ( x ) Y _ { l , j } ( y ) = \sum _ { l \geq 0 } p _ { l } ^ { * } c _ { l } G _ { l } ^ { \beta } ( \langle x , y \rangle ) ,$$

where : =( p 0 , p 1 , . . . , p 1 , . . . , p l , . . . , p l , . . . ) meaning that each eigenvalue p l has multiplicity dl and G l is the Gegenbauer polynomial of degree l with parameter : = d 2 2 and c l : = 2 l + d 2 d 2 . p is assumed bounded and as a consequence p 2 L 2 (( 1, 1 ) , w ) where the weight function w is defined by w ( t ) : =( 1 t 2 ) 1 = 2 . Note that the decomposition (5) shows that it is enough to estimate the eigenvalues ( p l ) l to recover the envelope function p .

### 4.2 Estimating the matrix of probabilities

Let us denote A the adjacency matrix of the Soft-RGG G given by entries Ai , j 2 φ 0, 1 γ where Ai , j = 1 if the nodes i and j are connected and Ai , j = 0 otherwise. We denote by the n n symmetric matrix with entries i , j = p η X i , X j ι for 1 i &lt; j n and zero diagonal entries. We consider the scaled version of the matrices A and given by


<!-- p:16 -->


$$\widehat { T } _ { n } = \frac { 1 } { n } A \ \text {and} \ T _ { n } = \frac { 1 } { n } \Theta .$$

Bandeira and van Handel (2016) proved a near optimal error bound for the operator norm of b Tn Tn . Coupling this result with the Weyl's perturbation Theorem gives a control on the difference between the eigenvalues of the matrices b Tn and Tn , namely with probability greater that 1 exp ( n ) it holds,

$$\forall k \in [ n ] , \ \ | \lambda _ { k } ( \widehat { T } _ { n } ) - \lambda _ { k } ( T _ { n } ) | \leq \| \widehat { T } _ { n } - T _ { n } \| = O ( 1 / \sqrt { n } ) ,$$

where k ( M ) is the k -th largest eigenvalue of any symmetric matrix M . This result shows that the spectrum of the scaled adjacency matrix b Tn is a good approximation of the one of the scaled matrix of probabilities Tn .

### 4.3 Spectrum consistency of the matrix of probabilities

For any R 0, we denote

$$\tilde { R } \coloneqq & \sum _ { l = 0 } ^ { R } d _ { l } , \\$$

which corresponds to the dimension of the space of Spherical Harmonics with degree at most R . Proposition 2 states that the spectrum of Tn converges towards the one of the integral operator T W in the 2 metric which is defined as follows.

Definition 6. Given two sequences x , y of reals-completing finite sequences by zeros-such that P i x 2 i + y 2 i &lt; 1 , we define the ' 2 rearrangement distance 2 ( x , y ) as

$$\delta _ { 2 } ^ { 2 } ( x , y ) \colon = \inf _ { \sigma \in \mathfrak { S } _ { n } } \sum _ { i } ( x _ { i } - y _ { \sigma ( i ) } ) ^ { 2 } \, ,$$

where S n is the set of permutations with finite support. This distance is useful to compare two spectra.

Proposition 2. (De Castro et al., 2020, Proposition 4) There exists a universal constant C &gt; 0 such that for all 2 ( 0, 1 = 3 ) and for all n 3  ̃ R log ( 2  ̃ R = ) , it holds

$$\delta _ { 2 } ( \lambda ( T _ { n } ) , \lambda ^ { * } ) \leq 2 \left [ \sum _ { l > R } d _ { l } \left ( p _ { l } ^ { * } \right ) ^ { 2 } \right ] ^ { 1 / 2 } + C \sqrt { \tilde { R } \left ( 1 + \log ( \tilde { R } / \alpha ) \right ) / n } ,$$

with probability at least 1 3 .

Proposition 2 shows that the ' 2 rearrangement distance between and ( Tn ) decomposes as the sum of a bias term and a variance term. The second term on the right hand side of (8) corresponds to the variance. The proof leading to this variance bound relies on the Hoffman-Wielandt inequality and borrows ideas from Koltchinskii and Giné (2000). It makes use of recent developments in random matrix concentration by applying a Bernstein-type concentration inequality (see Tropp (2015) for example) to control the operator norm of the sum of independent centered symmetric matrices given by

$$\sum _ { i = 1 } ^ { n } \left ( \Psi ( X _ { i } ) \Psi ( X _ { i } ) ^ { \top } - \mathbb { E } \left [ \Psi ( X _ { i } ) \Psi ( X _ { i } ) ^ { \top } \right ] \right ) ,$$

with Y ( x ) = Y 0,0 ( x ) , Y 1,1 ( x ) , . . . , Y 1, d 1 ( x ) , Y 2,1 ( x ) , . . . , Y 2, d 2 ( x ) , . . . , YR ,1 ( x ) , . . . , YR , dR ( x ) &gt; 2 R  ̃ R for all x 2 S d 1 . The proof of Proposition 2 also exploits concentration inequality for U-statistic dealing with a bounded, symmetric and -canonical kernel (see (De la Pena and Giné, 2012, Definition 3.5.1)). The first term on the right hand side of (8) is the bias arising from choosing a resolution level equal to R . Its behaviour as a function of R can be analyzed by considering some regularity condition on the envelope p .


<!-- p:17 -->


Assuming that p belongs to the Sobolev class Z s w (( 1, 1 )) (with regularity encoded by some parameter s &gt; 0) defined by

$$\left \{ g = \sum _ { k \geq 0 } g _ { k } ^ { * } c _ { k } G _ { k } ^ { \beta } \in L ^ { 2 } ( ( - 1 , 1 ) , w _ { \beta } ) \left | \left \| g \right \| _ { Z _ { w _ { \beta } } ^ { * } ( ( - 1 , 1 ) ) } ^ { * } \colon = \left [ \sum _ { l = 0 } ^ { \infty } d _ { l } | g _ { l } ^ { * } | ^ { 2 } \left ( 1 + ( l ( l + 2 \beta ) ) ^ { s } \right ) \right ] ^ { 1 / 2 } < \infty \right \} ,$$

and choosing the resolution level Ropt = δ ( n = log n ) 1 2 s + d 1 ε to balance the bias / variance tradeoff appearing on the right hand side of (8), we get that

$$\mathbb { E } \left [ \delta _ { 2 } ^ { 2 } ( \lambda ( T _ { n } ) , \lambda ^ { * } ) \right ] \lesssim \left [ \frac { n } { \log n } \right ] ^ { - \frac { 2 s } { 2 s + ( d - 1 ) } } .$$

Thus we recover a classical nonparametric rate of convergence for estimating a function with smoothness s in a space of dimension d 1. This is also the rate towards the probability matrix obtained by Xu (2018). Note that the choice of Ropt requires the knowledge of the regularity parameter s . To overcome this issue, De Castro et al. (2020) proposed an adaptive procedure using the Goldenshluger-Lepski method.

### 4.4 Estimation of the envelope function

Let us denote : = ( b Tn ) . For a prescribed model size R 2 N νφ 0 γ , De Castro et al. (2020) define the estimator b R of the truncated spectrum R : =( p 0 , p 1 , . . . , p 1 , . . . , p R , . . . , p R ) of as

$$\widehat { \lambda } ^ { R } \coloneqq ( p _ { 0 } ^ { R } ( \hat { \sigma } ) , p _ { 1 } ^ { R } ( \hat { \sigma } ) , \dots , p _ { 1 } ^ { R } ( \hat { \sigma } ) , \dots , p _ { 1 } ^ { R } ( \hat { \sigma } ) , \dots , p _ { R } ^ { R } ( \hat { \sigma } ) ) ,$$

with

$$\hat { \sigma } \in \arg \min _ { \sigma \in \mathfrak { S } _ { n } } \sum _ { l = 0 } ^ { R } \sum _ { k = \widetilde { l - 1 } } ^ { \widetilde { l } } \left ( p _ { l } ^ { R } ( \sigma ) - \lambda _ { \sigma ( k ) } \right ) ^ { 2 } + \sum _ { k = \widetilde { R } + 1 } ^ { n } \lambda _ { \sigma ( k ) } ^ { 2 } \quad \text {and} \quad p _ { l } ^ { R } ( \sigma ) = \frac { 1 } { d _ { l } } \sum _ { k = \widetilde { l - 1 } } ^ { \widetilde { l } } \lambda _ { \sigma ( k ) } , \\$$

where S n is the set of permutations of [ n ] and where we used the notation (7) with the convention 1 = 1. Using the results of the two previous subsections namely (6) and Proposition 2, we obtain (De Castro et al., 2020, Theorem.6) which states that

$$\mathbb { E } \left [ \delta _ { 2 } ^ { 2 } \left ( \widehat { \lambda } ^ { R _ { o p t } } , \lambda ^ { * } \right ) \right ] \lesssim \left [ \frac { n } { \log n } \right ] ^ { - \frac { 2 s } { 2 + ( d - 1 ) } } .$$

The envelope function p can then be approximated by the plug-in estimator b p P Ropt l = 0 p Ropt l ( ˆ ) clG l based on the decomposition (5). One drawback of this approach is the exponential complexity in R of the computation of b R . In the next section, we will describe an approach based on a Hierarchical Agglomerative Clustering algorithm to estimate the envelope function p efficiently .

### 4.5 Open problems and perspectives

The minimax rate of estimating a s -regular function on a space of (Riemannian) dimension d 1 such as S d 1 from n observations is known to be of order n s 2 s + d 1 . In the framework of this section, even if the domain of the envelope function p is [ 1, 1 ] , inputs of p are the pairwise distances given by inner products of points embedded in S d 1 . Hence it is still an open question to know if the dimension d of the latent space appears in the minimax rate of convergence. Moreover, the number of observations in the estimation problem considered is n 2 since the full adjacency matrix is known. Nevertheless the problem suffers from the presence of unobserved latent variables. This all contributes to a non standard estimation problem and finding the optimal rate of convergence is an open problem.


<!-- p:18 -->


## 5 Growth-model in RGGs

### 5.1 Description of the model

In Duchemin and De Castro (2022), a new growth model was introduced for RGGs. The so-called Markov Random Geometric Graph (MRGG) already presented in Definition 4 is a Soft-RGG where latent points are sampled with Markovian jumps. Namely, Duchemin and De Castro (2022) consider n points X 1 , X 2 , . . . , X n sampled on the Euclidean sphere S d 1 using a Markovian dynamic. They start by sampling uniformly X 1 on S d 1 . Then, for any i 2 φ 2, . . . , n γ , they sample

- a unit vector Yi 2 S d 1 uniformly, orthogonal to X i 1 ,
- a real r i 2 [ 1, 1 ] encoding the distance between X i 1 and X i , see (11). r i is sampled from a distribution f Λ : [ 1, 1 ] ! [ 0, 1 ] , called the latitude function ,

then X i is defined by

$$X _ { i } = r _ { i } \times X _ { i - 1 } + \sqrt { 1 - r _ { i } ^ { 2 } } \times Y _ { i } \, .$$

Figure 4: Visualization of the sampling scheme in S 2 .

This dynamic is illustrated with Figure 4 and can be understood as follows. Consider that X i 1 is the north pole, then choose uniformly a direction (i.e. a longitude) and, in an independent manner, randomly move along the latitudes (the longitude being fixed by the previous step). The geodesic distance i drawn on the latitudes satisfies

$$\gamma _ { i } = \arccos ( r _ { i } ) \, ,$$

where random variable r i = η X i , X i 1 ι has density f Λ ( r i ) .

### 5.2 Spectral convergences

In this framework and keeping the notations of the previous section, one can show that if p 2 Z s w (( 1, 1 )) and if f Λ satisfies the condition

$$( \mathcal { H } ) \quad \| f _ { \mathcal { L } } \| _ { \infty } \coloneqq \sup _ { t \in [ - 1 , 1 ] } | f _ { \mathcal { L } } ( t ) | < \infty \quad \text {and} \quad f _ { \mathcal { L } } \text { is bounded away from zero} ,$$

then

$$\mathbb { E } \left [ \delta _ { 2 } ^ { 2 } ( \lambda ( T _ { n } ) , \lambda ^ { * } ) \vee \delta _ { 2 } ^ { 2 } ( \lambda ^ { R _ { o p } } ( \widehat { T } _ { n } ) , \lambda ^ { * } ) \right ] = \mathcal { O } \left ( \left [ \frac { n } { \log ^ { 2 } ( n ) } \right ] ^ { - \frac { 2 s + d - 1 } { 2 s + d - 1 } } \right ) ,$$

with Ropt ( ˆ Tn ) = ( ˆ 1 , . . . , ˆ  ̃ Ropt , 0, 0, . . . ) and Ropt = β n = log 2 ( n ) 1 2 s + d 1 χ where ˆ 1 , . . . , ˆ n are the eigenvalues of b Tn sorted in decreasing order of magnitude. This result is the counterpart of Proposition 2 in this Markovian framework. The proof follows closely the steps of the one of the previous section but one needs to deal with the dependency of the latent positions. Results from Tropp (2015) are no longer suited to control the operator norm of (9) since ( X i ) i 0 is a Markov chain. Nevertheless, this can be achieved by using concentration inequalities for sum of functions of Markov chains and by exploiting the rank one structure of the random matrices Y ( X i ) Y ( X i ) &gt; together with a covering set argument. Another difficulty induced by the latent dynamic is the control of a U-statistic of order 2 of the Markov chain ( X i ) i 0 with a bounded kernel. Non-asymptotic results regarding the tail behaviour of U-statistics of a Markov chain have been so far very little touched. In a recent work, Duchemin et al. (2022) proved a concentration inequality for order 2 U-statistics with bounded kernels for uniformly ergodic Markov chain. Theorem 10 gives a simplified version of their main result. Assuming that the condition ( Η ) is fulfilled, the Markov chain ( X i ) i 1 satisfies the assumptions of Theorem 10 and one can show that (12) holds true.


<!-- p:19 -->


Theorem 10. (Duchemin et al., 2022, Theorem 2) Let us consider a Markov chain ( X i ) i 1 on some measurable space ( E , Ε ) (with E Polish) with transition kernel P : E E ! R and a function h : E E ! R . We assume that

1. ( X i ) i 1 is a uniformly ergodic Markov chain with invariant distribution ,
2. h is bounded and -canonical, namely

$$\forall x \in E , \quad \mathbb { E } _ { X \sim \pi } [ h ( X , x ) ] = \mathbb { E } _ { X \sim \pi } [ h ( x , X ) ] = 0 ,$$

3. there exist &gt; 0 and some probability measure on ( E , Ε ) such that

$$\forall x \in E , \, \forall A \in \mathcal { E } , \ \ P ( x , A ) \leq \delta \nu ( A ) .$$

Then there exist constants , &gt; 0 such that for any u 1 , it holds with probability at least 1 e u log n,

6

$$\frac { 1 } { n ( n - 1 ) } \sum _ { 1 \leq i , j \leq n , \, i \neq j } h ( X _ { i } , X _ { j } ) \leq \kappa \| h \| _ { \infty } \log n \left \{ \frac { u } { n } + \left [ \frac { u } { n } \right ] ^ { 2 } \right \} ,$$

where and only depend on constants related to the Markov chain ( X i ) i 1 .

Remark. Note that Theorem 10 holds for any initial distribution of the Markov chain. In their paper, Duchemin et al. (2022) go beyond the previous Hoeffding tail control by providing a Bernstein-type concentration inequality under the additional assumption that the chain is stationary. For the sake of simplicity we presented Theorem 10 for a single kernel h , but we point out that their results allow for the dependence of the kernels - say hi , j - on the indexes in the sums which brings technical difficulties since standard blocking techniques can no longer be applied. The interest for this concentration result goes beyond the scope of random graphs since U-statistics naturally arise in online learning Clémençon et al. (2008) or testing procedures Fromont and Laurent (2006).

### 5.3 Estimation procedure

Recalling the notation of the truncated spectrum R (resp. R ( b Tn ) ) of (resp. ( b Tn ) ) from Section 4.4, Duchemin and De Castro (2022) introduce a new procedure (namely the SCCHEi algorithm) based on a Hierarchical Agglomerative Clustering that returns a partition Χ d 0 , . . . , Χ dR , of the n eigenvalues of b Tn where for any i 2 φ 0, . . . , R γ , φΧ di φ = di (where we recall that di is the dimension of the space of spherical Harmonics of degree i ). The authors prove that for any fixed resolution level R , n can be chosen large enough so that the clusters obtained in polynomial time from the SCCHEi algorithm satisfy

$$\delta _ { 2 } ^ { 2 } ( \lambda ^ { * R } , \lambda ^ { R } ( \widehat { T } _ { n } ) ) = \sum _ { k = 0 } ^ { R } \sum _ { \hat { \lambda } \in \mathcal { C } _ { k } } ( \hat { \lambda } - p _ { k } ^ { * } ) ^ { 2 } .$$

The final estimate of the envelope function with resolution level R is defined as

$$\widehat { \mathbb { P } } \colon = \sum _ { k = 0 } ^ { R } \widehat { P } _ { k } G _ { k } ^ { \beta } , \quad \text {where} \quad \forall k \in \mathbb { N } , \quad \widehat { P } _ { k } = \left \{ \begin{array} { c c } \frac { 1 } { d _ { k } } \sum _ { \lambda \in \mathcal { C } _ { d _ { k } } } \lambda & \text {if } k \in \{ 0 , \dots , R \} \\ 0 & \text {otherwise.} \end{array}$$

Eq.(13) is not a sufficient condition to ensure that the L 2 error between the true envelope function and the plug-in estimator b p (see Eq.(14)) goes to 0 has n ! + 1 . This is due to identifiability issues coming from the 2 metric. In (Duchemin and De Castro, 2022, Theorem 3), the author obtain a theoretical guarantee on the L 2 error between the true envelope function and the plug-in estimate by considering additional assumptions on the eigenvalues ( p k ) k 0 . Let us finally mention that the optimal resolution level Ropt is unknown in practice. To bypass this issue, the authors propose a model selection procedure based on the slope heuristic (see Arlot (2019)).


<!-- p:20 -->


### 5.4 Non-parametric link prediction

We are now interesting in solving link prediction tasks. Namely, from the observation of the graph at time n , we want to estimate the probabilities of connection between the upcoming node n + 1 and the nodes already present in the graph. Recalling the definition of the random variables ( Yi ) i 2 from Section 5.1 and denoting further proj X ? n ( ) the orthogonal projection onto the orthogonal complement of Span ( Xn ) , the decomposition

$$\langle X _ { i } , X _ { n + 1 } \rangle = \langle X _ { i } , X _ { n } \rangle \langle X _ { n } , X _ { n + 1 } \rangle + \sqrt { 1 - \langle X _ { n } , X _ { n + 1 } \rangle ^ { 2 } } \sqrt { 1 - \langle X _ { i } , X _ { n } \rangle ^ { 2 } } \langle \frac { \ p r o j _ { X _ { n } ^ { 1 } } ( X _ { i } ) } { \| \ p r o j _ { X _ { n } ^ { 1 } } ( X _ { i } ) \| _ { 2 } } , Y _ { n + 1 } \rangle ,$$

shows that latent distances D 1: n =( η X i , X j ι ) 1 i , j n 2 [ 1, 1 ] n n are enough for link prediction. Indeed, it can be achieved by estimating the posterior probabilities defined for any i 2 [ n ] by

$$\eta _ { i } ( D _ { 1 ; n } ) & = \mathbb { P } \left ( A _ { i , n + 1 } = 1 \ | \ D _ { 1 ; n } \right ) \\ \eta _ { i } ( D _ { 1 ; n } ) & = \int _ { r , u ( - 1 , 1 ) } \mathbb { P } \left ( \langle X _ { i } , X _ { n } \rangle r + \sqrt { 1 - r ^ { 2 } } \sqrt { 1 - \langle X _ { i } , X _ { n } \rangle ^ { 2 } } u \right ) f _ { \mathcal { L } } ( r ) w _ { \frac { d - 3 } { 2 } } ( u ) \frac { \Gamma ( \frac { d - 1 } { 2 } ) } { \Gamma ( \frac { d - 2 } { 2 } ) \sqrt { \pi } } d r d u , \quad ( 1 6 )$$

where Ai , n + 1 2 φ 0, 1 γ is one if and only if node n + 1 is connected to node i , wd 3 2 ( u ) : = ( 1 u 2 ) d 3 2 1 2 and where : a 2 ] 0, + 1 [ 7! R + 1 0 t a 1 e t dt . Using an approach similar to Araya Valdivia and De Castro (2019), Duchemin and De Castro (2022) proved that one can get a consistent estimator b G of the Gram matrix of the latent positions G = η X i , X j ι 1 i , j n in Frobenius norm. Hence, one can use a traditional plug-in estimator for i ( D 1: n ) by replacing in (16) ( i ) the envelope function p by b p from (14), ( ii ) the pairwise distances by their estimates b Gi , j 1 i , j n and ( iii ) the latitude function f Λ by a non-parametric kernel density estimator built from the latent distances between consecutive nodes ( η X i , X i + 1 ι ) i 2 [ n 1 ] estimated by b Gi , i + 1 i 2 [ n 1 ] .

Through the example of MRGG, one can easily grasp the interest of growth model for random graphs with a geometric structure. Modeling the time evolution of networks, one can hope to solve tasks such as link prediction or collaborative filtering. An interesting research direction would be to extend the previous work to an anisotropic Markov kernel.

## 6 Connections with community based models

We have already described open problems and interesting directions to pursue regarding the questions tackled in the Sections 3, 4 and 5. In this last section, we want to look at RGGs from a different lens by highlighting a recently born line of research that investigates the connections between RGGs and community based models. Without aiming at presenting in a comprehensive manner the literature on this question, we rather focus on a few recent works that could inspire the reader to contribute in this emerging field.

A plenty number of random graph models have been so far studied. However real world problems never match a particular model and most of the time present several internal structures. To take into account this complexity, a growing number of works have been trying to take the best of several known random graph models. Papadopoulos et al. (2012) introduced a growth model where new connections with the upcoming node are drawn taking into account both popularity and similarity of vertices. The motivation is to find a balance between two trends for new connections in social networks namely homophily and popularity . One can also mention Jordan and Wade (2015) who consider a growth model that interpolates between pure preferential attachment (essentially the well-known Barabasi-Albert model) and a purely geometric model (the online nearest-neighbour graph). As pointed out by (Barthélemy, 2011, Section II.B.3.a), " it is clear that community detection in spatial networks is a very interesting problem which might receive a specific answer."


<!-- p:21 -->


### 6.1 Extension of RGGs to take into account community structure

6

Galhotra et al. (2017) proposed a new random graph model that incorporates community membership in standard RGGs. More precisely, they introduce the Geometric Block Model which is defined as follows. Consider V = V 1 τ V 2 τ   τ Vk a partition of [ n ] in k clusters, ( Xu ) u 2 [ n ] independent and identical random vectors uniformly distributed on S d 1 and let r i , j 1 i , j k 2 [ 0, 2 ] k k . The Geometric Block Model is a random graph with vertices V and an edge exists between v 2 Vi and u 2 Vj if and only if κ Xu X v κ r i , j . Focusing on the case where r i , i = r s , 8 i and r i , j = r d , 8 i = j , the authors want to recover the partition V observing only the adjacency matrix of the graph. They proved that in the relatively sparse regime (i.e. when r s , r d = n log n n ), a simple motif-counting algorithm allows to detect communities in the Geometric Block Model and is near-optimal. The proposed greedy algorithm affects two nodes to the same community if the number of their common neighbours lies in a prescribed range whose bounds depend on r s and r d that are assumed to be known. The method is proved to recover the correct partition of the nodes with probability tending to 1 as n goes to + 1 .

6

In Sankararaman and Baccelli (2017), the previous work is extended by considering arbitrary connection function. The paper sheds light on interesting differences between the standard SBMs and community models that incorporates some geometric structure. We start by presenting their model before highlighting some interesting results. Their model is the Planted Partition Random Connection Model (PPCM) that relies on a Poisson Point Process on R d with intensity &gt; 0 ' : = φ X 1 , X 2 , . . . γ where it is assumed that the enumeration of the points X i is such that for all i , j 2 N , i &gt; j = ) κ X i κ 1  κ X j κ 1 . Each atom i 2 N is marked with a random variable Zi 2 φ 1, + 1 γ . ' is the marked Poisson Point Process. The sequence φ Zi γ i 2 N is i.i.d. with each element being uniformly distributed in φ 1, + 1 γ . The interpretation of this marked point process is that for any node i 2 N , its location label is X i and its community label is Zi . Considering two connection functions f in , f out : R + ! [ 0, 1 ] , they first construct an infinite graph G with vertex set N and place an edge between any two nodes i , j 2 N with probability f in ( κ X i X j κ ) 1 Zi = Z j + f out ( κ X i X j κ ) 1 Zi = Z j . The graph Gn is then the induced subgraph of G consisting of the nodes 1 through Nn where Nn : = sup ƒ i 0 : X i 2 Bn : =[ n 1 = d 2 , n 1 = d 2 ] d ' . Considering that the graph is observed and that the connections functions f in , f out and the location labels ( X i ) i are known, the authors investigate conditions on the parameters of their model allowing to

extract information on the community structure from the observed data.

Weak recovery Weak Recovery is said to be solvable if for every n 2 N νφ 0 γ , there exists some algorithm that - based on the observed data Gn and ' - provides a sequence of φ 1, + 1 γ valued random variables φ ( n ) i γ Nn i = 1 such that there exists a constant &gt; 0 such that the overlap between φ ( n ) i γ Nn i = 1 and φ Zi γ Nn i = 1 is asymptotically almost surely larger than , namely

$$\lim _ { n \to \infty } \mathbb { P } \left ( \frac { \sum _ { i = 1 } ^ { N _ { n } } \tau _ { i } ^ { ( n ) } Z _ { i } } { N _ { n } } \geq \gamma \right ) = 1 .$$

The authors identify regimes where weak recovery can be solved or not. We summarize their results with Proposition 3.

6

Proposition 3. (Sankararaman and Baccelli, 2017, Proposition 1 - Corollary 2 - Theorem 2) For every f in ( ) , f out ( ) such that φ r 2 R + : f in ( r ) = f out ( r ) γ has positive Lebesgue measure and any d 2 , there exists a c 2 ( 0, 1 ) such that

- for any &lt; c , weak recovery is not solvable.
- for any &gt; c , there exists an algorithm (which could possibly take exponential time) to solve weak recovery.

Moreover, there exists  ̃ c &lt; 1 (possibly larger than c ) depending on f in ( ) , f out ( ) and d, such that for all &gt;  ̃ c , weak recovery is solvable in polynomial time.

The intrinsic nature of the problem of weak recovery is completely different in the PPCM model compared to the standard sparse SBM. Sparse SBMs are known to be locally tree-like with very few short cycles. Efficient algorithms that solve weak recovery in the sparse SBM (such as message passing algorithm, convex relaxation or spectral methods) deeply rely on the local tree-like structure. On the contrary, PPCMs are locally dense even if their are globally sparse. This is due to the presence of a lot of short loops (such as triangles). As a consequence, the standard tools used for SBMs are not relevant to solve weak recovery in PPCMs. Nevertheless, the local density allows to design a polynomial time algorithm that solves weak recovery for &gt;  ̃ c (see Proposition 3) by simply considering the neighbours of each node. Proposition 3 lets open the question of the existence of a gap between information versus computation thresholds. Namely, is it always possible to solve weak recovery in polynomial time when &gt; c ? In the sparse and symmetric SBM, it is known that there is no information-computation gap for k = 2 communities, while for k 4 a non-polynomial algorithm is known to cross the Kesten-Stigum threshold which was conjectured by Decelle et al. (2011) to be the threshold at which weak recovery can be solved efficiently.


<!-- p:22 -->


6

Distinguishability The distinguishability problem asks how well one can solve a hypothesis testing problem that consists in finding if a given graph has been sampled from the PPCM model or from the null, which is given by a plain random connection model with connection function ( f in ( ) + f out ( )) = 2 without communities but having the same average degree and distribution for spatial locations. Sankararaman and Baccelli (2017) prove that for every &gt; 0, d 2 N and connection functions f in ( ) and f out ( ) satisfying 1 f in ( r ) f out ( r ) 0 for all r 0, and φ r 0 : f in ( r ) = f out ( r ) γ having positive Lebesgue measure, the probability distribution of the null and the alternative of the hypothesis test are mutually singular. As a consequence, there exists some regimes (such as &lt; c and d 2) where we can be very sure by observing the data that a partition exists, but cannot identify it better than at random. In these cases, it is out of reach to bring together the small partitions of nodes in different regions of the space into one coherent. Such behaviour does not exist in the sparse SBM with two communities as proved by Mossel et al. (2014) and was conjectured to hold also for k 3 communities in Decelle et al. (2011).

### 6.2 Robustness of spectral methods for community detection with geometric perturbations

In another line of work, Péché and Perchet (2020) are studying robustness of spectral methods for community detection when connections between nodes are perturbed by some latent random geometric graph. They identify specific regimes in which spectral methods are still efficient to solve community detection problems despite geometric perturbations and we give an overview of their work in what follows. Let us consider some fixed parameter 2 [ 0, 1 ] that drives the balance between strength of the community signal and the noise coming from the geometric perturbations. For sake of simplicity, they consider a model with two communities where each vertex i in the network is characterized by some vector X i 2 R 2 with distribution Ν ( 0, I 2 ) . They consider p 1 , p 2 2 ( 0, 1 ) that may depend on the number of nodes n with p 1 &gt; p 2 and sup n p 1 = p 2 &lt; 1 . Assuming for technical reason + max φ p 1 , p 2 γ 1, the probability of connection between i and j is

$$\mathbb { P } \left \{ i \sim j \, | \, X _ { i } , X _ { j } \right \} = \kappa \exp \left ( - \gamma \| X _ { i } - X _ { j } \| ^ { 2 } \right ) + \left \{ \begin{array} { c c } \ p _ { 1 } & \text {if $i$ and $j$ belong to the same community} \\ \ p _ { 2 } & \text {otherwise.} \end{array} \right \} \, ,$$

where the inverse width &gt; 0 may depend on n . We denote by 2 φ 1 = π n γ n the normalized community vector illustrating to which community each vertex belong ( i = 1 = π n if i belongs to the first community and i = 1 = π n otherwise). The matrix of probabilities of this model is given by Q : = P 0 + P 1 where

$$P _ { 0 } \colon = \begin{bmatrix} p _ { 1 } J & p _ { 2 } J \\ p _ { 2 } J & p _ { 1 } J \end{bmatrix} \ \text {and} \ \ P _ { 1 } \colon = \kappa P = \kappa \left ( ( 1 - \delta _ { i , j } ) e ^ { - \gamma \| X _ { i } - X _ { j } \| ^ { 2 } } \right ) _ { 1 \leq i , j \leq n } .$$

The adjacency matrix A of the graph can thus be written as A = P 0 + P 1 + Ac where Ac is, conditionnally on the X i 's, a random matrix with independent Bernoulli entries which are centered. Given the graphadjacency matrix A , the objective is to output a normalized vector x 2 φ 1 = π n γ n such that, for some " &gt; 0,

- Exact recovery: with probability tending to 1, φ &gt; x φ = 1,
- Weak recovery (also called detection): with probability tending to 1, φ &gt; x φ &gt;" .


<!-- p:23 -->


Let us highlight that contrary to the previous section, the latent variables ( X i ) i are not observed. When = 0, we recover the standard SBM: Q = P 0 has two non zero eigenvalues which are 1 = n ( p 1 + p 2 ) = 2 with associated normalized eigenvector v 1 = 1 π n ( 1, 1, . . . , 1 ) &gt; and 2 = n ( p 1 p 2 ) = 2 associated to v 2 = = 1 π n ( 1, . . . , 1, 1, . . . , 1 ) &gt; . Spectral methods can thus be used to recover communities by computing the second eigenvector of the adjacency matrix A . To prove that spectral methods still work in the presence of geometric perturbations, one needs to identify regimes in which the eigenvalues of A are well separated and the second eigenvector is approximately v 2 .

In the regime where n = log n , the spectral radius ( P 1 ) of P 1 vanishes and we asymptotically recover a standard SBM. Hence, they focus on the following regime

$$\gamma _ { \underset { n \to \infty } { \rightarrow } \infty } \ \text { and } \ \frac { 1 } { \gamma } \frac { n } { \ln n } \underset { n \to \infty } { \rightarrow } \infty .$$

Under Assumption ( A 1 ), (Péché and Perchet, 2020, Proposition 2) states that with probability tending to one, ( P 1 ) is of order n 2 . Using (Benaych-Georges et al., 2020, Theorem 2.7) to get an asymptotic upperbound on the spectral radius of Ac , basic perturbation arguments would prove that standard techniques for community detection work in the regime where

$$\frac { \kappa n } { 2 \gamma } \ll \sqrt { \frac { n ( p _ { 1 } + p _ { 2 } ) } { 2 } } = \sqrt { \lambda _ { 1 } } .$$

Indeed, it is now well-known that weak recovery in the SBM can be solved efficiently as soon as 2 &gt; p 1 (for example using the power iteration algorithm on the non-backtracking matrix from Bordenave et al. (2015)). Hence, the regime of interest correspond to the case where

$$\exists c , C > 0 \ \ s . t . \quad \lambda _ { 2 } ^ { - 1 } \frac { \kappa n } { 2 \gamma } \in [ c , C ] , \quad \frac { \lambda _ { 2 } } { \lambda _ { 1 } } \in [ c , C ] \ \text { and } \ \lambda _ { 2 } \gg \sqrt { \lambda _ { 1 } } , \quad \\$$

which corresponds to the case where the noise induced by the latent random graph is of the same order of magnitude as the signal. Under ( A 2 ), the problem of weak recovery can be tackled using spectral methods on the matrix S = P 0 + P 1 : the goal is to reconstruct communities based on the second eigenvector of S . To prove that these methods work, the authors first find conditions ensuring that two eigenvalues of S exit the support of the spectrum of P 1 . Then, they provide an asymptotic lower bound for the level of correlation between v 2 = and the second eigenvector w 2 of S , which leads to Theorem 11.

####### Theorem 11. (Péché and Perchet, 2020, Theorem 10)

Suppose that Assumptions ( A 1 ) and ( A 2 ) hold and that 1 &gt; 2 + 2 2 . Then the correlation φ w &gt; 2 v 2 φ is uniformly bounded away from 0 . Moreover, denoting 1 the largest eigenvalue of P 1 , if the ratio 2 = 1 goes to infinity then φ w &gt; 2 v 2 φ tends to 1 , which gives weak (and even exact at the limit) recovery.

### 6.3 Recovering latent positions

From another viewpoint, one can think RGGs as an extension of stochastic block models where the discrete community structure is replaced by an underlying geometry. With this mindset, it is natural to directly transport concepts and questions from clustered random graphs to RGGs. For instance, the task consisting in estimating the communities in SBMs may correspond to the estimation of latent point neighborhoods in RGGs. More precisely, community detection can be understood in RGGs as the problem of recovering the geometric representation of the nodes (e.g. through the Gram matrix of the latent positions). This question has been tackled by Eldan et al. (2020) and Araya Valdivia (2020). Both works consider random graphs sampled from the TIRGG model on the Euclidean sphere S d 1 with some envelope function p (see Definition 3), leading to a graphon model similar to the one presented in Section 4.1. While the result from Araya Valdivia (2020) holds in the dense and relatively sparse regimes, the one from Eldan et al. (2020) covers the sparse case. Thanks to harmonic properties of S d 1 , the graphon eigenspace composed only with linear eigenfunctions (harmonic polynomials of degree one) directly relates to the pairwise distances of the latent positions. This allows Eldan et al. (2020) and Araya Valdivia (2020) to provide a consistent estimate of the Gram matrix of the latent positions in Frobenius norm using a spectral method. Their results hold under the following two key assumptions.


<!-- p:24 -->


1. An eigenvalue gap condition. They assume that the d eigenvalues of the integral operator T W - associated with the graphon W : = p ( η , ι ) (see (4)) - corresponding to the Spherical Harmonics of degree one is well-separated from the rest of the spectrum.
2. A regularity condition. They assume that the envelope function p belongs to some Weighted Sobolev space, meaning that the sequence of eigenvalues of T W goes to zero fast enough.

6

In addition to similar assumptions, Eldan et al. (2020) and Araya Valdivia (2020) share the same proof structure. First they need to recover the d eigenvectors from the adjacency matrix corresponding to the space of spherical Harmonics of degree one. Then the Davis-Kahan Theorem is used to prove that the estimate of the Gram matrix based on the previously selected eigenvectors is consistent in Frobenius norm. To do so, they require a concentration result ensuring that the adjacency matrix A (or some proxy of it) converges in operator norm towards the matrix of probabilities with entries i , j = p η X i , X j ι for 1 i = j n and zero diagonal entries. Araya Valdivia (2020) relies on (Bandeira and van Handel, 2016, Corollary 3.12), already discussed in (6), that provides the convergence κ A κ ! 0 as n !1 in the dense and relatively sparse regimes. In the sparse regime, such concentration no longer holds. Indeed, in that case, degrees of some vertices are much higher than the expected degree, say deg. As a consequence, some rows of the adjacency matrix A have Euclidean norms much larger than p deg, which implies that for n large enough, it holds with high probability κ A κ p deg. To cope with this issue, Eldan et al. (2020) do not work directly on the adjacency matrix but rather on a slightly amended version of it - say A 0 - where one reduces the weights of the edges incident to high degree vertices. In that way, all degrees of the new (weighted) network become bounded, and (Le et al., 2018, Theorem 5.1) ensures that A 0 converges to in spectral norm as n goes to + 1 . Hence in the sparse regime the adjacency matrix converges towards its expectation after regularization . The proof of this random matrix theory tool is based on a famous result in functional analysis known as the Grothendieck-Pietsch factorization. Let us finally mention that this change of behaviour of the extreme eigenvalues of the adjacency matrix according to the maximal mean degree has been studied in details for inhomogeneous Erdös-Rényi graphs

in Benaych-Georges et al. (2020) and Benaych-Georges et al. (2019).

### 6.4 Some perspectives

The paper Sankararaman and Baccelli (2017) makes the strong assumption that the locations labels ( X i ) i 1 are known. Hence it should be considered as an initial work calling for future theoretical and practical investigations. Keeping the same model, it would be of great interest to design algorithms able to deal with unobserved latent variables to allow real-data applications. A first step in this direction was made by Avrachenkov et al. (2021) where the authors propose a spectral method to recover hidden clusters in the Soft Geometric Block Model where latent positions are not observed. On the theoretical side, Sankararaman and Baccelli (2017) describe at the end of their paper several open problems. Their suggestions for future works include i ) the extension of their work to a larger number of communities, ii ) the estimation from the data of the parameters of their model (namely f in and f out that they assumed to be known), and iii ) the existence of a possible gap between information versus computation thresholds, namely, they wonder if there is a regime where community detection is solvable, but without any polynomial (in n ) time and space algorithms.

Another possible research direction is the extension of the work from Section 6.2 to study the same kind of robustness results for more than 2 communities and especially in the sparse regime where 1 pi 1 n . As highlighted by Péché and Perchet (2020), the sparse case may bring additional difficulties since " standard spectral techniques in this regime involve the non-backtracking matrix (see Bordenave et al. (2015)), and its concentration properties are quite challenging to establish." Regarding Section 6.3, for some applications it may be interesting to go beyond the recovery of the pairwise distances by embedding the graph in the latent space while preserving the Gram structure. Such question has been tackled for example by Perry et al. (2020) but only for the Euclidean sphere in small dimensions.


<!-- p:25 -->


Acknowledgements The authors are in debt to Tselil Schramm who gave a great talk at the S.S.Wilks Memorial Seminar in Statistics (at Princeton University) providing insightful comments on the problem of geometry detection or more specifically on her paper Liu et al. (2021).

## A Outline of the proofs of Theorems 6 and 7

The proofs of Theorems 6 and 7 (cf. Section 3.3) are quite complex and giving their formal descriptions would require heavy technical considerations. In the following, we provide an overview of the proofs highlighting the nice mathematical tools used by Liu et al. (2021) and their innovative combination while putting under the rug some technical aspects.

Step 1. Relate the TV distance of the whole graphs to single vertex neighbourhood.

$$2 T V ( G ( n , p , d ) , G ( n , p ) ) ^ { 2 } & \leq K L ( G ( n , p , d ) | G ( n , p ) ) \quad \text {from Pinsker's inequality} \\ & \leq n \times E _ { G _ { n - 1 } \sim G ( n - 1 , p , d ) } \left [ K L ( \nu _ { n } ( \cdot | G _ { n - 1 } ) , B e rn ( p ) ^ { \otimes ( n - 1 ) } ) \right ] & \quad \text {from Lemma 2} \\ & = E _ { G _ { n - 1 } \sim G ( n - 1 , p , d ) } E _ { S \sim \nu _ { n } ( | G _ { n - 1 } ) } \log \left ( \frac { \nu _ { n } ( S | G _ { n - 1 } ) } { p ^ { | S | ( 1 - p ) ^ { n - 1 } | S | } } \right ) , \\ \intertext { w h e r $ \nu ( | G | \cdot \detanotes the distribution of the n a \text { neighbourhood of vertex $n$ when the graph is } }$$

where n ( φ Gn 1 ) denotes the distribution of the neighbourhood of vertex n when the graph is sampled from G ( n , p , d ) conditional on the knowledge of the connections between pairs of nodes in [ n 1 ] given by Gn 1 . Hence, the main difference with Brennan et al. (2020) is that the tensorization argument from Lemma 2 is used node-wise (and not edge-wise). We are reduced to understand how a vertex incorporates a given graph of size n 1 sampled from the distribution G ( n 1, p , d ) . At a high level, the authors show that if one can prove that for some " &gt; 0, with high probability over Gn 1 G ( n 1, p , d ) , it holds

$$\forall S \subseteq [ n - 1 ] , \quad \nu _ { n } ( S | G _ { n - 1 } ) = \mathbb { P } _ { G \sim G ( n , p , d ) } ( N _ { G } ( n ) = S | \, G _ { n - 1 } ) = ( 1 \pm \varepsilon ) p ^ { | S | } ( 1 - p ) ^ { n - 1 - | S | } , \quad ( 1 8 )$$

where NG ( n ) denotes the set of nodes connected to node n in the graph G , then

$$T V ( G ( n , p , d ) , G ( n , p ) ) = o _ { n } ( n \varepsilon ^ { 2 } ) .$$

Step 2. Geometric interpretation of neighbourhood probabilities from Eq.(18).

For G G ( n , p , d ) , if vertex i is associated to a (random) vector X i , and ( i , j ) is an edge, we consequently know that η X i , X j ι t p , d . On the sphere S d 1 , the locus of points where X j can be, conditioned on ( i , j ) being an edge, is a sphere cap centered at X i with a p fraction of the sphere's surface area, which we denote by cap ( X i ) . Similarly, if we know that i and j are not adjacent, the locus of points where X j can fall is the complement of a sphere cap with measure 1 p namely cap ( X i ) , which we call an 'anti-cap'. Let us denote is the normalized Lebesgue measure on S d 1 so that ( S d 1 ) = 1. Equipped with this geometric picture, we can view the probability that vertex n 's neighborhood is exactly equal to S [ n 1 ] as ( L S ) , where L S S d 1 is a random set defined by

$$L _ { S } \coloneqq ( \bigcap _ { i \in S } \cap ( X _ { i } ) ) \cap ( \bigcap _ { j \notin S } \overline { \cap ( X _ { j } ) } ) .$$

To show that the TV distance between G ( n , p , d ) and G ( n , p ) is small, we need to prove that ( L S ) concentrates around p φ S φ ( 1 p ) n 1 φ S φ as suggested by Eqs.(18) and (19).

Step 3. S d 1

- Concentration of measure of intersections of sets in with random spherical caps. An essential contribution of Liu et al. (2021) is a novel concentration inequality for the area of the intersection of a random spherical cap with any subset L S d 1 .

Lemma 3. (see Liu et al., 2021, Corollary 4.10) Set-cap intersection concentration Lemma. Suppose L S d 1 and let us denote by the uniform probability measure on S d 1 . Then with high probability over z it holds

$$| \frac { \sigma ( L \cap \text {cap} ( z ) ) } { p \sigma ( L ) } - 1 | = \mathcal { O } _ { n } \left ( \delta _ { n } ( L ) \right ) \ \ a n d \quad | \frac { \sigma ( L \cap \overline { \text {cap} ( z ) } ) } { ( 1 - p ) \sigma ( L ) } - 1 | = \mathcal { O } _ { n } ( \frac { p } { 1 - p } \delta _ { n } ( L ) ) ,$$


<!-- p:26 -->


$$w h e r e \ \delta _ { n } ( L ) = \sqrt { \frac { \log \frac { 1 } { p } + \log \frac { 1 } { \sigma ( L ) } } { \sqrt { d } } } \text {polylog(n)} .$$

Sketch of proof of Lemma 3. We give an overview of the proof of Lemma 3, highlighting its interesting connection with optimal transport. Let us consider some probability distribution on S d 1 . Let us denote ∆ the optimal coupling between the measures and , i.e. ∆ is a probability measure on S d 1 S d 1 with marginals and such that

$$W _ { 2 } ( \nu , \sigma ) ^ { 2 } = \int \| x - y \| _ { 2 } ^ { 2 } d \mathcal { D } ( x , y ) ,$$

where W 2 ( , ) is the Wasserstein 2-distance between the measures and . Then for any z 2 S d 1 it holds

$$\mathbb { P } _ { x \sim v } ( \langle z , x \rangle > t _ { p , d } ) = & \mathbb { P } _ { ( x , y ) \sim \mathcal { B } } ( \langle z , y \rangle > t _ { p , d } - \langle z , x - y \rangle ) \\ \leq & \mathbb { P } _ { y \sim \sigma } ( \langle z , y \rangle > t _ { p , d } - u ( p , d ) ) + \mathbb { P } _ { ( x , y ) \sim \mathcal { B } } ( | \langle z , x - y \rangle | > u ( p , d ) ) ,$$

for some well chosen threshold u ( p , d ) depending on p and d . The first term in the right hand side of Eq.(20) can be proven to concentrate around p with high probability over z with standard arguments. The second term in Eq.(20) quantifies how often a randomly chosen transport vector x y with ( x , y ) ∆ has a large projection in the direction z . One can prove that the optimal transport map ∆ between x and y has bounded length with high probability, and then translate this into a tail bound for the inner product η z , x y ι for a random vector z . As a consequence, one can bound with high probability over z the fluctuations of P x ( η z , x ι &gt; t p , d ) p which gives Lemma 3 if we take for the uniform measure on the set L S d 1 . □

Applying Lemma 3 inductively and using a martingale argument, the authors prove that intersecting j random caps and ( k j ) random anticaps, we get a multiplicative fluctuation for ( L S ) around p φ S φ ( 1 p ) n 1 φ S φ that is of the order of ( 1 p j + p k j p 1 p ) . Going back to Eq.(19), this approach is sufficient to prove that

$$T V ( G ( n , p , d ) , G ( n , p ) ) = o _ { n } ( \frac { n ^ { 3 } p ^ { 2 } } { d } ) ,$$

leading to the first statement of Theorem 7.

Step 4. The sparse case and the use of the cavity method.

To get down to a polylogarithmic threshold in the sparse regime, the authors change of paradigm. Previously, they were bounding the quantity

$$\mathbb { P } _ { G \sim G ( n , p , d ) } ( N _ { G } ( n ) = S \, | \, G _ { n - 1 } ) = \mathbb { E } _ { X _ { 1 } , \dots , X _ { n - 1 } | \, G _ { n - 1 } } \mathbb { E } _ { X _ { n } , \sim \sigma } [ 1 _ { N _ { C } ( n ) = S } ] = \mathbb { E } _ { X _ { 1 } , \dots , X _ { n - 1 } | \, G _ { n - 1 } } \left [ \sigma ( L _ { S } ) \right ] ,$$

by fixing a specific realization of latent positions X 1 , . . . X n 1 and then analyzing the probability that the node n connects to some S [ n 1 ] . The probability that vertex n is adjacent to all vertices in S [ n 1 ] is exactly equal to the measure of the set-caps intersection, which appears to be tight. At a high level, this is a "worst case approach" to upper bound Eq.(21) in the sense that the bound obtained from this analysis may be due to an unlikely latent configuration conditioned on X 1 , . . . , X n 1 producing Gn 1 . To obtain a polylogarithmic threshold in the sparse case, one needs to analyze the concentration of ( L S ) on average over vector embeddings of Gn 1 . To do so, the authors rely on the so-called cavity method borrowed from the field of statistical physics. The cavity method allows to understand the distribution of ( X i ) i 2 S conditional on forming Gn 1 for any S [ n 1 ] with size of the order pn = ( 1 ) . We provide further details on this approach in the following.


<!-- p:27 -->


A simplification using tight concentration for intersections involving anti-caps. Liu et al. (2021) first prove that due to tight concentration for the measure of the intersection of random anticaps with sets of lower bounded measure, one can get high-probability estimates for n ( S φ Gn 1 ) by studying the probability that S NG ( n ) , namely

$$\mathbb { P } ( S \subseteq N _ { G } ( n ) \, | \, G _ { n - 1 } ) = \mathbb { P } \left ( \forall i \in S , \, \langle X _ { i } , X _ { n } \rangle \geq t _ { p , d } \, | \, G _ { n - 1 } \right ) = \sum _ { \substack { X _ { n } ^ { \prime } \sim \sigma ^ { \prime } \\ ( X _ { i } ) _ { i } \in [ n - 1 ] } } \mathbb { E } \prod _ { i \in S } 1 _ { \{ X _ { i } , X _ { n } \rangle \geq t _ { p , d } } , \quad ( 2 2 )$$

where Gn 1 : = ( n 1 ) φ Gn 1 . If ( X i ) i 2 S in Eq.(22) was a collection of independent random vectors distributed uniformly on the sphere then Eq.(22) would be exactly equal to p φ S φ . In the following, we explain how the authors prove that both of these properties are approximately true.

The cavity-method. To bound the fluctuation of Eq.(22) around p φ S φ , Liu et al. (2021) use the cavity-method. Let us consider S [ n 1 ] , Gn 1 sampled from G ( n 1, p , d ) and its corresponding latent vectors. Let us denote by Β Gn 1 ( i , ' ) the ball of radius-' around a vertex i 2 [ n 1 ] in the graph Gn 1 . Fixing all vectors except those in K : = S i 2 S Β Gn 1 ( i , ' 1 ) , the cavity method aims at computing the joint distribution of ( X i ) i 2 S conditional to ( X i ) i = 2 K and Gn 1 . Informally speaking, we "carve out" a cavity of depth ' around each vertex i 2 S and we fix all latent vectors outside of these cavities as presented with Figure 5. The choice of the depth ' results from the following tradeoff:

Figure 5: Illustration of the cavity method to bound the fluctuation of Eq.(22) around p φ S φ i.e., to bound the deviation of the random variable ( L S ) conditioned on X 1 , . . . , X n 1 producing Gn 1 . With high probability, the neighbourhood until depth ' = log n loglog n of vertices in S are disjoint trees. We fix the latent representation of vertices in the set R : = [ n 1 ] ν K . Using the Belief Propagation algorithm, one can compute the distribution of ( X i ) i 2 S φ ( X j ) j 2 R where the latent positions ( X j ) j 2 [ n 1 ] are sampled according to Gn 1 . This allows to bound the fluctuation of Eq.(22) around p φ S φ .

- We want to choose the depth ' small enough so that the balls Β Gn 1 ( i , ' ) for i 2 S are all trees and are pairwise disjoint with high probability.
- We want to choose ' as large as possible in order to get a bound on the fluctuations of Eq.(22) around p φ S φ as small as possible.

To formally analyze the distribution of the unfixed vectors upon resampling them, the authors set up a constraint satisfaction problem instance over a continuous alphabet that encodes the edges of Gn 1 within the trees around S : each node has a vector-valued variable in S d 1 , and the constraints are that nodes joined by an edge must have vectors with inner product at least t p , d . The marginal of the latent vectors X i for i 2 S can be obtained using the Belief-Propagation algorithm. Let us recall that Belief-Propagation computes marginal distributions over labels of constraints satisfaction problems when the constraints graph is a tree.

A simple analysis of Belief-Propagation. To ease the reasoning, let us suppose that 1 2 S is such that Β Gn 1 ( 1, ' 1 ) is a path. Without loss of generality, we consider that the path is given by Figure 6. Every vector is passing to its parent along the path a convolution of its own measure (corresponding to its "message") with a cap of measure p . Denoting by P the linear operator defined so that for any function h : S d 1 ! R ,


<!-- p:28 -->


Figure 6: Simple analysis of the Belief Propagation algorithm when the neighbourhood of vertex 1 2 S at depth ' is a path.

$$P h ( x ) = \frac { 1 } { p } \int _ { \text {cap} ( x ) } h ( y ) d \sigma ( y ) ,$$

the authors prove that for some a &gt; 0, for any probability measure on S d 1 with density h with respect to ,

$$T V ( P h , \sigma ) \leq \mathcal { O } _ { n } ( \frac { \log ^ { a } n } { \sqrt { d } } ) T V ( \mu , \sigma ) ,$$

which is a contraction result. Since at every step of the Belief Propagation algorithm, a vertex sends to its parent the image by the operator P of its own measure, we deduce from Eq.(23) that the parent receives a measure which is getting closer to the uniform distribution by a multiplicative factor equal to 1 π d . The proof of Eq.(23) relies on the set-cap intersection concentration result (see Lemma 3). To get an intuition of this connection, let us consider that h is the density of the uniform probability measure on some set L S d 1 , then

$$P h ( x ) = \frac { 1 } { p } P _ { Y \sim \mu } ( Y \in \text {cap} ( x ) ) = \frac { 1 } { p } \frac { \sigma ( L \cap \text {cap} ( x ) ) } { \sigma ( L ) } ,$$

and we can conclude using Lemma 3 that ensures that with high probability over x , ( L ∴ cap ( x )) = ( 1 Ο n ( log a n π d )) p ( L ) . Applying Eq.(23) ' = log n loglog n times for d being some power of log n , one can show that,

$$T V ( P ^ { \ell } \mu , \sigma ) = \mathcal { O } _ { n } [ ( \frac { \log ^ { a } n } { \sqrt { d } } ) ^ { \ell } ] = o _ { n } ( \frac { 1 } { \sqrt { n } } ) .$$

With this approach, one can prove that the distribution of ( X i ) i 2 S is approximately φ S φ . This allows to bound the fluctuations of Eq.(22) around p φ S φ which leads to Theorem 6 using Eqs.(18) and (19).

As a concluding remark, we mention that Liu et al. (2021) demonstrate a coupling of G G ( n , p on ( p )) , G G ( n , p , d ) , and G + G ( n , p + on ( p )) that satisfies G G G + with high probability. This sandwich-type result holds for a proper choice of the latent dimension and allows to transfer known properties of Erdös-Renyi random graphs to RGGs in the studied regime. For example, the authors use this coupling result to upper bound the probability that the depth-' neighborhood of some i 2 [ n ] forms a tree under G ( n , p , d ) in the sparse regime with d = polylog ( n ) .


<!-- p:29 -->
