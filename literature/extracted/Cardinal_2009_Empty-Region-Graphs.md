---
id: "Cardinal_2009_Empty-Region-Graphs"
source_pdf: "../pdf/Cardinal_2009_Empty-Region-Graphs.pdf"
source_filename: "Cardinal_2009_Empty-Region-Graphs.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "excellent"
extraction_score: 100.0
visual_assets: "disabled"
references_file: "../references/Cardinal_2009_Empty-Region-Graphs.references.md"
---

<!-- p:1 -->

## Empty region graphs

### Jean Cardinal ∗ , Sébastien Collette 1 , Stefan Langerman 2

Computer Science Department, Université Libre de Bruxelles, CP 212, Boulevard du Triomphe, 1050 Bruxelles, Belgium

###### a r t i c l e i n f o

###### a b s t r a c t

Article history: Received 24 June 2006 Received in revised form 3 September 2008 Accepted 7 September 2008 Available online 2 October 2008 Communicated by G. Toussaint

Keywords: Geometric graphs Proximity graphs Graph properties

### 1. Introduction

We consider here proximity graphs [15], also called neighborhood graphs . These graphs are defined on a finite set V of vertices in the plane and there exists an edge between any two vertices if they are close in some sense. The proximity can be measured for instance by the Euclidean distance between these vertices, the distance to other vertices of the graph, or the number of other vertices in a given neighborhood. These graphs are well studied; a survey of Jaromczyk and Toussaint [15] discusses many of them, such as Relative Neighborhood Graphs [1,15], Gabriel Graphs [12], β -Skeletons [17], Rectangular Influence Graphs [14]. Θ -Graphs [16,22], γ -Neighborhood Graphs [20] and Empty-Ellipse Graphs [7] are other examples. These graphs are commonly used for instance in geographic analysis [13] and pattern classification [8].

Previous work on proximity graphs traditionally consisted in the introduction of one or more graph families, followed by different contributions analyzing their properties and applications. For instance, in [19] the properties of the Gabriel Graphs were used to analyze geographical data sets; in [2] authors analyze the spanning ratio of some proximity graphs. Surprisingly, the natural opposite approach does not seem to have been considered: to try to find a practical method which, given a set of desired graph properties, returns a corresponding proximity graph family. For this, we have to define a class of proximity graphs general enough to encompass many useful graphs, but simple enough to be analyzed.

* Corresponding author.

E-mail addresses:

jcardin@ulb.ac.be (J. Cardinal), sebastien.collette@ulb.ac.be (S. Collette), stefan.langerman@ulb.ac.be (S. Langerman).

1 Chargé de Recherches du F.R.S.-FNRS.

2

Chercheur Qualifié du F.R.S.-FNRS.

A family of proximity graphs, called Empty Region Graphs (ERG) is presented. The vertices of an ERG are points in the plane, and two points are connected if their neighborhood, defined by a region, does not contain any other point. The region defining the neighborhood of two points is a parameter of the graph. This way of defining graphs is not new, and ERGs include several known proximity graphs such as Nearest Neighbor Graphs, β -Skeletons or Θ -Graphs. The main contribution is to provide insight and connections between the definition of ERG and the properties of the corresponding graphs.

We give conditions on the region defining an ERG to ensure a number of properties that might be desirable in applications, such as planarity, connectivity, triangle-freeness, cyclefreeness, bipartiteness and bounded degree. These conditions take the form of what we call tight regions : maximal or minimal regions that a region must contain or be contained in to make the graph satisfy a given property. We show that every monotone property has at least one corresponding tight region; we discuss possibilities and limitations of this general model for constructing a graph from a point set.

© 2008 Elsevier B.V. All rights reserved.

Contents lists available at ScienceDirect

## Computational Geometry: Theory and Applications

www.elsevier.com/locate/comgeo We define the ERG as the general class of proximity graphs using the following definition of proximity: two vertices are close, and thus form an edge, if and only if some neighborhood around them is empty. The region corresponding to the neighborhood is a parameter defining the exact family of graphs in the class.

<!-- p:2 -->


One motivation of our work was to design proximity graphs that are invariant under translations, rotations and uniform scaling. It can be shown that this property is satisfied if and only if the region defining the neighborhood around two points is obtained by translating, rotating and uniformly scaling a template region. We further focus on convex and symmetric regions, hence on undirected proximity graphs.

The properties of these graphs are determined by the choice of the template region. More specifically, we say that a given template region satisfies a property when for all point sets V the graph generated using that region satisfies the property. Graph properties that are monotone with respect to either edge deletion or insertion are good candidates for investigation, as monotone properties that are satisfied by a template region are satisfied by all template regions included in it in the case of edge insertion, or containing it in the case of edge deletion.

This naturally raises the issue of template regions that are extremal with respect to the inclusion partial order among regions. We show for instance that the lune, defined as the intersection of two disks of radius d2 ( p , q ) and respective centers p and q , is the unique maximal region ensuring the connectivity of the graph. We call these extremal regions tight regions . However, because the inclusion relation is not a total order, tight regions need not be unique. Tight regions can somehow be seen as a deterministic geometric analogue to thresholds for monotone properties studied in random graph theory [11]. We prove that these regions are defined for every monotone graph property.

The main contribution of this work is to provide a generalized approach to the problem of defining proximity graphs based on required properties. Also, even though some results were previously known, the analysis of the uniqueness of the template regions had never been considered before. And this strengthens the characterization: not only can we find a template region corresponding to a given list of properties, but we can also, given any template region, tell if some properties are guaranteed.

#### 1.1. Related works

The study of graph-theoretic and combinatorial properties of proximity graphs is not new. Numerous references [1,6,12, 14,15,17] present extensive analyses of what properties can be satisfied with which proximity graph.

