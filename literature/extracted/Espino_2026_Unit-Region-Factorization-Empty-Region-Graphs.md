---
id: "Espino_2026_Unit-Region-Factorization-Empty-Region-Graphs"
source_pdf: "../pdf/Espino_2026_Unit-Region-Factorization-Empty-Region-Graphs.pdf"
source_filename: "Espino_2026_Unit-Region-Factorization-Empty-Region-Graphs.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "excellent"
extraction_score: 108.0
visual_assets: "disabled"
references_file: "../references/Espino_2026_Unit-Region-Factorization-Empty-Region-Graphs.references.md"
---

<!-- p:1 -->

## Unit-Region Factorization for Empty-Region Proximity Graphs

Heriberto Espino-Montelongo a , ∗ , Héctor Maravillo b

a Universidad de las Américas Puebla, Ex Hacienda Santa Catarina Mártir S/N, San Andrés Cholula, 72810, Puebla, Mexico

b Universidad Autónoma de la Ciudad de México, Dr. García Diego 168, Col. Doctores, Alcaldía Cuauhtémoc, Ciudad de México, 06720, Mexico

## ARTICLE INFO

Keywords : Empty-region graph proximity graph Poisson point process Palm distribution computational geometry stochastic geometry

### 1. Introduction

### ABSTRACT

Many proximity graphs join two sites when a region determined by the pair contains no other site. We study finite empty-region rules for which the region associated with each pair is obtained from a fixed normalized Borel region by translation, rotation, and uniform scaling. If aK denotes the volume of the unit region, then the corresponding pairwise region has volume aK l d p,q , where d is the dimension and l p,q is the pair length. Thus, at the first-order stochastic level, the geometry of the rule enters through the single scalar aK .

For a homogeneous Poisson process, this factorization yields the exact fixed-pair void probability and, for any Borel unit-region rule, the incident-edge length intensity, mean out-degree, and normalized incident-edge length law. For symmetric rules, the out-degree coincides with the ordinary degree. The normalized incident-edge length law is Weibull with shape parameter d and scale ( ρaK ) -1 ∕ d . Explicit formulas for the d -dimensional volume aK are given for several proximity graphs, including the Gabriel graph, the relative-neighborhood graph, lune-based β -skeletons, and stepping-stone graphs. In the planar case, the framework also covers the circle-based β -skeleton through Veltkamp's diagonal parameterization, together with selected prescribed two-ball regions associated with Veltkamp's γ -neighborhood construction.

Proximity graphs are graphs defined on point sets in Euclidean space, in which two points are adjacent whenever they are sufficiently close according to some geometric criterion. A major subclass is based on empty-region rules: a region is associated with a candidate pair of points, and the pair is adjacent whenever this region contains no other points of the set (Jaromczyk and Toussaint, 1992; Cardinal, Collette and Langerman, 2009). Originally, motivated by their main applications, proximity graphs were defined for point sets in the plane, but their definition naturally extends to higher-dimensional spaces (Jaromczyk and Kowaluk, 1991; Devroye, 1988). Classical examples include the Gabriel graph, the relative neighborhood graph, the nearest neighbor graphs, β -skeletons, and the sphere-ofinfluence graph (Jaromczyk and Toussaint, 1992; Mitchell and Mulzer, 2017; Mathieson and Moscato, 2019). Proximity graphs have been used in geographic analysis (Gabriel and Sokal, 1969), data mining (Toussaint, 2005), topological data analysis (Correa and Lindstrom, 2011; Jurkiewicz, 2023), machine learning (Marchette, 2005; Toussaint and Berzan, 2012), modeling urban street networks (Watanabe, 2008; Maravillo, Calvillo and Treviño-Aguilar, 2023), communication and wireless-network design (Iguchi-Cartigny, Ruiz, Simplot-Ryl, Stojmenovic and Yago, 2008), and even in archaeological studies (Jiménez-Badillo and Chapman, 2002). For further applications, see (Jaromczyk and Toussaint, 1992; Toussaint, 2014a,b).

∗ Corresponding author.

hector.maravillo@uacm.edu.mx Proximity graphs have been extensively studied from both algorithmic and theoretical perspectives (Cimikowski, 1990; Hurtado, Liotta and Meijer, 2003; Cardinal et al., 2009; Bose, Dujmović, Hurtado, Iacono, Langerman, Meijer, Sacristán, Saumell and Wood, 2012; Kowaluk and Majewska, 2015). Their probabilistic properties have also received considerable attention for graphs built on random point sets. Devroye (1988) determined the expected size of empty-region graphs on n i.i.d. points with an arbitrary density in R d under suitable regularity and symmetry assumptions on the associated regions. Alonso, Méndez-Bermúdez and Estrada (2019) computationally analyzed the average degree of β -skeletons constructed on points uniformly distributed in the planar unit square. Watanabe (2008) derived the expected length of the edges of the relative neighborhood graph of a planar homogeneous Poisson process in terms of its intensity. More recently, Sambale, Schulte and Thaele (2026) established limit laws for longest edges in several empty-region graphs generated by stationary Poisson point processes.

The present paper continues this line of research on the probabilistic properties of proximity graphs. We consider empty-region graphs generated by a homogeneous Poisson point process in R d , allowing arbitrary defining regions that are Borel sets with finite positive Lebesgue measure. This framework includes well-known examples such as the Gabriel graph, the relative neighborhood graph, and β -skeletons. Our main contributions are summarized below:

heriberto.espinomo@udlap.mx (H. Espino-Montelongo); (H. Maravillo)

0009-0009-1230-2931

ORCID(s):

0000-0002-6101-1964

(H. Maravillo)

(H. Espino-Montelongo);

Geometric factorization. The paper identifies a class of finite similarity-region empty-region rules and proves that the region S ( p, q ) associated with each pair p ≠ q has volume


<!-- p:2 -->


$$\lambda _ { d } ( S ( p , q ) ) = a _ { K } \| p - q \| ^ { d } ,$$

where λd is the d -dimensional Lebesgue measure and aK is the volume of the unit region. Thus the geometric dependence of every rule in the class is reduced to one regionvolume constant.

Poisson-Palm consequences. For a homogeneous Poisson process with intensity ρ , the factorization yields the exact fixed-pair void probability, the mean out-degree, and the normalized incident-edge length law. For symmetric rules, the out-degree is the ordinary degree. The normalized incident-edge length law is Weibull with shape parameter d and scale parameter ( ρaK ) -1 ∕ d .

##### Explicit ball-generated constants.

Using hyperspherical-cap formulas, the paper derives explicit d -dimensional volume constants for lune-based β - skeleton regions. In the planar case, the same cap formulas apply to the diagonal Veltkamp subfamily, which recovers the circle-based β -skeleton, and to selected prescribed twoball regions associated with Veltkamp's γ -neighborhood construction.

Stepping-stone volume constant. For the stepping-stone diversion region, the paper derives a dimension-uniform integral representation for the volume of the unit region. This makes the unit-region factorization explicit for the stepping-stone family and therefore yields its Poisson-Palm consequences.

The remainder of the paper is organized as follows. Section 2 establishes the notation and standing assumptions. Section 3 introduces the similarity-region framework and proves the unit-region volume factorization. Section 4 derives its consequences for homogeneous Poisson input, including the fixed-pair void probability and the Palm incident-edge results. Section 5 evaluates the region-volume constants for the principal examples. Section 6 discusses the scope, limitations, and possible extensions of the framework. Section 7 concludes.

### 2. Notation and standing conventions

For x ∈ R d and r ≥ 0 , let

Throughout the paper, we work in the Euclidean space R d , with ambient dimension d ≥ 2 , equipped with the Euclidean norm ‖ ⋅ ‖ and the d -dimensional Lebesgue measure λd . We write 0 for the origin and e 1 = (1 , 0 , ... , 0) for the first coordinate vector.

$$B ( x , r ) \colon = \{ y \in \mathbb { R } ^ { d } \ \colon \| y - x \| \leq r \} \quad \ \ \ ( 2 . 1 ) \quad \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \$$

be the closed Euclidean ball. Its volume is

$$\lambda _ { d } ( B ( x , r ) ) = \kappa _ { d } r ^ { d } , & & ( 2 . 2 ) & \mod { \mathbf r } _ { \colon } \\$$

where

$$\kappa _ { d } \colon = \lambda _ { d } ( B ( 0 , 1 ) ) = \frac { \pi ^ { d / 2 } } { \Gamma ( 1 + d / 2 ) } ,$$

and Γ is Euler's gamma function.

For every candidate pair p ≠ q ∈ R d , define

$$\ell _ { p , q } \colon = \| p - q \| \, , \quad u _ { p , q } \colon = \frac { q - p } { \ell _ { p , q } } .$$

