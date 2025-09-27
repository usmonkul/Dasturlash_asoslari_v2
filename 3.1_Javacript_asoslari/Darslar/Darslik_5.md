<details>
    <summary>Obyekt nima?</summary>

## 14.1 Obyekt nima?

### Obyekt nima?

**Obyekt** - JavaScript da ma'lumotlarni bir-biriga bog'langan xususiyatlar (properties) va metodlar (methods) sifatida saqlash uchun ishlatiladi. Obyekt real dunyodagi narsalarni ifodalash uchun juda qulay.

### Obyekt tushunchasi

#### 1. Real hayot misoli
Agar biz mashina haqida gapirsak:
- **Xususiyatlar:** rang, model, yil, tezlik
- **Metodlar:** ishga tushirish, to'xtatish, tezlashtirish

#### 2. JavaScript obyekti
```javascript
let mashina = {
    rang: "qizil",
    model: "Toyota",
    yil: 2020,
    tezlik: 0,
    ishgaTushirish: function() {
        console.log("Mashina ishga tushdi!");
    }
};
```

### Obyekt xususiyatlari

#### 1. Xususiyatlar
- Obyekt ichidagi ma'lumotlar
- `kalit: qiymat` formatida yoziladi
- Har xil turdagi qiymatlar bo'lishi mumkin

#### 2. Metodlar
- Obyekt ichidagi funksiyalar
- Obyekt bilan bog'liq harakatlar
- `kalit: function()` formatida yoziladi

### Obyekt yaratish usullari

#### 1. Object literal (eng keng tarqalgan)
```javascript
let talaba = {
    ism: "Ahmad",
    yosh: 15,
    shahar: "Toshkent"
};
```

#### 2. Object konstruktori
```javascript
let talaba = new Object();
talaba.ism = "Ahmad";
talaba.yosh = 15;
talaba.shahar = "Toshkent";
```

#### 3. Object.create()
```javascript
let talaba = Object.create(null);
talaba.ism = "Ahmad";
talaba.yosh = 15;
talaba.shahar = "Toshkent";
```

### Amaliy misol - Obyekt asoslari
```javascript
// 1. Oddiy obyekt
let kitob = {
    nom: "JavaScript asoslari",
    muallif: "Ahmad Karimov",
    yil: 2023,
    sahifalar: 250,
    narx: 50000
};

console.log("Kitob nomi:", kitob.nom);
console.log("Muallif:", kitob.muallif);
console.log("Narx:", kitob.narx + " so'm");

// 2. Obyekt xususiyatlarini o'qish
let talaba = {
    ism: "Karim",
    familiya: "Abdullayev",
    yosh: 14,
    sinf: 9,
    shahar: "Samarqand",
    sevimliFan: "Matematika"
};

console.log("Talaba haqida ma'lumot:");
console.log("Ism:", talaba.ism);
console.log("Familiya:", talaba.familiya);
console.log("To'liq ism:", talaba.ism + " " + talaba.familiya);
console.log("Yosh:", talaba.yosh);
console.log("Sinf:", talaba.sinf);
console.log("Shahar:", talaba.shahar);
console.log("Sevimli fan:", talaba.sevimliFan);

// 3. Obyekt xususiyatlarini o'zgartirish
let mashina = {
    model: "Chevrolet",
    rang: "oq",
    yil: 2018,
    tezlik: 0
};

console.log("Boshlang'ich holat:", mashina);

mashina.rang = "qizil";
mashina.tezlik = 60;

console.log("O'zgartirilgan holat:", mashina);
console.log("Yangi rang:", mashina.rang);
console.log("Yangi tezlik:", mashina.tezlik);

// 4. Yangi xususiyat qo'shish
let uy = {
    manzil: "Chilonzor tumani",
    xonalar: 3,
    qavat: 5
};

console.log("Boshlang'ich uy:", uy);

uy.maydon = 120; // Yangi xususiyat
uy.remont = "yangi"; // Yangi xususiyat

console.log("Yangi xususiyatlar bilan:", uy);
console.log("Maydon:", uy.maydon + " kv.m");
console.log("Remont holati:", uy.remont);

// 5. Xususiyatni o'chirish
let telefon = {
    model: "iPhone",
    rang: "qora",
    xotira: "128GB",
    narx: 8000000
};

console.log("Boshlang'ich telefon:", telefon);

delete telefon.narx; // Xususiyatni o'chirish

console.log("Narx o'chirilgandan keyin:", telefon);
console.log("Narx mavjudmi?", telefon.narx !== undefined);

// 6. Obyekt xususiyatlarini tekshirish
let meva = {
    nom: "olma",
    rang: "qizil",
    ta'm: "shirin",
    vitaminlar: ["C", "A", "K"]
};

// Xususiyat mavjudligini tekshirish
console.log("Nom mavjudmi?", "nom" in meva);
console.log("Hajm mavjudmi?", "hajm" in meva);

// Xususiyat qiymatini tekshirish
console.log("Ta'm mavjudmi?", meva.ta'm !== undefined);
console.log("Ta'm qiymati:", meva.ta'm);

// 7. Obyekt ichida obyekt
let maktab = {
    nom: "15-sonli maktab",
    manzil: {
        shahar: "Toshkent",
        tuman: "Yunusobod",
        ko'cha: "Amir Temur ko'chasi"
    },
    oquvchilar: 500,
    oqituvchilar: 25
};

console.log("Maktab haqida:");
console.log("Nom:", maktab.nom);
console.log("Shahar:", maktab.manzil.shahar);
console.log("Tuman:", maktab.manzil.tuman);
console.log("Ko'cha:", maktab.manzil.ko'cha);
console.log("O'quvchilar soni:", maktab.oquvchilar);
console.log("O'qituvchilar soni:", maktab.oqituvchilar);

// 8. Massiv ichida obyektlar
let oquvchilar = [
    { ism: "Ahmad", yosh: 14, sinf: 9 },
    { ism: "Karim", yosh: 15, sinf: 10 },
    { ism: "Sardor", yosh: 13, sinf: 8 }
];

console.log("O'quvchilar ro'yxati:");
for (let i = 0; i < oquvchilar.length; i++) {
    let oquvchi = oquvchilar[i];
    console.log((i + 1) + ". " + oquvchi.ism + " - " + oquvchi.yosh + " yosh, " + oquvchi.sinf + "-sinf");
}

// 9. Obyekt xususiyatlarini sanash
let kompyuter = {
    protsessor: "Intel i5",
    xotira: "8GB",
    qattiqDisk: "256GB SSD",
    ekran: "15.6 inch",
    rang: "kumush"
};

let xususiyatlarSoni = 0;
for (let kalit in kompyuter) {
    xususiyatlarSoni++;
    console.log(kalit + ": " + kompyuter[kalit]);
}

console.log("Jami xususiyatlar soni:", xususiyatlarSoni);

// 10. Obyekt nusxasini olish
let originalObyekt = {
    nom: "test",
    qiymat: 100,
    holat: "faol"
};

let nusxaObyekt = {};
for (let kalit in originalObyekt) {
    nusxaObyekt[kalit] = originalObyekt[kalit];
}

console.log("Original obyekt:", originalObyekt);
console.log("Nusxa obyekt:", nusxaObyekt);

// Nusxani o'zgartirish originalni ta'sir qilmasligi
nusxaObyekt.qiymat = 200;
console.log("Original qiymat:", originalObyekt.qiymat);
console.log("Nusxa qiymat:", nusxaObyekt.qiymat);
```

