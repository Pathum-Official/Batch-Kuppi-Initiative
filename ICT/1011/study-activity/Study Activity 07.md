# Study Activity 07: Arrays and Custom Methods (අරා සහ මෙතඩ්ස්)

## 📌 The Question (ප්‍රශ්නය)

Write a complete Java program (සම්පූර්ණ Java කේතයක් ලියන්න) that performs the following tasks:
1. **Inside the `main` method (main method එක ඇතුලේ):**
   * Create an **integer array** of size 5.
   * Use a `Scanner` and a **loop** to read 5 numbers from the user and store them in the array.
2. **Create a separate custom method (වෙනම method එකක් හදන්න):**
   * Method name: `calculateAverage`
   * **Parameter:** It must accept an integer array (`int[]`).
   * **Return type:** It must return the **average (මධ්‍යන්‍යය)** of the numbers as a `double`.
3. **Call the method (Method එක කතා කිරීම):**
   * Back in the `main` method, **call** the `calculateAverage` method, pass your array to it, and **print** the final answer.

---

## 💻 Your Answer (ඔබේ පිළිතුර)

```java
import java.util.Scanner;

public class Average{

    public static double calculateAverage(int[] numbers){
        double sum=0;
        if (numbers==null || numbers.length==0){
            return 0;
        }
        for (int i=0;i<numbers.length;i++){
            sum +=numbers[i];
        }
        return sum/numbers.length;
    }

    public static void main (String[] args){
        Scanner input = new Scanner(System.in);
        int[] numberlist = new int[5];

        for(int i=0;i<numberlist.length;i++){
            System.out.print("Enter Value "+(i+1)+" to the list :");
            numberlist[i]=input.nextInt();
        }

        System.out.println("You Number list Average Is : "+calculateAverage(numberlist));
    }
}
```

---

## 💯 Evaluation & Marks (ඇගයීම සහ ලකුණු)

**Marks Awarded:** 9.5/10 (A+) 🌟

**Instructor's Impression:**
Outstanding work! අතිවිශිෂ්ටයි! ඔබ මේ කේතය ලියපු විදිය දැක්කම ඔබ programming වල පදනම (foundation) ඉතාමත් හොඳින් තේරුම් අරගෙන තියෙනවා කියලා පේනවා. 
ඔබ කලින් පාඩමේ ඉගෙනගත්ත **Guard Clause** (`if (numbers==null || numbers.length==0)`) එක මෙතනත් පාවිච්චි කරලා තියෙන එකෙන් පේන්නේ ඔබ දැන් Advanced මට්ටමට හිතන්න පුරුදු වෙලා කියන එකයි. ඒ වගේම `sum` කියන variable එක `double` විදියට declare කරපු නිසා Integer Division කියන ප්‍රශ්නයත් මඟහැරිලා තියෙනවා.

---

## 🧠 Explanation & Additional Tips (විවරණය සහ උපදෙස්)

### Integer Division Trap (විභාගයේදී අහුවෙන උගුලක්)
ගොඩක් ළමයි `sum` කියන variable එක හදන්නේ `int sum = 0;` කියලා. එහෙම හැදුවොත් `sum / numbers.length` බෙදද්දී උත්තරේ එන්නේ පූර්ණ සංඛ්‍යාවක් (Integer). උදාහරණයක් විදියට එකතුව `14` ඇවිත් ඒක `5` න් බෙදුවොත් උත්තරේ `2.8` වෙනුවට `2.0` කියලා එන්නේ.
නමුත් ඔබ `double sum = 0;` කියලා ගත්ත නිසා ඒ ප්‍රශ්නය ඇති වෙන්නේ නෑ. That was a very smart move! (ඉතාමත් බුද්ධිමත් පියවරක්!)

### Missing Semicolon / Small Error
ඔබේ කේතයේ Syntax Errors කිසිවක් නෑ. හැබැයි කලින් පාඩමේ කිව්වා වගේම **Scanner object** එක close කරන්න අමතක වෙලා තියෙනවා.
* `input.close();`

### English Terms to Remember (විභාගයට අවශ්‍ය ඉංග්‍රීසි වචන)
* **Declaration (ප්‍රකාශ කිරීම):** අලුත් array එකක් හදනකොට මුලින්ම ඒකේ වර්ගය කියන එක. `int[] numberlist`
* **Instantiation (නිර්මාණය කිරීම):** අලුත් දෙයක් මතකයේ (memory) හදන එක. `new int[5]`
* **Method Invocation / Calling a method:** අපි හදපු method එකක් පාවිච්චි කරන එක. උදා: `calculateAverage(numberlist)`
* **Iterating / Traversing:** Array එකක මුල ඉඳන් අගට යන එක. (Loop එක පාවිච්චි කරලා).

### The Final Touch (සුළු වෙනසක් සමඟ සම්පූර්ණ කේතය)

```java
import java.util.Scanner;

public class Average {

    // Custom method to calculate the average
    public static double calculateAverage(int[] numbers) {
        // Guard clause for edge cases
        if (numbers == null || numbers.length == 0) {
            return 0;
        }

        double sum = 0;
        for (int i = 0; i < numbers.length; i++) {
            sum += numbers[i];
        }
        
        return sum / numbers.length;
    }

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        
        // Array Declaration and Instantiation
        int[] numberlist = new int[5];

        // Iterating through the array to get input
        for (int i = 0; i < numberlist.length; i++) {
            System.out.print("Enter Value " + (i + 1) + " to the list: ");
            numberlist[i] = input.nextInt();
        }

        // Method Invocation and Printing
        System.out.println("Your Number list Average Is: " + calculateAverage(numberlist));
        
        // Don't forget to close the scanner!
        input.close(); 
    }
}
```
