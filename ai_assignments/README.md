## 8-Puzzle Solver – Search Algorithms Comparison

This project implements and compares classic search algorithms (BFS, DFS, UCS, A*, etc.) for solving the 8-puzzle problem — a sliding tile puzzle where you arrange numbers 1–8 into their goal configuration with the blank (0) at the end.

### Features
*- Multiple Search Strategies*

  -  BFS (Breadth-First Search) – Explores shallow nodes first. Guarantees shortest path, but memory heavy.

  -  DFS (Depth-First Search) – Explores deep paths first. Fast but not guaranteed to find optimal solution.

  -  UCS (Uniform Cost Search) – Explores lowest path cost first (like Dijkstra).

  -  A* – Uses heuristics for efficient goal search.

*-Manhattan Distance heuristic*

  -Linear Conflict heuristic (improved Manhattan)

  -Performance Metrics

  -Path cost

  -Nodes expanded

  -Execution time

  -Average statistics across multiple randomized start states

###  How It Works

1. The program generates random solvable 8-puzzle configurations.

2. Each configuration is solved using all algorithms.

3. Results are displayed in CSV-style output with timing and performance metrics.

4. The script compares UCS vs A*-Manhattan vs A*-LinearConflict averages.

###  Requirements

Python 3.8+

Jupyter Notebook (or run via VSCode/Colab)

No external dependencies required — only standard Python libraries:  random, time, heapq, itertools, collections, statistics

### Sample Output

Case, Method, PathCost, NodesExpanded, Time(s)
Case1,UCS,18,1850,0.053
Case1,A*-Manhattan,18,530,0.015
Case1,A*-LinearConflict,18,420,0.011

Averages over 5 starts:
UCS  : nodes=1720, time=0.0431s
A* M : nodes=560, time=0.0153s
A* LC: nodes=410, time=0.0112s
