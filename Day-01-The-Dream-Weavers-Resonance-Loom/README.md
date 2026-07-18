# Day 01 – The Dream Weaver's Resonance Loom

## 📌 Platform
Unstop – Problem of the Day (POTD)

## 📅 Date
17 July 2026

## 💻 Language
Python 3.11

## 📝 Problem Summary

Given a sequence of matrix dimensions, determine the minimum number of scalar multiplications required to multiply the entire chain of matrices. The order of multiplication affects the total computation cost, so the objective is to find the optimal parenthesization.

## 🧠 Approach

The problem is solved using **Dynamic Programming (Matrix Chain Multiplication)**.

- Define `dp[i][j]` as the minimum multiplication cost for matrices from `i` to `j`.
- For every possible split point `k`, calculate the multiplication cost.
- Store the minimum cost among all possible partitions.

## ⚙️ Algorithm

1. Create a 2D DP table.
2. Initialize diagonal values as 0.
3. Iterate over chain lengths from 2 to N.
4. Try every partition point.
5. Store the minimum multiplication cost.
6. Print the final answer.

## ⏱️ Time Complexity

O(N³)

## 💾 Space Complexity

O(N²)

## ✅ Status

Accepted