### Obyekt maslahatlari

#### 1. Obyekt yaratish
- Object literal dan foydalaning
- Aniq va tushunarli xususiyat nomlarini yozing
- Ma'lumotlarni mantiqiy guruhlang

#### 2. Xususiyatlarga murojaat
- Nuqta notatsiyasi (.) qulayroq
- Qavs notatsiyasi [] dinamik uchun
- Xususiyat mavjudligini tekshiring

#### 3. Kod soddaligi
- Obyektlarni kichik va fokusli qiling
- Keraksiz xususiyatlarni olib tashlang
- Aniq nomlar va izohlarni qo'shing

</details>

<details>
    <summary>Obyekt yaratish va xususiyatlar</summary>

## 14.2 Obyekt Yaratish va Xususiyatlar

### Obyekt yaratish usullari

#### 1. Object literal (eng keng tarqalgan)
```javascript
let talaba = {
    ism: "Ahmad",
    yosh: 15,
    sinf: 9
};
```

#### 2. Object konstruktori
```javascript
let talaba = new Object();
talaba.ism = "Ahmad";
talaba.yosh = 15;
talaba.sinf = 9;
```

#### 3. Object.create()
```javascript
let talaba = Object.create(null);
talaba.ism = "Ahmad";
talaba.yosh = 15;
talaba.sinf = 9;
```

### Xususiyatlarga murojaat qilish

#### 1. Nuqta notatsiyasi (.)
```javascript
let talaba = { ism: "Ahmad", yosh: 15 };
console.log(talaba.ism); // "Ahmad"
console.log(talaba.yosh); // 15
```

#### 2. Qavs notatsiyasi []
```javascript
let talaba = { ism: "Ahmad", yosh: 15 };
console.log(talaba["ism"]); // "Ahmad"
console.log(talaba["yosh"]); // 15
```

#### 3. Qavs notatsiyasining afzalliklari
- O'zgaruvchi bilan ishlash
- Maxsus belgilar bilan ishlash
- Dinamik xususiyat nomlari

### Xususiyatlarni o'zgartirish

#### 1. Mavjud xususiyatni o'zgartirish
```javascript
let talaba = { ism: "Ahmad", yosh: 15 };
talaba.yosh = 16; // O'zgartirish
console.log(talaba.yosh); // 16
```

#### 2. Yangi xususiyat qo'shish
```javascript
let talaba = { ism: "Ahmad" };
talaba.yosh = 15; // Yangi xususiyat
talaba.sinf = 9; // Yangi xususiyat
```

#### 3. Xususiyatni o'chirish
```javascript
let talaba = { ism: "Ahmad", yosh: 15 };
delete talaba.yosh; // O'chirish
console.log(talaba.yosh); // undefined
```

### Xususiyat mavjudligini tekshirish

#### 1. in operatori
```javascript
let talaba = { ism: "Ahmad", yosh: 15 };
console.log("ism" in talaba); // true
console.log("sinf" in talaba); // false
```

#### 2. undefined tekshiruvi
```javascript
let talaba = { ism: "Ahmad", yosh: 15 };
console.log(talaba.ism !== undefined); // true
console.log(talaba.sinf !== undefined); // false
```

#### 3. hasOwnProperty() metodi
```javascript
let talaba = { ism: "Ahmad", yosh: 15 };
console.log(talaba.hasOwnProperty("ism")); // true
console.log(talaba.hasOwnProperty("sinf")); // false
```

