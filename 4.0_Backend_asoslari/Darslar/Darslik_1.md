<details>
    <summary>Internet va Backend asoslari</summary>
## 🗓️ 1-hafta — 1-dars

### 🏷️ Mavzu: **Internet va Backend asoslari**

---

### Internet qanday ishlaydi?

Internet — bu butun dunyodagi kompyuterlar bir-biri bilan bog‘lanib, ma’lumot almashadigan ulkan tarmoqdir. Siz brauzerga biror sayt manzilini kiritganda (masalan, `www.youtube.com`), sizning kompyuteringiz boshqa bir kompyuterga — **serverga** murojaat qiladi. Server degani — ma’lumot saqlanadigan va uni boshqalarga jo‘natadigan kuchli kompyuter.

Masalan:

* Siz YouTube’ga kirdingiz → brauzer YouTube serveriga “menga sahifani yubor” deb so‘rov jo‘natadi.
* Server sahifa kodi, rasm va videolarni yuboradi.
* Sizning brauzeringiz shu ma’lumotni chiroyli qilib ekranda ko‘rsatadi.

---

### Frontend va Backend

**Frontend** — foydalanuvchi ko‘radigan qism. HTML, CSS, JavaScript yordamida ishlanadi.
**Backend** — foydalanuvchi ko‘rmaydigan qism. U ma’lumotni saqlaydi, hisob-kitob qiladi va frontendga yuboradi.

Misol:

* Onlayn do‘konda mahsulotlarni ko‘rasiz (frontend).
* Ammo u mahsulotlar qayerdan keladi? Serverdagi ma’lumotlar bazasidan (backend).
* Siz buyurtma berasiz → server uni yozib qo‘yadi → keyin do‘kon xodimlari ko‘radi.

---

### So‘rov (Request) va Javob (Response)

Har safar siz biror saytga kirganingizda brauzer **so‘rov** yuboradi, server esa **javob** qaytaradi.

* **So‘rov (Request):** Brauzerning “Menga shu narsani ber” degan xabari.
* **Javob (Response):** Serverning “Mana senga so‘raganing” deb yuborgan ma’lumoti.

Masalan: siz brauzerga `https://catfact.ninja/fact` yozasiz. Server quyidagicha javob yuboradi:

```json
{
  "fact": "Mushuklar kuniga 12-16 soat uxlashadi.",
  "length": 41
}
```

Bu javob **JSON** formatida.

---

### HTTP tushunchasi

HTTP — bu brauzer va server o‘rtasida ma’lumot almashish uchun ishlatiladigan asosiy qoidalar to‘plami.

HTTP’da bir nechta turdagi so‘rovlar bor:

* **GET** — ma’lumot olish. (masalan, mahsulot ro‘yxati so‘rash)
* **POST** — yangi ma’lumot yuborish. (masalan, yangi buyurtma yuborish)
* **PUT/PATCH** — ma’lumotni yangilash. (masalan, profilingizdagi telefon raqamini o‘zgartirish)
* **DELETE** — ma’lumotni o‘chirish. (masalan, eski postni o‘chirish)

---

### JSON nima va nega kerak?

JSON — bu ma’lumotlarni internet orqali tartibli yuborish usuli. Deyarli barcha backend va frontend dasturlar bir-biri bilan JSON orqali gaplashadi.

**Oddiy misol:**

```json
{
  "ism": "Dilshod",
  "yosh": 14,
  "hobby": "futbol"
}
```

* `{}` obyekt — ichida ma’lumot bor.
* `"ism": "Dilshod"` — “ism” degan kalit va uning qiymati “Dilshod”.
* `:` belgisi kalit va qiymatni ajratadi.
* `,` belgisi bir nechta ma’lumotlarni ajratib turadi.

**Ro‘yxat (array) misoli:**

```json
[
  { "ism": "Ali", "yosh": 13 },
  { "ism": "Vali", "yosh": 12 }
]
```

`[]` — bu ro‘yxat. Ichida obyektlar bor.

---

### JSON real hayotdan misollar

1. O‘yinlardagi foydalanuvchi ma’lumoti:

```json
{
  "nickname": "ProGamer",
  "level": 5,
  "score": 3200
}
```

2. Onlayn do‘kondagi mahsulot:

```json
{
  "nomi": "Telefon",
  "brend": "Samsung",
  "narx": 2500000,
  "omborda": true
}
```

3. Maktabdagi o‘quvchilar ro‘yxati:

```json
[
  { "ism": "Aziza", "sinfi": "7A" },
  { "ism": "Sardor", "sinfi": "7A" },
  { "ism": "Lola", "sinfi": "7B" }
]
```

---

### Developer Tools yordamida ko‘rish

Har bir brauzerda **Developer Tools** (F12) degan qulaylik bor.

1. Istalgan saytga kiring.
2. F12 tugmasini bosing yoki o‘ng tugma → “Inspect”.
3. “Network” bo‘limiga kiring.
4. Sahifani yangilang (Reload).
5. Ko‘p fayllar chiqadi: HTML, CSS, JS, rasmlar, JSON ma’lumotlar.

Masalan, YouTube’da video sahifasini ochsangiz ko‘plab `GET` so‘rovlari va `200` javob kodlarini ko‘rasiz.

* **200** — hammasi joyida.
* **404** — topilmadi.
* **500** — serverda xato bor.

---

### Oddiy mashq

1. Kompyuteringizda yangi `men.json` fayli yarating.
2. Quyidagicha yozing:

```json
{
  "ism": "Sizning ismingiz",
  "yosh": 13,
  "qiziqishlar": ["Kompyuter o‘yinlari", "Futbol", "Rasm chizish"]
}
```

3. Faylni VS Code yoki brauzerda ochib ko‘ring. JSON ma’lumot qanday yozilganiga e’tibor bering.

4. Brauzerga mana bu manzilni yozing:
   `https://jsonplaceholder.typicode.com/users`
   — ko‘p ma’lumotlar chiqadi, bu haqiqiy backenddan kelgan JSON.

---

### Asosiy tushunchalar

* **Backend** — yashirin qism, ma’lumotni boshqaradi.
* **Frontend** — foydalanuvchi ko‘radigan qism.
* **Server** — backend ishlaydigan kompyuter.
* **HTTP** — brauzer va serverning aloqa tili.
* **JSON** — ma’lumotni internet orqali yuborish va olish uchun eng ko‘p ishlatiladigan format.

---

</details>

<hr>

<details>
    <summary>Node.js o‘rnatish va birinchi backend kodimiz</summary>
## 🗓️ 1-hafta — 2-dars

### 🏷️ Mavzu: **Node.js o‘rnatish va birinchi backend kodimiz**

---

### Node.js nima?

Node.js — bu **JavaScript dasturini brauzerdan tashqarida ham ishlatish imkonini beradigan platforma**.
Biz odatda JavaScript’ni faqat saytning ko‘rinadigan qismida ishlatamiz (frontend). Ammo Node.js tufayli server tarafda ham JS yozish mumkin.
Ya’ni, **bir xil til — ikkala tomonda** (frontend va backend). Shu sababli o‘rganish oson.

**Oddiy taqqoslash:**

|              | Frontend               | Backend                                      |
| ------------ | ---------------------- | -------------------------------------------- |
| Til          | JavaScript (brauzerda) | JavaScript (Node.js bilan)                   |
| Ko‘rinadimi? | Ha                     | Yo‘q                                         |
| Vazifasi     | Dizayn, interaktivlik  | Ma’lumotni saqlash, hisoblash, qayta ishlash |

---

### Node.js o‘rnatish

