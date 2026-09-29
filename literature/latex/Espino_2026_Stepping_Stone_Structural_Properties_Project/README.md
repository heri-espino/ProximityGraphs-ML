# Structural Thresholds of Stepping-Stone Graphs

This project contains the structural graph-theory manuscript separated from
the geometry-and-volume paper.

## Compile

- Review version: `latexmk -pdf main.tex`
- Clean submission version: `latexmk -pdf -jobname=main_submission main_submission.tex`

The clean wrapper defines `\SubmissionVersion`, which suppresses revision
colors. The project includes the Elsevier class files, bibliography, and the
figures required for compilation.

## Scope

The manuscript develops unit-region order reversal, stepping-stone graph
monotonicity, comparisons with classical proximity graphs and
beta-skeletons, connectivity and dilation consequences, sharp thresholds for
intersection-free realizations and Delaunay containment, dimension-dependent
abstract planarity, and arbitrary-dimensional spectrum stabilization.