Thus l p,q is the pair length and up,q is the unit vector from p to q . When a rotation is needed, Rp,q ∈ O ( d ) denotes an orthogonal map satisfying Rp,q e 1 = up,q . The affine map

$$T _ { p , q } ( z ) \colon = p + \ell _ { p , q } R _ { p , q } z$$

sends the normalized segment [ 0 , e 1 ] to [ p, q ] .

The symbol K ⊂ R d denotes a normalized unit region, and

$$a _ { K } \colon = \lambda _ { d } ( K )$$

denotes its unit volume.

Let V ⊂ R d be a finite or locally finite set of points. To each pair of distinct points p, q ∈ V , associate a region or neighborhood S ( p, q ) ⊂ R d . A neighborhood graph, also called proximity graph, is a graph G = ( V , E ) whose edge set is determined by a property p of these regions: namely, ( p, q ) ∈ E if and only if S ( p, q ) satisfies  (Jaromczyk and Toussaint, 1992). When the property  consists of the empty-region rule

$$S ( p , q ) \cap ( V \ \{ p , q \} ) = \emptyset .$$

For a nonsymmetric rule, this condition defines a directed arc p → q . When the rule is symmetric, this condition also holds with p and q interchanged and defines the undirected edge { p, q } . The resulting graph is known as an emptyregion graph, and the pair p, q that satisfy this criterion are called adjacent; see Cardinal et al. (2009). The choice of the regions S ( p, q ) determines several well-known proximity graphs, such as nearest-neighbor graphs, the Gabriel graph (Gabriel and Sokal, 1969), the relative-neighborhood graph (Toussaint, 1980), β -skeletons (Kirkpatrick and Radke, 1985), γ -neighborhood graphs (Veltkamp, 1992), and stepping-stone graphs (Kannangara, Tanin, Harwood and Karunasekera, 2018).

In the probabilistic sections, Φ denotes a homogeneous Poisson point process on R d with intensity measure ρλd , where ρ &gt; 0 . The symbols P and E denote probability and expectation. For z ∈ R d , let P z denote the Palm probability of Φ at z , and let E z denote the corresponding expectation. In particular, Palm probability and expectation at the origin are denoted by P 0 and E 0 , respectively.

In this paper, we restrict attention to Borel sets S ( p, q ) satisfying 0 &lt; λd ( S ( p, q )) &lt; ∞ .

The set N 0 ∶= {0 , 1 , 2 , ...} is used for orderk emptyregion rules. Boundary conventions are fixed in the deterministic graph definition: the empty region may be open, closed, or given by an interior. Here ∂S ( p, q ) denotes the boundary of the pair region S ( p, q ) . For Poisson point process whose intensity measure is absolutely continuous with respect to λd , these conventions give the same void probabilities whenever λd ( ∂S ( p, q )) = 0 . For deterministic point sets, the chosen boundary convention can change the edge set when data points lie on ∂S ( p, q ) .


<!-- p:3 -->


Figure 1: Normalization of a pairwise empty region. Starting from a candidate pair p, q , translate by - p , rotate the segment q - p onto the e 1 -axis, and scale by l -1 p,q . The resulting normalized region is the unit region K , while the original pair region is recovered as S ( p, q ) = p + l p,q Rp,qK .

### 3. Unit regions

$$R _ { p , q } e _ { 1 } \ = \ u _ { p , q } \quad & & P r o o d { 3 . 1 } & & P r o o d { 3 . 1 } \\ R _ { p , q } ( \Omega ) = \ u _ { p , q } & & ( 3 . 1 ) & & \text {meas}$$

Definition 3.1 (Unit region) . Assume that S is a measurable translation-covariant pairwise empty-region rule. Then S has a unit region if there is a Borel set K ⊂ R d with 0 &lt; λd ( K ) &lt; ∞ such that, for every p ≠ q ∈ R d , there exists Rp,q ∈ O ( d ) satisfying

$$\begin{array} { r l r l } { R _ { p , q } e _ { 1 } } & { - } & { u _ { p , q } } & { ( 3 . 1 ) } \\ { S ( p , q ) } & { = } & { p + \ell _ { p , q } R _ { p , q } K . } & { ( 3 . 2 ) } \\ { \quad } & { \quad } & { ( 3 . 2 ) } & { \quad } \\ { \quad } & { \quad } & { \quad } & { \quad } \end{array} \quad \begin{array} { r r r } { \ m a s h s c r { E } } & { ( 3 . 2 ) } & { \quad } \\ { ( 3 . 2 ) } & { \quad } & { \quad } \\ { ( 3 . 2 ) } & { \quad } & { \quad } \end{array}$$

Proposition 3.2 (Similarity equivariance gives a unit region) . Suppose that S is measurable and that, for every Euclidean similarity T ( x ) = τRx + a , with τ &gt; 0 , R ∈ O ( d ) , and a ∈ R d , one has

The same condition can be expressed as a unit-region construction with a fixed normalized region that is translated, rotated, and uniformly scaled according to the candidate pair (Cardinal et al., 2009). It is also implied by set-level similarity equivariance.

$$S \left ( T ( p ) , T ( q ) \right ) = T \left ( S ( p , q ) \right ) . \quad \ \ ( 3 . 3 ) \quad \ \ \ \ \ \ t i o n .$$

Then S has a unit region, namely K = S ( 0 , e 1 ) .

Proof. For p ≠ q , choose Rp,q ∈ O ( d ) with Rp,q e 1 = up,q . The similarity T ( x ) = p + l p,q Rp,qx maps [ 0 , e 1 ] to [ p, q ] . Hence

$$S ( p , q ) & = S \left ( T ( 0 ) , T ( e _ { 1 } ) \right ) \\ & = T \left ( S ( 0 , e _ { 1 } ) \right ) = p + \ell _ { p , q } R _ { p , q } K . \\$$

Thus, similarity equivariance yields the required unit-region representation.

For d ≥ 3 , many orthogonal maps send e 1 to up,q . The volume identity is independent of this choice, since every orthogonal map preserves λd . The graph-level definition also needs a definite orientation convention when K lacks axial symmetry around the e 1 -axis. This can be supplied by a measurable choice ( p, q ) ↦ Rp,q , or by imposing invariance of K under all rotations fixing e 1 . The regions associated with the Gabriel graph, the relative-neighborhood graph, β -skeletons, and stepping-stone graphs satisfy this axialsymmetry condition.

Theorem 3.3 (Unit-region factorization) . If S has a unit region K , then for p ≠ q ∈ R d

$$\lambda _ { d } ( S ( p , q ) ) = a _ { K } \ell _ { p , q } ^ { d } .$$

Proof. Translation and orthogonal maps preserve Lebesgue measure. Scaling by l p,q multiplies d -dimensional volume by l d p,q . Applying this to (3.2) gives

$$\lambda _ { d } ( S ( p , q ) ) = \lambda _ { d } \left ( p + \ell _ { p , q } R _ { p , q } K \right ) = \ell _ { p , q } ^ { d } \lambda _ { d } ( K ) .$$

Therefore, the volume of the pair region factors into the unitregion constant and the distance scale.

### 4. Poisson void probabilities and Palm consequences

A pairwise empty-region rule is a geometric construction. Given a locally finite configuration η ⊂ R d , two distinct points p, q ∈ η are adjacent when the region S ( p, q ) associated with the pair contains no point of η other than the endpoints. Thus, the empty-region condition is

$$\eta ( S ( p , q ) \ \{ p , q \} ) = 0 ,$$

where η ( A ) denotes the number of points of η contained in a Borel set A ⊆ R d .

In this section, the vertex configuration is a homogeneous Poisson point process. The deterministic emptyregion condition then becomes a Poisson void event. The unit-region factorization established in Section 3 implies that the volume of the region associated with a pair depends only on its length and on the region constant:


<!-- p:4 -->


$$\lambda _ { d } ( S ( p , q ) \ \{ p , q \} ) & = \lambda _ { d } ( S ( p , q ) ) \\ & = a _ { K } \ell _ { p , q } ^ { d } , \quad p \neq q .$$

Hence, for the homogeneous Poisson model, the geometric effect of the rule enters the fixed-pair calculation through the single scalar aK .

Let Φ be a homogeneous Poisson point process on R d with intensity measure ρλd , where ρ &gt; 0 . For every Borel set A ⊂ R d with λd ( A ) &lt; ∞ ,

$$\Phi ( A ) \sim \text {Poisson} ( \rho \lambda _ { d } ( A ) ) , & & \text {Cor} \Phi ( A ) = \begin{matrix} 0 & \text {Cor} \Phi ( A ) \\ 4 . 3 \end{matrix} \\$$

