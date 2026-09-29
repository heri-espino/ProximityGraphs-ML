---
id: "Karp-Pinsky_1989_Small-Extrinsic-Ball-Submanifold"
source_pdf: "../pdf/Karp-Pinsky_1989_Small-Extrinsic-Ball-Submanifold.pdf"
source_filename: "Karp-Pinsky_1989_Small-Extrinsic-Ball-Submanifold.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "full-page-ocr"
extraction_quality: "excellent"
extraction_score: 98.0
visual_assets: "disabled"
references_file: "../references/Karp-Pinsky_1989_Small-Extrinsic-Ball-Submanifold.references.md"
---

<!-- p:1 -->

## VOLUME OF A SMALL EXTRINSIC BALL IN A SUBMANIFOLD

#### LEON KARP AND MARK PINSKY

## ABSTRACT

For a submanifold M  R, we determine a two-term asymptotic formula for vol(M ∩ Be(x)) for xe Mo as ε ↓0. The second term is a quadratic curvature invariant of the second fundamental form of the imbedding. Imbedded spheres are characterized among compact hypersurfaces by this term.

## 1. Introduction

In recent years there have been a number of works dealing with asymptotic results in differential geometry in which curvature invariants appear as coefficients in the expansions. Historically the first such formula is due to Bertrand, Diguet and Puiseux [1], who expressed the area of a non-Euclidean disk in terms of the curvature, to first order when the radius of the disk tends to zero. This formula was later generalized to geodesic balls in arbitrary Riemannian manifolds by Cartan [2] with subsequent Pa yed ae ] e    [ e  yal characterizations of Euclidean space and other model spaces in terms of the volume of small geodesic balls.

In order to obtain more effective characterizations of Euclidean space and other model spaces, several papers have been devoted to the mean exit time of Brownian motion [4, 6, 8]. The asymptotic formulas for the mean exit time involve new quadratic curvature invariants. In the case of the mean exit time from a tubular neighborhood, one obtains a quadratic form in the principal curvatures whose lowest ee e r  e s  e s e is  dsic balls of an immersed manifold, the mean exit time is expressed in terms of the mean curvature, to the first order of asymptotics. This leads to a characterization of minimal hypersurfaces in terms of the mean exit time of Brownian motion.

In this paper we consider a submanifold of R" and its intersection with a small ball of R". The volume of the resulting intersection is computed in the asymptotic limit of radius tending to zero. This leads to a new asymptotic formula for the volume, in which appears a quadratic form which generalizes that obtained in studying the mean exit time of Brownian motion from a tubular neighborhood of a hypersurface ([6, Theorem 11]). In Section 3 we obtain some characterizations of spheres and totally geodesic imbeddings by means of the volume.


<!-- p:2 -->


## 2. Statement and solution of problem

Let M be a p-dimensional submanifold of R~. For x0∈ M" we consider the intersection Mp(x) of M with the ambient space ball

$$B _ { t } ( x _ { 0 } ) = \{ y \in \mathbb { R } ^ { N } \colon | y - x _ { 0 } | < \varepsilon \}$$

or equivalently M(x0) = M ∩ B(x0). The asymptotics of the volume of M(x0) as ε↓0 are governed by the extrinsic curvatures of Mo as derived from the second fundamental form B, which is defined by the relation

$$B _ { x _ { 0 } } ( v , w ) = ( \nabla _ { v } W ) ^ { \perp } \ v , w \in T _ { x _ { 0 } } M , \\$$

where V and W are smooth extensions of v and w respectively, ∇ is the standard LeviCivita connection of Euclidean space R~ and ⊥ denotes the component normal to Tx M. The mean curvature normal is the vector

$$H _ { x _ { 0 } } = \text {trace} \, B _ { x _ { 0 } } = \sum _ { t = 1 } ^ { p } \, B _ { x _ { 0 } } ( e _ { 4 } , e _ { 4 } )$$

where {e} is an orthonormal frame for Tx, M; note that we have not divided by the dimension of M. Finally ∥H∥ denotes the length of H and ∥B∥ denotes the standard Hilbert-Schmidt norm of B:∥B|2 = ∑ ∥|B(e, e), with {e} as above. If M" is a hypersurface in Rn+1 with principal curvatures {λ} then ∥B|2 = ∑λ2 and H∥2 = (∑λi)2.

For background concerning B, consult [7].

Having formulated these preliminaries, we can state the main result.

THEOREM. The volume of the extrinsic neighborhood M(x) has the asymptotic behavior when ε↓0:

$$\ v o l ( M _ { \varepsilon } ^ { p } ( x ) ) = ( \sigma _ { p - 1 } \varepsilon ^ { p } / p ) + ( \sigma _ { p - 1 } / 8 p ( p + 2 ) ) \left \{ 2 \left \| B \right \| _ { \varepsilon } ^ { 2 } - \left \| H \right \| _ { x } ^ { 2 } \right \} \varepsilon ^ { p + 2 } + O ( e ^ { p + 3 } )$$

where σp-1 is the surface measure of the unit sphere in RP.

Proof. We consider the imbedded p-dimensional submanifold M ∈ R~ to be defined in a local representation by the smooth functions

$$x _ { \rho + 1 } = \psi _ { 1 } ( x ) , \dots , x _ { N } = \psi _ { q } ( x )$$

with x = (x1, ..., xp) being local coordinates in the tangent space TM at x0∈M, x0 = (0, ..., 0) and q = N−p, the codimension of MP. We have

$$M _ { \varepsilon } ^ { p } = \{ ( x _ { 1 } , \dots , x _ { N } ) \colon \sum _ { \iota = 1 } ^ { N } x _ { \iota } ^ { 2 } \leqslant \varepsilon ^ { 2 } , ( x _ { 1 } , \dots , x _ { N } ) \in M ^ { p } \} .$$

Let X(u) = (u, ψ1(u), .., ψq(u)). Then Mp is the diffeomorphic image of the region De =: {u∈ R:|X(u)|2 ≤ ε2}. The functions ψa may be written in the form

$$\psi _ { \alpha } ( x ) = \frac { 1 } { 2 } \sum _ { \iota , j } A _ { \alpha } ^ { \iota } x _ { k } x _ { \iota } + O ( | x | ^ { 3 } ) \quad ( | x | \to 0 )$$

where Aki is is symmetric in the upper indices. The volume is written as

$$v o l \left ( M _ { \varepsilon } ^ { p } \right ) = \int _ { D _ { \varepsilon } } \sqrt { g } \, d u \ \ g = \det \left ( g _ { \varepsilon } \right )$$


<!-- p:3 -->


where (g) may be computed as

$$VOLUME OF A SMALL EXTRINISTIC BALL IN A SUBMANIFOLD \\ \text {where } ( g _ { t } ) \text { may be computed as} \\ g _ { t } & = X _ { t } X _ { t } \\ & = \delta _ { t } + \sum _ { \alpha } \psi _ { t } \psi _ { \alpha } \quad ( \psi _ { t } = ( \partial \psi _ { t } / \partial u _ { t } ) ) \\ & = \delta _ { t } + \frac { 1 } { 4 } \sum _ { \substack { \text {akimn} \\ \text { } } } [ A _ { \alpha } ^ { k } ( \delta _ { k t } x _ { t } + \delta _ { u } x _ { t } ) ] [ A _ { \alpha } ^ { m } ( \delta _ { m } x _ { n } + \delta _ { j n } x _ { m } ) ] + O ( | x | ^ { 3 } ) \\ & = \delta _ { t } + \frac { 1 } { 4 } \sum _ { \alpha } \{ \sum _ { l } A _ { \alpha } ^ { u } x _ { l } + \sum _ { k } A _ { \alpha } ^ { k } x _ { k } \} \{ \sum _ { m } A _ { \alpha } ^ { j m } x _ { m } + A _ { \alpha } ^ { m } x _ { n } \} + O ( | x | ^ { 3 } ) \\ & = \delta _ { u } + \sum _ { \alpha } ( \sum _ { l } A _ { \alpha } ^ { u } x _ { l } ) ( \sum _ { k } A _ { \alpha } ^ { \mu } x _ { k } ) + O ( | x | ^ { 3 } ) \\ & = \delta _ { u } + \sum _ { \alpha } \sum _ { k l } B _ { x _ { l } } ^ { k l } x _ { k } x _ { l } + O ( | x | ^ { 3 } ) \\ & = \delta _ { u } + \sum _ { \alpha } B _ { x _ { d } } ( \xi ) ) \, r ^ { 2 } + O ( | x | ^ { 3 } ) \\ \text {where} \\ & \quad B _ { k l } ^ { k l } = A _ { \alpha } ^ { u } A _ { k } ^ { j k } \text { and } B _ { x _ { l } } ( \xi ) = \sum _ { \alpha } B _ { k l } ^ { k l } \xi _ { \xi } \xi _ { \xi } \\$$

