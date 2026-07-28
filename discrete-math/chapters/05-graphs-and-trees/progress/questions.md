# Question Bank

> Generated from `wiki/` during the compile step. Extended on wrong-answer targeting and graduation.
> Do not edit manually — all changes are made by Claude during compile and session flows.

---

<!-- Question format (do not delete this comment):

## Q{NNN}
**Status:** active | retired
**Type:** mcq | short-answer | conceptual | true-false
**Difficulty:** introductory | intermediate | advanced
**Topic:** {topic-slug}
**Focus Area:** {specific concept or sub-topic}
**Question:** {question text}
**Answer:** {model answer — sourced from wiki only}

-->

## Q001
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** understanding-graphs
**Focus Area:** Formal definition of a graph
**Question:** Write the formal definition of a graph, including what G, V and E stand for.
**Answer:** A graph is written G = (V, E), where V is a non-empty set of vertices (or nodes) and E is a set of edges (or links) connecting pairs of vertices. Each edge has one or two vertices associated with it, called its endpoints.

## Q002
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** understanding-graphs
**Focus Area:** Vertices and edges in a modelled network
**Question:** In a graph representing an airline network, what do the vertices represent? (a) Airports (b) Flights (c) Passengers (d) Air traffic controllers
**Answer:** (a) Airports. Each vertex represents an airport — a location that can connect to others through flight routes, which are the edges. Flights would be better represented by edges; passengers travel between vertices but aren't part of the graph structure itself.

## Q003
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** understanding-graphs
**Focus Area:** Structure vs. visual layout
**Question:** True or false: rearranging how a graph is drawn can change the relationships between vertices.
**Answer:** False. The layout might look different, but the connections between vertices remain the same. The structure of a graph is defined by its connections, not by how it looks on the page.

## Q004
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** understanding-graphs
**Focus Area:** Finite vs. infinite graphs
**Question:** Which of the following best describes a finite graph? (a) A graph with a limited number of vertices and edges (b) A graph with an unlimited number of vertices (c) A graph that contains loops (d) A graph that contains no connections
**Answer:** (a) A graph with a limited number of vertices and edges — a finite graph has a specific, countable number of vertices and edges. (b) describes an infinite graph; loops describe edge type, not graph size; and a graph with no connections would be a set of isolated vertices, not necessarily finite or infinite.

## Q005
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** understanding-graphs
**Focus Area:** Endpoints
**Question:** What are the endpoints of an edge?
**Answer:** The endpoints are the vertices connected by an edge — for example, the cities connected by a road.

## Q006
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** understanding-graphs
**Focus Area:** Graphs in computer science
**Question:** Give three distinct computing applications of graphs and explain what the graph models in each.
**Answer:** Any three of: routing and navigation (GPS and delivery systems use graphs to find the shortest or least expensive path between locations); dependency management (compilers and project planners track which modules depend on which others); web search and recommendation engines (graphs represent links between pages, people or products); cybersecurity (attack graphs model possible pathways an attacker could exploit).

## Q007
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** understanding-graphs
**Focus Area:** Modelling networks as graphs
**Question:** Explain what the vertices and edges represent in a social network, a metro network and a computer network.
**Answer:** In a social network, each vertex is a person and each edge is a friendship. In a metro network, vertices are stations and edges are the rails between them. In a computer network, vertices are devices and edges represent communication channels.

## Q008
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** graph-types-connectivity-and-components
**Focus Area:** Directed edge notation
**Question:** Which of the following represents a single directed edge? (a) A → B (b) A — B (c) A = B (d) A ↔ B
**Answer:** (a) A → B. The arrow shows direction from A to B. Without an arrow, A — B is undirected and could go both ways; A = B shows a parallel but undirected connection; A ↔ B indicates two directed edges in opposite directions, not one.

## Q009
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** graph-types-connectivity-and-components
**Focus Area:** Multigraph vs. pseudograph
**Question:** What is the difference between a multigraph and a pseudograph?
**Answer:** A multigraph allows multiple edges (parallel edges) between the same vertices but no self-loops. A pseudograph may include loops, and possibly multiple edges connecting the same pair of vertices or a vertex to itself.

## Q010
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** graph-types-connectivity-and-components
**Focus Area:** Walks, paths and cycles
**Question:** Define a walk, a path and a cycle, and state how each differs from the others.
**Answer:** A walk is any sequence of edges that connects vertices, allowing repetition of both vertices and edges (e.g. A → B → C → B → D). A path is a special kind of walk where no vertex is repeated (e.g. A → B → C → D). A cycle is a path that starts and ends at the same vertex, with all other vertices distinct (e.g. A → B → C → A).

