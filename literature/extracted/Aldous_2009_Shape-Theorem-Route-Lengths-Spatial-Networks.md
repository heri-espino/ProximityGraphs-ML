---
id: "Aldous_2009_Shape-Theorem-Route-Lengths-Spatial-Networks"
source_pdf: "../pdf/Aldous_2009_Shape-Theorem-Route-Lengths-Spatial-Networks.pdf"
source_filename: "Aldous_2009_Shape-Theorem-Route-Lengths-Spatial-Networks.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "good"
extraction_score: 90.0
visual_assets: "disabled"
references_file: "../references/Aldous_2009_Shape-Theorem-Route-Lengths-Spatial-Networks.references.md"
---

<!-- p:1 -->

## The Shape Theorem for Route-lengths in Connected Spatial Networks on Random Points

David J. Aldous ∗

November 6, 2018

##### Abstract

For a connected network on Poisson points in the plane, consider the route-length D ( r, θ ) between a point near the origin and a point near polar coordinates ( r, θ ), and suppose ED ( r, θ ) = O ( r ) as r →∞ . By analogy with the shape theorem for first-passage percolation, for a translation-invariant and ergodic network one expects r - 1 D ( r, θ ) to converge as r → ∞ to a constant ρ ( θ ). It turns out there are some subtleties in making a precise formulation and a proof. We give one formulation and proof via a variant of the subadditive ergodic theorem wherein random variables are sometimes infinite.

MSC 2000 subject classifications: 60D05, 90B15

Key words and phrases. Poisson point process, random network, spatial network, first-passage percolation, shape theorem, subadditive ergodic theorem.

Short title: Shape Theorem for Spatial Networks.

∗ Department of Statistics, 367 Evans Hall # 3860, U.C. Berkeley CA 94720; aldous@stat.berkeley.edu; www.stat.berkeley.edu/users/aldous. Aldous's research supported by N.S.F Grant DMS-0704159.


<!-- p:2 -->


## 1 Introduction

This paper is a technical part of a broader project investigating connected random spatial networks, in particular networks built over a Poisson process of points ξ in the plane. See [3] for the least technical overview. In any such network there is a (shortest-) route-length d ( ξ, ξ ′ ) between each pair of points of the Poisson process, which by connectivity is finite. Under weak assumptions (see [1] for a sufficient condition) one expects the mean route-length to grow only linearly with Euclidean distance. Consider a (deliberately vague, for now) notion

D ( r, θ ) is the route-length between a point ξ near the origin and a point ξ ′ near polar coordinates ( r, θ ),

and suppose we know ED ( r, θ ) = O ( r ) - that is, suppose we have a linear upper bound on mean route-length. If the random network has translationinvariant and ergodic distribution, then we intuitively expect that there should be a limit constant ρ ( θ ) = lim r →∞ r - 1 ED ( r, θ ) and that in some sense renormalized random route-lengths should converge to the limit constant: r - 1 D ( r, θ ) → ρ ( θ ). This intuition arises in part from an analogy with the shape theorem for first-passage percolation [6, 7] on the edges of the grid Z 2 . In the usual such model the times τ ( e ) attached to edges e are assumed i.i.d., but the proof (based on the subadditive ergodic theorem) extends to the setting where the τ ( e ) are assumed only to be ergodic translation-invariant. Studying route-lengths in random networks built over Poisson point processes is perhaps the most natural continuum analog of studying first-passage times in such lattice models. Two previously studied special continuum models, superficially different, can be fitted into our general setup - see section 1.3.

### 1.1 Formulating a theorem

In the broader project we visualize a spatial network as having vertices and edges; in most contexts, summary statistics such as 'mean edge-length per unit area' are natural and important. In the specific context of this paper, only the induced route-lengths d ( ξ, ξ ′ ) are of interest, so we will dispense with other structure and work within the following set-up throughout this paper.

(A1) There is a Poisson process of points Ξ = { ξ } of intensity one, on R 2 . (A2) On each realization of Ξ there are non-negative finite 'route-lengths' d ( ξ, ξ ′ ) = d ( ξ ′ , ξ ) which are assumed (only) to satisfy the triangle inequality.


<!-- p:3 -->


̸

(A3) The distribution of the whole structure { ξ ; d ( ξ, ξ ′ ) } is translationinvariant. That is, invariant w.r.t. the action of the group ( T a,b ; ( a, b ) ∈ R 2 ) where T a,b ( x, y ) = ( x + a, y + b ). Moreover for each ( a, b ) = (0 , 0) the action of T a,b is ergodic.

Some specific examples are mentioned briefly in section 1.2, though our emphasis is on the generality of the assumptions. So it is worth mentioning what we are not assuming. We are not assuming

- (B1) rotational invariance

(B2) that d ( ξ, ξ ′ ) ≥ | ξ - ξ ′ | (implicit in the underlying 'route-lengths' story) (B3) any kind of 'locality' for the route-lengths d ( ξ, ξ ′ ).

In particular, for a nearby pair ξ, ξ ′ the route-length d ( ξ, ξ ′ ) may depend on the entire configuration Ξ. Finally, we often describe points in Z 2 by their radial coordinates. So ( r, θ ) denotes a point z ∈ Z 2 ; conversely, given z ∈ Z 2 we write ( r z , θ z ) for its radial coordinates.