where

Thus

$$B _ { \alpha \bar { f } } ^ { k l } = A _ { \alpha } ^ { u } A _ { \alpha } ^ { j k } \text { and } B _ { \alpha \bar { f } } ( \xi ) = \sum _ { k l } B _ { \alpha \bar { f } } ^ { k l } \xi _ { k } \xi _ { l } . \\ \quad \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \$$

Now the boundary ∂De is defined by ∂D, = {u:|X(u)|2 = ε2}, or

$$v ^ { 2 } & = r ^ { 2 } + \sum _ { \alpha } \psi _ { \alpha } ( u ) ^ { 2 } \\ & = r ^ { 2 } + \frac { 1 } { 4 } \sum _ { \alpha } \left ( ( \sum _ { 6 } A _ { \alpha } ^ { 6 } \xi _ { t } \xi _ { 1 } ) r ^ { 2 } + O ( r ^ { 3 } ) \right ) ^ { 2 } \\ & = r ^ { 2 } + \frac { 1 } { 4 } Q r ^ { 4 } + O ( r ^ { 5 } )$$

where Q =: ∑a (Σt A ξt ξ,)2. Solving this quadratic equation for r2 yields

and

Consequently,

$$C o n s e q u e n t y , \\ \quad & v o l ( M _ { e } ^ { p } ) = \iint _ { D _ { e } } \sqrt { g } \, d u \\ & = \int _ { S ^ { p - 1 } } d \xi \, \int _ { 0 } ^ { \pi _ { e } ( \xi ) } [ 1 + \frac { 1 } { 2 } \sum _ { \mathfrak { A } _ { d } ( \xi ) } B _ { d } ( \xi ) \, r ^ { 2 } + O ( r ^ { 3 } ) ] | r ^ { p - 1 } d r \\ & = \int _ { S ^ { p - 1 } } d \xi \, \int _ { 0 } ^ { \pi _ { e } ( \xi ) } [ r ^ { p - 1 } + \frac { 1 } { 2 } \sum _ { \mathfrak { A } _ { d } ( \xi ) } \mathring { A } _ { d } ( \xi ) \, r ^ { p + 1 } + O ( r ^ { p + 2 } ) ] \, d r \\ & = I + \Pi I + O ( r ^ { p + 3 } ) ,$$

