# Algorithms: Data-Structure Checkpoint

This repository contains pseudocode solutions for two problems using arrays and clear, commented algorithms.

## Problem 1 — Sum of Distinct Elements

- Goal: Given two arrays `A` and `B`, compute the sum of all elements that appear in exactly one of the arrays (set symmetric difference).
- Approach: Arrays + nested loops. Two passes:
  1. Add elements in `A` that are not in `B` (count each value once).
  2. Add elements in `B` that are not in `A` (count each value once).
- File: `problem1.algo`
- Notes: Handles duplicates by ensuring each distinct value is added at most once.

Example:
- Set 1: [3, 1, 7, 9]
- Set 2: [2, 4, 1, 9, 3]
- Output: 13 (distinct values: 4, 7, 2)

## Problem 2 — Dot Product and Orthogonality

- Goal: Implement a dot product and use it to check if vector pairs are orthogonal.
- Files: `problem2.algo`
- Contains:
  - `PROCEDURE dot_product(v1, v2, n, REF ps)`: computes the dot product into `ps` (pass-by-reference OUT parameter).
  - `ALGORITHM Orthogonality_Check_Using_Procedure`: reads `t` pairs of vectors and reports whether each pair is orthogonal by calling the procedure.
  - `FUNCTION dot_product_f(v1, v2, n) RETURNS REAL`: returns the scalar dot product directly.
  - `ALGORITHM Orthogonality_Check_Using_Function`: same check using the function version.
- Parameter passing:
  - Procedure uses a REF (OUT) parameter for the result; vectors and `n` are IN parameters.
  - Function returns the result directly.
- Numerical note: Uses a small `EPS = 1e-9` when comparing to zero for floating-point safety.
- Structures used: Arrays and nested loops (reading inputs and iterating vector components).

## How to Use

These are language-agnostic pseudocode files. Open them to study the algorithms or use them as a guide to implement in your preferred language (C, Java, Python, etc.).

Suggested implementation steps in any language:
1. Read inputs (array sizes and elements).
2. Translate the pseudocode control structures (FOR, IF, FUNCTION/PROCEDURE) to the target language equivalents.
3. For Problem 2, remember to compare the dot product to zero with a small tolerance if using floating-point types.

## Evaluation Checklist

- Arrays used for data representation.
- Nested loops demonstrated (membership checks, input reading, dot product accumulation).
- Clear, commented pseudocode.
- This README explains approach and usage.
