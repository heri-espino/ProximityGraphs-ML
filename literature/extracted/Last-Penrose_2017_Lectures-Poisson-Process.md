---
id: "Last-Penrose_2017_Lectures-Poisson-Process"
source_pdf: "../pdf/Last-Penrose_2017_Lectures-Poisson-Process.pdf"
source_filename: "Last-Penrose_2017_Lectures-Poisson-Process.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "full-page-ocr"
extraction_quality: "excellent"
extraction_score: 100.0
visual_assets: "disabled"
references_file: "../references/Last-Penrose_2017_Lectures-Poisson-Process.references.md"
---

<!-- p:1 -->

### Lectures on the Poisson Process

Günter Last and Mathew Penrose, Version from 21 August 2017, Commercial reproduction prohibited, to be published as IMS Textbook by Cambridge University Press, ©Günter Last and Mathew Penrose

Günter Last Institut für Stochastik, Karlsruhe Institute of Technology, Englerstraße 2, D-76128 Karlsruhe, Germany, guenter.last@kit.edu Mathew Penrose Department of Mathematical Sciences, University of Bath, Bath BA2 7AY, United Kingdom, m. d.penrose@bath. ac. uk


<!-- p:2 -->


4.5

36

#### Contents

| Preface         | Preface                                                  | page x   |
|-----------------|----------------------------------------------------------|----------|
| List of Symbols | List of Symbols                                          | xiii     |
| 1               | Poisson and Other Discrete Distributions                 | 1        |
| 1.1             | The Poisson Distribution                                 | 1        |
| 1.2             | Relationships Between Poisson and Binomial Distributions | 3        |
| 1.3             | The Poisson Limit Theorem                                | 4        |
| 1.4             | The Negative Binomial Distribution                       | 5        |
| 1.5             | Exercises                                                | 7        |
| 2               | Point Processes                                          | 9        |
| 2.1             | Fundamentals                                             | 9        |
| 2.2             | Campbell's Formula                                       | 12       |
| 2.3             | Distribution of a Point Process                          | 14       |
| 2.4             | Point Processes on Metric Spaces                         | 16       |
| 2.5             | Exercises                                                | 18       |
| 3               | Poisson Processes                                        | 19       |
| 3.1             | Definition of the Poisson Process                        | 19       |
| 3.2             | Existence of Poisson Processes                           | 20       |
| 3.3             | Laplace Functional of the Poisson Process                | 23       |
| 3.4             | Exercises                                                | 24       |
| 4               | The Mecke Equation and Factorial Measures                | 26       |
| 4.1             | The Mecke Equation                                       | 26       |
| 4.2             | Factorial Measures and the Multivariate Mecke Equation   | 28       |
| 4.3             | Janossy Measures                                         | 32       |
| 4.4             | Factorial Moment Measures                                | 34       |
| 4.5             | Exercises                                                | 36       |


<!-- p:3 -->


|   vi | Contents                                              |     |
|------|-------------------------------------------------------|-----|
|    5 | Mappings, Markings and Thinnings                      |  38 |
|  5.1 | Mappings and Restrictions                             |  38 |
|  5.2 | The Marking Theorem                                   |  39 |
|  5.3 | Thinnings                                             |  42 |
|  5.4 | Exercises                                             |  44 |
|    6 | Characterisations of the Poisson Process              |  46 |
|  6.1 | Borel Spaces                                          |  46 |
|  6.2 | Simple Point Processes                                |  49 |
|  6.3 | R ́ enyi's Theorem                                     |  50 |
|  6.4 | Completely Orthogonal Point Processes                 |  52 |
|  6.5 | Turning Distributional into Almost Sure Identities    |  54 |
|  6.6 | Exercises                                             |  56 |
|    7 | Poisson Processes on the Real Line                    |  58 |
|  7.1 | The Interval Theorem                                  |  58 |
|  7.2 | Marked Poisson Processes                              |  61 |
|  7.3 | Record Processes                                      |  63 |
|  7.4 | Polar Representation of Homogeneous Poisson Processes |  65 |
|  7.5 | Exercises                                             |  66 |
|    8 | Stationary Point Processes                            |  69 |
|  8.1 | Stationarity                                          |  69 |
|  8.2 | The Pair Correlation Function                         |  71 |
|  8.3 | Local Properties                                      |  74 |
|  8.4 | Ergodicity                                            |  75 |
|  8.5 | A Spatial Ergodic Theorem                             |  77 |
|  8.6 | Exercises                                             |  80 |
|    9 | The Palm Distribution                                 |  82 |
|  9.1 | Definition and Basic Properties                       |  82 |
|  9.2 | The Mecke-Slivnyak Theorem                            |  84 |
|  9.3 | Local Interpretation of Palm Distributions            |  85 |
|  9.4 | Voronoi Tessellations and the Inversion Formula       |  87 |
|  9.5 | Exercises                                             |  89 |
|   10 | Extra Heads and Balanced Allocations                  |  92 |
| 10.1 | The Extra Head Problem                                |  92 |
| 10.2 | The Point-Optimal Gale-Shapley Algorithm              |  95 |
| 10.3 | Existence of Balanced Allocations                     |  97 |
| 10.4 | Allocations with Large Appetite                       |  99 |
| 10.5 | The Modified Palm Distribution                        | 101 |
| 10.6 | Exercises                                             | 101 |

101


<!-- p:4 -->


|           | Contents                                               |   vii |
|-----------|--------------------------------------------------------|-------|
| 11        | Stable Allocations                                     |   103 |
| 11.1      | Stability                                              |   103 |
| 11.2      | The Site-Optimal Gale-Shapley Allocation               |   104 |
| 11.3      | Optimality of the Gale-Shapley Algorithms              |   104 |
| 11.4      | Uniqueness of Stable Allocations                       |   107 |
| 11.5      | Moment Properties                                      |   108 |
| 11.6      | Exercises                                              |   109 |
| 12        | Poisson Integrals                                      |   111 |
| 12.1      | The Wiener-Itˆ o Integral                              |   111 |
| 12.2      | Higher Order Wiener-Itˆ o Integrals                    |   114 |
| 12.3      | Poisson U-Statistics                                   |   118 |
| 12.4      | Poisson Hyperplane Processes                           |   122 |
| 12.5      | Exercises                                              |   124 |
| 13        | Random Measures and Cox Processes                      |   127 |
| 13.1      | Random Measures                                        |   127 |
| 13.2      | Cox Processes                                          |   129 |
| 13.3      | The Mecke Equation for Cox Processes                   |   131 |
| 13.4      | Cox Processes on Metric Spaces                         |   132 |
| 13.5      | Exercises                                              |   133 |
| 14        | Permanental Processes                                  |   136 |
| 14.1      | Definition and Uniqueness                              |   136 |
| 14.2      | The Stationary Case                                    |   138 |
| 14.3      | Moments of Gaussian Random Variables                   |   139 |
| 14.4      | Construction of Permanental Processes                  |   141 |
| 14.5      | Janossy Measures of Permanental Cox Processes          |   145 |
| 14.6      | One-Dimensional Marginals of Permanental Cox Processes |   147 |
| 14.7      | Exercises                                              |   151 |
| 15        | Compound Poisson Processes                             |   153 |
| 15.1      | Definition and Basic Properties                        |   153 |
| 15.2      | Moments of Symmetric Compound Poisson Processes        |   157 |
| 15.3      | Poisson Representation of Completely Random Measures   |   158 |
| 15.4      | Compound Poisson Integrals                             |   161 |
| 15.5      | Exercises                                              |   163 |
| 16        | The Boolean Model and the Gilbert Graph                |   166 |
| 16.1      | Capacity Functional                                    |   166 |
| 16.2      | Volume Fraction and Covering Property                  |   168 |
| 16.3 16.4 | Contact Distribution Functions                         |   170 |
|           | The Gilbert Graph                                      |   171 |


<!-- p:5 -->


viii Contents

- 16.5 The Point Process of Isolated Nodes 176

16.6

Exercises

177

- 17 The Boolean Model with General Grains 179
- 17.2 Spherical Contact Distribution Function and Covariance 182
- 17.1 Capacity Functional 179
- 17.3 Identifiability of Intensity and Grain Distribution 183
- 17.4 Exercises 185

#### 18 Fock Space and Chaos Expansion 187

- 18.2 Fock Space Representation 189
- 18.1 Difference Operators 187
- 18.3 The Poincaré Inequality 193
- 18.5 Exercises 195
- 18.4 Chaos Expansion 194

#### 19 Perturbation Analysis 197

19.1

A Perturbation Formula

197

- 19.2 Power Series Representation 200
- 19.4 Surface Density of the Boolean Model 206
- 19.3 Additive Functions of the Boolean Model 203
- 19.5 Mean Euler Characteristic of a Planar Boolean Model 207
- 19.6 Exercises 208

#### 20 Covariance Identities 211

- 20.2 Two Covariance Identities 214
- 20.1 Mehler's Formula 211
- 20.3 The Harris-FKG Inequality 217
- 20.4 Exercises 217

#### 21 Normal Approximation 219

- 21.2 Normal Approximation via Difference Operators 221
- 21.1 Stein's Method 219
- 21.3 Normal Approximation of Linear Functionals 225
- 21.4 Exercises 226
5. 22 Normal Approximation in the Boolean Model 227
- 22.2 Normal Approximation of Additive Functionals 230
- 22.1 Normal Approximation of the Volume 227
- 22.3 Central Limit Theorems 235
- 22.4 Exercises 237


<!-- p:6 -->


| Contents                                           |   ix |
|----------------------------------------------------|------|
| Appendix A Some Measure Theory                     |  239 |
| A.1 General Measure Theory                         |  239 |
| A.2 Metric Spaces                                  |  250 |
| A.3 Hausdor Measures and Additive Functionals      |  252 |
| A.4 Measures on the Real Half-Line                 |  257 |
| A.5 Absolutely Continuous Functions                |  259 |
| Appendix B Some Probability Theory                 |  261 |
| B.1 Fundamentals                                   |  261 |
| B.2 Mean Ergodic Theorem                           |  264 |
| B.3 The Central Limit Theorem and Stein's Equation |  266 |
| B.4 Conditional Expectations                       |  268 |
| B.5 Gaussian Random Fields                         |  269 |
| Appendix C Historical Notes                        |  272 |
| References                                         |  281 |
| Index                                              |  289 |


<!-- p:7 -->


## Preface

The Poisson process generates point patterns in a purely random manner. It plays a fundamental role in probability theory and its applications, and enjoys a rich and beautiful theory. While many of the applications involve point processes on the line, or more generally in Euclidean space, many others do not. Fortunately, one can develop much of the theory in the abstract setting of a general measurable space.

We have prepared the present volume so as to provide a modern textbook on the general Poisson process. Despite its importance, there are not many monographs or graduate texts with the Poisson process as their main point of focus, for example by comparison with the topic of Brownian motion. This is probably due to a viewpoint that the theory of Poisson processes on its own is too insubstantial to merit such a treatment. Such a viewpoint now seems out of date, especially in view of recent developments in the stochastic analysis of the Poisson process. We also extend our remit to topics in stochastic geometry, which is concerned with mathematical models for random geometric structures [4, 5, 23, 45, 123, 126, 147]. The Poisson process is fundamental to stochastic geometry, and the applications areas discussed in this book lie largely in this direction, reflecting the taste and expertise of the authors. In particular, we discuss Voronoi tessellations, stable allocations, hyperplane processes, the Boolean model and the Gilbert graph.

Besides stochastic geometry, there are many other fields of application of the Poisson process. These include Lévy processes [10, 83], Brownian excursion theory [140], queueing networks [6, 149], and Poisson limits in xit os tt o   s tr  it  tore we hope nevertheless that this book will be a useful resource for people working in these and related areas.

This book is intended to be a basis for graduate courses or seminars on the Poisson process. It might also serve as an introduction to point process theory. Each chapter is supposed to cover material that can be presented


<!-- p:8 -->


(at least in principle) in a single lecture. In practice, it may not always be possible to get through an entire chapter in one lecture; however, in most chapters the most essential material is presented in the early part of the chapter, and the later part could feasibly be left as background reading if necessary. While it is recommended to read the earlier chapters in a linear order at least up to Chapter 5, there is some scope for the reader to pick and choose from the later chapters. For example, a reader more interested in stochastic geometry could look at Chapters 8–11 and 16–17. A reader wishing to focus on the general abstract theory of Poisson processes could look at Chapters 6, 7, 12, 13 and 18–21. A reader wishing initially to take on slightly easier material could look at Chapters 7–9, 13 and 15–17.

The book divides loosely into three parts. In the first part we develop basic results on the Poisson process in the general setting. In the second part we introduce models and results of stochastic geometry, most but not all of which are based on the Poisson process, and which are most naturally developed in the Euclidean setting. Chapters 8, 9, 10, 16, 17 and 22 are devoted exclusively to stochastic geometry while other chapters use stochastic geometry models for illustrating the theory. In the third part we return to the general setting and describe more advanced results on the stochastic analysis of the Poisson process.

Our treatment requires a sound knowledge of measure-theoretic probability theory. However, specific knowledge of stochastic processes is not assumed. Since the focus is always on the probabilistic structure, technical issues of measure theory are kept in the background, whenever possible. Some basic facts from measure and probability theory are collected in the appendices.

When treating a classical and central subject of probability theory, a certain overlap with other books is inevitable. Much of the material of the earlier chapters, for instance, can also be found (in a slightly more restricted form) in the highly recommended book [75] by J.F.C. Kingman. Further results on Poisson processes, as well as on general random measures and point processes, are presented in the monographs [6, 23, 27, 53, 62, 63, 69, 88, 107, 134, 139]. The recent monograph Kallenberg [65] provides an excellent systematic account of the modern theory of random measures. Comments on the early history of the Poisson process, on the history of the main results presented in this book and on the literature are given in Appendix C.

In preparing this manuscript we have benefited from comments on earlier versions from Daryl Daley, Fabian Gieringer, Christian Hirsch, Daniel Hug, Olav Kallenberg, Paul Keeler, Martin Möhle, Franz Nestmann, Jim Pitman, Matthias Schulte, Tomasz Rolski, Dietrich Stoyan, Christoph Thäle, Hermann Thorisson and Hans Zessin, for which we are most grateful. Thanks are due to Franz Nestmann for producing the figures. We also wish to thank Olav Kallenberg for making available to us an early version of his monograph [65].


<!-- p:9 -->


Günter Last, Mathew Penrose August 2017


<!-- p:10 -->


## Symbols

| Z = f 0 ; 1 ; 1 ; 2 ; 2 ; : : : g    | set of integers                                              |
|--------------------------------------|--------------------------------------------------------------|
| N = f 1 ; 2 ; 3 ; 4 ; : : : g        | set of positive integers                                     |
| N 0 = f 0 ; 1 ; 2 ; : : : g          | set of non-negative integers                                 |
| N = N [ f1g                          | extended set of positive integers                            |
| N 0 = N 0 [ f1g                      | extended set of non-negative integers                        |
| R = ( 1 ; 1 ) ; R + = [0 ; 1 )       | real line (resp. non-negative real half-line)                |
| R = R [ f 1 ; 1g                     | extended real line                                           |
| R + = R + [ f1g = [0 ; 1 ]           | extended half-line                                           |
| R ( X ) ; R + ( X )                  | R -valued (resp. R + -valued) measurable functions on X      |
| u + ; u                              | positive and negative part of an R -valued function u        |
| a ^ b ; a _ b                        | minimum (resp. maximum) of a ; b 2 R                         |
| 1 f g                                | indicator function                                           |
| a : = 1 f a , 0 g a 1                | generalised inverse of a 2 R                                 |
| card A = j A j                       | number of elements of a set A                                |
| [ n ]                                | f 1 ; : : : ; n g                                            |
| n                                    | group of permutations of [ n ]                               |
| n ; n                                | set of all partitions (resp. subpartitions) of [ n ]         |
| ( n ) k = n ( n k + 1)               | descending factorial                                         |
| x                                    | Dirac measure at the point x                                 |
| N < 1 ( X ) N < 1                    | set of all finite counting measures on X                     |
| N ( X ) N                            | set of all countable sums of measures from N < 1             |
| N l ( X ) ; N s ( X )                | set of all locally finite (resp. simple) measures in N ( X ) |
| N ls ( X ) : = N l ( X ) \ N s ( X ) | set of all locally finite and simple measures in N ( X )     |
| x 2                                  | short for f x g = ( f x g ) > 0, 2 N                         |
|                                      | restriction of a measure to a measurable set B               |


<!-- p:11 -->


| B ( X )                  | Borel -field on a metric space X                        |
|--------------------------|---------------------------------------------------------|
| X b                      | bounded Borel subsets of a metric space X               |
| R d                      | Euclidean space of dimension d 2 N                      |
| B d : = B ( R d )        | Borel -field on R d                                     |
| d                        | Lebesgue measure on ( R d ; B d )                       |
| k k                      | Euclidean norm on R d                                   |
| h ; i                    | Euclidean scalar product on R d                         |
| C d ; C ( d )            | compact (resp. non-empty compact) subsets of R d        |
| K d ; K ( d )            | compact (resp. non-empty compact) convex subsets of R d |
| R d                      | convex ring in R d (finite unions of convex sets)       |
| K + x ; K x              | translation of K R d by x (resp. x )                    |
| K L                      | Minkowski sum of K ; L R d                              |
| V 0 ; : : : ; V d        | intrinsic volumes                                       |
| i = Z V i ( K ) Q ( dK ) | i -th mean intrinsic volume of a typical grain          |
| B ( x ; r )              | closed ball with centre x and radius r 0                |
| d = d ( B d )            | volume of the unit ball in R d                          |
| <                        | strict lexicographical order on R d                     |
| l ( B )                  | lexicographic minimum of a non-empty finite set B R d   |
| ( ; F ; P )              | probability space                                       |
| E [ X ]                  | expectation of a random variable X                      |
| V ar[ X ]                | variance of a random variable X                         |
| C ov[ X ; Y ]            | covariance between random variables X and Y             |
| L                        | Laplace functional of a random measure                  |
| d = ; d !                | equality (resp. convergence) in distribution            |


<!-- p:12 -->


1

## Poisson and Other Discrete Distributions

The Poisson distribution arises as a limit of the binomial distribution. This chapter contains a brief discussion of some of its fundamental properties as well as the Poisson limit theorem for null arrays of integer-valued random variables. The chapter also discusses the binomial and negative binomial distributions.

### 1.1 The Poisson Distribution

A random variable X is said to have a binomial distribution Bi(n, p) with parameters n ∈ N0 := {0, 1, 2, . . .} and p ∈ [0, 1] if

$$\mathbb { P } ( X = k ) = \text {Bi} ( n , p ; k ) \colon = \binom { n } { k } p ^ { k } ( 1 - p ) ^ { n - k } , \quad k = 0 , \dots , n ,$$

where 00 := 1. In the case n = 1 this is the Bernoulli distribution with parameter p. If X1, ... , X are independent random variables with such a Bernoulli distribution, then their sum has a binomial distribution, that is

$$X _ { 1 } + \dots + X _ { n } \stackrel { d } { = } X ,$$

where X has the distribution Bi(n, p) and where ≡ denotes equality in distribution. It follows that the expectation and variance of X are given by

$$\mathbb { E } [ X ] = n p , \quad \mathbb { V } a r [ X ] = n p ( 1 - p ) .$$

A random variable X is said to have a Poisson distribution Po(γ) with parameter γ ≥ 0 if

$$\mathbb { P } ( X = k ) = \text {Po} ( \gamma ; k ) \colon = \frac { \gamma ^ { k } } { k ! } e ^ { - \gamma } , \quad k \in \mathbb { N } _ { 0 } .$$

If γ = 0, then P(X = 0) = 1, since we take 00 = 1. Also we allow γ = ∞; in this case we put P(X = ∞) = 1 so Po(∞; k) = 0 for k ∈ N0.

The Poisson distribution arises as a limit of binomial distributions as follows. Let pn ∈ [0, 1], n ∈ N, be a sequence satisfying npn → γ as n → ∞, with γ ∈ (0, ∞). Then, for k ∈ {0, . . . , n},


<!-- p:13 -->


$$\left ( \binom { n } { k } p _ { n } ^ { k } ( 1 - p _ { n } ) ^ { n - k } = \frac { ( n p _ { n } ) ^ { k } } { k ! } \cdot \frac { ( n ) _ { k } } { n ^ { k } } \cdot ( 1 - p _ { n } ) ^ { - k } \cdot \left ( 1 - \frac { n p _ { n } } { n } \right ) ^ { n } \to \frac { \gamma ^ { k } } { k ! } e ^ { - \gamma } , \ ( 1 . 5 )$$

as n → ∞, where

$$( n ) _ { k } \colon = n ( n - 1 ) \cdots ( n - k + 1 )$$

is the k-th descending factorial (of n) with (n)0 interpreted as 1.

Suppose X is a Poisson random variable with finite parameter γ. Then its expectation is given by

$$\mathbb { E } [ X ] = e ^ { - \gamma } \sum _ { k = 0 } ^ { \infty } k \frac { \gamma ^ { k } } { k ! } = e ^ { - \gamma } \gamma \sum _ { k = 1 } ^ { \infty } \frac { \gamma ^ { k - 1 } } { ( k - 1 ) ! } = \gamma .$$

The probability generating function of X (or of Po(γ)) is given by

$$\mathbb { E } [ s ^ { X } ] = e ^ { - \gamma } \sum _ { k = 0 } ^ { \infty } \frac { \gamma ^ { k } } { k ! } s ^ { k } = e ^ { - \gamma } \sum _ { k = 0 } ^ { \infty } \frac { ( \gamma s ) ^ { k } } { k ! } = e ^ { \gamma ( s - 1 ) } , \quad s \in [ 0 , 1 ] .$$

It follows that the Laplace transform of X (or of Po(γ)) is given by

$$\mathbb { E } [ e ^ { - t X } ] = \exp [ - \gamma ( 1 - e ^ { - t } ) ] , \quad t \geq 0 .$$

Formula (1.8) is valid for each s ∈ R and (1.9) is valid for each t ∈ R. A calculation similar to (1.8) shows that the factorial moments of X are given by

$$\mathbb { E } [ ( X ) _ { k } ] = \gamma ^ { k } , \ \ k \in \mathbb { N } _ { 0 } ,$$

where (0)0 := 1 and (0)k := 0 for k ≥ 1. Equation (1.10) implies that

$$\mathbb { V } a r [ X ] = \mathbb { E } [ X ^ { 2 } ] - \mathbb { E } [ X ] ^ { 2 } = \mathbb { E } [ ( X ) _ { 2 } ] + \mathbb { E } [ X ] - \mathbb { E } [ X ] ^ { 2 } = \gamma .$$

We continue with a characterisation of the Poisson distribution.

Proposition 1.1 An N0-valued random variable X has distribution Po(γ) if and only if, for every function f : N0 → R+, we have

$$\mathbb { E } [ X f ( X ) ] = \gamma \, \mathbb { E } [ f ( X + 1 ) ] .$$

Proof By a similar calculation to (1.7) and (1.8) we obtain for any function f : N0 → R+ that (1.12) holds. Conversely, if (1.12) holds for all such functions f, then we can make the particular choice f := 1{k} for k ∈ N, to obtain the recursion

$$k \, \mathbb { P } ( X = k ) = \gamma \, \mathbb { P } ( X = k - 1 ) .$$


<!-- p:14 -->


This recursion has (1.4) as its only (probability) solution, so the result follows. □

### 1.2 Relationships Between Poisson and Binomial Distributions

The next result says that if X and Y are independent Poisson random variables, then X + Y is also Poisson and the conditional distribution of X given X + Y is binomial:

Proposition 1.2 Let X and Y be independent with distributions Po(γ) and Po(δ), respectively, with 0 &lt; γ+δ &lt; ∞. Then X+Y has distribution Po(γ+δ) and

$$\mathbb { P } ( X = k \, | \, X + Y = n ) = \text {Bi} ( n , \gamma / ( \gamma + \delta ) ; k ) , \quad n \in \mathbb { N } _ { 0 } , \, k = 0 , \dots , n .$$

Proof For n ∈ N0 and k ∈ {0, . . . , n},

$$\text {Proof} \quad \text {For } n \in \mathbb { N } _ { 0 } \text { and } k \in \{ 0 , \dots , n \} , \\ \mathbb { P } ( X = k , X + Y = n ) = \mathbb { P } ( X = k , Y = n - k ) = \frac { \gamma ^ { k } } { k ! } e ^ { - \gamma } \frac { \delta ^ { n - k } } { ( n - k ) ! } e ^ { - \delta } \\ = e ^ { - ( \gamma + \delta ) } \left ( \frac { ( \gamma + \delta ) ^ { n } } { n ! } \right ) \binom { n } { k } \left ( \frac { \gamma } { \gamma + \delta } \right ) \left ( \frac { \delta } { \gamma + \delta } \right ) ^ { n - k } \\ = \text { } P o ( \gamma + \delta ; n ) \text { Bi} ( n , \gamma / ( \gamma + \delta ) ; k ) , \\ \intertext { \text { and the associated follow } } \text { } \intertext { o n d } \text { the associated follow } \text { } \intertext { o f } \text { } \intertext { i n } \text { } \intertext { e } \text { } \intertext { s e c t i o n } \text { } \intertext { f o l l } \text { } \intertext { i n } \text { } \intertext { s e c t i o n } \text { } \intertext { i n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { i n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n } \text { } \intertext { s e c t i o n$$

and the assertions follow.

□

Let Z be an N0-valued random variable and let Z1, Z2, . . . be a sequence of independent random variables that have a Bernoulli distribution with parameter p ∈ [0, 1]. If Z and (Z)n≥1 are independent, then the random variable

$$X \coloneqq \sum _ { j = 1 } ^ { z } Z _ { j }$$

is called a p-thinning of Z, where we set X := 0 if Z = 0. This means that the conditional distribution of X given Z = n is binomial with parameters n and p.

The following partial converse of Proposition 1.2 is a noteworthy property of the Poisson distribution.

Proposition 1.3 Let p ∈ [0, 1]. Let Z have a Poisson distribution with parameter γ ≥ 0 and let X be a p-thinning of Z. Then X and Z − X are independent and Poisson distributed with parameters pγ and (1 – p)γ, respectively.

e~δ


<!-- p:15 -->


Proof We may assume that γ &gt; 0. The result follows once we have shown that

$$\mathbb { P } ( X = m , Z - X = n ) = \text {Po} ( p \gamma ; m ) \text {Po} ( ( 1 - p ) \gamma ; n ) , \quad m , n \in \mathbb { N } _ { 0 } . \quad ( 1 . 1 4 )$$

Since the conditional distribution of X given Z = m + n is binomial with parameters m + n and p, we have

$$\mathbb { P } ( X = m , Z - X = n ) & = \mathbb { P } ( Z = m + n ) \, \mathbb { P } ( X = m \, | \, Z = m + n ) \\ & = \left ( \frac { e ^ { - \gamma } \gamma ^ { m + n } } { ( m + n ) ! } \right ) \binom { m + n } { m } p ^ { m } ( 1 - p ) ^ { n } \\ & = \left ( \frac { p ^ { m } \gamma ^ { n } } { m ! } \right ) e ^ { - p \gamma } \left ( \frac { ( 1 - p ) ^ { n } \gamma ^ { n } } { n ! } \right ) e ^ { - ( 1 - p ) \gamma } , \\ \intertext { a n d ( 1 4 ) follows } \mathbb { P } ( X = m , Z - X = n ) & = \left ( \frac { p ^ { m } \gamma ^ { n } } { m ! } \right ) e ^ { - p \gamma } \left ( \frac { ( 1 - p ) ^ { n } \gamma ^ { n } } { n ! } \right ) e ^ { - ( 1 - p ) \gamma } , \\$$

and (1.14) follows.

□

### 1.3 The Poisson Limit Theorem

The next result generalises (1.5) to sums of Bernoulli variables with unequal parameters, among other things.

Proposition 1.4 Suppose for n ∈ N that mn ∈ N and Xn,1, . . . , Xn,m are independent random variables taking values in No. Let pn,i := P(Xn,i ≥ 1) and assume that

$$\lim _ { n \to \infty } \max _ { 1 \leq i \leq m _ { n } } p _ { n , i } = 0 .$$

$$\lim _ { n \to \infty } \sum _ { i = 1 } ^ { m _ { n } } \mathbb { P } ( X _ { n , i } \geq 2 ) = 0 .$$

Let Xn := Σi=1 Xn,i. Then for k ∈ N0 we have

$$\lim _ { n \to \infty } \mathbb { P } ( X _ { n } = k ) = \text {Po} ( \gamma ; k ) .$$

Proof Let X′,i := 1{Xn,i ≥ 1} = min{Xn,i, 1} and X′ := ∑i=1 X′,i. Since Xn,i ≠ Xn,i if and only if Xn,i ≥ 2, we have

$$\mathbb { P } ( X ^ { \prime } _ { n } \neq X _ { n } ) \leq \sum _ { i = 1 } ^ { m _ { n } } \mathbb { P } ( X _ { n , i } \geq 2 ) .$$

By assumption (1.16) we can assume without restriction of generality that Xn,i = Xn,i for all n ∈ N and i ∈ {1, . . . , mn}. Moreover it is no loss of generality to assume for each (n, i) that pn,i &lt; 1. We then have


<!-- p:16 -->


$$\mathbb { P } ( X _ { n } = k ) = \sum _ { 1 \leq i _ { 1 } < i _ { 2 } < \cdots < i _ { k } \leq m _ { n } } p _ { n , i _ { 1 } } p _ { n , i _ { 2 } } \cdots p _ { n , i _ { k } } \frac { \prod _ { j = 1 } ^ { m _ { n } } ( 1 - p _ { n , j } ) } { ( 1 - p _ { n , i _ { 1 } } ) \cdots ( 1 - p _ { n , i _ { k } } ) } .$$

Let μn := max1≤i≤mn Pn,i. Since ∑j1 Pn,j ≤ λμn → 0 as n → ∞, we have

$$\log \left ( \prod _ { j = 1 } ^ { m _ { n } } ( 1 - p _ { n , j } ) \right ) = \sum _ { j = 1 } ^ { m _ { n } } ( - p _ { n , j } + O ( p _ { n , j } ^ { 2 } ) ) \rightarrow - \gamma \text { as } n \rightarrow \infty ,$$

where the function O(·) satisfies lim supr→0 |r|−1|O(r)| &lt; ∞. Also,

$$\inf _ { 1 \leq i _ { 1 } < i _ { 2 } < \cdots < i _ { k } \leq n _ { n _ { i } } } ( 1 - p _ { n , i _ { 1 } } ) \cdots ( 1 - p _ { n , i _ { k } } ) \geq ( 1 - \mu _ { n } ) ^ { k } \to 1 \text { as } n \to \infty . \ \ ( 1 . 2 0 )$$

denoting summation over all ordered k-tuples of distinct elements of {1, 2, . . . , mn}, we have

$$k ! \sum _ { 1 \leq i _ { 1 } < i _ { 2 } < \cdots < i _ { k } \leq m _ { n } } p _ { n , i _ { 1 } } p _ { n , i _ { 2 } } \cdots p _ { n , i _ { k } } = \sum _ { i _ { 1 } , \dots , i _ { k } \in \{ 1 , 2 , \dots , m _ { n } \} } ^ { \neq } p _ { n , i _ { 1 } } p _ { n , i _ { 2 } } \cdots p _ { n , i _ { k } } ,$$

and

$$0 & \leq \left ( \sum _ { i = 1 } ^ { m _ { n } } p _ { n , i } \right ) ^ { k } - \sum _ { i _ { 1 } , \dots , i _ { k } \in \{ 1 , 2 , \dots , m _ { n } \} } ^ { \neq } p _ { n , i _ { 1 } } p _ { n , i _ { 2 } } \cdots p _ { n , i _ { k } } \\ & \leq \left ( \begin{matrix} k \\ 2 \end{matrix} \right ) \sum _ { i = 1 } ^ { m _ { n } } p _ { n , i } ^ { 2 } \left ( \sum _ { j = 1 } ^ { m _ { n } } p _ { n , j } \right ) ^ { k - 2 } , \\ \intertext { t o n d e s } \intertext { t o r a $ o r $ a n }$$

which tends to zero as n → ∞. Therefore

$$k ! \sum _ { 1 \leq i _ { 1 } < i _ { 2 } < \cdots < i _ { k } \leq m _ { n } } p _ { n , i _ { 1 } } p _ { n , i _ { 2 } } \cdots p _ { n , i _ { k } } \to \gamma ^ { k } \text { as } n \to \infty .$$

The result follows from (1.18) by using (1.19), (1.20) and (1.21). □

### 1.4 The Negative Binomial Distribution

A random element Z of N0 is said to have a negative binomial distribution with parameters r &gt; 0 and p ∈ (0, 1] if

$$\mathbb { P } ( Z = n ) = \frac { \Gamma ( n + r ) } { \Gamma ( n + 1 ) \Gamma ( r ) } ( 1 - p ) ^ { n } p ^ { r } , \quad n \in \mathbb { N } _ { 0 } , \quad ( 1 . 2 2 )$$


<!-- p:17 -->


where the Gamma function Γ: (0, ∞) → (0, ∞) is defined by

$$\Gamma ( a ) \colon = \int _ { 0 } ^ { \infty } t ^ { a - 1 } e ^ { - t } \, d t , \quad a > 0 .$$

(In particular Γ(a) = (a− 1)! for a ∈ N.) This can be seen to be a probability distribution by Taylor expansion of (1 − x)−′ evaluated at x = 1 − p. The probability generating function of Z is given by

$$\mathbb { E } [ s ^ { Z } ] = p ^ { r } ( 1 - s + s p ) ^ { - r } , \quad s \in [ 0 , 1 ] .$$

For r ∈ N, such a Z may be interpreted as the number of failures before the rth success in a sequence of independent Bernoulli trials. In the special case r = 1 we get the geometric distribution

$$\mathbb { P } ( Z = n ) = ( 1 - p ) ^ { n } p , \ \ n \in \mathbb { N } _ { 0 } .$$

Another interesting special case is r = 1/2. In this case

$$\mathbb { P } ( Z = n ) = \frac { ( 2 n - 1 ) ! ! } { 2 ^ { n } n ! } ( 1 - p ) ^ { n } p ^ { 1 / 2 } , \quad n \in \mathbb { N } _ { 0 } , \quad ( 1 . 2 6 )$$

where we recall the definition (B.6) for (2n – 1)!!. This follows from the fact that Γ(n + 1/2) = (2n − 1)!! 2−n √π, n ∈ N0.

The negative binomial distribution arises as a mixture of Poisson distributions. To explain this, we need to introduce the Gamma distribution with shape parameter a &gt; 0 and scale parameter b &gt; 0. This is a probability measure on R+ with Lebesgue density

$$x \mapsto b ^ { a } \Gamma ( a ) ^ { - 1 } x ^ { a - 1 } e ^ { - b x }$$

on R+. If a random variable Y has this distribution, then one says that Y is Gamma distributed with shape parameter a and scale parameter b. In this case Y has Laplace transform

$$\mathbb { E } [ e ^ { - t Y } ] = \left ( \frac { b } { b + t } \right ) ^ { a } , \quad t \geq 0 .$$

In the case a = 1 we obtain the exponential distribution with parameter b. Exercise 1.11 asks the reader to prove the following result.

Proposition 1.5 Suppose that the random variable Y ≥ 0 is Gamma distributed with shape parameter a &gt; 0 and scale parameter b &gt; 0. Let Z be an N0-valued random variable such that the conditional distribution of Z given Y is Po(Y). Then Z has a negative binomial distribution with parameters a and b/(b + 1).


<!-- p:18 -->


### 1.5 Exercises

Exercise 1.1 Prove equation (1.10).

Exercise 1.2 Let X be a random variable taking values in N0. Assume that there is a γ ≥ 0 such that E[(X)k] = γk for all k ∈ N0. Show that X has a Poisson distribution. (Hint: Derive the Taylor series for g(s) := E[sX] at S0 = 1.)

Exercise 1.3 Confirm Proposition 1.3 by showing that

$$\mathbb { E } [ s ^ { X } t ^ { Z - X } ] = e ^ { p \gamma ( s - 1 ) } e ^ { ( 1 - p ) \gamma ( t - 1 ) } , \ \ s , t \in [ 0 , 1 ] ,$$

using a direct computation and Proposition B.4.

Exercise 1.4 (Generalisation of Proposition 1.2) Let m ∈ N and suppose that X1, ... , Xm are independent random variables with Poisson distribui X + . . . + X =: X    (     (  s Poisson distributed with parameter γ := γ1 + · . . + γm. Assuming γ &gt; 0, show moreover for any k ∈ N that

$$\mathbb { P } ( X _ { 1 } = k _ { 1 } , \dots , X _ { m } = k _ { m } \, | \, X = k ) = \frac { k ! } { k _ { 1 } ! \cdots k _ { m } ! } \left ( \frac { \gamma _ { 1 } } { \gamma } \right ) ^ { k _ { 1 } } \cdots \left ( \frac { \gamma _ { m } } { \gamma } \right ) ^ { k _ { m } } \quad ( 1 . 2 9 )$$

for k1 + ·. · + km = k. This is a multinomial distribution with parameters k and γ1/γ, . . . , γm/γ.

Exercise 1.5 (Generalisation of Proposition 1.3) Let m ∈ N and suppose that Z, n ∈ N, is a sequence of independent random vectors in Rm with common distribution P(Z1 = e) = pi, i ∈ {1, . . . , m}, where ei is the i-th unit vector in Rn and p1 + · . · + pm = 1. Let Z have a Poisson distribution with parameter γ, independent of (Z1, Z2, . . .). Show that the components of the random vector X := Σ=1 Zj are independent and Poisson distributed with parameters p1γ, . . . , Pmγ.

Exercise 1.6 (Bivariate extension of Proposition 1.4) Let γ &gt; 0, δ ≥ 0. Suppose for n ∈ N that mn ∈ N and for 1 ≤ i ≤ mn that pn,i, qn,i ∈ [0, 1) as n → ∞. Suppose for n ∈ N that (Xn, Yn) = ∑i=1(Xn,i, n,), where each (X,i, Yn,i) is a random 2-vector whose components are Bernoulli distributed with parameters pn,i, qn,i, respectively, and satisfy X,Yn,i = 0 almost surely. Assume the random vectors (X,i, Yn,i), 1 ≤ i ≤ m, are independent. Prove that X, Yn are asymptotically (as n → ∞) distributed as a pair of independent Poisson variables with parameters γ, δ, i.e. for k, l ∈ N0,


<!-- p:19 -->


$$\lim _ { n \to \infty } \mathbb { P } ( X _ { n } = k , Y _ { n } = \ell ) = e ^ { ( n * n ) } \frac { } { k ! \ell ! } .$$

Exercise 1.7 (Probability of a Poisson variable being even) Suppose X is Poisson distributed with parameter γ &gt; 0. Using the fact that the probability generating function (1.8) extends to s = -1, verify the identity P(X/2 ∈ Z) = (1 + e−2γ)/2. For k ∈ N with k ≥ 3, using the fact that the probability generating function (1.8) extends to a k-th complex root of unity, find a closed-form formula for P(X/k ∈ Z).

Exercise 1.8 Let γ &gt; 0, and suppose X is Poisson distributed with param&lt; 3  t ∞ &gt; [1 t ss  + ←  : f   ) Show that E[f(X + k)] &lt; ∞ for any k ∈ N.

Exercise 1.9 Let 0 &lt; γ &lt; γ'. Give an example of a random vector (X, Y) with X Poisson distributed with parameter γ and Y Poisson distributed with parameter γ', such that Y–X is not Poisson distributed. (Hint: First consider a pair X', Y' such that Y'-X' is Poisson distributed, and then modify finitely many of the values of their joint probability mass function.)

Exercise 1.10 Suppose n ∈ N and set [n] := {1, . . . , n}. Suppose that Z is a uniform random permutation of [n], that is a random element of the space Σ of all bijective mappings from [n] to [n] such that P(Z = π) = 1/n! for each π ∈ Σ. For a ∈ R let [a] := min{k ∈ Z : k ≥ a}. Let γ ∈ [0, 1] and let X := card{i ∈ [[γn]] : Z(i) = i} be the number of fixed points of Z among the first [yn] integers. Show that the distribution of X converges to Po(γ), that is

$$\lim _ { n \to \infty } \mathbb { P } ( X _ { n } = k ) = \frac { \gamma ^ { k } } { k ! } e ^ { - \gamma } , \ \ k \in \mathbb { N } _ { 0 } .$$

(Hint: Establish an explicit formula for P(X = k), starting with the case k = 0.)

Exercise 1.11 Prove Proposition 1.5.

Exercise 1.12 Let γ &gt; 0 and δ &gt; 0. Find a random vector (X, Y) such that X, Y and X + Y are Poisson distributed with parameter γ, δ and γ + δ, respectively, but X and Y are not independent.


<!-- p:20 -->


## Point Processes

A point process is a random collection of at most countably many points, possibly with multiplicities. This chapter defines this concept for an arbitrary measurable space and provides several criteria for equality in distribution.

### 2.1 Fundamentals

The idea of a point process is that of a random, at most countable, collection Z of points in some space X. A good example to think of is the d-dimensional Euclidean space Rd. Ignoring measurability issues for the moment, we might think of Z as a mapping ω → Z(ω) from Ω into the system of countable subsets of X, where (Ω, F, P) is an underlying probability space. Then Z can be identified with the family of mappings

$$\omega \mapsto \eta ( \omega , B ) \colon = \text {card} ( Z ( \omega ) \cap B ) , \ \ B \subset \mathbb { X } ,$$

counting the number of points that Z has in B. (We write card A for the number of elements of a set A.) Clearly, for any fixed ω ∈ Ω the mapping η(ω, ·) is a measure, namely the counting measure supported by Z(ω). It turns out to be a mathematically fruitful idea to define point processes as random counting measures.

To give the general definition of a point process let (X, X) be a measurable space. Let N&lt;∞(X) ≡ N&lt;∞ denote the space of all measures μ on X such that μ(B) ∈ N0 := N ∪ {0} for all B ∈ X, and let N(X) ≡ N be the space of all measures that can be written as a countable sum of measures from N&lt;∞. A trivial example of an element of N is the zero measure 0 that is identically zero on X. A less trivial example is the Dirac measure δx at a point x ∈ X given by δx(B) := 1B(x). More generally, any (finite or infinite) sequence (xn)k=1 of elements of X, where k ∈ N := N ∪ {∞} is the number of terms in the sequence, can be used to define a measure


<!-- p:21 -->


$$\mu = \sum _ { n = 1 } ^ { k } \delta _ { x _ { n } } .$$

$$\mu ( B ) = \sum _ { n = 1 } ^ { k } 1 _ { B } ( x _ { n } ) , \quad B \in \mathcal { X } .$$

More generally we have, for any measurable f : X → [0, ∞], that

$$\int f d \mu = \sum _ { n = 1 } ^ { k } f ( x _ { n } ) .$$

We can allow for k = 0 in (2.1). In this case μ is the zero measure. The points x1, X2, . .. are not assumed to be pairwise distinct. If xi = xj for some i, j ≤ k with i ≠ j, then μ is said to have multiplicities. In fact, the multiplicity of x is the number card{ j ≤ k : xj = x}. Any μ of the form (2.1) is interpreted as a counting measure with possible multiplicities.

In general one cannot guarantee that any μ ∈ N can be written in the form (2.1); see Exercise 2.5. Fortunately, only weak assumptions on (X, X) and μ are required to achieve this; see e.g. Corollary 6.5. Moreover, large parts of the theory can be developed without imposing further assumptions on (X, X), other than to be a measurable space.

A measure v on X is said to be s-finite if v is a countable sum of finite measures. By definition, each element of N is s-finite. We recall that a measure v on X is said to be σ-finite if there is a sequence Bm ∈ X, m ∈ N, such that ∪Bm = X and v(B) &lt; ∞ for all m ∈ N. Clearly every σ-finite measure is s-finite. Any N0-valued σ-finite measure is in N. In contrast to σ-finite measures, any countable sum of s-finite measures is again s-finite. If the points x in (2.1) are all the same, then this measure μ is not σ-finite. The counting measure on R (supported by R) is an example of a measure with values in N0 := Ñ ∪ {0}, that is not s-finite. Exercise 6.10 gives an example of an s-finite N0-valued measure that is not in N.

Let N(X) ≡ N denote the σ-field generated by the collection of all subsets of N of the form

$$\{ \mu \in \mathbf N \colon \mu ( B ) = k \} , \ \ B \in \mathcal { X } , \, k \in \mathbb { N } _ { 0 } .$$

This means that N is the smallest σ-field on N such that μ → μ(B) is measurable for all B ∈ X.

Then μ ∈ N and Definition 2.1 A point process on X is a random element η of (N, N), that is a measurable mapping η: Ω → N.


<!-- p:22 -->


If η is a point process on X and B ∈ X, then we denote by η(B) the mapping ω → η(ω, B) := η(ω)(B). By the definitions of η and the σ-field N these are random variables taking values in N0, that is

$$\{ \eta ( B ) = k \} \equiv \{ \omega \in \Omega \, \colon \eta ( \omega , B ) = k \} \in \mathcal { F } , \quad B \in \mathcal { X } , \, k \in \overline { \mathbb { N } } _ { 0 } .$$

Conversely, a mapping η: Ω → N is a point process if (2.3) holds. In this case we call η(B) the number of points of η in B. Note that the mapping (ω, B) → η(ω, B) is a kernel from Ω to X (see Section A.1) with the additional property that η(ω, ·) ∈ N for each ω ∈ Ω.

Example 2.2 Let X be a random element in X. Then

$$\eta \colon = \delta _ { X }$$

is a point process. Indeed, the required measurability property follows from

$$\{ \eta ( B ) = k \} = \begin{cases} \{ X \in B \} , & \text {if } k = 1 , \\ \{ X \notin B \} , & \text {if } k = 0 , \\ \emptyset , & \text {otherwise} . \end{cases}$$

The above one-point process can be generalised as follows.

a s ie   i aid     at X1,..., X are independent random elements in X with distribution Q. Then

$$\eta \colon = \delta _ { X _ { 1 } } + \cdots + \delta _ { X _ { m } }$$

is a point process on X. Because

$$\mathbb { P } ( \eta ( B ) = k ) = \binom { m } { k } \mathbb { Q } ( B ) ^ { k } ( 1 - \mathbb { Q } ( B ) ) ^ { m - k } , \quad k = 0 , \dots , m ,$$

η is referred to as a binomial process with sample size m and sampling distribution Q.

In this example, the random measure η can be written as a sum of Dirac measures, and we formalise the class of point processes having this property in the following definition. Here and later we say that two point processes η and η′ are almost surely equal if there is an A ∈ F with P(A) = 1 such that η(ω) = η′(ω) for each ω ∈ A.


<!-- p:23 -->


Definition 2.4 We shall refer to a point process η on X as a proper point process if there exist random elements X1, X2, ... in X and an N0-valued random variable κ such that almost surely

$$\eta = \sum _ { n = 1 } ^ { k } \delta _ { X _ { n } } .$$

In the case κ = 0 this is interpreted as the zero measure on X.

The motivation for this terminology is that the intuitive notion of a point process is that of a (random) set of points, rather than an integer-valued measure. A proper point process is one which can be interpreted as a countable (random) set of points in X (possibly with repetitions), thereby better fitting this intuition.

The class of proper point processes is very large. Indeed, we shall see later that if X is a Borel subspace of a complete separable metric space, hes s ( oe os  o oe o s ln  pnr and that, for general (X, X), if η is a Poisson point process on X there is   o ns on de  o enr o des  se concepts will be defined in due course); see Corollary 6.5 and Corollary 3.7. Exercise 2.5 shows, however, that not all point processes are proper.

### 2.2 Campbell's Formula

A first characteristic of a point process is the mean number of points lying in an arbitrary measurable set:

Definition 2.5 The intensity measure of a point process η on X is the measure λ defined by

$$\lambda ( B ) \colon = \mathbb { E } [ \eta ( B ) ] , \quad B \in \mathcal { X } .$$

It follows from basic properties of expectation that the intensity measure of a point process is indeed a measure.

Example 2.6 The intensity measure of a binomial process with sample size m and sampling distribution Q is given by

$$\lambda ( B ) = \mathbb { E } \left [ \sum _ { k = 1 } ^ { m } 1 \{ X _ { k } \in B \} \right ] = \sum _ { k = 1 } ^ { m } \mathbb { P } ( X _ { k } \in B ) = m \, \mathbb { Q } ( B ) .$$

Independence of the random variables X1, . . . , X is not required for this calculation.


<!-- p:24 -->


Let  ̄ := [−∞, ∞] and  ̄+ := [0, ∞]. Let us denote by R(X) (resp. R(X)) the set of all measurable functions u: X → R (resp. u: X → R). Let R+(X) (resp. R+(X)) be the set of all those u ∈ R(X) (resp. u ∈ R(X)) with u ≥ 0. Given u ∈ R(X), define the functions u+, u− ∈ R+(X) by u+(x) := max{u(x), 0} and u−(x) := max{−u(x), 0}, x ∈ X. Then u(x) = u+(x) − u−(x). We recall from measure theory (see Section A.1) that, for any measure v on X, the integral ∫ u dν ≡ ∫ u(x) v(dx) of u ∈ R(X) with respect to ν is defined as

$$\int u ( x ) \, \nu ( d x ) \equiv \int u \, d \nu \, \colon = \int u ^ { + } \, d \nu - \int u ^ { - } \, d \nu$$

whenever this expression is not of the form ∞ – ∞. Otherwise we use here the convention ∫ u(x) v(dx) := 0. We often write

$$\nu ( u ) \colon = \int u ( x ) \, \nu ( d x ) ,$$

so that v(B) = v(1B) for any B ∈ X. If η is a point process, then η(u) ≡ ∫ u dη denotes the mapping ω ↔ ∫ u(x) η(ω, dx).

Proposition 2.7 (Campbell's formula) Let η be a point process on (X, X) with intensity measure λ. Let u ∈ R(X). Then ∫ u(x) η(dx) is a random variable. Moreover,

$$\mathbb { E } \left [ \int u ( x ) \, \eta ( d x ) \right ] = \int u ( x ) \, \lambda ( d x )$$

whenever u ≥ 0 or ∫ |u(x)| λ(dx) &lt; ∞.

Proof If u(x) = 1B(x) for some B ∈ X then ∫ u(x) η(dx) = η(B) and both assertions are true by definition. By standard techniques of measure theory (linearity and monotone convergence) this can be extended, first to measurable simple functions and then to arbitrary u ∈ R+ (X).

Let u ∈ R(X). We have just seen that η(u+) and η(u−) are random variables, so that η(u) is a random variable too. Assume that ∫ |u(x)| λ(dx) &lt; ∞. Then the first part of the proof shows that η(u+) and η(u−) both have a finite expectation and that

$$\mathbb { E } [ \eta ( u ) ] = \mathbb { E } [ \eta ( u ^ { + } ) ] - \mathbb { E } [ \eta ( u ^ { - } ) ] = \lambda ( u ^ { + } ) - \lambda ( u ^ { - } ) = \lambda ( u ) .$$

This concludes the proof.

□


<!-- p:25 -->


### 2.3 Distribution of a Point Process

In accordance with the terminology of probability theory (see Section B.1), the distribution of a point process η on X is the probability measure Pη on (N, N), given by A → P(η ∈ A). If η′ is another point process with the same distribution, we write η = η'.

The following device is a powerful tool for analysing point processes. We use the convention e−∞ := 0.

Definition 2.8 The Laplace (or characteristic) functional of a point process η on X is the mapping Lη : R+(X) → [0, 1] defined by

$$L _ { \eta } ( u ) \colon = \mathbb { E } \left [ \exp \left ( - \int u ( x ) \, \eta ( d x ) \right ) \right ] , \quad u \in \mathbb { R } _ { + } ( \mathbb { X } ) .$$

Example 2.9 Let η be the binomial process of Example 2.3. Then, for u ∈ R+(X),

$$W \in \mathbb { E } ( \mathbb { A } ) , \\ L _ { \eta } ( u ) & = \mathbb { E } \left [ \exp \left ( - \sum _ { k = 1 } ^ { m } u ( X _ { k } ) \right ) \right ] = \mathbb { E } \left [ \prod _ { k = 1 } ^ { m } \exp [ - u ( X _ { k } ) ] \right ] \\ & = \prod _ { k = 1 } ^ { m } \mathbb { E } [ \exp [ - u ( X _ { k } ) ] ] = \left [ \int \exp [ - u ( x ) ] \, \mathbb { Q } ( d x ) \right ] ^ { m } . \\ \intertext { t h e f l o w i n g r a s i o n g r a t i c h e r s e q u a l i t y i n d i s t r i b u t i o n f o r n i t p o r n }$$

The following proposition characterises equality in distribution for point processes. It shows, in particular, that the Laplace functional of a point process determines its distribution.

Proposition 2.10 For point processes η and η′ on X the following assertions are equivalent:

- (ii) (η(B1), . . . , η(Bm)) = (η′(B1), . . , η′(B)) for all m ∈ N and all pairwise disjoint B1, . . . , Bm ∈ X;
- (iii) Lη(u) = Lη(u) for all u ∈ R+(X);
- (iv) for all u ∈ R+(X), η(u) = η' (u) as random variables in  ̄+.

Proof First we prove that (i) implies (iv). Given u ∈ R+(X), define the function gu : N → R+ by μ → ∫ u dμ. By Proposition 2.7 (or a direct check based on first principles), gu is a measurable function. Also,

$$\mathbb { P } _ { \eta ( u ) } ( \cdot ) = \mathbb { P } ( \eta ( u ) \in \cdot ) = \mathbb { P } ( \eta \in g _ { u } ^ { - 1 } ( \cdot ) ) ,$$

and likewise for η′. So if η = η′ then also η(u) ≡ η'(u).

Next we show that (iv) implies (iii). For any R+-valued random variable Y we have E[exp(-Y)] = ∫ e−y Pγ(dy), which is determined by the distribution Py. Hence, if (iv) holds,


<!-- p:26 -->


$$L _ { \eta } ( u ) = \mathbb { E } [ \exp ( - \eta ( u ) ) ] = \mathbb { E } [ \exp ( - \eta ^ { \prime } ( u ) ) ] = L _ { \eta ^ { \prime } } ( u )$$

for all u ∈ R+(X), so (iii) holds.

Assume now that (iii) holds and consider a simple function of the form u = c11B1 + · . · + cm1B, where m ∈ N, B1, . . . , Bm ∈ X and c1, . . . , Cm ∈ (0, ∞). Then

$$L _ { \eta } ( u ) = \mathbb { E } \left [ \exp \left ( - \sum _ { j = 1 } ^ { m } c _ { j } \eta ( B _ { j } ) \right ) \right ] = \hat { \widehat { P } } _ { ( \eta ( B _ { 1 } ) , \dots , \eta ( B _ { m } ) ) } ( c _ { 1 } , \dots , c _ { m } )$$

where for any measure μ on [0, ∞]" we write β for its multivariate Laplace transform. Since a finite measure on R' is determined by its Laplace transform (this follows from Proposition B.4), we can conclude that the restriction of P(γ(b1)..,B))( measure on [0, ∞]n) to (0, ∞)m is the same as the restriction of P('(1),),to (0, ∞). Then, using the fact tat P(η(B1)..)Bm) and P(η(B)..′'(B)) are probability measures on [0, ∞]m, by forming suitable complements we obtain ((1)..,) = P(η′(1)..'.)(tese details are let to the reader). In other words, (iii) implies (ii).

Finally we assume (ii) and prove (i). Let m ∈ N and B1, . . . , B ∈ X, not necessarily pairwise disjoint. Let C1, . . ., C be the atoms of the field generated by B1, ..., Bm; see Section A.1. For each i ∈ {1,..., m} there exists Ji ⊂ {1, . . . , n} such that Bi = ∪jeJiCj. (Note that Ji = ∅ if Bi = ∅.) Let D1, . . . , Dm ⊂ N0. Then

$$& \mathbb { P } ( \eta ( B _ { 1 } ) \in D _ { 1 } , \dots , \eta ( B _ { m } ) \in D _ { m } ) \\ & \quad = \int 1 \{ \sum _ { j \in J _ { 1 } } k _ { j } \in D _ { 1 } , \dots , \sum _ { j \in J _ { m } } k _ { j } \in D _ { m } \} \mathbb { P } _ { ( \eta ( C _ { 1 } ) , \dots , \eta ( C _ { n } ) ) } ( d ( k _ { 1 } , \dots , k _ { n } ) ) .$$

Therefore Pη and Pη coincide on the system H consisting of all sets of the form

$$\{ \mu \in \mathbf N \colon \mu ( B _ { 1 } ) \in D _ { 1 } , \dots , \mu ( B _ { m } ) \in D _ { m } \} ,$$

where m ∈ N, B1, . . . , Bm ∈ X and D1, . . . , Dm ⊂ N0. Clearly H is a πsystem; that is, closed under pairwise intersections. Moreover, the smallest σ-field σ(H) containing H is the full σ-field N. Hence (i) follows from the fact that a probability measure is determined by its values on a generating π-system; see Theorem A.5. □


<!-- p:27 -->


### 2.4 Point Processes on Metric Spaces

Let us now assume that X is a metric space with metric ρ; see Section A.2. Then it is always to be understood that X is the Borel σ-field B(X) of X. In particular, the singleton {x} is in X for all x ∈ X. If ν is a measure on X then we often write v{x} := v({x}). If ν{x} = 0 for all x ∈ X, then ν is said to be diffuse. Moreover, if μ ∈ N(X) then we write x ∈ μ if μ({x}) &gt; 0.

A set B ⊂ X is said to be bounded if it is empty or its diameter

$$d ( B ) \colon = \sup \{ \rho ( x , y ) \, \colon x , y \in B \}$$

is finite.

Definition 2.11 Suppose that X is a metric space. The system of bounded measurable subsets of X is denoted by Xb. A measure v on X is said to be locally finite if v(B) &lt; ∞ for every B ∈ Xb. Let N(X) denote the set of all locally finite elements of N(X) and let Nt(X) := {A ∩ Nl(X) : A ∈ N(X)}.

Fix some x0 ∈ X. Then any bounded set B is contained in the closed ball B(x0, r) = {x ∈ X : ρ(x, x0) ≤ r} for sufficiently large r &gt; 0. In fact, if B ≠ ∅, then we can take, for instance, r := d(B) + ρ(x1, x0) for some x1 ∈ B. Note that B(x0, n) ↑ X as n → ∞. Hence a measure v on X is locally finite if and only if v(B(x0, n)) &lt; ∞ for each n ∈ N. In particular, the set N1(X) is measurable, that is N(X) ∈ N(X). Moreover, any locally finite measure is σ-finite.

Proposition 2.12 Let η and η' be point processes on a metric space X. Suppose η(u) = η′(u) for all u ∈ R+(X) such that {u &gt; 0} is bounded. Then η = η'.

Proof Suppose that

$$\eta ( u ) \stackrel { d } { = } \eta ^ { \prime } ( u ) , \ \ u \in \mathbb { R } _ { + } ( \mathbb { X } ) , \ \{ u > 0 \} \text { bounded.}$$

Then Lη(u) = Lη (u) for any u ∈ R+(X) such that {u &gt; 0} is bounded. Given any v ∈ R+(X), we can choose a sequence u, n ∈ N, of functions in R+(X) such that {un &gt; 0} is bounded for each n, and un ↑ v pointwise. Then, by dominated convergence and (2.8),

$$L _ { \eta } ( v ) = \lim _ { n \to \infty } L _ { \eta } ( u _ { n } ) = \lim _ { n \to \infty } L _ { \eta ^ { \prime } } ( u _ { n } ) = L _ { \eta ^ { \prime } } ( v ) ,$$

so η = η′ by Proposition 2.10.

□

Definition 2.13 A point process η on a metric space X is said to be locally finite if P(η(B) &lt; ∞) = 1 for every bounded B ∈ X.


<!-- p:28 -->


If required, we could interpret a locally finite point process η as a random element of the space (N(X), Ni(X)), introduced in Definition2.11. Indeed, we can define another point process η by ñ(ω, ·) := η(ω, ·) if the latter is locally finite and by ñ(ω, ·) := 0 (the zero measure) otherwise. Then η is a random element of (N(X), Ni(X)) that coincides P-almost surely (P-a.s.) with η.

The reader might have noticed that the proof of Proposition 2.12 has not really used the metric on X. The proof of the next refinement of this result (not used later in the book) exploits the metric in an essential way.

Proposition 2.14 Let η and η' be locally finite point processes on a metric space X. Suppose η(u) = η′(u) for all continuous u: X → R+ such that {u &gt; 0} is bounded. Then η = η′.

Proof Let G be the space of continuous functions u: X → R+ such that {u &gt; 0} is bounded. Assume that η(u) = η'(u) for all u ∈ G. Since G is closed under non-negative linear combinations, it follows, as in the proof that (iii) implies (ii) in Proposition 2.10, that

$$( \eta ( u _ { 1 } ) , \eta ( u _ { 2 } ) , \dots ) \stackrel { d } { = } ( \eta ^ { \prime } ( u _ { 1 } ) , \eta ^ { \prime } ( u _ { 2 } ) , \dots ) ,$$

first for any finite sequence and then (by Theorem A.5 in Section A.1) for any infinite sequence u ∈ G, n ∈ N. Take a bounded closed set C ⊂ X and, for n ∈ N, define

$$u _ { n } ( x ) \colon = \max \{ 1 - n d ( x , C ) , 0 \} , \quad x \in \mathbb { X } ,$$

where d(x, C) := inf{ρ(x, y) : y ∈ C} and inf ∅ := ∞. By Exercise 2.8, un ∈ G. Moreover, un ↓ 1c as n → ∞, and since η is locally finite we obtain η(un) → η(C) P-a.s. The same relation holds for η'. It follows that statement (ii) of Proposition 2.10 holds whenever B1, . . . , B are closed and bounded, but not necessarily disjoint. Hence, fixing a closed ball C ⊂ X, Pη and Pη coincide on the π-system Hc consisting of all sets of the form

$$\{ \mu \in \mathbf N _ { l } \colon \mu ( B _ { 1 } \cap C ) \leq k _ { 1 } , \dots , \mu ( B _ { m } \cap C ) \leq k _ { m } \} ,$$

where m ∈ N, B1, . . . , B ⊂ X are closed and k1, . . . , km ∈ N0. Another application of Theorem A.5 shows that Pη and Pη coincide on σ(Hc) and then also on Ni := σ(i=1σ(HB)), where Bi := B(x0, i) and x0 ∈ X is fixed.

It remains to show that N′ = N1. Let i ∈ N and let Ni denote the smallest σ-field on N1 containing the sets {μ ∈ Nt : μ(B ∩ Bi) ≤ k} for all closed sets B ⊂ X and each k ∈ N0. Let D be the system of all Borel sets B ⊂ X such that μ → μ(B∩Bi) is Ni-measurable. Then D is a Dynkin system containing the π-system of all closed sets, so that the monotone class theorem shows D = X. Therefore σ(HBi) contains {μ ∈ Nl : μ(B ∩ Bi) ≤ k} for all B ∈ X and all k ∈ N0. Letting i → ∞ we see that N′ contains {μ ∈ Nt : μ(B) ≤ k} and therefore every set from Ni. □


<!-- p:29 -->


### 2.5 Exercises

Exercise 2.1 Give an example of a point process η on a measurable space (X, X) with intensity measure λ and u ∈ R(X) (violating the condition that u ≥ 0 or ∫ |u(x)|λ(dx) &lt; ∞), such that Campbell's formula (2.6) fails.

Exercise 2.2 Let X* ⊂ X be a π-system generating X. Let η be a point process on X that is σ-finite on X*, meaning that there is a sequence C ∈ X*, n ∈ N, such that ∪x=1Cn = X and P(η(Cn) &lt; ∞) = 1 for all n ∈ N. Let η′ be another point process on X and suppose that the equality in Proposition 2.10(ii) holds for all B1, . . . , Bm ∈ X* and m ∈ N. Show that η = η′.

Exercise 2.3 Let η1, η2, . . . be a sequence of point processes and define η := η1 + η2 + · · · , that is η(ω, B) := η1(ω, B) + η2(ω, B) + · · · for all ω ∈ Ω and B ∈ X. Show that η is a point process. (Hint: Prove first that N(X) is closed under countable summation.)

Exercise 2.4 Let η1, η2, . . . be a sequence of proper point processes. Show that η := η1 + η2 + · · ·. is a proper point process.

Exercise 2.5 Suppose that X = [0, 1]. Find a σ-field X and a measure μ on (X, X) such that μ(X) = 1 and μ(B) ∈ {0, 1} for all B ∈ X, which is not of the form μ = δx for some x ∈ X. (Hint: Take the system of all finite subsets of X as a generator of X.)

Exercise 2.6 Let η be a point process on X with intensity measure λ and let B ∈ X such that λ(B) &lt; ∞. Show that

$$\lambda ( B ) = - \frac { d } { d t } L _ { \eta } ( t \mathbf 1 _ { B } ) \Big | _ { t = 0 } .$$

Exercise 2.7 Let η be a point process on X. Show for each B ∈ X that

$$\mathbb { P } ( \eta ( B ) = 0 ) = \lim _ { t \to \infty } L _ { \eta } ( t \mathbf 1 _ { B } ) .$$

Exercise 2.8 Let (X, ρ) be a metric space. Let C ⊂ X, C ≠ 0. For x ∈ X let d(x, C) := inf{ρ(x, z) : z ∈ C}. Show that d(·, C) has the Lipschitz property

$$| d ( x , C ) - d ( y , C ) | \leq \rho ( x , y ) , \ \ x , y \in \mathbb { X } .$$

(Hint: Take z ∈ C and bound ρ(x, z) by the triangle inequality.)


<!-- p:30 -->


## Poisson Processes

For a Poisson point process the number of points in a given set has a Poisson distribution. Moreover, the numbers of points in disjoint sets are stochastically independent. A Poisson process exists on a general s-finite measure space. Its distribution is characterised by a specific exponential form of the Laplace functional.

### 3.1 Definition of the Poisson Process

In this chapter we fix an arbitrary measurable space (X, X). We are now ready for the definition of the main subject of this volume. Recall that for γ ∈ [0, ∞], the Poisson distribution Po(γ) was defined at (1.4).

Definition 3.1 Let λ be an s-finite measure on X. A Poisson process with intensity measure λ is a point process η on X with the following two properties:

- (i) For every B ∈ X the distribution of η(B) is Poisson with parameter λ(B), that is to say P(η(B) = k) = Po(λ(B); k) for all k ∈ N0.
- (ii) For every m ∈ N and all pairwise disjoint sets B1, .. . , B ∈ X the random variables η(B1), . . . , η(Bm) are independent.

Property (i) of Definition 3.1 is responsible for the name of the Poisson process. A point process with property (ii) is said to be completely independent. (One also says that η has independent increments or is completely random.) For a (locally finite) point process without multiplicities and a diffuse intensity measure (on a complete separable metric space) we shall see in Chapter 6 that the two defining properties of a Poisson process are equivalent.

If η is a Poisson process with intensity measure λ then E[η(B)] = λ(B), so that Definition 3.1 is consistent with Definition2.5. In particular, if λ = 0 is the zero measure, then P(η(X) = 0) = 1.


<!-- p:31 -->


Let us first record that for each s-finite λ there is at most one Poisson process with intensity measure λ, up to equality in distribution.

Proposition 3.2 Let η and η' be two Poisson processes on X with the same s-finite intensity measure. Then η = η'.

Proof The result follows from Proposition 2.10.

□

### 3.2 Existence of Poisson Processes

In this section we show by means of an explicit construction that Poisson processes exist. Before we can do this, we need to deal with the superposition of independent Poisson processes.

Theorem 3.3 (Superposition theorem) Let ηi, i ∈ N, be a sequence of independent Poisson processes on X with intensity measures λ. Then

$$\eta \colon = \sum _ { i = 1 } ^ { \infty } \eta _ { i }$$

is a Poisson process with intensity measure λ := λ1 + λ2 + . . .

Proof Exercise 2.3 shows that η is a point process.

For n ∈ N and B ∈ X, we have by Exercise 1.4 that ξn(B) := ∑i=1 ηi(B) has a Poisson distribution with parameter Σ=1 λ(B). Also ξ(B) converges monotonically to η(B) so by continuity of probability, and the fact that Po(γ; j) is continuous in γ for j ∈ N0, for all k ∈ N0 we have

$$\mathbb { P } ( \eta ( B ) \leq k ) & = \lim _ { n \to \infty } \mathbb { P } ( \xi _ { n } ( B ) \leq k ) \\ & = \lim _ { n \to \infty } \sum _ { j = 0 } ^ { k } \text {Po} \left ( \sum _ { i = 1 } ^ { n } \lambda _ { i } ( B ) ; j \right ) = \sum _ { j = 0 } ^ { k } \text {Po} \left ( \sum _ { i = 1 } ^ { \infty } \lambda _ { i } ( B ) ; j \right ) \\$$

so that η(B) has the Po(λ(B)) distribution.

Let B1, . . . , Bm ∈ X be pairwise disjoint. Then (η(Bj), 1 ≤ j ≤ m, i ∈ N) is a family of independent random variables, so that by the grouping property of independence the random variables Σ η(B1), . . . , Σ η(Bm) are independent. Thus η is completely independent. □

Now we construct a Poisson process on (X, X) with arbitrary s-finite intensity measure. We start by generalising Example 2.3.

Definition 3.4 Let V and Q be probability measures on N0 and X, respectively. Suppose that X1, X2, ... are independent random elements in X


<!-- p:32 -->


with distribution Q, and let κ be a random variable with distribution V, independent of (X). Then

$$\eta \colon = \sum _ { k = 1 } ^ { \kappa } \delta _ { X _ { k } }$$

is called a mixed binomial process with mixing distribution V and sampling distribution Q.

The following result provides the key for the construction of Poisson processes.

Proposition 3.5 Let Q be a probability measure on X and let γ ≥ 0. Suppose that η is a mixed binomial process with mixing distribution Po(γ) and sampling distribution Q. Then η is a Poisson process with intensity measure γ Q.

Proof Let κ and (X) be given as in Definition 3.4. To prove property (ii) of Definition 3.1 it is no loss of generality to assume that B1, . . . , B are pairwise disjoint measurable subsets of X satisfying Ui1 Bi = X. (Otherwise we can add the complement of this union.) Let k1, . . . , k ∈ N0 and set k := k1 + · · · + km. Then

$$\mathbb { P } ( \eta ( B _ { 1 } ) = k _ { 1 } , \dots , \eta ( B _ { m } ) = k _ { m } ) \\ = \mathbb { P } ( \kappa = k ) \mathbb { P } \left ( \sum _ { j = 1 } ^ { k } 1 \{ X _ { j } \in B _ { 1 } \} = k _ { 1 } , \dots , \sum _ { j = 1 } ^ { k } 1 \{ X _ { j } \in B _ { m } \} = k _ { m } \right ) . \\$$

Since the second probability on the right is multinomial, this gives

$$S u n c t e r s u n c t i o n a b i t y o n t i r e & \text { in the light of } \text { in } \text { multinom} , \text { thus gives} \\ \mathbb { P } ( \eta ( B _ { 1 } ) = k _ { 1 } , \dots , \eta ( B _ { m } ) = k _ { m } ) & = \frac { \gamma ^ { k } } { k ! } e ^ { - \gamma } \frac { k ! } { k _ { 1 } ! \cdots k _ { m } ! } \mathbb { Q } ( B _ { 1 } ) ^ { k _ { 1 } } \cdots \mathbb { Q } ( B _ { m } ) ^ { k _ { m } } \\ & = \prod _ { j = 1 } ^ { m } \frac { ( \gamma \mathbb { Q } ( B _ { j } ) ) ^ { k _ { j } } } { k _ { j } ! } e ^ { - \gamma \mathbb { Q } ( B _ { j } ) } . \\ \text {Summing over } k _ { 1 } & \quad k _ { 1 } \text { shows that } \eta ( B _ { 1 } ) \text { is Poisson distributed with } \rho _ { 1 } ,$$

Summing over k2, . . . , km shows that η(B1) is Poisson distributed with parameter γ Q(B1). A similar statement applies to η(B2), . . . , η(B). Therefore η(B1), . . . , η(Bm) are independent. □

Theorem 3.6 (Existence theorem) Let λ be an s-finite measure on X. Then there exists a Poisson process on X with intensity measure λ.

Proof The result is trivial if λ(X) = 0.

Suppose for now that 0 &lt; λ(X) &lt; ∞. On a suitable probability space, assume that κ, X1, X2, . .. are independent random elements, with κ taking values in N0 and each X taking values in X, with κ having the Po(λ(X)) distribution and each X having λ(·)/λ(X) as its distribution. Here the probability space can be taken to be a suitable product space; see the proof of Corollary 3.7 below. Let η be the mixed binomial process given by (3.2). Then, by Proposition 3.5, η is a Poisson process with intensity measure λ, as required.


<!-- p:33 -->


Now suppose that λ(X) = ∞. There is a sequence λi, i ∈ N, of measures on (X, X) with strictly positive and finite total measure, such that λ = Σi=1 λ. On a suitable (product) probability space, let ηi, i ∈ N, be a sequence of independent Poisson processes with η having intensity measure λ. This is possible by the preceding part of the proof. Set η = Σ=1 ηi. By the superposition theorem (Theorem 3.3), η is a Poisson process with intensity measure λ, and the proof is complete. □

A corollary of the preceding proof is that on arbitrary (X, X) every Pois-eq s   un (n eo  deid ss eut o on tion.

Corollary 3.7 Let λ be an s-finite measure on X. Then there is a probability space (Ω, F, P) supporting random elements X1, X2, . . . in X and κ in N0, such that

$$\eta \coloneqq \sum _ { n = 1 } ^ { \kappa } \delta _ { X _ { n } }$$

is a Poisson process with intensity measure λ.

Proof We consider only the case λ(X) = ∞ (the other case is covered by Proposition 3.5). Take the measures λ, i ∈ N, as in the last part of the proof of Theorem 3.6. Let γi := λ(X) and Qi := γ−1 λ. We shall take (Ω, F, P) to be the product of spaces (Ωi, Fi, Pi), i ∈ N, where each (Ωi, Fi, Pi) is again an infinite product of probability spaces (Ωj, Fij, Pij), j ∈ N0, with Ωi0 := N0, Pi0 := Po(γi) and (Ωij, Fij, Pij) := (X, X, Qi) for j ≥ 1. On this space we can define independent random elements κ, i ∈ N, and Xj, i, j ∈ N, such that κ has distribution Po(γ) and Xi j has distribution Q; see Theorem B.2. The proof of Theorem 3.6 shows how to define κ, X1, X2, . . . in terms of these random variables in a measurable (algorithmic) way. The details are left to the reader. □

As a consequence of Corollary 3.7, when checking a statement involving only the distribution of a Poisson process η, it is no restriction of generality to assume that η is proper. Exercise 3.9 shows that there are Poisson processes which are not proper. On the other hand, Corollary 6.5 will show that any suitably regular point process on a Borel subset of a complete separable metric space is proper.


<!-- p:34 -->


The next result is a converse to Proposition 3.5.

Proposition 3.8 Let η be a Poisson process on X with intensity measure λ satisfying 0 &lt; λ(X) &lt; ∞. Then η has the distribution of a mixed binomial process with mixing distribution Po(λ(X)) and sampling distribution Q := λ(X)−1 λ. The conditional distribution P(η ∈ · | η(X) = m), m ∈ N, is that of a binomial process with sample size m and sampling distribution Q.

Proof Let η' be a mixed binomial process that has mixing distribution Po(λ(X)) and sampling distribution Q. Then η′ ≡ η by Propositions 3.5 and 3.2. This is our first assertion. Also, by definition, P(η′ ∈ · | η'(X) = m) has the distribution of a binomial process with sample size m and sampling distribution Q, and by the first assertion so does P(η ∈ · | η(X) = m), yielding the second assertion. □

### 3.3 Laplace Functional of the Poisson Process

The following characterisation of Poisson processes is of great value for both theory and applications.

Theorem 3.9 Let λ be an s-finite measure on X and let η be a point process on X. Then η is a Poisson process with intensity measure λ if and only if

$$L _ { \eta } ( u ) = \exp \left [ - \int ( 1 - e ^ { - u ( x ) } ) \, \lambda ( d x ) \right ] , \quad u \in \mathbb { R } _ { + } ( \mathbb { X } ) .$$

Proof Assume first that η is a Poisson process with intensity measure λ. Consider first the simple function u := c11B, + · .· + cm1B, where m ∈ N, c1, . . . , cm ∈ (0, ∞) and B1, . . , Bm ∈ X are pairwise disjoint. Then

$$\mathbb { E } [ \exp [ - \eta ( u ) ] ] = \mathbb { E } \left [ \exp \left ( - \sum _ { i = 1 } ^ { m } c _ { i } \eta ( B _ { i } ) \right ) \right ] = \mathbb { E } \left [ \prod _ { i = 1 } ^ { m } \exp [ - c _ { i } \eta ( B _ { i } ) ] \right ] .$$

The complete independence and the formula (1.9) for the Laplace transform of the Poisson distribution (this also holds for Po(∞)) yield

$$\text {from or the Fosson distribution (this also holds for F 0(C)) yield} \\ L _ { \eta } ( u ) & = \prod _ { i = 1 } ^ { m } \mathbb { E } \left [ \exp [ - c _ { i } \eta ( B _ { i } ) ] \right ] = \prod _ { i = 1 } ^ { m } \exp [ - \lambda ( B _ { i } ) ( 1 - e ^ { - c _ { i } } ) ] \\ & = \exp \left [ - \sum _ { i = 1 } ^ { m } \lambda ( B _ { i } ) ( 1 - e ^ { - c _ { i } } ) \right ] = \exp \left [ - \sum _ { i = 1 } ^ { m } \int _ { B _ { i } } ( 1 - e ^ { - u } ) \, d \lambda \right ] .$$


<!-- p:35 -->


Since 1 − e−u(x) = 0 for x ∉ B1 ∪ · · · ∪ B, this is the right-hand side of (3.4). For general u ∈ R+(X), choose simple functions un with un ↑ u as n → ∞. Then, by monotone convergence (Theorem A.6), η(un) ↑ η(u) as n → ∞, and by dominated convergence for expectations the left-hand side of

$$\mathbb { E } [ \exp [ - \eta ( u _ { n } ) ] ] = \exp \left [ - \int ( 1 - e ^ { - u _ { n } ( x ) } ) \, \lambda ( d x ) \right ]$$

anonne  t te  ge o o  ( t ral with respect to λ), the right-hand side tends to the right-hand side of (3.4).

Assume now that (3.4) holds. Let η' be a Poisson process with intensity measure λ. (By Theorem 3.6, such an η′ exists.) By the preceding argument, Lη(u) = Lη(u) for all u ∈ R+(X). Therefore, by Proposition 2.10, η = η'; that is, η is a Poisson process with intensity measure λ. □

### 3.4 Exercises

Exercise 3.1 Use Exercise 1.12 to deduce that there exist a measure space (X, X, λ) and a point process on X satisfying part (i) but not part (ii) of the definition of a Poisson process (Definition 3.1).

Exercise 3.2 Show that there exist a measure space (X, X, λ) and a point ro  (  n  o  (  s  o t sioa definition with independent' replaced by pairwise independent', such that η is not a Poisson point process. In other words, show that we can have η(B) Poisson distributed for all B ∈ X, and η(A) independent of η(B) for all disjoint pairs A, B ∈ X, but η(A1), . . . , η(Ak) not mutually independent for all disjoint A1, . . . , Ak ∈ X.

Exercise 3.3 Let η be a Poisson process on X with intensity measure λ and let B ∈ X with 0 &lt; λ(B) &lt; ∞. Suppose B1, . . . , B are sets in X forming a partition of B. Show for all k1, . . . , kn ∈ N0 and m := Σ ki that

$$\mathbb { P } ( \cap _ { i = 1 } ^ { n } \{ \eta ( B _ { i } ) = k _ { i } \} \, | \, \eta ( B ) = m ) = \left ( \frac { m ! } { k _ { 1 } ! k _ { 2 } ! \cdots k _ { n } ! } \right ) \prod _ { i = 1 } ^ { n } \left ( \frac { \lambda ( B _ { i } ) } { \lambda ( B ) } \right ) ^ { k _ { i } } .$$

Exercise 3.4 Let η be a Poisson process on X with s-finite intensity measure λ and let u ∈ R+(X). Use the proof of Theorem 3.9 to show that

$$\mathbb { E } \left [ \exp \left ( \int u ( x ) \, \eta ( d x ) \right ) \right ] = \exp \left [ \int ( e ^ { u ( x ) } - 1 ) \, \lambda ( d x ) \right ] .$$


<!-- p:36 -->


Exercise 3.5 Let V be a probability measure on N0 with generating function Gy(s) := ∑n=0 V({n})sn, s ∈ [0, 1]. Let η be a mixed binomial process with mixing distribution V and sampling distribution Q. Show that

$$L _ { \eta } ( u ) = G _ { \mathbb { V } } ( \int e ^ { - u } \, d \mathbb { Q } ) , \quad u \in \mathbb { R } _ { + } ( \mathbb { X } ) .$$

Assume now that V is a Poisson distribution; show that the preceding formula is consistent with Theorem 3.9.

Exercise 3.6 Let η be a point process on X. Using the convention e−∞ := 0, the Laplace functional L(u) can be defined for any u ∈ R+(X). Assume now that η is a Poisson process with intensity measure λ. Use Theorem 3.9 to show that

$$\mathbb { E } \left [ \prod _ { n = 1 } ^ { \kappa } u ( X _ { n } ) \right ] = \exp \left [ - \int ( 1 - u ( x ) ) \, \lambda ( d x ) \right ] , \\$$

for any measurable u: X → [0, 1], where η is assumed to be given by (3.3).

The left-hand side of (3.5) is called the probability generating functional o s  (o o es se   os p  os   to expectation of exp [ f ln u(x) η(dx)].

Exercise 3.7 Let η be a Poisson process with finite intensity measure λ. Show for all f ∈ R+(N) that

$$\mathbb { E } [ f ( \eta ) ] & = e ^ { - \lambda ( \mathbb { Z } ) } f ( 0 ) + e ^ { - \lambda ( \mathbb { Z } ) } \sum _ { n = 1 } ^ { \infty } \frac { 1 } { n ! } \int f ( \delta _ { x _ { 1 } } + \cdots + \delta _ { x _ { n } } ) \, \lambda ^ { n } ( d ( x _ { 1 } , \dots , x _ { n } ) ) . \\$$

Exercise 3.8 Let η be a Poisson process with s-finite intensity measure λ and let f ∈ R+(N) be such that E[f(η)] &lt; ∞. Suppose that η′ is a Poisson process with intensity measure λ' such that λ = λ' + v for some finite measure v. Show that E[f(η')] &lt; ∞. (Hint: Use the superposition theorem.)

Exercise 3.9 In the setting of Exercise 2.5, show that there is a probability measure λ on (X, X) and a Poisson process η with intensity measure λ such that η is not proper. (Hint: Use Exercise 2.5.)

Exercise 3.10 Let 0 &lt; γ &lt; γ'. Give an example of two Poisson processes η, η′ on (0, 1) with intensity measures γλ1 and γ'λ1, respectively (λ1 denoting Lebesgue measure), such that η ≤ η′ but η′ – η is not a Poisson process. (Hint: Use Exercise 1.9.)

Exercise 3.11 Let η be a Poisson process with intensity measure λ and let B1, B2 ∈ X satisfy λ(B1) &lt; ∞ and λ(B2) &lt; ∞. Show that the covariance between η(B1) and η(B2) is given by Cov[η(B1), η(B2)] = λ(B1 ∩ B2).


<!-- p:37 -->


4

## The Mecke Equation and Factorial Measures

The Mecke equation provides a way to compute the expectation of integrals, i.e. sums, with respect to a Poisson process, where the integrand can depend on both the point process and the point in the state space. This functional equation characterises a Poisson process. The Mecke identity can be extended to integration with respect to factorial measures, i.e. to multiple sums. Factorial measures can also be used to define the Janossy measures, thus providing a local description of a general point process. The factorial moment measures of a point process are defined as the expected factorial measures. They describe the probability of the occurrence of points in a finite number of infinitesimally small sets.

### 4.1 The Mecke Equation

In this chapter we take (X, X) to be an arbitrary measurable space and use the abbreviation (N, N) := (N(X), N(X)). Let η be a Poisson process on X with s-finite intensity measure λ and let f ∈ R+(X × N). The complete independence of η implies for each x ∈ X that, heuristically speaking, η(dx) and the restriction η{x}e of η to X \ {x} are independent. Therefore

$$\mathbb { E } [ \int f ( x , \eta _ { ( x ) ^ { c } } ) \, \eta ( d x ) ] = \int \mathbb { E } [ f ( x , \eta _ { \{ x \} ^ { c } } ) ] \, \lambda ( d x ) , \\$$

where we ignore measurability issues. If P(η({x}) = 0) = 1 for each x ∈ X (which is the case if λ is a diffuse measure on a Borel space), then the righthand side of (4.1) equals ∫ E[f(x, η)] λ(dx). (Exercise 6.11 shows a way to extend this to an arbitrary intensity measure.) We show that a proper version of the resulting integral identity holds in general and characterises the Poisson process. This equation is a fundamental tool for analysing the Poisson process and can be used in many specific calculations. In the special case where X has just a single element, Theorem 4.1 essentially reduces to an earlier result about the Poisson distribution, namely Proposition 1.1.


<!-- p:38 -->


Theorem 4.1 (Mecke equation) Let λ be an s-finite measure on X and η a point process on X. Then η is a Poisson process with intensity measure λ if and only if

$$\mathbb { E } \left [ \int f ( x , \eta ) \, \eta ( d x ) \right ] = \int \mathbb { E } [ f ( x , \eta + \delta _ { x } ) ] \, \lambda ( d x )$$

for all f ∈ R+(X × N).

Proof Let us start by noting that the mapping (x, μ) → μ + δx (adding a point x to the counting measure μ) from X ×N to N is measurable. Indeed, the mapping (x, μ) → μ(B) + 1B(x) is measurable for all B ∈ X.

If η is a Poisson process, then (4.2) is a special case of (4.11) to be proved in Section 4.2.

Assume now that (4.2) holds for all measurable f ≥ 0. Let B1, . . . , Bm be disjoint sets in X with λ(Bi) &lt; ∞ for each i. For k1, . . . , km ∈ N0 with k1 ≥ 1 we define

$$f ( x , \mu ) = \mathbf 1 _ { B _ { 1 } } ( x ) \prod _ { i = 1 } ^ { m } \mathbf 1 \{ \mu ( B _ { i } ) = k _ { i } \} , \quad ( x , \mu ) \in \mathbb { X } \times N .$$

Then

$$\mathbb { E } \left [ \int f ( x , n ) \, \eta ( d x ) \right ] = \mathbb { E } \left [ \eta ( B _ { 1 } ) \prod _ { i = 1 } ^ { m } \mathbf 1 _ { \{ \eta ( B _ { i } ) = k _ { i } \} } \right ] = k _ { 1 } \mathbb { P } \left ( \cap _ { i = 1 } ^ { m } \{ \eta ( B _ { i } ) = k _ { i } \} \right ) ,$$

with the (measure theory) convention ∞ · 0 := 0. On the other hand, we have for each x ∈ X that

$$\mathbb { E } [ f ( x , \eta + \delta _ { x } ) ] = \mathbf 1 _ { B _ { 1 } } ( x ) \, \mathbb { P } ( \eta ( B _ { 1 } ) = k _ { 1 } - 1 , \eta ( B _ { 2 } ) = k _ { 2 } , \dots , \eta ( B _ { m } ) = k _ { m } )$$

(with ∞ − 1 := ∞) so that, by (4.2),

$$k _ { 1 } \, \mathbb { P } ( \cap _ { i = 1 } ^ { m } \{ \eta ( B _ { i } ) = k _ { i } \} ) = \lambda ( B _ { 1 } ) \, \mathbb { P } ( \{ \eta ( B _ { 1 } ) = k _ { 1 } - 1 \} \cap \cap _ { i = 2 } ^ { m } \{ \eta ( B _ { i } ) = k _ { i } \} ) .$$

Assume that P( ∩i=2 {η(Bi) = ki}) &gt; 0 and note that otherwise η(B1) and the event ∩i=2{η(Bi) = ki} are independent. Putting

$$\pi _ { k } = \mathbb { P } ( \eta ( B _ { 1 } ) = k \, | \, \cap _ { i = 2 } ^ { m } \{ \eta ( B _ { i } ) = k _ { i } \} ) , \ \ k \in \overline { \mathbb { N } } _ { 0 } ,$$

we have

$$k \pi _ { k } = \lambda ( B _ { 1 } ) \pi _ { k - 1 } , \ \ k \in \overline { \mathbb { N } } .$$

Since λ(B1) &lt; ∞ this implies π∞ = 0. The only distribution satisfying this recursion is given by πk = Po(λ(B1); k), regardless of k2, . . . , km; hence η(B1) is Po(λ(B1)) distributed, and independent of ∩i=2{η(Bi) = ki}. Hence, by an induction on m, the variables η(B1), . . . , η(Bm) are independent.


<!-- p:39 -->


For general B ∈ X we still get for all k ∈ N that

$$k \mathbb { P } ( \eta ( B ) = k ) = \lambda ( B ) \, \mathbb { P } ( \eta ( B ) = k - 1 ) .$$

If λ(B) = ∞ we obtain P(η(B) = k − 1) = 0 and hence P(η(B) = ∞) = 1.

It follows that η has the defining properties of the Poisson process.

### 4.2 Factorial Measures and the Multivariate Mecke Equation

Equation (4.2) admits a useful generalisation involving multiple integration. To formulate this version we consider, for m ∈ N, the m-th power (Xm, Xm) of (X, X); see Section A.1. Suppose μ ∈ N is given by

$$\mu = \sum _ { i = 1 } ^ { k } \delta _ { x _ { j } }$$

for some k ∈ N0 and some x1, x2, . . . ∈ X (not necessarily distinct) as in (2.1). Then we define another measure μ(m) ∈ N(Xm) by

$$\mu ^ { ( m ) } ( C ) = \sum _ { i _ { 1 } , \dots , i _ { m } \leq k } ^ { \# } 1 \{ ( x _ { i _ { 1 } } , \dots , x _ { i _ { m } } ) \in C \} , \quad C \in \mathcal { X } ^ { m } ,$$

where the superscript ≠ indicates summation over m-tuples with pairwise different entries and where an empty sum is defined as zero. (In the case k = ∞ this involves only integer-valued indices.) In other words this means that

$$\mu ^ { ( m ) } = \sum _ { i _ { 1 } , \dots , i _ { m } \leq k } ^ { \neq } \delta _ { ( x _ { i _ { 1 } } , \dots , x _ { i _ { m } } ) } .$$

To aid understanding, it is helpful to consider in (4.4) a set C of the special product form B1 × ·· × Bm. If these sets are pairwise disjoint, then the right-hand side of (4.4) factorises, yielding

$$\mu ^ { ( m ) } ( B _ { 1 } \times \cdots \times B _ { m } ) = \prod _ { j = 1 } ^ { m } \mu ( B _ { j } ) .$$

If, on the other hand, Bj = B for all j ∈ {1, . . . , m} then, clearly,

$$\mu ^ { ( m ) } ( B ^ { m } ) = \mu ( B ) ( \mu ( B ) - 1 ) \cdots ( \mu ( B ) - m + 1 ) = ( \mu ( B ) ) _ { m } .$$

Therefore μ(m) is called the m-th factorial measure of μ. For m = 2 and arbitrary B1, B2 ∈ X we obtain from (4.4) that

$$\mu ^ { ( 2 ) } ( B _ { 1 } \times B _ { 2 } ) = \mu ( B _ { 1 } ) \mu ( B _ { 2 } ) - \mu ( B _ { 1 } \cap B _ { 2 } ) ,$$


<!-- p:40 -->


provided that μ(B1 ∩ B2) &lt; ∞. Otherwise μ(2)(B1 × B2) = ∞. Factorial measures satisfy the following useful recursion:

Lemma 4.2 Let μ ∈ N be given by (4.3) and define μ(1) := μ. Then, for all m ∈ N,

$$d u & \in \mathbb { N } , \\ \mu ^ { ( m + 1 ) } & = \int \left [ \int \mathbf 1 \{ ( x _ { 1 } , \dots , x _ { m + 1 } ) \in \cdot \} \mu ( d x _ { m + 1 } ) \\ & - \sum _ { j = 1 } ^ { m } \mathbf 1 \{ ( x _ { 1 } , \dots , x _ { m } , x _ { j } ) \in \cdot \} \right ] \mu ^ { ( m ) } ( d ( x _ { 1 } , \dots , x _ { m } ) ) .$$

Proof Let m ∈ N and C ∈ Xm+1. Then

$$\mu ^ { ( m + 1 ) } ( C ) = \sum _ { i _ { 1 } , \dots , i _ { m } \leq k } ^ { \neq } \sum _ { j \in \{ i _ { 1 } , \dots , i _ { m } \} } ^ { k } 1 \{ ( x _ { i _ { 1 } } , \dots , x _ { i _ { m } } , x _ { j } ) \in C \} .$$

Here the inner sum equals

$$\sum _ { j = 1 } ^ { k } \mathbf 1 \{ ( x _ { i _ { 1 } } , \dots , x _ { i _ { m } } , x _ { j } ) \in C \} - \sum _ { l = 1 } ^ { m } \mathbf 1 \{ ( x _ { i _ { 1 } } , \dots , x _ { i _ { m } } , x _ { i _ { l } } ) \in C \} ,$$

where the latter difference is either a non-negative integer (if the first sum is finite) or ∞ (if the first sum is infinite). This proves the result. □

For a general space (X, X) there is no guarantee that a measure μ ∈ N can be represented as in (4.3); see Exercise 2.5. Equation (4.9) suggests a recursive definition of the factorial measures of a general μ ∈ N, without using a representation as a sum of Dirac measures. The next proposition confirms this idea.

Proposition 4.3 For any μ ∈ N there is a unique sequence μ(m) ∈ N(Xm), m ∈ N, satisfying μ(1) := μ and the recursion (4.9). The mappings μ → μ(m) are measurable.

The proof of Proposition 4.3 is given in Section A.1 (see Proposition A.18) and can be skipped without too much loss. It is enough to remember that μ(m) can be defined by (4.4), whenever μ is given by (4.3). This follows from Lemma 4.2 and the fact that the solution of (4.9) must be unique. It follows by induction that (4.6) and (4.7) remain valid for general μ ∈ N; see Exercise 4.4.

Let η be a point process on X and let m ∈ N. Proposition 4.3 shows that


<!-- p:41 -->


η(m) is a point process on Xm. If η is proper and given as at (2.4), then

$$\eta ^ { ( m ) } = \sum _ { i _ { 1 } , \dots , i _ { m } \in \{ 1 , \dots , K \} } ^ { \neq } \delta _ { ( X _ { i _ { 1 } } , \dots , X _ { i _ { m } } ) } .$$

We continue with the multivariate version of the Mecke equation (4.2).

Theorem 4.4 (Multivariate Mecke equation) Let η be a Poisson process on X with s-inite intensity measure λ. Then, for every m ∈ N and for every f ∈ R+(Xm × N),

$$\mathbb { E } & \left [ \int f ( x _ { 1 } , \dots , x _ { m } , \eta ) \, \eta ^ { ( m ) } ( d ( x _ { 1 } , \dots , x _ { m } ) ) \right ] \\ & = \int \mathbb { E } [ f ( x _ { 1 } , \dots , x _ { m } , \eta + \delta _ { x _ { 1 } } + \cdots + \delta _ { x _ { m } } ) ] \, \lambda ^ { m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) .$$

Proof By Proposition 4.3, the map μ → μ(m) is measurable, so that (4.11) involves only the distribution of η. By Corollary 3.7 we can hence assume that η is proper and given by (2.4). Let us first assume that λ(X) &lt; ∞. Then λ = γ Q for some γ ≥ 0 and some probability measure Q on X. By Proposition 3.5, we can then assume that η is a mixed binomial process as in Definition 3.4, with κ having the Po(γ) distribution. Let f ∈ R+(Xm ×N). Then we obtain from (4.10) and (2.2) that the left-hand side of (4.11) equals

$$e ^ { - \gamma } \sum _ { k = m } ^ { \infty } \frac { \gamma ^ { k } } { k ! } \mathbb { E } [ \sum _ { i _ { 1 } , \dots , i _ { m } \in \{ 1 , \dots , k \} } ^ { \neq } f ( X _ { i _ { 1 } } , \dots , X _ { i _ { m } } , \delta _ { X _ { 1 } } + \cdots + \delta _ { X _ { k } } ) ] \\ = e ^ { - \gamma } \sum _ { k = m } ^ { \infty } \frac { \gamma ^ { k } } { k ! } \sum _ { i _ { 1 } , \dots , i _ { m } \in \{ 1 , \dots , k \} } ^ { \neq } \mathbb { E } [ f ( X _ { i _ { 1 } } , \dots , X _ { i _ { m } } , \delta _ { X _ { 1 } } + \cdots + \delta _ { X _ { k } } ) ] , \quad 0 \\ \intertext { w h o w o w h o w e d f o r i n d o n d o n d o n o f w e n d ( Y ) o n d t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f o r i n t h e f$$

where we have used first independence of κ and (X) and then the fact that we can perform integration and summation in any order we want (since f ≥ 0). Let us denote by y = (y1, . . . , ym) a generic element of Xm. Since the X are independent with distribution Q, the expression (4.12) equals

$$t h e x _ { i } \, & \text {are independent with distribution $\mathbb{Q}$, the expression (4.12) equals} \\ e ^ { - \gamma } \sum _ { k = m } ^ { \infty } \frac { \gamma ^ { k } ( k ) _ { m } } { k ! } \mathbb { E } \left [ \int f ( y , \sum _ { i = 1 } ^ { k - m } \delta _ { X _ { i } } + \sum _ { j = 1 } ^ { m } \delta _ { y _ { j } } ) \mathbb { Q } ^ { m } ( d y ) \right ] \\ & = e ^ { - \gamma } \gamma ^ { m } \sum _ { k = m } ^ { \infty } \frac { \gamma ^ { k - m } } { ( k - m ) ! } \int \mathbb { E } \left [ f ( y , \sum _ { i = 1 } ^ { k - m } \delta _ { X _ { i } } + \sum _ { j = 1 } ^ { m } \delta _ { y _ { j } } ) \right ] \mathbb { Q } ^ { m } ( d y ) \\ & = \int \mathbb { E } [ f ( y _ { 1 } , \dots , y _ { m } , \eta + \delta _ { y _ { 1 } } + \cdots + \delta _ { y _ { m } } ) ] \, \lambda ^ { m } ( d ( y _ { 1 } , \dots , y _ { m } ) ) ,$$


<!-- p:42 -->


where we have again used the mixed binomial representation. This proves (4.11) for finite λ.

Now suppose λ(X) = ∞. As in the proof of Theorem 3.6 we can then assume that η = Σ ηi, where ηi are independent proper Poisson processes with intensity measures λ each having finite total measure. By the grouping property of independence, the point processes

$$\xi _ { i } \colon = \sum _ { j \leq i } \eta _ { j } , \ \chi _ { i } \colon = \sum _ { j \geq i + 1 } \eta _ { j }$$

are independent for each i ∈ N. By (4.10) we have ξ(m) ↑ η(m) as i → ∞. Hence we can apply monotone convergence (Theorem A.12) to see that the left-hand side of (4.11) is given by

$$\text {Iter-and slide of } ( 4 . 1 1 ) \text { is given by } \\ \lim _ { i \to \infty } \mathbb { E } \left [ \int _ { \ } f ( x _ { 1 } , \dots , x _ { m } , \xi _ { i } + \chi _ { i } ) \, \xi _ { i } ^ { ( m ) } ( d ( x _ { 1 } , \dots , x _ { m } ) ) \right ] \\ = \lim _ { i \to \infty } \mathbb { E } \left [ \int _ { \ } f _ { i } ( x _ { 1 } , \dots , x _ { m } , \xi _ { i } ) \, \xi _ { i } ^ { ( m ) } ( d ( x _ { 1 } , \dots , x _ { m } ) ) \right ] , \\ \\ \text {where } f ( x _ { i } , \quad x _ { i } \, \cup \, \omega ) \colon = \mathbb { E } \left [ f ( x _ { i } , \quad x _ { i } \, \cup + x _ { i } ) \right ] ( x _ { i } , \quad x _ { i } \, \cup \, \omega ) \in \mathbb { X } ^ { m } \times N$$

where fi(x1, . . , χm, μ) := E[f(x1, . . . , χm, μ +χi)], (x1, . . . , χm, μ) ∈ Xm ×N. Setting λ′ := Σj=1 λj, we can now apply the previous result to obtain from Fubini's theorem (Theorem A.13) that the expression (4.13) equals

$$\lim _ { i \to \infty } & \int \mathbb { E } [ f _ { i } ( x _ { 1 } , \dots , x _ { m } , \xi _ { i } + \delta _ { x _ { 1 } } + \cdots + \delta _ { x _ { m } } ) ] \left ( \lambda _ { i } ^ { \prime } \right ) ^ { m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) \\ & = \lim _ { i \to \infty } \int \mathbb { E } [ f ( x _ { 1 } , \dots , x _ { m } , \eta + \delta _ { x _ { 1 } } + \cdots + \delta _ { x _ { m } } ) ] \left ( \lambda _ { i } ^ { \prime } \right ) ^ { m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) .$$

By (A.7) this is the right-hand side of (4.11).

□

Next we formulate another useful version of the multivariate Mecke equation. For μ ∈ N and x ∈ X we define the measure μ \ δx ∈ N by

$$\mu \, \rangle \, \delta _ { x } \colon = \begin{cases} \mu - \delta _ { x } , & \text {if } \mu \geq \delta _ { x } , \\ \mu , & \text {otherwise.} \end{cases} \quad ( 4 . 1 4 )$$

For x1, . . , xm ∈ X, the measure μ\ δx1 \ · · · \ δx ∈ N is defined inductively.

Theorem 4.5 Let η be a proper Poisson process on X with s-inite intensity measure λ and let m ∈ N. Then, for any f ∈ R+(Xm ×N),

$$\mathbb { E } [ \int f ( x _ { 1 } , \dots , x _ { m } , \eta \, \lambda _ { x _ { 1 } } \, \vee \cdots \, \vee \delta _ { x _ { m } } ) \, \eta ^ { ( m ) } ( d ( x _ { 1 } , \dots , x _ { m } ) ) ] \\ = \int \mathbb { E } [ f ( x _ { 1 } , \dots , x _ { m } , \eta ) ] \, \lambda ^ { m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) .$$


<!-- p:43 -->


Proof If X is a subspace of a complete separable metric space as in Proposition 6.2, then it is easy to show that (x1, . . . , χm, μ) → μ \ δx1 \ · · . \ δx is a measurable mapping from X" × N1(X) to N(X). In that case, and if λ is locally finite, (4.15) follows upon applying (4.11) to the function (x1, . . , Xχm, μ) → f(x1, . . . , χm, μ \ δx1 \ · · . \ δx). In the general case we use that η is proper. Therefore the mapping (ω, x1, . . . , xm) ↔ η(ω)\δx1 \ · · ·\δx is measurable, which is enough to make (4.15) a meaningful statement. The proof can proceed in exactly the same way as the proof of Theorem 4.4. □

### 4.3 Janossy Measures

The restriction vB of a measure v on X to a set B ∈ X is a measure on X defined by

$$\nu _ { B } ( B ^ { \prime } ) \coloneqq \nu ( B \cap B ^ { \prime } ) , \quad B ^ { \prime } \in \mathcal { X } .$$

If η is a point process on X, then so is its restriction ηB. For B ∈ X, m ∈ N and a measure v on X we write v := (vB)n. For a point process η on X we write ηB (m) ) := (ηB)(m).

Factorial measures can be used to describe the restriction of point processes as follows.

Definition 4.6 Let η be a point process on X, let B ∈ X and m ∈ N. The Janossy measure of order m of η restricted to B is the measure on Xm defined by

$$J _ { \eta , B , m } \colon = \frac { 1 } { m ! } \mathbb { E } [ 1 \{ \eta ( B ) = m \} \eta _ { B } ^ { ( m ) } ( \cdot ) ] .$$

The number Jη,B,0 := P(η(B) = 0) is called the Janossy measure of order 0.

Note that the Janossy measures Jη,B,m are symmetric (see (A.17))) and

$$J _ { \eta , B , m } ( \mathbb { X } ^ { m } ) = \mathbb { P } ( \eta ( B ) = m ) , \quad m \in \mathbb { N } .$$

If P(η(B) &lt; ∞) = 1, then the Janossy measures determine the distribution of the restriction ηB of η to B:

Theorem 4.7 Let η and η′ be point processes on X. Let B ∈ X and assume that Jη,B,m = Jη′,B,m for each m ∈ N0. Then

$$\mathbb { P } ( \eta ( B ) < \infty , \eta _ { B } \in \cdot ) = \mathbb { P } ( \eta ^ { \prime } ( B ) < \infty , \eta ^ { \prime } _ { B } \in \cdot ) .$$


<!-- p:44 -->


Proof For notational convenience we assume that B = X. Let m ∈ N and suppose that μ ∈ N satisfies μ(X) = m. We assert for each A ∈ N that

$$\mathbf 1 \{ \mu \in A \} = \frac { 1 } { m ! } \int \mathbf 1 \{ \delta _ { x _ { 1 } } + \cdots + \delta _ { x _ { m } } \in A \} \mu ^ { ( m ) } ( d ( x _ { 1 } , \dots , x _ { m } ) ) .$$

Since both sides of (4.19) are finite measures in A, it suffices to prove this identity for each set A of the form

$$A = \{ \nu \in \mathbb { N } \colon \nu ( B _ { 1 } ) = i _ { 1 } , \dots , \nu ( B _ { n } ) = i _ { n } \} ,$$

where n ∈ N, B1, . . . , Bn ∈ X and i1, . . . , in ∈ N0. Given such a set, let μ' be defined as in Lemma A.15. Then μ ∈ A if and only if μ′ ∈ A and the right-hand side of (4.19) does not change upon replacing μ by μ'. Hence it suffices to check (4.19) for finite sums of Dirac measures. This is obvious from (4.4).

It follows from (4.17) that for all m ∈ N and f ∈ R+(X) we have

$$( 4 . 2 0 )$$

From (4.19) and (4.20) we obtain for each A ∈ N that

$$\mathbb { P } ( \eta ( \mathbb { X } ) < \infty , \eta \in A ) \\ = 1 \{ 0 \in A \} J _ { \eta , \mathbb { Z } , 0 } + \sum _ { m = 1 } ^ { \infty } \int 1 \{ \delta _ { x _ { 1 } } + \cdots + \delta _ { x _ { m } } \in A \} \, J _ { \eta , \mathbb { Z } , m } ( d ( x _ { 1 } , \dots , x _ { m } ) )$$

and hence the assertion.

□

Example 4.8 Let η be a Poisson process on X with s-finite intensity measure λ. Let m ∈ N and B ∈ X. By the multivariate Mecke equation (Theorem 4.4) we have for each C ∈ Xn that

$$J _ { \eta , B , m } ( C ) & = \frac { 1 } { m ! } \mathbb { E } [ \{ \eta ( B ) = m \} \eta ^ { ( m ) } ( B ^ { m } \cap C ) ] \\ & = \frac { 1 } { m ! } \mathbb { E } \left [ \int _ { C } \{ ( \eta + \delta _ { x _ { 1 } } + \dots + \delta _ { x _ { m } } ) ( B ) = m \} \lambda _ { B } ^ { m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) \right ] .$$

For x1, . . . , xm ∈ B we have (η + δx1 + · . · + δx)(B) = m if and only if η(B) = 0. Therefore we obtain

$$J _ { \eta , B , m } = \frac { e ^ { - \lambda ( B ) } } { m ! } \lambda _ { B } ^ { m } , \quad m \in \mathbb { N } .$$


<!-- p:45 -->


### 4.4 Factorial Moment Measures

Definition 4.9 For m ∈ N the m-th factorial moment measure of a point process η is the measure αm on X defined by

$$\alpha _ { m } ( C ) \colon = \mathbb { E } [ \eta ^ { ( m ) } ( C ) ] , \ \ C \in \mathcal { X } ^ { m } .$$

If the point process η is proper, i.e. given by (2.4), then

$$\alpha _ { m } ( C ) = \mathbb { E } \left [ \sum _ { i _ { 1 } , \dots , i _ { m } \leq \kappa } ^ { \neq } 1 \{ ( X _ { i _ { 1 } } , \dots , X _ { i _ { m } } ) \in C \} \right ] , \\ \intertext { d h e n c e $ f \in \mathbb { R } $ ( X ^ { m } ) $ w e h a v e $ that }$$

and hence for f ∈ R+(X") we have that

$$\int _ { X ^ { m } } f ( x _ { 1 } , \dots , x _ { m } ) \, \alpha _ { m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) = \mathbb { E } \left [ \sum _ { i _ { 1 } , \dots , i _ { m } \leq \kappa } ^ { \neq } f ( X _ { i _ { 1 } } , \dots , X _ { i _ { m } } ) \right ] .$$

The first factorial moment measure of a point process η is just the intensity measure of Definition 2.5, while the second describes the second order properties of η. For instance, it follows from (4.8) (and Exercise 4.4 if η is not proper) that

$$\alpha _ { 2 } ( B _ { 1 } \times B _ { 2 } ) = \mathbb { E } [ \eta ( B _ { 1 } ) \eta ( B _ { 2 } ) ] - \mathbb { E } [ \eta ( B _ { 1 } \cap B _ { 2 } ) ] ,$$

provided that E[η(B1 ∩ B2)] &lt; ∞.

Theorem 4.4 has the following immediate consequence:

Corollary 4.10 Given m ∈ N the m-th factorial moment measure of a Poisson process with s-finite intensity measure λ is λm.

$$\begin{array} { c c c } P r o o f & \text {Apply (4.11) to the function f(x_{1}, \dots , x_{m}, \eta) = 1 \{ ( x _ { 1 } , \dots , x _ { m } ) \in C \} } \\ \text {for } C \in \mathcal { X } ^ { m } . & \Box \end{array}$$

Let η be a point process on X with intensity measure λ and let f, g ∈ L1(λ) ∩ L2(λ). By the Cauchy-Schwarz inequality ((A.2) for p = q = 2) we have fg ∈ L1(λ) so that Campbell's formula (Proposition 2.7) shows that η(lfl) &lt; ∞ and η(lf gl) &lt; ∞ hold almost surely. Therefore it follows from the case m = 1 of (4.9) that

$$\int f ( x ) f ( y ) \, \eta ^ { ( 2 ) } ( d ( x , y ) ) = \eta ( f ) \eta ( g ) - \eta ( f g ) , \quad \mathbb { P } \text {-a.s.}$$

Reordering terms and taking expectations gives

$$\mathbb { E } [ \eta ( f ) \eta ( g ) ] = \lambda ( f g ) + \int f ( x ) g ( y ) \, \alpha _ { 2 } ( d ( x , y ) ) , \quad ( 4 . 2 5 )$$

provided that ∫|f(x)g(y)|α2(d(x, y)) &lt; ∞ or f, g ≥ 0. If η is a Poisson process with s-finite intensity measure λ, then (4.25) and Corollary 4.10 imply the following useful generalisation of Exercise 3.11:


<!-- p:46 -->


$$\mathbb { E } [ \eta ( f ) \eta ( g ) ] = \lambda ( f g ) + \lambda ( f ) \lambda ( g ) , \quad f , g \in L ^ { 1 } ( \lambda ) \cap L ^ { 2 } ( \lambda ) .$$

Under certain assumptions the factorial moment measures of a point process determine its distribution. To derive this result we need the following lemma. We use the conventions e−∞ := 0 and log 0 := -∞.

Lemma 4.11 Let η be a point process on X. Let B ∈ X and assume that there exists c &gt; 1 such that the factorial moment measures α of η satisfy

$$\alpha _ { n } ( B ^ { n } ) \leq n ! c ^ { n } , \ \ n \geq 1 .$$

Let u ∈ R+(X) and a &lt; c−1 be such that u(x) &lt; a for x ∈ B and u(x) = 0 for x∉B.Then

$$x \notin B . \, & \text {then} \\ & \mathbb { E } \left [ \exp \left ( \int \log ( 1 - u ( x ) ) \, \eta ( d x ) \right ) \right ] \\ & = 1 + \sum _ { n = 1 } ^ { \infty } \frac { ( - 1 ) ^ { n } } { n ! } \int u ( x _ { 1 } ) \cdots u ( x _ { n } ) \, \alpha _ { n } ( d ( x _ { 1 } , \dots , x _ { n } ) ) . \\ \intertext { \text {Proof} } & \text {Since } u \text { vanishes outside } B , \, \text {we have}$$

Proof Since u vanishes outside B, we have

$$P \coloneqq \exp \left ( \int \log ( 1 - u ( x ) ) \, \eta ( d x ) \right ) = \exp \left ( \int \log ( 1 - u ( x ) ) \, \eta _ { B } ( d x ) \right ) .$$

Hence we can assume that η(X \ B) = 0. Since α1(B) = E[η(B)] &lt; ∞, we can also assume that η(B) &lt; ∞. But then we obtain from Exercise 4.6 that

$$P = \sum _ { n = 0 } ^ { \infty } ( - 1 ) ^ { n } P _ { n } ,$$

where P0 := 1 and

$$P _ { n } \colon = \frac { 1 } { n ! } \int u ( x _ { 1 } ) \cdots u ( x _ { n } ) \, \eta ^ { ( n ) } ( d ( x _ { 1 } , \dots , x _ { n } ) ) ,$$

and where we note that η(n) = 0 if n &gt; η(X); see (4.7). Exercise 4.9 asks the reader to prove that

$$1 ^ { 2 m - 1 } & \sum _ { n = 0 } ^ { 2 m - 1 } ( - 1 ) ^ { n } P _ { n } \leq P \leq \sum _ { n = 0 } ^ { 2 m } ( - 1 ) ^ { n } P _ { n } , \quad m \geq 1 . \\$$

These inequalities show that

$$\left | P - \sum _ { n = 0 } ^ { k } ( - 1 ) ^ { n } P _ { n } \right | \leq P _ { k } , \ \ k \geq 1 .$$


<!-- p:47 -->


It follows that

$$\left | \mathbb { E } [ P ] - \mathbb { E } \left [ \sum _ { n = 0 } ^ { k } ( - 1 ) ^ { n } P _ { n } \right ] \right | \leq \mathbb { E } [ P _ { k } ] = \frac { 1 } { k ! } \int u ( x _ { 1 } ) \cdots u ( x _ { k } ) \, \alpha _ { k } ( d ( x _ { 1 } , \dots , x _ { k } ) ) ,$$

where we have used the definition of the factorial moment measures. The last term can be bounded by

$$\frac { a ^ { k } } { k ! } \alpha _ { k } ( B ^ { k } ) \leq a ^ { k } c ^ { k } ,$$

which tends to zero as k → ∞. This finishes the proof.

□

Proposition 4.12 Let η and η′ be point processes on X with the same factorial moment measures αn, n ≥ 1. Assume that there is a sequence Bk ∈ X, k ∈ N, with Bk ↑ X and numbers ck &gt; 0, k ∈ N, such that

$$\alpha _ { n } ( B _ { k } ^ { n } ) \leq n ! c _ { k } ^ { n } , \quad k , n \in \mathbb { N } .$$

Then η = η'.

Proof By Proposition 2.10 and monotone convergence it is enough to prove that Lη(v) = Lη(v) for each bounded v ∈ R+(X) such that there exists a set B ∈ {Bk : k ∈ N} with v(x) = 0 for all x ∉ B. This puts us into the setting of Lemma 4.11. Let v ∈ R+(X) have the upper bound a &gt; 0. For each t ∈ [0, −(log(1 − c−1))/a) we can apply Lemma 4.11 with u := 1 − e−tv. This gives us Lη(tv) = Lη(tv). Since t → Lη(tv) is analytic on (0, ∞), we (), = ()4    0     (), = () □

### 4.5 Exercises

Exercise 4.1 Let η be a Poisson process on X with intensity measure λ and let A ∈ N have P(η ∈ A) = 0. Use the Mecke equation to show that P(η + δx ∈ A) = 0 for λ-a.e. x.

Exercise 4.2 Let μ ∈ N be given by (4.3) and let m ∈ N. Show that

$$\mu ^ { ( m ) } ( C ) & = \int \cdots \int _ { 1 _ { C } ( x _ { 1 } , \dots , x _ { m } ) } ( \mu - \sum _ { j = 1 } ^ { m - 1 } \delta _ { x _ { j } } ) ( d x _ { m } ) \left ( \mu - \sum _ { j = 1 } ^ { m - 2 } \delta _ { x _ { j } } \right ) ( d x _ { m - 1 } ) \\ & \quad \cdots ( \mu - \delta _ { x _ { 1 } } ) ( d x _ { 2 } ) \mu ( d x _ { 1 } ) , \quad C \in \mathcal { X } ^ { m } .$$

This formula involves integrals with respect to signed measures of the form μ − ν, where μ, ν ∈ N and ν is finite. These integrals are defined as a difference of integrals in the natural way.


<!-- p:48 -->


Exercise 4.3 Let μ ∈ N and x ∈ X. Show for all m ∈ N that

$$\int [ 1 \{ ( x , x _ { 1 } , \dots , x _ { m } ) \in \cdot \} + \cdots + 1 \{ ( x _ { 1 } , \dots , x _ { m } , x ) \in \cdot \} ] \mu ^ { ( m ) } ( d ( x _ { 1 } , \dots , x _ { m } ) ) \\ + \mu ^ { ( m + 1 ) } = ( \mu + \delta _ { x } ) ^ { ( m + 1 ) } .$$

(Hint: Use Proposition A.18 to reduce to the case μ(X) &lt; ∞ and then Lemma A.15 to reduce further to the case (4.3) with k ∈ N.)

Exercise 4.4 Let μ ∈ N. Use the recursion (4.9) to show that (4.6), (4.7) and (4.8) hold.

Exercise 4.5 Let μ ∈ N be given by μ := Σk=1 δx, for some k ∈ N0 and some x1, . . . , xk ∈ X. Let u: X → R be measurable. Show that

$$\prod _ { j = 1 } ^ { k } ( 1 - u ( x _ { j } ) ) = 1 + \sum _ { n = 1 } ^ { k } \frac { ( - 1 ) ^ { n } } { n ! } \int u ( x _ { 1 } ) \cdots u ( x _ { n } ) \mu ^ { ( n ) } ( d ( x _ { 1 } , \dots , x _ { n } ) ) .$$

Exercise 4.6 Let μ ∈ N such that μ(X) &lt; ∞ and let u ∈ R+(X) satisfy u &lt; 1. Show that

$$u & < 1 . \text { Show that} \\ & \exp \left ( \int \log ( 1 - u ( x ) ) \mu ( d x ) \right ) \\ & = 1 + \sum _ { n = 1 } ^ { \infty } \frac { ( - 1 ) ^ { n } } { n ! } \int \prod _ { j = 1 } ^ { n } u ( x _ { j } ) \mu ^ { ( n ) } ( d ( x _ { 1 } , \dots , x _ { n } ) ) . \\$$

(Hint: If u takes only a finite number of values, then the result follows from Lemma A.15 and Exercise 4.5.)

Exercise 4.7 (Converse to Theorem 4.4) Let m ∈ N with m &gt; 1. Prove or disprove that for any σ-finite measure space (X, X, λ), if η is a point process on X satisfying (4.11) for all f ∈ R+(Xm × N), then η is a Poisson process with intensity measure λ. (For m = 1, this is true by Theorem 4.1.)

Exercise 4.8 Give another (inductive) proof of the multivariate Mecke identity (4.11) using the univariate version (4.2) and the recursion (4.9).

Exercise 4.9 Prove the inequalities (4.29). (Hint: Use induction.)

Exercise 4.10 Let η be a Poisson process on X with intensity measure λ and let B ∈ X with 0 &lt; λ(B) &lt; ∞. Let U1, . . . , U be independent random elements of X with distribution λ(B)−1 λ(B∩·) and assume that (U1, . . . , U) and η are independent. Show that the distribution of η + δu1 + · . · + δv is absolutely continuous with respect to P(η ∈ ·) and that μ → λ(B)-nμ(n)(Bn) is a version of the density.


<!-- p:49 -->


## Mappings, Markings and Thinnings

It was shown in Chapter 3 that an independent superposition of Poisson processes is again Poisson. The properties of a Poisson process are also preserved under other operations. A mapping from the state space to another space induces a Poisson process on the new state space. A more intriguing persistence property is the Poisson nature of position-dependent markings and thinnings of a Poisson process.

### 5.1 Mappings and Restrictions

Consider two measurable spaces (X, X) and (Y, Y) along with a measurable mapping T : X → Y. For any measure μ on (X, X) we define the image of μ under T (also known as the push-forward of μ), to be the measure T(μ) defined by T(μ) = μ  T−1, i.e.

$$T ( \mu ) ( C ) \colon = \mu ( T ^ { - 1 } C ) , \ \ C \in \mathcal { Y } .$$

In particular, if η is a point process on X, then for any ω ∈ Ω, T(η(ω)) is a measure on Y given by

$$T ( \eta ( \omega ) ) ( C ) = \eta ( \omega , T ^ { - 1 } ( C ) ) , \quad C \in \mathcal { Y } .$$

If η is a proper point process, i.e. one given by η = Σn=1 δx as in (2.4), the definition of T(η) implies that

$$T ( \eta ) = \sum _ { n = 1 } ^ { \kappa } \delta _ { T ( X _ { n } ) } .$$

Theorem 5.1 (Mapping theorem) Let η be a point process on X with intensity measure λ and let T : X → Y be measurable. Then T(η) is a point process with intensity measure T(λ). If η is a Poisson process, then T(η) is a Poisson process too.


<!-- p:50 -->


Proof We first note that T(μ) ∈ N for any μ ∈ N. Indeed, if μ = Σj=1 μj, then T(μ) = Σj=1 T(μj). Moreover, if the μj are N0-valued, so are the T(μj).

For any C ∈ Y, T(η)(C) is a random variable and by the definition of the intensity measure its expectation is

$$\mathbb { E } [ T ( \eta ) ( C ) ] = \mathbb { E } [ \eta ( T ^ { - 1 } C ) ] = \lambda ( T ^ { - 1 } C ) = T ( \lambda ) ( C ) .$$

If η is a Poisson process, then it can be checked directly that T(η) is completely independent (property (ii) of Definition 3.1), and that T(η)(C) has a Poisson distribution with parameter T(λ)(C) (property (i) of Definition 3.1). □

If η is a Poisson process on X then we may discard all of its points outside a set B ∈ X to obtain another Poisson process. Recall from (4.16) the definition of the restriction vB of a measure v on X to a set B ∈ X.

Theorem 5.2 (Restriction theorem) Let η be a Poisson process on X with s-finite intensity measure λ and let C1, C2,... ∈ X be pairwise disjoint. Then ηc1, ηC2, ... are independent Poisson processes with intensity measures λc1, λC2, . . . , respectively.

Proof As in the proof of Proposition 3.5, it is no restriction of generality to assume that the union of the sets C is all of X. (If not, add the complement of this union to the sequence (C).) First note that, for each i ∈ N, ηc, has intensity measure λc, and satisfies the two defining properties of a Poisson process. By the existence theorem (Theorem 3.6) we can find a sequence η, i ∈ N, of independent Poisson processes on a suitable (product) probability space, with ηi having intensity measure λc, for each i.

By the superposition theorem (Theorem 3.3), the point process η′ := Σi=1 ηi is a Poisson process with intensity measure λ. Then η′  η by Proposition 3.2. Hence for any k and any f1, . . . , fk ∈ R+ (N) we have

$$\mathbb { E } \left [ \prod _ { i = 1 } ^ { k } f _ { i } ( \eta _ { C _ { i } } ) \right ] = \mathbb { E } \left [ \prod _ { i = 1 } ^ { k } f _ { i } ( \eta _ { C _ { i } } ^ { \prime } ) \right ] = \mathbb { E } \left [ \prod _ { i = 1 } ^ { k } f _ { i } ( \eta _ { i } ) \right ] = \prod _ { i = 1 } ^ { k } \mathbb { E } [ f _ { i } ( \eta _ { i } ) ] .$$

Taking into account that ηci = η for all i ∈ N (Proposition 3.2), we get the result. □

### 5.2 The Marking Theorem

Suppose that η is a proper point process, i.e. one that can be represented as in (2.4). Suppose that one wishes to give each of the points X a random mark Yn with values in some measurable space (Y, Y), called the mark space. Given η, these marks are assumed to be independent, while their conditional distribution is allowed to depend on the value of X but not on any other information contained in η. This marking procedure yields a point process ξ on the product space X × Y. Theorem 5.6 will show the remarkable fact that if η is a Poisson process then so is ξ.


<!-- p:51 -->


To make the above marking idea precise, let K be a probability kernel from X to Y, that is a mapping K: X × y → [0, 1] such that K(x, ·) is a probability measure for each x ∈ X and K(·, C) is measurable for each C ∈ y.

Definition 5.3 Let η = Σn=1 δx be a proper point process on X. Let K be a probability kernel from X to Y. Let Y1, Y2, . .. be random elements in Y and assume that the conditional distribution of (Yn)n≤m given κ = m ∈ N and (X)n≤m is that of independent random variables with distributions K(X, ·), n ≤ m. Then the point process

$$\xi \coloneqq \sum _ { n = 1 } ^ { \kappa } \delta _ { ( X _ { n } , Y _ { n } ) } \\$$

is called a K-marking of η. If there is a probability measure Q on Y such that K(x, ·) = Q for all x ∈ X, then ξ is called an independent Q-marking of η.

For the rest of this section we fix a probability kernel K from X to Y. If the random variables Y, n ∈ N, in Definition 5.3 exist, then we say that the underlying probability space (Ω, F, P) supports a K-marking of η. We now explain how (Ω, F, P) can be modified so as to support a marking. Let Ω := Ω × Y∞ be equipped with the product σ-field. Define a probability kernel  from Ω to Y∞ by taking the infinite product

$$\tilde { K } ( \omega , \cdot ) \colon = \bigotimes _ { n = 1 } ^ { \infty } K ( X _ { n } ( \omega ) , \cdot ) , \quad \omega \in \Omega . \\$$

We denote a generic element of Y∞ by y = (yn)n≥1. Then

$$\tilde { \mathbb { P } } \coloneqq \int 1 \{ ( \omega , y ) \in \cdot \} \, \tilde { K } ( \omega , d y ) \, \mathbb { P } ( d \omega )$$

is a probability measure on  that can be used to describe a K-marking of η. Indeed, for  = (ω, y) ∈ Ω we can define η() := η(ω) and, for n ∈ N, (( ̄), Yn()) := (X(ω), yn). Then the distribution of (η(X), ()) under P coincides with that of (η(X), (X)) under P. Moreover, it is easy to check that under  the conditional distribution of (Yn)n≤m given ñ(X) = m ∈ N and


<!-- p:52 -->


()n≤m is that of independent random variables with distributions K(, ·), n ≤ m. This construction is known as an extension of a given probability space so as to support further random elements with a given conditional distribution. In particular, it is no restriction of generality to assume that our fixed probability space supports a K-marking of η.

The next proposition shows among other things that the distribution of a K-marking of η is uniquely determined by K and the distribution of η.

Proposition 5.4 Let ξ be a K-marking of a proper point process η on X as in Definition 5.3. Then the Laplace functional of ξ is given by

$$L _ { \xi } ( u ) = L _ { \eta } ( u ^ { * } ) , \ \ u \in \mathbb { R } _ { + } ( \mathbb { X } \times \mathbb { Y } ) ,$$

where

$$u ^ { * } ( x ) \colon = - \log \left [ \int e ^ { - u ( x , y ) } \, K ( x , d y ) \right ] , \quad x \in \mathbb { X } .$$

Proof Recall that Ñ0 := N0 ∪ {∞}. For u ∈ R+(X × Y) we have that

$$\text {Proof} \quad \text {Recall that } \mathbb { N } _ { 0 } \coloneqq \mathbb { N } _ { 0 } \cup \{ \infty \} . \text { For } u \in \mathbb { R } _ { + } ( \mathbb { X } \times \mathbb { Y } ) \text { we have that } \\ L _ { \xi } ( u ) & = \sum _ { m \in \mathbb { N } _ { 0 } } \mathbb { E } \left [ 1 \{ \kappa = m \} \exp \left [ - \sum _ { k = 1 } ^ { m } u ( X _ { k } , Y _ { k } ) \right ] \right ] \\ & = \sum _ { m \in \mathbb { N } _ { 0 } } \mathbb { E } \left [ 1 \{ \kappa = m \} \int \cdots \int \exp \left [ - \sum _ { k = 1 } ^ { m } u ( X _ { k } , y _ { k } ) \right ] \prod _ { k = 1 } ^ { m } K ( X _ { k } , d y _ { k } ) \right ] , \\ \text {where in the case } m = 0 \text { empty sums are set to } 0 \text { while empty products are }$$

where in the case m = 0 empty sums are set to 0 while empty products are set to 1. Therefore

$$L _ { \ell } ( u ) & = \sum _ { m \in \mathbb { N } _ { 0 } } \mathbb { E } \left [ 1 \{ \kappa = m \} \left ( \prod _ { k = 1 } ^ { m } \int \exp [ - u ( X _ { k } , y _ { k } ) ] K ( X _ { k } , d y _ { k } ) \right ) \right ] . \\$$

Using the function u* defined by (5.8) this means that

$$\L _ { \xi } ( u ) & = \sum _ { m \in \bar { \mathbb { N } } _ { 0 } } \mathbb { E } \left [ 1 \{ \kappa = m \} \left ( \prod _ { k = 1 } ^ { m } \exp [ - u ^ { * } ( x _ { k } ) ] \right ) \right ] \\ & = \sum _ { m \in \bar { \mathbb { N } } _ { 0 } } \mathbb { E } \left [ 1 \{ \kappa = m \} \exp \left ( - \sum _ { k = 1 } ^ { m } u ^ { * } ( X _ { k } ) \right ) \right ] , \\ \intertext { s i l e r g h t r i d h a n d s i d e o f t h e a s e r t e d i n d e t i o n g ( 5 . 7 ) . }$$

which is the right-hand side of the asserted identity (5.7).

□

The next result says that the intensity measure of a K-marking of a point process with intensity measure λ is given by λ ø K, where

$$( \lambda \otimes K ) ( C ) \colon = \iint \mathbf 1 _ { C } ( x , y ) \, K ( x , d y ) \, \lambda ( d x ) , \quad C \in \mathcal { X } \otimes \mathcal { Y } .$$


<!-- p:53 -->


In the case of an independent Q-marking this is the product measure λøQ. If λ and K are s-finite, then so is λ ⊗ K.

Proposition 5.5 Let η be a proper point process on X with intensity measure λ and let ξ be a K-marking of η. Then ξ is a point process on X ×Y with intensity measure λ⊗ K.

Proof Let C ∈ X ø Y. Similarly to the proof of Proposition 5.4 we have that

$$\text {that} \\ \mathbb { E } [ \xi ( C ) ] & = \sum _ { m \in \mathbb { N } _ { 0 } } \mathbb { E } \left [ 1 \{ \kappa = m \} \sum _ { k = 1 } ^ { m } 1 \{ ( X _ { k } , Y _ { k } ) \in C \} \right ] \\ & = \sum _ { m \in \mathbb { N } _ { 0 } } \mathbb { E } \left [ 1 \{ \kappa = m \} \sum _ { k = 1 } ^ { m } \int 1 \{ ( X _ { k } , y _ { k } ) \in C \} \, K ( X _ { k } , d y _ { k } ) \right ] . \\ \text {Using Campbell's formula} \, ( \text {Position} \, 2 . 7 ) \text { with } \mu \in \mathbb { R } _ { + } ( \mathbb { X } ) \text { defined by }$$

Using Campbell's formula (Proposition 2.7) with u ∈ R+(X) defined by u(x) := ∫ 1{(x, y) ∈ C} K(x, dy), x ∈ X, we obtain the result. □

Now we formulate the previously announced behaviour of Poisson processes under marking.

Theorem 5.6 (Marking theorem) Let ξ be a K-marking of a proper Poisson process η with s-inite intensity measure λ. Then ξ is a Poisson process with intensity measure λ⊗ K.

Proof Let u ∈ R+(X × Y). By Proposition 5.4 and Theorem 3.9,

$$L _ { \xi } ( u ) & = \exp \left [ - \int ( 1 - e ^ { - u ^ { * } ( x ) } ) \, \lambda ( d x ) \right ] \\ & = \exp \left [ - \iint ( 1 - e ^ { - u ( x , y ) } ) \, K ( x , d y ) \, \lambda ( d x ) \right ] . \\$$

Another application of Theorem 3.9 shows that ξ is a Poisson process.

Under some technical assumptions we shall see in Proposition 6.16 that any Poisson process on a product space is a K-marking for some kernel K, determined by the intensity measure.

### 5.3 Thinnings

A thinning keeps the points of a point process η with a probability that may depend on the location and removes them otherwise. Given η, the thinning decisions are independent for different points. The formal definition can be based on a special K-marking:


<!-- p:54 -->


Definition 5.7 Let p: X → [0, 1] be measurable and consider the probability kernel K from X to {0, 1} defined by

$$K _ { p } ( x , \cdot ) \colon = ( 1 - p ( x ) ) \delta _ { 0 } + p ( x ) \delta _ { 1 } , \quad x \in \mathbb { X } .$$

If ξ is a Kp-marking of a proper point process η, then ξ(· × {1}) is called a p-thinning of η.

We shall use this terminology also in the case where p(x) ≡ p does not depend on x ∈ X.

Figure 5.1 Illustration of a marking and a thinning, both based on the same set of marked points. The points on the horizontal axis represent the original point process in the first diagram, and the thinned point process in the second diagram.

o

0

o


0

→

X


More generally, let pi, i ∈ N, be a sequence of measurable functions from X to [0, 1] such that

$$\sum _ { i = 1 } ^ { \infty } p _ { i } ( x ) = 1 , \quad x \in \mathbb { X } .$$

Define a probability kernel K from X to N by

$$K ( x , \{ i \} ) \colon = p _ { i } ( x ) , \ \ x \in \mathbb { X } , \ i \in \mathbb { N } .$$

If ξ is a K-marking of a point process η, then ηi := ξ(· × {i}) is a pithinning of η for every i ∈ N. By Proposition 5.5, η has intensity measure p(x) λ(dx), where λ is the intensity measure of η. The following generalisation of Proposition 1.3 is consistent with the superposition theorem (Theorem 3.3).

Theorem 5.8 Let ξ be a K-marking of a proper Poisson process η, where K is given as in (5.11). Then ηi := ξ(· × {i}), i ∈ N, are independent Poisson processes.


<!-- p:55 -->


Proof By Theorem 5.6, ξ is a Poisson process. Hence we can apply Theorem 5.2with C := X × {i} to obtain the result. □

If ηp is a p-thinning of a proper point process η then (according to Definitions 2.4 and 5.7) there is an A ∈ F such that P(A) = 1 and ηp(ω) ≤ η(ω) for each ω ∈ A. We can then define a proper point process η – ηp by setting (η − ηp)(ω) := η(ω) − ηp(ω) for ω ∈ A and (η − ηp)(ω) := 0, otherwise.

Corollary 5.9 (Thinning theorem) Let p: X → [0, 1] be measurable and let ηp be a p-thinning of a proper Poisson process η. Then ηp and η − ηp are independent Poisson processes.

### 5.4 Exercises

Exercise 5.1 (Displacement theorem) Let λ be an s-finite measure on the Euclidean space Rd, let Q be a probability measure on Rd and let the convolution λ * Q be the measure on Rd, defined by

$$( \lambda * \mathbb { Q } ) ( B ) \colon = \iint 1 _ { B } ( x + y ) \, \lambda ( d x ) \, \mathbb { Q } ( d y ) , \quad B \in \mathcal { B } ( \mathbb { R } ^ { d } ) .$$

Show that λ * Q is s-finite. Let η = ∑n=1 δx be a Poisson process with intensity measure λ and let (Y) be a sequence of independent random vectors with distribution Q that is independent of η. Show that η′ := Σn=1 δx+r, is a Poisson process with intensity measure λ * Q.

Exercise 5.2 Let η1 and η2 be independent Poisson processes with intensity measures λ1 and λ2, respectively. Let p be a Radon-Nikodým derivative of λ1 with respect to λ := λ1 +λ2. Show that η1 has the same distribution as a p-thinning of η1 + η2.

Exercise 5.3 Let ξ1, . . . , ξn be identically distributed point processes and let ξ(n) be an n−1-thinning of ξ := ξ1 + · · · + ξn. Show that ξ(n) has the same intensity measure as ξ1. Give examples where ξ1, ..., ξ are independent and where ξ(n) and ξ1 have (resp. do not have) the same distribution.

Exercise 5.4 Let p: X → [0, 1] be measurable and let ηp be a p-thinning of a proper point process η. Using Proposition 5.4 or otherwise, show that

$$L _ { \eta _ { o } } ( u ) = \mathbb { E } \left [ \exp \left ( \int \log \left ( 1 - p ( x ) + p ( x ) e ^ { - u ( x ) } \right ) \eta ( d x ) \right ) \right ] , \quad u \in \mathbb { R } _ { + } ( \mathbb { X } ) .$$

Exercise 5.5 Let η be a proper Poisson process on X with σ-finite intensity measure λ. Let λ' be a σ-finite measure on X and let ρ := λ + λ'. Let h := dλ/dρ (resp. h′ := dλ'/dρ) be the Radon–Nikodým derivative of


<!-- p:56 -->


λ (resp. λ') with respect to ρ; see Theorem A.10. Let B := {h &gt; h'} and define p: X → [0, 1] by p(x) := h′(x)/h(x) for x ∈ B and by p(x) := 1, otherwise. Let η' be a p-thinning of η and let η" be a Poisson process with intensity measure 1x\B(x)(h′(x) − h(x)) ρ(dx), independent of η′. Show that η′ + η is a Poisson process with intensity measure λ'.

Exercise 5.6 (Poisson cluster process) Let K be a probability kernel from X to N(X). Let η be a proper Poisson process on X with intensity measure λ and let A ∈ F such that P(A) = 1 and such that (2.4) holds on A. Let ξ be a K-marking of η and define a point process χ on X by setting

$$\chi ( \omega , B ) \coloneqq \int \mu ( B ) \, \xi ( \omega , d ( x , \mu ) ) , \quad B \in \mathcal { X } ,$$

for ω ∈ A and χ(ω, ·) := 0, otherwise. Show that χ has intensity measure

$$\lambda ^ { \prime } ( B ) = \iint \mu ( B ) \, K ( x , d \mu ) \, \lambda ( d x ) , \quad B \in \mathcal { X } .$$

Show also that the Laplace functional of χ is given by

$$L _ { \chi } ( v ) = \exp \left [ - \int ( 1 - e ^ { - \mu ( v ) } ) \, \tilde { \lambda } ( d \mu ) \right ] , \quad v \in \mathbb { R } _ { + } ( \mathbb { X } ) , \quad ( 5 . 1 3 )$$

where λ := ∫ K(x, ·) λ(dx).

Exercise 5.7 Let χ be a Poisson cluster process as in Exercise 5.6 and let B ∈ X. Combine Exercise 2.7 and (5.13) to show that

$$\mathbb { P } ( \chi ( B ) = 0 ) = \exp \left [ - \int \mathbf 1 \{ \mu ( B ) > 0 \} \ \tilde { \lambda } ( d \mu ) \right ] .$$

Exercise 5.8 Let χ be as in Exercise 5.6 and let B ∈ X. Show that P(χ(B) &lt; ∞) = 1 if and only if λ({μ ∈ N : μ(B) = ∞}) = 0 and λ(μ ∈ N : μ(B) &gt; 0}) &lt; ∞. (Hint: Use P(χ(B) &lt; ∞) = lim,↓0 E[e−tχ(B)].)

Exercise 5.9 Let p ∈ [0, 1) and suppose that ηp is a p-thinning of a proper point process η. Let f ∈ R+(X ×N) and show that

$$\text {point process} \, \eta . \, \text {Let} \, f \in \mathbb { R } _ { + } ( \mathbb { X } \times \mathbb { N } ) \, \text {and show that} \\ \mathbb { E } [ \int f ( x , \eta _ { p } ) \, \eta _ { p } ( d x ) ] = \frac { p } { 1 - p } \mathbb { E } [ \int f ( x , \eta _ { p } + \delta _ { x } ) \, ( \eta - \eta _ { p } ) ( d x ) ] .$$


<!-- p:57 -->


6

## Characterisations of the Poisson Process

A point process without multiplicities is said to be simple. For locally finite simple point processes on a metric space without fixed atoms the two defining properties of a Poisson process are equivalent. In fact, Rényi's theorem says that in this case even the empty space probabilities suffice to imply that the point process is Poisson. On the other hand, a weak (pairwise) version of the complete independence property leads to the same conclusion. A related criterion, based on the factorial moment measures, is also given.

### 6.1 Borel Spaces

In this chapter we assume (X, X) to be a Borel space in the sense of the following definition. In the first section we shall show that a large class of point processes is proper.

Definition 6.1 A Borel space is a measurable space (Y, Y) such that there is a Borel-measurable bijection φ from Y to a Borel subset of the unit interval [0, 1] with measurable inverse.

A special case arises when X is a Borel subset of a complete separable metric space (CSMS) and X is the σ-field on X generated by the open sets in the inherited metric. In this case, (X, X) is called a Borel subspace of the CSMS; see Section A.2. By Theorem A.19, any Borel subspace X of a CSMS is a Borel space. In particular, X is then a metric space in its own right.

Recall that N&lt;∞(X) denotes the set of all integer-valued measures on X.

Proposition 6.2 There exist measurable mappings π: N&lt;∞(X) → X, n ∈ N, such that for all μ ∈ N&lt;∞(X) we have

$$\mu = \sum _ { n = 1 } ^ { \mu ( N ) } \delta _ { \pi _ { n } ( \mu ) } .$$


<!-- p:58 -->


Proof Take a measurable bijection φ from X onto a Borel subset U of [0, 1] such that the inverse of φ is measurable. For μ ∈ N&lt;∞ := N&lt;∞(X) we define a finite measure φ(μ) on R by φ(μ) := μ  φ−1, that is,

$$\varphi ( \mu ) ( B ) = \mu ( \{ x \, \colon \varphi ( x ) \in B \} ) , \quad B \in \mathcal { B } ( \mathbb { R } ) .$$

Here we interpret φ as a mapping from X to R, so that φ−1(B) = Ø whenever B ∩ U = 0. Hence φ(μ) is concentrated on U, that is φ(μ)(R \ U) = 0. For n ∈ N, set

$$Y _ { n } ( \mu ) \colon = \inf \{ x \in \mathbb { R } \, \colon \varphi ( \mu ) ( ( - \infty , x ] ) \geq n \} , \quad \mu \in N _ { < \infty } ,$$

where inf ∅ := ∞. For n &gt; μ(X) we have Yn(μ) = ∞. For n ≤ μ(X) we have Yn(μ) ∈ U. Indeed, in this case φ(μ){Yn(μ)} &gt; 0.

For x ∈ R we have

$$\{ \mu \in N _ { < \infty } \colon Y _ { n } ( \mu ) \leq x \} & = \{ \mu \in N _ { < \infty } \colon \varphi ( \mu ) ( ( - \infty , x ] ) \geq n \} \\ & = \{ \mu \in N _ { < \infty } \colon \mu ( \varphi ^ { - 1 } ( ( - \infty , x ] ) ) \geq n \} ,$$

so Yn is a measurable mapping on N&lt;∞. Also

$$\varphi ( \mu ) ( B ) = \sum _ { n = 1 } ^ { \mu ( \% ) } \delta _ { Y _ { n } ( \mu ) } ( B ) , \quad \mu \in N _ { < \infty } , \\$$

for all B of the form B = (−∞, x] with x ∈ R (a π-system of sets), and hence for all Borel sets B ⊂ R (by Theorem A.5). Fix x0 ∈ X and define

$$X _ { n } ( \mu ) \colon = \begin{cases} \varphi ^ { - 1 } ( Y _ { n } ( \mu ) ) , & \text {if $n \leq \mu ( \mathbb{X})$,} \\ x _ { 0 } , & \text {otherwise.} \end{cases}$$

By (6.2) we have for all B ∈ X that

$$\mu ( B ) = \mu ( \varphi ^ { - 1 } ( \varphi ( B ) ) ) = \sum _ { n = 1 } ^ { \mu ( Z ) } 1 \{ Y _ { n } ( \mu ) \in \varphi ( B ) \} = \sum _ { n = 1 } ^ { \mu ( Z ) } 1 \{ X _ { n } ( \mu ) \in B \}$$

and hence μ = ∑ μ(X) ) δx(μ). Then (6.1) holds with πn(μ) = Xn(μ).

□

In the case where X is a Borel subspace of a CSMS, recall from Definition 2.11 that N(X) denotes the class of all measures from N(X) that are locally finite, that is finite on bounded Borel sets. The preceding proposition implies a measurable decomposition of these measures.

Proposition 6.3 Suppose that X is a Borel subspace of a CSMS. Then there are measurable mappings π: N(X) → X, n ∈ N, such that for all Proof Let B1, B2, . .. be a sequence of disjoint bounded sets in X, forming a partition of X. Recall from (4.16) the definition of the restriction μBi of μ to B. By Theorem A.19, each Bi is a Borel space. Hence we can apply Proposition 6.2 to obtain for each i ∈ N measurable mappings πi,j : N1(X) → Bi, j ∈ N, such that


<!-- p:59 -->


$$\mu _ { B _ { i } } = \sum _ { j = 1 } ^ { \mu ( B _ { i } ) } \delta _ { \pi _ { i , j } ( \mu ) } , \quad \mu \in \mathbb { N } _ { l } ( \mathbb { X } ) .$$

Fix x0 ∈ X and let μ ∈ N1(X). If μ = 0 is the zero measure, for all n ∈ N we set π(μ) := x0. Otherwise let k1 = k1(μ) be the smallest i ∈ N such that μ(Bi) &gt; 0 and define πn(μ) := πk1,n(μ) for 1 ≤ n ≤ μ(Bk1 ). If μ(X) = μ(Bk1) 1et πn(μ) := x0 for n &gt; μ(B1). Otherwise we define πk1+m(μ) := πk2,m(μ) for 1 ≤ m ≤ μ(Bk2), where k2 ≡ k2(μ) is the smallest i &gt; k such that μ(Bi) &gt; 0.

It is now clear how to construct a sequence π : N1(X) → X, n ∈ N, inductively, such that (6.1) holds. Measurability can be proved by induction, using the fact that the πi,j are measurable. Since N(X) is a measurable subset of N(X) (see the discussion after Definition 2.11) the mappings π can be extended to measurable mappings on N(X). □

The following definition generalises the concept of a locally finite point process (see Definition 2.13) to point processes on an arbitrary (not necessarily Borel) phase space.

Definition 6.4 A point process η on a measurable space (Y, Y) is said to be uniformly σ-finite if there exist Bn ∈ Y, n ∈ N, such that ∪x=1Bn = Y and

$$\mathbb { P } ( \eta ( B _ { n } ) < \infty ) = 1 , \ \ n \in \mathbb { N } .$$

We note that Poisson processes with σ-finite intensity measure and locally finite point processes on a metric space are uniformly σ-finite.

It follows from Proposition 6.2 that every uniformly σ-finite point process on the Borel space X is proper. As mentioned just after Definition 2.4 this shows in particular that all locally finite point processes are proper.

Corollary 6.5 Let η be a uniformly σ-finite point process on X. Then η is a proper point process. That is, there exist random elements X1, X2, ... in X and an Ñ0-valued random variable κ such that almost surely

$$\eta = \sum _ { n = 1 } ^ { K } \delta _ { X _ { n } } .$$


<!-- p:60 -->


Proof Choose the sets Bk, k ∈ N, as in Definition 6.4 and assume without loss of generality that these sets are pairwise disjoint. Let ηk := ηBk be the restriction of η to Bk. By definition (see also the discussion after Definition 2.13) there are random elements ñk of N&lt;∞(X) such that ηk and ñk are almost surely equal. For each k we can now use Proposition 6.2 to define κ := η(X) and, for n ∈ N, Xn := π(ñk), to see that ηk is proper. Since η = Σk ηk, Exercise 2.4 shows that η is proper. □

### 6.2 Simple Point Processes

In this section we discuss point processes without multiplicities.

Definition 6.6 A measure μ ∈ N(X) is said to be simple if μ{x} ≤ 1 for all x ∈ X. Let Ns(X) denote the set of all simple measures in N(X). If (X, X) is a metric space then let Nls(X) := N1(X) ∩ Ns(X); see Definition2.11.

There is a convenient description of Ns(X) based on the diagonal in X2, defined by

$$D _ { \mathbb { X } } \colon = \{ ( x , y ) \in \mathbb { X } ^ { 2 } \, \colon x = y \} .$$

Proposition 6.7 Let μ ∈ N(X). Then μ ∈ Ns(X) if and only if μ(2)(Dx) = 0. Moreover, Ns(X) is measurable, i.e. Ns(X) ∈ N(X).

Proof We first note that Dx is measurable, that is Dx ∈ X ⊗ X. Indeed, this holds if X is a Borel subset of [0, 1]. Using the definition of a Borel space, the measurability can be extended to the general case.

By definition, there is a sequence μ, n ∈ N, of finite measures in N(X) such that μ = ∑ μ. By Proposition 6.2, each of the μ and hence also μ is of the form (4.3). Therefore (4.5) implies for each x ∈ X that μ(2){(x, x)} = 0 if and only if μ{x} ≤ 1. This proves the first assertion. The measurability of Ns(X) is then a consequence of Proposition 4.3. □

Point processes without multiplicities deserve a special name:

Definition 6.8 A point process η is said to be simple if P(η ∈ Ns(X)) = 1.

If η is a simple point process on X and η' ≡ η, then η′ is also simple. Similarly to Section 2.4 we say that a measure v on X is diffuse if v{x} := v({x}) = 0 for each x ∈ X.

Proposition 6.9 Let η be a Poisson process on X with s-finite intensity measure λ. Then η is simple if and only if λ is diffuse.


<!-- p:61 -->


Proof Suppose λ is not diffuse. Let x ∈ X with c := λ{x} &gt; 0. Then

$$\mathbb { P } ( \eta \{ x \} \geq 2 ) = 1 - e ^ { - c } - c e ^ { - c } > 0 ,$$

so that η is not simple.

Conversely, suppose that λ is diffuse. We need to show that η is simple. By Proposition 6.7 this amounts to proving that P(η(2)(Dx) = 0) = 1 or, equivalently, E[η(2)(Dx)] = 0. By Corollary 4.10 we have that

$$\mathbb { E } [ \eta ^ { ( 2 ) } ( D _ { \mathcal { X } } ) ] = \iint 1 \{ x = y \} \, \lambda ( d x ) \, \lambda ( d y ) = \int \lambda ( \{ y \} ) \, \lambda ( d y ) = 0 ,$$

and the proof is complete.

□

### 6.3 Rényi's Theorem

The following (at first glance surprising) result shows that the two defining properties of a Poisson process are not independent of each other. In fact, this result, together with Theorem 6.12, shows that under certain extra conditions, either of the defining properties of the Poisson process implies the other. We base the proof on a more general result for simple point processes.

Theorem 6.10 (Rényi's theorem) Suppose that λ is a diffuse s-inite measure on X, and that η is a simple point process on X satisfying

$$\mathbb { P } ( \eta ( B ) = 0 ) = \exp [ - \lambda ( B ) ] , \quad B \in \mathcal { X } .$$

Then η is a Poisson process with intensity measure λ.

Proof Let η' be a Poisson process with intensity measure λ. Then assumption (6.6) implies (6.7) below. Proposition 6.9 shows that η' is simple. Theorem 6.11 shows that η and η' have the same distribution. □

Theorem 6.11 Let η and η′ be simple point processes on X such that

$$\mathbb { P } ( \eta ( B ) = 0 ) = \mathbb { P } ( \eta ^ { \prime } ( B ) = 0 ) , \quad B \in \mathcal { X } .$$

Then η = η'.

Proof Take a measurable bijection φ from X onto a Borel subset of I := [1/4, 3/4] such that the inverse of φ is measurable. We interpret φ as a mapping from X to I. Define a point process ξ on I by

$$\xi ( B ) \coloneqq \eta \circ \varphi ^ { - 1 } ( B ) = \eta ( \{ x \in \mathbb { X } \colon \varphi ( x ) \in B \} ) , \quad B \in \mathcal { B } ( I ) .$$

Since φ is one-to-one it follows that ξ{x} = η(φ−1({x})) ≤ 1 for all x ∈ I, provided η ∈ Ns. Hence ξ is simple. The same holds for ξ′ := η′ o φ−1. Since φ is one-to-one we have η = ξ  φ and η′ = ξ′  φ. Furthermore, since μ ↔ μ(φ(B)) is measurable for all B ∈ X, μ → μ  φ is a measurable mapping from N(I) to N(X). Since equality in distribution is preserved under measurable mappings, it now suffices to prove that ξ = ξ'.


<!-- p:62 -->


Let N* denote the sub-σ-field of N(I) generated by the system

$$\mathcal { H } \colon = \{ \{ \mu \in \mathbf N ( I ) \, \colon \mu ( B ) = 0 \} \, \colon B \in \mathcal { B } ( I ) \} .$$

Since, for any measure μ on I and any two sets B, B′ ∈ B(I), the equation μ(B ∪ B′) = 0 is equivalent to μ(B) = μ(B′) = 0, H is a π-system. By assumption (6.7), Pξ agrees with Pξ on H, and therefore, by Theorem A.5, Pξ agrees with Pξ on N*.

For n ∈ N and j ∈ {1, . . . , 2n} let In,j := ((j−1)2−n, j2−"]. Given B ∈ B(I), define

$$g _ { n , B } ( \mu ) \colon = \sum _ { j = 1 } ^ { 2 ^ { n } } \mu ( I _ { n , j } \cap B ) \wedge 1 , \quad \mu \in \mathbb { N } ( I ) , \, n \in \mathbb { N } ,$$

where a ∧ b := min{a, b} denotes the minimum of a, b ∈  ̄. Define the function gB: N(I) → R+ by

$$g _ { B } ( \mu ) \coloneqq \lim _ { n \to \infty } g _ { n , B } ( \mu ) , \ \mu \in \mathbb { N } ( I ) .$$

Then gB is an N*-measurable function on N(I). Moreover, if μ ∈ Ns(X), then g(μ) = μ(B). To see this, one can represent μ in the form (4.3) (justified by Proposition 6.2 and the definition of N(X)) and distinguish the cases μ(B) &lt; ∞ and μ(B) = ∞. Since ξ is simple we obtain ξ(B) = gB(ξ), almost surely, and therefore, for any m ∈ N, B1, . . . , B ∈ B(I) and k1, . . . , km ∈ N0, we have

$$\mathbb { P } ( \cap _ { i = 1 } ^ { m } \{ \xi ( B _ { i } ) = k _ { i } \} ) = \mathbb { P } ( \xi \in \cap _ { i = 1 } ^ { m } g _ { B _ { i } } ^ { - 1 } ( \{ k _ { i } \} ) ) ,$$

and, since ∩i=18-−1({ki}) ∈ N*, the corresponding probability for ξ′ is the same. Therefore, by Proposition 2.10, ξ′ ≡ ξ. □

A point process η on X satisfies

$$\eta \{ x \} = 0 , \quad \mathbb { P } { \text {-a.s.} , \, x \in \mathbb { X } } ,$$

if and only if its intensity measure is diffuse. If, in addition, η is uniformly σ-finite and simple, then the following result shows that we need only a weak version of the complete independence property to ensure that η is a Poisson process. This complements Theorem 6.10.


<!-- p:63 -->


Theorem 6.12 Suppose that η is a uniformly σ-inite simple point process on X satisfying (6.11). Assume also that {η(B) = 0} and {η(B′) = 0} are independent whenever B, B' ∈ X are disjoint. Then η is a Poisson process.

Proof Let the sets B, n ∈ N, be as in Definition 6.4 and assume without loss of generality that B ⊂ Bn+1. Suppose for each n ∈ N that ηB is a Poisson process. Then it follows from Theorem 3.9 and monotone convergence that η is a Poisson process. Hence we can assume that P(η(X) &lt; ∞) = 1. Furthermore, we can (and do) assume X = R and η(R \ [0, 1]) = 0, cf. the proof of Theorem 6.11.

For t ∈ R set f(t) := P(η((−∞, t]) = 0), which is clearly non-increasing. Clearly f(−1) = 1. Suppose f(1) = 0. Let t0 := inf{t ∈ R : f(t) = 0}. By continuity of P, (6.11) and the assumption P(η(R) &lt; ∞) = 1, we have P(η((t0 − 1/n, t0 + 1/n)) = 0) → 1 as n → ∞. Hence we can choose n with

$$c \colon = \mathbb { P } ( \eta ( ( t _ { 0 } - 1 / n , t _ { 0 } + 1 / n ] ) = 0 ) > 0 .$$

Then by our assumption we have

$$f ( t _ { 0 } + 1 / n ) = c f ( t _ { 0 } - 1 / n ) > 0$$

which is a contradiction, so f(1) &gt; 0.

Define

$$\lambda ( B ) \colon = - \log \mathbb { P } ( \eta ( B ) = 0 ) , \quad B \in \mathcal { B } ( \mathbb { R } ) .$$

Then λ(0) = 0 and λ(R) &lt; ∞. We show that λ is a measure. By our assumption λ is additive and hence also finitely additive. Let C, n ∈ N, be an increasing sequence of Borel sets with union C. Then the events {η(C) = 0} are decreasing and have intersection {η(C) = 0}. Therefore λ(C) → λ(C) as n → ∞, showing that λ is indeed a measure. Furthermore, (6.11) implies for any x ∈ R that λ{x} = − log P(η{x} = 0) = 0, so that λ is diffuse. Now we can apply Rényi's theorem (Theorem 6.10) to conclude that η is a Poisson process. □

### 6.4 Completely Orthogonal Point Processes

For simple point processes satisfying (4.30) the assumptions of Proposition 4.12can be relaxed as follows.

Theorem 6.13 Suppose that η and η′ are simple point processes on X


<!-- p:64 -->


such that, for each m ∈ N and each collection B1, . . . , Bm of pairwise disjoint measurable sets,

$$\mathbb { E } [ \eta ( B _ { 1 } ) \cdots \eta ( B _ { m } ) ] = \mathbb { E } [ \eta ^ { \prime } ( B _ { 1 } ) \cdots \eta ^ { \prime } ( B _ { m } ) ] .$$

Suppose also that the factorial moment measures of η satisfy (4.30). Then η = η'.

Proof As in the proof of Theorem 6.12 we can assume that X = R.

We wish to apply Proposition 4.12. Let m ∈ N with m ≥ 2 and let

$$D _ { m } \colon = \{ ( x _ { 1 } , \dots , x _ { m } ) \in \mathbb { X } ^ { m } \, \colon \, \text {there exist } i < j \text { with } x _ { i } = x _ { j } \}$$

denote the generalised diagonal in Xm. Let H be the class of all Borel sets in R" which are either of the form B1 × · . · × Bm with the B1, . . . , Bm Borel and pairwise disjoint, or are contained in the generalised diagonal Dm. Then H is a π-system and the m-th factorial moment measure of η agrees with that of η' on all sets in H. Indeed, this is true by assumption for the first kind of set in H, and by Exercise 6.9 and our assumption both factorial moment measures are zero on the diagonal D. Then by Theorem A.5 and Proposition 4.12 we are done if we can show that H generates the product σ-field B(R)n = B(R"); see Lemma A.24. The latter is generated by all sets of the form B1 × · · · × B, where B1, . . . , B are open intervals. Let us fix such intervals. For all n ∈ N and j ∈ Z let In,j := ((j − 1)/n, j/n]. Define

$$J _ { n , i } \colon = \{ j \in \mathbb { Z } \, \colon I _ { n , j } \subset B _ { i } \} , \ \ i \in \{ 1 , \dots , m \} ,$$

and Jn := Jn,1 × · · · × Jn,m. Let ∆ denote the generalised diagonal in Zm. We leave it to the reader to check that

$$B _ { 1 } \times \cdots \times B _ { m } \ \ D _ { m } = \bigcup _ { n = 1 } ^ { \infty } \bigcup _ { ( i _ { 1 } , \dots , i _ { m } ) \in J _ { n } \ \Delta _ { m } } I _ { n , i _ { 1 } } \times \cdots \times I _ { n , i _ { m } } .$$

It therefore follows that B1 × · . · × B ∈ σ(H), finishing the proof.

□

Wee o s    od   rt as elt

$$\mathbb { E } [ \eta ( B _ { 1 } ) \cdots \eta ( B _ { m } ) ] = \prod _ { j = 1 } ^ { m } \mathbb { E } [ \eta ( B _ { j } ) ]$$

for all m ∈ N and all pairwise disjoint B1, . . . , Bm ∈ X.

Theorem 6.13 implies the following characterisation of simple Poisson processes.


<!-- p:65 -->


Theorem 6.14 Let η be a simple, completely orthogonal point process on X with a σ-inite diffuse intensity measure λ. Then η is a Poisson process.

Proof Let η' be a Poisson process with intensity measure λ. Proposition 6.9 shows that η' is simple. Corollary 4.10, (4.6) and assumption (6.15) show that the hypothesis (6.13) of Theorem 6.13 is satisfied. It remains to note that η' satisfies (4.30). □

### 6.5 Turning Distributional into Almost Sure Identities

In this section we prove a converse of Theorem 5.6. Consider a Poisson process ξ on X × Y with intensity measure λξ, where (X, X) and (Y, Y) are Borel subspaces of a CSMS. Assuming that λ := λξ(· × Y) is σ-finite, we can apply Theorem A.14 to obtain λξ = λ ø K, where K is a probability kernel from X to Y. Since ξ(· × Y) is a Poisson process with intensity measure λ (Theorem 5.1), Theorem 5.6 shows that ξ has the same distribution as a K-marking of ξ(· × Y). Moreover, if λ is locally finite, then it turns out that the second coordinates of the points of ξ have the conditional independence properties of Definition 5.3.

First we refine Proposition 6.3 in a special case. Let N* be the measurable set of all μ ∈ N(X × Y) with μ(· × Y) ∈ Nls(X); see Definition 6.6.

Lemma 6.15 There is a measurable mapping T : X × N* → Y such that

$$\mu = \sum _ { n = 1 } ^ { \bar { \mu } ( K ) } \delta _ { ( \pi _ { n } ( \bar { \mu } ) , T ( \pi _ { n } ( \bar { \mu } ) , \mu ) ) } , \quad \mu \in N ^ { * } ,$$

where μ := μ(· × Y).

Proof Let μ ∈ N*. If μ{x} = 0 we set T(x, μ) := y0 for some fixed value y0 ∈ Y. If μ{x} &gt; 0 then ν := μ({x} × ·) is an integer-valued measure on Y with v(X) = 1. By Proposition 6.2 there exists a unique y ∈ Y such that v{y} = 1, so that we can define T(x, μ) := y. Then (6.16) holds.

It remains to show that the mapping T is measurable. Let C ∈ Y. Then we have for all (x, μ) ∈ X ×N* that

$$1 \{ T ( x , \mu ) \in C \} = 1 \{ \bar { \mu } \{ x \} = 0 , y _ { 0 } \in C \} + 1 \{ \mu ( \{ x \} \times C ) > 0 \} .$$

Since X × Y is a Borel subspace of a CSMS, it follows from Proposition 6.3 that (x, μ) → (1{ ̄{x} = 0}, 1{μ({x} × C) &gt; 0}) is measurable. This shows that T is measurable. □

Proposition 6.16 Let ξ be a Poisson process on X × Y, where (X, X) and


<!-- p:66 -->


(Y, Y) are Borel subspaces of a CSMS. Suppose that the intensity measure of ξ is given by λøK, where λ is a locally finite diffuse measure on X and K is a probability kernel from X to Y. Then ξ is a K-marking of η := ξ(· × Y).

Proof Since λ is locally finite and diffuse, we can apply Proposition 6.9 to the Poisson process η to obtain P(ξ ∈ N*) = 1. It is then no restriction of generality to assume that ξ ∈ N* everywhere on Ω. By Lemma 6.15 we have the representation

$$\xi = \sum _ { n = 1 } ^ { \kappa } \delta _ { ( X _ { n } , Y _ { n } ) } ,$$

where κ := ξ(X × Y), and for each n ∈ N, Xn := πn(ξ), Yn := T(Xn, ξ). (Recall that ξ = ξ(· × Y).) We wish to show that the sequence (Y) has the properties required in Definition 5.3. Since κ has a Poisson distribution, we N  u   = (∞ = tt t t y n  { }  (∞ = t ) k ∈ {1, . . . , n}, A ∈ Xn and B1, . . . , Bk ∈ Y. Set B := B1 × · . × Bk and

$$C & \coloneqq \{ ( ( x _ { 1 } , y _ { 1 } ) , \dots , ( x _ { n } , y _ { n } ) ) \in ( \mathbb { X } \times \mathbb { Y } ) ^ { n } \colon ( x _ { 1 } , \dots , x _ { n } ) \in A , ( y _ { 1 } , \dots , y _ { k } ) \in B \} . \\ \text {Then}$$

$$\mathbb { P } ( ( X _ { 1 } , \dots , X _ { n } ) \in A , ( Y _ { 1 } , \dots , Y _ { k } ) \in B ) \\ = \mathbb { E } \left [ \int _ { C } g _ { n } ( x _ { 1 } , \dots , x _ { n } , \bar { \xi } ) \, \xi ^ { ( n ) } ( d ( ( x _ { 1 } , y _ { 1 } ) , \dots , ( x _ { n } , y _ { n } ) ) ) \right ] , \\ \intertext { w h o r } \mathbb { U } \left ( x _ { 1 } , \dots , x _ { n } \in \mathbb { Y } \text { and } x _ { n } \subset \mathbb { N } \right )$$

where, for x1, . . . , xn ∈ X and μ ∈ Nts,

$$g _ { n } ( x _ { 1 } , \dots , x _ { n } , \mu ) \colon = \mathbf 1 \{ \pi _ { 1 } ( \mu ) = x _ { 1 } , \dots , \pi _ { n } ( \mu ) = x _ { n } \} .$$

By the multivariate Mecke equation (Theorem 4.4) and the assumed form of the intensity measure of ξ, this equals

$$\mathbb { E } \left [ \int _ { A } g _ { n } ( x _ { 1 } , \dots , x _ { n } , \eta + \delta _ { x _ { 1 } } + \cdots + \delta _ { x _ { n } } ) \prod _ { i = 1 } ^ { k } K ( x _ { i } , B _ { i } ) \, \lambda ^ { n } ( d ( x _ { 1 } , \dots , x _ { n } ) ) \right ] .$$

By the multivariate Mecke identity for the Poisson process η, this comes to

$$\mathbb { E } \left [ 1 \{ ( X _ { 1 } , \dots , X _ { n } ) \in A \} \prod _ { i = 1 } ^ { k } K ( X _ { i } , B _ { i } ) \right ] .$$

Since n is arbitrary it follows from Theorem A.5 that

$$\mathbb { P } ( ( X _ { n } ) _ { n \geq 1 } \in \cdot , ( Y _ { 1 } , \dots , Y _ { k } ) \in B ) = \mathbb { E } \left [ 1 \{ ( X _ { n } ) _ { n \geq 1 } \in \cdot \} \prod _ { i = 1 } ^ { k } K ( X _ { i } , B _ { i } ) \right ] .$$


<!-- p:67 -->


Since k is arbitrary this implies the assertion.

Assume now that P(κ &lt; ∞) = 1 and let n ∈ N. Then, using similar notation to above (for the case k = n),

$$\mathbb { P } ( ( X _ { 1 } , \dots , X _ { n } ) \in A , ( Y _ { 1 } , \dots , Y _ { n } ) \in B , \eta ( \mathbb { K } ) = n )$$

where hn(x1, . . . , χn, μ) := 1{π1(μ) = x1, . . . , πn(μ) = χn, μ(X) = n}, and we can argue as above to conclude the proof. □

Exercise 6.12 shows that Proposition 6.16 remains true for possibly non-diffuse λ, provided that the underlying probability space supports a K-marking of ξ.

### 6.6 Exercises

Exercise 6.1 Suppose that X is a Borel subspace of a CSMS. Show that the mapping (x, μ) → μ{x} from X × N1(X) to N0 is B(X) ⊗ N1(X)- measurable. (Hint: Use Proposition 6.3.)

Exercise 6.2 Give an example to show that if the word "simple" is omitted from the hypothesis of Rényi's theorem, then the conclusion need not be true. (This can be done by taking a simple point process and modifying it to make it "complicated", i.e. not simple.)

Exercise 6.3 Give an example to show that if the word "diffuse" is omitted from the hypothesis of Rényi's theorem, then the conclusion need not be true. (This can be done by taking a "complicated" point process and modifying it to make it simple.)

Exercise 6.4 Let (X, X) be a Borel space. A measure λ on X is said to be purely discrete, if λ = Σi∈l cδxi, for some I ⊂ N, x ∈ X and ci &gt; 0. Let λ be a σ-finite measure on X and let A := {x ∈ X : λ{x} = 0}. Show that λA is diffuse and that λx\A is purely discrete.

Exercise 6.5 Give an example to show that if we drop the assumption (6.11) from the conditions of Theorem 6.12, then we cannot always conclude that η is a Poisson process.

Exercise 6.6 Suppose that (X, X) is a Borel subspace of a CSMS. Define for each μ ∈ N1(X) the measure μ* ∈ Ns(X) by

$$\mu ^ { * } \coloneqq \int \mu \{ x \} ^ { \oplus } \mathbf 1 \{ x \in \cdot \} \, \mu ( d x ) ,$$


<!-- p:68 -->


where a® := 1{a ≠ 0}a−1 is the generalised inverse of a ∈ R. Prove that the mapping μ → μ* from N1(X) to N1(X) is measurable. Prove also that the system of all sets {μ ∈ N(X) : μ(B) = 0}, where B is a bounded Borel set, is a π-system generating the σ-field

$$\mathcal { N } ^ { * } = \{ \{ \mu \in N _ { l } ( \mathbb { X } ) \colon \mu ^ { * } \in A \} \, \colon A \in \mathcal { N } _ { l } ( \mathbb { X } ) \} .$$

(Hint: Check the proof of Theorem 6.11.)

Exercise 6.7 Suppose that (X, X) is a Borel subspace of a CSMS. Recall from Definition 6.6 the notation Nls(X) = N1(X) ∩ Ns(X) and let

$$\mathcal { N } _ { l s } ( \mathbb { X } ) \colon = \{ A \cap N _ { l s } ( \mathbb { X } ) \, \colon A \in \mathcal { N } ( \mathbb { X } ) \} .$$

Show that the system of all sets {μ ∈ Nts(X) : μ(B) = 0}, where B is a bounded Borel set, is a π-system generating Nls(X).

Exercise 6.8 Let η and η' be point processes on an arbitrary measurable space (X, X). Assume that there are B ∈ X, n ∈ N, such that ∪x=1B = X and such that (6.3) holds for both η and η'. Prove that η ≡ η′ if and only if ηBn = ηBn for each n ∈ N.

Exercise 6.9 Let (X, X) be a Borel space, μ ∈ Ns(X) and m ∈ N with m ≥ 2. Show that μ(m)(Dm) = 0, where the generalised diagonal Dm is given by (6.14). Why is Dm a measurable set? (Hint: Use Proposition 6.2 and (4.5).)

Exercise 6.10 Let ν be the measure on [0, 1] defined by v(B) = 0 if λ1(B) = 0 and v(B) = ∞ otherwise. (Here λ1 denotes Lebesgue measure.) Show that v is s-finite but does not belong to N([0, 1]). (Hint: To prove the second assertion you can use the fact that each μ ∈ N([0, 1]) is an at most countably infinite sum of Dirac measures.)

Exercise 6.11 (Uniform randomisation) Let η be a proper Poisson process on a Borel space (X, X) and let ξ be an independent λ1-marking of η, where λ1 is Lebesgue measure on [0, 1]. Show that the Mecke identity for η can be derived from that for ξ.

Exercise 6.12 Suppose the assumptions of Proposition 6.16 are all satisfied except for the assumption that λ is diffuse. Assume that the probability space supports uniform randomisation of ξ (see Exercise 6.11) and show that then the assertion of Proposition 6.16 remains valid.


<!-- p:69 -->


## Poisson Processes on the Real Line

A Poisson process on the real half-line is said to be homogeneous if its intensity measure is a multiple of Lebesgue measure. Such a process is characterised by the fact that the distances between consecutive points are independent and identically exponentially distributed. Using conditional distributions this result can be generalised to position-dependent markings of non-homogeneous Poisson processes. An interesting example of a nonhomogeneous Poisson process is given by the consecutive record values in a sequence of independent and identically distributed non-negative random variables.

### 7.1 The Interval Theorem

In this chapter we study point processes on the real half-line R+ := [0, ∞). We shall consider point processes that are simple with at most one accumulation point of their atoms.

Given a measure μ on R+ (or on R) and an interval I ⊂ R+ (resp. I ⊂ R), we shall write μI := μ(I). For μ ∈ N(R+) set

$$T _ { n } ( \mu ) \colon = \inf \{ t \geq 0 \, \colon \mu [ 0 , t ] \geq n \} , \quad n \in \overline { \mathbb { N } } ,$$

where inf ∅ := ∞,  ̄ := N ∪ {∞} and where we interpret μ[0, t] ≥ ∞ as μ[0, t] = ∞. Let N+ be the space of all measures μ ∈ N(R+) such that μ[T∞(μ), ∞) = 0 and Tn(μ) &lt; Tn+1(μ) for all n ∈ N such that Tn(μ) &lt; ∞. In Exercise 7.1 the reader is asked to show that N+ ∈ N(R+).

Definition 7.1 We say that a point process η on R+ is ordinary if it satisfies P(η ∈ N+) = 1.

If η is an ordinary point process we can almost surely write

$$\eta = \sum _ { n = 1 } ^ { \infty } 1 \{ T _ { n } < \infty \} \delta _ { T _ { n } } ,$$


<!-- p:70 -->


where Tn := T(η) for n ∈ N. Sometimes Tn is called n-th arrival time of η. In the case Tn = ∞ the measure 1{Tn &lt; ∞}δτ is interpreted as the zero measure on R+. If T &lt; ∞ we say that explosion occurs.

An important example of an ordinary point process is a homogeneous Poisson process of rate (or intensity) γ &gt; 0. This is a Poisson process on R+ with intensity measure γλ+, where λ+ is Lebesgue measure on R+. (More generally, for d ∈ N and B ∈ B(Rd), a homogeneous Poisson process on B is a Poisson process η on B whose intensity measure is a multiple of Lebesgue measure on B. This multiple is called the intensity of η.) Given B ⊂ R and t ∈ R we set B + t := {s + t : s ∈ B}. A point process η on R+ is said to be stationary if

$$\theta _ { t } ^ { + } \eta \stackrel { d } { = } \eta , \ \ t \in \mathbb { R } _ { + } ,$$

where, for any measure μ on R+ and t ∈ R+, the measure θ+μ on R+ is defined by

$$\theta _ { t } ^ { + } \mu ( B ) \colon = \mu ( B + t ) , \ \ B \in \mathcal { B } ( \mathbb { R } _ { + } ) .$$

Any homogeneous Poisson process on R+ is stationary.

Our first aim in this chapter is to characterise homogeneous Poisson processes in terms of the inter-point distances T – T-1, where T0 := 0.

Theorem 7.2 (Interval theorem) Let η be a point process on R+. Then η is a homogeneous Poisson process with rate γ &gt; 0 if and only if the T − Tn−1, n ≥ 1, are independent and exponentially distributed with parameter γ.

Proof Suppose first that η is a Poisson process as stated. Let n ∈ N. Since η is locally finite we have

$$\{ T _ { n } \leq t \} = \{ \eta [ 0 , t ] \geq n \} , \quad \mathbb { P } \text {-a.s., } t \in \mathbb { R } _ { + } .$$

Since P(η(R+) = ∞) = 1 we have P(Tn &lt; ∞) = 1. Let f ∈ R+(Rn). Then

$$\mathbb { E } [ f ( T _ { 1 } , T _ { 2 } - T _ { 1 } , \dots , T _ { n } - T _ { n - 1 } ) ] = \mathbb { E } \left [ \int \mathbf 1 \{ t _ { 1 } < \cdots < t _ { n } \}$$

$$\times f ( t _ { 1 } , t _ { 2 } - t _ { 1 } , \dots , t _ { n } - t _ { n - 1 } ) \mathbf 1 \{ \eta [ 0 , t _ { n } ) = n - 1 \} \, \eta ^ { ( n ) } ( d ( t _ { 1 } , \dots , t _ { n } ) ) ] .$$

Now we use the multivariate Mecke theorem (Theorem 4.4). Since, for u4 &gt; . . · &gt; 11 7 0

$$\{ ( \eta + \delta _ { t _ { 1 } } + \cdots + \delta _ { t _ { n } } ) [ 0 , t _ { n } ) = n - 1 \} = \{ \eta [ 0 , t _ { n } ) = 0 \} ,$$

the right-hand side of (7.4) equals

$$\gamma ^ { n } \int \mathbf 1 \{ 0 < t _ { 1 } < \cdots < t _ { n } \} f ( t _ { 1 } , t _ { 2 } - t _ { 1 } , \dots , t _ { n } - t _ { n - 1 } ) \exp [ - \gamma t _ { n } ] \, d ( t _ { 1 } , \dots , t _ { n } ) ,$$


<!-- p:71 -->


where the integration is with respect to Lebesgue measure on R". After the change of variables s1 := t1, s2 := t2 − t1, . . . , sn := tn − tn−1 this yields

$$\mathbb { E } [ f ( T _ { 1 } , T _ { 2 } - T _ { 1 } , \dots , T _ { n } - T _ { n - 1 } ) ] \\ = \int _ { 0 } ^ { \infty } \dots \int _ { 0 } ^ { \infty } f ( s _ { 1 } , \dots , s _ { n } ) \gamma ^ { n } \exp [ - \gamma ( s _ { 1 } + \cdots + s _ { n } ) ] \, d s _ { 1 } \cdots d s _ { n } .$$

Therefore T1, T2 − T1, . . . , T − T-1 are independent and exponentially distributed with parameter γ. Since n ∈ N is arbitrary, the asserted properties of the sequence (T) follow.

Suppose, conversely, that (T) has the stated properties. Let η' be a homogeneous Poisson process of intensity γ &gt; 0. Then η′ has a representation as in (7.1) with random variables T′ instead of T. We have just proved that (Tn) = (Tn). Since, for any B ∈ B(R+),

$$\eta ( B ) = \sum _ { n = 1 } ^ { \infty } 1 \{ T _ { n } \in B \}$$

is a measurable function of the sequence (Tn), we can use Proposition2.10 ((ii) implies (i)) to conclude that η = η′ and hence η is a homogeneous Poisson process. □

A Poisson process on R+ whose intensity measure is not a multiple of λ+ is said to be non-homogeneous. Such a process can be constructed from a homogeneous Poisson process by a suitable time transform. This procedure is a special case of the mapping theorem (Theorem 5.1). Let v be a locally finite measure on R+ and define a function v← : R+ → [0, ∞] by

$$\nu ^ { \leftarrow } ( t ) \colon = \inf \{ s \geq 0 \, \colon \nu [ 0 , s ] \geq t \} , \ \ t \geq 0 ,$$

where inf Ø := ∞. This function is increasing, left-continuous and, in particular, measurable.

Proposition 7.3 Let v be a locally finite measure on R+, let η be a homogeneous Poisson process on R+ with rate 1 and let (T) be given by (7.1). Then

$$\eta ^ { \prime } \colon = \sum _ { n = 1 } ^ { \infty } \mathbf 1 \{ \nu ^ { \leftarrow } ( T _ { n } ) < \infty \} \delta _ { \nu ^ { \leftarrow } ( T _ { n } ) }$$

is a Poisson process on R+ with intensity measure v.

Proof By the mapping theorem (Theorem 5.1) Σn=1 δv-(Tn) is a Poisson process on R with intensity measure


<!-- p:72 -->


$$\lambda = \int \{ \nu ^ { \leftarrow } ( t ) \in \cdot \} \, d t .$$

Proposition A.31 shows that λ = v (on R+), and the assertion follows.

### 7.2 Marked Poisson Processes

In this section we consider Poisson processes on R+ × Y, where (Y, Y) (the mark space) is a Borel space. Let N+(Y) be the space of all μ ∈ N(R+ × Y) such that μ(· × Y) ∈ N+. Exercise 7.4 shows that there are measurable mappings T′ : N+(Y) → [0, ∞], n ∈ N, and Y′ : N+(Y) → Y, such that Tn ≤ Tn+1 for each n ∈ N and

$$\mu = \sum _ { n = 1 } ^ { \infty } 1 \{ T _ { n } ^ { \prime } ( \mu ) < \infty \} \delta _ { ( T _ { n } ^ { \prime } ( \mu ) , Y _ { n } ^ { \prime } ( \mu ) ) } , \quad \mu \in N ^ { + } ( \mathbb { Y } ) .$$

Let ξ be a point process on R+ ×Y such that η := ξ(· × Y) is ordinary. By (7.7) we have almost surely that

$$\xi = \sum _ { n = 1 } ^ { \infty } 1 \{ T _ { n } < \infty \} \delta _ { ( T _ { n } , Y _ { n } ) } ,$$

where T := T(η), n ∈ N, and where the Y are random elements of Y such that almost surely ξ{(Tn, Yn)} = 1 for Tn &lt; ∞.

If ξ is a Poisson process, then our next result (Theorem 7.4) provides a formula for the distribution of (T1, Y1, . . . , T, Y) in terms of the intensity measure of ξ. Corollary 7.5 will then extend Theorem 7.2 by allowing both for marks and for non-homogeneity of the Poisson process.

Given a measure μ on R+ ×Y and given t ≥ 0, we define another measure θ+μ on R+ × Y by

$$\vartheta _ { t } ^ { + } \mu ( B ) \coloneqq \int \mathbf 1 \{ ( s - t , y ) \in B \} \mu ( d ( s , y ) ) , \quad B \in \mathcal { B } ( \mathbb { R } _ { + } ) \otimes \mathcal { Y } .$$

This definition generalises (7.2). If μ ∈ N+(Y) then (7.7) implies that

$$\vartheta _ { t } ^ { + } \mu = \sum _ { n = 1 } ^ { \infty } \mathbf 1 \{ t \leq T _ { n } ^ { \prime } ( \mu ) < \infty \} \delta _ { ( T _ { n } ^ { \prime } ( \mu ) - t , Y _ { n } ^ { \prime } ( \mu ) ) } , \quad \mu \in N ^ { + } ( \mathbb { Y } ) .$$

This shows that (t, μ) ↔ θ+μ is measurable on R+ × N+(Y). Indeed, for each n ∈ N and each B ∈ B(R+) ⊗ y the expression δ(T′(μ)−t,Y(μ))(B) is a measurable function of (t, μ).


<!-- p:73 -->


Theorem 7.4 (Memoryless property) Suppose that ξ is a Poisson process on R+×Y with a σ-finite intensity measure λ such that P(ξ(· ×Y) ∈ N+) = 1. For n ∈ N let Tn := T(η), where η := ξ(· × Y). Let the sequence (Yn) be as in (7.8). Then the following hold for all n ∈ N.

- (i) For any f ∈ R+((R+ × Y)n),

$$\mathbb { E } [ 1 \{ T _ { n } < \infty \} f ( T _ { 1 } , Y _ { 1 } , \dots , T _ { n } , Y _ { n } ) ] & = \int 1 \{ 0 < t _ { 1 } < \cdots < t _ { n } \} \\ & \times f ( t _ { 1 } , y _ { 1 } , \dots , t _ { n } , y _ { n } ) \exp [ - \lambda ( ( 0 , t _ { n } ] \times \mathbb { Y } ) ] \, \lambda ^ { n } ( d ( t _ { 1 } , y _ { 1 } , \dots , t _ { n } , y _ { n } ) ) .$$

- (ii) The conditional distribution of θ+nξ given (T1, Y1, . . . , Tn, Yn) and Tn &lt; ∞ is almost surely that of a Poisson process with intensity measure θtλ.

Proof We interpret ξ as a random element of the space N+(Y) introduced at the beginning of this section. The assumptions and Proposition 6.9 imply that the measure λ(·×Y) is diffuse. We now use the same idea as in the proof of Theorem 7.2. Let f be as in (i) and let g ∈ R+(N+(Y)). Then

$$\mathbb { E } [ \{ T _ { n } < \infty \} f ( T _ { 1 } , Y _ { 1 } , \dots , T _ { n } , Y _ { n } ) g ( \vartheta _ { T _ { n } } ^ { + } \xi ) ] & = \mathbb { E } [ \int \mathbf 1 \{ t _ { 1 } < \dots < t _ { n } \} \\ & \times f ( t _ { 1 } , y _ { 1 } , \dots , t _ { n } , y _ { n } ) g ( \vartheta _ { t _ { n } } ^ { + } \xi ) \mathbf 1 \{ \eta [ 0 , t _ { n } ) = n - 1 \} \xi ^ { ( n ) } ( d ( t _ { 1 } , y _ { 1 } , \dots , t _ { n } , y _ { n } ) ) ] .$$

By the Mecke equation this equals

$$\int & 1 \{ t _ { 1 } < \cdots < t _ { n } \} f ( t _ { 1 } , y _ { 1 } , \dots , t _ { n } , y _ { n } ) \\ & \quad \times \mathbb { E } [ g ( \vartheta _ { t _ { n } } ^ { + } \xi ) 1 \{ \eta [ 0 , t _ { n } ) = 0 \} ] \, \lambda ^ { n } ( d ( t _ { 1 } , y _ { 1 } , \dots , t _ { n } , y _ { n } ) ) .$$

By Theorem 5.2, 1{η[0, t) = 0} and g(θ+ ξ) are independent for any fixed tn. Moreover, θ+ ξ is a Poisson process with intensity measure θ+ λ. Therefore we obtain both (i) and (ii). □

If, in the situation of Theorem 7.4, λ(R+ × Y) &lt; ∞, then ξ has only finitely many points and Tn = ∞ for n &gt; ξ(R+ × Y). In fact, the theorem shows that, P-a.s. on the event {Tn &lt; ∞},

$$\mathbb { P } ( T _ { n + 1 } = \infty \, | \, T _ { 0 } , Y _ { 0 } , \dots , T _ { n } , Y _ { n } ) = \exp [ - \lambda ( [ T _ { n } , \infty ) \times \mathbb { Y } ) ] .$$

If v, v' are measures on a measurable space (X, X) and f ∈ R+(X), we write v′(dx) = f(x) v(dx) if f is a density of v' with respect to ν, that is v′(B) = v(1Bf) for all B ∈ X.


<!-- p:74 -->


Corollary 7.5 Under the hypotheses of Theorem 7.4, we have for every n ∈ Nthat

$$& \{ t < \infty \} \mathbb { P } ( ( T _ { n } , Y _ { n } ) \in d ( t , y ) \, | \, T _ { 0 } , Y _ { 0 } , \dots , T _ { n - 1 } , Y _ { n - 1 } ) \\ & \quad = \mathbf 1 \{ T _ { n - 1 } < t \} \exp [ - \lambda ( [ T _ { n - 1 } , t ] \times \mathbb { Y } ) ] \lambda ( d ( t , y ) ) , \quad \mathbb { P } \text {-a.s. on } \{ T _ { n - 1 } < \infty \} ,$$

where T0 = 0 and Y0 is chosen as a constant function.

Proof The result is an immediate consequence of Theorem 7.4 and the definition of conditional distributions given in Section B.4. □

Independent markings of homogeneous Poisson processes can be characterised as follows.

Theorem 7.6 Let the point process ξ on R+ × Y be given by (7.8) and define η by (7.1). Let γ &gt; 0 and let Q be a probability measure on Y. Then ξ is an independent Q-marking of a homogeneous Poisson process with rate γ &gt; 0 if and only if T1, Y1, T2 − T1, Y2, . . . are independent, the Tn − T-1 have an exponential distribution with parameter γ and the Yn have distribution Q.

Proof If η is a homogeneous Poisson process and ξ is an independent Qmarking of η, then by Theorem 5.6, ξ is a Poisson process with intensity measure γλ+ ⊗Q. Hence the properties of the sequence ((T, Y))≥1 follow from Corollary 7.5 (or from Theorem 7.4). The converse is an immediate consequence of the interval theorem (Theorem 7.2). □

### 7.3 Record Processes

Here we discuss how non-homogeneous Poisson processes describe the occurrence of record levels in a sequence X1, X2, . . . of independent random variables with values in R+ and common distribution Q. Let N1 := 1 be the first record time and R1 := X1 the first record. The further record times N2, N3, . . . are defined inductively by

$$N _ { k + 1 } \colon = \inf \{ n > N _ { k } \colon X _ { n } > X _ { N _ { k } } \} , \quad k \in \mathbb { N } ,$$

where inf ∅ := ∞. The k-th record level is Rk := XNk. We consider the following point process on R+ × N:

$$\chi \colon = \sum _ { n = 1 } ^ { \infty } 1 \{ N _ { n + 1 } < \infty \} \delta _ { ( R _ { n } , N _ { n + 1 } - N _ { n } ) } .$$


<!-- p:75 -->


Proposition 7.7 Let Q be a diffuse probability measure on R+ and let (Xn)n≥1 be a sequence of independent R+-valued random variables with common distribution Q. Then the point process X on R+ × N defined by (7.9) is a Poisson process whose intensity measure λ is given by

$$\lambda ( d t \times \{ k \} ) = \mathbb { Q } ( 0 , t ] ^ { k - 1 } \mathbb { Q } ( d t ) , \ \ k \in \mathbb { N } .$$

Proof Let n ∈ N, k1, . . . , kn ∈ N and f ∈ R+ (Rn). We assert that

$$\mathbb { E } [ 1 \{ N _ { 2 } - N _ { 1 } = k _ { 1 } , \dots , N _ { n + 1 } - N _ { n } = k _ { n } \} f ( R _ { 1 } , \dots , R _ { n } ) ] \\ = \int 1 \{ t _ { 1 } < \cdots < t _ { n } \} f ( t _ { 1 } , \dots , t _ { n } ) \\ \times \mathbb { Q } [ 0 , t _ { 1 } ] ^ { k _ { 1 } - 1 } \cdots \mathbb { Q } [ 0 , t _ { n } ] ^ { k _ { n } - 1 } \mathbb { Q } ( t _ { n } , \infty ) \mathbb { Q } ^ { n } ( d ( t _ { 1 } , \dots , t _ { n } ) ) .$$

To prove this let A denote the event inside the indicator in the left-hand side of (7.10). Set Y1 := X1 and Yi := X1+k1++ki-1 for 2 ≤ i ≤ n, and let B := {Y1 &lt; · . · &lt; Yn}. Then the left-hand side of (7.10) equals

$$\mathbb { E } [ \mathbf 1 _ { A } \mathbf 1 _ { B } f ( Y _ { 1 } , \dots , Y _ { n } ) ] = \mathbb { E } [ f ( Y _ { 1 } , \dots , Y _ { n } ) \mathbf 1 _ { B } \mathbb { P } ( A \ | \ Y _ { 1 } , \dots , Y _ { n } ) ] ,$$

where the identity follows from independence and Fubini's theorem (or, equivalently, by conditioning on Y1, ... , Y). This equals the right-hand side of (7.10).

Effectively, the range of integration in (7.10) can be restricted to t &lt; t∞, where

$$t _ { \infty } \colon = \sup \{ t \in \mathbb { R } _ { + } \colon \mathbb { Q } [ 0 , t ] < 1 \} .$$

Indeed, since Q is diffuse, we have Q[t∞, ∞) = 0. Summing in (7.10) over k1, . . . , kn ∈ N, we obtain

$$\mathbb { E } [ 1 \{ N _ { n + 1 } < \infty \} f ( R _ { 1 } , \dots , R _ { n } ) ] \\ = \int 1 \{ t _ { 1 } < \cdots < t _ { n } \} f ( t _ { 1 } , \dots , t _ { n } ) \\ \times \mathbb { Q } ( t _ { 1 } , \infty ) ^ { - 1 } \cdots \mathbb { Q } ( t _ { n - 1 } , \infty ) ^ { - 1 } \, \mathbb { Q } ^ { n } ( d ( t _ { 1 } , \dots , t _ { n } ) ) .$$

Taking f ≡ 1 and performing the integration yields P(Nn+1 &lt; ∞) = 1. Next we note that

$$\lambda ( d t \times \mathbb { N } ) = ( \mathbb { Q } [ t , \infty ) ) ^ { \oplus } \mathbb { Q } ( d t )$$

is the hazard measure of Q, where a® := 1{a ≠ 0}a−1 is the generalised inverse of a ∈ R. Therefore by Proposition A.32

$$\mathbb { Q } [ t , \infty ) = \exp [ - \lambda ( [ 0 , t ] \times \mathbb { N } ) ] .$$


<!-- p:76 -->


Hence we obtain, for all n ∈ N and g ∈ R+((R+ × N)n), from (7.10) that

$$\mathbb { E } [ g ( R _ { 1 } , N _ { 2 } - N _ { 1 } , \dots , R _ { n } , N _ { n + 1 } - N _ { n } ) ] \\ = & \int \{ t _ { 1 } < \cdots < t _ { n } \} g ( t _ { 1 } , k _ { 1 } , \dots , t _ { n } , k _ { n } ) \\ & \times \exp [ - \lambda ( [ 0 , t _ { n } ] \times \mathbb { N } ) ] \, \lambda ^ { n } ( d ( t _ { 1 } , k _ { 1 } , \dots , t _ { n } , k _ { n } ) ) .$$

Now let ξ be a Poisson process as in Theorem 7.4 (with Y = N) with intensity measure λ. The identity (7.12) implies that λ([0, ∞) × N) = ∞, so that P(Tn &lt; ∞) = 1 holds for all n ∈ N. Comparing (7.13) and Theorem 7.4(i) yields

$$( R _ { 1 } , N _ { 2 } - N _ { 1 } , \dots , R _ { n } , N _ { n + 1 } - N _ { n } ) \stackrel { d } { = } ( T _ { 1 } , Y _ { 1 } , \dots , T _ { n } , Y _ { n } ) , \quad n \in \mathbb { N } .$$

As in the final part of the proof of Theorem 7.2 we obtain ξ ≡ χ and hence the assertion of the theorem. □

Proposition 7.7, (7.11) and the mapping theorem (Theorem 5.1) together show that the point process χ(· × N) of successive record levels is a Poisson process with the hazard measure of Q as intensity measure. Further consequences of the proposition are discussed in Exercise 7.14.

### 7.4 Polar Representation of Homogeneous Poisson Processes

In this section we discuss how Poisson processes on R+ naturally show up in a spatial setting. For d ∈ N let va–1 denote the uniform distribution on the unit sphere Sd-1 := {x ∈ Rd : ∥|x|| = 1}, where ∥ · ∥ denotes the Euclidean norm on Rd. This normalised spherical Lebesgue measure on Sd-1 is the probability measure defined by

$$\nu _ { d - 1 } ( C ) \coloneqq \kappa _ { d } ^ { - 1 } \int _ { B ^ { d } } \mathfrak { 1 } \{ x / | | x | | \in C \} \, d x , \quad C \in \mathcal { B } ( \mathbb { S } ^ { d - 1 } ) ,$$

where Bd := {x ∈ Rd : ∥x∥| ≤ 1} is the unit ball and κd := λd(Bd) is its volume. For x = 0 we let x/||x|| equal some fixed point in Sd-1.

Proposition 7.8 Let ζ be a homogeneous Poisson process on Rd with intensity γ &gt; 0. Then the point process ξ on Rd × Sd-1 defined by

$$\xi ( A ) \colon = \int \{ 1 \{ ( \kappa _ { d } \| x \| ^ { d } , x / \| x \| ) \in A \} \, \zeta ( d x ) , \quad A \in \mathcal { B } ( \mathbb { R } _ { + } \times \mathbb { S } ^ { d - 1 } ) ,$$

is an independent vd-1-marking of a homogeneous Poisson process with intensity γ.


<!-- p:77 -->


Proof By Theorem 5.1 (mapping theorem) and Proposition 6.16 it is sufficient to show for each A ∈ B(R+ × Sd-1) that

$$\mathbb { E } [ \xi ( A ) ] = \gamma \int _ { \mathbb { S } ^ { d - 1 } } \int _ { 0 } ^ { \infty } \mathbf 1 ( r , u ) \in A \} \, d r \, \nu _ { d - 1 } ( d u ) .$$

To this end, we need the polar representation of Lebesgue measure, which says that

$$\int _ { \ } g ( x ) \, d x = d \kappa _ { d } \int _ { \mathbb { S } ^ { d - 1 } } \int _ { 0 } ^ { \infty } r ^ { d - 1 } g ( r u ) \, d r \, \nu _ { d - 1 } ( d u ) ,$$

for all g ∈ R+(Rd). Indeed, if g(x) = 1{∥|x|| ≤ s, x/||x|| ∈ C}, for s ≥ 0 and C ∈ B(Sd-1), then (7.17) follows from definition (7.14) and the scaling properties of Lebesgue measure. Using first Campbell's formula for ζ and then (7.17) yields

$$\mathbb { B } [ \xi ( A ) ] & = \gamma \int 1 \{ ( \kappa _ { d } \| x \| ^ { d } , x / \| x \| ) \in A \} \, d x \\ & = \gamma d \kappa _ { d } \int _ { \mathbb { S } ^ { d - 1 } } \int _ { 0 } ^ { \infty } 1 \{ ( \kappa _ { d } r ^ { d } , u ) \in A \} r ^ { d - 1 } \, d r \, \nu _ { d - 1 } ( d u ) .$$

Hence (7.16) follows upon a change of variables.

□

Proposition 7.8 can be used along with the interval theorem (Theorem 7.2) to simulate the points of a homogeneous Poisson process in order of increasing distance from the origin.

### 7.5 Exercises

Exercise 7.1 Let μ ∈ N(R+) and define the function fμ ∈ R+(R+) as the right-continuous version of t → μ[0, t], that is

$$f _ { \mu } ( t ) \colon = \lim _ { s \downarrow t } \mu [ 0 , s ] , \ \ t \geq 0 .$$

(If μ is locally finite, then fμ(t) = μ[0, t].) Let n ∈ Ñ and t ∈ R+. Show that Tn(μ) ≤ t if and only if fμ(t) ≥ n. Show that this implies that the Tn are measurable mappings on N(R+) and that N+ (see Definition 7.1) is a measurable subset of N(R+).

Exercise 7.2 Let η be a Poisson process on R+ with intensity measure λ. Show that η is ordinary if and only if λ is diffuse and λ([λ←(∞), ∞)) = ∞, where λ←(∞) := inf{s ≥ 0 : γ[0, s] = ∞} and [∞, ∞) := ∅.


<!-- p:78 -->


Exercise 7.3 Let Tn be the n-th point of a homogeneous Poisson process η on R+with intensity γ. Use (7.3) to show that

$$\mathbb { P } ( T _ { n } \in d t ) = \frac { \gamma ^ { n } } { ( n - 1 ) ! } t ^ { n - 1 } e ^ { - \gamma t } \, d t .$$

This is a Gamma distribution with scale parameter γ and shape parameter n; see Section 1.4.

Exercise 7.4 Let (Y, Y) be a Borel space and let C ∈ y. Show that (t, μ) ↔ μ({t} × C) is a measurable mapping on R+ × N+(Y). Show also that there are measurable mappings Y'n : N+(Y) → Y, n ∈ N, such that (7.7) holds with T′(μ) := T(μ(· × Y)). (Hint: To prove the first assertion it suffices to show that (t, μ) → 1{t &lt; T∞(μ)}μ({t} × C) is measurable, which can be done by a limit procedure. Check the proof of Lemma 6.15 to see the second assertion.)

Exercise 7.5 Suppose that the hypotheses of Theorem 7.4 apply, and that there is a probability kernel J from R+ to (Y, Y) such that

$$\lambda ( d ( t , y ) ) = J ( t , d y ) \, \lambda ( d t \times \mathbb { Y } ) .$$

(By Theorem A.14 this is no restriction of generality.) Show for all n ∈ N that

$$\mathbb { P } ( Y _ { n } \in d y \, | \, T _ { 1 } , Y _ { 1 } , \dots , Y _ { n - 1 } , T _ { n } ) = J ( T _ { n } , d y ) , \quad \mathbb { P } \text {-a.s. on } \{ T _ { n } < \infty \} .$$

Exercise 7.6 Suppose that X is a Poisson distributed random variable and let k, i ∈ N with i ≤ k. Show that P(X ≥ k | X ≥ i) ≤ P(X ≥ k − i). (Hint: Use the interval theorem.)

Exercise 7.7 Let η be a homogeneous Poisson process of intensity γ &gt; 0. Prove that η[0, t]/t → γ as t → ∞. (Hint: Use the fact that η[0, n]/n satisfies a law of large numbers; see Theorem B.6.)

Exercise 7.8 Let η be a Poisson process on R+, whose intensity measure ν satisfies 0 &lt; v[0, t] &lt; ∞ for all sufficiently large t and v[0, ∞) = ∞. Use Exercise 7.7 to prove that

$$\lim _ { t \to \infty } \frac { \eta [ 0 , t ] } { \nu [ 0 , t ] } = 1 , \quad \mathbb { P } \text {-a.s.}$$

Exercise 7.9 Let η+ and η\_ be two independent homogeneous Poisson processes on R+ with intensity γ. Define a point process η on R by

$$\eta ( B ) \coloneqq \eta _ { + } ( B \cap \mathbb { R } _ { + } ) + \eta _ { - } ( B ^ { * } \cap \mathbb { R } _ { + } ) , \ \ B \in \mathcal { B } ^ { 1 } ,$$


<!-- p:79 -->


where B* := {−t : t ∈ B}. Show that η is a homogeneous Poisson process on R.

Exercise 7.10 Let η be a point process on R+ with intensity measure λ+ and let v be a locally finite measure on R+. Show that the point process η' defined by (7.6) has intensity measure v. (Hint: Use Theorem 5.1 and the properties of generalised inverses; see the proof of Proposition 7.3.)

Exercise 7.11 Show that Proposition 7.7 remains valid for a sequence (X)n≥1 of independent and identically distributed random elements of R+, provided that the distribution of X1is diffuse on R+.

Exercise 7.12 Let T be a random element of R+. Show that there is a Poisson process η on R+ such that T ≡ T1(η). (Hint: Use Exercise 7.11.)

Exercise 7.13 Suppose the assumptions of Proposition 7.7 hold. For n ∈ N let Mn := max{X1, . . . , X} (running maximum) and for t ∈ R+ let

$$L _ { t } = \int 1 \{ s \leq t \} k \chi ( d ( s , k ) ) .$$

Show that P-a.s. inf{n ∈ N : Mn &gt; t} = 1 + Lt, provided Q[0, t] &gt; 0. (Hence L, + 1 is the first time the running maximum exceeds the level t.)

Exercise 7.14 Suppose the assumptions of Proposition 7.7 hold and for t ∈ R+ define L, as in Exercise 7.13. Show that La and Lb − La are independent whenever 0 ≤ a &lt; b. Show also that

$$\mathbb { E } [ w ^ { L _ { b } - L _ { a } } ] = \frac { \mathbb { Q } ( b , \infty ) ( 1 - w \, \mathbb { Q } ( b , \infty ) ) } { \mathbb { Q } ( a , \infty ) ( 1 - w \, \mathbb { Q } ( a , \infty ) ) } , \quad w \in [ 0 , 1 ] ,$$

whenever Q[0, b] &lt; 1. Use this formula to prove that

$$\mathbb { P } ( L _ { b } - L _ { a } = n ) = \frac { \mathbb { Q } ( b , \infty ) } { \mathbb { Q } ( a , \infty ) } \mathbb { Q } ( a , b ) \mathbb { Q } ( b ) ^ { n - 1 } , \quad n \in \mathbb { N } .$$

(Hint: Use Theorem 3.9, Proposition A.31 and the logarithmic series to prove (7.18). Then compare the result with the probability generating function of the right-hand side of (7.19).)

Exercise 7.15 Let the assumptions of Proposition 7.7 hold. For j ∈ N let I j be the indicator of the event that X j is a record. Use a direct combinatorial argument to show that I1, I2, . . . are independent with P(Ij = 1) = 1/j.

Exercise 7.16 By setting g(x) := e−x|2/2 in (7.17), show that the volume of the unit ball Bd ⊂ Rd is given by κd = 2πd/2/Γ(1 + d/2), where the Gamma function Γ(·) is defined by (1.23).


<!-- p:80 -->


## Stationary Point Processes

A point process η on Rd is said to be stationary if it looks statistically the same from all sites of Ra. In this case the intensity measure is a multiple of Lebesgue measure. The reduced second factorial moment measure of a stationary point process can be used to express variances and covariances of point process integrals. Its density (when existing) is called the pair correlation function of η. A stationary point process is ergodic if its distribution is degenerate on translation invariant sets. In this case it satisfies a spatial ergodic theorem.

### 8.1 Stationarity

In this chapter we fix d ∈ N and consider point processes on the Euclidean space X = Rd. To distinguish between points of the point process and elements of Rd we call the latter sites. Stationarity is an important invariance concept in probability theory. Our aim here is to discuss a few basic properties of stationary point processes, using the Poisson process as illustration. Throughout the chapter we abbreviate (N, N) := (N(Rd), N(Rd)).

The formal definition of stationarity is based on the family of shifts θy : N → N, y ∈ Rd, defined by

$$\theta _ { y } \mu ( B ) \coloneqq \mu ( B + y ) , \ \mu \in \mathbb { N } , \ B \in \mathcal { B } ^ { d } ,$$

where B + y := {x + y : x ∈ B} and Bd := B(Rd) is the Borel σ-field on Rd. We write B − y := B + (−y). A good way to memorise (8.1) is the formula θyδy = δ0, where 0 is the origin in Rd. Definition (8.1) is equivalent to

$$\int g ( x ) \left ( \theta _ { y } \mu \right ) ( d x ) & = \int g ( x - y ) \mu ( d x ) , \quad \mu \in \mathbb { N } , \, g \in \mathbb { R } _ { + } ( \mathbb { R } ^ { d } ) .$$

We note that θ0 is the identity on N and the flow property θy  θx = θx+y for all x, y ∈ Rd. For any fixed y ∈ Rd, the mapping θy is measurable.


<!-- p:81 -->


Definition 8.1 A point process η on Rd is said to be stationary if θxη = η for all x ∈ Rd.

Let λd denote Lebesgue measure on Rd. Under a natural integrability as   r  s   n u  osie of λd.

Proposition 8.2 Let η be a stationary point process on Rd such that the quantity

$$\gamma \colon = \mathbb { E } [ \eta ( [ 0 , 1 ] ^ { d } ) ]$$

is finite. Then the intensity measure of η equals γλd.

Proof The stationarity of η implies that its intensity measure λ is translation invariant, that is λ(B + x) = λ(B) for all B ∈ Bd and all x ∈ Rd. Moreover, λ([0, 1]d) = γ &lt; ∞. It is a fundamental result from measure theory that γλa is the only measure with these two properties. □

The number γ given by (8.3) is called the intensity of η. Proposition 8.2 shows that a stationary point process with a finite intensity is locally finite. For a stationary Poisson process the intensity determines the distribution:

Proposition 8.3 Let η be a Poisson process on Rd such that the quantity γ defined by (8.3) is finite. Then η is stationary if and only if the intensity measure λ of η equals γλd.

Proof In view of Proposition 8.2 we need only to show that λ = γλd implies that θxη has the same distribution as η for all x ∈ Rd. Since θx preserves Lebesgue measure, this follows from Theorem 5.1 (the mapping theorem) or by a direct check of Definition 3.1. □

For examples of non-Poisson stationary point processes we refer to Exercises 8.2 and 8.3, Section 14.2 and Section 16.5.

The next result says that a stationary point process cannot have a positive but finite number of points. Given μ ∈ N we define the support of μ by

$$\sup p \mu \colon = \{ x \colon \mu \{ x \} > 0 \} .$$

Given x = (x1, . . . , xd) ∈ Rd and y = (y1, . . , yd) ∈ Rd one says that x is lexicographically smaller than y if there exists i ∈ {1, . . . , d – 1} such that xj = yj for j ∈ {1, . . . , i − 1} and xi &lt; yi. In this case we write x &lt; y. Every non-empty finite set B ⊂ Rd has a unique lexicographic minimum l(B); note that l(B + x) = l(B) + x for all x ∈ Rd. If B ⊂ Rd is empty or infinite we set l(B) := 0.


<!-- p:82 -->


Proposition 8.4 Suppose that η is a stationary point process on Rd. Then P(0 &lt; η(Rd) &lt; ∞) = 0.

Proof Assume on the contrary that P(0 &lt; η(Rd) &lt; ∞) &gt; 0 and consider the conditional probability measure P′ := P(· | 0 &lt; η(Rd) &lt; ∞). Since η is stationary under P and η(Rd) = θxη(Rd), η is stationary under P'. By Proposition 6.2, μ → l(supp μ) is a measurable mapping on N&lt;∞(Rd). For x ∈ Rd the random variable lI(supp η) has under P' the same distribution as

$$l ( \sup p \, \theta _ { x } \eta ) = l ( ( \sup p \, \eta ) - x ) = l ( \sup p \, \eta ) - x ,$$

where the second identity holds P'-a.s. This contradicts the fact that there is no translation invariant probability measure on Rd. □

### 8.2 The Pair Correlation Function

In this section we deal with certain second order properties of stationary point processes. We say that a point process η on Rd is locally square integrable if

$$\mathbb { E } [ \eta ( B ) ^ { 2 } ] < \infty , \quad B \in \mathcal { B } _ { b } ^ { d } ,$$

where Bd denotes the system of all bounded Borel subsets of Rd. For a stationary point process it suffices to check (8.5) for only one bounded set:

Lemma 8.5 Let η be a stationary point process on Rd and assume that E[η([0, 1]d)2] &lt; ∞. Then η is locally square integrable.

Proof Let B ∈ Bd. Then there exist n ∈ N and x1,.. .,xn ∈ Rd such that B ⊂ ∪i=1Bi, where Bi := [0, 1]d + xi. Then η(B) ≤ Σi=1 η(Bi) and Minkowski's inequality together with stationarity shows that E[η(B)2] is finite. □

If η is locally square integrable, then

$$\mathbb { E } [ \eta ^ { ( 2 ) } ( C ) ] < \infty , \quad C \subset \mathbb { R } ^ { d } \times \mathbb { R } ^ { d } \text { bounded and measurable} .$$

Indeed, for such C there exists B ∈ Bd such that C ⊂ B × B, so that (8.6) follows from (4.7) (see also Exercise 4.4) and Lemma 8.5. Recall the definition (4.22) of the factorial moment measures.

Definition 8.6 Let η be a stationary point process on Rd with second factorial moment measure α2. The measure α2 on Rd defined by

$$\alpha _ { 2 } ^ { ! } ( B ) \coloneqq \int \mathbf 1 \{ x \in [ 0 , 1 ] ^ { d } , y - x \in B \} \, \alpha _ { 2 } ( d ( x , y ) ) , \quad B \in \mathcal { B } ^ { d } , \quad ( 8 . 7 )$$


<!-- p:83 -->


is called the reduced second factorial moment measure of η.

Loosely speaking, α2(dx) measures the intensity of pairs of points at a relative displacement of x. The reduced second factorial moment measure α2 determines α2:

Proposition 8.7 Let η be a stationary point process on Rd with second factorial moment measure α2. Then η is locally square integrable if and only if its reduced second factorial moment measure α2 is locally finite. In this case,

$$\ m s \ c a { \real } e , \\ \int f ( x , y ) \, \alpha _ { 2 } ( d ( x , y ) ) = \iint f ( x , x + y ) \, \alpha _ { 2 } ^ { \prime } ( d y ) \, d x , \quad f \in \mathbb { R } _ { + } ( \mathbb { R } ^ { d } \times \mathbb { R } ^ { d } ) . \\$$

Proof Assume that η is locally square integrable and let B ⊂ Rd be compact. Then B′ := {x + y : x ∈ [0, 1]d, y ∈ B} is a compact set and, if y ∈ [0, 1]d and y − x ∈ B, then y ∈ B′, so that α2(B) ≤ α2([0, 1]d × B′) &lt; ∞ by (8.6). Hence α2 is locally finite. Conversely, the set inclusion

$$[ 0 , 1 ] ^ { d } \times [ 0 , 1 ] ^ { d } \subset \{ ( x , y ) \in \mathbb { R } ^ { d } \times \mathbb { R } ^ { d } \, \colon x \in [ 0 , 1 ] ^ { d } , y - x \in [ - 1 , 1 ] ^ { d } \}$$

shows that E[η([0, 1]d)(η([0, 1]d) − 1)] ≤ α2([−1, 1]d), and by Exercise 8.12 and Lemma 8.5 this proves the other direction of the asserted equivalence.

The proof of (8.8) is based on the fact that Lebesgue measure is the only ant   nn   t iy  uti tin factor. Let B ∈ Bd and define a measure vB on Rd by

$$\nu _ { B } ( C ) \coloneqq \int \mathbf 1 \{ x \in C , y - x \in B \} \, \alpha _ { 2 } ( d ( x , y ) ) , \quad C \in \mathcal { B } ^ { d } .$$

It follows, as in the first step of the proof, that this measure is locally finite. To show that it is also translation invariant we let z ∈ Rd and C ∈ Bd. Then

$$1 0 \, \text {show that} \, 1 1 \, \text {is also translated in invariant wec} \, 1 2 \in \mathbb { E } \, \cdot \, 2 \, . \, \text {In} \\ \nu _ { B } ( C + z ) & = \mathbb { E } \left [ \int 1 \{ x - z \in C , y - z - ( x - z ) \in B \} \, \eta ^ { ( 2 ) } ( d ( x , y ) ) \right ] \\ & = \mathbb { E } \int 1 \{ x \in C , y - x \in B \} \, ( \theta _ { z } \eta ) ^ { ( 2 ) } ( d ( x , y ) ) = \nu _ { B } ( C ) ,$$

where we have used the stationarity of η. Hence vB is translation invariant, so that νB = cBλd for some cB ∈ R+. Then cB = νB([0, 1]d) and

$$\nu _ { B } ( C ) = \nu _ { B } ( [ 0 , 1 ] ^ { d } ) \lambda _ { d } ( C ) = \alpha _ { 2 } ^ { ! } ( B ) \lambda _ { d } ( C ) .$$

Therefore

$$\int g ( x , y - x ) \, \alpha _ { 2 } ( d ( x , y ) ) = \int g ( x , z ) \, \alpha _ { 2 } ^ { ! } ( d z ) \, d x ,$$


<!-- p:84 -->


first for g = 1C×B and then for all g ∈ R+(Rd × Rd). Applying this with g(x, y) := f(x, y + x) yields the result. □

In principle, (8.8) can be used to compute second moments of integrals with respect to locally square integrable point processes. If η is stationary and locally square integrable and v, w ∈ R+ (Rd), then by (4.25) and (8.8)

$$\mathbb { E } [ \eta ( v ) \eta ( w ) ] = \iint v ( x ) w ( x + y ) \, \alpha _ { 2 } ^ { ! } ( d y ) \, d x + \gamma \int v ( x ) w ( x ) \, d x ,$$

where γ is the intensity of η. This formula remains true for v, w ∈ R(Rd), whenever the integrals on the right are finite.

Proposition 8.8 Let η be a stationary locally square integrable point process on Rd with second (resp. reduced second) factorial moment measure α2 (resp. α2). Then α2 « λd with Radon−Nikodým derivative ρ ∈ R+(Rd) if and only if

$$\int f ( x , y ) \, \alpha _ { 2 } ( d ( x , y ) ) = \int f ( x , y ) \rho ( y - x ) \, d ( x , y ) , \quad f \in \mathbb { R } _ { + } ( \mathbb { R } ^ { d } \times \mathbb { R } ^ { d } ) .$$

Proof If α2 « λd with density ρ, then Proposition 8.7 and a change of variables show that (8.9) holds. Conversely, if (8.9) holds, then Proposition 8.7 shows for each f ∈ R+(Rd × Rd) that

$$\iint f ( x , x + y ) \, \alpha _ { 2 } ^ { ! } ( d y ) \, d x = \int f ( x , x + y ) \rho ( y ) \, d ( x , y ) ,$$

or, for each g ∈ R+(Rd × Rd),

$$\iint g ( x , y ) \, \alpha _ { 2 } ^ { ! } ( d y ) \, d x & = \int g ( x , y ) \rho ( y ) \, d ( x , y ) . \\$$

Choosing g(x, y) = 1{x ∈ [0, 1]d}h(y) for h ∈ R+(Rd) gives α2(dy) = ρ(y) dy and hence the asserted result. □

Definition 8.9 Let η be a locally square integrable stationary point process on Rd with positive intensity γ and assume that (8.9) holds for some ρ ∈ R+(Rd). Then ρ2 := γ−2ρ is called the pair correlation function of η.

If η is not simple, that is P(η ∈ Ns(Rd)) &lt; 1, Exercise 8.10 shows that the pair correlation function cannot exist. In such a case one may apply Definition 8.9 to the simple point process η* defined in Exercise 8.7.

Example 8.10 Let η be a stationary Poisson process on Rd with positive intensity. Then Corollary 4.10 and Proposition 8.8 show that the pair correlation function of η is given by ρ2 ≡ 1.


<!-- p:85 -->


On a heuristic level, (4.24) and (8.9) (or (8.7)) imply that

$$\mathbb { E } [ \eta ( d x ) \eta ( d y ) ] = \rho ( y - x ) \, d x \, d y .$$

Hence the pair correlation function ρ2 of a stationary point process with intensity γ satisfies the heuristic equation

$$\mathbb { C } o v ( \eta ( d x ) , \eta ( d y ) ) = \gamma ^ { 2 } ( \rho _ { 2 } ( y - x ) - 1 ) \, d x \, d y .$$

Therefore the inequality ρ2(y-x) &lt; 1 indicates attraction between potential points at x and y, while ρ2(y − x) &gt; 1 indicates repulsion. Later in this book we shall encounter several examples of pair correlation functions.

### 8.3 Local Properties

In this section we assume that η is a stationary simple point process on Rd with intensity γ ∈ (0, ∞). We might expect that both P(η(B) = 1) and P(η(B) ≥ 1) behave like γλd(B) for small B ∈ Bd. This is made precise by the following result.

Proposition 8.11 Let B ⊂ Rd be a bounded Borel set with λd(B) &gt; 0 and let rn &gt; 0, n ∈ N, with limn→∞ rn = 0. For each n ∈ N let Bn := rnB. Then

$$\lim _ { n \to \infty } \frac { \mathbb { P } ( \eta ( B _ { n } ) \geq 1 ) } { \lambda _ { d } ( B _ { n } ) } = \lim _ { n \to \infty } \frac { \mathbb { P } ( \eta ( B _ { n } ) = 1 ) } { \lambda _ { d } ( B _ { n } ) } = \gamma .$$

Proof Let c &gt; 0. For each n ∈ N let Cn := [0, c/n)d and let Cn,1, . . . , Cn,nd be a collection of disjoint translates of C with union C1. Since η is simple (and locally finite), we have almost surely that

$$\eta ( C _ { 1 } ) = \lim _ { n \to \infty } \sum _ { i = 1 } ^ { n ^ { d } } 1 \{ \eta ( C _ { n , i } ) \geq 1 \} = \lim _ { n \to \infty } \sum _ { i = 1 } ^ { n ^ { d } } 1 \{ \eta ( C _ { n , i } ) = 1 \} .$$

The sums in the above limits are bounded by η(C1), so taking expectations we obtain from dominated convergence and stationarity that

$$\gamma c ^ { d } = \lim _ { n \to \infty } n ^ { d } \, \mathbb { P } ( \eta ( C _ { n } ) \geq 1 ) = \lim _ { n \to \infty } n ^ { d } \, \mathbb { P } ( \eta ( C _ { n } ) = 1 ) ,$$

which is (8.11) in the case where B = [0, c)d and rn = 1/n.

Next we note that for each bounded B ∈ Ba we have

$$\mathbb { E } [ \eta ( B ) ] - \mathbb { E } [ 1 \{ \eta ( B ) \geq 2 \} \eta ( B ) ] = \mathbb { P } ( \eta ( B ) = 1 ) \leq \mathbb { P } ( \eta ( B ) \geq 1 ) \leq \mathbb { E } [ \eta ( B ) ] .$$

Therefore (8.11) is equivalent to

$$\lim _ { n \to \infty } \frac { \mathbb { E } [ 1 \{ \eta ( B _ { n } ) \geq 2 \} \eta ( B _ { n } ) ] } { \lambda _ { d } ( B _ { n } ) } = 0 .$$


<!-- p:86 -->


Consider now a general sequence (r) but still assume that B is a halfopen cube containing the origin. Let n ∈ N and let m ∈ N satisfy the inequalities 1/(m + 1) &lt; rn ≤ 1/m (assuming without loss of generality that rn ≤ 1). Set Bn := m−1 B, so that Bn ⊂ B′. Then

$$\frac { \lambda _ { d } ( B _ { n } ^ { \prime } ) } { \lambda _ { d } ( B _ { n } ) } = \frac { 1 } { m _ { n } ^ { d } r _ { n } ^ { d } } \leq \frac { ( m _ { n } + 1 ) ^ { d } } { m _ { n } ^ { d } } \leq 2 ^ { d } .$$

Hence

$$\frac { \mathbb { E } [ 1 \{ \eta ( B _ { n } ) \geq 2 \} \eta ( B _ { n } ) ] } { \lambda _ { d } ( B _ { n } ) } \leq \frac { \mathbb { E } [ 1 \{ \eta ( B _ { n } ^ { \prime } ) \geq 2 \} \eta ( B _ { n } ^ { \prime } ) ] } { \lambda _ { d } ( B _ { n } ) } \leq 2 ^ { d } \frac { \mathbb { E } [ 1 \{ \eta ( B _ { n } ^ { \prime } ) \geq 2 \} \eta ( B _ { n } ^ { \prime } ) ] } { \lambda _ { d } ( B _ { n } ^ { \prime } ) }$$

which converges to zero by the case considered previously.

For a general B, choose a half-open cube C with B ⊂ C and set B′ := rnC, n ∈ N. Then Bn ⊂ Bn and λd(Bn)/λd(Bn) = λd(C)/λd(B), so that the assertion follows as before. □

### 8.4 Ergodicity

Sometimes stationary point processes satisfy a useful zero-one law. The invariant σ-field is defined by

$$\mathcal { I } \colon = \{ A \in \mathcal { N } \, \colon \theta _ { x } A = A \text { for all } x \in \mathbb { R } ^ { d } \} ,$$

q s s   sor od s  {   : x} =: θ b ergodic if P(η ∈ A) ∈ {0, 1} for all A ∈ I. Recall that a function h: Rd → R satisfies lim||x→∞ h(x) = a for some a ∈ R if, for each ε &gt; 0, there exists c &gt; 0 such that each x ∈ Rd with ∥x|| &gt; c satisfies |h(x) − a| &lt; ε.

Proposition 8.12 Suppose that η is a stationary point process on Rd. Assume that there exists a π-system H generating N such that

$$\lim _ { \| x \| \to \infty } \mathbb { P } ( \eta \in A , \theta _ { x } \eta \in A ^ { \prime } ) = \mathbb { P } ( \eta \in A ) \mathbb { P } ( \eta \in A ^ { \prime } ) \quad ( 8 . 1 4 )$$

for all A, A' ∈ H. Then (8.14) holds for all A, A′ ∈ N.

Proof We shall use the monotone class theorem (Theorem A.1). First fix A′ ∈ H. Let D be the class of sets A ∈ N satisfying (8.14). Then N ∈ D and D is closed with respect to proper differences. Let A ∈ H, n ∈ N, be such that A ↑ A for some A ∈ N. Then we have for all x ∈ Rd that


<!-- p:87 -->


```
| \mathbb { P } ( \eta \in A ) \mathbb { P } ( \eta \in A ^ { \prime } ) - \mathbb { P } ( \eta \in A , \theta _ { x } \eta \in A ^ { \prime } ) | \\ & \leq | \mathbb { P } ( \eta \in A ) \mathbb { P } ( \eta \in A ^ { \prime } ) - \mathbb { P } ( \eta \in A _ { n } ) \mathbb { P } ( \eta \in A ^ { \prime } ) | \\ & + | \mathbb { P } ( \eta \in A _ { n } ) \mathbb { P } ( \eta \in A ^ { \prime } ) - \mathbb { P } ( \eta \in A _ { n } , \theta _ { x } \eta \in A ^ { \prime } ) | \\ & + | \mathbb { P } ( \eta \in A _ { n } , \theta _ { x } \eta \in A ^ { \prime } ) - \mathbb { P } ( \eta \in A , \theta _ { x } \eta \in A ^ { \prime } ) | .
```

For large n the first and third terms are small uniformly in x ∈ Rd. For any fixed n ∈ N the second term tends to 0 as ∥|x| → ∞. It follows that A ∈ D. Hence D is a Dynkin system and Theorem A.1 shows that σ(H) ⊂ D, that is N = D. Therefore (8.14) holds for all A ∈ N and A' ∈ H.

Now fix A ∈ N and let D' be the class of sets A' ∈ N satisfying (8.14). It follows as before that D' is a Dynkin system. When checking that D' contains any monotone union A' of sets A′ ∈ D' one has to use the fact that

$$| \mathbb { P } ( \eta \in A , \theta _ { x } \eta \in A _ { n } ^ { \prime } ) - \mathbb { P } ( \eta \in A , \theta _ { x } \eta \in A ^ { \prime } ) | & \leq \mathbb { P } ( \theta _ { x } \eta \in A ^ { \prime } ) - \mathbb { P } ( \theta _ { x } \eta \in A _ { n } ^ { \prime } ) \\ & = \mathbb { P } ( \eta \in A ^ { \prime } ) - \mathbb { P } ( \eta \in A _ { n } ^ { \prime } ) ,$$

where the equality comes from the stationarity of η. Theorem A.1 shows that D' contains all A' ∈ N, implying the assertion. □

A stationary point process η satisfying (8.14) for all A, A' ∈ N is said to be mixing. Any point process with this property is ergodic. Indeed, if A ∈ N satisfies θxA = A for all x ∈ Rd, then we can take A = A' in (8.14) and conclude that P(η ∈ A) = (P(η ∈ A))2.

Proposition 8.13 Let η be a stationary Poisson process with finite intensity. Then η is mixing and in particular is ergodic.

Proof Let Nls := Nls(Rd); see Definition 6.6. Proposition 6.9 shows that η is simple, that is P(η ∈ Nls) = 1. Define Nls := {A ∩ Nls : A ∈ N}. Let H denote the system of all sets of the form {μ ∈ Nls : μ(B) = 0} for some bounded B ∈ Bd. By Exercise 6.7, H is a π-system and generates Nls. Let B, B′ ∈ Bd be bounded. Let A = {μ ∈ Nls : μ(B) = 0} and define A′ similarly in terms of B'. For x ∈ Rd we have by (8.1) that

$$\{ \theta _ { x } \eta \in A ^ { \prime } \} = \{ \eta ( B ^ { \prime } + x ) = 0 \} .$$

If ∥x|| is sufficiently large, then B ∩ (B′ + x) = Ø, so that the events {η ∈ A} and {θxη ∈ A'} are independent. Therefore,

$$\mathbb { P } ( \eta \in A , \theta _ { x } \eta \in A ^ { \prime } ) = \mathbb { P } ( \eta \in A ) \, \mathbb { P } ( \theta _ { x } \eta \in A ^ { \prime } ) = \mathbb { P } ( \eta \in A ) \, \mathbb { P } ( \eta \in A ^ { \prime } ) ,$$

implying (8.14). Since P(η ∈ Nls) = P(θxη ∈ Nls) = 1 for all x ∈ Rd, the proof of Proposition 8.12 shows that (8.14) holds for all A, A' ∈ N. □


<!-- p:88 -->


For an extension of Proposition 8.13 to marked Poisson processes see Exercise 10.1.

### 8.5 A Spatial Ergodic Theorem

In this section we let η be a stationary point process on Rd with finite intensity γ. Define

$$\mathcal { I } _ { \eta } \colon = \{ \eta ^ { - 1 } ( A ) \colon A \in \mathcal { I } \} ,$$

where the invariant σ-field I is given by (8.13). The following result is derived from the univariate version of the mean ergodic theorem, proved in Section B.2; see Theorem B.11.

Theorem 8.14 (Mean ergodic theorem) Let W ⊂ Rd be compact and convex with non-empty interior, and set W := aW for some sequence (an)n≥1 with an → ∞ as n → ∞. Then, as n → ∞,

$$\frac { \eta ( W _ { n } ) } { \lambda _ { d } ( W _ { n } ) } \rightarrow \mathbb { E } [ \eta ( [ 0 , 1 ] ^ { d } ) \, | \, \mathcal { I } _ { \eta } ] \, \ i n \, L ^ { 1 } ( \mathbb { P } ) .$$

Proof We consider only the case with d = 2, leaving the generalisation to other values of d to the reader.

For i, j ∈ N, set Xi,j := η([i, i + 1) × [j, j + 1)). Then for each j ∈ N the sequence (Xi,j)i∈N is stationary and satisfies 0 &lt; E[X1,j] &lt; ∞. By Theorem B.11, for each j ∈ N we have L1-convergence

$$n ^ { - 1 } \sum _ { i = 1 } ^ { n } X _ { i , j } \rightarrow Y _ { j }$$

for some integrable Yj. Moreover, (Yj)j≥1 is a stationary sequence and E[|Y1] &lt; ∞, so by applying Theorem B.11 again we have

$$m ^ { - 1 } \sum _ { j = 1 } ^ { m } Y _ { j } \rightarrow Z _ { 1 } \ \text {in} \ L ^ { 1 } ( \mathbb { P } )$$

for some integrable Z1. Writing ∥|X|l1 for E[|X|] for any random variable X, we have for n, m ∈ N that

$$\ w c { \text {have for } } n , m \subset & \inf \nolimits _ { 1 } ^ { m } \sum _ { i = 1 } ^ { n } \sum _ { j = 1 } ^ { m } X _ { i , j } - Z _ { 1 } \left \| _ { 1 } \\ & \leq \left \| m ^ { - 1 } \sum _ { j = 1 } ^ { n } \left ( n ^ { - 1 } \sum _ { i = 1 } ^ { n } X _ { i , j } - Y _ { j } \right ) \right \| _ { 1 } + \left \| m ^ { - 1 } \sum _ { j = 1 } ^ { m } Y _ { j } - Z _ { 1 } \right \| _ { 1 } .$$


<!-- p:89 -->


Therefore,

$$\text {There,} \\ & \quad \left \| ( n m ) ^ { - 1 } \sum _ { i = 1 } ^ { n } \sum _ { j = 1 } ^ { m } X _ { i , j } - Z _ { 1 } \right \| _ { 1 } \\ & \quad \leq m ^ { - 1 } \sum _ { j = 1 } ^ { m } \left \| n ^ { - 1 } \sum _ { i = 1 } ^ { n } X _ { i , j } - Y _ { j } \right \| _ { 1 } + \left \| m ^ { - 1 } \sum _ { j = 1 } ^ { m } Y _ { j } - Z _ { 1 } \right \| _ { 1 } \\ & \quad = \left \| n ^ { - 1 } \sum _ { i = 1 } ^ { n } X _ { i , 1 } - Y _ { 1 } \right \| _ { 1 } + \left \| m ^ { - 1 } \sum _ { j = 1 } ^ { m } Y _ { j } - Z _ { 1 } \right \| _ { 1 } , \\ \text {which tends to zero as $n,m\to \infty$} .$$

which tends to zero as n, m → ∞.

Let R0 be the class of all rectangles R of the form R = [0, s) × [0, t) with s, t &gt; 0. Then we assert that

$$a _ { n } ^ { - 2 } \eta ( a _ { n } R ) \rightarrow \lambda _ { 2 } ( R ) Z _ { 1 } \quad \text {in} \ L ^ { 1 } ( \mathbb { P } ) , \quad R \in \mathcal { R } _ { 0 } .$$

To show this we use (here and later in the proof) for a ∈ R the notation

$$\lfloor a \rfloor \colon = \max \{ k \in \mathbb { Z } \colon k \leq a \} , \quad \lceil a \rceil \colon = \min \{ k \in \mathbb { Z } \colon k \geq a \} .$$

Given s, t &gt; 0 and setting R = [0, s) × [0, t) we have

$$\| a _ { n } ^ { - 2 } \eta ( a _ { n } R ) - s t Z _ { 1 } \| _ { 1 } & \leq a _ { n } ^ { - 2 } \left \| \sum _ { i = 1 } ^ { \lfloor a _ { n } \rfloor \lfloor a _ { n } t \rfloor } X _ { i , j } - \lfloor a _ { n } s \rfloor \lfloor a _ { n } t \rfloor Z _ { 1 } \right \| _ { 1 } \\ & + a _ { n } ^ { - 2 } \| \eta ( a _ { n } R \vee [ 0 , \lfloor a _ { n } s \rfloor ) \times [ 0 , \lfloor a _ { n } t \rfloor ) ) \| _ { 1 } + a _ { n } ^ { - 2 } \| ( s t - \lfloor a _ { n } s \rfloor \lfloor a _ { n } t \rfloor ) Z _ { 1 } \| _ { 1 }$$

and the first term in the expression on the right-hand side tends to zero by the preceding argument, while the second and the third term are bounded by a−2γλ2(aR \ [0, Las]) × [0, Lat])), which tends to zero.

Now let R be the class of all rectangles R of the form R = [a, b) × [c, d) with 0 ≤ a &lt; b and 0 ≤ c &lt; d. Let R = [a, b) × [c, d) ∈ R. Defining

$$R _ { 1 } \colon & = [ 0 , b ) \times [ 0 , d ) , \quad R _ { 2 } \colon = [ 0 , a ) \times [ 0 , d ) , \\ R _ { 3 } \colon & = [ 0 , b ) \times [ 0 , c ) , \quad R _ { 4 } \colon = [ 0 , a ) \times [ 0 , c ) ,$$

by additivity of η we have for any t ∈ R+ that

$$\eta ( t R ) = \eta ( t R _ { 1 } ) - \eta ( t R _ { 2 } ) - \eta ( t R _ { 3 } ) + \eta ( t R _ { 4 } ) .$$

Therefore, applying (8.17) to R1, . . . , R4, we obtain

$$a _ { n } ^ { - 2 } \eta ( a _ { n } R ) \rightarrow \lambda _ { 2 } ( R ) Z _ { 1 } \quad \text {in} \ L ^ { 1 } ( \mathbb { P } ) , \quad R \in \mathcal { R } .$$

Now we assume that W ⊂ R2. In this case, given ε &gt; 0, since W is assumed convex we can choose disjoint rectangles R1, . . ., Rk ∈ R such that R := ∪k=1Ri ⊂ W and λ2(W \ R) &lt; ε. Then


<!-- p:90 -->


$$a _ { n } ^ { - 2 } \| \eta ( W _ { n } ) - Z _ { 1 } \lambda _ { 2 } ( W _ { n } ) \| _ { 1 } \\ & \leq a _ { n } ^ { - 2 } \| \eta ( a _ { n } ( W \vee R ) ) \| _ { 1 } + a _ { n } ^ { - 2 } \| \eta ( a _ { n } R ) - a _ { n } ^ { 2 } \lambda _ { 2 } ( R ) Z _ { 1 } \| _ { 1 } \\ & \quad + a _ { n } ^ { - 2 } \| \lambda _ { 2 } ( a _ { n } R ) Z _ { 1 } - \lambda _ { 2 } ( a _ { n } W ) Z _ { 1 } \| _ { 1 } .$$

On the right-hand side the first and third terms are each bounded by yε, while the middle term tends to zero by (8.18) and the additivity of η. Therefore, since ε is arbitrarily small, the left-hand side tends to zero as n → ∞, and this gives us

$$a _ { n } ^ { - 2 } \eta ( W _ { n } ) \rightarrow \lambda _ { 2 } ( W ) Z _ { 1 } \quad \text {in} \ L ^ { 1 } ( \mathbb { P } ) .$$

Here we have not used that λ2(W) &gt; 0.

Let Q1 be the upper right (closed) quadrant of R2 and let Q2, Q3, Q4 denote the other quadrants of R2. Just as in the case i = 1 we see that there are integrable random variables Z2, Z3, Z4 such that

$$a _ { n } ^ { - 2 } \eta ( W _ { n } ) \rightarrow Z _ { i } \quad \text {in} \ L ^ { 1 } ( \mathbb { P } ) ,$$

whenever i ∈ {1, 2, 3, 4} is such that W ⊂ Qi.

For general W we may write W = U1=1 Wi with each of the (convex) sets W1, . . . , W4 contained in a single quadrant of R2. Using (8.19) and the fact that E[η(Wi ∩ Wj)] = 0 for i ≠ j, we have as n → ∞ that

$$\lambda _ { 2 } ( a _ { n } W ) ^ { - 1 } \eta ( a _ { n } W ) \rightarrow Z , \quad \text {in } L ^ { 1 } ( \mathbb { P } ) ,$$

where Z := λ(W)−1(λ2(W1)Z1 + · · · + λ2(W4)Z4).

Next we show that the random variable Z can be chosen I η-measurable. Set Q := [−1/2, 1/2]2 and let

$$Z ^ { \prime } ( \mu ) \colon = \liminf _ { n \to \infty } n ^ { - 2 } \mu ( n Q ) , \quad \mu \in \mathbf N .$$

Let x = (u, v) ∈ R2. Then we have for each n ≥ 2 max{[|u|], [|v|]} that

$$( n - 2 \max \{ | | u | | , \lceil | v | \rceil \} ) Q \subset n Q + x \subset ( n + 2 \max \{ | | u | | , \lceil | v | \rceil \} ) Q ,$$

so that Z'(θxμ) = Z'(μ). Hence the mapping Z'(·) is I-measurable. By (8.20) with W = Q and a = n, and since L1-convergence implies convergence in probability (see Proposition B.8), we have that P(Z = Z'(η)) = 1. Hence we can assume that Z is I-measurable.

It remains to prove that Z = E[η[0, 1]a | Iη]. Let A ∈ I. For n ∈ N


<!-- p:91 -->


let Sn := n−2η(nQ), where again Q := [−1/2, 1/2]d. Then 1{η ∈ A}Sn converges to 1{η ∈ A}Z in L1(P). Therefore

$$\mathbb { E } [ 1 \{ \eta \in A \} Z ] & = \lim _ { n \to \infty } \mathbb { E } [ 1 \{ \eta \in A \} S _ { n } ] = \lim _ { n \to \infty } n ^ { - 2 } \mathbb { E } [ 1 \{ \eta \in A \} \eta ( n Q ) ] \\ & = \mathbb { E } [ 1 \{ \eta \in A \} \mathbb { E } [ \eta ( [ 0 , 1 ] ^ { d } ) \, | \, \mathcal { I } _ { \eta } ] ] ,$$

where we have used Exercise 8.11. Thus Z has the defining properties of E[η([0, 1]d) | Iη], so Z = E[η([0, 1]d) | Iη] P-a.s. □

A bounded set B ⊂ Rd is said to be Riemann measurable if 1B is Riemann integrable, that is, if B can be approximated in measure from below and above by finite unions of hypercubes. For example, a convex set has this property. The proof of Theorem 8.14 shows that it is enough to assume that W is Riemann measurable.

Theorem 8.14 justifies calling

$$\hat { \eta } \colon = \mathbb { E } [ \eta ( [ 0 , 1 ] ^ { d } ) \, | \, \mathcal { I } _ { \eta } ]$$

the sample intensity of η. If η is ergodic, then P(η = γ) = 1. The theorem remains valid for stationary random measures to be introduced in Exercise 13.12; see Exercise 13.13.

### 8.6 Exercises

Exercise 8.1 Let η be a stationary point process on R. Prove that

$$\mathbb { P } ( \eta \neq 0 , \eta ( ( - \infty , 0 ] ) < \infty ) = \mathbb { P } ( \eta \neq 0 , \eta ( [ 0 , \infty ) ) < \infty ) = 0 .$$

Exercise 8.2 Let Q be a probability measure on N(Rd) and let K be the probability kernel from Rd to N(Rd) defined by K(x, A) := Q(θxA). Let η be a stationary Poisson process on Rd with a (finite) intensity γ ≥ 0 and let χ be a Poisson cluster process as in Exercise 5.6. Show that χ is stationary with intensity γ ∫ μ(Rd) Q(dμ). (Hint: Use the Laplace functional in Exercise 5.6 to prove the stationarity.)

Exercise 8.3 Let C := [0, 1)d be a half-open unit cube. Let μ ∈ N&lt;∞(Rd) such that μ(Rd \ C) = 0 and let X be uniformly distributed on C. Show that η := Σy∈z θy+xμ is a stationary point process with intensity μ(C). Show also that η is ergodic. (Hint: To check ergodicity use that η = θxμ0 for some μ0 ∈N1(Rd).)

Exercise 8.4 Let T : N → N be measurable such that T(θxμ) = θxT(μ) for all (x, μ) ∈ Rd × N. Show that if η is a stationary (resp. stationary and ergodic) point process on Rd, then so is T(η).


<!-- p:92 -->


Exercise 8.5 Give an example of a stationary locally finite point process η with E[η([0, 1]d)] = ∞.

Exercise 8.6 Give an example of a stationary point process that is not locally finite. (Hint: Such a point process has to have infinitely many accumulation points.)

Exercise 8.7 Let η be a locally finite stationary point process on Rd. Use Exercise 8.4 to show that

$$\eta ^ { * } \colon = \int \eta \{ x \} ^ { \oplus } \mathbf 1 \{ x \in \cdot \} \, \eta ( d x )$$

is a stationary point process; see also Exercise 6.6.

Exercise 8.8 Let η be a stationary locally finite point process on Rd with finite intensity but do not assume that η is simple. Show that the first limit in (8.11) exists and equals E[η*([0, 1]d)], where η* is given by (8.22).

Exercise 8.9 Let η be a locally square integrable stationary point process ds ot on   n  t sp  n n Let W ⊂ Rd be a bounded Borel set and show that

$$\mathbb { V } a r [ \eta ( W ) ] = \gamma ^ { 2 } \int \lambda _ { d } ( W \cap ( W + x ) ) ( \rho _ { 2 } ( x ) - 1 ) \, d x + \gamma \lambda _ { d } ( W ) .$$

Exercise 8.10 Let η be a stationary point process on Rd with reduced second factorial moment measure α2. Show that η is simple if and only if α2({0}) = 0. (Hint: Assume without loss of generality that η is a random element of N(Rd) and note that η is simple if and only if the stationary point process η′ := ∫ 1{x ∈ ·}(η{x} − 1) η(dx) has intensity zero.)

Exercise 8.11 Let η be a stationary point process with finite intensity. Show that

$$\mathbb { E } [ \eta ( B ) \, | \, \mathcal { I } _ { \eta } ] = \lambda _ { d } ( B ) \mathbb { E } [ \eta ( [ 0 , 1 ] ^ { d } ) \, | \, \mathcal { I } _ { \eta } ] \quad \mathbb { P } { \text {-a.s} }$$

holds for each B ∈ Bd. (Hint: Take A ∈ I and use the proof of Proposition 8.2 to show that E[1{η ∈ A}η(B)] = λd(B)E[1{η ∈ A}η([0, 1]d)].)

Exercise 8.12 Let X ≥ 0 be a random variable with E[X(X − 1)] &lt; ∞. Show that E[X2] &lt; ∞.

Exercise 8.13 Let η be a locally finite stationary point process on Rd, interpreted as a random element of Nl := N1(Rd). Let f ∈ R+(N1) and let ν be a σ-finite measure on Rd such that v(Rd) &gt; 0 and v({x : f(θxη) ≠ 0}) = 0 P-a.s. Show that E[f(η)] = 0. (Hint: Use Fubini's theorem.)


<!-- p:93 -->


## The Palm Distribution

The Palm distribution of a stationary point process can be introduced via a refined Campbell theorem. It can be interpreted as a conditional distribution given that there is a point at the origin. A stationary point process is Poisson if and only if its Palm distribution is the distribution of the original process with an extra point added at the origin. For a given simple point process, Voronoi tessellations partition the space into regions based on the nearest neighbour principle. They are an important model of stochastic geometry but also provide a convenient setting for formulating the close relationship between the stationary distribution and the Palm distribution of a stationary simple point process. The latter is a volume-debiased version of the first, while, conversely, the former is a volume-biased version of the latter.

### 9.1 Definition and Basic Properties

Throughout this chapter η denotes a locally finite point process on Rd. It is convenient (and no loss of generality) to assume that η(ω) ∈ Nl for all ω ∈ Ω, where N1 := N1(Rd) ∈ N(Rd) is the space of locally finite measures from N(Rd) as in Definition 2.11. The advantage is that Lemma 9.2 below shows that the mapping (x, μ) → θxμ is measurable on Rd × Nl, where we choose N1 := Ni(Rd) = {A ∈ N(Rd) : A ⊂ Nl} as the σ-field on Nl.

If η is stationary, then the distribution Pη = P(η ∈ ·) of η does not change under a shift of the origin. We then also refer to Pη as the stationary distribution of η. We now introduce another distribution that describes η as seen from a typical point of η. In Chapter 10 we shall make this precise under an additional ergodicity hypothesis.

Theorem 9.1 (Refined Campbell theorem) Suppose that η is a stationary point process on Rd with finite strictly positive intensity γ. Then there exists a unique probability measure Pn on N1 such that


<!-- p:94 -->


$$\mathbb { E } [ \int f ( x , \theta _ { x } \eta ) \, \eta ( d x ) ] = \gamma \iint f ( x , \mu ) \, \mathbb { P } _ { \eta } ^ { 0 } ( d \mu ) \, d x , \quad f \in \mathbb { R } _ { + } ( \mathbb { R } ^ { d } \times N _ { l } ) .$$

Proof The proof generalises that of Proposition 8.7. For each A ∈ Ni we define a measure vA on Rd by

$$\nu _ { A } ( B ) \colon = \mathbb { E } \left [ \int 1 _ { B } ( x ) 1 _ { A } ( \theta _ { x } \eta ) \, \eta ( d x ) \right ] , \quad B \in \mathcal { B } ^ { d } ,$$

where the integrations are justified by Lemma 9.2. By definition of vA(·) and (8.2) we have for all y ∈ Rd that

$$8 . 2 ) \text { we have for all } y \in \mathbb { K } ^ { \text {th} } \text { that} \\ \nu _ { A } ( B + y ) = \mathbb { E } \left [ \int \mathbf 1 _ { B } ( x - y ) \mathbf 1 _ { A } ( \theta _ { x } \eta ) \, \eta ( d x ) \right ] \\ = \mathbb { E } \left [ \int \mathbf 1 _ { B } ( x ) \mathbf 1 _ { A } ( \theta _ { x + y } \eta ) \, ( \theta _ { y } \eta ) ( d x ) \right ] . \\$$

Because of the flow property θx+yη = θx(θyη), we can use stationarity to conclude that

$$\nu _ { A } ( B + y ) = \mathbb { E } \left [ \int \mathbf 1 _ { B } ( x ) \mathbf 1 _ { A } ( \theta _ { x } \eta ) \, \eta ( d x ) \right ] = \nu _ { A } ( B ) ,$$

so that vA is translation invariant. Furthermore, vA(B) ≤ E[η(B)] = γλd(B), so that vA is locally finite. Hence there is a number γA ≥ 0 such that

$$\nu _ { A } ( B ) = \gamma _ { A } \lambda _ { d } ( B ) , \ \ B \in \mathcal { B } ^ { d } .$$

Choosing B = [0, 1]d shows that γA = vA([0, 1]d) is a measure in A. Since it follows from (9.2) that

$$\mathbb { E } \left [ \int \mathbf 1 _ { B } ( x ) \mathbf 1 _ { A } ( \theta _ { x } \eta ) \, \eta ( d x ) \right ] = \gamma \mathbb { P } _ { \eta } ^ { 0 } ( A ) \lambda _ { d } ( B ) , \quad A \in \mathcal { N } _ { l } , \, B \in \mathcal { B } ^ { d } .$$

Hence (9.1) holds for functions of the form f(x, μ) = 1B(x)1A(μ) and then also for general measurable indicator functions by the monotone class theorem (Theorem A.1). Linearity of the integral and monotone convergence yield (9.1) for general f ∈ R+(Rd ×N1).

Conversely, (9.1) yields (9.3) and therefore

$$\mathbb { P } _ { \eta } ^ { 0 } ( A ) = \frac { 1 } { \gamma \lambda _ { d } ( B ) } \mathbb { E } \left [ \int \mathbf 1 _ { B } ( x ) \mathbf 1 _ { A } ( \theta _ { x } \eta ) \, \eta ( d x ) \right ] ,$$

provided that 0 &lt; λd(B) &lt; ∞.

□


<!-- p:95 -->


Clearly (9.4) extends to

$$\int f ( \mu ) \mathbb { P } _ { \eta } ^ { 0 } ( d \mu ) & = \frac { 1 } { \gamma \lambda _ { d } ( B ) } \mathbb { E } \left [ \int 1 _ { B } ( x ) f ( \theta _ { x } \eta ) \, \eta ( d x ) \right ] \\ \\$$

whenever 0 &lt; λd(B) &lt; ∞ and f ∈ R+(Nl). Multiplying this identity by γλa(B) yields a special case of (9.1).

We still need to prove the following measurability assertion.

Lemma 9.2 The mapping (x, μ) → θxμ from Rd × Nl to N1 is measurable.

where the mappings πn : Nl → Rd, n ∈ N, are measurable. For x ∈ Rd we the mapping (x, μ) → δπnμ)−x(B) = 1{π(μ) − x ∈ B} is measurable. □

Definition 9.3 Under the assumptions of Theorem 9.1 the measure P0 is η called the Palm distribution of η.

Sometimes we shall use the refined Campbell theorem in the equivalent form

$$\mathbb { E } [ \int f ( x , \eta ) \, \eta ( d x ) ] = \gamma \iint f ( x , \theta _ { - x } \mu ) \, \mathbb { P } _ { \eta } ^ { 0 } ( d \mu ) \, d x , \quad f \in \mathbb { R } _ { + } ( \mathbb { R } ^ { d } \times N _ { l } ) .$$

Indeed, for any f ∈ R+(Rd × N1) we can apply (9.1) with f ∈ R+(Rd × N1) defined by f(x, μ) := f(x, θ−xμ).

It follows from Proposition 6.3 that the mapping (x, μ) → 1{μ{x} &gt; 0} is measurable on Rd × N1. Indeed, we have

$$1 \{ \mu \{ x \} = 0 \} = \prod _ { n = 1 } ^ { \mu ( x ) } 1 \{ \pi _ { n } ( \mu ) \neq x \} . \\$$

By (9.4) we have for a stationary point process η that

$$\mathbb { P } _ { \eta } ^ { 0 } ( \mu \in \mathbb { N } _ { l } \colon \mu \{ 0 \} > 0 ) = \gamma ^ { - 1 } \mathbb { E } \left [ \int \mathbf 1 _ { [ 0 , 1 ] ^ { l } } ( x ) \mathbf 1 \{ \eta ( x ) \} > 0 \} \, \eta ( d x ) \right ] = 1 , \ \ ( 9 . 7 )$$

so that P0 is concentrated on those μ ∈ N, having an atom at the origin. If η is simple, we shall see in Proposition 9.5 that P can be interpreted as the conditional distribution of η given that η{0} &gt; 0.

### 9.2 The Mecke-Slivnyak Theorem

Our next result is a stationary version of Mecke's characterisation of the Poisson process (Theorem 4.1).


<!-- p:96 -->


Theorem 9.4 Let η be a stationary point process on Rd with intensity γ ∈ (0, ∞). Then η is a Poisson process if and only if

$$\mathbb { P } _ { \eta } ^ { 0 } = \mathbb { P } ( \eta + \delta _ { 0 } \in \cdot ) .$$

Proof Assume first that η is a Poisson process. For any A ∈ Ni we then obtain from the Mecke equation (4.2) that

$$\text {Obtain from} \ u n c { C } \ u n c { C } \ u n c { A } ( 4 . 2 ) \text { that} \\ \mathbb { E } \left [ \int \mathbf 1 _ { [ 0 , 1 ] ^ { d } } ( x ) \mathbf 1 _ { A } ( \theta _ { x } \eta ) \, \eta ( d x ) \right ] & = \gamma \mathbb { E } \left [ \int \mathbf 1 _ { [ 0 , 1 ] ^ { d } } ( x ) \mathbf 1 _ { A } ( \theta _ { x } ( \eta + \delta _ { x } ) ) \, d x \right ] \\ & = \gamma \int \mathbf 1 _ { [ 0 , 1 ] ^ { d } } ( x ) \mathbb { P } ( \eta + \delta _ { 0 } \in A ) \, d x = \gamma \mathbb { P } ( \eta + \delta _ { 0 } \in A ) ,$$

where we have used Fubini's theorem and stationarity for the second identity. Hence (9.8) follows from (9.4) with B = [0, 1]d.

Conversely, if (9.8) holds, we take f ∈ R+(Rd × N1) to obtain from (9.6) that

$$\mathbb { E } [ \int f ( x , \eta ) \, \eta ( d x ) ] = \gamma \int \mathbb { E } [ f ( x , \theta _ { - x } ( \eta + \delta _ { 0 } ) ) ] \, d x .$$

Stationarity yields that the Mecke equation (4.2) holds with λ = γλa. Theorem 4.1 then shows that η is a Poisson process. □

### 9.3 Local Interpretation of Palm Distributions

Let η be a stationary simple point process on Rd with intensity γ ∈ (0, ∞). Let η0 denote a Palm version of η, that is a point process (defined on the basic probability space (Ω, F, P)) with distribution P0. By Exercise 9.1 η0 is simple, while (9.7) implies that P(0 ∈ η0) = 1. If η(Ra) &gt; 0 we let X denote the point of η with smallest Euclidean norm, taking the lexicographically smallest such point if there is more than one. In the case η(Rd) = 0 we set X := 0. We now give a local interpretation of the Palm distribution.

Proposition 9.5 For n ∈ N let rn &gt; 0 and let B be the closed ball with centre 0 and radius rn. Assume that rn → 0 as n → ∞. Let g ∈ R(N) be bounded. Then

$$\lim _ { n \to \infty } \mathbb { E } [ g ( \theta _ { X } \eta ) \, | \, \eta ( B _ { n } ) \geq 1 ] = \mathbb { E } [ g ( \eta ^ { 0 } ) ] .$$

If, moreover, x → g(θxμ) is continuous for all μ ∈ Nls(Rd), then

$$\lim _ { n \to \infty } \mathbb { E } [ g ( \eta ) \, | \, \eta ( B _ { n } ) \geq 1 ] = \mathbb { E } [ g ( \eta ^ { 0 } ) ] .$$


<!-- p:97 -->


Proof By the triangle inequality

$$\left | \mathbb { E } [ g ( \theta _ { X } \eta ) \, | \, \eta ( B _ { n } ) \geq 1 ] - \mathbb { E } [ g ( \eta ^ { 0 } ) ] \right | \leq I _ { 1 , n } + I _ { 2 , n } ,$$

where we set

$$I _ { 1 , n } \colon = \gamma ^ { - 1 } \lambda _ { d } ( B _ { n } ) ^ { - 1 } \Big | \mathbb { E } [ \mathbf 1 \{ \eta ( B _ { n } ) \geq 1 \} g ( \theta _ { X } \eta ) ] - \gamma \lambda _ { d } ( B _ { n } ) \mathbb { E } [ g ( \eta ^ { 0 } ) ] \Big |$$

and

$$I _ { 2 , n } & \coloneqq \left | ( \mathbb { P } ( \eta ( B _ { n } ) \geq 1 ) ^ { - 1 } - \gamma ^ { - 1 } \lambda _ { d } ( B _ { n } ) ^ { - 1 } ) \mathbb { E } [ \{ \eta ( B _ { n } ) \geq 1 \} g ( \theta _ { X } \eta ) ] \right | \\ & \leq \frac { \mathbb { E } [ 1 \{ \eta ( B _ { n } ) \geq 1 \} | g ( \theta _ { X } \eta ) | ] } { \gamma \lambda _ { d } ( B _ { n } ) } \left | \frac { \gamma \lambda _ { d } ( B _ { n } ) } { \mathbb { P } ( \eta ( B _ { n } ) \geq 1 ) } - 1 \right | .$$

Since g is bounded, Proposition 8.11 shows that I2,n → 0 as n → ∞. By the refined Campbell theorem (Theorem 9.1),

$$I _ { 1 , n } = \gamma ^ { - 1 } \lambda _ { d } ( B _ { n } ) ^ { - 1 } \left | \mathbb { E } \left [ 1 \{ \eta ( B _ { n } ) \geq 1 \} g ( \theta _ { X } \eta ) - \int _ { B _ { n } } g ( \theta _ { x } \eta ) \, \eta ( d x ) \right ] \right | .$$

Since B is a ball, X ∈ B whenever η(B) ≥ 1. In the last expectation, distinguish the cases η(B) = 1 and η(B) ≥ 2; then we obtain

$$I _ { 1 , n } & \leq \gamma ^ { - 1 } \lambda _ { d } ( B _ { n } ) ^ { - 1 } \mathbb { E } \left [ 1 \{ \eta ( B _ { n } ) \geq 2 \} \int 1 _ { B _ { n } } ( x ) | g ( \theta _ { x } \eta ) | \, \eta ( d x ) \right ] \\ & \leq c \gamma ^ { - 1 } \lambda _ { d } ( B _ { n } ) ^ { - 1 } \mathbb { E } [ 1 \{ \eta ( B _ { n } ) \geq 2 \} \eta ( B _ { n } ) ] ,$$

where c is an upper bound of |gl. Therefore

$$I _ { 1 , n } \leq \frac { c ( \mathbb { E } [ \eta ( B _ { n } ) ] - \mathbb { P } ( \eta ( B _ { n } ) = 1 ) ) } { \gamma \lambda _ { d } ( B _ { n } ) } = c \left ( 1 - \frac { \mathbb { P } ( \eta ( B _ { n } ) = 1 ) } { \gamma \lambda _ { d } ( B _ { n } ) } \right ) ,$$

which tends to zero by Proposition 8.11.

To prove (9.10) it is now sufficient to show that

$$\lim _ { n \to \infty } \mathbb { E } [ | g ( \eta ) - g ( \theta _ { X } \eta ) | \, | \, \eta ( B _ { n } ) \geq 1 ] = 0 .$$

Given ε &gt; 0 and μ ∈ Nls := Nls(Rd), define

$$g _ { \varepsilon } ( \mu ) \colon = \sup \{ | g ( \mu ) - g ( \theta _ { x } \mu ) | \, \colon \| x \| \leq \varepsilon \} .$$

For μ ∈ N \ Nls we set gε(μ) := 0. Assuming that g has the stated additional continuity property, the supremum can be taken over a countable dense subset of B(0, ε). Since μ → θxμ is measurable for each x ∈ Rd (Lemma 9.2), we see that gε is a measurable function. Fixing ε &gt; 0 we note that

$$\mathbb { E } [ | g ( \eta ) - g ( \theta _ { X } \eta ) | \, | \, \eta ( B _ { n } ) \geq 1 ] \leq \mathbb { E } [ g _ { \varepsilon } ( \theta _ { X } \eta ) \, | \, \eta ( B _ { n } ) \geq 1 ]$$


<!-- p:98 -->


for sufficiently large n, where we have again used the fact that X ∈ B if η(B) ≥ 1. Applying (9.9) to gε we therefore obtain

$$\lim _ { n \to \infty } \sup _ { n \to \infty } \mathbb { E } [ | g ( \eta ) - g ( \theta _ { X } \eta ) | \, | \, \eta ( B _ { n } ) \geq 1 ] \leq \mathbb { E } [ g _ { s } ( \eta ^ { 0 } ) ] .$$

The assumption on g implies that gε(η0) → 0 as ε → 0, so that E[gε(η0)] → 0 by dominated convergence. This concludes the proof. □

### 9.4 Voronoi Tessellations and the Inversion Formula

In this section we shall assume that η is a stationary simple point process on Rd with finite intensity γ. We also assume that P(η(Rd) = 0) = 0, so that P(η(Rd) = ∞) = 1 by Proposition 8.4. In particular, γ &gt; 0. We shall discuss some basic relationships between the stationary distribution and the Palm distribution of η. For simplicity we assume for all ω ∈ Ω that η(ω) is a simple locally finite counting measure, that is η(ω) ∈ Nls := Nls(Rd); see Definition 6.6. As in the preceding section, we let η0 denote a Palm version of η.

In what follows we take advantage of the geometric idea of a Voronoi tessellation. For μ ∈ Nls with μ(Rd) &gt; 0 and for x ∈ Rd, let τ(x, μ) ∈ μ be the nearest neighbour of x in suppμ, i.e. the point in μ of minimal Euclidean distance from x. If there is more than one such point we take the lexicographically smallest. In the (exceptional) case μ(Rd) = 0 we put τ(x, μ) := x for all x ∈ Rd. The mapping τ: Rd × Nls → Rd is covariant under translations, that is,

$$\tau ( x - y , \theta _ { s } \mu ) = \tau ( x , \mu ) - y , \quad x , y \in \mathbb { R } ^ { d } , \, \mu \in \mathbb { N } _ { l s } .$$

For x ∈ μ ∈ Nls the Voronoi cell of x (with respect to μ) is defined by

$$C ( x , \mu ) \colon = \{ y \in \mathbb { R } ^ { d } \, \colon \tau ( y , \mu ) = x \} .$$

If μ(Rd) ≠ 0 these cells are pairwise disjoint and cover Rd; see Figure 9.1 for an illustration. In the following formulae we shall frequently use the abbreviation

$$C _ { 0 } \colon = C ( 0 , \eta ^ { 0 } ) .$$

This random set is also called the typical cell of the Voronoi tessellation. As before we denote by

$$X \coloneqq \tau ( 0 , \eta )$$

the point of η closest to the origin, and we set X := 0 if η(Rd) = 0.


<!-- p:99 -->


Figure 9.1 Voronoi tessellation based on a planar pattern of points. The dashed line connects the site x with its closest point.

τ(x)

o


0

o

Theorem 9.6 For all h ∈ R+(Rd × Nls) it is the case that

$$\mathbb { E } [ h ( X , \eta ) ] = \gamma \mathbb { E } \left [ \int _ { C _ { 0 } } h ( - x , \theta _ { x } \eta ^ { 0 } ) \, d x \right ] . \\$$

Proof Equation (9.6) (the refined Campbell theorem) and a change of variables yield

$$\mathbb { E } \left [ \int f ( x , \eta ) \, \eta ( d x ) \right ] = \gamma \, \mathbb { E } \left [ \int f ( - x , \theta _ { x } \eta ^ { 0 } ) \, d x \right ]$$

for all f ∈ R+(Rd × Nls). We apply this formula with

$$f ( x , \mu ) \colon = h ( x , \mu ) \mathbf 1 \{ \tau ( 0 , \mu ) = x \} .$$

Then the left-hand side of (9.15) reduces to the left-hand side of (9.14). Since, by the covariance property (9.11), τ(0, θxη0) = −x if and only if τ(x, η0) = 0 (that is, x ∈ C0), the right-hand side of (9.15) coincides with the right-hand side of (9.14). □

Let f ∈ R+(Nls). Taking h(x, μ) := f(μ) in (9.14) yields the inversion formula

$$\mathbb { E } [ f ( \eta ) ] = \gamma \mathbb { E } \left [ \int _ { C _ { 0 } } f ( \theta _ { x } \eta ^ { 0 } ) \, d x \right ] , \quad f \in \mathbb { R } _ { + } ( N _ { l s } ) ,$$

expressing the stationary distribution in terms of the Palm distribution. The choice f ≡ 1 yields the intuitively obvious formula

$$\mathbb { E } [ \lambda _ { d } ( C _ { 0 } ) ] = \gamma ^ { - 1 } .$$

Let g ∈ R+(Nls). Taking h(x, μ) := g(θxμ) in (9.14) yields

$$\gamma \mathbb { E } [ \lambda _ { d } ( C _ { 0 } ) g ( \eta ^ { 0 } ) ] = \mathbb { E } [ g ( \theta _ { x } \eta ) ] ,$$


<!-- p:100 -->


showing that the distribution of θxη is absolutely continuous with respect to the Palm distribution. The formula says that the stationary distribution is (up to a shift) a volume-biased version of the Palm distribution.

We define the (stationary) zero-cell of η by

$$V _ { 0 } \colon = C ( X , \eta ) = \{ x \in \mathbb { R } ^ { d } \, \colon \tau ( x , \eta ) = \tau ( 0 , \eta ) \} .$$

In the exceptional case where η(Rd) = 0, we have defined τ(x, μ) := x for all x ∈ Rd so that V0 = {0}. The next result shows that the Palm distribution can be derived from the stationary distribution by volume debiasing and shifting X to 0.

Proposition 9.7 We have for all f ∈ R+(Nls) that

$$\gamma \mathbb { E } [ f ( \eta ^ { 0 } ) ] = \mathbb { E } [ \lambda _ { d } ( V _ { 0 } ) ^ { - 1 } f ( \theta _ { X } \eta ) ] .$$

Proof We apply (9.19) with g(μ) := f(μ) · λd(C(0, μ))−1 to obtain

$$\gamma \mathbb { E } [ f ( \eta ^ { 0 } ) ] = \mathbb { E } [ \lambda _ { d } ( C ( 0 , \theta _ { X } \eta ) ) ^ { - 1 } f ( \theta _ { X } \eta ) ] .$$

Since C(0, θxη) = C(X, η) − X = V0 − X the result follows.

□

Given α ∈ R, putting f(μ) := λd(C(0, μ))a+1 in equation (9.20) yields

$$\gamma \mathbb { E } [ \lambda _ { d } ( C _ { 0 } ) ^ { \alpha + 1 } ] = \mathbb { E } [ \lambda _ { d } ( V _ { 0 } ) ^ { \alpha } ] .$$

In particular,

$$\mathbb { E } [ \lambda _ { d } ( V _ { 0 } ) ^ { - 1 } ] = \gamma .$$

By Jensen's inequality (Proposition B.1), E[λd(V0)−1] ≥ (E[λd(V0)])−1. Hence by (9.22) and (9.18) we obtain

$$\mathbb { E } [ \lambda _ { d } ( C _ { 0 } ) ] \leq \mathbb { E } [ \lambda _ { d } ( V _ { 0 } ) ] .$$

### 9.5 Exercises

Exercise 9.1 Let η be a stationary simple point process on Rd with positive finite intensity. Show that P0(Nls) = 1.

Exercise 9.2 Let η be a stationary simple point process with finite intensity and with P(η = 0) = 0. Let X be given by (9.13). Show that the conditional distribution of –X given θxη is the uniform distribution on V0 – X. (Hint: Use Theorem 9.6, then Proposition 9.7 and then again Theorem 9.6.)

Exercise 9.3 Let h ∈ R(Rd) be continuous with compact support. Show that x → ∫ h d(θxμ) is continuous for all μ ∈ Nts.


<!-- p:101 -->


Exercise 9.4 (Palm-Khinchin equations) Let η be a stationary simple p  =  = it t s  t t s   st t x ≥ 0 and j ∈ N0. Show that P-almost surely

$$1 \{ \eta ( 0 , x ] \leq j \} = \int 1 \{ t \leq 0 \} 1 \{ \eta ( t , x ] = j \} \, \eta ( d t ) .$$

Then use the refined Campbell theorem to prove that

$$\mathbb { P } ( \eta ( 0 , x ] \leq j ) = \gamma \, \left ( \sum _ { \substack { \mathbb { P } ( \eta ^ { 0 } ( 0 , t ] = j ) \, d t , \\ \, } } \eta ^ { 0 } ( 0 , t ] = j ) \, d t ,$$

where ηo has distribution P0.

Exercise 9.5 Let η be a stationary locally finite point process with finite positive intensity γ, and let A ∈ N1. Show that Pη(A) = 1 if and only if

$$\eta ( \{ x \in \mathbb { R } ^ { d } \colon \theta _ { x } \eta \notin A \} ) = 0 , \ \mathbb { P } \text {-a.s.}$$

(Hint: Use (9.4) to prove in the case Pη(A) = 1 that

$$\eta ( \{ x \in B \colon \theta _ { x } \eta \in A \} ) = \eta ( B ) , \quad \mathbb { P } \text {-a.s.} ,$$

for any B ∈ Bd with 0 &lt; λd(B) &lt; ∞.)

Exercise 9.6 Let η be a stationary simple point process with finite intensity γ. Let the sequence (B) be as in Proposition 8.11 and let X be a random vector such that X is the point of η in B whenever η(B) = 1. Let g ∈ R(N1) be bounded. Show that

lim E[g(θxn η) | η(Bn) = 1] = E[g(η0)]. n→∞

Exercise 9.7 In the setting of Exercise 9.6, assume that x → g(θxμ) is continuous for all μ ∈ Nls. Show that

$$\lim _ { n \to \infty } \mathbb { E } [ g ( \eta ) \, | \, \eta ( B _ { n } ) = 1 ] = \mathbb { E } [ g ( \eta ^ { 0 } ) ] .$$

(Hint: Use Exercise 9.6 and the proof of (9.10).)

Exercise 9.8 Let χ be the stationary Poisson cluster process defined in Exercise 8.2. Assume that γQ := ∫μ(Rd) Q(dμ) ∈ (0, ∞). Show that the Palm distribution of χ is given by

$$\mathbb { P } _ { \chi } ^ { 0 } = \int \mathbb { P } ( \chi + \mu \in \cdot ) \, \mathbb { Q } ^ { 0 } ( d \mu ) ,$$

where the probability measure Qo is given by

$$\mathbb { Q } ^ { 0 } \colon = \gamma _ { \mathbb { Q } } ^ { - 1 } \iint 1 \{ \theta _ { x } \mu \in \cdot \} \, \mu ( d x ) \, \mathbb { Q } ( d \mu ) .$$


<!-- p:102 -->


(Hint: Use the definition (5.12) of χ and the Mecke equation for ξ.)

Exercise 9.9 Let η be a stationary point process with finite positive intensity γ. Show that the reduced second factorial moment measure α2 of η (see Definition8.6) is given by

$$\alpha _ { 2 } ^ { ! } ( B ) = \gamma \int ( \mu ( B ) - 1 \{ 0 \in B \} ) \, \mathbb { P } _ { \eta } ^ { 0 } ( d \mu ) . \quad B \in \mathcal { B } ^ { d } .$$

Exercise 9.10 Let χ be a stationary Poisson cluster process as in Exercise 9.8. Show that the reduced second factorial moment measure α2 of χ is given by

$$\alpha _ { 2 } ^ { ! } ( B ) = \gamma _ { \chi } ^ { 2 } \lambda _ { d } ( B ) + \gamma \alpha _ { \mathbb { Q } } ^ { ! } ( B ) , \ \ B \in \mathcal { B } ^ { d } ,$$

where γχ := γγQ is the intensity of χ and the measure αQ on Rd is given by

$$\alpha _ { \mathbb { Q } } ^ { ! } ( B ) \colon = \iint \mu ( B + x ) \, \mu ( d x ) \, \mathbb { Q } ( d \mu ) - \gamma _ { \mathbb { Q } } 1 \{ 0 \in B \} .$$

(Hint: You may combine Exercises 9.8 and 9.9.)

Exercise 9.11 Let Q be a probability measure on N(Rd) such that γQ = ∫ μ(B) Q(dμ) &lt; ∞. Define a measure α by (9.24) and show that

$$\alpha _ { \mathbb { Q } } ^ { ! } ( B ) \coloneqq \iint 1 \{ y - x \in B \} \, \mu ^ { ( 2 ) } ( d ( x , y ) ) \, \mathbb { Q } ( d \mu ) , \quad B \in \mathcal { B } ^ { d } .$$

Exercise 9.12 Let χ be a stationary Poisson cluster process as in Exercise 9.8 but assume in addition that Q(Nts(Rd)) = 1. Assume that α is locally finite and absolutely continuous with respect to λa. Let ρQ denote the density. Show that the pair correlation function ρ2 of χ exists and can be chosen as ρ2 = 1 + γ−1γ−2ρQ. (As expected this function is at least one.)

Exercise 9.13 Suppose η has distribution Pη(A) = (1/2)IIγ(A), A ∈ Ni, and Pη({0}) = 1/2, where IIy is the distribution of a stationary Poisson process on Rd with intensity γ ∈ (0, ∞). Find the Palm distribution of η.


<!-- p:103 -->


## Extra Heads and Balanced Allocations

Is it possible to choose a point of a stationary Poisson process such that after removing this point and centring the process around its location (i.e. shifting so that this location goes to the origin) the resulting point process is still Poisson? More generally, one can ask whether it is possible to choose socer p- os st ons ser ss sos oes   ses a has the Palm distribution. This question can be answered using balanced allocations, which partition the space into regions of equal volume in a translation invariant way, such that each point is associated with exactly one region. Under an ergodicity assumption a spatial version of the Gale— Shapley algorithm of economics provides an important example of such an allocation. These results show that the Palm version of a stationary ergodic simple point process η can be constructed by a random shift of η.

### 10.1 The Extra Head Problem

Let d ∈ N. Throughout this chapter, η denotes a stationary simple point ro (∞ )    s   = (0 = o s p  ail from Section A.1 that the σ-field σ(η) generated by η consists of all sets {η ∈ A} with A ∈ N(Rd). Let T be a σ(η)-measurable random element of Rd such that P(η{T} = 1) = 1. Thus T picks one of the points of η using only the information contained in η. The shifted point process θτη (that is, the point process ω → θT(ω)η(ω)) has a point at the origin, and one might ask whether

$$\theta _ { T } \eta \stackrel { d } { = } \eta ^ { 0 } ,$$

where η0 is a Palm version of η, that is a point process with the Palm distribution P0, P0, as in Section 9.3. If η is a Poisson process, then the MeckeSlivnyak theorem (Theorem 9.4) shows that (10.1) is equivalent to

$$( 1 0 . 2 )$$


<!-- p:104 -->


This (as well as the more general version (10.1)) is known as the extra head problem. The terminology comes from the analogous discrete problem, given a doubly infinite sequence of independent and identically distributed coin tosses, of picking out a "head" in the sequence such that the distribution of the remaining coin tosses (centred around the picked coin) is still that of the original sequence. It turns out that the extra head problem can be solved using transport properties of point processes.

Before addressing the extra head problem we need to introduce a purely deterministic concept. It is convenient to add the point ∞ to Rd and to define Rd := Rd ∪ {∞}. We equip this space with the σ-field generated by Bd ∪ {{∞}}. We define ∞ + x = ∞ − x := ∞ for all x ∈ Rd. Recall from Definition 6.6 that Nls := Nts(Rd) is the space of all locally finite simple counting measures. Every μ ∈ Nls is identified with its support supp μ, defined at (8.4).

Definition 10.1 An allocation is a measurable mapping τ: Rd ×Nls → Rd such that

$$\tau ( x , \mu ) \in \mu \cup \{ \infty \} , \quad x \in \mathbb { R } ^ { d } , \, \mu \in N _ { l s } ,$$

and such that τ is covariant under shifts, i.e.

$$\tau ( x - y , \theta _ { s } \mu ) = \tau ( x , \mu ) - y , \quad x , y \in \mathbb { R } ^ { d } , \, \mu \in \mathbb { N } _ { l s } ,$$

where the shift operator θy was defined at (8.1).

Given an allocation τ, define

$$C ^ { \tau } ( x , \mu ) = \{ y \in \mathbb { R } ^ { d } \colon \tau ( y , \mu ) = x \} , \quad x \in \mathbb { R } ^ { d } , \, \mu \in \mathbb { N } _ { l s } .$$

Since τ(·, μ) is measurable for each μ ∈ Nls, the set C(x, μ) is Borel for each x ∈ μ. Note that C(x, μ) = ∅ whenever x ∉ μ and that {C(x, μ) : x ∈ μ} forms a partition of {x ∈ Rd : τ(x, μ) ≠ ∞}. The covariance property (10.3) implies that

$$C ^ { \tau } ( x - y , \theta _ { y } \mu ) = C ^ { \tau } ( x , \mu ) - y , \quad x , y \in \mathbb { R } ^ { d } , \, \mu \in \mathbb { N } _ { l s } .$$

An example is the Voronoi tessellation discussed in Chapter 9. In general we do not assume that x ∈ C(x, μ) or even that C(x, μ) ≠ ∅ for x ∈ μ.

Turning our attention back to the point process η, we may consider η as a random element of Nls. We can then assume that the Palm version η0 of η is a random element of Nts.


<!-- p:105 -->


Theorem 10.2 Let τ be an allocation and let f, g ∈ R+(Nts). Then

$$\mathbb { E } [ 1 \{ \tau ( 0 , \eta ) \neq \infty \} f ( \eta ) g ( \theta _ { \tau ( 0 , \eta ) } \eta ) ] = \gamma \, \mathbb { E } \left [ g ( \eta ^ { 0 } ) \int _ { C ^ { \tau ( 0 , \eta ^ { 0 } ) } } f ( \theta _ { x } \eta ^ { 0 } ) \, d x \right ] .$$

Proof The proof is similar to that of Theorem 9.6. Apply (9.15) (a direct consequence of the refined Campbell theorem) to the function (x, μ) → f(μ)g(θxμ)1{τ(0, μ) = x}. □

Definition 10.3 Let α &gt; 0. An allocation τ is said to be α-balanced for η if

$$\mathbb { P } ( \lambda _ { d } ( C ^ { \tau } ( x , \eta ) ) = \alpha \text { for all } x \in \eta ) = 1 .$$

Lemma 10.4 An allocation τ is α-balanced for η if and only if

$$\mathbb { P } ( \lambda _ { d } ( C ^ { \tau } ( 0 , \eta ^ { 0 } ) ) = \alpha ) = 1 .$$

Proof Because (x, y, μ) ↔ 1{τ(y, μ) = x} is a measurable mapping on Rd × Rd × Nls,

$$\lambda _ { d } ( C ^ { \tau } ( x , \mu ) ) = \int 1 \{ \tau ( y , \mu ) = x \} \, d y$$

depends measurably on (x, μ). Therefore Proposition 2.7 shows that the integral ∫ 1{λd(C(x, η)) ≠ α} η(dx) is a random variable. By (10.5) we have C(0, θxη) = C(x, η) − x for all x ∈ Rd. Therefore the refined Campbell theorem (Theorem 9.1) shows that

$$\mathbb { E } \left [ \int \mathbf 1 _ { \{ \lambda _ { d } ( C ^ { \tau } ( x , \eta ) ) \neq \alpha \} } \eta ( d x ) \right ] & = \mathbb { E } \left [ \int \mathbf 1 _ { \{ \lambda _ { d } ( C ^ { \tau } ( 0 , \theta _ { x } \eta ) ) \neq \alpha \} } \eta ( d x ) \right ] \\ & = \gamma \int \mathbb { P } ( \lambda _ { d } ( C ^ { \tau } ( 0 , \eta ^ { 0 } ) ) \neq \alpha ) \, d x ,$$

and the result follows.

□

The following theorem clarifies the relevance of balanced allocations for the extra head problem.

Theorem 10.5 Let α &gt; 0. Let τ be an allocation and put T := τ(0, η). Then τ is α-balanced for η if and only if

$$\mathbb { P } ( T \ne \infty ) = \alpha \gamma$$

$$\mathbb { P } ( \theta _ { T } \eta \in \cdot \, | \, T \neq \infty ) = \mathbb { P } _ { \eta } ^ { 0 } .$$

and Proof If τ is α-balanced for η, then (10.6) with f ≡ 1 yields


<!-- p:106 -->


$$\mathbb { E } [ 1 \{ T \neq \infty \} g ( \theta _ { T } \eta ) ] = \gamma \alpha \, \mathbb { E } [ g ( \eta ^ { 0 } ) ] .$$

This yields both (10.9) and (10.10). Assume, conversely, that (10.9) and (10.10) hold. Let C0 := C(0, η0). Using (10.6) with f ≡ 1 followed by a multiplication by P(T &lt; ∞)−1 gives us

$$\mathbb { E } [ g ( \eta ^ { 0 } ) ] = \mathbb { P } ( T \neq \infty ) ^ { - 1 } \gamma \, \mathbb { E } [ g ( \eta ^ { 0 } ) \lambda _ { d } ( C _ { 0 } ) ] = \alpha ^ { - 1 } \mathbb { E } [ g ( \eta ^ { 0 } ) \lambda _ { d } ( C _ { 0 } ) ] .$$

In particular, E[λd(C0)] = α. Choosing g(μ) = λd(C(O, μ)) yields

$$\mathbb { E } [ \lambda _ { d } ( C _ { 0 } ) ^ { 2 } ] = \alpha \, \mathbb { E } [ \lambda _ { d } ( C _ { 0 } ) ] = \alpha ^ { 2 } .$$

Since this implies (10.8), τ is α-balanced for η.

□

Theorem 10.5 shows that for α = γ−1 a solution to the extra head problem (10.1) may be obtained from an α-balanced allocation if one exists.

### 10.2 The Point-Optimal Gale-Shapley Algorithm

The identity (10.9) shows that α-balanced allocations can exist only if α ≤ γ−1. The extra head problem arises in the case α = γ−1.

We now describe one way to construct α-balanced allocations. Suppose that each point of μ ∈ Nls starts growing at time 0 at unit speed, trying to capture a region of volume α. In the absence of any interaction with other a point x ∈ μ grows to a ball B(x, t) by time t, where

$$B ( x , t ) \colon = \{ y \in \mathbb { R } ^ { d } \colon \| y - x \| \leq t \}$$

and where we recall that κd = λa(B(x, 1)). However, a growing point can only capture sites that have not been claimed by some other point before. Once a region reaches volume α, it stops growing. This idea is formalised as follows.

Algorithm 10.6 Let α &gt; 0 and μ ∈ Nls. For n ∈ N, x ∈ μ and z ∈ Rd, define the sets C(x) ⊂ Rd (in words, the set of sites claimed by x at stage n), R(x) ⊂ Rd (the set of sites rejecting x during the first n stages) and A(z) ⊂ μ (the set of points of μ claiming site z in the first n stages) via the following recursion. Define R0(x) := 0 for all x ∈ μ and for n ∈ N:

###### (i) For x ∈ μ, define

$$r _ { n } ( x ) \colon = \inf \{ r \geq 0 \, \colon \lambda _ { d } ( B ( x , r ) \ \ R _ { n - 1 } ( x ) ) \geq \alpha \} ,$$

$$C _ { n } ( x ) \colon = B ( x , r _ { n } ( x ) ) .$$


<!-- p:107 -->


- (ii) For z ∈ Rd, define

$$A _ { n } ( z ) \colon = \{ x \in \mu \, \colon z \in C _ { n } ( x ) \} .$$

If A(z) ≠ ∅ then define

$$\tau _ { n } ( z ) \colon = l ( \{ x \in A _ { n } ( z ) \, \colon \| z - x \| = d ( z , A _ { n } ( z ) ) \} )$$

as the point shortlisted by site z at stage n, where l(B) denotes the lexicographic minimum of a finite non-empty set B ⊂ Rd and where d(·, ·) is defined by (A.21). If An(z) = ∅ then define τn(z) := ∞.

- (iii) For x ∈ μ, define

$$R _ { n } ( x ) \colon = \{ z \in C _ { n } ( x ) \, \colon \tau _ { n } ( z ) \neq x \} .$$

The point-optimal Gale-Shapley allocation with appetite α is denoted τα,P and defined as follows. (The superscript p stands for "point-optimal".) Consider Algorithm 10.6 for μ ∈ Nls and let z ∈ Rd. If τ(z) = ∞ (that is, An(z) = ∅) for all n ∈ N we put τα,P(μ, z) := ∞. Otherwise, set τα,P(μ, z) := lim→∞ τ(z). We argue as follows that this limit exists. Defining r0(x) := 0 for all x ∈ μ, we assert that for all n ∈ N the following holds:

$$r _ { n } ( x ) \geq r _ { n - 1 } ( x ) , \ \ x \in \mu ,$$

$$A _ { n } ( z ) \supset A _ { n - 1 } ( z ) , \ \ z \in \mathbb { R } ^ { d } ,$$

$$R _ { n } ( x ) \supset R _ { n - 1 } ( x ) , \ \ x \in \mu .$$

)  (10) s 1)  os  o  ) implies (10.14), while (10.14) implies that (10.12) holds for the next value of n. By (10.13), ∥|τn(z) − z is decreasing in n, and hence, since μ is locally finite, there exist x ∈ μ and n0 ∈ N such that τ(z) = x for all n ≥ n0. In this case we define τα,P(z, μ) := x.

We have used the lexicographic minimum in (ii) to break ties in a shiftcovariant way. An alternative is to leave τ(z) undefined whenever z has the same distance from two different points of μ. We shall prove that τaP has the following properties.

Definition 10.7 Let α ∈ (0, ∞). An allocation τ is said to have appetite α &gt; 0 if both

$$\lambda _ { d } ( C ^ { \tau } ( x , \mu ) ) \leq \alpha , \ \ x \in \mu , \, \mu \in N _ { l s } ,$$

and there is no μ ∈ Nls satisfying

$$\{ z \in \mathbb { R } ^ { d } \colon \tau ( z , \mu ) = \infty \} \neq \emptyset \quad \text {and} \quad \{ x \in \mu \colon \lambda _ { d } ( C ^ { \tau } ( x , \mu ) ) < \alpha \} \neq \emptyset . \ ( 1 0 . 1 6 )$$


<!-- p:108 -->


Lemma 10.8 The point-optimal Gale-Shapley allocation τα,p is an allocation with appetite α.

Proof It follows by induction over the stages of Algorithm 10.6 that the mappings τ are measurable as a function of both z and μ. (The proof of this fact is left to the reader.) Hence τa,P is measurable. Moreover it is clear that τα,P has the covariance property (10.3). Upon defining τα,P we noted that for each z ∈ Rd, either τα,P(z, μ) = ∞ or τn(z) = x for some x ∈ μ and all sufficiently large n ∈ N. Therefore

$$1 \{ \tau ^ { \alpha , p } ( z , \mu ) = x \} = \lim _ { n \to \infty } 1 \{ z \in C _ { n } ( x ) \ \vee \ R _ { n - 1 } ( x ) \} , \quad z \in \mathbb { R } ^ { d } .$$

On the other hand, by Algorithm 10.6(i) we have λd(C(x) \ R−1(x)) ≤ α, so that (10.15) follows from Fatou's lemma (Lemma A.7).

Assume the strict inequality λd(CTM*p (x, μ)) &lt; α for some x ∈ μ. We assert that the radii rn(x) defined in step (i) of the algorithm diverge. To see this, suppose on the contrary that r(x) := lim→∞ rn(x) &lt; ∞. By (10.17) there exist n0 ∈ N and α1 &lt; α such that λd(B(x, rn(x)) \ Rn−1(x)) ≤ α1 for n ≥ n0. Hence there exists α2 ∈ (α1, α) such that λd(B(x, r(x)) \ R−1(x)) ≤ α2 for n ≥ n0, implying the contradiction rn+1(x) &gt; r(x) for n ≥ n0. Now taking z ∈ Rd, we hence have z ∈ C(x) for some n ≥ 1, so that z shortlists either x or some closer point of μ. In either case, τ(μ, z) ≠ ∞. □

### 10.3 Existence of Balanced Allocations

We now return to the stationary point process η. Under an additional hypothesis on η we shall prove that any allocation with appetite α ≤ γ−1 (and in particular the Gale-Shapley allocation) is α-balanced for η. To formulate this condition, recall the definitions (8.13) and (8.15) of the invariant σ-fields I and I η. We say that η is pseudo-ergodic if

$$\mathbb { E } [ \eta ( [ 0 , 1 ] ^ { d } ) \, | \, \mathcal { I } _ { \eta } ] = \gamma , \quad \mathbb { P } ^ { a . s . }$$

Every ergodic point process is pseudo-ergodic. Exercise 10.10 shows that the converse of this statement does not hold. If (10.18) holds then Exercise 8.11 shows that

$$\mathbb { E } [ \eta ( B ) \, | \, \mathcal { I } _ { \eta } ] = \gamma \lambda _ { d } ( B ) , \quad \mathbb { P } { \text {-a.s.} } , \, B \in \mathcal { B } ^ { d } .$$

Theorem 10.9 Assume that η is pseudo-ergodic and let τ be an allocation with appetite α ∈ (0, γ−1]. Then τ is α-balanced for η.

Proof Let A be the set of all μ ∈ Nls with {x ∈ μ : λd(C(x, μ)) &lt; α} ≠ ∅.


<!-- p:109 -->


Then A ∈ I by (10.5). In view of (10.16) we obtain from Theorem 10.2 that

P(η ∈ A) = P(τ(0, η) ≠ ∞, η ∈ A) = γ E[1{η0 ∈ A}λd(C(0, η0))].

Therefore by (9.5), for all B ∈ Bd with 0 &lt; λd(B) &lt; ∞, we have

$$\mathbb { P } ( \eta \in A ) & = \lambda _ { d } ( B ) ^ { - 1 } \mathbb { E } \left [ \int _ { B } \mathbf 1 _ { \{ \theta _ { x } \eta \in A \} \lambda _ { d } ( C ^ { \tau } ( 0 , \theta _ { x } \eta ) ) \, \eta ( d x ) \right ] \\ & = \lambda _ { d } ( B ) ^ { - 1 } \mathbb { E } \left [ \mathbf 1 _ { \{ \eta \in A \} } \int _ { B } \lambda _ { d } ( C ^ { \tau } ( x , \eta ) ) \, \eta ( d x ) \right ] , \quad ( 1 0 . 2 0 ) \\$$

where we have used the invariance of A under translations and (10.5). Using (10.15), this yields

$$\mathbb { P } ( \eta \in A ) & \leq \lambda _ { d } ( B ) ^ { - 1 } \alpha \mathbb { E } [ 1 \{ \eta \in A \} \eta ( B ) ] \\ & = \lambda _ { d } ( B ) ^ { - 1 } \alpha \mathbb { E } [ 1 \{ \eta \in A \} \mathbb { E } [ \eta ( B ) \ | \ \mathcal { I } _ { \eta } ] ] \\ & = \alpha \gamma \mathbb { P } ( \eta \in A ) \leq \mathbb { P } ( \eta \in A ) ,$$

where we have used (10.19) (a consequence of assumption (10.18)) and the assumption that α ≤ γ−1. Therefore inequality (10.21) is in fact an equality, so that, by (10.21) and (10.20),

$$\mathbb { E } \left [ 1 \{ \eta \in A \} \int _ { B } ( \alpha - \lambda _ { d } ( C ^ { \tau } ( x , \eta ) ) ) \, \eta ( d x ) \right ] = 0 .$$

Taking B ↑ Rd, this yields

$$1 \{ \eta \in A \} \int ( \alpha - \lambda _ { d } ( C ^ { \tau } ( x , \eta ) ) ) \, \eta ( d x ) = 0 , \quad \mathbb { P } \text {-a.s.}$$

Hence λd(C(x, η(ω))) = α for all x ∈ η(ω) for P-a.e. ω ∈ {η ∈ A}. By definition of A this is possible only if P(η ∈ A) = 0. Hence τ is α-balanced for η. □

Corollary 10.10 There is an allocation that is γ−1-balanced for η if and only if η is pseudo-ergodic. In this case the point-optimal Gale-Shapley allocation τγ−1p is one possible choice.

Proof If (10.18) holds, then by Theorem 10.9 and Lemma 10.8 the allocation τo−1,p is γ−1-balanced. For the converse implication, suppose that τ is an allocation that is γ−1-balanced for η. Then for each B ∈ Bd we have almost surely that

$$\gamma \int 1 \{ \tau ( z , \eta ) \in B \} \, d z = \gamma \sum _ { x \in \eta } \int 1 \{ \tau ( z , \eta ) = x , x \in B \} \, d z = \eta ( B ) .$$


<!-- p:110 -->


Taking A ∈ I (so that {θzη ∈ A} = {η ∈ A}) and using the shift-covariance property (10.3), we obtain

$$\mathbb { P } ( \Phi _ { \ } y ) ( \Phi _ { \ } z ) , & = \mathbb { C } _ { \ } z \mathbb { X } \int 1 \{ \theta _ { z } \eta \in A , \tau ( 0 , \theta _ { z } \eta ) + z \in B \} \, d z \right ] \\ \mathbb { E } [ 1 \{ \eta \in A \} \eta ( B ) ] & = \gamma \mathbb { E } \left [ \int 1 \{ \theta _ { z } \eta \in A , \tau ( 0 , \eta ) + z \in B \} \, d z \right ] = \gamma \mathbb { P } ( A ) \lambda _ { d } ( B ) ,$$

where we have used Fubini's theorem and stationarity to get the last two identities. This proves (10.18). □

By Proposition 8.13 the next corollary applies in particular to a stationary Poisson process.

Corollary 10.11 Suppose that the point process η is ergodic. Then the point-optimal Gale-Shapley allocation τγ−1,p provides a solution of the general extra head problem (10.1).

Proof Condition (10.18) follows by ergodicity. Then by Lemma 10.8 and Theorem 10.9 the allocation τγ−1,p is γ−1-balanced, and then by Theorem 10.5 we have (10.1) for T = τ(0, η). □

### 10.4 Allocations with Large Appetite

Let the point process η and the constant γ ∈ (0, ∞) be as before. If τ is an l   = (∞ ≠ (l   − =  dn n 0.m and (10.9). The following result shows that this remains true for α &gt; γ−1.

Proposition 10.12 Assume that η is pseudo-ergodic and let τ be an allocation with appetite α ≥ γ−1. Then P(τ(0, η) ≠ ∞) = 1 and

$$\mathbb { E } [ \lambda _ { d } ( C ^ { \tau } ( 0 , \eta ^ { 0 } ) ) ] = \gamma ^ { - 1 } .$$

If α &gt; γ−1, then P-a.s. there are infinitely many points x ∈ η with the property λd(C(x, η)) &lt; α.

Proof Let A′ ∈ I. Applying (10.6) with f ≡ 1 and g = 1A yields

$$\mathbb { P } ( \eta \in A ^ { \prime } , \tau ( 0 , \eta ) \neq \infty ) = \gamma \mathbb { E } [ \{ \eta ^ { 0 } \in A ^ { \prime } \} \lambda _ { d } ( C ^ { \tau } ( 0 , \eta ^ { 0 } ) ) ] .$$

Among other things, this implies (10.22) once we have proved the first assertion. Since A' is translation invariant it follows from the definition (9.3) of P0 and the definition (8.15) of I η that η

$$\mathbb { P } ( \eta ^ { 0 } \in A ^ { \prime } ) & = \gamma ^ { - 1 } \mathbb { E } [ 1 \{ \eta \in A ^ { \prime } \} \eta ( [ 0 , 1 ] ^ { d } ) ] \\ & = \gamma ^ { - 1 } \mathbb { E } [ 1 \{ \eta \in A ^ { \prime } \} \mathbb { E } [ \eta ( [ 0 , 1 ] ^ { d } ) \ | \ I _ { \eta } ] ] = \mathbb { P } ( \eta \in A ^ { \prime } ) ,$$


<!-- p:111 -->


where we have used assumption (10.18). The identity (10.23) can hence be written as

$$\gamma \mathbb { E } [ 1 \{ \eta ^ { 0 } \in A ^ { \prime } \} ( \alpha - \lambda _ { d } ( C ^ { \tau } ( 0 , \eta ^ { 0 } ) ) ) ] - \mathbb { P } ( \eta \in A ^ { \prime } , \tau ( 0 , \eta ) = \infty ) \\ = ( \gamma \alpha - 1 ) \, \mathbb { P } ( \eta \in A ^ { \prime } ) . \quad ( 1 0 . 2 5 )$$

We now choose A′ as the set of all μ ∈ Nls with ∫ 1{τ(x, μ) = ∞} dx &gt; 0. It is easy to check that A' ∈ I. By Fubini's theorem, invariance of A', stationarity and the covariance property (10.3),

$$\mathbb { B } \left [ 1 \{ \eta \in A ^ { \prime } \} \int 1 \{ \tau ( x , \eta ) = \infty \} \, d x \right ] & = \int \mathbb { P } ( \theta _ { x } \eta \in A ^ { \prime } , \tau ( x , \eta ) = \infty ) \, d x \\ & = \int \mathbb { P } ( \eta \in A ^ { \prime } , \tau ( 0 , \eta ) = \infty ) \, d x .$$

Assuming P(η ∈ A′) &gt; 0, this yields P(η ∈ A′, τ(0, η) = ∞) &gt; 0. Let A ∈ I be defined as in the proof of Theorem 10.9. Definition 10.7 shows that A' ⊂ Nls \ A, so that the first term on the left-hand side of (10.25) vanishes. Since this contradicts our assumption yα – 1 ≥ 0, we must have P(η ∈ A') = 0, and hence

$$0 = \mathbb { E } \left [ \int \mathbf 1 \{ \tau ( x , \eta ) = \infty \} \, d x \right ] & = \int \mathbb { P } ( \tau ( x , \eta ) = \infty ) \, d x \\ & = \int \mathbb { P } ( \tau ( 0 , \eta ) = \infty ) \, d x ,$$

where the last line comes from the covariance property and stationarity. Hence we have the first assertion of the proposition.

Assume, finally, that α &gt; γ−1 and consider the point process

$$\eta ^ { \prime } \coloneqq \int \mathbf 1 \{ x \in \cdot , \lambda _ { d } ( C ^ { \tau } ( x , \eta ) ) < \alpha \} \, \eta ( d x ) .$$

Since λd is translation invariant it follows that η' is stationary. In view of Proposition 8.4 we need to show that P(η' = 0) = 0. Let A' be the set of all μ ∈ Nls such that μ({x ∈ Rd : λd(C(x, μ)) &lt; α}) = 0. Then A′ ∈ I and {η′ = 0} = {η ∈ A′}. Since τ has appetite α, we have

$$\mathbb { E } [ \mathbf 1 \{ \eta ^ { 0 } \in A ^ { \prime } \} \lambda _ { d } ( C ^ { \tau } ( 0 , \eta ^ { 0 } ) ) ] = \alpha \, \mathbb { P } ( \eta ^ { 0 } \in A ^ { \prime } ) = \alpha \, \mathbb { P } ( \eta \in A ^ { \prime } ) ,$$

where we have used (10.24). Hence we obtain from (10.23) and the first assertion that P(η ∈ A′) = γα P(η ∈ A'). This shows that P(η ∈ A') = 0. □


<!-- p:112 -->


where

$$\mathbb { P } _ { \eta } ^ { * } \colon = \mathbb { E } \left [ \hat { \eta } ^ { - 1 } \int \mathbf 1 \{ x \in [ 0 , 1 ] ^ { d } , \theta _ { x } \eta \in \cdot \} \, \eta ( d x ) \right ]$$

is the modified Palm distribution of η. This distribution describes the statistical behaviour of η as seen from a randomly chosen point of η. For a pseudo-ergodic point process it coincides with the Palm distribution P0. η We do not give further details.

### 10.6 Exercises

Exercise 10.1 Let (Y, y, Q) be an s-finite measure space and suppose that ξ is a Poisson process on Rd ×Y with intensity measure γλd⊗Q. Show that θxξ ≡ ξ for all x ∈ Rd, where θx : N(Rd × Y) → N(Rd × Y) is the measurable mapping (shift) defined by

$$\vartheta _ { x } \mu \colon = \int 1 \{ ( x ^ { \prime } - x , y ) \in \cdot \} \, \mu ( d ( x ^ { \prime } , y ) ) .$$

Assume in addition that Y is a CSMS and that Q is locally finite. Show that ξ has the mixing property

$$\lim _ { \| x \| \to \infty } \mathbb { P } ( \xi \in A , \vartheta _ { x } \xi \in A ^ { \prime } ) = \mathbb { P } ( \xi \in A ) \mathbb { P } ( \xi \in A ^ { \prime } )$$

for all A, A' ∈ N(Rd ×Y). (Hint: The proof of Proposition 8.13 applies with a more general version of Proposition 8.12.)

### 10.5 The Modified Palm Distribution

Corollary 10.10 and Theorem 10.5 show that the extra head problem (10.1) can only be solved under the assumption (10.18). To indicate what happens without this assumption we recall the definition (8.21) of the sample intensity η of η. We assume that P(0 &lt; η &lt; ∞) = 1 and say that an allocation τ is balanced for η if

$$\mathbb { P } ( \lambda _ { d } ( C ^ { \tau } ( x , \eta ) ) = \hat { \eta } ^ { - 1 } \text { for all } x \in \eta ) = 1 .$$

It is possible to generalise the proof of Theorem 10.9 so as to show that balanced allocations exist without further assumptions on η. (The idea is to use allocations with a random appetite η−1.) If τ is such a balanced allocation and T := τ(η, O), then one can show that

$$\mathbb { P } ( \theta _ { T } \in \cdot ) = \mathbb { P } _ { \eta } ^ { * } ,$$


<!-- p:113 -->


Exercise 10.2 Let η be a stationary Poisson process on R and let X ∈ η be the point of η closest to the origin. Show that θxη \ δ0 is not a Poisson process. (Hint: Use Exercise 7.9 and Theorem 7.2 (the interval theorem).)

Exercise 10.3 Extend the assertion of Exercise 10.2 to arbitrary dimensions.

Exercise 10.4 Prove the analogue of Theorem 9.6 for a general allocation, defining C0 as the set of sites allocated to 0.

Exercise 10.5 Formulate and prove a generalisation of Proposition 9.7 and its consequence (9.21) to an arbitrary allocation τ. (Hint: Use Exercise 10.4.)

Exercise 10.6 Assume that η is pseudo-ergodic and let τ be an allocation with appetite α ≤ γ−1. Let g ∈ R+(Nls). Show that

E[1{τ(0, η) ≠ ∞}g(θτ(0,η)η)] = γα E[g(η0)].

(Hint: Use Theorems 10.5 and 10.9.)

Exercise 10.7 Assume that η is pseudo-ergodic and let τ be an allocation with appetite α &lt; γ−1. Show that P(τ(0, η) = ∞) &gt; 0. (Hint: Take in Exercise 10.6 the function g as the indicator function of all μ ∈ Nls satisfying ∫ 1{τ(x, μ) = ∞} dx = 0 and use (10.24).)

Exercise 10.8 Let η be a stationary locally finite point process on Rd such that P(0 &lt; η &lt; ∞) = 1, where η is given by (8.21). Define the modified invariant σ-field I, defined by (8.13).

Exercise 10.9 Let the point process η be as in Exercise 10.8. Show that there exists g ∈ R+(Nl) satisfying g(θxμ) = g(μ) for all (x, μ) ∈ Rd × Nl continuous with respect to the Palm distribution P0 of η with density γg. η (Hint: Apply the refined Campbell theorem to prove the second assertion.)

Exercise 10.10 For t ≥ 0 let ηt be a stationary Poisson process on Rd with intensity t. Let y ∈ Rd \ {0} and show that η′ := η1 + θyη1 is stationary. Let X be a {0, 1}-valued random variable and assume that η1, η2, X are independent. Show that η := 1{X = 0}η′ + 1{X = 1}η2 is stationary and pseudo-ergodic. Show also that η is not ergodic unless X is deterministic.


<!-- p:114 -->


## Stable Allocations

In the Gale-Shapley allocation introduced in Chapter 10, the idea is that points and sites both prefer to be allocated as close as possible. As a result there is no point and no site that prefer each other over their current partners. This property is called stability. Stable allocations are essentially unique. To prove this, it is useful to introduce a site-optimal version of the Gale-Shapley algorithm.

### 11.1 Stability

Let d ∈ N. Recall that Nls = Nls(Rd) is the space of all locally finite simple counting measures on Rd and that we identify each μ ∈ Nls with its support. We start by defining the key concept of this chapter.

Definition 11.1 Let τ be an allocation with appetite α &gt; 0. Let μ ∈ Nls, x ∈ μ and z ∈ Rd. We say the site z desires x if ∥z − x|| &lt; ∥z − τ(z, μ)||, where l|∞∥| := ∞. We say the point x covets z if

$$\| x - z \| < \| x - z ^ { \prime } \| \, \text { for some } z ^ { \prime } \in C ^ { \tau } ( x , \mu ) , \, \text { or } \lambda _ { d } ( C ^ { \tau } ( x , \mu ) ) < \alpha .$$

The pair (z, x) is said to be unstable (for μ and with respect to τ) if z desires x and x covets z. The allocation τ is said to be stable if there is no μ with an unstable pair.

Lemma 11.2 The point-optimal Gale-Shapley allocation with appetite α &gt; 0 is stable.

Proof Take μ ∈ Nls, x ∈ μ and z ∈ Rd. Consider Algorithm 10.6. If z desires x, then z ∉ C(x) for all n ≥ 1. But if x covets z, then z ∈ C(x) for some n ≥ 1. (Note that if λd(CαP (x, μ)) &lt; α then the radii rn(x) diverge, as explained in the proof of Lemma 10.8.) Therefore (z, x) cannot be an unstable pair. □


<!-- p:115 -->


### 11.2 The Site-Optimal Gale-Shapley Allocation

Our goal is to prove that stable allocations are essentially uniquely determined. To achieve this goal, it is helpful to introduce the site-optimal Gale-Shapley allocation.

Algorithm 11.3 Let α &gt; 0 and μ ∈ Nls. For n ∈ N, x ∈ μ and z ∈ Rd, define the point τ(x) ∈ μ ∪ {∞} (in words, the point claimed by z at stage n) and define the sets R(z) ⊂ μ (the set of points rejecting x during the first n stages), A(x) ⊂ Rd (the set of sites claiming point x at stage n) and S(x) ⊂ Rd (the set of sites shortlisted by x at stage n) via the following recursion. Define R0(z) := 0 for all z ∈ Rd and take n ∈ N.

- (i) For z ∈ Rd, define

$$\tau _ { n } ( z ) \colon = \begin{cases} l ( \{ x \in \mu \colon \| z - x \| = d ( z , \mu \ \ R _ { n - 1 } ( z ) ) \} ) , & \text {if } \mu \ \ R _ { n - 1 } ( z ) \neq \emptyset , \\ \infty , & \text {otherwise.} \end{cases}$$

- (ii) For x ∈ μ, define (recall the convention inf ∅ := ∞)

$$A _ { n } ( x ) & \colon = \{ z \in \mathbb { R } ^ { d } \colon \tau _ { n } ( z ) = x \} , \\ r _ { n } ( x ) & \colon = \inf \{ r \geq 0 \colon \lambda _ { d } ( B ( x , r ) \cap A _ { n } ( x ) ) \geq \alpha \} , \\ S _ { n } ( x ) & \colon = A _ { n } ( x ) \cap B ( x , r _ { n } ( x ) ) .$$

- (iii) For z ∈ Rd let Rn(z) := Rn−1(z)∪{x} if τn(z) = χ ∈ μ and z ∉ B(x, rn(x)). Otherwise define R(z) := R−1(z).

Given α &gt; 0, the site-optimal Gale-Shapley allocation τa,s with appetite α is defined as follows. (The superscript s stands for "site-optimal".) Let μ ∈ Nls and consider Algorithm 11.3. For z ∈ Rd there are two cases. In the first case z is rejected by every point, that is μ = Ux=1R(z). Then we define τα,s(z) := ∞. In the second case there exist x ∈ μ and n0 ∈ N such that z ∈ S (x) for all n ≥ n0. In this case we define τα,s(z, μ) := x.

The following lemma shows that τα,s has properties similar to those of the point-optimal version. The proof can be given as before and is left to the reader.

Lemma 11.4 The site-optimal Gale-Shapley allocation τα,s is a stable allocation with appetite α.

### 11.3 Optimality of the Gale-Shapley Algorithms

In this section we prove some optimality properties of the Gale-Shapley allocations. They are key to the forthcoming proof of the uniqueness of stable allocations. We start with two lemmas. We say that a site x ∈ Rd is normal for μ ∈ Nls if the distances from x to the points of μ are all distinct. Note that λa-almost all sites have this property.


<!-- p:116 -->


Lemma 11.5 Let τ be a stable allocation with appetite α &gt; 0 and let μ ∈ Nls. Then for λd-a.e. z with τ(z, μ) ≠ ∞, the point τ(z, μ) does not reject z in the site-optimal Gale-Shapley algorithm for μ. In particular,

$$\| \tau ^ { \alpha , s } ( z , \mu ) - z \| \leq \| \tau ( z , \mu ) - z \| , \quad \lambda _ { d } \bar { \ } a . e . \ z .$$

Proof For each n ∈ N we need to show that for λd-a.e. z with τ(z, μ) ≠ ∞, the point τ(z, μ) does not reject z in the first n stages of the site-optimal Gale-Shapley algorithm. We do this by induction on n. For n = 1 let us assume the opposite. Then there exist x ∈ μ and a measurable set

$$R _ { 1 } \subset C ^ { \tau } ( x , \mu ) \cap ( A _ { 1 } ( x ) \ \ B ( x , r _ { 1 } ( x ) ) )$$

with λd(R1) &gt; 0. Then S1 := S1(x) = A1(x) ∩ B(x, r1(x)) satisfies λd(S1) = α. Since R1 ∩ S1 = ∅ we obtain for the set T1 := S1 \ Cτ(x, μ) that

$$\lambda _ { d } ( T _ { 1 } ) & = \lambda _ { d } ( S _ { 1 } \ \langle \, ( C ^ { \tau } ( x , \mu ) \ \ R _ { 1 } ) \, ) \geq \lambda _ { d } ( S _ { 1 } ) - \lambda _ { d } ( C ^ { \tau } ( x , \mu ) \ \ R _ { 1 } ) \\ & = \alpha - \lambda _ { d } ( C ^ { \tau } ( x , \mu ) ) + \lambda _ { d } ( R _ { 1 } ) > 0 ,$$

where we have used that λa(C(x, μ)) ≤ α. Therefore we can pick normal z ∈ T1 and z′ ∈ R1. Then τ(z, μ) ≠ x, but x is the closest point of μ to z (since z ∈ S1) so z desires x. Also |z − x|| ≤ r1(x) &lt; ∥|z′ − x|| so x covets z. This contradicts the assumed stability of τ.

For the induction step we let n ∈ N and assume, for λa-a.e. z with τ(z, μ) ≠ ∞, that the point τ(z, μ) does not reject z in the first n stages of the site-optimal Gale-Shapley algorithm. To show that this is also true for n + 1 in place of n we assume the opposite. Then there exist x ∈ μ and a measurable set

$$R \subset C ^ { \tau } ( x , \mu ) \cap ( A _ { n + 1 } ( x ) \ \ B ( x , r _ { n + 1 } ( x ) ) )$$

with λd(R) &gt; 0. Then S := Sn+1(x) = An+1(x) ∩ B(x, rn+1(x)) satisfies λa(S) = α and every site in S is closer to x than every site in R is to x. As before we obtain the fact that T := S \ C(x, μ) satisfies λd(T) &gt; 0. A site z ∈ S ⊃ T claims x in stage n + 1 of the algorithm. Therefore z must have been rejected by all closer points of μ in one of the first n stages. Combining this with τ(z, μ) ≠ x for z ∈ T and with the induction hypothesis shows that ∥|τ(z, μ) − z|| &gt; ∥|x − z| for λd-a.e. z ∈ T. As we have already seen this contradicts the stability of τ.


<!-- p:117 -->


The final assertion follows upon noting that a normal site z is allocated in τα,s to the closest point in μ which does not reject it. □

The proof of the following lemma is similar to the preceding one and is left as an exercise; see Exercise 11.5.

Lemma 11.6 Let τ be a stable allocation with appetite α &gt; 0. Let μ ∈ Nls. Then for λd-a.e. z with τ(z, μ) ≠ ∞, the site z never rejects τ(z, μ) in the point-optimal Gale-Shapley algorithm for μ.

Given an allocation τ, we define functions gr, hτ : Rd × Nls × R+ → R+ by

$$g _ { \tau } ( z , \mu , r ) \colon = 1 \{ \| \tau ( z , \mu ) - z \| \leq r \} ,$$

$$h _ { \tau } ( x , \mu , r ) \colon = \lambda _ { d } ( C ^ { \tau } ( x , \mu ) \cap B ( x , r ) ) ,$$

where B(x, ∞) := Rd and ∥∞∥ := ∞. In a sense these functions describe the quality of the allocation for a site z ∈ Ra or a point x ∈ μ, respectively.

Proposition 11.7 Let τ be a stable allocation with appetite α &gt; 0. Let μ ∈ Nls and r ∈ R+. Then

$$g _ { \tau ^ { o , s } } ( z , \mu , r ) \geq g _ { \tau } ( z , \mu , r ) \geq g _ { \tau ^ { o , p } } ( z , \mu , r ) , \quad \lambda _ { d } \bar { a } . e . \ z ,$$

$$h _ { \tau ^ { \alpha , \mathbb { P } } } ( x , \mu , r ) \geq h _ { \tau } ( x , \mu , r ) \geq h _ { \tau ^ { \alpha , s } } ( x , \mu , r ) , \quad x \in \mu .$$

Proof By (11.1) the first inequality of (11.2) holds for λd-a.e. z ∈ Rd.

Now we prove the first inequality in (11.3). Assume the contrary, so that there exists x ∈ μ such that hτα,p(x, μ, r) &lt; hτ(x, μ, r). Then

$$T \colon = B ( x , r ) \cap ( C ^ { \tau } ( x , \mu ) \ \ C ^ { \tau ^ { \sigma , p } } ( x , \mu ) )$$

is a set with positive Lebesgue measure. Moreover, since τa,P and τ both have appetite α, either λd(CταP (x, μ)) &lt; α or CTTMP (x, μ) \ B(x, r) ≠ 0. In the first case x has claimed every site and must therefore have been rejected by the sites in T. In the second case x has claimed all sites in B(x, r). Again it must have been rejected by all sites in T. This contradicts Lemma 11.6.

Next we take x ∈ μ and r ≥ 0 and prove the second inequality in (11.3). Assume on the contrary that

$$\lambda _ { d } ( C ^ { \tau } ( x , \mu ) \cap B ( x , r ) ) < \lambda _ { d } ( C ^ { \tau ^ { a , s } } ( x , \mu ) \cap B ( x , r ) ) .$$

Then either λd(C(x, μ)) &lt; α or

$$C ^ { \tau } ( x , \mu ) \cap ( \mathbb { R } ^ { d } \ \ B ( x , r ) ) \neq \varnothing .$$


<!-- p:118 -->


(If (11.5) fails, then λd(C(x, μ)) &lt; λd(CTα8(x, μ)) ≤ α.) Further we obtain from (11.4) that λd(T) &gt; 0, where

$$T \coloneqq B ( x , r ) \cap ( C ^ { \tau ^ { a , s } } ( x , \mu ) \ \ C ^ { \tau } ( x , \mu ) ) .$$

For z ∈ T we have that τa,s(z, μ) = x and τ(z, μ) are distinct points of μ so that the first inequality in (11.2) implies |z − x|| &lt; ||z − τ(z, μ)|| for λd-a.e. z ∈ T. In particular, there is a site z ∈ T that desires x. On the other hand, we obtain from (11.5) and z ∈ B(x, r) that x covets z. Hence (z, x) is an unstable pair with respect to τ, contradicting our assumption.

The second inequality in (11.2) can be proved with the help of the first inequality in (11.3). Since it will not be used in what follows, we leave the proof to the reader. □

### 11.4 Uniqueness of Stable Allocations

In this section we let η be a stationary simple point process on Rd with intensity γ ∈ (0, ∞) and with P(η = 0) = 0. We shall need the following consequence of Theorem 10.2.

Lemma 11.8 Let τ be an allocation. Then

$$\mathbb { E } [ g _ { \tau } ( 0 , \eta , r ) ] = \gamma \, \mathbb { E } [ h _ { \tau } ( 0 , \eta ^ { 0 } , r ) ] , \quad r \in [ 0 , \infty ] .$$

Proof Let r ∈  ̄+ and define f ∈ R+(Nls) by f(μ) := 1{|τ(0, μ)| ≤ r}, μ ∈ Nls. Using Theorem 10.2 with g ≡ 1 gives

$$\mathbb { E } [ f ( \eta ) ] & = \gamma \, \mathbb { E } [ \int _ { C ^ { \tau } ( 0 , \eta ^ { 0 } ) } 1 \{ \| \tau ( 0 , \theta _ { z } \eta ^ { 0 } ) \| \leq r \} \, d z ] \\ & = \gamma \, \mathbb { E } [ \int _ { C ^ { \tau } ( 0 , \eta ^ { 0 } ) } 1 \{ \| \tau ( z , \eta ^ { 0 } ) - z \| \leq r \} \, d z ] , \\$$

where we have used (10.3) to get the last identity. But if z ∈ C(0, η0) then τ(z, η0) = 0, provided that 0 ∈ η0, an event of probability 1. The result follows. □

We are now able to prove the following uniqueness result.

Theorem 11.9 Let τ be a stable allocation with appetite α &gt; 0. Then

$$\mathbb { P } ( \tau ( 0 , \eta ) = \tau ^ { \alpha , s } ( 0 , \eta ) ) = 1 .$$

Proof Let r ∈ [0, ∞]. By (10.3) and stationarity we have for all z ∈ Rd that E[gτ(z, η, r)] = E[gτ(0, η, r)]. Applying Proposition 11.7 and Lemma 11.8 yields


<!-- p:119 -->


$$\mathbb { E } [ g _ { \tau ^ { \alpha s } } ( 0 , \eta , r ) ] & \geq \mathbb { E } [ g _ { \tau } ( 0 , \eta , r ) ] = \gamma \, \mathbb { E } [ h _ { \tau } ( 0 , \eta ^ { 0 } , r ) ] \\ & \geq \gamma \, \mathbb { E } [ h _ { \tau ^ { \alpha s } } ( 0 , \eta ^ { 0 } , r ) ] = \mathbb { E } [ g _ { \tau ^ { \alpha s } } ( 0 , \eta ^ { 0 } , r ) ] .$$

Therefore the above inequalities are all equalities and

$$\mathbb { E } [ g _ { \tau ^ { o , s } } ( z , \eta , r ) ] = \mathbb { E } [ g _ { \tau } ( z , \eta , r ) ] , \quad z \in \mathbb { R } ^ { d } .$$

By Proposition 11.7,

$$g _ { \tau ^ { a , s } } ( z , \eta , r ) \geq g _ { \tau } ( z , \eta , r ) , \quad \lambda _ { d ^ { - } } a . e . \ z ,$$

so that

$$g _ { \tau ^ { o , s } } ( z , \eta , r ) = g _ { \tau } ( z , \eta , r ) , \quad \mathbb { P } { \text {-a.a.} } \, z .$$

Now we take μ ∈ Nls and z ∈ Rd such that

$$1 \{ \| \tau ^ { \alpha , s } ( z , \mu ) - z \| \leq r \} = 1 \{ \| \tau ( z , \mu ) - z \| \leq r \} , \quad r \in D ,$$

where D ⊂ R+ is countable and dense. Then ∥τα,s(z, μ) − z|| = ∥τ(z, μ) − z|| and hence τα,s(z, μ) = τ(z, μ) for all normal sites z. Therefore (11.7) implies

$$\lambda _ { d } ( \{ z \in \mathbb { R } ^ { d } \colon \tau ( z , \eta ) \neq \tau ^ { \alpha , s } ( z , \eta ) \} ) = 0 , \quad \mathbb { P } \text {-a.s.}$$

By the covariance property (10.3) we have τ(z, η) ≠ τα,s(z, η) if and only if τ(0, θzη) ≠ τα,s(0, θzη). Therefore (11.6) follows by Exercise 8.13. □

### 11.5 Moment Properties

Finally in this chapter we show that stable allocations with appetite α have poor moment properties. In view of Theorem 10.5 we consider only the case α = γ-1. First we need the following generalisation of Lemma 11.5.

Lemma 11.10 Let τ be a stable allocation with appetite α &gt; 0 and let μ0, μ ∈ Nls such that μ0 ≤ μ. Then for λd-a.e. z with τ(z, μ0) ≠ ∞, the point τ(z, μo) does not reject z in the site-optimal Gale-Shapley algorithm for μ. In particular,

$$\| \tau ^ { \alpha , s } ( z , \mu ) - z \| \leq \| \tau ^ { \alpha , s } ( z , \mu _ { 0 } ) - z \| , \quad \lambda _ { d } \text {-a.e.} \ z .$$

Proof The proof of Lemma 11.5 extends with obvious changes.

□

Theorem 11.11 Let η be a stationary Poisson process on Rd with intensity γ &gt; 0 and let τ be a stable allocation with appetite γ−1. Then E[||τ(0, η)||d] = ∞.


<!-- p:120 -->


Proof Let α := γ−1. By Theorem 10.5 we have P(τ(0, η) ≠ ∞) = 1. By Theorem 11.9 there is (essentially) only one stable allocation with appetite α. By Lemma 11.4 we can therefore assume that τ = ταs. We first prove that

$$\lambda _ { d } ( \{ z \in \mathbb { R } ^ { d } \colon \| \tau ( z , \eta ) - z \| \geq \| z \| - 1 \} ) = \infty , \quad \mathbb { P } \text {-a.s.}$$

Let m ∈ N and let U1, . .. , U be independent and uniformly distributed on the unit ball Ba, independent of η. Define the point process

$$\eta ^ { \prime } \colon = \eta + \sum _ { i = 1 } ^ { m } \delta _ { U _ { i } } .$$

We can assume that η and η' are random elements of Nls. Let

$$A \colon = \{ \mu \in N _ { l s } \colon \lambda _ { d } ( C ^ { \tau } ( x , \mu ) ) = \alpha \text { for all } x \in \mu \} .$$

Theorem 10.9 and Lemma 11.4 show that P(η ∈ A) = 1. By Exercise 4.10, P(η′ ∈ A) = 1. Therefore

$$\lambda _ { d } ( \{ z \in \mathbb { R } ^ { d } \colon \tau ( z , \eta ^ { \prime } ) \in B ^ { d } \} ) \geq m \alpha , \quad \mathbb { P } ^ { \text {a.s.} }$$

But Lemma 11.10 shows, for λd-a.e. z with τ(z, η') ∈ Bd, that

$$\| \tau ( z , \eta ) - z \| \geq \| \tau ( z , \eta ^ { \prime } ) - z \| \geq \| z \| - 1 .$$

Since m is arbitrary, (11.10) follows.

By Fubini's theorem, (10.3) and stationarity,

$$\text {By Fubin series} \, ( 1 0 . 5 ) \text { and usually} , \\ \mathbb { E } [ \int \mathbf 1 \{ \| \tau ( z , \eta ) - z \| \geq \| z \| - 1 \} d z ] & = \int \mathbb { P } ( \| \tau ( z , \eta ) - z \| \geq \| z \| - 1 ) \, d z \\ & = \int \mathbb { P } ( \| \tau ( 0 , \eta ) \| \geq \| z \| - 1 ) \, d z = \mathbb { E } [ \int \mathbf 1 \{ \| \tau ( 0 , \eta ) \| \geq \| z \| - 1 \} d z ] \\ & = \kappa _ { d } \mathbb { E } [ ( \| \tau ( 0 , \eta ) \| + 1 ) ^ { d } ] .$$

The relationship (11.10) implies E[(τ(0, η)| + 1)d] = ∞ and hence the assertion. □

### 11.6 Exercises

Exercise 11.1 Let d = 1 and μ := δ0 + δ1. Compute the point-optimal Gale-Shapley allocations τα,P(·, μ) for α = 1 and for α = 2. Do they coincide with the site-optimal allocations τα,s(·, μ)?


<!-- p:121 -->


Exercise 11.2 Let μ ∈ N&lt;∞(Rd) and let τ be a stable allocation with appetite α &gt; 0. Show that

```
\tau ( x , \mu ) = \tau ^ { \alpha , p } ( x , \mu ) , \ \lambda _ { d } \text {a.e.} \ x .
```

(Hint: There is an n ∈ N and a cube C ⊂ Rd with side length n such that sor p s  n   eo n  = ()\ pnr as in Exercise 8.3.)

Exercise 11.3 Give an example of an allocation with appetite α that is not stable. (Hint: Use a version of the point-optimal Gale-Shapley Algorithm 11.3 with impatient sites.)

Exercise 11.4 Prove Lemma 11.4.

Exercise 11.5 Prove Lemma 11.6. (Hint: Proceed similarly to the proof of Lemma 11.5).

Exercise 11.6 A point process η on Rd is said to be insertion tolerant if, for each Borel set B ⊂ Rd with 0 &lt; λd(B) &lt; ∞ and each random vector X that is uniformly distributed on B and independent of η, the distribution of η + δυ is absolutely continuous with respect to P(η ∈ ·). Show that Theorem 11.11 remains valid for a stationary insertion tolerant point process η.

Exercise 11.7 Suppose that η1 and η2 are independent stationary point processes. Assume moreover, that η2 is a Poisson process with positive intensity. Show that η := η1 + η2 is insertion tolerant. (Hint: Use the Mecke equation for η2.)

Exercise 11.8 Let χ be a stationary Poisson cluster process as in Exercise 8.2. Show that χ is the sum of a stationary Poisson cluster process and an independent stationary Poisson process with intensity γ Q({δ0}). Deduce from Exercise 11.7 that χ is insertion tolerant, provided that γ Q({δ0}) &gt; 0.


<!-- p:122 -->


## Poisson Integrals

The Wiener-Itô integral is the centred Poisson process integral. By means of a basic isometry equation it can be defined for any function that is square integrable with respect to the intensity measure. Wiener-Itô integrals of higher order are defined in terms of factorial measures of the appropriate order. Joint moments of such integrals can be expressed in terms of combinatorial diagram formulae. This yields moment formulae and central limit theorems for Poisson U-statistics. The theory is illustrated with a Poisson process of hyperplanes.

### 12.1 The Wiener-Itô Integral

In this chapter we fix an s-finite measure space (X, X, λ). Let η denote a Pois s mmn  f   s s sn  o msd omee m ∈ N. Corollary 4.10 shows that if f ∈ L1(λ") then

$$\mathbb { E } [ \int f \, d \eta ^ { ( m ) } ] = \int f \, d \lambda ^ { m } ,$$

where the factorial measures η(m) are defined by Proposition 4.3. Our aim is to compute joint moments of random variables of the type ∫ f dη(m).

We start with a necessary and sufficient condition on f ∈ R+(X) for the integral η(f) = ∫ f dη to be almost surely finite.

Proposition 12.1 Let f ∈ R+(X). If

$$\int ( f \wedge 1 ) \, d \lambda < \infty ,$$

then P(η(f) &lt; ∞) = 1. If (12.2) fails, then P(η(f) = ∞) = 1.

Proof Assume that (12.2) holds and without loss of generality that η is proper. Then λ({f ≥ 1}) &lt; ∞ and therefore η({f ≥ 1}) &lt; ∞ a.s. Hence


<!-- p:123 -->


η(1{f ≥ 1}f) &lt; ∞ a.s. Furthermore we have from Proposition 2.7 that

$$\mathbb { E } [ \eta ( \mathbf 1 \{ f < 1 \} f ) ] = \lambda ( \mathbf 1 \{ f < 1 \} f ) < \infty ,$$

so that η(1{f &lt; 1}f) &lt; ∞ almost surely.

Assume, conversely, that (12.2) fails. By Theorem 3.9,

$$\mathbb { E } [ e ^ { - \eta ( f ) } ] = \exp \left [ - \lambda ( 1 - e ^ { - f } ) \right ] .$$

The inequality (1 − e−t) ≥ (1 − e−1)(t ∧ 1), t ≥ 0, implies λ(1 − e−f) = ∞ and hence E[e−n(f)] = 0. Therefore P(η(f) = ∞) = 1. □

Recall that LP(λ) = {f ∈ R(X) : λ(lf|P) &lt; ∞}; see Section A.1. For f ∈ L1(λ) the compensated integral of f with respect to η is defined by

$$I ( f ) \coloneqq \eta ( f ) - \lambda ( f ) .$$

It follows from Campbell's formula (Proposition2.7) that

$$\mathbb { E } [ I ( f ) ] = 0 .$$

The random variable I(f) is also denoted ∫ f d(η − λ) or ∫ f dη, where η := η – λ. However, the reader should keep in mind that η is not defined on on all of X but only on {B ∈ X : λ(B) &lt; ∞}. Let L1,2(λ) := L1(λ)∩L2(λ). The compensated integral has the following useful isometry property.

Lemma 12.2 Suppose f, g ∈ L1,2(λ). Then

$$\mathbb { E } [ I ( f ) I ( g ) ] = \int f g \, d \lambda .$$

)( (0) (  &gt; [(f] t s ()  (g)) is just the covariance between η(f) and η(g). A simple calculation gives

$$\mathbb { E } [ I ( f ) I ( g ) ] = \mathbb { E } [ \eta ( f ) \eta ( g ) ] - \lambda ( f ) \lambda ( g ) .$$

Applying (4.26) yields (12.6).

□

The next lemma shows that L1,2(λ) is a dense subset of L2(λ).

Lemma 12.3 Let f ∈ L2(λ) and n ∈ N. Then fn := 1{|f| ≥ 1/n} f ∈ L1(P). Moreover, fn → f in L2(P) as n → ∞.

Proof For each c &gt; 0 we have that

$$\int f ^ { 2 } \, d \lambda \geq \int 1 \{ f ^ { 2 } \geq c ^ { 2 } \} f ^ { 2 } \, d \lambda \geq c ^ { 2 } \lambda ( | f | \geq c ) .$$


<!-- p:124 -->


Therefore,

$$\text {here,} & , \\ & \int \mathbf 1 \{ | f | \geq c \} | f | \, d \lambda = \int \mathbf 1 \{ 1 \geq | f | \geq c \} | f | \, d \lambda + \int \mathbf 1 \{ | f | > 1 \} | f | \, d \lambda \\ & \leq \lambda ( | f | \geq c ) + \int f ^ { 2 } \, d \lambda < \infty ,$$

so that 1{|f| ≥ c}f ∈ L1(λ). Since lim→∞ fn(x) = f(x) for each x ∈ X and |f − fn| ≤ 2|f|, dominated convergence shows that λ((f − fn)2) → 0. □

Lemma 12.3 can be used to extend I to a mapping from L2(λ) to L2(P) as follows.

Proposition 12.4 The mapping I: L1,2(λ) → L2(P) defined by (12.4) can be uniquely extended to a linear mapping I: L2(λ) → L2(P) such that (12.5) and (12.6) hold for all f ∈ L2(λ).

Proof The proof is based on basic Hilbert space arguments. For f ∈ L2(λ) we define (f) as in Lemma 12.3 and then obtain from (12.6) that

$$\mathbb { E } [ ( I ( f _ { m } ) - I ( f _ { n } ) ) ^ { 2 } ] = \mathbb { E } [ ( I ( f _ { m } - f _ { n } ) ) ^ { 2 } ] = \lambda ( ( f _ { m } - f _ { n } ) ^ { 2 } ) ,$$

which tends to 0 as m, n → ∞. Since L2(P) is complete, the sequence (I(fn)) converges in L2(P) to some element of L2(P); we define I(f) to be this limit. If in addition f ∈ L1(λ), then, by dominated convergence, λ(fn) → λ(f), while dominated convergence and Proposition 12.1 show that η(fn) → η(f) almost surely. Hence our new definition is consistent with (12.4). Since E[I(fn)] = 0 for all n ∈ N, the L2-convergence yields E[I(f)] = 0. Furthermore,

$$\mathbb { E } [ I ( f ) ^ { 2 } ] = \lim _ { n \to \infty } \mathbb { E } [ I ( f _ { n } ) ^ { 2 } ] = \lim _ { n \to \infty } \lambda ( f _ { n } ^ { 2 } ) = \lambda ( f ^ { 2 } ) ,$$

where we have used Lemma 12.2 and, for the final identity, dominated convergence. The linearity

$$I ( a f + b g ) = a I ( f ) + b I ( g ) , \quad \mathbb { P } \text {-a.s., } f , g \in L ^ { 2 } ( \lambda ) , \ a , b \in \mathbb { R } , \quad ( 1 2 . 7 )$$

follows from the linearity of I on L1(λ).

If f, g ∈ L2(λ) coincide λ-a.e., then (12.6) implies that

$$\mathbb { E } [ ( I ( f ) - I ( g ) ) ^ { 2 } ] = \mathbb { E } [ ( I ( f - g ) ) ^ { 2 } ] = \lambda ( ( f - g ) ^ { 2 } ) = 0 ,$$

so that I(f) = I(g) a.s. Hence I: L2(λ) → L2(P) is a well-defined mapping.

If I' is another extension with the same properties as I then we can use the Minkowski inequality and I(f) = I'(fn) to conclude that

$$( \mathbb { E } [ ( I ( f ) - I ^ { \prime } ( f ) ) ^ { 2 } ] ) ^ { 1 / 2 } \leq ( \mathbb { E } [ ( I ( f ) - I ( f _ { n } ) ) ^ { 2 } ] ) ^ { 1 / 2 } + ( \mathbb { E } [ ( I ^ { \prime } ( f ) - I ^ { \prime } ( f _ { n } ) ) ^ { 2 } ] ) ^ { 1 / 2 }$$


<!-- p:125 -->


for all n ∈ N. By the isometry (12.6), both terms on the right-hand side of the preceding equation tend to 0 as n → ∞. □

Definition 12.5 For f ∈ L2(λ) the random variable I(f) ∈ L2(P) is called the (stochastic) Wiener-Itô integral of f.

Let f ∈ R(X) and define (f) as in Lemma 12.3. If f ∈ L1(λ), then as shown in the preceding proof the sequence I(f) converges almost surely towards I(f), defined pathwise (that is, for every ω ∈ Ω) by (12.4). If, however, f ∈ L2(λ) \ L1(λ), then I(fn) converges to I(f) in L2(P) and hence only in probability.

Note that L1(λ) is not contained in L2(λ), and, unless λ(X) &lt; ∞, neither is L2(λ) contained in L1(λ). Exercise 12.3 shows that it is possible to extend I to the set of all f ∈ R(X) satisfying

$$\int | f | \wedge f ^ { 2 } \, d \lambda < \infty .$$

### 12.2 Higher Order Wiener-Itô Integrals

In this section we turn to Poisson integrals of higher order. For m ∈ N and f ∈ L1(λm) define

$$I _ { m } ( f ) \coloneqq \sum _ { J \subset [ m ] } ( - 1 ) ^ { m - | J | } \iint f ( x _ { 1 } , \dots , x _ { m } ) \, \eta ^ { ( | J | ) } ( d x _ { J } ) \, \lambda ^ { m - | J | } ( d x _ { J ^ { c } } ) , \quad ( 1 2 . 9 )$$

where [m] := {1, .. . , m}, Jc := [m] \ J, xj := (xj)j∈J and where |J| := card J denotes the number of elements of J. The inner integral in (12.9) is interpreted as f(x1, . . . , xm) when J = 0. This means that we set η(0)(c) := c for all c ∈ R. Similarly, when J = [m] the outer integration is performed according to the rule λo(c) := c for all c ∈ R. For each J ⊂ [m] it follows from (12.1) and Fubini's theorem that

$$\left ] = \int | f | \, d \lambda ^ { m } < \infty .$$

Therefore, Im(f) is an almost surely finite random variable and

$$\mathbb { E } [ I _ { m } ( f ) ] = 0 .$$

A function f : Xm → R is said to be symmetric if

$$f ( x _ { 1 } , \dots , x _ { m } ) = f ( x _ { \pi ( 1 ) } , \dots , x _ { \pi ( m ) } ) , \quad ( x _ { 1 } , \dots , x _ { m } ) \in \mathbb { X } ^ { m } , \, \pi \in \Sigma _ { m } , \ \ ( 1 2 . 1 1 )$$

where Σm is the set of permutations of [m], that is the set of all bijective mappings from [m] to [m]. If f ∈ L1(λn) is symmetric, then the symmetry of η(m) (see (A.17)) and λ implies that


<!-- p:126 -->


$$I _ { m } ( f ) = \sum _ { k = 0 } ^ { m } ( - 1 ) ^ { m - k } { m \choose k } \eta ^ { ( k ) } \otimes \lambda ^ { m - k } ( f ) , \quad ( 1 2 . 1 2 )$$

where η(k) © λm-k(f) is the integral of f with respect to the product measure η(k) ⊗ λm−k. In accordance with our convention η(0)(c) = λ0(c) = c, we have set η(0) ⊗ λ := λ− and η(n) ⊗ λ0 := η(m).

For m = 1 the definition (12.9) reduces to (12.4). For m = 2 we have

$$I _ { 2 } ( f ) & = \int f ( x _ { 1 } , x _ { 2 } ) \, \eta ^ { ( 2 ) } ( d ( x _ { 1 } , x _ { 2 } ) ) - \iint f ( x _ { 1 } , x _ { 2 } ) \, \eta ( d x _ { 1 } ) \, \lambda ( d x _ { 2 } ) \\ & - \iint f ( x _ { 1 } , x _ { 2 } ) \, \lambda ( d x _ { 1 } ) \, \eta ( d x _ { 2 } ) + \int f ( x _ { 1 } , x _ { 2 } ) \, \lambda ^ { 2 } ( d ( x _ { 1 } , x _ { 2 } ) ) .$$

In general, Im(f) is a linear combination of η(m)(f) and integrals of the type η(k)(fk) for k ≤ m − 1, where fk is obtained from f by integrating m − k variables with respect to λm-k. In view of the forthcoming orthogonality iln fu s  s s s s l ( r than with η(m)(f).

We shall prove formulae for the mixed moments E[ Πk=1 η(ni)(fi¿)] and E[ Πk=1 Ini(fi)], where l, n1, . . , ne ∈ N and fi ∈ L1(λni) for i ∈ [l]. To do so we shall employ combinatorial arguments.

Let n ∈ N. A subpartition of [n] is a family of disjoint non-empty subsets of [n], which we call blocks. A partition of [n] is a subpartition σ of [n] such that ∪J∈σJ = [n]. We denote by ΠI (resp. II) the system of all partitions (resp. subpartitions) of [n]. The cardinality of σ ∈ II (i.e., the number of blocks of σ) is denoted by |σ|, while the cardinality of ∪J∈σJ is denoted by |σ||. If σ is a partition, then |σ|| = n.

Let l, n1, . . . , ne ∈ N. Define n := n1 + . . · + ne and

$$J _ { i } \coloneqq \{ j \in \mathbb { N } \, \colon n _ { 1 } + \cdots + n _ { i - 1 } < j \leq n _ { 1 } + \cdots + n _ { i } \} , \quad i = 1 , \dots , \ell .$$

Let π := {Ji : 1 ≤ i ≤ l} and let II(n1, . . , ne) ⊂ IIn (resp. II*(n1, . . . , ne) ⊂ In) denote the set of all σ ∈ ΠI (resp. σ ∈ In) with |J ∩ J'| ≤ 1 for all J ∈ σ and for all J' ∈ π. Let II≥2(n1, . . . , ne) (resp. II=2(n1, . . . , ne)) denote the set of all σ ∈ ΠI(n1, . . , ne) with |J| ≥ 2 (resp. |J| = 2) for all J ∈ σ. Let I:2(n1, . , ne) denote the set of all σ ∈ II*(n1, . . . , ne) with |J| ≥ 2 for all J ∈ σ.

Let σ ∈ Π(n1, . . . , ne). It is helpful to visualise the pair (π, σ) as a diagram with rows J1, ... , Je, where the elements in each block J ∈ σ are encircled by a closed curve. Since the blocks of σ are not allowed to contana  t  t      o a o anm (π, σ) is non-flat.


<!-- p:127 -->


The tensor product ∅i=1 fi (also written f1⊗. · ·©fe) of functions fi : Xni → R, i ∈ {1, . . . , l}, is the function from Xn to R which maps each (x1, . . . , xn) to ∏k=1 fi(xji). In the case that n1 = · . · = ne and f1 = . . · = fe = f for some f, we write f'l instead of ∅i=1fi.

For any function f : Xn → R and σ ∈ In we define fσ : Xn+|σl-lσ∥ → R by identifying those arguments which belong to the same block of σ. (The arguments x1, . . . , x+|σl-lσ| are inserted in the order of first occurrence.) For example, if n = 4 and σ = {{1, 3}, {4}}, then fσ(x1, x2, x3) = f(x1, x2, x1, x3). The partition {{2}, {1, 3}, {4}} and the subpartition {{1, 3}} lead to the same function.

We now give a formula for the expectation of a product of integrals with respect to factorial measures.

Proposition 12.6 Let fi ∈ L1(λi), i ∈ {1, . . . , l}, where l, n1, . . . , ne ∈ N. Let n := n1 + · . · + ne and assume that

$$\int ( | f _ { 1 } | \otimes \cdots \otimes | f _ { \ell } | ) _ { \sigma } \, d \lambda ^ { | \sigma | } < \infty , \quad \sigma \in \Pi ( n _ { 1 } , \dots , n _ { \ell } ) .$$

Then

$$\mathbb { E } [ \prod _ { i = 1 } ^ { \ell } \eta ^ { ( n _ { i } ) } ( f _ { i } ) ] = \sum _ { \sigma \in \Pi _ { z \sigma ^ { 2 } } ^ { * } ( n _ { 1 } , \dots , n _ { i } ) } \int ( f _ { i } \otimes \cdots \otimes f _ { \ell } ) _ { \sigma } \, d \lambda ^ { n + | \sigma | - | \sigma | } .$$

Proof Since we consider a distributional property, we can assume that η is proper and given by (2.4). Using (4.4) for each η(ni), we obtain

$$\prod _ { i = 1 } ^ { \ell } \eta ^ { ( n _ { i } ) } ( f _ { i } ) = \sum _ { i _ { 1 } , \dots , i _ { n } \leq \kappa } ^ { \ast } ( f _ { 1 } \otimes \dots \otimes f _ { \ell } ) ( X _ { i _ { 1 } } , \dots , X _ { i _ { n } } ) ,$$

where Σ* means that in the sum the ij and ik must be distinct whenever j ≠ k and j, k lie in the same block of π, where π was defined after (12.13). (The convergence of this possibly infinite series will be justified at the end of the proof.) Each multi-index (i1, . . . , in) induces a subpartition in I2(n1, . . . , ne) by taking j ≠ k to be in the same block whenever ij = ik. Then the right-hand side of (12.16) equals

$$\sum _ { \sigma \in \Pi _ { z 2 } ^ { * } ( n _ { 1 } , \dots , n _ { \ell } ) } \sum _ { i _ { 1 } , \dots , i _ { n + | \sigma | - | \sigma | } \leq K } ^ { \neq } ( f _ { 1 } \otimes _ { | \sigma | \leq K } ^ { \otimes }$$

Corollary 4.10 yields the asserted result (12.15). The same computation also shows that the series on the right-hand side of (12.16) has a finite expectation upon replacing fi by If| for each i ∈ [€] and using assumption (12.14). In particular this series converges absolutely, almost surely. □


<!-- p:128 -->


The following result is consistent with (12.5), (12.6) and (12.10).

Theorem 12.7 Let f1, . . . , fe be as in Proposition 12.6 and assume that (12.14) holds. Then

$$\mathbb { E } \left [ \prod _ { i = 1 } ^ { \ell } I _ { n _ { i } } ( f _ { i } ) \right ] = \sum _ { \sigma \in \Pi _ { \mathbb { Z } ^ { 2 } } ( n _ { 1 } , \dots , n _ { i } ) } \int ( f _ { 1 } \otimes \cdots \otimes f _ { \ell } ) _ { \sigma } \, d \lambda ^ { | \sigma | } .$$

Proof By the definition (12.9) and Fubini's theorem,

$$\prod _ { i = 1 } ^ { \ell } I _ { n _ { i } } ( f _ { i } ) = \sum _ { I \subset [ n ] } ( - 1 ) ^ { n - | I | } \int \dots \int f _ { 1 } \otimes \dots \otimes f _ { \ell } \\ \times \eta ^ { ( I \otimes J _ { 1 } ) | } ( d x _ { I \cap J _ { 1 } } ) \cdots \eta ^ { ( I \otimes J _ { \ell } ) | } ( d x _ { I \cap J _ { \ell } } ) \, \lambda ^ { n - | I | } ( d x _ { I ^ { \prime } } ) , \quad ( 1 2 . 1 8 )$$

where Ic := [n]\I and where we use definition (12.13) of J. By Proposition 12.6,

$$\mathbb { E } \left [ \prod _ { i = 1 } ^ { \ell } I _ { n _ { i } } ( f _ { i } ) \right ] = \sum _ { I \subset [ n ] } ( - 1 ) ^ { n - | I | } \sum _ { \sigma \in \Pi _ { \Sigma _ { 2 } } ^ { * } ( n _ { 1 } , \dots , n _ { l } ) \colon \sigma \subset I } \int ( \otimes _ { i = 1 } ^ { \ell } f _ { i } ) _ { \sigma } \, d \lambda ^ { n + | \sigma | - | | \sigma | | } ,$$

where σ ⊂ I means that every block of σ is contained in I. Interchanging the order of the above summations, and noting that for any given σ the sum Σr:σc(-1)n-|l comes to zero except when σ is a partition, in which case it comes to one, gives us (12.17). □

Given n ≥ 1, let L2(λn) denote the set of all f ∈ L2(λn) that are symmetric. Let L0,s(λn) ⊂ L2(λn) denote the set of all symmetric f ∈ R(Xn) such that f is bounded and λn({f ≠ 0}) &lt; ∞. The following result generalises Lemma 12.2.

Corollary 12.8 Let m, n ∈ N, f ∈ L0,s(λn) and g ∈ Lo,s(λn). Then

$$\mathbb { E } [ I _ { m } ( f ) I _ { n } ( g ) ] = 1 \{ m = n \} m ! \int f g \, d \lambda ^ { m } .$$

Proof The assumptions allow us to apply Theorem 12.7 with l = 2, fi = f and g2 = g. First assume m = n. Then each element of Π≥2(m, n) is a partition of [2m] with m blocks each having two elements, one from {1,...,m} and one from {m + 1,..., 2m}. We identify each element of I≥2(m, m) with a permutation of [m] in the obvious manner. With Σ denoting the set of all such permutations, (12.17) gives us


<!-- p:129 -->


$$\mathbb { E } [ I _ { m } ( f ) I _ { n } ( g ) ] = \sum _ { \sigma \in \Sigma _ { m } } \int f ( x _ { 1 } , \dots , x _ { m } ) g ( x _ { \sigma ( 1 ) } , \dots , x _ { \sigma ( m ) } ) \, \lambda ^ { m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) .$$

y es ea- e so  e   n ss sls ∫ f g dλn. Hence (12.19) holds for m = n. If m ≠ n then Π≥2(m, n) = ∅, so that (12.19) holds in this case too. □

The following result can be proved in the same manner as Proposition 12.4; see Exercise 12.4.

Proposition 12.9 The mappings Im: L0,s(λm) → L2(P), m ∈ N, can be uniquely extended to linear mappings Im: L2(λn) → L2(P) so that (12.10) (uχ)zT ∪ (uX),7 3 f fI ·(uχ)γT 3 8 pup (uν)γT ə f 11p 1of ploy (6171) pup then Im(f) is almost surely given by (12.9).

Definition 12.10 For m ∈ N and f ∈ L2(λn) the random variable Im(f) ∈ L2(P) is called the (stochastic, m-th order) Wiener-Itô integral of f.

### 12.3 Poisson U-Statistics

In the rest of this chapter we apply the preceding results to U-statistics. Let ans d (a  N ut

$$U \coloneqq \int h ( x _ { 1 } , \dots , x _ { m } ) \, \eta ^ { ( m ) } ( d ( x _ { 1 } , \dots , x _ { m } ) ) .$$

Then U is known as a Poisson U-statistic with kernel function h. For n ∈ {0, . . . , m}, define hn ∈ L1(λn) by

$$h _ { n } ( x _ { 1 } , \dots , x _ { n } ) \coloneqq \binom { m } { n } \int h ( x _ { 1 } , \dots , x _ { n } , y _ { 1 } , \dots , y _ { m - n } ) \, \lambda ^ { m - n } ( d ( y _ { 1 } , \dots , y _ { m - n } ) ) ,$$

where h0 := λm(h). With our earlier convention λ0(c) = c, c ∈ R, this means that h = h. A Poisson U-statistic can be decomposed into mutually orthogonal terms as follows.

Proposition 12.11 Let U be the Poisson U-statistic given by (12.20) and define the functions h by (12.21). Then

$$U = \mathbb { E } [ U ] + \sum _ { n = 1 } ^ { m } I _ { n } ( h _ { n } ) , \quad \mathbb { P } { \cdot } a . s .$$


<!-- p:130 -->


Proof We note that E[U] = λm(h) = h0 and set η(0) ⊗ λ0(h0) := h0. Then we obtain from (12.12) that

$$we \text { obtain from } ( 1 2 . 1 2 ) \text { that} \\ \mathbb { E } [ U ] + \sum _ { n = 1 } ^ { m } I _ { n } ( h _ { n } ) & = \sum _ { n = 0 } ^ { m } \sum _ { k = 0 } ^ { n } ( - 1 ) ^ { n - k } \binom { n } { k } \eta ^ { ( k ) } \otimes \lambda ^ { n - k } ( h _ { n } ) \\ & = \sum _ { k = 0 } ^ { m } \sum _ { n = k } ^ { m } ( - 1 ) ^ { n - k } \binom { n } { k } \binom { m } { n } \eta ^ { ( k ) } \otimes \lambda ^ { m - k } ( h ) \\ & = \sum _ { k = 0 } ^ { m } \binom { m } { k } \eta ^ { ( k ) } \otimes \lambda ^ { m - k } ( h ) \sum _ { r = 0 } ^ { m - k } ( - 1 ) ^ { r } \binom { m - k } { r } , \quad ( 1 2 . 2 3 ) \\ \text {where we have used the substitution } r \colon = n - k \text { and the combinatorial identity}$$

where we have used the substitution r := n – k and the combinatorial identity

$$\begin{pmatrix} k + r \\ k \end{pmatrix} \binom { m } { k + r } = \begin{pmatrix} m \\ k \end{pmatrix} \begin{pmatrix} m - k \\ r \end{pmatrix} .$$

The inner sum at (12.23) vanishes for m &gt; k and equals 1 otherwise. The result follows. □

Together with Proposition 12.9 the preceding proposition yields the following result.

Proposition 12.12 Let the Poisson U-statistic U be given by (12.20) and assume that the functions h defined by (12.21) are square integrable with respect to λn for all n ∈ [m]. Then U is square integrable with variance

$$\varpi [ U ] = \sum _ { n = 1 } ^ { m } n ! \int h _ { n } ^ { 2 } \, d \lambda ^ { n } .$$

Proof Proposition 12.11, the assumption h ∈ L2(λn) and Proposition 12.9 imply that U is square integrable. Moreover, the isometry relation (12.19) (see Proposition 12.9) gives us (12.24). □

If, in the situation of Proposition 12.12, λ(h2) = 0 then we say that U is degenerate. This happens if and only if

$$\lambda \Big \{ x _ { 1 } \colon \int h ( x _ { 1 } , \dots , x _ { m } ) \, \lambda ^ { m - 1 } ( d ( x _ { 2 } , \dots , x _ { m } ) ) \neq 0 \Big \} = 0 .$$

Therefore λn(h) ≠ 0 is sufficient for U not to be degenerate.

Next we generalise Proposition 12.12. For l ∈ N and σ ∈ I(m, . . . , m) (m occurs l times) let

[σ] := {i ∈ [l] : there exists J ∈ σ, J ∩ {m(i − 1) + 1, . . . , mi} ≠ 0}, i.e. [σ] is the set of rows of the diagram of (m, . . . , m) that are visited by σ. Let I*2(m, . . . , m) be the set of subpartitions in II*2(m, . . . , m) that satisfy [σ] = [€], i.e. that visit every row of the diagram.


<!-- p:131 -->


Proposition 12.13 Let the Poisson U-statistic U be given by (12.20). Let l ≥ 2 be an integer such that ∫(|h|®l)σ dλ|σ| &lt; ∞ for all σ ∈ ΠI(m, . . . , m) (with l occurring m times). Then

$$[ U ] ) ^ { \ell } ] = \sum _ { \sigma \in \Pi _ { \Sigma _ { 2 } } ^ { \ast } ( m , \dots , m ) } \int ( h ^ { \otimes \ell } ) _ { \sigma } \, d \lambda ^ { m \ell + | \sigma | - | | \sigma | | } .$$

Proof We have

$$\mathbb { E } [ ( U - \mathbb { E } [ U ] ) ^ { \ell } ] = \sum _ { I \subset [ \ell ] } \mathbb { E } [ U ^ { | I | } ] ( - \mathbb { E } [ U ] ) ^ { \ell - | I | } ,$$

and, using (12.15) along with the fact that E[U] = λn(h), we have that this equals

$$\sum _ { I \subset [ \ell ] } ( - 1 ) ^ { \ell - | I | } \sum _ { \sigma \in \Pi _ { \Sigma ^ { 2 } } ^ { * } ( m , \dots , m ) \colon [ \sigma ] \subset I } \int ( h \otimes \cdots \otimes h ) _ { \sigma } \, d \lambda ^ { m \ell + | \sigma | - | | \sigma | | } .$$

Interchanging the summations and arguing as in the proof of Theorem 12.7 gives the result. □

In the remainder of this chapter we extend our setting by considering for t &gt; 0 a Poisson process ηt with intensity measure λ := tλ. We study Poisson U-statistics of the form

$$U _ { t } \coloneqq b ( t ) \int h ( x _ { 1 } , \dots , x _ { m } ) \, \eta _ { t } ^ { ( m ) } ( d ( x _ { 1 } , \dots , x _ { m } ) ) ,$$

where m ∈ N, b(t) &gt; 0 for all t &gt; 0 and the kernel function h ∈ L1(λ") does not depend on t. We recall the definition (B.6) of the double factorial (€ – 1)!! for even integer l ≥ 2. This is the number of (perfect) matchings π of [€]. Such a matching is a partition of [€] whose blocks are all of size 2. If l is odd, then no such matching exists.

Theorem 12.14 Let m ∈ N and h ∈ L1(λm). Let U, be the Poisson U-statistic given by (12.27) and let l ≥ 2 be an integer. Assume that ∫(|h|®)σ dλ|σ| &lt; ∞ for all σ ∈ ΠI(m, . . . , m). Assume also that λ(h2) &gt; 0, where h1 is given by (12.21) for n = 1. Then

$$\lim _ { t \to \infty } \frac { \mathbb { E } [ ( U _ { t } - \mathbb { E } U _ { t } ) ^ { \ell } ] } { ( \mathbb { V } a r [ U _ { t } ] ) ^ { \ell / 2 } } = \begin{cases} ( \ell - 1 ) ! ! , & \text {if } \ell \text { is even} , \\ 0 , & \text {if } \ell \text { is odd} . \end{cases} \quad ( 1 2 . 2 8 )$$


<!-- p:132 -->


Proof Let n ∈ {1, . . . , m}. Our assumptions on h imply that the mapping that sends the vector (x1, . . . , xn, y1, . . . , ym-n, Z1, . . . , Zm-n) to the product of |h(x1, . . , xn, y1, . . . , ym−n)| and |h(x1, . . , χn, Z1, . . . , Zm−n)| is integrable with respect to λ2m-n. (To see this we might take a σ containing the pairs {1, m + 1}, . . . , {n, m + n} while the other blocks are all singletons.) Therefore by Fubini's theorem h ∈ L2(λ"), where h is given by (12.21). For t &gt; 0, define the function h,n by (12.21) with (h, λ) replaced by (b(t)h, λ). Then ht,n = b(t)tm−nh, so that Proposition 12.12 yields that Ut is square integrable and

$$\mathbb { V } a r [ U _ { t } ] = b ( t ) ^ { 2 } \sum _ { n = 1 } ^ { m } n ! t ^ { 2 m - n } \int h _ { n } ^ { 2 } \, d \lambda ^ { n } .$$

In the remainder of the proof we assume without loss of generality that b(t) = 1 for all t &gt; 0. Since we assume λ(h2) &gt; 0, we obtain from (12.29) that

$$( \mathbb { V } a r [ U _ { t } ] ) ^ { \ell / 2 } = ( \lambda ( h _ { 1 } ^ { 2 } ) ) ^ { \ell / 2 } t ^ { \ell ( m - 1 / 2 ) } + p ( t ) ,$$

where the remainder term p(·) is a polynomial of degree strictly less than l(m − 1/2).

In the present setting we can rewrite (12.26) as

$$\sigma \in \Pi _ { z ^ { 2 } } ^ { * * } ( m , \dots , m )$$

Note that for any σ ∈ I≥2(m, . . . , m) we have |σ|| ≥ l and |σ| ≤ ∥σ|/2. Therefore, if l is even, ml + |σ| – lσ‖| is maximised (over subpartitions σ ∈ I≥2(m, . . . , m)) by taking σ such that |σ| = l/2 and each block has size 2 and [σ] = l. The number of such σ is (l − 1)!!mf so the leading order term in the expression (12.31) comes to

$$t ^ { m \ell - \ell / 2 } \left ( \int h _ { 1 } ^ { 2 } d \lambda \right ) ^ { \ell / 2 } ( \ell - 1 ) ! !$$

as required. For l odd, the above inequalities show that

$$m \ell + | \sigma | - \| \sigma \| \leq m \ell - ( \ell + 1 ) / 2$$

so that lim,→∞ t−l(m−1/2)E[(Ut − E[Ut])] = 0.

□

The preceding proof implies the following result on the asymptotic variance of a Poisson U-statistic.


<!-- p:133 -->


Proposition 12.15 Let U, be the Poisson U-statistic given by (12.27). Let the functions h be given by (12.21) and assume that h ∈ L2(λn) for each n ∈ [m]. Then

$$\lim _ { t \to \infty } b ( t ) ^ { - 2 } t ^ { 1 - 2 m } \, \mathbb { V } a r [ U _ { t } ] = \int h _ { 1 } ^ { 2 } \, d \lambda .$$

Proof It is easy to see (and is explained at the beginning of the proof of Theorem 12.14) that our assumption that h ∈ L2(λ") for each n ∈ [m] is equivalent to the integrability assumption of Theorem 12.14 in the case l = 2. Hence we have (12.29) and the result follows. □

Theorem 12.14 leads to the following central limit theorem.

Theorem 12.16 (Central limit theorem for Poisson U-statistics) Suppose that m ∈ N and h ∈ L1(λn) and that U, is given by (12.27). Assume that ∫(|h|®)σ dλ|σ| &lt; ∞ for all l ∈ N and all σ ∈ ΠI(m, . . . , m). Assume also that λ(h2) &gt; 0, where h1 is given by (12.21) for n = 1. Then

$$( \mathbb { V } a r [ U _ { t } ] ) ^ { - 1 / 2 } ( U _ { t } - \mathbb { E } U _ { t } ) \stackrel { d } { \longrightarrow } N \ a s \ t \to \infty ,$$

where — denotes convergence in distribution and N is a standard normal random variable.

Proof By (B.5) we have E[Nł] = (l − 1)!! if l is even and E[Nt] = 0 otherwise. Moreover, with the help of Proposition B.4 one can show that the distribution of N is determined by these moments. Theorem 12.14 says that the moments of the random variable (Var[U])−1/2(U, − EUt) converge to the corresponding moments of N. The method of moments (see Proposition B.12) gives the asserted convergence in distribution. □

The following lemma is helpful for checking the integrability assumptions of Theorem 12.16.

Lemma 12.17 Let l ∈ N such that h ∈ Lk(λn). Assume that {h ≠ 0} ⊂ Bm, where B ∈ X satisfies λ(B) &lt; ∞. Then we have ∫(h|®)σ dλ|σ| &lt; ∞ for all σ ∈ ΠI(m, . . . , m).

Proof Apply Exercise 12.9 in the case f1 = · . . = fe = h.

□

### 12.4 Poisson Hyperplane Processes

Finally in this chapter we discuss a model from stochastic geometry. Let d ∈ N and let Hd-1 denote the space of all hyperplanes in Rd. Any such hyperplane H is of the form


<!-- p:134 -->


$$H _ { u , r } \colon = \{ y \in \mathbb { R } ^ { d } \, \colon \langle y , u \rangle = r \} ,$$

where u is an element of the unit sphere Sd-1, r ≥ 0 and 〈, ·〉 denotes the Euclidean scalar product. We can make Ha-1 a measurable space by introducing the smallest σ-field H containing the sets

$$[ K ] \colon = \{ H \in \mathbb { H } _ { d - 1 } \colon H \cap K \neq \emptyset \} , \ \ K \in \mathcal { C } ^ { d } ,$$

where Cd denotes the system of all compact subsets of Rd. In fact, Ha-1∪{0} is a closed subset of the space Fa of all closed subsets of Rd, equipped with the Fell topology, as defined in Section A.3.

We fix a measure λ on Hd-1 satisfying

$$\lambda ( [ K ] ) < \infty , \ \ K \in C ^ { d } .$$

In particular, λ is σ-finite. As before, for t &gt; 0 let ηt be a Poisson process with intensity measure λ, := tλ. The point process ηt is called a Poisson hyperplane process, while the union

$$Z \coloneqq \bigcup _ { \eta \{ H \} > 0 } H$$

of all hyperplanes in η is called a Poisson hyperplane tessellation. (It can be shown that the singletons in Ha-1 are closed and hence measurable.) The cells of this tessellation are the (closures of the) connected components of the complement Rd \ Z.

Recall from Section A.3 that Ka denotes the space of all convex compact subsets of Rd. Let W ∈ Kd and m ∈ N. Let ψ: Kd → R be a measurable function. By Lemma A.30, (H1, . . . , Hm) ↔ ψ(H1 ∩ · . · ∩ Hm ∩ W) is a measurable mapping from (Hd-1)n to R. We also assume that ψ(0) = 0 and that ψ(H1 ∩ · · · ∩ Hm ∩ W) ≤ cw for λm-a.e. (H1, . . . , Hm), where cw depends on W. (We shall give some examples at the end of this section.) We consider the Poisson U-statistic given by

$$U _ { t } \coloneqq \frac { 1 } { m ! } \int \psi ( H _ { 1 } \cap \cdots \cap H _ { m } \cap W ) \, \eta _ { t } ^ { ( m ) } ( d ( H _ { 1 } , \dots , H _ { m } ) ) , \ \ t > 0 . \ ( 1 2 . 3 6 )$$

To formulate a corollary to Theorem 12.16 we define, for n ∈ [m], a function ψn ∈ R((Hd−1)n) by

$$\psi _ { n } ( H _ { 1 } , \dots , H _ { n } ) \coloneqq \int \psi ( H _ { 1 } \cap \cdots \cap H _ { m } \cap W ) \, \lambda ^ { m - n } ( d ( H _ { n + 1 } , \dots , H _ { m } ) ) .$$

(12.37)


<!-- p:135 -->


Corollary 12.18 Let ψ satisfy the assumptions formulated before (12.36) and define Ut by (12.36). Then

$$\mathbb { E } [ U _ { t } ] = \frac { t ^ { m } } { m ! } \int \psi ( H _ { 1 } \cap \cdots \cap H _ { m } \cap W ) \, \lambda ^ { m } ( d ( H _ { 1 } , \dots , H _ { m } ) ) ,$$

$$\mathbb { V } _ { \ } [ U _ { t } ] = \sum _ { n = 1 } ^ { m } \frac { 1 } { n ! ( ( m - n ) ! ) ^ { 2 } } t ^ { 2 m - n } \int \psi _ { n } ^ { 2 } \, d \lambda ^ { n } ,$$

and if, moreover,

$$\int \psi ( H _ { 1 } \cap \cdots \cap H _ { m } \cap W ) \, \lambda ^ { m } ( d ( H _ { 1 } , \dots , H _ { m } ) ) \neq 0 ,$$

then the central limit theorem (12.33) holds.

Proof We apply the results of the preceding section, taking

$$h ( H _ { 1 } , \dots , H _ { m } ) \colon = \frac { 1 } { m ! } \psi ( H _ { 1 } \cap \cdots \cap H _ { m } \cap W ) .$$

For n ∈ [m] the function (12.21) is then given by h = (n)(m!)−1ψ. It follows from (12.35) and Lemma 12.17 that U, satisfies the integrability assumptions of Proposition 12.12 and Theorem 12.16. Hence (12.38) follows from (12.1) and (12.39) follows from (12.29). As noted at (12.25), the inequality (12.40) implies the non-degeneracy assumption of Theorem 12.16 and hence the central limit theorem. □

Under weak assumptions on λ the intersection of m different hyperplanes from η, is almost surely either empty or an affine space of dimension d – m. If we choose ψ(K) = Vd-(K) as the (d − m)-th intrinsic volume of K ∈ Kd, then U, is the total volume of the intersections of the (d – m)-dimensional faces of the hyperplane tessellation with W. This ψ satisfies the preceding assumptions. Another possible choice is ψ(K) = 1{K ≠ 0}. In that case Ut is the number of (d – m)-dimensional faces intersecting W.

### 12.5 Exercises

Exercise 12.1 Let η be a Poisson process on (0, ∞) with an intensity measure ν satisfying ∫ x ∧ 1 v(dx) &lt; ∞. Show that X := ∫ x η(dx) is a finite random variable with Laplace transform

$$\mathbb { E } [ \exp ( - t X ) ] = \exp \left [ - \int ( 1 - e ^ { - t x } ) \, \nu ( d x ) \right ] , \quad t \geq 0 .$$


<!-- p:136 -->


Show also that for each m ∈ N there are independent random variables X1, . . . , X with equal distribution such that X ≡ X1 + · . . + X. (Such an X is said to be infinitely divisible.)

Exercise 12.2 Suppose that v and v' are measures on (0, ∞) satisfying ∫ x ∧ 1 (ν + v′)(dx) &lt; ∞. Assume that ∫(1 − e−tx) v(dx) = ∫(1 − e−tx) ν′(dx), t ≥ 0. Show that v = v'. (Hint: Take derivatives and apply Proposition B.4 to suitable transforms of v and v'.)

Exercise 12.3 Let f ∈ R(X) satisfy (12.8); define g := 1{|f| ≤ 1}f and h := 1{lf| &gt; 1}f. Show that

$$\int _ { \ } g ^ { 2 } \, d \lambda + \int | h | \, d \lambda = \int | f | \wedge | f | ^ { 2 } \, d \lambda .$$

This result justifies the definition I(f) := I(g) + I(h), where I(g) is given by Definition 12.5 and I(h) := η(h) − λ(h). Let fn ∈ R(X), n ∈ N, be bounded such that λ({fn ≠ 0}) &lt; ∞, | fn| ≤ |f| and fn → f. Show that I(fn) → I(f) in probability.

Exercise 12.4 Prove Proposition 12.9.

Exercise 12.5 Let f, g ∈ L1,2(λ) and assume moreover that the functions f g2, f2g and f2 g2 are all in L1(λ). Show that

$$\mathbb { E } [ I ( f ) ^ { 2 } I ( g ) ^ { 2 } ] = \lambda ( f ^ { 2 } ) \lambda ( g ^ { 2 } ) + 2 [ \lambda ( f g ) ] ^ { 2 } + \lambda ( f ^ { 2 } g ^ { 2 } ) .$$

In particular, E[I(f)4] = 3[λ(f2)]2 + λ(f4) provided that f ∈ L1(λ) ∩ L4(λ).

Exercise 12.6 Let f ∈ L1(λ2) and g ∈ L1(λ). Show that

$$\mathbb { E } [ I _ { 2 } ( f ) ^ { 2 } I _ { 1 } ( g ) ] = 4 \int f ( x _ { 1 } , x _ { 2 } ) ^ { 2 } g ( x _ { 1 } ) \, \lambda ^ { 2 } ( d ( x _ { 1 } , x _ { 2 } ) )$$

holds under suitable integrability assumptions on f and g.

Exercise 12.7 Let f, g ∈ L2(λ) be such that fg ∈ L2(λ). Show that I1(f)I1(g) = I2(f ⊗ g) + I1(f g) + λ(f g).

Exercise 12.8 Let m, n ∈ N. Let f ∈ L1(λ") and g ∈ L1(λn) be such that f ⊗ g = 0 on the generalised diagonal of Xm+n. Show that Im(f)I(g) = Im+n(f ⊗ g).

Exercise 12.9 Let fi ∈ L1(λ'i), i = 1, ..., l, where l, n1, . . . , ne ∈ N. Assume for each i ∈ [l] that fi ∈ Ll(λni) and {fi ≠ 0} ⊂ Bni, where B ∈ X


<!-- p:137 -->


satisfies λ(B) &lt; ∞. Show for σ ∈ ∏(n1, . . . , ne) that

$$\left ( \int ( \otimes _ { i = 1 } ^ { \ell } | f _ { i } | ) _ { \sigma } \, d \lambda ^ { | \sigma | } \right ) ^ { \ell } \leq \lambda ( B ) ^ { | \sigma | - n _ { 1 } } \int | f _ { 1 } | ^ { \ell } \, d \lambda ^ { n _ { 1 } } \cdots \lambda ( B ) ^ { | \sigma | - n _ { c } } \int | f _ { \ell } | ^ { \ell } \, d \lambda ^ { n _ { \ell } } .$$

Note that this implies (12.14). (Hint: Apply the multivariate Hölder inequality (A.3) in the case m = l and p1 = · . · = pm = m.)

Exercise 12.10 (Moment and factorial moment measures) Suppose that η is a proper point process with factorial moment measures α j, j ∈ N. Let m ∈ N and f ∈ R(Xm) such that E[ ∫ |f| dη"] &lt; ∞. Show that

$$\mathbb { E } \left [ \int f \, d \eta ^ { m } \right ] = \sum _ { \sigma \in \Pi _ { m } } \int f _ { \sigma } \, d \alpha _ { | \sigma | } .$$

Exercise 12.11 Suppose that η is a Poisson process on X with s-finite intensity measure λ. Let m ∈ N and f ∈ R+(Xn ×N). Show that

$$\intertext { i n t e s i t y m e a s u r e \ \lambda . \ L e t \ m \in \mathbb { N } \ a n d \ f \in \mathbb { R } _ { + } ( \mathbb { X } ^ { m } \times \mathbb { N } ) } \mathbb { E } [ \int f ( x _ { 1 } , \dots , x _ { m } , \eta ) \, \eta ^ { m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) ] \\ = \sum _ { \sigma \in \Pi _ { m } } \int \mathbb { E } [ f _ { \sigma } ( x _ { 1 } , \dots , x _ { | \sigma | } , \eta + \delta _ { x _ { 1 } } + \cdots + \delta _ { x _ { | \sigma | } } ) \\ \text {where } f \left ( \sigma , \psi \right ) \coloneqq ( f ( \sigma , \psi ) ) \text { for each } \psi \in \mathbb { N }$$

where fσ(·, μ) := (f(·, μ))σ for each μ ∈ N.

Exercise 12.12 Show that the mapping (u, r) → Hu,r from Sd-1 × R to Hd-1 is measurable; see (12.34). (Hint: For any compact set K ⊂ Rd the set {(u, r) : H(u, r) ∩ K = 0} is open in Sd−1 × R.)

Exercise 12.13 Let the measure λ1 on Hd-1 be given by

$$( 1 2 . 4 1 )$$

where γ &gt; 0 and the directional distribution Q is a probability measure on the unit sphere. For t &gt; 0 let ηt be a Poisson process with intensity measure λ := tλ. Show that λ, satisfies (12.35). Show also that ηt is stationary in the sense that the distribution of θxηt does not depend on x ∈ Rd. Here, for any point x ∈ Rd and any measure μ on Hd–1, θxμ denotes the measure μ({H : H − x ∈ ·}).


<!-- p:138 -->


## Random Measures and Cox Processes

A Cox process is a Poisson process with a random intensity measure and hence the result of a doubly stochastic procedure. The study of Cox processes requires the concept of a random measure, a natural and important generalisation of a point process. The distribution of a Cox process determines that of its random intensity measure. Mecke's characterisation of the Poisson process via a functional integral equation extends to Cox processes.

### 13.1 Random Measures

A Cox process (here denoted η) can be interpreted as the result of a doubly stochastic procedure, which generates first a random measure ξ and then a Poisson process with intensity measure ξ. Before making this idea precise we need to introduce the concept of a random measure. Fortunately, the basic definitions and results are natural extensions of what we have seen before.

Let (X, X) be a measurable space and let M(X) ≡ M denote the set of all s-finite measures μ on X. Let M(X) ≡ M denote the σ-field generated by all sets of the form

$$\{ \mu \in \mathbf M \colon \mu ( B ) \leq t \} , \ \ B \in \mathcal { X } , \, t \in \mathbb { R } _ { + } .$$

This is the smallest σ-field of subsets of M such that μ → μ(B) is a measurable mapping for all B ∈ X.

For the following and later definitions we recall that all random elements are defined on a fixed probability space (Ω, F, P).

Definition 13.1 A random measure on X is a random element ξ of the space (M, M), that is, a measurable mapping ξ: Ω → M.

As in the case of point processes, if ξ is a random measure and B ∈ X, then we denote by ξ(B) the random variable ω → ξ(ω, B) := ξ(ω)(B). The mapping (ω, B) → ξ(ω, B) is a kernel from Ω to X with the additional property that the measure ξ(ω, ·) is s-finite for each ω ∈ Ω.


<!-- p:139 -->


The distribution of a random measure ξ on X is the probability measure Pξ on (M, M), given by A → P(ξ ∈ A). As in the point process seto eo  en  o eo is e s eos (ξ(B1), . . , ξ(Bm)) for pairwise disjoint B1, . . . , Bm ∈ X and m ∈ N. It is also determined by the Laplace functional Lξ: R+(X) → [0, 1] defined by

$$L _ { \xi } ( u ) \colon = \mathbb { E } \left [ \exp \left ( - \int u ( x ) \, \xi ( d x ) \right ) \right ] , \quad u \in \mathbb { R } _ { + } ( \mathbb { X } ) .$$

For ease of reference we summarise these facts with the following Proposition.

Proposition 13.2 Let η and η' be random measures on X. Then the assertions (i)–(iv) of Proposition 2.10 are equivalent.

Proof The proof is essentially the same as that of Proposition 2.10. . □

The intensity measure of a random measure ξ is the measure v on X defined by v(B) := E[ξ(B)], B ∈ X. It satisfies Campbell's formula

$$\mathbb { E } \left [ \int v ( x ) \, \xi ( d x ) \right ] = \int v ( x ) \, \nu ( d x ) , \quad v \in \mathbb { R } _ { + } ( \mathbb { X } ) , \quad ( 1 3 . 1 )$$

which can be proved in the same manner as Proposition 2.7. For m ∈ N we can form the m-th power ξm of ξ, that is ξTM := ξ(·)m. This is a random measure on Xn; see Exercise 13.3. The m-th moment measure of a random measure ξ is the measure β on X defined by

$$\beta _ { m } ( B ) \colon = \mathbb { E } [ \xi ^ { m } ( B ) ] , \quad B \in \mathcal { X } ^ { m } .$$

By definition, any point process is a random measure, even though, in the present generality, we cannot prove that N is a measurable subset of M. Here is another class of random measures. Later in the book we shall encounter further examples.

Example 13.3 Let (Y(x))x∈x be a non-negative random field on X, that is a family of R+-valued variables ω → Y(ω, x). Assume that the random field is measurable, meaning that (ω, x) → Y(ω, x) is a measurable mapping on Ω × X. Let γ be a σ-finite measure on X. Then

$$\xi ( B ) \colon = \int 1 _ { B } ( x ) Y ( x ) \, \nu ( d x ) , \quad B \in \mathcal { X } ,$$

defines a random measure ξ. Indeed, that ξ(ω, ·) is s-finite is a general fact from measure theory and easy to prove. The same is true for the measurablity of ω → ξ(ω, B); see also the paragraph preceding Fubini's theorem (Theorem A.13). The intensity measure of ξ is the measure with density E[Y(x)] with respect to v.


<!-- p:140 -->


### 13.2 Cox Processes

Given λ ∈ M(X), let IIλ denote the distribution of a Poisson process with intensity measure λ. The existence of II, is guaranteed by Theorem 3.6.

Lemma 13.4 Let f ∈ R+(N). Then λ ↔ ΠIλ(f) = ∫ f dΠλ is a measurable mapping from M to R+.

pdro  {  = ( )   ·  = ((} = (rf t   fomde m ∈ N, B1, . . . , Bm ∈ X and k1, . . . , km ∈ N0. Let C1, . . . , Cn be the atoms of the field generated by B1, . . . , B; see Section A.1. Then II(f) is a linear combination of the probabilities

$$\Pi _ { \lambda } ( \{ \mu \in N \colon \mu ( C _ { 1 } ) = \ell _ { 1 } , \dots , \mu ( C _ { n } ) = \ell _ { n } \} ) = \prod _ { i = 1 } ^ { n } \frac { \lambda ( C _ { i } ) ^ { \ell _ { i } } } { \ell _ { i } ! } \exp [ - \lambda ( C _ { i } ) ] , \\$$

where l1, . . . , ln ∈ N0. These products are clearly measurable functions of λ. By the monotone class theorem (Theorem A.1) the measurability property extends to f = 1A for arbitrary A ∈ N. The general case follows from monotone convergence. □

Definition 13.5 Let ξ be a random measure on X. A point process η on X is called a Cox process directed by ξ if

$$\mathbb { P } ( \eta \in A \, | \, \xi ) = \Pi _ { \xi } ( A ) , \quad \mathbb { P } \text {-a.s.} , \, A \in \mathcal { N } .$$

Then ξ is called a directing random measure of η.

Let ξ be a random measure on X. By Lemma 13.4 the right-hand side of (13.3) is a random variable for any fixed A ∈ N. The left-hand side is a conditional probability as defined in Section B.4. Equation (13.3) is equivalent to

$$\mathbb { E } [ h ( \xi ) \mathbf 1 \{ \eta \in A \} ] = \mathbb { E } [ h ( \xi ) \Pi _ { \xi } ( A ) ] , \quad A \in \mathcal { N } , \, h \in \mathbb { R } _ { + } ( \mathbf M ) .$$

Bmonno so no non n tnons s tno  on can be extended to

$$\mathbb { E } [ g ( \xi , \eta ) ] = \mathbb { E } \left [ \int g ( \xi , \mu ) \, \Pi _ { \xi } ( d \mu ) \right ] , \quad g \in \mathbb { R } _ { + } ( M \times N ) .$$


<!-- p:141 -->


Given any probability measure Q on (M, M), it is always the case that a Cox process directed by a random measure with distribution Q exists. For instance, (Ω, F, P) can be taken as (Ω, F) = (M × N, M ⊗ N) and

$$\mathbb { P } ( \cdot ) \colon = \iint 1 \{ ( \lambda , \mu ) \in \cdot \} \, \Pi _ { \lambda } ( d \mu ) \, \mathbb { Q } ( d \lambda ) .$$

Taking ξ and η as the first and second projections from Ω to M and N, respectively, it is easy to check that Pξ = Q and that (13.3) holds.

Suppose η is a Cox process on X directed by a random measure ξ. Taking in (13.5) a function g of product form yields

$$\mathbb { E } [ f ( \eta ) \, | \, \xi ] = \int f ( \mu ) \, \Pi _ { \xi } ( d \mu ) , \quad \mathbb { P } { \text {-a.s.} } , \, f \in \mathbb { R } _ { + } ( \text {N} ) .$$

As a first consequence we obtain for all B ∈ X that

$$\mathbb { E } [ \eta ( B ) ] = \mathbb { E } [ \mathbb { R } [ \eta ( B ) \ | \ \xi ] ] = \mathbb { E } \left [ \int \mu ( B ) \, \Pi _ { \xi } ( d \mu ) \right ] = \mathbb { E } [ \xi ( B ) ] ,$$

where we have used that ∫ μ(B) ΠIλ(dμ) = λ(B) for all λ ∈ M. Hence ξ and η have the same intensity measure. The next result deals with the second moment measure.

Proposition 13.6 Let η be a Cox process on X with directing random measure ξ. Let v ∈ L1(v), where ν is the intensity measure of ξ. Then E[η(v)2] &lt; ∞ if and only if E[ξ(v)2] &lt; ∞ and v ∈ L2(ν). In this case

$$\mathbb { W } a r [ \eta ( v ) ] = \nu ( v ^ { 2 } ) + \mathbb { V } a r [ \xi ( v ) ] .$$

Proof Let λ ∈ M and assume that v ∈ L1(λ) with v ≥ 0. By (4.26)

$$\int ( \mu ( v ) ) ^ { 2 } \, \Pi _ { \lambda } ( d \mu ) = \lambda ( v ^ { 2 } ) + ( \lambda ( v ) ) ^ { 2 } ,$$

first under the additional assumption v ∈ L2(λ) but then, allowing for the value ∞ on both sides of (13.9), for general v ∈ L1(λ). From equation (13.7) and Campbell's formula (13.1) we have E[η(v)] = E[ξ(v)] = v(v) &lt; ∞, so that we can apply (13.9) for Pξ-a.e. λ. It follows that

$$\mathbb { E } [ ( \eta ( v ) ) ^ { 2 } ] = \mathbb { E } [ \mathbb { E } [ ( \eta ( v ) ) ^ { 2 } \ | \ \xi ] ] = \mathbb { E } [ \xi ( v ^ { 2 } ) ] + \mathbb { E } [ ( \xi ( v ) ) ^ { 2 } ] = \nu ( v ^ { 2 } ) + \mathbb { E } [ ( \xi ( v ) ) ^ { 2 } ] .$$

This shows the asserted equivalence for v ≥ 0. The general case follows by taking positive and negative parts of v. The formula (13.8) for the variance follows upon subtracting (E[η(v)])2 = (E[ξ(v)])2 from both sides. □


<!-- p:142 -->


If η′ is a Poisson process with intensity measure v, then v(v2) is the variance of η'(v) by (4.26). If η is a Cox process with intensity measure v, then (13.8) shows that the variance of η(v) is at least the variance of η'(v). A Cox process is Poisson only if the directing measure is deterministic.

Corollary 4.10 and the law of total expectation show that the factorial moment measures of a Cox process η directed by ξ are given by

$$\mathbb { E } [ \eta ^ { ( m ) } ( \cdot ) ] = \mathbb { E } [ \xi ^ { m } ( \cdot ) ] , \ \ m \in \mathbb { N } ,$$

where E[ξ(·)] is the m-th moment measure of ξ; see (13.2).

The next result shows that the distribution of a Cox process determines that of the directing random measure.

Theorem 13.7 Let η and η′ be Cox processes on X with directing random measures ξ and ξ′, respectively. Then η = η′ if and only if ξ = ξ′.

Proof Suppose ξ≡ ξ′. By (13.3) we have for each A ∈ N that

$$\mathbb { P } ( \eta \in A ) = \mathbb { E } [ \Pi _ { \xi } ( A ) ] = \mathbb { E } [ \Pi _ { \xi ^ { \prime } } ( A ) ] = \mathbb { P } ( \eta ^ { \prime } \in A ) ,$$

and hence η = η′.

Assume, conversely, that η = η'. By (13.6) and Theorem 3.9,

$$\mathbb { E } [ \exp [ - \eta ( u ) ] ] = \mathbb { E } \left [ \exp \left ( - \int ( 1 - e ^ { - u ( x ) } ) \, \xi ( d x ) \right ) \right ] , \quad u \in \mathbb { R } _ { + } ( \mathbb { X } ) . \ \ ( 1 3 . 1 1 )$$

A similar equation holds for the pair (η′, ξ′). Let v: X → [0, 1) be measurable. Taking u := − log(1 − v) in (13.11) shows that

$$\mathbb { E } [ \exp [ - \xi ( v ) ] ] = \mathbb { E } [ \exp [ - \xi ^ { \prime } ( v ) ] ] .$$

For any such v we then also have E[exp[-tξ(v)]] = E[exp[-tξ'(v)]] for each t ∈ [0, 1]. Proposition B.5 shows that ξ(v) ≡ ξ′(v). The latter identity can be extended to arbitrary bounded v and then to any v ∈ R+(X) using monotone convergence. An application of Proposition 13.2 concludes the proof. . □

### 13.3 The Mecke Equation for Cox Processes

In this section we extend Theorem 4.1.

Theorem 13.8 Let ξ be a random measure on X and let η be a point process on X. Then η is a Cox process directed by ξ if and only if we have for every f ∈ R+(X ×N ×M) that

$$\mathbb { E } \left [ \int f ( x , \eta , \xi ) \, \eta ( d x ) \right ] = \mathbb { E } \left [ \int f ( x , \eta + \delta _ { x } , \xi ) \, \xi ( d x ) \right ] .$$


<!-- p:143 -->


Proof Suppose that η is a Cox process directed by the random measure ξ and let f ∈ R+(X × N × M). By taking g(ξ, η) = ∫ f(x, η, ξ) η(dx) in (13.5), the left-hand side of (13.12) equals

$$\mathbb { E } \left [ \iint f ( x , \mu , \xi ) \mu ( d x ) \, \Pi _ { \xi } ( d \mu ) \right ] = \mathbb { E } \left [ \iint f ( x , \mu + \delta _ { x } , \xi ) \, \xi ( d x ) \, \Pi _ { \xi } ( d \mu ) \right ] ,$$

where we have used Theorem 4.1 to get the equality. Applying (13.5) again yields (13.12).

Assume, conversely, that

$$\mathbb { E } \left [ h ( \xi ) \int g ( x , \eta ) \, \eta ( d x ) \right ] = \mathbb { E } \left [ \int h ( \xi ) g ( x , \eta + \delta _ { x } ) \, \xi ( d x ) \right ]$$

for all g ∈ R+(X ×N) and h ∈ R+(M). This implies that

$$\mathbb { E } \left [ \int _ { } g ( x , \eta ) \, \eta ( d x ) \, \Big | \, \xi \right ] = \mathbb { E } \left [ \int _ { } g ( x , \eta + \delta _ { x } ) \, \xi ( d x ) \, \Big | \, \xi \right ] , \quad \mathbb { P } \text {-a.s.} \quad ( 1 3 . 1 3 )$$

If there were a regular conditional probability distribution of η given ξ, we could again appeal to Theorem 4.1 to conclude that η is a Cox process. As this cannot be guaranteed in the present generality, we have to resort to the proof of Theorem 4.1 and take disjoint sets A1, . . . , A in X and k1, . . . , km ∈ N0 with k1 &gt; 0. Then (13.13) implies, as in the proof of Theorem 4.1, that

$$k _ { 1 } \mathbb { P } ( \eta ( A _ { 1 } ) = k _ { 1 } , \dots , \eta ( A _ { m } ) = k _ { m } \, | \, \xi ) \\ = \xi ( A _ { 1 } ) \mathbb { P } ( \eta ( A _ { 1 } ) = k _ { 1 } - 1 , \eta ( A _ { 2 } ) = k _ { 2 } , \dots , \eta ( A _ { m } ) = k _ { m } \, | \, \xi ) , \quad \mathbb { P } \text {-a.s.} ,$$

with the measure theory convention ∞ · 0 := 0. This implies that

$$\mathbb { P } ( \eta ( A _ { 1 } ) = k _ { 1 } , \dots , \eta ( A _ { m } ) = k _ { m } \ | \ \xi ) = \prod _ { j = 1 } ^ { m } \frac { \xi ( A _ { j } ) ^ { k _ { j } } } { k _ { j } ! } \exp [ - \xi ( A _ { j } ) ] , \quad \mathbb { P } \text {-a.s.} ,$$

for all k1, . . . , km ∈ N0, where we recall that (∞k) exp[-∞] := 0 for all k ∈ N0. This is enough to imply (13.3). □

### 13.4 Cox Processes on Metric Spaces

In this section we assume that X is a complete separable metric space. Let M denote the set of all locally finite measures on X. Also let Mld denote the set of all locally finite measures on X that are also diffuse.

Lemma 13.9 The sets M and Mld are measurable subsets of M.


<!-- p:144 -->


Proof Just as in the case of Nl, the measurability of M, follows from the fact that a measure μ on X is locally finite if and only if μ(B) &lt; ∞ for all n ∈ N, where B denotes the ball B(x0, n) for some fixed x0 ∈ X.

To prove the second assertion, we note that a measure μ ∈ M is in Ma if and only if μB ∈ M&lt;∞ ∩ Mld for each n ∈ N, where M&lt;∞ is the set of all finite measures on X. Hence it suffices to prove that M&lt;∞∩ Ma is measurable. This follows from Exercise 13.10. Indeed, a measure μ ∈ M&lt;∞ is diffuse if and only if τ(μ) = 0 for each n ∈ {1, . . . , k(μ)}. □

Definition 13.10 A random measure ξ on a metric space X is said to be locally finite if P(ξ(B) &lt; ∞) = 1 for each bounded B ∈ X. A locally finite random measure ξ on X is said to be diffuse if P(ξ ∈ Mld) = 1.

The next result says that the one-dimensional marginals of a diffuse random measure determine its distribution. Recall from Definition 2.11 that X denotes the system of bounded sets in X.

Theorem 13.11 Let ξ and ξ′ be locally finite random measures on X and assume that ξ is diffuse. If ξ(B) = ξ′(B) for all B ∈ Xb, then ξ = ξ′.

Proof Let η and η' be Cox processes directed by ξ and ξ', respectively. Then η and η' are locally finite. Moreover, by Proposition 6.9 and Lemma 13.9 the point process η is simple. Assuming ξ(B) = ξ′(B) for all B ∈ Xb we have for all such B that P(η(B) = 0) = P(η'(B) = 0). Let

$$\eta ^ { ^ { * } } \colon = \int \eta ^ { \prime } \{ x \} ^ { \oplus } 1 \{ x \in \cdot \} \, \eta ^ { \prime } ( d x )$$

be the simple point process with the same support as η', where we recall from Exercise 8.7 that a® := 1{a ≠ 0}a−1 is the generalised inverse of a ∈ R. Then η ≡ η* by Theorem 6.11. Since E[η(B)] = E[η'(B)] we have in particular that E[η'(B)] = E[η*(B)], and since η′(B) ≥ η*(B) we obtain the relation P(η'(B) = η*(B)) = 1. By the separability of X, there is an at most countably infinite π-system H ⊂ X containing only bounded sets and generating X. We have just proved that η and η' almost surely coincide on H. Theorem A.5 shows that this extends to X and hence that η = η'. Now we can conclude the proof using Theorem 13.7. □

### 13.5 Exercises

Exercise 13.1 Let f ∈ R+(X × Ω) and let ξ be a random measure on X. For ω ∈ Ω and B ∈ X define ξ′(ω, B) := ∫ 1{x ∈ B}f(x, ω) ξ(ω, dx). Show that ω → ξ′(ω, ·) is a random measure on X.


<!-- p:145 -->


Exercise 13.2 Let η be a Cox process directed by ξ and let f ∈ R+ (X×N). Show that

$$\mathbb { E } \left [ \int f ( x , \eta ) \, \xi ( d x ) \, \left | \, \xi \right \} = \int \mathbb { E } [ f ( x , \eta ) \, | \, \xi ] \, \xi ( d x ) , \quad \mathbb { P } \text {-a.s.} \\$$

(Hint: Use the monotone class theorem.)

Exercise 13.3 Let ξ be a random measure on X and let m ∈ N. Show that ξm is a random measure on Xm.

Exercise 13.4 Let η be a Cox process directed by a random measure of the form Yρ, where Y ≥ 0 is a random variable and ρ is an s-finite measure on X. Then η is called a mixed Poisson process. Assume now, in particular, that Y has a Gamma distribution with shape parameter a and scale parameter b, where a, b &gt; 0; see (1.27). Let B ∈ X with 0 &lt; ρ(B) &lt; ∞; show that

$$\mathbb { P } ( \eta ( B ) = n ) = \frac { \Gamma ( n + a ) } { \Gamma ( n + 1 ) \Gamma ( a ) } \left [ \frac { \rho ( B ) } { b + \rho ( B ) } \right ] ^ { n } \left [ \frac { b } { b + \rho ( B ) } \right ] ^ { a } , \quad n \in \mathbb { N } _ { 0 } .$$

This is a negative binomial distribution with parameters p = b and a; b+ρ(B) see (1.22).

Exercise 13.5 Let η be a Cox process directed by ξ and let B ∈ X. Show that ηB is a Cox process directed by ξB.

Exercise 13.6 Let ξ be a random measure on X with P(0 &lt; ξ(B) &lt; ∞) = 1 for some B ∈ X. For m ∈ N, define a probability measure Qm on M × Xn by

$$\iint \mathfrak { 1 } \{ ( \lambda , x _ { 1 } , \dots , x _ { m } ) \in \cdot \} \left ( \lambda ( B ) ^ { m } \right ) ^ { \oplus } ( \lambda _ { B } ) ^ { m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) \, \mathbb { V } ( d \lambda ) ,$$

where V is the distribution of ξ. Show that there is a unique probability measure Q on M × X∞ satisfying Q(A × B × X∞) = Qm(A × B) for all m ∈ N, A ∈ M and B ∈ Xm. (Hint: Use Theorem B.2.)

Exercise 13.7 Let ξ be a random measure on X such that P(ξ(B) &lt; ∞) = 1 for some measurable partition {B : n ∈ N} of X. Construct a suitable probability space supporting a proper Cox process directed by ξ.

Exercise 13.8 Let η be a Cox process directed by a random measure ξ satisfying the assumption of Exercise 13.7. Assume η to be proper and let χ be a K-marking of η, where K is a probability kernel from X to some measurable space (Y, Y). Show that χ has the distribution of a Cox process directed by the random measure ξ := ff 1{(x, y) ∈ ·} K(x, dy) ξ(dx). Show in particular that, for any measurable p: X → [0, 1], a p-thinning of η has the distribution of a Cox process directed by the random measure p(x) ξ(dx). (Hint: Use Proposition 5.4 and (13.11).)


<!-- p:146 -->


Exercise 13.9 Suppose that the assumptions of Exercise 13.8 are satisfied. Assume in addition that the sequence (Y)≥1 used in Definition 5.3 to define the K-marking of η is conditionally independent of ξ given (κ, (X)n≤κ). Show that χ is a Cox process directed by ξ.

Exercise 13.10 Let X be a Borel space and let M&lt; denote the space of all finite measures on X. Show that there are measurable mappings τn : M&lt;∞ → (0, ∞) and πn: M&lt;∞ → X, n ∈ N, along with measurable simple, D(μ) is diffuse for each μ ∈ M&lt;∞ and

$$\mu = D ( \mu ) + \sum _ { n = 1 } ^ { k ( \mu ) } \tau _ { n } ( \mu ) \delta _ { \pi _ { n } ( \mu ) } , \quad \mu \in M _ { < \infty } .$$

(Hint: Extend the method used in the proof of Proposition 6.2.)

Exercise 13.11 Assume that X is a CSMS. Show that N, is a measurable subset of M. (Hint: Use that X has a countable generator).

Exercise 13.12 Let d ∈ N. Given x ∈ Rd and μ ∈ M(Rd), define θxμ ∈ M(Rd) as in (8.1). A random measure ξ on Rd is said to be stationary if θxξ ≡ ξ for each x ∈ Rd. In this case the number E[ξ[0, 1]d] is called the intensity of ξ. Show that the intensity measure of a stationary random measure with finite intensity is a multiple of Lebesgue measure.

Exercise 13.13 Let d ∈ N and let η be a stationary random measure on Rd with finite intensity. Show that Theorem 8.14 remains valid with an appropriately defined invariant σ-field Iη.

Exercise 13.14 Let p ∈ (0, 1). Suppose that ηp (resp. η′) is a p-thinning of a proper point process η (resp. η'). Assume that ηp = η′p and show that η = η' (Hint: Use Exercise 5.4 and the proof of Theorem 13.7.)

Exercise 13.15 Let p ∈ (0, 1) and let η be a proper point process with s-finite intensity measure. Suppose that ηp is a p-thinning of η and that ηp and η − ηp are independent. Show that η is a Poisson process. (Hint: Use Exercise 5.9 to show that ηp satisfies the Mecke equation. Then use Exercise 13.14.)


<!-- p:147 -->


## Permanental Processes

For α &gt; 0, an α-permanental point process is defined by explicit algebraic formulae for the densities of its factorial moment measures. These densities are the α-permanents arising from a given non-negative definite kernel function K and determine the distribution. If 2α is an integer, then an α-permanental process can be constructed as a Cox process, whose directing random measure is determined by independent Gaussian random fields with covariance function K. The proof of this fact is based on moment formulae for Gaussian random variables. The Janossy measures of a permanental Cox process are given as the α-permanent of a suitably modified kernel function. The number of points in a bounded region is a sum of independent geometric random variables.

### 14.1 Definition and Uniqueness

In this chapter the state space (X, X) is assumed to be a locally compact separable metric space equipped with its Borel σ-field; see Section A.2. A set B ⊂ X is said to be relatively compact if its closure is compact. Let Xrc denote the system of all relatively compact B ∈ X. We fix a measure v on X such that v(B) &lt; ∞ for every B ∈ Xrc. Two important examples are X = Rd with v being Lebesgue measure and X = N with v being counting measure.

Let m ∈ N and let σ ∈ Σ be a permutation of [m]. A cycle of σ is a ktuple (i1 . . . ik) ∈ [m]k with distinct entries (written without commas), where k ∈ [m], σ(ij) = i j+1 for j ∈ [k − 1] and σ(ik) = i1. In this case (i2 . . . ik i1) denotes the same cycle, that is cyclic permutations of a cycle are identified. The number k is called the length of the cycle. Let #σ denote the number of cycles of σ ∈ Σm. For r ∈ [m] let ∑mn) be the set of permutations of [m] with exactly r cycles.

Definition 14.1 Let m ∈ N. Let A = (ai,j)i,j∈[m] be an (m × m)-matrix of real numbers. For r ∈ [m] let


<!-- p:148 -->


$$\text {per} ^ { ( r ) } ( A ) \colon = \sum _ { \sigma \in \Sigma _ { m } ^ { ( r ) } } \prod _ { i = 1 } ^ { m } a _ { i , \sigma ( i ) } .$$

For α ∈ R the α-permanent of A is defined by

$$\ p e r _ { \alpha } ( A ) \colon = \sum _ { \sigma \in \Sigma _ { m } } \alpha ^ { \# \sigma } \prod _ { i = 1 } ^ { m } a _ { i , \sigma ( i ) } = \sum _ { r = 1 } ^ { m } \alpha ^ { r } \ p e r ^ { ( r ) } ( A ) .$$

The number per,(A) is called the permanent of A.

We note that per\_1(-A) is the determinant of A.

Let X* denote the support of v. In this chapter we fix a symmetric jointly continuous function (sometimes called a kernel) K: X* × X* → R. We assume that K is non-negative definite; see (B.11). We extend K to X × X by setting K(x, y) := 0 for (x, y) ∉ X* × X*. For m ∈ N and x1, . . . , χm ∈ X we define [K](x1, . . . , xm) to be the (m × m)-matrix with entries K(xi, xj). Since K is continuous it is bounded on compact subsets of X*, so that

$$\sup \{ | K ( x , y ) | \colon x , y \in B \} < \infty , \quad B \in \mathcal { X } _ { r c } .$$

Definition 14.2 Let α &gt; 0. A point process η on X is said to be an αpermanental process with kernel K (with respect to v) if for every m ∈ N the m-th factorial moment measure of η is given by

$$\alpha _ { m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) = \text {per} _ { \alpha } ( [ K ] ( x _ { 1 } , \dots , x _ { m } ) ) \, v ^ { m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) .$$

If η is α-permanental with kernel K, then the case m = 1 of (14.2) implies that the intensity measure of η is given by

$$\mathbb { E } [ \eta ( B ) ] = \int _ { B } \alpha K ( x , x ) \, \nu ( d x ) , \quad B \in \mathcal { X } .$$

If B ∈ Xrc, then the relation (14.1) and our assumption v(B) &lt; ∞ imply = (∞ &gt; (t d   ∞ &gt; [] (1)

Proving existence of an α-permanental point process with a given kernel is a non-trivial task and is one of the themes of the rest of this chapter. We note first that the distribution of a permanental process is uniquely determined by its kernel.

Proposition 14.3 Let α &gt; 0. Suppose that η and η' are α-permanental processes with kernel K. Then η = η′'.


<!-- p:149 -->


Proof Let B ⊂ X be compact. It follows from (14.1) and v(B) &lt; ∞ that |perq([K](x1, . ., χm))| νm(d(x1, . . . , χxm)) ≤ m!(max{α, 1}) c−ν(B)m JBm

for some c &gt; 0. Since X is σ-compact (by Lemma A.20), the assertion follows from Proposition 4.12. □

We continue with a simple example.

Example 14.4 Suppose that X = {1} is a singleton and that v{1} = 1. A point process η on X can be identified with the random variable η{1}. Set γ := K(1, 1) ≥ 0. Let α &gt; 0 and m ∈ N. For (x1, . . . , χm) := (1, . . . , 1) and with Em denoting the (m × m)-matrix with all entries equal to 1, we have that

$$\ p e r _ { \alpha } ( [ K ] ( x _ { 1 } , \dots , x _ { m } ) ) & = \gamma ^ { m } \ p e r _ { \alpha } ( E _ { m } ) \\ & = \gamma ^ { m } \alpha ( \alpha + 1 ) \cdots ( \alpha + m - 1 ) ,$$

where the second identity follows from Exercise 14.1. By Definition 14.2, l s -     s d ()  ()

$$\mathbb { E } [ ( \eta ( \mathbb { X } ) ) _ { m } ] = \gamma ^ { m } \alpha ( \alpha + 1 ) \cdots ( \alpha + m - 1 ) , \ \ m \geq 1 .$$

Exercise 14.2 shows that these are the factorial moments of a negative binomial distribution with parameters α and 1/(1 + γ). Hence an α-permanental process with kernel K exists. Proposition 4.12 shows that its distribution is uniquely determined.

### 14.2 The Stationary Case

In this section we briefly discuss stationary permanental processes, assuming that X = Rd, ν = λd and the translation invariance

$$K ( x , y ) = K ( 0 , y - x ) , \ \ x , y \in \mathbb { R } ^ { d } .$$

For a given α &gt; 0 let η be an α-permanental process with kernel K (with respect to λd). Let x ∈ Rd and n ∈ N. Since

$$( \theta _ { x } \eta ) ^ { ( n ) } = \int 1 \{ ( x _ { 1 } - x , \dots , x _ { n } - x ) \in \cdot \} \, \eta ^ { ( n ) } ( d ( x _ { 1 } , \dots , x _ { n } ) ) ,$$

it follows from Definition 14.2 and (14.6) (and a change of variables) that θxη is also α-permanental with the same kernel K. Therefore Proposition


<!-- p:150 -->


14.3 shows that η is stationary. It follows from (14.3) that η has intensity αK(0, 0). Since

$$\ p e r _ { \alpha } ( [ K ] ( x , y ) ) = \alpha ^ { 2 } K ( x , x ) K ( y , y ) + \alpha K ( x , y ) K ( y , x ) ,$$

we can use (14.2) for m = 2 and a change of variables in (8.7), to see that the second reduced factorial moment measure α2 of η is given by

$$\alpha _ { 2 } ^ { ! } ( B ) = \int _ { B } ( \alpha ^ { 2 } K ( 0 , 0 ) ^ { 2 } + \alpha K ( 0 , x ) ^ { 2 } ) \, d x , \quad B \in \mathcal { B } ^ { d } .$$

By Definition 8.9 the pair correlation function ρ2 can be chosen as

$$\rho _ { 2 } ( x ) = 1 + \frac { K ( 0 , x ) ^ { 2 } } { \alpha K ( 0 , 0 ) ^ { 2 } } , \quad x \in \mathbb { R } ^ { d } .$$

Hence permanental processes are attractive; see (8.10).

### 14.3 Moments of Gaussian Random Variables

We now establish a combinatorial formula for mixed moments of normal random variables; later, we shall use this to show the existence in general of permanental processes. For l ∈ N let M(€) denote the set of matchings of [€] and note that M(€) is empty if l is odd. Recall that IIe denotes the system of all partitions of [€]. For any π ∈ Πe (in particular for π a matching) we denote the blocks of π (in some arbitrary order) as J1(π), . . . , J|π(π). In the case that π is a matching we write J(π) = {k,(π), k′(π)}.

Lemma 14.5 (Wick formula) Let l ∈ N and let f1, . . . , fe be functions on N such that Σm=1 fi(m)2 &lt; ∞ for all i ∈ {1, ..., l}. Let Y1, 2, ... be independent standard normal random variables and define

$$X _ { i } \colon = \sum _ { m = 1 } ^ { \infty } Y _ { m } f _ { i } ( m ) , \ \ i = 1 , \dots , \ell .$$

Then

$$\mathbb { E } \left [ \prod _ { i = 1 } ^ { \ell } X _ { i } \right ] = \sum _ { \pi \in M ( \ell ) } \prod _ { i = 1 } ^ { \ell / 2 } \left ( \sum _ { m = 1 } ^ { \infty } f _ { k _ { i } ( \pi ) } ( m ) f _ { k _ { i } ( \pi ) } ( m ) \right ) .$$

Proof Let λ0 denote the counting measure on N. We first show that both sides of (14.9) depend on each of the individual functions f1, . . . , fe in an L2(λ0)-continuous way. To see this we let f1n) ∈ L2(λ0) be such that f(n) → f1 in L2(λ0) as n → ∞. For each n ∈ N define X(n) by (14.8) with i = 1 and f1n) in place of f1. It is easy to check that E[(X1 − X(n)2] → 0 as n → ∞. Since normal random variables have moments of all orders, so does ∏k=2 X. By the Cauchy-Schwarz inequality,


<!-- p:151 -->


$$\lim _ { n \to \infty } \mathbb { E } \left [ \left | X - X _ { 1 } ^ { ( n ) } \right | \prod _ { i = 2 } ^ { \ell } X _ { i } \right ] = 0 ,$$

so that E[X(n) Πk=2 X] → E[ Π=1 X] as n → ∞. By another application of the Cauchy-Schwarz inequality, the right-hand side of (14.9) also depends on f1 in an L2(λ0)-continuous manner.

To prove (14.9) we can now assume that fi(m) = 0 for all i ∈ [€] and all sufficiently large m. We then obtain

$$\mathbb { E } [ \prod _ { i = 1 } ^ { \ell } X _ { i } ] = \sum _ { m _ { 1 } , \dots , m _ { \ell } = 1 } ^ { \infty } f _ { 1 } ( m _ { 1 } ) \cdots f _ { \ell } ( m _ { \ell } ) \mathbb { E } [ Y _ { m _ { 1 } } \cdots Y _ { m _ { \ell } } ] .$$

Each (m1, . . . , me) in the sum determines a partition σ ∈ IIe by letting i, k ∈ [l] be in the same block of σ if and only if mi = mk. Writing the distinct values of m1, . . . , me as n1, . . . , n|σ| and using (B.5) and (B.7), we may deduce that

$$\mathbb { J } & = \sum _ { \sigma \in \Pi _ { ( n _ { 1 } , \dots , n _ { | \sigma | } \in \mathbb { N } } \ \mathbb { N } } } \sum _ { i = 1 } ^ { \ell } \sum _ { \sigma ( | M ( | J _ { r } ( \sigma ) | ) | } \prod _ { i \in J _ { r } ( \sigma ) } f _ { i } ( n _ { r } ) ) } \\ & = \sum _ { \sigma \in \Pi _ { ( n _ { 1 } , \dots , n _ { | \sigma | } \in \mathbb { N } } \ \mathbb { N } } } \sum _ { n _ { 1 } , \dots , n _ { | \sigma | } \in \mathbb { N } } ^ { \neq } \prod _ { n = 1 } ^ { | \sigma | } \prod _ { i \in J _ { r } ( \sigma ) } f _ { i } ( n _ { r } ) ,$$

where cσ := ∏|=1 |M(J(σ)D)| is the number of matchings π ∈ M(€) such that each block of π is contained in a block of σ (that is, π is a refinement of σ).

Now consider the right-hand side of (14.9). By a similar partitioning argument to the above, this equals

$$\sum _ { \pi \in M ( \ell ) \ m _ { 1 } , \dots , m _ { n } / 2 } \prod _ { r = 1 } ^ { \infty } \prod _ { i \in J _ { r } ( \pi ) } f _ { i } ( m _ { r } ) = \sum _ { \pi \in M ( \ell ) \ \sigma \in \Pi _ { n / 2 } \ n _ { 1 } , \dots , n _ { n } | \sigma | \in \mathbb { N } } \sum _ { r = 1 } ^ { \infty } \prod _ { i \in J _ { n } ( \sigma , \pi ) } f _ { i } ( n _ { r } ) ,$$

where J(σ, π) := ∪j∈J,(σ)Jj(π). Each pair (π, σ) in the sum determines a partition π′ ∈ ΠIe by π′ := {Jr(π, σ) : 1 ≤ r ≤ |σ|}, and each π′ ∈ Πe is obtained from cπ such pairs. Hence, the last display equals the expression (14.10) so the result is proved. □


<!-- p:152 -->


### 14.4 Construction of Permanental Processes

In this section we construct α-permanental processes in the case 2α ∈ N. In fact, under certain assumptions on K such a process exists for other values of α (as already shown by Example 14.4) but proving this is beyond the scope of this volume. By Theorem B.17 and Proposition B.19 there exists a measurable centred Gaussian random field Z = (Z(x))x∈x with covariance function K/2, that is (Z(x1), . . . , Z(x)) has a multivariate normal distribution for all m ∈ N and (x1, . . . , xm) ∈ Xm, E[Z(x)] = 0 for all x ∈ X, and

$$\mathbb { E } [ Z ( x ) Z ( y ) ] = \frac { K ( x , y ) } { 2 } , \quad x , y \in \mathbb { X } .$$

Theorem 14.6 Let k ∈ N and let Z1, . . . , Zk be independent measurable random fields with the same distribution as Z. Define a random measure ξ on X by

$$\xi ( B ) \coloneqq \int _ { B } ( Z _ { 1 } ( x ) ^ { 2 } + \cdots + Z _ { k } ( x ) ^ { 2 } ) \, \nu ( d x ) , \quad B \in \mathcal { X } ,$$

and let η be a Cox process directed by ξ. Then η is (k/2)-permanental.

The proof of Theorem 14.6 is based on an explicit representation of the Gaussian random field Z in terms of independent standard normal random variables. For B ∈ Xrc let B* ⊂ X be the support of vB. Then B* is a closed subset of the closure of B (assumed to be compact) and therefore compact. By Lemma A.23,

$$\nu ( B \ \ B ^ { * } ) = 0 .$$

Applying Mercer's theorem (Theorem B.18) to the metric space B*, we see that there exist γB,j ≥ 0 and vB,j ∈ L2(νB), j ∈ N, such that

$$\int _ { B } v _ { B , i } ( x ) v _ { B , j } ( x ) \, \nu ( d x ) = 1 \{ \gamma _ { B , i } > 0 \} 1 \{ i = j \} , \quad i , j \in \mathbb { N } , \quad ( 1 4 . 1 4 )$$

and

$$K ( x , y ) = \sum _ { j = 1 } ^ { \infty } \gamma _ { B , j } v _ { B , j } ( x ) v _ { B , j } ( y ) , \quad x , y \in B ^ { * } , \quad ( 1 4 . 1 5 )$$

where the convergence is uniform and absolute. In (14.14) (and also later) we interpret vB,j as functions on B ∪ B* by setting vB,j(x) := 0 for x ∈ B \ B*. In view of (14.13) this modification has no effect on our subsequent calculations. A consequence of (14.15) is


<!-- p:153 -->


$$\sum _ { j = 1 } ^ { \infty } \gamma _ { B , j } v _ { B , j } ( x ) ^ { 2 } = K ( x , x ) < \infty , \quad x \in B ^ { * } \cup B .$$

Combining this with (14.14), we obtain from monotone convergence that

$$\sum _ { j = 1 } ^ { \infty } \gamma _ { B , j } = \int _ { B } K ( x , x ) \, \nu ( d x ) .$$

By (14.1) and v(B) &lt; ∞, this is a finite number.

Now let k ∈ N and let Yi,j, i = 1,.. . , k, j ∈ N, be a family of independent random variables with the standard normal distribution. Define independent measurable random fields ZB,i = (ZB,(x))x∈B*∪B, i ∈ [k], by

$$Z _ { B , i } ( x ) \coloneqq \frac { 1 } { \sqrt { 2 } } \sum _ { j = 1 } ^ { \infty } \sqrt { \gamma _ { B , j } } Y _ { i , j } v _ { B , j } ( x ) , \quad x \in B ^ { * } \cup B ,$$

making the convention that ZB,(x) := 0 whenever the series diverges. By (14.16) and Proposition B.7, (14.18) converges almost surely and in L2(P). Since componentwise almost sure convergence of random vectors implies convergence in distribution, it follows that ZB,1, . . . , ZB,k are centred Gaussian random fields. By the L2(P)-convergence of (14.18) and (14.15),

$$\mathbb { E } [ Z _ { B , i } ( x ) Z _ { B , i } ( y ) ] = \frac { 1 } { 2 } \sum _ { j = 1 } ^ { \infty } \gamma _ { B , j } v _ { B , j } ( x ) v _ { B , j } ( y ) = \frac { K ( x , y ) } { 2 } , \quad x , y \in B ^ { * } .$$

It follows that

$$( ( Z _ { B , 1 } ( x ) ) _ { x \in B ^ { * } } , \dots , ( Z _ { B , k } ( x ) ) _ { x \in B ^ { * } } ) \stackrel { d } { = } ( ( Z _ { 1 } ( x ) ) _ { x \in B ^ { * } } , \dots , ( Z _ { k } ( x ) ) _ { x \in B ^ { * } } ) .$$

Therefore, when dealing with the restriction of (Z1, . . ., Zk) to a given set B ∈ Xrc, we can work with the explicit representation (14.18). Later we shall need the following fact.

Lemma 14.7 Let B ∈ Xrc and WB(x) := ZB,1(x)2 + · · · + ZB,k(x)2, x ∈ B. Then we have P-a.s. that

$$\int _ { B } W _ { B } ( x ) \, \nu ( d x ) = \frac { 1 } { 2 } \sum _ { i = 1 } ^ { k } \sum _ { j = 1 } ^ { \infty } \gamma _ { B , j } Y _ { i , j } ^ { 2 } .$$


<!-- p:154 -->


Proof Let i ∈ {1, . . . , k} and n ∈ N. Then, by (14.18),

$$P r o f & \quad \text {Let } i \in \{ 1 , \dots , k \} \text { and } n \in \mathbb { N } . \text { Then, by } ( 1 4 . 1 8 ) , \\ & \quad \mathbb { B } \left [ \int _ { B ^ { * } } \left ( Z _ { B , i } ( x ) - \frac { 1 } { \sqrt { 2 } } \sum _ { j = 1 } ^ { n } \sqrt { \gamma _ { B , j } } Y _ { i , j } v _ { B , j } ( x ) \right ) ^ { 2 } \nu ( d x ) \right ] \\ & = \frac { 1 } { 2 } \int _ { B } \mathbb { E } \left [ \left ( \sum _ { j = n + 1 } ^ { \infty } \sqrt { \gamma _ { B , j } } Y _ { i , j } v _ { B , j } ( x ) \right ) ^ { 2 } \right ] \nu ( d x ) \\ & = \frac { 1 } { 2 } \int _ { B } \left ( \sum _ { j = n + 1 } ^ { \infty } \gamma _ { B , j } v _ { B , j } ( x ) ^ { 2 } \right ) \nu ( d x ) = \frac { 1 } { 2 } \sum _ { j = n + 1 } ^ { \infty } \gamma _ { B , j } \rightarrow 0 \quad a s \ n \to \infty , \\ \text {where we have used } ( 1 4 . 1 7 ) \text { to get the convergence. By Proposition } B . 8 ,$$

where we have used (14.17) to get the convergence. By Proposition B.8,

$$\int _ { B } \left ( Z _ { B , i } ( x ) - \frac { 1 } { \sqrt { 2 } } \sum _ { j = 1 } ^ { n } \sqrt { \gamma _ { B , j } } Y _ { i , j } v _ { B , j } ( x ) \right ) ^ { 2 } \nu ( d x ) \to 0$$

in probability. Hence we obtain from the Minkowski inequality that

$$\int _ { B } \left ( \frac { 1 } { \sqrt { 2 } } \sum _ { j = 1 } ^ { n } \sqrt { \gamma _ { B , j } } Y _ { i , j } v _ { B , j } ( x ) \right ) ^ { 2 } \nu ( d x ) \rightarrow \int _ { B } Z _ { B , i } ( x ) ^ { 2 } \, \nu ( d x )$$

in probability. By the orthogonality relation (14.14),

$$\int _ { B } \left ( \frac { 1 } { \sqrt { 2 } } \sum _ { j = 1 } ^ { n } \sqrt { \gamma _ { B , j } } Y _ { i , j } v _ { B , j } ( x ) \right ) ^ { 2 } \nu ( d x ) = \frac { 1 } { 2 } \sum _ { j = 1 } ^ { n } \gamma _ { B , j } Y _ { i , j } ^ { 2 } \rightarrow \frac { 1 } { 2 } \sum _ { j = 1 } ^ { \infty } \gamma _ { B , j } Y _ { i , j } ^ { 2 } ,$$

with almost sure convergence. Summing both limits over i ∈ {1,..., k} proves the result. □

Proof of Theorem 14.6 Let α := k/2. Let

$$W _ { k } ( x ) \colon = Z _ { 1 } ( x ) ^ { 2 } + \cdots + Z _ { k } ( x ) ^ { 2 } , \quad x \in \mathbb { X } .$$

In view of (14.12) and (13.10), we have for all m ∈ N and B ∈ X' that

$$\mathbb { E } [ \eta ^ { ( m ) } ( B ) ] = \int _ { R } \mathbb { E } [ W _ { k } ( x _ { 1 } ) \cdots W _ { k } ( x _ { m } ) ] \, \nu ^ { m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) .$$

Hence by Definition 14.2 we have to show that

$$\mathbb { E } [ W _ { k } ( x _ { 1 } ) \cdots W _ { k } ( x _ { m } ) ] = \text {per} _ { k / 2 } ( [ K ] ( x _ { 1 } , \dots , x _ { m } ) ) , \quad \nu ^ { m } \text {a.e.} \, ( x _ { 1 } , \dots , x _ { m } ) .$$

For the rest of the proof we fix m ∈ N and x1, . . . , xm ∈ X*. By (14.13) and (14.19) we can assume that Z = ZB, for every i ∈ {1, . . . , k}, where B ∈ Xrc satisfies {x1, . . . , xm} ⊂ B*.


<!-- p:155 -->


We first prove (14.21) for k = 1. Set (z1, . . . , Z2m) := (x1, x1, . . . , Xm, χm) and for i ∈ [2m], n ∈ N, set fi(n) = √γB,n/2vB,n(zi). Then, by (14.18),

$$a n d \, \text {for} \, 7 \in [ 2 n ] , \, h \in \mathbb { N } , \, & \leq \sqrt { \gamma _ { B , n } } \, 2 \sigma _ { B , n } ( \xi _ { i } ) . \, \text {In} \, \text {,} \\ W _ { 1 } ( x _ { 1 } ) \cdots W _ { 1 } ( x _ { m } ) & = Z _ { B , 1 } ( z _ { 1 } ) \cdots Z _ { B , 1 } ( z _ { 2 m } ) = \prod _ { r = 1 } ^ { 2 m } \left ( \sum _ { n = 1 } ^ { \infty } \sqrt { \frac { \gamma _ { B , n } } { 2 } } \, w _ { B , n } ( z _ { r } ) Y _ { 1 , n } \right ) \\ & = \prod _ { r = 1 } ^ { 2 m } \left ( \sum _ { j = 1 } ^ { \infty } f _ { r } ( j ) Y _ { 1 , j } \right ) . \\ \text {Hence we obtain from } ( 1 4 9 ) \text { that}$$

Hence we obtain from (14.9) that

$$\mathbb { E } [ W _ { 1 } ( x _ { 1 } ) \cdots W _ { 1 } ( x _ { m } ) ] & = \sum _ { \pi \in M ( 2 m ) } \prod _ { i = 1 } ^ { m } \left ( \sum _ { n = 1 } ^ { \infty } f _ { k _ { i } ( \pi ) } ( n ) f _ { k _ { i } ^ { ( \pi ) } ( \pi ) } ( n ) \right ) \\ & = \sum _ { \pi \in M ( 2 m ) } \prod _ { i = 1 } ^ { m } \left ( \sum _ { n = 1 } ^ { \infty } \frac { \gamma _ { B , n } } { 2 } v _ { B , n } ( z _ { k _ { i } ( \pi ) } ) v _ { B , n } ( z _ { k _ { i } ^ { ( \pi ) } ( \pi ) } ) \right ) ,$$

so, by (14.15),

$$\mathbb { E } [ W _ { 1 } ( x _ { 1 } ) \cdots W _ { 1 } ( x _ { m } ) ] = 2 ^ { - m } \sum _ { \pi \in M ( 2 m ) } \prod _ { i = 1 } ^ { m } K ( z _ { k _ { i } ( \pi ) , k _ { i } ^ { \prime } ( \pi ) } ) .$$

Any matching π ∈ M(2m) defines a permutation σ of [m]. The cycles of this permutation are defined as follows. Partition [2m] into m blocks Ji := {2i − 1, 2i}, i ∈ [m]. Let j2 ∈ [2m] such that {1, j2} ∈ π. Then j2 ∈ Ji2 for some i2 ∈ [m] and we define σ(1) := i2. If i2 = 1, then (1) is the first cycle of σ. Otherwise there is a j2 ∈ Ji \ {j2} and a j3 ∈ [2m] such that {j2, j3} ∈ π. Then j3 ∈ Ji3 for some i3 ∈ [m]; we let σ(i2) := i3. If i3 = 1, then (1 i2) is the first cycle. Otherwise we continue with this procedure. After a finite number of recursions we obtain the first cycle (i1 .. . ik) for some k ∈ [m], where i1 := 1. To get the second cycle we remove the blocks Ji, . . . , Jik and proceed as before (starting with the first available block). This procedure yields the cycles of σ after a finite number of steps. (In the case m = 3, for instance, the matching {{1, 2}, {3, 5}, {4, 6}} gives the permutation σ(1) = 1, σ(2) = 3 and σ(3) = 2. This permutation has two cycles.) The corresponding contribution to the right-hand side of (14.22) is

$$2 ^ { - m } \prod _ { i = 1 } ^ { m } K ( x _ { i } , x _ { \sigma ( i ) } )$$

and depends only on the permutation and not on the matching. Since any permutation σ of [m] with r cycles of lengths k1, . . . , k, corresponds to 2k1−1 . . . 2k−1 = 2m−r matchings, the case k = 1 of (14.21) follows.


<!-- p:156 -->


Finally consider a general k ∈ N. Let (x1, . . . , x) ∈ Xm such that (14.21) holds for k = 1. Then for k ∈ N, since (Z(x1)2, . . . , Z(xm)2), i ∈ [k], are independent vectors,

$$\text {dependent vectors,} \\ \mathbb { E } [ W _ { k } ( x _ { 1 } ) \cdots W _ { k } ( x _ { m } ) ] & = \mathbb { E } \left [ \sum _ { i _ { 1 } = 1 } ^ { k } \cdots \sum _ { i _ { m } = 1 } ^ { k } Z _ { i _ { 1 } } ( x _ { 1 } ) ^ { 2 } \cdots Z _ { i _ { m } } ( x _ { m } ) ^ { 2 } \right ] \\ & = \sum _ { \pi \in \Pi _ { m } } \sum _ { j _ { 1 } , \dots , j _ { m } \in [ k ] } \mathbb { E } \prod _ { s = 1 } ^ { | \pi | } \prod _ { r \in J _ { s } ( \pi ) } Z _ { j _ { r } } ( x _ { r } ) ^ { 2 } \right ] \\ & = \sum _ { \pi \in \Pi _ { m } } ( k ) _ { | \pi | } \prod _ { s = 1 } ^ { | \pi | } \mathbb { E } \left [ \prod _ { r \in J _ { s } ( \pi ) } Z _ { 1 } ( x _ { r } ) ^ { 2 } \right ] , \quad ( 1 4 . 2 3 ) \\ \text {and hence, by the case of } ( 1 4 . 2 1 ) \text { already proved,}$$

and hence, by the case of (14.21) already proved,

$$a n d \, \text {ence, by the case of (14 . 2 1) already proved,} \\ \mathbb { E } [ W _ { k } ( x _ { 1 } ) \cdots W _ { k } ( x _ { m } ) ] & = \sum _ { \pi \in \Pi _ { m } } ( k ) _ { \pi } \prod _ { J \in \pi } \, \text {per} _ { 1 / 2 } ( [ K ] ( ( x _ { j } ) _ { j \in J } ) ) \\ & = \sum _ { \pi \in \Pi _ { m } } ( k ) _ { \pi } \sum _ { \sigma \in \Xi _ { m } ; \pi \geq \sigma } ( 1 / 2 ) ^ { \# } \prod _ { i = 1 } ^ { m } \, K ( x _ { i } , x _ { \sigma ( i ) } ) , \\ \intertext { w h e r $ \pi > \sigma $ h e r $ \text {means that for each cycle of } \sigma \text { all entries in the cycle lie} }$$

where π ≥ σ here means that for each cycle of σ all entries in the cycle lie in the same block of π. Hence

$$\mathbb { E } [ W _ { k } ( x _ { 1 } ) \cdots W _ { k } ( x _ { m } ) ] = \sum _ { \sigma \in \Sigma _ { m } \, \pi \in \Pi _ { m } \colon \pi \geq \sigma } ( k ) _ { | \pi | } ( 1 / 2 ) ^ { \# \sigma } \prod _ { i = 1 } ^ { m } K ( x _ { i } , x _ { \sigma ( i ) } ) ,$$

and therefore the general case of (14.21) follows from the algebraic identity

$$\sum _ { \pi \in \Pi _ { n } } ( k ) _ { | \pi | } & = k ^ { n } , \quad k , n \in \mathbb { N } . \\$$

This identity may be proved by the same argument as in (14.23) (namely decomposition of multi-indices according to the induced partition), but now with each of the variables Z(xj) replaced by the unit constant. □

### 14.5 Janossy Measures of Permanental Cox Processes

In this section we provide a more detailed analysis of the probabilistic properties of the (k/2)-permanental Cox processes for k ∈ N.

Let B ∈ Xrc and let γB,1, . . . , γB,k and vB,1, . . , vB,k be chosen as in Section 14.4; see (14.15). Define a symmetric function B: B × B → R by

$$\tilde { K } _ { B } ( x , y ) = \sum _ { j = 1 } ^ { \infty } \tilde { \gamma } _ { B , j } v _ { B , j } ( x ) v _ { B , j } ( y ) , \quad x , y \in B ,$$


<!-- p:157 -->


where

$$\tilde { \gamma } _ { B , j } \colon = \frac { \gamma _ { B , j } } { 1 + \gamma _ { B , j } } , \quad j \in \mathbb { N } .$$

Since 0 ≤ γB,j ≤ γB,j this series converges absolutely. (For x ∈ B \ B* or y ∈ B \ B* we have B(x, y) = 0.) Then B is non-negative definite; see Exercise 14.4. Given α &gt; 0 we define

$$\delta _ { B , \alpha } \colon = \prod _ { j = 1 } ^ { \infty } \frac { 1 } { ( 1 + \gamma _ { B , j } ) ^ { \alpha } } = \prod _ { j = 1 } ^ { \infty } ( 1 - \tilde { \gamma } _ { B , j } ) ^ { \alpha } .$$

For B ∈ X and m ∈ N recall from Definition 4.6 that Jη,B,m denotes the Janossy measure of order m of a point process η restricted to B.

Theorem 14.8 Let k ∈ N and set α := k/2. Let η be an α-permanental process with kernel K and let B ∈ Xrc. Then we have for each m ∈ N that

$$J _ { \eta , B , m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) = \frac { \delta _ { B , \alpha } } { m ! } \, \text {per} _ { \alpha } ( [ \tilde { K } _ { B } ] ( x _ { 1 } , \dots , x _ { m } ) ) \, \nu ^ { m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) .$$

Proof Let η(B) be a Cox process directed by the random measure ξ(B), where ξ(B)(dx) := WB(x) v(dx) and WB(x) is defined as in Lemma 14.7. In the proof of Theorem 14.6 we have shown that η(B) is α-permanental with kernel KB, where KB is the restriction of K to B* × B*. On the other hand, it follows from Definition 14.2 that η has the same property, so that Proposition 14.3 shows that ηB = η(B). Hence we can assume that ηB = η(B).

Let m ∈ N and let C ∈ Xm. By conditioning with respect to ξ(B) we obtain from (4.21) that

$$J _ { \eta , B , m } ( C ) & = \frac { 1 } { m ! } \mathbb { E } \left [ \exp \left ( - \int W _ { B } ( x ) \, \nu ( d x ) \right ) \\ & \times \int _ { B ^ { ^ { * } } } \{ ( x _ { 1 } , \dots , x _ { m } ) \in C \} W _ { B } ( x _ { 1 } ) \cdots W _ { B } ( x _ { m } ) \, \nu ^ { m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) \right ] .$$

Hence we have to show that for vn-a.e. (x1, . . , xm) ∈ (B*)n we have

$$\mathbb { E } \left [ \exp \left ( - \int _ { B } W _ { B } ( x ) \, \nu ( d x ) \right ) W _ { B } ( x _ { 1 } ) \cdots W _ { B } ( x _ { m } ) \right ] \\ = \delta _ { B , \alpha } \, \text {per} _ { \alpha } ( [ \tilde { K } _ { B } ] ( x _ { 1 } , \dots , x _ { m } ) ) .$$

Let Yi,j : √YB.j Yi,j. By Lemma 14.7 the left-hand side of (14.29) can be √2


<!-- p:158 -->


14.6 One-Dimensional Marginals of Permanental Cox Processes 147 written as

$$\mathbb { E } \left [ f ( Y ^ { \prime } ) \prod _ { i = 1 } ^ { k } \prod _ { j = 1 } ^ { \infty } \exp \left [ - ( Y ^ { \prime } _ { i , j } ) ^ { 2 } \right ] \right ] ,$$

where Y' denotes the double array (Y) and f is a well-defined function on √γB.j (R∞)k. Now let Yμ j := Yi,j. If γB,j &gt; 0, the densities φ1 and φ2 of Yi,j √2

$$\varphi _ { 2 } ( t ) = \sqrt { 1 + \gamma _ { B , j } } e ^ { - t ^ { 2 } } \varphi _ { 1 } ( t ) , \ \ t \in \mathbb { R } .$$

Therefore (14.30) equals

$$\mathbb { E } \left [ f ( Y ^ { \prime \prime } ) \prod _ { i = 1 } ^ { k } \prod _ { j = 1 } ^ { \infty } ( 1 + \gamma _ { B , j } ) ^ { - 1 / 2 } \right ] = \delta _ { B , \alpha } \, \mathbb { E } [ f ( Y ^ { \prime \prime } ) ] ,$$

where Y" := (Yj). By (14.18) we have

$$f ( Y ^ { \prime \prime } ) = \sum _ { i = 1 } ^ { k } \left ( \sum _ { j = 1 } ^ { \infty } \frac { \sqrt { \gamma _ { B , j } } } { \sqrt { 2 } } Y _ { i , j } v _ { B , j } ( x _ { 1 } ) \right ) ^ { 2 } \cdots \sum _ { i = 1 } ^ { k } \left ( \sum _ { j = 1 } ^ { \infty } \frac { \sqrt { \tilde { \gamma } _ { B , j } } } { \sqrt { 2 } } Y _ { i , j } v _ { B , j } ( x _ { m } ) \right ) ^ { 2 } ,$$

so we can apply (14.21) (with B in place of K) to obtain (14.29) and hence the assertion (14.27). □

### 14.6 One-Dimensional Marginals of Permanental Cox Processes

Let k ∈ N and let η be a (k/2)-permanental point process with kernel K. Let B ∈ Xrc. With the correct interpretation, (14.27) remains true for m = 0. Indeed, as in (14.28) we have

$$\mathbb { P } ( \eta ( B ) = 0 ) = \mathbb { E } \left [ \exp \left ( - \int W _ { B } ( x ) \, v ( d x ) \right ) \right ] = \prod _ { i = 1 } ^ { k } \prod _ { j = 1 } ^ { \infty } \mathbb { E } \left [ \exp \left ( - \frac { \gamma _ { B , j } } { 2 } Y _ { i , j } ^ { 2 } \right ) \right ] ,$$

where we have used Lemma 14.7 to obtain the second identity. Using (B.8) we obtain

$$\mathbb { P } ( \eta ( B ) = 0 ) = \prod _ { i = 1 } ^ { k } \prod _ { j = 1 } ^ { \infty } ( 1 + \gamma _ { B , j } ) ^ { - 1 / 2 } ,$$

that is

$$J _ { \eta , B , 0 } \equiv \mathbb { P } ( \eta ( B ) = 0 ) = \delta _ { B , \alpha } ,$$


<!-- p:159 -->


where α := k/2. Combining (14.27) with (4.18) yields

$$\text {where } \alpha \colon = \kappa / \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \text {} \text {.} \$$

Therefore our next result yields the probability generating function of η(B).

Proposition 14.9 Let α &gt; 0 and B ∈ Xrc. Define

$$c \coloneqq \max \{ \alpha , 1 \} \nu ( B ) \sup \{ K ( x , y ) \, \colon x , y \in B \} .$$

Then we have for s ∈ [0, c−1 ∧ 1) that

$$1 + \sum _ { m = 1 } ^ { \infty } \frac { s ^ { m } } { m ! } \int _ { B ^ { \prime \prime } } \text {per} _ { \alpha } ( [ \tilde { K } _ { B } ] ( x _ { 1 } , \dots , x _ { m } ) \nu ^ { m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) = \prod _ { j = 1 } ^ { \infty } ( 1 - s \tilde { \gamma } _ { B , j } ) ^ { - \alpha } .$$

Proof We abbreviate K := KB, γi := γB,i and vi := vB,i, i ∈ N. Let m ∈ N and x1, . . . , χm ∈ B. For r ∈ [m] the number per(r)([](x1, . . . , χm)) is given in Definition 14.2. For r = 1 we have

$$in \, \text {Definition 14.2. For } r & = 1 \, \text { we have} \\ & \int _ { B ^ { m } } \, \text {per} ^ { ( 1 ) } ( \tilde { K } ) ( x _ { 1 } , \dots , x _ { m } ) ) \, \nu ^ { m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) \\ & = \sum _ { \sigma \in \Sigma _ { m } ^ { ( 1 ) } } \int _ { B ^ { m } } \prod _ { i = 1 } ^ { m } \tilde { K } ( x _ { i } , x _ { \sigma ( i ) } ) \, \nu ^ { m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) \\ & = \sum _ { \sigma \in \Sigma _ { m } ^ { ( 1 ) } , \, \dots , \, \jmath _ { m } = 1 } \int _ { B ^ { m } } \prod _ { i = 1 } ^ { m } \tilde { \gamma } _ { j _ { i } } v _ { j _ { i } } ( x _ { i } ) v _ { j _ { i } } ( x _ { \sigma ( i ) } ) \, \nu ^ { m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) , \quad ( 1 4 . 3 5 ) \\ \text {where we have used dominated convergence in } ( 1 4 . 1 5 ) \text { to interchange sum-}$$

where we have used dominated convergence in (14.15) to interchange summation and integration. (This is possible since the convergence (14.15) is uniform and K is bounded on B2.) By the invariance of vn under permutaright-hand side of (14.35). Moreover, there are (m – 1)! permutations with exactly one cycle. Therefore (14.35) equals

$$( m - 1 ) ! \sum _ { j _ { 1 } , \dots , j _ { m } = 1 } ^ { \infty } \int _ { B ^ { m } } \prod _ { i = 1 } ^ { m } \tilde { \gamma } _ { j _ { i } } v _ { j _ { i } } ( x _ { i } ) v _ { j _ { i } } ( x _ { i + 1 } ) \, \nu ^ { m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) , \quad ( 1 4 . 3 6 )$$

where x+1 is interpreted as x1. By (14.14) and Fubini's theorem the integral in (14.36) vanishes unless j1 = · . · = jm. Therefore

$$\int _ { B ^ { " " } } \text {per} ^ { ( 1 ) } ( [ \tilde { K } ] ( x _ { 1 } , \dots , x _ { m } ) ) \, \nu ^ { m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) = ( m - 1 ) ! \sum _ { j = 1 } ^ { \infty } \tilde { \gamma } _ { j } ^ { m } .$$


<!-- p:160 -->


14.6 One-Dimensional Marginals of Permanental Cox Processes 149

Using the logarithmic series −1og(1 − x) = x + x2/2 + x3 /3 + · · , x ∈ [0, 1), and noting that γ j &lt; 1, it follows that

$$\sum _ { m = 1 } ^ { \infty } \frac { s ^ { m } } { m ! } \int _ { B ^ { m } } \text {per} ^ { ( 1 ) } ( [ \tilde { K } ] ( x _ { 1 } , \dots , x _ { m } ) ) \, \nu ^ { m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) = \sum _ { m = 1 } ^ { \infty } \frac { s ^ { m } } { m } \sum _ { j = 1 } ^ { \infty } \tilde { \gamma } _ { j } ^ { m } = D _ { s } ,$$

where

Now let r ∈ N. Then

$$D _ { s } \colon = - \sum _ { j = 1 } ^ { \infty } \log ( 1 - s \tilde { \gamma } _ { j } ) .$$

Since −log(1 − x) = xR(x), x ∈ [0, 1), with R(·) bounded on [0, 1/2], and since ∑j=1 γ j &lt; ∞, the series (14.37) converges.

$$D _ { s } ^ { r } = \sum _ { m _ { 1 } \dots , m _ { r } = 1 } ^ { \infty } \frac { s ^ { m _ { 1 } + \dots + m _ { r } } } { m _ { 1 } ! \cdots m _ { r } ! } \prod _ { j = 1 } ^ { r } \int p e r ^ { ( 1 ) } ( [ \tilde { K } ] ( x ) ) \, \nu ^ { m _ { j } } ( d x ) ,$$

where we identify v with its restriction to B. Therefore

$$\frac { D _ { s } ^ { r } } { r ! } = \sum _ { m = r } ^ { \infty } \frac { s ^ { m } } { m ! } \sum _ { m _ { 1 } , \dots , m _ { r } = m } ^ { m } \frac { m ! } { r ! m _ { 1 } ! \cdots m _ { r } ! } \prod _ { j = 1 } ^ { r } \int \text {per} ^ { ( 1 ) } ( [ \tilde { K } ] ( \mathbf x ) ) \, \nu ^ { m _ { j } } ( d \mathbf x ) .$$

We assert for all m ≥ r that

$$\text {we assert for all } m \geq F \text { all} \\ \frac { 1 } { r ! } \sum _ { \substack { m _ { 1 } \dots m _ { r } = 1 \\ m _ { 1 } + \dots + m _ { r } = m } } ^ { m } \frac { m ! } { m _ { 1 } ! \dots m _ { r } ! } \prod _ { j = 1 } ^ { r } \int \text {per} ^ { ( 1 ) } ( [ \tilde { K } ] ( x ) ) \, \nu ^ { m _ { j } } ( d x ) \\ = \int \text {per} ^ { ( r ) } ( [ \tilde { K } ] ( x ) ) \, \nu ^ { m } ( d x ) .$$

Indeed, if σ ∈ Σ has r cycles with lengths m1, . . . , mr, then

$$\int \prod _ { i = 1 } ^ { m } \tilde { K } ( x _ { i } , x _ { \sigma ( i ) } ) \, \nu ^ { m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) \\ = \prod _ { j = 1 } ^ { r } \frac { 1 } { ( m _ { j } - 1 ) ! } \int \text {per} ^ { ( 1 ) } ( [ \tilde { K } ] ( x ) ) \, \nu ^ { m _ { j } } ( d x ) . \\$$

The factor m! on the left-hand side of (14.38) is the number of ways to m1...mr create an ordered sequence of r cycles of lengths m1, . . . , m, that partition [m]. The factor 1/r! reflects the fact that any permutation of cycles leads to the same permutation of [m]. Exercise 14.5 asks the reader to give a complete proof of (14.38).


<!-- p:161 -->


By (14.38),

$$\frac { D _ { s } ^ { r } } { r ! } = \sum _ { m = r } ^ { \infty } \frac { s ^ { m } } { m ! } \int p e r ^ { ( r ) } ( [ \tilde { K } ] ( \mathbf x ) ) \, \mathcal { V } ^ { m } ( d \mathbf x ) .$$

It follows for α &gt; 0 that

$$It follows for \alpha > 0 \text { that} \\ e ^ { \alpha D _ { s } } = \sum _ { r = 0 } ^ { \infty } \frac { \alpha ^ { r } D _ { s } ^ { r } } { r ! } = 1 + \sum _ { m = 1 } ^ { \infty } \frac { s ^ { m } } { m ! } \sum _ { r = 1 } ^ { m } \int \alpha ^ { r } \, \text {per} ^ { ( r ) } ( [ \tilde { K } ] ( x ) ) \, \nu ^ { m } ( d x ) \\ = 1 + \sum _ { m = 1 } ^ { \infty } \frac { s ^ { m } } { m ! } \int \text {per} _ { \alpha } ( [ \tilde { K } ] ( x ) ) \, \nu ^ { m } ( d x ) . \\$$

Since ∫|perα([K](x))| v"(dx) ≤ m!c and sc &lt; 1, this series converges absolutely. In view of the definition (14.37) of Ds, this finishes the proof.

□

The following theorem should be compared with Example 14.4.

Theorem 14.10 Let the assumptions of Theorem 14.8 be satisfied. Then

$$\eta ( B ) \stackrel { d } { = } \sum _ { j = 1 } ^ { \infty } \zeta _ { j } ,$$

where ζj, j ∈ N, are independent, and ζj has for each j ∈ N a negative binomial distribution with parameters α and 1/(1 + γB,j).

Proof Define c by (14.34) and let s ∈ [0, c−1 ∧ 1). By (14.32) and (14.33),

$$\dot { _ { B , \alpha } } + \delta _ { B , \alpha } \sum _ { m = 1 } ^ { \infty } \frac { s ^ { m } } { m ! } \int _ { B ^ { m } } \text {per} _ { \alpha } ( [ \tilde { K } _ { B } ] ( x _ { 1 } , \dots , x _ { m } ) ) \, \nu ^ { m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) .$$

Using Proposition 14.9 and the definition (14.26) of δB,α gives

$$\mathbb { E } [ s ^ { \eta ( B ) } ] = \prod _ { j = 1 } ^ { \infty } ( 1 - \tilde { \gamma } _ { B , j } ) ^ { \alpha } ( 1 - s \tilde { \gamma } _ { B , j } ) ^ { - \alpha } = \prod _ { j = 1 } ^ { \infty } \mathbb { E } [ s ^ { \zeta _ { j } } ] , \quad ( 1 4 . 4 0 )$$

where we have used (1.24) (with p = 1−γB,j = 1/(1 +γB,j) and a = α) to get the second identity. The assertion now follows from Proposition B.5.

Equation (14.39) implies that

$$\mathbb { E } [ \eta ( B ) ] = \sum _ { j = 1 } ^ { \infty } \mathbb { E } [ \zeta _ { j } ] = \alpha \sum _ { j = 1 } ^ { \infty } \gamma _ { B , j } ,$$

where the expectation of a negative binomial random variable can be obtained from Exercise 14.2 or from (1.24). This identity is in accordance with (14.3) and (14.17). Since Σj=1 γb,j &lt; ∞ we have Σj=1 E[ζj] &lt; ∞, so that almost surely only finitely many of the ζj are not zero (even though all γB,j might be positive). Exercise 14.6 provides the variance of ζ(B).


<!-- p:162 -->


### 14.7 Exercises

Exercise 14.1 For m ∈ N and k ∈ [m] let s(m, k) be the number of permutations in Σ having exactly k cycles. (These are called the Stirling numbers of the first kind.) Show that

$$s ( m + 1 , k ) = m s ( m , k ) + s ( m , k - 1 ) , \ \ m \in \mathbb { N } , \, k \in [ m + 1 ] ,$$

where s(m, 0) := 0. Use this to prove by induction that

$$\sum _ { k = 1 } ^ { m } s ( m , k ) x ^ { k } & = x ( x + 1 ) \cdots ( x + m - 1 ) , \quad x \in \mathbb { R } . \\$$

Exercise 14.2 Let Z be a random variable having a negative binomial distribution with parameters r &gt; 0 and p ∈ (0, 1]. Show that the factorial moments of Z are given by

$$\mathbb { E } [ ( Z ) _ { m } ] = ( 1 - p ) ^ { m } p ^ { - m } r ( r + 1 ) \cdots ( r + m - 1 ) , \quad m \geq 1 .$$

Exercise 14.3 Let α &gt; 0 and let ξ be an α-permanental process. Let B1, B2 ∈ Xrc. Show that Cov[ξ(B1), ξ(B2)] ≥ 0.

Exercise 14.4 Show that B defined by (14.24) is non-negative definite.

Exercise 14.5 Give a complete argument for the identity (14.38).

Exercise 14.6 Let α := k/2 for some k ∈ N and let η be α-permanental with kernel K. Let B ∈ Xrc and show that η(B) has the finite variance

$$\mathbb { V } a r [ \eta ( B ) ] = \alpha \sum _ { j = 1 } ^ { \infty } \gamma _ { B , j } ( 1 + \gamma _ { B , j } ) ,$$

where the γB,j are as in (14.15).

Exercise 14.7 Let B ∈ Xrc and assume that there exists γ &gt; 0 such that γB,j ∈ {0, γ} for each j ∈ N, where the γB,j are as in (14.15). Let k ∈ N and let η be (k/2)-permanental with kernel K. Show that η(B) has a negative binomial distribution and identify the parameters.

Exercise 14.8 Let m ∈ N, r &gt; 0 and p ∈ (0, 1]. Let (ζ1, . . . , ζm) be a random element of N such that ζ := ζ1 + ·  · + ζ has a negative binomial distribution with parameters r and p. Moreover, assume for all l ≥ 1 that the conditional distribution of (ζ1, . . . , ζm) given ζ = l is multinomial with parameters l and q1, . . . , qm ≥ 0, where q1 + · . . + qm = 1. Show that


<!-- p:163 -->


$$\mathbb { E } [ s _ { 1 } ^ { \zeta _ { 1 } } \cdots s _ { m } ^ { \zeta _ { m } } ] = \left ( \frac { 1 } { p } - \frac { 1 - p } { p } \sum _ { j = 1 } ^ { m } s _ { j } q _ { j } \right ) ^ { - r } , \quad s _ { 1 } , \dots , s _ { m } \in [ 0 , 1 ] .$$

(Hint: At some stage one has to use the identity

$$\sum _ { n = 0 } ^ { \infty } \frac { \Gamma ( n + r ) } { \Gamma ( n + 1 ) \Gamma ( r ) } q ^ { n } = ( 1 - q ) ^ { - r } , \ \ q \in [ 0 , 1 ) ,$$

which follows from the fact that (1.22) is a probability distribution.)

Exercise 14.9 Let k ∈ N and suppose that η1, . .. , ηk are independent (1/2)-permanental processes with kernel K. Show that η1 + · · · + ηk is (k/2)- permanental. (Hint: Assume that η1, . . . , ηk are Cox processes and use the identity (13.11).)

Exercise 14.10 For each k ∈ N let ηk be a (k/2)-permanental process with kernel (2/k)K. Let B ∈ Xrc and show that ηk(B) → ζB as k → ∞, where ζB has a Poisson distribution with mean ∫β K(x, x) v(dx). (Hint: Use (14.40), Proposition B.10 and (14.17).)


<!-- p:164 -->


## Compound Poisson Processes

A compound Poisson process ξ is a purely discrete random measure that is given as an integral with respect to a Poisson process η on a product space. The coordinates of of the points of η represent the positions and weights of the atoms of ξ. Every compound Poisson process is completely independent. Of particular interest is the case where the intensity measure of ξ is of product form. The second factor is then known as the Lévy measure of ξ. The central result of this chapter asserts that every completely independent random measure without fixed atoms is the sum of a compound Poisson process and a deterministic diffuse measure. The chapter concludes with a brief discussion of linear functionals of ξ and the shot noise Cox process.

### 15.1 Definition and Basic Properties

Let (Y, Y) be a measurable space. A compound Poisson process is a random measure ξ on Y of the form

$$\xi ( B ) = \int _ { B \times ( 0 , \infty ) } r \, \eta ( d ( y , r ) ) , \quad B \in \mathcal { Y } ,$$

where η is a Poisson process on Y × (0, ∞) with s-finite intensity measure λ. We might think of a point of η as being a point in Y with the second coordinate representing its weight. Then the integral (15.1) sums the weights of the points lying in B. Proposition 12.1 implies for each B ∈ y that P(ξ(B) &lt; ∞) = 1 if and only if

$$\int _ { B \times ( 0 , \infty ) } ( r \wedge 1 ) \, \lambda ( d ( y , r ) ) < \infty ,$$

We need to check that ξ really is a random measure in the sense of Definition 13.1.

Proposition 15.1 Let η be a point process on Y × (0, ∞). Then ξ given by (15.1) is a random measure on Y.


<!-- p:165 -->


Proof First we fix ω ∈ Ω and write ξ(ω, B) to denote the dependence of the right-hand side of (15.1) on ω. The measure property of ξ(ω) := ξ(ω, ·) follows from monotone convergence. We show next that ξ(ω) is s-finite. To this end we write η(ω) = Σ=1 ηi(ω), where the η(ω) are finite measures on Y × (0, ∞). Then ξ(ω) = Σij=1 ξi, (ω), here

$$\xi _ { i , j } ( \omega ) ( B ) \colon = \int _ { B \times ( 0 , \infty ) } 1 \{ j - 1 < r \leq j \} r \, \eta _ { i } ( \omega ) ( d ( y , r ) ) , \quad B \in \mathcal { Y } .$$

Since ξi,j(ω)(Y) ≤ j ηi(ω)(Y × (0, ∞)) &lt; ∞, this shows that ξ(ω) ∈ M(Y). Finally, by Proposition 2.7, for all B ∈ y the mapping ξ(B): Ω → R+ is measurable and hence ξ: Ω → M is measurable. □

Compound Poisson processes have the following remarkable property. In the special case of point processes we have already come across this property in Chapter 3.

Definition 15.2 A random measure ξ on a measurable space (X, X) is said to be completely independent if, for all m ∈ N and pairwise disjoint B1, . . . , Bm ∈ X, the random variables ξ(B1), . . . , ξ(Bm) are stochastically independent. In this case ξ is also called a completely random measure for short.

Proposition 15.3 Let ξ be a compound Poisson process on Y. Then ξ is completely independent.

Proof Assume that ξ is given by (15.1). Then ξ = T(η), where the mapping T : N(Y × (0, ∞)) → M(Y) is given by T(μ)(B) := ∫SB×(0,∞) rμ(d(y, r)) for μ ∈ N(Y × (0, ∞)) and B ∈ Y. Proposition 15.1 shows that T is measurable. Furthermore, ξB = T(ηB×(0,∞)), so that the result follows from Theorem 5.2. □

Proposition 15.4 Let ξ be the compound Poisson process given by (15.1). Then

$$L _ { \xi } ( u ) = \exp \left [ - \int ( 1 - e ^ { - r u ( y ) } ) \, \lambda ( d ( y , r ) ) \right ] , \ \ u \in \mathbb { R } _ { + } ( \mathbb { Y } ) .$$

Proof Let u ∈ R+(Y). It follows from (15.1) and monotone convergence that

$$\exp [ - \xi ( u ) ] = \exp \left ( - \int r u ( y ) \, \eta ( d ( y , r ) ) \right ) .$$

Then the assertion follows from Theorem 3.9.

□


<!-- p:166 -->


Let ξ be given by (15.1). Then we can apply (15.3) with u = t1B for t ≥ 0 and B ∈ y. Since 1 − e−tr1B(y) = 0 for y ∉ B, we obtain

$$\mathbb { E } [ \exp [ - t \xi ( B ) ] ] = \exp \left [ - \int ( 1 - e ^ { - t r } ) \, \lambda ( B , d r ) \right ] , \quad t \geq 0 ,$$

where λ(B, ·) := λ(B × ·). If P(ξ(B) &lt; ∞) = 1 then (15.2) and Exercise 12.2 show that the distribution of ξ(B) determines λ(B, ·).

Of particular interest is the case where λ = ρ0 © v, where v is a measure on (0, ∞) satisfying

$$\int ( r \wedge 1 ) \, \nu ( d r ) < \infty$$

and ρ0 is a σ-finite measure on Y. Then (15.4) simplifies to

$$\mathbb { E } [ \exp [ - t \xi ( B ) ] ] = \exp \left [ - \rho _ { 0 } ( B ) \int ( 1 - e ^ { - t r } ) \, \nu ( d r ) \right ] , \quad t \geq 0 ,$$

where we note that (15.5) is equivalent to ∫ (1 – e−t) v(dr) &lt; ∞ for one (and then for all) t &gt; 0. In particular, ξ is ρo-symmetric; that is ξ(B) ≡ ξ(B′) whenever ρ0(B) = ρo(B′). Therefore ξ is called a ρ0-symmetric compound Poisson process with Lévy measure v. Since ε1{r ≥ ε} ≤ r ∧ 1 for all r ≥ 0 and ε ∈ (0, 1) we obtain from (15.5) that

$$\nu ( [ \varepsilon , \infty ) ) < \infty , \ \varepsilon > 0 .$$

Example 15.5 Let η′ = Σn=1 δr be a homogeneous Poisson process on R+ with intensity γ &gt; 0; see Section 7.1. Let (Zn)n≥1 be a sequence of independent R+-valued random variables with common distribution Q. Then ξ := Σn=1 Zδr is a λ+-symmetric compound Poisson process with Lévy measure γ Q. Indeed, by the marking theorem (Theorem 5.6), η := ∑n=1 δ(Tn,zn) is a Poisson process on R+ × (0, ∞) with intensity measure γ λ+ ⊗ Q. Note that

$$\xi [ 0 , t ] = \sum _ { n = 1 } ^ { \eta ^ { \prime } [ 0 , t ] } Z _ { n } , \ \ t \in \mathbb { R } _ { + } .$$

This piecewise constant random process is illustrated by Figure 15.1.

Example 15.6 Let ρ0 be a σ-finite measure on Y and let ξ be a ρ0symmetric compound Poisson process with Lévy measure

$$\nu ( d r ) \colon = r ^ { - 1 } e ^ { - b r } d r ,$$


<!-- p:167 -->


Figure 15.1 Illustration of the process ξ[0, t] from Example 15.5, jumping at the times of a homogeneous Poisson process.

ξ[0, t]

t

T1

T2

T3

T4

T5

where b &gt; 0 is a fixed parameter. Then we obtain from (15.6) and the identity

$$\int _ { 0 } ^ { 0 } ( 1 - e ^ { - u r } ) r ^ { - 1 } e ^ { - r } \, d r = \log ( 1 + u ) , \quad u \geq 0$$

(easily checked by differentiation) that

$$\mathbb { E } [ \exp ( - t \xi ( B ) ) ] = ( 1 + t / b ) ^ { - \rho _ { 0 } ( B ) } , \ \ t \geq 0 ,$$

provided that 0 &lt; ρo(B) &lt; ∞. Hence ξ(B) has a Gamma distribution (see (1.28)) with shape parameter a := ρo(B) and scale parameter b. Therefore ξ is called a Gamma random measure with shape measure ρo and scale parameter b. An interesting feature of ξ comes from the fact that ∫® r-1e-br dr = ∞, which implies that if Y is a Borel space, ρo is diffuse and B ∈ y satisfies ρ0(B) &gt; 0, then almost surely ξ{y} &gt; 0 for infinitely many y ∈ B; see Exercise 15.2.

Example 15.7 Let λ denote Lebesgue measure on [0, ∞) and consider a λ+-symmetric compound Poisson process ξ with Lévy measure v. The stochastic process Y := (Yt)t≥0 := (ξ[0, t])t≥0 is called a subordinator with Lévy measure v. This process has independent increments in the sense that Y1 , Yt2 − Yt1 , . . . , Ytn − Ytn−1 are independent whenever n ≥ 2 and 0 ≤ t1 &lt; . . . &lt; t. Moreover, the increments are homogeneous, that is, for any h &gt; 0, the distribution of Yt+h − Y, = ξ(t, t + h] does not depend on t ≥ 0. If ν is given as in Example 15.6, then Y is called a Gamma process. This process is almost surely strictly increasing and everywhere discontinuous.


<!-- p:168 -->


### 15.2 Moments of Symmetric Compound Poisson Processes

The moments of a symmetric compound Poisson process can be expressed in terms of the moments of the associated Lévy measure. Before formulating the result, we introduce for n ∈ N and k1, . . . , kn ∈ N0 the notation

$$\begin{bmatrix} n \\ k _ { 1 } , \dots , k _ { n } \end{bmatrix} \coloneqq \frac { n ! } { ( 1 ! ) ^ { k _ { 1 } } k _ { 1 } ! ( 2 ! ) ^ { k _ { 2 } } k _ { 2 } ! \cdots ( n ! ) ^ { k _ { n } } k _ { n } ! } ,$$

whenever 1k1 + 2k2 + · · · + nk = n. In all other cases this number is defined as 0. This is the number of ways to partition {1, . . . , n} into k blocks of size i for i ∈ {1, . . . , n}.

Proposition 15.8 Let v be a measure on (0, ∞) satisfying (15.5) and let ρ0 be an σ-inite measure on Y. Let ξ be a ρo-symmetric compound Poisson process with Lévy measure v. Let B ∈ Y and n ∈ N. Then

$$\mathbb { E } [ \xi ( B ) ^ { n } ] = \sum _ { k _ { 1 } , \dots , k _ { n } , \in \mathbb { N } _ { 0 } } \left [ _ { k _ { 1 } , \dots , k _ { n } } ^ { n } \right ] \rho _ { 0 } ( B ) ^ { k _ { 1 } + \dots + k _ { n } } \prod _ { i = 1 } ^ { n } \alpha _ { i } ^ { k _ { i } } ,$$

where αi := ∫ ri v(dr).

Proof The proof is similar to that of Proposition 12.6 and can in fact be derived from that result. We prefer to give a direct argument. We can assume that η is proper. First we use Fubini's theorem to obtain

$$\xi ( B ) ^ { n } = \int _ { ( B \times ( 0 , \infty ) ) ^ { n } } r _ { 1 } \cdots r _ { n } \, \eta ^ { n } ( d ( ( y _ { 1 } , r _ { 1 } ) , \dots , ( y _ { n } , r _ { n } ) ) ) .$$

Consider now a partition of [n]. Within each of the blocks the indices of the integration variables are taken to be equal, while they are taken to be distinct in different blocks. Summing over all partitions and using the symmetry property (A.17) of factorial measures, we obtain

$$\ m e t { y } \ p { \sigma } { k } ( i . k . 1 ) & \text { or } \ m o t { k } \ m e t { u } , \text { we obtain } 5 , \ m o t { b } \ m e t { u } \\ \xi ( B ) ^ { n } & = \sum _ { k _ { 1 } , \dots , k _ { n } \in N _ { 0 } } \left [ _ { k _ { 1 } , \dots , k _ { n } } ^ { n } \right ] \int _ { ( B \times \mathbb { R } _ { + } ) ^ { n + \dots + k _ { n } } } \prod _ { i = 1 , \ j = k _ { 1 } + \dots + k _ { i - 1 } + 1 } ^ { n } \prod _ { j _ { i } } ^ { k _ { 1 } + \dots + k _ { j } } r _ { j _ { i } } ^ { i } \\ & \quad \times \eta ^ { ( k _ { 1 } + \dots + k _ { n } ) } ( d ( ( y _ { 1 } , r _ { 1 } ) , \dots , ( y _ { k _ { 1 } + \dots + k _ { n } } , r _ { k _ { 1 } + \dots + k _ { n } } ) ) ) , \quad ( 1 5 . 1 3 )$$

where k0 := 0. Since the integrand in the right-hand side of (15.13) is nonnegative, taking expectations, we can use the multivariate Mecke equation (Theorem 4.4) to derive (15.12). □

Corollary 15.9 Let ρo, v and ξ be as in Proposition 15.8. Suppose that B ∈ y satisfies 0 &lt; ρ0(B) &lt; ∞ and let n ∈ N. Then E[ξ(B)n] &lt; ∞ if and only if ∫ rn v(dr) &lt; ∞.


<!-- p:169 -->


Proof Suppose that E[ξ(B)"] &lt; ∞. Observe that the summand with k = 1 (and k1 = · . · = kn−1 = 0) on the right-hand side of (15.12) equals ρ0(B)nαn. Since ρ0(B) &gt; 0 we deduce that α &lt; ∞. Conversely, suppose that α &lt; ∞. Then (15.5) implies that αi &lt; ∞ for each i ∈ [n]. Since ρ0(B) &lt; ∞ we hence obtain from (15.12) that E[ξ(B)"] &lt; ∞. □

For n = 1 we obtain from (15.12) that

$$\mathbb { E } [ \xi ( B ) ] = \rho _ { 0 } ( B ) \int ^ { \ } r \, \nu ( d r ) ,$$

which is nothing but Campbell's formula (13.1) for this random measure. In the case n = 2 we have

$$\text {In the case } h = 2 \text { we have } \\ \mathbb { E } [ \xi ( B ) ^ { 2 } ] = \rho _ { 0 } ( B ) ^ { 2 } \left ( \int r \nu ( d r ) \right ) ^ { 2 } + \rho _ { 0 } ( B ) \int r ^ { 2 } \, \nu ( d r )$$

and therefore

$$\mathbb { V } a r [ \xi ( B ) ] = \rho _ { 0 } ( B ) \int r ^ { 2 } \, \nu ( d r ) .$$

Exercises 15.4 and 15.5 give two generalisations of (15.12).

### 15.3 Poisson Representation of Completely Random Measures

The following generalises Definition 6.4.

Definition 15.10 A random measure ξ on Y is said to be uniformly σfinite if there exist Bn ∈ y, n ∈ N, such that Bn ↑ Y as n → ∞ and

$$\mathbb { P } ( \xi ( B _ { n } ) < \infty ) = 1 , \ \ n \in \mathbb { N } .$$

In this case, and if Y is a Borel space, ξ is said to be diffuse if there exists A ∈ F such that P(A) = 1 and ξ(ω, {x}) = 0 for all x ∈ X and all ω ∈ A.

The second part of Definition 15.10 is justified by Exercise 13.10. The following converse of Proposition 15.1 reveals the significance of Poisson py eo os s oo  ss   oso in the point process case, we say that two random measures ξ and ξ' on Y are almost surely equal if there is an A ∈ F with P(A) = 1 such that ξ(ω) = ξ′(ω) for each ω ∈ A.

Theorem 15.11 Suppose that (Y, Y) is a Borel space and let ξ be a uniformly σ-inite completely independent random measure on Y. Assume that

$$\xi \{ y \} = 0 , \quad \mathbb { P } \text {-a.s.} , \, y \in \mathbb { Y } .$$


<!-- p:170 -->


Then there is a Poisson process η on Y × R+ with diffuse σ-finite intensity measure, and a diffuse measure v on Y, such that almost surely

$$\xi ( B ) = \nu ( B ) + \int _ { B \times ( 0 , \infty ) } r \, \eta ( d ( y , r ) ) , \quad B \in \mathcal { Y } .$$

Proof By Exercise 13.10 (a version of Proposition 6.2 that applies to general finite measures) and the assumption that ξ is uniformly σ-finite, we can write

$$\xi = \chi + \sum _ { n = 1 } ^ { \kappa } Z _ { n } \delta _ { Y _ { n } } , \quad \mathbb { P } \text {-a.s.} , \quad ( 1 5 . 1 6 )$$

where χ is a diffuse random measure, κ is an Ñ0-valued random variable, (Y) is a sequence of random elements of Y, (Z) is a sequence of (0, ∞)- valued random variables and Σn=1 δr is a simple point process. Since ξ is uniformly σ-finite, X has the same property. Let η := Σn=1 δ(r,z). This is a all in B ∈ y. The latter identities hold almost surely; but it is no restriction of generality to assume that they hold everywhere on Ω. For each ε &gt; 0 we have

$$\varepsilon \eta ( B \times [ \varepsilon , \infty ) ) \leq \sum _ { n = 1 } ^ { \kappa } Z _ { n } 1 \{ Y _ { n } \in B \} = \xi ( B ) - \chi ( B ) .$$

Therefore η is uniformly σ-finite. We need to show that χ a.s. equals its intensity measure and that η is a Poisson process. Let C ∈ y ø B((0, ∞)) be such that P(η(C) &lt; ∞) = 1 and define the simple point process η′ := ( )    = (∞ &gt; (),  ((∞ (0) × )(at

$$\eta ^ { \prime } ( B ) = \int 1 \{ y \in B , ( y , \xi \{ y \} ) \in C \} \, \xi ( d y ) , \quad B \in \mathcal { Y } ,$$

where we have used that

$$\int \mathbf 1 \{ ( y , \xi \{ y \} ) \in C \} \chi ( d y ) \leq \int \mathbf 1 \{ \xi \{ y \} > 0 \} \chi ( d y ) = 0 .$$

In particular, η'(B) is a measurable function of ξB. Exercise 15.9 shows that ξ1, . . . , ξB are independent whenever B1, . .. , Bm ∈ y are pairwise disjoint. It follows that η' is completely independent. Moreover, since we have η′{y} = ξ{y}1{(y, ξ{y}) ∈ C} for each y ∈ Y, (15.14) implies that η′ (and also η) has a diffuse intensity measure. By Theorem 6.12, η' is a Poisson process. In particular,

$$\mathbb { P } ( \eta ( C ) = 0 ) = \mathbb { P } ( \eta ^ { \prime } = 0 ) = \exp [ - \lambda ( C ) ] ,$$


<!-- p:171 -->


where λ is the intensity measure of η and where we have used the identity η(C) = η'(Y). Theorem 6.10 yields that η is a Poisson process. The decomposition (15.16) shows for any B ∈ Y that χ(B) depends only on the restriction ξ. Therefore χ is completely independent, so that Proposition 15.12 (to be proved below) shows that χ almost surely equals its intensity measure. □

The proof of Theorem 15.11 has used the following result.

Proposition 15.12 Let ξ be a diffuse, uniformly σ-finite random measure on a Borel space (Y, Y). If ξ is completely independent, then there is a diffuse σ-inite measure v on Y such that ξ and v are almost surely equal.

Proof Given B ∈ Y, define

$$\nu ( B ) \colon = - \log \mathbb { E } [ \exp [ - \xi ( B ) ] ] ,$$

s tns    o  =:  t- o  Sihn function ν is finitely additive. Moreover, if C ↑ C with C, C ∈ Y, then monotone and dominated convergence show that v(C) ↑ v(C). Hence v is a measure. Since ξ is diffuse, v is diffuse. Moreover, since ξ is uniformly σ-finite, v is σ-finite. Let η be a Cox process directed by ξ and let η' be a Poisson process with intensity measure v. By Proposition 6.9, η' is simple. Since ξ is diffuse, we can take A ∈ F as in Definition 15.10 to obtain from (13.10) that

$$\mathbb { E } [ \eta ^ { ( 2 ) } ( D _ { \mathbb { Y } } ) ] = \mathbb { E } [ \xi ^ { 2 } ( D _ { \mathbb { Y } } ) ] = \mathbb { E } [ 1 _ { A } \xi ^ { 2 } ( D _ { \mathbb { Y } } ) ] = 0 ,$$

where DY := {(x, y) ∈ Y2 : x = y}. Hence Proposition 6.7 shows that η is simple as well. Furthermore,

$$\mathbb { P } ( \eta ( B ) = 0 ) = \mathbb { E } [ \exp [ - \xi ( B ) ] ] = \exp [ - \nu ( B ) ] = \mathbb { P } ( \eta ^ { \prime } ( B ) = 0 ) , \quad B \in \mathcal { Y } .$$

By Theorem 6.10, η = η', so that Theorem 13.7 yields ξ ≡ v. Now let H be a countable π-system generating Y. Then A := {ξ(B) = v(B) for all B ∈ H} has full probability. As it is no restriction of generality to assume that the sets B from Definition 15.10 are in H, we can apply Theorem A.5 to conclude that ξ = γ on A. □

If ξ is a random measure on a Borel space (Y, Y) and y ∈ Y is such that

$$\mathbb { P } ( \xi \{ y \} > 0 ) > 0 ,$$

then y is called a fixed atom of ξ. Theorem 15.11 does not apply to a completely independent random measure ξ with fixed atoms. Exercise 15.8


<!-- p:172 -->


shows, however, that any such ξ is the independent superposition of a random measure with countably many fixed atoms and a completely independent random measure satisfying (15.14).

### 15.4 Compound Poisson Integrals

Let ξ be a compound Poisson process on a measurable space (Y, Y) as defined by (15.1). For f ∈ R(Y) we may then try to form the integral ∫ f dξ. Expressing this as

$$\int f ( z ) \, \xi ( d z ) = \int r f ( y ) \, \eta ( d ( y , r ) ) ,$$

we can apply Proposition 12.1 (or Campbell's formula) to see that the integral converges almost surely if ∫ r| f(z)| λ(d(r, z)) &lt; ∞. For applications it is useful to make f dependent on a parameter x ∈ X, where (X, X) is another measurable space. To do so, we take a measurable function k ∈ R(X × Y) (known as a kernel) and define a random field (Y(x))x∈x by

$$Y ( x ) \coloneqq \int r k ( x , y ) \, \eta ( d ( y , r ) ) , \quad x \in \mathbb { X } .$$

Here we can drop the assumption that the weights be positive and assume that η is a Poisson process on Y × R such that

$$\int | r k ( x , y ) | \, \lambda ( d ( y , r ) ) < \infty , \quad x \in \mathbb { X } ,$$

where λ is the intensity measure of η. Then for each x ∈ X the right-hand side of (15.18) is almost surely finite and we make the convention Y(x) := 0 whenever it is not. Using the monotone class theorem it can be shown that the random field is measurable; see Example 13.3. By Campbell's formula (Proposition 2.7),

$$\mathbb { E } [ Y ( x ) ] = \int r k ( x , y ) \, \lambda ( d ( y , r ) ) , \quad x \in \mathbb { X } .$$

Proposition 15.13 Let (Y(x))x∈x be the random field given by (15.18). Assume that (15.19) holds and that

$$\int r ^ { 2 } k ( x , y ) ^ { 2 } \, \lambda ( d ( y , r ) ) < \infty , \quad x \in \mathbb { X } .$$

Then

$$\mathbb { C } o v [ Y ( x ) , Y ( z ) ] = \int r ^ { 2 } k ( x , y ) k ( z , y ) \, \lambda ( d ( y , r ) ) , \quad x , z \in \mathbb { X } .$$


<!-- p:173 -->


Proof The random variable Y(x) -E[Y(x)] takes the form of a Wiener-Itô integral; see (12.4). Hence the result follows from Lemma 12.2. □

Example 15.14 Let d ∈ N. Consider the random field (Y(x))xeR given by (15.18) in the case X = Y = Rd with a kernel of the form k(x, y) = (x − y) for some k ∈ L1(λa). Assume also that the intensity measure λ of η is the product λd ⊗ v for some measure v on R satisfying ∫ |r| v(dr) &lt; ∞. Then

$$Y ( x ) = \int r \tilde { k } ( x - y ) \, \eta ( d ( y , r ) ) ,$$

and (15.20) shows that

$$\mathbb { E } [ Y ( x ) ] = \iint r \tilde { k } ( x - y ) \, d y \, \nu ( d r ) .$$

The random field (Y(x))x∈Rd is known as a Poisson driven shot noise, while (Y(x) − E[Y(x)])x∈Rd is known as a Poisson driven moving average field. A specific example is

$$\tilde { k } ( x ) = \mathbf 1 \{ x _ { 1 } \geq 0 , \dots , x _ { d } \geq 0 \} \exp [ - \langle v , x \rangle ] ,$$

where v ∈ Rd is a fixed parameter.

Example 15.15 Let λ be a σ-finite measure on Y × (0, ∞) and let η be a Poisson process with intensity measure λ. Let the random field (Y(x))x∈x be given by (15.18), where the kernel k is assumed to be non-negative. Let ρ be a σ-finite measure on X such that

$$( 1 5 . 2 3 )$$

is a σ-finite measure on X. Then (15.19) holds for ρ-a.e. x ∈ X. A Cox process χ driven by the random measure Y(x)ρ(dx) is called a shot noise Cox process. It has the intensity measure (15.23).

Proposition 15.16 Let χ be a shot noise Cox process as in Example 15.15. The Laplace functional of χ is given by

$$L _ { \chi } ( u ) = \exp \left [ - \int ( 1 - e ^ { - r u ^ { * } ( y ) } ) \, \lambda ( d ( y , r ) ) \right ] , \quad u \in \mathbb { R } _ { + } ( \mathbb { X } ) ,$$

where u*(y) := ∫ (1 − e−u(x))k(x, y) ρ(dx), y ∈ Y.

Proof By (13.11) and Fubini's theorem, we have for every u ∈ R+(X) that

$$R _ { \ } l o b { j } & = \mathbb { B } y \left ( 1 5 . 1 \right ) \text { and } \L a m b { 3 } \text { one} \text {c} \L a m b { 3 } \L a m b { ( a \L a m b { + } \L a m b { ( a \L a m b { + } \L a m b { ( a \L a m b { + } \L a m b { ( a \L a m b { + } \L a m b { ( a \L a m b { + } \L a m b { ( a \L a m b { + } \L a m b { ( a \L a m b { + } \L a m b { ( a \L a m b { + } \L a m b { ( a \L a m b { + } \L a m b { ( a \L a m b { + } \L a m b { ( a \L a m b { + } \L a m b { ( a \L a m b { + } \L a m b { ( a \L a m b { + } \L a m b { ( a \L a m b { + } \L a m b { ( a \L a m b { + } \L a m b { ( a \L a m b { + } \L a m b { ( a \L a m b { + } \L a m b { ( a \L a m b { + } \L a m b { ( a \L a m b { + } \L a m b { ( a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \L a m b { (a \L a m b { + } \$$

Theorem 3.9 yields the assertion.


<!-- p:174 -->


Example 15.17 Let χ be a shot noise Cox process as in Example 15.15 and assume that λ(d(y, r)) = r−1e−brρ0(dy)dr as in Example 15.6. Proposition 15.16 and (15.10) yield

$$L _ { \chi } ( u ) = \exp \left [ - \int \log \left ( 1 + \frac { u ^ { * } ( y ) } { b } \right ) \rho _ { 0 } ( d y ) \right ] .$$

### 15.5 Exercises

Exercise 15.1 Let n ≥ 2 and let

$$\Delta _ { n } \colon = \{ ( p _ { 1 } , \dots , p _ { n } ) \in [ 0 , 1 ] ^ { n } \, \colon p _ { 1 } + \cdots + p _ { n } = 1 \}$$

denote the simplex of all n-dimensional probability vectors. Lebesgue measure on ∆ is given by the formula

$$\mu _ { n } ( C ) \coloneqq \int _ { [ 0 , 1 ] ^ { n } } \mathbf 1 \{ ( x _ { 1 } , \dots , x _ { n - 1 } , 1 - x _ { 1 } - \dots - x _ { n - 1 } ) \in C \} \, \lambda _ { n - 1 } ( d ( x _ { 1 } , \dots , x _ { n - 1 } ) )$$

for C ∈ B(∆). This is the Hausdorff measure Hn-1 (introduced in Section A.3) restricted to the set ∆. The Dirichlet distribution with parameters α1, . . . , αn ∈ (0, ∞) is the distribution on ∆ with density

$$\frac { \Gamma ( \alpha _ { 1 } + \cdots + \alpha _ { n } ) } { \Gamma ( \alpha _ { 1 } ) \cdots \Gamma ( \alpha _ { n } ) } x _ { 1 } ^ { \alpha _ { 1 } - 1 } \cdots y$$

with respect to μn.

Let ξ be a Gamma random measure as in Example 15.6 and assume that the shape measure satisfies 0 &lt; ρo(Y) &lt; ∞. Then the random measure ζ := ξ(·)/ξ(Y) can be considered as a random probability measure. Let B1, . . . , B be a measurable partition of Y such that ρ0(Bi) &gt; 0 for all i ∈ {1, . . . , n}. Show that (ζ(B1), . . . , ζ(B)) has a Dirichlet distribution with parameters ρ0(B1), . . . , ρ0(B) and is independent of ξ(Y). (Hint: Use Example 15.6 to express the expectation of a function of (ζ(B1), . . . , ζ(B), ξ(Y)) as a Lebesgue integral on Rn+1 and change variables in an appropriate way.)

Exercise 15.2 Let η be a Poisson process on a Borel space (X, X) with intensity measure ∞ · v, where v is a finite diffuse measure on X. Let B ∈ X with v(B) &gt; 0. Show that almost surely there exist infinitely many x ∈ B with η{x} &gt; 0. (Hint: Use Proposition 6.9.)

Exercise 15.3 Let ξ be a compound Poisson process as in Proposition


<!-- p:175 -->


15.8 and let B ∈ y. Show that

$$1 5 . 8 \, \text {and let} \, B \in \mathcal { Y } . \, \text {Show that} \\ \mathbb { E } [ \xi ( B ) ^ { 3 } ] = \rho _ { 0 } ( B ) ^ { 3 } \left ( \int r \, \nu ( d r ) \right ) ^ { 3 } + 3 \rho _ { 0 } ( B ) ^ { 2 } \left ( \int r \, \nu ( d r ) \right ) \left ( \int r ^ { 2 } \, \nu ( d r ) \right ) \\ + \rho _ { 0 } ( B ) \int r ^ { 3 } \, \nu ( d r ) .$$

Exercise 15.4 Let ξ be a compound Poisson process as in Proposition 15.8. Let n ∈ N and f ∈ R+(Y). Show that

$$\mathbb { E } [ \xi ( f ) ^ { n } ] = \sum _ { r _ { 1 } , \dots , r _ { n } \in \mathbb { N } _ { 0 } } \left [ \sum _ { r _ { 1 } , \dots , r _ { n } } ^ { n } \right ] \rho _ { 0 } ( B ) ^ { r _ { 1 } + \dots + r _ { n } } \prod _ { i = 1 } ^ { n } \left ( \int f ^ { i } \, d \rho _ { 0 } \right ) ^ { r _ { i } } ( \int r ^ { i } \, \nu ( d r ) ) ^ { r _ { i } } .$$

(Hint: Generalise (15.13). You may assume that η is proper.)

Exercise 15.5 Let η be a Poisson process on Y ×R with intensity measure λ = ρ0 ⊗ ν, where ρ0 is σ-finite and ν is a measure on R with v{0} = 0, and

$$\int ( | r | \wedge 1 ) \nu ( d r ) < \infty .$$

Let B ∈ y satisfy ρ0(B) &lt; ∞. Show that (15.1) converges almost surely. Take n ∈ N and prove that E[ξ(B)"] &lt; ∞ if and only if ∫ |r|n v(dr) &lt; ∞ and, moreover, that (15.12) remains true in this case.

Exercise 15.6 Let p ∈ (0, 1). Show that the measure v on (0, ∞) defined by v(dr) := r−1-Pdr satisfies (15.5). Let ξ be a ρ0-symmetric compound Poisson process on Y with Lévy measure v for some σ-finite measure ρo on Y. Show for all B ∈  that

$$\mathbb { E } [ \exp [ - t \xi ( B ) ] ] = \exp \left [ - \ p ^ { - 1 } \Gamma ( 1 - p ) \rho _ { 0 } ( B ) t ^ { p } \right ] , \quad t \geq 0 .$$

Exercise 15.7 (Self-similar random measure) Let ξ be as in Exercise 15.6 and assume in addition that Y = Rd for some d ∈ N and that ρ0 is Lebesgue measure. Show that ξ is self-similar in the sense that ξc = ξ for any c &gt; 0, where ξc(B) := c−d/pξ(cB), B ∈ Bd. (Hint: Use Exercise 15.6.)

Exercise 15.8 Let ξ be a uniformly σ-finite random measure on a Borel space Y. Show that the set B ⊂ Y of fixed atoms of ξ is at most countable. Assume in addition that ξ is completely independent. Show that there are independent random variables Zx, x ∈ B, and a completely independent random measure ξo without fixed atoms such that

$$\xi = \xi _ { 0 } + \sum _ { x \in B } Z _ { x } \delta _ { Z _ { x } } , \quad \mathbb { P } \text {-a.s.}$$


<!-- p:176 -->


Exercise 15.9 Let ξ be a completely independent random measure on (Y, ) and let B1, . . . , B ∈  be pairwise disjoint. Show that ξB1 . . , ξB are independent random measures. (Hint: Reduce first to the case m = 2. Then use the monotone class theorem; see the proof of Proposition 8.12.)

Exercise 15.10 Let the random field (Y(x))x∈Rd be as in Example 15.14. Show that this field is stationary, that is, for any m ∈ N and x1, . . . , Xm ∈ Rd, the distribution of (Y(x1 + x), . . . , Y(xm + x)) does not depend on x ∈ Rd.

Exercise 15.11 Let χ be a shot noise Cox process as in Example 15.15 and assume moreover that

$$\iint \mathbf 1 \{ x \in \cdot \} r ^ { 2 } k ( x , y ) ^ { 2 } \, \lambda ( d ( y , r ) ) \rho ( d x )$$

is a σ-finite measure on X. Show that the second factorial moment measure α2 of χ is given by α2(d(x1, x2)) = g2(x1, x2) ρ2(d(x1, x2)), where

$$g _ { 2 } ( x _ { 1 } , x _ { 2 } ) \colon = & \int r ^ { 2 } k ( x _ { 1 } , y ) k ( x _ { 2 } , y ) \, \lambda ( d ( y , r ) ) \\ & + \left ( \int r k ( x _ { 1 } , y ) \, \lambda ( d ( y , r ) ) \right ) \left ( \int r k ( x _ { 2 } , y ) \, \lambda ( d ( y , r ) ) \right ) . \\ \intertext { C o n r a g h s c r { I } w i t h e c a s m = 2 o f T h e o r e m }$$

Compare this with the case m = 2 of Theorem 14.6. (Hint: Use Proposition 15.13.)

Exercise 15.12 Let χ be a shot noise Cox process as in Example 15.15 and assume that Y is at most countable. Show that χ is a countable superposition of independent mixed Poisson processes; see Exercise 13.4.

Exercise 15.13 A random measure ξ is said to be infinitely divisible if for every integer m ∈ N there are independent random measures ξ1, . . . , ξm with equal distribution such that ξ = ξ1 + · . · + ξm. Show that every compound Poisson process has this property.

Exercise 15.14 Suppose that χ is a shot noise Cox process. Show that χ is an infinitely divisible point process, meaning that for each m ∈ N there are independent identically distributed point processes X1, . . . ,Xm such that χ = X1 + · · · + Xm·

Exercise 15.15 Let χ be a Poisson cluster process as in Exercise 5.6. Show that χ is infinitely divisible.


<!-- p:177 -->


## The Boolean Model and the Gilbert Graph

The spherical Boolean model Z is a union of balls, where the centres form a stationary Poisson process η on Rd and the radii are obtained from an dn  n   ang      cc compact set C ⊂ Ra the probability that Z intersects C. It can be expressed explicitly in terms of the intensity of η and the radius distribution, and yields formulae for contact distributions of Z. The associated Gilbert graph has vertex set η with an edge between two vertices whenever the associated balls overlap. The point process of components isomorphic to a given finite connected graph is stationary, with an intensity that can, in principle, be computed as an integral with respect to a suitable power of the radius distribution.

### 16.1 Capacity Functional

Let d ∈ N and let η be a stationary Poisson process on Rd with strictly positive intensity γ. By Corollary 6.5 there exists a sequence X1, X2, . .. of random vectors in Ra such that almost surely

$$\eta = \sum _ { n = 1 } ^ { \infty } \delta _ { X _ { n } } . \\$$

Suppose further that (R)≥1 is a sequence of independent and identically distributed R+-valued random variables, independent of η. As in (10.11), for x ∈ Rd and r ≥ 0 set B(x, r) := {y ∈ Rd : |y − x|| ≤ r}, where ∥ · ∥ is the Euclidean norm on Rd. The union

$$Z \coloneqq \bigcup _ { n = 1 } ^ { \infty } B ( X _ { n } , R _ { n } ) & & ( 1 6 . 2 ) \\$$

of the closed balls with centres X and radii R ≥ 0 is a (random) subset of Rd. The balls B(X, R) are called grains. This is an important model of stochastic geometry:


<!-- p:178 -->


Definition 16.1 Let Q be a probability measure on R+ and let

$$\xi = \sum _ { n = 1 } ^ { \infty } \delta _ { ( X _ { n } , R _ { n } ) } & & ( 1 6 . 3 )$$

be an independent Q-marking of η. The random set (16.2) is called a (Poisson) spherical Boolean model with intensity γ and radius distribution Q.

The Boolean model is illustrated by Figure 16.1 It is helpful to note that by the marking theorem (Theorem 5.6) the point process ξ defined by (16.3) is a Poisson process with intensity measure γλa ⊗ Q.

Figure 16.1 Boolean model (left) and Gilbert graph (right), based on the same system of spheres.

Formally, a Boolean model Z is the mapping ω → Z(ω) from Ω into the space of all subsets of Rd. We shall prove the measurability statement

$$\{ Z \cap C = \emptyset \} \colon = \{ \omega \in \Omega \, \colon Z ( \omega ) \cap C = \emptyset \} \in \mathcal { F } , \quad C \in C ^ { d } ,$$

where Ca denotes the system of all compact subsets of Rd. The mapping C ↔ P(Z ∩ C = Ø) is known as the capacity functional of Z. It determines the intensity and the radius distribution of the Boolean model; we shall prove this in a more general setting in Chapter 17.

The Minkowski sum K ⊕ L of sets K, L ⊂ Rd is given by

$$K \oplus L \colon = \{ x + y \, \colon x \in K , y \in L \} .$$

The Minkowski sum of K and the ball B(0, r) centred at the origin with radius r is called the parallel set of K at distance r. If K ⊂ Rd is closed, then

$$K \oplus B ( 0 , r ) = \{ x \in \mathbb { R } ^ { d } \, \colon d ( x , K ) \leq r \} = \{ x \in \mathbb { R } ^ { d } \, \colon B ( x , r ) \cap K \neq \emptyset \} ,$$


<!-- p:179 -->


where

$$d ( x , K ) \coloneqq \inf \{ \| y - x \| \, \colon y \in K \}$$

is the Euclidean distance of x ∈ Rd from a set K ⊂ Rd and inf ∅ := ∞. We now give a formula for the capacity functional of Z.

Theorem 16.2 Let Z be a Boolean model with intensity γ and radius distribution Q. Then (16.4) holds and moreover

$$\mathbb { P } ( Z \cap C = \emptyset ) = \exp \left [ - \gamma \int \lambda _ { d } ( C \oplus B ( 0 , r ) ) \, \mathbb { Q } ( d r ) \right ] , \quad C \in C ^ { d } . \quad ( 1 6 . 8 )$$

Proof Let C ∈ Cad. We may assume that C ≠ 0. In view of the Lipschitz property in Exercise 2.8, the mapping (x, r) → d(x, C) − r is continuous. Together with (16.6) this implies that the set

$$A \coloneqq \{ ( x , r ) \in \mathbb { R } ^ { d } \times \mathbb { R } _ { + } \colon B ( x , r ) \cap C \neq \emptyset \}$$

is closed. With ξ given by (16.3) we have

$$\{ Z \cap C = \emptyset \} = \{ \xi ( A ) = 0 \} ,$$

and hence (16.4). Since ξ is Poisson with intensity measure γλa ⊗ Q, we have that

$$\mathbb { P } ( Z \cap C = \emptyset ) = \exp [ - \gamma ( \lambda _ { d } \otimes \mathbb { Q } ) ( A ) ] .$$

Using (16.6) we obtain

$$\text {ing (16.6)} & \text { we obtain} \\ & ( \lambda _ { d } \otimes \mathbb { Q } ) ( A ) = \iint 1 \{ B ( x , r ) \cap C \neq \emptyset \} \, d x \, \mathbb { Q } ( d r ) \\ & = \int \lambda _ { d } ( C \oplus B ( 0 , r ) ) \, \mathbb { Q } ( d r ) , \quad ( 1 6 . 1 1 )$$

and hence (16.8).

□

### 16.2 Volume Fraction and Covering Property

Let Z be a Boolean model with fixed intensity γ and radius distribution Q. Let R0 be a random variable with distribution Q. By (16.8),

$$\mathbb { P } ( Z \cap C \neq \emptyset ) = 1 - \exp ( - \gamma \, \mathbb { E } [ \lambda _ { d } ( C \oplus B ( 0 , R _ { 0 } ) ) ] ) , \quad C \in C ^ { d } .$$

Taking C = {x} we obtain

$$\mathbb { P } ( x \in Z ) = 1 - \exp \left ( - \gamma \kappa _ { d } \mathbb { E } [ R _ { 0 } ^ { d } ] \right ) , \quad x \in \mathbb { R } ^ { d } , \quad ( 1 6 . 1 3 )$$

where κd := λd(B(0, 1)) is the volume of the unit ball in Rd. Because of the next result, the number p := P(0 ∈ Z) is called the volume fraction of Z.


<!-- p:180 -->


Proposition 16.3 The mapping (ω, x) → 1z(ω)(x) is measurable and

$$\mathbb { E } [ \lambda _ { d } ( Z \cap B ) ] = p \lambda _ { d } ( B ) , \quad B \in \mathcal { B } ( \mathbb { R } ^ { d } ) .$$

Proof The asserted measurability follows from the identity

$$1 - \mathbf 1 _ { Z ( \omega ) } ( x ) = \prod _ { n = 1 } ^ { \infty } \mathbf 1 \{ \| x - X _ { n } ( \omega ) \| > R _ { n } ( \omega ) \} , \quad ( \omega , x ) \in \Omega \times \mathbb { R } ^ { d } .$$

Take B ∈ B(Rd). By (16.13) and Fubini's theorem,

$$\mathbb { E } [ \lambda _ { d } ( Z \cap B ) ] = \mathbb { E } \left [ \int 1 _ { Z } ( x ) 1 _ { B } ( x ) \, d x \right ] = \int _ { B } \mathbb { E } [ 1 \{ x \in Z \} ] \, d x = p \lambda _ { d } ( B ) ,$$

as asserted.

□

The next result gives a necessary and sufficient condition for Z to cover all of Rd. For A′ ⊂ Ω we write P(A') = 1 if there exists A ∈ F with A ⊂ A' and P(A) = 1. This is in accordance with our terminology on the almost sure equality of point processes and random measures.

Theorem 16.4 We have P(Z = Rd) = 1 if and only if E[Rd] = ∞.

Proof Assume that A ∈ F satisfies A ⊂ {Z = Rd} and P(A) = 1. Then P(0 ∈ Z) = 1 so that (16.13) implies E[Rd] = ∞.

Assume, conversely, that E[Rd] = ∞. As a preliminary result we first show for any n ∈ N that

$$\lambda _ { d } \otimes \mathbb { Q } ( \{ ( x , r ) \in \mathbb { R } ^ { d } \times \mathbb { R } _ { + } \colon B ( 0 , n ) \subset B ( x , r ) \} ) = \infty .$$

Since B(0, n) ⊂ B(x, r) if and only if r ≥ ∥x|| + n, the left-hand side of (16.15) equals

$$= \kappa _ { d } \int _ { [ n , \infty ) } ( r - n ) ^ { d } \, \mathbb { O } ( d r ) .$$

This is bounded below by

$$\kappa _ { d } \int _ { [ 2 n , \infty ) } \left ( \frac { r } { 2 } \right ) ^ { d } \mathbb { Q } ( d r ) = \kappa _ { d } 2 ^ { - d } \, \mathbb { E } [ 1 \{ R _ { 0 } \geq 2 n \} R _ { 0 } ^ { d } ] ,$$

proving (16.15). Since ξ is a Poisson process with intensity γλa ⊗ Q, the ball B(0, n) is almost surely covered even by infinitely many of the balls B(x, r), (x, r) ∈ ξ. Since n is arbitrary, it follows that P(Z = Rd) = 1. □


<!-- p:181 -->


### 16.3 Contact Distribution Functions

This section is concerned with the random variables given by the distance from the origin 0 to the Boolean model Z, and the distance from 0 to Z in a specified direction. We assume throughout that

$$\mathbb { E } [ R _ { 0 } ^ { d } ] < \infty .$$

By Exercise 16.1 it is no restriction of generality to assume that Z(ω) is closed for each ω ∈ Ω. Define

$$X _ { \circ } \colon = \inf \{ r \geq 0 \, \colon Z \cap B ( 0 , r ) \neq \emptyset \} = d ( 0 , Z ) .$$

Since Z is closed and closed balls are compact we have

$$\{ X _ { \circ } \leq t \} = \{ Z \cap B ( 0 , t ) \neq \emptyset \} , \ \ t \geq 0 ,$$

and by (16.4), X。 is a random variable. Since P(X。 = 0) = P(0 ∈ Z) = p, the distribution of X。 has an atom at 0. Therefore it is convenient to consider the conditional distribution of X。 given that the origin is not covered by Z. The function

$$H _ { \circ } ( t ) \colon = \mathbb { P } ( X _ { \circ } \leq t \, | \, 0 \notin Z ) , \quad t \geq 0 ,$$

is called the spherical contact distribution function of Z.

Proposition 16.5 The spherical contact distribution function of Z is given by

$$H _ { \circ } ( t ) = 1 - \exp \left ( - \gamma \kappa _ { d } \sum _ { j = 1 } ^ { d } \binom { d } { j } t ^ { j } \mathbb { E } [ R _ { 0 } ^ { d - j } ] \right ) , \quad t \geq 0 .$$

Proof Take t ≥ 0. Then, by (16.16) and (16.12),

$$\mathbb { P } ( X _ { \mathbf o } > t ) & = \mathbb { P } ( Z \cap B ( 0 , t ) = \emptyset ) = \exp \left ( - \gamma \, \mathbb { E } [ \lambda _ { d } ( B ( 0 , R _ { 0 } + t ) ) ] \right ) \\ & = \exp \left ( - \gamma \kappa _ { d } \, \mathbb { E } [ ( R _ { 0 } + t ) ^ { d } ] \right ) .$$

Since

$$1 - H _ { \circ } ( t ) = \mathbb { P } ( X _ { \circ } > 0 ) ^ { - 1 } \mathbb { P } ( X _ { \circ } > t ) ,$$

we can use the binomial formula to derive the result.

□

For x, y ∈ Rd let [x, y] := {x + s(y − x) : 0 ≤ s ≤ 1} denote the line segment between x and y. Let u ∈ Rd with ∥u| = 1 and let

$$X _ { [ u ] } \colon = \inf \{ r \geq 0 \ ; Z \cap [ 0 , r u ] \neq \emptyset \}$$


<!-- p:182 -->


denote the linear distance of the origin from Z in direction u. The function

$$H _ { [ u ] } ( t ) \colon = \mathbb { P } ( X _ { [ u ] } \leq t \, | \, 0 \notin Z ) , \ \ t \geq 0 ,$$

is called the linear contact distribution function of Z in direction u. The next result shows that if P(R0 = 0) &lt; 1 then H[u] is the distribution function o s dt mn  n o  a ton direction u. We set κ0 := 1.

Proposition 16.6 Let u ∈ Rd with ∥u|| = 1. The linear contact distribution function of Z in direction u is given by

$$H _ { [ u ] } ( t ) = 1 - \exp \left ( - \gamma t \kappa _ { d - 1 } \, \mathbb { E } [ R _ { 0 } ^ { d - 1 } ] \right ) , \ \ t \geq 0 .$$

Proof Let t ≥ 0. As at (16.16) it follows that

$$\{ X _ { [ u ] } \leq t \} = \{ Z \cap [ 0 , t u ] \neq \emptyset \} .$$

Hence (16.12) implies

$$\mathbb { P } ( X _ { [ u ] } > t ) = \exp \left ( - \gamma \, \mathbb { E } [ \lambda _ { d } ( B ( 0 , R _ { 0 } ) \oplus [ 0 , t u ] ) ] \right ) .$$

It is a well-known geometric fact (elementary in the cases d = 1, 2, 3) that

$$\lambda _ { d } ( B ( 0 , R _ { 0 } ) \oplus [ 0 , t u ] ) = \lambda _ { d } ( B ( 0 , R _ { 0 } ) ) + t \kappa _ { d - 1 } R _ { 0 } ^ { d - 1 } .$$

Since

$$1 - H _ { [ u ] } ( t ) = ( 1 - p ) ^ { - 1 } \mathbb { P } ( X _ { [ u ] } > t ) ,$$

the result follows from (16.13).

□

### 16.4 The Gilbert Graph

We need to introduce some graph terminology. An (undirected) graph is a pair G = (V, E), where V is a set of vertices and E ⊂ {{x, y} : x, y ∈ V, x ≠ y} is the set of edges. The number card V is known as the order of G. An edge {x, y} ∈ E is thought of as connecting its endpoints x and y. Two distinct points x, y ∈ V are said to be connected if there exist m ∈ N and x0, . . . , xm ∈ V such that x0 = x, xm = y and {xi−1, xi} ∈ E for all i ∈ [m]. The graph G itself is said to be connected if any two of its vertices are connected. Two graphs G = (V, E) and G′ = (V', E') are said to be isomorphic if there is a bijection T : V → V' such that {x, y} ∈ E if and only if {T(x), T(y)} ∈ E' for all x, y ∈ V with x ≠ y. In this case we write G ≈ G′.

The remainder of this chapter is concerned with the Gilbert graph, a close relative of the spherical Boolean model. We continue to work with the Poisson processes η from (16.1) and the point process ξ given by (16.3), that is


<!-- p:183 -->


$$\eta = \sum _ { n = 1 } ^ { \infty } \delta _ { X _ { n } } , \quad \xi = \sum _ { n = 1 } ^ { \infty } \delta ( X _ { n } , R _ { n } ) , \quad ( 1 6 . 2 1 )$$

where (R)≥1 is a sequence of independent R+-valued random variables with common distribution Q. Suppose that two points Xm, Xn ∈ η, m ≠ n, are connected by an edge whenever the associated balls overlap, that is, B(X, R) ∩ B(X, R) ≠ 0. This yields an undirected (random) graph with vertex set η; see Figure 16.1

For a formal definition of the Gilbert graph we introduce the space R[2d] of all sets e ⊂ Rd containing exactly two elements. Any e ∈ R[2d] is a potential edge of the graph. When equipped with a suitable metric, R[2d] becomes a separable metric space; see Exercise 17.5.

Definition 16.7 Let ξ be an independent marking of a stationary Poisson process on Rd as in (16.21). Define the point process χ on R[2d] by

$$\chi \colon = \int 1 \{ \{ x , y \} \in \cdot , x < y \} 1 \{ B ( x , r ) \cap B ( y , s ) \neq \emptyset \} \xi ^ { 2 } ( d ( ( x , r ) , ( y , s ) ) ) ,$$

where x &lt; y means that x is lexicographically strictly smaller than y. Then we call the pair (η,χ) the Gilbert graph (based on η) with radius distribution Q. In the special case where Q is concentrated on a single positive value (all balls have a fixed radius), it is also known as the random geometric graph.

Given distinct points x1, . . . , xk ∈ η we let G(x1, . . . , xk,χ) denote the graph with vertex set {x1, . . . , xk} and edges induced by χ, that is such that {xi, x j} is an edge if and only if {xi, x j} ∈ χ. This graph is called a component (of the Gilbert graph) if it is connected and none of the x is connected to a point in η − δx, − . . . − δxk. Let G be a connected graph with k ≥ 2 vertices. The point process ηG of all components isomorphic to G is then defined by

$$\eta _ { G } \colon = \int \mathbf 1 \{ x _ { 1 } \in \cdot , x _ { 1 } < \cdots < x _ { k } \}$$

× 1{G(x1, . . . , xk, χ) is a component isomorphic to G} ηk(d(x1, . , xk)).

Hence a component isomorphic to G contributes to ηg(C) if its lexicographic minimum lies in C. The indicator 1{x1 &lt; . .. &lt; xk} ensures that each component is counted only once. Given distinct x1, . . . , xk ∈ Rd and given r1, . . . , rk ∈ R+ we define a graph Γk(x1, r1, . . . , xk, rk) with vertex set {x1, . . . , xk} by taking {xi, xj} as an edge whenever B(xi, ri) ∩ B(xj, rj) ≠ ∅.


<!-- p:184 -->


The following theorem shows that ηG is stationary and yields a formula for its intensity. To ease notation, for each k ∈ N we define a function hk ∈ R+((Rd × R+)k) by

$$h _ { k } ( x _ { 1 } , r _ { 1 } , \dots , x _ { k } , r _ { k } ) \colon = \mathbb { E } \left [ \lambda _ { d } \left ( \bigcup _ { j = 1 } ^ { k } B ( x _ { j } , R _ { 0 } + r _ { j } ) \right ) \right ] ,$$

where R0 has distribution Q.

Theorem 16.8 Let k ∈ N with k ≥ 2 and suppose that G is a connected graph with k vertices. Then the point process ηG is stationary with intensity

$$\gamma _ { G } \colon = & \, \gamma ^ { k } \iint \{ 0 < y _ { 2 } < \cdots < y _ { k } \} \{ \Gamma _ { k } ( y _ { 1 } , r _ { 1 } , \dots , y _ { k } , r _ { k } ) \simeq G \} \\ & \quad \times \exp [ - \gamma h _ { k } ( y _ { 1 } , r _ { 1 } , \dots , y _ { k } , r _ { k } ) ] \, d ( y _ { 2 } , \dots , y _ { k } ) \, \mathbb { Q } ^ { k } ( d ( r _ { 1 } , \dots , r _ { k } ) ) ,$$

where y1 := 0.

Proof Let N* denote the measurable set of all μ ∈ N(Rd × R+) such that μ(· × Y) ∈ Nls (the space of all locally finite simple counting measures on Rd). It is no restriction of generality to assume that ξ is a random element of N* and that η is a random element of Nls. We construct a measurable mapping TG : N* → Nls as follows. Given μ ∈ N* and (x1, r1) ∈ Rd × R+, define fG(x1, r1, μ) := 1 if and only if (x1, r1) ∈ μ, there are (x2, r2), . . . , (xk, rk) ∈ μ such that Γk(x1, r1, . . . , xk, rk) ∼ G, x1 &lt; · . · &lt; xk and B(xi, ri) ∩ B(x, r) = ∅ for all i ∈ {1, . . . , k} and all (x, r) ∈ μ − δ(x1,r1) − . . . − δ(xk,rk); otherwise set fG(x1, r1, μ) := 0. Then set

$$T _ { G } ( \mu ) \colon = \int 1 \{ x _ { 1 } \in \cdot \} f _ { G } ( x _ { 1 } , r _ { 1 } , \mu ) \, \mu ( d ( x _ { 1 } , r _ { 1 } ) )$$

and note that ηG = TG(ξ). The mapping TG has the (covariance) property

$$T _ { G } ( \theta _ { x } ^ { * } \mu ) = \theta _ { x } T _ { G } ( \mu ) , \quad ( x , \mu ) \in \mathbb { R } ^ { d } \times \mathbb { N } ^ { * } ,$$

hh       (( s  (   s  by

$$\theta _ { x } ^ { * } \mu \colon = \int 1 \{ ( y - x , r ) \in \cdot \} \, \mu ( d ( x , r ) ) .$$

By Exercise 16.5we have

$$( 1 6 . 2 5 )$$


<!-- p:185 -->


Combining this fact with (16.24) shows for all x ∈ Rd that

$$\theta _ { x } \eta _ { G } = \theta _ { x } T _ { G } ( \xi ) = T _ { G } ( \theta _ { x } ^ { * } \xi ) \stackrel { d } { = } T _ { G } ( \xi ) = \eta _ { G } .$$

Thus, ηG is stationary.

Let (Xi1 , Ri1), . . . , (Xik, Rik) be distinct points of ξ. The graph

$$\Gamma ^ { \prime } \coloneqq G ( X _ { i _ { 1 } } , \dots , X _ { i _ { k } } , \chi ) = \Gamma _ { k } ( X _ { i _ { 1 } } , R _ { i _ { 1 } } , \dots , X _ { i _ { k } } , R _ { i _ { k } } )$$

is a component isomorphic to G if and only if Γ' ≈ G and none of the Xi, is connected to any point in η − δx, − . . . − δxiμ . Let C ∈ Bd with λd(C) = 1. By the multivariate Mecke equation for ξ (Theorem 4.5),

$$\text {By the multivariate Meecke equation for } & \xi ( \text {the} \text {rem} \, 4 . 3 ) , \\ & \mathbb { E } [ \eta _ { G } ( C ) ] = \gamma ^ { k } \iint \{ 1 _ { x _ { 1 } } \in C , x _ { 1 } < \cdots < x _ { k } \} \{ \Gamma _ { k } ( x _ { 1 } , r _ { 1 } , \dots , x _ { k } , r _ { k } ) \simeq G \} \\ & \quad \times \mathbb { P } ( \xi ( B _ { x _ { 1 } , r _ { 1 } , \dots , x _ { k } , r _ { k } } ) = 0 ) \, d ( x _ { 1 } , \dots , x _ { k } ) \, \mathbb { Q } ^ { k } ( d ( r _ { 1 } , \dots , r _ { k } ) ) ,$$

where

$$B _ { x _ { 1 } , r _ { 1 } , \dots , x _ { k } , r _ { k } } \colon = \left \{ ( y , r ) \in \mathbb { R } ^ { d } \times [ 0 , \infty ) \, \colon B ( y , r ) \cap \bigcup _ { j = 1 } ^ { k } B ( x _ { j } , r _ { j } ) \neq \emptyset \right \} .$$

It follows that

$$It follows that \\ \mathbb { E } [ \eta _ { G } ( C ) ] = \gamma ^ { k } \iint \mathfrak { 1 } \{ x _ { 1 } \in C , x _ { 1 } < \cdots < x _ { k } \} \mathfrak { 1 } \{ \Gamma _ { k } ( x _ { 1 } , r _ { 1 } , \dots , x _ { k } , r _ { k } ) \simeq G \} \\ \times \exp \left [ - \gamma \int h _ { k } ^ { \prime } ( y , x _ { 1 } , r _ { 1 } , \dots , x _ { k } , r _ { k } ) \, d y \right ] d ( x _ { 1 } , \dots , x _ { k } ) \, \mathbb { Q } ^ { k } ( d ( r _ { 1 } , \dots , r _ { k } ) ) , \\ \text {where}$$

where

$$h _ { k } ^ { \prime } ( y , x _ { 1 } , r _ { 1 } , \dots , x _ { k } , r _ { k } ) \colon = \mathbb { P } \left ( B ( y , R _ { 0 } ) \cap \bigcup _ { j = 1 } ^ { k } B ( x _ { j } , r _ { j } ) \neq \emptyset \right ) .$$

Since B(y, R0)∩∪kj=1 B(xj, rj) ≠ ∅ if and only if y ∈ ∪kj=1 B(xj, R0 + rj), we obtain from Fubini's theorem that

$$\int h _ { k } ^ { \prime } ( y , x _ { 1 } , r _ { 1 } , \dots , x _ { k } , r _ { k } ) \, d y = h _ { k } ( x _ { 1 } , r _ { 1 } , \dots , x _ { k } , r _ { k } ) .$$

Note that

$$\Gamma _ { k } ( x _ { 1 } , r _ { 1 } , \dots , x _ { k } , r _ { k } ) \simeq \Gamma _ { k } ( 0 , r _ { 1 } , x _ { 2 } - x _ { 1 } , r _ { 2 } , \dots , x _ { k } - x _ { 1 } , r _ { k } )$$

and that x1 &lt; . . · &lt; xk if and only if 0 &lt; x2 − x1 &lt; · . · &lt; xk − x1. Moreover,

$$h _ { k } ( x _ { 1 } , r _ { 1 } , \dots , x _ { k } , r _ { k } ) = h _ { k } ( 0 , r _ { 1 } , x _ { 2 } - x _ { 1 } , r _ { 2 } , \dots , x _ { k } - x _ { 1 } , r _ { k } ) .$$

Performing the change of variables yi := xi − x1 for i ∈ {2, . . . , k} and using the fact that λa(C) = 1 gives the asserted formula (16.23). □


<!-- p:186 -->


If the graph G has only one vertex, then η1 := ηG is the point process of isolated points of the Gilbert graph (η, χ). In this case (a simplified version of) the proof of Theorem 16.8 yields that η1 is a stationary point process with intensity

$$\gamma _ { 1 } & \coloneqq \gamma \int \exp ( - \gamma \mathbb { E } [ \lambda _ { d } ( B ( 0 , R _ { 0 } + r ) ) ] ) \, \mathbb { Q } ( d r ) \\ & = \gamma \int \exp \left ( - \gamma \kappa _ { d } \, \mathbb { E } [ ( R _ { 0 } + r ) ^ { d } ] \right ) \mathbb { Q } ( d r ) ,$$

where κd := λd(B(0, 1)) is the volume of the unit ball.

For k ∈ N let Gk denote a set of connected graphs with k vertices containing exactly one member of each isomorphism equivalence class. Thus for any connected graph G with k vertices there is exactly one G' ∈ Gk such that G ≈ G'. Then ΣGeGk ηG is a stationary point process counting the k-components of (η,χ), that is the components with k vertices.

Example 16.9 The set G2 contains one graph, namely one with two vertices and one edge. By Theorem 16.8, the intensity of 2-components is given by

$$\frac { \gamma ^ { 2 } } { 2 } \iint & \{ \| z \| \leq r _ { 1 } + r _ { 2 } \} \\ & \times \exp \left ( - \gamma \mathbb { E } [ \lambda _ { d } ( B ( 0 , R _ { 0 } + r _ { 1 } ) \cup B ( z , R _ { 0 } + r _ { 2 } ) ) ] \right ) d z \mathbb { Q } ^ { 2 } ( d ( r _ { 1 } , r _ { 2 } ) ) .$$

For x ∈ η denote by C(x) the set of vertices in the component containing x. This set consists of x and all vertices y ∈ η connected to x in the Gilbert graph. For k ∈ N we let

$$\eta _ { k } \coloneqq \int 1 \{ x \in \cdot , \text { card} \, C ( x ) = k \} \, \eta ( d x )$$

denote the point process of all points of η that belong to a component of order k. Note that η1 is the point process of isolated points introduced previously.

Theorem 16.10 Let k ≥ 2. Then ηk is a stationary point process with intensity

$$\gamma _ { k } & \colon = \frac { \gamma ^ { k } } { ( k - 1 ) ! } \iint \mathbf 1 \{ \Gamma ( y _ { 1 } , r _ { 1 } , \dots , y _ { k } , r _ { k } ) \, \text {is connected} \} \\ & \times \exp [ - \gamma h _ { k } ( y _ { 1 } , r _ { 1 } , \dots , y _ { k } , r _ { k } ) ] \, d ( y _ { 2 } , \dots , y _ { k } ) \, \mathbb { Q } ^ { k } ( d ( r _ { 1 } , \dots , r _ { k } ) ) ,$$

where y1 := 0.


<!-- p:187 -->


Proof Stationarity of ηk follows as at (16.26).

Let G ∈ Gk and j ∈ {1, ... , k}. In the definition of ηG we used the lexicographically smallest point to label a component. Using instead the j-smallest point yields a stationary point process ηG. Exactly as in the (j) proof of Theorem 16.8 it follows that ηG) has intensity

$$\gamma _ { G } ^ { ( j ) } \colon = \gamma ^ { k } \int _ { B _ { j } } 1 \{ \Gamma _ { k } ( y _ { 1 } , r _ { 1 } , \dots , y _ { k } , r _ { k } ) \simeq G \}$$

$$\gamma _ { G } ^ { ( j ) } \colon = & \ \gamma ^ { k } \int _ { B _ { j } } 1 \{ \Gamma _ { k } ( y _ { 1 } , r _ { 1 } , \dots , y _ { k } , r _ { k } ) \simeq G \} \\ & \times \exp [ - \gamma h _ { k } ( y _ { 1 } , r _ { 1 } , \dots , y _ { k } , r _ { k } ) ] \, d ( y _ { 2 } , \dots , y _ { k } ) \, \mathbb { Q } ^ { k } ( d ( r _ { 1 } , \dots , r _ { k } ) ) ,$$

where y1 := 0 and Bj denotes the set of all (y2, . . . , yk) ∈ (Rd)k-1 such that y2 &lt; · . . &lt; yk and 0 &lt; y2 for j = 1, y j−1 &lt; 0 &lt; yj for j ∈ {2, . . . , k − 1} and

$$\gamma _ { k } = \gamma ^ { k } \int \mathbf 1 \{ y _ { 2 } < \cdots < y _ { k } \} \mathbf 1 \{ \Gamma _ { k } ( y _ { 1 } , r _ { 1 } , \dots , y _ { k } , r _ { k } ) \text { is connected} \} \\ \times \exp [ - \gamma h _ { k } ( y _ { 1 } , r _ { 1 } , \dots , y _ { k } , r _ { k } ) ] \, d ( y _ { 2 } , \dots , y _ { k } ) \, \mathbb { Q } ^ { k } ( d ( r _ { 1 } , \dots , r _ { k } ) ) ,$$

so that the symmetry of the integrand (without the first indicator) implies the asserted identity (16.29). □

The quantity γk/γ is the fraction of Poisson points that belong to a component of order k. Hence it can be interpreted as probability that a typical point of η belongs to a component of order k. This interpretation can be deepened by introducing the point process η0 := η + δ0 and the Gilbert graph (η0, χ0), where η0 := η + δ0 and χ0 is a point process on R[2d] that is defined (in terms of an independent marking of η0) as before. Then

$$\mathbb { P } ( \text {card} \, C ^ { 0 } ( 0 ) = k ) = \gamma _ { k } / \gamma , \quad k \in \mathbb { N } , \quad ( 1 6 . 3 0 )$$

where C0(x) is the component of x ∈ η0 in the Gilbert graph (η0, χ0); see Exercise 16.6.

### 16.5 The Point Process of Isolated Nodes

In this section we compute the pair correlation function of the point process η1 of isolated nodes.

Proposition 16.11 The pair correlation function ρ2 of η1 is given, for λd-a.e. x ∈ Rd, by

$$\rho _ { 2 } ( x ) & = \frac { \gamma ^ { 2 } } { \gamma _ { 1 } ^ { 2 } } \int \{ 1 | | x | > r + s \} \\ & \quad \times \exp ( - \gamma \mathbb { E } [ \lambda _ { d } ( B ( 0 , R _ { 0 } + r ) \cup B ( x , R _ { 0 } + s ) ) ] ) \, \mathbb { Q } ^ { 2 } ( d ( r , s ) ) .$$


<!-- p:188 -->


Proof Let m, n ∈ N with m ≠ n. Then Xm and X are isolated if and only if ∥Xm − Xn|| &gt; Rm + Rn and

$$( B ( X _ { m } , R _ { m } ) \cup B ( X _ { n } , R _ { n } ) ) \cap \bigcup _ { k \neq m , n } B ( X _ { k } , R _ { k } ) = \emptyset .$$

Hence we obtain from the bivariate Mecke equation (Theorem 4.5) that the reduced second factorial moment measure of η1 (see Definition 8.6) is given by

$$\alpha _ { 2 } ^ { ! } ( B ) & = \gamma ^ { 2 } \iint \mathbf 1 _ { x _ { 1 } } \in [ 0 , 1 ] ^ { d } , x _ { 2 } - x _ { 1 } \in B \mathbf 1 \{ \| x _ { 2 } - x _ { 1 } \| > r + s \} \\ & \quad \times \mathbb { P } ( ( B ( x _ { 1 } , r ) \cup B ( x _ { 2 } , s ) ) \cap Z = \emptyset ) \, d ( x _ { 1 } , x _ { 2 } ) \, \mathbb { Q } ^ { 2 } ( d ( r , s ) ) , \quad B \in \mathcal { B } ^ { d } .$$

From (16.12), a change of variable and translation invariance of Lebesgue measure it follows that

$$\ m a t h s c r { E } ( B ) = & \gamma ^ { 2 } \iint \{ 1 \{ x \in B \} 1 \{ \| x \| > r + s \} \\ & \quad \times \exp ( - \gamma \mathbb { E } [ \lambda _ { d } ( B ( 0 , R _ { 0 } + r ) \cup B ( x , R _ { 0 } + s ) ) ] ) \, \mathbb { Q } ^ { 2 } ( d ( r , s ) ) \, d x .$$

Hence the assertion follows from Definition 8.9.

□

In the case of deterministic radii we have the following result.

Corollary 16.12 Assume that Q = δs/2 for some s ≥ 0. Then the pair correlation function ρ2 of η1 is given, for λd-a.e. x ∈ Rd, by

$$\rho _ { 2 } ( x ) = 1 \{ | | x | | > s \} \exp [ \gamma \, \lambda _ { d } ( B ( 0 , s ) \cap B ( x , s ) ) ] .$$

Proof By the additivity and invariance property of Lebesgue measure the right-hand side of (16.31) equals

$$\frac { \gamma ^ { 2 } } { \gamma _ { 2 } ^ { 2 } } 1 \{ \| x \| > s \} \exp [ - 2 \gamma \lambda _ { d } ( B ( 0 , s ) ) ] \exp [ \gamma \lambda _ { d } ( B ( 0 , s ) \cap B ( x , s ) ) ] .$$

Inserting here the formula (16.27) for γ1 yields the result.

### 16.6 Exercises

Exercise 16.1 Let Z be a Boolean model as in Definition 16.1 and assume that E[Rd] &lt; ∞. For n ∈ N let Yn := ξ({(x, r) : B(x, r) ∩ B(0, n) ≠ 0}). Show that E[Yn] &lt; ∞. Let A := ∩n≥1{Yn &lt; ∞}. Show that P(A) = 1 and that Z(ω) is closed for each ω ∈ A.

□


<!-- p:189 -->


Exercise 16.2 Given a Boolean model based on the Poisson process η, let us say that a point x ∈ η is visible if x is contained in exactly one of the balls B(X, R), n ∈ N. Show that the point process ηv of visible points is stationary with intensity

$$\gamma _ { v } \colon = \gamma \, \mathbb { E } [ \exp \left ( - \gamma \kappa _ { d } \, \mathbb { E } [ R _ { 1 } ^ { d } ] \right ) ] .$$

Now let c &gt; 0 and consider the class of all Boolean models with the same intensity γ and radius distributions Q satisfying ∫ r Q(dr) = c. Show that the intensity of visible points is then minimised by the distribution Q concentrated on a single point. (Hint: Use Jensen's inequality to prove the second part.)

Exercise 16.3 Let Z be a Boolean model with intensity γ and assume E[Rd] &lt; ∞. Let L be a one-dimensional line embedded in Rd (e.g., the first coordinate axis). Show that Z∩L is a one-dimensional Boolean model with intensity γκa-1E[Rd-1]. Use this to obtain an alternative proof of Proposition 16.6. What is the radius distribution of the Boolean model Z ∩ L?

Exercise 16.4 Consider the Gilbert graph under the assumption that R has an infinite mean. Show that γG = 0 for any connected graph G (with a finite number of vertices).

Exercise 16.5 Prove the stationarity relation (16.25).

Exercise 16.6 Prove (16.30).

Exercise 16.7 Consider the Gilbert graph under the assumption that Rd has a finite mean. Show that the pair correlation function ρ2 of the point process η1 of isolated nodes satisfies lim|x|→∞ ρ2(x) = 1.

Exercise 16.8 Consider the Gilbert graph under the assumption that Rd has a finite mean. Given an edge e of the Gilbert graph, let the left endpoint of e be the first of its endpoints in the lexicographic ordering. Define a point process ξ on Rd by setting ξ(B) to be the number of edges of the Gilbert graph having left endpoint in B, for each Borel B ⊂ Rd. Show that ξ is a stationary point process with intensity (γ2 /2) ∫ P(R0 + R1 ≥ ∥|x|l) dx, where R1 is independent of R0 and has the same distribution. Is ξ a simple point process?


<!-- p:190 -->


## The Boolean Model with General Grains

The spherical Boolean model Z is generalised so as to allow for arbitrary random compact grains. The capacity functional of Z can again be written in an exponential form involving the intensity and the grain distribution. This implies an explicit formula for the covariance of Z. Moreover, in the case of convex grains, the Steiner formula of convex geometry leads to a formula for the spherical contact distribution function involving the mean intrinsic volumes of a typical grain. In the general case the capacity functional determines the intensity and the grain distribution up to a centring.

### 17.1 Capacity Functional

Let C(d) denote the space of non-empty compact subsets of Rd and define the Hausdorff distance between sets K, L ∈ C(d) by

$$\delta ( K , L ) \coloneqq \inf \{ \varepsilon \geq 0 \, \colon K \subset L \oplus B ( 0 , \varepsilon ) , L \subset K \oplus B ( 0 , \varepsilon ) \} .$$

It is easy to check that δ(·, ·) is a metric. By Theorem A.26, C(d) is a CSMS. We equip C(d) with the associated Borel σ-field B(C(d)). For B ⊂ Rd and x ∈ Rd we recall the notation B + x := {y + x : y ∈ B}.

Definition 17.1 Let η be a stationary Poisson process on Rd with intensity γ &gt; 0, given as in (16.1). Let Q be a probability measure on C(d) and let

$$\xi = \sum _ { n = 1 } ^ { \infty } \delta _ { ( X _ { n } , Z _ { n } ) }$$

be an independent Q-marking of η. Then

$$Z \colon = \bigcup _ { n = 1 } ^ { \infty } ( Z _ { n } + X _ { n } ) & & ( 1 7 . 3 )$$

is called the Boolean model with intensity γ and grain distribution Q (or the Boolean model induced by ξ for short).


<!-- p:191 -->


As in Chapter 16, Z is a short-hand notation for the mapping ω → Z(ω). We wish to generalise Theorem 16.2 for the spherical Boolean model and give a formula for the capacity functional C → P(Z∩C ≠ Ø) of Z. As preparation we need to identify useful generators of the Borel σ-field B(C(d)). For B ⊂ Rd define

$$C _ { B } \colon = \{ K \in C ^ { ( d ) } \colon K \cap B \neq \emptyset \} ; \quad C ^ { B } \colon = \{ K \in C ^ { ( d ) } \colon K \cap B = \emptyset \} .$$

Lemma 17.2 The σ-field B(C(d)) is generated by {CB : B ∈ C(d)}.

Proof It is a quick consequence of the definition of the Hausdorff distance that CB is open whenever B ∈ C(d). Hence the σ-field H generated by {CB : B ∈ C(d)} is contained in B(C(d)).

To prove B(C(d)) ⊂ H we first note that C(a), equipped with the Hausdorff distance, is a separable metric space, that is has a countable dense set; see Exercise 17.3. It follows from elementary properties of separable metric spaces that any open set in C(a) is either empty or a countable union of closed balls. Hence it is sufficient to show that for any K ∈ C(d) and ε &gt; 0 the closed ball

$$B ( K , \varepsilon ) = \{ L \in \mathcal { C } ^ { ( d ) } \, \colon L \subset K \oplus B ( 0 , \varepsilon ) , K \subset L \oplus B ( 0 , \varepsilon ) \}$$

is in H. Since L ⊂ K ⊕ B(0, ε) is equivalent to L ∩ (Rd \ (K ⊕ B(0, ε))) = 0 we have

$$\{ L \in C ^ { ( d ) } \colon L \subset K \oplus B ( 0 , \varepsilon ) \} & = \bigcap _ { n \in \mathbb { N } } \{ L \in C ^ { ( d ) } \colon L \cap ( B _ { n } \ \lor ( K \oplus B ( 0 , \varepsilon ) ) ) = \emptyset \} , \\$$

where B is the interior of the ball B(0, n). Since A := B \ K ⊕ B(0, ε) is open, it is easy to prove that CA ∈ H, so that the right-hand side of (17.5) is in H as well. It remains to show that Cκ,ε := {L ∈ C(d) : K ⊂ L⊕ B(0, ε)} is in H. To this end we take a countable dense set D ⊂ K (see Lemma A.22) and note that K  L ⊕ B(0, ε) if and only if there exists x ∈ D such that B(x, ε) ∩ L = Ø. (Use (16.6) and a continuity argument.) Therefore C(d) \ Cκ,ε is a countable union of sets of the form CB, where B is a closed ball. Hence Cκ,ε ∈ H and the proof is complete. □

For C ⊂ Rd let C* := {−x : x ∈ C} denote the reflection of C in the origin.

Theorem 17.3 Let Z be a Boolean model with intensity γ and grain distribution Q. Then (16.4) holds and, moreover,

$$\mathbb { P } ( Z \cap C = \emptyset ) = \exp \left [ - \gamma \int \lambda _ { d } ( K \oplus C ^ { * } ) \, \mathbb { Q } ( d K ) \right ] , \quad C \in \mathcal { C } ^ { ( d ) } .$$


<!-- p:192 -->


Proof We can follow the proof of Theorem 16.2. By Exercise 17.6, the mapping (x, K) → K + x from Rd × C(d) to C(d) is continuous and hence measurable. Take C ∈ C(d). By Lemma 17.2,

$$A \colon = \{ ( x , K ) \in \mathbb { R } ^ { d } \times C ^ { ( d ) } \colon ( K + x ) \cap C \neq \emptyset \}$$

is a measurable set. Since (16.9) holds, (16.4) follows. Moreover, since ξ is a Poisson process with intensity measure γλd ⊗ Q we again obtain (16.10). Using the fact that

$$\{ x \in \mathbb { R } ^ { d } \colon ( K + x ) \cap C \neq \emptyset \} = C \oplus K ^ { * } ,$$

together with the reflection invariance of Lebesgue measure, we obtain the assertion (17.6). □

Taking B = {x} in (17.6) yields, as in (16.13), that

$$\mathbb { P } ( x \in Z ) = 1 - \exp \left ( - \gamma \, \int \lambda _ { d } ( K ) \, \mathbb { Q } ( d K ) \right ) , \quad x \in \mathbb { R } ^ { d } .$$

The quantity p := P(0 ∈ Z) is the volume fraction of Z.

Proposition 17.4 The mapping (ω, x) → 1z(ω)(x) is measurable and

$$\mathbb { E } [ \lambda _ { d } ( Z \cap B ) ] = p \lambda _ { d } ( B ) , \quad B \in \mathcal { B } ( \mathbb { R } ^ { d } ) .$$

Proof By (17.2),

$$1 - 1 _ { Z } ( x ) = \prod _ { n = 1 } ^ { \infty } 1 \{ x \notin Z _ { n } + X _ { n } \} , \quad x \in \mathbb { R } ^ { d } . \\$$

Therefore the asserted measurability follows from the fact that the mappings (x, K) ↔ 1{x ∉ K} and (x, K) → K + x are measurable on Rd × C(d); see Exercises 17.6 and 17.7. Equation (17.9) can then be proved in the same manner as (16.14). □

In what follows we shall always assume that

$$\int \lambda _ { d } ( K \oplus B ( 0 , r ) ) \, \mathbb { Q } ( d K ) < \infty , \ \ r \geq 0 .$$

By Exercise 17.1 we can assume, as in Section 16.3, that Z(ω) is a closed set for each ω ∈ Ω. By the next result, Z is a random element of the space Fd of closed subsets of Rd, equipped with the σ-field B(Fd) generated by the Fell topology; see Section A.3.

Proposition 17.5 Assume that (17.10) holds. Then Z is a random element of Fd.


<!-- p:193 -->


Proof The assertion follows from Theorem 17.3 and Lemma A.28.

By Lemma A.27 the mapping (F, x) → F + x from Fd × Rd to Fd is continuous and hence measurable. In particular, Z + x is, for each x ∈ Rd, again a random element of Fd. The next result says that Z is stationary.

Proposition 17.6 Assume that (17.10) holds. Let x ∈ Rd. Then Z + x = Z.

Proof We need to prove that P(Z + x ∈ A) = P(Z ∈ A) holds for each A ∈ B(Fd). By Lemma A.28 and Theorem A.5 it is sufficient to show for each C ∈ C(d) that P((Z + x) ∩ C = ∅) = P(Z∩C = ∅). Since (Z + x) ∩ C = ∅ if and only if Z ∩ (C – x) = 0, the assertion follows from Theorem 17.3 and translation invariance of Lebesgue measure. □

### 17.2 Spherical Contact Distribution Function and Covariance

In this section we first give a more general version of Proposition 16.5 under an additional assumption on Q. Let K(d) denote the system of all convex K ∈ C(d). By Theorem A.26, K(d) is a closed and hence measurable subset of C(a). Recall from Section A.3 the definition of the intrinsic volumes V0, . . . , Va as non-negative continuous functions on K(d). If the grain distribution Q is concentrated on K(d) (i.e. Q(K(d)) = 1), then we can define

$$\phi _ { i } \colon = \int V _ { i } ( K ) \, \mathbb { Q } ( d K ) , \ \ i = 0 , \dots , d .$$

Note that φ0 = 1. The Steiner formula (A.22) implies that φi &lt; ∞ for all i ∈ {0, . . . , d} if and only if (17.10) holds. The spherical contact distribution function H. of Z is defined by (16.17).

Proposition 17.7 Suppose that (17.10) holds and that Q is concentrated on K(d). Then the spherical contact distribution function of the Boolean model Z is given by

$$H _ { \circ } ( t ) = 1 - \exp \left [ - \sum _ { j = 0 } ^ { d - 1 } t ^ { d - j } \kappa _ { d - j } \gamma \phi _ { j } \right ] , \quad t \geq 0 ,$$

where φo, . . , φd are defined by (17.11).

Proof Let t ≥ 0. Similarly to the proof of Proposition 16.5 we obtain from (17.6) that

$$1 - H _ { \circ } ( t ) = \exp \left [ - \gamma \int ( \lambda _ { d } ( K \oplus B ( 0 , t ) ) - \lambda _ { d } ( K ) ) \, \mathbb { Q } ( d K ) \right ] .$$


<!-- p:194 -->


By assumption on Q we can use the Steiner formula (A.22) (recall that Vd = λd) to simplify the exponent and to conclude the proof of (17.12). □

Next we deal with second order properties of the Boolean model. The function (x, y) → P(x ∈ Z, y ∈ Z) is called the covariance (or two point correlation function) of Z. It can be expressed in terms of the function

$$\beta _ { d } ( x ) \colon = \int \lambda _ { d } ( K \cap ( K + x ) ) \, \mathbb { Q } ( d K ) , \quad x \in \mathbb { R } ^ { d } ,$$

as follows.

Theorem 17.8 Suppose that (17.10) holds. The covariance of Z is given by

$$\mathbb { P } ( x \in Z , y \in Z ) = p ^ { 2 } + ( 1 - p ) ^ { 2 } ( e ^ { \gamma \beta _ { d } ( x - y ) } - 1 ) , \quad x , y \in \mathbb { R } ^ { d } .$$

Proof Let Z0 have distribution Q and let x, y ∈ Rd. By (17.6),

$$\mathbb { P } ( Z \cap \{ x , y \} & = \emptyset ) = \exp ( - \gamma \mathbb { E } [ \lambda _ { d } ( ( Z _ { 0 } - x ) \cup ( Z _ { 0 } - y ) ) ] ) \\ & = \exp ( - \gamma \mathbb { E } [ \lambda _ { d } ( Z _ { 0 } \cup ( Z _ { 0 } + x - y ) ) ] ) .$$

By additivity of λa and linearity of expectation we obtain

$$\mathbb { P } ( Z \cap \{ x , y \} & = \emptyset ) = \exp ( - 2 \gamma \mathbb { E } [ \lambda _ { d } ( Z _ { 0 } ) ] ) \exp ( \gamma \mathbb { E } [ \lambda _ { d } ( Z _ { 0 } \cap ( Z _ { 0 } + x - y ) ) ] ) \\ & = ( 1 - p ) ^ { 2 } \exp [ \gamma \beta _ { d } ( x - y ) ] ,$$

where we have used (17.8). By the additivity of probability,

$$\mathbb { P } ( Z \cap \{ x , y \} = \emptyset ) = \mathbb { P } ( x \notin Z , y \notin Z ) = \mathbb { P } ( x \in Z , y \in Z ) + 1 - 2 p$$

and the result follows.

□

### 17.3 Identifiability of Intensity and Grain Distribution

In this section we shall prove that the capacity functional of a Boolean model Z determines the intensity and the centred grain distribution of the underlying marked Poisson process. To this end we need the following lemma, which is of some independent interest.

Lemma 17.9 Let v be a measure on C(d) satisfying

$$\nu ( C _ { B } ) < \infty , \ \ B \in \mathcal { C } ^ { ( d ) } .$$

Then v is determined by its values on {CB : B ∈ C(d)}.


<!-- p:195 -->


Proof For m ∈ N and B0, . . . , Bm ∈ Cd = C(d) ∪ {0} let

$$C _ { B _ { 1 } , \dots , B _ { m } } ^ { B _ { 0 } } \colon = \mathcal { C } ^ { B _ { 0 } } \cap \mathcal { C } _ { B _ { 1 } } \cap \dots \cap \mathcal { C } _ { B _ { m } } .$$

Since CB0 ∩ CB′ = CB0∪B′ for all B0, B′ ∈ Cd, the sets of the form (17.15) form a π-system. By Lemma 17.2 this is a generator of B(C(d)). Since (17.14) easily implies that v is σ-finite, the assertion follows from Theorem A.5 once we have shown that

$$\nu ( C _ { B _ { 1 } , \dots , B _ { m } } ^ { B _ { 0 } } ) = \sum _ { j = 0 } ^ { m } ( - 1 ) ^ { j + 1 } \sum _ { 1 \leq i _ { 1 } < \dots < i _ { j } \leq m } \nu ( C _ { B _ { 0 } \cup B _ { i _ { 1 } } \cup \dots \cup B _ { i _ { j } } } ) .$$

In fact, we only need the case with B0 = 0, but it is simpler to prove the more general case. Moreover, the identity (17.16) is of some independent interest. For m = 1 the identity means that

$$\nu ( C _ { B _ { 1 } } ^ { B _ { 0 } } ) = \nu ( C _ { B _ { 0 } \cup B _ { 1 } } ) - \nu ( C _ { B _ { 0 } } ) ,$$

a direct consequence of the equality C = CB0B1 \CB0. In the general case B1 we can use the equality

$$C _ { B _ { 1 } , \dots , B _ { m } } ^ { B _ { 0 } } = C _ { B _ { 1 } , \dots , B _ { m - 1 } } ^ { B _ { 0 } } \, \vee \, C$$

and induction.

□

We need to fix a centre function c: C(d) → Rd. This is a measurable function satisfying

$$c ( K + x ) = c ( K ) + x , \ \ ( x , K ) \in \mathbb { R } ^ { d } \times \mathcal { C } ^ { ( d ) } .$$

An example is the centre of the (uniquely determined) circumball of K, that is the smallest ball containing K.

Theorem 17.10 Let Z and Z' be Boolean models with respective intensities γ and γ' and grain distributions Q and Q'. Assume that Q satisfies (17.10). If

$$\mathbb { P } ( Z \cap B = \emptyset ) = \mathbb { P } ( Z ^ { \prime } \cap B = \emptyset ) , \ \ B \in \mathcal { C } ^ { ( d ) } ,$$

then γ = γ′ and Q({K : K − c(K) ∈ ·}) = Q′({K : K − c(K) ∈ ·}).

Proof Define a measure γ on (C(d), B(C(d)) by

$$\nu ( \cdot ) \colon = \gamma \iint \mathbf 1 \{ K + x \in \cdot \} \, \mathbb { Q } ( d K ) \, d x .$$

Similarly define a measure v′ by replacing (γ, Q) with (γ′, Q'). By (17.10)


<!-- p:196 -->


for B ∈ C(d) we have K ⊕ B* = {x ∈ Rd : K + x ∈ CB}. Theorem 17.3 then shows that

$$\nu ( C _ { B } ) = - \log \mathbb { P } ( Z \cap B = \emptyset ) , \ \ B \in C ^ { ( d ) } .$$

Assuming that (17.18) holds, we hence obtain from assumption (17.10) that

$$\nu ( C _ { B } ) = \nu ^ { \prime } ( C _ { B } ) < \infty , \ \ B \in C ^ { ( d ) } .$$

In particular, both measures satisfy (17.14). By Lemma 17.9 we conclude that ν = ν′.

Take a measurable set A ⊂ C(d) and B ∈ Bd with λd(B) = 1. Then, using property (17.17) of a centre function,

$$\text {property (17/17)} \text { of a centre function,} \\ \intertext { s u p p } = \gamma \iint 1 \{ K + x - c ( K + x ) \in A , c ( K ) \in B \} \nu ( d K ) \\ = \gamma \iint 1 \{ K - c ( K ) \in A , c ( K ) + x \in B \} \\ = \gamma \mathbb { Q } ( \{ K \colon K - c ( K ) \in A \} ) . \\ \text {Since } \nu ^ { \prime } \ s a t i s f i e s \ a \, \text {similar equation and } \nu = \nu ^ { \prime } , \, \text {the}$$

Since v' satisfies a similar equation and v = v', the assertion follows.

### 17.4 Exercises

Exercise 17.1 Let Z be a Boolean model whose grain distribution Q satisfies (17.10). Prove that almost surely any compact set is intersected by only a finite number of the grains Zn + Xn, n ∈ N. Show then that Z is almost surely a closed set.

Exercise 17.2 Let m ∈ N and assume that ∫ λd(K ⊕ B(0, ε))n Q(dK) &lt; ∞ for some (fixed) ε &gt; 0. Prove that ∫ λd(K ⊕ B(0, r)) Q(dK) &lt; ∞ for each r &gt; 0.

Exercise 17.3 Show that the space C(d) equipped with the Hausdorff distance (17.1) is a separable metric space. (Hint: Use a dense countable subset of Rd.)

Exercise 17.4 Let m ∈ N and let C ⊂ C(d) be the space of all compact non-empty subsets of Rd with at most m points. Show that C is closed (with respect to the Hausdorff distance).

□


<!-- p:197 -->


Exercise 17.5 For i ∈ {1, 2}, let ei := {xi, yi}, where x1, x2, y1, y2 ∈ Rd satisfy x1 ≠ x2 and y1 ≠ y2. Show that the Hausdorff distance between e1 and e2 is given by

$$\delta ( e _ { 1 } , e _ { 2 } ) = ( \| x _ { 1 } - y _ { 1 } \| \vee \| x _ { 2 } - y _ { 2 } \| ) \wedge ( \| x _ { 1 } - y _ { 2 } \| \vee \| x _ { 2 } - y _ { 1 } \| ) .$$

Show that R[2d] is not closed in C(d). Use Exercise 17.4 to show that R[2d] is a measurable subset of C(d). Show finally that a set C ⊂ R[2d] is bounded if and only if U(C) is bounded, where U(C) is the union of all e ∈ C.

Exercise 17.6 Prove that the mapping (x, K) → K + x from Rd × C(d) to C(d) is continuous. Prove also that the mapping (K, L) → K ⊕ L is continuous on C(d) × C(d). Why is this a more general statement?

Exercise 17.7 Prove that the mapping (x, K) → 1K(x) from Rd × C(d) to R is measurable. (Hint: Show that {(x, K) ∈ Rd × C(d) : x ∈ K} is closed.)

Exercise 17.8 Let Z be a Boolean model whose grain distribution Q satisfies (17.10) as well as the equation Q({K ∈ C(d) : λd(∂K) = 0}) = 1, where ∂K is the boundary of a set K. Show that

$$\lim _ { x \to 0 } \mathbb { P } ( 0 \in Z , x \in Z ) = \mathbb { P } ( 0 \in Z ) .$$

Exercise 17.9 Let v be a measure on C(d) satisfying (17.14). Show that v is locally finite. Show also that the measure

$$\nu \colon = \left \lfloor _ { 0 } \ 1 \{ B ( 0 , r ) \in \cdot \} \, d r \right \rfloor$$

is locally finite but does not satisfy (17.14).

Exercise 17.10 Consider a Boolean model whose grain distribution Q satisfies

$$\int \lambda _ { d } ( K ) ^ { 2 } \, \mathbb { Q } ( d K ) < \infty .$$

Prove that ∫ (eγβd(x) − 1) dx &lt; ∞. (Hint: Use that et − 1 ≤ tet, t ≥ 0.)

Exercise 17.11 Let W ⊂ Rd be a Borel set with 0 &lt; λd(W) &lt; ∞ such that the boundary of W has Lebesgue measure 0. Show that

$$\lim _ { r \to \infty } \lambda _ { d } ( r W ) ^ { - 1 } \lambda _ { d } ( r W \cap ( r W + x ) ) = 1$$

for all x ∈ Rd, where rW := {rx : x ∈ W}. (Hint: Decompose W into its interior and W ∩ ∂W; see Section A.2.)


<!-- p:198 -->


## Fock Space and Chaos Expansion

The difference operator is the increment of a measurable function of a counting measure, upon adding an extra point. It can be iterated to yield difference operators of higher orders. Each square integrable function f(η) of a Poisson process η determines an infinite sequence of expected difference operators. This sequence is an element of a direct sum of Hilbert spaces, called the Fock space associated with the intensity measure of η. The second moment of f(η) coincides with the squared norm of this Fock space representation. A consequence is the Poincaré inequality for the variance of f(η). A deeper result is the orthogonal decomposition of f(η) into a series of Wiener-Itô integrals, known as the chaos expansion.

### 18.1 Difference Operators

Throughout this chapter we consider a Poisson process η on an arbitrary measurable space (X, X) with σ-finite intensity measure λ. Let Pη denote the distribution of η, a probability measure on N := N(X). Let f ∈ R(N). For x ∈ X define the function Dxf ∈ R(N) by

$$D _ { x } f ( \mu ) \colon = f ( \mu + \delta _ { x } ) - f ( \mu ) , \quad \mu \in \mathbf N .$$

Iterating this definition, we define Dx,...,n f ∈ R(N) for each n ≥ 2 and (x1, . . . , xn) ∈ Xn inductively by

$$D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } f \coloneqq D _ { x _ { 1 } } ^ { 1 } D _ { x _ { 2 } , \dots , x _ { n } } ^ { n - 1 } f , \\ \intertext { D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } } D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } f \coloneqq D _ { x _ { 1 } } ^ { 1 } D _ { x _ { 2 } , \dots , x _ { n } } ^ { n - 1 } f ,$$

where D1 := D and D0 f = f. Observe that

$$D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } f ( \mu ) = \sum _ { J \subset ( 1 , 2 , \dots , n ) } ( - 1 ) ^ { n - | J | } f ( \mu + \sum _ { j \in J } \delta _ { x _ { j } } ) ,$$

where |J denotes the number of elements of J. This shows that D f is able. As a function of f these operators are linear.


<!-- p:199 -->


Example 18.1 Assume that X = C(d) is the space of all non-empty compact subsets of Rd, as in Definition 17.1. For μ ∈ N let

$$Z ( \mu ) \coloneqq \bigcup _ { K \in \Omega } K$$

whenever μ is locally finite (with respect to the Hausdorff distance); otherwise let Z(μ) := 0. Let γ be a finite measure on Rd and define f : N → R+ by

$$f ( \mu ) \colon = \nu ( Z ( \mu ) ) .$$

Thanks to Theorem A.26 we can apply Proposition 6.3. Therefore we obtain for all x ∈ Rd and all locally finite μ ∈ N that

$$1 - 1 _ { Z ( \mu ) } ( x ) = \prod _ { n = 1 } ^ { \mu ( C ^ { ( d ) } ) } 1 \{ x \notin \pi _ { n } ( \mu ) \} .$$

Hence Exercise 17.7 shows that (x, μ) ↔ 1z(μ)(x) is measurable on Rd × N. In particular, f is a measurable mapping. For each locally finite μ ∈ N and each K ∈ C(d), we have

$$f ( \mu + \delta _ { K } ) = \nu ( Z ( \mu ) \cup K ) = \nu ( Z ( \mu ) ) + \nu ( K ) - \nu ( Z ( \mu ) \cap K ) ,$$

that is

$$D _ { K } f ( \mu ) = \nu ( K ) - \nu ( Z ( \mu ) \cap K ) = \nu ( K \cap Z ( \mu ) ^ { c } ) .$$

It follows by induction that

$$D _ { K _ { 1 } , \dots , K _ { n } } ^ { n } f ( \mu ) = ( - 1 ) ^ { n + 1 } \nu ( K _ { 1 } \cap \cdots \cap K _ { n } \cap Z ( \mu ) ^ { c } ) , \quad \mu \in N ,$$

for all n ∈ N and K1, . . . , K ∈ C(d).

The next lemma yields further insight into the difference operators. For h ∈ R(X) we set h®0 := 1 and recall from Chapter 12 that for n ∈ N the function h®n ∈ R(Xn) is defined by

$$h ^ { \otimes n } ( x _ { 1 } , \dots , x _ { n } ) \colon = \prod _ { i = 1 } ^ { n } h ( x _ { i } ) , \quad x _ { 1 } , \dots , x _ { n } \in \mathbb { X } .$$

Lemma 18.2 Let v ∈ R+(X) and define f ∈ R+(N) by f(μ) = exp[−μ(v)], μ ∈N. Let n ∈ N. Then

$$D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } f ( \mu ) = \exp [ - \mu ( v ) ] ( e ^ { - v } - 1 ) ^ { \otimes n } ( x _ { 1 } , \dots , x _ { n } ) , \ \ x _ { 1 } , \dots , x _ { n } \in \mathbb { X } .$$


<!-- p:200 -->


Proof For each μ ∈ N and x ∈ X we have

$$f ( \mu + \delta _ { x } ) = \exp \left [ - \int v ( y ) \left ( \mu + \delta _ { x } \right ) ( d y ) \right ] = \exp [ - \mu ( v ) ] \exp [ - v ( x ) ] ,$$

so that

$$D _ { x } f ( \mu ) = \exp [ - \mu ( v ) ] ( \exp [ - v ( x ) ] - 1 ) .$$

Iterating this identity yields for all n ∈ N and all x1, . . . , x ∈ X that

$$D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } f ( \mu ) = \exp [ - \mu ( v ) ] \prod _ { i = 1 } ^ { n } ( \exp [ - v ( x _ { i } ) ] - 1 )$$

and hence the assertion.

□

### 18.2 Fock Space Representation

Theorem 18.6 below is the main result of this chapter. To formulate it, we need to introduce some notation. For n ∈ N and f ∈ R(N) we define the symmetric measurable function Tf : Xn → R by

$$T _ { n } f ( x _ { 1 } , \dots , x _ { n } ) \colon = \mathbb { E } [ D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } f ( \eta ) ] ,$$

and set T0f := E[f(η)].

The inner product of u, v ∈ L2(λ") for n ∈ N is denoted by

$$\langle u , v \rangle _ { n } \colon = \int u v \, d \lambda ^ { n } .$$

Denote byl·ln := &lt;·, ·&gt;1/2 the associated norm. For n ∈ N let H be the space of symmetric functions in L2(λn), and let H0 := R. The Fock space H is the set of all sequences (un)n≥0 ∈ ×n=0Hn such that 〈(un)n≥0, (un)n≥0&gt;H &lt; ∞, where, for (vn)n≥0 ∈ ×n=0Hn, we set

$$\langle ( u _ { n } ) _ { n \geq 0 } , ( v _ { n } ) _ { n \geq 0 } \rangle _ { \text {H} } \colon = \sum _ { n = 0 } ^ { \infty } \frac { 1 } { n ! } \langle u _ { n } , v _ { n } \rangle _ { n }$$

and 〈a, b&gt;0 := ab for a, b ∈ R. The space H is a vector space under componentwise addition and scalar multiplication and ·, ·&gt;í is bilinear. It is a well-known analytic fact (the reader is invited to prove this as an exercise) that H is a Hilbert space, that is H is a complete metric space with respect to the metric ((un)n≥0, (vn)n≥0) ↔ (&lt;(un − vn)n≥0, (un − vn)n≥0&gt;H)1/2. In this section we prove that the mapping f → (T(f))n≥0 is an isometry from L2(Pη) to H.

Let X0 be the system of all measurable B ∈ X having λ(B) &lt; ∞. Let R0(X) be the space of all functions v ∈ R+(X) such that v is bounded and {x ∈ X : v(x) &gt; 0} ∈ X0. Let G denote the space of all functions g : N → R of the form


<!-- p:201 -->


$$g ( \mu ) = a _ { 1 } e ^ { - \mu ( v _ { 1 } ) } + \dots + a _ { n } e ^ { - \mu ( v _ { n } ) } , \quad \mu \in \mathbb { N } ,$$

where n ∈ N, a1, . . . , an ∈ R and v1, . . . , vn ∈ R0(X). All such functions are bounded and measurable.

For each f ∈ L2(Pη) define T f := (Tnf)n≥0, where Tf is given at (18.8). By the next result, T f ∈ H for f ∈ G and

$$\mathbb { E } [ f ( \eta ) g ( \eta ) ] = \langle T f , T g \rangle _ { \mathbb { H } } , \quad f , g \in G .$$

Later we shall see that these assertions remain true for all f, g ∈ L2(Pη).

Lemma 18.3 The mapping T is linear on G and T(f) ∈ H for all f ∈ G. Furthermore, equation (18.10) holds for all f, g ∈ G.

Proof Let v ∈ R0(X) and define f ∈ G by f(μ) = exp[−μ(v)], μ ∈ N. From (18.7) and Theorem3.9 we obtain

$$T _ { n } f = \exp [ - \lambda ( 1 - e ^ { - v } ) ] ( e ^ { - v } - 1 ) ^ { \otimes n } .$$

Since v ∈ R0(X) it follows that Tf ∈ H, n ≥ 0. Since the difference operators are linear, this remains true for every f ∈ G. Moreover, the mapping T is linear on G.

By linearity, it is now sufficient to prove (18.10) in the case

$$f ( \mu ) = \exp [ - \mu ( v ) ] , \ \ g ( \mu ) = \exp [ - \mu ( w ) ] , \ \mu \in \mathbb { N } ,$$

for v, w ∈ R0(X). Using Theorem3.9 again, we obtain

$$\mathbb { E } [ f ( \eta ) g ( \eta ) ] = \exp [ - \lambda ( 1 - e ^ { - ( v + w ) } ) ] .$$

On the other hand, we have from (18.11) that

$$\underline { \infty }$$

$$On the other hand, we have from ( 1 8 . 1 1 ) \text { that} \\ \sum _ { n = 0 } ^ { \infty } \frac { 1 } { n ! } \langle T _ { n } f , T _ { n } g \rangle _ { n } \\ = \exp [ - \lambda ( 1 - e ^ { - v } ) ] \exp [ - \lambda ( 1 - e ^ { - w } ) ] \sum _ { n = 0 } ^ { \infty } \frac { 1 } { n ! } \lambda ^ { n } ( ( e ^ { - v } - 1 ) ( e ^ { - w } - 1 ) ) ^ { \otimes n } ) \\ = \exp [ - \lambda ( 2 - e ^ { - v } - e ^ { - w } ) ] \exp [ \lambda ( e ^ { - v } - 1 ) ( e ^ { - w } - 1 ) ) ] . \\ \text {This equals the right side of } ( 1 8 1 ) \text { , Choosing } f = a \text { yields } T ( f ) \in \mathbb { H } \ \square \\$$

This equals the right side of (18.12). Choosing f = g yields T(f) ∈ H. □

To extend (18.10) to general f, g ∈ L2(Pη) we need two lemmas.

Lemma 18.4 The set G is dense in L2(Pη).


<!-- p:202 -->


Proof Let W be the space of all bounded measurable g: N → R that can be approximated in L2(Pη) by functions in G. This space is closed under monotone uniformly bounded convergence and under uniform convergence. Also it contains the constant functions. The space G is closed under multiplication. Let N' := σ(G) denote the σ-field generated by the elements of G. A functional version of the monotone class theorem (Theorem A.4) shows that W contains every bounded N'-measurable g. On the other hand, we have for each C ∈ X0 and each t ≥ 0 that μ → e−tμ(C) is in G so is N'-measurable, and therefore, since

$$\mu ( C ) = \lim _ { t \to 0 + } t ^ { - 1 } ( 1 - e ^ { - t \mu ( C ) } ) , \ \mu \in N ,$$

also μ → μ(C) is N′-measurable. Since λ is a σ-finite measure, for any C ∈ X there is a monotone sequence Ck ∈ X0, k ∈ N, with union C, so that μ → μ(C) is N′-measurable. Hence N ⊂ N′ and it follows that W contains all bounded measurable functions. Hence W is dense in L2(Pη) and the proof is complete. □

Lemma 18.5 Suppose that f, f1, f2, . . . ∈ L2(Pη) satisfy fk → f in L2(Pη) as k → ∞. Let n ∈ N and C ∈ X0. Then

$$\lim _ { k \to \infty } \int _ { C ^ { n } } \mathbb { E } [ | D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } f ( \eta ) - D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } f ^ { k } ( \eta ) | ] \, \lambda ^ { n } ( d ( x _ { 1 } , \dots , x _ { n } ) ) = 0 . \quad ( 1 8 . 1 3 )$$

Proof By (18.3) it suffices to prove that

$$\lim _ { n \to \infty } \int _ { C ^ { n } } \mathbb { E } \left [ \left | f ( \eta + \sum _ { i = 1 } ^ { m } \delta _ { x _ { i } } ) - f ^ { k } ( \eta + \sum _ { i = 1 } ^ { m } \delta _ { x _ { i } } ) \right | \right ] \lambda ^ { n } ( d ( x _ { 1 } , \dots , x _ { n } ) ) = 0 \ ( 1 8 . 1 4 )$$

for all m ∈ {0, ... , n}. For m = 0 this follows from Jensen's inequality. Suppose m ∈ {1, . . . , n}. By the multivariate Mecke equation (see (4.11)), the integral in (18.14) equals

$$\text {the integer in } ( 1 8 . 1 4 ) \text { equals} \\ \lambda ( C ) ^ { n - m } \mathbb { E } \left [ \int _ { C ^ { n } } \left | f ( \eta + \sum _ { i = 1 } ^ { m } \delta _ { x _ { i } } ) - f ^ { k } ( \eta + \sum _ { i = 1 } ^ { m } \delta _ { x _ { i } } ) \right | \lambda ^ { m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) \right ] \\ = \lambda ( C ) ^ { n - m } \mathbb { E } \left [ \int _ { C ^ { n } } | f ( \eta ) - f ^ { k } ( \eta ) | \eta ^ { ( m ) } ( d ( x _ { 1 } , \dots , x _ { m } ) ) \right ] \\ = \lambda ( C ) ^ { n - m } \mathbb { E } [ | f ( \eta ) - f ^ { k } ( \eta ) | \eta ^ { ( m ) } ( C ^ { m } ) ] . \\ \intertext { = } \lambda ( C ) ^ { n - m } \mathbb { E } [ | f ( \eta ) - f ^ { k } ( \eta ) | \eta ^ { ( m ) } ( C ^ { m } ) ] . \\ \intertext { B y t h e C a u c h y - S h w a r z e \, i n e q u a l l e t h e l a s t h o u n d e a b o v e h y }$$

By the Cauchy-Schwarz inequality the last is bounded above by

$$\lambda ( C ) ^ { n - m } ( \mathbb { E } [ ( f ( \eta ) - f ^ { k } ( \eta ) ) ^ { 2 } ] ) ^ { 1 / 2 } ( \mathbb { E } [ ( \eta ^ { ( m ) } ( C ^ { m } ) ) ^ { 2 } ] ) ^ { 1 / 2 } .$$

Since the Poisson distribution has moments of all orders, we obtain (18.14) and hence the lemma. □


<!-- p:203 -->


Theorem 18.6 (Fock space representation) The mapping f → (Tn(f))n≥0 is linear on L2(Pη) and takes values in H. Furthermore, we have

$$\mathbb { E } [ f ( \eta ) g ( \eta ) ] = ( \mathbb { E } [ f ( \eta ) ] ) ( \mathbb { E } [ g ( \eta ) ] ) + \sum _ { n = 1 } ^ { \infty } \frac { 1 } { n ! } \langle T _ { n } f , T _ { n } g \rangle _ { n } \\$$

for all f, g ∈ L2(Pη). In particular,

$$\mathbb { E } [ f ( \eta ) ^ { 2 } ] = ( \mathbb { E } [ f ( \eta ) ] ) ^ { 2 } + \sum _ { n = 1 } ^ { \infty } \frac { 1 } { n ! } \| T _ { n } f \| _ { n } ^ { 2 } .$$

Proof We first prove (18.16) for f ∈ L2(Pη). By Lemma 18.4 there exist fk ∈ G, defined for k ∈ N, satisfying fk → f in L2(Pη) as k → ∞. By Lemma 18.3, for k, l ∈ N we have

$$\langle T f ^ { k } - T f ^ { l } , T f ^ { k } - T f ^ { l } \rangle _ { \mathbf H } = \mathbb { E } [ ( f ^ { k } ( \eta ) - f ^ { l } ( \eta ) ) ^ { 2 } ]$$

so that T fk, k ∈ N, is a Cauchy sequence in H. Let f = (fn)n≥0 ∈ H be the limit, meaning that

$$\lim _ { k \to \infty } \sum _ { n = 0 } ^ { \infty } \frac { 1 } { n ! } \| T _ { n } f ^ { k } - \tilde { f } _ { n } \| _ { n } ^ { 2 } = 0 .$$

Taking the limit in the identity E[fk(η)2] = 〈T fk, T fk&gt;H yields E[f(η)2] = &lt;f, f&gt;H. Since fk → f ∈ L2(Pη), we have E[fk(η)] → E[f(η)] as k → ∞. H    ( = [( = If t  () b o show for all n ≥ 1 that

$$\tilde { f } _ { n } = T _ { n } f , \quad \lambda ^ { n } \text {-a.e.}$$

Let C ∈ X0 and, as in Section 4.3, let λ denote the restriction of the measure λn to Cn. By (18.17), then Tfk converges in L2(λ) (and hence in L1(λ)) to fn, while, by the definition (18.8) of Tn and (18.13), Tfk converges in L1(λ) to Tf. Hence these L1-limits must be the same almost everywhere, so that fn = Tf λn-a.e. on Cn. Since λ is assumed to be σfinite, this implies (18.18) and hence (18.16); in particular, T f ∈ H.

To see that T is linear, we take f, g ∈ L2(Pη) and a, b ∈ R. As above we can approximate f (resp. g) by a sequence fk ∈ G (resp. gk ∈ G), k ∈ N. Then afk + bgk → af + bg in L2(Pη) as k → ∞. Since T is linear on G (Lemma 18.3), we have T(afk + bgk) = aT(fk) + bT(gk) for all k ∈ N. In the first part of the proof we have shown that the left-hand side of this equation tends to T(af + bg), while the right-hand side tends to aT(f) + bT(g).

To prove (18.15) we can now use linearity, the polarisation identity

$$4 \langle u , v \rangle _ { \text {H} } = \langle u + v , u + v \rangle _ { \text {H} } - \langle u - v , u - v \rangle _ { \text {H} } , \quad u , v \in \text {H} ,$$


<!-- p:204 -->


and its counterpart in L2(Pη).

□

### 18.3 The Poincaré Inequality

ABde e e e oe ads e t o oe r  sper bound for the variance of functions of η in terms of the expected squared difference operator, known as the Poincaré inequality.

Theorem 18.7 Suppose f ∈ L2(Pη). Then

$$\mathbb { V } a r [ f ( \eta ) ] \leq \int \mathbb { E } [ ( D _ { x } f ( \eta ) ) ^ { 2 } ] \, \lambda ( d x ) .$$

Proof We can assume that the right-hand side of (18.19) is finite. In particular, Dxf ∈ L2(Pη) for λ-a.e. x. By (18.16),

$$\ t i c u l a r , D _ { x } f \in L ^ { 2 } ( \mathbb { P } _ { \eta } ) \text { for } \lambda \text {-a.e. } x . \text { By (18.16)} \\ \varvar[ f ( \eta ) ] = \int ( \mathbb { E } [ D _ { x } f ( \eta ) ] ) ^ { 2 } \, \lambda ( d x ) \\ + \sum _ { n = 2 } ^ { \infty } \frac { 1 } { n ! } \iint ( \mathbb { E } [ D _ { x _ { 1 } , \dots , x _ { n - 1 } } ^ { n - 1 } D _ { x } f ( \eta ) ] ) ^ { 2 } \\ \leq \int ( \mathbb { E } [ D _ { x } f ( \eta ) ] ) ^ { 2 } \, \lambda ( d x ) \\ + \sum _ { m = 1 } ^ { \infty } \frac { 1 } { m ! } \iint ( \mathbb { E } [ D _ { x _ { 1 } , \dots , x _ { m } } ^ { m } D _ { x } f ( \eta ) ] ) ^ { 2 } \\ \text {Applying (18.16) to } D _ { x } f \text { shows that the } \text {pr} \\$$

Applying (18.16) to Dxf shows that the preceding upper bound for the variance of f(η) is equal to ∫E[(Dxf(η))2] λ(dx), as required. □

The Poincaré inequality is sharp. Indeed, let f(μ) := μ(B) for B ∈ X with λ(B) &lt; ∞. Then Dxf(μ) = 1{x ∈ B} for all (x, μ) ∈ X × N and the right-hand side of (18.19) equals λ(B), the variance of F.

Later we shall need the following L1 version of the Poincaré inequality.

Corollary 18.8 Let f ∈ L1(Pη). Then

$$\mathbb { E } [ f ( \eta ) ^ { 2 } ] \leq ( \mathbb { E } [ f ( \eta ) ] ) ^ { 2 } + \int \mathbb { E } [ ( D _ { x } f ( \eta ) ) ^ { 2 } ] \, \lambda ( d x ) .$$

Proof Let r &gt; 0. Applying Theorem 18.7 with fr := (f ∧ r) ∨ (−r) gives

$$\mathbb { E } [ f _ { r } ( \eta ) ^ { 2 } ] \leq ( \mathbb { E } [ f _ { r } ( \eta ) ] ) ^ { 2 } + \int \mathbb { E } [ ( D _ { x } f ( \eta ) ^ { 2 } ) ] \, \lambda ( d x ) ,$$

where we have used Exercise 18.4. Monotone (resp. dominated) convergence applied to E[fr(η)2] (resp. to E[fr(η)]) yields the result. □


<!-- p:205 -->


### 18.4 Chaos Expansion

Let f ∈ L2(Pη). In this section we prove that

$$f ( \eta ) = \sum _ { n = 0 } ^ { \infty } \frac { 1 } { n ! } I _ { n } ( T _ { n } f ) , \quad \text {in} \ L ^ { 2 } ( \mathbb { P } ) , \quad ( 1 8 . 2 0 )$$

where the Wiener-Itô integrals I(·), n ∈ N, are defined in Definition 12.10 and I0(c) := c for each c ∈ R. This is known as the chaos expansion of f(η). The following special case is the key for the proof.

Lemma 18.9 Let f(μ) := e−μ(v), μ ∈ N, where v ∈ R+(X) and v vanishes outside a set B ∈ X0. Then (18.20) holds.

ro ()  s -  (1   m r lm als the formal sum

$$I \coloneqq \exp [ - \lambda ( 1 - e ^ { - v } ) ] + \exp [ - \lambda ( 1 - e ^ { - v } ) ] \sum _ { n = 1 } ^ { \infty } \frac { 1 } { n ! } I _ { n } ( ( e ^ { - v } - 1 ) ^ { \otimes n } ) . \ \ ( 1 8 . 2 1 )$$

Using the pathwise identity (12.12) we obtain that almost surely

$$Using the pathwise identity ( 1 2 . 1 2 ) \, we \, \text {obtain that almost surely} \\ I = \exp [ - \lambda ( 1 - e ^ { - v } ) ] \sum _ { n = 0 } ^ { \infty } \frac { 1 } { n ! } \sum _ { k = 0 } ^ { n } \binom { n } { k } \eta ^ { ( k ) } ( ( e ^ { - v } - 1 ) ^ { \otimes k } ) ( \lambda ( 1 - e ^ { - v } ) ) ^ { n - k } \\ = \exp [ - \lambda ( 1 - e ^ { - v } ) ] \sum _ { k = 0 } ^ { \infty } \frac { 1 } { k ! } \eta ^ { ( k ) } ( ( e ^ { - v } - 1 ) ^ { \otimes k } ) \sum _ { n = k } ^ { \infty } \frac { 1 } { ( n - k ) ! } ( \lambda ( 1 - e ^ { - v } ) ) ^ { n - k } \\ = \sum _ { k = 0 } ^ { N } \frac { 1 } { k ! } \eta ^ { ( k ) } ( ( e ^ { - v } - 1 ) ^ { \otimes k } ) , & & ( 1 8 . 2 2 ) \\ \text {where } N \colon = \eta ( B ) . \, \text {Assume now that } \eta \text { is proper and write } \delta _ { X _ { 1 } } + \cdots + \delta _ { X _ { n } } \text { for}$$

where N := η(B). Assume now that η is proper and write δx, + · · · + δx for the restriction of η to B. Then we have almost surely that

$$I = \sum _ { J \subset \{ 1 , \dots , N \} } \prod _ { i \in J } ( e ^ { - v ( X _ { i } ) } - 1 ) = \prod _ { i = 1 } ^ { N } e ^ { - v ( X _ { i } ) } = e ^ { - \eta ( v ) } ,$$

and hence (18.20) holds with almost sure convergence of the series. To demonstrate that convergence also holds in L2(P), let I(m) be the partial sum given by the right-hand side of (18.21) with the series terminated at n = m. Then since λ(1 − e−ν) is non-negative and |1 − e−v(y)| ≤ 1 for all y, a similar argument to (18.22) yields

$$| I ( m ) | \leq \sum _ { k = 0 } ^ { \min ( N , m ) } \frac { 1 } { k ! } | \eta ^ { ( k ) } ( ( e ^ { - v } - 1 ) ^ { \otimes k } ) | \leq \sum _ { k = 0 } ^ { N } \frac { ( N ) _ { k } } { k ! } = 2 ^ { N } .$$


<!-- p:206 -->


Since 2" has finite moments of all orders, by dominated convergence the (e a ( ((0) n ) (10) )

Since (18.20) concerns only the distribution of η, by Proposition 3.2 it has been no restriction of generality to assume that η is proper. □

Theorem 18.10 (Chaos expansion) Let f ∈ L2(Pη). Then (18.20) holds.

Proof By (12.19) and Theorem 18.6,

$$I h o b j & = B y \left ( 1 2 . 1 9 \right ) \, \text {and} \, \text {the} \, \text {one} \, \i m \, 1 8 . 0 , \\ & \sum _ { n = 0 } ^ { \infty } \mathbb { E } \left [ \left ( \frac { 1 } { n ! } I _ { n } ( T _ { n } f ) \right ) ^ { 2 } \right ] = \sum _ { n = 0 } ^ { \infty } \frac { 1 } { n ! } \| T _ { n } f \| _ { n } ^ { 2 } = \mathbb { E } [ f ( \eta ) ^ { 2 } ] < \infty . \\ U h o b j & = \underset { n } { \underset { n = 0 } { \ a n } } i f f i n t _ { n } \, \underset { n } { \ a n } \, \underset { n } { \ a n } \, \underset { n } { \ a n } \, S \underset { n } { \ a n } \, \underset { S } { \ a n } \, \underset { \underset { S } { \ a n } } { \ a n } \, \underset { \underset { S } { \ a n } } { \ a n } \, S ^ { \infty } \underset { \underset { S } { \ a n } } { \ a n } \, U ( T _ { n } \, f ) _ { n } \, \underset { S } { \ a n }$$

Hence the infinite series of orthogonal terms Sf := ∑n=0 n! In(Tnf) converges in L2(P). Let h ∈ G, where G was defined at (18.9). By Lemma 18.9 and linearity of In(·) the sum ∑=0 1In(Th) converges in L2(P) to h(η). Using (12.19) followed by Theorem 18.6 yields

$$\mathbb { E } [ ( h ( \eta ) - S _ { f } ) ^ { 2 } ] & = \sum _ { n = 0 } ^ { \infty } \frac { 1 } { ( n ! ) ^ { 2 } } \mathbb { E } [ ( I _ { n } ( T _ { n } h - T _ { n } f ) ) ^ { 2 } ] \\ & = \sum _ { n = 0 } ^ { \infty } \frac { 1 } { n ! } \| T _ { n } h - T _ { n } f \| _ { n } = \mathbb { E } [ ( f ( \eta ) - h ( \eta ) ) ] ^ { 2 } . \\ \text {Hence if } \mathbb { E } [ ( f ( n ) - h ( n ) ) ^ { 2 } ] \text { is small} \text { then so } \mathbb { E } [ ( f ( n ) - S _ { n } ) ^ { 2 } ] \text { Since } G \text { is} \\$$

Hence if E[(f(η) − h(η))2] is small, then so is E[(f(η) − Sf)2]. Since G is dense in L2(Pη) by Lemma 18.4, it follows from the Minkowski inequality that f(η) = Sf almost surely. □

### 18.5 Exercises

Exercise 18.1 Let v ∈ R(X) and define f ∈ R+(N) by f(μ) := ∫ v dμ if f |v| dμ &lt; ∞ and by f(μ) := 0 otherwise. Show for all x ∈ X and all μ ∈ N with μ(|v|) &lt; ∞ that Dxf(μ) = v(x) .

- Exercise 18.2 Let f, g ∈ R(N) and x ∈ X. Show that Dx(f g) = (Dxf)g + f(Dxg) + (Dxf)(Dxg).

Exercise 18.3 Let f, f : N → R be measurable functions such that f(η) = f(η) P-a.s. Show for all n ∈ N that

Dx,xnf(η) = Dx1,xnf(η), λ-a.e.(x1, .., ), P-a.s.

(Hint: Use the multivariate Mecke equation (4.11).)

Exercise 18.4 Let f ∈ R(N) and r ≥ 0. Define fr ∈ R(N) by fr := (f ∧ r) ∨ (−r). Show that |Dxfr(μ)| ≤ |Dxf(μ)| for each x ∈ X and μ ∈ N.


<!-- p:207 -->


Exercise 18.5 Let X = C(d) as in Example 18.1 and define the function f by (18.5). Let the measure λ be given by the right-hand side of (17.19) (with γ = 1), where Q is assumed to satisfy (17.10) and

$$\int ( \nu ( K + z ) ) ^ { 2 } \, d z \, \mathbb { Q } ( d K ) < \infty .$$

Show that f ∈ L2(Pη) and, moreover, that

$$T _ { n } f ( K _ { 1 } , \dots , K _ { n } ) = ( - 1 ) ^ { n + 1 } ( 1 - p ) \nu ( K _ { 1 } \cap \cdots \cap K _ { n } ) ,$$

where p = P(0 ∈ Z(η)) is the volume fraction of the Boolean model Z(η). Also show that (18.23) is implied by (17.21) whenever v(dx) = 1w(x)dx for some W ∈ Bd with λd(W) &lt; ∞.

Exercise 18.6 Let X = C(d) and let λ be as in Exercise 18.5. Let v1, v2 be two finite measures on Rd satisfying (18.23) and define, for i ∈ {1, 2}, f(μ) := v(Z(μ)), μ ∈ N; see (18.5). Use Fubini's theorem and Theorem 17.8 to prove that

$$\mathbb { C } o v ( f _ { 1 } ( \eta ) , f _ { 2 } ( \eta ) ) = ( 1 - p ) ^ { 2 } \iint ( e ^ { \beta _ { d } ( x _ { 1 } - x _ { 2 } ) } - 1 ) \, \nu _ { 1 } ( d x _ { 1 } ) \, \nu _ { 2 } ( d x _ { 2 } ) ,$$

where βd is given by (17.13). Confirm this result using Theorem 18.6 and Exercise 18.5.

Exercise 18.7 Let v ∈ L1(λ) ∩ L2(λ) and define the function f ∈ R(N) as in Exercise 18.1. Show that (18.19) is an equality in this case.

Exercise 18.8 Let f ∈ L2(Pη) and n ∈ N. Show that

$$\mathbb { W } [ f ( \eta ) ] \geq \int ( \mathbb { E } [ D _ { x _ { 1 } , \dots , x _ { n } } f ( \eta ) ] ) ^ { 2 } \, \lambda ^ { n } ( d ( x _ { 1 } , \dots , x _ { n } ) ) .$$

Exercise 18.9 Suppose that f ∈ L2(Pη) and gn ∈ L2(λn), n ∈ N0, such λn-a.e. for all n ∈ N. (Hint: Let n ∈ N and h ∈ L2(λn) and use Theorem 18.10 to show that E[f(η)I(h)] = n!(Tnf, h)n.)

Exercise 18.10 Let g ∈ L2(λ) and h ∈ L1(λ2) ∩ L2(λ2). Define F := ∫ g(x)I(hx) λ(dx), where hx := h(x, ·), x ∈ X. Prove that E[F] = 0 and

$$\mathbb { E } [ F ^ { 2 } ] = \int g ( x _ { 1 } ) g ( x _ { 2 } ) h ( x _ { 1 } , z ) h ( x _ { 2 } , z ) \, \lambda ^ { 3 } ( d ( x _ { 1 } , x _ { 2 } , z ) ) .$$

(Hint: Prove that E[ ∫ lg(x)I(hx)| λ(dx)] &lt; ∞ using the Cauchy-Schwarz inequality. Then use f(μ) = ∫ g(x)(μ(hx) − λ(hx)) λ(dx), μ ∈ N, as a representative of F and apply (18.16).)


<!-- p:208 -->


## Perturbation Analysis

The expectation of a function of a Poisson process can be viewed as a function of the intensity measure. Under first moment assumptions the (suitably defined) directional derivatives of this function can be expressed in terms of the difference operator. This can be applied to geometric functionals of a Boolean model Z with convex grains, governed by a Poisson process with intensity t ≥ 0. The expectation of an additive functional of the restriction of Z to a convex observation window (viewed as a function of t) satisfies a linear differential equation. As examples we derive explicit formulae for the expected surface content of a general Boolean model with convex grains and the expected Euler characteristic of a planar Boolean model with an isotropic grain distribution concentrated on convex sets.

### 19.1 A Perturbation Formula

In this chapter we consider an arbitrary measurable space (X, X) and a Poisson process ηλ on X with s-finite intensity measure λ. We study the effect of a perturbation of the intensity measure λ on the expectation of a fixed function of η.

To explain the idea we take a finite measure v on X, along with a bounded measurable function f : N(X) → R, and study the behaviour of E[f(ηλ+tv)] as t ↓ 0. Here and later, given any s-finite measure ρ on X, we let ηρ denote a Poisson process with this intensity measure. By the superposition theorem (Theorem 3.3) we can write E[f(ηλ+tv)] = E[f(ηλ + ηív)], where η′ν is a Poisson process with intensity measure tv, independent of ηλ. Then

$$\mathbb { E } [ f ( \eta _ { \lambda + \nu } ) ] \\ = \mathbb { E } [ f ( \eta _ { \lambda } ) ] \, \mathbb { P } ( \eta ^ { \prime } _ { \nu } ( \mathbb { X } ) = 0 ) + \mathbb { E } [ f ( \eta _ { \lambda } + \eta ^ { \prime } _ { \nu } ) \, | \, \eta ^ { \prime } _ { \nu } ( \mathbb { X } ) = 1 ] \, \mathbb { P } ( \eta ^ { \prime } _ { \nu } ( \mathbb { X } ) = 1 ) \\ + \mathbb { E } [ f ( \eta _ { \lambda } + \eta ^ { \prime } _ { \nu } ) \, | \, \eta ^ { \prime } _ { \nu } ( \mathbb { X } ) \geq 2 ] \, \mathbb { P } ( \eta ^ { \prime } _ { \nu } ( \mathbb { X } ) \geq 2 ) .$$

The measure ν can be written as ν = γ Q, where γ ∈ R+ and Q is a probability measure on X. Using Proposition 3.5 (and the independence of ηλ and η) to rewrite the second term in the expression on the right-hand side of the preceding equation, we obtain


<!-- p:209 -->


$$\mathbb { E } [ f ( \eta _ { \lambda + \nu } ) ] = e ^ { - t \gamma } \, \mathbb { E } [ f ( \eta _ { \lambda } ) ] + \gamma t e ^ { - t \gamma } \, \int \mathbb { E } [ f ( \eta _ { \lambda } + \delta _ { x } ) ] \, \mathbb { Q } ( d x ) + R _ { t } , \ \ ( 1 9 . 1 )$$

where

$$R _ { t } \colon = ( 1 - e ^ { - t \gamma } - \gamma t e ^ { - t \gamma } ) \mathbb { E } [ f ( \eta _ { \lambda } + \eta _ { t \nu } ^ { \prime } ) \, | \, \eta _ { t \nu } ^ { \prime } ( \mathbb { X } ) \geq 2 ] .$$

Since f is bounded, |R,| ≤ ct2 for some c &gt; 0 and it follows that

$$\lim _ { t \downarrow 0 } t ^ { - 1 } ( \mathbb { E } [ f ( \eta _ { \lambda + \nu } ) ] - \mathbb { E } [ f ( \eta _ { \lambda } ) ] ) = - \gamma \mathbb { E } [ f ( \eta _ { \lambda } ) ] + \gamma \int \mathbb { E } [ f ( \eta _ { \lambda } + \delta _ { x } ) ] \, \mathbb { Q } ( d x ) .$$

Therefore, the right derivative of E[f(ηλ+tv)] at t = 0 is given by

$$\frac { d ^ { + } } { d t } \mathbb { E } [ f ( \eta _ { \lambda + \nu } ) ] \Big | _ { t = 0 } = \int \mathbb { E } [ D _ { x } f ( \eta _ { \lambda } ) ] \, \nu ( d x ) .$$

The following results elaborate on (19.2). Recall from Theorem A.9 the Hahn-Jordan decomposition ν = v+ − v\_ of a finite signed measure v on X. We also recall from Section A.1 that the integral ∫ f dv is defined as ∫ f dv+ – ∫ f dv\_, whenever this makes sense. Given a finite signed measure ν, we denote by I(λ, v) the set of all t ∈ R such that λ + tv is a measure. Then 0 ∈ I(λ, ν) and it is easy to see that I(λ, ν) is a (possibly infinite) closed interval. We abbreviate N := N(X).

Theorem 19.1 (Perturbation formula) Let v be a finite signed measure on X such that I(λ, v) ≠ {0} and suppose that f ∈ R(N) is bounded. Then t → E[f(ηλ+tv)] is infinitely differentiable on I(λ, v) and, for n ∈ N,

$$\frac { d ^ { n } } { d t ^ { n } } \mathbb { E } [ f ( \eta _ { \lambda + t \nu } ) ] = \int \mathbb { E } [ D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } f ( \eta _ { \lambda + t \nu } ) ] \, \nu ^ { \nu } ( d ( x _ { 1 } , \dots , x _ { n } ) ) , \quad t \in I ( \lambda , \nu ) .$$

(For t in the boundary of I(λ, v) these are one-sided derivatives.)

Proof We start by proving the case n = 1, that is

$$\frac { d } { d t } \mathbb { E } [ f ( \eta _ { \lambda + t \nu } ) ] = \int \mathbb { E } [ D _ { x } f ( \eta _ { \lambda + t \nu } ) ] \, \nu ( d x ) , \ \ t \in I ( \lambda , \nu ) .$$

We first assume that v is a measure. It is enough to prove (19.4) for t = 0 since then for general t ∈ I(λ, v) we can apply this formula with λ replaced by λ + tv. Assume that −s ∈ I(λ, v) for all sufficiently small s &gt; 0. For such s we let η'sy be a Poisson process with intensity measure sv, independent of ηλ-sv. By the superposition theorem (Theorem 3.3) we can then assume without loss of generality that ηλ = ηλ-sv + η'sy. Then it follows exactly as at (19.1) that


<!-- p:210 -->


$$\mathbb { E } [ f ( \eta _ { \lambda } ) ] = e ^ { - s \gamma } \mathbb { E } [ f ( \eta _ { \lambda - s \nu } ) ] + \gamma s e ^ { - s \gamma } \int \mathbb { E } [ f ( \eta _ { \lambda - s \nu } + \delta _ { x } ) ] \, \mathbb { Q } ( d x ) + R _ { s } ,$$

where |Rs| ≤ cs2 for some c &gt; 0. Therefore

$$- s ^ { - 1 } ( \mathbb { E } [ f ( \eta _ { \lambda - s \nu } ) ] - \mathbb { E } [ f ( \eta _ { \lambda } ) ] ) & = s ^ { - 1 } ( e ^ { - s \gamma } - 1 ) \mathbb { E } [ f ( \eta _ { \lambda - s \nu } ) ] \\ & + \gamma e ^ { - s \gamma } \int \mathbb { E } [ f ( \eta _ { \lambda - s \nu } + \delta _ { x } ) ] \, \mathbb { Q } ( d x ) + s ^ { - 1 } R _ { s } .$$

Since v is a finite measure

$$\mathbb { P } ( \eta _ { \lambda } \neq \eta _ { \lambda - s \nu } ) = \mathbb { P } ( \eta _ { s \nu } ^ { \prime } \neq 0 ) \to 0$$

as s ↓ 0. Since f is bounded it follows that E[f(ηλ–sv)] → E[f(ηλ)] as s ↓ 0. Similarly E[f(ηλ−sv +δx)] tends to E[f(ηλ +δx)] for all x ∈ X. By dominated convergence, even the integrals with respect to Q converge. By (19.5), the left derivative of E[f(ηλ+tv)] at t = 0 coincides with the right-hand side of (19.2). Hence (19.4) follows.

By dominated convergence the right-hand side of (19.4) is a continuous function of t ∈ I(λ, v). Therefore we obtain from the fundamental theorem of calculus for each t ∈ I(λ, v) that

$$\mathbb { E } [ f ( \eta _ { \lambda + t \nu } ) ] = \mathbb { E } [ f ( \eta _ { \lambda } ) ] + \int _ { 0 } ^ { t } \int _ { \mathbb { X } } \mathbb { E } [ D _ { x } f ( \eta _ { \lambda + s \nu } ) ] \, \nu ( d x ) \, d s ,$$

where we use the convention ∫ := – fo for t &lt; 0.

We now consider the case where v = ν+ – v\_ is a general finite signed measure. Suppose first that a ∈ I(λ, v) for some a &gt; 0. Then, by (19.6), for 0 ≤ t ≤ a we have

$$\mathbb { E } [ f ( \eta _ { \lambda } ) ] - \mathbb { E } [ f ( \eta _ { \lambda - \nu _ { - } } ) ] = \int _ { 0 } ^ { \tau } \int _ { \mathbb { X } } \mathbb { E } [ D _ { x } f ( \eta _ { \lambda + ( u - t ) \nu _ { - } } ) ] \, \nu _ { - } ( d x ) \, d u \quad$$

and

$$\mathbb { E } [ f ( \eta _ { \lambda - \nu _ { - } + \nu _ { + } } ) ] - \mathbb { E } [ f ( \eta _ { \lambda - \nu _ { - } } ) ] = \int _ { 0 } ^ { t } \int _ { \mathcal { K } } \mathbb { E } [ D _ { x } f ( \eta _ { \lambda - \nu _ { - } + \nu _ { + } } ) ] \, \nu _ { + } ( d x ) \, d u .$$

For s ≥ 0, let η be a Poisson process with intensity measure sv\_ independent of ηλ-sv\_. By the superposition theorem we can assume for all s ≥ 0


<!-- p:211 -->


that ηλ = ηλ–sv + η5 . Then it follows as before that

$$\mathbb { P } ( \eta _ { \lambda } \neq \eta _ { \lambda = s \nu _ { - } } ) = \mathbb { P } ( \eta _ { s } ^ { - } \neq 0 ) \to 0$$

as s ↓ 0, since v\_ is a finite measure. Since also f is bounded we have E[Dxf(ηλ−sv\_)] → E[Dxf(ηλ)] as s ↓ 0, so the right-hand side of (19.7) is asymptotic to t ∫ E[Dxf(ηλ)] ν\_(dx) as t ↓ 0. Similarly we have that E[f(ηλ-tv\_+uv+)] − E[f(ηλ-tv\_)] → 0 as t, u ↓ 0, so the right-hand side of (19.8) is asymptotic to t ∫ EDxf(ηλ) ν+(dx) as t ↓ 0. Then we can deduce (19.2) from (19.7) and (19.8).

If λ – av is a measure for some a &gt; 0, then applying the same argument with −v instead of ν gives the differentiability at t = 0 of E[f(ηλ+tv)]. For an arbitrary t ∈ I(λ, v) we can apply this result to the measure λ + tv (instead of λ) to obtain (19.4).

We can now prove (19.3) by induction. Assume that t → E[f(ηλ+tv)] is n times differentiable on I(λ, v) for each bounded f ∈ R(N). For a given f we apply (19.4) to the bounded function g ∈ R(N) defined by

$$g ( \mu ) \coloneqq \int D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } f ( \mu ) \nu ^ { n } ( d ( x _ { 1 } , \dots , x _ { n } ) ) , \quad \mu \in \mathbf N .$$

By linearity of integration we have for each x ∈ X that

$$D _ { x } g ( \mu ) = \int D _ { x _ { 1 } , } ^ { n + }$$

so that we can conclude the proof from Fubini's theorem.

□

### 19.2 Power Series Representation

Given an interval I ⊂ R containing the origin, we say that a function f : I → R has a power series representation (on I) if there is a sequence an ∈ R, n ∈ N, such that f(t) = ∑n=0 antn for each t ∈ I. In this section we show that t → E[f(ηλ+tv)] has this property under certain assumptions on the function f, the measure λ and the finite signed measure v.

Theorem 19.2 Suppose that the assumptions of Theorem 19.1 hold. Then

$$\mathbb { E } [ f ( \eta _ { \lambda + \nu } ) ] = \sum _ { n = 0 } ^ { \infty } \frac { t ^ { n } } { n ! } \int \mathbb { E } [ D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } f ( \eta _ { \lambda } ) ] \, \nu ^ { n } ( d ( x _ { 1 } , \dots , x _ { n } ) )$$

for all t ∈ I(λ, v), where for n = 0 the summand is interpreted as E[f(ηλ)].


<!-- p:212 -->


Proof By Theorem 19.1 and Taylor's theorem we have for each t ∈ I(λ, v) and each m ∈ N that

$$\mathbb { E } [ f ( \eta _ { \lambda + t \nu } ) ] = \sum _ { n = 0 } ^ { m } \frac { t ^ { n } } { n ! } \int \mathbb { E } [ D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } f ( \eta _ { \lambda } ) ] \, \nu ^ { n } ( d ( x _ { 1 } , \dots , x _ { n } ) ) + R _ { m } ( t ) ,$$

where |R(t)| ≤ (ν+(X) + ν\_(X))c2m+1|t|m+1 /(m + 1)!, with c being an upper bound of |f|. The result follows. □

The preceding result required the function f to be bounded. For some applications in stochastic geometry this assumption is too strong. The following results apply to more general functions. For a finite signed measure ν with Hahn–Jordan decomposition ν = ν+ − ν\_ we denote by |ν| = ν+ + ν\_ the total variation measure of v.

Theorem 19.3 Let v be a finite signed measure on X. Suppose that f ∈ R(N) and t ∈ I(λ, ν) satisfy E[|f(ηλ+|t|)|] &lt; ∞. Then

$$\sum _ { n = 0 } ^ { \infty } \frac { | t | ^ { n } } { n ! } \int \mathbb { E } [ | D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } f ( \eta _ { \lambda } ) | \, | \nu | ^ { n } ( d ( x _ { 1 } , \dots , x _ { n } ) ) < \infty$$

and (19.9) holds.

Proof It suffices to treat the case t = 1, since then we could replace v with tν. For all k ∈ N we define a bounded function fk := (f ∧ k) ∨ (−k) ∈ R(N), as in Exercise 18.4. By Theorem 19.2,

$$\mathbb { E } [ f _ { k } ( \eta _ { \lambda + \nu } ) ] = \sum _ { n = 0 } ^ { \infty } \frac { 1 } { n ! } \int \mathbb { E } [ D ^ { n } f _ { k } ( \eta _ { \lambda } ) ] \left ( h _ { + } - h _ { - } \right ) ^ { \otimes n } d | \nu | ^ { n } ,$$

where h\_ (resp. h+) is a Radon–Nikodým derivative of ν\_ (resp. ν+) with respect to |v| = ν\_ + ν+ (see Theorem A.10) and where we recall the definition (18.6) of (h+ − h\_)®n. Since ν− ≤ |ν| and ν+ ≤ |ν| we have that h\_(x) ≤ 1 and h+(x) ≤ 1 for |v|-a.e. x. Since v\_ and v+ are mutually singular we also have h\_(x)h+(x) = 0 for |v|-a.e. x. Therefore,

$$| ( h _ { + } ( x ) - h _ { - } ( x ) ) | = h _ { + } ( x ) + h _ { - } ( x ) = 1 , \quad | \nu | \text {-a.e.} \ x \in \mathbb { X } .$$

Now let k → ∞ in (19.11). By Exercise 3.8 we have E[l.f(ηλ)|] &lt; ∞. Dominated convergence shows that the left-hand side of (19.11) tends to E[f(ηλ+v)]. Also Dx,,.x k(ηλ) tends to Dx,.,xf(ηλ) for all n ∈ N0, alll x1, . . . , xn ∈ X and everywhere on Ω. Furthermore, by (18.3),

$$| D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } f _ { k } ( \eta _ { \lambda } ) | \leq \sum _ { J \subset \{ 1 , \dots , n \} } \left | f ( \eta _ { \lambda } + \sum _ { j \in J } \delta _ { x _ { j } } ) \right | .$$


<!-- p:213 -->


We shall show that

$$I \colon = \sum _ { n = 0 } ^ { \infty } \frac { 1 } { n ! } \int \mathbb { E } \left [ \sum _ { J \subset \{ 1 , \dots , n \} } \left | f \left ( \eta _ { \lambda } + \sum _ { j \in J } \delta _ { x _ { j } } \right ) \right | \right ] | \right |$$

so that (19.10) follows. Moreover, we can then deduce (19.9) from (19.11) and dominated convergence.

By symmetry, I equals

$$\sum _ { n = 0 } ^ { \infty } \frac { 1 } { n ! } \sum _ { m = 0 } ^ { n } \binom { n } { m } | \nu | ( \mathbb { K } ) ^ { n - m } \int \mathbb { E } [ | f ( \eta _ { \lambda } + \delta _ { x _ { 1 } } + \cdots + \delta _ { x _ { m } } ) | ] \, | \nu | ^ { m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) .$$

Swapping the order of summation yields that I equals

$$\exp [ | \nu | ( \mathbb { X } ) ] \sum _ { m = 0 } ^ { \infty } \frac { 1 } { m ! } \int \mathbb { E } [ | f ( \eta _ { \lambda } + \delta _ { x _ { 1 } } + \cdots + \delta _ { x _ { m } } ) | \, | \nu | ^ { m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) \\ = \exp [ 2 | \nu | ( \mathbb { X } ) ] \, \mathbb { E } [ | f ( \eta _ { \lambda } + \eta _ { | \nu | } ^ { \prime } ) | ] ,$$

where ηγ, is a Poisson process with intensity measure |v|, independent of ηλ, and where we have used Exercise 3.7 (or Proposition 3.5) to achieve the equality. By the superposition theorem (Theorem 3.3) we obtain

$$I = \exp [ 2 | \nu | ( \mathbb { X } ) ] \, \mathbb { E } [ | f ( \eta _ { \lambda + | \nu | } ) | ] ,$$

which is finite by assumption.

□

For f ∈ R(N) and v a finite signed measure on X we let If(λ, ν) denote the set of all t ∈ I(λ, ν) such that E[|f(ηλ+|z|)|] &lt; ∞. If If(λ, v) ≠ ∅ then Exercise 3.8 shows that I(λ, v) is an interval containing 0. Using Theorem 19.3 we can generalise (19.3) to potentially unbounded functions f.

Theorem 19.4 Let v be a finite signed measure on X and let f ∈ R(N). Then the function t → E[f(ηλ+tv)] is infinitely differentiable on the interior I0 of If(λ, v) and, for all n ∈ N and t ∈ I0,

$$\frac { d ^ { n } } { d t ^ { n } } \mathbb { E } [ f ( \eta _ { \lambda + \nu } ) ] = \int \mathbb { E } [ D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } f ( \eta _ { \lambda + \nu } ) ] \, \nu ^ { n } ( d ( x _ { 1 } , \dots , x _ { n } ) ) .$$

Proof The asserted differentiability is a consequence of (19.9) and wellknown properties of power series. The same is true for (19.3) in the case t = 0. For general t ∈ I0 we can apply this formula with λ replaced by λ + tv. □


<!-- p:214 -->


### 19.3 Additive Functions of the Boolean Model

As an application of the perturbation formulae, consider the Boolean model in Rd, as in Definition 17.1. Let ηt be a stationary Poisson process on Rd with intensity t ≥ 0 and let Q be a grain distribution satisfying (17.10). Recall that C(d) = Ca \ {0} is the system of all non-empty compact subsets of Rd equipped with the Hausdorff distance (17.1). We assume that Q is concentrated on the system K(d) of all convex K ∈ C(d). Let ξt be an independent Q-marking of ηt and define

$$Z _ { t } \coloneqq \bigcup _ { ( K , x ) \in \xi _ { t } } ( K + x ) .$$

Given compact W C Rd, Proposition 17.5 and Lemma A.30 show that Z ∩ W is a random element of Ca. In fact, by Exercise 17.1 we can assume without loss of generality that for all ω ∈ Ω and all compact convex W ⊂ Rd the set Z,(ω) ∩ W is a finite (possibly empty) union of convex sets. We define the convex ring Ra to be the system of all such unions. By Theorem A.26, Rd is a Borel subset of Ca. Therefore, Z, ∩ W is a random element of Rd, whenever W is a compact convex set.

A measurable function φ: Rd → R is said to be locally finite if

$$\sup \{ | \varphi ( K ) | \colon K \in \mathcal { K } ^ { d } , K \subset W \} < \infty , \quad W \in \mathcal { K } ^ { d } .$$

Recall that a function φ: Rd → R is said to be additive if φ(∅) = 0 and φ(K ∪ L) = φ(K) + φ(L) − φ(K ∩ L) for all K, L ∈ Rd.

Proposition 19.5 Let φ: Rd → R be measurable, additive and locally finite. For W ∈ Kd let S φ,w(t) := E[φ(Zt ∩ W)]. Then S φ,w(·) has a power series representation on R, and the derivative is given by

$$( 1 9 . 1 5 )$$

Proof We aim to apply Theorem 19.4 with

$$\mathbb { X } \coloneqq \{ ( x , K ) \in \mathbb { R } ^ { d } \times \mathcal { K } ^ { ( d ) } \colon ( K + x ) \cap W \neq \emptyset \} ,$$

λ = 0 and ν the restriction of λd ⊗ Q to X. By assumption (17.10) and (16.11), this measure is finite. Define the function f : N(X) → R+ by

$$f ( \mu ) \colon = \varphi ( Z ( \mu ) \cap W ) ,$$

where Z(μ) := ∪(x,K)∈μ(K + x) if μ(X) &lt; ∞ and Z(μ) := ∅ otherwise.


<!-- p:215 -->


By Theorem A.26 the space C(d) is a CSMS and, by Lemma A.24, so is Rd × C(d). Hence Proposition 6.2 applies and it follows as in Proposition 17.5 that μ → Z(μ) is a measurable mapping taking values in the convex ring Rd. Since φ is a measurable function, so is f. To show that E[f(ηtv)] &lt; ∞, we write ηt in the form

$$\eta _ { t \nu } = \sum _ { n = 1 } ^ { K } \delta _ { ( X _ { n } , Z _ { n } ^ { \prime } ) } ,$$

where κ is Poisson distributed with parameter λ(X), (X) is a sequence of random vectors in Rd and (Zn) is a sequence of random elements of K(a). Let Yn := Z′ + Xn. By the inclusion-exclusion principle (A.30),

$$f ( \eta _ { \nu } ) & = f \left ( \bigcup _ { n = 1 } ^ { \kappa } Y _ { n } \cap W \right ) \\ & = \sum _ { n = 1 } ^ { \kappa } ( - 1 ) ^ { n - 1 } \sum _ { 1 \leq i _ { 1 } < \cdots < i _ { n } \leq \kappa } \varphi ( W \cap Y _ { i _ { 1 } } \cdots \cap Y _ { i _ { n } } ) .$$

Using (19.14) we get

$$| f ( \eta _ { t v } ) | \leq \sum _ { n = 1 } ^ { \kappa } \binom { \kappa } { n } c _ { W } \leq 2 ^ { \kappa } c _ { W } ,$$

where cw is the supremum in (19.14). It follows that E[lf(ηv)|] &lt; ∞.

By Theorem 19.3 the function Sφ,w(·) has a power series representation on R+. By Theorem 19.4 the derivative is given by

$$S _ { \varphi , w } ^ { \prime } ( t ) = \iint \mathbb { E } [ D _ { ( x , K ) } f ( \eta _ { t \nu } ) ] \, d x \, \mathbb { Q } ( d K ) \\$$

From the additivity property (A.29) and linearity of integrals we obtain (19.15), provided that

$$\iint ( | \varphi ( W \cap ( K + x ) ) | + \mathbb { E } [ | \varphi ( Z _ { t } \cap W \cap ( K + x ) ) | ] ) \, d x \, \mathbb { Q } ( d K ) < \infty .$$

Since φ(0) = 0, we have

$$\iint | \varphi ( W \cap ( K + x ) ) | \, d x \, \mathbb { Q } ( d K ) \leq c _ { W } \iint 1 \{ W \cap ( K + x ) \neq \emptyset \} \, d x \, \mathbb { Q } ( d K ) ,$$

which is finite by (17.7) and assumption (17.10). Using (19.16) with W


<!-- p:216 -->


e [  [x + )     (x +    mnly in (K, x) ∈ Kd ×Rd. Hence we obtain as before that

$$\iint \mathbb { E } [ | \varphi ( Z _ { t } \cap W \cap ( K + x ) ) | ] \, d x \, \mathbb { Q } ( d K ) \\ \leq c _ { W } \mathbb { E } [ 2 ^ { x } ] \iint 1 \{ W \cap ( K + x ) \neq \emptyset \} \, d x \, \mathbb { Q } ( d K ) < \infty ,$$

and the proposition is proved.

□

Sometimes the right-hand side of (19.15) satisfies the assumptions of the following theorem.

Theorem 19.6 Let m ∈ N. For j ∈ {1, .. . , m} let ψj: Rd → R be a measurable, additive and locally finite function. For W ∈ Kd let S j,w(t) := E[ψ (Zt ∩ W)]. Suppose that

$$d K ) = \sum _ { j = 1 } ^ { m } c _ { j } \psi _ { j } ( A ) , \quad A \in \mathcal { R } ^ { d } , \quad ( 1 9 . 1 7 )$$

for certain constants cj ∈ R depending on Q but not on A. Then S 1,w is a differentiable function satisfying

$$S _ { 1 , W } ^ { \prime } ( t ) = \sum _ { j = 1 } ^ { m } c _ { j } \psi _ { j } ( W ) - \sum _ { j = 1 } ^ { m } c _ { j } S _ { j , W } ( t ) .$$

Proof Applying (19.15) with φ = ψ1 and using (19.17) twice (the second time with Z, ∩ W in place of W), we obtain

$$S _ { 1 , W } ^ { \prime } ( t ) = \sum _ { j = 1 } ^ { m } c _ { j } \psi _ { j } ( W ) - \mathbb { B } \left [ \sum _ { j = 1 } ^ { m } c _ { j } \psi _ { j } ( Z _ { t } \cap W ) \right ] ,$$

where we have also used Fubini's theorem. This yields the assertion.

□

Now we consider the intrinsic volumes Vi: Rd → R, i ∈ {0, . . . , d}, as defined in Section A.3. As mentioned after (A.26) these functionals are increasing on Ka with respect to set inclusion; therefore they are locally finite. The distribution Q is said to be isotropic if Q({ρK : K ∈ A}) = Q(A) for all measurable A ⊂ K(d) and (proper) rotations ρ: Rd → Rd, where ρK := {ρ(x) : x ∈ K}. If Q is isotropic then there are coefficients ci,j ∈ R (for i, j ∈ {0, . . . , d}) such that for each i ∈ {0, . . . , d}

$$d K ) = \sum _ { j = 0 } ^ { d } c _ { i , j } V _ { j } ( A ) , \ \ A \in \mathcal { R } ^ { d } . \quad ( 1 9 . 1 9 )$$


<!-- p:217 -->


This can be established with Hadwiger's characterisation theorem (Theorem A.25), just as in the special case i = 0 in the forthcoming proof of Theorem 19.8. In fact, for i ∈ {d – 1, d} isotropy is not needed; see (22.11) for the case i = d and (A.24) for the case i = d − 1. Moreover, it is possible to show that ci,j = 0 for i &gt; j. Now, Theorem 19.6 shows for W ∈ Kd and i ∈ {0, . . . , d} that

$$\frac { d } { d t } \mathbb { E } [ V _ { i } ( Z _ { t } \cap W ) ] & = \sum _ { j = 0 } ^ { d } c _ { i , j } V _ { j } ( W ) - \sum _ { j = 0 } ^ { d } c _ { i , j } \mathbb { E } [ V _ { j } ( Z _ { t } \cap W ) ] , \quad t \geq 0 , \\$$

which is a system of linear differential equations. Using methods from integral geometry it is possible to determine the coefficients cj. We shall not pursue this general case any further. In the following two sections we shall instead discuss the (simple) case i = d – 1 (without isotropy assumption) and the case i = 0 for isotropic planar Boolean models.

### 19.4 Surface Density of the Boolean Model

In this section we shall give a formula for the surface density

$$S _ { W } ( t ) \colon = \mathbb { E } [ V _ { d - 1 } ( Z _ { t } \cap W ) ] , \ \ t \geq 0 ,$$

where W ∈ Ka and where we refer to (A.23) for a geometric interpretation. It turns out that S w(t) can be easily expressed in terms of φd and φd–1, where as in (17.11) we define φi := ∫ V(K) Q(dK) for i ∈ {0, . . . , d}.

Theorem 19.7 Let Zt be as in (19.13) and let W ∈ Kd. Then

$$S _ { W } ( t ) = \phi _ { d - 1 } t e ^ { - t \phi _ { d } } V _ { d } ( W ) + ( 1 - e ^ { - t \phi _ { d } } ) V _ { d - 1 } ( W ) , \quad t \geq 0 .$$

Proof By Proposition 19.5 and (A.24),

$$S _ { W } ^ { \prime } ( t ) & = \int V _ { d } ( W ) V _ { d - 1 } ( K ) \mathbb { Q } ( d K ) + \int V _ { d - 1 } ( W ) V _ { d } ( K ) \mathbb { Q } ( d K ) \\ & - \int \mathbb { E } [ V _ { d } ( Z _ { t } \cap W ) ] V _ { d - 1 } ( K ) \mathbb { Q } ( d K ) \\ & - \int \mathbb { E } [ V _ { d - 1 } ( Z _ { t } \cap W ) ] V _ { d } ( K ) \mathbb { Q } ( d K ) .$$

By Proposition 17.4 we have for all t ≥ 0 that

$$\mathbb { E } [ V _ { d } ( Z _ { t } \cap W ) ] = ( 1 - e ^ { - t \phi _ { d } } ) V _ { d } ( W ) ,$$

and therefore

$$S _ { w } ^ { \prime } ( t ) = V _ { d } ( W ) \phi _ { d - 1 } + V _ { d - 1 } ( W ) \phi _ { d } - ( 1 - e ^ { - t \phi _ { d } } ) V _ { d } ( W ) \phi _ { d - 1 } - S _ { w } ( t ) \phi _ { d } .$$


<!-- p:218 -->


Note that S w(0) = 0. It is easily checked that this linear differential equation is (uniquely) solved by the right-hand side of the asserted formula (19.20). □

The right-hand side of (19.20) admits a clear geometric interpretation. The first term is the mean surface content in W of all grains that are not covered by other grains. Indeed, φa-1tVa(W) is the mean surface content of all grains ignoring overlapping, while e-tφd can be interpreted as the probability that a point on the boundary of a contributing grain is not covered by other grains; see (19.21). The second term is the contribution of that part of the boundary of W which is covered by the Boolean model.

### 19.5 Mean Euler Characteristic of a Planar Boolean Model

Finally in this chapter we deal with the Euler characteristic V0 in the case d = 2; see Section A.3 for the definition and a geometric interpretation.

Theorem 19.8 Let Z be a Boolean model in R2 with intensity t ≥ 0 and with an isotropic grain distribution Q concentrated on K(2) and satisfying (17.10). Then, for all W ∈ K2,

$$\mathbb { E } [ V _ { 0 } ( Z _ { t } \cap W ) ] & = ( 1 - e ^ { - t \phi _ { 2 } } ) V _ { 0 } ( W ) \\ & + \frac { 2 } { \pi } t e ^ { - t \phi _ { 2 } } \phi _ { 1 } V _ { 1 } ( W ) + t e ^ { - t \phi _ { 2 } } V _ { 2 } ( W ) - \frac { 1 } { \pi } t ^ { 2 } e ^ { - t \phi _ { 2 } } \phi _ { 1 } ^ { 2 } V _ { 2 } ( W ) . \quad ( 1 9 . 2 2 ) \\$$

Proof In the first part of the proof we work in general dimensions. We plan to apply Theorem 19.6 to the intrinsic volumes V0, . . . , Va. To do so, we need to establish (19.17), that is

$$d K ) = \sum _ { j = 0 } ^ { d } c _ { j } V _ { j } ( A ) , \quad A \in \mathcal { R } ^ { d } , \quad ( 1 9 . 2 3 )$$

for certain constants c0, . .. , cd ∈ R. Since both sides of this equation are additive in A, we can by (A.30) assume that A ∈ Kd. Then the left-hand side of (19.23) simplifies to

$$\varphi ( A ) \colon = \iint 1 \{ A \cap ( K + x ) \neq \emptyset \} \, d x \, \mathbb { Q } ( d K ) = \int V _ { d } ( K \oplus A ^ { * } ) \, \mathbb { Q } ( d K ) ,$$

where we recall that A* := {−x : x ∈ A}. By Exercise 19.7 the function φ is invariant under translations and rotations. We now prove that φ is continuous on K(d) (with respect to Hausdorff distance). If A ∈ K(d) converge to some A ∈ K(d), then (A)* converges to A*. Hence, for any K ∈ K(d), by Exercise 17.6 the sets K ⊕ (A)* converge to K ⊕ A*, so that the continuity of Vd on K(d) (mentioned in Section A.3) shows that Vd(K ⊕ (A)*) tends to Vd(K ⊕ A*). Moreover, the definition of Hausdorff distance implies that the A are all contained in some (sufficiently large) ball. By assumption (17.10) we can apply dominated convergence to conclude that φ(A) → φ(A) as n → ∞.


<!-- p:219 -->


Hadwiger's characterisation (Theorem A.25) shows that (19.23) holds. To determine the coefficients c0, . . . , cd we take A = B(0, r) for r ≥ 0. The Steiner formula (A.22) and the definition (17.11) of φ show that

$$\varphi ( B ( 0 , r ) ) = \sum _ { j = 0 } ^ { d } r ^ { j } \kappa _ { j } \int V _ { d - j } ( K ) \, \mathbb { Q } ( d K ) = \sum _ { j = 0 } ^ { d } r ^ { j } \kappa _ { j } \phi _ { d - j } .$$

On the other hand, by (A.25) and (A.26), for A = B(0, r) the right-hand side of (19.23) equals

$$\sum _ { j = 0 } ^ { d } c _ { j } r ^ { j } \binom { d } { j } \frac { \kappa _ { d } } { \kappa _ { d - j } } ,$$

where we recall that κ0 = 1. It follows that

$$c _ { j } = \phi _ { d - j } \frac { j ! \kappa _ { j } ( d - j ) ! \kappa _ { d - j } } { d ! \kappa _ { d } } , \ \ j = 0 , \dots , d .$$

In the remainder of the proof we assume that d = 2. Then (19.23) reads

$$\iint V _ { 0 } ( A \cap ( K + x ) ) \, d x \, \mathbb { Q } ( d K _ { 2 } ) = \phi _ { 2 } V _ { 0 } ( A ) + \frac { 2 \phi _ { 1 } } { \pi } V _ { 1 } ( A ) + V _ { 2 } ( A ) , \ ( 1 9 . 2 5 )$$

for each A ∈ R2. Inserting (19.20) and (19.21) into (19.18) yields

$$\frac { d } { d t } \mathbb { E } [ V _ { 0 } ( Z _ { t } \cap W ) ] = & \sum _ { j = 0 } ^ { 2 } c _ { j } V _ { j } ( W ) - c _ { 0 } \mathbb { E } [ V _ { 0 } ( Z _ { t } \cap W ) ] - c _ { 1 } \phi _ { 1 } t e ^ { - t \phi _ { 2 } } V _ { 2 } ( W ) \\ & - c _ { 1 } ( 1 - e ^ { - t \phi _ { 2 } } ) V _ { 1 } ( W ) - c _ { 2 } ( 1 - e ^ { - t \phi _ { 2 } } ) V _ { 2 } ( W ) .$$

A simple calculation shows that this differential equation is indeed solved by the right-hand side of (19.22). □

### 19.6 Exercises

Exercise 19.1 Let λ be an s-finite measure on X and v a finite measure on X. Suppose that f ∈ R(N) satisfies E[|f(ηλ+t|γ|)|] &lt; ∞ for some t &gt; 0. Prove by a direct calculation that (19.9) holds. (Hint: Use the calculation in the proof of Theorem 19.3.)


<!-- p:220 -->


Exercise 19.2 Let ν be a finite measure on X and let f ∈ R(N) satisfy E[|.f(ηav)|] &lt; ∞ for some a &gt; 0. Show that

$$\frac { d } { d t } \mathbb { E } [ f ( \eta _ { \nu } ) ] = t ^ { - 1 } \mathbb { E } \int ( f ( \eta _ { \nu } ) - f ( \eta _ { \nu } \vee \delta _ { x } ) ) \, \eta _ { \nu } ( d x ) , \quad t \in [ 0 , a ] .$$

Exercise 19.3 Let v be a finite measure on X and let A ∈ N be increasing, that is μ ∈ A implies μ + δx ∈ A for all x ∈ X. Let

$$N _ { A } ( t ) \colon = \int \mathbf 1 \{ \eta _ { t \nu } \in A , \eta _ { t \nu } \ \langle \ \delta _ { x } \notin A \} \, \eta _ { t \nu } ( d x )$$

denote the number of points of η that are pivotal for A. Show that

$$\frac { d } { d t } \mathbb { P } ( \eta _ { t \nu } \in A ) = t ^ { - 1 } \mathbb { E } [ N _ { A } ( t ) ] , \ \ t > 0 .$$

Exercise 19.4 Let v be a finite signed measure on X and let t &gt; 0 be such that λ + tv is a measure. Let f ∈ R(N) satisfy E[l.f(ηλ+tv)|] &lt; ∞, E[|f(ηλ)|] &lt; ∞ and

$$\int _ { 0 } ^ { t } \int _ { \mathcal { X } } \mathbb { E } [ | D _ { x } f ( \eta _ { \lambda + s \nu } ) | ] \, | \nu | ( d x ) \, d s < \infty .$$

Prove that then (19.6) holds. (Hint: Apply Theorem 19.1 to a suitably truncated function f and apply dominated convergence.)

Exercise 19.5 Let v be a finite signed measure and t &gt; 0 such that λ + tv is a measure. Suppose that f ∈ R+(N) satisfies (19.26). Show that E[f(ηλ+tv)] &lt; ∞ if and only if E[f(ηλ)] &lt; ∞. (Hint: Use Exercise 19.4.)

Exercise 19.6 Let W ∈ Kd such that λd(W) &gt; 0 and let S w(t) be as in Theorem 19.7. Show that

$$\lim _ { r \to \infty } \frac { S _ { r W } ( t ) } { \lambda _ { d } ( r W ) } = \phi _ { d - 1 } t e ^ { - t \phi _ { d } } .$$

Formulate and prove an analogous result in the setting of Theorem 19.8.

Exercise 19.7 Let Q be a distribution on K(a) satisfying (17.10) and let i ∈ {0, . . . , d}. Show that the function A → ∫∫f Vi(A ∩ (K + x)) dx Q(dK) from Ka to R is invariant under translations. Assume in addition that Q is invariant under rotations; show that then φ has the same property.

Exercise 19.8 Let η be a proper Poisson process on X with finite intensity measure λ. For p ∈ [0, 1] let Q be the probability measure on {0, 1} given by Qp := pδ1 + (1 − p)δ0. Let ξp be an independent Qp-marking of η. Suppose that f ∈ R(N(X × {0, 1})) is bounded and show that


<!-- p:221 -->


$$\frac { d } { d p } \mathbb { E } [ f ( \xi _ { p } ) ] & = \int \mathbb { E } [ f ( \xi _ { p } + \delta _ { ( x , 1 ) } ) - f ( \xi _ { p } + \delta _ { ( x , 0 ) } ) ] \, \lambda ( d x ) . \\$$

(Hint: Use Theorem 19.1 with λ replaced by λ © δ0 and with v replaced by λ ⊗ δ1 − λ ⊗ δ0.)

Exercise 19.9 Suppose that f ∈ R(N(X × {0, 1})). For each x ∈ X define ∆xf ∈ R(N(X × {0, 1})) by ∆xf(μ) := f(μ + δ(x,1)) − f(μ + δ(x,0)). For n ∈ N and x1,. . ., xn ∈ X define ∆x,.xn f ∈ R(N(X × {0, 1})) recursively by ∆1, f := ∆x1f and

$$\Delta _ { x _ { 1 } , \dots , x _ { n } } ^ { n } f \colon = \Delta _ { x _ { n } } \Delta _ { x _ { 1 } , \dots , x _ { n - 1 } } ^ { n - 1 } f , \ \ n \geq 2 .$$

Show for all μ ∈ N(X × {0, 1}) that

$$\Delta _ { x _ { 1 } , \dots , x _ { n } } ^ { n } f ( \mu ) = \sum _ { ( i _ { 1 } , \dots , i _ { n } ) \in \{ 0 , 1 \} ^ { n } } ( - 1 ) ^ { n - i _ { 1 } } \cdots ^ { - i _ { n } } f ( \mu + \delta _ { ( x _ { 1 } , i _ { 1 } ) } + \cdots + \delta _ { ( x _ { n } , i _ { n } ) } ) .$$

Exercise 19.10 Suppose that η and ξp, p ∈ [0, 1], are as in Exercise 19.8 and let f ∈ R(N(X × {0, 1})) be bounded. Let n ∈ N and show that

$$\int _ { \real ^ { n } } ^ { \real ^ { n } } & \frac { d ^ { n } } { d p ^ { n } } \mathbb { E } [ f ( \xi _ { p } ) ] = \int \mathbb { E } [ \Delta _ { x _ { 1 } , \dots , x _ { n } } ^ { n } f ( \xi _ { p } ) ] \, \lambda ^ { n } ( d ( x _ { 1 } , \dots , x _ { n } ) ) , \quad p \in [ 0 , 1 ] . \\$$

Deduce from Taylor's theorem for all p, q ∈ [0, 1] that

$$\mathbb { E } [ f ( \xi _ { q } ) ] = \mathbb { E } [ f ( \xi _ { p } ) ] + \sum _ { n = 1 } ^ { \infty } \frac { ( q - p ) ^ { n } } { n ! } \int \mathbb { E } [ \Delta _ { x _ { 1 } , \dots , x _ { n } } ^ { n } f ( \xi _ { p } ) ] \, \lambda ^ { n } ( d ( x _ { 1 } , \dots , x _ { n } ) ) .$$

(Hint: Use Exercise 19.8 and induction as in the final part of the proof of Theorem 19.1. The second assertion can be proved as Theorem 19.2.)

Exercise 19.11 Let η and ξp, p ∈ [0, 1], be as in Exercise 19.8. Assume that X is a Borel space and that λ is diffuse. Let μ ∈ N(X × {0, 1}) and x1, . . , n ∈ X. Define μx ,,xn := μ−δ(x1,j1)− . .−δ(x,jn) whenever μ(·×{0, 1}) is simple, x1, . . . , xn are pairwise distinct and (x1, j1), . . . , (xn, jn) ∈ μ for some j1,... , jn ∈ {0, 1}. In allx other cases define μx,..x := μ. Let f ∈ R(N(X × {0, 1})) be bounded. Show for all p, q ∈ [0, 1] that P-a.s.

$$\mathbb { E } [ f ( \xi _ { q } ) \, | \, \eta ] & = \mathbb { E } [ f ( \xi _ { p } ) \, | \, \eta ] \\ & + \sum _ { n = 1 } ^ { \infty } \frac { ( q - p ) ^ { n } } { n ! } \int \mathbb { E } [ \Delta _ { x _ { 1 } , \dots , x _ { n } } ^ { n } f ( ( \xi _ { p } ) _ { x _ { 1 } , \dots , x _ { n } } ^ { ! } ) \, | \, \eta ] \, \eta ^ { ( n ) } ( d ( x _ { 1 } , \dots , x _ { n } ) ) . \\ ( H i n t \colon U o \, E x o r i o \, 1 0 \, 1 0 \, \text {and} \, \text {the} \, \ m u t i v i o r i o \, \mathcal { M } o k o \, \text {occupation} \, \text {and} \, \text {note}$$

(Hint: Use Exercise 19.10 and the multivariate Mecke equation and note that η is simple.)


<!-- p:222 -->


## Covariance Identities

A measurable function of a Poisson process is called Poisson functional. Given a square integrable Poisson functional F, and given t ∈ [0, 1], the Poisson functional PF is defined by a combination of t-thinning and independent superposition. The family PF interpolates between the expectation of F and F. The Fock space series representation of the covariance bet u a an een  o n oon on oton involving only the first order difference operator and the operator P. This identity will play a key role in Chapter 21 on normal approximation. A corollary is the Harris-FKG correlation inequality.

### 20.1 Mehler's Formula

In this chapter we consider a proper Poisson process η on a measurable space (X, X) with σ-finite intensity measure λ and distribution Pη. Let L0 be the space of all R-valued random variables (Poisson functionals) F such that F = f(η) P-a.s. for some measurable f : N → R. This f is called a representative of F. If f is a (fixed) representative of F we define

$$D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } F \coloneqq D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } f ( \eta ) , \quad n \in \mathbb { N } , \, x _ { 1 } , \dots , x _ { n } \in \mathbb { X } .$$

Exercise 18.3 shows that the choice of the representative f does not affect x ∈ X. For ease of exposition we shall also allow for representatives f with values in [-∞, ∞]. In this case we apply the previous definitions to the representative 1{|f| &lt; ∞} f.

By assumption we can represent η as in (2.4), that is η = Σn=1δx. Let U1, U2, ... be independent random variables, uniformly distributed on [0, 1] and independent of (κ, (Xn)n≥1). Define

$$\eta _ { t } \colon = \sum _ { n = 1 } ^ { \kappa } \mathbf 1 \{ U _ { n } \leq t \} \delta _ { X _ { n } } , \quad t \in [ 0 , 1 ] .$$


<!-- p:223 -->


Then ηt is a t-thinning of η. Note that η0 = 0 and η1 = η. For q &gt; 0 let L9 denote the space of all F ∈ Lη such that E[|F|9] &lt; ∞. For F ∈ L1 with representative f we define

$$P _ { t } F \coloneqq \mathbb { E } \left [ \int f ( \eta _ { t } + \mu ) \, \Pi _ { ( 1 - t ) \lambda } ( d \mu ) \left | \, \eta \right ] , \ \ t \in [ 0 , 1 ] , \quad \ \ ( 2 0 . 2 )$$

where we recall that II denotes the distribution of a Poisson process with nteo os  a oons    ins en 3.3 and Corollary 5.9),

$$\Pi _ { \lambda } = \mathbb { E } \left [ \int \mathbf 1 \{ \eta _ { t } + \mu \in \cdot \} \, \Pi _ { ( 1 - t ) \lambda } ( d \mu ) \right ] .$$

Hence the definition of PF does not depend on the representative of F up to almost sure equality. Moreover, Lemma B.16 shows that

$$P _ { t } F = \int \mathbb { E } [ f ( \eta _ { t } + \mu ) \, | \, \eta ] \, \Pi _ { ( 1 - t ) \lambda } ( d \mu ) , \quad \mathbb { P } \text {-a.s.} , \quad t \in [ 0 , 1 ] .$$

We also note that

$$P _ { t } F = \mathbb { E } [ f ( \eta _ { t } + \eta _ { 1 - t } ^ { \prime } ) \, | \, \eta ] ,$$

where η′\_ is a Poisson process with intensity measure (1 –t)λ, independent of the pair (η, ηt). Exercise 20.1 yields further insight into the properties of the operator P.

By (20.5),

$$( 2 0 . 6 )$$

while the (conditional) Jensen inequality (Proposition B.1) shows for all p ≥ 1 the contractivity property

$$\mathbb { E } [ | P _ { t } F | ^ { p } ] \leq \mathbb { E } [ | F | ^ { p } ] , \ \ t \in [ 0 , 1 ] , \ F \in L _ { \eta } ^ { p } .$$

The proof of the covariance identity in Theorem 20.2 below is based on the following result, which is of independent interest.

Lemma 20.1 (Mehler's formula) Let F ∈ L2, n ∈ N and t ∈ [0, 1]. Then

$$D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } ( P _ { t } F ) = t ^ { n } P _ { t } D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } F , \quad \lambda ^ { n } \cdot a . e . \ ( x _ { 1 } , \dots , x _ { n } ) \in \mathbb { X } ^ { n } , \ \mathbb { P } \cdot a . s .$$

In particular,

$$\mathbb { E } [ D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } ( P _ { t } F ) ] = t ^ { n } \mathbb { E } [ D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } F ] , \quad \lambda ^ { n } \text {-a.e. ( } x _ { 1 } , \dots , x _ { n } ) \in \mathbb { X } ^ { n } . \quad ( 2 0 . 9 )$$


<!-- p:224 -->


Proof Let f be a representative of F. We first assume that f(μ) = e−μ(v) for some v ∈ R0(X), where R0(X) is as in the text preceding (18.9). It follows from the definition (20.1) (see also Exercise 5.4) that

$$\mathbb { E } [ e ^ { - \eta _ { v } ( v ) } \, | \, \eta ] = \exp \left [ \int \log \left ( 1 - t + t e ^ { - v ( y ) } \right ) \eta ( d y ) \right ] , \quad \mathbb { P } \text {-a.s.} \quad ( 2 0 . 1 0 )$$

Hence, by (20.5) and Theorem 3.9, the following function f, is a representative of PF:

$$f _ { t } ( \mu ) \coloneqq \exp \left [ - ( 1 - t ) \int ( 1 - e ^ { - w } ) \, d \lambda \right ] \exp \left [ \int \log \left ( ( 1 - t ) + t e ^ { - w ( y ) } \right ) \mu ( d y ) \right ] .$$

Let x ∈ X. Since

$$= \exp \left [ \int \log \left ( 1 - t + t e ^ { - v ( y ) } \right ) \mu ( d y ) \right ] ( 1 - t + t e ^ { - v ( x ) } ) ,$$

we obtain P-a.s. and for λ-a.e. x ∈ X that

$$D _ { x } P _ { t } F = f _ { t } ( \eta + \delta _ { x } ) - f _ { t } ( \eta ) = t ( e ^ { - v ( x ) } - 1 ) f _ { t } ( \eta ) = t ( e ^ { - v ( x ) } - 1 ) P _ { t } F .$$

This identity can be iterated to yield for all n ∈ N and λn-a.e. (x1, . . . , xn) and P-a.s. that

$$D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } P _ { t } F = t ^ { n } \prod _ { i = 1 } ^ { n } \left ( e ^ { - v ( x _ { i } ) } - 1 \right ) P _ { t } F .$$

On the other hand, we have from (18.7) that P-a.s.

$$P _ { t } D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } F & = P _ { t } \prod _ { i = 1 } ^ { n } \left ( e ^ { - v ( x _ { i } ) } - 1 \right ) F = \prod _ { i = 1 } ^ { n } \left ( e ^ { - v ( x _ { i } ) } - 1 \right ) P _ { t } F , \\$$

so that (20.8) holds for Poisson functionals of the given form.

By linearity, (20.8) extends to all F with a representative in the set G defined at (18.9). By Lemma 18.4 there exist functions fk ∈ G, k ∈ N, satisfying Fk := fk(η) → F = f(η) in L2(P) as k → ∞. Therefore we obtain from the contractivity property (20.7) that

$$\mathbb { E } [ ( P _ { t } F ^ { k } - P _ { t } F ) ^ { 2 } ] = \mathbb { E } [ ( P _ { t } ( F ^ { k } - F ) ) ^ { 2 } ] \leq \mathbb { E } [ ( F ^ { k } - F ) ^ { 2 } ] \to 0$$

as k → ∞. Taking B ∈ X with λ(B) &lt; ∞, it therefore follows from Lemma 18.5 that

$$\mathbb { E } \left [ \int _ { B ^ { n } } | D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } P _ { t } F _ { k } - D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } P _ { t } F | \lambda ^ { n } ( d ( x _ { 1 } , \dots , x _ { n } ) ) \right ] \to 0$$


<!-- p:225 -->


as k → ∞. On the other hand, we obtain from the Fock space representation (18.16) that E[|Dx ,..x 1] &lt; ∞ for λ-a.e. (x1, . ., x) ∈ Xn, so that the linearity of P, and (20.7) together imply

$$\leq \int _ { B ^ { n } } \mathbb { E } [ | D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } ( F _ { k } - F ) | ] \, \lambda ^ { n } ( d ( x _ { 1 } , \dots , x _ { n } ) ) .$$

Again by Lemma 18.5, this latter integral tends to 0 as k → ∞. Since (20.8) holds for each Fk we obtain from the triangle inequality that

$$\mathbb { E } \left [ \int _ { B ^ { n } } | D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } P _ { t } F - t ^ { n } P _ { t } D _ { x _ { 1 } , \dots , x _ { n } } ^ { n } F | \, \lambda ^ { n } ( d ( x _ { 1 } , \dots , x _ { n } ) ) \right ] = 0 .$$

Therefore (20.8) holds P ⊗ (λ)n-a.e., and hence, since λ is σ-finite, also P ⊗ λn-a.e.

Taking the expectation in (20.8) and using (20.6) proves (20.9). □

### 20.2 Two Covariance Identities

For F ∈ L2 we denote by DF the mapping (ω, x) → (DxF)(ω). The next theorem requires the additional assumption DF ∈ L2(P © λ), that is

$$\mathbb { E } \left [ \int ( D _ { x } F ) ^ { 2 } \, \lambda ( d x ) \right ] < \infty .$$

Theorem 20.2 For any F, G ∈ L2 such that DF, DG ∈ L2(P ⊗ λ),

$$\mathbb { E } [ F G ] - \mathbb { E } [ F ] \mathbb { E } [ G ] = \mathbb { E } \left [ \iint _ { 0 } ^ { 1 } ( D _ { x } F ) ( P _ { t } D _ { x } G ) \, d t \, \lambda ( d x ) \right ] . \quad ( 2 0 . 1 3 )$$

Proof Exercise 20.6 shows that the integrand on the right-hand side of (20.13) can be assumed to be measurable. Using the Cauchy-Schwarz inequality and then the contractivity property (20.7) yields

$$\leq \mathbb { E } \left [ \int ( D _ { x } F ) ^ { 2 } \, \lambda ( d x ) \right ] \mathbb { E } \left [ \int ( D _ { x } G ) ^ { 2 } \, \lambda ( d x ) \right ] ,$$

which is finite by assumption. Therefore we can use Fubini's theorem and (20.8) to obtain that the right-hand side of (20.13) equals

$$( 2 0 . 1 5 )$$


<!-- p:226 -->


For t ∈ [0, 1] and λ-a.e. x ∈ X we can apply the Fock space isometry (18.15) to DxF and DxPtG. Taking into account Lemma 20.1 this gives

$$\mathbb { E } [ ( D _ { x } F ) ( D _ { x } P _ { t } G ) ] & = t \mathbb { E } [ D _ { x } F ] \mathbb { E } [ D _ { x } G ] \\ & + \sum _ { n = 1 } ^ { \infty } \frac { t ^ { n + 1 } } { n ! } \int \mathbb { E } [ D _ { x _ { 1 } , \dots , x _ { n } , x } ^ { n + 1 } F ] \mathbb { E } [ D _ { x _ { 1 } , \dots , x _ { n } , x } ^ { n + 1 } G ] \, \lambda ^ { n } ( d ( x _ { 1 } , \dots , x _ { n } ) ) . \\$$

Inserting this into (20.15), applying Fubini's theorem (to be justified at the end of the proof) and performing the integration over [0, 1] shows that the double integral (20.15) equals

$$d o b l e \, & \text {integral (20.15)} \, \text {equals} \\ & \int \mathbb { E } [ D _ { x } F ] \mathbb { E } [ D _ { x } G ] \, \lambda ( d x ) \\ & + \sum _ { n = 1 } ^ { \infty } \frac { 1 } { ( n + 1 ) ! } \int \mathbb { E } [ D _ { x _ { 1 } , \dots , x _ { n } } ^ { n + 1 } F ] \, \mathbb { E } [ D _ { x _ { 1 } , \dots , x _ { n } } ^ { n + 1 } G ] \, \lambda ^ { n } ( d ( x _ { 1 } , \dots , x _ { n } ) ) \, \lambda ( d x ) \\ & = \sum _ { m = 1 } ^ { \infty } \frac { 1 } { m ! } \int \mathbb { E } [ D _ { x _ { 1 } , \dots , x _ { m } } ^ { m } F ] \, \mathbb { E } [ D _ { x _ { 1 } , \dots , x _ { m } } ^ { m } G ] \, \lambda ^ { m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) . \\ \text {By (18.15) this equals $\mathbb{E}[F G] - \mathbb{E} [F ] \mathbb{E} [G]$, which yields the asserted for-}$$

By (18.15) this equals E[FG] – E[F]E[G], which yields the asserted formula (20.13). By (18.16) and the Cauchy-Schwarz inequality we have that

$$\sum _ { m = 1 } ^ { \infty } \frac { 1 } { m ! } \int \left | \mathbb { E } [ D _ { x _ { 1 } , \dots , x _ { m } } ^ { m } F ] \right | \left | \mathbb { E } [ D _ { x _ { 1 } , \dots , x _ { m } } ^ { m } G ] \right | \lambda ^ { m } ( d ( x _ { 1 } , \dots , x _ { m } ) ) < \infty ,$$

justifying the use of Fubini's theorem.

□

Next we prove a symmetric version of Theorem 20.2 that avoids additional integrability assumptions.

$$\text {Theorem 2.0.3} \quad L e t \ F \in L _ { \eta } ^ { 2 } \ a n d \ G \in L _ { \eta } ^ { 2 } . \text {Then} \\ \mathbb { E } \Big [ \iint _ { 0 } ^ { 1 } ( \mathbb { E } [ D _ { x } F \, | \, \eta _ { 1 } ] ) ^ { 2 } \, d t \, \lambda ( d x ) \Big ] < \infty$$

and

$$\mathbb { E } [ G ] = \mathbb { E } [ \, \iint _ { 0 } ^ { 1 } \mathbb { E } [ D _ { x } F \, | \, \eta _ { t } ] \mathbb { E } [ D _ { x } G \, | \, \eta _ { t } ] \, d t \, \lambda ( d x ) \Big ] .$$

Proof By the thinning theorem (Corollary 5.9), ηt and η − ηt are independent Poisson processes with intensity measures tλ and (1 –t)λ, respectively. Therefore we have for F ∈ L2 with representative f and λ-a.e. x ∈ X that

$$\mathbb { E } [ D _ { x } F \, | \, \eta _ { t } ] = \int D _ { x } f ( \eta _ { t } + \mu ) \, \Pi _ { ( 1 - t ) \lambda } ( d \mu )$$


<!-- p:227 -->


holds almost surely. By (20.1), the right-hand side of (20.18) is a jointly measurable function of (the suppressed) ω ∈ Ω, x ∈ X and t ∈ [0, 1].

Now we take F, G ∈ L2 with representatives f and g, respectively. Let us first assume that DF, DG ∈ L2(P © λ). Then (20.16) follows from the (conditional) Jensen inequality and the law of the total expectation. The definition (20.2) shows for all t ∈ [0, 1] and λ-a.e. x ∈ X that

$$\mathbb { E } [ ( D _ { x } F ) ( P _ { t } D _ { x } G ) ] = \mathbb { E } \left [ D _ { x } F \int D _ { x } g ( \eta _ { t } + \mu ) \, \Pi _ { ( 1 - t ) \lambda } ( d \mu ) \right ] ,$$

so that by (20.18)

$$\mathbb { E } [ ( D _ { x } F ) ( P _ { t } D _ { x } G ) ] = \mathbb { E } [ D _ { x } F \mathbb { E } [ D _ { x } G \, | \, \eta _ { t } ] ] = \mathbb { E } [ \mathbb { E } [ D _ { x } F \, | \, \eta _ { t } ] \mathbb { E } [ D _ { x } G \, | \, \eta _ { t } ] ] .$$

Therefore (20.17) is just another version of (20.13).

Now we consider general F, G ∈ L2. By Lemma 18.4 there is a sequence Fk, k ∈ N, of Poisson functionals with representatives in G, such that s (L)   ←    ←  - 1I that DFk ∈ L2(P ⊗ λ). By the case of (20.17) already proved we have that

$$\mathbb { V } a r [ F ^ { k } - F ^ { l } ] = \mathbb { E } \left [ \int ( \mathbb { E } [ D _ { x } F ^ { k } \, | \, \eta _ { t } ] - \mathbb { E } [ D _ { x } F ^ { l } \, | \, \eta _ { t } ] ) ^ { 2 } \, \lambda ^ { * } ( d ( x , t ) ) \right ]$$

holds for all k, l ∈ N, where λ* is the product of λ and Lebesgue measure on [0, 1]. Since the space L2(Pø λ*) is complete, there exists H ∈ L2(P⊗ λ*) satisfying

$$\lim _ { k \to \infty } \mathbb { E } \left [ \int ( H ( x , t ) - \mathbb { E } [ D _ { x } F ^ { k } \, | \, \eta _ { t } ] ) ^ { 2 } \right ] \lambda ^ { * } ( d ( x , t ) ) = 0 .$$

On the other hand, it follows from the triangle inequality for conditional expectations and Lemma 18.5 that, for each C ∈ X with λ(C) &lt; ∞,

$$\int _ { C \times [ 0 , 1 ] } \mathbb { E } [ | \mathbb { E } [ D _ { x } F ^ { k } \, | \, \eta _ { t } ] - \mathbb { E } [ D _ { x } F \, | \, \eta _ { t } ] | ] \, \lambda ^ { * } ( d ( x , t ) ) \\ & \leq \int _ { C \times [ 0 , 1 ] } \mathbb { E } [ | D _ { x } F ^ { k } - D _ { x } F | ] \, \lambda ^ { * } ( d ( x , t ) ) \to 0 , \quad \text {as } k \to \infty . \\ \intertext { c o n n g i n g t h o w } \intertext { c o n n g i n g t h o w }$$

Comparing this with (20.19) shows that H(ω, x, t) = E[DxF | ηt](ω) for P ⊗ λ*-a.e. (ω, x, t) ∈ Ω × C × [0, 1] and hence also for P ⊗ λ*-a.e. (ω, x, t) ∈ Ω × X × [0, 1]. Therefore since H ∈ L2(P ⊗ λ*) we have (20.16). Now let Gk, k ∈ N, be a sequence approximating G similarly. Then equation (20.17) holds with (Fk, Gk) instead of (F, G). But the right-hand side is just an inner product in L2(P ⊗ λ*). Taking the limit as k → ∞ and using the L2-convergence proved above, namely (20.19) with H(x) = E[DxF | ηt] and likewise for G, yields the general result. □


<!-- p:228 -->


### 20.3 The Harris-FKG Inequality

As an application of the preceding theorem we obtain a useful correlation inequality for increasing functions of η. Given B ∈ X, a function f ∈ R(N) is said to be increasing on B if f(μ + δx) ≥ f(μ) for all μ ∈ N and all x ∈ B. It is said to be decreasing on B if (–f) is increasing on B.

Theorem 20.4 Suppose B ∈ X. Let f, g ∈ L2(Pη) be increasing on B and decreasing on X \ B. Then

$$\mathbb { E } [ f ( \eta ) g ( \eta ) ] \geq ( \mathbb { E } [ f ( \eta ) ] ) ( \mathbb { E } [ g ( \eta ) ] ) .$$

Proof The assumptions imply that the right-hand side of (20.17) is nonnegative. Hence the result follows. □

### 20.4 Exercises

Exercise 20.1 Suppose that X is a Borel subspace of a CSMS and that λ is locally finite. Let U1, U2, ... be independent random variables, uniformly distributed on [0, 1], and let η1\_ be a Poisson process with intensity measure (1 – t)λ, independent of the sequence (U). Let π, n ∈ N, be as in Proposition 6.3. Given μ ∈ N, if μ is locally finite then define

$$\xi _ { t } ( \mu ) \colon = \eta _ { 1 - t } ^ { \prime } + \sum _ { n = 1 } ^ { k } 1 \{ U _ { n } \leq t \} \delta _ { \pi _ { n } ( \mu ) } .$$

If μ ∈ N is not locally finite, let ξ(μ) := 0. Let F ∈ L1 have representative f. Show that μ ↔ E[f(ξt(μ))] is a representative of PF. (Hint: One needs to show that fi(μ) := E[f(ξt(μ))] is a measurable function of μ and that E[g(η)ft(η)] = E[g(η)PtF] for all g ∈ R+(N).)

Exercise 20.2 Let v ∈ L1(λ) and F := I(v) = η(v) − λ(v); see (12.4). Let t ∈ [0, 1] and show that P,F = tF, P-a.s. (Hint: Take f(μ) := μ(v) − λ(v) as a representative of F.)

Exercise 20.3 Let u ∈ L2(λ) and F ∈ L2 such that DF ∈ L2(P ©⊗ λ). Use Theorem 20.2 to show that

$$\mathbb { C } \text {Vol} [ I _ { 1 } ( u ) , F ] = \mathbb { E } \left [ \int u ( x ) D _ { x } F \, \lambda ( d x ) \right ] .$$

Give an alternative proof using the Mecke equation, making the additional assumption u ∈ L1(λ).

Exercise 20.4 Let h ∈ L1(λ2) and F := I2(h); see (12.9). Show that DxF = 2I(hx) for λ-a.e. x, where hx(y) := h(x, y), y ∈ X. (Hint: Use Exercise 4.3.)


<!-- p:229 -->


Exercise 20.5 Let h ∈ L1(λ) ∩ L2(λ) and let F := I2(h). Use Exercise 20.4 to show that DF ∈ L2(P ⊗ λ).

Exercise 20.6 Let f ∈ R(X × N) such that fx ∈ L1(Pη) for each x ∈ X, where fx := f(x, ·), and let Fx := fx(η). Show that there exists a jointly measurable version of PtFx, that is an f ∈ R(X × [0, 1] × Ω) satisfying

$$\tilde { f } ( x , t , \cdot ) = \mathbb { E } \left [ \int f _ { x } ( \eta _ { t } + \mu ) \, \Pi _ { ( 1 - t ) \lambda } ( d \mu ) \, \Big | \, \eta \right ] , \quad \mathbb { P } \text {-a.s.} , \, x \in \mathbb { X } , \, t \in [ 0 , 1 ] .$$

(Hint: Assume first that f does not depend on x ∈ X. Then (20.11) shows the assertion in the case f ∈ G, where G is defined at (18.9). The proof of Lemma 18.4 shows σ(G) = N, so that Theorem A.4 can be used to derive the assertion for a general bounded f ∈ R(N).)

Exercise 20.7 Let h ∈ L(λ2) ∩ L2(λ2) and F := I2(h). Show that

$$Z \coloneqq \iint _ { 0 } ^ { 1 } ( P _ { t } D _ { x } F ) ( D _ { x } F ) \, d t \, \lambda ( d x )$$

is in L2(P). Prove further that

$$Z = 2 \int I ( h _ { x } ) ^ { 2 } \, \lambda ( d x ) , \quad \mathbb { P } \text {-a.s.}$$

(with hx := h(x, ·)) and

D,Z = 4  h(x, y)I(hx) (dx) + 2  h(x,y)2 λ(dx), λ-a.e. y ∈ X, P-a.s.

(Hint: Use Exercises 20.2 and 20.4.)

Exercise 20.8 Let Z be a Boolean model as in Definition 17.1 and let K1, . . . , K be compact subsets of Rd. Use Theorem 20.4 to show that

$$\mathbb { P } ( Z \cap K _ { 1 } \neq \emptyset , \dots , Z \cap K _ { n } \neq \emptyset ) \geq \prod _ { j = 1 } ^ { n } \mathbb { P } ( Z \cap K _ { j } \neq \emptyset ) .$$

Give an alternative proof based on Theorem 17.3.

Exercise 20.9 Let f ∈ L2+ε for some ε &gt; 0 and assume that λ(X) &lt; ∞. Show that Df(η) ∈ L2(P ⊗ λ).


<!-- p:230 -->


## Normal Approximation

The Wasserstein distance quantifies the distance between two probability distributions. Stein's method is a general tool for obtaining bounds on this distance. Combining this method with the covariance identity of Chapter 20 yields upper bounds on the Wasserstein distance between the distribution of a standardised Poisson functional and the standard normal distribution. In their most explicit form these bounds depend only on the first and second order difference operators.

### 21.1 Stein's Method

In this chapter we consider a Poisson process η on an arbitrary measurable space (X, X) with σ-finite intensity measure λ. For a given Poisson functional F ∈ L2 (that is, F is a square integrable and σ(η)-measurable almost surely finite random variable) we are interested in the distance between the distribution of F and the standard normal distribution. We use here the Wasserstein distance to quantify the discrepancy between the laws of two (almost surely finite) random variables X0, X1. This distance is defined by

$$d _ { 1 } ( X _ { 0 } , X _ { 1 } ) = \sup _ { h \in \text {Lip(1)} } | \mathbb { E } [ h ( X _ { 0 } ) ] - \mathbb { E } [ h ( X _ { 1 } ) ] | ,$$

where Lip(1) denotes the space of all Lipschitz functions h: R → R with a Lipschitz constant less than or equal to one; see (B.3). If a sequence (X) of random variables satisfies lim→∞ d1(X, X0) = 0, then Proposition B.9 shows that X converges to X0 in distribution. Here we are interested in the central limit theorem, that is in the case where X0 has a standard normal distribution.

Let AC1,2 be the set of all differentiable functions g: R → R such that the derivative g′ is absolutely continuous and satisfies sup{lg'(x)| : x ∈ R} ≤ 1 and sup{lg"(x)| : x ∈ R} ≤ 2, for some version g" of the Radon− Nikodým derivative of g'. The next theorem is the key to the results of this chapter. Throughout the chapter we let N denote a standard normal random variable.


<!-- p:231 -->


Theorem 21.1 (Stein's method) Let F ∈ L1(P). Then

$$d _ { 1 } ( F , N ) \leq \sup _ { g \in A C _ { 1 , 2 } } | \mathbb { E } [ g ^ { \prime } ( F ) - F g ( F ) ] | .$$

Proof Let h ∈ Lip(1). Proposition B.13 shows that there exists g ∈ AC1,2 such that

$$h ( x ) - \mathbb { E } [ h ( N ) ] = g ^ { \prime } ( x ) - x g ( x ) , \quad x \in \mathbb { R } .$$

It follows that

$$| \mathbb { E } [ h ( F ) ] - \mathbb { E } [ h ( N ) ] | = | \mathbb { E } [ g ^ { \prime } ( F ) - F g ( F ) ] | .$$

Taking the supremum yields the assertion.

□

Next we use the covariance identity of Theorem 20.2 to turn the general bound (21.2) into a result for Poisson functionals.

Theorem 21.2 Assume that the Poisson process η is proper and suppose that F ∈ L2 satisfies DF ∈ L2(P ⊗ λ) and E[F] = 0. Then

$$d _ { 1 } ( F , N ) & \leq \mathbb { E } \left [ \left | 1 - \iint _ { 0 } ^ { 1 } ( P _ { t } D _ { x } F ) ( D _ { x } F ) \, d t \, \lambda ( d x ) \right | \right ] \\ & \quad + \mathbb { E } \left [ \iint _ { 0 } ^ { 1 } | P _ { t } D _ { x } F | ( D _ { x } F ) ^ { 2 } \, d t \, \lambda ( d x ) \right ] .$$

Proof Let f be a representative of F and let g ∈ AC1,2. Then we have for λ-a.e. x ∈ X and P-a.s. that

$$D _ { x } g ( F ) = g ( f ( \eta + \delta _ { x } ) ) - g ( f ( \eta ) ) = g ( F + D _ { x } F ) - g ( F ) .$$

Since g is Lipschitz (by the boundedness of its first derivative) it follows that |Dxg(F)| ≤ |DxF| and therefore Dg(F) ∈ L2(P ⊗ λ). Moreover, since

$$| g ( F ) | \leq | g ( F ) - g ( 0 ) | + | g ( 0 ) | \leq | F | + | g ( 0 ) | ,$$

also g(F) ∈ L2. Then Theorem 20.2 yields

$$\iint _ { 0 } ^ { 1 } ( P _ { t } D _ { x } F ) ( D _ { x } g ( F ) ) \, d t \, \lambda ( d x ) \Big |$$

and it follows that

$$| \mathbb { E } [ g ^ { \prime } ( F ) - F g ( F ) ] | \leq \mathbb { E } \left [ \left | g ^ { \prime } ( F ) - \int \int _ { 0 } ^ { 1 } ( P _ { t } D _ { x } F ) ( D _ { x } g ( F ) ) \, d t \, \lambda ( d x ) \right | \right ] .$$


<!-- p:232 -->


We assert that there exists a measurable function R: X × N → R such that for λ-a.e. x ∈ X and P-a.s.

$$D _ { x } g ( F ) = g ^ { \prime } ( F ) D _ { x } F + R ( x , \eta ) ( D _ { x } F ) ^ { 2 } , \quad x \in \mathbb { X } .$$

Indeed, for x ∈ X and μ ∈ N with Dxf(μ) ≠ 0, we can define

$$R ( x , \mu ) \colon = ( D _ { x } f ( \mu ) ) ^ { - 2 } ( D _ { x } g ( f ( \mu ) ) - g ^ { \prime } ( f ( \mu ) ) D _ { x } f ( \mu ) ) .$$

Otherwise we set R(x, μ) := 0. Since DxF = 0 implies that Dxg(F) = 0, we obtain (21.7). Using (21.7) in (21.6) gives

$$\mathcal { O } ( \mathbf E ) \cdot \mathbf E & ( \mathbf E ) \cdot \mathbf M ( \mathbf E ) \cdot \mathbf G ^ { 1 } \\ | \mathbb { B } [ g ^ { \prime } ( F ) - F g ( F ) ] | & \leq \mathbb { E } \left [ | g ^ { \prime } ( F ) | 1 - \iint _ { 0 } ^ { 1 } ( P _ { t } D _ { x } F ) ( D _ { x } F ) \, d t \, \lambda ( d x ) \right ] \\ & + \mathbb { E } \left [ \iint _ { 0 } ^ { 1 } | P _ { t } D _ { x } F | | R ( x , \eta ) | ( D _ { x } F ) ^ { 2 } \, d t \, \lambda ( d x ) \right ] .$$

By assumption, |g'(F)| ≤ 1. Moreover, Proposition A.35 and the assumption |g"(y)| ≤ 2 for λ1-a.e. y ∈ R imply for all (x, μ) ∈ X × N that

$$| g ( f ( \mu + \delta _ { x } ) ) - g ( f ( \mu ) ) - g ^ { \prime } ( f ( \mu ) ) D _ { x } f ( \mu ) | \leq ( D _ { x } f ( \mu ) ) ^ { 2 } ,$$

so that |R(x, μ)| ≤ 1. Using these facts in (21.8) and applying Theorem 21.1 gives the bound (21.4). □

### 21.2 Normal Approximation via Difference Operators

Since the bound (21.4) involves the operators P, it is often not easy to apply. The following bound is the main result of this chapter, and involves only the first and second order difference operators. In fact it can be represented in terms of the following three constants:

$$in \text {terms of the following three constants} & \int _ { \alpha _ { F , 1 } } \colon = 2 \left [ \int ( \mathbb { E } [ ( D _ { x } F ) ^ { 2 } ( D _ { y } F ) ^ { 2 } ] ) ^ { 1 / 2 } \\ & \times ( \mathbb { E } [ ( D _ { x , z } ^ { 2 } F ) ^ { 2 } ( D _ { y , z } ^ { 2 } F ) ^ { 2 } ] ) ^ { 1 / 2 } \, \lambda ^ { 3 } ( d ( x , y , z ) ) \right ] ^ { 1 / 2 } , \\ & \alpha _ { F , 2 } \colon = \left [ \int \mathbb { E } [ ( D _ { x , z } ^ { 2 } F ) ^ { 2 } ( D _ { y , z } ^ { 2 } F ) ^ { 2 } ] \, \lambda ^ { 3 } ( d ( x , y , z ) ) \right ] ^ { 1 / 2 } , \\ & \alpha _ { F , 3 } \colon = \int \mathbb { E } [ | D _ { x } F | ^ { 3 } ] \, \lambda ( d x ) . \\ \text {Theorem 21.3} & \quad S u p p o s e \ t h a t \ F \in L _ { \eta } ^ { 2 } \ s a t i s f i e s \ D F \in L ^ { 2 } ( \mathbb { P } \otimes \lambda ) , \, \mathbb { E } [ F ] = 0$$

Theorem 21.3 Suppose that F ∈ L2 satisfies DF ∈ L2(P ⊗ λ), E[F] = 0 and Var[F] = 1. Then,

$$d _ { 1 } ( F , N ) \leq \alpha _ { F , 1 } + \alpha _ { F , 2 } + \alpha _ { F , 3 } .$$


<!-- p:233 -->


Proof Clearly we can assume that αF,1, αF,2, αF,3 are finite.

Since (21.9) concerns only the distribution of η, by Corollary 3.7 it is no restriction of generality to assume that η is a proper point process. Our starting point is the inequality (21.4). By Hölder's inequality (A.2), the second term on the right-hand side can be bounded from above by

$$( 2 1 . 1 0 )$$

where the inequality comes from the contractivity property (20.7). Applying Jensen's inequality to the first term on the right-hand side of (21.4), we see that it is enough to show that

$$\left | \right ) ^ { 1 / 2 } \leq \alpha _ { F , 1 } + \alpha _ { F , 2 } . \quad ( 2 1 . 1 1 )$$

Let Z := ∫∫1 (P,DxF)(DxF) dt λ(dx). Theorem 20.2 and our assumptions on F show that E[Z] = 1. Hence the left-hand side of (21.11) equals (E[Z2]–1)1/2. By the L1-version of the Poincaré inequality (Corollary 18.8),

$$\mathbb { E } [ Z ^ { 2 } ] - 1 \leq \mathbb { E } \left [ \int ( D _ { y } Z ) ^ { 2 } \, \lambda ( d y ) \right ] .$$

By Hölder's inequality and (21.10), the random variable

$$W ( \eta ) \colon = \iint _ { 0 } ^ { 1 } | ( P _ { t } D _ { x } F ) ( D _ { x } F ) | \, d t \, \lambda ( d x ) \\$$

is integrable and therefore P-a.s. finite. Hence, by Exercise 4.1, W(η + δy) is also P-a.s. finite for λ-a.e. y ∈ X. Hence, by the triangle inequality,

$$\iint _ { 0 } ^ { 1 } | D _ { y } [ ( P _ { t } D _ { x } F ) ( D _ { x } F ) ] | \, d t \, \lambda ( d x ) < \infty , \quad \mathbb { P } \text {-a.s.} , \, \lambda \text {-a.e.} \, y \in \mathbb { X } . \ \ ( 2 1 . 1 3 )$$

Therefore

$$D _ { y } Z = \iint _ { 0 } ^ { 1 } D _ { y } [ ( P _ { t } D _ { x } F ) ( D _ { x } F ) ] \, d t \, \lambda ( d x ) ,$$

again P-a.s. and for λ-a.e. y ∈ X. Hence we obtain from (21.12) that

$$\mathbb { E } [ Z ^ { 2 } ] - 1 \leq & \mathbb { E } \left [ \int ( \iint _ { 0 } ^ { 1 } | D _ { y } [ ( P _ { t } D _ { x } F ) ( D _ { x } F ) ] | \, d t \, \lambda ( d x ) ) ^ { 2 } \, \lambda ( d y ) \right ] . \ \ ( 2 1 . 1 4 )$$

Comparison of (21.14) and (21.11) now shows that the inequality

$$( \mathbb { E } [ \int ( \iint _ { 0 } ^ { 1 } | D _ { y } ( ( P _ { t } D _ { x } F ) ( D _ { x } F ) ) | d t \, \lambda ( d x ) ] ^ { 2 } \, \lambda ( d y ) ] ) ^ { 1 / 2 } \leq \alpha _ { F , 1 } + \alpha _ { F , 2 } \\$$


<!-- p:234 -->


would imply (21.11).

We now verify (21.15). To begin with we apply Exercise 18.2 and the inequality (a + b + c)2 ≤ 3(a2 + b2 + c2) for any a, b, c ∈ R (a consequence of Jensen's inequality) to obtain

$$\mathbb { E } [ \int ( \iint _ { 0 } ^ { 1 } | D _ { y } ( ( P _ { t } D _ { x } F ) ( D _ { x } F ) ) | \, d t \, \lambda ( d x ) \right ] ^ { 2 } \lambda ( d y ) ] \leq 3 ( I _ { 1 } + I _ { 2 } + I _ { 3 } ) , \\$$

where

$$I _ { 1 } \colon = & \ \mathbb { E } [ \int ( \int _ { 0 } ^ { 1 } | P _ { y } D _ { x } F | | D _ { x } ^ { 2 } | \, | d t \, \lambda ( d x ) \Big ) ^ { 2 } \, ( d y ) ] , \\ I _ { 2 } \colon = & \ \mathbb { E } [ \int ( \int _ { 0 } ^ { 1 } | P _ { t } D _ { x } F | | D _ { x , y } ^ { 2 } F | \, d t \, \lambda ( d x ) ) ^ { 2 } \, \lambda ( d y ) ] , \\ I _ { 3 } \colon = & \ \mathbb { E } [ \int ( \int _ { 0 } ^ { 1 } | D _ { y } P _ { t } D _ { x } F | | D _ { x , y } ^ { 2 } F | \, d t \, \lambda ( d x ) ) ^ { 2 } \, \lambda ( d y ) ] . \\ \text {We shall bound } I _ { 1 } \, I _ { 2 } \, I _ { 3 } \text { with the help of } I _ { \ell } \text {gamma } 2 1 . 4 \text { below}$$

We shall bound I1, I2, I3 with the help of Lemma 21.4 below.

Since DF ∈ L2(P ⊗ λ) we have that DxF ∈ L2(P) for λ-a.e. x, so that Mehler's formula (Lemma 20.1) shows that DyPtDxF = tPD2 F for λ2a.e. (x, y) ∈ X2 and P-a.s. Applying Lemma 21.4 with G(x, y) = D2, F, H(x, y) = DxF and v(dt) = 2t dt gives

$$I ( x , y ) & = D _ { x } ^ { 1 } \text { and } \nu ( d _ { x } ) = 2 \, \text {u} \, \text {g} \, \text {c} \, \\ I _ { 1 } & \leq \frac { 1 } { 4 } \int ( \mathbb { E } [ ( D _ { x _ { 1 } , y } ^ { 2 } F ) ^ { 2 } ( D _ { x _ { 2 } , y } ^ { 2 } F ) ^ { 2 } ] ) ^ { 1 / 2 } ( \mathbb { E } [ ( D _ { x _ { 1 } } F ) ^ { 2 } ( D _ { x _ { 2 } } F ) ^ { 2 } ] ) ^ { 1 / 2 } \, \lambda ^ { 3 } ( d ( x _ { 1 } , x _ { 2 } , y ) ) \\ & \leq \frac { 1 } { 1 6 } \alpha _ { F , 1 } ^ { 2 } . \\ I \, \text {emma 21} \, 1 \, \text {with} \, G ( x _ { y } ) & = D _ { x } \, F \, H ( x _ { y } ) = | D ^ { 2 } \, F | \, \text {and} \, \nu ( d t ) = d t \, \text {gives}$$

Lemma 21.4 with G(x, y) = DxF, H(x, y) = |D2,yF| and v(dt) = dt gives

$$I _ { 2 } \leq \frac { 1 } { 4 } \alpha _ { F , 1 } ^ { 2 } .$$

Finally we apply Lemma 21.4 with G(x, y) = D2 y F, H(x, y) = |D2 F| and v(dt) = 2t dt to obtain

$$I _ { 3 } \leq \frac { 1 } { 4 } \int \mathbb { E } [ ( D _ { x _ { 1 } , y } ^ { 2 } F ) ^ { 2 } ( D _ { x _ { 2 } , y } ^ { 2 } F ) ^ { 2 } ] \, \lambda ^ { 3 } ( d ( x _ { 1 } , x _ { 2 } , y ) ) = \frac { 1 } { 4 } \alpha _ { F , 2 } ^ { 2 } .$$

Combining the bounds (21.17), (21.18) and (21.19) with the inequality √a + b ≤ √a + √b (valid for all a, b ≥ 0) yields

$$( 3 ( I _ { 1 } + I _ { 2 } + I _ { 3 } ) ) ^ { 1 / 2 } & \leq \sqrt { 3 } \sqrt { I _ { 1 } + I _ { 2 } } + \sqrt { 3 } \sqrt { I _ { 3 } } \\ & \leq \sqrt { 3 } \frac { \sqrt { 5 } } { \sqrt { 1 6 } } \alpha _ { F , 1 } + \frac { \sqrt { 3 } } { 2 } \alpha _ { F , 2 } \leq \alpha _ { F , 1 } + \alpha _ { F , 2 } .$$


<!-- p:235 -->


Inserting this into (21.16) yields (21.15), and hence the theorem.

□

The following lemma has been used in the preceding proof.

Lemma 21.4 Let g ∈ R(X2×N) and h ∈ R+(X2×N). For (x, y) ∈ X2 define G(x, y) := g(x, y, η) and H(x, y) := h(x, y, η). Assume that E[|G(x, y)|] &lt; ∞ for λ2-a.e. (x, y) and let v be a probability measure on [0, 1]. Then

$$& \quad \text {for } \lambda ^ { - a . e . } \left ( x , y \right ) a l d \, \text {let } \nu \, \text {be a probability measure on } [ 0 , 1 ] . \, \text {Then} \\ & \quad \mathbb { B } [ \int ( \iint | P _ { t } G ( x , y ) | H ( x , y ) \, \nu ( d t ) \, \lambda ( d x ) ) ^ { 2 } \, \lambda ( d y ) ] \\ & \quad \leq \int ( \mathbb { E } [ G ( x _ { 1 } , y ) ^ { 2 } G ( x _ { 2 } , y ) ^ { 2 } ] ) ^ { 1 / 2 } ( \mathbb { E } [ H ( x _ { 1 } , y ) ^ { 2 } H ( x _ { 2 } , y ) ^ { 2 } ] ) ^ { 1 / 2 } \, \lambda ^ { 3 } ( d ( x _ { 1 } , x _ { 2 } , y ) ) .$$

Proof Given y ∈ X define the random variable

$$J ( y ) \colon = \left ( \iint | P _ { t } G ( x , y ) | H ( x , y ) \, \nu ( d t ) \, \lambda ( d x ) \right ) ^ { 2 } . \\$$

By the representation (20.4) of the operator P and the triangle inequality for conditional expectations we have almost surely that

$$J ( y ) \leq \left ( \iint \mathbb { E } [ | g ( x , y , \eta _ { t } + \mu ) | \ | \ \eta ] H ( x , y ) \, \Pi _ { ( 1 - t ) \lambda } ( d \mu ) \, \nu ( d t ) \, \lambda ( d x ) \right ) ^ { 2 } .$$

By the pull out property of conditional expectations, Fubini's theorem and Lemma B.16,

$$L \text {Clima} \, B . 1 , & & \\ J ( y ) \leq \left ( \iint \mathbb { E } \left [ \int | g ( x , y , \eta _ { t } + \mu ) | H ( x , y ) \, \lambda ( d x ) \left | \, \eta \right ] \Pi _ { ( 1 - t ) , \lambda } ( d \mu ) \, \nu ( d t ) \right ) ^ { 2 } . \\ N & \quad - \\$$

Next we apply Jensen's inequality to the two outer integrations and the conditional expectation to obtain P-a.s. that

$$J ( y ) \leq \iint \mathbb { E } \left [ \left ( \int | g ( x , y , \eta _ { t } + \mu ) | H ( x , y ) \, \lambda ( d x ) \right ) ^ { 2 } \, \left | \, \eta \right ] \Pi _ { ( 1 - t ) \lambda } ( d \mu ) \, \nu ( d t ) .$$

By Fubini's theorem (and the pull out property) and Jensen's inequality applied to the conditional expectation and the integration II(1–t)(dμ) v(dt), it follows almost surely that

$$b ( y ) & \simeq \int H ( x _ { 1 } , y ) H ( x _ { 2 } , y ) \iint \mathbb { E } [ g ( x _ { 1 } , y , \eta _ { 1 } + \mu ) | \mathcal { S } ( x _ { 2 } , y , \eta _ { 2 } + \mu ) | \eta ] \\ & \times \Pi _ { ( 1 - t ) \lambda } ( d \mu ) \, \nu ( d t ) \, \lambda ^ { 2 } ( d ( x _ { 1 } , x _ { 2 } ) ) \\ & \leq \int H ( x _ { 1 } , y ) H ( x _ { 2 } , y ) \left ( \iint \mathbb { E } [ g ( x _ { 1 } , y , \eta _ { 1 } + \mu ) ^ { 2 } g ( x _ { 2 } , y , \eta _ { 2 } + \mu ) ^ { 2 } \, | \, \eta ] \\ & \quad \times \Pi _ { ( 1 - t ) \lambda } ( d \mu ) \, \nu ( d t ) \right ) ^ { 1 / 2 } \lambda ^ { 2 } ( d ( x _ { 1 } , x _ { 2 } ) ) .$$


<!-- p:236 -->


Set I := E[ ∫ J(y) λ(dy)], which is the left-hand side of the inequality we seek to prove. By the Cauchy-Schwarz inequality and the law of total expectation it follows that

$$I & \leq \int \left ( \iint \mathbb { E } [ g ( x _ { 1 } , y , \eta _ { t } + \mu ) ^ { 2 } g ( x _ { 2 } , y , \eta _ { t } + \mu ) ^ { 2 } ] \, \Pi _ { ( 1 - \lambda ) \lambda } ( d \mu ) \, \nu ( d t ) \right ) ^ { 1 / 2 } \\ & \quad \times ( \mathbb { E } [ H ( x _ { 1 } , y ) ^ { 2 } H ( x _ { 2 } , y ) ^ { 2 } ] ) ^ { 1 / 2 } \, \lambda ^ { 3 } ( d ( x _ { 1 } , x _ { 2 } , y ) ) .$$

Using the superposition and thinning theorems as in (20.3) we can conclude the proof. □

### 21.3 Normal Approximation of Linear Functionals

In this section we treat a simple example in the general setting.

Example 21.5 Let g ∈ L1(λ) ∩ L3(λ) such that ∫ g2 dλ = 1. Let F := I(g) a  =       ( −-  =   t ()   ie Var[F] = 1 by Proposition 12.4. The definition (12.4) and Proposition 12.1 show for λ2-a.e. (x1, x2) and P-a.s. that Dx1 F = g(x1) and Dx|,x2F = 0. Hence Theorem 21.3 implies that

$$d _ { 1 } ( I ( g ) , N ) \leq \int | g | ^ { 3 } \, d \lambda .$$

The bound (21.20) is optimal up to a multiplicative constant:

Proposition 21.6 Let X, be a Poisson distributed random variable with parameter t &gt; 0 and define t := t−1/2(Xt − t). Then d1(, N) ≤ t−1/2 and

$$\liminf _ { t \to \infty } \sqrt { t } \, d _ { 1 } ( \hat { X } _ { t } , N ) \geq 1 / 4 .$$

Proof The upper bound follows from (21.20) when applied to a homogeneous Poisson process on R+ of unit intensity with g(t) := t−1/21[0,t].

To derive the lower bound we construct a special Lipschitz function. Let h: R → R be the continuous 1-periodic function which is zero on the integers and increases (resp. decreases) with rate 1 on the interval [0, 1/2] (resp. [1/2, 1]). This function has Lipschitz constant 1. The same is then true for the function h1 : R → R defined by h,(x) := h( √tx + t)/ √t. By definition, h() ≡ 0. On the other hand, Exercise 21.1 shows that

$$\lim _ { t \to \infty } \sqrt { t } \, \mathbb { E } [ h _ { t } ( N ) ] = 1 / 4 ;$$

since d1(X,, N) ≥ E[h,(N)], the desired inequality follows.

□


<!-- p:237 -->


### 21.4 Exercises

Exercise 21.1 Prove (21.21). Is the result true for other random variables?

Exercise 21.2 Let η be a Poisson process on R+ with intensity measure v as in Exercise 7.8. Show the central limit theorem v(t)−1/2(η(t) − v(t)) → N as t → ∞. (Hint: Use Example 21.5.)

Exercise 21.3 Let u ∈ L1(λ), v ∈ R+(X) and F := η(u) + exp[−η(v)]. Show that P-a.s. and for λ2-a.e. (x, y) we have that |DxF| ≤ |u(x)| + v(x) exp[−η(v)] and |Dx,F| ≤ v(x)v(y) exp[−η(v)]. (Hint: Use Lemma 18.2.)

Exercise 21.4 Let u, v ∈ L1(λ) ∩ L2(λ). Assume that λ(u2) &gt; 0 and v ≥ 0. For t &gt; 0 let ηt be a Poisson process with intensity measure tλ. Define Ft := ηt(u) + exp[−η(v)]. Show that there exists a &gt; 0 such that Var[Ft] ≥ at for all t ≥ 1. (Hint: Use Exercise 18.8.)

Exercise 21.5 Let u, v ∈ L1(λ) ∩ L2(λ) and assume that v ≥ 0. Let F := η(u) + exp[−η(v)] and show that

$$\int ( \mathbb { E } [ ( D _ { x } F ) ^ { 2 } ( D _ { y } F ) ^ { 2 } ] ) ^ { 1 / 2 } ( \mathbb { E } [ ( D _ { x , z } ^ { 2 } F ) ^ { 2 } ( D _ { y , z } ^ { 2 } F ) ^ { 2 } ] ) ^ { 1 / 2 } \, \lambda ^ { 3 } ( d ( x , y , z ) ) \\ \leq \lambda ( v ^ { 2 } ) \lambda ( ( | u | + v ) v ) ^ { 2 } \exp \left [ - 2 ^ { - 1 } \lambda ( 1 - e ^ { - 4 v } ) \right ] .$$

Assume in addition that v ∈ L4(λ) and show that

$$\int \mathbb { E } [ ( D _ { x , z } ^ { 2 } F ) ^ { 2 } ( D _ { y , z } ^ { 2 } F ) ^ { 2 } ] \, \lambda ^ { 3 } ( d ( x , y , z ) ) \leq \lambda ( v ^ { 2 } ) ^ { 2 } \lambda ( v ^ { 4 } ) \exp \left [ - \lambda ( 1 - e ^ { - 4 v } ) \right ] .$$

Exercise 21.6 Let u, v ∈ L1(λ) ∩ L3(λ) and assume that v ≥ 0. Let F := η(u) + exp[−η(v)] and show that

$$\int \mathbb { E } [ | D _ { x } F | ^ { 3 } ] \, \lambda ( d x ) \leq \lambda ( | u | ^ { 3 } ) + 7 ( \lambda ( | u | ^ { 3 } ) + \lambda ( v ^ { 3 } ) ) \exp \left [ - \lambda ( 1 - e ^ { - v } ) \right ] .$$

Exercise 21.7 Let u ∈ L1(λ) ∩ L3(λ) and v ∈ L1(λ) ∩ L4(λ). Assume that v ≥ 0. For t &gt; 0 let ηt be a Poisson process with intensity measure tλ. Define Ft := ηt(u) + exp[−ηt(v)] and assume that σt := (Var[Ft])1/2 &gt; 0. Let Êt := σ−1(Ft − E[Ft]). Show that d1(Êt, N) ≤ c1σ−2t3/2 + c2σ−3t, t ≥ 1, where c1, c2 &gt; 0 depend on u, v and λ, but not on t. Assume in addition that λ(u2) &gt; 0 and show that then d1(Êt, N) ≤ c3t−1/2, t ≥ 1, for some c3 &gt; 0. (Hint: Combine Theorem 21.3 with Exercises 21.4–21.6.)


<!-- p:238 -->


## Normal Approximation in the Boolean Model

The intersection of a Boolean model Z having convex grains with a convex observation window W is a finite union of convex sets and hence amenable to additive translation invariant functionals φ, such as the intrinsic volumes. The general results of Chapter 21 yield bounds on the Wasserstein distance between the distribution of the standardised random variable φ(Z ∩ W) and the standard normal. These bounds depend on the variance of φ(Z ∩ W) and are of the presumably optimal order λa(W)-1/2 whenever this variance grows like the volume λa(W) of W.

### 22.1 Normal Approximation of the Volume

As in Definition 17.1, let d ∈ N, let Q be a probability measure on the space C(d) of non-empty compact sets in Rd, let ξ be an independent Qmarking of a stationary Poisson process η in Rd with intensity γ ∈ (0, ∞) and let Z be the Boolean model induced by ξ. Recall from Theorem 5.6 that ξ is a Poisson process on Rd × C(d) with intensity measure λ = γλd ©Q. Throughout this chapter we assume that the integrability condition (17.10) holds. Proposition 17.5 then shows that Z is a random element of Fd.

In the whole chapter we fix a Borel set (observation window) W ⊂ Rd satisfying λa(W) ∈ (0, ∞). In Section 22.2 we shall assume W to be convex. As in Section 19.3 we study Poisson functionals of the form φ(Z ∩ W), where φ is a (geometric) function defined on compact sets. Under certain assumptions on φ and Q we shall derive from Theorem 21.3 that φ(Z∩ rW) is approximately normal for large r &gt; 0. We start with the volume φ = λd.

By Proposition 17.4 and Fubini's theorem,

$$F _ { W } \colon = \lambda _ { d } ( Z \cap W )$$

is a (bounded) random variable and hence a Poisson functional. Recall from Proposition 17.4 that E[Fw] = pλd(W), where p &lt; 1 is given at (17.8). The variance of Fw is given as follows.


<!-- p:239 -->


Proposition 22.1 We have that

$$\mathbb { V } a r [ F _ { W } ] = ( 1 - p ) ^ { 2 } \int \lambda _ { d } ( W \cap ( W + x ) ) ( e ^ { \gamma \beta _ { d } ( x ) } - 1 ) \, d x ,$$

where βd(x) = ∫ λd(K ∩ (K + x)) Q(dK), as in (17.13). If λd(∂W) = 0 and ∫ λd(K)2 Q(dK) &lt; ∞, then

$$\lim _ { r \to \infty } \lambda _ { d } ( r W ) ^ { - 1 } \, \mathbb { V } a r [ F _ { r W } ] = ( 1 - p ) ^ { 2 } \int ( e ^ { \gamma \beta _ { d } ( x ) } - 1 ) \, d x .$$

Proof By Fubini's theorem

$$1 \, F _ { \ } C y \, F _ { \ } A d o w h { 1 } \, S \, d o w h { 1 } \, F _ { \ } C y \, \cdot \, & \in [ \, \iint 1 _ { \{ x \in W , y \in W \} 1 _ { \{ x \in Z , y \in Z \} \, d y \, d x } \, ] } \\ \mathbb { E } [ F _ { W } ^ { 2 } ] = \mathbb { E } [ \, \iint 1 _ { \{ x \in W , y \in W \} 1 _ { \{ x \in Z , y \in Z \} \, d y \, d x } \, ]$$

By Theorem 17.8 this equals

$$p ^ { 2 } \lambda _ { d } ( W ) ^ { 2 } + ( 1 - p ) ^ { 2 } \iint \{ 1 \{ x \in W , y \in W \} ( e ^ { \gamma \beta _ { d } ( x - y ) } - 1 ) \, d y \, d x .$$

Changing variables and using the equation E[λd(Z ∩ W)] = pλd(W), (22.2) follows.

The second assertion follows from (22.2) upon combining Exercises 17.10 and 17.11 with dominated convergence. □

In the next theorem we need to assume that φa,3 &lt; ∞, where

$$\phi _ { d , k } \colon = \int ( \lambda _ { d } ( K ) ) ^ { k } \, \mathbb { Q } ( d K ) , \quad k \in \mathbb { N } .$$

In particular, φd = φa,1 as given by (17.11). It follows from Exercise 22.2 that Var[Fw] &gt; 0 provided that φd &gt; 0. In this case we use the notation

$$c _ { W } \coloneqq \lambda _ { d } ( W ) ( 1 - p ) ^ { - 2 } \left [ \int \lambda _ { d } ( W \cap ( W + x ) ) ( e ^ { \gamma \beta _ { d } ( x ) } - 1 ) \, d x \right ] ^ { - 1 } . \quad ( 2 2 . 5 ) \\ \\$$

Recall from (21.1) the definition of the Wasserstein distance d1 and let N be a standard normal random variable.

Theorem 22.2 Define the random variable Fw by (22.1). Assume that φd,3 &lt; ∞ and also that φd &gt; 0. Define Êw := (Var[Fw])−1/2(Fw − E[Fw]). Then

$$d _ { 1 } ( \hat { F } _ { W } , N ) \leq [ 2 ( \gamma \phi _ { d , 2 } ) ^ { 3 / 2 } c _ { W } + \gamma ^ { 3 / 2 } \phi _ { d , 2 } c _ { W } + \gamma \phi _ { d , 3 } ( c _ { W } ) ^ { 3 / 2 } ] ( \lambda _ { d } ( W ) ) ^ { - 1 / 2 } .$$


<!-- p:240 -->


Proof We apply Theorem 21.3. To simplify notation, we assume γ = 1 and leave the general case to the reader. Let σ := (Var[Fw])1/2. We shall use the notation Kx := K + x for (x, K) ∈ Rd × C(d).

By the additivity of Lebesgue measure, we have almost surely and for λd ⊗ Q-a.e. (x, K) ∈ Rd × C(d) (similarly to Example 18.1) that

$$D _ { ( x , K ) } F _ { W } = \lambda _ { d } ( K _ { x } \cap W ) - \lambda _ { d } ( Z \cap K _ { x } \cap W ) .$$

(We leave it to the reader to construct a suitable representative of Fw.) Iterating this identity (or using (18.3)) yields P-a.s. and for (λd ⊗ Q)2-a.e. ((x, K), (y, L)) that

$$D _ { ( x , K ) , ( y , L ) } ^ { 2 } F _ { W } = \lambda _ { d } ( Z \cap K _ { x } \cap L _ { y } \cap W ) - \lambda _ { d } ( K _ { x } \cap L _ { y } \cap W ) .$$

In particular,

$$| D _ { ( x , K ) } F _ { W } | & \leq \lambda _ { d } ( ( K + x ) \cap W ) , \\ | D _ { ( x , K ) , ( y , L ) } ^ { 2 } F _ { W } | & \leq \lambda _ { d } ( ( K + x ) \cap ( L + y ) \cap W ) .$$

The following calculations rely on the monotonicity of Lebesgue measure and the following direct consequence of Fubini's theorem:

$$\int _ { \lambda _ { d } ( A \cap ( B + x ) ) \, d x } = \lambda _ { d } ( A ) \lambda _ { d } ( B ) , \quad A , B \in \mathcal { B } ^ { d } .$$

By (22.9),

$$\mathcal { B } \left ( 2 2 . 9 \right ) , \\ \mathbb { E } \left [ \int ( D _ { ( x , K ) } F _ { W } ) ^ { 2 } \, \lambda ( d ( x , K ) ) \right ] & \leq \iint \lambda _ { d } ( K _ { x } \cap W ) \lambda _ { d } ( W ) \, d x \, \mathbb { Q } ( d K ) \\ & = ( \lambda _ { d } ( W ) ) ^ { 2 } \int \lambda _ { d } ( K ) \, \mathbb { Q } ( d K ) .$$

Hence DFw ∈ L2(P ⊗ λ) and Theorem 21.3 applies. Let Ê := Êw. Using the bounds (22.9) and (22.10) in the definition of αf,1 yields

$$( \alpha _ { \hat { F } , 1 } ) ^ { 2 } & \leq \frac { 4 } { \sigma ^ { 4 } } \iiiiiii\iint _ { \lambda _ { d } ( K _ { x } \cap W ) \lambda _ { d } ( L _ { y } \cap W ) \lambda _ { d } ( K _ { x } \cap M _ { z } \cap W ) } \\ & \times \lambda _ { d } ( L _ { y } \cap M _ { z } \cap W ) \, d x \, d y \, d z \, \mathbb { Q } ^ { 3 } ( d ( K , L , M ) ) .$$

Since λd(Kx) = λd(K) we obtain

$$( \alpha _ { \hat { F } , 1 } ) ^ { 2 } & \leq \frac { 4 } { \sigma ^ { 4 } } \iiiiiiiint _ { \lambda _ { d } ( K ) \lambda _ { d } ( L ) \lambda _ { d } ( K _ { x } \cap M _ { z } \cap W ) \lambda _ { d } ( L _ { y } \cap M _ { z } \cap W ) } \\ & \quad \times d x \, d y \, d z \, \mathbb { Q } ^ { 3 } ( d ( K , L , M ) ) .$$


<!-- p:241 -->


Therefore, by (22.11),

$$( \alpha _ { \hat { F } , 1 } ) ^ { 2 } & \leq \frac { 4 } { \sigma ^ { 4 } } \iint \lambda _ { d } ( K ) ^ { 2 } \lambda _ { d } ( L ) \lambda _ { d } ( M _ { z } \cap W ) \lambda _ { d } ( L _ { y } \cap M _ { z } \cap W ) \\ & \quad \times d y \, d z \, \mathbb { Q } ^ { 3 } ( d ( K , L , M ) ) .$$

Since λd(Mz ∩ W) ≤ λd(M), applying (22.11) twice gives

$$( \alpha _ { \hat { F } , 1 } ) ^ { 2 } \leq \frac { 4 } { \sigma ^ { 4 } } \int \lambda _ { d } ( K ) ^ { 2 } \lambda _ { d } ( L ) ^ { 2 } \lambda _ { d } ( M ) ^ { 2 } \lambda _ { d } ( W ) \, \mathbb { Q } ^ { 3 } ( d ( K , L , M ) ) ,$$

that is

$$^ { 3 / 2 } \frac { ( \lambda _ { d } ( W ) ) ^ { 1 / 2 } } { \sigma ^ { 2 } } = 2 ( \phi _ { d , 2 } ) ^ { 3 / 2 } c _ { W } ( \lambda _ { d } ( W ) ) ^ { - 1 / 2 } ,$$

where we have used that σ2 = λd(W)/cw; see (22.5) and (22.2). We leave it to the reader to prove similarly that

$$\alpha _ { \hat { F } , 2 } \leq \phi _ { d , 2 } \frac { ( \lambda _ { d } ( W ) ) ^ { 1 / 2 } } { \sigma ^ { 2 } } = \phi _ { d , 2 } c _ { W } ( \lambda _ { d } ( W ) ) ^ { - 1 / 2 }$$

and

$$\alpha _ { \hat { F } , 3 } \leq \phi _ { d , 3 } \frac { \lambda _ { d } ( W ) } { \sigma ^ { 3 } } = \phi _ { d , 3 } ( c _ { W } ) ^ { 3 / 2 } ( \lambda _ { d } ( W ) ) ^ { - 1 / 2 } .$$

Inserting these bounds into (21.9) gives the result (22.6).

□

As a corollary we obtain a central limit theorem for the volume.

Corollary 22.3 Assume that λd(∂W) = 0. Assume also that φd &gt; 0 and φd,3 &lt; ∞. For r &gt; 0 let Wr := r1/dW. Then Ê w,d → N as r → ∞.

Proof By Proposition 22.1, cw, = λd(Wr) Var[Fw,]−1 tends, as r → ∞, to the inverse of (1 − p)2 ∫ (eγβa(x) – 1) dx, which is finite by Exercise 22.1 and our assumption φa &gt; 0. Hence the result follows from Theorem 22.2.

The rate of convergence (with respect to the Wasserstein distance) in Corollary 22.3 is r-1/2. Proposition 21.6 suggests that this rate is presumably optimal. Indeed, if Q is concentrated on a single grain with small volume v &gt; 0 then λd(Z ∩ W) approximately equals vη(W).

### 22.2 Normal Approximation of Additive Functionals

In the remainder of this chapter we assume that W ∈ K(d) is a compact, convex set with λa(W) &gt; 0. In particular, the boundary of W has Lebesgue measure 0. Let W, := r1/dW for r &gt; 0, so that λd(Wr) = rλd(W). We also assume that Q is concentrated on the system K(d) of all convex K ∈ C(d). As in Section 19.3 we can then assume that Z∩ K is for each K ∈ Ka a random element of the convex ring Rd. By Lemma A.30, (ω, K) ↔ Z(ω) ∩ K is a measurable mapping from Ω × Kd to Rd.


<!-- p:242 -->


A function φ: Cd → R is said to be translation invariant if, for all (x, K) ∈ Rd × Cd, φ(K + x) = φ(K). We say that a measurable function φ: Rd → R is geometric if it is translation invariant, additive and satisfies

$$M ( \varphi ) \coloneqq \sup \{ | \varphi ( K ) | \colon K \in \mathcal { K } ^ { ( d ) } , K \subset Q _ { 0 } \} < \infty ,$$

where Q0 := [-1/2,1/2]a denotes the unit cube centred at the origin. Fundamental examples of geometric functions are the intrinsic volumes V0, . . . , Va; see Section A.3. Given a geometric function φ, we wish to apply Theorem 21.3 to the Poisson functional

$$F _ { W , \varphi } \coloneqq \varphi ( Z \cap W ) .$$

Recalling that Bd denotes the unit ball in Rd, we define V: Kd → R by

$$\bar { V } ( K ) \coloneqq \lambda _ { d } ( K \oplus B ^ { d } ) , \ \ K \in \mathcal { K } ^ { d } .$$

Clearly V is translation invariant. By the Steiner formula (A.22),  ̄ is a linear combination of the intrinsic volumes. Therefore V is continuous on K(d) and hence measurable on Kd. Throughout this section we strengthen (17.10) by assuming that

$$\int \bar { V } ( K ) ^ { 3 } \, \mathbb { Q } ( d K ) < \infty ;$$

see also Exercise 17.2.

Before stating the main result of this section, we provide two preliminary results. For a given geometric function φ it is convenient to write

$$\varphi _ { Z } ( K ) \colon = | \varphi ( K ) | + | \varphi ( Z \cap K ) | , \quad K \in \mathcal { R } ^ { d } .$$

The constants c, c1, c2, . . . appearing in the following are allowed to depend on d, Q, γ and φ, but not on anything else.

Proposition 22.4 Let φ be a geometric function. Then there is a constant c &gt; 0 such that for any K, L ∈ Kd,

$$\mathbb { E } [ \varphi _ { Z } ( K ) ^ { 2 } \varphi _ { Z } ( L ) ^ { 2 } ] \leq c \overline { V } ( K ) ^ { 2 } \overline { V } ( L ) ^ { 2 } ,$$

$$\mathbb { E } [ \varphi _ { Z } ( K ) ^ { 2 } ] \leq c \bar { V } ( K ) ^ { 2 } , \quad \mathbb { E } [ \varphi _ { Z } ( K ) ^ { 3 } ] \leq c \bar { V } ( K ) ^ { 3 } .$$


<!-- p:243 -->


Proof For z ∈ Rd we set Qz := Q0 + z. Let K ∈ K(d) and define

$$I ( K ) \colon = \{ z \in \mathbb { Z } ^ { d } \colon Q _ { z } \cap K \neq \emptyset \} .$$

By the inclusion-exclusion principle (A.30) we have

$$| \varphi ( Z \cap K ) | = \left | \varphi \left ( Z \cap K \cap \bigcup _ { z \in I ( K ) } Q _ { z } \right ) \right | \leq \sum _ { I \subseteq I ( K ) \colon I \neq 0 } \left | \varphi \left ( Z \cap K \cap \bigcap _ { z \in I } Q _ { z } \right ) \right | .$$

For each compact set C ⊂ Rd let

$$N ( C ) \coloneqq \int \mathbf 1 \{ ( M + x ) \cap C \neq \emptyset \} \, \xi ( d ( x , M ) ) \quad ( 2 2 . 2 3 )$$

denote the number of grains in {M + x : (x, M) ∈ ξ} hitting C. For each non-empty I ⊂ I(K), fix some z(I) ∈ I and let Z1, . . . , ZN(Q2() denote the grains hitting Qz(t). Then, for Ø ≠ J ⊂ {1, . . . , N(Qz(t)}, assumption (22.16) and the translation invariance of φ yield that

$$\left | \varphi ( \bigcap _ { j \in J } Z _ { j } \cap K \cap \bigcap _ { z \in I } Q _ { z } ) \right | \leq M ( \varphi ) .$$

Using the inclusion-exclusion formula again and taking into account the fact that φ(0) = 0, we obtain

$$\text {fact that $\varphi(0)=0$, we obtain} \\ | \varphi ( Z \cap K ) | & \leq \sum _ { I \subset I ( K ) \colon I \neq 0 } \left | \varphi \left ( \bigcup _ { j = 1 } ^ { N ( Q _ { s } ) } Z _ { j } \cap K \cap \bigcap _ { Q \in I } Q \right ) \right | \\ & \leq \sum _ { I \subset I ( K ) \colon I \neq 0 } \sum _ { \substack { I \cap K \subset \{ 1 , \dots , N ( Q _ { s } ) \} \colon J \neq 0 \\ I \subset I ( K ) \colon I \neq 0 } } \left | \varphi ( \bigcap _ { j \in J } Z _ { j } \cap K \cap Q ) \right | \\ & \leq \sum _ { I \subset I ( K ) \colon I \neq 0 } 1 \{ \bigcap _ { z \in I } Q _ { z } \neq 0 \} 2 ^ { N ( Q _ { s } ( n ) ) } M ( \varphi ) . \\ \text {Taking into account a similar (but simpler) bound for | \varphi ( K)| we obtain}$$

Taking into account a similar (but simpler) bound for |φ(K)| we obtain

$$| \varphi _ { Z } ( K ) | \leq \sum _ { I \subset I ( K ) \colon I \neq \emptyset } 1 \{ \bigcap _ { z \in I } Q _ { z } \neq \emptyset \} ( 2 ^ { N ( Q _ { s ( I ) } ) } + 1 ) M ( \varphi ) .$$

Exercise 22.3 shows that the expectations

$$\mathbb { E } [ ( 2 ^ { N ( Q _ { x } ) } + 1 ) ( 2 ^ { N ( Q _ { y } ) } + 1 ) ( 2 ^ { N ( Q _ { z } ) } + 1 ) ( 2 ^ { N ( Q _ { w } ) } + 1 ) ]$$

are uniformly bounded in x, y, z, w ∈ Zd. Therefore we obtain from (22.24) for each L ∈ K(d) that

$$\text {for each $L \in \mathcal{K}^{+}$ if all} \\ \mathbb { E } [ \varphi _ { Z } ( K ) ^ { 2 } \varphi _ { Z } ( L ) ^ { 2 } ] \leq c _ { 2 } \left ( \sum _ { I C ( K ) \colon I \neq 0 } \mathbf 1 \left \{ \bigcap _ { z \in I } Q _ { z } \neq 0 \right \} \right ) ^ { 2 } \left ( \sum _ { I C ( L ) \colon I \neq 0 } \mathbf 1 \left \{ \bigcap _ { z \in I } Q _ { z } \neq 0 \right \} \right ) ^ { 2 } ,$$


<!-- p:244 -->


for some c2 &gt; 0, not depending on (K, L).

A combinatorial argument (left to the reader) shows that

$$\text {card} \left \{ I \subset I ( K ) \colon I \neq \emptyset , \bigcap _ { z \in I } Q _ { z } \neq \emptyset \right \} \leq 2 ^ { 2 ^ { d } } \text { card } I ( K ) .$$

Since card I(K) ≤ Vd(K + B(0, √)), Steiner's formula (A.22) yields

$$c r d \, I ( K ) \leq \sum _ { i = 0 } ^ { d } \kappa _ { d - i } d ^ { ( d - i ) / 2 } V _ { i } ( K ) \leq c _ { 3 } \bar { V } ( K ) \\$$

for some c3 &gt; 0 depending only on d. Using this bound, together with (22.26) in (22.25), yields inequality (22.21). The inequalities (22.22) follow in the same way. □

Proposition 22.5 Let K, L ∈ Kd. Then

$$\int \bar { V } ( K \cap ( L + x ) ) \, d x \leq \bar { V } ( K ) \bar { V } ( L ) .$$

Proof For each x ∈ Rd we have the inclusion

$$( K \cap ( L + x ) ) \oplus B ^ { d } \subset ( K \oplus B ^ { d } ) \cap ( ( L + x ) \oplus B ^ { d } ) .$$

Since (L + x) ⊕ Bd = (L ⊕ Bd) + x, the result follows from (22.11).

□

Lemma 22.6 Suppose that φ is a geometric function and that K ∈ Kd. Define Fκ,φ := φ(Z ∩ K) and let n ∈ N. Then we have P-a.s. and for (λd ⊗ Q)n -a.e. ((x1, K1), . . . , (χn, Kn)) that

$$( \iota _ { n } \, \iota _ { n } \, \mathcal { Q } ) _ { \ } m a t h s c r { K } _ { n } & ) , \\ D _ { ( x _ { 1 } , K _ { 1 } ) , \dots , ( x _ { n } , K _ { n } ) } ^ { n } F _ { K , \varphi } & = ( - 1 ) ^ { n } [ \varphi ( Z \cap ( K _ { 1 } + x _ { 1 } ) \cap \cdots \cap ( K _ { n } + x _ { n } ) \cap K ) \\ & - \varphi ( ( K _ { 1 } + x _ { 1 } ) \cap \cdots \cap ( K _ { n } + x _ { n } ) \cap K ) ] .$$

Proof Let

$$\mathbb { X } \coloneqq \{ ( x , L ) \in \mathbb { R } ^ { d } \times \mathcal { K } ^ { ( d ) } \, \colon ( L + x ) \cap K \neq \emptyset \} .$$

For μ ∈ N(Rd × K(d)) we define Z(μ) := ∪(x,K)∈μ(K + x) if μ(X) &lt; ∞ and Z(μ) := ∅ otherwise. Then f(μ) := φ(Z(μ) ∩ K) defines a representative f of Fκ,φ; see the proof of Proposition 19.5. For each (x, L) ∈ Rd × K(d) we recall that Lx := L + x. By additivity of φ,

$$f ( \mu + \delta _ { ( x , L ) } ) & = \varphi ( ( Z ( \mu ) \cap K ) \cup ( L _ { x } \cap K ) ) \\ & = \varphi ( Z ( \mu ) \cap K ) + \varphi ( L _ { x } \cap K ) - \varphi ( Z ( \mu ) \cap L _ { x } \cap K ) ,$$

so that

$$D _ { ( x , L ) } f ( \mu ) = \varphi ( L _ { x } \cap K ) - \varphi ( Z ( \mu ) \cap L _ { x } \cap K ) .$$


<!-- p:245 -->


This can be iterated to yield for each (y, M) ∈ Rd × Kd that

$$D _ { ( x , L ) , ( y , M ) } ^ { 2 } f ( \mu ) = \varphi ( Z ( \mu ) \cap L _ { x } \cap M _ { y } \cap K ) - \varphi ( L _ { x } \cap M _ { y } \cap K ) .$$

Hence the assertion follows by induction.

□

We are now ready to present the main result of this section.

Theorem 22.7 Suppose that φ is a geometric function and that (22.19) holds. Assume that σw,φ := (Var[Fw,φ])1/2 &gt; 0, where Fw,φ is given by (22.17). Let fw,φ := (σw,φ)−1(Fw,φ − E[Fw,φ]). Then

$$d _ { 1 } ( \hat { F } _ { W , \varphi } , N ) \leq c _ { 1 } \sigma _ { W , \varphi } ^ { - 2 } \bar { V } ( W ) ^ { 1 / 2 } + c _ { 2 } \sigma _ { W , \varphi } ^ { - 3 } \bar { V } ( W ) ,$$

where c1, c2 do not depend on W.

Proof We intend to apply Theorem 21.3. Proposition 22.4 shows that E[F2,] &lt; ∞. Recall the definition (22.20) of φz. By Lemma 22.6 we have for (λd ⊗ Q)2-a.e. ((x, K), (y, L)) and P-a.s. that

$$| D _ { ( x , K ) } F _ { W , \varphi } | & \leq \varphi _ { Z } ( K _ { x } \cap W ) , & ( 2 2 . 3 0 ) \\ | D _ { ( x , K ) , ( y , L ) } ^ { 2 } F _ { W , \varphi } | & \leq \varphi _ { Z } ( K _ { x } \cap L _ { y } \cap W ) , & ( 2 2 . 3 1 ) \\$$

where we recall the notation Kx := K + x. By (22.30), (22.22) and Proposition 22.5,

$$\S \left ( 2 . 2 , 3 , & & \\ & \mathbb { E } \left [ \iint ( D _ { ( x , K ) } F _ { W , \varphi } ) ^ { 2 } \, d x \, \mathbb { Q } ( d K ) \right ] \leq c \bar { V } ( W ) \iint \bar { V } ( K _ { x } \cap W ) \, d x \, \mathbb { Q } ( d K ) \\ & \leq c \bar { V } ( W ) ^ { 2 } \int \bar { V } ( K ) \, \mathbb { Q } ( d K ) ,$$

which is finite by assumption (22.19). Therefore Theorem 21.3 applies.

Let σ := σw,φ and F := fw,φ. Using (22.30), (22.31) and Proposition 22.4 yields (similarly to (22.12))

$$\alpha _ { F , 1 } ^ { 2 } & \leq \frac { 4 c \gamma ^ { 3 } } { \sigma ^ { 4 } } \iint \iiint \bar { V } ( K _ { x } \cap W ) \bar { V } ( L _ { y } \cap W ) \bar { V } ( K _ { x } \cap M _ { z } \cap W ) \\ & \quad \times \bar { V } ( L _ { y } \cap M _ { z } \cap W ) \, d x \, d y \, d z \, \mathbb { Q } ^ { 3 } ( d ( K , L , M ) ) .$$

Since the function V is monotone and translation invariant we can use Proposition 22.5 to conclude as at (22.13), (22.14) and (22.15) that

$$\alpha _ { F , 1 } ^ { 2 } \leq \frac { 4 c \gamma ^ { 3 } } { \sigma ^ { 4 } } \bar { V } ( W ) \int \bar { V } ( K ) ^ { 2 } \bar { V } ( L ) ^ { 2 } \bar { V } ( M ) ^ { 2 } \mathbb { Q } ^ { 3 } ( d ( K , L , M ) ) .$$


<!-- p:246 -->


By assumption (22.19), the preceding integral is finite. The constants αF,2 can be treated in the same way. For αF,3 we obtain

$$c a n \, b e t r e d \, i n \, t h e s a m e \, w a y . \, F o r \, \alpha _ { F , 3 } \, w e \, o b t a i n \\ \alpha _ { F , 3 } & \leq \frac { \gamma } { \sigma ^ { 3 } } \iint \mathbb { E } [ \varphi _ { Z } ( K _ { x } \cap W ) ^ { 3 } ] \, d x \, \mathbb { Q } ( d K ) \\ & \leq \frac { c \gamma } { \sigma ^ { 3 } } \iint \overline { V } ( K _ { x } \cap W ) ^ { 3 } \, d x \, \mathbb { Q } ( d K ) \\ & \leq \frac { c \gamma } { \sigma ^ { 3 } } \iint \overline { V } ( K ) ^ { 2 } \overline { V } ( K _ { x } \cap W ) \, d x \, \mathbb { Q } ( d K ) \leq \frac { c \gamma \overline { V } ( W ) } { \sigma ^ { 3 } } \int \overline { V } ( K ) ^ { 3 } \, \mathbb { Q } ( d K ) , \\ \text {which is finite by assumption (22.19)} , & \quad \square$$

which is finite by assumption (22.19).

□

### 22.3 Central Limit Theorems

Recall that W is a convex compact set such that λa(W) &gt; 0. As before we define Wr := r1/dW for r &gt; 0. Then Theorem 22.7 yields a central limit theorem, provided that

$$\liminf _ { r \to \infty } r ^ { - 1 } \sigma _ { W _ { r } , \varphi } ^ { 2 } > 0 .$$

Theorem 22.8 Suppose that the assumptions of Theorem 22.7 hold and, in addition, that (22.32) holds. Then there exists č &gt; 0 such that

$$d _ { 1 } ( \hat { F } _ { W _ { r } , \varphi } , N ) \leq \bar { c } r ^ { - 1 / 2 } , \ \ r \geq 1 .$$

In particular, Ê wr,φ → N as r → ∞.

Proof By the scaling property of λd we have  ̄(Wr) = rλd(W ⊕ r−1/d Bd). Dominated convergence shows that r−1 ̄(Wr) → λd(W) as r → ∞. Therefore (22.33) is a consequence of Theorem 22.7 and assumption (22.32).

Proposition 22.1 and Exercise 22.1 show that (22.32) holds for the volume φ = Vd provided that φd &gt; 0. Finally in this chapter we prove this result in the general case.

Theorem 22.9 Assume that (22.19) holds and suppose that φ is a geometric function satisfying Q({K ∈ K(d) : φ(K) ≠ 0}) &gt; 0. Then (22.32) holds.

Proof Define a measurable function φ* : Kd → R by

$$\varphi ^ { * } ( K ) \colon = \mathbb { E } [ \varphi ( Z \cap K ) ] - \varphi ( K ) , \ \ K \in \mathcal { K } ^ { d } .$$

The stationarity of Z (Proposition 17.6) and translation invariance of φ


<!-- p:247 -->


show that φ* is translation invariant. From Theorem 18.6 and Lemma 22.6 we have for each K ∈ K(d) that

$$\text {we have for each } K \in \mathcal { K } ^ { ( d ) } \text { that} \\ \forall [ \varphi ( Z \cap K ) ] = \sum _ { n = 1 } ^ { \infty } \frac { \gamma ^ { n } } { n ! } \iint ( \mathbb { E } [ D _ { ( x _ { 1 } , K _ { 1 } ) \dots , ( x _ { n } , K _ { n } ) } ^ { n } F _ { K , \varphi } ] ) ^ { 2 } \\ \times d ( x _ { 1 } , \dots , x _ { n } ) \, \mathbb { Q } ^ { n } ( d ( K _ { 1 } , \dots , K _ { n } ) ) \\ = \sum _ { n = 1 } ^ { \infty } \frac { \gamma ^ { n } } { n ! } \iint [ \varphi ^ { * } ( ( K _ { 1 } + x _ { 1 } ) \cap \cdots \cap ( K _ { n } + x _ { n } ) \cap K ) ] ^ { 2 } \\ \times d ( x _ { 1 } , \dots , x _ { n } ) \, \mathbb { Q } ^ { n } ( d ( K _ { 1 } , \dots , K _ { n } ) ) . \quad ( 2 2 . 3 4 ) \\ \text {Therefor we obtain for each } r > 0 \text { that}$$

Therefore we obtain for each r &gt; 0 that

$$\text {Therefor we obtain for each $r > 0$ that} \\ \varbar { W } [ F _ { r , \varphi } ] & \geq \sum _ { n = 1 } ^ { \infty } \frac { \gamma ^ { n } } { n ! } \iint [ \varphi ^ { * } ( ( K _ { 1 } + x _ { 1 } ) \cap \cdots \cap ( K _ { n } + x _ { n } ) ) ] ^ { 2 } \\ & \quad \times 1 \{ K _ { 1 } + x _ { 1 } \subset W _ { r } \} \, d ( x _ { 1 } , \dots , x _ { n } ) \, \mathbb { Q } ^ { n } ( d ( K _ { 1 } , \dots , K _ { n } ) ) \\ & = \sum _ { n = 1 } ^ { \infty } \frac { \gamma ^ { n } } { n ! } \iint [ \varphi ^ { * } ( K _ { 1 } \cap ( K _ { 2 } + y _ { 2 } ) \cap \cdots \cap ( K _ { n } + y _ { n } ) ) ] ^ { 2 } \\ & \quad \times 1 \{ K _ { 1 } + y _ { 1 } \subset W _ { r } \} \, d ( y _ { 1 } , \dots , y _ { n } ) \, \mathbb { Q } ^ { n } ( d ( K _ { 1 } , \dots , K _ { n } ) ) , \\ \text {where we have used the translation invariance of $\varphi^{\ast}$ and a change of vari-}$$

where we have used the translation invariance of φ* and a change of variables. A change of variables yields for each fixed K1 ∈ K(d) that

$$r ^ { - 1 } \int \{ 1 \{ K _ { 1 } + y _ { 1 } \subset W _ { r } \} \, d y _ { 1 } = \int \{ r ^ { - 1 / d } K _ { 1 } + y \subset W \} \, d y .$$

Note that for each y in the interior of W the inclusion r−1/dK1 + y ⊂ W holds for all sufficiently large r. Fatou's lemma (Lemma A.7) shows that

$$\text { for all sufficiently large } r \colon & \text { fatou's lemma (Lemma A.7) shows that} \\ \liminf & r ^ { - 1 } \vee & \text {var} [ F _ { W , r , \varphi } ] \geq \lambda _ { d } ( W ) \int [ \varphi ^ { * } ( K _ { 1 } ) ] ^ { 2 } \, \mathbb { Q } ( d K _ { 1 } ) \\ & + \lambda _ { d } ( W ) \sum _ { n = 2 } ^ { \infty } \frac { \gamma ^ { n } } { n ! } \iint [ \varphi ^ { * } ( K _ { 1 } \cap ( K _ { 2 } + y _ { 2 } ) \cap \cdots \cap ( K _ { n } + y _ { n } ) ) ] ^ { 2 } \\ & \times d ( y _ { 2 } , \dots , y _ { n } ) \, \mathbb { Q } ^ { n } ( d ( K _ { 1 } , \dots , K _ { n } ) ) , \ ( 2 2 . 3 5 )$$

where we have used the fact that the boundary of a convex set has Lebesgue measure 0. We now assume that the left-hand side of (22.35) vanishes. Then we obtain, for all m ∈ N, (λd ⊗ Q)n-a.e. ((y1, K1), . . . , (ym, Km)) and for Q-a.e. K, that φ*(K) = 0 and

$$\varphi ^ { * } ( K \cap ( K _ { 1 } + y _ { 1 } ) \cap \cdots \cap ( K _ { m } + y _ { m } ) ) = 0 .$$


<!-- p:248 -->


Hence we obtain from (22.34) that Var[φ(Z ∩ K)] = 0 for Q-a.e. K, that is

$$\varphi ( Z \cap K ) = \mathbb { E } [ \varphi ( Z \cap K ) ] , \quad \mathbb { P } \text {-a.s., } \mathbb { Q } \text {-a.e. } K .$$

Since φ*(K) = 0 we have E[φ(Z ∩ K)] = φ(K) for Q-a.e. K. Moreover, by Theorem 17.3 and assumption (17.10), P(Z∩K = 0) &gt; 0 for each K ∈ K(a). Therefore φ(K) = φ(0) = 0 for Q-a.e. K, as asserted. □

### 22.4 Exercises

Exercise 22.1 Show that ∫ (eγβd(x) − 1) dx &gt; 0 if ∫ λd(K) Q(dK) &gt; 0.

Exercise 22.2 Show that

$$\int _ { \lambda _ { d } ( W \cap ( W + x ) ) ( e ^ { \gamma \beta _ { d } ( x ) } - 1 ) \, d x } \geq \gamma \int _ { \lambda _ { d } ( W \cap ( K + x ) ) ^ { 2 } \, d x \, \mathbb { Q } ( d K ) } .$$

Use this and Proposition 22.1 (or Exercise 18.8) to show that Var[Fw] &gt; 0 provided that φd &gt; 0.

Exercise 22.3 Let ξ be a Poisson process on Rd × C(d) with intensity measure λ = γλd ⊗ Q and suppose that (17.10) holds. Let C ⊂ Rd be compact and let Ci := C + xi for i ∈ {1, . . . , m}, where m ∈ N and x1, . . . , x ∈ Rd. For I ⊂ [m] let N1 denote the number of points (x, K) ∈ ξ such that (K + x) ∩ Ci ≠ ∅ for i ∈ I and (K + x) ∩ Ci = ∅ for i ∉ I. Show that the N are independent Poisson random variables. Use this fact to show that

$$\mathbb { E } [ 2 ^ { N ( C _ { 1 } ) } \cdots 2 ^ { N ( C _ { m } ) } ] \leq \exp \left [ 2 ^ { m } ( 2 ^ { m } - 1 ) \gamma \int \lambda _ { d } ( K \oplus C ^ { * } ) \, \mathbb { Q } ( d K ) \right ] ,$$

where C* := (−1)C and the random variables N(C) are defined by (22.23). (Hint: Use that N(C1) + · · + N(Cm) ≤ m Σ1≠0 N1.)

Exercise 22.4 Assume that (22.19) holds and suppose that φ is a geometric function such that

$$\iint | \varphi ( ( K _ { 1 } + x _ { 1 } ) \cap \cdots \cap ( K _ { n } + x _ { n } ) ) | \, d ( x _ { 1 } , \dots , x _ { n } ) \, \mathbb { Q } ^ { n } ( d ( K _ { 1 } , \dots , K _ { n } ) ) > 0$$

for some n ∈ N. Use the final part of the proof of Theorem 22.9 to show that (22.32) holds.

Exercise 22.5 Consider the point process η1 of isolated nodes in the Gilbert graph with deterministic radius s/2 based on a stationary Poisson process η with intensity γ &gt; 0; see Corollary 16.12. Let W ⊂ Rd and set F := η1(W). Show for x, y ∈ Rd that


<!-- p:249 -->


$$| D _ { x } F | \leq \eta ( B ( x , s ) \cap W ) + 1 \{ x \in W \}$$

and

$$| D _ { x , y } ^ { 2 } F | & \leq \eta ( B ( x , s ) \cap B ( y , s ) \cap W ) \\ & \quad + 2 \cdot 1 \{ \{ x , y \} \cap W \neq \emptyset \} 1 \{ \| x - y \| \leq s \} .$$

Exercise 22.6 Let W ⊂ Rd be a Borel set with 0 &lt; λd(W) &lt; ∞ such that the boundary of W has Lebesgue measure 0. Let the point process η be given as in Exercise 8.9. Show that

$$\lim _ { r \to \infty } \lambda _ { d } ( r W ) ^ { - 1 } \, \mathbb { V } a r [ \eta ( r W ) ] = \gamma ^ { 2 } \int ( \rho _ { 2 } ( x ) - 1 ) \, d x + \gamma .$$

(Hint: Use Exercises 8.9 and 17.11.)

Exercise 22.7 Let η1 be as in Exercise 22.5 and let W ∈ Ba be such that λd(W) &lt; ∞. Show that

$$\mathbb { V } a r [ \eta _ { 1 } ( W ) ] \geq \lambda _ { d } ( W ) ( \gamma e ^ { - \gamma \kappa _ { d } s ^ { d } } - \gamma ^ { 2 } \kappa _ { d } s ^ { d } e ^ { - 2 \gamma \kappa _ { d } s ^ { d } } )$$

and that ye−γkdsd − γ2κdsd e−2γκdsd &gt; 0. Assume now that λd(W) &gt; 0 and that the boundary of W has Lebesgue measure 0. Show that

$$\lim _ { r \to \infty } \lambda _ { d } ( r W ) ^ { - 1 } \, \mathbb { W } & \, [ \eta _ { 1 } ( r W ) ] = \gamma e ^ { - \gamma \kappa _ { d } s ^ { d } } - \gamma ^ { 2 } \kappa _ { d } s ^ { d } e ^ { - 2 \gamma \kappa _ { d } s ^ { d } } \\ & + \gamma ^ { 2 } e ^ { - 2 \gamma \kappa _ { d } s ^ { d } } \int 1 \{ s < \| x \| \leq 2 s \} ( \exp [ \gamma \lambda _ { d } ( B ( 0 , s ) \cap B ( x , s ) ) ] - 1 ) \, d x . \\ ( H i n t \, \text {Combine Exercises 8 9 and 22 6 with Corollary 16 1 2 ) }$$

(Hint: Combine Exercises 8.9 and22.6 with Corollary 16.12.)

Exercise 22.8 Let η1 be as in Exercise 22.5 and let W ⊂ Rd be a compact set with λd(W) &gt; 0. Let η1(W) := Var[η1(W)]−1(η1(W) − E[η1(W)]). Show that

$$d _ { 1 } ( \hat { \eta } _ { 1 } ( W ) , N ) \leq c _ { 1 } \lambda _ { d } ( W _ { \oplus s } ) ^ { 1 / 2 } \lambda _ { d } ( W ) ^ { - 1 } + c _ { 2 } \lambda _ { d } ( W _ { \oplus s } ) \lambda _ { d } ( W ) ^ { - 3 / 2 } ,$$

where W⊕s := W ⊕ B(O, s) and c1, c2 &gt; 0 do not depend on W. (Hint: Use Theorem 21.3, Exercise 22.5 and Exercise 22.7.)

Exercise 22.9 Let η1 be as in Exercise 22.5 and let W ⊂ Rd be a compact convex set with λd(W) &gt; 0. Show that η1(rW) → N as r → ∞, where η1(rW) is defined as in Exercise 22.8. (Hint: Use Exercise 22.8 and the Steiner formula (A.22).)


<!-- p:250 -->


## Appendix A

## Some Measure Theory

### A.1 General Measure Theory

We assume that the reader is familiar with measure theory but provide here the basic concepts and results. More detail can be found in [13, 16, 30, 63].

Given a function (mapping) f from a set X to a set Y, we write f : X → Y and denote by f(x) the value of f at x. Let f and g be functions from X to the extended real line R := [−∞, +∞]. We often write {f ≤ g} := {x ∈ X : f(x) ≤ g(x)}. Similarly we define {f ≤ a, g ≤ b} (for a, b ∈ R) and other sets of this type. Using the convention 0∞ = ∞0 = 0(−∞) = (−∞)0 = 0 we may define the product f g pointwise by (f g)(x) := f(x)g(x). Similarly, we define the function f + g, whenever the sets {f = -∞, g = ∞} and {f = ∞, g = -∞} are empty. Here we use the common rules for calculating with ∞ and -∞. Let 1 denote the indicator function of A on X taking the value one on A and zero on X \ A. Given f : A → R, we do not hesitate to interpret 1Af as a function on X with the obvious definition. Then the equality 1Af = g means that f and g agree on A (i.e. f(x) = g(x) for all x ∈ A) and g vanishes outside A. Sometimes it is convenient to write 1{x : x ∈ A} instead of 1A and 1{x ∈ A} instead of 1A(x).

In what follows all sets under consideration will be subsets of a fixed set Ω. A class H of sets is said to be closed with respect to finite intersections if A ∩ B ∈ H whenever A, B ∈ H. In this case one also says that H is a πsystem. One defines similarly the notion of H being closed with respect to countable intersections, or closed with respect to finite unions, and so on. A class A of sets is called a field (on Ω) if, firstly, Ω ∈ A and, secondly, A, B ∈ A implies that A \ B ∈ A and A ∪ B ∈ A, that is A is closed with respect to finite unions and set differences. A field A that is closed with respect to countable unions (or, equivalently, countable intersections) is called a σ-field. The symbol σ(H) denotes the σ-field generated by H, i.e. the smallest σ-field containing H. In this case H is called a generator of σ(H). A class D of sets is called a monotone system if it is closed with respect to countable increasing unions and with respect to countable decreasing intersections, i.e. An ⊂ An+1, An ∈ D, implies ∪n=1 An ∈ D and An ⊃ An+1, An ∈ D, implies ∩n=1 An ∈ D. Thus, a field D is a σ-field if it is monotone. A class D of sets is called a Dynkin system (also known as a λ-system) if Ω ∈ D and if it is closed with respect to countable increasing unions and it is closed with respect to proper differences, i.e. if A, B ∈ D with A ⊂ B implies B \ A ∈ D. In this case D is a monotone system. The following theorem is a well-known version of a so-called monotone class theorem. If nothing else is stated then all definitions and theorems in this chapter can be found in [63], which is our basic reference for measure and probability theory.


<!-- p:251 -->


Theorem A.1 (Monotone class theorem) Let H and D be classes of subsets of Ω satisfying H ⊂ D. Suppose that H is a π-system and that D is a Dynkin system. Then σ(H) ⊂ D.

Later in this appendix we use the following version of the monotone class theorem (see e.g. Th. 4.4.2 in [30]).

Theorem A.2 (Monotone class theorem) Let A and M be classes of subsets of Ω with A ⊂ M. Suppose that A is a field and that M is a monotone system. Then σ(A) ⊂ M.

Let n ∈ N and let B1, . . . , Bn ⊂ Ω. Define A := σ({B1, . . . , Bn}). An atom of A is a non-empty set in the field A having no non-empty proper subset in the field. The atoms of the field are the non-empty sets of the form Bi1 ∩ . . ∩ Bn , where i1, . . . , in ∈ {0, 1} and, for B ⊂ X, B1 := B and B0 := X \ B. Every non-empty set in A is a union of some atoms.

A measurable space is a pair (X, X), where X is a set and X is a σfield of subsets of X. Let (X, X) be a measurable space and let f be a mapping from Ω into X. If F is a σ-field on Ω, then f is said to be F-Xmeasurable if f−1(X) ⊂ F, where f−1(X) := {f−1(B) : B ∈ X}. If there is no risk of ambiguity, we will also speak of F-measurability or, simply, of measurability. The σ-field σ(f) generated by f is the smallest σ-field G such that f is G-X-measurable; it is given by f−1(X). If X = R and nothing else is said, then X will always be given by the σ-field B(R) on R, which is generated by the system of open sets in R along with {-∞} and {+∞}. This is the Borel σ-field on R; see Section A.2. More generally, if X ∈ B(R), then we shall take X as the trace σ-field {B ∩ X : B ∈ B(R)}; see Section A.2. Now let F be fixed. Then we denote by R(Ω) the set of all measurable functions from Ω to R. The symbols R+(Ω) and R+(Ω) denote the set of [0, ∞]-valued (resp. [0, ∞)-valued) functions in R(Ω).


<!-- p:252 -->


Theorem A.3 Let f be a mapping from Ω into a measurable space (X, X) and let g be an R-valued function on Ω. Then g is σ(f)-measurable if and only if there exists an R-valued measurable function h from X into R such that g = h o f.

If G is a class of functions from Ω into X, then we denote by σ(G) the smallest σ-field A on Ω such that f is A-X-measurable for all f ∈ G. It is given by σ{f−1(B) : f ∈ G, B ∈ X}. The next theorem is a functional version of the monotone class theorem; see Th. 2.12.9 in [16].

Theorem A.4 Let W be a vector space of R-valued bounded functions on Ω that contains the constant functions. Further, suppose that, for every increasing sequence of non-negative functions fn ∈ W, n ∈ N, satisfying sup{|fn(ω)| : n ∈ N, ω ∈ Ω} &lt; ∞, the function f = limn→∞ fn belongs to W. Assume also that W is closed under uniform convergence. Let G be a subset of W that is closed with respect to multiplication. Then W contains all bounded σ(G)-measurable functions on Ω.

It is possible to show that the final assumption made on W in Theorem A.4 can be dropped.

Let (X, X) and (Y, Y) be two measurable spaces. When X and Y are fixed and nothing else is said, measurability on X × Y always refers to the product σ-field X ø Y generated by all sets of the form A × B with A ∈ X and B ∈ Y. The measurable space (X × Y, X ⊗ Y) is called the product of (X, X) and (Y, Y). Given a finite number (X1, X1), . . . , (X, X) of measurable spaces we can define the product (X1 ×· · · ×X, X1⊗· · ·∅Xn) in a similar way. In the case where (X, X) = (X, X) for every i ∈ {1, . . . , n} we abbreviate this product as (Xn, Xn) and refer to it as the n-th power of (X, X). Let (X, X), i ∈ N, be a countable collection of measurable spaces. The infinite product ∅i=1X is the σ-field on ×i=1X generated by the sets

$$B _ { 1 } \times \cdots \times B _ { n } \times \bigcup _ { i = n + 1 } ^ { \infty } \mathbb { X } _ { i } ,$$

where B ∈ X for i ∈ {1, . . . , n} and n ∈ N.

Let (X, X) be a measurable space. A function λ: X → [0, ∞] is said to be additive if λ(B ∪ B′) = λ(B) + λ(B') for all disjoint B, B′ ∈ X. In this case λ is finitely additive in the obvious sense. A measure on a measurable space (X, X) is a function λ: X → [0, ∞] such that λ(0) = 0 and such that λ is σ-additive (countably additive), that is

$$\lambda \left ( \bigcup _ { n = 1 } ^ { \infty } B _ { n } \right ) = \sum _ { n = 1 } ^ { \infty } \lambda ( B _ { n } ) ,$$


<!-- p:253 -->


whenever B1, B2, . . . are pairwise disjoint sets in X. In this case the triple (X, X, λ) is called a measure space. For simplicity we sometimes speak of a measure on X. A measure λ on (X, X) is said to be σ-finite if there are sets Bn ∈ X, n ∈ N, such that ∪n=1Bn = X and λ(Bn) &lt; ∞ for all n ∈ N. In this case we say that (X, X, λ) is a σ-finite measure space. The counting measure on (X, X) supported by a set A ⊂ X is the measure B ↔ card(A ∩ B), where card B denotes the number of elements of a set B. If, for instance, (X, X) = (R, B(R)) with B(R) generated by the open sets, then this measure is σ-finite if and only if A is finite or countably infinite.

The following result can easily be proved using Theorem A.1.

Theorem A.5 Let μ, v be measures on (X, X). Assume that μ and v agree on a π-system H with σ(H) = X. Assume moreover that there is an increasing sequence B ∈ H, n ∈ N, such that μ(B) &lt; ∞ for all n ∈ N and ∪n=1Bn = X. Then μ = v.

Let (X, X, λ) be a measure space. The integral ∫ f dλ of f ∈ R+(X) with respect to λ is defined as follows. If f is simple, that is of the form

$$f = \sum _ { i = 1 } ^ { m } c _ { i } 1 _ { B _ { i } }$$

for some m ∈ N, c1, . . , cm ∈ R+ and B1, . . . , Bm ∈ X, then

$$\int f \, d \lambda \colon = \sum _ { i = 1 } ^ { m } c _ { i } \lambda ( B _ { i } ) .$$

Any f ∈ R+(X) is the limit of simple functions fn given, for n ∈ N, by

$$f _ { n } ( x ) \colon = n 1 \{ n \leq f ( x ) \} + \sum _ { j = 1 } ^ { n ^ { 2 ^ { n - 1 } } } j 2 ^ { - n } 1 \{ j 2 ^ { - n } \leq f ( x ) < ( j + 1 ) 2 ^ { - n } \} ,$$

and one defines ∫ f dλ as the finite or infinite limit of ∫ f dλ. To extend the integral to f ∈ R(X) we define

$$\int f \, d \lambda = \int f ^ { + } \, d \lambda - \int f ^ { - } \, d \lambda$$

whenever one of the integrals on the right-hand side is finite. Here

$$f ^ { + } ( x ) \colon = f ( x ) \vee 0 , \ \ f ^ { - } ( x ) \colon = - ( f ( x ) \wedge 0 ) ,$$

and a V b (resp. a ∧ b) denotes the maximum (minimum) of two numbers a, b ∈ R. For definiteness we put ∫ f dλ := 0 in the case ∫ f+ dλ =


<!-- p:254 -->


∫ f− dλ = ∞. Sometimes we abbreviate λ(f) := ∫ f dλ. For B ∈ X one writes ∫B f dλ := λ(1Bf).

Given measurable functions f, g ∈ R(X), we write f ≤ g, λ-almost everywhere (short: λ-a.e.) if λ({f &gt; g}) = 0. We also write f(x) ≤ g(x), λ-a.e. x ∈ X. Similar notation is used for other measurable relationships.

Given p &gt; 0 let LP(λ) = {f ∈ R(X) : λ(|.f|P) &lt; ∞}. The mapping f ↔ λ(f) is linear on L1(λ) and satisfies the triangle inequality |λ(f)| ≤ λ(|fl). If f ≥ 0, λ-a.e. (that is, λ({f &lt; 0}) = 0) then λ(f) = 0 implies that f = 0, λ-a.e.

The next results show that the integral has nice continuity properties.

Theorem A.6 (Monotone convergence) Let fn ∈ R+(X), n ∈ N, be such that fn ↑ f (pointwise) for some f ∈ R+(X). Then λ(fn) ↑ λ(f).

Lemma A.7 (Fatou's lemma) Let fn ∈ R+(X), n ∈ N. Then

$$\liminf _ { n \to \infty } \lambda ( f _ { n } ) \geq \lambda ( \liminf _ { n \to \infty } f _ { n } ) .$$

Theorem A.8 (Dominated convergence) Let fn ∈ R+(X), n ∈ N, be such that fn → f (pointwise) for some f ∈ R+(X) and |fn| ≤ g (pointwise) for some g ∈ L1(λ). Then λ(fn) → λ(f).

Suppose that p, q &gt; 1 with 1/p + 1/q = 1. Let f ∈ LP(λ) and g ∈ La(λ). Hölder's inequality says that then

$$\int | f g | d \lambda \leq \left ( \int | f | ^ { p } \, d \lambda \right ) ^ { 1 / p } \left ( \int | f | ^ { p } \, d \lambda \right ) ^ { 1 / q } .$$

In the special case p = q = 2 this is known as the Cauchy-Schwarz inequality. Hölder's inequality can be generalised to

$$p _ { i } \, d \lambda \right ) ^ { 1 / p _ { i } }$$

whenever m ∈ N, p1, . . , Pm are positive numbers with 1/p1+· · .+1/pm = 1 and fi ∈ LPi(λ) for i ∈ {1, . . . , m}.

Let p &gt; 1. A quick consequence of (A.2) is the Minkowski inequality

$$\left ( \int | f + g | ^ { p } \, d \lambda \right ) ^ { 1 / p } \leq \left ( \int | f | ^ { p } \, d \lambda \right ) ^ { 1 / p } + \left ( \int | g | ^ { p } \, d \lambda \right ) ^ { 1 / p } , \quad f , g \in L ^ { p } ( \lambda ) .$$

Identifying f, f ∈ LP(λ) whenever λ({f ≠ f}) = 0, and giving f the norm ( f\f| dλ)1/p, LP(λ) becomes a normed vector space. A remarkable feature of this space is its completeness. This means that if (fn) is a Cauchy


<!-- p:255 -->


3 f     =  dl f – "f f ∞←  t (d  s LP(λ) such that lim→∞ fn = f in LP(λ), that is lim→∞ ∫ I.fn − f|P dλ = 0.

Let λ, ν be measures on (X, X). If v(B) = 0 for all B ∈ X with λ(B) = 0, then v is said to be absolutely continuous with respect to λ and one writes ν « λ. The two measures v and λ are said to be mutually singular if there exists some A ∈ X such that v(A) = λ(X \ A) = 0. A finite signed measure (on X or (X, X)) is a σ-additive bounded function v: X → R.

Theorem A.9 (Hahn-Jordan decomposition) Let v be a finite signed measure on X. Then there exist uniquely determined mutually singular finite measures ν+ and v\_ such that ν = ν+ − ν\_.

Theorem A.10 (Radon–Nikodým theorem) Let λ, v be σ-finite measures on (X, X) such that ν « λ. Then there exists f ∈ R+(X) such that

$$\nu ( B ) = \int _ { B } f \, d \lambda , \ \ B \in \mathcal { X } .$$

The function f in (A.4) is called the Radon–Nikodým derivative (or density) of v with respect to λ. We write ν = f λ. If g is another such function then f = g, λ-a.e., that is λ({f ≠ g}) = 0.

We need to integrate with respect to a finite signed measure v on (X, X). For f ∈ R(X) we define

$$\int f \, d \nu \colon = \int f \, d \nu _ { + } - \int f \, d \nu _ { - } \\ \dot { \cdot } _ { 0 } \cdot \dot { \cdot } _ { 1 } = 0$$

whenever this expression is well defined. This can be written as an ordinary integral as follows. Let ρ be a finite measure such that ν\_  ρ and v+  ρ; let h\_ and h denote the corresponding Radon-Nikodým derivatives. Then

$$\int f d \nu = \int f ( h _ { + } - h _ { - } ) \, d \rho ,$$

where the values -∞ and ∞ are allowed. A natural choice is ρ = v+ + v\_. This is called the total variation measure of v.

Any countable sum of measures is a measure. A measure λ is said to be s-finite if

$$\lambda = \sum _ { n = 1 } ^ { \infty } \lambda _ { n } & & ( A . 6 )$$

is a countable sum of finite measures λ. Given f ∈ R+(X) we then have

$$\int f d \lambda = \sum _ { n = 1 } ^ { \infty } \int f \, d \lambda _ { n } .$$


<!-- p:256 -->


This remains true for f ∈ L1(λ). Any σ-finite measure is s-finite. The converse is not true. If μ is a measure on (X, X) such that μ(X) &lt; ∞ we can define a measure ν by multiplying μ by infinity. (Recall that 0 · ∞ = 0.) Then ν(B) = 0 if μ(B) = 0 and ν(B) = ∞ otherwise. If μ(X) &gt; 0 then ν is s-finite but not σ-finite. If the measure v is of this form, i.e. if ν = ∞ · μ for some finite measure μ on X with μ(X) &gt; 0, then we say that v is totally infinite. The sum of a σ-finite and a totally infinite measure is s-finite. The converse is also true:

Theorem A.11 Let λ be an s-finite measure on X. Then there exist a σ-finite measure λ' and a measure λ" such that λ' and χ" are mutually singular, λ = λ' + λ" and λ" is either totally infinite or the zero measure.

Proof Assume that λ is given as in (A.6) and let v be a finite measure such that λ « ν for all n ∈ N. (The construction of v is left as an exercise.) By Theorem A.10 there are fn ∈ R+(X) such that λn = fnν, i.e. λ(B) = v(1Bfn) for all B ∈ X. Define f := ∑n=1 fn. Then f is a measurable function from X to [0, ∞] and, by Theorem A.6 (monotone convergence), λ = fv. It is easy (   ←    {∞ &gt; f} =:         ) is σ-finite. Moreover, if v(X \ A) &gt; 0, then by the definition of integrals the restriction of λ to X \ A is totally infinite. □

Suppose λ is an s-finite measure, given by (A.6). Then vn := Σnj=1 λj ↑ λ, in the sense that vn(B) ≤ νn+1(B) for all n ∈ N and all B ∈ X and νn(B) → λ(B) as n → ∞. We use this notation also for general measures. Theorem A.6 on monotone convergence can be generalised as follows.

Theorem A.12 Let vn, n ∈ N, be measures on X such that vn ↑ v for some measure v. Assume also that fn ∈ R(X), n ∈ N, satisfy vn({fn &lt; 0}) = 0, n ∈ N, and fn ↑ f for some f ∈ R(X). Then vn(fn) ↑ v(f).

Proof For all n ∈ N we have vn({f &lt; 0}) ≤ νn({fn &lt; 0}) = 0 and hence v({f &lt; 0}) = 0. Assume v({f &gt; 0}) &gt; 0. (Else we have for each n ∈ N that v({f ≠ 0}) = v({fn ≠ 0}) = 0 and there is nothing to prove.) Let c ∈ (0, v(f)). Then there exists a simple g ∈ R+(X) with g ≤ f+ such that v(g) &gt; c. Next we can pick n ∈ N with νn(g) &gt; c and then m0 ≥ n wt                 (f  it νm(fm) ≥ vn(fm) &gt; c, and the result follows. □

Let λ be an s-finite measure on (X, X). Then (X, X, λ) is said to be an s-finite measure space. Let (Y, Y) be an additional measurable space. If f ∈ R(X × Y), then y ↔ ∫ f(x, y) λ(dx) is a measurable function on Y. Hence, if ν is a measure on (Y, Y) we can form the double integral


<!-- p:257 -->


∫∫f f(x, y) λ(dx) v(dy). In particular, we can define the product measure λøv as the measure on (X × Y, X ⊗ Y) given by

$$( \lambda \otimes \nu ) ( A ) \colon = \iint \mathbf 1 _ { A } ( x , y ) \, \lambda ( d x ) \, \nu ( d y ) , \quad A \in \mathcal { X } \otimes \mathcal { Y } . \quad ( A . 8 )$$

If v is also s-finite, and given as the sum of finite measures vm, m ∈ N, then (A.7) and monotone convergence (Theorem A.6) show that

$$\lambda \otimes \nu = \sum _ { n , m \in \mathbb { N } } \lambda _ { n } \otimes \nu _ { m } .$$

In particular, λøv is s-finite. The product is linear with respect to countable sums and therefore also associative.

Theorem A.13 (Fubini's theorem) Let (X, X, λ) and (Y, Y, ν) be two sfinite measure spaces and let f ∈ R+(X × Y). Then

$$\iint f ( x , y ) \, \lambda ( d x ) \, \nu ( d y ) = \iint f ( x , y ) \, \nu ( d y ) \, \lambda ( d x ) \\$$

and both integrals coincide with (λ ⊗ v)(f). These assertions remain true for all f ∈ L1(λ ∅ ν).

If λ and v are σ-finite, then λ ø ν is σ-finite and uniquely determined by

$$( \lambda \otimes \nu ) ( B \times C ) = \lambda ( B ) \nu ( C ) , \quad B \in \mathcal { X } , C \in \mathcal { Y } .$$

In this case the proof of Fubini's theorem can be found in the textbooks. The s-finite case can be derived by using the formula (A.7) for both λ and v and then applying Fubini's theorem in the case of two finite measures.

Let us now consider s-finite measure spaces (X, Xi, λ), i ∈ {1, . . . , n}, for some n ≥ 2. Then the product ∅=1 λi of λ1, . . , λ is an s-finite measure on (×n=1Xi, ∅i=1Xi), defined inductively in the obvious way. Of particular importance is the case (Xi, Xi, λi) = (X, X, λ) for all i ∈ {1, . . . , n}. Then we write λn := ⊗=1λi and call this the n-th power of λ. The power vn can also be defined for a finite signed measure v. Similarly to (A.5) we have for f ∈ R(Xn) that

$$\int f d \nu ^ { n } = \int f ( h _ { + } - h _ { - } ) ^ { \otimes n } \, d | \nu | ,$$

where the tensor product (h+ – h\_)®n is defined by (18.6).

A kernel from (X, X) to (Y, Y) (or abbreviated: from X to Y) is a mapping K from X × Y to R+ such that K(·, A) is X-measurable for all A ∈ y and such that K(x, ·) is a measure on Y for all x ∈ X. It is called a probability kernel (resp. sub-probability kernel) if K(x, Y) = 1 (≤ 1) for all x ∈ X. A countable sum of kernels is again a kernel. A countable sum of sub-probability kernels is called an s-finite kernel. If K is an s-finite kernel and f ∈ R(X × Y) then x ↔ ∫ f(x, y) K(x, dy) is a measurable function. If, in addition, λ is an s-finite measure on (X, X), then


<!-- p:258 -->


$$( \lambda \otimes K ) ( A ) \colon = \iint \mathbf 1 _ { A } ( x , y ) \, K ( x , d y ) \, \lambda ( d x ) , \quad A \in \mathcal { X } \otimes \mathcal { Y } ,$$

defines an s-finite measure λ ⊗ K on (X × Y, X ⊗ Y).

For the next result we recall from Definition 6.1 the concept of a Borel space.

Theorem A.14 (Disintegration theorem) Suppose that (X, X) is a measurable space and that (Y, Y) is a Borel space. Let ν be a measure on (X × Y, X ∅ Y) such that λ := v(· × Y) is σ-finite. Then there exists a probability kernel K from X to Y such that v = λ ø K.

In the remainder of this section we prove Proposition 4.3. To this end we need some notation and auxiliary results. Let N&lt;∞ denote the set of all μ ∈ N := N(X) with μ(X) &lt; ∞. For μ ∈ N&lt;∞ the recursion (4.9) is solved by

$$\mu ^ { ( m ) } = \int \cdots \int 1 \{ ( x _ { 1 } , \dots , x _ { m } ) \in \cdot \} \left ( \mu - \sum _ { j = 1 } ^ { m - 1 } \delta _ { x _ { j } } \right ) ( d x _ { m } ) \cdots \mu ( d x _ { 1 } ) , \quad ( A . 1 2 )$$

where the integrations are with respect to finite signed measures. Note that μ(m) is a signed measure such that μ(m)(C) ∈ Z for all C ∈ Xm. At this stage it might not be obvious that μ(m)(C) ≥ 0. If, however, μ is given by (4.3) with k ∈ N, then Lemma 4.2 shows that (A.12) coincides with (4.4). Hence μ(m) is a measure in this case. For each μ ∈ N&lt;∞ we denote by μ(m) the signed measure (A.12). This is in accordance with the recursion (4.9). The next lemma is our main tool for proving Proposition 4.3.

Lemma A.15 Let n ∈ N and B1, . . . , B ∈ X. Let A be the field generated by these sets and let μ ∈ N&lt;∞. Then there exists a finite sum μ' of Dirac measures such that μ(m)(B) = (μ′)(m)(B) for each m ∈ N and each B ∈ An.

Proof Let A0 denote the set of all atoms of A. For A ∈ A0 we take xA ∈ A and set

$$\mu ^ { \prime } \colon = \sum _ { A \in \mathcal { R } _ { 0 } } \mu ( A ) \delta _ { x _ { A } } .$$

Since μ(X) &lt; ∞ and μ(A) ∈ N0 for each A ∈ A0, this is a finite sum of Dirac measures. By definition, μ and μ' coincide on A0 and hence by additivity also on A. To prove that μ(m) = (μ')(m) on An for m ∈ N it is by additivity sufficient to show that


<!-- p:259 -->


$$\mu ^ { ( m ) } ( A _ { 1 } \times \dots \times A _ { m } ) = ( \mu ^ { \prime } ) ^ { ( m ) } ( A _ { 1 } \times \dots \times A _ { m } )$$

holds for all m ∈ N and all A1, . . . , A ∈ A. By the recursion (4.9) we have for each m ∈ N and all A1, . . . , Am+1 ∈ A that

$$\mu ^ { ( m + 1 ) } ( A _ { 1 } \times \dots \times A _ { m + 1 } ) & = \mu ( A _ { m + 1 } ) \mu ^ { ( m ) } ( A _ { 1 } \times \dots \times A _ { m } ) \\ & - \sum _ { j = 1 } ^ { m } \mu ^ { ( m ) } ( A _ { 1 } \times \dots \times A _ { j } \cap A _ { m + 1 } \times \dots \times A _ { m } ) ,$$

so that (A.13) follows by induction.

□

Now we can show that μ(m) is a measure for μ ∈ N&lt;∞ and m ∈ N.

Lemma A.16 Let μ ∈ N&lt;∞ and m ∈ N. Then μ(m)(C) ≥ 0 for all C ∈ Xm.

Proof Given B1, . . . , Bm ∈ X we assert that μ(m)(B1 × · . · × Bm) ≥ 0. To see this, we apply Lemma A.15 in the case n = m. By (4.4) (applied to μ') we have (μ′)(m)(B1 × · ·  × B) ≥ 0 and hence the assertion.

Let A be the system of all finite disjoint unions of sets of the form C1 × · · · × Cm, with C1, . . . , Cm ∈ X. This is a field; see Prop. 3.2.3 in [30]. From the first step of the proof and additivity of μ(m) we deduce that μ(m)(A) ≥ 0 holds for all A ∈ A. The system M of all sets A ∈ Xm with the property that μ(m)(A) ≥ 0 is closed with respect to (countable) monotone unions and intersections. Hence Theorem A.2 implies that M = Xm. Therefore μ(m) is non-negative. □

Lemma A.17 Let μ, v ∈ N&lt;∞ with μ ≤ ν. Let m ∈ N. Then μ(m) ≤ v(m).

Proof By Theorem A.2 it suffices to show that

$$\mu ^ { ( m ) } ( B _ { 1 } \times \cdots \times B _ { m } ) \leq \nu ^ { ( m ) } ( B _ { 1 } \times \cdots \times B _ { m } )$$

for all B1, . . ., B ∈ X. Fixing the latter sets we apply Lemma A.15 to both μ and v to obtain finite sums μ' and v' of Dirac measures with the stated properties. Since μ ≤ ν we have μ' ≤ v'. Therefore (4.4) (applied to μ′ and v′) yields (μμ')(m) ≤ (v′)(m) and hence the asserted inequality (A.14). □

We are now in a position to prove a slightly more detailed version of Proposition 4.3.

Proposition A.18 For each μ ∈ N there is a sequence μ(m), m ∈ N, of measures on (X, X) satisfying μ(1) := μ and the recursion (4.9). Moreover, the mapping μ → μ(m) is measurable. Finally, if μn ↑ μ for a sequence (μ) of finite measures in N, then (μ)(m) ↑ μ(m).


<!-- p:260 -->


Proof For μ ∈ N&lt;∞ the functions defined by (A.12) satisfy the recursion (4.9) and are measures by Lemma A.16.

For general μ ∈ N we proceed by induction. For m = 1 we have μ(1) = μ and there is nothing to prove. Assume now that m ≥ 1 and that the measures μ(1), . . . , μ(m) satisfy the first m – 1 recursions and have the properties stated in the proposition. Then (4.9) forces the definition

$$\mu ^ { ( m + 1 ) } ( C ) \colon = \int K ( x _ { 1 } , \dots , x _ { m } , \mu , C ) \, \mu ^ { ( m ) } ( d ( x _ { 1 } , \dots , x _ { m } ) )$$

for C ∈ Xm+1, where

$$K ( x _ { 1 } , \dots , x _ { m } , \mu , C ) \\ \vdots = \int 1 \{ ( x _ { 1 } , \dots , x _ { m + 1 } ) \in C \} \mu ( d x _ { m + 1 } ) - \sum _ { j = 1 } ^ { m } 1 \{ ( x _ { 1 } , \dots , x _ { m } , x _ { j } ) \in C \} . \\ \\ \text {The function } K _ { \ } \mathbb { W } _ { m } \cup N _ { \ } Y m \ \ Y m _ { \ } \mu ( x _ { j } , x _ { m } ) \in \intertext { The function } K ( x _ { 1 } , \dots , x _ { m } , \mu ) \ \colon$$

The function K: Xn × N × Xn → (−∞, ∞] is a signed kernel in the following sense. The mapping (x1, . . , Xm, μ) ↔ K(x1, . . . , χm, μ, C) is measurable for all C ∈ Xm+1, while K(x1, . .. , xm, μ, ·) is σ-additive for all (x1, . . . , Xm, μ) ∈ Xn × N. Hence it follows from (A.15) and the measurability properties of μ(m) (which are part of the induction hypothesis) that μ(m+1)(C) is a measurable function of μ.

Next we show that

$$K ( x _ { 1 } , \dots , x _ { m } , \mu , C ) \geq 0 , \quad \mu ^ { ( m ) } \text {-a.e. ( } x _ { 1 } , \dots , x _ { m } ) \in \mathbb { X } ^ { m }$$

holds for all μ ∈ N and all C ∈ Xm+1. Since μ(m) is a measure (by the induction hypothesis), (A.15), (A.16) and monotone convergence then imply that μ(m+1) is a measure. Fix μ ∈ N. By definition of N we can choose a seu      r t ns  e  i  (r ne to μ and m + 1) shows that

$$K ( x _ { 1 } , \dots , x _ { m } , \mu _ { n } , C ) \geq 0 , \quad ( \mu _ { n } ) ^ { ( m ) } \text {-a.e. ( } x _ { 1 } , \dots , x _ { m } ) \in \mathbb { X } ^ { m } , \, n \in \mathbb { N } .$$

Indeed, we have for all B ∈ Xm that

$$\int _ { B } K ( x _ { 1 } , \dots , x _ { m } , \mu _ { n } , C ) \left ( \mu _ { n } \right ) ^ { ( m ) } ( d ( x _ { 1 } , \dots , x _ { m } ) ) = ( \mu _ { n } ) ^ { ( m + 1 ) } ( ( B \times \mathbb { X } ) \cap C ) \geq 0 .$$

Since K(x1, . . . , xm, ·, C) is increasing, this implies that

$$K ( x _ { 1 } , \dots , x _ { m } , \mu , C ) \geq 0 , \ \ ( \mu _ { n } ) ^ { ( m ) } \text {-a.e. ( } x _ { 1 } , \dots , x _ { m } ) \in \mathbb { X } ^ { m } , \ n \in \mathbb { N } .$$


<!-- p:261 -->


By the induction hypothesis we have that (μ)(m) ↑ μ(m) so that (A.16) follows.

To finish the induction we take μ ∈ N and μn ∈ N&lt;∞, n ∈ N, as above. We need to show that (μn)(m+1)(C) ↑ μ(m+1)(C) for each C ∈ χn+1. For each n ∈ N, let us define a measurable function fn : Xn → (−∞, ∞] by fn(x1, . . . , xm) := K(x1, . . . , xm, μ, C). Then fn ↑ f, where the function f is given by f(x1, . . . , xm) := K(x1, . . . , xm, μ, C). Hence we can apply Theorem A.12 (and (A.15)) to obtain

$$( \mu _ { n } ) ^ { ( m + 1 ) } ( C ) = ( \mu _ { n } ) ^ { ( m ) } ( f _ { n } ) \uparrow \mu ^ { ( m ) } ( f ) = \mu ^ { ( m + 1 ) } ( C ) .$$

This finishes the proof.

□

For each μ ∈ N and each m ∈ N the measure μ(m) is symmetric, that is

$$\int f ( x _ { 1 } , \dots , x _ { m } ) \mu ^ { ( m ) } ( d ( x _ { 1 } , \dots , x _ { m } ) ) \\ = \int f ( x _ { \pi ( 1 ) } , \dots , x _ { \pi ( m ) } ) \mu ^ { ( m ) } ( d ( x _ { 1 } , \dots , x _ { m } ) ) \\ \quad \ \ ( A . 1 7 ) \\ \int f \in \mathbb { R } \ \mathbb { C } ^ { m } \text { } \text { and all bijective mappings } \pi \text { from } [ m ] \coloneqq \{ 1 \, \quad m \} \text { to }$$

for each f ∈ R+ (Xm) and all bijective mappings π from [m] := {1, . . . , m} to [m]. To see this, we may first assume that μ(X) &lt; ∞. If f is the product of indicator functions, then (A.17) is implied by Lemma A.15 and (4.4). The case of a general f ∈ R+(Xn) follows by a monotone class argument. For a general μ ∈ N we can use the final assertion of Proposition A.18. Product measures λn yield other examples of measures satisfying (A.17).

### A.2 Metric Spaces

A metric on a set X is a symmetric function ρ: X × X → R+ satisfying ρ(x, y) = 0 if and only if x = y and the triangle inequality

$$\rho ( x , y ) \leq \rho ( x , z ) + \rho ( z , y ) , \quad x , y , z \in \mathbb { X } .$$

Then the pair (X, ρ) is called a metric space. A sequence x ∈ X, n ∈ N, converges to x ∈ X if lim→∞ ρ(xn, x) = 0. The closed ball with centre x0 ∈ X and radius r ≥ 0 is defined by

$$B ( x _ { 0 } , r ) \colon = \{ x \in \mathbb { X } \colon \rho ( x , x _ { 0 } ) \leq r \} .$$

A set U ⊂ X is said to be open if for each x0 ∈ U there exists ε &gt; 0 such that B(x0, ε) ⊂ U. A set F ⊂ X is said to be closed if its complement X \ F is open. The closure of a set B ⊂ X is the smallest closed set containing B. The interior int B of B ⊂ X is the largest open subset of B. The boundary ∂B of B is the set theoretic difference of its closure and its interior.


<!-- p:262 -->


The Borel σ-field B(X) on a metric space X is the σ-field generated by the open sets; see [30]. Another generator of B(X) is the system of closed sets. If C ⊂ X then we can restrict the metric to C × C to obtain a subspace of X. With respect to this restricted metric the open (resp. closed) sets are of the form C ∩ U, where U is open (resp. closed) in X. Therefore the σ-field B(C) generated by the open sets is given by B(C) = {B ∩ C : B ∈ B(X)}. If C ∈ B(X), then we call (C, B(C)) a Borel subspace of X.

Let (X, ρ) be a metric space. A sequence xn ∈ X, n ∈ N, is called a Cauchy sequence if limm,n→∞ ρ(xm, xn) = 0. A subset of X is said to be dense if its closure equals X. A metric space is said to be complete if every Cauchy sequence converges in X, and separable if it has a countable dense subset. A complete separable metric space is abbreviated as CSMS. The l u  se ( l l eds ou l ts on refer to [63, Th. A1.2] and [65, Th. 1.1].

Theorem A.19 Let (C, B(C)) be a Borel subspace of a CSMS X. Then (C, B(C)) is a Borel space.

A metric space is said to be σ-compact if it is a countable union of compact sets. A metric space is said to be locally compact if every x ∈ X has a compact neighbourhood U, that is, a compact set containing x in its interior. It is easy to see that any σ-compact metric space is separable. Here is a partial converse of this assertion:

Lemma A.20 Let X be a locally compact separable metric space. Then X is σ-compact.

Proof Let C ⊂ X be an at most countable dense subset of X and let U be the collection of all open sets {z ∈ X : ρ(y, z) &lt; 1/n}, where y ∈ C and n ∈ N. For each x ∈ X there exists an open set Ux with compact closure and with x ∈ Ux. There exists Vx ∈ U such that x ∈ Vx ⊂ Ux. The closures of the sets Vx, x ∈ X, are compact and cover X. □

The next fact is easy to prove.

Lemma A.21 Each closed subset of a locally compact metric space is locally compact.

Lemma A.22 Let X be a separable metric space and let B be a subspace of X. Then B is also separable.

Proof Let C ⊂ X be an at most countable dense subset of X. For each x ∈ C and each n ∈ N we take a point y(x, n) ∈ B(x, 1/n) ∩ B, provided this intersection is not empty. The set of all such points y(x, n) is dense in B. □


<!-- p:263 -->


Let v be a measure on a metric space X. The support supp v of v is the intersection of all closed sets F ⊂ X such that v(X \ F) = 0.

Lemma A.23 Let v be a measure on a separable metric space X. Then γ(X \ supp ν) = 0.

Proof By definition, the set X \ supp v is the union of all open sets U ⊂ X with v(U) = 0. Any such U is the union of some closed balls B(x, q), where x is in a given at most countable dense subset of X and q is a positive rational number. (The proof of this fact is left to the reader.) Hence the result follows from the sub-additivity of v. □

If (X, ρ) and (X′, ρ′) are metric spaces then X × X′ can be made into a metric space in its own right. One natural choice of metric is

$$( ( x , x ^ { \prime } ) , ( y , y ^ { \prime } ) ) \mapsto ( \rho ( x , y ) ^ { 2 } + \rho ( x ^ { \prime } , y ^ { \prime } ) ^ { 2 } ) ^ { 1 / 2 } .$$

Let B(X × Y) be the Borel σ-field on X × Y based on this metric.

Lemma A.24 Suppose that X and Y are separable metric spaces. Then so is X × Y and B(X × Y) = B(X) ⊗ B(Y). If, moreover, X and Y are complete, then so is X × Y.

A topology on a given set X is a system O of subsets of X containing Ø and X and being closed under finite intersections and arbitrary unions. The sets in O are said to be open and the pair (X, O) is called a topological space. An example is a metric space with O given as the system of open sets. Let (X, O) be a topological space. A sequence (x)n≥1 of points in X is said to converge to x ∈ X if for every U ∈ O with x ∈ U there is an n0 ∈ N such that x ∈ U for all n ≥ n0.

### A.3 Hausdorff Measures and Additive Functionals

In this section we fix a number d ∈ N and consider the Euclidean space Rd with scalar product 〈·, ·&gt;, norm ∥ · ∥ and Borel σ-field Bd := B(Rd). We shall discuss a few basic properties of Lebesgue and Hausdorff measure, referring to [63] for more detail on the first and to [35] for more information on the second. We shall also introduce the intrinsic volumes of convex bodies, referring to [147] and [146] for further detail.

The diameter of a non-empty set B ⊂ Rd is the possibly infinite number d(B) := sup{l|x−y| : x, y ∈ B}. The Lebesgue measure (or volume function)


<!-- p:264 -->


λd on (Rd, Bd) is the unique measure satisfying λd([0, 1]d) = 1 and the translation invariance λd(B) = λd(B + x) for all (B, x) ∈ Bd × Rd, where B + x := {y + x : y ∈ B}. In particular, λd is locally finite, that is λd(B) &lt; ∞ for all bounded Borel sets B ⊂ Rd. We also have λd = (λ1)d and therefore λd(rB) = rd λd(B) for all r ≥ 0 and B ∈ Bd, where rB := {rx : x ∈ B}. The Lebesgue measure is also invariant under rotations, that is we have λd(ρB) = λd(B) for all B ∈ Bd and all rotations ρ: Rd → Rd. (Here we write ρB := {ρx : x ∈ B}.) Recall that a rotation is a linear isometry (called proper if it preserves the orientation, that is has determinant 1). For f ∈ R(Rd) one usually writes ∫ f(x) dx instead of ∫ f(x) λd(dx).

The volume of the unit ball Bd := {x ∈ Rd : ∥x|| ≤ 1} is denoted by κd := λa(Bd). This volume can be expressed with the help of the Gamma function; see Exercise 7.16. We mention the special cases κ1 = 2, κ2 = π, and κ3 = (4π)/3. It is convenient to define κ0 := 1. Note that the ball

$$B ( x , r ) \colon = r B ^ { d } + x = \{ y \in \mathbb { R } ^ { d } \, \colon \| y - x \| \leq r \}$$

centred at x ∈ Rd with radius r ≥ 0 has volume κard.

For k ∈ {0, . . . , d} and δ &gt; 0 we set

$$\mathcal { H } _ { k , \delta } ( B ) \colon = \frac { \kappa _ { k } } { 2 ^ { k } } \inf \left \{ \sum _ { j = 1 } ^ { \infty } d ( B _ { j } ) ^ { k } \colon B \subset \bigcup _ { j = 1 } ^ { \infty } B _ { j } , d ( B _ { j } ) \leq \delta \right \} , \quad B \subset \mathbb { R } ^ { d } , \ ( A . 1 9 )$$

where the infimum is taken over all countable collections B1, B2, ... of subsets of Rd and where d(0) := 0. Note that Hk,δ(B) = ∞ is possible for k &lt; d even for bounded sets B. Define

$$\mathcal { H } _ { k } ( B ) \coloneqq \lim _ { \delta \downarrow 0 } \mathcal { H } _ { k , \delta } ( B ) .$$

The restriction of Hk to Ba is a measure, the k-dimensional Hausdorff measure. For k = d we obtain the Lebesgue measure, while H0 is the counting measure supported by Rd. If B ⊂ Rd is a k-dimensional smooth manifold then Hk(B) coincides with its differential geometric volume measure.

For K, L ⊂ Rd we define the Minkowski sum K ⊕ L by

$$K \oplus L \colon = \{ x + y \, \colon x \in K , y \in L \} .$$

Note that K ⊕ L = Ø if K = 0. The Minkowski sum of K and the ball B(0, r) centred at the origin with radius r is called the parallel set of K at distance r. If K ⊂ Rd is closed, then

$$K \oplus r B ^ { d } = \{ x \in \mathbb { R } ^ { d } \, \colon d ( x , K ) \leq r \} = \{ x \in \mathbb { R } ^ { d } \, \colon B ( x , r ) \cap K \neq \emptyset \} ,$$


<!-- p:265 -->


where

$$d ( x , B ) \colon = \inf \{ \| x - y \| \, \colon y \in B \}$$

is the distance of x from a set B ⊂ Rd and inf ∅ := ∞.

A set C ⊂ Rd is said to be convex if for all x, y ∈ C and all t ∈ [0, 1] the point tx + (1 – t)y belongs to C. A non-empty, compact convex subset of Rd is called a convex body for short. The system of all convex bodies is denoted by K(d). We let Kd := K(d) ∪ {0}. It turns out that the volume of the parallel set of a convex body is a polynomial of degree d:

$$\lambda _ { d } ( K \oplus r B ^ { d } ) & = \sum _ { j = 0 } ^ { d } r ^ { d - j } \kappa _ { d - j } V _ { j } ( K ) , \quad K \in \mathcal { K } ^ { d } . \quad ( A . 2 2 ) \\$$

This is known as the Steiner formula and determines the intrinsic volumes V0(K), . . . , Vd(K) of K. Clearly Vi(0) = 0 for all i ∈ {0, . . . , d}. Taking = (  t  s ()  ∞ ← t   ( ← d and V0(K) = 1 if K ≠ 0. More generally, if the dimension of the affine hull of K equals j, then V(K) equals the j-dimensional Hausdorff measure Hj(K) of K. If K has non-empty interior, then

$$V _ { d - 1 } ( K ) = \frac { 1 } { 2 } \mathcal { H } _ { d - 1 } ( \partial K ) ,$$

where ∂K denotes the boundary of K. If the interior of K is empty, then Vd−1(K) = Hd-1(∂K) = Hd-1(K). These facts are suggested by the following consequence of (A.22):

$$2 V _ { d - 1 } ( K ) = \lim _ { r \downarrow 0 } r ^ { - 1 } ( \lambda _ { d } ( K \oplus r B ^ { d } ) - \lambda _ { d } ( K ) ) .$$

Together with Fubini's theorem they can be used to show that

$$\int V _ { d - 1 } ( A \cap ( B + x ) ) \, d x = V _ { d } ( A ) V _ { d - 1 } ( B ) + V _ { d - 1 } ( A ) V _ { d } ( B ) . \quad ( A . 2 4 )$$

Taking K = Bd in (A.22), and comparing the coefficients in the resulting identity between polynomials, yields

$$V _ { i } ( B ^ { d } ) = \left ( \begin{matrix} d \\ i \end{matrix} \right ) \frac { \kappa _ { d } } { \kappa _ { d - i } } , \quad i = 0 , \dots , d . \quad \quad ( A . 2 5 ) \\ \vdots \quad \cdot \quad 1 \quad \cdot \quad 1 \quad \cdot \quad 0 \quad \cdot \quad 1 \quad \cdot \quad 0 \quad \cdot \quad 1 \quad \cdot \quad 0 \quad \cdot \quad 1 \quad \cdot \quad 0 \quad \cdot \quad 1 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0 \quad \cdot \quad 0$$

The intrinsic volumes inherit from Lebesgue measure the properties of invariance under translations and rotations. Moreover, the scaling property of Lebesgue measure implies for any i ∈ {0, . . . , d} that the function Vi is homogeneous of degree i, that is

$$V _ { i } ( r K ) = r ^ { i } V _ { i } ( K ) , \ \ K \in \mathcal { K } ^ { d } , \ r \geq 0 .$$


<!-- p:266 -->


A less obvious property of the intrinsic volumes is that they are monotone increasing with respect to set inclusion. In particular, since V(0) = 0, the intrinsic volumes are non-negative. The restrictions of the intrinsic volumes to K(a) are continuous with respect to the Hausdorff distance, defined by

$$\delta ( K , L ) \coloneqq \min \{ \varepsilon \geq 0 \colon K \subset L \oplus \varepsilon B ^ { d } , L \subset K \oplus \varepsilon B ^ { d } \} , \quad K , L \in \mathcal { K } ^ { ( d ) } .$$

The intrinsic volumes have the important property of additivity, that is

$$V _ { i } ( K \cup L ) = V _ { i } ( K ) + V _ { i } ( L ) - V _ { i } ( K \cap L ) , \ \ i = 0 , \dots , d ,$$

whenever K, L, (K ∪ L) ∈ Ka. The following result highlights the relevance of intrinsic volumes for convex geometry.

Theorem A.25 (Hadwiger's characterisation) Suppose that φ: Kd → R is additive, continuous on Kd \ {0} and invariant under translations and proper rotations. Then there exist c0, . . . , cd ∈ R such that

$$\varphi ( K ) & = \sum _ { i = 0 } ^ { d } c _ { i } V _ { i } ( K ) , \quad K \in \mathcal { K } ^ { d } . \\ \cdot & \quad \cdot \\$$

For applications in stochastic geometry it is necessary to extend the intrinsic volumes to the convex ring Rd. A set K ⊂ Rd belongs to Rd if it can be represented as a finite (possibly empty) union of compact convex sets. (Note that ∅ ∈ Rd.) The space Rd \ {0} is a subset of the space C(d) of all non-empty compact subsets of Rd. The latter can be equipped with the Hausdorff distance (defined again by (A.27)) and the associated Borel σ-field. For the following result we refer to [146, Th. 1.8.4] and [147, Th. 2.4.2]; see also Exercise 17.3.

Theorem A.26 The space C(d) is a CSMS, K(d) is a closed subset of C(d) and Rd \ {0} is a measurable subset of C(d).

Upon extending the Borel σ-field from C(a) to Ca in the usual minimal way (all elements of B(C(d)) and the singleton {0} should be measurable), Rd is a measurable subset of Ca. The σ-fields on these spaces are denoted by B(Cd) and B(Rd), respectively.

A function φ: Rd → R is said to be additive if φ(0) = 0 and

$$\varphi ( K \cup L ) = \varphi ( K ) + \varphi ( L ) - \varphi ( K \cap L ) , \quad K , L \in \mathcal { R } ^ { d } .$$

Such an additive function satisfies the inclusion-exclusion principle

$$\varphi ( K _ { 1 } \cup \cdots \cup K _ { m } ) = \sum _ { n = 1 } ^ { m } ( - 1 ) ^ { n - 1 } \sum _ { 1 \leq i _ { 1 } < \cdots < i _ { n } , \leq m } \varphi ( K _ { i _ { 1 } } \cap \cdots \cap K _ { i _ { n } } ) \quad ( A . 3 0 )$$


<!-- p:267 -->


for all K1, . . . , Km ∈ Rd and all m ∈ N. The intrinsic volumes Vi can be extended from Ka to Rd such that this extended function (still denoted by V) is additive. By (A.30) this extension must be unique. It is the existence that requires a (non-trivial) proof. Then Va is still the volume, while (A.23) holds whenever K ∈ Rd is the closure of its interior. Moreover, Va–1(K) ≥ 0 for all K ∈ Rd. The function V0 is known as the Euler characteristic and takes on integer values. In particular, V0(K) = 1 for all K ∈ K(d). When d = 2 the number V0(K) can be interpreted as the number of connected components minus the number of holes of K ∈ R2. The intrinsic volumes are measurable functions on Rd.

Let Fd denote the space of all closed subsets of Rd. The Fell topology on this space is the smallest topology such that the sets {F ∈ Fd : F ∩ G ≠ 0} and {F ∈ Fd : F ∩ K = 0} are open for all open sets G ⊂ Rd and all compact sets K ⊂ Rd. It can be shown that Fn → F in Fd if and only if d(x, Fn) → d(x, F) for each x in a dense subset of Rd; see [63, Th. A2.5]. This shows that the Fell topology is second countable, that is there is a countable family of open subsets of Fa such that every open set is the union of some sets in the family; see again [63, Th. A2.5].

In this book we use the following properties of the Fell topology. Further information can be found in [101, 112, 147].

Lemma A.27 The mapping (F, x) → F + x from Fd × Rd to Fd is continuous.

Proof Suppose that xn → x in Rd and Fn → F in Fd. For each y ∈ Rd we need to show that d(y, Fn + xn) → d(y, F + x). Assuming (for simplicity) that Fn ≠ Ø for all n ∈ N, this follows from the identities

d(y, Fn + xn) = d(y − xn, Fn) = (d(y − xn, Fn) − d(y − x, Fn)) + d(y − x, Fn) and the Lipschitz property from Exercise 2.8. □

We denote by B(Fd) the σ-field generated by the open subsets of Fd. Then (Fd, B(Fd)) is a measurable space.

Lemma A.28 The sets {F ∈ Fd : F ∩ K = 0}, K ∈ Cd, form a π-system generating B(Fd).

Proof The first assertion follows from the fact that for given K, L ∈ Ca the equations F ∩ K = ∅ and F ∩ L = ∅ are equivalent to F ∩ (K ∪ L) = 0. Let G ⊂ Rd be open. Then there exists a sequence K ∈ Ca, n ∈ N, such that G = ∪K. For F ∈ Fd we then have that F∩G ≠ Ø if and only if there exists n ∈ N such that F ∩ Kn ≠ 0. This shows the second assertion. □


<!-- p:268 -->


Lemma A.29 We have Cd ∈ B(Fd) and B(Cd) = {Cd ∩ A : A ∈ B(Fd)}.

Proof To prove that Cd ∈ B(Fd) it is sufficient to note that a set F ∈ Fd is compact if and only if there exists n ∈ N such that F ∩ (Rd \ B(0, n)) = 0. The second assertion follows from Lemma A.28 and Lemma 17.2. □

Lemma A.30 The mappings (F, F′) → F ∩ F′ from Fd × Fd to Fd and (F, K) ↔ F ∩ K from Fd × Cd to Cd are measurable.

Proof We sketch the proof, leaving some of the details to the reader. By Lemma A.29 we only need to prove the first assertion. Let C ∈ C(a). We shall show that H := {(F, F′) ∈ Fd × Fd : F ∩ F′ ∩ C = 0} is open in the product topology on Fd × Fd, which is the smallest topology containing the sets G × G′ for all open G, G′ ⊂ Fd. Assume that H is not open. Then there exists (F, F′) ∈ H such that every open neighbourhood of (F, F′) (an open set containing (F, F′)) has a non-empty intersection with the complement of H. Since the Fell topology is second countable, there exist sequences (Fn) and (Fn) of closed sets such that Fn ∩ F′ ∩ C ≠ ∅ for all n ∈ N and (Fn, Fn) → (F, F′) as n → ∞. For each n ∈ N choose xn ∈ Fn ∩ Fn ∩ C. Since C is compact, there exists x ∈ C such that x → x along a subsequence. Since Fn → F we have x ∈ F. (Otherwise there is a compact neighbourhood of x, not intersecting F, contradicting the definition of the Fell topology.) Similarly, we have x ∈ F'. This shows that x ∈ F ∩ F′∩ C, a contradiction. Hence H is open, and since the Fell topology is second countable it can be shown that H is a member of the product σ-field B(Fd)øB(Fd); see [30, Prop. 4.1.7]. Since C ∈ C(d) was arbitrarily chosen, Lemma A.28 implies the assertion. □

### A.4 Measures on the Real Half-Line

In this section we consider a locally finite measure γ on R+ = [0, ∞) with the Borel σ-field. We abbreviate v(t) := v([0, t]), t ∈ R+, and note that ν can be identified with the (right-continuous) mapping t → v(t). We define a function ν← : R+ → [0, ∞] by

$$\nu ^ { \leftarrow } ( t ) \colon = \inf \{ s \geq 0 \, \colon \nu ( s ) \geq t \} , \quad t \geq 0 ,$$

where inf ∅ := ∞. This function is increasing, left-continuous and thus measurable; see e.g. [139]. We also define v(∞) := limt→∞ v(t).


<!-- p:269 -->


Proposition A.31 Let f ∈ R+ (R+). Then

$$\int f ( t ) \, \nu ( d t ) = \int _ { 0 } ^ { \nu ( \infty ) } f ( \nu ^ { \leftarrow } ( t ) ) \, d t .$$

If v is diffuse, then we have for all g ∈ R+(R+) that

$$\int _ { \ } g ( \nu ( t ) ) \, \nu ( d t ) = \int _ { 0 } ^ { \nu ( \infty ) } g ( t ) \, d t .$$

Proof For all s, t ∈ R+ the inequalities v←(t) ≤ s and t ≤ v(s) are equivalent; see [139]. For 0 ≤ a &lt; b &lt; ∞ and f := 1(a,b] we therefore obtain

$$\int _ { 0 } ^ { \nu ( \infty ) } f ( \nu ^ { \leftarrow } ( t ) ) \, d t & = \int _ { 0 } ^ { \nu ( \infty ) } 1 \{ a < \nu ^ { \leftarrow } ( t ) \leq b \} \, d t \\ & = \int _ { 0 } ^ { \nu ( \infty ) } 1 \{ \nu ( a ) < t \leq \nu ( b ) \} \, d t = \nu ( b ) - \nu ( a ) ,$$

so that (A.32) follows for this choice of f. Also (A.32) holds for f = 1{0}, since v←(t) = 0 if and only if t ≤ v({0}). We leave it to the reader to prove the case of a general f using the tools from measure theory presented in Section A.1.

Assume now that ν is diffuse and let g ∈ R+(R+). Applying (A.32) with f(t) := g(v(t)) yields

$$\int _ { \ } g ( \nu ( t ) ) \, \nu ( d t ) = \int _ { 0 } ^ { \nu ( \infty ) } g ( \nu ( \nu ^ { \leftarrow } ( t ) ) ) \, d t = \int _ { 0 } ^ { \nu ( \infty ) } g ( t ) \, d t ,$$

since v(ν←(t)) = t; see [139].

□

Assume now that ν is a measure on R+ with v(R+) ≤ 1. With the definition v({∞}) := 1 − v(R+) we may then interpret ν as a probability measure on R. The hazard measure of v is the measure R on R+ given by

$$R _ { \nu } ( d t ) \colon = ( \nu [ t , \infty ) ) ^ { \oplus } \nu ( d t ) ,$$

where a® := 1{a ≠ 0}a−1 is the generalised inverse of a ∈ R. The following result is a consequence of the exponential formula of Lebesgue-Stieltjes calculus (see [18, 88]) and a special case of Th. A5.10 in [88].

Proposition A.32 If ν is a diffuse measure on R+ with v(R+) ≤ 1 and hazard measure Ry, then v((t, ∞]) = exp[−Rγ([0, t])] for all t ∈ R+.


<!-- p:270 -->


if a ≤ b and

### A.5 Absolutely Continuous Functions

Let I ⊂ R be a non-empty interval. This means that the relations a, b ∈ I and a &lt; b imply that [a, b] ⊂ I. A function f : I → R is said to be absolutely continuous if for every ∈ &gt; 0 there exists δ &gt; 0 such that

$$\sum _ { i = 1 } ^ { n } | f ( y _ { i } ) - f ( x _ { i } ) | \leq \varepsilon$$

whenever n ∈ N and x1, .. . , xn, y1, .. . , yn ∈ I satisfy xi ≤ yi for all i ∈ {1 . . , n}, yi &lt; xi+1 for al i ∈ {1, . . . , n − 1} and ∑i=1 |yi − xi| ≤ δ.

Recall that λ1 denotes the Lebesgue measure on R. For f ∈ R(I) and a, b ∈ I we write

$$\int _ { a } ^ { b } f ( t ) \, d t \, \colon = \int _ { [ a , b ] } f ( t ) \, \lambda _ { 1 } ( d t )$$

$$\int _ { a } ^ { b } f ( t ) \, d t \colon = - \int _ { [ b , a ] } f ( t ) \, \lambda _ { 1 } ( d t )$$

if a &gt; b. Absolutely continuous functions can be characterised as follows.

Theorem A.33 Let a &lt; b and suppose that f : [a, b] → R is a function. Then f is absolutely continuous if and only if there is a function f′ ∈ L1((λ1)[a,b]) such that

$$f ( x ) = f ( a ) + \, \left \lceil \, f ^ { \prime } ( t ) \, d t , \quad x \in [ a , b ] . \quad ( A . 3 5 )$$

The function f′ in (A.35) is called the Radon-Nikodým derivative of f. It is uniquely determined almost everywhere with respect to Lebesgue measure on [a, b].

Proposition A.34 (Product rule) Suppose that f, g ∈ R(I) are absolutely continuous with Radon–Nikodým derivatives f′, g'. Then the product f g is absolutely continuous with Radon–Nikodým derivative f′g + fg′.

Proof Let x ∈ [a, b]. By Theorem A.33 and Fubini's theorem,

$$( f ( x ) - f ( a ) ) ( g ( x ) - g ( a ) ) \\ = \int _ { a } ^ { x } \int _ { a } ^ { x } 1 \{ s > t \} f ^ { \prime } ( s ) g ^ { \prime } ( t ) \, d s \, d t + \int _ { a } ^ { x } \int _ { a } ^ { x } 1 \{ t \geq s \} f ^ { \prime } ( s ) g ^ { \prime } ( t ) \, d s \, d t \\ = \int _ { a } ^ { x } f ^ { \prime } ( s ) ( g ( s ) - g ( a ) ) \, d s + \int _ { a } ^ { x } ( f ( t ) - f ( a ) ) g ^ { \prime } ( t ) \, d t .$$


<!-- p:271 -->


Again by Theorem A.33 this can be simplified to

$$f ( x ) g ( x ) = f ( a ) g ( a ) + \int _ { a } ^ { a } f ^ { \prime } ( s ) g ( s ) \, d s + \int _ { a } ^ { a } f ( t ) g ^ { \prime } ( t ) \, d t .$$

Thus, by Theorem A.33 the proposition is true.

□

Let AC2 be the space of functions f : R → R such that f is differentiable with an absolutely continuous derivative f'. The following result can be proved using the preceding product rule (Proposition A.34).

Proposition A.35 Let f ∈ AC2. Then for all x ∈ R we have

$$f ( x ) = f ( a ) + f ^ { \prime } ( a ) ( x - a ) + \left \lceil \int _ { \ } f ^ { \prime \prime } ( t ) ( x - t ) \, d t , \right \rceil$$

where f" is a Radon–Nikodým derivative of f′.

Proof We claim that it suffices to prove

$$f ( x ) = f ( a ) - a f ^ { \prime } ( a ) + x f ^ { \prime } ( x ) - \int _ { a } ^ { a ^ { \prime \prime } } f ^ { \prime \prime } ( t ) t \, d t$$

for all x ∈ R. Indeed, by Theorem A.33 (applied with f' instead of f) the right-hand side of (A.36) equals that of (A.37). Both sides of (A.37) agree for x = a. By Theorem A.33 it is hence enough to show that both sides have the same Radon-Nikodým derivative. This follows from Proposition A.34 applied to xf'(x) and Theorem A.33. □


<!-- p:272 -->


## Some Probability Theory

### B.1 Fundamentals

For the reader's convenience we here provide terminology and some basic results of measure-theoretic probability theory. More detail can be found, for instance, in [13, 30] or in the first chapters of [63].

A probability space is a measure space (Ω, F, P) with P(Ω) = 1. Then P is called a probability measure (sometimes also a distribution), the sets A ∈ F are called events, while P(A) is known as the probability of the event A. In this book the probability space (Ω, F, P) will be fixed.

Let (X, X) be a measurable space. A random element of X (or of (X, X)) is a measurable mapping X: Ω → X. The distribution Px of X is the image of P under X, that is Px := P  X−1 or, written more explicitly, Px(A) = P(X ∈ A), A ∈ X. Here we use the common abbreviation

$$\mathbb { P } ( X \in A ) \colon = \mathbb { P } ( \{ \omega \in \Omega \, \colon X ( \omega ) \in A \} ) .$$

We write X  Y to express the fact that two random elements X, Y of X have the same distribution.

Of particular importance is the case (X, X) = (R, B(R)). A random element X of this space is called a random variable while the integral ∫ X dP is called the expectation (or mean) E[X] of X. If Y is a random element of a measurable space (Y, Y) and f ∈ R(Y), then f(Y) is a random variable, and it is easy to prove that E[f(Y)] = ∫ f dPy. If X is a random variable with E[|X|a] &lt; ∞ for some a &gt; 0 then E[|X|b] &lt; ∞ for all b ∈ [0, a]. In the case a = 1 we say that X is integrable, while in the case a = 2 we say that X is square integrable. In the latter case the variance of X is defined as

$$\mathbb { V } a r [ X ] \colon = \mathbb { E } [ ( X - \mathbb { E } [ X ] ) ^ { 2 } ] = \mathbb { E } [ X ^ { 2 } ] - ( \mathbb { E } [ X ] ) ^ { 2 } .$$

We have P(X = E[X]) = 1 if and only if Var[X] = 0. For random variables X, Y we write X ≤ Y, P-almost surely (shorter: P-a.s. or just a.s.) if P(X ≤ Y) = 1. For A ∈ F we write X ≤ Y, P-a.s. on A if P(A \ {X ≤ Y}) = 0.


<!-- p:273 -->


The covariance between two square integrable random variables X and Y is defined by

()(XT) − XT = ( − )(XT − ) =:  X])

The Cauchy-Schwarz inequality (see (A.2)) says that

$$| \mathbb { E } [ X Y ] | \leq ( \mathbb { E } [ X ^ { 2 } ] ) ^ { 1 / 2 } ( \mathbb { E } [ Y ^ { 2 } ] ) ^ { 1 / 2 } ,$$

or |Cov[X, Y] ≤ (Var[X])1/2(Var[Y])1/2. Here is another useful inequality for the expectation of convex functions of a random vector X in Rd, that is of a random element of Rd.

Proposition B.1 (Jensen's inequality) Let X = (X1, . . . , Xd) be a random vector in Rd whose components are in L1(P) and let f : Rd → R be convex (]   · ])f  [()f]  ∞ &gt; [()f  ()

Jensen's inequality (E[X])2 ≤ E[X2] and the Cauchy-Schwarz inequality E[XY] ≤ (E[X2])1/2(E[Y2])1/2 hold for all R+-valued random variables. To see this, we can apply these inequalities with X ∧ n and Y ∧ n, n ∈ N, in place of X (resp. Y) and then let n → ∞.

Let T ≠ Ø be an (index) set. A family {Ft : t ∈ T} of σ-fields contained in F is said to be independent if

$$\mathbb { P } ( A _ { t _ { 1 } } \cap \cdots \cap A _ { t _ { k } } ) = \mathbb { P } ( A _ { t _ { 1 } } ) \cdots \mathbb { P } ( A _ { t _ { k } } )$$

for any distinct t1, . . . , tk ∈ T and any At1 ∈ Ft1, . . , Atk ∈ Ftk. A family {X, : t ∈ T} of random variables with values in measurable spaces (X,, X) is said to be independent if the family {σ(X) : t ∈ T} of generated σ-fields is independent.

The following result guarantees the existence of infinite sequences of independent random variables in a general setting.

Theorem B.2 Let (Ω, Fn, Qn), n ∈ N, be probability spaces. Then there exists a unique probability measure Q on the space (×n=1Ωn, ∅n=1Fn) such that Q(A × ×m=n+1Ωm) = ∅i=1Qi(A) for all n ∈ N and A ∈ ∅n=1Fm.

Under a Borel assumption, Theorem B.2 extends to general probability measures on infinite products.

Theorem B.3 Let (Ω, Fn), n ∈ N, be a sequence of Borel spaces and let Qn be probability measures on (Ω1 × · · · × Ωn, F1 ⊗ · · · ∅ Fn) such that Qn+1(· × Ωn+1) = Qn for all n ∈ N. Then there is a unique probability measure Q on (×n=1Ωn, ⊗n=1Fn) such that Q(A××m=n+1Ωm) = Qn(A) for all n ∈N and A ∈ ∅"=1Fm.


<!-- p:274 -->


The characteristic function of a random vector X = (X1, . . . , Xd) in Rd is the function φx : Rd → C defined by

$$\varphi _ { X } ( t ) \colon = \mathbb { E } [ \exp [ - i \langle X , t \rangle ] ] , \quad t = ( t _ { 1 } , \dots , t _ { d } ) \in \mathbb { R } ^ { d } , \quad ( B . 1 )$$

where C denotes the complex numbers and i := √-1 is the imaginary unit. The Laplace transform of a random vector X = (X1, . . . , Xd) in Rd (a random element of R†) is the function Lx on Rd defined by

$$L _ { X } ( t ) \colon = \mathbb { E } [ \exp ( - \langle X , t \rangle ) ] , \ \ t = ( t _ { 1 } , \dots , t _ { d } ) \in \mathbb { R } _ { + } ^ { d } .$$

Proposition B.4 (Uniqueness theorem) Two random vectors in Rd (resp. in Rd) have the same distribution if and only if their characteristic functions (resp. Laplace transforms) coincide.

The Laplace transform of an R+-valued random variable is analytic on (0, ∞). Therefore it is determined by its values on any open (non-empty) interval I ⊂ (0, ∞) (see [78]), and Proposition B.4 yields:

Proposition B.5 Two R+-valued random variables have the same distribution if and only if their Laplace transforms coincide on a non-empty open interval.

A sequence (X) of finite random variables is said to converge P-almost surely (shorter: P-a.s. or just a.s.) to a random variable X if the event

$$\left \{ \lim _ { n \to \infty } X _ { n } = X \right \} \colon = \left \{ \omega \in \Omega \colon \lim _ { n \to \infty } X _ { n } ( \omega ) = X ( \omega ) \right \}$$

has probability 1. A similar notation is used for infinite series of random variables.

Theorem B.6 (Law of large numbers) Let X1, X2, . . . be independent and identically distributed random variables such that E[|X1] &lt; ∞. Then the sequence n−1(X1 + · . · + X), n ∈ N, converges almost surely to E[X1].

The following criterion for the convergence of a series with independent summands is useful.

Proposition B.7 Let X ∈ L2(P), n ∈ N, be independent random variables satisfying ∑n=1 Var[X] &lt; ∞. Then the series ∑n=1(Xn − E[Xn]) converges P-a.s. and in L2(P).

A sequence (X) of random variables converges in probability to a random variable X if P(|Xn − X| ≥ ε) → 0 as n → ∞ for each ε &gt; 0. Each almost surely converging sequence converges in probability. Markov's inequality says that every non-negative random variable Z satisfies


<!-- p:275 -->


$$\mathbb { P } ( Z \geq \varepsilon ) \leq \frac { \mathbb { E } [ Z ] } { \varepsilon } , \ \varepsilon > 0 ,$$

and implies the following fact.

Proposition B.8 Let p ≥ 1 and suppose that the random variables X, n ∈ N, converge in LP(P) to X. Then Xn → X in probability.

Let X, X1, X2, ... be random elements of a metric space X (equipped with its Borel σ-field). The sequence (X) is said to converge in distribution to X if lim→∞ E[f(X)] = E[f(X)] for every bounded continuous function f : X → R. One writes X → X as n → ∞. Let ρ denote the metric on X. A function f : X → R is said to be Lipschitz if there exists c ≥ 0 such that

$$| f ( x ) - f ( y ) | \leq c \rho ( x , y ) , \quad x , y \in \mathbb { X } .$$

The smallest of such c is the Lipschitz constant of f. The following result is proved (but not stated) in [12].

Proposition B.9 A sequence (X) of random elements of a metric space X converges in distribution to X if and only if lim→∞ E[f(X)] = E[f(X)] for every bounded Lipschitz function f : X → R.

Proposition B.10 A sequence (Xn)n≥1 of random vectors in Rd converges in distribution to a random vector X if and only if lim→∞ φx(t) = φx(t) for all t ∈ Rd. A sequence (X)n≥1 of random vectors in Rd converges in distribution to a random vector X if and only if lim→∞ Lx(t) = Lx(t) for all t ∈ Rd.

### B.2 Mean Ergodic Theorem

Random variables X1, X2, X3 . .. are said to form a stationary sequence if (X1, . . . , Xk) = (X2, . . . , Xk+1) for all k ∈ N. The following result is well known; see e.g. [30, 63]. For completeness we provide here a simple proof, which was inspired by [67].

Theorem B.11 (Mean ergodic theorem) Suppose (X)n≥1 is a stationary sequence of integrable random variables. For n ∈ N, set Sn := Σi=1 X and A := S/n. Then there exists a random variable Y with A → Y in L1(P) as n → ∞.


<!-- p:276 -->


Proof In the first part of the proof we assume that there exists c ∈ R such that |X| ≤ c for all i ∈ N. We show that there exists a random variable L with A → L a.s. It suffices to prove this in the case where c = 1 and E[X1] = 0, so assume this. Define the random variable L := lim sup→∞ A. It is enough to show that E[L] ≤ 0, since then the same argument shows that E[lim sup→∞(−A)] ≤ 0 so that E[lim inf→∞ A] ≥ 0, and hence

$$\mathbb { E } [ \lim \sup _ { n \to \infty } A _ { n } - \liminf _ { n \to \infty } A _ { n } ] \leq 0 ,$$

so that lim sup→∞ A = lim inf→∞ A almost surely.

Let ε ∈ (0, 1/4). Setting T := min{n : An &gt; L − ε}, we can and do choose k ∈ N such that P(T &gt; k) &lt; ε. For n, m ∈ N, define

$$A _ { n , m } \colon = m ^ { - 1 } ( X _ { n } + \cdots + X _ { n + m - 1 } )$$

and Tn := min{m : An,m &gt; L − ε}. In particular, T1 = T. Also, Tn has the same distribution as T for all n, because L = lim supm→∞ An,m for all n. Now set

$$X _ { n } ^ { * } \colon = X _ { n } + 2 1 \{ T _ { n } > k \} ,$$

and note that E[Xn] = E[X1]. Set Sn := Σi=1 Xi and An := Sn /n. Set T* := min{n : An &gt; L−ε}. Then T* ≤ T and if T &gt; k then S1 = X1 +2 ≥ 1 &gt; L−ε, so that T* = 1. It follows that P(T* ≤ k) = 1.

Set M0 := 0 and M1 := T*. Then M1 ∈ (0, k] with AM, &gt; L−ε. Repeating the argument, there exists M2 ∈ (M1, M1 + k] such that

$$( M _ { 2 } - M _ { 1 } ) ^ { - 1 } ( S _ { M _ { 2 } } ^ { * } - S _ { M _ { 1 } } ^ { * } ) > L - \varepsilon ,$$

Continuing in this way we have a strictly increasing sequence of random variables M0, M1, M2, ... such that the average of Xn over each interval (Mi-1, M] exceeds L − ε for each n ∈ N. Then for m ∈ N the average over (0, Mm] satisfies the same inequality: indeed, setting S0 = 0 we have

$$S _ { M _ { m } } ^ { * } = \sum _ { i = 1 } ^ { m } ( S _ { M _ { i } } ^ { * } - S _ { M _ { i - 1 } } ^ { * } ) \geq ( L - \varepsilon ) \sum _ { i = 1 } ^ { m } ( M _ { i } - M _ { i - 1 } ) = ( L - \varepsilon ) M _ { m } .$$

Given n ∈ N with n ≥ k, at least one of the times Mi (denoted M') lies in (n−k, n]. Since Xi ≥ −1 for all i we have Sn ≥ SM, −k and since AM ≥ L−ε by (B.4) and L − ε ≤ 1, we obtain

$$S _ { n } ^ { * } \geq ( L - \varepsilon ) n - ( L - \varepsilon ) ( n - M ^ { \prime } ) - k \geq ( L - \varepsilon ) n - 2 k$$

o       - [t         v E[An] = E[Xν] ≤ 2ε; hence E[L] ≤ 4ε, and hence E[L] ≤ 0, as required.

Now we turn to the second part of the proof, dropping the assumption that X1 is bounded. By taking positive and negative parts, it suffices to treat the case where X1 ≥ 0, so assume this. For k, n ∈ N, set Xn,k := min{X, k} and An,k := n−1 Σi=1 X,k. By the first part of the proof and dominated convergence, there exists a random variable Lk such that A,k → Lk almost surely and in L1. Then Lk ≥ 0, Lk is non-decreasing in k and E[Lk] ≤ E[X1] for all k. Hence there is a limit variable L := limk→∞ Lk.


<!-- p:277 -->


Leu os  3 - [t  [  s  &lt;     &lt; 3 t moreover E[[L – Lk|] &lt; ε. Then for large enough n we have

$$\mathbb { E } [ | A _ { n } - L | ] \leq \mathbb { E } [ | A _ { n } - A _ { n , k } | ] + \mathbb { E } [ | A _ { n , k } - L _ { k } | ] + \mathbb { E } [ | L _ { k } - L | ] < 3 \varepsilon ,$$

which yields the result.

□

### B.3 The Central Limit Theorem and Stein's Equation

A random variable N is said to be standard normal if its distribution has density x → (2π)−1/2 exp(−x2/2) with respect to Lebesgue measure on R. Its characteristic function is given by t → exp(-t2/2) while its moments are given by

$$\mathbb { E } [ N ^ { k } ] = \begin{cases} ( k - 1 ) ! ! , & \text {if $k$ is even,} \\ 0 , & \text {otherwise,} \end{cases} \quad ( B . 5 )$$

where for an even integer k ≥ 2 we define the double factorial of k – 1 by

$$( k - 1 ) ! ! \colon = ( k - 1 ) \cdot ( k - 3 ) \cdots 3 \cdot 1 .$$

Note that this is the same as the number of matchings of [k] := {1, ..., k} (a matching of [k] is a partition of [k] into disjoint blocks of size 2). Indeed, it can be easily checked by induction that

$$c a r d \, M ( k ) = \begin{cases} ( k - 1 ) ! ! , & \text {if $k$ is even,} \\ 0 , & \text {otherwise,} \end{cases} \quad ( B . 7 )$$

where M(k) denotes the set of matchings of [k]. The moment formula (B.5) can be proved by partial integration or by writing the characteristic function of N as a power series. Taking c &gt; 0 and using a change of variables we can derive from (B.5) that

$$\mathbb { E } [ \exp ( - c N ^ { 2 } ) N ^ { 2 m } ] = ( 1 + 2 c ) ^ { - m - 1 / 2 } ( 2 m - 1 ) ! ! , \ \ m \in \mathbb { N } _ { 0 } ,$$

where (−1)!! := 1. A random variable X is said to have a normal distribution with mean a ∈ R and variance b ≥ 0, if X ≡ bN + a, where N is standard normal. A sequence (X)n≥1 of random variables is said to satisfy the central limit theorem if X → N as n → ∞.


<!-- p:278 -->


A random vector X = (X1, . . . , Xd) is said to have a multivariate normal distribution if 〈X, t〉 has a normal distribution for all t ∈ Rd. In this case the distribution of X is determined by the means E[X] and covariances E[XXj], i, j ∈ {1, . . . , d}. Moreover, if a sequence (X(n))n≥1 of random vectors with a multivariate normal distribution converges in distribution to a random vector X, then X has a multivariate normal distribution.

Proposition B.12 Let X, X1, X2, . . . be random variables and assume that E[|X|k] &lt; ∞ for all k ∈ N. Suppose that

$$\lim _ { n \to \infty } \mathbb { E } [ X _ { n } ^ { k } ] = \mathbb { E } [ X ^ { k } ] , \ \ k \in \mathbb { N } ,$$

and that the distribution of X is uniquely determined by the moments E[Xk], k ∈ N. Then Xn → X as n → ∞.

Let Lip(1) denote the space of Lipschitz functions h: X → R with Lipschitz constant less than or equal to 1. For a given h ∈ Lip(1) a function g : R → R is said to satisfy Stein's equation for h if

$$h ( x ) - \mathbb { E } [ h ( N ) ] = g ^ { \prime } ( x ) - x g ( x ) , \quad x \in \mathbb { R } ,$$

where N is a standard normal random variable.

Proposition B.13 (Stein's equation) Suppose that h ∈ Lip(1). Then there exists a differentiable solution g of (B.9) such that g′ is absolutely continuous and such that g′(x) ≤ √2/π and g′(x) ≤ 2 for λ1-a.e. x ∈ R, where g" is a Radon–Nikodým derivative of g′.

Proof We assert that the function

$$g ( x ) \colon = e ^ { x ^ { 2 } / 2 } \int _ { - \infty } ^ { x } e ^ { - y ^ { 2 } / 2 } ( h ( y ) - \mathbb { E } [ h ( N ) ] ) \, d y , \quad x \in \mathbb { R } ,$$

is a solution. Indeed, the product rule (Proposition A.34) implies that g is absolutely continuous. Moreover, one version of the Radon-Nikodým derivative is given by

$$g ^ { \prime } ( x ) & = x e ^ { x ^ { 2 } / 2 } \int _ { - \infty } ^ { x } e ^ { - y ^ { 2 } / 2 } ( h ( y ) - \mathbb { E } [ h ( N ) ] ) \, d y + e ^ { x ^ { 2 } / 2 } e ^ { - x ^ { 2 } / 2 } ( h ( x ) - \mathbb { E } [ h ( N ) ] ) \\ & = h ( x ) - \mathbb { E } [ h ( N ) ] + x g ( x ) .$$

Hence (B.9) holds. Since a Lipschitz function is absolutely continuous (this can be checked directly) it follows from the product rule that g' is absolutely continuous. The bounds for g' and g" follow from some lines of calculus which we omit; see [20, Lem. 4.2] for the details. □


<!-- p:279 -->


### B.4 Conditional Expectations

Let X be a random variable and let G ⊂ F be a σ-field. If there exists a G-measurable random variable Y such that

$$\mathbb { E } [ \mathbf 1 _ { C } X ] = \mathbb { E } [ \mathbf 1 _ { C } Y ] , \quad C \in \mathcal { G } ,$$

then Y is said to be a version of the conditional expectation of X given G. If Y' is another version, then it follows that Y = Y', P-a.s. If, on the other hand, Y is a version of the conditional expectation of X given G, and Y' is another G-measurable random variable satisfying Y = Y', P-a.s., then Y' is also a version of the conditional expectation of X, given G. We use the notation Y = E[X | G] to denote one fixed version of the conditional expectation, if it exists. If the σ-field G is generated by an at most countable family of pairwise disjoint sets A1, A2, . . . of F, whose union is Ω, then

$$\mathbb { E } [ X \, | \, \mathcal { G } ] = \sum _ { n \geq 1 } \mathbf 1 _ { A _ { n } } \mathbb { E } [ X \, | \, A _ { n } ] , \quad \mathbb { P } \text {-a.s.}$$

Here we use the conditional expectation E[X | A] := P(A)−1E[1AX] of X with respect to an event A ∈ F, where 0/0 := 0.

In the general case one has the following result, which can be proved with the aid of the Radon–Nikodým theorem (Theorem A.10).

Proposition B.14 Let X be a random variable and let G ⊂ F be a σ-field.

- (i) If X is non-negative, then E[X | G] exists and has an almost surely finite version if and only if the measure C  E[1cX] is σ-finite on G.
- (ii) If X ∈ L1(P), then E[X | G] exists and has an almost surely finite version.

For A ∈ F the random variable

$$\mathbb { P } ( A \, | \, \mathcal { G } ) \colon = \mathbb { E } [ 1 _ { A } \, | \, \mathcal { G } ]$$

is called (a version of the) conditional probability of A given G. Let Y be a random element of a measurable space (Y, Y) and let X be a random variable. We write E[X | Y] := E[X | σ(Y)] if the latter expression is defined. Further, we write P(A | Y) := E[1A | Y] for A ∈ F. If X is a random element of the space (X, X) then the mapping (ω, B) ↔ P({X ∈ B} | Y)(ω)


<!-- p:280 -->


from Ω× X to R+ is called the conditional distribution of X given Y. If this mapping can be chosen as a probability kernel from Ω to X, it is called a regular version of this conditional distribution.

The conditional expectation is linear, monotone and satisfies the triangle and Jensen inequalities. The following properties can be verified immediately from the definition. Property (iii) is called the law of total expectation while (vi) is called the pull out property. If nothing else is said, then all relations concerning conditional expectations hold P-a.s.

Theorem B.15 Consider R+-valued random variables X and Y and σfields G, G1, G2 ⊂ F. Then:

- [X] = [5 | X]a  { } = 5 f (i)
- (ii) If X is G-measurable, then E[X | G] = X.
- (iii) E[E[X | G]] = E[X].
- (iv) Suppose that G1 ⊂ G2 P-a.s., i.e. suppose that for every A ∈ G1 there is a set B ∈ G2 with P((A\B) ∪ (B\A)) = 0. Then

$$\mathbb { E } [ \mathbb { E } [ X | \mathcal { G } _ { 2 } ] | \mathcal { G } _ { 1 } ] = \mathbb { E } [ X | \mathcal { G } _ { 1 } ] .$$

- '[ = [ |      s ( t n ()
- (vi) Suppose that X is G-measurable. Then E[XY | G] = X E[Y | G].

Let (X, X) be a measurable space and let f ∈ R+(Ω × X). Then, for any x ∈ X, f(x) := f(·, x) (this is the mapping ω ↔→ f(ω, x)) is a random variable. Hence, if G ⊂ F is a σ-field, we can form the conditional expectation E[f(x) | G]. A measurable version of this conditional expectation is a function f ∈ R+(Ω×X) such that f(x) = E[f(x) | G] holds P-a.s. for every x ∈ X. Using the monotone class theorem the linearity of the conditional expectation can be extended as follows.

Lemma B.16 Let (X, X, λ) be an s-inite measure space and suppose that f ∈ R+(Ω × X) or f ∈ L1(P ⊗ λ). Let G ⊂ F be a σ-field. Then there is a measurable version of E[f(x) | G] satisfying

$$\mathbb { E } [ \int f ( x ) \, \lambda ( d x ) \, \Big | \, \mathcal { G } ] = \int \mathbb { E } [ f ( x ) \, | \, \mathcal { G } ] \, \lambda ( d x ) , \quad \mathbb { P } _ { \mu } a . s .$$

### B.5 Gaussian Random Fields

Let X be a non-empty set, for instance a Borel subset of Rd. A random field (on X) is a family Z = (Z(x))x∈x of real-valued random variables. Equivalently, Z is a random element of the space RX of all functions from X to R, equipped with the smallest σ-field making all projection mappings f ↔ f(t), t ∈ X, measurable. It is customary to write Z(ω, x) := Z(ω)(x) for ω ∈ Ω and x ∈ X. A random field Z′ = (Z′(x))x∈x (defined on the same probability space as the random field Z) is said to be a version of Z if P(Z(x) = Z′(x)) = 1 for each x ∈ X. In this case Z ≡ Z'.


<!-- p:281 -->


A random field Z = (Z(x))x∈x is square integrable if E[Z(x)2] &lt; ∞ for each x ∈ X. In this case the covariance function K of Z is defined by

$$K ( x , y ) \colon = \mathbb { E } [ ( Z ( x ) - \mathbb { E } [ Z ( x ) ] ) ( Z ( y ) - \mathbb { E } [ Z ( y ) ] ) ] , \quad x , y \in \mathbb { X } .$$

This function is non-negative definite, that is

$$\sum _ { i , j = 1 } ^ { m } c _ { i } c _ { j } K ( x _ { i } , x _ { j } ) \geq 0 , \ \ c _ { 1 } , \dots , c _ { m } \in \mathbb { R } , \ x _ { 1 } , \dots , x _ { m } \in \mathbb { X } , \, m \in \mathbb { N } . \ \ ( B . 1 1 )$$

A random field Z is said to be Gaussian if, for each k ∈ N and all x1, . . . , xk ∈ X, the random vector (Z(x1), . . . , Z(xk)) has a multivariate normal distribution. Then the distribution of Z is determined by E[Z(x)], x ∈ X, and the covariance function of Z. A random field Z = (Z(x))x∈x is said to be centred if E[Z(x)] = 0 for each x ∈ X. The next theorem follows from Kolmogorov's existence theorem; see [63, Th. 6.16].

Theorem B.17 Let K: X × X → R be symmetric and non-negative definite. Then there exists a centred Gaussian random field with covariance function K.

The following result (see e.g. [59]) is an extension of the spectral theorem for symmetric non-negative matrices. It is helpful for the explicit construction of Gaussian random fields. Recall from Section A.2 that supp v denotes the support of a measure v on a metric space.

Theorem B.18 (Mercer's theorem) Suppose that X is a compact metric space. Let K: X × X → R be a symmetric, non-negative definite and continuous function. Let v be a finite measure on X. Then there exist γj ≥ 0 and v j ∈ L2(v), j ∈ N, such that

$$\int v _ { i } ( x ) v _ { j } ( x ) \, \nu ( d x ) = \mathbf 1 \{ \gamma _ { i } > 0 \} \mathbf 1 \{ i = j \} , \ \ i , j \in \mathbb { N } ,$$

and

$$K ( x , y ) = \sum _ { j = 1 } ^ { \infty } \gamma _ { j } v _ { j } ( x ) v _ { j } ( y ) , \quad x , y \in \sup v ,$$

where the convergence is absolute and uniform.


<!-- p:282 -->


If in Mercer's theorem j ∈ N is such that γj &gt; 0, then γj is an eigenvalue of K, that is ∫ K(x, y)vj(y) ν(dy) = γjvj(x), x ∈ supp ν. The eigenfunction v j is then continuous on supp v. There are no other positive eigenvalues.

A random field (Z(x))x∈x is said to be measurable if (ω, x) ↔ Z(ω, x) is a measurable function.

Proposition B.19 Let X be a locally compact separable metric space and let v be a measure on X which is finite on compact sets. Let X* denote the support of v. Let Z = (Z(x))x∈x be a centred Gaussian random field with a continuous covariance function. Then (Z(x))x∈x* has a measurable version.

Proof In principle, the result can be derived from [29, Th. II.2.6]. We give here another argument based on the Gaussian nature of the random field.

The set X* is closed and therefore a locally compact separable metric space in its own right; see Lemmas A.21 and A.22. Let v* be the measure on X* defined as the restriction of v to the measurable subsets of X*. It is easy to see that supp v* = X*. Therefore it is no restriction of generality to assume that X = X*.

Let us first assume that X is compact. Then the assertion can be deduced from a more fundamental property of Z, namely the Karhunen-Lòeve expansion; see [2]. Let K be the covariance function of Z. With γj and vj given as in Mercer's theorem (Theorem B.18), this expansion reads

$$Z ( x ) = \sum _ { j = 1 } ^ { \infty } \sqrt { \gamma _ { j } } Y _ { j } v _ { j } ( x ) , \quad x \in \mathbb { X } , \quad ( B . 1 4 )$$

where Y1, Y2,... are independent and standard normal random variables and the convergence is in L2(P). Since (B.13) implies Σj=1 γjνj(x)2 &lt; ∞, Proposition B.7 shows that the series in (B.14) converges almost surely. Let Z'(x) denote the right-hand side of (B.14), whenever the series converges. Otherwise set Z'(x) := 0. Then Z' is a measurable version of Z.

In the general case we find a monotone increasing sequence U, n ≥ 1, of open sets with compact closures B and ∪U = X. For n ∈ N let the measure vn on B be given as the restriction of v to B and let C ⊂ B be the support of v. Let v' be the measure on C given as the restriction of v to C. Then it is easy to see that supp v′ = C. From the first part of the proof we know that there is a measurable version (Z(x))xec. Since U is open it follows from the definition of the support of vn that Un ⊂ C. Hence there is a measurable version of (Z(x))xeU. Since ∪U = X it is now clear how to construct a measurable version of Z. □


<!-- p:283 -->


## Appendix C

## Historical Notes

### 1 Poisson and Other Discrete Distributions

The Poisson distribution was derived by Poisson [132] as the limit of binomial probabilities. Proposition 1.4 is a modern version of this limit theorem; see [63, Th. 5.7] for a complete statement. A certain Poisson approximation of binomial probabilities had already been used by de Moivre [111]. The early applications of the Poisson distribution were mostly directed to the "law of small numbers"; see von Bortkiewicz [17]. However, the fundamental work by de Finetti [39], Kolmogorov [77], Lévy [95] and Khinchin [71] clarified the role of the Poisson distribution as the basic building block of a pure jump type stochastic process with independent increments. Khinchin wrote in [70]: ".. genau so, wie die GaussLaplacesche Verteilung die Struktur der stetigen stochastischen Prozesse beherrscht ..., erweist sich die Poissonsche Verteilung als elementarer Baustein des allgemeinen unstetigen (sprungweise erfolgenden) stochastischen Prozesses, was zweifellos den wahren Grund ihrer großen Anwendungsfähigkeit klarlegt." A possible English translation is: ".. exactly as the Gauss-Laplace distribution governs the structure of continuous stochastic processes ..., it turns out that the Poisson distribution is the basic building block of the general discontinuous stochastic process (evolving by jumps), which undoubtedly reveals the true reason for its wide applicability."

### 2 Point Processes

The first systematic treatment of point processes (discrete chaos) on a general measurable phase space was given by Wiener and Wintner [160]. The vman ( n o moom o o vn oen oo first used by Moyal [116]. The results of this chapter along with historical comments can be found (in slightly less generality) in the monographs


<!-- p:284 -->


[27, 62, 63, 65, 69, 103, 82, 134]. The idea of Proposition 2.7 can be traced back to Campbell [19].

### 3 Poisson Processes

The Poisson process on the non-negative half-line was discovered several times. In a remarkable paper Ellis [32] introduced renewal processes and derived the Gamma distribution for the special case of an exponentially distributed time between successive events. In his study of risk processes, Lundberg [97] introduced the compound Poisson process, using what is now called Kolmogorov's forward equation; see Cramér [26] for a review of Lundberg's work. A similar approach was taken by Bateman [9] to derive the Poisson distribution for the occurrence of α-particles. Erlang [33] introduced the Poisson process to model a stream of incoming telephone calls. He obtained the Poisson distribution by a limit argument. Bateman, Erlang and Lundberg all based their analysis on an (implicit) assumption of independent increments.

Newcomb [118] used a rudimentary version of a spatial Poisson process to model the locations of stars scattered at random. The great generality of Poisson processes had been anticipated by Abbe [1]; see [148] for a translation. The first rigorous derivation and definition of a spatial Poisson process (Poisson chaos) was given by Wiener [159]. A few years later Wiener and Wintner [160] introduced the Poisson process on a general phase space and called this the completely independent discrete chaos. The construction of Poisson processes as an infinite sum of independent mixed binomial processes (implicit in [159]), as well as Theorem 3.9, is due to Moyal [116]; see also [74] and [105]. The conditional binomial property in Proposition 3.8 (again implicit in [159]) was derived by Feller [36] in the case of a homogeneous Poisson process on the line; see also Ryll-Nardzewski [144]. Theorem 3.9 was proved by Ryll-Nardzewski [144] for homogeneous Poisson processes on the line and by Moyal [116] in the general case. Further comments on the history of the Poisson process can be found in [27, 44, 53, 63, 65, 103].

### 4 The Mecke Equation and Factorial Measures

Theorem 4.1 was proved by Mecke [105], who used a different (and very elegant) argument to prove that equation (4.2) implies the properties of a Poisson process. Wiener and Wintner [160] used factorial moment measures as the starting point for their theory of point processes. Proposition


<!-- p:285 -->


4.3 is a slight generalisation of a result in [87]. Janossy measures and their relationship with moment measures were discussed in [160]. In the special case of a real phase space they were rediscovered by Bhabha [11]. The name was coined by Srinivasan [152], referring to Janossy [58]. Moment measures of random measures and factorial moment measures of simple point processes were thoroughly studied by Krickeberg [80] and Mecke [106]; see also [27] for an extensive discussion. Lemma 4.11 can be found in [116]. Proposition 4.12 can be derived from [162, Cor. 2.1].

### 5 Mappings, Markings and Thinnings

Mappings and markings are very special cases of so-called cluster fields, extensively studied by Kerstan, Matthes and Mecke in [69, 103]. The invariance of the Poisson process (on the line) under independent thinnings was observed by Rényi [136]. The general marking theorem (Theorem 5.6; see also Proposition 6.16) is due to Prékopa [133]. A special case was proved by Doob [29].

### 6 Characterisations of the Poisson Process

Proposition 6.7 was observed by Krickeberg [80]. A closely related result (for point processes) was derived in Wiener and Wintner [160, Sect. 12]. Theorem 6.10 was proved by Rényi [138], while the general point process version in Theorem 6.11 is due to Mönch [110]; see also Kallenberg [61]. Since a simple point process can be identified with its support, Theorem 6.10 is closely related to Choquet capacities; see [113, Th. 8.3] and [63, Th. 24.22]. A version of Rényi's theorem for more general phase spaces ad t  t a p  npn  t pn Poisson processes on the line are Poisson (Theorem 6.12) was noted by Erlang [33] and Bateman [9] and proved by Lévy [95] (in the homogeneous case) and by Copeland and Regan [24] (in the non-homogeneous case). In a more general Euclidean setting the result was proved in Doob [29] (in the homogeneous case) and Ryll-Nardzewski [143] (in the non-homogeneous case). For a general phase space the theorem was derived by Prékopa [133] and Moyal [116]. The general (and quite elegant) setting of a Borel state space was propagated in Kallenberg [63].


<!-- p:286 -->


### 7 Poisson Processes on the Real Line

Some textbooks use the properties of Theorem 7.2 to define (homogeneous) Poisson processes on the real half-line. The theorem was proved by Doob [29], but might have been folklore ever since the Poisson process was introduced in [9, 32, 33, 97]. Feller [36] proved the conditional uniformity property of the points, a fact that is consistent with the interval theorem. Another short proof of the fact that a Poisson process has independent and exponentially distributed interarrival times can be based on the strong Markov property; see e.g. [63]. The argument given here might be new. Doob [29] discussed non-homogeneous Poisson processes in the more general context of stochastic processes with independent increments. More details on a dynamic (martingale) approach to marked point processes on the real line can be found in the monographs [18, 88]. The Poisson properties of the process of record levels (see Proposition 7.7) was observed by Dwass [31]. The result of Exercise 7.15 was derived by Rényi [137]. A nice introduction to extreme value theory is given in [139].

### 8 Stationary Point Processes

Stationary point processes were introduced by Wiener and Wintner [160] and are extensively studied in [27, 69, 103, 85, 157]. The pair correlation function (introduced in [160]) is a key tool of point process statistics; see e.g. [8, 23, 53]. Krickeberg [81] is a seminal book on point process statistics. Khinchin [72] attributes Proposition 8.11 to Korolyuk. Proposition 8.13 is a special case of [103, Prop. 6.3.7]. The ergodic theorem for spatial point processes was discussed in [160]. Theorem 8.14 also holds in -nn    ss  n o o s e ss s so un ing a general spatial ergodic theorem. More information on spatial ergodic theory can be found in Chap. 10 of [63].

### 9 The Palm Distribution

The idea of Palm distributions goes back to Palm [122]. For stationary point processes on the line the skew factorisation of Theorem 9.1 is due 1s []    s dd  s ]  1s accommodate point processes on a locally compact Abelian group. Theorem 9.4 was proved by Mecke [105]. A preliminary version for stationary Poisson processes on the line was obtained by Slivnyak [151]. The formulae of Exercise 9.4 are due to Palm [122] and Khinchin [72]. For stationary point processes on the line Proposition 9.5 was proved by Ryll-Nardzewski [145], while the general case is treated in [69]. Theorem 9.6 can be seen as a special case of the inversion formula proved in Mecke [105]. Volume biasing and debiasing is known as the waiting time paradox. It was studied independently by Nieuwenhuis [120] for stationary point processes on the line and by Thorisson [157], who also studied the spatial case; see the notes to Chaps. 8 and 9 in [157] for an extensive discussion and more references. Stationary Voronoi tessellations are studied in [23, 147]. Equation (9.22) is an example of a harmonic mean formula; see Aldous [3].


<!-- p:287 -->


### 10 Extra Heads and Balanced Allocations

The extra head problem for a sequence of independent and identically distributed Bernoulli random variables was formulated and solved by Liggett [96]. This problem, as well as the point process version (10.1), are special cases of a shift-coupling. Thorisson [156] proved the existence of such couplings in a general group setting; see [157] for a discussion and more references. Stable allocations balancing Lebesgue measure and the stationary Poisson process were introduced and studied by Holroyd and Peres [49]. A discussion of balancing more general jointly stationary random measures can be found in [93] and [64]. Algorithm 10.6 (proposed in [48]) is a spatial version of an algorithm developed by Gale and Shapley [41] for the so-called stable marriage problem in a discrete non-spatial setting. Theorem 10.2 is taken from [84]. The modified Palm distribution was discussed in [69, Sec. 3.6] and [103, Sec. 9.1]. It was rediscovered in [120, 157].

### 11 Stable Allocations

The chapter is based on the article [48] by Hoffman, Holroyd and Peres. Algorithm 11.3 (taken from [49]) is another spatial version of the celebrated Gale-Shapley algorithm. In 2012 the Nobel Prize in Economics was awarded to Lloyd S. Shapley and Alvin E. Roth for the theory of stable allocations and the practice of market design. In the case of a finite measure Q, Exercise 10.1 is a special case of [103, Prop. 6.3.7].

### 12 Poisson Integrals

Multiple stochastic integrals were introduced by Wiener [159] and Itô [55, 56]. The pathwise identity (12.9) was noted by Surgailis [154]. Multiple Poisson integrals of more general integrands were studied by Kallenberg and Szulga [66]. Multiple point process integrals and an associated com-lk  s  s  ss ie i ekr berg [80] proved a version of Prop. 12.6 for general point processes. Theorem 12.7 can be found in [92, 125, 154]. Theorems 12.14 and 12.16 as well as Corollary 12.18 are taken from [92]. The results of Exercises 12.7 and 12.8 are special cases of formulae for the product of stochastic integrals; see Kabanov [60] and Proposition 1.5.3 in [87].


<!-- p:288 -->


### 13 Random Measures and Cox Processes

Doubly stochastic Poisson processes were introduced by Cox [25] and systematically studied in [43, 69, 103, 99]. Kallenberg [62, 65] gives an introduction to the general theory of random measures. Theorem 13.7 was proved by Krickeberg [79]. Theorem 13.11 was proved by Kallenberg [61]; see also Grandell [43]. The Poisson characterisation of Exercise 13.15was proved by Fichtner [38]. The present short proof is taken from [117]. In the special case of random variables the result was found by Moran [115].

### 14 Permanental Processes

Permanental processes were introduced into the mathematics literature by Macchi [98, 99] as rigorous point process models for the description of bosons. In the case of a finite state space these processes were introduced and studied by Vere-Jones [158]. Theorem 14.6 is due to Macchi [98]; see also Shirai and Takahashi [150]. Theorem 14.8 was proved by Macchi [98] (in the case α = 1) and Shirai and Takahashi [150]. Proposition 14.9 is from [150], although the present proof was inspired by [104]. Under a different assumption on the kernel it was proved in [150] that α-permanental processes exist for any α &gt; 0; see also [158]. A survey of the probabilistic properties of permanental and determinantal point processes can be found in [51]. Theorem 14.10 is taken from this source. The Wick formula of Lemma 14.5 can e.g. be found in [125].

We have assumed continuity of the covariance kernel to apply the classical Mercer theorem and to guarantee the existence of a measurable version of the associated Gaussian random field. However, it is enough to assume that the associated integral operator is locally of trace class; see [150].


<!-- p:289 -->


### 15 Compound Poisson Processes

Proposition 15.4 can be found in Moyal [116]. Proposition 15.8 can be seen as a specific version of a general combinatorial relationship between the moments and cumulants of random variables; see e.g. [27, Chap. 5] or [125]. The explicit Lévy-Khinchin representation in Theorem 15.11 was derived by Kingman [74]. This representation also holds for Lévy processes (processes with homogeneous and independent increments), a generalisation of the subordinators discussed in Example 15.7. In this case the result was obtained in de Finetti [39], Kolmogorov [77], Lévy [95], Khinchin [71, 73] and Itô [54]. The reader might wish to read the textbook [63] for a modern derivation of this fundamental result. The present proof of Proposition 15.12 (a classical result) is taken from the monograph [65]. The shot noise Cox process from Example 15.14 was studied by Møller [109]. Exercises 15.13 and 15.15 indicate the close relationship between infinite divisibility and complete independence. Seminal contributions to the theory of infinitely divisible point processes were made by Kerstan and Matthes [68] and Lee [94]. We refer here to [62, 65, 69, 103] and to [63] for the case of random variables and Lévy processes. An early paper on the Dirichlet distribution is Ferguson [37].

### 16 The Boolean Model and the Gilbert Graph

The spherical Boolean model already has many features of the Boolean model with general grains (treated in Chapter 17) while avoiding the technicalities of working with probability measures on the space of compact (convex) sets. Theorem 16.4 on complete coverage can be found in Hall [45]. In the case of deterministic radii the Gilbert graph was introduced by Gilbert in [42] and was extensively studied in [126]. The process of isolated nodes is also known as the Matérn I process; see [23]. This dependent thinning procedure can be generalised in several ways; see e.g. [155].

### 17 The Boolean Model with General Grains

The first systematic treatment of the Boolean model was given by Matheron [101]. Theorem 17.10 is essentially from [101]. We refer to [23, 45, 147] for an extensive treatment of the Boolean model and to [101, 113, 147] for the theory of general random closed sets. Percolation properties of the Boolean model are studied in [42, 45, 107].


<!-- p:290 -->


### 18 Fock Space and Chaos Expansion

The Fock space representation (Theorem 18.6) was proved in [90]. The chaos expansion of square integrable Poisson functionals (Theorem 18.10) as a series of orthogonal multiple Wiener-Itô integrals was proved by Itô [56]. The associated completeness property of multiple Poisson integrals was derived earlier in [160]; see also [159] for the Gaussian case. The present explicit version of the chaos expansion (based on the difference operators) was proved by Y. Ito [57] for homogeneous Poisson processes on the line, and in [90] for general Poisson processes. The Poincaré inequality of Theorem 18.7 was proved in Wu [161] using the Clark-Ocone representation of Poisson martingales. Chen [22] established this inequality for infinitely divisible random vectors with independent components.

### 19 Perturbation Analysis

In the context of a finite number of independent Bernoulli random variables Theorem 19.4 can be found in Esary and Proschan [34]. Later it was rediscovered by Margulis [100] and then again by Russo [142]. The Poisson version (19.3) is due to Zuyev [163] (for a bounded function f). In fact, this is nothing but Kolmogorov's forward equation for a pure birth process. Theorem 19.3 was proved (under stronger assumptions) by Molchanov and Zuyev [114]. For square integrable random variables it can be extended to certain (signed) σ-finite perturbations; see [86]. The present treatment of integrable random variables and finite signed perturbations might be new. A close relative of Theorem 19.4 for general point processes (based on a different difference operator) was derived in [14, 15]. Theorems 19.7 and 19.8 are classical results of stochastic geometry and were discovered by Miles [108] and Davy [28]. While the first result is easy to guess, Theorem 19.8 might come as a surprise. The result can be generalised to all intrinsic volumes of an isotropic Boolean model in Rd; see [147]. The present approach via a perturbation formula is new and can be extended so as to cover the general case. The result of Exercise 19.8 is taken from [40]. Exercise 19.11 implies the classical derivative formula for independent Bernoulli random variables.

### 20 Covariance Identities

Mehler's formula from Lemma 20.1 was originally devised for Gaussian processes; see e.g. [121]. The present version for Poisson processes as well as Theorem 20.2 are taken from [89]. Other versions of the covariance identity of Theorem 20.2 were derived in [22, 50, 90, 129, 161]. Theorem 20.3 is closely related to the Clark-Ocone martingale representation; see [91]. The Harris–FKG inequality of Theorem 20.4 was proved by Roy [141] by reduction to the discrete version for Bernoulli random fields; see [46]. An elegant direct argument (close to the one presented here) was given by Wu [161].


<!-- p:291 -->


### 21 Normal Approximation of Poisson Functionals

The fundamental Theorem 21.1 was proved by Stein [153]. Theorem 21.2 appears in the seminal paper by Peccati, Solé, Taqqu and Utzet [124] in a slightly different form. The second order Poincaré inequality of Theorem 21.3 was proved in [89] after Chatterjee [21] proved a corresponding result for Gaussian vectors. Abbe [1] derived a quantitative version of the normal approximation of the Poisson distribution; see Example 21.5. The normal approximation of higher order stochastic integrals and Poisson U-statistics was treated in [124] and in Reitzner and Schulte [135]. Many Poisson functionals arising in stochastic geometry have a property of stabilisation (local dependence); central limit and normal approximation theorems based on this property have been established in [128, 130, 131]. More examples for the application of Poisson process calculus to stochastic geometry can be found in [123].

### 22 Normal Approximation in the Boolean Model

Central limit theorems for intrinsic volumes and more general additive functions of the Boolean model (see Theorem 22.8) were proved in [52]. The volume was already studied in Baddeley [7]. The surface content was treated in Molchanov [112] before Heinrich and Molchanov [47] treated more general curvature-based non-negative functionals. A central limit theorem for the number of components in the Boolean model was established in [127]. Theorem 22.9 is new but closely related to a result from [52]. Using the geometric inequality [52, (3.19)] it is possible to prove that the condition from Exercise 22.4 is not only sufficient, but also necessary for the positivity (22.32) of the asymptotic variance.


<!-- p:292 -->

## Index

| absolute continuity, 244                                    | Cauchy sequence, 251                            |
|-------------------------------------------------------------|-------------------------------------------------|
| absolutely continuous function, 259                         | Cauchy-Schwarz inequality, 243                  |
| additive function                                           | central limit theorem, 219, 267                 |
| on a measurable space, 241                                  | centre function, 184                            |
| on the convex ring, 203, 255                                | centred random field, 270                       |
| allocation, 93                                              | chaos expansion, 194                            |
| balanced, 94, 101                                           | characteristic function, 263                    |
| stable, 103                                                 | characteristic functional, 14                   |
| almost sure convergence, 263                                | Choquet capacity, 274                           |
| almost sure equality                                        | circumball, 184                                 |
| of point processes, 11 158                                  | Clark-Ocone martingale representation,          |
| of random measures,                                         | 279                                             |
| arrival time, 59                                            | closed set, 250                                 |
| atom, 240                                                   | closure of a set, 250                           |
| ball, 16, 250                                               | cluster field, 274                              |
|                                                             | compensated integral, 112                       |
| binomial distribution, 1 process, 11                        | complete independence                           |
| binomial mixed, 21                                          | of a point process, 19 of a random measure,     |
| block, 115                                                  | 154                                             |
| Boolean model, 167, 179                                     | complete orthogonality, 53                      |
| capacity functional, 180                                    | complete randomness                             |
| central limit theorem, 230                                  | of a point process, 19 of a random measure, 154 |
| covariance, 183                                             | complete separable metric space                 |
| grain distribution, 179                                     | (CSMS), 251                                     |
| linear contact distribution, 171 mean Euler characteristic, | completeness of L p , 243                       |
| 207                                                         | component, 172                                  |
| spherical, 167 spherical contact distribution, 170, 182     | compound Poisson process, 153                   |
| stationarity, 182                                           | symmetric, 155 conditional distribution, 269    |
| surface density, 206                                        | regular version, 269                            |
| volume fraction, 168,                                       |                                                 |
| 181                                                         | conditional expectation, 268 268                |
| with general grains, 179                                    | conditional probability,                        |
| Borel -field, 251                                           | convergence                                     |
| Borel space, 46                                             | almost sure, 263                                |
| Borel subspace, 46, 251                                     | in a metric space, 250                          |
| boundary of a set, 250                                      | in a topological space, 252                     |
|                                                             | in distribution, 264                            |
| Campbell's formula, 13, 128                                 |                                                 |
| capacity functional, 167, 180                               | in probability, 263                             |


<!-- p:301 -->


#### Index

flow property, 69

invariant σ-field, 75

| convex body, 254                                  | Fock space, 189                                       |
|---------------------------------------------------|-------------------------------------------------------|
| convex ring, 203, 255                             | Fock space representation, 192                        |
| convex set, 254                                   | Fubini's theorem, 246                                 |
| convolution, 44                                   | Gale-Shapley                                          |
| counting measure, 9, 242                          | allocation 96                                         |
| with multiplicities, 10                           | point-optimal, site-optimal, 104                      |
| covariance, 262                                   | Gamma distribution, 6, 67, 134                        |
| covariance function, 270                          | Gamma function, 6                                     |
| covariance property, 93                           | Gamma process, 156                                    |
| Cox process, 129                                  | Gamma random measure, 156                             |
| shot noise, 162                                   | Gaussian random field, 270                            |
| CSMS, see complete separable metric               | generator, 239                                        |
| space                                             | geometric distribution, 6                             |
| cycle of a permutation, 136                       | geometric function, 231                               |
| length, 136                                       | Gilbert graph, 172                                    |
| dense subset, 251                                 | grain, 166                                            |
| density, 244                                      | grain distribution, 179                               |
| diagonal, 49                                      | graph, 171                                            |
| diagram, 115                                      | Hadwiger's characterisation theorem, 255              |
| diameter, 16, 252                                 | Hahn-Jordan decomposition, 244                        |
| di erence operator, 187, 211                      | harmonic mean formula, 276                            |
| Dirac measure, 9                                  | Harris-FKG inequality, 217                            |
| directing random measure, 129                     | Hausdor distance, 179, 255                            |
| directional distribution, 126                     | Hausdor measure, 253                                  |
| Dirichlet distribution, 163                       | hazard measure, 64, 258                               |
| disintegration, 247                               | H ̈ older's inequality, 243                            |
| displacement theorem, 44                          | image measure, 38                                     |
| distribution                                      | inclusion-exclusion principle, 255                    |
| of a point process, 14                            | increasing event, 209                                 |
| of a random element, 261 of a random measure, 128 | independence                                          |
| dominated convergence, 243                        | of random variables, 262                              |
| double factorial, 266                             | of -fields, 262                                       |
| Dynkin system, 240                                | independent increments, 19, 156                       |
| equality in distribution,                         | independent superposition, 20 125, 165                |
| 261 ergodic theorem, 77, 264                      | infinite divisibility,                                |
| ergodicity, 75                                    | integral, 242                                         |
| Euler characteristic, 207, 256                    | integral geometry, 206                                |
| expectation, 261                                  | intensity                                             |
| explosion, 59                                     | of a stationary point process, 70 random measure, 135 |
| exponential distribution, 6                       | of a stationary intensity measure                     |
| extra head problem, 93                            | of a point process,                                   |
| factorial measure, 28                             | 12 of a random measure, 128                           |
| factorial moment, 2                               | interior of a set, 250                                |
| factorial moment measure, 34                      | interval theorem, 59                                  |
| Fatou's lemma, 243                                | intrinsic volumes, 254                                |
| Fell topology, 256                                | additive extension, 256                               |
| field, 239                                        | additivity, 255                                       |
|                                                   | homogeneity, 254                                      |
| fixed atom, 160 flow property, 69                 | invariant -field, 75                                  |


<!-- p:302 -->


| inversion formula, 88                                | Mehler's formula, 212                                     |
|------------------------------------------------------|-----------------------------------------------------------|
| isolated point, 175                                  | Mercer's theorem, 270                                     |
| isometry, 112, 189                                   | method of moments, 267                                    |
| isotropic grain distribution, 205                    | metric, 250                                               |
| Janossy measures, 32                                 | metric space, 250                                         |
| Jensen's inequality, 262                             | complete, 251                                             |
| conditional, 269                                     | locally compact, 251                                      |
| Karhunen-L` oeve expansion, 271                      | separable, 180, 251 -compact, 251                         |
| kernel, 11, 246                                      | Minkowski inequality, 243                                 |
| probability, 40, 246                                 | Minkowski sum, 167, 253                                   |
| s -finite, 247                                       | mixed binomial process, 21                                |
| Laplace functional                                   | mixing property                                           |
| of a point process, 14 of a random measure, 128      | of a marked Poisson process, 101 of a Poisson process, 76 |
| Laplace transform, 2, 263                            | moment measure, 128                                       |
| law of total expectation, 269                        |                                                           |
| 252                                                  | monotone class theorem, 240                               |
| Lebesgue measure,                                    | functional version, 241                                   |
| L ́ evy measure, 155                                  | monotone convergence, 243                                 |
| lexicographic minimum, 70                            | monotone system, 239                                      |
| lexicographical order, 70                            | multinomial distribution, 7                               |
| Lipschitz function, 264                              | multiplicity, 10                                          |
| local square integrability, 71                       | mutual singularity, 244                                   |
| locally finite functional, 203                       | negative binomial distribution,                           |
| mapping theorem, 38                                  | 5 non-negative definite function, 270                     |
| mark, 40                                             | normal distribution, 266                                  |
| mark space, 40                                       | multivariate, 267                                         |
| marking, 40                                          | normal site, 105                                          |
| independent, 40 supported by a probability space, 40 | open set, 250, 252                                        |
| marking theorem, 42                                  | pair correlation function, 73                             |
| Markov's inequality, 264 matching, 120, 266          | isolated nodes, 176 permanental process,                  |
|                                                      | 139                                                       |
| mean ergodic theorem, 264 measurable mapping, 240    | Poisson cluster process, 91 Poisson process, 73           |
| measurable space, 240                                | distribution, 84                                          |
|                                                      | Palm                                                      |
| measure, 241                                         | modified, 101                                             |
| di use, 16, 49                                       | Palm version, 85 90                                       |
| locally finite, 16, 253 power, 246                   | Palm-Khinchin equations, parallel set, 253 partition, 115 |
| purely                                               |                                                           |
| discrete, 56 s -finite, 10, 244                      | permanent, 137                                            |
| -finite, 10, 242                                     | permanental process, 137, 138                             |
| signed, 36, 198, 244                                 | permutation, 8, 114                                       |
| simple, 49                                           | -system, 15, 239                                          |
| symmetric, 250                                       | pivotal point, 209                                        |
| space, 242                                           | Poincar ́ e inequality, 193                                |
| measure                                              |                                                           |
| Mecke equation, 27 for Cox processes,                | point process, 11 completely                              |
|                                                      | independent,                                              |
| 131 multivariate, 30, 31                             | 19 completely orthogonal, 53                              |
|                                                      | ergodic, 75                                               |
| 85                                                   |                                                           |
| Mecke-Slivnyak theorem,                              |                                                           |


<!-- p:303 -->


#### 292 Index

| infinitely divisible, 165                               | measurable, 128, 271                                |
|---------------------------------------------------------|-----------------------------------------------------|
| locally finite, 16                                      | moving average, 162                                 |
| mixing, 76                                              | shot noise, 162                                     |
| ordinary, 58                                            | random geometric graph, 172                         |
| proper, 12                                              | random measure, 127                                 |
| pseudo-ergodic, 97                                      | completely independent, 154                         |
| simple, 49                                              | di use, 133, 158                                    |
| stationary, 70                                          | locally finite, 133                                 |
| uniformly -finite, 48                                   | self-similar, 164                                   |
| Poisson cluster process, 45                             | stationary, 135                                     |
| stationary, 80                                          | uniformly -finite, 158                              |
| Poisson distribution,                                   | random variable, 261                                |
| 1                                                       | integrable, 261                                     |
| Poisson functional, 211 Poisson hyperplane process, 123 | square integrable, 261                              |
| stationary, 126                                         | random vector, 262                                  |
| Poisson hyperplane tessellation, 123                    | rate, 59                                            |
| Poisson process, 19                                     | record,                                             |
| compound, 153                                           | 63 reduced second factorial moment                  |
| doubly stochastic, 127                                  | measure, 72                                         |
| homogeneous, 59                                         | refined Campbell theorem, 82                        |
| mixed, 134                                              | reflection, 180                                     |
| non-homogeneous,                                        |                                                     |
| 60 stationary, 59, 84                                   | relatively compact set, 136                         |
| Poisson U-statistic, 118                                | R ́ enyi's theorem, 50                               |
|                                                         | representative, 211                                 |
| degenerate, 119                                         | restriction of a measure, 32, 245 measurability, 80 |
| polar representation process,                           | 65 Riemann rotation, 253                            |
| of a homogeneous Poisson of Lebesgue measure, 66        |                                                     |
| polarisation, 192                                       | sample intensity, 80                                |
| power series representation, 200                        | second order Poincar ́ e inequality, 280 shift, 69   |
| probability generating functional, 25                   | shift-coupling, 276                                 |
| probability kernel, 40                                  | shot noise, 162                                     |
| probability measure, 261                                | -additivity, 241                                    |
| probability space, 261                                  | -field, 239                                         |
| product measure, 246                                    | signed measure, 198, 244                            |
| product of measurable spaces, 241                       | simple function, 15, 242                            |
| product -field, 241                                     | simplex, 163                                        |
| product topology, 257                                   | site, 69                                            |
| proper rotation, 253                                    | spatial ergodic theorem, 77                         |
| pseudo-ergodic point process, 97                        | spherical Lebesgue measure, 65                      |
| p -thinning, 43                                         | stabilisation, 280                                  |
| pull out property, 269                                  | stable allocation, 103                              |
| push-forward, 38                                        | standard normal distribution, 266                   |
| Radon-Nikod ́ ym derivative                              | stationarity                                        |
| of a function, 259                                      | of a Boolean model, 182                             |
| of a measure, 244                                       | of a permanental process,                           |
| Radon-Nikod ́ ym theorem, 244                            | 139 of a point process on R d , 69                  |
| random element, 261                                     | of a point process on R + , 59 d 70                 |
| random field, 128, 269                                  | of a Poisson process on R ,                         |
|                                                         | of a random field, 165                              |
| covariance function, 141                                |                                                     |
|                                                         | of a random measure, 135                            |
| Gaussian, 141                                           |                                                     |

of a random measure, 135


<!-- p:304 -->


```
Index)

of a sequence of random variables, 264
Stein's equation, 267
Stein's method, 220
Steiner formula, 254
Stirling numbers, 151
subordinator, 156
subpartition, 115
supersession theorem, 20
support
    of a counting measure, 70
    of a measure, 252
symmetric function, 114
tensor product, 116
thinning
    of a point process, 43
    of a random variable, 3
thinning theorem, 44
time transform, 60
topological space, 252
topology, 252
    second countable, 256
total variation measure, 201, 244
totally infinite measure, 245
trace-gefield, 240
translation invariance
    of a function on C, 231
    of a measure on R, 70
triangle inequality, 250
    of integration, 243
typical cell, 87
uniform randomisation, 57
unit ball, 65, 253
unit sphere, 65
variance, 261
version of a random field, 270
volume, 252
volume-biased distribution, 89
volume-debiased distribution, 89
Voronoi cell, 87
Voronoi tessellation, 87
waiting time paradox, 276
Wasserstein distance, 219
Wick formula, 139
Wiener-It6 integral, 114
    m-th order, 118
zero measure, 9
zero-cell, 89

```
