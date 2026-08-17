# 🎓 MAT 112 2.0 Differential Equations - 2022 Past Paper Discussion

> [!NOTE]
> **Premium Discussion Guide**
> මෙය 2022 November විභාගයේ ප්‍රශ්න පත්‍රය සඳහා සකසන ලද අතිශය සවිස්තරාත්මක විවරණයකි. මෙහි සෑම ප්‍රශ්නයකටම අදාළ තියරි කොටස්, අපගේ `Notes_Organized` ෆෝල්ඩරයේ ඇති ගොනු වලට Link කර ඇත.

---

## 🎯 Question 01 (මූලික සංකල්ප සහ පළමු පෙළ සමීකරණ)

### Q1 (a) Order and Degree
> **Question:** Find the order and the degree of the following differential equations.
> **📖 Theory Link:** [01. Introduction: Order, Degree & Linearity](file:///c:/Project/Learning_with_ai/MAT/MAT%201032%20Differential%20Equations/Notes_Organized/01_Introduction_Order_Degree_Linearity.md)

**🔍 සුපිරි විවරණය:**
Degree එක හොයන්න කලින් අනිවාර්යයෙන්ම භාග බලයන් (fractional powers) සහ $\cos, \sin$ වගේ ශ්‍රිත ඇතුලේ අවකලනයන් හිරවෙලා තියෙනවා නම් ඒවා ගැන විශේෂයෙන් සැලකිලිමත් වෙන්න ඕනේ!

**✍️ Step-by-Step Solutions:**
**(i)** $\frac{d^2y}{dx^2} = \left[ 1 + \left(\frac{dy}{dx}\right)^2 \right]^3$
*   ඉහළම අවකලනය $\frac{d^2y}{dx^2}$ වේ. $\implies$ **Order = 2**
*   එයට ඇති බලය 1 වේ. $\implies$ **Degree = 1** (වරහනෙන් පිටත 3 තිබුණත් එය $\frac{dy}{dx}$ ට අදාළ වේ. $\frac{d^2y}{dx^2}$ හි බලය 1 කි).

**(ii)** $y = \frac{\left[ 1 + \left(\frac{dy}{dx}\right)^2 \right]^{3/2}}{\frac{d^2y}{dx^2}}$
*   හරස් ගුණිතය කරමු: $y \frac{d^2y}{dx^2} = \left[ 1 + \left(\frac{dy}{dx}\right)^2 \right]^{3/2}$
*   භාග බලය (3/2) ඉවත් කිරීමට දෙපසම වර්ග කරමු: $y^2 \left(\frac{d^2y}{dx^2}\right)^2 = \left[ 1 + \left(\frac{dy}{dx}\right)^2 \right]^3$
*   ඉහළම අවකලනය $\frac{d^2y}{dx^2}$ $\implies$ **Order = 2**
*   එයට ඇති බලය 2 $\implies$ **Degree = 2**

**(iii)** $\frac{d^4y}{dx^4} + \cos\left(\frac{d^2y}{dx^2}\right) = 5x$
*   ඉහළම අවකලනය $\frac{d^4y}{dx^4}$ $\implies$ **Order = 4**
*   $\cos$ ශ්‍රිතයක් ඇතුළත $\frac{d^2y}{dx^2}$ හිරවී ඇති බැවින්, මෙම සමීකරණය බහුපදයක් (polynomial) ලෙස ප්‍රසාරණය කළ නොහැක.
*   $\implies$ **Degree is Undefined (අර්ථ දක්වා නැත).**

---

### Q1 (b) Autonomous Equations & Stability
> **Question:** Find the critical points of $\frac{dx}{dt} = \alpha(x^2 - 5x + 6)$, where $\alpha$ is a non-zero real parameter. Sketch direction fields and discuss stability.

**✍️ Step-by-Step Solution:**
**Step 1: Critical Points (අවධි ලක්ෂ්‍ය)**
$\frac{dx}{dt} = 0 \implies \alpha(x - 2)(x - 3) = 0$.
$\alpha \neq 0$ බැවින්, **$x=2$** සහ **$x=3$** යනු Critical points වේ.

**Step 2: Stability (ස්ථාවරත්වය)**
$\alpha > 0$ සහ $\alpha < 0$ අවස්ථා දෙකම සලකා බැලිය යුතුය.
*   **Case 1: $\alpha > 0$ විට**
    *   $x < 2$: $(x-2)(-), (x-3)(-) \implies \frac{dx}{dt} > 0$ (ඊතල ඉහළට $\to 2$)
    *   $2 < x < 3$: $(x-2)(+), (x-3)(-) \implies \frac{dx}{dt} < 0$ (ඊතල පහළට $\to 2$)
    *   $x > 3$: $(x-2)(+), (x-3)(+) \implies \frac{dx}{dt} > 0$ (ඊතල ඉහළට $\to$ away from 3)
    *   **නිගමනය:** ඊතල $x=2$ දෙසට එන බැවින් **$x=2$ Stable** වේ. ඊතල $x=3$ න් ඉවතට යන බැවින් **$x=3$ Unstable** වේ.
*   **Case 2: $\alpha < 0$ විට**
    *   සෑම ඊතලයකම දිශාව අනිත් පැත්ත හැරේ.
    *   **නිගමනය:** **$x=2$ Unstable** වන අතර **$x=3$ Stable** වේ.

---

### Q1 (c) First Order DEs
**(i) Separable Equation:** $\frac{dy}{dx} = e^{x+y} + x^2 e^y$
*   $e^{x+y} = e^x e^y$ ලෙස ලිවිය හැක.
*   $\frac{dy}{dx} = e^x e^y + x^2 e^y = e^y (e^x + x^2)$ (මෙය Separable වේ).
*   $e^{-y} dy = (e^x + x^2) dx$
*   අනුකලනය: $\int e^{-y} dy = \int (e^x + x^2) dx \implies -e^{-y} = e^x + \frac{x^3}{3} + C$.

**(ii) Exact Equation:** $(x + \sin y)dx + (x\cos y - 2y)dy = 0$
*   $M = x + \sin y \implies \frac{\partial M}{\partial y} = \cos y$
*   $N = x\cos y - 2y \implies \frac{\partial N}{\partial x} = \cos y$
*   දෙකම සමාන බැවින් මෙය **Exact** වේ!
*   $f(x,y) = \int (x + \sin y) dx = \frac{x^2}{2} + x\sin y + g(y)$.
*   $\frac{\partial f}{\partial y} = x\cos y + g'(y) = x\cos y - 2y \implies g'(y) = -2y \implies g(y) = -y^2$.
*   **Final Answer: $\frac{x^2}{2} + x\sin y - y^2 = C$**

**(iii) Linear Equation:** $\frac{dy}{dx} - \frac{3y}{1+x} = (x+1)^4$
*   $P(x) = -\frac{3}{1+x}$.
*   I.F. = $e^{\int \frac{-3}{1+x} dx} = e^{-3 \ln(1+x)} = (1+x)^{-3}$.
*   $y \cdot (1+x)^{-3} = \int (x+1)^4 (1+x)^{-3} dx = \int (x+1) dx$
*   $\frac{y}{(1+x)^3} = \frac{x^2}{2} + x + C$.

---

### Q1 (d) Homogeneous Initial Value Problem
> **Question:** $-y dx + (x + \sqrt{xy})dy = 0 ; y(1)=1$

*   සමීකරණය නැවත ලියමු: $\frac{dy}{dx} = \frac{y}{x + \sqrt{xy}}$.
*   උඩ $y^1$, යට $x^1 + \sqrt{x^1 y^1} = x^1 + x^{1/2}y^{1/2}$ (Total power 1). එබැවින් මෙය **Homogeneous** වේ.
*   $y = vx \implies \frac{dy}{dx} = v + x\frac{dv}{dx}$ ආදේශ කර සුළු කිරීමෙන් පිළිතුර ලබාගත හැක.

---

## 🎯 Question 02 (Orthogonal Trajectories, Undetermined Coefficients & Systems)

### Q2 (a) Orthogonal Trajectories
> **Question:** Find orthogonal trajectories of $\frac{x^2}{16} + \frac{y^2}{\alpha+4} = 1$, where $\alpha$ is a parameter.
> **📖 Theory Link:** [05. Orthogonal Trajectories](file:///c:/Project/Learning_with_ai/MAT/MAT%201032%20Differential%20Equations/Notes_Organized/05_Orthogonal_Trajectories.md)

**✍️ Step-by-Step Solution:**
**Step 1: අවකලනය කර පරාමිතිය ඉවත් කිරීම ($\alpha$)**
$\frac{2x}{16} + \frac{2y}{\alpha+4}\frac{dy}{dx} = 0 \implies \alpha+4 = \frac{-16y \frac{dy}{dx}}{2x} = -\frac{8y y'}{x}$.
මුල් සමීකරණයට ආදේශ කිරීමෙන්:
$\frac{x^2}{16} + \frac{y^2}{\left(-\frac{8y y'}{x}\right)} = 1 \implies \frac{x^2}{16} - \frac{xy}{8y'} = 1$.

**Step 2: ලම්භක අනුක්‍රමණයට මාරු කිරීම**
$y' \to -\frac{1}{y'}$ ලෙස ආදේශ කරන්න.
$\frac{x^2}{16} - \frac{xy}{8(-1/y')} = 1 \implies \frac{x^2}{16} + \frac{xy y'}{8} = 1$.

**Step 3: විසඳීම (Separable DE)**
$\frac{xy y'}{8} = 1 - \frac{x^2}{16} \implies y y' = \frac{8}{x} - \frac{x}{2}$.
$\int y \, dy = \int \left(\frac{8}{x} - \frac{x}{2}\right) dx$
$\frac{y^2}{2} = 8\ln|x| - \frac{x^2}{4} + C$ (මෙයයි ලම්භක පථ පවුල).

---

### Q2 (b) Undetermined Coefficients
> **Question:** Solve $\frac{d^2y}{dx^2} + 4\frac{dy}{dx} + 3y = \sin x + xe^x$
> **📖 Theory Link:** [07. Higher Order Non-Homogeneous DEs](file:///c:/Project/Learning_with_ai/MAT/MAT%201032%20Differential%20Equations/Notes_Organized/07_Higher_Order_Non_Homogeneous_DEs.md)

**✍️ Step-by-Step Solution:**
**Step 1: Complementary Solution ($y_c$)**
$r^2 + 4r + 3 = 0 \implies (r+1)(r+3) = 0 \implies r = -1, -3$.
$y_c = c_1 e^{-x} + c_2 e^{-3x}$.

**Step 2: Particular Solution ($y_p$) අනුමාන කිරීම**
$f(x) = \sin x + x e^x$.
*   $\sin x$ සඳහා අනුමානය: $A \cos x + B \sin x$.
*   $x e^x$ සඳහා අනුමානය: බහුපදය $\times$ ඝාතීය බැවින් $(Cx + E)e^x$.
*   $y_c$ හි ඇති $e^{-x}, e^{-3x}$ සමඟ මෙම අනුමාන ගැටෙන්නේ නැති බැවින් $x$ න් ගුණ කිරීමට අවශ්‍ය නැත (No modifications needed!).
**$y_p = A \cos x + B \sin x + (Cx + E)e^x$**
(මෙය දෙවරක් අවකලනය කර මුල් සමීකරණයට ආදේශ කිරීමෙන් නියතයන් සොයාගත හැක).

---

### Q2 (c) Systems of Simultaneous Linear DEs
> **Question:** Solve $\frac{dx}{dt} + y = e^t$ and $\frac{dy}{dt} - x = e^{-t}$.

**✍️ Step-by-Step Solution:**
$Dx + y = e^t \implies y = e^t - Dx \implies Dy = e^t - D^2x$.
දෙවන සමීකරණයට ආදේශ කරමු:
$(e^t - D^2x) - x = e^{-t} \implies D^2x + x = e^t - e^{-t}$.

$x_c$: $r^2 + 1 = 0 \implies r = \pm i \implies x_c = c_1 \cos t + c_2 \sin t$.
$x_p$: $A e^t + B e^{-t}$ ලෙස ගෙන ආදේශ කිරීමෙන් $A=1/2, B=-1/2$ ලැබේ.
$x(t) = c_1 \cos t + c_2 \sin t + \frac{1}{2}e^t - \frac{1}{2}e^{-t}$.
මෙහි අවකලනය ගෙන $y = e^t - \frac{dx}{dt}$ වෙත ආදේශ කිරීමෙන් $y(t)$ සෙවිය හැක.

---

## 🎯 Question 03 (Singular Points & PDEs)

### Q3 (a) Singular Points Classification
> **Question:** Classify the singular points of $x^2(x^2-1)^2 y'' - x(x-1)y' + 2y = 0$.

**🔍 සුපිරි විවරණය:**
මුලින්ම $y''$ හි සංගුණකය 1 වන පරිදි මුළු සමීකරණයම බෙදන්න. හරය බිංදුව වන ලක්ෂ්‍ය තමයි Singular Points. ඊට පස්සේ ඒවා Regular ද Irregular ද කියලා බලන්න ලිමිට් (Limits) යොදන්න ඕනේ.

**✍️ Step-by-Step Solution:**
$y'' - \frac{x(x-1)}{x^2(x^2-1)^2} y' + \frac{2}{x^2(x^2-1)^2} y = 0$
$y'' - \frac{1}{x(x-1)(x+1)^2} y' + \frac{2}{x^2(x-1)^2(x+1)^2} y = 0$.
Singular Points: **$x=0, x=1, x=-1$**.

*   **$x=0$ සඳහා:** $p(x)$ හි $x$ න් ගුණ කළ විට සහ $q(x)$ හි $x^2$ න් ගුණ කළ විට හරයේ $x$ පද කැපී යයි. එබැවින් $\lim_{x \to 0}$ අගයක් පවතී. $\implies$ **Regular Singular Point**.
*   **$x=1$ සඳහා:** $p(x)$ හි $(x-1)$ න් ගුණ කළ විට සහ $q(x)$ හි $(x-1)^2$ න් ගුණ කළ විට අගයක් පවතී. $\implies$ **Regular Singular Point**.
*   **$x=-1$ සඳහා:** $p(x)$ හි හරයේ $(x+1)^2$ ඇත. එබැවින් $(x+1)$ න් ගුණ කළද හරයේ $(x+1)$ ඉතිරි වන බැවින් $x \to -1$ විට එය අනන්තයට (infinity) යයි. $\implies$ **Irregular Singular Point**.

---

### Q3 (b) Forming a PDE
> **Question:** Obtain PDE by eliminating $a$ and $b$ from $Z = (x^2+a)(y^2+b)$.

**✍️ Step-by-Step Solution:**
$Z_x = \frac{\partial Z}{\partial x} = 2x(y^2+b) \implies (y^2+b) = \frac{Z_x}{2x}$.
$Z_y = \frac{\partial Z}{\partial y} = 2y(x^2+a) \implies (x^2+a) = \frac{Z_y}{2y}$.
මුල් සමීකරණයට ආදේශ කරමු:
$Z = \left(\frac{Z_y}{2y}\right)\left(\frac{Z_x}{2x}\right)$
$4xy Z = Z_x Z_y$ (මෙයයි අදාළ PDE එක).

---

### Q3 (c) Solving Non-Homogeneous PDE
> **Question:** Solve $(D^3 - D'^2)z = \sin(2x+3y)$

**🔍 සුපිරි විවරණය:**
මෙය සුවිශේෂී PDE එකකි. වම්පස ඇත්තේ සමජාතීය (Homogeneous) නොවන ඔපරේටර් එකකි (එකක බලය 3, අනෙකේ බලය 2).

**✍️ Step-by-Step Solution:**
**Particular Integral (PI):**
$PI = \frac{1}{D^3 - D'^2} \sin(2x+3y)$
$\sin(ax+by)$ ආකාරයේ ශ්‍රිතයක් ඇතිවිට ආදේශ කරන්නේ:
$D^2 \to -a^2 = -2^2 = -4$
$D'^2 \to -b^2 = -3^2 = -9$
$D D' \to -ab = -6$.

මෙහි $D^3$ ඇත්තේ $D \cdot D^2$ ලෙසිනි. $D^2$ වෙනුවට $-4$ ආදේශ කරමු.
$PI = \frac{1}{D(-4) - (-9)} \sin(2x+3y) = \frac{1}{9 - 4D} \sin(2x+3y)$
හරයේ ඇති $D$ ඉවත් කිරීමට එහි අනුබද්ධයෙන් (conjugate) ගුණ කරමු:
$PI = \frac{9 + 4D}{(9 - 4D)(9 + 4D)} \sin(2x+3y) = \frac{9 + 4D}{81 - 16D^2} \sin(2x+3y)$
නැවතත් $D^2 \to -4$ ආදේශ කරන්න:
හරය = $81 - 16(-4) = 81 + 64 = 145$.
ලවය = $(9 + 4D)\sin(2x+3y) = 9\sin(2x+3y) + 4 \frac{\partial}{\partial x}(\sin(2x+3y)) = 9\sin(2x+3y) + 8\cos(2x+3y)$.
**$PI = \frac{9\sin(2x+3y) + 8\cos(2x+3y)}{145}$**.

---
**✅ 2022 Past Paper සම්පූර්ණයෙන්ම සාකච්ඡා කර අවසන්!**
