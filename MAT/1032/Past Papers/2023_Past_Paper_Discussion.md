# 🎓 MAT 112 2.0 Differential Equations - 2023 Past Paper Discussion

> [!NOTE]
> **Premium Discussion Guide**
> මෙය 2023 September විභාගයේ ප්‍රශ්න පත්‍රය සඳහා සකසන ලද අතිශය සවිස්තරාත්මක විවරණයකි. මෙහි සෑම ප්‍රශ්නයකටම අදාළ තියරි කොටස්, අපගේ `Notes_Organized` ෆෝල්ඩරයේ ඇති ගොනු වලට Link කර ඇත. යම් පියවරක් අපැහැදිලි නම්, අදාළ Link එක මත Click කර තියරි පාඩම නැවත අධ්‍යයනය කරන්න.

---

## 🎯 Question 01 (පළමු පෙළ සමීකරණ සහ මූලික සංකල්ප)

### Q1 (a) Autonomous Equations & Stability
> **Question:** Consider $\frac{dy}{dt} = a(y-1)$. Here $a$ is a non-zero parameter.
> (i) Find the critical points of the above differential equation.
> (ii) Sketch the direction fields and discuss the stability.

**🔍 සුපිරි විවරණය (Premium Discussion):**
මෙය අපේ සිලබස් එකේ මුලින්ම තියෙන Autonomous Equations (ස්වායත්ත සමීකරණ) සම්බන්ධ ප්‍රශ්නයකි. Critical points (අවධි ලක්ෂ්‍ය) කියන්නේ $\frac{dy}{dt} = 0$ වන ලක්ෂ්‍ය වලටයි. (ඒ කියන්නේ කාලයත් එක්ක වෙනස් වෙන්නේ නැති, ස්ථාවරව තියෙන අගයන්). Stability (ස්ථාවරත්වය) රඳා පවතින්නේ $a$ හි ලකුණ (ධන හෝ ඍණ) මතයි.

**✍️ Step-by-Step Solution:**
**(i) Critical Points:**
අවධි ලක්ෂ්‍ය සඳහා, $\frac{dy}{dt} = 0$ විය යුතුය.
$a(y-1) = 0$
$a \neq 0$ බැවින්, අනිවාර්යයෙන්ම $(y-1) = 0$ විය යුතුය.
$\implies \mathbf{y = 1}$ යනු එකම Critical Point එකයි.

**(ii) Direction Fields & Stability (දිශා ක්ෂේත්‍ර සහ ස්ථාවරත්වය):**
මෙම සමීකරණයේ හැසිරීම $a$ හි ලකුණ මත සම්පූර්ණයෙන්ම වෙනස් වේ. ඒ නිසා විභාගයේදී $a>0$ සහ $a<0$ යන අවස්ථා දෙකම සලකා බැලිය යුතුය.

*   **Case 1: $a > 0$ යැයි ගනිමු.**
    $y > 1$ විට, $(y-1) > 0 \implies \frac{dy}{dt} > 0$ (එනම් $y$ හි අගය ඉහළට/ධන දිශාවට ගමන් කරයි).
    $y < 1$ විට, $(y-1) < 0 \implies \frac{dy}{dt} < 0$ (එනම් $y$ හි අගය පහළට/ඍණ දිශාවට ගමන් කරයි).
    *නිගමනය:* ඊතල යන්නේ $y=1$ ලක්ෂ්‍යයෙන් ඉවතටයි. ඒ නිසා මෙය **Unstable (අස්ථාවර)** වේ.

*   **Case 2: $a < 0$ යැයි ගනිමු.**
    $y > 1$ විට, $(y-1) > 0$ නමුත් $a$ ඍණ බැවින් $\frac{dy}{dt} < 0$ (ඊතල පහළට).
    $y < 1$ විට, $(y-1) < 0$ සහ $a$ ඍණ බැවින් $\frac{dy}{dt} > 0$ (ඊතල ඉහළට).
    *නිගමනය:* ඊතල එන්නේ $y=1$ ලක්ෂ්‍යය දෙසටයි. ඒ නිසා මෙය **Stable (ස්ථාවර)** වේ.

