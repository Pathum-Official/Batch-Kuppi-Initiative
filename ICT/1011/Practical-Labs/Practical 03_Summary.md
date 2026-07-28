# Practical 03 - User Input & Math Operations - Summary

## Core Practical Concepts
This lab introduces reading dynamic input from the keyboard using the `Scanner` class and performing mathematical calculations.

## Key Setup
To read inputs, you must always import and initialize the `Scanner`:
```java
import java.util.Scanner;
// Inside main method:
Scanner input = new Scanner(System.in);
```

## Practical Questions & How to Code Them Easily

### Q1 & Q2: Read Details and Calculate Average
*   **Goal:** Read details (name, age, marks) and calculate Total and Average.
*   **How to code:** 
    *   Use `input.nextLine()` for String (Name).
    *   Use `input.nextInt()` for int (Age, Marks).
    *   *Calculation:* `int total = mark1 + mark2 + mark3; double avg = total / 3.0;` (Use `3.0` to force double division!).

### Q3: Invoice Calculation with VAT & NBT
*   **Goal:** Calculate Amount = Price * Qty. Add 12% VAT and 2% NBT.
*   **How to code:**
    *   `double amount = price * qty;`
    *   `double vat = amount * 0.12;`
    *   `double nbt = amount * 0.02;`
    *   `double netAmount = amount + vat + nbt;`

### Q4: Minimum Bank Notes in ATM
*   **Goal:** Find how many 5000, 1000, 500, 100 notes are needed for an amount (e.g. 1234500).
*   **How to code:** Use Division (`/`) for the count, and Modulo (`%`) for the remainder.
    ```java
    int count5000 = amount / 5000;
    amount = amount % 5000; // Remaining amount
    int count1000 = amount / 1000;
    // ... repeat for others
    ```

### Q7: Celsius to Fahrenheit
*   **Goal:** `F = (5/9) * C + 32`
*   **How to code:** **CRITICAL:** Do NOT write `5/9` in Java, it will result in `0` (integer division). Write `5.0 / 9.0` instead!
    `double f = (5.0 / 9.0) * c + 32;`

### Q9: Trigonometry (Sine, Cosine)
*   **Goal:** Calculate Math formulas for a given angle in degrees.
*   **How to code:** 
    1. Convert degrees to radians: `double radians = Math.toRadians(degrees);`
    2. Use `Math.sin(radians)`, `Math.cos(radians)`, `Math.tan(radians)`.

### Q10: Triangle Area (Heron's Formula)
*   **Goal:** `s = (a+b+c)/2`, Area = `sqrt(s(s-a)(s-b)(s-c))`
*   **How to code:** Use `Math.sqrt(...)` for the square root.

### Q11: Hide Password Input
*   **Goal:** Read a password securely without showing the characters on screen.
*   **How to code:** Use the `Console` class instead of `Scanner`.
    ```java
    java.io.Console console = System.console();
    char[] passwordArray = console.readPassword("Enter password: ");
    String password = new String(passwordArray);
    ```
