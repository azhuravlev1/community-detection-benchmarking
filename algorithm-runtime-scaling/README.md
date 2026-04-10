# Community Detection Runtime Scaling Study

## Objective

Quantify computational cost growth across community detection algorithms as graph size increases.

## Approach

- Generated benchmark graphs at multiple node sizes.
- Timed each algorithm on every graph size and built a runtime comparison table.

## Key Result

- **Girvan-Newman** is by far the slowest and scales poorly for larger graphs.
- **Label Propagation** is consistently the fastest among tested methods.

## Why this matters

In production analytics, algorithm choice is often constrained by runtime and resource budgets; this study supports defensible method selection under scale.

## Reproducibility

See notebook: `../analysis.ipynb` (runtime scaling section)

