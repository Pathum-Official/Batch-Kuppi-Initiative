---
course: MAT 1013
title: 01. Propositions and Logical Language
---

# 01. Propositions and Logical Language
### ප්‍රස්තුත සහ තාර්කික භාෂාව (Lesson 1)

> [!NOTE] 
> **මොකක්ද මේ පාඩම? ඇයි අපි මේක ඉගෙන ගන්නේ?**
> පරිගණකයකට වැඩසටහනක් (Program) ලියද්දී අපි නිතරම කියන දෙයක් තමයි "වැස්සොත් (If it rains) කුඩයක් අරන් යන්න, නැත්නම් (Else) තොප්පියක් දාන් යන්න" වගේ දේවල් (If-Else Conditions). මේවා හරිද වැරදිද කියලා පරිගණකයට තීරණය කරන්න අපි කතා කරන මේ සිංහල/ඉංග්‍රීසි භාෂාව තේරෙන්නේ නැහැ. ඒකට ගණිතමය භාෂාවක් ඕනෙ. අන්න ඒ භාෂාව (Logical Language) තමයි අපි මේ පාඩමෙන් ඉගෙන ගන්නේ.

---

## 1. ප්‍රස්තුතයක් (Proposition) කියන්නේ මොකක්ද? (From Zero!)

කවුරුහරි ඔබට දෙයක් කිව්වම, ඒක **"එක්කෝ ඇත්තක් (True), නැත්නම් බොරුවක් (False)"** කියලා ඔබට ස්ථිරවම කියන්න පුළුවන් නම්, අන්න ඒ කියපු දේට අපි කියනවා **Proposition (ප්‍රස්තුතයක්)** කියලා.

> [!IMPORTANT]
> **Key Definition (විභාගයට ලියන ඉංග්‍රීසි නිර්වචනය):**
> A **proposition** is a declarative statement that is either **true** or **false**, but not both.

**උදාහරණ වලින් තේරුම් ගනිමු:**
හිතන්න මම කියනවා, "2යි 3යි එකතු කළාම 5යි ($2+3=5$)". මේක ඇත්තක්ද බොරුවක්ද? ඇත්තක් (True). ඒ නිසා මේක Proposition එකක්. 
මම කිව්වොත් "2යි 3යි එකතු කළාම 10යි ($2+3=10$)", මේක ඇත්තක්ද බොරුවක්ද? මේක පැහැදිලිවම බොරුවක් (False). ඒක නිසා ඒකත් Proposition එකක්! (බොරුවක් වුණත් Proposition එකක් වෙනවා, මොකද අපිට ඒක බොරුවක් කියලා ස්ථිරවම කියන්න පුළුවන් නිසා).

**එහෙනම් Proposition එකක් නොවෙන්නේ මොනවාද?**
1. **Open sentences (විවෘත වාක්‍ය):** කවුරුහරි කිව්වොත් "$x + 2 = 5$". දැන් මේක ඇත්තක්ද බොරුවක්ද? අපිට කියන්න බෑ! මොකද අපි $x$ කියන්නේ කවුද කියලා දන්නේ නෑ. ($x=3$ වුණොත් ඇත්ත වෙනවා, වෙන එකක් වුණොත් බොරු වෙනවා). මෙන්න මේවා Proposition නෙවෙයි.
2. **Commands (අණ කිරීම්):** "දොර වහන්න! (Close the door)". මේකේ ඇත්තක් හරි බොරුවක් හරි තියෙනවද? නෑ.
3. **Questions (ප්‍රශ්න):** "දැන් වෙලාව කීයද?". මේකේ ඇත්තක් බොරුවක් නෑ.

| Type (වර්ගය) | Example (උදාහරණ) | Exam Sentence (විභාගයට ලියන විදිහ) |
| :--- | :--- | :--- |
| **Proposition** | `2 + 3 = 5` | "This is a proposition because it has a definitive truth value (True)." |
| **Proposition** | `2 + 3 = 6` | "This is a proposition because it has a definitive truth value (False)." |
| **Not a Proposition**| `x > 3` | "Not a proposition. The truth value depends on the variable $x$." |
| **Not a Proposition**| `Close the door.` | "Not a proposition. It is a command, so it has no truth value." |