$$\sum _ { \alpha } ( \sum _ { \tilde { \alpha } } A _ { \alpha } ^ { 2 } \varsigma _ { \tilde { \alpha } } \varsigma _ { \tilde { \alpha } } ) \cdot & \text {.} \, \text {Sovling this quadratic equation for } \Gamma ^ { 2 } \gamma \\ r ^ { 2 } & = ( - 1 + \sqrt { ( 1 - 4 ( \frac { 1 } { 4 } Q ) ) ( ( O r ^ { 5 } ) - \varepsilon ^ { 2 } ) ) / 2 ( \frac { 1 } { 4 } Q ) } \\ & = ( - 1 + \sqrt { ( 1 + Q \varepsilon ^ { 2 } + O ( \varepsilon ^ { 5 } ) ) ) / \frac { 1 } { 2 } Q } \\ & = ( - 1 + ( 1 + \frac { 1 } { 2 } Q \varepsilon ^ { 2 } - \frac { 1 } { 8 } Q ^ { 2 } \varepsilon ^ { 4 } + O ( \varepsilon ^ { 5 } ) ) ) / \frac { 1 } { 2 } Q \\ & = \varepsilon ^ { 2 } - \frac { 1 } { 4 } Q \varepsilon ^ { 4 } + O ( \varepsilon ^ { 5 } ) \\ r & = \varepsilon ( 1 - \frac { 1 } { 8 } Q \varepsilon ^ { 2 } + O ( \varepsilon ^ { 3 } ) ) \\ & = \varepsilon - \frac { 1 } { 8 } Q \varepsilon ^ { 3 } + O ( \varepsilon ^ { 4 } ) = \colon h _ { s } ( \xi ) .$$

