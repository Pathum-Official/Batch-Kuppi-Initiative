---
course: MAT 1013
title: 04. Arguments and Valid Reasoning
---

# 04. Arguments and Valid Reasoning
### තර්ක ගොඩනැගීම සහ වලංගුභාවය (Lesson 4)

> [!NOTE] 
> **මොකක්ද මේ පාඩම? ඇයි අපි මේක ඉගෙන ගන්නේ?**
> පරිගණකයකට (විශේෂයෙන්ම Artificial Intelligence එකකට) හිතන්න පුළුවන් වෙන්නේ කොහොමද? AI එකකට දේවල් කිහිපයක් කිව්වම (උදා: "බල්ලන්ට වලිගයක් ඇත", "ටොමී යනු බල්ලෙකි"), ඒ දේවල් දෙකෙන් AI එක අලුත් නිගමනයකට එනවා ("ටොමීට වලිගයක් ඇත"). මේකට කියන්නේ Automated Reasoning කියලා. මේ විදිහට කරුණු කිහිපයක් එකතු කරලා අලුත් නිගමනයකට එන එක ගණිතානුකූලව හරියටම කරන්නේ කොහොමද කියලයි අපි මේ පාඩමෙන් ඉගෙන ගන්නේ.

---

## 1. What is an Argument? (තර්කයක් යනු කුමක්ද?)

> [!IMPORTANT]
> **Key Definition (විභාගයට ලියන ඉංග්‍රීසි නිර්වචනය):**
> An **argument** is a sequence of propositions in which some propositions, called **premises** (හේතු/සාධක), are used to support another proposition, called the **conclusion** (නිගමනය).
> *(තර්කයක් කියන්නේ, හේතු කාරණා (premises) කිහිපයක් පාවිච්චි කරලා අලුත් නිගමනයකට (conclusion) එන එකටයි).*

**General Form (සාමාන්‍ය ආකෘතිය):**
Premise 1 (පළමු සාධකය)
Premise 2 (දෙවන සාධකය)
$\vdots$
$\therefore$ Conclusion (නිගමනය)
*(මෙහි $\therefore$ ලකුණින් "Therefore" හෙවත් "එමනිසා" යන්න අදහස් වේ).*

**උදාහරණයක් බලමු:**
- **Premise 1:** If it rains, then the ground is wet. (වැස්සොත් බිම තෙමෙනවා).
- **Premise 2:** It is raining. (දැන් වහිනවා).
- **$\therefore$ Conclusion:** The ground is wet. (එමනිසා, බිම තෙමී ඇත).

---

## 2. Validity vs. Truth (වලංගුභාවය සහ සත්‍යතාව අතර වෙනස)

මේක විභාගයේදී ළමයි නිතරම වරද්දන තැනක්! 
තර්කයක් "Valid (වලංගුයි)" කියන්නේ, ඒකෙ **ආකෘතිය (Pattern එක) හරි** කියන එකටයි. ඒක සැබෑ ලෝකයේ ඇත්තද බොරුද කියන එක අදාළම නෑ!

**උදාහරණයක්:**
- Premise 1: All cats are birds. (පූසෝ ඔක්කොම කුරුල්ලෝය). $\to$ *මේක සැබෑ ලෝකේ බොරුවක් (False).*
- Premise 2: Tom is a cat. (ටොම් කියන්නේ පූසෙකි).
- $\therefore$ Conclusion: Tom is a bird. (ඒ නිසා ටොම් කුරුල්ලෙකි).

මේ කතාව සැබෑ ලෝකේ බොරු වුණාට, මේක **Valid Argument** එකක්! මොකද කතාවේ pattern එක හරි (පළවෙනි කාරණා දෙක ඇත්ත කියලා හිතුවොත්, අනිවාර්යයෙන්ම තුන්වෙනි කාරණාව ඇත්ත වෙනවනේ).

> [!WARNING]
> **විභාගයට මතක තියාගත යුතු රහසක්:**
> "A valid argument can have false premises, but it **cannot** have true premises and a false conclusion!"
> *(වලංගු තර්කයකට බොරු හේතු තියෙන්න පුළුවන්. හැබැයි හේතු ටික සේරම ඇත්ත වෙලා, අවසාන නිගමනය බොරු වෙන්න බෑ! එහෙම වුණොත් ඒක Invalid).*

---

## 3. Common Valid Argument Forms (නිතර හමුවන වලංගු ආකෘති)

විභාගයේදී නිතරම අසන වලංගු තර්ක රටාවන් කිහිපයක් පහත දැක්වේ. මේවා නම් වලින්ම මතක තබාගන්න!

