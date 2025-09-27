<details>
    <summary>DOM nima?</summary>

## 13.1 DOM nima?

### DOM nima?

**DOM** (Document Object Model) - HTML hujjatini JavaScript orqali boshqarish uchun ishlatiladi. DOM HTML elementlarini obyekt sifatida ko'rsatadi va ularni o'zgartirish imkonini beradi.

### DOM tuzilishi

#### 1. HTML va DOM
```html
<!DOCTYPE html>
<html>
<head>
    <title>Mening sahifam</title>
</head>
<body>
    <h1>Salom dunyo!</h1>
    <p>Bu mening birinchi sahifam</p>
</body>
</html>
```

#### 2. DOM daraxti
```
document
└── html
    ├── head
    │   └── title
    └── body
        ├── h1
        └── p
```

### DOM elementlari

#### 1. Document obyekti
- `document` - butun HTML sahifani ifodalaydi
- Barcha elementlarga kirish nuqtasi
- Eng yuqori darajadagi obyekt

#### 2. Element obyektlari
- Har bir HTML tegi DOM da obyekt bo'ladi
- O'z xususiyatlari va metodlari bor
- Bir-biriga bog'langan

#### 3. Node turlari
- **Element nodes** - HTML teglari
- **Text nodes** - matn mazmuni
- **Attribute nodes** - atributlar

### DOM bilan ishlash

#### 1. Elementlarni topish
```javascript
// ID orqali topish
let element = document.getElementById("meningId");

// Class orqali topish
let elementlar = document.getElementsByClassName("meningClass");

// Teg nomi orqali topish
let teglar = document.getElementsByTagName("p");
```

#### 2. Mazmunni o'zgartirish
```javascript
let sarlavha = document.getElementById("sarlavha");
sarlavha.innerHTML = "Yangi matn";
```

#### 3. Stilni o'zgartirish
```javascript
let element = document.getElementById("meningElement");
element.style.color = "qizil";
element.style.fontSize = "20px";
```

### Amaliy misol - DOM asoslari
```javascript
// 1. Document obyektini ko'rish
console.log("Document obyekti:", document);
console.log("Document title:", document.title);
console.log("Document URL:", document.URL);

// 2. HTML elementlarini topish
let body = document.body;
console.log("Body elementi:", body);

let head = document.head;
console.log("Head elementi:", head);

// 3. Element mazmunini o'qish
let h1 = document.getElementsByTagName("h1")[0];
if (h1) {
    console.log("H1 mazmuni:", h1.innerHTML);
    console.log("H1 matni:", h1.textContent);
}

// 4. Element atributlarini o'qish
let link = document.getElementsByTagName("a")[0];
if (link) {
    console.log("Link href:", link.href);
    console.log("Link target:", link.target);
}

// 5. Element mavjudligini tekshirish
let element = document.getElementById("test");
if (element) {
    console.log("Element topildi:", element);
} else {
    console.log("Element topilmadi");
}

// 6. Barcha p teglarini topish
let pTeglar = document.getElementsByTagName("p");
console.log("P teglar soni:", pTeglar.length);

for (let i = 0; i < pTeglar.length; i++) {
    console.log("P " + (i + 1) + ":", pTeglar[i].textContent);
}

// 7. Class orqali elementlarni topish
let classElementlar = document.getElementsByClassName("meningClass");
console.log("Class elementlar soni:", classElementlar.length);

// 8. Element ota-onasini topish
let element = document.getElementById("bola");
if (element && element.parentNode) {
    console.log("Ota-ona element:", element.parentNode);
}

// 9. Element bolalarini topish
let ota = document.getElementById("ota");
if (ota && ota.children) {
    console.log("Bolalar soni:", ota.children.length);
    for (let i = 0; i < ota.children.length; i++) {
        console.log("Bola " + (i + 1) + ":", ota.children[i]);
    }
}

// 10. Element turini tekshirish
let element = document.getElementById("test");
if (element) {
    console.log("Element turi:", element.nodeType);
    console.log("Element nomi:", element.nodeName);
    console.log("Element qiymati:", element.nodeValue);
}
```

### DOM maslahatlari

#### 1. Elementlarni topish
- ID orqali eng tez topiladi
- Class va teg nomi orqali massiv qaytaradi
- Mavjud bo'lmagan element null qaytaradi

#### 2. Xavfsizlik
- Element mavjudligini tekshiring
- Null tekshiruvlarini qo'shing
- Xatolarni oldini oling

#### 3. Ishlash tezligi
- getElementById eng tez
- querySelector qulay, lekin sekinroq
- Keraksiz qidiruvlarni oldini oling

</details>

