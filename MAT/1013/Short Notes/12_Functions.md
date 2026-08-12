---
course: MAT 1013
title: 12. Functions and Their Properties
---

# 12. Functions and Their Properties
### ශ්‍රිත සහ ඒවායේ ගුණාංග (Lesson 12)

> [!NOTE] 
> **මොකක්ද මේ පාඩම? ඇයි අපි මේක ඉගෙන ගන්නේ?**
> පරිගණක ක්‍රමලේඛනයේදී (Programming) අපි ලියන Functions (උදා: `def calculateSum(a, b):`) කියන්නේ ගණිතයේ එන මේ ශ්‍රිත (Functions) වලටමයි. අපි Input එකක් දුන්නාම, ඒක ඇතුළේ මොකක්හරි වැඩක් වෙලා අපිට එක Output එකක් එළියට දෙනවා. "එක Input එකකට අනිවාර්යයෙන්ම එක Output එකක් විතරයි එන්න පුළුවන්" කියන නීතිය උඩ තමයි ලෝකේ තියෙන හැම පරිගණක වැඩසටහනක්ම දුවන්නේ!

---

## 1. What is a Function? (ශ්‍රිතයක් යනු කුමක්ද?)

> [!IMPORTANT]
> **Definition:** Let $A$ and $B$ be nonempty sets. A **function** $f$ from $A$ to $B$ (written as $f: A \to B$) is a relation such that:
> 1. For **every** $x \in A$, there exists a $y \in B$ such that $(x, y) \in f$. (පළමු කුලකයේ ඇති සෑම මූලද්‍රව්‍යයකින්ම ඊතලයක් පිටවිය යුතුය. කිසිවෙක් ඉතිරි විය නොහැක!).
> 2. If $(x, y_1) \in f$ and $(x, y_2) \in f$, then $y_1 = y_2$. (පළමු කුලකයේ එකම මූලද්‍රව්‍යයකින් ඊතල දෙකක් පිටවිය නොහැක. එක Input එකකට Outputs දෙකක් තියෙන්න බෑ!).
> 
> *(සරලවම: $A$ හි ඇති සෑම කෙනෙක්ම, $B$ හි එකම එක කෙනෙක්ට ඊතලයක් යැවිය යුතුය).*

**Domain, Codomain, and Range (වසම, සමවසම සහ පරාසය):**
* $A$ is the **domain** (වසම) - ඊතල පටන් ගන්නා තැන.
* $B$ is the **codomain** (සමවසම) - ඊතල යා හැකි සියලුම තැන්.
* The **range** (පරාසය) is the set of actual outputs: $f(A) = \{f(x) : x \in A\}$. (පරාසය යනු සමවසමේ උපකුලකයක් පමණි. එනම් ඇත්තටම ඊතල වැදුණු අය පමණි).

---

## 2. Special Types of Functions (විශේෂිත ශ්‍රිත වර්ග)

විභාගයේදී ශ්‍රිතයක් දීලා එය පහත කුමන වර්ගයට අයත්දැයි ඔප්පු කරන්නට අනිවාර්යයෙන්ම පැමිණේ! මේක තේරුම් ගන්න පුටු සෙට් එකකුයි, මිනිස්සු සෙට් එකකුයි ගැන හිතන්න.

### A. Injective (One-to-One / ඒකෛක)
* **තේරුම:** වෙනස් මිනිස්සු දෙන්නෙක් කවදාවත් එකම පුටුවේ වාඩි වෙන්නේ නෑ! (එනම්, එකිනෙකට වෙනස් Inputs වලට කවදාවත් එකම Output එක ලැබෙන්නේ නෑ).
* **විභාගයට ඔප්පු කරන ආකාරය:**
  "Assume $f(x_1) = f(x_2)$. Then show that $x_1 = x_2$."
  *(උත්තර දෙකක් සමානයි කියලා හිතලා, එහෙනම් ඒකට දාපු Inputs දෙකත් සමාන වෙන්නම ඕනෙ කියලා පෙන්නන්න).*

### B. Surjective (Onto / සංග්‍රාහක)
* **තේරුම:** හැම පුටුවකම කවුරුහරි වාඩි වෙලා ඉන්නවා! හිස් පුටු නෑ. (එනම්, Codomain එකේ තියෙන හැම අගයකටම අනිවාර්යයෙන්ම Input එකක් තියෙනවා. වෙනත් විදියකින් කිව්වොත් Codomain = Range වෙනවා).
* **විභාගයට ඔප්පු කරන ආකාරය:**
  "Let $y \in B$. Show there exists $x \in A$ such that $f(x) = y$."
  *(සමීකරණයේ $y$ තනි කරලා (solve for x), ඒ ලැබෙන $x$ අගය Domain එකේ තියෙනවා කියලා පෙන්නන්න).*

