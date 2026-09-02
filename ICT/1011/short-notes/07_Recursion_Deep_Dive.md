# 🚀 ICT 1011 Master Class: 07 - Recursion Deep Dive

> **මෙය ICT 1011 විෂය නිර්දේශයේ හත්වන කොටස සම්පූර්ණයෙන්ම ආවරණය කරන මහාචාර්ය මට්ටමේ (Professor-level) සටහනකි.**
> (Recursion හි මූලික සංකල්ප, Base cases, සහ Call Stack මතකය ක්‍රියා කරන අයුරු මෙහි සාකච්ඡා කෙරේ).

---

## 1. What is Recursion? (පුනරාවර්තනය යනු කුමක්ද?)
Recursion යනු **Method එකක් විසින් එය තුළම නැවත නැවතත් එම Method එකටම කතා කිරීමයි (A method calling itself)**. 
මෙය ලූපයක් (`for` හෝ `while` Loop එකක්) වැනිම කාර්යයක් කරන නමුත්, කේතය වඩාත් සරලව සහ පිරිසිදුව ලිවීමට (Clean code) උපකාරී වේ (විශේෂයෙන්ම ගණිතමය ගැටලු සහ Tree structures විසඳීමේදී - e.g., Factorial, Fibonacci).

### 🧩 Recursion එකක ප්‍රධාන කොටස් 2ක් ඇත:
1. **Base Case (පදනම් අවස්ථාව):** Recursion එක නැවැත්වීමේ කොන්දේසියයි. (මෙය නොමැති වුවහොත් සිදුවන දේ ගැන පහත 'Exam Traps' යටතේ බලන්න).
2. **Recursive Step (පුනරාවර්තන පියවර):** Method එක නැවත තමාටම කතා කරන (Call කරන) ස්ථානය. මෙය සෑම විටම Base Case එක දෙසට කුඩා වෙමින් ගමන් කළ යුතුය.

---

## 2. Classic Example: Factorial සෙවීම
Factorial `n!` යනු 1 සිට `n` දක්වා වූ සියලුම ධන නිඛිලයන්ගේ ගුණිතයයි.
උදා: `5! = 5 * 4 * 3 * 2 * 1 = 120`
*ගණිතමය සමීකරණය: `n! = n * (n-1)!`*

```java
public class RecursionExample {
    
    public static int factorial(int n) {
        // 1. Base Case (නැවැත්වීමේ කොන්දේසිය - 0! හෝ 1! වල අගය සෑම විටම 1 වේ)
        if (n == 0 || n == 1) {
            return 1;
        } 
        // 2. Recursive Step (එය විසින්ම එයට කුඩා අගයක් දී කතා කිරීම)
        else {
            return n * factorial(n - 1); 
        }
    }

    public static void main(String[] args) {
        int result = factorial(5);
        System.out.println("Factorial of 5 is: " + result); // Output: 120
    }
}
```

---

## 3. How the "Call Stack" Memory Works (යටිපෙළ ක්‍රියාවලිය)
මහාචාර්යවරුන් බොහෝ විට Recursion ක්‍රියා කරන අයුරු ගැන විභාගයේදී පරීක්ෂා කරති. කම්පියුටරය ඇතුලේ මෙය ක්‍රියාත්මක වන්නේ **Stack Data Structure** (LIFO - Last In First Out පදනම මත පිඟන් ගොඩක් ගසනවා වැනි) එකක් හරහාය.

ඉහත `factorial(5)` ධාවනය වන විට සිදුවන දේ පියවරෙන් පියවර:

**පහළට බැසීම (Wind Up / Pushing to Stack):**
1. `factorial(5)` ➔ `5 * factorial(4)` (අගය දන්නේ නැත, ඉතිරි ටික හොයන්න පහළට යයි).
2. `factorial(4)` ➔ `4 * factorial(3)`
3. `factorial(3)` ➔ `3 * factorial(2)`
4. `factorial(2)` ➔ `2 * factorial(1)`
5. `factorial(1)` ➔ `1` (මෙහිදී Base Case එක හමුවේ! දැන් ආපසු ඉහළට යෑම ආරම්භ කරයි).

**ඉහළට පැමිණීම (Unwind / Popping from Stack):**
1. `factorial(1)` returns `1`
2. `factorial(2)` computes `2 * 1` = `2`, and returns `2`
3. `factorial(3)` computes `3 * 2` = `6`, and returns `6`
4. `factorial(4)` computes `4 * 6` = `24`, and returns `24`
5. `factorial(5)` computes `5 * 24` = `120`, and returns `120`.

අවසාන පිළිතුර ලෙස `120` මුද්‍රණය වේ.

---

## 4. Exam Traps (විභාගයේදී වරදින තැන්)

> [!CAUTION]
> **Professor's Trap 1: Missing Base Case (StackOverflowError)**
> ඔබ Base Case එකක් ලිව්වේ නැතිනම් හෝ කොන්දේසිය වැරදි නම් (උදා: `if(n == -100)` කියා ලිව්වොත්), මෙම Method එක කිසිදිනක නොනැවතී තමාටම කතා කරයි (Infinite Recursion). 
> මෙහිදී පරිගණකයේ Call Stack memory එක සම්පූර්ණයෙන්ම පිරී ගොස් වැඩසටහන Crash වේ. මෙලෙස එන Error එක **`StackOverflowError`** ලෙස හැඳින්වේ. 
> 
> *(මහාචාර්යවරයෙකු "වැඩසටහන අනන්තයටම ධාවනය වී නතර වීමට හේතුව කුමක්ද?" කියා ඇසුවහොත්, පිළිතුර StackOverflowError යන්නයි).*

> [!CAUTION]
> **Professor's Trap 2: Infinite Loop vs Infinite Recursion**
> Infinite Loop එකකින් (`while(true)`) වැඩසටහන සිරවී (Freeze වී) දිගටම ධාවනය වෙනවා මිසක් ඉබේම Crash වෙන්නේ නැත. නමුත් Infinite Recursion එකකින් ඉතා ඉක්මනින් Memory එක පිරී ගොස් වැඩසටහන ඉබේම Crash (`StackOverflowError`) වේ.

---

## 5. Another Example: Sum of Array Elements (අරාවක අගයන් එකතු කිරීම)
Recursion මගින් Array එකක අගයන් එකතු කරන කේතයක් ද විභාගයට ඒමට ඉඩ ඇත.

```java
// index යනු දැනට එකතු කරමින් යන ස්ථානයයි (මුලින්ම 0 න් පටන් ගනී)
public static int arraySum(int[] arr, int index) {
    // 1. Base Case (අරාවේ අවසානයට පැමිණි විට)
    if (index == arr.length) {
        return 0; // තවත් එකතු කිරීමට අගයන් නැත
    }
    
    // 2. Recursive Step (වත්මන් අගය + ඉතිරි අගයන්ගේ එකතුව)
    return arr[index] + arraySum(arr, index + 1);
}

// Call කරන විදිහ: int total = arraySum(myArray, 0);
```