<details>
    <summary>getElementById va querySelector</summary>

## 13.2 getElementById va querySelector

### getElementById

#### 1. Asosiy ishlatish
```javascript
let element = document.getElementById("meningId");
```

#### 2. Xususiyatlari
- Faqat bitta element qaytaradi
- Eng tez ishlaydi
- ID bo'yicha qidiradi
- Topilmasa null qaytaradi

#### 3. Misol
```html
<div id="meningDiv">Bu mening divim</div>
```

```javascript
let div = document.getElementById("meningDiv");
console.log(div.innerHTML); // "Bu mening divim"
```

### querySelector

#### 1. Asosiy ishlatish
```javascript
let element = document.querySelector("css-selektor");
```

#### 2. Xususiyatlari
- CSS selektorlari bilan ishlaydi
- Birinchi mos elementni qaytaradi
- Qulay va moslashuvchan
- Topilmasa null qaytaradi

#### 3. Misollar
```javascript
// ID orqali
let element = document.querySelector("#meningId");

// Class orqali
let element = document.querySelector(".meningClass");

// Teg nomi orqali
let element = document.querySelector("p");

// Murakkab selektor
let element = document.querySelector("div.meningClass p");
```

### querySelectorAll

#### 1. Asosiy ishlatish
```javascript
let elementlar = document.querySelectorAll("css-selektor");
```

#### 2. Xususiyatlari
- Barcha mos elementlarni qaytaradi
- NodeList obyekti
- For tsikli bilan ishlatiladi
- Bo'sh bo'lsa bo'sh NodeList

#### 3. Misol
```javascript
let pTeglar = document.querySelectorAll("p");
console.log("P teglar soni:", pTeglar.length);

for (let i = 0; i < pTeglar.length; i++) {
    console.log(pTeglar[i].textContent);
}
```

### Selektor turlari

#### 1. ID selektor
```javascript
let element = document.querySelector("#meningId");
```

#### 2. Class selektor
```javascript
let element = document.querySelector(".meningClass");
```

#### 3. Teg selektor
```javascript
let element = document.querySelector("div");
```

#### 4. Atribut selektor
```javascript
let element = document.querySelector("[data-id='123']");
```

#### 5. Murakkab selektor
```javascript
let element = document.querySelector("div.meningClass p:first-child");
```

### Amaliy misol - Elementlarni topish
```javascript
// 1. getElementById
let sarlavha = document.getElementById("sarlavha");
if (sarlavha) {
    console.log("Sarlavha topildi:", sarlavha);
    console.log("Sarlavha mazmuni:", sarlavha.innerHTML);
} else {
    console.log("Sarlavha topilmadi");
}

// 2. querySelector - ID
let div = document.querySelector("#meningDiv");
if (div) {
    console.log("Div topildi:", div);
}

// 3. querySelector - Class
let classElement = document.querySelector(".meningClass");
if (classElement) {
    console.log("Class element topildi:", classElement);
}

// 4. querySelector - Teg
let pTeg = document.querySelector("p");
if (pTeg) {
    console.log("P teg topildi:", pTeg);
}

// 5. querySelectorAll - Barcha p teglar
let pTeglar = document.querySelectorAll("p");
console.log("P teglar soni:", pTeglar.length);

for (let i = 0; i < pTeglar.length; i++) {
    console.log("P " + (i + 1) + ":", pTeglar[i].textContent);
}

// 6. querySelectorAll - Class elementlar
let classElementlar = document.querySelectorAll(".meningClass");
console.log("Class elementlar soni:", classElementlar.length);

// 7. Murakkab selektor
let murakkab = document.querySelector("div.meningClass p");
if (murakkab) {
    console.log("Murakkab selektor natijasi:", murakkab);
}

// 8. Atribut selektor
let atribut = document.querySelector("[data-id='123']");
if (atribut) {
    console.log("Atribut selektor natijasi:", atribut);
}

// 9. Birinchi va oxirgi elementlar
let birinchiP = document.querySelector("p:first-child");
let oxirgiP = document.querySelector("p:last-child");

if (birinchiP) {
    console.log("Birinchi P:", birinchiP);
}
if (oxirgiP) {
    console.log("Oxirgi P:", oxirgiP);
}

// 10. Element mavjudligini tekshirish
let element = document.querySelector("#mavjudEmas");
if (element === null) {
    console.log("Element mavjud emas");
} else {
    console.log("Element mavjud:", element);
}

// 11. ForEach bilan ishlash
let divlar = document.querySelectorAll("div");
divlar.forEach(function(div, index) {
    console.log("Div " + (index + 1) + ":", div);
});

// 12. Shartli qidiruv
let elementlar = document.querySelectorAll("p, div, span");
console.log("Elementlar soni:", elementlar.length);

// 13. Ichki elementlarni qidirish
let konteyner = document.querySelector("#konteyner");
if (konteyner) {
    let ichkiElementlar = konteyner.querySelectorAll("p");
    console.log("Ichki P teglar soni:", ichkiElementlar.length);
}

// 14. Eng yaqin elementni topish
let element = document.querySelector(".bola");
if (element) {
    let ota = element.closest(".ota");
    if (ota) {
        console.log("Eng yaqin ota element:", ota);
    }
}

// 15. Qo'shni elementlarni topish
let element = document.querySelector("#markaz");
if (element) {
    let oldingi = element.previousElementSibling;
    let keyingi = element.nextElementSibling;
    
    if (oldingi) {
        console.log("Oldingi element:", oldingi);
    }
    if (keyingi) {
        console.log("Keyingi element:", keyingi);
    }
}
```