1. [https://nodejs.org](https://nodejs.org) saytidan **LTS (Recommended)** versiyasini yuklab oling.
2. O‘rnatish vaqtida barcha sozlamalarni standart qoldiring (Next, Next, Install).
3. O‘rnatish tugagach, **Terminal** yoki **CMD** ochib, quyidagilarni yozing:

```bash
node -v
```

Node versiyasini ko‘rsatadi (masalan `v20.11.0`).

```bash
npm -v
```

npm versiyasini ko‘rsatadi (masalan `10.2.4`).

✅ Bu Node.js va npm (Node Package Manager — Node uchun paketlar o‘rnatadigan dastur) ishlayotganini bildiradi.

---

### Node.js bilan birinchi dastur

1. Kompyuteringizda yangi papka yarating: `backend-lessons`
2. VS Code orqali shu papkani oching.
3. Yangi fayl yarating: `app.js`
4. Quyidagi kodni yozing:

```javascript
console.log("Salom, Node.js!");
```

5. Terminalda shu faylni ishga tushiring:

```bash
node app.js
```

Ekranda `Salom, Node.js!` yozuvi chiqadi.

➡️ Bu — bizning birinchi server tomondagi JavaScript ishga tushganini bildiradi.

---

### Node.js bilan oddiy hisoblash

```javascript
const a = 5;
const b = 7;
console.log("Yig‘indi:", a + b);
console.log("Ko‘paytma:", a * b);
```

`node app.js` bilan ishga tushiring. Natija terminalda chiqadi.
Bu bilan biz Node’ning oddiy JavaScript kodini qanday ishlatayotganini ko‘ramiz.

---

### Oddiy mini loyiha: shaxsiy ma’lumot

`info.js` degan fayl yarating va quyidagicha yozing:

```javascript
const ism = "Dilshod";
const yosh = 14;
const qiziqishlar = ["Futbol", "Kitob o‘qish", "Dasturlash"];

console.log("Mening ismim:", ism);
console.log("Yoshim:", yosh);
console.log("Qiziqishlarim:", qiziqishlar.join(", "));
```

Terminalda ishga tushiring:

```bash
node info.js
```

Natija:

```
Mening ismim: Dilshod
Yoshim: 14
Qiziqishlarim: Futbol, Kitob o‘qish, Dasturlash
```

---

### npm va `package.json`

npm — Node.js uchun kerakli dasturlarni (kutubxonalarni) o'rnatish imkonini beradi.
Masalan, loglarni chiroyli rangda chiqarish uchun `chalk` paketini o'rnatamiz.

1. Terminalda papka ichida quyidagini yozing:

```bash
npm init -y
```

Bu `package.json` degan fayl yaratadi — u loyiha haqida ma'lumot saqlaydi.

**Muhim:** ES Module syntaxidan foydalanish uchun `package.json` da quyidagi sozlash kerak:

```json
{
  "name": "backend-lessons",
  "version": "1.0.0",
  "type": "module",
  "description": "Backend asoslari kursi",
  "main": "server.js",
  "scripts": {
    "start": "node server.js",
    "dev": "nodemon server.js",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": ["backend", "node", "express"],
  "author": "Sizning ismingiz",
  "license": "MIT"
}
```

Asosiy moslashuvlar:
* `"type": "module"` — ES Module syntaxini ishlatish uchun majburiy
* `scripts` — tez-tez ishlatiladigan buyruqlar (`npm start`, `npm run dev`)

2. `chalk` kutubxonasini o‘rnatamiz:

```bash
npm install chalk
```

3. `app.js` faylida quyidagilarni yozamiz:

```javascript
import chalk from 'chalk';

console.log(chalk.blue('Salom, Node.js!'));
console.log(chalk.green('Backend boshlayapmiz 🚀'));
```

4. Ishga tushiring:

```bash
node app.js
```

Endi yozuvlar rangli chiqadi.

---

### Foydali buyruqlar

* `node fayl_nomi.js` — faylni ishga tushirish.
* `npm init -y` — yangi Node loyihasini yaratish.
* `npm install kutubxona_nomi` — qo‘shimcha kutubxonalar o‘rnatish.

---

### Xulosa

* Node.js — backend yozish uchun juda qulay, chunki JavaScript tilidan foydalanamiz.
* Node.js o‘rnatib, terminal orqali dasturlarni ishga tushirishni o‘rgandik.
* npm yordamida boshqa kutubxonalarni qo‘shish mumkin.

</details>

<hr>

<details>
    <summary>Express bilan birinchi server</summary>

## 🗓️ 1-hafta — 3-dars

### 🏷️ Mavzu: **Express bilan birinchi server**

---

### 🎯 Bu darsda nima o'rganamiz?

* Express nima va nega kerak
* Birinchi serverni qanday yaratish
* Oddiy yo'llar (routes) yaratish
* Brauzerda natijalarni ko'rish

---

### Express nima va nega kerak?

Node.js bilan ham server yozish mumkin, lekin har safar ko'p kod yozish kerak bo'ladi va chalkash bo'lib ketadi.
**Express** — bu Node.js uchun yozilgan maxsus kutubxona (tayyor kodlar to'plami).
Biz undan foydalansak:

* Serverni juda tez ishga tushira olamiz.
* Turli manzillar (yo'llar) yaratib, turli ma'lumot yubora olamiz.
* Katta kodlar o'rniga bir necha qator bilan ishni boshlaymiz.

**Oddiy hayotiy misol:**
Express — bu "tayyor oshxona". O'zingiz ham oshxona qurishingiz mumkin, lekin Express borida hammasi tayyor: gaz plitasi, idish-tovoq, pichoq. Siz faqat taom tayyorlaysiz.

---

### Express o'rnatish

1. Papka ochamiz: `backend-lessons`
2. Terminalda shu papkaga kiring.
3. Node loyihasini boshlang:

```bash
npm init -y
```

4. Expressni o'rnating:

```bash
npm install express
```

✅ Endi Express loyihangizga qo'shildi.

---

### Birinchi Express server

`server.js` faylini yarating va yozing:

```javascript
import express from 'express';    // Express kutubxonasini chaqiryapmiz

const app = express();            // Server dasturini yaratdik
const PORT = 3000;                // Server ishlaydigan port

// Asosiy manzil — bu / (ildiz)
app.get('/', function(req, res) {
  res.send('Salom! Bu mening birinchi backend serverim 🚀');
});

// Serverni ishga tushiramiz
app.listen(PORT, function() {
  console.log(`Server ishga tushdi: http://localhost:${PORT}`);
});
```

Keyin terminalda ishga tushiring:

```bash
node server.js
```

Brauzerga `http://localhost:3000` kirib ko'ring.
Sizning yozgan matningiz ekranga chiqadi.

✅ **Tabriklaymiz!** Siz birinchi backend serveringizni ishga tushirdingiz!

---

### Kod qanday ishlaydi?

Keling, har bir qatorni tushunib olaylik:

1. `import express from 'express'` — Express kutubxonasini chaqiramiz
2. `const app = express()` — Serverimizni yaratamiz
3. `const PORT = 3000` — Server qaysi "eshik"da tinglashini belgilaymiz
4. `app.get('/', ...)` — Asosiy manzilga kelgan so'rovga javob beramiz
5. `res.send(...)` — Foydalanuvchiga matn yuboramiz
6. `app.listen(...)` — Serverni ishga tushiramiz

---

### **GET** tushunchasi

Biz `app.get()` ishlatdik. **GET** — bu **so'rov turi**.

* Internetda foydalanuvchi serverdan ma'lumot olish uchun **GET** so'rovi yuboradi.
* Brauzerda har safar manzil kiritganingizda aslida GET yuboriladi.

Misol:

* Siz `https://google.com` deb yozasiz → brauzer Google serveriga **GET** so'rovi yuboradi → server sahifa qaytaradi.

Express'da `app.get('/yo'l', ...)` — "kimdir shu yo'lga GET so'rovi yuborsa, nima javob beramiz?" degani.

---

### Turli yo'llar (Routes) yaratish

"Route" — bu serverdagi manzil yoki sahifa. Xuddi uyingizda turli xonalar bor kabi, serveringizda ham turli yo'llar bo'ladi.

Keling, yana 2 ta yo'l qo'shamiz:

```javascript
import express from 'express';
const app = express();
const PORT = 3000;

// 1-yo'l: Asosiy sahifa
app.get('/', function(req, res) {
  res.send('Salom! Bu asosiy sahifa 🏠');
});

// 2-yo'l: Haqida sahifa
app.get('/about', function(req, res) {
  res.send('Bu — sayt haqida ma'lumot 📖');
});

// 3-yo'l: Kontakt sahifa
app.get('/contact', function(req, res) {
  res.send('Biz bilan bog\'lanish: contact@example.com 📧');
});

app.listen(PORT, function() {
  console.log(`Server ishga tushdi: http://localhost:${PORT}`);
});
```

Endi brauzerda sinab ko'ring:
* `http://localhost:3000/` → "Salom! Bu asosiy sahifa 🏠"
* `http://localhost:3000/about` → "Bu — sayt haqida ma'lumot 📖"
* `http://localhost:3000/contact` → "Biz bilan bog'lanish: ..."

---

### 🎮 Amaliy mashqlar

**1-mashq:** `/hello` degan yo'l yarating

```javascript
app.get('/hello', function(req, res) {
  res.send('Salom, dunyo! 🌍');
});
```

**2-mashq:** `/time` degan yo'l yarating, u hozirgi vaqtni ko'rsatsin

```javascript
app.get('/time', function(req, res) {
  const hozir = new Date();
  res.send(`Hozirgi vaqt: ${hozir.toLocaleTimeString()}`);
});
```

**3-mashq:** `/hobby` degan yo'l yarating, o'zingizning sevimli mashg'ulotingizni yozing

```javascript
app.get('/hobby', function(req, res) {
  res.send('Mening sevimli mashg\'ulotim: dasturlash 💻');
});
```

---

### Kodni yangilash va sinash

Hozir server kodini o'zgartirganda, uni qayta ishga tushirish kerak:

1. Terminalda **CTRL + C** ni bosing (serverni to'xtatish)
2. Yana `node server.js` yozing (qayta ishga tushirish)
3. Brauzerda sahifani yangilang (Refresh/F5)

> Keyingi darsda biz buni avtomatik qilishni o'rganamiz!

---

### 🌟 Ajoyib loyiha: O'zingiz haqingizda mini-sayt

Keling, barcha bilimlaringizni birlashtirgan holda kichik loyiha yarataylik:

```javascript
import express from 'express';
const app = express();
const PORT = 3000;

app.get('/', function(req, res) {
  res.send('<h1>Mening Mini Saytim 🌟</h1><p>Bosh sahifaga xush kelibsiz!</p>');
});

app.get('/about', function(req, res) {
  res.send('<h1>Men haqimda 👤</h1><p>Ismim: [sizning ismingiz]</p><p>Yoshim: 14</p>');
});

app.get('/hobbies', function(req, res) {
  res.send('<h1>Qiziqishlarim 🎯</h1><ul><li>Dasturlash</li><li>Futbol</li><li>Kitob o\'qish</li></ul>');
});

app.get('/contact', function(req, res) {
  res.send('<h1>Bog\'lanish 📞</h1><p>Email: sizning@email.com</p>');
});

app.listen(PORT, function() {
  console.log(`🚀 Mini saytingiz tayyor: http://localhost:${PORT}`);
});
```

**Topshiriq:** Yuqoridagi kodga o'zingiz haqingizdagi ma'lumotlarni qo'ying va ishga tushiring!

---

### Asosiy tushunchalar

* **Express** — serverni tez va oson yaratishga yordam beradi.
* **GET** — ma'lumot so'rash uchun ishlatiladi.
* **Route (yo'l)** — serverdagi manzillar (masalan `/`, `/about`, `/contact`).
* **res.send()** — foydalanuvchiga matn yoki HTML yuboradi.
* **PORT** — server qaysi "eshik"da ishlashi kerak (odatda 3000).

---

### 🏆 Nima o'rgandik?

✅ Express'ni o'rnatdik va ishlatdik
✅ Birinchi serverimizni yaratdik
✅ Bir nechta yo'llar (routes) yaratdik
✅ Brauzerda natijalarni ko'rdik
✅ Kichik loyiha yasadik

**Keyingi darsda:** Serverdan JSON ma'lumot yuborish va Thunder Client bilan ishlashni o'rganamiz! 🎯

---

</details>

<hr>

<details>
    <summary>JSON ma'lumot va Thunder Client</summary>

## 🗓️ 2-hafta — 1-dars

### 🏷️ Mavzu: **JSON ma'lumot va Thunder Client**

---

### 🎯 Bu darsda nima o'rganamiz?

* JSON nima va nega kerak
* `res.json()` va `res.send()` farqi
* Thunder Client'ni qanday ishlatish
* API test qilish

---

### JSON nima? (Qisqa takrorlash)

Birinchi darsda biz JSON haqida bilib olgan edik. Keling, yana bir bor eslaymiz:

**JSON** — bu ma'lumotlarni internet orqali yuborishning eng qulay usuli.

```json
{
  "ism": "Ali",
  "yosh": 14,
  "hobby": "futbol"
}
```

Bu — bitta **obyekt**. Ichida 3 ta ma'lumot bor: ism, yosh va hobby.

---

### res.send() vs res.json()

Oldingi darsda biz `res.send()` ishlatgan edik. Endi yangi narsa o'rganamiz: `res.json()`

**Farq qanday?**

```javascript
// res.send() — oddiy matn yuboradi
app.get('/hello', function(req, res) {
  res.send('Salom, dunyo!');
});

