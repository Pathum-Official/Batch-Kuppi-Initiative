# 02 Basic Syntax and Semantics - Summary

## 1. Java Program Structure
*   **Main Method:** A Java program is always executed from the `main` method. The main method is the entry point where the program begins execution.
    ```java
    public class Welcome { 
        public static void main(String[] args) {
            System.out.println("Welcome to Java!");
        }
    }
    ```
*   **Blocks:** Enclosed by `{ }`. Used to group components (classes and methods).
*   **Semicolons (`;`):** Every statement in Java ends with a semicolon.
*   **Case Sensitivity:** Java is strictly case-sensitive (`Area` and `area` are different).

## 2. Comments in Java
Used for documenting the program. Ignored by the compiler.
*   **Line Comment:** `//` (Ignores text on the same line)
*   **Block Comment:** `/* ... */` (Ignores text across multiple lines)

## 3. How Java Works (Compilation & Execution)
*   **Step 1:** Write the source code (`.java` file).
*   **Step 2:** Compile using `javac`. This creates a bytecode file (`.class`). Bytecode is platform-independent.
*   **Step 3:** The JVM (Java Virtual Machine) runs the bytecode.
*   *Note:* JDK (Java Development Kit) provides tools to compile/run. JRE (Java Runtime Environment) provides libraries and JVM to run the app.

## 4. Identifiers & Keywords
*   **Identifiers:** Names given to classes, methods, and variables (e.g., `main`, `number`, `ComputeArea`).
    *   **Rules:** Must consist of letters, digits, or `_`. Cannot start with a digit. Cannot be a keyword, `true`, `false`, or `null`.
*   **Keywords (Reserved Words):** Have specific meaning in Java (`public`, `static`, `void`, `int`, `class`, `if`, `return`). You cannot use them as identifiers.

## 5. Variables & Data Types
Variables store data that can change. Must be declared with a specific data type before use.
*   `datatype variableName;` (e.g., `int count = 1;`)

### Primitive Data Types
Store actual values. Fixed memory sizes.
*   **Integer Types:**
    *   `byte` (1 byte)
    *   `short` (2 bytes)
    *   `int` (4 bytes, default choice)
    *   `long` (8 bytes, must end with `L`)
*   **Floating-Point Types:**
    *   `float` (4 bytes, less precision, must end with `f`)
    *   `double` (8 bytes, high precision, default choice)
*   **Other Primitives:**
    *   `char` (2 bytes, uses single quotes e.g., `'A'`)
    *   `boolean` (1 byte, only `true` or `false`)

### Non-Primitive Data Types
Store memory references. Come from Java library or custom classes. Have built-in methods.
*   *Example:* `String name = "Kamal";` (String uses double quotes)

## 6. Console Input & Output
*   **Output:** `System.out.println("Text");`
*   **Input:** Java uses the `Scanner` class to read input. It must be imported.
    ```java
    import java.util.Scanner; // Import Scanner
    
    // Create Scanner object
    Scanner input = new Scanner(System.in); 
    
    // Read an integer
    int number = input.nextInt(); 
    ```
    *Types of Imports:* Specific import (`import java.util.Scanner;`) vs. Wildcard import (`import java.util.*;`).
