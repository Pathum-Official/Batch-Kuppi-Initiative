---
course: MAT 1013
title: 06. Natural Numbers, Divisibility and Primes
---

# 06. Natural Numbers, Divisibility and Primes
### ස්වභාවික සංඛ්‍යා, බෙදෙන සුළු බව සහ ප්‍රථමක සංඛ්‍යා (Lesson 6)

> [!NOTE] 
> **මොකක්ද මේ පාඩම? ඇයි අපි මේක ඉගෙන ගන්නේ?**
> පරිගණක වල දත්ත ගබඩා කරන්න, රහස් පද (Passwords) හදන්න, වගේම Encryption (දත්ත හැංගීම) කරන්න පාවිච්චි කරන්නේ මේ Number Theory (සංඛ්‍යා න්‍යාය) කියන කොටසයි. විශේෂයෙන්ම RSA කියන Cryptography ක්‍රමයට පදනම වෙන්නේ මේ පාඩමේ තියෙන "ප්‍රථමක සංඛ්‍යා (Prime numbers)" සහ "බෙදෙන සුළු බව (Divisibility)" යි. ඒ නිසා මේක IT කරන අයට ගොඩක් වැදගත් පාඩමක්!

---

## 1. The Well-Ordering Principle (සුක්‍රමණ මූලධර්මය)

ස්වභාවික සංඛ්‍යා කුලකය $\mathbb{N} = \{1, 2, 3, \dots\}$ ලෙස ලියයි. (මෙම පාඨමාලාවේදී 0 අයත් නොවේ).

> [!IMPORTANT]
> **Well-Ordering Principle (විභාගයට ලියන ඉංග්‍රීසි නිර්වචනය):**
> Every non-empty subset of $\mathbb{N}$ has a least element.
> *(ස්වභාවික සංඛ්‍යා වලින් හදන ඕනෑම හිස් නොවන කුලකයක, අනිවාර්යයෙන්ම **අවම (කුඩාම) අගයක්** තිබිය යුතුමයි).*

**සරල උදාහරණයක්:**
$A = \{n \in \mathbb{N} : n > 10\}$ කියලා කුලකයක් ගමු. මේකෙ තියෙන්නේ 10ට වඩා ලොකු ස්වභාවික සංඛ්‍යා ($11, 12, 13 \dots$). මේකෙ තියෙන කුඩාම අගය (least element) මොකක්ද? 11 යි! අන්න ඒක තමයි මේ මූලධර්මයෙන් කියන්නේ.

*(සටහන: මේක $\mathbb{R}$ වගේ තාත්වික සංඛ්‍යා වලට හරියන්නේ නෑ. මොකද 10ට වඩා ලොකු තාත්වික සංඛ්‍යා ගත්තොත් $10.1, 10.01, 10.001 \dots$ වගේ කොච්චර හරි කුඩා කරන්න පුළුවන්නේ).*

---

## 2. Divisibility (බෙදෙන සුළු බව)

> [!IMPORTANT]
> **Definition:** Let $a, b \in \mathbb{Z}$ with $a \neq 0$. We say that **$a$ divides $b$**, written as **$a \mid b$**, if there exists an integer $k$ such that $b = ak$.
> *(යම් නිඛිලයක් තවත් නිඛිලයකින් ඉතිරි නැතිව බෙදෙනවා නම් අපි එය $a \mid b$ ලෙස ලියමු).*

**උදාහරණ:**
* $3 \mid 12$ (ඇයි? මොකද 12 හදන්න 3න් ගුණ කරන්න පුළුවන් නිඛිලයක් තියෙනවා: $12 = 3 \times 4$).
* $5 \nmid 17$ (5න් 17 බෙදෙන්නේ නැති නිසා මේ $\nmid$ ලකුණ යොදයි).

---

## 3. The Division Algorithm (බෙදීමේ ඇල්ගොරිතමය)

මේ නම ඇහුණාම ලොකු අමාරු දෙයක් වගේ පෙනුණට මේක අපි 3 වසරෙදි ඉගෙන ගත්තු සාමාන්‍ය බෙදීමම තමයි!

