# GitHub ML developers: agreement between algorithms

Six algorithms (all except Girvan-Newman, which is too slow here) partition the machine learning subgraph of the GitHub developer network. With no ground truth available, the partitions are compared with each other in a pairwise AMI matrix. Leiden and Louvain agree most (about 0.65); Infomap and label propagation agree least (about 0.29).

Code: the GitHub ML section of [`../analysis.ipynb`](../analysis.ipynb).
