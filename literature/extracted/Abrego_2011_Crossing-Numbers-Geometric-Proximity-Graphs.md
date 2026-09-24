---
id: "Abrego_2011_Crossing-Numbers-Geometric-Proximity-Graphs"
source_pdf: "../pdf/Abrego_2011_Crossing-Numbers-Geometric-Proximity-Graphs.pdf"
source_filename: "Abrego_2011_Crossing-Numbers-Geometric-Proximity-Graphs.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "excellent"
extraction_score: 100.0
visual_assets: "disabled"
references_file: "../references/Abrego_2011_Crossing-Numbers-Geometric-Proximity-Graphs.references.md"
---

<!-- p:1 -->

Contents lists available at ScienceDirect

## Computational Geometry: Theory and Applications

www.elsevier.com/locate/comgeo

## On crossing numbers of geometric proximity graphs

Bernardo M. Ábrego a , Ruy Fabila-Monroy b , Silvia Fernández-Merchant a , David Flores-Peñaloza c , Ferran Hurtado d , 1 , Vera Sacristán d , 1 , Maria Saumell d , ∗ , 1

a Department of Mathematics, California State University, Northridge, CA, United States

b Departamento de Matemáticas, CINVESTAV, Mexico, DF, Mexico

c Departamento de Matemáticas, Facultad de Ciencias, Universidad Nacional Autónoma de México, Mexico

d Departament de Matemàtica Aplicada II, Universitat Politècnica de Catalunya, Barcelona, Spain

##### a r t i c l e i n f o

##### a b s t r a c t

Article history:

Received 15 June 2010 Accepted 30 November 2010 Available online 3 December 2010 Communicated by T. Tokuyama

Keywords:

Proximity graphs Geometric graphs Crossing number

### 1. Introduction

A geometric graph on a point set P is a pair G = ( P , E ) in which the vertex set P is assumed to be in general position, i.e., no three points are collinear, and the set E of edges consists of straight-line segments with endpoints in P . Notice that the focus is more on the drawing rather than on the underlying graph, as carefully pointed out by Brass, Moser, and Pach in their survey book [6, p. 373].

A proximity graph is a graph G = ( V , E ) in which the nodes represent geometric objects in a given set, typically points, and two nodes are adjacent when the corresponding objects are considered to be neighbors according to some specific proximity criterion. A geometric proximity graph is a geometric graph in which the adjacency is decided by some neighborhood rule; it is sometimes called a proximity drawing [19]. Examples of these graphs are the k-nearest neighbor graph , k - NNG ( P ) , in which every point is joined with a directed segment to its k closest neighbors, and the k -Delaunay graph, k - DG ( P ) , in which pi and p j are connected with a segment if there is some circle through pi and p j that contains at most k points from P in its interior. Other similar definitions are given later in this paper.

Proximity graphs have been widely used in applications in which extracting shape or structure from a point set is a required tool or even the main goal, as is the case of computer vision, pattern recognition, visual perception, geographic information systems, instance-based learning, and data mining [14,20,28]. In the area of Graph Drawing [5,12,15] the main

*

Corresponding author. E-mail addresses: bernardo.abrego@csun.edu (B.M. Ábrego), ruyfabila@math.cinvestav.edu.mx (R. Fabila-Monroy), silvia.fernandez@csun.edu

(S. Fernández-Merchant), dflorespenaloza@gmail.com (D. Flores-Peñaloza), ferran.hurtado@upc.edu (F. Hurtado), vera.sacristan@upc.edu (V. Sacristán), maria.saumell@upc.edu (M. Saumell).

1 Partially supported by projects MTM2009-07242 and Gen. Cat. DGR 2009SGR1040.

Let P be a set of n points in the plane. A geometric proximity graph on P is a graph where two points are connected by a straight-line segment if they satisfy some prescribed proximity rule. We consider four classes of higher order proximity graphs, namely, the k - nearest neighbor graph, the k -relative neighborhood graph, the k -Gabriel graph and the k -Delaunay graph. For k = 0 ( k = 1 in the case of the k -nearest neighbor graph) these graphs are plane, but for higher values of k in general they contain crossings. In this paper, we provide lower and upper bounds on their minimum and maximum number of crossings. We give general bounds and we also study particular cases that are especially interesting from the viewpoint of applications. These cases include the 1-Delaunay graph and the k -nearest neighbor graph for small values of k .

© 2010 Elsevier B.V. All rights reserved.

<!-- p:2 -->


goal is to realize-or to draw -a given combinatorial graph as a geometric proximity graph, which leads to problems on characterizing the graphs that admit such a representation and designing efficient algorithms to construct the drawing whenever possible (see the survey [19] in this respect).

Graphs are usually drawn in the plane with points as nodes and Jordan arcs as edges. When two edges share an interior point, we say that there is a crossing . Both as a natural aesthetic measure for graph drawing and as a fundamental issue in the mathematical context, the number of crossings is a parameter that has been extensively studied. Given a graph G , the crossing number of G , denoted by cr ( G ), is the minimum number of edge crossings in any drawing of G ; if this number is 0, we say that the graph is planar . The rectilinear crossing number of G , denoted by cr ( G ), is the smallest number of crossings in any drawing of G in which the edges are represented by straight-line segments.

Computing the crossing number of a graph is an NP-hard problem [9], and both the generic and rectilinear crossing numbers of very fundamental graphs, such as the complete graph Kn and the complete bipartite graph Km , n are still unknown [32,11]. These problems have attracted a great amount of attention and recently a continuous chain of improvements has led progressively to narrow the gap between the lower and upper bounds [16,3,2]. There are also several results on the numbers of crossings that are sensitive to the size of the graph-particularly the crossing lemma [4,18,6]-, or to the exclusion of some configurations [6,21,23,30,8].

In this paper, we study the crossing numbers of several higher order geometric proximity graphs related to Delaunay graphs. If P is a set of points in the plane, each of the proximity graphs we consider is a geometric graph on P that has some number of crossings that will be denoted by ⊠ ( ) . We investigate how this number varies when all possible point sets P in general position, with | P | = n , are considered. The generic conclusion that may be derived from our research is that this family of graphs has a relatively small number of crossings.

The fact that this specific issue has not been investigated previously is somehow surprising. As an explanation, one may first consider that 0-order proximity graphs, which have attracted most of the research and are better understood, are planar. On the other hand, regarding the applications in shape analysis, the data are what they are, and the user would not have the possibility of moving the points around to decrease the number of crossings. It is worth mentioning here that, while higher order proximity graphs were introduced and studied about twenty years ago [26,27], there has been a renewal of interest on them, especially for low orders, as they offer a flexibility which is desirable in several applications. For example, the Delaunay triangulation ( DT ) is unique, while one can extract a large number of different triangulations from the 1-Delaunay graph, all of them 'close' to DT , which may be preferable under some criterion. (See for example the papers [17,1] and the numerous references there.)

From the viewpoint of proximity drawings, it is desirable to have a small number of crossings, and hence we study its minimum value. On the other hand, we also consider the shape analysis situation in which choosing the points is not possible, which leads to study how large the number of crossings can be, i.e., its maximum value.

For example, consider the k -nearest neighbor graph of point sets P with | P | = n . We introduce and study the rectilinear crossing number and the worst crossing number defined respectively as

$$\overline { c r } ( k { - } N G ( n ) ) & = \min _ { | P | = n } \mathbb { Z } ( k { - } N G ( P ) ) , \\ \overline { w c r } ( k { - } N G ( n ) ) & = \max _ { | P | = n } \mathbb { Z } ( k { - } N G ( P ) ) .$$

$$\overline { w c r } ( k { \text {-NNG} } ( n ) ) = \max _ { | P | = n } \mathbb { Z } ( k { \text {-NNG} } ( P ) ) . \\$$

We define analogous parameters for the k -relative neighborhood graph, k - RNG ( P ) , in which pi , p j are adjacent if the open intersection of the circles centered at pi and p j with radius | pi p j | contains at most k points from P ; the k -Gabriel graph, k - GG ( P ) , in which pi and p j are adjacent if the closed circle with diameter pi p j contains at most k points from P different from pi , p j ; and the k -Delaunay graph, k - DG ( P ) . It is well known that

$$( k + 1 ) - N N G ( P ) \subseteq & k - R N G ( P ) \subseteq k - G G ( P ) \subseteq k - D G ( P ) . \\ & \\ ( k + 1 ) - N N G ( P ) \subseteq & k - R N G ( P ) \subseteq k - G G ( P ) \subseteq k - D G ( P ) .$$

Notice that, when the rectilinear crossing number of a combinatorial graph is considered, we draw the same graph on top of different points sets, while here we study a specific kind of proximity graph on top of different point sets, but the underlying combinatorial graphs may be different for many of these sets. Another somehow subtle issue that deserves a specific comment is the fact that the combinatorial graph obtained from a proximity drawing may have a smaller crossing number than the rectilinear crossing number of its proximity drawing. This is clearer with an example: We prove in this paper that cr ( 1DG ( n )) = n - 4; this means that 1DG ( P ) contains at least n - 4 crossings for any set P of n points, and that for some point set Q this number is achieved. The graph in Fig. 1(left) is the 1-Delaunay graph of its vertex set (the six shown points) and has 2 crossings; however, the combinatorial graph can be drawn on top of a different set and have only one crossing (Fig. 1, right). Obviously the latter is not the 1-Delaunay graph of its vertex set.

A substantial part of our research focuses on the 1-Delaunay graph and on the graphs k - NNG ( P ) with small k , widely used in classification scenarios, as these are the most interesting situations from the viewpoint of applications [1,7,10,13,17,31]. Our results are summarized in Tables 1 and 2, and presented in full detail in Sections 2 and 3. In Section 4, we look at the number of crossings for large values of k . Our bounds are gathered in Table 3. Throughout the paper, we assume that point sets P are in general position in an extended sense: no three points are collinear, no four points are concyclic and, for each p ∈ P , the set of its k -nearest points in P is well-defined, i.e., it has cardinality k , for any k ⩾ 1. We


<!-- p:3 -->


Fig. 1. The graph on the left is a 1-Delaunay graph; black edges belong to 0-DG . The graph on the right is isomorphic.

Table 1

1-Delaunay graphs.

|     | General case                    | Convex case                         |
|-----|---------------------------------|-------------------------------------|
| cr  | n - 4                           | 6 n - 3 ⌊ n 2 ⌋- 19                 |
| wcr | n 2 Θ( n ) ⩽ wcr ⩽ 4 n 2 Θ( n ) | n 2 2 Θ( n ) ⩽ wcr ⩽ 7 n 2 8 Θ( n ) |

