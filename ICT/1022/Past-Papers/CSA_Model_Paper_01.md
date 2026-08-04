# 📘 CSA Model Paper 01 (Core Architecture & Basics)

මෙය 2025 Past Paper ආකෘතියටම සකසන ලද පළමු අනුමාන ප්‍රශ්න පත්‍රයයි. මෙහි සෑම ප්‍රශ්නයකම නිවැරදි සිංහල පරිවර්තනය සහ පැහැදිලි කිරීම් අඩංගු කර ඇත.

---

## 📝 Question 01 [30 Marks]
**📌 ආවරණය වන දේශන:** L2 (Digital Computer), L5 (Basic Computer Operation)

### 🔹 Part (i) - CPU Architecture & Bottlenecks (15 Marks)

> [!TIP]
> **Short Note: Memory Bottleneck**
> The CPU operates at GHz (extremely fast), but RAM operates at MHz (slower). If they share a single bus, the CPU is starved for data. 

#### a. Explain the "Von Neumann Bottleneck" and describe how the Harvard architecture attempts to solve it. [6 marks]
**❓ සිංහල පරිවර්තනය:** "Von Neumann Bottleneck" යනු කුමක්දැයි පැහැදිලි කර, Harvard ගෘහ නිර්මාණ ශිල්පය (architecture) මගින් එය විසඳීමට උත්සාහ කරන්නේ කෙසේදැයි විස්තර කරන්න.
**💡 පැහැදිලි කිරීම:** මෙහිදී අසන්නේ Von Neumann ආකෘතියේ ඇති ප්‍රධාන දුර්වලතාවය (Data සහ Instructions එකම බස් එකක ගමන් කිරීම නිසා ඇතිවන තදබදය) සහ Harvard ආකෘතිය මගින් වෙන වෙනම බස් මාර්ග (buses) භාවිතා කර එය විසඳන ආකාරය ගැනයි. 

**✍️ Exam Answer:**
* **Von Neumann Bottleneck:** Occurs because both instructions and data share the exact same physical memory and bus system. Since the CPU is much faster than the memory, it constantly idles (stalls) waiting to fetch either instructions or data sequentially, severely limiting overall system throughput.
* **Harvard Solution:** Harvard architecture solves this by providing entirely separate physical memory modules and separate buses for instructions and data. This structural separation allows the CPU to fetch an instruction and read/write data concurrently in the same clock cycle, completely removing the shared bus bottleneck.
* **🎯 Marking Scheme:** 3 marks for clearly explaining the bottleneck (shared bus/stall). 3 marks for explaining the Harvard solution (separate buses/concurrent fetch).

#### b. "Adding a large L1 cache eliminates the need for Main Memory." State whether this statement is true or false, and justify your answer. [5 marks]
**❓ සිංහල පරිවර්තනය:** "විශාල L1 කෑෂ් එකක් (cache) එකතු කිරීම මගින් ප්‍රධාන මතකයේ (Main Memory) අවශ්‍යතාවය නැති කර දමයි." මෙම ප්‍රකාශය සත්‍ය ද අසත්‍ය ද යන්න සඳහන් කර, ඔබගේ පිළිතුර සාධාරණීකරණය කරන්න.
**💡 පැහැදිලි කිරීම:** ප්‍රකාශය වැරදියි. Cache memory කොච්චර තිබුණත් RAM එකක් අනිවාර්යයෙන්ම අවශ්‍ය ඇයි කියලා ලියන්න ඕනේ (Cache වල මිල වැඩියි, ධාරිතාවය/ඉඩ මදි නිසා).

**✍️ Exam Answer:**
* **False.**
* **Justification:** While an L1 cache is extremely fast (built with SRAM) and essential for storing frequently used instructions to prevent pipeline stalls, it is highly expensive and physically large per bit. Therefore, its capacity is strictly limited (usually a few Megabytes). 
* Main memory (built with DRAM) provides the massive, affordable capacity (Gigabytes) needed to store the Operating System, large applications, and background processes. A modern computer requires both to balance speed (Cache) and capacity (RAM).
* **🎯 Marking Scheme:** 1 mark for 'False'. 2 marks for Cache limits (expensive/small). 2 marks for RAM necessity (capacity/cheap).

