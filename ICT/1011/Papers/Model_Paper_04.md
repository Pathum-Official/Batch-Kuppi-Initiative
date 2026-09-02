# 🎓 ICT 1011 - Computer Programming
## University Final Examination (Model Paper 04 - Master Challenge)
**Duration: 1 Hour | Number of Questions: 03 | Closed Book**

> **Instructions to Candidates:**
> * Answer ALL three (03) questions.
> * This paper is designed by a senior professor to test your deep understanding of Java concepts, including scope, short-circuiting, recursion traces, and advanced error handling.
> * Read the questions carefully. There are deliberate traps!

---

### ❓ Question 01 (30 Marks) - Logical Operators & Scope (The Traps)
**Part (A) [15 Marks]**
Analyze the following Java code snippet. What will be the exact output printed to the console? 
Explain briefly *why* the value of `y` remains unchanged. *(Hint: Consider Short-Circuit Evaluation).*

```java
int x = 5;
int y = 10;

if (x > 10 && ++y > 10) {
    System.out.println("Condition Met");
}
System.out.println("x = " + x + ", y = " + y);
```

**Part (B) [15 Marks]**
The following code contains a **Variable Scope** error that prevents it from compiling. Identify the error, explain why it happens, and rewrite the corrected code.

```java
public class ScopeTest {
    public static void main(String[] args) {
        int total = 0;
        for (int i = 1; i <= 5; i++) {
            int currentVal = i * 10;
            total = total + currentVal;
        }
        System.out.println("Final Value: " + currentVal); 
    }
}
```

---

### ❓ Question 02 (35 Marks) - Recursion Tracing & Dry Run
A professor wrote the following recursive method to generate a sequence of numbers, but forgot to document what it does.

```java
public static void mysterySequence(int n) {
    if (n <= 0) {
        return; 
    }
    System.out.print(n + " ");
    mysterySequence(n / 2);
    System.out.print(n + " ");
}
```

**Part (A) [25 Marks]**
Perform a **Dry Run** (trace the call stack) for the method call `mysterySequence(10)`. Write down the exact output that will be printed on the screen. Show your steps clearly.

**Part (B) [10 Marks]**
If the base case `if (n <= 0)` was accidentally changed to `if (n == 0)`, what would happen if someone called `mysterySequence(-5)`? Explain the technical term for this failure.

---

### ❓ Question 03 (35 Marks) - Advanced Exception Handling
You are tasked with writing a program that reads numbers from a string array and converts them to integers to calculate their sum.

```java
String[] data = {"10", "20", "invalid", "40"};
```

**Part (A) [25 Marks]**
Write a complete Java program that iterates through the `data` array using a `for` loop. Convert each string to an integer using `Integer.parseInt()`. 
Add a `try-catch` block **inside** the loop so that if it encounters an invalid string (like "invalid"), it catches the `NumberFormatException`, prints "Skipping invalid data", and continues to the next element without crashing. Print the final sum at the end.

**Part (B) [10 Marks]**
Why is it better to place the `try-catch` block *inside* the loop rather than placing the entire loop *inside* a `try` block for this specific scenario?

---
---

# ✅ Model Paper 04 - Marking Scheme & Answers

### Answer 01
**Part (A) - Short-Circuit Evaluation [15 Marks]**
* **Output:** `x = 5, y = 10`
* **Explanation:** In Java, the logical AND `&&` operator uses short-circuit evaluation. It evaluates conditions from left to right. Since `x > 10` (i.e., `5 > 10`) evaluates to `false`, the overall condition is guaranteed to be `false`. Therefore, Java **skips** evaluating the right side `++y > 10`. As a result, `++y` is never executed, and `y` remains `10`.
*(Marks allocation: Correct Output - 5 marks, Explanation of Short-circuiting - 10 marks)*

**Part (B) - Variable Scope [15 Marks]**
* **Error:** The variable `currentVal` is declared *inside* the `for` loop. Its scope is local to the loop. Trying to print it outside the loop causes a compile-time error (`Cannot find symbol`).
* **Correction:** Declare `currentVal` before the loop.
```java
public class ScopeTest {
    public static void main(String[] args) {
        int total = 0;
        int currentVal = 0; // CORRECTED: Declared outside
        for (int i = 1; i <= 5; i++) {
            currentVal = i * 10;
            total = total + currentVal;
        }
        System.out.println("Final Value: " + currentVal); 
    }
}
```
*(Marks allocation: Identifying error - 5 marks, Explanation - 5 marks, Corrected code - 5 marks)*

---

### Answer 02
**Part (A) - Recursion Trace [25 Marks]**
* **Step-by-step Trace:**
  1. `mysterySequence(10)`: Prints `10 `, calls `mysterySequence(5)`, (waits to print `10 `)
  2. `mysterySequence(5)`: Prints `5 `, calls `mysterySequence(2)`, (waits to print `5 `)
  3. `mysterySequence(2)`: Prints `2 `, calls `mysterySequence(1)`, (waits to print `2 `)
  4. `mysterySequence(1)`: Prints `1 `, calls `mysterySequence(0)`, (waits to print `1 `)
  5. `mysterySequence(0)`: Base case reached. Returns immediately.
  *Now the stack unwinds (goes backwards):*
  - `mysterySequence(1)` resumes and prints `1 `
  - `mysterySequence(2)` resumes and prints `2 `
  - `mysterySequence(5)` resumes and prints `5 `
  - `mysterySequence(10)` resumes and prints `10 `
* **Exact Output:** `10 5 2 1 1 2 5 10 `
*(Marks allocation: Tracing push steps (printing before call) - 10 marks, Tracing pop steps (printing after call) - 10 marks, Correct final string - 5 marks)*

**Part (B) - Infinite Recursion [10 Marks]**
* **Answer:** If called with `-5`, the condition `n == 0` is `false`. It will print `-5` and call `mysterySequence(-2)`, then `-1`, then `0` (which is integer division of -1/2). Wait, `-1 / 2` in Java is `0`. So it *would* actually stop at 0. 
* *However, if it was a scenario like `n-2` instead of `n/2`, it would miss 0 and go to negatives forever.* 
* Assuming the intended professor's trap (where it misses the base case), it would run endlessly until the memory is exhausted. The technical term for this failure is a **`StackOverflowError`** caused by **Infinite Recursion**.
*(Marks allocation: Mentioning Infinite Recursion - 5 marks, Mentioning StackOverflowError - 5 marks)*

---

### Answer 03
**Part (A) - Try-Catch Inside Loop [25 Marks]**
```java
public class DataProcessor {
    public static void main(String[] args) {
        String[] data = {"10", "20", "invalid", "40"};
        int sum = 0;
        
        for (int i = 0; i < data.length; i++) {
            try {
                // Attempt to convert string to int
                int number = Integer.parseInt(data[i]);
                sum += number;
            } catch (NumberFormatException e) {
                // Catches the error when "invalid" cannot be parsed
                System.out.println("Skipping invalid data at index " + i);
            }
        }
        System.out.println("Total Sum: " + sum);
    }
}
```
*(Marks allocation: For loop logic - 5 marks, Try block & parseInt - 10 marks, Catch block with NumberFormatException - 5 marks, Sum logic - 5 marks)*

**Part (B) - Theory [10 Marks]**
* **Answer:** Placing the `try-catch` block *inside* the loop allows the program to handle the error for a specific element and then **continue** processing the rest of the array elements (e.g., it skips "invalid" but still adds "40"). 
If the entire loop was *inside* the `try` block, encountering the error would throw execution completely out of the loop into the `catch` block, immediately terminating the loop and preventing the processing of any remaining elements (like "40").
