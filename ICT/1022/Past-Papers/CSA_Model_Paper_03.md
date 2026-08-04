# 📘 CSA Model Paper 03 (Performance, Pipelining, & Advanced Data)

මෙය Advanced කොටස් ආවරණය කරමින් සකසා ඇති අවසාන (තෙවන) අනුමාන ප්‍රශ්න පත්‍රයයි. මෙහිදී ගණනය කිරීම් සහ Pipelining වැනි සංකීර්ණ කොටස් සාකච්ඡා කෙරේ. මෙහි සෑම ප්‍රශ්නයකම නිවැරදි සිංහල පරිවර්තනය සහ පැහැදිලි කිරීම් අඩංගු කර ඇත.

---

## 📝 Question 01 [30 Marks]
**📌 ආවරණය වන දේශන:** L7 (Number Systems)

### 🔹 Part (i) - Number Representation (15 Marks)

> [!TIP]
> **Short Note: Floating Point (IEEE 754)**
> 32 bits total = 1 Sign bit + 8 Exponent bits + 23 Mantissa bits.

#### a. Briefly explain the IEEE 754 Single Precision Floating-Point format. [6 marks]
**❓ සිංහල පරිවර්තනය:** IEEE 754 තනි නිරවද්‍යතා පාවෙන ලක්ෂ්‍ය (Single Precision Floating-Point) ආකෘතිය කෙටියෙන් පැහැදිලි කරන්න.
**💡 පැහැදිලි කිරීම:** මේකෙන් අහන්නේ දශම සංඛ්‍යා (decimals) පරිගණකය ඇතුළේ bit 32 කින් ලියන සම්මත ක්‍රමය ගැන. මේ bit 32 ප්‍රධාන කොටස් 3 කට (Sign, Exponent, Mantissa) බෙදෙන විදිහ ගැන ලියන්න ඕනේ.

**✍️ Exam Answer:**
* It is a standardized 32-bit format used by modern computers to represent real numbers (fractions/decimals) in binary.
* The 32 bits are divided into three distinct fields:
  1. **Sign bit (1 bit):** Bit 31. It indicates whether the number is positive (0) or negative (1).
  2. **Exponent (8 bits):** Bits 30-23. It represents the power of 2, stored using an excess/biased format (typically biased by 127) to easily handle both positive and negative exponents.
  3. **Mantissa / Fraction (23 bits):** Bits 22-0. It stores the significant digits (the precision) of the number in a normalized scientific format.
* **🎯 Marking Scheme:** 2 marks per field accurately described.

#### b. Convert the decimal number -25 into an 8-bit signed magnitude representation and an 8-bit 2's complement representation. [9 marks]
**❓ සිංහල පරිවර්තනය:** -25 යන දශම සංඛ්‍යාව 8-bit සලකුණු කළ විශාලත්ව (signed magnitude) නිරූපණයකට සහ 8-bit 2's complement නිරූපණයකට පරිවර්තනය කරන්න.
**💡 පැහැදිලි කිරීම:** මුලින්ම 25 ට අදාළ බයිනරි අගය ලියාගන්න. Signed magnitude එකේදී වම්පසම තියෙන bit එක (MSB) 1 කරන්න. 2's complement වලදී ඔක්කොම bits අනිත් පැත්ත හරවලා (1's complement) ඒකට 1 ක් එකතු කරන්න.

**✍️ Exam Answer:**
* **Step 1: Convert absolute value (25) to 8-bit binary.**
  * 25 in binary = `00011001`
* **Signed Magnitude Representation for -25:**
  * In signed magnitude, the MSB is simply flipped to 1 to denote a negative number.
  * Answer: `10011001`
* **2's Complement Representation for -25:**
  * Step A: Take the 1's complement of +25 (invert all bits) -> `11100110`
  * Step B: Add 1 to the LSB -> `11100110 + 1` = `11100111`
  * Answer: `11100111`
* **🎯 Marking Scheme:** 3 marks for finding binary of 25. 3 marks for correct Signed Magnitude. 3 marks for correct 2's complement (showing steps).

### 🔹 Part (ii) - Arithmetic Advantages (15 Marks)

