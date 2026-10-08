SLE-3: C4 Architectural Design – BFS vs DFS Graph Search System

Project Overview

This project presents the architectural design of a BFS vs DFS Graph Search System using the C4 Model.

The system implements Breadth-First Search (BFS) and Depth-First Search (DFS) on the same graph and compares their execution by observing the number of nodes expanded.

C4 Model

The architecture is represented at four levels:

1. Context Diagram – Shows the overall system and its interaction with the search request, results, and profiling tool.
2. Container Diagram – Shows the major modules of the system.
3. Component Diagram – Shows the internal components of the BFS Search Module.
4. Code Level – Shows the main Python files and implementation structure.

Main Modules

- Graph Data Module – Stores the graph used by both algorithms.
- BFS Search Module – Performs Breadth-First Search using a queue.
- DFS Search Module – Performs Depth-First Search using a stack.
- Output Module – Displays the search result and nodes expanded.
- Performance/Profiling Module – Supports performance observation using py-spy.

BFS

BFS explores the graph level by level using a queue. A visited set prevents the same node from being processed repeatedly.

DFS

DFS explores one branch deeply before backtracking. It uses a stack and a visited set.

Profiling

The project uses py-spy to observe Python program execution during BFS and DFS searches.

Files

- "bfs.py" – BFS implementation
- "dfs.py" – DFS implementation
- "bfs_for_pyspy.py" – BFS profiling execution
- "dfs_for_pyspy.py" – DFS profiling execution
- "profile_bfs.py" – BFS profiling script
- "profile_dfs.py" – DFS profiling script
- "C4_Context_Diagram.png" – Context diagram
- "C4_Container_Diagram.png" – Container diagram
- "C4_Component_Diagram.png" – Component diagram
- "SLE3_C4_Architecture.drawio" – Editable C4 diagrams
- "AI_Contribution_Log.md" – AI contribution record

Design Decisions

- The same graph is used for BFS and DFS to maintain a fair comparison.
- BFS uses a queue for level-by-level exploration.
- DFS uses a stack for depth-first exploration.
- A visited set avoids repeated node processing.
- Profiling is kept separate from the search implementation.

SLE-2 and SLE-3 Connection

SLE-2 focused on profiling and performance analysis of BFS and DFS.

SLE-3 extends the same project by representing its architecture using the C4 Model.

AI Contribution

ChatGPT was used to understand the SLE-3 requirements, plan the C4 architecture, organize the diagrams, and prepare documentation.

The implementation, testing, profiling, project organization, and final verification were carried out as part of the project work.

GitHub Repository

https://github.com/dudhaladiti-pixel/SLE2-BFS-DFS-Profiling
