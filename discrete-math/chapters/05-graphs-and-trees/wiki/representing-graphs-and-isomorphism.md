# Representing Graphs and Recognizing Isomorphism

> **Main concept:** Graphs

## Definition

Graphs may begin as pictures of dots and lines, but computers don't "see" pictures: they store data. To analyze a graph, we need a way to translate its structure into a form a computer can process efficiently. Graphs can be represented using lists and matrices, and those representations influence performance and memory.
> Source: Representing Graphs and Recognizing Isomorphism.html

## Key Concepts

### Why Representations Matter

Depending on how we store a graph, some questions become easy to answer and others take much longer:
- Want to know which cities are directly connected by a road? → a list is enough.
- Need to check if two specific cities are connected instantly? → a matrix makes that quick.
- Tracking how edges connect to vertices precisely? → use an incidence matrix (rows correspond to vertices and columns correspond to edges).

Each representation shows the same information, but in a different way.
> Source: Representing Graphs and Recognizing Isomorphism.html

Analogy: think of a graph like a novel. An adjacency list is the table of contents, telling you which chapters (vertices) connect. An adjacency matrix is the index, letting you look up any connection instantly. An incidence matrix is the editor's blueprint, listing how every chapter and reference (edge) interrelate.
> Source: Representing Graphs and Recognizing Isomorphism.html

### Adjacency Lists

An **adjacency list** stores, for each vertex, a list of all vertices directly connected to it.
> Source: Representing Graphs and Recognizing Isomorphism.html

- ✅ **Advantages:** space-efficient for sparse graphs (few edges); easy to iterate through neighbours of a vertex; simple to store and update dynamically.
  > Source: Representing Graphs and Recognizing Isomorphism.html
- ⚠️ **Drawbacks:** checking if two vertices are connected requires searching through a list; less efficient for dense graphs with many edges.
  > Source: Representing Graphs and Recognizing Isomorphism.html

### Adjacency Matrices

An **adjacency matrix** uses a square grid to show which vertices are connected. Each cell contains a number if their vertices are connected, and 0 otherwise.
> Source: Representing Graphs and Recognizing Isomorphism.html

- ✅ **Advantages:** fast to check adjacency — a single lookup; ideal for algorithms requiring frequent access to edges; naturally extends to weighted graphs by replacing 1s with edge weights.
  > Source: Representing Graphs and Recognizing Isomorphism.html
- ⚠️ **Drawbacks:** uses O(n²) memory, even if few edges exist; inefficient for sparse graphs with many empty cells.
  > Source: Representing Graphs and Recognizing Isomorphism.html

### Incidence Matrices

An **incidence matrix** focuses on edges instead of pairs of vertices. It records which vertices each edge touches.
> Source: Representing Graphs and Recognizing Isomorphism.html

- ✅ **Advantages:** captures explicit vertex–edge relationships; useful for network flow and optimization problems; works well with algorithms analyzing edge properties.
  > Source: Representing Graphs and Recognizing Isomorphism.html
- ⚠️ **Drawbacks:** larger matrices for dense graphs (many edges); more complex to interpret visually.
  > Source: Representing Graphs and Recognizing Isomorphism.html

### Comparison Summary

| Representation | Memory Use | Fast for... | Common Use Cases |
|---|---|---|---|
| Adjacency List | Low (depends on number of edges) | Traversing neighbours | Sparse graphs, social networks |
| Adjacency Matrix | High (n²) | Checking if two vertices are connected | Dense graphs, graph algorithms |
| Incidence Matrix | Moderate to High | Studying edge–vertex relationships | Network flow, transportation, optimization |

Each representation captures the same graph, but optimizes for different goals. Choosing the right one depends on how you plan to use the graph — are you searching, comparing or analyzing flow?
> Source: Representing Graphs and Recognizing Isomorphism.html

### Directed Graph Degrees and Balance

In a directed graph, each edge has a clear starting point and endpoint, so every vertex can have two different kinds of degree:
- **Out-degree deg⁺(v):** number of edges leaving v — think of it as how many messages you send.
- **In-degree deg⁻(v):** number of edges entering v — how many you receive.
> Source: Representing Graphs and Recognizing Isomorphism.html

**Theorem: Balance of In- and Out-Degrees** — Let G = (V, E) be a directed graph. Then

> Σ<sub>v ∈ V</sub> deg⁻(v) = Σ<sub>v ∈ V</sub> deg⁺(v) = |E|

Each directed edge adds one count to someone's out-degree (the sender) and one to someone's in-degree (the receiver). Since every edge connects exactly two vertices in this way, the total in-degree and total out-degree must always be equal and both equal the total number of edges.
> Source: Representing Graphs and Recognizing Isomorphism.html

### Isomorphism

**Definition: Isomorphic** — Two graphs G = (V, E) and H = (W, F) are isomorphic if there exists a one-to-one correspondence between their vertices such that edges are preserved. That means if two vertices are connected in G, their corresponding vertices are connected in H.
> Source: Representing Graphs and Recognizing Isomorphism.html

