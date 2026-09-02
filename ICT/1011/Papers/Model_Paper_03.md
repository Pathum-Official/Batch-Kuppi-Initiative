# 🎓 ICT 1011 - Computer Programming
## University Final Examination (Model Paper 03)
**Duration: 1 Hour | Number of Questions: 03 | Closed Book**

> **Instructions to Candidates:**
> * Answer ALL three (03) questions.
> * Write your Java code clearly. Syntax errors will be penalized.
> * This paper tests your knowledge on standard libraries (`Math`), output formatting (`printf`), and exit-controlled loops.

---

### ❓ Question 01 (35 Marks) - Math Library & Output Formatting
A scientific research team needs a program to calculate the Area and Circumference of a circle and print the results in a highly formatted table.

**Part (A) [15 Marks]**
Write a Java program that reads the `radius` (as a `double`) from the user. Using the `Math` library, calculate:
1. Area = π × radius² *(Use `Math.PI` and `Math.pow`)*
2. Circumference = 2 × π × radius

**Part (B) [20 Marks]**
Using `System.out.printf()`, print the results in the exact format shown below. Ensure that both calculated values are rounded to exactly **two decimal places** and are left-aligned in a column of width 15.

*Expected Output Format:*
```text
Enter radius: 5.0
-----------------------------
Property       | Value
-----------------------------
Area           | 78.54
Circumference  | 31.42
-----------------------------
```

---

### ❓ Question 02 (30 Marks) - Do-While Loop & Input Validation
Most programs require continuous input until the user decides to quit. 

**Part (A) [20 Marks]**
Write a complete Java program using a `do-while` loop that continuously asks the user to enter a positive integer. 
* If the user enters a positive integer, the program should print the square root of that number (using `Math.sqrt`).
* If the user enters `0` or a negative number, the loop must terminate (exit) and print "Program Ended.".

**Part (B) [10 Marks]**
Explain briefly in one or two sentences why a `do-while` loop is more suitable for this specific task than a standard `while` loop.

---

### ❓ Question 03 (35 Marks) - Array Search & String Manipulation
A teacher has stored the names of 5 students in a String array.

```java
String[] students = {"Amal", "Kamal", "Nimal", "Sunil", "Bimal"};
```

**Part (A) [20 Marks]**
Write a Java program that asks the user to input a name to search for. Use a `for` loop to iterate through the `students` array. If the name is found, print "Student Found at Index: [index]". If the name is not in the array, print "Student Not Found".
*(Hint: Use a boolean flag variable to keep track of whether the student was found).*

**Part (B) [15 Marks]**
Rewrite the search condition in Part (A) so that it ignores the case of the letters (e.g., if the user types "amal" or "AMAL", it should still successfully find "Amal" in the array). 
*(Hint: Use the `equalsIgnoreCase()` method available for Strings).*

---
---

# ✅ Model Paper 03 - Marking Scheme & Answers

### Answer 01
**Part (A) & (B) - Math Library & Printf Formatting [35 Marks]**
```java
import java.util.Scanner;

public class CircleCalculations {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter radius: ");
        double radius = scanner.nextDouble();
        
        // Part A: Calculations
        double area = Math.PI * Math.pow(radius, 2);
        double circumference = 2 * Math.PI * radius;
        
        // Part B: Formatting
        System.out.println("-----------------------------");
        System.out.printf("%-15s | %s \n", "Property", "Value");
        System.out.println("-----------------------------");
        
        // %-15s means Left-aligned string with 15 spaces
        // %.2f means float/double rounded to 2 decimal places
        System.out.printf("%-15s | %.2f \n", "Area", area);
        System.out.printf("%-15s | %.2f \n", "Circumference", circumference);
        
        System.out.println("-----------------------------");
        scanner.close();
    }
}
```
*(Marks allocation: Scanner & Input - 5 marks, Math.PI & Math.pow - 10 marks, Printf syntax - 10 marks, Precision `.2f` - 5 marks, Alignment `%-15s` - 5 marks)*

---

### Answer 02
**Part (A) - Do-While Loop [20 Marks]**
```java
import java.util.Scanner;

public class NumberProcessor {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        int number; // Declare outside the loop to use in 'while' condition
        
        do {
            System.out.print("Enter a positive integer (0 or negative to quit): ");
            number = input.nextInt();
            
            if (number > 0) {
                System.out.println("Square Root: " + Math.sqrt(number));
            }
            
        } while (number > 0);
        
        System.out.println("Program Ended.");
        input.close();
    }
}
```
*(Marks allocation: Variable declaration outside loop - 4 marks, do-while syntax - 6 marks, Math.sqrt usage - 5 marks, Correct while condition - 5 marks)*

**Part (B) - Theory [10 Marks]**
A `do-while` loop is an exit-controlled loop, which guarantees that the code inside the loop executes at least once. This is perfect for menu-driven programs or input validation where we must ask the user for input at least one time before checking the termination condition.

---

### Answer 03
**Part (A) - Array Search with Flag [20 Marks]**
```java
import java.util.Scanner;

public class StudentSearch {
    public static void main(String[] args) {
        String[] students = {"Amal", "Kamal", "Nimal", "Sunil", "Bimal"};
        Scanner input = new Scanner(System.in);
        
        System.out.print("Enter student name to search: ");
        String searchName = input.next(); // or nextLine()
        
        boolean isFound = false; // Flag variable
        
        for (int i = 0; i < students.length; i++) {
            // Using .equals() for String comparison, NOT ==
            if (students[i].equals(searchName)) {
                System.out.println("Student Found at Index: " + i);
                isFound = true;
                break; // Stop searching once found
            }
        }
        
        if (!isFound) { // if isFound == false
            System.out.println("Student Not Found");
        }
        input.close();
    }
}
```
*(Marks allocation: Flag variable logic - 5 marks, Loop limits - 5 marks, .equals() usage - 5 marks, If condition for Not Found - 5 marks)*

**Part (B) - Case Insensitive Search [15 Marks]**
```java
// Rewrite the condition inside the loop:
if (students[i].equalsIgnoreCase(searchName)) {
    System.out.println("Student Found at Index: " + i);
    isFound = true;
    break;
}
```
*(Marks allocation: Correct usage of `.equalsIgnoreCase()` instead of `.equals()` - 15 marks)*