$$= \varepsilon - \frac { 1 } { 8 } Q \varepsilon ^ { 3 } + O ( \varepsilon ^ { 4 } ) = \colon h _ { _ { \varepsilon } } ( \xi ) .$$


<!-- p:4 -->


where

Therefore

$$\ v o l ( M _ { \varepsilon } ^ { p } ) & = ( \sigma _ { p - 1 } / p ) \varepsilon ^ { p } + \frac { 1 } { 2 } \varepsilon ^ { p + 2 } \left \{ ( p + 2 ) ^ { - 1 } \sum _ { \varepsilon } \int _ { S ^ { p - 1 } } B _ { \varepsilon t } ( \xi ) \, d \xi - \frac { 1 } { 4 } \int _ { S ^ { p - 1 } } Q \right \} + O ( \varepsilon ^ { p + 2 } ) . \\ \intertext { w o l } \text {Now}$$

Now

$$\int _ { S ^ { p - 1 } } B _ { x i } ( \xi ) \, d \xi = \int _ { S ^ { p - 1 } \ k i } \sum _ { k } \, B _ { x i } ^ { k l } \, \xi _ { k } \, \xi _ { l } \, d \xi = ( \sigma _ { p - 1 } / p ) \, \sum _ { k } \, B _ { x i } ^ { k k } ,$$

so that

$$\frac { 1 } { p + 2 } \sum _ { \alpha } \int _ { S ^ { p - 1 } } B _ { \alpha \alpha } ( \xi ) \, d \xi = \frac { \sigma _ { p - 1 } } { p ( p + 2 ) } \sum _ { \alpha k } ( A _ { \alpha } ^ { u k } ) ^ { 2 } .$$

Now we make use of the identities ∫ξi ξi dξ = σp-1/p(p + 2) for i-j non-zero and ∫ ξ4 dξ = 3σp−1/p(p + 2) while ∫ H(ξ) dξ = 0 for all other homogeneous polynomials H of degree 4. This yields

$$\text {This yields} \\ \int _ { S ^ { p - 1 } } Q = \sum _ { \alpha } \int _ { S ^ { p - 1 } } \{ \sum _ { i j } A _ { \alpha } ^ { i j } \xi _ { i } \xi _ { j } \} ^ { 2 } d \xi \\ = \sum _ { \alpha } \int _ { S ^ { p - 1 } } \sum _ { i j k l } \left ( A _ { \alpha } ^ { i j } \xi _ { i } \xi _ { j } A _ { \alpha } ^ { k l } \xi _ { k } \xi _ { i } \right ) d \xi \\ = \sum _ { \alpha } \int _ { S ^ { p - 1 } } \{ \sum _ { i } A _ { \alpha } ^ { i j } A _ { \alpha } ^ { k l } \xi _ { i } \xi _ { j } \xi _ { k } \xi _ { i } \} d \xi . \\ = \frac { 2 \sigma _ { p - 1 } } { p ( p + 2 ) } \sum _ { \alpha } \left ( \sum _ { i j } ( A _ { \alpha } ^ { i j } ) ^ { 2 } + \frac { 1 } { 2 } \sum _ { i } A _ { \alpha } ^ { i j } \right ) . \\ \intertext { s e n c a l } \text {these and substituting in the formula for volume, we have}$$