// res.json() — JSON formatda ma'lumot yuboradi
app.get('/user', function(req, res) {
  res.json({
    ism: 'Ali',
    yosh: 14,
    hobby: 'futbol'
  });
});
```

**Qachon qaysi birini ishlatamiz?**
* `res.send()` → oddiy matn yoki HTML uchun
* `res.json()` → ma'lumotlar (obyekt, array) uchun ✅

---

### Birinchi JSON API'miz

Keling, kitoblar ro'yxatini qaytaradigan API yarataylik:

```javascript
import express from 'express';
const app = express();
const PORT = 3000;

// Bitta kitob haqida ma'lumot
app.get('/kitob', function(req, res) {
  res.json({
    nomi: 'Alpomish',
    muallif: 'Xalq og\'zaki ijodi',
    sahifalar: 120,
    til: 'O\'zbek'
  });
});

// Bir nechta kitoblar ro'yxati
app.get('/kitoblar', function(req, res) {
  res.json([
    { nomi: 'Alpomish', muallif: 'Xalq og\'zaki ijodi' },
    { nomi: 'Ufq', muallif: 'Odil Yoqubov' },
    { nomi: 'Kecha va Kunduz', muallif: 'Cho\'lpon' }
  ]);
});

app.listen(PORT, function() {
  console.log(`Server: http://localhost:${PORT}`);
});
```

Brauzerda sinab ko'ring:
* `http://localhost:3000/kitob` → bitta kitob ma'lumoti
* `http://localhost:3000/kitoblar` → kitoblar ro'yxati

---

### Thunder Client nima?

Brauzer faqat **GET** so'rovlarini yuborishi mumkin. Lekin biz keyinroq **POST**, **DELETE** va boshqa so'rovlarni ham yuborishimiz kerak bo'ladi.

**Thunder Client** — bu VS Code ichidagi maxsus vosita. U bizga:
* Har xil turdagi so'rovlar yuborish imkonini beradi
* JSON ma'lumot yuborish va olish oson
* Natijalarni chiroyli ko'rish mumkin

**Oddiy misol:**
Thunder Client — bu pochta bo'limi. Siz server uchun xat (so'rov) yozasiz va serverdan javob olasiz.

---

### Thunder Client o'rnatish

1. VS Code'ni oching
2. Chap tomonda **Extensions** (pazl belgisi) ni bosing
3. Qidiruv qismiga **Thunder Client** yozing
4. **Install** tugmasini bosing
5. Chap tomonda yangi chaqmoqcha 雷 belgisi paydo bo'ladi

✅ Tayyor! Endi ishlatishimiz mumkin.

---

### Thunder Client bilan birinchi test

**1-qadam:** Server ishga tushirilganiga ishonch hosil qiling

```bash
node server.js
```

**2-qadam:** Thunder Client'ni oching
* Chap tomonda **Thunder Client** belgisini bosing
* **New Request** tugmasini bosing

**3-qadam:** So'rov yuboring
* **Method:** GET (default bo'ladi)
* **URL:** `http://localhost:3000/kitoblar`
* **Send** tugmasini bosing

✅ Natija: Kitoblar ro'yxati JSON formatda chiqadi!

---

### 🎮 Amaliy mashqlar

**Mashq 1:** O'yinlar API'si yarating

```javascript
app.get('/oyinlar', function(req, res) {
  res.json([
    { nomi: 'Minecraft', janr: 'Sandbox', yil: 2011 },
    { nomi: 'FIFA 24', janr: 'Sport', yil: 2023 },
    { nomi: 'GTA 5', janr: 'Action', yil: 2013 }
  ]);
});
```

Thunder Client orqali test qiling!

**Mashq 2:** Meva-cheva API'si

```javascript
app.get('/mevalar', function(req, res) {
  res.json([
    { nomi: 'Olma', rang: 'qizil', narx: 5000 },
    { nomi: 'Banan', rang: 'sariq', narx: 8000 },
    { nomi: 'Uzum', rang: 'yashil', narx: 15000 }
  ]);
});
```

**Mashq 3:** O'zingiz haqingizda API

```javascript
app.get('/men', function(req, res) {
  res.json({
    ism: 'Sizning ismingiz',
    yosh: 14,
    maktab: '12-maktab',
    sevimli_fan: 'Informatika',
    qiziqishlar: ['Dasturlash', 'Futbol', 'Rasm chizish']
  });
});
```

---

### Foydali maslahat 💡

**Brauzerdagi natijani chiroyliroq ko'rish:**

Brauzerga maxsus extension o'rnatish mumkin:
* Chrome: **JSON Formatter**
* Firefox: **JSON Lite**

Yoki shunchaki Thunder Client ishlatishingiz mumkin — u avtomatik chiroyli ko'rsatadi!

---

### Asosiy tushunchalar

* **JSON** — ma'lumotlarni internet orqali yuborishning standart usuli
* **res.json()** — JSON formatda javob yuboradi
* **res.send()** — oddiy matn yuboradi
* **Thunder Client** — VS Code ichidagi API test qilish vositasi
* **Array** — bir nechta obyektlar ro'yxati `[{}, {}]`
* **Obyekt** — ma'lumotlar to'plami `{ kalit: qiymat }`

---

### 🏆 Nima o'rgandik?

✅ JSON formatda ma'lumot yuborishni
✅ res.json() va res.send() farqini
✅ Thunder Client'ni o'rnatishni va ishlatishni
✅ API'larni test qilishni
✅ Array va obyekt bilan ishlashni

**Keyingi darsda:** Query parametrlari bilan ishlashni o'rganamiz — foydalanuvchi serverga ma'lumot yuborishi! 🎯

---

</details>

<hr>

<details>
    <summary>Query parametrlari — Foydalanuvchidan ma'lumot olish</summary>

## 🗓️ 2-hafta — 2-dars

### 🏷️ Mavzu: **Query parametrlari — Foydalanuvchidan ma'lumot olish**

---

### 🎯 Bu darsda nima o'rganamiz?

* Query parametrlari nima
* URL orqali ma'lumot qanday yuboriladi
* `req.query` bilan ishlash
* Dinamik javoblar yaratish

---

### Query nima?

**Query** — bu URL oxiriga qo'shiladigan qo'shimcha ma'lumot.

Misol:
```
http://localhost:3000/salom?ism=Ali
```

Bu yerda:
* `?` — query qismi boshlanadi
* `ism` — kalit (key)
* `Ali` — qiymat (value)

**Real hayotdan misol:**
YouTube'da video qidirganingizda:
```
https://www.youtube.com/results?search_query=javascript
```

`search_query=javascript` — bu query parametri!

---

### Birinchi query parametrimiz

Keling, salomlashadigan API yarataylik:

```javascript
import express from 'express';
const app = express();
const PORT = 3000;

app.get('/salom', function(req, res) {
  const ism = req.query.ism;  // URL dan "ism" ni olamiz
  res.send(`Salom, ${ism}!`);
});

app.listen(PORT, function() {
  console.log(`Server: http://localhost:${PORT}`);
});
```

**Sinab ko'ramiz:**
* `http://localhost:3000/salom?ism=Ali` → "Salom, Ali!"
* `http://localhost:3000/salom?ism=Aziza` → "Salom, Aziza!"
* `http://localhost:3000/salom?ism=Sardor` → "Salom, Sardor!"

🎉 Ajoyib! Endi serverimiz foydalanuvchi yuborgan ma'lumotga javob beradi!

---

### Xavfsizlik: Default qiymat berish

Agar foydalanuvchi ism yubormasa nima bo'ladi?

```
http://localhost:3000/salom
```

Javob: "Salom, undefined!" — bu yaxshi emas! 😕

**Yechim:** Default (zaxira) qiymat beramiz:

```javascript
app.get('/salom', function(req, res) {
  const ism = req.query.ism || 'mehmon';  // ism bo'lmasa "mehmon" deb oladi
  res.send(`Salom, ${ism}!`);
});
```

Endi:
* `http://localhost:3000/salom?ism=Ali` → "Salom, Ali!"
* `http://localhost:3000/salom` → "Salom, mehmon!"

✅ Yaxshi! Endi xatolik chiqmaydi.

---

### Bir nechta query parametrlari

Bir vaqtning o'zida bir nechta ma'lumot yuborish mumkin:

```javascript
app.get('/info', function(req, res) {
  const ism = req.query.ism || 'Noma\'lum';
  const yosh = req.query.yosh || 'Noma\'lum';
  const shahar = req.query.shahar || 'Noma\'lum';
  
  res.json({
    ism: ism,
    yosh: yosh,
    shahar: shahar,
    xabar: `${ism} ${yosh} yoshda, ${shahar}dan`
  });
});
```

**Sinab ko'ring:**
```
http://localhost:3000/info?ism=Ali&yosh=14&shahar=Toshkent
```

Natija:
```json
{
  "ism": "Ali",
  "yosh": "14",
  "shahar": "Toshkent",
  "xabar": "Ali 14 yoshda, Toshkentdan"
}
```

**E'tibor bering:** Bir nechta parametrni `&` belgisi bilan ajratamiz:
* 1-parametr: `?ism=Ali`
* 2-parametr: `&yosh=14`
* 3-parametr: `&shahar=Toshkent`

---

### Qidiruv API'si yaratamiz

Real loyihalarning ko'pida qidiruv bor. Keling, oddiy qidiruv API'si yarataylik:

```javascript
// Kitoblar ro'yxati (xotir ichida)
const kitoblar = [
  { id: 1, nomi: 'Alpomish', muallif: 'Xalq og\'zaki ijodi' },
  { id: 2, nomi: 'Ufq', muallif: 'Odil Yoqubov' },
  { id: 3, nomi: 'Kecha va Kunduz', muallif: 'Cho\'lpon' },
  { id: 4, nomi: 'O\'tkan kunlar', muallif: 'Abdulla Qodiriy' }
];

app.get('/qidiruv', function(req, res) {
  const qidiruv = req.query.q || '';  // ?q=Ufq
  
  if (qidiruv === '') {
    return res.json({ xabar: 'Qidiruv so\'zi kiriting', misol: '/qidiruv?q=Ufq' });
  }
  
  // Qidirish (oddiy usul - to'liq mos kelishi kerak)
  const natija = kitoblar.filter(function(kitob) {
    return kitob.nomi.toLowerCase().includes(qidiruv.toLowerCase());
  });
  
  res.json({
    qidiruv_sozi: qidiruv,
    topildi: natija.length,
    kitoblar: natija
  });
});
```

**Sinab ko'ring:**
* `http://localhost:3000/qidiruv?q=Ufq`
* `http://localhost:3000/qidiruv?q=kun`
* `http://localhost:3000/qidiruv?q=Alpomish`

---

### 🎮 Amaliy mashqlar

**Mashq 1:** Kalkulyator API

