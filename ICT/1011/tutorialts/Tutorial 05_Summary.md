# Tutorial 05 - Strings & Recursion - Summary

## Core Concepts
This tutorial bridges the gap between writing simple functions, manipulating Strings (using built-in methods), and solving problems using Recursion (methods calling themselves).

## Practical Questions & Tricks

### Q1 & Q2: String Manipulation & Iteration
*   **Goal:** Write a method to count vowels in a String.
*   **How to code:**
    1.  *Signature:* `public static int countVowels(String text)`
    2.  *Simplify:* Convert everything to lowercase first so you only have to check 5 letters instead of 10. `text = text.toLowerCase();`
    3.  *Loop:* Use a `for` loop from `0` to `text.length() - 1`.
    4.  *Extract:* Get the character at the current index: `char c = text.charAt(i);`
    5.  *Check & Count:* `if (c == 'a' || c == 'e' || c == 'i' || c == 'o' || c == 'u') count++;`
    6.  *Return:* `return count;`

### Q3 & Q4: Recursion (Sum of Digits)
*   **Goal:** Find the sum of digits of a number (e.g., 123 -> 1+2+3 = 6) using recursion, without any loops.
*   **How to code (The 80/20 Rule for Recursion):**
    Every recursive function MUST have two parts:
    1.  **Base Case:** The condition where it stops.
        *   `if (number == 0) return 0;` (When there are no more digits left, stop).
    2.  **Recursive Step:** The math + calling the function again with a smaller piece of data.
        *   Get the last digit: `number % 10`
        *   Get the rest of the digits: `number / 10`
        *   `return (number % 10) + sumDigits(number / 10);`

### Q4: Calling Methods inside Methods
*   **Goal:** Write a method `isSpecialNumber` that returns `true` if the sum of digits is divisible by 5. You *must* use the method from Q3.
*   **How to code:**
    *   *Signature:* `public static boolean isSpecialNumber(int number)`
    *   *Logic:* Call the `sumDigits` method directly inside the `if` condition.
    *   `int sum = sumDigits(number);`
    *   `return (sum % 5 == 0);` (This is much cleaner than using an `if-else`!).