#### c. If the ALU only performs simple arithmetic (add/subtract) and logic (AND/OR) operations, briefly explain how a CPU performs complex multiplication. [4 marks]
**❓ සිංහල පරිවර්තනය:** ALU එක සිදු කරන්නේ සරල එකතු කිරීම්/අඩු කිරීම් සහ තාර්කික මෙහෙයුම් පමණක් නම්, CPU එකක් සංකීර්ණ ගුණ කිරීම් (multiplication) සිදු කරන්නේ කෙසේදැයි කෙටියෙන් පැහැදිලි කරන්න.
**💡 පැහැදිලි කිරීම:** ALU එක ඇතුළේ කෙළින්ම "ගුණ කිරීමේ" circuit එකක් නැති වුණත්, නැවත නැවත එකතු කිරීම (repeated addition) සහ bit ෂිෆ්ට් කිරීම (bit-shifting) මගින් ඒක කරගන්නා ආකාරය ලියන්න.

**✍️ Exam Answer:**
* The CPU performs complex operations like multiplication through a sequence of simpler ALU operations, orchestrated by the Control Unit.
* Specifically, multiplication is handled algorithmically using repeated **Addition** and **Bit-Shifting** (e.g., left shifts) operations within the ALU. In modern processors, this is often managed by specialized microcode or dedicated hardware multiplier circuits that sequence these basic ALU operations at high speed.
* **🎯 Marking Scheme:** 2 marks for stating it uses a sequence of simpler operations. 2 marks for specifying Addition and Bit-Shifting.

---

### 🔹 Part (ii) - Programming Languages & Execution (15 Marks)

#### a. Give one specific scenario where writing a program in Assembly language is strictly better than writing it in a High-Level Language (HLL) like Python, and explain why. [8 marks]
**❓ සිංහල පරිවර්තනය:** Python වැනි උසස් මට්ටමේ භාෂාවකට වඩා Assembly භාෂාවෙන් ක්‍රමලේඛයක් (program එකක්) ලිවීම නිශ්චිතවම වඩා හොඳ වන එක් නිශ්චිත අවස්ථාවක් ලබා දී, ඒ මන්දැයි පැහැදිලි කරන්න.
**💡 පැහැදිලි කිරීම:** Assembly language භාවිතා කිරීම අත්‍යවශ්‍ය වන අවස්ථාවක් (උදා: Hardware drivers ලිවීම) දීලා, ඒක වේගවත් ඇයි, hardware කෙළින්ම පාලනය කරන්නේ ඇයි කියලා ලියන්න.

**✍️ Exam Answer:**
* **Scenario:** Developing hardware device drivers, embedded systems firmware, or real-time OS kernels.
* **Why it's better:** 
  1. **Direct Hardware Control:** Assembly allows precise, bit-level manipulation of specific CPU registers and memory addresses, which is impossible in abstracted languages like Python.
  2. **Deterministic Execution:** It executes with minimal overhead and exact predictable timing. In real-time systems (e.g., medical equipment, airbag sensors), the garbage collection or interpreter overhead of an HLL would cause unacceptable delays or unpredictable latency. Assembly guarantees immediate execution.
* **🎯 Marking Scheme:** 3 marks for a valid scenario. 5 marks for a strong justification (Hardware control & no overhead).

#### b. Briefly explain the roles of a Compiler and an Assembler. [7 marks]
**❓ සිංහල පරිවර්තනය:** සම්පාදකයක (Compiler) සහ එකලස්කරනයක (Assembler) කාර්යභාරයන් කෙටියෙන් පැහැදිලි කරන්න.
**💡 පැහැදිලි කිරීම:** Compiler එකක් කරන්නේ High-level code (C++/Java) එකක් යන්ත්‍ර භාෂාවට හරවන එක. Assembler එකක් කරන්නේ Assembly code එකක් (ADD, SUB) යන්ත්‍ර භාෂාවට හරවන එක. මේ වෙනස ලියන්න.

**✍️ Exam Answer:**
* **Compiler:** A complex software tool that translates the entire source code written in a High-Level Language (like C++ or Java) into lower-level machine code or assembly language in one go, before execution. It handles complex optimizations and syntax checking.
* **Assembler:** A simpler program that translates Assembly language mnemonics (like `ADD`, `LOAD`) directly into the binary machine code (0s and 1s) understandable by the specific CPU architecture. It maps instructions almost 1-to-1.
* **🎯 Marking Scheme:** 3.5 marks for Compiler definition. 3.5 marks for Assembler definition.

