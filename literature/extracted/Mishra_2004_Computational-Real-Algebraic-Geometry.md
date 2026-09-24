---
id: "Mishra_2004_Computational-Real-Algebraic-Geometry"
source_pdf: "../pdf/Mishra_2004_Computational-Real-Algebraic-Geometry.pdf"
source_filename: "Mishra_2004_Computational-Real-Algebraic-Geometry.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "full-page-ocr"
extraction_quality: "good"
extraction_score: 95.9
visual_assets: "disabled"
references_file: "../references/Mishra_2004_Computational-Real-Algebraic-Geometry.references.md"
---

<!-- p:1 -->

## 33 COMPUTATIONAL

### REAL ALGEBRAIC GEOMETRY

Bhubaneswar Mishra

### INTRODUCTION

Computational real algebraic geometry studies various algorithmic questions dealing with the real solutions of a system of equalities, inequalities, and inequations of polynomials over the real numbers. This emerging field is largely motivated by the power and elegance with which it solves a broad and general class of problems arising in robotics, vision, computer-aided design, geometric theorem proving, etc.

The algorithmic problems that arise in this context are formulated as decision problems for the first-order theory of reals and the related problems of quantifier elimination (Section 33.1). The associated geometric structures are then examined via an exploration of the semialgebraic sets (Section 33.2). Algorithmic problems for semialgebraic sets are considered next. In particular, Section 33.3 discusses real algebraic numbers and their representation, relying on such classical theorems as Sturm's theorem and Thom's lemma (Section 33.3). This discussion is followed by a description of semialgebraic sets using the concept of cylindrical algebraic decomposition (CAD) in both one and higher dimensions (Sections 33.4 and 33.5). This leads to brief descriptions of two algorithmic approaches for the decision and quantifier elimination problems (Section 33.6): namely, Collins's algorithm based on CAD, and some more recent approaches based on critical points techniques and on reducing the multivariate problem to easier univariate problems. These new approaches rely on the work of several groups of researchers: Grigor'ev and Vorobjov [Gri88, GV88], Canny [Can88a, Can90], Heintz et al. [HRS90], Renegar [Ren91, Ren92a, Ren92b, Ren92c], and Basu et al. [BPR96]. A few representative applications of computational algebra conclude this chapter (Section 33.7).

### 33.1 FIRST-ORDER THEORY OF REALS

The decision problem for the first-order theory of reals is to determine if a Tarski sentence in the first-order theory of reals is true or false. The quantifier elimination problem is to determine if there is a logically equivalent quantifier-free formula for an arbitrary Tarski formula in the first-order theory of reals. As a result of Tarski's work, we have the following theorem.

###### THEOREM 33.1.1 [Tar51]

- Let Ψ be a Tarski sentence. There is an effective decision procedure for Ψ. ■
- ■ Let Ψ be a Tarski formula. There is a quantifier-free formula φ logically equiv-


<!-- p:2 -->


alent to Ψ. If Ψ involves only polynomials with rational coefficients, then so does the sentence φ.

Tarski formulas are formulas in a first-order language (defined by Tarski in 1930 [Tar51]) constructed from equalities, inequalities, and inequations of polynomials over the reals. Such formulas may be constructed by introducing logical connectives and universal and existential quantifiers to the atomic formulas. Tarski sentences are Tarski formulas in which all variables are bound by quantification.

#### GLOSSARY

- Term: A constant, variable, or term combining two terms by an arithmetic operator: {+, -, ·, /}. A constant is a real number. A variable assumes a real number as its value. A term contains finitely many such algebraic variables: x1, x2, . . . , xn·
- Atomic formula: A formula comparing two terms by a binary relational operator: {=, ≠, &gt;, &lt;, ≥, ≤}.
- Quantifier-free formula: An atomic formula, a negation of a quantifier-free formula given by the unary Boolean connective {¬}, or a formula combining two quantifier-free formulas by a binary Boolean connective: {⇒, ∧, V}. Example: The formula (x2 − 2 = 0) ∧ (x &gt; 0) defines the (real algebraic) number +√2.
- Tarski formula: If φ(y1, ..., yr) is a quantifier-free formula, then it is also a Tarski formula. All the variables yi are free in φ. Let Φ(y1, .. ., yr) and Ψ(z1, . . ., zs) be two Tarski formulas (with free variables yi and zi, respectively); then a formula combining Φ and Ψ by a Boolean connective is a Tarski formula with free variables {yi} ∪ {zi}. Lastly, if Q stands for a quantifier (either universal ∀ or existential ∃) and if Φ(y1, . . . , yr, x) is a Tarski formula (with free variables x and y), then

$$\left ( \mathcal { Q } _ { \ } x \right ) \left [ \Phi ( y _ { 1 } , \dots , y _ { r } , x ) \right ]$$

is a Tarski formula with only the y's as free variables. The variable x is bound in (Q x)[Φ].

Tarski sentence: A Tarski formula with no free variable.

Example: (∃ x) (∀ y) [y2 − x &lt; 0]. This Tarski sentence is false.

Prenex Tarski formula: A Tarski formula of the form

$$\left ( \mathcal { Q } \, x _ { 1 } \right ) \left ( \mathcal { Q } \, x _ { 2 } \right ) \cdots \left ( \mathcal { Q } \, x _ { n } \right ) \left [ \phi ( y _ { 1 } , y _ { 2 } , \dots , y _ { r } , x _ { 1 } , \dots , x _ { n } ) \right ] ,$$

where φ is quantifier-free. The string of quantifiers (Q x1) (Q x2) ·· · (Q xn) is called the prefix and φ is called the matrix.

- Prenex form of a Tarski formula, Ψ: A prenex Tarski formula logically equivalent to Ψ. For every Tarski formula, one can find its prenex form using a simple procedure that works in four steps: (1) eliminate redundant quantifiers; (2) rename variables so that the same variable does not occur as free and bound; (3) move negations inward; and finally, (4) push quantifiers to the left.
- Extension of a Tarski formula, Φ(y1, . . . , yr) with free variables {y1, . . . , yr}: The set of all 〈ζ1, . . . , ζr〉 ∈ Rr such that

$$\Phi ( \zeta _ { 1 } , \dots , \zeta _ { r } ) = \text {True} .$$


<!-- p:3 -->


#### THE DECISION PROBLEM

The general decision problem for the first-order theory of reals is to determine if a given Tarski sentence is true or false. A particularly interesting special case of the problem is when all the quantifiers are existential. We refer to the decision problem in this case as the existential problem for the first-order theory of reals.