Restricted families of template regions have also been studied before. The β -Skeletons are constructed using a template region based on a family of regions depending on a parameter β , and they were extensively analyzed in that context [17]: given a value of β , we know directly if the graph is guaranteed to be connected, planar, acyclic, etc. and we can thus use that approach to achieve our primary goal: determine the proximity relation satisfying a property for every set of points. But the class of regions considered is very restrictive in β -Skeletons, as it is always the intersection of two disks, while we propose an approach for every convex and symmetric region.

Theorems 11, 17 and 23 of this work are extensions of the work on β -Skeletons, where we consider the uniqueness and the tightness of the template region among all convex symmetric regions.

Numerous papers studied drawability problems for proximity graphs. For instance, Bose et al. [3,4] studied extensively the following graph drawing question: given a tree T , does there exist a set of points in the plane such that a proximity graph induced by these points is isomorphic to T . They were able to provide a complete characterization for trees if the proximity graph is a Relative Neighborhood Graph, Relatively Closest Graph or a Gabriel Graph, they also propose a partial characterization for β -Skeletons. Lubiw and Sleumer [18] showed that every maximal outerplanar graph can be represented as a Gabriel Graph and a Relative Neighborhood Graph; they described what geometric properties must be satisfied to layout a set of vertices such that the corresponding proximity graph is maximal outerplanar.

Other related drawability problems were surveyed in [9]. These studies are similar but fundamentally different from what is done here: we work on a fixed set of vertices in the plane while these papers propose a way to layout the vertices of a given graph G so that it is a proximity graph according to some proximity definition.

#### 1.2. Plan

In Section 2, we define ERGs, and show how known proximity graphs such as Nearest Neighbor Graphs, β -Skeletons and Θ -Graphs can be defined as ERGs. We then prove several facts, including that every monotone graph property has at least one tight region, and how to combine tight regions for conjunction of properties.

Section 3 is about geometric properties, which depend on the position of the vertices. We give the unique tight region guaranteeing that the current embedding is planar and prove that no ERG invariant under translation, rotation and uniform scaling can guarantee a constant spanning ratio. This is interesting in light of known bounds on the spanning ratio of Θ -Graphs [16], which are not rotation invariant.

In Section 4 we study the property of not having a given graph as subgraph, and how sets of tight regions can be constructed for forbidden combinations of subgraphs. Then we specifically consider the properties of not having a k -star or a k -cycle as subgraph.


<!-- p:3 -->


Section 5 presents tightness results for planarity, cycle-freeness, connectivity and bipartiteness. We end in Section 6 with a discussion on the limitations of our model and on the class of properties which can be ensured by the choice of a template region.

### 2. Empty region graphs

In this section, we define ERGs and prove some basic results. We give examples of well-known graph families that can be described in terms of empty neighborhoods, and are thus ERGs. We present some typical ERG template regions that we will use in this paper, and we give restrictions on the family of regions that we consider.

#### 2.1. Definitions

Definition 1. A template region R is a function mapping a pair ( p , q ) of points in R 2 to a subset of R 2 .

Definition 2. An anchored region R is a template region parameterized by a triple ( a , b , D ) , where a and b are points in R 2 and D is a subset of R 2 . The set R ( p , q ) is the subset of R 2 obtained by translating, rotating and uniformly scaling D so that a maps to p and b maps to q .

Definition 3. An Empty Region Graph ERGR ( V ) = ( V , E ) parameterized by a template region R is a graph where V is a finite subset of R 2 and

$$\forall p , q \in V \colon \ p q \in E \ \Leftrightarrow \ R ( p , q ) \cap S \ \{ p , q \} = \emptyset .$$

If the template region is not symmetric, then the graph is defined as a directed graph, and as an undirected graph otherwise.

#### 2.2. Examples

The following well-studied graph families are enclosed in our definition of ERG. If β -Skeletons are directly defined as graphs with some empty region, the original definitions of Nearest Neighbor Graphs and Θ -Graphs are not based on an empty region.

##### Nearest Neighbor Graphs

These are directed graphs where each vertex is connected to its nearest neighbor with respect to the Euclidean distance [10]. They can be equivalently defined as ERGs for the anchored region R where R ( p , q ) is the disk of center p and radius the length of the line segment pq . In that case, the region used does not yield a symmetric distance.

##### β -Skeletons

In what follows, d2 ( u , v ) is the Euclidean distance. This is another example of ERG in which the vertices are close if their template region I β ( p , q ) does not contain any other point, with I β ( p , q ) defined as follows:

- For β = 0, I β ( p , q ) is the line segment pq .
- For 1 ⩽ β &lt; ∞ , I β ( p , q ) is the intersection of the two disks of radius β d2 ( p , q )/ 2 and centered at the points ( 1 - β/ 2 ) p + (β/ 2 ) q and (β/ 2 ) p + ( 1 - β/ 2 ) q , respectively.
- For 0 &lt;β &lt; 1, I β ( p , q ) is the intersection of the two disks of radius d2 ( p , q )/( 2 β) passing through both p and q , where d2 is the Euclidean distance.
- For β =∞ , I β ( p , q ) is the infinite strip perpendicular to the line segment from p to p .

An open β -Skeleton uses an open template region, which does not contain its outer limit. A closed β -Skeleton uses a closed template region. A Gabriel Graph is a closed 1-Skeleton; a Relative Neighborhood Graph is an open 2-Skeleton. Every open β -Skeleton with β ⩽ 2 and every closed β -skeleton with β &lt; 2 is connected.

##### Θ -Graphs

