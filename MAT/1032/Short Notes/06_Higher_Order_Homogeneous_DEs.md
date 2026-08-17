# 06. Higher Order Homogeneous DEs

> [!NOTE]
> **Background & Prerequisites (අවශ්‍ය මූලික දැනුම)**
> *   දෙවන මාත්‍රයේ සමීකරණයක් ($ax^2 + bx + c = 0$) විසඳීම: මූල සෙවීමේ සූත්‍රය $x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$.
> *   $e^{i\theta} = \cos \theta + i \sin \theta$ බව මතක තබාගන්න.

---

## 1. Higher Order Homogeneous DEs (උසස් මාත්‍රයේ සමජාතීය සමීකරණ)

**"Dummy-Proof" Concept:**
මෙතෙක් අපි හැදුවේ $y'$ (පළමු අවකලනය) විතරක් තියෙන ගණන්. දැන් අපි හදන්නේ $y''$ සහ ඊට වඩා ලොකු අවකලනයන් තියෙන ගණන්. "Homogeneous" කියන්නේ සමීකරණයේ දකුණු පැත්තේ කවුරුත් නෑ (ඒ කියන්නේ දකුණු පැත්ත 0 යි). 
මේවා හදන්න තියෙන්නේ හරිම ලේසි ක්‍රමයක්. $y'$ වෙනුවට $r$ කියන අකුර දාලා සාමාන්‍ය වර්ගජ සමීකරණයක් විසඳනවා වගේ මූල (roots) ටික හොයන්න විතරයි තියෙන්නේ.

**How to Identify:** 
සමීකරණය $a y'' + b y' + c y = 0$ වගේ හැඩයක් තියෙනවා නම්. (දකුණු පස අනිවාර්යයෙන්ම 0 විය යුතුය).

### ✍️ Step-by-Step Worked Example

**Question 1:** Solve $y'' - 5y' + 6y = 0$

*   **Step 1: Auxiliary/Characteristic Equation ලියන්න**
    $y'' \implies r^2$, $y' \implies r$, $y \implies 1$ ලෙස ආදේශ කරන්න.
    $r^2 - 5r + 6 = 0$
    
*   **Step 2: මූල (Roots) සොයන්න**
    $(r - 2)(r - 3) = 0 \implies r = 2$ සහ $r = 3$.
    මේවා **අසමාන තාත්වික මූල** (Distinct Real Roots) වේ.
    
*   **Step 3: පිළිතුර ලියන්න**
    සූත්‍රය: $y = c_1 e^{r_1 x} + c_2 e^{r_2 x}$
    **$y = c_1 e^{2x} + c_2 e^{3x}$**

**Question 2:** Solve $y'' - 4y' + 4y = 0$
*   **Step 1:** $r^2 - 4r + 4 = 0$
*   **Step 2:** $(r - 2)^2 = 0 \implies r = 2, 2$.
    මේවා **සමාන තාත්වික මූල** (Repeated Real Roots) වේ.
*   **Step 3:** පිළිතුර ලිවීමේදී දෙවැනි එක $x$ වලින් ගුණ කළ යුතුය!
    **$y = c_1 e^{2x} + c_2 x e^{2x}$** හෝ $y = (c_1 + c_2 x)e^{2x}$.

> [!CAUTION]
> **Exam Trap:** මූල දෙකම සමාන වුණාම ළමයි නිකම්ම $y = c_1 e^{2x} + c_2 e^{2x}$ කියලා ලියනවා. එතකොට ඒ පද දෙක එකම ජාතියේ නිසා එකතු වෙලා එක නියතයක් වෙනවා. ඒ නිසා අනිවාර්යයෙන්ම දෙවැනි එක $x$ වලින් (තව එකක් තිබ්බොත් $x^2$ වලින්) ගුණ කරන්නම ඕනේ!

**Question 3:** Solve $y'' + 4y = 0$
*   **Step 1:** $r^2 + 4 = 0$
*   **Step 2:** $r^2 = -4 \implies r = \pm 2i$.
    මේවා **සංකීර්ණ මූල** (Complex Roots) වේ. ($r = \alpha \pm i\beta$ හි $\alpha = 0, \beta = 2$).
*   **Step 3:** සූත්‍රය: $y = e^{\alpha x} (c_1 \cos \beta x + c_2 \sin \beta x)$.
    **$y = c_1 \cos(2x) + c_2 \sin(2x)$** (මෙහි $e^{0} = 1$ වේ).

---

## 2. The Wronskian (රොන්ස්කියන්)

**"Dummy-Proof" Concept:**
අපිට උත්තර දෙකක් ආවම ($y_1$ සහ $y_2$), ඒ දෙක එකිනෙකින් ස්වාධීනද (Linearly Independent) කියලා බලන ටෙස්ට් එක තමයි Wronskian කියන්නේ. මේක නිකම්ම matrix එකක ඩිටර්මිනන්ට් එකක් (Determinant) හොයනවා වගේ වැඩක්.

**How to calculate:**
$W(y_1, y_2) = \begin{vmatrix} y_1 & y_2 \\ y_1' & y_2' \end{vmatrix} = y_1 y_2' - y_2 y_1'$

*   $W \neq 0$ නම්, ඒවා Linearly Independent (ස්වාධීනයි).
*   $W = 0$ නම්, Linearly Dependent.

**Example:** Check if $y_1 = \sin x$ and $y_2 = \cos x$ are linearly independent.
*   $y_1' = \cos x$
*   $y_2' = -\sin x$
*   $W = (\sin x)(-\sin x) - (\cos x)(\cos x) = -\sin^2 x - \cos^2 x = -(\sin^2 x + \cos^2 x) = -1(1) = -1$.
*   $-1 \neq 0$ බැවින්, ඒවා **Linearly Independent** වේ.