<br><hr><br>

## 📝 Question 02 [35 Marks]
**📌 ආවරණය වන දේශන:** L4 (Instruction Cycle), L6 (Buses)

### 🔹 Part (i) - CPU Registers and Instruction Cycle (15 Marks)

> [!TIP]
> **Short Note: The Fetch Cycle**
> 1. PC -> MAR
> 2. Memory -> MDR
> 3. MDR -> IR
> 4. PC = PC + 1

#### a. During an instruction fetch, explain the detailed interaction between the PC (Program Counter) and the MAR (Memory Address Register). [7 marks]
**❓ සිංහල පරිවර්තනය:** උපදෙස් ලබා ගැනීමේදී (instruction fetch), PC (Program Counter) සහ MAR (Memory Address Register) අතර සිදුවන සවිස්තරාත්මක අන්තර්ක්‍රියාව පැහැදිලි කරන්න.
**💡 පැහැදිලි කිරීම:** Fetch cycle එකේ මුලින්ම වෙන්නේ PC එකේ තියෙන address එක MAR එකට කොපි වෙන එක. ඊටපස්සේ MAR එක ඒක Address bus එකට දාන හැටි ලියන්න.

**✍️ Exam Answer:**
* At the very beginning of the fetch cycle, the CPU must know the exact memory address from which to fetch the next instruction.
* The memory address currently held in the **Program Counter (PC)** is electronically copied into the **Memory Address Register (MAR)** via the internal bus.
* The MAR is connected directly to the Address Bus. It places this copied address onto the Address Bus to locate the specific instruction in the external Main Memory. 
* Immediately after this transfer to the MAR, the PC increments its value to point to the address of the subsequent instruction.
* **🎯 Marking Scheme:** 2 marks for PC role. 2 marks for copying to MAR. 2 marks for placing on Address bus. 1 mark for PC increment.

#### b. Consider the instruction `SUB R3, R1`. Assume R1 = 15 and R3 = 40. Describe the Execute and Write-back phases for this specific instruction. [8 marks]
**❓ සිංහල පරිවර්තනය:** `SUB R3, R1` යන උපදෙස සලකා බලන්න. R1 = 15 සහ R3 = 40 යැයි උපකල්පනය කරන්න. මෙම නිශ්චිත උපදෙස සඳහා Execute (ක්‍රියාත්මක කිරීම) සහ Write-back (නැවත ලිවීම) අදියරයන් විස්තර කරන්න.
**💡 පැහැදිලි කිරීම:** Execute එකේදී ALU එක ඇතුළේ 40 න් 15 ක් අඩු වෙන හැටිත්, Write-back එකේදී ඒ උත්තරේ (25) ආපහු R3 register එකේ ගබඩා වෙන හැටිත් ලියන්න.

**✍️ Exam Answer:**
* **Execute Phase:** The Control Unit has already decoded the instruction as a subtraction. The ALU receives the actual operand values from the register file via the internal datapath: Value 40 from Register R3, and Value 15 from Register R1. The ALU then performs the binary arithmetic calculation: `40 - 15 = 25`. It also updates status flags (e.g., checking for zero or negative result).
* **Write-back Phase:** The newly calculated result (25) generated by the ALU is placed on the internal datapath and routed back to the register file. It is explicitly written into the destination register (which is R3 in this syntax). The old value of R3 (40) is overwritten, and R3 now securely holds the value 25.
* **🎯 Marking Scheme:** 4 marks for Execute phase details (operands to ALU, calculation). 4 marks for Write-back details (storing 25 in R3).

### 🔹 Part (ii) - Bus Architecture and Data Transfer (20 Marks)

#### a. Why do modern motherboards use separate buses for CPU-Memory communication (Front-Side Bus) and I/O devices (e.g., PCIe/USB)? [10 marks]
**❓ සිංහල පරිවර්තනය:** නවීන මවුපුවරු වල CPU සහ Memory අතර සන්නිවේදනය සඳහාත්, I/O උපාංග සඳහාත් වෙන වෙනම බස් මාර්ග (separate buses) භාවිතා කරන්නේ ඇයි?
**💡 පැහැදිලි කිරීම:** CPU එක සහ RAM එක ගොඩක් වේගවත්. I/O (උදා: Keyboard, HDD) ගොඩක් slow. සේරම එකම බස් එකකට දැම්මොත් CPU එකටත් slow වෙන්න වෙනවා. ඒ නිසා වේගයන් දෙකකට බස් දෙකක් භාවිතා කරන බව ලියන්න.

