# Day 04 – The Festival Drum Beat

## 📌 Platform
**Unstop – Problem of the Day (POTD)**

## 📅 Date
**20 July 2026**

## 💻 Language
**C++17 (GCC 13.2.0)**

## 📊 Difficulty
**Easy**

## 🏷️ Topics
- Mathematics
- Number Theory
- Greatest Common Divisor (GCD)
- Least Common Multiple (LCM)

## 📝 Problem Summary

Two ceremonial drums produce beats at fixed intervals:

- Kabir's drum beats every **A** seconds.
- Tara's drum beats every **B** seconds.

Both drums are struck together at time **0**.

The objective is to determine the earliest time when both drums beat together again.

## 💡 Approach

The first time both drums beat together again is the **Least Common Multiple (LCM)** of their beat intervals.

Using the mathematical relationship:

**LCM(A, B) = (A × B) / GCD(A, B)**

The Greatest Common Divisor (GCD) is computed using the built-in `__gcd()` function, and the LCM is calculated efficiently while avoiding unnecessary overflow by dividing before multiplying.

## ⚙️ Algorithm

1. Read integers `A` and `B`.
2. Compute `GCD(A, B)`.
3. Compute `LCM = (A / GCD) × B`.
4. Print the LCM.

## ⏱️ Time Complexity

**O(log(min(A, B)))**

## 💾 Space Complexity

**O(1)**

## 🎯 Learning Outcome

- Learned the relationship between GCD and LCM.
- Practiced solving mathematical problems using Number Theory.
- Understood how to compute LCM efficiently using the Euclidean Algorithm.

## ✅ Status

**Accepted (12/12 Test Cases Passed | Score: 100/100)**
