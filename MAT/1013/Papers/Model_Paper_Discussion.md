# Practice Final Examination - Ultimate Discussion Guide
### ආදර්ශ අවසාන විභාගය - සම්පූර්ණ විවරණය සහ අනුමාන

> [!NOTE]
> **භාවිතා කරන ආකාරය (How to use this guide):**
> මින් පෙර මඟහැරී තිබූ කොටස් සියල්ල නැවත පරීක්ෂා කර, මෙම විවරණ පත්‍රිකාවේ විභාග ප්‍රශ්න පත්‍රයේ ඇති **සෑම ප්‍රශ්නයකටම සහ අනු කොටසකටම (a, b, c, d, e)** පියවරෙන් පියවර විසඳුම් අලුතින්ම ලබා දී ඇත. 
> - **[Theory Link]** මඟින් අදාළ න්‍යාය කොටස අපගේ සටහන් පොතේ ඇති තැනට සම්බන්ධ කර ඇත. 
> - **[Exam Twist / Prediction]** මඟින් මෙම ප්‍රශ්නයම විභාගයේදී වෙනස් වී පැමිණිය හැකි ආකාරය සහ මගේ අනුමාන (Predictions) සාකච්ඡා කර ඇත.

---

## Question 1: Multiple-Choice Questions (Part 1 - Logic & Number Theory)

### Q1. The negation of $(p \wedge q) \to r$ is logically equivalent to:
**[Theory Link: Lesson 02 - Truth Tables & Equivalences](02_Truth_Tables_and_Equivalence.md)**

**Step-by-step Solution:**
1. මුලින්ම $\to$ ලකුණ (Implication) ඉවත් කළ යුතුය. අපි දන්නවා $A \to B \equiv \neg A \vee B$ බව.
   මෙම ප්‍රශ්නයේදී $A = (p \wedge q)$ සහ $B = r$ වේ.
   එමනිසා: $(p \wedge q) \to r \equiv \neg(p \wedge q) \vee r$
2. දැන් මේ මුළු එකේම නිෂේධය (Negation) සෙවිය යුතුය:
   $\neg [ \neg(p \wedge q) \vee r ]$
3. De Morgan's Law (ඩි මෝගන් නියමය) යොදන්න (OR එක AND වේ):
   $\neg(\neg(p \wedge q)) \wedge \neg r$
4. ද්විත්ව නිෂේධය ඉවත් වේ:
   $(p \wedge q) \wedge \neg r$

**Answer:** **b) $p \wedge q \wedge \neg r$**

> [!TIP]
> **[Exam Twist]:** ප්‍රශ්නය "What is the contrapositive?" කියලා ඇහුවා නම්, පිළිතුර $\neg r \to \neg(p \wedge q)$ එනම් $\neg r \to (\neg p \vee \neg q)$ වේ.

---

### Q2. Which of the following are tautologies?
**[Theory Link: Lesson 02 - Truth Tables](02_Truth_Tables_and_Equivalence.md)**

**Step-by-step Solution:**
* **I. $\neg(p \wedge \neg p)$**: $p \wedge \neg p$ කියන්නේ කවදාවත් වෙන්න බැරි දෙයක් (Contradiction). එතකොට ඒකෙ Negation එක $\neg(False)$ කියන්නේ **True** (Tautology).
* **II. $p \leftrightarrow \neg p$**: එක දෙයක්, ඒකේම අනිත් පැත්තට සමාන වෙන්න බෑ. (Contradiction).
* **III. $\neg(p \vee \neg p)$**: $p \vee \neg p$ කියන්නේ සර්වසත්‍යයක් (True). ඒකෙ Negation එක $\neg(True)$ කියන්නේ **False**.
* **IV. $p \to p$**: මේක $\neg p \vee p$ හා සමානයි. එය **True** (Tautology) වේ.

**Answer:** **c) I and IV only**

---

### Q3. The negation of $\exists x \in \mathbb{R} \, \forall y \in \mathbb{R}, x \le y$ is:
**[Theory Link: Lesson 03 - Predicates and Quantifiers](03_Predicates_and_Quantifiers.md)**

**Step-by-step Solution:**
Quantifiers වල Negation හොයද්දී නීති 3ක් තියෙනවා:
1. $\exists$ එක $\forall$ වෙනවා.
2. $\forall$ එක $\exists$ වෙනවා.
3. අග තියෙන සමීකරණයේ ලකුණ අනිත් පැත්ත හැරෙනවා ($\le$ යන්න $>$ බවට පත්වේ).
මේ නීති තුන දැම්මම: $\forall x \in \mathbb{R} \, \exists y \in \mathbb{R}, x > y$.

