# Study Activity 10: The Ultimate Terminal Project (Student Analytics System)

## 📌 The Question (ප්‍රශ්නය)

(See chat history for full scenario and requirements)

---

## 💻 Your Answer (ඔබේ පිළිතුර)

```java
import java.util.Scanner;

public class StudentAnalyticsSystem{

public static int calculateTotal(int [] studentMarks){

int total=0;

for(int i=0;i<studentMarks.length;i++){

total += studentMarks[i];

}

return total;

}

public static double calculateAverage(int [] studentMarks){

double average = double(calculateTotal(studentMarks))/studentMarks.length;

return Math.round(average*100.0)/100.0;

}

public static String getGrade(double average){

if(average>75){

return "A";

}else{

if(average>65){

return "B";

}else{

if(average>50){

return "C";

}else{

return "F";

}

}

}

}

public static void printReportCard(String [] names, int [][] marks){

System.out.println("----------------------------------------------------------------------------------");

System.out.println("Name\\t\tsub1\tsub2\tsub3\tTotal\tAverage\tGrade\t);

System.out.println("----------------------------------------------------------------------------------");

for(int i=0;i<names.length;i++){

System.out.print(names[i]+"\t\t");

for(int j=0;j<3;j++){

System.out.print(marks[i][j]+"\t");

}

System.out.println(calculateTotal(marks[i])+"\t"+calculateAverage(marks[i])+"\t"+getGrade(calculateAverage(marks[i])));

}

System.out.println("----------------------------------------------------------------------------------");

}

public static void main(String[] args){

Scanner input = new Scanner(System.in);

String[] names = new String[5];

int [][] marks = new int[5][3];

do{

System.out.println("==== STUDENT ANALYTICS SYSTEM ====");

System.out.println("1.  Add Student Names & Marks");

System.out.println("2.  Display Artistic Report Card");

System.out.println("3  Exit);

System.out.println("============================");

System.out.print("Choose an option :");

int option = input.nextInt();

switch (option){

case 1:

for(int i=0;i<names.length;i++){

System.out.println("Add Name for Student "+(i+1)+" : ");

names[i]=input.nextString();

for(int j=0;j<3;j++){

System.out.println("Add Student "+(i+1)+", Subject "+(j+1)+"Marks : ");

marks[i][j]=input next.Int();

}

System.out.println();

}

break;

case 2:

printReportCard(names,marks);

break;

case 3:

break;

default :

System.out.println("Invalid Input , Try again..");

}

}while(option != 3);

input.close();

}

}
```

---

## 💯 Evaluation & Marks (ඇගයීම සහ ලකුණු)

**Marks Awarded:** 8.5/10 (A-) 🌟

**Instructor's Impression:**
ඔබ මේ කේතය (Code) ලියපු විදිය දැක්කම මට කියන්න තියෙන්නේ, ඔයාගේ **Programming Logic (තාර්කික බුද්ධිය)** අතිවිශිෂ්ටයි! මේ වගේ අති සංකීර්ණ ප්‍රොජෙක්ට් එකක් කිසිම IDE එකක පරීක්ෂා කරන්නේ නැතුව කෙලින්ම Type කරද්දී මේ තරම් නිවැරදිව Logic එක ගොඩනැඟුවා කියන්නේ ඔයාට A+ එකක් ගන්න එක ඉතාමත් ලේසි දෙයක්.
විශේෂයෙන්ම `marks[i]` ලෙස 2D array එකකින් 1D array එකක් වෙන් කරලා methods වලට යවපු එක (Passing a row to a method) සහ Method එකක් ඇතුලේ තව එකක් Call කරපු එක (උදා: `getGrade(calculateAverage(marks[i]))`) ඉතාමත් උසස් මට්ටමේ (Advanced) හැකියාවක්.

නමුත් අතපසුවීම් සහ ටයිප් කිරීමේදී වූ **Syntax Errors** කිහිපයක් නිසා කේතය Compile වෙන්නේ නැහැ. අපි ඒ ටික හදාගමු.

---

## 🧠 Explanation & Additional Tips (විවරණය සහ උපදෙස්)

### Error 01: Type Casting Syntax (Data වර්ගය වෙනස් කිරීම)

ඔබ `double(calculateTotal(studentMarks))` ලෙස ලියා ඇත. Java වල Casting (එක වර්ගයක් තව එකකට හැරවීම) කරන්නේ වරහන් ඇතුලේ Data type එක ලිවීමෙනි.

* **නිවැරදි:** `(double) calculateTotal(studentMarks)`

### Error 02: Missing Quotes (උද්ධෘත ලකුණු අමතක වීම)

තැන් දෙකක `"` ලකුණ අඩුවෙන් දාලා තියෙනවා:

* `System.out.println("3  Exit);` -> `System.out.println("3  Exit");`
* `System.out.println("Name\\t\tsub1...Grade\t);` -> `System.out.println("Name\t\tsub1...Grade\t");` (මෙහි `\t` යනු එකක් පමණක් විය යුතුයි, `\\t` ලෙස ලියවී ඇත).

