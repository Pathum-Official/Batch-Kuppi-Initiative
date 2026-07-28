# 04. Control Structures and Alternatives (පාලන ව්‍යුහ සහ විකල්ප)

සාමාන්‍ය `for`, `while`, `do-while` සහ `switch` වලට අමතරව දැනගත යුතු විශේෂ දේවල්.

## 1. Enhanced For-Loop (For-Each Loop)
අරාවක (Array) ඇති අගයන් එකින් එක ලබා ගැනීමට භාවිතා කරන ඉතාම පහසු ක්‍රමයකි. මෙහිදී Index (`i`) භාවිතා නොවේ.

**සාමාන්‍ය For-Loop:**
```java
int[] marks = {80, 90, 75};
for (int i = 0; i < marks.length; i++) {
    System.out.println(marks[i]);
}
```

**Enhanced For-Loop (අතිශය වැදගත් විකල්පය):**
```java
int[] marks = {80, 90, 75};
// "marks අරාවේ ඇති සෑම int mark එකක් සඳහාම"
for (int mark : marks) { 
    System.out.println(mark); // මෙහිදී mark යනු අරාවේ ඇති අගයයි.
}
```

## 2. Break and Continue
* **`break;`** : Loop එක සම්පූර්ණයෙන්ම නතර කර ඉන් පිටතට පැමිණේ.
* **`continue;`** : Loop එකේ දැනට ක්‍රියාත්මක වන වාරය (Iteration) පමණක් මඟ හැර ඊළඟ වාරයට (Next iteration) යයි.
  ```java
  for (int i = 1; i <= 5; i++) {
      if (i == 3) continue; // 3 skip කරයි. 1, 2, 4, 5 පමණක් print වේ.
      System.out.println(i);
  }
  ```

## 3. Switch vs If-Else
* බොහෝදුරට සමාන අගයන් (Exact matches) පරීක්ෂා කිරීමට `switch` භාවිතා කිරීම සුදුසුය.
* පරාසයන් (Ranges - e.g. `marks > 75`) පරීක්ෂා කිරීමට අනිවාර්යයෙන්ම `if-else` භාවිතා කළ යුතුය.

## 4. Ternary Operator (කෙටි If-Else)
සරල `if-else` එකක් එක පේළියකින් ලිවීමට භාවිතා කරයි.
**Syntax:** `(Condition) ? TrueAction : FalseAction;`

```java
int age = 20;
// වයස 18ට වැඩි නම් "Adult", නැත්නම් "Minor"
String status = (age >= 18) ? "Adult" : "Minor"; 
```
