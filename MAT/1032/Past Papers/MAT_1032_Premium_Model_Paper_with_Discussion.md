# PREMIUM MODEL PAPER
## MAT 1032 – DIFFERENTIAL EQUATIONS

> [!IMPORTANT]
> **Instructions**
> 1. This paper consists of two parts: **Part A** (Short Questions) and **Part B** (Essay Questions).
> 2. Answer ALL questions in Part A.
> 3. Answer ANY THREE questions from Part B.
> 4. All necessary working and steps must be clearly shown.

---

### PART A: Short Questions

**Question 1**
Determine the order, degree, and linearity of the following differential equation:
$\left( \frac{d^3y}{dx^3} \right)^2 + x \frac{dy}{dx} - y^4 = \sin x$

**Question 2**
Check whether the following differential equation is exact or not. You do not need to solve it.
$(3x^2y + e^y) dx + (x^3 + x e^y - 2y) dy = 0$

**Question 3**
Find the Wronskian $W(y_1, y_2)$ of the functions $y_1 = e^{2x}$ and $y_2 = x e^{2x}$. Are these functions linearly independent on the real line?

**Question 4**
Classify the following second-order partial differential equation (PDE) as hyperbolic, parabolic, or elliptic:
$3 u_{xx} - 4 u_{xy} + u_{yy} + 2 u_x - u_y = 0$

---

### PART B: Essay Questions

**Question 5**
(a) Solve the initial value problem for the first-order linear differential equation:
$\frac{dy}{dx} - \frac{2}{x} y = x^2 \cos x, \quad y(\pi) = 0, \quad x > 0$

(b) Find the orthogonal trajectories of the family of parabolas given by $y = c x^2$, where $c$ is an arbitrary constant. Sketch a representative curve of both families on the same axes.

**Question 6**
(a) Solve the Bernoulli differential equation:
$x \frac{dy}{dx} + y = x^2 y^2, \quad x > 0$

(b) Solve the following second-order non-homogeneous differential equation using the Method of Undetermined Coefficients:
$y'' - 5y' + 6y = 2 e^{4x} + 12x$

**Question 7**
Solve the following system of simultaneous linear differential equations for $x(t)$ and $y(t)$, given that $x(0) = 1$ and $y(0) = 0$:
$\frac{dx}{dt} = 4x - 2y$
$\frac{dy}{dt} = 5x - y$

**Question 8**
Use the Frobenius Method to find the series solution for the following differential equation near the regular singular point $x = 0$:
$2x^2 y'' + x y' + (x^2 - 1) y = 0$
(Find the indicial equation, determine the roots $r_1, r_2$, find the recurrence relation, and write the first three non-zero terms of the solution corresponding to the larger root).

---
---

# 🎓 PREMIUM MODEL PAPER DISCUSSION & ANSWER GUIDE

