# Literature

## Filename convention

PDFs should use:

```
Author_year_Short-Title.pdf
```

Examples:

```
Devroye_1988_Expected-Size-Computational-Geometry-Graphs.pdf
Cardinal_2009_Empty-Region-Graphs.pdf
Penrose-Yukich_2001_Weak-Laws-Geometric-Probability.pdf
```

For two-author works, both surnames may be retained when useful. For larger author lists, the first author is sufficient. Titles should be concise, filesystem-safe, and recognizable.

Do not encode journal names, DOI strings, download-site tokens, or phrases such as `Download (1)` into filenames.


## Curation status

On 2026-09-23, the corpus was pruned to remove material clearly unrelated to Paper 1. Removed items included time-series smoothing/forecasting papers, *Attention Is All You Need*, an English-language exam trainer, unrelated education-support literature, a Mexican-city power-law paper, a nonspatial Weibull-network paper, and a Poisson-approximation paper on amenable groups.

Peripheral sources with a plausible role in proximity graphs, stochastic geometry, nearest-neighbor computation, geometric probability, manifold statistics, or supporting mathematics were retained pending the novelty audit.

## Unresolved PDFs

Two source files could not be identified reliably from accessible metadata during the normalization pass:

- `Unknown_nd_Unidentified-Scanned-Article.pdf` — image-only scan; original filename was `Download (1).pdf`.
- `Unknown_nd_Unidentified-PDF.pdf` — original filename was `PDF.pdf`.

These names are deliberately marked unknown rather than assigning false citation metadata. Identifying them is an open TODO.

## Core reading queue for Paper 1

### A. Empty-region / proximity graphs

Already represented in the repository:

- Gabriel & Sokal — origin/statistical use of the Gabriel graph.
- Matula & Sokal — Gabriel graph properties.
- Toussaint — relative neighborhood graph.
- Jaromczyk & Toussaint — RNG survey/relatives.
- Devroye — expected size of geometric graphs.
- Cardinal et al. — empty-region graphs.
- Veltkamp and beta/gamma-neighborhood literature.
- stepping-stone / beta-skeleton papers and the user's prior manuscripts.

### B. Stochastic geometric probability

Already represented in part:

- Penrose & Yukich — weak laws and CLTs for computational-geometry graphs.
- Last & Penrose — Poisson process foundations.
- stochastic-geometry references on Palm/Poisson methods.

### C. Must add / verify for the manifold paper

Before claiming novelty, obtain and read the closest sources on:

- **Penrose & Yukich — limit theory for point processes in manifolds.**
- **Brito, Quiroz & Yukich — graph-based intrinsic-dimension estimation.**
- **Levina & Bickel — maximum-likelihood intrinsic-dimension estimation from local Poisson/nearest-neighbor behavior.**
- **Dyballa & Zucker — IAN / Gabriel neighborhoods for manifold learning.**
- **Niyogi, Smale & Weinberger — manifold sampling / reach / topological inference.**
- **Aamari & Levrard — tangent-space, manifold, and curvature estimation.**

Years/filenames should be verified from the actual paper before adding them.

## Literature-review extraction template

For every close paper, record:

1. exact sampling model;
2. graph/neighborhood definition;
3. dimension assumptions;
4. density assumptions;
5. local scaling;
6. theorem statement;
7. whether the result is Euclidean or manifold-supported;
8. whether it gives degree, edge count, edge length, or full local convergence;
9. whether an intrinsic-dimension estimator is constructed;
10. proof tool: Palm theory, stabilization, Poissonization, tangent charts, empirical process, etc.;
11. direct overlap with our planned theorem;
12. what remains genuinely new.

The output of this review should become `docs/NOVELTY_MATRIX.md`.
