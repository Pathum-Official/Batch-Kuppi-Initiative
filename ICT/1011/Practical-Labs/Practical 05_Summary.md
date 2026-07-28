# Practical 05 - Control Structures (If-Else & Switch) - Summary

## Core Practical Concepts
This lab focuses heavily on **multi-way `if-else`** statements and **`switch`** statements. This is the most common exam format for 1st-year programming.

## Practical Questions & How to Code Them Easily

### Q1 & Q2: Salary & Water Bill Calculations
*   **Goal:** Calculate final values after applying various condition-based percentages.
*   **How to code:**
    ```java
    double epf = basicSalary * 0.08;
    double tax = basicSalary * 0.12;
    double netSalary = basicSalary + allowances - (epf + tax + loan);
    ```

### Q3 & Q16: Slab-based Calculations (Electricity Bill & UGC Salary)
*   **Goal:** Calculate a bill where the rate changes based on the range (e.g., 0-30 units, 31-60 units).
*   **How to code:** Use an `if - else if` ladder. **Always check from the smallest range to the largest** (or vice versa systematically).
    ```java
    if (units <= 30) {
        charge = units * 8.00;
    } else if (units <= 60) {
        // First 30 units at 8.00, remaining at 12.00
        charge = (30 * 8.00) + ((units - 30) * 12.00); 
    } else if (units <= 120) {
        charge = (30 * 8.00) + (30 * 12.00) + ((units - 60) * 20.00);
    }
    ```
    *Exam Tip:* Electricity bills are cumulative. You don't just multiply the total units by the slab rate! You must calculate previous slabs fully.

### Q4 & Q5: Calculator & ATM Machine
*   **Goal:** Build a menu-driven application (e.g., 1. Add, 2. Subtract...).
*   **How to code:** Use a `switch` statement based on the user's input choice.
    ```java
    int choice = input.nextInt();
    switch (choice) {
        case 1:
            // do addition
            break;
        case 2:
            // do subtraction
            break;
        default:
            System.out.println("Invalid option");
    }
    ```
