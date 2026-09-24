---
id: "Espino_2026_Stepping-Stone-Diversion-Neighborhoods"
source_pdf: "../pdf/Espino_2026_Stepping-Stone-Diversion-Neighborhoods.pdf"
source_filename: "Espino_2026_Stepping-Stone-Diversion-Neighborhoods.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "excellent"
extraction_score: 108.0
visual_assets: "disabled"
references_file: "../references/Espino_2026_Stepping-Stone-Diversion-Neighborhoods.references.md"
---

<!-- p:1 -->

## Geometry and Volume of Stepping-Stone Diversion Neighborhoods in Euclidean Spaces of Arbitrary Dimension

Heriberto Espino-Montelongo a , ∗ , Héctor Maravillo b

a Universidad de las Américas Puebla, Ex Hacienda Santa Catarina Mártir S/N, San Andrés Cholula, 72810, Puebla, Mexico

b Universidad Autónoma de la Ciudad de México, Ciudad de México, 06720, Mexico

## ARTICLE INFO

Keywords : Stepping-stone graph empty-region graph proximity graph volume constant stochastic geometry computational geometry

### 1. Introduction

An empty-region proximity graph joins two sites whenever a region determined by them contains no other site. Classical examples include the Gabriel graph, the relative-neighborhood graph, and the β -skeletons (Gabriel and Sokal, 1969; Toussaint, 1980; Jaromczyk and Toussaint, 1992; Kirkpatrick and Radke, 1985). The theoretical, probabilistic, and algorithmic properties of proximity graphs have been extensively studied (Bose and Smid, 2013; Devroye, 1988; Cardinal, Collette and Langerman, 2009). Higher-dimensional proximity constructions include relativeneighborhood graphs in R 3 (Agarwal and Matoušek, 1992) and extensions of proximity regions to higher dimensions (Ceyhan, 2010). These graphs also have applications in pattern recognition, data analysis, and spatial-network modeling (Jaromczyk and Toussaint, 1992; Watanabe, 2008).

The stepping-stone graph was introduced by Kannangara, Tanin, Harwood and Karunasekera (2018) for movement analysis and subsequently developed in (Kannangara, Tanin, Harwood and Karunasekera, 2019). Those works study the parameterized family of planar proximity graphs obtained as the diversion parameter varies, its relationship with classical proximity graphs, and its application to movement-corridor analysis. The parameter regulates how readily a third site can serve as a diversion between a pair of sites and hence controls

∗ Corresponding author

Email addresses:

heriberto.espinomo@udlap.mx

Espino-Montelongo);