```javascript
app.get('/hisob', function(req, res) {
  const a = Number(req.query.a) || 0;
  const b = Number(req.query.b) || 0;
  
  res.json({
    a: a,
    b: b,
    yigindi: a + b,
    ayirma: a - b,
    kopaytma: a * b,
    bolish: a / b
  });
});
```

Test: `http://localhost:3000/hisob?a=10&b=5`

**Mashq 2:** Tug'ilgan yildan yoshni hisoblash

```javascript
app.get('/yosh', function(req, res) {
  const tugilgan_yil = Number(req.query.yil);
  const hozirgi_yil = new Date().getFullYear();
  const yosh = hozirgi_yil - tugilgan_yil;
  
  res.json({
    tugilgan_yil: tugilgan_yil,
    hozirgi_yil: hozirgi_yil,
    yosh: yosh,
    xabar: `Siz ${yosh} yoshdasiz`
  });
});
```

Test: `http://localhost:3000/yosh?yil=2010`

**Mashq 3:** Salomlashish tili

```javascript
app.get('/hi', function(req, res) {
  const til = req.query.til || 'uz';
  const ism = req.query.ism || 'Do\'stim';
  
  const salomlar = {
    uz: 'Salom',
    en: 'Hello',
    ru: 'Привет',
    tr: 'Merhaba'
  };
  
  const salom = salomlar[til] || 'Salom';
  
  res.send(`${salom}, ${ism}!`);
});
```

Test:
* `http://localhost:3000/hi?ism=Ali&til=en`
* `http://localhost:3000/hi?ism=Aziza&til=tr`

---

### Thunder Client bilan test qilish

1. Thunder Client'ni oching
2. **New Request** → GET
3. URL yozing: `http://localhost:3000/salom?ism=Ali`
4. Send bosing
5. Query parametrlarini o'zgartiring va yana sinang

**Maslahat:** Thunder Client'da "Query" bo'limi bor — u yerda parametrlarni qulay yozish mumkin!

---

### Asosiy tushunchalar

* **Query** — URL oxiridagi qo'shimcha ma'lumot (`?kalit=qiymat`)
* **req.query** — query parametrlarini olish uchun ishlatiladi
* **Default qiymat** — `|| 'zaxira'` bilan xatoliklardan himoyalanamiz
* **Bir nechta parametr** — `&` belgisi bilan ajratiladi
* **Dinamik javob** — foydalanuvchi yuborgan ma'lumotga qarab javob o'zgaradi

---

### 🏆 Nima o'rgandik?

✅ Query parametrlari nima ekanligini
✅ req.query orqali ma'lumot olishni
✅ Default qiymatlar berishni
✅ Bir nechta parametr bilan ishlashni
✅ Qidiruv API'si yaratishni
✅ Dinamik javoblar qaytarishni

**Keyingi darsda:** Route parametrlari (:id) va Nodemon'ni o'rganamiz! 🚀

---

</details>

<hr>

<details>
    <summary>Route parametrlari va Nodemon</summary>

## 🗓️ 2-hafta — 3-dars

### 🏷️ Mavzu: **Route parametrlari va Nodemon**

---

### 🎯 Bu darsda nima o'rganamiz?

* Route parametrlari (params) nima
* Query va Params farqi
* `:id` bilan ishlash
* Nodemon o'rnatish va ishlatish

---

### Route parametrlari (Params) nima?

**Params** — bu URL'ning o'zida joylashgan ma'lumot.

**Query:**
```
http://localhost:3000/user?id=5
```

**Params:**
```
http://localhost:3000/user/5
```

Ikkalasi ham `5` raqamini yuboradi, lekin **params** yanada chiroyli va tushunarli! ✨

---

### Birinchi params API'miz

```javascript
import express from 'express';
const app = express();
const PORT = 3000;

app.get('/user/:id', function(req, res) {
  const id = req.params.id;  // URL dan ID ni olamiz
  res.send(`Siz ${id}-raqamli foydalanuvchini so'radingiz`);
});

app.listen(PORT, function() {
  console.log(`Server: http://localhost:${PORT}`);
});
```

**Sinab ko'ring:**
* `http://localhost:3000/user/1` → "Siz 1-raqamli foydalanuvchini so'radingiz"
* `http://localhost:3000/user/42` → "Siz 42-raqamli foydalanuvchini so'radingiz"
* `http://localhost:3000/user/999` → "Siz 999-raqamli foydalanuvchini so'radingiz"

**E'tibor bering:** `:id` — bu o'zgaruvchi. Siz uni `:raqam`, `:user_id` yoki boshqa nom bilan ham yozishingiz mumkin.

---

### Real ma'lumot bilan ishlash

Keling, kitoblar ro'yxatidan bitta kitobni ID bo'yicha oladigan API yarataylik:

```javascript
// Kitoblar ro'yxati
const kitoblar = [
  { id: 1, nomi: 'Alpomish', sahifa: 120, yil: 1980 },
  { id: 2, nomi: 'Ufq', sahifa: 200, yil: 1974 },
  { id: 3, nomi: 'Kecha va Kunduz', sahifa: 180, yil: 1936 },
  { id: 4, nomi: 'O\'tkan kunlar', sahifa: 350, yil: 1925 }
];

// Barcha kitoblar
app.get('/kitoblar', function(req, res) {
  res.json(kitoblar);
});

// Bitta kitob (ID bo'yicha)
app.get('/kitoblar/:id', function(req, res) {
  const id = Number(req.params.id);  // ID ni raqamga aylantiramiz
  
  const kitob = kitoblar.find(function(k) {
    return k.id === id;
  });
  
  if (kitob) {
    res.json(kitob);
  } else {
    res.status(404).json({ xato: 'Kitob topilmadi' });
  }
});
```

**Sinab ko'ring:**
* `http://localhost:3000/kitoblar` → Barcha kitoblar
* `http://localhost:3000/kitoblar/1` → Alpomish
* `http://localhost:3000/kitoblar/3` → Kecha va Kunduz
* `http://localhost:3000/kitoblar/999` → Xato: Kitob topilmadi

---

### Bir nechta params

Bir vaqtda bir nechta params ishlatish mumkin:

```javascript
app.get('/sinf/:sinf_raqami/oquvchi/:id', function(req, res) {
  const sinf = req.params.sinf_raqami;
  const id = req.params.id;
  
  res.json({
    sinf: sinf,
    oquvchi_id: id,
    xabar: `${sinf}-sinf, ${id}-raqamli o'quvchi`
  });
});
```

Test: `http://localhost:3000/sinf/7A/oquvchi/15`

---

### Query va Params farqi

| Taqqoslash | Query | Params |
|------------|-------|--------|
| Ko'rinishi | `/search?q=Alpomish` | `/kitoblar/5` |
| Majburiymi? | Yo'q (ixtiyoriy) | Ha (yo'l tarkibi) |
| Qachon ishlatiladi? | Qidiruv, filtr, opsiyalar | Aniq element, ID |
| Misol | YouTube qidiruv | Instagram profil |

**Oddiy qoida:**
* **Params** → aniq biror narsani olish (`/user/5`, `/post/42`)
* **Query** → qo'shimcha sozlamalar (`/search?q=...&limit=10`)

---

### Nodemon — Avtomatik restart

Hozir biz kodni har safar o'zgartirganda serverni to'xtatib, qayta ishga tushirishimiz kerak. Bu noqulay! 😓

**Nodemon** — serverni avtomatik qayta ishga tushiradigan dastur.

### Nodemon o'rnatish

```bash
npm install --save-dev nodemon
```

✅ `--save-dev` — bu dasturni faqat development (dastur yozish) paytida ishlatamiz

### package.json da sozlash

`package.json` faylini oching va `"scripts"` qismiga qo'shing:

```json
{
  "scripts": {
    "start": "nodemon server.js",
    "test": "echo \"Error: no test specified\" && exit 1"
  }
}
```

### Ishga tushirish

Endi odatdagi `node server.js` o'rniga:

```bash
npm start
```

✅ **Ajoyib!** Endi kodni saqlash bilan server avtomatik yangilanadi! 🎉

**Terminalda ko'rishingiz mumkin:**
```
[nodemon] 2.0.20
[nodemon] watching path(s): *.*
[nodemon] watching extensions: js
[nodemon] starting `node server.js`
Server: http://localhost:3000
```

Kodni o'zgartirib saqlaganda:
```
[nodemon] restarting due to changes...
[nodemon] starting `node server.js`
Server: http://localhost:3000
```

---

### 🎮 Amaliy mashqlar

**Mashq 1:** Matematika jadvallar

```javascript
app.get('/jadval/:son', function(req, res) {
  const son = Number(req.params.son);
  const jadval = [];
  
  for (let i = 1; i <= 10; i++) {
    jadval.push(`${son} x ${i} = ${son * i}`);
  }
  
  res.json({
    son: son,
    jadval: jadval
  });
});
```

Test: `http://localhost:3000/jadval/7`

**Mashq 2:** Sport komandalar

```javascript
const jamoalar = [
  { id: 1, nomi: 'Real Madrid', mamlakat: 'Ispaniya', yil: 1902 },
  { id: 2, nomi: 'Barcelona', mamlakat: 'Ispaniya', yil: 1899 },
  { id: 3, nomi: 'Manchester United', mamlakat: 'Angliya', yil: 1878 }
];

app.get('/jamoa/:id', function(req, res) {
  const id = Number(req.params.id);
  const jamoa = jamoalar.find(function(j) {
    return j.id === id;
  });
  
  if (jamoa) {
    res.json(jamoa);
  } else {
    res.json({ xato: 'Jamoa topilmadi' });
  }
});
```

**Mashq 3:** Query va Params birga

```javascript
app.get('/jamoa/:id/oyinchilar', function(req, res) {
  const id = req.params.id;
  const limit = req.query.limit || 10;  // ?limit=5
  
  res.json({
    jamoa_id: id,
    oyinchilar_soni: limit,
    xabar: `${id}-jamoa, ${limit} ta o'yinchi`
  });
});
```

Test: `http://localhost:3000/jamoa/5/oyinchilar?limit=20`

---

### Asosiy tushunchalar

