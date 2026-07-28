# 07 Functions I (Methods) - Summary

## 1. What is a Method?
A collection of statements grouped together to perform an operation. Used to define **reusable code** and simplify coding.

## 2. Method Definition (Signature)
A method definition consists of modifiers, a return type, a method name, and parameters.
*   *Syntax:*
    ```java
    public static returnValueType methodName(list of parameters) {
        // Method body
        return value; // (if returnValueType is not void)
    }
    ```
*   **Method Signature:** The method name + parameter list.
*   **Modifiers:** `public` and `static` are commonly used (static means the method belongs to the class itself).
*   **Return Type (`returnValueType`):** The data type the method returns (e.g., `int`, `double`). If the method doesn't return anything, use `void`.

## 3. Parameters vs. Arguments
*   **Formal Parameters:** The variables defined in the method header. They act as placeholders. *(e.g., `int num1, int num2`)*
*   **Actual Parameters (Arguments):** The actual values you pass into the method when invoking it. *(e.g., `max(5, 10)` -> 5 and 10 are arguments).*

## 4. Calling (Invoking) a Method
*   **Value-returning methods:** Usually treated as a value.
    *(e.g., `int larger = max(3, 4);`)*
*   **Void methods:** Called as a standalone statement.
    *(e.g., `System.out.println("Hello");`)*
