<details>
    <summary>Funksiya nima?</summary>

## 11.1 Funksiya Nima?

### Funksiya nima?

**Funksiya** - JavaScript da ma'lum bir vazifani bajaradigan kod bloki. Funksiyani bir marta yozib, keyin istalgan vaqtda chaqirish mumkin.

### Funksiya nima uchun kerak?

#### 1. Kodni qayta ishlatish
- Bir xil kodni takrorlamaslik
- Vaqt tejash
- Xatolarni kamaytirish

#### 2. Kodni tartibga solish
- Katta dasturni kichik qismlarga bo'lish
- Oson o'qish va tushunish
- Muammolarni tez topish

#### 3. Vazifalarni ajratish
- Har bir funksiya bir vazifani bajaradi
- Kodni tushunarli qilish
- Jamoa bilan ishlashda qulay

### Funksiya misollari

#### 1. Oddiy funksiya
```javascript
// Funksiya yaratish
function salom() {
    console.log("Salom, dunyo!");
}

// Funksiyani chaqirish
salom(); // "Salom, dunyo!" chiqadi
```

#### 2. Matematik funksiya
```javascript
// Ikki sonni qo'shadigan funksiya
function qoshish(a, b) {
    return a + b;
}

// Funksiyani chaqirish
let natija = qoshish(5, 3);
console.log(natija); // 8 chiqadi
```

#### 3. Matn funksiyasi
```javascript
// Ismni katta harflar bilan chiqaradigan funksiya
function kattaHarflar(ism) {
    return ism.toUpperCase();
}

// Funksiyani chaqirish
let kattaIsm = kattaHarflar("ahmad");
console.log(kattaIsm); // "AHMAD" chiqadi
```

### Funksiya tuzilishi

#### 1. Funksiya kalit so'zi
```javascript
function // JavaScript da funksiya yaratish uchun
```

#### 2. Funksiya nomi
```javascript
function salom() // "salom" - funksiya nomi
```

#### 3. Qavslar
```javascript
function salom() // () - parametrlar uchun
```

#### 4. Jig'a qavslar
```javascript
function salom() {
    // Funksiya kodi bu yerda
}
```

### Amaliy misollar

#### 1. Oddiy funksiyalar
```javascript
// 1. Oddiy funksiya
function salom() {
    console.log("Salom! Funksiya muvaffaqiyatli chaqirildi.");
}

// Funksiyani chaqirish
salom();

// 2. Vaqt funksiyasi
function vaqt() {
    let hozirgiVaqt = new Date();
    console.log("Hozirgi vaqt: " + hozirgiVaqt.toLocaleTimeString());
}

// Funksiyani chaqirish
vaqt();

// 3. Tasodifiy son funksiyasi
function tasodifiySon() {
    let son = Math.floor(Math.random() * 10) + 1;
    console.log("Tasodifiy son: " + son);
}

// Funksiyani chaqirish
tasodifiySon();

// 4. Alert bilan funksiya
function salomAlert() {
    alert("Salom! Bu alert xabari.");
}

// Funksiyani chaqirish
salomAlert();
```

#### 2. Funksiya tushuntirish
```javascript
// Funksiya nima?
// Funksiya - ma'lum bir vazifani bajaradigan kod bloki
// Uni bir marta yozib, keyin istalgan vaqtda chaqirish mumkin

function salom() {
    console.log("Salom, dunyo!");
}

// Funksiya qismlari:
// function - funksiya yaratish kalit so'zi
// salom - funksiya nomi (istalgan nom berish mumkin)
// () - parametrlar uchun qavslar
// {} - funksiya kodi jig'a qavslar ichida

// Funksiyani chaqirish:
salom(); // Funksiya nomi va qavslar

// Funksiya afzalliklari:
// 1. Qayta ishlatish: Bir marta yozib, ko'p marta chaqirish
// 2. Tartib: Katta dasturni kichik qismlarga bo'lish
// 3. Osonlik: Kodni oson o'qish va tushunish
// 4. Xatolarni topish: Muammolarni tez aniqlash

// Misol: Ikki sonni qo'shadigan funksiya
function qoshish(a, b) {
    return a + b;
}

// Funksiyani chaqirish
let natija = qoshish(5, 3);
console.log(natija); // 8 chiqadi

// Bu misolda:
// a, b - funksiya parametrlari (kiruvchi ma'lumotlar)
// return - funksiya natijasini qaytarish
// qoshish(5, 3) - funksiyani chaqirish parametrlar bilan
```