## Q011
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** graph-types-connectivity-and-components
**Focus Area:** Recognizing a disconnected graph
**Question:** Which of the following graphs is disconnected? (a) A —— B    C —— D (b) A —— B —— C —— D (c) A —— B —— C ——— A (d) A → B → C → D
**Answer:** (a) A —— B    C —— D. There's no path connecting the two sets of vertices. In (b) you can travel from any vertex to any other; (c) is a connected cycle; and in (d), despite direction, every vertex is reachable in the chain.

## Q012
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** graph-types-connectivity-and-components
**Focus Area:** Connectivity
**Question:** When is an undirected graph called connected?
**Answer:** An undirected graph is connected if every vertex is reachable from every other vertex — you can start anywhere and eventually reach any other vertex by following edges.

## Q013
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** graph-types-connectivity-and-components
**Focus Area:** Components
**Question:** What is a component of a graph? Give an example.
**Answer:** Each isolated "part" of a disconnected graph is called a component. For example, two disconnected Wi-Fi networks form two components: devices in one can't communicate with the other.

## Q014
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** graph-types-connectivity-and-components
**Focus Area:** Mixed graphs
**Question:** What is a mixed graph, and when would you use one to model a real system?
**Answer:** A mixed graph combines both directed and undirected edges in the same diagram. It's useful when some relationships are mutual and others are one-way — for example, in a communication network where some links allow two-way data transfer while others only send in one direction.

## Q015
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** degrees-adjacency-and-graph-properties
**Focus Area:** Adjacency and incidence
**Question:** What does it mean for two vertices to be adjacent, and what does it mean for an edge to be incident with a vertex?
**Answer:** Two vertices u and v are adjacent if an edge connects them. That edge is said to be incident with both vertices. For example, in A —— B —— C, A and B are adjacent (they share an edge), but A and C are not adjacent because there's no direct connection.

## Q016
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** degrees-adjacency-and-graph-properties
**Focus Area:** Neighbourhood N(v)
**Question:** If vertex A connects to B and C, what is N(A), and what does the neighbourhood of a vertex capture?
**Answer:** N(A) = {B, C}. The neighbourhood of a vertex is the set of vertices directly connected to it, capturing the local structure of the network — what's directly reachable in one step.

## Q017
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** degrees-adjacency-and-graph-properties
**Focus Area:** Handshake Lemma
**Question:** A graph has 8 vertices and 10 edges. What is the sum of all vertex degrees? (a) 20 (b) 8 (c) 16 (d) 10
**Answer:** (a) 20. By the Handshake Lemma, Σ deg(v) = 2m = 2 × 10 = 20. 8 is the number of vertices and 10 is the number of edges, neither of which is the degree sum.

## Q018
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** degrees-adjacency-and-graph-properties
**Focus Area:** Handshake Lemma — statement and reasoning
**Question:** State the Handshake Lemma and explain why it holds.
**Answer:** For any undirected graph G = (V, E) with m edges, 2m = Σ(v ∈ V) deg(v). It holds because every edge connects two vertices, and each connection contributes 1 to the degree of both endpoints, so every edge is counted twice in the degree sum.

## Q019
**Status:** active
**Type:** mcq
**Difficulty:** advanced
**Topic:** degrees-adjacency-and-graph-properties
**Focus Area:** Parity of odd-degree vertices
**Question:** In an undirected graph, three vertices have odd degree. What must be true? (a) The number of odd-degree vertices must be even (b) The total degree sum is odd (c) The graph has exactly one connected component (d) The graph cannot have loops
**Answer:** (a) The number of odd-degree vertices must be even — odd-degree vertices occur in pairs, so the stated situation is impossible. Vertex parity is unrelated to the number of connected components, and loops affect the degree count but not the parity rule.

## Q020
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** degrees-adjacency-and-graph-properties
**Focus Area:** Loops and degree
**Question:** True or false: in an undirected graph, a loop at a vertex adds 1 to that vertex's degree.
**Answer:** False. A loop at a vertex counts twice — once as start and once as end.

