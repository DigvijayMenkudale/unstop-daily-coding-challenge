# Day 02 – Lantern Grid of Diyari Festival

## 📌 Platform
**Unstop – Problem of the Day (POTD)**

## 📅 Date
**18 July 2026**

## 💻 Language
**C++17 (GCC 13.2.0)**

## 📊 Difficulty
**Hard**

## 🏷️ Topics
- Segment Tree
- Segment Tree Beats
- Range Queries
- Data Structures

## 📝 Problem Summary

Given an array representing the brightness of lanterns, process two types of range queries efficiently:

1. **Range Ceiling Update:** For all elements in a given range, replace every value greater than `v` with `v`.
2. **Range Sum Query:** Return the sum of all elements within a given range.

With up to **200,000 elements** and **200,000 queries**, a naive solution would exceed the time limit. The challenge is to support both operations efficiently.

## 💡 Approach

This problem is solved using **Segment Tree Beats**, an advanced variant of the Segment Tree designed to efficiently handle range `chmin` (minimum assignment) operations.

Each node of the segment tree stores:

- Sum of the segment
- Maximum value
- Second maximum value
- Count of occurrences of the maximum value

Using this information:

- Range ceiling updates only affect elements currently greater than the given value.
- If the update only modifies the maximum values of a segment, the update is applied directly without visiting all child nodes.
- Range sum queries are answered in logarithmic time.

This optimization significantly reduces unnecessary recursion and satisfies the strict performance requirements.

## ⚙️ Algorithm

1. Build a Segment Tree from the input array.
2. Store the following for each node:
   - Segment Sum
   - Maximum Value
   - Second Maximum Value
   - Count of Maximum Values
3. For each update query:
   - Ignore segments already satisfying the ceiling.
   - Apply the ceiling directly when possible.
   - Otherwise propagate updates recursively.
4. For each sum query:
   - Traverse only the required segments.
   - Return the accumulated sum.

## ⏱️ Time Complexity

- Build Segment Tree: **O(N)**
- Range Ceiling Update: **Amortized O(log N)**
- Range Sum Query: **O(log N)**

## 💾 Space Complexity

**O(N)**

## 🎯 Learning Outcome

- Learned the Segment Tree Beats technique.
- Understood how maintaining maximum and second maximum values enables efficient range ceiling updates.
- Practiced solving advanced range query problems under strict performance constraints.
- Improved understanding of optimized tree-based data structures.

## ✅ Status

**Accepted**
