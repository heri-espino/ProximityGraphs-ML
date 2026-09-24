---
id: "Devroye_2009_Maximum-Degree-Gabriel-Yao-Graphs"
source_pdf: "../pdf/Devroye_2009_Maximum-Degree-Gabriel-Yao-Graphs.pdf"
source_filename: "Devroye_2009_Maximum-Degree-Gabriel-Yao-Graphs.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "excellent"
extraction_score: 100.0
visual_assets: "disabled"
references_file: "../references/Devroye_2009_Maximum-Degree-Gabriel-Yao-Graphs.references.md"
---

<!-- p:1 -->

## ON THE EXPECTED MAXIMUM DEGREE OF GABRIEL AND YAO GRAPHS

Luc Devroye Joachim Gudmundsson Pat Morin November 2, 2018

ABSTRACT. Motivated by applications of Gabriel graphs and Yao graphs in wireless ad-hoc networks, we show that the maximal degree of a random Gabriel graph or Yao graph defined on n points drawn uniformly at random from a unit square grows as Θ(log n/ log log n ) in probability.

## 1 Introduction

Wireless ad-hoc networks consist of computers (or sensors) capable of communicating wirelessly with each other without any centralized information, infrastructure, or organization. A common mathematical model of such networks is the unit disk graph in which the nodes consist of n points in R 2 and an edge exists between two nodes if and only if the distance between them is at most r . Depending on the value of r , which represents the transmission range of the wireless transmitters, the network can be anything ranging from a set of isolated vertices to the complete graph.

The lack of centralized management and organization that occurs in ad-hoc networks means that individual nodes in the network typically only have local information about the nodes that they can communicate directly with. This makes even basic tasks, such as routing, highly non-trivial because the combination of complete lack of organization and the unit disk graph topology is too unwieldy.

One approach to taming ad-hoc networks has been to compute the intersection of the unit disk graph with some 'nice' proximity graph. If the right proximity graph is chosen, the resulting graph will remain connected (if the original unit disk graph is connected) and will inherit some of the nice properties of the proximity graph. Ideally, the intersection can be computed locally, so that individual nodes can locally determine which of their incident edges belong to the intersection.

One such approach computes the intersection of the unit disk graph with the Gabriel graph [9]. The Gabriel graph contain an edge between two points u and v if and only if the disk whose diameter is uv contains no points other than u and v (see Figure 1). The Gabriel graph is planar and therefore has only a linear number of edges. Algorithms for routing on planar graphs can be applied to the resulting graph or, more commonly, these algorithms can be used for recovery when routing heuristics fail. A number of routing algorithms and protocols have been proposed based on this strategy [2, 4, 12].

Another suggested approach uses the Yao graph [25]. Refer to Figure 2. Let p be a positive integer, let θ = 2 π/p , and let u be a point in R 2 . The i -cone of u is the set of all points w ∈ R 2 such that ∠ quw ∈ [( i - 1) θ, iθ ) , where q = u +(1 , 0) . The θ -Yao graph contains an edge from u to the nearest point in each of u 's i -cones, for i = 1 , . . . , p . For any constant p ≥ 6 , the θ -Yao graph has at most pn edges and is a spanner ; for any two vertices u and v , the θ -Yao graph contains a path whose Euclidean length is at most t · ‖ uv ‖ , where ‖ uv ‖ denotes the Euclidean distance between u and v and t = 1 / (1 - 2 sin( θ/ 2)) is called the stretch factor . When applied in the context of unit disk graphs, if there is a path of Euclidean length ‖ uv ‖ U in the original unit disk graph, then there is a path of length at most t · ‖ uv ‖ U in the intersection of the unit disk graph and the θ -Yao graph. Routing strategies based on the Yao graph attempt to find power-efficient routing paths [11, 13, 18, 19].


<!-- p:2 -->


Figure 1: A point set with its Gabriel graph. No circle has any data point in its interior and every circle has an edge as its diameter.

### 1.1 New Results

Motivated by the above applications in wireless networks, the current paper studies the Gabriel graph and Yao graph of n points uniformly and independently distributed in a unit square. This distribution assumption can be used to approximately model the unorganized nature of ad-hoc networks and is commonly used in simulations of such networks [24]. Additionally, some types of sensor networks, especially with military applications, are specifically designed to be deployed by randomly placing (scattering) them in the deployment area. This distribution assumption models these applications very well.

We show that the maximum degree of any node in a Gabriel graph or a Yao graph is concentrated at Θ(log n/ (log log n )) . 1 More specifically, if ∆ is the maximum degree of either graph, then we show that there exists constants a and b , such that

$$\lim _ { n \to \infty } \Pr \left \{ \Delta \in \left [ \frac { a \log n } { \log \log n } , \frac { b \log n } { \log \log n } \right ] \right \} & = 1 \ . \\$$

1 Throughout this paper log x denote the natural logarithm of x .


<!-- p:3 -->

Figure 2: The edges defined by a node u in a ( π/ 3) -Yao graph.

For Gabriel graphs, we show this for ( a, b ) = (1 / 12 , 1) and for Yao graphs we show it for ( a, b ) = (1 / 8 , 4) . The maximum degree is particularly important in wireless networks, since the degree of a node directly impacts the amount of bookkeeping the node must do. With wireless nodes typically being battery operated and often memory- and computation-constrained, the degree of a node should hopefully be as small as possible in order to minimize this bookkeeping.

### 1.2 Related Work

