# Degrees, Adjacency and Graph Properties

> **Main concept:** Graphs

## Definition

Graphs become powerful when we move beyond drawing connections to analyzing them. Mathematical properties like degree, adjacency and connectivity let us describe how vertices interact and predict how a network will behave.
> Source: Degrees, Adjacency, and Graph Properties.html

A graph G is defined as **G = (V, E)** where V is a non-empty set of vertices (nodes) and E is a set of edges (links) connecting pairs of vertices. Each edge connects one or two vertices called its endpoints. Edges are written as ordered or unordered pairs depending on whether the graph is directed or undirected.
> Source: Degrees, Adjacency, and Graph Properties.html

## Key Concepts

### Graph Notation

| Graph Type | Edge Notation | Example |
|---|---|---|
| Undirected | (u, v) or {u, v} | {A, B} means A is connected to B |
| Directed | ⟨u, v⟩ or (u → v) | A → B means a directed edge from A to B |

So `{A, B}` and `{B, A}` describe the same edge in an undirected graph, but `A → B` and `B → A` are different in a directed one.
> Source: Degrees, Adjacency, and Graph Properties.html

By expressing a graph as a set, we can use logic, counting and algebra to uncover deep patterns — it translates a map into a data structure that algorithms can navigate.
> Source: Degrees, Adjacency, and Graph Properties.html

### Adjacency and Neighbourhoods

- **Adjacent:** Two vertices u and v are adjacent if an edge connects them. That edge is said to be **incident** with both vertices. In `A —— B —— C`, A and B are adjacent (they share an edge) but A and C are not adjacent (no direct connection).
  > Source: Degrees, Adjacency, and Graph Properties.html
- **Direction of adjacency:** In a directed graph, if A → B, then A is adjacent *to* B, and B is adjacent *from* A.
  > Source: Degrees, Adjacency, and Graph Properties.html
- **Neighbourhood N(v):** The neighbourhood of a vertex shows its immediate surroundings — the set of vertices directly connected to it. If vertex A connects to B and C, then N(A) = {B, C}. This captures the local structure of the network, or what's directly reachable in one step.
  > Source: Degrees, Adjacency, and Graph Properties.html

### Degree of a Vertex

- **Degree:** The number of edges incident to a vertex. The degree of a vertex tells us a lot about its role in the network: some vertices act as hubs with many connections, while others sit quietly at the edge or apart from the system entirely.
  > Source: Degrees, Adjacency, and Graph Properties.html
- **Undirected graphs:** Each edge contributes 1 to the degree of both its endpoints. **A loop at a vertex counts twice** (once as start and once as end).
  > Source: Degrees, Adjacency, and Graph Properties.html
- **Directed graphs:** Each vertex has two measures of degree — **in-degree** indeg(v), the number of edges entering the vertex, and **out-degree** outdeg(v), the number of edges exiting the vertex.
  > Source: Degrees, Adjacency, and Graph Properties.html
- **Isolated vertex:** degree = 0 → has no incident edges.
  > Source: Degrees, Adjacency, and Graph Properties.html
- **Pendant vertex:** degree = 1 → connects to only one other vertex.
  > Source: Degrees, Adjacency, and Graph Properties.html

These distinctions matter: in graph algorithms, isolated vertices can signal failure points and pendant vertices often mark boundaries of communication or influence.
> Source: Degrees, Adjacency, and Graph Properties.html

### The Handshake Lemma

**The Handshake Lemma** — for any undirected graph G = (V, E) with m edges:

> 2m = Σ<sub>v ∈ V</sub> deg(v)

This tells us that every edge connects two vertices and that each connection contributes 1 to the degree of both endpoints, so it's counted twice.
> Source: Degrees, Adjacency, and Graph Properties.html

**Theorem: Parity of Odd Vertices** — In every undirected graph, the number of vertices of odd degree is even. This is a direct consequence of the Handshaking Lemma; it tells us that degree balance is mathematically required. The total degree is always even, meaning odd-degree vertices can only appear in pairs. You can have two, four, six, or more, but never just one or three.
> Source: Degrees, Adjacency, and Graph Properties.html

For directed graphs, a similar relationship holds: the total of all in-degrees equals the total of all out-degrees, and both equal the number of edges.
> Source: Degrees, Adjacency, and Graph Properties.html

### The Königsberg Bridge Problem

In the 1700s, the city of Königsberg, Prussia (now Kaliningrad, Russia) had seven bridges connecting two islands in the Pregel River to each other and to the riverbanks. Residents wondered: "Is it possible to take a walk through the city and cross every bridge exactly once?"
> Source: Degrees, Adjacency, and Graph Properties.html

Leonhard Euler realized this wasn't a problem about geography or navigation: it was a question of connections. He redrew the city as a graph where each landmass became a vertex and each bridge became an edge connecting two vertices. Every land area had an odd number of bridges connected to it:

