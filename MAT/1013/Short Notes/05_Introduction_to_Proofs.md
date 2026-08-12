---
course: MAT 1013
title: 05. Introduction to Proofs
---

# 05. Introduction to Proofs
### ගණිතමය සාධනය කිරීම් (Lesson 5)

> [!NOTE] 
> **මොකක්ද මේ පාඩම? ඇයි අපි මේක ඉගෙන ගන්නේ?**
> පරිගණක විද්‍යාවේදී (Computer Science) අපි ලියන Algorithm එකක් "හැම වෙලාවෙම හරියට වැඩ කරනවා" කියලා විශ්වාස කරන්නේ කොහොමද? බැංකුවක සල්ලි යවන System එකක් හැදුවොත්, ඒක එකපාරක්වත් වරදින්නේ නෑ කියලා අපිට ඔප්පු කරන්න (Prove කරන්න) වෙනවා. ගණිතයේදීත් එහෙමයි. යම් කිසි සමීකරණයක් හෝ කතාවක් ඇත්තද කියලා නිකන්ම පිළිගන්නේ නැතුව, "මේක මේ නිසාමයි වෙන්නේ" කියලා පියවරෙන් පියවර සාධනය කරන විදිහ (Proof techniques) තමයි මේ පාඩමේ තියෙන්නේ. විභාගයේදී මේකෙන් ලොකු ප්‍රශ්නයක් අනිවාර්යයෙන්ම එනවා!

---

## 1. Direct Proofs (සෘජු සාධනය)

Direct proof එකකදී අපි කරන්නේ, දීලා තියෙන දේ (Hypothesis) ඇත්ත කියලා උපකල්පනය කරලා, වීජගණිතය පාවිච්චි කරලා කෙලින්ම ගාණ හදාගෙන යන එකයි. 

> [!IMPORTANT]
> **විභාගයට මතක තබාගත යුතු මූලික නිර්වචන (Definitions):**
> මේ නිර්වචන නැතුව Proofs ලියන්නම බෑ! මේවා කටපාඩම් කරගන්න.
> - **Even (ඉරට්ටේ):** An integer $n$ is even if there exists an integer $k$ such that **$n = 2k$**.
> - **Odd (ඔත්තේ):** An integer $n$ is odd if there exists an integer $k$ such that **$n = 2k + 1$**.

### Exam Question Walkthrough (සෘජු සාධනයක් ලියන ආකාරය)

**Question: "Prove that if $n$ is an odd integer, then $n^2 - 1$ is divisible by 8."**
*(ප්‍රශ්නය: $n$ යනු ඔත්තේ නිඛිලයක් නම්, $n^2 - 1$ යන්න 8න් බෙදෙන බව සෘජුව ඔප්පු කරන්න).*

**How to Write the Answer (විභාගයට ලියන නිවැරදි පියවර):**

1. **Step 1: උපකල්පනය ලියන්න (Assume the hypothesis).**
   *"Let $n$ be an odd integer."*
2. **Step 2: නිර්වචනය යොදන්න (Apply the definition).**
   *"By definition of odd numbers, $n = 2k + 1$ for some integer $k$."*
3. **Step 3: වීජගණිතය සුළු කරන්න (Algebraic manipulation).**
   *"Now, consider $n^2 - 1$. Substituting $n = 2k + 1$:"*
   $$n^2 - 1 = (2k + 1)^2 - 1$$
   $$= (4k^2 + 4k + 1) - 1$$
   $$= 4k^2 + 4k$$
   $$= 4k(k + 1)$$
4. **Step 4: තර්කයක් ගොඩනගන්න (Logical reasoning).**
   *(මෙතනදී හිතන්න, $k$ සහ $(k+1)$ කියන්නේ ළඟින් තියෙන ඉලක්කම් දෙකක් (උදා: 3 සහ 4, නැත්නම් 6 සහ 7). ඒ දෙකෙන් එකක් අනිවාර්යයෙන්ම ඉරට්ටේ වෙනවනේ. ඉරට්ටේ සංඛ්‍යාවකින් ගුණ කළාම උත්තරේ ඉරට්ටේ වෙනවා).*
   *"Notice that $k(k + 1)$ is the product of two consecutive integers. One of them must be even. Therefore, their product $k(k + 1)$ is even, so we can write $k(k + 1) = 2m$ for some integer $m$."*
5. **Step 5: අවසාන නිගමනය (Conclusion).**
   *"Substitute this back: $n^2 - 1 = 4(2m) = 8m$. Since $8m$ is a multiple of 8, $n^2 - 1$ is divisible by 8. (Q.E.D)."*

---

## 2. Counterexamples (ප්‍රති-උදාහරණ මඟින් බොරු කිරීම)

යම් ප්‍රකාශයක් (Statement එකක්) **අසත්‍යයි (False)** කියලා පෙන්වන්න, මුළු ගාණම හදන්න ඕනෙ නෑ. ඒක වැරදෙන **එකම එක අවස්ථාවක්** (උදාහරණයක්) පෙන්නුවාම ඇති! ඒකට කියන්නේ Counterexample කියලා.

**Question:** Is the statement "For every integer $n$, $n^2 + n + 41$ is prime" true or false? If false, provide a counterexample.
*(ප්‍රශ්නය: සෑම $n$ සඳහාම $n^2 + n + 41$ ප්‍රථමක සංඛ්‍යාවක් වේ යන්න සත්‍යද අසත්‍යද? අසත්‍ය නම් ප්‍රති-උදාහරණයක් දෙන්න).*

**How to Write the Answer:**
"The statement is **false**. Let $n = 41$. Then:
$$n^2 + n + 41 = 41^2 + 41 + 41 = 41(41 + 1 + 1) = 41 \times 43$$
Since it can be factored into $41 \times 43$, it is NOT a prime number. Therefore, $n = 41$ is a counterexample."