### Amaliy misol - Obyekt yaratish va xususiyatlar
```javascript
// 1. Oddiy obyekt yaratish
let kitob = {
    nom: "JavaScript asoslari",
    muallif: "Ahmad Karimov",
    yil: 2023,
    sahifalar: 250,
    narx: 50000,
    til: "o'zbek"
};

console.log("Kitob haqida ma'lumot:");
console.log("Nom:", kitob.nom);
console.log("Muallif:", kitob.muallif);
console.log("Yil:", kitob.yil);
console.log("Sahifalar:", kitob.sahifalar);
console.log("Narx:", kitob.narx + " so'm");
console.log("Til:", kitob.til);

// 2. Xususiyatlarni o'zgartirish
let telefon = {
    model: "Samsung Galaxy",
    rang: "qora",
    xotira: "64GB",
    narx: 3000000
};

console.log("Boshlang'ich telefon:", telefon);

telefon.rang = "oq"; // Rangni o'zgartirish
telefon.xotira = "128GB"; // Xotirani o'zgartirish
telefon.narx = 3500000; // Narxni o'zgartirish

console.log("O'zgartirilgan telefon:", telefon);

// 3. Yangi xususiyatlar qo'shish
let uy = {
    manzil: "Chilonzor tumani",
    xonalar: 3
};

console.log("Boshlang'ich uy:", uy);

uy.qavat = 5; // Yangi xususiyat
uy.maydon = 120; // Yangi xususiyat
uy.remont = "yangi"; // Yangi xususiyat
uy.parkovka = true; // Boolean xususiyat

console.log("Yangi xususiyatlar bilan:", uy);
console.log("Qavat:", uy.qavat);
console.log("Maydon:", uy.maydon + " kv.m");
console.log("Remont:", uy.remont);
console.log("Parkovka:", uy.parkovka ? "Bor" : "Yo'q");

// 4. Xususiyatlarni o'chirish
let mashina = {
    model: "Chevrolet",
    rang: "oq",
    yil: 2018,
    tezlik: 0,
    yoqilgi: "benzin"
};

console.log("Boshlang'ich mashina:", mashina);

delete mashina.tezlik; // Xususiyatni o'chirish
delete mashina.yoqilgi; // Xususiyatni o'chirish

console.log("Xususiyatlar o'chirilgandan keyin:", mashina);
console.log("Tezlik mavjudmi?", "tezlik" in mashina);
console.log("Yoqilgi mavjudmi?", "yoqilgi" in mashina);

// 5. Xususiyat mavjudligini tekshirish
let talaba = {
    ism: "Karim",
    familiya: "Abdullayev",
    yosh: 14,
    sinf: 9,
    shahar: "Samarqand"
};

// in operatori bilan tekshirish
console.log("Ism mavjudmi?", "ism" in talaba);
console.log("Telefon mavjudmi?", "telefon" in talaba);

// undefined tekshiruvi
console.log("Familiya mavjudmi?", talaba.familiya !== undefined);
console.log("Email mavjudmi?", talaba.email !== undefined);

// hasOwnProperty() metodi
console.log("Yosh mavjudmi?", talaba.hasOwnProperty("yosh"));
console.log("Adres mavjudmi?", talaba.hasOwnProperty("adres"));

// 6. Qavs notatsiyasi bilan ishlash
let meva = {
    nom: "olma",
    rang: "qizil",
    ta'm: "shirin",
    vitaminlar: ["C", "A", "K"]
};

// O'zgaruvchi bilan ishlash
let xususiyatNom = "nom";
console.log("Meva nomi:", meva[xususiyatNom]);

let xususiyatRang = "rang";
console.log("Meva rangi:", meva[xususiyatRang]);

// Dinamik xususiyat nomlari
let xususiyatlar = ["nom", "rang", "ta'm"];
for (let i = 0; i < xususiyatlar.length; i++) {
    let xususiyat = xususiyatlar[i];
    console.log(xususiyat + ":", meva[xususiyat]);
}

// 7. Maxsus belgilar bilan ishlash
let maxsusObyekt = {
    "maxsus-xususiyat": "bu maxsus",
    "123": "raqam bilan boshlangan",
    "spase li": "bo'shliq bilan"
};

console.log("Maxsus xususiyat:", maxsusObyekt["maxsus-xususiyat"]);
console.log("Raqam xususiyat:", maxsusObyekt["123"]);
console.log("Bo'shliq xususiyat:", maxsusObyekt["spase li"]);

// 8. Obyekt ichida obyekt
let maktab = {
    nom: "15-sonli maktab",
    manzil: {
        shahar: "Toshkent",
        tuman: "Yunusobod",
        ko'cha: "Amir Temur ko'chasi",
        uy: "15"
    },
    oquvchilar: 500,
    oqituvchilar: 25,
    sinflar: {
        boshlangich: 12,
        o'rta: 8,
        katta: 4
    }
};

console.log("Maktab haqida:");
console.log("Nom:", maktab.nom);
console.log("Shahar:", maktab.manzil.shahar);
console.log("Tuman:", maktab.manzil.tuman);
console.log("To'liq manzil:", maktab.manzil.shahar + ", " + maktab.manzil.tuman + ", " + maktab.manzil.ko'cha + ", " + maktab.manzil.uy);
console.log("O'quvchilar:", maktab.oquvchilar);
console.log("O'qituvchilar:", maktab.oqituvchilar);
console.log("Boshlang'ich sinflar:", maktab.sinflar.boshlangich);
console.log("O'rta sinflar:", maktab.sinflar.o'rta);
console.log("Katta sinflar:", maktab.sinflar.katta);

// 9. Massiv ichida obyektlar
let oquvchilar = [
    { ism: "Ahmad", yosh: 14, sinf: 9, baholar: [5, 4, 5] },
    { ism: "Karim", yosh: 15, sinf: 10, baholar: [4, 5, 4] },
    { ism: "Sardor", yosh: 13, sinf: 8, baholar: [5, 5, 5] }
];

console.log("O'quvchilar ro'yxati:");
for (let i = 0; i < oquvchilar.length; i++) {
    let oquvchi = oquvchilar[i];
    console.log((i + 1) + ". " + oquvchi.ism + " - " + oquvchi.yosh + " yosh, " + oquvchi.sinf + "-sinf");
    console.log("   Baholar:", oquvchi.baholar.join(", "));
}

// 10. Obyekt xususiyatlarini sanash va ko'rsatish
let kompyuter = {
    protsessor: "Intel i5",
    xotira: "8GB",
    qattiqDisk: "256GB SSD",
    ekran: "15.6 inch",
    rang: "kumush",
    narx: 6000000
};

console.log("Kompyuter xususiyatlari:");
let xususiyatlarSoni = 0;
for (let kalit in kompyuter) {
    xususiyatlarSoni++;
    console.log(kalit + ": " + kompyuter[kalit]);
}

console.log("Jami xususiyatlar soni:", xususiyatlarSoni);

// 11. Obyekt nusxasini olish
let originalObyekt = {
    nom: "test",
    qiymat: 100,
    holat: "faol",
    sozlamalar: {
        til: "o'zbek",
        rang: "qizil"
    }
};

let nusxaObyekt = {};
for (let kalit in originalObyekt) {
    if (typeof originalObyekt[kalit] === "object") {
        nusxaObyekt[kalit] = {};
        for (let ichkiKalit in originalObyekt[kalit]) {
            nusxaObyekt[kalit][ichkiKalit] = originalObyekt[kalit][ichkiKalit];
        }
    } else {
        nusxaObyekt[kalit] = originalObyekt[kalit];
    }
}

console.log("Original obyekt:", originalObyekt);
console.log("Nusxa obyekt:", nusxaObyekt);

// Nusxani o'zgartirish originalni ta'sir qilmasligi
nusxaObyekt.qiymat = 200;
nusxaObyekt.sozlamalar.til = "ingliz";
console.log("Original qiymat:", originalObyekt.qiymat);
console.log("Nusxa qiymat:", nusxaObyekt.qiymat);
console.log("Original til:", originalObyekt.sozlamalar.til);
console.log("Nusxa til:", nusxaObyekt.sozlamalar.til);
```

### Obyekt yaratish va xususiyatlar maslahatlari

#### 1. Obyekt yaratish
- Object literal dan foydalaning
- Aniq va tushunarli xususiyat nomlarini yozing
- Ma'lumotlarni mantiqiy guruhlang

