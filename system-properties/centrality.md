# Centrally

## Centrality measures
### Degree
The simplest measure. A node's degree is just the **count of direct connections (edges) it has**. A node connected to 10 others has degree 10. It tells you who has the most immediate neighbors, but nothing about the quality or reach of those connections.

### Eigenvector
Captures the idea that **not all connections are equal** — being connected to well-connected nodes makes you more important. A node's eigenvector centrality score is proportional to the _sum of its neighbors' scores_, solved simultaneously across the whole network (hence the eigenvector). Google's original PageRank algorithm is a well-known variant of this idea. It rewards nodes that are connected to other influential nodes, not just many nodes.

### Betweenness
Measures how often a node sits **on the shortest path between other pairs of nodes**. You find the shortest route between every pair of nodes in the network, then count how many of those routes pass through each node. A node with high betweenness is a critical **bridge or bottleneck** — information or flow passing across the network likely goes through it. Removing a high-betweenness node can fragment the network.

### Strength
An extension of degree for **weighted networks**. Instead of counting edges, you **sum the weights** of all edges attached to a node. For example, if connections represent how often two people email each other, strength captures total communication volume — not just how many contacts you have, but how active those relationships are.

### Comparison

| Measure         | Core Question               | Weighted? | Global awareness? |
| --------------- | --------------------------- | --------- | ----------------- |
| **Degree**      | How many neighbors?         | No        | No                |
| **Strength**    | How strong are my ties?     | Yes       | No                |
| **Betweenness** | Am I a bridge?              | Optional  | Yes               |
| **Eigenvector** | Are my neighbors important? | Optional  | Yes               |
