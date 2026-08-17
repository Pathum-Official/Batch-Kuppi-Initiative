# 02. Separable & Homogeneous DEs

> [!NOTE]
> **Background & Prerequisites (අවශ්‍ය මූලික දැනුම)**
> මේ පාඩම කරන්න නම් ඔයාට මූලික අනුකලන (Integration) සූත්‍ර මතක තියෙන්න ඕනේ. විශේෂයෙන්ම:
> *   $\int x^n dx = \frac{x^{n+1}}{n+1}$
> *   $\int \frac{1}{x} dx = \ln|x|$
> *   $\int e^x dx = e^x$

---

## 1. Separable Equations (වෙන් කළ හැකි සමීකරණ)

**"Dummy-Proof" Concept:**
සමීකරණයක් දැක්කම, ඒකේ තියෙන $x$ පද සේරම එක පැත්තකටත් ($dx$ එක්ක), $y$ පද සේරම අනිත් පැත්තටත් ($dy$ එක්ක) ලේසියෙන්ම වෙන් කරන්න පුළුවන් නම්, අන්න ඒවට කියනවා Separable Equations කියලා. 

**How to Identify (හඳුනාගන්නා කෙටික්‍රමය):**
සමීකරණයේ පද එකතු වෙලා (+) හෝ අඩු වෙලා (-) නැතුව, ගුණ වෙලා ($\times$) හෝ බෙදිලා ($\div$) විතරක් තියෙනවා නම් බොහෝ දුරට ඒක Separable.
*උදා:* $\frac{dy}{dx} = x^2 y$ (මේක Separable, $x$ සහ $y$ ගුණ වෙලා තියෙන්නේ).

### ✍️ Step-by-Step Worked Example

**Question:** Solve $\frac{dy}{dx} = \frac{x}{y}$

*   **Step 1: විචල්‍යයන් වෙන් කිරීම (Separate Variables)**
    $y$ වම්පසටත්, $dx$ දකුණු පසටත් යවන්න. (හරස් ගුණිතය වගේ)
    $y \, dy = x \, dx$
    
*   **Step 2: දෙපසම අනුකලනය කිරීම (Integrate both sides)**
    $\int y \, dy = \int x \, dx$
    $\frac{y^2}{2} = \frac{x^2}{2} + C$
    
> [!CAUTION]
> **Exam Trap:** අනුකලනය කරපු ගමන් අනිවාර්යයෙන්ම දකුණු පසට $C$ (Integration Constant) දාන්නම ඕනේ! ගොඩක් අයට මේක අමතක වෙනවා. $C$ නැත්නම් උත්තරේ සම්පූර්ණයෙන්ම වැරදියි.

*   **Step 3: සුළු කිරීම (Simplify)**
    මුළු සමීකරණයම 2 න් ගුණ කරමු:
    $y^2 = x^2 + 2C$ 
    (මෙහි $2C$ යන්න තවත් නියතයක් බැවින් එය නිකම්ම $K$ කියලා ලියන්නත් පුළුවන්. $\implies y^2 - x^2 = K$)

---

## 2. Homogeneous Equations (සමජාතීය සමීකරණ)

**"Dummy-Proof" Concept:**
සමහර සමීකරණ තියෙනවා $x$ සහ $y$ වෙන් කරන්න බැරි (උදා: $\frac{dy}{dx} = \frac{x+y}{x}$). අන්න ඒ වගේ වෙලාවට හැම පදයකම $x$ සහ $y$ ගේ බලයන්ගේ එකතුව සමාන නම්, ඒවට අපි කියනවා Homogeneous කියලා.

**How to Identify (හඳුනාගන්නා කෙටික්‍රමය):**
උඩ සහ පහළ තියෙන හැම පදයකම Total Power එක සමානයි!
*උදා:* $\frac{dy}{dx} = \frac{x^2 + y^2}{xy}$ (උඩ පද වල බලය 2 යි. පහළ $x^1 \cdot y^1$ නිසා එකතුව 2 යි. ඒ නිසා මේක Homogeneous).

### ✍️ Step-by-Step Worked Example

**Question:** Solve $\frac{dy}{dx} = \frac{x+y}{x}$

*   **Step 1: Check Homogeneity (සමජාතීය ද බලමු)**
    $x$ ගේ බලය 1යි, $y$ ගේ බලය 1යි. හැම පදයකම බලය 1 නිසා මෙය සමජාතීය වේ.
    
*   **Step 2: ආදේශය කිරීම (The Magic Substitution)**
    **$y = vx$** ලෙස ආදේශ කරන්න.
    මෙය $x$ විෂයෙන අවකලනය කළොත් (Product Rule එකෙන්):
    $\frac{dy}{dx} = v \cdot (1) + x \cdot \frac{dv}{dx} \implies \frac{dy}{dx} = v + x\frac{dv}{dx}$
    
*   **Step 3: මුල් සමීකරණයට ආදේශය දැමීම (Substitute back)**
    $v + x\frac{dv}{dx} = \frac{x + vx}{x}$
    $v + x\frac{dv}{dx} = \frac{x(1 + v)}{x}$
    $v + x\frac{dv}{dx} = 1 + v$
    
*   **Step 4: සුළු කිරීම (දැන් මේක Separable එකක් වෙනවා!)**
    දෙපසම ඇති $v$ කැපී යයි.
    $x\frac{dv}{dx} = 1 \implies dv = \frac{1}{x} dx$
    
*   **Step 5: අනුකලනය කිරීම (Integrate)**
    $\int 1 \, dv = \int \frac{1}{x} \, dx$
    $v = \ln|x| + C$
    
*   **Step 6: අවසාන පිළිතුර $y$ වලින් ලිවීම**
    අපි දන්නවා $y = vx \implies v = \frac{y}{x}$. ඒක ආපහු දාන්න.
    $\frac{y}{x} = \ln|x| + C \implies y = x\ln|x| + Cx$
