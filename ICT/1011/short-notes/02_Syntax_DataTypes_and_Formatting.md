# 🚀 ICT 1011 Master Class: 02 - Syntax, Data Types & Formatting

> **මෙය ICT 1011 විෂය නිර්දේශයේ දෙවන කොටස සම්පූර්ණයෙන්ම ආවරණය කරන මහාචාර්ය මට්ටමේ (Professor-level) සටහනකි.**
> (Variables, Types, Naming conventions, Scanner Input, සහ `printf` Formatting මෙහි අන්තර්ගත වේ).

---

## 1. Variables and Data Types (විචල්‍ය සහ දත්ත වර්ග)
Java යනු **Statically Typed** භාෂාවකි. එනම් Variable එකක් සෑදීමේදී අනිවාර්යයෙන්ම එහි Type එක (වර්ගය) සඳහන් කළ යුතුය. (උදා: Python වල මෙන් නිකම්ම `x = 10` ලිවිය නොහැක).

### 📦 1. Primitive Types (මූලික දත්ත වර්ග 8කි)
මේවා තුළ සෘජුවම අගයන් ගබඩා වේ.
* **Integers (පූර්ණ සංඛ්‍යා):** `byte` (8-bit), `short` (16-bit), `int` (32-bit), `long` (64-bit). (සාමාන්‍ය භාවිතය `int` වේ).
* **Floating-point (දශම සංඛ්‍යා):** `float` (32-bit), `double` (64-bit). (සාමාන්‍ය භාවිතය `double` වේ. `float` භාවිතා කරන්නේ නම් අගට `f` අකුර දැමිය යුතුය. e.g. `float pi = 3.14f;`).
* **Characters (අකුරු):** `char` (16-bit). තනි අකුරක් පමණි. **නිසැකවම Single Quotes ('') භාවිතා කළ යුතුය!** e.g., `'A'`, `'x'`.
* **Booleans:** `boolean`. `true` හෝ `false` අගයන් පමණි.

### 📦 2. Reference Types (යොමු දත්ත වර්ග)
මේවායේ ගබඩා වන්නේ අදාළ අගය ඇති Memory Address එකයි (Object reference).
* **Strings:** වචන/වාක්‍ය. **Double Quotes ("") භාවිතා කළ යුතුය!** e.g., `"Hello World"`.
* Arrays (අරාවන්), Objects (වස්තූන්).

---

## 2. Identifiers & Naming Conventions (නම් තැබීමේ නීති)
Variables, Methods, සහ Classes සඳහා ලබා දෙන නම් **Identifiers** ලෙස හැඳින්වේ.

### 🚨 අනිවාර්ය නීති (Rules - කැඩුවොත් Error එයි):
1. අකුරු, ඉලක්කම්, Underscore (`_`), සහ Dollar sign (`$`) පමණක් භාවිතා කළ හැක. 
2. **කිසිවිටෙකත් ඉලක්කමකින් ආරම්භ කළ නොහැක!** (`1stStudent` වැරදියි. `student1` නිවැරදියි).
3. Java හි වෙන් කර ඇති වචන (Keywords - e.g., `class`, `public`, `int`) භාවිතා කළ නොහැක.
4. හිස්තැන් (Spaces) තැබිය නොහැක. (`first name` වැරදියි).

### 👔 සම්මුතීන් (Conventions - Good Practices):
* **Classes:** PascalCase (e.g., `StudentDetails`, `BankAccount`). අනිවාර්යයෙන්ම Capital අකුරකින් පටන් ගත යුතුය.
* **Methods & Variables:** camelCase (e.g., `calculateTotal`, `studentName`).
* **Constants (නියතයන් - වෙනස් නොවන අගයන්):** ALL_CAPS_WITH_UNDERSCORES (e.g., `final double PI = 3.14159;`). මෙහි `final` keyword එක යෙදූ විට එහි අගය පසුව වෙනස් කළ නොහැක.

---

## 3. Input and Output (ආදානය සහ ප්‍රතිදානය)

### ⌨️ Input (Scanner භාවිතය)
User ගෙන් Input එකක් ගැනීමට `Scanner` class එක භාවිතා කරයි.

```java
import java.util.Scanner; // 1. අනිවාර්යයෙන්ම Import කළ යුතුය!

public class UserInput {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in); // 2. Scanner Object එකක් සෑදීම
        
        System.out.print("Enter your age: ");
        int age = scanner.nextInt(); // Integer එකක් කියවීම
        
        System.out.print("Enter your name: ");
        String name = scanner.next(); // වචනයක් (String) කියවීම
        
        // 3. Scanner එක වැසීම (Memory leaks වළක්වා ගැනීමට)
        scanner.close(); 
    }
}
```

> [!CAUTION]
> **Professor's Trap (Scanner String Input):**
> විභාගයේදී String (වචන) input එකක් ගන්නවා නම් `scanner.next()` හෝ `scanner.nextLine()` භාවිතා කරන්න. `scanner.nextString()` කියා method එකක් Java වල **නැත!** සිසුන් බොහෝ විට මෙම වරද කරයි.
> * `next()`: හිස්තැනක් (space) හමුවන තුරු වචනයක් කියවයි (e.g. "John Doe" දුන්නොත් ගන්නේ "John" පමණි).
> * `nextLine()`: මුළු පේළියම (spaces ඇතුළුව) කියවයි.

---

## 4. Output Formatting (`printf` භාවිතය)
ප්‍රතිදානය ලස්සනට සකස් කිරීමට (Format කිරීමට) `System.out.printf()` භාවිතා කරයි. මෙහිදී **Format Specifiers** යොදා ගනී.

### 📝 ප්‍රධාන Format Specifiers
* `%d` : Integer (පූර්ණ සංඛ්‍යා) සඳහා.
* `%f` : Floating-point (දශම සංඛ්‍යා) සඳහා.
* `%s` : String (වචන) සඳහා.
* `%c` : Character (තනි අකුරක්) සඳහා.
* `\n` : අලුත් පේළියකට යෑම (New line).

### 🛠️ ප්‍රායෝගික උදාහරණ:
```java
int marks = 85;
double pi = 3.14159;
String name = "Amal";

// 1. සාමාන්‍ය භාවිතය
System.out.printf("Name: %s, Marks: %d \n", name, marks);
// Output: Name: Amal, Marks: 85 

// 2. දශම ස්ථාන පාලනය කිරීම (ඉතා වැදගත්!)
System.out.printf("Value of PI: %.2f \n", pi);
// Output: Value of PI: 3.14 (දශම 2 කට වටයන ලදී)

// 3. ඉඩ වෙන් කිරීම (Padding / Right Align)
System.out.printf("Marks: %5d \n", marks);
// Output: Marks:    85 (ඉලක්කමට පෙර හිස්තැන් 3ක් තබා සම්පූර්ණ ඉඩ 5ක් වෙන් කරයි)

// 4. වම් පසට බර කිරීම (Left Align)
System.out.printf("Name: %-10s! \n", name);
// Output: Name: Amal      ! (දකුණු පසින් හිස්තැන් 6ක් තබා සම්පූර්ණ ඉඩ 10ක් වෙන් කරයි)
```

> [!WARNING]
> **Professor's Trap (`println` vs `printf`):**
> `printf` භාවිතා කළ විට එය ස්වයංක්‍රීයව අලුත් පේළියකට (`New line`) යන්නේ නැත! අනිවාර්යයෙන්ම `\n` හෝ `%n` අගට එකතු කළ යුතුය. `println` එක ස්වයංක්‍රීයව අලුත් පේළියකට යයි.
