---
course: MAT 1013
title: 11. Relations, Equivalence and Partial Orders
---

# 11. Relations, Equivalence and Partial Orders
### සම්බන්ධතා, සමතුල්‍යතාව සහ භාගික ක්‍රම (Lesson 11)

> [!NOTE] 
> **මොකක්ද මේ පාඩම? ඇයි අපි මේක ඉගෙන ගන්නේ?**
> ගණිතයේදී සහ පරිගණක විද්‍යාවේදී විවිධ වස්තූන් අතර ඇති "සම්බන්ධතා (Relationships)" අධ්‍යයනය කිරීම ඉතා වැදගත් වේ. උදාහරණයක් විදිහට Facebook එකේ මිතුරන් සම්බන්ධ වෙන්නේ කොහොමද? කෙනෙක් තව කෙනෙක්ගේ යාළුවෙක් වුණොත් අනිත් කෙනාත් එයාගේ යාළුවෙක් වෙනවා (මේකට කියන්නේ Symmetric කියලා). හැබැයි Instagram එකේ කෙනෙක්ව Follow කළාට, එයා ආපහු Follow කරන්නේ නැතිවෙන්න පුළුවන් (Not symmetric). මේ වගේ සැබෑ ලෝකයේ ගැටලු Database එකකට දාන්න කලින් අපි මේවා ගණිතානුකූලව වෙන් කරලා අඳුරගන්න ඕනෙ. ඒක තමයි අපි මේ පාඩමෙන් කරන්නේ.

---

## 1. Binary Relations (ද්විමය සම්බන්ධතා)

> [!IMPORTANT]
> **Definition:** A **binary relation** from a set $A$ to a set $B$ is any subset of the Cartesian product $A \times B$.
> We write $R \subseteq A \times B$. If $(a, b) \in R$, we say $a$ is related to $b$ and write **$aRb$**.
> *(සම්බන්ධතාවයක් කියන්නේ නිකම්ම Cartesian product එකෙන් තෝරගත්තු ක්‍රමිත යුගල (Ordered pairs) කීපයක් විතරයි).*

**විභාගයට අනිවාර්යයෙන්ම එන වචන 3ක්:**
හිතන්න පිරිමි ළමයි කුලකයක් ($A$) ඉන්නවා. ගැහැණු ළමයි කුලකයක් ($B$) ඉන්නවා. අපි සම්බන්ධතාවය හදන්නේ "ආදරය කරනවා" කියලා.
1. **Source Set ($A$):** මුළු පිරිමි ළමයි ඔක්කොම. (මේකට Domain කියන්න එපා!).
2. **Target Set / Codomain ($B$):** මුළු ගැහැණු ළමයි ඔක්කොම.
3. **Actual Domain ($\text{Dom}(R)$):** ඇත්තටම කාටහරි ආදරය කරන පිරිමි ළමයි ටික විතරයි. (සමහර පිරිමි ළමයි කාටවත් ආදරය කරන්නේ නැතුව ඉන්න පුළුවන්නෙ. එයාලා Domain එකට අයිති නෑ).
4. **Range ($\text{Ran}(R)$):** ඇත්තටම ආදරය ලබන ගැහැණු ළමයි ටික විතරයි. (සමහර අයට කවුරුත් ආදරේ කරන්නේ නැතුව ඉන්න පුළුවන්. ඒ අය Range එකට අයිති නෑ).

*ඒ නිසා කවදාවත් Codomain එකයි Range එකයි පටලවා ගන්න එපා. $\text{Ran}(R) \subseteq B$ වේ.*

---

## 2. Properties of Relations (සම්බන්ධතාවල ගුණාංග)

$R$ යනු $A$ කුලකය මත ඇති සම්බන්ධතාවයක් යැයි සිතමු ($R \subseteq A \times A$). මේවා කටපාඩම් කරන්න එපා, තේරුම් ගන්න!