* **Params** — URL'ning o'zi ichidagi o'zgaruvchi (`/user/:id`)
* **req.params** — params'larni olish
* **`:id`** — params nomi (o'zingiz ixtiyoriy nom berishingiz mumkin)
* **Nodemon** — kodni avtomatik qayta ishga tushiradi
* **npm start** — nodemon bilan serverni ishga tushirish
* **Params + Query** — ikkalasini birga ishlatish mumkin

---

### 🏆 Nima o'rgandik?

✅ Route parametrlari (params) bilan ishlashni
✅ Query va Params farqini
✅ ID bo'yicha element olishni
✅ Nodemon'ni o'rnatish va sozlashni
✅ Avtomatik restart'ni yoqishni
✅ Real ma'lumotlar bilan ishlashni

**Keyingi hafta:** POST so'rovlar va ma'lumot yuborishni o'rganamiz! 🚀

---

</details>

<hr>




<details>
    <summary>POST so'rovi va Body ma'lumotlari bilan ishlash</summary>

## 🗓️ 3-hafta — 1-dars

### 🏷️ Mavzu: **POST so'rovi va Body ma'lumotlari bilan ishlash**

---

### 🎯 Bu darsda nima o'rganamiz?

* POST so'rovi nima
* GET va POST farqi
* Body orqali ma'lumot yuborish
* express.json() middleware
* Thunder Client bilan POST test qilish

---

### POST nima?

Avvalgi darslarda biz **GET** so'rovlarini ishlatdik — foydalanuvchi serverdan ma'lumot so'raydi.
**POST** esa buning aksi: foydalanuvchi serverga yangi ma'lumot yuboradi.

* **GET** — ma'lumot olish uchun 📥
* **POST** — ma'lumot yuborish uchun 📤

**Real hayotdan misollar:**

* Telegramda xabar yuborish → POST
* Instagramda rasm yuklash → POST
* Onlayn do'konda yangi buyurtma qilish → POST
* YouTube'ga comment yozish → POST
* Gmail'da email yuborish → POST

---

### GET va POST farqi

|                    | GET                                     | POST                                             |
| ------------------ | --------------------------------------- | ------------------------------------------------ |
| Qayerda ko‘rinadi  | Ma’lumot URL’da ko‘rinadi (`?name=Ali`) | Ma’lumot yashirin (URL’da ko‘rinmaydi)           |
| Qachon ishlatiladi | O‘qish, qidirish, ko‘rish               | Yuborish, saqlash, ro‘yxatdan o‘tish             |
| Ma’lumot hajmi     | Kichik bo‘lishi kerak                   | Ko‘p va katta bo‘lishi mumkin (matn, rasm, fayl) |

---

### POST bilan JSON yuborish

Foydalanuvchi serverga ma'lumot yuborayotganida uni **body** ichiga joylaydi.

**Body nima?**
Body — bu so'rovning ichidagi ma'lumotlar bo'limi. Xuddi konvert ichidagi xat kabi!

**Oddiy misol:**
* GET so'rov — "Menga ma'lumot ber" degan bo'sh konvert 📭
* POST so'rov — "Mana ma'lumot, saqlang" degan to'liq konvert 📬

Bizning server POST ma'lumotni tushunishi uchun Express'da maxsus sozlash kerak:

```javascript
app.use(express.json());
```

Bu qator serverga kelayotgan JSON ma'lumotni o'qib olish imkonini beradi.

**Muhim:** Bu qatorni **app.post() dan oldin** yozish kerak!

---

### Amaliy misol: `/feedback` API

1. `server.js` faylida quyidagilarni yozamiz:

```javascript
import express from 'express';
const app = express();
const PORT = 3000;

// JSON body ma’lumotni o‘qish uchun sozlash
app.use(express.json());

app.post('/feedback', function(req, res) {
  const data = req.body; // foydalanuvchi yuborgan JSON ma'lumot
  console.log(data);     // Terminalga ko'ramiz

  res.json({
    status: 'success',
    message: `Xabaringiz qabul qilindi: "${data.message}"`
  });
});

app.listen(PORT, function() {
  console.log(`Server http://localhost:${PORT} da ishlayapti`);
});
```

✅ Bu yerda:

* `app.use(express.json())` — POST orqali kelgan JSON’ni avtomatik o‘qib beradi.
* `req.body` — foydalanuvchi yuborgan ma’lumotlar.

---

### Thunder Client bilan test qilish

1. Thunder Client oching → **New Request** bosing.
2. Method: **POST**
3. URL: `http://localhost:3000/feedback`
4. **Body** bo‘limiga o‘ting → JSON formatini tanlang.
5. Quyidagicha yozing:

```json
{
  "message": "Backend juda qiziq ekan!"
}
```

6. **Send** tugmasini bosing.

✅ Natija:

```json
{
  "status": "success",
  "message": "Xabaringiz qabul qilindi: \"Backend juda qiziq ekan!\""
}
```

Terminalda esa quyidagiga o‘xshash chiqadi:

```bash
{ message: 'Backend juda qiziq ekan!' }
```

---

### Xatolikdan himoyalanish

Agar foydalanuvchi bo‘sh ma’lumot yuborsa, biz unga xatolik qaytaramiz.

```javascript
app.post('/feedback', function(req, res) {
  const { message } = req.body;

  if (!message) {
    return res.status(400).json({
      status: 'error',
      message: 'Xabar yuborilmadi!'
    });
  }

  res.json({
    status: 'success',
    message: `Xabaringiz qabul qilindi: "${message}"`
  });
});
```

Thunder Client orqali test qiling:

* Agar body bo‘sh bo‘lsa: `{"status":"error","message":"Xabar yuborilmadi!"}`
* To‘g‘ri ma’lumot yuborilsa: “Xabaringiz qabul qilindi …”

---

### Qo‘shimcha mashqlar

1. `/register` route yarating:

```json
{
  "ism": "Ali",
  "email": "ali@gmail.com"
}
```

Server “Xush kelibsiz, Ali!” deb javob qaytarsin.

2. `/comment` route yarating:

```json
{
  "username": "Aziza",
  "comment": "Darslar juda qiziqarli!"
}
```

Server foydalanuvchi nomi va izohini qaytarsin.

---

### Asosiy tushunchalar

* **POST** — serverga yangi ma'lumot yuborish uchun ishlatiladi.
* **Body** — POST so'rovida keladigan ma'lumotlar bo'limi.
* **`express.json()`** — serverga JSON formatdagi ma'lumotni tushuntiradi.
* **`req.body`** — foydalanuvchi yuborgan JSON'ni olish uchun ishlatiladi.
* **Validation** — kelgan ma'lumotni tekshirish (bo'sh yoki noto'g'ri emasligini)

---

### 🏆 Nima o'rgandik?

✅ POST so'rovi nima ekanligini
✅ GET va POST farqini
✅ express.json() middleware'ini
✅ req.body orqali ma'lumot olishni
✅ Thunder Client bilan POST test qilishni
✅ Validation (tekshirish) qo'shishni
✅ Status kod 400 va 201 ishlatishni

**Keyingi darsda:** Bu bilimlar bilan haqiqiy Todos API yaratamiz! 🚀

---
</details>

<hr>


<details>
    <summary>Oddiy Todos API — xotirada ma'lumot saqlash (in-memory)</summary>

## 🗓️ 3-hafta — 2-dars

### 🏷️ Mavzu: **Oddiy Todos API — xotirada ma'lumot saqlash (in-memory)**

---

### 🎯 Bu darsda nima o'rganamiz?

* Array ichida ma'lumot saqlash
* GET va POST'ni birgalikda ishlatish
* HTML forma bilan ma'lumot yuborish
* Haqiqiy API yaratish
* ID avtomatik berish
* Status kodlar (200, 201, 400)

---

### Maqsad

Oldingi darsda biz foydalanuvchi yuborgan ma'lumotni POST orqali qabul qila oldik.
Bugun esa **haqiqiy kichkina API** yasaymiz. Bu API foydalanuvchi yuborgan vazifalarni (todo'larni) xotirada saqlaydi va GET orqali ularni ko'rsatadi.

> 🎯 Bu darsdan keyin siz shunday serverga ega bo'lasiz:
>
> * `POST /todos` — yangi vazifa qo'shish
> * `GET /todos` — barcha vazifalarni ko'rish
> * HTML forma bilan vazifa qo'shish
>
> Xuddi YouTube'da videolar ro'yxati va yangi video yuklash kabi!

---

### Xotira (Memory) nima?

Hozircha biz ma'lumotni fayl yoki bazaga yozmaymiz.
**In-memory** degani — ma'lumot server ishayotgan vaqtida kompyuter xotirasida saqlanadi.
Server o'chsa yoki qayta ishga tushsa, ma'lumot yo'qoladi.

Bu o'quv bosqichida oddiy va tushunarli.

---

### Boshlang'ich kod

`server.js` faylimizni yangilaymiz:

```javascript
import express from 'express';
const app = express();
const PORT = 3000;

// JSON body o'qish
app.use(express.json());

// TODO larni saqlash uchun bo'sh array
let todos = [];
let nextId = 1;  // Keyingi ID uchun o'zgaruvchi

// Barcha TODO larni ko'rsatish
app.get('/todos', function(req, res) {
  res.json(todos);
});

// Yangi TODO qo'shish
app.post('/todos', function(req, res) {
  const { title } = req.body;

  if (!title) {
    return res.status(400).json({
      status: 'error',
      message: 'Todo sarlavhasi kerak!'
    });
  }

  const newTodo = {
    id: nextId,
    title: title,
    completed: false
  };

  todos.push(newTodo);
  nextId = nextId + 1;  // Keyingi ID uchun oshiramiz

  res.status(201).json({
    status: 'success',
    todo: newTodo
  });
});

app.listen(PORT, function() {
  console.log(`Server ishga tushdi: http://localhost:${PORT}`);
});
```

---

### Kodni tushuntirish

* `let todos = []` — vazifalar ro'yxati saqlanadigan bo'sh array.
* `let nextId = 1` — har bir yangi vazifaga beradigan ID raqami.
* `app.get('/todos')` — barcha vazifalarni JSON qilib qaytaradi.
* `app.post('/todos')` — yangi vazifa qabul qiladi va ro'yxatga qo'shadi.
* `id: nextId` — har bir vazifaga tartib raqami beramiz.
* `nextId = nextId + 1` — keyingi vazifa uchun ID'ni 1 ga oshiramiz.
* `completed` — vazifa bajarilgan yoki yo'qligini bilish uchun.

---

### Thunder Client bilan sinash

#### 1. Yangi vazifa qo'shish

* Method: POST
* URL: `http://localhost:3000/todos`
* Body → JSON format:

```json
{
  "title": "Uy vazifasini qilish"
}
```

**Natija:**

```json
{
  "status": "success",
  "todo": {
    "id": 1,
    "title": "Uy vazifasini qilish",
    "completed": false
  }
}
```

#### 2. Yana bir vazifa qo'shamiz

```json
{
  "title": "Kitob o'qish"
}
```

**Natija:**

```json
{
  "status": "success",
  "todo": {
    "id": 2,
    "title": "Kitob o'qish",
    "completed": false
  }
}
```

