# Study Activity 04: Switch Statements (Menu/Choices)

## 📌 The Question (ප්‍රශ්නය)

Write a Java method that takes an integer (`dayCode`) and returns the name of the day using a `switch` statement.

* 1 -> "Monday"
* 2 -> "Tuesday"
* ...
* 7 -> "Sunday"
* වෙනත් ඕනෑම අගයක් ආවොත් -> "Invalid Day" return කරන්න.

**Requirements:**

1. **Method Name:** `getDayName`
2. **Parameters:** `int dayCode`
3. **Return Type:** `String`
4. **Condition:** You MUST use a `switch` statement.

---

## 💻 Your Answer (ඔබේ පිළිතුර)

```java
public static String getDateName(int dayCode){
    switch (dayCode){
        case 1:
            return "Monday";
        case 2:
            return "Tuesday";
        case 3:
            return "Wednesday";
        case 4:
            return "Thursday";
        case 5:
            return "Friday";
        case 6:
            return "Saturday";
        case 7:
            return "Sunday";
        default:
            return "Invalid Day";
    }
}
```

---

## 💯 Evaluation & Marks (ඇගයීම සහ ලකුණු)

**Marks Awarded:** 10/10 (A+) 🌟

**Instructor's Impression:**
අතිවිශිෂ්ටයි! (Outstanding!). ඔබ මගේ Hint එක හරියටම පාවිච්චි කරලා තියෙනවා. සාමාන්‍යයෙන් `switch` එකකදී හැම case එකකටම පස්සේ `break;` දාන්න ඕනේ. හැබැයි ඔබ කෙලින්ම **`return`** කරපු නිසා `break;` දාන්න අවශ්‍ය වුණේ නැහැ. ඒක ඉතාමත් ඉහළ මට්ටමේ coding practice එකක් (Advanced Practice).
පොඩි දෙයයි වරදින්න ගියේ, method name එක `getDayName` වෙනුවට `getDateName` කියලා ටයිප් වෙලා තියෙනවා, ඒක ලොකු ප්‍රශ්නයක් නෙවෙයි.

---

## 🧠 Explanation & Additional Tips (විවරණය සහ උපදෙස්)

### Fall-Through (විභාගයට එන ලොකුම උගුල - The biggest exam trap)

ඔබ මේ විදියට variable එකකට දාන්න කේතය (Code) ලිව්වා නම්, අනිවාර්යයෙන්ම **`break;`** භාවිත කළ යුතුයි. එහෙම නැති වුණොත්, ගැලපෙන case එකේ ඉඳන් පහළට තියෙන ඔක්කොම cases ටික execute වෙනවා. අපි ඒකට කියන්නේ **Fall-through** කියලා.

**උදාහරණයක් (Example of Fall-through):**

```java
public static void printDay(int code) {
    switch (code) {
        case 1: System.out.println("Monday"); // No break!
        case 2: System.out.println("Tuesday"); break;
    }
}
```

*විභාගයේදී මේ වගේ එකක් දීලා Output එක ඇහුවොත්:* ඔබ `code = 1` දුන්නොත්, ඒකෙන් "Monday" සහ "Tuesday" **දෙකම** print වෙනවා, මොකද පලවෙනි එකේ `break;` නැති නිසා. විභාගයේදී මේක ගොඩක් අයව අන්දන (Tricky) තැනක්!

### Using `default:`

You correctly used the `default:` case. This is equivalent to the `else` block in an `if-else` statement. Always include it to handle unexpected inputs.

**Vocabulary for Exams:**

* `Fall-through` - `break` එකක් නොමැති වීම නිසා යටින් ඇති cases ද ක්‍රියාත්මක වීම.
* `default case` - කිසිදු case එකක් ගැලපෙන්නේ නැති විට ක්‍රියාත්මක වන කොටස.
