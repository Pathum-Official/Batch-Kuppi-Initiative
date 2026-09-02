# 🚀 ICT 1011 Master Class: 01 - Intro, Pseudocode & Java Basics

> **මෙය ICT 1011 විෂය නිර්දේශයේ පළමු කොටස සම්පූර්ණයෙන්ම ආවරණය කරන මහාචාර්ය මට්ටමේ (Professor-level) සටහනකි.**
> (මෙහිදී Pseudocode, Flowcharts, අල්ගොරිතම සහ Java වැඩ කරන ආකාරය ගැඹුරින් සාකච්ඡා කෙරේ.)

---

## 1. Introduction to Programming (ක්‍රමලේඛනය යනු කුමක්ද?)
පරිගණකයකට යම් කාර්යයක් කිරීමට ලබා දෙන උපදෙස් මාලාවක් (Set of instructions) **Program** එකක් ලෙස හැඳින්වේ. පරිගණකයට තේරෙන්නේ Machine Code (0 සහ 1) පමණක් වුවද, අපට එය ලිවීම අපහසු නිසා High-Level Languages (Java, Python, C++) භාවිතා කරමු.

### 🧠 Algorithm (අල්ගොරිතම)
අල්ගොරිතමයක් යනු යම් ගැටලුවක් විසඳීම සඳහා පියවරෙන් පියවර ලියන ලද තාර්කික උපදෙස් මාලාවකි.
* **ගුණාංග:** පැහැදිලි විය යුතුය (Unambiguous), සීමිත පියවර ගණනකින් අවසන් විය යුතුය (Finiteness).
* අල්ගොරිතමයක් නිරූපණය කිරීමට ප්‍රධාන ක්‍රම 2ක් ඇත:
  1. Pseudocode (ව්‍යාජ කේත)
  2. Flowcharts (ගැලීම් සටහන්)

---

## 2. Pseudocode (ව්‍යාජ කේත)
කිසිදු Programming භාෂාවක නීති (Syntax) මත රඳා නොපවතී. සාමාන්‍ය ඉංග්‍රීසි භාෂාවෙන් තර්කය (Logic) පමණක් ලියයි.

### ✍️ Basic Structure (මූලික ව්‍යුහය)
```text
BEGIN
    // Variables ප්‍රකාශ කිරීම
    DECLARE Number1, Number2, Sum AS INTEGER
    
    // User ගෙන් Input ගැනීම
    PRINT "Enter first number:"
    INPUT Number1
    PRINT "Enter second number:"
    INPUT Number2
    
    // ගණනය කිරීම (Calculation)
    Sum = Number1 + Number2
    
    // Output එක පෙන්වීම
    PRINT "The sum is: ", Sum
END
```

> [!CAUTION]
> **Professor's Trap (විභාගයේදී වරදින තැන්):** 
> Pseudocode ලියන විට කිසිවිටෙකත් Java codes (උදා: `System.out.println`, `Scanner`) භාවිතා කරන්න එපා! එයට ලකුණු නොලැබේ. `PRINT`, `INPUT`, `READ`, `IF`, `ELSE` වැනි සාමාන්‍ය වචන භාවිතා කරන්න.

---

## 3. Flowcharts (ගැලීම් සටහන්)
Flowchart එකක් යනු අල්ගොරිතමයක (Algorithm) චිත්‍රමය හෝ රූපමය නිරූපණයකි. (Visual representation).

### 🔷 සම්මත හැඩතල (Standard Shapes)
* **Oval (ඕවලාකාරය):** `Start` සහ `End` (වැඩසටහන ආරම්භය හා අවසානය).
* **Parallelogram (සමාන්තරාස්‍රය):** `Input` සහ `Output` (දත්ත ඇතුළත් කිරීම සහ ප්‍රතිදාන පෙන්වීම).
* **Rectangle (සෘජුකෝණාස්‍රය):** `Process` (ගණනය කිරීම් සහ අගයන් පැවරීම - Calculations/Assignments).
* **Diamond (දියමන්ති හැඩය):** `Decision` (තීරණ ගැනීම - If/Else කොන්දේසි).
* **Arrows (ඊතල):** Flow of control (වැඩසටහන ගලා යන දිශාව).

---

## 4. How Java Works? (Java ක්‍රියාත්මක වන අයුරු)
Java වල ඇති විශේෂත්වය වන්නේ එය **Platform Independent** (ඕනෑම OS එකක වැඩ කිරීම) වීමයි. මේ සඳහා භාවිතා වන්නේ "Write Once, Run Anywhere" (WORA) සංකල්පයයි.

### ⚙️ The Java Execution Process (සිදුවන පියවර)
1. **Source Code (`.java` file):** ඔබ ලියන සාමාන්‍ය කේතය (e.g., `Main.java`).
2. **Compiler (`javac`):** ජාවා කම්පයිලරය විසින් ඔබේ කේතය **Bytecode** බවට පරිවර්තනය කරයි. (Compiler එක මුළු කේතයම එකවර කියවා වැරදි තිබේදැයි බලයි).
3. **Bytecode (`.class` file):** මෙය OS එකට තේරෙන්නේ නැත. මෙය තේරෙන්නේ JVM එකට පමණි.
4. **JVM (Java Virtual Machine):** JVM එක විසින් Bytecode එක අදාළ පරිගණකයේ OS එකට තේරෙන භාෂාවට (Machine Code) පරිවර්තනය කර ධාවනය කරයි (Run). මෙහිදී භාවිතා වන්නේ **Interpreter** එකකි (පේළියෙන් පේළිය කියවා ධාවනය කරයි).

> [!TIP]
> **Mnemonic / Memory Trick:** 
> `Code (Human)` ➔ `Compiler` ➔ `Bytecode (Class)` ➔ `JVM (Interpreter -> Machine)`
> *Java යනු Compiled සහ Interpreted යන දෙකම භාවිතා කරන භාෂාවකි!*

### 🧩 Java Architecture Components
* **JDK (Java Development Kit):** Java කේත ලිවීමට සහ Compile කිරීමට අවශ්‍ය සියලුම මෙවලම් (Compiler, Debugger) මෙහි ඇත. (අලුතින් කේත ලියන Developers ලාට අවශ්‍ය වේ).
* **JRE (Java Runtime Environment):** Java වැඩසටහන් ධාවනය (Run) කිරීමට පමණක් අවශ්‍ය පරිසරය. (මෙය ඇතුලේ JVM එක ඇත).
* **JVM (Java Virtual Machine):** Bytecode එක Machine Code බවට පත් කර ධාවනය කරන එන්ජිමයි.

---

## 5. First Java Program Structure
```java
// 1. Package Declaration (අනිවාර්ය නැත)
package com.myuniversity;

// 2. Imports (වෙනත් Classes භාවිතා කිරීමට)
import java.util.Scanner;

// 3. Class Declaration
public class Main {
    
    // 4. Main Method (Entry Point - වැඩසටහන ආරම්භ වන තැන)
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

> [!CAUTION]
> **Professor's Trap (Entry Point Error):**
> `main` method එක `public static void main(String[] args)` ලෙසම ලිවිය යුතුය. `static` යන්න අමතක වුවහොත් කේතය Compile වුවද, ධාවනය වන විට (Runtime) `NoSuchMethodError: main` ලෙස දෝෂයක් පෙන්වයි. මන්දයත්, JVM එක Class එකේ Object එකක් නොසාදාම (without instantiating) මුලින්ම main method එකට call කරන බැවිනි (ඒ සඳහා static අනිවාර්යයි).