</details>

<details>
    <summary>Funksiya yaratish va chaqirish</summary>

## 11.2 Funksiya Yaratish va Chaqirish

### Funksiya yaratish usullari

#### 1. Function declaration (Funksiya e'lon qilish)
```javascript
function funksiyaNomi() {
    // Funksiya kodi
}
```

#### 2. Function expression (Funksiya ifodasi)
```javascript
let funksiyaNomi = function() {
    // Funksiya kodi
};
```

#### 3. Arrow function (O'q funksiyasi)
```javascript
let funksiyaNomi = () => {
    // Funksiya kodi
};
```

### Funksiya yaratish qoidalari

#### 1. Nom berish
- Harflar, raqamlar, _ va $ ishlatish mumkin
- Raqam bilan boshlanmasligi kerak
- JavaScript kalit so'zlari ishlatilmasligi kerak

#### 2. To'g'ri nomlar
```javascript
function salom() {}        // ✅ To'g'ri
function salom123() {}     // ✅ To'g'ri
function _salom() {}       // ✅ To'g'ri
function $salom() {}       // ✅ To'g'ri
```

#### 3. Noto'g'ri nomlar
```javascript
function 123salom() {}     // ❌ Raqam bilan boshlanadi
function salom-() {}       // ❌ Tire ishlatilgan
function function() {}     // ❌ Kalit so'z
```

### Funksiyani chaqirish

#### 1. Oddiy chaqirish
```javascript
function salom() {
    console.log("Salom!");
}

salom(); // Funksiyani chaqirish
```

#### 2. Parametrlar bilan chaqirish
```javascript
function salom(ism) {
    console.log("Salom, " + ism + "!");
}

salom("Ahmad"); // "Salom, Ahmad!" chiqadi
```

#### 3. Natijani o'zgaruvchiga saqlash
```javascript
function qoshish(a, b) {
    return a + b;
}

let natija = qoshish(5, 3);
console.log(natija); // 8
```

### Amaliy misollar

#### 1. Funksiya yaratish va chaqirish
```javascript
// 1. Oddiy funksiya
function salom() {
    return "Salom, dunyo!";
}

// Funksiyani chaqirish
let natija1 = salom();
console.log(natija1); // "Salom, dunyo!" chiqadi

// 2. Parametrli funksiya
function salomBilan(ism) {
    return "Salom, " + ism + "!";
}

// Funksiyani chaqirish
let natija2 = salomBilan("Ahmad");
console.log(natija2); // "Salom, Ahmad!" chiqadi

// 3. Matematik funksiya
function kvadrat(son) {
    return son * son;
}

// Funksiyani chaqirish
let natija3 = kvadrat(5);
console.log("5 ning kvadrati = " + natija3); // "5 ning kvadrati = 25" chiqadi

// 4. Ikki parametrli funksiya
function qoshish(a, b) {
    return a + b;
}

// Funksiyani chaqirish
let natija4 = qoshish(7, 3);
console.log("7 + 3 = " + natija4); // "7 + 3 = 10" chiqadi

// 5. Funksiya expression
let ayirish = function(a, b) {
    return a - b;
};

// Funksiyani chaqirish
let natija5 = ayirish(10, 4);
console.log("10 - 4 = " + natija5); // "10 - 4 = 6" chiqadi
```

