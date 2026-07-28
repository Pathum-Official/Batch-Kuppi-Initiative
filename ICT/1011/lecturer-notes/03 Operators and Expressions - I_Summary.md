# 03 Operators and Expressions I - Summary

## 1. Assignment Operators
*   **Basic Assignment (`=`):** Designates a value to a variable. Always evaluates from right to left.
    *   *Syntax:* `variable = expression;` (e.g., `x = y + 1;`)
    *   *Error:* `1 = x;` is wrong. The variable must be on the left.
*   **Constants:** Represents a permanent value. Uses the `final` keyword.
    *   *Syntax:* `final datatype CONSTANTNAME = value;` (e.g., `final double PI = 3.14159;`)
    *   *Why use constants?* Easier to read, and you only have to change the value in one place.

## 2. Augmented Assignment Operators
Combine basic operations with assignment to write shorter code.
*   `+=` (Addition assignment) : `i += 8` is equivalent to `i = i + 8`
*   `-=` (Subtraction assignment) : `i -= 8` is equivalent to `i = i - 8`
*   `*=` (Multiplication assignment) : `i *= 8` is equivalent to `i = i * 8`
*   `/=` (Division assignment) : `i /= 8` is equivalent to `i = i / 8`
*   `%=` (Remainder assignment) : `i %= 8` is equivalent to `i = i % 8`

## 3. Increment and Decrement Operators
Used to add or subtract 1 from a variable.
*   `++var` (Pre-increment): Increments `var` by 1, and uses the **new** value in the statement.
*   `var++` (Post-increment): Increments `var` by 1, but uses the **original** value in the statement.
*   `--var` (Pre-decrement): Decrements `var` by 1, and uses the **new** value.
*   `var--` (Post-decrement): Decrements `var` by 1, but uses the **original** value.

## 4. Numeric Type Conversions (Casting)
Casting converts a value of one data type into another.
*   **Widening:** Converting a smaller range type to a larger range type (e.g., `int` to `double`). Java does this **automatically**.
*   **Narrowing:** Converting a larger range type to a smaller range type (e.g., `double` to `int`). You must do this **explicitly** using casting.
    *   *Example:* `(int) 1.7` becomes `1` (fractional part is truncated, NOT rounded).
*   **Binary Operations:** If an integer and a floating-point are used together, the integer is automatically converted to a floating-point. (e.g., `3 * 4.5` becomes `3.0 * 4.5`).
*   **Integer Division:** `1 / 2` yields `0` because both are integers. `1.0 / 2` yields `0.5`.
