# Graph representation

## Basic graph formalization
A network is commonly represented as a graph $G=(V,E)$, where $V$ is the set of nodes and $E$ is the set of edges.

## Adjacency matrix
The adjacency matrix $A$ stores whether an edge exists between each pair of nodes:

$$
A_{ij}=
\begin{cases}
1 & \text{if there is an edge from } i \text{ to } j \\
0 & \text{otherwise}
\end{cases}
$$

The adjacency matrix requires $n^2$ space, but it allows constant-time edge lookup and makes linear algebra tools directly applicable.

One key relation is

$$
Av=\lambda v
$$

where $\lambda$ is an eigenvalue and $v$ is the corresponding eigenvector.

## Adjacency list
The adjacency list representation stores, for each node, the set of its neighbors. It is more space-efficient for sparse graphs and typically requires $n + 2m$ space in an undirected graph because each edge is recorded twice.

## Directed and weighted graphs
For a directed graph,

$$
A_{ij}=1
$$

means there is an edge $i \rightarrow j$.

The number of incoming edges to node $v$ is its in-degree, and the number of outgoing edges is its out-degree.

In weighted graphs, edges carry magnitudes rather than just binary presence. In undirected weighted networks, the strength of node $i$ is

$$
s_i=\sum_j w_{ij}
$$

In directed weighted networks, we distinguish in-strength and out-strength.