| Property (ගුණාංගය) | Definition (නිර්වචනය) | Graphically (ප්‍රස්ථාරිකව) | Everyday Example |
| :--- | :--- | :--- | :--- |
| **Reflexive** (පරාවර්තී) | $\forall a \in A, (a, a) \in R$ <br> *(සෑම මූලද්‍රව්‍යයක්ම තමන්ටම සම්බන්ධ වී ඇත)* | සෑම ලක්ෂ්‍යයකම Loop එකක් ඇත. | හැමෝම තමන්ටම ආදරය කරයි. |
| **Irreflexive** (අපරාවර්තී) | $\forall a \in A, (a, a) \notin R$ <br> *(කිසිම මූලද්‍රව්‍යයක් තමන්ට සම්බන්ධ නැත)* | එකම Loop එකක්වත් නැත. | කිසිවෙක් තමන්ටම ආදරය නොකරයි. |
| **Symmetric** (සමමිතික) | If $(a, b) \in R \implies (b, a) \in R$ <br> *($a$ සිට $b$ ට ඊතලයක් ඇත්නම්, $b$ සිට $a$ ටද ඊතලයක් තිබිය යුතුය)* | සෑම ඊතලයකටම ආපසු එන ඊතලයක් ඇත (Reverse arrow). | Facebook මිත්‍රත්වය (එකපැත්තකට යාළුවෙක් වෙන්න බෑ). |
| **Antisymmetric** (ප්‍රතිසමමිතික) | If $(a, b) \in R$ and $(b, a) \in R \implies a = b$ <br> *(වෙනස් ලක්ෂ්‍ය දෙකක් අතර දෙපැත්තටම ඊතල තිබිය නොහැක)* | ලක්ෂ්‍ය දෙකක් අතර එක පැත්තකට පමණක් ඊතල ඇත. | "වඩා කුඩා හෝ සමානයි ($\le$)" (2$\le$3 නම් 3$\le$2 වෙන්න බෑනෙ). |
| **Transitive** (සංක්‍රාමී) | If $(a, b) \in R$ and $(b, c) \in R \implies (a, c) \in R$ <br> *($a$ සිට $b$ ටත්, $b$ සිට $c$ ටත් ඊතල ඇත්නම්, $a$ සිට $c$ ට කෙලින්ම ඊතලයක් (shortcut) තිබිය යුතුය)* | සෑම step දෙකක ගමනකටම, කෙටි පාරක් (shortcut) ඇත. | ලේ නෑකම (A, B ගේ සහෝදරයෙක් නම්, B, C ගේ සහෝදරයෙක් නම්, A, C ගේ ද සහෝදරයෙක් වේ). |

> [!WARNING]
> **නිතර සිදුවන වැරැද්දක් (Common Mistake):**
> "Symmetric නොවේ" යන්නෙන් "Antisymmetric" අදහස් නොවේ! මේවා සම්පූර්ණයෙන්ම වෙනස් ගුණාංග දෙකකි. උදාහරණයක් ලෙස "Equality" ($=$) යනු Symmetric සහ Antisymmetric යන දෙකම වේ! සමහර සම්බන්ධතා මේ දෙකම නෙවෙයි වෙන්නත් පුළුවන්.

---

## 3. Exam Question Walkthrough (Proving an Equivalence Relation)

> [!TIP]
> **Equivalence Relation (සමතුල්‍යතා සම්බන්ධතාවක්)** කියන්නේ Reflexive, Symmetric, සහ Transitive කියන ගුණාංග 3ම තියෙන සම්බන්ධතාවයකටයි. විභාගයට අනිවාර්යයෙන්ම මේ 3 ඔප්පු කරන්න එනවා.

**Question: "Let $R$ be a relation on integers $\mathbb{Z}$ defined by $aRb \iff a - b$ is even. Prove that $R$ is an equivalence relation."**
*(ප්‍රශ්නය: නිඛිල කුලකය මත $aRb$ යන්න "a - b ඉරට්ටේ වේ" ලෙස අර්ථ දක්වා ඇත. මෙය සමතුල්‍යතාවයක් බව ඔප්පු කරන්න).*

**How to Write the Answer (විභාගයට ලියන පියවර):**

1. **Step 1: Prove Reflexivity (පරාවර්තී බව ඔප්පු කිරීම).**
   *"Let $a \in \mathbb{Z}$."*
   *"Consider $a - a = 0$."*
   *"Since 0 is an even integer (as $0 = 2 \times 0$), we have $aRa$."*
   *"Therefore, $R$ is reflexive."*

