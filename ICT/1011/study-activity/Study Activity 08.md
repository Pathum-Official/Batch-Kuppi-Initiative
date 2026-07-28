# Study Activity 08: Mini-Project (ATM Simulation)

## 📌 The Question (ප්‍රශ්නය)

ඔබට සරල ATM යන්ත්‍රයක ක්‍රියාවලියක් (simulation) නිර්මාණය කිරීමට අවශ්‍ය වී ඇත. මෙහිදී පරිශීලකයාට (user) තමන්ගේ ගිණුමේ ශේෂය (balance) බැලීමට, සල්ලි තැන්පත් කිරීමට (deposit) සහ මුදල් ලබාගැනීමට (withdraw) හැකි විය යුතුය. User 4 වන option එක (Exit) තෝරන තුරු මේ ATM මෙනුව (Menu) දිගටම තිරයේ දිස් විය යුතුය.

පහත අවශ්‍යතා (requirements) සපුරාලමින් `ATM` නමින් සම්පූර්ණ Java කේතයක් ලියන්න.

1. **Global Variable:** `static double balance = 0.0;`
2. **Custom Methods:** `deposit(double amount)`, `withdraw(double amount)`, `displayBalance()`
3. **The `main` Method:** Use a `Scanner`, `do-while` or `while(true)` loop, and a `switch` statement for the menu.

---

## 💻 Your Answer (ඔබේ පිළිතුර)

```java
import java.util.Scanner;

public class ATM{
    static double balance=0.0;

    public static void deposit(double amount){
        if(amount>0){
            balance +=amount;
            System.out.println("Deposit Successful");
        }
        else{
            System.out.println("Invalid amount");
        }
    }

    public static void withdraw(double amount){
        if(amount>0){
            if(amount<=balance){
                balance -=amount;
                System.out.println("Withdrawal Successful");
            }
            else{
                System.out.println("Insufficient funds");
            }
        }
        else{
            System.out.println("Invalid amount");
        }
    }

    public static void displayBalance(){
        System.out.println("Your current balance is "+balance);
    }

    public static void main (String[] args){
        Scanner input = new Scanner(System.in);
        do {
            System.out.println("--- ATM Menu ---");
            System.out.println("1. Check Balance");
            System.out.println("2. Deposit Money");
            System.out.println("3. Withdraw Money");
            System.out.println("4. Exit");
            System.out.print("Choose an option: ");

            char userChoose = input.nextChar();
            switch userChoose{
                case '1':
                    displayBalance();
                    break;
                case '2':
                    System.out.print("Enter You'r Deposit Amount : ");
                    deposit(input.nextDouble());
                    break;
                case '3':
                    System.out.print("Enter You'r Withdraw Amount : ");
                    withdraw(input.nextDouble());
                    break;
                case '4':
                    System.out.println("Thank you for using our ATM services!");
                    break;
                default:
                    System.out.println("Invalid Choose, Try Again...");
            }
        }while (userChoose!='4');
        input.close();
    }
}
```

---

## 💯 Evaluation & Marks (ඇගයීම සහ ලකුණු)

**Marks Awarded:** 8/10 (A-) 👍

**Instructor's Impression:**
ඔබේ ලොජික් (Logic) එක අතිවිශිෂ්ටයි! ඔබ මේ වගේ සම්පූර්ණ mini-project එකක් තනියම ලියපු එක ගැන මම ගොඩක් සතුටු වෙනවා. `deposit` සහ `withdraw` methods වල `if-else` ලියපු විදියත්, method එකට කෙලින්ම `deposit(input.nextDouble());` විදියට අගයන් යවපු විදියත් ඉතාමත් Advanced (සුපිරි) වැඩක්!
නමුත් කේතය Compile වීමට බාධා කරන **Syntax Errors 2ක්** සහ **Logical Error (Variable Scope issue) 1ක්** තියෙනවා. අපි ඒ ටික හදාගමු.

---

## 🧠 Explanation & Additional Tips (විවරණය සහ උපදෙස්)

### Error 01: Scanner `nextChar()` (නැති method එකක් භාවිතා කිරීම)

Java වල `Scanner` class එක ඇතුලේ `nextInt()`, `nextDouble()`, `nextLine()` වගේ ක්‍රම තිබුණට **`nextChar()` කියලා ක්‍රමයක් නැහැ**.

