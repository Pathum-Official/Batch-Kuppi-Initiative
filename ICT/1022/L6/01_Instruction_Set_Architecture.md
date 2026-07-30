# 📜 Instruction Set Architecture (ISA)

පරිගණකයක දෘඪාංග (Hardware) සහ මෘදුකාංග (Software) අතර සම්බන්ධතාවය ගොඩනඟන ප්‍රධානතම අතුරුමුහුණත (Interface) වන්නේ **Instruction Set Architecture (ISA)** යි.

> [!NOTE]
> ISA එකක් යනු Programmer කෙනෙකුට පරිගණකය පෙනෙන ආකාරයයි (Programmer's view). මෙයට රෙජිස්ටර්, බස් (Buses) සහ පරිගණකයට ලබා දිය හැකි සියලුම උපදෙස් මාලාව (Instruction set) අයත් වේ.

ISA එකක් යනු කිසියම් නිශ්චිත පරිගණකයකට පමණක් සීමා වූවක් නොවේ. හොඳ ISA එකක් පරම්පරා ගණනාවක් පුරා භාවිතා වේ (Survive across generations). 
* *උදාහරණ:* Intel x86 series, IBM 360 series.

---

## 🛠️ උපදෙස් මාලාවක් සැලසුම් කිරීමේදී ඇතිවන ගැටළු (Instruction Set Design Issues)

නව ISA එකක් නිර්මාණය කිරීමේදී ප්‍රධාන කරුණු කිහිපයක් ගැන තීරණ ගත යුතුය:

1. **Operands ගණන (Number of explicit operands):**
   * එක් උපදෙසක පැහැදිලිව දැක්විය යුතු දත්ත (Operands) කීයක් තිබේද? (0, 1, 2 හෝ 3 විය හැක).
2. **Operands පිහිටන ස්ථානය (Location):**
   * දත්ත ලබා ගත යුත්තේ කොතැනින්ද? (Registers, Accumulator, හෝ Memory).
3. **ලිපින ක්‍රමය (Specification of operand locations):**
   * දත්තය ඇති තැන දක්වන්නේ කෙසේද? (Addressing modes: Immediate, Direct, Indirect, ආදිය).
4. **දත්තවල ප්‍රමාණය (Sizes of operands supported):**
   * බිට් 8 (Byte), බිට් 16 (Half-word), බිට් 32 (Word), බිට් 64 (Double).
5. **සහාය දක්වන ක්‍රියාකාරකම් (Supported operations):**
   * එකතු කිරීම, අඩු කිරීම, තර්කන ක්‍රියා ආදිය (ADD, SUB, MUL, AND, OR, CMP, MOVE, JMP).