The general decision problem was shown to be decidable by Tarski [Tar51]. However, the complexity of Tarski's original algorithm could only be given by a very rapidly growing function of the input size (e.g., a function that could not be expressed as a bounded tower of exponents of the input size). The first algorithm with substantial improvement over Tarski's algorithm was due to Collins [Col75]; it has a doubly-exponential time complexity in the number of variables appearing in the sentence. Further improvements have been made by a number of researchers (Grigor'ev-Vorobjov [Gri88, GV88], Canny [Can88b, Can93], Heintz et al. [HRS89, HRS90], Renegar [Ren92a,b,c]) and most recently by Basu et al. [BPR98].

In the following, we assume that our Tarski sentence is presented in its prenex form:

$$( \mathcal { Q } _ { 1 } x ^ { [ 1 ] } ) \left ( \mathcal { Q } _ { 2 } x ^ { [ 2 ] } \right ) \cdots ( \mathcal { Q } _ { \omega } x ^ { [ \omega ] } ) \left [ \psi ( x ^ { [ 1 ] } , \dots , x ^ { [ \omega ] } ) \right ] ,$$

where the Qi's form a sequence of alternating quantifiers (i.e., ∀ or ∃, with every pair of consecutive quantifiers distinct), with x[i] a partition of the variables

$$\bigcup _ { i = 0 } ^ { \omega } x ^ { [ i ] } = \{ x _ { 1 } , x _ { 2 } , \dots , x _ { n } \} \stackrel { \triangle } { = } x , \ \text { and } \ | x ^ { [ i ] } | = n _ { i } ,$$

and where ψ is a quantifier-free formula with atomic predicates consisting of polynomial equalities and inequalities of the form

$$g _ { i } \left ( x ^ { [ 1 ] } , \dots , x ^ { [ \omega ] } \right ) \geqslant 0 , \ \ i = 1 , \dots , m .$$

Here, gi is a multivariate polynomial (over R or Q, as the case may be) of total degree bounded by d. There are a total of m such polynomials. The special case ω = 1 reduces the problem to that of the existential problem for the first-order theory of reals.

If the polynomials of the basic equalities, inequalities, inequations, etc., are over the rationals, then we assume that their coefficients can be stored with at most L bits. Thus the arithmetic complexity can be described in terms of n, ni, ω, m, and d, and the bit complexity will involve L as well.

Table 33.1.1 highlights a representative set of known bit-complexity results for the decision problem.

#### QUANTIFIER ELIMINATION PROBLEM

Formally, given a Tarski formula of the form,

$$\Psi ( x ^ { [ 0 ] } ) = ( \mathcal { Q } _ { 1 } x ^ { [ 1 ] } ) \left ( \mathcal { Q } _ { 2 } x ^ { [ 2 ] } \right ) \cdots \left ( \mathcal { Q } _ { \omega } x ^ { [ \omega ] } \right ) [ \psi ( x ^ { [ 0 ] } , x ^ { [ 1 ] } , \dots , x ^ { [ \omega ] } ) ] ,$$

where ψ is a quantifier-free formula, the quantifier elimination problem is to construct another quantifier-free formula, φ(x[0]), such that φ(x[0]) holds if and only if Ψ(x[o]) holds. Such a quantifier-free formula takes the form


<!-- p:4 -->


TABLE 33.1.1 Selected time complexity results.

| BZBXBXCABT CA BXCGCBCCBXCCBT                                                                                                 | CCBX BVBXCGCCCH                                                                                                                                                                                                                                                                                                                                                                                                      | CBCDCABVBX                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| BZCTD2CTD6CPD0 BXDCCXD7D8CTD2D8CXCPD0 BZCTD2CTD6CPD0 BXDCCXD7D8CTD2D8CXCPD0 BZCTD2CTD6CPD0 BXDCCXD7D8CTD2D8CXCPD0 BZCTD2CTD6CPD0 B4 |  BF B4 D1CS B5 BE  B4A6 D2 CX B5   B4BDB5 B4 D1CS B5  B4 D2 BE B5   B4BDB5 B4 D1CS B5 B4  B4  D2 CX B5B5 BG AX A0 BE  BDB7 D3 B4BDB5 B4 D1 B5 B4 D2 B7BDB5 B4 CS B5  B4 D2 BE B5 B4  D0D3CV  D0D3CV D0D3CV  B5B4 D1CS B5 B4BE  B4 AX B5 B5A5 D2 CX B4  D0D3CV  D0D3CV D0D3CV  B5 D1 B4 D1BPD2 B5 D2 B4 CS B5  B4 D2 B5  D0D3CV  D0D3CV D0D3CV  B5B4 D1 B5 A5B4 D2 CX B7BDB5 B4 CS B5 A5  B4 D2 CX B5 | CJBVD3D0BJBHCL CJBZCEBLBECL CJBZD6CXBKBKCL CJBVCPD2BKBKCQB8 BVCPD2BLBFCL CJCACTD2BLBECPB8CQB8CRCL CJBUCABLBICL CJBUCABLBICL |

$$\phi ( x ^ { [ 0 ] } ) \equiv \bigvee _ { i = 1 } ^ { I } \bigwedge _ { j = 1 } ^ { J _ { i } } \left ( f _ { i , j } ( x ^ { [ 0 ] } ) \stackrel { \geqslant 0 } { \equiv } 0 \right ) ,$$

where fi,j ∈ R[x[o]] is a multivariate polynomial with real coefficients.

Significantly improved bounds were given by Basu et al. [BPR96] and are summarized as follows:

$$\begin{array} { r c l } I & \leq & ( m ) \Pi ^ { ( n _ { i } + 1 ) } ( d ) \Pi ^ { O ( n _ { i } ) } \\ J _ { i } & \leq & ( m ) \Pi _ { i > 0 } ^ { ( n _ { i } + 1 ) } ( d ) \Pi _ { i > 0 } ^ { \ } O ( n _ { i } ) . \end{array}$$

The total degrees of the polynomials fi,j(x[o]) are bounded by

$$( d ) \Pi _ { i > 0 } O ( n _ { i } ) .$$

Nonetheless, comparing the above bounds to the bounds obtained in semilinear geometry, it appears that the "combinatorial part" of the complexity of both the formula and the computation could be improved to (m)Πi&gt;o(n+1). As a conseuue oe s ne ne  e t n ene oe set e onos oe enh equivalent quantifier-free formula is now

$$I , J _ { i } \leq ( m ) \Pi _ { i > 0 } ( n _ { i } + 1 ) _ { ( d ) ^ { n _ { 0 } ^ { \prime } } } \prod _ { i > 0 } O ( n _ { i } ) ,$$

where n′ = min(no, τ ∏i&gt;0(ni+ 1)) and τ is a bound on the number of free variables occurring in any polynomial in the original Tarski formula. The total degrees of the polynomials fi,j(x[0]) are still bounded by

$$( d ) \Pi _ { i > 0 } O ( n _ { i } ) .$$

Furthermore, the algorithmic complexity of Basu's new procedure involves only (m)Πi&gt;0(ni+1)(d)n′ IIi&gt;0 (ni) arithmetic operations.

Lower bound results for the quantifier elimination problem can be found in Davenport and Heintz [DH88]. They showed that for every n, there exists a Tarski formula Ψn with n quantifiers, of length O(n), and of constant degree, such that any quantifier-free formula ψn logically equivalent to Ψn must involve polynomials of


<!-- p:5 -->


$$\deg r e = 2 ^ { 2 ^ { \Omega ( n ) } } \quad \text {and} \quad \text {length} = 2 ^ { 2 ^ { \Omega ( n ) } } .$$

Note that in the simplest possible case (i.e., d = 2 and ni = 2), upper and lower bounds are doubly exponential and match well. This result, however, does not imply a similar lower bound for the decision problems.

### 33.2 SEMIALGEBRAIC SETS

Every quantifier-free formula composed of polynomial inequalities and Boolean connectives defines a semialgebraic set. Thus, these semialgebraic sets play an important role in real algebraic geometry.

#### GLOSSARY

Semialgebraic set: A subset S ⊆ Rn defined by a set-theoretic expression involving a system of polynomial inequalities

$$S = \bigcup _ { i = 1 } ^ { I } \bigcap _ { j = 1 } ^ { J _ { i } } \left \{ \langle \xi _ { 1 } , \dots , \xi _ { n } \rangle \in \mathbb { R } ^ { n } \ | \ \text {sgn} ( f _ { i , j } ( \xi _ { 1 } , \dots , \xi _ { n } ) ) = s _ { i , j } \right \} ,$$

where the fi,j's are multivariate polynomials over R and the si,j's are corresponding sets of signs in {−1, 0, +1}.

Real algebraic set: A subset Z ⊆ Rn defined by a system of algebraic equations.

$$Z = \left \{ \langle \xi _ { 1 } , \dots , \xi _ { n } \rangle \in \mathbb { R } ^ { n } \ \ | \ \ f _ { 1 } ( \xi _ { 1 } , \dots , \xi _ { n } ) = \cdots = f _ { m } ( \xi _ { 1 } , \dots , \xi _ { n } ) = 0 \right \} ,$$

where the f¿'s are multivariate polynomials over R.

Semialgebraic map: A map θ : S → T, from a semialgebraic set S ⊆ Rm to a semialgebraic set T ⊆ Rn, such that its graph {(s, θ(s)〉 ∈ Rm+n : s ∈ S} is a semialgebraic set in Rm+n. Note that projection, being linear, is a semialgebraic map.

#### TARSKI-SEIDENBERG THEOREM

Equivalently, semialgebraic sets can be defined as

$$S = \left \{ \langle \xi _ { 1 } , \dots , \xi _ { n } \rangle \in \mathbb { R } ^ { n } \ \ | \ \psi ( \xi _ { 1 } , \dots , \xi _ { n } ) = \text {True} \right \} ,$$

where ψ(x1, ..., xn) is a quantifier-free formula involving n algebraic variables. As a direct corollary of Tarski's theorem on quantifier elimination, we see that extensions of Tarski formulas are also semialgebraic sets.


<!-- p:6 -->


While real algebraic sets are quite interesting and would be natural objects of study in this context, they are not closed under projection onto a subspace. Hence they tend to be unwieldy. However, semialgebraic sets are closed under projection. This follows from a more general result: the famous Tarski-Seidenberg theorem which is an immediate consequence of quantifier elimination, since images are described by formulas involving only existential quantifiers.

###### THEOREM 33.2.1 Tarski-Seidenberg Theorem [Sei74]

Let S be a semialgebraic set in Rm, and let θ : Rm → Rn be a semialgebraic map. Then θ(S) is semialgebraic in Rn.

In fact, semialgebraic sets can be defined simply as the smallest class of subsets of Rn containing real algebraic sets and closed under projection.

#### GLOSSARY

- Connected component of a semialgebraic set: A maximal connected subset of a semialgebraic set. Semialgebraic sets have a finite number of connected components and these are also semialgebraic.
- Semialgebraic decomposition of a semialgebraic set S: A finite collection K of disjoint connected semialgebraic subsets of S whose union is S. The collection of connected components of a semialgebraic set forms a semialgebraic decomposition. Thus, every semialgebraic set admits a semialgebraic decomposition.
- Set of sample points for S: A finite number of points meeting every nonempty connected component of S.
- Sign assignment: A vector of sign values of a set of polynomials at a point p. More formally, let F be a set of real multivariate polynomials in n variables. Any point p = 〈ξ1, . . ., ξn〉 ∈ Rn has a sign assignment with respect to F as follows:

$$\ s g n _ { \mathcal { F } } ( p ) = \left \langle \ s g n ( f ( \xi _ { 1 } , \dots , \xi _ { n } ) ) \ | \ f \in \mathcal { F } \right \rangle .$$

- A sign assignment induces an equivalence relation: Given two points p, q ∈ Rn, we say

$$p \, \sim _ { \mathcal { F } } q , \ \text { if and only if } \ s g n _ { \mathcal { F } } ( p ) = s g n _ { \mathcal { F } } ( q ) .$$

- Sign class of F: An equivalence class in the partition of Rn defined by the equivalence relation ~F.
- Semialgebraic decomposition for F: A finite collection of disjoint connected semialgebraic subsets {Ci} such that each Ci is contained in some semialgebraic sign class of F. That is, the sign of each f ∈ F is invariant in each Ci. The collection of connected components of the sign-invariant sets for F forms a semialgebraic decomposition for F.
- Cell decomposition for F: A semialgebraic decomposition for F into finitely many disjoint semialgebraic subsets {Ci} called cells, such that each cell Ci is homeomorphic to Rδ(i) , 0 ≤ δ(i) ≤ n. δ(i) is called the dimension of the cell Ci, and Ci is called a δ(i)-cell.
- Cellular decomposition for F: A cell decomposition for F such that the closure Ci of each cell Ci is a union of cells Cj: Ci = UjCj.


<!-- p:7 -->


#### CONNECTED COMPONENTS OF SEMIALGEBRAIC SETS

A consequence of the Milnor-Thom result [Mil64, Tho65] gives a bound for the number (the zeroth Betti number, B0(S)) of connected components of a basic semialgebraic set S: the bound is polynomial in the number m and degree d of the polynomials defining S and singly exponential in the number of variables, n. The current best bound for B0(S) is due to Pollack and Roy [PR93]: B0(S) = O(md)n.

Most recent work of Basu ([Bas01], Theorem 4) provides even more precise information about the topological complexity of basic semialgebraic sets through the higher-order Betti numbers. While B0(S) measures the number of connected components of the semialgebraic set S, intuitively, Bi(S) (i &gt; 0) measures the number of i-dimensional holes in S. The following bound on Bi is due to Basu:

####### THEOREM 33.2.2

Let S ⊆ Rn be the set defined by the conjunction of m inequalities,

$$f _ { i } ( x _ { 1 } , \dots , x _ { n } ) & \geq 0 , \quad f _ { i } \in \mathbb { R } [ x _ { 1 } , \dots , x _ { n } ] , \\ & \quad d e g r e e ( f _ { i } ) \leq d , \quad 1 \leq i \leq m ,$$

contained in a variety V(Q) of real dimension n', and

$$d e g r e e ( Q ) \leq d .$$

$$B _ { i } ( S ) \leq m ^ { n ^ { \prime } - i } O ( d ) ^ { n } .$$

Then,

A key problem in computational real algebraic geometry is to compute at least one point in each connected component of each nonempty sign assignment. An elegant solution to this problem is obtained by Collins's cylindrical algebraic decomposition (CAD), which is, in fact, a cell decomposition; see Section 33.5 below. A related question is to provide a finitary representation for these sample points, e.g., each coordinate of the sample point may be a real algebraic number.

Currently, the best algorithm computing a finite set of points of bounded size that intersects every connected component of each nonempty sign condition is due to Basu et al. [BPR98] and has an arithmetic time-complexity of m(m/n)ndO(n).

### 33.3 REAL ALGEBRAIC NUMBERS

Real algebraic numbers are real roots of rational univariate polynomials and prono ss  so ist on  os o o ry ots Furthermore, we note that (1) real algebraic numbers have effective finitary representation, (2) field operations and polynomial evaluation on real algebraic numbers are efficiently (polynomially) computable, and (3) conversions among various representations of real algebraic numbers are efficiently (polynomially) computable. The key machinery used in describing and manipulating real algebraic numbers relies upon techniques based on the Sturm-Sylvester theorem, Thom's lemma, resultant construction, and various bounds for real root separation.


<!-- p:8 -->


#### GLOSSARY

Real algebraic number: A real root α of a univariate polynomial p(t) ∈ Z[t] with integer coefficients.

Polynomial for α: A univariate polynomial p such that α is a real root of p.

Minimal polynomial of α: A univariate polynomial p of minimal degree defining α as above.

Degree of a nonzero real algebraic number: The degree of its minimal polynomial. By convention, the degree of the 0 polynomial is -∞.

#### OPERATIONS ON REAL ALGEBRAIC NUMBERS

Note that if α and β are real algebraic numbers, then so are -α, α−1 (assuming α ≠ 0), α+β, and α·β. These facts can be constructively proved using the algebraic properties of a resultant construction.

####### THEOREM 33.3.1

The real algebraic numbers form a field.

A real algebraic number α can be represented by a polynomial for α and a component that identifies the root. There are essentially three types of information that may be used for this identification: order (where we assume the real roots are indexed from left to right), sign (by a vector of signs), or interval (an interval that contains exactly one root).

A classical technique due to Sturm and Sylvester shows how to compute the number of real roots of a univariate polynomial p(t) in an interval [a, b]. One important use of this classical theorem is to compute a sequence of relatively small (nonoverlapping) intervals that isolate the real roots of p.

#### GLOSSARY

Sturm sequence of a pair of polynomials p(t) and q(t) ∈ R[t]:

$$\overline { S T U R M } ( p , q ) = \left \langle \hat { r } _ { 0 } ( t ) , \hat { r } _ { 1 } ( t ) , \dots , \hat { r } _ { s } ( t ) \right \rangle ,$$

where

$$\text {where} & & \hat { r } _ { 0 } ( t ) & = & \ p ( t ) \\ & \hat { r } _ { 1 } ( t ) & = & \ q ( t ) \\ & \vdots \\ & \hat { r } _ { i - 1 } ( t ) & = & \ \hat { q } _ { i } ( t ) \, \hat { r } _ { i } ( t ) - \hat { r } _ { i + 1 } ( t ) , \quad \deg ( \hat { r } _ { i + 1 } ) < \deg ( \hat { r } _ { i } ) \\ & \vdots \\ & \hat { r } _ { s - 1 } ( t ) & = & \ \hat { q } _ { s } ( t ) \, \hat { r } _ { s } ( t ) . \\ \intertext { w h e r e } \text { } & & \hat { r } _ { i - 1 } ( t ) & = & \ \hat { q } _ { i } ( t ) \, \hat { r } _ { i } ( t ) - \hat { r } _ { i + 1 } ( t ) , \quad \deg ( \hat { r } _ { i + 1 } ) < \deg ( \hat { r } _ { i } ) \\ & & \vdots \\ & & \vdots \\ & & \hat { r } _ { s - 1 } ( t ) & = & \ \hat { q } _ { s } ( t ) \, \hat { r } _ { s } ( t ) .$$

Number of variations in sign of a finite sequence č of real numbers: Number of times the entries change sign when scanned sequentially from left to right; denoted Var(c).


<!-- p:9 -->


For a vector of polynomials P = 〈p1(t), . . ., pm(t)〉 and a real number a:

$$\ V a r _ { a } ( \overline { P } ) \, = \, \ V a r ( \overline { P } ( a ) ) \, = \, \ V a r ( \langle p _ { 1 } ( a ) , \dots , p _ { m } ( a ) \rangle ) .$$

Formal derivative: p'(t) = D(p(t)), where D: R[t] → R[t] is the (formal) derivative map, taking tn to ntn−1 and a ∈ R (a constant) to 0.

#### STURM-SYLVESTER THEOREM

THEOREM 33.3.2 Sturm-Sylvester Theorem [Stu35, Syl53]

Let p(t) and q(t) ∈ R[t] be two real univariate polynomials. Then, for any interval [a, b] ⊆ R ∪ {±∞} (where a &lt; b):

$$V a r [ \overline { P } ] _ { a } ^ { b } = c _ { p } \left [ q > 0 \right ] _ { a } ^ { b } - c _ { p } \left [ q < 0 \right ] _ { a } ^ { b } ,$$

$$\overline { P } \ \triangle q \ \overline { \text {TURM} } ( p , p ^ { \prime } q ) , \\ \text {Var} \left [ \overline { P } \right ] _ { a } ^ { b } \ \triangle q \ \text {Var} _ { a } ( \overline { P } ) - \text {Var} _ { b } ( \overline { P } ) \, ,$$

and cp[P]å counts the number of distinct real roots (without counting multiplicity) of p in the interval (a, b) at which the predicate P holds.

Note that if we take Sp  STURM(p, p′) (i.e., q = 1) then

$$\text {Var} \left [ S _ { p } \right ] _ { a } ^ { b } \ = \ c _ { p } \left [ \text {True} \right ] _ { a } ^ { b } - c _ { p } \left [ \text {False} \right ] _ { a } ^ { b } \\$$

# of distinct real roots of p in (a, b).

####### COROLLARY 33.3.3

Let p(t) and q(t) be two polynomials with coefficients in a real closed field K. For any interval [a, b] as before, we have

$$\left [ \begin{array} { c c c } 1 & 1 & 1 \\ 0 & 1 & - 1 \\ 0 & 1 & 1 \end{array} \right ] \left [ \begin{array} { c } c _ { p } \left [ q = 0 \right ] _ { a } ^ { b } \\ c _ { p } \left [ q > 0 \right ] _ { a } ^ { b } \\ c _ { p } \left [ q < 0 \right ] _ { a } ^ { b } \end{array} \right ] = \left [ \begin{array} { c } \ V a r [ \overline { S TURM } ( p , p ^ { \prime } ) ] _ { a } ^ { b } \\ \ V a r [ \overline { S TURM } ( p , p ^ { \prime } q ) ] _ { a } ^ { b } \\ \ V a r [ \overline { S TURM } ( p , p ^ { \prime } q ^ { 2 } ) ] _ { a } ^ { b } \end{array} \right ] .$$

These identities as well as some related algorithmic results (the so-called BKRalgorithm) are based on results of Ben-Or et al. [BKR86] and their extensions by others. Using this identity, it is a fairly simple matter to decide the sign conditions of a single univariate polynomial q at the roots of a univariate polynomial p. It is possible to generalize this idea to decide the sign conditions of a sequence of univariate polynomials q0(t), q1(t), .. ., qn(t) at the roots of a single polynomial

where p(t) and hence give an efficient (both sequential and parallel) algorithm for the decision problem for Tarski sentences involving univariate polynomials. Further applications in the context of general decision problems are described below.


<!-- p:10 -->


#### GLOSSARY

Fourier sequence of a real univariate polynomial p(t) of degree n:

$$\overline { \ F O U R I E R } ( p ) = \left \langle p ^ { ( 0 ) } ( t ) = p ( t ) , \, p ^ { ( 1 ) } ( t ) = p ^ { \prime } ( t ) , \, \dots , \, p ^ { ( n ) } ( t ) \, \right \rangle ,$$

where p(i) is the ith derivative of p with respect to t.

Sign-invariant region of R determined by a sign sequence s with respect to FOURIER(p): The region R() with the property that ξ ∈ R() if and only if sgn(p(i)(ξ)) = si.

#### THOM'S LEMMA

LEMMA 33.3.4 Thom's Lemma [Tho65]

e  sens ns    (sd uont -n nn t respect to FOURIER(p)) must be connected, i.e., consists of a single interval.

Let sgng(FOURIER(p)) be the sign sequence obtained by evaluating the polynomials of FoURIER(p) at ξ. Then as an immediate corollary of Thom's lemma, we have:

####### COROLLARY 33.3.5

Let ξ and ζ be two real roots of a real univariate polynomial p(t) of positive degree n &gt; 0. Then ξ = ζ, if

$$\ s g n _ { \xi } ( \overline { F O U R I E R } ( p ^ { \prime } ) ) = \ s g n _ { \zeta } ( \overline { F O U R I E R } ( p ^ { \prime } ) ) .$$

#### REPRESENTATION OF REAL ALGEBRAIC NUMBERS

Let p(t) be a univariate polynomial of degree d with integer coefficients. Assume that the distinct real roots of p(t) have been enumerated as follows:

$$\alpha _ { 1 } < \alpha _ { 2 } < \cdots < \alpha _ { j - 1 } < \alpha _ { j } = \alpha \, < \alpha _ { j + 1 } < \cdots < \alpha _ { l } ,$$

where l ≤ d = deg(p). Then we can represent any of its roots uniquely and in a finitary manner.

#### GLOSSARY

Order representation of an algebraic number: A pair consisting of its polynomial p and its index j in the monotone sequence enumerating the real roots of p: 〈α&gt;o = 〈p, j〉. Example: 〈√2 + √3)o = 〈x4 − 10x2 + 1, 4).