**✍️ Exam Answer:**
* **The Speed Discrepancy:** The CPU and Main Memory operate at extremely high frequencies (multi-Gigahertz range). In stark contrast, mechanical I/O devices (like HDDs) or human interface devices (like keyboards) operate at vastly slower speeds (often Kilohertz or Megahertz).
* **Avoiding Bottlenecks:** If a single universal system bus was used to connect everything, the fast CPU would have to dramatically slow down its clock rate to communicate with slow I/O devices, wasting millions of CPU cycles and causing severe bus contention.
* **The Multi-Bus Solution:** Using separate buses allows for tiered communication. The CPU can communicate with RAM via a dedicated, ultra-fast Front-Side Bus (or memory controller bus) at maximum speed. Simultaneously, slower I/O transfers can happen on an I/O bus (like PCIe). Bridge chips coordinate the traffic between these fast and slow buses without stalling the CPU.
* **🎯 Marking Scheme:** 3 marks for identifying the speed difference. 4 marks for the bottleneck problem of a single bus. 3 marks for the solution (concurrent transfers via bridges).

#### b. Explain the difference between a synchronous bus and an asynchronous bus. [10 marks]
**❓ සිංහල පරිවර්තනය:** සමමුහුර්ත බස් රථයක් (synchronous bus) සහ අසමමුහුර්ත බස් රථයක් (asynchronous bus) අතර වෙනස පැහැදිලි කරන්න.
**💡 පැහැදිලි කිරීම:** Synchronous කියන්නේ එකම clock signal එකකට වැඩ කරන වේගවත් හැබැයි flexibility අඩු බස් එකක්. Asynchronous කියන්නේ clock එකක් නැතුව 'handshaking' (ready, acknowledge) හරහා වැඩ කරන, ඕනෑම වේගයක උපාංග සම්බන්ධ කළ හැකි බස් එකක්.

**✍️ Exam Answer:**
* **Synchronous Bus:** All devices on the bus are synchronized by a central clock signal. Data transfers strictly occur at specific clock edges. 
  * *Pros:* Simple design, fast for devices with similar speeds. 
  * *Cons:* Not flexible; it forces all devices to operate at the speed of the slowest device on the bus, or requires wait states.
* **Asynchronous Bus:** There is no central clock. Devices coordinate data transfers using a "handshaking" protocol (e.g., using 'Ready' and 'Acknowledge' control signals).
  * *Pros:* Highly flexible. It can seamlessly connect devices of vastly different speeds (e.g., a fast CPU and a slow printer) without slowing down the fast device.
  * *Cons:* More complex circuitry and slight overhead due to the handshaking process.
* **🎯 Marking Scheme:** 5 marks for Synchronous (clocked, simple, rigid). 5 marks for Asynchronous (handshaking, flexible, complex).

<br><hr><br>

## 📝 Question 03 [35 Marks]
**📌 ආවරණය වන දේශන:** L7 (Number Systems), L8 (Addressing Modes)

### 🔹 Part (i) - 2's Complement Arithmetic (15 Marks)

#### Using 8-bit signed 2's complement arithmetic, demonstrate how the CPU evaluates `-12 + 5`. State whether an overflow occurs and explain why. [15 marks]
**❓ සිංහල පරිවර්තනය:** බිට් 8 ක සලකුණු සහිත 2's complement ක්‍රමය භාවිතයෙන්, CPU එක `-12 + 5` ගණනය කරන්නේ කෙසේදැයි පෙන්වා දෙන්න. මෙහිදී overflow එකක් (උතුරා යාමක්) සිදුවේද යන්න සඳහන් කර ඒ මන්දැයි පැහැදිලි කරන්න.
**💡 පැහැදිලි කිරීම:** 12 න් 2's complement එක හොයලා ඒකට 5 න් බයිනරි එකතු කරන්න. ධන සංඛ්‍යාවක් සහ සෘණ සංඛ්‍යාවක් එකතු කරද්දී කවදාවත් overflow වෙන්න බැරි බව තර්ක කරන්න.

