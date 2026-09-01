# Anatomy of a Tree

> **Main concept:** Trees & Forests

## Definition

**Definition: Rooted Tree** — A rooted tree is a tree where one vertex is identified as the root, and every edge is directed outward from it. The root has no parent; all other vertices have exactly one parent.
> Source: Anatomy of a Tree.html

We can change a rooted tree into an unrooted tree by selecting any other vertex as the root. This also means that different choices of the root produce different rooted trees.
> Source: Anatomy of a Tree.html

## Key Concepts

### Terminology

- **Root:** The topmost node, or the starting point of the hierarchy. Example: the main folder in a file system.
  > Source: Anatomy of a Tree.html
- **Parent:** A node directly connected above another. Example: a folder containing subfolders.
  > Source: Anatomy of a Tree.html
- **Child:** A node directly connected below another. Example: a subfolder or file.
  > Source: Anatomy of a Tree.html
- **Siblings:** Nodes with the same parent. Example: files inside the same folder.
  > Source: Anatomy of a Tree.html
- **Leaf:** A node with no children. Example: the lowest-level file.
  > Source: Anatomy of a Tree.html
- **Internal vertex:** A node that has at least one child. Example: a directory that contains other directories.
  > Source: Anatomy of a Tree.html
- **Ancestor / Descendant:** Relative positions in the hierarchy. Example: a folder (ancestor) containing files (descendants).
  > Source: Anatomy of a Tree.html
- **Subtree:** A node together with all its descendants. Example: any smaller branch of the tree.
  > Source: Anatomy of a Tree.html

### Levels and Height

- **Level:** The level of a vertex refers to how far it is from the root of a tree. More precisely, it's the number of edges along the path from the root to that vertex. **The root itself is always at level 0.** Its direct children are at level 1, their children are at level 2, and the pattern continues downward.
  > Source: Anatomy of a Tree.html
- **Height:** The height of a tree is the maximum level among all its vertices. It tells you how many levels the tree has, counting from the root at level 0 to the deepest vertex. The height shows how deep the structure goes — like a file system, where the height is the length of the longest folder path from the main directory down to the deepest subfolder.
  > Source: Anatomy of a Tree.html

### m-ary and Binary Trees

**Definition: m-ary tree** — A rooted tree is called an m-ary tree if every internal vertex has no more than m children. The tree is called a **full m-ary tree** if every internal vertex has exactly m children. An m-ary tree with m = 2 is called a **binary tree**.
> Source: Anatomy of a Tree.html

- **Branching factor (m):** The answer to "how many branches can each node grow?" You can think of m as the "fan-out," or how wide the tree's canopy can spread at each step. The branching factor controls how information expands — in computing, increasing m changes how quickly data structures grow and how much memory they need.
  > Source: Anatomy of a Tree.html
- **Binary tree (m = 2):** each internal node has up to two children. Think of it like a "yes/no" decision tree, or a tournament bracket.
  > Source: Anatomy of a Tree.html
- **Ternary tree (m = 3):** each internal node has up to three children. This could be a game where every position offers three possible moves.
  > Source: Anatomy of a Tree.html
- **Full m-ary tree:** every internal node has exactly m children — a perfectly regular branching pattern, like a balanced organization chart.
  > Source: Anatomy of a Tree.html
- **Kinds of binary tree:** A binary tree can be **full** (every internal node has two children), **complete** (every level except the last is full), or **arbitrary** (some nodes have one or no children).
  > Source: Anatomy of a Tree.html
- **Growth:** Each internal node creates up to m new branches. Tree growth follows geometric progressions: each level multiplies possible nodes by m.
  > Source: Anatomy of a Tree.html

### Theorems

- **Theorem:** A tree with n vertices has **n − 1 edges**.
  > Source: Anatomy of a Tree.html
- **Theorem:** A full m-ary tree with i internal vertices contains **n = mi + 1** vertices.
  > Source: Anatomy of a Tree.html
- **Theorem (internal vertices and leaves):** A full m-ary tree with
  - n vertices has **i = (n − 1)/m** internal vertices and **l = [(m − 1)n + 1]/m** leaves,
  - i internal vertices has **n = mi + 1** vertices and **l = (m − 1)i + 1** leaves,
  - l leaves has **n = (ml − 1)/(m − 1)** vertices and **i = (l − 1)/(m − 1)** internal vertices.

  These formulas mean that if you know how many internal vertices exist, you can compute how many leaves the tree will have, and vice versa.
  > Source: Anatomy of a Tree.html

Every new level multiplies leaves rapidly, so the number of terminal nodes always grows faster than the number of internal ones.
> Source: Anatomy of a Tree.html

### Ordered Rooted Trees

An **ordered rooted tree** is one where the children of each node are arranged in a specific sequence, usually from left to right. This means that even if two trees contain the same vertices and edges, changing the order of the children can create a different tree. Ordered trees are important when sequence affects meaning, outcome or evaluation.
> Source: Anatomy of a Tree.html

### Balanced Trees