Introduced by Yao [22] and Keil [16], they are another example of ERG. A Θ -Graph is a directed graph defined by a point set V in which each vertex has up to k outgoing edges connected to the closest vertex in k different cones. The i th cone associated to a vertex p in a Θ -Graph is the subspace containing all the points with absolute angle from p between i Θ included and ( i + 1 )Θ excluded. There are k = 2 π/Θ cones for each vertex. In each cone i of the vertex p , the outgoing edge is connected to the closest vertex, denoted by pi . This corresponds to an ERG, using the region which is the intersection of the disk of radius pq centered at p , and the cone of apex p containing q . Note that this is a template region, but not an anchored template region because it is not invariant under rotation.


<!-- p:4 -->


#### 2.3. Assumptions

In what follows, we restrict ourselves to using anchored regions parameterized by triples ( a , b , D ) where D is convex and symmetric with respect to the line supporting ab , and with a and b contained in D . The region is closed if not specified otherwise. Using only anchored regions is necessary and sufficient to guarantee the invariance of the graph structure under translation, rotation and uniform scaling of the set of points. We further restrict ourselves to symmetric regions with respect to the center ( a + b )/ 2, hence undirected graphs.

Note that the restriction to convex and symmetric regions was added to simplify the model, and will be used in most proofs. Of course, a natural extension of this work is to lift this assumption. Also, in the remainder of this paper, when we claim that a region is unique, or extremal, it means that it is the unique convex and symmetric region satisfying the property, or the extremal convex and symmetric region.

The regions presented on Fig. 1 will be used later. The pacman, or double pie-wedge, P Θ( p , q ) is bounded by the convex hull of two pie-wedges of angle Θ , with apex in p and in q facing each other, such that P 0 ( p , q ) is the segment pq . The lune L ( p , q ) is defined as P 2 π/ 3 ( p , q ) , while the mastercard M ( p , q ) is P 2 π ( p , q ) . The slab S ( p , q ) is the infinite strip perpendicular to the line segment pq with p and q on the boundary. The truncated slab S 5 ( p , q ) is the convex shape containing two lunes on top of each other separated by a distance 2d2 ( p , q ) .

#### 2.4. Properties

Definition 4. A graph property P on a family of graphs G is a set P ⊆ G . A graph G ∈ G has property P if G ∈ P .

Definition 5. A graph property P is monotone with respect to edge insertion (or to edge deletion , respectively) if and only if ∀ G = ( V , E ), G ′ = ( V , E ′ ), E ⊆ E ′ (or E ⊇ E ′ , respectively): G ∈ P ⇒ G ′ ∈ P .

Our definition of monotonicity is slightly different from the one commonly used in graph theory. Usually, this is stated as follows: a property is monotone if and only if it is closed upon taking subgraphs. We add the symmetric definition with properties monotone upon taking supergraphs.

Definition 6. An anchored region R satisfies a graph property P if and only if for all V ⊂ R 2 finite, ERGR ( V ) ∈ P .

Definition 7. A convex and symmetric anchored region R is tight for a graph property P monotone with respect to edge insertion (or to edge deletion, respectively) if and only if R satisfies P and none of the convex and symmetric anchored region R ′ ⊃ R (or R ′ ⊂ R , respectively), R ′ satisfies P .

Note that the monotonicity of the property with respect to edge deletion implies that any region containing a tight region as subset satisfies the property as well. On the other hand, for regions that are strictly contained in a tight region, one can always find a set of points generating a graph that does not have the property. A similar observation holds the other way round for properties that are monotone with respect to edge insertion.

Fig. 1. Examples of regions.

<!-- p:5 -->


Another definition of a tight region for a monotone property is a convex and symmetric region that satisfies the property and is extremal with respect to the inclusion partial order among the considered type of regions. We now show that tight regions always exist.

Lemma 8. For every graph property P monotone with respect to edge deletion ( or to edge insertion, respectively ) and region R satisfying P , either R is tight, or there exists at least one region R ′ ⊂ R ( or R ′ ⊃ R, respectively ) which is tight.

Proof. We first consider properties monotone with respect to edge deletion. Let R be an anchored, convex and symmetric region satisfying the property P , and C be the set of anchored, convex and symmetric regions { R ′ ⊆ R | R ′ satisfies P } .

A chain in that partially ordered set, with the relation of inclusion, is a sequence { R 0 , R 1 , . . . } such that for all i , Ri ⊇ Ri + 1 . The lower bound of that sequence is

which by definition is also convex and symmetric.

We first show that every chain in C has a lower bound in C . The proof is obtained by contradiction. Let R be a region in C and { R = R 0 , R 1 , . . . } any chain in C beginning with R . We assume that R ∞ does not belong to C and derive a contradiction. If R ∞ does not belong to C , it implies that it does not satisfy P . Thus there exists a set of vertices V such that ( V ) / .

ERGR ∞ ∈ P

∞ As R ∞ does not satisfy the property, while it was the case for every item in the chain, the problem has to come from an edge present in ERGR ∞ ( V ) but not in ERGRi ( V ) for any i .

Let ni be the size (number of edges) of the graph ERGRi ( V ) . We have n 0 ⩽ n 1 ⩽ · · · &lt; n ∞ . The last relation is strict, because otherwise there is a k such that ERGRk ( V ) = ERGR ( V ) and thus Rk does not satisfy P while it is in the chain.

Then, there exist three points p , q and r in V such that for all i , r ∈ Ri ( p , q ) and r / ∈ R ∞ ( p , q ) . But as R ∞ is the intersection of Ri for all i , r is in R ∞ ( p , q ) . This proves that R ∞ satisfies P and is thus in C .

For properties monotone with respect to edge insertion, the same reasoning applies. We consider upper bounds in chains and maximums regions. We can apply Zorn's Lemma to show that { . . . , R - 1 , R 0 = R } has always an upper bound in the set. The upper bound is R -∞ = ⋃ i R - i , which is convex and symmetric. ✷