At first sight it looks easy to state and prove a theorem under assumptions (A1-A3) - just find a suitable formalization of the vague notion D ( r, θ ) above, to which the subadditive ergodic theorem can be applied. But actually carrying this through seems surprisingly subtle. One attempt is to condition on points being planted at the origin and at ( r, θ ): the remaining points being still distributed as the Poisson point process, one can define a conditioned network and then define D ( r, θ ) to be the route-lengths between the planted points in the conditioned network. However, for rather trivial reasons the desired result is simply not true in this interpretation (see section 2.2). A second attempt is to interpret D ( r, θ ) as originally stated for the point nearest the origin and the point nearest ( r, θ ); this makes a precise definition but it seems hard to work directly with this definition. A third attempt is to start by finding some feature to which one can apply the subadditive ergodic theorem. For instance, let ξ n be the leftmost point in the semi-infinite strip [ n, ∞ ) × [ - 1 , 1]. One can certainly apply the subadditive ergodic theorem to the array ( d ( ξ m , ξ n )) to conclude that (under an integrability assumption) n - 1 d ( ξ 0 , ξ n ) converges a.s. to a constant limit ρ (0). At first sight this approach seems to resolve the whole issue. But the precise hypotheses and conclusions are tied to the particular feature initially chosen, and it seems technically hard to reconcile the results from different choices.

We adopt a fourth approach, aimed at a more natural type of conclusion. Write A,B for bounded subsets of R 2 and for z ∈ R 2 write z + B = { z + z ′ : z ′ ∈ B } . To motivate the precise definitions (1,2) below, consider ξ ∈ A and ξ ′ ∈ z + B with r z large; the route-length d ( ξ, ξ ′ ) provides one interpretation of our initial vague notion D ( r z , θ z ), which we want to prove is approximately the (deterministic) length r z ρ ( θ z ). To avoid conditioning on existence of points in sets, we sum: ∑ ξ ∈ A ∑ ξ ′ ∈ z + B d ( ξ, ξ ′ ) should be N ( A ) N ( z + B ) r z ρ ( θ z ) ± o ( r z ) where N ( · ) is the counting process of Ξ. But we can avoid writing N ( · ) by rewriting the approximation as ∑ ξ ∈ A ∑ ξ ′ ∈ z + B | d ( ξ, ξ ′ ) - r z ρ ( θ z ) | = o ( r z ). This prompts the following definitions.


<!-- p:4 -->


For c ≥ 0 define a random variable

$$S ( A , B ; c ) \colon = \sum _ { \xi \in A } \sum _ { \xi ^ { \prime } \in B } | d ( \xi , \xi ^ { \prime } ) - c | .$$

Say the random network has the L 1 shape property if there exist constants ρ ( θ ) such that, for all bounded A,B ,

$$r _ { z } ^ { - 1 } E S ( A , z + B ; r _ { z } \rho ( \theta _ { z } ) ) \rightarrow 0 \text { as } r _ { z } \rightarrow \infty .$$

Because S is an additive set function, it is enough to prove (2) when A and B are sufficiently large (or sufficiently small) squares centered at the origin; and in the latter case we see how this notion provides a formalization of the idea behind D ( r, θ ).

Having decided on the conclusion we seek, what hypotheses do we need? Obviously it is necessary that the corresponding linear upper bound holds: for all bounded A,B ,

$$E \sum _ { \xi \in A \, \xi ^ { \prime } \in z + B } d ( \xi , \xi ^ { \prime } ) = O ( r _ { z } ) \text { as } r _ { z } \to \infty .$$

We conjecture that (3) is sufficient (see section 2.1 for precise statement). However in this paper we work under the analogous, but stronger, L 2 assumption: for all bounded A,B ,

$$\sup _ { z } \frac { E \sum _ { \xi \in A } \sum _ { \xi ^ { \prime } \in z + B } d ^ { 2 } ( \xi , \xi ^ { \prime } ) } { \max ( 1 , r _ { z } ^ { 2 } ) } < \infty .$$

Again, it is enough to verify this when A and B are sufficiently small squares centered at the origin.

Theorem 1 Under the standing assumptions (A1 - A3), if hypothesis (4) holds then the L 1 shape property (2) holds. Moreover

̸

$$\sup _ { \theta _ { 2 } \neq \theta _ { 1 } } \frac { | \rho ( \theta _ { 2 } ) - \rho ( \theta _ { 1 } ) | } { | \theta _ { 2 } - \theta _ { 1 } | } < \infty .$$


<!-- p:5 -->


This is proved in section 2, though the main work is delegated to a new 'subadditive ergodic theorem with missing values', Proposition 4, stated and proved in section 3. A conjectured stronger 'a.s. shape theorem' conclusion is discussed briefly in section 2.1. Obviously, if we add the assumption of rotational invariance then ρ ( θ ) is constant.

### 1.2 Examples using route-lengths

In all these examples, the d ( ξ, ξ ′ ) are minimal route-lengths within given networks.

Proximity graphs [5, 3]. This family of graphs (our main example) is defined by:

( ξ, ξ ′ ) is an edge iff the set A ( ξ, ξ ′ ) contains no other point of the Poisson process

for different choices of A ( ξ, ξ ′ ), a fundamental choice (giving the relative neighborhood graph ) being

```
A(($, $\') is the intersection of the disc with center $\ and radius
| $\' - $\xi| and the disc with center $\' and radius | $\' - $\xi|.
```

Other graphs in the family use subsets of this A and hence are supergraphs of the relative neighborhood graph and hence can only have smaller routelengths. The purpose of the companion paper [1] is to give a general property that implies our present condition (4), and to verify this property for the relative neighborhood graph. It follows that (4) holds for the relative neighborhood graph (and hence for every proximity graph) on a Poisson point process. Because edges are defined by a deterministic rule, proximity graphs inherit the stationary ergodicity property (A3) from the trivial tail σ -field property of the Poisson process. So our Theorem 1 applies, and by rotational invariance ρ ( θ ) is a constant ρ , depending on the model. Monte Carlo estimates of ρ (around 1.4 for the relative neighborhood graph) can be seen in [3] but we do not know any explicit rigorous upper bound.

