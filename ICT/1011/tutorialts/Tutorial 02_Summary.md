# Tutorial 02 - Conditionals & Error Finding - Summary

## Core Concepts
This tutorial heavily tests your ability to spot syntax errors in `if-else` blocks and predict the output of conditional chains and `switch` statements.

## Practical Questions & Tricks

### Q1: Finding Syntax Errors
*   **Missing Semicolons:** A common trap. `System.out.println("Text")` without a `;` will cause a compile error.
*   **Equality Check vs Assignment:** `if (intNum % 2 = 0)` is **WRONG**. A single `=` is for assignment. You must use `==` for comparison in an `if` condition: `if (intNum % 2 == 0)`.

### Q2 & Q3: If-Else Ladders
*   **Logic:** When you have a chain of `if - else if - else`, the program checks from top to bottom. The **first** condition that evaluates to `true` is executed, and the rest of the chain is completely skipped.
*   *Exam Tip:* Always trace the variable value step-by-step downwards.

### Q4: The Conditional (Ternary) Operator
*   *Syntax:* `variable = (condition) ? value_if_true : value_if_false;`
*   *Example:* `String result = (10 > 20) ? "a is Greater" : "b is Greater";`
    *   Since 10 > 20 is false, `result` becomes `"b is Greater"`.

### Q5: Switch Statement & The `break` Keyword
*   *Logic:* A `switch` statement checks a variable against multiple `case` values.
*   *Crucial Trap:* If a `case` matches but does **not** have a `break;` statement at the end of it, the execution will "fall through" and execute all subsequent cases until it hits a `break` or the end of the switch block!
