# 🏆 ICT 1011 - 2025 Past Paper: Master Discussion (Full Review)

ඔබ ලබා දුන් 2025 Past paper (PDF) එක මා විසින් සම්පූර්ණයෙන්ම කියවා විශ්ලේෂණය කරන ලදී. මෙම පත්‍රය හරියටම අප කලින් කතා කළ **"Professor's Traps"** (උගුල්) වලින් පිරුණු එකකි!

විභාගයට පිළිතුරු ලිවිය යුතු **ඉංග්‍රීසි මාදිලිය (English Answers)** සහ ඒවාට අදාළ **සිංහල පැහැදිලි කිරීම් (Sinhala Explanations)** පහතින් දක්වා ඇත. ඊට අමතරව කථිකාචාර්යවරිය දුන් ඉඟි (Hints) වලට අනුව තවදුරටත් ඇසිය හැකි දේවල් ද මෙහි අන්තර්ගතය.

---

## 📝 Question 01: Pseudocode (25 Marks)

### I. Identify and describe four (04) significant characteristics of pseudocode. (04 marks)

> **සිංහල විවරණය:** Pseudocode වල ප්‍රධාන ලක්ෂණ 4ක් ලියන්න. මේක Theory ප්‍රශ්නයක්.

**✅ Exam Answer:**

1. **Language Independent:** Pseudocode is not tied to any specific programming language's syntax (like Java or C++). It uses plain English.
2. **Readability:** It is highly readable and easy to understand for both programmers and non-programmers.
3. **Simplicity:** It avoids strict grammatical rules or punctuation (like semicolons or curly braces).
4. **Step-by-step logic:** It focuses strictly on the logic and flow of the algorithm rather than implementation details.

### II. Write pseudocode solutions for the following problems:

#### (a) Determine the largest number among three given numbers. (07 marks)

> **සිංහල විවරණය:** ඉලක්කම් 3කින් ලොකුම එක හොයන්න. මෙතන Nested If (if ඇතුලේ තව if) පාවිච්චි කරන්න වෙනවා.

**✅ Exam Answer:**

```text
BEGIN
    DECLARE num1, num2, num3 AS NUMBERS
    PRINT "Enter three numbers:"
    INPUT num1, num2, num3

    IF (num1 >= num2) AND (num1 >= num3) THEN
        PRINT num1, "is the largest"
    ELSE IF (num2 >= num1) AND (num2 >= num3) THEN
        PRINT num2, "is the largest"
    ELSE
        PRINT num3, "is the largest"
    END IF
END
```

> [!TIP]
> **Extra Trap:** සමහර ළමයි `>` විතරක් දානවා (`>=` දාන්නේ නෑ). ඉලක්කම් තුනම සමාන උනොත් (උදා: 5, 5, 5) `>` විතරක් දැම්මොත් කොන්දේසිය fail වෙනවා. ඒ නිසා අනිවාර්යයෙන්ම `>=` දාන්න!

#### (b) Generate and display the multiplication table of a given number. (04 marks)

> **සිංහල විවරණය:** ගුණන චක්‍රය (Multiplication table) හදන්න. මේකට ලූපයක් (Loop) ඕනේ. `FOR` loop එකක් පාවිච්චි කරන එක ලේසියි.

**✅ Exam Answer:**

```text
BEGIN
    DECLARE num, i, result AS NUMBERS
    PRINT "Enter a number:"
    INPUT num

    FOR i = 1 TO 12 DO
        result = num * i
        PRINT num, "x", i, "=", result
    END FOR
END
```

#### (c) Check whether a given number is a prime number. (10 marks)

> **සිංහල විවරණය:** ප්‍රථමක සංඛ්‍යාවක්ද බලන්න. ප්‍රථමක සංඛ්‍යාවක් කියන්නේ 1 න් සහ ඒ සංඛ්‍යාවෙන්ම විතරක් බෙදෙන (ඉතිරියක් නැතුව) ඉලක්කම් වලට. මේකට Modulo `%` operator එක ඕනේ.

**✅ Exam Answer:**

```text
BEGIN
    DECLARE num, i, count AS INTEGER
    PRINT "Enter a number:"
    INPUT num
  
    count = 0 // To count how many numbers can divide 'num' evenly

    IF num <= 1 THEN
        PRINT "Not a prime number"
    ELSE
        FOR i = 1 TO num DO
            IF (num MOD i) == 0 THEN
                count = count + 1
            END IF
        END FOR
      
        IF count == 2 THEN
            PRINT "Prime Number"
        ELSE
            PRINT "Not a Prime Number"
        END IF
    END IF
END
```

---

## 📝 Question 02: Output Tracing & Logic (40 Marks)

### I. Write the output of the following code segments.

> **සිංහල විවරණය:** මෙන්න අපි Master Note එකේ කතා කරපු **"Professor's Traps"** ටික හරියටම ඇවිත් තියෙනවා!

**(a) Integer Division Trap (02 marks)**

```java
int a = 7;
int b = 2;
double result = a / b;
System.out.println(result);
```