A random Gabriel graph in this paper is a Gabriel graph for n points drawn uniformly and at random from [0 , 1] d . Its key properties were studied in great depth by Matula and Sokal [14]. For example, the expected number of edges grows as 2 d - 1 n [8, 14]. The length of an edge taken at random from all edges has expected value and standard deviation Θ( n - 1 /d ) [8]. These properties hold also for many non-uniform distributions [8].

For a uniform Poisson process, introduced to avoid edge effects, Bern, Eppstein and Yao [3] showed that the expected value of the maximal degree of a Delaunay triangulation grows as Θ(log n/ log log n ) . For that model, their proof also works for Gabriel graphs. It is known that the Gabriel graph is a subgraph of the Delaunay triangulation (see Toussaint [20]), so that our upper bound would in fact follow without too much work from the cited paper. Our work on Gabriel graphs differs in three aspects:

1. Weshowconvergence in probability: the fact that the expected maximal degree grows as Θ(log n/ log log n ) does not imply that the probability of obtaining such large maximal degrees tends to one. We show it does.
2. We deal with a fixed sample size model on a compact set, not the Poisson model on the entire plane.
3. Our proofs are different.

The relative neighborhood graph is obtained by joining all pairs whose loon is empty, where the loon defined by a pair is the intersection of two spheres of equal radius, each having one point as center and the other point on its surface (see Toussaint [21]). As it is a subgraph of the Gabriel graph, our results imply that its maximal degree is O (log n/ log log n ) in probability. For a general discussion of proximity graphs and their applications, we refer to the survey papers by Toussaint [20, 22]. For an application of the relative neighbourhood graph to wireless networks, see Karp and Kung [12].


<!-- p:4 -->


To the best of our knowledge, random Yao graphs have not been studied previously. Although researchers have been interested in spanners having small maximum degree (see, the textbook by Narasimhan and Smid [16] for a survey), most research in this area has been on constructing spanners that have low degree in the worst-case. Some of these constructions have been adapted for use in the unit disk graph model of wireless networks [23], but the computation of these spanners is not quite as straightforward and local as that of Yao graphs.

The remainder of this paper is organized as follows. Section 2 presents our results on Gabriel graphs. Section 3 presents our results on Yao graphs. Each of these sections concludes with a summary and discussion of possible generalizations and limitations.

## 2 Gabriel Graphs

In this section, we prove bounds on the maximum degree of vertices in a Gabriel graph. Before we begin, we discuss an equation that is central to all our upper and lower bound, as well as many other bounds of this type.

Let c &gt; 0 be a constant, and let k = c log n/ log log n . In all our bounds, the value k k appears at some point in the computations. Note that

$$k ^ { k } = n ^ { c ( 1 + \frac { \log c \, \log \log \log n } { \log \log n } ) } = n ^ { c - o ( 1 ) } \ .$$

In particular, k = O ( n c ) and, for any ǫ &gt; 0 , k = Ω( n c - ǫ ) .

### 2.1 A lower bound

In this section, we prove the following result.

Theorem 1. For a random Gabriel graph defined on n points drawn independently from the uniform distribution on [0 , 1] 2 ,

$$\lim _ { n \to \infty } \Pr \left \{ \max { \text {algebraic degree} } < \frac { c \log n } { \log \log n } \right \} = 0$$

for all c &lt; 1 / 12 .

Proof. We start with a technical construction of a region and then a point configuration. Given an integer k and positive number r . Define the angle ξ = 2 π/ (3 k ) , and partition the plane into 3 k sectors of angle ξ each, with center at the origin. We refer to Figure 3 for further explanations.

Draw two concentric circles of radii r and R with R &gt; r , so that r = R cos ξ . If the sectors are numbered C 1 , C 2 , . . . , C 3 k (clockwise) and the circles are S r and S R , then we mark k regions (shown in darker color in Figure 3). These regions are of the form ( S R - S r ) ∩ ( C 3 i +1 ∪ C 3 i +2 ) for 0 ≤ i ≤ k - 1 .


<!-- p:5 -->


Figure 3: The definition of a pearl

<!-- p:6 -->


Call these regions pearl regions and denote them by P 1 , . . . , P k . Any circle with its diameter being the segment linking the origin with any point in a pearl region totally avoids any other pearl region. To see this, refer to Figure 3 and recall that r = R cos ξ .

Assume we are given m points in the plane, x 1 , . . . , x m and a center x . If x + A denotes the translate of a set A by x , then we call x a tiara for x 1 , . . . , x m if exactly k of the points x i fall in x + S R , and if each set x + P j covers exactly one of these x i 's. If we construct the Gabriel graph for x, x 1 , . . . , x m , then the degree of the vertex at x is at least k if x is a ( k, r ) tiara for x 1 , . . . , x m .

̸

The above construction and definitions are for any point sets. Assume that a random sample of size n is drawn from the uniform distribution on [0 , 1] 2 , and denote it by X 1 , . . . , X n . Define k = max(3 , ⌊ c log n/ log log n ⌋ ) and r = 1 / √ n . We say that X i is a jewel if X i is a ( k, r ) tiara for { X j : j = i } and if X i is at distance at least 2 r from the perimeter of [0 , 1] 2 . Note that R ≤ 2 r , so that X i + P j ⊆ [0 , 1] 2 for all j .

We compute the probability that X 1 is a jewel given X 1 = x , provided that x is at distance at least 2 r from the perimeter of the unit square. Note that this probability may be written as a multinomial probability. If p is the area of x + P j , we have in particular,

