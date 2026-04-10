# Community Detection Benchmarking

Primary analysis notebook: `analysis.ipynb`

## Project Overview

This project benchmarks community detection algorithms across reference and real-world social-network graphs, comparing both **quality** and **runtime scalability**.

## Algorithms Compared

- ECG
- Leiden
- Louvain
- Infomap
- Label Propagation
- Girvan-Newman
- CNM (Fast Greedy)

## Evaluation Dimensions

- **Partition quality:** modularity, AMI
- **Cross-algorithm agreement:** pairwise AMI matrix
- **Performance scaling:** runtime by graph size on generated benchmark graphs

## Practical Relevance

This project supports common graph analytics tasks:
- unsupervised segmentation of connected systems,
- method selection under runtime constraints,
- transparent quality-vs-speed tradeoff reporting.

## Subprojects

- [`karate-club-community-detection`](karate-club-community-detection/README.md)
- [`github-ml-community-structure`](github-ml-community-structure/README.md)
- [`algorithm-runtime-scaling`](algorithm-runtime-scaling/README.md)


