# 🎓 MAT 112 2.0 Differential Equations - 2021 Past Paper Discussion

> [!NOTE]
> **Premium Discussion Guide**
> මෙය 2021 March විභාගයේ ප්‍රශ්න පත්‍රය සඳහා සකසන ලද අතිශය සවිස්තරාත්මක විවරණයකි. මෙහි සෑම ප්‍රශ්නයකටම අදාළ තියරි කොටස්, අපගේ `Notes_Organized` ෆෝල්ඩරයේ ඇති ගොනු වලට Link කර ඇත. 

---

## 🎯 Question 01 (මූලික සංකල්ප, අවධි ලක්ෂ්‍ය සහ පළමු පෙළ සමීකරණ)

### Q1 (a) Autonomous Equations & Stability
> **Question:** Consider $\frac{dy}{dt} = (y-\alpha)(y-\beta)$. Here $\alpha, \beta$ are positive parameters. Find the critical points and discuss stability.

**🔍 සුපිරි විවරණය:**
අවධි ලක්ෂ්‍ය (Critical Points) සෙවීමේදී $\frac{dy}{dt} = 0$ කර මූල සෙවිය යුතුය. පසුව $\alpha$ සහ $\beta$ අගයන් කුමක්දැයි නොදන්නා බැවින්, $\alpha > \beta$ යැයි උපකල්පනය කර (හෝ $\beta > \alpha$) අගයන් සලකා ඊතල අඳින්න.

**✍️ Step-by-Step Solution:**
**(i) Critical Points:**
$\frac{dy}{dt} = 0 \implies (y-\alpha)(y-\beta) = 0$.
එබැවින් අවධි ලක්ෂ්‍ය වන්නේ **$y = \alpha$** සහ **$y = \beta$** වේ.

**(ii) Direction Fields & Stability:**
උපකල්පනය කරමු: $\alpha > \beta > 0$.
*   **$y > \alpha$ විට:** $(y-\alpha) > 0, (y-\beta) > 0 \implies \frac{dy}{dt} > 0$ (ඊතල ඉහළට)
*   **$\beta < y < \alpha$ විට:** $(y-\alpha) < 0, (y-\beta) > 0 \implies \frac{dy}{dt} < 0$ (ඊතල පහළට, එනම් $\alpha$ ගෙන් ඈතට, $\beta$ දෙසට)
*   **$y < \beta$ විට:** $(y-\alpha) < 0, (y-\beta) < 0 \implies \frac{dy}{dt} > 0$ (ඊතල ඉහළට, එනම් $\beta$ දෙසට)

**නිගමනය:**
ඊතල $y=\beta$ දෙසට එන බැවින් **$y=\beta$ Stable (ස්ථාවර)** වේ.
ඊතල $y=\alpha$ න් ඉවතට යන බැවින් **$y=\alpha$ Unstable (අස්ථාවර)** වේ.

---

### Q1 (b) Solving First Order DEs
> **Question (i):** Solve $y^2 + \left(\frac{dy}{dx}\right)^2 = 1$
> **📖 Theory Link:** [02. Separable & Homogeneous DEs](MAT/1032/Short%20Notes/02_Separable_and_Homogeneous_DEs.md)

**✍️ Step-by-Step Solution:**
$\left(\frac{dy}{dx}\right)^2 = 1 - y^2 \implies \frac{dy}{dx} = \pm\sqrt{1-y^2}$ (මෙය Separable වේ).
$\frac{1}{\sqrt{1-y^2}} dy = \pm dx$
අනුකලනය කරමු: $\int \frac{1}{\sqrt{1-y^2}} dy = \pm\int dx$
**$\sin^{-1}(y) = \pm x + C \implies y = \sin(\pm x + C)$**

> **Question (ii):** Solve $\frac{dy}{dx} = \frac{y}{x} - \frac{x}{y}$

**✍️ Step-by-Step Solution:**
මෙය සරල කරමු: $\frac{dy}{dx} = \frac{y^2 - x^2}{xy}$.
සෑම පදයකම මුළු බලය 2 වන බැවින් මෙය **Homogeneous** වේ.
ආදේශය: $y = vx \implies \frac{dy}{dx} = v + x\frac{dv}{dx}$.
$v + x\frac{dv}{dx} = \frac{v^2x^2 - x^2}{x(vx)} = \frac{x^2(v^2-1)}{x^2 v} = \frac{v^2-1}{v}$
$x\frac{dv}{dx} = \frac{v^2-1}{v} - v = \frac{v^2 - 1 - v^2}{v} = -\frac{1}{v}$
$v \, dv = -\frac{1}{x} dx$ (දැන් Separable).
$\frac{v^2}{2} = -\ln|x| + C \implies \frac{y^2}{2x^2} = -\ln|x| + C \implies \mathbf{y^2 = 2x^2(C - \ln|x|)}$

