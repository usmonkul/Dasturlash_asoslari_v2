<details>
    <summary>JavaScript nima?</summary>

## 10.1 JavaScript Nima?

### JavaScript nima?

**JavaScript** - web-sahifalarni jonli va interaktiv qiladigan dasturlash tili. Bu til brauzerda ishlaydi va web-sahifalarga hayot baxsh etadi.

### JavaScript nima uchun kerak?

#### 1. Interaktivlik
- Tugmalarni bosganda ishlaydi
- Formalar to'ldirilganda tekshiradi
- Animatsiyalar yaratadi
- O'yinlar yaratish mumkin

#### 2. Dinamik mazmun
- Sahifa mazmunini o'zgartirish
- Yangi ma'lumotlarni yuklash
- Foydalanuvchi harakatlariga javob berish
- Real vaqtda yangilanish

#### 3. Web ilovalar
- To-do ro'yxatlari
- Kalkulyatorlar
- O'yinlar
- Chat ilovalari

### JavaScript qayerda ishlaydi?

#### 1. Brauzerda
- Chrome, Firefox, Safari
- Web-sahifalarda
- Foydalanuvchi bilan muloqot

#### 2. Serverda
- Node.js yordamida
- Backend ilovalar
- Ma'lumotlar bazasi bilan ishlash

### JavaScript afzalliklari

#### 1. Oson o'rganish
- Oddiy sintaksis
- Ko'p resurslar
- Keng jamiyat

#### 2. Keng qo'llaniladi
- Barcha brauzerlarda ishlaydi
- Web, mobil, desktop
- Eng mashhur dasturlash tili

#### 3. Tez rivojlantirish
- Darhol natija ko'rish
- Brauzerda test qilish
- Kam kod bilan ko'p ish

### JavaScript misollari

#### 1. Oddiy xabar
```javascript
alert("Salom, dunyo!");
```

#### 2. Konsolga yozish
```javascript
console.log("Bu xabar konsolda ko'rinadi");
```

#### 3. Matematik hisob
```javascript
var son = 5 + 3;
console.log(son); // 8 chiqadi
```

### Amaliy misol - JavaScript asoslari
```javascript
// 1. Xabar ko'rsatish
alert("JavaScript ga xush kelibsiz!");

// 2. Konsolga yozish
console.log("Bu birinchi JavaScript kodingiz");

// 3. O'zgaruvchi yaratish
var ism = "Ahmad";
console.log("Salom, " + ism + "!");

// 4. Matematik amallar
var a = 10;
var b = 5;
var yigindi = a + b;
console.log(a + " + " + b + " = " + yigindi);

// 5. Foydalanuvchi bilan muloqot
var foydalanuvchiIsmi = prompt("Ismingizni kiriting:");
console.log("Salom, " + foydalanuvchiIsmi + "!");
```

</details>

<details>
    <summary>Brauzer konsolida ishlash</summary>

## 10.2 Brauzer Konsolida Ishlash

### Brauzer konsoli nima?

**Brauzer konsoli** - JavaScript kodini yozish va test qilish uchun maxsus oyna. Bu yerda kod yozib, darhol natijasini ko'rish mumkin.

### Konsolni ochish

#### 1. Chrome brauzerida
- **F12** tugmasini bosing
- Yoki **Ctrl + Shift + I** (Windows)
- Yoki **Cmd + Option + I** (Mac)

#### 2. Firefox brauzerida
- **F12** tugmasini bosing
- Yoki **Ctrl + Shift + K** (Windows)
- Yoki **Cmd + Option + K** (Mac)

#### 3. Safari brauzerida
- **Cmd + Option + C** (Mac)
- Avval Developer menyusini yoqish kerak

### Konsol elementlari

#### 1. Kod yozish maydoni
- Pastki qismda joylashgan
- Bu yerda JavaScript kod yoziladi
- **Enter** tugmasi bilan kod ishga tushadi

#### 2. Natija ko'rsatish
- Yuqorida natijalar ko'rinadi
- Xatolar qizil rangda
- Muvaffaqiyatli kod qora rangda

