# Introducing Trees and Forests

> **Main concept:** Trees & Forests

## Definition

**Definition: Tree** — A tree is a connected, undirected graph with no simple circuits (no closed loops).
> Source: Introducing Trees and Forests.html

Because a tree cannot contain a circuit, it also cannot have multiple edges or loops. This means **every tree is a simple graph**: one connection between any two vertices, and no edge that starts and ends at the same vertex.
> Source: Introducing Trees and Forests.html

**Definition: Forest** — A forest is a graph that contains no simple circuits, but may have more than one connected component. Each connected component of a forest is a tree.
> Source: Introducing Trees and Forests.html

## Key Concepts

- **A tree is a special kind of graph:** it strips away all the excess, keeping only what's needed to stay connected. Trees are the simplest connected graphs — structures that grow by branching without ever looping back.
  > Source: Introducing Trees and Forests.html
- **Both conditions are required:** to be a tree, a graph must be connected **and** contain no cycles. Cycles violate the definition of a tree; direction is not part of the definition.
  > Source: Introducing Trees and Forests.html/practice/config-1762986056116.practice.json
- **Theorem: Unique Path Property** — An undirected graph is a tree if and only if there is a unique simple path between every pair of its vertices. In other words: if a graph is connected and has no cycles, only one path can connect any two vertices; and if exactly one simple path exists between every pair of vertices, the graph must be connected and acyclic — a tree.
  > Source: Introducing Trees and Forests.html
- **Forests as separate hierarchies:** Forests appear naturally when systems split into independent hierarchies — like multiple databases, isolated networks or separate family branches. A forest is like having several separate hierarchies, such as multiple independent file systems or family branches that never connect.
  > Source: Introducing Trees and Forests.html
- **Edge count:** A tree always has one fewer edge than vertices.
  > Source: Introducing Trees and Forests.html/practice/config-1762986056116.practice.json

## A Brief History

Trees have been studied for more than 150 years. As early as 1857, the English mathematician Arthur Cayley used them to count certain types of chemical compounds, which marks one of the earliest applications of graph theory to real-world problems.
> Source: Introducing Trees and Forests.html

In computer science, trees are indispensable. They're used to:
- Design efficient search and sorting algorithms.
- Build data structures such as binary trees, heaps and tries.
- Construct Huffman codes for data compression and transmission.
- Model decision processes, helping to analyze the complexity of algorithms.
- Support game strategies, such as exploring possible moves in chess or checkers.
- Enable systematic exploration through depth-first and breadth-first search, used in everything from network analysis to solving puzzles like the eight queens problem.
> Source: Introducing Trees and Forests.html

Trees show up wherever we need to organize, search and make decisions efficiently. They're the foundation for modeling processes, relationships and hierarchies in computing.
> Source: Introducing Trees and Forests.html

## Examples

- **File systems:** folders contain subfolders and files, but they never form loops.
  > Source: Introducing Trees and Forests.html
- **Family trees:** show how generations branch from common ancestors.
  > Source: Introducing Trees and Forests.html
- **Decision trees:** each question leads to a branch of possible outcomes.
  > Source: Introducing Trees and Forests.html
- **Unique path in action:** In a file system, there's exactly one path from the root directory to any file.
  > Source: Introducing Trees and Forests.html
- **Identifying trees (worked example):** Of four graphs G₁–G₄: G₁ and G₂ are trees since both are connected and contain no circuits. G₃ is not a tree, because it contains a simple circuit e–b–a–d–e. G₄ is not a tree, because it's disconnected.
  > Source: Introducing Trees and Forests.html
- **Forest example:** One graph with three connected components, none of which contain circuits, is a forest.
  > Source: Introducing Trees and Forests.html
- **Disconnected and acyclic:** A graph that is disconnected but contains no cycles is a **forest** — a collection of disconnected trees. It is not a tree (a tree must be connected).
  > Source: Introducing Trees and Forests.html/practice/config-1762986150819.practice.json

## Common Misconceptions

- **"A graph can have cycles as long as it's connected and still be a tree."** Incorrect — cycles violate the definition of a tree.
  > Source: Introducing Trees and Forests.html/practice/config-1762986056116.practice.json
- **"A tree must be directed."** Incorrect — direction isn't part of the definition of a tree.
  > Source: Introducing Trees and Forests.html/practice/config-1762986056116.practice.json
- **"A tree has equal numbers of vertices and edges."** Incorrect — a tree always has one fewer edge than vertices.
  > Source: Introducing Trees and Forests.html/practice/config-1762986056116.practice.json
- **"There can be two or more simple paths between two vertices in a tree."** Incorrect — having two paths would create a cycle. Exactly one simple path exists between any two vertices in a tree.
  > Source: Introducing Trees and Forests.html/practice/config-1762986236656.practice.json

## Related Topics

- [Graph Types, Connectivity and Components](graph-types-connectivity-and-components.md)
- [Anatomy of a Tree](anatomy-of-a-tree.md)
- [Traversing Trees](traversing-trees.md)
- [Applications of Trees](applications-of-trees.md)