Combining these and substituting in the formula for volume, we have

$$\ v o l \left ( M _ { \ell } ^ { p } \right ) = \frac { \varepsilon ^ { p } \sigma _ { p - 1 } } { p } + \frac { \sigma _ { p - 1 } \varepsilon ^ { p + 2 } } { 8 p ( p + 2 ) } \left \{ 2 \sum _ { \alpha } \left ( A _ { \alpha } ^ { t } \right ) ^ { 2 } - \sum _ { \alpha } \left ( \sum _ { t } A _ { \alpha } ^ { t } \right ) ^ { 2 } \right \} + O ( \varepsilon ^ { p + 3 } ) \\$$

where σp-1 is the surface area of Sp-1. This completes the proof. In fact, it is a simple matter to check that, since the frame {∂/∂u{} is orthonormal at u = 0, = (Hess ψ)o, ∥B|2 = ∑ (∂2ψa/∂x, ∂x,)(0), etc.

## 3. Consequences of the Theorem

As a corollary of the above expansion theorem, we can characterize certain manifolds by the volume growth of extrinsic balls, when the radius tends to zero. We first consider the case of surfaces in R3.

$$LEON KARP AND MARK PINSKY \\ I = \colon \int _ { S ^ { p - 1 } } d \xi \int _ { 0 } ^ { h _ { ( \ell ) } ( \ell ) } r ^ { p - 1 } d r = ( 1 / p ) \int _ { S ^ { p - 1 } } h _ { \ell } ( \xi ) ^ { p } \\ = ( 1 / p ) \int _ { S ^ { p - 1 } } d \xi [ 1 - \frac { 1 } { 8 } p Q \varepsilon ^ { 2 } + O ( \varepsilon ^ { 3 } ) ] \varepsilon ^ { p } \\ = ( \sigma _ { p - 1 } / p ) \varepsilon ^ { p } - \frac { 1 } { 8 } \left [ \int _ { S ^ { p - 1 } } Q \, d \xi \right ] \varepsilon ^ { p + 2 } + O ( \varepsilon ^ { p + 2 } ) , \\ \Pi = \colon \frac { 1 } { 2 } \int _ { S ^ { p - 1 } } d \xi \int _ { 0 } ^ { \aleph ( \xi ) } \sum _ { \aleph } B _ { \aleph ( \xi ) } ( \xi ) \, r ^ { p + 1 } \, d r \\ = \frac { 1 } { 2 } \int _ { S ^ { p - 1 } } d \xi \{ \sum _ { \aleph } B _ { \aleph t } ( \xi ) \} \varepsilon ^ { p + 2 } / ( p + 2 ) + O ( \varepsilon ^ { p + 3 } ) . \\ \intertext { o r e } ( M ( \beta ) = ( \sigma _ { p - 1 } , \aleph _ { t } ) , \aleph _ { 0 } + 2 \left \{ ( \varepsilon _ { 0 } , \varepsilon ) - 1 \sum _ { \aleph } \int _ { \Omega } R _ { \aleph } ( \xi ) , \varepsilon ^ { 1 } \ \int _ { \Omega } \left ( \Omega \right ) \right )$$


<!-- p:5 -->


PROPOsITION 3.1. If M2 is a compact surface in R3, then vol (M2(x)) ≥ πε2 + O(ε5) for all points x∈ M as ε↓0. Strict inequality obtains for at least one x unless M2 is a standard sphere (if M is compact) or a plane (if M is non-compact). In either of these exceptional cases, vol(M2(x)) = πε2 for all x (and ε small enough if M is compact).

Proof. For p = 2 and N = 3 we have

$$2 \| B \| ^ { 2 } - \| H \| ^ { 2 } = 2 \sum _ { t = 1 } ^ { 2 } \lambda _ { t } ^ { 2 } - \left ( \sum _ { t = 1 } ^ { 2 } \lambda _ { t } \right ) ^ { 2 } = ( \lambda _ { 1 } - \lambda _ { 2 } ) ^ { 2 } \geqslant 0 .$$

This gives the stated inequality for vol M2(x). If equality is obtained, then M2 is umbilic and hence a sphere if compact and a plane if non-compact. The equality vol (M2(x)) = πe2 is obvious for the plane; for the sphere of radius r,

$$M _ { \varepsilon } ^ { 2 } ( x ) = \{ x ^ { \prime } \in M ^ { 2 } ; | x - x ^ { \prime } | \leqslant \varepsilon \}$$

corresponds to a region 0 ≤ φ ≤ φ*, 0 ≤ θ ≤ 2π, and ρ = r, in spherical coordinates (ρ, θ, φ). A short calculation shows that 2 —2r2 cos φ* = ε2, so that vol (M2(x)) = πε2. For n = dim M &gt; 2 we have the following analogue.

PRoposirioN 3.2. Let M" be a hypersurface in Rn+1with scalar curvature function K. Then for each x∈ M",

$$\ v o l ( M _ { \varepsilon } ^ { n } ( x ) ) \geqslant \omega _ { \varepsilon } \varepsilon ^ { n } - [ \omega _ { \varepsilon } ( n - 2 ) / 4 ( n + 2 ) \left ( n - 1 \right ) ] \, K ( x ) \, \varepsilon ^ { n + 2 } + O ( \varepsilon ^ { n + 3 } ) ) .$$

Strict inequality obtains for at least one point x or Mn is umbilic. Consequently, if K ≡ n(n- 1)/2R2 (the scalar curvature of SR) and Mn is compact with

$$\ v o l { M } _ { \varepsilon } ^ { n } ( x ) = \omega _ { n } \varepsilon ^ { n } - \omega _ { n } [ ( n - 2 ) / 8 ( n + 2 ) ] [ n ( n + 1 ) / R ^ { 2 } ] \varepsilon ^ { n + 2 } + O ( \varepsilon ^ { n + 3 } ) ,$$

then Mn is a standard sphere of radius R. Similarly, if K(x) ≤0 for all x then vol t  t l t o s s i (e +    (x is a hyperplane in which case vol (M(x) = ωn ε" for all x.

Proof. The principal curvatures {λ} satisfy the identity

$$\sum ( \lambda _ { i } - \lambda _ { i } ) ^ { 2 } = ( n - 1 ) \, [ 2 \sum \lambda _ { i } ^ { 2 } - ( \sum \lambda _ { i } ) ^ { 2 } ] + 2 ( n - 2 ) \, K .$$

This yields the stated inequalities when combined with the volume expansion theorem, and equality entails ∑ (λ— λ)2 = 0, so that M" is umbilic and hence a sphere.

REMARK. See [6, p. 135] for similar results for the mean exit time.

As a final note, we have:

PROPosITiON 3.3. If Mo is a minimal submanifold of RTM, then for each x∈ M, we have

$$\ v o l ( M _ { t } ^ { p } ( x ) \geqslant \omega _ { p } \varepsilon ^ { p } + \omega _ { p } \left \| B \right \| ^ { 2 } \varepsilon ^ { p + 2 } / 8 ( p + 2 ) + O ( \varepsilon ^ { p + 3 } ) .$$

Consequently, if for each x

$$\ v o l M _ { \varepsilon } ^ { p } ( x ) \leqslant \omega _ { p } \varepsilon ^ { p } + O ( \varepsilon ^ { p + 3 } ) \ \ ( \varepsilon \downarrow 0 )$$

then Mo is a p-dimensional plane in R+1.


<!-- p:6 -->


The proof is immediate. We note that the inequality

vol(Mp(x)) ≥ ωp ε (M minimal)

follows from the monotonicity theorem for minimal submanifolds (cf. [9, p. 68; 10, p. 32].

ACKNOwLEDGEMENT. We would like to thank Carl Mueller for bringing this problem to our attention.

ReMARK. It is not difficult to extend the main result mutatis mutandis to submanifolds Mo of an arbitrary Riemannian manifold N. The proof would use normal coordinates in N in place of u and would involve the expansion of the metric tensor in normal coordinates. The coefficient of εn+o then also involves the curvature of N. We leave the details to the interested reader as an exercise.