+


Table 2 cr ( k - NNG ( n )) for the first values of k .

|   k | cr ( k - NNG ( n ))                       |
|-----|-------------------------------------------|
|   1 | 0                                         |
|   2 | 0                                         |
|   3 | 0                                         |
|   4 | 0, for n ⩾ 14                             |
|   5 | 0, for n ⩾ 44                             |
|   6 | ⩽ 58 , for n ⩾ 39                         |
|   7 | n / 2 + Θ( 1 )                            |
|   8 | n + Θ( 1 )                                |
|   9 | 13 n / 6 + 50 / 3 ⩽ cr ⩽ 9 n / 4 + Θ( 1 ) |
|  10 | 10 n / 3 50 / 3 ⩽ cr ⩽ 11 n / 3 Θ( 1 )    |

+


Table 3 Dominant terms of the general bounds. Some of the bounds only hold for 'intermediate' values of k . We refer to the precise statements in Section 4.

|       | k - NNG ( n )   | k - RNG ( n )                    | k - GG ( n )    | k - DG ( n )     |
|-------|-----------------|----------------------------------|-----------------|------------------|
| cr ⩾  | 128 31827 k 3 n | 128 31827 k 3 n                  | 128 31827 k 3 n | 1024 31827 k 3 n |
| cr ⩽  | 1 9 π 2 k 3 n   | π 9 ( 2 π/ 3 - √ 3 / 2 ) 3 k 3 n | 64 9 π 2 k 3 n  | 64 9 π 2 k 3 n   |
| wcr ⩾ | 1 3 k 3 n       | 1 3 k 3 n                        | 1 4 k 2 n 2     | 1 2 k 2 n 2      |
| wcr ⩽ | k 3 n           | 9 k 3 n                          | 3 k 2 n 2       | 3 k 2 n 2        |

denote by H the set of vertices of the convex hull of P , and we denote by I the set of points in the interior of this convex hull.

Throughout the paper, we denote by V ( G ) (respectively, E ( G ) ) the set of vertices (respectively, edges) of a given graph G , and by | V ( G ) | (respectively, | E ( G ) | ) the cardinality of this set. If v is a vertex in V ( G ), we denote by dG ( v ) the degree of v in G .

### 2. 1-Delaunay graphs

In this section, we carry out a detailed analysis of the number of crossings in a 1-Delaunay graph. We study the general case and also the particular case where all points are in convex position.

First we introduce some notation. We partition the edges of the 1-Delaunay graph into two groups: we say that an edge is blue if it also appears in 0DG ( P ) and it is red otherwise. We set | Eb | = | E ( 0DG ( P )) | and | Er | = | E ( 1DG ( P )) | - | E ( 0DG ( P )) | . Note that a red edge pi p j corresponds to an element in E ( 0DG ( P \ { pl } )) for some pl ∈ P . We say that pi p j is generated by pl . Observe that the fact that pi p j is generated by pl is equivalent to the existence of a disk through pi and p j containing pl and no other point in P , which implies that pi p l and p j pl belong to E ( 0DG ( P )) . Thus pi p j is generated

by at most two points. (See [1].)

In the figures of this section, the blue edges are represented in black and the red edges in gray.


<!-- p:4 -->


#### 2.1. Rectilinear crossing number

We establish the exact value of the rectilinear crossing number of the 1-Delaunay graph for both the general case and the convex case. More precisely, we show that the rectilinear crossing number is n - 4 in the general case and 6 n - 3 ⌊ n 2 ⌋ - 19 in the convex case.

For a point p ∈ P , let dG ( p ) denote the degree of p in G , where G = 0DG ( P ) , and let d ∗ ( p ) be the value 2 plus the number of points of I that are in the convex hull of P \ { p } .

In [1] it is shown that | Er | ⩾ n - 5. Since 0DG ( P ) is maximal planar, this immediately yields that every 1-Delaunay graph contains at least n - 5 crossings. We show an improved bound, | Er | ⩾ n - 4 (see Theorem 2.1.5), and provide a tight example. The first part of our proof follows the lines of previous techniques used in [1].

Our proof requires several remarks, already stated in [1]:

Lemma 2.1.1. If a red edge is generated by exactly two points, then it is the diagonal ( which is not a Delaunay edge ) of a quadrilateral defined by a pair of adjacent triangles t 1 and t 2 of 0 - DG ( P ) in convex position. We say that t 1 ∼ t 2 . The relation ∼ is a ( in general non-perfect ) matching between the triangles of 0 - DG ( P ) .

Lemma 2.1.2. The number of red edges generated by an element p ∈ P is :

- dG ( p ) - d ∗ ( p ), if p ∈ H ;
- dG ( p ) - 3 , if p ∈ I .

Lemma 2.1.3. If pl ∈ I is in the convex hull of both P \ { pi } and P \ { p j } , for some pair of points pi , p j ∈ H , then pi and p j are consecutive vertices in the convex hull of P. Furthermore, the triangle △ pi p j pl is empty, and the line through pi and pl separates △ pi p j pl from the rest of P , as does the line through p j and pl .

Lemma 2.1.4. Each element of I can contribute to d ∗ ( pi ) and d ∗ ( p j ) for at most two points pi , p j ∈ H , provided that n ⩾ 5 .

By Lemma 2.1.4, we may partition I into I 0 ∪ I 1 ∪ I 2, where I j is the set of elements of I that contribute to d ∗ for exactly j points.

Notice that, if pl ∈ I 2 contributes to d ∗ for pi and p j , then, by Lemma 2.1.3, the points pi , p j , and pl together with any other point of P are not in convex position. Hence △ pi p j pl is a triangle of 0DG ( P ) that does not participate in the matching given by Lemma 2.1.1. Such a triangle is called special triangle.

We wish to bound the number of red edges in 1DG ( P ) . By Lemma 2.1.2,

$$| E _ { r } | & = \sum _ { p \in \mathcal { H } } ( d _ { G } ( p ) - d ^ { * } ( p ) ) + \sum _ { p \in \mathcal { I } } ( d _ { G } ( p ) - 3 ) - \xi = 4 n - 6 - \left ( | \mathcal { I } | + \sum _ { p \in \mathcal { H } } d ^ { * } ( p ) \right ) - \xi , \\ \intertext { w h o r } \intertext { s u n t o r } \intertext { w h a r e } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { w h a r e } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { w h a r e } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r } \intertext { d i s e c h a n t a r r o w } \intertext { s u n t o r }$$

where is ξ the number of times a red edge is overcounted in the summation (which happens when two points induce the same edge). Using that ∑ p ∈ H d ∗ ( p ) = 2 | H | + | I 1 | + 2 | I 2 | , we obtain

Substituting | I 0 | ⩽ n -| H | , | I 2 | ⩾ 0, and ξ ⩾ 0, we infer

$$| E _ { r } | & = 2 n - 6 + | \mathcal { I } _ { 0 } | - | \mathcal { I } _ { 2 } | - \xi . \\ \intertext { | E _ { r } | = 2 n - 6 + | \mathcal { I } _ { 0 } | - | \mathcal { I } _ { 2 } | - \xi . } \intertext { (2 ) } \intertext { \xi - i t i o n s i t i o n } \tau ^ { ( \mathcal { I } _ { 1 } - \mathcal { I } _ { 2 } ) } & < \tau ^ { ( 2 ) } | \tau | \geq 0 , \, \tau _ { 0 } + \tau _ { 1 } \gtrdot \theta _ { 0 } \, \dots \, \tau _ { n } \intertext { (2 ) }$$

$$| E _ { r } | & \leqslant 3 n - | \mathcal { H } | - 6 . \\ \intertext { l $ | E _ { r } | \leqslant 3 n - | \mathcal { H } | - 6 $ } \text {This bound in the standard form of the theory of automorphism, but only } \intertext { ( 3 ) } \intertext { This bound in the standard form of the theory of automorphism, but only }$$

This bound is stated here for the sake of convenience but will not be used until we study the worst crossing number of the 1-Delaunay graph (see Lemma 2.2.5). Next we derive the expression for | Er | that is needed in the proof of Theorem 2.1.5.

Since the set of red edges generated by the removal of two points induces a matching in the triangles of 0DG ( P ) , we may introduce a new equation:

$$\xi = \frac { \triangle - | \mathcal { I } _ { 2 } | - m } { 2 } ,$$

where △ is the number of triangles in 0DG ( P ) (thus △=| H | + 2 | I | - 2), and m is the number of non-special triangles in 0DG ( P ) not matched by a red edge generated by two points.

Substituting (4) in (2), we conclude

$$| E _ { r } | & = n - 5 + | \mathcal { I } _ { 0 } | + \frac { 1 } { 2 } \left ( | \mathcal { H } | - | \mathcal { I } _ { 2 } | + m \right ) . \\ \text {Since } | \mathcal { I } _ { 0 } | & \geqslant 0 , \, | \mathcal { H } | - | \mathcal { I } _ { 2 } | \geqslant 0 , \, \text {and } m \geqslant 0 , \, \text {we have that}$$

Since | I 0 | ⩾ 0, | H | - | I 2 | ⩾ 0, and m ⩾ 0, we have that | Er | ⩾ n - 5, and | Er | = n - 5 if and only if

$$| \mathcal { I } _ { 0 } | = 0 , \quad | \mathcal { H } | = | \mathcal { I } _ { 2 } | , \quad \text {and} \quad m = 0 .$$


<!-- p:5 -->


Fig. 2. Part of the Delaunay triangulations of the point sets. Interior points are in gray. In the left figure, every edge of the convex hull of I is an edge of 0DG ( P ) . In the right figure, pi p l is a diagonal such that G 1 ( pi p l ) contains no diagonal of 0DG ( P ) .

We make some observations about the structure of P in the case where (5) is satisfied. Note that any point that contributes to d ∗ for some other point of H is in the second convex layer of P . Therefore, if we assume that | I 0 | = 0, then P has exactly two convex layers, and the second one is given by the set I = I 2 ∪ I 1. We say that each point pl ∈ I 2 is associated to two points of H , namely, those points for which pl contributes to d ∗ . Similarly, each point pl ∈ I 1 is associated to the point pi ∈ H for which pl contributes to d ∗ ( pi ) . With these last observations we are ready to prove the following lower bound:

Theorem 2.1.5. For every point set P , ⊠ ( 1 - DG ( P )) ⩾ n - 4 .

Proof. We prove that the graph 1DG ( P ) contains at least n - 4 red edges.

