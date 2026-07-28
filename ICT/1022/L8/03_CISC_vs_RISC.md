# 03. CISC vs RISC Architecture

> [!NOTE]
> **පසුබිම (Background):** 1970 දශකයේදී Memory (RAM) ඉතා මිල අධික විය. එබැවින් විද්‍යාඥයින් උත්සාහ කළේ ඉතා කෙටි, එහෙත් සංකීර්ණ Instructions (Complex instructions) සෑදීමටයි. මෙය **CISC** විය. නමුත් පසුව Memory ලාභදායී වූ අතර CPU වේගවත් විය. එවිට ඔවුන් තේරුම් ගත්තා "සරල Instructions ගොඩක්" වේගයෙන් Run කිරීම වඩාත් ඵලදායී බව. මෙය **RISC** විය.

---

## 1. CISC (Complex Instruction Set Computer)
පැරණි (Traditional) ප්‍රවේශයයි. මෙහි ප්‍රධාන අරමුණ වූයේ Hardware මඟින් වැඩි කාර්යභාරයක් සිදු කර, Software Instructions සංඛ්‍යාව අඩු කිරීමයි.

### ප්‍රධාන ලක්ෂණ (Main Features):
* **සංකීර්ණ විධාන (Complex instruction set):** එක විධානයකින් කාර්යයන් කිහිපයක් කරයි.
* **බොහෝ Addressing Modes:** (R-R, R-M, M-M, Indexed, Indirect ආදී බොහෝ ක්‍රම ඇත).
* **විශේෂ Registers:** Special-purpose registers සහ Flags (Sign, Zero, Carry) විශාල ප්‍රමාණයක් ඇත.
* **විචල්‍ය දිග (Variable-length instructions):** එක එක Instruction එකේ දිග (Bits ගාණ) වෙනස්‍ ය.
* **සංකීර්ණත්වය:** Instruction එක Decode කිරීම සහ Pipeline එක හදන්න අතිශය අමාරුයි (Complex control unit).
* **උදාහරණ:** IBM 360/370, VAX-11/780, **Intel x86 / Pentium**.

### CISC වල සංකීර්ණත්වයට සජීවී උදාහරණ (Lecture Slides හි ඇති පරිදි):

1. **Pentium (Intel x86) Register Set:** 
   RISC වල වගේ R0, R1 කියන සරල නම් වෙනුවට, CISC වල තියෙන්නේ අතිශය සංකීර්ණ කාර්යයන් සඳහා වෙන් වූ Registers ය.
   * `EAX, EBX, ECX, EDX` (General)
   * `EBP, ESP` (Stack)
   * `EDI, ESI` (Index)
   * `CS, SS, DS, ES, FS, GS` (Segment Registers)
   * `EIP` (Instruction Pointer), `EFLAGS` (Condition Codes)

2. **Addressing Modes in VAX (CISC Machine):**
   VAX වල අතිවිශාල Addressing Modes ප්‍රමාණයක් ඇත. ඒවා නම්: Register direct, Immediate, Displacement, Register indirect, Indexed, Direct, Memory indirect, Autoincrement, Autodecrement, සහ Scaled ය. මෙය Decoding තවත් අමාරු කරයි.

---

## 2. RISC (Reduced Instruction Set Computer)
නවීන ප්‍රවේශයයි. මෙය **Load-Store Architecture** ලෙසද හැඳින්වේ.

### ප්‍රධාන ලක්ෂණ (Main Features):
* **Memory Access සීමිතයි:** Memory එකට යන්න පුළුවන් `LOAD` සහ `STORE` කියන Instructions දෙකට විතරයි! අනිත් හැමදේම කරන්නේ Processor Registers ඇතුලෙමයි.
* **සරල Architecture:** ඉතා පහසුවෙන් Pipelining කළ හැකි සරල සැලසුමකි.
* **අඩු Addressing Modes:** සරල ක්‍රම කිහිපයක් පමණක් ඇත.
* **General Registers:** General-purpose registers විශාල ප්‍රමාණයක් ඇත. Special registers ඉතා අඩුවෙන් ඇත.
* **සමාන දිග (Uniform length):** හැම Instruction එකකම දිග (e.g., 32-bits) සමාන නිසා Decode කරන්න ලේසියි.
* **Compiler මත යැපීම:** සංකීර්ණ වැඩ කරගන්න Compiler එකේ සහය ලබා ගනී.
* **උදාහරණ:** CDC 6600, MIPS family, SPARC, **ARM**.

---

## 3. Comparative Study (සංසන්දනාත්මක අධ්‍යයනය - VAX vs MIPS)

> [!IMPORTANT]
> **Exam Point:** 1991 දී VAX 8700 (CISC) සහ MIPS M2000 (RISC) අතර කළ පරීක්ෂණයේ ප්‍රතිඵල.

| Feature (ලක්ෂණය) | VAX (CISC) | MIPS (RISC) | 
| :--- | :--- | :--- | 
| **Number of Instructions** | අඩුයි (Fewer) | VAX මෙන් **දෙගුණයක් (x2)** විධාන අවශ්‍ය විය. | 
| **Cycles Per Instruction (CPI)**| ගොඩක් වැඩියි | VAX එකේ CPI අගය MIPS වලට වඩා **6 ගුණයක්** විශාල විය. | 
| **Overall Performance** | අඩුයි | MIPS හි ක්‍රියාකාරීත්වය VAX ට වඩා **3 ගුණයක් (x3)** වැඩි විය! | 
| **Hardware Required** | ගොඩක් වැඩියි | ඉතා අඩු Hardware ප්‍රමාණයක් අවශ්‍ය විය. | 

**නිගමනය (Conclusion):** CISC යනු Hardware අතින් අධික වියදම් සහිත සහ Performance අඩු තාක්ෂණයක් බව ඔප්පු විය. (VAX වෙනුවට පසුව ALPHA නම් RISC processor එකක් පැමිණියේය).

---

## 4. ඇයි Intel x86 තවමත් පවතින්නේ? (The Intel Trick)

ලෝකයේ අසාර්ථක වුණත් Intel x86 (CISC) තාම Desktop/Laptops වල පවතින්නේ ඇයි?
1. **Huge Installed Base & Backward Compatibility:** පරණ Software ගොඩක් තියෙන නිසා අලුත් මැෂින් වලත් ඒවා වැඩ කරන්න ඕනේ. වාණිජමය වශයෙන් මෙය ඉතා වැදගත්.
2. **The Internal Trick (සමතුලිත ප්‍රවේශය):**
   * පිටතින් බලන User ට පේන්නේ ඒක **CISC** වගේ.
   * නමුත් ඇතුළත Hardware මඟින් ඒ හැම CISC Instruction එකක්ම **RISC Instructions ගොඩකට Translate (පරිවර්තනය)** කරනවා.
   * ඊටපස්සේ ඇතුළත තියෙන RISC Pipeline එකෙන් ඒක ඉතා වේගයෙන් Execute කරනවා!

> [!TIP]
> **Study Tip:** 
> "CISC uses **Hardware** to translate, RISC uses **Compilers** to translate". මෙය හොඳින් මතක තබාගන්න.
