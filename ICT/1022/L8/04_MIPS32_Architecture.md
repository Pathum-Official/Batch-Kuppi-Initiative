# 04. MIPS32 Architecture & CPU Registers

> [!NOTE]
> **පසුබිම (Background):** RISC Architecture එකට දිය හැකි හොඳම උදාහරණය (Case Study) තමයි MIPS32 කියන්නේ. මේකේ Instruction set එක, Data path එක සහ Pipelining ගැන විභාගයේදී අනිවාර්යයෙන්ම ප්‍රශ්න එනවා.

---

## 💡 ප්‍රායෝගික උදාහරණය (Real-World Analogy)

CPU එක ඇතුලේ තියෙන **Registers** කියන්නේ හරියට "පාසල් ළමයින්ගේ Lockers (කබඩ්)" වගේ. 
* **GPRs (General Purpose Registers):** මේවා සාමාන්‍ය ළමයින්ගේ කබඩ් 32ක් වගේ. ඕනෑම කෙනෙක්ට පොත් (Data) දාන්න ගන්න පුළුවන්. 
* **PC (Program Counter):** මේක හරියට "ඊළඟට උගන්නන්න තියෙන පාඩම" ගහලා තියෙන Notice Board එකක් වගේ. 
* **HI & LO:** මේ කබඩ් දෙක ලොකු ගණන් හදද්දි උත්තරේ කෑලි දෙකට කඩලා දාන්න වෙන් කරපු විශේෂ කබඩ් දෙකක්.

<div align="center">
  <img src="mips32_registers.png" alt="MIPS32 Registers Analogy" width="100%" style="max-width: 650px; border-radius: 12px; box-shadow: 0 8px 25px rgba(0,0,0,0.15); margin: 20px 0 10px;">
  <br>
  <em><small style="color: #64748b;">රූප සටහන 1: CPU එක ඇතුළත ඇති Registers (Lockers)</small></em>
</div>

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
> MIPS32 වල සාමාන්‍ය Processors (උදා: Intel x86) වල තියෙන දේවල් දෙකක් **නැහැ**!
>
> 1. වෙනම **Stack Pointer (SP) එකක් නැහැ**. ඒ වෙනුවට ඕනෑම GPR එකක් SP ලෙස භාවිතා කළ හැක (සාමාන්‍යයෙන් R29 භාවිතා කරයි). PUSH, POP විධාන නැත.
> 2. වෙනම **Flag Registers (ZERO, SIGN, CARRY) නැහැ**. Flags පාවිච්චි කළොත් Pipeline එකට බාධා වෙන නිසා අගයන් සාමාන්‍ය Registers වලම තියාගනී.

---

## 2. Assembly Language Conventions (සම්මත නාමයන්)

> [!IMPORTANT]
> R0 ඉඳන් R31 වෙනකම් Registers තිබ්බට, ලෝකයේ සම්මතයක් විදියට මේවට වෙනත් නම් (Alternate names) භාවිතා කරනවා. **විභාගයේදී මේ නම් අනිවාර්යයෙන්ම මතක තිබිය යුතුයි!**

| Register Name | No. | Usage (භාවිතය - සිංහලෙන්) | English Meaning |
| :---: | :---: | :--- | :--- |
| **`$zero`** | R0 | සැමවිටම අගය **0** වේ. කොතරම් උත්සාහ කළත් වෙනස් කළ නොහැක. | Hard-wired constant zero. |
| **`$at`** | R1 | Assembler එක විසින් තාවකාලිකව භාවිතා කරයි. අපිට පාවිච්චි කරන්න බෑ. | Reserved for assembler. |
| **`$v0`, `$v1`** | R2, R3 | Function එකකින් එළියට දෙන පිළිතුරු (Return values). | Result of function. |
| **`$a0` - `$a3`** | R4-R7 | Function එකකට යවන අගයන් (Arguments). | Arguments 1 to 4. |
| **`$t0` - `$t9`** | - | තාවකාලික වැඩ වලට. (Function call එකකදී මැකෙන්න පුළුවන්). | Temporary (Not preserved). |
| **`$s0` - `$s7`** | - | මේවත් තාවකාලික වැඩ වලට. හැබැයි Function call එකකදී මැකෙන්නේ නෑ. | Saved (Preserved across calls). |
| **`$gp`** | R28 | Global variables තියෙන තැන පෙන්වයි. | Pointer to global area. |
| **`$sp`** | R29 | **Stack එකේ උඩම තැන (Top of stack)** පෙන්වයි. | Stack pointer. |
| **`$fp`** | R30 | Stack එකේ Activation record පෙන්වයි. | Frame pointer. |
| **`$ra`** | R31 | **Return address** (Function එකකින් ආපහු එන්න ඕනේ Address එක). | Return address. |

