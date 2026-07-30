# 🗄️ Memory Characteristics & Classification

පරිගණකයක උපදෙස් සහ දත්ත ගබඩා කිරීමේ ප්‍රධානතම ඒකකය වන්නේ මතකයයි (Memory). මෙය ප්‍රොසෙසරයට සම්බන්ධ වන්නේ ප්‍රධාන බස් (Buses) 3 ක් හරහාය:
1. **Address Bus:** දත්තය ඇති ස්ථානයේ ලිපිනය ගෙන යයි.
2. **Data Bus:** දත්ත එහා මෙහා ගෙන යයි (Bidirectional).
3. **Control Bus:** කියවන්නද, ලියන්නද යන්න (READ/WRITE) උපදෙස් ලබා දෙයි.

---

## 1. මතක චිපයක මූලික ව්‍යුහය (Memory Module)

මතක චිපයක් නිර්මාණය වී ඇත්තේ මතක කෝෂ (Memory cells) අරාවක් ලෙසිනි. සෑම කෝෂයකම එක් බිට් එකක් (1 bit) ගබඩා කළ හැක.

* **Address lines ($n$):** ලිපින මාර්ග $n$ ගණනක් තිබේ නම්, උපරිම මතක ස්ථාන $2^n$ ක් සෑදිය හැක. (ඒ සඳහා $n \times 2^n$ Decoder එකක් භාවිතා කරයි).
* **Data lines ($m$):** එකවර යැවිය හැකි හෝ ලබාගත හැකි බිට් ගණන.
* **CS (Chip Select):** මෙම චිපය ක්‍රියාත්මක කරන්නද නැද්ද යන්න තීරණය කරයි.

> [!EXAMPLE]
> **256 x 16 Memory චිපයකට අවශ්‍ය මුළු කටු (Pins / Connections) ගණන සෙවීම:**
> * $256$ යනු ස්ථාන ගණනයි ($2^8$). එබැවින් Address සඳහා pins $8$ කි.
> * $16$ යනු Data ප්‍රමාණයයි. එබැවින් Data සඳහා pins $16$ කි.
> * Read/Write සඳහා $1$ යි.
> * Chip Select (CS) සඳහා $1$ යි.
> * Power සහ Ground සඳහා $2$ යි.
> * **මුළු ගණන:** $8 + 16 + 1 + 1 + 2 = 28$ pins.

---

## 2. මතකය වර්ග කිරීම (Classification)

### A. Volatile vs Non-volatile
* **Volatile Memory:** විදුලිය විසන්ධි වූ විට දත්ත මැකී යයි. (උදා: SRAM, DRAM).
* **Non-volatile Memory:** විදුලිය විසන්ධි වූවත් දත්ත මැකී නොයයි. (උදා: ROM, Hard Disk, Flash Memory).

### B. Access Method (ප්‍රවේශ වන ආකාරය)
* **Random-access:** ඕනෑම තැනක ඇති දත්තයක් එකම වේගයකින් ලබාගත හැක (උදා: RAM).
* **Sequential-access:** දත්ත ලබාගත යුත්තේ පිළිවෙළකටය. අග ඇති දත්තයක් ගැනීමට කල් ගතවේ (උදා: Magnetic tape).
* **Direct-access:** යම්කිසි කොටසකට කෙලින්ම ගොස්, එතැන් සිට පිළිවෙළට කියවයි (උදා: Hard Disk).

### C. RAM vs ROM
* **RAM (Random Access Memory):** කියවීමට මෙන්ම ලිවීමටද හැක. 
  * *SRAM (Static RAM):* ඉතා වේගවත්ය. විදුලිය ඇති තාක් දත්ත පවතී. (Cache memory සඳහා භාවිතා කරයි).
  * *DRAM (Dynamic RAM):* SRAM වලට වඩා ලාභදායී වුවත් මන්දගාමී වේ. මෙහි දත්ත රැඳී තිබීමට නිතරම Refresh කළ යුතුය.
* **ROM (Read Only Memory):** දත්ත වෙනස් කළ නොහැක. (උදා: PROM, EEPROM).