#### 2. Xususiyatlarga murojaat
- Nuqta notatsiyasi (.) qulayroq
- Qavs notatsiyasi [] dinamik uchun
- Xususiyat mavjudligini tekshiring

#### 3. Xususiyatlarni boshqarish
- Yangi xususiyatlarni qo'shing
- Keraksiz xususiyatlarni olib tashlang
- Xususiyat mavjudligini tekshiring

</details>

<details>
    <summary>Obyekt metodlari</summary>

## 14.3 Obyekt Metodlari

### Obyekt metodi nima?

**Metod** - obyekt ichidagi funksiya. U obyekt bilan bog'liq harakatlarni bajaradi va obyekt xususiyatlariga kirish imkonini beradi.

### Metod yaratish

#### 1. Asosiy metod yaratish
```javascript
let talaba = {
    ism: "Ahmad",
    yosh: 15,
    salomlashish: function() {
        return "Salom, men " + this.ism + "!";
    }
};
```

#### 2. Metodni chaqirish
```javascript
let xabar = talaba.salomlashish();
console.log(xabar); // "Salom, men Ahmad!"
```

#### 3. this kalit so'zi
- Obyektning o'ziga murojaat qiladi
- Metod ichida obyekt xususiyatlariga kirish
- Kontekstga bog'liq

### Metod turlari

#### 1. Oddiy metodlar
```javascript
let mashina = {
    tezlik: 0,
    tezlashtirish: function() {
        this.tezlik += 10;
        return "Tezlik: " + this.tezlik + " km/h";
    }
};
```

#### 2. Parametrli metodlar
```javascript
let kalkulyator = {
    yigindi: function(a, b) {
        return a + b;
    },
    ayirma: function(a, b) {
        return a - b;
    }
};
```

#### 3. Shartli metodlar
```javascript
let hisoblagich = {
    qiymat: 0,
    oshirish: function() {
        this.qiymat++;
        return this.qiymat;
    },
    kamaytirish: function() {
        if (this.qiymat > 0) {
            this.qiymat--;
        }
        return this.qiymat;
    }
};
```

