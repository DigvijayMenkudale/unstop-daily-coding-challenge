# Day 01 – The Dream Weaver's Resonance Loom

## 📌 Platform
**Unstop – Problem of the Day (POTD)**

## 📅 Date
**17 July 2026**

## 💻 Language
**Python 3.11**

## 📊 Difficulty
**Medium**

## 🏷️ Topics
- Dynamic Programming
- Matrix Chain Multiplication
- Interval DP

## 📝 Problem Summary

Given the dimensions of a sequence of matrices, determine the minimum number of scalar multiplications required to multiply the entire chain. Since matrix multiplication is associative, different parenthesizations lead to different computational costs. The objective is to find the minimum possible multiplication cost.

## 💡 Approach

This problem is solved using **Dynamic Programming (Matrix Chain Multiplication)**.

- Define `dp[i][j]` as the minimum multiplication cost for multiplying matrices from index `i` to `j`.
- Consider every possible partition point `k` between `i` and `j`.
- Compute the cost of splitting at `k` and keep the minimum value.
- Build the DP table from smaller chains to larger chains until the complete answer is obtained.

## ⚙️ Algorithm

1. Read the matrix dimensions.
2. Initialize a DP table with zero values.
3. Process matrix chains in increasing order of length.
4. For every chain, try every possible partition.
5. Store the minimum multiplication cost.
6. Output the minimum cost for the complete matrix chain.

## ⏱️ Time Complexity

**O(N³)**

## 💾 Space Complexity

**O(N²)**

## 🎯 Learning Outcome

- Learned how interval-based Dynamic Programming works.
- Understood optimization using Matrix Chain Multiplication.
- Practiced building solutions using bottom-up DP.

## ✅ Status

**Accepted**
