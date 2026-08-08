# Clustering
Clustering is about how nodes group up together. We use cluster coefficient to quantify this property.

## Metrics

### Cluster coefficient
Quantifies the extent to which node i and its neighbors form an interconnected cluster

$C_{i} = \frac{1/2 \Sigma_{j,m} A_{ij} A{jm} A{mi}}{k_{i}(k-1)/2}$

### Transitivity (global clustering coefficient)
Transitivity is the tendency for two nodes connected to a common neighbor to also be connected to each other.

$T = \frac{3 * number of triangles}{number of connected triplets}$

## Clustering in differnt network models
### $G(n,p)$ netowrk
Recall from the definition of the [G(n,p) network](network-structure.md#erdős-rényi-graph) that any two nodes in that model are connected with the same probability p. Therefore, the probability that a connected trplet A-B-C forms a triangle A-B-C-A is also p.