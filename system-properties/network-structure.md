# Network structure

Network structure describes how connections are distributed across the system, whether hubs exist, and whether high-degree nodes tend to connect to one another or to peripheral nodes.

## Degree distribution
The degree distribution describes the fraction of nodes with degree $k$.

Let $p_k$ denote the probability that a uniformly sampled node has degree $k$.

Two useful summary statistics are:

- First moment: the average degree
- Second moment: the average of squared degrees

The variance of the degree distribution is

$$
\mathrm{Var}(K)=\langle k^2\rangle-\langle k\rangle^2
$$

where

$$
\langle k\rangle=\sum_k k p_k,
\qquad
\langle k^2\rangle=\sum_k k^2 p_k
$$

## Complementary cumulative distribution
For large networks, we often visualize the degree distribution using the complementary cumulative distribution function (CCDF) rather than the empirical probability mass function.

The CCDF is

$$
\overline{P}(k)=\Pr[K\ge k]=\sum_{x\ge k} p_x
$$

This emphasizes the tail of the distribution and is often easier to interpret for heavy-tailed networks.

## Friendship paradox
The friendship paradox says that your neighbors tend to have more neighbors than you do, on average.

The average degree of a node reached by following a random edge is

$$
\frac{\langle k^2\rangle}{\langle k\rangle}
$$

Since

$$
\frac{\langle k^2\rangle}{\langle k\rangle}
=
\langle k\rangle+\frac{\mathrm{Var}(K)}{\langle k\rangle},
$$

the average neighbor degree is larger than the average node degree whenever the degree variance is positive.

The intuition is that high-degree nodes are more likely to be encountered when we sample through edges, because they appear many times in the edge list.

## Erdős-Rényi graph
In the Erdős-Rényi random graph model $G(n,p)$, each possible edge between a pair of nodes appears independently with probability $p$.

For a node in $G(n,p)$, the degree follows a binomial distribution:

$$
K \sim \mathrm{Binomial}(n-1, p)
$$

So

$$
\mathbb{E}[K]=(n-1)p
$$

and

$$
\mathrm{Var}(K)=(n-1)p(1-p)
$$

For large $n$ and small $p$ with $(n-1)p\approx \lambda$, this degree distribution is well approximated by a Poisson distribution with mean $\lambda$.

## Degree correlations
Degree correlations describe whether high-degree nodes tend to connect to other high-degree nodes or to low-degree nodes.

### Average nearest-neighbor degree
One way to quantify degree correlations is through the average nearest-neighbor degree as a function of node degree:

$$
k_{nn}(k)
$$

This is often approximated by a power law of the form

$$
k_{nn}(k)\approx a k^\mu
$$

### Interpretation

- If $\mu > 0$, higher-degree nodes tend to have higher-degree neighbors. The network is assortative.
- If $\mu < 0$, higher-degree nodes tend to have lower-degree neighbors. The network is disassortative.
- If $\mu$ is not statistically different from zero, the network is approximately neutral with respect to degree mixing.

Degree correlations matter because they shape how quickly influence, failure, or contagion moves across hubs and peripheral nodes.