### Amaliy misol - Obyekt metodlari
```javascript
// 1. Oddiy metodlar
let talaba = {
    ism: "Karim",
    yosh: 14,
    sinf: 9,
    baholar: [5, 4, 5, 4, 5],
    
    salomlashish: function() {
        return "Salom, men " + this.ism + "!";
    },
    
    maqomniKo'rsatish: function() {
        return this.ism + " - " + this.sinf + "-sinf o'quvchisi";
    },
    
    o'rtachaBahoniHisoblash: function() {
        let yigindi = 0;
        for (let i = 0; i < this.baholar.length; i++) {
            yigindi += this.baholar[i];
        }
        return yigindi / this.baholar.length;
    }
};

console.log("Talaba haqida:");
console.log(talaba.salomlashish());
console.log(talaba.maqomniKo'rsatish());
console.log("O'rtacha baho:", talaba.o'rtachaBahoniHisoblash().toFixed(2));

// 2. Parametrli metodlar
let kalkulyator = {
    yigindi: function(a, b) {
        return a + b;
    },
    ayirma: function(a, b) {
        return a - b;
    },
    ko'paytma: function(a, b) {
        return a * b;
    },
    bo'lish: function(a, b) {
        if (b !== 0) {
            return a / b;
        } else {
            return "Nolga bo'lish mumkin emas!";
        }
    },
    amalniBajarish: function(amal, a, b) {
        switch (amal) {
            case "+":
                return this.yigindi(a, b);
            case "-":
                return this.ayirma(a, b);
            case "*":
                return this.ko'paytma(a, b);
            case "/":
                return this.bo'lish(a, b);
            default:
                return "Noto'g'ri amal!";
        }
    }
};

console.log("\nKalkulyator misollari:");
console.log("10 + 5 =", kalkulyator.yigindi(10, 5));
console.log("10 - 5 =", kalkulyator.ayirma(10, 5));
console.log("10 * 5 =", kalkulyator.ko'paytma(10, 5));
console.log("10 / 5 =", kalkulyator.bo'lish(10, 5));
console.log("10 / 0 =", kalkulyator.bo'lish(10, 0));
console.log("Amal: 15 + 25 =", kalkulyator.amalniBajarish("+", 15, 25));

// 3. Shartli metodlar
let hisoblagich = {
    qiymat: 0,
    maksimal: 100,
    minimal: 0,
    
    oshirish: function() {
        if (this.qiymat < this.maksimal) {
            this.qiymat++;
            return "Qiymat oshdi: " + this.qiymat;
        } else {
            return "Maksimal qiymatga yetildi!";
        }
    },
    
    kamaytirish: function() {
        if (this.qiymat > this.minimal) {
            this.qiymat--;
            return "Qiymat kamaydi: " + this.qiymat;
        } else {
            return "Minimal qiymatga yetildi!";
        }
    },
    
    nolgaQaytarish: function() {
        this.qiymat = 0;
        return "Qiymat nolga qaytarildi!";
    },
    
    qiymatniO'rnatish: function(yangiQiymat) {
        if (yangiQiymat >= this.minimal && yangiQiymat <= this.maksimal) {
            this.qiymat = yangiQiymat;
            return "Qiymat o'rnatildi: " + this.qiymat;
        } else {
            return "Noto'g'ri qiymat! " + this.minimal + " dan " + this.maksimal + " gacha bo'lishi kerak.";
        }
    },
    
    holatniKo'rsatish: function() {
        return "Hozirgi qiymat: " + this.qiymat + " (min: " + this.minimal + ", max: " + this.maksimal + ")";
    }
};

console.log("\nHisoblagich misollari:");
console.log(hisoblagich.holatniKo'rsatish());
console.log(hisoblagich.oshirish());
console.log(hisoblagich.oshirish());
console.log(hisoblagich.oshirish());
console.log(hisoblagich.kamaytirish());
console.log(hisoblagich.qiymatniO'rnatish(50));
console.log(hisoblagich.qiymatniO'rnatish(150)); // Xato
console.log(hisoblagich.nolgaQaytarish());

// 4. Obyekt ichida obyekt bilan ishlash
let maktab = {
    nom: "15-sonli maktab",
    oquvchilar: 500,
    oqituvchilar: 25,
    sinflar: {
        boshlangich: 12,
        o'rta: 8,
        katta: 4
    },
    
    umumiyMaqomniKo'rsatish: function() {
        return this.nom + " - " + this.oquvchilar + " ta o'quvchi, " + this.oqituvchilar + " ta o'qituvchi";
    },
    
    sinflarniHisoblash: function() {
        return this.sinflar.boshlangich + this.sinflar.o'rta + this.sinflar.katta;
    },
    
    o'quvchiQo'shish: function() {
        this.oquvchilar++;
        return "Yangi o'quvchi qo'shildi. Jami: " + this.oquvchilar;
    },
    
    o'quvchiOlibTashlash: function() {
        if (this.oquvchilar > 0) {
            this.oquvchilar--;
            return "O'quvchi olib tashlandi. Jami: " + this.oquvchilar;
        } else {
            return "O'quvchilar yo'q!";
        }
    },
    
    toliqMaqomniKo'rsatish: function() {
        return this.umumiyMaqomniKo'rsatish() + ", " + this.sinflarniHisoblash() + " ta sinf";
    }
};

console.log("\nMaktab haqida:");
console.log(maktab.umumiyMaqomniKo'rsatish());
console.log("Sinflar soni:", maktab.sinflarniHisoblash());
console.log(maktab.o'quvchiQo'shish());
console.log(maktab.o'quvchiOlibTashlash());
console.log(maktab.toliqMaqomniKo'rsatish());

// 5. Massivlar bilan ishlash
let kutubxona = {
    nom: "Shahar kutubxonasi",
    kitoblar: [
        { nom: "JavaScript asoslari", muallif: "Ahmad Karimov", yil: 2023 },
        { nom: "HTML va CSS", muallif: "Karim Abdullayev", yil: 2022 },
        { nom: "Python dasturlash", muallif: "Sardor Rahimov", yil: 2023 }
    ],
    
    kitoblarSoni: function() {
        return this.kitoblar.length;
    },
    
    kitobQo'shish: function(nom, muallif, yil) {
        let yangiKitob = { nom: nom, muallif: muallif, yil: yil };
        this.kitoblar.push(yangiKitob);
        return "Kitob qo'shildi: " + nom;
    },
    
    kitobniTopish: function(nom) {
        for (let i = 0; i < this.kitoblar.length; i++) {
            if (this.kitoblar[i].nom === nom) {
                return this.kitoblar[i];
            }
        }
        return "Kitob topilmadi!";
    },
    
    kitoblarRo'yxatiniKo'rsatish: function() {
        let royxat = "Kutubxona kitoblari:\n";
        for (let i = 0; i < this.kitoblar.length; i++) {
            royxat += (i + 1) + ". " + this.kitoblar[i].nom + " - " + this.kitoblar[i].muallif + " (" + this.kitoblar[i].yil + ")\n";
        }
        return royxat;
    },
    
    muallifBo'yichaQidirish: function(muallif) {
        let topilganKitoblar = [];
        for (let i = 0; i < this.kitoblar.length; i++) {
            if (this.kitoblar[i].muallif === muallif) {
                topilganKitoblar.push(this.kitoblar[i]);
            }
        }
        return topilganKitoblar;
    }
};

console.log("\nKutubxona haqida:");
console.log("Kitoblar soni:", kutubxona.kitoblarSoni());
console.log(kutubxona.kitoblarRo'yxatiniKo'rsatish());
console.log(kutubxona.kitobQo'shish("Vue.js asoslari", "Bobur Toshmatov", 2024));
console.log("Kitoblar soni:", kutubxona.kitoblarSoni());
console.log("Qidirilgan kitob:", kutubxona.kitobniTopish("JavaScript asoslari"));
console.log("Muallif kitoblari:", kutubxona.muallifBo'yichaQidirish("Ahmad Karimov"));

// 6. Metodlar ichida metodlar chaqirish
let bank = {
    nom: "O'zbekiston banki",
    mijozlar: [
        { ism: "Ahmad", balans: 1000000, karta: "1234-5678-9012-3456" },
        { ism: "Karim", balans: 500000, karta: "2345-6789-0123-4567" },
        { ism: "Sardor", balans: 2000000, karta: "3456-7890-1234-5678" }
    ],
    
    mijozniTopish: function(ism) {
        for (let i = 0; i < this.mijozlar.length; i++) {
            if (this.mijozlar[i].ism === ism) {
                return this.mijozlar[i];
            }
        }
        return null;
    },
    
    balansniKo'rsatish: function(ism) {
        let mijoz = this.mijozniTopish(ism);
        if (mijoz) {
            return ism + " ning balansi: " + mijoz.balans + " so'm";
        } else {
            return "Mijoz topilmadi!";
        }
    },
    
    pulYechish: function(ism, miqdor) {
        let mijoz = this.mijozniTopish(ism);
        if (mijoz) {
            if (mijoz.balans >= miqdor) {
                mijoz.balans -= miqdor;
                return "Pul yechildi: " + miqdor + " so'm. Qolgan balans: " + mijoz.balans + " so'm";
            } else {
                return "Balans yetarli emas!";
            }
        } else {
            return "Mijoz topilmadi!";
        }
    },
    
    pulQo'yish: function(ism, miqdor) {
        let mijoz = this.mijozniTopish(ism);
        if (mijoz) {
            mijoz.balans += miqdor;
            return "Pul qo'yildi: " + miqdor + " so'm. Yangi balans: " + mijoz.balans + " so'm";
        } else {
            return "Mijoz topilmadi!";
        }
    },
    
    pulO'tkazish: function(kimdan, kimga, miqdor) {
        let jo'natuvchi = this.mijozniTopish(kimdan);
        let qabulQiluvchi = this.mijozniTopish(kimga);
        
        if (jo'natuvchi && qabulQiluvchi) {
            if (jo'natuvchi.balans >= miqdor) {
                jo'natuvchi.balans -= miqdor;
                qabulQiluvchi.balans += miqdor;
                return "Pul o'tkazildi: " + miqdor + " so'm " + kimdan + " dan " + kimga + " ga";
            } else {
                return "Balans yetarli emas!";
            }
        } else {
            return "Mijoz topilmadi!";
        }
    }
};

console.log("\nBank operatsiyalari:");
console.log(bank.balansniKo'rsatish("Ahmad"));
console.log(bank.pulYechish("Ahmad", 200000));
console.log(bank.pulQo'yish("Karim", 100000));
console.log(bank.pulO'tkazish("Sardor", "Ahmad", 500000));
console.log(bank.balansniKo'rsatish("Ahmad"));
console.log(bank.balansniKo'rsatish("Karim"));
console.log(bank.balansniKo'rsatish("Sardor"));
```

