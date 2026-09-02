# 01. Java Data Types & Operators (දත්ත වර්ග සහ කර්මක)

## 1. Primitive Data Types (මූලික දත්ත වර්ග)
Java වල ප්‍රධාන Data Types 8ක් ඇත. විභාගයේදී මේවායේ මතක ප්‍රමාණය (Bit size) ඇසීමට ඉඩ ඇත.

| Data Type | Size (Bits) | Description (විස්තරය) | Example |
| :--- | :--- | :--- | :--- |
| `byte` | 8-bit | ඉතා කුඩා පූර්ණ සංඛ්‍යා (-128 to 127) | `byte a = 100;` |
| `short` | 16-bit | කුඩා පූර්ණ සංඛ්‍යා | `short b = 10000;` |
| `int` | 32-bit | සාමාන්‍ය පූර්ණ සංඛ්‍යා (Standard Integer) | `int c = 100000;` |
| `long` | 64-bit | විශාල පූර්ණ සංඛ්‍යා (අගට 'L' දැමිය යුතුය) | `long d = 15000000000L;` |
| `float` | 32-bit | කුඩා දශම සංඛ්‍යා (අගට 'f' දැමිය යුතුය) | `float e = 10.5f;` |
| `double` | 64-bit | විශාල දශම සංඛ්‍යා (Standard Decimal) | `double f = 10.5;` |
| `char` | 16-bit | තනි අකුරක් හෝ සංකේතයක් (Single quotes `''`) | `char g = 'A';` |
| `boolean` | 1-bit | සත්‍ය හෝ අසත්‍ය (true / false) | `boolean h = true;` |

## 2. Operators (කර්මක)

### A. Arithmetic Operators (ගණිතමය)
`+`, `-`, `*`, `/` (බෙදීම), `%` (Modulo - බෙදූ පසු ඉතිරිය)

### B. Relational Operators (සංසන්දනාත්මක)
`==` (සමානයි), `!=` (අසමානයි), `>`, `<`, `>=`, `<=`

### C. Logical Operators (තාර්කික)
| Operator | Name | Meaning | Example |
| :--- | :--- | :--- | :--- |
| `&&` | Logical AND | දෙකම True නම් පමණක් True වේ | `(5 > 3 && 8 > 5)` -> True |
| `||` | Logical OR | එකක් හෝ True නම් True වේ | `(5 > 3 || 2 > 5)` -> True |
| `!` | Logical NOT | True නම් False කරයි, False නම් True කරයි | `!(5 > 3)` -> False |

### D. Increment / Decrement Operators
* `++a` (Pre-increment): කලින්ම එකතු කර පසුව අගය ලබා දෙයි.
* `a++` (Post-increment): අගය ලබා දී පසුව එකතු කරයි.

## 3. Operator Precedence (ප්‍රමුඛතා අනුපිළිවෙල)
ගණිතයේ BODMAS වගේ Java වලත් පිළිවෙලක් ඇත (ඉහළ සිට පහළට ප්‍රමුඛතාවය අඩුවේ):
1. `()` - වරහන් (Parentheses)
2. `++`, `--` - Increment/Decrement
3. `*`, `/`, `%` - ගුණ කිරීම, බෙදීම, Modulo (වමේ සිට දකුණට)
4. `+`, `-` - එකතු කිරීම, අඩු කිරීම
5. `>`, `<`, `>=`, `<=` - Relational
6. `==`, `!=` - Equality
7. `&&` - Logical AND
8. `||` - Logical OR
9. `=`, `+=`, `-=` - Assignment
