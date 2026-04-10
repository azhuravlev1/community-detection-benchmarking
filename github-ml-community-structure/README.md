# GitHub ML Community Structure Comparison

## Objective

Compare how different community detection algorithms partition a GitHub ML developer network when no explicit ground-truth communities are available.

## Approach

- Built ML-only subgraph from GitHub developer network.
- Ran 6 community detection algorithms (excluding Girvan-Newman for computational efficiency on this graph size).
- Computed pairwise **AMI agreement matrix** across algorithm outputs.

## Key Findings

- Highest agreement observed between **Leiden and Louvain** (AMI ~0.652).
- Lowest agreement observed between **Infomap and Label Propagation** (AMI ~0.290), indicating materially different community assumptions/behavior.

## Why this matters

Demonstrates practical model-selection analysis in unsupervised settings where:
- labels are unavailable,
- method agreement can guide confidence and downstream use.

## Reproducibility

See notebook: `../analysis.ipynb` (GitHub ML section)