### Obyekt metodlari maslahatlari

#### 1. Metod yaratish
- Aniq va tushunarli nomlar yozing
- this kalit so'zidan to'g'ri foydalaning
- Parametrlarni tekshiring

#### 2. Metod chaqirish
- Nuqta notatsiyasi bilan chaqiring
- Parametrlarni to'g'ri uzating
- Qaytarilgan qiymatni ishlating

#### 3. Kod soddaligi
- Metodlarni kichik va fokusli qiling
- Keraksiz metodlarni olib tashlang
- Aniq nomlar va izohlarni qo'shing

</details>

<details>
    <summary>JSON format</summary>

## 14.4 JSON Format

### JSON nima?

**JSON** (JavaScript Object Notation) - ma'lumotlarni saqlash va uzatish uchun ishlatiladigan matn format. Bu JavaScript obyektlariga juda o'xshash, lekin barcha brauzer va dasturlash tillari tomonidan qo'llab-quvvatlanadi.

### JSON xususiyatlari

#### 1. Asosiy qoidalar
- Faqat matn (string) formatida
- Kalitlar har doim qo'shtirnoq ichida
- Qiymatlar: string, number, boolean, null, array, object
- Vergul bilan ajratiladi

#### 2. JSON vs JavaScript
```javascript
// JavaScript obyekt
let talaba = {
    ism: "Ahmad",
    yosh: 15,
    sinf: 9
};

// JSON format
let jsonTalaba = '{"ism":"Ahmad","yosh":15,"sinf":9}';
```

### JSON metodlari

#### 1. JSON.stringify() - obyektni JSON ga aylantirish
```javascript
let talaba = { ism: "Ahmad", yosh: 15 };
let jsonString = JSON.stringify(talaba);
console.log(jsonString); // '{"ism":"Ahmad","yosh":15}'
```

#### 2. JSON.parse() - JSON ni obyektga aylantirish
```javascript
let jsonString = '{"ism":"Ahmad","yosh":15}';
let talaba = JSON.parse(jsonString);
console.log(talaba.ism); // "Ahmad"
```

### JSON turlari

#### 1. Oddiy qiymatlar
```json
{
    "ism": "Ahmad",
    "yosh": 15,
    "sinf": 9,
    "faol": true,
    "telefon": null
}
```

#### 2. Massivlar
```json
{
    "ism": "Ahmad",
    "baholar": [5, 4, 5, 4, 5],
    "fanlar": ["Matematika", "Fizika", "Kimyo"]
}
```

#### 3. Ichki obyektlar
```json
{
    "ism": "Ahmad",
    "manzil": {
        "shahar": "Toshkent",
        "tuman": "Yunusobod",
        "uy": "15"
    }
}
```

### Amaliy misol - JSON format
```javascript
// 1. Obyektni JSON ga aylantirish
let talaba = {
    ism: "Karim",
    yosh: 14,
    sinf: 9,
    baholar: [5, 4, 5, 4, 5],
    manzil: {
        shahar: "Samarqand",
        tuman: "Registon",
        uy: "25"
    },
    faol: true,
    telefon: null
};

let jsonString = JSON.stringify(talaba);
console.log("JSON format:");
console.log(jsonString);

// 2. JSON ni obyektga aylantirish
let yangiTalaba = JSON.parse(jsonString);
console.log("\nObyekt format:");
console.log(yangiTalaba);
console.log("Ism:", yangiTalaba.ism);
console.log("Yosh:", yangiTalaba.yosh);
console.log("Shahar:", yangiTalaba.manzil.shahar);

// 3. JSON formatini tekshirish
let toliqJson = '{"ism":"Ahmad","yosh":15,"sinf":9,"baholar":[5,4,5],"manzil":{"shahar":"Toshkent","tuman":"Yunusobod"}}';
console.log("\nTo'liq JSON:");
console.log(toliqJson);

let obyekt = JSON.parse(toliqJson);
console.log("Parsed obyekt:");
console.log(obyekt);
console.log("Baholar:", obyekt.baholar);
console.log("Manzil:", obyekt.manzil);

// 4. Massiv ichida obyektlar
let oquvchilar = [
    { ism: "Ahmad", yosh: 14, sinf: 9 },
    { ism: "Karim", yosh: 15, sinf: 10 },
    { ism: "Sardor", yosh: 13, sinf: 8 }
];

let oquvchilarJson = JSON.stringify(oquvchilar);
console.log("\nO'quvchilar JSON:");
console.log(oquvchilarJson);

let oquvchilarObyekt = JSON.parse(oquvchilarJson);
console.log("O'quvchilar obyekt:");
console.log(oquvchilarObyekt);
console.log("Birinchi o'quvchi:", oquvchilarObyekt[0].ism);

// 5. JSON xatolarini tekshirish
let notogriJson = '{"ism":"Ahmad","yosh":15,"sinf":9}'; // Noto'g'ri JSON
let toliqJson2 = '{"ism":"Ahmad","yosh":15,"sinf":9}'; // To'g'ri JSON

try {
    let obyekt1 = JSON.parse(notogriJson);
    console.log("Obyekt1:", obyekt1);
} catch (xato) {
    console.log("JSON xatosi:", xato.message);
}

try {
    let obyekt2 = JSON.parse(toliqJson2);
    console.log("Obyekt2:", obyekt2);
} catch (xato) {
    console.log("JSON xatosi:", xato.message);
}

// 6. JSON formatini chiroyli qilish
let maktab = {
    nom: "15-sonli maktab",
    oquvchilar: 500,
    oqituvchilar: 25,
    sinflar: {
        boshlangich: 12,
        o'rta: 8,
        katta: 4
    }
};

let chiroyliJson = JSON.stringify(maktab, null, 2);
console.log("\nChiroyli JSON:");
console.log(chiroyliJson);

// 7. JSON dan faqat kerakli xususiyatlarni olish
let talaba2 = {
    ism: "Bobur",
    yosh: 16,
    sinf: 10,
    telefon: "998901234567",
    email: "bobur@example.com",
    parol: "secret123"
};

// Faqat ism va yosh ni JSON ga aylantirish
let faqatKerakli = JSON.stringify(talaba2, ["ism", "yosh"]);
console.log("\nFaqat kerakli xususiyatlar:");
console.log(faqatKerakli);

// 8. JSON ni tekshirish va to'g'rilash
let notogriJson2 = '{"ism":"Ahmad","yosh":15,"sinf":9}'; // Noto'g'ri JSON
let toliqJson3 = '{"ism":"Ahmad","yosh":15,"sinf":9}'; // To'g'ri JSON

function jsonniTekshirish(jsonString) {
    try {
        let obyekt = JSON.parse(jsonString);
        console.log("JSON to'g'ri:", obyekt);
        return true;
    } catch (xato) {
        console.log("JSON noto'g'ri:", xato.message);
        return false;
    }
}

console.log("\nJSON tekshirish:");
jsonniTekshirish(notogriJson2);
jsonniTekshirish(toliqJson3);

// 9. JSON dan obyektga aylantirish va o'zgartirish
let jsonString2 = '{"ism":"Ahmad","yosh":15,"sinf":9}';
let talaba3 = JSON.parse(jsonString2);

console.log("\nO'zgartirishdan oldin:", talaba3);
talaba3.yosh = 16;
talaba3.sinf = 10;
console.log("O'zgartirishdan keyin:", talaba3);

let yangiJson = JSON.stringify(talaba3);
console.log("Yangi JSON:", yangiJson);

// 10. JSON bilan ishlash funksiyasi
function jsonBilanIshlash(obyekt) {
    // Obyektni JSON ga aylantirish
    let json = JSON.stringify(obyekt);
    console.log("JSON:", json);
    
    // JSON ni obyektga aylantirish
    let yangiObyekt = JSON.parse(json);
    console.log("Yangi obyekt:", yangiObyekt);
    
    // Obyektlarni solishtirish
    let birxil = JSON.stringify(obyekt) === JSON.stringify(yangiObyekt);
    console.log("Obyektlar bir xilmi?", birxil);
    
    return yangiObyekt;
}

let testObyekt = {
    nom: "Test",
    qiymat: 100,
    holat: "faol"
};

console.log("\nJSON bilan ishlash funksiyasi:");
jsonBilanIshlash(testObyekt);
```