### getElementById vs querySelector

#### 1. Tezlik
- **getElementById** - eng tez
- **querySelector** - sekinroq, lekin qulay

#### 2. Moslashuvchanlik
- **getElementById** - faqat ID
- **querySelector** - barcha CSS selektorlar

#### 3. Qaytarish
- **getElementById** - bitta element
- **querySelector** - birinchi mos element

#### 4. Qachon ishlatish
- **getElementById** - aniq ID bor bo'lsa
- **querySelector** - murakkab qidiruv kerak bo'lsa

### Elementlarni topish maslahatlari

#### 1. Tezlik
- getElementById dan foydalaning
- querySelector ni kerak bo'lganda ishlating
- Keraksiz qidiruvlarni oldini oling

#### 2. Xavfsizlik
- Null tekshiruvlarini qo'shing
- Element mavjudligini tekshiring
- Xatolarni oldini oling

#### 3. Kod soddaligi
- Aniq selektorlarni yozing
- Murakkab selektorlarni soddalashtiring
- Kodni o'qilishi qilish

</details>

<details>
    <summary>HTML mazmunini o'zgartirish</summary>

## 13.3 HTML Mazmunini O'zgartirish

### HTML mazmunini o'zgartirish usullari

#### 1. innerHTML
```javascript
let element = document.getElementById("meningElement");
element.innerHTML = "Yangi mazmun";
```

#### 2. textContent
```javascript
let element = document.getElementById("meningElement");
element.textContent = "Yangi matn";
```

#### 3. innerText
```javascript
let element = document.getElementById("meningElement");
element.innerText = "Yangi matn";
```

### innerHTML vs textContent vs innerText

#### 1. innerHTML
- HTML teglarini qo'llab-quvvatlaydi
- Xavfsizlik muammolari bo'lishi mumkin
- HTML kodini qabul qiladi

#### 2. textContent
- Faqat matnni qabul qiladi
- HTML teglarini matn sifatida ko'rsatadi
- Xavfsizroq

#### 3. innerText
- Ko'rinadigan matnni qaytaradi
- CSS ta'sirida qoladi
- Tezroq ishlaydi

### Mazmunni o'qish

#### 1. innerHTML o'qish
```javascript
let element = document.getElementById("meningElement");
let mazmun = element.innerHTML;
console.log(mazmun);
```

#### 2. textContent o'qish
```javascript
let element = document.getElementById("meningElement");
let matn = element.textContent;
console.log(matn);
```

#### 3. innerText o'qish
```javascript
let element = document.getElementById("meningElement");
let ko'rinadiganMatn = element.innerText;
console.log(ko'rinadiganMatn);
```