<!-- p:11 -->


Sign representation of an algebraic number: A pair consisting of its polynomial p and a sign sequence  representing the signs of its Fourier sequence eval= (ε + 〉 :dx) ((,es =  d = ( :x ( e (x4 − 10x2 + 1, (+1, +1, +1)). The validity of this representation follows easily from Thom's lemma.

Interval representation of an algebraic number: A triple consisting of its polynomial p and the two endpoints of an isolating interval, (l, r) (l, r ∈ Q, l &lt; r), (/   + x0 − x〉 = ( +〉 :dx (, 1) = (〉) :  2)

### 33.4 UNIVARIATE DECOMPOSITION

In the one-dimensional case, a semialgebraic set is the union of finitely many intervals whose endpoints are real algebraic numbers. For instance, given a set of univariate defining polynomials:

$$\mathcal { F } = \left \{ f _ { i } ( x ) \in \mathbb { Q } [ x ] \ \ | \ \ i = 1 , \dots , m \right \} ,$$

we may enumerate all the real roots of the fi's (i.e., the real roots of the single polynomial F = ∏ fi) as

$$- \infty \, < \, \xi _ { 1 } \, < \, \xi _ { 2 } \, < \, \cdots \, < \, \xi _ { i - 1 } \, < \, \xi _ { i } \, < \, \xi _ { i + 1 } \, < \, \cdots \, < \, \xi _ { s } \, < \, + \infty ,$$

and consider the following finite set K of elementary intervals defined by these roots:

$$[ - \infty , \xi _ { 1 } ) , & \ [ \xi _ { 1 } , \xi _ { 1 } ] , \ ( \xi _ { 1 } , \xi _ { 2 } ) , \ \dots , \\ & ( \xi _ { i - 1 } , \xi _ { i } ) , \ [ \xi _ { i } , \xi _ { i } ] , \ ( \xi _ { i } , \xi _ { i + 1 } ) , \ \dots , \ [ \xi _ { s } , \xi _ { s } ] , \ ( \xi _ { s } , + \infty ] .$$

Note that K is, in fact, a cellular decomposition for F. Any semialgebraic set S defined by F is simply the union of a subset of elementary intervals in K. Furthermore, for each interval C ∈ K, we can compute a sample point αc as follows:

$$\alpha _ { C } = \begin{cases} & \xi _ { 1 } - 1 , & \text { if } C = [ - \infty , \xi _ { 1 } ) ; \\ & \xi _ { i } , & \text { if } C = [ \xi _ { i } , \xi _ { i } ] ; \\ & ( \xi _ { i } + \xi _ { i + 1 } ) / 2 , & \text { if } C = ( \xi _ { i } , \xi _ { i + 1 } ) ; \\ & \xi _ { s } + 1 , & \text { if } C = ( \xi _ { s } , + \infty ] . \end{cases}$$

Now, given a first-order formula involving a single variable, its validity can be checked by evaluating the associated univariate polynomials at the sample points. Using the algorithms for representing and manipulating real algebraic numbers, we see that the bit complexity of the decision algorithm is bounded by (Lmd)O(1). The resulting cellular decomposition has no more than 2md + 1 cells.

Using variants of the theorem due to Ben-Or et al. [BKR86], Thom's lemma, and some results on parallel computations in linear algebra, one can show that this univariate decision problem is "well-parallelizable," i.e., the problem is solvable by uniform circuits of bounded depth and polynomially many "gates" (simple processors).


<!-- p:12 -->


### 33.5 MULTIVARIATE DECOMPOSITION

A straightforward generalization of the standard univariate decomposition to higher dimensions is provided by Collins's cylindrical algebraic decomposition [Col75]. In order to represent a semialgebraic set S ⊆ Rn, we may assume recursively that we can construct a cell decomposition of its projection π(S) ⊆ Rn-1 (also a semialgebraic set), and then decompose S as a union of the sectors and sections in the cylinders above each cell of the projection, π(S). This also leads to a cell decomposition of S. One can further assign an algebraic sample point in each cell of S recursively in a straightforward manner.

If F is a set of polynomials defining the semialgebraic set S ⊆ Rn, then at no additional cost, we may in fact compute a cell decomposition for F using the procedure described above. Such a decomposition leads to a cylindrical algebraic decomposition for F.

#### GLOSSARY

Cylindrical algebraic decomposition (CAD): A recursively defined cell decomposition of Rn for F. The decomposition is a cellular decomposition if the set of defining polynomials F satisfies certain nondegeneracy conditions.

In the recursive definition, the cells of n-dimensional CAD are constructed from an (n-1)-dimensional CAD: Every (n-1)-dimensional CAD cell C' has the property that the distinct real roots of F over C' vary continuously as a function of the points of C'.

Moreover, the following quantities remain invariant over a (n-1)-dimensional cell: (1) the total number of complex roots of each polynomial of F; (2) the number of distinct complex roots of each polynomial of F; and (3) the total number of common complex roots of every distinct pair of polynomials of F.

These conditions can be expressed by a set Φ(F) of at most O(md)2 polynomials in n - 1 variables, obtained by considering principal subresultant coefficients (PSC's). Thus, they correspond roughly to resultants and discriminants, and ensure that the polynomials of F do not intersect or "fold" in a cylinder over an (n-1)-dimensional cell. The polynomials in Φ(F) are each of degree no more than d2.

More formally, an F-sign-invariant cylindrical algebraic decomposition of Rn is:

- BASE CASE: n = 1. A univariate cellular decomposition of R1 as in the ■ previous section.
- INDUCTIVE CASE: n &gt; 1. Let K′ be a Φ(F)-sign-invariant CAD of Rn−1. For each cell C′ ∈ K′, define an auxiliary polynomial gc' (x1 , . . . , xn−1, xn) as the product of those polynomials of F that do not vanish over the (n-1)- dimensional cell, C'. The real roots of the auxiliary polynomial g'c over C' give rise to a finite number (perhaps zero) of semialgebraic continuous functions, which partition the cylinder C′ × (R ∪ {±∞}) into finitely many F-sign-invariant "slices." The auxiliary polynomials are of degree no larger than md.


<!-- p:13 -->


FIGURE 33.5.1 Sections and sectors "slicing" the cylinder over a lower dimensional

13

r2

C'

r1

Assume that the polynomial gc'(p', xn) has l distinct real roots for each p′ ∈ C′: r1 (p′), r2(p′), . . . , rl(p′), each ri being a continuous function of p′. The following sectors and sections are cylindrical over C' (see Figure 33.5.1):

$$The following sections and sections are c y l i n d r i c a l o r C ^ { \prime } \left ( s e e \, F i gure \, 3 3 . 5 . 1 \\ C _ { 0 } ^ { * } \ = \ \left \{ \langle p ^ { \prime } , x _ { n } \rangle \ | \ p ^ { \prime } \in C ^ { \prime } \wedge x _ { n } \in [ - \infty , r _ { 1 } ( p ^ { \prime } ) ) \right \} , \\ C _ { 1 } \ = \ \left \{ \langle p ^ { \prime } , x _ { n } \rangle \ | \ p ^ { \prime } \in C ^ { \prime } \wedge x _ { n } \in [ r _ { 1 } ( p ^ { \prime } ) , r _ { 1 } ( p ^ { \prime } ) ] \right \} , \\ C _ { 1 } ^ { * } \ = \ \left \{ \langle p ^ { \prime } , x _ { n } \rangle \ | \ p ^ { \prime } \in C ^ { \prime } \wedge x _ { n } \in ( r _ { 1 } ( p ^ { \prime } ) , r _ { 2 } ( p ^ { \prime } ) ) \right \} , \\ \vdots \\ C _ { l } ^ { * } \ = \ \left \{ \langle p ^ { \prime } , x _ { n } \rangle \ | \ p ^ { \prime } \in C ^ { \prime } \wedge x _ { n } \in ( r _ { l } ( p ^ { \prime } ) , + \infty ] \right \} .$$

The n-dimensional CAD is thus the union of all the sections and sectors computed over the cells of the (n-1)-dimensional CAD.

A straightforward recursive algorithm to compute a CAD follows from the above description.

#### CYLINDRICAL ALGEBRAIC DECOMPOSITION

If we assume that the dimension n is a fixed constant, then the preceding cylindrical algebraic decomposition algorithm is polynomial in m = |F| and d = deg(F). However, the algorithm can be easily seen to be doubly-exponential in n as the degree no larger than d2). The number of cells produced by the algorithm is also doubly-exponential. This bound can be seen to be tight by a result due to Davenport and Heintz [DH88], and is related to their lower bound for the quantifier elimination problem (Section 33.1).

#### CONSTRUCTING SAMPLE POINTS

Cylindrical algebraic decomposition provides a sample point in every sign-invariant connected component for F. However, the total number of sample points generated is doubly-exponential, while the number of connected components of all sign

cell.


<!-- p:14 -->


conditions is only singly-exponential. In order to avoid this high complexity (both algebraic and combinatorial) of a CAD, many recent techniques for constructing sample points use a single projection to a line instead of a sequence of cascading projections. For instance, if one chooses a height function carefully then one can easily enumerate its critical points and then associate at least two such critical points to every connected component of the semialgebraic set. From these critical points, it will be possible to create at least one sample point per connected component. Using Bézout's bound, it is seen that only a singly-exponential number of sample points is created, thus improving the complexity of the underlying algorithms.

However, in order to arrive at the preceding conclusion using critical points, one requires certain genericity conditions that can be achieved by symbolically deforming the underlying semialgebraic sets. These infinitesimal deformations can be handled by extending the underlying field to a field of Puiseux series. Many of the significant complexity improvements based on these techniques have been due to a careful choice of the symbolic perturbation schemes which results in keeping the number of perturbation variables small.

### 33.6 ALGORITHMIC APPROACHES

#### COLLINS'S APPROACH

The decision problem for the first-order theory of reals can be solved easily using a cylindrical algebraic decomposition. First consider the existential problem for a sentence with only existential quantifiers,

$$( \exists \, x ^ { [ 0 ] } ) \, [ \psi ( x ^ { [ 0 ] } ) ] .$$

This sentence is true if and only if there is a q ∈ C, a sample point in the cell C,

$$q \, = \, \alpha ^ { [ 0 ] } = \langle \alpha _ { 1 } , \dots , \alpha _ { n } \rangle \, \in \, \mathbb { R } ^ { n } ,$$

such that ψ(α[o]) is true. Thus we see that the decision problem for the purely existential sentence can be solved by simply evaluating the matrix ψ over the finitely many sample points in the associated CAD. This also implies that the existential quantifiers could be replaced by finitely many disjunctions ranging over all the sample points. Note that the same arguments hold for any semialgebraic decomposition with at least one sample point per sign-invariant connected component.

In the general case, one can describe the decision procedure by means of a search process that proceeds only on the coordinates of the sample points in the cylindrical algebraic decomposition. This follows because a sample point in a cell er st os eo s   o eo   n o  a s sne concerned.

Consider a Tarski sentence

$$( \mathcal { Q } _ { 1 } x ^ { [ 1 ] } ) \left ( \mathcal { Q } _ { 2 } x ^ { [ 2 ] } \right ) \cdots ( \mathcal { Q } _ { \omega } x ^ { [ \omega ] } ) \left [ \psi ( x ^ { [ 1 ] } , \dots , x ^ { [ \omega ] } ) ,$$

with F the set of polynomials appearing in the matrix ψ. Let K be a cylindrical algebraic decomposition of Rn for F. Since the cylindrical algebraic decomposition produces a sequence of decompositions:


<!-- p:15 -->


$$\mathcal { K } _ { 1 } \text { of } \mathbb { R } ^ { 1 } , \ \mathcal { K } _ { 2 } \text { of } \mathbb { R } ^ { 2 } , \ \dots , \ \mathcal { K } _ { n } \text { of } \mathbb { R } ^ { n } ,$$

such that the each cell Ci-1,j of Ki is cylindrical over some cell Ci-1 of Ki-1, the search progresses by first finding cells C1 of K1 such that

$$( \mathcal { Q } _ { 2 } x _ { 2 } ) \, \cdots ( \mathcal { Q } _ { n } x _ { n } ) \, [ \psi ( \alpha _ { C _ { 1 } } , x _ { 2 } , \dots , x _ { n } ) ] = T r u e .$$

For each C1, the search continues over cells C12 of K2 cylindrical over C1 such that

$$( \mathcal { Q } _ { 3 } x _ { 3 } ) \, \cdots \, ( \mathcal { Q } _ { n } x _ { n } ) \left [ \psi ( \alpha _ { C _ { 1 } } , \alpha _ { C _ { 1 2 } } , x _ { 3 } , \dots , x _ { n } ) \right ] = T r u e ,$$

etc. Finally, at the bottom level the truth properties of the matrix ψ are determined by evaluating at all the coordinates of the sample points.

This produces a tree structure, where each node at the (i—1)th level corresponds to a cell Ci-1 ∈ Ki-1 and its children correspond to the cells Ci-1,j ∈ Ki that are cylindrical over Ci-1. The leaves of the tree correspond to the cells of the final decomposition K = Kn. Because we only have finitely many sample points, the universal quantifiers can be replaced by finitely many conjunctions and the existential quantifiers by disjunctions. Thus, we label every node at the (i-1)th level "AND" (respectively, "OR") if Qi is a universal quantifier ∀ (respectively, ∃) to produce a so-called AND-OR tree. The truth of the Tarski sentence is thus determined by simply evaluating this AND-OR tree.

A quantifier elimination algorithm can be devised by a similar reasoning and a slight modification of the CAD algorithm described above.

#### NEW APPROACHES USING CRITICAL POINTS

In order to avoid the cascading projections inherent in Collins's algorithm, the new approaches employ a single projection to a one-dimensional set by using critical points in a manner described above. As before, we start with a sentence with only existential quantifiers,

$$( \exists \, x ^ { [ 0 ] } ) \, [ \psi ( x ^ { [ 0 ] } ) ] .$$

Let F = {f1, . . ., fm } be the set of polynomials appearing in the matrix ψ.

Under certain genericity conditions, it is possible to produce a set of sample points such that every sign-invariant connected component of the decomposition induced by F contains at least one such point. Furthermore, these sample points are described by a set of univariate polynomial sequences, where each sequence is of the form

$$p ( t ) , q _ { 0 } ( t ) , q _ { 1 } ( t ) , \dots , q _ { n } ( t ) ,$$

and encodes a sample point q1(α) g0(α), ·  . , q0(α) problem for the existential theory can be solved by deciding the sign conditions of the sequence of univariate polynomials

$$f _ { 1 } ( q _ { 1 } / q _ { 0 } , \dots , q _ { n } / q _ { 0 } ) , \dots , \, f _ { m } ( q _ { 1 } / q _ { 0 } , \dots , q _ { n } / q _ { 0 } ) ,$$

at the roots of the univariate polynomial p(t). Note that we have now reduced a multivariate problem to a univariate problem and can solve this by the BKR approach.


<!-- p:16 -->


In order to keep the complexity reasonably small, one needs to ensure that the number of such sequences is small and that these polynomials are of low degree. Assuming that the polynomials in F are in general position, one can achieve this and compute the polynomials p and qi (for example, by the u-resultant method in Renegar's algorithm).

If the genericity conditions are violated, one needs to symbolically deform the polynomials and carry out the computations on these polynomials with additional perturbation parameters. The Basu-Pollack-Roy (BPR) algorithm differs from Renegar's algorithm primarily in the manner in which these perturbations are made so that their effect on the algorithmic complexity is controlled.

Next consider an existential Tarski formula of the form

$$( \exists \, x ^ { [ 0 ] } ) \, [ \psi ( y , x ^ { [ 0 ] } ) ] ,$$

where y represents the free variables. If we carry out the same computation as before over the ambient field R(y), we get a set of parameterized univariate polynomial sequences, each of the form

$$p ( y , t ) , q _ { 0 } ( y , t ) , q _ { 1 } ( y , t ) , \dots , q _ { n } ( y , t ) .$$

For a fixed value of y, say y, the polynomials

$$p ( \bar { y } , t ) , q _ { 0 } ( \bar { y } , t ) , q _ { 1 } ( \bar { y } , t ) , \dots , q _ { n } ( \bar { y } , t )$$

can then be used as before to decide the truth or falsity of the sentence

$$( \exists \, x ^ { [ 0 ] } ) \, [ \psi ( \bar { y } , x ^ { [ 0 ] } ) ] .$$

Also, one may observe that the parameter space y can be partitioned into semialgebraic sets so that all the necessary information can be obtained by computing at sample values ī.

This process can be extended to ω blocks of quantifiers, by replacing each block of variables by a finite number of cases, each involving only one new variable; the last step uses a CAD method for these ω-many variables.

### 33.7 APPLICATIONS

Computational real algebraic geometry finds applications in robotics, vision, computer-aided design, geometric theorem proving, and other fields. Important problems in robotics include the kinematic modeling, the inverse kinematic solution, the computation of the workspace and workspace singularities, and the planning of an obstacle-avoiding motion of a robot in a cluttered environment—all arising from the algebro-geometric nature of robot kinematics. In solid modeling, graphics, and vision, almost all applications involve the description of surfaces, the generation of various auxiliary surfaces such as blending and smoothing surfaces, the classification of various algebraic surfaces, the algebraic or geometric invariants associated with a surface, the effect of various affine or projective transformations of a surface, the description of surface boundaries, and so on.

To give examples of the nature of the solutions demanded by various applications, we discuss a few representative problems from robotics, engineering, and computer science.


<!-- p:17 -->


#### ROBOT MOTION PLANNING

Given the initial and desired configurations of a robot (composed of rigid subparts) and a set of obstacles, find a collision-free continuous motion of the robot from the initial configuration to the final configuration.

The algorithm proceeds in several steps. The first step translates the problem to configuration space, a parameter space modeled as a low-dimensional algebraic manifold (assuming that the obstacles and the robot subparts are bounded by piecewise algebraic surfaces). The second step computes the set of configurations that avoid collisions and produces a semialgebraic description of this so-called "free space" (subspaces of the configuration space). Since the initial and final configurations correspond to two points in the configuration space, we simply have to test whether they lie in the same connected component of the free space. If so, they can be connected by a piecewise algebraic path. Such a path gives rise to an obstacle-avoiding motion of the robot(s). This path planning process can be carried out using Collins's CAD [SS83], yielding an algorithm with doubly-exponential time complexity (Theorem 40.1.1). A singly-exponential time complexity algorithm (the roadmap algorithm) has been devised by Canny [Can88a] (Theorem 40.1.2). The main idea of Canny's algorithm is to determine a one-dimensional connected subset (called the "roadmap") of each connected component of the free space. Once these roadmaps are available, they can be used to link up two points in the same connected component. The main geometric idea is to construct roadmaps starting from the critical sets of some projection function. The basic roadmap algorithm has been improved and extended by several researchers over the last decade (Heintz et al. [HRS90], Gournay and Risler [GR93], Grigor'ev and Vorobjov [Gri88, GV88], and Canny [Can88a, Can90]).

#### OFFSET SURFACE CONSTRUCTION IN SOLID MODELING

Given a polynomial f(x,y,z), whose zeros define an algebraic surface in threedimensional space, compute the envelope of a family of spheres of radius r whose centers lie on the surface f. Such a surface is called a (two-sided) offset surface of f.

Let p = 〈x, y, z〉 be a point on the offset surface and q = 〈u, v, w) be a footprint of p on f; that is, q is the point at which a normal from p to f meets f. Let t1 = 〈t1,1, t1,2, t1,3〉 and t2 = 〈t2,1, t2,2, t2,3〉 be two linearly independent tangent vectors to f at the point q. Then, we see that the system of polynomial equations

$$( x - u ) ^ { 2 } + ( y - v ) ^ { 2 } + ( z - w ) ^ { 2 } - r ^ { 2 } \ & = \ 0 , \\ f ( u , v , w ) \ & = \ 0 , \\ ( x - u ) t _ { 1 , 1 } + ( y - v ) t _ { 1 , 2 } + ( z - w ) t _ { 1 , 3 } \ & = \ 0 , \\ ( x - u ) t _ { 2 , 1 } + ( y - v ) t _ { 2 , 2 } + ( z - w ) t _ { 2 , 3 } \ & = \ 0 , \\$$

describes a surface in the (x, y, z, u, v, w) six-dimensional space, which, when projected into the three-dimensional space with coordinates (x, y, z), gives the offset surface in an implicit form. The offset surface is computed by simply eliminating the variables u, v, w from the preceding set of equations.

This approach (the envelope method) of computing the offset surface has several problematic features: the method does not deal with self-intersection in a clean way and, sometimes, generates additional points not on the offset surface. For a discussion of these and several other related problems in solid modeling, see [Hof89] and Chapter 56 of this Handbook.


<!-- p:18 -->


#### GEOMETRIC THEOREM PROVING

Given a geometric statement consisting of a inite set of hypotheses and a conclusion,

$$\begin{array} { l c l } \text {Hypotheses} & \colon & f _ { 1 } ( x _ { 1 } , \dots , x _ { n } ) = 0 , \dots , f _ { r } ( x _ { 1 } , \dots , x _ { n } ) = 0 \\ & \text {Conclusion} & \colon & g ( x _ { 1 } , \dots , x _ { n } ) = 0 \end{array}$$

( = e ee e oe ecnb  se  =  eoe te e eep ∧ · · · ∧ (fr = 0)).

Thus we need to determine whether the following universally quantified firstorder sentence holds:

$$\left ( \forall \, x _ { 1 } , \dots , x _ { n } \right ) \left [ \left ( ( f _ { 1 } = 0 ) \wedge \cdots \wedge ( f _ { r } = 0 ) \right ) \Rightarrow \ g = 0 \right ] .$$

One way to solve the problem is by first translating it into the form: decide if the following existentially quantified first-order sentence is unsatisfiable:

$$\left ( \exists \, x _ { 1 } , \dots , x _ { n } , z \right ) \left [ \left ( f _ { 1 } = 0 \right ) \wedge \cdots \wedge \left ( f _ { r } = 0 \right ) \wedge \left ( g z - 1 \right ) = 0 \right ] .$$

When the underlying domain is assumed to be the field of real numbers, then we may simply check whether the following multivariate polynomial (in x1, . . . , xn, z) has no real root:

$$f _ { 1 } ^ { 2 } + \dots + f _ { r } ^ { 2 } + ( g z - 1 ) ^ { 2 } .$$

If, on the other hand, the underlying domain is assumed to be the field of complex numbers (an algebraically closed field), then other tools from computational algebra are used (e.g., techniques based on Hilbert's Nullstellensatz). In the general setting, some techniques based on Ritt-Wu characteristic sets have proven very powerful. See [Cho88].

For another approach to geometric theorem proving, see Section 59.4.

#### CONNECTION TO SEMIDEFINITE PROGRAMMING

Checking global nonnegativity of a function of several variables occupies a central role in many areas of applied mathematics, e.g., optimization problems with polynomial objectives and constraints, as in quadratic, linear and boolean programming formulations. These problems have been shown to be NP-hard in the most general setting, but do admit good approximations involving polynomial-time computable relaxations. (See Parilo [Par00]).

Provide checkable conditions or procedure for verifying the validity of the proposition

$$F ( x _ { 1 } , \dots , x _ { n } ) \geq 0 , \ \forall x _ { 1 } , \dots , x _ { n } ,$$


<!-- p:19 -->


where F is a multivariate polynomial in the ring of multivariate polynomials over the reals, R[x1 , . . . , xn].

An obvious necessary condition for F to be globally nonnegative is that it has even degree. On the other hand, a rather simple sufficient condition for a real-valued polynomial F(x) to be globally nonnegative is the existence of a sum-of-squares decomposition:

$$F ( x _ { 1 } , \dots , x _ { n } ) = \sum _ { i } f _ { i } ^ { 2 } ( x _ { 1 } , \dots , x _ { n } ) , \ \ f _ { i } ( x _ { 1 } , \dots , x _ { n } ) \in \mathbb { R } [ x _ { 1 } , \dots , x _ { n } ] .$$

Thus one way to solve the global nonnegativity problem is by finding a sum-oooe o  tte ot ois t o osod se-l nomials not admitting a sum-of-squares decomposition (e.g., the Motzkin form x4y2 + x2y4 + z6 − 3x2y2z2), the procedure suggested below does not give a solution to the problem in all situations.

The procedure can be described as follows: express the given polynomial F(x1, . . ., xn) of degree 2d as a quadratic form in all the monomials of degree less than or equal to d:

$$F ( x _ { 1 } , \dots , x _ { n } ) = z ^ { T } Q z , \ \ z = [ 1 , x _ { 1 } , \dots , x _ { n } , x _ { 1 } x _ { 2 } , \dots x _ { n } ^ { d } ] ,$$

where Q is a constant matrix to be determined. If the above quadratic form can be solved for a positive semidefinite Q, then F(x1, . . . , xn) is globally nonnegative. Sn i  xi  i  t r   sr  it. unique, but lives in an affine subspace. Thus, we need to determine if the intersection of this affine subspace and the positive semidefinite matrix cone is nonempty. This problem can be solved by a semidefinite programming feasibility problem:

$$\begin{array} { r l } { \text {trace} ( z z ^ { T } Q ) } & = } & { F ( x _ { 1 } , \dots , x _ { n } ) , } \\ { Q } & \preceq } & { 0 . } \end{array}$$

The dimensions of the matrix inequality are p for fixed number of variables (n) or fixed degree (d). Thus our question reduces to efficiently solvable semidefinite programming (SDP) problems.

### 33.8 SOURCES AND RELATED MATERIAL

### SURVEYS

[Mis93]: A textbook for algorithmic algebra covering Gröbner bases, characteristic sets, resultants, and real algebra. Chapter 8 gives many details of the classical results in computational real algebra.

[CJ98]: An anthology of key papers in computational real algebra and real algebraic geometry. Contains reprints of the following papers cited in this chapter: [BPR98, Col75, Ren91, Tar51].

[AB88]: A special issue of the J. Symbolic Comput. on computational real algebraic geometry. Contains several papers ([DH88, Gri88, GV88] cited here) addressing many key research problems in this area.


<!-- p:20 -->


[BR90]: A very accessible and self-contained textbook on real algebra and real algebraic geometry.

[BCR98]: A self-contained textbook on real algebra and real algebraic geometry.

[HRR91]: A survey of many classical and recent results in computational real algebra.

[Cha94]: A survey of the connections among computational geometry, computational algebra, and computational real algebraic geometry.

[Tar51]: Primary reference for Tarski's classical result on the decidability of elementary algebra.

[Col75]: Collins's work improving the complexity of Tarski's solution for the decision problem [Tar51]. Also, introduces the concept of cylindrical algebraic decomposition (CAD).

[Ren91]: A survey of some recent results, improving the complexity of the decision problem and quantifier elimination problem for the first-order theory of reals. This is mostly a summary of the results first given in a sequence of papers by Renegar [Ren92a,b,c].

[Lat91]: A comprehensive textbook covering various aspects of robot motion planning problems and different solution techniques. Chapter 5 includes a description of the connection between the motion planning problem and computational real algebraic geometry.

[SS83]: A classic paper in robotics showing the connection between the robot motion planning problem and the connectivity of semialgebraic sets using CAD. Contains several improved algorithmic results in computational real algebra.

[Can88a]: Gives a singly-exponential time algorithm for the robot motion planning problem and provides complexity improvement for many key problems in computational real algebra.

[Hof89]: A comprehensive textbook covering various computational algebraic techniques with applications to solid modeling. Contains a very readable description of Gröbner bases algorithms.

[Cho88]: A monograph on geometric theorem proving using Ritt-Wu characteristic sets. Includes computer-generated proofs of many classical geometric theorems.

### RELATED CHAPTERS

Chapter 47: Algorithmic motion planning

Chapter 48: Robotics

Chapter 56: Solid modeling

Chapter 59: Geometric applications of the Grassmann-Cayley algebra
