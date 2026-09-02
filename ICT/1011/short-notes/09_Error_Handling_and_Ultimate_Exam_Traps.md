# 🚀 ICT 1011 Master Class: 09 - Error Handling & Ultimate Exam Traps

> **මෙය ICT 1011 විෂය නිර්දේශයේ අවසාන කොටස සම්පූර්ණයෙන්ම ආවරණය කරන මහාචාර්ය මට්ටමේ (Professor-level) සටහනකි.**
> (මෙම සටහන විභාගයට පෙර දින අනිවාර්යයෙන්ම කියවිය යුතුම එකකි. මන්දයත් මුළු සිලබස් එකේම ඇති ලකුණු කැපෙන සියුම් තැන් මෙහි සම්පිණ්ඩනය කර ඇති බැවිනි).

---

## 1. Exceptions and Error Handling (දෝෂ කළමනාකරණය)
වැඩසටහනක් ධාවනය වන අවස්ථාවේදී (Runtime) බලාපොරොත්තු නොවන ගැටලුවක් (උදා: බිංදුවෙන් බෙදීම, නැති අරා දර්ශකයක් සෙවීම) ආවොත් වැඩසටහන Crash වීම (බිඳ වැටීම) වැළැක්වීමට `try-catch` භාවිතා කරයි. 

### 🛡️ The `try-catch` Block
* **`try` block:** දෝෂයක් (Error එකක්) පැමිණිය හැකි යැයි අප සැක කරන කේත කොටස මෙහි ලියයි.
* **`catch` block:** යම් හෙයකින් `try` block එකේදී Error එකක් ආවොත්, වැඩසටහන Crash නොවී කෙලින්ම යන්නේ `catch` block එකටයි. ඉන්පසු වැඩසටහන සාමාන්‍ය පරිදි ඉදිරියට ධාවනය වේ.

```java
public class ExceptionDemo {
    public static void main(String[] args) {
        
        System.out.println("Program Started!");
        
        try {
            int result = 10 / 0; // 🚨 බිංදුවෙන් බෙදීම (ArithmeticException)
            System.out.println("This line will NOT be executed."); // ඉහත දෝෂය නිසා මෙම පේළිය වැඩ කරන්නේ නැත.
        } 
        catch (ArithmeticException e) {
            System.out.println("Oops! You cannot divide by zero."); 
            // e.printStackTrace(); // Error එක කුමක්දැයි විස්තරාත්මකව බැලීමට මෙය භාවිතා කළ හැක.
        }
        catch (Exception e) {
            // වෙනත් ඕනෑම වර්ගයක දෝෂයක් ආවොත් අල්ලා ගැනීමට මෙය ලියයි (Fall-back option).
            System.out.println("Something went wrong!");
        }
        
        System.out.println("Program Finished Successfully!"); // වැඩසටහන Crash නොවී මෙතැනට පැමිණේ.
    }
}
```

### 🛑 නිතර දකින Exception වර්ග (Common Exceptions):
1. **`ArithmeticException`:** ගණිතමය දෝෂ (උදා: බිංදුවෙන් බෙදීම - Division by zero).
2. **`ArrayIndexOutOfBoundsException`:** Array එකක නැති Index එකක් (Limit එක පැනලා) සෙවීමට යෑම.
3. **`NullPointerException`:** අගයක් (Object එකක්) නැති (Null වූ) විචල්‍යයක යමක් සෙවීමට යාම.
4. **`InputMismatchException`:** Scanner එකෙන් ඉලක්කමක් (`nextInt`) ඉල්ලූ විට අකුරක් ("abc") Type කිරීම.

---

## 2. 🎓 The Ultimate "Professor's Traps" Summary (විභාගයේදී වට්ටන තැන්)
මහාචාර්යවරුන් විසින් විභාග (විශේෂයෙන්ම MCQ සහ කේත ලියන ප්‍රශ්න වලදී) ළමයින්ගේ අවධානය පරීක්ෂා කිරීමට යොදන ප්‍රධාන උගුල් (Traps) මෙන්න:

