# Study Activity 06: Scanner, Math Library & Logic (ඛණ්ඩාංක සහ වෘත්තයක්)

## 📌 The Question (ප්‍රශ්නය)

(0,0) ලක්ෂ්‍යයේ කේන්ද්‍රය පිහිටන වෘත්තයක් සඳහා, පරිශීලකයාගෙන් වෘත්තයේ අරය (radius) සහ තවත් ඕනෑම ලක්ෂ්‍යයක x සහ y ඛණ්ඩාංක (coordinates) ලබාගෙන, එම ලක්ෂ්‍යය වෘත්තයට ඇතුලෙන්ද, පිටින්ද, නැත්නම් වෘත්තය මතද පිහිටන්නේ කියලා හොයන සම්පූර්ණ Java ප්‍රෝග්‍රෑම් එකක් ලියන්න.

**Requirements:**
1. `Scanner` පන්තිය Import කර භාවිතා කරන්න.
2. User ගෙන් `radius`, `x`, `y` අගයන් ලබා ගන්න (`double`).
3. `Math.pow()` සහ `Math.sqrt()` භාවිතා කර දුර (Distance) ගණනය කරන්න.
4. ගණනය කළ දුර තිරයේ මුද්‍රණය කරන්න (Print).
5. `if-else` භාවිතා කර ලක්ෂ්‍යයේ පිහිටීම Print කරන්න.

---

## 💻 Your Answer (ඔබේ පිළිතුර)

```java
import java.util.Scanner;

public class ThePointAndCircle{

public static void main (String[] args){

Scanner input= new Scanner(System.in);

System.out.print("Enter radius :");

double radius=input.nextDouble();

System.out.print("Enter  point x value :");

double x=input.nextDouble();

System.out.print("Enter point y value :")

double y=input.nextDouble();

double distance=Math.sqrt(Math.pow(x,2)+Math.pow(y,2));

if (distance<radius){

System.out.println(`"Point is inside the circle"`);

}

else if(distance>radius){

System.out.println(`"Point is outside the circle"`);

}

else{

System.out.println(`"Point is on the circle"`);

}

Scanner.close();

}

}
```

---

## 💯 Evaluation & Marks (ඇගයීම සහ ලකුණු)

**Marks Awarded:** 7.5/10 (B+) 👍

**Instructor's Impression:**
ඔබේ ලොජික් (Logic) එක සහ ගණිතමය සමීකරණය කේතයක් බවට පත් කරපු විදිය (`Math.sqrt` සහ `Math.pow` භාවිතය) 100% ක් නිවැරදියි! ඒ වගේම `Scanner` එක හරියටම පාවිච්චි කරලා තියෙනවා. නමුත් කේතය Compile වීමට බාධා කරන කුඩා **Syntax Errors (ව්‍යාකරණ දෝෂ) 3ක්** තියෙනවා. විභාගයේදී මේවා ගොඩක් වැදගත් වෙන නිසා අපි ඒ ටික හදාගමු.

---

## 🧠 Explanation & Additional Tips (විවරණය සහ උපදෙස්)

### Error 01: Missing Semicolon (සෙමිකෝලන් අඩුවීම)
`System.out.print("Enter point y value :")` කියන පේළිය අගට සෙමිකෝලන් එකක් (`;`) දාන්න අමතක වෙලා. Java වල හැම Statement එකක්ම ඉවර වෙන්න ඕනේ සෙමිකෝලන් එකකින්.
* **නිවැරදි:** `System.out.print("Enter point y value :");`

### Error 02: Backticks vs Double Quotes (String ලිවීමේදී)
ඔබ Print කරන වාක්‍යය දෙපැත්තේ Backticks (`) සහ Double quotes (") දෙකම දාලා තියෙනවා. 
උදාහරණයක් විදියට: `` `"Point is inside the circle"` ``.
Java වල Strings ලියද්දි පාවිච්චි කරන්නේ **Double Quotes (`""`)** පමණයි.
* **නිවැරදි:** `System.out.println("Point is inside the circle");`

### Error 03: Object vs Class name (Scanner එක Close කිරීම)
ඔබ `Scanner.close();` කියලා ලියලා තියෙනවා. `Scanner` කියන්නේ පන්තියේ (Class) නම. අපි Close කරන්න ඕනේ අපි හදාගත්ත object එක. ඔයා හැදුව object එකේ නම `input`.
* **නිවැරදි:** `input.close();`

### අමතක වූ කොටස (Missed Requirement):
ප්‍රශ්නයේ අවශ්‍යතා (Requirements) වල 4 වෙනි කාරණාව වුණේ "ගණනය කළ දුර තිරයේ මුද්‍රණය කරන්න (Print)" කියන එක. ඔයා ඒක Print කරලා තිබුණේ නෑ.

### The A+ Version (නිවැරදි කරන ලද සම්පූර්ණ කේතය):

```java
import java.util.Scanner;

public class ThePointAndCircle {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Enter radius: ");
        double radius = input.nextDouble();

        System.out.print("Enter point x value: ");
        double x = input.nextDouble();

        System.out.print("Enter point y value: ");
        double y = input.nextDouble();

        // ගණිතමය සමීකරණය නිවැරදිව භාවිත කර ඇත!
        double distance = Math.sqrt(Math.pow(x, 2) + Math.pow(y, 2));

        // දුර ප්‍රමාණය මුද්‍රණය කිරීම (ප්‍රශ්නයේ ඉල්ලා ඇති පරිදි)
        System.out.println("Distance to point: " + distance);

        if (distance < radius) {
            System.out.println("Point is inside the circle");
        } else if (distance > radius) {
            System.out.println("Point is outside the circle");
        } else {
            System.out.println("Point is on the circle");
        }

        input.close(); // නියමිත Object එක Close කිරීම
    }
}
```

**Vocabulary for Exams:**
* `Instantiating an Object` - Class එකකින් අලුත් object එකක් සෑදීම (උදා: `new Scanner(System.in)`).
* `Syntax Error` - භාෂාවේ ව්‍යාකරණ නීති කැඩීම නිසා එන දෝෂය (උදා: `;` අඩුවීම).