and the counts on disjoint Borel sets are independent. In particular,

$$\mathbb { P } \left \{ \Phi ( A ) = 0 \right \} = \exp \left \{ - \rho \lambda _ { d } ( A ) \right \} . \quad \left ( 4 . 4 \right ) ^ { 0 } \, \mathbb { E } ^ { 0 }$$

Equation (4.4) is the Poisson void probability; see (Last and Penrose, 2017; Baccelli and Błaszczyszyn, 2010).

Corollary 4.1 (Fixed-pair Poisson void law) . For every deterministic pair p ≠ q ,

$$\mathbb { P } \left \{ \Phi ( S ( p , q ) \ \{ p , q \} ) = 0 \right \} = \exp \left \{ - \rho a _ { K } \ell _ { p , q } ^ { d } \right \} . \ ( 4 . 5 )$$

Equivalently, (4.5) is the probability that the prescribed pair p, q is adjacent after the two points are inserted into an independent Poisson configuration.

Corollary 4.1 concerns a prescribed candidate pair. We now pass to the local neighborhood of a typical point of the process. Let P 0 denote the Palm distribution of Φ 0 at the origin, and let Φ ! 0 be the associated reduced Palm process. Under P 0 , the configuration may be viewed as a distinguished point at 0 together with the remaining process Φ ! 0 ; hence the candidate neighbors are the points of Φ ! 0 . By the Mecke-Slivnyak theorem,

$$\Phi _ { 0 } ^ { ! } \stackrel { d } { = } \Phi , & & \text {residue} \\$$

where the process on the right is again a homogeneous Poisson process with intensity measure ρλd ; see (Baccelli and Błaszczyszyn, 2010; Last and Penrose, 2017).

Corollary 4.2 (Typical points Poisson void law) . For every two typical points ( p, q ) with p ≠ q ,

$$\mathbb { P } ^ { p , q } \left \{ \Phi _ { p , q } ^ { ! } ( S ( p , q ) ) = 0 \right \} = \exp \left \{ - \rho a _ { K } \ell _ { p , q } ^ { d } \right \} . \ \ ( 4 . 7 ) \quad \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \$$

Proof. The two-point Palm identity follows from Slivnyak's theorem, since Φ ! p,q has the same distribution as Φ . Apply the Poisson void formula (4.4) to S ( p, q ) , then use λd ( S ( p, q )) = aK l d p,q .

For a candidate point x ∈ η , define

$$\chi _ { K } ( x ; \eta ) \colon = 1 \{ \eta ( S ( 0 , x ) \ \{ 0 , x \} ) = 0 \} \, . \quad ( 4 . 8 ) \quad P a l m$$

Thus χK ( x ; η ) = 1 precisely when no point of η other than the endpoints 0 and x lies in the pair region S ( 0 , x ) . In particular, under the reduced Palm distribution,

$$\chi _ { K } ( x ; \Phi _ { 0 } ^ { ! } ) = 1$$

if and only if the directed edge that goes from the Palm point to x is present. If the rule is symmetric, namely

$$S ( p , q ) = S ( q , p ) , \quad p \neq q ,$$

then this is equivalent to the undirected edge { 0 , x } being incident to the Palm point.

Corollary 4.3 (Palm-Mecke identity for incident edges) . For every nonnegative measurable function g ∶ R d → [0 , ∞) ,

$$\mathbb { E } ^ { 0 } \left [ \sum _ { x \in \Phi _ { 0 } ^ { \prime } } g ( x ) \chi _ { K } ( x ; \Phi _ { 0 } ^ { \prime } ) \right ] & = \rho \int _ { \mathbb { R } ^ { d } } g ( x ) \\ & \quad \times \exp \left \{ - \rho a _ { K } \ell _ { 0 , x } ^ { d } \right \} \, d x .$$

Proof. By (4.6), the reduced Palm process Φ ! 0 has the same distribution as a homogeneous Poisson process of intensity ρλd . Applying the Mecke formula to Φ ! 0 therefore yields

$$\mathbb { I } _ { n } ^ { r } & = \mathbb { E } ^ { 0 } \left [ \sum _ { x \in \Phi _ { 0 } ^ { \prime } } g ( x ) \chi _ { K } ( x ; \Phi _ { 0 } ^ { \prime } ) \right ] = \rho \int _ { \mathbb { R } ^ { d } } g ( x ) \\ & \quad \times \mathbb { P } \left \{ \Phi ( S ( 0 , x ) ) = 0 \right \} \, d x .$$

By Corollary 4.1,

$$\mathbb { P } \left \{ \Phi ( S ( 0 , x ) ) = 0 \right \} = \exp \left \{ - \rho a _ { K } \ell _ { 0 , x } ^ { d } \right \} .$$

$$\text {Substitution gives (4.11).}$$

The deterministic integration variable x in (4.11) represents the displacement of a candidate neighbor from the Palm point. Although the exclusion region S ( 0 , x ) may depend on the direction of x through the rotated region K , unit-region factorization depends on the candidate displacement only through l 0 ,x and on the region only through its volume constant aK = λd ( K ) . Thus, at this first-order voidprobability level, the detailed shape of K does not enter beyond its volume.

Definition 4.4 (Palm incident-edge length measure) . Define a measure νK on [0 , ∞) by

$$\nu _ { K } ( C ) \colon = \mathbb { E } ^ { 0 } \left [ \sum _ { x \in \Phi _ { 0 } ^ { \prime } } \chi _ { K } ( x ; \Phi _ { 0 } ^ { ! } ) 1 \left \{ \ell _ { 0 , x } \in C \right \} \right ] , \ ( 4 . 1 4 )$$

for every Borel set C ⊂ [0 , ∞) .

Thus νK ( C ) is the expected number of edges from the Palm point whose Euclidean lengths belong to C . In general,


<!-- p:5 -->


νK is a finite first-moment measure. In the nonsymmetric setting, this measure concerns edges directed outward from the Palm point. Under symmetry, these are the usual undirected edges incident to that point.

Corollary 4.5 (Incident-edge length law) . The Palm incident-edge length measure νK is absolutely continuous with respect to Lebesgue measure and satisfies

$$\nu _ { K } ( d r ) = \rho d \kappa _ { d } r ^ { d - 1 } \exp \left \{ - \rho a _ { K } r ^ { d } \right \} \, d r , \quad r \geq 0 . \ ( 4 . 1 5 )$$

Equivalently, for every r ≥ 0 ,

$$\nu _ { K } ( [ 0 , r ] ) = \frac { \kappa _ { d } } { a _ { K } } \left ( 1 - \exp \left \{ - \rho a _ { K } r ^ { d } \right \} \right ) . \quad ( 4 . 1 6 ) \quad \begin{matrix} \text {is trace} \\ \text {adjac} \\ \text {of 0} \end{matrix} .$$

Proof. Let h ∶ [0 , ∞) → [0 , ∞) be measurable. By Definition 4.4 and Corollary 4.3, applied with g ( x ) = h ( l 0 ,x ) ,

$$\int _ { [ 0 , \infty ) } h ( r ) \, \nu _ { K } ( d r ) & = \rho \int _ { \mathbb { R } ^ { d } } h ( \ell _ { 0 , x } ) \\ & \times \exp \left \{ - \rho a _ { K } \ell _ { 0 , x } ^ { d } \right \} \, d x .$$

The integrand is radial because it is a function only of l 0 ,x = ‖ x ‖ ; equivalently, it is invariant under every orthogonal transformation Q ∈ O ( d ) , since ‖ Qx ‖ = ‖ x ‖ . Hence polar coordinates in R d , with dκd equal to the surface area of the unit sphere in R d , yield

$$\int _ { [ 0 , \infty ) } h ( r ) \, \nu _ { K } ( d r ) & = \rho d \kappa _ { d } \int _ { 0 } ^ { \infty } h ( r ) r ^ { d - 1 } \\ & \times \exp \left \{ - \rho a _ { K } r ^ { d } \right \} \, d r .$$

Since this holds for every nonnegative measurable h , (4.15) follows.

Finally, integrating (4.15) over [0 , r ] , with the substitution u = ρaKs d , gives

$$\nu _ { K } ( [ 0 , r ] ) = \frac { \kappa _ { d } } { a _ { K } } \int _ { 0 } ^ { \rho a _ { K } r ^ { d } } e ^ { - u } \, d u , \quad \\$$

$$\text {which is (4.16)} .$$

For a locally finite configuration η and p ∈ η , define

$$\deg _ { \text {out} } ( p ; \eta ) \colon = \sum _ { q \in \eta \ \{ p \} } 1 \left \{ \eta ( S ( p , q ) \ \{ p , q \} ) = 0 \right \} .$$