### JSON maslahatlari

#### 1. JSON formatini to'g'ri yozish
- Kalitlarni qo'shtirnoq ichida yozing
- Vergullarni to'g'ri qo'ying
- Xatolarni tekshiring

#### 2. JSON metodlari
- JSON.stringify() - obyektni JSON ga
- JSON.parse() - JSON ni obyektga
- Try-catch bilan xatolarni boshqaring

#### 3. Xavfsizlik
- JSON.parse() ni ehtiyotkorlik bilan ishlating
- Foydalanuvchi kiritishini tekshiring
- Xatolarni oldini oling

</details>

<details>
    <summary>LocalStorage bilan ishlash</summary>

## 14.5 LocalStorage bilan Ishlash

### LocalStorage nima?

**LocalStorage** - brauzerda ma'lumotlarni doimiy saqlash uchun ishlatiladi. Ma'lumotlar sahifa yopilganda ham saqlanib qoladi va keyingi safar ochilganda mavjud bo'ladi.

### LocalStorage xususiyatlari

#### 1. Asosiy xususiyatlar
- Ma'lumotlar brauzerda saqlanadi
- Sahifa yopilganda ham saqlanib qoladi
- Faqat matn (string) formatida saqlaydi
- Har bir domen uchun alohida

#### 2. LocalStorage vs SessionStorage
- **LocalStorage** - doimiy saqlash
- **SessionStorage** - sessiya davomida saqlash

### LocalStorage metodlari

#### 1. setItem() - ma'lumot qo'shish
```javascript
localStorage.setItem("ism", "Ahmad");
localStorage.setItem("yosh", "15");
```

#### 2. getItem() - ma'lumot olish
```javascript
let ism = localStorage.getItem("ism");
let yosh = localStorage.getItem("yosh");
```

#### 3. removeItem() - ma'lumot o'chirish
```javascript
localStorage.removeItem("ism");
```

#### 4. clear() - barcha ma'lumotlarni o'chirish
```javascript
localStorage.clear();
```

#### 5. length - ma'lumotlar soni
```javascript
let soni = localStorage.length;
```

#### 6. key() - kalit nomini olish
```javascript
let kalit = localStorage.key(0);
```

### Obyektlarni LocalStorage da saqlash

#### 1. JSON.stringify() bilan saqlash
```javascript
let talaba = { ism: "Ahmad", yosh: 15 };
localStorage.setItem("talaba", JSON.stringify(talaba));
```

#### 2. JSON.parse() bilan olish
```javascript
let talaba = JSON.parse(localStorage.getItem("talaba"));
```

