# Day 05 – Ancient Archive Recovery

## 📌 Platform
**Unstop – Problem of the Day (POTD)**

## 📅 Date
**21 July 2026**

## 💻 Language
**C++17 (GCC 13.2.0)**

## 📊 Difficulty
**Medium**

## 🏷️ Topics
- Binary Search Tree (BST)
- Binary Tree
- Tree Traversal
- Postorder Traversal
- Recursion

## 📝 Problem Summary

A sequence of artifact numbers is inserted into a **Binary Search Tree (BST)** in the given order.

The historians follow a recovery protocol where they:

1. Explore the left subtree.
2. Explore the right subtree.
3. Record the current chamber.

The task is to print the resulting sequence of artifact numbers.

## 💡 Approach

- Construct the Binary Search Tree by inserting each artifact number in the given order.
- Perform a **Postorder Traversal (Left → Right → Root)**.
- Store the traversal in a vector and print the result.

## ⚙️ Algorithm

1. Read the number of nodes.
2. Insert each value into the BST.
3. Perform Postorder Traversal.
4. Print the traversal sequence.

## ⏱️ Time Complexity

- BST Construction: **O(N × H)**
- Postorder Traversal: **O(N)**

Where **H** is the height of the BST.

- Best/Average Case: **O(N log N)**
- Worst Case (Skewed Tree): **O(N²)**

## 💾 Space Complexity

- BST Storage: **O(N)**
- Recursion Stack: **O(H)**

Overall: **O(N)**

## 🎯 Learning Outcome

- Learned how Binary Search Trees are constructed.
- Practiced recursive tree traversal.
- Understood Postorder Traversal (Left → Right → Root).
- Strengthened Binary Tree problem-solving skills.

## ✅ Status

**Accepted (12/12 Test Cases Passed | Score: 120/120)**
