---
course: MAT 1013
title: 10. Sets, Set Algebra and Cardinality
---

# 10. Sets, Set Algebra and Cardinality
### කුලක, කුලක වීජගණිතය සහ අවයව සංඛ්‍යාව (Lesson 10)

> [!NOTE] 
> **මොකක්ද මේ පාඩම? ඇයි අපි මේක ඉගෙන ගන්නේ?**
> ඔබ දවසක Software Engineer කෙනෙක් වෙලා Database එකකින් දත්ත හොයන්න SQL Query එකක් ලියනකොට (උදා: `SELECT * FROM Users WHERE age > 20 AND city = 'Colombo'`), ඒ පිටිපස්සේ වැඩ කරන්නේ වෙන මොකක්වත් නෙවෙයි, මේ Set Algebra (කුලක වීජගණිතය) තමයි! දත්ත සමුදායක් (Database) කියන්නේම කුලකයක්. ඒ දත්ත එකතු කරන්නේ (Union), පොදු ඒවා හොයන්නේ (Intersection) මේ පාඩමේ තියෙන නීති වලට අනුවයි.

---

## 1. What is a Set? (කුලකයක් යනු කුමක්ද?)

> [!IMPORTANT]
> **Definition:** A **set** is a well-defined collection of objects. The objects in a set are called its **elements** (අවයව).

**Methods of Describing Sets (කුලකයක් දක්වන ක්‍රම):**
1. **Roster Method (අවයව ලැයිස්තුගත කිරීම):** $A = \{1, 2, 3, 4, 5\}$
2. **Descriptive Method (විස්තරාත්මකව):** $A = \text{the set of natural numbers less than 6}$
3. **Set-Builder Method (ගොඩනැගීමේ ආකාරය):** $A = \{x \in \mathbb{N} : x < 6\}$

### Membership vs. Subset ($\in$ සහ $\subseteq$ අතර වෙනස)
විභාගයේදී ළමයි නිතරම පටලවා ගන්න තැනක් තමයි මේක. 
$A = \{1, 2, 3\}$ ලෙස ගනිමු.
* **$\in$ (Element of):** මේකෙන් පෙන්නන්නේ "ඇතුලේ තියෙන කෑල්ලක්" කියන එකයි. උදාහරණයක් විදිහට $1 \in A$ (1 කියන්නේ A කුලකය ඇතුලේ තියෙන අවයවයක්).
* **$\subseteq$ (Subset):** මේකෙන් පෙන්නන්නේ "කුඩා කුලකයක්, ලොකු කුලකයක් ඇතුලේ තියෙනවා" කියන එකයි. ඒ කියන්නේ මේ ලකුණ දෙපැත්තේම තියෙන්න ඕනෙ කුලක! උදාහරණයක් විදිහට $\{1, 2\} \subseteq A$.

> [!WARNING]
> **නිතර සිදුවන වැරැද්දක්:**
> $2 \subseteq A$ කියා ලිවීම සම්පූර්ණයෙන්ම වැරදියි! (2 කියන්නේ අංකයක් මිසක් කුලකයක් නෙවෙයිනෙ). ඒ වගේම $\{2\} \in A$ කියලා ලියන්නත් බෑ! (A ඇතුලේ තියෙන්නේ නිකම්ම 2 මිසක් සඟල වරහන් දාපු 2 නෙවෙයිනෙ).

---

## 2. Power Sets (බල කුලක)

කුලකයකින් හදන්න පුළුවන් **සියලුම උපකුලක (Subsets)** ටික ඔක්කොම එකතු කරලා ආයෙත් කුලකයක් හැදුවොත්, අන්න ඒකට Power Set $\mathcal{P}(A)$ යැයි කියයි.

**උදාහරණයක්:**
$A = \{1, 2\}$ නම්,
$\mathcal{P}(A) = \{\emptyset, \{1\}, \{2\}, \{1, 2\}\}$.
*(මතක තබාගන්න: හිස් කුලකය $\emptyset$ සහ කුලකයම $A$, ඕනෑම කුලකයක උපකුලක වේ).*

> [!TIP]
> **අවයව ගණන සෙවීම:**
> යම් කුලකයක අවයව $n$ ගාණක් තියෙනවා නම්, එහි Power set එකේ අනිවාර්යයෙන්ම අවයව **$2^n$** ක් තියෙන්න ඕනෙ! (ඉහත උදාහරණයේ $2^2 = 4$ කි).

---