#### 3. Tarix
- Oldingi kodlar saqlanadi
- Yuqoriga pastga o'tish mumkin
- **Ctrl + L** bilan tozalash

### Konsol buyruqlari

#### 1. console.log() - xabar chiqarish
```javascript
console.log("Salom, dunyo!");
console.log(123);
console.log(true);
```

#### 2. console.error() - xato xabari
```javascript
console.error("Bu xato xabari");
```

#### 3. console.warn() - ogohlantirish
```javascript
console.warn("Bu ogohlantirish xabari");
```

#### 4. console.clear() - konsolni tozalash
```javascript
console.clear();
```

### Amaliy misol - Konsol bilan ishlash
```javascript
// 1. Birinchi xabar
console.log("JavaScript konsoliga xush kelibsiz!");

// 2. Raqamlar bilan ishlash
console.log("5 + 3 = " + (5 + 3));
console.log("10 - 4 = " + (10 - 4));
console.log("6 * 7 = " + (6 * 7));
console.log("15 / 3 = " + (15 / 3));

// 3. Matnlar bilan ishlash
console.log("Mening ismim: Ahmad");
console.log("Men " + 15 + " yoshdaman");

// 4. Mantiqiy qiymatlar
console.log("5 > 3: " + (5 > 3));
console.log("2 < 1: " + (2 < 1));

// 5. Xato va ogohlantirish
console.warn("Bu ogohlantirish xabari");
console.error("Bu xato xabari");

// 6. Konsolni tozalash
// console.clear(); // Bu buyruqni ishga tushiring
```

### Konsol maslahatlari

#### 1. Kod yozish
- Har bir buyruqdan keyin **Enter** bosing
- Katta-kichik harflarga e'tibor bering
- Qavslar va nuqta-vergullarni to'g'ri qo'ying

#### 2. Xatolarni tuzatish
- Qizil xabarlarni o'qing
- Qaysi qatorda xato borligini tekshiring
- Kodni qayta yozing

#### 3. Kodni saqlash
- Konsoldagi kod saqlanmaydi
- Muhim kodlarni boshqa joyga nusxalang
- HTML fayl ichida yozing

</details>

<details>
    <summary>O'zgaruvchilar (var, let, const)</summary>

## 10.3 O'zgaruvchilar (var, let, const)

### O'zgaruvchi nima?

**O'zgaruvchi** - ma'lumotlarni saqlash uchun ishlatiladigan konteyner. O'zgaruvchiga nom berib, unda qiymat saqlash mumkin.

### O'zgaruvchi yaratish

#### 1. var - eski usul
```javascript
var ism = "Ahmad";
var yosh = 15;
var oqish = true;
```

#### 2. let - yangi usul
```javascript
let ism = "Ahmad";
let yosh = 15;
let oqish = true;
```

#### 3. const - o'zgarmas
```javascript
const ism = "Ahmad";
const yosh = 15;
const oqish = true;
```

### O'zgaruvchi turlari

#### 1. var - eski usul
- Barcha joylarda ishlaydi
- Qayta e'lon qilish mumkin
- Hoisting qo'llab-quvvatlanadi

#### 2. let - yangi usul
- Faqat blok ichida ishlaydi
- Qayta e'lon qilish mumkin emas
- Zamonaviy usul

#### 3. const - o'zgarmas
- Qiymati o'zgarmaydi
- Qayta e'lon qilish mumkin emas
- Doimiy qiymatlar uchun

### O'zgaruvchi nomlari qoidalari

#### 1. To'g'ri nomlar
```javascript
var ism = "Ahmad";        // ✅ Harflar
var ism123 = "Ahmad";     // ✅ Harflar va raqamlar
var _ism = "Ahmad";       // ✅ Underscore
var $ism = "Ahmad";       // ✅ Dollar belgisi
var ismFamiliya = "Ahmad"; // ✅ CamelCase
```

#### 2. Noto'g'ri nomlar
```javascript
var 123ism = "Ahmad";     // ❌ Raqam bilan boshlanadi
var ism- = "Ahmad";       // ❌ Tire ishlatilgan
var var = "Ahmad";        // ❌ Kalit so'z
var ism familiya = "Ahmad"; // ❌ Bo'sh joy
```

