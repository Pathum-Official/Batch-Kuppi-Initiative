---
course: MAT 1013
title: 09. Complex Numbers, Polar Form and Roots of Unity
---

# 09. Complex Numbers, Polar Form and Roots of Unity
### සංකීර්ණ සංඛ්‍යා, ධ්‍රැවීය ආකාරය සහ ඒකකයේ මූල (Lesson 9)

> [!NOTE] 
> **මොකක්ද මේ පාඩම? ඇයි අපි මේක ඉගෙන ගන්නේ?**
> සාමාන්‍ය ගණිතයේදී $x^2 = -1$ කියලා ආවොත් අපි කියනවා "මේකට උත්තරයක් නෑ" කියලා. මොකද ඕනෙම ඉලක්කමක් වර්ග කළාම ධන වෙනවනේ. හැබැයි Electrical Engineering (විදුලි ඉංජිනේරු විද්‍යාව) වලදී තරංග (Waves/Signals) මනින්නත්, Computer Graphics වල 3D රූප කරකවන්නත් (Rotations) අපිට මේකට උත්තරයක් ඕනෙම වුණා. ඒ නිසා ගණිතඥයෝ අලුත් ඉලක්කමක් හඳුන්වා දුන්නා $i$ කියලා ($i^2 = -1$). මේ අලුත් සංඛ්‍යා වලට කියන්නේ "සංකීර්ණ සංඛ්‍යා (Complex Numbers)" කියලයි.

---

## 1. Complex Numbers (සංකීර්ණ සංඛ්‍යා - $\mathbb{C}$)

අපි අලුත් ඒකකයක් (Imaginary unit) $i$ ලෙස හඳුන්වා දෙමු:
$$i^2 = -1$$

> [!IMPORTANT]
> **Definition:** The set of complex numbers is:
> $$\mathbb{C} = \{ a + bi : a, b \in \mathbb{R}, i^2 = -1 \}$$
> $z = a + bi$ ලෙස ගත් විට:
> - **Real part (තාත්වික කොටස):** $\text{Re}(z) = a$
> - **Imaginary part (අතාත්වික කොටස):** $\text{Im}(z) = b$ (මෙහි $i$ අකුර ලියන්නේ නැත, $b$ පමණි).

### Arithmetic of Complex Numbers (සුළු කිරීම්)
$z_1 = 2 + 3i$ සහ $z_2 = 1 - 2i$ නම්:
* **Addition (එකතු කිරීම):** $(2+1) + (3-2)i = 3 + 1i$
* **Multiplication (ගුණ කිරීම):** 
  $(2 + 3i)(1 - 2i) = 2 - 4i + 3i - 6i^2$
  මෙහි $i^2 = -1$ බැවින්, $-6(-1) = +6$ වේ.
  පිළිතුර: $2 + 6 - i = 8 - i$.

---

## 2. Complex Conjugate and Modulus (සංයුග්මකය සහ මාපාංකය)

> [!TIP]
> භාගයක හරයේ (Denominator) $i$ අකුරක් තියෙනවා නම් එය සුළු කර ඉවත් කරන්නට **Complex conjugate (සංයුග්මකය)** භාවිතා කරයි.

* **Conjugate ($\bar{z}$):** $z = a + bi$ නම්, එහි සංයුග්මකය $\bar{z} = a - bi$ වේ. (මැද ලකුණ මාරු කරන්න).
* **Modulus ($|z|$):** $z = a + bi$ නම්, එහි මාපාංකය $|z| = \sqrt{a^2 + b^2}$ වේ. (මෙයින් අදහස් කරන්නේ ප්‍රස්ථාරයේ මූල ලක්ෂ්‍යයේ සිට $z$ ට ඇති දුරයි).

**වටිනා සමීකරණයක් (නිතරම භාවිතා වන):**
$$z \bar{z} = a^2 + b^2 = |z|^2$$

**Multiplicative Inverse ($z^{-1}$):**
$$z^{-1} = \frac{\bar{z}}{|z|^2} = \frac{a - bi}{a^2 + b^2}$$

---

## 3. The Complex Plane and Polar Form (සංකීර්ණ තලය සහ ධ්‍රැවීය ආකාරය)

සංකීර්ණ සංඛ්‍යාවක් $z = a + bi$, ප්‍රස්ථාරයක ඛණ්ඩාංකයක් $(a, b)$ ලෙස ඇඳිය හැක. මෙය Argand plane ලෙස හැඳින්වේ. (මෙහි X අක්ෂය Real axis වන අතර, Y අක්ෂය Imaginary axis වේ).