$$b a b i l i . \, \text {If } p \text { is the area of } x + P _ { j } , \, \text {we have in particular,} \\ \Pr \{ X _ { 1 } \text { is a jewel} | X _ { 1 } = x \} & = \frac { ( n - 1 ) ! } { ( n - 1 - k ) ! } \prod _ { j = 1 } ^ { k } p \times ( 1 - \pi R ^ { 2 } ) ^ { n - 1 - k } \\ & = \frac { ( n - 1 ) ! } { ( n - 1 - k ) ! } \prod _ { j = 1 } ^ { k } p \times ( 1 - \pi / n \cos ^ { 2 } \xi ) ^ { n - 1 - k } \\ & \geq \frac { ( n - 1 ) ! } { ( n - 1 - k ) ! } \prod _ { j = 1 } ^ { k } p \times ( 1 - 2 \pi / n ) ^ { n - 1 - k } \quad [ \text {since $\xi \leq 2\pi/9 < \pi/4$} ] \\ & \geq ( n - k ) ^ { k } p ^ { k } ( 1 - 2 \pi / n ) ^ { n } \\ & \geq ( n - k ) ^ { k } p ^ { k } ( 1 / 3 ) ^ { 2 \pi } \quad . \\ \text {As } k \geq 3 , \, \text {we have $\xi \leq 2\pi/9 < 1$, so that $\tan \xi = \sin \xi / \cos \xi \geq \xi$. Therefore,} \\ & \quad n - ( R ^ { 2 } - r ^ { 2 } ) \epsilon - R ^ { 2 } \epsilon \sin ^ { 2 } \epsilon - r ^ { 2 } \epsilon \tan ^ { 2 } \epsilon > \epsilon ^ { 3 } / n \\$$

As k ≥ 3 , we have ξ ≤ 2 π/ 9 &lt; 1 , so that tan ξ = sin ξ/ cos ξ ≥ ξ . Therefore,

Resubstitution yields

$$p = ( R ^ { 2 } - r ^ { 2 } ) \xi = R ^ { 2 } \xi \sin ^ { 2 } \xi = r ^ { 2 } \xi \tan ^ { 2 } \xi \geq \xi ^ { 3 } / n \ .$$

$$y i e l d y e l d \\ \Pr \{ X _ { 1 } \, \text { is a jewel} | X _ { 1 } = x \} & \geq ( n - k ) ^ { k } \frac { \xi ^ { 3 k } } { n ^ { k } } \left ( \frac { 1 } { 3 } \right ) ^ { 2 \pi } \\ & = \left ( 1 - \frac { k } { n } \right ) ^ { k } \left ( \frac { 1 } { 3 } \right ) ^ { 2 \pi } \xi ^ { 3 k } \\ & = \left ( 1 - \frac { k } { n } \right ) ^ { k } \left ( \frac { 1 } { 3 } \right ) ^ { 2 \pi } \left ( \frac { 2 \pi } { 3 } \right ) ^ { 3 k } k ^ { - 3 k } \\ & \geq k ^ { - 3 k } \\ \text {large enough, uniformly over all } x \text { at distance at least } 2 r \text { from the perimeter of the } u \text { } \\ \text {wrap uncondition. If } N \text { is the number of jewelys among the data points, we have }$$

when n is large enough, uniformly over all x at distance at least 2 r from the perimeter of the unit square. We may now uncondition. If N is the number of jewels among the data points, we have

$$E [ N ] = n \Pr \{ X _ { 1 } \text { is a jewel} \} \geq n ( 1 - 4 r ) ^ { 2 } k ^ { - 3 k } \sim n k ^ { - 3 k } \ . \\$$

If k is as we picked it, and c &lt; 1 / 3 , then E[ N ] →∞ . This is not quite enough to show that Pr { N &gt; 0 } → 1 . There are several routes one can follow at this point: one could Poissonize the sample size; one might redefine jewels so that at most one jewel occurs in any region of a regular grid. Both tricks create enough independence to get by. Instead, we opt to use the second moment method (for references, see Palmer (1985) or Alon, Spencer and Erd ̈ os (1992)). When applied to a counting random variable N = ∑ n i =1 Y i , where the Y i 's are { 0 , 1 } -valued with a permutation-invariant joint distribution, the second moment method implies that N/ E[ N ] → 1 in probability whenever E[ N ] →∞ and


<!-- p:7 -->


$$\lim _ { n \to \infty } \sup _ { \substack { E [ Y _ { 1 } ] E [ Y _ { 2 } ] \\ } } \frac { E [ Y _ { 1 } Y _ { 2 } ] } { E [ Y _ { 1 } ] E [ Y _ { 2 } ] } \leq 1 \ .$$

In our case, we only need to verify the latter condition when Y i is the indicator that X i is a jewel, so that N is the number of jewels. Let A be the event that X 1 or X 2 is within 2 r of the perimeter of the unit square, or that ‖ X 1 - X 2 ‖ ≤ 4 r . On A c , the complement of A , we have, by the multinomial argument given above, but now applied to two tiaras,

$$E [ Y _ { 1 } Y _ { 2 } | A ^ { c } ] & = \frac { ( n - 2 ) ! } { ( n - 2 - 2 k ) ! } p ^ { 2 k } ( 1 - 2 \pi R ^ { 2 } ) ^ { n - 2 - 2 k } \ , \\$$

where p is the area of a pearl region P j . We recall that

$$E [ Y _ { 1 } ] \geq \frac { ( n - 1 ) ! } { ( n - 1 - k ) ! } p ^ { k } \left ( 1 - \pi R ^ { 2 } \right ) ^ { n - 1 - k } \geq k ^ { - 3 k } \\ \text {Thus, for such large $n$,}$$

