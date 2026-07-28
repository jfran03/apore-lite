# Graph Types, Connectivity and Components

> **Main concept:** Graphs

## Definition

Not all graphs describe connections in the same way. Some connections have direction, some can repeat and others may include loops or even be disconnected. Graphs are classified based on their structure, and concepts like paths, cycles and connectivity describe how vertices relate to one another.
> Source: Graph Types, Connectivity, and Components.html

## Key Concepts

### Basic Types of Graphs

- **Undirected graph:** A graph where edges have no direction. If there's an edge between A and B, you can travel both ways: from A to B and from B to A. This kind of graph models mutual relationships, such as friendships or shared links.
  > Source: Graph Types, Connectivity, and Components.html
- **Directed graph (digraph):** A graph that has arrows showing the direction of each connection. An edge from A to B means you can go from A → B, but not necessarily B → A.
  > Source: Graph Types, Connectivity, and Components.html
- **Mixed graph:** A graph that combines both directed and undirected edges in the same diagram. Useful when some relationships are mutual and others are one-way.
  > Source: Graph Types, Connectivity, and Components.html
- **Multigraph:** A graph that allows multiple edges (parallel edges) between the same vertices but no self-loops.
  > Source: Graph Types, Connectivity, and Components.html
- **Pseudograph:** A graph that may include loops, and possibly multiple edges connecting the same pair of vertices or a vertex to itself.
  > Source: Graph Types, Connectivity, and Components.html

### Movement Through a Graph

- **Walk:** Any sequence of edges that connects vertices, allowing repetition of both vertices and edges — e.g. A → B → C → B → D. Think of a walk like wandering through a city: you can pass through the same street more than once.
  > Source: Graph Types, Connectivity, and Components.html
- **Path:** A special kind of walk where no vertex is repeated — e.g. A → B → C → D. Paths represent the simplest route without retracing steps.
  > Source: Graph Types, Connectivity, and Components.html
- **Cycle:** A path that starts and ends at the same vertex, with all other vertices distinct — e.g. A → B → C → A. A cycle forms a closed loop; once you return to the start, you've completed a circuit.
  > Source: Graph Types, Connectivity, and Components.html

### Connectivity

- **Connected graph:** An undirected graph is connected if every vertex is reachable from every other vertex. That means you can start anywhere and eventually reach any other vertex by following edges.
  > Source: Graph Types, Connectivity, and Components.html
- **Disconnected graph:** A graph that has two or more parts that are not connected by any edge.
  > Source: Graph Types, Connectivity, and Components.html
- **Component:** Each isolated "part" of a disconnected graph is called a component.
  > Source: Graph Types, Connectivity, and Components.html

## Examples

- **Mixed graph in practice:** In a communication network, some links allow two-way data transfer, while others only send in one direction.
  > Source: Graph Types, Connectivity, and Components.html
- **Connected:** In a connected road network, every city is reachable from every other city.
  > Source: Graph Types, Connectivity, and Components.html
- **Disconnected:** If two islands have no bridge or ferry between them, their transportation networks form separate disconnected graphs. Written as `A —— B    C —— D`, there is no path connecting the two sets of vertices.
  > Source: Graph Types, Connectivity, and Components.html; Graph Types, Connectivity, and Components.html/practice/config-1761848770111.practice.json
- **Components:** Two disconnected Wi-Fi networks would form two components: devices in one can't communicate with the other. Written as `(A —— B —— C) (D —— E)`.
  > Source: Graph Types, Connectivity, and Components.html
- **Notation for a single directed edge:** `A → B` represents a single directed edge; the arrow shows direction from A to B.
  > Source: Graph Types, Connectivity, and Components.html/practice/config-1761848646844.practice.json

## Common Misconceptions

- **"A ↔ B is a single directed edge."** Close, but that indicates two directed edges in opposite directions, not one. `A — B` without an arrow is undirected and could go both ways, and `A = B` shows a parallel but undirected connection.
  > Source: Graph Types, Connectivity, and Components.html/practice/config-1761848646844.practice.json
- **"A directed chain must be disconnected because you can only travel one way."** Incorrect — in `A → B → C → D`, despite direction, every vertex is reachable in this chain. Likewise `A —— B —— C ——— A` is a connected cycle, not disconnected.
  > Source: Graph Types, Connectivity, and Components.html/practice/config-1761848770111.practice.json

## Related Topics

- [Understanding Graphs](understanding-graphs.md)
- [Degrees, Adjacency and Graph Properties](degrees-adjacency-and-graph-properties.md)
- [Introducing Trees and Forests](trees-and-forests.md)
