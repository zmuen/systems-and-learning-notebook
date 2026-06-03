# Random walks

## Transition matrix
For an undirected graph, let the degree of node $i$ be

$$
k_i=\sum_j A_{ij}
$$

The transition matrix for a simple random walk is

$$
P_{ij}=\frac{A_{ij}}{k_i}
$$

or, in matrix form,

$$
P=D^{-1}A
$$

where $D=\mathrm{diag}(k_1,\dots,k_n)$.

## Random-walk dynamics
If $p^{(t)}$ is the probability distribution over nodes at time $t$, then the walk evolves as

$$
p^{(t+1)}=p^{(t)}P
$$

## Stationary distribution
A stationary distribution $\pi$ satisfies

$$
\pi=\pi P, \qquad \sum_i \pi_i=1
$$

So $\pi$ is both a probability distribution and a left eigenvector of $P$ with eigenvalue $1$:

$$
\pi P = 1\cdot \pi
$$

For a connected undirected graph,

$$
\pi_i=\frac{k_i}{\sum_j k_j}=\frac{k_i}{2m}
$$

Random walks are a simple but powerful way to model how load, information, exposure, or influence propagates through a network over time.
