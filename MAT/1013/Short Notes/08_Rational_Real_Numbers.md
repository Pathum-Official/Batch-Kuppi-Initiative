---
course: MAT 1013
title: 08. Rational Numbers, Real Numbers and Completeness
---

# 08. Rational Numbers, Real Numbers and Completeness
### පරිමේය සංඛ්‍යා, තාත්වික සංඛ්‍යා සහ පූර්ණතා ලක්ෂණය (Lesson 8)

> [!NOTE] 
> **මොකක්ද මේ පාඩම? ඇයි අපි මේක ඉගෙන ගන්නේ?**
> පරිගණකයක (Computer) එකකට සංඛ්‍යා මතක තියාගන්න පුළුවන් සීමාවක් තියෙනවා. අපි පරිගණකයට $\frac{1}{3}$ කියලා දුන්නොත් ඒක $0.333333...$ විදිහට අනන්තයටම යන නිසා පරිගණකය ඒක කොතනින් හරි කපලා දානවා (Rounding off). මේ නිසා Programming කරද්දී ලොකු ගණනය කිරීම් වලදී පොඩි පොඩි වැරදි (Precision errors) එනවා. මේ වැරදි එන්නේ ඇයි කියලා තේරුම් ගන්න නම් අපි ඉලක්කම් වල හැසිරීම, ඒ කියන්නේ "පරිමේය සහ අපරිමේය" සංඛ්‍යා ගැන හරියටම දැනගන්න ඕනෙ. 

---

## 1. Rational Numbers (පරිමේය සංඛ්‍යා - $\mathbb{Q}$)

> [!IMPORTANT]
> **Key Definition (විභාගයට ලියන ඉංග්‍රීසි නිර්වචනය):**
> The set of rational numbers ($\mathbb{Q}$) consists of all numbers that can be written as a fraction of two integers, where the denominator is not zero.
> $$\mathbb{Q} = \left\{ \frac{a}{b} : a, b \in \mathbb{Z}, b \neq 0 \right\}$$
> *(පූර්ණ සංඛ්‍යා දෙකක භාගයක් ලෙස ලිවිය හැකි ඕනෑම සංඛ්‍යාවක් පරිමේය වේ. හරය බිංදුව විය නොහැක).*

**Decimal Expansions (දශම ප්‍රසාරණය):**
විභාගයේදී දශම සංඛ්‍යාවක් දීලා ඒක පරිමේයද නැද්ද අහන්න පුළුවන්. 
සෑම පරිමේය සංඛ්‍යාවකම දශම අගය:
1. **එක්කෝ අවසන් වේ (Terminating):** උදා: $\frac{1}{4} = 0.25$
2. **නැතහොත් ආවර්ත වේ (Repeating):** උදා: $\frac{1}{3} = 0.33333\dots$, නැත්නම් $\frac{7}{11} = 0.636363\dots$

*හැබැයි අවසන් වෙන්නෙත් නැති, එකම රටාවකට ආවර්ත වෙන්නෙත් නැති ඉලක්කම් තියෙනවා (උදා: $0.1010010001\dots$). අන්න ඒවා තමයි **අපරිමේය (Irrational)** වෙන්නේ!*

---

## 2. Exam Question Walkthrough (The Irrationality of $\sqrt{2}$)

විභාගයේදී $\sqrt{2}$ හෝ $\sqrt{3}$ අපරිමේයයි කියලා ඔප්පු කරන්න අනිවාර්යයෙන්ම එනවා! මේක කරන්නේ "Proof by Contradiction" කියන ක්‍රමයටයි (ඒ කියන්නේ අපි මුලින්ම ඒක පරිමේයයි කියලා හිතලා, පස්සේ ඒක වැරදියි කියලා ඔප්පු කරනවා). මේ වාක්‍ය ටික මේ විදිහටම කටපාඩම් කරගන්න.

**Question: "Prove that $\sqrt{2}$ is irrational."**

**How to Write the Answer (විභාගයට ලියන පියවර):**

1. **Step 1: විරුද්ධ දේ උපකල්පනය කරන්න (Assume the opposite).**
   *"Assume for the sake of contradiction that $\sqrt{2}$ is rational."*
   *(එහෙනම් අපිට ඒක භාගයක් විදිහට ලියන්න පුළුවන් වෙන්න එපැයි).*

2. **Step 2: භාගයක් ලෙස ලියන්න (Apply definition).**
   *"Then we can write $\sqrt{2} = \frac{a}{b}$, where $a, b \in \mathbb{Z}$ and $b \neq 0$. We assume this fraction is in its simplest form, meaning $\gcd(a, b) = 1$."*
   *(මේ $\gcd(a, b) = 1$ කියන කෑල්ල අනිවාර්යයෙන්ම ලියන්න ඕනෙ. ඒකෙන් කියන්නේ මේ භාගය තවත් සුළු කරන්න බෑ කියන එකයි).*