The general condition in [1] might be applicable to other models, but the examples below can be handled more directly.

Lattice-based networks. One can start with (for instance) the square grid lattice as a network, and simply connect each Poisson point to the nearest grid point. One can see directly that this random network satisfies the shape property with ρ ( θ ) = | cos θ | + | sin θ | . This conclusion remains true if we make the network be translation-invariant and ergodic by replacing the deterministically-spaced grid lines by randomly-spaced ones.


<!-- p:6 -->


Asymptotically efficient networks. It is not surprising that there are networks which are 'optimal' in the sense ρ ( · ) ≡ 1. It is at first sight surprising that one can find such networks whose length-per-unit-area is arbitrarily close to the minimum possible (over all connected networks - attained by the Steiner tree) length-per-unit-area. But this can be achieved by the simple device of superimposing, over the Steiner tree, a sparse Poisson line process. This construction is studied in detail in [2].

The Hammersley network. This network, introduced in [3], has the remarkable property that at each point ξ there are exactly 4 edges, one in each of the four quadrant directions (i.e. between East and North, etc). This network has not been studied carefully, but it is plausible one can use known properties of the underlying Hammersley process to prove directly that the shape property holds with ρ ( θ ) = ρ 0 ( | cos( θ - π/ 4) | + | sin( θ - π/ 4) | ) for some constant ρ 0 .

### 1.3 Other examples

Suppose we remove the 'satisfy the triangle inequality' requirement from (A2), to get instead

```
(A 2 ^*) \ On each realization of \equiv there are ``costs'' 0 < c ( \xi , \xi ^*) = \\ c ( \xi ^ { * } , \xi ) \leq \infty .
```

One can now define d ( ξ, ξ ′ ) as the cost of the minimum-cost path from ξ to ξ ′ , and this makes d satisfy the triangle inequality. So, provided d is always finite, (A2) holds. If the other hypotheses of Theorem 1 hold for d , then the conclusion of Theorem 1 gives the L 1 shape property for d . The following two particular cases have been studied previously by direct methods which establish the a.s. shape theorem; our Theorem 1 applies (assuming second moments in (a)) to give the L 1 shape theorem.

- (a) Take the Delaunay triangulation on the Poisson points, and then take c ( ξ, ξ ′ ) to be i.i.d. with finite mean on the edges of the triangulation (and = ∞ elsewhere): [9].
- (b) Fix α &gt; 1 and set c ( ξ, ξ ′ ) = | ξ - ξ ′ | α : [4].


<!-- p:7 -->


## 2 Reducing the proof of Theorem 1 to a subadditivity result

Write A,B for bounded subsets of R 2 with non-zero area. Write N ( A ) for the number of points of the Poisson point process Ξ in A and write G ( A ) for the 'good' event { N ( A ) ≥ 1 } . On G ( A ) let ξ A be a uniform random point of Ξ ∩ A . Note that hypothesis (4) implies

$$E [ d ( \xi _ { z _ { 1 } + A } , \xi _ { z _ { 2 } + B } ) 1 _ { G ( z _ { 1 } + A ) \cap G ( z _ { 2 } + B ) } ] \leq \kappa ( A , B ) \max ( 1 , | z _ { 1 } - z _ { 2 } | ) \quad ( 6 )$$

where κ ( A,B ) &lt; ∞ depends only on A,B .

Fix θ ∈ [0 , 2 π ) and fix a bounded subset A ⊂ R 2 of non-zero area. Write z n for the point with radial coordinates ( nr 0 , θ ), where r 0 is sufficiently large that the sets z n + A are disjoint. So G ( z n + A ) is the event { N ( z n + A ) ≥ 1 } , and on G ( z n + A ) let ξ z n + A be a uniform random point of Ξ ∩ ( z n + A ).

Consider the array of random variables

$$X _ { m n } \ & = \ d ( \xi _ { z _ { m } + A } , \xi _ { z _ { n } + A } ) \ \text { on } G ( z _ { m } + A ) \cap G ( z _ { n } + A ) \\ & = \ \infty \ \text { otherwise } .$$

Note (A2) implies the triangle inequality

$$\text {for } \ell < m < n , \, X _ { \ell n } \leq X _ { \ell m } + X _ { m n } \text { on } 1 _ { G ( z _ { \ell } + A ) \cap G ( z _ { m } + A ) \cap G ( z _ { n } + A ) } \ . \quad ( 8 )$$

Proposition 4, stated and proved in section 3, is tailored to this setting. Specifically, hypothesis (i) is (7), (ii) is (8), (iii) follows from Poisson independence, (iv) from (A3) and (v) from (4). The conclusion of Proposition 4 is that there exists a constant 0 ≤ ρ ( θ ) &lt; ∞ such that

$$& \text {at there exists a constant } 0 \leq \rho ( \beta ) < \infty \text { such that } \\ & \quad E \left [ \left | \frac { d ( \xi _ { A } , \xi _ { z n + A } ) } { n r _ { 0 } } \ - \rho ( \theta ) \right | 1 _ { G ( A ) \cap G ( z _ { n } + A ) } \right ] \to 0 . \\ & \text {is the main ingredient of the proof; the argument below continues} \\ & \text {this is the main supporting } ( 0 ) \text {, its the $t$ated below continues}$$

This is the main ingredient of the proof; the argument below continues with the details of converting (9) into the stated conclusion of Theorem 1. The typography in (9) is potentially confusing; note we are multiplying an absolute value by an indicator, not taking a conditional expectation.

A priori the limit constant ρ ( θ ) in (9) might depend on A and on r 0 . We first show it does not depend on r 0 ; more precisely, we will show