First we assume that every edge of the convex hull of I is an edge of 0DG ( P ) . In this case, every triangle having exactly one point of H as a vertex is entirely contained between the first and second convex layers of P ; see Fig. 2(left). No two of these triangles are matched, because the four vertices of two such adjacent triangles are not in convex position. As m = 0 and the special triangles cannot be matched, we infer that every triangle having exactly one point of H as a vertex is matched with one triangle contained in the second convex layer of P . However, there are | I | triangles of the first type and | I | - 2 triangles of the second type. Thus | I 0 | = 0, | H | = | I 2 | , and m = 0 cannot simultaneously hold in this case.

Suppose, by means of a contradiction, that | Er | = n - 5 and thus (5) holds. We distinguish two cases.

Now let us suppose that there exists an edge e of the convex hull of I that is not an edge of 0DG ( P ) . Then there is an edge pi p l in 0DG ( P ) crossing e such that pi is a point of H and pl is not associated with pi . We call such an edge pi p l a diagonal . For each diagonal pi p l , if pl ∈ H , let pol ( pi p l ) be the edge pi p l ; otherwise, let pol ( pi p l ) be the polygonal chain pi p l p j , where p j is a point of H associated to pl . In both cases pol ( pi p l ) is a polygonal chain joining two vertices of H . If we take the two sub-polygonal chains of the convex hull of P joining the endpoints of pol ( pi p l ) together with pol ( pi p l ) , we define two closed polygonal chains that are the boundary of two bounded regions C 1 ( pi p l ) and C 2 ( pi p l ) . The regions C 1 ( pi p l ) and C 2 ( pi p l ) define two non-empty subsets P 1 ( pi p l ) and P 2 ( pi p l ) , the points of P that lie in the interior or on the boundary of C 1 ( pi p l ) and C 2 ( pi p l ) , respectively. Without loss of generality, assume that P 1 ( pi p l ) is the smallest of the two sets. Let G 1 ( pi p l ) and G 2 ( pi p l ) be the subgraphs of 0DG ( P ) induced by P 1 ( pi p l ) and P 2 ( pi p l ) . Let pi p l be a diagonal in 0DG ( P ) such that G 1 ( pi p l ) contains no diagonal of 0DG ( P ) . Observe that pl is a point of I . Among all points of H associated to pl , let p j be the one that yields the smallest possible value for | P 1 ( pi p l ) | . Now let I ′ := I ∩ P 1 ( pi p l ) and H ′ := H ∩ P 1 ( pi p l ) . The intersection of the convex hulls of I and I ′ is a convex polygonal chain Q 2 that has I ′ as its vertex set and pl as an endpoint. Since the only diagonal of 0DG ( P ) in G 1 ( pi p l ) is pi p l , Q 2 is a subgraph of G 1 ( pi p l ) (see Fig. 2, right). Let pm denote the endpoint of Q 2 different from pl . The edge pi p l is a side of some triangle of G 1 ( pi p l ) ; since there are no diagonals of 0DG ( P ) in G 1 ( pi p l ) except for pi p l , the third vertex of this triangle is pm . Thus G 1 ( pi p l ) contains a triangulation of I ′ as subgraph. Let T H be the set of triangles of G 1 ( pi p l ) consisting of an edge of Q 2 and a point in H ′ , and T I be the set of triangles of G 1 ( pi p l ) with all their vertices in I ′ . It is not difficult to see that any triangle in T H that participates in the matching is matched with a triangle in T I . Since | T H | = | I ′ | - 1 and | T I | = | I ′ | - 2, we conclude that m is greater than zero also in this case. ✷

In the next proposition, we show that the bound n - 4 is tight.

Proposition 2.1.6. There exists a point set Q such that ⊠ ( 1 - DG ( Q )) = n - 4 .

Proof. We start with n - 2 points in a vertical segment, denoted from top to bottom by q 1 , q 2 , . . . , qn - 2. We add one point to the left of this group, and one point to the right, as in Fig. 3(left). Then we slightly move the even points q 2 , q 4 , . . . to the right, and the odd points q 3 , q 5 , . . . to the left.

The only red edges in 1DG ( Q ) are qi q i + 2 , for i = 1 , 2 , . . . , n - 4. No pair of such edges crosses, and each of them creates exactly one crossing with 0DG ( Q ) . Thus the number of crossings of 1DG ( Q ) is n - 4. ✷


<!-- p:6 -->


Fig. 3. Left: point set whose 1-Delaunay graph has n - 4 crossings. Right: point set in convex position whose 1-Delaunay graph has 6 n - 3 ⌊ n 2 ⌋- 19 crossings.

Now assume that P is in convex position. In this case, the minimum number of red edges contained in any 1-Delaunay graph is larger [1] and, on average, these edges create more crossings. As a result, the rectilinear crossing number is larger than in the general case. In the following results we show that, for point sets in convex position, the rectilinear crossing number is roughly 9 n / 2.

Theorem 2.1.7. For every point set P in convex position, ⊠ ( 1 - DG ( P )) ⩾ 6 n - 3 ⌊ n 2 ⌋ - 19 .

Proof. Let p 1 , . . . , pn denote the points in P in clockwise order. Note that all edges of type pi p i + 2 are in 1DG ( P ), and that the total number of crossings between two edges of this family is n . Let G ′ be the graph obtained from 1DG ( P ) by removing these edges and the ones in the convex hull of P . Since | Er | ⩾ 2 n -⌊ n 2 ⌋ - 5 (see [1]), G ′ contains at least 2 n -⌊ n 2 ⌋ - 8 edges. Each of them induces two crossings with the edges that have been removed.

Adding everything up, the graph 1DG ( P ) has no less than 6 n - 3 ⌊ n 2 ⌋ - 19 crossings. ✷

Let G ′ p be a maximal planar subgraph of G ′ . It is easy to see that G ′ p contains at most n - 5 edges. Thus there are at least n -⌊ n 2 ⌋ - 3 edges in G ′ but not in G ′ p , each of which induces at least one crossing with an edge of G ′ p .

Proposition 2.1.8. There exists a point set Q in convex position such that ⊠ ( 1 - DG ( Q )) = 6 n - 3 ⌊ n 2 ⌋ - 19 .

Proof. Consider two horizontal lines such that each point in one line has a counterpart in the other line with the same abscissa. Add one point to the left of both lines such that its ordinate is the average of the ordinates of the lines. If the positions of the points are carefully chosen, it is possible to perturb them so that the point set is in convex position and 1DG ( Q ) contains only the edges drawn in Fig. 3(right). Easy calculations show that, in this case, the number of crossings of the graph is 6 n - 3 ⌊ n 2 ⌋ - 19. ✷

#### 2.2. Worst crossing number

While there exist point sets whose 1-Delaunay graph contains a linear number of crossings, the number of crossings in 1DG ( P ) could in principle be quadratic in other cases, since any pair of red edges might cross. In the following lines, we provide quadratic upper bounds on the number of crossings of 1DG ( P ) , and show examples where 1DG ( P ) contains a quadratic number of crossings.

The more general Theorem 4.2.1 says that at most 12 n 2 - 63 n + 81 crossings are present in 1DG ( P ) . In the following proof, we improve the dominant term of this bound to 4 n 2 .

A crossing in 1DG ( P ) is caused either by a red edge and a blue one or by a pair of red edges. We denote the cardinal number of the first and second sets of crossings by r ⊗ b and r ⊗ r , respectively. We derive upper bounds for r ⊗ b and r ⊗ r . The bound for r ⊗ b is given in Lemma 2.2.4 and requires several technical lemmas and observations.

Observation 2.2.1. Let pi p j and pl pm be two crossing edges. Either every circle through pi and p j contains pl or pm , or every circle through pl and pm contains pi or p j .

Lemma 2.2.2. If u , v , and w are three vertices of a planar graph G on n vertices, then dG ( u ) + dG ( v ) + dG ( w ) ⩽ 2 n + 2 .

Proof. Let V ′ ( G ) be the set of vertices in V ( G ) \ { u , v , w } that are adjacent to u , v , and w . Then dG ( u ) + dG ( v ) + dG ( w ) ⩽ 3 | V ′ ( G ) | + 2 ( n - 3 -| V ′ ( G ) | ) + 6 = 2 n +| V ′ ( G ) | . Since the graph K 3 , 3 is not planar, we have that | V ′ ( G ) | ⩽ 2. ✷

Lemma 2.2.3. Let G be a graph on n vertices. If G is a plane triangulation, then ∑ v ∈ V ( G ) d 2 G ( v ) ⩽ 2 n 2 + 33 n .

Proof. We prove the lemma by induction on n . The small cases are trivial. We proceed to the inductive step.

Let us first assume that there exists a vertex v ′ not in the external face having degree three, four, or five. Let G ′ be a graph containing all the edges in G \ v ′ and where the face bounded by the neighbors of v ′ in G has been triangulated. Let w 1 , w 2 , . . . , wI be the vertices in V ( G ) such that dG ′ ( wi ) = dG ( wi ) - 1 . Note that: if dG ( v ′ ) = 3, then I = 3; if dG ( v ′ ) = 4, then I = 2; and, if dG ( v ′ ) = 5, then I = 2. For any v ∈ V ( G ) , v ̸= v ′ , w 1 , . . . , wI , we have that dG ( v ) ⩽ dG ′ ( v ). Then


<!-- p:7 -->


Fig. 4. Crossings assigned to p . In the left figure, p is an interior point of P ; in the right figure, it belongs to the convex hull of P . The dashed edges correspond to the dual graphs of the triangulations given by the red edges.

$$\text { then } I & = 2 ; \text { and, if } d _ { G } ( v ^ { \prime } ) = 5 , \text { then } I = 2 . \text { For any } v \in V ( G ) , \, v \neq v ^ { \prime } , \, w _ { 1 } , \dots , v \\ & \sum _ { v \in V ( G ) } d _ { G } ^ { 2 } ( v ) = \sum _ { v \neq v ^ { \prime } , \, w _ { i } } d _ { G } ^ { 2 } ( v ) + d _ { G } ^ { 2 } ( v ^ { \prime } ) + \sum _ { i = 1 , \dots , I } d _ { G } ^ { 2 } ( w _ { i } ) \\ & \leqslant \sum _ { v \neq v ^ { \prime } } d _ { G ^ { \prime } } ^ { 2 } ( v ) + 2 \sum _ { i = 1 , \dots , I } \, d _ { G ^ { \prime } } ( w _ { i } ) + d _ { G } ^ { 2 } ( v ^ { \prime } ) + I \\ & \leqslant \sum _ { v \neq v ^ { \prime } } d _ { G ^ { \prime } } ^ { 2 } ( v ) + 2 \sum _ { i = 1 , \dots , I } \, d _ { G ^ { \prime } } ( w _ { i } ) + 2 7 . \\ \text {By the induction hypothesis and Lemma 2.2.2,}$$

