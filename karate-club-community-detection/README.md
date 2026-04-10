# Karate Club Community Detection Benchmark

## Objective

Measure how well major community detection algorithms recover known ground-truth communities on a canonical benchmark graph.

## Approach

- Ran multiple community detection methods on the Zachary Karate Club network.
- Evaluated each method with:
  - **AMI** (agreement with known labels)
  - **modularity** (intra-community density quality)

## Key Results

- **Girvan-Newman** achieved the highest AMI (~0.833), indicating strongest alignment with known labels.
- **Leiden/Louvain** produced the highest modularity (~0.420), indicating very strong structural partitioning.

## Why this matters

Shows clear understanding of the distinction between:
- recovering externally known classes,
- and optimizing internal graph structure objectives.

## Reproducibility

See notebook: `../analysis.ipynb` (karate benchmark section)

