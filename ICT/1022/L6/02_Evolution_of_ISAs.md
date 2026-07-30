# 📈 Evolution of Instruction Sets

කාලයත් සමඟ පරිගණක උපදෙස් මාලාවන් (Instruction sets) ප්‍රධාන වර්ග 5 ක් හරහා පරිණාමය වී ඇත.

---

## 1. Accumulator Based Architecture (1960 ගණන්වල)
මෙම ක්‍රමයේදී, සියලුම ගණනය කිරීම් සඳහා එක් විශේෂිත රෙජිස්ටරයක් භාවිතා කරයි. එය **Accumulator (ACC)** ලෙස හැඳින්වේ. සෑම උපදෙසකදීම එක් දත්තයක් සහ පිළිතුර සැමවිටම ඇත්තේ ACC එක තුළ බව උපකල්පනය කරයි (One of the operands is implicitly the accumulator).

> [!EXAMPLE]
> **කාර්යය:** `Z = X + Y`
> ```assembly
> LOAD X    // ACC = Mem[X] (X හි අගය ACC එකට ගනී)
> ADD Y     // ACC = ACC + Mem[Y] (Y හි අගය ACC එකට එකතු කරයි)
> STORE Z   // Mem[Z] = ACC (පිළිතුර Z හි ගබඩා කරයි)
> ```

---

## 2. Stack Based Architecture (1960-1970)
මෙහිදී දත්ත රඳවා තබා ගැනීමට **Stack (ස්ටැක්)** එකක් භාවිතා කරයි. මෙහි Operands කිසිවක් උපදෙසේ ලියන්නේ නැත (0-address instructions). ගණනය කිරීම සඳහා Stack එකේ ඉහළින්ම ඇති අගයන් දෙක (Top of Stack) ස්වයංක්‍රීයව භාවිතා කරයි.

> [!EXAMPLE]
> **කාර්යය:** `Z = X + Y`
> ```assembly
> PUSH X    // X අගය Stack එකට දමයි
> PUSH Y    // Y අගය Stack එකට දමයි
> ADD       // Stack එකේ උඩින්ම ඇති දෙක (X සහ Y) ගෙන එකතු කර, පිළිතුර නැවත Stack එකට දමයි
> POP Z     // Stack එකෙන් පිළිතුර අරන් Z හි ගබඩා කරයි
> ```

---

## 3. Memory-Memory Based Architecture (1970-1980)
මෙහිදී උපදෙස් වලට අදාළ සියලුම දත්ත (Operands) ලබා ගන්නේ සහ ගබඩා කරන්නේ කෙලින්ම **මතකයෙනි (Memory)**. (මෙහි Registers භාවිතයක් නැත). මෙය Operands 2ක් හෝ 3ක් සහිතව ලිවිය හැක.

> [!EXAMPLE]
> **කාර්යය:** `Z = X + Y`
> ```assembly
> // Operands 3ක් භාවිතා කිරීම:
> ADD Z, X, Y  // X සහ Y එකතු කර Z හි ගබඩා කරයි
> 
> // Operands 2ක් භාවිතා කිරීම:
> MOV Z, X     // X හි අගය Z ට දමයි
> ADD Z, Y     // Z හි අගයට Y එකතු කර Z හිම ගබඩා කරයි
> ```

---

## 4. Register-Memory Based Architecture (1970-අද දක්වා)
එක් දත්තයක් රෙජිස්ටරයක ද (Register), අනෙක් දත්තය මතකයේ ද (Memory) ඇති බව උපකල්පනය කර ගණනය කිරීම් සිදු කරයි. (Intel x86 processors වල මෙය භාවිතා වේ).

> [!EXAMPLE]
> **කාර්යය:** `Z = X + Y`
> ```assembly
> LOAD R1, X     // X හි අගය R1 රෙජිස්ටරයට ගනී
> ADD R1, Y      // R1 වලට Y අගය (මතකයෙන් ගෙන) එකතු කරයි
> STORE Z, R1    // පිළිතුර R1 හි සිට Z මතක ස්ථානයට යවයි
> ```

---

## 5. Register-Register (Load-Store) Architecture (1960-අද දක්වා)
මෙහිදී සියලුම ගණනය කිරීම් (ALU operations) සිදු කරන්නේ **රෙජිස්ටර් අතර පමණි**. මතකයට (Memory) පිවිසිය හැක්කේ `LOAD` සහ `STORE` යන උපදෙස් දෙකට පමණි. (මෙය MIPS වැනි RISC Architecture වල භාවිතා වේ).

> [!EXAMPLE]
> **කාර්යය:** `Z = X + Y`
> ```assembly
> LOAD R1, X       // X හි අගය R1 ට ගනී
> LOAD R2, Y       // Y හි අගය R2 ට ගනී
> ADD R3, R1, R2   // R1 සහ R2 එකතු කර පිළිතුර R3 හි ගබඩා කරයි
> STORE Z, R3      // R3 හි අගය Z මතක ස්ථානයේ ගබඩා කරයි
> ```
