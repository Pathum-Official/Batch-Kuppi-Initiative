# 🚀 ICT 1011 Master Class: 03 - Operators, Math & Expressions

> **මෙය ICT 1011 විෂය නිර්දේශයේ තුන්වන කොටස සම්පූර්ණයෙන්ම ආවරණය කරන මහාචාර්ය මට්ටමේ (Professor-level) සටහනකි.**
> (Operators, Type Casting, සහ Math Library එක ගැන මෙහි සාකච්ඡා කෙරේ).

---

## 1. Operators (මෙහෙයුම්කාරක)

### 🧮 Arithmetic Operators (ගණිත කර්ම)
* `+` : එකතු කිරීම (Addition) / String Concatenation (වචන යා කිරීම)
* `-` : අඩු කිරීම (Subtraction)
* `*` : ගුණ කිරීම (Multiplication)
* `/` : බෙදීම (Division) 
* `%` : Modulo (බෙදූ පසු ඉතිරි වන අගය / Remainder). e.g., `5 % 2 = 1`. 

> [!CAUTION]
> **Professor's Trap (Integer Division):**
> ඉලක්කම් දෙකම Integer (`int`) නම්, බෙදීමේදී (`/`) ලැබෙන දශම අගය ඉවත් වී යයි!
> `double result = 5 / 2;` මෙහිදී `result` හි අගය `2.0` වේ! (2.5 නොවේ).
> නිවැරදිව 2.5 ලබා ගැනීමට එකක් හෝ double විය යුතුය: `double result = 5.0 / 2;` හෝ Type Casting කළ යුතුය: `double result = (double) 5 / 2;`.

### ⚖️ Relational Operators (සංසන්දනය)
අගයන් දෙකක් සසඳා බලා `true` හෝ `false` ලබා දෙයි.
* `==` : සමානද? (Equal to) - * `=` (Assignment) එක්ක පටලවාගන්න එපා!*
* `!=` : අසමානද? (Not equal to)
* `>`, `<`, `>=`, `<=`

### 🧠 Logical Operators (තර්කණ)
කොන්දේසි (Conditions) කිහිපයක් එකට සම්බන්ධ කිරීමට.
* `&&` (Logical AND): දෙකම True නම් පමණක් True වේ. (T && T = T)
* `||` (Logical OR): එකක් හෝ True නම් True වේ. (T || F = T)
* `!` (Logical NOT): True නම් False කරයි, False නම් True කරයි. (!T = F)

### ➕➖ Increment / Decrement Operators
* `x++` (Post-increment): පසුව වැඩි වේ. (පළමුව වත්මන් අගය භාවිතා කර, පසුව අගය 1 කින් වැඩි කරයි).
* `++x` (Pre-increment): පෙර වැඩි වේ. (පළමුව අගය 1 කින් වැඩි කර, පසුව එම අගය භාවිතා කරයි).

```java
int a = 5;
int b = a++; // b = 5, a = 6 (පළමුව a හි අගය b ට ලබා දී පසුව a වැඩි වේ)

int c = 5;
int d = ++c; // c = 6, d = 6 (පළමුව c වැඩි වී පසුව එම අගය d ට ලබා දේ)
```

---

## 2. Java Math Library (ගණිතමය ශ්‍රිත)
සංකීර්ණ ගණනය කිරීම් සඳහා Java වල `Math` class එක භාවිතා කරයි. මේවා සියල්ලම `static` methods වන බැවින් Object එකක් නොසාදා කෙලින්ම `Math.` යොදා භාවිතා කළ හැක.

* **`Math.max(a, b)`:** අගයන් දෙකෙන් විශාල අගය ලබා දෙයි.
* **`Math.min(a, b)`:** අගයන් දෙකෙන් කුඩා අගය ලබා දෙයි.
* **`Math.sqrt(x)`:** වර්ගමූලය (Square root) ලබා දෙයි. (e.g., `Math.sqrt(25)` -> 5.0)
* **`Math.pow(x, y)`:** බලය (Power) ලබා දෙයි. x හි y වෙනි බලය. (e.g., `Math.pow(2, 3)` -> 8.0)
* **`Math.abs(x)`:** නිරපේක්ෂ අගය (Absolute value) ලබා දෙයි. සෘණ අගයන් ධන කරයි. (e.g., `Math.abs(-5)` -> 5)
* **`Math.PI`:** පයි (π) හි අගය (3.14159...). මෙය Method එකක් නොව Constant (නියත) අගයකි. එබැවින් වරහන් `()` නැත!

```java
double radius = 5.0;
// රවුමක වර්ගඵලය: A = π * r^2
double area = Math.PI * Math.pow(radius, 2);
```

### 🎲 Random Numbers (අහඹු සංඛ්‍යා)
* **`Math.random()`:** මෙය 0.0 (ඇතුළත්ව) සහ 1.0 (නොඇතුළත්ව) අතර දශම සංඛ්‍යාවක් ලබා දෙයි. (0.0 <= x < 1.0).

අපට අවශ්‍ය පරාසයක (උදා: 0 සිට 9 දක්වා) අහඹු පූර්ණ සංඛ්‍යාවක් (Integer) ලබා ගැනීමට:
```java
// 0 ත් 9 ත් අතර අහඹු සංඛ්‍යාවක්
int randomNum = (int) (Math.random() * 10);
```

> [!WARNING]
> **Professor's Trap (Math.random() Casting):**
> `int randomNum = (int) Math.random() * 10;` ලෙස ලිව්වොත් කුමක් වෙයිද?
> `Math.random()` වලින් එන දශම අගය (e.g. 0.85) පළමුව `int` බවට පත් වී 0 බවට පත්වේ. ඉන්පසු එය 10න් ගුණ වේ. (0 * 10 = 0). එනම් සෑමවිටම පිළිතුර 0 වේ!
> අනිවාර්යයෙන්ම ගුණ කිරීම වරහන් ඇතුළේ ලිවිය යුතුය: `(int) (Math.random() * 10)`

---

## 3. Type Casting (දත්ත වර්ග පරිවර්තනය)
එක් Data Type එකක් තවත් Type එකකට හැරවීම.

1. **Implicit Casting (ස්වයංක්‍රීයව සිදුවීම - Widening):** කුඩා Type එකකින් විශාල Type එකකට (දත්ත හානියක් නැත).
   * `int -> double`
   * `int myInt = 9;` -> `double myDouble = myInt;` (myDouble 9.0 බවට පත්වේ).

2. **Explicit Casting (බලහත්කාරයෙන් කිරීම - Narrowing):** විශාල Type එකකින් කුඩා Type එකකට (දත්ත හානි විය හැක). මෙය අතින්ම (manually) කළ යුතුය.
   * `double -> int`
   * `double myDouble = 9.78;` -> `int myInt = (int) myDouble;` (myInt 9 බවට පත්වේ - දශම අගය කැපී යයි!).
