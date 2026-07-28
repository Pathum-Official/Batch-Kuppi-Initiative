# Lab 01 - Basics & Environment Setup - Summary

## Core Practical Concepts
This lab focuses on setting up the Java environment, compiling, running, and understanding the basic structure of a Java program.

## Key Commands (Windows Command Prompt)
*   **Compile a Java file:** `javac HelloWorld.java` (This creates a `HelloWorld.class` file containing bytecode).
*   **Run a Java program:** `java HelloWorld` (Do not include `.class` at the end).

## Practical Questions & How to Code Them Easily

### Q1-Q4: Compiling and fixing syntax errors
*   **Goal:** Write a basic `HelloWorld` class and fix case-sensitivity errors (like `system.out` instead of `System.out` or `Public class` instead of `public class`).
*   **How to code:** Always remember Java is strictly case-sensitive. `public`, `static`, `void`, `class` must be all lowercase. `String` and `System` must start with a capital letter.

### Q5: Print details in separate lines
*   **Goal:** Print your index number, name, DOB, age, and address in different lines.
*   **How to code:** Use `System.out.println("Text");` multiple times. Every `println` automatically moves the cursor to the next line.

### Q6-Q7: Command Line Arguments (`args`)
*   **Goal:** Read inputs directly from the command line when running the program (e.g., `java ArgTest Sri Jayewardenepura`).
*   **How to code:** Use the `String[] args` array inside the main method.
    *   `args[0]` = "Sri"
    *   `args[1]` = "Jayewardenepura"
    *   *Code:* `System.out.println("First name: " + args[1]);`
