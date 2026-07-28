# Practical 06 - Tracing Code & Logic - Summary

## Core Practical Concepts
This lab is entirely about **Code Tracing** (reading pseudo-code/Java and predicting the output). This tests your understanding of operator precedence, pre/post increments, and logical short-circuits.

## Key Rules to Memorize for Exams

### 1. Pre vs. Post Increment
*   `++x` (Pre-increment): Add 1 immediately, then use the new value.
*   `x++` (Post-increment): Use the current value for the calculation *first*, then add 1 afterwards.
*   **Example 01:**
    ```java
    x = 4;
    y = x++ + ++x;
    // Step 1: x++ uses 4 for the math, but x immediately becomes 5 in memory.
    // Step 2: ++x sees x is 5, adds 1 (x becomes 6), and uses 6 for the math.
    // y = 4 + 6 = 10.
    ```

### 2. Logical Short-Circuiting (`&&` and `||`)
*   If the left side of `&&` is `false`, Java **will not** execute the right side (because the whole thing is already false).
*   If the left side of `||` is `true`, Java **will not** execute the right side (because the whole thing is already true).
*   **Example 25:**
    ```java
    a = 1; b = 2;
    c = ++a > b && --b < a;
    // ++a makes 'a' = 2. 
    // 2 > 2 is FALSE.
    // Because the left side of && is false, the right side (--b < a) is SKIPPED.
    // Therefore, 'b' remains 2!
    ```

### 3. Bitwise Shift Operators (`<<`, `>>`, `>>>`)
*   `a << 2` (Left Shift): Shifts bits to the left. Mathematically equivalent to multiplying by $2^n$. So `3 << 2` is $3 \times 2^2 = 3 \times 4 = 12$.
*   `a >> 2` (Right Shift): Shifts bits right. Equivalent to dividing by $2^n$. `6 >> 2` is $6 / 4 = 1$.