---

## 2. Logical Connectives (තාර්කික සම්බන්ධක)

දැන් අපි පොඩි වාක්‍ය දෙකක් එකතු කරලා ලොකු වාක්‍ය හදමු. 

### 2.1 Conjunction (AND - සහ / $\wedge$)
* **තේරුම:** දේවල් දෙකක් "සහ" (AND) වලින් එකතු කළාම, මුළු කතාවම ඇත්තක් වෙන්නේ කෑලි දෙකම ඇත්තක් වුණොත් විතරයි.
* **උදාහරණය:** "මම කේක් කනවා **සහ** අයිස්ක්‍රීම් කනවා." කවුරුහරි මේක කිව්වොත් එයා අනිවාර්යයෙන් දෙකම කන්න ඕනෙ. එකක් හරි කෑවේ නැත්නම් එයා කිව්වේ බොරුවක්!
* **Exam Phrase:** "$P \wedge Q$ is true if and only if both $P$ and $Q$ are true."

### 2.2 Disjunction (OR - හෝ / $\vee$)
* **තේරුම:** "හෝ" (OR) වලින් එකතු කළාම, දෙකෙන් එකක් හරි ඇත්ත වුණොත් මුළු කතාවම ඇත්ත වෙනවා.
* **උදාහරණය:** "මම කේක් **හෝ** අයිස්ක්‍රීම් කනවා." මම කේක් විතරක් කෑවත් මම කිව්වේ ඇත්ත. අයිස්ක්‍රීම් විතරක් කෑවත් මම කිව්වේ ඇත්ත. දෙකම කෑවත් මම කිව්වේ ඇත්ත. (Logic වල OR කියන්නේ "එක්කෝ මේක, එක්කෝ අරක, නැත්නම් දෙකම" කියන එකයි. මේකට **Inclusive OR** කියනවා).
* **Exam Phrase:** "$P \vee Q$ is true if at least one of $P$ or $Q$ is true."

### 2.3 Negation (NOT - නොවේ / $\neg$)
* **තේරුම:** තියෙන කතාවේ අනිත් පැත්ත.
* **උදාහරණය:** $P$ කියන්නේ "වහිනවා" නම්, $\neg P$ කියන්නේ "වහින්නේ නෑ".
* **Exam Phrase:** "The negation $\neg P$ has the opposite truth value of $P$."

### 2.4 Implication (IF... THEN... - නම්... එවිට... / $\rightarrow$)
* **තේරුම:** පළවෙනි දේ වුණොත්, අනිවාර්යයෙන්ම දෙවෙනි දේ වෙන්න ඕනෙ කියන එක.
* **උදාහරණය:** "ඔබ විභාගය පාස් වුණොත් (P), මම ඔබට කාර් එකක් අරන් දෙනවා (Q)".
  - පාස් වුණා, කාර් එකකුත් අරන් දුන්නා $\implies$ මම කිව්ව දේ **ඇත්ත (True)**.
  - පාස් වුණා, හැබැයි මම කාර් එක අරන් දුන්නේ නෑ $\implies$ මම කිව්වේ **බොරුවක් (False)**. (මෙතන විතරයි $P \rightarrow Q$ බොරු වෙන්නේ!).
  - පාස් වුණේ නෑ, හැබැයි මම කාර් එක අරන් දුන්නා $\implies$ මම බොරුවක් කිව්වද? නෑ. මම කිව්වේ පාස් වුණොත් දෙනවා කියලා විතරයි, ෆේල් වුණොත් දෙන්නේ නෑ කියලා මම පොරොන්දු වුණේ නෑනෙ! ඒ නිසා මම එතනදී කාර් එකක් අරන් දුන්නත් මම කිව්ව දේ තාම **ඇත්ත (True)**. 