2. **Step 2: Prove Symmetry (සමමිතික බව ඔප්පු කිරීම).**
   *"Assume $aRb$. This means $a - b$ is even."*
   *"By definition of even numbers, $a - b = 2k$ for some integer $k$."*
   *"Multiply both sides by -1: $-(a - b) = -2k \implies b - a = 2(-k)$."*
   *"Since $-k$ is also an integer, $b - a$ is even."*
   *"Therefore, $bRa$. Hence, $R$ is symmetric."*

3. **Step 3: Prove Transitivity (සංක්‍රාමී බව ඔප්පු කිරීම).**
   *"Assume $aRb$ and $bRc$."*
   *"This means $a - b$ is even (so $a - b = 2k$) and $b - c$ is even (so $b - c = 2m$) for some integers $k, m$."*
   *"Add the two equations together: $(a - b) + (b - c) = 2k + 2m$."*
   *"Simplifying gives: $a - c = 2(k + m)$."*
   *"Since $k + m$ is an integer, $a - c$ is even."*
   *"Therefore, $aRc$. Hence, $R$ is transitive."*

4. **Step 4: Final Conclusion (අවසාන නිගමනය).**
   *"Since $R$ is reflexive, symmetric, and transitive, $R$ is an equivalence relation. (Q.E.D)."*

---

## 4. Partial Orders and Hasse Diagrams (භාගික ක්‍රම)

වස්තූන් යම් පිළිවෙළකට (Order) පෙළගස්වන්න ඕනෙ වුණාම අපි පාවිච්චි කරන්නේ Partial orders. 
A relation that is **reflexive**, **antisymmetric**, and **transitive** is called a partial order. (උදා: $\le$, $\subseteq$, Divisibility $|$).

**Hasse Diagrams අඳින්නේ කොහොමද?**
මේක Partial order එකක් ප්‍රස්ථාරිකව අඳින ලේසිම ක්‍රමයයි. මෙහිදී:
1. හැම element එකටම රවුමක් අඳින්න.
2. ලොකු අගයන් උඩින්ද, කුඩා අගයන් පහළින්ද අඳින්න (උදා: $2|4$ නම්, 4 උඩින් අඳින්න).
3. **Loops අඳින්න එපා!** (Reflexive නිසා කොහොමත් loops තියෙන බව දන්නවා).
4. **ඊතල (Arrowheads) දාන්න එපා!** (හැම වෙලේම ඊතලේ යන්නේ පල්ලෙහා ඉඳන් උඩට කියලා අපි දන්නවා).
5. **Shortcuts (Transitive edges) අඳින්න එපා!** (උදා: 2න් 4 බෙදෙනවා, 4න් 8 බෙදෙනවා. එහෙනම් 2න් 8 බෙදෙනවා කියලා අමුතුවෙන් ඉරක් අඳින්න ඕනෙ නෑ). 

---

## 5. Closures of Relations (සම්බන්ධතා සංවෘත කිරීම)

යම් සම්බන්ධතාවයකට (Relation) උදාහරණයක් ලෙස Reflexive ගුණය නැත්නම්, අපි අඩුවෙලා තියෙන Loops ටික විතරක් එයට එකතු කරලා ඒක Reflexive කරනවා. මේකට තමයි Closure එකක් හොයනවා කියන්නේ. (මේක හරියට නැති ලක්ෂණයක් අලුතින් ඇතුල් කරනවා වගේ වැඩක්).

* **Reflexive Closure ($R_{\text{ref}}$):** අඩුවෙලා තියෙන $(a, a)$ දත්ත (loops) එකතු කිරීම.
  $$R_{\text{ref}} = R \cup I_A$$ (මෙහි $I_A$ යනු Identity relation එකයි).
* **Symmetric Closure ($R_{\text{sym}}$):** අඩුවෙලා තියෙන reverse ඊතල එකතු කිරීම.
  $$R_{\text{sym}} = R \cup R^{-1}$$
* **Transitive Closure ($R^+$):** අඩුවෙලා තියෙන shortcuts එකතු කිරීම. (මෙය පරිගණක වලදී පහසුවෙන් සොයාගැනීමට Warshall's algorithm භාවිතා කරයි).