Corollary 4.6 (Meanout-degree of a typical Poisson vertex) . For every z ∈ R d ,

$$\mathbb { E } ^ { z } \left [ \deg _ { \text {out} } ( z ) \right ] = \frac { \kappa _ { d } } { a _ { K } } .$$

Proof. By Definition 4.4,

$$\nu _ { K } ( [ 0 , \infty ) ) & = \mathbb { E } ^ { 0 } \left [ \sum _ { x \in \Phi _ { 0 } ^ { \prime } } \chi _ { K } ( x ; \Phi _ { 0 } ^ { \prime } ) \right ] & \quad \text {as class} \\ & = \mathbb { E } ^ { 0 } \left [ \deg _ { \text {out} } ( 0 ) \right ] .$$

Letting r → ∞ in (4.16) yields

$$\nu _ { K } ( [ 0 , \infty ) ) = \frac { \kappa _ { d } } { a _ { K } } .$$

Hence

$$\mathbb { E } ^ { 0 } \left [ \deg _ { \text {out} } \left ( 0 ; \Phi _ { 0 } \right ) \right ] = \frac { \kappa _ { d } } { a _ { K } } .$$

Now let z ∈ R d . Under P z , translating the Palm configuration by - z yields a configuration with the same law as the Palm configuration at the origin. Since the rule is translation covariant, this translation preserves directed adjacency and maps the out-degree of z to the out-degree of 0 . Therefore,

$$\mathbb { E } ^ { z } \left [ \deg _ { \text {out} } ( z ; \Phi ) \right ] = \mathbb { E } ^ { 0 } \left [ \deg _ { \text {out} } \left ( 0 ; \Phi _ { 0 } \right ) \right ] = \frac { \kappa _ { d } } { a _ { K } } . \ ( 4 . 2 5 )$$

Hence, the mean out-degree depends only on the volume of the unit region.

Corollary 4.7 (Undirected-edge intensity per Poisson vertex) . Assume that the unit-region rule is symmetric, namely, S ( p, q ) = S ( q, p ) , for p ≠ q. Then the directed relation defines an undirected graph, and deg( p ) = degout ( p ) . Let ρE,K denote the spatial intensity of undirected edges of the stationary graph. Then

$$\frac { \rho _ { E , K } } { \rho } = \frac { \kappa _ { d } } { 2 a _ { K } } .$$

Equivalently, the undirected-edge intensity normalized by the vertex intensity is κd ∕(2 aK ) ; it is one half of the mean degree of a typical vertex.

Proof. Under symmetry, the out-degree equals the ordinary undirected degree.

$$\mathbb { E } ^ { 0 } \left [ \deg ( 0 ; \Phi _ { 0 } ) \right ] = \mathbb { E } ^ { 0 } \left [ \deg _ { \text {out} } \left ( 0 ; \Phi _ { 0 } \right ) \right ] = \frac { \kappa _ { d } } { a _ { K } } , \, ( 4 . 2 7 )$$

Each undirected edge has exactly two endpoint incidences. Therefore, the spatial intensity of endpoint incidences is twice the spatial intensity of undirected edges:

by Corollary 4.6.

$$2 \rho _ { E , K } = \rho \mathbb { E } ^ { 0 } \left [ \deg \left ( 0 ; \Phi _ { 0 } \right ) \right ] .$$

Hence

$$2 \rho _ { E , K } = \rho \frac { \kappa _ { d } } { a _ { K } } .$$

Dividing by 2 ρ yields

$$\frac { \rho _ { E , K } } { \rho } = \frac { \kappa _ { d } } { 2 a _ { K } } ,$$

$$a s \, \text {claimed.}$$


<!-- p:6 -->


Definition 4.8 (Palm incident-edge length distribution) . The Palm incident-edge length distribution is the probability measure μK on [0 , ∞) defined, for every Borel set C ⊆ [0 , ∞) , by

$$\mu _ { K } ( C ) \colon = \frac { \nu _ { K } ( C ) } { \nu _ { K } ( [ 0 , \infty ) ) } = \frac { a _ { K } } { \kappa _ { d } } \nu _ { K } ( C ) . \quad & ( 4 . 3 1 ) \\ T u _ { K } ( 0 , \infty ) \, \nu _ { K } \colon & 1 , 1 , 1 , \cdots , \vdots ; 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , 1 , $$

Theorem 4.9 (Weibull law for incident-edge lengths) . Let LK be a random variable with distribution μK . Then, for every l ≥ 0 ,