By the induction hypothesis and Lemma 2.2.2,

$$\sum _ { v \in V ( G ) } d _ { G } ^ { 2 } ( v ) & \leqslant 2 ( n - 1 ) ^ { 2 } + 3 3 ( n - 1 ) + 2 ( 2 n + 2 ) + 2 7 = 2 n ^ { 2 } + 3 3 n . \\ \\$$

Now suppose that all the interior vertices have degree at least six (or there are no interior vertices). Let H be the set of vertices in the external face. By the handshaking lemma, ∑ v ∈ H dG ( v ) ⩽ 4 | H | - 6 . Consequently, there exists a vertex in the external face having degree three or two, and the same strategy can be used to prove the inequality. ✷

Lemma 2.2.4. For every set of points P , r ⊗ b ⩽ n 2 + Θ( n ).

Proof. If there is a crossing between a red edge r and a blue edge b = pi p j , then, by Observation 2.2.1, r is generated by pi or p j (or both). We assign the crossing to this point (or to any of them if r is generated by both).

First assume that p is not in the convex hull of P . Let ek = pqk be a blue edge incident to p ; we want to know how many edges in 0DG ( P \ { p } ) it may cross. Consider the triangulation T constituted by the cycle connecting the neighbors of p in 0DG ( P ) and the edges generated by p . (See Fig. 4, left.) Let T p be the triangle containing p and Tqk be the triangle incident to qk that is traversed by ek ( Tqk = T p if qk is a vertex of T p ). Observe that the number of edges in 0DG ( P \ { p } ) that ek crosses corresponds to the distance between Tqk and T p in the dual graph of T . Observe also that, if qk and ql are two different vertices that are adjacent to p in 0DG ( P ) and are not vertices of T p , we have that Tqk ̸= Tql . Then the configuration of the dual graph maximizing the sum of distances between Tqk and T p , for all qk neighbor of p in 0DG ( P ) (and not a vertex of T p ), is a tree rooted at T p . Consequently, at most ∑ dG ( p ) - 3 ν = 1 ν crossings (where G = 0DG ( P ) ) are assigned to p .

Next we bound the number of crossings that may be assigned to some point p ∈ P .

Next suppose that p is a vertex of the convex hull of P . Let q 1 , q 2 , . . . , qdG ( p ) be the neighbors of p in 0DG ( P ) in radial order around p ( G = 0DG ( P ) ). Let q τ be the first point that belongs to the convex hull of P \{ p } but does not belong to the convex hull of P (if there is not such q τ , we set q τ = qdG ( p ) ). Let us look at the triangulation of the polygon pq 1 q 2 . . . q τ p given by the red edges. In order to determine the number of edges in 0DG ( P \ { p } ) that an edge pqk ( k ∈ { 2 , 3 , . . . , τ - 1 } ) crosses, we can use the same argument as before, except that in this case T p is defined as the triangle having p as a vertex. We look at the next point that belongs to the convex hull of P \ { p } but does not belong to the convex hull of P (let us denote it by q ι ) and apply the same argument to the edges of the polygon pq τ q τ + 1 . . . q ι p . We proceed in this way until we reach qdG ( p ) . Then the number of crossings that may be assigned to p is less than or equal to ∑ dG ( p ) - 2 ν = 1 ν.

Now the result follows from Lemma 2.2.3. ✷

Next we give an upper bound for r ⊗ r .

Lemma 2.2.5. For every set of points P , r ⊗ r ⩽ 3 n 2 + Θ( n ).


<!-- p:8 -->

Fig. 5. Left: point set whose 1-Delaunay graph has n 2 + Θ( n ) crossings. Right: point set in convex position whose 1-Delaunay graph has n 2 / 2 + Θ( n ) crossings.

Proof. Let the red crossing graph be the graph whose vertices are the red edges of 1DG ( P ) and where two vertices are adjacent if their corresponding edges cross. In (3) we have seen that | Er | ⩽ 3 n -| H | - 6, that is, the red crossing graph has no more than 3 n -| H | - 6 vertices. We will show that the red crossing graph has no 4-clique. Then we apply Turán's theorem [29], which states that any Kr + 1-free graph on m vertices has at most ( 1 - 1 r ) m 2 2 edges. This yields the result.

Let us prove that the red crossing graph is K 4-free. We orient an edge from pl pm to pi p j in the red crossing graph, if every circle through pi and p j contains pl or pm . By Observation 2.2.1, every edge of the red crossing graph is oriented. The definition of red edges implies that, if two edges in the red crossing graph are oriented from pl pm to pi p j and from pr ps to pi p j , then, in 1DG ( P ) , pl pm and pr ps have a common endpoint. Thus, if a subset of vertices form a clique in the red crossing graph, in the subgraph induced by these vertices every vertex has in-degree at most one, but such an orientation is impossible for K 4. Therefore the red crossing graph is K 4-free. ✷

From Lemmas 2.2.4 and 2.2.5, we derive the next theorem.

Theorem 2.2.6. For every set of points P , ⊠ ( 1 - DG ( P )) ⩽ 4 n 2 + Θ( n ).

To complete the proof that the worst crossing number of the 1-Delaunay graph is quadratic, it remains to describe a point set whose 1-Delaunay graph contains a quadratic number of crossings.

Proposition 2.2.7. There exists a point set Q such that ⊠ ( 1 - DG ( Q )) = n 2 + Θ( n ).

Proof. We use the construction shown in Fig. 5(left). The number of crossings involving two points from the middle group and either two points from the upper group or two points from the lower group is 2 ( n - 4 2 ) . ✷

Now assume that P is in convex position. In the previous subsection we have seen that in this situation the rectilinear crossing number is larger than in the general case. Surprisingly, the worst crossing number behaves differently: both our lower and upper bounds are smaller in the convex case.

The upper bound is given in Theorem 2.2.9. We need a technical result.

Lemma 2.2.8. If G is a graph such that | V ( G ) | = n and | E ( G ) | ⩽ n - 5 , then ∑ v ∈ V ( G ) d 2 G ( v ) ⩽ | E ( G ) | 2 + 3 | E ( G ) | .

Proof. The proof of the lemma is by induction on n . As in the proof of Lemma 2.2.3, the small cases are trivial, so we proceed to the inductive step.

First, assume that v ′ has degree zero. If G has no edges, the result trivially holds. Otherwise, let uw be an edge of G and let G ′ be defined as the graph G \ v ′ \ uw . We have that

Observe that there exists a vertex v ′ in the graph having degree zero or one. We distinguish two cases.

$$let G ^ { \prime } \, \text { be defined as the graph } G \, \vee \, v ^ { \prime } \, \ u w . \, & \text { We have that} \\ \sum _ { v \in V ( G ) } d _ { G } ^ { 2 } ( v ) & = \sum _ { v \neq v ^ { \prime } , u , w } d _ { G } ^ { 2 } ( v ) + d _ { G } ^ { 2 } ( v ^ { \prime } ) + d _ { G } ^ { 2 } ( u ) + d _ { G } ^ { 2 } ( w ) \\ & = \sum _ { v \neq v ^ { \prime } , u , w } d _ { G ^ { \prime } } ^ { 2 } ( v ) + \left ( d _ { G ^ { \prime } } ( u ) + 1 \right ) ^ { 2 } + \left ( d _ { G ^ { \prime } } ( w ) + 1 \right ) ^ { 2 } \\ & = \sum _ { v \in V ( G ^ { \prime } ) } d _ { G ^ { \prime } } ^ { 2 } ( v ) + 2 ( d _ { G ^ { \prime } } ( u ) + d _ { G ^ { \prime } } ( w ) ) + 2 . \\ \text {Applying the induction hypothesis and using the fact that } d _ { G ^ { \prime } } ( u ) + d _ { G ^ { \prime } } ( w ) & \leqslant | E ( G ^ { \prime } ) |$$

$$\sum _ { \nu \in V ( G ) } d _ { G } ^ { 2 } ( \nu ) \leqslant \left ( | E ( G ) | - 1 \right ) ^ { 2 } + 3 \left ( | E ( G ) | - 1 \right ) + 2 \left | E ( G ) \right | + 2 = \left | E ( G ) \right | ^ { 2 } + 3 \left | E ( G ) \right | .$$

Applying the induction hypothesis and using the fact that dG ′ ( u ) + dG ′ ( w ) ⩽ | E ( G ′ ) | + 1 , Next, suppose that v ′ has degree one. Let u be the vertex adjacent to v ′ in G , and G ′ be the graph G \ v ′ . Then


<!-- p:9 -->


$$\text {Next, suppose that } \ v ^ { \ } h \text { degree one. Let } u \text { be the vertex adjacent to } v ^ { \ } h \text { in } C , \text { and } C ^ { \ } b \text { the graph } C \vee v . \text { Then} \\ \sum _ { \ v \in V ( G ) } d _ { G } ^ { 2 } ( v ) = \sum _ { \ v \neq v ^ { \prime } , u } d _ { G } ^ { 2 } ( v ) + d _ { G } ^ { 2 } ( v ^ { \prime } ) + d _ { G } ^ { 2 } ( u ) = \sum _ { \ v \neq v ^ { \prime } , u } d _ { G ^ { \prime } } ^ { 2 } ( v ) + 1 + ( d _ { G ^ { \prime } } ( u ) + 1 ) ^ { 2 } \\ = \sum _ { \ v \in V ( G ) } d _ { G ^ { \prime } } ^ { 2 } ( v ) + 2 d _ { G ^ { \prime } } ( u ) + 2 \leq \left ( | E ( G ) | - 1 \right ) ^ { 2 } + 3 \left ( | E ( G ) | - 1 \right ) + 2 \left ( | E ( G ) | - 1 \right ) + 2 \\ \leq | E ( G ) | ^ { 2 } + 3 | E ( G ) | . \quad \Box \\ \text {Theorem} \ 2 . 2 . 9 \text { For every set of points } P \text { in convex position, } \varnothing ( 1 - \text {DG} ( P ) ) \leq 7 n ^ { 2 } / 8 + \varTheta ( n ) .$$

Theorem 2.2.9. For every set of points P in convex position, ⊠ ( 1 - DG ( P )) ⩽ 7 n 2 / 8 + Θ( n ).

Proof. If P is in convex position, then | Eb | = 2 n - 3. Since, in general, | Er | ⩽ 3 n -| H | - 6 (see (3)), in the convex case we have that | Er | ⩽ 2 n - 6.

