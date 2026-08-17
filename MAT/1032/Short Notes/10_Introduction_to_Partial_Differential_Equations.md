# 10. Introduction to Partial Differential Equations (PDEs)

> [!NOTE]
> **Background & Prerequisites (අවශ්‍ය මූලික දැනුම)**
> *   ආංශික අවකලනය (Partial Differentiation) අත්‍යවශ්‍ය වේ.
> *   $u_x$ කියන්නේ $\frac{\partial u}{\partial x}$ (එනම් $x$ විෂයෙන වරක් අවකලනය කිරීම).
> *   $u_{xy}$ කියන්නේ මුලින් $x$ න් කරලා පස්සේ $y$ න් අවකලනය කිරීම.
> *   වර්ගජ සමීකරණයක මූල සෙවීමේදී අගය (Discriminant) $\Delta = B^2 - 4AC$ භාවිතය.

---

## 1. Classification of PDEs (වර්ග කිරීම)

**"Dummy-Proof" Concept:**
මෙතෙක් අපි කළේ Ordinary Differential Equations (ODEs). ඒ කියන්නේ ඒවයේ තිබුණේ එක විචල්‍යයක් ($x$) විතරයි. හැබැයි Partial (PDEs) වල විචල්‍යයන් දෙකක් හෝ කිහිපයක් තියෙනවා (ගොඩක් වෙලාවට $x$ සහ $t$, නැත්නම් $x$ සහ $y$). 

විභාගයේදී බහුලවම ලැබෙන කෙටි ප්‍රශ්නයක් (Short Question) වන්නේ, ලබා දී ඇති PDE එක කුමන වර්ගයේද (Hyperbolic ද, Parabolic ද, එහෙමත් නැත්නම් Elliptic ද) යන්න හඳුනාගැනීමයි. මේක හරියටම වර්ගජ සමීකරණ වල මූල වර්ග කරනවා වගේ වැඩක්.

### How to Identify (හඳුනාගන්නා කෙටික්‍රමය):

**Standard Form එක:**
$A u_{xx} + B u_{xy} + C u_{yy} + D u_x + E u_y + F u = G$

මෙතනදී අපිට අදාළ වෙන්නේ 2 වන මාත්‍රයේ (දෙපාරක් අවකලනය කරපු) පදවල සංගුණක වන **$A, B, C$** පමණි. අනිත් ඒවා ($D, E, F, G$) මොනවා වුණත් අපිට වැඩක් නෑ.

**වර්ග කිරීමේ කොන්දේසි:**
Discriminant (විවේචකය) **$\Delta = B^2 - 4AC$** ගණනය කරන්න.

1.  **$\Delta > 0$ නම් $\implies$ Hyperbolic (අතිපරාවලයික)**
    *   *උදාහරණය - Wave Equation (තරංග සමීකරණය):* $u_{tt} - c^2 u_{xx} = 0$
2.  **$\Delta = 0$ නම් $\implies$ Parabolic (පරාවලයික)**
    *   *උදාහරණය - Heat Equation (තාප සමීකරණය):* $u_t - \alpha^2 u_{xx} = 0$
3.  **$\Delta < 0$ නම් $\implies$ Elliptic (ඉලිප්සීය)**
    *   *උදාහරණය - Laplace's Equation (ලාප්ලාස් සමීකරණය):* $u_{xx} + u_{yy} = 0$

> [!TIP]
> **Trick to Remember (මතක තබා ගැනීමේ කෙටි ක්‍රමය):**
> *   **Hyper**bolic යනු $> 0$ (ධන) වේ. ("Hyper" කියන්නේ වැඩියි කියන අදහසනේ, ඒ නිසා බිංදුවට වඩා වැඩියි).
> *   **Para**bolic යනු $= 0$ වේ.
> *   **Elliptic** යනු $< 0$ (ඍණ) වේ.

### ✍️ Step-by-Step Worked Example

**Question:** Classify the PDE: $3 u_{xx} - 4 u_{xy} + u_{yy} + 2 u_x - 5 u = 0$

*   **Step 1: A, B, C අගයන් සොයාගැනීම**
    මෙතන $u_{xx}$ ළඟ ඉන්නේ $3$ (එනම් $A=3$).
    $u_{xy}$ ළඟ ඉන්නේ $-4$ (එනම් $B=-4$).
    $u_{yy}$ ළඟ ඉන්නේ $1$ (එනම් $C=1$).
    
*   **Step 2: $\Delta = B^2 - 4AC$ ගණනය කිරීම**
    $\Delta = (-4)^2 - 4(3)(1)$
    $\Delta = 16 - 12$
    $\Delta = 4$
    
*   **Step 3: වර්ග කිරීම**
    $\Delta = 4$ යනු 0 ට වඩා විශාල අගයකි ($4 > 0$).
    එබැවින් මෙම සමීකරණය **Hyperbolic (අතිපරාවලයික)** වේ.

> [!CAUTION]
> **Exam Trap:**
> ගොඩක් ළමයි $B$ අගය ගනිද්දි ඍණ ලකුණ ($-$) අමතක කරනවා. හැබැයි කොහොමත් $B^2$ කරද්දී ඒක ධන වෙනවා. ඒත් $A$ හෝ $C$ වල ඍණ ලකුණක් තිබ්බොත් ඒක අනිවාර්යයෙන්ම දාන්න ඕනේ, නැත්නම් $\Delta$ අගය සම්පූර්ණයෙන්ම වෙනස් වෙලා උත්තරේ වරදිනවා. (උදා: $-2 u_{yy}$ තිබ්බොත් $C = -2$ වේ).