## Q021
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** degrees-adjacency-and-graph-properties
**Focus Area:** Isolated and pendant vertices
**Question:** Define an isolated vertex and a pendant vertex, and give a real-world example of each.
**Answer:** An isolated vertex has degree 0 — it has no incident edges (e.g. a disconnected IoT sensor that lost its Wi-Fi link). A pendant vertex has degree 1 — it connects to only one other vertex (e.g. a printer connected to one router in a home network).

## Q022
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** degrees-adjacency-and-graph-properties
**Focus Area:** Königsberg Bridge Problem and Eulerian paths
**Question:** Why did Euler conclude that the Königsberg bridge walk was impossible? State the rule he relied on.
**Answer:** Euler redrew the city as a graph where each landmass became a vertex and each bridge became an edge. Every land area had an odd number of bridges (North Bank 3, South Bank 3, East Island 3, Middle Island 5), giving four vertices of odd degree. The rule is that a graph can have an Eulerian path — a walk that crosses every edge exactly once — only if it has exactly 0 or 2 vertices of odd degree. Since Königsberg's graph had four odd-degree vertices, the walk was impossible.

## Q023
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** degrees-adjacency-and-graph-properties
**Focus Area:** Complete graphs
**Question:** In a complete graph Kₙ, what is the degree of each vertex and how many edges does the graph have?
**Answer:** Each vertex has degree n − 1, and the total number of edges is n(n − 1)/2. A complete graph connects every vertex to every other vertex exactly once, representing maximum connectivity.

## Q024
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** degrees-adjacency-and-graph-properties
**Focus Area:** Bipartite graphs
**Question:** What makes a graph bipartite, and what is a bipartition?
**Answer:** A bipartite graph divides vertices into two distinct sets V₁ and V₂, where edges only connect vertices across the sets and never within them. When this condition holds, the pair (V₁, V₂) is called a bipartition of the vertex set V of G. Example: students enrolling in courses, with no edges directly connecting students to students or courses to courses.

## Q025
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** degrees-adjacency-and-graph-properties
**Focus Area:** Wheel graphs
**Question:** A wheel graph Wₙ has n vertices. How many edges does it have, and what is its defining structure? (a) 2(n − 1) edges; a central hub plus a surrounding cycle (b) n(n − 1)/2 edges; every vertex joined to every other (c) n − 1 edges; a connected acyclic structure (d) n edges; a single closed loop
**Answer:** (a) 2(n − 1) edges; a wheel graph combines a central hub with a surrounding cycle, where the hub vertex connects to every point on the rim. Airline route maps often form wheel graphs, with one major hub serving multiple regional spokes.

## Q026
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** degrees-adjacency-and-graph-properties
**Focus Area:** Weighted graphs
**Question:** What is a weighted graph, and why are weights useful?
**Answer:** A weighted graph assigns values to edges, often representing distance, time or cost. Weights allow us to compute optimal paths such as the fastest route, cheapest connection or least congested link — GPS navigation, shipping logistics and network routing all depend on them.

## Q027
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** degrees-adjacency-and-graph-properties
**Focus Area:** In-degree and out-degree
**Question:** In the directed graph A → B, B → C, B → D, give indeg and outdeg for every vertex.
**Answer:** indeg(A) = 0, outdeg(A) = 1 (to B); indeg(B) = 1 (from A), outdeg(B) = 2 (to C and D); indeg(C) = 1, outdeg(C) = 0; indeg(D) = 1, outdeg(D) = 0. B acts like a small hub, C and D are receivers, and A connects only once.

## Q028
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** representing-graphs-and-isomorphism
**Focus Area:** Identifying representations
**Question:** Which representation uses a square grid of 0s and 1s to record whether vertices are connected? (a) Adjacency matrix (b) Adjacency list (c) Incidence matrix (d) Weighted list
**Answer:** (a) Adjacency matrix. Each cell shows whether a pair of vertices is connected. An adjacency list uses lists of neighbours, an incidence matrix focuses on vertex–edge relationships, and "weighted list" is not a standard representation type.

## Q029
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** representing-graphs-and-isomorphism
**Focus Area:** Adjacency list trade-offs
**Question:** Give two advantages and two drawbacks of using an adjacency list.
**Answer:** Advantages: space-efficient for sparse graphs (few edges); easy to iterate through the neighbours of a vertex; simple to store and update dynamically. Drawbacks: checking if two vertices are connected requires searching through a list; less efficient for dense graphs with many edges.

