# Day 03 – Kingdom of Sealed Messengers

## 📌 Platform
**Unstop – Problem of the Day (POTD)**

## 📅 Date
**19 July 2026**

## 💻 Language
**C++17 (GCC 13.2.0)**

## 📊 Difficulty
**Hard**

## 🏷️ Topics
- Graph Theory
- Strongly Connected Components (SCC)
- Kosaraju's Algorithm
- Directed Graph
- Depth First Search (DFS)

## 📝 Problem Summary

The kingdom consists of **N** cities connected by one-way messenger portals.

A messenger starting from one city can travel through directed portals and spread the royal announcement to all reachable cities.

Some groups of cities form **Strongly Connected Components (SCCs)**, where every city in the group can reach every other city.

The objective is to determine the **minimum number of starting cities** required so that the announcement eventually reaches every city in the kingdom.

## 💡 Approach

The problem is solved using **Kosaraju's Algorithm**.

1. Perform DFS on the original graph to obtain the finishing order of vertices.
2. Reverse all edges of the graph.
3. Process vertices in reverse finishing order to identify all Strongly Connected Components.
4. Build the SCC condensation graph.
5. Count the number of SCCs having **zero incoming edges**.
6. That count represents the minimum number of initial announcers required.

To avoid recursion depth issues for large graphs, the implementation uses **iterative DFS** with explicit stacks.

## ⚙️ Algorithm

1. Read the directed graph.
2. Perform iterative DFS on the original graph.
3. Store vertices according to finishing time.
4. Traverse the reversed graph in reverse finishing order.
5. Assign component IDs for every vertex.
6. Identify SCCs with no incoming edges.
7. Output the total count.

## ⏱️ Time Complexity

- Building Graph: **O(N + M)**
- First DFS: **O(N + M)**
- Second DFS: **O(N + M)**
- Final Traversal: **O(M)**

**Overall:** **O(N + M)**

## 💾 Space Complexity

**O(N + M)**

## 🎯 Learning Outcome

- Learned how to identify Strongly Connected Components using Kosaraju's Algorithm.
- Understood SCC condensation graphs.
- Practiced iterative DFS to safely handle large graph constraints.
- Solved a large-scale graph traversal problem efficiently.

## ✅ Status

**Accepted (12/12 Test Cases Passed | Score: 150/150)**