For all i , the edges pi p i + 1 are not involved in any crossing. The edges of the form pi p i + 2 participate in a total number of at most 5 n - 18 crossings, as pairs of edges of this type generate n crossings, and each of the (at most) 2 n - 9 remaining edges in 1DG ( P ) induces two crossings with them. Let r ′ ⊗ r ′ denote the number of crossings between two red edges that are not of the form pi p i + 2 . Then

Let pi , pi + 1 , and pi + 2 be three consecutive points in the convex hull of P . Let us suppose that we momentarily remove from 1DG ( P ) the edges pi p i + 1 , pi + 1 pi + 2 , and pi p i + 2 for all i . Let | Eb ′ | and | Er ′ | be the number of blue and red edges, respectively, in 1DG ( P ) after these removals. It is not difficult to see that n / 2 - 3 ⩽ | Eb ′ | ⩽ n - 5 and | Er ′ | ⩽ 2 n - 9 -| Eb ′ | .

$$\mathbb { Z } ( 1 { - } D G ( P ) ) & \leqslant r \otimes b + r ^ { \prime } \otimes r ^ { \prime } + 5 n - 1 8 . \\ \text {Let } G & = 0 { - } D G ( P ) \text { and } G ^ { \prime } \text { be the graph on } P \text { consisting}$$

Let G = 0DG ( P ) and G ′ be the graph on P consisting of the edges of G not of the form pi p i + 1 or pi p i + 2 . As we have seen in Lemma 2.2.4,

$$r \otimes b \leqslant \sum _ { p \in P } \sum _ { \nu = 1 } ^ { d _ { G } ( p ) - 2 } \nu = \frac { 1 } { 2 } \sum _ { p \in P } ( d _ { G } ^ { 2 } ( p ) - 3 d _ { G } ( p ) + 2 ) . \\$$

Notice that, for all p ∈ P , dG ( p ) = dG ′ ( p ) + 4. Hence

$$r \otimes b \leqslant \frac { 1 } { 2 } \sum _ { \nu \in P } ( d _ { G ^ { \prime } } ^ { 2 } ( \nu ) + 5 d _ { G ^ { \prime } } ( \nu ) + 6 ) . \\ \intertext { r \otimes b \leqslant \frac { 1 } { 2 } \sum _ { \nu \in P } ( d _ { G ^ { \prime } } ^ { 2 } ( \nu ) + 5 d _ { G ^ { \prime } } ( \nu ) + 6 ) . } \intertext { B y l e m m a 2 3 8 }$$

By Lemma 2.2.8,

$$r \otimes b \leqslant \frac { | E _ { b ^ { \prime } } | ^ { 2 } } { 2 } + \frac { 1 3 | E _ { b ^ { \prime } } | } { 2 } + 3 n .$$

Next we bound r ′ ⊗ r ′ . Recall that | Er ′ | ⩽ 2 n - 9 -| Eb ′ | . Following the same argument as in the proof of Lemma 2.2.5, we obtain

$$r ^ { \prime } \otimes r ^ { \prime } \leqslant \frac { ( 2 n - 9 - | E _ { b ^ { \prime } } | ) ^ { 2 } } { 3 } .$$

Thus, putting everything together,

