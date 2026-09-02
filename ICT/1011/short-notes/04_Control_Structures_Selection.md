# 🚀 ICT 1011 Master Class: 04 - Control Structures (Selection)

> **මෙය ICT 1011 විෂය නිර්දේශයේ හතරවන කොටස සම්පූර්ණයෙන්ම ආවරණය කරන මහාචාර්ය මට්ටමේ (Professor-level) සටහනකි.**
> (If-else, Switch, සහ Ternary Operator මෙහි අන්තර්ගත වේ).

---

## 1. Selection Structures (තෝරාගැනීම් / කොන්දේසි)
වැඩසටහනක් ගලා යන මාර්ගය තීරණයක් (Decision) මත පදනම්ව වෙනස් කිරීමට මේවා භාවිතා වේ.

### 🔀 The `if - else` Statement
කොන්දේසිය (Condition) `true` නම් එක් මාර්ගයකත්, `false` නම් වෙනත් මාර්ගයකත් ගමන් කරයි.

```java
int marks = 75;

if (marks >= 75) {
    System.out.println("Grade A");
} else if (marks >= 65) {
    System.out.println("Grade B");
} else {
    System.out.println("Grade C");
}
```

> [!CAUTION]
> **Professor's Trap 1 (Dangling Else Problem):** 
> `if` හෝ `else` එකක් යටතේ ලියන්නේ එකම එක statement (පේළියක්) පමණක් නම් සඟල වරහන් (Curly braces `{}`) අත්‍යවශ්‍ය නැත. නමුත් විභාගයේදී පැටලීම වළක්වා ගැනීමට **සෑම විටම** `{}` භාවිතා කරන්න!
> 
> **Professor's Trap 2 (Semicolon After If):** 
> `if (marks > 50);` ලෙස අගට semicolon දැමුවහොත්, එම කොන්දේසිය එතනින්ම අවසන් වේ. ඉන්පසු පහළින් ඇති `{ ... }` කොටස කොන්දේසියට සම්බන්ධ නැතිව අනිවාර්යයෙන්ම ධාවනය වේ!

### 🔀 The `switch` Statement
එකම විචල්‍යයක් (Variable) විවිධ අගයන් සමඟ සංසන්දනය කිරීමේදී `if-else` වලට වඩා `switch` භාවිතය පහසු සහ කේතය කියවීමට (Readability) පහසු වේ.

```java
int day = 3;

switch (day) {
    case 1:
        System.out.println("Monday");
        break; // අනිවාර්යයෙන්ම break දැමිය යුතුය!
    case 2:
        System.out.println("Tuesday");
        break;
    case 3:
        System.out.println("Wednesday");
        break; // මෙතනින් නතර වී Switch එකෙන් එළියට යයි.
    default:
        System.out.println("Invalid Day");
}
```

> [!IMPORTANT]
> **The `break` Keyword in Switch (Fall-Through Trap):**
> `switch` එකක `break` එකක් නොදැමුවහොත්, ගැළපෙන (Match) වූ `case` එකේ සිට පහළට ඇති සියලුම `case` වල කේතය ක්‍රියාත්මක වේ! මෙය **Fall-through** ලෙස හැඳින්වේ. බොහෝ විට විභාග ප්‍රශ්න වල (MCQ වලදී විශේෂයෙන්ම) ළමයින්ව වට්ටන්න මේ විදිහට `break` නොදා ප්‍රශ්න දෙනවා. එවිට Output එක අදාළ case එක සහ ඊට පහළින් ඇති සියලුම දේවල් වේ!

### 💡 `switch` හි භාවිතා කළ හැකි Data Types:
Java වල `switch` එකක් ඇතුළේ භාවිතා කළ හැක්කේ පහත Data Types පමණි:
* `int`, `byte`, `short`, `char` (මූලික)
* `String` (Java 7 සිට)
* `Enums`
* **අවධානය යොමු කරන්න:** `double`, `float`, `boolean` භාවිතා **කළ නොහැක!**

---

## 2. Ternary Operator (කෙටි If-Else)
`if-else` එක පේළියකින් ලිවීම සඳහා මෙය භාවිතා කරයි. මෙහිදී කොන්දේසියක් පරීක්ෂා කර True නම් එක අගයකුත්, False නම් තව අගයකුත් Variable එකකට පවරයි.

**Syntax:** `variable = (condition) ? valueIfTrue : valueIfFalse;`

### 🛠️ උදාහරණය:
```java
int time = 20;

// සාමාන්‍ය if-else ක්‍රමය:
String result;
if (time < 18) {
  result = "Good day.";
} else {
  result = "Good evening.";
}

// Ternary Operator ක්‍රමය (එක පේළියයි!):
String result2 = (time < 18) ? "Good day." : "Good evening.";
System.out.println(result2);
```

> [!TIP]
> විභාගයේදී "Use a single line of code to..." වගේ ඇහුවොත්, Ternary operator එක මතක් කරගන්න!