**✍️ Exam Answer (Steps):**
1. **Represent initial values in 8-bit binary:**
   * Decimal +12 = `0000 1100`
   * Decimal +5  = `0000 0101`
2. **Find the 2's complement of 12 (to represent -12):**
   * Step A: 1's complement (invert all bits) = `1111 0011`
   * Step B: Add 1 to the LSB = `1111 0011 + 1` = `1111 0100` 
   * So, -12 = `1111 0100`
3. **Perform Binary Addition (-12 + 5):**
   ```text
     1111 0100  (represents -12)
   + 0000 0101  (represents +5)
   -------------
     1111 1001  (Result)
   ```
4. **Analyze the Result & Overflow:**
   * The Most Significant Bit (MSB) of the result `1111 1001` is **1**. In signed arithmetic, an MSB of 1 indicates a **negative number**.
   * (Verification: Inverting result and adding 1 gives `0000 0111` which is 7, so the result is indeed -7. Correct.)
   * **Overflow:** **No Overflow occurs.** 
   * **Reasoning:** An overflow in signed addition can *only* happen if you add two numbers of the *same sign* and the result produces the *opposite sign* (e.g., adding two huge positive numbers and getting a negative result due to exceeding bit capacity). When adding numbers of opposite signs (-12 and +5), it is mathematically impossible to exceed the capacity, hence overflow is impossible.
* **🎯 Marking Scheme:** 2 marks for binary representations. 4 marks for correctly calculating 2's complement of -12. 4 marks for the binary addition. 2 marks for stating No Overflow. 3 marks for the reasoning (opposite signs never overflow).

### 🔹 Part (ii) - Addressing Modes (20 Marks)

> [!TIP]
> **Short Note: Addressing Modes**
> * **Immediate:** Operand is in the instruction (`ADD R1, 5`).
> * **Direct:** Address is in the instruction (`LOAD R1, [1000]`).
> * **Indirect:** Address in instruction points to another address (`LOAD R1, [[1000]]`).

#### Distinguish between Immediate Addressing Mode, Direct Addressing Mode, and Indirect Addressing Mode. Provide a clear example and state one advantage for each. [20 marks]
**❓ සිංහල පරිවර්තනය:** Immediate Addressing Mode, Direct Addressing Mode, සහ Indirect Addressing Mode අතර වෙනස හඳුනාගන්න. පැහැදිලි උදාහරණයක් ලබා දී ඒ සෑම එකක් සඳහාම එක් වාසියක් සඳහන් කරන්න.
**💡 පැහැදිලි කිරීම:** Immediate (දත්ත කෙළින්ම උපදෙසේ ඇත), Direct (දත්ත තියෙන ලිපිනය උපදෙසේ ඇත), Indirect (ලිපිනයක් තියෙන ලිපිනයක් උපදෙසේ ඇත) යන ක්‍රම 3 න්‍යායාත්මකව විස්තර කර උදාහරණ දෙන්න.

**✍️ Exam Answer:**

**1. Immediate Addressing Mode:**
* **Definition:** The actual operand value is provided directly as a constant within the instruction word itself. No memory access is required to fetch the operand.
* **Example:** `ADD R1, #50` (Add the literal decimal value 50 to the contents of R1).
* **Advantage:** Extremely fast execution since it avoids a slow memory fetch cycle.

**2. Direct Addressing Mode:**
* **Definition:** The instruction contains the exact, physical memory address where the operand is stored. The CPU must perform one memory access to fetch the data.
* **Example:** `LOAD R1, [2050]` (Go to memory location 2050, read the data there, and put it in R1).
* **Advantage:** Very simple to understand and implement. Good for accessing static global variables.

**3. Indirect Addressing Mode:**
* **Definition:** The instruction contains a memory address, but the data at that address is *not* the operand. Instead, it is a *pointer* (another address) to the actual operand. The CPU must perform two memory accesses.
* **Example:** `LOAD R1, [[3000]]` (Go to location 3000, read the address stored there (e.g., 5000), then go to location 5000, read the data, and put it in R1).
* **Advantage:** Provides massive flexibility, essential for implementing pointers in languages like C, and for passing large arrays to functions by reference.
* **🎯 Marking Scheme:** For each mode: 3 marks for definition, 2 marks for example, 1 mark for advantage (Total 6 * 3 = 18). 2 marks for overall clarity.