> [!TIP]
> **Theorem:** Let $a \in \mathbb{Z}$ and $b \in \mathbb{N}$. Then there exist **unique** integers $q$ (quotient - ලබ්ධිය) and $r$ (remainder - ඉතිරිය) such that:
> **$$a = bq + r, \quad 0 \le r < b$$**

**සරලව තේරුම් ගනිමු:**
37, 5 න් බෙදමු. 
$37 = 5 \times 7 + 2$
මෙහි ලබ්ධිය ($q$) = 7. ඉතිරිය ($r$) = 2.
අනිවාර්යයෙන්ම ඉතිරිය ($r$) කියන අගය, අපි බෙදන අගයට ($b$) වඩා කුඩා වෙන්න ඕනෙ කියන එක තමයි $0 \le r < b$ කියන එකෙන් කියවෙන්නේ.

---

## 4. Greatest Common Divisor (මහා පොදු සාධකය - GCD)

Positive integer $d$ එකකට **Greatest Common Divisor - $\gcd(a,b)$** යැයි කියන්නේ:
1. $d$ මඟින් $a$ සහ $b$ දෙකම බෙදෙනවා නම් ($d \mid a$ and $d \mid b$).
2. වෙනත් ඕනෑම පොදු සාධකයක් ($c$), මෙම $d$ ට වඩා කුඩා හෝ සමාන නම් ($c \le d$).

### Exam Question Walkthrough (The Euclidean Algorithm - යුක්ලිඩියානු ඇල්ගොරිතමය)

විභාගයේදී ලොකු ඉලක්කම් දෙකක් දීලා මේකේ $\gcd$ හොයන්න කියන එක අනිවාර්යයෙන්ම එන ප්‍රශ්නයක්!
මේකෙදි කරන්නේ ලොකු ගාණ පොඩි ගාණෙන් බෙදලා, ඊටපස්සේ පොඩි ගාණ ඉතිරියෙන් බෙදලා... ඔහොම බිංදුව එනකම් බෙදාගෙන යන එකයි.

**Question: "Use the Euclidean algorithm to find $\gcd(252, 198)$."**

**How to Write the Answer (විභාගයට ලියන පියවර):**
1. **Step 1:** $252$ න් $198$ ඒවා කීයක් තියෙනවද බලන්න.
   $252 = 198(1) + 54$
2. **Step 2:** දැන් අර කලින් බෙදපු ගාණ ($198$) අරන් ඒක අලුත් ඉතිරියෙන් ($54$) බෙදන්න.
   $198 = 54(3) + 36$
3. **Step 3:** ආයෙත් ඒකම කරන්න ($54$ අරන් $36$ න් බෙදන්න).
   $54 = 36(1) + 18$
4. **Step 4:** ආයෙත් කරන්න ($36$ අරන් $18$ න් බෙදන්න).
   $36 = 18(2) + 0$
5. **Step 5: අවසාන නිගමනය.** ඉතිරිය බිංදුව ආවාම ගාණ හදලා ඉවරයි! බිංදුව එන්න කලින් ආපු අන්තිම ඉතිරිය තමයි උත්තරේ.
   *"The last non-zero remainder is 18. Therefore, $\gcd(252, 198) = 18$."*

---

## 5. Prime Numbers (ප්‍රථමක සංඛ්‍යා)

> [!IMPORTANT]
> **Definition:** An integer $p > 1$ is called **prime** if its only positive divisors are 1 and $p$.
> *(1 ට වඩා විශාල, 1න් සහ එම සංඛ්‍යාවෙන් පමණක් බෙදෙන සංඛ්‍යා ප්‍රථමක සංඛ්‍යා වේ).*
> **[WARNING] 1 යනු ප්‍රථමක සංඛ්‍යාවක් නොවේ! (1 is NOT a prime).**

### Fundamental Theorem of Arithmetic (අංක ගණිතයේ මූලික ප්‍රමේයය)
Every integer greater than 1 can be written as a product of prime numbers, and this factorization is **unique**.
*(1ට වඩා විශාල ඕනෑම සංඛ්‍යාවක්, ප්‍රථමක සංඛ්‍යා වල ගුණිතයක් විදිහට ලියන්න පුළුවන්. උදා: $84 = 2^2 \times 3 \times 7$. මේ ලියන විදිහ ඒ සංඛ්‍යාවට අනන්‍යයි).*
