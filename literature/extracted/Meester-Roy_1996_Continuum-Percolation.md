---
id: "Meester-Roy_1996_Continuum-Percolation"
source_pdf: "../pdf/Meester-Roy_1996_Continuum-Percolation.pdf"
source_filename: "Meester-Roy_1996_Continuum-Percolation.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "hybrid"
extraction_quality: "good"
extraction_score: 98.4
visual_assets: "disabled"
references_file: "../references/Meester-Roy_1996_Continuum-Percolation.references.md"
---

<!-- p:1 -->

Continuum percolation This book is the first systematic and rigorous account of continuum percolation. The authors treat two models, the Boolean model and the random connection model, in detail, and discuss a number of related continuum models. Where appropriate, they make clear the connections between discrete percolation and continuum percolation.

<!-- p:2 -->


All important techniques and methods are explained and applied to obtain results on the existence of phase transitions, equality of certain densities, continuity of critical densities with respect to distributions, uniqueness of the unbounded component, covered volume fractions, compression, rarefaction and so on. The book is self-contained, assuming only familiarity with measure theory and basic probability theory. The approach makes use of simple ergodic theory, but the underlying geometric ideas are always made clear.


<!-- p:3 -->


Published by the Press Syndicate of the University of Cambridge The Pitt Building, Trumpington Street, Cambridge CB2 1RP 40 West 20th Street, New York, NY 10011-4211, USA 10 Stamford Road, Oakleigh, Melbourne 3166, Australia

© Cambridge University Press 1996

First published 1996

Printed in the United States of America

Library of Congress Cataloging-in-Publication Data Meester, Ronald.

Continuum percolation / Ronald Meester, Rahul Roy.

p. cm.

Includes bibliographical references and index.

ISBN 0-521-47504-X (hc)

1. Percolation (Statistical physics) 2. Stochastic processes.

QC174.85.P45M441996

1. Roy, Rahul. II. Title.

530.1'3 – dc20

95-40924

CIP

A catalog record for this book is available from the British Library.

1SBN ()-52t-47504-X hardback


<!-- p:4 -->


### Contents

| Preface   | Preface                                                         |   page ix |
|-----------|-----------------------------------------------------------------|-----------|
| 1         | Introduction                                                    |         1 |
| 1.1       | Motivation for continuum models                                 |         1 |
| 1.2       | Discrete percolation                                            |         2 |
| 1.3       | Stationary point processes                                      |         9 |
| 1.4       | The Boolean model                                               |        14 |
| 1.5       | The random-connection model                                     |        18 |
| 1.6       | Notes                                                           |        20 |
| 2         | Basic methods                                                   |        21 |
| 2.1       | Ergodicity                                                      |        21 |
| 2.2       | Coupling and scaling                                            |        28 |
| 2.3       | The FKG inequality                                              |        31 |
| 2.4       | The BK inequality                                               |        34 |
| 2.5       | Notes                                                           |        39 |
| 3         | Occupancy in Poisson Boolean models                             |        40 |
| 3.1       | Introduction                                                    |        40 |
| 3.2       | One-dimensional triviality                                      |        43 |
| 3.3       | Critical phenomena                                              |        45 |
| tr        | Critical densities                                              |        52 |
| 3.5       | Equality of the critical densities                              |        59 |
| 3.6       | Uniqueness                                                      |        63 |
| 3.7       | Exponential decay                                               |        68 |
| 3.8       | Continuity of the crilical densily and the percolation function |        71 |


<!-- p:5 -->


| vi                                                     | Contents                                               |         |
|--------------------------------------------------------|--------------------------------------------------------|---------|
| 3.9                                                    | Bounds on λ,. and asymptotics for the cluster size     | 85      |
| 110                                                    | Notes                                                  | 90      |
| 4                                                      | Vacancy in Poisson Boolean models                      | 16      |
| 11                                                     | Critical densities                                     | 92      |
| 小 RSW                                                  | notation and definition                                | 95      |
| 小1 RSW                                                 | construetion                                           | 97      |
| 11 RSW                                                 | prehuminary results                                    | 103     |
| 小 RSW                                                  | joon                                                   | 106     |
| 10 tquahy of the eritical densities                    | 10 tquahy of the eritical densities                    | 108     |
| 11                                                     |                                                        | 116     |
| 1N Contunumty ot the percolation funetion              | 1N Contunumty ot the percolation funetion              | 119     |
| 19 Notes                                               | 19 Notes                                               | 121     |
| 5 Distinguishing feutures of the Poisson Boolean model | 5 Distinguishing feutures of the Poisson Boolean model | 122     |
| 11 The covered vohuune fraction                        | 11 The covered vohuune fraction                        | 122     |
| uossanduo.)                                            | uossanduo.)                                            | 125     |
| 5.1 Raretaction                                        | 5.1 Raretaction                                        | 138     |
| 5.4 Notes                                              | 5.4 Notes                                              | 150     |
| 6 The Poisson random-connection model                  | 6 The Poisson random-connection model                  | 151     |
| 6.1 Non-triviality of the model                        | 6.1 Non-triviality of the model                        | 152     |
| 6.2 Properties of the connection function              | 6.2 Properties of the connection function              | 155     |
| 6.3 Equality of the critical densities                 | 6.3 Equality of the critical densities                 | 159     |
| 6.4 Uniqueness                                         | 6.4 Uniqueness                                         | 172     |
| 6.5 High density                                       | 6.5 High density                                       | 173     |
| 6.6 Notes                                              | 6.6 Notes                                              | 180     |
| 7 Models driven by general processes                   | 7 Models driven by general processes                   | 181     |
| 7.1 Ergodic decomposition                              | 7.1 Ergodic decomposition                              | 181     |
| 7.2 Basic facts on coverage                            | 7.2 Basic facts on coverage                            | 184     |
| 7.3 Unbounded components in Boolean models             | 7.3 Unbounded components in Boolean models             | 187     |
| 7.4 Uniqueness in Boolean models                       | 7.4 Uniqueness in Boolean models                       | 194     |
| Uniqueness in random-connection models                 | Uniqueness in random-connection models                 |         |
| 7.5                                                    |                                                        | 197     |
| 7.6 Cutting and stacking 7.7                           | 7.6 Cutting and stacking 7.7                           | 199     |
| Examples 7.8 Notes                                     | Examples 7.8 Notes                                     | 204 208 |


<!-- p:6 -->


| Contents   | Contents                                       |   vii |
|------------|------------------------------------------------|-------|
| 8          | Other continuum percolation models             |   209 |
| 8.1        | Continuum fractal percolation                  |   209 |
| 8.2        | Percolation of level sets in random fields     |   216 |
| 8.3        | Dependent Boolean and random-connection models |   221 |
| 8.4        | Stationary spanning forests                    |   226 |
| 8.5        | Percolation of Poisson sticks                  |   229 |
| 8.6        | Notes                                          |   232 |
| References | References                                     |   233 |
| Index      | Index                                          |   237 |


<!-- p:7 -->


#### Preface

This is the first book completely devoted to continuum percolation. The idea to write this book came up after we noticed that even specialists working in the larger area of spatial random processes were unaware about the current state of the art of continuum percolation. Although stochastic geometers have extensively studied the Boolean model, which is one of the most common models of continuum percolation, their focus has been on geometric and statistical aspects rather than on percolation-theoretical issues.

Initially, we planned to write a review article, but it became clear very quickly that it would be impossible to cover even the most basic results in such a review. Also it became apparent that it would be impossible to include in one volume all available results of a subject this size and still expanding. Therefore, we decided on a book which would give attention to all major issues and techniques without necessarily pushing them to the frontier of today's knowledge. When there is more to say on a specific subject than is found here, we provide the appropriate references for further reading.

Continuum percolation models are easily described verbally, but unlike discrete percolation models, their formal mathematical construction is not completely straightforward. In fact, many people (the authors included) have been quite careless with these constructions in the literature. The setup we have chosen in this book is probably the simplest rigorous construction which allows us to use all the ergodic theory we want. Perhaps some people will be bothered by the fact that we define ergodicity in terms of discrete group actions rather than as a continuum, but we prefer to avoid measure-theoretical nightmares in a book which is supposed to be on percolation theory and in which ergodicity is just a tool to work with. This rigorous construction is more for the mathematical completeness of the book. The reader may easily understand the book with just the geometric notion of the models in mind.


<!-- p:8 -->


X

If we compare the results in this book to well-known results in discrete percolation models, we can roughly distinguish three classes of results. The first class of results consists of those for which there is a natural analogue in discrete percolation. For this class of results, the reader will notice that there are usually extra technical complications because we work in the continuum. These complications are often topological in nature or have something to do with the dependency structure in the models. As a result, statements are usually not quite the same as their discrete counterpart. Examples in this class are the nontriviality of phase transitions, the RSW lemma, the uniqueness of unbounded components and the equality of certain critical densities in random connection models. The second class of results consists of those whose discrete counterpart is either false or unknown. Examples in this class are the fact that the two most natural critical densities in certain Boolean models are not equal, the possible non-uniqueness of the unbounded component in certain cases and some limit results in continuum fractal percolation. And then, of course, there is a class of results which do not have a discrete analogue at all and which are special features of continuum models. This class, fortunately, is quite large and contains all high-density results like compression and rarefaction, results on the covered volume fraction, continuity of the critical densities when the radii distributions converge weakly in Boolean models, scaling properties and complete coverage results. In discrete models, the 'dual' structure plays an important role and can be described independently of the original structure. In continuum models, the vacancy structure plays a role similar to that of the dual, but the vacancy structure can only be described through the occupancy structure as its complement.

We have tried to make the book as self-contained as possible. It helps if the reader is familiar with discrete percolation theory, but this is not really necessary. The reader should feel comfortable with measure theory and basic probability theory, including branching processes. In order to avoid references scattered throughout the text, we conclude each chapter with notes which contain background information and references to related material.

Finally, we would like to thank Olle Häggström, Remco van der Hofstad, Karin Nelander, Mathew Penrose, Anish Sarkar and Jeffrey Steif for many comments on drafts of this book varying from correcting language to pointing out serious mathematical mistakes. Several visits of Rahul Roy to The Netherlands were partly financed by The Dutch Organisation of Scientific Research (N.W.O.). Ronald Meester would like to thank the people in the Indian Statistical Institute in New Delhi for their hospitality during several visits.

October 1995

Ronald Meester Rahul Roy


<!-- p:9 -->


## 1 Introduction

### 1.1 Motivation for continuum models

Many phenomena in physics, chemistry and biology can be modelled by spatial random processes where the randomness is in the geometry of the space rather than in the random behaviour or motion of an object in a deterministic setting. As typical examples of the phenomena we have in mind, consider the spread of a disease in an orchard where the trees are arranged in a grid, and where the disease spreads from an infected tree to its neighbouring trees. In this example, the owner of the orchard is interested in the probability that a particular disease will eventually kill all the trees in the orchard. Another example is the process of the ground getting wet during a period of rain. The randomness here is the place where the raindrops fall on the ground and the size of the wetted region per raindrop. Finally, consider the spread of a disease in a forest. The infection is transmitted from one tree to another, which need not be in the vicinity of the infected tree. This is more likely to happen when the trees are closely spaced than when they are far apart, The collection of infected trees forms a random subset of trees in the forest.

Txt t  te  se e e t  us  xt two examples, although the number of raindrops or trees is countable, the position of either is in the continuous space. A rigorous mathematical model to describe the first example is the standard discrete percolation model. This model has been studied extensively in the last three decades and an excellent reference on the mathematical aspects of this model is the book by Grimmett (1989). The second and third examples are usually described by a continuum percolation model; such models are the subject of this book.

Some geometric aspects of the continuum percolation model have been studied in the context of stochastic geometry. In the language of stochastic geometry, the continuum percolation model is usually referred to as a coverage process or a Boolean model.


<!-- p:10 -->


To get an idea of the kind of questions addressed in a percolation-theoretic study, we elaborate the examples of rainfall and the spread of a disease in a forest. Before the rain starts, the ground is assumed to be completely dry. At a point where a raindrop falls, the ground soaks up the water and a circular wet patch is formed. When the first raindrops fall, we see small wet regions inside a large dry region. The wet region grows when more raindrops reach the ground and at some instant, so many raindrops have reached the ground that the picture suddenly changes from wet 'islands' inside a large dry region to dry islands' inside a large wet region. This phenomenon of a sudden drastic change in the global spatial structure is called a phase transition. Typically, the parameter of the model is not the time, but the density of raindrops on the ground. So for instance, we say that the phase transition takes place at a given density of the raindrops, rather than at a given time. The nature of such phase transitions is an  r n s -ee   oes oa in the example of the spread of an infection in a forest, a question of interest is whether the infection of one particular tree may result in the infection being transmitted to a tree far away. This is of course more likely when the density of the trees in the forest is high. Based on the density of the trees, a phase transition formulation may be obtained for this model too.

The focus of this book is on mathematically rigorous results in models of continuum percolation. In this context, we remark that there are many results available in the applied literature which have yet to be mathematically verified.

### 1.2 Discrete percolation

Before we introduce continuum percolation models we present a short treatment of discrete models. There are several reasons for doing this. First, independent percolation on the integer lattice (to be defined below) was the first percolation model studied and many of the ideas in the theory of this model can be used in the study of continuum models as well; many of the results in the continuum are analogues of discrete results. Secondly, discrete percolation models are in some sense the simplest percolation models to describe and they are suitable for the reader to get a feeling for the types of problems which are involved. Finally, an important technique in the theory of continuum percolation is to approximate the continuum model by a discrete one. In these instances, we need to know something about discrete percolation. Our treatment of discrete percolation is concise, and we refer the reader to Grimmett (1989) for a detailed discussion of discrete percolation. For proofs which are not given here we refer to either Grimmett (1989) or the references in the notes.


<!-- p:11 -->


The setup is as follows. Each element of the d-dimensional integer lattice Za is a vertex, where d ≥ 1. Two vertices at a Euclidean distance one apart are called neighbours. Each pair of neighbours has an edge between them. The graph obtained this way is, with a slight abuse of notation, denoted by Za. An edge is often called a bond, and the set of all bonds is denoted by E. Bonds can be either open or closed. A path is a finite or infinite alternating sequence (z1, e1, z2, e2, . . .) of vertices zi and bonds ei such that zi ≠ zj and ei ≠ ej whenever i ≠ j and such that e is the bond between the neighbours z and zi+ 1, for all i. The length of a path is the number of bonds it contains. A circuit is a finite path, the only difference being that it starts and ends at the same vertex. An open (closed) path is a path whose bonds are all open (closed). Two vertices are said to be connected if there is a finite open path from one to the other. An open cluster is a set of connected vertices which is maximal with respect to this property. Of course, clusters can be either finite or infinite. The open cluster containing the origin is denoted by C(0).

Next we introduce probability. For 0 ≤ p ≤ 1, we equip the space Ω = {0, 1}E with the natural product measure Pp, which is defined via Pp(ω(e) = 1) = p for all e ∈ E. For any realisation ω ∈ Ω, the bond e is said to be open if ω(e) = 1 and closed otherwise. Thus each bond is open with probability p independently of all other bonds.

This is the basic percolation model on the d-dimensional integer lattice. We are interested in unbounded clusters, so here are some natural definitions:

Definition 1.1 The percolation function θ(d) is defined by

$$\theta ^ { ( d ) } ( p ) = P _ { p } ( c a r d ( C ( 0 ) ) = \infty ) .$$

We define the function χ(d) (p) by

$$\chi ^ { ( d ) } ( p ) = E _ { p } ( \text {card} ( C ( 0 ) ) ) ,$$

where Ep is thę expectation operator corresponding to Pp, and card(·) denotes cardinality.

Much of the theory of discrete percolation is concerned with the behaviour of these functions. It seems obvious that both θ(d) and χ(d) are non-decreasing in p. In Chapter 2 it will become clear how to prove this. Based on θ(d) and χ (d) we can define the following critical probabilities:


<!-- p:12 -->


Definition 1.2 The critical probability Pc(d) is defined by

$$p _ { c } ( d ) = \inf \{ p \colon \theta ^ { ( d ) } ( p ) > 0 \} .$$

The critical probability pτ (d) is defined by

$$p _ { T } ( d ) = \inf \{ p \, \colon \, \chi ^ { ( d ) } ( p ) = \infty \} .$$

The two critical probabilities just defined are quite natural. There is a third critical probability which may not seem that natural at first sight but which turns out to be very useful. To define this critical probability, let σp((n1, n2, . .. , nd), i) be the probability that the box [0, n1] × [0, n2] × · .  × [0, nd] contains an open path connecting two opposite faces in the i-th direction.

Definition 1.3 For d ≥ 2, the critical probability ps(d) is defined by

$$p _ { S } ( d ) = \inf \{ p \, \colon \lim _ { n \to \infty } \sup _ { n \to \infty } \sigma _ { p } ( ( n , 3 n , 3 n , \dots , 3 n ) , 1 ) = 0 \} .$$

It is obvious that pr (d) ≤ Pc(d) for all d. It is also clear that pc(1) = pr (1) = 1. Other properties of these critical probabilities are not so easy to obtain:

Theorem 1.1 For all d ≥ 2 we have 0 &lt; pc(d) &lt; 1.

Theorem 1.2 For all d ≥ 2 we have pc(d) = pτ (d) = ps(d).

Actual values are known only in one and two dimensions. It is obvious that Pc(1) = 1 and we also know that pc(2) = 1. This last result is far from trivial! The proof of Theorem 1.2 is very hard and we do not give it here. Theorem 1.1 lies at the very heart of percolation theory. It establishes the existence of a phase transition; i.e. the macroscopic behaviour of the system is very different for values of p below and above the critical probability pc(d). If an infinite cluster exists we say that percolation occurs. The idea behind the proof of Theorem 1.1 will be used a few more times in this book, so we present the proof here:

Proof of Theorem 1.1 The inequality pc(d) &gt; 0 is very simple. Indeed, the number of distinct paths of length n starting at the origin is at most 2d (2d – 1)n-1. (For the first bond, we have 2d possibilities; after that we have at most 2d — 1 possibilities for each new bond because we are not allowed to go back to where we came from.) Each of these paths has probability p" to be open. Thus the expected number of open paths of length n starting at the origin is at ∞ &gt; ud 1-u(I- 2) = udl -(1− 2) &gt; d JIud 1-u(1 - )


<!-- p:13 -->


and hence the expected number of open edges in the component C(0) is finite. This necessarily means that the probability that the component C(0) is finite is equal to 1 and hence θ(d)(p) = 0 if p &lt; (2d − 1)−1. Thus we obtain that Pc(d) ≥ (2d − 1)−1.

For the other inequality we observe that it suffices to prove it for the case d = 2 as pc(d) is clearly non-increasing in d. We need to introduce the dual The set of edges of the dual graph is denoted by E*. Each edge of E now crosses exactly one edge in E*. We declare an edge in E* to be open if and only if the edge it crosses in E is open, and closed otherwise. It is intuitively obvious and a well-known fact in graph theory (Whitney 1933) that there is a closed circuit in Z2* surrounding the origin if and only if C(0) is finite. Now we can perform a counting argument as in the first part of this proof. There are at most n3" distinct circuits of length n surrounding the origin. (This is a rather crude bound: such a circuit has to contain at least one vertex on the x-axis. There are at most n possibilities for this. Starting at this vertex, we have only three possibilities for each new bond.) If for some N &gt; 0 (i) all bonds in [−N, N] × [—N, N] are open and (ii) there is no closed circuit in the dual surrounding [—N, N] × [— N, N], then C (0) is infinite. The event in (i) certainly has positive probability. Furthermore, a circuit surrounding [—N, N] × [—N, N ] has length at least 4N. Hence, if p &gt; 213 a  &gt; d -  c = a e s  s a nd for such p and N, the event in (ii) also has positive probability. Because the events in (i) and (ii) depend on disjoint sets of edges, they are independent, and □

Now that we have established the existence of infinite open clusters for p &gt; Pc, the question arises of just how many infinite open clusters exist. There is a remarkable answer to that question. First observe that the existence of an infinite open cluster does not depend on the state of any finite set of bonds. Hence it follows from Kolmogorov's 0 – 1 law that the existence of an infinite open cluster has probability either zero or one. This, of course, corresponds to the different phases of the percolation model: for p &lt; Pc(d) there is no infinite open cluster a.s. and for p &gt; pc(d), the probability of having an infinite open cluster is positive and hence equal to 1. What happens at the critical probability is known in two dimensions and in dimension higher than 19 only: there is no infinite cluster a.s. in these cases. The remarkable fact referred to above is the following:

Theorem 1.3 There is at most one infinite open cluster a.s.

This result is referred to as the uniqueness of the infinite cluster.


<!-- p:14 -->


We continue the discussion with some basic inequalities which are very useful in the analysis of models of this type. For this, we need to introduce some terminology. There is a natural partial order on Ω = {0, 1}E: ω ≤ ω' if and only if ω(e) ≤ ω'(e) for all e ∈ E. An event A in Ω (we assume that Ω is equipped with the usual Borel σ-field) is said to be increasing if its indicator function is increasing (a real-valued function f on Ω is increasing if f(ω) ≤ f(ω') whenever ω ≤ ω′). An event A is said to be decreasing if its complement is increasing. A typical example of an increasing event is the event that two distinct vertices are connected to each other by an open path.

More generally, we can consider a product space Ωk = {0, 1, ... , k}Σ, where Σ is a countable set, and equip Ωk with product measure Pp = {Po, P1..., pk}2, where Σi=0 Pi = 1. There is a natural partial order onn Ω and the notions of increasing and decreasing events generalise easily. Writing Pp and Ep for probabilities and expectations with respect to p, we have the following important inequality:

Theorem 1.4 (FKG inequality) Let f1 and f2 be both increasing or both decreasing functions. Then

Epfi f2 ≥ Epfi Epf2.

Taking f1 and f2 to be the indicator functions of two increasing (or two decreasing) events A and B, respectively, this inequality reduces to

Pp(A ∩ B) ≥ Pp(A)Pp(B).

This result is not surprising: if there exists an open path connecting two different vertices, another path connecting two other vertices becomes more likely as it can 'use' the bonds of the first path.

Sometimes we need an inequality which goes in the opposite direction. Given the existence of an open path connecting two vertices, we can make it 'harder' for other connections to exist by requiring them to be disjoint from the first connection. This motivates the following definition. Suppose A and B are increasing events which depend only on the state of finitely many bonds. We define A  B to be the set of all configurations ω for which there exist disjoint sets of open bonds with the property that the first such set guarantees the occurrence of A and the second guarantees the occurrence of B. More precisely, A  B is the set of all configurations ω for which there exist finite and disjoint sets of bonds K and KB such that any configuration ω' with ω'(e) = 1, for all e ∈ KA, is in A, and any configuration ω" with ω"(e) = 1, for all e ∈ KB, is in B.


<!-- p:15 -->


Theorem 1.5 (BK inequality) Let A and B be two increasing events which depend on the state of only initely many bonds. Then

$$P _ { p } ( A \Box B ) \leq P _ { p } ( A ) P _ { p } ( B ) .$$

The requirement that A and B are allowed to depend on only finitely many bonds has a technical reason. As we shall see, this will not be important in applications. In the next chapter, we shall derive continuum analogues of Theorems 1.4 and 1.5.

Next, we discuss a method for estimating the rate of change of Pp(A) as a function of p, for increasing events A. Again, we assume that A depends on the state of finitely many edges only. For this, we need yet another definition. A bond ≠         s obtained from ω by changing the value at e; i.e. ωe(e) = 1 – ω(e). In words, a bond is pivotal for A if the occurrence or non-occurrence of A depends crucially on the state of the bond e. It is intuitively clear that the rate of change of Pp(A) as a function of p is related to the number of pivotal bonds.

Theorem 1.6 (Russo's formula) Let A be an increasing event which depends on only finitely many bonds. Then

$$\frac { d } { d p } P _ { p } ( A ) = \sum _ { e \in \mathbb { E } } P _ { p } ( e \, i s \, p i v o t a l \, f o r \, A ) .$$

In the discussion so far, we assumed that bonds were either open or closed with certain probabilities. There was no randomness in the vertices at all. This is the reason that we call this model bond percolation. But we could as well declare vertices instead of edges to be open or closed with probability p and 1 – p respectively, obtaining a site model. The discussion of this site model is similar to the discussion of the bond model above. All results in this section have a natural analogue in the site setting, although the value of the critical probability for independent site percolation on the two-dimensional integer lattice is not known. We shall use these results in the site setting freely with a possible reference to the result in the bond setting.

As mentioned before, discretisation is an important technique in the theory of continuum percolation. Sometimes we end up with a more complicated discrete lattice structure than the nearest-neighbour integer lattice. Also it might be the case that there are different types of sites which are open with different probabilities. Take the d-dimensional integer lattice and draw an edge between any two vertices v and w for which |v − w| ≤ 2L, where L is some positive constant. The graph obtained this way is denoted by GL. We can perform independent site percolation on this new graph, and this leads to the critical values Pc(GL), PT(GL) and ps(GL).


<!-- p:16 -->


This site-percolation model can also be extended to a multi-parametric setting. For example, consider a 'two-layered graph' G(L1,L2) which is defined as follows. We place a copy of GL2 'above'GL,and we draw an edge between v ∈ GL, and w ∈ GL2 if d(v, w) ≤ L1 + L2 (here we abuse notation: v and w are viewed as elements of IRd). Thus a vertex v ∈ GL, and a vertex w ∈ GL2 are adjacent if and only if d(v, w) ≤ L1 + L2. Now we perform multi-parameter independent site percolation on G(L,L2) by declaring a site in GL, to be open with probability p1 and a site in GL2 to be open with probability P2. Rather than a critical point, in this model we can define a region inside the unit square where percolation occurs:

$$p _ { c } ( \mathcal { G } _ { ( L _ { 1 } , L _ { 2 } ) } ) = \{ ( p _ { 1 } , p _ { 2 } ) \, \colon \, P _ { ( p _ { 1 } , p _ { 2 } ) } ( C ( 0 ) = \infty ) > 0 \} ,$$

where C(0) is the union of the open clusters of the origins in GL,and GL2. The regions PT(G(L,L2)) and ps(G(L1,L2)) are defined similarly. The result which we shall need is a generalisation of Theorem 1.2:

Theorem 1.7 In the setting just described it is the case that pc(GL) = pτ(GL) = Ps(GL), and pc(G(L1,L2)) = PT(G(L1,L2)) = Ps(G(L1,L2)).

We end this section with a short discussion on mixed bond/site models. In such a model, both the sites and bonds of the integer lattice are either open or closed with certain probabilities. In its most general form, we have a parameter p and for each bond or vertex, w say, there is a non-decreasing function fw such that w is open with probability fw(p), independently of all other bonds and vertices. Many of the results quoted thus far have their analogues in the mixed setting. In particular, Theorem 1.2 is still true in this setting. Here is a version of Russo's formula for this particular setting which we shall need in Chapter 6:

Theorem 1.8 (Russo's formula) Consider a mixed bond/site model and let A be an increasing event which depends on the state of only finitely many vertices and bonds. Suppose in addition that there are non-decreasing differentiable functions fb, such that the bond or vertex b is open with probability fb(p) independently of all other vertices and bonds. Then

<!-- p:17 -->


### 1.3 Stationary point processes

In the discrete percolation model of the previous section, the vertices of the random graph under consideration were non-random; they were formed by the elements of the d-dimensional integer lattice. In models for continuum percolation, this is no longer the case. The positions of the vertices themselves are random, and they are formed by the occurrences of a stationary point process. In this section, we introduce point processes, derive some basic properties and give some examples.

Oonon  os  pd  ns onos  s oon    s  s course, this is not a very mathematical definition, and we have to make precise what we mean by 'random' here. A natural way to do this is the following. Denote the σ-algebra of Borel sets in IRa by Ba, and denote by N the set of all counting measures on Ba which assign finite measure to bounded Borel sets and for which the measure of a point is at most 1. In this way, N can be identified with the set of all configurations of points in IRa without limit points. We equip N with the σ-algebra N generated by sets of the form

$$\{ n \in N \colon n ( A ) = k \} ,$$

where A ∈ Bd and k is an integer. A point process can now be defined as follows:

Definition 1.4 A point process X is a measurable mapping from a probability space (Ω, F, P) into (N, N).

The distribution of X is the measure μ on N induced by X; i.e. μ is defined through the equation μ(G) = P(X−1(G)), for all G ∈ N. The definition of N allows us to count the number of points in a set A ∈ Ba: the mapping fA : N → N defined by fA(n) = n(A) is measurable by the very construction of N. Hence the composition fA  X : Ω → N is a random variable which we denote by X(A). In words, X(A) represents the random number of points inside A.

In continuum models, we do not have a nice periodic structure as in discrete percolation models. The requirement that the lattice in discrete percolation is periodic is replàced by the requirement that the point process X is stationary. Let T, be the translation in IRd over the vector t: Tt (s) = t + s, for all s ∈ IRd. Then T, induces a transformation S, : N → N through the equation

$$( S _ { t } n ) ( A ) = n ( T _ { t } ^ { - 1 } ( A ) ) ,$$

for all A ∈ Ba . On a higher level, S, induces a transformation Š, on measures

9


<!-- p:18 -->


μ on N through the equation

$$( \tilde { S } _ { t } \mu ) ( G ) = \mu ( S _ { t } ^ { - 1 } G ) ,$$

for all G ∈ N. Now we can define stationarity:

Definition 1.5 The point process X is said to be stationary if its distribution is invariant under Št for all t ∈ IRd.

Definition 1.6 The finite-dimensional (fidi) distributions of a point process X are the joint distributions, for all finite families of bounded Borel sets A1, . . . , Ak, of the random variables X(A1), . . . , X(Ak).

Standard methods (see e.g. Daley and Vere-Jones 1988) show that the distriut n s  e o s  ous s  o onss The fidi distributions are thus one way of specifying a point process. In Chapter 7, we shall introduce a completely different way of specifying a stationary point process, namely via cutting and stacking. For now, we just note that a point process X with distribution μ is stationary if and only if the fidi distributions of μ coincide with the fidi distributions of Š (μ), for all t ∈ Rd.

Percolation theory is concerned with infinite objects and hence only makes sense on infinite graphs. We require therefore that our percolation models are based on point processes with the property that X(Ra) = ∞. This, however, basically is a consequence of stationarity as we now show.

Proposition 1.1 Let X be a stationary point process for which

$$P ( X ( I R ^ { d } ) = 0 ) = 0 .$$

Then P(X(IRd) = ∞) = 1.

Proof Suppose that there exists an integer k such that P(X(IRd) = k) &gt; 0. Then there must also exist an integer b such that

$$P \left ( X ( B _ { b } ) > \frac { 1 } { 2 } k , \, X ( \mathbb { R } ^ { d } \wedge B _ { b } ) < \frac { 1 } { 2 } k \right ) = \epsilon > 0 ,$$

where Bb is the set [-b, b]d. Let r ∈ Zd be a vector with integer-valued coordinates and let br = (br1, . . . , brd). Consider the events

$$E _ { r } = \left \{ X ( T _ { b r } ( B _ { b } ) ) > \frac { 1 } { 2 } k , \, X ( T _ { b r } ( \mathbb { R } ^ { d } \bigvee B _ { b } ) ) < \frac { 1 } { 2 } k \right \} .$$

It follows from the stationarity of X that P(Er) = €, for all r ∈ Zd. But the events E, are disjoint for distinct r, and this is the required contradiction.


<!-- p:19 -->


Before giving some examples of point processes, we state a few definitions.

Definition 1.7 The density of a stationary point process X is defined as E(X([0, 1]d)), where E is the expectation operator corresponding to P.

Definition 1.8 Two point processes X1 and X2 defined on the same probability space are said to be independent if

$$P ( X _ { 1 } ( A _ { 1 } ) & = k _ { 1 } , \dots , X _ { 1 } ( A _ { n } ) = k _ { n } , X _ { 2 } ( B _ { 1 } ) = l _ { 1 } , \dots , X _ { 2 } ( B _ { m } ) = l _ { m } ) \\ & = P ( X _ { 1 } ( A _ { 1 } ) = k _ { 1 } , \dots , X _ { 1 } ( A _ { n } ) = k _ { n } ) \\ & \quad \times P ( X _ { 2 } ( B _ { 1 } ) = l _ { 1 } , \dots , X _ { 2 } ( B _ { m } ) = l _ { m } ) ,$$

for every n, m ≥ 1, l, kj non-negative integers and Borel sets A and B.

Definition 1.9 The superposition of two point processes X1 and X2 defined on the same probability space (Ω, F, P) is the point process X defined by

$$X ( A ) ( \omega ) = X _ { 1 } ( A ) ( \omega ) + X _ { 2 } ( A ) ( \omega ) ,$$

for all Borel sets A. We write X = X1 * X2 or μ = μ1 * μ2, where μ, μ1 and μ2 are the distributions of X, X1 and X2 respectively.

Next we give some examples of point processes.

Example 1.1 Let U be a random d-dimensional vector defined on (Ω, F, P) which is uniformly distributed in [0, 1]a. Identifying a counting measure μ with the set {x ∈ IRd : μ({x}) = 1}, we define a point process X via the equation X(ω) = U (ω) + Zd . Hence we just shift the d-dimensional integer lattice over a random vector, and it is not hard to see, using fidi distributions, that X is stationary.

Ex   s 1  od d  c n o  sa Poisson process with density λ &gt; 0 if (i) and (ii) below are satisfied:

- (i) For mutually disjoint Borel sets A,..., Ak, the random variables X(A1), ..., X(Ak) are mutually independent.
- (ii) For any bounded Borel set A ∈ Bd we have for every k ≥ 0

$$P ( X ( A ) = k ) = e ^ { - \lambda \ell ( A ) } \frac { \lambda ^ { k } \ell ( A ) ^ { k } } { k ! } ,$$

where l(·) denotes Lebesgue measure in Ra.


<!-- p:20 -->


Note that we specified the distribution of a Poisson process by its fidi distributions. Condition (ii) guarantees that a Poisson process is stationary. Also, we have that E(X([0, 1]d)) = λ, and hence the fact that we called λ the density of the process is consistent with Definition 1.7.

Example 1.3 (The non-homogeneous Poisson process) The point process X is said to be a non-homogeneous Poisson process if (i) and (ii) below are satisfied:

- (i) For mutually disjoint Borel sets A1,..., Ak, the random variables X(A1), . . . , X(Ak) are mutually independent.
- (ii) There exists a measurable function Λ : IRd → [0, ∞), the intensity function of the process, such that for any bounded Borel set A ∈ Bd we have

$$P ( X ( A ) = k ) = e ^ { - \int _ { \Lambda } \Lambda ( x ) \, d x } \frac { ( \int _ { \Lambda } \Lambda ( x ) \, d x ) ^ { k } } { k ! } .$$

We obtain a Poisson process by taking Λ(x) ≡ λ. Clearly, this is the only case in which we obtain a stationary process here.

We remark that condition (i) in Example 1.2 and Example 1.3 is in fact redundant. (This is a result of Renyi; see Daley and Vere-Jones 1988, Theorem 2.3.1.) In this book, however, we use the independence property frequently and that is the reason to highlight condition (i) in both examples.

Suppose that we have a sequence of bounded Borel sets An C IRd which increases to A, where we do not require A to be bounded. Obviously, the events {X(An) ≥ k} increase to {X(A) ≥ k} when n → ∞, and hence P(X(An) = k) → P(X(A) = k). It follows from monotone convergence that

$$P ( X ( A ) & = k ) = \lim _ { n \to \infty } P ( X ( A _ { n } ) = k ) \\ & = \lim _ { n \to \infty } e ^ { - \int _ { A _ { n } } \Lambda ( x ) \, d x } \frac { ( \int _ { A _ { n } } \Lambda ( x ) \, d x ) ^ { k } } { k ! } \\ & = e ^ { - \int _ { A } \Lambda ( x ) \, d x } \frac { ( \int _ { A } \Lambda ( x ) \, d x ) ^ { k } } { k ! } , \\ \intertext { c h e r e } \text {there the last expression is to be interpreted as zero when } \intertext { c h e r e } ( A ( x ) \, d x ) = \infty$$

where the last expression is to be interpreted as zero when ∫ Λ(x) dx = ∞.

We end this section with some properties of the Poisson process. This process is of particular interest, and four chapters of this book are concerned with percolation models based on a Poisson process.

In the physics literature, people often use phrases like consider infinitely many points uniformly distributed in space'. In fact, they refer to a Poisson process in such a case, and the property they isolate in that phrase should be interpreted as in the following proposition.


<!-- p:21 -->


Proposition 1.2 Let X be a Poisson process and A be a Borel set with bounded positive Lebesgue measure. Then, for all measurable B ⊂ A, we have

$$P ( X ( B ) = m | \, X ( A ) = m + k ) = \left ( \begin{matrix} m + k \\ m \end{matrix} \right ) \left ( \frac { \ell ( B ) } { \ell ( A ) } \right ) ^ { m } \left ( 1 - \frac { \ell ( B ) } { \ell ( A ) } \right ) ^ { k } .$$

Proof This follows from straightforward calculations.

口

Another useful property of the Poisson process is the following: suppose we condition on the event that there is a point at x, for some x ∈ IRd. The independence property of the Poisson process now implies that, apart from the given point at x, the probabilistic structure of the conditioned process is w     v  id     s on Poisson process, μx for the process conditioned to have a point at x, and δx for the distribution of an independent process having only one point at x a.s., we can write this property as

$$\mu _ { x } = \mu * \delta _ { x } .$$

The distribution μx is called the Palm distribution of μ. For the tedious technical details, we refer to Daley and Vere-Jones (1988). If we condition on the event that there is a point at the origin, we still obtain, apart from that point at the origin, a Poisson process.

The third property we discuss is that the superposition of two independent Poisson processes Xλ, and Xλ2 with density λ1 and λ2, respectively, is again a Poisson process with density λ1 + λ2. The reason for this is that if we take the sum of two independent random variables with Poisson distribution with parameters λ and λ, respectively, we obtain a random variable with Poisson distribution with parameter λ+ λ2. Hence, in the obvious notation:

$$X _ { \lambda _ { 1 } } * X _ { \lambda _ { 2 } } = X _ { \lambda _ { 1 } + \lambda _ { 2 } } .$$

Finally, we show how one can obtain a non-homogeneous Poisson process from an ordinary Poisson process in a probabilistic way. We assume that the probability space is rich enough for our purposes here. Let X be a Poisson process with density λ, and let g : IRd → [0, 1] be a measurable mapping. We consider a realisation X(ω) of X. If there is a point at x, we take the point away with probability 1 – g(x) and leave it where it is with probability g(x), independently of all other points of the Poisson process. The ensuing point process is denoted by Ř. Thus, X is a thinning of the original process X.


<!-- p:22 -->


Proposition 1.3 The point process  is a non-homogeneous Poisson process with intensity function λg.

Proof The independence property is immediate from the construction. The fidi distribution of X can be computed as follows:

$$P ( \tilde { X } ( A ) = k ) = \sum _ { i = k } ^ { \infty } P ( X ( A ) = i ) P ( \tilde { X } ( A ) = k | \, X ( A ) = i ) .$$

We have from Proposition 1.2 that given the event {X(A) = i}, the i points of X in A are uniformly distributed over A. Thus

$$P ( \tilde { X } ( A ) = 1 | \, X ( A ) = 1 ) = \ell ( A ) ^ { - 1 } \int _ { A } g ( x ) \, d x ,$$

and more generally,

$$P ( \tilde { X } ( A ) = k | \, X ( A ) = i ) & = \begin{pmatrix} i \\ \ell ( A ) ^ { - 1 } \int _ { A } g ( x ) \, d x \end{pmatrix} ^ { k } [ 1 - \ell ( A ) ^ { - 1 } \\ & \times \int _ { A } g ( x ) \, d x ] ^ { i - k } .$$

Hence

$$H e n c \\ P ( \tilde { X } ( A ) = k ) & = e ^ { - \lambda \ell ( A ) } \frac { ( \lambda \int _ { A } g ( x ) \, d x ) ^ { k } } { k ! } \times \\ & \times \sum _ { i = k } ^ { \infty } \frac { ( \lambda \ell ( A ) [ 1 - \ell ( A ) ^ { - 1 } \int _ { A } g ( x ) \, d x ] ) ^ { i - k } } { ( i - k ) ! } \\ & = e ^ { - \lambda \ell ( A ) } \frac { ( \lambda \int _ { A } g ( x ) \, d x ) ^ { k } } { k ! } e ^ { \lambda \ell ( A ) ( 1 - \ell ( A ) ^ { - 1 } \int _ { A } g ( x ) \, d x ) } \\ & = \frac { ( \lambda \int _ { A } g ( x ) \, d x ) ^ { k } } { k ! } e ^ { - \lambda \int _ { A } g ( x ) \, d x } .$$

口

Note that if g is a constant function then we obtain a homogeneous Poisson process with lower density than the original process.

### 1.4 The Boolean model

The first model of continuum percolation which we introduce in this chapter is the Poisson blob model, or the Boolean model as we shall call it throughout the book. In this section we give the formal mathematical construction and we fix notation for this model.


<!-- p:23 -->


Figure 1.1. A realisation of a Boolean model; the shaded region is C, the darker shaded region is W, while V is empty here. Finally, x ~ y in A.

Before giving the mathematical details, let us try to say in words what this model is all about. We start with some stationary point process X, as introduced in the previous section. We say that the model is driven by X. Each point of X is the centre of a closed ball (in the usual Euclidean metric) with a random radius in such a way that radii corresponding to different points arc independent of each other and identically distributed. The radii are also independent of X. In this way, the space is partitioned into two regions, the occupied region, which is the region covered by at least one ball, and the vacant region, which is just the complement of the occupied region. (See Figure 1.1.) The occupied region is denoted by C. Both the occupied and vacant regions consist of connected components, and almost all results in this book have to do with these components. The connected components in the occupied region will be called occupied components. Similarly, the connected components in the vacant region are called vacant components. For A C IRd , we denote by W (A) the union of all occupied components which have non-empty intersection with A. When A = {0}, we wit l       et   (}  : e die case of vacancy, all definitions are similar, using the symbol V instead of W. We say that V is the vacant component of the origin. Note that either V or W is cmpty but not both. The ball centred at x is denoted by S(x) or by S(x, r), where r denotes the (random) radius of the ball.


<!-- p:24 -->


If two points x and y are in the same occupied component, we say that they are connected in the occupied region, and we write x  y (or y  x of course). Connectedness in the vacant region is defined similarly, and denoted by x y. If x and y are in the same occupied (vacant) component of C ∩ A (Cc ∩ A) for some A ⊂ IRd, we write x  y in A (x  y in A).

There are various instances in this book where the probability space on which the whole model is defined is important, and the description above does not suffice in such cases. So our first task is to construct the Boolean model on some probability space. In discrete percolation models this is straightforward, but here we have to be careful.

Perhaps the first construction that comes to mind is to order the points of X linearly according to some previously determined rule and to construct on one probability space the point process X and i.i.d. positive random variables Y1, Y2, . .. and construct a realisation by assigning radius Yi to the i-th point of X. The problem with this setup is that the ordering of the points of X is not preserved if we shift the configuration in space, and therefore this construction is not good enough to apply ergodic theorems (see the next chapter).

Another approach is to consider uncountably many random variables {Yx} indexed by IRd and assign radius Yx to the point of X at x if it exists. The problem with this setup is that even the simplest events will not be measurable.

We shall now describe a construction based on only countably many random variables in such a way that we can define shifts. Let X be defined on some probability space (Ω1, F1, P1). Let Ω2 be the product space ∏∈n ∏z∈za[0, ∞) and equip Ω2 with the usual product σ-field and product measure P2 with all marginals being μ, where μ is a probability measure on [0, ∞). An element ω2 ∈ Ω2 is sometimes denoted by ω2(n, z). Finally, we set Ω = Ω1× Ω2 and equip Ω with product measure P = P× P2 and the usual product σ-algebra. A Boolean model is a measurable mapping from Ω into N × Ω2 defined by (ω1, ω2) → (X(ω1), ω2), where N is as defined in Section 1.3. The configuration of balls in space corresponding to (ω1, ω2) is obtained as follows. Consider binary cubes

We call this a binary cube of order n. Each point x ∈ X is contained in a unique binary cube of order n, K(n, z(n, x)) say, and with P1-probability 1, for each point x ∈ X there is a unique smallest number no = no(x) such that K(no, z(no, x)) contains no other points of X. The radius of the ball centred at x is now defined to be ω2(n0, z(no, x)).


<!-- p:25 -->


The product structure of Ω implies that the radii are independent of the point process, and the product structure of Ω2 implies that different points have balls with independent, identically distributed radii. It is natural to denote this model by (X, μ). In most cases, however, we have a certain random variable ρ with distribution μ and we think of this random variable as governing the radii of the balls: the radii of the balls are random and are distributed as ρ. The model is then denoted by (X, ρ). In the case where X is a Poisson process with density λ we shall write P = Pλ = P(λ,ρ) to emphasise the dependence on the parameter. Also, the probability of an event A is denoted by either P(A) or P{A} depending on the circumstances.

Let the unit vectors in IRa be denoted by e1, ... , ed. The translation Te : Rd → IRd defined by x → x + e from the previous section induces a transformation Ue on Ω2 through the equation

$$( U _ { e _ { i } } \omega _ { 2 } ) ( n , z ) = \omega _ { 2 } ( n , z - e _ { i } ) .$$

As before, Se, is defined on Ωvia the equation

$$( S _ { e _ { i } } \omega _ { 1 } ) ( A ) = \omega _ { 1 } ( T _ { e _ { i } } ^ { - 1 } A ) .$$

Hence Te induces a transformation Te on Ω = Ω1× Ω2 defined by

$$\tilde { T } _ { e _ { i } } ( \omega ) = ( S _ { e _ { i } } \omega _ { 1 } , U _ { e _ { i } } \omega _ { 2 } ) .$$

The transformation Īe, corresponds to a translation by the vector e of a configuration of balls in space. As such, it will play a crucial role in the discussion of ergodicity in the next chapter.

In percolation theory, one is mainly interested in unbounded objects. In the present setting, this means that we are interested in unbounded occupied and vacant components. The most basic question one can ask about unbounded components concerns their existence. Given a certain Boolean model (X, ρ), is there a positive probability that the occupied or vacant component of the origin is unbounded? (The fact that we take the origin here is of no importance. From the stationarity of X and the independence of the radii, we cannot distinguish between different points of the space probabilistically.) For a given Boolean model (X, ρ), this question is usually very hard to answer. Instead, one considers a whole family of Boolean models and then proves that certain members of the family do not allow unbounded components, but others do. To whet the reader's pp l a o   e  a o en  dles driven by Poisson processes. A Boolean model driven by a Poisson process with density λ and radius random variable ρ is denoted by (X, ρ, λ), and we call it a Poisson Boolean model. We denote by θρ(λ) = θ(λ) the probability that the origin is an element of an unbounded occupied component. In other words, if d(A) denotes the diameter of a set A C IRd (i.e. d(A) = supx, yeA |x − yl), θ(λ) is the probability that d(W) = ∞. The function θ is called the percolation function. It seems obvious (but try to prove this!) that θ is non-decreasing in λ, and for the moment we assume this. A rigorous proof of this fact using coupling is given in Section 2.2. We can define the critical density λc = λc(ρ) as follows:


<!-- p:26 -->


$$\lambda _ { c } ( \rho ) = \inf \{ \lambda \geq 0 \ \colon \theta _ { \rho } ( \lambda ) > 0 \} .$$

In Chapter 3, we shall prove that λe is non-trivial in all reasonable cases; i.e. λc is strictly positive and finite. This fact is at the heart of percolation theory, and it immediately implies that for λ &gt; λc, unbounded occupied components do indeed exist with positive probability. For λ &lt; λc, the origin has probability zero to be contained in an unbounded occupied component and it follows immediately from the stationarity of the process that so has any other point. But any unbounded occupied component should contain at least one point with rational coordinates of which there are only countably many. Hence, no unbounded occupied components can exist with positive probability for λ &lt; λc. When λ &lt; λc, we say that the system is in the subcritical phase; when λ &gt; λc, the system is said to be supercritical. At the critical density λc the system is said to be critical.

We can define critical densities for unbounded vacant components in a similar manner. We write θ*(λ) for the probability that d(V) = ∞ and the critical density λ* = λ*(ρ) is defined as

$$\lambda _ { c } ^ { * } ( \rho ) = \sup \{ \lambda \geq 0 \ \colon \theta _ { \rho } ^ { * } ( \lambda ) > 0 \} ,$$

In Chapters 3, 4 and 5 the Poisson Boolean model is studied extensively. Boolean models driven by general point processes are treated in Chapter 7.

### 1.5 The random-connection model

Gvn  s at n  n  v  ttss  tng unbounded random objects and this section is concerned with this second model. Again, we first introduce the model in an informal way.

In a Boolean model, the second characteristic of the model (the first is of course the point process X) is a random variable ρ which governs the behaviour of the radii of the balls. In a random-connection model (RCM), the second characteristic is a so-called connection function, which is a non-increasing function from the positive reals into [0, 1]. Given a connection function g, the rule is as follows: for any two points x1 and x2 of the point process X, we insert an edge between x1 and x2 with probability g(|x1 − x2l), independently of all other pairs of points of X, where ·| denotes the usual Euclidean distance. The edge between two points x1 and x2 is denoted by the unordered pair {x1, x2}, and we say that x1 and x2 are the end vertices of {x1, x2}. Two points x and y of the process are said to be connected if there exists a finite sequence (x =: x1, x2, . . . , xn := y) such that the edge {x, x+1} is inserted for all i = 1, . . . , n − 1. A component can now be defined in the usual graph-theoretical way: a component is a set of points such that any two points of this set are connected to each other, and which is maximal with respect to this property. The occupied component of the origin is denoted by W . Of course for W to be non-empty, we need to condition the process to have a point at the origin (see Figure 1.2). This is the natural analogue of the occupied components in Boolean models. There is no analogue of vacant components in random-connection models. We again say that the RCM is driven by X, and the model is denoted by (X, g).


<!-- p:27 -->


Figure 1.2. A realisation of a random-connection model. Here, W contains the points {0, a, b, c}.

We remark that ordinary nearest-neighbour bond percolation on Za is a special case of a random-connection model. To see this, just take the point process of Example 1.1 in Section 1.3; i.e. we shift the d-dimensional integer lattice over a random vector. For the connection function g we can take g(x) = p1{|x|≤1}. In this sense, a random-connection model is more general than ordinary discrete percolation.

Here is a formal mathematical construction of a random-connection model (X, g); it is quite similar to the one of a Boolean model. The notation will o    sl   a    s l  an confusion, as it is always clear which model is under consideration. First we assume that the point process X is defined on a probability space (Ω1, F1, P1). Next we consider a second probability space Ω2 defined as where the product is over all unordered pairs of binary cubes. An element ω2 ∈ Ω2 is written as ω2({(n, z), (m, z′)}). We equip Ω2 with product measure P2 such that all marginals are Lebesgue measure on [0, 1]. As before, we set Ω = Ω1 × Ω2 and we equip Ω with product measure P = P1 × P2. A random-connection model is a measurable mapping from Ω into N × Ω2 defined by (ω1, ω2) → (X(ω1), ω2). The realisation corresponding to (ω1, ω2) is obtained as follows: for any two points x and y of X(ω1), consider the binary cubes K(no(x), z(n0(x), x)) and K(no(y), z(n0(y), y)) defined in the previous section. We connect x and y if and only if ω2({(no(x), z(n0(x), x)), (no(y), z(no(y), y))}) &lt; g(|x − y|). The transformations Uei on Ω2 and τe, on Ω can now be defined similar to (1.7) and (1.9) respectively. The transformation ĩe again corresponds to shifting a realisation of the RCM by the vector e in space.

<!-- p:28 -->


### 1.6 Notes

Continuum percolation models have been extensively studied by physicists. Most of their results are based on Monte Carlo simulations supported by heuristic arguments. The non-triviality of the critical probabilities in Theorem 1.1 goes back to Broadbent and Hammersley (1957). Theorem 1.2 was proved independently by Menshikov (1986) and Aizenman and Barsky (1987). The fact that Pc (2) =  is due to Kesten (1980). The uniqueness of the infinite cluster was proved by Harris (1960) in two dimensions and by Aizenman, Kesten and Newman (1987) in all dimensions. See Meester (1994) for a review on uniqueness in percolation theory. The FKG inequality goes back to Fortuin, Kasteleyn and Ginibre (1971), and the BK inequality was obtained for increasing events by v.d. Berg and Kesten (1985) and in general by Reimer (1994). Russo's formula is due to Russo (1978). It seems that continuum percolation models appeared for the first time in Gilbert (1961), in a very applied fashion.


<!-- p:29 -->


## 2 Basic methods

In this chapter we present a few basic results which will be used repeatedly in the subsequent development of the subject. The last few sections of this chapter will be devoted to obtain some inequalities, which are the continuum version of similar theorems in the discrete percolation models. Some proofs here will be obtained by a suitable discretisation and approximation, thus we will be making use of the corresponding results in discrete percolation. The first two sections are devoted to the concepts of ergodicity, coupling and scaling. The techniques of the proofs are hardly needed in the rest of the book, so it is quite possible to read the statements of the main results and move on to the next chapter.

### 2.1 Ergodicity

In this section, we review some results from classical ergodic theory and apply this theory to stationary point processes. The account on ergodic theory will be fairly short; we restrict ourselves to those results which we need in this book. More information about ergodicity and stationary point processes can be found in the book of Daley and Vere-Jones (1988). For a general account on ergodic theory, we refer to the books by Krengel (1985) and Petersen (1983). lt will be very convenient here to use a slightly different notation than in the rst s ss s s os s  s   o  sosdir viewpoint of measure-preserving transformations (which we introduce in the next paragraph).

Consider a probability space (Ω, F, μ) and let T : Ω → Ω be an invertible measure-preserving (m.p.) transformation, that is, μ(T −-1 F) = μ(F), for all F ∈ F. We call the quadruple (Ω, F, μ, T) an m.p. dynamical system. An element F ∈ F is said to be T-invariant if T−1 F = F. Clearly, the set of all T-invariant sets in F forms a σ-algebra, which we denote by T. The classical one-dimensional ergodic theorem is as follows:


<!-- p:30 -->


Proposition 2.1 Let (Ω, F, μ, T) be an m.p. dynamical system and let f be a μ-integrable real function on Ω. Then

$$\frac { 1 } { n } \sum _ { i = 0 } ^ { n - 1 } f ( T ^ { i } ( \omega ) ) \rightarrow E ( f | \mathcal { I } ) ( \omega ) ,$$

μ-a.s. when n → ∞.

To apply this proposition to stationary one-dimensional point processes, it is convenient to identify the space (N, N) with (Ω, F), so that any element ω ∈ Ω represents a counting measure in Ra and any measure μ on F is identified with a stationary point process. Let T, be the shift by a distance t to the right in IR. Then T, induces a transformation S, : Ω → Ω through the equation

$$( S _ { t } \omega ) ( A ) = \omega ( T _ { t } ^ { - 1 } A ) ,$$

where A is a measurable subset of R.

Lemma 2.1 If μ is stationary, then S, is measure preserving, for all t ∈ IR.

Proof For a bounded measurable set A ⊂ IR and k ∈ N, let F be the set {ω : ω(A) = k} ∈ F. Then we have μ(F) = μ{ω : ω(A) = k} = μ{ω : ω(T,−1(A)) = k} by stationarity of μ. Using (2.2), this is equal to μ{ω : (S,ω)(A) = k} = μ(S,1 F). The desired equality is then also true for sets of the form ∩7=1{ω : ω(A) = k} where Ai is bounded and measurable for all i. Hence we have shown the necessary equality for a generating π -system of F and the proof is complete. □

Taking t = -1 for convenience, we now have an m.p. dynamical system (Ω, F, μ, S\_1) and we can apply (2.1) as follows. Consider a point process with finite density and let f(ω) := ω(0, 1]. Obviously, we have f(S(ω)) = ω(i, i + 1], and hence it follows that ∑i=1 f(S1(ω)) = ω(0, n]. It follows from (2.1) that

$$n ^ { - 1 } \omega ( 0 , n ] \rightarrow E ( f | \mathcal { I } _ { 1 } ) ( \omega ) , \, a . s .$$

for n → ∞, where Z is the σ-algebra of S\_-invariant events. Note that n is an integer here. We can strengthen the conclusion to arbitrary intervals using the following inequalities, where [t 」 denotes the largest integer smaller than or equal to t:


<!-- p:31 -->


$$\frac { \lfloor t \rfloor } { t } \cdot \frac { \omega ( 0 , \lfloor t \rfloor ) } { \lfloor t \rfloor } & \leq \frac { \omega ( 0 , t ) } { t } \leq \frac { \lfloor t + 1 \rfloor } { t } \cdot \frac { \omega ( 0 , \lfloor t + 1 \rfloor ) } { \lfloor t + 1 \rfloor } . \\$$

We conclude that

when t → ∞.

Before we continue with the higher-dimensional case, we make the following remark. Let Z be the σ-algebra of events which are invariant under all translations S, t ∈ IR. Of course we have that T C I1. Now note that for a fixed positive number to we have a.s.

$$\lim _ { t \to \infty } t ^ { - 1 } ( S _ { t _ { 0 } } \omega ) ( 0 , t ] & = \lim _ { t \to \infty } t ^ { - 1 } ( \omega ( - t _ { 0 } , 0 ] + \omega ( 0 , t - t _ { 0 } ) ) \\ & = \lim _ { t \to \infty } t ^ { - 1 } \omega ( 0 , t ] ,$$

so that the right-hand side in (2.4) is invariant under translations and hence measurable with respect to T. But then we have a.s.

$$\begin{array} { r l } { E ( f | \mathcal { I } _ { 1 } ) = E ( E ( f | \mathcal { I } _ { 1 } ) | \mathcal { I } ) } \\ { = E ( f | \mathcal { I } ) , } \end{array}$$

and we finally obtain the important formula

$$t ^ { - 1 } \omega ( 0 , t ] \to E ( f | \mathcal { I } ) ( \omega ) \, a . s .$$

for t → ∞.

Next we consider the higher-dimensional case. As before, (Ω, F, μ) is a probability space, but now we consider d invertible, commuting, measurable and m.p. transformations T1, ... , Td from Ω into itself, where d ≥ 1. Let I1 be the σ-field of events in F which are invariant under all transformations T1, . . ., Td . The composition Ti . . . Tid is a transformation which we denote by T(,..ia). In this way the set {Tz : z ∈ Zd } forms a group and is called a Za -action on (Ω, F, μ). We also say that Za acts on Ω via the transformations T, . . . , Td. The classical higher-dimensional ergodic theorem is as follows:

Proposition 2.2 、 Let (Ω, F, μ) be a probability space and suppose Za acts on Ω via T1, ... , Td (which are supposed to be measure preserving). Let f be a real μ-integrable function on Ω. Then

$$\frac { 1 } { n ^ { d } } \sum _ { i _ { 1 } = 0 } ^ { n - 1 } \cdots \sum _ { i _ { d } = 0 } ^ { n - 1 } f ( T _ { 1 } ^ { i _ { 1 } } \cdots T _ { d } ^ { i _ { d } } ( \omega ) ) \to E ( f | \mathcal { I } _ { 1 } ) ( \omega ) , \ a . s .$$

when n → ∞.

$$t ^ { - 1 } \omega ( 0 , t ) \rightarrow E ( f | \mathcal { I } _ { 1 } ) ( \omega ) \, a . s .$$


<!-- p:32 -->


This proposition may now be applied to d-dimensional stationary point processes with finite density. For this, let x ∈ Ra and let Tx be the translation over the vector x. For ease of notation, we define T to be the shift over the i-th unit vector in IRd and Sx is defined by the higher-dimensional analogue of (2.2). The same reasoning as above yields the higher-dimensional analogue of (2.5):

$$t ^ { - d } \omega ( 0 , t ) ^ { d } \rightarrow E ( f | \mathcal { I } ) ( \omega ) \, a . s .$$

where I is the σ-algebra of events which are invariant under all transformations {Sx : x ∈ IRd}, and f(ω) = ω(0, 1]d.

wu ee  ei, de e e   m  s  s to obtain conclusions in continuous time like (2.5) and (2.6). Point processes are random measures in a continuum, and therefore the most natural ergodic theorems associated with them are ergodic theorems which are concerned with a group of transformations indexed by Rd rather than Zd . An IRd -action {Sx : x ∈ Rd} is a group of invertible, commuting, m.p. transformations acting measurably on a probability space (Ω, F, μ) and indexed by IRd. Our final ergodic theorem is the following:

Proposition 2.3 Let (Ω, F, μ) be a probability space and let {Sx : x ∈ IRd} be an IRd-action on Ω. Let f be a real measurable and μ-integrable function on Ω. Then,

$$\frac { 1 } { t ^ { d } } \int _ { [ 0 , t ] ^ { d } } f ( S _ { x } ( \omega ) ) d x \to E ( f | \mathcal { I } ) ( \omega ) \, a . s .$$

for t → ∞, where I is the σ-algebra of events which are invariant under the whole group {Sx : x ∈ IRd}.

The conditional expectations which appear in all ergodic theorems above may not be so easy to deal with in general. A very important special case occurs when the σ-algebra of invariant events is trivial, i.e. any invariant event has measure either zero or one.

Definition 2.1 An m.p. dynamical system (Ω, F, μ, T) is said to be ergodic if the σ-algebra of T-invariant events is trivial. An IRd-action or Zd -action is said to be ergodic (or to act ergodically) if the σ-algebra of events invariant under the whole group is trivial.

In the rest of this section, Tx is the translation in IRd by the vector x, and Sx is the corresponding operator on the probability space (Ω, F, μ) defined via (2.2).


<!-- p:33 -->


Definition 2.2 A stationary point process μ is said to be ergodic if {Sx : x ∈ Rd} acts ergodically on (Ω, F, μ).

If μ is an ergodic point process, then the σ-algebra of invariant events I in (2.6) is trivial and hence E(f |T) = Ef a.s. and the limit in (2.6) is an a.s. constant. When f (ω) = ω(0, 1]a, this constant is equal to the density of the point process. Hence we can immediately write down the following proposition.

Proposition 2.4 For a stationary ergodic point process with finite density, the average number of points per unit volume in [0, t]a converges for t → ∞ a.s. to the density of the point process.

It is not hard to show, using this proposition and a 'thinning argument', that a corresponding statement holds for infinite-density point processes. In such cases, the limit is infinity a.s.

In general it is very difficult to determine whether or not a given point process is ergodic. The following result can be of some help as it characterises ergodicity.

Proposition 2.5 The group {Sx : x ∈ IRd} acts ergodically on (Ω, F, μ) if and only if, for all E, F ∈ F we have

$$\lim _ { t \to \infty } \frac { 1 } { t ^ { \frac { t } { d } } } \int _ { [ 0 , t ] ^ { d } } \mu ( S _ { x } E \cap F ) d x = \mu ( E ) \mu ( F ) .$$

Proof Suppose that (2.8) holds and let E be an invariant event. This implies that μ(Sx E ∩ E) = μ(E), and it follows from (2.8) that

$$\frac { 1 } { t ^ { d } }$$

for t → ∞. Thus we have μ(E) = (μ(E))2 and we are done.

Conversely, suppose that any invariant event has measure 0 or 1. Then (2.7) lakes the form

$$\omega = \frac { 1 } { t ^ { d } } \int _ { [ 0 , t ] ^ { d } } f ( S _ { x } ( \omega ) ) d x \rightarrow E f , \, a . s .$$

Now take E, F ∈ F and take f(ω) = 1 E(ω) so that Ef = μ(E). Then (2.9) yields

$$\frac { 1 } { t ^ { d } } \int _ { t ( 0 ) , \, t ^ { d } } 1 _ { E } ( S _ { x } ( \omega ) ) d x \rightarrow \mu ( E ) , \, a . s .$$


<!-- p:34 -->


The assertion now follows from the following equalities, using Fubini's theorem, (2.10) and bounded convergence:

$$( 2 . 1 0 ) \, \text { and bounded convergence} \colon \\ & \lim _ { t \to \infty } t ^ { - d } \int _ { [ 0 , t ] ^ { d } } \int _ { F } 1 _ { E } ( S _ { x } ( \omega ) ) d \mu ( \omega ) d x \\ & = \lim _ { t \to \infty } \int _ { F } t ^ { - d } \int _ { [ 0 , t ] ^ { d } } 1 _ { E } ( S _ { x } ( \omega ) ) d x d \mu ( \omega ) \\ & = \int _ { F } \mu ( E ) d \mu ( \omega ) \\ & = \mu ( E ) \mu ( F ) . \\$$

□

This proposition is often used by checking that the group {Sx : x ∈ IRd} satisfies an even stronger property than (2.8), namely the mixing property:

Definition 2.3 An m.p. dynamical system (Ω, F, μ, T) is said to be mixing if for all E, F ∈ F, μ(Tn E ∩ F) − μ(E)μ(F) → 0, for n → ∞. An IRd -action {Sx : x ∈ IRd} is said to be mixing if for all E, F ∈ F we have

$$\mu ( S _ { x } E \cap F ) - \mu ( E ) \mu ( F ) \to 0 ,$$

when |x| → ∞. For a Zd -action the definition is similar.

It is clear from this definition and (2.8) that a mixing point process is also ergodic. It is now easy to prove the following result:

Proposition 2.6 A Poisson point process is ergodic.

Proof We prove the stronger statement that a Poisson process is mixing. When E and F are events which depend only on the realisation of the point process inside a bounded set, then (2.11) follows immediately because of the independence property of the Poisson process. For arbitrary events E and F, one approximates E and F by events which depend only on the realisation of the point process inside a bounded set, and the result follows easily. □

Let μ be a Poisson process with parameter λ. We can now apply Proposition 2.4 to μ and conclude that

$$t ^ { - d } \omega ( 0 , t ) ^ { d } \to \lambda , \text { a.s.}$$

when t → ∞. For the Poisson process, however, we do not really need the ergodic theorem to derive (2.12). The result also follows from the classical strong law of large numbers, because the number of points in disjoint sets is independent.


<!-- p:35 -->


Consider an ergodic point process μ. By definition, this means that any event which is invariant under the whole group of transformations {Sx : x ∈ IRd} has, n  o          son about the question of whether or not a particular transformation Sxo gives rise to an ergodic m.p. dynamical system (Ω, F, μ, Sxo). (Of course, the reverse is much simpler: if Sx0 is ergodic, then the σ-algebra Zx0 of Sx0-invariant events is trivial. The σ -algebra of events invariant under the whole group is contained in Īxo and hence also trivial.) Sometimes we need to find a particular ergodic transformation when the group acts ergodically. For this, we need the following classical result:

Proposition 2.7 Suppose that IRd acts ergodically on a probability space (Ω, F, μ) via the group {Sx : x ∈ IRd}, and suppose that the σ-algebra F is countably generated. Then there exists a countable set of hyperplanes (where a hyperplane is not assumed to contain the origin) such that for all elements x ∈ IRa which are not contained in any of these hyperplanes, the m.p. dynamical system (Ω, F, μ, Sx) is ergodic.

Note that we can safely apply this result to point processes: the σ-algebra F is generated by sets of the form {ω : ω(A) = k}, where A ⊂ IRd is a rectangle with rational coordinates and k an integer. The corresponding problem for mixing point processes is trivial. It follows immediately from Definition 2.3 that for a mixing point process μ, any element x ∈ IRa gives rise to a mixing m.p. dynamical system.

Finally, we discuss the ergodicity of Boolean models and random-connection models. The construction of the Boolean model and the random-connection model is such that it only makes sense to consider translations by integervalued vectors. Therefore a Boolean model is said to be ergodic if the group {Îz : z ∈ Zd } acts ergodically. For a random-connection model, the definition is similar. The following result shows that ergodicity of a point process carries on   oon sn d on osn  oo esn

Proposition 2.8 Suppose X is ergodic. Then any Boolean model (X, ρ) or RCM (X, g) is also ergodic.

I'roof We give the proof for the Boolean model. From Proposition 2.7 we have that there exists a t0 ∈ IRd with |to| = 1 such that (Ω1, F1, P1, St0) is an ergodic m.p. dynamical system. In the construction of the Boolean model, we can rotate the coordinate axes in such a way that to becomes one of the unit vectors. It is therefore no loss of generality to assume that to = ej. It is obvious that (Ω2, F2, P2, Ue1) is a mixing system, and it is a classical result in er    dt (  h   s h e product transformation Že, is ergodic. Hence (Ω, F, P, e1) is an ergodic m.p. dynamical system and it follows that {Īz : z ∈ Zd } acts ergodically. 0


<!-- p:36 -->


We end this section with an application of Proposition 2.8.

Theorem 2.1 Suppose that the Boolean model (X, ρ) or the RCM (X, g) is driven by an ergodic point process X. In the Boolean model, the number of unbounded occupied components is a constant a.s. and the same is true for the number of unbounded vacant components. In the RCM, the number of unbounded components is a constant a.s.

Proof Again, we give the proof in the case of a Boolean model. Denote the (random) number of unbounded occupied (or vacant) components by N. It is clear that the event {N = k} is invariant under the group {Īz : z ∈ Zd}, for all k ≥ 0. This implies, by the ergodicity of the Boolean model, that the event has probability either 0 or 1. As a result, we conclude that N is an a.s. constant (which can be infinity). 0

Note that this result immediately implies that unbounded components exist a.s. in the supercritical regime, because P(N ≥ 1) is positive and there must be some 1 ≤ k ≤ ∞ for which P(N = k) = 1.

### 2.2 Coupling and scaling

In this section we introduce two important concepts in the theory of continuum percolation. As we shall see, coupling and scaling are strongly related to each other.

It is not so easy to give a concise and clear definition of coupling. Maybe one could say that coupling is the construction of different models on the same probability space in some sensible way, in order to compare the two models directly. This 'definition' is somewhat vague, and this is why we think that the best way of introducing coupling is by means of some examples. Let us first give an example which has nothing to do with percolation theory, but which is quite instructive. Suppose there are two players, inevitably called A and B, who each have a coin. The coin of player A has probability PA of heads coming up; oud      d   uo    pose that we are interested in the expected number of tosses needed by either of the two players to see heads five times. It is intuitively clear that the expected number for A is no larger than the expected number for B. It is not hard to prove this by doing the right calculations, but we give a more elegant method based on coupling. Let U, for i = 1, 2, ... , be an i.i.d. sequence of uniform-(0, 1) distributed random variables. We model the experiments above by saying that heads comes up for player A at the i-th toss if and only if Ui ≤ PA. For B the requirement is that U ≤ pB. In this way, the tosses of the players are coupled and no longer independent. This, however, does not affect the expected number we are interested in. It is clear from the construction that player A sees heads five times no later than B surely, and hence the expected number of tosses to see a s    a   o   s s o. The coupling described here enables us to compare different players directly.


<!-- p:37 -->


After this warm-up, we give a percolation application of coupling. We prove the claim made in Chapter 1 that the percolation function θ in the Poisson Boolean model (X, ρ, λ) is non-decreasing in λ, the density of the process.

####### Proposition 2.9 If λ1 ≤ λ2 and ρ1 ≤ ρ2 a.s. then θρ1 (λ1) ≤ θρ2(λ2).

Proof To begin with, let ρ1 = ρ2 = ρ a.s. and consider a Boolean model (X, ρ, λ2). We thin this process as described in Proposition 1.3: each point of X is taken away (together with its associated ball) with probability 1 – λ(λ2)−1. It follows from Proposition 1.3 that the ensuing point process is again Poisson with density λ. We remove all balls centred at the deleted points and leave the other points and balls unchanged. It is easy to see that the ensuing model is a Poisson Boolean model (X, ρ, λ1). However, it is clear from the construction that we have coupled the two processes in such a way that the occupied region in (X, ρ, λ1) is a subset of the occupied region in (X, ρ, λ2). Hence the existence of an unbounded occupied component in (X, ρ, λ1) implies the existence of an unbounded occupied component in (X, ρ, λ2). The case when ρ1 and ρ2 are different is treated similarly. □

Another example of coupling which we shall use frequently is described in Figure 2.1. Here we place a Poisson point process X with density λ. Centred at each point we place two balls, one of radius ρ(ω) and the other of radius aρ(ω). Thus we define two Boolean models (X, ρ, λ) and (X, aρ, λ) on the same probability space and compare them.

Related to the concept of coupling is the concept of scaling. It is again not casy to give a precise definition, but we can say that scaling involves changing the unit of length in the model in order to compare two different percolation processes. It is often used in combination with coupling. An example works mu eu  s beu r p  enep  t t aea e ebt important example.


<!-- p:38 -->


Figure 2.1. Coupling of the models (X, ρ, λ) (solid balls) and (X, aρ, λ) (dashed balls) for a &gt; 1.

Proposition 2.10 Consider Poisson Boolean models in Rd. Let, for r ≥ 0, λc(r) denote the critical density in the case where ρ = r a.s. Then it is the case that

$$\lambda _ { c } ( r _ { 1 } ) r _ { 1 } ^ { d } = \lambda _ { c } ( r _ { 2 } ) r _ { 2 } ^ { d } ,$$

where r1, r2 &gt; 0.

Proof We discuss two approaches. First, consider the Boolean model (X, ρ1, λ), where ρ1 = r1 a.s. This means that the expected number of points of the point process inside the unit cube is equal to λ. Now we rescale the model by doing the following: instead of looking at unit cubes, we tile the space with cubes of side length r1/r2. The volume of such a cube is (r1/r2)a and hence the expected number of points of X inside such a cube is λ(r1/r2)a. Furthermore, the relative length of the radii compared to the side length of the new cubes is equal to r1(r2/r1) = r2. If we declare as our new unit of length the size of the new cubes (= r1 (r2)−1), then we see in fact a Boolean model with density λ(r1/r2)a and where the radii of the balls are equal to r2 a.s.; i.e. we see the model (X, ρ2, λ(r1/r2)d), where of course ρ2 takes the value r2 a.s. Note that we have not changed one single point or ball, we just look at the realisation from a different point of view. It follows that if (X, ρ1, λ) is supercritical, then so is (X, ρ2, λ(r1/r2)d), and if the former is subcritical, so is the latter. Hence, λc(r2) = λc(r1)(r1/r2)d, and we are done.


<!-- p:39 -->


Figure 2.2. Scaling by a factor 2.

The second approach is to consider a realisation of the model (X, ρ1, λ) and apply the transformation x → (r2/r1)x on the d-dimensional space. We then end up with a realisation of a Boolean model where all balls have radius r2 and where the points form a Poisson process with density λ(r1/r2)a (see Figure 2.2). Note that the structure of the configuration is not affected by this transformation: in the new model, the same balls overlap as in the original model. This means that if the first model is subcritical, so is the second and vice versa. The conclusion now follows as before. □

As follows from the proof of Proposition 2.10, the models (X, r1, λ1) and (X, r2, λ2) are related if λ2 = λ1 (r1/r2)d in the sense that the two models can be seen as scaled versions of each other. Any property in one of these models can be reformulated by a suitable scaling in the other model. This property is by no means restricted to Boolean models with fixed-size balls. The proof of the next proposition is similar to the proof of Proposition 2.10 and we omit it.

Proposition 2.11 In any d-dimensional Poisson Boolean model we have, for any a &gt; 0,

and

λc(aρ) = λc(p)a−d.

### 2.3 The FKG inequality

There is a natural definition of increasing and decreasing events in the present continuum setting. Consider two realisations ω and ω' of a Poisson Boolean model. We define a partial ordering '≤'as ω ≤ ω' if and only if every ball S(x, ρ) present in ω is also present in ω'; i.e. ω' can be obtained from ω by adding points (and associated balls).


<!-- p:40 -->


An event A ∈ Ω is said to be increasing (respectively decreasing) if for the indicator function of the event A.

Theorem 2.2 (FKG inequality) If A1 and A2 are both increasing or both decreasing events in a Poisson Boolean model, then P(A1∩ A2) ≥ P(A1) P(A2).

Proof Consider the lattice Ln = (2-"Z)d × (2−" Z). For any k = (k1, . . . , kd) ∈ Zd and s ∈ Z+ let C(k, s) denote the cell {(x, r) ∈ IRd × IR+ : (s − 1)2−n &lt; r ≤ s2−n and (ki − 1)2−n &lt; xi ≤ ki2−n for every i = 1, . .. , d}, where x = (x1, ... , xd). Thus for distinct (k, s), the cells C(k, s) are disjoint and also ∪ C(k, s) = IRd × IR+, where the union is over all k ∈ Zd and s ∈ Z+. Given any cell C = C(k, s), consider the random variable Nn(C) which is defined as the number of Poisson points in ∏=1 ((ki − 1)2−", k2−"] whose associated ball has radius in ((s — 1)2−", s2-"]. Let Fn be the σ-algebra generated by the random variables {N(C) : C is a cell in Ln}. Then for any event A, {E(1 A|Fn), n ≥ 1} is a martingale with respect to Fn whence, by the martingale convergence theorem, we have

$$E ( 1 _ { A } | \mathcal { F } _ { n } ) \rightarrow 1 _ { A } \, a . s . \, \text {as} \, n \rightarrow \infty .$$

For fixed n it is not hard to see that the random variables {N(C)} are all independent. Also, E(1 |Fn)(ω) is a function of {Nn(C)}C. As such, we easily see that if A is an increasing event, then E(1 AlFn) is an increasing function. Thus, for any ω ≤ ω′, E(1 A|Fn)(ω) ≤ E(1 A|Fn)(ω'). Now for two increasing events A1 and A2, we have by the standard FKG inequality (Theorem 1.4),

$$E \{ E ( 1 _ { A _ { 1 } } | \mathcal { F } _ { n } ) E ( 1 _ { A _ { 2 } } | \mathcal { F } _ { n } ) \} & \geq E \{ E ( 1 _ { A _ { 1 } } | \mathcal { F } _ { n } ) \} E \{ E ( 1 _ { A _ { 2 } } | \mathcal { F } _ { n } ) \} \\ & = E ( 1 _ { A _ { 1 } } ) E ( 1 _ { A _ { 2 } } ) .$$

Letting n tend to infinity and applying Lebesgue's dominated convergence theorem, we have from (2.14)

$$E \{ E ( 1 _ { A _ { 1 } } | \mathcal { F } _ { n } ) E ( 1 _ { A _ { 2 } } | \mathcal { F } _ { n } ) \} \to E \{ 1 _ { A _ { 1 } } 1 _ { A _ { 2 } } \} .$$

Thus from (2.15) we have P(A1 ∩ A2) ≥ P(A1) P(A2). This completes the proof of the theorem.

As an application of the FKG inequality we give two examples.


<!-- p:41 -->


Example 2.1 Let B ⊆ IRa be a bounded measurable set containing the origin. For m ≥ 0 consider the following events in the Poisson Boolean model (X, ρ, λ):

$$E = \{ d ( W ( B ) ) \geq m \} , \ \ F = \{ B \subseteq C \} ,$$

where, as defined in Chapter 1, W (B) denotes the union of all occupied components which intersect B, d(W (B)) denotes the diameter sup{d(x, y) : x, y ∈ W (B)} and C the occupied region. Clearly, E and F are both increasing events, so by the FKG inequality we have Pλ(E∩ F) ≥ Pλ(E) Pλ(F). Thus

$$P _ { \lambda } \{ d ( W ) \geq m \} & \geq P _ { \lambda } ( E \cap F ) \\ & \geq R _ { \lambda } ( E ) R _ { \lambda } ( F ) \\ & = C ( \lambda , B ) P _ { \lambda } \{ d ( W ( B ) ) \geq m \} ,$$

where C(λ, B) = Pλ(F) &gt; 0 because B is a bounded region. Thus we have the inequality

$$E _ { \lambda } ( d ( W ( B ) ) ) \leq K ( \lambda , B ) E _ { \lambda } ( d ( W ) ) ,$$

for any bounded region B containing the origin and a positive constant K (λ, B). For the vacant case, a similar application of the FKG inequality yields

$$E _ { \lambda } ( d ( V ( B ) ) ) \leq K ^ { * } ( \lambda , B ) E _ { \lambda } ( d ( V ) ) ,$$

for any bounded region B containing the origin and a positive constant K* (λ, B), where as in Chapter 1, V (B) denotes the union of all vacant components which intersect B and V denotes the vacant component of the origin.

Example 2.2 We first define crossing probabilities of a box. Consider the d-dimensional box B := [0, l1] × · . · × [0, ld] and let B0 (i) := [0, l1] × · . · × [0, li−1] × {0} × [0, li+1] × · · · × [0, ld] and B1 (i) := {0, l1] × · · · × [0, li−1] × {li} × [0, li+1] × · ·· × [0, la] be two faces of the box B. For 1 ≤ i ≤ d, we define the occupied crossing probability in the i-th direction as

$$\sigma ( ( l _ { 1 } , \dots , l _ { d } ) , \lambda , i ) \, \colon = \, P _ { \lambda } \{ \text {there is a continuous curve } \gamma \text { in } B \text { such that } \\ \quad \ \ \ ( i ) \ \gamma \subseteq C \cap B$$

$$( i i ) \, \gamma \cap B _ { 0 } ( i ) \neq \emptyset \, \text {and} \, \gamma \cap B _ { 1 } ( i ) \neq \emptyset \} .$$

In two dimensions, for i = 1, the event in the parentheses in (2.18) is called a left-right (L–R) occupied crossing of the rectangle [0, l1 } × [0, l2], and for i = 2 it is called a top-bottom (T-B) occupied crossing of the rectangle [0, l1] × [0, l2].


<!-- p:42 -->


The vacant crossing probabilities are defined similarly. For 1 ≤ i ≤ d, we define the vacant crossing probability in the i-th direction as

t          t = (  (

- (i) γ*∩C =∅

$$( i i ) \, \gamma ^ { * } \cap B _ { 0 } ( i ) \neq \emptyset \, \text { and } \gamma ^ { * } \cap B _ { 1 } ( i ) \neq \emptyset \} .$$

In two dimensions, for i = 1, the event in the parentheses in (2.19) is called a left-right (L-R) vacant crossing of the rectangle [0, l1] × [0, l2], and for i = 2 it is called a top–bottom (T–B) vacant crossing of the rectangle [0, I1] × [0, l2].

By an application of the FKG inequality we have P{there exists an L-R occupied and a T-B occupied crossing of [0, l1] × [0, l2]} ≥ P{there exists an L-R occupied crossing of [0, l1] × [0, l2]} P{there exists a T–B occupied crossing of [0, l1] × [0, l2]}. A similar statement can be made for vacant crossings and in higher dimensions.

### 2.4 The BK inequality

In this section we shall prove a result which is the analogue of the BK inequality for discrete percolation. The inequality will in some sense be dual to the FKG inequality. In order to state the result we need some definitions. Any ω ∈ Ω corresponds to a countable set of pairs S(ω) = {(x, r)} where the x's denote the points of the point process and r is the radius of the ball centred at x. For any bounded Borel set U C IRd, we define

$$\omega _ { U } = \{ ( x _ { i } , r _ { i } ) \, \colon ( x _ { i } , r _ { i } ) \in S ( \omega ) , x _ { i } \in U \} .$$

The event [ωU] is defined as

$$[ \omega _ { U } ] = \{ \omega ^ { \prime } \ \colon \text { there exists } \omega ^ { \prime \prime } \preceq \omega ^ { \prime } \text { such that } \omega _ { U } ^ { \prime \prime } = \omega _ { U } \} .$$

In words, this is the event that the configuration inside U is larger than ωu. We say that an increasing event A is an event on U if ω ∈ A and ω′ ∈ [ωu] imply that ω' ∈ A. A rational rectangle is an open d-dimensional cube with rational coordinates.

Definition 2.4 Let A and B be two increasing events on a bounded Borel set U. Then

A □ B = {ω : there are disjoint sets V and W such that V and W are finite unions of rational rectangles

and [ων]⊂A, [ωw]⊂B}.

When A  B occurs, we say that A and B occur disjointly.


<!-- p:43 -->


The fact that we only consider unions of rational rectangles in the definition has to do to with measurability problems but is otherwise unimportant. If a set V satisfies [ωv] C A, then any set containing V has the same property, and it is easy to see that there is also a subset of V with the same property. Hence no 'minimal set' with the required properties exists. Note also that this definition of A  B is equivalent to requiring the existence of two disjoint sets of points of the point process (in U) such that any configuration which agrees with ω on the first set of points (including the associated balls) is in A, and any configuration which agrees with ω on the second set of points is in B. Before proceeding we clarify the definition with an example.

Example 2.3 Consider a Boolean model in two dimensions and suppose that the radii are bounded from above by R &gt; 0. Consider a rectangle [0, /1] × [0, l2]. Let A be the event that there is an L-R occupied crossing of the rectangle, and let B be the event that there is an occupied T-B crossing. Then A and B are increasing events on [−R, I1 + R] × [−R, l2 + R], and A □ B is the event that there exist both an L-R crossing and a T-B crossing in such a way that the balls used for the L-R crossing are different than the balls used for the T-B crossing. Note that the balls in one crossing are allowed to (and in this case certainly will) intersect balls in the other crossing.

Theorem 2.3 (BK inequality) Suppose U is a bounded measurable set in Rd. For any two increasing events A and B on U in a Poisson Boolean model we have

$$P ( A \square B ) \leq P ( A ) P ( B ) .$$

The key to the proof of this theorem is an 'exchanging technique'. To explain this, consider two sets U and x + U in Rd, where U is bounded and x is chosen such that the two sets are disjoint. What we want to do is, given a realisation of the Boolean model, exchange the configurations on U and x + U in the sense that all balls centred in U are moved to x + U and vice versa. For our purposes it suffices to restrict ourselves to points x with integer coordinates. For such x we define, for ω ∈ Ω, TU (ω) to be the configuration obtained from ω by (i) translating all points of the point process in U by x and all points in x + U by —x, and (ii) for all points y of the point process in U, we interchange the values of the random variables corresponding to K(no(y), z(no, y)) and K(no(y), z(no, y)) + x, and for all points of the process in U + x we interchange the values of the random variables corresponding to K(no(y), z(no, y)) and K(no(y), z(no, y)) − x. (Recall that K(no(y), z(no, y)) is the binary cube whose associated random variable gives the radius of the ball centered at y.) In the realisation corresponding to ω, this comes down to exchanging points and balls in U and x + U, as anticipated previously. For any event A, TU (A) is defined as {TY (ω) : ω ∈ A}. In words, TY (A) is the event that A would occur if we were to interchange the realisations on U and x + U.


<!-- p:44 -->


The following lemma relates P(A  B) to P(A  TY (B)). The second event can be described as the event that A occurs, and if we were to interchange the realisations on U and x + U, B would occur. Thus the event A can 'use' U, and the event B can 'use' TU (U). This fact should make it easier for A and B to occur disjointly, and the next lemma is the first step in this direction.

Lemma 2.2 Let M be a bounded Borel set, U ⊂ M and x a vector with integer coordinates such that M ∩ (x + U) = ∅. For increasing events A and B on M we have

(()X)d+(())()d

Proof We define, for all bounded Borel sets U, the set ΩU = {ωu : ω ∈ Ω}. For any subset Γ C ΩU, we define [F] = U{y∈Γ}[γ]. For disjoint Borel sets U and U', we write (ωU, ωy) for the element in ΩU∪U which agrees with ω on U and with ω′ on U'. Also, for γ ∈ ΩM and V ⊂ M we write [γ]r to mean [γ′] for any γ′ ∈ Ω with γ = γ. For α ∈ Ω\U let A(α) be the set {σ ∈ Ωυ : there exist V, W ⊂ M, V ∩ W = ∅, W ⊂ M\U such that [(α, σ)]ν ⊂ A and [(α, σ)]w ⊂ B}. (Here we assume again that V and W are finite unions of rational rectangles.) The event B(α) is defined similarly with the roles of A and B interchanged. In words, A(α) is the set of configurations in Ωυ which make A  B to occur in such a way that the set W corresponding to B is outside U. The event B(α) can be described similarly.

Now let ω ∈ A  B. If it is impossible to choose V and W in such a way that they have non-empty intersection with U, then it follows, using the fact that both A and B are increasing events, that X(U) ≥ 2. Hence either ωU ∈ A(ωM\U), ωU ∈ B(ωM\U) or X(U)(ω) ≥ 2. Writing P′ for the conditional probability measure given ωM\U we thus find a.s.

$$P ^ { \prime } ( A \Box B ) & \leq P ^ { \prime } ( [ A ( \omega _ { M } \cup ) ] + P ^ { \prime } ( [ B ( \omega _ { M } \cup ) ] ) \\ & - P ^ { \prime } ( [ A ( \omega _ { M } \cup ) ] \cap [ B ( \omega _ { M } \cup ) ] ) + P ^ { \prime } ( X ( U ) \geq 2 ) \\ & \leq P ^ { \prime } ( [ A ( \omega _ { M } \cup ) ] ) + P ^ { \prime } ( [ B ( \omega _ { M } \cup ) ] ) \\ & - P ^ { \prime } ( [ A ( \omega _ { M } \cup ) ] ) P ^ { \prime } ( [ B ( \omega _ { M } \cup ) ] ) + P ^ { \prime } ( X ( U ) \geq 2 ) , \ ( 2 . 2 0 )$$

where the last inequality follows from the FKG inequality. Note that we can p  nuns  ins n  s ns   ot affected by the conditioning.


<!-- p:45 -->


Furthermore, if ωυ ∈ A(ωm\U) then, according to the definitions, ω ∈ A  B in such a way that the set W corresponding to B can be taken outside U. Hence after interchanging the configurations on U and x + U, B still occurs whence ω ∈ A □ TU (B).

If ωx+U ∈ Tν (B(ωM\U)) then after interchanging U and x + U, B(ωM\U) occurs, which means that after interchanging, A  B occurs in such a way that the set V corresponding to A is outside U. This implies that ω ∈ A  T (B).

From the last two paragraphs it follows that a.s.

$$From the last two paragraphs it follows that a . s . \\ P ^ { \prime } ( A \odot T _ { x } ^ { U } ( B ) ) & \geq \ P ^ { \prime } ( [ A ( \omega _ { M \vee } ) ] ) + P ^ { \prime } ( T _ { x } ^ { U } ( [ B ( \omega _ { M \vee } ) ] ) ) \\ & - P ^ { \prime } ( [ A ( \omega _ { M \vee } ) ] \cap T _ { x } ^ { U } ( [ B ( \omega _ { M \vee } ) ] ) ) \\ & = P ^ { \prime } ( [ A ( \omega _ { M \vee } ) ] ) + P ^ { \prime } ( T _ { x } ^ { U } ( [ B ( \omega _ { M \vee } ) ] ) ) \\ & - P ^ { \prime } ( [ A ( \omega _ { M \vee } ) ] ) P ^ { \prime } ( T _ { x } ^ { U } ( [ B ( \omega _ { M \vee } ) ] ) ) \\ & = P ^ { \prime } ( [ A ( \omega _ { M \vee } ) ] ) + P ^ { \prime } ( [ B ( \omega _ { M \vee } ) ] ) \\ & - P ^ { \prime } ( [ A ( \omega _ { M \vee } ) ] ) P ^ { \prime } ( T _ { x } ^ { U } ( [ B ( \omega _ { M \vee } ) ] ) ) , \ \ ( 2 . 2 1 ) \\ \intertext { w h e r e } \text {where the first equality follows from independence and the second from sta- }$$

-whs o s   oh o  e   oa tionarity. From (2.20) and (2.21) we find

$$P ^ { \prime } ( A \, \Box \, B ) \leq P ^ { \prime } ( A \, \Box \, T _ { x } ^ { U } ( B ) ) + P ^ { \prime } ( X ( U ) \geq 2 )$$

from which the lemma follows after integrating out the conditioning on ω\U.

口

Proof of Theorem 2.3 Using a simple scaling argument, we can assume with-

out loss of generality that A and B are increasing events on the unit cube I = [0, 1]a . Choose any x with integer coordinates such that (x + I) ∩ I = ∅. Fix an integer n and partition I into 2nd binary cubes S1 , . .. , S2nd . Define the events B(k) for k = 1,., 2nd as follows: B(0) = B, B(k+1) = T Sk+1 (B(k), for k = 0, ..., 2nd − 1. Note that with this definition, B(2"d) = Ti(B). Applying Lemma 2.2 2nd times (the k-th time with B replaced by B(k-1), M = U ∪ {x + (S1 ∪ . . . ∪ Sk−1)} and U = Sk), we obtain

$$P ( A \sqcup B ) & = P ( A \sqcup B ^ { ( 0 ) } ) \leq P ( A \sqcup B ^ { ( 1 ) } ) + P ( X ( S _ { 1 } ) \geq 2 ) \\ & \leq \cdots \leq P ( A \sqcup B ^ { ( 2 ^ { n d } ) } ) + 2 ^ { n d } P ( X ( S _ { 1 } ) \geq 2 ) \\ & \leq P ( A ) P ( B ) + 2 ^ { n d } ( \lambda 2 ^ { - n d } ) ^ { 2 } \\$$

$$= P ( A ) P ( B ) + \lambda ^ { 2 } 2 ^ { - n d } .$$

As n is arbitrary, we now take the limit for n → ∞ and the proof is complete.

口


<!-- p:46 -->


We give a typical application of the BK inequality which we shall need later on.

Theorem 2.4 Consider a Poisson Boolean model (X, ρ, λ) where ρ satisfies 0 ≤ ρ ≤ R for some R &lt; ∞. If E(d(W)) &lt; ∞ then there exist constants C1, C2 &gt; 0, depending on λ and the dimension d such that

$$P _ { \lambda } ( 0 \stackrel { \circ } { \sim } ( B _ { m } ) ^ { c } ) \leq C _ { 1 } e ^ { - C _ { 2 } m } .$$

Proof It follows from Example 2.1 that E(d(W (B)) &lt; ∞ for any bounded set B and it will be enough to show that under this condition P(B  (Bm)°) ≤ Ce-C2m, We partition the space with cubes of the form

$$B _ { R } ( z ) = \prod _ { i = 1 } ^ { d } ( 2 R z _ { i } - R , 2 R z _ { i } + R ] ,$$

where z ∈ Zd. Since E(d(W(BR(O))) &lt; ∞ we can choose M so large that E(WM) &lt; 3−d, where WM is the number of cubes BR(z) outside BM which intersect W(BR(O)). Now choose L so large that the set U||z|≥L-1 BR(z) is disjoint from BM, where |z| = max z. Then choose m so large that Bm ⊃ ||z}≤L+1 BR(z). Observe that if {BR(0)  (Bm)c} occurs, then there is some z with ||z|| = L for which {BR(0)  D(z)} and {BR(z)  (Bm)c} occur disjointly, where D(z) is defined to be the set D(z) = ∪llz-z'l=1 BR (z′). It then follows from the BK inequality that

$$\text {follows from the BK inequality that} \\ P ( B _ { R } ( 0 ) \stackrel { \circ } { \hookrightarrow } ( B _ { m } ) ^ { c } ) & \leq \sum _ { \{ z \colon | | z | = L \} } P ( B _ { R } ( 0 ) \stackrel { \circ } { \hookrightarrow } D ( z ) , B _ { R } ( z ) \stackrel { 0 } { \sim } ( B _ { m } ) ^ { c } ) \\ & \leq \max _ { \{ z \colon | | z | = L \} } P ( B _ { R } ( z ) \stackrel { \circ } { \sim } ( B _ { m } ) ^ { c } ) \times \\ & \times \sum _ { \{ z \colon | | z | = L \} } P ( B _ { R } ( 0 ) \stackrel { \circ } { \sim } D ( z ) ) \\ & \leq \max _ { \{ z \colon | | z | = L \} } P ( B _ { R } ( z ) \stackrel { \circ } { \sim } ( B _ { m } ) ^ { c } ) 3 ^ { d } E ( W _ { M } ) , \\ \text {where the last inequality follows from the fact that any cube is contained in at}$$

where the last inequality follows from the fact that any cube is contained in at most 3d sets D(z) with ||z|| = L. It follows that

$$n ) ^ { c } ) \leq \frac { 1 } { 2 } \max _ { \{ z \colon | | z | | = L \} } P ( B _ { R } ( z ) \stackrel { \circ } { \sim } ( B _ { m } ) ^ { c } ) .$$

To estimate the right-hand side of (2.22), suppose that m is so large that {z':l|z-z'l=1.) ⊂ Bm. Then the same argument as above shows that for all z with ||z|| = L,


<!-- p:47 -->


$$P ( B _ { R } ( z ) \stackrel { 0 } { \sim } ( B _ { m } ) ^ { c } ) \leq \frac { 1 } { 2 } \max _ { \{ z ^ { \prime } \colon \| z - z ^ { \prime } \| = L \} } P ( B _ { R } ( z ^ { \prime } ) \stackrel { 0 } { \sim } ( B _ { m } ) ^ { c } ) .$$

Repeating this argument now leads to the desired conclusion.

### 2.5 Notes

Proposition 2.7 is from Pugh and Shub (1971). The FKG inequality for continuum percolation appears in Roy (1988). The proof of the BK inequality given here is due to 'r  s op es        s  ( p rs ses. In Roy and Sarkar (1993), a more restricted version of the BK inequality is proved for certain classes of increasing events. Also in Bezuidenhout and Grimmett (1991), a version of the continuum BK inequality appears. Coupling methods are very old and have become quite popular in recent years. The scaling relations in Proposition 2.1 1 appear in Zuev and Sidorenko (1985).


<!-- p:48 -->


3

## Occupancy in Poisson Boolean models

The percolation-theoretical study of the Boolean model confines itself primarily to the study of the geometric and probabilistic properties of the occupied and vacant clusters. In this chapter we shali study the occupied region in a Poisson Boolean model (X, ρ, λ). Throughout this chapter (X, ρ, λ) will denote a Poisson Boolean model arising from an underlying Poisson point process X of density λ and radius random variable ρ. As usual we shall assume that centred at points x1, x2, ... of X are spheres S(x1), S(x2), ... of radius ρ1, ρ2, ..., respectively, where ρ1, ρ2, ... are independent and identically distributed and are also independent of the underlying point process X. Let ρ denote a random variable independent of ρ1, ρ2, ... and also independent of the process X and whose distribution is identical to that of ρ1. With a slight abuse of notation we shall let Pλ denote the probability measure governing this Poisson Boolean model.

### 3.1 Introduction

It is quite possible that the Boolean model is such that the space IRa is completely covered. To this end, we first give the following elementary result:

Lemma 3.1 Suppose that Eρd &lt; ∞. Then the number of balls which intersect S(O, t) (the ball with radius t centred at the origin) has a Poisson distribution with finite parameter

$$\lambda \int _ { \mathbb { R } ^ { d } } P ( \rho \geq | x | - t ) d x .$$

Proof It follows immediately from Proposition 1.3 and the independence of the radii and the point process that the random variable in question has a Poisson distribution with parameter given by (3.1). We need only show that this parameter is finite. For this, we have, writing Fρ for the distribution function of the radius random variable ρ, and for some positive constants C and C':


<!-- p:49 -->


$$0 \, \text { of the radius random variable $\rho$, and for some positive constants $C$ and $C$} \\ \int _ { \mathbb { R } ^ { d } } P ( \rho \geq | x | - t ) d x & = C \int _ { 0 } ^ { \infty } r ^ { d - 1 } P ( \rho \geq r - t ) d r \\ & = C \int _ { 0 } ^ { \infty } r ^ { d - 1 } \int _ { r - t } ^ { \infty } d F _ { \rho } ( y ) d r \\ & = C \int _ { 0 } ^ { \infty } \int _ { 0 } ^ { y + t } r ^ { d - 1 } d r d F _ { \rho } ( y ) \\ & = C \int _ { 0 } ^ { \infty } ( y + t ) ^ { d } d F _ { \rho } ( y ) < \infty .$$

Taking t = 0, we see that the expected number of balls which intersect the origin is equal to λ ∫R P(ρ ≥ |x)dx. The following argument shows that this is equal to the expected number of Poisson points in the random ball around the origin (assuming that the point process is conditioned to have a point at the origin):

$$\lambda \int _ { \mathbb { R } ^ { d } } P ( \rho \geq | x | ) d x & = E \left ( \sum _ { i } 1 _ { \{ S ( x _ { i } , \rho _ { i } ) \cap \{ 0 \} \neq \emptyset \} } \right ) \\ & = E \left ( \sum _ { i } 1 _ { \{ x _ { i } \in S ( 0 , \rho _ { i } ) \} } \right ) \\ & = E \left ( \sum _ { i } 1 _ { \{ x _ { i } \in S ( 0 , \rho ) \} } \right ) \\ & = \lambda \pi _ { d } E \rho ^ { d } , \\ \intertext { h e r e } \text { there } \pi _ { d } \text { denotes the volume of a 2-dimensional ball with unit radius, and}$$

where πd denotes the volume of a d-dimensional ball with unit radius, and where the last equality follows from conditioning on ρ. We conclude that the probability that the origin is not covered is equal to

$$P ( \mathcal { W } = \emptyset ) = e ^ { - \lambda \pi _ { d } E \rho ^ { d } } .$$

The question of complete coverage is settled in the next proposition.

Proposition 3.1 In a Poisson Boolean model (X, ρ, λ) on IRd, the whole space is covered a.s. if and only if Eρd = ∞.


<!-- p:50 -->


Proof Let us denote the vacant region inside the unit cube [0, 1]a by V'. We then have, by (3.3) and Fubini's theorem,

$$E ( \ell ( V ^ { \prime } ) ) & = E \int _ { [ 0 , 1 ] ^ { d } } 1 _ { \{ x \text { is not covered} \} } \, d x \\ & = e ^ { - \lambda \pi _ { d } E \rho ^ { d } } .$$

Hence if Eρd &lt; ∞, then E(l(V')) &gt; 0 and thus P(l(V′) &gt; 0) &gt; 0. Using Proposition 2.8 and Proposition 2.2 with T the translation over the i-th unit vector and f(ω) = l(V′)(ω), we see that the space is almost surely not completely covered.

Conversely, if Eρd = ∞, then the vacancy in the unit cube has expected Lebesgue measure zero. We distinguish between two possible cases.

Sup ny    y no    y ndny balls a.s. We then cover the space with countably many overlapping open sets of the form z + (0, 1)d =: D(z), for z ∈ Zd . The vacancy inside D(z) is an pd  s e ns n n s un   oz u  n es ty set, and we conclude that the whole space is covered a.s.

Next suppose that there is a t &gt; 0 such that S(0, t) is intersected by infinitely many balls with positive probability. If this happens then there exists a halfline l starting at the origin and a sequence (x1, x2, .. .) of points of the point proh t ss  (  sus (     at s  suothe angle between l and the line passing through the origin and xi tends to zero as i tends to infinity. However, since we must have |x| → ∞ as i → ∞, this implies that there is a half-space which is completely covered by balls. By rotation invariance, all transformations Se, act ergodically. (The notation is as in Chapter 2.) Consider random variables Yn and Zn, n ∈ Z defined as follows: if [0, 1 ]d−1 × [n, n + 1] is completely covered by balls, then Yn = 1, otherwise Yn = 0; if [n, n + 1] × [0, 1 ]d−1 is completely covered then Zn = 1, otherwise Zn = 0. If a half-space is completely covered by balls, then one of the following possibilities occurs:

- (i) Yn = 1 for all n large enough or Yn = 1 for all −n large enough,
- (ii) Zn = 1 for all n large enough or Zn = 1 for all −n large enough.

Suppose (i) occurs. If f := 1 {[0,1]d is completely covered} it follows from the ergodicity of Sed and Proposition 2.1 that Ef = 1, which implies that the unit cube is completely covered almost surely, which in turn implies by stationarity that the whole space is covered by balls a.s. If (ii) occurs the result follows similarly. □


<!-- p:51 -->


In view of this proposition we restrict our study to those random variables ρ for which

$$E \rho ^ { d } < \infty .$$

Suppose (3.4) holds. We define a stochastic process {Xn} as follows:

$$X _ { n } \coloneqq \begin{{cases} 1 & \text {if the point } ( n , 0 , \dots , 0 ) \text { is not covered in } ( X , \rho , \lambda ) , \\ 0 & \text {otherwise.} \end{cases}$$

The translation by the vector e1 is ergodic, and (3.3) together with Proposition 2.1 gives that P(Xn = 1 i.o.) = 1. This yields

Corollary 3.1 If (3.4) holds for a Poisson Boolean model (X, ρ, λ) on Rd, then, for any n ≥ 1, Pλ((Bn)c ⊆ W) = 0.

### 3.2 One-dimensional triviality

It is quite easy to provide a complete description of the percolation phenomenon in one-dimensional Boolean models. Indeed, from Corollary 3.1 we trivially have:

Theorem 3.1 For a Poisson Boolean model (X, ρ, λ) on IR, with ρ satisfying (3.4) for d = 1, unbounded components do not occur a.s.

Thus for a one-dimensional Poisson Boolean model, irrespective of the density of the underlying driving process, either there is complete coverage or no unbounded component, depending on the distribution of the radius random variable.

At this stage of the development of this chapter, we point out the importance of the geometric structure of the random shape at each point of the driving process. Let

$$\mathcal { S } _ { n } = \bigcup _ { i = - n ^ { 2 } } ^ { n ^ { 2 } } \left [ \frac { i } { n } - ( 2 n ^ { 2 } + 1 ) ^ { - 1 } , \ \frac { i } { n } + ( 2 n ^ { 2 } + 1 ) ^ { - 1 } \right ]$$

for n ≥ 1. Let x1, x2, . .. be an enumeration of the points of a Poisson point process on IR and let S(x) = x + S be the shape centred at the point x, where the distribution of S is given by

$$P ( S _ { i } = \mathcal { S } _ { n } ) = \frac { 6 } { \pi } n ^ { - 2 } \ \text { for } n \geq 1 .$$


<!-- p:52 -->


We also assume that S1, S2, . . . are i.i.d. and independent of the driving process. esxt     u     (   ) and hence

$$E \ell ( S ( x _ { i } ) ) = 2 \quad \text {for all } x _ { i } \in X .$$

Note the condition (3.4) for d = 1 for Poisson Boolean models on IR is similar to (3.5) in the sense that both guarantee that the expected Lebesgue measure of the associated shape S(x) is finite. We will show that each random shape S is intersected by infinitely many other random shapes almost surely.

Consider an interval (−a, a) for a &gt; 0. Let N1, N2, ... be i.i.d. random variables defined by Ni = k if and only if Si = xi + Sk for every i ≥ 1 and w x   + e     |x  t     es the smallest integer greater than or equal to x), the shape x + Sk has non-empty intersection with the interval (—a, a). Hence, if

$$P _ { \lambda } ( | x _ { i } | \leq N _ { i } \, i . o . ) = 1 ,$$

then, with probability 1, infinitely many shapes have non-empty intersection with (-a, a). This would, of course, prove our contention that each random shape is intersected by infinitely many random shapes with probability 1. To prove (3.6), we define, for every integer j,

$$E _ { j } \coloneqq \{ x _ { i } \in ( j - 1 , j ) \text { for some } i \geq 1 \text { and } j \leq N _ { i } \} .$$

Now,

$$P _ { \lambda } ( E _ { j } ) & \geq P _ { \lambda } \{ x _ { i } \in ( j - 1 , j ) \text { for some } i \geq 1 \} P _ { \lambda } ( j \leq N _ { i } ) \\ & = ( 1 - \exp ( - \lambda ) ) \frac { 6 } { \pi } \sum _ { n = j } ^ { \infty } n ^ { - 2 } ,$$

so Σj=1 Pλ (Ej) = ∞. Thus by the Borel-Cantelli lemma

$$P _ { \lambda } ( E _ { j } \, i . 0 , ) = 1 .$$

$$P _ { \lambda } ( | x _ { i } | \leq N _ { i } \, \mathbf i . o . ) \geq P _ { \lambda } ( E _ { j } \, \mathbf i . o . ) ,$$

which shows that (3.6) holds.

This example shows that if we allow different shapes then the natural analogue of Theorem 3.1 need not hold.

However,


<!-- p:53 -->


### 3.3 Critical phenomena

In two and higher dimensions, we cannot provide a complete description as in Theorem 3.1.

Theorem 3.2 Let (X, ρ, λ) be a Poisson Boolean model on IRd, for d ≥ 2, with ρ satisfying (3.4). There exists λo &gt; 0 such that the expected number of balls in the component W which contains the origin is finite whenever 0 &lt; λ &lt; λo if and only if

$$E \rho ^ { 2 d } < \infty .$$

Proof Suppose Ep2d &lt; ∞ and first assume that ρ takes only non-negative integer values. We shall employ an argument based on a comparison with a suitable branching process model to provide an upper bound on the expected number of balls contained in a component. The branching process we construct below is of multi-type (see Athreya and Ney 1972, chap. V, for the necessary theory). Suppose there is a ball S of radius i centred at x. Let nj denote the (random) number of balls of radius j which intersect S. Since the Boolean model (X, ρ, λ) can be thought of being the superposition of the independent Boolean models {(Xj, j, λ P(ρ = j)); j = 0, 1, 2, . . .} we have that n1, n2, . . . is an independent sequence of random variables with each n j having a Poisson distribution with mean

$$\mu _ { i , j } & \colon = E _ { \lambda } ( \text {number of balls of radius } j \text { centered in} \\ & \quad \{ z \colon | z - x | \leq i + j \} ) \\ & = \lambda P ( \rho = j ) \pi _ { d } ( i + j ) ^ { d } ,$$

where πd is the d-dimensional volume of a unit ball. In our branching process nj will represent the number of children of x of type j. More specifically, the member of the 0-th generation of the branching process is taken to be the origin. Here we place a ball S of random radius ρo, where ρo and ρ are independent and have the same distribution. Now consider independent Poisson processes X1,0, X1,1, X1,2, ... with Xi, j of density λP(ρ = j), j = 0, 1, 2, .... Let {x1, j,k }, k = 0, 1, 2, . . ., nj, be all the points of X1, j such that a ball of radius j centred at x1, j,k has non-empty intersection with S. The points {x1, j,k; k = 0, 1, 2, . . . , n j, j = 0, 1, 2, . . .} are taken to be members of the first generation, where there are nj members {x1, j,k; k = 0, 1, 2, . . ., nj} of type j. Since the superposition of the processes {X1,j; j ≥ 1} yields a Boolean model with radius random variable ρ, Lemma 3.1 tells us that the total number of balls of all these processes which intersect a given bounded region is finite almost surely. Therefore, ∑j=0 n j is finite a.s. Also, as argued earlier, for all j = 0, 1, 2, . . .,


<!-- p:54 -->


$$E _ { \lambda } ( n _ { j } | \rho _ { 0 } = i ) & = \lambda P ( \rho = j ) \pi _ { d } ( i + j ) ^ { d } \\ & = \mu _ { i , j } .$$

Inductively, let x1, x2, . . . , xm be the members of the n-th generation, Consider the member xl, and suppose it is of type i. The members of the (n + 1)-th generation which are children of xų are obtained by placing independent Poisson processes X0, X1, X2, . . . of densities λ P(ρ = 0), λ P(ρ = 1), λ P(ρ = 2), . . . -res   o e ose o sns osso se e esan dom processes already constructed. The children of x of type j are all those points of the process Xj such that a ball of radius j centred at any of these points will have non-empty intersection with a ball of radius i placed at xγ, where i was assumed to be the type of x. Thus given that xı is of type i, the expected total number of children of x1 of type j, for j = 0, 1, 2, . . . is μi,j·

Let ν(n) be the expected number of members of the n-th generation of type v(n). Also let M be j and let ν(n) denote the infinite vector whose j-th entry is ν the matrix with an infinite number of rows and an infinite number of columns, whose (i, j)-th entry is μi, j. By the theory of multi-type branching processes (see sec. 1.6 of Mode 1971) conditioned on the member of the 0-th generation being of type i, the evolution of the process is given by

$$v ^ { ( n ) } = \text {M} ^ { n } ,$$

where i denotes the infinite unit row vector whose i-th entry is 1 and all other entries are 0.

Let μi,.j (n) denote the (i, j)-th entry of the matrix Mn. Conditioned on the 0-th generation member being of type i, from (3.9) we have that the expected number of members of the n-th generation is

$$\sum _ { j = 0 } ^ { \infty } v _ { j } ^ { ( n ) } = \sum _ { j = 0 } ^ { \infty } \mu _ { i , j } ^ { ( n ) } ,$$

and the total expected number of members, μ, in the entire branching process is

$$\mu _ { t } = \sum _ { n = 0 } ^ { \infty } \sum _ { j = 0 } ^ { \infty } \nu _ { j } ^ { ( n ) } = \sum _ { n = 0 } ^ { \infty } \sum _ { j = 0 } ^ { \infty } \mu _ { i , j } ^ { ( n ) } .$$


<!-- p:55 -->


Now, for all i, j ≥ 1, (i + j)d ≤ 2d[max(i, j)]d ≤ 2did jd; thus, taking C = 2dπd,

$$d , \\ \mu _ { i , j } \leq \begin{cases} C \lambda P ( \rho = j ) i ^ { d } j ^ { d } & \text {for } i , \, j \geq 1 \\ C \lambda P ( \rho = j ) j ^ { d } & \text {for } i = 0 \\ C \lambda P ( \rho = 0 ) i ^ { d } & \text {for } j = 0 . \end{cases}$$

Hence, the (i, j)-th entry μi,) (2) of M2 satisfies, for i, j ≥ 1,

$$\left ( l , j \right ) - \text {in} \, \underset { l = 0 } { \overset { \infty } { \sum } } \mu _ { i , l } \mu _ { l , j } \\ \leq \sum _ { l = 0 } ^ { \infty } C ^ { 2 } \lambda ^ { 2 } i ^ { d } j ^ { d } l ^ { 2 d } P ( \rho = j ) P ( \rho = l ) \\ = C ^ { 2 } \lambda ^ { 2 } i ^ { d } j ^ { d } P ( \rho = j ) E \rho ^ { 2 d } ,$$

while, for i = 0,

and, for j = 0,

$$\mu _ { i , j } ^ { ( 2 ) } \leq C ^ { 2 } \lambda ^ { 2 } j ^ { d } P ( \rho = j ) E \rho ^ { 2 d }$$

$$\mu _ { i , j } ^ { ( 2 ) } \leq C ^ { 2 } \lambda ^ { 2 } i ^ { d } P ( \rho = 0 ) E \rho ^ { 2 d } .$$

Inductively, it is easy to see that

$$\mu _ { i , j } ^ { ( n ) } \leq \begin{cases} ( C \lambda ) ^ { n } ( E \rho ^ { 2 d } ) ^ { n - 1 } i ^ { d } j ^ { d } P ( \rho = j ) & \text { for } i , j \geq 1 \\ ( C \lambda ) ^ { n } ( E \rho ^ { 2 d } ) ^ { n - 1 } j ^ { d } P ( \rho = j ) & \text { for } i = 0 \\ ( C \lambda ) ^ { n } ( E \rho ^ { 2 d } ) ^ { n - 1 } i ^ { d } P ( \rho = 0 ) & \text { for } j = 0 . \end{cases}$$

Since Eρ2d &lt; ∞, we have for i ≥ 1,

$$\mu _ { i } \leq 1 + i ^ { d } \sum _ { n = 1 } ^ { \infty } ( C \lambda ) ^ { n } ( E \rho ^ { 2 d } ) ^ { n - 1 } \left [ P ( \rho = 0 ) + \sum _ { j = 1 } ^ { \infty } j ^ { d } P ( \rho = j ) \right ] \ \ ( 3 . 1 0 )$$

and for i = 0,

$$\mu _ { i } \leq 1 + \sum _ { n = 1 } ^ { \infty } ( C \lambda ) ^ { n } ( E \rho ^ { 2 d } ) ^ { n - 1 } \left [ P ( \rho = 0 ) + \sum _ { j = 1 } ^ { \infty } j ^ { d } P ( \rho = j ) \right ] .$$

Thus if Cλ Eρ2d &lt; 1, then μi &lt; ∞.

Comparing this branching process to the Boolean model, the expected number of balls in the Boolean model which are in the component containing the


<!-- p:56 -->


ball at the origin is at most the total number of members in the branching process. Consequently, if λ ≤ (2aπd Eρ2d)−1, then the expected number of balls comprising a component is finite.

In case the radius random variable takes values other than integers, then we consider the Boolean model (X, ρint, λ), where ρint = [ρ] denotes the smallest integer larger or equal than p. Clearly, Eρ2d &lt;  mplies Eρ2dt &lt; ∞. By a coupling argument, it is immediate that the expected number of balls in a component of the model (Xρint, λ) is at least that in a component of the model (X, ρ, λ), thereby proving the necessary part of the theorem.

To show the sufficiency part of the theorem, we assume that

$$E \rho ^ { 2 d } = \infty ,$$

and prove that in the resulting Boolean model the expected number of balls in a component is infinite for every λ &gt; 0. As before, we assume that the radius random variable ρ takes only non-negative integer values. The general case can be dispensed with by observing that if ρint = Lρ] denotes the largest integer smaller than or equal to ρ, then Eρ2d = ∞ implies that Eρ2nt 2d = ∞, and the expected number of balls in a component of the model (X, ρint, λ) is at most that in a component of the model (X, ρ, λ).

Again, as before, let S be a ball of radius i centred at x and let nj be the (random) number of balls of radius j in the Boolean model (X, ρ, λ) which intersect S. As in the argument leading to (3.8), we have that n1, n2, ... is a sequence of independent random variables with each nj having a Poisson distribution with mean given by (3.8). Let M = max{j : nj &gt; 0} and define M = −1 if n j = 0 for all j ≥ 0. Now

$$\{ M = m \} = \{ n _ { m } > 0 \text { and } n _ { j } = 0 \text { for all } j \geq m + 1 \} ,$$

so the event {M = m} depends only on the Boolean models {(Xj, j, λ P(ρ = j)); j ≥ m}. Thus the events {M = m} and {M ≥ m} are independent of the Boolean models {(Xj, j, λ P(ρ = j)) ; j = 0, 1, 2, . . . , m − 1}. Let k0 = min{ j ≥ 1 : P(ρ = j) &gt; 0}. Given S, a ball of radius i, and given M ≥ k0 + 1, let S' be a ball of radius M which has non-empty intersection with S. Then we have

Eλ (number of balls in the component containing S)

<!-- p:57 -->


The last term can be bounded easily, observing that from the independence property described earlier, given M = m and m ≥ ko + 1, the number of balls of radius ko which intersect S' has a Poisson distribution with mean λP(ρ = k0)πd(m + k0)d. Also,

$$P ( M = m ) & = P ( n _ { m } > 0 ) P ( n _ { j } = 0 \text { for all } j \geq m + 1 ) \\ & = P ( n _ { m } > 0 ) \prod _ { j \geq m + 1 } P ( n _ { j } = 0 ) \\ & \geq ( 1 - \exp ( - \mu _ { i , m } ) ) \exp \left ( - \sum _ { j = m + 1 } ^ { \infty } \mu _ { i , j } \right ) .$$

Thus, from (3.14),

Eλ (number of balls in the component containing S)

$$E _ { \lambda } ( \text {number of balls in the component containing $S$} ) \\ \geq \sum _ { m = k _ { 0 } + 1 } ^ { \infty } ( 1 - \exp ( - \mu _ { i , m } ) ) \exp \left ( - \sum _ { j = m + 1 } ^ { \infty } \mu _ { i , j } \right ) \lambda P ( \rho = k _ { 0 } ) \pi _ { d } ( m + k _ { 0 } ) ^ { d } \\ \geq \sum _ { m = k _ { 0 } + 1 } ^ { \infty } \lambda \pi _ { d } P ( \rho = k _ { 0 } ) ( m + k _ { 0 } ) ^ { d } ( 1 - \exp ( - \mu _ { i , m } ) ) \\ \times \exp \left ( - \sum _ { j = 0 } ^ { \infty } \mu _ { i , j } \right ) .$$

However, since Eρd &lt; ∞,

$$\sum _ { j = 0 } ^ { \infty } \mu _ { i , j } \leq C _ { 1 } ( \lambda ) \sum _ { j = 0 } ^ { \infty } ( i + j ) ^ { d } P ( \rho = j ) < \infty ,$$

and, from (3.16)

$$1 - \exp ( - \mu _ { i , m } ) & \geq \mu _ { i , m } \exp ( - \mu _ { i , m } ) \\ & \geq \lambda P ( \rho = m ) \pi _ { i } m ^ { d } \exp \left ( - \sum _ { j = 0 } ^ { \infty } \mu _ { i , j } \right ) \\ & \geq C _ { 2 } ( \lambda ) m ^ { d } P ( \rho = m ) ,$$

where C1(λ) and C2(λ) are positive constants.


<!-- p:58 -->


In view of our assumption (3.12), combining the bounds obtained in (3.14), (3.15), (3.16) and (3.17), we have

Eλ (number of balls in the component containing S)

$$& \quad \geq C ( \lambda ) \sum _ { m = k _ { 0 } + 1 } ^ { \infty } m ^ { 2 d } P ( \rho = m ) \\ & = \infty$$

where C(λ) is a positive constant. This completes the proof of the theorem.

While (3.7) is necessary and sufficient for the finiteness of the expected number of balls in a component for sufficiently small densities, the following theorem asserts that (3.7) is not necessary for the component to be finite with probability 1.

Theorem 3.3 For a Poisson Boolean model (X, ρ, λ) on IRd, for d ≥ 2, if Ep2d-1 &lt; ∞, then there exists 0 &lt; λ0 such that for all 0 &lt; λ &lt; λo, Pλ(number of balls in any occupied component is finite) = 1.

Proof As in the previous theorem, we shall construct a multi-type branching process to estimate the number of balls in a component. However, we have to be more careful in the construction to enable us to obtain a better estimate. Also as before, it suffices to assume that ρ takes only positive integer values. Indeed, if ρint = [ρ] denotes the smallest integer larger than or equal to ρ,

In the new construction, the children of type j of an initial ball S of type i are all those balls of radius j which have non-empty intersection with S and which are not completely contained in S. The number n j of such balls is clearly a Poisson random variable with mean

$$\mu _ { i , j } \coloneqq \lambda P ( \rho = j ) \pi _ { d } [ ( i + j ) ^ { d } - \{ \max ( 0 , i - j ) \} ^ { d } ] ,$$

and n 1, n2, . . . are independent. Using this construction we will obtain an upper bound for the expected number of balls which make up the boundary of the component of S.

As in the proof of Theorem 3.2, we construct a branching process with this type distribution; the only difference is that the associated ball of a child cannot be completely covered by its immediate forebear. Thus we obtain the equation with v(n) being the expected number of members in the n-th generation of type j in this branching process and μ, j is as defined in (3.18).


<!-- p:59 -->


Now observe that, for i ≤ j,

$$( i + j ) ^ { d } - \max \{ 0 , ( i - j ) \} ^ { d } & = ( i + j ) ^ { d } \\ & \leq 2 ^ { d } j ^ { d }$$

while, for i &gt; j,

$$w h l e , & \text { for } i > j , \\ & ( i + j ) ^ { d } - \max \{ 0 , ( i - j ) \} ^ { d } = \sum _ { k = 0 } ^ { d } \begin{pmatrix} d \\ k \end{pmatrix} i ^ { d - k } j ^ { k } - \sum _ { k = 0 } ^ { d } ( - 1 ) ^ { k } \begin{pmatrix} d \\ k \end{pmatrix} i ^ { d - k } j ^ { k } \\ & \leq \sum _ { k = 1 } ^ { d } 2 \begin{pmatrix} d \\ k \end{pmatrix} i ^ { d - k } j ^ { k } \\ & \leq 2 ^ { d + 1 } i ^ { d - 1 } j ^ { d } , \\ \intertext { w h l e } \text { where the last inequality holds because } \sum _ { k = 1 } ^ { d } k _ { k } = 0 \begin{pmatrix} d \\ 1 \end{pmatrix} = 2 ^ { d } .$$

Using the preceding inequalities, we have from (3.18), for every i, j ≥ 1,

∑k=0(k) where the last inequality holds because (d) = 2d.

$$\mu _ { i , j } \leq C \lambda P ( \rho = j ) i ^ { d - 1 } j ^ { d } ,$$

where C is a positive constant.

Performing a calculation as in the previous theorem, we see that

$$f o r m i g n a c l u dation as in the previous theorem, we see that \\ \mu _ { i , j } ^ { ( 2 ) } = \sum _ { l = 0 } ^ { \infty } \mu _ { i , l } \mu _ { l , j } \\ \leq \sum _ { l = 0 } ^ { \infty } C ^ { 2 } \lambda ^ { 2 } i ^ { d - 1 } j ^ { d / 2 d - 1 } P ( \rho = j ) P ( \rho = l ) \\ = \sum _ { l = 0 } ^ { \infty } C ^ { 2 } \lambda ^ { 2 } i ^ { d - 1 } j ^ { d } P ( \rho = j ) E \rho ^ { 2 d - 1 } , \\ \intertext { a s p l i m e d u c t i o n a g u m e n g t y l e d s }$$

and a simple induction argument yields

$$\mu _ { i , j } ^ { ( n ) } \leq ( C \lambda E \rho ^ { 2 d - 1 } ) ^ { n } P ( \rho = j ) i ^ { d - 1 } j ^ { d } .$$

Note that at this stage of the calculations in the previous theorem, we had the term Eρ2d in (3.10) and (3.11) instead of the term Eρ2d-1 as in (3.19).

Hence, from (3.19),

$$c e , \text { from } ( 3 . 1 9 ) , \\ \mu _ { i } = \sum _ { n = 0 } ^ { \infty } \sum _ { j = 0 } ^ { \infty } \mu _ { i , j } ^ { ( n ) } \\ \leq i ^ { d - 1 } \sum _ { n = 0 } ^ { \infty } ( C \lambda E \rho ^ { 2 d - 1 } ) ^ { n } \sum _ { j = 1 } ^ { \infty } j ^ { d } P ( \rho = j ) . \\ \text {if } C \lambda \, E \rho ^ { 2 d - 1 } \leq 1 \, \text { i.e. if } \lambda \text { is sufficiently small } \text { we have that }$$

Thus, if Cλ Eρ2d-1 &lt; 1, i.e., if λ is sufficiently small, we have that the expected number of balls which make up the boundary of the component of an arbitrary ball of radius i is finite. In particular, the number of boundary balls is finite a.s. From Corollary 3.1 we see that if a component is unbounded, then also the number of boundary balls must be infinite. We conclude that all components are bounded a.s.


<!-- p:60 -->


REMARK: It follows from Theorem 3.3 that if Eρ2d-1 &lt; ∞ then for all positive λ small enough, there are no unbounded occupied components a.s. We complement this result by showing that under the weakest possible condition, namely P(ρ = 0) &lt; 1, we do get unbounded components when λ is large enough. To see this, choose ∈ &gt; 0 so that P(ρ &gt; ε) &gt; ∈ and 1 − ∈ &gt; pc(d) is the critical probability for independent site percolation in d dimensions. Next we choose δ &gt; 0 so small that if we partition the space by cubes with side length δ, any two points in neighbouring cubes are at a distance at most 2e from each other. Next we choose N so large that(1 − (1 − €)~)(1 - ε) &gt; Pc(d), and finally we choose λ so large that the probability to have at least N Poisson points in a cube with side length δ is at least 1 - ε.

We call a cube open if it contains at least one point of the point process with a ball of radius at least e. The choice of our parameters implies that the probability that a cube is open is larger than pc(d). Also, distinct cubes are independently open or closed. Identifying the cubes with the vertices of the d-dimensional integer lattice, we see that the union of all open cubes contains an unbounded component. Thus the Boolean model percolates.

The above two theorems have an interesting consequence:

Corollary 3.2 If the radius random variable ρ of a Poisson Boolean model (X, ρ, λ) on IRd, for d ≥ 2, satisfies

- '∞&gt;1-prd (I)
- (ii) Eρ2d = ∞

then there exists λo such that, for all 0 &lt; λ &lt; λo, with probability 1 no component contains an infinite number of Poisson points, whereas the expected number of Poisson points in the component containing the origin is infinite.

REMARK: Such a dichotomy does not occur in the standard percolation models on the discrete lattice.

### 3.4 Critical densities

In the previous section we noticed that depending on the density of the underlying Poisson process, the Boolean model is either subcritical – that is, the occupied component of the origin contains a finite number of Poisson points almost surely – or supercritical – that is, the occupied component of the origin contains an infinite number of Poisson points with positive probability. We also noticed the existence of two other phases of the Boolean model; the expected number of Poisson points in the occupied component containing the origin is finite in one such phase and infinite in the other phase. To formalise this phase transition we define the critical densities


<!-- p:61 -->


$$\lambda _ { \# } \coloneqq \inf \{ \lambda \colon P _ { \lambda } \{ X ( W ) = \infty \} > 0 \}$$

$$\lambda _ { N } \coloneqq \inf \{ \lambda \colon E _ { \lambda } X ( W ) = \infty \} .$$

For a Poisson Boolean model (X, ρ, λ), Theorem 3.2 states that λN &gt; 0 if and only if Eρ2d &lt; ∞, while if Eρ2d-1 &lt; ∞ then Theorem 3.3 states that λ# &gt; 0. In Corollary 3.2 we showed that if Eρ2d-1 &lt; ∞ and Eρ2d = ∞ then we have 0 = λN &lt; λ#.

In Examples 2.1 and 2.4 , we have used another notion of the size of the component, namely d(W) = sup{d(x, y) : x, y ∈ W}. According to this notion of the size of W, we have the critical densities

$$\lambda _ { c } \coloneqq \inf \{ \lambda \colon P _ { \lambda } \{ d ( \mathcal { W } ) = \infty \} > 0 \}$$

$$\lambda _ { D } \coloneqq \inf \{ \lambda \colon E _ { \lambda } d ( W ) = \infty \} .$$

Another notion of size which is very natural is the Lebesgue measure l(W) of W. This leads to the critical densities

$$\lambda _ { H } \coloneqq \inf \{ \lambda \colon P _ { \lambda } \{ \ell ( W ) = \infty \} > 0 \}$$

$$\lambda _ { T } \coloneqq \inf \{ \lambda \colon E _ { \lambda } \ell ( W ) = \infty \} .$$

We remark here that all these critical densities depend on the underlying distribution of the radius random variable ρ. Thus if there is any scope for confusion we will write λ H (ρ) instead of λ H to emphasise the underlying radius random variable. In a similar fashion, we express the dependence on ρ for the other critical densities whenever there is any chance of confusion. Our first concern is to show that the notion of size does not affect the critical densities when ρ is bounded. We show

Theorem 3.4 In a Poisson Boolean model (X, ρ, λ) with

$$0 < \rho \leq R \, a . s . \, \text {for some } R > 0 ,$$

we have (a) λ# = λc = λH and (b) λN = λD = λτ.

and and


and Proof First suppose λ &gt; λ#. Then, for some δ &gt; 0, Pλ {X(W) = ∞} = δ &gt; 0. Now for every m &gt; 0 the box Bm = [-m, m]a contains at most a finite number of Poisson points a.s., thus Pλ{X(W ∩ Bc) = ∞} = δ &gt; 0. But X(W ∩ Bm) = ∞ implies that X(W ∩ Bc) &gt; 0; i.e., d(W) ≥ m. Hence we have Pλ{d(W) ≥ m} = δ &gt; 0. This being true for all m &gt; 0, we have λ ≥ λc. To show that λ# ≤ λc, we note that d(W) ≤ 2 R X(W), where R is as in (3.26). Thus X(W) &lt; ∞ implies d(W) &lt; ∞. This proves λ# = λc.


<!-- p:62 -->


To show λc = λH, we observe that l(W) ≤ (d(W))d; i.e., if d(W) &lt; ∞, then l(W) &lt; ∞. This shows that λc ≤ λH.

To show the reverse inequality we distinguish between two cases.

CAsE 1: Suppose there exists some η &gt; 0 such that ρ ≥ η a.s. If for some integer N, d(W) ≥ N, then there must be at least N/2R disjoint balls in the component W and so l(W) ≥ (N/2R)2πdηd. Thus λc ≥ λH.

CAsE 2: Suppose there does not exist any η with ρ ≥ η a.s. Since ρ &gt; 0 a.s. and P(ρ = 0) = 0, for any β &gt; 0, we can find 0 &lt; α &lt; β and ro such that

$$P ( \rho < r _ { 0 } ) = \alpha \, < \beta .$$

Nos  &gt;   ( - γ =   e ( =  &lt;   fy (3.27) for this choice of β. Define λ by α = (λ − λ)/λ. Since 0 &lt; α &lt; β, we have λc &lt; λ &lt; λ. Thus, if we set μ = λ - λ, we have

$$P ( \rho < r _ { 0 } ) = \frac { \mu } { \lambda } .$$

Since we shall use the technique of this proof more than once, we present the main idea of the proof before going into the details. We shall decompose the process (X, ρ, λ) into two independent processes such that (X, ρ, λ) is the superposition of these two processes. One of these processes will be chosen such that it has density λ with an associated radius distribution ρ1 which is equivalent in law to ρ given ρ ≥ ro. The other process is now determined from the choice of the first process and, as we shall see shortly, it turns out to be a process with density μ and radius ran              l ow observe that the first process with density λ and radius ρ1 'dominates'a process with density λ and radius ρ, thereby guaranteeing that the first process is supercritical in terms of the diameter of the occupied cluster. However, ρ1 is bounded below by ro &gt; 0 and thus by Case 1, this process is also supercritical in terms of the Lebesgue measure of the occupied cluster, Hence the superposition of this process with any other process will remain supercritical. In particular (X, ρ, λ), which is one such superposition, is supercritical in terms of the volume of the cluster. We now present the details of this idea.


<!-- p:63 -->


Introduce two independent Poisson processes X1 and X2 on the same probability space as our Boolean model with densities λ and μ, respectively. Also, let ρι and ρ2 be two positive random variables with distributions given by

$$P ( \rho _ { 1 } \geq r ) & = P ( \rho \geq r | \rho \geq r _ { 0 } ) \\ & = \begin{cases} \frac { P ( \rho \geq r ) } { P ( \rho \geq r _ { 0 } ) } & \text {for } r \geq r _ { 0 } \\ 1 & \text {for } r < r _ { 0 } , \end{cases} \\$$

$$P ( \rho _ { 2 } \geq r ) & = P ( \rho \geq r | \rho < r _ { 0 } ) \\ & = \begin{cases} \frac { P ( r \leq \rho < r _ { 0 } ) } { P ( \rho < r _ { 0 } ) } & \text {for } r < r _ { 0 } \\ 0 & \text {for } r \geq r _ { 0 } . \end{cases}$$

Now consider the Boolean models (X1, ρ1, λ) and (X2, ρ2, μ). The superposition of these two Boolean models is a Boolean model with density λ + μ = λ. Moreover, for all x, P(x ∈ X1|x ∈ X1 * X2) = (λ−μ)/λ, so the radius random variable associated with the superposed model of density λ is ρ. Let (X', ρ, λ) denote this superposed model. If W1 and W' denote the occupied components of the origin in the Boolean models (X1, ρ1, λ) and (X', ρ, λ), respectively, then

$$W _ { 1 } \subseteq W ^ { \prime } .$$

Now let (X, ρ, λ) be a Poisson Boolean model independent of all the random quantities defined as yet, and let W denote the occupied component of the origin in this Boolean model. From (3.29) we have P(ρ1 ≥ r) ≥ P(ρ ≥ r), which yields, by a coupling argument,

$$P _ { \tilde { \lambda } } ( d ( \overline { W } ) = \infty ) \leq P _ { \tilde { \lambda } } ( d ( W _ { 1 } ) = \infty ) .$$

$$P _ { \widetilde { \lambda } } ( d ( \overline { W } ) = \infty ) > 0 ,$$

so from (3.32) we have Pλ (d(W1) = ∞) &gt; 0. However, from (3.29), ρ1 ≥ ro &gt; 0 a.s., so the first case of this proof applied to the Boolean model (X1, ρ1, λ) yields from (3.33)

$$P _ { \bar { \lambda } } ( \ell ( W _ { 1 } ) = \infty ) > 0 .$$

and

But λ ≥ λc(ρ); i.e., Thus from (3.31), we have Pλ(l(W') = ∞) &gt; 0, i.e., λ ≥ λH. This proves (a) of the theorem.


<!-- p:64 -->


To prove (b), it is easy to observe that the proofs in both the first and second case above go through when we consider λτ instead of λH and λD instead of λc and take expectations instead of probabilities. This yields λD = λτ .

Thus to complete the proof of the theorem we need to show that λN = λτ . For this we observe that l(W) ≤ πd Rd X(W), where πd is, as usual, the d-dimensional volume of a unit ball. Thus if Eλ X(W) &lt; ∞ then Eλ(l(W)) &lt; ∞. This shows that λN ≤ λτ. To show λN ≥ λr, we again consider two cases.

CAsE 1: Suppose there exists η &gt; 0 such that ρ ≥ η a.s. We partition Ra by the integer lattice Za, and let I be a cell in this lattice. Let Xe denote the realisation of the Poisson process X outside the cell I. Let We denote the occupied component containing the origin in the 'Boolean model' (Xμc, ρ, λ). (Note here that if I contains the origin, then for We to be non-empty, there must be a Poisson point outside I whose associated ball covers the origin.) Let δ(x) denote the (random) Euclidean distance from the point x to Wc. For all cells I at a distance at least R from the origin, we have

$$E _ { \lambda } ( X ( \mathbb { W } \cap I ) | ( X _ { I ^ { c } } , \rho , \lambda ) ) \\ = \sum _ { k = 1 } ^ { \infty } k P _ { \lambda } \{ X ( W \cap I ) = k | ( X _ { I ^ { c } } , \rho , \lambda ) \} \\ \leq \sum _ { k = 1 } ^ { \infty } k P _ { \lambda } \{ X ( I ) \geq k \text { and at least one of these } k \text { points} \\ \text { has a ball which intersects } W _ { I ^ { c } } | ( X _ { I ^ { c } } , \rho , \lambda ) \} .$$

Of course, these inequalities and all the subsequent inequalities in this proof which use conditional probability or expectation are almost sure' statements. To calculate the sum in the last inequality of (3.34) we observe that for k ≥ 2λ-1,

$$P _ { \lambda } ( X ( I ) \geq k ) & = e ^ { - \lambda } \sum _ { n = k } ^ { \infty } \frac { \lambda ^ { n } } { n ! } \\ & \leq e ^ { - \lambda } \frac { \lambda ^ { k } } { k ! } \left \{ \frac { 1 } { 1 - \lambda / ( k + 1 ) } \right \} \\ & \leq 2 P ( X ( I ) = k ) .$$


<!-- p:65 -->


Using the independence of the Poisson process X and the radius distribution, we have from (3.34) and (3.35)

$$Using the independence of the Poisson process X and the radius distribution,
we have from (3.34) and (3.35)

        E _ { \lambda } ( X ( W \cap I ) | ( X _ { I } , \rho , \lambda ) )

        \leq \sum _ { k } ^ { \infty } k P ( X ( I ) \geq k ) \left \{ 1 - \left ( \int P ( \rho < \delta ( x _ { 1 } ) ) d x _ { 1 } \right ) \times \cdots \right \}

            \stackrel { \times } { \times } \left ( \int P ( \rho < \delta ( x _ { k } ) ) d x _ { k } \right ) \right \}

        \leq \sum _ { k = 1 } ^ { \lfloor 2 \lambda - 1 \rfloor } k P ( X ( I ) \geq k ) \left \{ k - k \left ( \int P ( \rho < \delta ( x ) ) d x \right ) \right \}

            + \sum _ { k = \lfloor 2 \lambda - 1 \rfloor + 1 } ^ { \infty } 2 k P ( X ( I ) = k ) \left \{ k - k \left ( \int P ( \rho < \delta ( x ) ) d x \right ) \right \} \\        \leq ( 2 \lambda - 1 ) ^ { 2 } \sum _ { k = 1 } ^ { \lfloor 2 \lambda - 1 \rfloor } \left ( \int P ( \rho \geq \delta ( x ) ) d x \right ) \\            + 2 \sum _ { k = \lfloor 2 \lambda - 1 \rfloor + 1 } ^ { \infty } \frac { 1 } { k ! } k ^ { 2 } \lambda ^ { k } \left ( \int P ( \rho > \delta ( x ) ) d x \right ) \\        = C ( \lambda ) \int P ( \rho \geq \delta ( x ) ) d x , \\ \intertext { for some positive constant C ( \lambda ) \ > 0 . Here we have used Proposition 1 . 2 at } the first inequality and the inequality 1 - \prod _ { i = 1 } ^ { n } a _ { i } \leq \sum _ { i = 1 } ^ { n } ( 1 - a _ { i } ) \text { for } 0 \leq \\ a _ { 1 } , a _ { 2 } , \dots , a _ { n } \leq 1 \text { at the second inequality. Since every ball has a radius of at }$$

for some positive constant C(λ) &gt; 0. Here we have used Proposition 1.2 at the first inequality and the inequality 1 − ∏7=1 ai ≤ Σ7=1(1 − a) for 0 ≤ a} , a2, . . . , an ≤ 1 at the second inequality. Since every ball has a radius of at least η, a ball centred in a cell will cover a d-dimensional volume of at least min{1, (1/2d)πd ηd } inside the cell. Thus we have

$$E _ { \lambda } ( \ell ( W \cap I ) | ( X _ { l ^ { c } } , \rho , \lambda ) ) \geq \int _ { I } v \exp ( - \lambda ) \lambda ( P ( \rho \geq \delta ( x ) ) d x , \quad ( 3 . 3 7 )$$

where v = min{ 1, (1/2d)πdηd }. So, from (3.36) and (3.37), for any cell I at a distance at least R from the origin, we obtain

$$E _ { \lambda } ( X ( W \cap I ) | ( X _ { I ^ { c } } , \rho , \lambda ) ) \\ \leq \frac { C ( \lambda ) } { v \exp ( - \lambda ) \lambda } E _ { \lambda } ( \ell ( W \cap I ) | ( X _ { I ^ { c } } , \rho , \lambda ) ) .$$

For a cell / at a distance less than R from the origin we have the trivial bound Eλ X(W ∩ 1) ≤ Eλ X(1) = λ. Now taking expectations on both sides of (3.38)


<!-- p:66 -->


and summing over all cells I of the lattice we have

$$E _ { \lambda } X ( W ) \leq \lambda ( 2 R ) ^ { d } + \frac { C ( \lambda ) } { v \lambda \exp ( - \lambda ) } E \ell ( W ) .$$

This shows that λr ≤ λN in this case.

CAsE 2: Suppose there does not exist any η &gt; 0 such that ρ ≥ η a.s. As in case (ii) of part (a), for λ &lt; λτ and β = (λτ − λ)/λτ, there exist 0 &lt; α &lt; β and ro with P(ρ &lt; ro) = α. Let λ &gt; λ be such that α = (λ − λ)/λ. Since 0 &lt; α &lt; β, we have λ &lt; λ &lt; λτ. Thus, if we set μ = λ − λ,

$$P ( \rho < r _ { 0 } ) = \frac { \mu } { \lambda + \mu } .$$

Now let (X1, ρ1, λ) and (X2, ρ2, μ) be two independent Poisson Boolean models defined on the same probability space, where ρ1 and ρ2 are chosen as in (3.29) and (3.30). As in part (a) a little calculation shows that the superposition of these Boolean models is another Boolean model with density λ and radius random variable ρ. Let (X′, ρ, λ) be this superposed model. If W1 and W′ denote, as before, the occupied components of the origin in (X1, ρ1, λ) and (X′, ρ, λ) respectively, then we have

$$W _ { 1 } \subseteq W ^ { \prime } .$$

Now let (X, ρ, λ) be a Poisson Boolean model independent of all the random quantities defined as yet, and let  denote the occupied component containing the origin in this model. Since λ &lt; λτ(ρ), we have Eλ(e(W)) &lt; ∞. But (X, ρ, λ) and (X′, ρ, λ) are equivalent in law, so Eλ (€(W′)) &lt; ∞. Thus, by (3.40), Eλ(l(W1)) ≤ Eλ(l(W′)) &lt; ∞. But ρ1 ≥ r0 a.s., so by Case 1 we have Eλ X(W) &lt; ∞. Since λ &lt; λ, we have by a coupling argument Eλ X(W) &lt; ∞ and consequently λ ≤ λN. This completes the proof of the theorem.

Before we end this section we introduce another critical density based on the crossing probabilities introduced in Example 2.2. Recall the definition of σ ((n, 3n, . . . , 3n), λ, 1) as the probability of the existence of an occupied crossing in the shortest direction of the rectangle [0, n] × [0, 3n] × ... × [0, 3n]. Since the size of the rectangle increases in n in all directions, we do not have monotonicity of σ ((n, 3n, . . . , 3n), λ, 1) in n. However, we can define the following:

$$\lambda _ { S } = \lambda _ { S } ( \rho ) = \inf \{ \lambda \colon \limsup _ { n \to \infty } \sigma \left ( ( n , 3 n , \dots , 3 n ) , \lambda , 1 \right ) > 0 \} .$$

Proposition 3.2 In any Poisson Boolean model we have λs ≤ λc.


<!-- p:67 -->


Proof For ease of notation we restrict ourselves to two dimensions. The proof for higher dimensions proceeds along the same lines.

Consider the box Bn = [−n, n] × {−n, n]. If λ &gt; λc, then Pλ{d(W) = ∞} &gt; 0 and so at least one of the following events occurs with probability at least P{{d(W) = ∞}:

- (i) there is an L-R occupied crossing of the rectangle [n, 3n] × [-3n, 3n],
- (ii) there is an L-R occupied crossing of the rectangle [—3n, -n]×[-3n, 3n],
- (iii) there is a T-B occupied crossing of the rectangle [—3n, 3n] × [n, 3n],
- (iv) there is a T-B occupied crossing of the rectangle [-3n, 3n] × [-3n, -n].

This implies by translation and rotation invariance of the model that σ ((2n, 6n), λ, 1) &gt;  Pλ (d(W) = ∞). This being true for all n, the proposition follows.

0

### 3.5 Equality of the critical densities

In this section we show that in dimensions 2 or more, if the radius random variable is bounded, then the critical densities λc, λD and λs are all equal. Note that some condition on the radius random variable is necessary, because it follows from Corollary 3.2 that the result cannot be true in general. The proof we present uses a lattice approximation and the scaling relation Proposition 2.11 to show first that in case the balls are all of a fixed size, the equality holds. In case the radius random variable ρ takes on finitely many distinct values, the approximating lattice we need is a multi-parametric one. Finally, a general ρ is approximated from below and above by random variables Un and Vn, each of which take finitely many values and this approximation yields the desired equality.

Theorem 3.5 For a Poisson Boolean model (X, ρ, λ) on Rd, d ≥ 2, with ρ bounded almost surely, we have λc(ρ) = λD(ρ) = λs(ρ).

####### Proof

CAsE 1: First we consider the case when ρ is a fixed constant. It can be easily seen that Proposition 2.11 holds for both λp and λs in addition to that for λc as stated. As such, it suffices to consider ρ ≡ 1 and prove the equality of the critical densities in this case.

Consider a discrete percolation model described as follows. Let V be the set of vertices of the lattice In := ((1/n)Z)d and for a vertex v = (v1, v2, . . . , vd) ∈ Vn, let Kn(v) = [v1 − (1/2n), v1 + (1/2n)) × · · · × [νd − (1/2n), vd + (1/2n)) be the cell containing v. Let Gn be the graph with vertices Vn and edges constructed by joining all pairs of vertices v and w of Vn with d(Kn(v), Kn(w)) ≤ 2, where d(A, B) = inf{d(a, b) : a ∈ A, b ∈ B} for any two regions A, B ⊆ IRa and d(a, b) being the Euclidean distance between a and b. A vertex of this graph is open with probability p and closed with probability 1 – p independently of all other vertices. This graph is clearly isomorphic to the one-parametric site-percolation graph described in the paragraphs preceding Theorem 1.7 for a suitable L. Returning to our graph G, we may define the critical values pc(Gn), Pτ (Gn) and ps(Gn) as in Section 1.2 and Theorem 1.7


<!-- p:68 -->


$$p _ { c } ( \mathcal { G } _ { n } ) = p _ { T } ( \mathcal { G } _ { n } ) = p _ { S } ( \mathcal { G } _ { n } ) .$$

We now incorporate the continuum model (X, 1, λ) in this site-percolation model on G. On IRd we place the graph Gn and for any x ∈ IRd, let v(x) denote the vertex v in Gn such that x ∈ Kn(v). A vertex v is open if X(K(v)) ≥ 1 and it is closed if X(K(v)) = 0; i.e., a vertex v is open if and only if there is at least one Poisson point in the cell containing v. Clearly, Pλ(v is open) = 1 − exp(−λ/nd) = pn(λ) (say) and Pλ(v is closed) = 1 − Pn(λ) for every v ∈ Vn; moreover, v is open or closed independently of other vertices. This is indeed the same site-percolation problem as described in the previous paragraph and is governed by the same set of critical values.

If x and y are two Poisson points of X such that d(x, y) ≤ 2, i.e. S(x, 1) ∩ S(y, 1) ≠ ∅, then either v(x) = v(y) or v(x) and v(y) are adjacent in the sense that there is an edge in G connecting v(x) and v(y). Thus if there is an unbounded occupied cluster in the continuum model, then there is an unbounded open cluster in its approximating site-percolation model on G; i.e., if λ &gt; λc(1), (d  (   s  ( d  ()  ) Since P(λ) is increasing in λ, we can take the inverse of the function p and restate the inequality we just obtained as

$$\lambda _ { c } ( 1 ) \geq p _ { n } ^ { - 1 } ( p _ { H } ( \mathcal { G } _ { n } ) ) .$$

Now we scale the radius of the continuum model by a factor ln := 1 + √d/n and consider the model (X, ln, λ). Notice that if v and w are two adjacent vertices in Gn then sup{d(x, y) : x ∈ Kn(v), y ∈ Kn(w)} ≤ 2 +2√d/n = 2ln, and so if v and w are two adjacent open vertices and x and y are two Poisson points in K (v) and K (w), respectively, then d(x, y) ≤ 2ln. Thus if there is an unbounded open cluster in G, then there is an unbounded occupied cluster in (X, In, λ); i.e., if p '(()d)d  () n  ()  (d)d  ("5)d &lt; d in conjunction with (3.43) we have

$$\lambda _ { c } ( l _ { n } ) \leq p _ { n } ^ { - 1 } ( p _ { I I } ( \mathcal { G } _ { n } ) ) \leq \lambda _ { c } ( 1 ) .$$


<!-- p:69 -->


A similar argument yields

$$\lambda _ { D } ( l _ { n } ) \leq p _ { n } ^ { - 1 } ( p _ { T } ( \mathcal { G } _ { n } ) ) \leq \lambda _ { D } ( 1 )$$

$$\lambda _ { S } ( l _ { n } ) \leq p _ { n } ^ { - 1 } ( p _ { S } ( \mathcal { G } _ { n } ) ) \leq \lambda _ { S } ( 1 ) .$$

Now the scaling relations (Proposition 2.11) and its equivalent version for the other critical densities imply that λc(ln) → λc(1), λτ (ln) → λτ(1) and λs(ln) → λs(1) as n → ∞. The equality of the critical densities now follows from this observation, the equality (3.42) and the inequalities (3.44), (3.45) and (3.46).

CASE 2: Now suppose ρ takes only k distinct values r1, ... , rk. Instead of the single-parameter site-percolation model we considered in the previous case, we now consider a graph Gn which consists of k layers as described in the paragraph preceding Theorem 1.7 for k = 2. The i-th layer consists of the vertices of the lattice ILn and the edges constructed by connecting any pair of vertices v and w in this layer if and only if d(Kn(v), K(w)) ≤ 2r. A vertex v in the i-th layer and a vertex w in the j-th layer (i ≠ j) are connected by an edge if d(Kn (v), Kn(w)) ≤ ri + rj. The graph Gn consists of all the vertices of the different layers and all the edges we have described. We define a sitepercolation model where a vertex v of the i-th layer is open with probability Pi, nh        r  =  +   .   rs As in Theorem 1.7, we get the equality (3.42) of the critical regions described by Pc(Gn), PT (Gn) and ps(Gn).

To connect the continuum model (X, ρ, λ) with this site-percolation model on the graph Gn, we call a vertex v of the i-th layer open if and only if on an embedding of the i-th layer in IRa, the cell K(v) contains at least one Poisson point of X with an associated ball of radius r. A similar application of the scaling relations and comparison with this approximating graph G will yield the desired equality of the critical densities in this case.

CASE 3: Next we consider the case where the support of ρ is contained in an interval [a, a + R] with a, R &gt; 0. Let n &gt; 0 and consider the set of points {a + k2−n, k = 0, . .. , [2" R]} and define

$$k ( n ) = \max _ { 0 \leq k \leq \lfloor 2 ^ { n } R \rfloor } \left \{ \frac { a + ( k + 1 ) 2 ^ { - n } } { a + k 2 ^ { - n } } \right \} .$$

It is easy to see that lim→∞ k(n) = 1. We define, on the same probability space as the Boolean model, the random variable Vn as follows: if

and a + k2−n ≤ ρ &lt; a + (k + 1)2−", then we put Vn = a + k2−n. Note that it follows from these definitions that


<!-- p:70 -->


$$V _ { n } \leq \rho \leq k ( n ) V _ { n } .$$

It follows from (3.47) and Proposition 2.11 that

$$\lambda _ { c } ( k ( n ) V _ { n } ) = \lambda _ { c } ( V _ { n } ) k ( n ) ^ { - d }$$

a s n   (   u s  gs together we find

$$\lambda _ { c } ( V _ { n } ) \geq \lambda _ { c } ( \rho ) \geq k ( n ) ^ { - d } \lambda _ { c } ( V _ { n } ) .$$

In a similar way we obtain

$$\lambda _ { D } ( V _ { n } ) \geq \lambda _ { D } ( \rho ) \geq k ( n ) ^ { - d } \lambda _ { D } ( V _ { n } )$$

$$\lambda _ { S } ( V _ { n } ) \geq \lambda _ { S } ( \rho ) \geq k ( n ) ^ { - d } \lambda _ { S } ( V _ { n } ) .$$

It follows from Case 2 that all critical densities for Vn are equal. Now note that λc(Vn) is non-increasing in n, whence Iim→∞ λc(Vn) exists. Hence we h    = (  ∞←   t  ( ( ( t  f λc(ρ), λD(ρ) and λs(ρ) are equal to lim→∞ λc(Vn). This completes the proof for this case.

CAsE 4: Finally we remove all restrictions on ρ (apart from it being bounded). Let ∈ &gt; 0 and choose a = a(€) so small that P(ρ ≤ a) ≤ €. Let ρa be a random variable with distribution equal to the conditional distribution of ρ conditioned on ρ ≥ a. Similarly, let ρa be a random variable with distribution equal to the conditional distribution of ρ conditioned on ρ &lt; a. Then we have by a simple coupling argument that λc(ρa) ≤ λc(ρ).

Consider two independent models (X1, ρa, λ) and (X2, ρa, λl), where l is chosen such that l(1 + 1)−1 = P(ρ ≤ a); i.e.

$$l = \frac { P ( \rho \leq a ) } { P ( \rho > a ) } \leq \frac { \epsilon } { 1 - \epsilon } .$$

The superposition of the two models is equivalent in law to a process (X, ρ, (      ( + a and hence λ(1 + 1) &gt; λc(ρ); i.e. λc(ρa)(1 + l) ≥ λc(ρ). Hence

$$| \lambda _ { c } ( \rho ) - \lambda _ { c } ( \rho ^ { a } ) | \leq l \lambda _ { c } ( \rho ^ { a } ) \leq \frac { \epsilon } { 1 - \epsilon } \lambda _ { c } ( \rho ) ,$$

and where we have used (3.51). Because λc(ρ) &lt; ∞, we see that λe(ρa(€)) → λc(ρ) when ∈ tends to zero. In a similar fashion, we find that λs(ρa(ε)) → λs(ρ) and λD(ρa(€)) → λD(ρ) when ∈ → 0. From Case 3 it follows that λc(ρa(€)) = λD(ρa(e)) = λs(ρa(€) for all ∈ &gt; 0 and the proof is complete.


<!-- p:71 -->


### 3.6 Uniqueness

We already concluded in Chapter 2 that in the supercritical regime, i.e. if λ &gt; λc(ρ), then unbounded occupied components exist almost surely and that the number of such components is an almost sure constant (which could be infinity). As we shall see now, in the case of a Poisson Boolean model there can be at most one unbounded occupied component a.s. In Chapter 7, we will prove a uniqueness result for Boolean models driven by arbitrary point processes.

Theorem 3.6 In a Poisson Boolean model (X, ρ, λ), there can be at most one unbounded occupied component a.s.

The rest of this section is devoted to a proof of this result. It is quite involved and requires some preliminary results. We start with a combinatorial result which turns out to be of great value and will be used a couple of times throughout the book.

Lemma 3.2 Let S be a set and let R be a non-empty finite subset of S. Suppose that

- (a) for all r ∈ R, we have a family (C(1), C(2), C(3) of disjoint nonempty subsets (which we shall call branches) of S, not containing r, and card(C(i)) ≥ K, for all i and r, where card(·) denotes the cardinality of a set,
- (b) for all r, r' ∈ R, one of the following events occurs, writing Cr for C(i)
- (i) ({r}∪C) ∩({r}∪C) = ∅
- and C() ⊃{r}∪ Cr\C(i).

Then card(S) ≥ K(card(R) + 2) + card(R), where card(·) denotes the cardinality of a set.

Proof First we claim that there exist ro ∈ R and io ∈ {1, 2, 3} such that To see this choose any r1 ∈ R and i1 ∈ {1, 2, 3}. If C(i1) ∩R = Ø we are done. If not, then there is an element r2 ∈ C C(1) )∩R. For this r2 we have that


<!-- p:72 -->


$$r _ { 2 } \in ( \{ r _ { 1 } \} \cup C _ { r _ { 1 } } ) \cap ( \{ r _ { 2 } \} \cup C _ { r _ { 2 } } ) .$$

Hence it must be the case that for some ji and j2 we have

$$\{ r _ { 1 } \} \cup C _ { r _ { 1 } } \rangle C _ { r _ { 1 } } ^ { ( j _ { 1 } ) } \subset C _ { r _ { 2 } } ^ { ( j _ { 2 } ) }$$

$$\{ r _ { 2 } \} \cup C _ { r _ { 2 } } \cup C _ { r _ { 2 } } ^ { ( j _ { 2 } ) } \subset C _ { r _ { 1 } } ^ { ( j _ { 1 } ) } .$$

and and

Using the fact that r2 ∈ C(i1) we conclude from (3.54) that j1 = i1. Hence r1 Cr2\C(2 (2) C This means that there must be some k2 ≠ j2 for which (k2) ). lt follows that Cr222 (k2) ⊃ (i1) ∩ R and this inclusion is strict r2 because r2 is an element of the right-hand side but not of the left-hand side. Hence

$$c a r d ( C _ { r _ { 2 } } ^ { ( k _ { 2 } ) } \cap R ) < c a r d ( C _ { r _ { 1 } } ^ { ( i _ { 1 } ) } \cap R ) .$$

We can repeat this procedure only finitely many times because R is a finite set. It follows that eventually we find ro and io as in (3.53).

Next we remove ro and C (i0) from our set. Thus we put R':= R\{ro} and S′ := S\Ci0 C(o). We claim that for S' and R' properties (a) and (b) still hold, where R is replaced by R' and S by S'. To prove this claim, let r ∈ R'. If Cr0 ∩ Cr = ∅, nothing has been changed in Cr. If not, then there are j and jo such that

$$\{ r _ { 0 } \} \cup C _ { r _ { 0 } } \langle C _ { r _ { 0 } } ^ { ( j _ { 0 } ) } \subset C _ { r } ^ { ( j ) }$$

$$\{ r \} \cup C _ { r } \langle C _ { r } ^ { ( j ) } \subset C _ { r _ { 0 } } ^ { ( j _ { 0 } ) } .$$

The element {r} is still in S' and hence it follows from the last inclusion that t l } o  s   at  t e ≠ te Cro). So for each r ∈ R', only one branch, C) removal of {ro} and C, say, may have been changed into C(1)\ C(). ). If this happens, it implies that C(o (i0) and hence there exist k and ko such that

$$\wedge C _ { r _ { 0 } } ^ { ( k _ { 0 } ) } \subset C _ { r } ^ { ( k ) }$$

$$\{ r \} \cup C _ { r } \langle C _ { r } ^ { ( k ) } \subset C _ { r _ { 0 } } ^ { ( k _ { 0 } ) } .$$

If k ≠ 1 in (3.55), then k0 has to be i0. But then it would follow from (3.56) that {r} has two branches in C (io) , which is impossible by the observation above. ro

and and

and and Thus k = 1 and k0 ≠ io. From (3.55) it then follows that C(1) contains at least and hence even after removing {ro} and C(i) it istill he case that card(C(1) ≥ K. This shows that (a) still holds. The inclusions in (b) remain true because for each r ∈ R' we remove points in at most one branch of r'.


<!-- p:73 -->


Finally, we repeat this procedure of taking away points in R and associated branches not containing points in R until only one element in R remains. This means that we do this step card(R) – 1 times, and each time we take away at least K + 1 points. In the end, we are left with at least 3K + 1 points, namely the remaining point in R together with its branches, each of which still contains at least K points. Hence the original set S contained at least 3K + 1 + (K + 1)(card(R) − 1) points, proving the lemma. 口

Here is the first step towards a uniqueness result:

Proposition 3.3 In a Poisson Boolean model, the number of unbounded occupied components is equal to either zero, one or infinity almost surely.

Proof It follows from the discussion on ergodicity in Chapter 2 that a Poisson Boolean model is ergodic (Proposition 2.6) and that the number of unbounded occupied components in such a model is an a.s. constant (Theorem 2.1).

First, we consider the case where the support of ρ is unbounded. The proof proceeds by contradiction, so we suppose that the number of unbounded occupied components is a.s. equal to K ≥ 2, say. If Bn is the box [-n, n]d as usual, it is clear that for n large enough, there is a positive probability that all K unbounded occupied components have non-empty intersection with Bn and, in addition, X(Bn) ≥ 1. Also, given any enumeration {x1, x2, . . .} of the points of X according to a fixed rule (for instance -th  :  l  t u  u t  vt (l t u bounded components intersect Bn, xm ∈ Bn} has positive probability. (Note that neither n nor m are random.) From the fact that ρ has unbounded support, it follows that the event E* = E ∩ {ρm &gt; 2n√d} also has positive probability, where ρm is the radius of the ball centred at xm. On E*, however, the number of unbounded occupied components is equal to 1, because the ball S(xm, ρm) connects all K formerly unbounded components. This is the desired contradiction. Note that we have not used the fact that X is a Poisson process so far.

It remains to prove the lemma in the case where the support of ρ is bounded. The idea here is the same as in the previous case, but the procedure to connect together different components is a little more involved. First, we find M &gt; 0 such that


<!-- p:74 -->


$$( \mathbf i ) & \ P ( \rho > M ) = 0 , \\ ( \mathbf i ) & \ P ( M - \eta < \rho \leq M ) > 0 , \text { for any } \eta > 0 .$$

Now suppose (X, ρ, λ) admits K ≥ 2 unbounded occupied components a.s. If we remove all the balls centred inside a box B, then the resulting configuration should contain at least K unbounded components a.s. Let, for A C IRd, C[A] denote the region Ux∈AS(x, ρ); that is, C[A] is the occupied region formed by points of X in A. Given a box B and € &gt; 0, consider the event A(B, ε) := {d(U, B) ≤ M − ε for any unbounded occupied component U in C[B]}. Partition the box into cubic cells with edge length a &gt; 0 and let Ca = {G, . . . , GN} denote the collection of all the cells which are adjacent to the boundary of B. Clearly, for a box B and € &gt; 0, we can find a = a(B, €) &gt; 0 and η = η(a) &gt; 0 such that for any point x ∉ B with d(x, B) ≤ M − (€/2), there exists a cell G = G(x) ∈ Ca for which we have sup y∈G d(x, y) ≤ M −2η. This means that, if we centre in each cell of Ca a ball with radius between M — η and M, then the region {x  B : d(x, B) ≤ M − ∈/2} will be completely covered by these balls.

Let E = E(a, η) be the event that each cell in Ca contains at least one Poisson point with an associated ball of radius between M — η and M. Since E depends on the configuration inside the box β and A(B, €) depends on the configuration outside the box B, and the radii are independent of the Poisson process, we have

$$P ( A ( B , \epsilon ) \cap E ) = P ( A ( B , \epsilon ) ) P ( E ) .$$

If both A(B, €) and E occur, then there is only one unbounded occupied component. Now P(E) &gt; 0, so in order to arrive at a contradiction, we need to show that there exist a box B and an € &gt; 0 such that P(A(B, €)) &gt; 0. Since (X, ρ, λ) admits K ≥ 2 unbounded occupied components, we can find a box B so large that, with positive probability, d(U, B) &lt; M for every unbounded component U of C. Also, the radius of any ball is at most M, so, with positive probability, d(U, B) &lt; M for every unbounded occupied component U in C[ B]. Thus for this B we can find € &gt; 0 such that A(B, €) occurs with positive probability.

口

Proof of Theorem 3.6 According to Proposition 3.3 it suffices to rule out the possibility of having infinitely many unbounded occupied components, so we again proceed by assuming the contrary and then derive a contradiction. Suppose there are infinitely many unbounded occupied components a.s. Define for each integer n and z = (z1, . . . , zd) ∈ Zd


<!-- p:75 -->


Figure 3.1. The branches of C' are the connected regions outside the box.

$$B _ { n } ^ { z } \colon = B _ { n } ^ { 0 } + ( z _ { 1 } , \dots , z _ { d } ) ,$$

where of course B0 = [−n, n]d. (Note that in this notation, Bn = B0.) As in the proof of Proposition 3.3 we can find an N such that C[ B ] contains at least three unbounded occupied components which can be connected to each other via extra balls centred in BN. It follows from this that for some N, the following event has positive probability η (say):

E0(N) = {there is an unbounded occupied component C' with the property that C'∩ (B0)c contains at least three unbounded components and

We shall all the unbounded components in C'∩ (B0 )c branches (see Figure 3.1). Next we choose K very large, we shall see at the end of the proof exactly how large. Given K, we choose M so large that the following event has probability at least 27:

E0(N, M) := E0(N) ∩ {all three branches of BN contain at least K Poisson points in BMN\ BO ).

The events E2(N) and E(N, M) are defined by translating E0(N) and E0(N, M) over the vector z. It follows that if R is the set

R := {z ∈ Zd : B2 2Nz ⊂ BL.N, E2Nz(N, M) occurs}, MN


<!-- p:76 -->


then, for any L &gt; 0, then, Tor any Z &gt; 0,

and

$$E ( \text {card} ( R ) ) \geq \frac { 1 } { 4 } \eta L ^ { d } .$$

For z ∈ R, if we denote by C C(1) C(2) and C C(3) the set of all Poisson points in each of its three branches contained in B2 2Nz , then Ci = ∅ for i ≠ j, and MN, card(Ci) ≥ K for ll i. Furthermore, for z, z′ ∈ R, z ≠ z′, if we identify z and 2Nz z' with a Poisson point in B ∩ C' (which exists according to the definition N of E0(N )), it is not difficult to check that (i) in Lemma 3.2 occurs if the points of X in B 2Nz are in a different component of C ∩ B0 than the points of X N LN in B 2Nz' , and that (ii) occurs otherwise. Hence, we conclude from Lemma 3.2 N and (3.57) that

$$E ( X ( B _ { L N } ) ) \geq K \left ( \frac { \eta } { 4 } L ^ { d } + 2 \right ) .$$

To see that this leads to a contradiction, note that

$$E ( X ( B _ { L N } ) ) = \lambda ( 2 L N ) ^ { d } .$$

Hence we find from (3.58) and (3.59) that for L large enough,

$$K \left ( \frac { \eta } { 4 } L ^ { d } + 2 \right ) \leq \lambda ( 2 L N ) ^ { d } ,$$

which gives the desired contradiction if we choose K large.

### 3.7 Exponential decay

We now prove a result which allows us to give bounds on the growth of the occupied cluster of the origin in the subcritical regime. Consider a Poisson Boolean model (X, ρ, λ) with 0 &lt; ρ ≤ R. Recall that σ((N1, ... , Nd), λ, i) = Pλ {there exists an occupied crossing in the i-th direction of the rectangle [0, N1] × · · · × [0, Nd]}.

Lemma 3.3 Consider a Boolean model with ρ ≤ R a.s. Let κ0 = (e3d)−11d−1. If σ((3N1, ..., 3Ni−1, Ni, 3Ni+1, .. ., 3Nd), λ, i) &lt; κ0 for all i = 1, ..., d and for some N1, ... , Nd with Nj &gt; R for all 1 ≤ j ≤ d, then, for all a sufficiently large, we have

$$P _ { \lambda } ( d ( W ) > a ) \leq C _ { 1 } \exp ( - C _ { 2 } a )$$

$$P _ { \lambda } ( \ell ( W ) > a ) \leq C _ { 3 } \exp ( - C _ { 4 } a )$$

for some positive constants C1, C2, C3 and C4.

口


<!-- p:77 -->


Proof Consider the integer lattice Zd with vertices (v1 , . . . , vd) and (w , . . . , wd) adjacent if and only if max{|vi − wi|, i = 1, ... , d} = 1. A vertex z ∈ Zd is open if and only if there exists a connected component Λ of the covered region C of the Boolean model (X, ρ, λ) such that

$$\Lambda \cap ( [ z _ { 1 } N _ { 1 } , ( z _ { 1 } + 1 ) N _ { 1 } ) \times \dots \times [ z _ { d } N _ { d } , ( z _ { d } + 1 ) N _ { d } ) ) \neq \emptyset \\ \text {and}$$

$$\Lambda \cap ( [ ( z _ { 1 } - 1 ) N _ { 1 } , ( z _ { 1 } + 2 ) N _ { 1 } ) \times \cdots \\ \times [ ( z _ { d } - 1 ) N _ { d } , ( z _ { d } + 2 ) N _ { d } ) ) ^ { c } \neq \emptyset ,$$

where N1, N2, ..., Nd are as in the lemma. The vertex z is closed if it is not open. Clearly we have constructed a dependent site percolation process where the state of a vertex z depends on the configuration of the Boolean model (X, ρ, λ) in the region

$$[ ( z _ { 1 } - 1 ) N _ { 1 } - R , ( z _ { 1 } + 2 ) N _ { 1 } + R ) \times \cdots \\ \times [ ( z _ { d } - 1 ) N _ { d } - R , ( z _ { d } + 2 ) N _ { d } + R ) \\ \subseteq [ ( z _ { 1 } - 2 ) N _ { 1 } , ( z _ { 1 } + 3 ) N _ { 1 } ) \times \cdots \\ \times [ ( z _ { d } - 2 ) N _ { d } , ( z _ { d } + 3 ) N _ { d } ) .$$

Thus if z and z′ are vertices of Zd such that max{|zi − zψ|; i = 1, . . . , d} ≥ 5 then the states of the vertices z and z' are independent of each other. Also observe that for a vertex z to be open the Boolean model must admit an occupied crossing in the i-th direction of a suitable translate of the rectangle [0, 3N1] × . . . × [0, 3Ni−1] × [0, Ni] × [0, 3Ni+1] × . . . × [0, 3Nd] for some i = 1, . . . , d. Thus, by the hypothesis of the lemma,

$$p & \colon = P _ { \lambda } ( z \text { is open} ) \\ & \leq 2 \sum _ { i = 1 } ^ { d } \sigma ( ( 3 N _ { 1 } , \dots , 3 N _ { i - 1 } , N _ { i } , 3 N _ { i + 1 } , \dots , 3 N _ { d } ) , \lambda , i ) \\ & \leq 2 d \tau _ { 0 } .$$

Now suppose d(W) ≥ a. Since, for any z ∈ Zd,

$$d ( \mathcal { W } \cap ( [ z _ { 1 } N _ { 1 } , ( z _ { 1 } + 1 ) N _ { 1 } ) \times \cdots \times [ z _ { d } N _ { d } , ( z _ { d } + 1 ) N _ { d } ) ) ) \\ \leq d ( [ z _ { 1 } N _ { 1 } , ( z _ { 1 } + 1 ) N _ { 1 } ) \times \cdots \times [ z _ { d } N _ { d } , ( z _ { d } + 1 ) N _ { d } ) ) \\ \leq \sqrt { N _ { 1 } ^ { 2 } + \cdots + N _ { d } ^ { 2 } }$$


<!-- p:78 -->


and

$$d ( W \cap ( ( [ z _ { 1 } - 1 ) N _ { 1 } , ( z _ { 1 } + 2 ) N _ { 1 } ) \times \cdots \times [ ( z _ { d } - 1 ) N _ { d } , ( z _ { d } + 2 ) N _ { d } ) ) ) \\ \leq d ( ( [ ( z _ { 1 } - 1 ) N _ { 1 } , ( z _ { 1 } + 2 ) N _ { 1 } ) \times \cdots \times [ ( z _ { d } - 1 ) N _ { d } , ( z _ { d } + 2 ) N _ { d } ) ) \\ \leq 3 \sqrt { N _ { 1 } ^ { 2 } + \cdots + N _ { d } ^ { 2 } } ,$$

there must be at least a(N2 + ... + N2)−1/2 vertices z ∈ Zd such that (3.62) holds. Also, if a is such that a &gt; 3√ N2 + . . . + N, then each of the a(N2 + . . . + N2)−1/2 vertices z in Zd satisfies (3.63). Moreover, for z = 0, the origin, both (3.62) and (3.63) hold whenever d(W) ≥ a, thus we have that card(C') ≥ a(N2 + . . · + N2)−1/2 whenever d(W) ≥ a, a ≥ 3√ N2 + ... + N2, where C′ is the open cluster of the origin in the lattice Za (with the adjacency structure given above).

A similar argument yields that for a ≥ 3a N1 · · . Nd, whenever l(W) ≥ a, we must have card(C') ≥ a(N1 · . Nd)−1.

Thus for a large enough,

$$P _ { \lambda } ( d ( W ) \geq a ) \leq P ( \text {card} ( C ^ { \prime } ) \geq a ( N _ { 1 } ^ { 2 } + \cdots + N _ { d } ^ { 2 } ) ^ { - 1 / 2 } )$$

and

$$P _ { \lambda } ( \ell ( W ) \geq a ) \leq P ( \text {card} ( C ^ { \prime } ) \geq a ( N _ { 1 } \cdots N _ { d } ) ^ { - 1 } ) .$$

Now given a set S of n vertices of Za, since the states of two vertices z and z′ are independent whenever max{|zi − z'|; i = 1, . . . , d} ≥ 5, we have that Sn must contain at least n1 1-d vertices whose states are independent of each other. Thus

$$P _ { \lambda } ( \text {all vertices of } S _ { n } \text { are open} ) \leq p ^ { n / 1 1 ^ { d } }$$

where p is as defined in (3.64).

Hence from (3.67) we have

$$P _ { \lambda } ( \text {card} ( C ^ { \prime } ) = n ) & = \sum _ { S _ { n } } P _ { \lambda } ( C ^ { \prime } = S _ { n } ) \\ & \leq b _ { n } p ^ { n / 1 1 ^ { d } } ,$$

where the sum is over all connected sets Sn of n vertices of Za containing the origin and b is the total number of such sets S. Combining (3.68) with (3.65)


<!-- p:79 -->


and using the estimate bn ≤ (e3a)n (Kesten 1982, Lemma 5.1), we have

$$a n d \, \text {using the estimate } b _ { n } & \leq ( e 3 ^ { d } ) ^ { n } \, ( K { \text {sten} } \, 1 9 2 , \, \text {Lemma 5.1} ) , \, \text {we have} \\ & \quad P _ { \lambda } ( d ( W ) \geq a ) \leq \sum _ { n \geq a ( N _ { 1 } ^ { 2 } + \cdots + N _ { d } ^ { 2 } ) ^ { - 1 / 2 } } P _ { \lambda } ( \text {card} ( C ^ { \prime } ) = n ) \\ & \leq \sum _ { n \geq a ( N _ { 1 } ^ { 2 } + \cdots + N _ { d } ^ { 2 } ) ^ { - 1 / 2 } } b _ { n } p ^ { n / 1 1 ^ { d } } \\ & \leq \sum _ { n \geq a ( N _ { 1 } ^ { 2 } + \cdots + N _ { d } ^ { 2 } ) ^ { - 1 / 2 } } ( e 3 ^ { d } ) ^ { n } p ^ { n / 1 1 ^ { d } } \\ & < C _ { 1 } \exp ( - C _ { 2 } a ) , \\ \text {where}$$

where

and

$$C _ { 2 } & = - \frac { 1 + d \log 3 } { \sqrt { N _ { 1 } ^ { 2 } + \cdots + N _ { d } ^ { 2 } } } - \frac { 1 + d \log 3 } { 1 1 ^ { d } \sqrt { N _ { 1 } ^ { 2 } + \cdots + N _ { d } ^ { 2 } } } - \frac { \log \kappa _ { 0 } } { 1 1 ^ { d } \sqrt { N _ { 1 } ^ { 2 } + \cdots + N _ { d } ^ { 2 } } } \\ & \quad + \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \colon \$$

which is positive by our choice of κo. This proves (3.60). Combining (3.68) with (3.66) and performing similar calculations as in (3.69) yields (3.61). This proves the lemma. □

### 3.8 Continuity of the critical density and the percolation function

The Boolean model (X, ρ, λ) has two parameters λ and ρ. In this section we investigate to what extent quantities like λc(ρ) and θρ(λ) are continuous with respect to these parameters. For continuity with respect to ρ we need to choose a notion of convergence, and we shall use weak convergence throughout. The first question we want to answer is whether or not λc(ρk) converges to λc(ρ) when ρk → ρ, where '⇒' denotes weak convergence. In fact we already know that this can not be true in general. In Proposition 3.1 we already proved that if Eρd = ∞ then λc(ρ) = 0, while it follows easily from Theorem 3.3 that if we take ρ to be an a.s. positive constant, then λc(ρ) &gt; 0. Combining these two facts, we can take a sequence ρ1, ρ2, .. . converging weakly to ρ such that

The next theorem gives a sufficient condition on the radii random variables to guarantee convergence of the critical density.

Theorem 3.7 Let ρk and ρ be random variables such that for some R &gt; 0 we have 0 ≤ ρ ≤ R and 0 ≤ ρk ≤ R a.s. for all k ≥ 1. If ρk ⇒ ρ then λc(ρk) → λc(ρ).

$$C _ { 1 } = ( 1 - e 3 ^ { d } ( e 3 ^ { d } \kappa _ { 0 } ) ^ { 1 1 ^ { - d } } ) ^ { - 1 }$$


<!-- p:80 -->


Our strategy will be to approximate the radii ρ and ρk by radii which take only finitely many values. For ease of notation, we shall restrict ourselves to two dimensions. The proof for higher dimensions is similar.

Lemma 3.4 Let 0 &lt; r1 &lt; r2 &lt; . .. &lt; rn &lt; ∞ and let ρ and ρ′ be random variables taking values ri with probability pi and p', respectively, for i = 1, 2, .. . , n, where ∑i=1 Pi = Σi=1 P'i = 1. Suppose that there exist 1 ≤ j &lt; l ≤ n such that for all i ≠ j or l and i = 1, . . . , n, pi = pi and pl and pi are both positive. Then,

$$| \lambda _ { c } ( \rho ) - \lambda _ { c } ( \rho ^ { \prime } ) | \leq \frac { \lambda _ { c } ( r _ { 1 } ) } { \min \{ p _ { l } , p _ { l } ^ { \prime } \} } | p _ { j } - p _ { j } ^ { \prime } | .$$

Proof Suppose first that pj &gt; p'j. We shall use a coupling argument to prove that

$$\lambda _ { c } ( \rho ) \geq \lambda _ { c } ( \rho ^ { \prime } ) .$$

To see this, consider n independent Poisson processes X1, X2, . . . , Xn of densities p1λ, P2λ, ... , Pj-1λ, Pjλ, Pj+1λ, ... , Pnλ, respectively. At each point of the process X we centre à ball of radius r. Now consider another indepen t  i dt o (t - d s  , end  dnt of this process X' we centre a ball of radius rj then the superposition of the models (X1, r1, p1λ), (X2, r2, p2λ), ..., (Xj−1, rj−1, Pj−1λ), (Xj, rj, pjλ), (Xj+1, rj+1, Pj+1λ), ... , (Xn, rn, Pnλ) and (X′, rj, (Pj − pj)λ) is a Poiso    on (   o n o i = 1, ..., n. If, instead, at the points of the process X' we centre a ball of radius r and then superpose all the models, we obtain a Poisson Boolean model (X, ρ′, λ). Since rj &lt; rl, the occupied region in (X, ρ, λ) will be contained in the occupied region in (X, ρ′, λ). Hence the existence of an unbounded component in the model (X, ρ, λ) will imply the existence of an unbounded component in the model (X, ρ′, λ) which implies inequality (3.71). We have explained this in detail because we shall be using this kind of coupling results very often later without going into the details of the proof.

Now choose λ &gt; λc(ρ'). Consider the models (Xi, ri, λli), for i = 1, . .. , l – 1, l + 1, . . . , n, where the li's are chosen such that

$$\frac { \lambda p _ { i } ^ { \prime } + \lambda l _ { i } } { \lambda ( 1 + L ) } = p _ { i } , \ \ i = 1 , \dots , l - 1 , l + 1 , \dots , n ,$$

for L := l1 + · . · + ll−1 + ll+1 + · . · + ln. The system of linear equations (3.72) can be explicitly solved to yield li = (pt)−1(pi pi − pt pi) ≥ 0. Next, let (X, ρ'. λ) be a Boolcan model independent of the models (Xi, r, λli) and consider the superposition of (X, ρ′, λ) and (Xi, r, λli), i = 1, . . . , l − 1, l + 1, ... n to obtain a model equivalent in law to (X, ρ, λ(1 + L)) where X = X1 * · . · * Xl−1 * Xl+1 *· · · * Xn * X and * denotes superposition. (To see that the radius random variable in this superposition is ρ, just use (3.72).) Since λ &gt; λc(ρ′), the model (X, ρ′, λ) is supercritical and hence the superposition is certainly supercritical. Thus


<!-- p:81 -->


$$\lambda ( 1 + L ) > \lambda _ { c } ( \rho ) .$$

The above inequality holds for all λ &gt; λc(ρ'), so we have

$$\lambda _ { c } ( \rho ^ { \prime } ) ( 1 + L ) \geq \lambda _ { c } ( \rho ) ,$$

We have from (3.72) and some elementary calculations L = (pl)−1(pj − pj). The result now follows since λc(ρ') ≤ λc(r1). □

For the case pj &lt; p′j, we just reverse the roles of ρ and ρ'. A similar argument as above yields (3.70). □

Lemma 3.5 Let 0 &lt; r1 &lt; ... &lt; rn, and let ρ be a random variable taking values ri with probability pi for i = 1, 2, .. , n, where Σi=1 Pi = 1. Suppose that pn &gt; 0. For all k = 1, 2, . . . define the random variables ρk taking values ri with probability Pk,i for all i = 1, .. , n, where Σi=1 Pk,i = 1 for all k. If Pk,i → pi for all i when k → ∞, then λc(ρk) → λc(ρ).

Proof We have assumed that Pn &gt; 0 so we can pick 0 &lt; δ &lt; pn. Take ko so large that ∑=1 | pk,i − Pi| &lt; 8 for all k ≥ k0. Then, of course, we have Pk,n &gt; -   =       t SK (l) be the random variable defined by

$$P ( \xi _ { k } ^ { ( l ) } = r _ { l } ) = \begin{cases} \ p _ { k , i } & \text { for } i = 1 , \dots , l , \\ \ p _ { i } & \text { for } i = l + 1 , \dots , n - 1 , \\ \ p _ { n } + \sum _ { i = 1 } ^ { l } ( p _ { i } - p _ { k , i } ) & \text { for } i = n . \end{cases}$$

Clearly, ξk (n-1) has the same distribution as ρk and we define (0) := ρ.

According to Lemma 3.4, for l = 1, . . . , n – 1, we have

$$| \lambda _ { c } ( \xi _ { k } ^ { ( l ) } ) - \lambda _ { c } ( \xi _ { k } ^ { ( l - 1 ) } ) | \leq 2 \delta ^ { - 1 } \lambda _ { c } ( r _ { 1 } ) | p _ { l } - p _ { k , l } | .$$

Adding the previous inequalities over all l, and using the triangle inequality, we obtain

$$| \lambda _ { c } ( \rho _ { k } ) - \lambda _ { c } ( \rho ) | \leq 2 \delta ^ { - 1 } \lambda _ { c } ( r _ { 1 } ) \sum _ { l = 1 } ^ { n - 1 } | p _ { l } - p _ { k , l } | ,$$

for all k ≥ ko. This proves the lemma.


<!-- p:82 -->


Next we drop the assumption that pn should be positive:

Lemma 3.6 Let 0 &lt; r1 &lt; . . . &lt; rn, and, for k ≥ 1, let ρ and ρk be random variables taking values ri with probability pi and pk,i for i = 1, 2, ..., n, u  1     ∞ ←    ←  f  =  = = d = then λc(ρk) → λc(ρ) as k → ∞.

Proof In view of Lemma 3.5, we need to prove this lemma for the case when there exists 1 ≤ m ≤ n − 1 such that

$$p _ { m } > 0 \, \text {and} \, p _ { m + 1 } = \dots = p _ { n } = 0 .$$

First we show that it suffices to prove the lemma for the case m = n — 1. Let the random variables ξ and ξ be defined by

$$P ( \xi _ { k } ^ { \prime } = r _ { i } ) = \begin{cases} p _ { k , i } & \text {for $i=1,\dots,m$,} \\ 0 & \text {for $i=m+1,\dots,n-1$,} \\ \sum _ { i = m + 1 } ^ { n } ( p _ { i } - p _ { k , i } ) & \text {for $i=n$,} \end{cases}$$

and

$$P ( \xi _ { k } ^ { \prime \prime } = r _ { i } ) = \begin{cases} \ p _ { k , i } & \text {for } i = 1 , \dots , m , \\ \sum _ { i = m + 1 } ^ { n } ( p _ { i } - p _ { k , i } ) & \text {for } i = m + 1 , \\ 0 & \text {for } i = m + 1 , \dots , n , \end{cases}$$

then we clearly have

$$\lambda _ { c } ( \xi _ { k } ^ { \prime } ) \leq \lambda _ { c } ( \rho _ { k } ) \leq \lambda _ { c } ( \xi _ { k } ^ { \prime \prime } ) .$$

So it suffices to show that λc(ρk) converges to λc(ρ) when the ρk's take at most one value larger than rm with positive probability. Thus we henceforth assume 0 = d  0  1-− · :  - u =  .

Next let ρk be a random variable taking values r1, . .. , rn with probabilities P1, P2, ..., Pn−2, Pk,n−1, Pk,n, respectively, where Pk,n−1 := Pn−1 − Pk,n. For k large enough, since Pn−1 &gt; 0 and pk,n → 0 as k → ∞, so P'k,n−1 ≥ 0. We shall now prove

$$\lim _ { k \to \infty } \lambda _ { c } ( \rho _ { k } ^ { \prime } ) = \lambda _ { c } ( \rho ) .$$

We observe from our choice of ρ that

$$\lambda _ { c } ( \rho _ { k } ^ { \prime } ) \leq \lambda _ { c } ( \rho ) .$$

Sodd (  ( ∞   s    ( d  se there exists a λ such that lim infk→∞ λc(ρ) &lt; λ &lt; λc(ρ). Since λ &lt; λc(ρ), for κo as in Lemma 3.3 and using Theorem 3.5, we can find an N such that the crossing probability in (X, ρ, λ) satisfies


<!-- p:83 -->


$$\sigma ( ( N , 3 N ) , \lambda , 1 ) < \frac { 1 } { 2 } \kappa _ { 0 } .$$

Now we construct independent Poisson Boolean models (Xi, ri, λlk,i) for i = 1, 2, . . . , n − 2, n and another independent Poisson Boolean model (X', ρ, λ) so as to yield the model (X, ρk, λ(1 + Lk)) when all the models are superposed, where X = X′ * X1 * .. · * Xn−2 * Xn and Lk = lk,1 + · . · + lk,n-2 + lk,n. For this, we choose lk,1.. k,n–2, l to satisfy the following relations:

$$\frac { p _ { i } + l _ { k , i } } { 1 + L _ { k } } = p _ { i } \quad \text {for } i = 1 , \dots , n - 2 ,$$

$$\frac { l _ { k , n } } { 1 + L _ { k } } = p _ { k , n } .$$

The system of linear equations (3.76) and (3.77) can be explicitly solved to yield

$$l _ { k , i } = \left ( \frac { p _ { n - 1 } - p _ { k , n - 1 } ^ { \prime } } { p _ { k , n - 1 } ^ { \prime } } \right ) p _ { i } \geq 0 \ \text { for } i = 1 , \dots , n - 2 ,$$

and pup

and and

$$l _ { k , n } = \frac { p _ { n - 1 } } { p _ { k , n - 1 } ^ { \prime } } p _ { k , n } \geq 0 .$$

Clearly, for every i = 1, . .. , n − 2 and i = n, lk,i → 0 when k → ∞. Thus, we can choose k large enough such that for all i = 1, . . . , n − 2 and i = n, we have

$$P _ { \lambda _ { k , i } } ( X _ { i } ( [ - R , N + R ] \times [ - R , 3 N + R ] ) \geq 1 ) < \kappa _ { 0 } / 2 n ,$$

where κo is as chosen before.

The superposition of the Poisson Boolean models (Xi, ri, λlk,i) for all i = 1, ..., n – 2, n and (X', ρ, λ) is equivalent in law to the Poisson Boolean model (X, ρk, λ(1 + Lk)). For k large enough, (3.75) and (3.78) imply that σ((N, 3N), λ(1 + Lk), 1) &lt; κ0, and thus it follows from Lemma 3.3, that the superposed model is subcritical. However, by the choice of λ, (X, ρ, λ) is sup    o (( +         on.

(1) Finally, to complete the proof of the lemma, we construct as in the previous lemma, where ξ( (n−1 has the same distribution as ρk and ( (0) = ρk.


<!-- p:84 -->


This method shows that

$$| \lambda _ { c } ( \rho _ { k } ) - \lambda _ { c } ( \rho _ { k } ^ { \prime } ) | \leq 2 ( p _ { n - 1 } ) ^ { - 1 } \lambda _ { c } ( r _ { 1 } ) \sum _ { i = 1 } ^ { n - 2 } | p _ { k , i } - p _ { i } | ,$$

and the lemma follows.

口

Proof of Theorem 3.7 First we suppose that the supports of both ρ and ρk, k = 1,2,... are contained in an interval [a, R], where a &gt; 0. The distribution function of ρ is denoted by F, and the distribution function of ρk by Fk. We can assume that both a and R are continuity points of F. Take a sequence {πn} of partitions of [a, R], which we write as πn = {a = γ0 &lt; γn &lt; .. &lt; γn = R}. The partitions are chosen in such a way that π+1 refines π, all points γ" are continuity points of F and such that |πn| := max1≤i≤kn {γi" − γi−1} → 0 when n → ∞. Now define, for all n ≥ 1, the random variables ρ(n) and ρ(n) by the requirement that if ρ ∈ (γi−1, γi ], then ρ(n) = γi and ρ(n) = γi−1 . It follows from a simple coupling argument that λc(ρ(n) ≤ λc(ρ) ≤ λc(ρ(n)) ≤ λc(a). Also, it is easy to see that λc(ρ(n)) is increasing and λc(ρ(n)) is decreasing in n. Now write

$$\alpha _ { n } \coloneqq \max _ { 1 \leq i \leq k _ { n } } \frac { \gamma _ { i } ^ { n } } { \gamma _ { i - 1 } ^ { n } } \leq 1 + \frac { | \pi _ { n } | } { a } ,$$

which tends to 1 when n → ∞. Hence ρ(n) ≤ αρ(n), which implies that λc(ρ(n)) ≥ λc(αnρ(n)) = α−2λc(ρ(n)) and thus

$$\lambda _ { c } ( \rho ^ { ( n ) } ) \leq \lambda _ { c } ( \rho ) \leq \alpha _ { n } ^ { 2 } \lambda _ { c } ( \rho ^ { ( n ) } ) .$$

$$& \leq \left [ \left ( 1 + \frac { | \pi _ { n } | } { a } \right ) ^ { 2 } - 1 \right ] \lambda _ { c } ( a ) = \colon \beta _ { n } \left ( \text {say} . \right ) \\ \intertext { s u c h a l p o c l u a } & \quad \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \$$

e to  a d o alsn d n p  os ao to nd o.n the obvious notation

$$\lambda _ { c } ( \rho _ { k } ) - \lambda _ { c } ( \rho _ { k } ^ { ( n ) } ) \leq \beta _ { n } .$$

Now given any € &gt; 0, take n so large that βn &lt; €. Observe that ρ(n) takes with probability Fk (γi") – Fk(γi\_). Hence by the choice of the partitions, the fact that ρk ⇒ ρ and Lemma 3.6, we see that |λc(ρ(n)) − λc(ρ(n)} &lt; ∈ for

We can now write k sufficiently large. Together with (3.79) and (3.80) this proves the theorem in this case.


<!-- p:85 -->


Next we drop the assumption that the supports are bounded from below by some positive number. Let δ &gt; 0 be a continuity point of F and let η &gt; 0 be u &lt; ( &lt; (d)d   d ← t   &lt; ( &lt; )()d t pps for k sufficiently large. Certainly, if (X′, δ, ηλ) is supercritical, so is (X, ρk, λ) and it follows that if ηλ &gt; λc(δ) then λ &gt; λc(ρk), or

$$\lambda _ { c } ( \rho _ { k } ) \leq \frac { 1 } { \eta } \lambda _ { c } ( \delta ) .$$

Now let ∈ &gt; 0 and choose a to be a continuity point of F such that F(a) &lt; €, and choose k0 so large that Fk (a) &lt; € for all k ≥ k0. Let ρa be a random variable with distribution equal to the conditional distribution of ρ, given that ρ ≥ a. Similarly, let ρa be a random variable with distribution equal to the conditional distribution of ρ given ρ &lt; a. Then we have λc(ρa) ≤ λc(ρ).

Consider the model (X1, ρa, λ) and (X2, ρa, λl), where l is chosen such that 1(1 + l)−1 = P(λ,ρ)(ρ ≤ a). This means that

$$l = \frac { F ( a ) } { 1 - F ( a ) } .$$

The superposition of the two models is equivalent in law to a process (X, ρ, λ(1 + l)). The following formula is obtained as in (3.52):

$$| \lambda _ { c } ( \rho _ { k } ) - \lambda _ { c } ( \rho _ { k } ^ { a } ) | \leq \frac { \epsilon } { 1 - \epsilon } \lambda _ { c } ( \rho _ { k } ^ { a } ) \leq \frac { \epsilon } { \eta ( 1 - \epsilon ) } \lambda _ { c } ( \delta ) .$$

When ρk ⇒ ρ, then ρ% ⇒ ρa and from the case already proved we conclude that

$$| \lambda _ { c } ( \rho _ { k } ^ { a } ) - \dot { \lambda } ( \rho ^ { a } ) | < \epsilon$$

for k large enough. The result now follows from (3.52), (3.83) and (3.84).

The obvious question arises as to whether or not the percolation probabilities also converge when the radii are uniformly bounded and ρk ⇒ ρ. Note that poinnn  n  og onnd  o onn snce of the critical densities.

Theorem 3.8 Let ρk and ρ be random variables such that for some R &gt; 0 we have 0 &lt; ρ ≤ R and 0 &lt; ρk ≤ R a.s. for all k ≥ 1. If ρk ⇒ ρ, then θρk (λ) → θρ(λ) for all λ ≠ λc(ρ).

In the proof of this theorem we shall need the fact that θρ(λ) is, for fixed ρ, a continuous function of λ, for λ ≠ λc(ρ).


<!-- p:86 -->


Theorem 3.9 In a Poisson Boolean model (X, ρ, λ), the percolation function θρ is a continuous function of λ for all λ ≠ λc(ρ).

Proof of Theorem 3.9 First we show that θ is continuous from the right. The event {d(W) = ∞} is the decreasing limit of the events En = {0 ~ ∂(Bn)} where Bn = [−n, n]d. We claim that Pλ(En) is continuous in λ. To see this, first note that it follows from Lemma 3.1 that if we let δ → 0, the probability that in the Boolean model (X, ρ, δ) there is a ball intersecting Bn tends to zero. Thus if we couple two Boolean models with densities λ and λ + δ respectively on the same probability space as usual, the probability that {0 ~∂(B)} in one model but not in the other tends to 0 when δ → 0. Thus we obtain that θ is a decreasing limit of a sequence of non-decreasing and continuous functions. This implies that it is continuous from the right.

Continuity from the left requires more work. Fix λo &gt; λc(ρ) and take any λ ∈ (λc(ρ), λ0). Let α := (λ/λ0)1/d and scale (X, ρ, λ) by α to obtain the model (α X, αρ, λ0). It follows immediately from the scaling that θαp(λo) = θρ(λ). Now define

$$\psi ( \alpha ) \colon = \theta _ { \alpha \rho } ( \lambda _ { 0 } ) = \theta _ { \rho } ( \lambda _ { 0 } \alpha ^ { d } ) .$$

It is enough to prove that ψ is continuous from the left at 1, and this is what we shall do.

We couple all processes (X, αρ, λo), 0 ≤ α ≤ 1 in the (by now) obvious way and we denote by Wα the occupied component of the origin in (X, αρ, λo). In this coupling we clearly have Wα, ⊆ Wα2 whenever α1 ≤ α2. It suffices to prove

$$P ( d ( W _ { 1 } ) = \infty , d ( W _ { \alpha } ) < \infty \text { for all } \alpha < 1 ) = 0 .$$

In order to prove (3.85) we need to show that for almost all configurations for which d(W1) = ∞, there exists a β &lt; 1 (depending on the configuration!) such that also d(W β) = ∞. First we claim that in any Boolean model (X, ρ, λ), the probability that two balls have exactly one point in common is zero. To see this, let ρo be the radius of the ball centred at the origin and first condition sa x i t   li  a i   s    aos exactly one point in common with the ball centred at the origin is equal to P(ρ = |x| – s). According to Proposition 1.3, the number of such balls is Poisson distributed with parameter λ ∫Ra P(ρ = |x| — s)dx. The integrand, however, is almost surely equal to zero and the claim now follows by integrating over s.

Now suppose that d(W1) = ∞ and let α &lt; 1 be as defined previously. For this choicc of α we have θαρ(λ0) = θρ(λ) &gt; 0. We know from Theorem 3.6


<!-- p:87 -->


that in (X, αρ, λ0) there is almost surely exactly one unbounded occupied component Uα, say, which must be contained in W, by the coupling. If the origin is contained in Uα we are done, so suppose it is not. In that case there exists a.s. a sequence (0 = x0, x1, . . . , xn−1, xn) of points of the point process such that

- (i) xn ∈ Uα.
- (ii) d(xi, x+1) &lt; ri + ri+1, where ri is the radius of the ball centred at x. (The strict inequality here follows from the claim above.)

Now choose α′ &lt; 1 such that d(xi, xi+1) ≤ α′(ri + ri+1) for all i = ( t      , }  =:     -      at d(Wβ) = ∞ and the proof is complete. □

REMARK: In Chapter 4 we shall prove that, in two dimensions, the percolation function θρ is also continuous at criticality when the balls are bounded. The necessary machinery for this will be developed in Chapter 4.

For the proof of Theorem 3.8, we first note from Theorem 3.7 that if λ &lt; λc(ρ), then for n large λ &lt; λc(ρn). So θρ(λ) = θρ (λ) = 0 for n large and λ &lt; λc. Thus we need only consider λ &gt; λc(ρ). As in the proof of Theorem 3.7, we shall approximate the radius random variable by random variables which take only finitely many values. The approximation techniques used to prove this theorem are similar to those used to prove Theorem 3.7.

Lemma 3.7 Let 0 &lt; r1 &lt; r2 &lt; . .. &lt; rn &lt; ∞ and let ρ and ρ′ be random variables taking values ri with probability Pi and p'i, respectively, for i = 1, .. . , n, where Σi=1 Pi = Σi=1 Pi = 1. Suppose that there exist 1 ≤ j &lt; l ≤ n such that pi = p' for all i ≠ j, l and where pl and p'i are both positive. Then,

$$\theta _ { \rho } \left ( \frac { \lambda } { 1 + ( p _ { l } ^ { \prime } ) ^ { - 1 } | p _ { j } - p _ { j } ^ { \prime } | } \right ) \leq \theta _ { \rho ^ { \prime } } ( \lambda ) \leq \theta _ { \rho } ( \lambda ( 1 + ( p _ { l } ) ^ { - 1 } | p _ { j } - p _ { j } ^ { \prime } | ) ) .$$

Proof Suppose first that pj &gt; p'j. By a coupling argument as before we obtain

$$\theta _ { \rho } ( \lambda ) \leq \theta _ { \rho ^ { \prime } } ( \lambda ) .$$

As in the proof of Lemma 3.4, we consider the models (X, ri, λl), for i = 1, . . . , l – 1, 1 + 1, . . . , n, where the li's are chosen as in (3.72). Next, consider the superposition of (X, ρ′, λ) and (Xi, ri, λli), i = 1, . . . , l − 1, l + 1, . . . , n to obtain a model equivalent in law to (X, ρ, λ(1 + L)) where L = l1 + . . . + /1−1 + ll+1 + · . · + ln. By a coupling argument we obtain

$$\theta _ { \rho } ( \lambda ( 1 + L ) ) \geq \theta _ { \rho ^ { \prime } } ( \lambda ) .$$


<!-- p:88 -->


Now L = (pt)−1(pj − pj) and thus we have

$$\theta _ { \rho } ( \lambda ( 1 + L ) ) \geq \theta _ { \rho ^ { \prime } } ( \lambda ) \geq \theta _ { \rho } ( \lambda ) \geq \theta _ { \rho } ( \lambda / ( 1 + L ^ { \prime } ) ) ,$$

where L′ = (p′)−1}pj - pj| and the last inequality follows by the nondecreasingness of the percolation function.

=   e s e t rt  w   d an λ/(1 + L') with the roles of ρ and ρ′ interchanged. 口

Lemma 3.8 Let 0 &lt; r1 &lt; ... &lt; rn, and let ρ be a random variable taking values ri with probability pi for i = 1, .. , n, where Σi=1 Pi = 1. Suppose that pn &gt; 0. For all k = 1, 2, . . . , define the random variables ρk taking values f     wu    = 1      n . If pk,i → pi as k → ∞ for all i, then θρk(λ) → θp(λ) as k → ∞ for all λ &gt; λc(ρ).

Proof The proof of this lemma is similar to that of Lemma 3.5. We first choose 0 &lt; δ &lt; Pn and take ko o large that Σi=1 | Pk,i − i| &lt; δ, for all ≥ ko. Then, of course, we have pk,n &gt; ¿δ, for ali k ≥ k0. So, by using Lemma 3.7, we obtain,

$$\theta _ { \rho } \left ( \lambda \prod _ { i = 1 } ^ { n - 1 } \left ( 1 - \frac { 2 | p _ { k , i } - p _ { i } | } { \delta } \right ) \right ) \leq \theta _ { \rho _ { k } } ( \lambda ) \leq \theta _ { \rho } \left ( \lambda \prod _ { i = 1 } ^ { n - 1 } \left ( 1 + \frac { 2 | p _ { k , i } - p _ { i } | } { \delta } \right ) \right ) .$$

Thus,

$$| \theta _ { p _ { k } } ( \lambda ) - \theta _ { \rho } ( \lambda ) | \\ \leq \theta _ { \rho } \left ( \lambda \prod _ { i = 1 } ^ { n - 1 } \left ( 1 + \frac { 2 | p _ { k , i } - p _ { i } | } { \delta } \right ) \right ) - \theta _ { \rho } \left ( \lambda \prod _ { i = 1 } ^ { n - 1 } \left ( 1 - \frac { 2 | p _ { k , i } - p _ { i } | } { \delta } \right ) \right ) .$$

Now, by continuity of θρ(λ) for λ &gt; λc(ρ) (Theorem 3.9), we have

$$\theta _ { \rho } \left ( \lambda \prod _ { i = 1 } ^ { n - 1 } \left ( 1 + \frac { 2 | p _ { k , i } - p _ { i } | } { \delta } \right ) \right ) - \theta _ { \rho } \left ( \lambda \prod _ { i = 1 } ^ { n - 1 } \left ( 1 - \frac { 2 | p _ { k , i } - p _ { i } | } { \delta } \right ) \right ) \rightarrow$$

∞←y .

Lemma 3.9 Let 0 &lt; r1 &lt; ... &lt; rn and for k ≥ 1, suppose ρ and ρk are random variables taking value r with probability pi and pk.i, respectively, for all 1 ≤ i ≤ n, where ∑i=1 Pi = ∑i=1 pk,i = 1. If pk,i → pi as k → ∞, for all 1 ≤ i ≤ n. then λc(ρk) → λc(ρ) as k → ∞.


<!-- p:89 -->


Proof We need to prove this lemma for the case when there exists 1 ≤ m ≤ n - 1 such that

$$p _ { m } > 0 \, \text {and} \, p _ { m + 1 } = \cdots = p _ { n } = 0 .$$

The same argument as in the proof of Lemma 3.6 shows that we may assume that m = n − 1; i.e. Pn−1 &gt; 0 and pn = 0. Using the same idea as before, it is enough to prove the result in case pk,i = pi for all i = 1, 2, . . . , n − 2 for each k ≥ 1. Also we may assume that pk,n decreases to zero as k → ∞.

Now, let BM = [−M, M]d and ∂(BM) be the boundary of BM. Then, for every k ≥ 1, it is not hard to see that

$$P _ { ( \lambda , \rho _ { k } ) } ( 0 \stackrel { 0 } { \sim } \partial ( B _ { M } ) ) \downarrow \theta _ { \rho _ { k } } ( \lambda ) \text { as } M \to \infty .$$

$$P _ { ( \lambda , \rho ) } ( 0 \stackrel { \circ } { \sim } \partial ( B _ { M } ) ) \downarrow \theta _ { \rho } ( \lambda ) \text { as } M \to \infty .$$

Fix an M ≥ 1. We claim that

$$\lim _ { k \to \infty } P _ { ( \lambda , \rho _ { k } ) } ( 0 \stackrel { \circ } { \sim } \partial ( B _ { M } ) ) = P _ { ( \lambda , \rho ) } ( 0 \stackrel { \circ } { \sim } \partial ( B _ { M } ) ) .$$

Cleay, for each k ≥ 1, we have

$$P _ { ( \lambda , \rho _ { k } ) } ( 0 \stackrel { \circ } { \sim } \partial ( B _ { M } ) ) \geq P _ { ( \lambda , \rho _ { k + 1 } ) } ( 0 \stackrel { \circ } { \sim } \partial ( B _ { M } ) ) \geq P _ { ( \lambda , \rho ) } ( 0 \stackrel { \circ } { \sim } \partial ( B _ { M } ) ) .$$

Hence Hence

$$\lim _ { k \to \infty } P _ { ( \lambda , \rho _ { k } ) } ( 0 \stackrel { \circ } { \sim } \partial ( B _ { M } ) ) \geq P _ { ( \lambda , \rho ) } ( 0 \stackrel { \circ } { \sim } \partial ( B _ { M } ) ) .$$

Given € &gt; 0 we choose k large such that 1 − exp(−λ(2M)d pk,n) &lt; ∈. Now we consider n independent Poisson processes X1, X2, ..., Xn with densities λp1, λp2, . . . , λpn−2, λpk,n−1, λpk,n respectively. At each point of Xi, 1 ≤ i ≤ n — 1, we centre a ball of radius r. For the n-th process Xn we distinguish two cases: (i) at each point of the process Xn we centre a ball of radius rn and (ii) at each point of the process Xn we centre a ball of radius rn–1. In case (i) we obtain the Poisson Boolean model (X, ρk, λ), while in case (ii) we obtain the Poisson Boolean model (X, ρ, λ). Thus by this coupling, we obtain,

$$F & \text {model} \left ( \lambda , \rho , \lambda \right ) . \text { This by this coupling, we obtain,} \\ & P _ { ( \lambda , \rho _ { k } ) } ( 0 \stackrel { \circ } { \sim } \partial ( B _ { M } ) ) - P _ { ( \lambda , \rho ) } ( 0 \stackrel { \circ } { \sim } \partial ( B _ { M } ) ) \\ & \leq \, P ( X _ { n } ( [ - M , M ] ^ { d } ) \geq 1 ) \\ & \, = 1 - \exp ( - \lambda ( 2 M ) ^ { d } p _ { k , n } ) \\ & < \epsilon .$$

Similarly, Smmamly,

This proves (3.88).


<!-- p:90 -->


Now consider the double sequence {P(λ,ρ) (0  ∂(Bm))} in k and M. Note that the sequence is decreasing in both M and k. Hence both the iterated limits exist and are equal. Hence,

$$t \text { and are equal. Hence,} \\ \lim _ { k \to \infty } \theta _ { \rho _ { k } } ( \lambda ) & = \lim _ { k \to \infty } \lim _ { M \to \infty } P _ { ( \lambda , \rho _ { k } ) } ( 0 \stackrel { \circ } { \sim } \partial ( B _ { M } ) ) \\ & = \lim _ { M \to \infty } \lim _ { k \to \infty } P _ { ( \lambda , \rho _ { k } ) } ( 0 \stackrel { \circ } { \sim } \partial ( B _ { M } ) ) \\ & = \lim _ { M \to \infty } P _ { ( \lambda , \rho ) } ( 0 \stackrel { \circ } { \sim } \partial ( B _ { M } ) ) \\ & = \theta _ { \rho } ( \lambda ) .$$

Proof of Theorem 3.8 First we assume that for some a &gt; 0,

$$a > 0 \text { such that } a < \rho , \rho _ { k } \leq R \text { for all } k \geq 1 .$$

Our strategy is to approximate the random variables ρ and ρk by random variables which take only finitely many values. Let the distribution functions of ρ and ρk be denoted by F and Fk respectively. We can assume that both a and R are continuity points of F. Take a sequence {πn} of partitions = R}. We choose the partitions in such a way that πn+1 is a refinement of πn. Also assume that all points γ} are continuity points of F and |πn| := max1≤i≤kn {γi" − γi-−1} → 0, as n → ∞. Now define, for all n ≥ 1, the random variables ρ(n) and ρ(n) by the requirement that if ρ ∈ (γi-1, γi], then ρ(n) = γμ and ρ(n) = γi−1. It follows from a simple coupling argument that θρ(n) (λ) ≤ θρ(λ) ≤ θρ(n) (λ). Now for each k ≥ 1, define the random variables ρk,(n) and ρk (u) as follows: if ρk ∈ (γi−1, γi], then ρk,(n) = γi−1 and ρk (n) = γμn. Clearly, for each n ≥ 1 and k ≥ 1, we have θρk,(n)(λ) ≤ (n) θρk (λ) ≤ θρk (λ).

Now, given € &gt; 0, choose

$$\lambda _ { c } ( \rho ) < \lambda _ { 1 } < \lambda < \lambda _ { 2 }$$

$$\theta _ { \rho } ( \lambda _ { 2 } ) - \theta _ { \rho } ( \lambda _ { 1 } ) < \epsilon .$$

(Note that here we use the continuity of θρ w.r.t. λ.) As before, let for each n ≥ 1,

$$\alpha _ { n } \colon = \max _ { 1 \leq i \leq k _ { n } } \frac { \gamma _ { i } ^ { n } } { \gamma _ { i \wedge 1 } ^ { n } } \leq 1 + \frac { | \pi _ { n } | } { a } ,$$

such t that which tends to 1 as n → ∞. Note that ρ(n) ≤ αn ρ(n). Applying a change of scale to (X, ρ(n), λ0), we obtain the model (α X,, αnρ(n), (α)−dλ0). Since ρ(n) ≤ αn ρ(n), we have for any λ0 &gt; 0


<!-- p:91 -->


$$\theta _ { \rho _ { ( n ) } } ( \lambda _ { 0 } ) = \theta _ { \alpha _ { n } \rho _ { ( n ) } } ( ( \alpha _ { n } ) ^ { - d } \lambda _ { 0 } ) \geq \theta _ { \rho ^ { ( n ) } } ( ( \alpha _ { n } ) ^ { - d } \lambda _ { 0 } ) .$$

Choose n large such that (αn)−d λ &gt; λ2 and (αn)d λ &lt; λ1. Now, by the choice of the partitions and the fact that ρk ⇒ ρ we note that the random variables dd (n) and ρ(n) satisfy the conditions of Lemma 3.9. Thus applying the lemma, we obtain that there exists K1 such that for k ≥ K1

$$| \theta _ { \rho _ { k } ^ { ( n ) } } ( \lambda ) - \theta _ { \rho ^ { ( n ) } } ( \lambda ) | < \epsilon ,$$

For k ≥ K1, we may now write

$$\text {For} \, k \geq K _ { 1 } , \, \text {we may now write} \\ \theta _ { \rho _ { k } } ( \lambda ) - \theta _ { \rho } ( \lambda ) \, \leq \, \theta _ { \rho _ { k } ^ { ( n ) } } ( \lambda ) - \theta _ { \rho } ( \lambda ) \\ \leq \, \theta _ { \rho } ( n ) ( \lambda ) + \epsilon - \theta _ { \rho } ( \lambda ) \text { by } ( 3 . 9 5 ) \\ \leq \, \theta _ { \rho } ( n ) ( \alpha _ { n } ^ { d } ) + \epsilon - \theta _ { \rho } ( \lambda ) \text { by } ( 3 . 9 4 ) \\ \leq \, \theta _ { \rho } ( \alpha _ { n } ^ { d } ) + \epsilon - \theta _ { \rho } ( \lambda ) \\ \leq \, \theta _ { \rho } ( \lambda _ { 2 } ) + \epsilon - \theta _ { \rho } ( \lambda ) \\ \leq 2 \epsilon , \\ \text {where the last inequality follows from} \, ( 3 . 9 2 ) \text { and } ( 3 . 9 3 ) ,$$

where the last inequality follows from (3.92) and (3.93).

Similarly, for fixed n we can choose K2 so large that for k ≥ K2 we have

$$\theta _ { \rho } ( \lambda ) - \theta _ { \rho _ { k } } ( \lambda ) \leq 2 \epsilon .$$

This proves the theorem in case (3.91) holds.

Now let ρ have support (0, R]. Here again, given € &gt; 0, choose λ1 &lt; λ &lt; λ2 such that (3.93) holds. Let a be a continuity point of F, the distribution function of ρ. Let ρa be a random variable with distribution equal to the conditional distribution of ρ, given that ρ ≥ a. Similarly, let ρa be a random variable with distribution equal to the conditional distribution of ρ given ρ &lt; a. Then we have θρ (λ) ≤ θρa (λ). Also define ρ as the random variable having distribution equal to the conditional distribution of ρk, given that ρk ≥ a and ρk,a as the random variable having the distribution function equal to the conditional distribution of ρk, given ρk &lt; a. Note that θρk (λ) ≤ θpq (λ).

For any λ0 &gt; 0, consider the models (X1, ρa, λ0) and (X2, ρa, λ0l), where / is such that 1(1 + 1)−1 = F(a); i.e.,

$$\imath = \frac { F ( a ) } { 1 - F ( a ) } .$$


<!-- p:92 -->


The superposition of these two models is equivalent in law to the model (X, ρ, λ0(1 + I)). Thus, we obtain

$$\theta _ { \rho } ( \lambda _ { 0 } ( 1 + l ) ) \geq \theta _ { \rho ^ { a } } ( \lambda _ { 0 } ) .$$

The same calculations may be carried out for ρk with lk = Fk(a)/(1 − Fk (a)), giving

$$\theta _ { \rho _ { k } } ( \lambda _ { 0 } ( 1 + l _ { k } ) ) \geq \theta _ { \rho _ { k } ^ { a } } ( \lambda _ { 0 } ) .$$

Now, as a → 0, F(a) → 0. Thus we may choose a small enough so that λ(1 + l) &lt; λ2 and λ/(1 + l) &gt; λ1. Now, for this a, we have Fk(a) → F(a) as k → ∞. Choose K3 large so that λ(1 + lk) &lt; λ2 and λ/(1 + lk) &gt; λ1 for k ≥ K3.

Now, the random variables ρk and ρa are bounded below by a. Also, ρ% ⇒ ρa an  rt s t  t          ←  he argument, we may choose K4 large so that for k ≥ K4 we have

$$( 3 . 9 9 )$$

$$| \theta _ { \rho _ { k } ^ { a } } ( \lambda _ { 1 } ) - \theta _ { \rho ^ { a } } ( \lambda _ { 1 } ) | < \epsilon .$$

Thus, we have from (3.93), (3.98) and (3.100) with λ0 = λ/(1 + lk),

$$\theta _ { \rho } ( \lambda ) - \theta _ { \rho _ { k } } ( \lambda ) & \leq \theta _ { \rho } ( \lambda ) - \theta _ { \rho _ { k } ^ { a } } ( \lambda / ( 1 + l _ { k } ) ) \\ & \leq \theta _ { \rho } ( \lambda ) - \theta _ { \rho _ { k } ^ { a } } ( \lambda _ { 1 } ) \\ & \leq \theta _ { \rho } ( \lambda ) - \theta _ { \rho ^ { a } } ( \lambda _ { 1 } ) + \epsilon \\ & \leq \theta _ { \rho } ( \lambda ) - \theta _ { \rho } ( \lambda _ { 1 } ) + \epsilon \\ & \leq 2 \epsilon ,$$

and using (3.93), (3.97) and (3.99) with λ0 = λ,

$$\theta _ { \rho _ { k } } ( \lambda ) - \theta _ { \rho } ( \lambda ) & \leq \theta _ { \rho _ { k } ^ { a } } ( \lambda ) - \theta _ { \rho } ( \lambda ) \\ & \leq \theta _ { \rho ^ { a } } ( \lambda ) - \theta _ { \rho } ( \lambda ) + \epsilon \\ & \leq \theta _ { \rho } ( \lambda ( 1 + l ) ) - \theta _ { \rho } ( \lambda ) + \epsilon \\ & \leq \theta _ { \rho } ( \lambda _ { 2 } ) - \theta _ { \rho } ( \lambda ) + \epsilon \\ & \leq 2 \epsilon .$$

This completes the proof of the theorem.

and


<!-- p:93 -->


### 3.9 Bounds on λc and asymptotics for the cluster size

Consider a Boolean model (X, 1, λ) in two dimensions. We have the following explicit bounds for the critical density:

Theorem 3.10 For a Poisson Boolean model (X, 1, λ) on IR2 we have,

$$0 . 1 7 4 < \lambda _ { c } < 0 . 8 4 3 .$$

Proof First we show that λc &gt; 0.174 and for this we employ a multi-type branching process argument as in Theorem 3.2. The types we consider now are distributed over all real numbers in (0, 2), unlike in the earlier cases when the t'yp  es  aues.

Let x1, x2, ... be the points of the Poisson process X of density λ and fix x to be the initial member of the O-th generation of the branching process. We take another Poisson process X1 of density λ, independent of X and let x1, 1, x1,2, . . . , x1,n, be all the points of X1 which lie in the ball S(x1, 2) = {y : |y — x1| ≤ 2}. The children of x1 in this branching process are these points x1,1, x1,2, . .., x1,n1·

Let xk, 1 , Xk,2, . . . , Xk,nk be the members of the k-th generation of the branching process. To obtain the children of xk,, we consider a Poisson point process Xk+1,i of density λ on IR2, where Xk+1,i is independent of all the processes described as yet. The children of xk,i are those points of the process Xk+1,i wh d   f-  (-x\( x     or xk.i. The type of a child xk+1,1 of xk,i is t := |xk,t − xk+1,1| ∈ (0, 2). Clearly, the distribution of the number and types of children of xk,i depend only on xk,i and its type. Indeed, the distribution of the number of children of xk,i whose types lie in (a, b), 0 ≤ a &lt; b ≤ 2 depends only on the area of the region

$$( S ( x _ { k , i } , 2 ) \smallsetminus S ( x _ { k - 1 , j } , 2 ) ) \cap \{ y \colon \{ y - x _ { k , i } | \in ( a , b ) \} ,$$

and this area depends on xk−1, j only through the distance |xk,i — xk−1, jl, which is precisely the type of xk,. Also, the distribution of the number and types of children of an individual xk,i does not depend on its generation k.

Given that xk,i is of type u, i.e. |xk,i − xk−1, j| = u, let g(v|u) be the length of he  (( = |x -  : (}  (( -x\( x)    s expression for g(vlu) follows from an elementary trigonometric calculation, which yields

$$g ( v | u ) = \begin{cases} 2 v \cos ^ { - 1 } \frac { 4 - u ^ { 2 } - v ^ { 2 } } { 2 u v } & \text {if $2-u<v<2$} \\ 0 & \text {if $0<v\leq 2-u$} . \end{cases}$$


<!-- p:94 -->


Recalling our earlier discussion on the independence properties of the offspring distribution, we easily see that the expected number of children whose types lie in (a, b) of an individual whose type is u is given by ∫b λg(v|u)dv. Moreover, given that an individual is of type u, the expected total number of grandchildren of this individual whose types lie in (a, b) is given by

$$\int _ { 0 } ^ { 2 } \left ( \int _ { a } ^ { b } \lambda ^ { 2 } g ( v | w ) \, d v \right ) g ( w | u ) \, d w .$$

In other words, if we let

$$g _ { 1 } ( v | u ) \colon = \int _ { 0 } ^ { 2 } g ( v | w ) g ( w | u ) d w ,$$

the integral in (3.102) reduces to

$$\lambda ^ { 2 } \int _ { 0 } ^ { b } g _ { 1 } ( v | u ) \, d v .$$

Thus defining recursively,

$$g _ { n } ( v | u ) \colon = \int _ { 0 } ^ { 2 } g _ { n - 1 } ( v | w ) g ( w | u ) \, d w ,$$

we easily see that the expected number of members of the n-th generation having types in (a, b) coming from a particular individual of type u as an ancestor n generations previously is given by

$$\lambda ^ { n } \int _ { a } ^ { a } g _ { n } ( v | u ) \, d v .$$

Hence the expected total number of individuals in the branching process if we start off with an individual of type u is

$$\sum _ { n = 1 } ^ { \infty } \lambda ^ { n } \int _ { 0 } ^ { 2 } g _ { n } ( v | u ) \, d v .$$

To show that (3.103) converges for sufficiently small λ, we use an estimate based on the theory of Hilbert-Schmidt operators (see Dunford and Schwartz 1958, chap. XI, sec. 6). For all complex-valued, square integrable functions f defined on the interval (0, 2), consider the linear operator Tf defined by

$$T _ { f } ( u ) = \int _ { 0 } ^ { 2 } f ( v ) g ( v | u ) d v .$$

$$\int _ { 0 } ^ { 1 } g _ { n } ( v | u ) d v = T _ { 1 } ^ { n } ( u )$$

It is easy to see that where 1(v) ≡ 1 for all v ∈ (0, 2). Thus to show that (3.103) converges for sufficiently small λ we need to know that


<!-- p:95 -->


Figure 3.2. The triangular lattice with the flower' as described in the text.

$$\sum _ { n = 1 } ^ { \infty } \lambda ^ { n } T _ { 1 } ^ { n } ( u )$$

converges for sufficiently small λ. This is indeed true for λ &lt; T-1, where ||T|| denotes the usual operator norm of T, i.e. ||T|| = sup{||Tf||2 : f square integrable, complex-valued functions on (0, 2) with f2 ≤ 1} and fl2 denotes the L2 norm of f. Hence we need to estimate |T|.

It can be seen that, for g as in (3.101) the operator T is compact and positive; thus if α is the largest eigenvalue of T, then α = ∥T|. Hence (3.104) (and thereby (3.103)) converges for all λ ≤ α−1. The standard numerical methods of calculating eigenvalues show that α &gt; 5.718 and thus, if λ ≤ 1/5.718 = 0.174, then (3.103) converges.

Comparing the branching process as in Theorem 3.2 with the Boolean model, it is obvious that the expected number of balls in a component is at most the expected total number of members in this branching process. Thus if λ ≤ 0.174, then the expected number of balls in a component is finite; i.e. λc ≥ 0.174.

To obtain the upper bound, we compare the Boolean model with a sitepercolation model on the triangular lattice. Consider the triangular lattice as in Figure 3.2 with each edge being of unit length. Each site of the lattice is enclosed in a 'flower' which is formed by the six arcs of circles, each of unit radius and centred at the midpoints of the six edges adjacent to the site. A site will be called occupied if there is a point of the Poisson process X situated inside the interior of the associated flower of the site. It is clear that if there are two djacent sites both occupied, then each of the flowers of these two sites must contain the centre of at least one ball, and because of the size of the flower, the balls centred at these flowers of radius 1 must have pairwise non-empty intersection. Thus if site percolation of the triangular lattice occurs (i.e., if there sin od n sisn  c on  i  shn Boolean model.


<!-- p:96 -->


Now, by the construction of the site-percolation model, since the occupancy of a site depends on the realisation of the Poisson process X inside the interior of its associated flower, and for two different sites, the interiors of their respective flowers are disjoint, the occupancy of a site is independent of the occupancy of -  :  ss  s s   ie ss e sis s) where A denotes the area of a flower.

We know from the theory of discrete percolation (see Kesten 1982, p. 52) that if p &gt; ↓ then with positive probability there is percolation in the site percolation model on the triangular lattice. Thus if Aλ &gt; log 2, then there is percolation with positive probability in the Boolean model. An elementary calculation shows that A ≈ 0.8227, thus we have that λc &lt; 0.843. 口

It is clear that computations like this become completely untractable in higher dimensions. However, it is often easier to obtain asymptotic results for important quantities in high dimensions than to perform explicit computations in, say, two dimensions. The reason for this is that most estimates using branching processes become more and more precise when the dimension gets higher, because there is less dependency between the branches of the process in high dimensions. We shall illustrate this idea with asymptotic results on the cluster-size distribution. See the notes for more information on the asymptotics of the critical density. The following lemma is what makes high dimensions 'special':

Lemma 3.10 Suppose that X(d) and Y(d) are independent and uniformly distributed on the unit ball in IRa. Then we have

$$\lim _ { d \to \infty } P \left \{ | X ( d ) | > \frac { 3 } { 4 } \right \} = 1 , \quad ( 3 . 1 0 5 )$$

$$\lim _ { d \to \infty } \left \{ \sup _ { | x | > 3 / 4 } \{ P \{ | X ( d ) - x | \leq 1 \} \} \right \} = 0 ,$$

$$\lim _ { d \to \infty } P \{ | X ( d ) - Y ( d ) | \leq 1 \} = 0 .$$

and and Writing X1(d) for the first coordinate of X(d), we see that it suffices to show that |X1(d)| converges to zero in probability. This follows from the fact that E(|X1(d)|2) ≤ 1/d. Equation (3.107) follows by conditioning on Y(d) and using (3.105) and (3.106). □


<!-- p:97 -->


It will be convenient to assume that we always have a point at the origin. Also, we reparametrise the model writing the density as λ(πd)−1 rather than λ, where πd denotes the volume of a ball in d dimensions with radius 1. In high dimensions it is convenient to consider the Boolean model with fixed radius 2 rather than with radius 1. The reason for this will become clear in the proof of the following theorem.

Theorem 3.11 Consider a Boolean model (X, 2, λ(πd)−1) in d dimensions. Denote by fk(λ) the probability that a Galton-Watson branching process with Poisson-λ offspring distribution has total progeny k. Then, writing Wa for the component containing the origin in d dimensions, we have

$$\lim _ { d \to \infty } P _ { \lambda ( \pi _ { d } ) ^ { - 1 } } ( X ( W _ { d } ) = k ) = f _ { k } ( \lambda ) .$$

Proof The important tool to use here is a stochastic process which is called a branching random walk (BRW). This is arandom process {Zn ; n = 0, 1, 2, . . .} such that Zd consists of just the origin and Zd +1 is obtained from Za by replacing each point y ∈ Z by an independent Poisson-λ number of points uniformly distributed in S(y, 1), i.e. the unit ball centred at y. The set Z is referred to as the n-th generation of the BRW. We can order all points in this BRW as follows: all members of an earlier generation precede all members of a later generation, and the members of any particular generation are ranked in increasing distance to the origin. Let x1, x2, . . . be the ordering of the points of the BRW.

We modify the BRW according to the following algorithm: having checked x1, . . . , xk, we discard xk+1 if (a) it is a descendant of a point previously discarded or (b) xk+1 ∈ U=1 S(xj, 1), where l is such that xi is the immediate forbear of xk+1. It is not hard to see that the remaining points of the BRW have the same spatial distribution as the Poisson points forming the occupied component of the origin in the Boolean model with density λ(πa)−1. This coupling shows that

$$\sum _ { j = 1 } ^ { k } P _ { \lambda ( \pi _ { d } ) ^ { \sim 1 } } ( X ( W _ { d } ) = j ) - \sum _ { j = 1 } ^ { k } f _ { j } ( \lambda ) \geq 0 ,$$


<!-- p:98 -->


for all k ≥ 1. The left-hand side in (3.108) is the probability that in the construction above, (i) the BRW has total progeny greater than k, and (ii) after modifying the BRW as indicated, we are left with at most k points. Denote by Ex the event that none of the first k points in the ordering of the BRW is thrown away. It suffices to prove that limd→∞ P(Ed) = 1 for all k. To do this, let xi be the i-th point in the BRW and write F for the event that (i) none of the offspring of x lies in Uj−1 S(xj, 1), (ii)no two points of this offspring are separated by a distance less than 1 and (iii) each point of this offspring is it follows easily that both P( Fd) and P( Fd  Fk-1) tend to 1 when d tends to infinity, and the proof is complete. 口

### 3.10 Notes

The question of complete coverage of a region A ⊆ IRa by a Boolean model is one of the oldest problems in stochastic geometry, more details of which may be obtained in Hall (1988).

The material of Sections 3.2 and 3.3 and the bounds for λe in two dimensions in Section 3.9 are contained in Hall (1985), which is one of the first mathematical papers devoted exclusively to the study of continuum percolation. The results in Sections 3.4 and 3.7 are from Roy (1990), which also contains the equality result of Section 3.5 but for two dimensions only. The d-dimensional equality result is a combination of results of Zuev and Sidorenko (1985), Menshikov (1986) and Meester, Roy and Sarkar (1994). It may be pointed out here that the results of Zuev and Sidorenko (1985) and Menshikov (1986) establish the equality only in the case when the radius random variable is bounded from below by a strictly positive quantity. The result of Meester, Roy and Sarkar (1994) is used here to extend this case to an arbitrary bounded positive radius random variable.

The uniqueness result of Section 3.6 is from Meester and Roy (1994). Continuity and convergence results of Section 3.8 are from Meester, Roy and Sarkar (1994) and Sarkar (1994). It may be noted that Penrose (1995c) generalised some of these results to a wider class of radii distributions, using results of Tanemura (1993). The latter paper contains a continuum version of a renormalisation technique of Grimmett and Marstrand (1990) for discrete nearest-neighbour percolation models. The asymptotics in Section 3.9 are taken from Penrose (1995b). The method using the branching random walk can be pushed much further. In the same paper, Penrose shows that the critical expected number of balls intersecting the unit ball at the origin is larger than 1, the model percolates with positive probability in high dimensions. This corresponds with positive survival probability of a Galton-Watson branching process when the expected number of offspring is larger than 1.


<!-- p:99 -->


#### 4 Vacancy in Poisson Boolean models

In this chapter we discuss the properties of the vacant components in the Poisson Boolean model. Unlike the occupied components in the Poisson Boolean model, where the structure of the occupied regions arises because of placing balls around the Poisson points, the vacancy structure arises in the negative sense, i.e., in the absence of any ball covering a point. This lack of a structure to describe directly the vacancy configuration is a limitation due to which it is often harder to establish results concerning vacancy.

In the study of percolation on discrete graphs, the vacancy configuration is usually thought of as the dual' of the occupancy structure. In that sense we shall occasionally refer to the vacant region as the dual of the occupied region. This nomenclature is more informal than exact, because in the discrete percolation models, the dual structure has a legitimate construct of its own, rather than being just an appendage of the occupied structure.

-a l      t s al  s e sions, when the radii are bounded, λ* = λ*, where these notations have the same meaning in the vacancy as they had (without the superscript) in the occupancy. In addition, we shall show that in two dimensions, the critical densities arising from the occupancy agree with that arising from vacancy. We shall also establish a uniqueness result for the vacant component as in Section 3.6 of Chapter 3. This will show that in two dimensions for λ &lt; λc, with probability 1, there is exactly one unbounded vacant component and no unbounded -cn n     aa r  &lt;  o   nnn bounded occupied component and no unbounded vacant component. For three n o e  u  se  u      t  t show the co-existence of unbounded vacant and occupied components – i.e.,


<!-- p:100 -->


λ H &lt; λ*H – in three or higher dimensions as suggested by simulation studies in physics.

To prove the equality in two dimensions, we establish an RSW lemma for the Poisson Boolean model. Russo (1978) and Seymour and Welsh (1978) independently proved that in a Z2 lattice-percolation model, if the crossing probabilities of suitable rectangles in either direction are larger than 8, then the crossing probability of a bigger rectangle is larger than f(δ), where the function f depends only on the ratio of the size of the larger and the smaller rectangle. The idea of their proof is to connect a left-right crossing of a rectangle [0, l1] × [0, l2] and a left-right crossing of another rectangle [l1/2, 3l1/2] × [0, l2] by a top-bottom crossing of a suitable rectangle to yield a left-right crossing of the rectangle [0, 3//2] × [0, l2]. Using similar ideas and employing a lattice approximation of the continuum model, we prove the RSW lemma for vacant crossings in our Poisson Boolean model. However, we need some additional construction to take care of the dependency structure of our model. As we shall see later, this involves modifying the Poisson Boolean model in a small region near the intersection of the lowest vacant left-right crossing of [0, l1] × [0, l2] with the right edge of the rectangle [0, l1] × [0, l2] to obtain a dependence structure where we can apply the FKG inequality.

### 4.1 Critical densities

As in the case of the occupied region, the size of a vacant cluster can be measured by either its diameter or its Lebesgue measure. The notion of measuring the size of an occupied cluster by the number of Poisson points comprising the cluster does not have any analogue in vacancy. Thus we have the critical densities:

$$\lambda _ { c } ^ { * } \coloneqq & \sup \{ \lambda \colon P _ { \lambda } \{ d ( V ) = \infty \} > 0 \} , \\ \lambda _ { D } ^ { * } \coloneqq & \sup \{ \lambda \colon E _ { \lambda } ( d ( V ) ) = \infty \} , \\ \lambda _ { H } ^ { * } \coloneqq & \sup \{ \lambda \colon P _ { \lambda } \{ \ell ( V ) = \infty \} > 0 \} , \\ \lambda _ { T } ^ { * } \coloneqq & \sup \{ \lambda \colon E _ { \lambda } ( \ell ( V ) ) = \infty \} , \\ \intertext { b e c k e n g } \intertext { a n d } \intertext { p h e r } \intertext { s u p } \intertext { c o n g } \intertext { p r a c t } \intertext { s u p } \intertext { c o n g }$$

where V is the vacant component of the origin as defined in Section 1.4.

In addition to the above four critical densities, we have the critical density defined through vacant crossings:

$$\lambda _ { S } ^ { * } \coloneqq \sup \{ \lambda \colon \lim _ { n \to \infty } \sup \sigma ^ { * } ( ( n , 3 n , \dots , 3 n ) , \lambda , 1 ) > 0 \} ,$$

where σ*((n, 3n, . .. , 3n), λ, 1) is the probability, under Pλ, of the existence o   ×     o vas    sss n  no . . ·. × [0, 3n] as defined in Section 2.3.


<!-- p:101 -->


Our first goal is to show that, when ρ is bounded, the critical densities corresponding to the two different notions of measuring the size of a vacant cluster are equal.

Theorem 4.1 For a Poisson Boolean model (X, ρ, λ) on IRd with ρ bounded almost surely, we have (a) λ* = λ*H and (b) λ*D = λ*.

Unlike the proof of the analogous result for the occupancy (Theorem 3.4), for the proof of Theorem 4.1 we need a bound on the growth of the vacant cluster V when the probability of a vacant crossing is very small. The following lemma can be proved as Lemma 3.3.

Lemma 4.1 Let (X, ρ, λ) be a Poisson Boolean model on IRd with 0 &lt; ρ ≤ R a.s. for some R &gt; 0. There exists κ0 &gt; 0 such that, if for some N = (N1, .. . , Nd) with Nj ≥ R, for all 1 ≤ j ≤ d, we have

$$\sigma ^ { * } ( ( 3 N _ { 1 } , \dots , 3 N _ { i - 1 } , N _ { i } , 3 N _ { i + 1 } , \dots , 3 N _ { d } ) , \lambda , i ) \leq \kappa _ { 0 } ,$$

for all 1 ≤ i ≤ d, then

$$P _ { \lambda } \{ d ( V ) \geq a \} \leq C _ { 1 } \exp ( - C _ { 2 } a )$$

$$P _ { \lambda } \{ \ell ( V ) \geq a \} \leq C _ { 3 } \exp ( - C _ { 4 } a ) ,$$

for all a &gt; O, where C1, C2, C3 and C4 are positive constants independent ofa.

An immediate consequence of this lemma is that for a Poisson Boolean model with a bounded radius random variable, we have

$$\lambda _ { D } ^ { * } \leq \lambda _ { S } ^ { * } \text { \ and \ } \lambda _ { T } ^ { * } \leq \lambda _ { S } ^ { * } .$$

Proof of Theorem 4.1 For ease of notation we shall present the proof only lo  o  o  xo o  ao sy s  do dimensions is straightforward.

First we show (b) λ D = λγ. Let B2R(i) = (0, i4R) + B2R for all i ≥ 0. Observe that an L-R vacant crossing of the rectangle [0, 3k]× [0, 3k+1] necessitates the existence of a vacant region starting from the left edge of [0, 3k] × [0, 3k+1]

and which has a diameter at least 3k. Hence we have, for any k ≥ 1,


<!-- p:102 -->


$$h \, a \, \text {diameter at least } 3 ^ { k } . \, \text {Hence we have, for any } k \geq 1 , \\ \sigma ^ { * } ( ( 3 ^ { k } , 3 ^ { k + 1 } ) , \lambda , 1 ) \\ \leq \, P _ { \hat { A } } \left ( \bigcup _ { i = 0 } ^ { 3 ^ { k + 1 } / 4 R } \{ d ( V ( B _ { 2 R } ( i ) ) ) \geq 3 ^ { k } \} \right ) \\ \leq \, \sum _ { i = 0 } ^ { 3 ^ { k + 1 } / 4 R } P _ { \lambda } \{ d ( V ( B _ { 2 R } ( i ) ) ) \geq 3 ^ { k } \} \\ \leq \left ( \frac { 3 ^ { k + 1 } } { 4 R } + 1 \right ) P _ { \lambda } \{ d ( V ( B _ { 2 R } ( 0 ) ) ) \geq 3 ^ { k } \} . \\ \text {preceding inequalities we have assumed, without any loss of generality,}$$

In the preceding inequalities we have assumed, without any loss of generality, that 3k+1/4R is an integer.

If λ &gt; λ*D, then Eλ(d(V )) &lt; ∞ and thus

$$\sum _ { k = 1 } ^ { \infty } 3 ^ { k + 1 } P _ { \lambda } ( d ( V ) \geq 3 ^ { k } ) & \leq C _ { 1 } E _ { \lambda } ( d ( V ) ) < \infty , \\$$

where C1 is a positive constant. Now as in Example 2.1 of Section 2.3, from (4.6) we have

$$\sum _ { k = 1 } ^ { \infty } 3 ^ { k + 1 } P _ { \lambda } ( d ( V ( B _ { 2 R } ( 0 ) ) ) \geq 3 ^ { k } ) \leq C _ { 2 } E _ { \lambda } ( d ( V ( B _ { 2 R } ( 0 ) ) ) ) < \infty ,$$

for some constant C2 &gt; 0. Thus from (4.7) and (4.5) we have

$$\sum _ { k = 1 } ^ { \infty } \sigma ^ { * } ( ( 3 ^ { k } , 3 ^ { k + 1 } ) , \lambda , 1 ) < \infty .$$

Hence, for some integer k0 ≥ 0 we have σ*((3k, 3k+1), λ, 1) ≤ κ0 for all k ≥ ko, where κ0 is as in Lemma 4.1. Thus applying that lemma, we obtain λ ≥ λ*. This shows that λ* ≤ λ .

To complete the proof of (b) we need to show that λ* ≤ λ*. We use an argument based on scaling. We first show this in the case when there exists η &gt; 0 such that ρ ≥ η a.s. Fix λ &lt; λ and consider the Poisson Boolean models (Xa, aρ, λ), for 0 &lt; a ≤ 1. We couple these models on the same probability space and thus, letting Va denote the vacant cluster of the origin in (Xa, aρ, λ), we have Vb ⊆ Va for all 0 &lt; a ≤ b ≤ 1. Moreover, if x ∈ V1, then, for any 0 &lt; a &lt; 1, the open ball centred at x of radius (1 — a)η will be completely contained in Va, and so

$$\ell ( V _ { a } ) & \geq \pi ( ( 1 - a ) \eta ) ^ { 2 } \frac { d ( V _ { 1 } ) } { 2 ( 1 - a ) \eta } \\ & = C ( a ) d ( V _ { 1 } ) ,$$


<!-- p:103 -->


for some constant C(a) &gt; 0. Hence, if d(V) = ∞ then l(Va) = ∞. This implies that whenever λ &lt; λ*(ρ) we have

$$\lambda \leq \lambda _ { T } ^ { * } ( a \rho ) , \text { for all } a > 0 .$$

However, from Proposition 2.11 we have λ‡ (aρ) = λ*(ρ)/ad, so (4.9) yields the desired inequality.

For general ρ we use an argument similar to the one used in Case 2 of the proof of (a) in Theorem 3.4, and as such we omit it.

Next we show (a) λ* = λ*. We note that for λ &lt; λ and for any m &gt; 0,

$$P _ { \lambda } \{ d ( V ) = \infty \} & \geq \lim _ { m \to \infty } P _ { \lambda } \{ V \cap B _ { m } ^ { c } \neq \emptyset \} \\ & \geq \lim _ { m \to \infty } P _ { \lambda } \{ \ell ( V ) \geq ( 2 m ) ^ { 2 } \}$$

$$\geq P _ { \lambda } \{ \ell ( V ) = \infty \} .$$

Now suppose λ &lt; λ*; i.e., Pλ {d(V) = ∞} &gt; 0. We partition the space with boxes of the form B2mz = 2mz + Bm, where z ∈ Zd . Consider the event m Fz = { B2mz is completely contained in an unbounded vacant component}. It is clear that P(F2) is positive and independent of z. The translation over the vector 2me1 is ergodic, and it follows by the ergodic theorem that P(F2z i.o.) = 1. But then, using the uniqueness of the unbounded component (see Section 4.8) we conclude that for all z for which Fz occurs, the box B2mz is contained in the same unbounded component V'. It follows that l(V') = ∞, whence λ &lt; λ *. This establishes that λ = λ·

Thus, if λ &lt; λ*H then λ ≤ λ*. H

REMARK: It is possible to prove the last step of the preceding proof; i.e. λ* ≤ λ*, along the same lines as the proof of (b); this proof does not involve uniqueness. However, the preceding proof is presented for its elegance and because it does not use the boundedness of the radii.

### 4.2 RSW - notation and definition

Consider a Poisson Boolean niodel (X, ρ, λ) on R2. We define a continuous curve γ to be a vacant path if γ ⊂ Co, the vacant region. A continuous curve γ is said to be an occupied path if γ ⊂ C. A vacant path γ is said to be a vacant left-right (L−R) crossing of the rectangle [0, l1] × [0, l2] if γ ∩ ({0} × [0, l2]) ≠ , γ ∩ ({l1} × [0, l2]) ≠ ∅ and, except for its end points, γ is contained in (0), l1) × (0, l2). Similarly, we define a vacant top-bottom (T-B) crossing by requiring that the end points of γ lie on the top and bottom edges of the rectangle, respectively. We assume that all curves under consideration do not have any self-intersections.


<!-- p:104 -->


Let L  be the lattice an Z × anZ, where {an } is a sequence of positive numbers decreasing to zero when n tends to infinity. Suppose l1 and l2 are positive integer multiples of a. By a cell in this lattice we mean a set [anz1, anz1 + an] × [an z2, an z2 + an] for z} , z2 ∈ Z. Note here that we include the perimeter of the cell in the definition. Two cells in the lattice are said to be adjacent if they have an  cdl d        c   n C0 ∩ (Ui≥1S(xi)) = ∅ (respectively, C0 ∩ (∪i≥1S(xi)) ≠ ∅). An ILn-path is a sequence of disjoint adjacent cells. A vacant (occupied) ILn-path is an In-path wh-      (    a ing Γ of the rectangle [0, l1] × [0, l2] is an Ln-path such that Γ⊆ [0, l1]× [0, l2], Γ∩ ({0} × [0, l2]) ≠ ∅, Γ∩ ({l1} × [0, l2]) ≠∅ and, in addition, each of Γ ∩ ({0} × [0, l2]) and Γ ∩ ({l1} × [0, l2]) consists of a single edge. We define T-B ILn-crossings, vacant/occupied L-R ILn-crossings and vacant/occupied T-B Ln-crossings in a similar fashion. The crossing probabilities (see (2.19)) are denoted as follows:

- σ*((l1, l2), λ, 1) = Pλ {there exists a vacant L-R crossing of [0, l1] × [0, l2]},

σ*((l1, l2), λ, 2)

= Pλ {there exists a vacant T–B crossing of [0, l1] × [0, l2]}.

The RSW lemma states the following:

Theorem 4.2 (RSW lemma) Let (X, ρ, λ) be a Poisson Boolean model in two dimensions with

$$0 < \rho \leq R \ a . s .$$

for some R &gt; 0. If there exist constants δ1 &gt; 0 and δ2 &gt; 0 such that

$$\sigma ^ { * } ( ( l _ { 1 } , l _ { 2 } ) , \lambda , 1 ) \geq \delta _ { 1 }$$

$$\sigma ^ { * } ( ( l _ { 3 } , l _ { 2 } ) , \lambda , 2 ) \geq \delta _ { 2 } ,$$

for some l1 &gt; 4 R and 2 R &lt; l3 ≤ 3l1/2, then for any integer k,

$$\sigma ^ { * } ( ( k l _ { 1 } , l _ { 2 } ) , \lambda , 1 ) \geq C _ { k } ( \lambda , R ) f _ { k } ( \delta _ { 1 } , \delta _ { 2 } ) ,$$

where Ck(λ. R) &gt; (0) is independent of δ1 and δ2 and fk (δ1, δ2) &gt; 0.

and The proof of this theorem is presented in the next three sections and applications can be found in Section 4.6. The main step of the proof is to obtain an RSW result for a discrete approximation of the Boolean model. This, however, does not follow from the discrete percolation results because in any discretisation of the Boolean model, the dependency structure of the model remains. We have to warn the reader that the proof of the RSW lemma is very technical; one can sa  o     sos e   d os We take n so large that


<!-- p:105 -->


####### RSW – construction 4.3

$$l _ { 1 } > 4 R + a _ { n } .$$

Let l1n := [l1/4an|4an and l3n := l3/an|an + an, where for any x ∈ R, [x denotes the largest integer less than or equal to x. Clearly, both l1n and l3n are integer multiples of a. By the monotonicity property of crossing probabilities, σ*((l1n, l2), λ, 1) ≥ σ*((l1, l2), λ, 1) and σ*((l3n, l2), λ, 2) ≥ σ*((l3, l2), λ, 2). Moreover, as an → 0, l1n → I1 and l3n → l3 and it is easy to check that also σ*((l1n, l2), λ, 1) → σ*((l1, l2), λ, 1) and σ*((l3n, l2), λ, 2) → σ*((l3, l2), λ, 2). Since in our calculations we later let an → 0, we may replace l1n by l, and l3n by l3 and thus for the sake of simplicity in notation, we assume that in addition to (4.14) the following also holds:

####### R/4, l1/4, l2 and l3 are all integer multiples of an. (4.15)

On the lattice IL of 'size an' we fix an L-R self-avoiding (i.e. all cells in the path are different) ILn-crossing r which consists of cells Co, C1, ... , Cm of [0, l1 − R] × [0, l2] with C0 ∩ ({0} × [0, l2]) ≠ ∅, Cm ∩ ({l1 − R} × [0, l2]) ≠ ∅, {C1, . . . , Cm−1} ⊆ (0, l1 − R) × [0, l2] and Ci and Ci+1 are adjacent for all i = 0, ..., m – 1. We now consider different pieces of the L-crossing r. Suppose 0 ≤ i1 &lt; i2 &lt; ... &lt; il(r) ≤ m are all indices such that Ci ∩ ({l1/4} × [0, l2]) ≠ ∅ and Ci ⊆ [l1/4, l1 − R] × [0, l2]. In other words Cij, j = 1, 2, ..., I(r) are all the cells of r which are adjacent to the line {l1/4} × [0, l2] and lie on the right side of this line. By our choice of notation, Cir, is the last intersection'' of r with {l1/4} × [0, l2], i.e., Cj ⊂ (l1/4, l1 − R] × [0, l2] for all j &gt; il(r). Let F(r) := (Cit(r), Ci(r)+1, ..., Cm) be the piece of r after this last intersection. Let rk := (Cik, Cik+1, . . . , Cik+1) for all k = 1, . .., 1(r) − 1. Also let 1 ≤ j1 ≤ j2 ≤ ..· ≤ jb(r) ≤ 1(r) − 1 be such that rj ⊆ [l1/4, l1 − R] × [0, l2] if and only if j ∈ {j1, j2, . . . , jb(r)}. Thus F(r) is the piece of r lying completely in the rectangle [l1/4, l1 – R] × [0, l2] and on the right of the line {/1/4} × [0, l2], with one of its end cells adjacent to the line {l1/4} × [0, l2]. Also, for every 1 ≤ i ≤ b(r) − 1, rji has both its end cells adjacent to the line {l1/4} × [0, l2] and lies completely in the rectangle [l1/4, l1 − R] × [0, l2]. (Figure 4.1 depicts this notation.) Let the corner vertices of the cell C0 be (0, α), (an, α) (a, α + an) and (0, α + an) and the corner vertices of the cell Cm be (l1 − R, β), (l1 − R − an, β), (l1 − R − an, β + an) and (l1 − R, β + an). Let Γ, be an In-path defined as follows (see Figure 4.2): Γ, is the collection of cells in the region


<!-- p:106 -->


Figure 4.1. The paths r1, r3 and r5 are the paths rj1 , rj2 and rj3.

Figure 4.2. The shaded path is r, the blackened, Γr and the dotted region, A'.

- (i) ([l1 − R − an, l1 − R] × [β, β + R + 2an]) ∪ ([l1 − R, l1] × [β + R + an, β + R + 2an ]) if β &lt; l2 − R − 2an,
- (ii) ([l1 − R − an, 11 − R] × [β, l2]) ∪ ([l1 − R, l1] × [l2 − an, l2]) if β≥ l2-R-2an.

The In-path r ∪ Γ, is an IL-crossing of [0, 11] × [0, l2] (see Figure 4.2).


<!-- p:107 -->


Figure 4.3. The shaded region is J1+.

Figure 4.4. The shaded region is J2+.

For any set of cells s in [0, l1] × [0, l2], let ref(s) be the reflection of s in {l1} × [0, l2]. Then (F(r) ∪ Γr) ∪ (ref(F(r) ∪ Γr)) is an L−R Ln-crossing of [/1/4, 71/4] × [0, l2]. Next we define the region (see Figure 4.3)

J1+ (r) := {(x, y) ∈ [0, l1 − R] × [0, l2] : (x, y) can be connected to [0, l1 − R] × {l2} by a continuous curve γ such that γ ⊆ [0, l1 − R] × [0, l2] and γ ∩ r = 0}.

This is the part of [0, l1 – R] × [0, l2] which lies above r. We also define the regions (see Figures 4.4 and 4.5)

J2+ (r) := {(x, y) ∈ [l1/4, 7l1/4] × [0, l2] : (x, y) can be connected to [l1/4, 7l1/4] × {l2} by a continuous curve γ such that γ ⊆[1/4,7l1/4] ×[0,l2] and γ ∩ ((r ∪ Γ,) ∪ (ref( F(r) ∪ Γ,))) = ∅}.


<!-- p:108 -->


Figure 4.5. The shaded region is J3+.

J3+ (r) := {(x, y) ∈ [l1/4, 7l1/4] × [0, l2] : (x, y) can be connected to [l1/4, 7l1/4] × {l2} by a continuous curve γ such that γ⊆{l1/4, 7l1/4] ×[0, l2] and γ ∩ ((F(r) ∪ Γ) ∪ (ref(F(r) ∪ Γ,))) = 0}.

The difference between J2+ (r) and J3+(r) is that J2+(r) is the region in [1/4, 7l1/4] × [0, l2] which lies above the path (r ∪ Γ) ∪ (ref(F(r) ∪ Γr)), while J3+(r) is the region in [l1/4, 7l1/4] × [0, l2] which lies above the path (F(r) ∪ Γ,) ∪ (ref(F(r) ∪ Γ,)).

Let J{ (r) := ([0, l1 − R] × [0, l2])\ J1+ (r). We observe that r ⊆ J− (r) and J1+ (r) is a connected region, while J2+ (r) is connected if β &lt; l2 − R − 2an. For any region A, let À denote the closure of A, and int(A) the interior.

For r as above let A′ be the region ([l1 − 2 R − an, l1 + R] × [β, β + 2R + 2an ]) ∩ (J}+ (r) ∪ ([l1 − R, ∞) × IR) ∪ (IR × [l2, ∞))) (see Figure 4.2). We introduce the following events:

```
introduce the following events:

            A, := {X(A'') = 0},
            E, := {r isVacant},
            L, := {any L-R  || _n-crossing s of [0, l_1 - R] \times [0, l2] such that
                      s # r and s \subseteq J^(- r) is not vacant,
            D2(r) := {there exists a vacant L_n-path s    := (C0', C1', \dots , C_v) such that
                        s'  \subseteq \overline{J^+}(r),  C_0 \cap ( [l1/4, 7 l1/4] \times {l2}) \neq \emptyset,
                        C_v \cap ( F(r) \cup \Gamma_) \neq \emptyset and
                        C_k \cap ( ( [l1/4, 7 l1/4] \times {l2}) ) \cup ( F(r) \cup \Gamma_)) = \emptyset,
                        for all k = 1, \dots , \nu - 1}),
```

D2(r) := {there exists a vacant Ln-path s" := (C0, C1 , . .. , Cy) such that for all k = 1, . . . , ν − 1},


<!-- p:109 -->


- D3(r) := {there exists a vacant Ln-path s′ := (C0, C1, . . . , Cμ) such that s′⊆ J}+ (r), C0∩ ([l1/4, 7l1/4]× {l2}) ≠∅, Cμ∩(F(r)∪Γr)≠∅and Ck ∩ (([l1/4, 7l1/4] × {l2) ∪ (F(r) ∪ Γr)) = 0 for all k = 1, . . . , μ − 1}, D(r) := {there exist disjoint vacant Ln-paths s1, . . . , sq for some q ∈ {1, . . ., b(r)} with sk := (C0,k, . . . , Cμk,k) for all k = 1, . .. , q, such that (i) C0,1∩([l1/4, 7l1/4] × {l2}) ≠∅, Cμq,q∩(F(r) ∪ Γ) ≠∅, (ii) Ci,k ⊆ J2+ (r) for all i = 1, ..., μk − 1 and for all k = 1, ... , q, (iii) for all k = 1, . . . , q − 1, Cμx,k lies on ri and C0,k+1 lies
- on rik,, where ik, ik' ∈ {j1, ... , jb(r)} and ik is such that either ik' = ik or there exists a set of indices Φk in {j1, . .. , jb(r)} such that ri, can be connected to rik by a continuous path γ which lies completely in int [(Ui∈φkri) ∩ ([l1/4, 7l1/4] × [0, l2])]}.

In words, D3(r) is the event that there is a vacant ILn-path in J3+ (r) which connects the top edge of the rectangle [l1/4, 7l1/4] × [0, l2] to the path F(r)∪Γr; D2(r) is the event that there is a vacant L-path in J2+ (r) which connects the top edge of the rectangle [l1/4, 7l1/4] × [0, l2] to the path F(r) ∪Γ, and D(r) is the event that there are vacant IL-paths in [l1/4, 7l1/4] × [0, l2] connecting some of the r's adjacent to the boundary of J2+ (r), and two other vacant ILn-paths, one connecting one such r to the path F(r) ∪ Γ, and the other connecting another Su   [  × [            .6 and 4.7).

Given two L-R L-crossings r1 and r2 of [0, a1] × [0, a2] (for some positive numbers a1 and a2) we define r1 ≤ r2 if J1+ (r2) ⊆ J1+ (r1). For any two L-R Ln-crossings r1 and r2, there is an L-R L-crossing s in r1 U r2 of [0, a1] × [0, a2] such that J1+(s) = J1+ (r1) ∪ J1+ (r2) and so s ≤ r1 and s ≤ r2. In particular if r1 and r2 are such that r1 ≤ r2 then s = r1 satisfies s ≤ r1 and s ≤ r2. However, if neither r1 ≤ r2 nor r2 ≤ r1 hold, then r1 ∩ r2 ≠ 0. If we consider the L-R ILn-crossing r' of [0, a1] × [0, a2] which is the 'lower' part of ri U r2 then it is not hard to believe that for s = r' the following is satisfied: there exists a L-R ILn-crossing s of [0, a1] × [0, a2] such that


<!-- p:110 -->


Figure 4.6. The thick line is the path r, the thin line is the path s with segments s1, S2 and s3 as in the event D(r).

Figure 4.7. The black line is a portion of r, the segments 1, 2 and 3 are sk, Sk+1 and sk+2, respectively, and the segments a, b and c are rik, rik, and rik+1

(a) s ⊆ r1 ∪ r2, (b) s ≤ r for all L–R In-crossings r of [0, a1] × [0, a2] with r ⊆ r1 ∪r2. Thus for the finite collection C = {all vacant L-R ILn-crossings of the rectangle [0, a1] × [0, a2]}, we can define the lowest vacant L-R ILn-crossing of [0, a1] × [0, a2] as the L–R IL-crossing r of [0, a1] × [0, a2] such that r ≤ s for every s ∈ C and r ⊆ Us∈cs. Note that all IL-cells comprising Usecs are vacant, and hence the L-R L-crossing r is also a vacant L-R L-crossing of [0, a1] × [0, a2] and thus r ∈ C. The existence of such a lowest vacant L-R


<!-- p:111 -->


IL-crossing is intuitively clear; however a formal proof is quite technical and we refer the reader to Lemma 1 of Kesten (1982). Let D0(r) = D2(r) ∪ D(r). We observe:

Lemma 4.2 The following hold:

- ×-    -      } =    () [0,{2]},
- (ii) D3(r) ∩ Er = D0(r) ∩ Er.

Proof The statement of the lemma is quite easy to see from the definitions bu s ro s  e   e   s ron spelling out the details. □

### 4.4 RSW - preliminary results

In this section we shall use the FKG inequality and a conditional independence property, obtained from our choice of Γr, to derive some preliminary inequalities. It is to have this conditional independence that we introduced the path Γr instead of using an L–R crossing of [0, l1] × [0, l2] directly.

Let R denote the (random) lowest vacant L-R L-crossing of [0, l1 - R] × [0, l2] in the Poisson Boolean model (X, ρ, λ) and r a fixed self-avoiding L-R Ln-crossing of [0, l1 − R] × [0, l2].

####### Lemma 4.3 Pλ(Ar ∩ D0(r)|R = r) ≥ Pλ(Ar)Pλ(D3(r)).

Proof First, we show that given Er, the events Lr and A, ∩ Do(r) are conditionally independent. Indeed, any ball centred in J1+ (r) which intersects J(r) must also intersect r. On E, no such ball can exist. Moreover, for α as chosen in Section 4.3 and for any x ∈ A′ ∪ ([-R, 0] × [α, ∞)), d(x,r) = d(x, J,(r)), where R is as in (4.10). So, any ball centred in A' ∪ ([-R, 0] × [α, ∞)) which intersects J (r) must also intersect r. Also, any ball of radius at most R centred in ((-∞, —R) × IR) ∪ ((l1, ∞) × IR) ∪ (R × (-∞, - R)) does not intersect J (r). Thus given Er, the event L, depends on the Poisson points in the region Λ, := J (r) ∪ (−R, 0] × [− R, α))∪([l1 − R, l1]×[−R, β))∪([0, 11]×[−R, 0]), where β is as defined in Section 4.3.

We now show that, given Er, no ball with centre in Λr can influence the occurrence of Do(r). Indeed, any ball of radius at most R centred in / (r) which intersects J2+(r) must intersect r. Also, no ball of radius at most R centred in either [−R, 0] × [−R, α] or [0, l1] × [−R, 0] can intersect J2+ (r) without intersecting r. Now, for any y ∈ [l1 − R, l1] × [−R, β], d(y,r) ≤ d(y, J2+ (r)), so any ball of radius at most R with centre in [l1 − R, l1] × [−R, β] which intersects J2+ (r) must intersect r. Again, on Er no such ball can exist and therefore no ball in Λr can influence the occurrence of Do(r). Thus, conditioned on Er, the event Lr depends on the Poisson points inside the region Λr, while (A,∩ D0(r)) depends on the Poisson points outside Λr. Hence, given Er, the events Lr and (A, ∩ D0(r)) are independent. It follows that


<!-- p:112 -->


$$P _ { \lambda } ( A , \cap D _ { 0 } ( r ) | \mathcal { R } & = r ) \, = \, P _ { \lambda } ( A _ { r } \cap D _ { 0 } ( r ) | E _ { r } \cap L _ { r } ) \\ & = \, \frac { P _ { \lambda } ( A _ { r } \cap D _ { 0 } ( r ) \cap L _ { r } | E _ { r } ) } { P _ { \lambda } ( L _ { r } | E _ { r } ) } \\ & = \, \frac { P _ { \lambda } ( A _ { r } \cap D _ { 0 } ( r ) | E _ { r } ) P _ { \lambda } ( L _ { r } | E _ { r } ) } { P _ { \lambda } ( L _ { r } | E _ { r } ) } . \\ \intertext { \text {Now using (ii) of Lemma 4.2 and noting that all the three events } A _ { r } , E _ { r } \text { and} }$$

Now using (ii) of Lemma 4.2 and noting that all the three events Ar, E, and D3(r) are decreasing, we obtain from the FKG inequality,

$$P _ { \lambda } ( A _ { r } \cap D _ { 0 } ( r ) | E _ { r } ) \geq P _ { \lambda } ( A _ { r } ) P _ { \lambda } ( D _ { 3 } ( r ) ) .$$

We let the cell size of the lattice Ln go to zero along a sequence {an }n≥1 such that (4.15) holds for every n ≥ 1. Define the L-crossing probabilities as follows:

$$\sigma _ { n } ^ { * } ( ( l _ { 1 } , l _ { 2 } ) , \lambda , 1 )$$

$$0 _ { n } ( ( l _ { 1 } , l _ { 2 } ) , \lambda , 1 ) \\ \colon = P _ { \lambda } \{ \text {there exists aVacant $L$-R $ \mathbb{L}_{n}$-crossing of $[0, l_{1}] \times [0, l_{2}]$} \} , \\ \\ \sigma _ { n } ^ { * } ( ( l _ { 1 } , l _ { 2 } ) , \lambda , 2 ) \\ \colon = P _ { \lambda } \{ \text {there exists aVacant $T$-B $ $\mathbb{L}_{n}$-crossing of $[0, l_{1}] \times [0, l_{2}]$} \} .$$

Now suppose (4.11) and (4.12) hold. For i = 1, 2 let {δ(n)}n≥1 be a se(u)   ( γ ( )   ∞ ← u  ' ← (u   ns n and σn((l3, l2), λ, 2) ≥ δ2(n). This is possible since σn((l1, l2), λ, 1) → σ*((l1, l2), λ, 1) and σn((l3, l2), λ, 2) → σ*((l3, l2), λ, 2) as n → ∞. We will now provide a lower bound for Pλ(D3 (r)). Consider the event

$$\ref ( D _ { 3 } ( r ) ) \, \colon = \, & \{ \text {there exists a variant } \mathbb { L } _ { n } \text {-path} \, s ^ { \prime \prime } = ( C _ { 0 } ^ { \prime \prime } , \dots , C _ { \mu } ^ { \prime \prime } ) \\ & \quad \text {such that } C _ { 0 } \cap ( [ l _ { 1 } / 4 , 7 l _ { 1 } / 4 ] \times \{ l _ { 2 } \} ) \neq \emptyset , \\ & C _ { \mu } ^ { \prime \prime } \cap ( \ref ( F ( r ) \cup \Gamma , ) ) \neq \emptyset , s ^ { \prime \prime } \subseteq \overline { \ J _ { 3 } ^ { + } ( r ) } \text { and }$$


<!-- p:113 -->


Clearly,

Also

$$A \, \text {is} \, 0 \\ P _ { \lambda } ( D _ { 3 } ( r ) \cup ( \ref ( D _ { 3 } ( r ) ) ) ) & = P _ { \lambda } \{ \exists \mathbb { L } _ { n - } \text {path} \, \hat { s } = ( \hat { C } _ { 0 } , \dots , \hat { C } _ { k } ) \text { for a } k \geq 1 \\ & \text {such that} \, ( \hat { C } _ { 1 } , \dots , \hat { C } _ { k } ) \subseteq J _ { 3 } ^ { + } ( r ) , \\ \hat { C } _ { 0 } \cap ( [ d _ { 1 } / 4 , 7 l _ { 1 } / 4 ] \times \{ l _ { 2 } \} ) & \neq \emptyset \text { and } \\ \hat { C } _ { k } \cap [ ( F ( r ) \cup \Gamma , ) \cup ( \ref ( F ( r ) \cup \Gamma , ) ) ] & \neq \emptyset \} \\ & \geq \sigma _ { n } ^ { * } ( ( l _ { 3 } , l _ { 2 } ) , \lambda , 2 ) \\ & \geq \delta _ { 2 } ( n ) ,$$

and hence, from (4.17), we have

$$P _ { \lambda } ( D _ { 3 } ( r ) ) \geq \delta _ { 2 } ( n ) / 2 .$$

Now let s′ := (C0, . .. , C′) be a self-avoiding L–R ILn-crossing of [0, l1 − R] × [0, l2] with C0 ∩ ({0} × [0, l2]) ≠ ∅, Ck ∩ ({l1 − R} × [0, l2]) ≠ ∅ and be, as defined earlier, the 'last intersection' of s' with {l1/4} × [0, l2]. Let Y (s') denote the second coordinate

H1 := {there exists a vacant L-R In-crossing s of [0, l1 − R] × [0, l2] with Y (s) ≤ l2/2},

H2 := {there exists a vacant L-R ILn-crossing s of [0, l1 − R] × [0, l2] with Y(s) ≥ l2/2}.

Clearly, Pλ(H1) = Pλ(H2) and Pλ(H1 ∪ H2) = Pλ{there exists a vacant L−R L-crossing s of [0, l1 − R] × [0, l2]}. Thus Pλ(H1) ≥ δ1 (n)/2. But, H1 ⊆ {R exists and Y(R) ≤ l2/2}, so

Pλ{R exists and Y (R) ≤ l2/2} ≥ δ1(n)/2. (4.19)

C% ∩ (l1/4, 7l1/4] × {2}) ∪ (ref(F(r) ∪ Γr))) = 0 for all k = 1, . . . , μ − 1}.

$$P _ { \lambda } ( D _ { 3 } ( r ) ) = P _ { \lambda } ( \text {ref} ( D _ { 3 } ( r ) ) ) .$$


<!-- p:114 -->


### 4.5 RSW - proof

Now we are in a position to prove the RSW lemma.

Proof of the RSW lemma First we show that

$$P _ { \lambda } \{ & \text {there exists a\/vacant $L-R$   $\mathbb{L}$-crossing $r^{\prime}$ of $[0, l_{1}] \times [0, l_{2}]$ with} \\ & Y ( r ^ { \prime } ) \leq l _ { 2 } / 2 \text { and there exists a\/vacant   $\mathbb{L}$-path $s^{\prime}$ with} \\ & s ^ { \prime } \cap F ^ { \prime } ( r ^ { \prime } ) \neq \emptyset , s ^ { \prime } \subseteq \overline { J _ { 3 } ^ { 3 } ( r ^ { \prime } ) } \text { and $s^{\prime} \cap ( [l_{1} / 4 , 7 l_{1}/4 ] \times \{ l_{2} \} ) \neq \emptyset \} } \\ & \geq C _ { 1 } ( \lambda , R ) \delta _ { 1 } ( n ) \delta _ { 2 } ( n ) / 4 ,$$

$$( 4 , 2 0 )$$

where C1(λ, R) = exp{−λ(3R + an)(2R + 2an)}. Here F′(r′) denotes the piece of r′ after the last intersection of r' with the line {l1/4} × [0, l2] and J3+ (r') is the closure of the region J3+ (r′), which is defined as in the definition of J3+ (r) in Section 4.3 with F′(r′) instead of F(r) ∪ Γ, and ref( F′(r')) instead of ref(F(r) ∪Γr).

To this end we observe that for an L-R Ln-crossing r of [0, l1 – R] × [0, l2],

$$\{ \mathcal { R } = r \} \cap A _ { r } \subseteq \{ \mathcal { R } = r , \Gamma _ { r } \text { is vacant} \} .$$

Indeed, if there are no balls centred in A', and no balls intersecting r then there cannot be any ball intersecting Γr. Moreover, for the L-R IL-crossing r ∪U Γr of [0, l1] × [0, l2], we have F′(r ∪ Γr) = F(r) ∪ Γr.

Thus from (ii) of Lemma 4.2, Lemma 4.3, (4.18), (4.19) and (4.21) we obtain

- Pλ {there exists a vacant L-R In-crossing r′ of [0, l1] × [0, l2] with

Y (r′) ≤ l2/2 and there exists a vacant Ln-path s'with

- s′∩F′(r′) ≠0, s′⊆ J3+(r′) and s′∩([1/4,7l1/4] ×{l2}) ≠0}

≥ Pλ {R exists , Y(R) ≤ l2/2, ΓR is vacant and D3(R) occurs}

$$& \quad S \, | \, | F \, ( \mathcal { R } ) \, \rangle \neq \mathcal { B } , \, \stackrel { \subseteq } { \sim } \mathcal { J } _ { 3 } \, ( \mathcal { R } \, ) \, \text { and } \, \mathcal { D } _ { 1 } \, | \, ( \mathcal { I } / 4 , \, \mathcal { I } _ { 1 } / 4 ) \, \times \, \{ \mathcal { R } \} \neq \mathcal { B } \} \\ & \quad \geq \, P _ { \lambda } \{ \mathcal { R } \, \text { exists } \, , \, Y ( \mathcal { R } ) \leq l _ { 2 } / 2 , \, \Gamma _ { \mathcal { R } } \, \text { is vacant and } \, D _ { 3 } ( \mathcal { R } ) \, \text { occurs} \} \\ & \quad = P _ { \lambda } \begin{pmatrix} \bigcup _ { ( r \colon Y ( r ) \leq l _ { 2 } / 2 ) } \{ \mathcal { R } = r , \, \Gamma _ { r } \, \text { is vacant and } \, D _ { 0 } ( r ) \, \text { occurs} \} \\ \\ = \sum P _ { \lambda } \{ \mathcal { R } = r , \, \Gamma _ { r } \, \text { is vacant and } \, D _ { 0 } ( r ) \, \text { occurs} \} \\ \\ \geq \sum P _ { \lambda } \{ \mathcal { R } = r \} \cap A _ { r } \cap D _ { 0 } ( r ) \\ \\ = \sum P _ { \lambda } \{ \mathcal { R } = r \} \} P _ { \lambda } ( A _ { r } \cap D _ { 0 } ( r ) | \{ \mathcal { R } = r \} ) \\ \\ \geq \sum P _ { \lambda } \{ ( \mathcal { R } = r ) P _ { \lambda } ( A _ { r } ) P _ { \lambda } ( D _ { 3 } ( r ) ) \\ \\ \geq \sum _ { r } \frac { 1 } { 2 } P _ { \lambda } ( \{ \mathcal { R } = r \} ) \delta _ { 2 } ( n ) \exp \{ - \lambda ( 3 R + a _ { n } ) ( 2 R + 2 a _ { n } ) \} \\ \\ \geq \frac { 1 } { 4 } \delta _ { 1 } ( n ) \delta _ { 2 } ( n ) \exp \{ - \lambda ( 3 R + a _ { n } ) ( 2 R + 2 a _ { n } ) \} .$$


<!-- p:115 -->


(In the calculations above, U, and ∑, are, respectively, the union and sum over all L–R IL n-crossings r of [0, l1 − R] × [0, l2] with Y (r) ≤ l2/2.) This proves (4.20).

Now, for any L–R crossing γ of [0, l1] × [0, l2], let F′(γ) denote the piece of γ after its last intersection with the line {l1/4} × [0, l2]. Also, let Y(γ) := inf {y : (l1/4, y) ∈ F′(γ)∩{l1/4} × [0, l2]} and J3+ (γ) the closure of J3+ (γ) := {(x, y) ∈ [l1/4, 7l1/4] × [0, l2] : (x, y) can be connected to [l1/4, 7l1/4} × {l2} by a continuous curve γ lying in [l1/4, 7l1/4] × [0, l2] and γ ∩ (F′(γ) ∪ ref( F′(γ))) = ∅}, where ref( F′(γ)) is the reflection of F′(γ) in {l1} × [0, l2}. Now making the lattice finer and taking limits in (4.22) along the sequence {an } chosen earlier, we obtain,

Pλ {there exists a vacant L-R crossing γ1L of [0, l1] × [0, l2] with Y(γ1L) ≤ l2/2 and there exists a vacant path γ1τ with γ1T∩F′(γ1τ) ≠0, γ1T ⊆ J3+(γ1L) and γ1τ∩([1/4,7l1/4]×{l2})≠0} ≥ [δ1δ2 exp(-6λ R2)]/4.

$$( 4 , 2 3 )$$

An iterative procedure will now complete the proof. Suppose the event described in (4.23) occurs; then γ1L U γ1τ contains a vacant path ζ connecting {11/4} × [0, l2/2] to [l1/4, 7l1/4] × {l2}. If for some M &gt; 0, ζ contains any point in the region [(l1/4) + M, ∞) × [0, l2], then γ1L ∪ γ1π provides a vacant L−R crossing of [0, (l1/4) + M] × [0, l2]. Otherwise, if ζ ⊂ ([0, (l1/4) + M] × [0, l2]), then consider a vacant L-R crossing γ2L of [l1/4, (l1/4) + M] × [0, /2] with Y2(γ2L) ≥ l2/2, where Y2(γ2L) is the second coordinate of the initial po   ( /1 = ( × {4/  7  : cs {1/4} × [0, l2/2] to {l1/4, 7l1/4] × {l2} and lies in [0, (l1/4) + M] × [0, l2], we have γ2L∩ζ ≠ ∅. Thus γ1L∪ γ1τ ∪ γ2L provides an L-R crossing of |0), (l1/4) + M] × [0, l2]. Hence, applying the FKG inequality, we have

Pλ {there exists a vacant L-R crossing of [0, (l1/4) + M] × [0, l2}} ≥ Pλ {the event in (4.23) occurs and there exists a vacant L-R crossing γ2L of [l1/4, (l1/4) + M] × [0, l2] with Y2(γ2L) ≥ l2/2} ≥ δ1δ2 exp{−6λR2}Pλ(V1)/4, (4.24)

where V1 = {there exists a vacant L-R crossing γ2L of [l1/4, (l1/4) + M] × [0, 2| with Y2(γ2L) ≥ l2/2}. Clearly

$$P _ { \lambda } ( V _ { 1 } ) \geq \sigma ^ { * } ( ( M , l _ { 2 } ) , \lambda , 1 ) / 2 ,$$


<!-- p:116 -->


and (4.24) and (4.25) yield

$$\sigma ^ { * } ( ( ( l _ { 1 } / 4 ) + M , l _ { 2 } ) , \lambda , 1 ) \geq \delta _ { 1 } \delta _ { 2 } \exp \{ - 6 \lambda R ^ { 2 } \} \sigma ^ { * } ( ( M , l _ { 2 } ) , \lambda , 1 ) / 8 .$$

Taking M = M0 := l1 in (4.26),

$$\sigma ^ { * } ( ( 5 l _ { 1 } / 4 , l _ { 2 } ) , \lambda , 1 ) & \geq \delta _ { 1 } \delta _ { 2 } \exp \{ - 6 \lambda R ^ { 2 } \} \sigma ^ { * } ( ( l _ { 1 } , l _ { 2 } ) , \lambda , 1 ) / 8 \\ & \geq \delta _ { 1 } ^ { 2 } \delta _ { 2 } \exp \{ - 6 \lambda R ^ { 2 } \} / 8 .$$

Again, from (4.26), taking M = M1 := M0 + l1/4, we have

$$\sigma ^ { * } ( ( 3 l _ { 1 } / 2 , l _ { 2 } ) , \lambda , 1 ) \geq \delta _ { 1 } \delta _ { 2 } \exp \{ - 6 \lambda R ^ { 2 } \} \sigma ^ { * } ( ( 5 l _ { 1 } / 4 , l _ { 2 } ) , \lambda , 1 ) / 8 ,$$

which after applying (4.27) yields a lower bound on σ*((3l1/2, l2), λ, 1). Repeating this procedure, we obtain

$$\sigma ^ { * } ( ( M _ { j + 1 } , l _ { 2 } ) , \lambda , 1 ) \geq \delta _ { 1 } \delta _ { 2 } \exp \{ - 6 \lambda R ^ { 2 } \} \sigma ^ { * } ( ( M _ { j } , l _ { 2 } ) , \lambda , 1 ) / 8 ,$$

where Mj = l1 +  l1, for every j ≥ 1. Thus, for every k ≥ 1, we can recursively obtain the lower bound for σ*((kl1, l2), λ, 1). This completes the proof of the theorem. □

### 4.6 Equality of the critical densities

In this section we show that, in two dimensions, the various critical densities defined in this chapter are all equal. Unfortunately, the higher dimensional analogue of this result is not known.

The vacancy structure in the continuum model corresponds to the dual' structure of the discrete percolation model on lattices. However, this correspondence is rather rough, in the sense that while the 'dual' structure of a discrete model can be defined without any reference to the original percolation model, the vacancy structure in the continuum arises as the complement of the occupancy structure. It is for this reason that analysing the 'dual' of a suitable discrete percolation model will not give us the equality of the critical densities defined through the vacancy structure as we were able to do in Theorem 3.4 for the critical densities defined through the occupancy structure.

The proof of the equality of the critical densities defined through the vacancy structure relies on the RSW theorem and as such the two-dimensional restriction of the RSW theorem carries through. However, a bonus of this proof is that we obtain a sharp transition in two dimensions; i.e., we obtain that λc = λ*. Thus, in two dimensions, for λ &lt; λc, we have a regime where there is no unbounded occupied component and there is at least one unbounded vacant component, wha       d n a     ast one unbounded occupied component. Of course, this statement is probabilistic and holds only with probability 1. Together with the results from Section 3.6 and the results in the next section, we see that in either of these regimes there is almost surely exactly one unbounded component of the appropriate type. We show the following:


<!-- p:117 -->


Theorem 4.3 For a two-dimensional Poisson Boolean model (X, ρ, λ) with ρ bounded almost surely, we have λ* = λ = λ*.

Theorem 4.4 For a two-dimensional Poisson Boolean model (X, ρ, λ) with ρ bounded almost surely, we have λc = λ.

Before we prove the theorems, we first state and prove a preliminary result. This lemma allows us to give a lower bound of the probability of the existence of an occupied crossing of a rectangle in terms of the probability of the existence of an occupied crossing of a bigger rectangle which is however of the same length in the direction of the crossing as that of the smaller rectangle.

Lemma 4.4 Let n and k be positive integers and let η &gt; 0 be such that

$$\sigma ^ { * } ( ( n , ( 1 + 2 k ) n ) , \lambda , 1 ) > \eta ;$$

then, for any t &gt; 0 and for some f (t, k, η) &gt; 0,

$$\sigma ^ { * } ( ( n , ( 1 + 2 t ) n ) , \lambda , 1 ) > f ( t , k , \eta ) .$$

(The point here is that f does not depend on n.)

Proof If t ≥ k then the lemma holds trivially. Otherwise, we set Hu := {0} × [(1 + k)n, (1 + 2k)n], Hm := {0} × [kn, (1 +k)n] and Hb := {0} × [0, kn] and for j = u, m or b we define the events Aj := {there is an L-R vacant crossing s of the rectangle [0, n] × [0, (1 + 2k)n] with s ∩ Hj ≠ Ø}. Clearly, Au ∪ Am ∪ Ab = {there exists an L-R vacant crossing of [0, n] × [0, (1 +2k)n]}. Moreover, since Au, Am and Ab are all decreasing events, applying the FKG inequality and noting that Pλ(Au) = Pλ(Ab), we have

$$1 - \sigma ^ { * } ( ( \pi , ( 1 + 2 k ) n ) , \lambda , 1 ) & = P _ { \lambda } ( A _ { u } ^ { c } \cap A _ { m } ^ { c } \cap A _ { b } ^ { c } ) \\ & \geq P _ { \lambda } ( A _ { u } ^ { c } ) P _ { \lambda } ( A _ { m } ^ { c } ) P _ { \lambda } ( A _ { b } ^ { c } ) \\ & = ( 1 - P _ { \lambda } ( A _ { m } ) ) ( 1 - P _ { \lambda } ( A _ { b } ) ) ^ { 2 } .$$

'Thus at least one of the following (4.30) and (4.31) holds:

$$P _ { \lambda } ( A _ { m } ) & \geq 1 - ( 1 - \sigma ^ { * } ( ( n , ( 1 + 2 k ) n ) , \lambda , 1 ) ) ^ { 1 / 3 } \\ & \geq 1 - ( 1 - \eta ) ^ { 1 / 3 } \colon = \eta ^ { \prime } \text { (say),}$$


<!-- p:118 -->


Figure 4.8. The three possibilities Bu, Bm and Bb.

$$P _ { \lambda } ( A _ { b } ) \geq 1 - ( 1 - \sigma ^ { * } ( ( n , ( 1 + 2 k ) n ) , \lambda , 1 ) ) ^ { 1 / 3 } .$$

Suppose first (4.30) holds. We observe that Am ⊆ Bu U Bm ∪ Bb, where

Bu := {there exists a vacant L-R crossing of [0, n] × [kn, (1 + 2k)n]},

Bm := {there exists a vacant T-B crossing of [0, n] × [kn, (1 + k)n]},

Bb := {there exists a vacant L-R crossing of [0, n] × [0, (1 + k)n]}

(see Figure 4.8). Since Bu, Bm and Bb are all decreasing events, (4.30) and an application of the FKG inequality yields

$$1 - \eta ^ { \prime } & \geq P _ { \lambda } ( B _ { u } ^ { c } \cap B _ { m } ^ { c } \cap B _ { b } ^ { c } ) \\ & \geq ( 1 - P _ { \lambda } ( B _ { m } ) ) ( 1 - P _ { \lambda } ( B _ { b } ) ) ^ { 2 } .$$

Thus at least one of the following (4.32) and (4.33) must hold:

$$P ( B _ { m } ) \geq 1 - ( 1 - \eta ^ { \prime } ) ^ { 1 / 3 } ,$$

$$P ( B _ { b } ) \geq 1 - ( 1 - \eta ^ { \prime } ) ^ { 1 / 3 } .$$

Next, suppose that (4.31) holds. We observe that Ab ⊆ Bm U Bb and so an application of the FKG inequality implies that at least one of (4.32) and (4.33) is true. In either case (i.e., (4.32) or (4.33)), the monotonicity of the crossing probabilities yields that

$$\sigma ^ { * } ( ( n , ( 1 + k ) n ) , \lambda , 1 ) \geq 1 - ( 1 - \eta ^ { \prime } ) ^ { 1 / 3 } .$$

Now take k0 := k in (4.34) and define k1 := k0/2. Then we have σ*((n, (1 + 2k1)n), λ, 1) ≥ 1 − (1 − η0)1/3, where η0 := 1 −(1 − σ*((n, (1 + 2k0)n),


<!-- p:119 -->


λ, 1))1/3. Defining successively kj := kj-1/2 for j ≥ 1, we see that σ*((n, (1 + 2kj)n), λ, 1) ≥ 1−(1−σ*((n, (1 +2kj−1)n), λ, 1))1/3. Since kj ↓ 0 as j ↑∞, this iterative procedure yields (4.29) for a suitable f(t, k, η) &gt; 0. 口

Proof of Theorems 4.3 and 4.4 Throughout this proof we assume that

$$0 < \rho \leq R ,$$

for some R &gt; 0, and that the Poisson Boolean model is defined on IR2. First we list some of the inequalities we obtain quite easily. It is clear that

$$\lambda _ { c } ^ { * } \leq \lambda _ { D } ^ { * } .$$

$$\lambda _ { D } ^ { * } \leq \lambda _ { S } ^ { * } .$$

In view of (4.36) and (4.37), to prove Theorem 4.3 and 4.4, it suffices to show that

$$\lambda _ { c } \leq \lambda _ { c } ^ { * } ,$$

$$\lambda _ { S } ^ { * } \leq \lambda _ { c } .$$

To show (4.38), let λ &lt; λc and note that if instead of vacancy we consider occupancy in the proof of part (b) of Theorem 4.1 we obtain

$$\sum _ { k = 1 } ^ { \infty } \sigma ( ( 3 ^ { k } , 3 ^ { k + 1 } ) , \lambda , 1 ) < \infty .$$

However, σ((3k, 3k+1), λ, 1)+ σ*((3k, 3k+1), λ, 2) = 1 because, if an occupied crossing does not exist in the horizontal direction then, almost surely, there must exist a vacant crossing in the vertical direction and vice versa. Hence, from (4.40) and the Borel-Cantelli lemma we have

$$P _ { \lambda } \{ \text {there is avacant $T-B$ crossing $t_{k}$ of $[0, 3^{k}] \times [0, 3^{k+1}]$} \\ \text {for all large $k\} = 1 . }$$

The rotation invariance allows us to restate (4.41) as

$$P _ { \lambda } \{ \text {there is a vacant L-R crossing} \, l _ { k } \, \text {of} \, [ 0 , \, 3 ^ { k + 2 } ] \times [ 0 , \, 3 ^ { k + 1 } ] \\ \text {for all large} \, k \} = 1 .$$

Now a vertical crossing tk of [0, 3k] × [0, 3k+1] and a horizontal crossing lk of [0, 3k+2] × [0, 3k+1] must intersect. Also tk+1 and lk must intersect. Thus the vacant crossings tk and lk defined in (4.41) and (4.42) combine to give an

Moreover, by (4.4), Morcovr, uy (4.4),

and unbounded vacant component in the first quadrant. Hence, using the fact that vacant components are open, we obtain


<!-- p:120 -->


$$P _ { \lambda } \{ d ( V ( x ) ) = \infty \text { for some } x \in Q ^ { 2 } \} = 1 ,$$

where Q2 is the set of all points in IR2 with rational coordinates. Since

$$P _ { \lambda } \{ d ( V ( x ) ) = \infty \text { for some } x \in Q ^ { 2 } \} \\ \leq \sum _ { x \in Q ^ { 2 } } P _ { \lambda } \{ d ( V ( x ) ) = \infty \} ,$$

$$x \in Q ^ { 2 }$$

we have by translation invariance Pλ {d(V) = ∞} &gt; 0. Thus λ ≤ λ* and this completes the proof of (4.38).

Finally, to prove (4.39), we show that for λ &lt; λ*, there are infinitely many annuli around the origin, each annulus containing a vacant circuit with a probability larger than a positive constant. Thus a Borel-Cantelli argument would show that, with probability 1, there exist infinitely many circuits surrounding the origin and hence both d(W) and l(W) are finite. To this end we introduce another critical density:

s := sup{λ : there exists 0 ≤ n1 ≤ n2 · · · with nk ↑ ∞ as k ↑ ∞, such that, for every k ≥ 1 and for some δ &gt; 0, the following hold:

- n  1-s (1)
- (ii) σ*((n2k−1, n2k), λ, 1) ≥ δ &gt; 0,
- (iii) σ*((5n2k−1/4, n2k), λ, 2) ≥ δ &gt; 0}.

We first show that

$$\lambda _ { S } ^ { * } \leq \hat { \lambda } _ { S } ^ { * } .$$

$$( 4 . 4 3 )$$

Let λ &lt; λ*. Then there exists an increasing sequence {mk}k≥1 of positive numbers, with mk ↑ ∞ as k ↑ ∞, and some η &gt; 0 such that σ*((mk, 3mk), λ, 1) &gt; η for each k ≥ 1. Now, for every k ≥ 1, we take n2k-1 = 5mk/6 and n2k = m k. Applying first the monotonicity property of the crossing probabilities and Lemma 4.4, we have σ*((n2k−1, n2k), λ, 1) &gt; δ and σ*((5n2k−1/4, n2k), λ, 2) &gt; δ for some 0 &lt; δ &lt; η and for every k ≥ 1. Thus λ ≤ λ* and consequently λ*s ≤ λs. This proves (4.43).

Next suppose that for some δ &gt; 0 and for every k ≥ 1, n2k and n2k-1 are such that (i), (ii) and (iii) in the definition of λ hold. For every k ≥ 1, we put

$$m _ { k } = n _ { 2 k - 1 } \ \text { and } \ \tilde { m } _ { k } = m _ { k } + n _ { 2 k } .$$


<!-- p:121 -->


Figure 4.9. The events Å+ , Å− , B+ and B−.

We also assume that the sequence {nk}k≥1 is chosen so that

$$m _ { k + 1 } > 3 m _ { k } + 2 R .$$

Consider the rectangles

$$A _ { k } ^ { + } & = [ - 3 m _ { k } , 3 m _ { k } ] \times [ m _ { k } , \tilde { m } _ { k } ] , \\ A _ { k } ^ { - } & = [ - 3 m _ { k } , 3 m _ { k } ] \times [ - \tilde { m } _ { k } , - m _ { k } ] , \\ B _ { k } ^ { + } & = [ m _ { k } , \tilde { m } _ { k } ] \times [ - 3 m _ { k } , 3 m _ { k } ] , \\ B _ { k } ^ { - } & = [ - \tilde { m } _ { k } , - m _ { k } ] \times [ - 3 m _ { k } , 3 m _ { k } ] . \\ = + \text { or } & = \text { we let}$$

Also, for € = + or −, we let

Ãk = {there exists an L-R vacant crossing of Ak}

and nun Bk = {there exists a T-B vacant crossing of B }.

lor an illustration of these events, see Figure 4.9. By the invariance properties of the model,

$$P _ { \lambda } ( \tilde { A } _ { k } ^ { + } ) = P _ { \lambda } ( \tilde { A } _ { k } ^ { - } ) = P _ { \lambda } ( \tilde { B } _ { k } ^ { + } ) = P _ { \lambda } ( \tilde { B } _ { k } ^ { - } ) = \sigma ^ { * } ( ( 6 n _ { 2 k - 1 } , n _ { 2 k } ) , \lambda , 1 ) .$$


<!-- p:122 -->


By the RSW lemma, we have

$$\sigma ^ { * } ( ( 6 n _ { 2 k - 1 } , n _ { 2 k } ) , \lambda , 1 ) \geq K ( \lambda , R ) g ( \delta ) ,$$

for some K(λ, R) &gt; 0 and g(δ) &gt; 0. For both ∈ = + or −, the events Åk and Ã are decreasing, so we have, from (4.45) and (4.46) and the FKG inequality,

$$P _ { \lambda } ( \tilde { A } _ { k } ^ { + } \cap \tilde { A } _ { k } ^ { - } \cap \tilde { B } _ { k } ^ { + } \cap \tilde { B } _ { k } ^ { - } ) & \geq P _ { \lambda } ( \tilde { A } _ { k } ^ { + } ) P _ { \lambda } ( \tilde { A } _ { k } ^ { - } ) P _ { \lambda } ( \tilde { B } _ { k } ^ { + } ) P _ { \lambda } ( \tilde { B } _ { k } ^ { - } ) \\ & \geq \{ \sigma ^ { * } ( ( 6 n _ { 2 k - 1 } , n _ { 2 k } ) , \lambda , 1 ) \} ^ { 4 } \\ & \geq \{ K ( \lambda , R ) g ( \delta ) \} ^ { 4 } .$$

B   a  ei =:            in the annulus ([0, mk] × [0, mk])\([0, mk] × [0, mk])} (see Figure 4.9 and note that by our choice of m k and ñk, 3mk &gt; mk). Thus, from (4.47), we have

$$\sum _ { k = 1 } ^ { \infty } P _ { \lambda } ( G _ { k } ) \geq \sum _ { k = 1 } ^ { \infty } \{ K ( \lambda , R ) g ( \delta ) \} ^ { 4 } = \infty .$$

However, (4.44) guarantees that {Gk}k≥1 is a sequence of independent events, so that the Borel–Cantelli lemma yields that Pλ {Gk occurs infinitely often} = 1. But Pλ {there are infinitely many vacant circuits around the origin} ≥ Pλ{Gk occurs infinitely often} = 1, whence

$$P _ { \lambda } \{ d ( W ) = \infty \} = 0 .$$

Now, if λ &lt; λ *s, t then there exists a δ &gt; 0 and a sequence {nk }k≥1 satisfying This, along with (4.43), proves (4.39) and completes the proof of Theorems 4.3 and 4.4.

An immediate consequence of this theorem is that, in two dimensions, for λ &gt; λc, σ*((n, 3n), λ, 1) → 0 as n → ∞ and thus σ((n, 3n), λ, 2) → 1 as n → ∞, while for λ &lt; λc, σ((n, 3n), λ, 1) → 0 as n → ∞ and thus σ*((n, 3n), λ, 1) → 1 as n → ∞. This argument can be easily generalised along the lines of the proof of Lemma 4.4 to yield

Corollary 4.1 Consider a Poisson Boolean model (X, ρ, λ) in two dimensions with ρ bounded. For λ &gt; λc, we have σ((kn, n), λ, 1) → 1 as n → ∞ for every k ≥ 1, and for λ &lt; λc, we have σ*((kn, n), λ, 1) → 1 as n → ∞ for every k ≥ 1.

Theorem 4.5 Consider the Poisson Boolean model (X, ρ, λ) on IRd with 0 &lt; ρ ≤ R for some R &gt; 0. For d = 2, we have Pλc {d(W) = ∞} = 0. However, for any d ≥ 2, Eλc(d(W)) = ∞.


<!-- p:123 -->


Proof Suppose Pλc {d(W) = ∞} &gt; 0. We shall show that this implies that

$$\sigma ^ { * } ( ( n , 3 n ) , \lambda _ { c } , 1 ) \to 0 \, \text {as} \, n \to \infty .$$

Indeed, if (4.49) does not hold, then there exist δ &gt; 0 and an infinite sequence n1, n2, . . . such that, for all i ≥ 1, σ*((n, 3n), λc, 1) ≥ δ. Without loss of generality we may assume that, for all i ≥ 1,

$$6 n _ { i + 1 } \geq 9 n _ { i } + 2 R .$$

The RSW lemma implies that there exist 0 &lt; δ0 &lt; δ such that for all i ≥ 1,

$$\sigma ^ { * } ( ( 1 8 n _ { i } , 3 n _ { i } ) , \lambda _ { c } , 1 ) \geq \delta _ { 0 } .$$

As in the proof of the previous theorem, for every i ≥ 1, the FKG inequality together with (4.51) allows us to construct vacant circuits in the annulus B18n \ B15n with a probability larger than δ4. Thus, for Ei := {there exists a vacant circuit in the annulus B18n\B15n), we have

$$\sum _ { i = 1 } ^ { \infty } P _ { \lambda _ { c } } ( E _ { i } ) = \infty .$$

By our choice (4.50) of n, E1, E2, ... is a sequence of independent events; thus an application of the Borel-Cantelli lemma yields

$$P _ { \lambda _ { c } } \{ E _ { i } \text { occurs infinitely often} \} = 1 ,$$

and it follows that Pλc {d(W) = ∞} = 0. This contradiction establishes (4.49).

To complete the proof of the first part of the theorem, note that (4.49) implies that, for some N ≥ 0,

$$\sigma ^ { * } ( ( N , 3 N ) , \lambda _ { \epsilon } , 1 ) < \kappa _ { 0 } ,$$

where κo is as in Lemma 4.1. As in Chapter 3, since the event {there is a vacant L-R crossing of the rectangle [0, N] × [0, 3N]} depends on the bounded rectangle [−R, N + R] × [− R, 3N + R], σ*((N, 3N), λ, 1) is a continuous function of λ. Thus from (4.52) we have that for some λ &lt; λc,

$$\sigma ^ { * } ( ( N , 3 N ) , \lambda , 1 ) < \kappa _ { 0 } .$$

However, (4.53) implies from Lemma 4.1 that, for this λ, Pλ {d(V) = ∞} = 0. This contradicts the fact that λc = λ and thus proves the first part of the theorem.

To show the second part of the theorem, observe that if Eλc (d(W)) &lt; ∞, then from Theorem 2.4, we have that

$$P _ { \lambda _ { c } } \{ d ( W ( B _ { 1 } ) ) \geq a \} \leq C _ { 1 } e ^ { - a C _ { 2 } }$$


<!-- p:124 -->


for some positive constants C1 and C2. Now let Dk = k + B1 for k ∈ Zd. Clearly, for the existence of an occupied crossing in the shorter direction of the rectangle [0, n] × [0, 3n] × · . . × [0, 3n], there must be an occupied component of diameter at least n from some Dk with k = (k1, ..., ka), k1 = 0 and 0 ≤ k; ≤ 3n. Hence,

$$& \leq k _ { i } \leq 5 n . \text { Hence} , \\ & \quad \sigma ( ( n , 3 n , 3 n , \dots , 3 n ) , \lambda _ { c } , 1 ) \\ & \quad \leq \ P _ { \lambda _ { c } } \{ d ( W ( D _ { k } ) ) \geq n \text { for some } k = ( k _ { 1 } , \dots k _ { d } ) \\ & \quad \text { with } k _ { 1 } = 0 \text { and } 0 \leq k _ { 1 } \leq 3 n \} \\ & \quad \leq \ ( 3 m ) ^ { d - 1 } C _ { 1 } e ^ { - n C _ { 2 } } \\ & \quad \to 0 \text { as } n \to \infty \\ \text {here the last inequality follows from } ( 4 . 5 ) . \text { For } n \text { sufficiently large} , ( 4 . 5 )$$

where the last inequality follows from (4.54). For n sufficiently large, (4.55) yields that

$$\sigma ( ( n , 3 n , 3 n , \dots , 3 n ) , \lambda _ { c } , 1 ) < \kappa _ { 0 } ,$$

A continuity argument as in the previous part yields, for some λ &gt; λc,

$$\sigma ( ( n , 3 n , 3 n , \dots , 3 n ) , \lambda , 1 ) < \kappa _ { 0 } .$$

This along with Lemma 3.3 shows that for this λ, Pλ {d(W) = ∞} = 0, which contradicts the fact that λ &gt; λe. This completes the proof of the theorem.

### 4.7 Uniqueness

In Section 3.6, it was shown that in a Poisson Boolean model, there can be at most one unbounded occupied component. This section is devoted to the analogous result for the vacant region. As in the occupancy case, the result holds in its most general form:

Theorem 4.6 In a Poisson Boolean model (X, ρ, λ), there can be at most one unbounded vacant component a.s.

According to Proposition 3.1 we can with no loss of generality assume in this section that

$$E \rho ^ { d } < \infty .$$

The idea of the proof is similar to that in Section 3.6. There is, however, one extra difficulty. In the proof for occupancy, we used the fact that different occupied components contain different points of the process and that the density of such points is finite. We can not use such a direct argument here. We have to find other objects which have finite density and which can not be 'shared' by different vacant components. To this end, we state the following geometric result:


<!-- p:125 -->


Lemma 4.5 If k d-dimensional balls intersect the unit cube [0, 1]a then the vacant region inside the unit cube has at most cakd connected components, where cd is a constant which depends only on the dimension.

Proof For ease of exposition, we first give the proof for the case d = 3. Without loss of generality we can assume that no ball is contained in the union of the others, since adding this particular ball would not affect the number of vacant components. So we consider three balls, none of which is contained in the union of the other two. We claim that the intersection of the boundaries of these balls consist of at most two points. To see this, note that if the intersection of the boundaries of the first two balls is not empty, it is the boundary γ of some circle. Denote the plane containing this circle by H. The intersection of all three boundaries can be larger than two points only if the intersection of the third ball with H is γ. It is easy to check that in this case there is a ball which is contained in the other two, a contradiction. We call a point in the intersection of three boundaries a triple point. Now each vacant component in [0, 1]a which does not intersect the boundary of the cube contains at least one triple point on its boundary, and a triple point can belong to only one vacant component. Hence there are at most 2() vacant components which do not intersect the boundary of the unit cube. Next, we look at the intersection of vacant components with the faces of the cube. The intersection of a three-dimensional ball with a face is v l l  va cl l ac t  at e unit cube but does not intersect any of its edges must contain at least one point of intersection of two such two-dimensional balls. For each face therefore there caum e  sqt te u sl uaat os  so e  ost ) for all the faces of the cube. Finally, an analogous argument shows that e + t t t e t t  t  t t n Hence, the total number of vacant components is bounded by c3k3 for a suitable constant c3. The argument in higher dimensions is essentially the same and is omitted. □

A random variable which has a Poisson distribution has finite moments of all orders. Combining Lemma 3.1, Lemma 4.5 and the fact that the box B is contained in the ball S(0, n√), we conclude:

Proposition 4.1 In a Poisson Boolean model, the number of connected components in V ∩ Bn has inite expectation for all n.


<!-- p:126 -->


As in the occupancy case, we first show that the number of unbounded vacant components can be only zero, one or infinity:

Proposition 4.2 In a Poisson Boolean model, the number of unbounded vacant components equals either zero, one or infinity a.s.

Proof Using ergodicity as before, we see that the number of unbounded vacant Go       t t t n n     o any region A ⊂ Rd, we denote by V [A] the vacant region which we obtain after we remove all points (and associated balls) in the complement Ao of A. Using the assumption that the model admits K unbounded vacant components, Lemma 3.1, and the obvious fact that the number of vacant unbounded components can not increase by removing finitely many balls, we conclude that for all n, V [Bc] contains no more that K unbounded vacant components a.s. For all positive integers n, let En be the event that all unbounded vacant components in V[B] have non-empty intersection with Bn. For n large enough, we have P(Èn) &gt; 0. Sns  ee  sne  n y ne   iy  eck that the event

####### En∩ {there are at most L1balls which intersect

B and all these balls have radius at most L2}

has positive probability. Now consider the annulus B+L2\ B. We partition this annulus using the integer lattice and let C be the (finite) collection of cells in this lattice. Since C is finite, we can choose non-random cells W1, . . . , WL, in C such that forW :=W1U..∪WL1the event

Fn := {all unbounded vacant components in V[(Bn ∪ W)c] have non-empty intersection with B and all balls with non-empty intersection with Bn are centred in B U W}

has positive probability. Note that Fn depends only on the points of the point process outside B ∪ W and their associated balls. Hence,

P(Fn ∩ {X(Bn ∪ W) = 0}) = P(Fn)P(X(Bn ∪W) = 0) &gt; 0.

But if Fn ∩ {X(B ∪ W) = 0} occurs, then there is only one unbounded vacant component. This is the desired contradiction and completes the proof. □

Proof of Theorem 4.6 The idea of the proof is similar to that in the proof of Theorem 3.6. However, the application of Lemma 3.2 is much easier here for reasons which will be explained below.


<!-- p:127 -->


According to Proposition 4.2 we need to rule out the possibility of having infinitely many unbounded vacant components. As before, we proceed by assuming that there are infinitely many such components and we want to derive a contradiction. It follows from the proof of Proposition 4.2 that we can find boxes Bn C Bm such that with positive probability η, say, Bn is completely contained in a vacant unbounded component V′ such that V'∩ B contains at least three disjoint unbounded components. If this is the case, we call Bm an encounter box, and B its central box. The three unbounded components of V′∩BC are again called branches. Translating this event over the vector 2mz, m for z ∈ Zd , gives the requirement for B2mz to be an encounter box. For all L, B2m contained in the box the expected number of encounter boxes of the form B2 m BmL is equal to ηLd. Now any branch of an encounter box in BmL intersects AL := Bm(L +1) \ mL and hence contains at least one component of Cc ∩ B2mz for some z ∈ Zd such that B2mz C AL. (Recall that Cc is the vacant region in space.) We choose one such component for each branch b and call it Vb. Now we want to apply Lemma 3.2. For this, let R be the set of all central boxes corresponding to encounter boxes in BmL. For r ∈ R, the sets Ct) are defined as follows. Choose a branch b of the encounter box to which r belongs. Take all central boxes of other encounter boxes which are contained in b, together with Vb which is chosen before. Together these elements form one of the sets C(i) . It is obvious that card(C(i) ≥ 1 for all r and i. Let S consist of all central then yields the conclusion that card(S) ≥ 2 card(R) + 2. Hence the number of components Vb must be at least card(R) + 2 since S consists of the union of these components together with card(R) other elements. Thus the expected η Ld. However, it follows from Proposition 4.1 that this expected number can be at most c Ld-1 for some constant c &gt; 0, and this gives the desired contradiction for L sufficiently large. 口

REMAR K: It is instructive to compare this proof to the proof of Theorem 3.6. The reason that the application of Lemma 3.2 is so much easier here is the fact that in our definition, a branch in the occupancy case need not contain points in the annulus AL. For a vacant branch b, the component Vb defined above has to exist. This means that the volume-boundary argument is much easier in the latter case.

### 4.8 Continuity of the percolation function

In this section we investigate to what extent we can prove analogues of Theorem 3.9 and Theorem 3.7 for vacancy. For this, we define the vacant percolation function θ*(λ) as the probability that in (X, ρ, λ) the vacant component of the origin is unbounded. The corresponding critical density is λ*(ρ), which can now be written as λ*(ρ) = sup{λ : θ*(λ) &gt; 0}.


<!-- p:128 -->


It was shown in Theorem 4.4 that whenever ρ is bounded almost surely and the dimension is 2, λ*(ρ) = λc(ρ). In conjunction with Theorem 3.7 this trivially gives that in dimension 2, λ*(ρk) → λ*(ρ) whenever all radii are uniformly bounded and ρk ⇒ ρ. Note, however, that in the proof of Theorem 3.7 we used the fact that λs = λc. The corresponding statement for vacancy is only known in two dimensions (Theorem 4.3).

What we can show in full generality is the continuity of the vacant percolation function as a function of λ, at least for λ ≠ λ*(ρ):

Theorem 4.7 In a Poisson Boolean model (X, ρ, λ), the vacant percolation function θ* is a continuous function of λ for all λ ≠ λ(ρ).

Proof As in the proof of Theorem 3.9, {d(V) = ∞} is the decreasing limit of the events Fn := {0 ~ ∂(Bn)} and Pλ(Fn) is continuous in λ. Hence θ* is the decreasing limit of a sequence of non-increasing continuous functions and is therefore continuous from the left.

For continuity from the right we fix λo &lt; λ*. As in the proof of Theorem 3.9 we couple all processes (X, αρ, λo) on the same probability space, this time for all α ≥ 1. Writing Vα for the vacant component of the origin in (X, αρ, λ0), we need to show that

$$P ( d ( V _ { 1 } ) = \infty , d ( V _ { \alpha } ) < \infty \text { for all } \alpha > 1 ) = 0 .$$

In words, if d(V1) is infinite, then there is an α &gt; 1 such that if we multiply all radii by α, the vacant component of the origin remains unbounded. From scaling as in the proof of Theorem 3.9 we observe that for α &gt; 1 small enough, component Uα, say (Theorem 4.6). It follows that Uα is contained in V1. This implies that there exists a bounded, closed curve γ ⊂ V1 connecting the origin to Ua. At this point, the argument is different from the occupancy case. From Lemma 3.1 and the fact that E((αρ)d) &lt; ∞ by assumption, we see that there are a.s. only finitely many balls in (X, αρ, λ0) which intersect γ and none of these balls intersect γ when the radius is reduced to the original value. It follows that for some value of α &gt; 1, no ball in (X, αρ, λo) intersects γ and the proof is complete. 0


<!-- p:129 -->


### 4.9 Notes

The first seven sections of this chapter are from Roy (1990), the uniqueness result of Section 4.8 is from Meester and Roy (1994), and the continuity result of Section 4.9 is from Sarkar (1995). The RSW lemma is an analogue of the RSW lemma of discrete percolation obtained by Russo (1978) and Seymour and Welsh (1978). One of the first applications of this result in discrete percolation was by Kesten (1980) to show pe = . Subsequently, it has been used to obtain a variety of results in two-dimensional discrete percolation. One of the main open questions in percolation theory is to obtain a higher-dimensional analogue of the RSW lemma. The difficulty in this arises from the fact that a crossing in one direction of a cube may not intersect a crossing in another direction of the cube. Although, in three dimensions, if we consider a sheet crossing in one direction and another sheet crossing in another direction, then they will intersect. A suitable higher-dimensional analogue of this may also be formulated. The RSW theorem for this will go through; however, for the full import of the result in higher dimensions, we need line crossings.

In the discrete case, the notion of the lowest crossing was introduced and conditioned on the lowest crossing; the configuration above' the crossing and the configuration 'below' the crossing are independent. In the continuum case, this independence does not exist and, as such, the term Ck(λ, R) enters the picture. The independence structure of discrete percolation allows one to formulate a stronger RSW lemma for the discrete than the continuum version we have here. In particular, in the discrete percolation setup, it may be shown that if the crossing probability of a smaller rectangle tends to 1 then the crossing probability of the larger rectangle also tends to 1. Here, however, the term Ck(λ, R) prevents such a strong result.

More recently, Alexander (1994) has obtained an RSW lemma for occupied crossings with fixed sized balls. The proof of this result also proceeds through a lowest crossing argument. The difficulty here lies in the definition of a lowest occupied crossing. Alexander has an ingenious way of defining the lowest occupied crossing to obtain enough conditional independence between the region above and the region below the conditioned lowest crossing. The steps of this proof are significantly different from that of the RSW lemma for vacant crossings given in this chapter. The dependency structure persists here too and this brings in a term Ck(λ, R) in the formulation of the RSW result in the occupied case. Thus the statement of the result is quite similar to the RSW lemma for vacant crossings, the only difference being that σ* has to be replaced by σ. This theorem will also provide the vacant counterpart of the first part of Theorem 4.5 to yield that Pλ* {d(V) = ∞} = 0 in two dimensions. However, the second part of this theorem needs a vacancy version of Theorem 2.4 which is not known to be true.


<!-- p:130 -->


5

#### Distinguishing features of the Poisson Boolean mmode

The title of this chapter needs some explanation. The word 'distinguishing' refers to two facts. In the first place, we are going to describe some fundamental differences between Boolean models with balls of a fixed radius and balls with random radii. These differences have to do with the so-called covered volume fraction and with the phenomena of compression and rarefaction. These notions will be introduced shortly. In the second place, the phenomena described in this chapter do not have natural analogues in the discrete setting.

### 5.1 The covered volume fraction

Loosely speaking, the covered volume fraction (CVF) is supposed to be the 'fraction' of space which is covered by balls. In order to give a more precise definition, let us first recall from (3.3) that the probability that the origiņ is covered in the Poisson Boolean model (X, ρ, λ) is equal to 1 – e−λπdρ . It then follows easily from Fubini's theorem that the expected Lebesgue measure of the occupied region in the unit cube is equal to the same number. The ergodic theorem now guarantees that if B is the box [—n, n]a as usual, then the limit

$$\lim _ { n \to \infty } \frac { 1 } { ( 2 n ) ^ { d } } \ell ( B _ { n } \cap C )$$

exists a.s. and equals 1 — e−λπ&amp; Eρa. The limit in (5.1) is taken as the definition of the CVF:

Definition 5.1 The covered volume fraction of a Poisson Boolean model (X, ρ, λ) is defined as the almost sure limit

and is therefore equal to 1 – e−λπdEρd.


<!-- p:131 -->


We remark that in case Eρa = ∞, the CVF is equal to 1.

Definition 5.2 The critical CVF of a Poisson Boolean model (X, ρ, λ) is defined as

$$A _ { c } ( \rho ) \colon = 1 - e ^ { - \lambda _ { c } ( \rho ) \pi _ { d } E \rho ^ { d } } .$$

Thus Ac(ρ) is the fraction of space covered at criticality. Now consider two Boolean models, one with balls of a fixed radius r1 and the other with balls of a fixed radius r2, and denote their critical CVF by Ac(r1) and Ac(r2) respectively. Ilo   o   oa oo o o at

$$A _ { c } ( r _ { 1 } ) = A _ { c } ( r _ { 2 } ) .$$

Hence in any Poisson Boolean model with balls of a fixed radius, the fraction of space covered at criticality is a constant depending only on the dimension and CVF if the balls do not have a fixed radius. We shall show that the critical CVF is certainly not a universal constant among all possible Boolean models.

Theorem 5.1 Consider Boolean models (X, ρ, λ) in IRd. There exists a random variable ρ taking values a &gt; 0 and b &gt; 0 with probability p and 1 − p respectively, where a ≠ b, 0 &lt; p &lt; 1 such that

$$( 5 . 2 )$$

Proof For ease of notation we give the proof for the case d = 2 and we notation becomes rather tedious to handle. Let 0 &lt; r1 &lt; r2 &lt; ∞ be arbitrary positive numbers. Fix €, δ &gt; 0 such that

$$( 2 - \epsilon - \delta ) A _ { c } - ( 1 - \epsilon ) ( 1 - \delta ) A _ { c } ^ { 2 } > A _ { c } .$$

The expression in (5.3) will become clear in a moment. Next we choose λ2 &lt; λc(r2) such that the CVF of (X, r2, λ2) is equal to (1 − €)Ac. Also choose λ1 &lt; λc(r1) such that the CVF of (X, r1, λ1) is equal to (1 − δ)Ac. Note that both processes are subcritical. Next we consider the superposition of these processes. We claim that the CVF of this superposition is strictly larger than Ac. To see this, note that the probability that the origin is covered in the superposition of the two processes is just the left-hand side of (5.3) and the claim follows.

Now consider the process (X, r1, λ1) and scale it by a factor α &lt; 1 to obtain a.    (         i (X, r1, λ1) consists of the points {x1, x2, . . .}, with associated balls of radius r1, then the scaled model consists of the points {αx1, αx2, . . .} with associated balls of radius αr1 . (Note that in this way, we couple all processes together for α &lt; 1.) The CVF of (X, αr1, α−2λ1) does not depend on α, whence it follows from (5.3) that the CVF of the superposition of (X, r2, λ2) and (X, αr1, α−2λ1) is strictly larger than Ac. Our goal now is to show that this superposition is subcritical for α sufficiently small.


<!-- p:132 -->


Fix a 0 &lt; κ &lt; κ0 where κ0 is as in Lemma 3.3. Since λ2 &lt; λc(r2), Theorem 3.5 implies that λ2 &lt; λs(r2) and we can thus find a number N so large that

$$\sigma ( ( N , 3 N ) , \lambda _ { 2 } , 1 ) < \frac { 1 } { 3 } \kappa .$$

If there is no occupied L-R crossing in [0, N] × [0, 3N], then there is a vacant T-B crossing defined in the obvious way. In other words, there is at least one component in ([0, N] ×[0, 3N ])∩V intersecting the top and bottom sides of the rectangle. We can order these components from left to right, say, and the leftmost component is called L. Only finitely many balls intersect [0, N] × [0, 3N] a.s. and hence the boundary ∂L of L has only finitely many components a.s. Hence, for n large enough, the event En := {L exists and all components of ∂L ∩ int([0, N] × [0, 3N]) have distance at least n−1 from each other} has probability at least 1 – κ. We fix no such that

$$P _ { ( \lambda _ { 2 } , r _ { 2 } ) } ( E _ { n _ { 0 } } ) > 1 - \frac { 1 } { 2 } \kappa .$$

Next we turn again to (X, r1, λ1). Since λ1 &lt; λc(r1), it follows from Lemma 3.3 a   - =    (  -   dd  .

$$P _ { ( \lambda _ { 1 } , r _ { 1 } ) } ( d ( W ( B _ { 1 } ) ) ) \geq b ) \leq C _ { 3 } e ^ { - C _ { 4 } b } ,$$

for all b &gt; 0, where C3 and C4 are again positive constants independent of b. Scaling down by a factor α &lt; 1 yields

$$P _ { ( \alpha ^ { - 2 } \lambda _ { 1 } , \alpha r _ { 1 } ) } ( d ( W ( B _ { \alpha } ) ) \geq \alpha b ) \leq C _ { 3 } e ^ { - C _ { 4 } b } ,$$

where Bα = [−α, α]2. Taking α = m−1 for some large integer m, and b = (2αno)−1 (with no as in (5.4)), we obtain

$$P _ { ( m ^ { 2 } \lambda _ { 1 } , m ^ { - 1 } r _ { 1 } ) } ( d ( W ( B _ { m ^ { - 1 } } ) ) \geq ( 2 n _ { 0 } ) ^ { - 1 } ) \leq C _ { 3 } e ^ { - C _ { 4 } m / 2 n _ { 0 } } .$$

Now we combine the conclusions obtained in (5.4) and (5.5). Divide [0, N] × [0, 3N] into 3N2m2 boxes with side length m−1, and denote these boxes by B1, B2, . . , B3N2m2. Then, from (5.5), the probability that in the model (X, m−1r1, m2λ1) the event

$$= \bigcup _ { i = 1 } ^ { 3 N ^ { 2 } m ^ { 2 } } \{ a \}$$


<!-- p:133 -->


Figure 5.1. The superposition of the two processes. The small balls do not cross the gap left by the big balís. Hence no L-R crossing of the rectangle exists.

occurs has probability at most 3N2m2C3e−C4m/2no, which tends to zero for m → ∞. We now fix an m0 such that this probability is at most κ. If En0 occurs in (X, r2, λ2) and F m0 Our does not occur in (X, m−1 r1, mλ1), then it follows that there is no occupied L-R crossing in [0, N] × [0, 3N] in the superposition of the two processes; see Figure 5.1. This superposition is in fact the model (X, ρ, λ2 + mλ1), where ρ is a random variable taking values r2 and m−1 r1 with probability λ2(m2λ1 + λ2)−1 and m2λ1(m2λ1 + λ2)−1, respectively. Hence, the probability of an occupied L-R crossing of [0, N] × [0, 3N] in (X, ρ, λ2 + m2λ1) is at most κ + κ &lt; κ. According to Lemma 3.3, this implies that this model is subcritical and this proves the theorem. 口

The following continuity result follows immediately from Definition 5.2 and Theorem 3.7. Together with Theorem 5.1 it also provides us with a class of radius distributions for which the strict inequality in (5.2) holds.

Theorem 5.2 Let ρk and ρ be random variables such that for some R &gt; 0 we have 0 ≤ ρ ≤ R and 0 ≤ ρk ≤ R a.s. for all k ≥ 1. If ρk ⇒ ρ then Ad(ρk) → Ad(ρ).

### 5.2 Compression

In this section we investigate the structure of bounded components in a highdensity Poisson Boolean model. Clearly, for any fixed k ≥ 0, Pλ {X(W) = k} is very small for large λ. Moreover, in the case when the balls are all of a fixed-size r, for the occurrence of the event {X(W) = k} the component obtained by the k balls constituting W should be surrounded by a fence of a vacant region. The only way this is possible is if the region formed by placing balls of radius 2r at each of these k points does not contain any point of the Poisson process other than these k. It is easy to observe that the volume of this region is less when the k points are close together than when the k points are quite separated from each other. Indeed the volume is minimized when all the k points are co-incident with each other. Thus one possible way the event {X(W) = k} can occur is when all the k points are clustered very close to each other and around these k points there is an 'annulus' of width approximately 2r where there is no Poisson point. In case the density of the Boolean model is large, then having k points very close to each other is quite feasible, although having the annulus free of Poi  o  or  ny n  s  snce of {X(W) = k} involves a larger volume left free of Poisson points and placing k points in a larger volume and this would have an even lower probability of occurrence than in the situation described previously. Thus in a high-density Boolean model {X(W) = k} is a rare event', and if it occurs then it is quite likely that it is due to the first scenario of k points being very close to each other and an annulus around these points of width 2r being free of Poisson points. In the rest of this section we make these heuristics rigorous.


<!-- p:134 -->


Here the Poisson process X we consider will be conditioned to have a point at the origin, i.e. 0 ∈ X, where 0 is the origin. Also, the radius of the balls comprising the Boolean model will be of a fixed radius r. Since X will always contain a point at the origin, instead of components of the origin W with k Poisson points, for ease of calculation, we shall subsequently consider components with k + 1 points.

Before we state and prove the main result, we introduce some notation. One possible situation whereby the first scenario described earlier could occur is to have k points besides the point at the origin in a ball of radius α and outside this ball is an annulus of width 2r where there are no Poisson points. The probability of this is clearly

$$\frac { ( \lambda \pi _ { d } \alpha ^ { d } ) ^ { k } } { k ! } & \exp ( - \lambda \pi _ { d } \alpha ^ { d } ) \exp ( - \lambda [ \pi _ { d } ( \alpha + 2 r ) ^ { d } - \pi _ { d } \alpha ^ { d } ] ) \\ & = \frac { ( \lambda \pi _ { d } \alpha ^ { d } ) ^ { k } } { k ! } \exp ( - \lambda \pi _ { d } ( \alpha + 2 r ) ^ { d } ) .$$

An easy calculation shows that as a function of α, the expression on the right side of the equality (5.6) is maximized at α = αk/λ where α denotes the positive solution of the equation

$$\alpha ( \alpha + 2 r ) ^ { d - 1 } = \frac { c } { \pi _ { d } } .$$

$$p ( \lambda , k ) = \sup _ { \alpha > 0 } \frac { ( \lambda \pi _ { d } \alpha ^ { d } ) ^ { k } } { k ! } \exp ( - \lambda \pi _ { d } ( \alpha + 2 r ) ^ { d } ) .$$

Let In case αk/λ is so small that the balls of radius r at the k Poisson points constitute a connected set, then clearly


<!-- p:135 -->


$$P _ { \lambda } \{ X ( W ) = k + 1 \} \geq p ( \lambda , k ) .$$

W  e  +  = (} l   e      .

In this connection a quantity to study is the relative density of the component W with respect to the ambient density λ of the underlying Poisson process. For any region C ⊆ IRd containing at least one Poisson point, let diam(C) denote the largest distance between any pair of Poisson points lying in C; i.e. diam(C) := sup{d(x, x') : x, x' Poisson points in C}. In case C contains only one Poisson point, diam(C) is taken to be 0. Thus, for a bounded component W, a ball centred at any Poisson point of W and of radius diam(W) contains all the Poisson points of the component W and it also contains the convex hull WH of the Poisson points of W. We define the density of the component W as X(W)/l(WH). Thus the ratio φ(λ) := X(W)/λl(WH) defines the relative density of the component W with respect to the ambient density λ. We observe that

$$\phi ( \lambda ) \geq \frac { X ( W ) } { \lambda \pi _ { d } ( d i a m ( W ) ) ^ { d } } .$$

Theorem 5.3 As λ → ∞, for a fixed k ≥ 1, we have

- (i) αk/λ → 0,
- Moreover, given any ∈ &gt; 0 and M &gt; 0, there exist 0 &lt; a &lt; b &lt; ∞ (depending only on ∈) and λ′ &lt; ∞ such that, for all λ ≥ λ′,
- ι  { +  = ()X|  (γ)φ} ()
- (iii) P {a &lt; diam(W) &lt;b|X(W)=k+1}≥1-∈, αk/λ

Statement (iv) says that typically a bounded component in a high-density Boolean model is formed by the Poisson points constituting the component being very close to each other. The density of the component is of a larger order than the ambient density of the process. This is known as the phenomenon of compression.

We note, from (5.7), αk/λ → 0 as λ → ∞ and this proves (i) of the theorem. Als      ← s t t    s    γ   nd

$$\frac { k } { \lambda \pi _ { d } ( \nu _ { \lambda } + 2 r ) ^ { d - 1 } } \leq \alpha _ { k / \lambda } \leq \frac { k } { \lambda \pi _ { d } ( 2 r ) ^ { d - 1 } } .$$


<!-- p:136 -->


This shows that for large λ, αk/λ is approximately k/λπd(2r)d-1. For the remainder of the proof we need to do much more work. Since we make extensive use of Stirling's formula, we state the version we use (see Feller 1978, pp. 52-54).

Stirling's formula Stiriing's formula

$$\lim _ { n \to \infty } \frac { n ! } { \sqrt { 2 \pi } n ^ { n + 1 / 2 } e ^ { - n } } = 1 ,$$

Moreover, for every n ≥ 1,

$$\sqrt { 2 \pi } n ^ { n + 1 / 2 } e ^ { - n } \exp ( 1 / ( 1 2 n + 1 ) ) & \leq n ! \\ & \leq \sqrt { 2 \pi } n ^ { n + 1 / 2 } e ^ { - n } \exp ( 1 / ( 1 2 n ) ) .$$

We begin with an easy lower bound for Pλ{X(W) = k + 1}.

Lemma 5.1 There exists λ0 &lt; ∞ such that, for λ ≥ λ0

$$P _ { \lambda } \{ X ( W ) & = k + 1 \} \\ & \geq \exp \left ( - \left \lceil \lambda \pi _ { d } ( 2 r ) ^ { d } + ( d - 1 ) k \log \frac { \lambda } { \tilde { k } } \right \rceil \\ & + ( d - 1 ) k \log ( e \pi _ { d } ( 2 r ) ^ { d } ) + C _ { 1 } \frac { k ^ { 2 } } { \lambda } + C _ { 2 } \log k \right ] \right ) , \\ \intertext { s u r s i t i v e c h o n t s } \left ( \begin{array} { c c } P _ { \lambda } \{ X ( W ) = k + 1 \} \\ & \end{array} \right ) ,$$

for positive constants C1 and C2 independent of λ.

Proof Let S denote the unit ball centred at the origin and, for α &gt; 0, αS denote the ball of radius α centred at the origin. If λ is so large that k/λπa(2d)d–1 &lt; 2r, then all the Poisson points in the ball (k/λπd(2d)d-1)S are in the same component and thus we have

$$2 , \text { then all the Poisson points in the ban } ( k / \pi _ { d } ( 2 d ) ^ { - 3 } ) \text { are in the same } \\ \text { component and thus we have } \\ P _ { \lambda } \{ X ( W ) = k + 1 \} \\ \geq P _ { \lambda } \left \{ X \left ( \frac { k } { \lambda \pi _ { d } ( 2 r ) ^ { d - 1 } } S \right ) = k \text { and } \\ X \left ( \left ( \frac { k } { \lambda \pi _ { d } ( 2 r ) ^ { d - 1 } } + 2 r \right ) S \right \} \frac { k } { \lambda \pi _ { d } ( 2 r ) ^ { d - 1 } } S \right ) = 0 \right \} \\ = \frac { 1 } { k ! } \exp \left ( - \lambda \pi _ { d } \left ( \frac { k } { \lambda \pi _ { d } ( 2 r ) ^ { d - 1 } } \right ) ^ { d } \right ) \left [ \lambda \pi _ { d } \left ( \frac { k } { \lambda \pi _ { d } ( 2 r ) ^ { d - 1 } } \right ) ^ { d } \right ] ^ { k } \\ \times \exp \left ( - \lambda \pi _ { d } \left [ \left ( \frac { k } { \lambda \pi _ { d } ( 2 r ) ^ { d - 1 } } + 2 r \right ) ^ { d } - \left ( \frac { k } { \lambda \pi _ { d } ( 2 r ) ^ { d - 1 } } \right ) ^ { d } \right ] \right ) .$$


<!-- p:137 -->


Now using Stirling's formula in this expression, we have for positive constants C1 and C2 independent of k or λ,

Noe n  l t la l e  l l lt l l n Lemma 5.1 contribute exp(−[(d − 1)k log(eπd(2r)d) + C1(k2 /λ) + C2 log k]) which, for fixed k ≥ 1 and as λ → ∞, is of the order of exp(−O(1)). In other words, the bound obtained in (5.10) is the expression we required in (ii) of the theorem. Thus to complete the proof of the theorem we need to show that the k + 1 Poisson points forming the component W cannot be separated any more than required to compute (5.10). We prove this in a sequence of lemmas. The first lemma considers the case when the component W is bounded and has a large diameter.

Lemma 5.2 For every β &lt; ∞, there exist l &lt; ∞ and λ1 &lt; ∞ such that for λ &gt; λ1 we have

$$P _ { \lambda } \{ l \leq d ( W ) < \infty \} \leq \exp ( - \lambda \beta ) .$$

Proof The proof proceeds by a lattice approximation. Suppose l ≤ d(W) &lt; ∞. Consider a lattice I of width a with 0 &lt; a &lt; r/4. Since d(W) ≥ l, there must exist a connected component δ0(W) (say) of the boundary δ(W) such that δ0(W) encloses the origin and its diameter d(δ0(W)) is at least l. Let δ(W) be the collection of cells of the lattice I which intersects δ0(W). Since d(δ0(W)) ≥ l, the number of cells in δc(W) is at least l/a and also ∪C∈δc(W) C is a connected set. Moreover, by our choice of the lattice width a, no Poisson point can lie on any cell in δc(W).

Now for every n≥ 1 consider the set K of all collections C of cells of the lattice IL such that (i) the number of cells in C is n, (ii) ∪cecC is a connected set, and (iii) UC∈cC contains a (d – 1)-dimensional surface which encloses the origin. (In other words, the set K contains all collections C of cells which have cardinality n and which arise as a collection δc(W) of a bounded component W.) A counting argument as in Theorem 1.1 yields that the cardinality κn of K is at most c" for some constant c &gt; 1 which depends on the dimension d. Thus,


<!-- p:138 -->


$$P _ { \lambda } \{ l \leq d ( W ) < \infty \} & \leq \sum _ { n \geq l / a } \sum _ { C \in \mathcal { C } _ { n } } P _ { \lambda } ( X ( \cup _ { C \in C } C ) = 0 ) \\ & \leq \sum _ { n \geq l / a } c ^ { n } \exp ( - \lambda n a ^ { d } ) .$$

Now given β &lt; ∞ choose l such that β = lad-1 log(2bl/a); then, for λ such that 1 − c exp(−λad) &gt; 1/2, we have ∑n≥1/a cn exp(−λnad) &lt; exp(−λβ). This along with (5.11) proves the lemma. □

REMARK: Under the conditions of Lemma 5.2 we also obtain

$$P _ { \lambda } \{ l \leq \dim ( W ) < \infty \} \leq \exp ( - \lambda \beta ) .$$

Now we turn our attention to components of smaller diameter. The next lemma will be repeatedly applied in the subsequent lemmas.

Lemma 5.3 Let μ &gt; 1 and define, for y &gt; 0,

$$\psi _ { \mu } ( y ) = \frac { \pi _ { d - 1 } ( 2 r ) ^ { d - 1 } y } { 4 } - \log ( e \pi _ { d } \mu ^ { d } y ^ { d } ) .$$

There exists a constant C3 = C3(μ, r) such that for y(k/λ) &lt; C3, we have

$$P _ { \lambda } & \left \{ X ( W ) = k + 1 , \ y _ { \overline { \lambda } } ^ { k } < \dim ( W ) \leq \mu y _ { \overline { \lambda } } ^ { k } \right \} \\ & \leq \exp \left ( - \left [ \lambda \pi _ { d } ( 2 r ) ^ { d } + ( d - 1 ) k \log \frac { \lambda } { k } + k \psi _ { \mu } ( y ) \right ] \right ) .$$

Proof Let Wp denote the set of all Poisson points of X (including the origin) in the ball μy(k/λ)S. Define

$$y ( k / \lambda ) S . \, \text {Define} \\ A & \colon = \left \{ X \left ( \mu y _ { \lambda } ^ { k } S \right ) = k \right \} \\ B & \colon = \left \{ y _ { \overline { \lambda } } ^ { k } < \text {diam} ( W _ { p } ) \leq \mu y _ { \overline { \lambda } } ^ { k } \right \} .$$


<!-- p:139 -->


If μy(k/λ) &lt; 2r, we have

$$\leq \mu y \frac { k } { \lambda } \Big \} \\ \text {diag} ( W ) \leq \mu y \frac { k } { \lambda } | W _ { p } \Big \} \Big ) \\ \mu y \frac { k } { \lambda } S \Big ) = 0 | W _ { p } \Big \} \left \{ 1 _ { A } 1 _ { B } \right ) , \quad ( 5 . 1 4 )$$

where as usual S(w, 2r) denotes the ball of radius 2r centred at w.

To estimate the last term in (5.14), we need to estimate the Lebesgue measure of ∪w∈wp S(w, 2r). Let w1 and w2 be two points of Wp such that w1 and w2 are farthest apart among all pairs of points of Wp; i.e., d(w1, w2) = diam(Wp). Let H1 and H2 be hyperplanes through w1 and w2 respectively, both of which are perpendicular to the line L passing through w1 and w2. Clearly all points of Wp lie in the slab T between the two hyperplanes H1 and H2. Let wo be the point of Wp which lies farthest (in terms of the perpendicular distance) from the line L, and let Ho be the hyperplane passing through wo and which is perpendicular to the shortest line joining wo to L. Clearly each of the hyperplanes H1, H2 and Ho divides the space IRa into a pair of distinct half-spaces such that one of each pair H+, H2+ and H+ (say) contains no point of Wp. The Lebesgue measure of ∪w∈w S(w, 2r) is clearly larger than the sum of the Lebesgue measures of

- s    r se   t  ees t (region I in Figure 5.2)
- (ii) a semisphere centred at w2 of radius 2r and lying completely in H2+ (region II in Figure 5.2) and
- (iii) the region in the slab T enclosed by the semisphere centred at wo of radius 2r and lying completely in H+ (region II in Figure 5.2).

Thus,

$$\ell ( \cup _ { w \in W _ { p } } S ( w , 2 r ) ) \\ \geq \ell ( H _ { 1 } ^ { + } \cap S ( w _ { 1 } , 2 r ) ) + \ell ( H _ { 2 } ^ { + } \cap S ( w _ { 2 } , 2 r ) ) + \ell ( T \cap H _ { 0 } ^ { + } \cap S ( w _ { 0 } , 2 r ) ) \\ = \pi _ { d } ( 2 r ) ^ { d } + \ell ( T \cap H _ { 0 } ^ { + } \cap S ( w _ { 0 } , 2 r ) ) .$$

To estimate l(T ∩ H+ ∩ S(wo, 2r)), we first give an argument in two dimensions. A Pythagorean calculation gives that in two dimensions, the disc S(wo, 2r) centred at wo makes an intercept of length at least √(2r)2 – (y)2


<!-- p:140 -->


Figure 5.2. Regions I, II and III.

with each of the two lines H1 and H2. Thus, if diam(Wp) ≥ yx, then T ∩ H+ ∩ S(wo, 2r) contains a rectangle of dimension √(2r)2 – (y)2 × y(k/λ). Hence, for λ large enough l(T ∩ H+ ∩ S(wo, 2r)) ≥ 2ry(k/4λ).

In general, for higher dimensions, the intercepts on each of the hyperplanes H1 and H2 will be (d — 1)-dimensional semispheres of (d — 1)-dimensional Lebesgue measure at least πd(√(2r)2 − (yk)2)d-1. Thus, if diam(Wp) ≥ Vy-s   snn     (der whose base is a (d - 1)-dimensional semisphere and whose height is y. Thus, we have, for large λ,

$$\ell ( T \cap H _ { 0 } ^ { + } \cap S ( w _ { 0 } , 2 r ) ) \geq \pi _ { d - 1 } ( 2 r ) ^ { d - 1 } y \frac { k } { 4 \lambda } .$$

We now use independence obtained from the fact that the event A depends only on the configuration inside the ball μyS, whereas the event {X(∪w∈wS(w, 2r)\μy(k/λ)S) = 0} depends only on the configuration outside the ball μyk/λS, to have from (5.15) and (5.16),

$$E _ { \lambda } \left ( P _ { \lambda } \left \{ X \left ( \cup _ { w \in W _ { p } } S ( w , 2 r ) \ \langle \mu y \frac { d } { \lambda } \right ) = 0 | W _ { p } \right \} ^ { 1 _ { A } 1 _ { B } } \right ) \\ \leq E _ { \lambda } \left ( P _ { \lambda } \left \{ X \left ( \cup _ { w \in W _ { p } } S ( w , 2 r ) \ \langle \mu y \frac { k } { \lambda } S \right ) = 0 | W _ { p } \right \} ^ { 1 _ { A } } \right ) \\ \leq \exp \left ( - \lambda \left [ \pi _ { d } ( 2 r ) ^ { d } + \pi _ { d - 1 } ( 2 r ) ^ { d - 1 } y \frac { k } { 4 \lambda } - \ell \left ( \mu y \frac { k } { \lambda } S \right ) \right ] \right ) P _ { \lambda } ( 4 ) \\ = \exp \left ( - \lambda \left [ \pi _ { d } ( 2 r ) ^ { d } + \pi _ { d - 1 } ( 2 r ) ^ { d - 1 } y \frac { k } { 4 \lambda } - \pi _ { d } \left ( \mu y \frac { k } { \lambda } \right ) ^ { d } \right ] \right )$$


<!-- p:141 -->


$$5 . 2 \, \ C o m p r e s s i o n \\ \times \xrightarrow { [ \lambda \pi _ { d } ( \mu y _ { \lambda } ^ { k } ) ^ { d } ] ^ { k } } \exp \left ( - \lambda \pi _ { d } \left ( \mu y _ { \overline { \lambda } } ^ { k } \right ) ^ { d } \right ) \\ \\ \leq \exp \left ( - \left [ \lambda \pi _ { d } ( 2 r ) ^ { d } + ( d - 1 ) \log \frac { \lambda } { k } + k \psi _ { \mu } ( y ) \right ] \right ) ,$$

where we have used Stirling's formula in the last inequality. From (5.14) and (5.17), we see that the lemma holds for any C3 with μC3 &lt; 2r. 口

We now use the counting method of Lemma 5.2 and the geometric argument of Lemma 5.3 to study the case when the component is of 'medium' size.

Lemma 5.4 For every 0 &lt; δ and l &lt; ∞, there exist constants C4 &gt; 0 and λ2 &lt; ∞ such that for λ ≥ λ2

$$P _ { \lambda } \{ \delta \leq d i a m ( W ) \leq l \} \leq \exp ( - \lambda [ \pi _ { d } ( 2 r ) ^ { d } + C _ { 4 } ] ) .$$

Proof As in the geometric argument given in Lemma 5.3, here, if diam(W) ≥ δ, then we require that two semispheres of radius 2r each separated by a distance of at least δ and a region formed by the intersection of a semisphere and a slab of thickness at least δ have to be free of Poisson points. Let this region be denoted by A. Clearly A ⊆ [−1 – 2r, l + 2r]d. The argument given to justify (5.16) yields in this case that the Lebesgue measure of the region A satisfies l(A) ≥ πd(2r)d + c1πd−1(2r)d−18, for some constant 0 &lt; c1 &lt; 1. (Note that here δ plays the role of y(k/λ) of the previous lemma.) Introducing a lattice approximation as in Lemma 5.2 with a lattice L of width a &gt; 0, we have the inner lattice approximation Aa of A given by Aa := U{C : C a cell of the lattice L and C ⊆ A}. For a &lt; c2 where c2 &gt; 0 is a sufficiently small constant, we obtain a constant c3 &gt; 0 depending on c1 and c2 such that l(Aa) ≥ πd(2r)d + c3δ. Now Aa ⊆ [−l − 2r, l + 2r]d; thus for a fixed a, there are only finitely many possible choices of Aa. Hence a summation over all possible Aa's yields

$$P _ { \lambda } \{ \delta \leq \dim ( W ) \leq l \} \leq \sum _ { \Lambda _ { a } } P _ { \lambda } \{ A _ { a } \text { contains no Poisson point} \} , \quad ( 5 . 1 8 )$$

where the summation is over all Aa's such that Aa's are unions of cells of the lattice IL and l(Aa) ≥ πd(2r)d + c3δ. Let Na(= Na (l, δ, r)) be the total number of such choices of Aa possible. From (5.18) we have


<!-- p:142 -->


$$P _ { \lambda } \{ \delta \leq \dim ( W ) \leq l \} & \leq \sum _ { \Lambda _ { a } } \exp ( - \lambda [ \pi _ { d } ( 2 r ) ^ { d } + c _ { 3 } \delta ] ) \\ & \leq N _ { a } \exp ( - \lambda [ \pi _ { d } ( 2 r ) ^ { d } + c _ { 3 } \delta ] ) .$$

Taking C4 = c3δ/2, we obtain λ2 &lt; ∞ such that for λ ≥ λ2,

$$\exp ( - \lambda c _ { 3 } \delta + \log N _ { a } ( l , \delta , r ) ) \leq \exp ( - \lambda C _ { 4 } ) .$$

Combining (5.19) and (5.20) yields the lemma. 口

In the next lemma we apply Lemma 5.3 to take care of small components.

Lemma 5.5 Given β &lt; ∞, there exist C5 &gt; 0, δ &gt; 0 (depending only on β) and λ3 such that, for λ ≥ λ3, we have

$$d \lambda _ { 3 } \ s u c h t a t , & \text {for} \, \lambda \geq \lambda _ { 3 } , \, w e h a v e \\ P _ { \lambda } & \left \{ X ( W ) = k + 1 , C _ { 5 } \frac { k } { \lambda } \leq \text {diam} ( W ) \leq \delta \right \} \\ & \leq \exp \left ( - \left [ \lambda \pi _ { d } ( 2 r ) ^ { d } + ( d - 1 ) k \log \frac { \lambda } { k } + \beta k \right ] \right ) .$$

Proof First we fix μ &gt; 1 and obtain the constant C3 as in Lemma 5.3. Now we fix δ &lt; C3. Observe that the function ψμ of Lemma 5.3 satisfies ψμ(y) → ∞ as y → ∞, so that we may choose a constant C5 such that the following two conditions hold:

$$\psi _ { \mu } ( C _ { 5 } ) > \beta + \log 2 ,$$

$$\sum _ { i \mp 1 } ^ { \infty } \exp ( - k [ \psi _ { \mu } ( C _ { 5 } \mu ^ { j } ) - \psi _ { \mu } ( C _ { 5 } ) ] ) \leq 1 .$$

Let λ3 &lt; ∞ be such that C5(k/λ) &lt; δ and for some j ≥ 1, δ &lt; C5μ(k/λ) &lt; C3 whenever λ ≥ λ3. We now partition the interval [Cs(k/λ), 8] by intervals of the type [C5μ(k/λ), C5μj+1(k/λ)], j = 0, 1, .. .. Let N be the smallest integer such that [C5(k/λ), 8] ⊆ Uj=0[C5μj(k/λ), C5μj+1 (k/λ)]. Since C5μ (k/λ) → ∞ as j → ∞ for fixed λ, we have that N is finite. Now observe that

$$\text {that} \\ P _ { \lambda } \left \{ X ( W ) = k + 1 , \ C _ { \lambda } \frac { k } { \lambda } \leq \text {diam} ( W ) \leq \delta \right \} \\ \leq \sum _ { J = 0 } ^ { N } P _ { \lambda } \left \{ X ( W ) = k + 1 , \ C _ { \S \mu ^ { J } } \frac { k } { \lambda } \leq \text {diam} ( W ) \leq C _ { \S \mu ^ { J } } + 1 \ \frac { k } { \lambda } \right \} .$$


<!-- p:143 -->


Applying Lemma 5.3 to each of the terms inside the summation of (5.23) we have, for λ ≥ λ3,

$$Applying Lemma 5.3 to each of the terms inside the summation of ( 5 . 2 3 ) we
have, for \lambda \geq \lambda _ { 3 } , \\ P _ { \lambda } \left \{ X ( W ) = k + 1 , \, C _ { \lambda } \leq \text {dice} ( W ) \leq \delta \right \} \\ \leq \sum _ { j = 0 } ^ { N } \exp \left ( - \left \lceil \lambda _ { d } ( 2 r ) ^ { d } + ( d - 1 ) k \log \frac { \lambda } { k } + k \psi _ { \mu } ( C _ { 5 } \mu ^ { j } ) \right \rceil \right ) \\ \leq \exp \left ( - \left [ \lambda _ { d } ( 2 r ) ^ { d } + ( d - 1 ) k \log \frac { \lambda } { k } + k \psi _ { \mu } ( C _ { 5 } ) \right ] \right ) \\ + \sum _ { j = 1 } ^ { N } \exp \left ( - \left [ \lambda _ { d } ( 2 r ) ^ { d } + ( d - 1 ) k \log \frac { \lambda } { k } + k \psi _ { \mu } ( C _ { 5 } \mu ^ { j } ) \right ] \right ) \\ \leq 2 \exp \left ( - \left [ \lambda _ { d } ( 2 r ) ^ { d } + ( d - 1 ) k \log \frac { \lambda } { k } + k \psi _ { \mu } ( C _ { 5 } ) \right ] \right ) \\ \leq \exp \left ( - \left [ \lambda _ { d } ( 2 r ) ^ { d } + ( d - 1 ) k \log \frac { \lambda } { k } + \beta k \right ] \right ) , \\ \text {where the last two inequalities follow from (5.22) and (5.21). This completes} \\ \text {the proof of the lemma.}$$

where the last two inequalities follow from (5.22) and (5.21). This completes the proof of the lemma. □

In the last four lemmas, we have covered the case when diam (W) ≥ C5(k/λ). The next lemma considers the case when the component is very small.

Lemma 5.6 Given any β &lt; ∞, there exist C6 &gt; 0 and λ4 &lt; ∞ such that, for λ ≥ λ4, we have C6(k/λ) &lt; δ and

$$\lambda \geq \lambda _ { 4 } , \, \text {we have} \, C _ { 6 } ( k / \lambda ) & < b \, \text {lambda} \\ P _ { \lambda } \left \{ X ( W ) = k + 1 , \, \text {dim} ( W ) \leq C _ { 6 } \frac { k } { \lambda } \right \} \\ & \leq \exp \left ( - \left [ \lambda \pi _ { d } ( 2 r ) ^ { d } + ( d - 1 ) k \log \frac { \lambda } { k } + \beta k \right ] \right ) .$$

Proof The proof of this lemma is similar to that of the previous lemma and as such we just sketch the proof. Here we observe that ψμ(y) → ∞ as y → 0. Thus we have to choose C6 &lt; C5 sufficiently small such that

$$\psi _ { \mu } ( C _ { 6 } ) > \beta + \log 2 ,$$

$$\sum _ { j = 1 } ^ { \infty } \exp ( - k [ \psi _ { \mu } ( C _ { 6 } \mu ^ { - j } ) - \psi _ { \mu } ( C _ { 6 } ) ] ) \leq 1 ,$$


<!-- p:144 -->


where μ &gt; 1 is a previously fixed quantity. Also, we may choose λ4 large ue  t   t         (u t a ply Lemma 5.3. Covering the interval (0, C6(k/λ)] by intervals of the type [C6μ−(j+1)(k/λ), C6μ−j(k/λ)], j = 0, 1,..., we obtain an inequality as in (5.23)

$$M \left ( 5 . 2 3 \right ) \\ P _ { \lambda } \left \{ X ( W ) = k + 1 , \, \text { diam} ( W ) \leq C _ { \lambda } \frac { k } { } \right \} \\ \leq \sum _ { j = 0 } ^ { \infty } P _ { \lambda } \left \{ X ( W ) = k + 1 , \, C _ { 6 } \mu ^ { - \left ( J + 1 \right ) } \frac { k } { \lambda } \leq \text { diam} ( W ) \leq C _ { \S } \mu ^ { - j } \frac { k } { \lambda } \right \} . \\ A \, \text { calculation similar to } ( 5 . 2 4 ) \, \text { using } ( 5 . 2 6 ) \, \text { and } ( 5 . 2 5 ) \, \text { completes the proof of }$$

A calculation similar to (5.24) using (5.26) and (5.25) completes the proof of the lemma. □

Proof of Theorem 5.3 First observe that taking μo = C5/C6, where C5 and C6 are as in Lemmas 5.5 and 5.6, we have μo &gt; 1. Also, from Lemma 5.3, for λ5 large enough such that C5(k/λ) &lt; C3(μo, r) for all λ ≥ λ5, we have

$$x _ { 5 } \, \text {large enough such that } C _ { 5 } ( x / \lambda ) & < C _ { 3 } ( \lambda / 6 ) \, \Gamma \text { for all } x \geq x _ { 3 } , \, \text {we have} \\ P _ { \lambda } & \left \{ X ( W ) = k + 1 , \, C _ { 6 } \frac { k } { \lambda } \leq \text {diam} ( W ) \leq C _ { 5 } \frac { k } { \lambda } \right \} \\ & \leq \exp \left ( - \left [ \lambda \pi _ { d } ( 2 r ) ^ { d } + ( d - 1 ) k \log \frac { \lambda } { k } + k \psi _ { \mu _ { 0 } } ( C _ { 6 } ) \right ] \right ) .$$

Now let us collect all our observations. Fix β such that

$$\beta > \pi _ { d } ( 2 r ) ^ { d } \quad \text {and} \quad 1 + \exp ( - \beta k ) \leq \exp \left ( \frac { \beta k } { 6 } \right )$$

(the need for this choice will be apparent later), and accordingly obtain 0 &lt; I(= 1(β)) as in Lemma 5.2, 0 &lt; δ(= δ(β)) and C5(= C5(β)) &lt; ∞ as in Lemma 5.5 and 0 &lt; C6(= C6(β)) &lt; C5 as in Lemma 5.6. For X(W) = k + 1, we see that, if λ ≥ max{λ1, λ2, λ3, λ4, λs},

- (i) (5.12) accounts for the case when diam(W) ≥ l for some l,
- (ii) Lemma 5.4 accounts for the case when δ ≤ diam(W) ≤ l,
- (iii) Lemma 5.5 accounts for the case when C5(k/λ) ≤ diam(W) ≤ δ,
- (iv) Lemma 5.6 accounts for the case when diam(W) ≤ C6(k/λ),
- (v) (5.27) accounts for the case when C6(k/λ) ≤ diam(W) ≤ C5(k/λ).

Thus we have accounted for the entire possible range of diam(W). Moreover, the upper bound on the probability obtained in each of these cases is at most exp(−[λπd(2r)d + (d − 1)k log(λ/k) + O(1)]). Thus, we have obtained

$$P _ { \lambda } \{ X ( W ) = k + 1 \} \leq \exp \left ( - \left [ \lambda \pi _ { d } ( 2 r ) ^ { d } + ( d - 1 ) k \log \frac { \lambda } { k } + O ( 1 ) \right ] \right )$$


<!-- p:145 -->


as λ → ∞. This along with the lower bound obtained in Lemma 5.1 proves (ii) of the theorem.

The choice of β comes in to prove (iii). From Lemma 5.2, Lemma 5.4 and Lemma 5.5, for all sufficiently large λ,

$$P _ { \lambda } \left \{ X ( W ) = k + 1 , \, \text {di} ( W ) \geq C _ { \overline { \lambda } } \right \} \\ \leq \exp \left ( - \left [ \lambda \pi _ { d } ( 2 r ) ^ { d } + ( d - 1 ) k \log \frac { \lambda } { k } + \frac { \beta k } { 2 } \right ] \right ) \\$$

and from Lemma 5.6

$$\text {and from Lemma 5.6} \\ P _ { \lambda } \left \{ X ( W ) = k + 1 , \text { diam} ( W ) \leq C _ { \lambda } \frac { k } { } \right \} \\ \leq \exp \left ( - \left [ \lambda \pi _ { d } ( 2 r ) ^ { d } + ( d - 1 ) k \log \frac { \lambda } { k } + \beta k \right ] \right ) . \\ \text {Combining the lower bound obtained in} \, I \, \text {emma 5.1 with} \, ( 5 . 2 9 ) \, \text {and} \, ( 5 . 3 0 ) \, \text {and}$$

Combining the lower bound obtained in Lemma 5.1 with (5.29) and (5.30), and using the second part of (5.28) in the choice of β, we obtain for all sufficiently large λ

$$\text {using the second part of (5.28) in the choice of $\beta$, we obtain for all sufficiently
large $\lambda$} \\ \frac { P _ { \lambda } \{ X ( W ) = k + 1 , \, \text {diam} ( W ) \leq C _ { 6 } ( k / \lambda ) \, or \, \text {diam} ( W ) \geq C _ { 5 } ( k / \lambda ) \} } { P _ { \lambda } \{ X ( W ) = k + 1 \} } \\ \leq \exp \left ( - \left [ \lambda \pi _ { d } ( 2 r ) ^ { d } + ( d - 1 ) k \log \frac { \lambda } { k } + \frac { \beta k } { 3 } \right ] \right ) \\ \times \exp \left ( \left [ \lambda \pi _ { d } ( 2 r ) ^ { d } + ( d - 1 ) k \log \frac { \lambda } { k } \right ] \right ) \\ + ( d - 1 ) k \log ( e \pi _ { d } ( 2 r ) ^ { d } ) + C _ { 1 } \frac { k ^ { 2 } } { \lambda } + C _ { 2 } \log k \right ] \right ) \\ \leq \exp \left ( - \left [ \frac { \beta k } { 3 } - ( d - 1 ) k \log ( e \pi _ { d } ( 2 r ) ^ { d } ) \right ] \right ) \\ + C _ { 1 } \frac { k ^ { 2 } } { \lambda } + C _ { 2 } \log k \right ] \right ) . \\ \text {Given $\epsilon > 0$, we choose $\beta$ such that $(5.28)$ is satisfied and} \\ \exp \left ( \int \beta k ^ { 2 } \left ( d - 1 \right ) k \log ( e \pi _ { d } ( 2 r ) ^ { d } ) + C _ { 1 } ^ { k ^ { 2 } } + C _ { 2 } \log k \right ) \right ) < ( 5 . 3 )$$

Given € &gt; 0, we choose β such that (5.28) is satisfied and

$$\exp \left ( - \left [ \frac { \beta k } { 3 } - ( d - 1 ) k \log ( e \pi _ { d } ( 2 r ) ^ { d } ) + C _ { 1 } \frac { k ^ { 2 } } { \lambda } + C _ { 2 } \log k \right ] \right ) \leq \epsilon \quad ( 5 . 3 2 )$$

for all λ sufficiently large. Without loss of generality suppose that this λ is so large that k/(2λπd(2r)d−1) ≤ k/(λπd(νλ + 2r)d−1), where νλ is as in (5.9). Now choose

$$a = C _ { 6 } \pi _ { d } ( 2 r ) ^ { d - 1 } \quad \text {and} \quad b = 2 C _ { 5 } \pi _ { d } ( 2 r ) ^ { d - 1 } ,$$


<!-- p:146 -->


according to this choice of β. Forβ satisfying (5.28) and (5.32) and a and b as in (5.33), from (5.30) we have

$$P _ { \lambda } \left \{ a < \frac { \text {diam} ( W ) } { \alpha _ { k / \lambda } } < b | X ( W ) = k + 1 \right \} \geq 1 - \epsilon ,$$

and this proves (iii).

To show the compression phenomenon we first observe that (5.9) and (iii) yield that, for all sufficiently large λ, with Pλ probability at least 1 — ∈ we have

$$\frac { k } { \lambda \pi _ { d } \ d i a m ( W ) ^ { d } } \geq \frac { k } { b \lambda \pi _ { d } \left ( \frac { k } { \lambda \pi _ { d } ( 2 r ) ^ { d - 1 } } \right ) ^ { d } } .$$

Given € &gt; 0 and M &gt; 0, we may choose λ so large that the term on the right side of the above expression is larger than M and this, along with (5.8), proves (iv) of the theorem.

### 5.3 Rarefaction

In the previous section the compression phenomenon was obtained by considering balls of a fixed radius r. A natural question is what happens when we have varying radius, and in this section we investigate this.

We shall assume throughout this section that the radius random variable ρ is non-degenerate and takes exactly two different values; i.e. for 0 &lt; r &lt; R &lt; ∞, we have

$$P ( \rho = R ) = 1 - P ( \rho = r ) = p ,$$

for some 0 &lt; p &lt; 1. Throughout this section, big balls will always refer to balls of radius R and small balls will always refer to balls of radius r.

Before we present the formal details, we give some intuitive ideas about the structure of a bounded component in the Boolean model (X, ρ, λ) when the density λ is very large and ρ satisfies (5.34). The Boolean model (X, ρ, λ) is assumed to include a Poisson point at the origin.

In case the Poisson point at the origin accommodates a big ball and the component W consists of k big balls (besides the ball centred at the origin) and I small balls, then a possible structure of the component W is that the centres of the k big balls and the big ball at the origin are all clustered near the origin, while the small balls are distributed 'uniformly'in the region formed by the big balls such that none of the small balls protrude outside the region formed by the big balls. In this case an annulus of width 2r around the region formed by the big balls has to be devoid of Poisson points which are centres of small balls, and an annulus of width 2R around the region formed by the big balls has to be devoid of Poisson points which are centres of big balls. A little thought shows that it is this structure which would minimize the volume of the annular region which needs to be free of Poisson points.


<!-- p:147 -->


In the argument above, we assumed that the origin is the centre of a big ball. However, if the origin is the centre of a small ball and component W contains exactly k big balls and l small balls (besides the ball centred at the origin), then, provided k ≥ 1, the structure of the component W will not be vastly different from that described in the previous paragraph. Indeed what could happen is that the centres of the big balls are all clustered together (which need not be around the origin) and the l + 1 small balls (including the small ball at the origin) are uniformly distributed in the region formed by the big balls such that none of the small balls protrude outside this region. Thus the difference between the structure of the cluster obtained in this case and that obtained in the previous paragraph involves just a change in the position of the origin.

In case the component W consists of k + 1 big balls and there is no small ball centred in W, then as in the previous section, we will have a compression phenomenon with all the Poisson points (besides the origin) compressed in a small region around the origin. A similar phenomenon will be observed when the component W consists of l + 1 small balls and no big ball is centred in W.

Returning to the situation when the component W contains both big and small balls and a big ball is centred at the origin, we see that the l small balls are distributed in the region formed by the k + 1 big balls. This region formed by the k + 1 big balls contains a spherical region inside it of Lebesgue measure at least πa Rd. The centres of the small balls may be placed anywhere inside this region at a distance at least r from the boundary of the region to guarantee that the small balls do not protrude out of this region. This means that the small balls may be centred in a region whose Lebesgue measure is at least πa(R — r)d. Thus looking at the whole picture we see that the k + l + 1 Poisson points forming the component W are distributed in a region of Lebesgue measure at least πd(R — r)d with k + 1 of these points compressed together while the remaining l are distributed uniformly in this region. This would yield a rarefaction phenomenon as λ → ∞, because a region of Lebesgue measure at least πd(R − r)d should typically accommodate λπd(R − r)d Poisson points.

In this section we will state and prove the result only for the case when the origin is the centre of a big ball and there is at least one small ball present in the component W. The case when the component contains at least one big ball and the origin is the centre of a small ball should follow after tedious technical details from the previous case and it involves conditioning on the position of a hig ball. We shall omit this case. The details of the case when the component W consists only of big balls or only of small balls are similar to those described in the previous section and as such we omit this case too.


<!-- p:148 -->


Before we introduce the relevant notation, it may be observed that the intuitive degenerate ρ which has support in [r, R] for some 0 &lt; r &lt; R &lt; ∞. We do not

reasoning given above needs the existence of at least two different sized balls. hnd e an-d n e  n ss d  sos variable ρ. However, the technical details of the result extend only to nonventure to prove the result for ρ other than that satisfying (5.34).

Let (Y, R, λp) be a Poisson Boolean model conditioned to have a point at the origin and (Z, r, λ(1 – p)) be another Poisson Boolean model, where r, R and p are as in (5.34) and (Y, R, λp) and (Z, r, λ(1 − p)) are independent processes. The superposition of these two Boolean models is a Boolean model which is equivalent in law to a Poisson Boolean model of density λ and radius random variable ρ conditioned to have a point at the origin with a ball of radius R. Throughout this section 0, y1, y2, ... represent points of the point process Y and z1 , z2, . . . represent points of the point process Z. Let Wy and Wz denote the occupied components of the origin in (Y, R, λp) and (Z, r, λ(1 − p)), respectively, and let W denote the occupied component of the origin in the superposition of these models. Clearly WWy U Wz.

For l ≥ 1, k ≥ 0, let

{#W = (k, l)} := {the origin is the centre of a big ball and W contains exactly k + 1 points of Y and l points of Z}.

As a measure of the size, for any set S containing the origin, let

$$\ r a d ( S ) & = \sup \{ d ( 0 , x ) \colon x \text { is a point of } Y * Z \text { in } S \} , \\ \ r a d _ { Y } ( S ) & = \sup \{ d ( 0 , y ) \colon y \text { is a point of } Y \text { in } S \} ,$$

$$\ r a d _ { Z } ( S ) = \sup \{ d ( 0 , z ) \colon z \text { is a point of } Z \text { in } S \} ,$$

where d(., ·) denotes the Euclidean distance on IRd.

Theorem 5.4 Let (X, ρ, λ) be a Boolean model with ρ as in (5.34). For l ≥ 0 and k ≥ 1 fixed, all functions a(λ) with a(λ) → 0 as λ → ∞ and for every

€ &gt; 0, we have, as λ → ∞,

- (i) Pλ(#W = (k, l)|the origin is the centre of a big ball)
- = exp(−λπd E(ρ + R)d + (l − (d − 1)k) log λ + O(1))
- (ii) Pλ(rad(W) &gt; a(λ)|#W = (k, I), the origin is the centre of a big ball) → 1,


<!-- p:149 -->


- (iii) Pλ(φ(λ) &lt; ∈|#W = (k, 1),

the origin is the centre of a big ball) → 1,

where φ(λ) is the relative density as introduced in the previous section.

The proof proceeds as in the last section. In the first lemma we obtain a lower bound, while in the subsequent lemmas we obtain an upper bound, In all the lemmas, we shall be working on the superposed model (Y, R, λp) * (Z, r, λ(1 - p)) and as such Pλ will incorporate the condition that there is a big ball at the origin. As in the previous section, S denotes the unit ball centred at the origin.

Lemma 5.7 For k and l fixed, as λ → ∞,

$$P _ { \lambda } \{ \# W & = ( k , l ) \} \\ & \geq \exp ( - \lambda \pi _ { d } E ( \rho + R ) ^ { d } + ( l - ( d - 1 ) k ) \log \lambda + O ( 1 ) ) .$$

Proof Given that there is a big ball at the origin, if the remaining k big balls are placed in the region α(k/λ)S where α = (pπd(2R)d−1)−1, and λ is so large that α(k/λ) &lt; 2 R, then the k big balls, together with the ball at the origin, are in the same component. (Note, as obtained in the previous section, α(k/λ) corresponds to the optimal diameter of the Poisson points in the component W when the Boolean model consists only of big balls; i.e. p = 1.) Now centre the l small balls in the region (R — r)S. If an annular region of width R of the component Wy formed by the k + 1 big balls is free of Poisson points of Y and an annular region of width r is free of Poisson points of Z, then W = Wy and #W = (k, l). Thus

$$& \text {an universal region of width } r \text { is free of Poisson points of } Z , \text { then } W = W \\ & \# W = ( k , l ) . \text { Thus} \\ & \quad P _ { \lambda } \{ \# W = ( k , l ) \} \\ & \quad \geq P _ { \lambda } \left \{ Y \left ( \alpha _ { \lambda } ^ { k } S \right ) = k , \, Z ( ( R - r ) S ) = l , \\ & \quad Y \left ( \left ( 2 R + \alpha _ { \frac { k } { \lambda } } \right ) S \right \rangle \alpha _ { \frac { k } { \lambda } } S \right ) = 0 , \\ & \quad Z \left ( ( R + r ) + \alpha _ { \frac { k } { \lambda } } ^ { k } \right ) S \left ( ( R - r ) S \right ) = 0 \right \} \\ & \quad = \exp \left ( - \lambda \left [ p \pi _ { d } \left ( \alpha _ { \frac { k } { \lambda } } ^ { k } \right ) ^ { d } + ( 1 - p ) \pi _ { d } ( R - r ) ^ { d } \right ] \right ) \\ & \quad \times \frac { | \lambda p \pi _ { d } ( \alpha ( k / \lambda ) ) ^ { d } | ^ { k } } { k ! } \frac { [ \lambda ( 1 - p ) \pi _ { d } ( R - r ) ^ { d } ] ^ { l } } { l ! }$$


<!-- p:150 -->


$$D i s t i n g i s h i n g e f a tures o f t h e P o i s s o n B o olean e n l \\ \times \exp \left ( - \lambda p \pi _ { d } \left [ \left ( 2 R + \alpha \frac { k } { \lambda } \right ) ^ { d } - \left ( \alpha \frac { k } { \lambda } \right ) ^ { d } \right ] \right ) \\ \times \exp \left ( - \lambda ( 1 - p ) \pi _ { d } \left [ \left ( R + r + \alpha \frac { k } { \lambda } \right ) ^ { d } - ( R - r ) ^ { d } \right ] \right ) \\ = \exp ( - \lambda \pi _ { d } [ p ( 2 R ) ^ { d } + ( 1 - p ) ( R + r ) ^ { d } ] ) \\ \times \exp \left ( - \lambda \pi _ { d } p \sum _ { j = 1 } ^ { d } \binom { d } { j } \left ( \alpha \frac { k } { \lambda } \right ) ^ { j } ( 2 R ) ^ { d - j } \right ) \\ \times \exp \left ( - \lambda \pi _ { d } ( 1 - p ) \sum _ { j = 1 } ^ { d } \binom { d } { j } \left ( \alpha \frac { k } { \lambda } \right ) ^ { j } ( R + r ) ^ { d - j } \right ) \\ \times \frac { [ \lambda p \pi _ { d } ( \alpha ( k / \lambda ) ) ^ { d } ] ^ { k } } { k ! } \frac { [ \lambda ( 1 - p ) \pi _ { d } ( R - r ) ^ { d } ] ^ { l } } { l ! } \\ = \exp ( - \lambda \pi _ { d } E ( \rho + R ) ^ { d } ) \\ \times \exp \left ( - \lambda \pi _ { d } \sum _ { j = 1 } ^ { d } \binom { d } { j } \left ( \alpha \frac { k } { \lambda } \right ) ^ { j } E ( \rho + R ) ^ { d - j } \right ) \\ \times \frac { [ \lambda p \pi _ { d } ( \alpha ( k / \lambda ) ) ^ { d } ] ^ { k } } { k ! } \frac { [ \lambda ( 1 - p ) \pi _ { d } ( R - r ) ^ { d } ] ^ { l } } { l ! } . \\$$

Using Stirling's formula for k! and /!, and noting that the quantity

$$\lambda \pi _ { d } \sum _ { j = 1 } ^ { d } \binom { d } { j } \left ( \alpha \frac { k } { \lambda } \right ) ^ { j } E ( \rho + R ) ^ { d - j }$$

is O(1) as λ → ∞, we have

$$is \, O ( 1 ) \, \text {as} \, \lambda \to \infty , \, \text {we have} \\ P _ { \lambda } \{ \# W = ( k , l ) \} \\ \geq \exp \left ( - \lambda \pi _ { d } E ( \rho + R ) ^ { d } + ( d - 1 ) k \log \frac { k } { \lambda } \right ) \\ + l \log \frac { \lambda ( 1 - p ) } { l } + l \log ( \pi _ { d } ( R - r ) ^ { d } ) + O ( 1 ) \right ) \\ \geq \exp \left ( - \lambda \pi _ { d } E ( \rho + R ) ^ { d } + ( l - ( d - 1 ) k ) \log \frac { k } { \lambda } + O ( 1 ) \right ) . \quad \Box$$

As in the previous section, we shall show an upper bound on the probability of obtaining #W = (k, l). In the next two lemmas we show that the probability that there is a Poisson point of either Y or Z at a distance at least R away from the origin is significantly smaller than the lower bound obtained in Lemma 5.7.


<!-- p:151 -->


Lemma 5.8 For some positive constants C1, C2, C3 and C4, we have

$$P _ { \lambda } \{ \# W & = ( k , l ) , \, \text {rad} _ { Y } ( W ) > 2 R \} \\ & \leq \exp \left ( - \lambda \pi _ { d } E ( \rho + R ) ^ { d } - \frac { \lambda } { 2 } p _ { d } \left ( \frac { R } { 2 } \right ) ^ { d } + C _ { 1 } k + C _ { 2 } l \right )$$

and

$$P _ { \lambda } \{ \# W = ( k , l ) , \, \text {rad} _ { Z } ( W ) > R + r \}$$

$$& \leq \exp \left ( - \lambda \pi _ { d } E ( \rho + R ) ^ { d } - \frac { \lambda } { 2 } ( 1 - p ) \pi _ { d } \left ( \frac { r } { 2 } \right ) ^ { d } + C _ { 3 } k + C _ { 4 } l \right ) .$$

Proof Let

$$A _ { i } \colon = \{ Y ( ( 2 R ) S ) = i \} \ \text { for } i = 0 , 1 \dots , k ,$$

$$B _ { j } \colon = \{ Z ( ( R + r ) S ) = j \} \quad \text {for } j = 0 , 1 , \dots , l .$$

Since the origin is the centre of a big ball, if #W = (k, l) and rady (W) &gt; 2R there can be at most k — 1 points of Y besides the origin in the ball (2R)S, while at most l small balls can be accommodated in the ball (R + r)S. Also if ymax is the point of Y in W which is farthest from the origin, then ymax| &gt; 2R and the hyperplane passing through y'max and perpendicular to the line joining the of  a  d s d-   dds      o and all the Poisson points of Y in W lie on one half-space H1 (say) and in the other half-space H2 (say) there is no point of Y which is at a distance less than 2R from ymax. This means that there must be a semisphere T(ymax) of radius 2R centred at ymax and lying in H2 which contains no points of Y.

To make this formal, we need a conditioning argument. First note that

$$P _ { \lambda } \left \{ \# W & = ( k , l ) , \, \text {rad} _ { Y } ( W ) \geq 2 R \right \} \\ & \leq \sum _ { m = 2 } ^ { k + l } P _ { \lambda } \left ( \# W = ( k , l ) , \, \ m R < \text {rad} _ { Y } ( W ) \leq ( m + 1 ) R \right ) .$$

$$\underline { m } = 2$$

To estimate the summands, we condition on Wp, the position of the Poisson points of both Y and Z in the ball (m + 1) RS. Let ymax be the farthest point of Y in Wp which is connected to the origin in Wp. From our discussion


<!-- p:152 -->


$$Y \text { in } W _ { p } \text { which is connected to the origin in } W _ { p } . \text { From our discussion} \\ P _ { \lambda } \{ \# W = ( k , l ) , \ m R < \ r a d _ { Y } ( W ) \leq ( m + 1 ) R \} \\ \leq \sum _ { i = 0 } ^ { k - 1 } \sum _ { j = 0 } ^ { l } E _ { \lambda } ( P _ { \lambda } ( \{ Y ( T ( y _ { \max } ) \rangle ( m + 1 ) R S ) = 0 \} \cap A _ { i } \cap B _ { j } | W _ { p } ) \\ k - 1 \leq \sum _ { i = 0 } ^ { k - 1 } E _ { \lambda } ( P _ { \lambda } ( \{ Y ( T ( y _ { \max } ) \rangle ( m + 1 ) R S ) = 0 \} | W _ { p } ) 1 _ { A _ { i } 1 } B _ { j } ) \\ \leq \exp ( - \lambda p \pi _ { d } ( R / 2 ) ^ { d } ) \sum _ { i = 0 } ^ { k - 1 } \sum _ { j = 0 } ^ { l } P _ { \lambda } ( A _ { i } ) P _ { \lambda } ( B _ { j } ) . \\ \\ \text {In the last inequality above we have used the fact that the events } A _ { i } \text { and } B _ { j } \text { are}$$

In the last inequality above we have used the fact that the events A and Bj are independent and that the distribution of the Poisson process outside (m + 1) RS is independent of Wp.

Now

$$Now & & \\ & \sum _ { i = 0 } ^ { k - 1 } \sum _ { j = 0 } ^ { l } P _ { \lambda } ( A _ { i } ) P _ { \lambda } ( B _ { j } ) \\ & = \exp ( - \lambda \pi _ { d } E ( \rho + R ) ^ { d } ) \\ & \times \sum _ { i = 0 } ^ { k - 1 } \sum _ { j = 0 } ^ { l } \frac { [ \lambda p \pi _ { d } ( 2 R ) ^ { d } ] ^ { i } } { i ! } \frac { [ \lambda ( 1 - p ) \pi _ { d } ( R + r ) ^ { d } ] ^ { j } } { j ! } . \quad ( 5 . 3 8 ) \\ \text {Let } c _ { j } > 1 \text { and } c _ { 2 } > 1 \text { be constants such that}$$

Let c1 ≥ 1 and c2 ≥ 1 be constants such that

$$( 2 R ) ^ { d } \leq \frac { c _ { \lfloor } } { 4 } \left ( \frac { R } { 2 } \right ) ^ { d } \quad \text {and} \quad ( 1 - p ) ( R + r ) ^ { d } \leq \frac { c _ { 2 } } { 4 } p \left ( \frac { R } { 2 } \right ) ^ { d } .$$

With this choice of c1 and c2, we see that

$$\text {this choice of } c _ { 1 } \text { and } c _ { 2 } , \text { we see that} \\ \sum _ { i = 0 } ^ { k - 1 } \sum _ { j = 0 } ^ { l } \frac { [ \lambda p \pi _ { d } ( 2 R ) ^ { d } ] ^ { i } } { i ! } \frac { [ \lambda ( 1 - p ) \pi _ { d } ( R + r ) ^ { d } ] ^ { j } } { j ! } \\ \leq \sum _ { i = 0 } ^ { k - 1 } \sum _ { j = 0 } ^ { l } \frac { [ \lambda p \pi _ { d } c _ { 1 } \frac { R ^ { d } } { 2 } ] ^ { i } } { i ! } \frac { [ \lambda p \pi _ { d } c _ { 2 } \frac { R ^ { d } } { 2 } ] ^ { j } } { j ! } \\ \leq c _ { 1 } ^ { k } c _ { 2 } ^ { l } \sum _ { i = 0 } ^ { \infty } \sum _ { j = 0 } ^ { \infty } \frac { [ \lambda p \pi _ { d } \frac { R ^ { d } } { 2 } ] ^ { i } } { i ! } \frac { [ \lambda p \pi _ { d } \frac { R ^ { d } } { 2 } ] ^ { j } } { j ! } \\ = c _ { 1 } ^ { k } c _ { 2 } ^ { l } \exp ( \lambda p \pi _ { d } R ^ { d } ) .$$


<!-- p:153 -->


Combining (5.37), (5.38) and (5.39) we obtain (5.35) with appropriate positive constants C1and C2.

The proof of (5.36) is similar and as such we present only an outline of it. Since the origin is the centre of a big ball, if #W = (k, I) and radz (W) &gt; R + r there can be at most I – 1 small balls centred in (R + r) S and, besides the ball at the origin, at most k big balls centred in (2R)S. As in the previous part, we obtain a point zmax and a semisphere T′(zmax) of radius 2r which is free of oi        s s    n sy

$$p ( 2 R ) ^ { d } \leq \frac { c _ { 3 } } { 4 } ( 1 - p ) \left ( \frac { r } { 2 } \right ) ^ { d } \quad \text {and} \quad ( R + r ) ^ { d } \leq \frac { c _ { 4 } } { 4 } \left ( \frac { r } { 2 } \right ) ^ { d } ,$$

we obtain the desired inequality (5.36).

口

Lemma 5.9 There exist positive constants C5, C6, C7 and C8 such that

$$P _ { \lambda } \{ \# W & = ( k , l ) , \ R \, < \, \text {rad} _ { Y } ( W ) \leq 2 R \} \\ & \leq \exp ( - \lambda \pi _ { d } E ( \rho + R ) ^ { d } - \lambda C _ { 5 } \pi _ { d - 1 } R ^ { d } + C _ { 6 } l )$$

and

$$P _ { \lambda } \{ \# W & = ( k , l ) , \ R < \ r a d _ { Z } ( W ) \leq R + r \} \\ & \leq \exp ( - \lambda \pi _ { d } E ( \rho + R ) ^ { d } - \lambda C _ { 7 } \pi _ { d - 1 } r ^ { d } + C _ { 8 } k ) .$$

Proof Throughout this proof, with a slight abuse of notation, we shall write Y ∩ C for the set of all points of Y in a region C ⊆ IRd. First observe that if rady(W) &gt; R then diam(Y ∩ W) &gt; R, where diam denotes the diameter of a set as introduced in the previous section. If Wp denotes the position of the Poisson points of both Y and Z in 2 RS, we can find two points y1 and y2 in Y ∩Wp which are the farthest apart among all pairs of points in Y ∩Wp, and let yo be the point in Y ∩ Wp which is farthest from the line joining y1 and y2. As in the proof of Lemma 5.3, we obtain half-spaces H1, H2 and Ho, such that H1 and H2 are disjoint and there exist two semispheres of radius 2R centred at yı and y2 respectively and also a region in Ho formed by a semisphere of radius 2 R and bounded in the slab lying between the half-spaces H1 and H2 which are all free of Poisson points of Y. If d(y1, y2) &gt; R, then (as justified in the proof of Lemma 5.3) the last region described above will have a Lebesgue measure at least c Rπd-1 (2 R)d−1 for some constant 0 &lt; c &lt; 1. Moreover, since there is a big ball at the origin, there can be at most / small balls centred in (R + r)S.


<!-- p:154 -->


A conditioning argument as in the previous lemma yields

$$P _ { \lambda } \{ \# W = ( k , l ) , \ R < \ r a d _ { Y } ( W ) \leq 2 R \} \\ \leq \exp ( - \lambda \pi _ { d } p ( 2 R ) ^ { d } ) \frac { ( \lambda \pi _ { d } p ( 2 R ) ^ { d } ) ^ { k } } { k ! } \exp ( - \lambda c \pi _ { d - 1 } R ^ { d } ) \\ \times \sum _ { j = 0 } ^ { l } \exp ( - \lambda \pi _ { d } ( 1 - p ) ( R + r ) ^ { d } ) \frac { [ \lambda \pi _ { d } ( 1 - p ) ( R + r ) ^ { d } ] ^ { j } } { j ! } . \\$$

Now choosing positive constants C5 and C6 suitably as in the previous lemma, we obtain (5.40).

The proof of (5.41) is similar and we omit it.

□

In the next lemma we consider the case when the big balls are centred in the optimal cluster region (α(k/λ))S for the big balls where α is as in the proof of Lemma 5.7.

Lemma 5.10 There is a constant C9 &gt; 0 such that

$$P _ { \lambda } & \left \{ \# W = ( k , l ) , \ r a d _ { Y } ( W ) \leq \alpha \frac { k } { \lambda } , \ r a d _ { Z } ( W ) \leq R \right \} \\ & \leq \exp ( - \lambda \pi _ { d } E ( \rho + R ) ^ { d } + ( l - ( d - 1 ) k ) \log \lambda + C _ { 9 } k ) ,$$

where α = (pπd(2R)d−1)−1.

Proof

$$P r o f \\ P _ { \lambda } \left \{ \# W = ( k , l ) , \ r a d _ { Y } ( W ) \leq \alpha \frac { k } { \lambda } , \ r a d _ { Z } ( W ) \leq R \right \} \\ \leq P _ { \lambda } \left \{ Y \left ( \alpha \frac { k } { \lambda } S \right ) = k , \ Y \left ( ( 2 R ) S \Big \langle \alpha \frac { k } { \lambda } S \right ) = 0 , \\ Z ( R S ) = l , \ Z ( ( R + r ) S \Big \rangle R S ) = 0 \right \} \\ \leq \exp \left ( - \lambda p \pi _ { d } \left ( \alpha \frac { k } { \lambda } \right ) ^ { d } - \lambda ( 1 - p ) \pi _ { d } R ^ { d } \right ) \frac { [ \lambda p \pi _ { d } ( \alpha \frac { k } { \lambda } ) ^ { d } ] ^ { k } } { k ! } \frac { [ \lambda ( 1 - p ) \pi _ { d } R ^ { d } ] ^ { l } } { l ! } \\ \times \exp \left ( - \lambda \pi _ { d } \left [ P \left ( ( 2 R ) ^ { d } - \left ( \alpha \frac { k } { \lambda } \right ) ^ { d } \right ) \right ) \\ \\ + ( 1 - p ) ( ( R + r ) ^ { d } - R ^ { d } ) \right ] \right ) .$$


<!-- p:155 -->


T oa g   a ona  f (a ng oa o m suitable C9. □

To take care of medium-sized clusters, we need a result similar to Lemma 5.3.

Lemma 5.11 Let μ &gt; 1 and define, for y &gt; 0,

$$\psi _ { \mu } ( y ) \colon = \frac { p \pi _ { d - 1 } ( 2 R ) ^ { d - 1 } y } { 4 } - \log ( e p \pi _ { d } \mu ^ { d } y ^ { d } ) .$$

There exists a constant C10 &gt; 0 such that, for λ large with μy(k/λ) &lt; 2R, we have

$$P _ { \lambda } \left \{ \# W = ( k , l ) , \ y _ { \frac { k } { \lambda } } ^ { k } < \text {rad} _ { Y } ( W ) \leq \mu y _ { \frac { k } { \lambda } } ^ { k } \, a n d \, \text {rad} _ { Z } ( W ) \leq R \right \} \\$$

$$\leq \exp ( - \lambda \pi _ { d } E ( \rho + R ) ^ { d } + ( l - ( d - 1 ) k ) \log \lambda - k \psi _ { \mu } ( y ) + C _ { 1 0 } ( k ) ) .$$

Proof The proof closely follows the proof of Lemma 5.3. Let

$$\Pi _ { Y } \coloneqq Y \cap \left ( \mu y \frac { k } { \lambda } \right ) S , \ \Pi _ { Z } \coloneqq Z \cap R S$$

$$A \coloneqq \left \{ Y \cap \left ( \mu \frac { k } { \lambda } \right ) S = k \right \} , \quad B \coloneqq \{ Z ( R S ) = l \} .$$

and let and let

For a &gt; 0 let

$$S _ { Y } ( a ) \colon = \cup _ { y \in ( \Pi _ { Y } \ \{ 0 \} ) } S ( y , a ) , \quad S _ { Z } ( a ) \colon = \cup _ { z \in \Pi _ { Z } } S ( z , a ) .$$

If μy(k/λ) &lt; 2 R, then all the big balls are in the same component, and so, as in (5.14), we have

$$in ( 5 . 1 4 ) , \, \text {we have} \\ P _ { \lambda } \left \{ \# W = ( k , l ) , \, y \frac { k } { \lambda } < \ r a d _ { Y } ( W ) \leq \mu y \frac { k } { \lambda } \, \text {and} \, \ r a d _ { Z } ( W ) \leq R \right \} \\ = E _ { \lambda } \left ( P _ { \lambda } \left \{ \# W = ( k , l ) , \, y \frac { k } { \lambda } < \ r a d _ { Y } ( W ) \leq \mu y \frac { k } { \lambda } \right \} \\ \quad \text {and} \, \ r a d _ { Z } ( W ) < R | \Pi _ { Y } , \Pi _ { Z } \rangle \\ = E _ { \lambda } \left ( 1 _ { A 1 } b P _ { \lambda } \left \{ Y \left ( ( S _ { Y } ( 2 R ) \cup S _ { Z } ( R + r ) ) \bigwedge \left ( \mu y \frac { k } { \lambda } \right ) s \right ) = 0 , \\ Z ( ( S _ { Y } ( R + r ) \cup S _ { Z } ( 2 R ) ) \bigwedge R ) = 0 | \Pi _ { Y } , \Pi _ { Z } \right \} \right ) .$$


<!-- p:156 -->


Since there is a big ball at the origin, l(Sy (R + r)\ RS) ≥ πd((R + r)d − Rd). Also, if radγ &gt; y(k /λ), then exactly the same argument as used to justify (5.15) and (5.16) yields

$$& \text {and} \, ( S . 1 0 ) \, y \text {extends} \, \\ & \quad \ell \left ( S _ { Y } ( 2 R ) \Big \langle \left ( \mu y \frac { k } { \lambda } \right ) S \right ) \geq \pi _ { d } ( 2 R ) ^ { d } + \pi _ { d - 1 } ( 2 R ) ^ { d - 1 } y \frac { k } { 4 \lambda } - \pi _ { d } \left ( \mu y \frac { k } { \lambda } \right ) ^ { d } . \\ & \text {Combining this observation with } ( 5 4 ) \text { and using independent properties we}$$

Combining this observation with (5.44) and using independence properties we have

$$Combining this observation with ( 5 . 4 4 ) and using independent properties we
have \\ P _ { \uparrow } \left \{ \# W = ( k , l ) \ y _ { \lambda } ^ { k } \ < \ r a d _ { Y } ( W ) \leq \mu y _ { \lambda } ^ { k } \text { and } r a d _ { Z } ( W ) \leq R \right \} \\ \leq \exp \left ( - \lambda p \pi _ { d } \left ( \mu y _ { \lambda } ^ { k } \right ) ^ { d } - \lambda ( 1 - p ) \pi _ { d } R ^ { d } \right ) \\ \times \frac { [ \lambda p \pi _ { d } ( \mu y ( k / \lambda ) ) ^ { d } ] ^ { k } } { k ! } \frac { [ \lambda ( 1 - p ) \pi _ { d } R ^ { d } ] ^ { \mu } } { l ! } \\ \times \exp \left ( - \lambda p \left [ \pi _ { d } ( 2 R ) ^ { d } + \pi _ { d - 1 } ( 2 R ) ^ { d - 1 } y \frac { k } { 4 \lambda } - \pi _ { d } \left ( \mu y \frac { k } { \lambda } \right ) ^ { d } \right ] \right ) \\ \times \exp ( - \lambda \pi _ { d } ( 1 - p ) ( ( R + r ) ^ { a } - R ^ { d } ) ) \\ \leq \exp ( - \lambda \pi _ { d } E ( \rho + R ) ^ { d } + ( l - ( d - 1 ) k \log \lambda \\ - k \psi _ { \mu } ( y ) + C _ { 1 0 } k ) , \\ \text {for some positive constant } C _ { 1 0 } , \text { where we have used Striling's formula in the } \\ \text {last inequality.}$$

for some positive constant C1o, where we have used Stirling's formula in the last inequality. □

We use the previous lemma to take care of medium-sized components.

Lemma 5.12 There exists β &lt; ∞, a positive constant C11 and λ0 &lt; ∞ such that, for λ ≥ λo,

$$P _ { \lambda } & \left \{ \# W = ( k , l ) , \ \beta \frac { k } { \lambda } < \ r a d _ { Y } ( W ) \leq R , \ r a d _ { Z } ( W ) \leq R \right \} \\ & \leq \exp ( - \lambda \pi _ { d } E ( \rho + R ) ^ { d } + ( l - ( d - 1 ) k ) \log \lambda + C _ { l 1 } k ) .$$

Proof Fix μ &gt; 1 and choose β large such that ψμ(μjβ) ≥ j for every j ≥ 1. (Note, the function ψμ admits such a choice.) Let λo be such that, for all λ ≥ λo,

$$\beta \mu \frac { k } { \lambda } < r _ { 1 } \, \text {and, for some } j \geq 1 , \ R < \beta \mu ^ { j } \frac { k } { \lambda } \leq 2 \, R .$$


<!-- p:157 -->


Let N := min{ j : βμj k &gt; R}. From (5.47), N ≥ 1. As in Lemma 5.5 we cover the interval (βμ(k/λ), R] by intervals of the type (βμj−1(k/λ), βμj(k/λ)], j = 0, 1, . . . , N − 1, and apply Lemma 5.11 to obtain, for k ≥ 1,

$$Let N \coloneqq \min \{ j \colon \beta \mu ^ { j } k > R \} . \text { From (5.47), } N \geq 1 . \text { As in Lemma 5.5 we cover } \\ \text { the interval } ( \beta u ( k / \lambda ) , R ) \text { by intervals of the type } ( \beta \mu ^ { j - 1 } ( k / \lambda ) , \beta \mu ^ { j } ( k / \lambda ) ] , \\ j = 0 , 1 , \dots , N - 1 , \text { and apply Lemma 5.11 to obtain, for } k \geq 1 , \\ P _ { \lambda } \left \{ \# W = ( k , l ) , \ \beta \frac { k } { \lambda } < \text { rad} ( W ) \leq R , \ \text { rad} z \leq R \right \} \\ N - 1 \\ \leq \sum _ { j = 0 } P _ { \lambda } \left \{ \# W = ( k , l ) , \ \beta \mu ^ { j } \frac { k } { \lambda } < \text { rad} ( W ) \leq \beta \mu ^ { j + 1 } \frac { k } { \lambda } , \ \text { rad} z ( W ) \leq R \right \} \\ \\ \leq \sum _ { j = 0 } ^ { N - 1 } \exp ( - \lambda \pi _ { d } E ( \rho + R ) ^ { d } + ( l - ( d - 1 ) k ) \log \lambda \\ - k \psi _ { \mu } ( \beta \mu ^ { j } ) + C _ { 1 0 } k ) \\ \leq \exp ( - \lambda \pi _ { d } E ( \rho + R ) ^ { d } + ( l - ( d - 1 ) k ) \log \lambda + C _ { 1 0 } k ) \\ \times \sum _ { j = 0 } ^ { N - 1 } \exp ( - k \psi _ { \mu } ( \beta \mu ^ { j } ) ) \\ \leq \exp ( - \lambda \pi _ { d } E ( \rho + R ) ^ { d } + ( l - ( d - 1 ) k ) \log \lambda + C _ { 1 0 } k ) \\ \times \sum _ { j = 0 } ^ { \infty } \exp ( - k j ) \\ \leq 2 \exp ( - \lambda \pi _ { d } E ( \rho + R ) ^ { d } + ( l - ( d - 1 ) k ) \log \lambda + C _ { 1 0 } k ) . \\ \text {This proves the lemmma.}$$

This proves the lemma.

□

Proof of Theorem 5.4 To begin with, we observe that Lemmas 5.8–5.12 obtain upper bounds for all possible radii of the component W except the case when α(k/λ) &lt; radγ(W) ≤ β(k/λ) (if α &lt; β) and radz(W) ≤ R. For this case, we may apply Lemma 5.11 with μ = β/α &gt; 1 to obtain

$$P _ { \lambda } \left \{ \# W & = ( k , l ) , \, \alpha \frac { k } { \lambda } < \ r a d _ { Y } ( W ) \leq \beta \frac { k } { \lambda } , \, \ r a d _ { Z } \leq R \right \} \\ & \leq \exp ( - \lambda \pi _ { d } E ( \rho + R ) ^ { d } + ( l - ( d - 1 ) k ) \, \log \lambda \\ & - k \psi _ { \mu } ( \alpha ) + C _ { 1 2 k } ) ,$$

« here C12 is a positive constant depending on μ.

The upper bounds obtained in (5.48), Lemmas 5.8, 5.9, 5.10 and 5.12 together with the lower bound obtained in Lemma 5.7 prove (i) of the theorem.


<!-- p:158 -->


To prove (ii), we observe that, for 0 &lt; a(λ) &lt; R − r,

$$P _ { \lambda } \{ \text {rad} ( W ) > a ( \lambda ) | \# W = ( k , l ) \} \\ & \leq P _ { \lambda } \{ \text {rad} _ { Z } ( W ) > a ( \lambda ) | \# W = ( k , l ) \} \, .$$

Since a big ball is placed at the origin, if radz(W) ≤ R, the small balls may be centred uniformly in (R — r)S without affecting the component. Thus,

$$P _ { \lambda } \{ \text {rad} _ { Z } ( W ) > a ( \lambda ) | \# W = ( k , l ) , \, \text {rad} _ { Z } ( W ) \leq R \} \geq 1 - \left ( \frac { a ( \lambda ) } { R - r } \right ) _ { \substack { . \\ ( 5 . 5 0 ) } } ^ { d l } .$$

Now choose a(λ) such that a (λ) → 0 as λ → ∞, to obtain, from (5.49), (5.50), (5.36), (5.41) and (i) of the theorem,

$$P _ { \lambda } \{ r a d ( W ) > a ( \lambda ) | \# W = ( k , l ) \} \to 1 \text { as } \lambda \to \infty .$$

Finally, Finally,

$$\phi ( \lambda ) = \frac { k + l + 1 } { \lambda \ell ( W _ { H } ) } \leq \frac { k + l + 1 } { \lambda \pi _ { d } ( r a d ( W ) ) ^ { d } } .$$

In (ii) if we choose a(λ) such that a(λ) → 0 and λa(λ)d → ∞ as λ → ∞, then we have, as λ → ∞,

$$P _ { \lambda } \left \{ \phi ( \lambda ) \leq \frac { k + l + 1 } { \pi _ { d } \lambda a ( \lambda ) ^ { d } } | \# W = ( k , l ) \right \} \to 1 .$$

This proves (iii).

### 5.4 Notes

Kertesz and Vicsek (1982) conjectured, based on simulations, that the critical covered volume fraction should be a universal constant for all Poisson Boolean models. In Phani and Dhar (1984) a heuristic argument was given showing that this is not the case, and finally the conjecture was disproved (Theorem 5.1 above) in Meester, Roy and Sarkar (1994). The results in Section 5.2 are due to Alexander (1991), and the results in Section 5.3 are taken from Sarkar (1994).


<!-- p:159 -->


and and

#### The Poisson random-connection model

A random-connection model (RCM) which is driven by a Poisson process with density λ and connection function g will be denoted by (X, g, λ). In this chapter we will always assume that X has a point at the origin. In Section 1.5, we defined g as a function from IR into [0, 1], and two points x1 and x2 of X are connected to each other with probability g(|x1 — x2). It will be convenient however, to define g as a function from IRa into [0, 1] with the following restrictions:

(| = |x|  ( = (x)

g(x) ≤ g(y) whenever |x| ≥ |y|.

The only reason for this different point of view is that the notation and formulae will be somewhat simpler.

As in Boolean models, some restrictions on g are necessary in order to obtain a non-trivial model, i.e. a model with a non-trivial phase transition. The first section of this chapter is devoted to that problem. In the second section, we shall derive some useful but technical results concerning the connection function g. In the third section, we shall demonstrate that unlike the Boolean model, equality of the two most important critical densities is always true here. Further topics in this chapter are uniqueness and high-density processes.

Unfortunately, the proofs in the RCM tend to be quite technical. To some extent, this is the price we have to pay for allowing a large class of connection functions. The ideas behind the various proofs, however, are very often not so hard to grasp, and we shall always try to give the reader an idea of what is going on. Some words about the notation: we denote by W (x) the component containing the point x of X, and W denotes the component containing the origin. The cardinality of a component W is denoted by W|. The origin itself is as earlier denoted by 0. The probability measure in the model will be denoted by P(λ,g) = Pλ = P, when no confusion is possible and the corresponding expectation operator will be denoted by E(λ,g) = Eλ = E.


<!-- p:160 -->


### 6.1 Non-triviality of the model

It  n   t  t    n n is st a.s. For this, we just take a look at Proposition 1.3. If Y denotes the (random) number of points of X which are connected directly to the origin, then we see that

$$P ( Y = k ) = e ^ { - \lambda \int _ { \mathbb { R } ^ { d } } g ( x ) \, d x } \frac { ( \lambda \int _ { \mathbb { R } ^ { d } } g ( x ) \, d x ) ^ { k } } { k ! } .$$

Hence, if ∫Rd g(x) dx = ∞, then P(Y = k) = 0 for all k and the conclusion is that Y = ∞ a.s. This is true for all λ &gt; 0, and it implies that percolation occurs for all positive values of λ. So in order for the model to become more interesting, we need the condition

$$0 < \int _ { \mathbb { R } ^ { d } } g ( x ) \, d x < \infty .$$

Our first result shows that this necessary condition is also sufficient for the occurrence of a non-trivial phase transition. We write θg(λ) = θ(λ) = P(λ.g)(|W| = ∞) and χ (λ) = xg(λ) = E(a,g)(IWI).

Theorem 6.1 Consider a Poisson RCM (X, g, λ) in IRd, for d ≥ 2. If g satisfies (6.2), then there exist two densities 0 &lt; λτ(g) ≤ λH (g) &lt; ∞ such that

- (1) x(λ) &lt; ∞ forλ &lt; λτ(g), and x(λ) = ∞ forλ &gt; λτ(g).
- (2) θ(λ) = 0 for λ &lt; λH(g) and θ(λ) &gt; 0 for λ &gt; λH(g).

Proof Using coupling as before, we see that both X and θ are non-decreasing in λ, whence it is clear that λτ (g) and λ  (g) with the properties in (1) and (2) exist and that λτ (g) ≤ λH(g). It suffices therefore to show that λτ (g) &gt; 0 and that λH(g) &lt; ∞.

We need to show then, that for λ sufficiently small (but positive) the expected size of W is finite. We tackle this problem with a branching process argument together with coupling. The branching process argument is quite similar to that in Chapter 3. As we saw in (6.1), the expected number of points connected directly to the origin is equal to λ ∫Ra g(x) dx. More precisely, the points connected directly to the origin form a non-homogeneous Poisson process with intensity function λg(x). We denote this point process by Xo. We are going to build' a Poisson process as the superposition of many non-homogeneous Poisson processes as follows. Suppose that the points of X0 are given by x1, x2, . . . , xn. We call this the points of the first generation. To construct the second generation we proceed as follows. Take the first point, x1, of the first generation, and superpose it with a non-homogeneous Poisson process X} with intensity function λ(1 − g(x)) g(x − x1) and which is independent of X0. The occurrences of X1 are the second generation points coming from x1 and they represent all points which are connected to x1 (and possibly to x2, .. . , x) but not to the origin. For x2, we take another non-homogeneous Poisson process X2 with intensity fn  {X  0X  d '(x- x)((x - x)8 -  )((x) - 1) s are the points of the second generation coming from x2 and they represent all points which are connected to x2 but not to the origin and x1. We continue this procedure in the obvious way, obtaining non-homogeneous Poisson processes X1, ..., X1 which are all independent of each other. For each i, the intensity function of Xì contains the factor g(x – x) and therefore Xį can be coupled to independent non-homogeneous Poisson processes X with intensity functions λg(x — x) such that the occurrences of Xi are a subset of the occurrences of i. The total number of points of X is a random variable with a Poisson dis    (x  f  = x (x - x f  d  she coupling just described, the total number of points in the second generation is bounded from above by the total number of points in the second generation of ag d s ss r  og ao na to λ ∫Ra g(x) dx. In general, the number of points in the n-th generation is bounded from above by the number of points in the n-th generation of such a branching process. It is well known (see e.g. Grimmett and Stirzaker 1992, Lemma 5.4.2) that the expected number of points in the n-th generation of an ordinary Galton-Watson branching process with expected offspring μ is equal to μ". Hence, the expected number of points in W satisfies


<!-- p:161 -->


$$E _ { \lambda } ( | W | ) \leq \sum _ { n = 1 } ^ { \infty } \left ( \lambda \int _ { \mathbb { R } ^ { d } } g ( x ) \, d x \right ) ^ { n } .$$

Thus, if g satisfies (6.2) we can choose λ &lt; (SRa g(x) d x)−1 to make the sum in (6.3) finite. This shows that λτ (g) ≥ (∫IRd g(x) dx)−1 &gt; 0.

For the second part of the theorem we need to show that for λ sufficiently large, we have |W | = ∞ with positive probability. For this, we use the notion of the Lebesgue set of a function g. This is defined as the set of points y ∈ IRd such that

$$\lim _ { * \downarrow 0 } ( 2 \epsilon ) ^ { d } \int _ { v _ { * } + \beta _ { * } } | g ( x ) - g ( y _ { 0 } ) | \, d x = 0 ,$$


<!-- p:162 -->


where Be = [−∈, ∈]d and y + B€ denotes the set {y + x : x ∈ Be}. It is well known (see Rudin 1970, Theorem 8.8) that the Lebesgue set of g has full Lebesgue measure. Hence we can select d linearly independent points yi, . . . , yd which are all in the Lebesgue set of g and for which g(yi) &gt; 0, i = 1, . . . , d. From (6.4) it follows that we can find δ &gt; 0 such that for all i and for all boxes B with side length at most δ containing some yi,

$$( 6 , 5 )$$

for all i. At the same time, δ can be taken so small that all sets of the form n1yi + .. + ndyd + B8 =: B8(n1, ... , nd), n1, ..., nd ∈ Z, are mutually disjoint.

For any edge e in Zd between vertices (n1, . .. , nd) and (m1, . .. , md) with Σi=1 ni − m| = 1, we place an independent Poisson process Xe with density (2d)− 1 λ on the boxes B8 (n  , . . . , nd) and B8 (m 1, . . . , md). On the complement of the union of all these sets, we place a Poisson process X* with density λ, independent of all other processes. The superposition of X* with Xe for all edges e yields a homogeneous Poisson process X with density λ on IRa.

Let n = (n1, . . . , nd) and m = (m1, . . . , md) be such that ∑i=1 |ni − mi| = 1 and let e be the edge between n and m. Then B8 (m) can be written as B8 (n) + yi for suitable i. Given a point x of X in the box B8(n), the probability that x is not connected to any point of Xe in B8 (m) is then equal to

$$& \leq \exp \left ( - \lambda ( 2 d ) ^ { - 1 } \frac { 1 } { 2 } ( 2 \epsilon ) ^ { d } g ( y _ { t } ) \right ) \\ & = \exp \left ( - \lambda ( 4 d ) ^ { - 1 } ( 2 \epsilon ) ^ { d } g ( y _ { t } ) \right ) ,$$

where B8 = B8(m1,..., md) and where we have used (6.5). Now we can perform independent bond percolation on Zd as follows. The cluster C of the origin in this discrete percolation model is built in steps. We start with C consisting of the origin only, and define xo to be the origin. In an inductive fashion, assume that C consists of a finite number of vertices such that for each n ∈ C, we have chosen a point xn of X inside the box B(n). Next we consider an edge e between n and m which has not been considered before, such that n belongs to C, but m does not. If no such edge exists we stop, but if it exists we check whether or not there is a point of Xe in B8(m) which is connected to xn. If such a point exists we choose one, denote it by xm and add m to C.


<!-- p:163 -->


It follows from the construction and (6.6) that the cluster C obtained by this procedure can be seen as the cluster of the origin in discrete bond percolation with parameter at least min1≤i≤d{1 − e−λ(4d)-1(2e) g(r)}. Hence for λ sufficiently large, the probability that the cluster of the origin is infinite (which means that the inductive procedure above does not stop) is positive. But if C is infinite, then certainly the component W in the underlying RCM is unbounded. This observation completes the proof of the theorem. 0

### 6.2 Properties of the connection function

In this section we collect some technical results which will be used later. At this stage, the idea behind the various definitions might not be so clear, but the readability of the subsequent section certainly increases if we isolate all technical lemmas. Readers not interested in technical details may just note the statements of the results and move on to the next section.

First, we define three functions based on the connection function g.

Definition 6.1 For L &gt; 0, the function gL : IRd → [0, 1] is defined as

$$g _ { L } ( x ) = 1 - \prod _ { z \in \mathcal { Z } ^ { d } } ( 1 - g ( x + 2 L z ) ) .$$

Definition 6.2 For y, x1, ..., xk ∈ IRd, let g1(y; x1, ..., xk) be the probability that in the random graph with (non-random) vertices y, x1,..., xk and connection function g, the point y is not isolated. Furthermore, g2(x1, ... , xk) is defined to be the probability that the graph with vertices X1, .. . , Xk and connection function g is connected.

It is clear from the definition that gL (x) ≥ g(x) for all L and x. Here are some further properties of g and gL:

####### Proposition 6.1

- (i) For every L, the function gL is continuous almost everywhere (with respect to Lebesgue measure).
- (ii) For all ∈ &gt; 0, we have, for all L large enough, {gL (x) − g(x)| &lt; ∈, for all x ∈ B1..

(iii) limL .∞ ∫B, 81 (x)dx − ∫md g(x) dx.


<!-- p:164 -->


Proof (i) As g is a non-increasing function of the absolute value, its set of discontinuities has Lebesgue measure zero. Hence, we can restrict our attention to those x for which g is continuous at all points of the form x + 2Lz, z ∈ Za.

First suppose x is such that g(x + 2Lz) = 1 for some z ∈ Zd. Then of course gL (x) = 1. For any sequence {xn} converging to x we have that g(xn + 2L z) → 1 and it follows that also gL (xn) → 1.

Now suppose g(x + 2Lz) &lt; 1 for all z. This implies that g(x + 2Lz) is bounded away from 1. Furthermore, if {x} converges to x, it follows from the continuity of g at all points x + 2Lz and the fact that g(z) tends to zero whenever |z| tends to infinity, that g(xn + 2Lz) is uniformly bounded away from 1, for all z and for all n large enough. We now have − log(1 - gL (x)) = ∑z∈zd − log(1 − g(x + 2Lz)). It is enough to show that we can interchange limit and sum in the expression limn→∞ Σzezd − log(1 - g(xn + 2L z)). This is not hard, we write, for large K:

$$r d , \, w e \, w i t e , \, f o r \, l o g e \, K \colon \\ \sum _ { | z | > K } - \log ( 1 - g ( x _ { n } + 2 L z ) ) \\ = \sum _ { | z | > K } \log ( ( 1 - g ( x _ { n } + 2 L z ) ) ^ { - 1 } ) \\ = \sum _ { | z | > K } \log \left ( 1 + \sum _ { k = 1 } ^ { \infty } ( g ( x _ { n } + 2 L z ) ) ^ { k } \right ) . \\ \intertext { d o w $ e $ } \int o n d e f o r $ a $ b o w$$

This is bounded from above by

$$\sum _ { | z | > K } \frac { g ( x _ { n } + 2 L z ) } { 1 - g ( x _ { n } + 2 L z ) } \leq C \sum _ { | z | > K } g ( x _ { n } + 2 L z ) ,$$

for some constant C. This tends to zero uniformly in n when K → ∞, using condition (6.2).

For (ii), let x ∈ BL be arbitrary. For any € &gt; 0, we can take L large enough so that

$$\prod _ { z \in \mathbb { Z } ^ { d } \ \{ 0 \} } ( 1 - g ( x + 2 L z ) ) \\ \geq 1 - \sum _ { z \in \mathbb { Z } ^ { d } \ \{ 0 \} } g ( x + 2 L z ) \\ \geq 1 - \int _ { \mathbb { R } ^ { d } \ B _ { L - 1 } } g ( y ) \, d y \geq 1 - \epsilon .$$

(Here we use the integrability condition (6.2).) For such L, we thus find that (x) - (x     (x) - )( - )  (x  - gL (x) ≥ g(x) for all x, the result follows.


<!-- p:165 -->


For (iii) we write

$$g _ { L } ( x ) = 1 - \prod _ { z \in \mathcal { Z } ^ { d } } ( 1 - g ( x + 2 L z ) ) \leq \sum _ { z \in \mathcal { Z } ^ { d } } g ( x + 2 L z ) .$$

Thus, on the one hand,

$$1 \, \text {one hand} , \\ \int _ { B _ { L } } g _ { L } ( x ) \, d x & \leq \int _ { B _ { L } } \sum _ { z \in \mathcal { Z } ^ { d } } g ( x + 2 L z ) \, d x \\ & = \sum _ { z \in \mathcal { Z } ^ { d } } \int _ { B _ { L } } g ( x + 2 L z ) \, d x \\ & = \int _ { \mathbb { R } ^ { d } } g ( x ) \, d x . \\ \intertext { f o r } \text {hand} , \int _ { \mathbb { R } ^ { d } } g ( x ) \, d x . \\$$

Onthe otherhand, ∫BL gL(x)dx ≥ ∫BL g(x)dx, which converges to ∫Rd g(x)dx when L → ∞. □

The next result explains why gı and g2 are defined the way they are:

Proposition 6.2 Consider a Poisson RCM (X, g, λ) in IRd. It is the case that

$$P o s t i o n & \, 6 . 2 \, \text { consider a Poisson RCM } ( x , g , \lambda ) \, \text { in } \text { R-} . \, \text { its the case that} \\ & \quad P ( | W | = k , W \subset B _ { n } ) = \frac { \lambda ^ { k - 1 } } { ( k - 1 ) ! } \int _ { B _ { n } \times \cdots \times B _ { n } } g _ { 2 } ( 0 , x _ { 1 } , \dots , x _ { k - 1 } ) \\ & \quad \times \exp \left ( - \lambda \int _ { \mathbb { R } ^ { d } } g _ { 1 } ( y ; 0 , x _ { 1 } , \dots , x _ { k - 1 } ) \, d y \right ) d ( x _ { 1 } , \dots , x _ { k - 1 } ) .$$

Proof We denote by E(k, n) the event that {W| = k and W ⊂ Bn. Conditioned o'  vsn v    -    t   =   t   n that the m points of X in B are uniformly distributed on Bn. This implies that (remember that the origin always belongs to W)

$$P ( E ( k , n ) \, | \, X ( B _ { n } ) = m ) & = \binom { m } { k - 1 } ( 2 n ) ^ { - d m } \\ & \times \int _ { B _ { n } } \cdots \int _ { B _ { n } } P ^ { \prime } ( W = \{ 0 , x _ { 1 } , \dots , x _ { k - 1 } \} ) \, d x _ { 1 } \cdots d x _ { m } ,$$

where P' denotes the probability measure of a RCM where we superpose the origin 0 and the points x1, . . . , xm–1 with a Poisson process with density λ on the complement of Bn, and connect any two points according to the connection function g as usual.

The probability that a point y is connected to at least one of the points {0), x1, . . . , xk − 1} is g1(y; 0, x1, . . . xk−1) by definition. Hence the probability


<!-- p:166 -->


that no point of the Poisson process with density λ on the complement of Bn is connected to any of the points 0, x1, . . . , xk is equal to

$$\exp \left ( - \lambda \int _ { \mathbb { R } ^ { d } \bigtriangledown B _ { n } } g _ { 1 } ( y ; 0 , x _ { 1 } , \dots , x _ { k - 1 } ) \, d y \right ) .$$

From the definition of g2 we then obtain

$$\text {the definition of} \, g _ { 2 } \text { we then obtain} \\ P ^ { \prime } ( W = \{ 0 , x _ { 1 } , \dots , x _ { k - 1 } \} ) & = g _ { 2 } ( 0 , x _ { 1 } , \dots , x _ { k - 1 } ) \\ & \times \exp \left ( - \lambda \int _ { \mathbb { R } ^ { d } } \, g _ { 1 } ( y ; 0 , x _ { 1 } , \dots , x _ { k - 1 } ) \, d y \right ) \\ & \times \prod _ { i = k } ^ { m } ( 1 - g _ { 1 } ( x _ { i } ; 0 , x _ { 1 } , \dots , x _ { k - 1 } ) ) . \\ \text {s we substitute into} \, 6 ( 9 ) \text { to obtain}$$

This we substitute into (6.9) to obtain

$$This we substitute into ( 6 . 9 ) to obtain \\ P ( E ( k , n ) \cap \{ X ( B _ { n } ) = m \} ) & = e ^ { - \lambda ( 2 n ) ^ { d } } \lambda ^ { m } ( ( k - 1 ) ! ( m - ( k - 1 ) ) ! ) ^ { - 1 } \\ & \times \int _ { B _ { n } } \cdots \int _ { B _ { n } } g _ { 2 } ( 0 , x _ { 1 } , \dots , x _ { k - 1 } ) \\ & \times \exp \left ( - \lambda \int _ { \mathbb { R } ^ { d } \, \mathbb { B } _ { n } } g _ { 1 } ( \gamma ; 0 , x _ { 1 } , \dots , x _ { k - 1 } ) \, d y \right ) \\ & \times \left ( \int _ { B _ { n } } ( 1 - g _ { 1 } ( z ; 0 , x _ { 1 } , \dots , x _ { k - 1 } ) ) \, d z \right ) ^ { m - ( k - 1 ) } \, d x _ { 1 } \cdots d x _ { k - 1 } .$$

Summing this last expression over m ≥ k - 1 yields

$$S u mming \text { this last expression over } m & \geq k - 1 \text { yields} \\ P ( E ( k , n ) ) & = \frac { e ^ { - \lambda ( 2 n ) ^ { d } } \lambda ^ { k - 1 } } { ( k - 1 ) ! } \int _ { B _ { n } } \cdots \int _ { B _ { n } } g _ { 2 } ( 0 , x _ { 1 } , \dots , x _ { k - 1 } ) \\ & \quad \times \exp \left \{ \lambda \int _ { B _ { n } } ( 1 - g _ { 1 } ( 2 , 0 , x _ { 1 } , \dots , x _ { k - 1 } ) ) d z \right \} \\ & \quad - \lambda \int _ { \mathbb { R } ^ { d } \sqrt { B _ { n } } } g _ { 1 } ( y ; 0 , x _ { 1 } , \dots , x _ { k - 1 } ) d y \right \} d x _ { 1 } \cdots d x _ { k - 1 } \\ & = \frac { e ^ { - \lambda ( 2 n ) ^ { d } } \lambda ^ { k - 1 } } { ( k - 1 ) ! } \int _ { B _ { n } } \cdots \int _ { B _ { n } } g _ { 2 } ( 0 , x _ { 1 } , \dots , x _ { k - 1 } ) \\ & \quad \times \exp \left \{ - \lambda \int _ { \mathbb { R } ^ { d } } g _ { 1 } ( y ; 0 , x _ { 1 } , \dots , x _ { k - 1 } ) d y + \lambda \int _ { B _ { n } } d z \right \} \\ & \quad d x _ { 1 } \cdots d x _ { k - 1 }$$


<!-- p:167 -->


$$b . 3 \, \text {Equality of the critical densities} \\ = \frac { \lambda ^ { k - 1 } } { ( k - 1 ) ! } \int _ { B _ { n } } \cdots \int _ { B _ { n } } g _ { 2 } ( 0 , x _ { 1 } , \dots , x _ { k - 1 } ) \\ \times \exp \left \{ - \lambda \int _ { \mathbb { R } ^ { d } } g _ { 1 } ( y ; 0 , x _ { 1 } , \dots , x _ { k - 1 } ) \, d y \right \} d x _ { 1 } \cdots d x _ { k - 1 } .$$

Finally, we shall need the following result:

Proposition 6.3 Suppose that g has bounded support. Then we have

$$\liminf _ { | h | \to 0 } | h | ^ { - 1 } \int _ { \mathbb { R } ^ { d } } | g ( x + h ) - g ( x ) | \, d x > 0 .$$

Proof It is easy to see that

$$\int _ { \mathbb { R } ^ { d } } ( g ( x - h ) - g ( x ) ) x \, d x = h \int _ { \mathbb { R } ^ { d } } g ( x ) \, d x .$$

Hence it follows that

$$\int _ { \mathbb { R } ^ { d } } | x | \cdot | g ( x - h ) - g ( x ) | \, d x \geq | h | \int _ { \mathbb { R } ^ { d } } g ( x ) \, d x .$$

We can find a number r &gt; 0 such that g(x) = 0, whenever |x| &gt; r. If |h| ≤ 1, then both g(x − h) and g(x) are zero for x satisfying |x{ &gt; r + 1. It follows that for h with |h| ≤ 1 we have

$$| h | \int _ { \mathbb { R } ^ { d } } g ( x ) \, d x \leq ( r + 1 ) \int _ { \mathbb { R } ^ { d } } | g ( x - h ) - g ( x ) | \, d x ,$$

which implies the desired result because ∫Ra g(x) dx &gt; 0.

### 6.3 Equality of the critical densities

The critical densities λ H (g) and λτ (g) defined in Section 6.1 satisfy the obvious inequality λπ(g) ≤ λH(g). It is a very natural question as to whether or not these densities are actually the same. In Chapter 3 we proved that this need not be the case in a Boolean model. The reason for this latter fact is that one ball can give rise to a very large volume. This phenomenon does not occur in random connection models and we can prove the following result:

Theorem 6.2 For every connection function g we have

λ,(g) = λr(g).


<!-- p:168 -->


As far as condition (6.2) is concerned, note that if ∫rRd g(x) dx = ∞, then λH(g) = λT (g) = 0 and in case ∫Rd g(x) dx = 0, then λH(g) = λT (g) = ∞. Note that Theorem 6.2 implies the corresponding statement in Boolean models with fixed-size balls, i.e. in the case where g(x) = I{x|≤r} for some positive r. As in the proof for the Boolean model, the proof which we shall give here uss ol    o      od  sotn the proof of Theorem 6.2, so it pays to take a moment to explain the strategy of the proof.

The first step of the proof is to introduce an extra parameter 0 &lt; γ &lt; 1 in the model, in such a way that the original model can in some sense be viewed as the limit for γ → 0. In the second step, the new model (with the extra parameter γ) is then approximated by a discrete percolation model in a finite box. Here we encounter a difficulty. It is necessary to have a notion of stationarity also in the model in a finite box. This is not automatically the case, because different points have different positions with respect to the boundary of the box. Hence we adapt our model to this end. It is here where we use the map gL defined preant     l ds    ies governing the behaviour of the important quantities in the discrete model in the finite box. The next two steps consist of limit procedures: one to go from the discrete model at finite volume to the continuum model at finite volume, and the other from the continuum model at finite volume to the continuum model on IRd. Finally, we are left with two differential inequalities in the model with ta rt a  t  t t  tt   ad ti tes imply the desired result.

STEP 1: Let us start then with the introduction of the extra parameter γ. Consider a realisation of the point process X. We label each point of X with probability γ, where γ is assumed to be strictly between 0 and 1. The (random) set of labelled points is denoted by G. The idea behind the labelied points is to see them as surrogates for 'the point at infinity'. If we denote by θ(λ, γ) the probability that the component of the origin W contains a labelled point, then by taking γ smaller and smaller, it is likely that W should be larger and larger in order to contain a labelled point. In a similar fashion, x (λ, γ) denotes the expectation of |W  on the event that W does not contain a labelled point: χ(λ, γ) = E(|W} · 1{w∩G=0}). It is in the following sense that the original model is retrieved by taking the limit for γ → 0.

####### Lemma 6.1

- (i) limγ→0 θ(λ, γ) = θ(λ),
- (ii) limγ→0 χ(λ, γ) = E(|W|· 1{W|&lt;∞}).


<!-- p:169 -->


Proof If |W | = ∞, then with probability one W contains at least one labelled point. The labelling is independent of the percolation structure and hence we can write

$$\text {can write} \\ \theta ( \lambda , \gamma ) = 1 - \sum _ { n = 1 } ^ { \infty } P ( W \cap G = \emptyset \, | \, | W | = n ) P ( | W | = n ) \\ = 1 - \sum _ { n = 1 } ^ { \infty } ( 1 - \gamma ) ^ { n } P ( | W | = n ) . \\ \text {This is a power series in } ( 1 - \gamma ) \text { with radius of convergence at least } 1 \text { and } \text { we }$$

This is a power series in (1 – γ) with radius of convergence at least 1, and we can take the limit for γ → 0 to obtain (i). For the second result, we write

$$\text {take the limit for } 0 \leq 0 \leq 6 \text { again} ( 1 ) . \text { For the second result, we write} \\ \chi ( \lambda , \gamma ) = \sum _ { n = 1 } ^ { \infty } n P ( W \cap G = \emptyset \, | \, | W | = n ) \, P ( | W | = n ) \\ = \sum _ { n = 1 } ^ { \infty } n ( 1 - \gamma ) ^ { n } P ( | W | = n ) . \\ \text {Taking the limit for } \gamma \to 0 \text { gives } ( i j )$$

Taking the limit for γ → 0 gives (ii).

0

It is therefore natural to define θ(λ, 0) = θ(λ) and χ (λ, 0) = χ f (λ), where x f (λ) is the expected size of the component of the origin on the event that it is fnite.

STEP 2: We continue with the second part of our programme, the approximation of the model by a discrete percolation model in a finite box. One important feature of this discrete model is that both vertices and edges are randomly chosen to be either open or closed. In order to define the approximating models, we choose two parameters L and n, both integers. Let BL be the box [−L, L]d and divide this box into little boxes of side length 2-". Put a vertex in the middle of each of these boxes. A vertex v is said to be open if the Poisson process has at least one point in the small box containing v; otherwise v is said to be closed. Note that the state of a vertex is independent of the states of all other vertices. Next we consider connections between these vertices. We want to obtain a notion of stationarity at finite volume. In order to achieve this, we use the connection function gL rather than g. Recall that gL is defined as follows:

$$g _ { L } ( x ) = 1 - \prod _ { z \in \mathcal { Z } ^ { d } } ( 1 - g ( x + 2 L z ) ) .$$

Note that gL is translation invariant in the box BL, see Figure 6.1. We connect any two vertices v and v' in BL with probability gL(v' — v), independently of anything else. When v and v' are connected, we say that the edge between them is open; otherwise it is closed. Note that an open edge can have zero, one or two closed end points. Also note that the probability for a vertex to be open depends on the density of the Poisson process, but the probability for an edge to be open is independent of the Poisson process (and hence also independent of λ).


<!-- p:170 -->


Figure 6.1. The bold line square is BL. The probability that a and b are connected with the connection function gz is the probability that b is connected to any of the points a1, a2, . .. when the connection function is g.

It will be convenient to define C¿(v), the component of a vertex v, as the set of all vertices v' in BL for which there exists an alternating sequence (vo = v, e1, v1, e2, v2, . .. , en, vn = v') of vertices and edges such that en connects vn-1 and vn and which are all open, except possibly v itself. According to this definition, v ∈ Cγ(v) whether v is open or not. In this discrete model, we again label each vertex with probability γ, independently of all other vertices. Note that closed vertices may also be labelled. The component of the origin is denoted by Cγ, the set of labelled sites by G^, and the relevant functions are

$$\theta _ { L } ^ { n } ( \lambda , \gamma ) = P ( C _ { L } ^ { n } \cap G _ { L } ^ { n } \neq \emptyset ) ,$$

$$\chi _ { L } ^ { n } ( \lambda , \gamma ) = E ( | C _ { L } ^ { n } | \cdot 1 _ { \{ C _ { L } ^ { n } \cap G _ { L } ^ { n } = \emptyset \} } ) .$$

STEP 3: The third step in the proof is to derive the two differential inequalities.


<!-- p:171 -->


Lemma 6.2 Let M denote the expected number of open edges with one end point at the origin. For λ &gt; 0 and 0 &lt; γ &lt; 1 it is the case that

$$( i ) \ \frac { \partial \theta _ { L } ^ { n } } { \partial \lambda } & \leq 2 ^ { - n d } \theta _ { L } ^ { n } \cdot \chi _ { L } ^ { n } \cdot M _ { L } ^ { n } , \\ ( i i ) \ \theta _ { L } ^ { n } & \leq \gamma \frac { \partial \theta _ { L } ^ { n } } { \partial \gamma } + ( \theta _ { L } ^ { n } ) ^ { 2 } + 2 ^ { n d } ( e ^ { \lambda 2 ^ { - n d } } - 1 ) \theta _ { L } ^ { n } \frac { \partial \theta _ { L } ^ { n } } { \partial \lambda } .$$

$$\frac { \partial \theta _ { L } ^ { n } } { \partial ) } =$$

$$( \mathbf i ) \ \theta _ { L } ^ { n } \leq \gamma \frac { \partial \theta _ { L } ^ { n } } { \partial \gamma } + ( \theta _ { L } ^ { n } ) ^ { 2 } + 2 ^ { n d } ( e ^ { \lambda 2 ^ { - n d } } - 1 ) \theta _ { L } ^ { n } \frac { \partial \theta _ { L } ^ { n } } { \partial \lambda } .$$

Proof For (i), first note that the labelling procedure is independent of everything else and hence, given a set of vertices Γ in BL,

$$P ( C _ { l } ^ { n } \cap \Gamma \neq \emptyset | \, G _ { L } ^ { n } = \Gamma ) = P ( C _ { L } ^ { n } \cap \Gamma \neq \emptyset ) ,$$

$$\theta _ { L } ^ { n } ( \lambda , \gamma ) = \sum _ { \Gamma } P ( G _ { L } ^ { n } = \Gamma ) P ( C _ { L } ^ { n } \cap \Gamma \neq \emptyset ) ,$$

where the sum is over all possible subsets Γ of vertices in BL. But P(Gì = Γ) does not depend on λ and hence, writing A (Γ) for {Cν ∩Γ ≠ Ø} we obtain

$$\frac { \partial \theta _ { L } ^ { n } } { \partial \lambda } = \sum _ { \Gamma } P _ { \lambda } ( G _ { L } ^ { n } = \Gamma ) \frac { d } { d \lambda } P _ { \lambda } ( A _ { L } ^ { n } ( \Gamma ) ) .$$

Next we use Russo's formula Theorem 1.8. The probability for a vertex to be open is equal to 1 – exp(-λ2-nd), while the probability for an edge to be open is independent of λ. Hence we obtain

$$\frac { \partial \theta _ { L } ^ { n } } { \partial \lambda } = 2 ^ { - n d } \sum _ { \Gamma } P ( G _ { L } ^ { n } = \Gamma ) \sum _ { v } P ( v \text { is pivotal for } A _ { L } ^ { n } ( \Gamma ) \text { and closed} ) .$$

(6.14)

Let the closure cl (C¿) of C¿ be the set of vertices and edges consisting of

- (i) all vertices in Cγ,
- (iii) all closed neighbours of Cγ , where two vertices are said to be neighbours if the edge between them is open.
- (ii) all edges (open and closed) with at least one end point in Cì, L

Note that conditioned on {Ci = Σ, cl(Cn) = Σ*}, the configuration of open and closed vertices and edges outside cl(C) is still unconditioned and chosen according to the appropriate product measure. Now let {Ci = Σ, cl(Ci) = Σ*} =: E(Σ, Σ*), where Σ and Σ* are such that 0 ∈ ∑, v ∉ Σ but v ∈ Σ*. Then

$$P ( v \text { is pivotal for } A _ { L } ^ { n } ( \Gamma ) \text { and closed} ) \\ = \sum _ { ( \Sigma , \Sigma ^ { \cdot } ) } P ( ( \Gamma ^ { n } _ { l } \cap \Gamma = \varpi , C _ { l / \Sigma ^ { \cdot } } ^ { n } ( v ) \cap \Gamma \neq \vartheta , E ( \Sigma , \Sigma ^ { * } ) ) ,$$

whence whence where CI/Σ(v) is the cluster of v if we restrict ourselves to the graph where we first delete all vertices (other than v) and edges in Σ* and the sum is over all Σ ⊆ Σ* such that 0 ∈ Σ, v ∉ Σ, v ∈ Σ*. Hence, ∂θγ/∂λ can be written as


<!-- p:172 -->


$$w i s e \colon & \quad \Delta ( \Sigma ^ { L } / \Sigma ^ { ( n ) } ( \Sigma ^ { L } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } / \Sigma ^ { ( n ) } \, \Delta ( \Sigma ^ { n } /$$

Given the event E(Σ, Σ*), the event {CI ∩ Gn = Ø} is independent of the event {CL/Σ*(v) ∩Gi ≠ ∅}. Hence we obtain

$$Given the event E ( \Sigma , E ^ { * } ) , the event \{ C _ { L } ^ { n } \cap G _ { L } ^ { n } = \emptyset \} is independent of the
event \{ C _ { L / \Sigma } ^ { n } ( v ) \cap G _ { L } ^ { n } \neq \emptyset \} . Hence we obtain

\frac { \partial \theta _ { L } ^ { n } } { \partial \lambda } = 2 ^ { - n d } \sum _ { v } \sum _ { ( \Sigma , E ^ { * } ) } P ( C _ { L } ^ { n } \cap G _ { L } ^ { n } = \emptyset | E ( \Sigma , E ^ { * } ) ) P ( E ( \Sigma , E ^ { * } ) ) \\ \times P ( C _ { L / \Sigma } ^ { n } ( v ) \cap G _ { L } ^ { n } \neq \emptyset | E ( \Sigma , E ^ { * } ) ) \\ \leq 2 ^ { - n d } \sum _ { v } \theta _ { L } ^ { n } P ( C _ { L } ^ { n } \cap G _ { L } ^ { n } = \emptyset , v \text { is a closed neighbour of } C _ { L } ^ { n } ) \\ \leq 2 ^ { - n d } \theta _ { L } ^ { n } \sum _ { v } \sum _ { v ^ { \prime } \neq v } P ( C _ { L } ^ { n } \cap G _ { L } ^ { n } = \emptyset , v ^ { \prime } \in C _ { L } ^ { n } , v \text { is closed} ) \\ v \text { is a closed neighbour of } v ^ { \prime } \\ = 2 ^ { - n d } \theta _ { L } ^ { n } \sum _ { v } \sum _ { v ^ { \prime } \neq v } P ( C _ { L } ^ { n } \cap G _ { L } ^ { n } = \emptyset , v ^ { \prime } \in C _ { L } ^ { n } ) \\ \times P ( v \text { is a neighbour of } v ^ { \prime } ) \\ \leq 2 ^ { - n d } \theta _ { L } ^ { n } \sum _ { v } \sum _ { v ^ { \prime } \neq v } P ( C _ { L } ^ { n } \cap G _ { L } ^ { n } = \emptyset , v ^ { \prime } \in C _ { L } ^ { n } ) \\ \times P ( v \text { is a neighbour of } v ^ { \prime } )$$


<!-- p:173 -->


Figure 6.2. Some situations concerning double connectedness. The vertices g and g' are in Cn ∩ Gn . In (i), v is doubly connected to Gn, in (i, 0 is doubly connected and in (iii), v is doubly connected in such a way that one of the paths consists of v only.

$$& = 2 ^ { - n d } \theta _ { L } ^ { n } \sum _ { v ^ { \prime } } P ( C _ { L } ^ { n } \cap G _ { L } ^ { n } = \emptyset , v ^ { \prime } \in C _ { L } ^ { n } ) \\ & \quad \times \sum _ { v \neq v ^ { \prime } } E \left ( 1 _ { \{ v \text { is a neighbour of } v \} } \right ) \\ & = 2 ^ { - n d } \theta _ { L } ^ { n } \cdot \chi _ { L } ^ { n } \cdot M _ { L } ^ { n } . \\ \text {The proof of (ii) is based on the BK-inequality. We write}$$

The proof of (ii) is based on the BK-inequality. We write θ as follows:

$$\theta _ { L } ^ { n } = P ( | C _ { L } ^ { n } \cap G _ { L } ^ { n } | = 1 ) + P ( | C _ { L } ^ { n } \cap G _ { L } ^ { n } | \geq 2 ) .$$

The first term in (6.15) is easily computed:

$$P ( | C _ { L } ^ { n } \cap G _ { L } ^ { n } | = 1 ) = \sum _ { k = 1 } ^ { \infty } k \gamma ( 1 - \gamma ) ^ { k - 1 } P ( | C _ { L } ^ { n } | = k ) = \frac { \gamma } { 1 - \gamma } x _ { L } ^ { n } = \gamma \frac { \partial \theta _ { L } ^ { n } } { \partial \gamma } ,$$

where the last equality is an easy consequence of the definitions. If C¿ ∩Gλ | ≥ 2, then it is not hard to see (but quite hard to prove!) that

- (i) There exist two edge/site disjoint paths (apart from the origin) connecting the origin to two vertices in Gn Gμ. (We say that the origin is doubly connected to G"L.)
- (ii) There exists an open vertex v such that if we close v, Ci ∩ G" becomes empty and v is doubly connected to Gn using no vertices in Cη.

We refrain from proving this assertion and refer to Figure 6.2 instead. Hence the second term in (6.15) can be estimated from above by the sum of the probabilities of these events. The probability of the event in (i) is bounded by (θπ)2 by the BK-inequality. For (ii). we write Av for the event {Cη (v) ∩ Gν ≠ Ø}.


<!-- p:174 -->


Then the probability of this event is bounded from above by

$$\sum _ { v } \frac { P ( v \text { is open} ) } { P ( v \text { is closed} ) } P ( C _ { L } ^ { n } \cap G _ { L } ^ { n } = \emptyset , v \text { is a closed neighbour of } C _ { L } ^ { n } ,$$

$$\sum _ { v } \frac { P ( v \text { is open} ) } { P ( v \text { is closed} ) } \, P ( C _ { L } ^ { n } \cap G _ { L } ^ { n } = \emptyset , v \text { is a closed neighborhood of } C _ { L } ^ { n } , \\ A _ { v } \Box A _ { v } \text { outside } c l ( C _ { L } ^ { n } ) \\ = ( e ^ { \lambda 2 ^ { - n d } } - 1 ) \sum _ { v } \sum _ { ( \Sigma , \Sigma ^ { * } ) } P ( C _ { L } ^ { n } \cap G _ { L } ^ { n } = \emptyset , \\ A _ { v } \Box A _ { v } \text { outside } \Sigma ^ { * } | E ( \Sigma , \Sigma ^ { * } ) ) P ( E ( \Sigma , \Sigma ^ { * } ) ) \\ = ( e ^ { \lambda 2 ^ { - n d } } - 1 ) \sum _ { v } \sum _ { ( \Sigma , \Sigma ^ { * } ) } P ( C _ { L } ^ { n } \cap G _ { L } ^ { n } = \emptyset | E ( \Sigma , \Sigma ^ { * } ) ) \\ \times P ( A _ { v } \Box A _ { v } \text { outside } \Sigma ^ { * } | E ( \Sigma , \Sigma ^ { * } ) ) P ( E ( \Sigma , \Sigma ^ { * } ) ) \\ \leq ( e ^ { \lambda 2 ^ { - n d } } - 1 ) \theta _ { L } ^ { n } \sum _ { v } \sum _ { ( \Sigma , \Sigma ^ { * } ) } P ( A _ { v } , C _ { L } ^ { n } \cap G _ { L } ^ { n } = \emptyset | E ( \Sigma , \Sigma ^ { * } ) ) \\ \times P ( E ( \Sigma , \Sigma ^ { * } ) ) \\ \leq 2 ^ { n d } ( e ^ { \lambda 2 ^ { - n d } } - 1 ) \theta _ { L } ^ { n } \sum P ( G _ { L } ^ { n } = \Gamma ) \\ \times \sum _ { v } P ( v \text { is pivotal for } A _ { L } ^ { n } ( \Gamma ) \text { and closed} ) 2 ^ { - n d } , \\ \text {and it follows from } ( 6 . 1 4 ) \text { that this expression is equal to the desired bound.} \\ \Box$$

and it follows from (6.14) that this expression is equal to the desired bound.

□

STEP 4: The next step in our argument is the limit from the finite discrete model to a continuum model in a finite box. Formally, we have not as yet defined a finite volume RCM, so here are the definitions. The model consists of a Poisson process in the box BL, and any two points of the point process are connected to each other according to the connection function gL rather than g. Each point is again labelled with probability γ. The component containing the origin is denoted by WL and the set of labelled vertices by GL. Of course, we define θL (λ, γ) as the probability that WL∩GL ≠ ∅, and XL (λ, γ) as the expected size of WL on the event that WL ∩ GL = Ø. Here are the required limits:

Lemma 6.3 The function θL (λ, γ) is differentiable with respect to both λ &gt; 0 and γ ∈ (0, 1). Furthermore, we have that

$$\ u n d { \gamma } \in ( 0 , 1 ) . \, 1 \, u n d { m } o n e , \\ ( 1 ) \, \lim _ { n \to \infty } \theta _ { L } ^ { n } = \theta _ { L } , \\ ( 2 ) \, \lim _ { n \to \infty } \frac { \partial \theta _ { L } ^ { n } } { \partial \gamma } = \frac { \partial \theta _ { L } } { \partial \gamma } ,$$


<!-- p:175 -->


- ∂θn ∂θl

$$( 3 ) \, \lim _ { n \to \infty } \frac { \partial \theta _ { L } ^ { n } } { \partial \lambda } & = \frac { \partial \theta _ { L } } { \partial \lambda } , \\ ( 4 ) \, \lim _ { n \to \infty } 2 ^ { - n d } M _ { L } ^ { n } & = \int _ { B _ { L } } g _ { L } ( x ) \, d x .$$

Proof For (1), we write

$$1 - \theta _ { L } ^ { n } = \sum _ { k = 1 } ^ { \infty } ( 1 - \gamma ) ^ { k } P ( | C _ { L } ^ { n } | = k ) ,$$

$$1 - \theta _ { L } = \sum _ { k = 1 } ^ { \infty } ( 1 - \gamma ) ^ { k } P ( | W _ { L } | = k ) .$$

It suffices to prove that P(|Ci| = k) → P(|CL| = k), for all k. The probability that there are two points x and y of the point process X for which x – y is a point of discontinuity of gz is zero, by Proposition 6.1. Hence it follows that

$$P ( | C _ { L } ^ { n } | = k | \, X ( B _ { L } ) = l ) \to P ( | C _ { L } | = k | \, X ( B _ { L } ) = l ) ,$$

for all l, which proves (1). From (6.16) and (6.17) we also get that

$$\frac { \partial \theta _ { L } ^ { n } } { \partial \gamma } = \sum _ { k = 1 } ^ { \infty } k ( 1 - \gamma ) ^ { k - 1 } P ( | C _ { L } ^ { n } | = k ) ,$$

$$\frac { \partial \theta _ { L } } { \partial \gamma } = \sum _ { k = 1 } ^ { \infty } k ( 1 - \gamma ) ^ { k - 1 } P ( | C _ { L } | = k ) ,$$

and and

Hence, also (2) follows from the previous argument. (Note that the differentia-

bility of θL with respect to γ is no problem as it is a power series in (1 - γ).) Next, we want to show that θL can be differentiated with respect to λ. The right-hand side of (6.16) is just a finite sum because there are only finitely many vertices in B¿. Hence the derivative of the right-hand side of (6.16) is just the sum of the term-by-term derivatives. Therefore, to show that θL is differentiable with respect to λ, together with (3), it suffices to prove that ← o   n   ( =  d (/  ,( - ) ∞. For this, we again use Russo's formula. The event {|Ci| = k} is not increasing, but it can be written as the difference of two increasing events: P(|CL| = k) = P(|C | ≥ k) − P(|CL| ≥ k + 1). We first compute, according to Russo's formula:

$$\frac { d } { d \lambda } \, P ( | C _ { L } ^ { n } | \geq k ) \, = \, 2 \, \ ^ { n d } \exp ( - \lambda 2 ^ { - n d } ) \\$$

× E(number of pivotal vertices for {|Ci| ≥ k}).

and and Let us now pause for a moment to realise what we are trying to do. We are approximating the continuum model by a discrete model. In a continuum model, we can define pivotal points in the obvious way, but the notion of closed pivotal points does not make sense. Hence we are interested in open pivotal vertices in the discrete model. The state of a vertex is independent of its pivotality and we can write


<!-- p:176 -->


$$\text { can write} & & \frac { d } { d \lambda } P ( | C _ { L } ^ { n } | \geq k ) = \frac { 2 ^ { - n d } \exp ( - \lambda 2 ^ { - n d } ) } { 1 - \exp ( - \lambda 2 ^ { - n d } ) } \\ & & \times \sum _ { l = 0 } ^ { \infty } E ( \text {number of open pivotals vertices for} \\ & & \{ | C _ { l } ^ { n } | > k ) \ | \ X ( R _ { l } ) - l ) P ( X ( R _ { l } ) - l )$$

$$\{ | C _ { L } ^ { n } | \geq k \} \, | \, X ( B _ { L } ) = l ) P ( X ( B _ { L } ) = l ) .$$

Now we use Proposition 1.2 to conclude that the expected number of open pivotal vertices for {{Ci| ≥ k} given {X(BL) = I} is independent of λ, and, because there are only l points in BL, trivially bounded from above by l. This quantity is denoted by f¿(k, l, n). Using once more the almost everywhere continuity of gL (Proposition 6.1), it is obvious that lim→∞ fL (k, l, n) exists and is equal to the corresponding quantity in the continuous model. Finally, we can now write

$$\text { can now write} \\ \lim _ { n \to \infty } \sum _ { k = 1 } ^ { \infty } ( 1 - \gamma ) ^ { k } \frac { d } { d \lambda } \, P ( | C _ { L } ^ { n } | ) & = k ) \\ & = \lim _ { n \to \infty } \exp ( - \lambda | B _ { L } | ) \frac { 2 ^ { - n d } } { 1 - \exp ( - \lambda 2 ^ { - n d } ) } \\ & \times \sum _ { k = 1 } ^ { \infty } ( 1 - \gamma ) ^ { k } \sum _ { l = 0 } ^ { \infty } ( f _ { L } ( k , l , n ) - f _ { L } ( k + 1 , l , n ) ) \frac { ( \ell ( B _ { L } ) \lambda ) ^ { l } } { l ! } . \\ \text {Using the convergence of } f _ { L } ( k , l , n ) \text { and the fact that } f _ { L } ( k , l , n ) \text { is bounded}$$

Using the convergence of fL (k, l, n) and the fact that fL (k, l, n) is bounded from above by l, for all k and n, this expression is easily seen to converge locally uniformly in λ, for n → ∞.

It remains to prove (4). This is easy though, as we can write

$$2 ^ { - n d } M _ { L } ^ { n } = 2 ^ { - n d } \sum _ { v } g _ { L } ( v ) , \\$$

where the sum is over all non-zero vertices in the box BL in the n-th approximating lattice model. But the right-hand side of (6.18) is just a Riemann sum which converges to ∫BL gL(x) dx.

STEP 5: In this step, we take the so-called infinite volume limit, which means that we let L tend to infinity.


<!-- p:177 -->


Lemma 6.4 For λ &gt; 0 and γ ∈ (0, 1), it is the case that

- (1) lim θL = θ, ∞←7
2. 70e θe (2) \_lim L→∞∂γ ∂γ

Proof It suffices to prove that

$$\lim _ { L \to \infty } P ( | W _ { L } | = k ) = P ( | W | = k ) .$$

First, we decompose the event {|W| = k} into {|W| = k, W ⊂ Bn} ∪ {|W| = k, W  Bn }, and similarly for WL, where L &gt; n. From Proposition 6.2 (and its proof) we easily deduce that

$$\beta ( W _ { L } ) \, & \, w ( C \, \text {carry} \, \tt a r t ) \\ P ( | W _ { L } | = k , W _ { L } \subset B _ { n } ) = \frac { \lambda ^ { k - 1 } } { ( k - 1 ) ! } \int _ { B _ { n } \times \cdots \times B _ { n } } g L , 2 ( 0 , x _ { 1 } , \dots , x _ { k - 1 } ) \\ & \times e ^ { - \lambda \int _ { B _ { L } } g L _ { L } , ( y ; 0 , x _ { 1 } , \dots , x _ { k - 1 } ) \, d y } d ( x _ { 1 } , \dots , x _ { k - 1 } ) ,$$

where gL,1 and gL,2 are the analogues of g1 and g2 for the connection function gL. As a consequence of Proposition 6.1, for (x1, . . . , xk-1) ∈ Bn × · .. × Bn, it is the case that

$$g _ { L , 2 } ( 0 , x _ { 1 } , \dots , x _ { k - 1 } ) \to g _ { 2 } ( 0 , x _ { 1 } , \dots , x _ { k - 1 } ) ,$$

as L → ∞. Furthermore, for fixed y and x1, ..., xk, it follows that 1 B (y) . gL,1(y; 0, x1, . . . , xk−1) → g1(y; 0, x1, ... , xk−1), for L → ∞. In order to use dominated convergence for the integrals in the exponents of (6.8) and (6.20), we write

$$g _ { L , 1 } ( y ; 0 , x _ { 1 } , \dots , x _ { k - 1 } ) \leq \sum _ { i = 0 } ^ { k - 1 } g _ { L } ( y - x _ { i } ) ,$$

where xo is just the origin. Furthermore,

$$w \text {here } x _ { 0 } \text { is just the origin. Furthermore,} \\ \int _ { B _ { L } } \sum _ { i = 0 } ^ { k - 1 } g _ { L } ( y - x _ { i } ) \, d y & \leq \sum _ { i = 0 } ^ { k - 1 } \sum _ { z \in Z ^ { d } } \int _ { B _ { L } } g ( y - x _ { i } + 2 L z ) \, d y \\ & = \sum _ { i = 0 } ^ { k - 1 } \int _ { \mathbb { R } ^ { d } } g ( y - x _ { i } ) \, d y < \infty , \\ \intertext { c o n d i p g } \text { according to (6.2) From this it follows that (6.20) converges to (6.8) for } L \to$$

according to (6.2). From this it follows that (6.20) converges to (6.8) for L → ∞. Finally, we show that P(Wl.| = k, WL  Bn) can be made arbitrarily small uniformly for all l. large enough, by taking n fixed but large enough. For 0) &lt; N &lt; M &lt; l, let E1 (N. M) be the cvent that in the finite volume model in BL there is at least one direct connection from a point inside BN to a point outside Bm. For any non-negative integer-valued random variable Y we have P(Y ≥ 1) ≤ EY, and this implies here that


<!-- p:178 -->


$$P ( E _ { L } ( N , M ) ) & \leq \lambda ^ { 2 } \int _ { B _ { N } } \int _ { B _ { L } \, \rangle B _ { M } } g _ { L } ( y - x ) \, d y \, d x \\ & \leq \lambda ^ { 2 } \int _ { B _ { N } } \int _ { I R ^ { d } \, \rangle B _ { M } } g ( y - x ) \, d y \, d x ,$$

where the last inequality follows from arguments as in the proof of (1). Note that this estimate is uniform in L and hence P(EL(N, M)) is small uniformly in L for M large.

Next let € &gt; 0 and take boxes Bn, C ..· C Bn-1 such that the following events A1, . .., Ak–1 all have probability at most €, uniformly in L:

A1 = {the origin is connected to a point outside Bn1 },

Al = {there is a point inside Bn\_1 connected to a point outside Bn },

for l = 2, ... , k − 1. Now take n = nk−1. If {|WL| = k, WL  Bn} occurs then there is a point outside B connected to the origin in less than k steps. This means that Uk=1 A1 must occur. However, this has probability at most (k – 1)€e for all L and this proves the lemma.

STEP 6: Finally we are able to prove the desired result. The reader should note that from now on the argument is completely analytic. Let λo &lt; λ and suppose that x (λ0) = ∞. We write fL(γ) = θL(λ0, γ) and f(γ) = θ(λ0, γ). If we first combine the two conclusions in Lemma 6.2 and then take the limit for n → ∞ (Lemma 6.3) we obtain

$$f _ { L } \leq \gamma \frac { d f _ { L } } { d \gamma } + ( f _ { L } ) ^ { 2 } + ( 1 - \gamma ) \left ( \int _ { B _ { L } } g _ { L } ( x ) \, d x \right ) \lambda _ { 0 } ( f _ { L } ) ^ { 2 } \frac { d f _ { L } } { d \gamma } .$$

From Lemma 6.4 and Proposition 6.1 we then find, taking the limit for L → ∞,

$$f & \leq \gamma \frac { d f } { d \gamma } + f ^ { 2 } + ( 1 - \gamma ) \left ( \int _ { \mathbb { R } ^ { d } } g ( x ) \, d x \right ) \lambda _ { 0 } \, f ^ { 2 } \frac { d f } { d \gamma } . \\$$

We have f(γ) → 0 for γ → 0, because of Lemma 6.1(i) and the fact that λ0 &lt; λH. Also,

$$\frac { f ( \gamma ) } { \gamma } \rightarrow \infty$$

for γ → 0, where we use Lemma 6.1 again, the mean value theorem and the fact that x(λo) = ∞. Now let h be the inverse function of f and substitute y = f(γ) a and in (6.21) to obtain


<!-- p:179 -->


$$\left ( \frac { d h } { d y } \right ) = \left ( \frac { d f } { d \gamma } \right ) ^ { - 1 }$$

$$\frac { 1 } { y } \frac { d h } { d y } - \frac { 1 } { y ^ { 2 } } h & \leq C ( 1 - h ) + \frac { d h } { d y } , \\$$

where C is a constant depending on λo. Using (6.22) we see that dh/dy is bounded on an interval (0, b) for some b &gt; 0 and hence there is a positive constant β such that

$$\frac { 1 } { y } \frac { d h } { d y } - \frac { 1 } { y ^ { 2 } } h \leq \beta$$

for 0 &lt; y &lt; b. Integrating this expression from 0 to x with x ≤ b yields

$$\left [ \frac { 1 } { y } h ( y ) \right ] _ { 0 } ^ { x } \leq \beta x$$

and it follows from this and the fact that h(y)/y → 0 when y → 0 (use (6.21)) that for small enough γ,

$$f ( \gamma ) \geq C ^ { \prime } \gamma ^ { \frac { 1 } { 2 } } ,$$

where C' is a positive constant depending on λo.

We let n → ∞ in Lemma 6.2 and obtain, using Lemma 6.3,

$$\theta _ { L } \leq \gamma \, \frac { \partial \theta _ { L } } { \partial \gamma } + ( \theta _ { L } ) ^ { 2 } + \lambda \theta _ { L } \frac { \partial \theta _ { L } } { \partial \lambda } . \\$$

Rewrite this inequality as

$$0 \leq ( \theta _ { L } ) ^ { - 1 } \frac { \partial \theta _ { L } } { \partial \gamma } + \gamma ^ { - 1 } \frac { \partial } { \partial \lambda } ( \lambda \theta _ { L } - \lambda ) , \\$$

which can be integrated over [e, 8] × [λ0, λ1] (where λ &lt; λH) to obtain

$$0 \leq ( \lambda _ { 1 } - \lambda _ { 0 } ) \log \left ( \frac { \theta _ { L } ( \lambda _ { 1 } , \delta ) } { \theta _ { L } ( \lambda _ { 0 } , \epsilon ) } \right ) + ( \lambda _ { 1 } \theta _ { L } ( \lambda _ { 1 } , \delta ) - \lambda _ { 1 } + \lambda _ { 0 } ) \log \left ( \frac { \delta } { \epsilon } \right ) .$$

Now we use Lemma 6.4 and take the limit for L → ∞, which means that we cr     (    o  us   ro and use (6.23) to find

$$0 \leq \frac { 1 } { 2 } ( \lambda _ { 1 } - \lambda _ { 0 } ) + \lambda _ { 1 } \theta ( \lambda _ { 1 } , \delta ) - \lambda _ { 1 } + \lambda _ { 0 } .$$

If we take the limit for δ → 0 here, it follows that θ(λ1) = θ(λ1, 0) &gt; 0, which is the desired contradiction because λ &lt; λ. □


<!-- p:180 -->


### 6.4 Uniqueness

In view of the uniqueness results in Boolean models, we may expect the unbounded component in the Poisson RCM to be unique. This is indeed the case:

Theorem 6.3 In a Poisson RCM (X, g, λ), there is at most one unbounded component a.s.

The proof of this result is not very different from the corresponding proof in the Boolean model. It is again the ergodicity of the model which guarantees that the number of unbounded components is an a.s. constant. As before, we first show that this number cannot be any finite number apart from zero or one:

Lemma 6.5 The number of unbounded components in a Poisson RCM is equal a.s. to either zero, one or infinity.

Proof To derive a contradiction, let us suppose that this number is a.s. equal to K ≥ 2. This means that there is a box B such that there is a positive probability that Bn intersects all of them. Choose M ≤ ∞ so that g(x) = 0 whenever |x| &gt; M, noting that M can take the value infinity. Next we partition Bn into at least K cubic cells Gj in such a way that for two neighbouring cells G1 and G2 we have d(x, y) ≤ M for all x ∈ G1 and y ∈ G2. For any subset A ⊂ Rd, we write (XA, g, λ) for the RCM obtained by removing all Poisson points outside A and all connections leading to such points. By taking smaller cells if necessary and a possible renumbering of the cells, we can find K cells G1, . . . , G κ such that the following event has positive probability, writing

E := {(XG∪(B)c, g, λ) contains exactly K unbounded components C1, ..., Cκ such that C has exactly one Poisson point x in G, for i = 1, .. . , K}.

Obviously, the following event F also has positive probability:

F := {each of the cells Gj in Bn outside G contains exactly one Poisson point xj}.

Now observe that E and F are independent, because they depend on disjoint regions in space. Hence,

P(E∩ F) = P(E)P(F) &gt; 0.


<!-- p:181 -->


But given the event E ∩ F, we can, with positive probability, connect the points x and x j if the cells G and G j share a face, i.e. if they are neighbours, because of the choice of the cell size. However, after doing that, the resulting configuration contains only one unbounded component and this is the desired contradiction. Note that in case M = ∞, there is no need to consider the event F at all. In that case we can directly connect all points x1, . . . , xK.

Proof of Theorem 6.3 It remains to rule out the case of infinitely many unbounded components. This, however, can be done in exactly the same way as in the proof of Theorem 3.6. As such, we do not repeat the argument here.

In Chapter 7 we shall discuss a uniqueness result for random-connection models driven by general stationary point processes.

### 6.5 High density

One of the features of continuum percolation models which they do not share with discrete percolation models is the possibility to consider the model at arbitrary high density. When the density λ of the underlying point process tends to infinity, one expects several things to happen. In the first place, larger λ implies that there are on the average more points per unit volume, so it must be easier for the origin to be contained in an infinite component. This should imply that

$$\lim _ { \lambda \to \infty } \theta _ { g } ( \lambda ) = 1 .$$

In fact, a proof of (6.25) is not hard. We shall, however, prove a much stronger result below. In addition to the probability of the origin being in an infinite component, one can consider the distribution of finite components. It seems reasonable to guess that the probability for a point to be isolated (i.e. not connetr  ss  s     d r   gess to 1 for λ - ∞. In other words, 'most' finite components should consist of only one point. We shall prove the following theorem:

Theorem 6.4 Suppose g satisfies (6.2). Then we have

$$\lim _ { \lambda \to \infty } \frac { - \log ( 1 - \theta _ { g } ( \lambda ) ) } { \lambda \int _ { \mathbb { R } ^ { d } } g ( x ) \, d x } = 1 .$$

Before giving the proof of this result, let us spend a few words on it. In fact, the assertion of the theorem implies that 1 − θg(λ) ∼ exp(−λ ∫Rd g(x) dx), which is equal to the probability that the origin is isolated. So not only does Theorem 6.4 imply (6.25), it also asserts that the rate at which θ(λ) = θg(λ) tends to 1 corresponds to the rate at which the probability of being isolated tends to zero. The proof of Theorem 6.4 is based on the following lemma.


<!-- p:182 -->


Lemma 6.6 Suppose that g has bounded support. Then we have

$$\lim _ { \lambda \to \infty } \frac { ( 1 - \theta _ { g } ( \lambda ) ) } { P _ { \lambda } ( | W | = 1 ) } = 1 .$$

Before giving the proof of Lemma 6.6, we demonstrate how Theorem 6.4 follows from it. Let g satisfy (6.2), and let gr(x) := g(x)1{|x|≤r). A simple coupling argument shows that

$$1 - \theta _ { g } ( \lambda ) \leq 1 - \theta _ { g _ { r } } ( \lambda ) .$$

From the fact that 1 − θg(λ) ≥ P(λ,g)(|W| = 1) and Lemma 6.6 we thus find

$$From the fact that 1 - \theta _ { g } ( \lambda ) \geq P _ { \lambda , g } ( | W | = 1 ) \, \text {and} \, \text {Lemma} \, 6 . \, 6 \, \text {we thus find} \\ 1 \, \leq \, \liminf _ { \lambda \to \infty } \left ( \frac { 1 - \theta _ { g } ( \lambda ) } { P _ { \lambda , g } ( | W | = 1 ) } \right ) ^ { 1 / \lambda } \, \leq \, \lim \sup _ { \lambda \to \infty } \left ( \frac { 1 - \theta _ { g } ( \lambda ) } { P _ { ( \lambda , g ) } ( | W | = 1 ) } \right ) ^ { 1 / \lambda } \\ \leq \, \lim \sup _ { \lambda \to \infty } \left ( \frac { 1 - \theta _ { g } ( \lambda ) } { P _ { ( \lambda , g ) } ( | W | = 1 ) } \right ) ^ { 1 / \lambda } \\ = \lim \sup _ { \lambda \to \infty } \left ( \frac { 1 - \theta _ { g } ( \lambda ) } { P _ { ( \lambda , g ) } ( | W | = 1 ) } \cdot \frac { P _ { ( \lambda , g ) } ( | W | = 1 ) } { P _ { ( \lambda , g ) } ( | W | = 1 ) } \right ) ^ { 1 / \lambda } \\ = \lim \sup _ { \lambda \to \infty } \left ( \frac { \exp ( - \lambda \int _ { | x | \leq r } g ( x ) \, d x ) } { \exp ( - \lambda \int _ { \mathbb { R } ^ { d } } g ( x ) \, d x ) } \right ) ^ { 1 / \lambda } = e ^ { \int _ { | x | > r } g ( x ) \, d x } . \\ \text {Letting} \, r \to \, \infty , \, \text {we obtain}$$

Letting r → ∞, we obtain

$$\lim _ { \lambda \to \infty } \left ( \frac { 1 - \theta _ { g } ( \lambda ) } { P _ { \lambda } ( | W | = 1 ) } \right ) ^ { 1 / \lambda } = 1 .$$

Taking logarithms completes the proof of Theorem 6.4. It remains therefore to prove Lemma 6.6. We write qk(λ) for Pλ (|W| = k). In this notation we need to show that

$$\lim _ { \lambda \to \infty } \frac { 1 } { q _ { 1 } ( \lambda ) } \sum _ { k = 1 } ^ { \infty } q _ { k } ( \lambda ) = 1 ,$$

$$\lim _ { \lambda \to \infty } \frac { 1 } { q _ { 1 } ( \lambda ) } \sum _ { k = 2 } ^ { \infty } q _ { k } ( \lambda ) = 0 .$$

or or We partition the event that |W | = k as follows. Let δ &gt; 0 and let (8Z)d be the lattice of points of the form δz for z ∈ Zd. We denote by F8 : IRd  8Zd the map which sends each point of IRd to the closest point of (8Z)d . This map is well defined for almost all points in IRd. In particular, the image S = S8 = F8(W) is well defined with probability 1. We may now write


<!-- p:183 -->


$$\frac { 1 } { q _ { 1 } ( \lambda ) } \sum _ { k = 2 } ^ { \infty } q _ { k } ( \lambda ) = \frac { 1 } { q _ { 1 } ( \lambda ) } \, \sum _ { m = 1 } ^ { \infty } \sum _ { k = 2 } ^ { \infty } P _ { \lambda } ( | W | = k , | S _ { \delta } | = m ) .$$

It therefore suffices to prove the three following propositions:

Proposition 6.4 Suppose g has bounded support. For δ &gt; 0 sufficiently small we have

$$\lim _ { \lambda \to \infty } \frac { 1 } { q _ { 1 } ( \lambda ) } \sum _ { k = 2 } ^ { \infty } P _ { \lambda } ( | W | = k , | S _ { \delta } | = 1 ) = 0 .$$

Proposition 6.5 Suppose g has bounded support. For δ &gt; 0 sufficiently small, there exists an mo such that

$$\lim _ { \lambda \to \infty } \frac { 1 } { q _ { 1 } ( \lambda ) } \sum _ { m = m _ { 0 } } ^ { \infty } \sum _ { k = 2 } ^ { \infty } P _ { \lambda } ( | W | = k , | S _ { \delta } | = m ) = 0 .$$

Proposition 6.6 Suppose g has bounded support. For δ &gt; 0 sufficiently small we have for each fixed m,

$$\lim _ { \lambda \to \infty } \frac { 1 } { q _ { 1 } ( \lambda ) } \sum _ { k = 2 } ^ { \infty } P _ { \lambda } ( | W | = k , | S _ { \delta } | = m ) = 0 .$$

Of course, Proposition 6.6 is stronger than Proposition 6.4, but the latter will be used in the proof of the former.

Proof of Proposition 6.4 We define qk(λ) = Pλ(|Ss| = 1, |W| = k). When no confusion can arise, we drop sub- and superscripts. When |W | = 1, |S| can be 1 only if all points of W are concentrated in B8/2. Hence from Proposition 6.2 we find

$$w \text { find } & & \frac { \lambda ^ { k - 1 } } { ( k _ { 1 } ^ { \lambda } ) } \int _ { B _ { \delta / 2 } } \cdots \int _ { B _ { \delta / 2 } } e ^ { - \lambda } \int _ { \mathbb { R } ^ { d } } g _ { 1 } ( y ; 0 , x _ { 1 } , \dots , x _ { k - 1 } ) \, d y \\ & & = \frac { ( k _ { 1 } ^ { \lambda } ) } { ( k _ { 1 } ^ { \lambda } ) } = \frac { ( k - 1 ) ! } { \exp ( - \lambda \int _ { \mathbb { R } ^ { d } } g ( y ) \, d y ) } \\ & & = \frac { \lambda ^ { k - 1 } } { ( k - 1 ) ! } \int _ { B _ { \lambda } } \cdots \int _ { B _ { \lambda / 2 } } \exp \left ( - \lambda \int _ { \mathbb { R } ^ { d } } ( g _ { 1 } ( y ; 0 , x _ { 1 } , \dots , x _ { k - 1 } ) ) \\ & & - g ( y , y ) \, d y \, d \lambda _ { 1 } \cdots d x _ { k } \ | .$$


<!-- p:184 -->


From the definition of g1 and g, g1 (y; 0, x1, . . . , xk–1) − g(y) equals the probability that if we take a graph with non-random vertices 0, x1, . .. , xk–1 and y, the vertex y is not isolated but not connected directly to 0 (all with connection function g of course). This expression is therefore bounded from below, for all i, by g(y−xi)(1−g(y)) = g(y−xi)-g(y)g(y- xi) ≥ (g(y− xi)- g(y))+, where f+ = max{ f, 0} denotes the positive part of the function f. It follows from Proposition 6.3 that

$$\int _ { \mathbb { R } ^ { d } } ( g ( y - x _ { i } ) - g ( y ) ) ^ { + } d y & = \frac { 1 } { 2 } \int _ { \mathbb { R } ^ { d } } | g ( y - x _ { i } ) - g ( y ) | d y \\ & \geq c _ { i } | x _ { i } | \text { for all } x _ { i } \in B _ { \delta / 2 } ,$$

for a suitable positive constant c. We thus find, writing ⊂ (IRd)k-1 for 8/2 the set {x1, ..., xk−1 ∈ (B8/2)k−1 : |x| ≥ maxj≠i |xj|},

$$e \, \det \left \{ x _ { 1 } , \dots , x _ { k - 1 } \in ( B _ { \delta / 2 } ) ^ { k - 1 } \colon | x _ { i } | \geq \max _ { j \neq i } | x _ { j } | \right \} , \\ \frac { q _ { k } ^ { \delta } ( \lambda ) } { q _ { 1 } ( \lambda ) } \leq \sum _ { i = 1 } ^ { k - 1 } \frac { \lambda ^ { k - 1 } } { ( k - 1 ) ! } \int _ { B _ { / 2 } ^ { i } } e ^ { - \lambda c _ { 1 } | x _ { i } | } d ( x _ { 1 } , \dots , x _ { k - 1 } ) \\ = \frac { \lambda ^ { k - 1 } } { ( k - 2 ) ! } \int _ { B _ { \delta / 2 } ^ { 1 } } e ^ { - \lambda c _ { 1 } | x _ { 1 } | } d ( x _ { 1 } , \dots , x _ { k - 1 } ) \\ = \frac { \lambda ^ { k - 1 } } { ( k - 2 ) ! } \int _ { B _ { \delta / 2 } } ( \pi _ { d } | x _ { 1 } | ^ { d } ) ^ { k - 2 } e ^ { - \lambda c _ { 1 } | x _ { 1 } | } d x _ { 1 } , \\ \intertext { e r $ n $ t h e v o u m e $ o f $ t h e v o u m e $ t h e v o u m e $ }$$

where πd is the volume of the unit ball in Rd. Note that the integrand is a function of |xı | and we can change variables to obtain

$$\frac { q _ { k } ^ { \delta } ( \lambda ) } { q _ { 1 } ( \lambda ) } & \leq c _ { 2 } \int _ { 0 } ^ { \delta / ( 2 \sqrt { d } ) } \frac { \lambda ^ { k - 1 } } { ( k - 2 ) ! } e ^ { - \lambda c _ { 1 } r } r ^ { d ( k - 1 ) - 1 } \pi _ { d } ^ { k - 2 } d r \\$$

for a positive constant c2. Thus,

$$\text { for a positive constant } c _ { 2 } . 1 & \text { thus,} \\ \sum _ { k = 2 } ^ { \infty } \frac { q _ { k } ^ { \delta } ( \lambda ) } { q _ { 1 } ( \lambda ) } & \leq c _ { 2 } \lambda \int _ { 0 } ^ { \delta / ( 2 \sqrt { d } ) } e ^ { - \lambda c _ { 1 } r } r ^ { d - 1 } \sum _ { k = 2 } ^ { \infty } \frac { ( \lambda \pi _ { d } ) ^ { k - 2 } } { ( k - 2 ) ! } ( r ^ { d } ) ^ { k - 2 } d r \\ & = c _ { 2 } \lambda \int _ { 0 } ^ { \delta / ( 2 \sqrt { d } ) } r ^ { d - 1 } e ^ { \lambda \pi _ { d } r ^ { d - \lambda c _ { 1 } r } d r } .$$

We can take δ so small that for all r ≤ δ/(2√ã) we have πdrd ≤ c1r and 2 thus the right-hand side of (6.28) is bounded from above by

$$c _ { 2 } \lambda \int _ { 0 } ^ { \delta / ( 2 \sqrt { d } ) } e ^ { - \lambda c _ { 1 } r / 2 } r ^ { d - 1 } d r & \leq c _ { 2 } ( \lambda ) ^ { - ( d - 1 ) } \int _ { 0 } ^ { \infty } e ^ { - c _ { 1 } s / 2 } s ^ { d - 1 } d s .$$

The result follows immediately from this.

口


<!-- p:185 -->


Proof of Proposition 6.5 We give the proof for the two-dimensional case. It will be clear that a similar proof works in any dimension, but the details become very lengthy to write down. We start by choosing R and δ such that

- (i) g(x) = 0 for all x with |x| ≥ R,
- (ii) δ &lt;  R,
- (iii) g(2 R + 38) ≥ δ.

Consider the component W of the origin. If we place a ball S(x, ↓R) with radius  R around each point x of W, then, using (i) above, the set Fw := ∪x∈w S(x,  R) is a connected set. Denote by Fw the union of all squares of the form [δn, δ(n + 1)] × [δm,δ(m + 1)] which intersect Fw, where n and m are integers. Then Fw is a bounded set whenever |W| &lt; ∞. We denote by ∂ Fw the exterior boundary of Fw. The boundary γ = ∂ Fw consists of a number of edges of length δ, and the number of such edges is denoted by lyl. We want to estimate the probability that ∂ Fw is a particular curve γ. For such a curve γ, let γ8 be the set of points in the plane which are at a distance at most δ from γ. We denote by int (γ8) the set of points which are in the interior of γ but not in γ8. Suppose now that ∂Fw = γ. We claim that W ∩ γ8 = ∅ a.s. To see this, suppose that there is a point x ∈ W, and a point y ∈ γ such that |x - y| ≤ δ. With probability 1, each point in ∂Fw is not in Fw and hence y ∉ w a.s. But because of (ii), this is impossible and the claim follows.

Let Wy be the component of the origin obtained from points in int (γ8) and all edges between these points. We define the event Ek.γ := {Wγ| = k, ∂ Fw, = γ}, and the event that there is no direct edge between any point in γ8 and Wy is denoted by Ek,y. Using Proposition 1.3 we have

$$P ( E _ { k , \gamma } ^ { \prime } \left | \, E _ { k , \gamma } \right ) = \exp \left ( - \lambda \int _ { \mathcal { N } } g _ { 1 } ( y ; W _ { \gamma } ) \, d y \right ) .$$

Let y be in γ8. If Ek,y occurs, then each point on the boundary γ of Fw, must be closer than 2δ to a point of w, . Hence each point of γ8 must be closer than 38 to wy . Thus, each y ∈ γ8 must be closer than 3δ +  R to a point in Wγ and it follows from (iii) that g1 (y; Wγ) ≥ δ. Also, the volume of γ8 can be estimated using the observation that each edge of γ has a square of side length δ centered at the midpoint of the edge and which are disjoint for different edges. Thus, the Lebesgue measure l(γs) is at least {γ{δ2/4. We now obtain from (6.29):

$$P ( E _ { k , \gamma } ^ { \prime } | E _ { k , \gamma } ) \leq \exp ( - \lambda | \gamma | \delta ^ { 3 } / 4 ) .$$


<!-- p:186 -->


It follows that

$$\sum _ { k = 1 } ^ { \infty } P ( | W | = k , \partial F _ { W } = \gamma ) & \leq \exp ( - \lambda | \gamma | \delta ^ { 3 } / 4 ) \sum _ { k = 1 } ^ { \infty } P ( E _ { k , \gamma } ) \\ & \leq \exp ( - \lambda | \gamma | \delta ^ { 3 } / 4 ) .$$

The rest of the argument consists of classical counting arguments. We need two facts here: the area enclosed by a curve γ, which in our case is piecewise linear, is at most some constant c1 (independent of γ) times |γ2, and the number of closed curves γ with |γ| = m along edges of the square lattice and which encloses the origin is at most c7 for some positive constant c2; see the proof of Theorem 1.1. We may now write

$$\text {Theorem 1.1. We may now write} \\ \sum _ { k = 1 } ^ { \infty } P ( | W | = k , | S | \geq m _ { 0 } ) & \, \leq \sum _ { k = 1 } ^ { \infty } P ( | W | = k , | \gamma | \geq c _ { 1 } m _ { 0 } ^ { 1 / 2 } ) \\ & = \sum _ { m \geq c _ { 1 } m _ { 0 } ^ { 1 / 2 } } \sum _ { k = 1 } ^ { \infty } P ( | W | = k , | \gamma | = m ) \\ & = \sum _ { m \geq c _ { 1 } m _ { 0 } ^ { 1 / 2 } } \sum _ { k = 1 } ^ { \infty } \sum _ { \gamma \colon | \gamma | = m } P ( | W | = k , \partial F _ { C } = \gamma ) \\ & \leq \sum _ { m \geq c _ { 1 } m _ { 0 } ^ { 1 / 2 } } \exp ( - \lambda m \delta ^ { 3 } / 4 ) c _ { 2 } ^ { m } , \\ \intertext { using ( 6 . 3 ) . Now using the fact that }$$

using (6.30). Now using the fact that

$$= \exp ( - c _ { 3 } \lambda ) , \, \text { say}$$

$$\frac { 1 } { q _ { 1 } ( \lambda ) } \sum _ { m = m _ { 0 } } ^ { \infty } \sum _ { k = 1 } ^ { \infty } P ( | W | = k , | S | \geq m _ { 0 } ) \\ \leq \sum _ { m \geq c _ { 1 } m _ { 0 } ^ { 1 / 2 } } e ^ { c _ { 3 } \lambda } ( c _ { 2 } e ^ { - \lambda \delta ^ { 3 } / 4 } ) ^ { m } \\ \leq e ^ { c _ { 3 } \lambda } \frac { ( c _ { 2 } \exp ( - \lambda \delta ^ { 3 } / 4 ) ) ^ { c _ { 1 } m _ { 0 } ^ { 1 / 2 } } } { ( 1 - c _ { 2 } \exp ( - \lambda \delta ^ { 3 } / 4 ) ) } .$$

we find When 183c1m/ 1/2 &gt; c3, this tends to zero for λ → ∞, proving the proposition. □


<!-- p:187 -->


Proof of Proposition 6.6 Again, we shall give the proof for the two-dimensional case, as the higher-dimensional case can be proved similarly. From the fact that g has bounded support, it follows that there are only finitely many configurations for S such that |S| = m. So it is enough to show that for any finite subset η of δZ2, we have

$$\lim _ { \lambda \to \infty } \frac { 1 } { q _ { 1 } ( \lambda ) } \sum _ { k = 2 } ^ { \infty } P ( | W | = k , S = \eta ) = 0 . \\$$

We have to introduce some more notation. We denote by W, the component ot s    (  s   s    to e =  uen  t   = ue  t  t      s s Furthermore, Hn is defined to be the event that no point of the point process X in IR2\ F− 1(η) is connected to any point in Wη. Then,

$$\{ | W | = k , \, S = \eta \} = \{ E _ { \eta , k } \cap H _ { \eta } \} .$$

We want to estimate the probability of Hn given En,k. Let δ1 be so small that the conclusion of Proposition 6.4 holds for 2δ1. Define rn as the highest first coordinate of a point in η: rη = max {x1 : (x1, x2) ∈ η}. The points lη and tη are defined similarly for the lowest first coordinate and highest second coordinate, respectively. The set Ar C R2 is defined as {(x1, x2) : x1 &gt; rη + 1δ}. Furthermore, A1 := {(x1, x2) : x1 &lt; lη − 2δ} and At := {(x1, x2) : x2 &gt; tη + δ}. Note that A, and A, are disjoint. Given the event Eη,k, the probability that Hη occurs is (using Proposition 1.3)

$$\exp \left ( - \lambda \int _ { \mathbb { R } ^ { 2 } \sqrt { F _ { \delta } ^ { - 1 } ( \eta ) } } g _ { 1 } ( y ; W _ { \eta } ) \, d y \right ) . \\ > 0 \, \text {be much smaller than } \delta _ { 1 } \cdot \text {If } E _ { \eta , k } \, \text { occurs, then there is at least one }$$

Let δ &gt; 0 be much smaller than δ1. If Eη,k occurs, then there is at least one point (x1, x2) ∈ Wη for which |x1 − rη| ≤ 2δ and we have

$$\int _ { A _ { r } } g _ { 1 } ( y ; W _ { \eta } ) \, d y \geq \int _ { ( \delta , \infty ) \times \mathbb { R } } g ( y ) \, d y ,$$

$$\int _ { A _ { l } } g _ { 1 } ( y ; W _ { \eta } ) \, d y \geq \int _ { ( - \infty , - \delta ) \times \mathbb { R } } g ( y ) \, d y .$$

and similarly,

So,

$$\int _ { A _ { l } \cup A _ { d } , } g _ { 1 } ( y ; W _ { l } ) \, d y \, \cdot \int _ { I R ^ { 2 } } g ( y ) \, d y - \int _ { ( u , \delta , \delta ) \times \mathbb { R } } g ( y ) \, d y .$$


<!-- p:188 -->


Let A+ = (0, δ) × (δ, ∞) and A\_ = (−δ, 0) × (δ, ∞) and take δ so small that

$$\int _ { A _ { - } } g ( y ) \, d y = \int _ { A _ { + } } g ( y ) \, d y \geq \int _ { ( - \delta , \delta ) \times \mathbb { R } } g ( y ) \, d y + c _ { 1 }$$

for some positive c1 . If both the width rn — In and the height (defined similarly) of η are smaller than 2δ1, we are done by Proposition 6.4. So without loss of generality, we may assume that the width rη — lη is at least 2δ1. If Eη,k occurs, then there is at least one point (x1, x2) ∈ Wη such that |tn − x2| ≤ 1δ. Either A+ + (0, x2) or A\_ + (0, x2) is contained in IR2\ Fδ− 1(η) and hence we find, using (6.31) and (6.32),

$$P ( H _ { \eta } | E _ { \eta , k } ) \geq \int _ { \mathbb { R } ^ { 2 } } g ( y ) \, d y + c .$$

Thus

$$\text {This} \quad & \frac { 1 } { q _ { 1 } ( \lambda ) } \sum _ { k = 2 } ^ { \infty } P ( | W | = k , S = \eta ) \, = \, e ^ { - \lambda \int _ { R ^ { d } } g ( y ) d y } \sum _ { k = 2 } ^ { \infty } P ( E _ { \eta , k } \cap H _ { \eta } ) \\ & \leq \sum _ { k = 2 } ^ { \infty } P ( E _ { \eta , k } ) e ^ { - \lambda c _ { 1 } } .$$

This tends to zero when λ → ∞.

□

####### 6.6Notes

The material in Sections 6.1 and 6.5 is taken from Penrose (1991). Proposition 6.1 is from Meester (1995) and Propositions 6.2 and 6.3 are taken from Penrose (1991). The equality of the critical densities is due to Meester (1995), but also Sarkar (1994) obtained the equality for a restricted class of connection functions. The argument given here is a continuum version of the argument given by Aizenman and Barsky (1987) for discrete percolation. The uniqueness of the unbounded component appears in Burton and Meester (1993).


<!-- p:189 -->


#### 7 Models driven by general processes

The case in which the driving point process is Poisson has been studied extensively in the previous chapters. It is natural to investigate what happens when the underlying process is not necessarily Poisson. Many of the results obtained for Poisson processes seem to depend heavily on the independence structure of such processes. However, sometimes it turns out that it is stationarity rather than independence which makes an argument work. In such cases, the assumption of independence obscures the picture of what is really happening. The assumption h tt  sv  as s a  s s  is   any proofs require, in addition to stationarity, that the point process also be ergodic. The class of ergodic point processes is much smaller than the class of stationary ones, so this seems to be a real loss of generality. However, in the first section we shall treat an interesting technique which makes it possible to carry over results for ergodic models to stationary ones. In this chapter, unless we specify sht   s       oss     s stationary.

### 7.1 Ergodic decomposition

Consider a measurable space (Ω, F) and let T be a transformation from Ω into itself. We denote by Mτ the set of all probability measures μ on (Ω, F) which make (Ω, F, μ, T) into a measure-preserving dynamical system. Our aim here is to show that the ergodic measures in Mr are very special in the following sense:

Proposition 7.1 The set Mτ is convex and the ergodic measures (w.r.t. T) are exactly the extremal points of Mτ.


<!-- p:190 -->


Proof For convexity we need to show that whenever μ1 and μ2 are in Mτ, so is αμ1 + (1 − α)μ2 for all 0 ≤ α ≤ 1, where (αμ1 + (1 − α)μ2)(E) = αμ(E) + (1 − α)μ2(E) for all E ∈ F. This, however, follows immediately from the definition of measure-preserving transformations.

To prove the second assertion of the proposition, suppose that μ ∈ M is not ergodic. This means that the σ-algebra of T-invariant sets is not trivial. Hence there exists a T-invariant measurable set E such that 0 &lt; μ(E) &lt; 1. We can define two probability measures μ and μ2 such that for every A ∈ F we have

$$\mu _ { 1 } ( A ) = \frac { \mu ( A \cap E ) } { \mu ( E ) } \quad \text {and} \quad \mu _ { 2 } ( A ) = \frac { \mu ( A \cap E ^ { c } ) } { \mu ( E ^ { c } ) } .$$

Because

$$\mu _ { 1 } ( T ^ { - 1 } A ) & = \frac { \mu ( T ^ { - 1 } A \cap E ) } { \mu ( E ) } = \frac { \mu ( T ^ { - 1 } A \cap T ^ { - 1 } E ) } { \mu ( E ) } \\ & = \frac { \mu ( T ^ { - 1 } ( A \cap E ) ) } { \mu ( E ) } = \frac { \mu ( A \cap E ) } { \mu ( E ) } = \mu _ { 1 } ( A ) ,$$

it follows that T is measure-preserving w.r.t. μ1. (We also say that μ is Tinvariant in such a case.) A similar argument is valid for μ2. Note that 1 = ll   ≠    =  ≠ lve

$$\mu ( A ) = \mu ( E ) \mu _ { 1 } ( A ) + ( 1 - \mu ( E ) ) \mu _ { 2 } ( A )$$

and hence μ is not an extremal point of Mτ. Conversely, suppose that μ is not extremal but ergodic. Then μ = αμ1 + (1 − α)μ2 for some 0 &lt; α &lt; 1 and μ1 ≠ μ2 both in Mτ. This of course implies that μ1 is absolutely continuous w.r.t. μ, whence the Radon-Nikodym theorem guarantees the existence of a μ-integrable function f such that

$$\mu _ { 1 } ( A ) = \int _ { A } f d \mu$$

for all A ∈ F. Both μ1 and μ2 are T-invariant and it follows easily that f is T-invariant also, i.e. f(T) = f μ-a.s. It is well known (see e.g. Petersen 1983 Proposition 4.1, p. 42) that this implies that f is an a.s. constant, which in turn implies by (7.1) that f ≡ 1 a.s. Hence μ = μ1 and hence either α = 1 or μ1 = μ2, a contradiction in either case. 口

Given the structure of a convex set of invariant measures, the extremal points of which are exactly the ergodic ones, it should not come as a surprise that it is possible to decompose' any T-invariant measure into ergodic ones. We make this precise in a moment, but first let us return to stationary point processes and start with an elementary example of such a decomposition.


<!-- p:191 -->


Consider two independent Poisson point processes X1 and X2 on IRa with densities λ1 and λ2, respectively, where λ1 ≠ λ2. Let X be the point process defined to be equal to X1 with probability and equal to X2 with probability . In other words, with probability 1, X(A) = X1 (A) for all A ⊂ IRd simultaneously, and with probability , X(A) = X2(A) for all A ⊂ IRd. Then X is a stationary point process which is not ergodic. To see the latter fact, consider the event E = {limt→∞ t−d X([0, t]d) = λ1}. According to Proposition 2.4 and 2.6 and the fact that λ1 ≠ λ2, the probability of E is ¿. It is an easy matter to check that E is translation invariant and hence X cannot be ergodic. In the notation of Chapter 2, if μ is the measure on (Ω, F) corresponding to X and μ1 and μ2 the measures corresponding to X1 and X2, respectively, then (Ω, F, μ, S) is not an ergodic m.p. dynamical system, but it is the case that μ = 2μ1 +  μ2. Furthermore (Ω, F, μi, St), i = 1, 2, are ergodic systems (Proposition 2.6).

The following proposition shows that this construction can be carried through in much greater generality than the example above. For a proof of the proposition we refer to Denker, Grillenberger and Sigmund (1976, section 13).

Proposition 7.2 Let (Ω, F, μ, T) be an m.p. dynamical system and let f be a real, μ-integrable function on Ω. There is a set E ∈ F with μ(E) = 0 such that for all ω ∈ Ω\ E, there exists an ergodic measure μω on (Ω, F, T) such that ω → ∫Ω fdμω is F-measurable, f is μω-integrable and

$$\int _ { \Omega } f d \mu = \int _ { \Omega \vee E } \int _ { \Omega } f d \mu _ { \omega } d \mu ( \omega ) .$$

The family of measures (μω)ωeΩ\E is called the ergodic decomposition of μ. (There is a certain uniqueness of the ergodic decomposition, that is why we call it the ergodic decomposition. We will not be concerned with this here though.) Note that we do not require that the μω's be different for different values of ω. Indeed, in the example given, μω = μ1 whenever ω is such that X(A) = X1(A) for all A, and μω = μ2 otherwise. As a special case of (7.2), consider the case where f = 1A for some A ∈ F. Then (7.2) reduces to

$$\mu ( A ) = \int _ { \Omega \rangle E } \mu _ { \omega } ( A ) d \mu ( \omega ) .$$

Note that by taking A = Ω in (7.3), we see that for almost all ω ∈ Ω\ E we have

$$\mu _ { w } ( \Omega ) = 1 .$$


<!-- p:192 -->


As an application of (7.3), consider a Boolean model (Ω, F, P), where Ω = Ω1 × Ω2 and P = P1 × P2 as in Chapter 1. What form does the ergodic decomposition of this Boolean model have? For this, consider the point process P defined on (Ω1, F1) (the notation is as in Chapter 2, Section 2.1). As already observed in Chapter 2, we may assume that an ergodic point process is ergodic under translation by e1. This point process has, according to (7.3), an ergodic decomposition (P1,ω1)ω1∈Ω1\E, where E ∈ F1 satisfies P1(E) = 0. From (7.4) it follows that (Ω1, F1, P1,ω1) is an (ergodic) point process. From Proposition 2.8 we know that any Boolean model driven by an ergodic point process is ergodic. Hence the Boolean model (Ω1, F1, P1,ω1) × (Ω2, F2, P2) is ergodic. We conclude that (P1,ω1× P2)ωjeΩ1\E is the ergodic decomposition of the Boolean model P1 × P2. In particular, the distribution of the radii is the same for all ergodic components of the decomposition. A similar remark applies to random-connection models; the connection function is the same in almost all components of the ergodic decomposition.

Returning specifically to Boolean models, suppose we can show that for all ergodic Boolean models with a certain property Q, an event A occurs almost surely and that we are faced with the problem of extending this result to staoda an od oan os  n  on orn ottn Q, we use (7.3) and conclude that whenever Pω(A) = 1 for all ω ∈ E, then also P(A) = 1, provided that almost all elements in the ergodic decomposition of P satisfy property Q. (We emphasize the latter statement because this is a necessary part of the argument which is sometimes forgotten in the literature.) Ergodic decomposition, therefore, provides a technique to extend results from ergodic models to general stationary models, but care is needed throughout this procedure.

### 7.2 Basic facts on coverage

Before we investigate percolation properties of general models, we prove some facts which are either interesting in themselves or which will be useful in later sections. The first result is a generalisation of a result which we already proved for Poisson Boolean models in Proposition 3.1.

Proposition 7.3 Consider a Boolean model (X, ρ) in IRd. If Eρd = ∞ then the whole space is covered by balls a.s.

Proof As noticed in the previous section, the ergodic components of (X, ρ) under Te, say, all have the same radius distribution ρ and we can henceforth assume that the model is ergodic with respect to Te, (which implies ergodicity under the group of all translations).


<!-- p:193 -->


In as s ss  n   ,   s    so as to obtain a finite density process. If we prove the proposition for this process, then it is certainly true for the original infinite density process. Therefore, we may assume that the density λ(X) of X is finite and is equal to 1. Let Cn be the ball centred at the origin and with radius 2n/d, n ∈ N. (Cn is non-random.) Note that l(Cn+1) = cd2n+1 = 2l(Cn), where cd is a constant depending only on the dimension. From Proposition 2.4 we have that for n large enough (depending on the realisation) Vn ≤ X(Cn) ≤ Vn, where Vn = (Cn). Now we write, for large enough n, X(Cn+1\Cn) = X(Cn+1) − X(Cn) ≥ λ Vn+1 − Vn = Vn- Vn =  Vn. Hence, forn large enough the annulus' Cn\Cn-1 contains at least ba2+1 points of the point process, where bd is another constant depending only on the dimension.

Now let E be the event that Co is not completely covered by a ball which is centred in C\C-1. Furthermore, let Am be the event that m is the first index such that X(C\Cn−1) ≥ bd2n+1 for all n ≥ m. It follows from the above that up to a set of measure 0, the Am's form a partition of the probability space. Write

$$P \left ( \bigcap _ { k = m } ^ { \infty } E _ { k } | A _ { m } \right ) & \leq P \left ( \bigcap _ { k = m } ^ { \infty } ( \text {all balls centered in } C _ { k } \langle C _ { k - 1 } \text {,} h \right ) \\ & \quad \text {radius at most } 2 ^ { k / d } + 1 ) | A _ { m } \right ) \\ & \leq \prod _ { k = m } ^ { \infty } P ( \rho \leq 2 ^ { k / d } + 1 ) ^ { b _ { d } 2 ^ { k + 1 } } , \\ \intertext { w h e r e t h e l s i n e q u a l l y f o w s f o r w i n g e n d e n c e $ f o r $ the r a d i s }$$

where the last inequality follows from the independence of the radii and the point process. It suffices to show that this expression equals zero. For k large enough, 2k/d + 1 ≤ 2(k+1)/d, so if we replace k + 1 by k, for k large, each term in the product is at most P(ρ ≤ 2k/d)ba2. Now, for m large enough, we find

<!-- p:194 -->


$$& \text {is an even by general processes} \\ & = \left \{ \prod _ { k = 2 ^ { * } } ^ { \infty } P ( \rho ^ { d } \leq k ) \right \} ^ { b _ { d } } \\ & = \left \{ \prod _ { k = 2 ^ { * } } ^ { \infty } \left ( 1 - P ( \rho ^ { d } > k ) \right ) \right \} ^ { b _ { d } } . \\ & \text {and only if } \sum ^ { \infty } _ { k = 2 ^ { * } } R ( \rho ^ { d } > k ) \right \} = .$$

This expression is zero if and only if Σk=2m P(ρd &gt; k) = ∞, which is equivalent to Eρa = ∞, proving the proposition. 口

The converse of the last proposition is not true in general (but it is in the Poisson case, see Chapter 3). It is not hard to show, using the same argument as in (3.2), that if Eρd &lt; ∞ and λ(X) &lt; ∞, then the expected number of balls intersecting a bounded region is finite. Of course the condition that the density of X be finite is necessary: if the density of X is infinite, then the expected number of points in a bounded region is infinite and so is the expected number of balls intersecting this bounded region. However, if we only want the number of intersecting balls to be finite a.s. then we do not need the finite-density assumption:

Proposition 7.4 Consider an ergodic Boolean model (X, ρ) in IRd such that the probability that the whole space is completely covered is strictly smaller than 1 (and hence equal to 0 by ergodicity). Then any bounded region in Rd is intersected by only initely many balls a.s.

Proof It suffices to consider the unit circle as the bounded region, so suppose that infinitely many balls have non-empty intersection with the unit circle with positive probability. Look at the proof of Proposition 3.1 and observe that the only properties of the Poisson process we have used there are the fact that the Poisson process is locally finite and the ergodicity of the transformations Se. The former is a property shared by all point processes and the latter can be generalised too: it follows from Proposition 2.7 that we can choose an orthonormal base (e1, .. . , ed) of IRd such that all transformations Sei act ergodically. (Again, the notation is as in Chapter 2.) Consider random variables Yn and Zn, n ∈ Z, defined as in the proof of Proposition 3.1 but now with respect to this new base. It then follows from that proof that the whole space is covered a.s., which is the required contradiction. 口

Note that the requirement that the process is ergodic in the last proposition is necessary: the conclusion is false for stationary processes. To see this, take a mixture of two ergodic processes, one where vacancy exists a.s. and one where bounded regions are intersected by infinitely many balls a.s.


<!-- p:195 -->


### 7.3 Unbounded components in Boolean models

We consider a Boolean model (X, ρ) where X is a stationary point process in Ra and ρ is the radius random variable of the model. Our aim here is to provide a classification of the possible topological structure of unbounded components in this model. In this section, C denotes a component which can be either occupied or vacant. Often, we consider the complement of a component C and, in particular, we are interested in the connected components of this complement in the usual topological sense. The latter components have nothing to do with the components in the Boolean model; so in order to avoid any confusion, we shall refer to these connected components as connected sets. Thus, the complement of a (vacant or unbounded) component of the Boolean model is the union of its connected sets.

Definition 7.1 Let C be a component of the Boolean model. Then the interior of C is defined as

int (C) := ∪{K; K is a bounded connected set in IRd\ C}.

The closure is defined as cl(C) := C ∪ int (C),

and the exterior is defined as

ext(C) := ∪{K; K is an unbounded connected set in IRd\C}.

If for two components C1 and C2 we have

C1 ⊆ cl(C2),

we say that C1 is enclosed by C2 and we write C1 &lt; C2. The relation&lt;' defines a partial ordering on the set of all components.

Lemma 7.1 The maximal components with respect to the ordering 'are exactly all unbounded components a.s.

Proof It is enough to prove the lemma for all ergodic components of (X, ρ) so we can assume ergodicity of the Boolean model. If IRd is completely covered by balls, we are done, so suppose it is not. From Proposition 7.4 we have that only finitely many balls intersect any bounded area a.s. This implies that any bounded occupied component has strictly positive distance to the nearest other occupied component a.s. 1n particular, for any bounded occupied component C there is some € &gt; 0 (depending on () such that the distance from C to the nearest other occupied component is at least 2e, say. (Note that both C and € depend on the configuration.) This means that the set {x ∈ IRd : 0 &lt; d(x, cl(C)) &lt; ∈} is completely vacant. Moreover, this set is connected and is a subset of a vacant component C'. It follows that C &lt; C' and C is not maximal indeed. If C is a bounded vacant component, then the boundary of cl(C) belongs to one occupied component and hence C is not maximal.


<!-- p:196 -->


It is clear from the definitions that an unbounded component has to be maximal. □

A realisation is said to be complete if for each component C, there exists an unbounded component C' such that C &lt; C'. A realisation is said to be an infinite cascade if each component is bounded. As an example of an infinite cascade, consider a Poisson Boolean model with fixed radii in two dimensions at criticality. It follows from Theorem 4.5 and the last paragraph in the Notes to Chapter 4 that in this situation, no unbounded vacant or occupied components exist a.s.

It is quite possible to construct a realisation which is neither complete nor an infinite cascade. However, we have the following result:

Proposition 7.5 In any Boolean model, the probability of a realisation which is neither complete nor an infinite cascade is zero.

Proof If the result is true in all ergodic components of the Boolean model we are done, so we again assume ergodicity. Suppose that with positive probability, there exists an infinite sequence of (bounded) components C1 &lt; C2 &lt; C3 &lt;  . . twill be enough to show that U=1 cl(C) = IR2. For this, take any x ∈ IRd and fix some y ∈ C1. If x ∈ C for some n we are done. Otherwise, we draw the straight line segment / from y to x and we take a box Bn which contains the line segment l. We shall colour I with two colours, red and blue, as follows. First, y is coloured red. We move along l in the direction of x and we change colour as soon as we enter a different component C. We move farther aonr  n   nr  ns s  r   nr so on. Note that it is quite possible to enter the same component more than once. If the colour changes infinitely often before we reach x then it must be the case that l goes through infinitely many balls. (Here we use the fact that the balls are convex.) But that would imply that infinitely many balls intersect the box B and this has probability zero according to Proposition 7.4. So with probability 1, only finitely many changes of colour are possible. Now m changes of colour means that the line segment l could have gone to at most Cm+1. In that case, x ∈ cl(Cm+1). Since x is arbitrary, the proof is complete. 口


<!-- p:197 -->


It is clear from the definition that being complete is a translation-invariant property. So if the Boolean model is ergodic, then either almost all realisations are complete or almost all realisations are an infinite cascade. From now on we assume that all Boolean models under consideration are complete.

Definition 7.2 An N-branch of the occupied component W of the origin is a maximal unbounded connected subset of W ∩ (BN)c.

Before we state the main results of this section we take a closer look at the realisations of Boolean models in two dimensions. Consider three disjoint boxes BN (:= BN + zi), i = 1, 2, 3, where zi ∈ 2NZ2. Suppose that in a realisation of (X, ρ), for i = 1, 2, 3, the vacant component Vi containing zi is unbounded and that ext(V) consists of (at least) three unbounded connected sets which we denote by Cj, j = 1, 2, 3. By taking N larger if necessary (and assuming that the boxes are so far apart that this increase in size causes no intersection among them) we can find points rj ∈ Cj ∩ Bλ for all i and j and continuous polygonal curves γj from z to rj such that the curve γj is contained (except and such that γj ∩ γj, = zi whenever j ≠ j'. We then have the following result, needed later on.

Lemma 7.2 In a two-dimensional Boolean model it is the case that, in the situation just described, the set

has cardinality at most 1.

Proof The proof proceeds by contradiction, using the well-known result on planar graphs by Kuratowski. So suppose that S contains at least two elements C and C', say. This means that we can find j1, j2 and j3 such that C = Ci ji for i = 1, 2, 3 and k1, k2 and k3 such that C′ = for i = 1, 2, 3. This implies that we can find continuous polygonal curves γ1 from to .2 and j2 γ2 from r .2 to r 3 which are completely contained in C. Let s 2 denote the last j2 j3 j2 point (starting from r2) these curves have in common. Similarly, we can find continuous polygonal curves γ from to1 .2 and γ2 from .2 to 3 which k2 are completely contained in C'. Let s denote the last point (starting from r2) these curves have in common. For ease of notation, we denote by rì t the point in {r|, r2, r3 \{r}, r}. The points and are defined in a similar fashion. Nexı we consider the bipartite graph G defined as follows. The vertices of G


<!-- p:198 -->


are {z1, z2, z3} ∪ {s 2 }. The edges are imbedded in the plane along the curves constructed above as follows:

- (i) z1 is connected to 2 along) and γ1, j2
- (ii) z2 is connected to 2 and along γ 2 , γk2 2 2 respectively, j2
- (ii) z1 is connected to 2 along γk1 and γí, k2
- (iv) z3 is connected to 2:2 along and γ2,
- (v) z3 is connected to 2 and γ2.

The construction of the edges of G is such that two edges can intersect only at vertices of G. Now suppose that it is possible to connect r with r by l2 rbi t o  hs    d  d st s nrsy of course). This would imply that along γi and α, respectively, γ3 and β. Thus this would create a new graph G' which is isomorphic to the complete bipartite graph K3,3. It is a well-known result in graph theory, due to Kuratowski, that K3,3 cannot be imbedded in the plane without non-trivial intersections between the edges. Hence curves α and β do not exist. But this implies that not all three points 2 and 3 are contained in the exterior of the Jordan curve J 33 connecting (z1, 1 .1 2 , Z3, rk3, s 2, rk1, z1) along edges of G. Thus at least 3 one of these three points, say, is contained in the interior of J. However, r and hence there exists a continuous polygonal curve from r} to infinity which is completely contained in C}. This curve then has to intersect an edge of G, but this is impossible because all edges of G are contained in vacant components or occupied components disjoint from C}. 口 11

Here are our main results. The first (occupancy) result is true in any dimension, but for the corresponding result for vacancy we need the dimension to be 2.

Theorem 7.1 Let W denote the occupied component containing the origin. Then for any N &gt; O, the probability that W has more than two N-branches is equal to zero.

Theorem 7.2 Consider a Boolean model in two dimensions and let V be the vacant component which contains the origin. The probability that ext(V) consists of more than two connected sets is equal to zero.


<!-- p:199 -->


Before we prove these results, let us look at the consequences in two dimensions. In two dimensions, the fact that any unbounded occupied component C has at most two N-branches implies that ext(C) consists of at most two connected sets. So in two dimensions the exterior of any unbounded component, vacant or occupied, contains at most two connected sets. Each of these connected sets gives rise to one neighbouring' unbounded component of the opposite type, and we conclude that each unbounded component has at most two i =  -     n  n ng, this immediately yields:

Theorem 7.3 In a Boolean model in two dimensions, the number of unbounded occupied components and the number of unbounded vacant components differ by at most one a.s.

In the last section of this chapter, we shall construct, for any integer K, a Boolean model with K unbounded occupied and K ± 1 unbounded vacant components. The proof of Theorem 7.1 resembles the proof of uniqueness of unbounded components in Poisson Boolean models. In that proof we already used the idea of branches. In the next section we shall see that Theorem 7.3 can be used to prove uniqueness results for Boolean models driven by general point processes under certain conditions on the radius random variable.

Trying to use the ideas of Chapter 3 creates problems similar to those in Chapter 4. We do not want to assume that the density of the point process is finite, and this is crucial in the proof of Theorem 3.6. In the proof of Theorem 4.6, the way out was to look at vacant components inside little cubes. Here, we can do something similar:

Lemma 7.3 Consider a Boolean model (X, ρ, λ) and choose K &lt; ∞ such that P(ρ &gt; K) &gt; 0. Let A ⊂ IRd be a convex set with diameter at most K. Let C[A] denote the (random) region

that is, C[A] is the occupied region formed by points in A. Then the number of connected components in A∩C[A], to be denoted by YA, has finite expectation.

Proof The set A is convex, and hence its intersection with any ball, if not e     t t   ty      k. This would complete the proof if the density of X were finite. To treat the general case, note that YA can be larger than 1 only if all balls centred in A have radius at most K. Now condition on the number of points in A to obtain


<!-- p:200 -->


$$r i d u s a t o m k . \text { Now condition on the number of points in } A & \text { to obtain} \\ E \{ Y _ { A } | \, X ( A ) = k \} & = \sum _ { n = 1 } ^ { \infty } n P ( Y _ { A } = n \, | \, X ( A ) = k ) \\ & \leq \, P ( Y _ { A } = 1 \, | \, X ( A ) = k ) + \sum _ { n = 2 } ^ { \underline { k } } n \{ P ( \rho \leq K ) \} ^ { k } \\ & \leq \, 1 + \frac { 1 } { 2 } k ( k + 1 ) \{ P ( \rho \leq K ) \} ^ { k } .$$

Hence

$$E Y _ { A } \leq \sum _ { k = 0 } ^ { \infty } \left ( 1 + \frac { 1 } { 2 } k ( k + 1 ) \{ P ( \rho \leq K ) \} ^ { k } \right ) P ( X ( A ) = k ) ,$$

and this sum is finite because P(ρ ≤ K) &lt; 1 by assumption.

口

Proof of Theorem 7.1 It is clear from the discussion on ergodic decomposition in Section 7.1 that it suffices to prove the theorem for ergodic Boolean models. Suppose that W has more than two N-branches with positive probability for some N. The event that W has more than two N-branches is denoted by E0(N ). Choose ∈ &gt; 0 so small that P(ρ &gt; 2€ √♂) &gt; 0. A local component is a connected set in C[B2ez] = Ux B2e(S(x, i)∩ B2 ez), for some z ∈ Zd. From Lemma 7.3, it follows that the expected number of local components in Be is finite. As in Chapter 3, we choose a number K large. Given K, we choose M &gt; N and define the event E0(N, M) := E0(N) ∩ {all N-branches of W contain balls centred in at least K different boxes B2€z C BMN\ BN} ∩ {B€ is covered by a ball centred in Be }. It is clear that this event has positive probability η, say, if ∈ is small enough. The event E2(N, M) is defined by translating this event over the vector z.

lt follows from Proposition 2.7 that we can choose € such that all translations Ž2ee, are ergodic. (It might be necessary to rotate the coordinate axes for this.) As in the proof of Theorem 3.6, it follows that the expected cardinality of the set

$$R = \left \{ z \in Z ^ { d } \ \colon \ B _ { M N } ^ { 2 N z } \subset B _ { L N } ^ { 0 } , \ E ^ { 2 N z } ( N , M ) \text { occurs} \right \}$$

is equal to ηLd. For z ∈ R, we have Y B2N: = 1 by definition. Furthermore, for ) and C(3) the set of all local omponents in each z ∈ R, we denote by C (1) C(2) of the first three N-branches (which can be thought of as being ordered in some arbitrary way) contained in B


<!-- p:201 -->


card(Ci)) ≥ K for all i. Finally, for z ∈ R, we identify z with the only local of Theorem 3.6, using local components instead of points of the point process.

0

REMARK: The reader should note that the only place in the proof of Theorem 7.1 where we used the independence of the radii and the point process was to derive the fact that the expected number of local components in B€ is finite. The fact that we put balls around each point rather than some other shape is only relevant as far as this affects the expected number of local components. mns n  s r s  s pe s a sa ses around each point in a stationary way such that the expected number of local components is finite, the proof above goes through without difficulty.

Proof of Theorem 7.2 In order to arrive at a contradiction, suppose that ext(V ) consists of at least three (unbounded) connected sets with positive probability. By looking at the boundary of these connected sets we see that there are at least three unbounded occupied components with positive probability. Hence there is a non-random box BN such that BN intersects these three unbounded occupied components with positive probability. We now perform the following trick: consider the two-dimensional lattice 2NZ2 = {2Nz : z ∈ Z2}. As in Chapter 1, we can create a stationary point process Y by 'shifting' this lattice over a random vector which is chosen uniformly on Bn. Now consider the superposition of X and Y, where X and Y are chosen to be independent. It is easy tsups sst ss sn t t os t tat s ses is again stationary. The points which come from the process Y will not be the centre of a ball with random radius. Instead we do the following: for every point y of the point process Y we check whether or not the square B has at least three occupied N-branches in the model (X, ρ); i.e. we check whether or not the complement of B contains at least three unbounded occupied components which intersect the boundary of B. If this is not the case, we do not put any shape around y. If this is the case, however, then with probability , we centre a square with side length 2N — 8 at y where δ is a small positive number, and with probability  we do nothing. The model obtained is stationary, even though the configuration of squares depends on the realisation of the original model (X, ρ).

We do not change the balls which are centred at the points of X. As we already saw above, for € &gt; 0 small enough, the expected number of local components in B€ in the Boolean model (X, ρ) is finite. If, in addition,


<!-- p:202 -->


2€ &lt; 2N – δ, then the extra squares coming from points of the process Y can increase the number of local components in B€ by at most one, because once a point of Y is centred in B€, the whole box B€ is covered by the square centred at this point. We conclude from the remark preceding this proof that the new superposed model has all the properties which make the proof of Theorem 7.1 wo          s s   wo N-branches in the occupied component of the origin a.s. However, we already concluded that for the Boolean model (X, ρ) there exists a number N such that probability. There is a positive probability that y is the centre of a square with side length 2N — δ. For δ small enough, there is a positive probability that this square intersects all three unbounded occupied components and that the square is contained in BN. According to Lemma 7.2, for N large enough, there are only finitely many boxes By, y ∈ Y which have a non-empty intersection with more than one of the three unbounded occupied components of (X, ρ) which intersect BN and whose complement contains at least three N-branches. With positive probability, no point of Y in one of these boxes is the centre of a square and hence with positive probability, these unbounded components remain disjoint outside BN. The conclusion is that we have constructed in the superposed model an unbounded occupied component with three N-branches. According to Theorem 7.1 and the remark preceding this proof, this is impossible and the proof is complete.

### 7.4 Uniqueness in Boolean models

In Chapters 3 and 4 we proved that in a Poisson Boolean model both the unbounded occupied and unbounded vacant component are unique a.s. We cannot expect this to be true in general Boolean models. Here is a very simple counterexample in two dimensions. Consider the following point process in the spirit of Example 1 in Section 1.2: we translate the points of the lattice {(z1, 2z2) : z1, z2 ∈ Z} over a random (uniform) vector in {0, 1] × [1, 2]. Thus the horizontal distance between two points is 1, and the vertical distance bet    = (   t  s     s d t lean model it is easy to see that we get infinitely many unbounded occupied and vacant components a.s. Hence certain conditions are necessary in order to obtain uniqueness. The sufficient conditions which we obtain are conditions conceming the support of the radius random variable ρ and moment conditions on the point process X.


<!-- p:203 -->


Theorem 7.4 Consider a Boolean model (X, ρ) in IRd. If for every M &gt; 0 we have

$$P ( \rho > M ) > 0$$

then there is at most one unbounded occupied component a.s.

The situation for vacant components is not quite as nice as this. In two dimensions however, we have the following result.

Theorem 7.5 Consider a Boolean model (X, ρ) in two dimensions. Iffor every € &gt; 0 we have

$$P ( \rho < \epsilon ) > 0$$

then there is at most one unbounded vacant component a.s.

To obtain uniqueness for vacancy in higher dimensions, we have to impose further conditions on the point process X. But it is easy to rule out all possibilities except zero, one and infinity:

Theorem 7.6 For an ergodic Boolean model (X, ρ) in any dimension, if (7.7) holds, the number of unbounded vacant components is either zero, one or infinity a.s.

The last result of this section gives a condition to rule out the case of infinitely many unbounded vacant components.

Theorem 7.7 Consider a Boolean model in dimension d ≥ 3. Suppose that (7.7) holds and that, in addition,

$$E ( ( X ( B _ { n } ) ) ^ { d } ) < \infty$$

for all n and that the support of ρ is bounded. Then there is at most one unbounded vacant component a.s.

Proof of Theorem 7.4 First we remark that it suffices to prove the result for ergodic Boolean models. This is clear from the discussion of ergodic decomposition in Section 7.1 and the fact that the distribution of the radii is the same in almost all ergodic components; see the discussion just before the end of Section 7.1.

In an ergodic Boolean model, the number of unbounded occupied components is an a.s. constant according to Theorem 2.1. We have to show that this constant is either zero or one. To this end, suppose first that it is at least three (which covers the case of infinitely many). This implies that there is a box B such that the following event E has positive probability: E := {there are at least three unbounded occupied components intersecting Bn and X(B) ≥ 1}. A contradiction arises as follows. We choose a point of X in B and we increase the radius of the ball centred at this point until this ball intersects at least three unbounded occupied components. Leaving the rest of the realisation as it is, we create in this way a realisation with an unbounded occupied component with three M-branches for some large M. Also, this has positive probability because of the independence of the radii and the point process and the fact that the support of the radii is unbounded. This then contradicts Theorem 7.1.


<!-- p:204 -->


Next we suppose that the number of unbounded occupied components is finite but larger than one. (Note that there is overlap with the previous case.) Then there exists a number K ≥ 2 such that the number of unbounded occupied components is equal to K a.s. The argument is almost the same as above: there exists a box Bm such that this box intersects at least two unbounded occupied components and at the same time contains at least one point of X with positive probability. By increasing the radius of a ball centred in this box, we can connect two different unbounded components. In the resulting realisation, we have strictly less than K unbounded occupied components, and all this occurs with positive probability. This contradicts the fact that the number of unbounded occupied components is K a.s.

Proof of Theorem 7.5 Again, by the same reason as above, it suffices to prove the theorem for ergodic Boolean models. The proof is similar to the proof of Theorem 7.4, though a little more care is needed. Suppose first that the number of unbounded vacant components is at least three. Then there exist boxes Bn and BN with n &lt; N such that with positive probability B intersects at least three unbounded vacant components and at the same time, all balls centred in B are contained in BN. The fact that the balls can be arbitrarily small now allows us to reduce the radii of all balls centred in B until the intersection between any two such balls is empty. All unbounded components in the original realisation which intersected Bn are now connected to each other through the vacancy in B, but the configuration outside BN remains unchanged. Thus no new unbounded vacant components can arise by this procedure. But now we have created an unbounded vacant component whose exterior consists of at least three unbounded connected sets, and this contradicts Theorem 7.2. The case in which the number of unbounded vacant components is finite but larger than one is treated similarly and we omit the proof. 口


<!-- p:205 -->


Proof of Theorem 7.6 In fact the proof of this theorem has been given already in the proof of Theorem 7.5. It is shown in that proof that we may connect any finite number of unbounded vacant components by reducing the radii of certain balls. So if we first assume that the number of unbounded vacant components (an almost sure constant by ergodicity) is K, say, then by connecting them we see that there is also a strict positive probability of having strictly less than K such components, a contradiction. □

It remains to prove Theorem 7.7.

Proof of Theorem 7.7 It follows from the ergodic decomposition in (7.2) that (in the notation of (7.2)) if a random variable Y has finite expectation ∫Ω Ydμ, then almost all expectations ∫Ω Ydμω are also finite. As before, the radius distribution is the same in almost all ergodic components of the Boolean model. Hence we can again assume that the model is ergodic.

We see from (7.8), the boundedness of the balls and Lemma 4.5 that the expected number of vacant components in the unit cube is finite. Check the proof of Theorem 7.1 and observe that if we redefine a local component as a connected vacant component in a cube, the proof goes through completely. Thus we have shown that if V denotes the vacant component of the origin, for any N &gt; 0, the probability that V has more than two N-branches is zero.

The rest of the argument is as in Theorem 7.5. According to Theorem 7.6 we only need to rule out the possibility to have infinitely many unbounded vacant components. Indeed, if more than three unbounded vacant components exist with positive probability, we can connect them by reducing the radii of certain balls, thereby obtaining an unbounded vacant component with three N-branches for some N, which is a contradiction.

### 7.5 Uniqueness in random-connection models

We already proved in Chapter 6 that in a Poisson random-connection model, only one unbounded component can exist a.s. The fact that the driving point process is Poisson was used in two places only. First of all, we used the fact that one can 'add' points to an existing configuration. However, we already noted at the end of the proof of Lemma 6.5 that in case the connection function g has infinite range (i.e. satisfies M = ∞ in the notation of Chapter 6) we do not need to add these points at all.

The second fact about Poisson point processes we used was that it has finite density. So without any work, we conclude that if the RCM is such that X has finite density and g has infinite range, there can be at most one unbounded cn nt n mnn nnnnrt nn n e  rn nnte  nn t is easy to construct an RCM with finite-range connection function for which there are infinitely many unbounded components. In fact, the example at the beginning of the previous section can serve here as well, noting that a Boolean model with fixed-radius balls is in fact an RCM too. But we shall see now that it is possible to remove the assumption that the density of X be finite:


<!-- p:206 -->


Theorem 7.8 Let (X, g) be an RCM such that g has infinite range. Then there can be at most one unbounded component a.s.

As noted before, the proof of Lemma 6.5 goes through without difficulty if g has infinite range. Hence we need only to rule out the case of having infinitely many unbounded components. Here we follow the usual strategy and we first deal with the analogue of Lemma 7.3:

Lemma 7.4 Consider an RCM (X, g) and denote by G the (a.s. finite) graph obtained from this RCM by taking all points of X in Bn and all connections between them. Then the expected number of connected components in G is bounded from above by (g(2n√d))-1 &lt; ∞.

Proof First we condition on the event that X(Bn) = k and we shall obtain a bound which is independent of k. We denote the points of X in Bn by x1 , . . . , xk. Let for i = 1,..., k Gi be the graph which we obtain by only taking into account the points x1, ..., x and the connections between these points, so that Gk = G. Denote by Ci the number of connected components in G. We obviously have that EC1 = 1. To estimate ECn+1, we note that adding a vertex xn+1 to {x1, . . . , xn} and possible connections between xn+1 and {x1, . . . , xn} only can increase the number of connected components if x+1 is not connected to any of the previous points. Hence, where p := (g(2n√))−1. Hence it follows that

<!-- p:207 -->


$$E C _ { n + 1 } \leq \sum _ { i = 0 } ^ { n } ( 1 - p ) ^ { i } \leq p ^ { - 1 }$$

for all n. This bound is independent of k and the proof is complete.

口

Proof of Theorem 7.8 Using the argument in the proof of Lemma 6.5 in Chapter 6 we see that if infinitely many unbounded components exist then, for some N, the component of the origin has with positive probability more than two (disjoint) N-branches, where a branch is defined as in Definition 7.2. If we redefine a local component as a component of the graph obtained by considering 2Nz the RCM in a box B only (as in Lemma 7.4), we can now copy the proof of Theorem 7.1 to show that this leads to a contradiction. This completes the proof. 0

### 7.6 Cutting and stacking

Stationary and ergodic point processes were introduced in Chapter 1. Some examples were given, but no mechanism was provided to obtain stationary and ergodic point processes in a constructive way. In the examples given in the next section we need a certain type of point processes and the goal of this section is to introduce these point processes. It is quite possible to describe the construction of these processes at a heuristic level. To prove, however, that this construction gives rise to stationary and ergodic point processes, more rigour is needed.

We explain the construction in detail for the two-dimensional case, the higherdimensional case being a straightforward generalisation of this. The probability space involved is the cube Ω := [0, 1)3 with ordinary Lebesgue measure which we shall denote by P here. An element ω ∈ Ω is denoted by ω = (u, x), where u ∈ [0, 1)2 and x ∈ [0, 1). The method is such that any suitable (to be made precise later) subset A of Ω gives rise to a stationary and ergodic point process XA defined on Ω.

Suppose that (u, x) and (u + u', x) are both in Ω. Then we set

$$S _ { u ^ { \prime } } ( u , x ) = ( u + u ^ { \prime } , x ) .$$

Thus we have defined the transformation Su' on a subset of Ω. Next, we want to extend this definition to a larger subset of Ω. To this end, we perform the so-called cutting and stacking procedure. We subdivide Ω into four slices

$$A _ { 1 } ^ { k } \colon = [ 0 , 1 ) ^ { 2 } \times \left [ \frac { k } { \bar { 4 } } , \, \frac { k + 1 } { 4 } \right ) , \quad k = 0 , 1 , 2 , 3 .$$


<!-- p:208 -->


Figure 7.1. The cutting and stacking procedure.

We now rearrange these slices as follows. Let Ω1 be the set [0, 2)2 × [0, ‡) and define the 'stacking function''fi : Ω → Ω1 as follows

$$\begin{array} { r l } { \text {define the stacking function} \int _ { 1 } \colon \mathbb { S } \to \mathbb { S } _ { 1 } \text { as follows} } \\ { \intertext { f ( a , b , x ) = } \left \{ \begin{array} { l l } { ( a , 1 + b , x ) } & { \text { for } ( a , b , x ) \in A _ { 1 } ^ { 0 } , } \\ { ( 1 + a , 1 + b , x - \frac { 1 } { 4 } ) } & { \text { for } ( a , b , x ) \in A _ { 1 } ^ { 1 } , } \\ { ( a , b , x - \frac { 1 } { 2 } ) } & { \text { for } ( a , b , x ) \in A _ { 1 } ^ { 2 } , } \\ { ( 1 + a , b , x - \frac { 3 } { 4 } ) } & { \text { for } ( a , b , x ) \in A _ { 1 } ^ { 3 } . } \end{array} } \\ { \text {Thus the function } f \text { just computes the algorithm } A _ { 1 } ^ { 1 } \text { to } ( a , b , x ) \in A _ { 1 } ^ { 2 } , } \end{array}$$

Thus the function fi just stacks the slice A to fi (A) which is one of the four blocks making up Ω1; see Figure 7.1. Now we can define Su' on a larger subset of Ω as follows: if both (u, x) and (u + u′, x) are in Ω1 we set

$$S _ { u ^ { \prime } } ( f _ { 1 } ^ { - 1 } ( u , x ) ) = f _ { 1 } ^ { - 1 } ( u + u ^ { \prime } , x ) .$$

Note that this is really an extension of Su. If Su was already defined in (7.9) it coincides with (7.10).

This procedure can be repeated. We divide Ω1 into four slices

$$A _ { 2 } ^ { k } \colon = \{ 0 , 2 ) ^ { 2 } \times \left [ \frac { k } { 1 6 } , \frac { k + 1 } { 1 6 } \right ) , \quad k = 0 , 1 , 2 , 3 .$$

Putting Ω2 := [0, 4)2 × [0, ) we define the stacking function f2 : Ω1 → Ω2 as the function which stacks the slice A2 to f2(A2), where f2(Ak) is one of the four blocks making up Ω2, so

$$f _ { 2 } ( A _ { 2 } ^ { 0 } ) & = [ 0 , 2 ) \times [ 2 , 4 ) \times [ 0 , \frac { 1 } { 1 6 } ) \\ f _ { 2 } ( A _ { 2 } ^ { 1 } ) & = [ 2 , 4 ) \times [ 2 , 4 ) \times [ 0 , \frac { 1 } { 1 6 } ) \\ f _ { 2 } ( A _ { 2 } ^ { 2 } ) & = [ 0 , 2 ) \times [ 0 , 2 ) \times [ 0 , \frac { 1 } { 1 6 } ) \\$$

$$f _ { 2 } ( A _ { 2 } ^ { 3 } ) = [ 2 , 4 ) \times [ 0 , 2 ) \times [ 0 , \frac { 1 } { 1 6 } ) .$$


<!-- p:209 -->


If (u, x) and (u + u', x) are both in Ω2 we set

$$S _ { u ^ { \prime } } ( ( f _ { 2 } \circ f _ { 1 } ) ^ { - 1 } ( u , x ) ) = ( f _ { 2 } \circ f _ { 1 } ) ^ { - 1 } ( u + u ^ { \prime } , x ) .$$

We continue in the obvious way, obtaining sets Ωn and maps fn : Ωn-1 → Ωn for all n ≥ 1 (where Ω0 = Ω). At each step we extend the definition of Su'. We claim that the subset of points (u, x) of Ω for which Su' is defined for all u' ∈ IR2 has Lebesgue measure 1. To see this, let Em be the set of points (u, x) for which Su is defined for all u′ ∈ R2 with u'| ≤ M. Furthermore, we put

$$E _ { M } ^ { n } \coloneqq \{ \omega \in \Omega \, \colon d ( ( f _ { n } \circ f _ { n - 1 } \circ \cdots \circ f _ { 1 } ) ( \omega ) , \partial ( \Omega _ { n } ) ) \geq M \} ,$$

and that EM = ∪x=1 EM. But P(EM) = (1/2n)(2n − 2M)2 → 1 as n → ∞. Hence P(EM) = 1 for all M and the claim follows.

Now we can define the point process XA. For any measurable B C IR2 consider the set

$$U _ { B } ( \omega ) \coloneqq \{ u \in B \ \colon S _ { u } ( \omega ) \in A \} .$$

If A is such that UB (ω) is almost surely finite for every measurable and bounded set B then we define XA by the relation

$$X _ { A } ( B ) ( \omega ) = \text {card} ( U _ { B } ( \omega ) ) ;$$

i.e. there is a point at x if and only if Sx (ω) ∈ A.

Proposition 7.6 Let A ⊂ Ω be such that X A(B)(ω) is a.s. finite for all bounded sets B ⊂ R2. Then XA is a stationary and ergodic point process.

Proof It is an easy matter to check that {Su : u ∈ IR2} is an IRd-action on Ω equipped with Lebesgue measure (for the definition of IRd-actions, see Chapter 2). In particular, each transformation Su is measure preserving. Also, for x ∈ IR2 and writing Tx for the translation in IR2 over the vector x we have

$$P ( X _ { A } ( B _ { 1 } ) & = k _ { 1 } , \dots , \, X _ { A } ( B _ { n } ) = k _ { n } ) \\ & = P ( S _ { x } ^ { - 1 } ( X _ { A } ( B _ { 1 } ) = k _ { 1 } , \dots , \, X _ { A } ( B _ { n } ) = k _ { n } ) ) \\ & = P ( X _ { A } ( T _ { - x } B _ { 1 } ) = k _ { 1 } , \dots , \, X _ { A } ( T _ { - x } B _ { n } ) = k _ { n } )$$

and hence the stationarity of XA follows from the measure-preservingness of the group {Su : u ∈ IR2}.

For ergodicity we need to show that {Su : u ∈ R2} acts ergodically on Ω. This can be done as follows. Suppose that there exists a set E ⊂ Ω with 0 &lt; P(E) &lt; 1 and which is invariant under all transformations {Su : u ∈ IR2}. This would imply that P(S−' E) = P(E) for all u. According to Lebesgue's density theorem, for all € &gt; 0 it is the case that for almost all x ∈ E, there exists a k large enough so that the box Bx,k of the form [l1, l1 + 4−k] × [l2, l2 + 4−k] × [l3, l3 + 4−k] containing x and where li is of the form n4−k for integers ni satisfies l(E ∩ Bx,k)/l(Bx,k) ≥ 1 − €. This implies that for k large, the set Ωk contains two little cubes with side length 4-k such that E covers the first cube more than half, and Ec covers the second cube more than half. Now note that the 'thickness' of Ωk is exactly 4-k. Thus we can find a transformation Su such that Su(E) ∩ E has positive measure, a contradiction.


<!-- p:210 -->


Figure 7.2. The generalised cutting and stacking.

Here are some examples of stationary and ergodic point processes obtained this way.

Example 7.1 If the set A is a countable collection of points, then XA satisfies XA(Rd) = 0 a.s. This is certainly a stationary and ergodic point process.

ESx   ×   ) =  t        r  or some 0 ≤ x1, x2. The point process obtained this way is just the point process of Example 1.1 in Section 1.3. As already explained in Chapter 1, we can think of this process as the integer lattice Z2 translated over a random vector which is uniformly distributed over the unit square.

The construction up to this point is not flexible enough for our purposes. Here is a generalisation: Choose a sequence {αn} of positive numbers with the requirement that αn grows at most polynomially in n. (This assumption is too strong but enough for our purposes.) Instead of rearranging the slices next to each other as above, we now construct a frame' around the slices of width α at the n-th iteration; see Figure 7.2. To this end, we define for each n mutually disjoint subsets Γn ⊂ IR3 which are also disjoint from Ω. We shall see in a moment that we can take each Γ to be a finite union of disjoint blocks of a certain size. The stacking function fi in the first construction is replaced by a map g1 : Ω ∪ Γ1 → IR3, which on Ω is defined as


<!-- p:211 -->


$$\begin{array} { r l } & { \mathbf l a p g | \cdot \Omega \cup \mathbf l a p | \mapsto \mathbb { I } \, , \, \text {which on } \Omega \, \text { is defined as} } \\ & { \quad g _ { 1 } ( A _ { 1 } ^ { 0 } ) = [ 0 , 1 ) \times [ 1 , 2 ) \times [ 0 , \frac { 1 } { 4 } ) + ( \alpha _ { 1 } , 1 + 2 \alpha _ { 1 } , 0 ) } \\ & { \quad g _ { 1 } ( A _ { 1 } ^ { 1 } ) = [ 1 , 2 ) \times [ 1 , 2 ) \times [ 0 , \frac { 1 } { 4 } ) + ( 1 + 2 \alpha _ { 1 } , 1 + 2 \alpha _ { 1 } , 0 ) } \\ & { \quad g _ { 1 } ( A _ { 1 } ^ { 2 } ) = [ 0 , 1 ) \times [ 0 , 1 ) \times [ 0 , \frac { 1 } { 4 } ) + ( \alpha _ { 1 } , \alpha _ { 1 } , 0 ) } \\ & { \quad g _ { 1 } ( A _ { 1 } ^ { 3 } ) = [ 1 , 2 ) \times [ 0 , 1 ) \times [ 0 , \frac { 1 } { 4 } ) + ( 1 + 2 \alpha _ { 1 } , \alpha _ { 1 } , 0 ) . } \\ & { \quad A t h i s p o i n g w e c h o o s e \Gamma , i n s u c h a w a y t h a r w e c a n d f i n e , g a n o r \Gamma , s u c h } \end{array}$$

At this point we choose Γ in such a way that we can define gı on Γ1such that g1 is measure preserving and

$$g _ { 1 } ( \Gamma _ { 1 } ) = \{ [ 0 , 2 + 3 \alpha _ { 1 } ] ^ { 2 } \times [ 0 , \frac { 1 } { 4 } ) \} \rangle g _ { 1 } ( \Omega ) .$$

One can think of g1 acting on Γ1 as taking blocks from Γ1 and rearranging them so as to form a frame of width α1 around the four slices coming from Ω. As such g1 is still piecewise linear on Ω U Γ1. On U2Fi, which will be defined in a moment, we shall define gi to be the identity. We write Ω1 := g1(Ω ∪ Γ1) = [0, 2 + 3α1]2 × [0, ‡). As before, if both (u, x) and (x   t

$$S _ { u ^ { \prime } } ( g _ { 1 } ^ { - 1 } ( u , x ) ) = g _ { 1 } ^ { - 1 } ( u + u ^ { \prime } , x )$$

as in (7.10). This procedure is repeated. We cut 1 into four slices which we rearrange with a frame of width α2 around it, where the frame is constructed from a rearrangement of blocks which form the set Γ2 C IR3. The map which accomplishes this stacking is the analogue of stacking function f2 above and is denoted by g2. Hence g2 is a piecewise linear map from 1 ∪ Γ2 → 2. On λ=3Γi, we define g2 to be the identity. If (u, x) and (u + u', x) are both in 2 we set

$$S _ { u ^ { \prime } } ( ( g _ { 2 } \circ g _ { 1 } ) ^ { - 1 } ( u , x ) ) = ( g _ { 2 } \circ g _ { 1 } ) ^ { - 1 } ( u + u ^ { \prime } , x )$$

as before. We continue in the obvious way, obtaining maps gn : n-1 =n Γi → Ωn as analogues of the stacking maps fn above. We put Γ := U=1 and the probability space on which we define our point processes is just Ω ∪ Γ with normalised Lebesgue measure P as to have P(Ω ∪ Γ) = 1. Note that it is here where we use the fact that the sequence {α} does not grow too fast: it is an easy matter to check that the Lebesgue measure of Γ is finite under our assumptions, i.e. the total volume of the framework added is finite. As before, for almost all ω ∈ Ω ∪ Γ, the map Su(ω) is defined for all u ∈ IR2.

Ergodic point processes XA, for A ⊂ Ω ∪ Γ for which (7.12) is finite for every measurable and bounded set B C R2 can now be defined as in (7.13). Examples of this construction will be given in the next section.


<!-- p:212 -->


Figure 7.3. The bold line segments form the set π(B1). The large square is the front face of Ωn

### 7.7 Examples

The cutting and stacking procedure of the previous section can be used as a counter-example machine'. We shall construct some examples which can be used to show that certain conditions in results of this chapter can not be omitted. We freely use the notation of the previous section.

Example 7.3 (A stationary tree) Consider the generalised cutting and stacking procedure of the previous section and take αn = 1 for all n. If we define dn via Ωn = [0, dn]2 × [0, ()n), we see that dn satisfies the recurrence relation dn+1 = 2dn + 3, which is readily solved under the boundary condition d0 = 1, giving that dn = 2"+2 — 3 for all n. In order to describe a point process XA we need to specify a set A. In fact, in order to specify A it is enough to specify sets of the form gn  ...  g1(A) ∩ Ωn =: An for all n and this is what we shall do. It is convenient to first describe a set Bn C Ωn and then explain how An can be obtained from it. The first thing to remark is that if π denotes projection on the plane {(x1, x2, x3) : x3 = 0}, Bn and An will be such that π−1π(Bn) ∩Ωn = Bn and π−1π(An) ∩Ωn = An respectively. It is therefore enough to describe the projections π(B) and π(An) for all n. A picture is worth more than a thousand words, so the set π(B1) is defined to be the union of a finite number of straight line segments and is depicted in Figure 7.3.

The next iteration gives the set B2 and π(B2) is depicted in Figure 7.4. It sho s  o      ss       e yields a stationary (and ergodic) imbedding of a tree-like structure in the plane. The set π(An) can now be obtained from π(B) by replacing the straight line s   n s  n  (   n  ns nts each neighbouring point; see Figure 7.5 for the case n = 1.


<!-- p:213 -->


Figure 7.4. The bold line segments form the set π(B2).

Figure 7.5. The set π(A1) is obtained from π(B1) by replacing the straight line segments by evenly spaced points.

The question may arise where the origin is in this construction and what the actual point process X looks like. Well, take n so large that ω ∈ , and denote by 0 the projection π (ω) of ω. From the fact that π−1π(An) ∩n = An we see that Sx (ω) ∈ An if and only if Sx (0) ∈ π (An). So once ω ∈ n, the projections π(A) tell it all and the points which make up π(An) are the actual points of the point process XA. Once ω is in n, each further iteration determines the points of the point process in a larger box containing the origin.


<!-- p:214 -->


Figure 7.6. The second iteration in the construction of two disjoint stationary trees with a positive distance from each other.

Example 7.4 (Intertwined trees) Once we have the example of the stationary tree above, it is quite easy to come up with some variations on the same theme. Instead of one tree we can construct two trees simultaneously in the same spirit as in Example 7.1. It is not necessary to repeat the whole construction, we just give the picture (Figure 7.6) which is the analogue of Figure 7.4. In this construction we obtain two intertwined trees with a positive distance from each other. Of course, in the point process which we construct from this, we replace all straight line segments by evenly spaced points as in the first example.

n  n  n n n   k n extended to any finite number of trees. Here is a way to construct any finite number of stationary trees using the cutting and stacking procedure. We depict the first iteration of a construction in Figure 7.7, as it will be clear how to continue.

After these examples we discuss the relevance to percolation theory. From Theorem 7.4 we know that whenever the radii of the balls are unbounded, there can be at most one unbounded occupied component. Furthermore, in two dimensions, if the radii can be arbitrary small, there can be at most one unbounded vacant component (Theorem 7.5). In an RCM, we know from Theorem 7.8 that infinite range models have at most one unbounded component a.s. As already noticed, it is not hard to find examples of a Boolean model or RCM


<!-- p:215 -->


Figure 7.7. The first iteration in the construction of two stationary 'parallel' trees. It is clear how to generalise this to any finite number of trees.

where infinitely many unbounded components arise a.s. The point of the examples above is that they give rise to Boolean models or RCMs with multiple but finitely many unbounded components.

First, consider the construction in Example 7.5. Suppose that the distance between successive points on the trees is € &gt; 0 and that the distance between the different trees is δ with δ &gt; €. Consider a Boolean model driven by this point process, and where the radius random variable ρ satisfies P(ρ = ε) = 1. It is then clear that each tree in the construction gives rise to exactly one unbounded vacant component and also that the unbounded components corresponding to different trees are disjoint. Hence we have created a Boolean model with two unbounded occupied components. Generalisation to any finite number of unbounded components is clear. We remark that a Boolean model with fixed radii is in fact an RCM too. Thus this also gives an example of an RCM with two unbounded components.

A small variation of the construction in Example 7.4 may be used to create an example of a Boolean model where the radii are bounded from above but not from below, such that the model has two unbounded occupied components a.s. (and, according to Theorem 7.5, only one unbounded vacant component). The idea is the following. The trees have line segments of increasing lengths l1, l2, ... say. Depending on the precise distribution of ρ we put, on each line set ind  n (ds  sn       hast the whole line segment is contained in the union of all balls centred at these points is at least 1 — 2−". Starting at an arbitrary point on a tree there is a unique sequence of line segments along which we can radiate to infinity starting at that point. Denote this sequence by In, In2, .... From the Borel-Cantelli lemma it follows that with probability 1, all line segments ln are covered by balls for k sufficiently large. Thus each tree gives rise to at least one unbounded component. A little thought reveals the conclusion that each tree can give rise to at most one unbounded component and we conclude that, in this Boolean model, exactly two unbounded occupied components exist a.s.


<!-- p:216 -->


### 7.8 Notes

The material in Section 7.2 is taken from Meester and Roy (1994). The topological structure of unbounded components in two dimensions is based on Burton and Keane (1989, 1991). The results in Section 7.4 are improved versions of results in Meester and Roy (1994), and the results in Section 7.5 are taken from Burton and Meester (1993). Cutting and stacking goes back to Rudolph (1979), and the examples constructed using this technique are from Meester and Roy (1994).


<!-- p:217 -->


8

## Other continuum percolation models

This chapter is devoted to a miscellany of random processes related to the models discussed so far. Some of these models have been studied quite extensively but others are new. Consequently, there are many open questions in these models and we hope that this small survey will initiate research in this direction.

### 8.1 Continuum fractal percolation

There is a natural way to construct fractal like sets with countably many Boolean models. Take λ &gt; 0 and consider the two-dimensional Boolean models (Xk, 21−k, 4k−1λ), for k = 1, 2, . . . . The reason for this particular choice of the parameters will become clear as we proceed, but note at this stage that the covered volume fraction (CVF) of all these Boolean models is the same. (For the definition of the CVF, see Chapter 5.) Now denote by Vn the vacancy which remains after the superposition of the first n Boolean models. We denote this superposition by (Yn, ρn, λn). Obviously, we have V1  V2  V3  .. . and we define the limit by

k=i

-nt   st a t t i i t     i n deed, the CVF of a model is equal to the probability that a particular point in the plane is covered. If we denote the CVF of an individual Boolean model (Xk, 21−k, 4k-1λ) by α, then the probability that the origin is in Vn is equal to (1 — α)"; see Chapter 5. Thus the probability that the origin is in V∞ is zero. But now we cannot, as in the proof of Proposition 3.1, conclude that the whole plane is covered a.s. The point is that this time infinitely many balls are centred in the unit square a.s. and as such we do not have local finiteness and the argument in the proof of Proposition 3.1 breaks down. In fact, as we shall see now, if λ is sufficiently small, the vacant region is not empty a.s.


<!-- p:218 -->


Proposition 8.1 If λ &gt; 4 log 4, then V∞ = ∅ a.s.

$$P r o p o s i t i o n \, 8 . 2 \ \ I f \lambda < \frac { \log 4 } { 4 5 } , \, t h e n \, V _ { \infty } \neq \emptyset \, a . s .$$

Proof of Proposition 8.1 The proof proceeds by a simple branching process argument. Consider the unit square I2, say, and divide I2 into four smaller squares with side length . The 0-th generation is just 12, and the first generation of our branching process are those squares S among the four subsquares for which X1(S) = 0. Note that whenever X1(S) ≥ 1, the whole square S is covered. Hence the union of the squares in the first generation contains the vacant region in (X1, λ, 1). Note also that the probability that a particular subsquare is in the first generation is equal to exp(—λ/4).

Each of the subsquares in the first generation is now divided into four further subsquares with side length À. Such a further subsquare S is in the second generation if and only if X2(S) = 0. This happens with probability exp(—4λ/16) = exp(-λ/4). It is clear that different squares in the first generation give birth to members in the second generation independently of each other. Thus we have constructed a branching process in such a way that whenever this process becomes extinct, there is no vacancy left in the original model. Extinction takes place a.s. whenever the expected number of members in the first generation is less than 1; i.e. if 4exp(−λ/4) &lt; 1, i.e. if λ &gt; 4 log 4. □

Proof of Proposition 8.2 This result can also be proved by a branching process argument. This time we shall construct a branching process in such a way that if this process survives, then V∞ ≠ Ø. To this end, consider again the unit square I2 and suppose that X1(I2) = X2(I2) = 0. This happens with positive probability. As before, the 0-th generation of our branching process consists of 12 only. The first generation consists of those squares among [0, †] × [0, ‡], [0, ‡] × [, 1], [λ, 1] × [0, ‡] and [, 1] × [, 1] (i.e. all 'corner subsquares' of 12) which are not intersected by any ball coming from X3 or X4. The probability that e.g. [0, ‡] × [0, ‡] is in the first generation is at least as large as the probability that there is no point of X3 and X4 in [−1, 2] × [−1, 21. This λ) exp(-64λ probability is equal to exp(−16λ 16) = exp(-45λ). The other 9 corner squares are in the first generation with the same probability.

Now each of the squares of the first generation is divided into 16 subsquares and the second generation consists of those corner squares' among these which are not intersected by any ball coming from X5 or X6. The probability that this happens is the same as in the corresponding event described above. Also note that members of the first generation give birth to members of the second generation independently of each other. We continue in the obvious way. Now observe that if this branching process survives, we have a non-increasing sequence A1 A2  ... of non-empty compact sets such that An ⊆ Vn for all n. This implies that V∞  ∩n≥1An ≠ ∅ by Cantor's intersection theorem. Survival is possible with positive probability if 4 exp(—45λ) &gt; 1, i.e. λ &lt; log 4/45. A reader concerned with details will notice that in the statement of the proposition we claim that V∞ is not empty a.s. To see that this stronger statement is also true, we divide the plane into unit squares and consider a sequence I1, I2, . .. of such squares such that d(Ij, Ik) &gt; 4 for all j ≠ k (to guarantee independence). Now P(V∞ ∩ Ij ≠ Ø) is positive and independent of j whence P(V∞ ≠ 0) = 1.


<!-- p:219 -->


From a percolation point of view we are interested in the existence of large connected components of V∞. So our next task is to show that large components do indeed exist. To this end, we define a new critical density λf (the f' refers to 'fractal') as follows:

Definition 8.1 Let θf(λ) be the probability that V∞ ∩ [0, 1]2 contains a connee     s     n t as

$$\lambda _ { f } = \inf \{ \lambda \, \colon \, \theta _ { f } ( \lambda ) = 0 \} .$$

Note that λf is defined in terms of crossing probabilities like λs and λ in Chapters 3 and 4. We shall see later that λf is strongly related to the classical critical densities in the ordinary Poisson Boolean model. Our first task is to show that λf is not equal to zero.

Theorem 8.1 λf &gt; 0.

Proof The idea of the proof is related to the proof of the well-known extinction theorem for branching processes. First we define the notion for the unit square I2 to be m-good, for all m ≥ 0. We assume that X1(I2) = X2(I2) = X3(I2) = X4(I2) = 0, something which happens with positive probability. We divide the unit square into 256 subsquares which we shall call level-1 squares. We say that 12 is 0-good if at least 255 of these level-1 squares do not contain any point of Xs, X6, X7 and Xg. A level-1 square which does not contain any such point will be called empty. We further divide each empty level-1 square into 256 level-2 squares. An empty level-1 square is called 0-good if at least 255 of its level-2


<!-- p:220 -->


subsquares do not contain any point of X9, X10, X11 and X12. The unit square is said to be 1-good if it contains at least 255 0-good level-1 squares. Inductively, the unit square is called m-good if at least 255 of its 256 level-1 subsquares are (m — 1)-good. We denote the probability that the unit square is m-good by θm(λ).

The idea behind these definitions is the following. If the unit square is O-good, then it is an easy matter to check that each side of the unit square touches at least five level-1 squares which are completely vacant (with respect to Yg). (Note that the diameter of the balls associated with X5 is 16.) The same statement, s s  ss  sus - - ss s ss es ues adjacent if they share a side. A path of squares is a finite sequence of squares S1, S2, . .. , Sk such that Si and S+1 are adjacent for all i = 1, ... , k — 1. If both [0, 1]2 and [1, 2] × [0, 1] are 0-good, then there exists a connection from {0} × [0, 1] to {2} × [0, 1] (inside the rectangle) of adjacent vacant (w.r.t. Yg) level-1 squares. It is now easy to show inductively that if the unit square is m-good, then there is a path of vacant (with respect to Y4(m+2)) level-m squares connecting the left and right sides of the unit square. Thus if I2 is m-good for all m = 1, 2, ..., then we can find a non-increasing sequence of connected compact sets Am with the properties that (i) Am ⊆ Vm, and (ii) Am intersects the left and right sides of I2. It follows immediately that V∞ ≠ Ø in such a case. It therefore suffices to show that if λ is sufficiently small then

$$\lim _ { m \to \infty } \theta _ { m } ( \lambda ) > 0 .$$

To prove this, let p := exp(-85λ) be the probability that a level-m square is empty (i.e. does not contain a point of X4m +1, X4m+2, X4m+3 and X3m +4.). Writing θm as a function of p rather than of λ we obtain by definition:

$$\theta _ { m } ( p ) = 2 5 6 p ^ { 2 5 5 } ( 1 - p ) ( \theta _ { m - 1 } ( p ) ) ^ { 2 5 5 } + \\ + p ^ { 2 5 6 } ( 2 5 6 ( \theta _ { m - 1 } ( p ) ) ^ { 2 5 5 } ( 1 - \theta _ { m - 1 } ( p ) ) + ( \theta _ { m - 1 } ( p ) ) ^ { 2 5 6 } ,$$

for m ≥ 1, and

$$\theta _ { 0 } ( p ) = p ^ { 2 5 6 } + 2 5 6 p ^ { 2 5 5 } ( 1 - p ) .$$

Define ψp(x) = p255x255(256 − 255 px). It then follows that

$$\theta _ { m } ( p ) = \psi _ { p } ^ { m + 1 } ( 1 ) ,$$

for all m ≥ 0. It is easy to check that ψp(x) is increasing in both p and x. It follows that limm→∞ θm(p) is equal to the largest fixed point of ψp in [0, 1]. We need only to show now that for p sufficiently large but smaller than 1 (which means for λ sufficiently small but positive) the largest fixed point of ψp in [0, 1]


<!-- p:221 -->


is larger than zero. This, however, follows from the fact that ψı(1) = 1 and (d/dx)ψ1(x)|x=1 = 0. □

We shall now formulate a relation between ordinary' Poisson Boolean models and the fractal model of this section. Fix some n ≥ 0 and consider the (independent) Poisson Boolean models

$$( X _ { 1 + ( i - 1 ) n } , 2 ^ { - ( i - 1 ) n } , 4 ^ { ( i - 1 ) n } \lambda ) ,$$

for i = 1, 2, .. . , defined on the same probability space. The i-th model will be denoted by Z(n) and when there is any chance of confusion the probability measure in that model will be denoted by Pz(n). Note that Z1(n) is just (Xt, 1, λ) for all n. Also observe that Z+1(n) can be obtained from Z (n) by scaling with a factor 2−". We shall denote the vacant region in Z(n) by Vi (n). Instead of looking at V∞, we now concentrate on

$$\bigcap _ { i = 1 } ^ { \infty } V _ { i } ( n ) = \colon V ( n ) .$$

The reason for doing so is that when n gets larger, Z1 (n) will be more and more dominant so that V (n) will be more and more like V1(1). But V1 (1) is equivalent in law to the vacant region in the Boolean model (X, 1, λ) and this will give the relation between the critical densities for fractal percolation and λ*(1). To make this precise, let θ(n) (λ) be the probability of a vacant L-R crossing of the unit square in V (n), and define

$$\lambda _ { f } ( n ) = \inf \{ \lambda \ \colon \theta _ { f } ^ { ( n ) } ( \lambda ) = 0 \} .$$

Theorem 8.2 limn→∞ λf(n) = λ*(1) (= λc(1)).

Proof First we prove that

$$\lambda _ { f } ( n ) \leq \lambda _ { c } ( 1 )$$

for all n. Recall that σ((m, m), λ, 1) is the probability of an occupied L–R crossing of the square [0, m]2 in the Poisson Boolean model (X, 1, λ). Fix λ &gt; λc(1). From Corollary 4.1 we have that

$$\lim _ { m \to \infty } \sigma ( ( m , m ) , \lambda , 1 ) = 1 .$$

Consider the event E, = {there is an L-R occupied crossing of the unit square in Z(n)}. A simple scaling argument gives

$$P ( E _ { i } ) = \sigma ( ( 2 ^ { ( i - 1 ) n } , 2 ^ { ( i - 1 ) n } ) , \lambda , 1 ) .$$


<!-- p:222 -->


From (8.3) and the independence of the events E we have that

$$P ( \lim \sup _ { i \to \infty } E _ { i } ) = 1 .$$

By symmetry, this is also true if we consider T-B occupied crossings instead of L-R crossings. So infinitely many models Z (n) (for fixed n) have occupied

The other inequality is harder, and we concentrate first on the ordinary Poisson Boolean model (X, 1, λ). Fix some λ &lt; λc(1), let RM be the rectangle [0, 3M] × [0, M] and let DM be the square [0, M]2. Using the FKG inequality and Corollary 4.1 we see that for all €1 &gt; 0, the following event EM,η = {there is a path of vacant squares of side length η crossing R from left to right and two such T–B crossings in Dm and DM + (2M, 0), respectively} satisfies

$$P ( E _ { M , \eta } ) > 1 - \epsilon _ { 1 } ,$$

for M sufficiently large and η sufficiently small. Next we choose n so large that 2−" &lt; η and such that 2" = (2kn + 1)M for some integer kn. We divide D2 into squares of side length M and we denote by IM,n the set of vertices {(M/2, M/2) + (2Mi, 2M j)}, where i, j ∈ Z. We connect any two vertices v and v' in IL M,n if and only if d(v, v') = 2M. We now perform bond percolation on the ensuing lattice (also to be denoted by I M,n), declaring a bond to be open if the event EM,η, properly translated and rotated, occurs in the union of the three squares which intersect the bond. If this is not the case, the bond is said o o  d     ds which do not have an end point in common are independent. Now let FM,n be the event that there is an L-R crossing of D2 in IM,n of open bonds, i.e. a crossing from a vertex in {(i, j) ∈ I M,n : i = M/2} to a vertex in {(i, j) ∈ IL M,n : i = (2n /M) − (M/2)}. It is clear from the construction that the occurrence of the event FM,n implies that there is an L-R vacant crossing of D2 in the underlying Poisson Boolean model (X, 1, λ). To estimate P(FM,n) we introduce the dual lattice Ld. M,n which is just the lattice LM,n translated over the vector (M, M). Each bond in the dual lattice intersects one bond of the original lattice and a bond in the dual is declared open if and only if the intersecting bond is open, and closed otherwise. Now FM,n does not occur if and only if there a closed T–B crossing of [M, 2n − M] × [−M, 2n + M] in the dual (see Section 1.2 in Chapter 1). The probability of the latter event can be estimated by counting arguments as in Chapter 1: each such T-B crossing starts from any of the (2n — M)/(2M) vertices at the bottom and must contain at least (2n + M)/(2M) bonds. Furthermore, the number of distinct paths of length k is at most 3k. Finally, the state of a bond in the dual depends on the state of only six other bonds in the dual and the geometry of this dependence structure is such that any path of length k in the dual contains at least [k/4 bonds which are mutually independent. Putting these observations together gives


<!-- p:223 -->


$$M ( F _ { M , n } ) & \geq 1 - \frac { 2 ^ { n } - M } { 2 M } \sum _ { k \geq \frac { 2 ^ { n } + M } { 2 M } } 3 ^ { k } \epsilon _ { 1 } ^ { k / 4 } \\ & = 1 - \frac { 2 ^ { n } - M } { 2 M } \frac { ( 3 \epsilon _ { 1 } ^ { 1 / 4 } ) ^ { ( 2 ^ { n } + M ) / ( 2 M ) } } { ( 1 - 3 \epsilon _ { 1 } ^ { 1 / 4 } ) } . \\ \intertext { w e r u t h e f r a c l a l p e r a l l }$$

Now we return to the fractal model. Recall that we have chosen λ &lt; λc(1). It suffices to show that for all n sufficiently large V (n) contains an L-R crossing of the unit square with positive probability.

Assume that [0, 1]2 is completely vacant in V1. This happens with positive probability and is just for convenience. Scaling (8.4) and (8.5) yields

$$P _ { Z _ { i } ( \mathfrak { n } ) } ( E _ { M / 2 ^ { ( i - 1 ) \mathfrak { n } } , \eta / 2 ^ { ( i - 1 ) \mathfrak { n } } } ) > 1 - \epsilon _ { 1 }$$

PZ2(n) (there is a vacant L-R crossing of the unit square)

$$& \geq 1 - \frac { 2 ^ { n } - M } { 2 M } \frac { ( 3 \epsilon _ { 1 } ^ { 1 / 4 } ) ^ { ( 2 ^ { n } + M ) / ( 2 M ) } } { ( 1 - 3 \epsilon _ { 1 } ^ { 1 / 4 } ) } \\ & = 1 - h M , n ( \epsilon _ { 1 } ) , \text { say} .$$

The lattice construction above can also be carried out, suitably scaled, in any of the models Z(n). Suppose vacant paths as in the definition of the event EM/2" , η/2 exist, and let G3 (n) be the event that inside these paths, there is a path oot t   o s ssns re t s  s o o the model Z3(n) has been placed'. To estimate P(G3(n) | EM/2n) we perform a similar discretisation as above, suitably scaled. For the counting argument, note that the path in the event EM/2",η/2 consists of at most 3M2 squares. There are, on either side of the path, at most 3M2[(2" — M)/(2M)} vertices in the dual which are adjacent to an edge in the dual crossing an edge of the path. In order for G3(n) not to occur, one of these vertices in the dual has to be the starting point of a path of at least (2n + M)/(2M) closed edges. A similar calculation as above now yields

$$P ( G _ { 3 } ( n ) \, | \, E _ { M / 2 ^ { n } , \eta / 2 ^ { n } } ) & \geq 1 - 3 M ^ { 2 ^ { n } - M } \, \frac { ( 3 \epsilon _ { 1 } ^ { 1 / 4 } ) ^ { ( 2 ^ { n } + M ) / ( 2 M ) } } { 2 M } \, \frac { ( 1 - 3 \epsilon _ { 1 } ^ { 1 / 4 } ) } { ( 1 - 3 \epsilon _ { 1 } ^ { 1 / 4 } ) } \\ & = 1 - g _ { M , n } ( \epsilon _ { 1 } ) , \, \text {say} .$$

and Hence from (8.6) we find


<!-- p:224 -->


$$P ( G _ { 3 } ( n ) ) & \, \geq \, ( 1 - \epsilon _ { 1 } ) ( 1 - g _ { M , n } ( \epsilon _ { 1 } ) ) \\ & \geq \, 1 - \epsilon _ { 1 } - g _ { M , n } ( \epsilon _ { 1 } ) \\ & = \colon 1 - \epsilon _ { 2 } .$$

So the probability that in the superposition of Z2(n) and Z3(n) there is a vacant crossing of RM/2n by squares of side length 2-2n is at least 1 —€2. This statement can be scaled properly so as to yield a similar statement about the superposition of Z (n) and Z+1 (n) and suitable crossings in suitable rectangles. Define Gk (n) as the event that in the superposition of Z2(n), Z3(n), . .. , Zk(n) there exists a path of vacant squares of side length 2(k–1)n crossing RM/2n from left to right. Choosing

$$\epsilon _ { k + 1 } \colon = \epsilon _ { 1 } + g _ { M , n } ( \epsilon _ { k } )$$

for all k ≥ 1 we conclude that

$$P ( G _ { k } ( n ) ) \geq 1 - \epsilon _ { k - 1 }$$

for all k ≥ 2. Thus the probability of a vacant L-R crossing of the unit square in Vk(n), given that the unit square is contained in V1 is bounded from below y  d e    -    s  e by ∈k.

To complete the proof we again perform an iterative procedure. Take €1 such that 3(2€1)1/4 &lt; 1. Now choose some M and η and choose n so large that gM,n(2ε1) &lt; €1 and such that hM,n(2€1) &lt; 1. (The reader may check easily that this can be done.) The function gM,n is non-decreasing and so is the function ψ(x) := ∈1 + gM,n(x). Note that

$$\epsilon _ { k + 1 } = \psi ( \epsilon _ { k } )$$

for all k ≥ 1. From the choice of ∈1 we have that ψ(€1) &gt; €1 and ψ(2€1) &lt; 2€1, whence ψ has a fixed point in the interval (€1, 2€1). It follows that ∈ :== limk→∞ €k exists and is contained in (€1, 2∈1). Hence V (n) contains a vacant L-R crossing of the unit square with probability at least 1 – h M,n (2€1) &gt; 0.

□

### 8.2 Percolation of level sets in random fields

Imagine a hilly landscape and a certain level h, say. The level h is supposed to rypr, y    a sea e    e ly.. one expects that if h is sufficiently small, then there are only bounded lakes of water and an infinite land mass; if h is large enough, then there should be only bounded islands in an infinite ocean.


<!-- p:225 -->


To formulate this model mathematically, we consider a stationary, ergodic, a.s. continuous random field {ψ(x) : x ∈ IRd}. We shall always assume that Eψ(x) = 0 for all x ∈ IRd. We define level sets as follows:

$$S _ { h } = \{ x \, \colon \psi ( x ) = h \} ,$$

$$S _ { \leq h } = \{ x \colon \psi ( x ) \leq h \} ,$$

for all h ∈ IR. As usual, we say that a subset of IRd percolates if it contains an unbounded connected component. In analogy with the percolation models discussed in this book we may define

hc = hc(ψ) = inf{h : S≤h percolates with positive probability}.

Note that if S≤h percolates with positive probability it percolates almost surely by ergodicity.

First we shall give a condition under which he(ψ) is bounded away from infinity. This is the analogue of Theorem 1.1 in Chapter 1 and, as we shall see, the proof proceeds very much along the same line. In order to formulate the condition for non-triviality of he, we discretise Ra in the usual way: the space is partitioned into unit cubes B1, B2,. .., where Bi = zi + (−1, ]d, for an enumeration {z} of the vertices in Za.

Theorem 8.3 Suppose that there exists a non-increasing function g : IR → IR such that g(h) ↓ 0 as h → ∞ and a constant c = c(h) &gt; 0 such that for any subset {Bi1, Bi2, . .. , Bik} of unit cubes

$$P \left ( \bigcap _ { j = 1 } ^ { k } \{ \max _ { x \in B _ { j } } \psi ( x ) \geq h \} \right ) \leq c ( h ) \{ g ( h ) \} ^ { k } .$$

Then hc(ψ) &lt; ∞.

Proof Consider the random field {φ(z) : z ∈ Zd} defined as

$$\phi ( z _ { i } ) = \max _ { x \in B _ { i } } \psi ( x ) .$$

We say that a vertex z is h-open if φ(z) ≤ h and h-closed otherwise. If we can show that for h large enough, there is (discrete) site percolation of h-open vertices, then it follows from the a.s. continuity of ψ that h.(ψ) &lt; ∞.

and It follows from (8.10) that for every finite subset {z1, . .. , zk} of vertices


<!-- p:226 -->


$$P \left ( \bigcap _ { i = 1 } ^ { k } \{ \phi ( z _ { i } ) \geq h \} \right ) \leq c ( h ) \{ g ( h ) \} ^ { k } .$$

To show that this implies that h-open percolation occurs in φ for h sufficiently large, we need to introduce the notion of so-called *-connections in Zd. This is the analogue of the dual graph in bond percolation (see Chapter 1). Two vertices z and z′ are *-neighbours if {z − z′| ≤ √♂. Note that each vertex has 3a — 1 *-neighbours. We can define *-paths and *-clusters in the obvious way with this new connection rule. Now it can be seen that there is no h-          i  d connected sets 'surrounding'the origin. (Here 'surrounding' means that the origin is cut off from infinity from the percolation point of view.) Now we perform a counting argument as in the proof of Theorem 1.1. Let E be the event that there is a h-closed *-connected set of n vertices surrounding the origin. For each such set of n vertices, the probability that it is h-closed is at most c(h){g(h)}", using (8.11). There are at most n(3d − 2)n - 1 such sets whence P(En) ≤ n(3d − 2)n-1c(h){g(h)}n. Now choose h so large that g(h) &lt; (3d − 2)−1. Then ∑ P(En) &lt; ∞ and h-open percolation occurs a.s. □

mhot   er ass  r   e  a est ous special case is a random field with finite correlation radius. This means that there exists an R &gt; 0 such that for any collection A1, ..., An of bounded measurable sets with inf {d(x, y) : x ∈ A, y ∈ Aj} &gt; R whenever i ≠ j, the σ-algebras generated by the values of ψ(x) on these sets are independent.

Corollary 8.1 A stationary random field ψ with finite correlation radius has hc(ψ) &lt; ∞.

Proof Let F be the distribution function of maxx∈B, ψ(x). From the continuis   lt   ←   ← xt t  o st  oit unit cubes contains at least k/(2R + 3)d cubes whose σ-fields are indepedent. Now apply Theorem 8.3 with c(h) = 1 and g(h) = (1 − F(h))1/(2R+3)d . □

Another application of Theorem 8.3 can be found in the theory of stationary Gaussian random fields. If the correlations in such a field decay sufficiently fast, then it is possible to show that (8.10) holds. The correlation function R in a random field ψ is defined as R(x) :== E(ψ(0)ψ(x)). We give the next result without proof.


<!-- p:227 -->


Theorem 8.4 Let ψ be a stationary Gaussian field and suppose there exists a non-increasing function f : R → IR satisfying ∫∞ xd−1 f(x)d x &lt; ∞ such that for some positive constants c

- (|x|)1  |(x)| (|x|)  |(x)(| (1)
- ∂2R (ii) ≤ c2f(|x|), xexe
- (iii) |1 − R(x)| ≤ log -(3+δ) 1 for some δ &gt; 0 and for all |x| &lt; 1. |x|′

Then (8.10) is satisfied for suitable g and hence hc(ψ) &lt; ∞.

We continue the discussion with a different class of random fields in two dimensions. Let G denote either the square lattice or the triangular lattice (see the last section of Chapter 3) with bonds of length 1. Let {xi : i = 1, 2, . . .} be the set of vertices of G. Let {Ai : i = 1, 2, . . .} be a sequence of i.i.d. random variables with zero mean. Finally, let φ : IR → IR satisfy ∫R xφ(x)dx &lt; ∞. The latter condition is just to guarantee that the model is non-trivial. Now define a random field ψ on IR2 as

$$\psi ( x ) = \sum _ { i = 1 } ^ { \infty } A _ { i } \phi ( | x - x _ { i } - U | ) ,$$

where U is a random vector uniformly distributed over a particular face of G. (The vector U is only there to make sure that ψ is stationary and it has no effect on the important features of the realisations.) This type of random fields has received some attention in the physics literature; see the references in the Notes. Apart from questions concerning the non-triviality of hc(ψ), the behaviour in the subcritical regime has been an object of research. Here some interesting phenomena can occur. In Boolean models with bounded radii we showed that the phase transition is sharp in the sense that if there is no percolation, then the distribution function of the size of the components of the origin goes down exponentially fast. It turns out that this need not be the case here. To describe this, we specialise to the case in which P(A1 = 1) = P(A1 = −1) = 12 and φ is a smooth, strictly decreasing and strictly convex function with support [0, λ + €] with φ(0) = 1, where € &gt; 0 is chosen such that balls centred at the sites of G with radius 2 + € intersect only pairwise.

Theorem 8.5 If G is the triangular lattice, we have

$$h _ { c } ( \psi ) = 2 \phi ( \frac { 1 } { 2 } ) ,$$


<!-- p:228 -->


and for all h with |h| &lt; hc(ψ) we have

$$P ( d ( S _ { h } ) \, > \, t \, | \, \psi ( 0 ) = h ) \geq c _ { 1 } ( h ) t ^ { - \alpha } ,$$

for positive constants c1(h) and α where α does not depend on h and d(·) denotes diameter of a set. If G is the square lattice, we have

$$h _ { c } ( \psi ) = 0 ,$$

$$P ( d ( S _ { h } ) > t \, | \, \psi ( 0 ) = h ) \leq c _ { 2 } e ^ { - c _ { 3 } t } ,$$

for positive constants c2 and c3.

The different behaviour for the triangular and square lattice is due to the different geometry of the lattices: in discrete percolation on the triangular lattice, a finite open cluster is surrounded by a closed circuit. On the square lattice, however, a finite open cluster is surrounded by a closed *-cluster, as noted in the proof of Theorem 8.3.

Partial proof of Theorem 8.5 Consider first the case where G is the triangular lattice. The critical probability for independent site percolation on the triangular lattice is ¿, and there is no percolation at criticality (see Kesten 1982) whence the origin is surrounded by infinitely many disjoint open and infinitely many disjoint closed circuits. We can perform independent site percolation by declaring the site xi to be open if and only if A = 1 and closed otherwise. Note that it follows from the convexity of φ that for any bond b connecting two plus sites (i.e. sites xi with Ai = 1), inf xeb ψ(x) = 2φ(). This implies immediately that for h &lt; 2φ(), S≤h cannot cross an open circuit and hence does not percolate. Conversely, each face of the lattice contains a region where ψ (x) = 0, and it is nol   s n t   (  &lt;    s   tes are connected in S≤h. This implies that he(ψ) = 2φ().

To prove the corresponding result when G is the square lattice, we note that ion rod   s  nai ai  t i s n te ii ti l lt   tt ite iis se i lr for *-percolation satisfies Pc + p* == 1 (see Notes). This means that there are infinitely many *-circuits of either type surrounding the origin, but only finitely many ordinary circuits of either type. Now let h &lt; 0. Given a plus *-circuit we can, by transforming the bonds slightly so as to avoid balls centred at minus vertices, find a curve through the same faces and vertices as the *-circuit such that ψ(x) ≥ 0 on the curve. The sets S≤h cannot cross such curves and hence S≤h does not percolate. Conversely, it is not hard to see that a component of So

and for all h ≠ 0, can only be bounded if it is surrounded by a plus or minus circuit in the lattice. As observed above, there are only finitely many such circuits surrounding the origin and we conclude that So, and thus also S≤o percolates.


<!-- p:229 -->


To give the idea behind the proof of the two remaining statements, note that is critical for independent site percolation on the triangular lattice, but subcritical for independent site percolation on the square lattice. As a result of this, if C denotes the cluster of the origin in either model (so depending on the state of the origin, C is a plus or a minus cluster), the function P(|C| ≥ n) goes down (when n → ∞) only polynomially in the triangular lattice, but exponentially in the square lattice. The idea of the proof is now to relate the size of the level set of the origin to the cluster C in the coupled discrete percolation model. For the square lattice this is quite simple, as for h ≠ 0, the level set Sψ(0) which contains the origin is contained in Ux∈C0 S(x,  + ε). For the triangular lattice, the proof is a little more involved and we do not give it here. (See references in the Notes.) 0

### 8.3 Dependent Boolean and random-connection models

In the standard Poisson Boolean model, each point of a Poisson point process X with density λ &gt; 0 is the centre of a ball with random radius. Radii of different balls are independent of each other and all radii are independent of X. In this section, we introduce a stationary (and ergodic) model where the radii are no longer independent of each other and the point process.

We start with a Poisson process in IRa with density λ. In the model the density turns out to be irrelevant (as can be seen by a simple scaling argument) and we take it to be equal to 1. Choose an integer k ≥ 1, the parameter of the model. The configuration of balls in space is constructed dynamically as follows. At time 0, all points of X are the centre of a ball with radius 0. Then, as time t evolves, the radius of each ball grows linearly in t, and all radii grow with the same speed. Balls start intersecting each other while growing and each ball remembers with how many balls it has non-empty intersection. As soon as a ball hits the k-th ball, it stops growing forever. Thus at each time t the space is pad         o   icd we call the vacant region. Let C (k) be the occupied region at time t. We are interested in the limiting configuration Ca (k) defined as

Note that it is not completely obvious that this model exists, in the sense that Ca (k) can actually be constructed this way for all values of t. The problem is that at any time, a ball might need 'information from infinity' to decide whether or not it can continue growing. Actually, the argument in Case 2 in the proof of Theorem 8.6 below can easily be modified as to obtain an existence proof. We do not elaborate this here and refer to the references in the Notes.


<!-- p:230 -->


From a percolation point of view we are interested in the existence of unbounded connected components in Cd(k). If these exist, we say that Cd (k) percolates. Let us define the critical k as kc(d) := min{k ≥ 1 : Cd(k) percolates with positive probability}. The parameter space in this model is discrete and this gives us some hope that ke(d) might be computed explicitly. We shall prove the following estimate:

Theorem 8.6 For all d ≥ 2, it is the case that

2 ≤ kc(d) &lt; ∞.

The fact that kc(d) &lt; ∞ follows from Theorem 8.7 below. Therefore we only prove the first inequality here. From now on, k = 1 and we shall prove that Ca (1) does not percolate a.s. The argument will be dimension free, so we write C := Cd (1) and Ct := Cd (1) from now on.

It will be convenient to define a graph T as follows. The vertices of T are the occurrences of X and two points x and y are neighbours (to be denoted n   t    x      ( x yv non-empty intersection). To say that C percolates is the same as to say that T contains an infinite component (in the usual graph-theoretical sense). We say that the point x is smaller than y (notation: x &lt; y) if the ball centred at x has smaller radius than the ball centred at y. We define the relation ≤'between points of X in the obvious way.

Lemma 8.1 With probability 1, each point x of X has at most one neighbour y for which y ≤ x.

Proof The only way for a ball to get a neighbour with the same radius is to hit each other while both are still growing. This obviously implies that a ball can have at most one such neighbour and in such case has no smaller neighbours.

The only way for a ball to get a smaller neighbour is to hit a ball which already stopped growing before. Hence it suffices to show that it is a.s. impossible that a     s  o  s   rn a one way of seeing this is the following. Select two points x and y of X and wait until they both stop growing. Suppose this happens at time to. Consider the union of the components in Ct containing x and y and denote this union by W. Given W, the point process X outside the region W′ := {x ∈ IRd : |x − W| ≤ t0} is still unconditioned. But all potential balls which might hit W at two different balls at the same time are centred outside W'. Note that W consists of the union of finitely many balls and the set of points outside W' which have the same distance to two or more balls of W has Lebesgue measure zero. Hence the s     x i st sil  at l larger ball is zero.


<!-- p:231 -->


It follows from Lemma 8.1 that T is almost surely a forest, i.e. its components are a.s. trees. To see this, note that if T contains a circuit, then this circuit has to contain a largest point (i.e. a point with largest associated radius), which leads to a contradiction if we consider the two neighbours of this point in the circuit. Furthermore, two tangent balls in C have the same radius if and only if they stop growing at the same time, i.e. when they hit each other. We call two such balls a root. It follows from Lemma 8.1 that any component in C can contain at most one root a.s. To see this, suppose there is a component with two roots. It is obvious that the two roots have different associated radii a.s. The balls in the larger root can, according to Lemma 8.1, only have larger neighbours and such a neighbour can again only have larger farther neighbours and so on. Hence a path to the smaller root cannot exist a.s.

Proof of Theorem 8.6 We shall derive a contradiction by assuming that C percolates with positive probability. An unbounded component in C either contains a root or does not contain one. We rule out both possibilities separately:

CAsE 1: Suppose that with positive probability (and hence with probability 1 by ergodicity) C contains an unbounded component W with a root. As remarked above, W contains exactly one root a.s. in such a situation. We call the point of intersection between two balls of a root contained in an unbounded component an encounter point. If encounter points exist, then there has to be a density μ &gt; 0, say, of such points in space. Then, for all K &gt; 0 there exists a number Nk such that the following event E han t  t  t t   :t   i ter point and the associated unbounded component contains at least K points in BNk}, where Bn denotes the box [−n, n]d. For z ∈ Zd, the event E(z) is defined by replacing B1/2 and BNK by z+ B1/2 and z+ BNK, respectively. It follows from the ergodic theorem that for M sufficiently large (depending on the realisation) the box BM contains at least (μ/4)(2M)a cubes of the form z + B1/2 for which E(z) occurs and for which z + BNk ⊆ BM. However, the sets of K points associated with the different encounter points are mutually disjoint whence


<!-- p:232 -->


$$X ( B _ { M } ) \geq \frac { \mu } { 4 } ( 2 M ) ^ { d } .$$

On the other hand, the ergodic theorem implies that for all M large enough

$$X ( B _ { M } ) \leq 2 ( 2 M ) ^ { d }$$

(remember that λ = 1 throughout). Taking K &gt; 8μ−1 now gives the required contradiction.

CASE 2: Next we rule out the possibility of unrooted unbounded components. First note that an unrooted component cannot contain a smallest point as this point would be one of a root. Also, a point cannot have only neighbours which are all strictly larger than the point itself. Hence every point has at least one neighbour which is strictly smaller than the point itself, and we conclude that any unbounded unrooted component contains an infinite sequence of tangent balls with strictly decreasing radii. The radii in such a sequence approach a limit α, say, which is random. Note however that the set Γ of possible limits a   w  a w  w    s?

First suppose that 0 ∈ Γ. This would imply that for every € &gt; 0, the standard Poisson Boolean model with balls of fixed radius € percolates for λ = 1. However, for € sufficiently small λ = 1 is subcritical (see Chapter 3) and we have a contradiction. Next suppose that for some β &gt; 0 we have β ∈ Γ. We can assume that there is a Poisson point at the origin. Then, for all ∈ &gt; 0 there is a positive probability that the radits of the ball at the origin is in (β, β + ε) and that this ball is one of an infinite chain of tangent balls with decreasing radii which are all at least β. We shall now prove with a branching process argument that this is impossible. Denote the ball centred at x with radius r by S(x, r). First, we choose ∈ &gt; 0 so small that the annulus A(2β, 2€) := S(0, 2β + 2€)\S(0, 2β) has d-dimensional Lebesgue measure less than 1. We are going to construct a Poisson process with density 1 in IRa step by step as follows. First consider a Poisson process X with density 1 restricted to A(2β, 2€). The expected number of points of X1 is at most one by construction. If there are no points we stop, otherwise denote the points by x1, ..., xn. Now we concentrate on x1 first and consider a Poisson process X2 (independent of X     \y       e denoted by x1,1, ..., x1,n1. As before, the expected number of such points is less than 1. Next, we examine the point x2 and put a Poisson process X3 with density 1 in x2 + A(2β, 2€)\(A(2β, 2ε)∪(x1 + A(2β, 2∈))) and denote the points of this process by x2,1,..., x2,n2. We continue in the obvious way, each time adding a Poisson process in a region which is disjoint from all regions inspected so far. It is clear from the construction that if this branching process dies out, the origin cannot be in a chain with decreasing radii all of which are at least β. But by construction, the branching process dies out a.s. and the proof is complete. □


<!-- p:233 -->


We continue with a 'dependent RCM' in the same spirit as the previous example. The setup is the same: take a Poisson process in IRa with density 1 (as in the first model of this section, the density is irrelevant). Now we connect each point x of X with the m points of X nearest to x. Again, m ≥ 1 is the parameter of the model and we can define mc(d) as the smallest m for which percolation occurs in this model. For me(d), we have the same bounds as for kc(d) above:

Theorem 8.7 For every d ≥ 2 it is the case that

$$2 \leq m _ { c } ( d ) < \infty .$$

The proof of the lower bound in Theorem 8.7 proceeds by a branching process argument as in the proof of Theorem 8.6 above and we do not give it here. We shall now show that m (d) is bounded away from infinity. The bound we obtain is very crude and the conjecture, based on simulations, is that mc(2) = 3 and mc(d) = 2 for all d ≥ 3.

Proof of Theorem 8.7 For ease of exposition, we will give the proof for the case d = 2 only, the generalisation to higher dimensions being completely straightforward. Let pc denote the critical value for site percolation on the square lattice. As noted before, the density λ of the Poisson process is irrelevant for the occurrence of infinite clusters, so we can pick λ so large that the probability of seeing no point in the square [0, ]2 satisfies

$$P \left ( X \left ( \left [ 0 , \frac { 1 } { 7 } \right ] ^ { 2 } \right ) = 0 \right ) < \frac { 1 - p _ { c } } { 2 \cdot 7 ^ { 2 } } .$$

Let E0,0 be the event that for i, j = 0, . .. , 6 we have that

$$x \left ( \left [ \frac { i } { 7 } , \frac { i + 1 } { 7 } \right ] \times \left [ \frac { j } { 7 } , \frac { j + 1 } { 7 } \right ] \right ) > 0 ;$$

i.e., E0.0 is the event that we see at least one point in each of the 72 basic subsquares (of the form [i/7, (i + 1)/7] × {,j/7, (j + 1)/7]) of the unit square


<!-- p:234 -->


[0, 1]2. We have

$$P ( E _ { 0 , 0 } ^ { \prime } ) > 1 - 7 ^ { 2 } \left ( \frac { 1 - p _ { c } } { 2 \cdot 7 ^ { 2 } } \right ) = \frac { 1 + p _ { c } } { 2 } .$$

Now pick m so large that the probability of seeing more than m/72 points in the square [0, ] satisfies

$$\left [ 0 , \frac { 1 } { 7 } \right ] ^ { 2 } \right ) > \frac { m } { 7 ^ { 2 } } \right ) < \frac { 1 - p _ { c } } { 2 \cdot 7 ^ { 2 } } .$$

be the event that for i, j = 0, . . . , 6 we have

$$X \left ( \left [ \frac { i } { 7 } , \frac { i + 1 } { 7 } \right ] \times \left [ \frac { j } { 7 } , \frac { j + 1 } { 7 } \right ] \right ) \leq \frac { m } { 7 ^ { 2 } } ,$$

i.e., that we see at most m /72 points of X in each of the 72 basic subsquares. We have

$$P ( E _ { 0 , 0 } ^ { * } ) > 1 - 7 ^ { 2 } \left ( \frac { 1 - p _ { c } } { 2 \cdot 7 ^ { 2 } } \right ) = \frac { 1 + p _ { c } } { 2 } .$$

Let E0,0 be the event given by E0,0 = E0,0 ∩ E0,0 E0,0, and for l, n ∈ Z, let El,n be the obvious analogous event for the square [l, I + 1] × [n, n + 1]. We have that the events {E{,n }l,n∈z are independent with probabilities

$$P ( E _ { l , n } ) = P ( E _ { 0 , 0 } ) > 1 - \left ( 1 - P ( E _ { 0 , 0 } ^ { \prime } ) \right ) - \left ( 1 - P ( E _ { 0 , 0 } ^ { * } ) \right ) = p _ { c } .$$

[1+3, +] × [7, ] and note that So For i = 0, .. , let S denote the quare [13, and S7 are centred at the same points as the squares [0, 1]2 and [1, 2] × [0, 1], respectively. Suppose now that the events Eo,o and E1,0 occur. We then have that no point of X in U=1Si has more than m points within distance . Two points x and y in S and S+1 are at distance at most √5/7 from each other. Since √5 &lt; 3, this implies that for all x ∈ S, y ∈ S+1, there is an edge between x and y. This in turn implies that for all x ∈ So, y ∈ S7, there is a path from x to y. Similar statements hold whenever two events El,n and El+1,n (or El,n and El,n+1) occur. A simple comparison with independent site percolation on the square lattice now shows that there is an infinite cluster a.s. 口

### 8.4 Stationary spanning forests

Suppose we are given a finite set of points S = {x1, . .. , xn} in d-dimensional Euclidean space. A tree T with vertex set S is called a spanning tree for S if each vertex of S is incident to at least one edge of T. A minimal spanning tree (MST) for S is a spanning tree such that the sum of the edge lengths is minimal among all spanning trees. If S is such that the distances |xi – xjl are all different, then there is a unique MST for S and this tree can be constructed as follows. Start with an arbitrary vertex, x1 say, and define T1(x1) = {x1}. Choose the point in S closest to x1, x2 say, draw the edge between x1 and x2 and define T2(x1) = {x1, x2}. Inductively, after having defined Tk(x1) for some 1 ≤ k ≤ n − 1, choose the vertex of S\ Tk(x1) closest to any point in Tk(x1), draw the edge between these two points and add the new point to Tk(x1) to obtain Tk+1(x1). This algorithm is called the greedy algorithm for obvious reasons and it can be shown that Tn (x) is the same for all 1 ≤ i ≤ n.


<!-- p:235 -->


We are now going to describe an infinite and stationary version of this procedure. Note that the notion of a spanning tree (or a spanning forest, i.e. a graph with no circuits but not necessarily connected) still makes sense on an infinite set of vertices, but the notion of a minimal spanning tree typically does not. Th s  s      s    i ke a Poisson process X in IRd with density 1 (the value of the density is unimportant). For any point x ∈ X we can apply the greedy algorithm described above. This yields, for any integer n ≥ 1, a tree Tn(x). We write

Definition 8.2 The (random) graph F is the graph with vertex set all points of X and which contains the (undirected) edge e = (x, xj) if and only if e is an edge in either T∞(x) or T∞(xj).

It is clear that F is stationary in the sense that the distribution of the graph structure is invariant under translations. We are interested in the geometry of F and we shall discuss both local and global properties of F.

Theorem 8.8 The graph F is a.s. a forest and all components of F are unbounded.

Proof Suppose that F contains a circuit (x1, x2, ..., xn, x1) with all xi's different. Suppose that the maximal edge length in this circuit is attained by the edge e = (xn, x1), say. Observe that T∞(x1) cannot contain e because the greedy algorithm would first have added all other edges of the circuit. Similarly, T∞(xn) cannot contain e. It follows that F does not contain e, a contradiction.

Next we show that F contains only unbounded components. We claim that if f = (x1, x2) is an edge of T∞(x) for some x ∈ X, then f ∈ F. This claim is enough since it implies that the component of F which contains x also contains T∞(x). To prove the claim, suppose that f is an edge of T∞(x) and that x1 is added to T∞(x) before x2 by the greedy algorithm. If f is not an edge of T∞(x1), then T∞(x1) contains only edges which are shorter than |x1 - x2|. But then, f will never be added to T∞(x) which is a contradiction. Hence f is an edge of T∞(x1) and thus also of F.


<!-- p:236 -->


The obvious question to be answered here is whether or not F is a tree. One might guess that a tree is obtained, but this is not so clear, especially if we take into account some results of Pemantle (1991). He shows that 'uniform spanning forests' on the d-dimensional integer lattice can be a.s. trees or forests depending on the dimension.

We end the section with two local properties of F which could be of some help in understanding the model.

Proposition 8.3 Suppose without loss of generality that the origin is a point of X and let D be the degree of the origin in F. Then there is a constant cd, depending on the dimension only, such that D ≤ cd. Furthermore, E D = 2, in any dimension.

Proof It is easy to see that in any minimal spanning tree, two edges sharing a vertex cannot make an angle of less then 60 degrees. So for any vertex x there is a uniform bound (in dimension 2 this bound is 6) on the number of edges in T∞(x) which have x as an end vertex. Denote these edges by e1, ..., ek, where e = (x, x). In addition to these edges, x can also be the end vertex of an edge (x, y) in G for which (x, y) is an edge of T∞(y). Denote these edges by fi, ... , fn where fj = (x, yj). We claim that for all i ≠ j, fi and fj make an angle of at least 60 degrees. To see this, suppose not and suppose that d(x, yj) &gt; d(x, yi), say. Then d(yi, yj) &lt; d(yj, x) and it follows that also (yj, yi) and fi are edges in T∞(yj). This is a contradiction because T∞(yj) cannot contain a circuit. Finally we claim that fj and e cannot make an angle of less than 60 degrees for any i and j. This follows as in the proof of the first claim after noting that d(x, x) &lt; d(yi, x).

It remains to show that ED = 2. The proof is based on a typical volumeboundary argument. Consider the box BL = [−L, L]d as usual. Let FL be the number of components in the graph which we obtain from G if we only look at points of X in BL and the connections between them. Let GL be the number of edges which cross the boundary of BL, i.e. all edges which have exactly one end point in BL. (Note that there are a.s. no points of X on the boundary of BL.) Finally, we denote by h(x) the degree of the vertex x in G. We now claim that


<!-- p:237 -->


$$\sum _ { x \in X \cap B _ { L } } ( h ( x ) - 2 ) = G _ { L } - 2 F _ { L } .$$

This formula seems somewhat mysterious, but it is easy to prove by induction: if X has only one point in BL the left and right sides of (8.13) are both equal to —2. If we add a point of X in BL both sides decrease by 2; if we add an edge between two points in B then this edge has to be between different components (G is a forest!) and both sides increase by 2; if we add an edge between a point in BL and a point outside BL both sides increase by 1.

We want to take expectations in (8.13). To this end we observe that E X(BL) = (2L)a and it is not hard to show with the theory of Palm measures (and intuitively obvious) that E (Σx∈ X∩BL h(x)) = (2L)a E D. Hence we obtain

$$E D - 2 = \frac { E ( G _ { L } ) } { ( 2 L ) ^ { d } } - 2 \frac { E ( F _ { L } ) } { ( 2 L ) ^ { d } } .$$

Using the fact that all components of G are unbounded we see that FL ≤ GL and it suffices therefore to show that E(GL) = o(Ld) for L → ∞. For this, let D, denote the number of edges at the origin in G with length at least r. Now GL counts edges crossing the boundary of BL and by considering separately those edges with end point in BL\BL-r and those with end point in BL-r we have, using Proposition 8.3,

$$E G _ { L } \leq c _ { d } \ell ( B _ { L } \rangle B _ { L - r } ) + ( 2 ( L - r ) ) ^ { d } E D _ { r }$$

whence lim supL→∞ E BL/(2L)d ≤ E Dr. Now let r → ∞, and the proof is complete. □

### 8.5 Percolation of Poisson sticks

The strength and brittleness of a metal object depends on the fractures present in the material. Typically, the fractures are represented as cracks of varying lns  o      t    ch fractures are also present in geological objects, e.g. fault lines in the study of earthquakes. Although in the first case, the material may be assumed to have homogeneous composition, the geological study will not admit such an assumption of homogeneity. Nonetheless, a simple model used to study such phenomenon is the Boolean model with 'sticks' instead of balls.

Consider a Poisson point process X on IR2 and suppose that each point of the process is the centre of a one-dimensional line (stick) of random length and of random orientation θ with respect to the x-axis. These sticks represent the cracks. Again we assume that the different sticks have an i.i.d. distribution. More precisely, our model consists of points x1, x2, ... of a Poisson point process with density λ on IR2 and one-dimensional line segments L1, L2, ... centred at x1, x2, . . . respectively, where L has length l, and orientation θ with respect to the x-axis. We assume that l1, l2, . . . are i.i.d., θ1, θ2, .. . are i.i.d. and, for all 1 ≤ i, j, li and θj are independent of each other. For this model we may define the critical quantities λc, λr and λs as in the ordinary' Boolean model.


<!-- p:238 -->


Clearly if θ, has a degenerate distribution, i.e. all sticks are oriented in the same direction, then no two sticks will intersect a.s. ard so percolation will never occur almost surely. Thus for any meaningful study of this model we need to assume that θ has a non-degenerate distribution.

As a simple example let us study the case where

$$\theta _ { 1 } = \begin{cases} 0 & \text {with probability } p , \\ 1 / ( 2 \pi ) & \text {with probability } 1 - p , \end{cases}$$

and

$$l _ { 1 } = 1 \quad \text {with probability } l .$$

Let Lo be a stick of unit length centred at the origin and with orientation 0. Let Li, Li2, ..., Lik be sticks which intersect Lo. Clearly, with probability 1, all these sticks are perpendicular to Lo and are centred in the box B1/2 = [−1, ↓] × [−, ↓]. Thus k has a Poisson distribution with mean λ(1 − p). We call these sticks the first generation sticks. The second generation sticks are all the sticks, except the stick Lo, which intersect the first generation sticks. In a similar fashion we define the (n + 1)-th generation sticks as all the sticks, except the sticks which have already been considered in previous generations, which intersect a stick of the n-th generation. Clearly, the expected number of sticks which lie in the component containing Lo equals the sum of the expected number of sticks at each of the generations. We shall obtain an upper bound of this quantity by placing an independent Poisson process for each stick of the n-th generation and computing the expected number of sticks from this process which intersect the given stick. Adding this expected number over all the sticks of the n-th generation, we obtain an upper bound of the expected number of sticks of the (n + 1)-th generation.

Given a stick L of the n-th generation, by placing an independent Poisson process of intensity λ with the orientation and length of sticks given by (8.14) and (8.15) respectively, we have

$$E _ { \lambda } ( \text {number of sticks intersecting } L ) \leq \begin{cases} \lambda p & \text {if $n$ is odd} \\ \lambda ( 1 - p ) & \text {if $n$ is even} . \end{cases}$$


<!-- p:239 -->


Thus, if the n-th generation consists of sticks Lj1 , . . . , Ljm, then

Eλ (number of sticks in the (n + 1)-th generation|Lj, . . . , Ljm

are all the sticks of the n-th generation)

$$& \text {are all the sticks of the n-th generation} ) \\ & \leq \sum _ { i = 1 } ^ { m } E _ { \lambda } ( \text {number of sticks intersecting } L _ { j _ { i } } | L _ { j _ { i } } \text { is a stick} \\ & \text {of the } n - \text {th generation} ) \\ & \leq \begin{cases} \ m \lambda _ { p } & \text {if $n$ is odd} \\ \ m \lambda ( 1 - p ) & \text {if $n$ is even.} \end{cases} \\ \text {now the number of sticks } \ m \text { is in the } n \text {th generation} is a random variable \text { and}$$

Now the number of sticks, m, in the n-th generation is a random variable, and an induction argument assuming that

$$E _ { \lambda } ( m ) & \leq \begin{cases} ( \lambda p ) ^ { n / 2 } ( \lambda ( 1 - p ) ) ^ { n / 2 } & \text {if $n$ is even} \\ ( \lambda p ) ^ { ( n - 1 ) / 2 } ( \lambda ( 1 - p ) ) ^ { ( n + 1 ) / 2 } & \text {if $n$ is odd} \end{cases} \\ & < \infty$$

yields, on an application of Wald's equation,

$$E _ { \lambda } ( \text {number of sticks in the } ( n + 1 ) - \text {th generation} ) \\ \leq \begin{cases} ( \lambda p ) ^ { n / 2 } ( \lambda ( 1 - p ) ) ^ { ( n / 2 ) + 1 } & \text {if $n$ is even} \\ ( \lambda p ) ^ { ( n + 1 ) / 2 } ( \lambda ( 1 - p ) ) ^ { ( n + 1 ) / 2 } & \text {if $n$ is odd.} \end{cases}$$

Hence the expected number of sticks in all generations is at most

$$\text {expected number of sticks in all generations is at most} \\ \sum _ { n = 0 } ^ { \infty } [ ( \lambda p ) ^ { n } ( \lambda ( 1 - p ) ) ^ { n } + ( \lambda p ) ^ { n } ( \lambda ( 1 - p ) ) ^ { n + 1 } ] \\ = ( 1 + \lambda ( 1 - p ) ) \sum _ { n = 0 } ^ { \infty } ( \lambda ^ { 2 } p ( 1 - p ) ) ^ { n } \\ < \infty \text { if } \lambda < \sqrt { \frac { 1 } { p ( 1 - p ) } } . \\ \geq \sqrt { 1 / ( p ( 1 - p ) ) } . \text { In particular, when } p = \frac { 1 } { n } , \text { we have } \lambda _ { c } \geq 2 .$$

Thus λc ≥ √1/(p(1 − p)). In particular, when p = , we have λc ≥ 2. In general, we assume that

$$0 < l _ { 1 } \leq R ,$$

for some R &gt; 0, and

$$\theta _ { 1 } \text { has a uniform } [ 0 , 1 ] \text { distribution} .$$

Under these conditions, not only can we prove the equality of the critical densities λc, λτ and λs, we may also define the critical densities via the vacancy structure λ*, λ and λ* and prove their equality. As in Theorems 3.5 and 4.3 we have Theorem 8.9 For the Poisson stick model on the two-dimensional plane, if (8.16) and (8.17) hold then λc = λτ = λs = λc = λ = λs.


<!-- p:240 -->


For higher dimensions, if we consider one-dimensional lines satisfying (8.16) and (8.17) in a higher-dimensional Poisson setting, then it is easy to see that two lines will almost surely never intersect and thus we will not have any percolation. The appropriate analogy will consist of bounded (d — 1)-dimensional rectangles in a d-dimensional Poisson setting.

####### 8.6Notes

The results in Section 8.1 are due to Meester and Sarkar (forthcoming) and motivated by a number of papers on discrete fractal percolation (Chayes, Chayes and Durrett, 1988; Chayes and Chayes, 1989; Dekking and Meester, 1990). Theorem 8.3 and Theorem 8.4 are from Molchanov and Stepanov (1983), and Theorem 8.5 is due to Alexander and Molchanor (1994). The equality pc + p* = 1 is from Russo (1978). The material in Section 8.3 is taken from Häggström and Meester (1995), where it is shown that m c(d) = 2 for all d sufficiently large. The basic reference for Section 8.4 is Aldous and Steele (1992). Alexander (1994) has shown, using the occupied version of the RSW theorem, that F is a tree a.s. in two dimensions. The results of Section 8.5 are taken from Roy (1991).


<!-- p:241 -->

#### Index

```
action: 23, 24                                         density: 11, 25
                                    relative: 127
                                    differential: 1,
                                    differential inequality: 163
                                    continuum: 35
                                    discrete: 7, 16
                                    discrete: 2, 65
            Boolean model
                dependent: 2221
                general: 15, 184
                Poisson, 7, 40, 92, 122
            bounds on \a c, 52, 89
            branching random walk, 89
                                 ergodic decomposition, 183
            circuit, 3
            closure, 187
            cluster, 3
                size, 89
            complete coverage, 41, 184
            component
                occupied, 15,
                vacant, 15
            compression, 127
            connection function, 18, 155
            continuity
                of critical density, 71
                of percolation function 77, 78, 119
            coupling, 28
            covered volume fraction, 122, 209
                at criticality, 123
            critical densities, 45, 50, 53, 92, 152
                equality of, 53, 59, 109, 159
            critical probability, 3
            crossing probability
                continuum, 33
                discrete, 4
            cutting and stacking, 199
                generalised, 202
                                                        2,37
```


<!-- p:245 -->


####### Index

| infinite volume limit, 168 interior, 187                                                                 | random-connection model                                                   |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
|                                                                                                          | dependent, 225                                                            |
| invariant, 21                                                                                            | general, 18, 197                                                          |
| Kuratowski's criterion, 190                                                                              | Poisson, 151 random field, 216 rarefaction, 139                           |
| latice, 3                                                                                                | relative density, 127                                                     |
| Lebesgue density theorem, 153, 201                                                                       | RSW lemma                                                                 |
| Lebesgue set, 153                                                                                        | occupied, 121                                                             |
| level set, 217                                                                                           | vacant, 96                                                                |
| martingale convergence, 32                                                                               | Russo's formula, 7, 8, 163, 167                                           |
| measure-preserving (m.p.) dynamical system, 21                                                           | scaling, 29                                                               |
| transformation, 21 mixing, 26 neighbour, 3 occupied region, 15 Palm distribution, 13 path, 3 percolation | spanning forest, 226 spanning tree, 226                                   |
| bond/site, 8 discrete, 2                                                                                 | stationary, 10 sticks, 229 Stirling's formula, 128                        |
|                                                                                                          | subcritical, 18 supercritical, 18                                         |
|                                                                                                          | superposition, 11                                                         |
|                                                                                                          | tangent balls, 224                                                        |
|                                                                                                          | thinning, 13                                                              |
| fractal, 209                                                                                             | T-invariant, 21 tree, 204, 206, 226                                       |
| level set, 216 in one dimension, 43                                                                      | triangular lattice, 87 uniqueness, 5                                      |
| percolation function, 3, 18                                                                              | in general Boolean model, 194                                             |
| monotonicity of, 3, 29                                                                                   | in general random-connection model, 197 in Poisson Boolean model, 63, 116 |
| continuity of, 77, 78, 119                                                                               |                                                                           |
| phase transition, 2, 4, 53                                                                               |                                                                           |
| pivotal, 7 planar graph, 190                                                                             |                                                                           |
| point process, 9                                                                                         | in Poisson random-connection model, 172                                   |
| stationary, 10                                                                                           |                                                                           |
|                                                                                                          | vacant region, 15                                                         |
| Poisson Boolean model, 17                                                                                |                                                                           |
| Poisson process                                                                                          |                                                                           |
| homogeneous, 11                                                                                          |                                                                           |
| non-homogeneous, 12                                                                                      | weak convergence, 71                                                      |