By applying Zorn's Lemma [5] to that set, we know that if every chain in C has a lower bound in the set, then there is at least one minimal region R ′ in C satisfying a property contained in any region R . A region R ′ is minimal with respect to C if and only if no strict subset of R ′ is in C . Thus R ′ ⊆ R is a tight region for P .

Knowing tight regions for useful properties is important in practice, because it allows to check quickly if the properties we wish to obtain are satisfied or not. The uniqueness of a tight region is even more important, because knowing a single tight region R does not, in general, give any information on the properties guaranteed by regions that simultaneously do not contain R and are not contained in R . If the tight region R is unique, any region that does not contain R does not satisfy the property, even if it is not strictly included in R .

Lemma 9. Let P be a monotone property with respect to edge deletion and R be the unique tight region satisfying that property. No region R ′ ̸⊇ R satisfies P .

Proof. By contradiction, suppose that R ′ satisfies P . By Lemma 8 either R ′ is tight, which is impossible as R is the unique tight region, or there exists a tight region R ′′ ⊂ R ′ which satisfies the property. In that case, we know that R ′′ ̸⊂ R , because otherwise R would not be tight. Thus, R ′′ and R are two tight regions, contradicting the uniqueness of R . ✷

The same lemma holds for edge insertion, where every region R ′ ̸⊆ R does not satisfy P . Now, given a set of regions corresponding to different properties which are monotone with respect to edge deletion, any region strictly containing the union of the regions of the set will satisfy the whole set of properties. In the case of convex and symmetric regions and properties that are monotone with respect to edge deletion, this is achieved by taking the convex hull of the union of the tight regions for each property. In some cases, this region can be proved to be extremal with respect to the inclusion partial order among the considered type of regions.

Lemma 10. Let P and P ′ be two monotone properties with respect to edge deletion, and R and R ′ two regions satisfying P and P ′ , respectively. Then the convex hull of R ∪ R ′ satisfies P ∩ P ′ . Furthermore, if R and R ′ are the unique tight regions for P and P ′ , then the convex hull of R ∪ R ′ is tight and unique for P ∩ P ′ .

Proof. The first statement directly follows from the definition. If R and R ′ are the unique tight regions, then from Lemma 9 any subset of R ∪ R ′ fails to satisfy either P or P ′ . Hence R ∪ R ′ is tight for P ∩ P ′ .


<!-- p:6 -->


For each other convex region R ′′ , such that R ′′ ⊇ R and R ′′ ⊇ R ′ , we know that R ′′ contains the convex hull of R ∪ R ′ . If R ′′ does not contain the convex hull of R ∪ R ′ , either R ′′ ̸⊇ R and R ′′ does not satisfy P , or R ′′ ̸⊇ R ′ and R ′′ does not satisfy P ′ , and thus R ′′ does not satisfy P ∩ P ′ . This shows that R is unique. ✷

A similar lemma holds for properties that are monotone with respect to edge insertion as well, where regions are composed by taking their intersection.

Compatible properties are properties which can be guaranteed at the same time. We distinguish between properties which are always incompatible, such as connected and not connected , and properties which cannot be guaranteed at the same time while using ERGs. All pairs of monotone properties with respect to edge insertion are compatible. Similarly, all pairs of monotone properties with respect to edge deletion are compatible. At the end of this paper, we discuss the compatibility issues between one property monotone with respect to edge insertion and one property monotone with respect to edge deletion.

### 3. Geometric properties

Here we consider geometric properties, i.e., properties depending on the position of the vertices.

#### Planar embedding

The following theorem shows that the graph embedding obtained by drawing edges as straight line segments is planar if and only if the region contains the ball of diameter pq . It strengthens a result of [6], as it introduces the uniqueness of the tight region.

Theorem 11. The closed ball B is the unique tight region ensuring a planar embedding.

Proof. We first note that the ball B ensures a planar embedding, as the graph is a subset of the Delaunay graph, which is planar. This will thus also be true for any region R ( p , q ) which contains the ball B ( p , q ) , as the graph will be a subset of the one obtained with B .

To prove that B ( p , q ) is tight, we will show that if any point on the boundary of B ( p , q ) is not contained in a region R ( p , q ) , then R ( p , q ) does not satisfy the property. This also proves uniqueness, as any other tight convex region which contains all points of the boundary of B ( p , q ) is strictly larger than B ( p , q ) and thus not tight.

The proof is by contradiction: let a be a point on the circle of diameter d2 ( p , q ) that is not in R ( p , q ) . By the symmetry of center ( p + q )/ 2, we know that there exists a point b which is also not in R ( p , q ) . Using the set { p , q , a , b } , we consider the ERG generated by R ( p , q ) : there is an edge between p and q as R ( p , q ) does not contain any other point. There is also an edge between a and b as R ( a , b ) does not contain p and q by symmetry. Thus, crossing edges exist and the embedding of the graph is not planar. ✷

#### Spanning ratio

In the following, d G ( P ) is the length of a path P = { u 1 , u 2 , . . . , uk } in the graph G : d G ( P ) = ∑ k - 1 i = 1 d2 ( ui , ui + 1 ) . The distance in the graph G between any pair u , v , noted by d G ( u , v ) is the minimal length among all paths between u and v .

Definition 12. A graph G in the plane is a t-spanner for t ∈ [ 1 , ∞ ) , if and only if ∀ u , v ∈ V : d G ( u , v )/ d2 ( u , v ) ⩽ t . The minimum such t is called the spanning ratio of G .

