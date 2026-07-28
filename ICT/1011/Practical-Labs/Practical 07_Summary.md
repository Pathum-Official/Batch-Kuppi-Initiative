# Practical 07 - Control Structures & Logic Building - Summary

## Core Practical Concepts
This lab reinforces decision-making using `if-else` structures. It involves taking inputs and categorizing them into different logical "buckets".

## Practical Questions & How to Code Them Easily

### Q1: Even or Odd
*   **Goal:** Check if a number is even or odd.
*   **How to code:** Use the modulo operator `%`. 
    ```java
    if (number % 2 == 0) { // even } else { // odd }
    ```

### Q3 & Q4: Maximum & Minimum of Numbers
*   **Goal:** Find the max/min from 2 or 3 numbers.
*   **How to code:** You can use `Math.max(a, b)` and `Math.min(a, b)`. For three numbers, nest them: `Math.max(a, Math.max(b, c))`. Alternatively, use `if-else` blocks to compare them manually.

### Q5, Q6, Q7, Q8: Categorization (Temp, BMI, Ads, Grades)
*   **Goal:** Map a number (e.g., Temperature, BMI, Words, Marks) to a specific String/Grade based on a table.
*   **How to code:** This is a classic `if - else if` ladder. Always start from the top or bottom of the range to keep it simple.
    *   *BMI Example:*
        ```java
        double bmi = weight / (heightInMeters * heightInMeters);
        if (bmi < 18.5) {
            System.out.println("Underweight");
        } else if (bmi <= 24.9) {
            System.out.println("Normal");
        } // ... continue for others
        ```
    *   *Marks/Grade Example:*
        ```java
        if (marks >= 75) grade = "A";
        else if (marks >= 65) grade = "B";
        // ... continue
        ```

## Exam Tip
Whenever a question gives you a **table with ranges**, immediately think of an **`if - else if` ladder**. Do not write separate isolated `if` statements, because you want the code to stop checking once it finds the correct range.
