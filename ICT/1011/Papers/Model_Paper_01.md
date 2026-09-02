"??">?

# /🎓 ICT 1011 - Computer Programming

## University Final Examination (Model Paper 01)

**Duration: 1 Hour | Number of Questions: 03 | Closed Book**

> **Instructions to Candidates:**
>
> * Answer ALL three (03) questions.
> * Write your Java code clearly. Syntax errors will be penalized.
> * Assume all necessary standard libraries (e.g., `java.util.Scanner`) are imported unless otherwise specified.

---

### ❓ Question 01 (35 Marks) - Fundamentals & Control Structures

A local university uses a grading system to assign letter grades based on student marks. The grading criteria are as follows:

* 80 to 100 : Grade A
* 60 to 79  : Grade B
* 40 to 59  : Grade C
* Below 40  : Fail (F)

**Part (A) [15 Marks]**
Write a pseudocode to read a student's mark from the user, determine the corresponding grade based on the criteria above, and print the grade. If the user enters a mark less than 0 or greater than 100, the system must print "Invalid Mark".

**Part (B) [20 Marks]**
Write a complete Java program (including the `main` method and `Scanner`) that implements the exact logic of the pseudocode from Part A.

---

### ❓ Question 02 (35 Marks) - Methods & Overloading

The mathematics department requires a utility class to calculate the volume of different 3D shapes.

**Part (A) [15 Marks]**
Write a Java method named `calculateVolume` that accepts a single `double` parameter representing the length of a side of a cube, and returns the volume of the cube (Volume = side × side × side).

**Part (B) [20 Marks]**
Demonstrate Method Overloading by writing another method with the exact same name `calculateVolume`. This second method should calculate the volume of a Cylinder. It must accept two `double` parameters: `radius` and `height`.
*(Formula for Cylinder Volume = π × radius² × height. Use `Math.PI` for the value of π).*

---

### ❓ Question 03 (30 Marks) - Arrays & Loops

You are given a 1D integer array containing the daily temperatures (in Celsius) of a city recorded over a week (7 days).

```java
int[] temperatures = {28, 31, 29, 35, 26, 33, 30};
```

**Part (A) [15 Marks]**
Write a Java code snippet (using a `for` loop) that iterates through the given `temperatures` array and calculates the **Average Temperature** for the week. Print the average temperature to the console.

**Part (B) [15 Marks]**
Write another Java code snippet (using a `while` loop) to find and print the **Highest Temperature** recorded during the week.
*(Hint: Initialize a variable `max` with the first element of the array before starting the loop).*

---

---

# ✅ Model Paper 01 - Marking Scheme & Answers

### Answer 01

**Part (A) - Pseudocode [15 Marks]**

```text
BEGIN
    DECLARE mark AS INTEGER
    PRINT "Enter your mark:"
    INPUT mark
  
    IF mark < 0 OR mark > 100 THEN
        PRINT "Invalid Mark"
    ELSE IF mark >= 80 THEN
        PRINT "Grade A"
    ELSE IF mark >= 60 THEN
        PRINT "Grade B"
    ELSE IF mark >= 40 THEN
        PRINT "Grade C"
    ELSE
        PRINT "Fail (F)"
    END IF
END
```

*(Marks allocation: Variables/Input - 3 marks, Validations - 4 marks, If-else logic - 8 marks)*

**Part (B) - Java Code [20 Marks]**

```java
import java.util.Scanner;

public class GradingSystem {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Enter your mark: ");
        int mark = input.nextInt();
      
        if (mark < 0 || mark > 100) {
            System.out.println("Invalid Mark");
        } else if (mark >= 80) {
            System.out.println("Grade A");
        } else if (mark >= 60) {
            System.out.println("Grade B");
        } else if (mark >= 40) {
            System.out.println("Grade C");
        } else {
            System.out.println("Fail (F)");
        }
      
        input.close();
    }
}
```

*(Marks allocation: Scanner usage - 5 marks, Correct Syntax - 5 marks, If-else Logic - 10 marks)*

---

### Answer 02

**Part (A) - Cube Volume [15 Marks]**

```java
public static double calculateVolume(double side) {
    return side * side * side;
}
```

*(Marks allocation: Correct method signature - 5 marks, Correct calculation/return - 10 marks)*

**Part (B) - Cylinder Volume (Overloading) [20 Marks]**

```java
public static double calculateVolume(double radius, double height) {
    return Math.PI * radius * radius * height;
    // OR return Math.PI * Math.pow(radius, 2) * height;
}
```

*(Marks allocation: Correct method signature (same name, different params) - 10 marks, Correct calculation - 10 marks)*

---

### Answer 03

**Part (A) - Average Temperature (For Loop) [15 Marks]**

```java
int[] temperatures = {28, 31, 29, 35, 26, 33, 30};
double sum = 0; // Using double to get accurate decimal average

for (int i = 0; i < temperatures.length; i++) {
    sum = sum + temperatures[i];
}

double average = sum / temperatures.length;
System.out.println("Average Temperature: " + average);
```

*(Marks allocation: Variable initialization - 2 marks, Correct loop bounds (`< temperatures.length`) - 5 marks, Sum calculation - 5 marks, Average logic - 3 marks)*

**Part (B) - Highest Temperature (While Loop) [15 Marks]**

```java
int[] temperatures = {28, 31, 29, 35, 26, 33, 30};
int max = temperatures[0];
int i = 1; // Start from index 1 since max is already index 0

while (i < temperatures.length) {
    if (temperatures[i] > max) {
        max = temperatures[i];
    }
    i++; // 🚨 Crucial: Update statement to prevent infinite loop
}
System.out.println("Highest Temperature: " + max);
```

*(Marks allocation: Initializing max - 3 marks, While loop logic - 5 marks, If condition - 5 marks, Increment `i++` - 2 marks)*
