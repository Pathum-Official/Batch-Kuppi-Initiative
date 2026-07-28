# 04. MIPS32 Architecture & CPU Registers

> [!NOTE]
> **පසුබිම (Background):** RISC Architecture එකට දිය හැකි හොඳම උදාහරණය (Case Study) තමයි MIPS32 කියන්නේ. මේකේ Instruction set එක, Data path එක සහ Pipelining ගැන විභාගයේදී අනිවාර්යයෙන්ම ප්‍රශ්න එනවා.

---

## 1. MIPS32 CPU Registers (මූලික මතකයන්)

Programmer ට පෙනෙන (Visible) ප්‍රධාන Registers වර්ග 3ක් ඇත:

1. **General Purpose Registers (GPRs):**
   * R0 සිට R31 දක්වා 32-bit Registers 32ක් ඇත.
2. **Program Counter (PC):**
   * මීළඟට Fetch කර Execute කළ යුතු Instruction එකේ Address එක මතක තබා ගන්නා 32-bit විශේෂ Register එකයි.
   * මෙය Programmer ට කෙලින්ම වෙනස් කළ නොහැක (Not directly visible). Jump, Branch වැනි විධාන මඟින් වක්‍රව වෙනස් වේ.
3. **HI and LO Registers:**
   * Multiply (ගුණ කිරීම්) සහ Divide (බෙදීම්) වල පිළිතුරු රඳවා ගැනීමට භාවිතා කරන 32-bit Registers දෙකකි.
   * **Multiply (ගුණ කිරීමකදී):** `HI` හි ඉහළ Bits 32 ද, `LO` හි පහළ Bits 32 ද ගබඩා වේ.
   * **Divide (බෙදීමකදී):** `HI` හි ඉතිරිය (Remainder) ද, `LO` හි පිළිතුර (Quotient) ද ගබඩා වේ.

> [!WARNING]
> **Exam Trap (අනිවාර්යයෙන් වරදින තැන):**
> MIPS32 වල සාමාන්‍ය Processors වල තියෙන දේවල් දෙකක් **නැහැ**!
> 1. වෙනම **Stack Pointer (SP) එකක් නැහැ**. ඒ වෙනුවට ඕනෑම GPR එකක් SP ලෙස භාවිතා කළ හැක (PUSH, POP විධාන නැත).
> 2. වෙනම **Flag Registers (ZERO, SIGN, CARRY) නැහැ**. Flags පාවිච්චි කළොත් Pipeline එකට බාධා වෙන නිසා අගයන් සාමාන්‍ය Registers වලම තියාගනී.

---

## 2. Assembly Language Conventions (සම්මත නාමයන්)

> [!IMPORTANT]
> R0 ඉඳන් R31 වෙනකම් Registers තිබ්බට, ලෝකයේ සම්මතයක් විදියට මේවට වෙනත් නම් (Alternate names) භාවිතා කරනවා. **විභාගයේදී මේ නම් අනිවාර්යයෙන්ම මතක තිබිය යුතුයි!**

| Register Name | No. | Usage (භාවිතය - සිංහලෙන්) | English Meaning |
| :---: | :---: | :--- | :--- |
| **`$zero`** | R0 | සැමවිටම අගය **0** වේ. කොතරම් උත්සාහ කළත් වෙනස් කළ නොහැක. (ශුන්‍යය අවශ්‍ය තැන් වලට ගනී). | Hard-wired constant zero. |
| **`$at`** | R1 | Assembler එක විසින් තාවකාලිකව භාවිතා කරයි. අපිට පාවිච්චි කරන්න බෑ. | Reserved for assembler. |
| **`$v0`, `$v1`** | R2, R3 | Function එකකින් එළියට දෙන පිළිතුරු (Return values) 2ක් දක්වා තියාගන්න. | Result of function / expression. |
| **`$a0` - `$a3`** | R4-R7 | Function එකකට යවන අගයන් (Arguments 4ක් දක්වා) තියාගන්න. | Arguments 1 to 4. |
| **`$t0` - `$t9`** | - | තාවකාලික වැඩ වලට. Function call එකකදී මේවා මැකෙන්න පුළුවන්. | Temporary (Not preserved across calls). |
| **`$s0` - `$s7`** | - | මේවත් තාවකාලික වැඩ වලට. හැබැයි Function call එකක් කරත් මේවා මැකෙන්නේ නෑ. | Temporary (Preserved across calls). |
| **`$gp`** | R28 | Global variables තියෙන තැන (Global area) පෙන්වයි. | Pointer to global area. |
| **`$sp`** | R29 | **Stack එකේ උඩම තැන (Top of stack)** පෙන්වයි. | Stack pointer. |
| **`$fp`** | R30 | Stack එකේ Activation record පෙන්වයි. | Frame pointer. |
| **`$ra`** | R31 | **Return address** (Function එකකින් ආපහු එන්න ඕනේ Address එක තියාගන්නවා. `JAL` මඟින් මෙය පිරවේ). | Return address. |
| **`$k0`, `$k1`** | R26, R27 | OS Kernel එකට වෙන් කරලා තියෙන්නේ. (භාවිතා කිරීම නිර්දේශ නොකරයි). | Reserved for OS kernel. |

> [!TIP]
> **Study Tip:** මෙහිදී `$zero` (R0), `$ra` (R31) සහ `$sp` අනිවාර්යයෙන්ම මතක තබා ගන්න!

---

## 3. MIPS32 Assembly Code Examples (සැබෑ උදාහරණ)

> [!TIP]
> **Study Tip:** විභාගයේදී MIPS කේතයක් ලබා දී එහි ප්‍රතිඵලය කුමක්දැයි ඇසිය හැක. මෙහිදී භාවිතා වන `LD` (Load Double), `SD` (Store Double), `JAL` (Jump and Link), `JR` (Jump Register) විධාන හොඳින් අධ්‍යයනය කරන්න.

* **Memory එකෙන් Register එකට ගෙන ඒම (Load):**
  `LD R4, 50(R3)`  --> අදහස: `R4 = Mem[50 + R3]`
* **Registers දෙකක් එකතු කිරීම (Add):**
  `ADD R2, R1, R4` --> අදහස: `R2 = R1 + R4`
* **Register එකෙන් Memory එකට යැවීම (Store):**
  `SD 54(R3), R2`  --> අදහස: `Mem[54 + R3] = R2`
* **නියතයක් (Constant) එකතු කිරීම (Add Immediate):**
  `ADDI R1, R0, 35` --> අදහස: `R1 = 0 + 35` ($zero හෙවත් R0 යනු ශුන්‍යයයි)

**Function Call එකක් සිදු කරන ආකාරය (JAL & JR භාවිතය):**
```assembly
MAIN: 
    ADDI R1, R0, 35    // R1 = 35
    ADDI R2, R0, 56    // R2 = 56
    JAL GCD            // GCD Function එකට Jump කරන්න. (R31 ට Return Address එක සේව් වේ).
    
GCD: 
    .....              // GCD සෙවීමේ කේතය
    JR R31             // Function එක අවසන් වී ආපසු MAIN වෙත යාමට R31 (Return Address) භාවිතා කරයි.
```
