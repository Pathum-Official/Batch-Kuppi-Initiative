# Practical 08 - Loops, Patterns & Math Series - Summary

## Core Practical Concepts
This lab is heavily focused on **loops (`for`, `while`)** to perform repetitive calculations, generate mathematical series, and print visual patterns.

## Practical Questions & How to Code Them Easily

### 1. Basic Sums & Averages (Q1-Q4)
*   **Goal:** Find sum and average of $N$ numbers.
*   **How to code:** Use a `for` loop, a `sum` variable (starting at 0), and add to it inside the loop.
    ```java
    int sum = 0;
    for(int i = 1; i <= n; i++) {
        sum += i;
    }
    double avg = (double) sum / n;
    ```

### 2. Printing Patterns (Q5, Q6, Q14, Q15)
*   **Goal:** Print shapes like Right Angle Triangles, Pascal's Triangle, Floyd's Triangle.
*   **How to code:** Use **Nested Loops**. The outer loop controls the *rows*, the inner loop controls the *columns*.
    ```java
    for (int i = 1; i <= rows; i++) {
        for (int j = 1; j <= i; j++) {
            System.out.print(j + " "); // Or print a counter for Floyd's Triangle
        }
        System.out.println(); // Move to next line
    }
    ```

### 3. Math Series (Factorial, Harmonic, Fibonacci, $e^x$)
*   **Factorial (Q9):** Multiply numbers from 1 to $n$. `for(int i=1; i<=n; i++) fact *= i;`
*   **Fibonacci (Q13):** Keep track of two previous numbers. `next = a + b; a = b; b = next;`
*   **Permutation/Combination (Q10, Q11):** $nPr = \frac{n!}{(n-r)!}$. Create a factorial function and call it multiple times.
*   **$e^x$ series (Q23):** You need a loop that calculates $\frac{x^n}{n!}$ and adds it to a sum.

### 4. Number Checking (Prime, Perfect)
*   **Prime Number (Q16):** A number divisible only by 1 and itself. Loop from 2 to $n/2$ and check if `n % i == 0`. If yes, it's not prime.
*   **Perfect Number (Q18):** Sum of its divisors equals the number itself (e.g., 6 = 1+2+3).

## Exam Tip
Questions asking for "Series", "Factorials", or "Patterns" are guaranteed to need **`for` loops**. If you need to print a 2D shape, always write a **nested `for` loop**.