### Trap #1: Integer Division (බෙදීමේ උගුල)
```java
double a = 5 / 2;
System.out.println(a);
```
**ඔබ හිතන පිළිතුර:** `2.5`
**නියම පිළිතුර:** `2.0`
**හේතුව:** ඉලක්කම් දෙකම Integers (5 සහ 2) නිසා බෙදීමේදී දශම ටික කැපී යයි (5/2 = 2 වේ). ඉන්පසු එය double එකකට දමන නිසා 2.0 වේ. නිවැරදි වීමට `5.0 / 2` විය යුතුය.

### Trap #2: String Concatenation vs Addition (එකතු කිරීමේ උගුල)
```java
System.out.println(10 + 20 + "Hello");
System.out.println("Hello" + 10 + 20);
```
**Output 1:** `30Hello` (වමේ සිට දකුණට යන නිසා පළමුව 10+20=30 වේ, පසුව Hello එකතු වේ).
**Output 2:** `Hello1020` (පළමුව Hello වචනය හමුවූ නිසා, ඉන්පසු එන ඉලක්කම් ද වචන ලෙසම යා වේ. එනම් Hello10 සහ පසුව Hello1020 වේ. 30 නොවේ!).

### Trap #3: Missing `break` in Switch (Fall-through උගුල)
`switch` එකක `case 1:` හි `break;` නැතිනම්, එයට ගැලපුනද එතැනින් නොනැවතී ඊළඟට ඇති `case 2`, `case 3` යනාදී සියල්ලේ කේතයන් ධාවනය වේ!

### Trap #4: Semicolon after `if` or `for` (තිතේ උගුල)
```java
if (marks > 50); {
    System.out.println("Pass");
}
```
**ප්‍රතිඵලය:** ළමයාගේ marks කීය වුණත් (marks 10ක් වුණත්) "Pass" කියා Print වේ! 
**හේතුව:** `if` එකට පසුව ඇති `;` නිසා if කොන්දේසිය එතැනින්ම අවසන් වේ. යට ඇති `{ ... }` කොටස කොන්දේසියට අදාළ නැති සාමාන්‍ය කේත කොටසක් ලෙස ධාවනය වේ.

### Trap #5: Array Initialization Limits (අරා උගුල)
`int[] arr = new int[5];`
මෙම array එකේ ප්‍රමාණය 5කි. නමුත් එහි අගයන් දැමිය හැක්කේ `arr[0]` සිට `arr[4]` දක්වා පමණි. විභාගයේදී `arr[5] = 10;` ලෙස දී තිබුණොත් එය **`ArrayIndexOutOfBoundsException`** දෝෂයකි.

### Trap #6: Overloading by Return Type (Method උගුල)
Method එකක නම සහ Parameters දෙකම සමාන වී, Return Type එක පමණක් වෙනස් කිරීමෙන් Method Overloading **කළ නොහැක!** එය Compile error එකකි. (Overload වීමට නම් Parameters වල වෙනසක් තිබිය යුතුමය).

### Trap #7: Equality `==` vs Assignment `=` (සමාන කිරීමේ උගුල)
```java
int x = 5;
if (x = 10) { ... } // 🚨 ERROR!
```
**හේතුව:** `x = 10` යනු අගය පැවරීමකි (Assignment). සංසන්දනය කිරීමකට අනිවාර්යයෙන්ම `==` භාවිතා කළ යුතුය (`if (x == 10)`).

> [!TIP]
> **ප්‍රායෝගික උපදෙස (Exam Strategy):**
> 1. කේතයක් කියවන විට, ඔබ Compiler එකක් සේ සිතා පේළියෙන් පේළිය (Line by line) කියවන්න.
> 2. Variable වල අගයන් වෙනස් වන ආකාරය පැන්සලකින් කොළයක ලියාගන්න (Trace the variables).
> 3. වරහන් `{ }` සහ කොමා `;` නිවැරදි ස්ථාන වල ඇතිදැයි හොඳින් පරීක්ෂා කරන්න.