The spanning ratio is also called the dilation. We say that the spanning ratio is unbounded whenever it cannot be bounded by a constant independent of n , i.e., it can be made arbitrarily large for sufficiently large n .

Theorem 13. For each anchored region R with non-empty interior, there exists a real number α &gt; 0 such that for all n, there exists a set V ⊂ R 2 , with | V | = n, so that the spanning ratio of ERGR ( V ) is Omega1 ( n α ) .

Proof. Let us consider a convex and symmetric region R ( p , q ) with non-empty interior. Any such region contains a point r that is not on the segment pq . Every R ( p , q ) contains a triangle with the points p , q and r as vertices. Symmetrically, a triangle pqr ′ is also contained in R ( p , q ) , where r ′ is a point symmetric to r with respect to the line pq .

By definition of the β -Skeleton, for 0 &lt;β &lt; 1, I β ( p , q ) is the intersection of the two disks of radius d2 ( p , q )/( 2 β) passing through both p and q . The value of β can be chosen such that the intersection of the discs is contained in the union of the two triangles. Thus R ( p , q ) ⊇ I β ( p , q ) and ERGR ( V ) is a subgraph of the β -Skeleton of V .

It has been shown in [2,21] that the spanning ratio of every β -Skeleton with β &gt; 0 is Omega1 ( n α ) , with n the number of vertices in the graph and α a function of β . ✷

When we introduced ERGs, one of our motivations was to find a class of rotation-invariant proximity graphs that would produce t -spanners for any t &gt; 1. The well-known Θ -Graph, which is not invariant to rotations, exhibits a constant spanning ratio. The theorem above shows that it is not possible to find any convex and symmetric anchored region other than the segment or the empty region that yields ERGs with a constant spanning ratio.


<!-- p:7 -->


Fig. 2.

### 4. Forbidden subgraphs

A property P defined by a forbidden subgraph F is a set of graphs not having any subgraph isomorphic to F . Such a property P is monotone with respect to edge deletions. We denote by F ⊆ F ′ the fact that F ′ has a subgraph isomorphic to F . The union F ∪ F ′ of two graphs F = ( V , E ) and F ′ = ( V ′ , E ′ ) with V ∩ V ′ =∅ is ( V ∪ V ′ , E ∪ E ′ ) .

Lemma 14. If the region R is tight for a forbidden subgraph F and for a forbidden subgraph F ′ ⊇ F, then it is tight for all forbidden subgraphs G with F ⊆ G ⊆ F ′ .

Proof. The region R forbids G , as its subgraph F is forbidden by R . Suppose that R is not tight. Then by Lemma 8 there exists a region R ′ ⊂ R forbidding G . As G is a subgraph of F ′ , R ′ forbids F ′ , leading to a contradiction as this means that R is not tight for forbidding F ′ . ✷

Theorem 15. If R is the set of tight regions for a forbidden subgraph F and if R ′ is the set of tight regions for a forbidden subgraph F ′ , then the set of tight regions for the forbidden subgraph F ∪ F ′ is { R ∈ R ∪ R ′ | ∀ R ′ ̸= R ∈ R ∪ R ′ : R ̸⊇ R ′ } .

Proof. We know that every region R in the set defined by the theorem satisfies the property, as it forbids either F or F ′ , which ensures that F ∪ F ′ is forbidden. To derive a contradiction, we assume without loss of generality that some R ∈ R which belongs to the set is not tight for forbidding F ∪ F ′ , the case with R ∈ R ′ not tight being symmetric.

So R ′ does not forbid F nor F ′ , and there exists two sets of points V and V ′ such that ERGR ′ ( V ) ⊇ F and ERGR ′ ( V ′ ) ⊇ F ′ . Now we consider the union C of the regions R ′ ( p , q ) for all pairs ( p , q ) in V . If R ′ is bounded, then R 2 \ C is not empty, and has compact subsets of arbitrary large surfaces. If rotated and placed far enough, the other set V ′ of points can be embedded in such a subset, yielding a subgraph of the form F ∪ F ′ , contradicting the fact that R ′ forbids F ∪ F ′ . If R ′ is not bounded and different than the whole plane, then it can be either a horizontal or a vertical slab. In both cases, the conclusion holds, for a union of a finite number of slabs always leaves uncovered angles.

By Lemma 8, if R is not tight, it implies that there exists a region R ′ ⊂ R forbidding F ∪ F ′ . We first note that R ′ does not forbid F since R is tight for forbidding F . We also know that R ′ does not forbid F ′ otherwise there would be a tight region R ′′ contained in R ′ forbidding F ′ . In that case, since R ′′ ⊆ R ′ ⊂ R , R would not have been taken in the set of regions for forbidding F ∪ F ′ .

To prove that the list is complete, we can use the same contradiction. The existence of a tight region for forbidding F ∪ F ′ that would not forbid F nor F ′ allows a similar construction. ✷

#### k-Star

Theorem 16. The closed pacman P 4 π/ k is a tight region forbidding a k-Star, for all k ⩾ 2 .

Proof. We show by construction that if we take any convex and symmetric region R smaller and included in the pacman P 4 π/ k , then we can construct a set V such that ERGR ( V ) contains a k -Star.

Let R ( p , q 1 ) be a region contained in P 4 π/ k ( p , q 1 ) as shown on Fig. 2. We place a point q 2 on the boundary of P 4 π/ k ( p , q 1 ) and out of R ( p , q 1 ) . Note that the angle ̸ q 1 pq 2 is less than 2 π/ k , say 2 π/ k - δ .

Every edge pqi is present in the proximity graph, because the points were placed such that the template region R ( p , qi ) is empty for every i ; thus we have a k -Star.

