# 📘 CSA Model Paper 02 (Control Unit, Memory, & I/O)

මෙය සම්පූර්ණ විෂය නිර්දේශයේ (L10, L11, L12) ඇති අතිශය වැදගත් සහ විභාගයට බලාපොරොත්තු වන අමතර කොටස් ආවරණය කරමින් සකසා ඇති දෙවන අනුමාන ප්‍රශ්න පත්‍රයයි. මෙහි සෑම ප්‍රශ්නයකම නිවැරදි සිංහල පරිවර්තනය සහ පැහැදිලි කිරීම් අඩංගු කර ඇත.

---

## 📝 Question 01 [30 Marks]
**📌 ආවරණය වන දේශන:** L10 (Control Unit), L12 (I/O Systems)

### 🔹 Part (i) - Control Unit Design (15 Marks)

> [!TIP]
> **Short Note: Control Unit Types**
> * **Hardwired:** Fast, built with logic gates, inflexible (RISC).
> * **Microprogrammed:** Slower, built with microcode in ROM, very flexible (CISC).

#### a. What is the main difference between a Hardwired Control Unit and a Microprogrammed Control Unit? [7 marks]
**❓ සිංහල පරිවර්තනය:** Hardwired Control Unit එකක් සහ Microprogrammed Control Unit එකක් අතර ඇති ප්‍රධාන වෙනස කුමක්ද?
**💡 පැහැදිලි කිරීම:** මේ පාලන ඒකක (Control Units) හදන ක්‍රම දෙක ගැනයි අහන්නේ. Hardwired එක හදන්නේ electronic කෑලි (gates) එකතු කරලා. ඒ නිසා ඒක වේගවත්, හැබැයි වෙනස් කරන්න බෑ. Microprogrammed එක හදන්නේ ROM එකක code එකක් ලියලා. ඒක වෙනස් කරන්න ලේසියි.

**✍️ Exam Answer:**
* **Hardwired Control Unit:** Uses physical, sequential logic circuits (flip-flops, gates, decoders) wired together to directly generate control signals. It is incredibly fast but extremely rigid; changing the instruction set requires physically redesigning the wiring.
* **Microprogrammed Control Unit:** Operates like a tiny computer within the CPU. It executes a sequence of microinstructions stored in a special internal memory (Control Memory / ROM). It is generally slower than hardwired logic but highly flexible and easy to modify simply by updating the microcode.
* **🎯 Marking Scheme:** 3.5 marks for Hardwired definition. 3.5 marks for Microprogrammed definition.

#### b. State two advantages of using a Microprogrammed Control Unit. [4 marks]
**❓ සිංහල පරිවර්තනය:** Microprogrammed Control Unit එකක් භාවිතා කිරීමේ වාසි දෙකක් සඳහන් කරන්න.
**💡 පැහැදිලි කිරීම:** ROM එකේ ලියපු code එකක් (microcode) පාවිච්චි කරන එකේ වාසි දෙකක්. (වෙනස් කරන්න/අලුත් කරන්න ලේසි වීම සහ සංකීර්ණ දේවල් හදන්න ලේසි වීම).

**✍️ Exam Answer:**
1. **Flexibility & Upgradability:** It is extremely easy to modify the control logic, fix hardware bugs, or add entirely new instructions by merely updating the microcode in the ROM, without changing the physical hardware.
2. **Simplifies Complex Designs:** It is ideal for implementing complex instruction sets (CISC architecture), as complex multi-step instructions can be easily written as a simple sequence of microcode.
* **🎯 Marking Scheme:** 2 marks per valid advantage.

#### c. Describe the role of the Control Address Register (CAR) in a microprogrammed CPU. [4 marks]
**❓ සිංහල පරිවර්තනය:** Microprogrammed CPU එකක් තුළ Control Address Register (CAR) හි කාර්යභාරය විස්තර කරන්න.
**💡 පැහැදිලි කිරීම:** සාමාන්‍ය CPU එකේ PC (Program Counter) එක වගේම, Control Unit එක ඇතුළේ ඊළඟට execute කරන්න ඕනේ instruction එකේ (microinstruction එකේ) address එක තියාගෙන ඉන්න එක තමයි CAR එකෙන් කරන්නේ.

