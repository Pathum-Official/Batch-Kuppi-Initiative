# Tutorial 03 - Loops & Tracing - Summary

## Core Concepts
This tutorial focuses entirely on **Loops** (`for`, `while`, `do-while`), nested loops, and loop control statements (`break`, `continue`).

## Practical Questions & Tricks

### Tracing `while` and `do-while` loops
*   **`while (condition)`:** Checks the condition *before* entering. If false initially, it runs 0 times.
*   **`do { ... } while (condition)`:** Executes the body *first*, then checks the condition. It always runs at least 1 time.
*   *Exam Tip:* When tracing loops, write down the variables on a piece of paper and cross them out as they change during each iteration.

### Nested `for` loops
*   *Logic:* For every single iteration of the outer loop, the inner loop runs completely from start to finish.
*   *Example Output:*
    ```java
    for(int a=0; a<2; a++) {
        for(int b=0; b<2; b++) {
            System.out.print("* ");
        }
        System.out.print("\n");
    }
    ```
    This prints a 2x2 grid of stars. The outer loop handles rows (`\n`), the inner loop handles columns.

### `break` vs. `continue`
*   **`break;`**: Instantly kills the loop entirely. Execution jumps to the code *after* the loop block.
*   **`continue;`**: Instantly skips the *rest of the current iteration* and jumps straight to the next cycle of the loop.
    *   *Example:* `for(int i=0; i<3; i++) { if(i==1) continue; print(i); }` -> Prints `0` and `2`. `1` is skipped.