* එක අකුරක් (char) ගන්න නම් අපි ලියන්න ඕනේ: `input.next().charAt(0);`
* **වඩාත් ලේසි ක්‍රමය (A+ Tip):** Menu options තෝරද්දී `char` වෙනුවට `int` (පූර්ණ සංඛ්‍යා) භාවිතා කිරීමයි. එතකොට `int userChoose = input.nextInt();` විදියට ලේසියෙන්ම ගන්න පුළුවන්.

### Error 02: Switch Statement Syntax

`switch` කියන එක ලියද්දී variable එක අනිවාර්යයෙන්ම වරහන් (Parentheses) ඇතුලේ තියෙන්න ඕනේ.

* **ඔබේ කේතය:** `switch userChoose {`
* **නිවැරදි කේතය:** `switch (userChoose) {`

### Error 03: Variable Scope (විභාගයේදී අනිවාර්යයෙන්ම එන උගුලක්)

ඔබ `char userChoose = input.nextChar();` කියලා variable එක **Declare** කරලා තියෙන්නේ `do { ... }` කියන block එක ඇතුලේ. Java වල නීතියක් තමයි සඟල වරහන් `{ }` ඇතුලේ හදන variables, ඒ වරහනෙන් එළියට ගියාම මැකිලා යනවා (destroyed).
ඒ නිසා අන්තිමට තියෙන `while (userChoose != '4');` එකේදී Java වලට `userChoose` කියන එක අඳුරගන්න බැරි වෙනවා (Error: Cannot find symbol).

* **විසඳුම:** Variable එක `do` එකට කලින් ප්‍රකාශ (Declare) කරන්න.

### The Final Touch (නිවැරදි කරන ලද සම්පූර්ණ කේතය)

මෙහිදී මම `char` වෙනුවට වඩාත් පහසු `int` භාවිතා කර ඇත.

```java
import java.util.Scanner;

public class ATM {
  
    // Global Variable (Class-level)
    static double balance = 0.0;

    public static void deposit(double amount) {
        if (amount > 0) {
            balance += amount;
            System.out.println("Deposit Successful");
        } else {
            System.out.println("Invalid amount");
        }
    }

    public static void withdraw(double amount) {
        if (amount > 0) {
            if (amount <= balance) {
                balance -= amount;
                System.out.println("Withdrawal Successful");
            } else {
                System.out.println("Insufficient funds");
            }
        } else {
            System.out.println("Invalid amount");
        }
    }

    public static void displayBalance() {
        System.out.println("Your current balance is " + balance);
    }

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
      
        // Variable Scope: Declared outside the loop!
        int userChoose; 

        do {
            System.out.println("\n--- ATM Menu ---");
            System.out.println("1. Check Balance");
            System.out.println("2. Deposit Money");
            System.out.println("3. Withdraw Money");
            System.out.println("4. Exit");
            System.out.print("Choose an option: ");

            // Initialization happens inside the loop
            userChoose = input.nextInt(); 

            // Parentheses added!
            switch (userChoose) { 
                case 1:
                    displayBalance();
                    break;
                case 2:
                    System.out.print("Enter Your Deposit Amount: ");
                    // Passing input directly to the parameter
                    deposit(input.nextDouble()); 
                    break;
                case 3:
                    System.out.print("Enter Your Withdraw Amount: ");
                    withdraw(input.nextDouble());
                    break;
                case 4:
                    System.out.println("Thank you for using our ATM services!");
                    break;
                default:
                    System.out.println("Invalid Choice, Try Again...");
            }
        } while (userChoose != 4);

        input.close();
    }
}
```

### English Terms to Remember

* **Global Variable / Class-level Variable:** මුළු පන්තියටම (Class) පොදු විචල්‍යයක් (උදා: `static double balance`).
* **Variable Scope:** විචල්‍යයක් වලංගු වන සීමාව (උදා: `{ }` ඇතුලේ සීමාව).
* **Infinite Loop (අනන්ත ලූපය):** කවදාවත් නතර වෙන්නේ නැති loop එකක්. අපේ menu එක `4` එබුවොත් විතරක් නතර වෙන නිසා ඒක හොඳයි.
* **Syntax / Parentheses:** කේතයේ ව්‍යාකරණ සහ වරහන්.
