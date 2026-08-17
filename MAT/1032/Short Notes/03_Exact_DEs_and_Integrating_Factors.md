# 03. Exact DEs & Integrating Factors

> [!NOTE]
> **Background & Prerequisites (අවශ්‍ය මූලික දැනුම)**
> මේ පාඩමට Partial Differentiation (ආංශික අවකලනය) අත්‍යවශ්‍ය වේ. 
> *   $y$ විෂයෙන ආංශික අවකලනය කරන විට, $x$ අකුර නිකම්ම නිකම් අංකයක් (Constant) වගේ සලකන්න.
> *   $x$ විෂයෙන ආංශික අවකලනය කරන විට, $y$ අකුර අංකයක් වගේ සලකන්න.

---

## 1. Exact Differential Equations (යථාර්ථ සමීකරණ)

**"Dummy-Proof" Concept:**
අපිට සමීකරණයක් දෙනවා $M(x,y) dx + N(x,y) dy = 0$ කියලා හැඩයකින්. මේක Exact ද නැද්ද කියලා අඳුරගන්න පොඩි ටෙස්ට් එකක් තියෙනවා. ඒ ටෙස්ට් එක පාස් වුණොත්, අපිට කෙලින්ම සූත්‍රයක් පාවිච්චි කරලා උත්තරේ ගන්න පුළුවන්.

**How to Identify (හඳුනාගන්නා කෙටික්‍රමය):**
$\frac{\partial M}{\partial y} = \frac{\partial N}{\partial x}$ වෙනවා නම්, ඒක Exact!
*   $M$ කියන්නේ $dx$ ළඟ ඉන්න කෙනා (එයාව $y$ න් අවකලනය කරන්න).
*   $N$ කියන්නේ $dy$ ළඟ ඉන්න කෙනා (එයාව $x$ න් අවකලනය කරන්න).

### ✍️ Step-by-Step Worked Example

**Question:** Solve $(2xy + 3) dx + (x^2 - 1) dy = 0$

*   **Step 1: Check Exactness (ටෙස්ට් එක කරමු)**
    මෙහි $M = 2xy + 3$ සහ $N = x^2 - 1$.
    $\frac{\partial M}{\partial y} = 2x(1) + 0 = 2x$ (මෙහි $x$ නියතයකි).
    $\frac{\partial N}{\partial x} = 2x - 0 = 2x$ (මෙහි $y$ නියතයකි).
    දෙකම සමාන නිසා, මෙය **Exact** වේ!

*   **Step 2: $M$ යන්න $x$ විෂයෙන අනුකලනය කරන්න ($f$ සෙවීම)**
    $f(x,y) = \int M \, dx + g(y)$
    $f(x,y) = \int (2xy + 3) \, dx + g(y)$
    (මෙහි $y$ නියතයක් ලෙස සලකා $x$ වලින් integrate කරන්න).
    $f(x,y) = 2y \left(\frac{x^2}{2}\right) + 3x + g(y) = x^2 y + 3x + g(y)$ --- (Equation 1)

*   **Step 3: ලැබුණු උත්තරය $y$ න් අවකලනය කර $N$ ට සමාන කරන්න**
    Equation 1 න් $\frac{\partial f}{\partial y}$ ගනිමු:
    $\frac{\partial f}{\partial y} = x^2(1) + 0 + g'(y) = x^2 + g'(y)$
    
    මෙය $N$ ට සමාන කරන්න ($N = x^2 - 1$):
    $x^2 + g'(y) = x^2 - 1 \implies g'(y) = -1$

*   **Step 4: $g(y)$ සොයාගෙන අවසාන පිළිතුර ලිවීම**
    $g'(y) = -1$ නම් අනුකලනය කළ විට $\implies g(y) = -y$.
    අවසාන පිළිතුර $f(x,y) = C$ ලෙස ලියන්න:
    **$x^2 y + 3x - y = C$**

---

## 2. Integrating Factors (අනුකලන සාධක)

**"Dummy-Proof" Concept:**
සමහර වෙලාවට අපි අර කලින් කරපු ටෙස්ට් එක ෆේල් වෙනවා ($\frac{\partial M}{\partial y} \neq \frac{\partial N}{\partial x}$). ඒ කියන්නේ ඒක Exact නෑ. හැබැයි අපි "Integrating Factor (I.F.)" කියලා විශේෂ පදයකින් මුළු සමීකරණයම ගුණ කළොත්, ඒක මැජික් එකක් වගේ ආයෙත් Exact වෙනවා!

**How to find I.F. (සූත්‍ර 2ක් ඇත):**
1.  **Rule 1:** $\frac{1}{N} \left( \frac{\partial M}{\partial y} - \frac{\partial N}{\partial x} \right) = P(x)$ ආවොත්, **I.F. = $e^{\int P(x) dx}$**
2.  **Rule 2:** $\frac{1}{M} \left( \frac{\partial N}{\partial x} - \frac{\partial M}{\partial y} \right) = Q(y)$ ආවොත්, **I.F. = $e^{\int Q(y) dy}$**

> [!CAUTION]
> **Exam Trap:**
> ගොඩක් ළමයි I.F. එක හෙව්වට පස්සේ අමතක වෙලා නිකම්ම ඉන්නවා. I.F. එක හෙව්වට පස්සේ අනිවාර්යයෙන්ම **මුල් සමීකරණයේ හැම පදයක්ම I.F. එකෙන් ගුණ කරන්න ඕනේ!** එතකොට තමයි ඒක Exact වෙන්නේ. ඊට පස්සේ අර කලින් Exact ගාණ හදපු විදිහටම ගාණ හදන්න ඕනේ.
