# Practical 04 - Applied Math & Expressions - Summary

## Core Practical Concepts
This lab forces you to translate real-world mathematical formulas into Java expressions using variables and the `Math` library.

## Practical Questions & How to Code Them Easily

### Q1 & Q2: Bill & Commission Calculations
*   **Goal:** Calculate values based on percentages and fixed charges.
*   **How to code:** 
    *   Percentages: Always multiply by the decimal (e.g., 30% is `0.30`).
    *   *Example:* `double earning = premium * 0.30;`

### Q3 & Q7: Geometric Formulas (Cone Volume, Cartesian Distance)
*   **Goal:** Write formulas like $V = \pi r^2 (h/3)$ or distance $= \sqrt{(x_1-x_2)^2 + (y_1-y_2)^2}$
*   **How to code:**
    *   Use `Math.PI` for $\pi$.
    *   Use `Math.pow(base, exponent)` for powers. -> `Math.pow(r, 2)`
    *   Use `Math.sqrt(value)` for square roots.
    *   *Volume:* `double v = Math.PI * Math.pow(r, 2) * (h / 3.0);` (Remember `3.0` for double division!).

### Q8: Complex Trigonometry (Geographic Distance)
*   **Goal:** Convert formulas with `sin`, `cos`, `atan2` into Java.
*   **How to code:**
    *   `Math.toRadians(degrees)` to get radians.
    *   `Math.sin(radians)`, `Math.cos(radians)`
    *   `Math.atan2(y, x)` (Note the order of y and x).
    *   `Math.abs(value)` for absolute differences.

## Key Exam Takeaway
When writing math formulas in Java:
1.  **Never** write fractions like `1/2` or `5/9` if you expect a decimal result. Always write `1.0/2.0`.
2.  Use the built-in `Math` class methods. You don't need to import `java.lang.Math`, it's automatic.