**Answer:** **b) $\forall x \in \mathbb{R} \, \exists y \in \mathbb{R}, x > y$**

---

### Q4. The greatest common divisor of 252 and 198 is:
**[Theory Link: Lesson 06 - Divisibility and Primes](06_Natural_Numbers_Divisibility_Primes.md)**

**Step-by-step Solution:**
Euclidean Algorithm එක පාවිච්චි කරමු:
* $252 = 198 \times 1 + 54$
* $198 = 54 \times 3 + 36$
* $54 = 36 \times 1 + 18$
* $36 = 18 \times 2 + 0$
අවසානයට ඉතිරි වූ බිංදුව නොවන අගය 18 වේ.

**Answer:** **c) 18**

---

### Q5. Which of the following arguments are valid?
**[Theory Link: Lesson 04 - Arguments and Valid Reasoning](04_Arguments_and_Valid_Reasoning.md)**

**Step-by-step Solution:**
* **I. $p \to q, \neg q \therefore \neg p$**: මෙය Modus Tollens වේ. **Valid**.
* **II. $p \to q, q \therefore p$**: මෙය Affirming the Consequent දෝෂයයි. **Invalid**.
* **III. $p \vee q, \neg p \therefore q$**: මෙය Disjunctive Syllogism වේ. **Valid**.
* **IV. $p \to q, \neg p \therefore \neg q$**: මෙය Denying the Antecedent දෝෂයයි. **Invalid**.

**Answer:** **c) I and III only**

---

### Q6. Which of the following is congruent to 37 modulo 23?
**[Theory Link: Lesson 07 - Modular Arithmetic](07_Modular_Arithmetic_RSA.md)**

**Step-by-step Solution:**
$37 \pmod{23} \equiv 14$. එනම් පිළිතුර 14 ට සමතුල්‍ය විය යුතුය.
* **Option d) $2^8 + 5^{31}$** පරීක්ෂා කරමු:
  * $2^8 = 256$. $256 = 23 \times 11 + 3$. එබැවින් $2^8 \equiv 3 \pmod{23}$.
  * Fermat's Little Theorem අනුව, $5^{22} \equiv 1 \pmod{23}$.
  * $5^{31} = 5^{22} \times 5^9 \equiv 1 \times 5^9 \pmod{23}$.
  * $5^2 = 25 \equiv 2 \implies 5^8 = (5^2)^4 \equiv 2^4 = 16$. 
  * $5^9 = 16 \times 5 = 80$. $80 = 23 \times 3 + 11 \implies 5^9 \equiv 11$.
  * එකතුව $= 3 + 11 = 14$.
මෙය අපගේ 14 ට සමාන වේ!

**Answer:** **d) $2^8 + 5^{31}$**

---

### Q7. The least non-negative solution of $9x \equiv 12 \pmod{26}$ is:
**[Theory Link: Lesson 07 - Modular Arithmetic](07_Modular_Arithmetic_RSA.md)**

**Step-by-step Solution:**
9 හි Inverse එක සෙවිය යුතුය. 9න් ගුණ කළාම $\pmod{26}$ වලදී 1 එන අගය කුමක්ද?
$9 \times 3 = 27 \equiv 1 \pmod{26}$. එනම් Inverse එක 3 වේ.
සමීකරණය දෙපසම 3න් ගුණ කරන්න:
$3 \times 9x \equiv 3 \times 12 \pmod{26} \implies x \equiv 36 \pmod{26}$.
$36 \pmod{26} \equiv 10$. එබැවින් $x = 10$.

**Answer:** **c) 10**

---

### Q8. The solution set of $|3x - 2| \ge 7$ is:
**[Theory Link: Lesson 08 - Rational & Real Numbers](08_Rational_Real_Numbers.md)**

**Step-by-step Solution:**
මාපාංකය (Absolute value) ඉවත් කරන විට සමීකරණ 2ක් සෑදේ:
1) $3x - 2 \ge 7 \implies 3x \ge 9 \implies x \ge 3$
2) $3x - 2 \le -7 \implies 3x \le -5 \implies x \le -\frac{5}{3}$
එමනිසා විසඳුම් කුලකය: $(-\infty, -\frac{5}{3}] \cup [3, \infty)$.

**Answer:** **d) $(-\infty, -\frac{5}{3}] \cup [3, \infty)$**

---

### Q9. Which of the following statements is/are true?
**[Theory Link: Lesson 08 - Real Numbers](08_Rational_Real_Numbers.md)**