**✍️ Exam Answer:**
* The CAR functions similarly to the main Program Counter (PC), but specifically for the Control Unit. 
* It holds the memory address of the next *microinstruction* to be fetched from the internal Control Memory, ensuring the microprogram executes in the correct sequence to complete a macro-instruction.
* **🎯 Marking Scheme:** 2 marks for comparison with PC. 2 marks for stating it points to the next microinstruction in Control Memory.

### 🔹 Part (ii) - Direct Memory Access (DMA) (15 Marks)

#### a. What is Direct Memory Access (DMA) and when is it most appropriate to use? [8 marks]
**❓ සිංහල පරිවර්තනය:** Direct Memory Access (DMA) යනු කුමක්ද සහ එය භාවිතා කිරීම වඩාත් යෝග්‍ය වන්නේ කවදාද?
**💡 පැහැදිලි කිරීම:** I/O device එකක ඉඳන් කෙළින්ම RAM එකට Data යවන (CPU එක මැදට එන්නේ නැතුව) ක්‍රමය තමයි DMA. මේක ගොඩක් පාවිච්චි කරන්නේ ලොකු files, videos වගේ ලොකු දත්ත ප්‍රමාණයක් (large blocks) යවන්න ඕනේ වුණාම. 

**✍️ Exam Answer:**
* **What it is:** DMA is a specialized hardware component (DMA Controller) on the motherboard that manages data transfers directly between I/O peripherals and Main Memory, entirely bypassing the CPU.
* **When to use:** It is most appropriate for transferring massive blocks of data at high speeds (e.g., reading a large file from an SSD, or transferring video frames to a graphics card). It prevents the CPU from being bogged down with trivial byte-by-byte transfer tasks, freeing it up to perform complex computations concurrently.
* **🎯 Marking Scheme:** 4 marks for defining it (bypassing CPU). 4 marks for the use-case (large blocks of data / freeing CPU).

#### b. Describe the process of "Cycle Stealing" in DMA. [7 marks]
**❓ සිංහල පරිවර්තනය:** DMA හි "Cycle Stealing" ක්‍රියාවලිය විස්තර කරන්න.
**💡 පැහැදිලි කිරීම:** DMA එකෙන් data යවද්දී බස් එක සම්පූර්ණයෙන්ම අල්ලගෙන හිටියොත් CPU එකට වැඩක් කරගන්න බැරි වෙනවා. ඒ නිසා CPU එකට නොදැනෙන්න තත්පරේකින් පොඩිම පොඩි අංශුවක් (one clock cycle) විතරක් බස් එක අරන් data යවන එක තමයි මේ Cycle Stealing කියන්නේ.

**✍️ Exam Answer:**
* Cycle stealing is a technique used by the DMA controller to share the system bus with the CPU. 
* Instead of locking the bus for the entire duration of a large data transfer (which would completely freeze the CPU), the DMA controller momentarily takes control of the system bus for just a single clock cycle to transfer one word of data. 
* It essentially "steals" this cycle from the CPU. The CPU is paused for only a fraction of a microsecond, allowing both computation and I/O transfers to seemingly occur simultaneously.
* **🎯 Marking Scheme:** 3 marks for mentioning bus sharing. 4 marks for explaining single-cycle transfer and CPU pause.

<br><hr><br>

## 📝 Question 02 [35 Marks]
**📌 ආවරණය වන දේශන:** L11 (Memory Systems)

### 🔹 Part (i) - Memory Hardware & Hierarchy (15 Marks)

