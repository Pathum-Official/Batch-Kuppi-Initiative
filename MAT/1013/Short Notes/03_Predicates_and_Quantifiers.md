---
course: MAT 1013
title: 03. Predicates and Quantifiers
---

# 03. Predicates and Quantifiers
### ප්‍රාඛ්‍යාත සහ ප්‍රමාණක (Lesson 3)

> [!NOTE] 
> **මොකක්ද මේ පාඩම? ඇයි අපි මේක ඉගෙන ගන්නේ?**
> පරිගණකයක Database එකකින් දත්ත හොයද්දී අපි ලියනවා `SELECT * FROM Students WHERE marks > 50` කියලා. මෙතන "marks > 50" කියන එක හරියටම කාටද අදාළ වෙන්නේ කියලා අපි මුලින් දන්නේ නෑ. කවුරුහරි ළමයෙක්ගේ ලකුණු ඒකට දැම්මම තමයි ඒක ඇත්තද බොරුද කියලා තීරණය වෙන්නේ. ගණිතයේදී මෙන්න මේ වගේ දේවල් වලට තමයි අපි **"Predicates" (ප්‍රාඛ්‍යාත)** කියලා කියන්නේ.

---

## 1. Propositions vs. Predicates (ප්‍රස්තුත සහ ප්‍රාඛ්‍යාත)

* **Proposition (ප්‍රස්තුතය):** බැලූ බැල්මටම ඇත්තද බොරුද කියලා කියන්න පුළුවන් දේවල්. 
  *(උදා: $2 + 5 = 7$ කියන්නේ පැහැදිලිවම True. ඒ නිසා මේක Proposition එකක්).*
* **Predicate (ප්‍රාඛ්‍යාතය):** අකුරක් (variable) තියෙන නිසා, ඒ අකුරට අගයක් දෙනකම් ඇත්තද බොරුද කියන්න බැරි දේවල්.
  *(උදා: $x + 3 = 10$. මෙතන $x$ කියන්නේ 7 නම් මේක True. 7 නෙවෙයි නම් False. ඉතින් $x$ දන්නේ නැතුව මුකුත් කියන්න බැරි නිසා මේක Predicate එකක්).*

> [!IMPORTANT]
> **Key Definition (විභාගයට ලියන ඉංග්‍රීසි නිර්වචනය):**
> A **predicate** is a sentence containing one or more variables that becomes a proposition when values are assigned to the variables.
> *(අගයන් ආදේශ කළ විට ප්‍රස්තුතයක් බවට පත්වන විචල්‍යයන් අඩංගු වාක්‍යයකි).*

---

## 2. Quantifiers (ප්‍රමාණක)

ප්‍රාඛ්‍යාතයක් (Predicate) ප්‍රස්තුතයක් (Proposition) බවට පත් කරන්න පුළුවන් තවත් ක්‍රමයක් තමයි මේ **Quantifiers**. ඒ කියන්නේ අකුරක් (variable) වෙනුවට අපි කියනවා "මේක හැමෝටම අදාළයි" එහෙමත් නැත්නම් "මේකට හරියන එක්කෙනෙක් හරි ඉන්නවා" කියලා.

### 2.1 Universal Quantifier (සර්වත්‍ර ප්‍රමාණකය) - $\forall$
* **Symbol:** $\forall$ (මේක මතක තියාගන්න "All" කියන එකේ 'A' අකුර අනිත් පැත්ත හරවලා වගේ කියලා).
* **Meaning:** සියලුම / සෑම (For all, for every).
* **Example:** $\forall x \in \mathbb{R}, x^2 \ge 0$
  * **English:** "For every real number $x$, $x^2$ is greater than or equal to zero."
  * **Sinhala:** "සෑම තාත්වික සංඛ්‍යාවක් සඳහාම, එහි වර්ගය ධන හෝ බිංදුව වේ." (සෑම අගයකටම මේක හරියන නිසා මේ සම්පූර්ණ වාක්‍යය **True** වේ).

### 2.2 Existential Quantifier (අස්තිත්ව ප්‍රමාණකය) - $\exists$
* **Symbol:** $\exists$ ("Exists" කියන එකේ 'E' අකුර අනිත් පැත්ත හරවලා වගේ).
* **Meaning:** පවතී / අවම වශයෙන් එකක් හෝ ඇත (There exists, for some).
* **Example:** $\exists x \in \mathbb{Z}, x^2 = 4$
  * **English:** "There exists an integer $x$ such that $x^2 = 4$."
  * **Sinhala:** "වර්ගය 4 වන පරිදි නිඛිලයක් පවතී." (ඔව්, 2 සහ -2 තියෙනවා. ලෝකෙ එක ඉලක්කමක් හරි මේකට ගැලපෙනවා නම් මේ වාක්‍යය **True** වේ).

---

## 3. Multiple Quantifiers (බහු ප්‍රමාණක භාවිතය)