#### Why do modern computer architectures exclusively prefer 2's complement representation over Signed Magnitude for integer arithmetic? Give two detailed reasons. [15 marks]
**❓ සිංහල පරිවර්තනය:** නවීන පරිගණක ගෘහ නිර්මාණ ශිල්පයන් (architectures) පූර්ණ සංඛ්‍යා අංක ගණිතය (integer arithmetic) සඳහා Signed Magnitude වලට වඩා 2's complement නිරූපණයට තනිකරම මනාපයක් දක්වන්නේ ඇයි? සවිස්තරාත්මක හේතු දෙකක් දෙන්න.
**💡 පැහැදිලි කිරීම:** 2's complement භාවිතා කිරීමේ ප්‍රධාන වාසි 2ක් තමයි, බිංදුවට (Zero) තියෙන්නේ එකම එක බයිනරි අගයයි (Signed වල +0 සහ -0 කියලා දෙකක් තියෙනවා). අනිත් වාසිය තමයි, අඩු කරන්න වෙනම circuit ඕනේ නෑ, එකතු කරන circuit එකෙන්ම (Adder) අඩු කිරීමත් කරන්න පුළුවන්.

**✍️ Exam Answer:**
1. **Single Representation of Zero:** In Signed Magnitude, there are two separate binary representations for zero (`+0` is `00000000` and `-0` is `10000000`). This causes unnecessary complexity in logical comparisons (e.g., checking if `A == B`). 2's complement mathematically guarantees only one unique representation for zero (`00000000`), greatly simplifying CPU logic.
2. **Unified Adder Hardware:** In Signed Magnitude, addition and subtraction require completely different hardware circuits and complex logic to compare signs before calculating. However, in 2's complement, subtraction (`A - B`) is gracefully handled as addition (`A + 2's comp of B`). This means the CPU can use the exact same, simple binary Adder circuit for both addition and subtraction, saving massive amounts of transistors and chip space.
* **🎯 Marking Scheme:** 7.5 marks per detailed reason. (Must mention zero representation and unified adder hardware).

<br><hr><br>

## 📝 Question 02 [35 Marks]
**📌 ආවරණය වන දේශන:** L1 (Intro to Performance), L4 (Basic Operation)

### 🔹 Part (i) - CPU Performance (15 Marks)

> [!TIP]
> **Short Note: CPU Time Equation**
> `CPU Time = (Instruction Count) × (Cycles per Instruction - CPI) × (Clock Cycle Time)`

#### a. State the CPU Clock Equation used to calculate Execution Time and briefly explain its three components. [9 marks]
**❓ සිංහල පරිවර්තනය:** ක්‍රියාත්මක වීමේ කාලය (Execution Time) ගණනය කිරීම සඳහා භාවිතා කරන CPU ඔරලෝසු සමීකරණය (CPU Clock Equation) සඳහන් කර එහි සංරචක තුන (components) කෙටියෙන් පැහැදිලි කරන්න.
**💡 පැහැදිලි කිරීම:** CPU Execution Time එක හොයන සූත්‍රය ලියලා, ඒකේ තියෙන IC (Instruction Count), CPI (Cycles per Instruction) සහ Clock Cycle Time කියන්නේ මොනවද කියලා විස්තර කරන්න.

**✍️ Exam Answer:**
* **Equation:** `CPU Execution Time = Instruction Count (IC) × Cycles Per Instruction (CPI) × Clock Cycle Time`
* **Components:**
  1. **Instruction Count (IC):** The total number of machine instructions that a specific program executes. (Affected by the compiler and ISA).
  2. **CPI:** The average number of clock cycles it takes to execute a single instruction. (Affected by CPU architecture and pipelining).
  3. **Clock Cycle Time:** The duration of one single tick of the CPU clock (e.g., 1 nanosecond for a 1GHz processor). It is the inverse of the Clock Rate.
* **🎯 Marking Scheme:** 3 marks for the equation. 2 marks per component explanation (6 total).

#### b. How does increasing the Clock Rate (GHz) affect the CPU Time equation, and what is its primary physical limitation? [6 marks]
**❓ සිංහල පරිවර්තනය:** ඔරලෝසු වේගය (Clock Rate - GHz) වැඩි කිරීම CPU Time සමීකරණයට බලපාන්නේ කෙසේද, සහ එහි මූලික භෞතික සීමාව කුමක්ද?
**💡 පැහැදිලි කිරීම:** Clock speed එක (GHz) වැඩි කරාම Clock Cycle Time එක අඩු වෙනවා, ඒ නිසා මුළු Execution Time එක අඩු වෙනවා (වේගවත් වෙනවා). හැබැයි මේක දිගටම කරන්න බෑ, මොකද ගොඩක් වේගවත් කරාම CPU එකේ රස්නය (Heat) වැඩි වෙලා පිච්චෙන්න පුළුවන් (Power Wall).

**✍️ Exam Answer:**
* **Effect:** Increasing the Clock Rate directly decreases the *Clock Cycle Time*. According to the CPU equation, if the cycle time shrinks while IC and CPI remain constant, the overall CPU Execution Time decreases, making the computer process tasks faster.
* **Limitation:** The primary physical limitation is the **Power Wall** (Thermal Dissipation). Switching transistors at ultra-high frequencies generates massive amounts of heat. Beyond ~4-5 GHz, standard cooling cannot remove the heat fast enough, causing the silicon chip to melt or malfunction.
* **🎯 Marking Scheme:** 3 marks for the effect on the equation. 3 marks for mentioning heat/power wall as the limit.

### 🔹 Part (ii) - Amdahl's Law & Parallelism (20 Marks)

#### State Amdahl's Law and mathematically explain its significance in parallel computing (multi-core processors). [20 marks]
**❓ සිංහල පරිවර්තනය:** Amdahl ගේ නියමය (Amdahl's Law) ප්‍රකාශ කර, සමාන්තර පරිගණනය (parallel computing - multi-core processors) තුළ එහි වැදගත්කම ගණිතමය වශයෙන් පැහැදිලි කරන්න.
**💡 පැහැදිලි කිරීම:** Amdahl's Law කියන්නේ මොකක්ද කියලා ලියලා, අපි cores කීයක් වැඩි කරත් මුළු program එකම වේගවත් කරන්න බැරි ඇයි කියලා තර්ක කරන්න (සමහර කොටස් අනිවාර්යයෙන්ම එකින් එක (sequentially) run වෙන්න ඕනේ නිසා).

**✍️ Exam Answer:**
* **Definition:** Amdahl's Law states that the overall performance improvement (speedup) gained by optimizing a single specific part of a system is strictly limited by the fraction of execution time that the unoptimized part takes.
* **Significance in Parallel Computing:** 
  * If you buy an 8-core or 16-core CPU, you might expect a program to run 8x or 16x faster. Amdahl's law proves this is mathematically impossible for most software.
  * Every program has a strictly sequential portion (code that must run one after the other on a single core) and a parallelizable portion. 
  * If a program is 80% parallelizable and 20% strictly sequential, no matter if you add 1,000 CPU cores to speed up that 80%, the overall execution time can *never* be less than that 20% sequential time. 
  * The maximum theoretical speedup is bound by `1 / (1 - Parallel Fraction)`. Adding infinite cores yields diminishing returns.
* **🎯 Marking Scheme:** 6 marks for definition. 8 marks for explaining the sequential vs parallel breakdown. 6 marks for concluding about diminishing returns/maximum limits.

<br><hr><br>

## 📝 Question 03 [35 Marks]
**📌 ආවරණය වන දේශන:** L9 (MIPS32 & Pipelining)

### 🔹 Part (i) - Pipelining Basics (15 Marks)

#### a. Define "Throughput" and "Latency" in the context of CPU pipelining. Does pipelining improve both? [7 marks]
**❓ සිංහල පරිවර්තනය:** CPU Pipelining සන්දර්භය තුළ "Throughput" සහ "Latency" නිර්වචනය කරන්න. Pipelining මගින් මේ දෙකම වැඩි දියුණු කරයිද?
**💡 පැහැදිලි කිරීම:** Latency කියන්නේ එක වැඩක් (instruction එකක්) පටන් අරන් ඉවර කරන්න යන මුළු කාලය. Throughput කියන්නේ තත්පරයකට ඉවර කරන මුළු වැඩ ගණන (instructions ගණන). Pipelining වලින් Throughput එක විතරයි වැඩි වෙන්නේ, Latency එක වැඩි වෙන්නේ නෑ.

**✍️ Exam Answer:**
* **Latency:** The total time taken to completely execute a *single* instruction from start (fetch) to finish (write-back). 
* **Throughput:** The total number of instructions that completely finish execution per unit of time (e.g., per second).
* **Does it improve both?** **No.** Pipelining massively increases *Throughput* because multiple instructions are processed concurrently in different stages. However, it does *not* improve the *Latency* of an individual instruction; in fact, due to pipeline register overheads, the latency of a single instruction might slightly increase.
* **🎯 Marking Scheme:** 2.5 marks for Latency. 2.5 marks for Throughput. 2 marks for stating it only improves throughput.

#### b. Explain the concept of "Data Forwarding" (Bypassing) in a pipelined CPU. [8 marks]
**❓ සිංහල පරිවර්තනය:** Pipelined CPU එකක් තුළ "Data Forwarding" (Bypassing) සංකල්පය පැහැදිලි කරන්න.
**💡 පැහැදිලි කිරීම:** Data Hazard එකක් ආවම (පරණ instruction එකක උත්තරේ අලුත් එකකට ඕනේ වුණාම) CPU එක stall වෙලා (නැවතිලා) කල් මරනවා වෙනුවට, ALU එකේ උත්තරේ කෙළින්ම ආයේ ALU එකේ input එකටම දෙන (forward කරන) bypass ක්‍රමය පැහැදිලි කරන්න.

**✍️ Exam Answer:**
* **Problem:** A Data Hazard occurs when a current instruction needs the result of a previous instruction that is still flowing through the pipeline and hasn't yet written its result to the register file.
* **Solution (Data Forwarding):** Instead of stalling the entire pipeline and wasting cycles waiting for the write-back stage, Data Forwarding uses special hardware bypass circuits. 
* These circuits detect the dependency and route (forward) the newly calculated output directly from the ALU's output buffer straight back into the ALU's input buffer for the next instruction that immediately needs it, completely avoiding a stall.
* **🎯 Marking Scheme:** 3 marks for defining the problem (Data Hazard). 5 marks for explaining the hardware bypass/routing solution.

### 🔹 Part (ii) - Branch Hazards & MIPS (20 Marks)

#### a. What is a "Control Hazard" (Branch Hazard) in a pipeline, and mention two techniques used to minimize its impact. [10 marks]
**❓ සිංහල පරිවර්තනය:** Pipeline එකක "Control Hazard" (Branch Hazard) යනු කුමක්ද, සහ එහි බලපෑම අවම කිරීම සඳහා භාවිතා කරන ශිල්පීය ක්‍රම (techniques) දෙකක් සඳහන් කරන්න.
**💡 පැහැදිලි කිරීම:** if/while වගේ Branch එකක් ආවම CPU එක වැරදි පාරක ගිහින් වැරදි instructions pipeline එකට අරන්, පස්සේ ඒවා මකලා (flush) දාන්න වෙන නිසා කාලය නාස්ති වෙන එකට තමයි Control Hazard කියන්නේ. මේක අඩු කරන්න Branch Prediction සහ Delayed Branching පාවිච්චි කරනවා.

**✍️ Exam Answer:**
* **What it is:** A control hazard occurs due to branch instructions (like `if`, `while`, or `j`). The pipeline continuously fetches instructions sequentially assuming the branch won't be taken. If the branch *is* actually taken, the flow of execution suddenly changes. All the sequential instructions that were incorrectly fetched into the pipeline stages must now be discarded (flushed), resulting in a massive waste of cycles (a pipeline stall/bubble).
* **Two Techniques to Minimize:**
  1. **Branch Prediction:** The CPU uses historical data to guess whether the branch will be taken or not before it is actually calculated. If guessed correctly, no flush occurs.
  2. **Delayed Branching:** The compiler cleverly inserts a useful, independent instruction into the "branch delay slot" (the cycle right after the branch), ensuring the CPU does useful work while calculating the branch target.
* **🎯 Marking Scheme:** 6 marks for explaining the flush/stall mechanism of control hazards. 4 marks (2x2) for the two techniques.

#### b. Translate this pseudo-instruction into actual MIPS32 instructions: `li $t0, 0x12345678` [10 marks]
**❓ සිංහල පරිවර්තනය:** මෙම ව්‍යාජ උපදෙස (pseudo-instruction) සැබෑ MIPS32 උපදෙස් බවට පරිවර්තනය කරන්න: `li $t0, 0x12345678`
**💡 පැහැදිලි කිරීම:** MIPS instruction එකකට උපරිම තියෙන්න පුළුවන් bits 32 යි. ඒක ඇතුළේ opcode එකයි register එකයි දාලා ආයෙත් bits 32 ක value එකක් (`0x12345678`) එකවර දාන්න ඉඩ නෑ. ඒ නිසා මේක උපදෙස් 2 කට කඩන්න ඕනේ (`lui` සහ `ori`).

**✍️ Exam Answer:**
* **The Problem:** A single MIPS32 instruction is strictly 32 bits long. It must contain the opcode and register fields, so there is not enough room to fit an entire 32-bit immediate value (`0x12345678`) inside one instruction.
* **The Translation:** The assembler automatically breaks this pseudo-instruction down into two actual machine instructions:
  1. It uses `lui` (Load Upper Immediate) to place the top 16 bits into the upper half of the register.
  2. It uses `ori` (OR Immediate) to place the bottom 16 bits into the lower half.
* **MIPS Code:**
  ```assembly
  lui $t0, 0x1234        # Load upper 16 bits into $t0 (lower 16 become 0000)
  ori $t0, $t0, 0x5678   # Bitwise OR to inject the lower 16 bits without altering upper bits
  ```
* **🎯 Marking Scheme:** 4 marks for explaining the 32-bit limitation. 6 marks for the correct two instructions (`lui` and `ori`).