#### a. Differentiate between SRAM and DRAM. Which one is used for Cache memory and why? [8 marks]
**❓ සිංහල පරිවර්තනය:** SRAM සහ DRAM අතර වෙනස දක්වන්න. Cache memory සඳහා භාවිතා කරන්නේ මින් කුමක්ද? ඒ මන්ද?
**💡 පැහැදිලි කිරීම:** SRAM කියන්නේ flip-flops වලින් හදන, වේගවත් හැබැයි ගණන් වැඩි එක. DRAM කියන්නේ capacitors වලින් හදන, නිතරම refresh කරන්න ඕනේ, ගණන් අඩු එක. Cache වලට පාවිච්චි කරන්නේ SRAM, මොකද ඒක විතරයි CPU එකේ වේගයට සමානව වැඩ කරන්නේ.

**✍️ Exam Answer:**
* **SRAM (Static RAM):** Built using flip-flops. It is extremely fast, expensive per byte, physically larger, and retains its data as long as power is supplied without needing to be refreshed.
* **DRAM (Dynamic RAM):** Built using capacitors. It is slower, much cheaper, physically dense (allowing massive capacities), but its capacitors leak charge, meaning it must be constantly refreshed thousands of times a second to prevent data loss.
* **Which is used for Cache:** **SRAM** is exclusively used for Cache memory because its lightning-fast speed perfectly matches the CPU's requirements, preventing pipeline stalls. DRAM is too slow for Cache but perfect for Main Memory.
* **🎯 Marking Scheme:** 3 marks for SRAM features. 3 marks for DRAM features. 2 marks for selecting SRAM for Cache and giving the reason.

#### b. Explain "Direct Mapping" in Cache memory and state its primary disadvantage. [7 marks]
**❓ සිංහල පරිවර්තනය:** Cache මතකයේ ඇති "Direct Mapping" පැහැදිලි කර, එහි ඇති ප්‍රධාන අවාසිය සඳහන් කරන්න.
**💡 පැහැදිලි කිරීම:** RAM එකේ තියෙන block එකක් Cache එකේ අනිවාර්යයෙන්ම දාන්න ඕනේ තැන (specific line) කලින්ම fix කරලා තියෙන ක්‍රමය. අවාසිය තමයි එකම තැනට යන්න ඕනේ blocks දෙකක් නිතරම ආවොත්, ඒ දෙක මාරුවෙන් මාරුවට delete කර කර අලුතින් දාන්න වෙනවා (Conflict miss).

**✍️ Exam Answer:**
* **Direct Mapping:** This is a cache placement policy where each specific block of main memory is mathematically mapped to one, and *only one*, specific line in the cache memory (usually calculated using modulo arithmetic).
* **Disadvantage:** It suffers from high **Conflict Misses**. If a program alternately accesses two different memory blocks that happen to map to the exact same cache line, they will constantly overwrite (evict) each other, destroying the cache hit rate (a phenomenon known as thrashing).
* **🎯 Marking Scheme:** 4 marks for definition (one-to-one mapping). 3 marks for disadvantage (conflict misses/thrashing).

### 🔹 Part (ii) - Virtual Memory (20 Marks)

> [!TIP]
> **Short Note: Virtual Memory**
> HDD/SSD space acting as fake RAM. When RAM is full, inactive pages are swapped to disk.

#### a. Explain the concept of "Virtual Memory" and how it benefits a modern Operating System. [10 marks]
**❓ සිංහල පරිවර්තනය:** "Virtual Memory" සංකල්පය පැහැදිලි කර, එය නවීන මෙහෙයුම් පද්ධතියකට (OS) ප්‍රයෝජනවත් වන්නේ කෙසේදැයි විස්තර කරන්න.
**💡 පැහැදිලි කිරීම:** RAM එක පිරුණාම, Hard disk එකේ (SSD එකේ) තියෙන ඉඩ පාවිච්චි කරලා RAM එක ලොකුයි වගේ පෙන්නන ක්‍රමය. මේක නිසා RAM එකේ ඉඩට වඩා ලොකු Games/Softwares run කරන්නත්, ගොඩක් Softwares එකවර run කරන්නත් පුළුවන්.