**Step-by-step Solution:**
* I. Every irrational number is a real number. **(True)**.
* II. The sum of two irrational numbers is always irrational. **(False. e.g: $\sqrt{2} + (-\sqrt{2}) = 0$. බිංදුව පරිමේයයි)**.
* III. The product of a nonzero rational and an irrational is irrational. **(True)**.
* IV. Every non-terminating decimal is irrational. **(False. $0.3333\dots = 1/3$ පරිමේයයි)**.

**Answer:** **b) I and III only**

---

### Q10. The value of $\left(\frac{1 + \sqrt{3}i}{1 - i}\right)^{15}$ is:
**[Theory Link: Lesson 09 - Complex Numbers](09_Complex_Numbers.md)**

**Step-by-step Solution:**
Polar form එකට හරවන්න:
* ලවය: $1 + \sqrt{3}i \implies r=2, \theta=\pi/3 \implies 2e^{i\pi/3}$
* හරය: $1 - i \implies r=\sqrt{2}, \theta=-\pi/4 \implies \sqrt{2}e^{-i\pi/4}$
* බෙදූ විට: $\frac{2}{\sqrt{2}} e^{i(\frac{\pi}{3} - (-\frac{\pi}{4}))} = \sqrt{2} e^{i\frac{7\pi}{12}}$
15 වෙනි බලය සොයමු:
* $r^{15} = (\sqrt{2})^{15} = 2^7\sqrt{2} = 128\sqrt{2}$
* කෝණය: $15 \times \frac{7\pi}{12} = \frac{105\pi}{12} = \frac{35\pi}{4}$. මෙය සම්පූර්ණ රවුම් (multiples of $2\pi$) ඉවත් කළ පසු $\frac{3\pi}{4}$ ට සමතුල්‍ය වේ.
* $\cos(\frac{3\pi}{4}) = -\frac{1}{\sqrt{2}}$ සහ $\sin(\frac{3\pi}{4}) = \frac{1}{\sqrt{2}}$.
අවසාන පිළිතුර: $128\sqrt{2} \left(-\frac{1}{\sqrt{2}} + i\frac{1}{\sqrt{2}}\right) = -128 + 128i$.

**Answer:** **b) $-128 + 128i$**

---

## Question 2: Multiple-Choice Questions (Part 2 - Sets & Relations)

### Q1. If $|A| = 3$ and $|B| = 5$, then the number of elements in $\mathcal{P}(A \times B)$ is:
**[Theory Link: Lesson 10 - Sets and Set Algebra](10_Sets_and_Set_Algebra.md)**

**Step-by-step Solution:**
Cartesian Product එකේ අවයව ගණන: $|A \times B| = 3 \times 5 = 15$.
Power Set $\mathcal{P}(X)$ එකක අවයව ගණන $2^{|X|}$ වේ. එනම් $2^{15}$.

**Answer:** **b) $2^{15}$**

---

### Q2. Which identity is valid for all subsets $A$ and $B$?
**[Theory Link: Lesson 10 - Sets and Set Algebra](10_Sets_and_Set_Algebra.md)**

**Step-by-step Solution:**
De Morgan's Laws වලට අනුව, Complement එකක් (ඩෑෂ් එකක්) වරහන ඇතුළට දානකොට $\cup$ එක $\cap$ වෙනවා.
එනම්, $(A \cup B)^c = A^c \cap B^c$.

**Answer:** **c) $(A \cup B)^c = A^c \cap B^c$**

---

### Q3 & Q4. Relations Matrix and Inverse
**[Theory Link: Lesson 11 - Relations](11_Relations_and_Equivalence.md)**

**Step-by-step Solution:**
* **Q3:** $R = \{(1, 2), (2, 1), (2, 3), (3, 3)\}$. 
  පේළිය (row) පළමු අගය ලෙසත්, තීරුව (column) දෙවන අගය ලෙසත් ගන්න. 
  Row 1: (1,1)=0, (1,2)=1, (1,3)=0 $\to$ `0 1 0`
  Row 2: (2,1)=1, (2,2)=0, (2,3)=1 $\to$ `1 0 1`
  Row 3: (3,1)=0, (3,2)=0, (3,3)=1 $\to$ `0 0 1`
  **Answer:** **a**
* **Q4:** Inverse relation $R^{-1}$ හි අගයන් දෙක මාරු කරයි. $\{(2, 1), (1, 2), (3, 2), (3, 3)\}$.
  **Answer:** **b**

---