---

### Q1 (c) Exact Equations
> **Question:** Solve $\frac{dy}{dx} + \frac{e^x y + 2x}{2y + e^x} = 0, \quad y(0)=0$.

**✍️ Step-by-Step Solution:**
හරස් ගුණ කර $Mdx + Ndy = 0$ හැඩයට ගමු:
$(e^x y + 2x)dx + (2y + e^x)dy = 0$.
$M = e^x y + 2x \implies \frac{\partial M}{\partial y} = e^x$.
$N = 2y + e^x \implies \frac{\partial N}{\partial x} = e^x$.
දෙකම සමාන බැවින් මෙය **Exact** වේ!
$f(x,y) = \int M \, dx = \int (e^x y + 2x) dx = e^x y + x^2 + g(y)$.
$\frac{\partial f}{\partial y} = e^x + g'(y) = 2y + e^x \implies g'(y) = 2y \implies g(y) = y^2$.
සාමාන්‍ය විසඳුම: $e^x y + x^2 + y^2 = C$.
**Initial Condition:** $y(0)=0 \implies e^0(0) + 0^2 + 0^2 = C \implies C=0$.
**Final Answer: $e^x y + x^2 + y^2 = 0$.**

---

### Q1 (d) Order and Degree
> **Question:** Find order and degree of $\left[ 1 + \left(\frac{dy}{dx}\right)^2 \right]^2 = 3 \frac{d^3y}{dx^3}$.

**✍️ Step-by-Step Solution:**
*   ඉහළම අවකලනය $\frac{d^3y}{dx^3}$ (3 වැනි අවකලනය) $\implies$ **Order = 3**
*   එයට ඇති ඉහළම බලය 1 වේ. $\implies$ **Degree = 1**
*(වම්පස ඇති 2 වැනි බලය අදාළ වන්නේ පළමු අවකලනයට බැවින්, Degree එකට එය බලපාන්නේ නැත).*

---