for n large enough. Thus, for such large n ,

$$\text { for } n \, \text { large enough.  Thus, for such large $n$,} \\ \frac { E [ Y _ { 1 } Y _ { 2 } ] } { E [ Y _ { 1 } ] E [ Y _ { 2 } ] } & = \frac { \Pr \{ A \} E [ Y _ { 1 } Y _ { 2 } | A ] } { E [ Y _ { 1 } ] E [ Y _ { 2 } ] } + \frac { \Pr \{ A ^ { * } \} E [ Y _ { 1 } Y _ { 2 } | A ^ { * } ] } { E [ Y _ { 1 } ] E [ Y _ { 2 } ] } \\ & \overset { < } { \Pr } ( A ) ^ { 2 } + \frac { E [ Y _ { 1 } Y _ { 2 } | A ] } { E [ Y _ { 1 } ] E [ Y _ { 2 } ] } \\ & \leq \frac { 8 r + 1 6 \pi r ^ { 2 } } { E [ X ] E [ Y _ { 2 } ] } + \frac { ( n - 2 ) ! } { ( n - 2 - 2 k ) ! } \rho ^ { 2 k } ( 1 - 2 \pi R ^ { 2 } ) ^ { n - 2 - 2 k } \times \frac { ( n - 1 - k ) ! ^ { 2 } } { ( n - 1 ) ! ^ { 2 } } p ^ { - 2 k } ( 1 - \pi R ^ { 2 } ) ^ { 2 k + 2 - 2 n } \\ & \leq \frac { - \pi ^ { 2 } / 2 - k ^ { 6 } } { n ^ { 1 / 2 } } + 1 + O ( k ^ { 2 / n } ) \, . \\ \intertext { We are done if $n ^ { 2 / k - 6 } \to \infty$.  For this, in the definition of $k$, we need only pick 6c < 1 / 2 , or c < 1 / 1 2 . }$$

We are done if n 1 / 2 k - 6 k →∞ . For this, in the definition of k , we need only pick 6 c &lt; 1 / 2 , or c &lt; 1 / 12 . We have thus shown that N/ E[ N ] → 1 in probability when c &lt; 1 / 12 in the definition of k . We conclude that Pr { N = 0 } → 0 for such choices of c . Therefore,

$$\lim _ { n \to \infty } \Pr \left \{ \text {Maximal degree in Gabriel graph} < \frac { c \log n } { \log \log n } \right \} & = 0 \\$$

for all c &lt; 1 / 12 . By Poissonization, or by tighter bounding above, the constant 1 / 12 can be improved.

### 2.2 An upper bound

Theorem 2. For a random Gabriel graph defined on n points drawn independently from the uniform distribution on [0 , 1] 2 ,

$$\lim _ { n \to \infty } \Pr \left \{ \max i m a l \deg r e e \, > \frac { c \log n } { \log \log n } \right \} = 0$$

for all c &gt; 1 .


<!-- p:8 -->


Figure 4: The shaded regions define a (7 , r ) tiara.

<!-- p:9 -->


Figure 5: The definition of a wedge

Proof. At a point x , partition the space into k equal sectors of angle 2 π/k each, where k = ⌈ √ log n ⌉ . Within each sector, we color the point nearest to x red if its distance is less than r = 3 √ log n/n . If a sector has a red point y , consider the perpendicular line at y to the segment ( y, x ) . Call this line the separator. All points in the same sector but at the same side as x of the separator are colored blue. In Figure 5, these are precisely the points that fall in the shaded wedge. Finally, among all points, color those yellow that are Gabriel neighbors and that are at least r away from x . We first claim that each Gabriel graph neighbor of x is colored red, blue or yellow. Indeed, any point y excludes all points at the other side of the separator-the side that does not contain x . Thus, if there is a red point in the sector, only blue points can possibly be Gabriel neighbors of x .

Figure 6 shows several points with their separators. No point in the shaded area can be a Gabriel neighbor of the point at the origin. Note that for every point in the shaded area, the Gabriel circle through the origin contains another point.

Figure 7 shows several sectors and red points, together with the wedges in which blue points must fall. The angle of each sector is θ = 2 π/k .

Let N r , N b , N y be the total number of red, blue and yellow points respectively. Clearly, N r ≤ k = o (log n/ log log n ) . Also, conditioning on X 1 = x ,

```
k = o(log n/ log log n). Also, conditioning on X_1 = x,

                    E[N_y|X_1 = x] = nPr{X_2 is a Gabriel neighbor of X_1, ||X_2 - X_1|| \geq r|X_1 = x}
                        \
                            \leq n(1 - r^2/4)^n-1
                            (because at least a 1/7 fraction
                            of the Gabriel circle through x and X_2 falls in the unit square)
                            \
                            \leq ne^9(n-1)log n/(4n)
                            \
                            \sim n^1-9/4
                            \
                            \to 0 .

Thus, it suffices to study N_b.

```

Thus, it suffices to study N b .


<!-- p:10 -->


As tan

θ

≤

θ

+

θ

3

Figure 6: Several points and their separators

for

0

≤

The total wedge area around

X

1

θ

≤

=

x

≤


1

, the area of each wedge is at most

r

2


9 log nθ

2

n

72 log nπ

3

2

nk

3

≤

1200 log

n

nk

is thus not more than

1200 log

n

1200

nk

2

≤

n

3

.

