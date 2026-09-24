---
id: "Baccelli-Blaszczyszyn_2010_Stochastic-Geometry-Wireless-Networks-I"
source_pdf: "../pdf/Baccelli-Blaszczyszyn_2010_Stochastic-Geometry-Wireless-Networks-I.pdf"
source_filename: "Baccelli-Blaszczyszyn_2010_Stochastic-Geometry-Wireless-Networks-I.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "full-page-ocr"
extraction_quality: "excellent"
extraction_score: 100.0
visual_assets: "disabled"
references_file: "../references/Baccelli-Blaszczyszyn_2010_Stochastic-Geometry-Wireless-Networks-I.references.md"
---

<!-- p:1 -->

Foundations and Trends® in Networking Vol. 3, Nos. 3-4 (2009) 249–449 © 2009 F. Baccelli and B. Błaszczyszyn DOI: 10.1561/1300000006

mou

the essence of knowledge

### Stochastic Geometry and Wireless Networks: Volume I Theory

By François Baccelli and Bartłomiej Błaszczyszyn

### Contents

|   I | Classical Stochastic Geometry                |   259 |
|-----|----------------------------------------------|-------|
|   1 | Poisson Point Process                        |   261 |
| 1.1 | Definition and Characterizations             |   262 |
| 1.2 | Laplace Functional                           |   266 |
| 1.3 | Operations Preserving the Poisson Law        |   269 |
| 1.4 | Palm Theory                                  |   276 |
| 1.5 | Strong Markov Property                       |   282 |
| 1.6 | Stationarity and Ergodicity                  |   284 |
|   2 | Marked Point Processes and Shot-Noise Fields |   291 |
| 2.1 | Marked Point Processes                       |   291 |
| 2.2 | Shot-Noise                                   |   300 |
| 2.3 | Interference Field as Shot-Noise             |   305 |
| 2.4 | Extremal Shot-Noise                          |   316 |
|   3 | Boolean Model                                |   318 |
| 3.1 | Boolean Model as a Coverage Process          |   318 |
| 3.2 | Boolean Model as a Connectivity Model        |   329 |


<!-- p:2 -->


| 4                               | Voronoi Tessellation                                                         |   338 |
|---------------------------------|------------------------------------------------------------------------------|-------|
| 4.1                             | Introduction                                                                 |   338 |
| 4.2                             | The Inverse Formula of Palm Calculus                                         |   340 |
| 4.3                             | The Neveu Exchange Formula                                                   |   343 |
| 4.4                             | Neighbors in the Voronoi Tessellation, Delaunay Triangulation                |   345 |
| 4.5                             | The Voronoi Tessellation Model for Cellular Access Networks                  |   347 |
| Bibliographical Notes on Part I | Bibliographical Notes on Part I                                              |   350 |
| II                              | Signal-to-Interference Ratio Stochastic Geometry                             |   351 |
| 5                               | Signal-to-Interference Ratio Cells                                           |   353 |
| 5.1                             | Introduction                                                                 |   353 |
| 5.2                             | The Signal-to-Interference Ratio Cell is Well-Defined                        |   355 |
| 5.3                             | Standard Stochastic Scenario and First Order Cell Characteristics            |   355 |
| 5.4                             | Fading in Signal-to-Interference Ratio Cell and Higher Order Characteristics |   360 |
| 5.5                             | Noise or Interference Limited Cell: Towards a Boolean or Voronoi Shape       |   362 |
| 6                               | Interacting Signal-to-Interference Ratio Cells                               |   377 |
| 6.1                             | Introduction                                                                 |   377 |
| 6.2                             | Constraints on Cell Intersections                                            |   379 |
| 6.3                             | Stochastic Scenarios and Coverage Probabilities                              |   380 |
| 6.4                             | Joint Point-Coverage Probability                                             |   380 |
| 7                               | Signal-to-Interference Ratio Coverage                                        |   383 |
| 7.1                             | Introduction                                                                 |   383 |
| 7.2                             | Typical Cell of the Coverage Process                                         |   385 |
| 7.3                             | Nearest Transmitter Cell                                                     |   386 |


<!-- p:3 -->


| 7.4                                       | Ξ SINR as a Random Closed Set                                      |   388 |
|-------------------------------------------|--------------------------------------------------------------------|-------|
| 7.5                                       | The Coverage Process Characteristics                               |   392 |
| 8                                         | Signal-to-Interference Ratio Connectivity                          |   401 |
| 8.1                                       | Introduction                                                       |   401 |
| 8.2                                       | Signal-to-Interference Ratio Graph                                 |   401 |
| 8.3                                       | Percolation of the Signal-to-Interference Ratio Connectivity Graph |   402 |
| Bibliographical Notes on Part II          | Bibliographical Notes on Part II                                   |   410 |
| III                                       | Appendix: Mathematical Complements                                 |   411 |
| 9 Higher Order Moment Measures of a Point | Process                                                            |   412 |
| 9.1                                       | Higher Order Moment Measures                                       |   412 |
| 9.2                                       | Palm Measures                                                      |   414 |
| 10 Stationary Marked Point Processes      | 10 Stationary Marked Point Processes                               |   417 |
| 10.1                                      | Marked Point Processes                                             |   417 |
| 10.2                                      | Palm-Matthes Distribution of a Marked Point Process                |   418 |
| 11                                        | Fairness and Optimality                                            |   422 |
| 12 Lemmas on Fourier Transforms           | 12 Lemmas on Fourier Transforms                                    |   424 |
| 12.1                                      | Fourier Transforms                                                 |   424 |
| 12.2                                      | Lemmas                                                             |   424 |
| 13                                        | Graph Theoretic Notions                                            |   429 |
| 13.1                                      | Minimum Spanning Tree                                              |   429 |


<!-- p:4 -->


14 Discrete Percolation 433

- 14.1 Bond Percolation on Zd. 433
- 14.2 Independent Site Percolation 437

References 439

Table of Mathematical Notation and Abbreviations 442

Index 445


<!-- p:5 -->


Foundations and Trends® in Networking Vol. 3, Nos. 3-4 (2009) 249–449 © 2009 F. Baccelli and B. Błaszczyszyn DOI: 10.1561/1300000006

mou

the essence of knowledge

### Stochastic Geometry and Wireless Networks: Volume I Theory

### François Baccelli1 and Bartłomiej Błaszczyszyn2

- INRIA &amp; Ecole Normale Supérieure, 45 rue d'Ulm, Paris, francois.baccelli@ens.fr
- 2 INRIA &amp; Ecole Normale Superieure and Math. Inst. University of Wroctaw, 45 rue d'Ulm, Paris, bartek.blaszczyszyn@ens.fr

### Abstract

Volume I first provides a compact survey on classical stochastic geometry models, with a main focus on spatial shot-noise processes, coverage processes and random tessellations. It then focuses on signal to interference noise ratio (SINR) stochastic geometry, which is the basis for the modeling of wireless network protocols and architectures considered in Volume II. It also contains an appendix on mathematical tools used throughout Stochastic Geometry and Wireless Networks, Volumes I and II.


<!-- p:6 -->


### Preface

A wireless communication network can be viewed as a collection of nodes, located in some domain, which can in turn be transmitters or receivers (depending on the network considered, nodes may be mobile users, base stations in a cellular network, access points of a WiFi mesh, etc.). At a given time, several nodes transmit simultaneously, each toward its own receiver. Each transmitter-receiver pair requires its own wireless link. The signal received from the link transmitter may be jammed by the signals received from the other transmitters. Even in the simplest model where the signal power radiated from a point decays in an isotropic way with Euclidean distance, the geometry of the locations of the nodes plays a key role since it determines the signal to interference and noise ratio (SINR) at each receiver and hence the possibility of establishing simultaneously this collection of links at a given bit rate. The interference seen by a receiver is the sum of the signal powers received from all transmitters, except its own transmitter.

Stochastic geometry provides a natural way of defining and computing macroscopic properties of such networks, by averaging over all potential geometrical patterns for the nodes, in the same way as queuing theory provides response times or congestion, averaged over all potential arrival patterns within a given parametric class.


<!-- p:7 -->


Preface 251

Modeling wireless communication networks in terms of stochastic geometry seems particularly relevant for large scale networks. In the simplest case, it consists in treating such a network as a snapshot of a stationary random model in the whole Euclidean plane or space and analyzing it in a probabilistic way. In particular the locations of the network elements are seen as the realizations of some point processes. When the underlying random model is ergodic, the probabilistic analysis also provides a way of estimating spatial averages which often capture the key dependencies of the network performance characteristics (connectivity, stability, capacity, etc.) as functions of a relatively small number of parameters. Typically, these are the densities of the underlying point processes and the parameters of the protocols involved. By spatial average, we mean an empirical average made over a large collection of 'locations' in the domain considered; depending on the cases, these locations will simply be certain points of the domain, or nodes located in the domain, or even nodes on a certain route defined on this domain. These various kinds of spatial averages are defined in precise terms in the monograph. This is a very natural approach e.g. for ad hoc networks, or more generally to describe user positions, when these are best described by random processes. But it can also be applied to represent both irregular and regular network architectures as observed in cellular wireless networks. In all these cases, such a space average is performed on a large collection of nodes of the network executing some common protocol and considered at some common time when one takes a snapshot of the network. Simple examples of such averages are the fraction of nodes which transmit, the fraction of space which is covered or connected, the fraction of nodes which transmit their packet successfully, and the average geographic progress obtained by a node forwarding a packet towards some destination. This is rather new to classical performance evaluation, compared to time averages. Stochastic geometry, which we use as a tool for the evaluation of

such spatial averages, is a rich branch of applied probability particularly adapted to the study of random phenomena on the plane or in higher dimension. It is intrinsically related to the theory of point processes. Initially its development was stimulated by applications to biology, astronomy and material sciences. Nowadays, it is also used in image analysis and in the context of communication networks. In this latter case, its role is similar to that played by the theory of point processes on the real line in classical queuing theory.


<!-- p:8 -->


The use of stochastic geometry for modeling communication networks is relatively new. The first papers appeared in the engineering literature shortly before 2000. One can consider Gilbert's paper of 1961 [19] both as the first paper on continuum and Boolean percolation and as the first paper on the analysis of the connectivity of large wireless networks by means of stochastic geometry. Similar observations can be made on [20] concerning Poisson-Voronoi tessellations. The number of papers using some form of stochastic geometry is increasing fast. One of the most important observed trends is to take better account in these models of specific mechanisms of wireless communications.

Time averages have been classical objects of performance evaluation since the work of Erlang (1917). Typical examples include the random delay to transmit a packet from a given node, the number of time steps required for a packet to be transported from source to destination on some multihop route, the frequency with which a transmission is not granted access due to some capacity limitations, etc. A classical reference on the matter is [28]. These time averages will be studied here either on their own or in conjunction with space averages. The combination of the two types of averages unveils interesting new phenomena and leads to challenging mathematical questions. As we shall see, the order in which the time and the space averages are performed matters and each order has a different physical meaning.

This monograph surveys recent results of this approach and is structured in two volumes.

Volume I focuses on the theory of spatial averages and contains three parts. Part I in Volume I provides a compact survey on classical stochastic geometry models. Part II in Volume I focuses on SINR stochastic geometry. Part III in Volume I is an appendix which contains mathematical tools used throughout the monograph. Volume II bears on more practical wireless network modeling and performance analysis. It is in this volume that the interplay between wireless communications and stochastic geometry is deepest and that the time-space framework alluded to above is the most important. The aim is to show how stochastic geometry can be used in a more or less systematic way to analyze the phenomena that arise in this context. Part IV in Volume II is focused on medium access control (MAC). We study MAC protocols used in ad hoc networks and in cellular networks. Part V in Volume II discusses the use of stochastic geometry for the quantitative analysis of routing algorithms in MANETs. Part VI in Volume II gives a concise summary of wireless communication principles and of the network architectures considered in the monograph. This part is self-contained and readers not familiar with wireless networking might either read it before reading the monograph itself, or refer to it when needed.


<!-- p:9 -->


Here are some comments on what the reader will obtain from studying the material contained in this monograph and on possible ways of reading it.

For readers with a background in applied probability, this monograph provides direct access to an emerging and fast growing branch of spatial stochastic modeling (see, e.g., the proceedings of conferences such as IEEE Infocom, ACM Sigmetrics, ACM Mobicom, etc. or the special issue [22]). By mastering the basic principles of wireless links and the organization of communications in a wireless network, as summarized in Volume II and already alluded to in Volume I, these readers will be granted access to a rich field of new questions with high practical interest. SINR stochastic geometry opens new and interesting mathematical questions. The two categories of objects studied in Volume II, namely medium access and routing protocols, have a large number of variants and implications. Each of these could give birth to a new stochastic model to be understood and analyzed. Even for classical models of stochastic geometry, the new questions stemming from wireless networking often provide an original viewpoint. A typical example is that of route averages associated with a Poisson point process as discussed in Part V in Volume II. Reader already knowledgeable in basic stochastic geometry might skip Part I in Volume I and follow the path:

Part II in Volume I ⇒ Part IV in Volume II ⇒ Part V in Volume II, using Part VI in Volume II for understanding the physical meaning of the examples pertaining to wireless networks.


<!-- p:10 -->


For readers whose main interest in wireless network design, the monograph aims to offer a new and comprehensive methodology for the performance evaluation of large scale wireless networks. This methodology consists in the computation of both time and space averages within a unified setting. This inherently addresses the scalability issue in that it poses the problems in an infinite domain/population case from the very beginning. We show that this methodology has the potential to provide both qualitative and quantitative results as below:

- Some of the most important qualitative results pertaining to these infinite population models are in terms of phase transitions. A typical example bears on the conditions under which the network is spatially connected. Another type of phase transition bears on the conditions under which the network delivers packets in a finite mean time for a given medium access and a given routing protocol. As we shall see, these phase transitions allow one to understand how to tune the protocol parameters to ensure that the network is in the desirable "phase" (i.e. well connected and with small mean delays). Other qualitative results are in terms of scaling laws: for instance, how do the overhead or the end-to-end delay on a route scale with the distance between the source and the destination, or with the density of nodes?
- Quantitative results are often in terms of closed form expressions for both time and space averages, and this for each variant of the involved protocols. The reader will hence be in a position to discuss and compare various protocols and more generally various wireless network organizations. Here are typical questions addressed and answered in Volume II: is it better to improve on Aloha by using a collision avoidance scheme of the CSMA type or by using a channel-aware extension of Aloha? Is Rayleigh fading beneficial or detrimental when using a given MAC scheme? How does geographic routing compare to shortest path routing in a mobile


<!-- p:11 -->


ad hoc network? Is it better to separate the medium access and the routing decisions or to perform some cross layer joint optimization? The reader with a wireless communication background could either read the monograph from beginning to end, or start with Volume II, i.e. follow the path Part IV in Volume II ⇒ Part V in Volume II ⇒ Part II in Volume I and use Volume I when needed to find the mathematical results which are needed to progress through Volume II. We conclude with some comments on what the reader will not find

in this monograph:

- We do not discuss statistical questions and give no measurement based validation of certain stochastic assumptions used in the monograph, e.g., when are Poisson-based models justified? When should one rather use point processes with some repulsion or attraction? When is the stationarity/ergodicity assumption valid? Our only aim is to show what can be done with stochastic geometry when assumptions of this kind can be made.
- We will not go beyond SINR models either. It is well known that considering interference as noise is not the only possible option in a wireless network. Other options (collaborative schemes, successive cancellation techniques) can offer better rates, though at the expense of more algorithmic overhead and the exchange of more information between nodes. We believe that the methodology discussed in this monograph has the potential of analyzing such techniques but we decided not to do this here.

Here are some final technical remarks. Some sections, marked with G  t   S    eds   s  t used in what follows; the index, which is common to the two volumes, is designed to be the main tool to navigate within and between the two volumes.


<!-- p:12 -->


##### Acknowledgments

The authors would like to express their gratitude to Dietrich Stoyan, who first suggested them to write a monograph on this topic, as well as to Daryl Daley and Martin Haenggi for their very valuable proof-reading of the manuscript. They would also like to thank the anonymous reviewer of NOW for his/her suggestions, particularly so concerning the two volume format, as well as Paola Bermolen, Pierre Brémaud, Srikant Iyer, Mohamed Karray, Omid Mirsadeghi, Paul Muhlethaler, Barbara Staehle and Patrick Thiran for their useful comments on the manuscript.


<!-- p:13 -->


### Preface to Volume I

This volume focuses on the theory and contains three parts.

Part I provides a compact survey on classical stochastic geometry models. The basic models defined in this part will be used and extended throughout the whole monograph, and in particular to SINR based models. Note, however, that these classical stochastic models can be used in a variety of contexts which go far beyond the modeling of wireless networks. Chapter 1 reviews the definition and basic properties of Poisson point processes in Euclidean space. We review key operations on Poisson point processes (thinning, superposition, displacement) as well as key formulas like Campbell's formula. Chapter 2 is focused on properties of the spatial shot-noise process: its continuity properties, Laplace transform, moments, etc. Both additive and max shot-noise processes are studied. Chapter 3 bears on coverage processes, and in particular on the Boolean model. Its basic coverage characteristics are reviewed. We also give a brief account of its percolation properties. Chapter 4 studies random tessellations; the main focus is on PoissonVoronoi tessellations and cells. We also discuss various random objects associated with bivariate point processes such as the set of points of the first point process that fall in a Voronoi cell w.r.t. the second point process.


<!-- p:14 -->


Part II focuses on the stochastic geometry of SINR. The key new stochastic geometry model can be described as follows: consider a marked point process of the Euclidean space, where the mark of a point is a positive random variable that represents its "transmission power". The SINR cell of a point is then defined as the region of the space where the reception power from this point is larger than an affine function of the interference power. Chapter 5 analyzes a few basic stochastic geometry questions pertaining to such SINR cells in the case with independent marks, such as the volume and the shape of the typical cell. Chapter 6 focuses on the complex interactions that exist between cells. Chapter 7 studies the coverage process created by the collection of SINR cells. Chapter 8 studies the impact of interferences on the connectivity of large-scale mobile ad hoc networks using percolation theory on the SINR graph.

Part III is an appendix which contains mathematical tools used throughout the monograph.

It was our choice not to cover Gibbs point processes and the random closed sets that one can associate to them. And this in spite of the fact r   t s ea s   ein this wireless network context (see the bibliography of Chapter 18 in Volume II for instance). There are two main reasons for this decision: first, these models are rarely amenable to closed form analysis, at least in the case of systems with randomly located nodes as those considered here; second and more importantly, the amount of additional material needed to cover this part of the theory is not compatible with the format retained here.


<!-- p:15 -->


Part I

Classical Stochastic Geometry The most basic objects studied in classical stochastic geometry are multidimensional point processes, which are covered in Chapter 1, with a special emphasis on the most prominent one, the Poisson point process. Our default observation space in this part will be the Euclidean space Rd of dimension d ≥ 1. Even if for most of the applications studied later, the plane R2 (2D) suffices, it is convenient to formulate some results in 3D or 4D (e. g., to consider time and space).


<!-- p:16 -->


Shot noise fields, which are used quite naturally to represent interference fields, are studied in Chapter 2. Chapter 3 is focused on coverage processes, with the particularly important special case of the Boolean model. Chapter 4 bears on Voronoi tessellations and Delaunay graphs, which are useful in a variety of contexts in wireless network modeling. These basic tools will be needed for analyzing the SINR models stemming from wireless communications to be analyzed from Part II on. They will be instrumental for analyzing spatio-temporal models when combined with Markov process techniques.


<!-- p:17 -->


1

### Poisson Point Process

Consider the d-dimensional Euclidean space Rd. A spatial point process (p.p.)Φ is a random, finite or countably-infinite collection of points in the space Rd, without accumulation points.

One can consider any given realization φ of a point process as a discrete subset φ = {xi} ⊂ Rd of the space. It is often more convenient to think of φ as a counting measure or a point measure φ = Σiεxi where εx is the Dirac measure at x; for A ⊂ Rd, εx(A) = 1 if x ∈ A and εx(A) = 0 if x ∉ A. Consequently, φ(A) gives the number of "points" of φ in A. Also, for all real functions f defined on Rd, we have Σi f (xi) = ∫Rd f(x) φ(dx). We will denote by M the set of all point measures that do not have accumulation points in Rd. This means that any φ ∈ M is locally finite, that is φ(A) &lt; ∞ for any bounded A ⊂ Rd (a set is bounded if it is contained in a ball with finite radius).

Note that a p.p. Φ can be seen as a stochastic process Φ = {Φ(A)}A∈z with state space N = {0, 1, . . .} ∃ Φ(A) and where the index A runs over bounded Borel subsets of Rd. Moreover, as for "usual" stochastic processes, the distribution of a p.p. is entirely characterized by the family of finite dimensional distributions (Φ(A1),...,Φ(Ak)), where A1, . . . , Ak run over the bounded subsets of Rd.1


<!-- p:18 -->


## 1.1 Definition and Characterizations

### 1.1.1 Definition

Let Λ be a locally finite non-null measure on Rd.

Definition 1.1. The Poisson point process Φ of intensity measure Λ is defined by means of its finite-dimensional distributions:

$$P \{ \Phi ( A _ { 1 } ) = n _ { 1 } , \dots , \Phi ( A _ { k } ) = n _ { k } \} = \prod _ { i = 1 } ^ { k } \left ( e ^ { - \Lambda ( A _ { i } ) } \frac { \Lambda ( A _ { i } ) ^ { n _ { i } } } { n _ { i } ! } \right ) ,$$

for every k = 1,2,... and all bounded, mutually disjoint sets Ai for i = 1, . . . , k. If Λ(dx) = λ dx is a multiple of Lebesgue measure (volume) in Rd, we call Φ a homogeneous Poisson p.p. and λ is its intensity parameter.

It is not evident that such a point process exists. Later, we will show how it can be constructed. Suppose for the moment that it does exist. Here are a few immediate observations made directly from the above definition:

- Φ is a Poisson p.p., if and only if for every k = 1,2, . .. and all bounded, mutually disjoint Ai ⊂ Rd for i = 1, . . . , k, (Φ(A1), . . . , Φ(Ak)) is a vector of independent Poisson random variables of parameter Λ(Ai), . . . , Λ(Ak), respectively. In particular, E(Φ(A)) = Λ(A), for all A.
- Let W be some bounded observation window and let A1, . . . , Ak be some partition of this window: Ai ∩ Aj = Ø for

1 We do not discuss here the measure-theoretic foundations of p.p. theory; we remark that each time we talk about a subset B of Rd or a function f defined on Rd, we understand that they belong to some "nice class of subsets that can be measured" and to some "nice class of functions that can be integrated". A similar convention is assumed for subsets of M and functions defined on this space (typically, we want all events of the type {μ ∈ M: μ(A) = k}, A ⊂ Rd, k ∈ N, to be "measurable"). See [9] or [10], [11] for details.


<!-- p:19 -->


$$j \neq i \, \text {and} \, \bigcup _ { i } A _ { i } & = W . \text { For all } n , n _ { 1 } , \dots , n _ { k } \in \mathbb { N } \text { with } \sum _ { i } n _ { i } = n , \\ & \quad P \{ \Phi ( A _ { 1 } ) = n _ { 1 } , \dots , \Phi ( A _ { k } ) = n _ { k } \, | \, \Phi ( W ) = n \} \\ & = \frac { n ! } { n _ { 1 } ! \dots n _ { k } ! } \frac { 1 } { \Lambda ( W ) ^ { n } } \prod _ { i } \Lambda ( A _ { i } ) ^ { n _ { i } } . \\ \intertext { T h e a r o g d i t i o n }$$

The above conditional distribution is the multinomial distribution. This last property shows that given there are n points in the window W, these points are independently and identically distributed (i.i.d.) in W according to the law ()v/(·)v

Example 1.1 (Locations of nodes in ad hoc networks). Assume that nodes (users), who are supposed to constitute an ad hoc network (see Section 25.3.1 in Volume II), arrive at some given region W (a -sud  d   ues    dd   tdca tions in W at random according to some probability distribution a(·). This means that each user chooses location dx with probability a(dx); the uniform distribution corresponds to a "homogeneous" situation and non-uniform distributions allow us to model, e.g., various "hot spots". Then, in view of what was said above, the configuration of n users of this ad hoc network coincides in law with the conditional distribution of the Poisson p.p. Φ with intensity Λ(dx) proportional to a(dx) on W, given Φ(W) = n.

Suppose now that one does not want to fix a priori the exact numnxy r e,         odde of nodes per dx is known. In such a situation it is natural to assume that the locations of nodes in W are modeled by the atoms of the (non-conditioned) Poisson process with intensity Λ(dx) = A(dx).2

The observation about conditional distribution suggests a first construction of the Poisson p.p. in a bounded window; sample a Poisson random variable of parameter Λ(W) and if the outcome is n, sample n i.i.d. random variables with distribution Λ(·)/Λ(W) on W. The extension of the construction to the whole space Rd can then be done by considering a countable partition of Rd into bounded windows and an independent generation of the Poisson p.p. in each window. We will return to this idea in Section 1.2. Before this, we give more terminology and other characterizations of the Poisson p.p.

2 One can make the story of nodes arriving to W more complete. Assuming a spatio-temporal Poisson arrival process of nodes, independent Markovian mobility of each node and independent exponential sojourn time of each node in the network before its departure one obtains a spatial birth-and-death process with migrations, who has Poisson p.p. as its stationary (in time) distribution; see [41, Section 9]


<!-- p:20 -->


### 1.1.2 Characterizations by the Form of the Distribution

- Say that Φ has a fixed atom at x0 if P{Φ({x0}) &gt; 0} &gt; 0.
- Call a p.p. Φ simple if P{Φ({x}) = 0 or 1 for all x } = 1; i.e., if with probability 1, Φ = Σiεxi, where the points {xi} are pairwise different.

Proposition 1.1. Let Φ be a Poisson p.p. with intensity measure Λ.

- Φ has a fixed atom at {x0} if and only if Λ has an atom at x0 ∈ Rd (i.e. Λ({x0}) &gt; 0).
- A Poisson p.p. Φ is simple if Λ is non-atomic, i.e. admits a density with respect to Lebesgue measure in Rd.

Proof. The first part is easy: use Definition 1.1 to write P{Φ({xo}) &gt; 0} = 1 − e−Λ({x0}) &gt; 0 if and only if Λ({x0 }) &gt; 0.

The second part can be proved using the conditioning (1.1) along the following lines. Let us take a bounded subset A ⊂ Rd.

P{Φ is simple in A}

$$P \{ \Phi \text { is simple in } A \} \\ = & \sum _ { n = 2 } ^ { \infty } P \{ \Phi ( A ) = n \} P \{ \text {all $n$ points of $\Phi$ are different $| \Phi(A) = n$} \} \\ = & \sum _ { n = 2 } ^ { \infty } e ^ { - \Lambda ( A ) } \frac { ( \Lambda ( A ) ) ^ { n } } { n ! } \frac { 1 } { ( \Lambda ( A ) ) ^ { n } } \\ & \times \int _ { A } \dots \int _ { A } \mathbb { I } ( x _ { j } \text { all different} ) \Lambda ( d x _ { 1 } ) \cdots \Lambda ( d x _ { n } ) = 1 .$$


<!-- p:21 -->


We conclude the proof that P{Φ is simple } = 1 by considering an increasing sequence of bounded sets Ak  Rd and using the monotone convergence theorem. □

We now give two characterizations of the Poisson p.p. based on the form of the distribution of the variable Φ(A) for all A.

Theorem 1.2. Φ is a Poisson p.p. if and only if there exists a locally finite measure Λ on Rd such that for all bounded A, Φ(A) is a Poisson random variable (r. v. ) with parameter Λ(A).

Proof. We use the following fact that can be proved using moment generating functions (cf. Daley and Vere-Jones, [9], Lemma 2.3.I): suppose (X, X1, . . . , Xn) is a random vector with Poisson marginal distributions and such that X = Σi=1 Xi; then X1, . .., Xn are mutually independent. □

Theorem 1.3. Suppose that Φ is a simple p.p. Then Φ is a Poisson p.p. if and only if there exists a locally finite non-atomic measure Λ such that for any subset A, P{Φ(A) = 0 } = e−Λ(A).

Proof. This is a consequence of a more general result saying that the distribution of the p.p. is completely defined by its void probabilities; see ([27], Th. 3.3) for more details. □

### 1.1.3 Characterization by Complete Independence

Definition 1.2. One says that the p.p. Φ has the property of complete independence if for any finite family of bounded subsets A1, . . . , Ak that are mutually disjoint, the random variables Φ(A1), . . . , Φ(Ak) are independent.


<!-- p:22 -->


Theorem 1.4. Suppose that Φ is a p.p. without fixed atoms. Then Φ is a Poisson p.p. if and only if

- (1) Φ is simple, and
- (2) Φ has the property of complete independence.

Proof. The necessity follows from Proposition 1.1. For sufficiency, one shows that the measure Λ(A) = −log(P{Φ(A) = 0}) satisfies the assumptions of Theorem 1.3. (cf. [27], Section 2.1). □

## 1.2 Laplace Functional

Definition 1.3. The Laplace functional L of a p.p. Φ is defined by the following formula

$$\mathcal { L } _ { \Phi } ( f ) = E \left [ e ^ { - \int _ { \mathbb { R } ^ { d } } f ( x ) \, \Phi ( d x ) } \right ] ,$$

where f runs over the set of all non-negative functions on Rd.

Note that the Laplace functional completely characterizes the distribution of the p.p. Indeed, for f (x) = Σi=1 ti1(x ∈ Ai),

$$\mathcal { L } _ { \Phi } ( f ) = E \left [ e ^ { - \sum _ { i } t _ { i } \Phi ( A _ { i } ) } \right ] ,$$

seen as a function of the vector (t1, . . . , tk), is the joint Laplace transform of the random vector (Φ(A1), . . . , Φ(Ak)), whose distribution is characterized by this transform. When A1, . . . , Ak run over all bounded subsets of the space, one obtains a characterization of all finite-dimensional distributions of the p.p.

Here is a very useful characterization of the Poisson p.p. by its Laplace functional.

Proposition 1.5. The Laplace functional of the Poisson p.p. of intensity measure Λ is

$$\mathcal { L } _ { \Phi } ( f ) = e ^ { - \int _ { \mathbb { R } ^ { d } } ( 1 - e ^ { - f ( x ) } ) \Lambda ( d x ) } .$$


<!-- p:23 -->


Proof. For a given non-negative function f(x), consider the function g(x) = f(x)1(x ∈ A), where A ∈ B is bounded. We have

$$( x ) & = f ( x ) \mathbf 1 ( x \in A ) , \text { where } A \in \mathcal { B } \text { is bounded. We have} \\ & \quad \mathcal { L } _ { \Phi } ( g ) = e ^ { - \Lambda ( A ) } \sum _ { n = 0 } ^ { \infty } \frac { ( \Lambda ( A ) ) ^ { n } } { n ! } \frac { 1 } { ( \Lambda ( A ) ) ^ { n } } \\ & \quad \times \int _ { A } \cdots \int _ { A } e ^ { - \sum _ { i = 1 } ^ { n } f ( x _ { i } ) } \, \Lambda ( d x _ { 1 } ) \cdots \Lambda ( d x _ { n } ) \\ & = e ^ { - \Lambda ( A ) } \sum _ { n = 0 } ^ { \infty } \frac { 1 } { n ! } \left ( \int _ { A } e ^ { - f ( x ) } \, \Lambda ( d x ) \right ) ^ { n } \\ & = e ^ { - \int _ { \mathbb { R } ^ { d } } ( 1 - e ^ { - g ( x ) } ) \, \Lambda ( d x ) } . \\$$

We conclude the proof by considering an increasing sequence of bounded sets Ak Rd and using the monotone convergence theorem. □

Taking f(x) = sg(x) with s ≥ 0 and with g(·) ≥ 0 in (1.2) and differentiating w.r.t. s at s = 0, we get the following corollary:

$$E \int _ { \mathbb { R } ^ { d } } f ( x ) \Phi ( d x ) = \int _ { \mathbb { R } ^ { d } } f ( x ) \Lambda ( d x ) .$$

Construction of the Poisson p.p. in a Bounded Window. Given an intensity measure Λ and a bounded subset W of the space, consider the following independent random objects {N, X1, X2,...}, where

- N is a Poisson r. v. with parameter Λ(W),
- X1, X2, . . . are identically distributed random vectors (points) taking values in W ⊂ Rd with P{ X1 ∈ · } = Λ(·)/Λ(W).

In connection with the remark at the end of Section 1.1.1, we show with intensity measure Λ|w(·) = Λ(· ∩ W), the restriction of Λ to W. Evidently Φ is a random set of points in W. We now calculate the Laplace functional of Φ. For a non-negative function f, we have


<!-- p:24 -->


$$\text {Laplace functional of } \Phi . \text { For a non-negative function } f , \text { we have} \\ \mathcal { L } _ { \Phi } ( f ) & = E \left [ 1 ( N = 0 ) + 1 ( N > 0 ) e ^ { - \sum _ { k = 1 } ^ { N } f ( X _ { i } ) } \right ] \\ & = e ^ { - \Lambda ( W ) } \sum _ { k = 0 } ^ { \infty } \frac { ( \Lambda ( W ) ) ^ { k } } { k ! } \left ( \int _ { W } e ^ { - f ( x ) } \, \frac { \Lambda ( d x ) } { \Lambda ( W ) } \right ) ^ { k } \\ & = e ^ { - \Lambda ( W ) + \int _ { W } e ^ { - f ( x ) } \, \Lambda ( d x ) } \\ & = e ^ { - \int _ { W } ( 1 - e ^ { - f ( x ) } ) \Lambda ( d x ) } ,$$

which shows that Φ is the announced Poisson p.p. The above construction can be extended to the whole space. We will do it in the next section.

In the following example, we show that Definition 1.1 for d = 1, i.e. of a Poisson p.p. in 1D, is equivalent to frequently used definition based on independent, exponentially distributed inter-point distances.

Example 1.2 (Homogeneous Poisson p.p. in 1D). Consider a Poisson p.p. Φ = Σk εSk on the real line R with intensity measure λdx, where 0 &lt; λ &lt; ∞. Assume that the atoms of Φ are numbered in such a way that Sk−1 &lt; Sk for k ∈ Z (by Proposition 1.1 the atoms of Φ are pairwise different) and S1 = max{x &gt; 0: Φ((0, x)) = 0} is the first atom of Φ in the open positive half-line (0,∞). We will show that {Sk} can be constructed as a renewal process with exponential holding times, i.e., Sk = Σk=1 Fi for k ≥ 1 and Sk = − Σi=k Fi for k ≤ 0, where {Fk : k = ... , −1,0,1...} is a sequence of independent, identically distributed exponential random variables. Indeed, P{F1 &gt; t} = px [eəodxə s  = IS os qχ−∂ = {0 = ([70))Φ}d = {7 &lt; IS}d variable with parameter λ. By the the strong Markov property (Proposition 1.16), for all k ≥ 2,

$$P \{ F _ { k } > t \, | \, F _ { 1 } , \dots , F _ { k - 1 } \} & = P \{ S _ { k } - S _ { k - 1 } > t \, | \, S _ { 1 } , \dots , S _ { k - 1 } \} \\ & = P \{ S _ { k } - S _ { k - 1 } > t \, | \, S _ { k - 1 } \} \\ & = P \{ \Phi ( ( S _ { k - 1 } , S _ { k - 1 } + t ) ) = 0 \, | \, S _ { k - 1 } \} \\ & = e ^ { - \lambda t }$$

and similarly for k ≤ 0, with {Fk }k≤0 and {Fk }k≥1 being independent.


<!-- p:25 -->


Remark. In the last example, we have evaluated the probabilities of the events of the form {S1 &gt; t}, {Sk − Sk−1 &gt; t}. This was done under the tacit assumption that in the representation Φ = ΣkεSk, the variables {Sk} are random variables, i.e., that the corresponding events belong to the "nice class" of events whose probabilities can be measured. This is true in this particular case and, more generally, points of any p.p. Φ can always be numbered in such a way that the location of the point with a given number is a random variable (see Kallenberg, [27]). In what follows, we assume that {xk} are random variables any time we use a representation of the form Φ = Σk εxk·

## 1.3 Operations Preserving the Poisson Law

### 1.3.1 Superposition

Definition 1.4. The superposition of point processes Φk is defined as the sum Φ = ∑k Φk.

Note that the summation in the above definition is understood as the mn   n a n n (nn  oes which however, in general, might not be locally finite (we do not assume the last sum to have finitely many terms). Here is a very crude, but useful condition for this to not happen.

Lemma 1.6. The superposition Φ = Σk Φk is a p.p. if Σk E[Φk(·)] is a locally finite measure.

A refined sufficient condition may be found by the Borel-Cantelli lemma.

Proposition 1.7. The superposition of independent Poisson point processes with intensities Λk is a Poisson p.p. with intensity measure Σk Λk if and only if the latter is a locally finite measure.

Proof. ⇒ By the definition.

← By Lemma 1.6 the superposition is a p.p. One evaluates its Laplace functional as follows


<!-- p:26 -->


$$\text {functional as follows} \\ E [ e ^ { - \sum _ { k } \int _ { \mathbb { R } ^ { d } } f ( x ) \, \Phi _ { k } ( d x ) } ] & = E \left [ \prod _ { k } e ^ { - \int _ { \mathbb { R } ^ { d } } f ( x ) \, \Phi _ { k } ( d x ) } \right ] \\ & = \prod _ { k } e ^ { - \int _ { \mathbb { R } ^ { d } } ( 1 - e ^ { - f ( x ) } ) \, \Lambda _ { k } ( d x ) } \\ & = e ^ { - \int _ { \mathbb { R } ^ { d } } ( 1 - e ^ { - f ( x ) } ) ( \sum _ { k } \Lambda _ { k } ( d x ) ) } . \quad \square$$

Construction of Poisson p.p. on the Whole Space. We return to the construction of the Poisson p.p. with given intensity measure Λ. Let {Wk}k=1,... be a countable partition of the space with Wk bounded for all k. Following the arguments described in Section 1.1.1, we construct in each Wk an independent copy of the Poisson p.p. with intensity measure Λk(·) = Λ(· ∩ Wk). By Proposition 1.7, Φ = Σk Φk is a Poisson p.p. of intensity measure Λ = Σk Λk.

### 1.3.2 Thinning

Consider a function p: Rd → [0, 1] and a p.p. Φ.

Definition 1.5. The thinning of Φ with the retention function p is a p.p. given by

$$\Phi ^ { p } = \sum _ { k } \delta _ { k } \varepsilon _ { x _ { k } } \, ,$$

where the random variables {δk}k are independent given Φ, and P{ δk = 1 | Φ } = 1 − P{δk = 0 | Φ } = p(xk).

Less formally, we can say that a realization of Φp can be constructed from that of Φ by randomly and independently removing some fraction of points; the probability that a given point of Φ located at x is not removed (i.e. is retained in Φp) is equal to p(x).

It is not difficult to verify that the above construction transforms a Poisson p.p. into another Poisson p.p.


<!-- p:27 -->


Proposition 1.8. The thinning of the Poisson p.p. of intensity measure Λ with the retention probability p yields a Poisson p.p. of intensity measure pΛ with (pΛ)(A) = ∫Ap(x) Λ(dx).

Proof. The Laplace functional of Φp at g = f1A with A bounded is

□

$$P r o f . \, \text { The Laplace functional of } \Phi ^ { p } \, \text { at } g & = f 1 _ { A } \text { with } A \text { bounded is} \\ \mathcal { L } _ { \Phi ^ { p } } ( g ) & = e ^ { - \Lambda ( A ) } \sum _ { n = 0 } ^ { \infty } \frac { ( \Lambda ( A ) ) ^ { n } } { n ! } \frac { 1 } { ( \Lambda ( A ) ) ^ { n } } \\ & \times \int _ { A } \dots \int _ { A } \prod \left ( p ( x _ { i } ) e ^ { - f ( x _ { i } ) } + 1 - p ( x _ { i } ) \right ) \Lambda ( d x _ { 1 } ) \dots \Lambda ( d x _ { n } ) \\ & = e ^ { - \Lambda ( A ) } \sum _ { n = 0 } ^ { \infty } \frac { 1 } { n ! } \left ( \int _ { A } \left ( p ( x ) e ^ { - f ( x ) } + 1 - p ( x ) \right ) \Lambda ( d x ) \right ) ^ { n } \\ & = e ^ { - \int _ { \mathbb { R } ^ { d } } ( 1 - e ^ { - g ( x ) } ) p ( x ) \Lambda ( d x ) } .$$

Example 1.3 (Aloha). A typical application is that of some ad hoc network made of nodes distributed according to some Poisson point process and using Aloha as medium access control (see Section 25.1.2 in Volume II). The principle of this protocol is that each node tosses a coin independently of everything else to decide whether it accesses the shared wireless medium or not. The bias of this coin may depend on the local density of nodes. The last result shows that the set of transmitters is a Poisson p.p. The set of nodes which refrain transmitting is also Poisson.

Corollary 1.9. The restriction Φ|w of a Poisson p.p. of intensity measure Λ to some given set W is a Poisson p.p. with intensity measure Λ(· ∩ W) = Λ|w(···).

### 1.3.3 Random Transformation of Points

Consider a probability kernel p(x, B) from Rd to Rd', where d' ≥ 1, i.e. for all x ∈ Rd, p(x, ·) is a probability measure on Rd'.


<!-- p:28 -->


Definition 1.6. The transformation ΦP of a p.p. Φ by a probability kernel p(·, ·) is a point process in Rd' given by

$$\Phi ^ { p } = \sum _ { k } \varepsilon _ { y _ { k } } \, ,$$

where the Rd'-valued random vectors {yk}k are independent given Φ, with P{ yk ∈ B′ |Φ} = p(xk, B′).3

In other words, Φp is obtained by randomly and independently displacing each point of Φ from Rd to some new location in Rd' according to the kernel p. This operation preserves the Poisson p.p. property as stated in the following theorem.

Theorem 1.10 (Displacement Theorem). The transformation of the Poisson p.p. of intensity measure Λ by a probability kernel p is the Poisson p.p. with intensity measure Λ′(A) = ∫Rd p(x, A) Λ(dx), A ⊂ Rd'.

Proof. The Laplace functional of Φp is

$$p _ { r o o f . } \ T h e \ L a p l a c \ f o n t i a l \ o f \ \Phi ^ { p } \ i s \\ \mathcal { L } _ { \Phi ^ { p } } ( f ) = E \exp \left [ - \sum _ { i } f ( Y _ { i } ) \right ] \\ = E \int _ { \mathbb { R } ^ { d ^ { \prime } } } \dots \int _ { \mathbb { R } ^ { d ^ { \prime } } } e ^ { - \sum _ { i } f ( y _ { i } ) } \prod _ { j } p ( X _ { j } , d y _ { j } ) \\ = E \prod _ { j } \int _ { y _ { j } \in \mathbb { R } ^ { d ^ { \prime } } } e ^ { - f ( y _ { j } ) } p ( X _ { j } , d y _ { j } ) \\ = E \exp \left [ \sum _ { j } \log \left ( \int _ { y \in \mathbb { R } ^ { d ^ { \prime } } } e ^ { - f ( y ) } p ( X _ { j } , d y _ { j } ) \\ \right )$$

3 We use the same notation Φp for the p-thinning and the transformation by kernel p. The context indicates what is meant.


<!-- p:29 -->


Evaluating now the Laplace functional of Φ at g with g(x) = − log (Sy∈Rd' e−f(y)p(x,dy)), we get

$$- \log \left ( \int _ { y \in \mathbb { R } ^ { d ^ { \prime } } } e ^ { - f ( y ) } p ( x , d y ) \right ) , & \text { we get } \\ \mathcal { L } _ { \Phi ^ { p } } ( f ) & = \mathcal { L } _ { \Phi } ( g ) = \exp \left [ - \int _ { \mathbb { R } ^ { d } } \left ( 1 - e ^ { \log \int _ { \mathbb { R } ^ { d ^ { \prime } } } e ^ { - f ( y ) } p ( x , d y ) } \right ) \Lambda ( d x ) \right ] \\ & = \exp \left [ - \int _ { \mathbb { R } ^ { d } } \left ( 1 - \int _ { \mathbb { R } ^ { d ^ { \prime } } } e ^ { - f ( y ) } p ( x , d y ) \right ) \Lambda ( d x ) \right ] \\ & = \exp \left [ - \int _ { \mathbb { R } ^ { d ^ { \prime } } } \left ( 1 - e ^ { - f ( y ) } \right ) p ( x , d y ) \Lambda ( d x ) \right ] \\ & = \exp \left [ - \int _ { \mathbb { R } ^ { d ^ { \prime } } } ( 1 - e ^ { - f ( y ) } ) \Lambda ^ { \prime } ( d y ) \right ] . \quad \Box \\ \frac { \ } { \ } \text {Example 1.4 (Random walk and random waypoint mobility).}$$

□

Example 1.4 (Random walk and random waypoint mobility). Consider some Mobile Ad hoc NETwork (MANET) — see Section 25.3.1 in Volume II. Assume the MANET nodes to be initially distributed according to some Poisson p.p. Assume each node then moves according to some discrete time, continuous state space Markov chain with kernel p(x,dy) on Rd. More precisely, at each time slot, each node is displaced from its initial position x ∈ Rd to a new position y ∈ Rd, independently of everything else. The displacement is random and its law depends only on x.

The last result shows that the displaced points still form a Poisson p.p. The joint Laplace functional of Φ = {Xi} (the initial p.p.) and Φ′ = {Yi} (the displaced p.p.) at f, g, where f and g are positive functions, is defined as

$$\mathcal { L } _ { \Phi , \Phi ^ { \prime } } ( f , g ) = \mathbf E ( e ^ { - \sum _ { i } f ( X _ { i } ) - \sum _ { i } g ( Y _ { i } ) } ) .$$

Using arguments similar to those in the last proof, one gets that

$$& = \exp \left [ - \int _ { \mathbb { R } ^ { d } } ( 1 - e ^ { - g ( y ) } ) \Lambda ^ { \prime } ( d y ) \right ] \\ & = \exp \left [ - \int _ { \mathbb { R } ^ { d } } ( 1 - e ^ { - g ( y ) } ) \Lambda ^ { \prime } ( d y ) \right ] \\$$


<!-- p:30 -->


This displacement scheme can of course be iterated further while preserving the Poisson property.

Notice that if the initial Poisson p.p. has an intensity measure which is 0 outside a finite window W, one can use this Markov model to maintain' all displaced points in W by appropriate choices of the displacement laws.

Here are a few particular cases of this general model:

- The random walk model is that where the displacement consists in adding to x an independent random variable D with some fixed law H on Rd \ {0} which does not depend on x.
- The random waypoint model is similar to the latter, but with the displacement equal to 0 with probability π and to a nonnull random vector with a fixed distribution H on Rd \ {0} with probability 1 − π. A node either 'stops' with probability π or moves in some new direction with the complementary probability.
- The high mobility random walk case features a small parameter € &gt; 0 and consists in adding the random variable D/€ to x to get the new position; here, the law of D is as in the first case above. Then

$$\mathcal { L } _ { \Phi , \Phi ^ { \prime } } ( f , g ) & = \mathcal { L } _ { \Phi ^ { \prime } } ( g ) \exp \left [ - \int _ { \mathbb { R } ^ { d } } ( 1 - e ^ { - f ( x ) } ) \\ & \quad \times \left ( \int _ { \mathbb { R } ^ { d } \ \{ 0 \} } e ^ { - g ( x + y / \epsilon ) } H ( d y ) \right ) \Lambda ( d x ) \right ] .$$

Let us show how to use this formula to prove that for homogeneous Poisson p.p., this high mobility case leads to independence between Φ and Φ' when € → 0. For this, it is enough to prove that for all functions g which tend to 0 at infinity in all directions,

$$\lim _ { \epsilon \to \infty } & \int _ { \mathbb { R } ^ { d } } ( 1 - e ^ { - f ( x ) } ) \left ( \int _ { \mathbb { R } ^ { d } \langle \{ 0 \} } e ^ { - g ( x + y / \epsilon ) } H ( d y ) \right ) d x \\ & = \int _ { \mathbb { R } ^ { d } } ( 1 - e ^ { - f ( x ) } ) d x .$$


<!-- p:31 -->


But for all x and all y ≠ 0, g(x + y/€) tends to 0 when € tends to 0. This and the dominated convergence theorem allow one to conclude the proof of independence.

Notice that this independence property does not hold in the high mobility random waypoint model as defined above.

Example 1.5 (Transformation of space). Consider a function G: Rd → Rd'. Note that the mapping G can be seen as a special case of a probability kernel from one space to the other, which transforms x ∈ Rd into G(x) with probability 1. Suppose Φ is a Poisson p.p. with intensity measure Λ on Rd. By Theorem 1.10, Φ' = Σk εG(xk) is a Poisson p.p. on Rd' with intensity measure Λ'(·) = Λ(G−1(·)).

Example 1.6 (Dilation). A special case of a transformation Rd onto itself is a dilation by a given factor γ: G(x) = γx, x ∈ Rd. By the above result Φ′ = Σkεγxk is a Poisson p.p. with intensity measure Λ'(A) = Λ(A/γ), where A/γ = {y/γ: y ∈ A}.

Example 1.7 (Homogenization). Another special case consists in finding some transformation G which makes of Φ′ a homogeneous Poisson p.p. For this, assume that Λ(dx) = λ(x)dx and suppose that G(x) is a differentiable mapping from Rd to Rd, which satisfies the functional equation on Rd given by

$$\lambda ( x ) = \lambda | J _ { G } ( x ) | ,$$

where λ is some constant and JG is the Jacobian of G. Then, note that for all A ⊂ Rd

$$\Lambda ( G ^ { - 1 } ( A ) ) = \int _ { G ^ { - 1 } ( A ) } \lambda ( x ) \, d x = \int _ { G ^ { - 1 } ( A ) } \lambda | J _ { G } ( x ) | \, d x = \int _ { A } \lambda \, d x ,$$

which proves that the intensity measure of Φ′ is Λ'(dx) = λdx; see (Senoussi et al., [40]) for more details. In particular in 1D (d = 1), the function G(t) = ∫t λ(s) ds transforms the inhomogeneous Poisson p.p. on [0, ∞) into the homogeneous one of intensity (parameter) 1 on [0,∞). This construction can easily be extended to R by considering the analogous transformation on the negative half-line.


<!-- p:32 -->


Example 1.8 (Polar coordinates). Consider a homogeneous Poisson p.p. Φ on R2 with constant intensity λ and let G(x): R2 → R+ × [0, 2π) be the mapping G(x) = (|x|, ∠(x)), where ∠(x) is the argument of x) (i. e., the angle between vector x and the X axis). Then the transformation Φ' of Φ by G(x) is a Poisson p.p. with intensity measure

$$\Lambda ^ { \prime } ( [ 0 , r ) , [ 0 , \theta ) ) = \lambda \pi r ^ { 2 } \theta / ( 2 \pi ) , \ \ r \geq 0 , \ 0 \leq \theta < 2 \pi .$$

The point process Φ' can also be seen as Poisson p.p. on [0, ∞) with intensity measure ΛT(dt) = λπt2, independently marked in the space [0,2π), with uniform mark distribution (cf. Section 2.1).

## 1.4 Palm Theory

Palm theory formalizes the notion of the conditional distribution of a general p.p. given it has a point at some location. Note that for a p.p. without a fixed atom at this particular location, the probability of the condition is equal to 0 and the basic discrete definition of the conditional probability does not apply. In this section, we will outline the definition based on the Radon-Nikodym theorem.

We first define two measures associated with a general point process:

Definition 1.7. The mean measure of a p.p. Φ is the measure

$$M ( A ) = E [ \Phi ( A ) ]$$

on Rd. The reduced Campbell measure of Φ is the measure

$$C ^ { ! } ( A \times \Gamma ) = E \left [ \int _ { A } 1 ( \Phi - \varepsilon _ { x } \in \Gamma ) \, \Phi ( d x ) \right ]$$

on Rd × M, where M denotes the set of point measures.


<!-- p:33 -->


Note that M(A) is simply the mean number of points of Φ in A. The reduced Campbell measure C!(A × Γ) is a refinement of this mean measure; it gives the expected number of points of Φ in A such that when removing a particular point from Φ, the resulting configuration satisfies property Γ. The fact that one measure is a refinement of the other, or more formally, that C!(. × Γ) for each Γ is absolutely continuous with respect to M(·), allows us to express the former as an integral of some latter:

$$C ^ { ! } ( A \times \Gamma ) = \int _ { A } P _ { x } ^ { ! } M ( d x ) , \quad \text {for all } A \subset \mathbb { R } ^ { d } .$$

The function Pi = Pd(Γ) depends on Γ. Moreover, if M(·) is a locally finite measure, P'(·) can be chosen as a probability distribution on M for each given x.

Definition 1.8. Given a point process with a locally finite mean measure, the distribution P'(·) is called the reduced Palm distribution of Φ given a point at x.

The following central formula of Palm calculus, which is called the Campbell-Mecke formula, is a mere rewriting of the above definition when f(x, μ) = 1(x ∈ A, μ ∈ Γ). Its extension to general f follows from classical monotone class arguments.

Theorem 1.11 (Reduced Campbell-Little-Mecke Formula). For all non-negative functions defined on Rd × M

$$\mathbf E \left [ \int _ { \mathbb { R } ^ { d } } f ( x , \Phi - \varepsilon _ { x } ) \, \Phi ( d x ) \right ] = \int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { M } } f ( x , \phi ) \, P _ { x } ^ { ! } ( d \phi ) \, M ( d x ) .$$

In what follows, we will call formula (1.9) the (reduced) Campbell formula.


<!-- p:34 -->


One can define the (non-reduced) Campbell measure by replacing 1(Φ ∈ Γ − εx) by 1(Φ ∈ Γ) in (1.8), i.e.,

$$\in \Gamma - \varepsilon _ { x } ) \text { by } 1 ( \Phi \in \Gamma ) \text { in } ( 1 . 8 ) , \text { i.e.,} \\ C ( A \times \Gamma ) = E \left [ \int _ { A } 1 ( \Phi \in \Gamma ) \, \Phi ( d x ) \right ] \\ = E \left [ \sum _ { i } 1 ( x _ { i } \in A ) 1 ( \Phi \in \Gamma ) \right ] \\ = E [ \Phi ( A ) 1 ( \Phi \in \Gamma ) ] . \quad ( 1 . 1 0 ) \\ \text { leads to a } ( \text { non-reduced} ) \, \text { Palm measure } P _ { x } \text { which can also be}$$

This leads to a (non-reduced) Palm measure Px which can also be defined by

$$P _ { x } ( \Gamma ) = P _ { x } ^ { ! } ( \{ \phi \colon \phi + \varepsilon _ { x } \in \Gamma \} ) .$$

We call Px the Palm distribution of Φ.

Taking f(x, φ) = g(x,φ + εx) and substituting in (1.9), we obtain the following (non-reduced) version of Campbell's formula:

$$( 1 . 1 1 )$$

We now focus on Poisson point processes. Directly from Definition 1.1, we have:

Corollary 1.12. The mean measure of a Poisson p.p. is equal to its intensity measure M(·) = Λ(·).

We now state a central result of the Palm theory for Poisson p.p. It makes clear why the reduced Palm distributions are more convenient in many situations.

Theorem 1.13 (Slivnyak-Mecke Theorem). Let Φ be a Poisson p.p. with intensity measure Λ. For Λ almost all x ∈ Rd,

$$P _ { x } ^ { ! } ( \cdot ) = P \{ \Phi \in \cdot \} ;$$

that is, the reduced Palm distribution of the Poisson p.p. is equal to its (original) distribution.

In what follows, we will call the above result Slivnyak's theorem.


<!-- p:35 -->


Proof of Theorem 1.13. The proof is based on a direct verification of the integral formula

$$C ^ { ! } ( A \times \Gamma ) = \int _ { A } P \{ \Phi \in \Gamma \} M ( d x ) = \Lambda ( A ) P \{ \Phi \in \Gamma \} .$$

By Theorem 1.2 it is enough to prove this formula for all Γ of the form {μ: μ(B) = n}. For all such Γ

$$C ^ { ! } ( A \times \Gamma ) = E \left [ \sum _ { X _ { i } \in A } \mathbb { I } \left ( ( \Phi - \varepsilon _ { X _ { i } } ) ( B ) = n \right ) \right ] .$$

If A∩ B = ∅

$$E \left [ \sum _ { X _ { i } \in A } 1 ( \Phi - \varepsilon _ { X _ { i } } ) ( B ) = n \right ] & = E [ \Phi ( A ) 1 ( \Phi ( B ) = n ) ] \\ & = \Lambda ( A ) P \{ \Phi ( B ) = n \} .$$

If A∩B≠∅,

$$E & \left [ \sum _ { X _ { i } \in A } 1 ( \Phi - \varepsilon _ { X _ { i } } ) ( B ) = n ) \right ] \\ & = E [ \Phi ( A \ \ B ) \mathbb { I } ( \Phi ( B ) = n ) ] + E [ \Phi ( B \cap A ) \mathbb { I } ( \Phi ( B ) = n + 1 ) ] \\ & = \Lambda ( A \ \ B ) \mathbb { P } \{ \Phi ( B ) = n \} + E [ \Phi ( A \cap B ) \mathbb { 1 } ( \Phi ( B \ \ A ) \\ & = n - \Phi ( B \cap A ) + 1 ] . \\$$

But

$$B u & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & & &$$


<!-- p:36 -->


Before showing an application of the above theorem, we remark that it is often useful to see Px(·) and Pi(·) as the distributions of some p.p. Φx and Φ called, respectively, the Palm and the reduced Palm version of Φ. One can always take Φx = Φ! + εx, however, for a general po   n oe o er  or s  r Φx, Φx on one probability space, with the same probability measure P. But Slivnyak's theorem implies the following result which is a popular approach to the Palm version of Poisson p.p.s:

Corollary 1.14. For Poisson p.p. Φ one can take Φ! = Φ and Φx = x Φ + εx for all x ∈ Rd.

Using now the convention, according to which a p.p. is a family of random variables Φ = {xi}i, which identify the locations of its atoms (according to some particular order) we can rewrite the reduced Campbell formula for Poisson p.p.

$$E \left [ \sum _ { x _ { i } \in \Phi } f ( x _ { i } , \Phi \ \{ x _ { i } \} ) \right ] = \int _ { \mathbb { R } ^ { d } } E [ f ( x , \Phi ) ] \, M ( d x ) .$$

Here is one of the most typical applications of Slivnyak's theorem.

Example 1.9. (Distance to the nearest neighbor in a Poisson p.p.) For a given x ∈ Rd and φ ∈ M, define the distance R*(x) = R*(x, φ) = minxi∈φ |xi − x| from x to its nearest neighbor in φ ∈ M. Note that the min is well defined due to the fact that φ is locally finite, even if arg minxi∈φ |xi − x| is not unique. Let Φ be a Poisson p.p. with intensity measure Λ and let P1 be its reduced Palm measure given a point at x. By Slivnyak's theorem

$$P _ { x } ^ { ! } ( \{ \phi \colon R ^ { * } ( x , \phi ) > r \} ) = \mathbf P \{ \Phi ( B _ { x } ( r ) ) = 0 \} = e ^ { - \Lambda ( B _ { x } ( r ) ) } ,$$

where Bx(r) is the (closed) ball centered at x and of radius r. Interat x, the above equality means that for a Poisson p.p. Φ conditioned to have a point at x, the law of the distance from this point to its nearest neighbor is the same as that of the distance from the location x to the nearest point of the non-conditioned Poisson p.p. Note that this distance can be equal to 0 with some positive probability if Φ has a fixed atom at x. Note that this property becomes an a.s. tautology = Φ of the reduced Palm version of the Poisson p.p. Φ. Indeed, in this case R*(x, Φx) = R*(x, Φ) trivially. The mean value of R* (x, Φ) is equal to ∫0 e−A(Bx(r)) dr. In the case of Poisson p.p. on R2 with intensity measure λ dx


<!-- p:37 -->


$$E [ R ^ { * } ( x , \Phi ) ] = \frac { 1 } { 2 \sqrt { \lambda } } .$$

A surprising fact is that the property expressed in Slivnyak's theorem characterizes Poisson point processes.

Theorem 1.15. (Mecke's Theorem) Let Φ be a p.p. with a σ-finite mean measure M (i.e., there exists a countable partition of Rd such that M is finite on each element of this partition). Then Φ is the Poisson p.p. with intensity measure Λ = M if and only if

$$P _ { x } ^ { ! } ( \cdot ) = P \{ \, \Phi \in \cdot \} .$$

Proof. ⇒ By Slivnyak's theorem.

⇐ By Theorem 1.2 it suffices to prove that for any bounded B

$$P \{ \Phi ( B ) = n \} = P \{ \Phi ( B ) = 0 \} \frac { ( M ( B ) ) ^ { n } } { n ! } .$$

From the definition of the reduced Palm distribution with Γ = {μ: μ(B) = n },

$$C ^ { ! } ( B \times \{ \mu \colon \mu ( B ) = n \} ) & = \mathbf E \left [ \sum _ { x _ { i } \in \Phi } \mathbb { I } ( x _ { i } \in B ) \mathbb { I } ( \Phi ( B ) = n + 1 ) \right ] \\ & = ( n + 1 ) \mathbf P \{ \Phi ( B ) = n + 1 \} .$$


<!-- p:38 -->


Using now the assumption that Pd(Γ) = P{Φ ∈ Γ, }, for all Γ

$$C ^ { ! } ( B \times \Gamma ) & = \int _ { B } P _ { x } ^ { ! } ( \Gamma ) M ( d x ) \\ & = \int _ { B } P \{ \Phi \in \Gamma \} M ( d x ) \\ & = M ( B ) P \{ \Phi \in \Gamma \} .$$

Hence

$$( n + 1 ) P \{ \Phi ( B ) = n + 1 \} = M ( B ) P \{ \Phi ( B ) = n \} ,$$

from which (1.14) follows.

□

## 1.5 Strong Markov Property

Consider a point process Φ. We call S ⊂ Rd a random compact set (with respect to Φ) when S = S(Φ) is a compact set that is a function of the realization of Φ. We give an example in Example 1.10.

Definition 1.9. A random compact set S(Φ) is called a stopping set if one can say whether the event {S(Φ) ⊂ K } holds or not knowing only the points of Φ in K.

Remark. It can be shown that if S = S(Φ) is a stopping set, then for all φ ∈ M,

$$S ( \Phi ) = S ( \Phi \cap S ( \Phi ) \cup \phi \cap S ^ { c } ( \Phi ) ) ,$$

where Sc is the complement of S. In other words, all modifications of Φ outside the set S(Φ) have no effect on S(Φ).

Here is a very typical example of a stopping set.

Example 1.10 (kth smallest random ball). Consider the random (closed) ball B0(R) centered at the origin, with the random radius equal to the kth smallest norm of xi ∈Φ; i.e., Rk = Rk(Φ) = min{r ≥0: Φ(B0(r)) = k}. In order to prove that B0(Rk) is a stopping set let us perform the following mental experiment. Given a realization of Φ


<!-- p:39 -->


nt t  ( t   r, os s  t t   t origin, increasing its radius r from 0 until the moment when either (1) it accumulates k or more points or (2) it hits the complement Kc of K. If (1) happens, then B0(Rk) ⊂ K. If (2) happens, then B0(Rk)  K. In each of these cases, we have not used any information about points of dt  s dd  t (( = (t os  o Φ

Remark. The above example shows a very useful way to establish the stopping property. If there is a one-parameter sequence of growing compact sets which eventually leads to the construction of a random compact, then this compact is a stopping set.

Suppose now that Φ is a Poisson p.p. By the complete independence (see Definition 1.2) we have

$$E [ f ( \Phi ) ] = E \left [ f ( ( \Phi \cap B ) \cup ( \Phi ^ { \prime } \cap B ^ { c } ) ) \right ] ,$$

where Φ' is an independent copy of Φ.

The following result extends the above result to the case when B is a random stopping set.

Proposition 1.16 (Strong Markov property of Poisson p.p.). Let Φ be a Poisson p.p. and S = S(Φ) a random stopping set relative to Φ. Then (1.15) holds with B replaced by S(Φ).

Proof. The Poisson process is a Markov process. Therefore, it also possesses the strong Markov property; see ([39], Theorem 4). □

Example 1.11 (Ordering the points of a Poisson p.p. according to their norms). Let

$$\{ R _ { k } ^ { * } = R _ { k } ^ { * } ( \Phi ) \} _ { k \geq 1 }$$

be the sequence of norms of the points of the Poisson p.p. Φ arranged in increasing order (i.e. R is the norm of the kth nearest point of Φ to the origin). We assume that the intensity measure Λ of Φ has a density.


<!-- p:40 -->


One can conclude from the strong Markov property of the Poisson p.p. that this sequence is a Markov chain with transition probability

$$P \{ R _ { k } ^ { * } > t \, | \, R _ { k - 1 } ^ { * } = s \} = \begin{cases} e ^ { - \Lambda ( B _ { 0 } ( t ) ) - \Lambda ( B _ { 0 } ( s ) ) } , & \text {if } t > s , \\ 1 , & \text {if } t \leq s . \end{cases}$$

## 1.6 Stationarity and Ergodicity

### 1.6.1 Stationarity

Throughout the section, we will use the following notation: for all v ∈ Rd and Φ = ∑i εxi,

$$v + \Phi = v + \sum _ { i } \varepsilon _ { x _ { i } } = \sum _ { i } \varepsilon _ { v + x _ { i } } .$$

Definition 1.10. A point process Φ is stationary if its distribution is invariant under translation through any vector v ∈ Rd; i.e. P{v + Φ ∈Γ} = P{Φ ∈ Γ} for any v ∈ Rd and Γ.

It is easy to see that

Proposition 1.17. A homogeneous Poisson p.p. (i.e. with intensity measure λ dx for some constant 0 &lt; λ &lt; ∞) is stationary.

Proof. This can be shown, e.g. using the Laplace functional.

□

It is easy to show the following properties of stationary point processes:

Corollary 1.18. Given a stationary point process Φ, its mean measure is a multiple of Lebesgue measure: M(dx) = λ dx.

Obviously λ = E[Φ(B)] for any set B ∈ Rd of Lebesgue measure 1. One defines the Campbell-Matthes measure of the stationary p.p. Φ as the following measure on Rd × M:


<!-- p:41 -->


$$\mathcal { C } ( A \times \Gamma ) & = E \left [ \int _ { A } 1 ( \Phi - x \in \Gamma ) \, \Phi ( d x ) \right ] \\ & = E \left [ \sum _ { i } 1 ( x _ { i } \in A ) 1 ( \Phi - x _ { i } \in \Gamma ) \right ] .$$

Notice that this definition is different from that in (1.7) or in (1.10). In particular, in the last formula Φ — x is the translation of all atoms of Φ by the vector -x (not to be confused with Φ − εx, the subtraction of the atom εx from Φ).

If λ &lt; ∞, by arguments similar to those used in Section 1.4, one can define a probability measure P0 on M, such that

$$\mathcal { C } ( A \times \Gamma ) = \lambda | A | P ^ { 0 } ( \Gamma ) ,$$

for all Γ (see Section 10.2 in the Appendix).

Definition 1.11 (Intensity and Palm distribution of a stationary p.p.). For a stationary point process Φ, we call the constant λ described in Corollary 1.18 the intensity parameter of Φ. The probability measure P0 defined in (1.17) provided λ &lt; ∞ is called the Palm− Matthes distribution of Φ.

Again, one can interpret P0 as conditional probability given Φ has a point at the origin (see Section 10.2).

Below, we always assume 0 &lt; λ &lt; ∞. The following formula, which will often be used in what follows, can be deduced immediately from (1.17):

Corollary 1.19 (Campbell-Matthes formula for a stationary p.p.). For a stationary point process Φ with finite, non-null intensity λ, for all positive functions g

$$E \left [ \int _ { \mathbb { R } ^ { d } } g ( x , \Phi - x ) \, \Phi ( d x ) \right ] = \lambda \int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { M } } g ( x , \phi ) P ^ { 0 } ( d \phi ) \, d x \, .$$


<!-- p:42 -->


Remark 1.1 (Typical point of a stationary p.p.). It should not be surprising that in the case of a stationary p.p. we actually define only one conditional distribution given a point at the origin 0. One may guess that due to the stationarity of the original distribution of the p.p. conditional distribution given a point at another location x should be somehow related to P0. Indeed, using formulae (1.18) and (1.11) one can prove a simple relation between Px (as defined in Section 1.4 for a general p.p.) and P0. More specifically, taking g(x, φ) = 1(φ + x ∈ Γ) we obtain

$$\int _ { \mathbb { R } ^ { d } } P _ { x } \{ \phi \colon \phi \in \Gamma \} \, { \mathrm d } x = \int _ { \mathbb { R } ^ { d } } P ^ { 0 } \{ \phi \colon \phi + x \in \Gamma \} \, { \mathrm d } x \, ,$$

which means that for almost all x ∈ Rd the measure Px is the image of the measure P0 by the mapping φ → φ + x on M (see Section 10.2.3 for more details). This means in simple words, that the conditional distribution of points of Φ "seen" from the origin given Φ has a point there is exactly the same as the conditional distribution ofpoints of Φ "seen" from an arbitrary location x given Φ has a point at x. In this context, P0 (resp. Px) is often called the distribution of Φ seen o  o ,d (x p d)  p l d od,  ide Slivnyak Theorem 1.13 and Corollary 1.14 that for a stationary Poisson p.p. Φ, P0 corresponds to the law of Φ + ε0 under the original distribution.

In what follows we will often consider, besides Φ, other stochastic objects related to Φ.4 Then, one may be interested in the conditional distribution of these objects "seen" from the typical point of Φ.5

4Two typical examples of such situations are:

· random marks attached to each point of Φ and carrying some information (to be introduced in Section 2),

· another point process on the same space (considered, e.g., in Section 4.3).

Another,slightly more complicated example, is the cross-fading model mentioned in Example 2.4 and exploited in many places in Part IV in Volume II of this book (see in particular Section 16.2 in Volume II).

5 For example, the distribution of the mark of this typical point, or points of other point processes located in the vicinity of the typical point of Φ.


<!-- p:43 -->


In these situations, it is more convenient to define the Palm-Matthes (or shortly Palm) probability P0 on the probability space where the p.p. Φ and all other objects are assumed to be defined, rather than on (some extension of) M as above.6 Expectation with respect to P0 will be denoted by E0. We will return to this idea in Sections 2.1.2 and 4.3. Here note only that P0 is the distribution of Φ under P0. Thus the Campbell-Matthes formula (1.18) can be rewritten as

$$E \left [ \int _ { \mathbb { R } ^ { d } } g ( x , \Phi - x ) \, \Phi ( d x ) \right ] = \lambda \int _ { \mathbb { R } ^ { d } } E ^ { 0 } [ g ( x , \Phi ) ] \, d x \, .$$

### 1.6.2 Ergodicity

Consider a stationary p.p. Φ. Let f be some function M → R+. We are interested in spatial averages of the form

$$\lim _ { n \to \infty } \frac { 1 } { | A _ { n } | } \int _ { A _ { n } } f ( v + \Phi ) \, d v , \quad | A _ { n } | \to \infty ,$$

whenever the limit exists. Roughly speaking Φ is ergodic if the last limit exists and is equal to E[f(Φ)] for almost all realizations of Φ, for all integrable functions f and for some "good" sets An, for instance An = B0(n). As we see, ergodicity is a requirement for simulation.

Several other types of averages can be defined like, e.g. directional averages

$$\lim _ { n \to \infty } \frac { 1 } { n } \sum _ { k = 1 } ^ { n } f ( v k + \Phi )$$

where v ∈ Rd, v ≠ 0. Note that the existence of the limit in (1.21) would follow from the strong law of large numbers if f (vk + Φ), k = 1, . . . were independent random variables.

6 For this, one has to assume that this probability space is endowed with an abstract "shift" operator (see Remark 10.1 for the details) that says how the translation of the "observation point" by some vector x ∈ Rd impacts the "observed picture" of all considered objects. In the simple scenarios considered above, this consists in translating, by the vector -x, the points of all the considered point processes while preserving their original marks.


<!-- p:44 -->


Definition 1.12. We say that a stationary p.p. Φ

- is mixing if

$$P \{ v + \Phi \in \Gamma , \Phi \in \Delta \} \to P \{ \Phi \in \Gamma \} P \{ \Phi \in \Delta \} \quad \text {when} \ | v | \to \infty ,$$

for all for configuration sets Γ and ∆ that depend on the realization of the p.p. in some bounded set;

- is ergodic if

$$& \lim _ { t \to \infty } \frac { 1 } { ( 2 t ) ^ { d } } \int _ { [ - t , t ] ^ { d } } 1 ( v + \Phi \in \Gamma , \Phi \in \Delta ) \, d v = P \{ \Phi \in \Gamma \} P \{ \Phi \in \Delta \} , \\ & \text {for all such $\Gamma$, $\Delta$} .$$

By the dominated convergence theorem, we have the following fact:

Corollary 1.20. A mixing point process is ergodic.

Also

Proposition 1.21. A homogeneous Poisson p.p. Φ is mixing and hence ergodic.

Proof. For Γ and ∆ as in Definition 1.12, Γ − v = {−v + φ: φ ∈ Γ} and ∆ depend on the configuration of points in disjoint subsets of Rd. Thus, by the very definition of the Poisson p.p., 1(v + Φ ∈ Γ) = 1(Φ ∈ Γ − v) and 1(Φ ∈ ∆) are independent. □

{o} eods  a sedd od o o i od of convex sets a convex averaging sequence if A1 ⊂ A2 ⊂ ... ⊂ Rd and sup{r: An contains a ball of radius r} → ∞ when n → ∞. One can can prove the following result for general stationary point processes (cf. Daley and Ver-Jones, [9], Section 10.3; Pugh and Shub, [37]).

Proposition 1.22. Suppose that Φ is translation invariant. Then the following statements are equivalent.


<!-- p:45 -->


- (1) Φ is ergodic.
- (2) For any f such that E[f(Φ)] &lt; ∞ and for all vectors v ∈ Rd, possibly off some countable set of hyperplanes in Rd (a hyperplane is not assumed to contain the origin), the limit (1.21) almost surely exists.
- (3) For any f such that E[f(Φ)] &lt; ∞ and any convex averaging sequence {Ai} the limit in (1.20) is equal to E[f(Φ)] almost surely.
- (4) Any function f of Φ that is translation invariant (i.e. such that for all v ∈ Rd, f(v + Φ) = f(Φ) almost surely), is almost surely constant.

In many problems, rather than (1.20), one is interested in another kind of spatial average that will be referred to as spatial point averages in what follows, and which are of the form

$$\lim _ { n \to \infty } \frac { 1 } { \Phi ( A _ { n } ) } \sum _ { x _ { i } \in A _ { n } } f ( \Phi - x _ { i } ) , \ \ | A _ { n } | \to \infty ,$$

whenever the limit exists. The following result can be found in, e.g., Daley and Vere-Jones ([9], cf. Proposition 12.2.VI).

Proposition 1.23. If Φ is translation invariant and ergodic, for all f and for any convex averaging sequence {An}

$$\lim _ { t \to \infty } \frac { 1 } { \Phi ( A _ { n } ) } \sum _ { x _ { i } \in A _ { n } } \, f ( \Phi - x _ { i } ) = \int f ( \phi ) \, P ^ { 0 } ( d \phi ) = E ^ { 0 } [ f ( \Phi ) ] \quad a . s . , \\ \intertext { i n d e v i d e F ^ { 0 } [ f ( \Phi ) ] }$$

provided E0[.f(Φ)] &lt; ∞.

The above ergodic property says that the distribution P0 of the point -i o o  ( on     o es, ors tribution of Φ "seen from its randomly chosen point".

In Part V in Volume II we will also consider route averages associated with certain multihop routing algorithms. A routing algorithm is defined through a map AD: Rd × M → Rd, where AD(X, Φ) ∈ Φ, for X ∈ Φ, is the next hop from X on the route. This next hop depends on the destination node D and also on the rest of the point process Φ.


<!-- p:46 -->


Within this setting, when denoting by An the nth order iterate of AD and by N(O, D) the number of hops from origin O to destination D, route averages are quantities of the type

$$\frac { 1 } { N ( O , D ) } \sum _ { n = 1 } ^ { N ( O , D ) } f ( \mathcal { A } _ { D } ^ { n } ( O , \Phi ) - \mathcal { A } _ { D } ^ { n - 1 } ( O , \Phi ) ) ,$$

where f is some function Rd → R+. One of the key questions within this context is the existence of a limit for the last empirical average when |O − D| → ∞.


<!-- p:47 -->


2

### Marked Point Processes and Shot-Noise Fields

In a marked point process (m.p.p.), a mark belonging to some measurable space and carrying some information is attached to each point.

## 2.1 Marked Point Processes

Consider a d-dimensional Euclidean space Rd, d ≥ 1, as the state space of the point process. Consider a second space Rl, l ≥ 1, called the space of marks. A marked p.p.  (with points in Rd and marks in Rl) is a locally finite, random set of points in Rd, with some random vector in Rl attached to each point.

One can represent a marked point process either as a collection of pairs  = {(xi, mi)}i, where Φ = {xi} is the set of points and {mi} the set of marks, or as a point measure

$$\widetilde { \Phi } = \sum _ { i } \varepsilon _ { ( x _ { i } , m _ { i } ) } ,$$

where ε(x,m) is the Dirac measure on the Cartesian product Rd × Rl with an atom at (x, m). Both representations suggest that Φ is a p.p. in the space Rd × Rl, which is a correct and often useful observation. We denote the space of its realizations (locally finite counting measures on Rd × Rl) by . As a point process in this extended space,  has one important particularity inherited from its construction, namely that Φ(A × Rl) is finite for any bounded set A ⊂ Rd, which is not true for a general p.p. in this space.


<!-- p:48 -->


### 2.1.1 Independent Marking

An important special case of marked p.p. is the independently marked p.p.

Definition 2.1. A marked p.p. is said to be independently marked (i.m.) if, given the locations of the points Φ = {xi}, the marks are mutually independent random vectors in Rl, and if the conditional distribution of the mark m of a point x ∈ Φ depends only on the location of this point x it is attached to; i.e., P{m ∈ · | Φ} = P{m ∈ · | x} = Fx(dm) for some probability kernel or marks F.(·) from Rd to Rl.

An i.m.p.p. can also be seen as a random transformation of points by a particular probability transition kernel (cf. Section 1.3.3). This leads to immediate results in the Poisson case.

Corollary 2.1. An independently marked Poisson p.p.  with intensity measure Λ on Rd and marks with distributions Fx(dm) on Rl is a Poisson p.p. on Rd × Re with intensity measure

$$\widetilde { \Lambda } ( A \times K ) = \int _ { A } \widetilde { p } ( x , K ) \, \Lambda ( d x ) , \ \ A \subset \mathbb { R } ^ { d } , K \subset \mathbb { R } ^ { \ell } ,$$

where p(x, K) = ∫K Fx(dm). Consequently, its Laplace transform is equal to

$$\mathcal { L } _ { \widetilde { \Phi } } ( \widetilde { f } ) = E \left [ \exp \left \{ - \sum _ { i } \widetilde { f } ( x _ { i } , m _ { i } ) \right \} \right ]$$

for all functions f: Rd+l → R+.


<!-- p:49 -->


Proof. Take d' = d + l, and consider the following transition kernel from Rd to Rd':

$$p ( x , A \times K ) = \mathbf 1 ( x \in A ) \widetilde { p } ( x , K ) \quad x \in \mathbb { R } ^ { d } , A \subset \mathbb { R } ^ { d } , K \subset \mathbb { R } ^ { \ell } .$$

The independently marked Poisson p.p. can be seen as a transformation of the (non-marked) Poisson p.p. of intensity Λ on Rd by the probability kernel (2.3). The result follows from the Displacement Theorem (see Theorem 1.10). □

Remark. An immediate consequence of the above result and of i.m. Poisson p.p.  given a point at x with mark m is that of the i.m. Poisson p.p. with intensity measure Λ and with mark distribution Fx(dm). Moreover, a mere rewriting of the reduced Campbell formula for Poisson point processes yields

$$E \left [ \int _ { \mathbb { R } ^ { d } \times \mathbb { R } ^ { \ell } } f ( x , m , \Phi \ \{ x \} ) \widetilde { \Phi } ( d ( x , m ) ) \right ] \\ = \int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { R } ^ { \ell } } E \left [ f ( x , m , \widetilde { \Phi } ) \right ] F _ { x } ( d m ) \, M ( d x ) .$$

In the general case, independent marking leads to the following results:

Corollary 2.2. Let  be an i.m.p.p.

- (1) The mean measure of  is equal to

$$E [ \widetilde { \Phi } ( A \times K ) ] & = \int _ { A } F _ { x } ( K ) \, M ( d x ) \quad A \subset \mathbb { R } ^ { d } , \, K \subset \mathbb { R } ^ { \ell } , \\ \\ \intertext { u n s o n } \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \qu$$

where M(A) = E[Φ(A)] is the mean measure of the points Φ of Φ.

- at x with mark m is equal to the distribution of the i.m.p.p., with points distributed according to the reduced Palm distribution PI t of Φ and with the same mark distributions Fx(dm).


<!-- p:50 -->


- (3) (Reduced Campbell's formula for i.m.p.p.) For all nonnegative functions f defined on Rd × Re × ,

$$\begin{array} { r l } { \ n e g a t i v e f u n c t i o n s f i d e n o n \mathbb { R } ^ { d } \times \mathbb { R } ^ { \ell } \times \mathbb { M } , } \\ { E \left [ \int _ { \mathbb { R } ^ { d } \times \mathbb { R } ^ { \ell } } f ( x , m , \tilde { \Phi } \ \rangle \ \varepsilon _ { ( x , m ) } ) \widetilde { \Phi } ( d ( x , m ) ) \right ] } \\ { = \int _ { \mathbb { R } ^ { d } \times \mathbb { R } ^ { \ell } } \int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { R } ^ { ( x , m ) } } \widetilde { f } ( x , m , \widetilde { \phi } ) P _ { ( x , m ) } ^ { ! } ( d \widetilde { \phi } ) F _ { x } ( d m ) M } \end{array}$$

Proof. We only prove the first statement; for the remaining ones see e.g., Daley and Vere-Jones ([9]). Conditioning on Φ, we have

$$= E \left [ \int _ { \mathbb { R } ^ { d } } \mathbb { I } ( x \in A ) F _ { x } ( K ) \, \Phi ( d x ) \right ] = \int _ { A } F _ { x } ( K ) \, M ( d x ) ,$$

which proves (2.5).

□

### 2.1.2 Typical Mark of a Stationary Point Process

Many stochastic models constructed out of independently marked point processes may also be seen as marked point processes, however, they are often no longer independently marked. The Matérn model considered below in Section 2.1.3 is an example of such a situation; the Voronoi tessellation of Chapter 4 is another.

Consider thus a general marked p.p.  as in (2.1). In general, it is not true that, given the locations of points of Φ, the mark m of some x ∈ Φ is independent of other marks with its distribution determined only by x. However, it is still interesting and even of primary interest to the analysis of  to know the conditional distribution P{m ∈ · | x } of mark m given its point is located at x. In what follows, we treat this question in the case of a stationary p.p.

Definition 2.2. A marked point process (2.1) is said to be stationary if for any v ∈ Rd, the distributions of v +  = Σiε(v+xi,mi) and are the same. The constant λ = E[Φ(B)] = E[(B × Re)], where B has Lebesgue measure 1, is called its intensity.


<!-- p:51 -->


Note that in the above formulation the translation by the vector v "acts" on the points of Φ and not on their marks, thus ensuring that shifted points "preserve their marks".

Define the Campbell-Matthes measure Č of the marked p.p.  as

$$\widetilde { C } ( B \times K ) = \mathbf E \left [ \int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { R } ^ { \ell } } \mathbf 1 ( x \in B ) \mathbb { I } ( m \in K ) \, \widetilde { \Phi } ( d ( x , m ) ) \right ] .$$

If λ &lt; ∞, by arguments similar to those used in Section 1.4, one can show that it admits the representation

$$\widetilde { C } ( B \times K ) = \lambda | B | \nu ( K ) .$$

Definition 2.3. (Palm distribution of the marks) The probability measure ν(·) on the space of marks Rl given in (2.8) is called the Palm distribution of the marks.

The Palm distribution ν of the marks may be interpreted as the conditional distribution ν(·) = P{m ∈ · | 0 ∈ Φ} of the mark m of a point located at the origin 0, given 0 ∈ Φ. Not surprisingly, taking f (x, m, φ) = 1(x ∈ B)1(m ∈ K) in (2.6) and comparing to (2.8) we find that

Corollary 2.3. Consider a stationary i.m.p.p. For (almost all) x, the probability kernel of marks Fx(·) = ν(·· ·) is constant and equal to the Palm distribution of the marks.

In view of the above observation, we shall sometimes say that the points of a stationary i.m.p.p. are independently and identically marked.

Under the Palm probability P0 of a stationary p.p. Φ, all the objects defined on the same space as Φ have their distributions "seen" from the typical point of the process, which is located at 0 (cf. the discussion at the end of Section 1.6.1). In the case of a stationary m.p.p., under P0, the mark attached to the point at 0 has the distribution ν; this explains why it is also called the distribution of the typical mark. In this context, the Campbell–Matthes formula (1.18) can be rewritten to encompass the marks


<!-- p:52 -->


$$\mathbf E \left [ \int _ { \mathbb { R } ^ { d } } g ( x , \tilde { \Phi } - x ) \, \Phi ( d x ) \right ] = \lambda \int _ { \mathbb { R } ^ { d } } \mathbf E ^ { 0 } [ g ( x , \tilde { \Phi } ) ] \, d x .$$

Note that in the above formula, in contrast to (2.6), the m.p.p.  is not treated as some p.p. in a higher dimension but rather as a point process Φ on a probability space on which marks are defined as well. This approach is more convenient in the case of a stationary m.p.p., since it exploits the property of the invariance of the distribution of with respect to a specific translation of points which preserves marks (cf. Definition 2.2).1

The following observation is a consequence of Slivnyak's theorem 1.13:

Remark 2.1. Consider a stationary i.m. Poisson p.p.  with a probability kernel of marks Fx such that Fx(·) = F(·). One can conclude from Corollary 2.3 and the Remark after Corollary 2.1 that its distribution under the Palm probability P0 is equal to that of  + ε(0,mo), where is taken under the original (stationary distribution) P and the mark m0 of the point at the origin is independent of  and has the same distribution F(·) as for any of the points of .

Almost all stochastic models considered throughout this monograph are constructed from some marked point processes. Here is a first example driven by an i.m. Poisson p.p.

### 2.1.3 Matérn Hard Core Model

Hard core models form a generic class of point processes whose points are never closer to each other than some given distance, say h &gt; 0 (as if the points were the centers of some hard balls of radius h). For the Poisson p.p. there exists no h &gt; 0 such that the p.p. satisfies the hard core property for h.

1 The Palm probability P0 can be defined as the Palm distribution of the marks in the case when the whole configuration of points and all other random objects existing on the probability space "seen" from a given point of x ∈ Φ is considered as a mark of this point — the so called universal mark. This requires a more abstract space of marks than Re considered above; see Section 10.2 for more details.


<!-- p:53 -->


We now present a hard core p.p. constructed from an underlying Poisson p.p. by removing certain points of the Poisson p.p. depending on the positions of the neighboring points and additional marks attached to the points.

Let Φ be a Poisson p.p. of intensity λ on Rd:

$$\Phi = \sum _ { i } \varepsilon _ { x _ { i } } .$$

Let us consider the following independently marked version of this process:

$$\widetilde { \Phi } = \sum _ { i } \varepsilon _ { ( x _ { i } , U _ { i } ) } ,$$

where {Ui}i are random variables uniformly distributed on [0, 1]. Define new marks {mi} of points of Φ by

$$m _ { i } = 1 ( U _ { i } < U _ { j } \quad \text {for all } y _ { j } \in B _ { x _ { i } } ( h ) \ \{ x _ { i } \} ) .$$

n s  to ns  n ax t  , ot   Stns. indicator that the point xi is the "youngest" one among all the points in its neighborhood Bxi(h).

The Matérn hard core (MHC) point process is defined by:

$$\Phi _ { M H C } = \sum _ { i } m _ { i } \varepsilon _ { x _ { i } } .$$

ΦMHc is thus an example of a dependent thinning of Φ. In contrast to what happens for an independent thinning of a Poisson p.p. as considered in Section 1.3.2, the resulting MHC p.p. is not a Poisson p.p. Nevertheless some characteristics of the MHC p.p. can be evaluated explicitly, as we show shortly. Consider also the "whole" marked p.p.

$$\tilde { \Phi } _ { M H C } = \sum _ { i } \varepsilon _ { ( x _ { i } , ( U _ { i } , m _ { i } ) ) } .$$

Clearly MHc is not independently marked, because of {mi}. Nevertheless MHC (as well as ΦMHc) is stationary. This follows from the following fact. Let MHc() denote the (deterministic) mapping from to MHC. Then for all v ∈ Rd,


<!-- p:54 -->


$$\tilde { \Phi } _ { M H C } ( v + \widetilde { \Phi } ) = v + \tilde { \Phi } _ { M H C } ( \widetilde { \Phi } )$$

with v +  interpreted as in Definition 2.2.

We now identify the distribution of marks by first finding the distribution of the typical mark of MHC and then calculating the intensity λMHC of the p.p. ΦMHC. For B ⊂ Rd and 0 ≤ a ≤ 1, by Slivnyak's theorem (see Proposition 1.13)

$$\text {om} \, ( \text {see Proposition } 1 . 1 3 ) \\ \tilde { C } ( B \times ( [ 0 , a ] \times \{ 1 \} ) ) \\ = E \left [ \int _ { B } \int _ { [ 0 , a ] } \mathbb { 1 } ( u < U _ { j } \text { for all } y _ { j } \in B _ { x } ( h ) \cap \Phi \ \{ x \} ) \, \widetilde { \Phi } ( d ( x , u ) ) \right ] \\ = \lambda | B | \int _ { B } \int _ { 0 } ^ { a } \mathbb { P } \left \{ \left ( \sum _ { ( x _ { j } , U _ { j } ) \in \widetilde { \Phi } } \mathbb { 1 } ( U _ { j } \leq u ) \varepsilon _ { x _ { j } } \right ) ( B _ { x } ( h ) ) = 0 \right \} d u \, d x \\ = \lambda | B | \int _ { 0 } ^ { a } e ^ { - \lambda u \nu _ { d } h ^ { d } } d u = | B | \frac { 1 - e ^ { - \lambda \nu _ { d } h ^ { d } } } { \nu _ { d } h ^ { d } } , \\ \text {where } \nu _ { d } = \sqrt { \pi ^ { d } } / \Gamma ( 1 + d / 2 ) \text { is the volume of the ball } B _ { 0 } ( 1 ) \text { of } \mathbb { R } ^ { d } . \text {Com-} \\$$

where νd = √πd/Γ(1 + d/2) is the volume of the ball B0(1) of Rd. Comparing the last formula with (2.8), we find that

$$\nu ( d u \times \{ 1 \} ) = \mathbf P ^ { 0 } \{ U _ { 0 } \in d u , m _ { 0 } = 1 \} = e ^ { - \lambda u \nu _ { d } h ^ { d } } d u ,$$

for 0 ≤ u ≤ 1, where (U0, m0) is the mark of the point located at 0 under P0. In this formula, we recognize that U0 has the original uniform distribution of marks Ui and, given U0 = u, the point at 0 is retained in ΦMHC (i.e. m0 = 1) with probability e−λuνdhd.

In order to calculate the intensity λMHC of the Matérn p.p., we take a set B with volume |B| = 1 and obtain

$$\lambda _ { M H C } = \tilde { C } ( B \times [ 0 , 1 ] \times \{ 1 \} ) = \lambda P ^ { 0 } \{ m _ { 0 } = 1 \} = \frac { 1 - e ^ { - \lambda \nu _ { d } h ^ { d } } } { \nu _ { d } h ^ { d } } .$$

Notice that when λ → ∞, λMHC 1 hard spheres of radius h/2 with a volume fraction (proportion of space covered by spheres — see Section 3.4 for a general definition) of

$$p = \frac { 1 } { \nu _ { d } h ^ { d } } \nu _ { d } \left ( \frac { h } { 2 } \right ) ^ { d } = \frac { 1 } { 2 ^ { d } } .$$


<!-- p:55 -->


Remark 2.2. The value 1/2d is a good lower bound (sometimes called the "greedy" one) for the volume fraction obtained by any saturated hard sphere packing. A configuration of non-overlapping (hard) balls with the same radius is called saturated if no further ball with this radius can be added without violating the no-overlap constraint. Let p be the fraction of the space (say, in some empirical mean sense) covered by a saturated configuration {Bxi(R)}i of balls with radius R. The saturation condition implies that all points of the space are at distance no larger than 2R from the center of some ball of this configuration (otherwise a new ball could be added there). This implies that when doubling the radius of each ball of the original configuration, one obtains a full coverage of the space, i.e., 三 = Ui Bxi (2R) = Rd. The volume fraction p' of Ξ is thus equal to 1. On the other hand, when denoting by p the volume fraction of the original configuration, we get that p' ≤ 2dp (when using the multiplication of the radius by 2 and the inequality stemming from the overlapping). Thus 1 = p' ≤ 2dp, which implies p ≥ 1/2d.

For comparison, an upper bound given in ([6]) for the volume fraction of any hard sphere model valid for all d ≥ 1 is (d/2 + 1)2−d/2 and the best currently known upper bound is 2-0.5990d(1+o(1)) when d →∞ ([26]).

Table 2.1 gives the volume fractions of some classical hard-sphere models for d = 1, 2, 3.

Example 2.1 (Carrier sense multiple access). The above MHC model can be used as a (very) simple model of the instantaneous repartition of active nodes in an ad hoc network using carrier sensing mutiple access (CSMA) protocol (see Section 25.1.3 in Volume II). In this protocol, a node which wants to access the shared wireless medium senses its occupation and refrains from transmitting if the channel is already locally occupied. Hence, each active node creates some exclusion region around itself preventing other nodes located in this region from transmitting. The simplest possible model taking such an exclusion is the MHC with a radius h equal to the sensing (exclusion) range of CSMA.


<!-- p:56 -->


Table 2.1. Volume fractions of some classical hard-sphere models.

|   Model dimension |   saturated Mat ́ ern | RSA         | Densest packing   |
|-------------------|----------------------|-------------|-------------------|
|                 1 |                  0.5 | 0.747598... | 1.                |
|                 2 |                 0.25 | 0.54700     | 0.90689...        |
|                 3 |                0.125 | 0.38278     | 0.74048...        |

Volume fractions of some classical hard-sphere models. The left column gives the exact value (2.13) for the saturated Matérn model. The center column gives the value of the saturated RSA (Random Sequential Addition) model. For d = 1 this model, known as the Rényi car parking problem, has an exact solution; for d = 2,3 we used simulated values taken from [44]. It should be mentioned that the construction of the RSA model on the whole space is not trivial; see [43, 36] for a rigorous proof of the convergence of the empirical volume fractions when the observation window tends to infinity. The densest packing is given on the rightmost column. On the plane the densest packing is that of the hexagonal lattice (cf. Section 19.3.2 in Volume II), the volume fraction of which is 1/6π√3. For d = 3 it was conjectured by Kepler in 1611 and proved only recently that the cubic or hexagonal packings (which both have volume fraction π/(3√2)) are the densest possible.

Note that in this model λMHC = λMHc(λ, h) corresponds to the spatial density of active nodes in the ad hoc network of density λ, when this network uses CSMA with a sensing range of h.

## 2.2 Shot-Noise

### 2.2.1 General Point Processes

A shot-noise (SN) field is a non-negative vector random field I(y) defined for all y in some Euclidean space and which is a functional of a marked point process . Here is a list of the spaces involved in its definition:

- The field is defined on Rd' i.e., for all y ∈ Rd';
- It is generated by a marked point process  = Σi ε(xi,mi) on Rd with marks in Rl.
- The vector feld takes its values in (R+)k, i.e., IΦ(y) ∈ R+k for all y;

The additional ingredient for its definition is some non-negative response function L = (L1, . . ., Lk): Rd' × Rd × Rl → (IR+)k.


<!-- p:57 -->


Definition 2.4. Under the setting described above, the SN field associated with the marked point process Φ and the response function L is defined by

$$I _ { \widetilde { \Phi } } ( y ) & = ( I _ { 1 } ( y ) , \dots , I _ { k } ( y ) ) \\ & = \int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { R } ^ { \ell } } L ( y , x , m ) \, \widetilde { \Phi } ( d ( x , m ) ) \\ & = \sum _ { ( x _ { i } , m _ { i } ) \in \widetilde { \Phi } } L ( y , x _ { i } , m _ { i } ) , \quad y \in \mathbb { R } ^ { d ^ { \prime } } , \\ \intertext { h e i n g r a l a n d t h e s u m a r e e a l u f a l u d e n g p o n p e n t - w i s e }$$

where the integral and the sum are evaluated component-wise for the vector response function L.

e se r r e e s  e r sae re me point process Φ (i.e., d' = d) is the most common. The term "ShotNoise" comes from this special case with d = 1. It describes a stochastic process with 'shots' taking place at the epochs {Xi} of a Poisson point process on the real line, which represents time. The shot at Xi has an effect over time of the form l(t − Xi), where l: R → R+ is a function which is usually such that l(x) = 0 for x &lt; 0 (non anticipativeness) and decreasing for x ≥ 0. The Shot-Noise at time t,

$$I ( t ) = \sum _ { i } l ( t - X _ { i } ) \, ,$$

is then the sum' of the effects of the shots that took place before time t.

Since L is positive, I(y) is well defined but can be infinite. In the sequel, we require this random field to be a.s. finite and moreover to have finite expectation. Using the Campbell formula (2.6) we can easily express this expectation in the case of an i.m.p.p. .

Proposition 2.4. Let I(y) be the SN field as above and assume that is an i.m.p.p. Then

$$E [ I _ { \widetilde { \Phi } } ( y ) ] = \int _ { \mathbb { R } ^ { d } \times \mathbb { R } ^ { \ell } } L ( y , x , m ) \, F ( d m \, | \, x ) M ( d x )$$

componentwise.


<!-- p:58 -->


Proof. We have by (2.6)

$$= \int _ { \mathbb { R } ^ { d } \times \mathbb { R } ^ { \ell } } L ( y , x , m ) \, F ( d m \, | \, x ) M ( d x ) . \quad \square$$

Assuming that the right-hand side in (2.14) is finite for all y, we guarantee that each random vector I(y) has finite expectation and thus is finite almost surely. This however is not sufficient to be able to say that with probability 1 the whole field {I(y): y ∈ Rd' } is finite. For this latter, as well as for a continuity property of the paths of this field (which will be useful later on) we prove the following technical result.

Proposition 2.5. Let I(y) be the shot-noise field defined above and assume that  is an i.m.p.p. If for each y ∈ Rd', there exists €y &gt; 0 such that

$$\int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { R } ^ { \ell } \ z \in B _ { y } ( \epsilon _ { y } ) } \sup _ { B _ { y } ( \epsilon _ { y } ) } L ( z , x , m ) \, F ( d m \, | \, x ) M ( d x ) < \infty$$

componentwise, then with probability 1, the field I(y) is finite for all y ∈ Rd'. If moreover the response function L(y, x, m) is a continuous (lower semi-continuous) function in y for any fixed (x, m), then with probability 1, the field I(y) has continuous (lower semi-continuous) paths.

Proof. From the open covering {By(€y): y ∈ Rd' } of Rd′ one can choose a countable covering {Byw (€yw): w = 1,2, . ..} (this is possible since Rd′ is separable). From (2.15), there exists a subset Ω' of the space on which Φ is defined and having probability one, such that for all ω ∈Ω'

$$I ^ { \prime } ( y _ { w } ) = \int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { R } ^ { \ell } \ z \in B _ { y w } ( \epsilon _ { y w } ) } L ( z , x , m ) \, \widetilde { \Phi } ( d ( x , m ) ) < \infty ,$$

for all w = 1, 2,. . .. Consequently, for all ω ∈ Ω′ and z ∈ Rd', I(z) ≤ I'(yw(z)) &lt; ∞ componentwise, where w(z) denotes the center of the ball of radius €yw(z) of the countable coverage which covers z; i.e., z ∈ Byw(z) (€yw(z) ). This proves the first statement.


<!-- p:59 -->


For continuity (lower semi-continuity), take any z ∈ Rd' and zn → z (zn z). For sufficiently large n, zn and z belong to Byw(z)(€yw(z)). Then by dominated convergence,

$$\lim _ { n \to \infty } I _ { \widetilde { \Phi } } ( z _ { n } ) = \int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { R } ^ { \ell } } \lim _ { n \to \infty } L ( z _ { n } , x , m ) \, \widetilde { \Phi } ( d ( x , m ) ) = I _ { \widetilde { \Phi } } ( z ) \, ,$$

because L is continuous (lower semi-continuous) in its first argument. □

### 2.2.2 Poisson Point Processes

In the case of a SN I(y) = I(y) generated by an i.m. Poisson p.p. , the distribution of the SN vector I(y) is known in terms of its multivariate Laplace transform L1(y)(t1, . ., tk) = E[e−Σk=1tiIi(y)].

Proposition 2.6. Suppose that  is an i.m. Poisson p.p. with intensity measure Λ and mark distribution Fx(dm). Consider the SN I(y) = I ̄(y) with response function L = (L1, . . . , Lk). Then

$$\mathcal { L } _ { I ( y ) } ( t _ { 1 } , \dots , t _ { k } ) = \exp \left \{ - \int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { R } ^ { \ell } } \left ( 1 - e ^ { - \sum _ { i = 1 } ^ { k } t _ { i } L _ { i } ( y , x , m ) } \right ) F _ { x } ( d m ) \, \Lambda ( d x ) \right \} .$$

Proof. Observe that L1(y) (t1, . . . ,tk) = L(f) where L(·) is the Laplace transform of  at the function f = f(x,m)= − Σk=1tiLi(y,x, m). Equation (2.16) follows from Corollary 2.1 and Proposition 1.5. □

One can evaluate explicitly the higher moments of I by differentiating the above formula at 0.

Joint Distribution of the Field at Several Points. Let I(y) = I(y) be an SN field with response function L as in Definition 2.4 and let Ψ be a linear transformation (R+)k×n → (R+)k′ for some integers n and k'. Then

$$I _ { \widetilde { \Phi } } ^ { \prime } ( y _ { 1 } , \dots , y _ { n } ) = \Psi ( I ( y _ { 1 } ) , \dots , I ( y _ { n } ) )$$


<!-- p:60 -->


is an SN field on Rd'×n with response function

$$L ^ { \prime } ( ( y _ { 1 } , \dots , y _ { n } ) , x , m ) = \Psi ( L ( y _ { 1 } , x , m ) , \dots , L ( y _ { n } , x , m ) ) .$$

In particular, taking Ψ(a1,..,an) = Σj=1aj, we see that the ndimensional aggregate Iγ(y1, . .,n) = Σj=1 I(yj) is a SN on Rd'×n with associated function LΣ,((y1, . ,yn), x, m) = Σn=1 L(yj, x, m). Similarly, the integrals I(A) = ∫AI(y)dy can be interpreted as a shotΦ noise field on the space of (say) closed subsets A ⊂ Rd'. As another immediate consequence of the above formulation, we have the next result by setting k′ = k × n, using the identity transformation Ψ and appealing to Proposition 2.6:

Corollary 2.7. Let I = I(y) be as in Proposition 2.6. Then the joint Laplace transform, LI(y)(t) of the vector I(y) = (I(y1), . . . , I(yn)) is given by

$$\mathcal { L } _ { I ( y ) } ( t ) = \exp \left \{ - \int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { R } ^ { \ell } } \left ( 1 - e ^ { - \sum _ { j = 1 } ^ { n } \sum _ { i = 1 } ^ { k } t _ { i j } L _ { i } ( y _ { j } , x , m ) } \right ) F _ { x } ( d m ) \Lambda ( d x ) \right \} ,$$

where t = (tij: j = 1, . . , n, i = 1, . . . , k).

Absolute Continuity. In the following proposition, we give simple conditions for the Poisson SN vector I(y) to have a probability law which is absolutely continuous (has a density) with respect to Lebesgue measure. This property can be used to derive the distribution function of the shot-noise from its Laplace (or Fourier) transform via the Plancherel-Parseval Theorem (cf. Section 12.1).

Proposition 2.8. Let I = I(y) be as in Proposition 2.6.

If Λ(Rd) = ∞ and if, for each A ⊂ (R+)k of Lebesgue measure 0,

$$( 2 . 1 7 )$$

then, for all y ∈ Rd', the random vector I(y) is absolutely continuous with respect to the k-dimensional Lebesgue measure (i.e. has a density).


<!-- p:61 -->


Proof. Fix y ∈ Rd'; without loss of generality let y = 0. Take A ⊂ (R+)k of k-dimensional Lebesgue measure 0. For any r &gt; 0

$$P \{ I _ { \widetilde { \Phi } } ( 0 ) \in A \} = P \{ I _ { r } + I _ { r } ^ { c } \in A \} ,$$

where Ir = ∫|x|≤r ∫Re L(0, x, m) δ(d(x, m)) and Ic = ∫|x|&gt;r ∫Re L(0, x, m) Φ(d(x, m)). By the Poisson assumption Ir and Ic are independent. Moreover

$$P \{ I _ { \widetilde { \Phi } } ( 0 ) \in A \} & = \sum _ { n = 0 } ^ { \infty } P \{ I _ { r } + I _ { r } ^ { c } \in A \ | \ \widetilde { \Phi } \{ x \colon | x | \leq r \} = n \} \\ & \quad \times P \{ \widetilde { \Phi } \{ x \colon | x | \leq r \} = n \} .$$

Recall from the discussion at the end of Section 1.1.1 that conditioned on Φ{x: |x| ≤ r} = n, with n &gt; 0, the random variable Ir can be represented as the sum of n independent random variables, distributed as L(0, x, m) where x and m have joint distribution

$$\frac { 1 } { \Lambda ( \{ x \colon | x | \leq r \} ) } F _ { x } ( d m ) \Lambda ( d x ) .$$

Thus, by (2.17)

$$P \{ I _ { r } + I _ { r } ^ { c } \in A | \widetilde { \Phi } \{ x \colon | x | \leq r \} = n \, \} = 0 .$$

Consequently,

$$P \{ I _ { \widetilde { \Phi } } ( 0 ) \in A \} \leq P \{ \Phi \{ x \colon | x | \leq r \} = 0 \} \to 0 \quad \text {when } r \to \infty$$

because Λ(Rd) = ∞. This completes the proof.

## 2.3 Interference Field as Shot-Noise

Consider a collection of transmitters distributed in the space and sharing a common radio medium. Following the observations made in Chapter 23 in Volume II, assume that signal attenuation depends on distance (cf. Section 23.1 in Volume II) and some stochastic ingredients (cf. Section 23.2 in Volume II).

The total power received from this collection of transmitters at a given location is in essence a shot-noise field at this location. For instance in the case of a planar model with omni-directional antennas,

□


<!-- p:62 -->


the simplest model consists of

- a collection of points {xi} representing the locations of transmitters on the plane R2 (d = 2 in Definition 2.4);
- marks mi = pi representing the powers of the transmitters (l = 1); and
- a scalar (k = 1) response function L(y, x,p) = p/l(|x − y|), where l is the omni-directional path-loss function (cf. Section 23.1.2 in Volume II).

As we shall see, fine elements of the radio wave propagation model (antenna azimuth, random fading model, etc.) can be taken into account by enriching the marks of the p.p.

As outlined in Section 24.3.4 in Volume II, the total power received from a set of transmitters scattered in the plane can often be considered as interference or noise with respect to the signal received from one (or more) transmitter(s) not belonging to this set. Within this setting, this total power plays a key role in detection theory as explained in Section 24.3.4 in Volume II. The fact that the interference field of such a set of transmitters can be interpreted as a shot-noise field opens new ways of assessing its statistical properties. In the same way as Rayleigh fading was shown to be an efficient statistical model better suited to assessing the fluctuations of a multipath channel than solving the electromagnetic field equations, the shot-noise model can be seen to be an efficient statistical model for predicting the fluctuations of the interference field. This is often more practical than evaluating exactly the power of interference.

### 2.3.1 Standard Stochastic Scenario

Consider a marked point process  = {xi, pi} with points on the plane {xi} ∈ R2 and marks pi ∈ R+. Points represent transmitter locations and marks emitted powers. Consider some isotropic or ommi-directional path-loss (OPL) function l, for example, models OPL 1-OPL 3 described in detail in Example 23.3 in Volume II and defined as follows:

$$( O P L \ 1 ) \ l ( r ) & = ( A \max ( r _ { 0 } , r ) ) ^ { \beta } , \\ ( O P L \ 2 ) \ l ( r ) & = ( 1 + A r ) ^ { \beta } , \\ ( O P L \ 3 ) \ l ( r ) & = ( A r ) ^ { \beta } ,$$


<!-- p:63 -->


for some A &gt; 0, r0 &gt; 0 and β &gt; 2, where β is called the path-loss exponent. Assuming the signals are transmitted and received by omnidirectional antennas, the total power received at some location y is

$$I ( y ) = I _ { \widetilde { \Phi } } ( y ) = \sum _ { ( x _ { i } , p _ { i } ) \in \widetilde { \Phi } } \frac { p _ { i } } { l ( | y - x _ { i } | ) } , \ \ y \in \mathbb { R } ^ { 2 } . \\$$

We shall often consider the following standard stochastic scenario for the above interference shot-noise field:

- (1) Φ is a stationary i.m.p.p. with points in R2 and intensity λ;
- (2) the marks have some distribution P{p ≤ s } = G(s) that does not depend on the location of the point.

-o  e se o or  d  t odoe tion 25.2 in Volume II where powers are functions of the transmitter locations.

Kendall-like Notation for the Standard Interference Model. Mimicking Kendall's notation in queuing theory, we call the above standard stochastic scenario of SN a GI/GI interference model, where the first GI denotes a general independently marked stationary p.p. and the second GI stands for a general mark distribution. Some special cases are:

M/· if the underlying i.m.p.p.  is Poisson;

D/· if the underlying i.m.p.p. Φ is deterministic;

·/M if the marks are exponentially distributed; i.e. G(s) = 1 − e−μs with μ ≥ 0.

·/D if the marks are deterministic (constant).

For instance, the interference field in a MANET with nodes located according to a Poisson p.p. and without power control (see Section 25.3.1 in Volume II) can be seen as an M/· SN. Similarly, the famous honeycomb model used in certain cellular network models for representing the location of base stations leads to a downlink interfero od o od  e   e    oe used (see Section 25.3.2 in Volume II).

Remark 2.3. Assume that emitted powers pi = p are constant and that we have some Rayleigh fading (see Section 23.2.4 in Volume II).


<!-- p:64 -->


Then the power received at the location y from a transmitter at xi is equal to pFi/l(|xi − y|), where Fi is an exponential random variable with mean 1. Thus, interpreting pFi as a "virtual power" (which is hence exponential with mean p), the GI/M model may be used to describe the interference in the presence of Rayleigh fading. In what follows, we shall most often work directly with the virtual power, or equivalently assume that Rayleigh fading is represented by an exponential random variable of parameter μ = p−1.

The independence between Fi for different transmitters, which is assumed in the GI/M model, can be justified if the point process is sparse on the scale of the coherence distance (see Section 23.3 in Voluo      oe   oe ( en location. Indeed, using the same value of the fading Fi from point xi to different locations y ∈ R2 would not be a reasonable assumption as the channel conditions change significantly when y varies more than the coherence distance. We will return to this problem in Section 2.3.3.

Corollary 2.9. The mean total received power in the GI/GI model is constant and equal to

$$E [ I ( y ) ] & = E [ I ] \\ & = E [ p ] \lambda \int _ { \mathbb { R } ^ { 2 } } \frac { 1 } { l ( | y | ) } \, d y \\ & = \int _ { 0 } ^ { \infty } ( 1 - G ( s ) ) \, d s \, 2 \pi \lambda \int _ { 0 } ^ { \infty } \frac { r } { l ( r ) } \, d r . \quad ( 2 . 1 9 ) \\ \intertext { b o d e r } \L a o p l e o o w _ { \ } t h o w \, i n \, t h o w \, M / C I _ { \ } m o d o l _ { \ } i s$$

The Laplace transform of the received power in the M/GI model is equal to

$$\mathcal { L } _ { I ( y ) } ( t ) = \mathcal { L } _ { I } ( t ) = \exp \left \{ - 2 \pi \lambda \int _ { 0 } ^ { \infty } r \left ( 1 - \mathcal { L } _ { p } ( t / l ( r ) ) \right ) d r \right \} ,$$

where Lp(t) = ∫α e−ts G(ds) is the Laplace transform of the transmitted power. The second moment in the M/GI model is equal to

$$E [ I ^ { 2 } ( y ) ] = ( E [ I ] ) ^ { 2 } + E [ p ^ { 2 } ] \, 2 \pi \lambda \int _ { 0 } ^ { \infty } \frac { r } { ( l ( r ) ) ^ { 2 } } \, d r \, .$$


<!-- p:65 -->


Example 2.2. For the M/M model, these values are equal to

$$E [ I ] = \frac { 2 \pi \lambda } { \mu } \int _ { 0 } ^ { \infty } \frac { r } { l ( r ) } \, d r , \\$$

$$\mathcal { L } _ { I } ( t ) = \exp \left \{ - 2 \pi \lambda \int _ { 0 } ^ { \infty } \frac { r } { 1 + \mu l ( r ) / t } \, d r \right \} .$$

Below, we use the fact that

$$\int _ { 0 } ^ { \infty } \frac { 1 } { 1 + x ^ { u } } d x = 1 / u \Gamma ( 1 / u ) \Gamma ( 1 - 1 / u ) .$$

Assuming OPL 3 for l, one obtains

$$\mathcal { L } _ { I } ( t ) = \exp \left \{ - \lambda \left ( \frac { t } { \mu } \right ) ^ { 2 / \beta } \frac { K ( \beta ) } { A ^ { 2 } } \right \} ,$$

with

$$K ( \beta ) = \frac { 2 \pi ^ { 2 } } { \beta \sin ( 2 \pi / \beta ) } = \frac { 2 \pi \Gamma ( 2 / \beta ) \Gamma ( 1 - 2 / \beta ) } { \beta } \, .$$

Assuming OPL 1 for l with β = 4, one obtains

$$\mathcal { L } _ { I } ( t ) & = \exp \left [ \frac { \lambda \pi } { A ^ { 2 } } \sqrt { \frac { t } { \mu } } \arctan \left ( ( A r _ { 0 } ) ^ { 2 } \sqrt { \frac { \mu } { t } } \right ) \\ & - \frac { \lambda \pi ^ { 2 } } { 2 A ^ { 2 } } \sqrt { \frac { t } { \mu } } - \lambda \pi r _ { 0 } ^ { 2 } \frac { t } { t + ( A r _ { 0 } ) ^ { 4 } \mu } \right ] .$$

Corollary 2.10. Consider an M/GI model with the non-null marks (i.e., G(0) &lt; 1), for which at least one of the following conditions is satisfied: the distribution function G of the mark admits a density or the OPL function l(r) is strictly decreasing. Then for 0 ≤ a ≤ b

$$P \{ a \leq I \leq b \} = \int _ { - \infty } ^ { \infty } \mathcal { L } _ { I } ( 2 i \pi s ) \frac { e ^ { - 2 i \pi b s } - e ^ { - 2 i \pi a s } } { 2 i \pi s } \, d s \, ,$$

provided ∫-∞|L1(2iπs)|2ds &lt; ∞.


<!-- p:66 -->


Proof. Under our assumptions, by Proposition 2.8, the SN I has a density that is square integrable provided the Fourier transform of I is square integrable (see [14, p.510]). Then the result follows by the Plancherel-Parseval theorem (see Lemma 12.1). □

Remark 2.4. For the GI/GI scenario with OPL 1 and OPL 2 and E[p] = ∫0∞ s G(ds) &lt; ∞ we can conclude from Proposition 2.5 and formula (2.19) with l(r) replaced by l(max(r − €, 0)) that, with probability 1, the SN field Iĩ(y) is finite for all y ∈ R2. For OPL 3 one has to be more careful. Note that by (2.19) the integral expressing E[I] is infinite in this case for β &gt; 2 due the pole at the origin (cf. also Example 23.3 in Volume II). Consequently, the simplified isotropic path-loss function OPL 3 cannot be used to model the mean interference field created by a homogeneous i.m.p.p. on the plane. However, with probability 1, I(y) is finite for all y ∈ R2 except for y ∈ Φ. One can prove this by considering the mean of the shot-noise created by transmitters outside some vicinity of the receiver (which is finite) and knowing that the number of transmitters within this vicinity is finite with probability 1.

Using the explicit formula (2.20) one can also check that in the M/GI model with OPL 3 and G(0) &lt; 1 the Fourier transform L1(2iπ) of I is square integrable.

Note that for the M/GI model, Proposition 2.6 allows one to calculate the joint Laplace transform of the received power at several locations.

## 2.3.2*Directional Antennas

In the case of directional transmitter antennas, one can enrich the marked point process Φ of the previous section by taking as marks (pi, θi), where pi is, as above, the power transmitted by point xi and where θi is its antenna azimuth. We assume all the antennas have the same radiation pattern α2 = α2 (cf. Section 23.1.2 in Volume II). If this is not the case, one has to consider the whole radiation pattern function as the mark of a point. Using the model (23.3 in Volume II), it makes sense to model the total power received at y by the shot-noise


<!-- p:67 -->


$$I ( y ) = I _ { \widetilde { \Phi } } ( y ) = \sum _ { ( x _ { i } , ( p _ { i } , \theta _ { i } ) ) \in \widetilde { \Phi } } \frac { p _ { i } \bar { \alpha } ^ { 2 } ( \theta _ { i } - \mathcal { L } ( y - x _ { i } ) ) } { l ( | y - x _ { i } | ) } \, , \quad y \in \mathbb { R } ^ { d } . \quad ( 2 . 2 9 )$$

Corollary 2.11. The mean total received power in a GI/GI interference model with directional antennas having the same radiation pattern α2 and having independently, uniformly distributed azimuth θ is constant in y and equal to

$$E [ I ( y ) ] = E [ I ] = \int _ { 0 } ^ { \infty } ( 1 - G ( s ) ) \, d s \, \frac { 1 } { 2 \pi } \int _ { 0 } ^ { 2 \pi } \bar { \alpha } ^ { 2 } ( \theta ) \, d \theta \, 2 \pi \lambda \int _ { 0 } ^ { \infty } \frac { r } { l ( r ) } \, d r \, .$$

The Laplace transform of the received power in the M/GI model with the above directional antennas is equal to

$$\mathcal { L } _ { I ( y ) } ( t ) = \mathcal { L } _ { I } ( t ) = \exp \left \{ - \lambda \int _ { 0 } ^ { 2 \pi } \int _ { 0 } ^ { \infty } r ( 1 - \mathcal { L } _ { p } ( t \bar { \alpha } ^ { 2 } ( \theta ) / l ( | r | ) ) \, d r \, d \theta \right \} .$$

Example 2.3. Continuing Example 23.4 in Volume II, note that for the radiation pattern RP0 we have 1 ∫−π α2(θ) dθ = 1, whereas for RP1, π this integral can be expressed in terms of the Sine integral

$$\frac { 1 } { 2 \pi } \int _ { - \pi } ^ { \pi } \frac { \sin ( \omega \theta ) } { \omega \theta } \, d \theta = \frac { 1 } { \omega \pi } \int _ { 0 } ^ { \omega \pi } \frac { \sin \theta } { \theta } \, d \theta = \frac { S i ( \omega \pi ) } { \omega \pi } \, .$$

Numerical integration for ω = 1.81 (so as to have α2(π/3) = 1/2 = 3dB) gives

$$\frac { 3 } { 2 \pi } \, \frac { 2 S i ( \omega \pi ) } { \omega } = 0 . 3 9 6 8 .$$

For a general radiation pattern RP2, the integral ∫ ̄π α2(θ) dθ can be easily evaluated analytically

$$\frac { 1 } { 2 \pi } \int _ { - \pi } ^ { \pi } \bar { \alpha } ^ { 2 } ( \theta ) \, d \theta = \frac { 1 } { 2 \pi } \, \frac { - 6 \theta _ { 1 } \pi + 9 \theta _ { 1 } ^ { 2 } - 9 \theta _ { 2 } ^ { 2 } + 1 8 \theta _ { 2 } \pi - 4 \pi ^ { 2 } } { 6 ( \pi - 3 \theta _ { 1 } ) } \, .$$

The above value for θ1 = π ,θ2 = 23 π is equal to 19/48 = 0.39583. 12


<!-- p:68 -->


### 2.3.3 Fading Field

We return to the question of the joint law of the interference field at several locations of the space in the case of a Rayleigh fading, already alluded to above. We consider this question in the omni-directional path-loss function case.

In order to model the actual received power, one introduces a random fading field F = F(x, y) on R2 × R2, where F(x, y) reflects the multipath signal propagation from x to y (cf. Chapter 23 in Volume II). It is then natural to introduce the response function

$$L ( y , x , p ) = p F ( x , y ) / l ( | x - y | )$$

in the SN description of the interference field. Consequently, a fadingaware SN model takes the form

$$I ( y ) = I _ { \widetilde { \Phi } } ( y ) = \sum _ { ( x _ { i } , ( p _ { i } , F _ { i } ) ) \in \widetilde { \Phi } } \frac { p _ { i } F _ { i } ( y ) } { l ( | y - x _ { i } | ) } \, , \quad y \in \mathbb { R } ^ { d } \, , \quad \ ( 2 . 3 0 )$$

where Fi(·) = F(xi, ·). Note the above formula remains compatible with Definition 2.4 with marks mi = (pi, Fi(·)) which comprise the emitted power and the fading fields of transmitter xi (we admit, however, that the space of this mark is more complex than Rl as assumed in Definition 2.4).

As far as probabilistic assumptions are concerned, it is difficult to describe completely the distribution of the fading field F(·, ·), and thus of the marks Fi(·). However, inspired by what is said in Section 23.2.4 in Volume II it is reasonable to assume the following fading process postulates:

- (1) The stochastic process F(., ·) is independent of the other elements of the standard scenario for SN described in Section 2.3.1 and has a constant marginal distributions with mean 1.
2. ne s     &lt; |x − x|  ∇ &lt; | − I|  () then F(x1, y1) and F(x2, y2) are independent random variables.
- (3) If |y1 − y2| &lt; δ and |x1 − x2| &lt; δ, where δ &lt; ∆ is some constant, then F(x1, y1) = F(x2, y2).


<!-- p:69 -->


Remark. Typically the constants δ and ∆, which are related to the coherence distance, are of the order of the wave-length, and so are very small compared to the typical distance between transmitters and/or receivers.

#### 2.3.3.1 Interference at a SingleLocation

The above fading process postulates, together with the exact form of the marginal distribution of F, are enough to evaluate (or to reasonably approximate) the characteristics of the interference field at one location, say y0. In this case only the distribution of the vector (Fi = Fi(yo) = F(xi, y0): xi ∈ Φ) is required. Our postulates on the fading process and the remark following them justify the assumption that this is a vector of independent and identically distributed (i.i.d.) random variables. This assumption is reasonable at least if the mean nearest neighbor distance for the point process Φ (which equals 1/(2√λ) in the case of the Poisson p.p. with intensity λ) is much larger than the constant ∆ in the second postulate. Thus, taking a standard model with pi := piFi captures the fading effect well. Recall in particular that a constant emitted power p Ran, a    r  s tng una powers" pi (and no fading).

### 2.3.3.2Fading at Discrete Locations

We now focus on the value of the interference field at several locations of the plane, say y1, . . . , Yk.

Our standard model for SN (see Section 2.3.1) can be enriched by random variables representing fading in the channel from xi ∈ Φ to yj, for each pair (i,j) of transmitter i = 1,... and receiver locations, j = 1,. . ., k. For this, one considers marks (pi, (F 1 , dom vector representing the value of Fi = F(xi, yj), the fading in the channels from transmitter i to receivers yj, j = 1, . . . , k.

Consider the vector shot-noise field (I1(y), . .. , Ik(y)) defined on R2×k by

$$I _ { j } ( y ) = \sum _ { ( x _ { i } , ( p _ { i } , ( F _ { i } ^ { 1 } , \dots , F _ { i } ^ { k } ) ) ) \in \widetilde { \Phi } } \frac { p _ { i } F _ { i } ^ { j } } { l ( | y - x _ { i } | ) } .$$


<!-- p:70 -->


Note that due to our assumption on the fading, the value of this vector field taken at (y1, . . . , yk), i.e., (I1(y1), . . . , Ik(yk)) corresponds to the total power received by yj from all the transmitters xi when the fading from xi to yj is F i .

As far as probabilistic assumptions are concerned we assume that

- (1)  is a general stationary i.m.p.p. in R2 with intensity λ (note that the i.m. assumption is reasonable in view of our postulates for the fading process, at least for point processes with a mean nearest neighbor distance sufficiently large compared to ∆), and
- (2) marks are identically distributed and such that p and the vector (F1, . . . , Fk) are independent; we denote by Fpower(dp) the distribution of p.

When appropriate, we also assume the following:

- (3) The components of the fading vector (F1, . ., Fk) are i.i.d. 2

A Rayleigh fading channel would consist in assuming Fj exponential random variables (cf. Section 23.2.4 in Volume II).

Kendall-like Notation (cont.). By analogy with queuing theory, we call the model (2.31) a GI/GI/k SN, where k stands for the number of different channels represented. If the underlying point process is Poisson, we denote it by M/·/k, while ·/M/k stands for the model with independent exponential received powers in each of the k channels (e.g. constant emitted power and Rayleigh fading).

As above, using (2.5), we can calculate the mean value of the total signal received at yk in the GI/GI/k model:

$$E [ I _ { j } ] = E [ p ] E [ F ] \int _ { \mathbb { R } ^ { 2 } } \frac { 1 } { l ( | y - x | ) } \, M ( d x ) \, ,$$

where E[F] is the mean fading of the channel.

For the M/GI/k model, i.e. under the assumption that  is an i.m. Poisson p.p., by Corollary 2.7, we can evaluate the joint Laplace transfor (1,..k)(t,.,tk) = [exp{− Σj=1tj,Ij.,j].

2 Assumption 3 is reasonable if the locations y1, . . . , yk, are we,ll separated in space.


<!-- p:71 -->


Corollary 2.12. For the M/GI/k SN

$$& = \exp \left \{ - \int _ { \mathbb { R } ^ { d } } \left ( 1 - \int _ { \mathbb { R } ^ { \ell } } \mathcal { L } _ { f } \left ( \frac { \ p t _ { 1 } } { l ( | y _ { 1 } - x | ) } , \\ & \dots , \frac { \ p t _ { k } } { l ( | y _ { k } - x | ) } \right ) F _ { p o w e r } ( d p ) \right ) \Lambda ( d x ) \right \} , \\ & \text {le} \, \L a l a c e \, t r a n s f o r m o t h e f a d i n g e r \, v e c t o r \, f \, \text {If} \, f$$

where Lf(t1, . . . , tk) is the Laplace transform of the fading vector f. If f consists of independent components then Lf(t1, . . .,tk) = Ik=1 Lf (tj).

Example 2.4 (Random cross-fading model). In the previous example, we considered some finite set of fixed locations and a random pattern of transmitters. Consider now a more general situation, when one has a random pattern of transmitters Φe and another, possibly infinite, random set Φr of receivers. This model is very flexible and does not exclude the case where certain transmitters and receivers are located at the same points, i.e. possibly Φe ∩ Φr ≠ ∅; in the extreme case, one can consider Φe = Φr. In this context, it is useful to attach to xi marks of the form (pi, fij, xj ∈ Φr) where pi denotes the power of transmitter xi and fij the fading of the channel from xi to yj. This model could be denoted by GI/GI/∞ and is related to the so-called random connection model considered in continuum percolation (see [31]).

### 2.3.4 Time-Space Shot-Noise

This section is concerned with a time-space model which leads to a vector shot-noise field, namely to a field which takes its values in (R+)k with k &gt; 1 (see the beginning of Section 2.2.1). The basic data in this model are:

- a collection of points {xi} representing the locations of transmitters on the plane R2 (d = d' = 2 in Definition 2.4);
- a collection of marks Pi ∈ R+k; the ith coordinate of Pi, denoted by pi,n, is the power/fading of transmitter i at time 1 ≤ n ≤ k (the dimension l of the mark space of Definition 2.4 is hence here equal to k); and


<!-- p:72 -->


- a k-dimensional response function L(y, x, P) with nth coordinate Ln(y, x, P) = pn/l(|x − y|), where pn is the nth coordinate of P and where l is some omni-directional path-loss function.

This time-space model is a natural extension of the standard model of Section 2.3.3.1: transmitters are fixed but their power/fading conditions change over time and

$$I ( y ) = \sum _ { i } L ( y , x _ { i } , P _ { i } ) \in \mathbb { R } ^ { + k } \\$$

is then the vector of R+k the nth coordinate of which, denoted by In(y), gives the interference at location y and at time n. Proposition 2.6 allows one to derive the Laplace transform LI(y)(t1, . . . tk) = E[e− Σn=1 tnIn(y)] of I(y).

A natural instance of the model is that where the transmitter locations form a Poisson p.p. of intensity λ, the marks Pi are i.i.d. and the coordinates of Pi are i.i.d. Then

$$C o r d a m a t e s \, & \, 0 \, 1 \, i \, a r e \, 1 . 1 . d . \, 1 \, \text {len} \\ \mathcal { L } _ { I ( y ) } ( t _ { 1 } , \dots , t _ { k } ) = & \exp \left \{ - 2 \pi \lambda \int _ { 0 } ^ { \infty } r \left ( 1 - \prod _ { n = 1 } ^ { k } \mathcal { L } _ { p } ( t _ { n } / l ( r ) ) \right ) d r \right \} , \\ \\ \text {where } \mathcal { L } _ { n } ( u ) \, \text { denotes the Laplace transform of } p _ { 1 } \, u ,$$

where Lp(u) denotes the Laplace transform of p1,1 at u.

## 2.4 Extremal Shot-Noise

We now introduce a shot-noise model in which instead of adding the impact of all points (and their marks) we look for points having extremal impact. For simplicity, we consider here only a scalar extremal shot-noise field defined on the same space as the point-process . More precisely, consider a marked point process  = Σiε(xi,mi) on Rd with marks in Rl and some non-negative response function L:ird' × Rd × Rl → R+.

Definition 2.5. Given a marked point process  and response function as above the extremal shot-noise (ESN) field is defined by

$$X _ { \widetilde { \Phi } } ( y ) = \sup _ { ( x _ { i } , m _ { i } ) \in \widetilde { \Phi } } L ( y , x _ { i } , m _ { i } ) , \ \ y \in \mathbb { R } ^ { d ^ { \prime } } .$$


<!-- p:73 -->


Since L is positive, Xõ(y) is well defined but can be infinite.

Interestingly, the finite-dimensional distributions of the field {X(y) = X(y):y ∈ Rd' } can be expressed via the Laplace transform of certain associated (additive) shot-noise variables. For this note that

$$P \{ X ( y _ { 1 } ) \leq t _ { 1 } , \dots , X ( y _ { k } ) \leq t _ { k } \} \\ = P \{ L ( y _ { j } , x _ { i } , m _ { i } ) \leq t _ { j } \text { for all } j = 1 , \dots , k , ( x _ { i } , m _ { i } ) \in \tilde { \Phi } \} \\ = E \left [ \exp \left \{ \sum _ { ( x _ { i } , m _ { i } ) \in \tilde { \Phi } } \log \left ( \prod _ { j = 1 } ^ { k } \P ( L ( y _ { j } , x _ { i } , m _ { i } ) \leq t _ { j } ) \right ) \right \} \right ] . \ \ ( 2 . 3 3 ) \\$$

Consequently, for i.m. Poisson p.p. we can express these finitedimensional distributions explicitly.

Proposition 2.13. Suppose that  is an i.m. Poisson p.p. with intensity measure Λ and mark distribution Fx(dm). Consider the ESN X(y) = X(y) with the response function L. Then

$$P \{ X ( y _ { 1 } ) \leq t _ { 1 } , \dots , X ( y _ { k } ) \leq t _ { k } \} \\ = \exp \left \{ - \int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { R } ^ { \ell } } \left ( 1 - \prod _ { j = 1 } ^ { k } \mathbb { 1 } ( L ( y _ { 3 } ( y _ { j } - 1 ) + 1 ) ) \right )$$

In particular

$$P \{ X ( y ) \leq t \} = \exp \left \{ - \int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { R } ^ { \ell } } \mathbb { I } ( L ( y , x , m ) > t ) \, F _ { x } ( d m ) \, \Lambda ( d x ) \right \} .$$

Proof. The results follow from (2.33) and (2.2).

□

The extremal shot-noise model is often used in situations where one looks for some optimal transmitter/receiver. For instance, the extremal shot-noise X(y) represents the strongest signal power received at y.


<!-- p:74 -->


3

### Boolean Model

In this chapter, we introduce the most celebrated model of stochastic geometry — the Boolean model (BM). It is also a basic model of continuum percolation.

## 3.1 Boolean Model as a Coverage Process

In the simplest setting, the BM is based on (1) a Poisson p.p., whose points are also called germs, and (2) an independent sequence of i.i.d. compact sets called the grains. The Poisson set of germs and the independence of the grains make the BM analytically tractable. The BM is often used as the null hypothesis in stochastic geometry modeling.

We define the BM as a model driven by an i.m. Poisson p.p. on Rd,

$$\tilde { \Phi } = \sum _ { i } \varepsilon _ { ( x _ { i } , \equiv _ { i } ) } \, ,$$

with marks 三i being independent random closed sets (RACs) of Rd, representing the grains. One can make the set of closed subsets of Rd a measurable space (see [29]). Note that in Section 2.1 we considered (for simplicity) only marks mi in some Euclidean space Rl. To handle more general mark spaces we can think of subsets 三i as being chosen from some family of closed sets, 三i ∈ {三(m): m ∈ Rl}, by a random sampling of some parameter m ∈ Rl. Perhaps the simplest example is the following family of random closed balls:


<!-- p:75 -->


Example 3.1 (Random closed balls). By a random closed ball we mean a closed ball 三(m) = B0(m) of random radius m ∈ R+, centered at the origin 0 ∈ Rd.

More general, non-parametric RACs, modeling possibly very irregular random grains, can also be considered using the measure-theoretic formalism (see [29]).

Let us introduce the following operations on the subsets A, B ∈ Rd of the Euclidean space:

$$A \oplus B & = \{ x + y \colon x \in A , y \in B \} , \\ x + B & = \{ x + y \colon y \in B \} , \quad \text {for } x \in \mathbb { R } ^ { d } , \\ \check { B } & = \{ - x \colon x \in B \} , \\ r B & = \{ r y \colon y \in B \} , \quad \text {for } r \in \mathbb { R } .$$

Definition 3.1. Let Φ be a Poisson p.p. of intensity Λ(·) on Rd and let be given by (3.1) for some independent and i.i.d. sequence of marks {三i} which are RACs of Rd. We assume that the common distribution of these RACs satisfies the condition that

$$E [ \Lambda ( \check { \Xi } \oplus K ) ] < \infty , \ \text { for each compact } K \subset \mathbb { R } ^ { d } \ ,$$

where Ξ is a generic RAC with this distribution. The associated Boolean model is the union

$$\Xi _ { B M } = \bigcup _ { i } \left ( x _ { i } + \Xi _ { i } \right ) .$$

Lemma 3.1 below shows that condition (3.2) guarantees that almost surely, in each bounded window, there are at most finitely many grains. This desired local structure of the model implies that the countable infinite union 三BM of closed sets xi + 三i is a closed set and thus that the BM is also a RAC.

We often consider the following example of a BM.


<!-- p:76 -->


Example 3.2 (Homogeneous BM in Rd with random spherical grains). Let Φ be a stationary Poisson process with intensity λ on Rd (i.e., Λ(dx) = λdx). Assume that 三i = B0(Ri) where Ri are i.i.d. and distributed as the generic random variable R. The random set Ξ given by (3.3) is called the homogeneous BM with random spherical grains. Note that condition (3.2) is equivalent to E[Rd] &lt; ∞, which is always assumed. Figure 3.1 shows a realization of a BM with random spherical grains in dimension 2.

We now study some basic characteristics of the BM.

### 3.1.1 Capacity Functional

The capacity functional plays for RACs a role analogous to that of the (cumulative) distribution function for random variables. It is a key characteristic of a RAC that uniquely defines its distribution.

Fig. 3.1 Boolean Model with random spherical grains.

<!-- p:77 -->


Definition 3.2. Let 三 be a RAC. The capacity functional T=(K) of 三 is defined as

$$T _ { \Xi } ( K ) = P \{ \Xi \cap K \neq \emptyset \}$$

for all compacts K ⊂ Rd.

Remark. Obviously, we have T=(∅) = 0 and in general 0 ≤ T=(K) ≤ 1. These properties can be seen as analogous to the properties F(-∞) = 0,0 ≤ F(x) ≤ 1 of a distribution function F of a random variable. One can complete the above two properties by another couple of properties, analogous to monotonicity and right continuity of a distribution function, and then define a Choquet alternating capacity functional as any functional T(K) of the compact sets K satisfying the four conditions. A celebrated theorem of the theory of RACs (Choquet's theorem; see [29]) states that each such capacity functional uniquely defines some RAC distribution, exactly as each d.f. defines the distribution of a random variable.

Before calculating the capacity functional of the BM, we prove the following very useful lemma.

Lemma 3.1. Let ΞBM be the BM with intensity of germs Λ and the generic grain 三. Then, the number of grains of the BM intersecting a given compact K,

$$N _ { K } = \# \{ x _ { i } \colon ( x _ { i } + \Xi _ { i } ) \cap K \neq \emptyset \} \, ,$$

is a Poisson random variable with parameter E[Λ( ⊕ K)].

Proof. Let  be a marked Poisson p.p. generating the BM as in Definition 3.1. For a given compact K define the point process

$$\Phi _ { K } = \sum _ { ( x _ { i } , \Xi _ { i } ) \in \tilde { \Phi } } \varepsilon _ { x _ { i } } \mathbb { I } ( ( x _ { i } + \Xi _ { i } ) \cap K \neq \emptyset ) \, .$$

Note that ΦK is an independent thinning of the points of  (germs of the BM) with the thinning probability

$$p _ { K } ( x ) = \mathbf P \{ x + \Xi \cap K \neq \emptyset \} = \mathbf P \{ x \in \check { \Xi } \oplus K \} \, .$$


<!-- p:78 -->


By Proposition 1.8, ΦK is a Poisson p.p. with intensity measure pK(x)Λ(dx). Moreover, NK = ΦK(Rd) is a Poisson random variable with parameter ∫Rd pK(x) Λ(dx). By Fubini's theorem

$$\int _ { \mathbb { R } ^ { d } } p _ { K } ( x ) \, \Lambda ( d x ) & = \int _ { \mathbb { R } ^ { d } } P \{ x \in \check { \Xi } \oplus K \} \, \Lambda ( d x ) \\ & = E \left [ \int _ { \mathbb { R } ^ { d } } \mathbb { I } ( x \in \check { \Xi } \oplus K ) \, \Lambda ( d x ) \right ] \\ & = E [ \Lambda ( \check { \Xi } \oplus K ) ] \, ,$$

which completes the proof.

□

We can now calculate the capacity functional of the BM.

Proposition 3.2. The capacity functional of the BM ΞBM with intensity of germs Λ and the generic grain Ξ is equal to

$$T _ { \Xi _ { B M } } ( K ) = 1 - e ^ { - E [ \Lambda ( \check { \Xi } \oplus K ) ] } .$$

Proof. Note that T≡(K) = P{ NK ≠ 0}, where NK = #{xi: (xi + 三i) ∩ K ≠ Ø0}. The result follows from Lemma 3.1. □

### 3.1.2 Characteristics of the Homogeneous BM

Definition 3.3. We say that the BM EBM is homogeneous if the underlying Poisson p.p. Φ is stationary. The intensity of the latter, 0 &lt; λ &lt; ∞, is also called the intensity of the homogeneous BM.

Remark. Note that the distribution of the homogeneous BM is invariant with respect to any translation in Rd. Indeed, the homogeneity assumption implies that the capacity functional of EBM is translation invariant, i.e., T3BM(a + K) = T3BM(K) for any a ∈ Rd. This follows from Proposition 3.2 and the simple observation that | ⊕ (a + K)| = |a + (È ⊕ K)| = |È ⊕ K|, where |·| denotes Lebesgue measure (volume)


<!-- p:79 -->


in Rd. The fact that

$$T _ { \Xi _ { B M } } ( a + K ) & = P \{ \Xi _ { B M } \cap ( a + K ) \neq \emptyset \} \\ & = P \{ ( \Xi _ { B M } - a ) \cap K \neq \emptyset \} \\ & = T _ { \Xi _ { B M } - a } ( K )$$

and the remark after Definition 3.2 imply that the same holds true for the distribution of EBM.

In the sequel, we will define some important characteristics of a RAC whose distribution is invariant with respect to any translation in Rd (for short, we will speak of a translation invariant RAC) and evaluate these characteristics for the homogeneous BM.

Definition 3.4. (Volume fraction) The volume fraction p of the translation invariant RAC 三 is defined as the mean fraction of the volume occupied by 三

$$p = \frac { E [ | \Xi \cap B | ] } { | B | }$$

for |B| &gt; 0, which, by translation invariance of Ξ, can be shown not to depend on the particular choice of bounded B.

Remark. Due to the translation invariance of the RAC, the volume fria d r  tan ri  s d  oe oe rso the origin) is covered by 三. Indeed

$$i s \ c o v e r e d \ b y \coloneqq & \text {Indeed} \\ p & = \frac { E [ | \Xi \cap B | ] } { | B | } \\ & = \frac { 1 } { | B | } \int _ { B } E [ 1 ( x \in \Xi ) ] d x \\ & = P \{ 0 \in \Xi \} = P \{ \Xi \cap \{ 0 \} \neq \emptyset \} \\ & = T _ { \Xi } ( \{ 0 \} ) , \\ \intertext { o t h i n g } b y \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text$$

which is nothing but the capacity functional of 三 evaluated on a singleton.


<!-- p:80 -->


By the above remark and Proposition 3.2, we immediately obtain that:

Corollary 3.3. The homogeneous BM with intensity λ and generic grain 三 has the volume fraction

$$p = 1 - e ^ { - \lambda E [ | \Xi | ] } .$$

Definition 3.5. (Covariance function) The covariance function C(x) of the translation invariant RAC EBM is defined as the probability that two points separated by the vector x ∈ Rd belong to ΞBM, i.e., by

$$C ( x ) = P \{ 0 \in \Xi _ { B M } , x \in \Xi _ { B M } \} \, .$$

This definition can be extended to any translation invariant RAC.

Note that C(x) = E[1(0 ∈ 三)1(x ∈ 三)], so it is a "non-centered" covariance of the random variables 1(0 ∈ 三) and 1(x ∈ 三); the "true" τd − (x) = (( ∃ 0)d) − (x)  n s eo )

If the distribution of the RAC Ξ is invariant with respect to all translations and rotations in Rd then C(x) depends only on |x|. In this case, we will write C(x) = C(|x|), with a slight abuse of notation.

Corollary 3.4. The covariance function of the homogeneous BM with intensity λ and the generic grain 三 is equal to

$$C ( x ) = 2 p - 1 + ( 1 - p ) ^ { 2 } e ^ { \lambda E [ | \Xi \cap ( \Xi - x ) | ] } .$$

Proof. We write

```
ProObJ:  We write

C(x) = P{0 \in E \cap (E - x) }

= P{0 \in E} + P{x \in E} - P{0 \in E \cup (E - x) }

= 2p - P{0 \in E \cup (E - x) }

= 2p - P{E \cap {0,x} } \neq \emptyset

= 2p - T_{(0,x)}

```


<!-- p:81 -->


$$& = 2 p - 1 + e ^ { - \lambda E [ | \check { \Xi } \oplus \{ 0 , x \} | ] } \\ & = 2 p - 1 + e ^ { - \lambda E [ | \Xi | + | \Xi - x | - | \Xi \cap ( \Xi - x ) | ] } \\ & = 2 p - 1 + ( 1 - p ) ^ { 2 } e ^ { \lambda E [ | \Xi \cap ( \Xi - x ) | ] } ,$$

which completes the proof.

□

Definition 3.6(Contact distribution function). Consider a translation invariant RAC 三. Let B be a given bounded convex set containing the origin, i.e., 0 ∈ B. The contact distribution function (CDF) HB(r) of Ξ with respect to the test set B is defined as the conditional probability that the dilation of the set B by the factor r is included in the complement 三c = Rd \ 三 of the RAC 三 given 0 ∈ 3c, i.e.,

$$H _ { B } ( r ) = P \{ r B \subset \Xi ^ { c } | 0 \in \Xi ^ { c } \} = \frac { P \{ \Xi \cap r B = \emptyset \} } { 1 - p } , \ \ r \geq 0 \, ,$$

where p is the volume fraction of 三.

Different instances of contact distribution functions can be considered, depending on the choice of the test set B. The most popular cases are as follows:

- The spherical CDF. This is the case when B = B0(1); in this case the CDF HB0(1)(r) is the conditional distribution function of the distance from 0 to 三 given 0 ∉ 三; see Figure 3.2.
- The linear CDF. This case arises when B = [0, v], a segment from the origin with direction v ∈ Rd, |v| = 1; in this case the CDF H[o,v](r) is the conditional distribution function of the distance from 0 to 三 in the direction of the vector v, given 0 ∉三. If 三 is invariant with respect to rotations, then the linear CDF does not depend on the direction v and H[o,v](r) = H(r) can be seen as the conditional distribution function of the distance from the origin to 三 in a randomly chosen direction; see Figure 3.2.

Note that the CDF can be expressed in terms of the capacity functional. In particular, the CDF of the homogeneous BM can be evaluated using Proposition 3.2.


<!-- p:82 -->


Fig. 3.2 The radius of the smallest sphere centered at 0 and intersecting the BM and the shortest segment joining 0 with the BM in the direction of (-1,0). The conditional distribution functions of the radius of the sphere and the length of the segment, given 0 is not covered by the BM, are called, respectively, the spherical and linear contact distribution functions.

●

Definition 3.7.(Coverage probability) The coverage probability of the compact set K by a RAC E (not necessarily translation invariant) is defined as the probability that K is included in 三, i.e. as P{K ⊂ 三}.

The coverage probability is, in general, difficult to evaluate. Obviously

$$P \{ K \subset \Xi \} \leq T _ { \Xi } ( K )$$

and equality holds for a singleton K = {x}.

More explicit results can be obtained for some hard-core germ-grain models, in which points ("germs") of some point process are centroids of some non-intersecting closed sets ("grains"); c.f. e.g., the Matérn model in Example 2.1.3. For such models, for any connected K, the event {K ⊂ E} is equal to the event that K is entirely contained in one of the grains.

For the BM, the following easy result holds.


<!-- p:83 -->


Proposition 3.5. Let ΞBM be the BM given by (3.3) driven by a stationary Poisson p.p. with intensity 0 &lt; λ &lt; ∞ and with typical grain 三. The random set EBM covers any given subset K ⊆ Rd of non-null ∞ = |   on   &lt; || wo os-−

Proof. Assume that the BM covers K for all K with positive volume. Then, by Definition 3.4, its volume fraction is p = 1. Using the explicit formula given in Corollary 3.3, one finds that necessarily E[[三|] = ∞.

Conversely, if the latter is true, we have p = 1 and consequently the d-dimensional volume of the complement of the BM, Rd \ 三BM is almost surely null. In order to conclude that 三BM covers all K as above, we show that EBM = Rd. For this consider the following €-dilation 三BM(€) = ∪i(xi + (三i ⊕ B0(€))) of 三BM, and note that |Rd \ 三BM| = 0 nmpn ooo     r s p =   ce

$$P \{ \Xi _ { B M } = \mathbb { R } ^ { d } \} = \lim _ { \epsilon \to 0 } P \{ \Xi _ { B M } ( \epsilon ) = \mathbb { R } ^ { d } \} = 1 \, ,$$

which completes the proof.

□

More informative results for the coverage of the BM are known only in asymptotic form. In this regard, consider the following parametric family of homogeneous BMs on the plane R2 with spherical grains with random radius R of finite second moment (cf. Example 3.2).

$$\Xi _ { B M } ( r ) = \bigcup _ { i } \left ( x _ { i } + B _ { 0 } ( r R _ { i } ) \right ) .$$

Proposition 3.6. Let K be a compact set in R2 whose boundary ∂K has zero 2-D Lebesgue measure, i.e., |∂K| = 0. Consider the family of BMs (3.4) with intensity of germs λ and assume that E[R2+€] &lt; ∞ for some ∈ &gt; 0. Denote

$$\phi ( \lambda , r ) = \pi r ^ { 2 } \lambda E [ R ^ { 2 } ] - \log \frac { | K | } { \pi r ^ { 2 } E [ R ^ { 2 } ] } - 2 \log \log \frac { | K | } { \pi r ^ { 2 } E [ R ^ { 2 } ] } - \log \frac { E [ R ] ^ { 2 } } { E [ R ^ { 2 } ] } \, .$$

1 Strictly speaking, in this case, the set 3BM is no longer a BM since the condition E[|3|] &lt; ∞ is not satisfied; cf. condition (3.2).


<!-- p:84 -->


Then

$$P \{ K \subset E _ { B M } ( r ) \} & = \exp [ - e ^ { - \phi ( \lambda , r ) } ] + o ( 1 ) , \quad \text {as } \lambda \to \infty , r \to 0 , \ \ ( 3 . 5 ) \\ \underline { \text {provided } } \phi ( \lambda , r ) \text { tends to some limit } ( \text {possibly } \pm \infty ) .$$

The original proof of the above result (which is very technical and more general – dimension d ≥ 2, more general grains, and multiple coverage − can be found in [25, cf. Lemma 7.3].

Note that the above result gives approximations of the coverage probability for dense BMs with small grains. The following two particular parameterizations are of interest if one wants to design a BM with some given (approximate) probability of coverage of a given set K. The first one shows how many germs of a given size are needed, while the second one indicates how large grains should be if the density of germs is given.

Corollary 3.7. For a given u (−∞ &lt; u &lt; ∞) take

$$\lambda & = \lambda ( r ) \\ & = \frac { 1 } { \pi r ^ { 2 } E [ R ^ { 2 } ] } \left ( \log \frac { | K | } { \pi r ^ { 2 } E [ R ^ { 2 } ] } + 2 \log \log \frac { | K | } { \pi r ^ { 2 } E [ R ^ { 2 } ] } + \log \frac { E [ R ] ^ { 2 } } { E [ R ^ { 2 } ] } + u \right ) \\$$

or

$$r = r ( \lambda ) = \sqrt { \frac { \log \lambda + \log \log \lambda + \log ( | K | E [ R ] ^ { 2 } / E [ R ^ { 2 } ] ) + u } { \lambda \pi E [ R ^ { 2 } ] } } .$$

Then

$$P \{ K \subset \Xi \} = \exp [ - e ^ { - u } ] + o ( 1 )$$

as r → 0 or λ → ∞, respectively.

Proof. Note that (3.6) is a solution of the equality φ(λ,r) = u in λ while (3.7) implies φ(λ, r(λ)) → u when λ → ∞. The result follows from Proposition 3.6. □

The following bounds have been shown in [23, Theorem 3.11] in the case of the BM with grains of fixed (deterministic) radius.


<!-- p:85 -->


Proposition 3.8. Let ΞBM(r) be the homogeneous BM given by (3.4) with constant Ri ≡ 1 and intensity of grains λ. Let B = B0(1) denote the unit disc. Then

$$1 - \min \{ 1 , 3 ( 1 + \pi r ^ { 2 } \lambda ^ { 2 } ) e ^ { - \pi r ^ { 2 } \lambda } \} & < P \left \{ B \subset \bigcup _ { i \colon x _ { i } \in B } ( x _ { i } + \Xi _ { i } ) \right \} \\ & < 1 - \frac { 1 } { 2 0 } \min \{ 1 , ( 1 + \pi r ^ { 2 } \lambda ^ { 2 } ) e ^ { - \pi r ^ { 2 } \lambda } \} .$$

$$\overline { 2 0 } ^ { 1 }$$

Note that the above result gives bounds for the probability that the unit disc is included in the union of grains whose germs belong to this disc and not to the whole union 三BM.

The BM is often considered as a model for the total coverage obtained by a deployment of an irregular radio network. One can think of an access network, or a sensor network. Points denote locations of access points or sensors, whereas the grains model communication or sensing regions of the antennas. In this context, one can use level sets of the path-loss function (see Section 2.3.1) as these grains.

## 3.2 Boolean Model as a Connectivity Model

One says that two nodes xi and xj of the BM at (3.3) are connected if (xi + 三i) ∩ (xj + 三j) ≠ ∅.

The random geometric graph is the graph associated by Boolean connectivity: its nodes are the points of the point process and there is an edge between two nodes if they are connected.

Continuum percolation (also referred to as Boolean percolation) is about the existence of infinite connected components of the BM (or equivalently infinite components in the random geometric graph).

In this section, we restrict our attention to a BM with spherical grains.

### 3.2.1 Connectivity in a Compact Set

Definition 3.8 (Connectivity in a finite window). Given a compa   t   s  et  tt e s t ts tet Ui:xi∈K (xi + 三i) is connected.


<!-- p:86 -->


Only an asymptotic result is known for the probability of the above event in the case of the BM with spherical grains all of the same constant radius.

Proposition 3.9. Let K be a square in R2 and consider the parametric family of BMs ΞBM(r) on R2 given by (3.4) with constant Ri ≡ 1 and intensity λ. Let φ(λ, r) = 4πr2λ/|K| − log λ. Then

$$P \{ \Xi _ { B M } ( r ) \text { is connected in the square } K \} \\ = \exp [ - e ^ { - \phi ( \lambda , r ) } ] + o ( 1 ) \quad \text {as } \lambda \to \infty , r \to 0 \, ,$$

provided φ(λ, r) tends to some limit (possibly ±∞).

Proof. We use Proposition 13.4 concerning the Minimal Spanning Tree (MST) of the Poisson p.p. (see Chapter 13). The key observation is that EBM(r) percolates in the square K iff the longest edge MK of the minimal spanning tree of Φ ∩ K is not longer than 2r, which is equivalent to

$$\lambda \pi M _ { K } ^ { 2 } - \log \lambda \leq 4 \lambda \pi r ^ { 2 } - \log \lambda .$$

Scaling down the radius of the grains and the side of the square K by the factor √|K|, we obtain

$$\lambda \pi M ^ { 2 } - \log \lambda \leq 4 \lambda \pi r ^ { 2 } / | K | - \log \lambda \, ,$$

where M is the longest edge of the MST of Φ in the unit square. The result now follows from Proposition 13.4. □

Corollary 3.10. For a given u (−∞ &lt; u &lt; ∞) take

$$\lambda = \lambda ( r ) = \frac { | K | } { 4 \pi r ^ { 2 } } \left ( \log \frac { | K | } { 4 \pi r ^ { 2 } } + \log \log \frac { | K | } { 4 \pi r ^ { 2 } } + u \right )$$

or

$$r = r ( \lambda ) = \sqrt { \frac { | K | ( \log \lambda + u ) } { 4 \lambda \pi } } \, .$$


<!-- p:87 -->


Then

P{三BM(r) is connected in the square K } = exp[−e−u] + o(1) as r → 0 or λ → ∞, respectively.

Proof. Note that (3.10) is a solution of the equation φ(λ, r) = u with unknown λ, while (3.9) implies φ(λ(r), r) → u when r → 0. The result follows from Proposition 3.6. □

### 3.2.2 Percolation in Rd

In this section, we restrict our attention to homogeneous BMs with spherical grains of random radius R (cf. Example 3.2). Assume that E[Rd] &lt; ∞. With probability 1 the BM with spherical grains (3.4) is not connected in Rd. In fact, one can prove the following stronger fact. Denote by νd the volume of a unit-radius ball in Rd. Denote by B0(R0) the grain (ball) centered at 0 under the Palm probability P0 (call it a "typical grain"; cf. Section 2.1.2).

Proposition 3.11. Consider the homogeneous BM EBM in Rd given by (3.4), with r = 1 and intensity λ. Assume that E[Rd] &lt; ∞. Then

- the probability that a typical grain is isolated is equal to

$$P ^ { 0 } \Big \{ B _ { 0 } ( R _ { 0 } ) \cap \bigcup _ { x _ { i } \neq 0 } ( x _ { i } + B _ { 0 } ( R _ { i } ) ) & = \emptyset \Big \} \\ & = E [ e ^ { - \lambda \nu _ { d } \sum _ { k = 0 } ^ { d } ( \binom { d } { k } R _ { 0 } ^ { d - k } E [ R ^ { k } ] } ] \, ,$$

and

- the number of isolated grains of ΞBM is infinite with probability 1.

Proof. Conditioning on the radius R0 = r of the typical grain B0(R0) located at the origin under P0, all other points whose grains are not disjoint from B0(r) form an independent thinning (cf. Section 1.3.2)


<!-- p:88 -->


of the marked p.p. ′ = Σi:|xi|≠0ε(xi,B0(Ri)). The retention probability for position xi and radius Ri is pr(xi, Ri) = P{r + Ri ≥ |xi| }. By Slivnyak's theorem (see Proposition 1.13), under P0, ' is homogeneous Poisson with intensity λ and by Proposition 1.8, the thinning is a non-homogeneous Poisson p.p. with intensity measure Λ such that

$$\Lambda ( \mathbb { R } ^ { d } ) & = \lambda \int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { R } ^ { + } } p _ { r } ( x , s ) \, d x \, F ( d s ) = \lambda \nu _ { d } \sum _ { k = 0 } ^ { d } \binom { d } { k } r ^ { d - k } E [ R ^ { k } ] \colon = \gamma ( r ) , \\$$

where F is the distribution of R. Consequently, the probability that B0(r) is isolated is equal to e−γ(r) and (3.11) follows when deconditioning with respect to the radius R0 = r.

In order to prove the second statement, denote by N = N() the number of isolated grains of the BM ΞBM, where  is a Poisson p.p. that generates EBM (cf. Definition 3.1). By the ergodicity of the homogeneous Poisson p.p. (this is easily extended to i.m. Poisson p.p.s; cf. proof of Proposition 1.21), it follows from Proposition 1.22 (4) that N is almost surely constant. In what follows, we show that N is not bounded, implying N = ∞ almost surely. Indeed, by Campbell's formula (1.19) and (3.11) we have

$$E [ N ( \Phi ) ] = \lambda \int _ { \mathbb { R } ^ { d } } P ^ { 0 } \{ \, B _ { 0 } ( R _ { 0 } ) \, \text { is isolated set } \} d x = \infty \, , \\$$

which implies that N cannot be bounded.

□

Remark. From the above considerations it should be clear that even very "strange" but possible (i.e., of positive probability) local configurations of points of the Poisson p.p. can be observed infinitely many times in the whole pattern.

We now continue on percolation, which, in view of what was said, cannot be reasonably defined as a total connectivity of EBM.

Definition 3.9. The BM percolates on Rd if there exists an infinite connected component of 三BM.

Just as with isolated grains, one is also interested in the event that, under the Palm distribution, the typical grain B0(R0) belongs to an infinite component.


<!-- p:89 -->


Remark. By "infinite component" we understand a component which consists of an infinite number (#) of grains. Note that such an infinite component is almost surely an unbounded set in the sense that it is not contained in any bounded window, because the number of grains visible in a compact window is a.s. finite (as a consequence of E[Rd] &lt; ∞, cf. Lemma 3.1). Denote by C the maximal (in the sense of inclusion) connected subset of 三BM which includes B0(R0). We call C the clump.

Let our homogeneous BM with spherical grains (see Example 3.2) be parameterized by the intensity λ of the stationary Poisson p.p. Denote by λc the following "critical" intensity

$$\lambda _ { c } = \inf \left \{ \lambda \geq 0 \colon \text {P} _ { \lambda } ^ { 0 } \{ \# C = \infty \} > 0 \right \} ,$$

where #C denotes the number of grains in the clump C and the notagrains λ.

Remark. Note that the probability Pλ{ #C = ∞ } is increasing in λ. This can be easily seen using the results on thinning and superposition of Poisson p.p.s (see Section 1.3). Consequently, P0{ #C = ∞ } = 0 for all 0 ≤ λ &lt; λc (which might be the empty set if λc = 0).

One of the central questions of percolation theory for BMs concerns the non-degeneracy of λc (which here means 0 &lt; λc &lt; ∞). The following "phase transition" type results are known on the matter.

Proposition 3.12. Let λc be the critical intensity (3.12) of the family of BMs with spherical grains of random radius R.

- If d ≥ 2 and P{R0 = 0 } &lt; 1 (i.e., if R is not almost surely equal to 0), then λc &lt; ∞.
- If E[R2d−1] &lt; ∞, then λc &gt; 0.

Remark. For a one-dimensional BM with E[R] &lt; ∞, we have λc = ∞ (i.e., #C is almost surely finite for all λ), while if E[R] = ∞ we have λc = 0: the BM covers the whole line for any λ &gt; 0.2

2Strictly speaking in this case it is no longer a BM, for which E[R] &lt; ∞ is required; cf. Example 3.2.


<!-- p:90 -->


Proof. The proof of the finiteness of the critical intensity exploits some discretization and known results for discrete site percolation (cf. Section 14.2). Namely, consider some constants η &gt; 0 and p0 &gt; 0, such that P{ R ≥ η } = p0 &gt; 0; such positive constants exist under the assumption P{ R0 = 0 } &lt; 1. Consider a square lattice (in Rd) with side of length η/(2d√d). Note that this value is chosen so that any two balls of radius not less than η, centered at some points of any two adjacent sites of the lattice, are not disjoint. We declare a site of the lattice open if there is a point of  in it marked with a ball of radius R ≥ η. Otherwise, we declare the site closed. Note that the probability p = p(λ) for a given site to be open is positive and tends to 1 when λ → ∞. Moreover, the sites are declared open independently. It is known that in this discrete model with p large enough, but still p &lt; 1, the origin belongs to an infinite connected set of opened sites with a positive probability; see Proposition 14.5. By the construction of our discrete model, this implies that B0(R0) belongs to an infinite connected component with non-null probability for λ large enough, thereby ensuring that λc &lt; ∞.

In order to prove that λc &gt; 0, consider the following generations of grains connected to B0(R0). The first generation consists of all the grains directly connected to it. Given n ≥ 1 generations, the (n + 1)st generation consists of all grains directly connected to some grain of the nth generation and which do not intersect any grain of generation −       ( + x    s   − Ri &lt; k (k = 1,2 ...). Note that the number of grains of type k of the (n + 1)th generation, directly connected to a given grain of type i of the nth generation, but not totally contained in it, is not larger than the number of all grains of radius R, k ≤ R &lt; k + 1 intersecting this given grain and not totally contained in it, which is in turn dominated by a Poisson random variable of parameter

$$\mu ( i , k ) & = E [ \# \{ \text {points of Poisson } p . p . \text { in } B _ { 0 } ( i + k ) \, \rangle \\ & = \lambda \nu _ { d } \left ( ( i + k ) ^ { d } - ( i - k ) _ { + } ^ { d } \right ) \text {P} \{ k \leq R < k + 1 \} \, .$$

The process of generations of grains connected to B0(R0) is not a branching process due to the dependence between generations; however it can be stochastically bounded by a multi-type branching (GaltonWatson) process with a Poisson number of children of type k born to a parent of type i; this Poisson number has mean μ(i, k). It is not diht h t squ  fo t dxce t ht ls t i ations of this branching process, given the root is of type i, is equal to n is the jkth entry of the nth power of jk the matrix {mik = μ(i, k)}. It is a matter of a direct calculation (see the details in [31, proof of Theorem 3.3]) that the (unconditional) expectation of the total number of individuals is finite for sufficiently small λ &gt; 0 provided E[R2d−1] &lt; ∞. □


<!-- p:91 -->


The critical intensity λc is related to the size of a clump generated by a typical grain under P0. The following result says that it is also critical for percolation as defined in Definition 3.9.

Proposition 3.13. Let λc be the critical intensity (3.12) of the family of BMs with spherical grains of random radius R.

- Assume λc &gt; 0. If 0 &lt; λ &lt; λc then Pλ{BM percolates } = 0.
- Assume λc &lt; ∞. If λc &lt; λ then Pλ{BM percolates } = 1.
- The number of infinite connected components is Pλ-almost surely constant and equal to 0 or 1.

Proof. Assume 0 &lt; λ &lt; λc. We have by the Campbell formula

$$P _ { \lambda } \{ B M \, p e r c o lates \} \\ \leq E _ { \lambda } \left [ \sum \mathbb { 1 } ( x _ { i } \oplus B _ { 0 } ( R _ { i } ) \, \text {belongs to an infinite component} ) \right ] \\ = \lambda \int _ { \mathbb { R } ^ { d } } P _ { \lambda } ^ { 0 } \{ \# C = \infty \} d x = 0 \, . \\ \text {By the periodicity of the homogeneous Poisson } p . n . \, ( \mathbf t a t { \, } c a n \, \text {be easily}$$

By the ergodicity of the homogeneous Poisson p.p. (that can be easily extended to independently marked Poisson p.p.; cf. proof of Proposition 1.21), it follows from Proposition 1.22 (4) that the number of infinite connected components is almost surely constant.


<!-- p:92 -->


Assume now that λc &lt; λ &lt; ∞. Note that the BM percolates iff the number N of grains which belong to an infinite component is not less tha     h  n n o   at Eλ[N] = ∞. Consequently, Pλ{N ≥ 1 } &gt; 0, which implies by ergodicity that Pλ{ N ≥ 1 } = Pλ{BM percolates } = 1.

Proving that the number of infinite connected components is at most 1 is trickier. The arguments are based on the ergodicity of the BM (see [31, Section 3.6]). □

Example 3.3 (Connectivity in ad hoc networks). Consider an ad hoc network. Following Example 1.1 we assume that the locations of the mobile nodes are modeled by some homogeneous Poisson p.p. Φ. Assume that two nodes xi, xj ∈ Φ can communicate directly with each other if |xi − xj| ≤ ∆, where ∆ is some constant communication range. This is equivalent to saying that these nodes are connected in the BM based on Φ and with spherical grains of radius r = ∆/2 (cf. the definition of connectivity at the beginning of Section 3.2). Assume that the nodes of this network can relay packets and that multihop routing is used. Then, nodes can communicate through some multihop route iff they belong to the same connected component of this BM.

A first question concerning the performance of this network concerns its connectivity. One can distinguish two scenarios:

- Limited network case. If we assume a bounded window K then, it makes sense to ask for the probability of full connectivity, i.e., the probability that any two nodes in the network can communicate with each other (through a multihop route). The results of Proposition 3.9 and its corollary can be used to approximate this probability if the node density λ is large (i.e., if there are very many nodes in K) and the communication range ∆ is small compared to (the side of the square) K.
- Large network case. For networks in a large domain, it is more appropriate to adopt a model based on the BM on the whole plane (or space). Then, in view of the negative result of Proposition 3.11, full connectivity cannot hold and


<!-- p:93 -->


the best one can hope for is that a node can communicate with an infinite number of nodes. In other words, the infinite ad hoc network is said to be "connected" if the corresponding BM percolates. Note that in this case, the BM has a unique infinite connected component (Proposition 3.13). The latter can be interpreted as the "main part" of the network.

We conclude from the above models that one can bring a disconnected (non-percolating) network to the percolation regime by increasing the density of nodes or by enlarging the communication range. We shall return to this problem in Chapter 8 where we show that this method for connecting a network does not always work when interference is taken into account.


<!-- p:94 -->


### Voronoi Tessellation

### 4.1Introduction

In this chapter, we introduce an important random tessellation of the Euclidean space Rd. By definition, a tessellation is a collection of open, pairwise disjoint polyhedra (polygons in the case of R2), the union of whose closures cover the space, and which is locally finite (i.e., the number of polyhedra intersecting any given compact set is finite).

Definition 4.1. Given a simple point measure μ on Rd and a point x ∈ Rd, the Voronoi cell Cx(μ) = Cx of the point x ∈ Rd w.r.t. μ is defined to be the set

$$\mathcal { C } _ { x } ( \mu ) = \{ y \in \mathbb { R } ^ { d } \colon | y - x | < \inf _ { x _ { i } \in \mu , x _ { i } \neq x } | y - x _ { i } | \} \, .$$

The Voronoi cell is often defined as the closure of the last set. Given a simple point process Φ = Σiεxi on Rd, the Voronoi Tessellation ( VT) or mosaic generated by Φ is defined to be the marked point process

$$\mathcal { V } = \sum _ { i } \varepsilon _ { ( x _ { i } , \mathcal { C } _ { x _ { i } } ( \Phi ) - x _ { i } ) } \, .$$


<!-- p:95 -->


Fig. 4.1 Voronoi tessellation generated by a random sample of points.

o

。

o

。

o

0

。


o


0


。

o


0

0%

o

。

9

o

The Voronoi cell Cx(μ) as defined above is an open set; it is often defined instead as the closure of this set. Observe that, with our definition, not every point in Rd is covered by some Voronoi cell: given two points xi and xj say of Φ that have Voronoi cells that abut each other, there are some points y that are common to the boundaries of both cells but are not in either (cf. Figure 4.1 which shows the Voronoi tessellation generated by some realization of a point process).

Note that the cell Cxi (Φ) of the atom xi is the set of all those points of Rd that are closer to this atom xi than to any other atom of Φ. Note also that we consider these cells {Cxi − xi} shifted to the origin as marks of the points {xi} of Φ. This extends slightly the concept of marked point processes considered in Section 2.

One can easily see that each Voronoi cell is a convex polyhedron, but it may be unbounded. It is not difficult to prove, by considering the typical cell Co(μ) under the Palm distribution, that in the case of a Voronoi tessellation generated by a homogeneous Poisson p.p., all cells are bounded with probability 1.

The Voronoi tessellation is an important model for the theory of point processes as well as for applications. In the remaining part of this chapter, we will show it "in action" in a few theoretical and more practical contexts.


<!-- p:96 -->


## 4.2 The Inverse Formula of Palm Calculus

In Section 1.6 (and in more detail in Chapter 10) we defined the PalmMatthes distribution P0 of a stationary point process Φ; it can be interpreted as the conditional distribution of Φ given Φ({0}) ≥ 1. We will now show how the stationary distribution P of Φ can be retrieved from P0using Voronoi cells.

Theorem 4.1. Let Φ be a simple stationary point process with intensity 0 &lt; λ &lt; ∞. For all non-negative functions f: M → R+,

$$E [ f ( \Phi ) ] = \lambda E ^ { 0 } \left [ \int _ { \mathbb { R } ^ { d } } f ( \Phi - x ) \mathbb { I } ( x \in \mathcal { C } _ { 0 } ( \Phi ) ) \, d x \right ] .$$

Proof. Let us take

$$h ( x , \Phi ) = 1 ( \Phi \left ( B _ { 0 } ^ { \circ } ( | x | ) \right ) = 0 ) ,$$

where Bx(r) = {y: |y − x| &lt; r } is the open ball of radius r centered at x. Let us take for granted the property (proved below in Lemma 4.2) that among the points of Φ, with probability 1 w.r.t. P, there is a unique point which is closest to the origin. Using this property, we can state that with probability 1,

$$\int _ { \mathbb { R } ^ { d } } h ( x , \Phi ) \, \Phi ( d x ) = 1 \, ,$$

and consequently by the Campbell–Matthes formula (1.19) (see also Section 10.2.2),

$$Section 1 0 . 2 . 2 ) , \\ E [ f ( \Phi ) ] & = E \left [ \int _ { \mathbb { R } ^ { d } } f ( \Phi + x - x ) h ( x , \Phi + x - x ) \, \Phi ( d x ) \right ] \\ & = \lambda \int _ { \mathbb { R } ^ { d } } E ^ { 0 } [ f ( \Phi + x ) h ( x , \Phi + x ) ] \, d x \\ & = \lambda \int _ { \mathbb { R } ^ { d } } E ^ { 0 } [ f ( \Phi - x ) h ( - x , \Phi + x ) ] \, d x \\ & = \lambda E ^ { 0 } \left [ \int _ { \mathbb { R } ^ { d } } f ( \Phi - x ) \mathbb { I } ( x \in \mathcal { C } _ { 0 } ( \Phi ) ) \, d x \right ] . \quad \square$$


<!-- p:97 -->


It remains to prove:

Lemma 4.2. For a simple stationary non-null point process Φ

P{there exist two or more distinct points

equidistant to the origin 0 } = 0.

Proof.

P{there exist two or more distinct points equidistant to the origin}

$$P \{ t h e r e s i s t w o r m o r d i n t p o r i n t o w i d i s t a n t o t h e o r i g n u r \} \\ & \leq E \left [ \int _ { \mathbb { R } ^ { d } } 1 ( \Phi ( \{ y \ne x \colon | y | = | x | \} ) \geq 1 ) \, \Phi ( d x ) \right ] \\ & \leq E \left [ \int _ { \mathbb { R } ^ { d } } 1 ( ( \Phi - x ) ( \{ y ^ { \prime } \ne 0 \colon | y ^ { \prime } + x | = | x | \} ) \geq 1 ) \, \Phi ( d x ) \right ] \\ & = \lambda E ^ { 0 } \left [ \int _ { \mathbb { R } ^ { d } } 1 ( \Phi ( \{ y ^ { \prime } \ne 0 \colon | y ^ { \prime } + x | = | x | \} ) \geq 1 ) \, d x \right ] \\ & \leq \lambda E ^ { 0 } \left [ \int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { R } ^ { d } \langle \{ 0 \} } 1 ( | y ^ { \prime } + x | - | x | ) \, \Phi ( d y ^ { \prime } ) \, d x \right ] \\ & = \lambda E ^ { 0 } \left [ \int _ { \mathbb { R } ^ { d } \langle \{ 0 \} } \| \{ x \colon | y ^ { \prime } + x | = | x | \} \| \, \Phi ( d y ^ { \prime } ) \right ] = 0 , \\ \text {where } \| \cdot \| \detotes the d \text {-dimensional volume.} \quad \square$$

where ∥· ∥ denotes the d-dimensional volume.

□

Let us now take f ≡ 1; this yields the following formula, which determines the mean value of the volume of the typical cell:

### Corollary 4.3.

$$1 = \lambda E ^ { 0 } [ | \mathcal { C } _ { 0 } ( \Phi ) | ] .$$

There are no closed form expressions for the distribution of the volume of the typical cell except for dimension 1.

Let us call now C(0,Φ) the cell of the stationary tessellation V that covers the origin (i.e., 0 ∈ C(0, Φ)). In view of Lemma 4.2, C(0, Φ) is uniquely defined for almost all realizations of Φ w.r.t. P. Let us take f = g(C(0, Φ)) if C(0, Φ) is unique and 0 if not, where g is some non-negative function of C(0, Φ) (e.g., its volume, perimeter, number of sides, etc.). We obtain the following corollary.


<!-- p:98 -->


### Corollary 4.4.

In particular,

$$E \left [ \frac { 1 } { | C ( 0 , \Phi ) | } \right ] = \frac { 1 } { E ^ { 0 } [ | \mathcal { C } _ { 0 } ( \Phi ) | ] } \, .$$

By Jensen's inequality, one obtains the following result that can be seen as yet another incarnation of the waiting time paradox (see [14], Vol. 2)

$$E [ | C ( 0 , \Phi ) | ] \geq E ^ { 0 } [ | ( \mathcal { C } _ { 0 } ( \Phi ) | ] \, .$$

This paradox is explained by the fact that the cell which covers the origin is sampled with some bias with respect to the distribution of the typical cell C0(Φ) under P0, namely, this sampling favors large cells (as having more chance to cover a given fixed point). For more on this bias, see e.g., [33].

The next example shows how Theorem 4.1 can be used to construct a stationary periodic point process.

Example 4.1 (Stationarization of the honeycomb). Consider a regular hexagonal grid on R2 with the distance ∆ between two adjacent vertexes of this grid. (The set of vertexes of this grid can be described on the complex plane by Hex = {∆(u1 + u2eiπ/3), u = (u1, u2) ∈ {0, ±1, . ..}2}). Consider a (deterministic) point process ΦHex whose points are located on this grid. Consider this deterministic scenario as the Palm distribution P0 of some stationary point process. Note that the surface area of the typical cell (hexagon) of this process is equal to ∆2/(2π√3). Thus its intensity is λHex = 2π√3/∆2. By Theorem 4.1, the stationary version of this periodic p.p. can be constructed by randomly shifting the deterministic pattern Hex through a

$$\mathbf E [ g ( C ( 0 , \Phi ) ) ] = \lambda \mathbf E ^ { 0 } [ g ( \mathcal { C } _ { 0 } ( \Phi ) ) | \mathcal { C } _ { 0 } ( \Phi ) | ] \, .$$


<!-- p:99 -->


vector uniformly distributed in the Voronoi cell (hexagon) of the origin. The Voronoi tessellation generated by this (Palm or stationary) p.p. is sometimes called the honeycomb model.

## 4.3 The Neveu Exchange Formula

In this section, we will prove another useful formula of the Palm calculus connecting the Palm distributions of two stationary point processes. Again, the Voronoi tessellation will be used as a tool. The formalism for Palm probabilities is that defined in Remark 10.1 which allows one to define several Palm probabilities on a common probability space that carries several point processes. The key tool is again the CampbellMatthes formula that in the case of two stationary (not necessarily independent!) point processes has the following incarnation

$$E \left [ \int _ { \mathbb { R } ^ { d } } g ( x , \Phi - x , \Phi ^ { \prime } - x ) \, \Phi ( d x ) \right ] = \lambda \int _ { \mathbb { R } ^ { d } } E ^ { 0 } [ g ( x , \Phi , \Phi ^ { \prime } ) ] \, d x , \quad ( 4 . 1 )$$

where λ &lt; ∞ is the intensity of Φ and E0 is the expectation with respect to its Palm probability P0; i.e., in particular, P0{Φ({0}) ≥ 1 } = 1.

Theorem 4.5 (Exchange formula). Let Φ and Φ' be two simple stationary point processes (defined on the same probability space) with intensity, respectively, 0 &lt; λ &lt; ∞ and 0 &lt; λ' &lt; ∞. Let E0 and E0, Φ′ denote the Palm-Matthes probabilities of Φ and Φ', respectively. If

$$E _ { \Phi ^ { \prime } } ^ { 0 } \left [ \Phi ( \partial \mathcal { C } _ { 0 } ( \Phi ^ { \prime } ) ) \right ] = 0 ,$$

wohnt n-tr r   n  nt  onton f(φ, φ′) of the point measures (φ, φ′) we have

$$\lambda E _ { \Phi } ^ { 0 } \left [ f ( \Phi , \Phi ^ { \prime } ) \right ] = \lambda ^ { \prime } E _ { \Phi ^ { \prime } } ^ { 0 } \left [ \int _ { \mathbb { R } ^ { d } } f ( \Phi - x , \Phi ^ { \prime } - x ) \mathbb { I } ( x \in \mathcal { C } _ { 0 } ( \Phi ^ { \prime } ) ) \, \Phi ( d x ) \right ] .$$

Proof. It suffices to prove the formula for a bounded function, so in what follows we assume that sup f ≤ 1. For any x ∈ Rd let Fx = Fx(Φ, Φ′) = f(Φ − x, Φ′ − x). By the Campbell formula (4.1) (see also Section 10.2.2) and due to (4.2)


<!-- p:100 -->


$$\lambda ^ { 0 } _ { \Phi } [ f ( \Phi , \Phi ^ { \prime } ) ] & = E \left [ \int _ { [ 0 , 1 ] ^ { d } } F _ { x } \Phi ( d x ) \right ] \\ & = E \left [ \int _ { [ 0 , 1 ] ^ { d } } \Phi ^ { \prime } ( d y ) \int _ { \mathbb { R } ^ { d } } F _ { x } 1 ( x \in \mathcal { C } _ { y } ( \Phi ^ { \prime } ) ) \Phi ( d x ) \right ] + A - B , \\$$

where

Note first that

$$& = E \left [ \int _ { [ 0 , 1 ] ^ { d } } \Phi ^ { \prime } ( d y ) \int _ { \mathbb { R } ^ { d } } F _ { x } 1 ( x - y \in \mathcal { C } _ { y - y } ( \Phi ^ { \prime } - y ) \\ & = E \left [ \int _ { [ 0 , 1 ] ^ { d } } \Phi ^ { \prime } ( d y ) \int _ { \mathbb { R } ^ { d } } F _ { x + y } 1 ( x \in \mathcal { C } _ { 0 } ( \Phi ^ { \prime } - y ) ) \\ & = \lambda ^ { \prime } E _ { \Phi ^ { \prime } } ^ { 0 } \int _ { \mathbb { R } ^ { d } } F _ { x } 1 ( x \in \mathcal { C } _ { 0 } ( \Phi ^ { \prime } ) ) \, \Phi ( d x ) \right ] .$$

In order to show that A − B = 0, knowing that A ≤ E[Φ([0, 1]d)] = λ &lt; ∞, it suffices to prove that A = B. For this, we consider a partition of Rd by hypercubes Rd = Uv(∆ + v), where ∆ = [0, 1]d and v runs over all vectors v = Σi=1 αiei, where αi ∈ Z, and ei are the unit vectors of the Euclidean base. We have

$$\sum _ { v \neq 0 } 1
 \sum _ { v \neq 0 } E O
$$

$$e ^ { \prime } ( d y ) \int _ { [ 0 , 1 ] ^ { d } } F _ { x } \mathbb { 1 } ( x \in \mathcal { C } _ { y } ( \Phi ^ { \prime } ) ) \, \Phi ( d x ) \Big ] , \\ y ) \int _ { \mathbb { R } ^ { d } \langle [ 0 , 1 ] ^ { d } } F _ { x } \mathbb { 1 } ( x \in \mathcal { C } _ { y } ( \Phi ^ { \prime } ) ) \, \Phi ( d x ) \Big ] .$$


<!-- p:101 -->


and for each v ≠ 0,

$$E \left [ \int _ { \Delta + v } \Phi ^ { \prime } ( d y ) \int _ { \Delta } F _ { x } 1 ( x \in \mathcal { C } _ { y } ( \Phi ^ { \prime } ) ) \, \Phi ( d x ) \right ] \\ = E \left [ \int _ { \Delta } ( \Phi ^ { \prime } - v ) ( d y ) \int _ { \Delta } F _ { x } 1 ( x \in \mathcal { C } _ { y + v } ( \Phi ^ { \prime } ) ) \, \Phi ( d x ) \right ] \\ = E \left [ \int _ { \Delta } ( \Phi ^ { \prime } - v ) ( d y ) \int _ { \Delta } F - x \, \mathbb { I } ( x \in \mathcal { C } _ { y } ( \Phi ^ { \prime } - v ) + v ) \, \Phi ( d x ) \right ] \\ = E \left [ \int _ { \Delta } ( \Phi ^ { \prime } - v ) ( d y ) \int _ { \Delta } F _ { x } 1 ( x - v \in \mathcal { C } _ { y } ( \Phi ^ { \prime } - v ) ) \, \Phi ( d x ) \right ] \\ = E \left [ \int _ { \Delta } ( \Phi ^ { \prime } - v ) ( d y ) \int _ { \Delta - v } F _ { x + v } 1 ( x \in \mathcal { C } _ { y } ( \Phi ^ { \prime } - v ) ) ( \Phi - v ) ( d x ) \right ] \\ = E \left [ \int _ { \Delta } ( \Phi ^ { \prime } ( d y ) \int _ { \Delta } F _ { x } 1 ( x \in \mathcal { C } _ { y } ( \Phi ^ { \prime } ) ) \, \Phi ( d x ) \right ] ,$$

where the last equality is due to the stationary of both point processes. Thus A = B, which concludes the proof. □

## 4.4 Neighbors in the Voronoi Tessellation, Delaunay Triangulation

Let Cx(μ) be the Voronoi cell of x ∈ Rd generated by the point pattern μ that is always assumed in this section to be simple (μ({z}) = 0 or 1). We will call any point y ∈ μ such that y ≠ x and |a − x| = |a − y| for some a ∈ Cx(μ), where Cx(μ) denotes the closure of Cx(μ), a Voronoi neighbor of x.

Definition 4.2. The Delaunay triangulation generated by a simple point measure μ is a graph with the set of vertices μ and edges connecting each y ∈ μ to any of its Voronoi neighbors.

Example 4.2 (Neighborhood in ad hoc networks). In a periodic (say hexagonal or square) grid, it is obvious to define the neighbors of a given vertex. However, for irregular patterns of points like a realization of a Poisson p.p., which we use below to model the set of nodes of ad hoc neta     n n ( n  ay triangulation offers some purely geometric definition of 'neighborhood' in such patterns.


<!-- p:102 -->


```
Define, for x \in \mathbb { R } ^ { d },
    \mathcal { N } _ { x } ( \mu ) = \{ y \in \mu \colon \mu ( B ( x , y , z ) ) = 0
                    for some z = \{ z _ { 1 } , \dots , z _ { d - 1 } \} \in \mu , \, x , y , \{ z _ { i } \} , \, \text {distinct} \} ,
```

where B(x, y, z) is the open ball circumscribed on the points x, y, {zi}. The following geometric result allows us to identify the Voronoi neighbors of x in μ or equivalently the edges from x in the Delaunay triangulation:

Lemma 4.6. Assume that Cx(μ) is bounded. Then, for x in μ, Nx(μ) coincides with the set of Voronoi neighbors of x.

Proof. Define a vertex of the cell Cx(μ) to be any location in z ∈ Rd equidistant to x and (at least) d − 1 other points y1, . . . , yd−1 ∈ μ. We use below the fact that if z is such a vertex, then each of the points y1, . . . , Yd−1 is a Voronoi neighbor of x.

If y ∈ μ belongs to Nx(μ), then by definition, there exists an empty open ball with x, y, z1, . . . , zd−1 on its boundary, where z1, . ., zd−1 ∈ μ. So, the center of this ball is a vertex of the cell Cx(μ) and therefore, y is a Voronoi neighbor of x.

Conversely, if y is a Voronoi neighbor of x, since the cell Cx(μ) is finite, its boundary contains a finite domain Dd1 included in the hyperplane of dimension d − 1 equidistant to x and y; the boundaries of Dd1 are finite domains contained in hyperplanes of dimension d — 2. Let Dd-2 be one of the latter. There exists a triple of points (x,y, z1) which are equidistant to any element of the Dd-2. More generally, for all 2 ≤ k ≤ d − 1, there exists a finite domain Dd−k included in some hyperplane of dimension d − k and such that all the elements of Dd−k -r    -       (-     x)   r ticular, there exists a location z of the boundary of Cx(μ) and points z1, . . , zd−1 ∈ μ such that z is equidistant to x, y and z1, . . . , zd−1. That is y ∈ Nx(μ). □


<!-- p:103 -->


The open ball centered at a vertex of Cx(μ) and having x on its boundary is empty of points of μ. The union of these balls over all vertexes of the cell is called the fundamental region (or the Voronoi flower) of the cell Cx(μ). It is easy to see that the Voronoi flower contains the Voronoi cell.

Proposition 4.7. Assume that Cx(μ) is bounded. Then the Voronoi flower of Cx(μ) is a random stopping set.

rt t  so n t r onn on  ot oaet vertexes of Cx(μ) with radii growing until they hit x or any of them hits the complement Kc of K. Use a similar argument as in Example 1.10. □

## 4.5 The Voronoi Tessellation Model for Cellular Access Networks

We give an example of VT based model of cellular access networks (see Section 25.3.2 in Volume II) which will be used later.

Example 4.3 (Cellular Access Network). The model components are as below:

- Users and Access Points located on the plane R2 are represented by two independent stationary point processes, denoted, respectively, by Φu and Φa.
- Each access point xi ∈ Φa serves users in a geographical zone which is modeled by its Voronoi cell Cxi(Φa). Note that this assumption is equivalent to the hypothesis that each user is served by the nearest access point.
- The model parameters are the intensities λu, λa of the p.p.s Φu, Φa, respectively. Typically λu &gt; λa, but this assumption is not essential for our analysis.

Consider now the following mean additive characteristic associated with the typical cell of the access network model:

$$\mathbf E _ { \Phi _ { a } } ^ { 0 } \left [ \int _ { \mathbb { R } ^ { 2 } } \mathbf 1 ( x \in \mathcal { C } _ { 0 } ( \Phi _ { a } ) ) g ( x , \Phi _ { a } ) \, \Phi _ { u } ( d x ) \right ] ,$$


<!-- p:104 -->


where E0 is the expectation w.r.t the Palm distribution of Φa and g Φa is a non-negative function of the location x ∈ R2 and the pattern Φa of access points. Taking different functions g, one gets the following examples of such additive characteristics:

- if g(x,φ) ≡ 1, then Ī =  represents the mean number of users in the typical cell;
- if g(x, φ) = |x|, then  ̄ =  ̄ is the mean total length of connections in this cell (which is more pertinent in a wired access network);
- if g(x, φ) = 1/l(|x|), where l(r) is some omni-directional pathloss function as considered in Example 23.3 in Volume II, then ī = P represents the mean total power received by the access point from all the users attached to it (assuming all users transmit with a constant power 1);
- if g(x, φ) = l(|x|) with l(·) as above, then ī = (PL) represents the mean total path-loss "received" at the access point from all the users it serves;
- if g(x, φ) = l(|x|) ∑yi∈φ1/l(|x − yi|) with l(·) as above, then I = (RPL) represents the mean total relative path-loss ratio "received" at the access point from all its users.

Let h(x, Φ) be defined as in the proof of Theorem 4.1 and take

$$f ( \Phi _ { u } , \Phi _ { a } ) = f ( \Phi _ { a } ) = \int _ { \mathbb { R } ^ { 2 } } g ( - y , \Phi _ { a } - y ) h ( y , \Phi _ { a } ) \, \Phi _ { a } ( d y ) \, .$$

Recall from the definition of h that f(Φa) = g(−Y*, Φa − Y*) where Y* = arg min{|yi|: y ∈ Φa} is the access point nearest to the origin (a.s. uniquely defined due to stationarity and the fact that the p.p. is simple). Moreover, on the set {Φa({0}) ≥ 1} for x ∈ C0(Φa) we have f(Φa − x) = g(x, Φa). Thus, by Neveu's exchange formula (Theorem 4.5) we obtain that

$$\bar { I } = \frac { \lambda _ { u } } { \lambda _ { a } } E _ { \Phi _ { u } } ^ { 0 } \left [ g ( - Y ^ { * } , \Phi _ { a } - Y ^ { * } ) \right ] .$$

We see that the Neveu exchange formula allows us to transform the "access-point centric" scenario into a dual "user-centric" scenario. This transformation shows that the mean number of users per access point (case g(x) ≡ 1) is equal to


<!-- p:105 -->


$$\bar { M } = \frac { \lambda _ { u } } { \lambda _ { a } } \, .$$

When Φa is a Poisson p.p. one can explicitly evaluate (4.3) for various types of additive characteristics. Under Poisson assumptions (for Φa r } = P0 {Φa(B0(r)) = 0 } = exp[−λaπr2], and it is not difficult to see that the argument ∠(Y*) is uniformly distributed on [0,2π). Moreover, given |Y*| = r, all points of Φa which are farther away from 0 than r form a non-homogeneous Poisson p.p. with intensity measure λa1(|y| &gt; r) dy (see Section 1.5). We denote this Poisson process by Φa|&gt;r. Consequently

$$\bar { I } = \frac { \lambda _ { u } } { \lambda _ { a } } \, \frac { 1 } { 2 \pi } \int _ { 0 } ^ { 2 \pi } \int _ { 0 } ^ { \infty } r E \left [ g ( ( r \cos \theta , r \sin \theta ) , \Phi _ { a } | _ { > r } ) \right ] e ^ { - \lambda _ { a } \pi r ^ { 2 } } \, d r \, d \theta .$$

For g(x, φ) = |x|, we obtain

$$\bar { L } = \frac { \lambda _ { a } } { 2 \lambda _ { c } ^ { 3 / 2 } } \, .$$

The mean received power P with l(r) given by OPL 1 or OPL 2 in Example 23.3 in Volume II can be given in terms of some special functions (note that for OPL 3, ī = ∞ due to the pole at the origin). The mean path-loss expression is explicit and, for OPL 3, it takes the form

$$\overline { ( P L ) } = \frac { \lambda _ { u } } { \lambda _ { a } } \, \frac { A ^ { \beta } \Gamma ( 1 + \beta / 2 ) } { ( \lambda _ { a } \pi ) ^ { \beta / 2 } } \, .$$

Under the same assumption, the mean relative path-loss is equal to

$$\overline { ( R P L ) } = \frac { \lambda _ { u } } { \lambda _ { a } } \frac { 2 } { \beta - 2 } \, .$$


<!-- p:106 -->


### Bibliographical Notes on Part I

Chapters 1 and 2 cover classical topics in point process theory. A classical reference on the matter is [9]. Most results are well known. The approach of Section 1.5 is borrowed from [46]. For more on hard-sphere packing problems mentioned in Example 2.1.3, see e.g., [8]. We did not find references for the discussion of Example 1.4 but it is likely that these simple observations were already made.

Shot noise processes and Boolean models as considered in Chapters 2 and 3 respectively, are core topics in stochastic geometry. For a comprehensive treatise on the matter, see [42]. For an analysis of the tail behavior of Shot Noise fields, the reader might consult [17]. For a history on the use of Shot Noise fields to represent interference, see the introductory paper of [22]. We did not find earlier papers on the joint distribution of the time-space SN proposed in Section 2.3.4.

For the class of random tessellations discussed in Chapter 4, the reader could consult [33]. For a general book on tessellations, see [34]. The models of Section 4.5 come from [3] and [2]. For a recent survey on the matter, see [47].

Point processes and stochastic geometry models are widely used in spatial statistics; see, e.g., [24] for a recent book on this subject.


<!-- p:107 -->


Part II

Signal-to-Interference Ratio Stochastic Geometry This part bears on stochastic geometry models defined by SINR. More precisely, we define and analyze a random coverage process of the d-dimensional Euclidean space which stems from the wireless communication setting described in Part VI in Volume II. As for the Boolean model, the minimal stochastic setting consists of a point process on this Euclidean space and a sequence of real-valued random variables considered as marks of this point process. In this coverage process, the cell attached to a point is defined as the region of the space where the effect/response of the mark of this point exceeds an affine function of the shot-noise process associated with the other points of the marked point process.


<!-- p:108 -->


Chapter 5 describes the typical cell: its volume, its shape, etc. Chapter 6 focuses on the interaction between cells within this setting. Chapter 7 studies the coverage process created by the collection of SINR cells. Finally, Chapter 8 studies the connectivity of this coverage process and in particular the conditions under which it percolates.


<!-- p:109 -->


5

### Signal-to-Interference Ratio Cells

## 5.1 Introduction

Let  = Σiε(xi,mi) be a marked point process, with points {xi} in Rd and marks {mi} in Rl. Consider a scalar shot-noise field Iδ(y) defined on the same space as  (i.e. on Rd), and generated by  and by the response function L: Rd × Rd × Re → R+ (cf. Section 2.2). Let w(y) ≥ 0 be some external or thermal noise field.

Definition 5.1. We define the Signal to Interference and Noise Ratio (SINR) cell of point (X, M) for threshold t ≥ 0 as

$$C _ { ( X , M ) } = C _ { ( X , M ) } ( \widetilde { \Phi } , w , t ) = \{ y \in \mathbb { R } ^ { d } \colon L ( y , X , M ) \geq t \left ( I _ { \widetilde { \Phi } } ( y ) + w ( y ) \right ) \} . \\$$

For more on the physical meaning of SINR, see Section 24.3.4 in Volume II.

Example 5.1. (Bit-rate level sets in interference and noise field) The simplest scenario is that where the mark of point X is the power P ∈ R+ emitted by the antenna located at X ∈ R2 and where L(y, x, P) = P/l(|x − y|), with l the mean omni-directional path-loss function (see Section 23.1.2 in Volume II). More general scenarios can be described with richer marks (such as antenna azimuth, fading, etc.). Other cases of interest are those where some interference and/or noise cancellation techniques are used. This results in models where the cell is defined with a more general affine function:


<!-- p:110 -->


$$C _ { ( X , M ) } = C _ { ( X , M ) } ( \widetilde { \Phi } , w , t ) = \{ y \in \mathbb { R } ^ { d } \colon L ( y , X , M ) \geq t \left ( \kappa I _ { \widetilde { \Phi } } ( y ) + \gamma w ( y ) \right ) \} \\ \\$$

where κ and γ are factors smaller than one (cf. Section 24.3.4 in Volume II where we discuss the case γ = 1 and κ small in Equation (24.20 in Volume II).

Then C(x,P) represents the set of locations y where the SINR of the channel from X to y is larger than the threshold t as illustrated by Figure 5.1.

Within the setting of Section 24.3.4 in Volume II, this translates into some bit-error probability, and consequently into some channel goodput. The exact relation between t and the bit-rate depends on particular modulation and coding used.

Fig. 5.1 Location y belongs to the cell C of point x because the SINR from x exceeds t at y. The cell C is the set of locations of the plane where a minimum bit rate can be guaranteed from transmitter x.

x5

t1

ux

x3

P/l(y−x)

x4

V

W

+

146)


<!-- p:111 -->


S            .1. Notice that the SINR cell C(x,P) is not always a convex set. In some cases it can even be not connected.

## 5.2 The Signal-to-Interference Ratio Cell is Well-Defined

There are two levels at which the definition of the SINR cell can be treated.

Firstly, recall from Section 2.2 that the shot-noise field with nonnegative response function is always well defined but may be infinite. At a second, more theoretical level, one may ask whether the SINR cell, which is a random set, is almost surely a closed set. This is a natural question in stochastic geometry, where the space of closed sets is a standard observation space for random objects. The following result, which immediately follows from Proposition 2.5 gives some sufficient conditions for this to hold.

Corollary 5.2. Let  be an i.m.p.p. Assume that the thermal noise w(y) has almost surely continuous trajectories. If L(y, x, m) is continuous in y and if for each y ∈ Rd, there exists a ball B(y, €y) such that (2.15) holds, then I(y) is almost surely finite and has continuous trajectories. Consequently the SINR cell C(x,M)(Φ, w,t) is a (random) closed set with probability 1.

## 5.3 Standard Stochastic Scenario and First Order Cell Characteristics

Following the assumptions of Section 2.3.1, we will often consider the following standard stochastic scenario for SINR cells:

- (1)  is a general stationary i.m.p.p. with points in R2 and intensity λ &gt; 0;
- (2) the marks pi have a distribution P{p ≤ s } = G(s) that does not depend on the location of the point;
- (3) The mark M = P of the point X generating the cell C(x,P) is independent of  and has also distribution function G.


<!-- p:112 -->


- (4) The thermal noise field w(y) = W is constant in space and equal everywhere to some non-negative random variable W ≥ 0 independent of  and P.

A slightly more general case is that where:

- (3') the mark M = P of the point X generating the cell C(x,P) is independent of Φ but has a different distribution function G' than the marks of the point process.

Remark. More general scenarios are considered in other chapters. For instance power control, studied in Chapter 19 in Volume II, requires powers which are dependent marks of the p.p.; similarly, the case of space and/or time dependent thermal noise is studied in Chapter 17 in Volume II.

Kendall-like Notation cont. Developing our previous Kendall-like notation for SN (see Section 2.3.1), we call the above scenario the GI model, where the GI in the numerator denotes a general disW+I tribution for P and the GI/GI in the denominator denotes the SN interference model. Special cases of distributions are deterministic (D) and exponential (M). We recall that M/· denotes an SN model with a Poisson point process.

This contains two important particular cases:

- The 0I GI model, which will be referred to as the interference limited model (since the thermal noise is not present);
- The 0+M GI model, where the interference is absent, and which will be referred to as the noise limited model, and which boils down to the Boolean (or to the conditional Boolean) model under natural assumptions on the attenuation function (see Section 5.5).

### 5.3.1 One Point Coverage Probability

Assume the standard SINR cell scenario of Section 5.3. We are interested in the probability that the SINR cell C(x,P) generated by a point located, say, at the origin X = 0, covers a given location y; i.e.,


<!-- p:113 -->


$$p _ { 0 } ( y ) = & \, P \left \{ \, y \in C _ { ( 0 , P ) } ( \widetilde { \Phi } , W , t ) \, \right \} = P \left \{ \, P \geq l ( | y | ) t ( W + I _ { \widetilde { \Phi } } ( y ) ) \, \right \} . \\ N _ { \widetilde { \Phi } } \, \ t h a t \, \ t i n g { \, w h a b i l i t } \, \text {in} \, \ t h a n \, w h a r w \, \ t h a t \, \ t h a n \, w h a r w \, \ t h a t \, \ t i n g { \, w h a r w } \right \} .$$

Note that this probability is the value of the capacity functional TC(o,P) ({y}) of the random (assume closed) set C(0,P) evaluated on the singleton {y} (cf. Definition 3.2).

Here is a general result for the W+GI/GI GI case.

Proposition 5.3. Assume the GI standard scenario of SecW+GI/GI tion 5.3 with condition (3') (i.e. P can have a distribution which differs from that of the marks of Φ). Assume the following:

- at least one of the random variables W, I or P has a Fourier transform which is square integrable;
- each of the random variables W, I and P has a finite first moment.

Let

$$\eta ( \xi ) & = E [ \exp ( - 2 i \pi \xi I _ { \widetilde { \phi } } ( y ) ) ] E [ \exp ( - 2 i \pi \xi W ) ] \\ & \quad \times E [ \exp ( - 2 i \pi \xi P / ( t l ( | y | ) ) ) ] \, .$$

Then

$$p _ { 0 } ( y ) = \frac { 1 } { 2 } - \frac { 1 } { 2 i \pi } \int _ { - \infty } ^ { \infty } \frac { \eta ( \xi ) } { \xi } \, d \xi ,$$

where the singular contour integral in the right-hand side, which has a pole at ξ = 0, is understood in the principal value sense; i.e., one has to calculate this integral over the domain (-∞, -€] ∪ [e, ∞) and then let ∈ decrease to 0.

Proof. Since X is the sum of independent random variables, it suffices that one of the terms of the sum has a density for X to have one. If this density has a square integrable Fourier transform, so does X. If all terms in the sum have finite first moments, so has X. The result follows from applying Corollary 12.4 in the Appendix to the density of the random variable X = P/(tl(|y|)) − W − Iδ(y). □


<!-- p:114 -->


The above proposition is useful when one knows the Fourier transform of the shot-noise Iγ. This is the case in particular for the M/GI SN; i.e, when  is an i.m. Poisson p.p. (and more generally some doubly stochastic Poisson process). Indeed, E[e−2iπξI] = LI, (2iπξ) and the Laplace transform L1 of the Poisson shot-noise is known in closed form (see Proposition 2.6 and Example 2.2).

Some sufficient conditions for IΦ(y) to have a density are given in Proposition 2.8.

There are several interesting cases where the shot-noise I has an infinite mean. Even in the M/GI SN case, this is the case when one adopts the OPL 3 attenuation model (see Remark 2.4 of Chapter 2). For such scenarios, the assumptions of the last proposition do not hold. We can then use the following result.

Proposition 5.4. Assume the GI standard scenario of SecW+GI/GI tion 5.3 with condition (3') (i.e. P can have a distribution which differs from that of the marks of ). Assume the following:

- at least one of the random variables W, I has density with a Fourier transform which is square integrable;
- the random variable P has density with a Fourier transform which is square integrable;
- the random variable P has a finite first moment.

Then

$$p _ { 0 } ( y ) & = \int _ { \mathbb { R } } \mathbf E \left [ \exp ( - 2 i \pi \xi I _ { \widetilde { \Phi } } ( y ) ) \right ] \mathbf E [ \exp ( - 2 i \pi \xi W ) ] \\ & \quad \times \frac { \mathbf E \left [ \exp ( - 2 i \pi \xi P / ( t l ( | y | ) ) ) \right ] - 1 } { 2 i \pi s } \, d s .$$

Proof. The proof follows immediately from Equation (5.3) above and Corollary 12.2 in the Appendix. □

Proposition 5.5. For the M

$$\text {on } 5 . 5 . \text {  For the } \frac { M } { W + G I / G \overline { I } } \text { model} \\ p _ { 0 } ( y ) = \mathcal { L } _ { W } \left ( \mu t l ( | y | ) \right ) \mathcal { L } _ { I _ { \overline { \Phi } } } \left ( \mu t l ( | y | ) \right ) ,$$

where Lw is the Laplace transform of W.


<!-- p:115 -->


Proof. We have

$$p _ { 0 } ( y ) & = P \{ P \geq t l ( | y | ) ( W + I _ { \widetilde { \Phi } } ) \} \\ & = \int _ { 0 } ^ { \infty } e ^ { - \mu u t l ( | y | ) } F _ { W + I _ { \widetilde { \Phi } } } ( d u ) \\ & = \mathcal { L } _ { W } \left ( \mu t l ( | y | ) \right ) \mathcal { L } _ { I _ { \widetilde { \Phi } } } \left ( \mu t l ( | y | ) \right ) ,$$

where the last equality relies on the fact that the Laplace transform of the sum of independent random variables is equal to the product of the Laplace transforms of the terms. □

Example 5.6. For M model with OPL 3 and W = 0, 0+M/M p0(y) = e−λ|y|2t2/βK, , where K = K(β) = (2πΓ(2/β)Γ(1 − 2/β))/β.

Example 5.7. Consider the PH model, where PH means that P W+GI/GI has the phase-type distribution PH(α, B, b). Recall that it is defined as the distribution of the time until absorption of the pure-jump Markov chain on the state space {0,1,...,b} with infinitesimal generator B (which is a (b + 1) × (b + 1)-matrix), where 0 is an absorbing state and where α is the vector describing the initial distribution on {1,...,b}. The tail-distribution function of P is known to be equal to

$$P \{ P \geq u \} = \alpha e ^ { u B } = \alpha \sum _ { n = 0 } ^ { \infty } \frac { u ^ { n } B ^ { n } } { n ! } ,$$

where eB is the matrix exponential defined by the corresponding power series. For this model, we have

$$p _ { 0 } ( y ) & = \int _ { 0 } ^ { \infty } P \{ P \geq t l ( | y | ) u \} P ( W + I = d u ) \\ & = \int _ { 0 } ^ { \infty } \alpha \sum _ { n = 0 } ^ { \infty } \frac { ( u t l ( | y | ) B ) ^ { n } } { n ! } P ( W + I = d u )$$


<!-- p:116 -->


$$& = \alpha \sum _ { n = 0 } ^ { \infty } \frac { ( t l ( | y | ) B ) ^ { n } } { n ! } \int _ { 0 } ^ { \infty } u ^ { n } P ( W + I = d u ) \\ & = \alpha \sum _ { n = 0 } ^ { \infty } \frac { ( t l ( | y | ) B ) ^ { n } } { n ! } E [ ( W + I ) ^ { n } ] . \\ \text {t} \text { for the } M / G \text { SN model, the moments of the shot-noise}$$

Note that for the M/G SN model, the moments of the shot-noise can be obtained from the closed form expression of the Laplace transform. Hence it is possible to evaluate (at least numerically) all terms of the above expansion.

### 5.3.2 Mean Cell Volume

The one-point coverage probability is related to the mean cell volume by the following simple relation:

$$v _ { 0 } \equiv E \left [ | C _ { ( 0 , P ) } | \right ] = E \left [ \int \mathfrak { 1 } ( y \in C _ { ( 0 , P ) } ) \, d y \right ] = \int p _ { 0 } ( y ) \, d y \, .$$

Example 5.8. For the M model with OPL 3 0+M/M

$$v _ { 0 } \equiv E [ | C _ { ( 0 , P ) } | ] = \frac { 1 } { \lambda t ^ { 2 / \beta } } \frac { \beta } { 2 \Gamma ( 2 / \beta ) \Gamma ( 1 - 2 / \beta ) } \, .$$

## 5.4 Fading in Signal-to-Interference Ratio Cell and Higher Order Characteristics

A simple higher order characteristic of a random closed set is its covariance function defined as the two-point coverage probability P{y1 ∈ C(0,P), y2 ∈ C(0,P)} for two given points y, z (cf. Definition 3.5). In general, it is difficult to evaluate this probability analytically even for the M model. A special, but very important case, is when the fading W+M/M is appropriately taken into account in the SINR cell model.

We have seen in Section 2.3.3 that a precise description of reality requires a response function of the form L(x, y, p) = pF(x, y)/l(|x − y|) where F(x, y) is a random fading field on R2 × R2.

Moreover, in Section 2.3.3.2 we have introduced the GI/GI/k model for SN, which is useful when a discrete number of receiver locations yj, j = 1, . . . , k is involved. In this model, instead of considering the whole fading field, one attaches a k-dimensional fading vector (fi . ., fk) to each point of the point process, where (f , . , fk) represents the channel conditions fj = F(xi, yj), in the channels from the considered point towards the k receivers. Now we adopt this approach in the SINR cell model.


<!-- p:117 -->


Kendall-like Notation cont. We consider the GI/k/(W + GI/GI/k) model, where the k in the numerator means that the mark attached to point X consists of the emitted power P and a fading vector (F1, .. . , Fk), with Fj = F(X, yj), describing the channels from X to k locations y1, . . . , Yk. The notation GI/GI/k in the denominator means that the fading conditions are taken into account for all interfering signals as well. In this model, we assume that all fading variables are independent.

### 5.4.1 Covariance Function

We now analyze the covariance function po(y1, y2) = P{y1 ∈ C(0,P), y2 ∈ C(0,P)} of the SINR cell with fading.

M/2 Proposition 5.9. For the W/++/+12 model, we have

$$p _ { 0 } ( y _ { 1 } , y _ { 2 } ) = \mathcal { L } _ { W } \left ( \mu t \left ( l ( | y _ { 1 } | ) + l ( | y _ { 2 } | ) \right ) \mathcal { L } _ { ( I _ { 1 } , I _ { 2 } ) } \left ( \mu t l ( | y _ { 1 } | ) , \mu t l ( | y _ { 2 } | ) \right ) ,$$

where L(I1,I2)(t1,t2) is the joint Laplace transform of the vector (I1, I2) = (Iδ(y1), Iδ(y2)) of the SN in the GI/GI/2 model.

Proof. When using the same type of arguments as in the proof of Proposition 5.5, we have

$$S i d v & \ L a r { W } \\ p _ { 0 } ( y _ { 1 } , y _ { 2 } ) & = \mathbf P \{ \ P F _ { 1 } \geq t l ( | y _ { 1 } | ) ( W + I _ { 1 } ) , \ P F _ { 2 } \geq t l ( | y _ { 2 } | ) ( W + I _ { 2 } ) \} \\ & = \int _ { 0 } ^ { \infty } \int _ { 0 } ^ { \infty } \int _ { 0 } ^ { - \mu u t ( | ( y _ { 1 } | ) + l ( | y _ { 2 } | ) ) } e ^ { - \mu v _ { 1 } t l ( | y _ { 1 } | ) } e ^ { - \mu v _ { 2 } t l ( | y _ { 2 } | ) } \\ & \quad \times \mathbf P \left ( W = d u , I _ { 1 } = d v _ { 1 } , I _ { 2 } = d v _ { 2 } \right ) \\ & = \mathcal { L } _ { W } \left ( \mu t ( l ( | y _ { 1 } | ) + l ( | y _ { 2 } | ) ) \mathcal { L } _ { ( I _ { 1 } , I _ { 2 } ) } ( \mu t l ( | y _ { 1 } | ) , \mu t l ( | y _ { 2 } | ) ) ,$$


<!-- p:118 -->


where the first equality uses the fact that in the M/2 model, the received powers PF1, PF2 are independent exponential random variables with parameter μ, while the second equality uses the fact that (I1, I2) and W are independent. □

M/2 Example 5.10. For the model with deterministic emitted 0+M/D/2 power p = 1/μ, Proposition 2.6 implies that

$$p _ { 0 } ( y _ { 1 } , y _ { 2 } ) \\ = \exp \left [ - \lambda \int _ { 0 } ^ { 2 \pi } \int _ { 0 } ^ { \infty } r ( 1 - e ^ { - t \left ( l ( r ) / l ( r _ { 1 } ) + l ( \sqrt { r ^ { 2 } + s ^ { 2 } - 2 r s \cos \theta } ) / l ( r _ { 2 } ) \right ) } ) \, d r d \theta \right ] ,$$

where r1 = |y1|, r2 = |y2| and s = |y1 − y2|. For the M/2 model, we get from Corollary 2.12 that 0+M/M/2

$$p0(y1, y2) c2π ∞J = exp −λ r 1 X drdθ (1 +tl(r)/l(r1))(1+tl(√r2+s2−2rscosθ)/l(r2))$$

## 5.5 Noise or Interference Limited Cell: Towards a Boolean or Voronoi Shape

We focus now on the shape of the SINR cell. In general it is very complicated and few things can be said about it. However in some special cases, it takes a "classical" form. These cases consist of:

(noise limited cell) diminishing the influence of the interference field in such a way that the noise field becomes predominant; in this case, the SINR cell takes the form of a Boolean cell (the Boolean model could then be seen as a Signal to Noise Ratio (SNR) cell model);

(interference limited cell) in the absence of noise field, and when the power attenuation is strong, then the impact of the nearestneighbor interferers becomes predominant; in this case the SINR cell takes the form of a Voronoi cell;


<!-- p:119 -->


(noise and interference limited cell) when the power attenuation is strong and related in an appropriate way to the thermal noise field, then the cell expands like the Voronoi cell in the directions towards the interferers which are close enough, and it expands like the Boolean cell in directions where the nearest interferers are farther away than some threshold distance. This case can be related to the so called Johnson-Mehl cell; see e.g. [42, Section 10.7, p. 333–334].

Before starting let us formalize the notion of convergence of closed sets (see [29, Theorem 1.2.2, p. 6]),

Definition 5.2 (Painlevé-Kuratowski convergence of closed sets). We say that the sequence {Fn} of closed subsets of Rd converges to a closed set F ⊂ Rd (we write limn Fn = F) if the following two conditions are satisfied:

- (1) For any x ∈ F, there exists a sequence xn, where xn ∈ Fn for all n ≥ 1 except for at most a finite number, such that xn converges to x in Rd.
- (2) For any sub-sequence of sets Fnk, k ≥ 1, and any sequence of points xk ∈ Fnk converging to x, we have x ∈ F.

The following results are useful when studying the above convergence (see [29, Cor. 3, p. 7].

Corollary 5.11. Let Fn, F be closed subsets of Rd:

- If F1 ⊃ F2 ⊃ · · · and ∩n Fn = F, then limn Fn = F.
- If F1 ⊂ F2 ⊂ · · · and Un Fn = A, then limn Fn = A, where A is the closure of A.

### 5.5.1 Noise Limited Cell: Towards the Boolean Case

Assume the following parametric dependence of the SINR cell on the SN generated by :

$$C ^ { ( \kappa ) } ( X , M ) = \left \{ y \colon L ( y , X , M ) \geq t ( \kappa I _ { \widetilde { \Phi } } ( y ) + w ( y ) ) \right \}$$


<!-- p:120 -->


-wh e n Sse e r nn  se  r    nre tion 2.2.1 (here with d′ = d).

Example 5.12. See the end of Section 24.3.4 in Volume II for an example of such an interference cancellation based on spread spectrum techniques.

Obviously the set C(0) (X,M), which we call the Signal to Noise Ratio (SNR) cell , is a Boolean cell1 and no longer depends on ; this limiting case is easy to analyze. In what follows, we study the following continuity and differentiability problems, when κ → 0.

- In what sense and under what conditions does the SINR cell C(k) ? (X,M) (X,M)
- Assuming this continuity and taking κ small, what first (or a higher) order perturbation should one apply to the characteristics of the SNR cell to get the characteristic of the SINR cell?

Convergence in the Space of Closed Sets. In order to prove convergence theorems, we need the following technical condition on the response function L:

- (1) for each x, y ∈ Rd and m ∈ Rl, there exists a sequence yn such that L(yn, x, m) &gt; L(y, x, m) and limn yn = y.

We also suppose for simplicity that the condition (4) of the standard scenario of Section 5.3 for SINR holds, i.e., that the thermal noise field w(y) = W is constant in space (but the value W can be random).

Proposition 5.13. Assume that the conditions of Corollary 5.2 with w(y) = W &gt; 0 and Condition (1) are satisfied. Then almost surely

$$C _ { ( X , M ) } ^ { ( 0 ) } = \overline { \bigcup _ { \kappa } C _ { ( X , M ) } ^ { ( \kappa ) } } ,$$

1 Recall that in the Boolean model the cell (grain) attached to a given point, say at X, neither depends on the locations of the points of the point process nor on their grains.


<!-- p:121 -->


where  ̄ denotes the closure of C. Consequently, since (y)0 is an (X,M) increasing family of closed sets, limκ→0 C (y) γ(0) in the space (X,M) (X,M) of closed sets (Painlevé-Kuratowski convergence).

(0)O ⊃ (zi)O = = C(0) and C(0) is closed, (X,M) (X,M) ∪C(k) ⊂ C(0).

$$\kappa$$

It remains to show that C(0) ⊂ Uk C(k). For this, take any y ∈ C(0). This means L(y, X, M) ≥ tw. Condition (1) above then guarantees the ' &lt; (  )t u e t t s  ←  s   xe) which implies that yn ∈ C(κn) for some κn &gt; 0. So

$$y = \lim _ { n } y _ { n } \in \overline { \bigcup _ { n } C ^ { ( \kappa _ { n } ) } } \, ,$$

which completes the proof.

Figure 5.2 illustrates this convergence.

Convergence of Characteristics. We now consider the convergence of certain characteristics of the SINR cell to those of the SNR cell, including the probability for a point to be covered (volume fraction), the capacity functional, and the volume of the typical cell. This can only be done under some additional conditions, because these characteristics are not continuous functions on the space of closed sets. Here is an example of such a result.

Denote by

$$D _ { ( X , M ) } = \{ y \colon L ( y , X , M ) = t W \}$$

the set of locations where the signal-to-noise ratio (without interference) is exactly equal to t. One can think of it as the boundary of the SNR cell C(0) (X,M); however this is not always true.

Proposition 5.14. Suppose the conditions of Proposition 5.13 are satisfied. Let K be a compact set and K denote the largest open set

□


<!-- p:122 -->


10

Fig. 5.2 The SINR cells limited by the noise (converging to a Boolean model). Standard stochastic scenario U,..., U scenario; see Section 6.3) with U uniform distribution on [0, 2], w(y) = W = 0.1, t = 1, and OPL with path loss exponent β = 3. On successive figures κ = 0.4,0.2,0.2 and 0.0001. For more discussion see Example 7.8.

10

8


6

O

4


2


0

2

4

6

8

10

0

2

4

6

8

10


8


6

4

2

4

6

8

10

0

2

4

6

8

10

contained in K. If

$$P \{ \, D _ { ( X , M ) } \cap K \neq \emptyset \, \text { and } D _ { ( X , M ) } \cap \mathring { K } = \emptyset \, \} = 0$$

then we have the following convergence of the capacity functional of the SINR cell on the set K:

$$\lim _ { \kappa \rightarrow 0 } P \{ \, K \cap C _ { ( X , M ) } ^ { ( \kappa ) } \neq$$


<!-- p:123 -->


Proof. The result is a consequence of the following fact: if D(x,M) ∩ K ≠∅ implies D(x,M) ∩K ≠∅ then

$$\lim _ { \kappa \to 0 } 1 ( K \cap C _ { ( X , M ) } ^ { ( \kappa ) } \neq \emptyset ) = 1 ( K \cap C ^ { ( 0 ) } ( X , M ) \neq \emptyset ) \, .$$

In order to prove (5.11) we assert the following inequalities:

$$1 ( K \cap C _ { ( X , M ) } ^ { ( 0 ) } \neq \emptyset ) - \i ( K \cap D _ { ( X , M ) } \neq \emptyset , \mathring { K } \cap D _ { ( X , M ) } = \emptyset ) \\ \leq \lim _ { \kappa \to 0 } \i ( K \cap C _ { ( X , M ) } ^ { ( \kappa ) } \neq \emptyset ) \\$$

$$1 ( K \cap C _ { ( X , M ) } ^ { ( 0 ) } \neq \emptyset ) \, .$$

Inequality (5.13) is immediate from the fact that (x)0 C(0) (X,M) (X,M) Jr       ( r       t K∩C(0) (X,M) ) ≠∅ and if in addition, for all κ &gt; 0, K ∩ C(x) (X,M) = ∅, then the second indicator in the left-hand side of (5.12) is equal to 1. But under these two assumptions, there exists y ∈ K such that L(y, X, M) ≥ tW and L(y, X, M) &lt; tW + κ1 for any positive κ1, and so L(y, X, M) = tW. This means K ∩ D(x,M) ≠ ∅ and by our assumption also K ∩ D(x,M) ≠ ∅. Let y ∈ K ∩ D(x,M). By Condition (1) we can find y′ ∈ K in the neighborhood of y, such that L(y′, X, M) &gt; tW. This gives K ∩ C(k) ≠ ∅ for some κ &gt; 0, contradicting our assump(X,M) tion and concluding the proof of (5.12). □

Remark. Note that in the case of a translation invariant function L, i.e., when L(y, x, m) = L(y − x,0, m) for all x, y, ∈ Rd, the condition (5.10) is equivalent to

$$P \{ \, X \in ( \check { D } _ { ( 0 , M ) } \oplus K ) \ \, \Big ( \check { D } _ { ( 0 , M ) } \oplus \mathring { K } \Big ) \, \Big \} = 0 \, ,$$

where ň = {−y : y ∈ D}. In particular for the standard SINR scenario and for the path-loss models OPL 2 and OPL 3, the assumptions of Proposition 5.14 are satisfied. Then, for K = {y}, Condition (5.10) reads P{ P = tWl(|y − X|) } = 0.

Let

$$E C \\ p _ { 0 } ^ { ( \kappa ) } ( y ) = P \{ y \in C _ { ( 0 , P ) } ^ { ( \kappa ) } \} \quad \text {and} \quad v _ { 0 } ^ { ( \kappa ) } = E [ | C _ { ( 0 , P ) } ^ { ( \kappa ) } | ] . \\ \\ E w o n o i t i o n \, \mathbf E = 1 4 \, w o n o o i g i l l \, d o w i w \, t h e f l o w i w n o w l t o t$$

From Proposition 5.14 we can easily derive the following results.


<!-- p:124 -->


Corollary 5.15. Assume the standard SINR scenario and a path-loss model OPL 2 or OPL 3. Assume that either the distribution function G of P or that of W has a density. Then P{P = tWl(|z|) } = 0 for all z ∈ Rd and

$$\mathbb { Z } \in \mathbb { K } ^ { \ast } \text { and } \\ & \lim _ { \kappa \to 0 } p _ { 0 } ^ { ( \kappa ) } ( y ) = p _ { 0 } ^ { ( 0 ) } ( y ) = 1 - E [ G ^ { - } ( t W l ( | y | ) ) ] , \\ & \lim _ { \kappa \to 0 } v ^ { ( \kappa ) } = v _ { 0 } ^ { ( 0 ) } = 2 \pi \int _ { 0 } ^ { \infty } r ( 1 - E [ G ^ { - } ( t W l ( r ) ) ] ) \, d r \, ,$$

where G− (u) = limv u G(v) is the left-continuous version of G and the expectation is taken with respect to the random noise W.

The second relation follows from (5.7).

Perturbation Formulae. Assume the standard SINR scenario. Note that Corollary 5.15 gives the following approximation of the one point coverage probability

$$p _ { x } ^ { ( \kappa ) } ( y ) = 1 - E [ G ^ { - } ( t W l ( | y | ) ) ] + o ( 1 ) \, ,$$

when κ → 0, for OPL 2 or OPL 3 and provided the distribution function G of the emitted power P has a density. Now we briefly show how to

Let F* denote the left-continuous version of the distribution function of the random variable P/(tl(|y|)) − W, i.e.

$$F _ { * } ( u ) = \mathbf P \{ P / ( t l ( | y | ) ) - W < u \} .$$

We suppose that F* admits the following approximation at 0

$$\lim _ { u \searrow 0 } \frac { F _ { * } ( u ) - F _ { * } ( 0 ) } { u ^ { \eta } } = f _ { * } \quad \text {for some } \eta \geq 0 , f _ { * } < \infty .$$

Proposition 5.16. Assume that (5.17) holds for some η ≥ 0 and f* &lt; ∞. Then when E[(Iδ(y))η &lt; ∞],

$$p _ { 0 } ^ { ( \kappa ) } ( y ) = 1 - \mathbf E [ G ^ { - } ( t W l ( | y | ) ) ] \\ - \kappa ^ { \eta } f _ { * } \mathbf E \left [ ( I _ { \tilde { \Phi } } ( y ) ) ^ { \eta } 1 ( I _ { \Phi } ( y ) > 0 ) \right ] + o ( \kappa ^ { \eta } ) .$$


<!-- p:125 -->


Remark. Note that if either G or the distribution function of W has a density, then F*(u) admits the density f*(u) at the origin (which however might be infinite) and η = 1, f* = f*(0). On the other hand, if P/(tl(|y|)) − W has an atom at 0; i.e., if P{ P = tWl(|y|) } &gt; 0 (which is not possible under the assumptions of Corollary 5.15), then (5.17) holds for η = 0, f = P{ P = tl(|y|) − W }, and thus (5.18) yields

$$= P \{ P > t l ( | y | ) W \} + P \{ P = t l ( | y | ) W , \, I _ { \widetilde { \Phi } } ( y ) = 0 \} + o ( 1 ) .$$

Proof of Proposition 5.16. We have

$$1 0 0 1 0 1 P \text { position } 1 . 0 . \text { we have} \\ p _ { 0 } ^ { ( \kappa ) } ( y ) = P \{ P \geq t l ( | y | ) W \} - P \{ 0 \leq P / ( t l ( | y | ) ) - W < \kappa I _ { \widetilde { \Phi } } ( y ) \} . \\ \\$$

Sn  (   n  e r  n  d al to E[F*(κI ̄(y)) − F*(0)]. If E[(I∼(y))η] &lt; ∞ and (5.17) holds then

$$E \left [ \frac { F _ { * } ( \kappa I _ { \widetilde { \Phi } } ( y ) ) - F _ { * } ( 0 ) } { ( \kappa I _ { \widetilde { \Phi } } ( y ) ) ^ { \eta } } 1 ( I _ { \widetilde { \Phi } } ( y ) > 0 ) ( I _ { \widetilde { \Phi } } ( y ) ) ^ { \eta } \right ] \\ \leq E \left [ ( f _ { * } + A ) ( I _ { \widetilde { \Phi } } ( y ) ) ^ { \eta } \right ] < \infty \, ,$$

o eo q sn on   y e o  &gt;  tonn eons ted convergence theorem

$$\lim _ { \kappa \to 0 } \frac { 1 } { \kappa ^ { \eta } } P \{ 0 \leq p / ( t l ( | y | ) ) - W < \kappa I _ { \widetilde { \Phi } } ( y ) \} \\ = f _ { * } E \left [ ( I _ { \widetilde { \Phi } } ( y ) ) ^ { \eta } I ( I _ { \widetilde { \Phi } } ( y ) > 0 ) \right ] ,$$

which completes the proof.

□

If the distribution function F* admits a higher order approximation, 1, . . . , h, at 0; i.e.,

$$1 , \dots , h , \, a t \, 0 ; 1 . e . , \\ F _ { * } ( u ) = F _ { * } ( 0 ) + \sum _ { k = 1 } ^ { h } \frac { F _ { * } ^ { ( k ) } ( 0 ) } { k ! } u ^ { k } + \mathcal { R } ( u ) \quad \text {and} \quad \mathcal { R } ( u ) = o ( u ^ { h } ) \quad u \searrow 0 .$$


<!-- p:126 -->


Proposition 5.17. Assume that (5.20) holds for some h ≥ 1. Then

$$p _ { 0 } ^ { ( \kappa ) } ( y ) & = 1 - E [ G ^ { - } ( t W l ( | y | ) ) ] - \sum _ { k = 1 } ^ { h } \kappa ^ { k } \frac { F _ { ^ { * } } ^ { ( k ) } ( 0 ) } { k ! } E [ ( I _ { \widetilde { \Phi } } ( y ) ) ^ { k } ] + o ( \kappa ^ { h } ) , \\ \intertext { provided } \intertext { provided } E [ ( I _ { \widetilde { \ast } } ( y ) ) ^ { h } ] & < \infty ,$$

provided E[(Iδ(y))h] &lt; ∞.

The proof goes along the same lines as the proof of Proposition 5.16. From (5.7) we see that, in principle, any approximation of the coverage probability also yields an approximation of the mean cell volume, simply by integration of the terms of the latter expansion with respect to y. In what follows, we show how to justify the interchange of the integral and the expansion for the case of formula (5.21), assuming, as before, the standard scenario for SINR.

In order to express the dependence on y, we write F*(u;y) and (u; y) to denote F* defined in (5.16) and its derivatives with respect to u. Similarly, we denote the remainder term in (5.20) by R(u;y). Assume now that (5.20) holds for all y ∈ Rd and moreover

$$| \mathcal { R } ( u , y ) | \leq \mathcal { H } _ { 1 } ( u ) \mathcal { H } _ { 2 } ( y )$$

where H1(u) is a nondecreasing function satisfying

$$\lim _ { u \searrow 0 } \frac { \mathcal { H } _ { 1 } ( u ) } { u ^ { h } } = 0$$

$$\int _ { 0 } ^ { \infty } \mathcal { H } _ { 2 } ( y ) \, d y < \infty \, .$$

Proposition 5.18. Assume that (5.20) and (5.22)−(5.24) hold for some h ≥ 1. Then the mean cell volume is

$$v ^ { ( \kappa ) } = v ^ { ( 0 ) } - \sum _ { k = 1 } ^ { h } \kappa ^ { k } \frac { 1 } { k ! } \int _ { 0 } ^ { \infty } F _ { * } ^ { ( k ) } ( 0 ; y ) \, d y \, E \left [ ( I _ { \widetilde { \Phi } } ( 0 ) ) ^ { k } \right ] + o ( \kappa ^ { h } ) \, , \quad ( 5 . 2 5 )$$

provided ∞ (0; y) dy &lt; ∞ for k = 1, . . . , h and

$$E \left [ \mathcal { H } _ { 1 } ( I _ { \widetilde { \Phi } } ( 0 ) ) \left ( I _ { \widetilde { \Phi } } ( 0 ) \right ) ^ { h } \right ] < \infty \, .$$

and Proof. By (5.7), (5.19) and (5.20), it suffices to show that


<!-- p:127 -->


$$\lim _ { \kappa \to 0 } \kappa ^ { - h } \int _ { 0 } ^ { \infty } \mathbf E [ \mathcal { R } ( \kappa I _ { \widetilde { \Phi } } ( y ) ; y ) ] \, d y = 0 \, .$$

For fixed y, by Proposition 5.21 we have pointwise convergence κ−hE[...] → 0. We establish the conditions of the dominated convergence theorem for lim ∫ κ−hE[...]dy. For this, thanks to (5.23), take any ∆ &gt; 0 and u0 such that H1(u) ≤ ∆ for u ≤ u0. Now, by monotonicity of H1(u), for κ ≤ 1

$$\kappa ^ { - h } & \int _ { 0 } ^ { \infty } \mathbf E | \mathcal { R } ( \kappa I _ { \widetilde { \Phi } } ( y ) ; y ) | d y \\ & \leq \int _ { 0 } ^ { \infty } \mathcal { H } _ { 2 } ( y ) \, d y \left ( \mathbf E [ \Delta ( I _ { \widetilde { \Phi } } ( 0 ) ) ^ { h } \mathbf I ( \kappa I _ { \widetilde { \Phi } } ( 0 ) \leq u _ { 0 } ) ] \\ & + \mathbf E \left [ \mathcal { H } _ { 1 } ( I _ { \widetilde { \Phi } } ( 0 ) ) \left ( \frac { I _ { \widetilde { \Phi } } ( 0 ) } { u _ { 0 } } \right ) ^ { h } \mathbf I ( \kappa I _ { \widetilde { \Phi } } ( 0 ) > u _ { 0 } ) \right ] \right ) , \\ \text {which is finite by } \, ( 5 . 2 4 ) \text { and Assumption } ( 5 . 2 6 ) ; \text { this completes the}$$

which is finite by (5.24) and Assumption (5.26); this completes the proof. □

Example 5.19. Consider the standard stochastic scenario with OPL 2 (with A = 1) and assume that the distribution function G of P admits a density g. Then the conditions of Proposition 5.16 are satisfied if

$$f _ { * } = E \left [ \frac { g ( t W l ( | y | ) ) } { \ t W l ( | y | ) } \right ] < \infty .$$

Assume in addition that t,l(|y|) and W are strictly positive. Direct computations give the following first order expansion for the mean volume of the typical cell (provided the moments used in the expansion are all finite):

$$\text {the of the typical cell (provided the moments used in the expansion)}} \\ \text {all finite): \\ v ^ { ( \kappa ) } = \pi \text {E} \left [ \left ( \left ( \frac { P } { W } \right ) ^ { 1 / \beta } - 1 \right ) ^ { + } \right ) ^ { 2 } \right ] \\ + \kappa \frac { 2 \pi E [ I _ { \Phi } ( 0 ) ] } { \beta } \left ( E \left [ \left ( \frac { P } { W } \right ) ^ { 1 + 1 / \beta } \right ] E [ P ^ { 1 / \beta } ] \\ - E \left [ \left ( \frac { P } { W } \right ) ^ { 1 / \beta } \right ] E [ P ^ { - 1 + 1 / \beta } ] \right ) + o ( \kappa ) \, ,$$


<!-- p:128 -->


Note that the existence of the negative moment E[P-1+1/β] is guaranteed by Condition (5.17) and that

$$\text {ed by Condition (3.11) and that} \\ E [ I _ { \widetilde { \Phi } } ( 0 ) ] & = \int _ { 0 } ^ { \infty } s g ( s ) d s \, 2 \pi \lambda \int _ { 0 } ^ { \infty } \frac { r } { ( 1 + r ) ^ { \beta } } \, d r \\ & = \frac { 2 \pi \lambda } { - 3 \beta + \beta ^ { 2 } + 2 } \int _ { 0 } ^ { \infty } s g ( s ) \, d s \, .$$

### 5.5.2 Interference Limited Cell: Towards the Voronoi Case

Consider for simplicity the standard SINR scenario. Recall that from Definition 4.1, the Voronoi cell Cx = Cx(Φ) attached to point X of Φ, is determined by some "neighboring" points of Xi ∈ Φ only. It is quite reasonable to expect that if we let the OPL function l(r) increase fast in r, we get the same effect for the SINR cell C(x,P). We formalize this observation taking appropriate families of OPL functions.

Convergence in the Space of Closed Sets. Let ln(r) = (1 + r)n, W = 0, P &gt; 0 almost surely. Denote by Cnx (X,P) C(X,P)( ̄, 0,t) the yn SINR cell corresponding to the OPL ln.

Proposition 5.20. Almost surely the following convergence holds on the space of closed sets (Painlevé-Kuratowski convergence)

$$\lim _ { n \to \infty } C _ { ( X , P ) } ^ { n } = \mathcal { C } _ { X } \, ,$$

where Cx = Cx(Φ) is the Voronoi cell of point X ∈ Φ w.r.t. Φ.

Proof. Denote by r(n) (y) the SN associated with the OPL function ln. Φ Note that we have I(n) (y) &gt; 0 for all n provided Φ(R2) &gt; 0; otherwise Φ C(x,P) = Cx = R2 and the result trivially holds. Moreover, since we assumed P &gt; 0 almost surely, we have

$$\text {assumed } P > 0 \text { almost surely, we have} \\ ( I _ { \tilde { \Phi } } ^ { ( n ) } ( y ) ) ^ { 1 / n } = \left ( \sum _ { ( x _ { k } , p _ { k } ) \in \tilde { \Phi } } P _ { k } ( 1 + | y - x _ { k } | ) ^ { - n } \right ) ^ { 1 / n } \\ \stackrel { n \to \infty } { \longrightarrow } \sup _ { x _ { k } \in \Phi } ( 1 + | y - x _ { k } | ) ^ { - 1 } = \left ( 1 + \min _ { x _ { k } \in \Phi } | y - x _ { k } | \right ) ^ { - 1 } \quad ( 5 . 2 7 )$$


<!-- p:129 -->


(this property differs from the standard calculus exercise in that the number of terms in the sum is infinite; it uses the property that a.s. the above supremum is reached by a unique point of Φ). Moreover |y − X| ≤ fn(y)}, where

$$f _ { n } ( y ) = \left ( \frac { P } { t I _ { \widetilde { \Phi } } ^ { ( n ) } ( y ) } \right ) ^ { 1 / n } - 1 \, .$$

$$\lim _ { n \to \infty } f _ { n } ( y ) = \min _ { x _ { k } \in \Phi } | y - X |$$

|y − X| ≤ minxk∈Φ |y − xk|}. According to Definition 5.2 we have to show that the following two conditions hold:

- (i) For any y s.t. |y − X| ≤ minxk∈Φ |y − xk|, there exists a sequence of points yn → y such that |yn − X| ≤ fn(yn) for all sufficiently large n.
- (ii) If a sequence of points ykn, such that |ykn − X| ≤ fkn(ykn) for all n, converges to y, then |y − X| ≤ minxk∈Φ |y − xk|.

Suppose y is in the interior of the Voronoi cell; i.e., |y − X| &lt; minxk∈Φ |y − xk|. Then |y − X| ≤ fn(y) for all sufficiently large n because fn(y) → minxk∈Φ |y − xk|. So Condition (i) is satisfied with the constant sequence yn = y. If y is on the boundary of the Voronoi cell, i.e. if |y − X| = minxk∈Φ |y − xk|, then there exists a sequence of points yn converging to y and such that for all n, |yn − X| &lt; minxk∈Φ |yn − xk|. One can use this sequence to construct the one required in (i).

Let ykn be as given in (ii). For all n

$$| y _ { k _ { n } } - X | \leq f _ { k _ { n } } ( y _ { k _ { n } } ) .$$

Letting n → ∞, the left-hand side tends to |y − X| and the right-hand side (because of the uniform convergence of fn) to minxk∈Φ |y − xk| and ·|ix − h| Φ∃(xα &gt; |X − h| 4ə ə □

By (5.27)


<!-- p:130 -->


Remark. A result similar to (5.20) can be proved for any family of OPL functions lα satisfying

$$\lim _ { \alpha \to \alpha _ { 0 } } l _ { \alpha } ^ { - 1 } \left ( \sum _ { i } p _ { i } / l _ { \alpha } ( x _ { i } ) \right ) \to \frac { 1 } { \min _ { i } x _ { i } }$$

for any (positive) coefficients pi. For example for lα(yi) = exp[αyi] and α0 =∞.

We show some snapshots in Figure 5.3. Note also that the above result suggests that the VT access model considered in Section 4.5 may be a reasonable model, at least for high path-loss exponents.

Convergence of Characteristics. As in the Boolean case, one can prove the convergence of various functionals. We consider here only the cell volume.

converges in distribution to the volume of the Voronoi cell Cx(Φ) provided the boundary of Cx(Φ) has volume 0 almost surely.

Proof. This can be done using the following inequalities

$$1 ( z \in \mathcal { C } _ { X } ( \Phi ) ) - 1 ( | z - X | = \min _ { x _ { k } \in \Phi } | z - x _ { k } | ) & \leq \liminf _ { n \to \infty } ( z \in C _ { ( X , P ) } ^ { n } ) \\ & \leq \limsup _ { n \to \infty } ( z \in C _ { ( X , P ) } ^ { n } ) \\ & \leq 1 ( z \in \mathcal { C } _ { X } ( \Phi ) ) ,$$

which hold for all z ∈ Rd. Then, representing volumes as integrals with respect to Lebesgue measure, using the Fatou lemmas for liminf and limsup, we get the conclusion provided that

$$\int _ { \mathbb { R } ^ { d } } 1 \left ( | z - x | = \min _ { x _ { k } \in \Phi } | z - x _ { k } | \right ) d z = 0$$

almost surely.

□

The last condition of the proof is true, e.g. for the Poisson p.p. Φ with a diffuse intensity measure Λ, in particular for any stationary Poisson p.p.


<!-- p:131 -->


10


□

Q

2

4

10

0

2

8

10


8

6

10

0

2

4

8


10

Fig. 5.3 The SINR cells limited by increasing impact of interference in the absence of noise (converging to the Voronoi tessellation). Standard stochastic scenario 0/M+0 U,...,U (the sequence of symbols U, ... , U corresponds to a multi-cell scenario; see Section 6.3), with U uniform distribution on [0, 2], w(y) = 0, t = 0.2; OPL with path loss exponent β = 3, 5, 12 and 100. For more discussion, see Example 7.12.

### 5.5.3 Noise and Interference Limited Cell: Towards the Johnson-Mehl Cell

We also have convergence to intermediate states of the Johnson-Mehl grain growth model (see, e.g. [42, Section 10.7, pp. 333–334],

Corollary 5.22. Under the assumptions of Proposition 5.20, if, instead of W ≡ 0, we take W = (R + 1)−n for some fixed or random


<!-- p:132 -->


10

Fig. 5.4 The SINR cells limited by strong interference and increasing noise (JohnsonMehl grain growth model). Standard stochastic scenario U,...,U (the sequence of symbols W+M/U U,... , U corresponds to a multi-cell scenario; see Section 6.3), with U uniform distribution on [0, 2], t = 0.5, OPL with path loss exponent β = 30. Increasing noise w(y) = W = (1 + R)−30, where R = 0.4, 1.2,2 and ∞ (i.e., W = 0). For more discussion, see, Example 7.13.

10

口

8


6

4

2

10

2

4

6

8

10


2

4

6

8

10

0

8


口


4

0

2


4

6

8

10

0

2

4

6

8

10

variable R, then

$$\lim _ { n \to \infty } C _ { ( X , P ) } ^ { n } = \mathcal { C } _ { X } ( \Phi ) \cap B _ { X } ( R ) \, ,$$

where Bx(R) is the ball centered at X of radius R.

We give an illustration of this convergence in Figure 5.4.


<!-- p:133 -->


6

### Interacting Signal-to-Interference Ratio Cells

## 6.1 Introduction

We consider now the relationships between several SINR cells. As in Chapter 5, let  = Σiε(xi,mi) be an i.m.p.p. with points {xi} in Rd s-s as   ( tt   {} s e generated by  and the response function L: Rd × Rd × Rl → R+.

Definition 6.1. Let n be a positive integer and let (Xi, Mi), i = 1, . . . , n, X ∈ Rd, M ∈ R, be a collection of n marked points. Let ti ≥ 0, i = 1, . . . , n be a collection of n thresholds. We define the SINR cells of this collection of marked points and thresholds in the shot-noise field I and the thermal noise field w(y) ≥ 0 as

$$I _ { \Phi } ^ { \dagger } \text { and the merhal house field } w ( i ) \geq 0 \text { as } \\ C _ { ( X _ { i } , M _ { i } ) } = C _ { ( X _ { i } , M _ { i } ) } ( \tilde { \Phi } , \{ ( X _ { j } , M _ { j } ) , j \neq i \} , w , t _ { i } ) \\ = \left \{ y \colon L ( y , X _ { i } , m ) \geq t _ { i } ( I _ { \tilde { \Phi } } ( y ) + \kappa \sum _ { j \neq i } L ( y , X _ { j } , M _ { j } ) + w ( y ) ) \right \} , \\ \\ \text {where } 0 < 6 < 1 \text { is some constant.}$$

where 0 &lt; κ ≤ 1 is some constant.


<!-- p:134 -->


If κ = 1, this is the collection of SINR cells of the points Xi, i = 1, . . . , n for the SN created by the p.p.

$$\widetilde { \Phi } + \sum _ { i = 1 } ^ { n } \delta _ { X _ { i } , M _ { i } } .$$

If κ ≠ 1, the response of the points Xj and that of the points of  are weighted differently.

Example 6.1 (Downlink in a Code Division Multiple Access cell with several users). Let  be an i.m. Poisson p.p. representing the location of base stations using Code Division Multiple Access (CDMA) (see Section 25.1.4 in Volume II). Let X be the location of a tagged base station with n users. Since all n users are served by the tagged base station, we take Xi = X for i = 1, . . . , n. In this case the cell C(xi,Pi) gives the locations where user i, when served by the tagged base station with power Pi, receives a signal strong enough to sustain the goodput that corresponds to the SINR threshold ti. In this case the factor κ might stem from the fact that orthogonal signatures are used within a cell. Another essential feature of CDMA is power control (addressed in Section 25.2 in Volume II).

Remark 6.1. Note that when changing the thresholds ti to

$$t _ { i } ^ { \prime } = \frac { t _ { i } } { 1 + \kappa t _ { i } } & & ( 6 . 2 )$$

( X )T ν= q ()  ( X )T≠ dax ) ( Indeed,

$$L ( y , X _ { i } , m ) & \geq t _ { i } ( I _ { \widetilde { \Phi } } ( y ) + \kappa \sum _ { j \neq i } L ( y , X _ { j } , M _ { j } ) + w ( y ) ) \\$$

iff

$$L ( y , X _ { i } , m ) & \geq t _ { i } / ( 1 + \kappa t _ { i } ) ( I _ { \widetilde { \Phi } } ( y ) + \kappa \sum _ { j = 1 } ^ { n } L ( y , X _ { j } , M _ { j } ) + w ( y ) ) . \\$$

This means that

$$C _ { ( X _ { i } , M _ { i } ) } ( \widetilde { \Phi } , \{ ( X _ { j } , M _ { j } ) \} _ { j \neq i } , t _ { i } ) = & C _ { ( X _ { i } , M _ { i } ) } ( \widetilde { \Phi } , \{ ( X _ { j } , M _ { j } ) \} _ { j = 1 , \dots , n } , t _ { i } ^ { \prime } ) .$$


<!-- p:135 -->


## 6.2 Constraints on Cell Intersections

We now comment on a basic algebraic property which sheds some light n    s   t t  ve holes, and this happens even in the case of a simple isotropic response function L.

Proposition 6.2. Consider the collection of SINR cells C(Xi,Mi) = C(Xi,Mi)(δ, {(Xj, Mj), j ≠ i}, ti) of Definition 6.1. For any subset J ⊂ {1,. . ., n} of cells, if ∩i∈J C(Xi,Mi) ≠ ∅, then Σi∈J ti ≤ 1/κ, where ti is given by (6.2).

Proof. Assume y ∈∩i∈J C(xi,Mi) ≠ ∅. Then by Remark 6.1, we have the set of inequalities

$$L ( y , X _ { i } , m ) \geq t _ { i } ^ { \prime } \kappa \sum _ { j \in J } L ( y , X _ { j } , M _ { j } ) , \quad i \in J \, ,$$

Summing them up, we obtain

$$\sum _ { j \in J } L ( y , X _ { j } , M _ { j } ) \geq \kappa \sum _ { i \in J } t _ { i } ^ { \prime } \sum _ { j \in J } L ( y , X _ { j } , M _ { j } ) \, ,$$

which is equivalent to Σi∈J t′i ≤ 1/κ.

□

Remark 6.2. Note that the above result is purely algebraic (no stochastic assumptions are made). It says that by increasing the signals L(y, Xi, Mi) that one cannot cover a given point y by arbitrarily many cells. In particular, in the case of constant ti = t no location can be covered by more than s = [tκ/(1 + tκ)], cells, whatever the locations Xi of the transmitters and whatever the strength of their signals L(y, Xi, Mi). For example, in Figure 5.3 s = 4, while in Figure 5.4 s = 1 inhibits any overlapping of cells.

Example 6.3 (Pole capacity of the downlink CDMA cell). Let us continue Example 6.1 and consider one given antenna, say located at X, which transmits a compound signal of total power P1 + . .· + Pn for serving n users with respective bit-rates corresponding to tk, k = 1, . . . , n. Since the possible locations of these users are described by the cells C(x,Pk), by Proposition 6.2, if Σi=1ti &gt; 1/κ then these cells cannot simultaneously cover any given location. This means that if all the users are at the same location, they cannot be served simultaneously by the tagged base station, no matter how strong the emitted powers are. If one assumes ti = t, this mean that no more than n1 ≤ (1 + κt)/(κt) users can be served. This upper bound for the number of users is called the pole capacity of the CDMA cell. It gives the maximal number of users that can be served at a given location with a bit-rate corresponding to the SINR threshold t.


<!-- p:136 -->


## 6.3 Stochastic Scenarios and Coverage Probabilities

By the standard stochastic scenario for collections of SINR cells, we understand the framework described in Section 5.3, with the response function L(y, x, p) = p/l(|y − x|), where l is an omni-directional power attenuation function (see Section 23.1.2 in Volume II), with assumption (3) of the single cell scenario replaced by:

- (3*) The marks Mj = Pj of the points Xj (j = 1, . . . , n) generating the cells C(xj,Pj) are mutually independent, independent of Φ, and have the same distribution function G as the marks ofΦ.

In a slightly more general case one can consider the scenario where

- (3*′) The marks P1, . . . , Pn are mutually independent and independent of  and have some given distribution G'.

Kendall-like Notation cont. Extending our previous notation for SINR, we call the above framework for collections of SINR cells GI,...,GI model, where GI's in the numerator denote the general disW+GI/GI tribution of the Pj's.

## 6.4 Joint Point-Coverage Probability

Assume the standard scenario for collections of SINR cells. Let y1, . . . , Yn be n locations. We are interested in theprobability that for all j = 1, . . . , n the cell C(xj,Pj) covers location yj:


<!-- p:137 -->


$$a l l \ j = 1 , \dots , n \, \text { the cell } C _ { ( X _ { j } , P _ { j } ) } \, \text { covers location } y _ { j } \colon \\ p _ { X _ { 1 } , \dots , X _ { n } } ( y _ { 1 } , \dots , y _ { n } ) \\ = P \left \{ \bigcap _ { j = 1 } ^ { n } \{ y _ { j } \in C _ { ( X _ { j } , P _ { j } ) } ( \widetilde { \Phi } , \{ ( X _ { l } , P _ { l } ) , l \neq j \} , W , t _ { i } ) \} \right \} \\ = P \left \{ \bigcap _ { j = 1 } ^ { n } \left \{ P _ { j } \geq t _ { i } l ( | y _ { j } - X _ { j } | ) \left ( I _ { \widetilde { \Phi } } ( y _ { j } ) + \kappa \sum _ { l \neq i } P _ { l } / ( | y _ { j } - X _ { l } | ) + W \right ) \right \} \right \} . \\ \\ \text {Special cases are the probability } p _ { X _ { 1 } , \dots , X _ { n } } ( y , \dots , y ) \text { that all cells cover a }$$

Special cases are the probability px,.., x(y, . . .,y) that all cells cover a given point y and the probability px,...,x(y1, . . .,yn) that a given node -nns  oeo o  os oons ons  on ple 6.3). Recall, that in all these cases, the powers Pl for l ≠ j are considered as interference with respect to the transmission j.

The following result gives the joint point-coverage probability for the W+Gi/GI model, where the received powers P1, ..., Pn are exponen-nM,...,M tial with mean 1/μ. Recall from Section 5.4 that this might correspond to a situation when Pj = Pfj, where P is some constant emitted power and fj is an exponential random variable modeling Rayleigh fading in the channel from Xj to yj. For simplicity we state and prove the result for two cells.

I (  (2s s)() ( e  =  (|X − |) =  (nt Laplace transform of the vector (I(y1), I(y2)) and Lw(s) the Laplace transform of W.

Proposition 6.4. Consider the standard M, Mw + GI/GI model. If

$$\delta = \frac { t _ { 1 } t _ { 2 } \kappa ^ { 2 } l _ { 1 1 } l _ { 2 2 } } { l _ { 2 1 } l _ { 1 2 } } < 1$$

then the joint point-coverage probability is equal to

$$\text {then the joint point-coverage probability is equal to} \\ p _ { X _ { 1 } , X _ { 2 } } ( y _ { 1 } , y _ { 2 } ) & = \mu \frac { 1 - \delta } { ( l _ { 2 1 } + t _ { 1 l 1 1 } \kappa ) ( l _ { 1 2 } + t _ { 2 l 2 2 } \kappa ) } \\ & \times \mathcal { L } _ { W } \left ( \frac { \xi _ { 1 } + \xi _ { 2 } } { 1 - \delta } \right ) \mathcal { L } _ { ( I _ { 1 } , I _ { 2 } ) } \left ( \frac { \xi _ { 1 } } { 1 - \delta } , \frac { \xi _ { 2 } } { 1 - \delta } \right ) , \\ \intertext { w h e r e } \xi _ { i } = t _ { i l j l i } ( l _ { i j } + t _ { l i j } + i ) , \, i , j = 1 , 2 , \, i \neq j , \, \text {otherwise} \, p _ { X _ { 1 } , X _ { 2 } } ( y _ { 1 } , y _ { 2 } ) = 0 ,$$

where ξi=tililji(lij+tjljjκ), i, j=1,2, i≠j. Otherwise px1,X2(y1, y2)=0.


<!-- p:138 -->


Proof. Note first that the condition (6.4) is necessary for the inequalities in (6.3) with j = 1,2 and n = 2 to hold when W ≡ 0 and Iī ≡ 0. So it is necessary for px1,X2(y1, y2) &gt; 0. In what follows, we assume it is satisfied. Similarly as in the proof of Proposition 5.9 we have

$$p _ { X _ { 1 } , X _ { 2 } } ( y _ { 1 } , y _ { 2 } ) & = \int _ { 0 } ^ { \infty } \int _ { 0 } ^ { \infty } \int _ { 0 } ^ { \infty } A ( u , v _ { 1 } , v _ { 2 } ) \\ & \quad \times P ( W = d u , I _ { 1 } = d v _ { 1 } , I _ { 2 } = d v _ { 2 } ) ,$$

with

$$A ( v , u _ { 1 } , u _ { 2 } ) = \int _ { 0 } ^ { \infty } \int _ { 0 } ^ { \infty } \mathbb { 1 } ( p _ { 1 } \geq t _ { 1 } l _ { 1 1 } ( u + v _ { 1 } + \kappa p _ { 2 } / l _ { 2 1 } ) ) \\ \times \mathbb { 1 } ( p _ { 2 } \geq t _ { 2 } l _ { 2 2 } ( u + v _ { 2 } + \kappa p _ { 1 } / l _ { 1 2 } ) ) \mu ^ { 2 } e ^ { - \mu ( p _ { 1 } + p _ { 2 } ) } \, d p _ { 1 } d p _ { 2 } .$$

For ai, bi ≥ 0, i = 1, 2 and b1b2 &lt; 1, we have

$$\int _ { 0 } ^ { \infty } \int _ { 0 } ^ { \infty } 1 ( p _ { 1 } \geq a _ { 1 } + b _ { 1 } p _ { 2 } ) \mathbb { 1 } ( p _ { 2 } \geq a _ { 2 } + b _ { 2 } p _ { 1 } ) \mu ^ { 2 } e ^ { - \mu ( p _ { 1 } + p _ { 2 } ) } \, d p _ { 1 } d p _ { 2 } \\ = \mu \frac { 1 - b _ { 1 } b _ { 2 } } { ( 1 + b _ { 1 } ) ( 1 + b _ { 2 } ) } \exp \left ( - \mu \frac { a _ { 1 } ( 1 + b _ { 2 } ) + a _ { 2 } ( 1 + b _ { 1 } ) } { 1 - b _ { 1 } b _ { 2 } } \right ) .$$

Taking ai = tilii(u + vi), bi = tiliiκ/lji with i, j = 1, 2, j ≠ i, we observe that b1b2 &lt; 1 is equivalent to (6.4) which we assume to be satisfied. Thus we have

$$\text {Thus we have} \\ p _ { X _ { 1 } , X _ { 2 } } ( y _ { 1 } , y _ { 2 } ) & = \frac { 1 - \delta } { ( l _ { 2 1 } + t _ { 1 1 1 } \kappa ) ( l _ { 1 2 } + t _ { 2 2 2 } \kappa ) } \\ & \times \int _ { 0 } ^ { \infty } \int _ { 0 } ^ { \infty } \int _ { \ e ^ { - \mu ( ( v + u _ { 1 } ) \xi _ { 1 } + ( v + u _ { 2 } ) \xi _ { 2 } ) / ( 1 - \delta ) } } \\ & \times P ( W = d u , I _ { 1 } = d v _ { 1 } , I _ { 2 } = d v _ { 2 } ) \, ,$$

and the result follows.


<!-- p:139 -->


7

### Signal-to-Interference Ratio Coverage

## 7.1 Introduction

Let  = Σiε(xi,mi,ti) be a marked point process, with points {xi} in Rd and marks {mi} in Rl (as in Chapter 5) and ti ∈ R+. As in Chapter 5, let I(y) be the SN on Rd, generated by  = Σiε(xi,mi) (i.e.,  without the marks ti) and by the response function L: Rd × Rd × Re → R+.

Definition 7.1. We define the SINR coverage process generated by and the thermal noise field w(y) ≥ 0, as the following union of SINR cells:

$$\Xi _ { \sin R } & = \Xi ( \widehat { \Phi } , w ) \\ & = \bigcup _ { ( x _ { i } , m _ { i } , t _ { i } ) \in \widehat { \Phi } } C _ { ( x _ { i } , m _ { i } ) } ( \widetilde { \Phi } - \varepsilon _ { ( x _ { i } , m _ { i } ) } , w , t _ { i } ) \\ & = \{ y \colon \text {there exist } ( x _ { i } , m _ { i } , t _ { i } ) \in \widehat { \Phi } \colon L ( y , x _ { i } , m _ { i } ) \\ & \geq t _ { i } ( I _ { \widetilde { \Phi } } ( y ) - L ( y , x _ { i } , m _ { i } ) + w ( y ) ) \} .$$


<!-- p:140 -->


Remark. From Remark 6.1, C(xi,mi)(δ − ε(xi,mi), w,ti) in (7.1) is equal to C(xi,mi)(Φ, w, ti) with

$$t _ { i } ^ { \prime } = \frac { t _ { i } } { 1 + t _ { i } } \, .$$

Moreover, if ti &gt; 0 for all i, then EsinR can also be expressed as

$$\Xi _ { \sin R } = \{ y \colon X _ { \widehat { \Phi } } ( y ) \geq I _ { \widetilde { \Phi } } ( y ) + w ( y ) \} \, ,$$

where

$$X _ { \widehat { \Phi } } ( y ) = \max _ { ( x _ { i } , m _ { i } , t _ { i } ) \in \widehat { \Phi } } \left ( \frac { L ( y , x _ { i } , m _ { i } ) } { t _ { i } } \right )$$

is a max-shot-noise process generated by  and the response function L(y, x, m, t) = L(y, x, m)/t (cf. Section 2.4), provided the max is well defined, for example when there is an a.s. finite number of cells covering point y.

Standard Stochastic Scenario and Kendall-like Notation. We shall often consider the following standard scenario for the coverage process.

- (1) We assume that  is a general stationary independently marked point process with points in R2 and intensity λ &gt; 0.
- (2) The marks (mi = (pi, ti)) have some given distribution P{p ≤ u, t ≤ v } = G(u, v) that does not depend on the location of the corresponding point.
- (3) The thermal noise field w(y) = W is constant in space and equal everywhere to some non-negative random variable W ≥ 0 independent of .

Note that assumptions (1) and (2) correspond to some natural extension (marks ti are added) of the standard scenario for SN, for which the following isotropic response function L(y, x, p) = p/l(|y − x|) is assumed, with l some omni-directional power attenuation function (see Section 23.1.2 in Volume II).

Extending our previous Kendall-like notation to SINR coverage, we call the above scenario the W+GI/GI GI/GI model.


<!-- p:141 -->


Fig. 7.1 SINR coverage model without fading.

M/D Figure 7.1 shows a realization of the SINR coverage model W+M/D while Figure 7.2 shows the same situation with an independent fading for each point.

## 7.2 Typical Cell of the Coverage Process

Let P(x,m,) denote the reduced Palm distribution of  (see Section 1.4). Recalì that one can consider this distribution as the conditional distriSINR cell C(x,m,t) (, w,t) is called the typical cell of the coverage process 三SINR at (x, m, t).1

From Corollary 2.2, in the case of an i.m.p.p., P!x is also the dis(x,m,t) tribution of an independently marked point process with marks having the original distribution.

1 The name "typical cell" is natural in the stationary case.


<!-- p:142 -->


Fig. 7.2 SINR coverage model with point dependent fading.

If moreover  is an i.m. Poisson p.p. then by Slivnyak's Theorem is equal to the original Poisson distribution of . Moreover, the moment measure M of  is equal to

$$\widehat { M } ( d ( x , m , t ) ) = F ( d ( m , t ) ) \Lambda ( d x ) ,$$

where Λ is the intensity measure of the Poisson p.p. Φ. This allows us to interpret many results obtained in Chapter 5 for a single SINR cell as concerning the typical cell of the SINR coverage process EsiNR with (possibly) a randomized mark P. Note also that Assumption (3) of the standard scenario for SINR cells states that P is randomized according to its original generic distribution.

## 7.3 Nearest Transmitter Cell

Consider a GI/GI model. We are interested in the probability that a W+GI/GI given location, say the origin y = 0, is covered by the cell of the nearest transmitter:


<!-- p:143 -->


$$p _ { * } & = \Pr \left \{ y \in C _ { ( x ^ { o } , p ^ { o } ) } ( \widetilde { \Phi } - \varepsilon _ { ( x ^ { o } , p ^ { o } ) } , W , t ) \right \} \\ & = \Pr \left \{ p ^ { o } \geq l ( | x ^ { o } | ) t ( W + I _ { \widetilde { \Phi } } ( y ) - p ^ { o } / l ( | x ^ { o } | ) ) \right \} ,$$

where xo = arg minxi∈Φ |xi| (by Lemma 4.2, x0 is almost surely well defined) and po is the mark of x* in . In the case of Poisson p.p., the joint distribution of (x*, p*) and  − ε(xo,po) is known. Thus, conditioning on x*, one can evaluate p* by similar arguments as po(y) (see Section 5.3.1). These calculations are explicit in the M/M model. W+M/M

M/M Proposition 7.1. For the model with deterministic ti = t W+M/M

$$w + & M / M \\ p _ { * } & = \int _ { 0 } ^ { \infty } 2 \pi \lambda r \exp ( - \lambda \pi r ^ { 2 } ) \mathcal { L } _ { W } ( \mu t l ( r ) ) \\ & \times \exp \left ( - 2 \pi \lambda \int _ { r } ^ { \infty } \frac { u } { 1 + l ( u ) / ( t l ( r ) ) } \, d u \right ) d r ,$$

where E[p0] = 1/μ.

Proof. Recall that P{ |xo| &gt; r} = e−λπr2. Moreover, given xo = r,  − ε(xo,po) is an i.m. Poisson p.p. with intensity λ1(|x| &gt; r) and independent of p*. Thus conditioning on |x0| = r, by the same arguments as in the proof of Proposition 5.5, the coverage probability is equal to

$$\mathcal { L } _ { W } ( \mu t l ( r ) ) \exp \left ( - 2 \pi \lambda \int _ { r } ^ { \infty } \frac { u } { 1 + l ( u ) / ( t l ( r ) ) } \, d u \right ) .$$

We obtain the result by integrating with respect to the law of |xo|.

Example 7.2. Consider OPL 3 with β = 4 and W ≡ 0. Then using the fact that

$$\int _ { r } ^ { \infty } \frac { u } { 1 + l ( u ) / ( t l ( r ) ) } \, d u = \frac { r ^ { 2 } } { 4 } \sqrt { t } ( \pi - 2 \arctan ( 1 / \sqrt { t } ) ) ,$$

we get that

$$p _ { * } = \int _ { 0 } ^ { \infty } 2 \pi \lambda r \exp \left ( - r ^ { 2 } \lambda \pi \left ( 1 + \frac { 1 } { 2 } \sqrt { t } ( \pi - 2 \arctan ( 1 / \sqrt { t } ) ) \right ) \right ) d r . \\$$


<!-- p:144 -->


## 7.4 ESINR as a Random Closed Set

We now consider some stochastic-geometry theoretic properties of SINR coverage processes. We require that the typical cell be a closed set for M(d(x, m,t)) almost all (x, m, t) ∈ Rd × Rl × R+. By Campbell's formula, one can then conclude that under the original (unconditional) distribution of 三sINR, all the cells C(xi,mi)( − ε(xi,mi), w, ti) are almost surely closed sets. In the case of an i.m.p.p., conditions for the typical cell to be a closed set can hence be found in Corollary 5.2.

In stochastic geometry it is customary to require EsiNR to be a closed set (note that the countable union of closed sets need not be closed). In fact, we require the stronger property that for any given bounded set in Rd (with compact closure), the number of cells that have non-empty intersection with it is almost surely finite.2

Denote by NK the random number of cells

$$C _ { i } = C _ { ( x _ { i } , m _ { i } ) } ( \widetilde { \Phi } - \varepsilon _ { ( x _ { i } , m _ { i } ) } , w , t _ { i } )$$

that hit a given bounded set K

$$N _ { K } = \sum _ { i } \mathbb { I } ( K \cap C _ { i } \neq \emptyset ) .$$

In what follows, we assume that  is an i.m. Poisson p.p. and we give several instances of moment-conditions (bearing on the distribution F(d(m, t)) of the generic mark (m, t) and the intensity measure Λ of the p.p.) for E[Nk] to be finite for arbitrary large K. Later on we will comment on the general stationary case as well.

Note first that the required property is always satisfied if Λ(Rd) &lt; ∞ (i.e. when  has almost surely a finite number of points in Rd). In the following, we will assume one of the two following conditions on the

2An equivalent statement is that the collection of cells is a.s. a Radon point measure on the space of closed sets, so that it can be treated as a point process

$$\sum _ { ( x _ { i } , m _ { i } , t _ { i } ) } \varepsilon _ { C _ { i } }$$

on the space of closed sets. This is a typical assumption for coverage processes (in particular for the Boolean model, see e.g. [42], Equation (3.1.1), p. 59).


<!-- p:145 -->


response function:

- (A1) There exists a finite real number R*, such that L(y, x, m) = 0 for all m ∈ Rl and y, x ∈ Rd with |y − x| &gt; R*.
- (A2) There exist positive constants A and β such that L(y, x, m) ≤ A|s|z|−β, for all y,x ∈ Rd, s ∈ Re, where |·| denotes the Euclidean norm.

Note that condition (A2) is satisfied for the standard scenario with OPL 1 and OPL 2.

Proposition 7.3. Let  an be i.m. Poisson p.p. with intensity Λ. Assume that ti &gt; 0 a.s. We have

$$E [ N _ { K } ] < \infty$$

for an arbitrary large K if one of the following conditions holds:

- (i) Condition (A1) is satisfied and w(x) &gt; 0 for all x ∈ Rd with probability 1,
- (ii) Condition (A2) is satisfied, w(t) ≥ W &gt; 0 a.s. for some (possibly random) variable W, and for all R &gt; 0

$$\mathbb { E } \left [ \Lambda \left ( B \left ( 0 , R + \left ( \frac { A | m _ { 0 } | } { t _ { 0 } W } \right ) ^ { 1 / 3 } \right ) \right ) \right ] < \infty .$$

- (iii) Condition (A2) is satisfied, L(y, x, m) &gt; 0 a.s. for all y ∈ Rd, and for all R &gt; 0

$$\int _ { \mathbb { R } ^ { d } } e ^ { - \Lambda ( B ( 0 , | x | ) ) } E \left [ \Lambda \left ( B \left ( 0 , R + \left ( \frac { A | m _ { 1 } | } { t _ { 1 } \underline { L } ( R , x , m _ { 0 } ) } \right ) ^ { 1 / \beta } \right ) \right ) \right ] \\ \times \Lambda ( d x ) < \infty ,$$

where m0 is independent of (m1,t1), with both having the distribution of the marginals of a typical mark, and L(r, x, m) = infy:|y|≤r L(y, x, m).


<!-- p:146 -->


Proof. In order to prove (7.8), we construct various Boolean models dominating our coverage process EsinR and we use Lemma 3.1 to ensure that the number of cells of the Boolean model which intersect K is of finite mean, which is equivalent to

$$E [ \Lambda ( \breve { \Xi } \oplus K ) ] < \infty \, ,$$

where Ξ is the generic grain of the BM.

- (i) Under (A1), we have Ci ⊂ B(Xi, R*) and the result follows from the fact that (7.11) is obviously finite for the Boolean model with deterministic cells.
- (ii) Under (A2) we have

$$( i ) & \text { Under (A2) we have } \\ & C _ { i } = \left \{ y \colon L ( y , x _ { i } , m _ { i } ) \geq t _ { i } ( I _ { \widetilde { \Phi } } ( y ) - L ( y , x _ { i } , m _ { i } ) + w ( y ) ) \right \} \\ & \subset \left \{ y \colon L ( y , x _ { i } , m _ { i } ) \geq t _ { i } W \right \} \\ & \subset \left \{ y \colon A | m _ { i } | \, | y - x _ { i } | ^ { - \beta } \geq t _ { i } W \right \} \\ & \subset \left \{ y \colon | y - x _ { i } | \leq \left ( \frac { A | m _ { i } } { t _ { i } W } \right ) ^ { 1 / \beta } \right \} . \\ \text { Thus, we have } C _ { i } \subset B ( x _ { i } , \rho _ { i } ) , \, a . s . , \, \text { where }$$

Thus, we have Ci ⊂ B(xi, ρi) , a.s., where

$$\rho _ { i } = \left ( \frac { A | m _ { i } | } { t _ { i } W } \right ) ^ { 1 / \beta } .$$

There is no loss of generality in assuming that the bounded set K is the ball B(0, R) and the result now follows from the simple observation that B(0, R) ⊕ B(0, ρi) = B(0, R + ρi).

- (iii) Now we do not assume anything about w(t) (thus it may by positive or null). Instead we use one of the points of the process Φ to guarantee a sufficient level for the variable I and thus bound cell sizes from above. Let x0 denote the point of Φ which is nearest to the origin, and let m0 be its mark.


<!-- p:147 -->


We have

$$N _ { K } & = 1 ( K \cap C _ { 0 } \neq \emptyset ) + \sum _ { i \neq 0 } 1 ( K \cap C _ { i } \neq \emptyset ) \\ & \leq 1 + \sum _ { i \neq 0 } \mathbb { 1 } ( K \cap C _ { i } \neq \emptyset ) .$$

For any point xi ≠ x0 (i.e., |xi| &gt; |xo|) of the point process, with mark mi, ti, and K = B(0, R)

$$with \, \text {mark} \, m _ { i } , t _ { i } , \, \text {and} \, K & = B ( 0 , R ) \\ C _ { i } ( \Phi ) \cap K & \subset \left \{ y \colon | y | \leq R \text { and } | y - x _ { i } | \leq \left ( \frac { A | m _ { i } | } { t _ { i } L ( y , x _ { 0 } , m _ { 0 } ) } \right ) ^ { 1 / \beta } \right \} \\ & \subset \left \{ y \colon | y - x _ { i } | \leq \left ( \frac { A | m _ { i } | } { t _ { i } \inf _ { y , \, | y | \leq R } L ( y , x _ { 0 } , m _ { 0 } ) } \right ) ^ { 1 / \beta } \right \} \\ & \subset B ( x _ { i } , \rho ( R , m _ { i } , t _ { i } , x _ { 0 } , m _ { 0 } ) ) \ , \\ \text {where}$$

where

$$\rho ( R , m _ { i } , t _ { i } , x _ { 0 } , m _ { 0 } ) = \left ( \frac { A | m _ { i } | } { t _ { i } L ( R , x _ { 0 } , m _ { 0 } ) } \right ) ^ { 1 / \beta } .$$

Using now (7.13) and the assumption that x0 is the point nearest to the origin, we get

$$\text {using now (7.13) and the assumption that } x _ { 0 } \text { is the point
    nearest to the origin, we get
    \\ E [ N _ { K } ] \leq E \left [ 1 + \sum _ { i \neq 0 } 1 ( K \cap C _ { i } \neq \emptyset ) \right ] \\ = E \left [ \int _ { \mathbb { R } ^ { d } } \left ( \Phi ( B ^ { o } ( 0 , x _ { 0 } ) ) = 0 \right ) \\ \times \left ( 1 + \sum _ { i \neq 0 } 1 ( K \cap C _ { i } \neq \emptyset ) \right ) \Phi ( d x _ { 0 } ) \right ] \\ \leq \int _ { \mathbb { R } ^ { d } } e ^ { - \Lambda ( B ( 0 , | x _ { 0 } | ) ) } \\ \times E \left [ 1 + \sum _ { i , \ | x _ { i } | > x _ { 0 } } 1 ( K \cap B ( x _ { i } , \rho ( R , m _ { i } , t _ { i } , x _ { 0 } , m _ { 0 } ) ) \neq \emptyset \right ] \\ \Lambda ( d x _ { 0 } ) \, .$$


<!-- p:148 -->


So by (7.11) for the Boolean model with Gi = B(0, ρ(R, mi, ti, x0, m0)) conditioned on x0, m0

$$E [ N _ { K } ] & \leq \int _ { \mathbb { R } ^ { d } } e ^ { - \Lambda ( B ( 0 , | x _ { 0 } | ) ) } \\ & \times E \left [ 1 + \Lambda \left ( K \oplus B \left ( 0 , \rho ( R , m _ { 1 } , t _ { 1 } , x _ { 0 } , m _ { 0 } ) \right ) \right ) \right ] \Lambda ( d x ) \, .$$

The proof is concluded by observing that B(0, R) ⊕ B(0, ρ(· · ·)) = B(0, R + ρ(· ··)). □

Corollary 7.4. Let Φ be an independently marked and homogeneous Poisson p.p. with intensity Λ(dx) = λdx. Then (7.9) is equivalent to the following condition

$$E \left [ \left ( \frac { | m _ { 0 } | } { t _ { 0 } W } \right ) ^ { d / \beta } \right ] < \infty ,$$

whereas (7.10) is equivalent to the conjunction of the following two conditions

$$\text {conditions} \\ \int _ { \mathbb { R } ^ { d } } e ^ { - \lambda \nu _ { d } | x | ^ { d } } \left ( E [ \underline { L } ( R , x , m _ { 0 } ) ] \right ) ^ { - d / \beta } d x < \infty , \quad E \left [ \left ( \frac { | m _ { 0 } | } { t _ { 0 } } \right ) ^ { d / \beta } \right ] < \infty . \\$$

Remark. Conditions analogous to parts (i) and (ii) of Proposition 7.3 can be observed in the stationary ergodic case; (7.9) and (7.14) have the same form with E[. . .] replaced with E0[. . .], where E0 is the expectation w.r.t. the Palm distribution of the mark (mo, t0). The proof is based on Campbell's formula. Part (iii) has no generalization due to the lack of an explicit form of the joint distribution of xo (the point which is nearest to the origin) and the remaining part of a general point process.

## 7.5 The Coverage Process Characteristics

Our goal in this section is to analyze the coverage process EsinR, and more specifically, the distribution of the number of cells covering a given point. From this, the volume fraction and other characteristics of 3sINR can be derived. Let Nx = N{x} (cf. (7.7)) denote the number of cells covering a given point x. For all integers k, let k(n) = k(k − 1) . . . (k − n + 1)+, where k+ = max(0, k). Below, we give formulae for be derived using the formula


<!-- p:149 -->


$$P ( N _ { x } = n ) = \frac { 1 } { n ! } \sum _ { k = 0 } ^ { \infty } ( - 1 ) ^ { k } \frac { \mathbf E [ N _ { x } ^ { ( n + k ) } ] } { k ! } ,$$

which follows from the well-known expansion of the generating function. Of course, these expansions usually require strong conditions (existence of all moments and convergence of the series). However, these issues disappear when Nx is bounded.

### 7.5.1 Bounded Nx

Suppose now that the distribution of the marks is such that ti are bounded away from 0, i.e.

(B) ti ≥ ρ a.s. for some constant ρ &gt; 0.

Using the result of Proposition 6.2, we immediately have the following property of the coverage process:

Corollary 7.5. If Condition (B) is satisfied then Nx &lt; 1/ρ almost surely.

Proof. Assume that n = Nx cells cover point x. Then from Proposition 6.2, Σk=1 tik ≤ 1, where tik, k = 1,... n are marks of the cells covering x. Since tik ≥ ρ, so n ≤ 1/ρ. □

Remark. This bound suggests an analogy with queueing theory. One can think of queueing theory as a way of sharing time between customers arriving at a queue according to some point process on the line, and requiring some given service times. We can also think of our coverage process as a way of sharing space between the points of a spatial point process with given marks. Under the condition mentioned in the last lemma, the coverage process can be seen as a spatial analogue of the l-server queue, with l = min{n integer : n ≥ 1/ρ}, in that no point in space can be covered by more than l cells; in the same way, the lserver queue forbids that at any point in time, more than l-customers could be served. Note that sharing actually means quite different things here and there: in queues, the sharing of time is implemented by shifting customers in excess to later times, while keeping their service times unchanged. In contrast, for this coverage process, sharing of space is obtained by shrinking the marks: if one defines the space request of point (0) x0 as the set C = {y: L(y, x0, m0) ≥ t0w(y)}, which would be the share of space obtained by x0 if there were no other points, then one can se '{((h)m + (0u0x h)T − (h)Φ1)0q (0u0x 'h)T :h} = 0 təs ə7 əs resulting from the competition with the other points.


<!-- p:150 -->


In the same vein, the Boolean model, which is a limiting case of our coverage process (see Section 5.5.1), can also be seen as a spatial analogue of the infinite server queue, and that in this case, the analogy is quite strong, with in particular the same Poisson distribution for the number of marks (customers or cells) covering a given (time or space) point.

### 7.5.2 Factorial Moments of Nx

We are now in a position to prove the following result.

Proposition 7.6. Assume  is a simple i.m. Poisson p.p. with intensity measure Λ. Then the nth factorial moment of the number Nx of cells of EsInR(Φ) covering point x is equal to

$$E [ N _ { x } ^ { ( n ) } ] & = \int _ { ( \mathbb { R } ^ { d } ) ^ { n } } \mathbf P \left ( x \in \bigcap _ { k = 1 } ^ { n } C _ { ( x _ { k } , m _ { k } ) } \left ( \widetilde { \Phi } + \sum _ { i = 1 , i \neq k } ^ { n } \varepsilon _ { ( x _ { i } , m _ { i } ) } , w ( y ) , t _ { i } \right ) \right ) \\ & \quad \Lambda ( d x _ { 1 } ) \cdots \Lambda ( d x _ { n } ) ,$$

where  is distributed as  without marks ti and {(mi, ti)}i=1 are mutuirt t t er   rnt r  re mark. This relation holds provided the integral on the right hand side is finite. In particular, if  is a homogeneous Poisson p.p. with intensity


<!-- p:151 -->


Λ(dx) = λdx then for each x ∈ Rd

$$E [ N _ { x } ] = \lambda E \left [ | C _ { ( x , m _ { 0 } ) } ( \widetilde { \Phi } , w ( y ) , t _ { 0 } ) | \right ] ,$$

where |C| is the d-dimensional volume of the cell C.

Proof. For a particular realization  of the marked Poisson p.p, denote by (n) its nth factorial power, that is the following point measure on (Rd × Re × R+)n

$$\widehat { \Phi } ^ { ( n ) } & = \sum _ { \substack { x _ { 1 } , \dots , x _ { n } \in \Phi \\ \text {distinct} } } \varepsilon _ { ( x _ { 1 } , \dots , x _ { n } ) , ( m _ { i _ { 1 } } , \dots , m _ { i _ { n } } ) , ( t _ { i _ { 1 } } , \dots , t _ { i _ { n } } ) ) } . \\ & \widehat { \widehat { \Phi } } ( x )$$

In other words, (n) consists of all n-tuples of distinct points of  (see Chapter 9). Now we can write the factorial power (Nx)(n) of the number cells covering point x as the following integral with respect to (n)

$$C e C o r v e r g \, p o r \, x \, u s \, \text {circ} \, N o w i n \, T e p s e c t \, u s \, T e p s e c t \\ N _ { x } ^ { ( n ) } = \int _ { ( \mathbb { R } ^ { d } ) ^ { n } } \prod _ { k = 1 } ^ { n } 1 ( x \in C _ { ( x _ { k } , m _ { k } ) } ( \widetilde { \Phi } , w ( y ) , t _ { i } ) ) \\ \times \widehat { \Phi } ^ { ( n ) } ( d ( ( x _ { 1 } , \dots , x _ { n } ) , ( m _ { 1 } , \dots , m _ { n } ) , ( t _ { 1 } , \dots , t _ { n } ) ) . \ \ ( 7 . 1 9 ) \\$$

We get (7.17) by applying the refined Campbell theorem to the (see -or a t   a s  dx  reo rial moment measures of Poisson processes are Lebesgue measures (Proposition 9.1). □

Remark. For the finiteness of the integral that appears in Proposition 7.6, it is enough to assume exactly the same conditions as for the σ-finiteness of the mean measure of ΣiεCi given in Proposition 7.3 parts (i) and (ii). In the case P(w(y) = 0) &gt; 0, however, some integrals of the negative moments of order nd/α of L(y, x0, m) have to be finite, where x0 is the point which is nearest to the origin. Details can be found in [1].

### 7.5.3 Volume Fraction

The volume fraction p = P(0 ∈ 三siNR) is a basic characteristic of a stationary coverage process. Strictly speaking, it can be defined and calculated for any coverage process, but then the notion might be misleading, since it is only when we assume that the probability P(x ∈ EsinR) does not depend on x, that we can say that the expected fraction of the d-dimensional volume of EsiNR per unit ball is equal to p (cf. the remark after Definition 3.4). Thus for the remaining part of this section, we assume that Φ is a homogeneous Poisson p.p. with intensity λ, that the function L(y, x, m) = L(y − x, 0, m) depends only on (|x − y|, m)) and that w(y) is stationary. Using the expansion (7.16) we can write p = ∑k=1(−1)k+1/k!E[(N0)(k)], where the coefficients are given in Proposition 7.6, provided all moments are finite and the series is convergent. Note however, that if we assume condition (B) of Section 7.5.1 (ti ≥ ρ &gt; 0 a.s.), then the expansion has only finitely many non-zero terms.


<!-- p:152 -->


Note that the dependent marking of our coverage process (cells are dependent) makes it impossible to calculate the volume fraction in the way typically used for Boolean models. Nevertheless using the factorial moment expansion technique for a general class of functionals of spatial p.p.s presented in [4] (see also references therein), the first order approximation of the volume fraction can be represented as

$$p = \lambda \int _ { \mathbb { R } ^ { d } } p _ { 0 } ( x ) \, d x + O ( \lambda ^ { 2 } ) = \lambda \mathbf E [ | C _ { ( 0 , M ) } | ] + O ( \lambda ^ { 2 } ) \, ,$$

where po(x) is the single (typical) cell coverage probability and E[|C(0,M)|] is the expected volume of the typical cell. The first term in the last formula differs from the formula (7.18) for E[N0] only in that  is replaced by the null measure (without points). More general approximation formulae (involving polynomials in λ) can be obtained via this expansion technique.

### 7.5.4 Noise or Interference Limited Coverage — Extremal Cases

The aim of this section is to extend the results of Section 5.5 on the convergence of cells Ci towards, e.g. those of the BM or those of a VT to the convergence of the whole SINR coverage process.

Noise Limited Cells — Towards a Boolean Model. By analogy to what was done in Section 5.5.1 consider the following family of SINR


<!-- p:153 -->


coverage processes

where

$$C _ { i } ^ { ( \kappa ) } = \{ y \colon L ( y , x _ { i } , m _ { i } ) \geq t ( \kappa ( I _ { \widetilde { \Phi } } ( y ) - L ( y , x _ { i } , m ) ) + W ) \} .$$

Note that (for simplicity) we have assumed a random noise W which is constant in space, but possibly random.

Proposition 7.7. Assume that the conditions of Corollary 5.2 with w(y) = W are satisfied as well as Condition (1) in Section 5.5.1. Then, almost surely on the space of closed sets, limκ→0 3SINR = 3 =(κ) =(0) =SINR (Painlevé-Kuratowski convergence), provided 三 SINR (κ) is a random closed set for κ ∈ [0, κ0] and some κ0 &gt; 0.

Proof. Observe that

$$\overline { \bigcup _ { \kappa } \Xi ^ { ( \kappa ) } } = \overline { \bigcup _ { \kappa \ i } C _ { i } ^ { ( \kappa ) } } = \overline { \bigcup _ { i } \overline { \bigcup _ { \kappa } C _ { i } ^ { ( \kappa ) } } } = \overline { \bigcup _ { i } C _ { i } ^ { ( 0 ) } } = \bigcup _ { i } C _ { i } ^ { ( 0 ) } ,$$

where the last but one equality follows from (5.9) and the last one from (0) the assumption that 3 SINR is a closed set. □

Remark. Suppose that  is an independently marked Poisson point process. Then 3sINR given W is a Boolean model with grains (0) γ(0) i {y : L(y, xi, mi) ≥ tiW }.

Example 7.8. We now illustrate Proposition 7.7 by showing some patterns of our coverage process EsiNR "conforming" to a Boolean model pattern. We simulated a Poisson p.p. with 60 points on the square [−5,15]2 (so that λ = 0.15). While observing only the square [0, 10]2, we take all 60 points of the larger square into account for evaluating I. We assume the standard scenario for the coverage process with the OPL function (1 + |y|)3. The pi's are uniformly distributed

$$\Xi _ { S I N R } ^ { ( \kappa ) } = \bigcup _ { i } C _ { i } ^ { ( \kappa ) } \, ,$$


<!-- p:154 -->


- ao aut tnd r o  ≡  n I   ] ing various values for κ. Figure 5.2 presents the coverage process ΞsiNR "on its way" to a Boolean model. We have: (a) κ = 0.4; note that 2κ &lt; 1 &lt; 3κ; thus at most two cells could cover any given point, although this is not observed; (b) κ = 0.2; since 4κ &lt; 1 = 5κ, at most four cells could cover any given point; (c) κ = 0.1; cells occupy more and more of the final space that they occupy under the Boolean model regime; (d) κ = 0.0001; almost the limiting case where each cell is a disc with independent radius distributed as (10p)1/3 – 1 (with mean 201/3 × 3/4 − 1 ≈ 1.035).

Here is an extension of Proposition 5.14. Denote D(x,m,t) = {y: L(y, x, m) = tW}.

Proposition 7.9. Suppose that the conditions of Proposition 7.7 are satisfied. If for a given compact K ∈ Rd

$$\times \widehat { M } ( \mathbf d ( x , m , t ) ) = 0 \, ,$$

where Z = (S, (a, b, c)) is a generic mark, then as κ ↓ 0, the number of cells NK(≡SINR) hitting set K converges almost surely and in expecta(κ) tion to the number of cells of 三 (0) hitting K. SINR

Proof. Note that under assumption (7.21) the (expected) number of points of  not satisfying (5.10) is equal to 0. Thus by Proposition 5.14

$$\lim _ { \kappa \to 0 } N _ { K } ( \Xi _ { S I N R } ^ { ( \kappa ) } ) = \lim _ { \kappa \to 0 } \sum _ { i } 1 ( K \cap C _ { i } ^ { ( \kappa ) } \neq \emptyset ) = \sum _ { i } 1 ( K \cap C _ { i } ^ { ( 0 ) } \neq \emptyset ) . \quad \square$$

Corollary 7.10. Suppose that  is an i.m. Poisson point process. Then under the assumptions of Proposition 7.7 we have the following convergence of the capacity functional:

$$\lim _ { \kappa \to 0 } & P \{ \Xi _ { S I N R } ^ { ( \kappa ) } \cap K \neq 0 \} \\ & = 1 - \exp \left [ \int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { R } ^ { \ell } } \int _ { \mathbb { R } ^ { + } } \P ( K \cap C _ { ( x , m , t ) } ^ { ( 0 ) } \neq \emptyset ) \, \widehat { M } ( d ( x , m , t ) ) \right ] .$$

$$\frac { = 1 - \exp \left [ \int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { R } ^ { \ell } } \int _ { \mathbb { R } ^ { + } } \mathbb { 1 } ( K \cap C _ { ( x , m , t ) } ^ { ( 0 ) } \neq \emptyset ) \, \widehat { M } ( d ( x , m , t ) ) \right ] .$$


<!-- p:155 -->


Nearest-interferer Limited Cells — Towards the Voronoi TesCn is the SINR cell Cn = Cn (xi,pi) i)( − ε(xi,pi), 0, ti) obtained for the OPL 2 function ln(r) = (1 + r)n and for W ≡ 0. Similarly to Proposition 5.20 we have the following result:

Proposition 7.11. Assume that  is simple. Then for all i

$$\lim _ { n \to \infty } C _ { i } ^ { n } = \mathcal { C } _ { x _ { i } } \, ,$$

almost surely on the space of closed sets (Painlevé-Kuratowski convergence), where Cxi = Cxi (Φ) is the Voronoi cell of xi generated by Φ, provided Cn is a (random) closed set for sufficiently large n.

Also the mean volume of the SINR cell can be approximated by the mean volume of the Voronoi cell, as in Proposition 5.21.

Example 7.12. We now illustrate Proposition 7.11 by showing some patterns of our coverage process EsiNR "conforming" to the Voronoi tessellation of the plane (see Figure 5.3). The Poisson p.p., the observation and the simulation windows are as in Example 7.8. Marks pi are uniformly distributed on [0, 2], W ≡ 0, ti ≡ 0.2 thus allowing for at most four cells to overlap at a given point. The various patterns result from taking the OPL function l(r) = (1 + r)n with various n. We have: (a) n = 3, (b) n = 5, (c) n = 12, (d) n = 100. The effect of overlapping is still visible. A more accurate tessellation can be obtained inhibiting overlapping, e.g., by taking ti ≡ 0.5.

Nearest-interferer and Noise Limited Cells — the JohnsonMehl Model. When a strong attenuation remains in some relation to the noise then the SINR coverage process might look like a subtessellations, with each of its cells constrained to remain within some disc with the diameter related to the noise.

Example 7.13. We now illustrate Corollary 5.22 by showing some patterns of our coverage process EsiNR "growing" to the Voronoi tessellation as in the Johnson-Mehl model (see Figure 5.4). The observation and simulation windows and the Poisson p.p. are as in the previous examples. Marks pi are uniformly distributed on [0, 2] and we take ti ≡ 0.5, thus inhibiting any intersections. The OPL function l(y) = (1 + |y|)30 is strong enough to give a tessellation covering almost the whole plane when W ≡ 0. We assume W = (1 + R)−30 and take: (a) R = 0.4, (b) R = 1.2, (c) R = 2, (d) R = ∞ (equivalent to W ≡ 0). The result is a sequence of sub-tessellations, with each of the cells constrained to a disc of radius R (wherever a cell has diameter less than R it has its final shape). All cells start growing at the same time.


<!-- p:156 -->


### Signal-to-Interference Ratio Connectivity

## 8.1 Introduction

Consider a marked point process  = Σiε(xi,mi,ti) as in Chapter 7 and the coverage process EsiNR = UiCi it generates, where Ci is the SINR cell of the point (xi, mi) for the SINR threshold ti (see (7.6) in Chapter 7).

Suppose that the points of this point process constitute a network, in which one node is able to communicate with other nodes of the network, possibly via several hops (e.g., a MANET − see Section 25.3.1 in Volume II). Suppose that the communication from xi to xj is feasible if xj ∈ Ci. Important questions then arise about the connectivity of the SINR model EsinR. They are similar to those concerning the connectivity of the Boolean model studied in Section 3.2. Recall that the connectivity of the Boolean model in the whole plane (space) is analyzed using percolation theory, in which setting the central question is the existence of an infinite connected component.

## 8.2 Signal-to-Interference Ratio Graph

Consider the following graphs associated with the SINR model 三siNR generated by a marked point process .


<!-- p:157 -->


Definition 8.1. Let Ci be defined by (7.6), Chapter 7.

- The directed SINR graph GS1N GsINR is the graph with vertices, the atoms of Φ and with directed edges from xi to xj if xj ∈ Ci.
- The bidirectional SINR graph GsiNR is the graph with vertices the atoms of Φ and with non-directed edges between xi and xj if xj ∈ Ci and xi ∈ Cj.

In this chapter we concentrate on the latter, which can be described in other words as the graph where two points of Φ are connected iff they cover each other by their respective SINR cells.

Definition 8.2. One says that the SINR graph GsiNR percolates if it contains an infinite connected component.

Remark. As already explained, the interest of percolation is to maintain simultaneous links allowing one to build routes between any pair of nodes belonging to the infinite component. Let us note that in spite of its mathematical interest, this percolation model has one main practical drawback that stems from the technical difficulty of having a node being at the same time a transmitter and a receiver on the same frequency band. This problem is taken care of in Chapter 22 in Volume II, where we consider time-space routing schemes where receivers and transmitters form a partition of the set of nodes.

## 8.3 Percolation of the Signal-to-Interference Ratio Connectivity Graph

M/D Consider the model (see Chapter 7), i.e., the model generated W+M/D by a homogeneous Poisson p.p. of the plane with intensity λ, marked by constant emitted powers pi = p and SINR thresholds ti = t. We assume moreover that the noise w(y) = w is spatially constant and deterministic. We consider the response function given by L(y, x, p) = p/l(|y − x|), where l is some OPL function satisfying the following conditions:


<!-- p:158 -->


- (1) l(r) ≥ 1,
- (2) l is continuous and strictly increasing (when finite),
- (3) l(0) &lt; p/(tw),
- (4) ∫∞ r/l(r) dr &lt; ∞.

Note that the condition (3) is necessary for the SINR cell Ci to contain some neighborhood of its nucleus xi (even in the absence of interference), while condition (4) guarantees that the SN generated by the underlying marked p.p. and the response function is almost surely finite.

Under the above assumptions, we consider the parametric family of SINR coverage processes

$$\Xi _ { S I N R } ^ { ( \kappa ) } = \bigcup _ { i } C _ { i } ^ { ( \kappa ) } ,$$

where

$$C _ { i } ^ { ( \kappa ) } = \{ y \colon p / l ( | y - x _ { i } | ) \geq t \left ( \kappa ( I _ { \tilde { \Phi } } ( y ) - p / l ( | y - x _ { i } | ) ) + w \right ) \} .$$

From Section 7.5.4 (see Proposition 7.7 and the remark following it), converges monotonically to the spherical cell i

$$C _ { i } ^ { ( 0 ) } = \{ y \colon | y - x _ { i } | \leq l ^ { - 1 } ( p / ( t w ) ) \}$$

of the Boolean model 三 (0) = Ui C(0), where l−1 is the inverse function SINR of l.

Fixing all other parameters, we denote by GsiNR(λ, κ) the SINR graph corresponding to ESINR· In what follows, we focus on the characterization of the two-dimensional set of parameter values

$$\{ ( \lambda , \kappa ) \colon \mathcal { G } _ { \text {SINR} } ( \lambda , \kappa ) \ p e r c o l a t e s \text { with probability } 1 \} .$$

Since the underlying point process is ergodic, it should be obvious that for the values of (λ, κ) not belonging to the above set, GsinR(λ, κ) percolates with probability 0 (i.e., does not percolate; cf. the proof of Proposition 3.13 concerning the BM). Recall also that the parameter κ stems from interference cancellation technique (see the discussion on the interference cancellation factor at the end of Section 24.3.4 in Volume II). Thus, the above set describes the pairs (density of nodes, interference cancellation factor) for which the infinite network contains an infinite connected component, the nodes of which are able to communicate simultaneously with the bit-rate associated to the SINR threshold t.


<!-- p:159 -->


By monotonicity in κ, for each value of λ &gt; 0, there exists a critical value κ*(λ), such that GsINR(λ, κ) percolates for 0 ≤ κ &lt; κ*(λ) and does not percolate for κ &gt; κ*(λ). The main question is to show whether (and when) this SINR percolation threshold κ*(λ) is strictly positive.

Let λSNR be the critical intensity for the percolation of the Boolean model 三BM(λ, rB) with spherical grains of fixed radii rB = l−1(p/(tw))/2 (see (3.12) of Chapter 3 for the definition of the critical intensity). Note that rB is defined as the half of the radius of the SINR Thus, any two grains of EBM(λ, rB) overlap iff the corresponding vertices of GsinR(λ,0) are connected by an edge.

Note that λSNR represents the critical density of nodes for the existence of the infinite connected component in the SNR network; i.e., in the network where interference between coexisting channels is perfectly (κ) and its Boolean limit 三(0) we have the following immediate property: SINR,

then κ*(λ) = 0, i.e., for all κ ≥ 0, P{ GsINR(λ, κ) percolates } = 0.

Proof. Since (41) ~(0) for all κ ≥ 0 so GSINR(λ, κ) ⊂ GSINR(λ, 0); i.e., the graphs have the same set of edges and the inclusion concerns the set of vertices. The result follows from the fact that GsiNR(λ, 0) percolates iff the Boolean model with spherical grains of the fixed radius rB = l−1(p/(tw))/2 percolates. □

We now state the main result of this section.

Proposition 8.2. For any λ &gt; λSNR, the critical κ*(λ) is strictly positive, i.e., P{ GsINR(λ, κ) percolates } = 1 for all 0 ≤ κ &lt; κ*.


<!-- p:160 -->


Proof. The main ideas of the proof given in [13] are as follows.

- Assuming λ&gt; λSNR, one observes first that the BM 三BM(λ, r0) also percolates for some r0 &lt; rB. This means that the graph GsınR(λ, 0) also percolates with any slightly larger constant noise w′ = w + δ′, for some δ′ &gt; 0.
- Moreover, one can show that the level-set {y:I(y) ≤ M} of the SN field I percolates (contains an infinite connected component) for sufficiently large M. Consequently, taking κ = δ′/M one has percolation of the level-set {y: κIδ(y) ≤ δ′}.
- The main difficulty consists in showing that GsiNR(λ,0) with noise w′ = w + δ′ percolates within an infinite connected component of {y: Iδ(y) ≤ δ'}. This is done by some mapping of the model to a discrete lattice.

the BM ΞBM(λ, rB) with intensity λ and spherical grains of fixed radius rB percolates. Denote by r*(λ) &lt; rB the critical radius for the percolation of the BM ΞBM(λ, r); the existence of such a critical radius follows from Proposition 3.13, by a rescaling argument (cf. Example 1.6). In what follows, we pick some radius r0 ∈ (r*(λ), rB). By assumption, 三BM(λ, r0) percolates.

In what follows, we prove the percolation of some bond-percolation model (cf. Section 14.1). Then we show how this implies the percolation of GsINR(λ, κ) for some κ sufficiently small.

Consider a square lattice of side-length d &gt; 0, whose value is specified later on. One defines two random fields Aa and Ba with values in {0, 1}, where a runs over the set Ld of all vertical and horizontal edges of the above lattice. Let za = (xa, ya) ∈ R2 denote the geometric center of edge a.

- For a denoting a horizontal edge, let Aa be equal to 1 iff the following two conditions are satisfied:
- — the rectangle [xa − 3d/4, xa + 3d/4] × [ya − d/4, ya +d/4] is crossed from left to right by a connected component of 三BM(λ, r0),


<!-- p:161 -->


- — both squares [xa − 3d/4, xa − d/4] × [ya − d/4, ya + d/4] and [xa + d/4, xa + 3d/4] × [ya − d/4, ya + d/4] are crossed from top to bottom by a connected component of 三BM(λ, r0).

For a denoting a vertical edge, the value Aa is defined similarly, by swapping the horizontal and vertical coordinates.

- For a ∈ Ld let Ba = 1 iff Ī(za) &lt; M, where  ̄(z) is the SN generated by the underlying marked Poisson pp  (the one generating ΞsiNR) with the modified OPL function given by

$$\widetilde { l } ( r ) = \begin{cases} l ( 0 ) , & \text {if $0 \leq r \leq \sqrt{1 0} d/4$,} \\ l ( r - \sqrt { 1 0 } d / 4 ) , & \text {otherwise.} \end{cases}$$

The value of the constant M is specified later on.

Note that if a and a' are not adjacent then Aa and Aa' are independent. Consequently, the random field {Aa: a ∈ Ld} defines a onedependent bond (edge) percolation process, where the edge a is open iff Aa = 1. Consequently, using the fact that the probability of the crossing oan res       o o  Bmom converges monotonically to 1 when the sides tend to infinity (see [31, Corollary 4.1]), we get that for any € &gt; 0, one can find some value for the lattice side-length d large enough to ensure that

$$P \{ A _ { a _ { 1 } } = 0 , \dots , A _ { a _ { n } } = 0 \} \leq \epsilon ^ { n }$$

for any set of n different edges a1, . . . , an.

Án          s  ny given side-length d and any € &gt; 0, one can find a value for the constant M large enough for ensuring that

$$P \{ B _ { a _ { 1 } } = 0 , \dots , B _ { a _ { n } } = 0 \} \leq \epsilon ^ { n }$$

for any set of n different edges a1, . . . , an. The proof of this statement is based on the following inequality, which holds true for all s ≥ 0

$$P [ B _ { a _ { 1 } } = 0 , \dots , B _ { a _ { n } } = 0 ] & \leq P \left [ \sum _ { i = 1 } ^ { n } \widetilde { I } ( z _ { a _ { i } } ) > n M \right ] \\ & \leq e ^ { - s n M } E [ e ^ { s \sum _ { i = 1 } ^ { n } \widetilde { I } ( z _ { a _ { i } } ) } ] .$$


<!-- p:162 -->


Note that the last expectation can be interpreted as the value of the Laplace transform of a Poisson p.p. (by changing the order of summation Σi=1 and the sum which defines the SN value Î(zai)). Using the known form of this transform and assumption (4), one can show that for sufficiently small s &gt; 0

$$\mathbf E \left [ e ^ { s \sum _ { i = 1 } ^ { n } \widetilde { I } ( z _ { a _ { i } } ) } \right ] \leq K ^ { n }$$

for some constant K which depends on λ and d and not on M. This completes the proof of (8.4).

Using (8.3) and (8.4) one can show by the Cauchy-Schwartz inequality that for any ∈ &gt; 0, there exist values of the lattice side-length d and of the constant M large enough for ensuring that

$$P \{ A _ { a _ { 1 } } B _ { a _ { 1 } } = 0 , \dots , A _ { a _ { n } } B _ { a _ { n } } = 0 \} \leq \epsilon ^ { n }$$

for any set of n different edges a1, . . , an.

By Peierls' argument (see Proposition 14.1 in Section 14.1.1) this last statement implies that one can find values of d and M such that we have percolation for the bond process on Ld, where the edge a ∈ Ld is open iff Ca = AaBa = 1.

It remains to show that the percolation of the above bond model implies that of GsinNR(λ, κ) for some sufficiently small κ = κ(λ). From the fact that r0 &lt; rB = l−1(p/(tw))/2 and from the strict monotonicity of l, it follows that for all atoms xi,xj of the Poisson p.p. such that their spherical grains of common radius r0 intersect each other, n 0 &lt; ρ os  ( − I)(7)/d  |x − x|)1 p/l(|xi − xj|) ≥ tw/(1 − δ) = t(w + δ′), for some δ′ &gt; 0. Moreover, the existence of the infinite connected component of the bond percolation defined by the field {Ca} implies the existence of an infinite connected component in the intersection of EBm(λ,ro) and the region {y ∈ R2:I(y) ≤ M} where the original shot noise I is not larger than M. Thus the GsinR(λ, κ) percolates for κ ≤ δ′/M, which concludes the proof. □

### 8.3.1 Bounds on the SINR Percolation Threshold κ*(λ)

M/D We consider the model in Section 8.3. Note that if the OPL W+M/D function l(r) is bounded away from 0 (i.e., if the attenuation function is finite), then when the density λ of nodes increases, the right-hand side of the inequality in (8.2) increases, while the left-hand side is bounded. Hence one may expect densification (taking λ → ∞) to possibly destroy connectivity of the SINR graph. This is confirmed by simulation as shown by Figure 8.1 where we plot the critical value κ*(λ) of κ that separates the super- and subcritical-phases in function of the node density λ.


<!-- p:163 -->


Fig. 8.1 Critical value of κ as a function of the node density.

0.06

sub-critical

+


0.05

+


0.04

+

kappa

+


0.03

+


0.02

+

super-critical

+


0.01

+

十

0

+

0

0.5

1

1.5

2

2.5

3

3.5

4

Node density

The aim of this section is to provide bounds on κ*(λ). A first immediate bound follows from Proposition 6.2.

Corollary 8.3. κ*(λ) ≤ 1/t for all λ.

Proof. In order to have two different nodes communicating to one given node, this last node has to be covered by two cells. By Proposition 6.2 this requires (as a necessary condition) 2t/(1 + κt) ≤ 1/κ which is equivalent to κ ≤ 1/t. □


<!-- p:164 -->


In [12] the following asymptotic bound was proved in the case of an OPL function l which is infinite outside some bounded set.

Proposition 8.4. Under the assumptions of Proposition 8.2 and assuming that l is infinite outside some bounded set,

$$A1 A2 ∑(X)*y> λ λ$$

for some positive and finite constants A1, A2.


<!-- p:165 -->


### Bibliographical Notes on Part II

Chapters 5–7 follow [1]. Approximations and bounds for the probability of coverage are considered in [45]. Under the assumption of Rayleigh fading, the SINR coverage probability for a class of Poisson-Poisson cluster p.p. known as Neyman-Scott p.p. was studied in [16]. The direct analytical methods have been used to compare this provability for both stationary and Palm repartition of nodes in the considered Poisson-Poisson cluster p.p. to the coverage probability in the Poisson p.p. scenario. In a more general scenario, relying extensively on the theory of stochastic ordering, in [5] one studies the effects of ordering of random measures on ordering of shot-noise fields generated by the respective random measures. Some applications to the comparison of SINR coverage probabilities are presented there.

The results of Chapter 8 stem from [12] and [13]. The percolation of the SINR graph is also studied and further developed in [15].


<!-- p:166 -->


Part III Appendix: Mathematical

## Complements


<!-- p:167 -->


9

### Higher Order Moment Measures of a Point Process

In this chapter, Φ is a p.p. on Rd and B is the Borel σ-algebra on Rd. We denote by M the set of point measures on Rd and by M the σ-algebra on M generated by sets of the form {μ ∈ M: μ(A) = k}.

## 9.1 Higher Order Moment Measures

Definition 9.1. For n ≥ 1, we define the nth power Φn and the nth factorial power Φ(n) of Φ as the following p.p. on Rdn:

$$\Phi ^ { n } ( A _ { 1 } \times \dots \times A _ { n } ) & = \Phi ( A _ { 1 } ) \dots \Phi ( A _ { n } ) \\ \Phi ^ { ( n ) } ( A _ { 1 } \times A _ { 2 } \times \dots \times A _ { n } ) & = \int _ { A _ { 1 } \times A _ { 2 } \times \dots \times A _ { n } } \dots \int \left ( \Phi - \sum _ { k = 1 } ^ { n - 1 } \varepsilon _ { x _ { k } } \right ) ( d x _ { n } ) \\ & \left ( \Phi - \sum _ { k = 1 } ^ { n - 2 } \varepsilon _ { x _ { k } } \right ) ( d x _ { n - 1 } ) \dots \Phi ( d x _ { 1 } ) .$$


<!-- p:168 -->


Here are a few immediate observations on these point processes:

- Φn = ∑i,,in:xij ∈∈(x,...,xn),
- For all A1, . . ., An pairwise disjoint, Φn(∅k Ak) = (4V(∅)(u)Φ
- Φ(n)(A × · . . × A) = Φ(A)(Φ(A) − 1) · (Φ(A) − n + 1)+.

Definition 9.2. For n ≥ 1, we define the nth moment Mn and the nth factorial moment M(n) of the p.p. Φ as the following measures on Rd:

$$M ^ { n } ( B ) & = \mathbf E [ \Phi ^ { n } ( B ) ] \\$$

$$M ^ { ( n ) } ( B ) = E [ \Phi ^ { ( n ) } ( B ) ] , \quad B \in \mathcal { B } ^ { n } .$$

Here are some obvious observations on these measures:

- M(1)(A) = M1(A) = M(A) = E[Φ(A)].
- M2(A × A) − (M(A))2 = Var(Φ(A)) is the variance of Φ(A).
- M2(A × B) − M(A)M(B) = Cov(Φ(A), Φ(B)) is the covariance of Φ(A) and Φ(B).
- For A1, . . . , An ∈ B, Mn(∅k Ak) = E[Πk Φ(Ak)]; in particular Mn(An) = E[Φ(A)n].
- For A1, . , An pairwise disjoint, Mn(∅k Ak) = M(n) (∅k Ak) = E[ΠIkΦ(Ak)].
- M2(A × B) = M(A ∩ B) + M(2)(A × B).
- M(n)(A × · · · × A) = E[Φ(A)(Φ(A) − 1) · · · (Φ(A) − n + 1)+].

Proposition 9.1. For the Poisson p.p. Φ with intensity measure Λ, M = Λ and M(n) = Λn, for all n.

Proof. Since Φ(A) is a Poisson r.v. with parameter Λ(A),

$$M ^ { ( n ) } ( A ^ { n } ) = E [ \Phi ( A ) ( \Phi ( A ) - 1 ) \cdots ( \Phi ( A ) - n + 1 ) ^ { + } ] = ( \Lambda ( A ) ) ^ { n }$$


<!-- p:169 -->


Let n1, . . . , nk ∈ N, with Σi ni = n and let A1, . . . , Ak be pairwise disjoint Borel sets. We have

$$\underline { k }$$

$$J o n \ B o r { S c h s c r { W c h a v c } } \\ M ^ { ( n ) } \left ( \bigotimes _ { i = 1 } ^ { k } A _ { i } ^ { n _ { i } } \right ) \\ = E \left [ \prod _ { i } \Phi ^ { ( n _ { i } ) } ( A _ { i } ^ { n _ { i } } ) \right ] = \prod _ { i } E [ \Phi ^ { ( n _ { i } ) } ( A _ { i } ^ { n _ { i } } ) ] = \prod _ { i } M ^ { ( n _ { i } ) } ( A _ { i } ^ { n _ { i } } ) \\ = \prod _ { i } \Lambda ^ { n _ { i } } ( A _ { i } ^ { n _ { i } } ) = \Lambda ^ { n } \left ( \bigotimes _ { i = 1 } ^ { k } A _ { i } ^ { n _ { i } } \right ) .$$

## 9.2 Palm Measures

Definition 9.3. For n ≥ 1, the nth order Campbell measure Cn and the nth order reduced Campbell measure C(n) of Φ are the following measures on Rnd × M:

$$m e u s \, \text { on } \mathbb { R } ^ { n d } \times \mathbb { M } \colon \\ C ^ { n } ( B \times \Gamma ) = E \left [ \int _ { B } 1 ( \Phi \in \Gamma ) \, \Phi ^ { n } ( d ( x _ { 1 } , \dots , x _ { n } ) ) \right ] \\ C ^ { ( n ) } ( B \times \Gamma ) = E \left [ \int _ { B } 1 \left ( \Phi - \sum _ { i = 1 } ^ { n } \varepsilon _ { x _ { 1 } } \in \Gamma \right ) \Phi ^ { ( n ) } ( d ( x _ { 1 } , \dots , x _ { n } ) ) \right ] , \\ B \in \mathcal { B } ^ { n } , \ \Gamma \in \mathcal { M } .$$

By the same type of arguments as in Section 1.4, we get:

Definition 9.4. If Mn is σ-finite, for all Γ ∈ M, there exist nonnegative functions Pxn, n(Γ) and Px,.,xn(F) such that (n) x1,..,xn

$$C ^ { n } ( B \times \Gamma ) = \int _ { B } P _ { x _ { 1 } , \dots , x _ { n } } ^ { n } ( \Gamma ) \, M ^ { n } ( d ( x _ { 1 } , \dots , x _ { n } ) )$$

$$C ^ { ( n ) } ( B \times \Gamma ) = \int _ { B } P _ { x _ { 1 } , \dots , x _ { n } } ^ { ( n ) } ( \Gamma ) M ^ { ( n ) } ( d ( x _ { 1 } , \dots , x _ { n } ) ) .$$

n(·) and Px,..x (.) is callled reduced Palm distribution of Φ.


<!-- p:170 -->


The following formulas, known as Campbell's formulas, are an immediate consequence of Definition 9.4:

Corollary 9.2. For all non-negative functions f on (Rnd × MI)

$$& \overline { \text {Corollary 9.2. For all non-negative functions } f \text { on } ( \mathbb { R } ^ { n d } \times \mathbb { M } ) } \\ & \int _ { \mathbb { R } ^ { n d } } \int _ { \mathcal { M } } f ( x _ { 1 } , \dots , x _ { n } , \phi ) \, C ^ { n } ( d ( x _ { 1 } , \dots , x _ { n } , \phi ) ) \\ & \quad = \int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { M } } f ( x _ { 1 } , \dots , x _ { n } , \phi ) \, P _ { x _ { 1 } , \dots , x _ { n } } ^ { n } \left ( d \phi \right ) M ^ { n } ( d ( x _ { 1 } , \dots , x _ { n } ) ) \\ & \int _ { \mathbb { R } ^ { n d } } \int _ { \mathcal { M } } f ( x _ { 1 } , \dots , x _ { n } , \phi ) \, C ^ { ( n ) } ( d ( x _ { 1 } , \dots , x _ { n } , \phi ) ) \\ & \quad = \int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { M } } f ( x _ { 1 } , \dots , x _ { n } , \phi ) \, P _ { x _ { 1 } , \dots , x _ { n } } ^ { ( n ) } ( d \phi ) \, M ^ { ( n ) } ( d ( x _ { 1 } , \dots , x _ { n } ) ) . \quad ( 9 . 1 0 ) \\ & \quad \text {For } x _ { 1 } , \dots , x _ { n } \in \mathbb { R } ^ { d } \, \text { let } \Phi _ { x _ { 1 } } \, \text { and } \Phi _ { x _ { n } } ^ { ! } \, \text { be point processes on }$$

For x1, . .,xn ∈ Rxd let ,x,.,xn and 11 be point processes on Rnd with laws Pn x1,...,xn

$$P _ { x _ { 1 } , \dots , x _ { n } } ^ { n } ( \cdot ) & = P _ { \Phi _ { x _ { 1 } , \dots , x _ { n } } } ( \cdot ) = P \{ \Phi _ { x _ { 1 } , \dots , x _ { n } } \in \cdot \} \\ P _ { x _ { 1 } , \dots , x _ { n } } ^ { ( n ) } ( \cdot ) & = P _ { \Phi _ { x _ { 1 } , \dots , x _ { n } } } ^ { \prime } ( \cdot ) = P \{ \Phi _ { x _ { 1 } , \dots , x _ { n } } ^ { \prime } \in \cdot \} . \\ \text {Campbell formulas can be rewritten as}$$

The Campbell formulas can be rewritten as

$$The CAMPbell formulas can be rewritten as \\ & \quad E \left [ \sum _ { x _ { 1 } , \dots , x _ { n } \in \Phi } f ( x _ { 1 } , \dots , x _ { n } , \Phi ) \right ] \\ & = \int _ { \mathbb { R } ^ { n d } } E [ f ( x _ { 1 } , \dots , x _ { n } , \Phi _ { x _ { 1 } , \dots , x _ { n } } ) ] M ^ { n } ( d ( x _ { 1 } , \dots , x _ { n } ) ) \\ & \quad E \left [ \sum _ { x _ { 1 } , \dots , x _ { n } \in \Phi } f ( x _ { 1 } , \dots , x _ { n } , \Phi ) \right ] \\ & = \int _ { \mathbb { R } ^ { n d } } E [ f ( x _ { 1 } , \dots , x _ { n } , \Phi _ { x _ { 1 } , \dots , x _ { n } } ^ { ! } ) ] M ^ { ( n ) } ( d ( x _ { 1 } , \dots , x _ { n } ) ) . \\ \text {If } M ^ { ( n ) } \text { is } \sigma \text {finite, we have}$$

If M(n) is σ-finite, we have

$$P \{ \Phi _ { x _ { 1 } , \dots , x _ { n } } - \sum _ { i = 1 } ^ { n } \varepsilon _ { x _ { i } } \in \cdot \} = P \{ \Phi _ { x _ { 1 } , \dots , x _ { n } } ^ { ! } \in \cdot \} = P _ { x _ { 1 } , \dots , x _ { n } } ^ { ( n ) } ( \cdot ) , \quad ( 9 . 1 3 ) \\$$

for M(n)-a.s. all pairwise different points (x1, . . .,xn) ∈ Rd.


<!-- p:171 -->


### 9.2.1 The Palm Measure Algebra

Assume that M(n+m) is σ-finite. For all (x1, . . . ,xn) ∈ Rnd, let

- γ(n,m) be the mth reduced Campbell measure of Φx1,..xn; x1,...,xn
- D(n,m) the mth reduced Palm measure of Φx,..,x· P x1,...,xn,y1,.,ym
- Mx1,.,xm (n,m) the mth factorial power of Φx1,..,x;

Here is the composition rule for Palm measures:

Corollary 9.3. For all A ∈ Bn, B ∈ Bm

$$M ^ { ( n + m ) } ( A \times B ) & = \int _ { \mathbb { E } ^ { n } } \int _ { \mathbb { E } ^ { m } } 1 ( ( x _ { 1 } , \dots , x _ { n } ) \in A ) 1 ( ( y _ { 1 } , \dots , y _ { m } ) \in B ) \\ & M _ { x _ { 1 } , \dots , x _ { n } } ^ { ( m ) } ( d ( y _ { 1 } , \dots , y _ { m } ) ) \, M ^ { ( n ) } ( d ( x _ { 1 } , \dots , x _ { n } ) ) \\$$

and

$$P _ { x _ { 1 } , \dots , x _ { n } , y _ { 1 } , \dots , y _ { m } } ^ { ( n , m ) } = P _ { x _ { 1 } , \dots , x _ { n } , y _ { 1 } , \dots , y _ { m } } ^ { ( n + m ) }$$

for M(n+m)-almost a,l (x1, . . ., xn, ,1, . . , ym) ∈ Rn+m.

Here is a direct consequence and extension of Slivnyak's theorem to higher order factorial moment measures:

Corollary 9.4. Let Φ be a Poisson p.p. with intensity measure Λ. For Λn-almost all (x1, . . . , xn) ∈ Rd distinct,

$$P _ { x _ { 1 } , \dots , x _ { n } } ^ { ( n ) } ( \cdot ) = P \{ \Phi \in \cdot \}$$

$$\Phi + \sum _ { i } \varepsilon _ { x _ { i } } \in \cdot \Big \} .$$

The proof follows from (9.13) and Corollary 9.3 and from Slivnyak's theorem.


<!-- p:172 -->


### Stationary Marked Point Processes

## 10.1 Marked Point Processes

Let (K, K) be some measurable mark space. In this chapter, we consider the space M of point measures on (Rd × K, B ⊗ K) such that for all μ ∈ MI, μ(B × K) &lt; ∞ for all bounded B ∈ B (B denotes the Borel σfield of Rd). Let M denote the σ-field of M generated by the mappings μ → μ(B × K) where B and K are sets of B, and K respectively.

aia mos i oia nai a   oa in y space (Ω, A, P) → (, M).

## 10.1.1Translations

On I, we define the translation operator of vector x ∈ Rd as

$$S _ { x } \widetilde { \mu } ( A \times K ) = \widetilde { \mu } ( ( A + x ) \times K ) \, ,$$

where A + x = {y + x ∈ Rd: y ∈ A}. Note that if μ = Σiε(xi,ki), then Sx ̄ = ∑iε(xi−x,ki)·

Definition 10.1. A marked p.p.  is stationary if its law is invariant by all translations, i.e. if P(Sx ∈ Γ) = P( ∈ Γ) for all x ∈ Rd and Γ ∈ M.


<!-- p:173 -->


### 10.1.2 Rotations

On M, we define the rotation operator

$$R _ { r } \widetilde { \mu } ( A \times K ) = \widetilde { \mu } ( r A \times K ) \, ,$$

where rA = {ry ∈ Rd: y ∈ A } and where r is a rotation (w.r.t. the origin of Rd) if r:x → Ax with A an orthogonal matrix (i.e. a matrix such that ATA = I and det A = 1). Note that if μ = Σi ε(xi,ki), then Rrμ = ∑iε(r−1xi,ki)·

Definition 10.2. The p.p. Φ is isotropic if its law is invariant by all rotations, i.e. if P(r ∈ Γ) = P( ∈ Γ), for all rotations r and Γ ∈ M.

The homogeneous Poisson point process and its associated hard core Matérn point process are both stationary and isotropic.

## 10.2 Palm-Matthes Distribution of a Marked Point Process

### 10.2.1 Campbell-Matthes Measure of a Marked Point Process

The intensity of a stationary marked p.p.  is

$$\lambda = E [ \widetilde { \Phi } ( U \times \mathbb { K } ) ] = E [ \Phi ( U ) ] \, ,$$

where U = (0, 1]d and Φ(·) = δ(· × K). In what follows, we assume that ·∞&gt; &gt;0

The Campbell–Matthes measure Č of the marked p.p.  is defined as

$$\widetilde { C } ( B \times K ) = \mathbf E \left [ \int _ { \mathbb { E } } \int _ { \mathbb { K } } \mathbf I ( x \in B ) \mathbf I ( z \in K ) \, \widetilde { \Phi } ( d ( x , z ) ) \right ] .$$

It admits the representation

$$\widetilde { C } ( B \times K ) = \lambda | B | \nu ( K ) .$$

The probability measure ν(·) on (K, K) is called the Palm distribution of the marks.


<!-- p:174 -->


Using classical monotone class arguments, (10.5) gives:

Corollary 10.1. For all functions f: Rd × K → R+,

$$E \left [ \sum _ { x _ { n } \in \Phi } f ( x _ { n } , k _ { n } ) \right ] = \lambda \int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { M } } f ( x , k ) \, \nu ( d k ) d x .$$

The last formula is the Campbell-Matthes formula for stationary marked p.p.

### 10.2.2 Palm-Matthes Probability of a Stationary Point Process

Let Φ be a stationary p.p. It is easy to check that

$$\widetilde { \Phi } = \sum _ { i } \varepsilon _ { x _ { i } , S _ { x _ { i } } \Phi } = \sum _ { i } \varepsilon _ { x _ { i } , \Phi - x _ { i } }$$

is a stationary marked p.p. with marks taking their values in the measurable space (M,M). These specific marks are called the universal marks of Φ.

By definition, the Palm-Matthes distribution of the stationary p.p. Φ on (M, M) is the Palm distribution of the marks of this stationary marked p.p. It is denoted by P0. When making use of (10.5), we get that it can be defined by

$$C a l \, \hat { C } \, \hat { C } \, \hat { C } \, \hat { C } \, \hat { D } & \, y \\ P ^ { 0 } ( \Gamma ) & = \frac { 1 } { \lambda | B | } E \left [ \int _ { \mathbb { R } ^ { d } } 1 ( x \in B ) 1 ( S _ { x } \Phi \in \Gamma ) \, \Phi ( d x ) \right ] \\ & = \frac { 1 } { \lambda | B | } E \left [ \int _ { \mathbb { R } ^ { d } } 1 ( x \in B ) 1 ( \Phi - x \in \Gamma ) \, \Phi ( d x ) \right ] , \quad \Gamma \in \mathcal { M } , \quad ( 1 0 . 7 ) \\$$

where B is any bounded Borel set of Rd.

Using classical monotone class arguments, (10.5) gives:

Corollary 10.2. For all functions f: Rd × M → R+,

$$C o r l o r y \, & \, 1 0 . 2 . \ \text { For all functions } f \colon \mathbb { R } ^ { d } \times \mathbb { M } \to \mathbb { R } ^ { \dagger } , \\ & \, E \left [ \int _ { R ^ { d } } f ( x , S _ { x } ( \Phi ) ) \Phi ( d x ) \right ] = E \left [ \sum _ { x _ { n } \in \Phi } f ( x _ { n } , \Phi - x _ { n } ) \right ] \\ & = \lambda \int _ { \mathbb { R } ^ { d } } \int _ { \mathbb { M } } f ( x , \phi ) \, P ^ { 0 } ( d \phi ) d x . \ \ ( 1 0 . 8 )$$


<!-- p:175 -->


The last formula is the Campbell-Matthes formula for stationary p.p.

The distribution P0 is often interpreted as that of the point process n o on  o n, nn n   o ,, of Φ. This latter interpretation is justified when

$$P ^ { 0 } ( \Gamma ) & = \frac { 1 } { \lambda | B | } E \left [ \sum _ { x _ { k } \in \Phi } 1 ( x _ { k } \in B ) 1 ( \Phi - x _ { k } \in \Gamma ) \right ] \\ & = \lim _ { B _ { n } \uparrow \mathbb { R } ^ { d } } \frac { 1 } { \lambda | B _ { n } | } \sum _ { x _ { k } \in \Phi } 1 ( x _ { k } \in B _ { n } ) 1 ( \Phi - x _ { k } \in \Gamma ) .$$

Remark 10.1. It is often better to define the Palm-Matthes probability on the probability space (Ω, A) where the p.p. Φ is assumed to be defined, rather than on (M, M) as above. For this, one has to assume that this probability space is endowed with an abstract shift operator θx, x ∈ Rd, such that

$$\Phi ( \theta _ { x } \omega ) = S _ { x } \Phi ( \omega ) .$$

If the probability P on (Ω, A) is such that E(f o θx) = E(f) for all x, then any p.p. satisfying (10.10) is stationary. One then proceeds as above; one defines the Campbell-Matthes measure on Rd × Ω by

$$\mathcal { C } ( B \times F ) = \mathbf E \left [ \int _ { \mathbb { R } ^ { d } } \int _ { \Omega } \mathbb { 1 } ( x \in B ) \mathbb { 1 } ( \theta _ { x } \omega \in F ) \, \Phi ( \mathbf d ( x ) ) \right ] , \quad ( 1 0 . 1 1 )$$

for all F ∈ A. It admits the representation

$$\mathcal { C } ( B \times F ) = \lambda | B | \mathbf P ^ { 0 } ( F ) .$$

The probability measure P0 is called the Palm-Matthes probability of Φ on (Ω, A). It can also be defined by the relation:

$$P ^ { 0 } ( F ) = \frac { 1 } { \lambda | B | } E \left [ \int _ { \mathbb { R } ^ { d } } \mathbb { I } ( x \in B ) \mathbb { 1 } ( \theta _ { x } \omega \in F ) \, \Phi ( d x ) \right ] . \quad ( 1 0 . 1 3 )$$

The associated Campbell-Matthes formula reads

with E0 the expectation w.r.t. P0 on (Ω, A).

$$T h e s a s o i c i a s d o t i a s s o u l a r e d s \\ E \left [ \sum _ { x _ { n } \in \Phi } f ( x _ { n } , \theta _ { x _ { n } } \omega ) \right ] = \lambda E ^ { 0 } \left [ \int _ { \mathbb { R } ^ { d } } f ( x , \Phi ) \, d x , \right ] \\ \intertext { w i t h E ^ { 0 } the e x p e r a t i o n w r t P ^ { 0 } on ( \Omega , A ) }$$


<!-- p:176 -->


### 10.2.3 Relation with the Definition Given in the Non-stationary Case

The aim of this section is to clarify the relationships between:

- the Palm distributions defined in Section 1.4, which was denoted by Px;
- the Palm distribution of order 1, defined in Section 9.2, which was denoted by P1; x,
- the Palm-Matthes probability P0 which was defined above,

whenever the underlying p.p. Φ is stationary.

We have Px = P1 (this is just a matter of notation). The relationship between Px and P0, which are two probability measures on M, is clarified by the following lemma:

Lemma 10.3. For almost all x in Rd and for all Γ in M,

$$P _ { x } ( \Gamma ) = P ^ { 0 } ( S _ { - x } ^ { - 1 } ( \Gamma ) ) \, ,$$

where S−1(Γ) = {φ ∈ M: Saφ ∈ Γ}, a ∈ Rd.

Proof. Applying the Campbell-Matthes formula to the function

$$f ( x , \phi ) = \mathbb { 1 } ( x \in B ) \mathbb { 1 } ( \phi \in S _ { - x } ^ { - 1 } ( \Gamma ) ) = \mathbb { 1 } ( x \in B ) \mathbb { 1 } ( S _ { - x } ( \phi ) \in \Gamma ) ,$$

we get that for all bounded Borel sets B and all Γ ∈ M

$$\ w \, \text {get that for an bounded B and an } & \in S ^ { 1 } \, \Phi \\ \lambda \int _ { B } P ^ { 0 } ( S _ { - x } ^ { - 1 } ( \Gamma ) ) \, d x & = E \left [ \int _ { \mathbb { R } ^ { d } } 1 ( x \in B ) 1 ( S _ { x } \circ S _ { - x } ( \Phi ) \in \Gamma ) \, \Phi ( d x ) \right ] \\ & = E \left [ \int _ { \mathbb { R } ^ { d } } 1 ( x \in B ) 1 ( \Phi \in \Gamma ) \, \Phi ( d x ) \right ] = C ^ { 1 } ( B \times \Gamma ) ,$$

where C1 is defined in Section 9.2. Hence, from (9.7) in Chapter 9,

$$\lambda \int _ { B } P ^ { 0 } ( S _ { - x } ^ { - 1 } ( \Gamma ) ) \, d x = \lambda \int _ { B } P _ { x } ( \Gamma ) \, d x . \quad \square$$


<!-- p:177 -->


### Fairness and Optimality

Here, we briefly remind the basic notions and facts concerning the fairness and optimality in resource allocation.

We assume that we have N entities (think of mobile users in a given cell). The goal is to allocate some positive real valued resource (think of rates) R = (R1, . . . , RN) to these entities respecting some constraint of the form R ∈ R, where the set of feasible allocations R is some given subset of RN. An allocation R ∈ R is called

- (globally) optimal if it maximizes ∑n=1 Rn.
- max−min fair if for each n ∈ {1, . . . , N} increasing Rn must be at the expense of decreasing Rm for some m such that initially Rm &lt; Rn. If a max-min fair allocation exists, then it is unique and strictly Pareto optimal (for a unified treatment see [38]).
- (strictly) Pareto optimal if there is no solution R' ∈ R dominating it, i.e., such that Rn ≥ Rn for all n = 1, . . . , N and Rn0 &gt; Rn0 for some n0 ∈ {1, . . . , N}.


<!-- p:178 -->


- proportionally fair if for each other allocation R' ∈ R we have ∑n=1(Rn − Rn)/Rn ≤ 0. If a proportionally fair allocation exists on R, then it is unique and it is the solution of the following maximization problem maxR∈R Σn=1 log Rn ( [30]).

Consider the maximization problem

$$\max _ { R \in \mathcal { R } } \sum _ { n = 1 } ^ { N } R _ { n } ^ { 1 - \alpha } / ( 1 - \alpha ) ,$$

where α is a real number. Its solution is called the α-fair optimal. The following relations hold (see [32] for the proof).

Proposition 11.1. An α-fair optimal policy is globally optimal when α → 0, proportionally fair when α → 1, and max-min fair when α → ∞.


<!-- p:179 -->


### Lemmas on Fourier Transforms

## 12.1 Fourier Transforms

For all functions f from R to R we will denote by

$$\widehat { f } ( s ) = \int _ { \mathbb { R } } e ^ { - 2 i \pi t s } f ( t ) d t$$

its Fourier transform at s ∈ R when it exists.

Below, we will make use of the fact that the Fourier transform is an isometry on the space of square integrable functions (PlancherelParseval Theorem; [7]). Namely, for all square integrable functions f and g,

$$\int _ { \mathbb { R } } f ( t ) g ( t ) d t = \int _ { \mathbb { R } } \widehat { f } ( s ) \overline { \widehat { g } ( s ) } d s ,$$

where g(s) denotes the complex conjugate of g(s).

## 12.2 Lemmas

The following lemma and its corollaries establish representations of the mass that a (square integrable) density puts on an interval (possibly a random interval) in terms of the Fourier transform of this density.


<!-- p:180 -->


Lemma 12.1. Let f be a square integrable function. Then for all real numbers a &lt; b,

$$\int _ { a } ^ { b } f ( t ) d t = \int _ { \mathbb { R } } \widehat { f } ( s ) \frac { e ^ { 2 i \pi b s } - e ^ { 2 i \pi a s } } { 2 i \pi s } d s .$$

Proof. This immediately follows from the isometry property and from the fact that the Fourier transform of the square integrable function g(t) = 1(a ≤ t ≤ b) is

$$\frac { e ^ { - 2 i \pi b s } - e ^ { - 2 i \pi a s } } { \widehat { g } ( s ) = \frac { e ^ { - 2 i \pi s } } { - 2 i \pi s } . } \quad \square$$

Note that if f is a bounded probability density, then it is square integrable.

Corollary 12.2. Let X be a non-negative real valued random variable with a square integrable density f; let Y be a non-negative and integrable real-valued random variable with a square integrable density g. Assume that X and Y are independent. Then

$$P ( X \leq Y ) = \int _ { \mathbb { R } } \widehat { f } ( s ) \frac { \overline { \widehat { g } ( s ) } - 1 } { 2 i \pi s } d s .$$

Proof. We deduce from (12.2) that the L.H.S. of (12.3) is equal to

$$\int _ { 0 } ^ { \infty } g ( y ) \int _ { \mathbb { R } } \widehat { f } ( s ) \frac { e ^ { 2 i \pi y s } - 1 } { 2 i \pi s } d s \, d y .$$

Equation (12.3) follows provided one can swap the two integrals. This is licit provided the function

$$( s , y ) \rightarrow g ( y ) \widehat { f } ( s ) \frac { e ^ { 2 i \pi y s } - 1 } { 2 i \pi s } \\$$

is absolutely integrable. For large |s| this function is integrable as a corollary of the Cauchy-Schwarz inequality and the integrability of f2(·), which in view of (12.1) is equivalent to the integrability of |f(s)|2 (see also [14, p. 510]). For small |s| the modulus of this function is bounded from above by the function g(y) |f(s)| yK for some constant K so that absolute integrability holds when g has a first moment.


<!-- p:181 -->


For instance, if both X and Y are exponential with parameters λ and μ, resp., then we can use the Cauchy residue theorem to check that

$$P ( X < Y ) = \int _ { \mathbb { R } } \frac { \lambda } { ( \lambda + 2 i \pi s ) ( \mu - 2 i \pi s ) } d s = \frac { \lambda } { \lambda + \mu }$$

as expected.

The next lemma extends the previous representations to the Laplace transform of the positive part of a real valued random variable.

Lemma 12.3. Let X be a real valued random variable with a square integrable density f. Let X+ = max(X,0). Then, for all u &gt; 0,

$$E ( e ^ { - u X ^ { + } } ) = P ( X < 0 ) + \int _ { \mathbb { R } } \frac { \widehat { f } ( s ) } { u - 2 i \pi s } d s .$$

Proof. The integral to be evaluated for obtaining the second term is

$$I ( u ) = \int _ { - \infty } ^ { \infty } f ( t ) 1 ( t > 0 ) e ^ { - s t } d t .$$

Since the Fourier transform g(s) of the function t → 1(t &gt; 0)e−ut is 1/(u + 2iπs), it follows from the isometry property that

$$I ( u ) = \int _ { \mathbb { R } } \frac { \widehat { f } ( s ) } { u - 2 i \pi s } \text {d} s . \quad \square$$

A naive use of (12.4) would lead to the result that

$$P ( X > 0 ) = \lim _ { u \to 0 } I ( u ) = - \int _ { \mathbb { R } } \frac { \widehat { f } ( s ) } { 2 i \pi s } d s .$$

As we shall see below, this is wrong.

A first question anyway is the sense to give to the last singular integral (it is called singular because of the singularity at s = 0).

Let φ(.) be some complex valued function which satisfies the following assumptions (referred to as A below):

- it is differentiable, with finite derivatives;
- it is such that |φ(s)| ≤ 1/|s|μ, when |s| tends to ∞, for some μ &gt; 0.


<!-- p:182 -->


One can then give a sense to the singular integral

$$J = \int _ { \mathbb { R } } \frac { \phi ( s ) } { s } d s ,$$

(note that thanks to our assumption on the tail behavior of φ, the only singularity that matters here is that at s = 0) as the principal value form which is defined as

$$J = \lim _ { \epsilon \to 0 } \int _ { \mathbb { R } / [ - \epsilon , \epsilon ] } \frac { \phi ( s ) } { s } d s .$$

For more on the evaluation of singular integrals and their principal value, see [18].

Corollary 12.4. If f is a square integrable probability density with a finite first moment, then for all real numbers a

$$\int _ { a } ^ { \infty } f ( t ) d t = \frac { 1 } { 2 } - \frac { 1 } { 2 i \pi } \int _ { \mathbb { R } } \frac { \widehat { f } ( s ) e ^ { 2 i \pi a s } } { s } d s ,$$

where the singular integral is defined as above.

Proof. First, it is enough to prove the formula for a = 0 since the function f (t − a) has for Fourier transform f(s)e2iπas.

The formula for a = 0 is a direct corollary of Lemma 12.3 and of the so-called Sokhotski formula (see [18]) which states that for all functions φ as above, for all u &gt; 0,

$$\lim _ { u \to 0 } \int _ { \mathbb { R } } \frac { \phi ( s ) } { s + i u } d s = \int _ { \mathbb { R } } \frac { \phi ( s ) } { s } d s + i \pi \phi ( 0 ) .$$

Equation (12.4) and the last relation applied to φ(s) = −(1/2iπ)f(s) immediately give (12.7). Equivalently

$$\lim _ { u \to 0 } I ( u ) = \frac { 1 } { 2 } - \int _ { \mathbb { R } } \frac { \widehat { f } ( s ) } { 2 i \pi s } d s .$$

We can use the Sokhotski formula because the Fourier transform of a density admitting a first moment is differentiable and has finite derivatives. In addition the fact that the density is square integrable implies that its Fourier transform is square integrable, so that the tail decay of Assumption A holds.


<!-- p:183 -->


Here is another proof based on more elementary arguments. When letting b go to ∞ in (12.2), the L.H.S. tends to ∫0∞ f(t)dt. We rewrite the R.H.S. as the sum of three terms

$$\int \frac { \widehat { f } ( s ) } { \partial \dot { \cdot } } d$$

$$= \int _ { \mathbb { R } } \frac { } { 2 i \pi s }$$

$$I _ { 1 } & = - \int _ { \mathbb { R } } \frac { \widehat { f } ( s ) } { 2 i \pi s } d s \\ I _ { 2 } & = \int _ { \mathbb { R } } e ^ { 2 i \pi b s } \frac { \widehat { f } ( s ) - 1 ( s \in [ - \epsilon , + \epsilon ] ) } { 2 i \pi s } d s \\ I _ { 3 } & = \int _ { \mathbb { R } } \frac { e ^ { 2 i \pi b s } - 1 ( s \in [ - \epsilon , + \epsilon ] ) } { 2 i \pi s } d s = \frac { 1 } { 2 } ,$$

where ∈ is a positive real number.

The Riemann-Lebesgue lemma [7] states that for all integrable functions g,

$$\lim _ { b \to \infty } \int _ { \mathbb { R } } g ( s ) e ^ { 2 i \pi b s } d s = 0 .$$

So, in order to prove that I2 tends to 0 when b tends to ∞, it is enough to show that

$$\int _ { \mathbb { R } } \frac { | \widehat { f } ( s ) - \mathbb { 1 } ( s \in [ - \epsilon , + \epsilon ] ) | } { 2 \pi | s | } d s < \infty .$$

But this follows from the following two bounds:

$$\int _ { \mathbb { R } / [ - \epsilon , \epsilon ] } \frac { \left | \widehat { f } ( s ) \right | } { | s | } d s \leq \left ( \int _ { \mathbb { R } / [ - \epsilon , \epsilon ] } \frac { 1 } { s ^ { 2 } } d s \int _ { \mathbb { R } } \left | \widehat { f } ( s ) \right | ^ { 2 } d s \right ) ^ { \frac { 1 } { 2 } } < \infty ,$$

where we used the Cauchy-Shwarz inequality and the fact that f(s) is square integrable because f(s) is

$$\int _ { [ - \epsilon , \epsilon ] } \frac { | \frac { s | } { s | } } { | s | }$$

where we used that fact that if X has a finite first moment then its Fourier transform is differentiable and has a finite derivative. □


<!-- p:184 -->


### Graph Theoretic Notions

Let (Φ,E) be a connected undirected graph with the set of vertices Φ and edges ε. The neighbors of vertex (node) x ∈ Φ are defined as the set of nodes y ∈ Φ such that the edge (x, y) ∈ ε.

Let w be a collection of non-negative weights associated with the edges of the graph (i.e., a non-negative function described on E). Define the weight of a subgraph of (Φ, E) as the sum of the weights of its edges.

## 13.1 Minimum Spanning Tree

A spanning tree of this graph is a subgraph which is a tree and which connects all the vertices of this graph. A Minimum Weight Spanning Tree (or Minimum Spanning Tree (MST) for short) is a spanning tree with weight no larger than that of all other spanning trees.

Given a connected weighed graph (Φ,E,w), an MST can be constructed using Prim's algorithm:

- Initialize Ψ = {x}, where x is any node and F = ∅;
- Repeat until Ψ = Φ:


<!-- p:185 -->


- − Choose an edge (u, v) from E with u ∈ Ψ and v ∉Ψ and with minimum weight (if there are multiple solutions, pick one arbitrarily);
- − Add v to Ψ and (u, v) to F.

The proof of the fact that the output (Ψ = Φ,F) of this algorithm is an MST of (Φ, E, w) is classical.

Assume the MST is unique. Here are two useful properties.

Lemma 13.1. Assume that for all x, there is a unique neighbor x* of x such that w(x, x*) &lt; w(x, y), for all other neighbors y of x. Then (x, x*) ∈ F; i.e., this is an edge of the MST.

Proof. When initializing Prim's algorithm with x, we see that (x, x*) is an edge of the MST. Uniqueness concludes the proof. □

Lemma 13.2. (Cycle property) For all x and y neighbors, if the edge (x,y) belongs to the MST, there is no sequence of vertices z0, Z1, · · . , Zn, zn+1 in Φ, with n ≥ 1, x = z0, y = zn+1, (zk, zk+1) ∈ E for all k = 0, . . . n, and for which w(zk+1, zk) &lt; w(x, y), for all k = 0, . . . , n.

Proof. The above sequence defines a cycle of the graph. Assume (x, y) is in the MST and w(zk+1, zk) &lt; w(x, y), for all k = 0, . . . , n. If we delete edge (x,y) in the MST, this breaks it into two subtrees Tx and Ty with x ∈ Tx and y ∈ Ty. Since each node of Φ is either in Tx or in Ty, there is an integer 0 ≤ k ≤ n such that the nodes z0, . . . , zk all belong to Tx and the nodes zk+1, . . . , zn all belong to Ty. Consider now the tree obtained by adding the edge (zk, zk+1) to Tx ∪ Ty. Then this tree has a weight strictly smaller than that of the initial MST, which is a contradiction. □

### 13.1.1 Nearest Neighbor Graph

For any vertex x ∈ Φ call any x* ∈ Φ satisfying w(x,x*) ≤ miny∈Φ w(x, y) a w-nearest neighbor of x. We call the nearest neighbor graph (NNG) of Φ the graph on the set of vertexes Φ for which edges are drawn between any x and any of its nearest neighbors.


<!-- p:186 -->


The following statements are simple consequences of the definition of the NNG and of Lemma 13.1.

Corollary 13.3. Suppose each node x ∈ Φ has a unique nearest neighbor. Then the NNG has at most card(Φ) edges. Moreover, NNG is a subgraph of the MST.

### 13.1.2 Euclidean MST of the Poisson Point Process

Let Φ be a realization of a homogeneous Poisson p.p. on Rd with intensity λ. Consider Φ as the set of vertices of the complete graph (i.e., n ə əq |h − x| = (hx)m ə ·(3 ∃ (hx) Φ ∃ hx e 1an distance.

Let K be a compact subset of Rd. Consider the MST (ΦK,FK) of (ΦK, EK, ω), where ΦK = Φ ∩ K and EK = {(x, y): x, y ∈ ΦK}; it is unique with probability 1. Denote by M = MK(λ) = max(x,y)∈FK |x − y| the longest edge in the MST of Φ∩ K.

The following result was proved in [35] for the BM in R2 (and for the BM in higher dimension on the torus):

Proposition 13.4. Given a unit square K = [− homogeneous Poisson p.p. Φ with intensity λ on the plane R2. Denote by M = M(λ) the longest edge of the MST of Φ∩ K. Then

$$\lim _ { \lambda \to \infty } \mathbf P \{ \lambda \pi M ^ { 2 } - \log \lambda \leq u \} = \exp [ - e ^ { - u } ] \quad u \in \mathbb { R } .$$

Proof. We will only give a sketch of the reasoning presented in [35]: Denote by M = M(λ) the longest edges of the NNG of Φ ∩ K. Because the NNG is a subgraph of the MST, M ≤ M. Conversely, one gets that all edges (x,y) of the MST of Φ∩ K which satisfy the condition λπ|x − y|2 − logλ &gt; u (we call them u-long) belong to the NNG of


<!-- p:187 -->


Φ ∩ K with a probability converging to 1 when λ → ∞. Consequently

$$P \{ \lambda \pi M ^ { 2 } - \log \lambda \leq u \} & \leq P \{ \lambda \pi \tilde { M } ^ { 2 } - \log \lambda \leq u \} \\ & \leq P \{ \lambda \pi M ^ { 2 } - \log \lambda \leq u \} \\ & + P \{ \exists \text {edge } u \text {-long in MST}$$

that is not in NNG}

and for all u,

$$\lim _ { \lambda \to \infty } P \{ \lambda \pi M ^ { 2 } - \log \lambda \leq u \} = \lim _ { \lambda \to \infty } P \{ \lambda \pi \tilde { M } ^ { 2 } - \log \lambda \leq u \} \, .$$

Now, let us study the following surrogate model of the longest edge in the NNG. Consider λ (assumed to be an integer) i.i.d. random variables S1,  , Sλ, with a generic S having for distribution P(S ≥ u) = e−πλu2, and define M = M(λ) = max(S1 . . . , Sλ). Note that the distribution of S corresponds to the distribution of the length of the distance form a typical point of the homogeneous Poisson p.p. with intensity λ to its nearest neighbor; so the surrogate model ignores the boundary-effects of the "true" NNG. Moreover, in the true NNG, the number of points in K (|K| = 1) is Poisson with mean λ rather than deterministic and equal to λ, and their nearest neighbor distances are not independent. Despite this, it is shown in [35] using the Chen-Stein method that

$$\lim _ { \lambda \to \infty } P \{ \lambda \pi \tilde { M } ^ { 2 } - \log \lambda \leq u \} = \lim _ { \lambda \to \infty } P \{ \lambda \pi \widehat { M } ^ { 2 } - \log \lambda \leq u \} \, .$$

Thanks to independence, it is easy to show that the latter limit of the surrogate model is equal to

$$\lim _ { \lambda \to \infty } & P \{ \lambda \pi \widehat { M } ^ { 2 } - \log \lambda \leq u \} = \lim _ { \lambda \to \infty } \left ( 1 - \frac { e ^ { - u } } { \lambda } \right ) ^ { \lambda } = \exp [ - e ^ { - u } ] . \quad \Box$$


<!-- p:188 -->


### Discrete Percolation

## 14.1 Bond Percolation on Zd.

Consider the integer lattice Zd in d dimensions. In what follows, we will consider d ≥ 2. Denote by L the set of edges joining any two adjacent points of Zd (which are at distance 1 from each other). Consider a family of random variables {X(e)}e∈c which are identically distributed with P{ X(e) = 1 } = 1 − P{ X(e) = 0 } = p for some p ∈ [0, 1]. We assume that this family is ergodic with respect to the natural shift on Zd, however, we do not assume X(e) to be mutually independent. We will say that the edge e ∈ L is open if X(e) = 1 and closed otherwise. This model is known as bond percolation on L; see Figure 14.1.

Definition 14.1. We say that the bond percolation model percolates if the set of open edges contains an infinite connected subset.

Denote by C the maximal connected component in the set of open edges containing the origin (as the endpoint of one of the edges). Define θ(p) = P{#C = ∞}, where #C denotes the number of edges in the set C.


<!-- p:189 -->


Fig. 14.1 Left: bond percolation on the square lattice in R2. Right: closed circuit surrounding (0,0) on the dual lattice.

(1

1)

(0,0)

0,0

closed bond

open bond

Remark 14.1. If θ(p) = 0, then the probability that the model percolates is 0 (we say that "it does not percolate"). Indeed, the probability that some edge belongs to an infinite component can be bounded by the sum of these probabilities over all edges, which is 0 due to the assumption. By ergodicity of the family {X(e)}, the converse is also true: if θ(p) &gt; 0, then with probability 1 the model percolates.

Let pc = sup{[0, 1] ∃ p: θ(p) = 0}. By stochastic monotonicity, the model percolates with probability 1 for p &gt; pc and does not percolate for p &lt; pc.

Remark 14.2. Another important monotonicity, with respect to dimension d, implies that pc(d + 1) ≤ pc(d), where we mark in the notation the explicit dependence of the critical probability pc on the dimension. To realize this it is enough to embed Ld in Ld+1 considering the natural projection of Ld+1 onto the subspace generated by the first d coordinates and noting that any infinite component in Ld is also an infinite component in Ld+1.

Note that pc may be degenerated (i.e., equal to 0 or 1). A first question answered in the theory of percolation is that of the conditions under which 0 &lt; pc &lt; 1.


<!-- p:190 -->


### 14.1.1 Upper Bound for the Critical Probability

We will give now some sufficient condition for pc &lt; 1. We will state and prove the result for d = 2. By Remark 14.2 this will be also a sufficient condition in all higher dimensions.

Assume thus d = 2. Denote by L' the shift of the square lattice L by the half of its side-length horizontally and vertically. The lattice L' is called the dual to L. Note that for each edge e ∈ L there exists a unique edge e' ∈ L', intersecting e at its center. Thus, one can define uniquely ud s :() = (,, ud  ,(,}  p e Denote by ρ(n) the number of self-avoiding circuits (closed paths) of length n in the dual lattice L' surrounding the origin. The proof of the following results is often referred to as Peierls's argument (see e.g. [21, pp.16–19]).

Proposition 14.1. Consider the bond percolation model {X(e): e ∈ L} on the square lattice Z2. Suppose that for some q (0 ≤ q &lt; 1)

$$P \{ X ( e _ { 1 } ) = 0 , \dots , X ( e _ { n } ) = 0 \} \leq q ^ { n }$$

for any set of n different edges e1, . , en. If

$$\sum _ { n = 1 } ^ { \infty } \rho ( n ) q ^ { n } < 1 \, ,$$

then the bond percolation model percolates.

Proof. The origin belongs to an infinite connected component iff it is not surrounded by any closed circuit of the dual bond percolation defined on L'. We will show that this last probability is positive by proving that its complement is strictly less than 1. For this, note that, the probability that there exists a closed circuit surrounding the origin is bounded by the expected number of such circuits, which in turn is bounded by ∑n=1 ρ(n)qn &lt; 1. □

Remark. For the square lattice L on the plane, we have the following bound: ρ(n) = 0 for n = 1, 2, 3 and ρ(n) ≤ 4n3n−2 for n ≥ 4. Thus condition (14.1) reads


<!-- p:191 -->


$$4 / 9 \sum _ { 4 } ^ { \infty } n ( 3 q ) ^ { n } & = \frac { 4 ( 3 q ) ^ { 4 } ( 4 - 9 q ) } { 9 ( 3 q - 1 ) ^ { 2 } } < 1 \, , \\$$

which is true for q &lt; 0.2075.. ..

Example 14.2 (Independent bond percolation). In the case of independent bond percolation on Z2, i.e. when X(e):e ∈ L are independent, condition (14.1) is obviously satisfied by q = 1 − p. Thus condition (14.2) is satisfied for p &gt; 1 − 0.2075 · · · = 0.7924 · · · or, in other words, pc(2) ≤ 0.7924 · · · . However, in this case some refinement of the proof of Proposition 14.1 can be used to show that percolation holds provided the series in (14.2) is only convergent. Indeed, in this case, some number N can be found such that Σn=N ρ(n)qn &lt; 1. Thus, with positive probability there is no closed circuit surrounding the origin of length larger than N. Moreover, for any rectangle containing the origin, the configuration of bonds outside the rectangle is independent of the configuration of bonds inside the rectangle, and with positive probability all the bonds inside it are open. This shows that the probability that the origin belongs to an infinite open connected component is positive. This new condition implies that the independent bond percolation model percolates for p &gt; 2/3 or, in other words, that pc(2) ≤ 2/3. e nn n ng o s ns on ns e n hes ' ·p   == ( p nre  pe p  p ns. Chapter 9]).

### 14.1.2 Lower Bound for the Critical Probability; IndependentPercolation Case

In the case of independent bond percolation, it is also relatively easy to show that pc(d) &gt; 0 for any d.

Denote by σ(n) = σ(n, d) the number of self-avoiding paths of length n on Zd starting at the origin and let λ(d) = limn→∞(σ(n, d))1/n.

Proposition 14.3. For independent bond percolation on Zd we have pc(d) ≥ 1/λ(d).


<!-- p:192 -->


Proof. Denote by N(n) the number of open paths starting at the origin and of length at least n. If the origin belongs to an infinite open path then obviously for all n, we have N(n) ≥ 1. Thus

$$\theta ( p ) \leq P \{ N ( n ) \geq 1 \} \leq E [ N ( n ) ] \leq p ^ { n } \sigma ( n )$$

for all n. If θ(p) &gt; 0 then limn p(σ(n))1/n = pλ(d) ≥ 1, i.e.; p &gt; 1/λ(d), which completes the proof. □

The exact value of λ(d) is not known, however, a simple observation gives σ(n, d) ≤ 2d(2d − 1)n−1 and thus λ(d) ≤ 2d − 1.

Concluding what was said about the independent bond percolation we have proved the following result.

Theorem 14.4. For independent bond percolation on Zd with d ≥ 2 we have 0 &lt; λc &lt; 1.

## 14.2 Independent Site Percolation

In site percolation, one opens or closes the vertexes of a given graph rather than its edges. Consider again Zd as the set of vertexes (called here "sites") and edges L defined exactly as in Section 14.1.

Let {Y(v)}v∈zd be a family of i.i.d. random variables with P{Y (v) = 1 } = 1 − P{ Y (v) = 0 } = p. We will say that the site v ∈ Zd is open if Y(v) = 1 and closed otherwise. This model is known as site percolation on Zd; cf. Figure 14.2 Two sites are said adjacent if they are connected by some edge (bond). A subset of sites is said connected if the corresponding sub-graph is connected.

Definition 14.2. We say that the site percolation model percolates if it contains an infinite connected sub-graph with open vertexes.

Denote by Csite the maximal connected sub-graph with open vertexes containing the origin. Define θsite(p) = P{#Csite = ∞ }, where #Csite denotes the number of vertexes in the set Csite and psite = -n t  t ets  {0 = ( sθ : d ∈ [ ] }r colates with probability 1 for p &gt; psite and does not percolate for p &lt; psite.


<!-- p:193 -->


Fig. 14.2 Left: site percolation on the square lattice in R2. Right: dual bond percolation.

C

1

(1,1)

O

l0)

closed site

C

つ

U

open site

O


Proposition 14.5. For all d we have psite &lt; 1; i.e. the site percolation model percolates for sufficiently large p &lt; 1.

Proof. We will prove this result considering the following dual onedependent bond percolation. For any edge e ∈ L with end-points in v and w, define X(e) = Y(v)Y (w); i.e., the edge is open iff its end-points are both open as sites. Obviously, if the dual bond model percolates then the original site model percolates as well. By Remark 14.2 it is enough to prove that the bond model percolates in dimension d = 2. For this we will use Proposition 14.1. Note that the independence of {Y (v)} implies the following one-dependence of {X(e) }: variables X(e1), . . . , X(en) are mutually independent if no two edges in e1, . . . , en have a common vertex. Any vertex in any edge in L (in dimension 2) has six edges sharing some vertex with it. This implies that condition (14.1) is satisfied for q = (1 − p2)n/7 and, by the Remark after Proposition 14.1, condition (14.1) reads

$$4 / 9 \sum _ { n = 4 } ^ { \infty } n \left ( 3 ( 1 - p ^ { 2 } ) ^ { 1 / 7 } \right ) ^ { n } < 1 \, ,$$

which is satisfied for sufficiently large p &lt; 1.

□


<!-- p:194 -->

### Table of Mathematical Notation and Abbreviations

| &#124; X &#124;                | Euclidean norm of vector X .                                                             |
|--------------------------------|------------------------------------------------------------------------------------------|
| &#124; B &#124;                | Lebesgue measure of set B ∈ B .                                                          |
| \                              | set difference.                                                                          |
| 〈 X,Y 〉                        | scalar product of vectors X and Y .                                                      |
| A                              | parameter of the OPL attenuation models.                                                 |
| a.s.                           | almost surely.                                                                           |
| A ( X ) (resp. A n ( X ))      | radial point map at X (resp. time-space point map at X and at time n ).                  |
| A d ( X ) (resp. A d ,n ( X )) | d-directional point map at X (resp. time-space point map at X and at time n              |
| B                              | the Borel σ -algebra of the Euclidean space.                                             |
| B X ( r )                      | ball of center X and radius r .                                                          |
| β                              | attenuation exponent of the OPL attenuation models.                                      |
| C X (Φ)                        | Voronoi cell of point X w.r.t. the p.p. Φ.                                               |
| C ( X,M ) (Φ)                  | SINR cell of point X w.r.t. the marks (fading, threshold, power, etc.) M and the p.p. Φ. |
| D                              | the destination node (in routing context; Part V in Volume II).                          |


<!-- p:198 -->


| e (resp. e ( n ))   | indicator of MAC channel access (resp. at time n ).                                         |
|---------------------|---------------------------------------------------------------------------------------------|
| E E 0               | expectation. expectation w.r.t. the Palm probability.                                       |
| ε x                 | Dirac measure at x . fading variable (resp. at time n ).                                    |
| F (resp. F ( n ))   |                                                                                             |
| G SINR              | the SINR graph.                                                                             |
| G SINR              | the time-space SINR graph.                                                                  |
| GI                  | General fading.                                                                             |
| GI W+GI / GI        | Kendall-like notation for a wireless cell or network.                                       |
| iff                 | if and only if.                                                                             |
| i.i.d.              | independently and identically distributed.                                                  |
| I Φ                 | shot noise field associated with the point process Φ.                                       |
| K ( β )             | constant associated with Rayleigh fading SN. See (2.26 in Volume I) and (16.9 in Volume II) |
| L ( X )             | length to the next hop from point X in a routing algorithm.                                 |
| L ( X )             | local delay at node X .                                                                     |
| l ( . )             | attenuation function of the OPL models.                                                     |
| L Φ                 | Laplace functional of the p.p. Φ.                                                           |
| L V                 | Laplace transform of the random variable V .                                                |
| λ                   | the intensity parameter of a homogeneous Poisson p.p.                                       |
| Λ( . )              | the intensity measure of a Poisson p.p.                                                     |
| L.H.S.              | left hand side.                                                                             |
| M                   | exponential random variable (or Rayleigh fading).                                           |
| M                   | space of point measures. 1 .                                                                |
| μ                   | the mean fading is μ -                                                                      |
| N                   | the non-negative integers.                                                                  |
| N ( μ,σ 2 )         | the Gaussian law of mean μ and variance σ 2 on R .                                          |


<!-- p:199 -->


| N C (0 ,σ 2 )             | the complex vauled Gaussian law.                                             |
|---------------------------|------------------------------------------------------------------------------|
| O                         | the origin of the Euclidean plane (in routing context; Part V in Volume II). |
| p                         | medium access probability in Aloha.                                          |
| P ( X )                   | progress from point X towards destination in a routing algorithm.            |
| P                         | probability.                                                                 |
| P 0                       | Palm probability.                                                            |
| p c Φ                     | probability of coverage. point process.                                      |
| R d                       | Euclidean space of dimension d .                                             |
| S                         | the source node (in routing context; Part V in Volume II).                   |
| R.H.S.                    | right hand side.                                                             |
| T                         | threshold for SINR.                                                          |
| Var                       | Variance.                                                                    |
| V ( X ) (resp. V ( X,n )) | set of neighbors of X in G SINR (resp. of ( X,n ) in G SINR ).               |
| W (resp. W ( n )) Z       | thermal noise (resp. at time n ). the relative integers.                     |


<!-- p:200 -->


### Index

| 3G, see third generation cellular network 296                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------|
| access point, 296, 347 ad hoc network, 263 , 271 , 336 , 345 adaptive coding, 22, 26, 50, 68, 102 admission control, 127, 138, 151 |
| Aloha, 123, 205, 206, 271 , 287 opportunistic, 44, 206 spatial, 17 antenna                                                         |
| azimuth beam-width, 258 antipodal signaling, 277 atom, 264 attenuation                                                             |
| ball property, 215, 236                                                                                                            |
| 296                                                                                                                                |
| beam-width of antenna, 258                                                                                                         |
| bipolar model, 18, 122                                                                                                             |
| baseband signal, 267, 273                                                                                                          |
| base station, 126, 147,                                                                                                            |

| blocking probability, 148, 149 rate, 152                                                                 |
|----------------------------------------------------------------------------------------------------------|
| BM, 163, see Boolean model 319 percolation, 163 bond percolation, 433 Boolean model (BM), 319 clump, 333 |
| connectivity in a finite window, 329 homogeneous, 322                                                    |
| percolation, 332 time-space, 111 bounded set, 261 broadcast, 61 BS, see base station 126                 |
| Campbell formula, 31, 277 , 278 , 388 higher order, 395 , 415                                            |
| reduced, 277 , 280 measure, 276                                                                          |
| higher order, 414 reduced, 276 , 414                                                                     |


<!-- p:201 -->


#### 446 INDEX

Campbell-Little-Mecke formula, see Campbell formula 277 Campbell-Matthes formula, 285, 340, 419, 420 measure, 285, 295, 418 capacity functional, see RAC ... 321 capture, 21 CDF, see contact distribution function 325 spherical, 325 CDMA, 126, see code division multiple access 288, 378 admission control, 138 power control, 129 rate control, 138 virtual load, 134 cell rejection probability, 142 chip, 280 clump, see BM ... 333 cluster head, 201, 295 coherence bandwidth, 275 distance, 261, 308, 313 time, 263, 275 collision, 286 complete independence, 265 concentrator, 296 connectivity of a BM in a finite window, see BM ... 329 contact distribution function, 325 contention domain, 286 continuum percolation, 329 counting measure, 261 covariance function, see RAC ... 324 coverage probability CSMA, 122 of a RAC, 326 CPR, see cell rejection probability 142 CSMA, 112, see carrier sense multiple access 288, 299 back-off, 113, 288 busy medium, 112 contention domain, 112, 288

detection threshold, 112, 114,

123 idle medium, 112 data rate, 279 dead end, 219 dead end problem, 183 Delaunay graph, 162, 181, 291 triangulation, 345 delay, 167 end-to-end, 214, 221, 242, 248 local, 82, 211, 214 delay rate, 213, 223 delay spread, 261 density of progress, 71 of successful transmissions, 15, 123 of throughput, 15 digital communication model, 11, 26, 167 Dijkstra's algorithm, 168, 238, 292 Dirac measure, 261 direct-sequence spread-spectrum, 280 directed spanning forest, 187 directional progress, 70 distribution circular-symmetric, 272 complex-valued Gaussian, 273 Gaussian, 269, 277 isotropic, 272 multinomial, 263 phase type, 359 diversity, 99 DL, see downlink 127 Doppler shift, 262 spread, 263, 275 downlink, 129, 296, 307 DSF, see directed spanning forest 187, see directed spanning forest 196 dynamic programming, 168, 292


<!-- p:202 -->


ergodicity, 189, 287, 288, 420 Erlang loss formula, 148 error probability, 278 ESN, see extremal shot-noise 316 Euclidean distance approximation, 177, 200 exchange formula, 343, 348 exclusion zone, 287

fading, 313 fast, 12, 83, 208, 220, 242 flat, 275, 276, 278, 280 heavy tailed, 99 lognormal, 99 Nakagami, 157, 270 Rayleigh, 34, 48, 49, 220, 254, 270 Rician, 34, 49, 254, 270 slow, 12, 83, 208, 242 Weibull, 99 far-field, 28, 257, 264 forest, 201 Fourier transform, 424

Gaussian vector, 272 goodput, 284 graph Boolean connectivity, 329 Delaunay, 162, 171, 174, 175, 177, 181, 200, 291 nearest neighbor, 431 random geometric, 162, 178, 181, 238, 329 SINR, 156, 163, 178, 401 connectivity, 63, 156, 401 time-space, 209, 235 strip, 188, 219 transmission range, 162, 291 graph distance, 167

hard core p.p., 296, 300 Hex, see honeycomb model 137 honeycomb model, 136, 137, 149, 307, 343

i.m.p.p., 114, see independently marked p.p. 292

INDEX 447

independent nearest receiver, 56 independent receiver model, 54 infinite connected component, 163, 178, 332, 334, 335, 337, 401, 402, 404 infinite server queue, 148 INR, see independent nearest receiver 56 intensity critical, 333, 404 measure, 262, 278 of a stationary p.p., 285, 418 interference, 21 cancellation factor, 128, 284, 404 field, 306 isotropy, 418

Johnson–Mehl cell, 363, 375, 399 jump vector, 161

Kendall-like notation, 23 for SINR cell, 356, 380 for SINR cell with fading, 361 for SINR coverage, 384 for SN, 307, 314 Kingman's theorem, 170, 222, 223

Lambert function, 76 local delay, 82, 211, 215, 219 multicast, 105 phase transition, 85, 90 Shannon, 102 locally finite measure, 261

m.p.p., see marked point process 291 MAC, 165, see medium access control 286 Aloha, 17 MANET, see mobile ad hoc network 273, 290, 307 Aloha, 18 nearest neighbor, 58 nearest receiver, 58 Poisson bipolar model, 18, 122 MANET receiver model, 55, 207


<!-- p:203 -->


#### 448 INDEX

MAP, see medium access probability 17, 45 mark of a point process, 190, 417 mass transport principle, 63, 68 Matérn p.p., 296 CSMA, 114 hard core, 296, 297 matched filter, 281, 288 measure Campbell m. of a p.p., 276 mean m. of a p.p., 276 medium access control, 286 probability, 17 MHC, see Matérn hard core 297, 418 minimal spanning tree, 179 minimum spanning tree, 429 MNN, see MANET nearest neighbor 58 MNR, see MANET nearest receiver 58 mobile ad hoc network, 273, 290 mobility, 13, 101, 273 high, 83, 274 moment measure factorial, 413 higher order, 395, 413, 416 MST, 179 multi-layer coding, 68 multicast, 61, 68, 105, 186, 295 one-to-many, 295 multipath fading, 261 multiple access carrier sense, 288 code division, 288 frequency division, 284 time division, 287 MWR, see minimal weight routing 168, 186 Nakagami fading, 157, 270 near-field, 28 nearest neighbor distance to, 280 graph, 431 in a cone, 98

nearest receiver in a cone, 80 network cellular, 136, 296, 307, 347 third generation, 296 delay tolerant, 13 interference limited, 95, 220, 356, 396 mobile ad hoc, 290 noise limited, 93, 220, 356, 396 sensor, 181, 201, 295 with periodic infrastructure, 100, 207 NNG, see nearest neighbor graph 431 non-outage, 21 NR, see routing; nearest receiver routing 56 number of hops, 161, 211, 248 omni-directional path-loss, 257, 306 OPL, 20, see omni-directional path loss 306 opportunism, 44, 165 opportunistic Aloha, 44, 206 choice of receiver, 70 routing, 206, 235 orthogonal signature sequence, 283, 378 p.p., see point process 261 packet, 18, 287 capture, 11, 205 velocity, 215, 224 packet model, 11, 82, 205 Painlevé-Kuratowski convergence, 363, 365, 372, 397, 399 Palm distribution, 189, 278 higher order, 415 of marks, 295, 418 reduced, 277, 415 version of a p.p. reduced, 280 Palm-Matthes distribution, 285, 289, 340, 343, 419, 420


<!-- p:204 -->


paradox Poisson p.p., 262 Feller's, 164, 342 homogeneous, 262 routing, 164, 251 Palm distribution passband signal, 267 k fold, 118 path-gain Poisson-Voronoi model, 136 distance and angle dependent, pole capacity, 65, 380 257 power control, 15, 126, 288 level-set, 260 cellular network, 128 path-loss feasibility, 129, 148 exponent, 258, 307 feasibility probability, 142, 148 price of anarchy, 164, 200 omni-directional, 257, 306 Peierls' argument, 407, 435 Prim's algorithm, 429 percolation principal value, 357, 427 processing gain, 280 Boolean, 183, 329 progress, 18, 30, 58, 161, 165, 188, first passage, 213, 222 214 of a BM, 332, see BM 404 directional, 70, 199, 245 of bonds, 174, 405, 406, 407, modified, 74 433 radial, 191 of sites, 171, 435, 437 pseudo-noise signature sequence, 280 SINR, 156, 179, 402 PV, see Poisson-Voronoi model 136 phase transition wireless contention, 85, 90, 95 QAM, see quadrature amplitude point average, 289 modulation 267 point map, 161, 180, 183, 216, 236 quadrature amplitude modulation, directional, 186, 187, 195, 215, 267 245 RAC, see random closed set 318 radial, 186, 214, 236 radial spanning tree, 181 time-space, 165, 213, 216, 236, radiation pattern, 258, 310 245 random point measure, 261, 417 closed ball, 319 point process, 261 closed set (RAC), 318 n-th factorial power, 395, 412 capacity functional, 321, n-th power, 412 357 ergodic, 23, 63, 287, 288 contact distribution isotropic, 418 function, 325 Laplace functional, 266 covariance function, 324, marked, 291, 417 360 independently, 292 coverage probability, 326 stationary, 294 translation invariant, 323 point transformation, 272 volume fraction, 323 Poisson, 262 compact set, 282 homogeneous, 262 cross-fading model, 21, 70, 135, simple, 264 315 stationary, 284, 417 sequential addition, 300 superposition, 269 walk, 273 thinning, 270 waypoint, 273


<!-- p:205 -->


450 INDEX

rate control, 127, 138, 145 Rayleigh fading, 34, 48, 49, 254, 270, 276, 278, 280, 308 response function, 300, 353, 364 Restart algorithm, 91, 98, 102 retention function, 270, 332 Rician fading, 34, 49, 254, 270 rotation operator, 418 route average, 163, 166, 198, 219, 224, 248, 289 time-space, 206, 215 routing, 161 best hop, 54, 181, 186, 235 cross-layer, 53, 69, 206, 235 directional, 195, 245, 246, 247 geographic, 180, 185, 251, 294 greedy, 165, 180, 235 largest bottleneck, 178 layer-aware, 205, 216 minimal delay, 176 minimal weight, 168, 291 multicast, 54, 193, 295 multihop, 161, 290, 336 nearest receiver, 55, 56, 58 next-in-strip, 183, 188, 219 opportunistic, 54, 69, 165, 206, 235 point-to-point, 181, 291, 295 radial, 190, 295 shortest path, 165, 168, 291 smallest hop, 53, 58, 80, 182, 186, 187, 192, 248 time-space, 165, 205, 215 time-space, 402 routing paradox, 164, 199, 251 routing table, 180, 294 RP, see radiation pattern 258 RST, see radial spanning tree 181, 186, 192, 197 internal, 201 local, 201

scaling law Gupta-Kumar, 29, 246 scaling laws, 29, 67, 69 scatterer, 261 self-avoidance, 222, 229 shadowing, 84 Shannon capacity, 11, 26, 40, 50, 158 multicast, 68 shift operator, 420 shot-noise, 21, 84, 209, 300 extremal, 75, 116, 119, 316 field, 301, 353, 405 time-space, 315 signal to interference and noise ratio, 353 signal to noise ratio, 362 signature, 280, 281, 283 singular integral, 357, 427 SINR, 282, see signal to interference and noise ratio 353 cell, 353, 377, 401 connectivity graph, 63 coverage, 21 coverage process, 383 graph, 156, 163, 178, 401 modified, 128, 134 neighbor, 62, 209, 216, 229 target, 128 site percolation, 437 Slivnyak's theorem, 278, 293, 386 higher order, 416 Slivnyak-Mecke theorem, see Slivnyak's theorem 278 slow fading, 208 small scale fading, 263 SN, see shot noise 21, see shot-noise 300 SNR, 278, see signal to noise ratio 362 SNR cell, 364 source-destination pair, 291 spanning tree, 429 spatial average, 63, 86, 102, 117, 164, 197, 199, 206, 287

S-D, see source-destination pair 291 saturated hard balls, 299 SBD, see spatial birth and death process 149 scale invariance, 177, 190


<!-- p:206 -->


birth and death process, 149 Erlang loss formula, 148, 152 reuse, 18, 287 spatial reuse factor, 42 spectral radius, 130, 289 sphere packing, 298, 300 standard stochastic scenario for SINR cell, 355 for SN, 167, 307 stopping set, 173, 282 strip graph, 188, 219 strong Markov property, 60, 232, 282 subadditive process, 170, 222, 223 successful reception, 21

INDEX 451

routing, 165, 215 shot-noise, 82, 315 SINR graph, 209 time-space routing, 402 traffic constant bit rate, 26 elastic, 138 translation operator, 417 transmission range, 163, 178, 238, 291 transport, 30, 58 tree spanning, 295 radial, 181 typical node, 22

TDMA, see Time Division multiple access 287 tessellation, 338 theorem Kingman's, 170, 222, 223 Slivnyak's, 190, 278, 280, 281, 293, 332, 386 higher order, 416 thermal noise, 20, 80, 129, 353 space independent, 356, 384 time independent, 356 thinning, 36, 114, 270, 297 independent, 20 throughput, 158, 178, 247 tilt, 257 time average, 102 time constant, 213 time slot, 12 time-space graph, 229 loss, 147 path, 210

UL, see uplink 127 universal marks, 419 uplink, 132, 296

virtual power, 20, 62, 122, 308, 313 volume fraction, 298, 323, 395 Voronoi cell, 136, 201, 339 fundamental region, 347 flower, 184, 347 neighbor, 162, 186, 291, 345, 346 tessellation, 155, 184, 338 VT, see Voronoi tessellation 338

WiFi, 122, 125, 290 mesh, 181, 295