> [!TIP]
> **ඉදිරි අනුමාන (Exam Prediction):** මීළඟ විභාගයේදී $\frac{dy}{dt} = y(y-2)$ වැනි වර්ගජ හැඩයේ (Quadratic) එකක් ලැබිය හැක. එවිට Critical Points දෙකක් ($y=0$ සහ $y=2$) එන අතර, එකක් Stable ද අනෙක Unstable ද කියා පරීක්ෂා කිරීමට සිදුවේ.

---

### Q1 (b) Separable Equations & Valid Range
> **Question:** Solve $\frac{dy}{dx} + (\sin x)y^2 = 0, y(\frac{\pi}{2}) = y_0$. Determine the range where the solutions are valid. Here $y_0$ is an arbitrary constant.
> **📖 Theory Link:** [02. Separable & Homogeneous DEs](file:///c:/Project/Learning_with_ai/MAT/MAT%201032%20Differential%20Equations/Notes_Organized/02_Separable_and_Homogeneous_DEs.md)

**🔍 සුපිරි විවරණය:**
මේක බලපු ගමන් පේනවා Separable කියලා (මොකද $x$ සහ $y$ පද ලේසියෙන්ම වෙන් කරන්න පුළුවන්). අමාරුම කෑල්ල තමයි "Valid Range" (වලංගු පරාසය) හොයන එක. ඒ කියන්නේ අපිට ලැබෙන පිළිතුරේ $y$ අගය අනන්තයට (infinity) නොගිහින් තියෙන්න නම් $x$ තිබිය යුතු පරාසයයි. (හරය 0 වීම වැළැක්වීම).

**✍️ Step-by-Step Solution:**
**Step 1: Separate Variables**
$\frac{dy}{dx} = -(\sin x)y^2$
$\frac{1}{y^2} dy = -\sin x \, dx$

**Step 2: Integrate both sides**
$\int y^{-2} dy = -\int \sin x \, dx$
$\frac{y^{-1}}{-1} = -(-\cos x) + C$
$-\frac{1}{y} = \cos x + C$

**Step 3: Apply Initial Condition**
$x = \frac{\pi}{2}$ වන විට $y = y_0$.
$-\frac{1}{y_0} = \cos(\frac{\pi}{2}) + C$
$\cos(\frac{\pi}{2}) = 0$ බැවින්, $\implies C = -\frac{1}{y_0}$

**Step 4: Final Solution**
$-\frac{1}{y} = \cos x - \frac{1}{y_0}$
$-\frac{1}{y} = \frac{y_0 \cos x - 1}{y_0}$
$\mathbf{y(x) = \frac{y_0}{1 - y_0 \cos x}}$  (මෙයයි අවසාන විසඳුම).

**Step 5: Valid Range**
මෙම ශ්‍රිතය අර්ථ දැක්වීමට නම්, එහි හරය 0 නොවිය යුතුය.
එනම්, $1 - y_0 \cos x \neq 0 \implies \cos x \neq \frac{1}{y_0}$.
මෙය වලංගු වීමට නම් $x$ හි අගය $\cos^{-1}(1/y_0)$ වන ලක්ෂ්‍ය අතර තිබිය යුතුය.
($-1 \leq \cos x \leq 1$ බැවින් $|y_0| > 1$ අවස්ථාවද විශේෂයෙන් සැලකිය යුතුය).

---

### Q1 (c)(i) Order and Degree
> **Question:** Find the order and degree of $y = 2\left(\frac{dy}{dx}\right)^2 + 4x\left(\frac{dx}{dy}\right)$.
> **📖 Theory Link:** [01. Introduction: Order, Degree & Linearity](file:///c:/Project/Learning_with_ai/MAT/MAT%201032%20Differential%20Equations/Notes_Organized/01_Introduction_Order_Degree_Linearity.md)

**🔍 සුපිරි විවරණය:**
කෙලින්ම බැලුවොත් මේකේ ඉහළම අවකලනය $\frac{dy}{dx}$ වගේ පේනවා. ඒත් $\frac{dx}{dy}$ කියලා එකකුත් තියෙනවා (ඒ කියන්නේ $\frac{1}{dy/dx}$). Order/Degree හොයන්න කලින් සමීකරණයේ තියෙන භාග අයින් කරන්න ඕනේ!

**✍️ Step-by-Step Solution:**
මුළු සමීකරණයම $\frac{dy}{dx}$ න් ගුණ කරමු:
$y \left(\frac{dy}{dx}\right) = 2\left(\frac{dy}{dx}\right)^3 + 4x$
දැන් බලන්න:
*   ඉහළම අවකලනය කුමක්ද? එය $\frac{dy}{dx}$ (එනම් 1 වැනි අවකලනයයි). $\implies$ **Order = 1**
*   මෙම ඉහළම අවකලනයට ඇති ඉහළම බලය කුමක්ද? එය 3 වේ. $\implies$ **Degree = 3**

> [!CAUTION]
> **Exam Trap:** $\frac{dx}{dy}$ කියන්නේ භාගයක් ($\frac{1}{y'}$) බව අමතක කිරීම නිසා ළමයි ගොඩක් මෙතන Degree එක 2 යැයි වැරදියට ලියනවා.

---

### Q1 (c)(ii) Homogeneous Equations
> **Question:** Show that $x^2 \frac{dy}{dx} = x^2 + 3xy + y^2$ is homogeneous and solve it.
> **📖 Theory Link:** [02. Separable & Homogeneous DEs](file:///c:/Project/Learning_with_ai/MAT/MAT%201032%20Differential%20Equations/Notes_Organized/02_Separable_and_Homogeneous_DEs.md)

**✍️ Step-by-Step Solution:**
**Step 1: Standard form & Show Homogeneity**
$\frac{dy}{dx} = \frac{x^2 + 3xy + y^2}{x^2}$
$f(x,y) = \frac{x^2 + 3xy + y^2}{x^2}$
$f(\lambda x, \lambda y) = \frac{(\lambda x)^2 + 3(\lambda x)(\lambda y) + (\lambda y)^2}{(\lambda x)^2} = \frac{\lambda^2(x^2 + 3xy + y^2)}{\lambda^2(x^2)} = f(x,y)$.
$\lambda^0 f(x,y)$ බැවින් මෙය **Degree 0 හි සමජාතීය (Homogeneous)** වේ.

**Step 2: Substitution (ආදේශය)**
**$y = vx$** ආදේශ කරන්න. එවිට $\frac{dy}{dx} = v + x\frac{dv}{dx}$ වේ.
$v + x\frac{dv}{dx} = \frac{x^2 + 3x(vx) + (vx)^2}{x^2} = \frac{x^2(1 + 3v + v^2)}{x^2} = 1 + 3v + v^2$

**Step 3: Separate Variables & Solve**
$x\frac{dv}{dx} = 1 + 3v + v^2 - v = v^2 + 2v + 1 = (v+1)^2$
$\frac{1}{(v+1)^2} dv = \frac{1}{x} dx$

දෙපසම අනුකලනය කරමු:
$\int (v+1)^{-2} dv = \int \frac{1}{x} dx$
$\frac{(v+1)^{-1}}{-1} = \ln|x| + C \implies -\frac{1}{v+1} = \ln|x| + C$

අවසානයේ $v = \frac{y}{x}$ යොදන්න:
$-\frac{1}{\frac{y}{x}+1} = \ln|x| + C \implies \mathbf{-\frac{x}{y+x} = \ln|x| + C}$

---

### Q1 (d)(i) Exact vs Separable Trap
> **Question:** Solve $(1 + y + yx^2)dx + x(1+x^2)dy = 0$
> **📖 Theory Link:** [02. Separable & Homogeneous DEs](file:///c:/Project/Learning_with_ai/MAT/MAT%201032%20Differential%20Equations/Notes_Organized/02_Separable_and_Homogeneous_DEs.md)

**🔍 සුපිරි විවරණය:**
මේක දැක්කම හැඩය Exact වගේ ($Mdx + Ndy=0$). ඒත් පොඩ්ඩක් සුළු කරලා බැලුවොත් මේක සරලවම Separable Equation එකක්! Exact ක්‍රමයට ගියොත් වැඩේ ගොඩක් දිග වෙනවා.

**✍️ Step-by-Step Solution:**
පළමු වරහනෙන් $y$ පොදු සාධකයක් ලෙස එළියට ගනිමු:
$(1 + y(1+x^2))dx + x(1+x^2)dy = 0$
(Oops! $y$ එළියට ගත්තට 1 වෙනම ඉතුරු වෙනවා. ඒ නිසා මේක Separable නෙමෙයි වගේ. අපි Exactness බලමු!)

Let $M = 1 + y + yx^2$ and $N = x(1+x^2) = x + x^3$.
$\frac{\partial M}{\partial y} = 1 + x^2$
$\frac{\partial N}{\partial x} = 1 + 3x^2$
$\frac{\partial M}{\partial y} \neq \frac{\partial N}{\partial x}$, එබැවින් **Not Exact**. 

අපි Integrating Factor (I.F.) එකක් හොයමු.
$\frac{\frac{\partial M}{\partial y} - \frac{\partial N}{\partial x}}{N} = \frac{(1+x^2) - (1+3x^2)}{x(1+x^2)} = \frac{-2x^2}{x(1+x^2)} = \frac{-2x}{1+x^2}$
මෙය $x$ වල පමණක් ශ්‍රිතයකි ($P(x)$).
I.F. = $e^{\int \frac{-2x}{1+x^2} dx} = e^{-\ln(1+x^2)} = (1+x^2)^{-1} = \mathbf{\frac{1}{1+x^2}}$.

දැන් සමීකරණය I.F. එකෙන් ගුණ කරමු:
$\frac{1 + y(1+x^2)}{1+x^2} dx + \frac{x(1+x^2)}{1+x^2} dy = 0$
$\left(\frac{1}{1+x^2} + y\right) dx + x \, dy = 0$

දැන් මෙය Exact වේ!
$f(x,y) = \int \left(\frac{1}{1+x^2} + y\right) dx + g(y) = \tan^{-1}x + xy + g(y)$.
$\frac{\partial f}{\partial y} = x + g'(y)$. මෙය $N_{new} = x$ ට සමාන කරන්න.
$x + g'(y) = x \implies g'(y) = 0 \implies g(y) = C$.
**Final Answer: $\tan^{-1}x + xy = C$**

---

### Q1 (d)(ii) Bernoulli DE
> **Question:** Solve $\frac{dy}{dx} + \frac{2}{x}y = 2x^2 y^2 \sin x$
> **📖 Theory Link:** [04. First Order Linear & Bernoulli DEs](file:///c:/Project/Learning_with_ai/MAT/MAT%201032%20Differential%20Equations/Notes_Organized/04_First_Order_Linear_and_Bernoulli_DEs.md)

**✍️ Step-by-Step Solution:**
**Step 1: බෙදීම (Divide by $y^2$)**
$y^{-2}\frac{dy}{dx} + \frac{2}{x}y^{-1} = 2x^2 \sin x$

**Step 2: ආදේශය (Substitution)**
$v = y^{-1} \implies \frac{dv}{dx} = -y^{-2}\frac{dy}{dx} \implies y^{-2}\frac{dy}{dx} = -\frac{dv}{dx}$
$-\frac{dv}{dx} + \frac{2}{x}v = 2x^2 \sin x \implies \frac{dv}{dx} - \frac{2}{x}v = -2x^2 \sin x$ (Linear in terms of $v$).

**Step 3: I.F. සෙවීම**
$P(x) = -\frac{2}{x} \implies$ I.F. = $e^{\int -\frac{2}{x} dx} = e^{-2\ln x} = x^{-2} = \frac{1}{x^2}$.

**Step 4: විසඳුම**
$v \cdot (I.F.) = \int Q(x) \cdot (I.F.) \, dx$
$v \cdot \frac{1}{x^2} = \int (-2x^2 \sin x) \left(\frac{1}{x^2}\right) dx$
$\frac{v}{x^2} = \int -2\sin x \, dx = 2\cos x + C$
$v = 2x^2 \cos x + Cx^2$
**Final Answer: $\frac{1}{y} = 2x^2 \cos x + Cx^2$**

---

### Q1 (e) Wronskian and Linear Independence
> **Question:** Using the Wronskian, find linearly independent solutions of the following equation: $\frac{d^2y}{dx^2} - 2\frac{dy}{dx} + y = 0$.
> **📖 Theory Link:** [06. Higher Order Homogeneous DEs](file:///c:/Project/Learning_with_ai/MAT/MAT%201032%20Differential%20Equations/Notes_Organized/06_Higher_Order_Homogeneous_DEs.md)

**🔍 සුපිරි විවරණය:**
පළමුව සමීකරණය විසඳා $y_1$ සහ $y_2$ සොයාගත යුතුය. ඉන්පසු ඒවායේ Wronskian අගය 0 නොවන බව (එනම් $\neq 0$) පෙන්වීමෙන් ඒවා ස්වායත්ත (independent) බව තහවුරු කළ හැක.

**✍️ Step-by-Step Solution:**
**Step 1: Solve the Homogeneous Equation**
$r^2 - 2r + 1 = 0$
$(r - 1)^2 = 0 \implies r = 1, 1$ (Repeated roots).
විසඳුම් දෙක වන්නේ: $y_1 = e^x$ සහ $y_2 = x e^x$.

**Step 2: Calculate the Wronskian**
$W(y_1, y_2) = \begin{vmatrix} e^x & x e^x \\ \frac{d}{dx}(e^x) & \frac{d}{dx}(x e^x) \end{vmatrix} = \begin{vmatrix} e^x & x e^x \\ e^x & e^x + x e^x \end{vmatrix}$
$W = e^x(e^x + x e^x) - (x e^x)(e^x)$
$W = e^{2x} + x e^{2x} - x e^{2x} = e^{2x}$

**Step 3: Conclusion**
$W(x) = e^{2x}$. කුමන $x$ අගයක් සඳහා වුවද $e^{2x} > 0$ වේ. එබැවින් $W \neq 0$.
මේ නිසා $e^x$ සහ $x e^x$ යනු **Linearly Independent** විසඳුම් යුගලයක් වේ!

---

## 🎯 Question 02 (Orthogonal Trajectories & Higher Order DEs)

### Q2 (a) Orthogonal Trajectories
> **Question:** Find the set of orthogonal trajectories of the family of curves $\tan 2y = cx$, where $c$ is a given parameter.
> **📖 Theory Link:** [05. Orthogonal Trajectories](file:///c:/Project/Learning_with_ai/MAT/MAT%201032%20Differential%20Equations/Notes_Organized/05_Orthogonal_Trajectories.md)

**✍️ Step-by-Step Solution:**
**Step 1: අවකලනය කරන්න (Implicit differentiation)**
$x$ විෂයෙන අවකලනය කරමු:
$\frac{d}{dx}(\tan 2y) = \frac{d}{dx}(cx)$
$2\sec^2(2y) \frac{dy}{dx} = c$

**Step 2: $c$ ඉවත් කරන්න (Eliminate c)**
මුල් සමීකරණයෙන් $c = \frac{\tan 2y}{x}$. මෙය ආදේශ කරමු:
$2\sec^2(2y) \frac{dy}{dx} = \frac{\tan 2y}{x}$
$\frac{dy}{dx} = \frac{\tan 2y}{2x \sec^2(2y)}$
$\tan 2y = \frac{\sin 2y}{\cos 2y}$ සහ $\sec^2 2y = \frac{1}{\cos^2 2y}$ බැවින්:
$\frac{dy}{dx} = \frac{\frac{\sin 2y}{\cos 2y}}{2x \frac{1}{\cos^2 2y}} = \frac{\sin 2y \cos 2y}{2x} = \frac{\sin 4y}{4x}$ 
*(මෙහි $\sin 4y = 2\sin 2y \cos 2y$ ත්‍රිකෝණමිතික සම්බන්ධය භාවිතා විය).*

**Step 3: ලම්භක අනුක්‍රමණයට මාරු කිරීම**
$\frac{dy}{dx} \implies -\frac{dx}{dy}$
$-\frac{dx}{dy} = \frac{\sin 4y}{4x} \implies 4x \, dx = -\sin 4y \, dy$

**Step 4: අනුකලනය කරන්න**
$\int 4x \, dx = -\int \sin 4y \, dy$
$2x^2 = -\left(-\frac{\cos 4y}{4}\right) + k$
$2x^2 - \frac{\cos 4y}{4} = k$ (මෙයයි ලම්භක පථ පවුල).

---

### Q2 (b) Non-Homogeneous DE (Undetermined Coefficients)
> **Question:** Solve $(D^2 - 1)y = e^{(x+1)} + 3^x + \cos x$.
> **📖 Theory Link:** [07. Higher Order Non-Homogeneous DEs](file:///c:/Project/Learning_with_ai/MAT/MAT%201032%20Differential%20Equations/Notes_Organized/07_Higher_Order_Non_Homogeneous_DEs.md)

**🔍 සුපිරි විවරණය:**
මෙහි දකුණු පස වෙනස් ජාති තුනක් තියෙනවා: ඝාතීය ($e$), වෙනත් පාදයක් සහිත ඝාතීය ($3^x = e^{x\ln 3}$), සහ ත්‍රිකෝණමිතික ($\cos$). ඒ නිසා $y_p$ අනුමාන කරද්දී කොටස් තුනක් වෙන වෙනම අනුමාන කරන්න ඕනේ.

**✍️ Step-by-Step Solution:**
**Step 1: Complementary Solution ($y_c$)**
$r^2 - 1 = 0 \implies r = \pm 1$
$y_c = c_1 e^x + c_2 e^{-x}$

**Step 2: Particular Solution ($y_p$) අනුමාන කිරීම**
$f(x) = e \cdot e^x + e^{x \ln 3} + \cos x$.
*   $e^x$ සඳහා අනුමානය: $A e^x$. නමුත් $y_c$ හි $e^x$ ඇති බැවින් (Modification Rule) එය **$Ax e^x$** විය යුතුය.
*   $e^{x \ln 3}$ සඳහා අනුමානය: **$B e^{x \ln 3}$** (එනම් $B \cdot 3^x$).
*   $\cos x$ සඳහා අනුමානය: **$C \cos x + E \sin x$**.

$y_p = Ax e^x + B \cdot 3^x + C \cos x + E \sin x$.
*(සුළු කිරීම් දිගු බැවින්, සෑම කොටසක්ම වෙන වෙනම ආදේශ කර A, B, C, E සෙවිය හැක. මෙය විභාගයේදී ඉතා කාලය ගතවන ගණනය කිරීමකි).*

---

### Q2 (c) Systems of Simultaneous Linear DEs
> **Question:** Solve $Dx - y = t^2$ and $9x + Dy = 7t$.
> **📖 Theory Link:** [08. Systems of Simultaneous Linear DEs](file:///c:/Project/Learning_with_ai/MAT/MAT%201032%20Differential%20Equations/Notes_Organized/08_Systems_of_Simultaneous_Linear_DEs.md)

**✍️ Step-by-Step Solution:**
**Step 1: $y$ කපා හැරීම (Elimination)**
Eq 1: $Dx - y = t^2$ $\implies$ මෙයින් $y$ හි අවකලනය $Dy = D(Dx - t^2) = D^2x - 2t$ බව ලැබේ.
Eq 2: $9x + Dy = 7t$. මෙයට $Dy$ ආදේශ කරමු:
$9x + (D^2x - 2t) = 7t$
$D^2x + 9x = 9t \implies x'' + 9x = 9t$

**Step 2: Solve for $x$ (Complementary & Particular)**
$x_c$: $r^2 + 9 = 0 \implies r = \pm 3i \implies x_c = c_1 \cos 3t + c_2 \sin 3t$.
$x_p$: $f(t) = 9t$ බැවින් $x_p = At + B$ ලෙස අනුමාන කරමු.
$x_p' = A, x_p'' = 0$.
$0 + 9(At+B) = 9t \implies 9At + 9B = 9t \implies A=1, B=0 \implies x_p = t$.
එබැවින්, **$x(t) = c_1 \cos 3t + c_2 \sin 3t + t$**.

**Step 3: $y(t)$ සෙවීම**
Eq 1 න් $y = Dx - t^2$.
$Dx = \frac{dx}{dt} = -3c_1 \sin 3t + 3c_2 \cos 3t + 1$.
එබැවින්:
**$y(t) = -3c_1 \sin 3t + 3c_2 \cos 3t + 1 - t^2$**.

---

## 🎯 Question 03 (Frobenius Method & Partial Differential Equations)

### Q3 (a) Frobenius Method (Series Solutions)
> **Question:** Find the linearly independent series solutions $y_1(x)$ and $y_2(x)$ of the differential equation $\frac{d^2y}{dx^2} + \frac{2}{3x}\frac{dy}{dx} + \frac{x}{3}y = 0$ near $x=0$ and form the general solution.
> **📖 Theory Link:** [09. Series Solutions & Frobenius Method](file:///c:/Project/Learning_with_ai/MAT/MAT%201032%20Differential%20Equations/Notes_Organized/09_Series_Solutions_and_Frobenius_Method.md)

**🔍 සුපිරි විවරණය:**
මෙහි හරයේ $x$ ඇති බැවින් $x=0$ යනු Singular Point එකකි. එමනිසා අනිවාර්යයෙන්ම Frobenius Method ($y = \sum c_n x^{n+r}$) භාවිතා කළ යුතුය.

**✍️ Step-by-Step Solution:**
**Step 1: සමීකරණය පහසු කරගැනීම**
මුළු සමීකරණයම $3x$ න් ගුණ කරමු:
$3x y'' + 2y' + x^2 y = 0$

**Step 2: ආදේශ කිරීම**
$y = \sum_{n=0}^{\infty} c_n x^{n+r}$
$y' = \sum_{n=0}^{\infty} c_n (n+r) x^{n+r-1}$
$y'' = \sum_{n=0}^{\infty} c_n (n+r)(n+r-1) x^{n+r-2}$

සමීකරණයට ආදේශ කරමු:
$3x \sum c_n (n+r)(n+r-1) x^{n+r-2} + 2 \sum c_n (n+r) x^{n+r-1} + x^2 \sum c_n x^{n+r} = 0$
$\sum 3c_n (n+r)(n+r-1) x^{n+r-1} + \sum 2c_n (n+r) x^{n+r-1} + \sum c_n x^{n+r+2} = 0$

**Step 3: බලයන් සමාන කිරීම (Shifting Indices)**
පළමු සහ දෙවන පද වල බලය $x^{n+r-1}$. තෙවන පදයේ බලය $x^{n+r+2}$.
පළමු පද දෙක එකට එකතු කළ හැක:
$\sum c_n [3(n+r)(n+r-1) + 2(n+r)] x^{n+r-1} + \sum c_n x^{n+r+2} = 0$
$\sum c_n (n+r)[3n+3r-1] x^{n+r-1} + \sum_{n=0}^{\infty} c_n x^{n+r+2} = 0$

අපි දෙවැනි $\sum$ එකේ බලයත් $x^{n+r-1}$ කරගමු (එනම් $n \to n-3$ ආදේශ කිරීමෙන්):
$\sum c_n (n+r)(3n+3r-1) x^{n+r-1} + \sum_{n=3}^{\infty} c_{n-3} x^{n+r-1} = 0$

**Step 4: Indicial Equation (දර්ශක සමීකරණය)**
අඩුම බලය ලැබෙන්නේ $n=0$ වූ විටය.
$c_0 (r)(3r-1) = 0$
$c_0 \neq 0$ බැවින්, $r(3r-1) = 0 \implies \mathbf{r = 0, \frac{1}{3}}$

**Step 5: Recurrence Relation (ප්‍රත්‍යාවර්ත සම්බන්ධය)**
පොදු පදය $x^{n+r-1}$ හි සංගුණකය බිංදුවට සමාන කරන්න ($n \geq 3$ සඳහා):
$c_n (n+r)(3n+3r-1) + c_{n-3} = 0$
**$c_n = \frac{-c_{n-3}}{(n+r)(3n+3r-1)}$**

*(විභාගයේදී $r=1/3$ සඳහා සහ $r=0$ සඳහා මෙම සූත්‍රයට $n=3,6,9...$ ආදේශ කර $c_3, c_6$ අගයන් සොයාගෙන $y_1$ සහ $y_2$ යන ශ්‍රේණි දෙකම ලිවිය යුතුය).*

---

### Q3 (b) Forming a PDE
> **Question:** Obtain a partial differential equation by eliminating $m$ and $n$ from $z = m e^{-n^2 y} \sin(nx)$.
> **📖 Theory Link:** [10. Introduction to Partial Differential Equations](file:///c:/Project/Learning_with_ai/MAT/MAT%201032%20Differential%20Equations/Notes_Organized/10_Introduction_to_Partial_Differential_Equations.md)

**✍️ Step-by-Step Solution:**
සමීකරණය $z(x,y)$ බැවින් $x$ සහ $y$ වලින් ආංශිකව අවකලනය කරමු.
$z_x = m e^{-n^2 y} \cdot n \cos(nx)$
$z_{xx} = m e^{-n^2 y} \cdot (-n^2 \sin(nx)) = -n^2 \left[ m e^{-n^2 y} \sin(nx) \right] = -n^2 z$

දැන් $y$ න් අවකලනය කරමු:
$z_y = m \left( -n^2 e^{-n^2 y} \right) \sin(nx) = -n^2 \left[ m e^{-n^2 y} \sin(nx) \right] = -n^2 z$

ඉහත දෙකම $-n^2 z$ ට සමාන බැවින්, ඒවා එකිනෙකට සමාන කළ හැක:
**$z_{xx} = z_y$** (මෙය ප්‍රසිද්ධ Heat Equation එකයි!).

---

### Q3 (c) Solving a PDE using D-operators
> **Question:** Given that $D = \frac{\partial}{\partial x}$ and $D' = \frac{\partial}{\partial y}$, solve $D^2(D - 2D')Z = 6x^2y + \sin(x+2y)$.
> **📖 Theory Link:** [10. Introduction to Partial Differential Equations](file:///c:/Project/Learning_with_ai/MAT/MAT%201032%20Differential%20Equations/Notes_Organized/10_Introduction_to_Partial_Differential_Equations.md)

**🔍 සුපිරි විවරණය:**
මෙය ඝන මාත්‍රයේ (3rd order) PDE එකකි. සාමාන්‍ය ODE වල වගේම මෙහිද Complementary Function ($CF$) සහ Particular Integral ($PI$) සෙවිය යුතුය.

**Step 1: Complementary Function (CF)**
$D^2(D - 2D')Z = 0$
*   $D^2$ වලින් හැඟෙන්නේ මූල $m=0, 0$ බවයි. $\implies f_1(y) + x f_2(y)$.
*   $(D - 2D')$ වලින් හැඟෙන්නේ $(D - mD')$ හැඩයයි, එනම් $m=2$. $\implies f_3(y + 2x)$.
**$CF = f_1(y) + x f_2(y) + f_3(y + 2x)$**

**Step 2: Particular Integral (PI)**
මෙය කොටස් දෙකකට වෙන් කරමු:
$PI_1 = \frac{1}{D^2(D-2D')} (6x^2y)$  සහ  $PI_2 = \frac{1}{D^2(D-2D')} \sin(x+2y)$.
*(විභාගයේදී මෙම $PI$ සෙවීම සඳහා Binomial Expansion (ද්විපද ප්‍රසාරණය) සහ $D^2 \to -a^2, DD' \to -ab, D'^2 \to -b^2$ වැනි ආදේශ භාවිතා කළ යුතුය).*

**Final Answer:** $Z(x,y) = CF + PI_1 + PI_2$.

> [!TIP]
> **ඉදිරි අනුමාන (Exam Prediction):** 
> *   $Q3(a)$ හිදී Frobenius වල අනිවාර්යයෙන්ම $x=0$ Regular Singular Point එකක් වෙන ගණනක්ම එනවා. (Bessel's Equation එක වගේ).
> *   $Q3(b)$ වලදී අනිවාර්යයෙන්ම Heat Equation ($u_t = u_{xx}$) හෝ Wave Equation හැදෙන විදිහේ ප්‍රශ්න තමයි අහන්නේ.

---
**✅ 2023 Past Paper සම්පූර්ණයෙන්ම සාකච්ඡා කර අවසන්!**