### Amaliy misol - HTML mazmunini o'zgartirish
```javascript
// 1. innerHTML bilan mazmun o'zgartirish
let sarlavha = document.getElementById("sarlavha");
if (sarlavha) {
    sarlavha.innerHTML = "<strong>Yangi sarlavha</strong>";
    console.log("Sarlavha o'zgartirildi");
}

// 2. textContent bilan matn o'zgartirish
let paragraf = document.getElementById("paragraf");
if (paragraf) {
    paragraf.textContent = "Bu yangi matn";
    console.log("Paragraf o'zgartirildi");
}

// 3. innerText bilan ko'rinadigan matn o'zgartirish
let matn = document.getElementById("matn");
if (matn) {
    matn.innerText = "Bu ko'rinadigan matn";
    console.log("Matn o'zgartirildi");
}

// 4. Mazmunni o'qish
let element = document.getElementById("test");
if (element) {
    console.log("innerHTML:", element.innerHTML);
    console.log("textContent:", element.textContent);
    console.log("innerText:", element.innerText);
}

// 5. HTML teglar bilan ishlash
let konteyner = document.getElementById("konteyner");
if (konteyner) {
    konteyner.innerHTML = `
        <h2>Yangi sarlavha</h2>
        <p>Bu yangi paragraf</p>
        <ul>
            <li>Birinchi element</li>
            <li>Ikkinchi element</li>
        </ul>
    `;
}

// 6. Matn qo'shish
let mavjudMatn = document.getElementById("mavjudMatn");
if (mavjudMatn) {
    let eskiMatn = mavjudMatn.textContent;
    mavjudMatn.textContent = eskiMatn + " - qo'shilgan matn";
}

// 7. Shartli mazmun o'zgartirish
let holat = document.getElementById("holat");
if (holat) {
    let vaqt = new Date().getHours();
    if (vaqt < 12) {
        holat.textContent = "Xayrli tong!";
    } else if (vaqt < 18) {
        holat.textContent = "Xayrli kun!";
    } else {
        holat.textContent = "Xayrli kech!";
    }
}

// 8. Ro'yxat elementlarini o'zgartirish
let royxat = document.getElementById("royxat");
if (royxat) {
    let elementlar = ["olma", "banan", "apelsin"];
    let royxatHTML = "<ul>";
    
    for (let i = 0; i < elementlar.length; i++) {
        royxatHTML += "<li>" + elementlar[i] + "</li>";
    }
    
    royxatHTML += "</ul>";
    royxat.innerHTML = royxatHTML;
}

// 9. Jadval yaratish
let jadval = document.getElementById("jadval");
if (jadval) {
    let ma'lumotlar = [
        ["Ism", "Yosh", "Shahar"],
        ["Ahmad", "20", "Toshkent"],
        ["Karim", "25", "Samarqand"],
        ["Sardor", "22", "Buxoro"]
    ];
    
    let jadvalHTML = "<table border='1'>";
    
    for (let i = 0; i < ma'lumotlar.length; i++) {
        jadvalHTML += "<tr>";
        for (let j = 0; j < ma'lumotlar[i].length; j++) {
            if (i === 0) {
                jadvalHTML += "<th>" + ma'lumotlar[i][j] + "</th>";
            } else {
                jadvalHTML += "<td>" + ma'lumotlar[i][j] + "</td>";
            }
        }
        jadvalHTML += "</tr>";
    }
    
    jadvalHTML += "</table>";
    jadval.innerHTML = jadvalHTML;
}

// 10. Xavfsiz matn o'zgartirish
let xavfsizMatn = document.getElementById("xavfsizMatn");
if (xavfsizMatn) {
    let foydalanuvchiMatni = "<script>alert('Xavf!')</script>";
    xavfsizMatn.textContent = foydalanuvchiMatni; // Xavfsiz
    // xavfsizMatn.innerHTML = foydalanuvchiMatni; // Xavfli!
}

// 11. Matnni bo'lish va qo'shish
let uzunMatn = document.getElementById("uzunMatn");
if (uzunMatn) {
    let matn = uzunMatn.textContent;
    let sozlar = matn.split(" ");
    let yangiMatn = "";
    
    for (let i = 0; i < sozlar.length; i++) {
        if (sozlar[i].length > 3) {
            yangiMatn += "<strong>" + sozlar[i] + "</strong> ";
        } else {
            yangiMatn += sozlar[i] + " ";
        }
    }
    
    uzunMatn.innerHTML = yangiMatn;
}

// 12. Vaqtni yangilash
let vaqt = document.getElementById("vaqt");
if (vaqt) {
    function vaqtniYangilash() {
        let hozirgiVaqt = new Date();
        vaqt.textContent = hozirgiVaqt.toLocaleTimeString();
    }
    
    vaqtniYangilash();
    setInterval(vaqtniYangilash, 1000);
}

// 13. Hisoblagich
let hisoblagich = document.getElementById("hisoblagich");
if (hisoblagich) {
    let son = 0;
    hisoblagich.textContent = "Hisob: " + son;
    
    // 5 soniyada bir marta oshirish
    setInterval(function() {
        son++;
        hisoblagich.textContent = "Hisob: " + son;
    }, 5000);
}

// 14. Matnni tekshirish va o'zgartirish
let tekshiruvMatn = document.getElementById("tekshiruvMatn");
if (tekshiruvMatn) {
    let matn = tekshiruvMatn.textContent;
    
    if (matn.includes("yaxshi")) {
        tekshiruvMatn.innerHTML = matn.replace("yaxshi", "<em>juda yaxshi</em>");
    }
    
    if (matn.length > 100) {
        tekshiruvMatn.textContent = matn.substring(0, 100) + "...";
    }
}

// 15. Dinamik ro'yxat
let dinamikRoyxat = document.getElementById("dinamikRoyxat");
if (dinamikRoyxat) {
    let elementlar = [];
    
    function royxatniYangilash() {
        let royxatHTML = "<ul>";
        for (let i = 0; i < elementlar.length; i++) {
            royxatHTML += "<li>" + elementlar[i] + "</li>";
        }
        royxatHTML += "</ul>";
        dinamikRoyxat.innerHTML = royxatHTML;
    }
    
    // Yangi element qo'shish
    elementlar.push("Birinchi element");
    elementlar.push("Ikkinchi element");
    royxatniYangilash();
}
```