Now, we add the points q 3 , q 4 , . . . , qk with d2 ( p , qi ) = d2 ( p , q 1 ) , such that the angle ̸ qi pqi + 1 is equal to 2 π/ k + δ/ k for all 1 &lt; i ⩽ k . Thus q 1 / ∈ R ( p , qi ) for all 1 &lt; i &lt; k .

Now we must prove that if R ( p , q ) contains P 4 π/ k ( p , q ) the graph does not contain a k -Star. We can use a simple argument: we consider two consecutive edges pqi and pqi + 1 . The angle ̸ qi pqi + 1 is greater than 2 π/ k , otherwise either qi is in P 4 π/ k ( p , qi + 1 ) or qi + 1 is in P 4 π/ k ( p , qi ) . Thus there are less than k edges. ✷

<!-- p:8 -->


#### k-Cycle

The regions corresponding to forbidding a k -cycle depend on the parameter k . The tight regions for forbidding 3-cycles (also called triangle freeness) and 4-cycles are unique, while there are at least two regions for k = 5.

Theorem 17. The closed lune L is the unique tight region for triangle freeness.

Proof. For every three vertices p , q and r of an ERGR we consider the longest edge of any triangle in the graph. Suppose it is the edge pq , the other cases being symmetric. If R ( p , q ) contains the lune L ( p , q ) , this edge does not appear because L ( p , q ) contains r , as the lune is the locus of the points at a distance less than or equal to d2 ( p , q ) from p and from q . This proves that the lune ensures triangle freeness.

Now, to prove that it is tight and unique we show that if a point of L ( p , q ) is not in R ( p , q ) , there exists a point set which leads to a graph containing a triangle.

Fig. 3 shows how to construct such a set: let r ∈ L ( p , q ) \ R ( p , q ) be a point on the boundary of the lune. We show that pqr is a triangle in the graph if the point set is { p , q , r } .

The edge pq exists, because r is not in R ( p , q ) . The edge pr exists, because the lengths of pr and pq are equal and the region is symmetric. To prove that p is not in R ( q , r ) , we consider the lowest point t on the bisector of pq such that r is in the triangle pqt (see Fig. 3). Note that this point t cannot be in R ( p , q ) , otherwise r would also be in R ( p , q ) . By construction, the triangles ptq and qpr are similar. Hence p is not in R ( q , r ) and the edge qr exists.

This also proves the uniqueness of the lune, as any point of the boundary of L ( p , q ) has to be in R ( p , q ) , meaning that any region R satisfying the property contains L . ✷

Theorem 18. The closed pacman P π is the unique tight region forbidding a 4 -cycle.

Proof. Let p , q , r , s be the four vertices of a 4-cycle, with pq the longest edge. Either the angle ̸ pqr is smaller or equal to π/ 2, or the angle ̸ spq is smaller or equal to π/ 2. As pq is the longest edge, r or s is in P π ( p , q ) , and thus that edge of the cycle is not present.

For each other region R ( p , q ) ̸⊇ P π ( p , q ) , we can create a 4-cycle: as we consider convex and symmetric regions, we know that if P π ( p , q ) \ R ( p , q ) is not empty, then we can place 4 points on the vertices of a square, such that every edge of a 4-cycle will be present.

- [ ] This also proves the uniqueness of the pacman, as we showed that any incomparable region leads to a 4-cycle. ✷

Theorem 19. The closed P 6 π/ 5 is tight for forbidding 5 -cycles.

Proof. In every 5-cycle, there is at least one angle which is not greater than 3 π/ 5 (see Fig. 4). Let us say that it is the angle ̸ pqr , with pq at least as long as qr (the other case being symmetric). As ̸ pqr is at most 3 π/ 5, r is in P 6 π/ 5 ( p , q ) , and the 5-cycle is not present. For every convex and symmetric region R ( p , q ) ⊂ P 6 π/ 5, there exists a set of points corresponding to a 5-cycle. This can be obtained as follows: as R is convex and symmetric, and R ( p , q ) is strictly contained in P 6 π/ 5, we place, given a pair of points p and q , a point r at distance d2 ( p , q ) of q , out of R ( p , q ) and on the outer limit of P 6 π/ 5 (see Fig. 4). We place t at distance d2 ( p , q ) from p , in the corresponding missing region. We have ̸ pqr = ̸ tpq = 3 π/ 5 - α . We add a point s such that ̸ rst is 3 π/ 5 - α , and that rs and st have the same length. This ensures that the edges rs and st are present. By construction, s is not in R ( t , p ) nor in R ( q , r ) , and thus the edges st and qr are present. ✷

Fig. 3. Construction leading to a triangle in the graph.

<!-- p:9 -->


Fig. 4.

Fig. 5.

Fig. 6.

Lemma 20. The truncated slab S 5 satisfies 5 -cycle freeness.

Proof. Let us consider the largest edge of a 5-cycle, pq , and the slab S ( p , q ) . The slab always contains at least one vertex of the cycle: as p and q are at each side of S ( p , q ) and that it is a cycle, another edge has to go through the slab. As pq is the longest edge, no other edge can go through without having one of its endpoints in the region. This proves that the slab is sufficient.

However, the slab is not necessary: if pq is the largest edge of a cycle pqrst , the point t is at a distance at most d2 ( p , q ) from p , as r from q . Now, the point s is contained in the intersection of a disk centered at t and a disk centered at r and with radius d2 ( p , q ) . So there is only a part of the slab which is useful to ensure the 5-cycle freeness: the locus of the points of the slab which could be a vertex of the 5-cycle if all the other points were out of the slab. This region is S 5 ( p , q ) , as shown on Fig. 5, which is tight as removing a single point leads to a 5-cycle. ✷

