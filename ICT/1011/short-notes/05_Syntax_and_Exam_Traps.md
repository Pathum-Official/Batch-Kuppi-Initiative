# 05. Syntax and Exam Traps (ව්‍යාකරණ සහ විභාග උගුල්)

ඔබගේ ලොජික් (Logic) කොතරම් හොඳ වුණත්, පහත වැරදි නිසා කේතය Compile නොවේ.

## 1. The Integer Division Trap (පූර්ණ සංඛ්‍යා බෙදීමේ උගුල)
පූර්ණ සංඛ්‍යා (int) දෙකක් බෙදූ විට පිළිතුරද පූර්ණ සංඛ්‍යාවක්ම වේ. දශමස්ථාන ඉවත් වේ.
```java
int a = 10;
int b = 4;
double answer = a / b; // උත්තරය 2.0 වේ (2.5 නොවේ!)
```
**විසඳුම:** එක අගයක් හෝ `double` බවට පත් කරන්න (Type Casting).
`double answer = (double) a / b;`

## 2. Case Sensitivity (අකුරු වල ප්‍රමාණය)
Java හි Capital සහ Simple අකුරු වල විශාල වෙනසක් ඇත.
* `System.out.println` විය යුතුය (`system` ලෙස ලියන්න එපා).
* `String` විය යුතුය (`string` ලෙස ලියන්න එපා).
* `Scanner` විය යුතුය (`scanner` ලෙස ලියන්න එපා).

## 3. Variable Scope (විචල්‍ය වලංගු සීමාව)
සඟල වරහන් `{ }` ඇතුලේ හදන විචල්‍යයන්, ඉන් පිටතදී භාවිතා කළ නොහැක.
```java
do {
    int option = input.nextInt(); // option හැදුවේ මෙතන
} while (option != 0); // ERROR! option මෙතනට පේන්නේ නෑ.
```
**විසඳුම:** විචල්‍යය අනිවාර්යයෙන්ම වරහනෙන් පිටත ප්‍රකාශ කරන්න.
```java
int option;
do {
    option = input.nextInt();
} while (option != 0);
```

## 4. Scanner Issues
* `input.nextChar()` කියා Method එකක් නැත. -> `input.next().charAt(0);` භාවිතා කරන්න.
* String එකක් ගන්න:
  * වචනයක් ගන්න -> `input.next();`
  * මුළු පේළියම ගන්න -> `input.nextLine();`

## 5. Arrays and Exceptions (අරා දෝෂ)
* **`ArrayIndexOutOfBoundsException`:** Array එකක නැති තැනකින් අගයක් ඉල්ලීම.
  `int[] arr = new int[5];` (මෙහි ඇත්තේ Index 0 සිට 4 දක්වා පමණි). `arr[5]` ඉල්ලුවහොත් මෙම Error එක එයි.
* **`NullPointerException`:** Array එකක් හෝ Object එකක් null (හිස්) වී තිබියදී එය පාවිච්චි කිරීමට යාම.

## 6. Semicolons and Quotes
* හැම Statement එකක්ම ඉවර වෙන්නේ සෙමිකෝලන් (`;`) එකකින්.
* වාක්‍ය (Strings) ලිවීමට අනිවාර්යයෙන්ම **Double Quotes (`""`)** භාවිතා කරන්න. (උදා: `"Hello"`)
* තනි අකුරු (Chars) ලිවීමට **Single Quotes (`''`)** භාවිතා කරන්න. (උදා: `'A'`)

මේ කරුණු ටික හොඳින් මතක තබා ගත්තොත් විභාගයේදී 100/100 ක් ලබා ගැනීම ඉතාමත් පහසුයි!