---

## 3. Proof by Contrapositive (ප්‍රතිපක්ෂය මඟින් ඔප්පු කිරීම)

සමහර ගණන් තියෙනවා කෙලින්ම (Direct proof) හදන්න ගියාම අමාරුයි. ඒ වෙලාවට අපි ගාණ අනිත් පැත්ත හරවනවා!
$p \rightarrow q$ ඔප්පු කරනවා වෙනුවට, $\neg q \rightarrow \neg p$ ඔප්පු කරනවා. (මෙය Logical equivalence පාඩමේදී ඉගෙන ගත්තා මතකද?).

**Question: "Prove that if $n^2$ is even, then $n$ is even."**
*(මෙය කෙලින්ම හදන්න ගියොත් $n^2 = 2k$ කියලා අරන් $n = \sqrt{2k}$ කියලා ගන්න වෙනවා. වර්‍ගමූල ආවාම ගාණ අමාරුයි! ඒ නිසා අනිත් පැත්ත හරවමු).*

**How to Write the Answer:**
1. **ප්‍රතිපක්ෂය ලියන්න:** *"We will prove the contrapositive: If $n$ is not even (i.e., odd), then $n^2$ is not even (i.e., odd)."*
2. *"Assume $n$ is an odd integer. Then $n = 2k + 1$ for some integer $k$."*
3. *"Squaring both sides: $n^2 = (2k + 1)^2 = 4k^2 + 4k + 1 = 2(2k^2 + 2k) + 1$."*
4. *"Let $m = 2k^2 + 2k$. Then $n^2 = 2m + 1$, which is the definition of an odd number."*
5. *"Since the contrapositive is true, the original statement is also true."*

---

## 4. Proof by Contradiction (පරස්පරතාව මඟින් ඔප්පු කිරීම)

මේක ගණිතයේ තියෙන ලස්සනම Proof එකක්. මෙහිදී කරන්නේ **"ඔප්පු කරන්න ඕනෙ දේට සම්පූර්ණයෙන්ම විරුද්ධ දේ මුලින්ම ඇත්ත කියලා හිතනවා"**. ඊටපස්සේ ගාණ හදාගෙන යද්දී කොතනහරි ලොකු ගණිතමය වරදක් (Contradiction එකක්) වෙනවා. එතකොට අපිට තේරෙනවා "ආහ්, අපි මුලින් හිතපු විදිහ වැරදියි, ඒ කියන්නේ ගාණේ දීලා තියෙන දේ තමයි ඇත්ත" කියලා.

> [!TIP]
> විභාගයේදී $\sqrt{2}$ හෝ $\sqrt{3}$ පරිමේය නොවේ (irrational) යැයි ඔප්පු කරන්න කියන ගාණ බොහෝ දුරට පැමිණිය හැක!

**Question: "Prove that $\sqrt{3}$ is irrational."**
**How to Write the Answer:**
1. *"Assume for the sake of contradiction that $\sqrt{3}$ is **rational**."* (අපරිමේය නෙවෙයි, පරිමේයයි කියලා හිතමු).
2. *"Then $\sqrt{3}$ can be written as a fraction $\frac{a}{b}$, where $a$ and $b$ are integers with **no common factors**."* (ඒ කියන්නේ මේ භාගය තවත් සුළු කරන්න බෑ කියලා උපකල්පනය කරනවා).
3. *"$\sqrt{3} = \frac{a}{b} \implies 3 = \frac{a^2}{b^2} \implies a^2 = 3b^2$."*
4. *"Since $a^2$ is a multiple of 3, $a$ must also be a multiple of 3. Let $a = 3k$."*
5. *"Substitute this back: $(3k)^2 = 3b^2 \implies 9k^2 = 3b^2 \implies b^2 = 3k^2$."*
6. *"This means $b^2$ is a multiple of 3, so $b$ is also a multiple of 3."*
7. *"Now both $a$ and $b$ are multiples of 3. But we initially assumed they have **no common factors**! This is a contradiction."* (අපේ උපකල්පනය වැරදිලා!).
8. *"Therefore, our assumption was false. $\sqrt{3}$ must be irrational."*

---

## 5. Mathematical Induction (ගණිත අභ්‍යුහනය)

ස්වභාවික සංඛ්‍යා ($n = 1, 2, 3 \dots$) වල රටාවක් (Pattern) හැමදාටම සත්‍ය වෙනවා කියලා ඔප්පු කරන්නේ මේකෙන්. හරියට ඩොමිනෝ (Domino) ගල් පේළියක් පෙරළෙනවා වගේ. පළවෙනි එක පෙරළුණාම (Base case), ඊළඟ එකත් පෙරළෙනවා (Inductive step) කියලා පෙන්නුවාම ඇති. මුළු පේළියම පෙරළෙනවා.

**පියවර 2 කින් ගාණ හදමු:**
1. **Base Case:** $n=1$ සඳහා ප්‍රකාශය සත්‍ය බව පෙන්වන්න. (වම් පැත්ත = දකුණු පැත්ත).
2. **Inductive Step:** $n=k$ සඳහා සත්‍ය යැයි **උපකල්පනය කර** (Assume true for $n=k$), එය භාවිතා කරමින් $n=k+1$ සඳහාද සත්‍ය බව ඔප්පු කරන්න.

*(විභාගයේදී Induction Proof එකක් ලියනකොට මේ පියවර දෙක පැහැදිලිව මාතෘකා (Headings) දාලා ලියන්න. එවිට ලකුණු ලබාගැනීම ඉතා පහසුයි!)*