### C. Bijective (ඒකෛක හා සංග්‍රාහක)
A function is **bijective** if it is BOTH injective and surjective.
*(මෙය "One-to-one correspondence" ලෙසද හැඳින්වේ. පුටු ගාණයි මිනිස්සු ගාණයි හරියටම සමානයි! එක්කෙනාට එක පුටුව ගානේ ලැබිලා තියෙනවා. ශ්‍රිතයකට **Inverse (ප්‍රතිලෝම ශ්‍රිතයක්)** තිබිය හැක්කේ එය Bijective නම් පමණි!)*

---

## 3. Exam Question Walkthrough (Proving Bijectivity and Finding Inverse)

**Question: "Let $f: \mathbb{R} \to \mathbb{R}$ be defined by $f(x) = 2x - 3$. Prove that $f$ is bijective and find its inverse."**

**How to Write the Answer (විභාගයට ලියන පියවර):**

1. **Step 1: Prove Injectivity (ඒකෛක බව ඔප්පු කිරීම).**
   *"Let $x_1, x_2 \in \mathbb{R}$ and assume $f(x_1) = f(x_2)$."*
   *"Then $2x_1 - 3 = 2x_2 - 3$."*
   *"Adding 3 to both sides: $2x_1 = 2x_2$."*
   *"Dividing by 2: $x_1 = x_2$."*
   *"Therefore, $f$ is injective."*

2. **Step 2: Prove Surjectivity (සංග්‍රාහක බව ඔප්පු කිරීම).**
   *"Let $y \in \mathbb{R}$ (from the codomain)."*
   *"We need to find an $x \in \mathbb{R}$ such that $f(x) = y$."*
   *"Set $y = 2x - 3$ and solve for $x$:"*
   *"$2x = y + 3 \implies x = \frac{y + 3}{2}$."*
   *"Since $y \in \mathbb{R}$, $x = \frac{y + 3}{2}$ is also a real number ($x \in \mathbb{R}$)."*
   *"Thus, for every $y$, there exists an $x$ such that $f(x) = y$. Therefore, $f$ is surjective."*

3. **Step 3: State Bijectivity.**
   *"Since $f$ is both injective and surjective, $f$ is bijective."*

4. **Step 4: Find the Inverse ($f^{-1}$).**
   *"Since $f$ is bijective, it has an inverse."*
   *"From Step 2, we have $x = \frac{y + 3}{2}$."*
   *"Interchanging $x$ and $y$, we get $y = \frac{x + 3}{2}$."*
   *"Therefore, $f^{-1}(x) = \frac{x + 3}{2}$."*

*(මේ විදිහට පියවරෙන් පියවර ලියද්දී විභාගයේදී සම්පූර්ණ ලකුණු ලැබෙනවා අනිවාර්යයි!)*

---

## 4. Composition of Functions (සංයුක්ත ශ්‍රිත)

Let $f: A \to B$ and $g: B \to C$. The composition $g \circ f : A \to C$ is defined by:
$$(g \circ f)(x) = g(f(x))$$

> [!WARNING]
> **නිතර සිදුවන වැරැද්දක් (Common Mistake):**
> $(g \circ f)$ ලෙස ලියා ඇති විට, මුලින්ම ගණනය කරන්නේ අගට තියෙන $f$ ශ්‍රිතයයි! බොහෝ ළමයි මුලින් තියෙන $g$ අගය මුලින්ම ආදේශ කරන්න ගොස් වරද්දා ගනී. $g \circ f \neq f \circ g$.

**උදාහරණයක්:**
$f(x) = 2x + 1$ සහ $g(x) = x^2$ නම්,
$(g \circ f)(x) = g(f(x)) = g(2x + 1) = (2x + 1)^2$.

---

## 5. Floor and Ceiling Functions

* **Floor ($\lfloor x \rfloor$):** The greatest integer less than or equal to $x$.
  *( $x$ ට වඩා කුඩා හෝ සමාන විශාලතම නිඛිලය. උදා: $\lfloor 3.7 \rfloor = 3$ )*.
* **Ceiling ($\lceil x \rceil$):** The least integer greater than or equal to $x$.
  *( $x$ ට වඩා විශාල හෝ සමාන කුඩාම නිඛිලය. උදා: $\lceil 3.7 \rceil = 4$ )*.

> [!TIP]
> **Negative Numbers (ඍණ සංඛ්‍යා වලදී ප්‍රවේශම් වන්න!):**
> ඍණ සංඛ්‍යා රේඛාවේ කුඩා වන්නේ වම් පසට බව මතක තබාගන්න.
> $\lfloor -1.2 \rfloor = -2$ (මොකද $-1.2$ ට වඩා කුඩා ඊළඟ නිඛිලය $-2$ වේ).
> $\lceil -1.2 \rceil = -1$ ($-1.2$ ට වඩා විශාල ඊළඟ නිඛිලය $-1$ වේ).
