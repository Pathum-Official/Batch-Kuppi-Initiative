# 03. Java Math Library (ගණිතමය ක්‍රියාකාරකම්)

Java වල `Math` class එකේ ගොඩක් වැදගත් Methods තියෙනවා. මේවා අනිවාර්යයෙන්ම විභාගයට එනවා. මේ සියලුම methods `static` නිසා අපිට කෙලින්ම `Math.methodName()` ලෙස භාවිතා කළ හැක.

## 1. Power and Root (බල සහ මූල)
* **`Math.pow(base, exponent)`** : බලය සෙවීම. 
  `Math.pow(2, 3)` -> Return කරන්නේ `8.0` (Double).
* **`Math.sqrt(number)`** : වර්ගමූලය (Square root) සෙවීම.
  `Math.sqrt(16)` -> Return කරන්නේ `4.0` (Double).

## 2. Rounding Functions (රවුම් කිරීම)
* **`Math.round(number)`** : ආසන්නතම පූර්ණ සංඛ්‍යාවට රවුම් කරයි.
  `Math.round(5.4)` -> `5`, `Math.round(5.6)` -> `6`. (Return type is `long` or `int`).
* **`Math.ceil(number)`** : ඊළඟට තියෙන **ඉහළ** පූර්ණ සංඛ්‍යාවට (Ceiling/සිවිලිම) රවුම් කරයි.
  `Math.ceil(5.1)` -> `6.0`
* **`Math.floor(number)`** : ඊළඟට තියෙන **පහළ** පූර්ණ සංඛ්‍යාවට (Floor/පොළව) රවුම් කරයි.
  `Math.floor(5.9)` -> `5.0`

## 3. Absolute & Comparison (නිරපේක්ෂ සහ සංසන්දනය)
* **`Math.abs(number)`** : සෘණ ලකුණ ඉවත් කර ධන අගය (Absolute value) ලබා දෙයි.
  `Math.abs(-125)` -> `125`.
* **`Math.max(a, b)`** : ලබාදෙන අගයන් දෙකෙන් **විශාල** අගය ලබා දෙයි.
  `Math.max(10, 20)` -> `20`.
* **`Math.min(a, b)`** : ලබාදෙන අගයන් දෙකෙන් **කුඩා** අගය ලබා දෙයි.
  `Math.min(10, 20)` -> `10`.

## 4. Random Numbers (අහඹු සංඛ්‍යා)
* **`Math.random()`** : 0.0 සහ 1.0 අතර අහඹු දශම සංඛ්‍යාවක් ලබා දෙයි (1.0 ඇතුලත් නොවේ).
  * 0 ත් 10 ත් අතර අහඹු පූර්ණ සංඛ්‍යාවක් ගැනීමට: `(int)(Math.random() * 11)`

## 5. Constants (නියතයන්)
* **`Math.PI`** : PI හි අගය (3.14159...) ලබා ගැනීමට.