### O'zgaruvchi qiymatlarini o'zgartirish

#### 1. var va let
```javascript
var ism = "Ahmad";
ism = "Karim";  // Qiymat o'zgartirildi
console.log(ism); // "Karim" chiqadi

let yosh = 15;
yosh = 16;  // Qiymat o'zgartirildi
console.log(yosh); // 16 chiqadi
```

#### 2. const
```javascript
const ism = "Ahmad";
// ism = "Karim";  // ❌ Xato! const o'zgarmaydi
console.log(ism); // "Ahmad" chiqadi
```

### Amaliy misol - O'zgaruvchilar
```javascript
// 1. var bilan o'zgaruvchilar
var ism = "Ahmad";
var yosh = 15;
var maktab = "15-maktab";

console.log("Ism: " + ism);
console.log("Yosh: " + yosh);
console.log("Maktab: " + maktab);

// 2. let bilan o'zgaruvchilar
let fan = "Matematika";
let baho = 5;

console.log("Fan: " + fan);
console.log("Baho: " + baho);

// 3. const bilan o'zgaruvchilar
const pi = 3.14;
const maktabRaqami = 15;

console.log("Pi: " + pi);
console.log("Maktab raqami: " + maktabRaqami);

// 4. Qiymatlarni o'zgartirish
yosh = 16;  // let o'zgaruvchisi
baho = 4;   // let o'zgaruvchisi

console.log("Yangi yosh: " + yosh);
console.log("Yangi baho: " + baho);

// 5. O'zgaruvchilarni bir-biriga tayinlash
var birinchiSon = 10;
var ikkinchiSon = 5;
var yigindi = birinchiSon + ikkinchiSon;

console.log(birinchiSon + " + " + ikkinchiSon + " = " + yigindi);
```

### O'zgaruvchi maslahatlari

#### 1. Nom berish
- Aniq va tushunarli nomlar ishlating
- CamelCase usulidan foydalaning
- Kalit so'zlardan qoching

#### 2. Tur tanlash
- **const** - o'zgarmas qiymatlar uchun
- **let** - o'zgaruvchan qiymatlar uchun
- **var** - eski kodlarda qolgan

#### 3. E'lon qilish
- O'zgaruvchini ishlatishdan oldin e'lon qiling
- Bir vaqtda bir nechta e'lon qilish mumkin
- Qiymat bermasdan ham e'lon qilish mumkin

</details>

<details>
    <summary>Ma'lumot turlari (string, number, boolean)</summary>

## 10.4 Ma'lumot Turlari (String, Number, Boolean)

### Ma'lumot turlari nima?

**Ma'lumot turlari** - JavaScript da turli xil ma'lumotlarni ifodalash usullari. Har bir tur o'ziga xos xususiyatlarga ega.

### Asosiy ma'lumot turlari

#### 1. String (Matn)
- Matn ma'lumotlari
- Qo'shtirnoq ichida yoziladi
- Harflar, raqamlar, belgilar

#### 2. Number (Raqam)
- Raqamli ma'lumotlar
- Butun va kasr sonlar
- Matematik amallar

#### 3. Boolean (Mantiqiy)
- True yoki False
- Ha yoki Yo'q
- Mantiqiy qiymatlar

### String (Matn) turlari

#### 1. Qo'shtirnoq
```javascript
var ism = "Ahmad";
var familiya = "Karimov";
var maktab = "15-maktab";
```

#### 2. Birtirnoq
```javascript
var ism = 'Ahmad';
var familiya = 'Karimov';
var maktab = '15-maktab';
```

#### 3. Backtick
```javascript
var ism = `Ahmad`;
var familiya = `Karimov`;
var maktab = `15-maktab`;
```

### Number (Raqam) turlari

#### 1. Butun sonlar
```javascript
var yosh = 15;
var sinf = 9;
var maktabRaqami = 15;
```

#### 2. Kasr sonlar
```javascript
var baho = 4.5;
var pi = 3.14;
var foiz = 85.7;
```

