# 09 Arrays - Summary

## 1. Basics of Arrays
Used to store a bulk collection of data of the same type. Array sizes are fixed once created.
*   **Declaring & Creating:**
    `elementType[] arrayRefVar = new elementType[arraySize];`
    *(e.g., `double[] myList = new double[10];`)*
*   **Array Size:** Can be obtained using `arrayName.length`. *(e.g., `myList.length`)*. Default values are `0` (numbers) or `false` (booleans).
*   **Accessing Elements:** Uses 0-based indexing `[0, 1, ..., length-1]`.
    *(e.g., `myList[2] = myList[0] + myList[1];`)*
*   **Array Initializer (Shortcut):**
    `double[] myList = {1.9, 2.9, 3.4, 3.5};`

## 2. Processing Arrays
Usually done with `for` loops because all elements are the same type and the array size is known.
*   *Common Operations:* Finding the sum of elements, finding the maximum/minimum value, shifting elements, shuffling randomly.

## 3. Passing Arrays to Methods
*   Java uses **Pass-by-Value** for arguments. 
*   However, for arrays, the *value* passed is the **reference (memory address)** of the array. This acts like *pass-by-sharing*. 
*   **Crucial Exam Concept:** If you modify an array inside a method, the changes **will reflect outside** the method!

## 4. Multi-Dimensional Arrays
An array of arrays. Often used to represent tables or matrices (rows and columns).
*   **Declaration:** `int[][] matrix = new int[5][5];`
*   **Accessing:** `matrix[row][column]` *(e.g., `matrix[2][1] = 7;`)*
*   **Processing:** Usually processed using **Nested for-loops** (one loop for rows, another inside for columns).