$$\ W \text { first show } & \text { if } \text { does not depend on } 7 \{ , \text { in } \text { precisely, } \text { we } \text { win } \text { show } \\ & \text { } E \left [ \left | \frac { d ( \xi _ { A } , \xi ( r , \theta ) + A ) } { r } \ - \rho ( \theta ) \right | 1 _ { G ( A ) \cap G ( ( r , \theta ) + A ) } \right ] \to 0 \text { as } r \to \infty .$$


<!-- p:8 -->


Let us give the argument for (10) in some detail, intending to omit similar details later. Write r = ( n 1 + n 2 ) r 0 + γ for some 0 ≤ γ &lt; r 0 . Let r →∞ while choosing n 1 = n 1 ( r ) → ∞ and n 2 = n 2 ( r ) → ∞ . By (9) and translationinvariance

$$\text {invariance} \\ E \left [ \left [ \frac { d ( \xi _ { A } , \xi _ { ( n _ { 1 } r _ { 0 } , \theta ) + A } ) - n _ { 1 } r _ { 0 } \rho ( \theta ) } { r } \right | 1 _ { G ( A ) \cap G ( ( n _ { 1 } r _ { 0 } , \theta ) + A ) } \right ] \to 0 \\ \\ E \left [ \left [ \frac { d ( \xi _ { ( n _ { 1 } r _ { 0 } + \gamma , \theta ) + A } , \xi _ { ( r , 0 ) + A } ) - n _ { 2 } r _ { 0 } \rho ( \theta ) } { r } \right | 1 _ { G ( ( n _ { 1 } r _ { 0 } + \gamma , \theta ) + A ) \cap G ( ( r , \theta ) + A ) } \right ] \to 0 . \\ \\ \text {Combining these with } ( 6 ) \text { applied to } \xi _ { ( n _ { 1 } r _ { 0 } , \theta ) + A } \text { and } \xi _ { ( n _ { 1 } r _ { 0 } + \gamma , \theta ) + A } , \text { and using} \\ \text {the triangle inequality for } d ( \cdot , \cdot ) ,$$

Combining these with (6) applied to ξ ( n 1 r 0 ,θ )+ A and ξ ( n 1 r 0 + γ,θ )+ A , and using the triangle inequality for d ( · , · ),

$$& \text {the range in} \, \Omega \text {,} \, , \, , \\ & \quad E \left [ \left | \frac { d ( \xi _ { A } , \xi _ { ( r , \theta ) + A } ) } { r } \, - \rho ( \theta ) \right | 1 _ { G ( A ) \cap G ( ( r , \theta ) + A ) \cap G ( ( n _ { 1 r _ { 0 } , \theta ) + A ) \cap G ( ( n _ { 1 r _ { 0 } + \gamma , \theta ) + A ) } ] } \right ] \to 0 \text { as } r \to \infty . \\ & \quad \text {This expression differs from } ( 1 0 ) \text { only by the inclusion of the restriction to } \\ & \quad C ( ( \begin{array} { c c } 0 \\ - \rho \end{array} ) + A ) \subset C ( ( \begin{array} { c c } 0 \\ - \rho \end{array} ) + A ) \, .$$

This expression differs from (10) only by the inclusion of the restriction to G (( n 1 r 0 , θ ) + A ) ∩ G (( n 1 r 0 + γ, θ ) + A ), an event which has probability at least 1 - p for some p = p ( r 0 , A ) &lt; 1. Given k we can choose (for large r ) k different values of n 1 such that the k corresponding events are independent because the underlying sets are disjoint; it follows that

$$& \text { because the underlying $G$-adic $H$-functor, and if $H$-functor $W$-functor} \\ & \quad E \left [ \left | \frac { d ( \xi _ { A } , \xi _ { ( r , \theta ) + A ) } } { r } \ - \rho ( \theta ) \Big | 1 _ { G ( A ) \cap G ( ( r , \theta ) + A ) \cap H ( r , k ) } \right ] \to 0 \text { as } r \to \infty \\ & \quad \text {for certain events} \ H ( r , k ) \text { such that } P ( H ( r , k ) ) \geq 1 - p ^ { k } \text { for large } r . \text { Letting}$$

for certain events H ( r, k ) such that P ( H ( r, k )) ≥ 1 - p k for large r . Letting k →∞ and appealing to the L 2 bound (4) establishes (10).

Now consider two subsets A ⊂ A ′ . Could the two constants ρ ( θ ) and ρ ′ ( θ ) in (10) be different? When we make independent choices of random points ξ z + A and ξ z + A ′ there is some fixed probability p ( A,A ′ ) &gt; 0 that the two random points are the same, and it easily follows that the limit constants must be equal. That is, ρ ( θ ) does not depend on choice of A .

Next we prove the Lipschitz property (5). Fix θ 1 and θ 2 . The triangle inequality and (6) give

$$E [ | d ( \xi _ { A } , \xi _ { ( r , \theta _ { 1 } ) + A } ) - d ( \xi _ { A } , \xi _ { ( r , \theta _ { 2 } ) + A } ) | 1 _ { G ( A ) \cap G ( ( r , \theta _ { 1 } ) + A ) \cap G ( ( r , \theta _ { 2 } ) + A ) } ] \leq$$

E [ d ( ξ ( r,θ 1 )+ A , ξ ( r,θ 2 )+ A ) | 1 G ( A ) ∩ G (( r,θ 1 )+ A ) ∩ G (( r,θ 2 )+ A ) ] ≤ κ ( A,A ) min(1 , r | θ 2 - θ 1 | ) . Applying (10),

$$| \rho ( \theta _ { 2 } ) - \rho ( \theta _ { 1 } ) | P ^ { 3 } ( G ( A ) ) \leq \kappa ( A , A ) \ | \theta _ { 2 } - \theta _ { 1 } |$$


<!-- p:9 -->


and now any choice of A establishes (5).

Next we want to prove the analog of (10) where the angle is not fixed. That is, for z = ( r z , θ z ) with r z →∞ , we claim

$$\text {that is, for } & z = ( r _ { z } , z _ { z } ) \text { with } r _ { z } \to \infty , \text { we can } \\ & E \left [ \left | \frac { d ( \xi _ { A } , \xi _ { z + A } ) } { r _ { z } } \ - \rho ( \theta _ { z } ) \right | 1 _ { G ( A ) \cap G ( z + A ) } \right ] \to 0 \text { as } r _ { z } \to \infty . \\ \intertext { B y c o p a c t h e n s } & \text {by compactness and continuity of } \rho ( \cdot ) \text { we can reduce to the case } ( r _ { n } , \theta _ { n } )$$

By compactness and continuity of ρ ( · ) we can reduce to the case ( r n , θ n ) where θ n → θ , and it is enough to prove

$$\text {where } & b _ { n } \rightarrow v , \text { and } f \text { is enough to prove } \\ & E \left [ \left | \frac { d ( \xi _ { A } , \xi _ { ( r _ { n } , \theta _ { n } ) + A } ) } { r _ { n } } \ - \rho ( \theta ) \right | 1 _ { G ( A ) \cap G ( ( r _ { n } , \theta _ { n } ) + A ) } \right ] \rightarrow 0 \text { as } r _ { n } \rightarrow \infty . \\ & \text {Here we repeat the format of the argument for } ( 1 0 ) . \text { Take } r _ { n } ^ { * } = ( 1 + o ( 1 ) ) r _ { n } .$$

Here we repeat the format of the argument for (10). Take r ∗ n = (1+ o (1)) r n . Apply the triangle inequality to ξ A , ξ ( r ∗ n ,θ )+ A , ξ ( r n ,θ n )+ A , apply the fixedθ result (10) to the first distance and apply (6) to the second distance; we deduce the analog of (12) with the extra term 1 G (( r ∗ n ,θ )+ A ) . But this is true for each of multiple possible choices for r ∗ n , so we can deduce (12) and thence (11).

To complete the proof we need to convert (11) into an assertion involving the sums S ( A,z + B ; r z ρ ( θ z )) appearing in (2). Let us state the underlying logical structure carefully; note there is no assumption that the ( Y ( n ) ij ) are independent of ( N ( n ) 1 , N ( n ) 2 ).

Lemma 2 Fix λ 1 , λ 2 . For each n let ( Y ( n ) ij , 1 ≤ i ≤ N ( n ) 1 , 1 ≤ j ≤ N ( n ) 2 ) be an array of nonnegative random variables, and suppose that N ( n ) 1 and N ( n ) 2 are independent with Poisson( λ 1 ) (resp. λ 2 ) distributions. On the event { N ( n ) 1 ≥ 1 , N ( n ) 2 ≥ 1 } , and conditional on the entire collection ( Y ( n ) ij , 1 ≤ i ≤ N ( n ) 1 , 1 ≤ j ≤ N ( n ) 2 ) , take ( U ( n ) 1 , U ( n ) 2 ) to be independent with Uniform [1 , 2 , . . . , N ( n ) 1 ] and Uniform [1 , 2 , . . . , N ( n ) 2 ] distributions. Suppose

$$Y _ { U _ { 1 } ^ { ( n ) } , U _ { 2 } ^ { ( n ) } } ^ { ( n ) } \ 1 _ { ( N _ { 1 } ^ { ( n ) } \geq 1 , N _ { 2 } ^ { ( n ) } \geq 1 ) } \to 0 \ i n \ p r o b a b i l i t y \ a s \ n \to \infty .$$

Then

$$\sum _ { i = 1 } ^ { N _ { 1 } ^ { ( n ) } } \sum _ { j = 1 } ^ { N _ { y } ^ { ( n ) } } \ Y _ { i j } ^ { ( n ) } \rightarrow 0 \ i n \ p r o b a b i l i t y \ a s \ n \to \infty .$$

Proof. It is enough to prove the conclusion restricted to { 1 ≤ N ( n ) 1 ≤ L, 1 ≤ N ( n ) 2 ≤ L } for fixed L . But with this restriction, the hypothesis implies max ij Y ( n ) ij → 0 in probability, which in turn implies the conclusion.


<!-- p:10 -->


Now consider the setting of (11). As r z →∞ the array

$$\text {consider the setting of (111).} \ A s \ r _ { z } \to \infty \text { the array} \\ \left ( \left | \frac { d ( \xi , \xi ^ { \prime } ) } { r _ { z } } \ - \rho ( \theta _ { z } ) \right | , \ \xi \in A , \ \xi ^ { \prime } \in z + A \right ) \\ \text {the assumptions of Lemmma 2, and the conclusion is}$$

satisfies the assumptions of Lemma 2, and the conclusion is

$$r _ { z } ^ { - 1 } \ S ( A , z + A ; r _ { z } \rho ( \theta _ { z } ) ) \to 0 \text { in probability} .$$

The L 2 bound (4) extends this to

$$r _ { z } ^ { - 1 } \ E S ( A , z + A ; r _ { z } \rho ( \theta _ { z } ) ) \rightarrow 0$$

which is enough to establish the L 1 shape property.

### 2.1 The conjectured a.s. shape theorem

Implicit in the underlying picture of route-lengths in spatial networks is that route-lengths are at least as big as Euclidean distance:

$$d ( \xi , \xi ^ { \prime } ) \geq | \xi - \xi ^ { \prime } | .$$

This was not assumed for Theorem 1; assuming it here, we see ρ ( θ ) ≥ 1. Using 'triangle inequality' arguments as in the previous section, it is easy to check that

$$B \colon = \{ z = ( r , \theta ) \, \colon \, r \leq 1 / \rho ( \theta ) \}$$

defines a convex subset of the unit disc. A natural informal statement of a shape theorem is that, if we plant one Poisson point ξ 0 at the origin, then for large l the set of points at route-length at most l from ξ 0 is approximately the set of points within l B . So one can formalize the a.s. shape property as follows, in the context of a planted point ξ 0 at the origin. For each ε &gt; 0 there exists random L ( ε ) &lt; ∞ such that for all l &gt; L ( ε )

$$\Xi \cap ( 1 - \varepsilon ) \ell B \subseteq \{ \xi \in \Xi \colon d ( \xi , \xi _ { 0 } ) \leq \ell \} \subseteq ( 1 + \varepsilon ) \ell B .$$

This has been proved by direct methods in the two special models of section 1.3. Because our Theorem 1 conclusion involves L 1 convergence instead of a.s. convergence, it implies only a somewhat weaker result; and also our '' L 2 bounded' assumption is stronger than seems necessary. In other words, the natural conjecture suggested by the analogy with the shape theorem for first-passage percolation is as follows.


<!-- p:11 -->


Conjecture 3 Under the standing assumptions (A1 - A3), and (3) and (13), there exists a convex set B such that the a.s. shape property holds.

And though we work throughout with an underlying Poison point process, such a result might be expected to hold for any ergodic translation-invariant point process.

### 2.2 A minor counter-example

Take a model to which Theorem 1 applies with ρ ( θ ) &gt; 1. Choose r k ↑ ∞ fast and δ k ↓ 0. Modify the model by putting a straight line link between each pair of points whose distance apart is in ∪ k [ r k , r k + δ k ]. By making the δ k ↓ 0 sufficiently fast and appealing to the 'minimum cost path' device of section 1.3, the hypotheses and conclusion of Theorem 1 remain true with the same limit ρ ( θ ) - the extra links make no difference to route-length between typical pairs. But if we had attempted to formulate the theorem using ' D ( r, θ ) = distance between two points at distance r apart' then we would not get a r →∞ limit, because of the exceptional r ∈ ∪ k [ r k , r k + δ k ].

## 3 Asubadditive ergodic theorem with missing values

We develop a variation of Kingman's subadditive ergodic theorem (see e.g. [8]) in which the random variables ( X ij , 0 ≤ i &lt; j &lt; ∞ ) are sometimes undefined (in which case we will set the value to ∞ , though that isn't quite the natural interpretation in our application). Consider a sequence ( G i , 0 ≤ i &lt; ∞ ) of 'good' events, and write I i for the indicator 1 G i and write I ij = I i I j = 1 G i ∩ G j . Our assumptions are

- (i) 0 ≤ X ij ≤ ∞ ; X ij &lt; ∞ on G i ∩ G j .
- (ii) For i &lt; j &lt; k , X ik ≤ X ij + X jk on G i ∩ G j ∩ G k .
- (iii) The process ( I i , 0 ≤ i &lt; ∞ ) is independent Bernoulli( δ ) for fixed 0 &lt; δ &lt; 1.
- (iv) Setting X i = ( I i , X i,i + k , 1 ≤ k &lt; ∞ ), the process ( X i , 0 ≤ i &lt; ∞ ) is stationary and ergodic.
- (v) sup n ≥ 1 n - 2 E [ X 2 0 n I 0 n ] &lt; ∞ .

Mostly these are the obvious analogs of the usual assumptions [8]. Note that in the usual setting we have a trivial implication

$$\text {if } E X _ { 0 1 } < \infty \text { then } \sup _ { n } n ^ { - 1 } E X _ { 0 n } \leq E X _ { 0 1 } < \infty$$


<!-- p:12 -->


whereas in our setting the implication:

$$\text {if } E [ X _ { 0 1 } I _ { 0 1 } ] < \infty \text { then } \sup _ { n } n ^ { - 1 } E [ X _ { 0 n } I _ { 0 n } ] < \infty$$

is not trivial (we don't know if it is true). The latter would be the natural hypothesis in our setting, but to make our straightforward proof technique work we make the stronger L 2 assumption (v). Also to keep matters simple, we assume ergodicity and seek only L 1 convergence.

Proposition 4 Assume (i)-(v). Then there exists a constant 0 ≤ c &lt; ∞ such that E [ | X 0 n n - c | I 0 n ] → 0 .

Proof. We compare the given process with another process in which one is allowed to use the 'bad' indices, but with high penalty. Fix large K . Define

 ̃ X ij = X ij on G i ∩ G j  ̃ X i,i +1 = K on the complement ( G i ∩ G i +1 ) c of G i ∩ G i +1  ̃ X ij undefined, otherwise.

Now define a process

$$Y _ { i j } = \min \left ( \widetilde { X } _ { i _ { 0 } , i _ { 1 } } + \widetilde { X } _ { i _ { 1 } , i _ { 2 } } + \dots + \widetilde { X } _ { i _ { m - 1 } , i _ { m } } \right ) , \\ \intertext { i m u m o r $ i = i _ { 0 } < i _ { 1 } < i _ { 2 } < \dots < i _ { m } = j $ such that each }$$

the minimum over i = i 0 &lt; i 1 &lt; i 2 &lt; . . . &lt; i m = j such that each  ̃ X i u - 1 ,i u is defined. Observe that Y ij is always defined and finite, and is subadditive. Also, because Y 01 = X 01 I 01 + K (1 - I 01 ) we have EY 01 &lt; ∞ . So we can apply Kingman's subadditive ergodic theorem to deduce there exists a constant 0 ≤ c ( K ) &lt; ∞ such that

$$\infty \text { such that } \\ E \left | \frac { Y _ { 0 n } ^ { ( K ) } } { n } \ - c ^ { ( K ) } \right | \to 0 \text { as } N \to \infty \\ \intertext { w o r w i t h e Y ( K ) \ t o e m p h as i size d e p e n d e n e \ o n \ K . }$$

where we now write Y ( K ) to emphasize dependence on K .

Note that the L 1 convergence in (14) implies

$$\delta ^ { 2 } c ^ { ( K ) } = \lim _ { n \to \infty } E [ c ^ { ( K ) } I _ { 0 n } ] = \lim _ { n \to \infty } E [ \frac { Y _ { 0 n } ^ { ( K ) } } { n } I _ { 0 n } ] .$$

Now by assumption (v) we have

$$B _ { 1 } \colon = \sup _ { n } n ^ { - 1 } E [ X _ { 0 n } I _ { 0 n } ] < \infty$$


<!-- p:13 -->


and from the definition

for which 0 ≤ c &lt; ∞ .

The essential issue is to bound the difference in (15). Fix K and n . By definition there is some path 0 = i 0 &lt; i 1 &lt; i 2 &lt; . . . &lt; i m = n for which

$$Y _ { 0 n } ^ { ( K ) } = \widetilde { X } _ { i _ { 0 } , i _ { 1 } } + \widetilde { X } _ { i _ { 1 } , i _ { 2 } } + \dots + \widetilde { X } _ { i _ { m - 1 } , i _ { m } } . \\ \ e p s \text { on the path are of the form } ( \text {for some } i )$$

Some steps on the path are of the form (for some i )

$$( i _ { u } , i _ { u + 1 } ) & = ( i , i + 1 ) \text { and } G _ { i } \cap G _ { i + 1 } \text { fails, so } \widetilde { X } _ { i _ { u } , i _ { u + 1 } } = K . \\ \text {Write } \mathcal { I } \text { for the random set of } i \text { for which this occurs (for some } i _ { u } ) , \text { and note}$$

$$Y _ { 0 n } ^ { ( K ) } \geq K | \mathcal { I } | .$$

Write I for the random set of i for which this occurs (for some i u ), and note for later use

Now consider a maximal run [ b, b ′ ] of bad events; that is, G i occurs for i = b - 1 and i = b ′ +1 but not for b ≤ i ≤ b ′ . Then the path in (16) must either use all the edges ( b - 1 , b ) , ( b, b + 1) , . . . , ( b ′ - 1 , b ′ ) , ( b ′ , b ′ + 1) or none of them. If it uses all of them, replace the path segment b - 1 → b → . . . → b ′ → b ′ +1 by the single edge b - 1 → b ′ +1, that is replace the part  ̃ X b - 1 ,b + . . . +  ̃ X b ′ ,b ′ +1 of the sum (16) by X b - 1 ,b ′ +1 . Make this replacement for each bad run touched by the path, and assume we are on G 0 ∩ G n so there are no endpoint issues. This converts (16) into a new sum

$$Z _ { 0 n } ^ { ( K ) } = X _ { j _ { 0 } , j _ { 1 } } + X _ { j _ { 1 } , j _ { 2 } } + \dots + X _ { j _ { q - 1 } , j _ { q } }$$

where all the steps are between good indices, and so by the subadditivity assumption (ii) we have

$$X _ { 0 n } \leq Z _ { 0 n } ^ { ( K ) } \, o n \, G _ { 0 } \cap G _ { n } .$$

The net effect of this conversion can be written precisely as

$$Z _ { 0 n } ^ { ( K ) } - Y _ { 0 n } ^ { ( K ) } = \sum _ { ( b , b ^ { \prime } ) \in \mathcal { B } } X _ { b - 1 , b ^ { \prime } + 1 } - K | \mathcal { I } | \text { on } G _ { 0 } \cap G _ { n }$$

$$Y _ { 0 n } ^ { ( K ) } \leq X _ { 0 n } \text { on } G _ { 0 } \cap G _ { n } .$$

So δ 2 c ( K ) ≤ B 1 . Also from the definition we see that Y ( K ) 0 n is non-decreasing in K . Hence so is c ( K ) , and so we can define the limit

$$c \colon = \lim _ { K \to \infty } c ^ { ( K ) }$$


<!-- p:14 -->


where B is the set of bad runs touched by the path. So we can bound the difference in (15) rather crudely as

$$E \left [ ( X _ { 0 n } - Y _ { 0 n } ^ { ( K ) } ) I _ { 0 n } \right ] & \leq E \left [ I _ { 0 n } \sum _ { ( b , b ^ { \prime } ) \in \mathcal { B } } X _ { b - 1 , b ^ { \prime } + 1 } \right ] .$$

Recall hypothesis (v):

$$B _ { 2 } \colon = \sup _ { m } m ^ { - 2 } E [ X _ { 0 m } ^ { 2 } I _ { 0 m } ] < \infty .$$

For 0 ≤ i, j ≤ n, j - i ≥ 2 write Λ ij for the event { ( i +1 , j - 1) ∈ B} and note Λ ij ⊂ I ij . Using the Cauchy-Schwarz inequality.

$$X _ { i j } & \subset I _ { i j } . \, \text {C} \, \text { among } \, \text {since} \, \Omega \, \text { which} . \\ & E [ 1 _ { \Lambda _ { i j } } X _ { i j } I _ { 0 n } ] \ \leq \ \sqrt { P ( \Lambda _ { i j } \cap I _ { 0 n } ) } \ \sqrt { E [ X _ { i j } ^ { 2 } I _ { i j } ] } \\ & \leq \ \sqrt { P ( \Lambda _ { i j } \cap I _ { 0 n } ) } \ \left ( j - i \right ) B _ { 2 } ^ { 1 / 2 } \\ \intertext { s o c o n d \, i n c u l a t i y . \, b y \, t h o s t a t i o n a r t y \, a s s u m p t i o n \, ( i v ) }$$

the second inequality by the stationarity assumption (iv).

Set p ij = P (Λ ij ∩ I 0 n ) and note

$$p _ { i j } \leq P ( \Lambda _ { i j } ) \leq P ( G _ { i + 1 } ^ { c } \cap \dots \cap G _ { j - 1 } ^ { c } ) = ( 1 - \delta ) ^ { j - i - 1 }$$

by assumption (iii). Because the sum in (19) can be written as ∑ ij 1 Λ ij X ij , we can combine (19) and (20) to get

$$E [ ( X _ { 0 n } - Y _ { 0 n } ^ { ( K ) } ) I _ { 0 n } ] \leq B _ { 2 } ^ { 1 / 2 } \sum _ { i = 0 } ^ { n - 2 } \sum _ { j = i + 2 } ^ { n } ( j - i ) p _ { i j } ^ { 1 / 2 } .$$

Now consider the double sum above with p 1 / 2 ij replaced by p ij . That is, consider

$$\text {consider} \\ \sum _ { i = 0 } ^ { n - 2 } \sum _ { j = i + 2 } ^ { n } ( j - i ) p _ { i j } \ = \ E I _ { 0 n } \sum _ { i = 0 } ^ { n - 2 } \sum _ { j = i + 2 } ^ { n } ( j - i ) 1 _ { \Lambda _ { i j } } \\ \ = \ E I _ { 0 n } | \mathcal { I } | \text { for the random set } \mathcal { I } \text { in } ( 1 7 ) \\ \leq \ K ^ { - 1 } E I _ { 0 n } Y _ { 0 n } ^ { ( K ) } \text { by } ( 1 7 ) \\ \leq \ K ^ { - 1 } E I _ { 0 n } X _ { 0 n } \text { by } ( 1 5 ) \\ \leq \ B _ { 1 } n / K .$$


<!-- p:15 -->


Now an elementary inequality (stated and proved as Lemma 5 below) bounds the right side of (21) in terms of the left side of (22). Combining this inequality with (21,23) gives: for any J ≥ 2,

$$B _ { 2 } ^ { 1 / 2 } n ^ { - 1 } E [ ( X _ { 0 n } - Y _ { 0 n } ^ { ( K ) } ) I _ { 0 n } ] \leq \sum _ { j = J + 1 } ^ { \infty } j ( 1 - \delta ) ^ { ( j - 1 ) / 2 } \ + \ J \sqrt { B _ { 1 } / K } .$$

Taking J = K 1 / 2 we see

$$\lim _ { K \to \infty } \sup _ { n } n ^ { - 1 } E [ ( X _ { 0 n } - Y _ { 0 n } ^ { ( K ) } ) I _ { 0 n } ] = 0$$

which by the L 1 convergence (14) and the inequality (15) implies

$$\lim _ { K \to \infty } \lim _ { n } \sup _ { n } E [ | n ^ { - 1 } X _ { 0 n } - c ^ { ( K ) } | I _ { 0 n } ] = 0$$

establishing Proposition 4 for c = lim K →∞ c ( K ) which was previously shown to be finite.

Lemma 5 Let 0 &lt; η &lt; 1 and let ( p ij , 0 ≤ i, j ≤ n, j - i ≥ 2) be constants such that 0 ≤ p ij ≤ η j - i - 1 . Then for any J ≥ 2

$$3 a c t \ t a t { 0 } ^ { 0 } \stackrel { - p _ { i j } } { \sim } & \eta ^ { - 1 } j \stackrel { n - 2 } { \sim } 2 ^ { n } \\ n ^ { - 1 } \sum _ { i = 0 } ^ { n - 2 } \sum _ { j = i + 2 } ^ { n } ( j - i ) p _ { i j } ^ { 1 / 2 } \leq \sum _ { j = J + 1 } ^ { \infty } j \eta ^ { ( j - 1 ) / 2 } \, + \, J n ^ { - 1 / 2 } \sqrt { \sum _ { i = 0 } ^ { n - 2 } \sum _ { j = i + 2 } ^ { n } ( j - i ) p _ { i j } } . \\ \intertext { b r o f $ \ F i j $ and $ o t $ a s }$$

Proof. Fix i and set q j = p i,i + j for 2 ≤ j ≤ n - i . Then

$$\sum _ { j = 2 } ^ { n - i } j q _ { j } ^ { 1 / 2 } \ & \leq \ \sum _ { j = J + 1 } ^ { \infty } j \eta ^ { ( j - 1 ) / 2 } + \sum _ { j = 2 } ^ { J } j q _ { j } ^ { 1 / 2 } \\ & \leq \ \sum _ { j = J + 1 } ^ { \infty } j \eta ^ { ( j - 1 ) / 2 } + J \sqrt { \sum _ { j = 2 } ^ { J } j q _ { j } } \\ \text {caych-Schwarz inequality} \ \ & \text {setting } d _ { i } = \sum _ { j = 1 } ^ { J } j q _ { i } , \text { and}$$

by the Cauchy-Schwarz inequality. Setting d i = ∑ J j =2 jq j , another use of Cauchy-Schwarz gives

$$\sum _ { i = 0 } ^ { n - 2 } \sqrt { d _ { i } } \leq n ^ { 1 / 2 } \sqrt { \sum _ { i = 0 } ^ { n - 2 } d _ { i } }$$

and the result follows.


<!-- p:16 -->