#### 3. Barcha vazifalarni ko'rish

* Method: GET
* URL: `http://localhost:3000/todos`

**Natija:**

```json
[
  { "id": 1, "title": "Uy vazifasini qilish", "completed": false },
  { "id": 2, "title": "Kitob o'qish", "completed": false }
]
```

---

### 🌐 HTML Forma bilan ma'lumot yuborish

Endi HTML sahifa yaratib, forma orqali vazifa qo'shishni ko'ramiz.

**1-qadam:** HTML fayl yarating (`public/index.html`):

```html
<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Vazifalar Ro'yxati</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      max-width: 600px;
      margin: 50px auto;
      padding: 20px;
      background: #f5f5f5;
    }
    h1 {
      color: #333;
      text-align: center;
    }
    .form-container {
      background: white;
      padding: 20px;
      border-radius: 8px;
      margin-bottom: 20px;
    }
    input[type="text"] {
      width: 70%;
      padding: 10px;
      font-size: 16px;
      border: 1px solid #ddd;
      border-radius: 4px;
    }
    button {
      padding: 10px 20px;
      font-size: 16px;
      background: #4CAF50;
      color: white;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }
    button:hover {
      background: #45a049;
    }
    #todoList {
      background: white;
      padding: 20px;
      border-radius: 8px;
    }
    .todo-item {
      padding: 10px;
      margin: 5px 0;
      background: #f9f9f9;
      border-left: 4px solid #4CAF50;
      border-radius: 4px;
    }
  </style>
</head>
<body>
  <h1>📝 Mening Vazifalarim</h1>
  
  <div class="form-container">
    <h3>Yangi vazifa qo'shish</h3>
    <form id="todoForm">
      <input 
        type="text" 
        id="todoInput" 
        placeholder="Vazifani kiriting..."
        required
      >
      <button type="submit">Qo'shish</button>
    </form>
  </div>

  <div id="todoList">
    <h3>Vazifalar ro'yxati:</h3>
    <div id="todos"></div>
  </div>

  <script>
    const form = document.getElementById('todoForm');
    const input = document.getElementById('todoInput');
    const todosDiv = document.getElementById('todos');

    // Barcha vazifalarni yuklash
    function loadTodos() {
      fetch('http://localhost:3000/todos')
        .then(function(response) {
          return response.json();
        })
        .then(function(todos) {
          todosDiv.innerHTML = '';
          
          // Har bir vazifani ko'rsatish (oddiy for loop)
          for (let i = 0; i < todos.length; i++) {
            const todo = todos[i];
            const div = document.createElement('div');
            div.className = 'todo-item';
            div.textContent = todo.id + '. ' + todo.title;
            todosDiv.appendChild(div);
          }
        })
        .catch(function(error) {
          console.log('Xato:', error);
        });
    }

    // Forma yuborilganda
    form.addEventListener('submit', function(event) {
      event.preventDefault();  // Sahifani yangilanishini to'xtatish
      
      const title = input.value;
      
      // Serverga POST so'rov yuborish
      fetch('http://localhost:3000/todos', {
        method: 'POST',
        headers: {
          'Content-Type': 'application/json'
        },
        body: JSON.stringify({ title: title })
      })
      .then(function(response) {
        return response.json();
      })
      .then(function(data) {
        console.log('Muvaffaqiyat:', data);
        input.value = '';  // Inputni tozalash
        loadTodos();  // Ro'yxatni yangilash
      })
      .catch(function(error) {
        console.log('Xato:', error);
      });
    });

    // Sahifa yuklanganida vazifalarni ko'rsatish
    loadTodos();
  </script>
</body>
</html>
```

**2-qadam:** Server.js ga static fayl xizmati qo'shish:

```javascript
import express from 'express';
const app = express();
const PORT = 3000;

// JSON body o'qish
app.use(express.json());

// Static fayllar uchun (HTML, CSS, JS)
app.use(express.static('public'));

// ... qolgan kod ...
```

**3-qadam:** `public` papkasini yarating va `index.html` ni ichiga qo'ying.

**4-qadam:** Brauzerda oching: `http://localhost:3000/index.html`

---

### 🌟 Kengaytirish: PATCH va DELETE (oddiy usul)

Endi API'mizni yanada kuchliroq qilamiz! Vazifalarni o'zgartirish va o'chirish imkoniyatini qo'shamiz.

#### PATCH — Vazifani bajarilgan/bajarilmagan qilish

```javascript
app.patch('/todos/:id', function(req, res) {
  const id = parseInt(req.params.id);
  let foundTodo = null;
  
  // Oddiy for loop bilan todo topish
  for (let i = 0; i < todos.length; i++) {
    if (todos[i].id === id) {
      foundTodo = todos[i];
      break;
    }
  }

  if (!foundTodo) {
    return res.status(404).json({ message: 'Todo topilmadi' });
  }

  foundTodo.completed = !foundTodo.completed;
  res.json({ status: 'success', todo: foundTodo });
});
```

---

#### DELETE — Vazifani o'chirish (oddiy usul)

```javascript
app.delete('/todos/:id', function(req, res) {
  const id = parseInt(req.params.id);
  let foundIndex = -1;
  
  // Oddiy for loop bilan index topish
  for (let i = 0; i < todos.length; i++) {
    if (todos[i].id === id) {
      foundIndex = i;
      break;
    }
  }
  
  if (foundIndex === -1) {
    return res.status(404).json({ xato: 'Todo topilmadi' });
  }
  
  // Array dan element o'chirish (oddiy usul)
  const ochirilgan = todos[foundIndex];
  const yangiTodos = [];
  
  for (let i = 0; i < todos.length; i++) {
    if (i !== foundIndex) {
      yangiTodos.push(todos[i]);
    }
  }
  
  todos = yangiTodos;
  
  res.json({ 
    xabar: 'Todo o\'chirildi', 
    todo: ochirilgan 
  });
});
```

---

### 🎮 Qo'shimcha mashqlar (oddiy usul bilan)

**Mashq 1:** `/count` — Vazifalar sonini ko'rsatish

```javascript
app.get('/count', function(req, res) {
  let bajarilganSoni = 0;
  let bajarilmaganSoni = 0;
  
  for (let i = 0; i < todos.length; i++) {
    if (todos[i].completed) {
      bajarilganSoni = bajarilganSoni + 1;
    } else {
      bajarilmaganSoni = bajarilmaganSoni + 1;
    }
  }
  
  res.json({ 
    jami: todos.length,
    bajarilgan: bajarilganSoni,
    bajarilmagan: bajarilmaganSoni
  });
});
```

**Mashq 2:** `/clear` — Barcha vazifalarni tozalash

```javascript
app.post('/clear', function(req, res) {
  const soni = todos.length;
  todos = [];
  nextId = 1;  // ID ni ham qaytadan 1 dan boshlaymiz
  res.json({ xabar: soni + ' ta vazifa o\'chirildi' });
});
```

**Mashq 3:** `/completed` — Faqat bajarilgan vazifalar

```javascript
app.get('/completed', function(req, res) {
  const bajarilganlar = [];
  
  for (let i = 0; i < todos.length; i++) {
    if (todos[i].completed === true) {
      bajarilganlar.push(todos[i]);
    }
  }
  
  res.json(bajarilganlar);
});
```

---

### Asosiy tushunchalar

* **In-memory** — ma'lumot server xotirasida saqlanadi (o'chsa yo'qoladi).
* **GET** — saqlangan ma'lumotni olish.
* **POST** — yangi ma'lumot qo'shish.
* **PATCH** — mavjud ma'lumotni o'zgartirish.
* **DELETE** — ma'lumotni o'chirish.
* **Array** — bir nechta obyektlarni tartibli saqlash uchun.
* **Status kodlar** — 200 (OK), 201 (yaratildi), 400 (xato), 404 (topilmadi).
* **HTML Form + fetch()** — brauzerdan serverga ma'lumot yuborish.
* **For loop** — arrayni tekshirish uchun oddiy usul.

---

### 🏆 Nima o'rgandik?

✅ Haqiqiy API yaratishni (GET + POST)
✅ Array'da ma'lumot saqlashni
✅ PATCH va DELETE operatsiyalarini
✅ ID avtomatik berishni
✅ Xatolarni to'g'ri qaytarishni
✅ CRUD amaliyotlarini
✅ HTML forma bilan ma'lumot yuborishni
✅ Oddiy for loop bilan array'da ishlashni

**Keyingi hafta:** Ma'lumotni xotirada emas, faylda saqlashni o'rganamiz — server o'chsa ham ma'lumot saqlanadi! 💾

---

</details>

<hr>

<details>
    <summary>Ma'lumotni xotirada emas, faylda saqlash (Database va Memory tushunchasi)</summary>

## 🗓️ 4-hafta — 1-dars

### 🏷️ Mavzu: **Ma'lumotni xotirada emas, faylda saqlash (Database va Memory tushunchasi)**

---

### 🎯 Bu darsda nima o'rganamiz?

