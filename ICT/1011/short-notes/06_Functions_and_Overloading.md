# 🚀 ICT 1011 Master Class: 06 - Functions & Overloading

> **මෙය ICT 1011 විෂය නිර්දේශයේ හයවන කොටස සම්පූර්ණයෙන්ම ආවරණය කරන මහාචාර්ය මට්ටමේ (Professor-level) සටහනකි.**
> (Methods හඳුන්වාදීම, Return Types, Scope, සහ Method Overloading මෙහි අන්තර්ගත වේ).

---

## 1. Functions / Methods (ශ්‍රිත)
වඩා විශාල වැඩසටහනක් කුඩා, කළමනාකරණය කළ හැකි (manageable) සහ නැවත භාවිත කළ හැකි (reusable) කොටස් වලට කැඩීම සඳහා Functions භාවිතා කරයි. (Java වලදී Functions හඳුන්වන්නේ **Methods** ලෙසයි).

### 🛠️ Method එකක් සාදන ආකාරය (Method Declaration)
Method එකක් ප්‍රධාන කොටස් 4කින් සමන්විත වේ:
1. **Access Modifier:** (e.g., `public`, `private`, `protected`). මෙයින් තීරණය කරන්නේ මෙම method එක වෙනත් classes වලට පෙනෙනවාද නැද්ද යන්නයි.
2. **Return Type:** Method එකෙන් පිටතට ලබා දෙන අගයේ වර්ගය (e.g., `int`, `double`, `void`).
3. **Method Name:** Method එකේ නම (camelCase භාවිතයෙන්). e.g., `calculateSum`.
4. **Parameters (Arguments):** Method එකට ඇතුළට ලබා දෙන දත්ත. (වරහන් තුළ කොමා වලින් වෙන් කර ලියයි).

```java
// උදාහරණයක්: ඉලක්කම් 2ක එකතුව සෙවීමේ Method එකක්
public static int calculateSum(int a, int b) {
    int sum = a + b;
    return sum; // int වර්ගයේ අගයක් Return (ආපසු ලබා දීම) කළ යුතුය.
}
```
*(මෙහි `static` යෙදුවේ Object එකක් නොසාදාම `main` method එක ඇතුළෙන් කෙලින්ම කතා කිරීමට (Call කිරීමට) අවශ්‍ය බැවිනි).*

### 🈳 `void` Return Type
Method එකකින් කිසිදු අගයක් ආපසු ලබා දෙන්නේ නැතිනම් (Return කරන්නේ නැතිනම්), එහි Return Type එක ලෙස `void` යෙදිය යුතුය. එවැනි Methods වල අගට `return;` කියා පමණක් ලියයි (හෝ කිසිවක් නොලියා සිටිය හැක).

```java
public static void printGreeting(String name) {
    System.out.println("Hello, " + name + "!");
    // මෙහි return statement එකක් අවශ්‍ය නැත (void නිසා).
}
```

> [!CAUTION]
> **Professor's Trap (Missing Return Statement):** 
> Method එකේ Return Type එක `int`, `double`, හෝ `String` වැනි යමක් නම්, අනිවාර්යයෙන්ම ඒ අදාළ වර්ගයේ අගයක් `return` කළ යුතුමය! එසේ නොමැති නම්, `Missing return statement` යනුවෙන් Compile-time error එකක් පැමිණේ. `if-else` වැනි කොන්දේසි ඇතුළේ `return` කරනවා නම්, සියලුම කොන්දේසි අසමත් (Fail) වුවත් යම් අගයක් return වන බවට තහවුරු කළ යුතුය.

---

## 2. Variable Scope (විචල්‍ය පරාසය)
Variable එකක් භාවිත කළ හැකි ප්‍රදේශය Scope එක ලෙස හැඳින්වේ.

1. **Local Variables (ස්ථානීය විචල්‍ය):**
   Method එකක් (හෝ Loop එකක්, If block එකක්) ඇතුළේ සාදන Variables, Local Variables වේ. ඒවා භාවිතා කළ හැක්කේ ඒ අදාළ වරහන් `{}` ඇතුළේ පමණි! වරහනෙන් එළියට ආපසු ඒවා Memory එකෙන් මකා දැමේ.
2. **Global / Instance / Class Variables (ගෝලීය විචල්‍ය):**
   Class එකක් ඇතුළේ (නමුත් Methods වලින් පිටත) සාදන Variables මේවා වේ. Class එකේ ඕනෑම Method එකකට මේවා භාවිතා කළ හැක.

---

## 3. Method Overloading (ශ්‍රිත අධිපූරණය)
Java වල **එකම නම (same name) සහිත Methods කිහිපයක්** එකම Class එකක් ඇතුළේ ලිවීමේ හැකියාව Method Overloading ලෙස හැඳින්වේ. (Polymorphism හි එක් ආකාරයකි). 
නමුත් එසේ කිරීමට නම්, ඒවායේ **Parameters (Arguments) වල (අවම වශයෙන් එක) වෙනසක්** තිබිය යුතුය! (මෙම වෙනස Method Signature එකේ වෙනසක් ලෙසද හැඳින්වේ).

### 🔄 Overloading කළ හැකි ක්‍රම 3ක්:
1. **පරාමිති ගණන වෙනස් වීම (Different number of parameters):**
   ```java
   public int add(int a, int b) { ... }
   public int add(int a, int b, int c) { ... } // ✅ නිවැරදියි (පරාමිති 3යි)
   ```
2. **පරාමිති වල දත්ත වර්ගය වෙනස් වීම (Different data types):**
   ```java
   public int add(int a, int b) { ... }
   public double add(double a, double b) { ... } // ✅ නිවැරදියි (double වර්ගය)
   ```
3. **පරාමිති වල අනුපිළිවෙල වෙනස් වීම (Different order of parameters):**
   ```java
   public void display(int age, String name) { ... }
   public void display(String name, int age) { ... } // ✅ නිවැරදියි (අනුපිළිවෙල වෙනස්)
   ```

> [!WARNING]
> **Professor's Ultimate Trap (Return Type Overloading):** 
> විභාග ප්‍රශ්න පත්‍ර හදන බොහෝ දෙනෙකුගේ ප්‍රියතම MCQ ප්‍රශ්නයක් මෙයයි. 
> Method දෙකක නම සහ Parameters දෙකම එක සමාන වී, ඒවායේ **Return Type එක පමණක් වෙනස් කිරීමෙන්** Method Overloading කළ හැකිද? **නොහැක!** එය Compile-time Error එකකි.
> 
> ```java
> public int add(int a, int b) { return a + b; }
> public double add(int a, int b) { return a + b; } // 🚨 ERROR! Cannot overload by return type alone.
> ```
> (හේතුව: ඔබ `add(5, 5)` ලෙස කතා කළොත්, ඒ කුමන add method එකටද කියා Compiler එකට හඳුනාගැනීමට Return type එක කිසිසේත් උදව් නොකරන බැවිනි).
