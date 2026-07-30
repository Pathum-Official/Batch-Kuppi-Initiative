# 🗃️ General Purpose Registers (GPRs)

පරිගණකයක ගණනය කිරීම් සහ දත්ත හුවමාරුව කාර්යක්ෂම කිරීමට රෙජිස්ටර් (Registers) විශාල කාර්යභාරයක් ඉටු කරයි.

---

## 1. Special Purpose vs General Purpose Registers

* **පැරණි වාස්තු විද්‍යාවන් (Older architectures):**
  * පැරණි පරිගණක වල වැඩිපුරම තිබුණේ එක් එක් විශේෂිත කාර්යයකට පමණක් වෙන්වූ Special Purpose Registers ය.
  * *උදාහරණ:* Program counter, Stack pointer, Index register, Flag register, Accumulator.

* **නව වාස්තු විද්‍යාවන් (Newer architectures):**
  * වර්තමාන පරිගණක වල බහුලවම ඇත්තේ ඕනෑම කාර්යයකට භාවිතා කළ හැකි **General Purpose Registers (GPRs)** ය. (බොහෝ ප්‍රොසෙසර වල GPRs 32 ක් හෝ ඊට වැඩි ගණනක් ඇත).

### ඇයි නව ප්‍රොසෙසර වල GPRs වැඩිපුර පාවිච්චි කරන්නේ?
1. **පරිවර්තකයට ඇති පහසුව (Easy for compiler):** විචල්‍යයන් (Variables) වල අගයන් රෙජිස්ටර් වලට ලබාදීමට Compiler එකට පහසු වේ.
2. **වේගය (Speed):** රෙජිස්ටර් වල වේගය සාමාන්‍ය මතකයට (Memory) වඩා ඉතා ඉහළ ය.
3. **කේතය කුඩා වීම (Compact instruction encoding):** මතකයේ ලිපිනයක් සෙවීමට වඩා රෙජිස්ටරයක් සෙවීමට යන බිට් ගණන අඩු බැවින් (උදා: රෙජිස්ටර් 32 ක් සෙවීමට අවශ්‍ය වන්නේ බිට් 5 ක් පමණි), උපදෙස් සඳහා වැයවන ඉඩ ප්‍රමාණය අඩු වේ.

---

## 2. Load-Store Architecture සහ RISC

ඉහත කතා කළ GPRs බහුලවම භාවිතා වන්නේ Register-Register හෙවත් **Load-Store Architecture** එකකය. මෙම වාස්තු විද්‍යාව RISC (Reduced Instruction Set Computer) හි පදනම වේ.
* *උදාහරණ:* MIPS, ARM.

### Load-Store / GPRs භාවිතයේ වාසි (Pros):
* දත්ත වරක් මතකයෙන් රෙජිස්ටරයට ගත් පසු (`LOAD`), සියලුම ගණනය කිරීම් රෙජිස්ටර් ඇතුළතම සිදුවන බැවින් මතකයට යන වාර ගණන (Memory traffic) විශාල ලෙස අඩු වේ.
* Compiler එක මඟින් ඉතා කාර්යක්ෂම කේත (Efficient code) නිපදවයි.

### අවාසි (Cons):
* වැඩසටහනක් අතරතුර යම් Function එකක් (Procedure) කෝල් කළහොත් හෝ Interrupt එකක් පැමිණියහොත්, ඒ මොහොතේ රෙජිස්ටර් වල ඇති අගයන් සියල්ලම මතකයේ Save කර, නැවත Restore කළ යුතු වේ.
* රෙජිස්ටර් ගණන වැඩි වූ විට මේ සඳහා අමතර කාලයක් සහ ඉඩක් (Overhead) වැය වේ.
