# Traversing Trees

> **Main concept:** Trees & Forests

## Definition

Ordered rooted trees store data in a structured hierarchy. To make use of that data, you need a clear visiting pattern, called a **traversal**. Traversal algorithms visit every vertex exactly once in a specific order. These patterns support tasks like copying structures, evaluating expressions, deleting subtrees or listing elements in sorted order.
> Source: Traversing Trees.html

The three fundamental traversal types are:
- **Preorder:** Visit the root first, then its subtrees (left to right)
- **Inorder:** Visit the left subtree, then the root, then the right subtree (binary trees only)
- **Postorder:** Visit all subtrees first, then the root
> Source: Traversing Trees.html

## Key Concepts

### Universal Address System

Traversal only makes sense if there's a consistent order among siblings. The **universal address system** gives every vertex a unique label that defines its exact position in the tree.

Labelling rule:
- Label the root **0**.
- Label its children **1, 2, …, k** from left to right.
- For any vertex labelled A, label its children **A.1, A.2, …, A.k_A**.

A vertex label like `2.1.3` means: from the root, go to the 2nd child, then the 1st, then the 3rd.
> Source: Traversing Trees.html

These labels follow **lexicographic order**, which gives a consistent left-to-right order across the entire tree. This matches the **preorder traversal** order exactly.
> Source: Traversing Trees.html

### Traversal Algorithms

Traversal defines how you move through a hierarchy. Each pattern reflects a different intent: building, inspecting or cleaning up.
> Source: Traversing Trees.html

- **Preorder:** Visit the root, then traverse each subtree from left to right. Use cases: copying or serializing trees; generating prefix (Polish) expressions.
  > Source: Traversing Trees.html
- **Inorder:** Used **only for binary trees**. Visit the left subtree, then the root, then the right subtree. Use cases: binary search trees (produces sorted order); expression trees (infix notation; parentheses required).
  > Source: Traversing Trees.html
- **Postorder:** Visit all subtrees first, then the root. Use cases: deleting a tree safely (bottom-up); evaluating postfix expressions; computing subtree properties before parent use.
  > Source: Traversing Trees.html

### The Single-Curve Model

All three traversals can be visualized using a single motion. Imagine drawing a curve that hugs the outer edge of the tree, starting and ending at the root:
- **Preorder:** Record a vertex the first time the curve touches it.
- **Inorder (binary):** Record a leaf on the first touch, an internal vertex on the second.
- **Postorder:** Record a vertex the last time the curve passes it.

This visual model ties the three orders together and helps you see how they differ by timing.
> Source: Traversing Trees.html

### Expression Trees and Notation

Ordered rooted trees give a clear structural view of nested or compound expressions. In an expression tree:
- **Internal vertices** represent operators (like +, −, ∗, /, ↑).
- **Leaves** represent operands (variables, constants, or literals).
- Each internal node applies its operator to its left and right subtrees, in that order.

This structure captures the order of operations without relying on parentheses. This visual hierarchy mirrors how computers evaluate expressions: the tree defines what depends on what.
> Source: Traversing Trees.html

| Traversal | Notation | Operator Position | Parentheses Needed |
|---|---|---|---|
| Preorder | Prefix | Before operands | No |
| Inorder | Infix | Between operands | Yes |
| Postorder | Postfix | After operands | No |
> Source: Traversing Trees.html

- **Prefix** form is unambiguous and easy for machines to parse.
- **Infix** form is human-readable but needs parentheses to clarify order.
- **Postfix** form is efficient for stack-based evaluators, as used in many compilers and calculators.
> Source: Traversing Trees.html

## Examples

- **The three orders on one small tree** (root B with children A and C):
  - Preorder: **B A C**
  - Inorder: **A B C**
  - Postorder: **A C B**
  > Source: Traversing Trees.html
- **Expression tree for ((x + y) * (x − y)):** `*` is the root, showing that multiplication happens last. The left and right subtrees represent the additions and subtractions that happen first.
  > Source: Traversing Trees.html
- **Worked traversal of ((x + y)^2) + ((x − 4)/3):**
  - Preorder (prefix): `+ ^ + x y 2 / - x 4 3`
  - Inorder (infix, fully parenthesized): `((x + y) ^ 2) + ((x − 4) / 3)`
  - Postorder (postfix): `x y + 2 ^ x 4 − 3 / +`

  Each traversal lists the same structure in a different logical order.
  > Source: Traversing Trees.html
- **Traversal practice tree** — root M, with left child H (children D and J) and right child T (child R):
  - Inorder: **D H J M R T** — the left subtree gives D H J, then root M, then the right subtree R T.
  - Postorder: **D J H R T M** — postorder lists children before their parent: left subtree D J H, right subtree R T, then root M.
  > Source: Traversing Trees.html/practice/config-1763054448442.practice.json; Traversing Trees.html/practice/config-1763054546018.practice.json

## Real Uses of Tree Traversal

- **Compilers and interpreters** use traversal to read and evaluate code. Every programming language parser walks expression trees to generate or execute instructions.
  > Source: Traversing Trees.html
- **Access control models** often use hierarchical structures (roles, permissions or trust relationships). Traversal identifies which users or processes inherit specific rights.
  > Source: Traversing Trees.html
- **Data serialization** (saving and loading structured data) uses preorder or postorder patterns to preserve hierarchy.
  > Source: Traversing Trees.html
- **File systems** use tree traversal to search, list and delete directories. Preorder can copy a file structure, while postorder safely removes one.
  > Source: Traversing Trees.html
- **Malware analysis tools** walk abstract syntax trees to trace how code behaves or hides instructions.
  > Source: Traversing Trees.html
- **AI decision trees and syntax parsing** depend on systematic tree visits.
  > Source: Traversing Trees.html

## Common Misconceptions

- **"Inorder traversal can start with the root."** No — in inorder the root appears too early if listed first. Inorder traversal visits the left subtree first, then the root, then the right subtree. A traversal that starts with the root is closer to preorder.
  > Source: Traversing Trees.html/practice/config-1763054448442.practice.json
- **"Postorder lists the parent before its children."** Incorrect — that is closer to preorder. Postorder lists children before their parent.
  > Source: Traversing Trees.html/practice/config-1763054546018.practice.json
- **"Inorder traversal works for any tree."** Inorder is used only for binary trees.
  > Source: Traversing Trees.html

## Related Topics

- [Anatomy of a Tree](anatomy-of-a-tree.md)
- [Applications of Trees](applications-of-trees.md)
- [Introducing Trees and Forests](trees-and-forests.md)