## Q030
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** representing-graphs-and-isomorphism
**Focus Area:** Adjacency matrix trade-offs
**Question:** What is the memory cost of an adjacency matrix, and when is that cost a problem?
**Answer:** An adjacency matrix uses O(n²) memory, even if few edges exist. That makes it inefficient for sparse graphs, where many cells are empty. Its advantage is that checking adjacency is a single fast lookup, and it naturally extends to weighted graphs by replacing 1s with edge weights.

## Q031
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** representing-graphs-and-isomorphism
**Focus Area:** Incidence matrix
**Question:** What does an incidence matrix record, and what problems is it well suited to?
**Answer:** An incidence matrix focuses on edges instead of pairs of vertices — it records which vertices each edge touches, with rows corresponding to vertices and columns to edges. It captures explicit vertex–edge relationships and is useful for network flow and optimization problems, and for algorithms analyzing edge properties. Its drawbacks are larger matrices for dense graphs and being more complex to interpret visually.

## Q032
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** representing-graphs-and-isomorphism
**Focus Area:** In-degree meaning
**Question:** In a directed graph, what does an in-degree of 3 for a vertex mean? (a) It receives edges from three other vertices (b) It has three outgoing connections (c) It connects to itself three times with self-loops (d) It has three total connections
**Answer:** (a) It receives edges from three other vertices. (b) describes an out-degree of 3; a self-loop contributes 1 to both in-degree and out-degree for the same vertex; and (d) is too vague — total degree in a directed graph would be the sum of in-degree and out-degree.

## Q033
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** representing-graphs-and-isomorphism
**Focus Area:** Balance of in- and out-degrees
**Question:** If a digraph has 8 edges, what must the total sum of in-degrees be? (a) 8 (b) 16 (c) 4 (d) 2
**Answer:** (a) 8. By the Balance of In- and Out-Degrees Theorem, Σ deg⁻(v) = Σ deg⁺(v) = |E|, so the total in-degree equals the total number of edges.

## Q034
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** representing-graphs-and-isomorphism
**Focus Area:** Balance theorem — reasoning
**Question:** State the Balance of In- and Out-Degrees Theorem and explain why it must be true.
**Answer:** For a directed graph G = (V, E), Σ(v ∈ V) deg⁻(v) = Σ(v ∈ V) deg⁺(v) = |E|. Each directed edge adds one count to someone's out-degree (the sender) and one to someone's in-degree (the receiver). Since every edge connects exactly two vertices in this way, the total in-degree and total out-degree must always be equal, and both equal the total number of edges.

## Q035
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** representing-graphs-and-isomorphism
**Focus Area:** Definition of isomorphism
**Question:** When are two graphs G = (V, E) and H = (W, F) isomorphic?
**Answer:** They are isomorphic if there exists a one-to-one correspondence between their vertices such that edges are preserved — meaning if two vertices are connected in G, their corresponding vertices are connected in H.

## Q036
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** representing-graphs-and-isomorphism
**Focus Area:** Testing for isomorphism
**Question:** Two graphs each have 5 vertices and 6 edges. The first has degree sequence 2, 2, 3, 2, 3 and the second has 4, 2, 3, 2, 1. Are they isomorphic? Justify your answer using the standard checks.
**Answer:** No, they are not isomorphic. The three checks are: count vertices and edges (they must match — here they do); compare degrees (each vertex must correspond to another with the same degree — here the degree sequences differ); compare adjacency patterns (neighbour sets must match under the mapping). Since the degree sequences differ, there's no one-to-one correspondence preserving adjacency — no vertex in the first graph has 4 neighbours as one does in the second — so the adjacency patterns cannot match.

## Q037
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** representing-graphs-and-isomorphism
**Focus Area:** Isomorphism — necessary vs. sufficient conditions
**Question:** True or false: if two graphs have the same number of vertices and the same number of edges, they must be isomorphic.
**Answer:** False. Matching vertex and edge counts is not sufficient — the degree sequences must also match and the adjacency patterns must correspond under the mapping. The worked example has two graphs with 5 vertices and 6 edges each that are not isomorphic because their degree sequences differ.

## Q038
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** trees-and-forests
**Focus Area:** Definition of a tree
**Question:** Which condition must a graph meet to be a tree? (a) It must be connected and contain no cycles (b) It can have cycles as long as it's connected (c) It must be directed (d) It must have equal numbers of vertices and edges
**Answer:** (a) It must be connected and contain no cycles — both are required. Cycles violate the definition of a tree; direction isn't part of the definition; and a tree always has one fewer edge than vertices.

