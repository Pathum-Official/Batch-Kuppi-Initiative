---
course: MAT 1013
title: 02. Truth Tables and Logical Equivalence
---

# 02. Truth Tables and Logical Equivalence
### සත්‍යතා වගු සහ තාර්කික සමතුල්‍යතාව (Lesson 2)

> [!NOTE] 
> **මොකක්ද මේ පාඩම? ඇයි අපි මේක ඉගෙන ගන්නේ?**
> පරිගණකයක ඇතුලේ වැඩ කරන්නේ 1 සහ 0 (True and False). අපි පරිගණකයට දෙන ලොකු කමාන්ඩ් එකක් (උදා: `if (A and not B or C)`) ඇත්තටම වැඩ කරන්නේ කොහොමද කියලා බලාගන්න අපි **සත්‍යතා වගු (Truth Tables)** පාවිච්චි කරනවා.
> ඒ වගේම, ක්‍රමලේඛකයින් දෙන්නෙක් එකම වැඩේ කරන්න ලියපු කේත (Code) දෙකක් සම්පූර්ණයෙන්ම සමානද කියලා බලන්න අපි **Logical Equivalence (තාර්කික සමතුල්‍යතාව)** පාවිච්චි කරනවා. මේක Computer Architecture සහ Logic Design වලදී අතිශයින්ම වැදගත්!

---

## 1. Truth Tables (සත්‍යතා වගු)

කලින් පාඩමේ ඉගෙන ගත්තු $P \wedge Q$ වගේ පොඩි කෑලි එකතු කරලා හදන ලොකු වාක්‍යයක අවසාන උත්තරය True ද False ද කියලා එකපාරටම හිතින් කියන්න අමාරුයි. ඒ නිසා අපි ඒකට වගුවක් අඳිනවා.

> [!IMPORTANT]
> **Key Definition (විභාගයට ලියන ඉංග්‍රීසි නිර්වචනය):**
> A **truth table** is a table that lists all possible combinations of truth values for the propositional variables in a logical expression, and shows the resulting truth value of the entire expression.
> *(ප්‍රකාශනයක තියෙන්න පුළුවන් හැම True/False කම්බිනේෂන් එකක්ම දාලා, අවසාන උත්තරේ පෙන්නන වගුව).*

### පේළි ගණන (Number of Rows) හොයන රහස
විචල්‍යයන් (Variables - ඒ කියන්නේ $p, q, r$ වගේ අකුරු) $n$ ගාණක් තියෙනවා නම්, වගුවේ පේළි ගණන අනිවාර්යයෙන්ම **$2^n$** ක් වෙන්න ඕනෙ.
- අකුරු 2ක් නම් ($p, q$): $2^2 = 4$ පේළි.
- අකුරු 3ක් නම් ($p, q, r$): $2^3 = 8$ පේළි.

**මතක තියාගන්න ලේසි ක්‍රම (Shortcuts for basic tables):**
- **AND ($\wedge$):** දෙකම True වුණොත් විතරක් True වේ. නැත්නම් False.
- **OR ($\vee$):** එකක් හරි True නම් True. (දෙකම False වුණොත් විතරක් False).
- **IMPLIES ($\rightarrow$):** පළවෙනි එක True වෙලා දෙවෙනි එක False වුණොත් විතරක් **False** වේ. අනිත් හැම වෙලාවෙම True!
- **IFF ($\leftrightarrow$):** දෙකම සමාන නම් (දෙකම T හෝ දෙකම F) True වේ.

---

## 2. Tautology and Contradiction (සර්වසත්‍යය සහ පරස්පරය)

විභාගයේදී නිතරම අසන ප්‍රශ්නයකි: "Is this a tautology?" (මෙය සර්වසත්‍යයක්ද?). 

| Term | Sinhala Meaning | English Definition (විභාගයට ලියන්න) | Example |
| :--- | :--- | :--- | :--- |
| **Tautology** | සර්වසත්‍යය | "A proposition that is **always true**." (සත්‍යතා වගුවේ අවසාන තීරුවේ සියල්ල 'T' නම්). | $p \vee \neg p$ |
| **Contradiction** | පරස්පරය | "A proposition that is **always false**." (සත්‍යතා වගුවේ අවසාන තීරුවේ සියල්ල 'F' නම්). | $p \wedge \neg p$ |

---

## 3. Logical Equivalence (තාර්කික සමතුල්‍යතාව - $\equiv$)

වාක්‍ය දෙකක් බැලූ බැල්මට වෙනස් වගේ පෙනුණත්, ඒ දෙකෙන් කියවෙන්නේ එකම අදහස වෙන්න පුළුවන්. ඒක ඔප්පු කරන්නේ මෙහෙමයි:

> [!IMPORTANT]
> **Definition:** Two compound propositions are **logically equivalent** if they have the same truth value for every possible assignment.
> *(සත්‍යතා වගු දෙකක අවසාන තීරු දෙක සම්පූර්ණයෙන්ම සමාන නම්, එම ප්‍රකාශන දෙක Logically Equivalent වේ. මෙය $\equiv$ ලකුණින් පෙන්වයි).*

