# Walks, paths, and cycles

## Walks
A walk of length $k$ from node $s$ to node $t$ is a sequence

$$
s=v_0,v_1,\dots,v_k=t
$$

such that $(v_{i-1}, v_i)\in E$ for every $i=1,\dots,k$.

The number of walks of length $k$ from node $s$ to node $t$ is given by the $(s,t)$ entry of $A^k$:

$$
(A^k)_{st}=\sum_{v\in V}(A^{k-1})_{sv}A_{vt}
$$

In particular,

$$
(A^1)_{st}=A_{st}, \qquad (A^2)_{st}=\sum_{v\in V}A_{sv}A_{vt}
$$

## Paths
A path is a walk in which all vertices are distinct.

The shortest-path distance from $s$ to $t$ can be written as

$$
d(s,t)=\min\{k\ge 0:(A^k)_{st}>0\}
$$

## Cycles
A cycle is a closed walk with

$$
v_0=v_k
$$

and no repeated vertices other than the first and last.

## Dense structures
A complete graph, or clique, is a graph in which every vertex is connected to every other vertex. In an $n$-node complete graph, each node has degree $n-1$.
