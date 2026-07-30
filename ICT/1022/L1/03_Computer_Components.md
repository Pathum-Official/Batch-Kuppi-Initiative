# 🖥️ Components of a Computer System

පරිගණක පද්ධතියක ප්‍රධාන කොටස් සහ ඒවායේ ක්‍රියාකාරීත්වය තේරුම් ගැනීම සඳහා අප **Von-Neumann Architecture** (වොන්-නියුමාන් වාස්තු විද්‍යාව) භාවිතා කරයි. 

> [!TIP]
> **Von-Neumann Architecture හි මූලික සංකල්පය:**
> සියලුම උපදෙස් (Instructions) සහ දත්ත (Data) එකම මතකයක (Memory) ගබඩා කර තබන අතර, අවශ්‍ය වූ විට ප්‍රොසෙසරය (Processor) මඟින් ඒවා ලබාගෙන ක්‍රියාත්මක කරයි.

---

## 1. Processor (සකසනය / CPU)

Central Processing Unit (CPU) හෙවත් ප්‍රොසෙසරය පරිගණකයේ මොළය ලෙස ක්‍රියා කරයි. මෙහි ප්‍රධාන කාර්යය වන්නේ මතකයෙන් (Memory) උපදෙස් ලබාගෙන (Fetch), ඒවා තේරුම් ගෙන (Decode), අදාළ දත්ත මත ක්‍රියාත්මක කිරීමයි (Execute).

ප්‍රොසෙසරය ප්‍රධාන කොටස් 2 කින් සමන්විත වේ:

### A. Arithmetic Logic Unit (ALU)
සියලුම ගණනය කිරීම් (Calculations) සිදුවන්නේ මෙහිදීය.
* **Registers:** තාවකාලිකව දත්ත ගබඩා කර ගැනීමට General-purpose සහ Special-purpose රෙජිස්ටර් කිහිපයක් මෙහි අඩංගු වේ.
* **Logic Operations:** AND, OR, NOT, Shift, Compare වැනි තාර්කික ක්‍රියා සිදුකරයි.
* **Arithmetic Operations:** එකතු කිරීම (Addition), අඩු කිරීම (Subtraction), ගුණ කිරීම, බෙදීම වැනි ගණිතමය ක්‍රියා සිදුකරයි.

### B. Control Unit (පාලන ඒකකය)
මෙය පරිගණකයේ **ස්නායු මධ්‍යස්ථානය (Nerve Center)** ලෙස ක්‍රියා කරයි.
* අනෙකුත් සියලුම ඒකක වල තත්වය (State) නිරීක්ෂණය කරමින්, ඒවා පාලනය කිරීමට අවශ්‍ය **Control Signals (පාලන සංඥා)** නිකුත් කරයි.
* උදාහරණයක් ලෙස `R1 -> R2 + R3` යන ක්‍රියාව කිරීමට නම්:
  1. R2 සහ R3 රෙජිස්ටර් වල Output එක සක්‍රීය කිරීම.
  2. එකතු කිරීමේ (Addition) ක්‍රියාව තේරීම.
  3. ලැබෙන පිළිතුර නැවත R1 රෙජිස්ටරයේ ගබඩා කිරීම.
* උපදෙසක් (Instruction) මතකයෙන් ලබාගත් පසු, එහි ඇති Opcode එක (කළ යුතු ක්‍රියාව) Decode කර අදාළ සංඥා නිකුත් කරන්නේ Control Unit එක මඟිනි.

---

## 2. Memory Unit (මතක ඒකකය)

පරිගණකයේ මතකය ප්‍රධාන වශයෙන් කොටස් 2 කට බෙදිය හැක. (ප්‍රොසෙසරයට සෘජුවම සම්බන්ධ විය හැක්කේ ප්‍රාථමික මතකයට පමණි).

1. **Primary / Main Memory (ප්‍රාථමික මතකය):** දැනට ක්‍රියාත්මක වන වැඩසටහන් වලට අදාළ උපදෙස් (Active instructions) සහ දත්ත ගබඩා කර ගනී. (උදා: RAM, ROM)
2. **Secondary Memory (ද්විතියික මතකය):** Backup එකක් ලෙස සහ දැනට ක්‍රියාත්මක නොවන (Inactive) වැඩසටහන් සහ ලිපිගොනු (Files) ස්ථිරව ගබඩා කර තබා ගනී. (උදා: Hard Disks, SSDs)

> [!NOTE]
> වේගවත් මතකයකට පිවිසීමක් (Faster memory access) දැරිය හැකි මිලකට (Affordable cost) ලබාදීම සඳහා, මතකය **ස්ථර කිහිපයක් (Hierarchy)** ලෙස සකස් කර ඇත.
> *(L1 cache -> L2 cache -> L3 cache -> Primary memory -> Secondary memory)*

### විවිධ මතක වර්ග (Types of Memory)
* **RAM (Random Access Memory):** කියවීමට සහ ලිවීමට (Read/Write) එකම කාලයක් ගතවන, Cache සහ Primary මතකය සඳහා යොදාගන්නා මතකයකි.
* **ROM (Read Only Memory):** වෙනස් කළ නොහැකි ස්ථිර දත්ත ගබඩා කිරීමට භාවිතා කරයි.
* **Magnetic Disk:** ලෝහ තැටියක ඇති කුඩා චුම්භක අංශු භාවිතයෙන් දත්ත ගබඩා කරන ද්විතියික මතකයකි. (Hard drives).
* **Flash Memory:** Magnetic disks වෙනුවට දැන් බහුලව භාවිතා වේ. මේවා ඉතා වේගවත් වන අතර ප්‍රමාණයෙන් ද කුඩාය (SSD, Pen drives).

---

## 3. Input & Output Units (ආදාන සහ ප්‍රතිදාන ඒකක)

බාහිර ලෝකය (Outside world) සමග පරිගණකය සම්බන්ධ කිරීම මෙම ඒකක මඟින් සිදු කෙරේ.

### Input Unit (ආදාන ඒකකය)
බාහිර පරිසරයෙන් පරිගණකයට දත්ත ලබා දීමට (Feed data) භාවිතා කරයි. මෙහිදී දත්ත ලබාදී, ඒවා නිසි පරිදි කේතනය කර (Encoding) ප්‍රොසෙසරයට හෝ මතකයට යවයි.
* **උදාහරණ:** Keyboard, Mouse, Joystick, Camera, Scanner, Microphone.

### Output Unit (ප්‍රතිදාන ඒකකය)
පරිගණකය මඟින් කළ ගණනය කිරීම් වල (Computations) ප්‍රතිඵලය බාහිර ලෝකයට ලබාදීමට භාවිතා කරයි.
* **උදාහරණ:** LCD/LED Screen (Monitor), Printer, Plotter, Speaker, Buzzer, Projector.

---
> [!TIP]
> **ලැප්ටොප් පරිගණකයක ඇතුලත (Inside a laptop):** 
> ලැප්ටොප් වල සියලුම කොටස් ඉතා කුඩා කර (Miniaturization) ඇත. අද වන විට Hard Drives වෙනුවට Flash-based memory (SSD) ආදේශ වී ඇති අතර, සිසිලනය (Cooling) කිරීම ලැප්ටොප් වල ඇති ප්‍රධානතම අභියෝගයකි.