### HTML mazmunini o'zgartirish maslahatlari

#### 1. Xavfsizlik
- textContent dan foydalaning
- innerHTML ni ehtiyotkorlik bilan ishlating
- Foydalanuvchi kiritishini tozalang

#### 2. Ishlash tezligi
- innerText eng tez
- textContent o'rtacha
- innerHTML sekinroq

#### 3. Kod soddaligi
- Aniq usulni tanlang
- Kodni o'qilishi qilish
- Izohlarni qo'shing

</details>

<details>
    <summary>CSS stillarini JavaScript orqali o'zgartirish</summary>

## 13.4 CSS Stillarini JavaScript Orqali O'zgartirish

### CSS stillarini o'zgartirish usullari

#### 1. style xususiyati
```javascript
let element = document.getElementById("meningElement");
element.style.color = "qizil";
element.style.fontSize = "20px";
```

#### 2. className xususiyati
```javascript
let element = document.getElementById("meningElement");
element.className = "yangiClass";
```

#### 3. classList metodlari
```javascript
let element = document.getElementById("meningElement");
element.classList.add("yangiClass");
element.classList.remove("eskiClass");
element.classList.toggle("aktivClass");
```

### style xususiyati

#### 1. Asosiy ishlatish
```javascript
let element = document.getElementById("meningElement");
element.style.backgroundColor = "yashil";
element.style.color = "oq";
element.style.padding = "10px";
```

#### 2. CSS xususiyatlari
- camelCase formatida yoziladi
- background-color → backgroundColor
- font-size → fontSize
- margin-top → marginTop

#### 3. Qiymatlar
- String formatida beriladi
- Birliklar bilan (px, em, %)
- Ranglar nomi yoki hex kod

### classList metodlari

#### 1. add() - class qo'shish
```javascript
let element = document.getElementById("meningElement");
element.classList.add("yangiClass");
```

#### 2. remove() - class olib tashlash
```javascript
let element = document.getElementById("meningElement");
element.classList.remove("eskiClass");
```

#### 3. toggle() - class yoqish/o'chirish
```javascript
let element = document.getElementById("meningElement");
element.classList.toggle("aktivClass");
```

#### 4. contains() - class borligini tekshirish
```javascript
let element = document.getElementById("meningElement");
if (element.classList.contains("meningClass")) {
    console.log("Class mavjud");
}
```