## Q039
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** trees-and-forests
**Focus Area:** Forests
**Question:** If a graph is disconnected but contains no cycles, what type of graph is it? (a) Forest (b) Tree (c) Weighted graph (d) Complete graph
**Answer:** (a) Forest — a forest is a collection of disconnected trees. A tree must be connected; weighting doesn't affect structure; and a complete graph would connect every vertex to every other.

## Q040
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** trees-and-forests
**Focus Area:** Unique Path Theorem
**Question:** According to the Unique Path Theorem, how many simple paths exist between any two vertices in a tree? (a) Exactly one (b) At least two (c) None (d) Unlimited
**Answer:** (a) Exactly one. Having one unique path between any two vertices is what makes a graph a tree; two or more paths would create a cycle, and vertices with no path between them wouldn't be connected.

## Q041
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** trees-and-forests
**Focus Area:** Trees as simple graphs
**Question:** Why can a tree never contain multiple edges or loops?
**Answer:** Because a tree cannot contain a circuit. That rules out multiple edges and loops, which means every tree is a simple graph: one connection between any two vertices, and no edge that starts and ends at the same vertex.

## Q042
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** trees-and-forests
**Focus Area:** Identifying trees
**Question:** Four graphs are given: G₁ and G₂ are connected with no circuits; G₃ contains the circuit e–b–a–d–e; G₄ is disconnected. Which are trees, and why are the others not?
**Answer:** G₁ and G₂ are trees since both are connected and contain no circuits. G₃ is not a tree because it contains a simple circuit (e–b–a–d–e). G₄ is not a tree because it's disconnected.

## Q043
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** trees-and-forests
**Focus Area:** Forests in real systems
**Question:** Describe a situation that would naturally be modelled as a forest rather than a single tree.
**Answer:** Forests appear when systems split into independent hierarchies — multiple databases, isolated networks or separate family branches. A forest is like having several separate hierarchies, such as multiple independent file systems or family branches that never connect. Each connected component of a forest is itself a tree.

## Q044
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** trees-and-forests
**Focus Area:** History of trees
**Question:** Who first used trees to count chemical compounds, and in what year?
**Answer:** The English mathematician Arthur Cayley, as early as 1857 — one of the earliest applications of graph theory to real-world problems.

## Q045
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** anatomy-of-a-tree
**Focus Area:** Rooted trees
**Question:** What is a rooted tree, and what is special about the root?
**Answer:** A rooted tree is a tree where one vertex is identified as the root, and every edge is directed outward from it. The root has no parent; all other vertices have exactly one parent. Selecting a different vertex as the root produces a different rooted tree.

## Q046
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** anatomy-of-a-tree
**Focus Area:** Leaf vs. internal vertex
**Question:** What distinguishes a leaf from an internal vertex?
**Answer:** A leaf is a node with no children (e.g. the lowest-level file in a file system). An internal vertex is a node that has at least one child (e.g. a directory that contains other directories).

## Q047
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** anatomy-of-a-tree
**Focus Area:** Reading tree relationships
**Question:** In the tree with root A whose children are B, C and D, where B's children are E and F and D's child is G, which statement is true? (a) F is a sibling of E (b) C is the parent of D (c) G is a descendant of C (d) A is a leaf vertex
**Answer:** (a) F is a sibling of E — they share the same parent, B. C and D share the same parent (A), so they are siblings, not parent and child; G is part of the branch under D, not C; and A has children (B, C, D), so it's the root, not a leaf.

## Q048
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** anatomy-of-a-tree
**Focus Area:** Levels and height
**Question:** A tree has A at the top, then B, C, D, then E, F, G. What is its height? (a) 2 (b) 1 (c) 3 (d) 4
**Answer:** (a) 2. Level 0 is A; level 1 is B, C, D; level 2 is E, F, G. The height is the maximum level among all vertices, and levels start at 0, not 1.

## Q049
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** anatomy-of-a-tree
**Focus Area:** Level and height definitions
**Question:** Define the level of a vertex and the height of a tree.
**Answer:** The level of a vertex is how far it is from the root — the number of edges along the path from the root to that vertex, with the root always at level 0. The height of a tree is the maximum level among all its vertices.

## Q050
**Status:** active
**Type:** mcq
**Difficulty:** advanced
**Topic:** anatomy-of-a-tree
**Focus Area:** m-ary vs. full m-ary trees
**Question:** A rooted tree has internal vertices M and N; M has three children and N has two. What type of tree is it? (a) 3-ary tree (b) Full binary tree (c) Full 3-ary tree (d) 2-ary tree
**Answer:** (a) 3-ary tree — each internal node has at most three children. It is not a full 3-ary tree, because a full m-ary tree requires every internal vertex to have exactly m children, and N only has two. Binary (2-ary) means at most two children per node, which M exceeds.

