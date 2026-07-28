# Study Activity 05: While Loops & Digit Extraction (සංඛ්‍යා වෙන් කිරීම)

## 📌 The Question (ප්‍රශ්නය)

ඔබට ලබා දෙන ඕනෑම පූර්ණ සංඛ්‍යාවක (integer) ඇති ඉලක්කම් වල එකතුව (Sum of digits) සොයන Java method එකක් ලියන්න. මේ සඳහා **`while` loop** එකක් භාවිත කිරීම අනිවාර්ය වේ.

**Requirements:**
1. **Method Name:** `sumOfDigits`
2. **Parameters:** `int number`
3. **Return Type:** `int`
4. **Condition:** You MUST use a `while` loop.

---

## 💻 Your Answer (ඔබේ පිළිතුර)

```java
public static int sumOfDigits (int number){
    int sum = 0;
    while(number > 0){
        sum += number % 10;
        number /= 10;
    }
    return sum;
}
```

---

## 💯 Evaluation & Marks (ඇගයීම සහ ලකුණු)

**Marks Awarded:** 9/10 (A) 👏

**Instructor's Impression:**
ඔබේ ලොජික් (Logic) එක ඉතාමත් නිවැරදියි! ඔබ `% 10` භාවිතයෙන් අවසාන ඉලක්කම වෙන් කර ගන්නා ආකාරයත්, `/ 10` භාවිතයෙන් ඒ ඉලක්කම ඉවත් කරන ආකාරයත් ඉතා නිවැරදිව තේරුම් අරගෙන තියෙනවා. සාමාන්‍ය ධන සංඛ්‍යා (Positive numbers) සඳහා මේ කේතය 100% ක් වැඩ කරනවා.

---

## 🧠 Explanation & Additional Tips (විවරණය සහ උපදෙස්)

### ඇයි මේ කේතය නිවැරදි? (How it works)
අපි `125` කියන අගය ගත්තොත් loop එක ඇතුලේ වෙන දේ:
1. **Step 1:** `number = 125`. `125 > 0` (True). `sum += 125 % 10` -> `sum = 5`. `number /= 10` -> `number = 12`.
2. **Step 2:** `number = 12`. `12 > 0` (True). `sum += 12 % 10` -> `sum = 5 + 2 = 7`. `number /= 10` -> `number = 1`.
3. **Step 3:** `number = 1`. `1 > 0` (True). `sum += 1 % 10` -> `sum = 7 + 1 = 8`. `number /= 10` -> `number = 0`.
4. **Step 4:** `number = 0`. `0 > 0` (False). Loop එක නතර වෙනවා. `8` return වෙනවා.

### The A+ Strategy (Edge Cases for Math Operations)

ඔබේ කේතයේ කුඩා අඩුවක් තියෙනවා. කවුරුහරි **සෘණ සංඛ්‍යාවක් (Negative Number)** දුන්නොත් මොකද වෙන්නේ? උදාහරණයක් විදියට `-125` දුන්නොත්?

ඔබේ condition එක තියෙන්නේ `while (number > 0)` කියලයි. එතකොට `-125 > 0` False වෙන නිසා loop එක එක පාරක්වත් වැඩ කරන්නේ නැතුව කෙලින්ම `0` කියන අගය return කරනවා. 

**මේක විසඳන A+ ක්‍රමය (Absolute Value):**
සංඛ්‍යාවක් දුන්නම ඒකේ සෘණ ලකුණ අයින් කරලා ධන අගය (Absolute value) ගන්න අපිට `Math.abs()` කියන function එක පාවිච්චි කරන්න පුළුවන්.

```java
public static int sumOfDigits(int number) {
    // Edge case: සෘණ අගයන් ධන අගයන් බවට පත් කිරීම (Handle negative numbers)
    number = Math.abs(number);
    
    int sum = 0;
    while (number > 0) {
        sum += number % 10;
        number /= 10;
    }
    return sum;
}
```

දැන් කවුරුහරි `-125` දුන්නත් ඒක `125` බවට පත් වෙලා, නිවැරදි උත්තරය වන `8` ලබා දෙනවා.

**Vocabulary for Exams:**
* `Modulo operator (%)` - බෙදුවට පස්සේ ඉතුරු වෙන අගය (Remainder) ලබා ගන්නා සංකේතය.
* `Integer division (/)` - පූර්ණ සංඛ්‍යා දෙකක් බෙදුවම දශම අගයන් ඉවත් කරලා පූර්ණ සංඛ්‍යාවක්ම ලබා දීම.
* `Absolute value` - ලකුණ (Sign) නොසලකා හරින අගය (උදා: -5 හි නිරපේක්ෂ අගය 5 වේ).