3. **Step 3: වීජගණිතය සුළු කරන්න (Algebraic manipulation).**
   *"Squaring both sides and cross-multiplying gives:"*
   $$2 = \frac{a^2}{b^2} \implies a^2 = 2b^2$$

4. **Step 4: තර්කනය ගොඩනගන්න (Logical Deduction - Part 1).**
   *"Since $a^2$ is a multiple of 2, $a^2$ is even. Therefore, $a$ must also be even. So, we can write $a = 2k$ for some integer $k$."*

5. **Step 5: අලුත් අගය ආදේශ කරන්න (Substitute and Deduce - Part 2).**
   *"Substituting $a = 2k$ into our equation:"*
   $$(2k)^2 = 2b^2 \implies 4k^2 = 2b^2 \implies b^2 = 2k^2$$
   *"Since $b^2$ is a multiple of 2, $b^2$ is even. Therefore, $b$ must also be even."*

6. **Step 6: දෝෂය පෙන්වා නිගමනයට එන්න (The Contradiction and Conclusion).**
   *"Now we have shown that both $a$ and $b$ are even (they are both divisible by 2). This contradicts our initial assumption that $\gcd(a, b) = 1$ (that they have no common factors). Therefore, our assumption was false, and $\sqrt{2}$ must be irrational. (Q.E.D)."*

---

## 3. Real Numbers and Completeness (තාත්වික සංඛ්‍යා සහ පූර්ණතාව)

තාත්වික සංඛ්‍යා කුලකය $\mathbb{R}$ ලෙස දක්වන අතර එයට $\mathbb{Q}$ (පරිමේය) සහ අපරිමේය සංඛ්‍යා සියල්ලම අයිති වේ ($\mathbb{N} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R}$).

> [!IMPORTANT]
> **Completeness of Real Numbers (තාත්වික සංඛ්‍යා වල පූර්ණතාව):**
> $\mathbb{Q}$ (පරිමේය සංඛ්‍යා) වල නැති, නමුත් $\mathbb{R}$ වල තියෙන විශේෂ ලක්ෂණයක් තමයි "Completeness" කියන්නේ. 
> 
> **"Every non-empty subset of $\mathbb{R}$ that is bounded above has a least upper bound."**
> *(සරලව: යම් කුලකයකට උපරිම සීමාවක් (Upper bound) තියෙනවා නම්, ඒ කුලකයට අනිවාර්යයෙන්ම "වඩාත්ම නිවැරදි/ආසන්නතම උපරිම සීමාවකුත්" (Least upper bound) තියෙන්නම ඕනෙ).*

**ඇයි $\mathbb{Q}$ වලට මේක නැත්තේ?**
හිතන්න අපි කුලකයක් හදනවා "වර්ගය 2 ට වඩා අඩු පරිමේය සංඛ්‍යා" කියලා ($S = \{x \in \mathbb{Q} : x^2 < 2\}$). මේ කුලකයේ තියෙන ලොකුම අගය $\sqrt{2}$ වෙන්න ඕනෙ. හැබැයි $\sqrt{2}$ කියන්නේ පරිමේය සංඛ්‍යාවක් නෙවෙයිනෙ! ඒ නිසා $\mathbb{Q}$ කුලකය ඇතුලේ මේකට හරියටම උපරිම අගයක් දෙන්න බැහැ (හිඩැසක්/gap එකක් තියෙනවා). අන්න ඒ හිඩැස් සේරම පුරවන්නේ මේ $\mathbb{R}$ වලිනුයි. ඒකයි ඒකට "පූර්ණතාව (Completeness)" කියලා කියන්නේ.

---

## 4. Absolute Value (නිරපේක්ෂ අගය - $|x|$)

විභාගයේදී සමීකරණ විසඳන්න ආවොත් මේක ගොඩක් වැදගත්.

> [!NOTE]
> $|x| = \begin{cases} x, & x \ge 0 \\ -x, & x < 0 \end{cases}$
> *(මෙහි තේරුම නම්, $|x|$ මඟින් $x$ හි ධන හෝ ඍණ ලකුණ ඉවත් කර, හුදෙක් බිංදුවේ සිට ඇති දුර (Distance) පමණක් සලකන බවයි).*

**වටිනා නීතියක්:**
$\sqrt{x^2} = |x|$
*(බොහෝ ළමයි $\sqrt{x^2} = x$ කියා ලියා වරද්දා ගනී. උදා: $\sqrt{(-3)^2} = \sqrt{9} = 3$. එනම් $|-3|$ වේ).*