## Q051
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** anatomy-of-a-tree
**Focus Area:** m-ary tree definitions
**Question:** Define an m-ary tree, a full m-ary tree and a binary tree.
**Answer:** A rooted tree is an m-ary tree if every internal vertex has no more than m children. It is a full m-ary tree if every internal vertex has exactly m children. An m-ary tree with m = 2 is called a binary tree.

## Q052
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** anatomy-of-a-tree
**Focus Area:** Edge count theorem
**Question:** How many edges does a tree with n vertices have?
**Answer:** n − 1 edges.

## Q053
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** anatomy-of-a-tree
**Focus Area:** n = mi + 1
**Question:** A full 3-ary tree has 4 internal vertices. How many vertices does it have in total? Show the formula you used.
**Answer:** A full m-ary tree with i internal vertices contains n = mi + 1 vertices. Here n = 3(4) + 1 = 13 vertices. Every internal node contributes m new nodes, plus one root that anchors the structure.

## Q054
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** anatomy-of-a-tree
**Focus Area:** Internal vertices, leaves and edges
**Question:** For a full 3-ary tree with 5 internal vertices, find the total vertices, the number of leaves and the number of edges.
**Answer:** n = mi + 1 = 3(5) + 1 = 16 total vertices; l = (m − 1)i + 1 = (2)(5) + 1 = 11 leaves; edges = n − 1 = 15.

## Q055
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** anatomy-of-a-tree
**Focus Area:** Full m-ary tree formulas
**Question:** State the formulas for a full m-ary tree with l leaves: how many vertices and how many internal vertices does it have?
**Answer:** A full m-ary tree with l leaves has n = (ml − 1)/(m − 1) vertices and i = (l − 1)/(m − 1) internal vertices.

## Q056
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** anatomy-of-a-tree
**Focus Area:** Balanced trees
**Question:** When is a rooted m-ary tree of height h balanced, and why does balance matter?
**Answer:** It is balanced if all leaves are at levels h or h − 1 — every leaf is either on the last level or one level above it, so no branch extends dramatically further than the rest. Balance matters because a balanced tree ensures data access, search and traversal take roughly the same number of steps no matter where information sits; when trees become skewed, performance can degrade.

## Q057
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** anatomy-of-a-tree
**Focus Area:** Ordered rooted trees
**Question:** What is an ordered rooted tree, and why can two trees with identical vertices and edges still differ?
**Answer:** An ordered rooted tree is one where the children of each node are arranged in a specific sequence, usually left to right. Two trees can contain the same vertices and edges but differ if the order of children changes — the connections are the same, but the meanings can differ completely, much like "cats chase dogs" versus "dogs chase cats." Ordered trees matter when sequence affects meaning, outcome or evaluation.

## Q058
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** anatomy-of-a-tree
**Focus Area:** Kinds of binary tree
**Question:** Name and describe the three kinds of binary tree.
**Answer:** Full (every internal node has two children), complete (every level except the last is full), and arbitrary (some nodes have one or no children).

## Q059
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** traversing-trees
**Focus Area:** The three traversals
**Question:** Describe the visiting order for preorder, inorder and postorder traversal.
**Answer:** Preorder: visit the root first, then its subtrees left to right. Inorder: visit the left subtree, then the root, then the right subtree (binary trees only). Postorder: visit all subtrees first, then the root.

## Q060
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** traversing-trees
**Focus Area:** Traversal on a small tree
**Question:** For the tree with root B, left child A and right child C, give the preorder, inorder and postorder traversals.
**Answer:** Preorder: B A C. Inorder: A B C. Postorder: A C B.

## Q061
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** traversing-trees
**Focus Area:** Inorder traversal
**Question:** For the tree with root M, left child H (children D and J) and right child T (child R), what is the inorder traversal? (a) D H J M R T (b) M H D J T R (c) M H D J R T (d) H D J M T R
**Answer:** (a) D H J M R T. The left subtree gives D H J, then the root M, then the right subtree R T. Options placing M first list the root too early — that's closer to preorder.

