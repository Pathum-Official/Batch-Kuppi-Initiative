# 05 Control Structures I - Summary

## 1. `if` Statements
Used to specify alternative paths of execution based on a condition.
*   **One-way `if`:** Executes an action only if the condition is `true`.
    ```java
    if (boolean-expression) {
        // statement(s)
    }
    ```

## 2. `if-else` Statements
Decides the execution path based on whether the condition is true or false.
*   **Two-way `if-else`:**
    ```java
    if (boolean-expression) {
        // executes if true
    } else {
        // executes if false
    }
    ```

*   **Secret Tip for Exams:** If the condition returns a boolean directly, you don't need the `if-else`. 
    *   *Long way:* `if (number % 2 == 0) even = true; else even = false;`
    *   *Short way:* `boolean even = (number % 2 == 0);`

## 3. Nested & Multi-way `if-else`
*   **Nested `if`:** An `if` statement inside another `if` statement. No depth limit.
*   **Multi-way `if-else` (Preferred format):** Used for grading or multiple alternatives.
    ```java
    if (score >= 90.0) {
        System.out.print("A");
    } else if (score >= 80.0) {
        System.out.print("B");
    } else {
        System.out.print("F");
    }
    ```

## 4. `switch` Statements
Simplifies coding for multiple conditions based on the value of a single variable.
*   **Rules:**
    1.  The `switch-expression` must yield a `char`, `byte`, `short`, `int`, or `String`.
    2.  The `case` values must be constants (no variables like `1 + x`) and match the expression's data type.
    3.  The `break` keyword stops the switch block. If omitted, execution falls through to the next case!
    4.  The `default` case is optional and runs if no match is found.

*   **Syntax:**
    ```java
    switch (switch-expression) {
        case value1: 
            // statement(s)
            break;
        case value2: 
            // statement(s)
            break;
        default: 
            // statement(s)
    }
    ```