$$\mathbb { P } ( L _ { K } \leq \ell ) = 1 - \exp \left \{ - \rho a _ { K } \ell ^ { d } \right \} . \quad \text { \quad \ and } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \ } \quad \text { \quad \ \$$

Consequently, LK has density

$$g _ { K } ( \ell ) = \rho d a _ { K } \ell ^ { d - 1 } \exp \left \{ - \rho a _ { K } \ell ^ { d } \right \} , \quad \ell \geq 0 . \ ( 4 . 3 3 ) \\$$

Hence,

$$L _ { K } \sim \text {Weilull} \left ( d , ( \rho a _ { K } ) ^ { - 1 / d } \right ) , & & \text {ter} \left ( \rho a _ { 3 } \right ) ^ { - 1 / 3 } & & \text {rule} .$$

under the shape-scale parameterization

$$\mathbb { P } ( W \leq w ) & = 1 - \exp \left \{ - \left ( \frac { w } { \sigma } \right ) ^ { \alpha } \right \} , \quad w \geq 0 , \ ( 4 . 3 5 ) \\$$

Proof. Let l ≥ 0 . By Definition 4.8,

for W ∼ Weibull( α, σ ) .

$$\mathbb { P } ( L _ { K } \leq \ell ) = \mu _ { K } ( [ 0 , \ell ] ) \\$$

By Corollary 4.5,

$$K & = \bar { \ } v \, _ { K } ( [ 0 , \ell ] ) \\ & = \frac { \nu _ { K } ( [ 0 , \ell ] ) } { \nu _ { K } ( [ 0 , \infty ) ) } .$$

$$\nu _ { K } ( [ 0 , \ell ] ) = \frac { \kappa _ { d } } { a _ { K } } \left [ 1 - \exp \left \{ - \rho a _ { K } \ell ^ { d } \right \} \right ] , \quad ( 4 . 3 8 ) \\ \intertext { v i n g t h s c r . } \nu _ { K } ( [ 0 , \ell ] ) = \frac { \kappa _ { d } } { a _ { K } } \left [ 1 - \exp \left \{ - \rho a _ { K } \ell ^ { d } \right \} \right ] , \quad ( 4 . 3 8 ) \\ \intertext { v e c h s c r . } \intertext { v i n g t h s c r . } \intertext { v e c h s c r . } \intertext { v i n g t h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r . } \intertext { v e c h s c r$$

while Corollary 4.6 gives

$$\nu _ { K } ( [ 0 , \infty ) ) = \frac { \kappa _ { d } } { a _ { K } } . & & ( 4 . 3 9 ) \\ & & \quad a b i n b { 1 }$$

$$\mathbb { P } ( L _ { K } \leq \ell ) = 1 - \exp \left \{ - \rho a _ { K } \ell ^ { d } \right \} , \quad \ \ ( 4 . 4 0 ) \quad \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \$$

Therefore,

which proves (4.32).

$$g _ { K } ( \ell ) = \rho d a _ { K } \ell ^ { d - 1 } \exp \left \{ - \rho a _ { K } \ell ^ { d } \right \} ,$$

Differentiating (4.32) on (0 , ∞) gives

proving (4.33). Since

$$\rho a _ { K } \ell ^ { d } = \left ( \frac { \ell } { ( \rho a _ { K } ) ^ { - 1 / d } } \right ) ^ { d } , \\ \intertext { t h e d i s h i t i s } \rho a _ { K } \ell ^ { d } = \left ( \frac { \ell } { ( \rho a _ { K } ) ^ { - 1 / d } } \right ) ^ { d } , \\$$

Finally, the Palm measure νK ( C ) counts edge incidences at a typical Poisson vertex whose lengths lie in C by stationarity of the homogeneous Poisson process and translation covariance of the rule. If the rule is symmetric, every edge will have two endpoint incidences with the same length. Hence the factor 2 cancels after normalization. Therefore the normalized Palm incident-edge law μK coincides with the length law of a typical undirected edge.

the distribution function in (4.32) is the shape-scale Weibull distribution with shape parameter d and scale parameter ( ρaK ) -1 ∕ d .

Corollary 4.10 (Scaling and exponential transform) . Let LK be the Palm incident-edge length of Theorem 4.9. Then

$$Z _ { K } \colon = ( \rho a _ { K } ) ^ { 1 / d } L _ { K } \sim \text {Webull} ( d , 1 ) .$$

Equivalently,

$$U _ { K } \colon = \rho a _ { K } L _ { K } ^ { d } = Z _ { K } ^ { d } \sim \exp ( 1 ) .$$

Proof. By Theorem 4.9, multiplication by the reciprocal scale parameter gives (4.43). Raising a unit-scale Weibull random variable with shape parameter d to the power d gives a standard exponential random variable, which proves (4.44).

Interpretation of the Weibull parameters. The Palm incident-edge length is Weibull distributed. Its scale parameter ( ρaK ) -1∕ d is the natural length scale of the empty-region rule. Indeed, for a candidate neighbor at distance l , the expression

$$\rho \lambda _ { d } \left ( S ( 0 , x ) \right ) = \rho a _ { K } \ell ^ { d }$$

represents the mean number of other Poisson points inside its exclusion region. At l = ( ρaK ) -1 ∕ d , this mean equals 1 . Equivalently, the corresponding void probability is e -1 , yielding

$$\mathbb { P } ( L _ { K } \leq ( \rho a _ { K } ) ^ { - 1 / d } ) = 1 - e ^ { - 1 } .$$

Thus, the scale parameter ( ρaK ) -1 ∕ d operates as a characteristic edge-length scale, although it does not coincide generally with the mean or the median of LK . Increasing either the intensity ρ or the geometric region factor aK monotonically decreases this scale.

The shape parameter is explicitly governed by the ambient dimension d . The exclusion-region volume scales as aK l d , which induces the void probability factor exp(- ρaK l d ) , while the differential change of variables in polar coordinates contributes the shell Lebesgue measure factor l d -1 . Integrated dually, they yield the probability density function

$$g _ { K } ( \ell ) = d \rho a _ { K } \ell ^ { d - 1 } \exp \left ( - \rho a _ { K } \ell ^ { d } \right ) ,$$

and hence the Weibull shape parameter d . In particular,

$$( \rho a _ { K } ) ^ { 1 / d } L _ { K } \sim \text {Weull} ( d , 1 ) ,$$

implying that, within a fixed dimension d , the law of the standardized Palm incident-edge length ( ρaK ) 1∕ d LK is invariant across admissible rules.

The Weibull identification determines every quantity that depends only on the one-dimensional distribution of a single edge length LK . In particular, its distribution and survival functions, density, hazard and cumulative hazard functions, quantiles, and moments are all available in closed form. Thus, the moment, quantile, coefficient-of-variation, and related formulas in Table 3 are exact first-order characteristics of the edge-length distribution. Here, 'first-order'


<!-- p:7 -->


refers to the point-process level of the result: each quantity concerns one selected edge length LK . This includes the second raw moment and the variance, despite their involving powers of LK . Such quantities require no joint distribution for two distinct edges, two distinct vertices, or several edge lengths from a common realization.

Table 2 summarizes the exact Poisson-Palm quantities determined by the common unit-volume constant aK .

By contrast, the edge lengths observed in one realization of the graph are not, in general, an i.i.d. sample from μK . The number of observed edges is random, and distinct edge events are typically dependent. Nearby candidate edges may share vertices or have overlapping exclusion regions, so their acceptance is partly determined by the same Poisson points. Consequently, the occurrence and length of one retained edge can be statistically dependent on those of another. Thus, even conditional on the number of observed edges, an enumeration L 1 , ... , Lm of their lengths is not generally an i.i.d. sample from μK . Its joint law is not determined by the one-dimensional Palm law μK , or by the scalar aK , alone.

The planar relative-neighborhood graph (RNG) provides an earlier instance of this functional form. Watanabe (2008) obtained the edge-length density of an RNG from a homogeneous Poisson process in the plane.

$$2 \rho a _ { 2 , R N G } \ell \exp \{ - \rho a _ { 2 , R N G } \ell ^ { 2 } \} , \quad \ell \geq 0 , \quad ( 4 . 4 9 )$$

through a geometric-probability calculation based on the RNGregion. Equation (4.49) is the present normalized Palm incident-edge density for the relative-neighborhood graph in dimension d = 2 . The calculation was not formulated as a normalized Palm first-moment law, nor was its Weibull form or its extension to general finite similarity regions made explicit.

### 5. Special cases

All numerical figures in this section use the same threepanel format: the left panel shows the normalized unit region, the center panel compares the empirical mean degree with its theoretical value, and the right panel compares rescaled edge-length distributions with the limiting Weibull law. We begin with the hyperspherical-cap volume formula, which provides the geometric ingredient for ball-generated regions, and then apply the same unit-region framework to the remaining graph families.

#### 5.1. Ball-generated regions

The volume calculations in this subsection are based on the following hyperspherical-cap formula.

Lemma 5.1 (Hyperspherical-cap volume) . Let r &gt; 0 and 0 ≤ h ≤ 2r . The volume of a d -dimensional spherical cap of radius r and height h is

$$\intertext { t h i n t y } \theta ( f ) \frac { d \alpha } { r } I _ { \text {cap} } = \begin{cases} \frac { \kappa _ { d } r ^ { d } } { 2 } & 0 \leq h \leq r , \\ V _ { \text {cap} } ^ { ( d ) } ( r , h ) = \begin{cases} \frac { \kappa _ { d } r ^ { d } } { 2 } & 0 \leq h \leq r , \\ \kappa _ { d } r ^ { d } - \frac { \kappa _ { d } r ^ { d } } { 2 } & r \leq h \leq 2 r , \\ \times I _ { 1 - ( 1 - h / r ) ^ { 2 } } \left ( \frac { d + 1 } { 2 } , \frac { 1 } { 2 } \right ) , & r \leq h \leq r , \\ \end{cases} \\ \intertext { t h i n t y } \mu _ { K } . \quad & \times I _ { 1 - ( 1 - h / r ) ^ { 2 } } \left ( \frac { d ^ { 2 } + 1 } { 2 } , \frac { 1 } { 2 } \right ) , & \quad \\ \text {their} & \quad \\ \text {points.} & \quad \text {where } I _ { \text {ax} } ( a , b ) \text { is the regularized incomplete beta function.}$$

where Ix ( a, b ) is the regularized incomplete beta function.

Proof. This is the hyperspherical-cap formula of Li (2011).

Proposition 5.2 (Volume of a two-ball region) . Let

$$K = B ( c _ { 0 } , r _ { 0 } ) \cap B ( c _ { 1 } , r _ { 1 } ) , \quad \delta \colon = \left \| c _ { 1 } - c _ { 0 } \right \| , \ ( 5 . 2 )$$

where r 0 , r 1 &gt; 0 . If δ ≥ r 0 +r1 , then

$$\lambda _ { d } ( K ) = 0 .$$

If δ ≤ | r 0 -r1 | , then

$$\lambda _ { d } ( K ) = \kappa _ { d } \min \{ r _ { 0 } , r _ { 1 } \} ^ { d } .$$

In the transverse-overlap case | r 0 -r1 | &lt; δ &lt; r 0 +r1 , define

$$x _ { 0 } \colon = \frac { \delta ^ { 2 } + r _ { 0 } ^ { 2 } - r _ { 1 } ^ { 2 } } { 2 \delta } , \quad x _ { 1 } \colon = \delta - x _ { 0 } ,$$

and

Then

$$\lambda _ { d } ( K ) = V _ { c a p } ^ { ( d ) } ( r _ { 0 } , h _ { 0 } ) + V _ { c a p } ^ { ( d ) } ( r _ { 1 } , h _ { 1 } ) .$$

Proof. The first two cases correspond, respectively, to disjoint balls and to containment of the smaller ball in the larger one. In the transverse-overlap case, the common boundary of the two balls lies in a hyperplane perpendicular to c 1 - c 0 . The intersection is therefore the union, up to a Lebesgue-null boundary, of two caps with heights h 0 and h 1 . Equation (5.7) follows from Lemma 5.1.

Corollary 5.3 (Gabriel region) . For

$$K _ { G G } = B \left ( \frac { e _ { 1 } } { 2 } , \frac { 1 } { 2 } \right ) ,$$

the unit region volume is

$$a _ { d , G G } = 2 ^ { - d } \kappa _ { d } .$$

Proof. The region is a ball of radius 1∕2 .

$$h _ { 0 } \colon = r _ { 0 } - x _ { 0 } , \quad h _ { 1 } \colon = r _ { 1 } - x _ { 1 } .$$


<!-- p:8 -->

u1D462

u1D45B

Figure 2: Numerical results for the planar Gabriel graph: unit region, empirical mean degree, and rescaled edge-length distributions.

u1D462

u1D45B

Figure 3: Numerical results for the planar relativeneighborhood graph: unit region, empirical mean degree, and rescaled edge-length distributions.

Corollary 5.4 (Relative-neighborhood region) . For

$$K _ { R N G } = B ( 0 , 1 ) \cap B ( e _ { 1 } , 1 ) , \quad \quad ( 5 . 1 0 ) \quad \begin{smallmatrix} P r o o \\ \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \, \,$$

the unit region volume is

$$a _ { d , R N G } = \kappa _ { d } I _ { 3 / 4 } \left ( \frac { d + 1 } { 2 } , \frac { 1 } { 2 } \right ) . \quad \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \$$

Proof. Apply Proposition 5.2 with r 0 = r 1 = 1 and δ = 1 . The two caps have common height 1∕2 .

Corollary 5.5 (Lune-based β -skeleton region) . For β ≥ 1 , let

$$K _ { d , \beta } = B \left ( \left ( 1 - \frac { \beta } { 2 } \right ) e _ { 1 } , \frac { \beta } { 2 } \right ) \cap B \left ( \frac { \beta } { 2 } e _ { 1 } , \frac { \beta } { 2 } \right ) . \ \ ( 5 . 1 2 ) \quad \text {reg} \quad \underset { \text {rescale} } { \text {region} }$$

Then

$$a _ { d , \beta } = \kappa _ { d } \left ( \frac { \beta } { 2 } \right ) ^ { d } I _ { \frac { 2 \beta - 1 } { \beta ^ { 2 } } } \left ( \frac { d + 1 } { 2 } , \frac { 1 } { 2 } \right ) .$$

Proof. The two balls have common radius β ∕2 , center separation β - 1 , and cap height 1∕2 . Proposition 5.2 therefore gives the stated formula.

u1D462

u1D45B

Figure 4: Numerical results for the planar lune-based β -skeleton with β = 3∕2 : unit region, empirical mean degree, and rescaled edge-length distributions.

#### 5.2. Stepping-stone diversion regions

For α ≥ 1 , define the stepping-stone region

$$S _ { S S , \alpha } ( p , q ) & = \left \{ z \in \mathbb { R } ^ { d } \ \colon \| z - p \| ^ { \alpha } \\ & \quad + \| z - q \| ^ { \alpha } \leq \ell _ { p , q } ^ { \alpha } \right \} .$$

It has unit representative

$$K _ { S S , \alpha } = \{ z \in \mathbb { R } ^ { d } \ \colon \| z \| ^ { \alpha } + \left \| z - e _ { 1 } \right \| ^ { \alpha } \leq 1 \} \ .$$

For α = 1 , the triangle inequality forces the region to be the segment [ p, q ] , which has zero d -dimensional volume. Thus α = 1 lies outside the positive-volume unit-region class of Definition 3.1. For α &gt; 1 , set

Then

$$y _ { \alpha } ( u ) & = \frac { 1 } { 2 } \left [ 4 u ^ { 2 } - \left ( 1 + u ^ { 2 } - ( 1 - u ^ { \alpha } ) ^ { 2 / \alpha } \right ) ^ { 2 } \right ] ^ { 1 / 2 } , \\ x _ { \alpha } ^ { \prime } ( u ) & = u + u ^ { \alpha - 1 } \left ( 1 - u ^ { \alpha } \right ) ^ { 2 - \alpha / \alpha } .$$

$$a _ { d , S S } ( \alpha ) = 2 \kappa _ { d - 1 } \int _ { 2 ^ { - 1 / \alpha } } ^ { 1 } y _ { \alpha } ( u ) ^ { d - 1 } x _ { \alpha } ^ { \prime } ( u ) \, d u .$$

Proof. Normalize the pair ( p, q ) to ( 0 , e 1 ) , parametrize one symmetric half of its boundary by u , whose longitudinal coordinate has derivative x ′ α ( u ) , and whose orthogonal ( d - 1) -dimensional section is a ball of radius yα ( u ) ; integrating the section volume κd -1 yα ( u ) d -1 with respect to x ′ α ( u ) du , and doubling by symmetry, yields (5.17).

Figure 5: Numerical results for the planar stepping-stone region with α = 3 : unit region, empirical mean degree, and rescaled edge-length distributions.

#### 5.3. Planar one-region Veltkamp subfamilies

Lemma 5.1 applies directly to two planar one-region subfamilies of Veltkamp's γ -neighborhood construction. Write

$$m \colon = \frac { 1 } { 2 } e _ { 1 } , \quad e _ { 2 } \colon = ( 0 , 1 ) ,$$

and, for

$$\gamma _ { 0 } , \gamma _ { 1 } \in ( - 1 , 1 ) , \quad | \gamma _ { 0 } | \leq | \gamma _ { 1 } | ,$$

$$R _ { \gamma } \colon = \frac { 1 } { 2 ( 1 - | \gamma | ) } , \quad h _ { \gamma } \colon = \frac { \sqrt { | \gamma | ( 2 - | \gamma | ) } } { 2 ( 1 - | \gamma | ) } .$$

define

For the nonsymmetric planar regions considered below, we use the unique orientation-preserving rotation

$$R _ { p , q } \in S O ( 2 )$$


<!-- p:9 -->


satisfying

$$R _ { p , q } e _ { 1 } = u _ { p , q } .$$

This fixes the orientation of the normalized region relative to each ordered pair ( p, q ) .

The (0 , γ ) -subfamily. For γ 0 = 0 and γ 1 = γ , set

$$D _ { 0 } \colon = B \left ( m , \frac { 1 } { 2 } \right ) , \quad D _ { \gamma } \colon = B ( m + h _ { \gamma } e _ { 2 } , R _ { \gamma } ) . \ ( 5 . 2 3 )$$

The construction has one prescribed neighborhood, namely

$$K _ { 0 , \gamma } \colon = \begin{cases} D _ { 0 } \cap D _ { \gamma } , & \gamma < 0 , \\ D _ { 0 } , & \gamma = 0 , \\ D _ { 0 } \cup D _ { \gamma } , & \gamma > 0 . \end{cases}$$

Thus the (0 , γ ) -subfamily is of intersection type for γ &lt; 0 and of union type for γ &gt; 0 .

u1D462

u1D45B

Figure 6: Numerical results for the planar (0 , γ ) -subfamily with γ = 0 . 55 : unit region, empirical mean out-degree, and rescaled edge-length distributions.

Diagonal ( γ, γ ) -subfamily. When

$$\gamma _ { 0 } = \gamma _ { 1 } = \gamma ,$$

For γ ∈ (-1 , 1) ⧵ {0} , write

$$D _ { \gamma } ^ { \pm } \colon = B ( m \pm h _ { \gamma } e _ { 2 } , R _ { \gamma } ) \, .$$

The original diagonal Veltkamp construction is recovered by coupling the set operation to the sign of γ :

$$K _ { \gamma , \gamma } \colon = \begin{cases} D _ { \gamma } ^ { - } \cap D _ { \gamma } ^ { + } , & - 1 < \gamma < 0 , \\ B \left ( m , \frac { 1 } { 2 } \right ) , & \gamma = 0 , \\ D _ { \gamma } ^ { - } \cup D _ { \gamma } ^ { + } , & 0 < \gamma < 1 . \end{cases} \\$$

Corollary 5.6 (Diagonal Veltkamp subfamily and the circle-based β -skeleton) . For γ ∈ (-1 , 1) , the planar diagonal Veltkamp subfamily Kγ,γ coincides with the circle-based β - skeleton in Veltkamp's normalized parameterization, with

$$\beta _ { n o r m } = \gamma . \quad \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \$$

Equivalently, if β &gt; 0 denotes the standard nonnegative circle-based parameter, then

$$\beta = \begin{cases} 1 + \gamma , & - 1 < \gamma \leq 0 , \\ \frac { 1 } { 1 - \gamma } , & 0 \leq \gamma < 1 . \end{cases} ( 5 . 2 9 )$$

Proof. For γ &lt; 0 , the circle-based neighborhood is the intersection of two disks of radius

$$\frac { 1 } { 2 ( 1 + \gamma ) } = \frac { 1 } { 2 ( 1 - | \gamma | ) } = R _ { \gamma } .$$

For γ &gt; 0 , it is the union of two disks of radius

$$\frac { \beta } { 2 } = \frac { 1 } { 2 ( 1 - \gamma ) } = R _ { \gamma } .$$

At γ = 0 , both constructions reduce to the Gabriel disk.

Figure 7: Numerical results for the planar diagonal ( γ, γ ) - subfamily with γ = -0 . 3 : unit region, empirical mean degree, and rescaled edge-length distributions.

These two subfamilies are full prescribed empty-region graphs. For general parameter pairs ( γ 0 , γ 1 ) , Veltkamp's construction may involve two alternative neighborhoods and is not, in general, determined by the emptiness of one prescribed pair region.

γ -parameterized planar regions. Set

$$\epsilon _ { \gamma _ { 0 } , \gamma _ { 1 } } \colon = \begin{cases} - 1 , & \gamma _ { 0 } \gamma _ { 1 } > 0 , \\ 1 , & \gamma _ { 0 } \gamma _ { 1 } \leq 0 . \end{cases}$$

Define the two disks

$$D ( \theta _ { \gamma _ { 0 } , \gamma _ { 1 } } ^ { ( 0 ) } \colon = B \begin{pmatrix} m + h _ { \gamma _ { 0 } } e _ { 2 } , \\ R _ { \gamma _ { 0 } } \end{pmatrix} , \\ D _ { \gamma _ { 0 } , \gamma _ { 1 } } ^ { ( 1 ) } \colon = B \begin{pmatrix} m + \epsilon _ { \gamma _ { 0 } , \gamma _ { 1 } } h _ { \gamma _ { 1 } } e _ { 2 } , \\ R _ { \gamma _ { 1 } } \end{pmatrix} . \\$$

The γ -parameterized two-ball region is

$$K _ { \gamma _ { 0 } , \gamma _ { 1 } } = \begin{cases} D _ { \gamma _ { 0 } , \gamma _ { 1 } } ^ { ( 0 ) } \cap D _ { \gamma _ { 0 } , \gamma _ { 1 } } ^ { ( 1 ) } , & \gamma _ { 1 } < 0 , \\ B \left ( m , \frac { 1 } { 2 } \right ) , & \gamma _ { 0 } = \gamma _ { 1 } = 0 , \\ D _ { \gamma _ { 0 } , \gamma _ { 1 } } ^ { ( 0 ) } \cup D _ { \gamma _ { 0 } , \gamma _ { 1 } } ^ { ( 1 ) } , & \gamma _ { 1 } > 0 . \end{cases} \\$$

This parameterization is useful because it selects one prescribed pair region S ( p, q ) for each candidate pair, rather than requiring the two alternative neighborhoods that may arise in Veltkamp's general planar construction. Consequently, the selected rule belongs to the unit-region framework, so the factorization, Poisson void, mean outdegree, and incident-edge length identities derived above apply directly.


<!-- p:10 -->

u1D462

u1D45B

Figure 8: Numerical results for the planar γ -parameterized two-ball region with γ 0 = -0 . 15 and γ 1 = -0 . 35 : unit region, empirical mean out-degree, and rescaled edge-length distributions.

#### 5.4. Densities

For a fixed ambient dimension d and a fixed Poisson intensity ρ , the normalized Palm edge-length law depends on the particular unit region K only through its volume aK . Indeed,

$$g _ { K } ( \ell ) = \rho d a _ { K } \ell ^ { d - 1 } \exp \left \{ - \rho a _ { K } \ell ^ { d } \right \} , \quad \ell \geq 0 . \ ( 5 . 3 5 ) \quad \text {graph}$$

Thus, when d and ρ are held fixed, the Weibull shape parameter remains unchanged, whereas the unit-region volume aK is the only rule-specific quantity affecting the scale parameter ( ρaK ) -1∕ d . In particular, regions with larger volume produce shorter characteristic edge lengths.

4

u1D4C1

Figure 9: Theoretical planar edge-length densities for the normalized regions at unit intensity. Larger unit-region areas shift the densities toward shorter edge lengths; the curves correspond to the graph families described above.

### 6. Discussion

#### 6.1. Region volume as a geometric complexity parameter

A key feature of the present framework is that, for finite similarity-region empty-region rules, the volume of the unit region,

$$a _ { K } = \lambda _ { d } ( K ) , & & a _ { \ } n e { s . } \\ a _ { K } = \lambda _ { d } ( K ) , & & ( 6 . 1 ) \\ & & a _ { \ } n e { s . }$$

acts as a geometric complexity parameter. The factorization

$$\lambda _ { d } ( S ( p , q ) ) = a _ { K } \| p - q \| ^ { d }$$

shows that the effect of the exclusion rule on the volume of the region associated with a pair is completely captured by aK . Consequently, at the fixed-pair and first-moment levels, proximity rules with different shapes but the same unitregion volume have the same Poisson void probability as a function of pair length, the same mean out-degree of a typical point, and the same normalized incident-edge length law. For symmetric rules, the out-degree coincides with the ordinary degree.

This interpretation gives aK a direct geometric and probabilistic meaning. A larger value of aK corresponds to a more restrictive exclusion rule: the region that must be empty for a pair to form an edge is larger, so edges occur less frequently. Quantitatively, the mean out-degree of a typical point is κd ∕ aK . For symmetric rules, this is also the mean degree. The characteristic incident-edge length scale is ( ρaK ) -1 ∕ d . Thus the region volume simultaneously controls graph sparsity and the scale of the edges that remain.

#### 6.2. Explicit families and computable consequences

This separation is useful because the same stochastic formulas apply to every admissible region, whereas the geometric calculation of aK depends on the particular rule. Ballgenerated regions can be treated through hyperspherical-cap formulas, while the stepping-stone family leads naturally to a different integral representation. The framework therefore accommodates distinct geometric mechanisms without requiring a new probabilistic derivation for each graph family.

The formulas for lune-based β -skeleton regions, selected planar two-ball regions associated with Veltkamp's construction, and stepping-stone diversion regions demonstrate that the general factorization is not merely formal. For these families, explicit or one-dimensional integral expressions for the unit region volume make it possible to obtain concrete edge probabilities, mean out-degrees, and, for symmetric subfamilies, mean degrees, together with Weibull scales.

#### 6.3. Scope and limitations of the pairwise-region framework

Constructions beyond prescribed pairwise regions. The framework requires one prescribed finite region S ( p, q ) for each candidate pair. Delaunay adjacency is existential: two points are joined by an edge when some sphere with the two points on its boundary and center on their perpendicularbisector hyperplane is empty (Devroye, 1988); thus the test ranges over a family of balls rather than one prescribed region S ( p, q ) .

Voronoi cells are determined by comparisons with all sites, whereas the Euclidean minimum spanning tree is

Veltkamp's γ -neighborhood construction requires a separate qualification. In ambient dimension d ≥ 3 , its defining neighborhood is associated with d sites ( x 1 , ... , x d ) , and an empty neighborhood joins all ( d 2 ) pairs among those sites. It is therefore a higher-arity construction rather than a prescribed pairwise rule.


<!-- p:11 -->


selected by a global optimization criterion. These constructions are closely related to the present graphs, but do not fall within the prescribed finite pairwise-region framework without additional analysis (Devroye, 1988; Toussaint, 1980; Jaromczyk and Toussaint, 1992; Veltkamp, 1992; Penrose and Yukich, 2001).

Infinite-volume regions. Infinite strips and halfspaces may be similarity-covariant, but they satisfy

$$\lambda _ { d } ( K ) = \infty .$$

For example, in the lune-based β -skeleton family, the limiting region as β → ∞ is the infinite slab bounded by the hyperplanes through p and q perpendicular to q - p ; in the plane, this is the usual infinite strip (Cardinal et al., 2009). Consequently, the finite-volume Poisson void formulas and the constants derived here do not apply directly (Devroye, 1988; Veltkamp, 1992).

#### 6.4. Limits of the first-moment theory

The reduction to aK has a precise scope. It governs onepair void probabilities and Palm first-moment quantities, but it does not determine joint statistics of distinct edges. For example, degree variances, edge-length correlations, and factorial moment measures depend on the overlap geometry of two or more exclusion regions. These quantities involve volumes such as

$$\lambda _ { d } \left ( S ( 0 , x ) \cup S ( 0 , y ) \right ) ,$$

which cannot generally be recovered from the single scalar aK .

The framework is also restricted to prescribed finite pairwise regions. Delaunay adjacency, Voronoi constructions, Euclidean minimum spanning trees, infinite-volume regions, and cone constructions based on an external orientation convention fall outside this setting for different structural reasons. These exclusions are not defects of the factorization theorem; rather, they identify which geometric mechanisms must be incorporated by a more general theory.

#### 6.5. Directions beyond Euclidean similarity regions

A natural extension is to normed or anisotropic settings. In Euclidean space, rotation covariance makes the volume constant independent of the direction of the pair. Let ‖ ⋅ ‖ L denote a norm on R d with unit ball L . In a general normed space or under anisotropic pairwise rules, the exclusionregion volume may instead take the form

$$\lambda _ { d } ( S ( p , q ) ) = a ( u ) \left \| p - q \right \| _ { L } ^ { d } , \quad \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \$$

where u denotes the direction of q - p . In that setting, conditional edge-length laws may remain Weibull in each direction, while the unconditional law becomes a directional mixture. Characterizing the rules for which a directionindependent Weibull law persists would extend the present universality result.

A second direction is higher-order Palm analysis. Explicit formulas for degree variance, joint incident-edge statistics, and stabilization properties would require a systematic treatment of exclusion-region overlaps.

Finally, the exact Weibull law suggests statistical questions. It would be natural to investigate how the effective scale ρaK can be estimated or tested from observed proximity graphs, and whether departures from the predicted law can be used to diagnose anisotropy, spatial inhomogeneity, or non-Poisson interaction.

### 7. Conclusion

Finite similarity-region empty-region rules admit a simple geometric reduction: their pairwise region volumes are determined by the unit region volume aK . This reduction yields exact Poisson void probabilities, first-moment directed-edge statistics, and a Weibull law for incident-edge lengths. For symmetric rules, these directed-edge results yield the corresponding undirected degree and typicaledge statements. Explicit constants for ball-generated and stepping-stone regions show that the theory applies to several classical and nonclassical proximity constructions. The remaining challenge is to move beyond one-pair and first-moment quantities toward overlap-sensitive, anisotropic, and higher-order theories.

##### Data availability

No external datasets were used or analyzed in this study. The numerical results were obtained from point-process simulations generated using the ProximityGraphs Python package (Maravillo, Villarreal and Espino-Montelongo, 2026).

##### Declaration of competing interest

The authors declare no competing interests.

####### Declaration of generative AI and AI-assisted technologies in the manuscript preparation process

During the preparation of this work, the authors used ChatGPT, an AI language model by OpenAI, to assist with drafting descriptions of figures and tables and with improving language, clarity, and structure. After using this tool, the authors reviewed and edited the content as needed and take full responsibility for the content of the published article. No generative AI tool was used to generate research data, conduct simulations, or replace the mathematical derivations and verification reported in the manuscript.

##### Funding

This research did not receive any specific grant from funding agencies in the public, commercial, or not-for-profit sectors.


<!-- p:12 -->


#### CRediT authorship contribution statement

- Heriberto Espino-Montelongo: Conceptualization, Methodology, Formal analysis, Investigation, Validation, Visualization, Writing - original draft. Héctor Maravillo: Conceptualization, Investigation, Supervision, Writing - review and editing.

##### A. Applied uses of fixed-region proximity graphs

The same empty-region regions also appear outside the Poisson setting. In these applications the point set is usually observed, constructed, or simulated, and the graph is used as a geometric summary of adjacency, obstruction, or movement. Table 1 records the role of the region in each setting; it is not an extension of the Poisson formulas above.

Table 1 Applied settings where fixed-region proximity graphs are used as geometric adjacency rules.

| Source                                            | Setting                                       | Role of the region                                                                                                                      |
|---------------------------------------------------|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| (Gabriel and Sokal, 1969; Matula and Sokal, 1980) | Geographic variation and clustering           | The Gabriel disk with diameter pq is used as a local adjacency criterion for geographic data analysis.                                  |
| (Toussaint, 1980; Jaromczyk and Toussaint, 1992)  | Computational morphology and spatial analysis | Gabriel, relative-neighborhood, and β -skeleton regions encode neighborhood and shape information in finite planar point sets.          |
| (Watanabe, 2008)                                  | Transportation-network models                 | Proximity graphs are compared as idealized road- network skeletons and evaluated through travel- efficiency criteria.                   |
| (Maravillo et al., 2023; Maravillo, 2024)         | Street-network and tiling models              | β -skeleton regions are used to recover cyclic tiling graphs motivated by empirical street-network structures.                          |
| (Kannangara et al., 2018)                         | Public movement analysis                      | The stepping-stone region gives a parameterized diversion corridor bounded between the Gabriel case and the relative-neighborhood case. |
| (Jurkiewicz, 2023)                                | Network topology generation                   | Gabriel graph regions are used to generate repro- ducible reference physical network topologies in structural design.                   |


<!-- p:14 -->


##### B. Consequences of the unit-volume constant ( a K )

Table 2 Poisson-Palm and Weibull consequences of the unit-volume constant ( a K ).

| Source    | Result                       | Exact consequence                                                                                     |
|-----------|------------------------------|-------------------------------------------------------------------------------------------------------|
| Cor. 4.1  | Fixed-pair void law          | P { Φ ( S ( p, q ) ⧵ { p, q } ) = 0 } = exp { - ρa K l d p,q }                                        |
| Cor. 4.2  | Typical points void law      | P p,q { Φ ! p,q ( S ( p, q ) ) = 0 } = exp { - ρa K l d p,q }                                         |
| Cor. 4.3  | Palm-Mecke identity          | E 0 ⎡ ⎢ ⎢ ⎣ ∑ x ∈Φ ! 0 g ( x ) χ K ( x ;Φ ! 0 ) ⎤ ⎥ ⎥ ⎦ = ρ ∫ R d g ( x ) exp { - ρa K l d 0 ,x } d x |
| Def. 4.4  | Incident-edge length measure | ν K ( C ) = E 0 ⎡ ⎢ ⎢ ⎣ ∑ x ∈Φ ! 0 χ K ( x ;Φ ! 0 ) 1 { l 0 ,x ∈ C } ⎤ ⎥ ⎥ ⎦                          |
| Cor. 4.5  | Incident-edge length density | ν K (d r ) = ρdκ d r d -1 exp { - ρa K r d } d r                                                      |
| Cor. 4.6  | Mean out-degree              | E z [ deg out ( z ) ] = κ d a K , z ∈ R d                                                             |
| Cor. 4.7  | Undirected edge intensity    | ρ E,K ρ = κ d 2 a K (for symmetric rules)                                                             |
| Def. 4.8  | Palm edge distribution       | μ K ( C ) = ν K ( C ) ν K ([0 , ∞)) , L K ∼ μ K                                                       |
| Thm. 4.9  | Weibull law                  | L K ∼ Weibull ( d, ( ρa K ) -1 ∕ d )                                                                  |
| Cor. 4.10 | Universal scaling            | Z K ∶= ( ρa K ) 1 ∕ d L K ∼ Weibull( d, 1)                                                            |
| Cor. 4.10 | Exponential transform        | U K ∶= ρa K L d K ∼ Exp(1)                                                                            |

Here aK = λd ( K ) , and χK ( x ; η ) is the indicator that the pair region S ( 0 , x ) contains no point of η other than its endpoints.


<!-- p:15 -->


##### C. First-order distributional characteristics of edge length

Table 3 Derived distributional characteristics of the length LK of a typical incident edge

| Quantity                     | Formula                                                              |
|------------------------------|----------------------------------------------------------------------|
| Length distribution          | L K ∼ Weibull ( d, ( ρa K ) -1 ∕ d )                                 |
| Distribution function        | P { L K ≤ l } = 1 -exp{- ρa K l d } , l ≥ 0                          |
| Density                      | g K ( l ) = dρa K l d -1 exp{- ρa K l d } , l ≥ 0                    |
| Hazard function              | h K ( l ) = dρa K l d -1 , l > 0                                     |
| Cumulative hazard function   | H K ( l ) = ρa K l d , l ≥ 0                                         |
| p -quantile, 0 < p < 1       | Q ( p ) = ( ρa K ) -1 ∕ d [-log(1- p )] 1 ∕ d                        |
| Median                       | med( L K ) = ( ρa K ) -1 ∕ d (log 2) 1 ∕ d                           |
| Raw moment                   | E [ L m K ] = ( ρa K ) - m ∕ d Γ ( 1+ m d ) , m ≥ 0                  |
| Mean length                  | E [ L K ] = ( ρa K ) -1 ∕ d Γ ( 1+ 1 d )                             |
| Variance                     | var( L K ) = ( ρa K ) -2 ∕ d [ Γ ( 1+ 2 d ) -Γ ( 1+ 1 d ) 2 ]        |
| Coefficient of variation     | CV( L K ) = ⎡ ⎢ ⎢ ⎢ ⎣ Γ ( 1+ 2 d ) Γ ( 1+ 1 d ) 2 -1 ⎤ ⎥ ⎥ ⎥ ⎦ 1 ∕ 2 |
| Exponential transform        | ρa K ( L K ) d ∼ Exp(1)                                              |
| Standardized edge length     | ( ρa K ) 1 ∕ d L K ∼ Weibull( d, 1)                                  |
| Planar specialization, d = 2 | L K ∼ Rayleigh ( 1 √ 2 ρa K )                                        |