### Amaliy misol - CSS stillarini o'zgartirish
```javascript
// 1. Asosiy stillar
let element = document.getElementById("meningElement");
if (element) {
    element.style.color = "qizil";
    element.style.fontSize = "18px";
    element.style.fontWeight = "bold";
    element.style.backgroundColor = "sariq";
    element.style.padding = "15px";
    element.style.margin = "10px";
    element.style.border = "2px solid qora";
    element.style.borderRadius = "5px";
}

// 2. Ranglarni o'zgartirish
let rangElement = document.getElementById("rangElement");
if (rangElement) {
    let ranglar = ["qizil", "yashil", "ko'k", "sariq", "binafsha"];
    let hozirgiRang = 0;
    
    setInterval(function() {
        rangElement.style.backgroundColor = ranglar[hozirgiRang];
        hozirgiRang = (hozirgiRang + 1) % ranglar.length;
    }, 1000);
}

// 3. O'lchamlarni o'zgartirish
let o'lchamElement = document.getElementById("olchamElement");
if (o'lchamElement) {
    let kenglik = 100;
    let balandlik = 100;
    
    setInterval(function() {
        kenglik += 10;
        balandlik += 10;
        o'lchamElement.style.width = kenglik + "px";
        o'lchamElement.style.height = balandlik + "px";
        
        if (kenglik > 300) {
            kenglik = 100;
            balandlik = 100;
        }
    }, 500);
}

// 4. classList bilan ishlash
let classElement = document.getElementById("classElement");
if (classElement) {
    // Class qo'shish
    classElement.classList.add("yangiClass");
    
    // Class olib tashlash
    classElement.classList.remove("eskiClass");
    
    // Class yoqish/o'chirish
    classElement.classList.toggle("aktivClass");
    
    // Class borligini tekshirish
    if (classElement.classList.contains("meningClass")) {
        console.log("Class mavjud");
    }
}

// 5. Shartli stillar
let shartliElement = document.getElementById("shartliElement");
if (shartliElement) {
    let holat = true;
    
    function holatniO'zgartirish() {
        if (holat) {
            shartliElement.style.backgroundColor = "yashil";
            shartliElement.style.color = "oq";
            shartliElement.textContent = "Faol";
        } else {
            shartliElement.style.backgroundColor = "qizil";
            shartliElement.style.color = "oq";
            shartliElement.textContent = "Nofaol";
        }
        holat = !holat;
    }
    
    setInterval(holatniO'zgartirish, 2000);
}

// 6. Hover effektlari
let hoverElement = document.getElementById("hoverElement");
if (hoverElement) {
    hoverElement.addEventListener("mouseenter", function() {
        this.style.backgroundColor = "yashil";
        this.style.transform = "scale(1.1)";
        this.style.transition = "all 0.3s ease";
    });
    
    hoverElement.addEventListener("mouseleave", function() {
        this.style.backgroundColor = "oq";
        this.style.transform = "scale(1)";
    });
}

// 7. Animatsiya
let animatsiyaElement = document.getElementById("animatsiyaElement");
if (animatsiyaElement) {
    let pozitsiya = 0;
    let yo'nalish = 1;
    
    setInterval(function() {
        pozitsiya += yo'nalish * 5;
        animatsiyaElement.style.left = pozitsiya + "px";
        
        if (pozitsiya >= 300 || pozitsiya <= 0) {
            yo'nalish *= -1;
        }
    }, 50);
}

// 8. Matn stillari
let matnElement = document.getElementById("matnElement");
if (matnElement) {
    matnElement.style.fontFamily = "Arial, sans-serif";
    matnElement.style.fontSize = "16px";
    matnElement.style.lineHeight = "1.5";
    matnElement.style.textAlign = "center";
    matnElement.style.textDecoration = "underline";
    matnElement.style.textTransform = "uppercase";
    matnElement.style.letterSpacing = "2px";
    matnElement.style.wordSpacing = "5px";
}

// 9. Border stillari
let borderElement = document.getElementById("borderElement");
if (borderElement) {
    borderElement.style.border = "3px solid qizil";
    borderElement.style.borderRadius = "10px";
    borderElement.style.borderTopColor = "yashil";
    borderElement.style.borderRightColor = "ko'k";
    borderElement.style.borderBottomColor = "sariq";
    borderElement.style.borderLeftColor = "binafsha";
}

// 10. Shadow effektlari
let shadowElement = document.getElementById("shadowElement");
if (shadowElement) {
    shadowElement.style.boxShadow = "5px 5px 10px rgba(0,0,0,0.3)";
    shadowElement.style.textShadow = "2px 2px 4px rgba(0,0,0,0.5)";
}

// 11. Opacity va visibility
let opacityElement = document.getElementById("opacityElement");
if (opacityElement) {
    let opacity = 1;
    let yo'nalish = -0.1;
    
    setInterval(function() {
        opacity += yo'nalish;
        opacityElement.style.opacity = opacity;
        
        if (opacity <= 0 || opacity >= 1) {
            yo'nalish *= -1;
        }
    }, 100);
}

// 12. Transform effektlari
let transformElement = document.getElementById("transformElement");
if (transformElement) {
    let burchak = 0;
    
    setInterval(function() {
        burchak += 5;
        transformElement.style.transform = "rotate(" + burchak + "deg)";
    }, 50);
}

// 13. Responsive stillar
let responsiveElement = document.getElementById("responsiveElement");
if (responsiveElement) {
    function responsiveStillar() {
        let kenglik = window.innerWidth;
        
        if (kenglik < 600) {
            responsiveElement.style.fontSize = "14px";
            responsiveElement.style.padding = "5px";
        } else if (kenglik < 900) {
            responsiveElement.style.fontSize = "16px";
            responsiveElement.style.padding = "10px";
        } else {
            responsiveElement.style.fontSize = "18px";
            responsiveElement.style.padding = "15px";
        }
    }
    
    responsiveStillar();
    window.addEventListener("resize", responsiveStillar);
}

// 14. Gradient fonlar
let gradientElement = document.getElementById("gradientElement");
if (gradientElement) {
    gradientElement.style.background = "linear-gradient(45deg, qizil, yashil)";
    gradientElement.style.backgroundSize = "200% 200%";
    
    let pozitsiya = 0;
    setInterval(function() {
        pozitsiya += 1;
        gradientElement.style.backgroundPosition = pozitsiya + "% " + pozitsiya + "%";
    }, 50);
}

// 15. Dinamik class o'zgartirish
let dinamikClassElement = document.getElementById("dinamikClassElement");
if (dinamikClassElement) {
    let classlar = ["class1", "class2", "class3", "class4"];
    let hozirgiClass = 0;
    
    setInterval(function() {
        // Eski classni olib tashlash
        dinamikClassElement.classList.remove(classlar[hozirgiClass]);
        
        // Yangi classni qo'shish
        hozirgiClass = (hozirgiClass + 1) % classlar.length;
        dinamikClassElement.classList.add(classlar[hozirgiClass]);
    }, 1000);
}
```

