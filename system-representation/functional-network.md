---
bibliography: references.bib
---

# Functional netowrk

## Network
A network is defined in graph theory as a set of nodes or vertices and the edges or lines between them.

Structural and functional network can be explored using graph theory through the following four steps {cite}`bullmore2009`:
- Define the network nodes
- Estimate a continuous measure of association between nodes
- Generate an association matrix by compiling all pairwise associations between nodes and usually apply a threshold to each element of this matrix to produce a binary adjacency matrix or undirected graph
- Calculate the network parameters of interest in this graphical model of a brain network and compare them to the equivalent parameters of a population of random networks

## Construction of functional network
A structural network encodes the physical connections between elements: wires, pipes, axons, roads. A functional network, by contrast, is derived from observed behavior, specifically, from statistical associations in how elements co-vary or co-activate over time, regardless of whether a direct physical link exists between them.

## Functional network types

| Undirected               | Directed                    |
| ------------------------ | --------------------------- |
| Covariance / correlation | Granger causality           |
| Mutual information       | Transfer entropy            |
| Spectral coherence       | Convergent cross mapping    |
| Phase sync / DTW         | Causal discovery (PC / FCI) |
| Recurrence networks      | Structural VAR / SEM        |


## Structure–function relations
In the context of brain networks, the functionality of an individual neural node is partly determined by the pattern of its interconnections with other node in the network. Nodes with similar connection patterns tend to exhibit similar functionality {cite}`bullmore2009`.

Structural and functional networks are related but not identical. Direct physical connections strongly predict functional coupling, but indirect pathways also generate functional linkages: two nodes with no direct connection may be strongly co-active if they share many common neighbors or if they occupy similar positions in the network. Conversely, physical connections do not guarantee functional coupling. A connection may be present but inactive under a given operating regime. This partial decoupling of structure and function is precisely what makes functional network analysis informative: it reveals which structural pathways are actually operative, and under what conditions.

## How this connects to infra systems
Why construct a functional network on top of a system whose topology is already known?

The structural network describes what _can_ interact; the functional network describes what _does_ interact. Both are necessary for a complete account of infrastructure system behavior.

In a power grid, for example, two substations may be separated by several electrical hops yet exhibit tightly correlated voltage behavior due to shared load patterns, common upstream sources, or system-wide oscillation modes. Conversely, two directly connected nodes may decouple functionally under specific dispatch configurations or protective relay actions. A functional network, derived from observed operational co-variation, captures these _effective dependencies_ — the relationships that actually govern system behavior under real conditions.

This distinction matters most in three contexts:
- First, in resilience analysis: cascade failures propagate through functional dependencies, not just physical links. A failure in a structurally peripheral node may trigger widespread correlated failures if that node is functionally central. 
- Second, in anomaly detection and monitoring: deviations in functional network topology, like shifts in clustering, path length, or hub connectivity, can serve as early indicators of stress or degradation before physical failure occurs. 
- Third, in system design and intervention: identifying the functional hubs and bridging edges in an infrastructure network allows planners to target hardening investments where operational impact, not just physical degree, is highest.

:::{bibliography}
:::