* Memory (xotira) nima va uning muammolari
* Database (ma'lumotlar bazasi) nima
* Nega ma'lumotni faylda saqlash kerak
* lowdb kutubxonasi bilan tanishuv
* JSON faylda ma'lumot saqlash

---

### Xotira (Memory) nima va uning cheklovlari

O‘tgan darsda biz “Todos” ma’lumotini **memory (RAM)** ichida saqladik:

```javascript
let todos = [];
```

Bu juda oddiy va tez, lekin katta muammo bor:

> **Serverni to‘xtatsak yoki kompyuterni o‘chirib yonsak, barcha ma’lumot yo‘qoladi.**

**Sababi:** RAM — vaqtinchalik xotira. Kompyuter o‘chsa, undagi hamma narsa yo‘q bo‘ladi.

💡 Oddiy misol:

* Siz daftar o‘rniga doskaga yozyapsiz. Dars tugab doska artib yuborilsa — hamma yozganlaringiz yo‘qoladi.
* Xotira ham xuddi shunday, server to‘xtaganda ma’lumot ham ketadi.

---

### Database nima?

**Database (ma’lumotlar bazasi)** — ma’lumotni saqlab qoladigan joy.
Server o‘chsa ham ma’lumot qoladi. Keyingi safar server ishga tushganda uni qayta o‘qib olish mumkin.

Oddiy ko‘rinishda database shunday ish qiladi:

1. Server yangi ma’lumot oladi (masalan, todo qo‘shish).
2. Uni faylga yoki ma’lumotlar bazasiga yozadi.
3. Keyingi safar shu fayldan yoki bazadan o‘qiydi.

---

### Hozircha JSON fayl ishlatamiz

Biz hali katta, murakkab bazalarga (MySQL, MongoDB) o‘tmaymiz.
Hozir biz uchun eng oddiy va tushunarli usul — **JSON faylga yozish**.

JSON fayl — xuddi katta daftar kabi. Server har safar ma’lumotni yozadi, biz keyin uni qayta o‘qib olamiz.

> Bu degani: endi yozgan vazifalarimiz server o‘chsa ham saqlanadi.

---

### lowdb nima?

**lowdb** — Node.js uchun oddiy kutubxona bo‘lib, u JSON faylni ma’lumotlar bazasi sifatida ishlatish imkonini beradi.

* Kod oddiy.
* Kichkina loyihalar va o‘rganish uchun juda qulay.
* Hech qanday qo‘shimcha server kerak emas.

Biz bugun lowdb’ni tanishtiramiz va keyingi darsda undan foydalana boshlaymiz.

---

### lowdb o‘rnatish

Terminalda yozing:

```bash
npm install lowdb
```

Shu bilan loyiha papkasiga lowdb qo‘shiladi.

---

### lowdb bilan ishlashga kirishish

Avval oddiy fayl yaratamiz va ichiga yozib o‘qishni ko‘ramiz.

#### 1. Fayl yaratish va yozish

`server.js` faylida:

```javascript
import { Low } from 'lowdb'
import { JSONFile } from 'lowdb/node'

const adapter = new JSONFile('db.json') // ma'lumot saqlanadigan fayl
const db = new Low(adapter, { todos: [] }) // boshlang'ich bo'sh massiv

await db.read() // db.json bor bo'lsa o'qiydi, yo'q bo'lsa yaratadi
db.data.todos.push({ id: 1, title: 'Backend o'rganish', completed: false })
await db.write() // faylga yozadi

console.log('DB ichidagi ma'lumot:', db.data)
```

Keyin terminalda ishga tushiring:

```bash
node server.js
```

✅ Loyihangiz papkasida `db.json` fayli yaratiladi va ichida quyidagi yozuv bo‘ladi:

```json
{
  "todos": [
    { "id": 1, "title": "Backend o‘rganish", "completed": false }
  ]
}
```

Bu juda muhim o‘zgarish: endi ma’lumot faylga saqlanadi va server qayta ishga tushganda ham yo‘qolmaydi.

---

### Memory va Database taqqoslash

|                    | Memory (RAM)                     | Fayl / Database (JSON yoki haqiqiy DB) |
| ------------------ | -------------------------------- | -------------------------------------- |
| Tezlik             | Juda tez                         | Biroz sekinroq                         |
| Saqlanish          | Server o‘chsa ma’lumot yo‘qoladi | Ma’lumot saqlanadi                     |
| Oddiyligi          | Juda oddiy                       | Biroz sozlash kerak                    |
| Qachon ishlatamiz? | Sinov va mashq uchun             | Haqiqiy loyihalarda                    |

---

### Amaliy mashq

1. Loyihangizda `db.json` degan bo‘sh fayl yarating:

```json
{
  "todos": []
}
```

2. `server.js` faylida lowdb’ni o‘rnating va bir nechta todo yozib saqlang.

```javascript
import { Low } from 'lowdb'
import { JSONFile } from 'lowdb/node'

const adapter = new JSONFile('db.json')
const db = new Low(adapter, { todos: [] })

await db.read()

db.data.todos.push({ id: 1, title: 'Bugungi uy vazifasi', completed: false })
db.data.todos.push({ id: 2, title: 'Sport zalga borish', completed: false })

await db.write()

console.log('Saqlangan ma’lumotlar:', db.data.todos)
```

3. Terminalda ishga tushiring:
   `node server.js`
   Keyin `db.json` faylini ochib, yozilgan ma’lumotlarni ko‘ring.

---

### Asosiy tushunchalar

* **Memory** — vaqtinchalik xotira, server to'xtasa ma'lumot yo'qoladi.
* **Database** — ma'lumotni doimiy saqlash joyi.
* **JSON fayl** — oddiy ko'rinishdagi kichik database.
* **lowdb** — JSON faylni database sifatida ishlatish uchun juda oddiy va qulay kutubxona.
* **Persistence** — ma'lumotning doimiy saqlanishi

---

### 🏆 Nima o'rgandik?

✅ Memory va Database farqini
✅ Nega ma'lumotni saqlash kerakligini
✅ lowdb kutubxonasi nima ekanligini
✅ JSON faylga ma'lumot yozish va o'qishni
✅ await db.read() va await db.write()
✅ Ma'lumot yo'qolmasligi uchun yechim

**Keyingi darsda:** Todos API'ni lowdb bilan to'liq ishlaydigan qilamiz! 💾

---
</details>

<hr>

<details>
    <summary>lowdb bilan oddiy ma'lumotlar bazasini sozlash va Todos API'ni saqlash</summary>

## 🗓️ 4-hafta — 2-dars

### 🏷️ Mavzu: **lowdb bilan oddiy ma'lumotlar bazasini sozlash va Todos API'ni saqlash**

---

### 🎯 Bu darsda nima o'rganamiz?

* lowdb'ni loyihaga ulash
* db.json fayl yaratish
* API'ni lowdb bilan ishlashga o'zgartirish
* await db.read() va await db.write()
* Doimiy saqlash (persistence)

---

### lowdb bilan ishlashni boshlash

Oldingi darsda biz **memory** va **database** farqini o'rgandik va lowdb kutubxonasini ko'rdik. Bugun esa bizning **Todos API**'mizni to'liq **db.json** fayliga ulaymiz. 

> 🎉 Eng katta o'zgarish: Endi ma'lumotlar server o'chsa ham saqlanib qoladi!

---

### 1️⃣ lowdb o‘rnatish

Agar hali o‘rnatilmagan bo‘lsa, terminalda yozing:

```bash
npm install lowdb
```

> Bu kutubxona orqali biz JSON fayl bilan oddiy database sifatida ishlay olamiz.

---

### 2️⃣ Yangi db.json fayl yaratish

Loyihangizning ichida `db.json` nomli bo‘sh fayl yarating va quyidagicha yozing:

```json
{
  "todos": []
}
```

* `"todos"` — bu bizning ro‘yxatimiz nomi.
* Hozircha bo‘sh, keyinchalik bizning API bu faylga yozadi.

---

### 3️⃣ lowdb’ni ulash va sozlash

`server.js` faylingizni yangilang:

```javascript
import express from 'express'
import { Low } from 'lowdb'
import { JSONFile } from 'lowdb/node'

const app = express()
const PORT = 3000

app.use(express.json()) // POST so‘rovlar uchun body o‘qish

// 1. lowdb adapter va db o‘rnatamiz
const adapter = new JSONFile('db.json')      // ma’lumotlar saqlanadigan fayl
const db = new Low(adapter, { todos: [] })   // boshlang‘ich ma’lumot

// 2. Fayldan ma’lumotlarni o‘qish
await db.read()

// Agar db.json bo‘sh bo‘lsa, default qiymat beramiz
db.data ||= { todos: [] }
```

✅ Endi bizning `db` o‘zgaruvchimiz orqali fayldagi ma’lumot bilan ishlashimiz mumkin.

---

### 4️⃣ GET /todos — ma’lumotni o‘qish

```javascript
app.get('/todos', function(req, res) {
  res.json(db.data.todos)
})
```

Bu orqali biz fayldagi barcha todos ro‘yxatini qaytarib beramiz.

---

### 5️⃣ POST /todos — yangi todo qo‘shish

```javascript
app.post('/todos', async function(req, res) {
  const { title } = req.body

  if (!title) {
    return res.status(400).json({ status: 'error', message: 'Todo nomi kerak!' })
  }

  const newTodo = {
    id: db.data.todos.length + 1,
    title,
    completed: false
  }

  db.data.todos.push(newTodo)  // ro'yxatga qo'shamiz
  await db.write()             // faylga yozamiz

  res.status(201).json({ status: 'success', todo: newTodo })
})
```

✅ Muhim:

* `await db.write()` — o‘zgartirishlarni faylga yozadi, shunda saqlanadi.
* `db.data.todos` — bu JSON ichidagi massiv.

---

### 6️⃣ Serverni ishga tushirish

`package.json` da agar hali bo‘lmasa:

```json
"scripts": {
  "start": "nodemon server.js"
}
```

Keyin terminalda:

```bash
npm start
```

---

### 7️⃣ Thunder Client orqali test qilish

#### A. Yangi todo qo‘shish (POST)

* Method: **POST**
* URL: `http://localhost:3000/todos`
* Body → JSON:

```json
{
  "title": "Node.js dars qilish"
}
```

Natija:

```json
{
  "status": "success",
  "todo": {
    "id": 1,
    "title": "Node.js dars qilish",
    "completed": false
  }
}
```

`db.json` faylida ham shu yozuv paydo bo‘lganini ko‘rasiz.

#### B. Yana todo qo‘shish

```json
{
  "title": "Sport zalga borish"
}
```

Natija:

```json
{
  "status": "success",
  "todo": {
    "id": 2,
    "title": "Sport zalga borish",
    "completed": false
  }
}
```

`db.json` faylida endi ikkita element bor.

#### C. Barcha todo’larni olish (GET)

* Method: **GET**
* URL: `http://localhost:3000/todos`

Natija:

```json
[
  { "id": 1, "title": "Node.js dars qilish", "completed": false },
  { "id": 2, "title": "Sport zalga borish", "completed": false }
]
```

---

### 8️⃣ Qo‘shimcha xavfsizlik

Agar foydalanuvchi bo‘sh `title` yuborsa, server 400 xato qaytaradi.
Bu yaxshi odat — foydalanuvchi noto‘g‘ri ma’lumot yuborishi mumkin.

---

### Amaliy mashqlar

1. **Delete route qo‘shing:**
   `DELETE /todos/:id` → todo’ni id bo‘yicha o‘chirib tashlash.

2. **Completed qiymatini o‘zgartirish:**
   `PATCH /todos/:id` → todo bajarilganligini o‘zgartiring.

Masalan:

```javascript
app.patch('/todos/:id', async function(req, res) {
  const { id } = req.params
  const todo = db.data.todos.find(function(t) {
    return t.id === parseInt(id)
  })

  if (!todo) return res.status(404).json({ message: 'Todo topilmadi' })

  todo.completed = !todo.completed
  await db.write()

  res.json({ status: 'success', todo })
})
```

---

### Asosiy tushunchalar

* **lowdb** — JSON faylni oddiy database sifatida ishlatadi.
* **await db.read()** — fayldan ma'lumotni o'qiydi.
* **await db.write()** — ma'lumotni faylga yozadi.
* **GET /todos** — ma'lumotlarni olish.
* **POST /todos** — yangi ma'lumot qo'shish va saqlash.
* **db.data** — fayldagi ma'lumotlarga murojaat qilish

---

### 🏆 Nima o'rgandik?

✅ lowdb'ni Express bilan birlashtirishni
✅ db.json faylini yaratish va sozlashni
✅ await db.read() va db.write() ishlatishni
✅ API'ni lowdb bilan ishlashga o'zgartirishni
✅ Ma'lumotni doimiy saqlashni
✅ Server o'chib-yonganida ham ma'lumot saqlanishini

**Keyingi darsda:** To'liq CRUD (DELETE va PUT/PATCH) qo'shamiz! 🎯

---
</details>

<hr>


<details>
    <summary>CRUD to'liq: DELETE va PUT/PATCH bilan yakunlash (lowdb)</summary>

## 🗓️ 4-hafta — 3-dars

### 🏷️ Mavzu: **CRUD to'liq: DELETE va PUT/PATCH bilan yakunlash (lowdb)**

---

### 🎯 Bu darsda nima o'rganamiz?

* DELETE operatsiyasi (o'chirish)
* PATCH operatsiyasi (qisman yangilash)
* PUT operatsiyasi (to'liq yangilash)
* To'liq CRUD API yaratish
* Thunder Client bilan test qilish

---

### CRUD nima?

**CRUD** — bu har bir API'da bo'lishi kerak bo'lgan 4 ta asosiy operatsiya:

* **C**reate — yaratish (POST)
* **R**ead — o'qish (GET)
* **U**pdate — yangilash (PUT/PATCH)
* **D**elete — o'chirish (DELETE)

Bu darsda Todos API'miz to'liq **CRUD** holatiga keladi:

* **DELETE `/todos/:id`** — todo'ni o'chirish
* **PATCH `/todos/:id`** — todo'ni qisman yangilash (masalan, `completed`ni belgilash)
* **PUT `/todos/:id`** — todo'ni to'liq yangilash

> Quyidagi kodlar oldingi darsdagi **ESM** (import) uslubiga mos: `package.json` ichida `"type": "module"` bor deb hisoblaymiz.

---

### 1) Boshlang‘ich loyiha (oldingi darsdan)

`server.js`:

```javascript
import express from 'express'
import { Low } from 'lowdb'
import { JSONFile } from 'lowdb/node'

const app = express()
const PORT = 3000

app.use(express.json())

const adapter = new JSONFile('db.json')
const db = new Low(adapter, { todos: [] })
await db.read()
db.data ||= { todos: [] }   // agar bo‘sh bo‘lsa, default

// READ: Barcha todo'lar
app.get('/todos', function(req, res) {
  res.json(db.data.todos)
})

// CREATE: Yangi todo
app.post('/todos', async function(req, res) {
  const { title } = req.body
  if (!title) {
    return res.status(400).json({ status: 'error', message: 'Todo nomi kerak!' })
  }

  const newTodo = {
    id: db.data.todos.length ? Math.max(...db.data.todos.map(function(t) { return t.id })) + 1 : 1,
    title,
    completed: false
  }

  db.data.todos.push(newTodo)
  await db.write()

  res.status(201).json({ status: 'success', todo: newTodo })
})
```

> Eslatma: `id` qiymatini **takrorlanmas** qilish uchun `Math.max(...ids)+1` usulidan foydalandik.

---

### 2) DELETE `/todos/:id` — O‘chirish

**Maqsad:** berilgan `id` bo‘yicha todo’ni topish, topilsa massivdan olib tashlash, bazaga yozish.

```javascript
// DELETE: Todo o'chirish
app.delete('/todos/:id', async function(req, res) {
  const id = Number(req.params.id)

  // noto'g'ri id yuborilsa
  if (Number.isNaN(id)) {
    return res.status(400).json({ status: 'error', message: 'Noto'g'ri ID' })
  }

  const index = db.data.todos.findIndex(function(t) {
    return t.id === id
  })

  if (index === -1) {
    return res.status(404).json({ status: 'error', message: 'Todo topilmadi' })
  }

  const [removed] = db.data.todos.splice(index, 1)
  await db.write()

  res.json({ status: 'success', removed })
})
```

**Kutilgan javob:**

```json
{
  "status": "success",
  "removed": { "id": 2, "title": "Sport zalga borish", "completed": false }
}
```

---

### 3) PATCH `/todos/:id` — `completed` ni belgilash/almashish

**Maqsad:** mavjud todo’ning faqat **bir qismini** yangilash. PATCH ko‘pincha **qisman** yangilash uchun ishlatiladi.

#### Variant A — `completed` qiymatini **toggle** (teskari) qilish:

```javascript
// PATCH: completed ni teskari qilish (true <-> false)
app.patch('/todos/:id', async function(req, res) {
  const id = Number(req.params.id)
  if (Number.isNaN(id)) {
    return res.status(400).json({ status: 'error', message: 'Noto'g'ri ID' })
  }

  const todo = db.data.todos.find(function(t) {
    return t.id === id
  })
  if (!todo) {
    return res.status(404).json({ status: 'error', message: 'Todo topilmadi' })
  }

  todo.completed = !todo.completed
  await db.write()

  res.json({ status: 'success', todo })
})
```

#### Variant B — `completed` ni **aniq qiymat**ga o‘rnatish:

```javascript
// PATCH: completed ni aniq qiymatga o'rnatish (body: { completed: true/false })
app.patch('/todos/:id/complete', async function(req, res) {
  const id = Number(req.params.id)
  const { completed } = req.body

  if (Number.isNaN(id)) {
    return res.status(400).json({ status: 'error', message: 'Noto'g'ri ID' })
  }
  if (typeof completed !== 'boolean') {
    return res.status(400).json({ status: 'error', message: 'completed true/false bo'lishi kerak' })
  }

  const todo = db.data.todos.find(function(t) {
    return t.id === id
  })
  if (!todo) {
    return res.status(404).json({ status: 'error', message: 'Todo topilmadi' })
  }

  todo.completed = completed
  await db.write()

  res.json({ status: 'success', todo })
})
```

---

### 4) PUT `/todos/:id` — to‘liq yangilash (ixtiyoriy, lekin foydali)

**PUT** odatda obyektni **to‘liq** almashtirish uchun ishlatiladi (majburiy maydonlarni qayta yuborasiz).

```javascript
// PUT: to'liq yangilash (title va completed talab qilinadi)
app.put('/todos/:id', async function(req, res) {
  const id = Number(req.params.id)
  const { title, completed } = req.body

  if (Number.isNaN(id)) {
    return res.status(400).json({ status: 'error', message: 'Noto'g'ri ID' })
  }
  if (typeof title !== 'string' || !title.trim()) {
    return res.status(400).json({ status: 'error', message: 'title talab qilinadi' })
  }
  if (typeof completed !== 'boolean') {
    return res.status(400).json({ status: 'error', message: 'completed true/false bo'lishi kerak' })
  }

  const index = db.data.todos.findIndex(function(t) {
    return t.id === id
  })
  if (index === -1) {
    return res.status(404).json({ status: 'error', message: 'Todo topilmadi' })
  }

  const updated = { id, title: title.trim(), completed }
  db.data.todos[index] = updated
  await db.write()

  res.json({ status: 'success', todo: updated })
})
```

---

### 5) Serverni ishga tushirish

```javascript
app.listen(PORT, function() {
  console.log(`Server: http://localhost:${PORT}`)
})
```

> `npm start` (agar `scripts.start = "nodemon server.js"` bo‘lsa) yoki `node server.js`.

---

## Thunder Client’da sinov ssenariylari (Activity)

**1. CREATE (POST `/todos`)**
Body (JSON):

```json
{ "title": "Matematika uy vazifasi" }
```

Kutilgan: `201 Created`, qaytishda yangi `todo`.

**2. READ (GET `/todos`)**
Kutilgan: mavjud ro‘yxat (array).

**3. UPDATE (PATCH `/todos/:id`) – toggle**
URL: `/todos/1` (Method: PATCH)
Kutilgan: `completed` qiymati teskari bo‘ladi.

**4. UPDATE (PATCH `/todos/:id/complete`) – set**
URL: `/todos/1/complete` (Method: PATCH)
Body:

```json
{ "completed": true }
```

Kutilgan: `completed: true`.

**5. UPDATE (PUT `/todos/:id`) – full replace**
URL: `/todos/1` (Method: PUT)
Body:

```json
{ "title": "Matematika uy vazifasi (yangilandi)", "completed": false }
```

**6. DELETE (DELETE `/todos/:id`)**
URL: `/todos/1` (Method: DELETE)
Kutilgan: `removed` obyekt qaytadi.
Keyin **GET `/todos`** bilan ro‘yxatdan yo‘qolganini tekshiring.

---

### Status kodlar (foydalanilayotganlari)

* **200 OK** — muvaffaqiyatli.
* **201 Created** — yangi obyekt yaratildi (POST).
* **400 Bad Request** — noto‘g‘ri ma’lumot.
* **404 Not Found** — topilmadi.

---

### Yakuniy holat

Endi sizning "Todos API"ngiz to'liq **CRUD** funksiyalariga ega:

* **POST** `/todos` — yaratish (Create)
* **GET** `/todos` — o'qish (Read)
* **PATCH/PUT** `/todos/:id` — yangilash (Update)
* **DELETE** `/todos/:id` — o'chirish (Delete)

---

### 🏆 Nima o'rgandik?

✅ To'liq CRUD operatsiyalarini
✅ DELETE so'rovi bilan ishlashni
✅ PATCH va PUT farqini
✅ Ma'lumotni faylda saqlashni
✅ Haqiqiy API yaratishni
✅ lowdb bilan professional ishlashni

**Keyingi darsda (Darslik_2.md):** Haqiqiy ma'lumotlar bazasi (SQLite) bilan ishlashni o'rganamiz! 🚀

---

### 💡 Siz allaqachon bilib olgansiz:

1. ✅ Internet va Backend qanday ishlashini
2. ✅ Node.js va npm bilan ishlashni
3. ✅ Express bilan server yaratishni
4. ✅ Routes (yo'llar) yaratishni
5. ✅ Query va Params bilan ishlashni
6. ✅ JSON formatida ma'lumot yuborishni
7. ✅ Thunder Client bilan test qilishni
8. ✅ POST orqali ma'lumot qabul qilishni
9. ✅ In-memory ma'lumot saqlashni
10. ✅ To'liq CRUD API yaratishni
11. ✅ lowdb bilan faylga ma'lumot yozishni
12. ✅ Doimiy ma'lumot saqlanishini (persistence)

**Siz endi haqiqiy backend dasturchi sifatida ishlashingiz mumkin!** 🎉👏

---

</details>

<hr>