This proves that there are at least two tight regions for 5-cycle freeness, as there is a tight region contained in S 5, and that S 5 and P 6 π/ 5 are incomparable. We show in the next sections that cycle freeness, which corresponds to forbidding a k -cycle for every k , has also at least two tight regions.

### 5. Other properties

We grouped in this section other monotone properties which are neither geometric, nor do they consist in forbidden graphs.

#### Cycle freeness

The two following lemmas will help up to characterize all the tight regions for cycle freeness.

Lemma 21. The closed slab S is tight for the cycle freeness property.

Proof. Let us consider the largest edge pq of a cycle. Since pq is the largest edge, there must be another edge in the cycle going through S ( p , q ) with at least one of its endpoints in S ( p , q ) . Hence pq cannot be an edge.

If S is not tight, by Lemma 8 there exists a convex and symmetric region R ( p , q ) ⊂ S ( p , q ) ; this region is either bounded or points on the border of the slab are missing (infinite continuous pieces of the border are missing, the region is neither closed nor open) and contained in the slab.

In either cases, placing a large even number of points equidistantly on a circle yields a cycle in the ERG, as the points will be properly aligned. ✷

We can even create an odd cycle if we take care of the intersections of the slabs. An example of a 7-cycle not forbidden by an open slab is shown on Fig. 6; if the region is convex and the slab not closed we can always create a cycle.

Lemma 22. Let M be the closed mastercard. If a region R not containing the slab S satisfies the cycle freeness property, M ( p , q ) \ R ( p , q ) does not contain a connected portion of the boundary ∂ M ( p , q ) of positive length. In particular, R contains the open mastercard.

q


<!-- p:10 -->

Proof. We first note that the closed mastercard M satisfies the property as it forbids a chain of length two: the mastercard of the largest of two edges would contain the endpoint of the other.

Let R ( p , q ) be a region such that there is a range of adjacent points on the boundary of M ( p , q ) not contained in R ( p , q ) . By our symmetry and convexity assumptions, the region R is contained in a diamond.

There exists a set of points generating an ERG containing a cycle that we can construct as follows. Let p and q be two points (see Fig. 7). There is a point r in M ( p , q ) \ R ( p , q ) and a neighborhood around r which is not in R ( p , q ) . We denote by Θ the angle of that neighborhood from p , centered at q ; ̸ pqr is in the interval (Θ,Θ + ε) .

To construct the cycle, we create a very long chain, as shown on Fig. 7; this is possible because of the symmetry of the region. The ε freedom allows to bend it: every two segments, we can turn with an angle of up to ε degree in the same direction (see Fig. 7).

Thus, we create a chain of 2 ⌈ 2 π/ε ⌉ segments, with turning angles (Θ, 2 π - (Θ + δ), Θ, 2 π - (Θ + δ), . . .) , with δ = 2 π/ ⌈ 2 π/ε ⌉ . As ε is a fixed value given by the region, a finite number of steps suffice to create a cycle.

This proves that no adjacent points on the boundary of the closed mastercard are missing. By convexity, this implies that R contains the open mastercard. ✷

Theorem 23. There is an infinite number of tight regions for cycle freeness : the closed slab S and an infinite set of regions M ′ contained in the closed mastercard and containing the open mastercard.

Proof. By Lemma 21, we know that the slab S is a tight region. We note that the open mastercard does not forbid cycles whose edges have the same length, and thus does not satisfy the property. However, by Lemma 22 any region satisfying the cycle freeness property and not containing the slab S contains the open mastercard M .

Let R ( p , q ) be a convex and symmetric region such that there are exactly 4 points on its boundary missing compared to M ( p , q ) . Then, for some of these configurations we can create a cycle. Let Θ and Θ ′ = π - Θ be then angles associated to these points, as shown on Fig. 8. We can create a chain, in which we can only choose to rotate by Θ ′ clockwise or counterclockwise. We define the absolute angle of the first edge in the chain as 0. If a chain contains k edges, and that we chose i times to turn counterclockwise then the absolute direction of the k th edge is i Θ ′ - ( k - i )Θ ′ .

This means that if, for any k , the 4 points on the boundary of M whose corresponding Θ ′ is exactly equal to 2 π/ k are not in R , we can create a cyclic chain which is a regular k -gon; these points must be contained in any tight region not containing the slab.

The considered chain forms a k -cycle when the ( k + 1 ) th edge and the first one are the same i.e., begin at the same position and have the same absolute direction. For every set of vertices V , ERGR ( V ) is a planar graph as R contains the ball B . Thus the sum of the rotations is exactly equal to ± 2 π .

By Lemma 22, we know that every tight region not containing S cannot have a connected portion of ∂ M ( p , q ) of positive length missing. We also know that these missing points in M \ R cannot allow regular k -gons. Now, for any region R with exactly 4 points missing such that Θ ′ ̸= 2 π/ k , ∀ k ∈ N , the resulting graph contains no cycle. However, combinations of these missing points could lead to cycles.

If points at angles Θ 1 , Θ 2 , . . . , Θ m (with supplementary angles Θ ′ 1 , Θ ′ 2 , . . . , Θ ′ m ) are in M ( p , q ) \ R ( p , q ) , we can create a k -cycle only if

∃ k ∈ N 0 , ∃ α 1 , α 2 , . . . , α m ∈ N


<!-- p:11 -->


such that

$$\sum _ { i = 1 } ^ { m } \alpha _ { i } = k$$

and

$$\sum _ { i = 1 } ^ { m } \Theta _ { i } ^ { \prime } \alpha _ { i } = 2 \pi$$

as linear combinations of these angles would lead to cycles. This is only a necessary condition, some of these sets cannot produce cycles (i.e., the corresponding chain would be self intersecting or the last edge of the chain is not adjacent to the first one).

