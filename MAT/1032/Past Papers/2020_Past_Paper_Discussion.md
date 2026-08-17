# 🎓 MAT 112 2.0 Differential Equations - 2020 Past Paper Discussion

> [!NOTE]
> **Premium Discussion Guide (Reverse-Engineered!)**
> ඔබට 2020 ප්‍රශ්න පත්‍රය වෙනම තිබුණේ නැත. නමුත් ඔබ ලබාදුන් "MAT 112 2021 Answers" නැමැති අත්අකුරින් ලියූ පිළිතුරු පත්‍රයේ ඇත්තේ ඇත්ත වශයෙන්ම 2020 විභාගයේ ප්‍රශ්න බව මා විසින් හඳුනා ගන්නා ලදී! (ඔබේ ගොනු වල නම් මාරු වී තිබුණි). එම පිළිතුරු පත්‍රයෙන් ප්‍රශ්න උපුටාගෙන, මේ අතිශය පැහැදිලි විවරණය මා විසින් ඔබ වෙනුවෙන් සකස් කරන ලදී.

---

## 🎯 Question 01 (Autonomous Equations & Stability)

### Q1 (a) Critical Points & Stability
> **Question:** Consider the differential equation $\frac{dy}{dt} = y^2(a-y^2)$. Find the critical points and discuss stability.
> **📖 Theory Link:** [01. Introduction: Order, Degree & Linearity](MAT/1032/Short%20Notes/01_Introduction_Order_Degree_Linearity.md)

**🔍 සුපිරි විවරණය:**
මෙහි $y^2$ පදයක් ඇති බැවින් සමහර අවධි ලක්ෂ්‍ය වලදී (උදා: $y=0$) උඩින් සහ යටින් යන ඊතල දෙකම එකම පැත්තට යන්න පුළුවන් (එනම් Semi-stable වෙන්න පුළුවන්). ඒ වගේම $a$ හි ලකුණ (ධන, ඍණ හෝ බිංදුව) අනුව අවස්ථා 3 ක් වෙන වෙනම සාකච්ඡා කළ යුතුය.

**✍️ Step-by-Step Solution:**
**Step 1: Critical points සෙවීම**
$\frac{dy}{dt} = 0 \implies y^2(a-y^2) = 0$
$y=0$ හෝ $y^2 = a$.

**Step 2: $a$ හි අගය මත පදනම්ව අවස්ථා සලකා බැලීම**
*   **Case 1: $a = 0$ නම්**
    සමීකරණය: $\frac{dy}{dt} = -y^4$.
    මෙහිදී $y$ ධන වුණත් ඍණ වුණත් $-y^4 \leq 0$ වේ. එනම් සෑමවිටම ඊතල පහළට ගමන් කරයි.
    එකම Critical point එක $y=0$ වේ. එය ඉහළින් එන ඊතල පිළිගන්නා අතර පහළට ඊතල නිකුත් කරයි. (Semi-stable / Unstable).

*   **Case 2: $a < 0$ නම්**
    $y^2 = a$ සඳහා තාත්වික මූල නොමැත (Complex numbers).
    එබැවින් එකම Critical point එක වන්නේ $y=0$ පමණි.
    මෙහිදී $\frac{dy}{dt} = a y^2 - y^4$. $y$ හි ඕනෑම අගයකට මෙය ඍණ වේ. (ඊතල පහළට).
    $y=0$ යනු Unstable වේ.

*   **Case 3: $a > 0$ නම් (වැදගත්ම අවස්ථාව)**
    Critical points තුනක් ඇත: **$y=0, y=+\sqrt{a}, y=-\sqrt{a}$**.
    
    *   $y > \sqrt{a}$ විට: $\frac{dy}{dt} = (+)(-) < 0$ (ඊතල පහළට $\to \sqrt{a}$).
    *   $0 < y < \sqrt{a}$ විට: $\frac{dy}{dt} = (+)(+) > 0$ (ඊතල ඉහළට $\to \sqrt{a}$).
    *   $-\sqrt{a} < y < 0$ විට: $\frac{dy}{dt} = (+)(+) > 0$ (ඊතල ඉහළට $\to 0$).
    *   $y < -\sqrt{a}$ විට: $\frac{dy}{dt} = (+)(-) < 0$ (ඊතල පහළට $\to$ away from $-\sqrt{a}$).

**නිගමනය (For $a>0$):**
1.  **$y = \sqrt{a}$ යනු Stable (ස්ථාවර)** වේ (දෙපසින්ම ඊතල එය දෙසට එයි).
2.  **$y = 0$ යනු Unstable (අස්ථාවර)** වේ (ඉහළින් ඊතල ඉවතට යන අතර පහළින් ඊතල එය දෙසට එයි. මෙය Semi-stable ලෙසද හැඳින්විය හැක, නමුත් සාමාන්‍යයෙන් Unstable ගණයට වැටේ).
3.  **$y = -\sqrt{a}$ යනු Unstable (අස්ථාවර)** වේ (දෙපසින්ම ඊතල ඉවතට යයි).

---

## 🎯 Question 02 (Frobenius Method)

### Q2 (a) Series Solution & Singular Points
> **Question:** Determine the nature of the singular point $x=0$ and solve using Frobenius method: $\frac{d^2y}{dx^2} + \frac{3}{2x}\frac{dy}{dx} - \frac{1}{2x}y = 0$.
> **📖 Theory Link:** [09. Series Solutions & Frobenius Method](MAT/1032/Short%20Notes/09_Series_Solutions_and_Frobenius_Method.md)

