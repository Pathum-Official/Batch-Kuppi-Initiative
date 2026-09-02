# 🚀 ICT 1011 Master Class: 08 - Arrays (1D & 2D)

> **මෙය ICT 1011 විෂය නිර්දේශයේ අටවන කොටස සම්පූර්ණයෙන්ම ආවරණය කරන මහාචාර්ය මට්ටමේ (Professor-level) සටහනකි.**
> (1D Arrays, 2D Arrays, Arrays හරහා ගමන් කිරීම සහ නිතර එන ප්‍රශ්න මෙහි අන්තර්ගත වේ).

---

## 1. What is an Array? (අරාවක් යනු කුමක්ද?)
Array එකක් යනු **එකම වර්ගයේ (same data type)** දත්ත රාශියක් එකම නමකින් (single variable) ගබඩා කර තබාගත හැකි දත්ත ව්‍යුහයකි (Data structure). 
උදාහරණයක් ලෙස, සිසුන් 50 දෙනෙකුගේ ලකුණු ගබඩා කිරීමට `mark1`, `mark2`... ලෙස විචල්‍ය 50ක් සෑදීම වෙනුවට එක `marks` array එකක් සෑදිය හැක.

### 🛑 Arrays වල ප්‍රධාන ලක්ෂණ:
1. **ස්ථාවර ප්‍රමාණය (Fixed Size):** Array එකක් සෑදූ පසු එහි ප්‍රමාණය (දිග) වෙනස් කළ නොහැක!
2. **දර්ශක (Zero-based Indexing):** Array එකක පළමු අගය ගබඩා වන්නේ 0 වෙනි ස්ථානයේය (Index 0). අවසාන අගය ඇත්තේ `(ප්‍රමාණය - 1)` වෙනි ස්ථානයේය.

---

## 2. One-Dimensional (1D) Arrays (ඒකමාන අරාවන්)

### 🛠️ 1D Array එකක් සාදන ආකාර (Declaration & Initialization)
ක්‍රම දෙකක් ඇත:

**ක්‍රමය 1: අගයන් කලින් දන්නා විට (Direct Initialization)**
```java
// 5, 10, 15, 20 යන අගයන් සහිත Array එකක් සෑදීම
int[] numbers = {5, 10, 15, 20}; 

// ප්‍රවේශ වීම (Accessing):
System.out.println(numbers[0]); // Output: 5
System.out.println(numbers[3]); // Output: 20
```

**ක්‍රමය 2: අගයන් පසුව ඇතුළත් කරන විට (Using `new` keyword)**
```java
// ඉලක්කම් 5ක් ගබඩා කළ හැකි හිස් Array එකක් සෑදීම
int[] marks = new int[5]; // ප්‍රමාණය 5කි (Index 0 සිට 4 දක්වා)

marks[0] = 75; // පළමු අගය ඇතුළත් කිරීම
marks[1] = 80;
// marks[5] = 90; // 🚨 ERROR! Index 5 කියන්නේ 6 වෙනි ස්ථානයයි. (ArrayIndexOutOfBoundsException)
```

### 🔄 1D Array එකක් හරහා ගමන් කිරීම (Iterating through an array)
Array එකක දිග (Length) දැනගැනීම සඳහා `.length` ප්‍රොපටිය (Property) භාවිතා කරයි. (මතක තබාගන්න: String වල මෙන් මෙහි වරහන් `()` නැත! එය `array.length` මිස `array.length()` නොවේ).

```java
int[] marks = {75, 80, 65, 90, 85};
int sum = 0;

for (int i = 0; i < marks.length; i++) {
    sum = sum + marks[i];
    System.out.println("Mark " + (i+1) + " is: " + marks[i]);
}
System.out.println("Total is: " + sum);
```

> [!CAUTION]
> **Professor's Trap (Array Index Out of Bounds):**
> විභාගයේ ලූපයේ කොන්දේසිය `i <= marks.length` ලෙස ලිව්වහොත් කුමක් වෙයිද? 
> උදාහරණයකට Array එකේ ප්‍රමාණය 5 නම්, අවසාන ඉලක්කම ඇත්තේ Index 4 හිය. නමුත් ලූපය `i=5` දක්වා ගමන් කළහොත් `marks[5]` සෙවීමට උත්සාහ කරයි. මෙය **`ArrayIndexOutOfBoundsException`** නම් භයානක Error එකට හේතු වේ! සෑම විටම `< length` මිස `<=` භාවිතා නොකරන්න.

---

## 3. Two-Dimensional (2D) Arrays (ද්විමාන අරාවන් / Matrix)
2D Array එකක් යනු **පේළි (Rows) සහ තීරු (Columns)** සහිත වගුවක් වැනිය. සරලවම කිව්වොත් මෙය Array ඇතුලේ තියෙන තවත් Arrays ය! (Array of arrays).

### 🛠️ 2D Array එකක් සාදන ආකාර
```java
// පේළි 3ක් සහ තීරු 4ක් (3x4 Matrix) ඇති 2D Array එකක්
int[][] matrix = {
    {1, 2, 3, 4},       // පේළිය 0 (Row 0)
    {5, 6, 7, 8},       // පේළිය 1 (Row 1)
    {9, 10, 11, 12}     // පේළිය 2 (Row 2)
};

// ප්‍රවේශ වීම: (arrayName[row][column])
System.out.println(matrix[1][2]); // පේළිය 1 හි, තීරුව 2 ➔ අගය 7 වේ.
```
*(හිස් 2D Array එකක් සෑදීම: `int[][] matrix = new int[3][4];` - පේළි 3යි, තීරු 4යි).*

### 🔄 2D Array එකක් හරහා ගමන් කිරීම (Nested Loops)
2D Array එකක ඇති සියලුම අගයන් කියවීමට අනිවාර්යයෙන්ම `for` ලූප දෙකක් (Nested for loops) භාවිතා කළ යුතුය.

```java
int[][] matrix = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};

int totalSum = 0;

// පිටත ලූපය (Outer Loop): පේළි (Rows) හරහා ගමන් කරයි
for (int row = 0; row < matrix.length; row++) {
    
    // ඇතුළත ලූපය (Inner Loop): තීරු (Columns) හරහා ගමන් කරයි
    // matrix[row].length යනු අදාළ පේළියේ ඇති තීරු ගණනයයි!
    for (int col = 0; col < matrix[row].length; col++) {
        totalSum += matrix[row][col];
    }
}
System.out.println("Total Sum of 2D Array: " + totalSum);
```

> [!IMPORTANT]
> **Professor's Tip (`matrix[row].length` vs `matrix.length`):** 
> * `matrix.length`: මෙමගින් ලැබෙන්නේ මුළු 2D Array එකේ ඇති **පේළි (Rows) ගණනයි** (ඉහත උදාහරණයේ 3යි). 
> * `matrix[row].length`: මෙමගින් ලැබෙන්නේ නිශ්චිත පේළියක් ඇතුළේ ඇති **තීරු (Columns) ගණනයි**. Java වල සෑම පේළියකම තීරු ගණන සමාන විය යුතුම නැත (Jagged arrays). එබැවින් ඇතුළත ලූපය සඳහා සෑම විටම `col < matrix[row].length` භාවිතා කිරීම අනිවාර්ය හොඳ පුරුද්දකි (Good practice).