**How to tell if graphs are isomorphic:**
1. **Count vertices and edges** — they must match.
2. **Compare degrees** — each vertex must correspond to another with the same degree.
3. **Compare adjacency patterns** — neighbour sets must match under the mapping.
> Source: Representing Graphs and Recognizing Isomorphism.html

## Examples

- **Adjacency list** for the graph on vertices A, B, C, D with edges AB, AC, BC, BD, CD:

  | Vertex | Neighbours |
  |---|---|
  | A | B, C |
  | B | A, C, D |
  | C | A, B, D |
  | D | B, C |
  > Source: Representing Graphs and Recognizing Isomorphism.html

- **Adjacency matrix** for the same graph:

  |  | A | B | C | D |
  |---|---|---|---|---|
  | A | 0 | 1 | 1 | 0 |
  | B | 1 | 0 | 1 | 1 |
  | C | 1 | 1 | 0 | 1 |
  | D | 0 | 1 | 1 | 0 |
  > Source: Representing Graphs and Recognizing Isomorphism.html

- **Incidence matrix** for the same graph with edges e₁ = (A,B), e₂ = (A,C), e₃ = (B,C), e₄ = (B,D), e₅ = (C,D):

  |  | e₁ | e₂ | e₃ | e₄ | e₅ |
  |---|---|---|---|---|---|
  | A | 1 | 1 | 0 | 0 | 0 |
  | B | 1 | 0 | 1 | 1 | 0 |
  | C | 0 | 1 | 1 | 0 | 1 |
  | D | 0 | 0 | 0 | 1 | 1 |
  > Source: Representing Graphs and Recognizing Isomorphism.html

- **Balanced digraph:** In a digraph where deg⁺(a) = deg⁺(b) = deg⁺(c) = deg⁺(d) = 1 and deg⁻(a) = deg⁻(b) = deg⁻(c) = deg⁻(d) = 1: total in-degree = 4, total out-degree = 4, and |E| = 4. Both sums equal the number of edges, confirming the theorem. Every vertex sends one edge and receives one, so the flow through the graph is perfectly balanced.
  > Source: Representing Graphs and Recognizing Isomorphism.html
- **Applying the balance theorem:** If a digraph has 8 edges, the total sum of in-degrees must be 8 — the total in-degree equals total edges.
  > Source: Representing Graphs and Recognizing Isomorphism.html/practice/config-1762367216671.practice.json
- **Isomorphic mapping:** Two graphs G and H look different, but mapping u₁ → v₁, u₂ → v₃, u₃ → v₂, u₄ → v₄ makes all edges correspond perfectly.
  > Source: Representing Graphs and Recognizing Isomorphism.html
- **Not isomorphic (worked example):** Two graphs each have 5 vertices and 6 edges. Left graph degrees: deg(a) = 2, deg(b) = 2, deg(c) = 3, deg(d) = 2, deg(e) = 3. Right graph degrees: deg(a) = 4, deg(b) = 2, deg(c) = 3, deg(d) = 2, deg(e) = 1. Since the degree sequences differ, there's no one-to-one correspondence that preserves adjacency patterns — no vertex on the left has 4 neighbours like `a` does on the right. **Conclusion:** the graphs are not isomorphic. Same number of vertices and edges ✔️, but different degree sequences ❌, therefore their adjacency patterns cannot match.
  > Source: Representing Graphs and Recognizing Isomorphism.html

## Common Misconceptions

- **"An in-degree of 3 means the vertex has three total connections."** Too vague — "total connections" could mean in or out. In-degree specifically measures incoming edges (it receives edges from three other vertices), while total degree in a directed graph would be the sum of in-degree and out-degree. Three *outgoing* connections would be an out-degree of 3.
  > Source: Representing Graphs and Recognizing Isomorphism.html/practice/config-1762366887074.practice.json
- **"A self-loop only affects one kind of degree."** A self-loop contributes 1 to both in-degree and out-degree for the same vertex.
  > Source: Representing Graphs and Recognizing Isomorphism.html/practice/config-1762366887074.practice.json
- **"Matching vertex and edge counts prove two graphs are isomorphic."** Not sufficient — the degree sequences must also match, and the adjacency patterns must correspond under the mapping.
  > Source: Representing Graphs and Recognizing Isomorphism.html
- **"An incidence matrix is the square grid of 0s and 1s recording whether vertices are connected."** No — that is the adjacency matrix. The incidence matrix focuses on vertex–edge relationships, and the adjacency list uses lists of neighbours.
  > Source: Representing Graphs and Recognizing Isomorphism.html/practice/config-1762366319899.practice.json

## Related Topics

- [Understanding Graphs](understanding-graphs.md)
- [Degrees, Adjacency and Graph Properties](degrees-adjacency-and-graph-properties.md)
- [Graph Types, Connectivity and Components](graph-types-connectivity-and-components.md)
- [Introducing Trees and Forests](trees-and-forests.md)