**Definition: Balance** — A rooted m-ary tree of height h is balanced if all leaves are at levels h or h − 1. This means every leaf is either on the last level or one level above it; no branch extends dramatically further than the rest.
> Source: Anatomy of a Tree.html

A balanced tree ensures that data access, search and traversal take roughly the same number of steps no matter where information sits. When trees become skewed, performance can degrade.
> Source: Anatomy of a Tree.html

Think about searching for a file on your computer: in a balanced directory structure, every file is just a few folders away; in an unbalanced one, you might dig through a long chain of nested folders. Balanced trees minimize that depth, which keeps access fast and predictable.
> Source: Anatomy of a Tree.html

## Examples

- **Worked structure:** For the tree with root A, children B, C, D; B's children E, F; D's child G:

  | Node | Parent | Children | Degree |
  |---|---|---|---|
  | A | — | B, C, D | 3 |
  | B | A | E, F | 2 |
  | C | A | — | 0 |
  | D | A | G | 1 |
  | E | B | — | 0 |
  | F | B | — | 0 |
  | G | D | — | 0 |

  In this example: A is the root; E, F, C, G are leaves; the subtree rooted at B contains B, E, F. A is at level 0; B, C and D are at level 1; E, F and G are at level 2. The highest level is 2, so the tree's height is 2.
  > Source: Anatomy of a Tree.html; Anatomy of a Tree.html/practice/config-1762991533061.practice.json
- **Sibling relationships:** In that same tree, F is a sibling of E because F and E share the same parent, B. C is not the parent of D — C and D share the same parent (A), so they are siblings. G is part of the branch under D, not C. A is not a leaf: it has children (B, C, D), so it's the root.
  > Source: Anatomy of a Tree.html/practice/config-1762990747688.practice.json
- **Complete binary tree:** In the tree with root A, children B and C, and leaves D, E (under B) and F (under C): A is the root, B and C are its children, and D, E, F are leaves. It's a complete binary tree because all levels are full except the last, which fills from left to right.
  > Source: Anatomy of a Tree.html
- **m-ary growth:** A binary tree (m = 2) with 3 levels can hold up to 7 nodes. A ternary tree (m = 3) with 3 levels can hold up to 13 nodes. A 4-ary tree (m = 4) with 3 levels can hold up to 21 nodes.
  > Source: Anatomy of a Tree.html
- **Applying n = mi + 1:** Each node has exactly three children (m = 3) and there are four internal nodes (i = 4). Then n = 3(4) + 1 = 13, so the tree has 13 vertices in total. Every internal node contributes m new nodes, plus one root that anchors the structure.
  > Source: Anatomy of a Tree.html
- **Full 3-ary tree with 5 internal vertices:** n = mi + 1 = 3(5) + 1 = 16 and l = (m − 1)i + 1 = (2)(5) + 1 = 11.

  | Quantity | Symbol | Value |
  |---|---|---|
  | Internal Vertices | i | 5 |
  | Leaves | l | 11 |
  | Total Vertices | n | 16 |
  | Edges | n − 1 | 15 |
  > Source: Anatomy of a Tree.html
- **Ordered trees matter:** Imagine a root with two children, B and C. In one version B comes before C; in another, C comes before B. Both have the same connections, but their meanings can differ completely, much like the sentences "cats chase dogs" and "dogs chase cats." Similarly in a file directory, all files may live inside the same folder, but their order (alphabetical, by date, by type) affects how they're displayed or accessed.
  > Source: Anatomy of a Tree.html
- **Balanced vs unbalanced:** A tree with root A, children B and C, and leaves at levels 2 and 3 is balanced. A tree where one branch extends far deeper than the others is unbalanced.
  > Source: Anatomy of a Tree.html
- **Why these relationships matter:** In a binary search tree, each additional level doubles possible values, keeping searches logarithmic in size. In a decision tree, the branching factor m controls how many choices can be tested at once — larger m means broader reasoning, but more computation. In network design, limiting m controls congestion and redundancy, ensuring stability.
  > Source: Anatomy of a Tree.html

## Common Misconceptions

- **"Height is counted starting at level 1."** No — we start at level 0. For the tree with levels A / B,C,D / E,F,G the height is 2, not 3.
  > Source: Anatomy of a Tree.html/practice/config-1762991533061.practice.json
- **"Any tree where nodes have up to three children is a *full* 3-ary tree."** Close, but not correct — a full m-ary tree requires that *every* internal node has exactly m children. If one internal node has only two children while m = 3, it is a 3-ary tree but not a full 3-ary tree.
  > Source: Anatomy of a Tree.html/practice/config-1762991748168.practice.json
- **"A node with three children could still be part of a binary tree."** Incorrect — binary means at most two children per node (m = 2), so a node with three children exceeds that limit.
  > Source: Anatomy of a Tree.html/practice/config-1762991748168.practice.json

## Related Topics

- [Introducing Trees and Forests](trees-and-forests.md)
- [Traversing Trees](traversing-trees.md)
- [Applications of Trees](applications-of-trees.md)