Given X 1 = x and the collection of red points, the n - 1 - N r other points are uniformly distributed on the unit square minus the N r circular sectors just inside the wedges, and minus circular sectors of radius r defined when no red point is present in the sector. Call the density f and its support set S . Clearly, 1 ≤ f ≤ 1 / (1 - πr 2 ) . Of the n - 1 - N r points, let M denote the total number of points falling in the wedges. Clearly, M is stochastically smaller than a binomial random variable with parameters m = n - 1 - N r and p = 1200 /n (1 - πr 2 ) . In particular, using l ! ≥ ( l/e ) l , and letting Pr denote the

10

3

(tan

θ

-

θ

)

.


<!-- p:11 -->


Figure 7: Sectors, red points, and blue wedges.

<!-- p:12 -->


conditional probability,

$$Pr \{ M \geq l \} & \leq \sum _ { j = l } ^ { m } \binom { m } { j } p ^ { j } ( 1 - p ) ^ { m - j } \\ & \leq \sum _ { j = l } ^ { \infty } \frac { ( m p ) ^ { j } } { j ! } \\ & = \frac { ( m p ) ^ { l } } { l ! } \sum _ { j = 0 } ^ { \infty } \frac { ( m p ) ^ { j } l ! } { ( l + j ) ! } \\ & \leq \frac { ( m p ) ^ { l } } { l ! } \sum _ { j = 0 } ^ { \infty } \left ( \frac { m p } { l } \right ) ^ { j } \\ & = \frac { ( m p ) ^ { l } } { l ! ( 1 - m p / l ) } \\ & \leq \frac { ( m p e / l ) ^ { l } } { ( 1 - m p / l ) } \\ & \leq \frac { ( n p e / l ) ^ { l } } { ( 1 - n p / l ) } \cdot \\ & = \frac { ( m p ) ^ { l } } { l ! ( 1 - m p / l ) } \\ & \leq \frac { ( m p e / l ) ^ { l } } { ( 1 - m p / l ) } \\ & \leq \frac { ( n p e / l ) ^ { l } } { ( 1 - n p / l ) } \cdot \\ & = \frac { ( 1 - n p / l ) } { l ! ( 1 - n p / l ) } \, .$$

We set l = ⌈ c log n/ log log n ⌉ for a constant c and note that np/l = o (1) . By the union bound, the probability that for one of the n data points, the number of blue color points in the wedge collection for that point is greater than or equal to l does not exceed

$$n \times \frac { ( n p e / l ) ^ { l } } { ( 1 - n p / l ) } \ . \\$$

As np = 1200 + o (1) , the above expression is for all n large enough not more than

$$2 n ( 3 6 0 0 / l ) ^ { l } \, .$$

This tends to zero when c &gt; 1 .

The probability that for one of the data points, N y &gt; 0 is not more than

$$n \times ( 1 + o ( 1 ) ) n ^ { 1 - 9 / 4 } \rightarrow 0 \, .$$

Thus, we have shown that for c &gt; 1 , the probability that the maximal degree exceeds k + l tends to zero. As k + l ∼ l , we are done.

### 2.3 Remarks

Higher dimensions. Just as Bern, Eppstein and Yao (1991) showed for the expected maximal degree in a Delaunay triangulation, the results for in probability convergence for Gabriel graphs extend easily to R d . In particular, for any d , there exist constants a &gt; 0 and b &lt; ∞ only depending upon d such that

$$\lim _ { n \to \infty } \Pr \left \{ \max { \text {imal degree } } \not \in \left ( \frac { a \log n } { \log \log n } , \frac { b \log n } { \log \log n } \right ) \right \} = 0 \ .$$


<!-- p:13 -->


Edge lengths. The results on N y in the proof above show that the expected number of Gabriel edges of length at least 3 √ log n/n is o (1) . Hence, the probability that the maximal edge length exceeds 3 √ log n/n tends to zero. In R d , the maximal edge length is easily shown to be O ((log n/n ) 1 /d ) in probability. In contrast, one can show that if E i is the maximal edge length among the Gabriel edges incident to X i , then (1 /n ) ∑ n i =1 E[ E i ] = O ( n - 1 /d ) , and that if F i is the minimal edge length among the Gabriel edges incident to X i , then (1 /n ) ∑ n i =1 E[ F i ] = Ω( n - 1 /d ) .

## 3 Yao Graphs

In this section we present our results on Yao graphs. For simplicity we consider θ -Yao graphs with θ = π/ 2 . The modifications required for other (smaller) values of θ are discussed at the end of this section. The lower bound in Section 3.1 is obtained using a construction and argument similar to the pearl used to prove Theorem 1. The upper bound in Section 3.2 uses different arguments based on maxima.

For the upper bound, we change the distribution model slightly by rotating it by π/ 4 . More precisely, let D 2 denote the unit square rotated by π/ 4 . The upper bound assumes that points are distributed uniformly and independently in D 2 . At the end of this section, we discuss why this slightly different assumption is necessary.

### 3.1 A lower bound

Our lower bound argument is similar to that used for Gabriel graphs, in that we define a configuration of points whose existence implies a vertex of degree k and show that, with high probability, this configuration exists in a random point set.

Theorem 3. For a random π/ 2 -Yao graph defined by n points drawn independently from the uniform distribution on [0 , 1] 2 ,

$$\lim _ { n \to \infty } \Pr \left \{ M a x i m a l \deg r e e < \frac { c \log n } { \log \log n } \right \} = 0 \ ,$$

for all c &lt; 1 / 8 .

Proof. Refer to Figure 8.a. Let r &gt; 0 be a real number and let k be a positive integer. Define k square regions P 1 , . . . , P k where P i = [( i - 1) r/k, ir/k ] × [ r - ir/k, r - ( i - 1) r/k ] . These regions are called steps .