### Q5. Let $D$ be the divisibility relation on $\{1, 2, 4, 8\}$. Which is correct?
**[Theory Link: Lesson 11 - Partial Orders](11_Relations_and_Equivalence.md)**

**Step-by-step Solution:**
Divisibility (බෙදෙන සුළු බව) යනු Partial Order එකකි. එය Reflexive, Antisymmetric, සහ Transitive වේ. නමුත් Symmetric නොවේ (2න් 4 බෙදුණාට 4න් 2 බෙදෙන්නේ නැත).

**Answer:** **b) Reflexive, antisymmetric, and transitive, but not symmetric.**

---

### Q6. Composition $T \circ S$
**[Theory Link: Lesson 11 - Relations](11_Relations_and_Equivalence.md)**

**Step-by-step Solution:**
$S = \{(1, a), (2, b), (3, a)\}$, $T = \{(a, x), (a, y), (b, y)\}$.
$T \circ S$ සෙවීමට $S$ හි දෙවන අගය සහ $T$ හි පළමු අගය සමාන වන යුගල සම්බන්ධ කරන්න:
* $1 \xrightarrow{S} a \xrightarrow{T} x, y \implies (1, x), (1, y)$
* $2 \xrightarrow{S} b \xrightarrow{T} y \implies (2, y)$
* $3 \xrightarrow{S} a \xrightarrow{T} x, y \implies (3, x), (3, y)$

**Answer:** **b) $\{(1, x), (1, y), (2, y), (3, x), (3, y)\}$**

---

### Q7, Q8, Q9. Properties of $R, S, T$
**[Theory Link: Lesson 11 - Relations](11_Relations_and_Equivalence.md)**

* $R = \{(1, 1), (2, 2), (3, 3)\}$
* $S = \{(1, 1), (1, 2), (2, 1), (2, 2), (2, 3), (3, 2), (3, 3)\}$
* $T = \{(1, 1), (1, 2), (1, 3), (2, 2), (2, 3), (3, 3)\}$

**Step-by-step Solution:**
* **Q7 (Reflexive):** 1, 2, 3 යන සියල්ලටම $(x,x)$ පවතීද? කුලක 3 හිම ඇත. **Answer: e) All three**
* **Q8 (Symmetric):** $S$ හි (1,2) හා (2,1) ඇත. (2,3) හා (3,2) ඇත. $S$ සමමිතික වේ. $T$ හි (1,2) ඇතත් (2,1) නැත. $R$ සමමිතික වේ. **Answer: a) R and S only**
* **Q9 (Transitive):** $S$ හි (1,2) හා (2,3) ඇත, නමුත් (1,3) නැත. එමනිසා $S$ සංක්‍රාමී නොවේ. $R, T$ සංක්‍රාමී වේ. **Answer: b) R and T only**

---

### Q10. Composition $T \circ S$
**Step-by-step Solution:**
* $1 \xrightarrow{S} 1, 2 \xrightarrow{T} 1, 2, 3, 2, 3 \implies 1 \to 1, 2, 3$.
* $2 \xrightarrow{S} 1, 2, 3 \xrightarrow{T} 1, 2, 3, 2, 3, 3 \implies 2 \to 1, 2, 3$.
* $3 \xrightarrow{S} 2, 3 \xrightarrow{T} 2, 3, 3 \implies 3 \to 2, 3$.
මෙම සියලුම සම්බන්ධතා ඇත්තේ (a) පිළිතුරේය.

**Answer:** **a**

---

## Question 3: Structured Questions

### Part 1: Euclidean Algorithm and Inverses (a, b, c, d)
**[Theory Link: Lesson 06 & 07 - Number Theory](07_Modular_Arithmetic_RSA.md)**

**(a) Euclidean Algorithm:**
* $157 = 36(4) + \mathbf{13}$
* $36 = \mathbf{13}(2) + 10$
* $13 = 10(1) + \mathbf{3}$
* $10 = 3(\mathbf{3}) + 1$
* $3 = 1(\mathbf{3}) + 0$

**(b) GCD:** $\gcd(157, 36) = \mathbf{1}$ (අවසන් බිංදුව නොවන ඉතිරිය).

**(c) Back Substitution:**
* $1 = 10 - 3(\mathbf{3})$
* $= 10 - 3(13 - \mathbf{10})$
* $= \mathbf{4}(10) - 3(13)$  *(මොකද 10 ඒවා 1කුයි, තව 3කුයි එකතු වෙලා 4ක් වෙනවා).*
* $= 4(36 - 2(13)) - 3(13)$
* $= 4(36) - \mathbf{11}(13)$ *(මොකද 13 ඒවා 8ක් අඩු වෙලා තව 3ක් අඩු වෙනවා = 11ක් අඩු වෙනවා).*
* $= 4(36) - 11(157 - 4(36))$
* $= \mathbf{48}(36) - 11(157)$ *(මොකද -11 * -4 = +44. 44යි 4යි 48යි).*