#### 2. Funksiya turlari taqqoslash
```javascript
// 1. Function Declaration (Funksiya E'lon Qilish)
function salomDeclaration() {
    return "Function Declaration";
}

// Xususiyatlari:
// - Funksiya nomi bilan yaratiladi
// - Hoisting (yuqoriga ko'tarilish) qo'llab-quvvatlanadi
// - Eng keng tarqalgan usul

// Funksiyani chaqirish
let natija1 = salomDeclaration();
console.log(natija1); // "Function Declaration" chiqadi

// 2. Function Expression (Funksiya Ifodasi)
let salomExpression = function() {
    return "Function Expression";
};

// Xususiyatlari:
// - O'zgaruvchiga tayinlanadi
// - Hoisting qo'llab-quvvatlanmaydi
// - Anonim funksiya sifatida ishlatiladi

// Funksiyani chaqirish
let natija2 = salomExpression();
console.log(natija2); // "Function Expression" chiqadi

// 3. Arrow Function (O'q Funksiyasi)
let salomArrow = () => {
    return "Arrow Function";
};

// Xususiyatlari:
// - Qisqa sintaksis
// - ES6 da kiritilgan
// - this kontekstini o'zgartirmaydi

// Funksiyani chaqirish
let natija3 = salomArrow();
console.log(natija3); // "Arrow Function" chiqadi

// 4. Parametrli Funksiyalar
// Function Declaration
function qoshish(a, b) {
    return a + b;
}

// Function Expression
let ayirish = function(a, b) {
    return a - b;
};

// Arrow Function
let kopaytirish = (a, b) => {
    return a * b;
};

// Barchasini test qilish
console.log("Qo'shish: " + qoshish(10, 5)); // "Qo'shish: 15" chiqadi
console.log("Ayirish: " + ayirish(10, 5)); // "Ayirish: 5" chiqadi
console.log("Ko'paytirish: " + kopaytirish(10, 5)); // "Ko'paytirish: 50" chiqadi
```

</details>

<details>
    <summary>Parametrlar va return</summary>

## 11.3 Parametrlar va Return

### Parametrlar nima?

**Parametrlar** - funksiyaga ma'lumot yuborish uchun ishlatiladi. Funksiya chaqirilganda parametrlar qiymat oladi.

### Parametrlar bilan ishlash

#### 1. Bitta parametr
```javascript
function salom(ism) {
    console.log("Salom, " + ism + "!");
}

salom("Ahmad"); // "Salom, Ahmad!" chiqadi
```

#### 2. Bir nechta parametr
```javascript
function toliqSalom(ism, familiya) {
    console.log("Salom, " + ism + " " + familiya + "!");
}

toliqSalom("Ahmad", "Karimov"); // "Salom, Ahmad Karimov!" chiqadi
```

#### 3. Parametrlar bo'lmasa
```javascript
function salom() {
    console.log("Salom, dunyo!");
}

salom(); // "Salom, dunyo!" chiqadi
```

### Return nima?

**Return** - funksiyadan natija qaytarish uchun ishlatiladi. Funksiya bajarilgandan keyin qiymat qaytaradi.

### Return bilan ishlash

#### 1. Oddiy return
```javascript
function qoshish(a, b) {
    return a + b;
}

let natija = qoshish(5, 3);
console.log(natija); // 8 chiqadi
```

#### 2. Return bo'lmasa
```javascript
function salom(ism) {
    console.log("Salom, " + ism + "!");
    // Return yo'q - undefined qaytadi
}

let natija = salom("Ahmad");
console.log(natija); // undefined chiqadi
```

#### 3. Erta return
```javascript
function musbatSon(son) {
    if (son < 0) {
        return "Manfiy son";
    }
    return "Musbat son";
}

console.log(musbatSon(5)); // "Musbat son"
console.log(musbatSon(-3)); // "Manfiy son"
```

