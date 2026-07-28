# Applications of Trees

> **Main concept:** Trees & Forests

## Definition

Trees appear wherever information needs to be organized, searched or processed efficiently. Because they grow without cycles, they form predictable paths that let computers make decisions, store data and compress information quickly.
> Source: Applications of Trees.html

## Key Concepts

### Binary Search Trees (BSTs)

**Definition: Binary Search Tree** — A binary search tree is a binary tree where each node follows a specific ordering rule:
- Every vertex (or node) has at most one left child and one right child.
- Each vertex is assigned a **key**: one of the items being stored.
- **The key of a vertex is larger than all keys in its left subtree and smaller than all keys in its right subtree.**

This rule allows us to search for, insert or delete items efficiently, since at every step we know whether to move left (smaller) or right (larger).
> Source: Applications of Trees.html

**Building a BST** — build recursively from a list of items using a simple comparison process:
1. Start with an empty tree.
2. Make the first item in the list the root.
3. For each new item: compare it to the key at the current node; if it's smaller, move left; if larger, move right. If no appropriate child exists, create a new vertex there and insert the item.
> Source: Applications of Trees.html

**Searching in a BST:**
1. Start at the root.
2. Compare the target value to the current node's key.
3. Move left if smaller, right if larger.
4. Stop if you find the key — or reach a leaf (not found).
> Source: Applications of Trees.html

**Key insight:** Each comparison removes half of the remaining possibilities. Searching in a well-balanced BST takes time proportional to the height of the tree, about **O(log n)** in the best case.
> Source: Applications of Trees.html

**Inserting and removing:** Insertion follows the same comparison logic — move left or right until you find an empty spot. Deletion is slightly trickier: if a node has two children, we replace it with the smallest value from its right subtree to preserve order.
> Source: Applications of Trees.html

**Why ordering matters:** Ordering matters because the tree's structure itself encodes the sorting. Order makes searching and insertion much faster than scanning a linear list.
> Source: Applications of Trees.html

### Decision Trees

**Definition: Decision Tree** — A decision tree is a rooted tree in which each internal vertex represents a decision or test, and each edge corresponds to one possible outcome of that decision. The leaves represent final solutions or results.
> Source: Applications of Trees.html

Each path from the root to a leaf describes one complete sequence of choices leading to a result. A decision tree structures reasoning: every condition reduces uncertainty until a final decision is reached.
> Source: Applications of Trees.html

A binary search tree can also be seen as a type of decision tree — at each node, we decide whether to go left or right based on comparison results (for instance, "Is the key less than or greater than 50?"). More generally, decision trees represent any problem solved through a chain of conditional checks.
> Source: Applications of Trees.html

**In AI and algorithms:** decision trees model classification and prediction. Each internal node tests a condition on a dataset (e.g. "Is age > 30?"); each path leads to a prediction (e.g. "Approved" or "Denied"); algorithms like ID3, CART and Random Forests rely on this structure to analyze data efficiently. In game theory, similar trees (called **game trees**) represent possible moves and countermoves in strategy games such as chess or checkers. Algorithms traverse these trees using backtracking or minimax techniques to evaluate outcomes and find the best play. Decision trees are powerful because they mimic human reasoning — each step eliminates possibilities until only one outcome remains.
> Source: Applications of Trees.html

### Other Uses of Trees in Computing

- **Huffman coding trees:** Huffman coding uses binary trees to compress data by assigning shorter codes to frequent symbols and longer codes to rare ones. This minimizes the total number of bits used to store or transmit data and forms the basis of many compression standards (ZIP, JPEG, MP3). Example: the letter "E" might be encoded as 0, while "Q" might be 11110, ensuring no code is a prefix of another.
  > Source: Applications of Trees.html
- **Syntax trees:** In programming languages, syntax trees represent the grammatical structure of source code. Each node corresponds to a component (an expression, operator, or statement) showing how the code must be parsed and executed. The tree with `=` at the root, `x` on the left and `+` (over `y` and `3`) on the right represents the statement `x = y + 3`.
  > Source: Applications of Trees.html
- **File-system trees:** Your computer's folder structure is literally a tree. The root directory (like `/` or `C:\`) is the root node, folders are internal vertices, and files are leaves. Each file path (`/Documents/Projects/Report.docx`) is a unique path from the root to a leaf.
  > Source: Applications of Trees.html
- **Game trees:** In competitive games, game trees represent every possible move sequence. Each branch corresponds to a possible move, and each leaf represents an end state (win, loss, draw). Algorithms use pruning (e.g. alpha–beta pruning) to skip irrelevant paths and focus on the most promising strategies.
  > Source: Applications of Trees.html

### Structural Advantages of Trees

All these applications rely on the same structural advantages:
- **Minimal redundancy:** only one path connects any two vertices.
- **Hierarchical order:** decisions and searches follow clear top-down logic.
- **Balanced performance:** well-structured trees reduce operations from linear to logarithmic time.
- **Predictability:** the number of steps needed to find or process information depends on the tree's height.

In short, trees convert complex systems into organized hierarchies that are easy to navigate, process and reason about.
> Source: Applications of Trees.html

## Examples

- **Building a BST:** Inserting the numbers 50, 30, 70, 20, 40, 60, 80 builds the tree with 50 at the root, 30 and 70 as its children, and 20, 40, 60, 80 as leaves. At each step, comparisons guide where to place the new node.
  > Source: Applications of Trees.html
- **Searching a BST:** To find 40, start at 50 → move left (40 < 50) → find 40 at the next step. To find 75, start at 50 → right to 70 → right to 80 → not found.
  > Source: Applications of Trees.html
- **Real-world BST applications:** databases and indexing systems (fast lookups); compilers (symbol tables); file systems and dictionaries; auto-complete and spell-check engines. Each relies on the same property: once data is organized in a BST, finding any element becomes as simple as walking a path.
  > Source: Applications of Trees.html
- **Decision tree — "Should I bring an umbrella?":** The root asks "Is it raining?" If yes, bring an umbrella; if no, check the forecast, which branches to rain (bring umbrella) or clear (no umbrella). Each internal vertex poses a question; each edge represents a possible answer; each leaf shows the outcome.
  > Source: Applications of Trees.html
- **What cannot be modelled as a tree:** A road network with circular routes cannot be modelled as a tree, because trees cannot contain cycles. By contrast, a hierarchical file system, a business organizational chart and a decision model are all standard tree use cases.
  > Source: Applications of Trees.html/practice/config-1763051205526.practice.json

## Common Misconceptions

- **"BSTs are fast because they store data randomly / use extra memory for indexing / connect all nodes in a loop."** None of these are correct. A BST is fast because it maintains order, so each comparison halves the search space — the ordered structure lets you skip large sections of data. Randomness would slow searching down, indexing isn't what makes BSTs efficient, and trees never contain cycles.
  > Source: Applications of Trees.html/practice/config-1763051024294.practice.json
- **"A leaf in a decision tree represents a question or test."** No — that's an internal node. A leaf represents a final decision or outcome; the starting condition is the root; and relationships between outcomes are represented by edges, not leaves.
  > Source: Applications of Trees.html/practice/config-1763051106045.practice.json

## Related Topics

- [Introducing Trees and Forests](trees-and-forests.md)
- [Anatomy of a Tree](anatomy-of-a-tree.md)
- [Traversing Trees](traversing-trees.md)