**(d) Multiplicative Inverse:**
* $1 = \mathbf{48}(36) - \mathbf{11}(157)$.
* Therefore, $\mathbf{48}(36) \equiv 1 \pmod{157}$.
* Hence, $36^{-1} \equiv \mathbf{48} \pmod{157}$.

**(e) Solve $36u \equiv 19 \pmod{157}$:**
* $u \equiv \mathbf{48} \cdot 19 \equiv \mathbf{912} \pmod{157}$.
* Thus, $u = \mathbf{127} + 157k, \quad k \in \mathbb{Z}$, *(මොකද $912 = 157 \times 5 + 127$ නිසා).*
* and the least non-negative solution is $u = \mathbf{127}$.

---

### Part 2: Complex Numbers (a, b, c, d)
**[Theory Link: Lesson 09 - Complex Numbers](09_Complex_Numbers.md)**

**(a) Polar Form:**
* $z_0 = -4 + 4\sqrt{3}i$
* $|z_0| = \mathbf{8}$, $\text{Arg}(z_0) = \mathbf{\frac{2\pi}{3}}$,
* and hence $z_0 = \mathbf{8}(\cos \mathbf{\frac{2\pi}{3}} + i \sin \mathbf{\frac{2\pi}{3}})$.

**(b) De Moivre's Theorem ($z_0^3$):**
* $z_0^3 = (\mathbf{8})^{\mathbf{3}} (\cos (\mathbf{3} \cdot \mathbf{\frac{2\pi}{3}}) + i \sin (\mathbf{3} \cdot \mathbf{\frac{2\pi}{3}}))$
* $= \mathbf{512}(\cos \mathbf{2\pi} + i \sin \mathbf{2\pi})$
* $= \mathbf{512}$.

**(c) Roots of Unity ($z^3 = z_0$):**
* Since $z_0 = \mathbf{8}(\cos \mathbf{\frac{2\pi}{3}} + i \sin \mathbf{\frac{2\pi}{3}})$,
* we obtain $r^3 = \mathbf{8}$, $3\theta = \mathbf{\frac{2\pi}{3}} + 2k\pi$.
* Hence, $r = \mathbf{2}$, $\theta = \mathbf{\frac{2\pi}{9}} + \mathbf{\frac{2k\pi}{3}}$, $k = \mathbf{0}, \mathbf{1}, \mathbf{2}$.
* **Table of solutions:**

| k | $\theta$ | z |
|---|---|---|
| **0** | **$\frac{2\pi}{9}$** | **$2(\cos \frac{2\pi}{9} + i\sin \frac{2\pi}{9})$** |
| **1** | **$\frac{8\pi}{9}$** | **$2(\cos \frac{8\pi}{9} + i\sin \frac{8\pi}{9})$** |
| **2** | **$\frac{14\pi}{9}$** | **$2(\cos \frac{14\pi}{9} + i\sin \frac{14\pi}{9})$** |

**(d) Plot the solutions in the complex plane:**
* රූප සටහනේ මූල ලක්ෂ්‍යයේ සිට අරය (radius) $r=2$ වන රවුමක් අඳින්න. 
* පළමු ලක්ෂ්‍යය (k=0) අංශක 40 ක කෝණයක අඳින්න ($2\pi/9 = 40^\circ$).
* අනෙකුත් ලක්ෂ්‍ය දෙක, අංශක 120 ක ($2\pi/3$) දුරින් අඳින්න. එනම් $160^\circ$ සහ $280^\circ$ වලය. ඒවා එකතු කළ විට සමපාද ත්‍රිකෝණයක් (Equilateral triangle) සෑදේ.

---

### Part 3: Congruence Relation Matrix (a, b)
**[Theory Link: Lesson 11 - Relations](11_Relations_and_Equivalence.md)**

$A = \{1, 2, 3, 4, 5, 6\}$. $aRb \iff a \equiv b \pmod 4$.

