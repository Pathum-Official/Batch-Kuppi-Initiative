# 04. First Order Linear & Bernoulli DEs

> [!NOTE]
> **Background & Prerequisites (අවශ්‍ය මූලික දැනුම)**
> *   $e^{\ln x} = x$ බව මතක තබාගන්න. ඒ වගේම $e^{-\ln x} = e^{\ln x^{-1}} = x^{-1} = \frac{1}{x}$ වේ. (I.F. සුළු කිරීමේදී මෙය අනිවාර්යයෙන්ම ඕනේ වෙනවා).
> *   $\int \frac{1}{x} dx = \ln x$ 

---

## 1. First Order Linear Equations (පළමු පෙළ රේඛීය සමීකරණ)

**"Dummy-Proof" Concept:**
සමීකරණයක් දැක්කම, ඒකෙ $\frac{dy}{dx}$ එක්ක සහ $y$ එක්ක පද ගුණ වෙලා තියෙනවා නම්, හැබැයි $y$ හෝ $y'$ වර්ග වෙලා නැත්නම් ඒක Linear සමීකරණයක්. මේවා හදන්න තියෙන්නේ නියමිත පියවර (Standard Steps) කිහිපයක් විතරයි.

**Standard Form (සම්මත හැඩය):**
$\frac{dy}{dx} + P(x)y = Q(x)$
*(මෙහි $P(x)$ සහ $Q(x)$ කියන්නේ $x$ අඩංගු ඕනෑම පද. හැබැයි $\frac{dy}{dx}$ ළඟ කිසිම දෙයක් ඉන්න බෑ, එයා තනියම ඉන්න ඕනේ!)*

### ✍️ Step-by-Step Worked Example

**Question:** Solve $\frac{dy}{dx} - \frac{2}{x}y = x^2$

*   **Step 1: සමීකරණය Standard Form එකට ගේන්න**
    මේ ගානේ $\frac{dy}{dx}$ ළඟ කවුරුත් නෑ, ඒ නිසා ඒක දැනටමත් Standard Form එකේ තියෙන්නේ.
    මෙතනදී $P(x)$ සහ $Q(x)$ අඳුරගන්න:
    $P(x) = -\frac{2}{x}$ (සෘණ ලකුණත් එක්කම ගන්න!)
    $Q(x) = x^2$

> [!CAUTION]
> **Exam Trap:** ගොඩක් ළමයි $P(x)$ ගනිද්දි ඉස්සරහා තියෙන සෘණ (-) ලකුණ අමතක කරනවා. එතකොට I.F. එක වැරදිලා මුළු ගාණම වැරදියි! අනිවාර්යයෙන්ම ලකුණත් එක්කම ගන්න.

*   **Step 2: Integrating Factor (I.F.) එක සොයන්න**
    **I.F. = $e^{\int P(x) dx}$**
    $\int P(x) dx = \int -\frac{2}{x} dx = -2 \ln x$
    I.F. = $e^{-2 \ln x} = e^{\ln x^{-2}} = x^{-2} = \frac{1}{x^2}$

*   **Step 3: සූත්‍රයට ආදේශ করে කෙලින්ම පිළිතුර ලියන්න**
    සූත්‍රය: **$y \cdot \text{(I.F.)} = \int Q(x) \cdot \text{(I.F.)} \, dx + C$**
    $y \cdot \left(\frac{1}{x^2}\right) = \int x^2 \cdot \left(\frac{1}{x^2}\right) \, dx + C$
    $\frac{y}{x^2} = \int 1 \, dx + C$
    $\frac{y}{x^2} = x + C$
    $y = x^3 + Cx^2$

---

## 2. Bernoulli Equations (බර්නූලි සමීකරණ)

**"Dummy-Proof" Concept:**
Bernoulli කියන්නේ Linear වගේම එකක්. හැබැයි එකම වෙනස තමයි දකුණු පැත්තේ $Q(x)$ ළඟ $y$ ගේ බලයක් ($y^n$) ඉන්නවා. ඒක අයින් කරාම මේකත් අර උඩ කරපු Linear ගාණක්ම තමයි!

**Standard Form:**
$\frac{dy}{dx} + P(x)y = Q(x)y^n$ 

### ✍️ Step-by-Step Worked Example

**Question:** Solve $\frac{dy}{dx} + \frac{1}{x}y = xy^2$

*   **Step 1: දකුණු පස ඇති $y^n$ ගෙන් මුළු සමීකරණයම බෙදන්න**
    මෙතන දකුණු පස තියෙන්නේ $y^2$. ඒකෙන් හැමෝවම බෙදමු.
    $\frac{1}{y^2}\frac{dy}{dx} + \frac{1}{x}\frac{y}{y^2} = x$
    $y^{-2}\frac{dy}{dx} + \frac{1}{x}y^{-1} = x$ --- (Equation 1)
    
*   **Step 2: ආදේශය කිරීම (The Magic Substitution)**
    **$v = y^{1-n}$** ලෙස ආදේශ කරන්න. මෙතන $n=2$ නිසා $v = y^{-1}$.
    දෙපසම $x$ විෂයෙන අවකලනය කරන්න (Chain Rule එකෙන්):
    $\frac{dv}{dx} = -1 \cdot y^{-2} \frac{dy}{dx} \implies y^{-2}\frac{dy}{dx} = -\frac{dv}{dx}$
    
*   **Step 3: Equation 1 ට ආදේශ කර අලුත් Linear සමීකරණයක් හැදීම**
    $-\frac{dv}{dx} + \frac{1}{x}v = x$
    Standard form එකට ගේන්න සෘණ ලකුණෙන් ගුණ කරමු:
    $\frac{dv}{dx} - \frac{1}{x}v = -x$
    *(දැන් මේක $v$ සහ $x$ තියෙන සාමාන්‍ය Linear ගාණක්!)*
    
*   **Step 4: I.F. හොයාගෙන ගාණ සාමාන්‍ය විදිහට හදන්න**
    $P(x) = -\frac{1}{x}$
    I.F. = $e^{\int -\frac{1}{x} dx} = e^{-\ln x} = x^{-1} = \frac{1}{x}$
    
    සූත්‍රය: $v \cdot \text{(I.F.)} = \int Q(x) \cdot \text{(I.F.)} \, dx + C$
    $v \cdot \left(\frac{1}{x}\right) = \int -x \cdot \left(\frac{1}{x}\right) \, dx + C$
    $\frac{v}{x} = \int -1 \, dx + C$
    $\frac{v}{x} = -x + C \implies v = -x^2 + Cx$
    
*   **Step 5: අවසාන පිළිතුර $y$ වලින් ලිවීම**
    අපි ගත්තේ $v = y^{-1} = \frac{1}{y}$. ඒක ආපහු දාන්න.
    $\frac{1}{y} = Cx - x^2 \implies y = \frac{1}{Cx - x^2}$