* **Exam Phrase:** "The implication $P \rightarrow Q$ is false only when $P$ is true and $Q$ is false."

### 2.5 Biconditional (IF AND ONLY IF - නම් සහ නම් පමණි / $\leftrightarrow$)
* **තේරුම:** දේවල් දෙකම හරියටම එකම වෙලාවට වෙන්න ඕනෙ.
* **Exam Phrase:** "$P \leftrightarrow Q$ is true exactly when $P$ and $Q$ have the same truth value."

---

## 3. විභාගයට එන උපක්‍රම: Translation (වාක්‍ය සංකේත වලට හැරවීම)

විභාගයේදී නිතරම ලැබෙන ගැටලුවක් තමයි ඉංග්‍රීසි වාක්‍යයක් දීලා ඒක $P \wedge Q$ වගේ සංකේත වලින් ලියන්න කියන එක.

**උපකල්පනය කරන්න (Let):**
$P$ : "I study" (මම පාඩම් කරනවා)
$Q$ : "I pass" (මම පාස් වෙනවා)

| Exam Question (ඉංග්‍රීසි වාක්‍යය) | Logical Form (සංකේතය) | ළමයි නිතර කරන වැරැද්ද (Common Mistake) |
| :--- | :--- | :--- |
| I study and I pass | $P \wedge Q$ | මේක හරි ලේසියි. හැමෝම හරියට ලියනවා. |
| If I study, then I pass | $P \rightarrow Q$ | මේකත් ලේසියි. "If" එක ගාව තියෙන අකුර තමයි ඊතලේ මුලට එන්නේ. |
| I pass **only if** I study | $Q \rightarrow P$ | **[WARNING]** ගොඩක් ළමයි මේක $P \rightarrow Q$ කියලා ලියනවා. "Only if" කියන්නේ "Then" කියන එකටමයි. ඒ නිසා "only if" වලට පස්සේ තියෙන දේ (P) තමයි ඊතලේ අගට එන්න ඕනෙ. අනිත් දේ (Q) ඊතලේ මුලට එන්න ඕනෙ. |
| I study **if and only if** I pass | $P \leftrightarrow Q$ | "if and only if" ආවොත් දෙපැත්තටම ඊතලේ තියෙන ලකුණ යොදන්න. |

---

## 4. Exam Question Walkthrough (විභාග ප්‍රශ්නයක් විසඳමු)

**Question: "Analyze the following statement, express it symbolically, and find its truth value: A number is even and greater than 10."**
*(ප්‍රශ්නය: "සංඛ්‍යාවක් ඉරට්ටේ වේ සහ 10ට වඩා විශාල වේ" යන වාක්‍යය සංකේතාත්මකව ලියා එහි සත්‍ය/අසත්‍ය බව දක්වන්න).*

**How to Write the Answer (විභාගයට ලියන නිවැරදි පියවර):**

1. **Step 1: Identify the basic propositions (මූලික වාක්‍ය ටික අකුරු වලට කඩා ගන්න).**
   Let $P$: "A number is even"
   Let $Q$: "A number is greater than 10"

2. **Step 2: Express symbolically (සංකේත වලින් ලියන්න).**
   The word "and" represents conjunction ($\wedge$).
   Therefore, the statement is: **$P \wedge Q$**

3. **Step 3: Decide truth value (ඇත්තද බොරුද තීරණය කරන්න).**
   "The truth value of this statement **cannot be given** (සත්‍ය අසත්‍ය බවක් දිය නොහැක). This is because the statement depends on an unknown variable (the number). For example, if the number is 12, the statement is True. If the number is 4, the statement is False."

*(මේ විදිහට පියවරෙන් පියවර විස්තර කරලා ලිව්වාම ඔබට විභාගයේදී සම්පූර්ණ ලකුණු ලැබෙනවා අනිවාර්යයි!)*
