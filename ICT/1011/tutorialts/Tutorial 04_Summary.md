# Tutorial 04 - Math Expressions & Custom Methods - Summary

## Core Concepts
Translating mathematical formulas into Java expressions, and writing complete standalone functions (methods) based on specifications.

## Practical Questions & Tricks

### Q1: Writing Java Math Expressions
You must convert standard math notation into code understandable by the compiler.
*   **Fractions:** $\frac{1}{2}z$ becomes `(1.0 / 2.0) * z` OR `0.5 * z`. (Never use `1/2` as it equals `0` in integer division).
*   **Powers:** $\frac{x^3}{y^2}$ becomes `Math.pow(x, 3) / Math.pow(y, 2)`.
*   **Roots:** $\sqrt{x^2 + y^2}$ becomes `Math.sqrt( (x*x) + (y*y) )` OR `Math.sqrt( Math.pow(x,2) + Math.pow(y,2) )`.

### Q2: Writing Custom Functions (Methods)
When an exam asks you to "Write a function...", you must provide the full method signature and body.

*   **(c) Grade Function:** `public static char grade(int mark)` -> Use an `if - else if` ladder.
*   **(d) Max of 3 Integers:** `public static int max(int a, int b, int c)` -> Use `Math.max(a, Math.max(b, c));` or nested `if` statements.
*   **(e) Discount Function:** `public static double discount(int quantity, double unitPrice)`
    *   `double total = quantity * unitPrice;`
    *   Use an `if - else if` ladder on `total` to determine the rate.
    *   `return total * rate;`
*   **(f) Leap Year Function:** `public static boolean leapyear(int year)`
    *   *Formula:* `return (year % 4 == 0 && year % 100 != 0) || (year % 400 == 0);`
