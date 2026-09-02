# 02. Output Formatting (තිරයේ මුද්‍රණය සහ හැඩතල ගැන්වීම)

## 1. Print vs Println
* `System.out.print()` : ලබාදෙන දේ මුද්‍රණය කර ඊළඟට එන දේ **එම පේළියේම** තබයි.
* `System.out.println()` : ලබාදෙන දේ මුද්‍රණය කර ඊළඟට එන දේ **අලුත් පේළියකට (New Line)** ගෙන යයි.

## 2. Escape Sequences (විශේෂ සංකේත)
String එකක් ඇතුලේ විශේෂ දේවල් කරන්න මේවා පාවිච්චි කරයි.
* `\n` : New line (අලුත් පේළියක්)
* `\t` : Tab space (හිස් ඉඩක්/ටැබ් එකක්)
* `\"` : Double quote එකක් print කිරීමට (උදා: `System.out.println("He said \"Hello\"");`)
* `\'` : Single quote එකක් print කිරීමට
* `\\` : Backslash එකක් print කිරීමට

## 3. System.out.printf() (අතිශය වැදගත්)
කලාත්මකව (Artistic) සහ පිළිවෙලට Print කරන්න `printf` භාවිතා කරයි.

### Format Specifiers (ආදේශක සංකේත)
* `%d` : Integer (පූර්ණ සංඛ්‍යා)
* `%f` : Floating point / Double (දශම සංඛ්‍යා)
* `%s` : String (වචන/වාක්‍ය)
* `%c` : Char (තනි අකුරු)

### Formatting Tricks (මැජික් ට්‍රික්ස්)
1. **දශමස්ථාන පාලනය (Decimal Places):**
   `System.out.printf("Average is %.2f", 45.6789);` -> Print වෙන්නේ **45.68** (දශම 2කට රවුම් වේ).
   
2. **ඉඩ වෙන් කිරීම (Padding):**
   `System.out.printf("%5d", 25);` -> ඉලක්කම් 5ක ඉඩක් වෙන් කර දකුණු පැත්තට බර කර Print කරයි. (Output: `   25`)
   `System.out.printf("%-5d", 25);` -> ඉලක්කම් 5ක ඉඩක් වෙන් කර වම් පැත්තට බර කර Print කරයි. (Output: `25   `)

3. **වගුවක් (Table) නිර්මාණය:**
   ```java
   System.out.printf("%-10s %-10s %-10s\n", "Name", "Marks", "Grade");
   System.out.printf("%-10s %-10d %-10s\n", "Kamal", 85, "A");
   ```