### CSS stillarini o'zgartirish maslahatlari

#### 1. style xususiyati
- camelCase formatida yozing
- Birliklar bilan qiymatlar bering
- String formatida yozing

#### 2. classList metodlari
- add(), remove(), toggle() dan foydalaning
- contains() bilan tekshiring
- Bir nechta class larni boshqaring

#### 3. Ishlash tezligi
- classList style dan tezroq
- Keraksiz o'zgarishlarni oldini oling
- CSS transition dan foydalaning

</details>

<details>
    <summary>Event listeners</summary>

## 13.5 Event Listeners

### Event nima?

**Event** - foydalanuvchi yoki tizim tomonidan yuzaga keladigan hodisalar. Masalan, tugma bosish, sichqoncha harakati, sahifa yuklanishi.

### Event listener qo'shish

#### 1. addEventListener
```javascript
let element = document.getElementById("meningElement");
element.addEventListener("click", function() {
    console.log("Tugma bosildi!");
});
```

#### 2. Xususiyatlari
- Elementga hodisa qo'shadi
- Bir nechta listener qo'shish mumkin
- removeEventListener bilan olib tashlash mumkin

#### 3. Sintaksis
```javascript
element.addEventListener(hodisa, funksiya, parametrlar);
```

### Asosiy event turlari

#### 1. Sichqoncha hodisalari
- **click** - bosish
- **dblclick** - ikki marta bosish
- **mouseenter** - ichkariga kirish
- **mouseleave** - tashqariga chiqish
- **mousemove** - harakat

#### 2. Klaviatura hodisalari
- **keydown** - tugma bosilganda
- **keyup** - tugma qo'yilganda
- **keypress** - tugma bosilganda

#### 3. Form hodisalari
- **submit** - form yuborilganda
- **change** - qiymat o'zgarganda
- **focus** - fokus olganda
- **blur** - fokus yo'qolganda

#### 4. Sahifa hodisalari
- **load** - sahifa yuklanganda
- **resize** - o'lcham o'zgarganda
- **scroll** - scroll qilinganda