> [!TIP]
> **To the Student:** මෙහි ඇත්තේ හුදෙක් Answers පමණක් නොවේ. විභාගයේදී **ලකුණු ලබා දෙන ආකාරය (Marking Scheme)**, **ඔබට නිතරම වැරදෙන තැන් (Common Mistakes)** සහ **ගැටලුව පිටුපස ඇති සැබෑ න්‍යාය (Lecturer's Explanation)** ඉතා සරලව සිංහලෙන් මෙහි අන්තර්ගත කර ඇත.

## ✅ PART A: Short Questions

**1. Order, Degree, and Linearity**
- **Order:** 3 (Highest derivative is $\frac{d^3y}{dx^3}$). `[+2 Marks]`
- **Degree:** 2 (The power of the highest derivative is 2). `[+2 Marks]`
- **Linearity:** Non-linear (Because of the square on the 3rd derivative and the $y^4$ term). `[+1 Mark]`
*(පැහැදිලි කිරීම: $y$ හෝ එහි කිසිඳු අවකලනයක් තවත් එකක් සමග ගුණ වී හෝ වර්ග වී ඇත්නම් එය අනිවාර්යයෙන්ම Non-linear වේ).*

**2. Exactness Check**
Let $M(x,y) = 3x^2y + e^y$ and $N(x,y) = x^3 + x e^y - 2y$. `[+1 Mark]`
$\frac{\partial M}{\partial y} = 3x^2 + e^y$ `[+2 Marks]`
$\frac{\partial N}{\partial x} = 3x^2 + e^y$ `[+2 Marks]`
Since $\frac{\partial M}{\partial y} = \frac{\partial N}{\partial x}$, the differential equation is **Exact**. `[+1 Mark]`
*(පැහැදිලි කිරීම: M අවකලනය කරන්නේ y විෂයෙනි. එහිදී x යනු නියතයකි. N අවකලනය කරන්නේ x විෂයෙනි. එය Exact ද යන්න විභාගයේදී නිතරම අසන ප්‍රශ්නයකි).*

**3. The Wronskian**
$W(y_1, y_2) = y_1 y_2' - y_2 y_1'$
$y_1 = e^{2x} \implies y_1' = 2e^{2x}$
$y_2 = x e^{2x} \implies y_2' = e^{2x} + 2x e^{2x}$ `[+2 Marks]`
$W = (e^{2x})(e^{2x} + 2x e^{2x}) - (x e^{2x})(2e^{2x})$
$W = e^{4x} + 2x e^{4x} - 2x e^{4x} = e^{4x}$ `[+2 Marks]`
Since $e^{4x} \neq 0$ for all real $x$, the functions are **linearly independent**. `[+1 Mark]`

**4. PDE Classification**
Standard form coefficients: $A = 3$, $B = -4$, $C = 1$. `[+2 Marks]`
Calculate Discriminant $\Delta = B^2 - 4AC$:
$\Delta = (-4)^2 - 4(3)(1) = 16 - 12 = 4$. `[+2 Marks]`
Since $\Delta > 0$, the PDE is **Hyperbolic**. `[+1 Mark]`
*(පැහැදිලි කිරීම: මතක තබාගන්න, $B^2 - 4AC$ ධන නම් Hyperbolic, බිංදුව නම් Parabolic, ඍණ නම් Elliptic වේ).*

---

## ✅ PART B: Essay Questions

### Question 5
**(a) First-Order Linear DE**
$y' - \frac{2}{x} y = x^2 \cos x$
This is in standard form $y' + P(x)y = Q(x)$, where $P(x) = -\frac{2}{x}$ and $Q(x) = x^2 \cos x$. `[+1 Mark]`
Integrating Factor (I.F.):
$I.F. = e^{\int -\frac{2}{x} dx} = e^{-2 \ln x} = x^{-2} = \frac{1}{x^2}$. `[+3 Marks]`
*(Common Mistake: $P(x)$ හි ඇති සෘණ ලකුණ (-) බොහෝ ළමයින්ට අමතක වේ).*

Multiply both sides by I.F.:
$\frac{d}{dx} \left( y \cdot \frac{1}{x^2} \right) = (x^2 \cos x) \cdot \frac{1}{x^2} = \cos x$ `[+2 Marks]`
Integrate both sides:
$y x^{-2} = \sin x + C$ `[+2 Marks]`
$y(x) = x^2 \sin x + C x^2$ `[+1 Mark]`

Apply Initial Condition $y(\pi) = 0$:
$0 = \pi^2 \sin(\pi) + C \pi^2 \implies 0 = 0 + C\pi^2 \implies C = 0$. `[+2 Marks]`
Final Solution: $y(x) = x^2 \sin x$. `[+1 Mark]`

**(b) Orthogonal Trajectories**
Family of curves: $y = c x^2$.
Differentiate with respect to $x$: $\frac{dy}{dx} = 2cx$. `[+1 Mark]`
Eliminate $c$: From original, $c = \frac{y}{x^2}$.
So, $\frac{dy}{dx} = 2\left(\frac{y}{x^2}\right)x = \frac{2y}{x}$. `[+2 Marks]`
*(පැහැදිලි කිරීම: අනිවාර්යයෙන්ම $c$ ඉවත් කළ යුතුය! $c$ සහිතව ඊළඟ පියවරට ගියොත් ලකුණු නොලැබේ).*

Slope of orthogonal trajectories is $-\frac{dx}{dy}$:
$-\frac{dx}{dy} = \frac{2y}{x} \implies x \, dx = -2y \, dy$. `[+2 Marks]`
Integrate both sides:
$\int x \, dx = \int -2y \, dy$
$\frac{x^2}{2} = -y^2 + k$ `[+2 Marks]`
$\frac{x^2}{2} + y^2 = k$ (This is a family of ellipses). `[+2 Marks]`
*(Sketch: Draw parabolas opening upwards/downwards, and ellipses centered at the origin intersecting them at 90 degrees).* `[+3 Marks]`

---

### Question 6
**(a) Bernoulli DE**
$x y' + y = x^2 y^2 \implies y' + \frac{1}{x} y = x y^2$. (Standard Bernoulli form with $n=2$). `[+1 Mark]`
Divide by $y^2$: $y^{-2}y' + \frac{1}{x}y^{-1} = x$. `[+1 Mark]`
Let $v = y^{1-2} = y^{-1}$. Then $v' = -y^{-2}y' \implies y^{-2}y' = -v'$. `[+2 Marks]`
Substitute into DE:
$-v' + \frac{1}{x}v = x \implies v' - \frac{1}{x}v = -x$. `[+2 Marks]`
*(මෙය දැන් සාමාන්‍ය First-order Linear සමීකරණයකි).*
I.F. = $e^{\int -1/x \, dx} = x^{-1} = \frac{1}{x}$. `[+2 Marks]`
$\frac{d}{dx}(v \cdot \frac{1}{x}) = -x \cdot \frac{1}{x} = -1$
$v \cdot \frac{1}{x} = -x + C \implies v = -x^2 + Cx$. `[+2 Marks]`
Since $v = \frac{1}{y}$, final answer: $\frac{1}{y} = -x^2 + Cx \implies y = \frac{1}{Cx - x^2}$. `[+2 Marks]`

**(b) Undetermined Coefficients**
$y'' - 5y' + 6y = 2 e^{4x} + 12x$
**Step 1: Complementary Solution ($y_c$)**
Auxiliary eq: $r^2 - 5r + 6 = 0 \implies (r-2)(r-3) = 0 \implies r = 2, 3$. `[+2 Marks]`
$y_c = C_1 e^{2x} + C_2 e^{3x}$. `[+1 Mark]`

**Step 2: Particular Solution ($y_p$)**
Let $y_p = A e^{4x} + (Bx + C)$. `[+2 Marks]`
*(Note: $e^{4x}$ is not in $y_c$, so no need to multiply by $x$).*
$y_p' = 4A e^{4x} + B$
$y_p'' = 16A e^{4x}$ `[+2 Marks]`
Substitute into DE:
$(16A e^{4x}) - 5(4A e^{4x} + B) + 6(A e^{4x} + Bx + C) = 2 e^{4x} + 12x$
$e^{4x}(16A - 20A + 6A) + x(6B) + (6C - 5B) = 2 e^{4x} + 12x$
$2A e^{4x} + 6B x + (6C - 5B) = 2 e^{4x} + 12x$. `[+2 Marks]`

Compare coefficients:
$2A = 2 \implies A = 1$
$6B = 12 \implies B = 2$
$6C - 5(2) = 0 \implies C = \frac{10}{6} = \frac{5}{3}$. `[+2 Marks]`
So, $y_p = e^{4x} + 2x + \frac{5}{3}$.
General Solution: $y = y_c + y_p = C_1 e^{2x} + C_2 e^{3x} + e^{4x} + 2x + \frac{5}{3}$. `[+2 Marks]`

---

### Question 7
**Systems of Simultaneous Linear DEs**
Using operator $D = \frac{d}{dt}$:
$(D - 4)x + 2y = 0$  --- (1)
$-5x + (D + 1)y = 0$ --- (2) `[+2 Marks]`

To eliminate $y$, multiply (1) by $(D+1)$ and (2) by $2$:
$(D+1)(D-4)x + 2(D+1)y = 0$
$-10x + 2(D+1)y = 0$ `[+2 Marks]`
Subtracting them:
$[(D^2 - 3D - 4) - (-10)] x = 0$
$(D^2 - 3D + 6)x = 0 \implies x'' - 3x' + 6x = 0$. `[+3 Marks]`

Auxiliary eq: $r^2 - 3r + 6 = 0$.
Roots: $r = \frac{3 \pm \sqrt{9 - 24}}{2} = \frac{3 \pm \sqrt{-15}}{2} = \frac{3}{2} \pm i\frac{\sqrt{15}}{2}$. `[+2 Marks]`
So, $x(t) = e^{3t/2} (C_1 \cos(\frac{\sqrt{15}}{2}t) + C_2 \sin(\frac{\sqrt{15}}{2}t))$. `[+2 Marks]`

Now find $y(t)$ using eq (1): $2y = 4x - x'$.
$x' = \frac{3}{2}x + e^{3t/2} (-\frac{\sqrt{15}}{2} C_1 \sin(\frac{\sqrt{15}}{2}t) + \frac{\sqrt{15}}{2} C_2 \cos(\frac{\sqrt{15}}{2}t))$.
$2y = 4x - x' = \frac{5}{2}x - e^{3t/2}(\dots)$. `[+2 Marks]`
(Final expression for $y(t)$ is derived by dividing by 2).

Apply initial conditions $x(0) = 1, y(0) = 0$:
$x(0) = e^0 (C_1(1) + C_2(0)) = C_1 = 1$. `[+2 Marks]`
$2y(0) = \frac{5}{2}(1) - \frac{\sqrt{15}}{2} C_2 = 0 \implies C_2 = \frac{5}{\sqrt{15}} = \frac{\sqrt{15}}{3}$. `[+2 Marks]`
*(පැහැදිලි කිරීම: විචල්‍යයන් ඉවත් කිරීමේදී (Elimination), $D$ Operator එක හරියටම සාමාන්‍ය වීජීය පදයක් (Algebraic term) වගේ සලකා ගණනය කළ හැක).*

---

### Question 8
**Frobenius Method**
$2x^2 y'' + x y' + (x^2 - 1) y = 0$
Assume $y = \sum_{n=0}^{\infty} c_n x^{n+r}$.
$y' = \sum_{n=0}^{\infty} (n+r) c_n x^{n+r-1}$
$y'' = \sum_{n=0}^{\infty} (n+r)(n+r-1) c_n x^{n+r-2}$ `[+2 Marks]`

Substitute into DE:
$2x^2 \sum (n+r)(n+r-1) c_n x^{n+r-2} + x \sum (n+r) c_n x^{n+r-1} + (x^2 - 1) \sum c_n x^{n+r} = 0$
$\sum 2(n+r)(n+r-1) c_n x^{n+r} + \sum (n+r) c_n x^{n+r} + \sum c_n x^{n+r+2} - \sum c_n x^{n+r} = 0$. `[+3 Marks]`

Group $x^{n+r}$ terms:
$\sum_{n=0}^{\infty} [2(n+r)(n+r-1) + (n+r) - 1] c_n x^{n+r} + \sum_{n=0}^{\infty} c_n x^{n+r+2} = 0$.
Simplify the bracket:
$2(n+r)^2 - 2(n+r) + (n+r) - 1 = 2(n+r)^2 - (n+r) - 1 = (2(n+r)+1)((n+r)-1)$. `[+2 Marks]`

**Indicial Equation (Lowest power of x, when n=0):**
$(2r+1)(r-1) c_0 = 0$. Since $c_0 \neq 0$, $(2r+1)(r-1) = 0$.
Roots: $r_1 = 1, r_2 = -1/2$. `[+2 Marks]`

For $n=1$ (power $x^{r+1}$):
$(2(r+1)+1)(r+1-1) c_1 = 0 \implies (2r+3)r c_1 = 0$.
For $r=1$, this gives $5(1)c_1 = 0 \implies c_1 = 0$. `[+1 Mark]`

**Recurrence Relation (Shift index of the second sum $n \to n-2$):**
For power $x^{n+r}$ ($n \ge 2$):
$(2(n+r)+1)(n+r-1) c_n + c_{n-2} = 0$
$c_n = \frac{-c_{n-2}}{(2(n+r)+1)(n+r-1)}$. `[+3 Marks]`

For $r=1$ (the larger root):
$c_n = \frac{-c_{n-2}}{(2n+3)n}$.
Since $c_1 = 0$, all odd terms $c_3, c_5, \dots = 0$. `[+1 Mark]`
$n=2: c_2 = \frac{-c_0}{(7)(2)} = -\frac{c_0}{14}$. `[+1 Mark]`
$n=4: c_4 = \frac{-c_2}{(11)(4)} = \frac{c_0}{616}$. `[+1 Mark]`

First three non-zero terms for $r=1$:
$y(x) = c_0 x^{1} \left( 1 - \frac{1}{14}x^2 + \frac{1}{616}x^4 - \dots \right)$. `[+2 Marks]`
*(පැහැදිලි කිරීම: Frobenius Method එකේදී Indicial Equation එක ලබාගන්නේ $n=0$ යෙදීමෙන් lowest power එක බිංදුවට සමාන කිරීමෙනි. එයින් $r$ අගයන් ලැබේ).*

---
---
**End of Model Paper & Discussion Guide.**
*Created by the Batch Kuppi Portal AI Teacher.*