### Amaliy misol - Parametrlar va return
```javascript
// 1. Bitta parametr
function salom(ism) {
    return "Salom, " + ism + "!";
}

// Funksiyani chaqirish
let natija1 = salom("Ahmad");
console.log(natija1); // "Salom, Ahmad!" chiqadi

// 2. Ikki parametr
function toliqSalom(ism, familiya) {
    return "Salom, " + ism + " " + familiya + "!";
}

// Funksiyani chaqirish
let natija2 = toliqSalom("Ahmad", "Karimov");
console.log(natija2); // "Salom, Ahmad Karimov!" chiqadi

// 3. Matematik funksiya
function qoshish(a, b) {
    return a + b;
}

// Funksiyani chaqirish
let son1 = 10;
let son2 = 5;
let natija3 = son1 + " + " + son2 + " = " + qoshish(son1, son2);
console.log(natija3); // "10 + 5 = 15" chiqadi

// 4. Return bo'lmagan funksiya
function salomConsole(ism) {
    console.log("Salom, " + ism + "!");
    // Return yo'q
}

// Funksiyani chaqirish
let natija4 = salomConsole("Ahmad");
console.log("Natija: " + natija4); // "Natija: undefined" chiqadi

// 5. Erta return
function musbatSon(son) {
    if (son < 0) {
        return "Manfiy son";
    }
    return "Musbat son";
}

// Funksiyani chaqirish
let natija5 = musbatSon(5);
console.log("5 - " + natija5); // "5 - Musbat son" chiqadi

let natija6 = musbatSon(-3);
console.log("-3 - " + natija6); // "-3 - Manfiy son" chiqadi
```

</details>

<details>
    <summary>Alert, prompt va confirm</summary>

## 11.4 Alert, Prompt va Confirm

### Alert, prompt va confirm nima?

Bu JavaScript ning built-in (tayyor) funksiyalari bo'lib, foydalanuvchi bilan muloqot qilish uchun ishlatiladi.

### Alert - xabar ko'rsatish

**Alert** - foydalanuvchiga xabar ko'rsatadi va "OK" tugmasini bosguncha kutadi.

#### Alert sintaksisi
```javascript
alert("Xabar matni");
```

#### Alert misollari
```javascript
alert("Salom, dunyo!");
alert("Xato yuz berdi!");
alert("Muvaffaqiyatli saqlandi!");
```

### Prompt - ma'lumot olish

**Prompt** - foydalanuvchidan matn kiritishni so'raydi va kiritilgan matnni qaytaradi.

#### Prompt sintaksisi
```javascript
let javob = prompt("Savol matni", "Standart qiymat");
```

#### Prompt misollari
```javascript
let ism = prompt("Ismingizni kiriting:");
let yosh = prompt("Yoshingizni kiriting:", "18");
let shahar = prompt("Qaysi shaharda yashaysiz?");
```

### Confirm - tasdiqlash

**Confirm** - foydalanuvchidan "Ha" yoki "Yo'q" javobini so'raydi.

#### Confirm sintaksisi
```javascript
let javob = confirm("Savol matni");
```

#### Confirm misollari
```javascript
let tasdiq = confirm("Haqiqatan ham o'chirmoqchimisiz?");
let saqlash = confirm("Ma'lumotlarni saqlaymizmi?");
let chiqish = confirm("Dasturdan chiqmoqchimisiz?");
```

### Amaliy misol - Alert, prompt va confirm
```javascript
// 1. Alert test
function testAlert() {
    alert("Bu alert xabari! OK tugmasini bosing.");
    console.log("Alert ko'rsatildi va yopildi.");
}

// Funksiyani chaqirish
testAlert();

// 2. Prompt test
function testPrompt() {
    let ism = prompt("Ismingizni kiriting:", "Ahmad");
    if (ism) {
        console.log("Sizning ismingiz: " + ism);
    } else {
        console.log("Siz bekor qildingiz.");
    }
}

// Funksiyani chaqirish
testPrompt();

// 3. Confirm test
function testConfirm() {
    let tasdiq = confirm("Haqiqatan ham o'chirmoqchimisiz?");
    if (tasdiq) {
        console.log("Siz 'Ha' tugmasini bosdingiz.");
    } else {
        console.log("Siz 'Yo'q' tugmasini bosdingiz.");
    }
}

// Funksiyani chaqirish
testConfirm();

// 4. Kombinatsiya - Foydalanuvchi ma'lumotlari
function foydalanuvchiMa'lumotlari() {
    let ism = prompt("Ismingizni kiriting:");
    if (!ism) {
        console.log("Siz bekor qildingiz.");
        return;
    }
    
    let yosh = prompt("Yoshingizni kiriting:");
    if (!yosh) {
        console.log("Siz bekor qildingiz.");
        return;
    }
    
    let tasdiq = confirm("Ma'lumotlar to'g'rimi?\nIsm: " + ism + "\nYosh: " + yosh);
    if (tasdiq) {
        console.log("Ma'lumotlar tasdiqlandi:");
        console.log("Ism: " + ism);
        console.log("Yosh: " + yosh);
    } else {
        console.log("Ma'lumotlar tasdiqlanmadi.");
    }
}

// Funksiyani chaqirish
foydalanuvchiMa'lumotlari();
```