| Land Area | Bridges (# of degrees) |
|---|---|
| North Bank | 3 |
| South Bank | 3 |
| East Island | 3 |
| Middle Island | 5 |

That meant four vertices with odd degree.
> Source: Degrees, Adjacency, and Graph Properties.html

**The Rule:** A graph can have an Eulerian path (a walk that crosses every edge exactly once) only if it has exactly 0 or 2 vertices of odd degree. Because Königsberg's graph had four odd-degree vertices, Euler proved the walk was impossible.
> Source: Degrees, Adjacency, and Graph Properties.html

When all vertices have even degrees, movement can form perfect loops or cycles. But when some have odd degrees, movement fragments — you can't traverse all edges in a single sweep. Euler's insight became the foundation of graph theory and the first formal proof that linked structure to movement in a network.
> Source: Degrees, Adjacency, and Graph Properties.html

**Why this matters:** routing systems ensure balanced paths for delivery trucks or data packets; circuit design verifies that every node has matching input and output terminals; game design guarantees that a player can traverse every connection exactly once.
> Source: Degrees, Adjacency, and Graph Properties.html

### Special Graph Structures

- **Complete graph (Kₙ):** Connects every vertex to every other vertex exactly once. Each vertex has degree = n − 1, and total edges = n(n − 1)/2. Represents a system with maximum connectivity. Example: a fully meshed network where each server communicates directly with all others.
  > Source: Degrees, Adjacency, and Graph Properties.html
- **Incomplete graph:** If even one possible connection is missing, the graph is incomplete. Example: in a social graph, not everyone is friends with everyone else. Most real-world systems are incomplete.
  > Source: Degrees, Adjacency, and Graph Properties.html
- **Wheel graph (Wₙ):** Combines a central hub with a surrounding cycle. Vertices: n. Edges: 2(n − 1). The hub vertex connects to every point on the rim. Example: airline route maps often form wheel graphs, with one major hub serving multiple regional spokes.
  > Source: Degrees, Adjacency, and Graph Properties.html
- **Bipartite graph:** Divides vertices into two distinct sets V₁ and V₂, where edges only connect vertices across the sets (never within them). When this condition holds, the pair (V₁, V₂) is called a bipartition of the vertex set V of G. Example: in a post-secondary course system, students V₁ = (A, B, E) enroll in courses V₂ = (C, D, F); there are no edges directly connecting students to students or courses to courses.
  > Source: Degrees, Adjacency, and Graph Properties.html
- **Weighted graph:** A graph with values assigned to edges, often representing distance, time or cost. Weights allow us to compute optimal paths such as the fastest route, cheapest connection or least congested link. Example: GPS navigation, shipping logistics and network routing.
  > Source: Degrees, Adjacency, and Graph Properties.html

## Examples

- **Undirected degrees:** In the graph `A —— B`, with A also joined to C and D: deg(A) = 3 (connected to B, C, D), deg(B) = 1, deg(C) = 1, deg(D) = 1.
  > Source: Degrees, Adjacency, and Graph Properties.html
- **Directed degrees:** In `A → B → C` with `B → D`: indeg(A) = 0, outdeg(A) = 1 (to B); indeg(B) = 1 (from A), outdeg(B) = 2 (to C and D); indeg(C) = 1, outdeg(C) = 0; indeg(D) = 1, outdeg(D) = 0. B acts like a small hub (many outgoing connections), C and D are receivers, and A connects only once.
  > Source: Degrees, Adjacency, and Graph Properties.html
- **Special vertices in practice:** In a home network, a printer connected to one router is a pendant vertex. A disconnected IoT sensor that lost its Wi-Fi link becomes an isolated vertex.
  > Source: Degrees, Adjacency, and Graph Properties.html
- **Handshake Lemma:** Imagine 5 people standing in a circle shaking hands with the person next to them. If you add up how many handshakes each person performs, the total will be twice the number of unique handshakes. In the graph where each of A, B, C, D, E has degree 2: edges m = 5, sum of degrees = 10 = 2 × 5.
  > Source: Degrees, Adjacency, and Graph Properties.html
- **Applying the lemma:** A graph has 8 vertices and 10 edges → Σ deg(v) = 2m = 2 × 10 = 20. (8 is the number of vertices, not the degree sum; 10 is the number of edges, not the degree sum.)
  > Source: Degrees, Adjacency, and Graph Properties.html/practice/config-1761867348531.practice.json
- **Reading a degree off a drawing:** A vertex B that connects to A, C and E has degree 3, because it has 3 edges.
  > Source: Degrees, Adjacency, and Graph Properties.html/practice/config-1761867192879.practice.json

## Common Misconceptions

- **"An undirected graph can have exactly three vertices of odd degree."** No — the number of odd-degree vertices must be even, because odd-degree vertices occur in pairs. Vertex parity is unrelated to how many connected components the graph has, and loops affect the degree count but not the parity rule.
  > Source: Degrees, Adjacency, and Graph Properties.html/practice/config-1761867494082.practice.json; Degrees, Adjacency, and Graph Properties.html
- **"A loop adds 1 to a vertex's degree."** A loop at a vertex counts **twice** — once as start and once as end.
  > Source: Degrees, Adjacency, and Graph Properties.html

## Related Topics

- [Understanding Graphs](understanding-graphs.md)
- [Graph Types, Connectivity and Components](graph-types-connectivity-and-components.md)
- [Representing Graphs and Recognizing Isomorphism](representing-graphs-and-isomorphism.md)