**✅ Exam Answer:** `3.0`

> **විවරණය:** `7 / 2` කියන්නේ Integer division එකක්. දශම කැපිලා ගිහින් `3` වෙනවා. ඊට පස්සේ ඒක `double` variable එකකට යන නිසා `3.0` වෙනවා. (3.5 ලිව්වොත් වැරදියි!).

**(b) String Concatenation Trap (03 marks)**

```java
String s1 = "Hello";
String s2 = s1;
s1 = s1.concat(" World");
System.out.println(s1);
System.out.println(s2);
```

**✅ Exam Answer:**
`Hello World`
`Hello`

> **විවරණය:** Java වල Strings "Immutable" (වෙනස් කරන්න බෑ). `concat` කරාම අලුත් වචනයක් හැදිලා ඒක `s1` ට යනවා. නමුත් `s2` තවමත් බලන් ඉන්නේ පරණ "Hello" කියන අගයටයි.

**(c) Pre/Post Increment Trap (04 marks)**

```java
int x = 5;
int y = x++ + ++x;
System.out.println("x = " + x + ", y = " + y);
```

**✅ Exam Answer:** `x = 7, y = 12`

> **විවරණය:**
>
> 1. `x++` (post) : මෙතැනදී x ගේ අගය 5 ම ගන්නවා. හැබැයි ඊළඟ පියවරට යන්න කලින් x = 6 වෙනවා.
> 2. `++x` (pre) : දැන් x=6 යි. pre නිසා මුලින්ම එකක් එකතු වෙලා x = 7 වෙනවා. ඒ 7 ම ගන්නවා.
> 3. `y = 5 + 7 = 12`.
> 4. අවසානයේ x ගේ අගය 7යි.

**(d) Array Reference Trap (02 marks)**

```java
int[] arr1 = {1, 2, 3};
int[] arr2 = arr1;
arr2[1] = 10;
System.out.println(arr1[1]);
```

**✅ Exam Answer:** `10`

> **විවරණය:** Arrays කියන්නේ Reference types. `arr2 = arr1` කිව්වම අලුත් Array එකක් හැදෙන්නේ නෑ! දෙන්නම පෙන්වන්නේ එකම Array එකට (Memory address එකට). ඒ නිසා `arr2` ගෙන් වෙනස් කරත් `arr1` එකෙත් ඒ වෙනසම වෙනවා.

**(e) String Equality Trap (04 marks)**

```java
String s2 = "Java";
String s3 = "Java";
System.out.println(s2 == s3);
System.out.println(s2.equals(s3));
```

**✅ Exam Answer:**
`true`
`true`

> **විවරණය:** අපි `new String("Java")` නොලියා කෙලින්ම `"Java"` කියලා ලිව්වොත්, ඒක යන්නේ "String Pool" එකට. එකම වචනය නිසා `s2` සහ `s3` දෙකම Pool එකේ තියෙන එකම Object එකට point කරනවා. ඒ නිසා Memory address බලන `==` එකත් True, අකුරු ටික සමානද බලන `equals()` එකත් True.

---

### II. Smart Parking Fee Calculator

> **සිංහල විවරණය:** මේක සම්පූර්ණ Java Program එකක්. Method එකක් හදන්න (`Math.ceil` පාවිච්චි කරලා) සහ parameters අරගෙන ගණනය කරන්න අහලා තියෙනවා.

**✅ Exam Answer:**

```java
import java.util.Scanner;

// (a) Define a class with parking charge parameters
public class SmartParkingFeeCalculator {
    // Parameters declared as constants (or static variables)
    static final int GRACE_PERIOD = 15; // in minutes
    static final double SLOT_RATE = 120.0;
    static final double DAILY_CAP = 1500.0;
    static final double OVERALL_CAP = 3500.0;

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        // (b) Read the number of days parked
        System.out.print("Enter number of days parked (within a week): ");
        int days = input.nextInt();

        double totalStayFee = 0;

        // (c) Read minutes for each day
        for (int i = 1; i <= days; i++) {
            System.out.print("Enter minutes parked on day " + i + ": ");
            int minutes = input.nextInt();
          
            // Call the function from part (d)
            double dailyFee = calculateDailyFee(minutes);
            System.out.println("Day " + i + " fee: Rs. " + (int)dailyFee);
          
            totalStayFee += dailyFee;
        }

        // Apply Overall Cap
        if (totalStayFee > OVERALL_CAP) {
            totalStayFee = OVERALL_CAP;
        }

        // (e) Display total fee
        System.out.println("Total parking fee for the stay: Rs. " + (int)totalStayFee);
        input.close();
    }

    // (d) Function to calculate daily parking fee
    public static double calculateDailyFee(int totalMinutes) {
        if (totalMinutes <= GRACE_PERIOD) {
            return 0.0; // Free
        }

        int chargeableMinutes = totalMinutes - GRACE_PERIOD;
      
        // Math.ceil expects a double. So divide by 30.0 (not 30)
        double slots = Math.ceil(chargeableMinutes / 30.0);
        double fee = slots * SLOT_RATE;

        // Apply Daily Cap
        if (fee > DAILY_CAP) {
            fee = DAILY_CAP;
        }
        return fee;
    }
}
```

