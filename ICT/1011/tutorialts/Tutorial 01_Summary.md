# Tutorial 01 - Basics & Data Types - Summary

## Core Concepts
This tutorial tests your foundational knowledge of variable declarations, data types, basic operators, and the standard `main` method structure.

## Practical Questions & Tricks

### Q1: The Main Method Skeleton
*   **Code:** `public class Hello { public static void main(String[] args) { ... } }`
*   *Explanation:* `public` means accessible anywhere. `class` defines the blueprint. `static` means it belongs to the class itself. `void` means it returns nothing. `main` is the entry point. `String[] args` handles command-line arguments.

### Q2 & Q3: Variable Declarations & Data Types
*   **Valid/Invalid Names:** Variable names *cannot* start with a number. (e.g., `int 2count = 5;` is INVALID).
*   **Choosing Data Types:**
    *   Age: `int` (or `byte`)
    *   Population of the world: `long` (it's > 2 billion!)
    *   Price: `double` (needs decimals)
    *   Passed an exam: `boolean` (true/false)
    *   Letter grade: `char` (single character)

### Q4, Q5, Q6, Q7: Expressions & Operators
*   **Integer Division:** `10 / 3` evaluates to `3` (fraction is truncated).
*   **Floating Division:** `10.0 / 3` evaluates to `3.333333...`
*   **Modulo:** `10 % 3` evaluates to `1` (remainder).
*   **Pre vs. Post Increment:**
    *   `int a = i++;` -> `a` gets the old value of `i`, then `i` increases.
    *   `int b = ++i;` -> `i` increases first, then `b` gets the new value.