> [!TIP]
> **Study Tip:** මෙහිදී `$zero` (R0), `$ra` (R31) සහ `$sp` අනිවාර්යයෙන්ම මතක තබා ගන්න!

---

## 3. MIPS32 Assembly Code Examples (සැබෑ උදාහරණ)

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
    JAL GCD            // GCD Function එකට Jump කරන්න. (R31 / $ra ට Return Address එක සේව් වේ).
  
GCD: 
    .....              // GCD සෙවීමේ කේතය
    JR R31             // Function එක අවසන් වී ආපසු MAIN වෙත යාමට R31 (Return Address) භාවිතා කරයි.
```

---

## 🎓 Exam Q&A (මහාචාර්ය මට්ටමේ ප්‍රශ්න සහ පිළිතුරු)

> [!TIP]
> විභාගයේදී මේ ප්‍රශ්න හරහා ඔයාගේ තර්කන හැකියාව පරීක්ෂා කරනු ඇත.

**Q1: Why doesn't the MIPS32 architecture have dedicated PUSH and POP instructions for Stack operations?**
(MIPS32 හි Stack සඳහා වෙනම PUSH සහ POP විධාන නැත්තේ ඇයි?)
* **Answer:** MIPS follows a strict RISC philosophy where simplicity is key. Instead of creating complex, dedicated PUSH/POP instructions, it expects the compiler to use standard `Load` and `Store` instructions along with arithmetic instructions (to increment/decrement the Stack Pointer `$sp`) to achieve the same result. This keeps the hardware simple and fast.

**Q2: What is the purpose of the HI and LO registers in MIPS? Explain with an example.**
(HI සහ LO Registers වල ප්‍රයෝජනය කුමක්ද? උදාහරණයක් සහිතව පැහැදිලි කරන්න.)
* **Answer:** When multiplying two 32-bit numbers, the result can be up to 64 bits long, which cannot fit into a single 32-bit GPR. Therefore, MIPS uses the `HI` and `LO` registers to hold the 64-bit result (`HI` gets the upper 32 bits, `LO` gets the lower 32 bits). Similarly, for division, `HI` holds the remainder, and `LO` holds the quotient.

**Q3: Explain the role of `$ra` (Register 31) when a function call is made using the `JAL` instruction.**
(`JAL` විධානය හරහා Function call එකක් කිරීමේදී `$ra` හෙවත් Register 31 හි කාර්යභාරය පැහැදිලි කරන්න.)
* **Answer:** `JAL` stands for "Jump And Link". When calling a function, the CPU needs to remember where to return after the function finishes. The `JAL` instruction automatically saves the address of the next instruction (the Return Address) into `$ra` (Register 31). Inside the function, the `JR $ra` (Jump Register) instruction is used to jump back to that saved address.

**Q4: If a programmer accidentally writes a value into `$zero` (R0), what happens?**
(ක්‍රමලේඛකයෙක් අත්වැරදීමකින් `$zero` වෙත අගයක් ආදේශ කළහොත් කුමක් සිදුවේද?)
* **Answer:** **Nothing happens.** The `$zero` register is hardware-wired to always contain the constant value `0`. Any attempt to write data into it is simply ignored by the processor. This is very useful for synthesizing instructions like copying values (`ADD R1, R2, $zero` effectively means `R1 = R2`).
