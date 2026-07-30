# 🏗️ Multilevel Machine Concept

නවීන පරිගණක නිර්මාණය කර ඇත්තේ ස්තර කිහිපයකින් (Levels) සමන්විත වූ "Multilevel Machine" එකක් ලෙසයි. පරිගණකයක වාස්තු විද්‍යාව තේරුම් ගැනීමට මෙය ඉතා වැදගත් සංකල්පයකි.

> [!IMPORTANT]
> **මූලික රීතිය:** ඉලෙක්ට්‍රොනික පරිපථ (Electronic circuits) වලට සෘජුවම කිසිදු පරිවර්තනයකින් තොරව ක්‍රියාත්මක කළ හැක්කේ **Level 0 (L0)** හි ඇති භාෂාවෙන් ලියූ වැඩසටහන් පමණි.

වෙනත් ඕනෑම භාෂාවකින් (L1, L2... Ln) ලියන වැඩසටහන් ක්‍රියාත්මක කිරීමට පෙර, පහළ මට්ටමේ භාෂාවකට (Lower-level language) පරිවර්තනය කිරීම හෝ අර්ථකථනය කිරීම (Interpreted) කළ යුතුමය.

---

## 🏢 Six-Level Machine Architecture (ස්තර 6කින් යුත් පරිගණක ව්‍යුහය)

පරිගණකයක ඇති ප්‍රධාන ස්තර 6 පහත පරිදි වේ:

### Level 0: Digital Logic Level (ඩිජිටල් තාර්කික ස්තරය)
* මෙය පරිගණකයේ පහළම මට්ටමයි (Hardware).
* මෙහිදී දත්ත සැකසීම සිදුවන්නේ **Logic Gates** (AND, OR ආදිය) භාවිතයෙනි. 

### Level 1: Microarchitecture Level (ක්ෂුද්‍ර වාස්තු විද්‍යා ස්තරය)
* CPU එක ඇතුළත ඇති Local memory (Registers) සහ ALU (Arithmetic Logic Unit) මෙයට අයත් වේ.
* දත්ත සහ ගණනය කිරීම් සිදුවන්නේ මෙම ස්තරයේදීය.

### Level 2: Instruction Set Architecture (ISA) Level
* මෙය පරිගණකයේ අත්පොත (Manual for the computer) ලෙස හැඳින්වේ. 
* Programmer කෙනෙකුට ලබා දිය හැකි සියලුම උපදෙස් (Instructions) සහ ඒවායේ හැඩය (Format) මෙහි අඩංගු වේ.

### Level 3: Operating System Machine Level (මෙහෙයුම් පද්ධති ස්තරය)
* මෙහෙයුම් පද්ධතිය (OS) මඟින් Hardware, Memory, CPU සහ Peripherals සෘජුවම පාලනය කරයි.
* පරිශීලකයින්ට (Users) සේවා සහ Interface ලබා දෙන්නේ මෙම ස්තරය හරහාය.

### Level 4: Assembly Language Level (ඇසෙම්බ්ලි භාෂා ස්තරය)
* Level 1, 2 සහ 3 සඳහා මිනිසුන්ට තේරුම් ගත හැකි අයුරින් වැඩසටහන් ලිවීමට මෙම ස්තරය පහසුකම් සලසයි.
* යන්ත්‍ර භාෂාවට වඩා මෙය ලිවීමට සහ කියවීමට පහසුය.

### Level 5: Problem-Oriented Language Level (ගැටළු-අභිමුඛ භාෂා ස්තරය)
* මෙය අප එදිනෙදා භාවිතා කරන High-Level Languages වලින් සමන්විත වූ ඉහළම ස්තරයයි.
* **උදාහරණ:** JAVA, C, C++, Python.

---

> [!TIP]
> **Programmers vs Designers:** 
> බොහෝ Programmers ලා අවධානය යොමු කරන්නේ ඉහළම ස්තරය (Level 5) ගැන පමණි. නමුත් නව පරිගණකයක් නිර්මාණය කරන Designer කෙනෙකුට මෙම **ස්තර 6 ගැනම මනා අවබෝධයක්** තිබීම අනිවාර්ය වේ.
