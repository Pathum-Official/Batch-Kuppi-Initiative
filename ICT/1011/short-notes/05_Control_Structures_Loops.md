# 🚀 ICT 1011 Master Class: 05 - Control Structures (Loops)

> **මෙය ICT 1011 විෂය නිර්දේශයේ පස්වන කොටස සම්පූර්ණයෙන්ම ආවරණය කරන මහාචාර්ය මට්ටමේ (Professor-level) සටහනකි.**
> (For, While, Do-While loops සහ Break/Continue මෙහි අන්තර්ගත වේ).

---

## 1. Repetition Structures / Loops (ලූප / පුනරාවර්තන)
එකම කේත කොටසක් කිහිප වතාවක් නැවත නැවත ක්‍රියාත්මක කිරීමට ලූප (Loops) භාවිතා කරයි.

### 🔄 1. The `for` Loop
ලූප් එක ධාවනය කළ යුතු වාර ගණන (Number of iterations) කල්තියාම දන්නා විට මෙය භාවිතා කරයි.
මෙය කොටස් 3කින් සමන්විත වේ: `Initialization` (ආරම්භය), `Condition` (කොන්දේසිය), `Update` (වෙනස් වීම).

```java
// i හි අගය 1 සිට 5 දක්වා (වාර 5ක්) ධාවනය වේ.
for (int i = 1; i <= 5; i++) {
    System.out.println("Count: " + i);
}
```
* **Execution Flow:** `Initialization` සිදුවන්නේ එකම එක වරක් පමණි. ඉන්පසු `Condition` එක බලයි -> ඇතුළේ කේතය ක්‍රියාත්මක කරයි -> `Update` කරයි -> නැවත `Condition` බලයි (මේ චක්‍රය Condition එක False වන තුරු සිදුවේ).

### 🔄 2. The `while` Loop
ලූප් එක ධාවනය කළ යුතු වාර ගණන නොදන්නා විට සහ කොන්දේසියක් (Condition) සත්‍ය වන තාක් කල් පමණක් ධාවනය කිරීමට අවශ්‍ය විට මෙය භාවිතා කරයි. මෙහිදී පළමුව කොන්දේසිය පරීක්ෂා කර, පසුව කේතය ක්‍රියාත්මක කරයි (Entry-controlled loop).

```java
int count = 1; // Initialization (පිටතින්)
// කොන්දේසිය මුලින්ම පරීක්ෂා කරයි
while (count <= 5) {
    System.out.println("Count: " + count);
    count++; // Update කිරීම අමතක නොකරන්න! නැතිනම් Infinite Loop (නොනවතින ලූපයක්) සෑදේ.
}
```

### 🔄 3. The `do-while` Loop
මෙහිදී පළමුව කේතය එක් වරක් හෝ ක්‍රියාත්මක කර, ඉන්පසු අවසානයේදී කොන්දේසිය පරීක්ෂා කරයි (Exit-controlled loop). එමනිසා කොන්දේසිය අසත්‍ය (False) වුවද, කේතය **අඩුම තරමේ එක වරක් හෝ** අනිවාර්යයෙන්ම ධාවනය වේ.

```java
int count = 10;
do {
    // මේ කොටස අනිවාර්යයෙන්ම එක් වරක් ක්‍රියාත්මක වේ.
    System.out.println("Count is: " + count);
    count++;
} while (count <= 5); // කොන්දේසිය False වුවද, ඉහත කේතය එක් වරක් Run වී ඇත.
```

> [!CAUTION]
> **Professor's Trap (Semicolons in Loops):** 
> 1. `while (count <= 5);` ලෙස සාමාන්‍ය `while` loop එකක අගට semicolon (`;`) එකක් තැබුවහොත්, ලූපයට ඇතුලේ කේතයක් (body එකක්) නැති බව සිතා එය Infinite Loop එකක් බවට පත් වේ (count වැඩි වෙන්නේ නැති නිසා). වැඩසටහන හිර වෙයි!
> 2. නමුත්, `do-while` loop එකේ අගට අනිවාර්යයෙන්ම `;` තැබිය යුතුය! (උදා: `} while(count <= 5);`). මෙය විභාගයේදී නිතරම ලකුණු කපන තැනකි.

---

## 2. Loop Control Statements (`break` vs `continue`)

### 🛑 `break`
ලූපය සම්පූර්ණයෙන්ම නවතා දමා, ලූපයෙන් පිටතට (Exit) පැමිණේ.

```java
for (int i = 1; i <= 5; i++) {
    if (i == 3) {
        break; // i 3 වූ විට මුළු ලූපයම නවතී. 
    }
    System.out.println(i);
}
// Output: 
// 1
// 2
```

### ⏭️ `continue`
ලූපය සම්පූර්ණයෙන්ම නවත්වන්නේ නැත. ඒ වෙනුවට වත්මන් වටය (Current iteration) පමණක් මඟ හැර (Skip කර), ඊළඟ වටයට (Next iteration) ගමන් කරයි.

```java
for (int i = 1; i <= 5; i++) {
    if (i == 3) {
        continue; // i 3 වූ විට ඒ වටය පමණක් Skip වේ. 
    }
    System.out.println(i);
}
// Output: 
// 1
// 2
// 4 (3 නැත!)
// 5
```

> [!TIP]
> **Nested Loops වලදී Break/Continue භාවිතය:**
> ලූපයක් ඇතුළේ තව ලූපයක් ඇති විට (Nested Loops), `break` හෝ `continue` භාවිතා කළහොත්, ඉන් බලපෑමක් වන්නේ එය කෙලින්ම ඇතුළත්ව ඇති **අභ්‍යන්තරම ලූපයට (innermost loop) පමණි!** පිටත ලූපය (outer loop) සාමාන්‍ය පරිදි ධාවනය වේ.
