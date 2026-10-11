ADR-001: Use the Same Test Conditions for BFS and DFS Profiling
Student Information

- Name: Aditi Annaso Dudhal
- PRN: 25UAM134
- Division: B
- Course: 02AML204 – Introduction to Artificial Intelligence

1. Context

The BFS vs DFS Graph Search System implements two graph-search algorithms: Breadth-First Search (BFS) and Depth-First Search (DFS). Both algorithms need to be evaluated under consistent conditions to make their performance comparison meaningful.

In SLE-2, the profiling setup uses the same graph, starting node A, and goal nodes B, I, and K. The profiling scripts are designed to run 10 timing measurements and summarize the best, average, and worst execution times.

SLE-3 represents the system using context, container, and component diagrams. This ADR documents the decision connecting the implementation and profiling work with the system architecture.

2. Decision

Use the same graph, starting node, and goal-node test cases when comparing BFS and DFS. Keep their implementations and profiling scripts separate so that each algorithm can be executed and evaluated independently.

3. Alternatives Considered

Alternative 1: Use Different Graphs

Use different graphs for BFS and DFS. This could make the comparison unfair because the input structure would differ.

Alternative 2: Test Only One Goal Node

Use only one goal node for the comparison. This would provide less information about how the algorithms behave for different search cases.

Alternative 3: Compare Only Theoretical Complexity

Compare BFS and DFS using theoretical time and space complexity without executing profiling scripts. This would not provide measured execution times for the selected test cases.

4. Rationale

- Using the same graph keeps the input conditions consistent.
- Using the same starting node makes the test setup easier to compare.
- Testing goal nodes B, I, and K provides multiple search cases.
- Separate implementations help identify which algorithm is being executed.
- Repeated timing runs can reduce the influence of a single unusual measurement.
- Best, average, and worst recorded times provide different views of the measured performance.
- The decision connects the profiling activity in SLE-2 with the architecture diagrams in SLE-3.
- Actual timing results must be collected from program execution before drawing conclusions about which algorithm performs better.

5. Consequences

Positive Consequences

- The comparison uses consistent test conditions.
- Both algorithms can be profiled independently.
- The experiment is easier to repeat and verify.
- The decision and its reasoning are documented clearly.

Trade-offs and Limitations

- Profiling results can vary depending on the computer and runtime environment.
- A small number of test cases may not represent every possible graph.
- Measured execution time alone does not describe every aspect of algorithm performance.
- Actual profiling outputs must be retained to support performance claims.

6. Validation

The decision can be validated by checking that:

1. Both algorithms use the same graph.
2. Both algorithms use starting node A.
3. The test cases include goal nodes B, I, and K.
4. The profiling scripts perform the intended timing runs.
5. The best, average, and worst values are calculated from actual measurements.
6. The implementation and architecture files are present in the repository.

7. References

See "references.md" for the related SLE-2 and SLE-3 project links.
