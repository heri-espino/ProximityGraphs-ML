---
id: "Li_2010_Hyperspherical-Cap-Area-Volume"
source_pdf: "../pdf/Li_2010_Hyperspherical-Cap-Area-Volume.pdf"
source_filename: "Li_2010_Hyperspherical-Cap-Area-Volume.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "excellent"
extraction_score: 98.0
visual_assets: "disabled"
references_file: "../references/Li_2010_Hyperspherical-Cap-Area-Volume.references.md"
---

<!-- p:1 -->

Asian Journal of Mathematics and Statistics, 2011

ISSN 1994-5418 / DOI: 10.3923/ajms.2011.

© 2011 Asian Network for Scientific Information

## Concise Formulas for the Area and Volume of a Hyperspherical Cap

## S. Li

National Institute for Occupational Safety and Health, Health Effects Lab Division, Morgantown, WV 26505, USA

Corresponding Author: Shengqiao Li, 1095 Willowdale Road, MS 4050, Morgantown, WV 26505, USA Tel: 1.304.285.5960Fax: 1.304.285.6112

#### ABSTRACT

Spherical caps in hyperspace have found applications in stochastic optimizations and software engineering. However, there is a need for concise formulas for surface area and volume that are easy to express and compute. In this note, concise formulas are given in closed-forms. These formulas are obtained by integrating the area/volume of an (n-1)-sphere over a great circle arc in hyperspherical coordinates.

Key words: Hyperspace, hyperspherical cap, hyperspherical sector, hyperspherical cone, area, volume

#### INTRODUCTION

Let Sn be an n-hypersphere, or n-sphere for short, of radius r in n-dimensional euclidian space, that is:

$$S ^ { \mathbf e } = \left \{ x \in R ^ { n } \colon \| x \| \models \mathbf r \right \} .$$

The volume V and surface area An for the hypersphere are well known:

$$V _ { n } ( r ) = \frac { \pi ^ { n / 2 } } { \Gamma ( \frac { N } { 2 } + 1 ) } r ^ { \Gamma } ,$$

$$A _ { \mathfrak { c } } ( r ) = \frac { 2 \pi ^ { \mathfrak { a } / 2 } } { \Gamma ( \frac { n } { 2 } ) } r ^ { \mathfrak { a } - 1 } ,$$

where, Γ is the gamma function. These formulas are short and clear. But for a portion of a hypersphere, such as hyperspherical caps or sectors, there is a need for concise and simple formulas. Applications of hypershperical caps are found in spherical distributions (Ruymgaart, 1989), stochastic optimizations (Bohachevsky et al., 1992; Hughes, 2008) and information technology (Shen et al., 2005), etc. Most of the related formulas are in the form of complex finite series,

and recurrence or integrals. For instance, Jacquelin (2003) gave volume formulas for a sector and cap using finite series for even and odd n separately. Chen and He (2008) derived volume formulas in the similar form. In addition to the volume formula, they also provided a surface area formula for a hyperspherical cap. Hughes (2008) used Jacquelin's hypersector volume formula to deduce a cap area formula in the same series form. In Ericson and Zinoviev (2001) and Cox et αl. (2001, 2007), recursive formulas are given for the cap surface area. These formulas are lengthy and cumbersome in mathematical expression and hard to understand and interpret. In this note, simple formulas in closed-forms are given and appliable to any integer n, either odd or even. These formulas are based on the widely used gamma function and incomplete beta functions.


<!-- p:2 -->


Table 1: Beta and regularized incomplete beta functions in special cases

|   n | BC" ~) 2'2   | I C"~) sm'f 2'2       |
|-----|--------------|-----------------------|
|   1 | TI           | 2¢/n                  |
|   2 | 2            | l-cos¢                |
|   3 | TI/2         | (2¢-sin2¢ )/n         |
|   4 | 4/3          | 1-3/2cos¢+ 1I2cos 3 ¢ |

In this note, O≤φ≤π/2 denotes the colatitude angle, i.e., the angle between a vector of the sphere and its positive nth-axis. The integral of sinnθ will be used for the derivation. One identity with the integral is given here:

$$J _ { n } ( \phi ) & = \int _ { 0 } ^ { \phi } \sin ^ { n } \theta \ d \theta = \frac { 1 } { 2 } B \left ( \sin ^ { 2 } \phi ; \frac { n + 1 } { 2 } , \frac { 1 } { 2 } \right ) \\ & = \frac { 1 } { 2 } B \left ( \frac { n + 1 } { 2 } , \frac { 1 } { 2 } \right ) I _ { s i u ^ { 2 } \phi } \left ( \frac { n + 1 } { 2 } , \frac { 1 } { 2 } \right ) ,$$