### Amaliy misol - Event listeners
```javascript
// 1. Click hodisasi
let tugma = document.getElementById("tugma");
if (tugma) {
    tugma.addEventListener("click", function() {
        console.log("Tugma bosildi!");
        this.style.backgroundColor = "yashil";
    });
}

// 2. Double click hodisasi
let element = document.getElementById("element");
if (element) {
    element.addEventListener("dblclick", function() {
        console.log("Ikki marta bosildi!");
        this.style.backgroundColor = "qizil";
    });
}

// 3. Mouse enter va leave
let hoverElement = document.getElementById("hoverElement");
if (hoverElement) {
    hoverElement.addEventListener("mouseenter", function() {
        this.style.backgroundColor = "yashil";
        this.style.transform = "scale(1.1)";
    });
    
    hoverElement.addEventListener("mouseleave", function() {
        this.style.backgroundColor = "oq";
        this.style.transform = "scale(1)";
    });
}

// 4. Mouse move hodisasi
let moveElement = document.getElementById("moveElement");
if (moveElement) {
    moveElement.addEventListener("mousemove", function(event) {
        this.textContent = "X: " + event.clientX + ", Y: " + event.clientY;
    });
}

// 5. Klaviatura hodisalari
document.addEventListener("keydown", function(event) {
    console.log("Bosilgan tugma:", event.key);
    console.log("Kod:", event.code);
    
    if (event.key === "Enter") {
        console.log("Enter tugmasi bosildi!");
    }
    
    if (event.key === "Escape") {
        console.log("Escape tugmasi bosildi!");
    }
});

// 6. Form hodisalari
let form = document.getElementById("meningForm");
if (form) {
    form.addEventListener("submit", function(event) {
        event.preventDefault(); // Sahifani yangilanishdan to'xtatish
        console.log("Form yuborildi!");
        
        let input = document.getElementById("input");
        if (input) {
            console.log("Kiritilgan matn:", input.value);
        }
    });
}

// 7. Input change hodisasi
let input = document.getElementById("input");
if (input) {
    input.addEventListener("change", function() {
        console.log("Input qiymati o'zgardi:", this.value);
    });
    
    input.addEventListener("input", function() {
        console.log("Hozirgi qiymat:", this.value);
    });
}

// 8. Focus va blur hodisalari
let focusInput = document.getElementById("focusInput");
if (focusInput) {
    focusInput.addEventListener("focus", function() {
        this.style.border = "2px solid yashil";
        this.style.backgroundColor = "yashil";
    });
    
    focusInput.addEventListener("blur", function() {
        this.style.border = "1px solid qora";
        this.style.backgroundColor = "oq";
    });
}

// 9. Sahifa hodisalari
window.addEventListener("load", function() {
    console.log("Sahifa to'liq yuklandi!");
});

window.addEventListener("resize", function() {
    console.log("Sahifa o'lchami o'zgardi!");
    console.log("Kenglik:", window.innerWidth);
    console.log("Balandlik:", window.innerHeight);
});

window.addEventListener("scroll", function() {
    console.log("Scroll qilindi!");
    console.log("Scroll pozitsiyasi:", window.scrollY);
});

// 10. Event parametrlari
let parametrElement = document.getElementById("parametrElement");
if (parametrElement) {
    parametrElement.addEventListener("click", function(event) {
        console.log("Event obyekti:", event);
        console.log("Target:", event.target);
        console.log("Current target:", event.currentTarget);
        console.log("Event turi:", event.type);
        console.log("Vaqt:", event.timeStamp);
    });
}

// 11. Event bubbling
let ota = document.getElementById("ota");
let bola = document.getElementById("bola");

if (ota && bola) {
    ota.addEventListener("click", function() {
        console.log("Ota element bosildi!");
    });
    
    bola.addEventListener("click", function(event) {
        console.log("Bola element bosildi!");
        event.stopPropagation(); // Bubbling ni to'xtatish
    });
}

// 12. Event delegation
let royxat = document.getElementById("royxat");
if (royxat) {
    royxat.addEventListener("click", function(event) {
        if (event.target.tagName === "LI") {
            console.log("Ro'yxat elementi bosildi:", event.target.textContent);
            event.target.style.backgroundColor = "yashil";
        }
    });
}

// 13. removeEventListener
let olibTashlanadiganElement = document.getElementById("olibTashlanadiganElement");
if (olibTashlanadiganElement) {
    function bosishFunksiyasi() {
        console.log("Element bosildi!");
    }
    
    // Event listener qo'shish
    olibTashlanadiganElement.addEventListener("click", bosishFunksiyasi);
    
    // 5 soniyadan keyin olib tashlash
    setTimeout(function() {
        olibTashlanadiganElement.removeEventListener("click", bosishFunksiyasi);
        console.log("Event listener olib tashlandi!");
    }, 5000);
}

// 14. Bir nechta hodisalar
let ko'pHodisaElement = document.getElementById("ko'pHodisaElement");
if (ko'pHodisaElement) {
    ko'pHodisaElement.addEventListener("click", function() {
        console.log("Click hodisasi!");
    });
    
    ko'pHodisaElement.addEventListener("mouseenter", function() {
        console.log("Mouse enter hodisasi!");
    });
    
    ko'pHodisaElement.addEventListener("mouseleave", function() {
        console.log("Mouse leave hodisasi!");
    });
}

// 15. Shartli event listener
let shartliElement = document.getElementById("shartliElement");
if (shartliElement) {
    let holat = true;
    
    function shartliFunksiya() {
        if (holat) {
            console.log("Holat: Faol");
            this.style.backgroundColor = "yashil";
        } else {
            console.log("Holat: Nofaol");
            this.style.backgroundColor = "qizil";
        }
        holat = !holat;
    }
    
    shartliElement.addEventListener("click", shartliFunksiya);
}
```

### Event listener maslahatlari

#### 1. Xavfsizlik
- event.preventDefault() dan foydalaning
- event.stopPropagation() ni ehtiyotkorlik bilan ishlating
- Xatolarni oldini oling

#### 2. Ishlash tezligi
- Event delegation dan foydalaning
- Keraksiz listener larni olib tashlang
- Debouncing va throttling qo'llang

#### 3. Kod soddaligi
- Aniq funksiya nomlarini yozing
- Event larni guruhlang
- Kodni o'qilishi qilish

</details>