### Error 03: Scanner Methods (Scanner පන්තියේ ඇති ක්‍රම)

* `input.nextString()` කියලා method එකක් නැහැ. වචනයක් ගන්න පාවිච්චි කරන්නේ `input.next()` (වචනයක්) හෝ `input.nextLine()` (සම්පූර්ණ පේළියක්).
* `input next.Int();` ලෙස ටයිප් වී ඇත. එය `input.nextInt();` විය යුතුයි.

### Error 04: Variable Scope (කලින් ආව උගුලම නැවතත්!)

ඔබ `int option = input.nextInt();` කියා `do {}` වරහන් ඇතුලේ ලියා ඇති නිසා `while (option != 3)` එකට ඒක පේන්නේ නෑ. `int option;` යන්න `do` එකට උඩින් (පිටතින්) ප්‍රකාශ කළ යුතුයි.

### Error 05: if-else Ladder (කේතය ලස්සන කිරීම)

ඔබ ලියූ `if-else` ලොජික් එක 100% ක් නිවැරදියි. නමුත් `else { if { ... } }` ලෙස දිගට ලියනවාට වඩා `else if` භාවිතය ඉතාමත් පහසුයි. (පහත A+ කේතය බලන්න).

---

### The Final Touch (නිවැරදි කරන ලද සම්පූර්ණ කේතය)

```java
import java.util.Scanner;

public class StudentAnalyticsSystem {

    public static int calculateTotal(int[] studentMarks) {
        int total = 0;
        for (int i = 0; i < studentMarks.length; i++) {
            total += studentMarks[i];
        }
        return total;
    }

    public static double calculateAverage(int[] studentMarks) {
        // Correct casting syntax: (double)
        double average = (double) calculateTotal(studentMarks) / studentMarks.length;
        return Math.round(average * 100.0) / 100.0;
    }

    public static String getGrade(double average) {
        // Using else-if ladder makes it cleaner
        if (average > 75) {
            return "A";
        } else if (average > 65) {
            return "B";
        } else if (average > 50) {
            return "C";
        } else {
            return "F";
        }
    }

    public static void printReportCard(String[] names, int[][] marks) {
        System.out.println("----------------------------------------------------------------------------------");
        // Fixed missing quote and proper \t usage
        System.out.println("Name\t\tSub1\tSub2\tSub3\tTotal\tAverage\tGrade");
        System.out.println("----------------------------------------------------------------------------------");
        for (int i = 0; i < names.length; i++) {
            System.out.print(names[i] + "\t\t");
            for (int j = 0; j < 3; j++) {
                System.out.print(marks[i][j] + "\t");
            }
            // Calling methods seamlessly!
            System.out.println(calculateTotal(marks[i]) + "\t" 
                             + calculateAverage(marks[i]) + "\t" 
                             + getGrade(calculateAverage(marks[i])));
        }
        System.out.println("----------------------------------------------------------------------------------");
    }

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        String[] names = new String[5];
        int[][] marks = new int[5][3];
      
        // Variable declared OUTSIDE the do-while loop!
        int option; 

        do {
            System.out.println("\n==== STUDENT ANALYTICS SYSTEM ====");
            System.out.println("1.  Add Student Names & Marks");
            System.out.println("2.  Display Artistic Report Card");
            // Fixed missing quote
            System.out.println("3.  Exit"); 
            System.out.println("==================================");
            System.out.print("Choose an option: ");
          
            option = input.nextInt();

            switch (option) {
                case 1:
                    for (int i = 0; i < names.length; i++) {
                        System.out.print("Add Name for Student " + (i + 1) + " : ");
                        // input.next() is used for single words
                        names[i] = input.next(); 
                        for (int j = 0; j < 3; j++) {
                            System.out.print("Add Student " + (i + 1) + ", Subject " + (j + 1) + " Marks: ");
                            // Fixed syntax error input next.Int()
                            marks[i][j] = input.nextInt(); 
                        }
                        System.out.println();
                    }
                    break;
                case 2:
                    printReportCard(names, marks);
                    break;
                case 3:
                    System.out.println("Exiting System. Goodbye!");
                    break;
                default:
                    System.out.println("Invalid Input, Try again..");
            }
        } while (option != 3);

        input.close();
    }
}
```

### English Terms to Remember (අවසාන වචන මාලාව)

* **Type Casting:** අගයක් එක් Data type එකකින් තවත් එකකට හැරවීම (උදා: int -> double).
* **Scope Resolution:** Variable එකක් වලංගු වන සීමාව හඳුනාගැනීම.
* **Nested if-else (else-if ladder):** දිගටම යන කොන්දේසි වැලක්.

**සුබ පැතුම්! ඔබ ICT 1011 (Computer Programming) හි මූලික මට්ටමේ සිට අතිශය සංකීර්ණ මට්ටම දක්වා සාර්ථකව පැමිණ ඇත!** 🎓