**Polar Representation (ධ්‍රැවීය ආකාරය):**
සංඛ්‍යාවට $(a, b)$ අගයන් දෙනවා වෙනුවට, මූල ලක්ෂ්‍යයේ සිට ඇති දුර ($r$) සහ X අක්ෂය සමඟ සාදන කෝණය ($\theta$) මඟින්ද මෙය ලිවිය හැක.
* $r = |z| = \sqrt{a^2 + b^2}$
* $\tan \theta = \frac{b}{a}$ (මෙම $\theta$ කෝණය Argument එක හෙවත් $\text{arg}(z)$ ලෙස හැඳින්වේ).

එවිට: $a = r \cos \theta$ සහ $b = r \sin \theta$.
$$z = r(\cos \theta + i \sin \theta)$$

### Euler's Formula (ඔයිලර්ගේ සමීකරණය)
$$e^{i\theta} = \cos \theta + i \sin \theta$$
මේ නිසා Polar form එක ඉතාමත් කෙටියෙන් මෙහෙමත් ලියන්න පුළුවන්:
$$z = r e^{i\theta}$$

---

## 4. Exam Question Walkthrough (De Moivre's Theorem)

සංකීර්ණ සංඛ්‍යාවක ලොකු බලයක් (Power එකක්) හොයන්න ආවොත්, ඒක ගුණ කර කර ඉන්න අමාරුයි. අන්න ඒකට තමයි **De Moivre's Theorem (ඩි මුවාවර්ගේ ප්‍රමේයය)** පාවිච්චි කරන්නේ! 
> $$(\cos \theta + i \sin \theta)^n = \cos(n\theta) + i \sin(n\theta)$$
> *(Power එක කෙලින්ම ඇවිත් කෝණයෙන් ගුණ වෙනවා!)*

**Question: "Compute $(1 + i)^8$ using De Moivre's Theorem."**

**How to Write the Answer (විභාගයට ලියන පියවර):**
1. **Step 1: Polar form එකට හරවන්න.**
   *"Let $z = 1 + i$. Then $r = \sqrt{1^2 + 1^2} = \sqrt{2}$."*
   *"And $\tan \theta = \frac{1}{1} = 1 \implies \theta = \frac{\pi}{4}$."*
   *"So, $z = \sqrt{2} \left( \cos \frac{\pi}{4} + i \sin \frac{\pi}{4} \right)$ or $z = \sqrt{2} e^{i\pi/4}$."*

2. **Step 2: De Moivre's Theorem යොදන්න.**
   *"Applying De Moivre's Theorem for $z^8$: "*
   $$z^8 = (\sqrt{2})^8 \left( \cos \left(8 \times \frac{\pi}{4}\right) + i \sin \left(8 \times \frac{\pi}{4}\right) \right)$$
   $$z^8 = 16 (\cos 2\pi + i \sin 2\pi)$$

3. **Step 3: අවසාන උත්තරය ගන්න.**
   *"Since $\cos 2\pi = 1$ and $\sin 2\pi = 0$:"*
   $$z^8 = 16(1 + 0i) = 16$$

---

## 5. Roots of Unity (ඒකකයේ මූල)

$z^n = 1$ යන සමීකරණය විසඳීම මෙයින් අදහස් වේ. තාත්වික ලෝකයේදී නම් මෙයට තියෙන්නේ උත්තර 1යි හරි 2යි හරි විතරයි. (උදා: $x^2 = 1 \implies x = \pm 1$). නමුත් සංකීර්ණ ලෝකයේදී **$z^n = 1$ ට හරියටම උත්තර $n$ ප්‍රමාණයක් තියෙනවා!** ඒවට අපි කියන්නේ "$n$-th roots of unity" කියලයි.

**මූලයන් සොයන සමීකරණය:**
$$z_k = e^{i\frac{2\pi k}{n}} = \cos\left(\frac{2\pi k}{n}\right) + i \sin\left(\frac{2\pi k}{n}\right)$$
මෙහි $k = 0, 1, 2, \dots, n-1$ අගයන් ආදේශ කිරීමෙන් පිළිතුරු $n$ ප්‍රමාණයම ලබාගත හැක.

> [!NOTE]
> මෙම මූලයන් $n$ ප්‍රමාණය ප්‍රස්ථාරයක ලකුණු කළොත්, ඒවා අරය 1ක් වන රවුමක් වටේට සමාන දුරින් පිහිටන ලක්ෂ්‍යයන් වේ (Vertices of a regular $n$-gon).
