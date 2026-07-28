# 08 Functions II (Overloading & Recursion) - Summary

## 1. Method Overloading
Allows you to define multiple methods with the **same name** in the same class, as long as their **parameter lists (signatures) are different** (different number of parameters or different data types).
*   *Example:*
    ```java
    public static int max(int num1, int num2) { ... }
    public static double max(double num1, double num2) { ... }
    ```
    The Java compiler automatically determines which method to call based on the arguments provided.

## 2. Recursion
A recursive method is a method that **invokes (calls) itself**.
*   It must always have a **Base Case** to stop the recursion (otherwise it runs infinitely and causes a stack overflow).
*   *Example (Factorial):*
    ```java
    public static long factorial(int n) {
        if (n == 0) { // Base Case
            return 1;
        } else {
            return n * factorial(n - 1); // Recursive Call
        }
    }
    ```
*   *Common Exam Problems:* Factorial, Fibonacci Series.