විභාගයේදී ළමයි නිතරම වරද්දන තැනක් තමයි මේක! විචල්‍යයන් කිහිපයක් තියෙනකොට අපි Quantifiers දෙකක් පාවිච්චි කරනවා.

> [!WARNING]
> **නිතර සිදුවන වැරැද්ද (Common Mistake):**
> Quantifiers වල අනුපිළිවෙල මාරු කළොත් මුළු කතාවම කණපිට හැරෙනවා! 
> උදාහරණයක් විදිහට:
> - $\forall x \exists y$ (Every person has someone they love - හැමෝම කාටහරි ආදරේ කරනවා. මෙතනදී එක එක්කෙනා ආදරේ කරන්නේ වෙනස් අයට වෙන්න පුළුවන්).
> - $\exists y \forall x$ (There is someone who is loved by everyone - හැමෝම ආදරේ කරන එකම එක විශේෂ කෙනෙක් ඉන්නවා). 
> මේ දෙකෙන් කියවෙන්නේ සම්පූර්ණයෙන්ම වෙනස් කතා දෙකක්!

**ගණිතමය උදාහරණයක් බලමු:**
1. **$\forall x \exists y \; (x + y = 0)$**
   - **තේරුම:** "ඕනෑම $x$ අගයක් සඳහා, ඊට ගැලපෙන $y$ අගයක් හොයාගන්න පුළුවන් (එකතුව බිංදුව වෙන්න)."
   - **සත්‍ය/අසත්‍ය බව:** මෙය **True**. මොකද $x=5$ නම් $y=-5$ ගන්න පුළුවන්. $y$ හි අගය $x$ මත රඳා පවතී (Dependent).
2. **$\exists y \forall x \; (x + y = 0)$**
   - **තේරුම:** "සියලුම $x$ අගයන්ටම හරියන එකම එක පොදු $y$ අගයක් තියෙනවා."
   - **සත්‍ය/අසත්‍ය බව:** මෙය **False**. මොකද 5 සහ 10 කියන දෙකටම එකම $y$ අගයක් දාලා බිංදුව හදාගන්න බැහැනෙ. 

---

## 4. Free and Bound Variables (නිදහස් සහ බැඳුණු විචල්‍යයන්)

* **Bound Variable:** Quantifier එකකින් පාලනය වන විචල්‍යයක්.
* **Free Variable:** Quantifier එකකින් පාලනය නොවන නිදහස් විචල්‍යයක්.

**උදාහරණයක්:**
$\forall x (x + y > 0)$
මෙහිදී $x$ යනු Bound variable එකකි (මොකද $\forall x$ කියන එකෙන් ඒක පාලනය වෙනවා). නමුත් $y$ ගැන මුකුත් කියල නෑ, ඒ නිසා ඒක Free variable එකකි. යම් වාක්‍යයක එක හරි Free variable එකක් තියෙනවා නම්, ඒක Proposition එකක් වෙන්නේ නෑ!

---

## 5. Exam Question Walkthrough (ප්‍රමාණක වල නිෂේධය - Negation)

විභාගයට අනිවාර්යයෙන්ම එන ප්‍රශ්නයක් තමයි දීලා තියෙන Quantifier වාක්‍යයක අනිත් පැත්ත (Negation එක) ලියන්න කියන එක.

> [!TIP]
> **De Morgan's Laws for Quantifiers (මතක තබාගත යුතු රහස):**
> 1. $\neg(\forall x P(x)) \equiv \exists x \neg P(x)$
>    *(හැමෝම ඇඳුම් ඇඳන් ඉන්නවා කියන එකේ විරුද්ධ අර්ථය වෙන්නේ "අඩුම තරමේ එකෙක් හරි ඇඳුම් නැතුව ඉන්නවා" කියන එකයි. $\forall$ එක $\exists$ වෙනවා!)*
> 2. $\neg(\exists x P(x)) \equiv \forall x \neg P(x)$
>    *(එකෙක් හරි පාස් වුණා කියන එකේ විරුද්ධ අර්ථය වෙන්නේ "හැමෝම ෆේල්" කියන එකයි).*

**Question: "Negate the following statement: $\forall x \in \mathbb{R}, x^2 \ge 0$"**
*(ප්‍රශ්නය: සෑම තාත්වික සංඛ්‍යාවකම වර්ගය ධන හෝ බිංදුව වේ යන්නෙහි නිෂේධය ලියන්න).*

**How to Write the Answer:**
1. Put a NOT sign in front: $\neg (\forall x \in \mathbb{R}, x^2 \ge 0)$
2. Change $\forall$ to $\exists$: $\exists x \in \mathbb{R}, \neg(x^2 \ge 0)$
3. Negate the math part ($\ge$ becomes $<$): $\exists x \in \mathbb{R}, x^2 < 0$

**Final Exam Answer:**
The negation is $\exists x \in \mathbb{R}, x^2 < 0$.
