# Practical 09 - Arrays & Character Manipulation - Summary

## Core Practical Concepts
This lab focuses on **Array Operations** (sorting, merging, searching) and **String/Character Array Manipulations** (palindromes, encryption, language translation).

## Practical Questions & How to Code Them Easily

### 1. Basic Array Operations (Q1-Q4, Q8-Q10)
*   **Reverse Order (Q2):** Loop backwards: `for(int i = arr.length - 1; i >= 0; i--)`
*   **Sum/Max/Min (Q3, Q9):** Set `max = arr[0]`, loop through array, `if(arr[i] > max) max = arr[i]`.
*   **Copy Arrays (Q4):** `int[] arr2 = new int[arr1.length]; for(int i=0; i<arr1.length; i++) arr2[i] = arr1[i];`
*   **Separate Odd/Even (Q10):** Loop through the main array, check `if (arr[i] % 2 == 0)` put it in `evenArray`, else in `oddArray`.

### 2. Advanced Array Operations (Q5, Q6, Q7, Q11, Q12)
*   **Sorting (Q6):** Use Bubble Sort or Selection Sort logic (nested loops swapping elements). Or simply use `java.util.Arrays.sort(arr);` if allowed.
*   **Merge & Sort (Q7):** Create a new array of size `arr1.length + arr2.length`, copy both into it, then sort descending.
*   **Delete/Insert (Q11, Q12):** Arrays are fixed size! You must create a *new* array, copy the elements over, skipping the deleted index (or shifting elements for insertion).

### 3. Character Arrays & Strings (Q14-Q19)
*   **Palindrome (Q15):** Check if string is the same forwards and backwards. Loop from $0$ to $length/2$, checking `if(str[i] != str[length - 1 - i])`.
*   **Reverse In-Place (Q16):** Swap the first character with the last, second with second-to-last, etc., until the middle.
*   **Encryption / Shift Cipher (Q18):** Add the key to the character. `char encrypted = (char) (arr[i] + key);`. Ensure it wraps around 'Z' to 'A' using modulo arithmetic.
*   **Cow Latin Translation (Q19):** 
    1.  Check first letter (vowel or consonant).
    2.  If consonant: move to end, append "oo".
    3.  If vowel: append "moo".
    4.  *Tip:* Use `String.substring()` and `String.charAt()` to slice and build the new words easily.

## Exam Tip
Array manipulation requires strict index management to avoid `ArrayIndexOutOfBoundsException`. Remember array bounds are strictly `0` to `length - 1`.
