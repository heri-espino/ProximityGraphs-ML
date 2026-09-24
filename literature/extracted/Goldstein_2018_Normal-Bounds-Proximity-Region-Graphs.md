---
id: "Goldstein_2018_Normal-Bounds-Proximity-Region-Graphs"
source_pdf: "../pdf/Goldstein_2018_Normal-Bounds-Proximity-Region-Graphs.pdf"
source_filename: "Goldstein_2018_Normal-Bounds-Proximity-Region-Graphs.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "good"
extraction_score: 90.0
visual_assets: "disabled"
references_file: "../references/Goldstein_2018_Normal-Bounds-Proximity-Region-Graphs.references.md"
---

<!-- p:1 -->

[Available online at www.sciencedirect.com](http://www.elsevier.com/locate/spa)

### ScienceDirect

[Stochastic Processes and their Applications 128 (2018) 1208-1237](http://dx.doi.org/10.1016/j.spa.2017.07.002)

## Bounds to the normal for proximity region graphs

Larry Goldstein a , Tobias Johnson a , Raphaël Lachièze-Rey b, ∗

a University of Southern California, United States

b Université Paris Descartes, Sorbonne Paris Cité, France

Received 7 July 2016; received in revised form 10 April 2017; accepted 5 July 2017 Available online 13 July 2017

####### Abstract

In a proximity region graph G in R d , two distinct points x , y of a point process μ are connected when the 'forbidden region' S ( x , y ) these points determine has empty intersection with μ . The Gabriel graph, where S ( x , y ) is the open disk with diameter the line segment connecting x and y , is one canonical example. When μ is a Poisson or binomial process, under broad conditions on the regions S ( x , y ), bounds on the Kolmogorov and Wasserstein distances to the normal are produced for functionals of G , including the total number of edges and the total length. Variance lower bounds, not requiring strong stabilization, are also proven to hold for a class of such functionals.

c ⃝ 2017 Elsevier B.V. All rights reserved.

MSC:

60D05; 52A22; 60F05

Keywords: Forbidden region graph; Berry-Esseen bounds; Stabilization; Poisson functionals

### 1. Introduction

The family of graphs that we study here, all with vertex sets given by a locally finite point process μ in R d , is motivated by two canonical examples considered in [1], the Gabriel graph and the relative neighborhood graph. Two distinct points x and y of μ are connected by an edge in the Gabriel graph if and only if there does not exist any point z of the process μ lying in the open disk whose diameter is the line segment connecting x and y . The relative neighborhood graph has an edge between x and y if and only if there does not exist a point z of μ such that

$$\max ( \| x - z \| , \| z - y \| ) < \| x - y \| ,$$

∗ Corresponding author.

E-mail address:

[raphael.lachieze-rey@parisdescartes.fr (R. Lachi` eze-Rey).](mailto:raphael.lachieze-rey@parisdescartes.fr)


<!-- p:2 -->


that is, if and only if there is no point z of μ that is closer to either x or y than these points are to each other.

These two examples are special cases of 'proximity graphs' as defined in [3], where distinct points x and y of μ are connected if and only if a region S ( x , y ) determined by x and y contains no points of μ , that is, when μ ∩ S ( x , y ) = ∅ . As S ( x , y ) must be free of points of μ in order for x and y to be joined, we call S ( x , y ) the 'forbidden region' determined by x and y . In particular, with B ( x , r ) and B o ( x , r ) denoting the closed and open ball of radius r centered at x , respectively, the forbidden regions of the Gabriel graph are given by

$$S ( x , y ) = B ^ { \varphi } ( ( x + y ) / 2 , \| y - x \| / 2 ) ,$$

and those of the relative neighborhood graph by

$$S ( x , y ) = B ^ { o } ( x , \| y - x \| ) \cap B ^ { o } ( y , \| x - y \| ) .$$

It is easy to check that the forbidden regions S ( x , y ) of the Gabriel graph are contained in those of the relative neighbor graph, and hence edges of latter are also edges of former.

We refer to the graphs formed in this manner also as 'forbidden region graphs'. Indeed, when coining the label 'proximity graphs' in [3], one reads that 'this term could be misleading in some cases'. Indeed, forbidden region graphs may depend on 'non-proximate' information, such as the graph considered in Example 5 of [3], whose forbidden region S ( x , y ) is the infinite strip bounded by the two parallel hyperplanes containing x and y , each perpendicular to y - x . Allowing forbidden regions to depend on larger sets of points and to be determined by more complex rules yield well studied graphs with additional structure, including the Minimum Spanning Tree and the Delaunay triangulation, see [1].

For a forbidden region graph G and a Poisson or binomial point process μ in some bounded measurable 'viewing window' denoted X in the sequel, ensuring that the graph and functional L ( μ ) in (3) are finite, we study the distribution of

$$L ( \mu ) = \sum _ { \{ x , y \} \in \mu , x \neq y } \mathbf 1 ( \mu \cap S ( x , y ) = \emptyset ) \psi ( x , y ) ,$$

for some ψ : R d × R d → R satisfying ψ ( x , y ) = ψ ( y , x ). For instance, taking ψ ( x , y ) = ∥ x - y ∥ α for some α ≥ 0, for α = 0 and α = 1 the value of L ( μ ) is the number of edges and the total length of G , respectively.

Recall that the Kolmogorov distance between random variables U and V is defined as

$$d _ { K } ( U , V ) = \sup _ { t \in \mathbb { R } } | \mathbb { P } ( U \leqslant t ) - \mathbb { P } ( V \leqslant t ) | \, ,$$

and the Wasserstein distance as

$$d _ { W } ( U , V ) = \sup _ { h \in L i p _ { 1 } } | \mathbb { E } [ h ( U ) - h ( V ) ] | \, ,$$

where Lip 1 stands for the class of 1-Lipschitz functions R → R . Theorem 2, our main result, is a bound on the normal approximation of L in d ( · , · ), denoting either the Wasserstein or Kolmogorov metric, that holds under broad conditions on the forbidden regions and underlying point process. Its immediate corollary, in conjunction with the variance lower bound of Theorem 4, provides the following result for the two motivating examples just introduced.

Corollary 1. Let X = B (0 , 1) , and suppose that η t is either a Poisson process with intensity t on X , or a binomial process of t independent and uniformly distributed points on X , and let Ft := L ( η t ) for t ≥ 1 , where L ( · ) is given in (3) with ψ ( x , y ) = ∥ x - y ∥ α for some α ≥ 0 . Then for the Gabriel graph and the relative neighborhood graph, there exists a constant C &gt; 0 such that


<!-- p:3 -->


$$d ( \widetilde { F } _ { t } , N ) \leq C t ^ { - 1 / 2 } \ \ f o r \ a l l t \geq 1 ,$$

where  ̃ Ft = ( Ft - E Ft ) / √ Var Ft , and N is a standard Gaussian.

Proximity graphs arise frequently in stochastic geometry, especially for their use in communication networks, see [1,3,10,11] and references therein. For most models, first and second order limit theorems were already known from the theory of stabilizing functionals (see [10,11]), but obtaining optimal speed of convergence and confidence intervals remained open. With Poisson input, the general results available only give a non-optimal rate of convergence, while the speed obtained here is typically optimal for stationary stabilizing functions. For integer-valued functionals like the number of edges, the methods of [4] imply the rate here is optimal whenever the rates of upper and lower variance bounds agree. Only recently was an optimal rate of convergence established for any geometric functional with non-deterministic range of interaction, when [8] did so for statistics of the nearest neighbor graph and of the Poisson-Voronoi tessellation. Furthermore, those results are only valid with Poisson input, whereas ours also hold for binomial input. In general, with binomial input there are few preexisting results on geometric functionals as considered here. Though one can most likely derive asymptotic normality from [10], no speed of convergence was available at all for the models considered in this paper. See [6] for an optimal speed for the Boolean model, where the interaction range is bounded. Chatterjee also gives a slower power law decay for some nearest-neighbor statistics in [2]. Our paper is the first example of an optimal speed of convergence for geometric functionals with possibly complex dependency structure between points, and no prior bound on the speed of convergence, when the input consists of n i.i.d. points uniformly distributed in a square of volume n .

In our consideration of more general graphs, we will assume that the collection of forbidden regions { S ( x , y ) : { x , y } ⊆ R d , x ̸= y } consists of nonempty measurable subsets of R d that are symmetric in that

$$S ( x , y ) = S ( y , x ) \quad \text {for all } \{ x , y \} \subseteq \mathbb { R } ^ { d } , x \neq y .$$

Nonsymmetric sets S ( x , y ) would be natural for the construction of directed forbidden region graphs, and though we do not consider them here our methods would apply. With S denoting the closure of a set S ⊆ R d , we assume also that

$$\{ x , y \} \subseteq S ( x , y ) \ \ S ( x , y ) ,$$

and that the normalized diameter D of the collection of forbidden regions is finite, that is,

$$\mathcal { D } < \infty \quad \text {where} \quad \mathcal { D } = \sup \left \{ \frac { \| s - t \| } { \| x - y \| } \, \colon \{ s , t \} \subseteq S ( x , y ) , \{ x , y \} \subseteq \mathbb { R } ^ { d } , x \neq y \right \} .$$

Assumption A below requires that as x and y become farther apart, the forbidden regions S ( x , y ) contain increasingly large balls. This is to avoid pathological cases such as when the forbidden regions have empty interior and negligible boundary, in which case the graph determined by a Poisson or binomial input process with an absolutely continuous intensity measure is the complete graph almost surely. In Assumptions A and B and Theorem 2, X will denote a window specified by a given bounded measurable subset of R d .


<!-- p:4 -->


Assumption A ( Scaled Ball Condition ) . For some δ &gt; 0 and window X , it holds for all { x , y } ⊆ X that S ( x , y ) ∩ X contains a ball of radius δ ∥ x - y ∥ .

With some slight abuse of notation, |·| will be used to denote both the Lebesgue measure of a measurable subset of R d and also cardinality of a finite set; use will be clear from context. Our results below provide bounds on the normal approximation of L in (3) when the underlying graph is generated by a point process η t , t &gt; 0 that satisfies the following conditions.

Assumption B. Let λ be a probability measure on X satisfying

$$c _ { \lambda } | B | \leq \lambda ( B ) \leq b _ { \lambda } | B | \quad \text {for all measurable $B \subseteq \mathbb{X}$}$$

for some 0 &lt; c λ ≤ b λ . The point process η t is either a Poisson process P t on X with intensity λ t = t λ, t &gt; 0, or a binomial process U t consisting of a set of i.i.d. variables X 1 , . . . , Xt with common distribution λ , for t ∈ N .

Lastly, we require the following variance lower bound.

Assumption C. For α ⩾ 0, there exists vα &gt; 0 such that

$$\text {Var} \, L ( \eta _ { t } ) \geq v _ { \alpha } t ^ { 1 - 2 \alpha / d } \quad \text {for all} \, t \geq 1 .$$

Assumption C is a serious one, and we separately address the question of when it is satisfied in Section 4, see Theorem 4.

We inform the reader that the C that appears in our bounds denotes a positive constant that may not be the same at each occurrence.

Theorem 2. For a given window X , let { S ( x , y ) : x , y ∈ X , x ̸= y } be a collection of forbidden regions satisfying (4) - (6) , and let Assumption A hold. Let η t be a point process on X satisfying Assumption B , and let

Ft := L ( η t ) , for t ≥ 1 ,

where L ( · ) is given in (3) , where for some C &gt; 0 and α ≥ 0 we have | ψ ( x , y ) | ≤ C ∥ x - y ∥ α for all { x , y } ⊆ R d .

If Assumption C holds, then with d ( · , · ) denoting either the Wasserstein or Kolmogorov distance, there exists a constant C not depending on t such that

$$d ( \widetilde { F } _ { t } , N ) \leq C t ^ { - 1 / 2 } \ \ f o r \ a l l \ t \geq 1 ,$$

where  ̃ Ft = ( Ft - E Ft ) / √ Var Ft , and N is a standard Gaussian.

Theorem 2 is based on the methods of [8], in particular on second order Poincar ́ e inequalities, and also the key notion of stabilization. To define stabilization, let f ( μ ) be a function of a point process μ in R d . For x ∈ R d consider the difference (or derivative) at x given by

$$D _ { x } f ( \mu ) = f ( \mu \cup \{ x \} ) - f ( \mu ) ,$$

which is the amount that f changes upon the insertion of the point x into μ . Higher order differences are defined iteratively, for instance D 2 x , y f ( μ ) = Dx ( Dy f ( μ )), so

$$D _ { x , y } ^ { 2 } f ( \mu ) = f ( \mu \cup \{ x , y \} ) - f ( \mu \cup \{ y \} ) - f ( \mu \cup \{ x \} ) + f ( \mu ) .$$


<!-- p:5 -->


There are a number of related notions of a stabilization radius for a functional f . The one we will use is a radius R ( x ; μ ) such that

$$D _ { x , y } ^ { 2 } f ( \mu ) = 0 \quad \text {if } \| y - x \| > R ( x ; \mu ) .$$

We say in this case that R ( x ; μ ) is a stabilization radius for f around x .

When dealing with a function of a Poisson process P t with growing intensity λ t , one key condition from [8] required to obtain bounds to the normal for a properly standardized functional f is that over the observation window X ,

$$\sup _ { x \in \mathbb { X } , \overline { x } \geq 1 } \int \mathbb { P } ( D _ { x , y } ^ { 2 } f ( \mathcal { P } _ { t } ) \neq 0 ) ^ { a } \lambda _ { t } ( d y ) < \infty ,$$

for a some small number, depending on low moments of the derivatives of f . If there exists a stabilization radius for f that is small with sufficiently high probability, then (10) holds. In Section 2, we construct such a radius and prove that it exhibits exponential decay under very weak conditions on the forbidden regions.

We now address Assumption C in Theorem 2, the lower bound on Var L ( η t ). Penrose and Yukich give a general lower bound for the variance of Poisson and binomial statistics in [10]. Their result requires a statistic to be strongly stabilized . (This notion of stabilization is also referred to as stabilization for add-one cost or as external stabilization-see [11] for a general survey.) We cannot apply this result because our statistic L is not strongly stabilized unless we impose additional constraints on the forbidden regions, such as requiring them to be convex. Another possible approach would be to use the results of [8, Section 5]. These are applicable to L , but only for the easier case of Poisson input. We are thus forced to give a new argument to prove that Assumption C holds in some generality. We state Assumption D, an additional technical condition required, followed by Theorem 4, providing sufficient conditions for Assumption C. For a simple statement we restrict ourselves to the regular isotropic case as specified by Definition 3, but a more general result can be formulated on conditions that make the expectation (53) zero. Let ∂ B denote the boundary of a set B ⊆ R d .

Assumption D. For all { w, z } ⊆ B (0 , 1) there exists y ∈ ∂ S ( w, z ) such that z ̸∈ ∂ S ( w, y ) and w ̸∈ ∂ S ( z , y ). We furthermore assume that the choice ( w, z ) ↦→ y ∈ ∂ S ( w, z ) can be made in a measurable way.

To state the variance lower bound, we work in a setup where the forbidden region S ( x , y ) is given by a template shifted and scaled according to x and y .

Definition 3 ( Regular Isotropic Family ) . Let S ⊆ R d be a bounded, measurable set symmetric around an axis given by a unit vector u 0 ∈ R d ; that is, any rotation leaving u 0 invariant also leaves S invariant. Assume that rotations taking u 0 to - u 0 leave S fi xed and that { u 0 , - u 0 } ⊆ 2( S \ S ). Also assume that S contains an open ball and has negligible boundary.

Given x , y ∈ R d with x ̸= y , let ρ xy be the rotation transforming u 0 into ( x - y ) / ∥ x - y ∥ and leaving invariant the orthogonal complement of the space spanned by { u 0 , x - y } . Then, define

$$S ( x , y ) = ( x + y ) / 2 + \| x - y \| \rho _ { x y } ( S ) .$$

We call the resulting collection of forbidden regions a regular ( S , u 0) isotropic family .

Because S is symmetric around u 0, we could have taken ρ xy to be any rotation transforming u 0 into ( x - y ) / ∥ x - y ∥ without affecting the final definition of S ( x , y ). Indeed, if ρ and ρ ′


<!-- p:6 -->


are any two rotations transforming u 0 into ( x - y ) / ∥ x - y ∥ , then the rotation ρ - 1 ρ ′ leaves u 0 invariant and hence also leaves S invariant. Thus ρ ′ ( S ) = ρρ - 1 ( ρ ′ ( S )) = ρ ( S ). We also mention that in R 2 , the vector u 0 is irrelevant and S need not have any rotational invariance, since the only rotation leaving u 0 invariant is the identity, which necessarily leaves S invariant as well.

One should think of S ( x , y ) in a regular ( S , u 0) isotropic family as being generated by translating S to the midpoint of x and y , then rotating S according to the orientation of x and y , and then scaling S according to the distance between x and y . Our assumptions that rotations taking u 0 to - u 0 leave S fi xed and that { u 0 , - u 0 } ⊆ 2( S \ S ) ensure that the family satisfies properties (4) and (5). Later in this introduction, we will show that the forbidden regions of our two canonical examples, the Gabriel graph and the relative neighborhood graph, are regular isotropic families.

Theorem 4. Suppose the forbidden regions { S ( x , y ) : { x , y } ⊆ R d , x ̸= y } form a regular ( S , u 0) isotropic family and satisfy Assumption D . Assume further that the scaled ball condition, Assumption A , is satisfied with the role of X played by t 1 / d X ∩ B ( x , r ) for a fixed δ &gt; 0 for any t and r, that X is star shaped with star center at the origin, and that it contains an open set around the origin. For the function ψ in the definition (3) of L, assume

- ψ ( ax , ay ) = a α ψ ( x , y ) for all a &gt; 0 and { x , y } ⊆ R d
- ψ ( x , y ) ̸= 0 for all x ̸= y
- ψ ( x , y ) is continuous on R d × R d .

Then there is a constant vα &gt; 0 such that Assumption C holds when η t is either a homogeneous Poisson process on X with intensity t or a binomial point process of t independent and uniformly distributed points on X .

We end this section by introducing some additional terminology about forbidden regions and regular isotropic families. As already stated, the graph with vertex set a locally finite point configuration μ in R d is the S ( x , y ) forbidden region graph on μ when an edge exists between points x and y of μ if and only if x ̸= y and S ( x , y ) ∩ μ = ∅ . That is, we connect points x and y of μ if and only if they are distinct, and there are no points of μ lying in the forbidden region S ( x , y ) that these two points generate. Hence, for x ∈ μ , the set of edges G S ( x ; μ ) incident to x in μ , and the edge set G S ( μ ) of the forbidden region graph are given, respectively, by

$$\mathcal { G } _ { S } ( x ; \mu ) & = \{ x , y \} \colon \{ x , y \} \subseteq \mu , x \neq y , S ( x , y ) \cap \mu = \emptyset \} \quad \text {and} \\ \mathcal { G } _ { S } ( \mu ) & = \bigcup _ { x \in \mu } \mathcal { G } _ { S } ( x ; \mu ) .$$

We may drop the subscript when the dependence on S is clear from context.

We call a collection S ( x , y ) of forbidden regions translation invariant when

$$S ( x + z , y + z ) = S ( x , y ) + z \quad \text {for all } \{ x , y , z \} \subseteq \mathbb { R } ^ { d } , x \neq y ,$$

and we observe that a regular isotropic family is always translation invariant. The normalized diameter (6) for a regular ( S , u 0) isotropic family is given by

$$\mathcal { D } = \sup \{ \| y - x \| \, \colon \{ x , y \} \subseteq S \} .$$

Our two canonical examples, the Gabriel graph and the relative neighborhood graph, are both regular isotropic families. With u 0 = (1 , 0 , . . . , 0), the Gabriel graph is obtained by setting S = B o (0 , 1 / 2), and the relative neighborhood graph by S = B o ( u 0 / 2 , 1) ∩ B o ( - u 0 / 2 , 1). For the Gabriel graph, we then have

$$S ( x , y ) = ( x + y ) / 2 + \| x - y \| \rho _ { x y } \left ( B ^ { o } ( 0 , 1 / 2 ) \right ) = ( x + y ) / 2 + \| x - y \| B ^ { o } ( 0 , 1 / 2 ) ,$$


<!-- p:7 -->


which agrees with (1). Rotating the template S given above for the relative neighborhood graph, we have

$$\rho _ { x y } ( S ) = B ^ { o } \left ( ( x - y ) / 2 \| x - y \| , 1 \right ) \cap B ^ { o } \left ( ( y - x ) / 2 \| y - x \| , 1 \right ) ,$$

which yields

$$S ( x , y ) & = ( x + y ) / 2 + \| x - y \| \rho _ { x , y } ( S ) \\ & = ( x + y ) / 2 + B ^ { o } ( ( x - y ) / 2 , \| x - y \| ) \cap B ^ { o } ( ( y - x ) / 2 , \| y - x \| ) \\ & = B ^ { o } ( x , \| y - x \| ) \cap B ^ { o } ( y , \| x - y \| ) ,$$

agreeing with (2).

### 2. Radius of stabilization

We begin this section by constructing a set in (12) that will serve as a stabilizing region about a point x ∈ R d , or more generally around a subset U ⊆ R d . Our radius RS ( U ; μ ; X ) is then constructed in (14) in terms of this set. We prove in Lemma 5 that RS ( U ; μ ; X ) is monotone in μ , and in Lemma 7 that it is a stabilization radius for L around x as defined in (9). In Proposition 9, we show that the stabilization radius has exponentially decaying tails with standard Poisson or binomial input under Assumption A, the scaled ball condition, on the forbidden regions. We remind the reader that X ⊆ R d is a bounded measurable window.

For U ⊆ R d , let

$$\mathcal { R } _ { S } ( U ; \mu ; \mathbb { K } ) \\ = \bigcup \{ S ( w , z ) \colon \{ w , z \} \subseteq \mathbb { X } \text { such that } S ( w , z ) \cap \mu = \emptyset \text { and } U \cap \overline { S ( w , z ) } \neq \emptyset \} .$$

Intuitively, this set consists of all forbidden regions affected by the addition of a point somewhere in U . The most important case for us is U = { x } , which we write as R S ( x ; μ ; X ).

First, we show R S ( U ; μ ; X ) satisfies a monotonicity property in μ .

Lemma 5. If μ ⊆ ν , then

$$\mathcal { R } _ { S } ( U ; v ; \mathbb { X } ) \subseteq \mathcal { R } _ { S } ( U ; \mu ; \mathbb { X } ) ,$$

with equality if ν \ μ lies outside of R S ( U ; μ ; X ) .

Proof. Suppose that S ( w, z ) satisfies S ( w, z ) ∩ ν = ∅ and U ∩ S ( w, z ) ̸= ∅ . Then this forbidden region also satisfies S ( w, z ) ∩ μ = ∅ , showing that R S ( U ; ν ; X ) ⊆ R S ( U ; μ ; X ).

Now, assume that ν \ μ lies outside of R S ( U ; μ ; X ). Suppose that S ( w, z ) satisfies S ( w, z ) ∩ μ = ∅ and U ∩ S ( w, z ) ̸= ∅ . Then S ( w, z ) ⊆ R S ( U ; μ ; X ), and hence μ = ν on S ( w, z ). This implies that S ( w, z ) ∩ ν = ∅ , which means that S ( w, z ) ⊆ R S ( U ; ν ; X ). Therefore R S ( U ; μ ; X ) ⊆ R S ( U ; ν ; X ), proving the two sets equal. □

Now we consider the relation between R S ( U ; μ ; X ) and the graphs G ( μ ) and G ( μ ∪{ x } ). Let E + x ( μ ) denote the edges found in G ( μ ∪ { x } ) but not in G ( μ ), and let E - x ( μ ) denote the edges found in G ( μ ) but not in G ( μ ∪ { x } ), that is

$$E _ { x } ^ { + } ( \mu ) = \mathcal { G } ( \mu \cup \{ x \} ) \ \mathcal { G } ( \mu ) \quad \text {and} \quad E _ { x } ^ { - } ( \mu ) = \mathcal { G } ( \mu ) \ \mathcal { G } ( \mu \cup \{ x \} ) .$$

Lemma 6. Suppose that μ and ν are supported on some bounded measurable windows X 1 and X 2 , respectively, and that U ⊆ X 1 ∩ X 2 . If R S ( U ; μ ; X 1) = R S ( U ; ν ; X 2) and μ and ν agree on the closure of this set, then E ± x ( μ ) = E ± x ( ν ) for any x ∈ U.


<!-- p:8 -->


Proof. Suppose that x ∈ U and { x , y } ∈ E + x ( μ ). Then, by { x , y } ⊆ X 1, S ( x , y ) ∩ μ = ∅ and (5), we have S ( x , y ) ⊆ R S ( U ; μ ; X 1) = R S ( U ; ν ; X 2). Again by (5) the closure of this set contains y , and μ and ν agree on it. Thus y ∈ ν and S ( x , y ) ∩ ν = ∅ , implying that { x , y } ∈ E + x ( ν ). Therefore E + x ( μ ) ⊆ E + x ( ν ). By symmetry, the opposite inclusion holds as well.

Now suppose that x ∈ U and { w, z } ∈ E - x ( μ ). As { w, z } ∈ G ( μ ) we have { w, z } ⊆ X 1 and S ( w, z ) ∩ μ = ∅ , and as { w, z } ̸∈ G ( μ ∪ { x } ) we must have x ∈ S ( w, z ), so that U ∩ S ( w, z ) ⊇ { x } ̸= ∅ . Hence S ( w, z ) ⊆ R S ( U ; μ ; X 1), and so is also a subset of R S ( U ; ν ; X 2). As ν agrees with μ on the closure of this set we have { w, z } ⊆ X 2 and S ( w, z ) ∩ ν = ∅ , so { w, z } ∈ G ( ν ). As { w, z } ̸∈ G ( μ ∪ { x } ) we have x ∈ S ( w, z ), and therefore S ( w, z ) ∩ ( ν ∪ { x } ) = { x } . Hence { w, z } ̸∈ G ( ν ∪ { x } ), showing E - x ( μ ) ⊆ E - x ( ν ). By symmetry, the opposite inclusion also holds. □

Next, for U ⊆ X and μ supported on X , define

$$R _ { S } ( U ; \mu ; \mathbb { X } ) = \sup \{ \| y - x \| \, \colon y \in \mathcal { R } _ { S } ( U ; \mu ; \mathbb { X } ) , \, x \in U \} ,$$

writing this quantity as RS ( x ; μ ; X ) if U = { x } . The next lemma shows that RS ( x ; μ ; X ) is a stabilization radius.

Lemma 7. The radius RS ( U ; μ ; X ) given in (14) is stabilizing in the sense of (9) for L ( μ ) , the statistic defined in (3) . That is,

D 2 x , y L ( μ ) = 0 for all { x , y } ⊆ X with x ∈ U and ∥ y - x ∥ &gt; RS ( U ; μ ; X ) . .

Furthermore, for x ∈ U and { x 1 , . . . , xn } ⊆ X satisfying ∥ xi - x ∥ &gt; RS ( U ; μ ; X ) ,

$$D _ { x } L ( \mu ) = D _ { x } L ( \mu \cup \{ x _ { 1 } , \dots , x _ { n } \} ) .$$

Proof. Assume that x ∈ U and ∥ y - x ∥ &gt; RS ( U ; μ ; X ). We need to show that Dx L ( μ ∪{ y } ) = Dx L ( μ ). To do so, we will show that E ± x ( μ ∪ { y } ) = E ± x ( μ ). Since ∥ y - x ∥ &gt; RS ( U ; μ ; X ), the point y lies outside of R S ( U ; μ ; X ). By Lemma 5, R S ( U ; μ ∪ { y }; X ) = R S ( U ; μ ; X ). On the closure of this set, μ and μ ∪ { y } agree, and so applying Lemma 6 with ν = μ ∪ { y } and X 1 = X 2 = X yields the first conclusion.

Now, we will repeatedly apply this first conclusion to establish (15). Applying it once shows that since ∥ x 1 - x ∥ &gt; RS ( U ; μ ; X ),

Dx L ( μ ) = Dx L ( μ ∪ { x 1 } ) .

By Lemma 5, we have RS ( U ; μ ∪ { x 1 }; X ) ≤ RS ( U ; μ ; X ). Thus applying the first claim again yields

$$D _ { x } L ( \mu \cup \{ x _ { 1 } \} ) = D _ { x } L ( \mu \cup \{ x _ { 1 } , x _ { 2 } \} ) .$$

Repeating this argument proves (15). □

To prove that our stabilization radius has exponential tails under Poisson or binomial input, the rough idea is that if the stabilization radius is large, then there must be a large ball empty of points of μ .

Lemma 8. Assume that X and the collection of forbidden regions S ( x , y ) satisfy the scaled ball condition (Assumption A ) with δ &gt; 0 , and let μ be supported on X . If for some u ∈ X , r ≥ 0 and 0 &lt; r 1 &lt; r 2 we have B ( u , r ) ⊆ X and 0 &lt; r 1 &lt; RS ( B ( u , r ) ; μ ; X ) ≤ r 2 , then with D the normalized diameter in (6) , there exists a ball of radius ( r 1 - 2 r ) δ/ D lying within B ( u , r 2) ∩ X that contains no points of μ .


<!-- p:9 -->


Proof. Since RS ( B ( u , r ) ; μ ; X ) &gt; r 1, there exist { w, z } ⊆ X such that

- S ( w, z ) contains no points of μ ;
- S ( w, z ) contains some point of B ( u , r );
- and there exists y ∈ S ( w, z ) and x ∈ B ( u , r ) with ∥ y - x ∥ &gt; r 1.

The diameter of S ( w, z ) is then greater than r 1 - 2 r by the triangle inequality, and by the definition of the normalized diameter D , we have ∥ z - w ∥ &gt; ( r 1 - 2 r ) / D . By the scaled ball condition, S ( w, z ) ∩ X contains a ball of radius δ ( r 1 - 2 r ) / D . Since RS ( B ( u , r ) ; μ ; X ) ≤ r 2, the set S ( w, z ) is contained within B ( u , r 2) (in fact, it is contained in B ( u , r 2 - r ), but we will not need this fact), and so the ball is also contained within B ( u , r 2) ∩ X . By virtue of being a subset of S ( w, z ), the ball contains no points of μ . □

Using Lemma 8 we now show our stabilization radius has exponential tails.

Proposition 9. If the scaled ball condition (Assumption A ) holds for δ &gt; 0 , and η t satisfies Assumption B with c λ &gt; 0 , then for any x ∈ X , 0 ≤ ε &lt; 1 / 2 and r such that B ( x , ε r ) ⊆ X ,

$$\mathbb { P } ( R _ { S } ( B ( x , \epsilon r ) ; \eta _ { t } ; \mathbb { X } ) \geq r ) \leq C ( 1 - 2 \epsilon ) ^ { - d } \exp ( - c _ { \lambda } \kappa t r ^ { d } ) \ \ f o r \ a l l \ r > 0$$

with κ = ((1 - 2 ε ) δ/ D √ d ) d , and C a constant that depends only on d, D , and δ . In particular,

$$\mathbb { P } ( R _ { S } ( x ; \eta _ { t } ; \mathbb { X } ) \geq r ) \leq C \exp ( - c _ { \lambda } \kappa t r ^ { d } ) \ \ f o r \, a l l \, r > 0 .$$

Proof. Let π d be the volume of the d -dimensional ball of radius 1. First, we show that for any s &gt; 0 and 0 ≤ ε &lt; 1 / 2,

$$\mathbb { P } [ s < R _ { S } ( B ( x , \epsilon s ) ; \mu ; \mathbb { X } ) \leq 2 s ] \leq \left ( \frac { 2 \mathcal { D } \sqrt { d } } { ( 1 - 2 \epsilon ) \delta } \right ) ^ { d } \pi _ { d } \exp ( - c _ { \lambda } \kappa t s ^ { d } ) .$$

To prove this claim, suppose that s &lt; RS ( B ( x , ε s ) ; μ ; X ) ≤ 2 s and apply Lemma 8 to conclude that there exists a ball of radius (1 - 2 ε ) δ s / D within B ( x , 2 s ) ∩ X containing no points of μ . Now, consider the lattice ((1 - 2 ε ) δ sd - 1 / 2 / D ) Z d . By a volume argument, B ( x , 2 s ) ∩ X contains at most

$$\frac { | B ( 0 , 2 s ) | } { ( ( 1 - 2 \epsilon ) \delta s d ^ { - 1 / 2 } / \mathcal { D } ) ^ { d } } = \left ( \frac { 2 \mathcal { D } \sqrt { d } } { ( 1 - 2 \epsilon ) \delta } \right ) ^ { d } \pi _ { d }$$

lattice cells. Any ball of radius (1 - 2 ε ) δ s / D contains a cell of this lattice.

In all, we have shown that if s &lt; RS ( B ( x , ε s ) ; μ ; X ) ≤ 2 s , then at least one of the at most (2 D √ d / (1 - 2 ε ) δ ) d π d lattice cells within B ( x , 2 s ) ∩ X contains no point of μ . With binomial input, applying Assumption B, the probability of a single cell being empty is bounded by

$$\left [ 1 - c _ { \lambda } \left ( \frac { ( 1 - 2 \epsilon ) \delta } { \mathcal { D } \sqrt { d } } \right ) ^ { d } s ^ { d } \right ] ^ { t } \leq \exp \left [ - c _ { \lambda } \left ( \frac { ( 1 - 2 \epsilon ) \delta } { \mathcal { D } \sqrt { d } } \right ) ^ { d } t s ^ { d } \right ] .$$

With Poisson input, each lattice cell contains no point of μ with probability at most the right hand side of (19). A union bound now proves (18).

Now consider r &gt; 0, arbitrary. If exp ( - c λκ tr d ) &gt; 1 / 2, then (16) is trivially satisfied with C = 2. Otherwise, applying a union bound using (18) with s = r , 2 r , 4 r , . . . gives

$$\mathbb { P } [ R _ { S } ( B ( x , \epsilon r ) ; \mu ; \mathbb { X } ) > r ] \leq \left ( \frac { 2 \mathcal { D } \sqrt { d } } { ( 1 - 2 \epsilon ) \delta } \right ) ^ { d } \pi _ { d } \sum _ { i = 0 } ^ { \infty } \exp ( - c _ { \lambda } \kappa t ( 2 ^ { i } r ) ^ { d } ) .$$


<!-- p:10 -->


Using exp ( - c λκ tr d ) ≤ 1 / 2, inequality (17) may now be established by bounding the sum in the above inequality by a geometric series summing to 2 exp ( - c λκ tr d ) . □

### 3. Functionals of forbidden regions graphs satisfy a Berry-Esseen bound

In this section we let P t be a Poisson process with intensity λ t = t λ, t ≥ 1 for some fixed probability measure λ on X , and we prove the Poisson input case of Theorem 2. For a functional Ft on P t with finite, non-zero variance, recall that

$$\widetilde { F } _ { t } = ( F _ { t } - \mathbb { E } F _ { t } ) / \sqrt { \text {Var} ( F _ { t } ) } .$$

Proposition 10 ( Proposition 1.4, Last, Peccati and Schulte [8] ) . Let E F 2 t &lt; ∞ , t ≥ 1 , and assume there are finite positive constants p 1 , p 2 &gt; 0 and c such that

$$\mathbb { E } | D _ { x } F _ { t } | ^ { 4 + p _ { 1 } } \leq c \quad \lambda \cdot a . e . \ x \in \mathbb { X } , t \geq 1$$

and

$$\mathbb { E } | D _ { x , y } ^ { 2 } F _ { t } | ^ { 4 + p _ { 2 } } \leq c \quad \lambda ^ { 2 } \text {-a.e.} \, ( x , y ) \in \mathbb { X } ^ { 2 } , t \geq 1 .$$

Moreover, assume that for some v &gt; 0

$$\frac { \text {Var} ( F _ { t } ) } { t } & \geq v \quad \text {for all} \, t \geq 1 , \\$$

and that

$$m \coloneqq \sup _ { x \in \mathbb { X } , t \geq 1 } \int \mathbb { P } ( D _ { x , y } ^ { 2 } F _ { t } \neq 0 ) ^ { p _ { 2 } / ( 1 6 + 4 p _ { 2 } ) } \lambda _ { t } ( d y ) < \infty .$$

Then there exists a finite constant C, depending only on c , p 1 , p 2 , v, m and λ ( X ) such that with d ( · , · ) denoting either the Wasserstein or Kolmogorov distance and N a standard Gaussian random variable,

$$d ( \widetilde { F } _ { t } , N ) \leq C t ^ { - 1 / 2 } \ \ f o r \ a l l \ t \geq 1 .$$

We first prove Lemma 11, a bound on the derivative of the functional L in (3), which is used when considering both Poisson and binomial input processes. In preparation, for any finite point configuration μ ⊆ X and x ∈ X \ μ , we let

$$A ( x ; \mu ) \\ = \{ z \in \mu \colon \exists w \in \mu , w \neq z , S ( w , z ) \cap ( \mu \cup \{ x \} ) = \{ x \} \} \bigcup _ { \{ z \in \mu } \in \mu \colon S ( x , z ) \cap \mu = \emptyset \} .$$

Recalling (12), we see

$$A ( x ; \mu ) & \subseteq \bigcup \{ \overline { S ( w , z ) } \colon \{ w , z \} \subseteq \mathbb { X } , S ( w , z ) \cap \mu = \emptyset , x \in \overline { S ( w , z ) } \} \\ & \subseteq \overline { \mathcal { R } _ { S } ( x ; \mu ; \mathbb { X } ) } .$$

Let | A ( z ; μ ) | denote the cardinality of A ( z ; μ ).

Lemma 11. Let μ be a locally finite subset of R d and x ∈ X , and let F = L ( μ ) where L ( · ) is given in (3) with | ψ ( x , y ) | ≤ C ∥ x - y ∥ α for some α ≥ 0 , C &gt; 0 . Then there is a constant C α , depending only on α and C, such that

$$| D _ { x } F | \leq C _ { \alpha } \sum _ { z \in A ( x ; \mu ) } \| z - x \| ^ { \alpha } \max ( | A ( z ; \mu ) | , 1 ) .$$


<!-- p:11 -->


Proof. For x ∈ μ we have Dx F = 0. Otherwise take x ∈ X \ μ and, noting that the insertion of x into μ can only break existing edges and form new edges incident to x , we have

$$D _ { x } F = - \sum _ { z \neq w , S ( z , w ) \cap ( \mu \cup [ x ] ) = [ x ] } \psi ( z , w ) + \sum _ { z \in \mu , S ( z , x ) \cap \mu = \emptyset } \psi ( z , x ) .$$

For the first term we note

$$| \psi ( z , w ) | \leq C \| z - w \| ^ { \alpha } \leq C \max ( 1 , 2 ^ { \alpha - 1 } ) \left ( \| z - x \| ^ { \alpha } + \| w - x \| ^ { \alpha } \right )$$

so that

$$\text { so that} \\ | D _ { x } F | \leq C _ { \alpha } \left ( \sum _ { \substack { | z , w | \in \mu \\ z \neq u , S ( z , w ) \sim \mu ( \alpha \cup \{ x \} ) = \{ x \} } } \| z - x \| ^ { \alpha } + \sum _ { \substack { z \in \mu , S ( z , x ) \cap \mu = \emptyset \\ z \in A ( x ; \mu ) } } \| z - x \| ^ { \alpha } \right ) \\ \leq C _ { \alpha } \sum _ { \substack { z \in A ( x ; \mu ) \\ z \in A ( x ; \mu ) } } \| z - x \| ^ { \alpha } \max ( | A ( z ; \mu ) | , 1 ) , \\ \text {where } \text { for the two sums, we see that } \text { if } \{ z - w \} \text { or } z \text { respectively } \text { satisfy the condition}$$

where, for the two sums, we see that if { z , w } or z , respectively, satisfy the conditions of summation then z ∈ A ( x ; μ ), while for the first sum S ( w, z ) ∩ μ = ∅ , which implies w ∈ A ( z ; μ ). □

The proof of the following lemma is provided immediately after the proof of Theorem 2; we will make use of the fact that

$$\int _ { 0 } ^ { \infty } r ^ { \beta } \exp ( - \gamma r ^ { d } ) d r = \frac { 1 } { d \gamma ^ { ( \beta + 1 ) / d } } \Gamma \left ( \frac { \beta + 1 } { d } \right ) \quad \text {for } \beta > - 1 , \gamma > 0 \text { and } d > 0 .$$

In the following, let U t = ∅ for t &lt; 0.

Lemma 12. For t ≥ 1 let P t and U t be as in Assumption B , and let A ⊆ R d . Then

$$\sup _ { t \geq 1 , \, x \in X , \, \mathcal { A } \subseteq X , \, 0 \leq | \mathcal { A } | \leq 2 } \mathbb { E } | D _ { x } t ^ { \alpha / d } L ( \mathcal { D } _ { t } \cup \mathcal { A } ) | ^ { 6 } & < \infty \quad a n d \\ \sup _ { t \geq 1 , \, 0 \leq k \leq 3 , \, x \in X , \, 0 \leq | \mathcal { A } | \leq 2 } \mathbb { E } | D _ { x } t ^ { \alpha / d } L ( \mathcal { W } _ { t - | \mathcal { A } | - k } \cup \mathcal { A } ) | ^ { 6 } & < \infty .$$

Proof ( Proof of Theorem 2, Poisson Input ) . We apply Proposition 10 to Ft = t α/ d L ( P t ), with L as given in (3) where P t is a Poisson process satisfying the conditions of Assumption B. First, the condition E F 2 t &lt; ∞ is seen to be satisfied in light of the inequality | Ft | ≤ t α/ d C ( sup { x , y }⊆ X ∥ y - x ∥ ) α | P t | 2 , where | ν | denotes the number of points of the process ν .

As Assumption C holds by hypothesis, we have

$$\text {Var} ( t ^ { \alpha / d } L ( \mathcal { P } _ { t } ) ) \geq v _ { \alpha } t ,$$

verifying (22).

Next, choosing p 1 and p 2 both equal to 1, inequalities (20), (21) and (23) become, respectively,

$$\mathbb { E } | D _ { x } F _ { t } | ^ { 5 } \leq c , \quad \lambda \text {-a.e.} , x \in \mathbb { X } , t \geq 1 ,$$

$$\mathbb { E } | D _ { x , y } ^ { 2 } F _ { t } | ^ { 5 } \leq c , \quad \lambda ^ { 2 } \text {-a.e.} , ( x , y ) \in \mathbb { X } \times \mathbb { X } , t \geq 1 ,$$


<!-- p:12 -->


and

$$\sup _ { x \in X , t \geq 1 } t \int _ { \mathbb { X } } \mathbb { P } ( D _ { x , y } ^ { 2 } F _ { t } \neq 0 ) ^ { 1 / 2 0 } \lambda ( d y ) < \infty .$$

We next note that by (24),

$$y \in A ( x ; \mu ) \text { \ \ implies \ } R _ { S } ( x ; \mu ; \mathbb { X } ) \geq \| y - x \| .$$

Applying Lemma 12 with A = ∅ shows that (28) is satisfied, and letting A = { y } we see that (29) also holds, as (8) yields

$$\mathbb { E } | D _ { x , y } ^ { 2 } F _ { t } | ^ { 5 } \leq 1 6 \left ( \mathbb { E } | D _ { x } F _ { t } ( \mathcal { P } _ { t } \cup \{ y \} ) | ^ { 5 } + \mathbb { E } | D _ { x } F _ { t } ( \mathcal { P } _ { t } ) | ^ { 5 } \right ) .$$

We now show condition (30) is satisfied. Letting x ∈ X be arbitrary, invoking Assumption B and Lemma 7, followed by Proposition 9 and (26), we obtain

$$and Lemma 7 , \text { followed by Proposition 9 and (26), we obtain} \\ b _ { \lambda } ^ { - 1 } t \int _ { \mathbb { X } } \mathbb { P } ( D _ { x , y } ^ { 2 } F _ { t } \neq 0 ) ^ { 1 / 2 0 } \lambda ( d y ) \leq t \int _ { \mathbb { X } } \mathbb { P } ( D _ { x , y } ^ { 2 } F _ { t } \neq 0 ) ^ { 1 / 2 0 } d y \\ \leq t \int _ { \mathbb { X } } \mathbb { P } ( R _ { S } ( x ; \mathcal { P } _ { t } ; \mathbb { X } ) \geq \| y - x \| ) ^ { 1 / 2 0 } d y \leq C t \int _ { \mathbb { X } } \exp \left ( - c _ { \lambda } \kappa t \| y - x \| ^ { d } / 2 0 \right ) d y \\ = C t \int _ { \mathbb { X } - x } \exp \left ( - c _ { \lambda } \kappa t \| y \| ^ { d } / 2 0 \right ) d y \leq C t \int _ { \mathbb { R } ^ { d } } \exp \left ( - c _ { \lambda } \kappa t \| y \| ^ { d } / 2 0 \right ) d y \\ = C t \sigma _ { d } \int _ { 0 } ^ { \infty } \exp \left ( - c _ { \lambda } \kappa t r ^ { d } / 2 0 \right ) r ^ { d - 1 } d r = \frac { 2 0 C \sigma _ { d } } { d c _ { \lambda } \kappa } . \\ \text {Hence, the superaccum over } x \in \mathbb { X } \text { and } t \geq 1 \text { in (30) is finite, and the proof of the Poisson input}$$

Hence, the supremum over x ∈ X and t ≥ 1 in (30) is finite, and the proof of the Poisson input case of Theorem 2 is complete. □

Proof of Lemma 12. Let η denote P t ∪ A and U t -| A |- k ∪ A in the Poisson and binomial cases, respectively. With Ft = t α/ d L ( η ), for fixed x ∈ X we have by Lemma 11

$$| D _ { x } F _ { t } | & \leqslant t ^ { \alpha / d } \sum _ { y \in \eta } \| y - x \| ^ { \alpha } \mathbf 1 ( y \in A ( x ; \eta ) ) ( 1 + | A ( y ; \eta ) | ) .$$

We develop a general bound to handle the moments of (32). Given a positive integer m ∈ { 1 , . . . , 6 } , we say a set P = { m 1 , . . . , mp } ⊆ { 1 , . . . , m } is a partition of m with p elements when ∑ p i = 1 mi = m . Let P m denote the class of all partitions. Let φ ( z ; η ) , z ∈ X be some non-negative kernel and for a subset μ ⊆ R d , let μ p ̸= denote the collection of all vectors ( z 1 , . . . , z p ) with z := { z 1 , . . . , z p } ⊆ μ and | z | = p . We remark that given { z 1 , . . . , zm } ⊆ μ , with p = |{ z 1 , . . . , zm }| there is a unique partition P ∈ P m with p elements, and at most γ P ⩽ p ! vectors z ∈ μ p ̸= such that { z 1 , . . . , zm } consists in the elements of z appearing with multiplicities given by the elements of P ordered in decreasing order. Reciprocally, any such pair ( P , z ) corresponds to exactly one set { z 1 , . . . , zm } .

By writing the sum (32) over y ∈ P t in the Poisson case, or over y ∈ U t -| A |- k for the binomial, plus a sum over y ∈ A , and using inequalities of the form ( a + b ) m ≤ 2 m - 1 ( a m + b m ), to obtain a bound on E | Dx Ft | m it suffices to obtain m th moment bounds on each component summand; see, for instance, (34).

First consider the Poisson case. The multivariate Mecke formula as in (2.10) of [9], along with the upper bound of Assumption B on the intensity of P t , yields

$$\mathbb { E } \left ( \sum _ { z \in \mathcal { P } _ { t } } \varphi ( z ; \eta ) \right ) ^ { m } \leq m ! \mathbb { E } \sum _ { \{ z _ { 1 } , \dots , z _ { m } \} \subset \mathcal { P } _ { t } } \varphi ( z _ { 1 } ; \eta ) \cdots \varphi ( z _ { m } ; \eta )$$


<!-- p:13 -->


$$L \ G o l d s t e { i n e t a l . / S o t h a s t i c P r e c s e s a n d t h e i r } & \text {Applications} \ 1 2 8 ( 2 0 1 8 ) \ 1 2 0 8 { - 1 2 3 7 } \\ = m ! \sum _ { \{ m _ { 1 } , \dots , m _ { p } \} \in \mathcal { P } _ { m } } \gamma _ { p } \mathbb { E } \sum _ { z = ( z _ { 1 } , \dots z _ { p } ) \in \mathcal { P } _ { t } ^ { p } } \prod _ { i = 1 } ^ { p } \varphi ( z _ { i } ; \eta ) ^ { m _ { i } } \\ \leqslant 6 ! \sum _ { \{ m _ { 1 } , \dots , m _ { p } \} \in \mathcal { P } _ { m } } p ! ( b _ { t } ) ^ { p } \int _ { \mathbb { R } ^ { p } } \mathbb { E } \left [ \prod _ { i = 1 } ^ { p } \varphi ( z _ { i } ; \mathcal { P } _ { t } \cup \mathcal { A } \cup \mathcal { Z } ) ^ { m _ { i } } \right ] d z _ { 1 } \dots d z _ { p } \\ \leqslant C \sum _ { \{ m _ { 1 } , \dots , m _ { p } \} \in \mathcal { P } _ { m } } t ^ { p } \int _ { \mathbb { X } ^ { p } } \prod _ { i = 1 } ^ { p } \left [ \mathbb { E } \varphi ( z _ { i } ; \mathcal { P } _ { t } \cup \mathcal { A } \cup \mathcal { Z } ) ^ { m _ { i } / m } d z _ { 1 } \dots d z _ { p } . \\ \text {In the binomial case, a similar computation yields}$$

In the binomial case, a similar computation yields

$$In the binomial case, a \text { similar computation yields} \\ \mathbb { E } \left ( \sum _ { z \in \mathcal { W } _ { 1 } \mathcal { A } | - k } \varphi ( z ; \eta ) \right ) ^ { m } & = m ! \mathbb { E } \sum _ { \{ z _ { 1 } , \dots , z _ { m } \} \in \mathcal { W } _ { 1 } \mathcal { A } | - k } \varphi ( z _ { 1 } ; \eta ) \dots \varphi ( z _ { m } ; \eta ) \\ & = m ! \sum _ { \{ m _ { 1 } , \dots , m _ { p } \} \in \mathcal { P } _ { m } } \gamma _ { p } \mathbb { E } \sum _ { \substack { z = ( z _ { 1 } , \dots , z _ { p } ) \in \mathcal { W } _ { p } ^ { p } \\ \mathbb { A } ^ { k } \} } \prod _ { | A | = 1 } \varphi ( z _ { i } ; \eta ) ^ { m _ { i } } \\ & \leqslant 6 ! \sum _ { \{ m _ { 1 } , \dots , m _ { p } \} \in \mathcal { P } _ { m } } p ! ^ { 2 } \left ( \tbinom { t - | \mathcal { A } | - k } { p } \int _ { \mathbb { X } ^ { p } } \left [ \prod _ { i = 1 } ^ { p } \varphi ( z _ { i } ; \mathcal { W } _ { t - | \mathcal { A } | - k - p } \cup \mathcal { A } \cup \mathfrak { z } ) ^ { m _ { i } } \right ] d z _ { 1 } \dots d z _ { p } \\ & \leqslant C \sum _ { \{ m _ { 1 } , \dots , m _ { p } \} \in \mathcal { P } _ { m } } t ^ { p } \int _ { \mathbb { X } ^ { p } } \prod _ { i = 1 } ^ { p } \left [ \varphi ( z _ { i } ; \mathcal { W } _ { t - | \mathcal { A } | - k - p } \cup \mathcal { A } \cup \mathfrak { z } ) ^ { m _ { i } / m } d z _ { 1 } \dots d z _ { p } , \\ \text {as in (33) for the Poisson case.} \\ \text {Returning to the Poisson case, by writing | A ( y ; n ) | as a sum over $\mathcal{Z}_{p}$ added to another over $A$, we first}$$

as in (33) for the Poisson case.

Returning to the Poisson case, by writing | A ( y ; η ) | as a sum over P t added to another over A , we first control the moments of

$$control \, \text { the moments of} \\ \mathbb { E } ( 1 + | A ( y ; \eta ) | ^ { m } ) ^ { m } & = \mathbb { E } \left ( 1 + \sum _ { z \in \eta } 1 _ { \{ z \in A ( y ; \eta ) \} } \right ) ^ { m } \leq 3 ^ { m - 1 } \left ( 1 + T _ { 1 } + T _ { 2 } \right ) , \quad \text {where} \\ T _ { 1 } & = \mathbb { E } \left ( \sum _ { z \in \mathcal { T } _ { 1 } } 1 _ { \{ z \in A ( y ; \eta ) \} } \right ) ^ { m } \quad \text {and} \quad T _ { 2 } = \left ( \sum _ { z \in A } 1 _ { \{ z \in A ( y ; \eta ) \} } \right ) ^ { m } \leq | A | ^ { m } . \\ \\ \text {We handle } T _ { 1 } \text { by singular } ( 3 ) \text { to the } \Omega \text { a where } ( s _ { i } ) = 1 _ { \{ s \in A ( y ; \eta ) \} } \text { supercrating } y \text { for notations} \\$$

We handle T 1 by specializing (33) to the case where φ ( z ; η ) = 1 ( z ∈ A ( y ; η )), suppressing y for notational ease in the functional. By (24), (14) and Lemma 5, for any collection of points z = { z 1 , . . . , z p } we have

$$z \in A ( y ; \eta \cup \mathbf z ) & \Longrightarrow z \in \overline { \mathcal { R } _ { S } ( y ; \eta \cup \mathbf z ; \mathbb { X } ) } \Longrightarrow R _ { S } ( y ; \mathcal { P } _ { t } \cup \mathcal { A } \cup \mathbf z ; \mathbb { X } ) \geq \| y - z \| \\ & \Longrightarrow R _ { S } ( y ; \mathcal { P } _ { t } ; \mathbb { X } ) \geq \| y - z \| .$$

Proposition 9 now yields that for all A ⊆ R d ,

$$\mathbb { P } ( z \in A ( y ; \eta \cup \zeta ) ) \leqslant C \exp ( - c _ { \lambda } \kappa t \| y - z \| ^ { d } ) .$$

Now, by (35) we obtain

$$T _ { 1 } & \leq C \sum _ { \{ m _ { 1 } , \dots , m _ { p } \} \in \mathcal { T } _ { m } } t ^ { p } \int _ { \mathbb { X } ^ { p } } \prod _ { i = 1 } ^ { p } \exp ( - c _ { \lambda } \kappa t \| y - z _ { i } \| ^ { d } ) d z _ { 1 } \dots d z _ { p } \\ & \leq C \sum _ { \{ m _ { 1 } , \dots , m _ { p } \} \in \mathcal { T } _ { m } } t ^ { p } \int _ { ( \mathbb { R } ^ { d } ) ^ { p } } \prod _ { i = 1 } ^ { p } \exp ( - c _ { \lambda } \kappa t \| y - z _ { i } \| ^ { d } ) d z _ { 1 } \dots d z _ { p }$$


<!-- p:14 -->


$$L _ { \ } G o l d s t e { i n e t a l . S o t h a s t i c P o r c h e s } & \, a n d \, \text {their} \, \text {Applications} \, \ 1 2 8 \, ( 2018 ) \, 1 2 0 8 \, - 1 2 3 7 \\ & = C \sum _ { \{ m _ { 1 } , \dots , m _ { p } \} \in \mathcal { P } _ { m } } t ^ { p } \int _ { ( \mathbb { R } ^ { d } ) ^ { p } } \prod _ { i = 1 } ^ { p } \exp ( - c _ { \lambda } \kappa t \| z _ { i } \| ^ { d } ) d z _ { 1 } \dots d z _ { p } \\ & = C \sum _ { \{ m _ { 1 } , \dots , m _ { p } \} \in \mathcal { P } _ { m } } \left ( t \int _ { \mathbb { R } ^ { d } } \exp ( - c _ { \lambda } \kappa t \| z \| ^ { d } ) d z \right ) ^ { p } \\ & = C \sum _ { \{ m _ { 1 } , \dots , m _ { p } \} \in \mathcal { P } _ { m } } \left ( \frac { \sigma _ { p } } { d c _ { \lambda } \kappa } \right ) ^ { p } \\ & \leqslant C , \\ \intertext { w h e r in the f i n e l a i n e l a y } \text {where in the final inequarity we apply ( 26 ), and C depends on m , } \kappa , c _ { \lambda } \text {. As } \mathcal { A } \text { is finite the term } T _ { 2 } \text { in } ( 34 ) \text { is}$$

where in the final inequality we apply (26), and C depends on m , κ, c λ . As A is finite the term T 2 in (34) is finite, yielding for all positive integers m a constant C such that

$$\mathbb { E } ( 1 + | A ( y ; \eta ) | ) ^ { m } \leq C .$$

Inequalities (35), and then (36) followed by (37), are obtained in the identical manner for the binomial case. To consider the right hand side of (32), suppressing x for notational ease, let φ ( y ; η ) = ∥ y - x ∥ α 1 { y ∈ A ( x ; η ) } (1 + | A ( y ; η ) | ). The Cauchy-Schwarz inequality, the bound (35) with z any collection of points, and (37) with η replaced by η ∪ z , yield for any y ∈ X

$$\mathbb { E } | \varphi ( y ; \eta \cup \mathbf z ) | ^ { 6 } & \leqslant \| y - x \| ^ { 6 \alpha } \sqrt { \mathbb { P } ( y \in A ( x ; \eta \cup \mathbf z ) ) } \sqrt { \mathbb { E } ( 1 + | A ( y ; \eta \cup \mathbf z ) | ) ^ { 1 2 } } \\ & \leqslant C \| y - x \| ^ { 6 \alpha } \exp ( - c _ { \lambda } \kappa t \| y - x \| ^ { d } / 2 ) .$$

Now decompose the right hand side of (32) into two summands as in (34); we only consider the Poisson case, the binomial case being identical after replacing P t with U t -| A |- k . For the sum over P t , using (33) and (38), we obtain

$$Now decompose the right hand side of ( 3 ) into two summands as in ( 3 ) ; we only consider the Poisson
case, the binomial case being identical after replacing , & \mathcal { P } , with \mathcal { Y } _ { - } | A _ { - } | _ { - } k . \text { For the sum over } \mathcal { P } , \text { using ( 3 )} \\ and ( 3 ) , & \text { with } \\ & \mathbb { E } | \alpha / d \sum _ { y \in \mathcal { P } _ { 1 } } \varphi ( y ; \eta ) | \\ & \leqslant C t ^ { 6 \alpha / d } \sum _ { \substack { m _ { 1 } , \dots , m _ { p } \in \mathcal { P } _ { 6 } \\ m _ { 1 } } } t ^ { p } \int _ { ( \mathbb { R } ^ { d } ) ^ { p } } \prod _ { i = 1 } ^ { p } \left ( \| y _ { i } - x \| ^ { 6 \alpha } \exp ( - c _ { i } \kappa t \| y _ { i } - x \| ^ { d } / 2 ) \right ) ^ { m _ { 1 } / 6 } d y _ { 1 } \dots d y _ { p } \\ & \leqslant C t ^ { 6 \alpha / d } \sum _ { \substack { ( m _ { 1 } , \dots , m _ { p } ) \in \mathcal { P } _ { 6 } \\ m _ { 1 } , \dots , m _ { p } } } t ^ { p } \int _ { ( \mathbb { R } ^ { d } ) ^ { p } } \prod _ { i = 1 } ^ { p } ( \| y _ { i } \| ^ { 6 \alpha } \exp ( - c _ { i } \kappa t \| y _ { i } \| ^ { d } / 2 ) ) ^ { m _ { i } / 6 } d y _ { 1 } \dots d y _ { p } \\ & = C t ^ { 6 \alpha / d } \sum _ { \substack { ( m _ { 1 } , \dots , m _ { p } ) \in \mathcal { P } _ { 6 } \\ m _ { 1 } , \dots , m _ { p } } } t ^ { p } \prod _ { i = 1 } ^ { p } \sigma _ { d } \int _ { 0 } ^ { \infty } r ^ { \alpha m _ { i } + d - 1 } \exp ( - m _ { i } c _ { \lambda } \kappa t r ^ { d } / 1 2 ) d r \\ & = C t ^ { 6 \alpha / d } \sum _ { \substack { ( m _ { 1 } , \dots , m _ { p } ) \in \mathcal { P } _ { 6 } \\ m _ { 1 } , \dots , m _ { p } } } t ^ { p } \prod _ { i = 1 } ^ { p } \frac { \sigma _ { d } } { d ( m _ { i } c _ { \lambda } \kappa / 1 2 ) ^ { \alpha m _ { i } / d + 1 } } \, \Gamma \left ( \frac { \alpha m _ { i } } { d } + 1 \right ) \\ & = C \sum _ { \substack { ( m _ { 1 } , \dots , m _ { p } ) \in \mathcal { P } _ { 6 } \\ m _ { 1 } , \dots , m _ { p } } } \prod _ { i = 1 } ^ { p } \frac { \sigma _ { d } ^ { p } } { d ( m _ { i } c _ { \lambda } \kappa / 1 2 ) ^ { \alpha m _ { i } / d + 1 } } \, \Gamma \left ( \frac { \alpha m _ { i } } { d } + 1 \right ) , \\ \text {where we have used ( 26) with $\beta = \alpha m_{i} + d - 1$ and $\gamma = m_{i} c_{\lambda}k\tau/1 2$ in the next to last equality.}$$

where we have used (26) with β = α mi + d - 1 and γ = mi c λ κ t / 12 in the next to last equality.


<!-- p:15 -->


Now considering the sum over A , and setting v = t ∥ y - x ∥ d in the last inequality, we obtain

$$\text {Now considering the sum over } A , & \text { and setting } v = t \| y - x \| ^ { \prime } \text { in the last inequality, we obtain} \\ & \mathbb { E } \left | t ^ { \alpha / d } \sum _ { y \in A } \varphi ( y ; \eta ) \right | \, \leq | \mathcal { A } | ^ { 6 } t ^ { \alpha / d } \mathbb { E } \varphi ( \eta ; y ) \\ & \leq C | \mathcal { A } | ^ { 6 } t ^ { \alpha / d } \| y - x \| ^ { 6 } \exp ( - c _ { \lambda } c _ { \lambda } t \| y - x \| ^ { d } / 2 ) \\ & \leq C | \mathcal { A } | ^ { 6 } \left ( \sup _ { v > 0 } v ^ { \alpha / d } \exp ( - c _ { \lambda } c _ { \lambda } v / 2 ) \right ) . \\ \intertext { A s ( 3 ) and ( 4 ) are constants not depending on t or x } & \text {is } \exp ( - c _ { \lambda } c _ { \lambda } t ) .$$

As (39) and (40) are constants not depending on t or x ∈ X , the proof is complete. □

We shall now use the results of [7] to prove Theorem 2 for binomial input. Here n ∈ N plays the former role of t and X = ( X 1 , . . . , Xn ) is a vector of independent variables with distribution λ over X , and U n = { X 1 , . . . , Xn } . Let X ′ ,  ̃ X be independent copies of X . We write U a . s . = V if two variables U and V satisfy P ( U = V ) = 1. In the vocabulary of [7], a random vector Y = ( Y 1 , . . . , Yn ) is a recombination of { X , X ′ ,  ̃ X } if for each 1 ⩽ i ⩽ n , either Yi a . s . = Xi , Yi a . s . = Y ′ i or Yi a . s . =  ̃ Xi . For a vector x = ( x 1 , . . . , xn ), and indices { i 1 , . . . , i q } ⊆ { 1 , . . . , n } , define

$$x ^ { i _ { 1 } , \dots , i _ { q } } \colon = ( x _ { j } , j \notin \{ i _ { 1 } , \dots , i _ { q } \} ) .$$

For 1 ≤ i , j ≤ n , and f a real valued function taking in n , n - 1 or n - 2 ordered arguments in R d , let

$$D _ { i } f ( X ) & = f ( X ) - f ( X ^ { i } ) \quad \text {and} \\ D _ { i , j } f ( X ) & = f ( X ) - f ( X ^ { i } ) - f ( X ^ { j } ) + f ( X ^ { i , j } ) , \quad \text {noting that } D _ { i , j } f ( X ) = D _ { j , i } f ( X ) .$$

Recalling that X ′ ,  ̃ X are independent copies of X , let

Bn ( f ) = sup { γ Y , Z ( f ) : ( Y , Z ) recombinations of { X , X ′ ,  ̃ X }} and B ′ n ( f ) = sup { γ ′ Y , Y ′ , Z ( f ) : ( Y , Y ′ , Z ) recombinations of { X , X ′ ,  ̃ X }} , where γ Y , Z ( f ) = E [ 1 { D 1 , 2 f ( Y ) ̸= 0 } D 2 f ( Z ) 4 ] and γ ′ Y , Y ′ , Z ( f ) = E [ 1 { D 1 , 2 f ( Y ) ̸= 0 , D 1 , 3 f ( Y ′ ) ̸= 0 } D 2 f ( Z ) 4 ] .

Then Theorem 5.1 of [7], simplified by [7, Remark 5.2] and [7, Proposition 5.3] yields the following Kolmogorov distance bound for the normal approximation of f ( X ), properly standardized.

Theorem 13 ( Lachièze-Rey and Peccati [7] ) . Let f be a functional taking in ordered arguments of n , n - 1 , or n - 2 elements of X . Assume furthermore that f is invariant under permutation of its arguments, that E f ( X ) = 0 and that σ 2 := Var( f ( X )) is non-zero and finite. Let d ( · , · ) denote either the Kolmogorov or the Wasserstein distance. Then, for some C &gt; 0 not depending on f or n,

$$\partial _ { \ } f \partial _ { n } , \\ d ( \sigma ^ { - 1 } f ( X ) , N ) \leqslant & \, C \left [ \frac { 4 \sqrt { 2 } n ^ { 1 / 2 } } { \sigma ^ { 2 } } \left ( \sqrt { n B _ { n } ( f ) } + \sqrt { n ^ { 2 } B _ { n } ^ { \prime } ( f ) } + \sqrt { \mathbb { E } D _ { 1 } f ( X ) ^ { 4 } } \right ) \right ] \\ & + \frac { n } { 4 \sigma ^ { 3 } } \sqrt { \mathbb { E } | D _ { 1 } f ( X ) ^ { 6 } | } + \frac { \sqrt { 2 \pi } n } { 1 6 \sigma ^ { 3 } } \mathbb { E } | D _ { 1 } f ( X ) ^ { 3 } | \right ] ,$$

where N is a standard normal random variable.

$$( 4 1 )$$


<!-- p:16 -->


The authors of [7] focus on the Kolmogorov distance, but the bound they prove is valid for the Wasserstein, even though it is not stated there formally. More precisely, we refer the reader to the inequality in Theorem 2.2 of [2], involving Wasserstein distance. The first term in this inequality, σ - 2 √ Var( E ( T | W )), has been shown in [7] to be bounded by the terms of the first line of the right hand member of (42). The second term in the inequality of [2] is equal to n σ - 3 E | D 1 f ( X ) | 3 , also taken care of in (42). The term ( n / (4 σ 3 )) √ E | D 1 f ( X ) 6 | is in fact only necessary for the Kolmogorov distance, and can be removed when treating the Wasserstein distance. Hence the upper bound (42) for the Kolmogorov distance also upper bounds the Wasserstein.

For L as in (3) with | ψ ( x , y ) | ≤ C ∥ x - y ∥ α for some α ≥ 0 , C &gt; 0, let Fn = n α/ d L ( U n ), and let the functional f , defined on ordered sets of variables, be given by f ( x 1 , . . . , xq ) = Fn ( { x 1 , . . . , xq } ) - E f ( X ) for any q ⩾ 1 and { x 1 , . . . , xq } ⊆ R d . We note that D defined in (41), and D as in (7), obey the relations

$$D _ { i } f ( X ) = D _ { X _ { i } } F _ { n } ( \mathcal { U } _ { n } \ \{ X _ { i } \} ) , \quad \text {and for } i \neq j \quad D _ { i j } f ( X ) = D _ { X _ { i } , X _ { j } } F _ { n } ( \mathcal { U } _ { n } \ \{ X _ { i } , X _ { j } \} ) .$$

WenowshowhowTheorem13, and Lemma 14 below, prove the Kolmogorov and Wasserstein bounds of Theorem 2 for binomial input.

Proof of Theorem 2 for binomial input. Assumption C yields σ 2 ⩾ Cn for some C &gt; 0. Using (27) and (43) of Lemma 12 with A = ∅ , k = 1 we obtain,

$$\sup _ { n \geq 1 } \mathbb { E } [ D _ { 1 } f ( X ) ^ { 6 } ] = \sup _ { n \geq 1 } \int _ { \mathbb { X } } \mathbb { E } | D _ { x } F _ { n } ( \mathcal { U } _ { n - 1 } ) | ^ { 6 } \lambda ( d x ) < \infty .$$

For the last three terms of (42), applying H ̈ older's inequality, we find that there exists C &gt; 0 such that

$$\frac { 4 \sqrt { 2 } n ^ { 1 / 2 } } { \sigma ^ { 2 } } \sqrt { \mathbb { E } D _ { 1 } f ( X ) ^ { 4 } } + \frac { n } { 4 \sigma ^ { 3 } } \sqrt { \mathbb { E } | D _ { 1 } f ( X ) ^ { 6 } | } + \frac { \sqrt { 2 \pi } n } { 1 6 \sigma ^ { 3 } } \mathbb { E } | D _ { 1 } f ( X ) ^ { 3 } | \leqslant C n ^ { - 1 / 2 } .$$

Lemma 14 yields C such that

$$B _ { n } ( f ) \leqslant \frac { C } { n } \quad \text {and} \quad B _ { n } ^ { \prime } ( f ) \leqslant \frac { C } { n ^ { 2 } } .$$

Applying these bounds for the first two terms in (42) completes the proof.

Lemma 14. There exists C such that

$$B _ { n } ( f ) \leqslant \frac { C } { n } \ \ a n d \ \ B _ { n } ^ { \prime } ( f ) \leqslant \frac { C } { n ^ { 2 } } .$$

Proof. We begin with the first inequality. Let Y = ( Y 1 , . . . , Yn ) and Z = ( Z 1 , . . . , Zn ) be recombinations of { X , X ′ ,  ̃ X } . Note that Y 1 is independent of { Y 2 , Z 2 } because Y 1 is either X 1 , X ′ 1 or  ̃ X 1 and these three variables are independent of X 2 , X ′ 2 ,  ̃ X 2. Also, either Y 2 , Z 2 both equal the same element of { X 2 , X ′ 2 ,  ̃ X 2 } , in which case Y 2 a . s . = Z 2 , or they are assigned to different elements of this set, in which case they are independent. Letting λ Y 1 , Y 2 , Z 2 denote the law of ( Y 1 , Y 2 , Z 2), we therefore have d λ Y 1 , Y 2 , Z 2 ( y 1 , y 2 , z 2) = 1 { y 2 = z 2 } d λ ( y 1) d λ ( y 2) in the first case, and d λ Y 1 , Y 2 , Z 2 ( y 1 , y 2 , z 2) = d λ ( y 1) d λ ( y 2) d λ ( z 2) in the second.

□


<!-- p:17 -->


Using the conditional H ̈ older inequality with conjugate exponents 3 , 3 / 2 yields that for every { y 1 , y 2 , z 2 } ⊆ X , with the following conditionings valid λ ( Y 1 , Y 2 , Z 2 ) - a.s.,

$$\mathbb { E } \left [ 1 _ { \{ D _ { 1 , 2 } f ( Y ) \neq 0 \} } D _ { 2 } f ( Z ) ^ { 4 } | Y _ { 1 } = y _ { 1 } , Y _ { 2 } = y _ { 2 } , Z _ { 2 } = z _ { 2 } \right ] \\ \leq & \mathbb { P } ( D _ { 1 , 2 } f ( Y ) \neq 0 | Y _ { 1 } = y _ { 1 } , Y _ { 2 } = y _ { 2 } , Z _ { 2 } = z _ { 2 } ) ^ { 1 / 3 } \\ & \times \mathbb { E } [ D _ { 2 } f ( Z ) ^ { 6 } | Y _ { 1 } = y _ { 1 } , Y _ { 2 } = y _ { 2 } , Z _ { 2 } = z _ { 2 } ] ^ { 2 / 3 } .$$

Either Z 2 a . s . = Y 2, and when conditioning on Y 2 = y 2 , Z 2 = z 2 we must take y 2 = z 2, or Y 2 and Z 2 are independent. In both cases, for λ Y 1 , Y 2 , Z 2 -a.e. ( y 1 , y 2 , z 2), with L ( U ) denoting the law of U , and adopting similar notation for the conditional law, by (43) we have

$$\mathcal { L } \left ( \mathbf D _ { 1 , 2 } f ( Y ) | Y _ { 1 } = y _ { 1 } , Y _ { 2 } = y _ { 2 } , Z _ { 2 } = z _ { 2 } \right ) = \mathcal { L } ( D _ { y _ { 1 } , y _ { 2 } } F _ { n } ( \mathcal { W } _ { n - 2 } ) ) .$$

Similarly, separately studying the cases Y 1 a . s . = Z 1 and ( Y 1 , Z 1) independent, one has for λ Y 1 , Y 2 , Z 2 -a.e.( y 1 , y 2 , z 2) ,

$$\mathcal { L } \left ( D _ { 2 } f ( Z ) | Y _ { 1 } = y _ { 1 } , Y _ { 2 } = y _ { 2 } , Z _ { 2 } = z _ { 2 } \right ) \\ = \begin{cases} \mathcal { L } ( D _ { z _ { 2 } } F _ { n } ( \mathcal { W } _ { n - 2 } \cup \{ y _ { 1 } \} ) ) & \text {if } Y _ { 1 } \stackrel { a . s . } { = } Z _ { 1 } \\ \mathcal { L } ( D _ { z _ { 2 } } F _ { n } ( \mathcal { W } _ { n - 1 } ) ) & \text {if } Y _ { 1 } , Z _ { 1 } \text { are independent.} \end{cases}$$

Applying (27) of Lemma 12 with x = z 2 , A = { y 1 } and k = 2 for the first case above, and similarly for the second, shows the final factor in (45) is bounded by M . Now integrating (45) over λ Y 1 , Y 2 , Z 2 and applying Lemma 7 and Proposition 9 yields

$$\text {over $\lambda^{1},\i2,\i2$ and applying Lemma } / \text { and Proposition 9 yields} \\ \gamma _ { Y , Z } ( f ) & \leqslant C \int _ { \mathbb { X } ^ { 2 } } \mathbb { P } ( D _ { y _ { 1 } , y _ { 2 } } F _ { n } ( \mathcal { U } _ { n - 2 } ) \neq 0 ) ^ { 1 / 3 } d y _ { 1 } d y _ { 2 } \\ & \leqslant C \int _ { \mathbb { X } ^ { 2 } } \mathbb { P } ( R _ { S } ( y _ { 1 } ; \mathcal { U } _ { n - 2 } ; \mathbb { X } ) \geqslant \| y _ { 2 } - y _ { 1 } \| ) ^ { 1 / 3 } d y _ { 1 } d y _ { 2 } \\ & \leqslant C \int _ { \mathbb { X } ^ { 2 } } C \exp ( - c _ { \lambda } \kappa ( n - 2 ) \| y _ { 1 } - y _ { 2 } \| ^ { d } / 3 ) d y _ { 1 } d y _ { 2 } \leqslant \frac { C } { n } \\ \text {for some final constant } C & > 0 , \text {demoting the first inequality in } ( 4 4 ) .$$

for some final constant C &gt; 0, demonstrating the first inequality in (44).

The second inequality in (44) is proved similarly. Let Y , Y ′ , Z be recombinations of { X , X ′ ,  ̃ X } . Applying the conditional H ̈ older inequality for a three way product,

$$\{ x , X , X \} . \text {Applying the conditional Holder uniformly for a three way product} , \\ \gamma ^ { \prime } _ { Y , r , z } ( f ) \leqslant \int _ { \mathbb { X } ^ { s } } \mathbb { P } ( D _ { 1 , 2 } f ( Y ) \neq 0 | Y _ { 1 } = y _ { 1 } , \, Y _ { 2 } = y _ { 2 } , \, Y _ { 1 } ^ { \prime } = y _ { 1 } ^ { \prime } , \, Y _ { 3 } ^ { \prime } = y _ { 3 } ^ { \prime } , \, Z _ { 2 } = z _ { 2 } ) ^ { 1 / 6 } \\ \mathbb { P } ( D _ { 1 , 3 } f ( Y ^ { \prime } ) \neq 0 | Y _ { 1 } = y _ { 1 } , \, Y _ { 2 } = y _ { 2 } , \, Y _ { 1 } ^ { \prime } = y _ { 1 } ^ { \prime } , \, Y _ { 3 } ^ { \prime } = y _ { 3 } ^ { \prime } , \, Z _ { 2 } = z _ { 2 } ) ^ { 1 / 6 } \\ \mathbb { E } [ D _ { 2 } f ( Z ) ^ { 6 } | Y _ { 1 } = y _ { 1 } , \, Y _ { 2 } = y _ { 2 } , \, Y _ { 1 } ^ { \prime } = y _ { 1 } ^ { \prime } , \, Y _ { 3 } ^ { \prime } = y _ { 3 } ^ { \prime } , \, Z _ { 2 } = z _ { 2 } ] ^ { 2 / 3 } \\ d \lambda _ { 1 } , Y _ { 2 } , Y _ { 1 } ^ { \prime } , Y _ { 3 } ^ { \prime } , z _ { 2 } ( y _ { 1 } , y _ { 2 } , y _ { 1 } ^ { \prime } , y _ { 3 } ^ { \prime } , z _ { 2 } ) , \\ \intertext { w i t h the conditions will be $ \intertext { a } y _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 2 } , y _ { 2 } , z _ { 2 } , z _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } \intertext { c } \intertext { a } y _ { 2 } , y _ { 1 } , y _ { 2 } , y _ { 2 } , y _ { 1 } , y _ { 3 } , z _ { 2 } , z _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } \intertext { d } y _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 2 } , y _ { 2 } , z _ { 2 } , z _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } \intertext { d } y _ { 2 } , y _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } , z _ { 2 } , z _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } \intertext { d } y _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } , z _ { 2 } , z _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } \intertext { d } y _ { 2 } , y _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } , z _ { 2 } , z _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } \intertext { d } y _ { 2 } , y _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } , z _ { 2 } , z _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } \intertext { d } y _ { 2 } , y _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } , z _ { 2 } , z _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } \intertext { d } y _ { 2 } , y _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } , z _ { 2 } , z _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } \intertext { d } y _ { 2 } , y _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } , z _ { 2 } , z _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } \intertext { d } y _ { 2 } , y _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } , z _ { 2 } , z _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } \intertext { d } y _ { 2 } , y _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } , z _ { 2 } , z _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } \intertext { d } y _ { 2 } , y _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } , z _ { 2 } , z _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } \intertext { d } y _ { 2 } , y _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } , z _ { 2 } , z _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } \intertext { d } y _ { 2 } , y _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } , z _ { 2 } , z _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } \intertext { d } y _ { 2 } , y _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } , z _ { 2 } , z _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } \intertext { d } y _ { 2 } , y _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } , z _ { 2 } , z _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } \intertext { d } y _ { 2 } , y _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } , z _ { 2 } , z _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } \intertext { d } y _ { 2 } , y _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } , z _ { 2 } , z _ { 1 } , y _ { 2 } , y _ { 1 } , y _ { 3 } \intertext { d } y _ { 2 } , y _ { 1$$

with the conditionings valid λ Y 1 , Y 2 , Y ′ 1 , Y ′ 3 , Z 2 -a.e. We have, for some m ∈ { 0 , 1 , 2 } and A ⊆ X with | A | = m , depending on how the recombination Z is composed,

$$\mathcal { L } \left ( \mathbf D _ { 2 } f ( Z ) | Y _ { 1 } = y _ { 1 } , Y _ { 2 } = y _ { 2 } , Y _ { 1 } ^ { \prime } = y _ { 1 } ^ { \prime } , Y _ { 3 } ^ { \prime } = y _ { 3 } ^ { \prime } , Z _ { 2 } = z _ { 2 } \right ) = \mathcal { L } ( D _ { z _ { 2 } } F _ { m } ( \mathcal { W } _ { n - 1 - m } \cup \mathcal { A } ) ) ,$$

whenever Y 2 a . s . = Z 2, necessitating y 2 = z 2, or Y 2 , Z 2 are independent. Hence, (27) of Lemma 12 yields that the last term in the integral is a.e. bounded by M 2 / 3 .


<!-- p:18 -->


The values of Y ′ 1 , Z 2 are irrelevant to Y once we have conditioned on the values of Y 1 , Y 2. Therefore we have

$$\mathbb { P } ( D _ { 1 , 2 } f ( Y ) \neq 0 | Y _ { 1 } = y _ { 1 } , Y _ { 2 } = y _ { 2 } , Y _ { 1 } ^ { \prime } = y _ { 1 } ^ { \prime } , Y _ { 3 } ^ { \prime } = y _ { 3 } ^ { \prime } , Z _ { 2 } = z _ { 2 } ) \\ = \begin{cases} \mathbb { P } ( D _ { y _ { 1 } , y _ { n } } F ( \mathcal { W } _ { n - 2 } ) \neq 0 ) \, \text {if} \, Y _ { 3 } \text { is independent of } Y _ { 3 } ^ { \prime } \\ \mathbb { P } ( D _ { y _ { 1 } , y _ { n } } F ( \mathcal { W } _ { n - 3 } \cup \{ y _ { 3 } ^ { \prime } \} ) \neq 0 ) \, \text {if} \, Y _ { 3 } \, \stackrel { a . s. } { = } Y _ { 3 } ^ { \prime } \\ \leqslant \mathbb { P } ( R _ { s } ( y _ { 1 } , \mathcal { W } _ { n - 3 } ) \geqslant \| y _ { 1 } - y _ { 2 } \| ) \\ \leqslant C \exp ( - \alpha _ { K } ( n - 3 ) \| y _ { 1 } - y _ { 2 } \| ^ { d } ) , \\ \end{cases}$$

where we have used that RS ( x ; μ ; X ) stabilizes, from Lemma 7, and that

$$\max ( R _ { S } ( y _ { 1 } ; \mathcal { U } _ { n - 2 } ; \mathbb { X } ) , R _ { S } ( y _ { 1 } ; \mathcal { U } _ { n - 3 } \cup \{ y _ { 3 } ^ { \prime } \} ; \mathbb { X } ) ) \leqslant R _ { S } ( y _ { 1 } ; \mathcal { U } _ { n - 3 } ; \mathbb { X } ) ,$$

justified by the monotonicity property provided by Lemma 5, and Proposition 9. Similarly, as the value of Y 1 is irrelevant to Y ′ once we condition on Y ′ 1 , and Y ′ 2 will either equal one of Y 2 or Z 2 a.s., or be independent of both, for some m ∈ { 0 , 1 } and some set A with m elements,

$$\mathbb { P } ( D _ { 1 , 3 } f ( Y ^ { \prime } ) \neq 0 | Y _ { 1 } = y _ { 1 } , Y _ { 2 } = y _ { 2 } , Y _ { 1 } ^ { \prime } = y _ { 1 } ^ { \prime } , Y _ { 3 } ^ { \prime } = y _ { 3 } ^ { \prime } , Z _ { 2 } = z _ { 2 } ) \\ \leq & \mathbb { P } ( R _ { S } ( y _ { 1 } ^ { \prime } , \mathcal { W } _ { n - 2 - m } \cup \mathcal { A } ) \geqslant \| y _ { 1 } ^ { \prime } - y _ { 3 } ^ { \prime } \| ) \\ \leq & C \exp ( - c _ { \lambda } \kappa ( n - 3 ) \| y _ { 1 } ^ { \prime } - y _ { 3 } ^ { \prime } \| ^ { d } ) .$$

If Y 1 a . s . = Y ′ 1 and n ≥ 4 we have

$$If Y _ { 1 } \stackrel { a . s . } { = } Y _ { 1 } ^ { \prime } \, \text {and} \, n \geq 4 \, \text {we have} \\ \gamma _ { \gamma , \gamma ^ { \prime } , Z } ( f ) \leqslant C \int _ { \mathbb { X } } \left [ \int _ { \mathbb { X } } \exp ( - c _ { \lambda } \kappa ( n - 3 ) \| y _ { 1 } - y _ { 2 } \| ^ { d } / 6 ) d y _ { 2 } \right ] \\ \times \left [ \int _ { \mathbb { X } } \exp ( - c _ { \lambda } \kappa ( n - 3 ) \| y _ { 1 } - y _ { 3 } ^ { \prime } \| ^ { d } / 6 ) d y _ { 3 } ^ { \prime } \right ] d y _ { 1 } \\ \leqslant C \int _ { \mathbb { X } } \left [ \int _ { \mathbb { R } ^ { d } } \exp ( - c _ { \lambda } \kappa ( n - 3 ) \| y _ { 1 } - y _ { 2 } \| ^ { d } / 6 ) d y _ { 2 } \right ] ^ { 2 } d y _ { 1 } \\ = C \int _ { \mathbb { X } } \left [ \int _ { \mathbb { R } ^ { d } } \exp ( - c _ { \lambda } \kappa ( n - 3 ) \| y _ { 2 } \| ^ { d } / 6 ) d y _ { 2 } \right ] ^ { 2 } d y _ { 1 } \\ \leqslant C \int _ { \mathbb { X } } \left [ ( n - 3 ) ^ { - 1 } \int _ { \mathbb { R } ^ { d } } \exp ( - c _ { \lambda } \kappa \| y _ { 1 } - y _ { 2 } \| ^ { d } / 6 ) d y _ { 2 } \right ] \, d y _ { 1 } \\ \leqslant \frac { C } { n ^ { 2 } } . \\ \text {If } Y _ { 1 } \text { and } Y _ { 1 } ^ { \prime } \text { are independent,}$$

If Y 1 and Y ′ 1 are independent,

$$If Y _ { 1 } \text { and } Y _ { 1 } ^ { \prime } \text { are independent,} \\ \gamma _ { Y , Y ^ { \prime } , Z } ^ { \prime } ( f ) \leqslant C \int _ { \mathbb { X } ^ { 2 } } \exp ( - c _ { \lambda } \kappa ( n - 3 ) \| y _ { 1 } - y _ { 2 } \| ^ { d } / 6 ) d y _ { 1 } d y _ { 2 } \\ \times \int _ { \mathbb { X } ^ { 2 } } \exp ( - c _ { \lambda } \kappa ( n - 3 ) \| y _ { 1 } ^ { \prime } - y _ { 3 } ^ { \prime } \| ^ { d } / 6 ) d y _ { 1 } ^ { \prime } d y _ { 3 } ^ { \prime } \\ = C \left [ \int _ { \mathbb { X } } \left [ \int _ { \mathbb { X } } \exp ( - c _ { \lambda } \kappa ( n - 3 ) \| y _ { 1 } - y _ { 2 } \| ^ { d } / 6 ) d y _ { 1 } \right ] d y _ { 2 } \right ] ^ { 2 } \\ \leqslant C \left [ \int _ { \mathbb { X } } \left [ ( n - 3 ) ^ { - 1 } \int _ { \mathbb { R } ^ { d } } \exp ( - c _ { \lambda } \kappa \| y _ { 2 } \| ^ { d } / 6 ) d y _ { 1 } \right ] d y _ { 2 } \right ] ^ { 2 } \leqslant \frac { C } { n ^ { 2 } } . \\ \text {In both cases, } B _ { n } ^ { \prime } ( f ) \leqslant C / n ^ { 2 } , \text { which conclcludes the proof.} \quad \Box$$

In both cases, B ′ n ( f ) ⩽ C / n 2 , which concludes the proof. □


<!-- p:19 -->


### 4. Variance lower bounds

In this section, we prove Theorem 4, providing a lower bound on Var L ( η t ) under broad conditions on the collection of forbidden regions. One key step of the proof, accomplished in Lemma27, is to show that if the input process is split into two independent processes then the first process is likely to contain many influential point pairs. Intuitively, a point pair ( x , y ) ∈ R d × R d is influential if an additional process point falling in the vicinity of x produces an effect on L that differs from its effect had the point fallen in the vicinity of y . To prove Theorem 4, we show that conditional on the first process containing many influential pairs, the effect of adding the second process contributes at least an amount Ω ( t ), a quantity satisfying lim inf t →∞ Ω ( t ) / t &gt; 0, to the variance of L ( η t ).

Throughout this section we assume that the function ψ used to define L in (3) satisfies the hypotheses of Theorem 4. In addition, we will be working at a different scale from the rest of the paper, considering Poisson and binomial processes of constant intensity on a growing space, rather than of growing intensity on a fixed space. The reason for using this scaling is that we will need to consider the limiting case of a Poisson process on R d . In particular, in this section, for any t ≥ 1, we let P t denote a homogeneous Poisson point process on t 1 / d X with intensity 1, and let U t denote a binomial process of ⌈ t ⌉ points independently and uniformly placed in t 1 / d X . We couple all P t by defining P t = P ∞ ∩ t 1 / d X where P ∞ is a homogeneous Poisson point process on R d of intensity 1.

We assume throughout that X is star shaped with star center at the origin, and contains an open set around the origin. The first property implies that s 1 / d X ⊆ t 1 / d X if s ≤ t , and the second that for all x ∈ R d and r &gt; 0 that there exists a finite value t 0( x , r ) such that

$$B ( x , r ) \subseteq t ^ { 1 / d } \mathbb { X } \quad \text { for all } t > t _ { 0 } ( x , r ) .$$

Before stating the following result we recall the definition of E ± x ( μ ) from (13), and inform the reader that the constant r 0 may take on different values in the statements below.

Proposition 15. Assume that the forbidden regions satisfy the scaled ball condition (Assumption A ) for some fixed δ &gt; 0 and all x ∈ R d and positive t , r when the role of X is played by t 1 / d X ∩ B ( x , r ) . Then for any ε &gt; 0 , there exists r 0 such that for all r &gt; r 0 , all x ∈ R d and all t ∈ ( t 0( x , r ) , ∞ ] ,

$$\mathbb { P } \left ( E _ { x } ^ { \pm } ( \mathcal { P } _ { t } ) = E _ { x } ^ { \pm } ( \mathcal { P } _ { \infty } \cap B ( x , r ) ) \right ) \geq 1 - \epsilon ,$$

and for all t ∈ ( t 0( x , r ) , ∞ ) ,

$$\mathbb { P } \left ( E _ { x } ^ { \pm } ( \mathcal { W } _ { t } ) = E _ { x } ^ { \pm } ( \mathcal { W } _ { t } \cap B ( x , r ) ) \right ) \geq 1 - \epsilon .$$

Before proving Proposition 15, first observe that (47) could be equivalently stated with P t appearing instead of P ∞ , since if B ( x , r ) ⊆ t 1 / d X , then P t ∩ B ( x , r ) = P ∞ ∩ B ( x , r ).

For x ∈ R d , r &gt; 0 , t &gt; t 0( x , r ) and a point process μ , define the events

$$\Phi ( x , r , t , \mu ) = \left \{ \mathcal { R } _ { S } ( x ; \mu ; t ^ { 1 / d } \mathbb { X } ) \cap \mathcal { R } _ { S } \left ( x ; \mu \cap B ( x , r ) ; \, B ( x , r ) \right ) ^ { c } \neq \emptyset \right \}$$

and

$$\Psi ( x , r , t , \mu ) = \left \{ \mathcal { R } _ { S } \left ( x ; \mu \cap B ( x , r ) ; B ( x , r ) \right ) \cap \mathcal { R } _ { S } \left ( x ; \mu ; t ^ { 1 / d } \mathbb { X } \right ) ^ { c } \neq \emptyset \right \} .$$

Note that since t &gt; t 0( x , r ), we have B ( x , r ) ⊆ t 1 / d X . Thus, to picture these events, start with the point process restricted to the viewing window B ( x , r ), and consider the region R S ( x ; μ ∩ B ( x , r ) ; B ( x , r ) ) that is affected by the addition of x to μ . The first event is that this affected region grows when we expand the window to t 1 / d X , and the second event is that it shrinks. To prove Proposition 15 we require the following result showing that these events are unlikely.


<!-- p:20 -->


Lemma 16. Under the hypotheses of Proposition 15 , given any ε &gt; 0 , there exists r 0 such that for all r &gt; r 0 and x ∈ R d

$$\mathbb { P } \Big ( \Phi ( x , r , t , \mathcal { P } _ { t } ) ) < \epsilon / 2 \ \ a n d \quad \mathbb { P } \Big ( \Psi ( x , r , t , \mathcal { P } _ { t } ) ) < \epsilon / 2 \ \ f o r \ t \in ( t _ { 0 } ( x , r ) , \infty ] ,$$

and

$$\mathbb { P } \Big ( \Phi ( x , r , t , \mathcal { W } _ { t } ) ) < \epsilon / 2 \ \ a n d \quad \mathbb { P } \Big ( \Psi ( x , r , t , \mathcal { W } _ { t } ) ) < \epsilon / 2 \ \ f o r \ t \in ( t _ { 0 } ( x , r ) , \infty ) .$$

Proof. We use the same argument as in Proposition 9. Suppose that Φ ( x , r , t , μ ) holds for μ = P t or μ = U t . Then there exist points { w, z } such that

- (a) { w, z } ⊆ t 1 / d X ;
- (b) S ( w, z ) ∩ μ = ∅ ;
- (c) x ∈ S ( w, z );
- (d) S ( w, z ) ̸⊆ R S ( x ; μ ∩ B ( x , r ) ; B ( x , r ) ) .

If { w, z } ⊆ B ( x , r ), then (d) is a contradiction. Thus either ∥ w - x ∥ &gt; r or ∥ z - x ∥ &gt; r . For u &gt; 0, let ˆ Φ ( u ) be the event that there exists { w, z } such that (a)-(c) hold and

$$u < \max ( \| w - x \| , \| z - x \| ) \leq 2 u .$$

We have now shown that if Φ ( x , r , t , μ ) holds, then there exist points { w, z } such that (a)-(c) hold and max( ∥ w - x ∥ , ∥ z - x ∥ ) &gt; r , implying that

$$\Phi ( x , r , t , \mu ) \subseteq \bigcup _ { i = 0 } ^ { \infty } \widehat { \Phi } ( 2 ^ { i } r ) .$$

For a given u &gt; 0 we bound the probability of ˆ Φ ( u ) and apply a union bound. If ˆ Φ ( u ) holds, then { w, z } ⊆ t 1 / d X ∩ B ( x , 2 u ), and S ( w, z ) contains no points of μ and has diameter at least u . By the scaled ball condition, with the role of X played by t 1 / d X ∩ B ( x , 2 u ), the set S ( w, z ) ∩ t 1 / d X ∩ B ( x , 2 u ) contains a ball of radius δ u / D . Thus, ˆ Φ ( u ) implies the existence of a ball of radius δ u / D within t 1 / d X ∩ B ( x , 2 u ) containing no points of μ . Every ball of radius δ u / D contains a cell of the lattice ( δ u / D √ d ) Z d , and by considering the volume of B ( x , 2 u ), the set t 1 / d X ∩ B ( x , 2 u ) contains at most

$$\frac { \pi _ { d ( 2 u ) ^ { d } } } { ( \delta u / \mathcal { D } \sqrt { d } ) ^ { d } } = \frac { \pi _ { d } ( 2 \mathcal { D } \sqrt { d } ) ^ { d } } { \delta ^ { d } }$$

cells of this lattice. Bounding ˆ Φ ( u ) by the event that all of these cells have no points of μ , in the case μ = P t , recalling that P t has intensity 1,

$$\mathbb { P } ( \widehat { \Phi } ( u ) ) & \leq \frac { \pi _ { d } ( 2 \mathcal { D } \sqrt { d } ) ^ { d } } { \delta ^ { d } } \exp \left ( - \kappa u ^ { d } \right ) ,$$

where κ = ( δ/ D √ d ) d . If μ = U t , a similar statement holds, as

$$\mathbb { P } ( \widehat { \Phi } ( u ) ) \leq \frac { \pi _ { d } ( 2 \mathcal { D } \sqrt { d } ) ^ { d } } { \delta ^ { d } } \left ( 1 - \frac { \kappa u ^ { d } } { | \mathbb { X } | \lceil t \rceil } \right ) ^ { \lceil t \rceil } \leq \frac { \pi _ { d } ( 2 \mathcal { D } \sqrt { d } ) ^ { d } } { \delta ^ { d } } \exp \left ( - \frac { \kappa u ^ { d } } { | \mathbb { X } | } \right ) .$$


<!-- p:21 -->


Applying the union bound in (49) followed by these two inequalities, and then bounding the resulting sum by a geometric series as in Proposition 9, shows that in either case we have P ( Φ ( x , r , t , μ ) ) ≤ Ce - cr d for constants C and c . Now choose r 0 such that this upper bound is less than ε/ 2 for r &gt; r 0.

Bounding Ψ ( x , r , t , P t ) and Ψ ( x , r , t , U t ) is similar. If Ψ ( x , r , t , μ ) holds, then there must exist { w, z } ⊆ B ( x , r ) with x ∈ S ( w, z ) such that

$$S ( w , z ) \cap \mu \cap B ( x , r ) = \emptyset \quad \text {but} \quad S ( w , z ) \cap \mu \neq \emptyset .$$

These relations imply that S ( w, z ) extends outside of B ( x , r ), which means that S ( w, z ) has diameter at least r . Hence, by the scaled ball condition with the role of X played by t 1 / d X ∩ B ( x , r ) = B ( x , r ), the set S ( w, z ) ∩ B ( x , r ) contains a ball of radius δ r / D . Thus, there exists a ball of radius δ r / D containing no points of μ , and one may now argue as for Φ ( x , r , t , μ ). □

Proof of Proposition 15. For ε &gt; 0 let r 0 be given as in Lemma 16. For μ = P t or μ = U t , for all r ≥ r 0, x ∈ R d , and t &gt; t 0( x , r ), it holds except on an event of probability at most ε that R S ( x ; μ ; t 1 / d X ) = R S ( x ; μ ∩ B ( x , r ) ; B ( x , r )). By Lemma 6, on this event E ± ( μ ) = E ± ( μ ∩ B ( x , r ) ) .

Since G ( P ∞ ) is an infinite graph, L ( P ∞ ) does not exist in general. However, when E ± x ( P ∞ ) is finite we may define Dx L ( P ∞ ) by the difference

$$D _ { x } L ( \mathcal { P } _ { \infty } ) = \sum _ { \{ x , y \} \in E _ { x } ^ { + } ( \mathcal { P } _ { \infty } ) } \psi ( x , y ) - \sum _ { \{ w , z \} \in E _ { x } ^ { - } ( \mathcal { P } _ { \infty } ) } \psi ( w , z ) .$$

The following corollary implies that Dx L ( P ∞ ) is also the almost surely finite limit of Dx L ( P ∞ ∩ B ( x , r )) as r →∞ .

Corollary 17. For all x ∈ R d the set E ± x ( P ∞ ) is finite almost surely, and for any ε &gt; 0 there exists r 0 such that for all r &gt; r 0

$$\mathbb { P } \Big ( D _ { x } L ( \mathcal { P } _ { \infty } ) = D _ { x } L ( \mathcal { P } _ { \infty } \cap B ( x , r ) ) \Big ) \geq 1 - \epsilon .$$

Proof. Inequality (47) of Proposition 15 with t = ∞ yields an r 0 such that E ± x ( P ∞ ) = E ± x ( P ∞ ∩ B ( x , r )) for all x ∈ R d and r &gt; r 0 with probability at least 1 - ε , proving that (50) holds. On the event that Dx L ( P ∞ ) = Dx L ( P ∞ ∩ B ( x , r )), the quantity E ± x ( P ∞ ) is finite. Thus E ± x ( P ∞ ) is finite with probability at least 1 - ε . Since ε is arbitrary, E ± x ( P ∞ ) is finite with probability one. □

We will use the next lemma to replace binomial processes with Poisson processes on large regions.

Lemma 18. For any bounded measurable set A ⊆ R d , as t →∞

$$\mathcal { W } _ { t } \cap A \rightarrow \mathcal { P } _ { \infty } \cap A$$

in total variation.

Proof. Let M and N be the number of points of U t and P t that fall in A , respectively. Once t is large enough that A ⊆ t 1 / d X , the distribution of M is Bin( t , | A | / t ), and the distribution of N is Poi( | A | ). It is well known that this binomial distribution converges in total variation to this Poisson distribution, and so M and N can be coupled so that they are equal with probability approaching 1 as t →∞ . As U t ∩ A can be represented as M points uniformly distributed over A and P ∞∩ A as N points uniformly distributed over A , the two point processes can be coupled to be equal with probability tending to 1. □


<!-- p:22 -->


The next piece of the proof is to show that Dx L ( P ∞ ) is nondeterministic. For any concrete collection of forbidden regions, this is typically straightforward, but to show it in more generality we need to present some technical arguments.

Lemma 19. Suppose E = int E. Then for all x ∈ ∂ E, every open neighborhood of x intersects the interiors of E and E c .

Proof. Let x ∈ ∂ E and let U be an open neighborhood of x . By the definition of the boundary, U intersects E and E c . Since E is open, E = int E . Thus it just remains to show that U intersects int( E c ).

Since E c is an open set contained in E c , we have E c ⊆ int( E c ). Thus int( E c ) c ⊆ E . Now, suppose that U does not intersect int( E c ). Then U ⊆ int( E c ) c ⊆ E . Since U is open, we have U ⊆ int( E ) = E . Hence x ∈ E . But this contradicts x ∈ ∂ E , since E is open and hence contains none of its boundary. □

For a set E ⊆ R d and a direction u ∈ S d - 1 := { u ∈ R d : ∥ u ∥ = 1 } , let Eu = { t ∈ [0 , ∞ ) : tu ∈ E } , which one should think of as the one-dimensional slice of E in direction u . Let σ denote uniform measure on S d - 1 .

Lemma 20. Suppose that E ⊆ R d has Lebesgue measure zero. Then for σ -a.e. u ∈ S d - 1 , the set Eu has one-dimensional Lebesgue measure zero.

Proof. By [5, Theorem 2.49],

$$0 = \int _ { \mathbb { R } ^ { d } } \mathbf 1 \{ x \in E \} \, d x = C \int _ { \mathbb { S } ^ { d - 1 } } \int _ { 0 } ^ { \infty } \mathbf 1 \{ r \in E _ { u } \} r ^ { d - 1 } \, d r \, d \sigma ( u ) ,$$

where C is the volume of S d - 1 . This shows that the inner integrand is zero for σ -a.e. u . As the inner integrand is zero if and only if Eu has measure zero, this completes the proof. □

In the remainder of this section for the convenience we take S ( x , x ) = ∅ for all x ∈ R d . For instance, this convention allows us to write x ∈ R d in place of x ∈ R d \ { y } in the following lemma.

Lemma 21. Suppose that the forbidden regions S ( x , y ) form an ( S , u 0) regular isotropic family (see Definition 3 ). Then for any w, y ∈ R d with w ̸= y, the set { x ∈ R d : w ∈ ∂ S ( y , x ) } has Lebesgue measure zero.

Proof. First note that by translation invariance of the forbidden regions,

$$\{ x \in \mathbb { R } ^ { d } \colon w \in \partial S ( y , x ) \} & = \{ x \in \mathbb { R } ^ { d } \colon w - y \in \partial S ( 0 , x - y ) \} \\ & = \{ x \in \mathbb { R } ^ { d } \colon w - y \in \partial S ( 0 , x ) \} + y .$$

Hence it suffices to prove that { x ∈ R d : w ∈ ∂ S (0 , x ) } has measure zero for all w ∈ R d \ { 0 } .


<!-- p:23 -->


The rest of the argument is easier to follow in R 2 , and we present it there first. Let us identify R 2 with C for convenience. Observe that our isotropic assumption implies that S (0 , re i θ ) = re i θ S (0 , 1). Thus, with T = S (0 , 1), for any w ∈ C \ { 0 } ,

$$\gamma ^ { \ } e ^ { \ } S ( 0 , 1 ) \colon & \text {hints, with } r = \mathbb { S } ( 0 , 1 ) , \text { for any } w \in \mathbb { C } \ \{ \{ 0 \} , \\ & \int _ { \mathbb { R } ^ { 2 } } 1 \{ w \in \partial S ( 0 , x ) \} \, d x = \int _ { 0 } ^ { 2 \pi } \int _ { 0 } ^ { \infty } 1 \{ r ^ { - 1 } e ^ { - i \theta } \in w ^ { - 1 } \partial T \} \, r \, d r \, d \theta \\ & = \int _ { 0 } ^ { 2 \pi } \int _ { 0 } ^ { \infty } 1 \{ t e ^ { - i \theta } \in w ^ { - 1 } \partial T \} \, t ^ { - 3 } \, d t \, d \theta , \\ & = \int _ { 0 } ^ { 2 \pi } \int _ { 0 } ^ { \infty } 1 \{ t e ^ { - i \theta } \in w ^ { - 1 } \partial T \} \, t ^ { - 3 } \, d t \, d \theta , \\$$

making the substitution t = r - 1 . For a given θ , the inner integrand is zero except when t ∈ ( w - 1 ∂ T ) e - i θ , in the notation of Lemma 20. By our assumption in Definition 3 that S has negligible boundary, w - 1 ∂ T has measure zero. Thus the inner integral is zero for a.e. θ by Lemma 20, making the entire integral equal to zero.

In higher dimensions, the proof is more complicated because rotation is more complicated, but the idea is the same. First, we record some facts about rotations of R d around the origin, which can be represented as elements of SO( d ), the special orthogonal group of order d . The group SO( d ) is isomorphic to S d - 1 × SO( d - 1). The decomposition works by specifying a vector u ∈ S d - 1 that a chosen vector u 0 is mapped to (note that we take this chosen vector to be the same as the axis of symmetry for the isotropic family), and then specifying how the orthogonal complement of the span of u is rotated. As a corollary to this decomposition, if u is chosen uniformly over S d - 1 , and the rotation of the orthogonal complement of u is chosen from Haar measure on SO( d - 1), then the result is distributed as Haar measure on SO( d ). We let ρ u ∈ SO( d ) denote the rotation of R d around the origin taking u 0 to u by rotating the plane containing u 0 and u and fixing its orthogonal complement (if u = u 0, take ρ u to be the identity). We use the notation SO( u ⊥ ) to denote the subgroup of SO( d ) fixing u , which as discussed above is isomorphic to SO( d - 1).

Let x ∈ S d - 1 denote x / ∥ x ∥ for x ̸= 0. Let T = S + u 0 / 2 = S (0 , u 0). It follows from our isotropic assumption that

$$\partial S ( 0 , x ) = \| x \| \rho _ { \overline { x } } ( \partial T ) .$$

Thus, with σ d denoting Haar measure on S d , the measure of { x ∈ R d : w ∈ ∂ S (0 , x ) } can be expressed as

$$\int _ { \mathbb { R } ^ { d } } \mathbf 1 \{ w \in \| x \| \rho _ { \overline { x } } ( \partial T ) \} \, d x = C \int _ { 0 } ^ { \infty } \int _ { \mathbb { S } ^ { d } } \mathbf 1 \{ w \in r \rho _ { u } ( \partial T ) \} r ^ { d - 1 } \ d \sigma _ { d } ( u ) \, d r$$

with the (irrelevant) constant determined by the volume of S d - 1 . Letting μ u denote Haar measure on SO( u ⊥ ) normalized to have measure one, we can rewrite the integral as

$$C \int _ { 0 } ^ { \infty } \int _ { \mathbb { S } ^ { d - 1 } } \int _ { \S O ( \mu ^ { - 1 } ) } 1 \{ w \in r \tau \rho _ { u } ( \partial T ) \} r ^ { d - 1 } \, d \mu _ { u } ( \tau ) \, d \sigma _ { d - 1 } ( u ) \, d r \\ = C \int _ { 0 } ^ { \infty } \int _ { \mathbb { S } ^ { d - 1 } } \int _ { \S O ( u ^ { - 1 } ) } 1 \{ r ^ { - 1 } ( \tau \rho _ { u } ) ^ { - 1 } ( w ) \in \partial T \} r ^ { d - 1 } \, d \mu _ { u } ( \tau ) \, d \sigma _ { d - 1 } ( u ) \, d r . \\ \ \ A s . \, w . \, \text { mentioned before } \tau \rho _ { u } \text { with } \tau \text { distributed } \text { as } \mu _ { u } \text { and } \mu _ { \ } \text {distributed } \text { as } \alpha _ { u } \text { . } \text { is } \text { Haar}$$

As we mentioned before, τρ u with τ distributed as μ u and u distributed as σ d - 1 is Haardistributed over SO( d ). By the invariance of Haar measure under multiplication, the distribution of ( τρ u ) - 1 ( w ) under this measure is uniform over ∥ w ∥ S d - 1 . Hence we can rewrite the integral as

$$\int _ { 0 } ^ { \infty } & \int _ { \mathbb { S } ^ { d - 1 } } 1 \{ r ^ { - 1 } \| w \| u \in \partial T \} r ^ { d - 1 } \, d \sigma _ { d - 1 } ( u ) \, d r \\ & = \int _ { \mathbb { S } ^ { d - 1 } } \int _ { 0 } ^ { \infty } 1 \{ t u \in \| w \| ^ { - 1 } \partial T \} t ^ { - ( d + 1 ) } \, d t \, d \sigma _ { d - 1 } ( u ) ,$$


<!-- p:24 -->


substituting t = 1 / r . The inner integral is supported on the ray ( ∥ w ∥ - 1 ∂ T ) u . Since the set ∥ w ∥ - 1 ∂ T has measure zero, the inner integral is thus zero for σ -a.e. u by Lemma 20. □

Lemma 22. Assume the forbidden regions S ( x , y ) are a ( S , u 0) regular isotropic family satisfying Assumption D , and that S ( x , y ) = int S ( x , y ) for all { x , y } ⊆ R d . Let { w, z } ⊆ B (0 , 1) be distinct points. Let μ be a homogeneous Poisson process on R d \ B (0 , 1 + 2 D ) , and let μ ′ = { w, z } ∪ μ . Then a.s.- μ , there exist open balls A , A ′ ⊆ R d such that

$$D _ { x } L ( \mu ^ { \prime } ) \neq D _ { x ^ { \prime } } L ( \mu ^ { \prime } )$$

for all x ∈ A, x ′ ∈ A ′ , and furthermore the center and radii of A and A ′ are measurable random variables.

Proof. Let y ∈ ∂ S ( w, z ) be a point satisfying z ̸∈ ∂ S ( w, y ) and w ̸∈ ∂ S ( z , y ), whose existence is promised by Assumption D. The main idea of the proof is that adding to μ ′ any point close to y has the same effect on G ( μ ′ ) except for possibly causing the deletion of the edge w z . Note that w z is always present in G ( μ ′ ), as S ( w, z ) has at most diameter 2 D and hence is contained in B (0 , 1 + 2 D ), while μ ′ has no points in B (0 , 1 + 2 D ) besides w and z .

Step 1. A.s.- μ , we have b ̸∈ ∂ S ( y , a ) for all { a , b } ⊆ μ ′ with a ̸= b . By Assumption D, w ̸∈ ∂ S ( y , z ) and z ̸∈ ∂ S ( y , w ). Since ∂ S ( y , z ) and ∂ S ( y , w ) have measure zero, almost surely no points of μ fall in either of these sets. Now we are left to show that

$$b \notin \partial S ( y , a ) \ a s . \text {, for } a \in \mu , \, b \in \mu ^ { \prime } , \, a \neq b .$$

For a point process configuration χ , let

$$f ( \chi , a ) = \# \left ( \left ( ( \{ w , z \} \cup \chi ) \ \{ a \} \right ) \cap \partial S ( y , a ) \right ) .$$

Our goal is then to show that ∑ a ∈ μ f ( μ, a ) = 0 a.s. By Mecke's formula,

$$\mathbb { E } \sum _ { a \in \mu } f ( \mu , a ) & = \mathbb { E } \int _ { \mathbb { R } ^ { d } \langle B ( 0 , 1 + 2 D ) } f ( \mu \cup \{ a \} , a ) \, d a \\ & = \int _ { \mathbb { R } ^ { d } \langle B ( 0 , 1 + 2 D ) } \mathbb { E } \left [ \# ( ( \{ w , z \} \cup \mu ) \cap \partial S ( y , a ) ) \right ] d a , \\ \intertext { w i t h e t r o n s i t i o n $ f $ t h e i n g a l $ a $ t h e i n d e x p a t i o n $ i s f e i n t i o n $ w h a n d $ t h e i n g a l $ a $ t h e i n d e x p a t i o n $ }$$

with the transposition of the integral and expectation justified by non-negativity of the integrand. For any a ∈ R d , the set ∂ S ( y , a ) has measure zero by our assumption that S has negligible boundary, and hence no points of μ are in ∂ S ( y , a ) a.s. Thus we can simplify the above expression to

$$\exp ( 3 s o t ) & = 0 \\ & \mathbb { E } \sum _ { a \in \mu } f ( \mu , a ) = \int _ { \mathbb { R } ^ { d } } \# ( \{ w , z \} \cap \partial S ( y , a ) ) \, d a \\ & = \int _ { \mathbb { R } ^ { d } } ( \{ w \in \partial S ( y , a ) \} + \{ z \in \partial S ( y , a ) \} ) \, d a , \\ & \text {with the annotation removed, above there is no longer any randomness in the integer $\mathbb{ }Th_{s}$} .$$

with the expectation removed because there is no longer any randomness in the integrand. Thus it follows from Lemma 21 that the integrand is zero except on a set of measure zero, proving that E ∑ a ∈ μ f ( μ, a ) = 0. This proves (52), completing the proof of this step.

Step 2: A.s.- μ , we have y ̸∈ ∂ S ( a , b ) for { a , b } ⊂ μ ′ , { a , b } ̸= { w, z } . This step follows by essentially the same proof as for Step 1.


<!-- p:25 -->


In the next step, we say that E + x ( μ ′ ) and E + y ( μ ′ ) are equivalent if the set of edges E + x ( μ ′ ) is equal to the set E + y ( μ ′ ) when all edges of the form { y , a } in the latter are replaced by { x , a } . Note that we do not need a definition like this for E - x ( μ ′ ) and E - y ( μ ′ ), since edges with vertices x or y do not appear in these collections.

To prepare for the next step, recall that the Hausdorff metric between two subsets A and B of R d is defined as

$$d _ { H } ( A , B ) = \inf \{ \epsilon > 0 \colon A \subseteq B _ { \epsilon } , \, B \subseteq A _ { \epsilon } \} \quad \text {where} \quad F _ { \epsilon } = \bigcup _ { x \in F } \{ y \in \mathbb { R } ^ { d } \colon \| y - x \| \leq \epsilon \} .$$

It is clear that when the forbidden regions form a regular isotropic family, the map ( x , y ) ↦→ S ( x , y ) is Hausdorff continuous in ( x , y ) ∈ R d × R d .

Step 3. For some random radius ρ &gt; 0, it holds for all x ∈ B ( y , ρ ) that E + x ( μ ′ ) is equivalent to E + y ( μ ′ ), and that E - x ( μ ′ ) is equal to either E - y ( μ ′ ) or E - y ( μ ′ ) ∪ {{ w, z }} . d d by Propoprobability, is bounded )

Let R = R S ( B ( y , 1) ; μ ′ ; R ). The set R S ( B ( y , 1) ; P ∞; R ) is bounded a.s.- P ∞ sition 9. Since μ is distributed as P ∞ conditional on an event of positive R S ( B ( y , 1) ; μ ; R d ) is bounded a.s.- μ . As μ ⊆ μ ′ , Lemma 5 shows that the set R a.s.- μ . Recall by using (11) that the addition of any point x ∈ B ( y , 1) changes the graph G ( μ ′ only by the addition of edges xa and deletion of edges ab for a , b ∈ R .

Step 1 shows that for each a ∈ μ ′ ∩ R , the set ∂ S ( y , a ) does not contain any points of ( μ ′ \ { a } ) ∩ R . Since ( μ ′ \ { a } ) ∩ R is almost surely finite, the set ∂ S ( y , a ) has positive distance from ( μ ′ \{ a } ) ∩ R , as both sets are compact. By the Hausdorff continuity of the map S , there is a positive distance ρ + a such that for all x ∈ B ( y , ρ + a ), the set ∂ S ( x , a ) avoids ( μ ′ \{ a } ) ∩ R . Set ρ + to be the minimum of ρ + a over the almost surely finitely many a ∈ μ ′ ∩ R . Then for all x ∈ B ( y , ρ + ), the collections E + x ( μ ′ ) and E + y ( μ ′ ) are equivalent. Standard continuity considerations yield that the ρ a , and therefore ρ , can be built to be measurable random variables.

Step 2 implies that for all { a , b } ⊆ μ ′ ∩ R except for { w, z } , the set ∂ S ( a , b ) has a positive distance ρ - ab from y . Set ρ - as the minimum of ρ - ab over this almost surely finite collection of { a , b } . Then for x ∈ B o ( y , ρ - ), as y ∈ ∂ S ( w, z ), and S ( w, z ) is open, it holds that E - x ( μ ′ ) is equal to either E - y ( μ ′ ) or E - y ( μ ′ ) ∪ {{ w, z }} . Taking ρ less than ρ + and ρ - completes the step.

###### Step 4. Construction of A , A ′ satisfying (51).

Let A 0 = B o ( y , ρ ′ ) ∩ int S ( w, z ) and A ′ 0 = B o ( y , ρ ′ ) ∩ int( S ( w, z ) c ) for ρ ′ ∈ (0 , ρ ) to be specified later. By Lemma 19, both sets A 0 and A ′ 0 are open and nonempty, thus we define A and A ′ to be the balls with maximal radii centered respectively at arbitrary points y 0 ∈ A 0 and y ′ 0 ∈ A ′ 0 , chosen in some measurable way. By the previous step, E + x ( μ ′ ) and E + y ( μ ′ ) are equivalent for x ∈ A ∪ A ′ . For x ′ ∈ A ′ , we have E - x ′ ( μ ′ ) = E - y ( μ ′ ), and for x ∈ A , we have E - x ( μ ′ ) = E - y ( μ ′ ) ∪ {{ w, z }} . Thus for x ∈ A and x ′ ∈ A ′ ,

$$D _ { x ^ { \prime } } L ( \mu ^ { \prime } ) - D _ { x } L ( \mu ^ { \prime } ) = \psi ( w , z ) + \sum _ { a \colon \{ a , x \} \in E _ { x } ^ { + } ( \mu ^ { \prime } ) } \left ( \psi ( a , x ^ { \prime } ) - \psi ( a , x ) \right ) .$$

By the continuity of ψ , and that E + x ( μ ′ ) is finite, the sum can be made arbitrarily small over all x ∈ A , x ′ ∈ A ′ by choosing ρ ′ small enough, a choice which can be made in a measurable way with respect to μ . If we choose ρ ′ to make the sum smaller than ψ ( w, z ), non-zero by hypothesis as w ̸= z , then (51) holds for x ∈ A , x ′ ∈ A ′ . □

Theorem 23. Assume that the forbidden regions S ( x , y ) are a ( S , u 0) regular isotropic family satisfying Assumption D . Then for all x ∈ R d , the random variable Dx L ( P ∞ ) is nondeterministic.


<!-- p:26 -->


Proof. As int S ( x , y ) ⊆ int S ( x , y ) ⊆ S ( x , y ), the sets S ( x , y ) and int S ( x , y ) differ only on ∂ S ( x , y ), a set of measure zero. For each of the almost surely countably many pairs { a , b } ⊂ P ∞ , there are almost surely no points of P ∞ on ∂ S ( a , b ) besides a and b . Thus G ( P ∞ ) is almost surely unaffected by replacing each forbidden region S ( x , y ) by int S ( x , y ). If B = int A , then B ⊆ A hence B ⊆ A , and taking interiors and using that B is open yields B ⊆ int B ⊆ int A = B , and thus B = int B . Hence we can assume that S ( x , y ) = int S ( x , y ) for all x , y .

Let w and z be chosen uniformly and independently from B (0 , 1), and let μ be a homogeneous Poisson process with intensity 1 on R d \ B (0 , 1 + 2 D ). With positive probability, P ∞ has exactly two points in B (0 , 1 + 2 D ), both of which are contained in B (0 , 1). Conditional on this event, P ∞ is distributed as μ ′ := { w, z } ∪ μ . By Lemma 22, a.s.- μ there exist open sets A , A ′ ⊆ R d such that Dx L ( μ ′ ) ̸= Dx ′ L ( μ ′ ) for all x ∈ A and x ′ ∈ A ′ . Thus, with positive probability, there exist open sets A , A ′ ⊆ R d such that Dx L ( P ∞ ) ̸= Dx ′ L ( P ∞ ) for all x ∈ A and x ′ ∈ A ′ .

Suppose that Dx L ( P ∞ ) = c a.s. for some x ∈ R d and some constant c . By the translation invariance of P ∞ , this holds for all x ∈ R d . Hence it holds almost surely that Dx L ( P ∞ ) = c for all x in a countable dense set of R d . But this contradicts the conclusion of the previous paragraph. □

We now use Theorem 23 to show that if x and y are far enough apart, then with positive probability adding x or y to the process produces different effects on L .

Lemma 24. Assume the conditions of Theorem 4 . There exist constants a &gt; b , r 0 ∈ (0 , ∞ ) and p 0 ∈ (0 , 1] such that for all r &gt; r 0 the following statement holds: for all x , y ∈ R d , if the r-balls around x and y are disjoint and t &gt; t 1( x , y , r ) = max { t 0( x , r ) , t 0( y , r ) , t 2( r ) } where t 2 is a function depending only on r, then

$$\mathbb { P } \left ( D _ { x } L ( \mu ) > a \ a n d \ D _ { y } L ( \mu ) < b \right ) \geq p _ { 0 }$$

for μ = P t or μ = U t .

Proof. Let first μ = U t . By Theorem 23, and that the distribution of Dz L ( P ∞ ) does not depend on z by translation invariance, there exist a &gt; b and p &gt; 0 such that for all z ∈ R d ,

$$\mathbb { P } \Big ( D _ { z } L ( \mathcal { P } _ { \infty } ) > a \Big ) \geq p \quad \text {and} \quad \mathbb { P } \Big ( D _ { z } L ( \mathcal { P } _ { \infty } ) < b \Big ) \geq p .$$

Let p 0 = ( p - ε ) 2 - 3 ε , choosing ε &gt; 0 small enough that p 0 &gt; 0. By Corollary 17, for all sufficiently large r and for all z ∈ R d the random variables Dz L ( P ∞ ) and Dz L ( P ∞ ∩ B ( z , r )) are within ε in total variation distance, and hence

$$\mathbb { P } ( D _ { z } L ( \mathcal { P } _ { \infty } \cap B ( z , r ) ) & > a ) \geq p - \epsilon \quad \text {and} \\ \mathbb { P } ( D _ { z } L ( \mathcal { P } _ { \infty } \cap B ( z , r ) ) & < b ) \geq p - \epsilon .$$

Next, from the total variation convergence given by invoking Lemma 18 with A = B ( x , r ) ∪ B ( y , r ), for all r large enough that (54) holds, and t &gt; t 2( r ) depending on r , for any { x , y } ⊆ R d satisfying ∥ x - y ∥ &gt; 2 r ,

$$\mathbb { P } ( D _ { x } L ( \mathcal { U } _ { t } \cap B ( x , r ) ) > a \text { and } D _ { y } L ( \mathcal { U } _ { t } \cap B ( y , r ) ) < b ) \\ \geq & \mathbb { P } ( D _ { x } L ( \mathcal { P } _ { \infty } \cap B ( x , r ) ) > a \text { and } D _ { y } L ( \mathcal { P } _ { \infty } \cap B ( y , r ) ) < b ) - \epsilon \\ \geq & ( p - \epsilon ) ^ { 2 } - \epsilon ,$$


<!-- p:27 -->


with the last line following from (54) and the independence of P ∞∩ B ( x , r ) and P ∞∩ B ( y , r ). By Proposition 15, for all sufficiently large r and all t &gt; max { t 0( x , r ) , t 0( y , r ) } , it holds that

$$\mathbb { P } ( D _ { x } L ( \mathcal { W } _ { t } \cap B ( x , r ) ) & = D _ { x } L ( \mathcal { W } _ { t } ) ) \geq 1 - \epsilon \ \text { and} \\ \mathbb { P } ( D _ { y } L ( \mathcal { W } _ { t } \cap B ( y , r ) ) & = D _ { y } L ( \mathcal { W } _ { t } ) ) \geq 1 - \epsilon .$$

Hence, by a union bound,

$$\mathbb { P } \left ( D _ { x } L ( \mathcal { U } _ { t } \cap B ( x , r ) ) = D _ { x } L ( \mathcal { U } _ { t } ) \text { and } D _ { y } L ( \mathcal { U } _ { t } \cap B ( y , r ) ) = D _ { y } L ( \mathcal { U } _ { t } ) \right ) \geq 1 - 2 \epsilon .$$

Now, taking any r 0 so that (54) and (56) hold for all r &gt; r 0, for all t &gt; t 1( x , y , r ), by (55) and (56),

$$\mathbb { P } \Big ( D _ { x } L ( \mathcal { W } _ { t } ) > a \text { and } D _ { y } L ( \mathcal { W } _ { t } ) < b \Big ) \geq ( p - \epsilon ) ^ { 2 } - \epsilon - 2 \epsilon = p _ { 0 } .$$

The proof for the Poisson case is the same, except that the step involving Lemma 18 is unnecessary. □

We will need the following elementary lemma, which is essentially just Markov's inequality applied to a bounded random variable.

Lemma 25. Suppose that X is a random variable supported on [0 , n ] , and E X ≥ np. Then

$$\mathbb { P } \Big ( X > \frac { n p } { 2 } \Big ) \geq \frac { p } { 2 - p } .$$

Proof. Let Y = n - X . Then E Y ≤ n (1 - p ), and applying Markov's inequality to Y yields

$$\mathbb { P } \left ( X \leq \frac { n p } { 2 } \right ) = \mathbb { P } \left ( Y \geq n \left ( 1 - \frac { p } { 2 } \right ) \right ) \leq \frac { 1 - p } { 1 - p / 2 } ,$$

yielding (57). □

In the remainder of this section let a , b , r 0, and p 0 be the constants given by Lemma 24. For some m &gt; 0 and 1 &lt; r &lt; ∞ , we say that a pair of points x and y with ∥ x - y ∥ &gt; 2 r is ( m , r , t )- influential for μ if

INFLUENTIAL1( μ ): There exist sets A ⊆ B ( x , 1) and B ⊆ B ( y , 1) each of Lebesgue measure m such that Dz L ( μ ) &gt; a for z ∈ A and Dz L ( μ ) &lt; b for z ∈ B , and INFLUENTIAL2( μ ): RS ( B ( x , 1) ; μ ; t 1 / d X ) ≤ r and RS ( B ( y , 1) ; μ ; t 1 / d X ) ≤ r .

Note that a pair of influential points for μ are not required to be, and in fact will in general not be, points of μ . We have made the radii of the balls containing x and y equal to 1 in these definitions, but the value is unimportant.

Lemma 26. Assume the conditions of Theorem 4 . There exist constants m ∈ (0 , ∞ ) , p ∈ (0 , 1] and r ∈ (1 , ∞ ) such that if x and y are any two points such that the ( r + 1) -balls centered around each are disjoint, then for all sufficiently large t

$$\mathbb { P } \left ( ( x , y ) \ i s \ ( m , r , t ) \text {-infty} \, \forall u e n t i a l \, f o r \ \mu \right ) \geq p$$

for μ = P t and μ = U t .

Proof. By Proposition 9, for all { x , y } ⊆ R d and t &gt; max { t 0( x , r ) , t 0( y , r ) } , as r → ∞ the probability of INFLUENTIAL2( μ ) is lower bounded by a quantity tending to one, not depending

$$a n d$$


<!-- p:28 -->


on { x , y } . With r 0 and p 0 the constants given by Lemma 24, let p ′ 0 = p 0 / (2 - p 0), and choose r &gt; r 0 large enough that INFLUENTIAL2( μ ) holds with probability at least 1 - p ′ 0 / 2. Let X and Y be independent and distributed uniformly over B ( x , 1) and B ( y , 1), respectively. Let

$$P ( \mu ) & \coloneqq \mathbb { P } ( D _ { X } L ( \mu ) > a \text { and } D _ { Y } L ( \mu ) < b \ | \ \mu ) \\ & = \mathbb { P } ( D _ { X } L ( \mu ) > a \ | \ \mu ) \mathbb { P } ( D _ { Y } L ( \mu ) < b \ | \ \mu ) .$$

Note that

$$\mathbb { P } \Big ( D _ { X } L ( \mu ) > a \ | \ \mu ) = \frac { | \{ z \in B ( x , 1 ) \colon D _ { z } L ( \mu ) > a \} | } { | B ( x , 1 ) | } ,$$

with an analogous statement holding for the second factor in (58). By Lemma 24, using that the r -balls around points in B ( x , 1) and B ( y , 1) do not intersect, by averaging X and Y over their supports we see that for t &gt; sup u ∈ B ( x , 1) ,v ∈ B ( y , 1) t 1( u , v, r ) we have E P ( μ ) ≥ p 0. Since P ( μ ) is supported on [0 , 1], we apply Lemma 25 with n = 1 and p = p 0 to conclude that P ( P ( μ ) &gt; p 0 / 2) ≥ p 0 / (2 - p 0) = p ′ 0 . If P ( μ ) ≥ p 0 / 2, then both factors in (58) are larger than p 0 / 2. Therefore, with probability at least p ′ 0 , the pair ( x , y ) satisfies INFLUENTIAL1( μ ) with m = p 0 | B ( x , 1) | / 2.

Since INFLUENTIAL1( μ ) holds with probability at least p ′ 0 and INFLUENTIAL2( μ ) holds with probability at least 1 - p ′ 0 / 2, by a union bound both hold simultaneously with probability at least p ′ 0 / 2. □

From now on, we take m , r , and p to be constants provided by Lemma 26.

Lemma 27. Assume the conditions of Theorem 4 . Let INFLUENTIAL( μ, t , β ) be the event that there are at least β t pairs of ( m , r , t ) -influential points for μ , all of whose ( r + 1) -neighborhoods are disjoint and contained in t 1 / d X . For some β, q &gt; 0 independent of t, for either μ = P t or μ = U t , it holds for all sufficiently large t that

P (INFLUENTIAL( μ, t , β )) ≥ q .

Proof. For some β ′ &gt; 0, for all sufficiently large t one can place at least 2 ⌈ β ′ t ⌉ points in t 1 / d X so that all points have disjoint ( r + 1)-neighborhoods contained in t 1 / d X . Let n = ⌈ β ′ t ⌉ , and arbitrarily form these 2 n points into n disjoint pairs. For large enough t , by Lemma 26, each pair has probability at least p of being ( m , r , t )-influential, so the expected number of such ( m , r )- influential pairs is at least np . By Lemma 25, there are at least np / 2 such pairs with probability at least p / (2 - p ). Now we can take q = p / (2 - p ) and β = p β ′ / 3, say. □

Proof of Theorem 4. It suffices to show that there exists v such that Var L ( μ ) ≥ v t where μ is either Poisson on t 1 / d X with intensity 1 or binomial with ⌈ t ⌉ points. Indeed, as ψ ( ax , ay ) = a α ψ ( x , y ) for any a &gt; 0, we have L ( a μ ) = a α L ( μ ), where a μ = { ax , x ∈ μ } . Hence, when Var L ( μ ) ≥ v t , scaling a process μ on t 1 / d X to a process on X , we have

$$\text {Var} ( L ( t ^ { - 1 / d } \mu ) ) = \text {Var} ( t ^ { - \alpha / d } L ( \mu ) ) = t ^ { - 2 \alpha / d } \text {Var} ( L ( \mu ) ) \geq v t ^ { 1 - 2 \alpha / d } .$$

The argument will go by splitting μ into a sum of independent point processes μ 1 and μ 2. Initially, take μ 1 to be a deterministic set of points such that INFLUENTIAL( μ 1 , t , β ) holds for some β &gt; 0, and define μ 2 as a point process on t 1 / d X that is either Poisson with intensity 1 / 2 or binomial with ⌊ t / 2 ⌋ points. We start by arguing that Var L ( μ 1 ∪ μ 2) &gt; Ct for some C &gt; 0.


<!-- p:29 -->


Since INFLUENTIAL( μ 1 , t , β ) holds, there exist point pairs ( x 1 , y 1) , . . . , ( xn , yn ) with n ≥ β t with sets Ai ⊆ B ( xi , 1) and Bi ⊆ B ( yi , 1) of measure m such that INFLUENTIAL1( μ 1) and INFLUENTIAL2( μ 1) hold for each pair. For some γ &gt; 0 to be specified, consider the event

$$F & = \{ | \{ 1 \leq i \leq n \colon \left | \mu _ { 2 } \cap ( B ( x _ { i } , r + 1 ) \cup B ( y _ { i } , r + 1 ) ) \right | = \left | \mu _ { 2 } \cap ( A _ { i } \cup B _ { i } ) \right | = 1 \} | \\ & \geq \gamma n \} \, ,$$

that is, that for at least γ n of the pairs ( xi , yi ), exactly one point of μ 2 lands in the ( r + 1)- neighborhoods of xi and yi , and it lands in either Ai or Bi . We claim that F occurs with positive probability not depending on t . Indeed, for any fixed i , the process μ 2 will satisfy

$$\left | \mu _ { 2 } \cap ( B ( x _ { i } , r + 1 ) \cup B ( y _ { i } , r + 1 ) ) \right | = \left | \mu _ { 2 } \cap ( A _ { i } \cup B _ { i } ) \right | = 1$$

with at least some fixed, positive probability for large enough t . Choosing γ small enough, the event F then holds with some positive probability independent of t by Lemma 25.

Now, the idea is that given that μ 2 has exactly one point in either Ai or Bi , it is equally likely to be in either. Conditional on F , we then essentially have γ n = Ω ( t ) coin flips, each contributing a constant term to Var L ( μ 1 ∪ μ 2). To put this into practice, we partition μ 2 into { X 1 , . . . , Xl } and { Y 1 , . . . , Yl ′ } , where the first set consists of the points of μ 2 that are contained in Ai ∪ Bi for some i satisfying (59). Thus l ≥ γ n when F holds. Now, let  ̃ μ = μ 1 ∪{ Y 1 , . . . , Yl ′ } , and express L ( μ 1 ∪ μ 2) as the telescoping sum

$$L ( \mu _ { 1 } \cup \mu _ { 2 } ) = L ( \widetilde { \mu } ) + D _ { X _ { 1 } } L ( \widetilde { \mu } ) + D _ { X _ { 2 } } L ( \widetilde { \mu } \cup \{ X _ { 1 } \} ) + \dots + D _ { X _ { l } } L ( \widetilde { \mu } \cup \{ X _ { 1 } , \dots , X _ { l - 1 } \} ) .$$

By INFLUENTIAL2( μ 1), for any 1 ≤ j ≤ l we have RS ( X j ; μ 1 ; t 1 / d X ) ≤ r . Because X j satisfies (59) for some i , all points of μ 2 except for X j lie outside of B ( X j , r ). By (15) of Lemma 7,

$$D _ { X _ { j } } L ( \widetilde { \mu } \cup \{ X _ { 1 } , \dots , X _ { j - 1 } \} ) = D _ { X _ { j } } L ( \mu _ { 1 } ) .$$

Thus we can rewrite L ( μ 1 ∪ μ 2) as

$$L ( \mu _ { 1 } \cup \mu _ { 2 } ) = L ( \widetilde { \mu } ) + D _ { X _ { 1 } } L ( \mu _ { 1 } ) + D _ { X _ { 2 } } L ( \mu _ { 1 } ) + \cdots + D _ { X _ { l } } L ( \mu _ { 1 } ) .$$

By construction, X j falls into Ai ∪ Bi for exactly one choice of i . Conditional on F , the point X j is equally likely to be in Ai or Bi . Furthermore, which of these it lands in is independent for 1 ≤ j ≤ l conditional on F . If X j lands in Ai , then DXj L ( μ 1) &gt; a , and if X j lands in Bi , then DXj L ( μ 1) &lt; b , by the definition of INFLUENTIAL1( μ 1). Thus, (60) expresses L ( μ 1 ∪ μ 2) as a sum of terms that are conditionally independent given F and  ̃ μ and which each have conditional variance bounded from below, showing that

$$\text {Var} \left ( L ( \mu _ { 1 } \cup \mu _ { 2 } ) \left | \, \mathbf 1 _ { F } , \widetilde { \mu } \right ) \geq C l \geq C \gamma n \geq C \gamma \beta t$$

on the event F , for some absolute constant C &gt; 0. As F occurs with probability that can be bounded away from zero uniformly for all t , and

$$\text {Var} \, L ( \mu _ { 1 } \cup \mu _ { 2 } ) & = \mathbb { E } \, \text {Var} \left ( L ( \mu _ { 1 } \cup \mu _ { 2 } ) \left | \, 1 _ { F } , \widetilde { \mu } \right ) + \text {Var} \, \mathbb { E } \left ( L ( \mu _ { 1 } \cup \mu _ { 2 } ) \left | \, 1 _ { F } , \widetilde { \mu } \right ) \right ) \\ & \geq \mathbb { E } \, \text {Var} \left ( L ( \mu _ { 1 } \cup \mu _ { 2 } ) \left | \, 1 _ { F } , \widetilde { \mu } \right ) ,$$

we have shown that Var L ( μ 1 ∪ μ 2) grows at least as a constant times t .

To complete the proof, we now let μ 1 be a point process on t 1 / d X , independent of μ 2, and either Poisson with intensity 1 / 2 or binomial with ⌈ t / 2 ⌉ points. Thus μ can be expressed as μ 1 ∪ μ 2. By Lemma 27, for all t sufficiently large, the event INFLUENTIAL( μ 1 , t , β ) holds with

probability at least q for some β, q &gt; 0 not depending on t . (Strictly speaking, we replace X by 2 1 / d X and t by t / 2 when applying Lemma 27.) By the previous argument, the variance of L ( μ ) conditional on INFLUENTIAL( μ 1 , t , β ) for sufficiently large t is at least Ct for a constant C &gt; 0 not depending on t , from which the theorem follows. □


<!-- p:30 -->


### Acknowledgments

The work of the first author was partially supported by NSA-H98230-15-1-0250, and of the second author by NSF grant DMS-1401479.