## 3. Set Operations and Venn Diagrams (කුලක කර්ම සහ වෙන් රූප)

Let $A$ and $B$ be subsets of a universal set $U$.
* **Union (මේලය - $\cup$):** $A \cup B = \{x : x \in A \text{ or } x \in B\}$
* **Intersection (ඡේදනය - $\cap$):** $A \cap B = \{x : x \in A \text{ and } x \in B\}$
* **Difference (අන්තරය - $\setminus$):** $A \setminus B = \{x : x \in A \text{ and } x \notin B\}$
* **Complement (අනුපූරකය - $A^c$):** $A^c = \{x \in U : x \notin A\}$

---

## 4. Cartesian Products (කාටීසීය ගුණිතය)

කුලක දෙකකින් සමන්විත ක්‍රමිත යුගල (Ordered pairs) සෑදීම මෙයින් අදහස් වේ.
$$A \times B = \{(a, b) : a \in A, b \in B\}$$

**උදාහරණයක්:**
$A = \{1, 2\}$ සහ $B = \{a, b, c\}$ නම්:
$A \times B = \{(1, a), (1, b), (1, c), (2, a), (2, b), (2, c)\}$.

*සටහන: $\text{Cardinality}$ හෙවත් අවයව ගණන සෙවීමේදී $|A \times B| = |A| \times |B|$ වේ. (මෙහි $2 \times 3 = 6$ කි).*

---

## 5. Exam Question Walkthrough (Proving Set Identities)

විභාගයේදී $X = Y$ යැයි කුලක දෙකක් සමාන බව ඔප්පු කරන්න ආවොත්, ඒක කරන්නේ **"Mutual Inclusion (අන්‍යෝන්‍ය අන්තර්ගතය)"** කියන ක්‍රමයටයි. ඒ කියන්නේ වම් පැත්ත, දකුණු පැත්තේ උපකුලකයක් කියලත්, දකුණු පැත්ත වම් පැත්තේ උපකුලකයක් කියලත් වෙන වෙනම පෙන්වන්න ඕනෙ. (ඔබ මෙහිදී Venn diagrams පාවිච්චි කළොත් ලකුණු ලැබෙන්නේ නෑ!).

**Question: "Prove De Morgan's Law for sets: $(A \cup B)^c = A^c \cap B^c$"**

**How to Write the Answer (විභාගයට ලියන පියවර):**

1. **Part 1: Prove $(A \cup B)^c \subseteq A^c \cap B^c$**
   *"Let $x \in (A \cup B)^c$."* (වම් පැත්තේ තියෙනවා කියලා හිතමු).
   *"By definition of complement, $x \notin (A \cup B)$."*
   *"This means $x$ is neither in $A$ nor in $B$."*
   *"So, $x \notin A$ **and** $x \notin B$."*
   *"Therefore, $x \in A^c$ **and** $x \in B^c$."*
   *"By definition of intersection, $x \in A^c \cap B^c$."*
   *"Hence, $(A \cup B)^c \subseteq A^c \cap B^c$."*

2. **Part 2: Prove $A^c \cap B^c \subseteq (A \cup B)^c$**
   *"Conversely, let $x \in A^c \cap B^c$."* (දකුණු පැත්තේ තියෙනවා කියලා හිතමු).
   *"By definition of intersection, $x \in A^c$ **and** $x \in B^c$."*
   *"This means $x \notin A$ **and** $x \notin B$."*
   *"So, $x$ cannot be in their union: $x \notin (A \cup B)$."*
   *"By definition of complement, $x \in (A \cup B)^c$."*
   *"Hence, $A^c \cap B^c \subseteq (A \cup B)^c$."*

3. **Part 3: Final Conclusion**
   *"Since both inclusions hold, $(A \cup B)^c = A^c \cap B^c$. (Q.E.D)."*

---

## 6. Inclusion-Exclusion Principle (අන්තර්ගත-බහිෂ්කෘත මූලධර්මය)

කුලක දෙකක් එකතු කළ විට (Union), පොදු කොටස (Intersection) දෙපාරක් ගණනය වන නිසා එය එක් වරක් අඩු කළ යුතුය.

**For two sets (කුලක 2ක් සඳහා):**
$$|A \cup B| = |A| + |B| - |A \cap B|$$

**For three sets (කුලක 3ක් සඳහා):**
$$|A \cup B \cup C| = |A| + |B| + |C| - |A \cap B| - |B \cap C| - |A \cap C| + |A \cap B \cap C|$$
