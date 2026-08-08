---
bibliography: references.bib
---

# Flow and Cuts

## Min-cut problem
Given a graph with a source node $s$ and a sink node $t$, a cut $(s,t)$ is a set of edges whose removal disrupts all paths from $s$ to $t$.

In unweighted networks, the min-cut problem asks for the cut with the minimum number of edges.

In weighted networks, the min-cut is the cut with minimum total edge weight.

From a control and intervention perspective, min-cut identifies the smallest set of links whose removal can block transmission, flow, or contagion through the system.

## Max-flow problem
The max-flow problem asks for the greatest amount of flow that can originate at $s$ and terminate at $t$, subject to:

- Capacity constraints on edges
- Flow conservation at intermediate nodes

The classical solution method is the Ford-Fulkerson algorithm.

Max-flow is useful when we want to understand not just whether a system is connected, but how much material, information, traffic, or energy it can transmit under constraints.

## Max-flow = min-cut
The sum of the weights of the min-cut is equal to the max-flow in that network.

## How this is related to infrastructure systems