## Q062
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** traversing-trees
**Focus Area:** Postorder traversal
**Question:** For the tree with root M, left child H (children D and J) and right child T (child R), what is the postorder traversal? (a) D J H R T M (b) H D J M R T (c) M H D J T R (d) D H J M T R
**Answer:** (a) D J H R T M. Postorder lists children before their parent: left subtree D J H, then right subtree R T, then the root M.

## Q063
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** traversing-trees
**Focus Area:** Universal address system
**Question:** State the labelling rule for the universal address system, and explain what the label 2.1.3 means.
**Answer:** Label the root 0; label its children 1, 2, …, k from left to right; for any vertex labelled A, label its children A.1, A.2, …, A.k_A. The label 2.1.3 means: from the root, go to the 2nd child, then the 1st, then the 3rd.

## Q064
**Status:** active
**Type:** true-false
**Difficulty:** advanced
**Topic:** traversing-trees
**Focus Area:** Lexicographic order and preorder
**Question:** True or false: the lexicographic order of universal address system labels matches the preorder traversal order exactly.
**Answer:** True. The labels follow lexicographic order, giving a consistent left-to-right order across the entire tree, and this matches preorder traversal exactly.

## Q065
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** traversing-trees
**Focus Area:** Traversal use cases
**Question:** Give a use case for each of preorder, inorder and postorder traversal.
**Answer:** Preorder: copying or serializing trees, and generating prefix (Polish) expressions. Inorder: binary search trees (produces sorted order) and expression trees in infix notation (parentheses required). Postorder: deleting a tree safely bottom-up, evaluating postfix expressions, and computing subtree properties before parent use.

## Q066
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** traversing-trees
**Focus Area:** Expression trees
**Question:** In an expression tree, what do internal vertices and leaves represent, and how is the order of operations captured?
**Answer:** Internal vertices represent operators (like +, −, ∗, /, ↑) and leaves represent operands (variables, constants or literals). Each internal node applies its operator to its left and right subtrees, in that order. This structure captures the order of operations without relying on parentheses — the tree defines what depends on what.

## Q067
**Status:** active
**Type:** mcq
**Difficulty:** advanced
**Topic:** traversing-trees
**Focus Area:** Traversal and notation
**Question:** Which traversal produces postfix notation, and does it require parentheses? (a) Postorder; no parentheses needed (b) Inorder; no parentheses needed (c) Preorder; parentheses needed (d) Postorder; parentheses needed
**Answer:** (a) Postorder produces postfix notation, with the operator after the operands, and no parentheses are needed. Preorder produces prefix (operator before operands, no parentheses); inorder produces infix (operator between operands, parentheses required).

## Q068
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** traversing-trees
**Focus Area:** Worked expression traversal
**Question:** For the expression ((x + y)^2) + ((x − 4)/3), give the prefix and postfix forms.
**Answer:** Prefix (preorder): + ^ + x y 2 / - x 4 3. Postfix (postorder): x y + 2 ^ x 4 − 3 / +.

## Q069
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** traversing-trees
**Focus Area:** The single-curve model
**Question:** Explain how one curve drawn around a tree can produce all three traversal orders.
**Answer:** Imagine drawing a curve that hugs the outer edge of the tree, starting and ending at the root. For preorder, record a vertex the first time the curve touches it. For inorder (binary trees), record a leaf on the first touch and an internal vertex on the second. For postorder, record a vertex the last time the curve passes it. The three orders differ only by timing.

## Q070
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** traversing-trees
**Focus Area:** Traversal in real systems
**Question:** Why would a file system use preorder for copying but postorder for deleting?
**Answer:** File systems use tree traversal to search, list and delete directories: preorder can copy a file structure, while postorder safely removes one. Postorder visits all subtrees before the root, which is the bottom-up order needed for safe teardown, whereas preorder visits the root first, which suits building or copying structures.

## Q071
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** applications-of-trees
**Focus Area:** Binary search tree definition
**Question:** State the ordering rule that defines a binary search tree.
**Answer:** Every vertex has at most one left child and one right child; each vertex is assigned a key (one of the items being stored); and the key of a vertex is larger than all keys in its left subtree and smaller than all keys in its right subtree.

## Q072
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** applications-of-trees
**Focus Area:** Why BSTs are fast
**Question:** Why does a binary search tree provide faster searches than scanning a list? (a) It maintains order, so each comparison halves the search space (b) It stores data randomly (c) It uses extra memory for indexing (d) It connects all nodes in a loop
**Answer:** (a) It maintains order, so each comparison halves the search space — the ordered structure lets you skip large sections of data. Randomness would slow searching down, indexing isn't what makes BSTs efficient, and trees never contain cycles.

