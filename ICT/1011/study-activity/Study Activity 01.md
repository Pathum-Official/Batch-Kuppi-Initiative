# Study Activity 01: Multi-way If-Else (Categorization)

## 📌 The Question (ප්‍රශ්නය)

Write a Java method that takes a student's marks and returns the grade based on the following table:

* 75 to 100 -> "A"
* 65 to 74 -> "B"
* 50 to 64 -> "C"
* Below 50 -> "F"

**Requirements:**

1. Method name must be `getGrade`.
2. Must accept an `int marks` parameter.
3. Must return a `String`.

---

## 💻 Your Answer (ඔබේ පිළිතුර)

```java
public static String getGrade(int marks){
    if (marks >= 75){
        return "A";
    }
    else if (marks >=65){
        return "B";
    }
    else if (marks>=50){
        return "C";
    }
    else{
        return "F";
    }
}
```

---

## 💯 Evaluation & Marks (ඇගයීම සහ ලකුණු)

**Marks Awarded:** 10/10 (A+) 🌟

**Instructor's Impression:**
Your logic is flawless. You correctly utilized the `if - else if` ladder. More importantly, you correctly checked the conditions in **descending order** (highest to lowest), which is the standard best practice for range checking in programming.

---

## 🧠 Explanation & Additional Tips (විවරණය සහ උපදෙස්)

### Why is your code correct?

When you use `else if`, Java stops checking conditions as soon as it finds the first `true` statement.
Because you checked `>= 75` first, if a student gets `80`, it returns "A" and exits immediately. It does not even look at `>= 65`. This is highly efficient (**optimized execution**).

### The A+ Strategy (Edge Cases)

You asked a brilliant question: *"Should I handle invalid inputs like marks > 100 or marks < 0?"*
In an exam, if it's not explicitly asked, it is not mandatory. **However**, adding **Input Validation** (දත්ත පරීක්ෂා කිරීම) shows the examiner that you think like a real Software Engineer.

If you have 10 extra seconds in the exam, add a **guard clause** at the very top:

```java
public static String getGrade(int marks){
    // Input Validation (Guard Clause)
    if (marks > 100 || marks < 0) {
        return "Invalid Marks";
    }
  
    // ... your correct code follows here ...
}
```

This simple addition guarantees an A+ impression. Always keep **Edge Cases** in mind!