$$\mathbb { Z } ( 1 { \text {-DG} } ( P ) ) & \leqslant \frac { 5 | E _ { b ^ { \prime } } | ^ { 2 } } { 6 } + \left ( \frac { 2 5 } { 2 } - \frac { 4 n } { 3 } \right ) | E _ { b ^ { \prime } } | + \left ( \frac { 4 n ^ { 2 } } { 3 } - 4 n + 9 \right ) = \colon f ( | E _ { b ^ { \prime } } | ) . \\ \intertext { \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text$$

For n large enough, the maximum value of the function f ( | Eb ′ | ) in the domain [ n / 2 - 3 , n - 5 ] is achieved in the lower extreme of the interval and is equal to 7 n 2 / 8 + 15 n / 4 - 21. This completes the proof. ✷

In our best construction the 1-Delaunay graph contains roughly n 2 / 2 crossings.

Proposition 2.2.10. There exists a set of points Q in convex position such that ⊠ ( 1 - DG ( Q )) = n 2 / 2 + Θ( n ).

Proof. Consider a set of n - 2 points on an arc of a circle together with 2 points close to its center, as in Fig. 5(right). In the graph 1DG ( Q ) each point in the circular chain is adjacent to both central points. Therefore the number of crossings of 1DG ( Q ) is greater than ( n - 2 2 ) . ✷


<!-- p:10 -->


Fig. 6. Set of 56 points whose 5-NNG is plane.

### 3. k -nearest neighbor graphs for small values of k

We provide bounds on the rectilinear crossing number of the k -nearest neighbor graph k - NNG for small values of k . Due to the inclusion relations satisfied by the graphs we investigate, the lower bounds also hold for the rectilinear crossing number of the other proximity graphs if we shift the value of k one unit down. (See (1).)

#### 3.1. kNNG for k ⩽ 10

Our results are stated in the following propositions. It is interesting to notice that, even though the lower bounds do not rely on specific properties of k - NNG but on generic results, for many values of k we are able to construct point sets attaining these bounds.

The k -nearest neighbor graphs of all the constructions in this section have been obtained by means of a computer program implemented by the authors. The arrows in the figures have been suppressed for the sake of clarity.

Proposition 3.1.1. For any n ⩾ 44 and k ⩽ 5 , cr ( kNNG ( n )) = 0 .

Proof. It suffices to prove the result for k = 5.

We start considering values of n of the form n = 4 l , with l ⩾ 13 . We place the following four groups of l points ( i ∈ { 1 , 2 , . . . , l } ):

$$& \{ 1 , 2 , \dots , l \} ; \\ & p _ { i } = \frac { 1 } { 2 \sin ( \pi / l ) } \left ( \cos \left ( \frac { 2 \pi i } { l } \right ) , \sin \left ( \frac { 2 \pi i } { l } \right ) \right ) , \\ & q _ { i } = \left ( \frac { 1 } { 2 \tan ( \pi / l ) } + \frac { \sqrt { 3 } } { 2 } \right ) \left ( \cos \left ( \frac { 2 \pi i } { l } + \frac { \pi } { l } \right ) , \sin \left ( \frac { 2 \pi i } { l } + \frac { \pi } { l } \right ) \right ) , \\ & r _ { i } = \frac { 1 } { 2 \sin ( \pi / l ) ( 1 - 2 \sin ( \pi / l ) ) } \left ( \cos \left ( \frac { 2 \pi i } { l } \right ) , \sin \left ( \frac { 2 \pi i } { l } \right ) \right ) , \\ & s _ { i } = \left ( \frac { 1 } { 2 \tan ( \pi / l ) } + \frac { \sqrt { 3 } } { 2 } \right ) ( 1 + 2 \sin ( \pi / l ) \left ( \cos \left ( \frac { 2 \pi i } { l } + \frac { \pi } { l } \right ) , \sin \left ( \frac { 2 \pi i } { l } + \frac { \pi } { l } \right ) \right ) ) . \\ & \text {These points correspond to four regular and noncentric $l$-gons with increasing radius} \, (see Fig. 6). \, \text {E} . \\ \text {that} \, | p _ { i } p _ { i + 1 } | = | p _ { i + 1 } q _ { i } | = 1 , \ | p _ { i } r _ { i } | = | r _ { i } r _ { i + 1 } | , \ and \ | q _ { i } q _ { i + 1 } | = | q _ { i } s _ { i } | . \ \text {In order to break the} \, \text {land} .$$

These points correspond to four regular and concentric l -gons with increasing radius (see Fig. 6). Easy calculations show that | pi p i + 1 | = | pi + 1 qi | = | qi p i | = 1 , | pi r i | = | r i r i + 1 | , and | qi q i + 1 | = | qi s i | . In order to break the last two equalities, we slightly decrease the radius of the third and fourth polygons. We also perturb the points to reach a general position.

The five-nearest neighbor graph of the resulting set of points has the edges shown in Fig. 6. In particular, it is plane. If l &lt; 13 , the adjacencies change and the graph contains several crossings. However, for l = 11 and l = 12 these crossings can be removed by decreasing a bit the radius of the third circle. So we have proved that for any n ⩾ 44 , n ≡ 0 ( mod 4 ), there exists an n -point set Qn whose five-nearest neighbor graph is plane.

If n = 4 l + j , with l ⩾ 11 and j ∈{ 1 , 2 , 3 } , then we can add j points close to the center of the set Q 4 l in such a way that the five-nearest neighbor graph remains plane. ✷


<!-- p:11 -->


Fig. 7. Set of 78 points whose 6NNG has 52 crossings.

Remark 3.1.2. For k ⩽ 4 , we have obtained sets of less than 44 points whose k - NNG is plane. Specifically, if k ∈{ 1 , 2 , 3 } , we can construct point sets of any size greater than k whose k - NNG is plane. For k = 4 , we can construct point sets of size at least 14 whose k - NNG is plane. The details of these constructions will be given in [25].

In a 6NNG all vertices have degree 6 or greater. This implies that the number of edges is at least 3 n , which prevents these graphs from being plane. In the next proposition, we show that the minimum number of crossings is bounded by a constant.

Proposition 3.1.3. For any n ⩾ 39 , cr ( 6 - NNG ( n )) ⩽ 58 .

Proof. Let us first assume that n = 13 l , with l ⩾ 3 .

Consider a group of l regular and concentric 13-gons R 1 , R 2 , . . . , Rl . The polygon Ri , for i ∈ { 2 , 3 , . . . , l - 1 } , is rotated by an angle of π/ 13 with respect to the polygon Ri - 1 , while Rl is rotated by an angle slightly larger than π/ 13 with respect to Rl - 1 to break ties. The radius of R 1 is 0.9, and the radius of Ri for i &gt; 2 is 1 . 386 i - 1 . The points are perturbed so that they are in general position. See Fig. 7.

Regardless of the value of l , the six-nearest neighbor graph of this set of points has 52 crossings, as the crossings only involve vertices from R 1 , Rl - 2 , Rl - 1 , and Rl . This settles the problem for values of n that are multiples of 13.

If n = 13 l + j , with l ⩾ 3 and j ∈{ 1 , 2 , . . . , 12 } , we add j consecutive points of the polygon Rl + 1 . The six-nearest neighbor graph of the new point set has 6 extra crossings. ✷

For values of k which are a constant greater than 6, the graph k - NNG contains a linear number of crossings. In Proposition 3.1.5, we provide lower bounds for k ∈ { 7 , 8 , 9 , 10 } . We use the following result:

Lemma 3.1.4. (See [22].) The crossing number of any graph G with | V ( G ) | ⩾ 3 vertices and | E ( G ) | edges satisfies

$$c r ( G ) & \geqslant \frac { 7 } { 3 } | E ( G ) | - \frac { 2 5 } { 3 } \left ( | V ( G ) | - 2 \right ) . \\$$

Proposition 3.1.5. For any n ⩾ 11 ,

- (i) cr ( 7 - NNG ( n )) ⩾ n 2 + 6 ,
- (iii) cr ( 9 - NNG ( n )) ⩾ 13 n 6 + 50 3 , and
- (ii) cr ( 8 - NNG ( n )) ⩾ n + 50 3 ,

- (iv) cr ( 10 - NNG ( n )) ⩾ 10 n 3 + 50 3 .


<!-- p:12 -->


Fig. 8. Left: point set whose 7NNG has n / 2 + Θ( 1 ) crossings. Right: point set whose 8NNG has n + Θ( 1 ) crossings.

Proof. For every set of points P , the number of edges of k - NNG ( P ) is at least kn / 2, because each vertex has degree k or greater. Now the first bound follows from the well-known fact that, for any graph G , its crossing number satisfies that cr ( G ) ⩾ | E ( G ) | - ( 3 | V ( G ) | - 6 ) . The remaining bounds are a corollary of Lemma 3.1.4. ✷

In the case of k ∈{ 7 , 8 } , we can provide examples that match the lower bound, except for the term of constant size.

Proposition 3.1.6. For any n ⩾ 8 , cr ( 7 - NNG ( n )) ⩽ n 2 + Θ( 1 ).

Proof. If n ⩽ 24, the result is trivial.

If n = 25 l with l ⩾ 1, we place l regular and concentric 25-gons R 1 , R 2 , . . . , Rl . (See Fig. 8, left.) The polygons Ri such that i = 4 j + 1 or i = 4 j + 2 for some j ⩾ 0 have all the same orientation, while the remaining polygons are rotated by an angle of π/ 25 with respect to them. For all i , the radius of Ri is 1 . 27 i . The points are perturbed to attain general position.

Ignoring some crossings that occur near the boundaries, the seven-nearest neighbor graph of this point set contains n / 2 crossings (or ( n - 25 )/ 2, depending on the parity of l ), because the crossings only take place between consecutive 25-gons of the form R 2 j + 1 , R 2 j + 2 , and the number of such crossings for each pair is 25. The crossings near the boundaries only contribute an additive factor of constant size.

Finally, if n = 25 l + j , with l ⩾ 1 and j ∈ { 1 , 2 , . . . , 24 } , we add j consecutive points of the polygon Rl + 1 . This only adds a constant number of crossings. ✷

Proposition 3.1.7. For any n ⩾ 9 , cr ( 8 - NNG ( n )) ⩽ n + Θ( 1 ).

Proof. We also use concentric polygons. For constant values of n the bound is trivial, and for n = 26 l + j we use the same strategy as in previous cases, so here we focus on the case where n = 26 l . We consider l regular and concentric 26-gons R 1 , R 2 , . . . , Rl with the same orientation. (See Fig. 8, right.) For all i , the radius of Ri is 1 . 3 i . The points are infinitesimally perturbed.

The eight-nearest neighbor graph of this point set has n + Θ( 1 ) crossings. The linear term comes from the fact that in the region between any pair of consecutive 26-gons there are 26 crossings. The constant term comes from some additional crossings that take place near the boundaries of the point set. ✷

For k = 9 and k = 10 there is a small gap between the upper bounds that can be derived from our constructions and the lower bounds stated in Proposition 3.1.5.

Proposition 3.1.8. For any n ⩾ 10 , cr ( 9 - NNG ( n )) ⩽ 9 n / 4 + Θ( 1 ).

Proof. We propose the construction in Fig. 9(left). The points are placed in horizontal lines forming strips that can be gathered in groups of six units. The first group of six strips is described as follows: The first strip contains all points of the form ( 3 j , 0 ) and ( 3 j + 1 , 0 ) , with j ∈ Z . The second strip contains all points of the form ( 3 j + 3 2 , √ 3 2 ) and ( 3 j + 5 2 , √ 3 2 ) . The third, fourth, fifth, and sixth strip contain all points of the form ( 3 j + 1 2 , 7 √ 3 6 ) , ( 3 j + 2 , 11 √ 3 6 ) , ( 3 j + 1 2 , 16 √ 3 6 ) , and


<!-- p:13 -->


Fig. 9. Left: point set whose 9NNG has 9 n / 4 + Θ( √ n ) crossings. Right: point set whose 10NNG has 11 n / 3 + Θ( √ n ) crossings.

( 3 j + 2 , 10 √ 3 3 ), respectively. The next group of strips consists of a copy of the first group where the ordinate of all points is increased by 4 √ 3. This step can be iterated to produce all the points in the construction.

Proposition 3.1.9. For any n ⩾ 11 , cr ( 10 - NNG ( n )) ⩽ 11 n / 3 + Θ( 1 ).

A careful analysis of the drawing yields that the nine-nearest neighbor graph of the point set has 9 n / 4 + Θ( √ n ) crossings. The term Θ( √ n ) comes from crossings that take place near the boundary of the point set. Since the nine-nearest neighbors of each point are well-defined, the point positions can be slightly perturbed without modifying the set of nearest neighbors of each point. Thus we can rearrange the points in circular strips, where each strip contains exactly the minimum number of points ensuring that the adjacencies in the nine-nearest neighbor graph do not change. This reduces the number of crossings to 9 n / 4 + Θ( 1 ). We omit further details due to the high complexity of the point set. ✷

Proof. Our point set is shown in Fig. 9(right). As in the previous construction, the points form horizontal strips, and these strips can be organized in groups of six units. The first group of six strips contains all points of the form ( 2 j , 0 ) , ( 2 j , 1 ) , ( 2 j , 2 ) , ( 2 j + 1 . 1 , 2 . 5 ) , ( 2 j + 1 , 3 . 5 ) , and ( 2 j , 4 ) , with j ∈ Z . The next group of strips consists of a copy of the first group where the ordinate of all points is increased by 5. This step is iterated to complete the construction.

It can be seen that the ten-nearest neighbor graph of the point set contains 11 n / 3 + Θ( √ n ) crossings. Using the same strategy as in the previous example, we can modify the construction to obtain a new set of points whose 10NNG has 11 n / 3 + Θ( 1 ) crossings. ✷

So far we have analyzed the rectilinear crossing number of the k -nearest neighbor graphs for values of k smaller than 11. As for the worst crossing number, we will give bounds for all k in Section 4, and we can improve on these only minimally for small k . Those details will be given in [25].

### 4. General bounds

In this section, we are interested in the number of crossings in the graphs under study when the value of k is large. We have derived bounds for both the rectilinear crossing number and the worst crossing number of all graphs. In all cases, we can specify the exact order of magnitude of these parameters up to multiplicative constants.

#### 4.1. Rectilinear crossing number

Our lower bounds for the rectilinear crossing numbers follow from an improved version of the crossing lemma.

Lemma 4.1.1. (See [22].) The crossing number of any graph G such that | E ( G ) | ⩾ 103 16 | V ( G ) | satisfies cr ( G ) ⩾ 1024 31827 | E ( G ) | 3 | V ( G ) | 2 .

For every set of points P , the number of edges of k - NNG ( P ) is no less than kn / 2. A stronger lower bound is known for the graph k - DG ( P ) : If k &lt; n 2 - 1, then the number of edges of k - DG ( P ) is at least ( k + 1 ) n [1]. As observed in the same paper, for any n and k such that n ⩾ k ⩾ n 2 - 1, graph k - DG ( P ) is the complete graph. In particular, for k = n 2 - 1 the number of edges is greater than kn . Consequently, Theorem 4.1.2. If 13 ⩽ k ⩽ n - 1 , then cr ( kNNG ( n )) ⩾ 128 31827 k 3 n . If 6 ⩽ k ⩽ n 2 - 1 , then cr ( kDG ( n )) ⩾ 1024 31827 k 3 n .


<!-- p:14 -->


Corollary 4.1.3. If 13 ⩽ k ⩽ n - 1 , then cr ( kRNG ( n )) ⩾ 128 31827 k 3 n and cr ( kGG ( n )) ⩾ 128 31827 k 3 n .

For the upper bounds, we use a suitable construction proposed in [24]. We note that, instead of π/ 9, the incorrect coefficient 2 π/ 27 was originally reported. The correct coefficient was later reported in [22].

Lemma 4.1.4. (See [24].) Let ω( 1 ) ⩽ d ⩽ o ( √ n ) . Let Q be a set of n points arranged in a slightly perturbed unit square grid of size √ n × √ n, so that the points are in general position. Define G d as the geometric graph on Q where two points are connected if their distance is at most d. Then the number of crossings in G d satisfies ⊠ ( Gd ) = π 9 nd 6 + o ( nd 6 ) .

This construction is the current asymptotically best example of a graph with fixed number of edges and minimum number of crossings. In the next proposition, we show that it can be seen as a proximity graph.

Proposition 4.1.5. If ω( 1 ) ⩽ k ⩽ o ( n ), there exists a point set Q such that

- (i) ⊠ ( kNNG ( Q )) ⩽ 1 9 π 2 k 3 n + o ( k 3 n ),
- (iii) ⊠ ( kGG ( Q )) ⩽ 64 9 π 2 k 3 n + o ( k 3 n ), and
- (ii) ⊠ ( kRNG ( Q )) ⩽ π 9 ( 2 π/ 3 - √ 3 / 2 ) 3 k 3 n + o ( k 3 n ),
- (iv) ⊠ ( kDG ( Q )) ⩽ 64 9 π 2 k 3 n + o ( k 3 n ).

Proof. Let Q be the set described in Lemma 4.1.4. First note that the k closest points to a point in Q not close to the boundary consist of those points inside a circle of radius √ k /π + Θ( 1 ) . Let d be the value of this radius. For the points close to the boundary, that is, at distance at most d from it, their k closest points consist of those points in Q inside a circle of radius at most 2 d . Thus k - NNG ( Q ) has all the edges in Gd and some of the edges in G 2 d whose endpoints are within d of the boundary. Thus

$$\mathbb { Z } ( k { \text {NG} } ( Q ) ) & \leqslant \frac { \pi } { 9 } n ^ { 6 } + o ( n ^ { 6 } ) + \left ( \frac { \pi } { 9 } n ( 2 d ) ^ { 6 } + o ( n d ^ { 6 } ) - \frac { \pi } { 9 } ( \sqrt { n } - 2 d ) ^ { 2 } ( 2 d ) ^ { 6 } - o ( ( \sqrt { n } - 2 d ) ^ { 2 } d ^ { 6 } ) \right ) \\ & \leqslant \frac { \pi } { 9 } n ^ { 6 } + o ( n d ^ { 6 } ) + \Theta ( \sqrt { n } d ^ { 7 } ) = \frac { \pi } { 9 } n ^ { 6 } + o ( n d ^ { 6 } ) = \frac { 1 } { 9 \pi ^ { 2 } } k ^ { 3 } n + o ( n d ^ { 6 } ) . \\ \text {Except for a similar analysis for the points close to the boundary, two points in } Q \text { are neighbors in } k { \text {RG} } ( Q ) \text { if their }$$

Except for a similar analysis for the points close to the boundary, two points in Q are neighbors in k - RNG ( Q ) if their distance is at most d = √ k /( 2 π/ 3 - √ 3 / 2 ) + Θ( 1 ) . Similarly, two points are neighbors in k - GG ( Q ) or in k - DG ( Q ) if their distance is at most d = 2 √ k /π . The result follows by Lemma 4.1.4 and by noting that the extra crossings caused by the points close to the boundary are at most o ( nd 6 ) . ✷

#### 4.2. Worst crossing number

Any upper bound on the number of edges of some higher order proximity graph can be used to produce an upper bound on its worst crossing number. For k -Delaunay graphs, it has been proved that the number of edges is at most 3 ( k + 1 ) n - 3 ( k + 1 )( k + 2 ) [1]. In the worst-case scenario, all pairs of edges might cross, so the number of crossings is no more than 9 2 k 2 n 2 + o ( k 2 n 2 ) . In the following theorem we improve this bound.

Theorem 4.2.1. For every point set P , ⊠ ( kGG ( P )) ⩽⊠ ( kDG ( P )) ⩽ ( 3 k 2 + 6 k + 3 ) n 2 + ( - 6 k 3 - 21 k 2 - 51 2 k - 21 2 ) n + ( 3 k 4 + 15 k 3 + 57 2 k 2 + 51 2 k + 9 ).

Proof. If k ⩾ n / 2 - 1 , graph k - DG ( P ) is the complete graph and the bound is trivial. Therefore, it suffices to study the case where k &lt; n / 2 - 1 . Let e be an edge of k - DG ( P ) . Let us see that there are many edges in k - DG ( P ) that do not cross e .

First assume that | Pa | ⩾ k + 2 and | Pb | ⩾ k + 2. Let p 1 , p 2 , . . . , pl denote the points in Pa sorted from top to bottom. If i ∈ [ 2 , k + 2 ] and j ∈ [ 1 , i - 1 ] , then pi is adjacent to p j in k - DG ( P ) . It suffices to consider the circle through pi and p j tangent to the horizontal line containing pi . From all points in P , this circle can only contain { p 1 , p 2 , . . . , pi - 1 } \ { p j } in its interior. Notice that the edges pi p 1 , pi p 2 , . . . , pi p i - 1 do not cross e . If i ∈ [ k + 3 , l ] , we consider the same family of circles. More precisely, we consider a circle tangent to the horizontal line through pi growing until its interior contains k + 1 points from Pa (it could happen that the interior of the circle goes from having k points from Pa to having k + 2 points

For simplicity, let us assume that e is horizontal. The line extending e divides P minus the endpoints of e into two groups. Let Pa and Pb denote the sets of points above and below the line, respectively. We set | Pa | = l . Observe that | Pb | = n - l - 2.


<!-- p:15 -->

Fig. 10. Left: set of points whose k - GG has k 2 n 2 / 4 + o ( k 2 n 2 ) crossings. Right: set of points whose k - DG has k 2 n 2 / 2 + o ( k 2 n 2 ) crossings.

from Pa ; this case is similar). Then in k - DG ( P ) these k + 1 points are connected to pi and all these edges do not cross e . In conclusion, there exist ( k + 1 )( k + 2 )/ 2 + ( l - ( k + 2 ))( k + 1 ) edges between points in Pa not crossing e . By analogous arguments, there exist ( k + 1 )( k + 2 )/ 2 + ( n - l - 2 - ( k + 2 ))( k + 1 ) edges between points in Pb not crossing e . This adds up to a total number of ( k + 1 )( n - k - 4 ) edges.

It remains to settle the case where either Pa &lt; k 2 or Pb &lt; k 2. Let us suppose that Pa &lt; k 2; since k &lt; n / 2 we have that | Pb | ⩾ k + 1. Arguing as in the previous case, we find ( l - 1 ) l / 2 + ( k + 1 )( k + 2 )/ 2 + ( n - l - 2 - ( k + 2 ))( k + 1 edges that do not cross e . It is not difficult to see that, for any l &lt; k 2, this number is always greater than ( k 1 )( n k 4 )

In summary, since k - DG ( P ) contains at most 3 ( k 1 ) n 3 ( k 1 )( k 2 ) edges, e crosses no more than 3 ( k 1 ) n 3 ( k + 1 )( k + 2 ) - 1 - ( k + 1 )( n - k - 4 ) edges in k - DG ( P ) . Hence the number of crossings of k - DG ( P ) 1 2 ( 3 ( k + 1 ) n - 3 ( k + 1 )( k + 2 ))( 3 ( k + 1 ) n - 3 ( k + 1 )( k + 2 ) - 1 - ( k + 1 )( n - k - 4 )) . ✷

| | + | | + | | + - 1, ) + + - - . + - + + + - is upper bounded by

The preceding bounds are tight up to a multiplicative constant.

Proposition 4.2.2. If k = o ( n ), there exists a point set Q such that ⊠ ( kGG ( Q )) = k 2 n 2 / 4 + o ( k 2 n 2 ).

Proof. Refer to Fig. 10(left). The upper chain contains n - k - 1 points on a circle C such that the distance between consecutive points is always the same. Let qi and qi + 1 be two such consecutive points. Let l be the line through qi + 1 perpendicular to - - - - - → qi q i + 1 , and let d be the distance between l and the center of C . The lower chain forms a convex chain seen from the upper chain and contains k + 1 points that are at distance less than d from the center of C . This ensures that the closed disk with diameter formed by qi and some point from the lower chain does not contain any point from the upper chain different from qi . Thus in k - GG ( Q ) each point from the upper group is adjacent to each point from the lower group. These edges create k 2 n 2 / 4 (minus terms of lower order) crossings. Edges between points belonging to the same group cause o ( k 2 n 2 ) crossings and have been omitted in the figure. Notice that the construction can be perturbed to attain general position. ✷

Proposition 4.2.3. If k = o ( n ), there exists a point set Q such that ⊠ ( kDG ( Q )) = k 2 n 2 / 2 + o ( k 2 n 2 ).

Proof. Refer to Fig. 10(right). The number of points in the upper group is k + 1, and the lower group contains the same number of points. The remaining points are placed in the middle group. In k - DG ( Q ) each point qi in the middle group is connected to all upper and lower points, as it suffices to consider families of increasing circles through qi with center at the vertical line through qi . This construction can be perturbed so that it becomes non-degenerate. ✷

For k -relative neighborhood graphs, it can be shown that the number of edges is bounded above by 3 kn + 3 n (see the proof of Theorem 4.2.5), which yields an upper bound of 9 k 2 n 2 + o ( k 2 n 2 ) for the worst crossing number. We have proved that the order of magnitude of this parameter is smaller provided that k = o ( n ) .

Lemma4.2.4. In any angular sector with apex p ∈ P and amplitude α ⩽ π/ 3 , the only points that can be connected to p in the graph kRNG ( P ) are the k + 1 closest points to p that are contained in the sector.

Proof. Let p 1 , p 2 , . . . be the points of P that are contained in the sector sorted by increasing distance to p . For each i ⩾ 2, the points p 1 , p 2 , . . . , pi - 1 are contained in the intersection of the two disks centered at p and pi with radius | ppi | . (See Fig. 11, left.) Consequently, p and pi are not connected in k - RNG ( P ) for i - 1 &gt; k . ✷

Theorem 4.2.5. For every point set P , ⊠ ( kRNG ( P )) ⩽ ( 9 k 2 + 18 k + 9 ) kn .


<!-- p:16 -->

Fig. 11. Left: an angular sector with apex p and amplitude α ⩽ π/ 3. Middle: four points satisfying the hypothesis of Lemma 4.2.7. Right: The region R in Lemma 4.2.8.

Proof. Let e = pi p j be an edge in k - RNG ( P ). We define the lens 2 associated to e as the open intersection of the circles centered at pi and p j with radius | pi p j | .

Now let us define a charging scheme that assigns every crossing in k - RNG ( P ) to each of the two involved edges e satisfying that at least one of the endpoints of the other edge is contained in the lens associated to e . Since each crossing defines a quadrilateral having at least one obtuse angle, the crossing is (at least) assigned to the edge opposite to this angle. Let e be an edge in k - RNG ( P ) . The lens associated to e contains at most k points in P . By Lemma 4.2.4, each of them is adjacent to no more than 3 k + 3 points in P such that the edge that connects them crosses e . Consequently, at most 3 k 2 + 3 k crossings may be assigned to e . Since each vertex in P has degree at most 6 k + 6 (see Lemma 4.2.4), the number of edges of k - RNG ( P ) does not exceed 3 kn + 3 n , which yields the theorem. ✷

Finally, the number of edges of k - NNG is no greater than kn . In this case, Theorem 4.2.9 and Proposition 4.2.10 show that the worst crossing number is also cubic in k and linear in n .

The proof of Theorem 4.2.9 requires several technical lemmas. The first one is a corollary of Lemma 4.2.4.

Corollary 4.2.6. In any angular sector with apex p ∈ P and amplitude α ⩽ π/ 3 , the only points that can be connected to p in the graph kNNG ( P ) are the k closest points to p that are contained in the sector.

Lemma4.2.7. Let pi , p j , pl , and pm be four elements of P , with | pi p j | &lt; | pi p l | &lt; | pi pm | . If p j pm crosses pi p l , then | p j pl | &lt; | p j pm | .

Proof. Let Ci , l and C j , l respectively be the circles centered at pi and p j containing pl in the boundary. (See Fig. 11, middle.) These circles have a non-empty intersection and, since pi , p j , and pl are not aligned, Ci , l is not contained in C j , l , nor C j , l is contained in Ci , l . Let q be the intersection point between Ci , l and the ray starting at p j and passing through pi . We have that | p jq | &gt; | p j pl | . Therefore the ray starting at p j and passing through pi intersects C j , l before Ci , l . This property is maintained for all rays starting at p j and contained in the wedge induced by the angle ̸ pi p j pl . In particular, it is maintained for the ray starting at p j and containing pm . Since pm lies outside Ci , l , pm is not contained in C j , l , so | p j pl | &lt; | p j pm | . ✷

Lemma 4.2.8. Let pi , p j , and pl be three elements of P , with | pi p j | &lt; | pi p l | . Then all points pm such that p j pm crosses pi p l , | pi p l | &lt; | pi pm | , | pmpi | &gt; | pmp j | , and | pmpl | &gt; | pmp j | are contained in an angular sector with apex pi and amplitude at most π/ 3 .

Proof. Without loss of generality, we assume that the line through pi and pl is vertical, pi is above pl , and p j is to the left of this line. The other situations are symmetric.

Let C be the circle centered at pi and containing pl in the boundary. Let l i , j and l j , l be the bisectors of pi p j and p j pl , respectively. A point pm satisfying the hypothesis of the lemma must lie on the intersection R of the following four regions: the exterior of C , the semiplane opposite to pi determined by l i , j , the semiplane opposite to pl determined by l j , l , and the wedge induced by the angle ̸ pi p j pl . (See Fig. 11, right.) If p j has greater or equal ordinate than pi , it is not difficult to see that the region R is empty. Observe that R is also empty if l i , j or l j , l do not intersect the arc of C determined by the wedge induced by ̸ pi p j pl . Therefore the lemma clearly holds in these cases.

Now assume that p j has smaller ordinate than pi , l i , j intersects the arc of C determined by the wedge induced by ̸ pi p j pl in a point q , and l j , l intersects the arc of C determined by the wedge induced by ̸ pi p j pl in a point r . Let t be the intersection of l i , j and l j , l . In order for R not to be empty, t must lie outside C .

Consider the wedge formed by the ray starting at p j and passing through q together with the ray starting from p j and passing through r . Observe that R is contained in this wedge. We will end the proof by showing that this wedge has angle at most π/ 3 . Let t ′ be the intersection of the bisector of pi p l with the arc of C determined by the wedge induced by ̸ pi p j pl .

2 Unfortunately, it is standard in the computational geometry literature that a lens is incorrectly called a lune .


<!-- p:17 -->


Notice that ̸ p j pi q &gt; ̸ p j pi t ′ &gt; ̸ pl pi t ′ . By analogous arguments, ̸ p j pl r &gt; ̸ pi p l t ′ . Since ̸ pl pi t ′ and ̸ pi p l t ′ are angles of the equilateral triangle formed by pi , pl , and t ′ , then ̸ p j pi q and ̸ p j pl r are greater than π/ 3. This implies that ̸ pi p jq and ̸ pl p j r are greater than π/ 3, since ̸ p j pi q = ̸ pi p jq and ̸ pl p j r = ̸ p j pl r . Given that ̸ pi p jq + ̸ qp j r + ̸ rp j pl &lt;π , we conclude that ̸ qp j r &lt;π/ 3. ✷

Theorem 4.2.9. For every point set P , ⊠ ( kNNG ( P )) ⩽ ( 2 k 2 - 3 k + 1 ) kn / 2 .

Proof. Consider two crossing edges in k - NNG ( P ) involving the vertices pi , p j , pl , and pm . We assign the crossing to each of the pairs of edges { - - - → pi p l , - - - → pi p j } satisfying: (i) one of the two crossing edges is - - - → pi p l ; (ii) | pi p j | &lt; | pi p l | (so - - -→ pi p j ∈ E ( k - NNG ( P )) ). Let us show that this assignment is consistent. The quadrilateral defined by the vertices involved in the crossing has at least one obtuse angle. Then the crossing is assigned to the pair of directed edges consisting of the edge opposite to this obtuse angle (which is a diagonal of the quadrilateral) and one edge with the same origin and lying in one side of the quadrilateral.

We devise a charging scheme that divides the weight of each crossing by the number of pairs of edges the crossing is assigned to. We say that a crossing is simple if it is assigned only to one pair of edges, and we say that it is multiple otherwise. In the following we find the maximum weight that a pair of edges of the form { - - - → pi p l , - - -→ pi p j } can receive.

Next we analyze the maximum number of simple crossings that may be assigned to { - - - → pi p l , - - - → pi p j } . Let pm be a vertex in P such that the edge p j pm (with some orientation) causes a crossing assigned to { - - - → pi p l , - - -→ pi p j } . If | pi pm | &lt; | pi p l | , then the crossing is also assigned to { - - - → pi p l , - - - - → pi pm } . If | pi pm | &gt; | pi p l | and - - - - → p j pm ∈ E ( k - NNG ( P )) , then, by Lemma 4.2.7, | p j pl | &lt; | p j pm | and the crossing is also assigned to { - - - - → p j pm , - - - → p j pl } . If | pi pm | &gt; | pi p l | , - - - - → pmp j ∈ E ( k - NNG ( P )) , and | pmp j | &gt; | pmpi | or | pmp j | &gt; | pmpl | , then the crossing is also assigned to { - - - - → pmp j , - - - - → pmpi } or { - - - - → pmp j , -- - → pmpl } . Therefore, there are three necessary conditions for pm to cause a simple crossing assigned to { - - - → pi p l , - - -→ pi p j } : (i) | pi pm | &gt; | pi p l |; (ii) - - - - → pmp j ∈ E ( k - NNG ( P )) ; (iii) | pmpi | &gt; | pmp j | and | pmpl | &gt; | pmp j | . By Lemma 4.2.8 and Corollary 4.2.6, there are at most k such points.

Let p j and pl be two of the k -nearest neighbors of pi , with | pi p j | &lt; | pi p l | . Each crossing assigned to { - - - → pi p l , - - -→ pi p j } can be associated with a vertex adjacent to p j in k - NNG ( P ) (the fourth point involved in the crossing). We want to bound the maximum number of such vertices. Let ˆ w be the wedge induced by ̸ pi p j pl . If ˆ w has amplitude at most 2 π/ 3, then, by Corollary 4.2.6, the maximum number of crossings that may be assigned to { - - - → pi p l , - - -→ pi p j } is 2 k . Otherwise, we partition ˆ w into three wedges ˆ w 1, ˆ w 2, and ˆ w 3 as follows: ˆ w 1 is bounded by the half-line with origin at p j and direction given by - - -→ p j pi and has amplitude π/ 3; ˆ w 3 is bounded by the half-line with origin at p j and direction given by - - - → p j pl and has amplitude π/ 3; ˆ w 2 consists of the part of ˆ w not covered by ˆ w 1 and ˆ w 3. For ν ∈ { 1 , 2 , 3 } , let n ν be the number of vertices in ˆ w ν that create a crossing assigned to { - - - → pi p l , - - -→ pi p j } . A direct application of Corollary 4.2.6 yields that n ν ⩽ k for ν ∈ { 1 , 2 , 3 } . Furthermore, since pi is a point in ˆ w 1 adjacent to p j , we have that n 1 ⩽ k - 1 . Finally, consider the k closest points to p j contained in ˆ w 3, which, by Corollary 4.2.6, are the only candidates to be connected to p j in k - NNG ( P ) . Observe that pl belongs to this set: otherwise, by Lemma 4.2.7, there would be k points pm such that | pi p l | &gt; | pi pm | , which is absurd because - - - → pi p l ∈ E ( k - NNG ( P )) . Thus n 3 ⩽ k - 1 . In conclusion, the maximum number of crossings that may be assigned to { - - - → pi p l , - - -→ pi p j } is 3 k - 2 .

To conclude, in the worst-case scenario k simple crossings and 2 k - 2 crossings of weight 1 / 2 are assigned to { - - - → pi p l , - - - → pi p j } . Thus any pair of edges in k - NNG ( P ) of the form { - - - → pi p l , - - -→ pi p j } receives weight at most 2 k - 1 . To complete the proof of the theorem it suffices to notice that there are n ( k 2 ) such pairs of edges. ✷

In the following proposition, we describe a point configuration whose k - RNG and k - NNG contain Θ( k 3 n ) crossings.

Proposition 4.2.10. If k = o ( n ), there exists a point set Q such that ⊠ ( kRNG ( Q )) ⩾⊠ ( kNNG ( Q )) = k 3 n / 3 + o ( k 3 n ).

Proof. Consider the set Q ={ q 1 , q 2 , . . . , qn } , where qi = ( 2 i , 0 ) . Let us slightly perturb the configuration so that the points are in convex position. The k -nearest neighbors of each point qi such that i &gt; k are qi - 1 , qi - 2 , . . . , qi - k . Therefore, if i ∈ [ k + 1 , n - k ] , then qi is connected in k - NNG ( Q ) to its k predecessors and k successors in the 'line'.

Let -- → qi q j and - - - → ql qm be two crossing edges such that j &lt; m &lt; i &lt; l . We assign this crossing to q j . Suppose that j ∈ [ k + 1 , n - k ] . Then the crossings between -- → qi q j and the following edges are assigned to q j : -- - - - - - → q j + 1 q j - 1 , -- - - - - - → q j + 2 q j - 1 , . . . , - - - - - - - - - - → q j + k - 1 q j - 1 , -- - - - - - → q j + 1 q j - 2 , -- - - - - - → q j + 2 q j - 2 , . . . , - - - - - - - - - - → q j + k - 2 q j - 2 , . . . , - - - - - - -→ q j + 1 qi + 1 , - - - - - - -→ q j + 2 qi + 1 , . . . , - - - - - - - - -→ qi + k + 1 qi + 1 . This adds up to ∑ k - 1 ν = i + k + 1 - j ν crossings. Since i might take values from j - k to j - 2, the total number of crossings assigned to q j is

$$\sum _ { i = j - k } ^ { j - 2 } \sum _ { \nu = i + k + 1 - j } ^ { k - 1 } \nu & = \sum _ { \nu = 1 } ^ { k - 1 } \nu ^ { 2 } = \frac { k ^ { 3 } } { 3 } - \frac { k ^ { 2 } } { 2 } + \frac { k } { 6 } . \\ \text {Given that } i \text { is an index in } [ k + 1 , n - k ] \text {, the preceding}$$

Remark4.2.11. For constant values of k , we have found a slightly better construction giving ⊠ ( k - NNG ( Q )) ⩾ ( 2 k 2 - k - 1 ) kn / 6 + Θ( 1 ). The details will be given in [25].

Given that j is an index in [ k + 1 , n - k ] , the preceding charging scheme guarantees that k - NNG ( Q ) contains ( n - 2 k ) × ( k 3 / 3 - k 2 / 2 + k / 6 ) crossings. Notice that the crossings we have not considered in this argument have order o ( k 3 n ) . ✷


<!-- p:18 -->


### Acknowledgements

We would like to thank the referees for many helpful suggestions.