**✍️ Exam Answer:**
* **Concept:** Virtual memory is a sophisticated memory management technique implemented jointly by the OS and the hardware (MMU). It creates the illusion for software that there is a massive, contiguous block of main memory available, even if physical RAM is limited. It achieves this by seamlessly using a portion of secondary storage (like an SSD) as a temporary extension of physical RAM.
* **Benefits:** 
  1. It allows programs that are significantly larger than the available physical RAM to execute by loading them in small chunks (pages).
  2. It allows many programs to run simultaneously (multitasking) without running out of memory.
  3. It provides strong memory isolation and security, preventing one program from accessing another program's memory space.
* **🎯 Marking Scheme:** 4 marks for concept (SSD acting as RAM extension). 6 marks for benefits (2 marks x 3 benefits).

#### b. What is a "Page Fault" and how does the Operating System handle it? [10 marks]
**❓ සිංහල පරිවර්තනය:** "Page Fault" එකක් යනු කුමක්ද සහ මෙහෙයුම් පද්ධතිය (OS) එය හසුරුවන්නේ කෙසේද?
**💡 පැහැදිලි කිරීම:** CPU එකට ඕන කරන කොටසක් (Page එකක්) RAM එකේ නැතුව Hard disk එකට යවලා තිබුණොත් ඒකට කියන්නේ Page Fault කියලා. එතකොට OS එක කරන්නේ, දැනට වැඩ කරන එක pause කරලා, ඒ ඕන කරන කොටස Hard disk එකෙන් හොයාගෙන ආයේ RAM එකට ගෙනත් දාලා, වැඩේ ආයේ පටන් ගන්න එක.

**✍️ Exam Answer:**
* **What it is:** A page fault is an exception (hardware trap) that occurs when the CPU attempts to access a block of memory (a "page") that is part of the program's virtual memory space but is currently *not* loaded into the physical RAM (it has been swapped out to the hard drive).
* **How it is handled (Steps):**
  1. The MMU detects the missing page and triggers a page fault interrupt to the OS.
  2. The OS pauses the currently executing process.
  3. The OS locates the required page on the secondary storage (SSD/HDD).
  4. The OS loads this page into a free frame in physical RAM (if RAM is full, it evicts an old page first using an algorithm like LRU).
  5. The OS updates the Page Table to reflect the new physical address.
  6. The OS restarts the paused instruction, which now succeeds.
* **🎯 Marking Scheme:** 4 marks for definition (accessing a page not in RAM). 6 marks for the handling steps logically presented.

<br><hr><br>

## 📝 Question 03 [35 Marks]
**📌 ආවරණය වන දේශන:** L12 (Input-Output Systems), L4 (Interrupts)

### 🔹 Part (i) - I/O Techniques (20 Marks)

#### a. Explain "Programmed I/O" and state its major drawback. [10 marks]
**❓ සිංහල පරිවර්තනය:** "Programmed I/O" පැහැදිලි කර, එහි ප්‍රධාන දුර්වලතාවය සඳහන් කරන්න.
**💡 පැහැදිලි කිරීම:** CPU එක නිතරම ගිහින් I/O device (උදා: Keyboard) එකෙන් අහනවා "වැඩේ ඉවරද, වැඩේ ඉවරද" කියලා. මේකට කියන්නේ Polling කියලා. මේකේ ප්‍රධාන දුර්වලතාවය තමයි I/O device එක වැඩේ ඉවර කරනකම් CPU එකට වෙන කිසිම වැඩක් නොකර බලාගෙන ඉන්න වෙන එක (busy-waiting / CPU cycles නාස්ති වීම).