Assume we are given m points in the plane, x 1 , . . . , x m and a center x . Then we call x a ( k, r ) - staircase for x 1 , . . . , x m if exactly k of the points x i fall into the square x + [ - r, r ] 2 and if each step x + P j covers exactly one of these x i 's. If we construct the π/ 2 -Yao graph for x, x 1 , . . . , x m and x is a ( k, r ) -staircase for x 1 , . . . , x m , then every point in each of the k steps is adjacent to x , so x is a vertex of degree at least k (Figure 8.b).

Let k = c log n/ log log n , let r = √ 2 /n , and let X 1 , . . . , X n be n points drawn uniformly and independently from [0 , 1] 2 . Then the area, p , of a step in a ( k, r ) -staircase is p = ( r/k ) 2 = 2 /nk 2 , so


<!-- p:14 -->


Figure 8: An (8 , r ) staircase.

$$\Pr \{ X _ { 1 } \, \text { is a } ( k , r ) \text {-staircase} \, | \, X _ { 1 } \in [ r , 1 - r ] ^ { 2 } \} & = \frac { ( n - 1 ) ! } { ( n - k - 1 ) ! } p ^ { k } ( 1 - 8 / n ) ^ { n - k - 1 } \\ & \geq ( 1 - k / n ) ^ { k } ( 1 - 8 / n ) ^ { n } 2 ^ { k - 2 k } \\ & \geq k ^ { - 2 k } \ , \\ \intertext { \text {for } n \text { sufficiently large. Thus, if } N \text { is the number of staircases among } X _ { 1 } , \dots , X _ { n } \text {, then } }$$

for n sufficiently large. Thus, if N is the number of staircases among X 1 , . . . , X n , then

$$E [ N ] \geq n ( 1 - 2 r ) ^ { 2 } k ^ { - 2 k } = \Omega ( n ^ { 1 - 2 c - \epsilon } ) \to \infty \ ,$$

provided that c &lt; 1 / 2 .

As before, we finish the proof using the second moment method. Let A denote the event that { X 1 , X 2 } ̸⊂ [ r, 1 - r ] 2 or that X 2 ∈ X 1 + [ - r, r ] 2 , and let A c denote the complement of A . Let Y i , i ∈ { 1 , 2 } , denote the indicator variable that X i is a staircase. Then, for sufficiently large n ,

$$X _ { 1 } , X _ { 2 } \} \, \mathcal { C } \, \left | r , 1 - r \right | ^ { 2 } \, \text { or that } \, X _ { 2 } \, \in \, X _ { 1 } \, + \, [ - r , r ] ^ { 2 } , \text { and let } \, A ^ { \, \prime } \, \Delta \, \text { denote the complement of } \, A . \, \text { Let } Y _ { i } , \\ \in \{ 1 , 2 \} , \, \text { denote the indicator variable that } \, X _ { i } \, \text { is a staircase. Then, for sufficiently large } n , \\ \frac { E [ Y _ { 1 } Y _ { 2 } ] } { E [ Y _ { 1 } ] E [ Y _ { 2 } ] } \leq \frac { E [ Y _ { 1 } Y _ { 2 } ] } { k - 4 k } \leq \frac { E [ Y _ { 1 } Y _ { 2 } ] } { k - 4 k } \\ = k ^ { 4 k } ( \Pr \{ A \} E [ Y _ { 1 } Y _ { 2 } | A ] + \Pr \{ A ^ { \, \prime } \} E [ Y _ { 1 } Y _ { 2 } | A ^ { \, \prime } ] ) \\ \leq k ^ { 4 k } ( ( 4 r + 4 r ^ { 2 } ) + \Pr \{ A ^ { \, \prime } \} E [ Y _ { 1 } Y _ { 2 } | A ^ { \, \prime } ] ) \\ \leq k ^ { 4 k } \left ( ( 4 r + 4 r ^ { 2 } ) + \frac { ( n - 2 ) ! } { ( n - 2 \, k ) ! } \left ( \frac { 1 } { n ^ { k } } \right ) ^ { 2 k } \right ) ^ { ( 1 - 1 6 / n ) ^ { n - 2 - 2 k } } \right ) \\ \leq k ^ { 4 k } \left ( ( 4 r + 4 r ^ { 2 } ) + n ^ { 2 k } \left ( \frac { 1 } { n ^ { k } } \right ) ^ { 2 k } ( 1 - 1 6 / n ) ^ { n - 2 - 2 k } \right ) \\ \leq k ^ { 4 k } \left ( 4 \sqrt { 2 / n } + 8 / n \right ) + 1 \\ = 1 + O ( n ^ { 4 c - 1 / 2 } ) \ , \\ \intertext { o lim } \Delta \, \intertext { o lim } E [ Y _ { 1 } Y _ { 2 } ] = 1 \, f o r \, a n y \, c < 1 / 8 .$$

so lim n →∞ E[ Y 1 Y 2 ] E[ Y 1 ]E[ Y 2 ] = 1 for any c &lt; 1 / 8 .


<!-- p:15 -->


### 3.2 An upper bound

Next we prove an upper bound on the maximum degree in a ( π/ 2) -Yao graph. The upper bound is based on the observation that the neighbours of a node in a Yao graph are so-called minima. Let x 1 , . . . , x n be a set of points. We say that a point x i dominates x j if the x - and y -coordinate of x i are larger than the x - and y -coordinate of x j , respectively. A point x is maximal with respect to x 1 , . . . , x n if x is not dominated by any x i . A point x is minimal if x does not dominate any point x i .