where, B(α, β) is the beta function, B(x; α, β) is the incomplete beta function and is the regularized incomplete beta function. The last identity can be shown by changing of variable, z = sin2θ. In Table 1, some special forms are listed for B and I in lower dimensional spaces.

#### AREA OF A HYPERSPHERICAL CAP

A hypersphere can be cut into two parts, two caps, by a hyperplane. In the following, the formulas are for the smaller cap (φ≤π/2). The extension to larger caps is straight forward and thus is ignored. The area of a hyperspherical cap in a n-sphere of radius r can be obtained by integrating the surface area of an (n-1)-sphere of radius rsinθ with arc element rdθ over a great circle arc, that is:

$$^ { \circ }$$

$$A _ { s } ^ { \otimes } ( r ) & = \int _ { 0 } ^ { 0 } A _ { s - 1 } ( r \sin \theta ) r d \theta \\ & = \frac { 2 \pi ^ { ( n - 1 ) / 2 } } { \Gamma ( \frac { n - 1 } { 2 } ) } r ^ { n - 1 } \int _ { 0 } ^ { n - 2 } \sin ^ { 2 } \theta d 0$$

$$\hat { z }$$


<!-- p:3 -->


Asian J. Math. Stat., 2011

$$2 \pi ^ { ( a - 1 ) / 2 } _ { 2 }$$

$$A s i a n \, J . \, M a t h . \, S t a t , \, 2 0 1 1 \\ = \frac { 2 \pi ^ { ( a - 1 ) / 2 } } { \Gamma ( \frac { n - 1 } { 2 } ) } \Gamma ^ { n - 1 } J _ { a - 2 } ( \phi ) \\ = \frac { 2 \pi ^ { ( a - 1 ) / 2 } } { \Gamma ( \frac { n - 1 } { 2 } ) } \Gamma ^ { n - 1 } \frac { 1 } { 2 } \left ( \frac { n - 1 } { 2 } , \frac { 1 } { 2 } \right ) I _ { x + 2 } \left ( \frac { n - 1 } { 2 } , \frac { 1 } { 2 } \right ) \\ = \frac { 2 \pi ^ { ( n - 1 ) / 2 } } { 2 } \Gamma ^ { n - 1 } \frac { 1 } { 2 } \Gamma ( \frac { n - 1 } { 2 } ) \Gamma ( \frac { 1 } { 2 } ) \\ = \frac { 1 } { 2 } \frac { 2 \pi ^ { ( n - 1 ) / 2 } } { \Gamma ( \frac { n - 1 } { 2 } ) } \Gamma ^ { n - 1 } \frac { 1 } { 2 } I _ { x + 2 } \left ( \frac { n - 1 } { 2 } , \frac { 1 } { 2 } \right ) \\ = \frac { 1 } { 2 } \frac { 2 \pi ^ { n ^ { \prime \prime } } } { \Gamma ( \frac { n } { 2 } ) } \Gamma ^ { n - 1 } I _ { x + 2 } \left ( \frac { n - 1 } { 2 } , \frac { 1 } { 2 } \right ) \\ = \frac { 1 } { 2 } A _ { n } ( r ) I _ { \sin ^ { 4 } } \left ( \frac { n - 1 } { 2 } , \frac { 1 } { 2 } \right ) . \\$$

It can be shown that the surface area of a cap in a 2-sphere (a circle) is the arc length, i.e., 2φr and the surface area of a cap in a 3-sphere (a usual ball) is or 2π (1-cosφ)r2 or 2πrh, where, h = (1-cosφ) r is the cap height.

The regularized incomplete beta factor in Eq. 1 can be interpreted as the probability of a random vector on a hemisphere falling onto the cap or the cap is a set of such random vectors. Immediately, this formula provides one mechanism for randomly picking a point from a hemisphere:

- Generate u from a beta distribution with shape parameters (n-1)/2 and 1/2 ·
- Generate a random vector x-1from an (n-1)-sphere of radius r√u ·
- Then, x = {x-1, r√1-u} is a random vector from an n-dimensional hemisphere ·

#### VOLUME OF A HYPERSPHERICAL CAP

Similarly, the volume of a hyperspherical cap in an n-sphere of radius r can be obtained by integrating the volume of an (n-1)-sphere of radius rsinθ with height element drcosθ, i.e.:

$$\Theta _ { \uparrow } 0$$