> [!WARNING]
> **Trap in Part (d):** `Math.ceil` එක ඇතුලේ `chargeableMinutes / 30.0` කියලා අනිවාර්යයෙන්ම `.0` දාන්න ඕනේ! නැත්නම් Integer Division වෙලා දශම කැපිලා යන නිසා `ceil` එකෙන් වැඩක් නැති වෙනවා.

---

## 📝 Question 03: Arrays & Logic (35 Marks)

### I. Two different approaches in Java to store data. (02 marks)

> **සිංහල විවරණය:** Data store කරන ක්‍රම 2ක්. මේකෙන් අදහස් කරන්නේ Variables සහ Arrays වෙන්න පුළුවන් (හෝ Primitive vs Reference).

**✅ Exam Answer:**

1. **Variables (Primitive types):** Used to store a single value (e.g., `int x = 5;`).
2. **Arrays (Data Structures):** Used to store multiple values of the same data type in a single contiguous block of memory (e.g., `int[] marks = new int[5];`).

### II. 2D Array - Factory Production

> **සිංහල විවරණය:** 2D Array එකක් අරගෙන, ඒකේ එකතුව (Total), වැඩිම එකතුව, සහ අඩුම අගය හොයන්න අහලා තියෙන්නේ. මේක හරියටම අපේ Master Note 08 හි තිබෙන විදිහටම එන ප්‍රශ්නයකි!

**✅ Exam Answer:**

```java
import java.util.Scanner;

public class FactoryProduction {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
      
        // 4 weeks, 7 days per week
        int[][] production = new int[4][7];
        int[] weeklyTotal = new int[4];
      
        // Tracking lowest value
        int lowestValue = Integer.MAX_VALUE; // Set to max possible value initially
        int lowestWeek = -1;
        int lowestDay = -1;

        // (a) Accept and store data
        System.out.println("Enter production values for 4 weeks (7 days each):");
        for (int w = 0; w < 4; w++) {
            System.out.print("Week " + (w+1) + ": ");
            for (int d = 0; d < 7; d++) {
                production[w][d] = input.nextInt();
              
                // Keep summing for the weekly total
                weeklyTotal[w] += production[w][d];

                // (d) Logic to find the lowest daily production
                if (production[w][d] < lowestValue) {
                    lowestValue = production[w][d];
                    lowestWeek = w + 1; // +1 for display
                    lowestDay = d + 1;  // +1 for display
                }
            }
        }
      
        System.out.println(); // Blank line

        // (b) Display total production of each week
        int highestTotal = weeklyTotal[0];
        int highestWeek = 1;

        for (int w = 0; w < 4; w++) {
            System.out.println("Total of Week " + (w+1) + ": " + weeklyTotal[w]);
          
            // (c) Logic to find week with highest total production
            if (weeklyTotal[w] > highestTotal) {
                highestTotal = weeklyTotal[w];
                highestWeek = w + 1;
            }
        }

        // Display results for (c) and (d)
        System.out.println("Week with highest total production: Week " + highestWeek + " (" + highestTotal + ")");
        System.out.println("Lowest daily production: " + lowestValue + " (Week " + lowestWeek + ", Day " + lowestDay + ")");
      
        input.close();
    }
}
```

> [!TIP]
> **Extra Knowledge (Lecturer Hint Focus):**
>
> * **Finding the Minimum:** අවම අගය (Lowest) හොයන්න ලූපයක් යද්දී, මුලින්ම ඒ variable එකට ලොකුම අගය (e.g. `Integer.MAX_VALUE` හෝ array එකේ පළවෙනි අගය) දාගන්න ඕනේ. නැත්නම් බිංදුව (`0`) දාලා පටන් ගත්තොත්, හැමදාම බිංදුවම තමයි අඩුම අගය විදිහට එන්නේ!
> * **2D Array Traversing:** 2D array එකක් කිව්ව ගමන් අනිවාර්යයෙන්ම Nested Loops (for ලූප් ඇතුලේ තව for ලූප් එකක්) මතක් වෙන්නම ඕනේ!

---

**🎓 මහාචාර්යවරයෙකුගේ අවසන් පණිවිඩය (Final Word):**
මෙම 2025 පත්‍රය හරහා අපට පැහැදිලි වන්නේ **"කේතය කටපාඩම් කරනවාට වඩා, එය ක්‍රියාත්මක වන ආකාරය (Logic) තේරුම් ගැනීම"** ඉතා වැදගත් බවයි. විශේෂයෙන්ම Question 2 හි ඇති MCQ / Output tracing ප්‍රශ්න වලදී ඔබ කම්පියුටරය සේ සිතා පියවරෙන් පියවර අගයන් වෙනස් වන ආකාරය (Dry run) කොළයක ලියා බැලීම අනිවාර්ය වේ.
