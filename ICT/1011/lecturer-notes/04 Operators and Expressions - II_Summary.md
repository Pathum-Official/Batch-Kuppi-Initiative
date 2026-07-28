# 04 Operators and Expressions II - Summary

## 1. Relational (Comparison) Operators
Used to compare two values. The result is always a `boolean` (`true` or `false`).
*   `<` : Less than (e.g., `radius < 0`)
*   `<=` : Less than or equal to
*   `>` : Greater than
*   `>=` : Greater than or equal to
*   `==` : Equal to (Do not confuse with `=` which is for assignment!)
*   `!=` : Not equal to

## 2. Logical Operators
Used to combine multiple boolean expressions into a compound expression.

### `!` (NOT / Logical Negation)
Reverses the truth value.
*   `!true` becomes `false`
*   `!false` becomes `true`

### `&&` (AND / Logical Conjunction)
Returns `true` ONLY IF **both** conditions are `true`.
*   `true && true` -> `true`
*   `true && false` -> `false`
*   `false && false` -> `false`

### `||` (OR / Logical Disjunction)
Returns `true` if **at least one** condition is `true`.
*   `true || false` -> `true`
*   `false || true` -> `true`
*   `false || false` -> `false`

### `^` (XOR / Logical Exclusion)
Returns `true` if the conditions are **different** (one true, one false). Returns `false` if they are the same.
*   `true ^ false` -> `true`
*   `false ^ true` -> `true`
*   `true ^ true` -> `false`
*   `false ^ false` -> `false`

## 3. High-Yield Exam Applications
You will often see these in exam scenarios:
*   Checking divisibility: `number % 2 == 0` (Is the number even?)
*   Checking multiple conditions: `(number % 2 == 0) && (number % 3 == 0)` (Is it divisible by both 2 AND 3?)
*   Checking leap years: `(year % 4 == 0 && year % 100 != 0) || (year % 400 == 0)`