**(a) Relation Matrix:**
$$M_R = \begin{pmatrix} 
\mathbf{1} & \mathbf{0} & \mathbf{0} & \mathbf{0} & \mathbf{1} & \mathbf{0} \\
\mathbf{0} & \mathbf{1} & \mathbf{0} & \mathbf{0} & \mathbf{0} & \mathbf{1} \\
\mathbf{0} & \mathbf{0} & \mathbf{1} & \mathbf{0} & \mathbf{0} & \mathbf{0} \\
\mathbf{0} & \mathbf{0} & \mathbf{0} & \mathbf{1} & \mathbf{0} & \mathbf{0} \\
\mathbf{1} & \mathbf{0} & \mathbf{0} & \mathbf{0} & \mathbf{1} & \mathbf{0} \\
\mathbf{0} & \mathbf{1} & \mathbf{0} & \mathbf{0} & \mathbf{0} & \mathbf{1} 
\end{pmatrix}$$

**(b) Properties:**
* $R$ is reflexive **True**
* $R$ is symmetric **True**
* $R$ is antisymmetric **False** *(1R5 and 5R1 ඇත, නමුත් $1 \neq 5$)*
* $R$ is transitive **True**

---

### Part 4: Functions (a, b)
**[Theory Link: Lesson 12 - Functions](12_Functions.md)**

Define $f: \mathbb{Q} \setminus \{0\} \to \mathbb{Q}$ by $f(a) = \frac{18}{a}$.

**(a) Classify the function:**
* $f$ is injective **True** *(මොකද $18/a = 18/b$ නම් අනිවාර්යයෙන්ම $a=b$ වේ)*.
* $f$ is surjective **False** *(Codomain එක $\mathbb{Q}$ බැවින් එහි බිංදුව ඇත. නමුත් $18/a = 0$ වීමට $a$ ට කිසිදු අගයක් නැත. එබැවින් 0 ට ඊතලයක් නැත)*.
* $f$ is bijective **False** *(Surjective නොවන නිසා Bijective විය නොහැක)*.

**(b) Compute $(f \circ f)(a)$:**
* $(f \circ f)(a) = \mathbf{a}$. *(මොකද $f(18/a) = \frac{18}{(18/a)} = a$ වේ).*

---

## Question 4: Essay Questions (a, b, c, d, e)

### (a) Complex Roots of Unity
**Solve the equation $z^5 = i$ and plot the answer on the complex plane.**
* $i$ යනු polar form වලින් ලියූ විට $\cos(\frac{\pi}{2}) + i\sin(\frac{\pi}{2})$ වේ. 
* $z^5 = 1 \cdot (\cos(\frac{\pi}{2}) + i\sin(\frac{\pi}{2}))$.
* De Moivre's Theorem අනුව, මූලයන් 5 සොයාගත හැක. $r^5 = 1 \implies r=1$.
* $5\theta = \frac{\pi}{2} + 2k\pi \implies \theta = \frac{\pi}{10} + \frac{2k\pi}{5}$.
* $k = 0, 1, 2, 3, 4$ ආදේශ කළ විට:
  * $k=0 \to \theta = \frac{\pi}{10} (18^\circ)$
  * $k=1 \to \theta = \frac{\pi}{10} + \frac{4\pi}{10} = \frac{5\pi}{10} = \frac{\pi}{2} (90^\circ)$
  * $k=2 \to \theta = \frac{9\pi}{10} (162^\circ)$
  * $k=3 \to \theta = \frac{13\pi}{10} (234^\circ)$
  * $k=4 \to \theta = \frac{17\pi}{10} (306^\circ)$
* **Plotting:** අරය 1ක් වන රවුමක් මත (Unit circle), අංශක 18 කින් පටන් ගෙන සමාන දුරින් (අංශක 72න් 72ට) පිහිටන ලක්ෂ්‍ය 5ක් ලකුණු කරන්න (Regular pentagon).

---

### (b) Relations Analysis (1 to 7)
* $R: a \mid b$ (බෙදෙන සුළු බව) on $A=\{1,2,3,4,5,6\}$.
* $S: \text{Even} \to T, \text{Odd} \to F$.

**1. Draw the directed graph of $R$:**
* ලක්ෂ්‍ය 1 සිට 6 දක්වා අඳින්න. 
* සෑම ලක්ෂ්‍යයකටම තමා වෙතටම ඊතලයක් (loop) අඳින්න.
* 1 සිට 2,3,4,5,6 දක්වා ඊතල අඳින්න. 
* 2 සිට 4ට සහ 6ට ඊතල අඳින්න. 
* 3 සිට 6ට ඊතලයක් අඳින්න.