Before we can present the upper bound, we require a few preliminary results about maxima and minima. First, though, we recall a classic result obtained using Chernoff's bounding method [5]:

Lemma 1. Let Y 1 , . . . , Y m be a sequence of independent { 0 , 1 } -valued random variables, let Y = ∑ m i =1 Y i , and let μ = E[ Y ] . Then, for any, δ &gt; 0 ,

$$\Pr \{ Y > ( 1 + \delta ) \mu \} \leq \left ( \frac { e ^ { \delta } } { ( 1 + \delta ) ^ { ( 1 + \delta ) } } \right ) ^ { \mu } \ .$$

The following result is already quite well-known. We include a proof sketch only for the sake of completeness.

Lemma 2. Let X 1 , . . . , X m be a sequence of points drawn independently and uniformly from a rectangle [ a, b ] × [ c, d ] having area greater than 0 and let M be the number of maximal (respectively, minimal) points among X 1 , . . . , X m . Then, for any δ &gt; 0 ,

$$\log m \leq E [ M ] \leq \log m + 1$$

$$\Pr \{ M > ( 1 + \delta ) E [ M ] \} \leq \left ( \frac { e ^ { \delta } } { ( 1 + \delta ) ^ { 1 + \delta } } \right ) ^ { \log m } \ .$$

and

Proof. Sort the elements of X 1 , . . . , X m by decreasing x -coordinate, so that X i is maximal if and only if its y -coordinate is the maximum among the y -coordinates of X 1 , . . . , X i . Let Y i = 1 if X i is maximal and Y i = 0 otherwise. Obviously E[ Y i ] = 1 /i , so

$$E [ M ] = E \left [ \sum _ { i = 1 } ^ { m } Y _ { i } \right ] = \sum _ { 1 = 1 } ^ { m } 1 / i \ . \\$$

The inequality log m ≤ E[ M ] ≤ log m +1 is then obtained by bounding the above Harmonic sum using the integral ∫ n 1 (1 /x ) dx (see, e.g., Cormen et al [6, Appendix A.2]).

To prove the second part of the lemma, we use the fact that the random variables Y 1 , . . . , Y m are independent [8, 10]. The result then follows immediately from Lemma 1.

Unfortunately, the points we consider will not always be drawn from a rectangle. A t -shape is a closed maximal subset of R 2 that is bounded by the x - and y -axes and a y -monotone polygonal path consisting of at most t edges. See Figure 9.a.


<!-- p:16 -->


as required.

We now have all the tools required to prove our upper bound

Theorem 4. For a random ( π/ 2) -Yao graph defined on n points drawn independently from the uniform distribution on D 2 ,

for all c &gt; 4 .

$$\lim _ { n \to \infty } \Pr \left \{ \max { \text {imal degree} } > \frac { c \log n } { \log \log n } \right \} = 0$$

Figure 9: (a) a t -shape S , (b) covering S to obtain a shape S ′ and uniformly distributing points in S ′ , and (c) reflecting the points in S ′ to obtain points uniformly distributed in S .

Lemma 3. Let X 1 , . . . , X m be a sequence of points drawn independently and uniformly from a t -shape S having area greater than 0 and let M be the number of minimal points among X 1 , . . . , X m . Then, for any δ &gt; 0 ,

and

$$E [ M ] \leq 2 t ( \log m + 1 )$$

$$\Pr \{ M > ( 1 + \delta ) 2 t ( \log m + 1 ) \} \leq 2 t \left ( \frac { e ^ { \delta } } { ( 1 + \delta ) ^ { 1 + \delta } } \right ) ^ { \log m } \ .$$

Proof. Cover S with at most t rectangles R 1 , . . . , R l whose total area is twice the area of S , as shown in Figure 9.b. Let S ′ = ⋃ l i =1 R i be the resulting subset of R 2 . Generate points Z = { Z 1 , . . . , Z m } uniformly and independently in S ′ . For each point Z i in R j , if Z i ∈ S then set X i = Z i . Otherwise, set X i to be the reflection of Z i through the center of R j . Observe that X 1 , . . . , X m are uniformly distributed in S . Furthermore, if X i ∈ R j is minimal with respect to X 1 , . . . , X m , then Z i is either maximal or minimal with respect to Z ∩ R j .

Therefore, if M j denotes the number of minimal elements of X contained in R j , then, by the first part of Lemma 2, E[ M j ] ≤ 2(log m +1) and

$$E [ M ] = E \left [ \sum _ { j = 1 } ^ { t } M _ { j } \right ] \leq 2 t ( \log m + 1 ) \ . \\ \intertext { i t o f L e m m a 2 t i m e s , a n d u s i n g t h e u n i o n b o u n d , }$$

By applying the second part of Lemma 2 t times, and using the union bound, we also obtain

$$\Pr \{ M > ( 1 + \delta ) 2 t ( \log m + 1 ) \} \leq 2 t \left ( \frac { e ^ { \delta } } { ( 1 + \delta ) ^ { 1 + \delta } } \right ) ^ { \log m }$$


<!-- p:17 -->


Proof. Let X 1 , . . . , X n be points uniformly and independently distributed in D 2 and let G the the ( π/ 2 )- Yao graph of X 1 , . . . , X n . Let l = √ d log n/n . We will first consider the edges of G whose length is at most l . Consider the square S = X 1 +[0 , l ] 2 . Let N denote the number of points of X 2 , . . . , X n contained in S . Then E[ N ] ≤ nl 2 = d log n and, by Lemma 1,