#### 3. Manfiy sonlar
```javascript
var harorat = -5;
var balandlik = -100;
var xato = -1;
```

### Boolean (Mantiqiy) turlari

#### 1. True (Ha)
```javascript
var oqish = true;
var ishlash = true;
var tushunish = true;
```

#### 2. False (Yo'q)
```javascript
var oqish = false;
var ishlash = false;
var tushunish = false;
```

### Ma'lumot turlarini tekshirish

#### 1. typeof operatori
```javascript
var ism = "Ahmad";
console.log(typeof ism); // "string" chiqadi

var yosh = 15;
console.log(typeof yosh); // "number" chiqadi

var oqish = true;
console.log(typeof oqish); // "boolean" chiqadi
```

#### 2. Turli misollar
```javascript
console.log(typeof "Salom"); // "string"
console.log(typeof 123); // "number"
console.log(typeof true); // "boolean"
console.log(typeof false); // "boolean"
```

### Amaliy misol - Ma'lumot turlari
```javascript
// 1. String (Matn) misollari
var ism = "Ahmad";
var familiya = "Karimov";
var maktab = "15-maktab";
var manzil = "Toshkent shahar";

console.log("Ism: " + ism);
console.log("Familiya: " + familiya);
console.log("Maktab: " + maktab);
console.log("Manzil: " + manzil);

// 2. Number (Raqam) misollari
var yosh = 15;
var sinf = 9;
var baho = 4.5;
var maktabRaqami = 15;

console.log("Yosh: " + yosh);
console.log("Sinf: " + sinf);
console.log("Baho: " + baho);
console.log("Maktab raqami: " + maktabRaqami);

// 3. Boolean (Mantiqiy) misollari
var oqish = true;
var ishlash = false;
var tushunish = true;
var qiyin = false;

console.log("O'qish: " + oqish);
console.log("Ishlash: " + ishlash);
console.log("Tushunish: " + tushunish);
console.log("Qiyin: " + qiyin);

// 4. Ma'lumot turlarini tekshirish
console.log("ism turi: " + typeof ism);
console.log("yosh turi: " + typeof yosh);
console.log("oqish turi: " + typeof oqish);

// 5. Matematik amallar
var a = 10;
var b = 5;
var yigindi = a + b;
var ayirma = a - b;
var kopaytma = a * b;
var bolinma = a / b;

console.log(a + " + " + b + " = " + yigindi);
console.log(a + " - " + b + " = " + ayirma);
console.log(a + " * " + b + " = " + kopaytma);
console.log(a + " / " + b + " = " + bolinma);
```

### Ma'lumot turlari maslahatlari

#### 1. String ishlatish
- Matnlar uchun qo'shtirnoq ishlating
- Bo'sh joylarga e'tibor bering
- Maxsus belgilarni to'g'ri yozing

#### 2. Number ishlatish
- Raqamlar uchun qo'shtirnoq ishlatmang
- Kasr sonlarda nuqta ishlating
- Katta sonlarni o'qish oson qiling

#### 3. Boolean ishlatish
- Faqat true yoki false ishlating
- Mantiqiy qiymatlarni aniq belgilang
- Shartlarda ishlatish uchun

</details>

<details>
    <summary>Oddiy amallar</summary>

## 10.5 Oddiy Amallar

### Oddiy amallar nima?

**Oddiy amallar** - JavaScript da asosiy matematik va mantiqiy operatsiyalar. Bu amallar yordamida hisob-kitoblar va taqqoslashlar bajariladi.

### Matematik amallar

#### 1. Qo'shish (+)
```javascript
var a = 5;
var b = 3;
var yigindi = a + b;
console.log(yigindi); // 8 chiqadi
```

#### 2. Ayirish (-)
```javascript
var a = 10;
var b = 4;
var ayirma = a - b;
console.log(ayirma); // 6 chiqadi
```

#### 3. Ko'paytirish (*)
```javascript
var a = 6;
var b = 7;
var kopaytma = a * b;
console.log(kopaytma); // 42 chiqadi
```