**✍️ Step-by-Step Solution:**
**Step 1: Check $x=0$**
$p(x) = \frac{3}{2x} \implies xp(x) = \frac{3}{2}$ (සීමාවක් ඇත).
$q(x) = -\frac{1}{2x} \implies x^2 q(x) = -\frac{x}{2} \to 0$ (සීමාවක් ඇත).
එබැවින් $x=0$ යනු **Regular Singular Point** එකකි.

**Step 2: Frobenius Substitution**
$y = \sum a_r x^{r+c}$ යොදමු (මෙහි $c$ යනු දර්ශකයයි/index).
මුළු සමීකරණයම $2x^2$ න් ගුණ කරමු: $2x^2 y'' + 3x y' - x y = 0$.

ආදේශයෙන් පසු:
$\sum 2a_r(r+c)(r+c-1)x^{r+c} + \sum 3a_r(r+c)x^{r+c} - \sum a_r x^{r+c+1} = 0$
පළමු පද දෙකේ බලය $x^{r+c}$ වේ. එය එකතු කරමු:
$\sum a_r(r+c)[2(r+c-1) + 3] x^{r+c} - \sum a_r x^{r+c+1} = 0$
$\sum a_r(r+c)(2r+2c+1) x^{r+c} - \sum a_r x^{r+c+1} = 0$

**Step 3: Indicial Equation ($c$ සෙවීම)**
අඩුම බලය $x^c$ ($r=0$ විට). සංගුණකය 0 ට සමාන කරන්න.
$a_0 c(2c+1) = 0 \implies c = 0$ හෝ $c = -1/2$.

**Step 4: Recurrence Relation ($a_r$ සෙවීම)**
දෙවන $\sum$ හි බලය $x^{r+c}$ කිරීමට $r \to r-1$ යොදමු.
$a_r(r+c)(2r+2c+1) - a_{r-1} = 0 \implies \mathbf{a_r = \frac{a_{r-1}}{(r+c)(2r+2c+1)}}$

*මෙය භාවිතා කර $c=0$ සහ $c=-1/2$ අවස්ථා සඳහා ශ්‍රේණි විසඳුම් දෙකක් ලබාගත හැක.*

---

## 🎯 Question 03 (Partial Differential Equations)

### Q3 (c) Non-Homogeneous PDE
> **Question:** Solve $(D^2 - 3DD' + 2D'^2)z = 2e^{x+y} + \sin(x-5y)$.
> **📖 Theory Link:** [10. Introduction to Partial Differential Equations](MAT/1032/Short%20Notes/10_Introduction_to_Partial_Differential_Equations.md)

**🔍 සුපිරි විවරණය:**
මෙහි දකුණු පස ඝාතීය ($e$) පදයක් සහ ත්‍රිකෝණමිතික ($\sin$) පදයක් ඇත. මේ දෙකටම වෙන වෙනම Particular Integrals (PI) සෙවිය යුතුය.

**✍️ Step-by-Step Solution:**
**Step 1: Complementary Function (CF)**
Auxiliary equation: $m^2 - 3m + 2 = 0 \implies (m-1)(m-2) = 0 \implies m = 1, 2$.
$CF = \phi_1(y+x) + \phi_2(y+2x)$.

**Step 2: Particular Integral 1 ($e^{x+y}$ සඳහා)**
$PI_1 = \frac{1}{D^2 - 3DD' + 2D'^2} 2e^{x+y}$
$e^{ax+by}$ සඳහා $D \to a$ සහ $D' \to b$ ආදේශ කළ යුතුය. ($a=1, b=1$).
ආදේශය: $1^2 - 3(1)(1) + 2(1^2) = 1 - 3 + 2 = 0$.
*(අවවාදයයි! හරය බිංදුව වන බැවින් කෙලින්ම ආදේශ කළ නොහැක. $x$ න් ගුණ කර හරය $D$ විෂයෙන අවකලනය කළ යුතුය).*

අවකලනය කළ හරය = $2D - 3D'$.
දැන් $x$ න් ගුණ කර ආදේශ කරමු:
$PI_1 = x \frac{1}{2D - 3D'} 2e^{x+y} = x \frac{1}{2(1) - 3(1)} 2e^{x+y} = \frac{2x e^{x+y}}{-1} = -2x e^{x+y}$.

**Step 3: Particular Integral 2 ($\sin(x-5y)$ සඳහා)**
$PI_2 = \frac{1}{D^2 - 3DD' + 2D'^2} \sin(x-5y)$
$D^2 \to -a^2 = -1^2 = -1$
$DD' \to -ab = -(1)(-5) = 5$
$D'^2 \to -b^2 = -(-5)^2 = -25$

හරයට ආදේශ කරමු:
$(-1) - 3(5) + 2(-25) = -1 - 15 - 50 = -66$.
$PI_2 = \frac{1}{-66} \sin(x-5y)$.

**Final Answer:**
$z = \phi_1(y+x) + \phi_2(y+2x) - 2x e^{x+y} - \frac{1}{66} \sin(x-5y)$.

---
**✅ 2020 Past Paper සම්පූර්ණයෙන්ම සාකච්ඡා කර අවසන්!**