### Q1 (e) Integrating Factors (I.F.)
> **Question:** Find integrating factors.
> (i) $x \log x \frac{dy}{dx} + y = 25 \log x$  &  (ii) $x \frac{dy}{dx} + y = y^2 x^2 \ln x$.
> **📖 Theory Link:** [04. First Order Linear & Bernoulli DEs](file:///c:/Project/Learning_with_ai/MAT/MAT%201032%20Differential%20Equations/Notes_Organized/04_First_Order_Linear_and_Bernoulli_DEs.md)

**✍️ Step-by-Step Solution:**
**(i) Linear Equation:**
මුලින්ම $\frac{dy}{dx}$ ළඟින් $x \log x$ ඉවත් කරන්න (සමීකරණය ඊන් බෙදන්න):
$\frac{dy}{dx} + \frac{1}{x \log x}y = \frac{25}{x}$.
මෙහි $P(x) = \frac{1}{x \log x}$.
$I.F. = e^{\int \frac{1}{x \log x} dx}$.
$u = \log x$ ලෙස ගත් විට $du = \frac{1}{x} dx$. එබැවින් $\int \frac{1}{u} du = \ln|u| = \ln(\log x)$.
**$I.F. = e^{\ln(\log x)} = \log x$**.

**(ii) Bernoulli Equation:**
$x$ න් බෙදමු: $\frac{dy}{dx} + \frac{1}{x}y = y^2 x \ln x$.
මෙය $y^2$ වලින් බෙදා විසඳිය යුතු Bernoulli එකකි. $y^{-2}\frac{dy}{dx} + \frac{1}{x}y^{-1} = x \ln x$.
$v = y^{-1}$ ආදේශ කර $v$ සඳහා Linear Equation හැදූ විට $P(x) = -\frac{1}{x}$ වේ.
**$I.F. = e^{\int -\frac{1}{x} dx} = e^{-\ln x} = \mathbf{\frac{1}{x}}$**.

---

### Q1 (f) Wronskian & Initial Value Problem
> **Question:** Using the Wronskian, find two independent solutions of the following IVP: $\frac{d^2y}{dx^2} + y = 0, y(0)=1, y'(0)=-1$.

**🔍 සුපිරි විවරණය:**
*ප්‍රශ්නයේ ඇති වරදක්:* "IVP (Initial Value Problem) එකකට independent solutions දෙකක් හොයන්න" කිවුවම ඒක ව්‍යාකරණානුකූලව වැරදියි. IVP එකකට තියෙන්නේ එකම එක නිශ්චිත විසඳුමයි (Unique solution). මෙහිදී බලාපොරොත්තු වන්නේ සාමාන්‍ය සමීකරණයේ independent solutions ($y_1, y_2$) හොයාගෙන, ඒවා Wronskian එකෙන් තහවුරු කරලා, අන්තිමට ඒක IVP එකට දාලා $c_1, c_2$ නියතයන් හොයන එකයි.

**✍️ Step-by-Step Solution:**
$r^2 + 1 = 0 \implies r = \pm i$.
විසඳුම් දෙක: $y_1 = \cos x$ සහ $y_2 = \sin x$.
$W = \begin{vmatrix} \cos x & \sin x \\ -\sin x & \cos x \end{vmatrix} = \cos^2 x - (-\sin^2 x) = \cos^2 x + \sin^2 x = 1$.
$W = 1 \neq 0$ බැවින් $y_1, y_2$ යනු Independent Solutions වේ.
සාමාන්‍ය විසඳුම: $y = c_1 \cos x + c_2 \sin x$.
$y(0)=1 \implies c_1(1) + c_2(0) = 1 \implies c_1 = 1$.
$y' = -c_1 \sin x + c_2 \cos x \implies y'(0) = -1 \implies -1(0) + c_2(1) = -1 \implies c_2 = -1$.
**Final IVP Solution: $y = \cos x - \sin x$**.

---

## 🎯 Question 02 (Orthogonal Trajectories, Cauchy-Euler & Systems)

### Q2 (a) Orthogonal Trajectories
> **Question:** Find orthogonal trajectories of $y = \frac{1}{a+x}$.

**✍️ Step-by-Step Solution:**
**Step 1: අවකලනය කරන්න (Implicit differentiation)**
$\frac{dy}{dx} = -1(a+x)^{-2} \cdot (1) = -\frac{1}{(a+x)^2}$.
මුල් සමීකරණයෙන් $a+x = \frac{1}{y}$ බව පෙනේ. එය ආදේශ කරන්න:
$\frac{dy}{dx} = -\frac{1}{(1/y)^2} = -y^2$. (දැන් පරාමිතිය $a$ ඉවත්වී ඇත).

**Step 2: ලම්භක අනුක්‍රමණයට මාරු කිරීම**
$\frac{dy}{dx} \implies -\frac{dx}{dy}$
$-\frac{dx}{dy} = -y^2 \implies dx = y^2 dy$.

**Step 3: අනුකලනය කරන්න**
$\int dx = \int y^2 dy \implies \mathbf{x = \frac{y^3}{3} + C}$.

---

### Q2 (b)(i) Undetermined Coefficients
> **Question:** Solve $(D^3 + 25D)y = \sin 5x + e^{5x}$
> **📖 Theory Link:** [07. Higher Order Non-Homogeneous DEs](file:///c:/Project/Learning_with_ai/MAT/MAT%201032%20Differential%20Equations/Notes_Organized/07_Higher_Order_Non_Homogeneous_DEs.md)

**✍️ Step-by-Step Solution:**
**Step 1: Complementary Solution ($y_c$)**
$r^3 + 25r = 0 \implies r(r^2 + 25) = 0 \implies r = 0, \pm 5i$.
$y_c = c_1 e^0 + c_2 \cos 5x + c_3 \sin 5x = c_1 + c_2 \cos 5x + c_3 \sin 5x$.

**Step 2: Particular Solution ($y_p$) අනුමාන කිරීම**
*   $e^{5x}$ සඳහා අනුමානය: $A e^{5x}$. (මෙය $y_c$ සමඟ නොගැටේ).
*   $\sin 5x$ සඳහා අනුමානය: $B \cos 5x + C \sin 5x$. **නමුත්!** මෙය $y_c$ හි ඇති පද වලට සමාන වේ. එබැවින් $x$ න් ගුණ කළ යුතුය (Modification Rule). අලුත් අනුමානය: $x(B \cos 5x + C \sin 5x)$.
**$y_p = A e^{5x} + x(B \cos 5x + C \sin 5x)$**. (මෙය අවකලනය කර ආදේශ කිරීමෙන් නියතයන් ලැබේ).

---

### Q2 (b)(ii) Cauchy-Euler Equation
> **Question:** Solve $x^2 \frac{d^2y}{dx^2} - 3x \frac{dy}{dx} + 4y = 4\ln x$

**🔍 සුපිරි විවරණය:**
අවකලනයේ මාත්‍රාවටම හරියටම සමාන $x$ හි බලයකින් ගුණවී ඇති සමීකරණ (උදා: $x^2 y''$, $x^1 y'$) Cauchy-Euler සමීකරණ නම් වේ. මේවා විසඳීමට **$x = e^t$** (එනම් $t = \ln x$) යන සම්මත ආදේශය යෙදිය යුතුය. එවිට $x \frac{dy}{dx} = Dy$ සහ $x^2 \frac{d^2y}{dx^2} = D(D-1)y$ බවට පත්වේ. (මෙහි $D = \frac{d}{dt}$).

**✍️ Step-by-Step Solution:**
ආදේශය: $x = e^t \implies t = \ln x$.
$[D(D-1) - 3D + 4]y = 4t \implies (D^2 - D - 3D + 4)y = 4t \implies (D^2 - 4D + 4)y = 4t$.

දැන් මෙය සාමාන්‍ය Non-Homogeneous සමීකරණයක් වී ඇත.
$y_c$ සඳහා: $r^2 - 4r + 4 = 0 \implies (r-2)^2 = 0 \implies r=2,2$.
$y_c(t) = c_1 e^{2t} + c_2 t e^{2t}$. $x = e^t$ ආදේශයෙන්: $y_c(x) = c_1 x^2 + c_2 x^2 \ln x$.

$y_p$ සඳහා: $4t$ නිසා $y_p(t) = At + B$ ලෙස අනුමාන කරමු.
$y_p' = A, y_p'' = 0 \implies 0 - 4A + 4(At+B) = 4t \implies 4At + (4B-4A) = 4t$.
සංගුණක සමාන කිරීමෙන්: $4A = 4 \implies A=1$. $4B-4A = 0 \implies B=1$.
$y_p(t) = t + 1 \implies y_p(x) = \ln x + 1$.
**Final Answer: $y = c_1 x^2 + c_2 x^2 \ln x + \ln x + 1$**.

---

### Q2 (c) System of DEs (Showing it's a circle)
> **Question:** $\frac{dx}{dt} = -ay, \frac{dy}{dt} = ax$. Show solution represents a circle.

**✍️ Step-by-Step Solution:**
පළමු සමීකරණය $t$ විෂයෙන අවකලනය කරමු:
$\frac{d^2x}{dt^2} = -a \left(\frac{dy}{dt}\right)$.
දෙවන සමීකරණයෙන් $\frac{dy}{dt} = ax$ යන්න මෙයට ආදේශ කරමු:
$\frac{d^2x}{dt^2} = -a(ax) = -a^2 x \implies x'' + a^2 x = 0$.

මෙය සාමාන්‍ය 2nd order DE එකකි: $r^2 + a^2 = 0 \implies r = \pm ai$.
$x(t) = c_1 \cos(at) + c_2 \sin(at)$.

$y(t)$ සෙවීමට, පළමු සමීකරණයෙන් $y = -\frac{1}{a} \frac{dx}{dt}$ යොදමු:
$\frac{dx}{dt} = -a c_1 \sin(at) + a c_2 \cos(at)$.
$y(t) = -\frac{1}{a} [ -a c_1 \sin(at) + a c_2 \cos(at) ] = c_1 \sin(at) - c_2 \cos(at)$.

**වෘත්තයක් බව පෙන්වීම:**
$x^2 + y^2 = (c_1 \cos(at) + c_2 \sin(at))^2 + (c_1 \sin(at) - c_2 \cos(at))^2$
$x^2 + y^2 = c_1^2 \cos^2(at) + c_2^2 \sin^2(at) + 2c_1c_2\cos\sin + c_1^2 \sin^2(at) + c_2^2 \cos^2(at) - 2c_1c_2\sin\cos$
$x^2 + y^2 = c_1^2(\cos^2 + \sin^2) + c_2^2(\sin^2 + \cos^2) = c_1^2 + c_2^2$.
මෙය $x^2 + y^2 = R^2$ (මෙහි $R^2 = c_1^2 + c_2^2$) ආකාරයේ සමීකරණයක් බැවින්, මෙය **කේන්ද්‍රය (0,0) වූ වෘත්තයක් (Circle)** නිරූපණය කරයි.

---

## 🎯 Question 03 (Singular Points & PDEs)

### Q3 (a)(i) Ordinary vs Singular Points
> **Question:** Determine whether $x=0$ is an ordinary point for $\frac{d^2y}{dx^2} + 5(\ln x)\frac{dy}{dx} = 0$.

**✍️ Step-by-Step Solution:**
$y'$ හි සංගුණකය $p(x) = 5\ln x$ වේ. $x=0$ විට $\ln(0)$ යන්න අර්ථ දැක්වෙන්නේ නැත (එනම් එය අනන්තයට යයි). එබැවින් $p(x)$ යන්න $x=0$ දී analytic නොවේ. $\implies$ **$x=0$ is NOT an ordinary point (It is a singular point)**.

### Q3 (a)(ii) Classify Singular Points
> **Question:** $2x^2 \frac{d^2y}{dx^2} - x \frac{dy}{dx} + (x-5)y = 0$.

**✍️ Step-by-Step Solution:**
සමීකරණය $2x^2$ න් බෙදමු:
$y'' - \frac{1}{2x} y' + \frac{x-5}{2x^2} y = 0$.
Singular point එක **$x=0$** පමණි.
*   $x p(x) = x \left(-\frac{1}{2x}\right) = -\frac{1}{2}$. මෙහි $\lim_{x \to 0}$ අගයක් පවතී.
*   $x^2 q(x) = x^2 \left(\frac{x-5}{2x^2}\right) = \frac{x-5}{2}$. $\lim_{x \to 0} \frac{x-5}{2} = -\frac{5}{2}$. අගයක් පවතී.
දෙකෙහිම අගයන් පවතින බැවින් මෙය **Regular Singular Point** එකකි.

---

### Q3 (b) Forming a PDE
> **Question:** Eliminate $a, b$ from $z = a e^{-b^2 y} \cos(bx)$.

**✍️ Step-by-Step Solution:**
$y$ න් අවකලනය:
$z_y = a(-b^2) e^{-b^2 y} \cos(bx) = -b^2 \left[ a e^{-b^2 y} \cos(bx) \right] = -b^2 z$.

$x$ න් අවකලනය:
$z_x = a e^{-b^2 y} (-b \sin(bx)) = -ab e^{-b^2 y} \sin(bx)$.
නැවත $x$ න් අවකලනය ($z_{xx}$):
$z_{xx} = -ab e^{-b^2 y} (b \cos(bx)) = -b^2 \left[ a e^{-b^2 y} \cos(bx) \right] = -b^2 z$.

$z_{xx}$ සහ $z_y$ දෙකම $-b^2 z$ ට සමාන බැවින්:
**$z_{xx} = z_y$** (මෙය Heat Equation එකයි).

---

### Q3 (c) Solving Homogeneous PDE
> **Question:** Solve $(D^2 - 2DD' + D'^2)Z = 2x^3$.
> **📖 Theory Link:** [10. Introduction to Partial Differential Equations](file:///c:/Project/Learning_with_ai/MAT/MAT%201032%20Differential%20Equations/Notes_Organized/10_Introduction_to_Partial_Differential_Equations.md)

**✍️ Step-by-Step Solution:**
**Step 1: Complementary Function (CF)**
Auxiliary equation ($D \to m, D' \to 1$):
$m^2 - 2m + 1 = 0 \implies (m-1)^2 = 0 \implies m = 1, 1$.
Repeated roots බැවින්: $CF = f_1(y+x) + x f_2(y+x)$.

**Step 2: Particular Integral (PI)**
$PI = \frac{1}{(D-D')^2} 2x^3$
$f(x,y)$ හි $y$ නොමැති බැවින්, $D'$ යනු බිංදුවට සමාන ලෙස සලකා සුළු කිරීම කළ හැක (මන්ද $y$ විෂයෙන අවකලනයන් බිංදුව වේ).
$PI = \frac{1}{D^2} (2x^3)$
මෙයින් කියවෙන්නේ $x$ විෂයෙන දෙවරක් අනුකලනය කළ යුතු බවයි.
1st integration: $\int 2x^3 dx = 2 \frac{x^4}{4} = \frac{x^4}{2}$.
2nd integration: $\int \frac{x^4}{2} dx = \frac{1}{2} \frac{x^5}{5} = \frac{x^5}{10}$.
**Final Answer: $Z(x,y) = f_1(y+x) + x f_2(y+x) + \frac{x^5}{10}$**.

---
**✅ 2021 Past Paper සම්පූර්ණයෙන්ම සාකච්ඡා කර අවසන්!**
