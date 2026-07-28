# Lab 02 - Printing & Formatting - Summary

## Core Practical Concepts
This lab tests your ability to format output neatly on the console using Java's print statements.

## Key Methods
*   `System.out.println("text");` -> Prints text and moves to the next line.
*   `System.out.print("text");` -> Prints text but stays on the same line.
*   `System.out.printf();` -> (Optional but useful for invoices) Used for formatting strings and numbers.

## Practical Questions & How to Code Them Easily

### Q1: Print a simple greeting
*   **Goal:** Print "Hello Freshers - Welcome to JAVA Programming"
*   **How to code:** Simply wrap the text in a `System.out.println()`.

### Q2: Print a formatted Invoice
*   **Goal:** Print an invoice with aligned columns (Item Code, Description, Unit Price, Quantity, Net Amount).
*   **How to code:** Use multiple `System.out.println()` statements. Use spaces or the Tab escape sequence (`\t`) to align the colons (`:`) and equal signs (`=`).
    ```java
    System.out.println("Item Code\t: INV0010");
    System.out.println("Description\t: Smart TV 55\"");
    ```

### Q3 & Q4: Print Patterns and ASCII Art
*   **Goal:** Print shapes using `#` and ASCII art (like a face or car).
*   **How to code:** Just copy the exact pattern inside `System.out.println()`. 
    *   **Crucial Tip:** If the ASCII art contains a double quote (`"`), you must escape it using a backslash (`\"`) so Java doesn't think the string ended. Same for backslashes (`\\`).

### Q5 & Q6: Formatted Invoices and Bar Charts
*   **Goal:** Print a neat invoice and a text-based bar chart.
*   **How to code:** Again, heavily relies on manual alignment using spaces, `\t` (tab), and `\n` (new line) inside `System.out.println()`.
