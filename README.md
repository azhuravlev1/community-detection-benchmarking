# Community Detection Benchmarking

A comparison of seven community detection algorithms on a benchmark graph with known communities, on a real GitHub developer network, and on synthetic graphs of growing size. It was an assignment for DS8014 (Graph Mining) at Toronto Metropolitan University. All the code is in `analysis.ipynb`.

Algorithms: ECG, Leiden, Louvain, Infomap, label propagation, Girvan-Newman and CNM (fast greedy modularity).

## Three experiments

[Karate club](karate-club-community-detection/README.md). Zachary's karate club has known ground-truth groups, so each partition can be scored two ways: AMI against the true labels, and modularity as a measure of internal structure. Girvan-Newman recovered the real groups best (AMI about 0.83), while Leiden and Louvain found the partitions with the highest modularity (about 0.42). The two measures reward different things, and the best method depends on which one you care about.

[GitHub ML developers](github-ml-community-structure/README.md). On the machine learning subgraph of the GitHub developer network there is no ground truth, so I compared the algorithms with each other using a pairwise AMI matrix. Leiden and Louvain agreed most (AMI about 0.65), and Infomap and label propagation least (about 0.29). Girvan-Newman was left out because it is too slow at this size.

[Runtime scaling](algorithm-runtime-scaling/README.md). Each algorithm was timed on generated graphs of increasing size. Girvan-Newman becomes impractical quickly, and label propagation was the fastest at every size.

## Files

`analysis.ipynb` holds all three experiments. `musae_git_edges.csv` and `musae_git_target.csv` are the GitHub developer network (MUSAE dataset). Requirements: Python with igraph, networkx, pandas and scikit-learn.