$$\Pr \{ N > 2 d \log n \} \leq ( e / 4 ) ^ { d \log n } = n ^ { d ( 1 - \log 4 ) } \ .$$

Let N ′ denote the number of points in S that are neighbours of X 1 in the Yao graph. Each such point is minimal with respect to the N points of X 2 , . . . , X n contained in S . Furthermore, S ∩ D 2 is a t -shape, for t ≤ 2 . By the first part of Lemma 3, conditioned on N ≤ 2 d log n , the expected number of minimal points, and hence the number of neighbours of X 1 in S is small;

$$E [ N ^ { \prime } | N \leq 2 d \log n ] \leq 4 ( \log ( 2 d \log n ) + 1 ) = 4 \log \log n + \Theta ( 1 ) \ . \\$$

Define v = log(2 d log n ) and let k = ( c log n ) / (log log n ) . By the second part of Lemma 3, with t = 2 ,

$$\minimal points, and hence the number of neighbours of X _ { 1 } in S is small; \\ & \quad E [ N ^ { \prime } | N \leq 2 d \log n ] \leq 4 ( \log ( 2 d \log n ) + 1 ) = 4 \log n + \Theta ( 1 ) \ . \\ \text {Define } v = \log ( 2 d \log n ) \text { and let } k = ( c \log n ) / ( \log \log n ) . \text { By the second part of Lemma 3, with } t = 2 , \\ & \quad \Pr \left \{ N ^ { \prime } > k | N \leq 2 d \log n \right \} = \Pr \left \{ N ^ { \prime } > \frac { c \log n } { 4 ( v + 1 ) ( \log \log n ) } \cdot ( 4 ( v + 1 ) ) | N \leq 2 d \log n \right \} \\$$

for any ǫ &gt; 0 . Unconditioning, we obtain

$$\Pr \{ N ^ { \prime } > k \} = O ( n ^ { - c / 4 + \epsilon } + n ^ { d ( 1 - \log 4 ) } ) \ .$$

Let G ′ be the subgraph of G consisting only of edges of length at most l and let D ′ denote the maximum degree of a vertex in G ′ . Repeating the above argument 4 n times and using the union bound gives

$$\Pr \{ D ^ { \prime } > k \} = O ( n ^ { 1 - c / 4 + \epsilon } + n ^ { 1 + d ( 1 - \log 4 ) } )$$


<!-- p:18 -->


Figure 10: An edge of length l defines an empty subset of D 2 whose area is at least ( l/ 2) 2 .

Finally, all that remains is to argue that G has no edges of length greater than l . An edge of length at least l defines an empty region of area at least πl 2 / 4 . For l &lt; 1 / 2 , a portion of this empty region whose area is at least ( l/ 2) 2 is contained in D 2 (see Figure 10). Therefore, the probability of there being any edge of length greater than l = √ d log n/n is at most

$$4 n ( 1 - \ell ^ { 2 } / 4 ) ^ { n - 2 } & = 4 n \left ( 1 - \frac { d \log n } { 4 n } \right ) ^ { n - 2 } \\ & \leq 4 n e ^ { - ( n - 1 ) d \log n / 4 n } \\ & \leq 4 n ^ { 1 - ( n - 1 ) d / 4 n } \\ & = 4 n ^ { 1 - ( 1 - 1 / n ) d / 4 }$$

At last, let D be the maximum degree of any vertex in G . Putting everything together, we obtain

$$\Pr \{ D > k \} = O ( n ^ { 1 - c / 4 + \epsilon } + n ^ { 1 + d ( 1 - \log 4 ) } + n ^ { 1 - ( 1 - 1 / n ) d / 4 } ) \to 0$$

for any c &gt; 4 and d &gt; max { 1 / (log 4 - 1) , 4 } .

### 3.3 Remarks

Why D 2 ? The proof of Theorem 4 actually shows that the probability that G has a vertex of degree more than c log n/ log log n is n - Ω( c ) . The last step in the proof requires that any edge of length l defines portion of the support set of area Ω( l 2 ) that is empty of points. This is true when the support set is D 2 but not true when the support set is the unit square [0 , 1] 2 . Indeed, the proof breaks down for points drawn from the unit square, since with probability 1 /n , some element, say X 1 , simultaneously has the minimum x - and y -coordinate. In this case, the expected degree of X 1 is equal to the expected number of minimal elements among X 2 , . . . , X n , which is, by Lemma 2, Θ(log n ) .

In a situation where points are uniformly distributed in the unit square, the upper bound in Theorem 4 holds if one considers only the points whose distance from the boundary of the square is at least √ d log n/n .


<!-- p:19 -->


Smaller values of θ . For any constant value of θ ≤ π/ 2 , the upper and lower bounds of Theorem 3 and Theorem 4 still hold. The arguments are almost identical with the exception that the definition of a staircase and of minima and maxima are modified to take the value of θ into account. Although the value of θ appears in the intermediate calculations, for any constant θ , the constants c = 1 / 8 and c = 4 in Theorem 3 and Theorem 4 are unchanged. However, as noted above, to prove a version of Theorem 4 the support set must be rotated so that the difference in angle between any side of the support set and iθ , for 0 ≤ i ≤ 2 π/θ is lower-bounded by a constant.

Higher dimensions. Yao graphs are also defined for point sets in R d . The lower bound of Theorem 3 can be extended to show that Yao graphs of n points uniformly and independently distributed in [0 , 1] d have maximum degree Ω(log n/ log log n ) . Unfortunately, the proof of the upper bound in Theorem 4 does not continue to hold in R d .