$$& \text {of an } ( n - 1 ) \text {-sphere of radius } r \sin \theta \text { with height } \text {el.} \\ & \quad V _ { n } ^ { \circledast } ( r ) = \int _ { \theta _ { 1 } } V _ { \theta _ { 1 } } ( r \sin \theta ) d r \cos \theta \\ & \quad = \int _ { \theta _ { 1 } - 1 } V _ { n - 1 } ( r \sin \theta ) r \sin \theta d \theta \\ & \quad = \frac { \pi ^ { ( n - 1 ) / 3 } } { \Gamma ( - \frac { n - 1 } { 2 } + 1 ) } r ^ { n } \int _ { \sin ^ { n } \theta } \theta d \theta \\ & = \frac { \pi ^ { ( n - 1 ) / 3 } } { \Gamma ( - \frac { n - 1 } { 2 } + 1 ) } r ^ { n } J _ { \theta } ( \phi ) \\ & = \frac { \pi ^ { ( n - 1 ) / 2 } } { \Gamma ( \frac { n - 1 } { 2 } + 1 ) } r ^ { n } \frac { 1 } { 2 } B \left ( \frac { 1 + 1 } { 2 } , \frac { 1 } { 2 } \right ) I _ { \sin ^ { 3 } \theta } \left ( \frac { n + 1 } { 2 } , \frac { 1 } { 2 } \right ) \\$$


<!-- p:4 -->


Asian J. Math. Stat., 2011

$$= \frac { 1 } { 2 } \frac { \pi ^ { ( n - 1 ) / 2 } } { \Gamma ( \frac { n - 1 } { 2 } + 1 ) } \Gamma ^ { n } \frac { \Gamma ( \frac { n + 1 } { 2 } ) \Gamma ( \frac { 1 } { 2 } ) } { \Gamma ( \frac { n } { 2 } + 1 ) } 1 _ { \sin ^ { 2 } \phi } ^ { \left ( \frac { n + 1 } { 2 } , \frac { 1 } { 2 } \right ) }$$

$$= \frac { 1 } { 2 } \frac { \pi ^ { n / 2 } } { \Gamma ( \frac { \Pi } { 2 } + 1 ) } \Gamma ^ { \Pi } \sin ^ { 2 } \left ( \frac { \Pi + 1 } { 2 } , \frac { 1 } { 2 } \right ) \\$$

$$= \frac { 1 } { 2 } \, V _ { n } ( \mathbf r ) 1 _ { \mathbf i n ^ { 2 } \circ \mathbf f } \left ( \frac { \mathbf n + 1 } { 2 } , \frac { 1 } { 2 } \right ) .$$

For n = 2, V2ap(r) is the area of a circle segment, i.e., (φ-sinφcosφ)r2. For n = 3, V8ap (r) = (2/3-cosφ+1/3cos8φ)πr8. The Eq. 3 can be interpreted in the similar way as the area equation and the random number generator can be devised similarly.

#### DISCUSSION

With the area formula of a cap expressed in terms of the sphere area and the relationship between the volume of a hyperspherical sector V sector and the area of the cap, in a n-sphere of n radius r:

$$V _ { n } ^ { s e c t x f } ( r ) = \frac { A _ { \hat { n } } ^ { \text {cap} } ( r ) } { A _ { n } ( r ) } V _ { n } ( r ) ,$$

the volume of a hypersector is immediate:

$$V _ { \mathfrak { a } } ^ { s o c t o r } ( \mathbf r ) = \frac { 1 } { 2 } \, V _ { \mathfrak { n } } ( \mathbf r ) I _ { \sin ^ { \mathfrak { z } } \phi } \left ( \frac { \mathbf n - 1 } { 2 } , \frac { 1 } { 2 } \right ) .$$

Special cases are V sector(r) = φr2 and Vsector(r) = 2/3π(1 -cosφ)r3.

The volume of a hyperspherical cone Vcone is also easy to derive by the difference between the sector volume and the cap volume, V cne(r) = V sectr(r)-V cap(r) = 1/nVn-1(rsinφ)rcosφ. This shows that the volume of a cone is 1/n·volume of base·height. For n = 2 and 3, V2cone(r) = sinφcosφr2 and V cne(r) = π/3sin2φcosφr8.

The regularized incomplete beta function is widely available in scientific software packages such as the betainc function in MATLAB, the pbeta function (the cumulative density function for beta distribution) in R (http://www.r-project.org) and the gsl\_sf\_beta\_inc function in gsl library (http://www.gnu.org/software/gslI).

In summary, the area and volume formulas for a hyperspherical cap provided in this note are concise, easy to understand and compute.

#### ACKNOWLEDGMENTS

The author would like to thank Michael E. Andrew and Robert Mnatsakanov for their thoughtful discussion. The findings and conclusions in this report are those of the author(s) and do not necessarily represent the views of the National Institute for Occupational Safety and Health.


<!-- p:5 -->

### Asian J. Math. Stat., 2011