On the other hand, we know that the following condition is sufficient to lead to a lk -cycle if missing from R :

$$\exists k , l \geqslant 3 \in \mathbb { N } _ { 0 } , \exists \alpha _ { 1 } , \alpha _ { 2 } , \dots , \alpha _ { m } \in \mathbb { N } \\$$

such that

$$\sum _ { i = 1 } ^ { m } \alpha _ { i } = k$$

and

$$\sum _ { i = 1 } ^ { m } \Theta _ { i } ^ { \prime } \alpha _ { i } = 2 \pi / l .$$

We can construct these kl -cycles as follows: with k edges we can construct a chain such that the absolute angle between the first and last edge is exactly 2 π/ l . By concatenating l such chains we ensure that the cumulative rotation is exactly 2 π and the cycle is closed. Note that for this to work, the angles must be reasonably small, i.e., the sequence of k edges must be planar and consecutive blocks of k edges cannot intersect. But there is still an infinity of such configurations.

In conclusion, we know that there is an infinity of subsets of the boundary of M which cannot be missing, as their lack would lead to cycles. We can restrict the subsets to consider to the extremal ones, where we cannot add a single point without enabling the creation of cycles, and there is still an infinity of subsets (any pair of missing points leading to a cycle generate at least two extremal subsets). They correspond to tight regions for cycle-freeness.

The last step consists in proving that these tight regions are contained in the closed mastercard M . We proceed by contradiction: if a region R is tight, contains the open mastercard and is not contained in the closed mastercard, there exists at least one point, r ∈ R ( p , q ) out of the mastercard. r is at a distance bigger than d2 ( p , q ) from p and from q . Thus this point forbids an edge in a cycle where every edge has not the same length. But that cycle is forbidden by the open mastercard, which contradicts the fact that R is tight.

We end with an incomplete characterization of the regions M ′ in M which are tight, but this proves that there are infinitely many of these. ✷

#### Planarity

Here we consider the planarity of the graph, and not of its embedding which was analyzed in Section 3. Kuratowski's theorem says that planarity corresponds to forbidding K 3 , 3 and K 5 as minors.

Theorem 24. The closed ball B is a tight region for planarity.

Proof. As shown previously, the embedding of any ERGB is planar. For every region R ( p , q ) ⊂ B ( p , q ) , we can create a set of edges having a K 5 as minor, as shown on Fig. 10. The two gadgets used in this construction are crossing edges, which are constructed using the fact that the region is contained in the ball, and the induced K 1 , 4 that is not even forbidden by the ball. ✷

#### Connectivity

Theorem 25. The open lune L is the unique tight region for connectivity.

Proof. The open lune defines a connected graph as it is a Relative Neighborhood Graph [15]. Connectivity is monotone with respect to edge insertion. We cannot add a single point to the lune without losing the graph property, because otherwise, there are sets of vertices for which the ERG is not connected. We can obtain such a set of vertices in the following way: R ( p , q ) strictly contains a triangle joining the points p and q and a point z out of the open L ( p , q ) (see Fig. 9). We first consider the case where the edge pq is smaller than the edge qz , the case with pq greater than qz being symmetric; then we analyze the case where pq and qz are equal.


<!-- p:12 -->


Fig. 11. Partial order of inclusion among regions and corresponding monotone properties.

We construct our set of vertices as shown in Fig. 9. Given a pair of points ( p , q ) we define a third point z which is contained in the region R ( p , q ) \ L ( p , q ) . We repeat the process using the points z and q while the triangle defined by the three points does not contain a previously defined point. This set of points defines an unconnected ERG: q is not connected to any other point, because there is always an item contained in R ( p , q ) .

For the case where pq and qz have the same length, we consider only three points, as shown in Fig. 9. The edge pq is not in the graph as z is in R ( p , q ) . Symmetrically, the edge qz is not in the graph as p is in R ( p , q ) . Thus the point q is isolated.

The uniqueness comes from the fact that any other region which does not contain any point out of the open L ( p , q ) is strictly contained in it, and is thus not tight. ✷

#### Bipartiteness

Theorem 26. There is an infinite number of tight regions for bipartiteness including the closed slab S and an infinite set of regions M ′ contained in the closed mastercard and containing the open mastercard.

Proof. Cycle freeness implies bipartiteness. The tight regions for cycle freeness are tight for bipartiteness, because our counter-examples presented in the cycle freeness proof can be used to create odd cycles: even by adding a restriction on the parity of the cycles to create, we can still prove the existence of an infinite number of tight regions using exactly the same arguments. ✷

### 6. Discussion

Fig. 11 summarizes some of the results. Properties for which we proved that the tight region is unique are marked with ⋆ ; the vertical dotted lines represent the threshold at which some property is ensured. For instance every region at least as big as the lune ensures triangle freeness, while every region smaller than the lune leads to a connected graph.


<!-- p:13 -->


The ERG model has limitations and not all set of properties can be satisfied by a region. For instance, in our model, we cannot combine cycle freeness and connectivity, as the region cannot be smaller than the lune and bigger than the mastercard or than the slab at the same time. Some other properties always come together, such as forbidding a 4-star and a 4-cycle.

The figure can help in studying the properties of existing classes of graphs. For instance, for β -Skeletons the parameter β determines the position of the template region in the partial order from which one can deduce the set of properties that are satisfied.

ERGs constitute a convenient way to construct graphs from sets of points. Other definitions of proximity graph using for instance non-convex, non-anchored, or non-symmetric template regions, could lead to a more fine-grained way of ensuring properties.

### Acknowledgements

We thank Samuel Fiorini for helpful discussions about partial orders and the mathematical foundations of our work. We also thank the anonymous reviewer whose comments helped to improve the presentation of our results.