| Name (නම) | Logical Form (ආකෘතිය) | Example (උදාහරණය) |
| :--- | :--- | :--- |
| **Modus Ponens** | $p \rightarrow q$ <br> $p$ <br> $\therefore q$ | වැස්සොත් තෙමෙනවා ($p \to q$). වහිනවා ($p$). ඒ නිසා තෙමෙනවා ($q$). |
| **Modus Tollens** | $p \rightarrow q$ <br> $\neg q$ <br> $\therefore \neg p$ | වැස්සොත් තෙමෙනවා ($p \to q$). තෙමිලා නෑ ($\neg q$). ඒ නිසා වැහැලා නෑ ($\neg p$). |
| **Hypothetical Syllogism** | $p \rightarrow q$ <br> $q \rightarrow r$ <br> $\therefore p \rightarrow r$ | පාඩම් කළොත් පාස් ($p \to q$). පාස් වුණොත් ගෙදරින් තෑගි දෙනවා ($q \to r$). ඒ නිසා, පාඩම් කළොත් තෑගි ලැබෙනවා ($p \to r$). |
| **Disjunctive Syllogism** | $p \vee q$ <br> $\neg p$ <br> $\therefore q$ | අංකය ඉරට්ටේ හෝ ඔත්තේ ($p \vee q$). එය ඉරට්ටේ නොවේ ($\neg p$). ඒ නිසා එය ඔත්තේ ($q$). |

---

## 4. Invalid Forms / Fallacies (අවලංගු තර්ක / නිතර කරන වැරදි)

මිනිසුන් නිතරම රැවටෙන, වලංගු යැයි පෙනෙන නමුත් ඇත්තටම **අවලංගු (Invalid)** වන තර්ක රටා දෙකක් තියෙනවා.

### 4.1 Affirming the Consequent (ප්‍රතිඵලය සත්‍ය යැයි ගැනීම)
* ආකෘතිය:
  $p \rightarrow q$
  $q$
  $\therefore p$
* **Invalid Example:** 
  If it rains, then the ground is wet. (වැස්සොත් බිම තෙමෙනවා).
  The ground is wet. (බිම තෙමිලා).
  $\therefore$ It rained. (එහෙනම් වහල තියෙන්න ඕනෙ).
* **ඇයි මෙය අවලංගු?** බිම තෙමෙන්න වෙන හේතුවක් තියෙන්නත් පුළුවන්! (උදා: කවුරුහරි වතුර දැම්මා නම්). ඒ නිසා බිම තෙමුණා කියලා අනිවාර්යයෙන් වැස්සා වෙන්නම අවශ්‍ය නැහැ.

### 4.2 Denying the Antecedent (හේතුව අසත්‍ය යැයි ගැනීම)
* ආකෘතිය:
  $p \rightarrow q$
  $\neg p$
  $\therefore \neg q$
* **Invalid Example:** 
  If I study, then I pass. (මම පාඩම් කළොත්, පාස් වෙනවා).
  I did not study. (මම පාඩම් කළේ නෑ).
  $\therefore$ I did not pass. (ඒ නිසා මම ෆේල්).
* **ඇයි මෙය අවලංගු?** පාඩම් නොකර වෙනත් හේතුවක් නිසාත් කෙනෙක්ට පාස් වෙන්න පුළුවන් (උදා: කලින් දැනුමක් තිබුණා නම්). ඒ නිසා මෙය අනිවාර්ය සත්‍යයක් නොවේ.

---

## 5. Exam Question Walkthrough (විභාග ප්‍රශ්නයක් විසඳමු)

**Question: "Determine whether the following argument is valid using a truth table: If I study, then I pass. I passed. Therefore, I studied."**
*(ප්‍රශ්නය: "මම පාඩම් කළොත් පාස් වේ. මම පාස් විය. එමනිසා මම පාඩම් කළෙමි" යන තර්කය සත්‍යතා වගුවක් භාවිතයෙන් වලංගුදැයි බලන්න).*

**How to Write the Answer:**

1. **Step 1: Translate to symbols (සංකේත වලට හරවන්න).**
   Let $p$: "I study" and $q$: "I pass".
   Premise 1: $p \rightarrow q$
   Premise 2: $q$
   Conclusion: $p$

2. **Step 2: Form the Implication (තර්කය එක සමීකරණයක් විදිහට ලියන්න).**
   තර්කයක් වලංගු වෙන්න නම්, "Premises වල ගුණිතය (AND) $\rightarrow$ Conclusion" කියන එක සර්වසත්‍යයක් (Tautology) වෙන්න ඕනෙ.
   The associated logical statement is: **$((p \rightarrow q) \wedge q) \rightarrow p$**.

3. **Step 3: Draw the truth table (වගුව අඳින්න).**

| $p$ | $q$ | $p \rightarrow q$ | $(p \rightarrow q) \wedge q$ | $((p \rightarrow q) \wedge q) \rightarrow p$ |
|:---:|:---:|:---:|:---:|:---:|
| T | T | T | T | **T** |
| T | F | F | F | **T** |
| F | T | T | T | **F** |
| F | F | T | F | **T** |

4. **Step 4: The Final Exam Sentence (නිගමනය ලිවීම).**
   "The final column of the truth table contains an 'F' (it is not a tautology). Therefore, the argument is **invalid**. (This is the fallacy of affirming the consequent)."