#### 4. Bo'lish (/)
```javascript
var a = 15;
var b = 3;
var bolinma = a / b;
console.log(bolinma); // 5 chiqadi
```

#### 5. Qoldiq (%)
```javascript
var a = 17;
var b = 5;
var qoldiq = a % b;
console.log(qoldiq); // 2 chiqadi
```

### Taqqoslash amallari

#### 1. Teng (=)
```javascript
var a = 5;
var b = 5;
var teng = (a == b);
console.log(teng); // true chiqadi
```

#### 2. Teng emas (!=)
```javascript
var a = 5;
var b = 3;
var tengEmas = (a != b);
console.log(tengEmas); // true chiqadi
```

#### 3. Katta (>)
```javascript
var a = 10;
var b = 5;
var katta = (a > b);
console.log(katta); // true chiqadi
```

#### 4. Kichik (<)
```javascript
var a = 3;
var b = 7;
var kichik = (a < b);
console.log(kichik); // true chiqadi
```

#### 5. Katta yoki teng (>=)
```javascript
var a = 5;
var b = 5;
var kattaTeng = (a >= b);
console.log(kattaTeng); // true chiqadi
```

#### 6. Kichik yoki teng (<=)
```javascript
var a = 4;
var b = 5;
var kichikTeng = (a <= b);
console.log(kichikTeng); // true chiqadi
```

### Mantiqiy amallar

#### 1. AND (&&)
```javascript
var a = true;
var b = true;
var and = (a && b);
console.log(and); // true chiqadi
```

#### 2. OR (||)
```javascript
var a = true;
var b = false;
var or = (a || b);
console.log(or); // true chiqadi
```

#### 3. NOT (!)
```javascript
var a = true;
var not = !a;
console.log(not); // false chiqadi
```

### Amaliy misol - Oddiy amallar
```javascript
// 1. Matematik amallar
var a = 20;
var b = 4;

console.log("a = " + a);
console.log("b = " + b);
console.log("a + b = " + (a + b));
console.log("a - b = " + (a - b));
console.log("a * b = " + (a * b));
console.log("a / b = " + (a / b));
console.log("a % b = " + (a % b));

// 2. Taqqoslash amallari
var x = 15;
var y = 10;

console.log("x = " + x);
console.log("y = " + y);
console.log("x == y: " + (x == y));
console.log("x != y: " + (x != y));
console.log("x > y: " + (x > y));
console.log("x < y: " + (x < y));
console.log("x >= y: " + (x >= y));
console.log("x <= y: " + (x <= y));

// 3. Mantiqiy amallar
var p = true;
var q = false;

console.log("p = " + p);
console.log("q = " + q);
console.log("p && q: " + (p && q));
console.log("p || q: " + (p || q));
console.log("!p: " + (!p));
console.log("!q: " + (!q));

// 4. Amallarni bir-biriga ulash
var son1 = 10;
var son2 = 5;
var son3 = 3;

var natija1 = son1 + son2 * son3;
var natija2 = (son1 + son2) * son3;
var natija3 = son1 - son2 + son3;

console.log("son1 + son2 * son3 = " + natija1);
console.log("(son1 + son2) * son3 = " + natija2);
console.log("son1 - son2 + son3 = " + natija3);

// 5. Matnlar bilan amallar
var ism = "Ahmad";
var familiya = "Karimov";
var toliqIsm = ism + " " + familiya;

console.log("Ism: " + ism);
console.log("Familiya: " + familiya);
console.log("To'liq ism: " + toliqIsm);
```

### Amallar maslahatlari

#### 1. Matematik amallar
- Qavslar bilan tartibni belgilang
- Kasr sonlarda ehtiyot bo'ling
- Nolga bo'lishdan saqlaning

#### 2. Taqqoslash amallari
- == va === farqini bilish
- Mantiqiy qiymatlarni to'g'ri ishlatish
- Null va undefined ni tekshirish

#### 3. Mantiqiy amallar
- && va || farqini tushunish
- ! operatorini to'g'ri ishlatish
- Murakkab shartlarni soddalashtirish

</details>
