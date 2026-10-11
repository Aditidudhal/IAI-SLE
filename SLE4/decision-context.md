Decision Context: BFS vs DFS Graph Search System

1. Purpose

This file explains the technical context behind the architecture decision documented in "ADR-001-same-test-conditions.md".

2. Breadth-First Search (BFS)

BFS explores a graph level by level, visiting nearby nodes before moving to nodes farther away. It commonly uses a queue to manage the order of exploration.

3. Depth-First Search (DFS)

DFS explores one path as deeply as possible before returning to explore another path. It commonly uses a stack or recursion to manage the exploration process.

4. Why Compare BFS and DFS?

Both algorithms can search a graph, but their traversal order and resource usage can differ. Testing them with the same graph and test conditions makes their observed behaviour easier to compare.

5. SLE-2 Profiling Setup

The documented profiling setup includes:

- Starting node: A
- Goal nodes: B, I, and K
- Number of timing runs: 10
- Measurements summarized: best, average, and worst execution times

These describe the profiling setup, not verified performance results. Actual results must be copied from the output of the executed scripts.

6. Connection with SLE-3

The C4 architecture diagrams describe the system at different levels:

- Context diagram: Shows the system and its interactions with external actors or systems.
- Container diagram: Shows the main applications or containers that make up the system.
- Component diagram: Shows the internal components and their responsibilities.

7. Final Design Reasoning

The decision to use consistent test conditions supports a fairer comparison between BFS and DFS. Keeping implementations and profiling scripts separate also makes it easier to execute, inspect, and verify each algorithm independently.
