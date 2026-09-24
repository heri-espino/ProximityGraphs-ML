# ProximityGraphs-ML

Research repository for **Paper 1** of a planned line connecting empty-region proximity graphs, stochastic geometry, and manifold inference.

## Working paper

**Tentative title:** *Empty-Region Proximity Graphs on Manifolds: Local Limits and Intrinsic Dimension*

The central question is whether a fixed-template empty-region graph built on an i.i.d. sample from an unknown smooth manifold has a local limit governed by a homogeneous Poisson process on the tangent space, and whether the resulting degree and edge-length laws can be converted into statistically useful information about intrinsic dimension.

This project starts from the unit-region/fixed-template viewpoint developed for Euclidean empty-region proximity graphs and asks what survives when the sample is supported on an unknown manifold.

## Current state

- Repository initialized.
- Literature PDFs collected in `literature/pdf/`.
- PDF filenames normalized to `Author_year_Short-Title.pdf` where metadata is identifiable.
- Research scope for Paper 1 fixed.
- Theorem targets, literature review, simulation plan, and statistical goals are documented.
- **No theorem claimed in this repository is proved yet unless explicitly marked proved.**
- No production experiment suite or paper draft has been started yet.

## Start here

1. `docs/AI_HANDOFF.md` — current intellectual state and immediate next actions.
2. `TODO.md` — executable task list.
3. `docs/ROADMAP.md` — full research roadmap and paper boundary.
4. `literature/README.md` — literature organization, naming convention, and unresolved files.

## Paper-1 boundary

Paper 1 is intentionally narrow. It targets:

- local tangent-space limits for fixed-template empty-region proximity graphs;
- asymptotic edge probabilities and edge-length laws;
- degree limits / graph-size laws;
- intrinsic-dimension estimators derived from those laws;
- clean simulations validating the asymptotics and comparing dimension estimators.

It does **not** currently target persistent homology, Čech/Vietoris–Rips complexes, Laplace–Beltrami convergence, spectral embeddings, UMAP/Isomap replacements, or a full topological reconstruction theorem. Those are possible later papers.

## Candidate graph families

Primary examples:

- Gabriel graph;
- relative neighborhood graph (RNG);
- beta-skeleton / stepping-stone families;
- nearest-neighbor-type graphs where they fit the formal template.

The abstract theory should be stated for a carefully defined fixed-template / similarity-copy empty-region class rather than proved separately for each named graph.
