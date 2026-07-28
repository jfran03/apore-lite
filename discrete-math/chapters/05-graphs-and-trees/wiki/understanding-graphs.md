# Understanding Graphs

> **Main concept:** Graphs

## Definition

A graph is the mathematical model that captures the idea of connected entities. A graph consists of:
- **V**: a non-empty set of vertices (or nodes), and
- **E**: a set of edges (or links) connecting pairs of vertices.

Each edge has one or two vertices associated with it, called its endpoints. We write this as **G = (V, E)**.
> Source: Understanding Graphs.html

Graphs can describe simple relationships like "A is connected to B," or complex ones involving direction, weight and structure.
> Source: Understanding Graphs.html

## Key Concepts

- **Vertex (Node):** An object, entity or point — for example a city, person or computer.
  > Source: Understanding Graphs.html
- **Edge (Link):** A relationship or connection between vertices — for example a road, friendship or data link.
  > Source: Understanding Graphs.html
- **Endpoints:** The vertices connected by an edge — for example the cities connected by a road.
  > Source: Understanding Graphs.html
- **Graph:** The entire structure of vertices and edges — for example a road map.
  > Source: Understanding Graphs.html
- **Finite graph:** A finite graph has a limited number of nodes and connections. Most real-world networks fall into this category. A finite graph has a specific, countable number of vertices and edges.
  > Source: Understanding Graphs.html; Understanding Graphs.html/practice/config-1761844212066.practice.json
- **Infinite graph:** An infinite graph extends without limit; these often appear in theoretical contexts, like modeling number sequences or infinite grids.
  > Source: Understanding Graphs.html
- **Structure over layout:** Graphs can look very different on the page, but what matters is which vertices are connected, not how they are arranged visually. A single graph can be drawn in many ways while keeping its structure identical.
  > Source: Understanding Graphs.html
- **Entities and connections:** Every network example involves entities (people, places, devices, pages) and connections between them.
  > Source: Understanding Graphs.html

## Examples

- **Everyday networks:** Social networks (people connected by friendships or follows); technological networks (cities or intersections connected by roads, subway lines or flight routes; computers, servers and phones exchanging data through wired or wireless links); web networks (web pages connected through hyperlinks).
  > Source: Understanding Graphs.html
- **Social network:** each vertex is a person, and each edge is a friendship.
  > Source: Understanding Graphs.html
- **Metro network:** vertices are stations, and edges are rails between them.
  > Source: Understanding Graphs.html
- **Computer network:** vertices are devices, and edges represent communication channels.
  > Source: Understanding Graphs.html
- **Airline network:** the vertices represent airports — a location that can connect to others through flight routes (the edges). Flights are better represented by edges; passengers travel between vertices but are not part of the graph structure itself.
  > Source: Understanding Graphs.html/practice/config-1761844138986.practice.json
- **Two drawings, one graph:** The drawings `(A)——(B) / (D)——(C)` and `(D)——(A) / (C)——(B)` change the layout, but the connections remain identical.
  > Source: Understanding Graphs.html

## Applications in Computer Science

- **Routing and navigation:** GPS and delivery systems use graphs to find the shortest or least expensive path between locations.
  > Source: Understanding Graphs.html
- **Dependency management:** Compilers and project planners use graphs to track which modules depend on which others.
  > Source: Understanding Graphs.html
- **Web search and recommendation engines:** Graphs represent links between pages, people or products.
  > Source: Understanding Graphs.html
- **Cybersecurity:** Attack graphs model possible pathways an attacker could exploit.
  > Source: Understanding Graphs.html

These applications depend on the mathematical properties of graphs to ensure efficient, reliable decision-making.
> Source: Understanding Graphs.html

## Common Misconceptions

- **"Rearranging how a graph is drawn can change the relationships between vertices."** This is false. The layout might look different, but the connections between vertices remain the same — the relationships depend only on which vertices are connected, not how they appear visually.
  > Source: Understanding Graphs.html/practice/config-1761844275636.practice.json; Understanding Graphs.html
- **"A finite graph is one that contains no connections."** Not correct — a graph with no connections would be a set of isolated vertices, not necessarily finite or infinite. Loops likewise describe edge type, not graph size.
  > Source: Understanding Graphs.html/practice/config-1761844212066.practice.json

## Related Topics

- [Graph Types, Connectivity and Components](graph-types-connectivity-and-components.md)
- [Degrees, Adjacency and Graph Properties](degrees-adjacency-and-graph-properties.md)
- [Representing Graphs and Recognizing Isomorphism](representing-graphs-and-isomorphism.md)