**2. Verify properties of $R$:**
* **Reflexive:** $\forall a \in A, a \mid a$. එනම් සෑම සංඛ්‍යාවක්ම එයින්ම බෙදේ.
* **Antisymmetric:** $a \mid b$ සහ $b \mid a$ නම් $a=b$ විය යුතුය (ධන නිඛිල නිසා). 
* **Transitive:** $a \mid b$ සහ $b \mid c$ නම්, ගණිතමය නීති අනුව $a \mid c$ වේ. 

**3. Matrices for $R$ and $S$:**
$$M_R = \begin{pmatrix} 1 & 1 & 1 & 1 & 1 & 1 \\ 0 & 1 & 0 & 1 & 0 & 1 \\ 0 & 0 & 1 & 0 & 0 & 1 \\ 0 & 0 & 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 & 0 & 1 \end{pmatrix}, \quad M_S = \begin{pmatrix} 0 & 1 \\ 1 & 0 \\ 0 & 1 \\ 1 & 0 \\ 0 & 1 \\ 1 & 0 \end{pmatrix}$$
*(S න්‍යාසයේ තීරු $T, F$ ලෙස ගෙන ඇත. 1 ඉරට්ටේ නොවන නිසා $1 \to F$. 2 ඉරට්ටේ නිසා $2 \to T$.)*

**4. What can you say about $R \circ R^{-1}$? Justify your answer.**
* $x (R \circ R^{-1}) y \implies x R^{-1} z$ and $z R y$ for some $z$.
* එනම් $z R x$ (z න් x බෙදේ) සහ $z R y$ (z න් y බෙදේ).
* අපගේ කුලකයේ ඇති $z=1$ යන ඉලක්කම ගත් විට, 1 මඟින් කුලකයේ ඇති ඕනෑම ඉලක්කම් යුගලයක් බෙදේ. එබැවින් සෑම $(x,y)$ යුගලයක්ම මෙම සම්බන්ධතාවයේ පවතී.
* මෙය $A \times A$ හෙවත් **Universal Relation** (සර්ව සම්බන්ධතාවය) වේ.

**5. Determine the matrix of $S \circ R$:**
* Matrix ගුණ කිරීමෙන් ($M_R \times M_S$) මෙය ලබාගත හැක. Boolean arithmetic (AND/OR) භාවිත කරන්න.
$$M_{S \circ R} = \begin{pmatrix} 1 & 1 \\ 1 & 0 \\ 1 & 1 \\ 1 & 0 \\ 0 & 1 \\ 1 & 0 \end{pmatrix}$$

**6. Write the domain, codomain and range of $S \circ R$:**
* **Domain:** $\{1, 2, 3, 4, 5, 6\}$ (සෑම ඉලක්කමකින්ම ඊතලයක් පිටවේ).
* **Codomain:** $\{T, F\}$
* **Range:** $\{T, F\}$ (T සහ F දෙකටම ඊතල පැමිණේ).

**7. Determine $(S \circ R)^{-1}(T)$:**
* මෙයින් අදහස් කරන්නේ T වෙත පැමිණෙන ඊතල පිටවූයේ කුමන අගයන්ගෙන්ද යන්නයි. න්‍යාසයේ පළමු තීරුවේ (T තීරුව) 1 අගය ඇති පේළි මොනවාද?
* එය 1, 2, 3, 4, 6 වේ. 
* පිළිතුර: $\{1, 2, 3, 4, 6\}$.

---

### (c) Direct Proof / Contrapositive Proof
**Using a suitable method, prove: For every integer $n$, if $3 \mid n^2$, then $3 \mid n$.**
* මේ සඳහා Contrapositive ක්‍රමය (ප්‍රතිපක්ෂය) භාවිතා කිරීම පහසුය. 
* **Proof Statement:** Assume $3 \nmid n$. Then we will prove $3 \nmid n^2$.
* යම් සංඛ්‍යාවක් 3න් බෙදෙන්නේ නැත්නම්, එහි ඉතිරිය (remainder) 1 හෝ 2 විය යුතුය. 
  එනම්, $n = 3k+1$ හෝ $n = 3k+2$.
* **Case 1 ($n=3k+1$):** 
  $n^2 = (3k+1)^2 = 9k^2+6k+1 = 3(3k^2+2k) + 1$. 
  මෙහි 1ක් ඉතිරි වන බැවින් 3න් නොබෙදේ ($3 \nmid n^2$).
* **Case 2 ($n=3k+2$):** 
  $n^2 = (3k+2)^2 = 9k^2+12k+4 = 3(3k^2+4k+1) + 1$. 
  මෙහිද 1ක් ඉතිරි වන බැවින් 3න් නොබෙදේ ($3 \nmid n^2$).
