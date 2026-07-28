# 06 Control Structures II (Loops) - Summary

## 1. `while` Loop
Executes statements repeatedly **while** the condition is true. It evaluates the condition *before* executing the loop body.
*   *Syntax:*
    ```java
    while (loop-continuation-condition) {
        // Loop body
    }
    ```
*   *Note:* If the condition is initially false, the loop body might not execute even once.

## 2. `do-while` Loop
Similar to the `while` loop, but it executes the loop body **first**, and *then* checks the condition.
*   *Syntax:*
    ```java
    do {
        // Loop body
    } while (loop-continuation-condition);
    ```
*   *Note:* The loop body is guaranteed to execute at least once.

## 3. `for` Loop
A concise syntax for writing loops, mostly used when you know exactly how many times the loop should run (counter-controlled loop).
*   *Syntax:*
    ```java
    for (initial-action; loop-continuation-condition; action-after-each-iteration) {
        // Loop body
    }
    ```
    *(e.g., `for (int i = 0; i < 100; i++)`)*
*   *Note:* The variable `i` declared inside the `for` loop cannot be used outside of it (Block Scope).

## 4. `foreach` Loop
Used to easily traverse an array sequentially without needing an index variable.
*   *Syntax:*
    ```java
    for (elementType element : arrayRefVar) {
        // Process the element
    }
    ```