(H.

hector.maravillo@uacm.edu.mx

(H. Maravillo)

ORCID(s):

0009-0009-1230-2931

0000-0002-6101-1964

(H. Maravillo)

(H. Espino-Montelongo);

##### ABSTRACT

The stepping-stone graph forms a one-parameter family of empty-region graphs originally introduced in the plane. We develop a geometric, graph-theoretic, and probabilistic analysis of the stepping-stone graph in R d , for every d ≥ 2 . The volume of the diversion neighborhood factorizes as the d th power of the distance between the defining sites times a normalized constant that depends only on α , the steppingstone parameter. An explicit boundary parametrization reduces the original d -dimensional volume problem to a one-dimensional integral. We recover the degenerate case and the case corresponding to the region defining the Gabriel graph and prove, in every dimension, that, after removing the two defining sites, the finite-parameter neighborhoods converge from within to the open lune defining the relative-neighborhood graph. Consequently, their volumes converge to the classical volume of the lune defining the relative-neighborhood graph, for which we record an equivalent regularized incomplete-beta representation. For arbitrary ambient dimension, we also prove strict region and volume monotonicity, derive the corresponding inclusions among classical proximity graphs, establish connectivity, and show that, for α ≥ 2 , the defining empty-region condition need only be evaluated for those edges in the Gabriel graph that are not in the open relative-neighborhood graph. The resulting volume constant specializes existing expected-size results for random proximity graphs. Finally, a change of variables gives a stable quadrature formula, which we validate independently by rejection sampling applied directly to the defining inequality.

the edges retained by the graph. We denote their parameter by α , reserving d for the ambient dimension.

In the original formulation, a planar point belongs to the diversion neighborhood when the sum of the α th powers of its distances to the two defining sites does not exceed the α th power of the distance between the sites. For a point set V , two points p, q ∈ V are adjacent in the stepping-stone graph precisely when this neighborhood contains no point of V ⧵ { p, q } . The diversion neighborhood reduces to the segment joining the sites at α = 1 and equals the region associated with the Gabriel graph at α = 2 . It has been shown that the relative-neighborhood graph is the limiting memberofthe graph family and that the family is nested under edge inclusion (Kannangara et al., 2018, 2019). Although the original definition is planar, the same inequality defines a diversion neighborhood in R d for every d ≥ 2 .

The principal contribution of this paper is a unified arbitrary-dimensional framework for the stepping-stone diversion neighborhood. For every d ≥ 2 , we derive its similarity factorization, obtain an explicit boundary parametrization and a one-dimensional integral for its normalized volume, and establish the resulting graph inclusions, connectivity properties, and probabilistic consequences. The volume is especially relevant under random-point models, where it enters empty-region probabilities and the constants governing expected graph size. To our knowledge, an explicit boundary parametrization and a dimension-uniform one-dimensional volume representation have not previously been established for the stepping-stone family.

The main difficulty is that the defining distance condition describes the region only implicitly. Direct numerical computation therefore treats every choice of dimension and parameter as a new multidimensional integration problem over a curved region. We instead place the two sites in a standard position and exploit the rotational symmetry around the line joining them. An explicit description of the resulting boundary profile then reduces the volume calculation to a one-dimensional integral.


<!-- p:2 -->


The similarity reduction provides a normalization principle. Once the dimension d and the parameter α are fixed, changing the distance between the two sites changes only the scale of the diversion neighborhood, not its normalized shape, so its volume factorizes into the d th power of that distance and a constant depending only on α and d . The main theorem is the analytic reduction from the implicitly defined boundary to an explicit parametrization and then to a one-dimensional integral for this constant.

Wealso derive a numerically stable form for its evaluation and recover the degenerate segment, the closed ball associated with the Gabriel graph, and the relative-neighborhood limit. We further prove, for every d ≥ 2 , that both the diversion neighborhoods and their volumes increase strictly with α , while the corresponding empty-region graphs decrease under edge inclusion. We establish strict containment in the closed ball defining the Gabriel graph for 1 ≤ α &lt; 2 , obtain dimension-dependent bounds for the normalized volume constants, and derive connectivity and classical graph inclusions. These results refine the previously known monotonic decrease of the planar stepping-stone graphs by establishing strict geometric and volumetric monotonicity in arbitrary dimension.

We locate the stepping-stone graph within the classical inclusion hierarchy involving the minimum spanning tree, relative-neighborhood graph, Gabriel graph, and Delaunay graph, and obtain connectivity in every ambient dimension. These inclusions are consequences of the region comparisons. For each fixed finite point set, the nested graph family stabilizes exactly at the open-lune relative-neighborhood graph after a finite, point-set-dependent parameter.

For diversion-parameter values of two or greater, every edge in the stepping-stone graph must also be an edge in the Gabriel graph, whereas every edge in the open-lune relativeneighborhood graph is automatically retained. Consequently, once the Gabriel and open-lune relative-neighborhood graphs have been constructed, only those edges in the Gabriel graph that are not also edges in the relative-neighborhood graph remain undecided and require evaluation of the steppingstone empty-region condition. In the plane and under general position, the Delaunay graph provides a linear-size starting graph. In higher dimensions, however, the inclusions in the Delaunay and Gabriel graphs do not by themselves provide a subquadratic worst-case starting set.

The relevance of the normalized volume constant is also reflected in probabilistic analyses of proximity graphs. Devroye's theorem for graphs defined by regular sets relates the volume of the normalized empty region to limiting expected degrees and asymptotic edge-count bounds (Devroye, 1988).

We verify the required regularity conditions for the steppingstone graph family and obtain the corresponding asymptotic expected degree and edge-count lower bound for every d ≥ 2 . In the planar Poisson setting, the same area constant can be used in Watanabe's edge-length approximation (Watanabe, 2008). These are applications of existing probabilistic frameworks; the contribution supplied here is the previously unavailable stepping-stone volume constant and its geometric derivation in arbitrary dimension.

For numerical evaluation, we derive a change of variables that removes the endpoint singularity present in the original integral representation. The computational companion to this paper (Espino-Montelongo and Maravillo, 2026) records the quadrature, visualization, and validation procedures, together with their outputs, sample counts, and deterministic seeds. The numerical values are independently validated through rejection sampling applied directly to the defining inequality; this calculation does not use the boundary parametrization or either quadrature formula.

The remainder of the paper is organized as follows. Section 2 defines the normalized diversion neighborhood and establishes similarity normalization and its elementary geometric properties. Section 3 derives the boundary parametrization and the one-dimensional volume formula and treats the degenerate case and the cases corresponding to the Gabriel and relative-neighborhood graphs. Section 4 proves strict region and volume monotonicity and records the resulting graph inclusions, connectivity, finite-parameter stabilization, and candidate-set consequences. Section 5 applies Devroye's theorem for graphs to obtain expecteddegree and edge-count results for the stepping-stone graph. It also specializes Watanabe's edge-length approximation to the planar stepping-stone family. Finally, Section 6 develops the stable quadrature, describes the computational implementation, and reports the independent numerical validation.

### 2. Definitions and geometric preliminaries

Throughout, d ≥ 2 denotes the ambient dimension, and all points and regions are considered in R d . We write 0 for the origin, e 1 for the first standard basis vector, and

$$B ( x , r ) \, \colon = \, \left \{ z \in \mathbb { R } ^ { d } \ \colon \| z - x \| \leq r \right \}$$

for the closed Euclidean ball of radius r centered at x ∈ R d , and

$$B ^ { \circ } ( x , r ) \colon = \{ z \in \mathbb { R } ^ { d } \ \colon \| z - x \| < r \}$$

for the corresponding open ball. Furthermore, λ d denotes d -dimensional Lebesgue measure, and

$$\kappa _ { d } \colon = \lambda _ { d } \left ( B ( 0 , 1 ) \right ) = \frac { \pi ^ { d / 2 } } { \Gamma ( 1 + d / 2 ) }$$

is the volume of the unit ball in R d .

Definition 1 (Stepping-stone diversion neighborhood) . Let p, q ∈ R d be distinct, and set

$$\ell _ { p , q } \colon = \| q - p \| \, , \quad u _ { p , q } \colon = \frac { q - p } { \ell _ { p , q } } .$$


<!-- p:3 -->


For α ≥ 1 , the stepping-stone diversion neighborhood determined by p and q is

$$S _ { S S , \alpha } ( p , q ) \colon = \left \{ z \in \mathbb { R } ^ { d } \ \colon \| z - p \| ^ { \alpha } + \| z - q \| ^ { \alpha } \leq \ell _ { p , q } ^ { \alpha } \right \} \cdot \quad \text {Altheos} \quad \begin{matrix} \text {A} \text {thought} \\ \text {dimes} \end{matrix} \quad \begin{matrix} \text {A} \text {thought} \\ \text {when} \end{matrix}$$

Its normalized region is

$$K _ { S S , \alpha } \colon = S _ { S S , \alpha } ( 0 , e _ { 1 } ) = \left \{ z \in \mathbb { R } ^ { d } \ \colon \| z \| ^ { \alpha } + \| z - e _ { 1 } \| ^ { \alpha } \leq 1 \right \} . \quad \text {tions of} \\$$

The normalized volume constant is

$$a _ { d , S S } ( \alpha ) \colon = \lambda _ { d } \left ( K _ { S S , \alpha } \right ) . & & ( 7 ) & \quad \text {finite} \\$$

Following the standard terminology for empty-region graphs (Devroye, 1988; Cardinal et al., 2009), we use the following arbitrary-dimensional formulation.

Definition 2 (Empty-region graph) . Let V ⊂ R d be finite or locally finite, and let N be a symmetric region assignment that associates with every pair of distinct points p, q ∈ R d a region

$$N ( p , q ) = N ( q , p ) \subseteq \mathbb { R } ^ { d } .$$

The empty-region graph induced by N on V is the simple undirected graph

$$G _ { N } ( V ) \colon = \left ( V , E _ { N } ( V ) \right ) , \quad \ \ ( 9 ) \quad P r o o { J }$$

where V is the vertex set and EN ( V ) is the edge set defined by

$$\{ p , q \} \in E _ { N } ( V ) \ \iff \ N ( p , q ) \cap \left ( V \ \{ p , q \} \right ) = \varnothing \ ( 1 0 ) \quad d ^ { - \dim }$$

for every pair of distinct vertices p, q ∈ V . For brevity, we write pq ∈ EN ( V ) to mean { p, q } ∈ EN ( V ) .

For later comparison, let p, q ∈ R d be distinct. The closed and open regions defining the corresponding Gabriel graphs are the closed and open balls with diameter pq , respectively (Gabriel and Sokal, 1969; Matula and Sokal, 1980):

$$G _ { c l } ( p , q ) \ \colon = \ B \left ( \frac { p + q } { 2 } , \frac { \ell _ { p , q } } { 2 } \right ) , \quad \ \ ( 1 1 ) \quad \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \$$

$$G _ { \text {op} } ( p , q ) \ \colon = \ B ^ { \circ } \left ( \frac { p + q } { 2 } , \frac { \ell _ { p , q } } { 2 } \right ) .$$

The closed and open regions defining the corresponding relative-neighborhood graphs are (Toussaint, 1980; Jaromczyk and Toussaint, 1992)

$$L _ { c l } ( p , q ) \ \colon = \ B ( p , \ell _ { p , q } ) \cap B ( q , \ell _ { p , q } ) , \quad ( 1 3 ) \quad t h r o u$$

$$L _ { \text {op} } ( p , q ) \ \colon = \ B ^ { \circ } ( p , \ell _ { p , q } ^ { \dagger } ) \cap B ^ { \circ } ( q , \ell _ { p , q } ) .$$

Henceforth, we refer to G cl ( p, q ) and G op ( p, q ) as the closed and open Gabriel balls, respectively, and to L cl ( p, q ) and L op ( p, q ) as the closed and open relative-neighborhood lunes, respectively. The associated empty-region graphs are denoted by GGcl ( V ) , GGop ( V ) , RNGcl ( V ) , and RNGop ( V ) .

Thus GGcl ( V ) ⊆ GGop ( V ) and RNGcl ( V ) ⊆ RNGop ( V ) . Although the corresponding region boundaries have zero d - dimensional volume, the graph conventions may only differ when a third site lies on such a boundary.

Throughout the paper, GG( V ) denotes GGcl ( V ) and RNG( V ) denotes RNGop ( V ) , consistently with the original stepping-stone construction and the empty-region conventions of Kannangara et al. (2018) and Cardinal et al. (2009). The alternative graphs GGop ( V ) and RNGcl ( V ) are always identified explicitly.

Definition 3 (Stepping-stone graph) . For a finite or locally finite set V ⊂ R d , the stepping-stone graph with parameter α is the graph G = ( V , E ) such that two distinct points p, q ∈ V are adjacent if

$$S _ { S S , \alpha } ( p , q ) \cap \left ( V \ \{ p , q \} \right ) = \emptyset .$$

Proposition 1 (Similarity normalization and volume factorization) . If Q is an orthogonal transformation satisfying Qe 1 = u p,q , then

$$S _ { S S , \alpha } ( p , q ) = p + \ell _ { p , q } Q K _ { S S , \alpha } .$$

Consequently,

$$\lambda _ { d } \left ( S _ { S S , \alpha } ( p , q ) \right ) = \ell _ { p , q } ^ { d } \, a _ { d , S S } ( \alpha ) .$$

Proof. For w ∈ R d , substitute z = p + l p,qQw in (5). The two normalized distances become ‖ w ‖ and ‖ ‖ w - e 1 ‖ ‖ , which proves (16). Translations and orthogonal transformations preserve Lebesgue measure, while dilation by l p,q multiplies d -dimensional volume by l d p,q , proving (17).

Thus it suffices to study the normalized region K SS ,α . Figure 1 shows the same three representative parameter values in two and three dimensions. The dashed planar boundary is the limiting relative-neighborhood lune.

To complement the static views in Figure 1, the computational companion (Espino-Montelongo and Maravillo, 2026) provides an interactive three-dimensional visualization of the normalized diversion neighborhood.

Proposition 2 (Elementary geometry) . For every α ≥ 1 , the region S SS ,α ( p, q ) is compact and convex. It is centrally symmetric about

$$m \colon = \frac { p + q } { 2 } ,$$

rotationally symmetric about the line through p and q and invariant under every Euclidean isometry fixing the line through p and q pointwise. If α &gt; 1 , then S SS ,α ( p, q ) has nonempty interior and is strictly convex.

Proof. The function

$$F _ { p , q , \alpha } ( z ) \colon = \| z - p \| ^ { \alpha } + \| z - q \| ^ { \alpha }$$


<!-- p:4 -->


x

K

SS,

α

,

α

1

=1.25

K

SS,

α

1


,

α

=2

K

SS,

α

,

α

=10

Figure 1: Normalized stepping-stone diversion neighborhoods for α = 1 . 25 , 2 , and 10 . Top: planar regions, with the limiting relative-neighborhood lune shown by the dashed boundary. Bottom: three-dimensional regions for the same parameter values. The defining sites are fixed at 0 and e 1 .

is continuous and convex for α ≥ 1 . Hence its sublevel set S SS ,α ( p, q ) is closed and convex. Its defining inequality implies

$$\| z - p \| \leq \ell _ { p , q } , \quad \| z - q \| \leq \ell _ { p , q } , \quad \text {only} \, \quad \ \ ( 2 0 ) \quad \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \$$

so the region is bounded and therefore compact.

The reflection z ↦ p + q - z exchanges the two distance terms and preserves the region, invariant under every Euclidean isometry fixing the line through p and q pointwise and therefore proving central symmetry. Every rotation about the line through p and q preserves both distances and therefore preserves the region.

For α &gt; 1 , the map z ↦ ‖ z - p ‖ α is strictly convex, and so is F p,q,α . If z 1 ≠ z 2 belong to the region and t ∈ (0 , 1) , then

$$F _ { p , q , \alpha } ( t z _ { 1 } + ( 1 - t ) z _ { 2 } ) & < t F _ { p , q , \alpha } ( z _ { 1 } ) \\ & + ( 1 - t ) F _ { p , q , \alpha } ( z _ { 2 } ) \quad ( 2 1 ) \\ & \leq \ell _ { p , q } ^ { \alpha } .$$

Thus the open segment joining z 1 and z 2 lies in the interior. Moreover,

$$F _ { p , q , \alpha } ( m ) = 2 \left ( \frac { \ell _ { p , q } } { 2 } \right ) ^ { \alpha } = 2 ^ { 1 - \alpha } \ell _ { p , q } ^ { \alpha } < \ell _ { p , q } ^ { \alpha } , \quad ( 2 2 ) \quad v e r s e$$

so the interior is nonempty.

### 3. Boundary parametrization and volume

All results in this section are valid for every ambient dimension d ≥ 2 ; the planar formula is recorded afterward only as a special case.

#### 3.1. Boundary parametrization

We work in the normalized configuration ( p, q ) = ( 0 , e 1 ) and write

$$z = ( X , Z ) , \quad X \in \mathbb { R } , \quad Z \in \mathbb { R } ^ { d - 1 } , \quad ( 2 3 )$$

with transverse radius Y ∶= ‖ Z ‖ . The boundary is specified implicitly by

$$\left ( X ^ { 2 } + Y ^ { 2 } \right ) ^ { \alpha / 2 } + \left ( ( X - 1 ) ^ { 2 } + Y ^ { 2 } \right ) ^ { \alpha / 2 } = 1 .$$

The following result turns this implicit equation into the boundary profile used throughout the volume calculation.

Proposition 3 (Boundary parametrization) . Let α &gt; 1 and set u 0 ∶= 2 -1 ∕ α . For u ∈ [ u 0 , 1] , define

$$\rho ( u ) \colon = ( 1 - u ^ { \alpha } ) ^ { 1 / \alpha } , \quad X _ { \alpha } ( u ) \colon = \frac { 1 + u ^ { 2 } - \rho ( u ) ^ { 2 } } { 2 } , \ ( 2 5 )$$

and define the midpoint-centered axial coordinate and transverse radius by

$$x _ { \alpha } ( u ) \colon = X _ { \alpha } ( u ) - \frac { 1 } { 2 } & = \frac { u ^ { 2 } - ( 1 - u ^ { \alpha } ) ^ { 2 / \alpha } } { 2 } , \\ y _ { \alpha } ( u ) \colon = \sqrt { u ^ { 2 } - X _ { \alpha } ( u ) ^ { 2 } }$$


<!-- p:5 -->


$$= \frac { 1 } { 2 } \left [ 4 u ^ { 2 } - \left ( 1 + u ^ { 2 } - ( 1 - u ^ { \alpha } ) ^ { 2 / \alpha } \right ) ^ { 2 } \right ] ^ { 1 / 2 } . \ \ ( 2 7 )$$

Then ( Xα ( u ) , y α ( u )) traces the complete boundary profile in the half-space X ≥ 1 ∕2 ; orthogonal transformations fixing the e 1 -axis give the complete right boundary of K SS ,α . Moreover,

$$x _ { \alpha } ( u _ { 0 } ) = 0 , \quad x _ { \alpha } ( 1 ) = \frac { 1 } { 2 } , \quad & ( 2 8 ) \\ \stackrel { \gtrsim } { \sim } 0$$

and

$$x _ { \alpha } ^ { \prime } ( u ) = u + u ^ { \alpha - 1 } ( 1 - u ^ { \alpha } ) ^ { ( 2 - \alpha ) / \alpha } > 0 , \quad ( u _ { 0 } \leq u < 1 ) . \ ( 2 9 )$$

Thus x α maps [ u 0 , 1] continuously and strictly increasingly onto [0 , 1 ∕2] .

Proof. Parametrize a boundary point by its distance to the first site, u ∶= ‖ z ‖ . Its distance to the second site is then ρ ( u ) because u α + ρ ( u ) α = 1 . On the right half, u ≥ ρ ( u ) , which is equivalent to u ≥ u 0 ; the endpoint u = 1 is the site e 1 . The two sphere equations

$$X ^ { 2 } + Y ^ { 2 } = u ^ { 2 } , \quad ( X - 1 ) ^ { 2 } + Y ^ { 2 } = \rho ( u ) ^ { 2 } \quad ( 3 0 )$$

give 2 X -1 = u 2 - ρ ( u ) 2 , and hence (26)-(27). Conversely, for every u ∈ [ u 0 , 1] we have

$$u + \rho ( u ) \geq u ^ { \alpha } + \rho ( u ) ^ { \alpha } = 1 , \quad | u - \rho ( u ) | \leq 1 , \ ( 3 1 )$$

so the two spheres intersect and (27) is real. These equations therefore construct a boundary point, and every boundary point in the right half has exactly one value of u . The endpoint identities follow by substitution. Differentiating (26) gives (29), whose two terms are positive on [ u 0 , 1) . For α &gt; 2 , the second term has an endpoint singularity at u = 1 . Since 1 - u α ∼ α (1 - u ) and 2 ∕ α - 1 &gt; -1 , the singularity is integrable; the integrals below are interpreted as improper integrals in that case. □

#### 3.2. One-dimensional volume formula

Theorem 1 (One-dimensional volume formula) . Let d ≥ 2 and α &gt; 1 . Then

$$a _ { d , S S } ( \alpha ) = 2 \kappa _ { d - 1 } \int _ { 2 ^ { - 1 / \alpha } } ^ { 1 } y _ { \alpha } ( u ) ^ { d - 1 } x _ { \alpha } ^ { \prime } ( u ) \, d u , \quad ( 3 2 )$$

where y α and x ′ α are given by (27) and (29) . Together with Proposition 1, this determines the volume for every pair of distinct sites in R d .

Proof. Every point z = ( X,Z ) in the normalized region satisfies 0 ≤ X ≤ 1 . Indeed, (6) implies

$$\| z \| \leq 1 \quad \text {and} \quad \| z - e _ { 1 } \| \leq 1 , \quad \text { (33)}$$

since both terms on its left-hand side are nonnegative. If X &lt; 0 , then

$$\left \| z - e _ { 1 } \right \| \geq | 1 - X | = 1 - X > 1 , \quad \ \ a v a l i n g r a l { 3 } { 4 }$$

y

x

Figure 2: Midpoint-centered slicing of K SS ,α . The right half is parametrized by x = x α ( u ) , and the transverse radius is y α ( u ) .

whereas, if X &gt; 1 , then

$$\| z \| \geq | X | = X > 1 .$$

Both cases contradict the preceding necessary inequalities. Hence the normalized region is contained in the slab 0 ≤ X ≤ 1 .

For x ∈ [0 , 1 ∕2] , define the transverse section

$$\mathcal { S } _ { x } \colon = \{ Z \in \mathbb { R } ^ { d - 1 } \ \colon ( x + 1 / 2 , Z ) \in K _ { S S , \alpha } \} \, .$$

By Proposition 2,  x is compact, convex, and invariant under every orthogonal transformation of R d -1 . Moreover, 0 ∈  x , since the segment [ 0 , e 1 ] is contained in the normalized region.

Let

$$R ( x ) \colon = \max \left \{ \| Z \| \, \colon Z \in S _ { x } \right \} ,$$

where the maximum exists by compactness. If Z ∗ ∈  x satisfies ‖ ‖ Z ∗ ‖ ‖ = R ( x ) , orthogonal invariance implies that

$$\left \{ Z \in \mathbb { R } ^ { d - 1 } \, \colon \, \| Z \| = R ( x ) \right \} \subseteq S _ { x } .$$

Since  x is convex, it contains the convex hull of this sphere, namely the closed ball of radius R ( x ) . Conversely, the definition of R ( x ) implies that every Z ∈  x satisfies ‖ Z ‖ ≤ R ( x ) . Hence

$$\mathcal { S } _ { x } = \left \{ Z \in \mathbb { R } ^ { d - 1 } \, \colon \| Z \| \leq R ( x ) \right \} ,$$

and therefore

$$\lambda _ { d - 1 } ( \mathcal { S } _ { x } ) = \kappa _ { d - 1 } R ( x ) ^ { d - 1 } .$$

By Proposition 3, the boundary of the right half is given by x = x α ( u ) and R ( x α ( u )) = y α ( u ) for u ∈ [ u 0 , 1] , and x α is a valid change of variables from [ u 0 , 1] onto [0 , 1 ∕2] .


<!-- p:6 -->


By Cavalieri's principle,

$$\lambda _ { d } ( K _ { S S , \alpha } \cap \{ X \geq 1 / 2 \} ) = \int _ { 0 } ^ { 1 / 2 } \kappa _ { d - 1 } R ( x ) ^ { d - 1 } \, d x . \ ( 4 1 ) \quad \text {stat} \quad \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \$$

Changing variables from x to u gives

$$\lambda _ { d } ( K _ { S S , \alpha } \cap \{ X \geq 1 / 2 \} ) = \kappa _ { d - 1 } \int _ { u _ { 0 } } ^ { 1 } y _ { \alpha } ( u ) ^ { d - 1 } x _ { \alpha } ^ { \prime } ( u ) \, d u . \ ( 4 2 ) \quad _ { c o n s t a }$$

Finally, the reflection ( X,Z ) ↦ (1 - X,Z ) preserves K SS ,α and exchanges the two halves. The midpoint hyperplane has zero d -dimensional Lebesgue measure, so multiplying the last display by 2 proves (32).

Remark 1 (Planar specialization) . For d = 2 , κ d -1 = κ 1 = 2 , and therefore

$$a _ { 2 , S S } ( \alpha ) = 4 \int _ { 2 ^ { - 1 / \alpha } } ^ { 1 } y _ { \alpha } ( u ) x _ { \alpha } ^ { \prime } ( u ) \, d u .$$

#### 3.3. Special and limiting cases

The graph identity at α = 2 was established in the original planar stepping-stone study by Kannangara et al. (2018, Theorem 3.4). The next proposition records the corresponding diversion regions and their normalized volumes in every dimension, together with the degenerate case α = 1 .

Proposition 4 (Degenerate and Gabriel graph region cases) . For every d ≥ 2 ,

$$a _ { d , S S } ( 1 ) = 0 ,$$

whereas

$$a _ { d , S S } ( 2 ) = \frac { \kappa _ { d } } { 2 ^ { d } } .$$

At α = 1 , the diversion neighborhood is the segment [ p, q ] ; at α = 2 , it is the closed ball with diameter pq . In particular, SSG2 ( V ) = GG( V ) for every finite or locally finite point set V . At α = 1 , two sites are adjacent exactly when the open segment joining them contains no other point of V ; consequently, SSG1 ( V ) is complete whenever no three points of V are collinear.

Proof. At α = 1 , the triangle inequality shows that

$$\| z - p \| + \| z - q \| \leq \ell _ { p , q }$$

holds precisely on the segment joining p and q , which has zero d -dimensional measure. At α = 2 , let m = ( p + q ) ∕2 . The parallelogram identity gives

$$\| z - p \| ^ { 2 } + \| z - q \| ^ { 2 } = 2 \, \| z - m \| ^ { 2 } + 2 \left ( \frac { \ell _ { p , q } } { 2 } \right ) ^ { 2 } . \ ( 4 7 ) \quad \text {cap} \ v .$$

Thus the region is the ball centered at m with radius l p,q ∕2 , and its normalized volume is κ d ∕2 d . The graph identity follows from the closed-ball convention in the definition of GG( V ) . The characterization at α = 1 follows by deleting the two defining sites from the segment [ p, q ] .

The convergence of the planar graph to the relativeneighborhood graph was identified by Kannangara et al. (2018, Theorem 3.5). The following result strengthens that statement by identifying the increasing union of the diversion regions and the limiting volume in arbitrary dimension.

Proposition 5 (Convergence to the relative-neighborhood lune) . Define the normalized relative-neighborhood volume constant by

$$a _ { d , \text {RNG} } \colon = \lambda _ { d } \left ( L _ { \text {op} } ( \emptyset , e _ { 1 } ) \right ) = \lambda _ { d } \left ( L _ { \text {cl} } ( \emptyset , e _ { 1 } ) \right ) .$$

As α → ∞ , the diversion neighborhoods converge from within to the open relative-neighborhood lune in the precise sense that

$$\bigcup _ { 1 < \alpha < \infty } \left ( S _ { S S , \alpha } ( p , q ) \, \smallsetminus \{ p , q \} \right ) = L _ { o p } ( p , q ) .$$

Moreover,

$$\lim _ { \alpha \to \infty } a _ { d , S S } ( \alpha ) = a _ { d , R N G } = \kappa _ { d } I _ { 3 / 4 } \left ( \frac { d + 1 } { 2 } , \frac { 1 } { 2 } \right ) . \quad ( 5 0 )$$

where I 3 ∕4 is the regularized incomplete beta function.

Proof. For z ∉ { p, q } , the defining inequality implies the strict bounds

$$\| z - p \| < \ell _ { p , q } , \quad \| z - q \| < \ell _ { p , q } .$$

Thus every finite-parameter diversion neighborhood, after removing its defining sites, is contained in L op ( p, q ) .

Conversely, let z ∈ L op ( p, q ) . Then

$$0 \leq \frac { \| z - p \| } { \ell _ { p , q } } < 1 , \quad 0 \leq \frac { \| z - q \| } { \ell _ { p , q } } < 1 ,$$

and consequently

$$\left ( \frac { \| z - p \| } { \ell _ { p , q } } \right ) ^ { \alpha } + \left ( \frac { \| z - q \| } { \ell _ { p , q } } \right ) ^ { \alpha } \longrightarrow 0 \quad \text {as } \alpha \to \infty . \, ( 5 3 )$$

Hence, for all sufficiently large α ,

$$\| z - p \| ^ { \alpha } + \| z - q \| ^ { \alpha } \leq \ell _ { p , q } ^ { \alpha } ,$$

so z ∈ S ( p, q )

$$& \| z - p \| ^ { \alpha } + \| z - q \| ^ { \alpha } \leq \ell _ { p , q } ^ { \alpha } , \\ \text {so } & z \in S _ { S S , \alpha } ( p , q ) . \\ & \text {This provos} \, ( 1 0 ) \, \text {, Sino m o m b o r s h i p is eventually constant}$$

This proves (49). Since membership is eventually constant at every point, the neighborhoods lie in the bounded closed lune, and deleting their two defining sites does not change Lebesgue measure, dominated convergence yields

$$\lim _ { \alpha \to \infty } \lambda _ { d } \left ( S _ { S S , \alpha } ( p , q ) \right ) = \lambda _ { d } \left ( L _ { \text {cl} } ( p , q ) \right ) .$$

The volume of the unit relative-neighborhood lune in arbitrary dimension was previously represented as a radial integral by Devroye (1988, Sec. 5, p. 59). Equivalently, in normalized coordinates, the midpoint hyperplane partitions L cl ( 0 , e 1 ) into two congruent unit-ball caps of height 1 ∕2 . The standard hyperspherical-cap formula of Li (2011) gives one cap volume

$$\frac { \kappa _ { d } } { 2 } I _ { 3 / 4 } \left ( \frac { d + 1 } { 2 } , \frac { 1 } { 2 } \right ) . \\$$

Doubling proves (50). For example, in dimension three the benchmarks corresponding to the Gabriel graph and relativeneighborhood-graph benchmarks are a 3 , SS (2) = π ∕6 and a 3 , RNG = 5 π ∕12 , respectively. □


<!-- p:7 -->


### 4. Monotonicity and graph consequences

The strict region and volume results, the graph inclusion chains, connectivity, and finite-parameter stabilization established in this section hold in every ambient dimension. The containment in the Delaunay and Gabriel graphs also remain valid in arbitrary dimension.

The linear bound on the number of Delaunay edges used as an initial candidate set is specific to the plane. In dimension three, both Delaunay and Gabriel graphs may have quadratic size, so neither containment yields a subquadratic worst-case set of edges to be tested.

#### 4.1. Strict region and volume monotonicity

The monotone decrease of the planar stepping-stone graph with the configuration parameter is due to Kannangara et al. (2018, Theorem 3.3). The next theorem proves the strict geometric refinement needed here: strict inclusion of the diversion regions, positive measure of their difference, and strict monotonicity of the normalized volume in every dimension.

Theorem 2 (Strict monotonicity) . For every 1 ≤ α 1 &lt; α 2 and every distinct p, q ∈ R d ,

$$S _ { S S , \alpha _ { 1 } } ( p , q ) \subsetneq S _ { S S , \alpha _ { 2 } } ( p , q ) , \\$$

and the set difference has positive d -dimensional measure. Consequently,

$$a _ { d , S S } ( \alpha _ { 1 } ) < a _ { d , S S } ( \alpha _ { 2 } ) .$$

Proof. For a, b ≥ 0 , the map

$$r \longmapsto ( a ^ { r } + b ^ { r } ) ^ { 1 / r } \, , \quad r > 0 ,$$

is nonincreasing. If z ∈ S SS ,α 1 ( p, q ) , then

$$\left ( \| z - p \| ^ { \alpha _ { 1 } } + \| z - q \| ^ { \alpha _ { 1 } } \right ) ^ { 1 / \alpha _ { 1 } } \leq \ell _ { p , q } .$$

The monotonicity of this map gives

$$\left ( r ^ { \alpha _ { 2 } } + s ^ { \alpha _ { 2 } } \right ) ^ { 1 / \alpha _ { 2 } } & \leq \left ( r ^ { \alpha _ { 1 } } + s ^ { \alpha _ { 1 } } \right ) ^ { 1 / \alpha _ { 1 } } \\ & \leq \ell _ { p , q } , \\$$

so z ∈ S SS ,α 2 ( p, q ) . Taking Lebesgue measure and using (17) gives the volume monotonicity.

The monotonicity of this map gives

$$\left ( r ^ { \alpha _ { 2 } } + s ^ { \alpha _ { 2 } } \right ) ^ { 1 / \alpha _ { 2 } } & \leq \left ( r ^ { \alpha _ { 1 } } + s ^ { \alpha _ { 1 } } \right ) ^ { 1 / \alpha _ { 1 } } \\ & \leq \ell _ { p , q } , \\$$

so z ∈ S SS ,α 2 ( p, q ) . Taking Lebesgue measure and using (17) gives the volume monotonicity.

To prove strictness, let m = ( p + q ) ∕2 and choose a unit vector v perpendicular to q - p . On the midpoint hyperplane, a point z = m + tv belongs to S SS ,α ( p, q ) precisely when

$$| t | \leq r _ { \alpha } , \quad r _ { \alpha } \colon = \ell _ { p , q } \sqrt { 2 ^ { - 2 / \alpha } - \frac { 1 } { 4 } } . \quad \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \$$

The function α ↦ 2 - 2 ∕ α is strictly increasing, so r α 1 &lt; r α 2 . Choose t strictly between these two radii. Then m + tv lies in the interior of the larger region and outside the closed smaller region. A neighborhood of this point is therefore contained in the set difference, which has positive d -dimensional measure. The strict inequality for the normalized volumes follows from (17). □

Corollary 1 (Continuous parameter calibration) . For every d ≥ 2 , the map α ↦ a d, SS ( α ) is continuous and strictly increasing on [1 , ∞) , with image [0 , a d, RNG ) . Consequently, every target volume c ∈ (0 , a d, RNG ) determines a unique finite parameter α &gt; 1 .

Proof. Let α n → α ≥ 1 . Away from the boundary of K SS ,α , continuity of the defining inequality implies eventual agreement of membership in K SS ,α n and K SS ,α . This boundary has Lebesgue measure zero: for α &gt; 1 it is the boundary of a convex body, while for α = 1 the entire region is a line segment. All these regions are contained in the bounded closed relative-neighborhood lune, so dominated convergence proves continuity of their volumes. The image and uniqueness now follow from Propositions 4 and 5 and Theorem 2. □

Corollary 2 (Bounds and Gabriel graph region comparison) . For every d ≥ 2 , the following holds:

$$\begin{cases} a _ { d , S S } ( \alpha ) = 0 , & \alpha = 1 , \\ 0 < a _ { d , S S } ( \alpha ) < \kappa _ { d } / 2 ^ { d } , & 1 < \alpha < 2 , \\ a _ { d , S S } ( \alpha ) = \kappa _ { d } / 2 ^ { d } , & \alpha = 2 , \\ \kappa _ { d } / 2 ^ { d } < a _ { d , S S } ( \alpha ) < a _ { d , R N G } , & 2 < \alpha < \infty . \end{cases}$$

Moreover, for every distinct p, q ∈ R d ,

$$S _ { S S , \alpha } ( p , q ) \subsetneq G G _ { c l } ( p , q ) \ \ ( 1 \leq \alpha < 2 ) ,$$

whereas GGcl ( p, q ) ⊊ S SS ,α ( p, q ) for every 2 &lt; α &lt; ∞ .

Proof. Combine Propositions 4 and 5 and Theorem 2. The strict upper bound by a d, RNG at every finite parameter follows because a strictly increasing function cannot attain its limiting value at a finite argument.

#### 4.2. Monotonicity and graph inclusions

For i ∈ {1 , 2} , let Si ( p, q ) be a region assigned to each pair of distinct sites, and let Gi ( V ) = ( V , E i ( V )) join p and q precisely when Si ( p, q ) contains no point of V ⧵ { p, q } . Directly from this definition, whenever the region inclusion below holds for every distinct pair, so does the edge inclusion:

$$S _ { 1 } ( p , q ) \ \{ p , q \} & \subseteq S _ { 2 } ( p , q ) \ \{ p , q \} \\ & \Longrightarrow E _ { 2 } ( V ) \subseteq E _ { 1 } ( V ) .$$

Indeed, if the intersection of S 2 ( p, q ) with V ⧵ { p, q } is empty, then the corresponding intersection with S 1 ( p, q ) is also empty.


<!-- p:8 -->


Let MST( V ) denote a Euclidean minimum spanning tree of a nonempty finite point set V , and let Del( V ) denote its Delaunay graph (Mitchell and Mulzer, 2017). With the closed Gabriel-ball and open relative-neighborhood lune conventions adopted above, the standard inclusions are

$$M S T ( V ) \subseteq R N G ( V ) \subseteq G G ( V ) \subseteq D e l ( V ) .$$

The hierarchy is reviewed by Jaromczyk and Toussaint (1992); the closed-ball Gabriel convention and the corresponding inclusion in the Delaunay graph are explicit in Matula and Sokal (1980) and Cardinal et al. (2009). In particular, an empty closed ball with diameter pq certifies that pq is a Delaunay edge, including in configurations with cospherical sites.

In the planar setting, the parameter endpoint cases corresponding to the Gabriel and relative-neighborhood graphs, and the containment in the Delaunay graph for parameters at least two were established by Kannangara et al. (2018, Theorems 3.3-3.5 and 3.11). The next proposition gives a region-based derivation that makes the open-closed conventions explicit and extends the resulting inclusion chains to every ambient dimension.

Proposition 6 (Monotonicity and classical proximity-graph inclusions) . If 1 ≤ α 1 &lt; α 2 , then

$$E _ { \alpha _ { 2 } } ( V ) \subseteq E _ { \alpha _ { 1 } } ( V ) . \quad \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \$$

Thus {SSG α ( V ) ∶ α ≥ 1} is a monotonically decreasing family of graphs under edge inclusion, although the inclusion need not be strict for a fixed point set. Furthermore, for every nonempty finite V ⊂ R d and every finite α ≥ 1 ,

$$M S T ( V ) \subseteq R N G ( V ) \subseteq S S G _ { \alpha } ( V ) .$$

If 1 ≤ α ≤ 2 , then

$$M S T ( V ) \subseteq R N G ( V ) \subseteq G G ( V ) \subseteq S S G _ { \alpha } ( V ) . \quad ( 7 0 )$$

If α ≥ 2 , then

$$M S T ( V ) \subseteq R N G ( V ) & \subseteq S S G _ { \alpha } ( V ) & \text { and } & \text { and } \\ & \subseteq G G ( V ) \subseteq D e l ( V ) . & \text { } & \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text { } \text {$$

Proof. The first edge inclusion follows directly from Theorem 2 and the preceding implication; it is the region-inclusion formulation of the nestedness proved for the original d - spectrum by Kannangara et al. (2018, 2019).

For z ∉ { p, q } , the inequality defining S SS ,α ( p, q ) implies

$$\| z - p \| < \ell _ { p , q } , \quad \| z - q \| < \ell _ { p , q } .$$

Thus S SS ,α ( p, q ) ⧵ { p, q } ⊂ L op ( p, q ) , and the same implication gives RNG( V ) ⊆ SSG α ( V ) . The remaining steppingstone inclusions follow from Proposition 4 and Theorem 2; the other inclusions are classical.

Corollary 3 (Connectivity in arbitrary dimension) . For every nonempty finite V ⊂ R d and every finite α ≥ 1 , the graph SSG α ( V ) is connected.

Proof. Connectivity follows from

$$M S T ( V ) \subseteq R N G _ { o p } ( V ) \subseteq S S G _ { \alpha } ( V ) .$$

Therefore, SSG α ( V ) contains a connected spanning subgraph and is itself connected.

Corollary 4 (Finite-parameter stabilization) . For every finite V ⊂ R d , there exists a finite parameter α ∗ ( V ) ≥ 1 such that

$$S S G _ { \alpha } ( V ) = R N G _ { o p } ( V ) \quad \text {for all $\alpha\geq \alpha_{*}(V)$} .$$

Proof. For every pair p, q ∈ V that is not an edge of RNGop ( V ) , choose a point z ∈ L op ( p, q ) ∩ ( V ⧵ { p, q }) . By Proposition 5, that point belongs to S SS ,α ( p, q ) for every sufficiently large α . There are only finitely many such pairs, so their individual thresholds have a finite maximum α ∗ ( V ) ; if there are no such pairs, take α ∗ ( V ) = 1 . Beyond this threshold, no non-relative-neighborhood edge remains, while Proposition 6 preserves every relative-neighborhood edge. □

Remark 2 (Dependence and provenance of the stabilization threshold) . In the planar case, finite stabilization is already implicit in the finite deletion thresholds of the d -spectrum introduced by Kannangara et al. (2018, Def. 3.12); the preceding argument extends the observation to every fixed ambient dimension. The threshold cannot be chosen uniformly over finite point sets.

To see that the stabilization threshold cannot be chosen uniformly, let p = (0 , 0) , q = (1 , 0) , and z = (1∕2 , h ) , where 0 &lt; h &lt; √ 3∕2 . Setting r h = √ 1∕4 + h 2 &lt; 1 , the point z enters S SS ,α ( p, q ) precisely when 2 r α h ≤ 1 , or equivalently when

$$\alpha \geq \frac { \log 2 } { - \log r _ { h } } .$$

This threshold tends to infinity as h ↑ √ 3∕2 .

Remark 3 (Planar Delaunay starting graph) . For V ⊂ R 2 and α ≥ 2 , SSG α ( V ) is a subgraph of the Gabriel graph and hence of the Delaunay graph. Therefore, if V is in general position and n = | V | ≥ 3 , the defining empty-region condition need only be tested for at most 3 n - 6 Delaunay edges, rather than for all ( n 2 ) pairs. Testing each candidate against the remaining n - 2 sites still gives a naive O ( n 2 ) procedure. In their planar d -spectrum algorithm, Kannangara et al. (2018, 2019) use the Delaunay triangulation as the starting graph. Although the Delaunay containment remains valid in higher dimensions, it does not yield a subquadratic worst-case candidate set, since Delaunay graphs can already have Θ( n 2 ) edges in R 3 (Agarwal and Matoušek, 1992). The obstruction is not removed merely by restricting the initial candidate set to Gabriel graph edges, since Gabriel graphs themselves can have Θ( n 2 ) edges in R 3 (Chazelle, Edelsbrunner, Guibas, Hershberger, Seidel and Sharir, 1994, Lemma 5.1). Hence the candidate-edge characterization is not, by itself, a subquadratic construction algorithm in higher dimensions.


<!-- p:9 -->


### 5. Probabilistic consequences

The normalized volume is also the parameter that enters the expected-size theory of regular empty-region graphs. The first part of this section records the arbitrary-dimensional consequences of Devroye's theorem. The second part is an explicitly planar specialization of the graph-edge-length approximation of Watanabe (2008). The verification below uses compactness, midpoint symmetry, and similarity equivariance from Section 2; convexity itself is not a hypothesis in Devroye's definition.

#### 5.1. Expected size in arbitrary dimension

Proposition 7 (Regularity in the sense of Devroye) . For every fixed α &gt; 1 , the stepping-stone construction defines a regular set in the sense of Devroye (1988), with normalized volume a d, SS ( α ) .

Proof. In Devroye's terminology, take the bounded target set

$$T _ { \alpha } \colon = \{ ( u , v ) \in \mathbb { R } \times [ 0 , \infty ) \, \colon \\ ( u ^ { 2 } + v ^ { 2 } ) ^ { \alpha / 2 } + \left ( ( 1 - u ) ^ { 2 } + v ^ { 2 } \right ) ^ { \alpha / 2 } \leq 1 \} .$$

By Proposition 2, it is bounded and symmetric about u = 1∕2 . Given distinct p, q ∈ R d , the translation, rotation, and rescaling in Proposition 1 reduce membership of any point z ∈ R d in S SS ,α ( p, q ) to membership of the pair formed by its axial coordinate and its distance from that axis in T α . Allowing every transverse vector with prescribed radius v produces K SS ,α , whose volume is a d, SS ( α ) . This volume is strictly positive for α &gt; 1 because Proposition 2 gives nonempty interior. These are precisely the boundedness, symmetry, and similarity requirements in Devroye's definition of a regular set. □

Corollary 5 (Expected degree and number of edges) . Fix d ≥ 2 and α &gt; 1 . Let X 1 , ... , X n be independent points with a common density f with respect to d -dimensional Lebesgue measure on R d , and let Nn ( X 1 ) denote the number of stepping-stone neighbors of X 1 at parameter α . Then, for f ( x ) d x -almost every x ,

$$\lim _ { n \to \infty } \mathbb { E } [ N _ { n } ( X _ { 1 } ) \, | \, X _ { 1 } = x ] = \frac { \kappa _ { d } } { a _ { d , S S } ( \alpha ) } .$$

If Mn denotes the total number of undirected edges, then

$$\liminf _ { n \to \infty } \frac { \mathbb { E } [ M _ { n } ] } { n } \geq \frac { \kappa _ { d } } { 2 a _ { d , S S } ( \alpha ) } .$$

Proof. By Proposition 7, the volume in Devroye's regular-set theorem is a d, SS ( α ) , while the volume denoted there by V d is κ d . Substitution in the conditional degree conclusion of that theorem gives (77). Its edge-count conclusion gives (78); the factor 1 ∕2 appears because the sum of the vertex degrees counts every undirected edge twice. □

#### 5.2. Planar Poisson specialization

We now specialize to d = 2 and use the homogeneous Poisson model of Watanabe (2008), with point intensity ρ &gt; 0 . For brevity set

$$a \colon = a _ { 2 , S S } ( \alpha ) , \quad \alpha > 1 .$$

Proposition 8 (Planar edge-length approximation) . Within Watanabe's approximation, let L denote the modeled edge length for the planar stepping-stone graph generated by a homogeneous Poisson process of intensity ρ . Its distribution function is

$$F _ { L } ( r ) = 1 - \exp \{ - \rho a r ^ { 2 } \} , \quad r \geq 0 ,$$

and its density is

$$f _ { L } ( r ) = 2 \rho a r \exp \{ - \rho a r ^ { 2 } \} , \quad r > 0 .$$

Consequently

$$\mathbb { E } [ L ] = \frac { \sqrt { \pi } } { 2 \sqrt { \rho a } } , \quad \text {Var} ( L ) = \frac { 4 - \pi } { 4 \rho a } .$$

Proof. For a pair of sites at distance r , the area factorization (17) gives the area of the diversion neighborhood

$$A ( r ) = a r ^ { 2 } .$$

The Poisson probability that this region contains no point is

$$\P ^ { \text {city} } _ { \ } P \{ 0 \text { points in } A ( r ) \} = \exp \{ - \rho A ( r ) \} = \exp \{ - \rho a r ^ { 2 } \} .$$

Within Watanabe's approximation, the probability that the restricted search has found at least one point by distance r is the complement of this void probability; this gives (80). Differentiation with respect to r gives (81).

For completeness, the same gamma-integral calculation gives

$$\mathbb { E } [ L ] = 2 \rho a \int _ { 0 } ^ { \infty } r ^ { 2 } e ^ { - \rho a r ^ { 2 } } \, d r = \frac { \Gamma ( 3 / 2 ) } { \sqrt { \rho a } } = \frac { \sqrt { \pi } } { 2 \sqrt { \rho a } } .$$

Moreover,

$$\mathbb { E } [ L ^ { 2 } ] = 2 \rho a \int _ { 0 } ^ { \infty } r ^ { 3 } e ^ { - \rho a r ^ { 2 } } \, d r = \frac { 1 } { \rho a } ,$$

so subtracting E [ L ] 2 yields the variance in (82). At α = 2 ,

$$a _ { 2 , S S } ( 2 ) = \pi / 4 ,$$

and the formula recovers Watanabe's formula for the Gabriel graph. As α → ∞ ,

$$a _ { 2 , S S } ( \alpha ) \longrightarrow \frac { 2 \pi } { 3 } - \frac { \sqrt { 3 } } { 2 } ,$$

which recovers his approximation for the relativeneighborhood graph. □


<!-- p:10 -->


### 6. Numerical evaluation and validation

#### 6.1. Stable quadrature

The formula in Theorem 1 is suitable for numerical evaluation, although its original form is not always the most stable one. For α &gt; 2 , the derivative in (29) diverges as u → 1 , but the transverse radius simultaneously tends to zero. A direct endpoint expansion gives that

$$y _ { \alpha } ( u ) ^ { d - 1 } x _ { \alpha } ^ { \prime } ( u ) \text { is of order } ( 1 - u ) ^ { ( d + 1 ) / \alpha - 1 } . \quad \ \ ( 8 9 ) \quad \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \$$

Therefore, the complete integrand is unbounded only when α &gt; d + 1 , and it remains integrable for every finite α &gt; 1 . Nevertheless, adaptive quadrature may lose accuracy near the endpoint, which motivates the following reparametrization.

Proposition 9 (Stable quadrature) . For α &gt; 1 , define

$$u ( t ) \colon = ( 1 - t ^ { \alpha } ) ^ { 1 / \alpha } , & & ( 9 0 ) \\$$

and

Then

$$a _ { d , S S } ( \alpha ) = 2 \kappa _ { d - 1 } \int _ { 0 } ^ { 2 ^ { - 1 / \alpha } } & & \text {th} s & & \text {implies} & & \text {comple} & & \text {th} s \\ & \widetilde { y } _ { \alpha } ( t ) ^ { d - 1 } \left ( t + u ( t ) ^ { 2 - \alpha } t ^ { \alpha - 1 } \right ) \text { d t} . & & \\$$

and the integrand has no endpoint singularity.

Proof. Parametrize the right boundary by the distance to the second site,

$$t = ( 1 - u ^ { \alpha } ) ^ { 1 / \alpha } , \quad u = ( 1 - t ^ { \alpha } ) ^ { 1 / \alpha } .$$

Then 0 ≤ t ≤ 2 - 1 ∕ α and x = ( u 2 - t 2 ) ∕2 . Since u ′ ( t ) = - u ( t ) 1α t α -1 ,

$$\frac { d x } { d t } = - \left ( t + u ^ { 2 - \alpha } t ^ { \alpha - 1 } \right ) .$$

The coordinate x ( t ) decreases from 1 ∕2 to 0 , so the slicing formula uses the positive element -d x = | d x ∕d t | d t . Substitution in (32) gives (92).The factorized expression for ̃ y α ( t ) follows from

$$4 u ^ { 2 } - ( 1 + u ^ { 2 } - t ^ { 2 } ) ^ { 2 } = ( u + t - 1 ) ( u + t + 1 ) \\ \cdot ( 1 + u - t ) ( 1 - u + t ) ,$$

after setting u = u ( t ) . Finally, as t → 0 , we have u ( t ) → 1 , u ( t ) 2α t α -1 → 0 because α &gt; 1 , and ̃ y α ( t ) → 0 . Therefore, the integrand extends continuously to the left endpoint and has no endpoint singularity.

Evaluating the transverse radius in this factored form reduces the cancellation caused by subtracting two nearly equal squared quantities; all four factors are nonnegative on the integration interval. The degenerate case is evaluated separately using a d, SS (1) = 0 from Proposition 4.

$$\widetilde { y } _ { \alpha } ( t ) \colon = \frac { 1 } { 2 } \left [ \left ( u ( t ) + t - 1 \right ) \left ( u ( t ) + t + 1 \right ) \\ \times \left ( 1 + u ( t ) - t \right ) \left ( 1 - u ( t ) + t \right ) \right ] ^ { 1 / 2 } .$$

#### 6.2. Implementation

An earlier implementation of the stepping-stone graph was developed in Java 8 by Kannangara et al. (2018, Sec. 4.2). For planar input, their implementation constructed the Delaunay triangulation, computed the d -spectrum, approximated edge d -values numerically with the secant method, and extracted the requested stepping-stone graph. It was used in their visualization and movement-analysis system.

The stepping-stone graph is also available in Python through PROXIMITYGRAPHS, an open-source package for constructing and analyzing proximity graphs (Maravillo, Villarreal de la Cerda and Espino-Montelongo, 2026). This makes the construction and the volume formulas available within Python scientific computing workflows rather than only through paper-specific scripts. The package is distributed under the MIT License and is available from PyPI.

For the stepping-stone family, the package provides Python routines for constructing diversion neighborhoods and graphs and for evaluating the normalized volume from the formulas developed above. GitHub public repository (Espino-Montelongo and Maravillo, 2026) uses these routines for the numerical evaluations and visualizations reported here. Additionally records the quadrature and Monte Carlo workflows, outputs, sample counts, and deterministic seeds required to reproduce the reported validation experiments. Thus PROXIMITYGRAPHS provides the reusable Python implementation, while the companion preserves the exact computational workflow for this article.

#### 6.3. Numerical curves and benchmark values

Figure 3 plots the volume constants themselves. The curves agree with the special and limiting values proved above: they start at zero when α = 1 , pass through the dimension-specific Gabriel graph value at α = 2 , increase strictly, and approach a d, RNG as α → ∞ . Numerically, the two low-dimensional crossings shown in the figure satisfy a 2 , SS ( α ) = a 3 , SS ( α ) at α ≈ 7 . 118390847 and a 2 , SS ( α ) = a 4 , SS ( α ) at α ≈ 23 . 643510648 . These intersections are numerical observations.

, RNG

ad

Parameter

α

Figure 3: Numerical values of a d, SS ( α ) for several dimensions on a logarithmic α -axis. The right endpoint shows a d, RNG , the relative-neighborhood limit. The auxiliary labels 7 . 12 and 23 . 64 mark the two numerical intersections described in the text.


<!-- p:11 -->


|   α = 1 . 25 - d | α = 1 . 25 - a quad   | α = 1 . 25 - ̂ a MC   | α = 1 . 25 - s.e.   |   α = 1 . 25 - 10 4 ε rel |   α = 1 . 25 - z |
|------------------|-----------------------|-----------------------|---------------------|---------------------------|------------------|
|                2 | 0.41429435            | 0.41431538            | 2 . 501e-5          |                     0.508 |            0.841 |
|                3 | 0.15209303            | 0.15209032            | 1 . 226e-5          |                    -0.178 |           -0.221 |
|                4 | 0.04995978            | 0.04995401            | 4 . 721e-6          |                    -1.156 |           -1.223 |
|                5 | 0.01493763            | 0.01493994            | 1 . 572e-6          |                     1.546 |            1.469 |
|                8 | 2 . 567962e-4         | 2 . 567629e-4         | 3 . 299e-8          |                    -1.297 |           -1.009 |
|                9 | 5 . 884669e-5         | 5 . 885745e-5         | 7 . 912e-9          |                     1.827 |            1.359 |
|               10 | 1 . 283446e-5         | 1 . 283558e-5         | 1 . 795e-9          |                     0.869 |            0.622 |
|               12 | 5 . 352895e-7         | 5 . 352658e-7         | 8 . 002e-11         |                    -0.443 |           -0.297 |
|               20 | 4 . 188191e-13        | 4 . 187867e-13        | 7 . 450e-17         |                    -0.772 |           -0.434 |

Table 1 Monte Carlo validation of the stable quadrature formula. Each row uses 10 8 samples. Here ε rel = ( a ̂ MC - a quad )∕ a quad , and z is the discrepancy divided by its Monte Carlo standard error. The notation x e k denotes x × 10 k .

|   α = 10 - d | α = 10 - a quad   | α = 10 - ̂ a MC   | α = 10 - s.e.   |   α = 10 - 10 4 ε rel |   α = 10 - z |
|--------------|-------------------|-------------------|-----------------|-----------------------|--------------|
|            2 | 1.1966680         | 1.1967769         | 6 . 732e-5      |                 0.910 |        1.617 |
|            3 | 1.2306930         | 1.2306571         | 9 . 406e-5      |                -0.291 |       -0.381 |
|            4 | 1.1257499         | 1.1255807         | 1 . 019e-4      |                -1.503 |       -1.660 |
|            5 | 0.93604703        | 0.93620155        | 9 . 501e-5      |                 1.651 |        1.626 |
|            8 | 0.34611889        | 0.34607030        | 4 . 336e-5      |                -1.404 |       -1.120 |
|            9 | 0.22068237        | 0.22068795        | 2 . 900e-5      |                 0.253 |        0.192 |
|           10 | 0.13394539        | 0.13397369        | 1 . 835e-5      |                 2.113 |        1.542 |
|           12 | 0.04328974        | 0.04329731        | 6 . 355e-6      |                 1.749 |        1.192 |
|           20 | 1 . 226485e-4     | 1 . 226420e-4     | 2 . 155e-8      |                -0.527 |       -0.300 |

#### 6.4. Independent rejection-sampling validation

The Monte Carlo calculation evaluates the original defining inequality in (6); it does not use the boundary parametrization or either quadrature formula.

The region is contained in the cylinder

$$C _ { d , \alpha } \colon = [ 0 , 1 ] \times B _ { d - 1 } ( 0 , r _ { \alpha } ) , \quad r _ { \alpha } \colon = \sqrt { 2 ^ { - 2 / \alpha } - \frac { 1 } { 4 } } . \ ( 9 6 ) \quad \text {yes if} \quad \ y s i s \ f o r e$$

Here Bd -1 (0 , r α ) denotes the closed ball of radius r α in R d -1 . Indeed, the defining inequality gives 0 ≤ X ≤ 1 . If ( X,Z ) belongs to the normalized region, midpoint symmetry in Proposition 2 shows that its reflection (1X,Z ) also belongs to it; convexity then places their midpoint ( 1 ∕ 2 , Z ) in the region. The largest possible transverse norm is therefore attained in the midpoint slice, where the defining equality gives ‖ Z ‖ = r α . Consequently,

$$V _ { d , \alpha } \colon = \lambda _ { d } ( C _ { d , \alpha } ) = \kappa _ { d - 1 } r _ { \alpha } ^ { d - 1 } .$$

If H of N independent uniform points in this cylinder satisfy (6), then

$$\hat { p } \colon = \frac { H } { N } , & & \text {lune of} \\ \hat { a } ^ { M C } = V _ { d , \alpha } \hat { p } = V _ { d , \alpha } \frac { H } { N } , & & \text {otherwise} \\ \hat { s } \equiv V _ { d , \alpha } \sqrt { \frac { \widehat { p } ( 1 - \widehat { p } ) } { N } } . & & \text {cor} \\$$

Where a ̂ MC is the Monte Carlo estimate for a d, SS ( α ) , ̂ se is the standard error of the Monte Carlo estimate, and p ̂ is the proportion of points that fall in the region. Thus the estimator is unbiased, and its reported standard error is the usual binomial plug-in estimate.

We evaluated 18 parameter combinations with N = 10 8 samples each, for a total of 1 . 8 × 10 9 membership tests. The parameters were α = 1 . 25 and 10 in dimensions 2, 3, 4, 5, 8, 9, 10, 12, and 20. Each run used a recorded deterministic seed. The complete results are reported in Table 1.

All 18 theoretical values lie within the corresponding two-sided normal 95% Monte Carlo intervals: the maximum absolute standardized discrepancy is 1 . 660 , and the maximum absolute relative error is 2 . 113 × 10 -4 . The largest absolute quadrature error estimate reported by the adaptive routine across these cases is 3 . 552 × 10 -11 . These results provide numerical support for the theoretical predictions.

### 7. Conclusion

We developed an arbitrary-dimensional geometric analysis for the stepping-stone diversion neighborhood. As proved in Proposition 1, similarity normalization isolates a normalized volume constant through (17).

The boundary profile is explicitly parametrized in Proposition 3. Integrating its orthogonal cross-sections then gives the one-dimensional representation (32) of Theorem 1, valid for every d ≥ 2 and every finite α &gt; 1 .

The resulting formula places three distinguished geometric regimes within a single framework. By Proposition 4, at α = 1 the neighborhood degenerates to the segment joining the defining sites, whereas at α = 2 it is the closed Gabriel ball. By Proposition 5, as α → ∞ the finite-parameter neighborhoods, after removal of their defining sites, converge from within to the open relative-neighborhood lune, and their normalized volumes converge to the relative-neighborhoodlune constant given in (50).

The strict increase of the diversion neighborhoods and their normalized volumes is established in Theorem 2. Together with continuity, this yields the calibration result of Corollary 1: the map

$$\alpha \longmapsto a _ { d , S S } ( \alpha )$$

is continuous and strictly increasing from [1 , ∞) onto [0 , a d, RNG ) . Consequently, every normalized volume strictly between the degenerate and relative-neighborhood values determines a unique finite diversion parameter.

At the graph level, Proposition 6 shows that enlargement of the diversion neighborhood reverses edge inclusion and places the stepping-stone graph family within the classical proximity-graph inclusion hierarchy. In particular, for every finite parameter value, the stepping-stone graph contains the open-lune relative-neighborhood graph and therefore contains a Euclidean minimum spanning tree. This yields connectivity for every nonempty finite point set in every ambient dimension, as stated in Corollary 3. Furthermore, Corollary 4 shows that, for every fixed finite point set, the stepping-stone graph coincides exactly with the open-lune relative-neighborhood graph once the diversion parameter exceeds a finite threshold depending on that point set. Thus the graph does not merely converge asymptotically: it eventually stabilizes exactly. As shown in Remark 2, however, no single finite threshold works uniformly over all finite point sets.


<!-- p:12 -->


For α ≥ 2 , the inclusion chain in (71) places the steppingstone graph inside the Gabriel and Delaunay graphs. In the plane and under general position, this provides a linearsize Delaunay starting graph, as used by Kannangara et al. (2018, 2019). It does not, by itself, produce a linear-time construction, because testing every initial edge against the remaining sites still gives a naive quadratic procedure. In higher dimensions, the same containment does not even guarantee a subquadratic worst-case starting set: Delaunay and Gabriel graphs can already have quadratic size in three dimensions (Agarwal and Matoušek, 1992; Chazelle et al., 1994).

The regularity verification in Proposition 7 permits the application of Devroye's theorem for graphs defined by regular sets. In particular, Corollary 5 gives the limiting conditional expected degree in (77) and the asymptotic edgecount lower bound in (78). These conclusions are applications of Devroye's tageneral results; the new input supplied here is the explicit stepping-stone volume constant in arbitrary dimension.

In the planar homogeneous Poisson setting, Proposition 8 substitutes the normalized area into Watanabe's edge-length formulation. The resulting edge-length density is given in (81). At α = 2 , it specializes to the Gabriel-graph edgelength density, whereas, as α → ∞ , it converges to relativeneighborhood-graph edge-length density.

Finally, the change of variables introduced in Proposition 9 removes the endpoint singularity and produces the stable quadrature formula (92). The calculation is implemented in the PROXIMITYGRAPHS Python package, as described in Section 6.2, and is validated numerically by the rejectionsampling experiments reported in Table 1. The rejection sampler evaluates the original defining inequality and does not use the boundary parametrization or either quadrature formula; its only additional geometric input is the proved enclosing cylinder.

The principal outcome is therefore a dimension-uniform reduction from an implicit Euclidean region to an explicit boundary profile and a computable one-dimensional volume formula. This representation simultaneously explains the special and limiting geometries, strict parameter dependence, proximity-graph inclusions, random-graph constants, and stable numerical evaluation. More broadly, this analysis motivates the study of other empty-region graph families whose pairwise regions, for each fixed parameter value, are obtained from a single normalized template by translation, rotation, and scaling. Examples include the influence regions of β -skeletons (Kirkpatrick and Radke, 1985) and the twoparameter regions defining planar γ -neighborhood graphs (Veltkamp, 1992). For such families, the normalized template provides a natural starting point for investigating the geometry and volume of the corresponding empty regions and their consequences for the associated graphs.

### CRediT authorship contribution statement

Heriberto Espino-Montelongo: Conceptualization, Methodology, Formal analysis, Investigation, Validation, Visualization, Writing - original draft. Héctor Maravillo: Investigation, Supervision, Visualization, Writing - review and editing.

### Code and data availability

No external datasets were used. The exact computational release is archived on Zenodo under DOI 10.5281/zenodo.21291269 (Espino-Montelongo and Maravillo, 2026). It contains the quadrature, Monte Carlo, and figure-generation code, outputs, random seeds, and reproduction instructions. The public GitHub repository hosts the maintained version of these materials. To complement Figure 1, the same companion provides an interactive three-dimensional visualization of the normalized diversion neighborhood; the parameter α can be varied continuously, and the region can be rotated and magnified. Two supplementary CSV files underlying Table 1 add the hit counts, acceptance rates, samplingcylinder volumes, quadrature error estimates, sample counts, and random seeds for each run.

The reusable Python implementation is available in the PROXIMITYGRAPHS package on PyPI and in its public source repository; the version used here is archived under DOI 10.5281/zenodo.21088183 (Maravillo et al., 2026).

### Declaration of competing interest

The authors declare no competing interests.

### Declaration of generative AI and AI-assisted technologies in the manuscript preparation process

During the preparation of this work, the authors used ChatGPT by OpenAI to assist with language, clarity, organization, and LaTeX formatting. After using this tool, the authors reviewed and edited the content as needed and take full responsibility for the content of the publication.

### Funding

This research did not receive any specific grant from funding agencies in the public, commercial, or not-for-profit sectors.
