# 🗂️ MIPS32 Instruction Categories

MIPS32 යනු Load-Store ආකෘතිය (RISC) භාවිතා කරන ප්‍රොසෙසරයකි. මෙහි ඇති **සියලුම උපදෙස් බිට් 32 කින් (32 bits)** සමන්විත වේ.

MIPS32 හි ඇති උපදෙස් ප්‍රධාන කාණ්ඩ කිහිපයකට බෙදිය හැක:

---

## 1. Load and Store Instructions (දත්ත ලබාගැනීම සහ ගබඩා කිරීම)
MIPS32 හි මතකයට (Memory) පිවිසිය හැක්කේ Load සහ Store උපදෙස් වලට පමණි. අනෙක් සියලුම ගණනය කිරීම් සිදුවන්නේ රෙජිස්ටර් තුළය.

* **Size එක අනුව:**
  * Word (බිට් 32): `LW`, `SW`
  * Half-word (බිට් 16): `LH`, `SH`
  * Byte (බිට් 8): `LB`, `SB`
* **ලකුණ (Sign) අනුව:**
  * සාමාන්‍යයෙන් Load කිරීමේදී Sign Extension සිදුවේ (Signed).
  * ලකුණ අවශ්‍ය නැත්නම් Unsigned ලෙස Load කළ හැක (උදා: `LHU`, `LBU`).

> [!NOTE]
> **Alignment of Words (වචන පෙළගැස්ම):** 
> MIPS වල මතකයෙන් Word එකක් කියවීමේදී එය 4 න් බෙදෙන ලිපිනයකින් (Power of 4) ආරම්භ විය යුතුමය. (එනම් ලිපිනයේ අග බිට් දෙක 00 විය යුතුය). මෙසේ පෙළගස්වා ඇති විට එක් ඔරලෝසු චක්‍රයකින් (Single cycle) දත්තය ලබා ගත හැක.

---

## 2. Arithmetic and Logic Instructions (ගණිතමය සහ තර්කන)
මේවා ක්‍රියාත්මක වන්නේ රෙජිස්ටර් මත පමණි.

* **3-Operand (දත්ත 3 ක් අවශ්‍ය ඒවා):**
  * `ADD`, `SUB`, `AND`, `OR`, `XOR`, `NOR` 
  * `SLT` (Set on Less Than - එකක් අනෙකට වඩා කුඩාදැයි බැලීමට)
* **Immediate (නියත අගයන් සමඟ ක්‍රියා කරන ඒවා):**
  * උපදෙසේම අංකයක් අඩංගු වේ (16-bit). අගට `I` අකුර යොදයි.
  * `ADDI`, `ANDI`, `ORI`, `LUI` (Load Upper Immediate)
* **Shift (බිට් මාරු කිරීම):**
  * `SLL` (Shift Left Logical), `SRL` (Shift Right Logical), `SRA` (Shift Right Arithmetic)

---

## 3. Jump and Branch Instructions (තීරණ ගැනීම සහ පැනීම)
වැඩසටහනක සාමාන්‍ය ගමන් මාර්ගය වෙනස් කිරීමට මේවා භාවිතා කරයි.

* **PC-Relative Conditional Branch:**
  * යම් කොන්දේසියක් සත්‍ය නම් පමණක් වෙනත් තැනකට යයි.
  * රෙජිස්ටර් දෙකක් සසඳන: `BEQ` (Branch on Equal), `BNE` (Not Equal)
  * බිංදුව සමඟ සසඳන: `BGEZ` (Greater Than or Equal to Zero), `BGTZ`, `BLEZ`
* **Unconditional Jump:**
  * කොන්දේසියක් නොමැතිව කෙලින්ම වෙනත් තැනකට යයි.
  * `J` (Jump), `JAL` (Jump and Link - Function call වලදී Return address එක R31 හි ගබඩා කරයි).
* **Absolute Register Jump:**
  * රෙජිස්ටරයක ඇති ලිපිනයකට පැනීම. `JR` (Jump Register).

---

## 4. Miscellaneous & Coprocessor (විවිධ සහ සහායක)
* **Miscellaneous:** Exception හැසිරවීමට, `NOP` (කිසිවක් නොකර සිටීම).
* **Coprocessor:** MIPS හි සහායක ප්‍රොසෙසර 4 ක් ඇත. `CP0` (System Control, Exceptions හැසිරවීමට), `CP1` (Floating point සඳහා).
