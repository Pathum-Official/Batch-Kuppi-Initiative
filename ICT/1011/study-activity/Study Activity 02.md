# Study Activity 02: Array Processing & Loops

## 📌 The Question (ප්‍රශ්නය)
Write a Java method to find the maximum value in an integer array.

**Requirements:**
1.  Method name must be `findMax`.
2.  Must accept an `int[] numbers` array as a parameter.
3.  Must return the maximum `int` value.

---

## 💻 Your Answer (ඔබේ පිළිතුර)
```java
public static int findMax (int[] numbers){
    int max=numbers[0];
    for (int i=1; i<numbers.length;i++){
        if (max<numbers[i]){
            max=numbers[i];
        }
    }
    return max;
}
```

---

## 💯 Evaluation & Marks (ඇගයීම සහ ලකුණු)
**Marks Awarded:** 10/10 (A+) 🌟

**Instructor's Impression:**
Excellent implementation! You correctly assigned the first element (`numbers[0]`) to the `max` variable and started the loop from index `1`. This is the most optimal way to find a maximum value. Your syntax and logic are perfect.

---

## 🧠 Explanation & Additional Tips (විවරණය සහ උපදෙස්)

### Breakdown of the Logic
1.  **Initialization:** By setting `int max = numbers[0];`, you assume the first item is the biggest. 
2.  **Iteration (Looping):** `for (int i=1; i<numbers.length; i++)` traverses the array starting from the second item (index 1). Using `numbers.length` (without parentheses) is correct for arrays.
3.  **Condition:** `if (max < numbers[i])` checks if the current item is larger than your recorded maximum.
4.  **Update:** If true, `max = numbers[i];` updates the record.

### The A+ Strategy (Edge Cases for Arrays)
What if the array is completely empty? If `numbers` has no elements, `numbers[0]` will cause an **`ArrayIndexOutOfBoundsException`** (fatal error in Java).

To make this code 100% bulletproof for an A+ grade, add a **null check** and a **length check** at the top:
```java
public static int findMax(int[] numbers) {
    // Edge case handling (Guard Clause)
    if (numbers == null || numbers.length == 0) {
        return 0; // Or handle the error appropriately
    }
    
    int max = numbers[0];
    // ... your correct code follows here ...
}
```
**Vocabulary to remember for exams:**
*   `traverse` or `iterate` - looping through an array.
*   `index` - the position of an element in an array.
*   `Array Index Out Of Bounds` - the error when you try to access a position that doesn't exist.