* අවස්ථා දෙකේදීම $3 \nmid n^2$ බව ඔප්පු වූ නිසා මුල් ප්‍රකාශය සත්‍ය වේ. (Q.E.D)

---

### (d) Mathematical Induction (ගණිත අභ්‍යුහනය)
**Prove using mathematical induction that $\sum_{k=1}^n k(k + 1) = \frac{n(n + 1)(n + 2)}{3}$**
* **Base case ($n=1$):** 
  LHS $= 1(1+1) = 2$.
  RHS $= \frac{1(1+1)(1+2)}{3} = \frac{1(2)(3)}{3} = 2$.
  LHS = RHS. එමනිසා $n=1$ සඳහා සත්‍ය වේ.
* **Inductive Hypothesis:** Assume true for some positive integer $m$. 
  එනම්, $\sum_{k=1}^m k(k + 1) = \frac{m(m + 1)(m + 2)}{3}$.
* **Inductive Step ($n=m+1$ සඳහා ඔප්පු කිරීම):**
  LHS $= \sum_{k=1}^{m+1} k(k + 1) = \sum_{k=1}^m k(k + 1) + (m+1)(m+2)$.
  අපගේ Assumption එක මෙයට ආදේශ කරමු:
  LHS $= \frac{m(m + 1)(m + 2)}{3} + (m+1)(m+2)$.
  දැන් $(m+1)(m+2)$ පොදු සාධකයක් ලෙස එළියට ගනිමු:
  LHS $= (m+1)(m+2) \left[ \frac{m}{3} + 1 \right]$
  LHS $= (m+1)(m+2) \left[ \frac{m+3}{3} \right] = \frac{(m+1)(m+2)(m+3)}{3}$.
* මෙය $n=m+1$ යෙදූ විට ලැබිය යුතු අගයම වේ. එමනිසා, ගණිත අභ්‍යුහන මූලධර්මය අනුව මෙය සෑම $n \in \mathbb{Z}^+$ සඳහාම සත්‍ය වේ.

---

### (e) Venn Diagrams and Set Identities
**Using the labelled Venn diagram below, verify $(A \cup B) \setminus C = (A \setminus C) \cup (B \setminus C)$.**

රූප සටහනේ ඇති Region (කලාප) අංක භාවිතා කරමු:
* $A = \{1, 4, 5, 7\}$
* $B = \{2, 4, 6, 7\}$
* $C = \{3, 5, 6, 7\}$

**Left Hand Side (LHS):** $(A \cup B) \setminus C$
* $(A \cup B)$ යනු A හෝ B හි ඇති සියල්ලයි = $\{1, 2, 4, 5, 6, 7\}$.
* එයින් C හි ඇති අගයන් ඉවත් කළ විට ($(A \cup B) \setminus C$): 5, 6, 7 ඉවත් වේ.
* LHS $= \{1, 2, 4\}$.

**Right Hand Side (RHS):** $(A \setminus C) \cup (B \setminus C)$
* $(A \setminus C)$ යනු A ගෙන් C ඉවත් කළ විටයි = $\{1, 4\}$.
* $(B \setminus C)$ යනු B ගෙන් C ඉවත් කළ විටයි = $\{2, 4\}$.
* මේ දෙකේ Union එක (එකතුව) $= \{1, 4\} \cup \{2, 4\} = \{1, 2, 4\}$.
* RHS $= \{1, 2, 4\}$.

LHS = RHS බව පැහැදිලිවම ඔප්පු වේ.

---

> [!TIP]
> **[Final Exam Predictions - මගේ අනුමාන]**
> 1. **Extended Euclidean Algorithm** අනිවාර්යයෙන්ම විභාගයට එනවා. Inverses සහ Modulo equations විසඳීම හොඳින් පුහුණු වන්න.
> 2. **Complex Numbers ($z^n = z_0$)** - Roots සෙවීමේදී $2k\pi$ එකතු කර බෙදන කොටස කිසිසේත්ම අමතක නොකළ යුතුය. Essay ප්‍රශ්නයේදී මෙන් plot කරන්නටද පැමිණේ.
> 3. **Induction Proofs** - $\Sigma$ (Summation) සංකේතය සහිත අභ්‍යුහන සාධනයක් නිසැකවම පැමිණේ. Base Case සහ Inductive Step අනිවාර්යයෙන් ලියා දක්වන්න!
> 4. **Composition of Relations ($S \circ R$)** - Matrices ගුණ කිරීමෙන් (Boolean arithmetic) පිළිතුරු සෙවීම පුහුණු වන්න.