**✍️ Exam Answer:**
* **Programmed I/O:** This is the simplest method of I/O communication. The CPU initiates an I/O request and then enters a tight loop, constantly polling the I/O device's status register over and over again to check if the device is ready or has completed the data transfer. 
* **Major Drawback:** It results in a massive waste of CPU cycles. This constant polling is known as **"busy-waiting"**. Because mechanical I/O devices are extremely slow compared to the CPU, the CPU spends 99% of its time just waiting doing nothing productive, severely degrading the overall performance of the entire computer system.
* **🎯 Marking Scheme:** 5 marks for explanation (polling). 5 marks for drawback (busy-waiting / wasted cycles).

#### b. How does "Interrupt-driven I/O" effectively solve the problem associated with Programmed I/O? [10 marks]
**❓ සිංහල පරිවර්තනය:** "Interrupt-driven I/O" මගින් Programmed I/O හි ඇති ගැටලුව ඵලදායී ලෙස විසඳන්නේ කෙසේද?
**💡 පැහැදිලි කිරීම:** මේකෙදි CPU එක I/O device එකට වැඩේ බාර දීලා වෙන වැඩක් කරන්න යනවා. I/O device එක වැඩේ ඉවර වුණාම CPU එකට signal එකක් (interrupt එකක්) එවනවා. එතකොට CPU එකට අර කලින් වගේ රස්තියාදු වෙන්න (busy-waiting) වෙන්නේ නෑ.

**✍️ Exam Answer:**
* Interrupt-driven I/O completely eliminates the need for the CPU to poll the device.
* **How it works:** The CPU issues the I/O command to the device controller and then immediately moves on to execute other useful tasks (e.g., running another program). 
* When the I/O device has finally prepared the data and is ready to transfer, it sends a dedicated hardware signal called an **Interrupt** to the CPU. 
* The CPU finishes its current instruction, pauses its current task, jumps to an Interrupt Service Routine (ISR) to handle the data transfer, and then smoothly resumes its original task. This guarantees that zero CPU cycles are wasted on waiting.
* **🎯 Marking Scheme:** 5 marks for explaining the mechanism (CPU moves on, device sends signal). 5 marks for explaining how it solves the problem (eliminates polling/wasting cycles).

### 🔹 Part (ii) - Exceptions vs Interrupts (15 Marks)

#### Explain the fundamental difference between an Hardware Interrupt and a Software Exception (Trap). Provide an example for each. [15 marks]
**❓ සිංහල පරිවර්තනය:** Hardware Interrupt එකක් සහ Software Exception (Trap) එකක් අතර මූලික වෙනස පැහැදිලි කරන්න. ඒ සෑම එකක් සඳහාම උදාහරණයක් සපයන්න.
**💡 පැහැදිලි කිරීම:** Hardware Interrupt එකක් එන්නේ බාහිරින් (උදා: Keyboard, Mouse). ඒක කවදා එයිද කියන්න බෑ (Asynchronous). Software Exception එකක් කියන්නේ program එක ඇතුළේම සිදුවෙන දෝෂයක් (උදා: බිංදුවෙන් බෙදීම). ඒක අනිවාර්යයෙන්ම ඒ code එක run වෙද්දී එනවා (Synchronous).

**✍️ Exam Answer:**
* **Hardware Interrupt:**
  * **Nature:** Asynchronous. It is generated by external hardware components, independently of the CPU clock and the currently executing instruction. It can happen at any unpredictable time.
  * **Purpose:** To signal the CPU that an external event requires immediate attention.
  * **Example:** A user presses a key on the keyboard, or a network card receives a data packet.
* **Software Exception (Trap):**
  * **Nature:** Synchronous. It is generated internally by the CPU itself specifically during the execution of a faulty or exceptional instruction. It is completely predictable (running the exact same code will always cause the exact same exception at the exact same place).
  * **Purpose:** To handle software errors or invoke special OS services.
  * **Example:** A program attempts a "division by zero", tries to access unauthorized memory (segmentation fault), or triggers a page fault.
* **🎯 Marking Scheme:** 
  * Interrupt: 4 marks for definition (Asynchronous/External), 3.5 marks for example. 
  * Exception: 4 marks for definition (Synchronous/Internal error), 3.5 marks for example.
