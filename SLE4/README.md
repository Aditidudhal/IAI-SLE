# SLE-4: Architecture Decision Record (ADR)

**Course:** 02AML204 – Introduction to Artificial Intelligence  
**Student:** Aditi Annaso Dudhal  
**PRN:** 25UAM134  
**Division:** B  
**System:** BFS vs DFS Graph Search System

## Project Overview

This repository documents the design decisions, algorithm design, profiling approach, testing considerations, and limitations of a graph-search system that compares Breadth-First Search (BFS) and Depth-First Search (DFS).

The purpose of SLE-4 is to explain why a particular design decision was selected, what alternatives were considered, and what consequences follow from that decision.

## Objectives

- Document an important architectural and experimental decision.
- Explain the difference between BFS and DFS.
- Describe how the profiling experiment is organized.
- Connect the design decision with the earlier SLE activities.
- Identify testing considerations and limitations.
- Maintain a transparent record of AI assistance.

## SLE Progress

- **SLE-1:** Basic AI agent + AI Contribution Log.
- **SLE-2:** Profiling and comparison of BFS and DFS using separate scripts.
- **SLE-3:** Architectural documentation using the C4 model.
- **SLE-4:** Documentation and justification of a design decision using an ADR.

## Repository Structure

| File | Purpose |
|---|---|
| `README.md` | Project overview and navigation |
| `ADR-001-same-graph-for-bfs-dfs.md` | Main design decision |
| `design-and-profiling.md` | Algorithm design and profiling methodology |
| `testing-and-limitations.md` | Testing approach and limitations |
| `AI_Contribution_Log.md` | AI assistance and verification |
| `references.md` | Source repositories |

## Main Decision

Use the same graph and starting node for BFS and DFS, and compare their behaviour using the same selected goal nodes. This provides more consistent experimental conditions.