### De Morgan's Laws (ඩි මෝගන් නීති) - විභාගයට අනිවාර්යයි!
වරහනකින් එළියේ ඇති NOT ($\neg$) ලකුණක් ඇතුළට දාන විට සිදුවන දේ මෙයින් කියැවේ. ලකුණ ඇතුළට යද්දී $\wedge$ එක $\vee$ වෙනවා. $\vee$ එක $\wedge$ වෙනවා!
1. $\neg(p \wedge q) \equiv \neg p \vee \neg q$
2. $\neg(p \vee q) \equiv \neg p \wedge \neg q$

---

## 4. Exam Question Walkthrough (විභාග ප්‍රශ්නයක් විසඳමු)

**Question: "Show that $p \rightarrow q$ is logically equivalent to $\neg p \vee q$ using a truth table."**
*(ප්‍රශ්නය: $p \rightarrow q$ සහ $\neg p \vee q$ යනු සමතුල්‍ය බව සත්‍යතා වගුවක් ඇඳ ඔප්පු කරන්න).*

**How to Write the Answer (විභාගයට ලියන නිවැරදි පියවර):**

1. **Step 1: අකුරු කීයද බලන්න.** මෙහි ඇත්තේ $p$ සහ $q$ පමණි. ඒ නිසා $2^2 = 4$ පේළි අඳින්න.
2. **Step 2: වගුව අඳින්න.** අවශ්‍ය වෙන හැම කෑල්ලටම (column) එකක් බැගින් අඳින්න.

| $p$ | $q$ | $\neg p$ | $p \rightarrow q$ | $\neg p \vee q$ |
|:---:|:---:|:---:|:---:|:---:|
| T | T | F | **T** | **T** |
| T | F | F | **F** | **F** |
| F | T | T | **T** | **T** |
| F | F | T | **T** | **T** |

3. **Step 3: විභාගයට ලියන අවසාන වාක්‍යය (Conclusion).**
   *"As seen in the truth table, the column for $p \rightarrow q$ and the column for $\neg p \vee q$ have identical truth values for every possible assignment. Therefore, they are logically equivalent."*

> [!WARNING]
> වගුව විතරක් ඇඳලා නිකන් ඉන්න එපා. යටින් අනිවාර්යයෙන්ම **"Therefore, they are logically equivalent"** කියලා ලියන්නම ඕනෙ. නැත්නම් ලකුණු අඩුවෙනවා!

---

## 5. Logical Puzzle Analysis (ප්‍රහේලිකාවක් විසඳමු)

**ප්‍රහේලිකාව:** 
යහළුවන් 4 දෙනෙක් (Gregory, April, August, June) ජනේලයක් කැඩුවා යැයි චෝදනා ලබා ඇත. ඔවුන් කියන දේවල් මෙසේය:
- **Gregory:** "June did it." (June තමයි කැඩුවේ)
- **April:** "August did not do it." (August කැඩුවේ නෑ)
- **August:** "April did not do it." (April කැඩුවේ නෑ)
- **June:** "Gregory lied when he said I did it." (Gregory බොරු කියන්නේ)

*If only one person is telling the truth, who broke the window? (එක් අයෙක් පමණක් ඇත්ත කියන්නේ නම් ජනේලය කැඩුවේ කවුද?)*

**විසඳන ආකාරය (Step-by-step Logical Approach):**
1. හොඳින් බලන්න, Gregory ගේ ප්‍රකාශය සහ June ගේ ප්‍රකාශය එකිනෙකට සම්පූර්ණයෙන්ම විරුද්ධයි (Opposites / Negations). 
   - එනම්, Gregory ඇත්ත කියනවා නම් June බොරු කියන්න ඕනෙ. June ඇත්ත කියනවා නම් Gregory බොරු කියන්න ඕනෙ. 
2. මෙයින් අදහස් වෙන්නේ, මේ දෙන්නගෙන් අනිවාර්යයෙන්ම **එක්කෙනෙක් ඇත්ත කියනවාමයි** කියන එකයි.
3. ප්‍රශ්නයේ දීලා තියෙනවා "ඇත්ත කියන්නේ එක්කෙනයි (only one person is telling the truth)" කියලා. ඒ කියන්නේ ඒ ඇත්ත කියන එක්කෙනා Gregory හරි June හරි වෙන්නම ඕනෙ.
4. ඒ නිසා, අනිත් දෙන්නා (April සහ August) අනිවාර්යයෙන්ම **බොරු කියන්න ඕනෙ!**
5. April කියන්නේ "August did not do it" කියලා. හැබැයි එයා කියන්නේ බොරුවක්! එහෙනම් ඒකෙ ඇත්ත තත්ත්වය මොකක්ද? **August තමයි ජනේලය කඩලා තියෙන්නේ!**

*(විභාගයකදී මේ වගේ ප්‍රශ්නයක් ආවොත්, මෙන්න මේ වගේ පියවරෙන් පියවර තර්ක කරන විදිහ ඉංග්‍රීසියෙන් පැහැදිලි කරන්න).*