### Amaliy misol - LocalStorage bilan ishlash
```javascript
// 1. Oddiy ma'lumotlarni saqlash
localStorage.setItem("foydalanuvchi", "Ahmad");
localStorage.setItem("yosh", "15");
localStorage.setItem("shahar", "Toshkent");

console.log("Ma'lumotlar saqlandi!");

// 2. Ma'lumotlarni olish
let foydalanuvchi = localStorage.getItem("foydalanuvchi");
let yosh = localStorage.getItem("yosh");
let shahar = localStorage.getItem("shahar");

console.log("Foydalanuvchi:", foydalanuvchi);
console.log("Yosh:", yosh);
console.log("Shahar:", shahar);

// 3. Ma'lumotlarni o'zgartirish
localStorage.setItem("yosh", "16");
let yangiYosh = localStorage.getItem("yosh");
console.log("Yangi yosh:", yangiYosh);

// 4. Ma'lumotlarni o'chirish
localStorage.removeItem("shahar");
let o'chirilganShahar = localStorage.getItem("shahar");
console.log("O'chirilgan shahar:", o'chirilganShahar); // null

// 5. LocalStorage holatini tekshirish
console.log("Ma'lumotlar soni:", localStorage.length);
console.log("Birinchi kalit:", localStorage.key(0));
console.log("Ikkinchi kalit:", localStorage.key(1));

// 6. Obyektlarni saqlash
let talaba = {
    ism: "Karim",
    yosh: 14,
    sinf: 9,
    baholar: [5, 4, 5, 4, 5],
    manzil: {
        shahar: "Samarqand",
        tuman: "Registon"
    }
};

// Obyektni JSON ga aylantirib saqlash
localStorage.setItem("talaba", JSON.stringify(talaba));
console.log("Talaba ma'lumotlari saqlandi!");

// Obyektni olish
let saqlanganTalaba = JSON.parse(localStorage.getItem("talaba"));
console.log("Saqlangan talaba:", saqlanganTalaba);
console.log("Ism:", saqlanganTalaba.ism);
console.log("Baholar:", saqlanganTalaba.baholar);

// 7. Massivlarni saqlash
let oquvchilar = [
    { ism: "Ahmad", yosh: 14, sinf: 9 },
    { ism: "Karim", yosh: 15, sinf: 10 },
    { ism: "Sardor", yosh: 13, sinf: 8 }
];

localStorage.setItem("oquvchilar", JSON.stringify(oquvchilar));
console.log("O'quvchilar saqlandi!");

let saqlanganOquvchilar = JSON.parse(localStorage.getItem("oquvchilar"));
console.log("Saqlangan o'quvchilar:", saqlanganOquvchilar);
console.log("Birinchi o'quvchi:", saqlanganOquvchilar[0].ism);

// 8. LocalStorage ni tozalash
console.log("Tozalashdan oldin ma'lumotlar soni:", localStorage.length);
localStorage.clear();
console.log("Tozalashdan keyin ma'lumotlar soni:", localStorage.length);

// 9. Ma'lumot mavjudligini tekshirish
function maqomniTekshirish(kalit) {
    let qiymat = localStorage.getItem(kalit);
    if (qiymat !== null) {
        console.log(kalit + " mavjud:", qiymat);
        return true;
    } else {
        console.log(kalit + " mavjud emas");
        return false;
    }
}

// Test ma'lumotlari
localStorage.setItem("test1", "qiymat1");
localStorage.setItem("test2", "qiymat2");

console.log("\nMa'lumot mavjudligini tekshirish:");
maqomniTekshirish("test1");
maqomniTekshirish("test2");
maqomniTekshirish("test3");

// 10. LocalStorage bilan ishlash funksiyasi
function localStorageBilanIshlash(kalit, qiymat) {
    if (qiymat === undefined) {
        // Ma'lumot olish
        let saqlanganQiymat = localStorage.getItem(kalit);
        if (saqlanganQiymat !== null) {
            try {
                return JSON.parse(saqlanganQiymat);
            } catch (xato) {
                return saqlanganQiymat;
            }
        }
        return null;
    } else {
        // Ma'lumot saqlash
        if (typeof qiymat === "object") {
            localStorage.setItem(kalit, JSON.stringify(qiymat));
        } else {
            localStorage.setItem(kalit, qiymat);
        }
        return true;
    }
}

// Funksiya bilan ishlash
localStorageBilanIshlash("ism", "Ahmad");
localStorageBilanIshlash("yosh", 15);
localStorageBilanIshlash("obyekt", { rang: "qizil", o'lcham: "katta" });

console.log("\nFunksiya bilan olish:");
console.log("Ism:", localStorageBilanIshlash("ism"));
console.log("Yosh:", localStorageBilanIshlash("yosh"));
console.log("Obyekt:", localStorageBilanIshlash("obyekt"));

// 11. LocalStorage ni boshqarish
let localStorageManager = {
    saqlash: function(kalit, qiymat) {
        if (typeof qiymat === "object") {
            localStorage.setItem(kalit, JSON.stringify(qiymat));
        } else {
            localStorage.setItem(kalit, qiymat);
        }
        console.log("Ma'lumot saqlandi:", kalit);
    },
    
    olish: function(kalit) {
        let qiymat = localStorage.getItem(kalit);
        if (qiymat !== null) {
            try {
                return JSON.parse(qiymat);
            } catch (xato) {
                return qiymat;
            }
        }
        return null;
    },
    
    o'chirish: function(kalit) {
        localStorage.removeItem(kalit);
        console.log("Ma'lumot o'chirildi:", kalit);
    },
    
    tozalash: function() {
        localStorage.clear();
        console.log("Barcha ma'lumotlar tozalandi!");
    },
    
    royxatniKo'rsatish: function() {
        console.log("LocalStorage ma'lumotlari:");
        for (let i = 0; i < localStorage.length; i++) {
            let kalit = localStorage.key(i);
            let qiymat = localStorage.getItem(kalit);
            console.log(kalit + ":", qiymat);
        }
    }
};

// Manager bilan ishlash
localStorageManager.saqlash("foydalanuvchi", "Ahmad");
localStorageManager.saqlash("yosh", 15);
localStorageManager.saqlash("obyekt", { rang: "qizil" });

console.log("\nManager bilan olish:");
console.log("Foydalanuvchi:", localStorageManager.olish("foydalanuvchi"));
console.log("Yosh:", localStorageManager.olish("yosh"));
console.log("Obyekt:", localStorageManager.olish("obyekt"));

localStorageManager.royxatniKo'rsatish();

// 12. LocalStorage xatolarini tekshirish
function xavfsizSaqlash(kalit, qiymat) {
    try {
        if (typeof qiymat === "object") {
            localStorage.setItem(kalit, JSON.stringify(qiymat));
        } else {
            localStorage.setItem(kalit, qiymat);
        }
        console.log("Ma'lumot xavfsiz saqlandi:", kalit);
        return true;
    } catch (xato) {
        console.log("Saqlash xatosi:", xato.message);
        return false;
    }
}

function xavfsizOlish(kalit) {
    try {
        let qiymat = localStorage.getItem(kalit);
        if (qiymat !== null) {
            try {
                return JSON.parse(qiymat);
            } catch (xato) {
                return qiymat;
            }
        }
        return null;
    } catch (xato) {
        console.log("Olish xatosi:", xato.message);
        return null;
    }
}

// Xavfsiz ishlash
xavfsizSaqlash("test", "qiymat");
let natija = xavfsizOlish("test");
console.log("Xavfsiz olish natijasi:", natija);
```

### LocalStorage maslahatlari

#### 1. Ma'lumot saqlash
- Faqat matn formatida saqlaydi
- Obyektlarni JSON.stringify() bilan saqlang
- Ma'lumot mavjudligini tekshiring

#### 2. Ma'lumot olish
- JSON.parse() bilan obyektlarni oling
- Null tekshiruvlarini qo'shing
- Xatolarni boshqaring

#### 3. Xavfsizlik
- Ma'lumotlarni tekshiring
- Try-catch dan foydalaning
- Keraksiz ma'lumotlarni o'chiring

</details>
