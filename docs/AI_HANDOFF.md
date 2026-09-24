# AI Handoff — ProximityGraphs-ML

**Last updated:** 2026-09-24  
**Project:** Paper 1 — proximity graphs on manifolds  
**Repository:** `heri-espino/ProximityGraphs-ML`

## What this project is

This repository is for a new theoretical/statistical paper extending fixed-template empty-region proximity-graph ideas from Euclidean stochastic geometry to data sampled from a smooth manifold.

The user's prior work develops a **unit-region factorization** viewpoint for empty-region graphs: for similarity-copy exclusion regions, a dimension/template-dependent unit-volume constant \(a_{d,T}\) controls Poisson void probabilities and several local graph statistics in flat Euclidean space.

The current project asks whether the correct local replacement on a manifold is obtained by:

1. zooming into \(x\in\mathcal M\);
2. replacing the manifold by its tangent space \(T_x\mathcal M\cong\mathbb R^m\);
3. replacing the local binomial sample by a homogeneous Poisson process of intensity \(f(x)\);
4. replacing ambient dimension \(D\) by intrinsic dimension \(m\);
5. transferring degree and edge-length laws into intrinsic-dimension inference.

This is the central research program, **not an established result yet**.

## Current paper boundary

Working title:

> **Empty-Region Proximity Graphs on Manifolds: Local Limits and Intrinsic Dimension**

Paper 1 should contain:

- a precise admissible template class;
- local manifold-volume asymptotics;
- tangent-space Poisson / local graph limits;
- degree and edge-length consequences;
- at least one consistent intrinsic-dimension estimator;
- simulations on controlled manifolds;
- comparisons to established intrinsic-dimension estimators.

Paper 1 should **not** expand into persistent homology, Čech/Rips, topological reconstruction, graph Laplacians, Laplace–Beltrami convergence, spectral embeddings, or a new manifold-learning algorithm unless the scope is explicitly changed later.

## Intellectual starting point

For a candidate pair at local distance \(r\), the Euclidean fixed-template intuition is
\[
\mathrm{Vol}_m(S_T)=a_{m,T}r^m.
\]

On a smooth manifold, the first target is
\[
\mathrm{vol}_{\mathcal M}(S_T(x,y)\cap\mathcal M)
=
a_{m,T}r^m+o(r^m).
\]

With local sample intensity \(nf(x)\), the corresponding candidate edge-void probability should then behave like
\[
\exp[-nf(x)a_{m,T}r^m].
\]

At the local scale \(r=t n^{-1/m}\), this suggests
\[
P(x\sim y)\to \exp[-f(x)a_{m,T}t^m].
\]

The major conceptual point is:
\[
D \text{ (ambient dimension) } \quad\leadsto\quad m \text{ (intrinsic tangent-space dimension).}
\]

Do **not** treat the displayed manifold formulas as proved merely because they are plausible.

## Closest existing literature / novelty risks

The novelty claim must be conservative.

Known/nearby strands include:

- classical Gabriel and RNG theory;
- Devroye-style expected-size laws for geometric/empty-region graphs in Euclidean space;
- Cardinal et al.'s empty-region graph formalism;
- stabilization, weak laws, and CLTs for geometric graph functionals (Penrose/Yukich and related work);
- point-process limit theory for samples on manifolds;
- graph-based intrinsic-dimension estimation;
- nearest-neighbor Poisson models for intrinsic dimension (e.g. Levina–Bickel);
- use of Gabriel graphs in manifold-learning neighborhoods (IAN).

In particular, **\(E[D_{GG}]\approx 2^m\) by itself is not a novelty claim**. The intended contribution is the unified manifold/tangent-space ERG theory and the statistical inference derived from it.

Before writing the introduction, create a novelty matrix that makes this distinction explicit.

## Literature status

The repository currently contains a broad literature dump in `literature/pdf/`. Filenames have been normalized.

Two PDFs could not be identified reliably from repository-accessible metadata:

- `Unknown_nd_Unidentified-Scanned-Article.pdf`
- `Unknown_nd_Unidentified-PDF.pdf`

Do not guess their citation metadata. Identify them manually when possible.

The folder also contains clearly tangential/unrelated material. It was intentionally retained during the rename pass. Curate later, after the novelty audit.

Core sources still likely need to be added, especially the manifold point-process limit paper, the graph-based intrinsic-dimension paper, IAN, and standard manifold-estimation references. See `literature/README.md`.

## What has been done

- Paper 1 was separated conceptually from later topology/manifold-learning ideas.
- The theorem chain and estimator ideas were sketched.
- The simulation design was sketched.
- The repository was initialized.
- Literature files were renamed into a consistent convention.
- Operational TODO and research roadmap were added.

## What has NOT been done

- No final submission-level exhaustive prior-art review; a first-pass core-literature novelty audit is complete.
- `docs/NOVELTY_MATRIX.md` now records the overlap/gap analysis.
- No formal template definition for this paper.
- No proof of the manifold-volume lemma.
- No proof of a tangent-space graph limit.
- No validated edge-length law on manifolds.
- No intrinsic-dimension estimator proof.
- No simulation code.
- No paper draft.

## Immediate next task

**Use the completed first-pass novelty matrix to formalize the template class and attack the manifold-volume lemma.**

Recommended order:

1. Devroye (1988): extract the exact ERG-like hypotheses and expected-size derivation.
2. Cardinal et al. (2009): map the formal ERG definition to the user's fixed-template class.
3. Penrose–Yukich manifold limit theory: identify the reusable theorem and stabilization hypotheses.
4. Brito–Quiroz–Yukich / related graph-based intrinsic-dimension theory.
5. Levina–Bickel nearest-neighbor Poisson dimension estimation.
6. IAN: record exactly what it uses/claims about Gabriel neighborhoods and dimension.
7. Manifold geometry references for reach, tangent approximation, and curvature error.

The first-pass `docs/NOVELTY_MATRIX.md` is now complete. Its main conclusion is that generic graph-based intrinsic-dimension estimation and tangent-Poisson limits are prior art; Paper 1 should be centered on the fixed-template manifold exclusion-volume factorization and explicit ERG laws. Do not freeze the estimator until that theorem is proved.

## Conventions for future agents

- Distinguish **proved results**, **known literature results**, **conjectures**, and **simulation observations** in every document.
- Do not call all proximity graphs “single-template” unless the precise class is defined.
- Prefer the established umbrella term **empty-region graph (ERG)** when discussing prior literature; use the fixed-template/similarity-copy terminology for the narrower structural subclass being studied.
- Do not conflate candidate-pair edge probability with the distribution of a randomly selected retained edge.
- Keep intrinsic dimension \(m\) distinct from ambient dimension \(D\).
- Keep boundary-free exact-manifold sampling as the main theorem setting initially; boundary and noise belong in robustness experiments unless scope changes.
- Reuse prior submitted results rather than duplicating them as if new.
- Heavy derived-output GitHub Actions, if introduced later, must be manual-only via `workflow_dispatch`; lightweight CI may remain automatic.