## Q073
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** applications-of-trees
**Focus Area:** BST search complexity
**Question:** How long does searching a well-balanced BST take, and why?
**Answer:** About O(log n) in the best case. Searching takes time proportional to the height of the tree because each comparison removes half of the remaining possibilities.

## Q074
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** applications-of-trees
**Focus Area:** Searching a BST
**Question:** In the BST built from 50, 30, 70, 20, 40, 60, 80, trace the search for 40 and the search for 75.
**Answer:** To find 40: start at 50 → move left (40 < 50) → find 40 at the next step. To find 75: start at 50 → right to 70 → right to 80 → not found.

## Q075
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** applications-of-trees
**Focus Area:** BST deletion
**Question:** How do you delete a node with two children from a BST, and why?
**Answer:** Replace it with the smallest value from its right subtree, in order to preserve the ordering of the tree.

## Q076
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** applications-of-trees
**Focus Area:** Decision tree leaves
**Question:** In a decision tree, what does each leaf node represent? (a) A final decision or outcome (b) A question or test (c) A starting condition (d) A relationship between outcomes
**Answer:** (a) A final decision or outcome — every path ends at a leaf that represents a result. A question or test is an internal node, the starting condition is the root, and edges (not leaves) represent relationships.

## Q077
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** applications-of-trees
**Focus Area:** Decision tree definition
**Question:** Define a decision tree, naming what the internal vertices, edges and leaves each represent.
**Answer:** A decision tree is a rooted tree in which each internal vertex represents a decision or test, each edge corresponds to one possible outcome of that decision, and the leaves represent final solutions or results. Each path from the root to a leaf describes one complete sequence of choices leading to a result.

## Q078
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** applications-of-trees
**Focus Area:** BSTs as decision trees
**Question:** In what sense is a binary search tree a type of decision tree?
**Answer:** At each node we decide whether to go left or right based on comparison results — for instance, "Is the key less than or greater than 50?" More generally, decision trees represent any problem solved through a chain of conditional checks.

## Q079
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** applications-of-trees
**Focus Area:** Limits of tree models
**Question:** Which of the following cannot be modelled as a tree? (a) A road network with circular routes (b) A hierarchical file system (c) A business organizational chart (d) A decision model
**Answer:** (a) A road network with circular routes — trees cannot contain cycles. The other three are standard tree use cases.

## Q080
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** applications-of-trees
**Focus Area:** Huffman coding
**Question:** How do Huffman coding trees compress data?
**Answer:** Huffman coding uses binary trees to compress data by assigning shorter codes to frequent symbols and longer codes to rare ones, minimizing the total number of bits used to store or transmit data. For example, "E" might be encoded as 0 while "Q" might be 11110, ensuring no code is a prefix of another. This forms the basis of many compression standards (ZIP, JPEG, MP3).

## Q081
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** applications-of-trees
**Focus Area:** File-system trees
**Question:** Map the parts of a file system onto tree terminology.
**Answer:** The root directory (like / or C:\) is the root node, folders are internal vertices, and files are leaves. Each file path (e.g. /Documents/Projects/Report.docx) is a unique path from the root to a leaf.

## Q082
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** applications-of-trees
**Focus Area:** Syntax trees
**Question:** What do syntax trees represent, and what statement does the tree with `=` at the root, `x` on the left, and `+` over `y` and `3` on the right represent?
**Answer:** In programming languages, syntax trees represent the grammatical structure of source code — each node corresponds to a component (an expression, operator or statement), showing how the code must be parsed and executed. That tree represents the statement x = y + 3.

## Q083
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** applications-of-trees
**Focus Area:** Game trees
**Question:** What do game trees represent, and what technique keeps them manageable?
**Answer:** In competitive games, game trees represent every possible move sequence: each branch corresponds to a possible move and each leaf represents an end state (win, loss, draw). Algorithms use pruning (e.g. alpha–beta pruning) to skip irrelevant paths and focus on the most promising strategies.

## Q084
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** applications-of-trees
**Focus Area:** Structural advantages of trees
**Question:** List the four structural advantages that make trees useful across all their applications.
**Answer:** Minimal redundancy (only one path connects any two vertices); hierarchical order (decisions and searches follow clear top-down logic); balanced performance (well-structured trees reduce operations from linear to logarithmic time); and predictability (the number of steps needed to find or process information depends on the tree's height).