</details>

<details>
    <summary>HTML elementlari bilan ishlash</summary>

## 11.5 HTML Elementlari bilan Ishlash

### HTML elementlari bilan ishlash

JavaScript yordamida HTML elementlarini o'zgartirish, yangi elementlar qo'shish va mavjud elementlarni o'chirish mumkin.

### Elementlarni topish

#### 1. getElementById
```javascript
let element = document.getElementById("elementId");
```

#### 2. getElementsByClassName
```javascript
let elementlar = document.getElementsByClassName("className");
```

#### 3. getElementsByTagName
```javascript
let elementlar = document.getElementsByTagName("div");
```

### Elementlarni o'zgartirish

#### 1. innerHTML - ichki mazmun
```javascript
document.getElementById("demo").innerHTML = "Yangi matn";
```

#### 2. innerText - faqat matn
```javascript
document.getElementById("demo").innerText = "Yangi matn";
```

#### 3. style - stillar
```javascript
document.getElementById("demo").style.color = "red";
document.getElementById("demo").style.fontSize = "20px";
```

### Elementlarni qo'shish va o'chirish

#### 1. createElement - yangi element yaratish
```javascript
let yangiElement = document.createElement("div");
```

#### 2. appendChild - element qo'shish
```javascript
document.getElementById("container").appendChild(yangiElement);
```

#### 3. removeChild - element o'chirish
```javascript
document.getElementById("container").removeChild(element);
```

### Amaliy misol - HTML elementlari
```javascript
// Eslatma: Bu misollar DOM (Document Object Model) haqida
// DOM keyingi darslarda o'rganiladi
// Hozircha faqat console.log va alert ishlatamiz

// 1. Matn o'zgartirish funksiyasi
function matnOzgartir() {
    console.log("Matn o'zgartirish funksiyasi chaqirildi");
    console.log("Hozirgi vaqt: " + new Date().toLocaleTimeString());
}

// Funksiyani chaqirish
matnOzgartir();

// 2. Rang o'zgartirish funksiyasi
function rangOzgartir() {
    let ranglar = ["qizil", "ko'k", "yashil", "binafsha", "apelsin"];
    let tasodifiyRang = ranglar[Math.floor(Math.random() * ranglar.length)];
    console.log("Tasodifiy rang: " + tasodifiyRang);
    alert("Rang o'zgartirildi: " + tasodifiyRang);
}

// Funksiyani chaqirish
rangOzgartir();

// 3. Yangi element qo'shish funksiyasi
function yangiElementQoshish() {
    let elementRaqami = Math.floor(Math.random() * 100) + 1;
    let hozirgiVaqt = new Date().toLocaleTimeString();
    console.log("Yangi element " + elementRaqami + " - " + hozirgiVaqt);
    alert("Yangi element qo'shildi: " + elementRaqami);
}

// Funksiyani chaqirish
yangiElementQoshish();

// 4. Elementlarni topish funksiyasi
function elementlarniTopish() {
    console.log("Elementlarni topish funksiyasi chaqirildi");
    console.log("Bu funksiya keyingi darslarda o'rganiladi");
    alert("Elementlarni topish - keyingi darsda!");
}

// Funksiyani chaqirish
elementlarniTopish();
```

</details>
