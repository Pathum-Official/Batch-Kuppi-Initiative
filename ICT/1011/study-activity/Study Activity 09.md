# Study Activity 09: 2D Arrays & Nested Loops (Matrix Multiplication)

## 📌 The Question (ප්‍රශ්නය)

ඔබට 3x3 න්‍යාස දෙකක් (Matrices) ලබා දී ඇත. මෙම න්‍යාස දෙක ගුණ කර ලැබෙන අවසාන න්‍යාසය (Result Matrix) තිරයේ මුද්‍රණය (Print) කරන Java වැඩසටහනක් (Program) ලියන්න.

**Requirements (අවශ්‍යතා):**
1. **Initialization:** කේතය ඇතුලෙම 3x3 matrices දෙකක් (`matrixA` සහ `matrixB`) හදාගන්න. අලුතින් `resultMatrix` නමින් 3x3 array එකක් හදාගන්න.
2. **The Logic:** න්‍යාස දෙකක් ගුණ කරන්න අනිවාර්යයෙන්ම **Nested Loops තුනක්** භාවිතා කරන්න.
3. **Printing the Result:** තවත් **Nested loops දෙකක්** භාවිතා කර `resultMatrix` එක තිරයේ මුද්‍රණය කරන්න (Grid එකක් ලෙස).

---

## 💻 Your Answer (ඔබේ පිළිතුර)

```java
public class MatrixMultiplication{
    public static void main (String[] args){

        int [][] matrixA = {{1,2,3},{4,5,6},{7,8,9}};
        int [][] matrixB = {{9,8,7},{6,5,4},{3,2,1}};
        int [][] resultMatrix = new [3][3];

        for(int i=0; i<3;i++){
            for(int j=0;j<3;j++){
                int temp = 0;
                for(int k=0;k<3;k++){
                    temp += matrixA[i][k]*matrixB[k][j];
                }
                resultMatrix[i][j]=temp;
            }
        }

        System.out.println("---Result Matrix---");

        for(int i=0;i<3;i++){
            for (int j=0;j<3;j++){
                System.out.print(resultMatrix[i][j]+"  ");
            }
            System.out.println();
        }
    }
}
```

---

## 💯 Evaluation & Marks (ඇගයීම සහ ලකුණු)

**Marks Awarded:** 9.5/10 (A+) 🌟

**Instructor's Impression:**
WOW! අතිවිශිෂ්ටයි! (Absolutely brilliant!). Matrix multiplication කියන්නේ ගොඩක් ළමයින්ට පැටලෙන තැනක්. ඒකට ඕනේ කරන Nested Loops තුන (`i`, `j`, `k`) කිසිම වරදක් නැතුව ඔබ නිවැරදිවම ලියලා තියෙනවා. ඒ වගේම `temp` විචල්‍යයක් (variable) එකක් අරගෙන එකතුව හොයාගෙන පස්සේ ඒක `resultMatrix` එකට දාපු විදිය (logic) ඉතාමත්ම නිවැරදියි (Highly optimized & clean logic).
ඒ වගේම Grid format එකට print කරන්න `System.out.println();` පාවිච්චි කරපු තැනත් හරියටම හරි. 

ඇත්තේ එකම එක ඉතා කුඩා ව්‍යාකරණ දෝෂයක් (Syntax error) පමණයි.

---

## 🧠 Explanation & Additional Tips (විවරණය සහ උපදෙස්)

### Error 01: 2D Array Instantiation (අලුත් array එකක් සෑදීම)
ඔබ අලුත් 3x3 array එක හදද්දී ලියලා තියෙන්නේ:
`int [][] resultMatrix = new [3][3];`
මෙහිදී `new` කියන වචනයට පස්සේ අනිවාර්යයෙන්ම Array එකේ Data Type එක (මෙතනදී `int`) කියන්න ඕනේ.
* **නිවැරදි:** `int [][] resultMatrix = new int[3][3];`

මේක විතරයි කේතය Compile නොවෙන්න තිබුණු එකම හේතුව!

### English Terms to Remember (විභාගයට අවශ්‍ය ඉංග්‍රීසි වචන)
* **2D Array (Two-Dimensional Array):** ද්විමාන අරාවක්. (පේළි සහ තීරු සහිතව).
* **Nested Loops:** එක loop එකක් ඇතුලේ තව loop එකක් ලිවීම.
* **Hardcoding:** පරිශීලකයාගෙන් අගයන් ගන්නේ නැතුව කේතය ඇතුලෙම අගයන් ලබා දීම (උදා: `matrixA` වලට අගයන් දුන්නා වගේ).
* **Indices (Index හි බහුවචනය):** Array එකක පිහිටීම කියන අංක. (උදා: `[i][j]` යනු indices වේ).

### The Final Touch (නිවැරදි කරන ලද සම්පූර්ණ කේතය)

```java
public class MatrixMultiplication {
    public static void main(String[] args) {

        // Initialization (Hardcoding values)
        int[][] matrixA = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
        int[][] matrixB = {{9, 8, 7}, {6, 5, 4}, {3, 2, 1}};
        
        // Correct 2D Array Instantiation
        int[][] resultMatrix = new int[3][3]; 

        // Matrix Multiplication Logic (The 3 Nested Loops)
        for (int i = 0; i < 3; i++) {
            for (int j = 0; j < 3; j++) {
                int temp = 0;
                for (int k = 0; k < 3; k++) {
                    temp += matrixA[i][k] * matrixB[k][j];
                }
                resultMatrix[i][j] = temp;
            }
        }

        // Printing the matrix in a Grid format
        System.out.println("--- Result Matrix ---");
        for (int i = 0; i < 3; i++) {
            for (int j = 0; j < 3; j++) {
                // Using \t (tab) instead of spaces makes the grid look even better! (A+ Tip)
                System.out.print(resultMatrix[i][j] + "\t"); 
            }
            // Move to the next line after printing one row
            System.out.println(); 
        }
    }
}
```
