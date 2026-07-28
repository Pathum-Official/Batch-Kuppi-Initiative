# Study Activity 03: String Manipulation (Text Processing)

## 📌 The Question (ප්‍රශ්නය)

Write a Java method to count how many times a specific letter appears in a given String.

**Requirements:**

1. **Method Name:** `countOccurrences`
2. **Parameters:** `String text` AND `char letter`.
3. **Return Type:** `int`.

---

## 💻 Your Answer (ඔබේ පිළිතුර)

```java
public static int countOccurrences(String text;char letter){

    int count = 0;

    for (int i=0;i<text.length;i++){
        if (text.charAt(i)==letter){
            count++;
        }
    }
   return count;
}
```

---

## 💯 Evaluation & Marks (ඇගයීම සහ ලකුණු)

**Marks Awarded:** 8/10 (A-) 👍

**Instructor's Impression:**
ඔබේ Logic එක (for-loop එක සහ `charAt` භාවිත කළ ආකාරය) 100% ක් නිවැරදියි! ඔබ ප්‍රශ්නය හරියටම තේරුම් අරගෙන තියෙනවා. නමුත් කේතයේ කුඩා **Syntax Errors (ව්‍යාකරණ දෝෂ) 2ක්** තියෙනවා. මේවා විභාගයේදී Examiners ලා ගොඩක්ම බලන (අඩුපාඩු හොයන) තැන්. අපි ඒවා හදාගමු!

---

## 🧠 Explanation & Additional Tips (විවරණය සහ උපදෙස්)

### Error 01: Parameter Separator (මායිම් කිරීම)

ඔබ ලියා ඇත්තේ: `(String text;char letter)`
**නිවැරදි විය යුත්තේ:** `(String text, char letter)`

* *Rule:* Parameters දෙකක් වෙන් කරන්නේ **කොමාවකින් (comma `,`)** මිසක් සෙමිකෝලන් (`;`) එකකින් නෙවෙයි.

### Error 02: Array Length vs. String Length (ගොඩක් අයට වරදින තැනක්!)

ඔබ ලියා ඇත්තේ: `text.length`
**නිවැරදි විය යුත්තේ:** `text.length()`

* *Rule:*
  * **Array (අරා)** වල දිග හොයන්න පාවිච්චි කරන්නේ **`array.length`** (වරහන් නැහැ).
  * **String (වචන)** වල දිග හොයන්න පාවිච්චි කරන්නේ **`string.length()`** (මෙය method එකක් නිසා අනිවාර්යයෙන්ම වරහන් `()` තිබිය යුතුයි). විභාගයේදී මේක පටලවගන්න එපා!

### The A+ Version (නිවැරදි කරන ලද කේතය සහ Edge Cases):

Here is the perfect, 100% bug-free version containing a Guard Clause:

```java
public static int countOccurrences(String text, char letter) {
    // Edge case handling (Guard Clause)
    if (text == null || text.length() == 0) {
        return 0; // If string is empty or null, count is 0
    }
  
    int count = 0;
    // Remember the brackets for text.length() !
    for (int i = 0; i < text.length(); i++) {
        if (text.charAt(i) == letter) {
            count++;
        }
    }
    return count;
}
```

**Vocabulary for Exams:**

* `Syntax Error` - වැරදි අක්ෂර/සංකේත භාවිතය (Compile වෙන්නේ නැහැ).
* `Logical Error` - කේතය වැඩ කරනවා, නමුත් එන උත්තරය වැරදියි.
