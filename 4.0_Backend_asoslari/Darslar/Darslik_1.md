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
---

## 🗓️ 1-hafta — 3-dars

### 🏷️ Mavzu: **Express bilan birinchi server**

---

### Express nima va nega kerak?

Node.js bilan ham server yozish mumkin, lekin har safar ko‘p kod yozish kerak bo‘ladi va chalkash bo‘lib ketadi.
**Express** — bu Node.js uchun yozilgan maxsus kutubxona (tayyor kodlar to‘plami).
Biz undan foydalansak:

* Serverni juda tez ishga tushira olamiz.
* Turli manzillar (yo‘llar) yaratib, turli ma’lumot yubora olamiz.
* Katta kodlar o‘rniga bir necha qator bilan ishni boshlaymiz.

**Oddiy hayotiy misol:**
Express — bu “tayyor oshxona”. O‘zingiz ham oshxona qurishingiz mumkin, lekin Express borida hammasi tayyor: gaz plitasi, idish-tovoq, pichoq. Siz faqat taom tayyorlaysiz.

---

### Express o‘rnatish

1. Papka ochamiz: `backend-lessons`
2. Terminalda shu papkaga kiring.
3. Node loyihasini boshlang:

```bash
npm init -y
```

4. Expressni o‘rnating:

```bash
npm install express
```

✅ Endi Express loyihangizga qo‘shildi.

---

### Birinchi Express server

`server.js` faylini yarating va yozing:

```javascript
import express from 'express';    // Express kutubxonasini chaqiryapmiz

const app = express();            // Server dasturini yaratdik
const PORT = 3000;                // Server ishlaydigan port

// Asosiy manzil — bu / (ildiz)
app.get('/', (req, res) => {
  res.send('Salom! Bu mening birinchi backend serverim 🚀');
});

// Serverni ishga tushiramiz
app.listen(PORT, () => {
  console.log(`Server ishga tushdi: http://localhost:${PORT}`);
});
```

Keyin terminalda ishga tushiring:

```bash
node server.js
```

Brauzerga `http://localhost:3000` kirib ko‘ring.
Sizning yozgan matningiz ekranga chiqadi.

---

### **GET** tushunchasi

Biz `app.get()` ishlatdik. **GET** — bu **so‘rov turi**.

* Internetda foydalanuvchi serverdan ma’lumot olish uchun **GET** so‘rovi yuboradi.
* Brauzerda har safar manzil kiritganingizda aslida GET yuboriladi.

Misol:

* Siz `https://google.com` deb yozasiz → brauzer Google serveriga **GET** so‘rovi yuboradi → server sahifa qaytaradi.

Express’da `app.get('/yo‘l', ...)` — “kimdir shu yo‘lga GET so‘rovi yuborsa, nima javob beramiz?” degani.

---

### Turli yo‘llar (Routes) yaratish

“Route” — bu serverdagi manzil yoki sahifa.

```javascript
app.get('/about', (req, res) => {
  res.send('Bu — sayt haqida ma’lumot.');
});

app.get('/contact', (req, res) => {
  res.send('Biz bilan bog‘lanish: contact@example.com');
});
```

* `http://localhost:3000/about` ga kirsangiz “Bu — sayt haqida ma’lumot.”
* `http://localhost:3000/contact` ga kirsangiz “Biz bilan bog‘lanish: …”

---

### JSON qaytarish

Backendning eng muhim vazifasi — **JSON yuborish**. Bu ma’lumotni tartibli ko‘rsatadi.

```javascript
app.get('/user', (req, res) => {
  res.json({
    ism: 'Ali',
    yosh: 14,
    hobby: 'futbol'
  });
});
```

Brauzerga `http://localhost:3000/user` yozing.
Siz JSON ma’lumotni ko‘rasiz — bu serverdan kelgan real javob.

---

### Query va Params tushunchasi

#### Query nima?

* Query — bu manzilga `?` dan keyin yoziladigan ma’lumot.
* Masalan: `http://localhost:3000/salom?ism=Ali`

  * `ism=Ali` — bu query (so‘rov parametri).

Kodni yozamiz:

```javascript
app.get('/salom', (req, res) => {
  const ism = req.query.ism;    // ?ism=Ali orqali kelgan qiymat
  res.send(`Salom, ${ism || 'mehmon'}!`);
});
```

* Agar `?ism=Ali` qo‘ysangiz → “Salom, Ali!”
* Agar hech narsa yozmasangiz → “Salom, mehmon!”

#### Params nima?

* Params — manzilning bir qismi sifatida yoziladigan ma’lumot.
* Misol: `http://localhost:3000/user/15` → bu yerda **15** — params.

```javascript
app.get('/user/:id', (req, res) => {
  const id = req.params.id;
  res.send(`Siz so‘ragan foydalanuvchi ID: ${id}`);
});
```

* `user/15` → “Siz so‘ragan foydalanuvchi ID: 15”
* `user/42` → “Siz so‘ragan foydalanuvchi ID: 42”

✅ Farq:

* Query `?kalit=qiymat` (manzil oxirida, `?` bilan).
* Params `/qiymat` (to‘g‘ridan-to‘g‘ri yo‘l ichida).

---

### Avtomatik restart — Nodemon

Serverni qayta ishga tushirishga hojat qolmasin, `nodemon` ishlatamiz:

```bash
npm install --save-dev nodemon
```

`package.json` da quyidagicha yozing:

```json
"scripts": {
  "start": "nodemon server.js"
}
```

Endi `npm start` deb yozsangiz, kodni saqlaganda server avtomatik yangilanadi.

---

### Amaliy mashqlar

1. `/books` yo‘lini yarating va kitoblar ro‘yxatini JSON qilib qaytaring:

```json
[
  { "nomi": "Alpomish", "muallif": "Xalq og'zaki ijodi" },
  { "nomi": "Ufq", "muallif": "Odil Yoqubov" }
]
```

2. `/salom` yo‘lida `ism` query orqali foydalanuvchini kutib oling:
   `/salom?ism=Dilshod` → “Salom, Dilshod!”

3. `/time` yo‘lida joriy vaqtni qaytaring:

```javascript
app.get('/time', (req, res) => {
  const hozir = new Date();
  res.send(`Hozirgi vaqt: ${hozir.toLocaleTimeString()}`);
});
```

---

### Asosiy tushunchalar

* **Express** — serverni tez va oson yaratishga yordam beradi.
* **GET** — ma’lumot so‘rash uchun ishlatiladi.
* **Route (yo‘l)** — serverdagi manzillar.
* **Query** — manzilga `?` bilan qo‘shiladigan ma’lumot.
* **Params** — yo‘lning bir qismi sifatida keladigan qiymat.
* **JSON** — backenddan ma’lumot yuborishning asosiy formati.

---

</details>

<hr>

<details>
    <summary>Express bilan birinchi server (takror va mustahkamlash)</summary>
## 🗓️ 2-hafta — 1-dars

### 🏷️ Mavzu: **Express bilan birinchi server (takror va mustahkamlash)**

---

### Express nima?

Oldingi darsda biz Express bilan tanishdik. Bugun esa amaliy jihatdan yana bir bor ko‘rib chiqamiz va butun sinf birga server ishga tushirib ko‘radi.

* **Express** — Node.js uchun yozilgan juda mashhur kutubxona.
* Server yaratishni osonlashtiradi va kodni tartibli qiladi.
* Biz undan foydalanganimizda turli manzillarga (routes) juda tez javob bera olamiz.

---

### Express’ni o‘rnatish

1. Papka yarating yoki oldingi loyihadan foydalaning (masalan: `backend-lessons`).
2. Terminalda shu papkaga kiring va quyidagilarni yozing:

```bash
npm init -y
```

Bu loyiha uchun kerakli `package.json` faylini yaratadi.

3. Express’ni o‘rnating:

```bash
npm install express
```

✅ Shu bilan loyihaga Express qo‘shildi.

---

### Birinchi server kodi

`server.js` faylini yarating va quyidagicha yozing:

```javascript
import express from 'express';       // Express kutubxonasini chaqiramiz (ES Module syntax)
const app = express();               // Server yaratamiz
const PORT = 3000;                    // Port — server tinglaydigan eshik raqami

// Asosiy sahifa uchun GET so'roviga javob
app.get('/', (req, res) => {
  res.send('Salom! Mening birinchi backend serverim 🚀');
});

// Serverni ishga tushiramiz
app.listen(PORT, () => {
  console.log(`Server ishga tushdi: http://localhost:${PORT}`);
});
```

**Izoh:**

* `import express from 'express'` — loyihaga Express kutubxonasini chaqirish (ES Module syntax).
* `app.get('/', ...)` — `GET` so‘roviga javob berish (asosiy manzil `/`).
* `res.send()` — foydalanuvchiga matn yuboradi.
* `app.listen(PORT, ...)` — serverni ishga tushiradi va ko‘rsatilgan portni tinglaydi.

---

### Serverni ishga tushirish

Terminalda yozing:

```bash
node server.js
```

Agar hammasi to‘g‘ri bo‘lsa, quyidagiga o‘xshash yozuv chiqadi:

```
Server ishga tushdi: http://localhost:3000
```

Endi brauzerga `http://localhost:3000` yozing — sahifada `Salom! Mening birinchi backend serverim 🚀` degan yozuv chiqadi.

✅ Tabriklaymiz! Sizning shaxsiy backend serveringiz ishlayapti.

---

### Foydali mashqlar

1. `about` degan yangi yo‘l yarating:

```javascript
app.get('/about', (req, res) => {
  res.send('Bu mening sayt haqidagi sahifa.');
});
```

Brauzerda: `http://localhost:3000/about`

2. `contact` degan yo‘l yarating:

```javascript
app.get('/contact', (req, res) => {
  res.send('Biz bilan bog‘lanish: contact@example.com');
});
```

Brauzerda: `http://localhost:3000/contact`

3. `books` degan yo‘l yarating va JSON qaytaring:

```javascript
app.get('/books', (req, res) => {
  res.json([
    { nomi: 'Alpomish', muallif: 'Xalq og‘zaki ijodi' },
    { nomi: 'Ufq', muallif: 'Odil Yoqubov' }
  ]);
});
```

Brauzerda: `http://localhost:3000/books`

---

### Oddiy tushunchalarni mustahkamlash

* **GET** — serverdan ma’lumot so‘rash turi.
* **Route (yo‘l)** — manzil, masalan `/`, `/about`, `/books`.
* **res.send()** — matn yoki HTML qaytaradi.
* **res.json()** — JSON ma’lumot qaytaradi.
* **Port** — server ishlaydigan eshik raqami (odatda 3000 yoki 5000).

---

</details>

<hr>


<details>
    <summary>Routes va JSON javobi</summary>
## 🗓️ 2-hafta — 2-dars

### 🏷️ Mavzu: **Routes va JSON javobi**

---

### Route nima?

**Route** (yo‘l) — bu serverdagi manzil.
Har safar foydalanuvchi brauzerda biror manzilga kirganda, server shu manzilga qarab javob beradi.

Misol:

* `http://localhost:3000/` → asosiy sahifa.
* `http://localhost:3000/about` → haqida sahifa.
* `http://localhost:3000/hello` → salomlashish sahifasi.

Biz har bir manzil uchun alohida **route** yozamiz.

---

### Matn yuborish (takrorlash)

`server.js` faylida:

```javascript
import express from 'express';
const app = express();
const PORT = 3000;

app.get('/', (req, res) => {
  res.send('Salom! Bu asosiy sahifa.');
});

app.listen(PORT, () => {
  console.log(`Server http://localhost:${PORT} da ishlayapti`);
});
```

✅ `res.send()` — foydalanuvchiga oddiy matn yuboradi.

---

### JSON yuborish

Backendning eng katta kuchi — **JSON** ma’lumot yuborish.
JSON — bu ma’lumotni tartibli qilib ko‘rsatish usuli.

```javascript
app.get('/user', (req, res) => {
  res.json({
    ism: 'Ali',
    yosh: 14,
    hobby: 'futbol'
  });
});
```

Brauzerda `http://localhost:3000/user` ga kirsangiz:

```json
{
  "ism": "Ali",
  "yosh": 14,
  "hobby": "futbol"
}
```

✅ `res.json()` — foydalanuvchiga JSON formatida ma’lumot yuboradi.

---

### Bir nechta routes yaratish

Serverda turli manzillar uchun turli ma’lumotlar qaytarishimiz mumkin.

```javascript
app.get('/about', (req, res) => {
  res.json({
    loyiha: 'Backend asoslari',
    muallif: 'Sizning ismingiz',
    til: 'JavaScript (Node.js + Express)'
  });
});

app.get('/hello', (req, res) => {
  res.json({
    salom: 'Salom, dunyo!',
    vaqt: new Date().toLocaleTimeString()
  });
});
```

* `http://localhost:3000/about` → loyiha haqida JSON ko‘rsatadi.
* `http://localhost:3000/hello` → salomlashadi va hozirgi vaqtni ko‘rsatadi.

---

### Amaliy faoliyat

🛠 **Mashq:** “O‘zim haqimda API”

1. `info` degan yangi route yarating.
2. `ism`, `yosh`, `hobby`, `maktab` kabi maydonlarni qo‘shing.
3. JSON ko‘rinishida qaytaring.

Masalan:

```javascript
app.get('/info', (req, res) => {
  res.json({
    ism: 'Dilshod',
    yosh: 14,
    hobby: 'dasturlash',
    maktab: '12-maktab'
  });
});
```

Brauzerda:
`http://localhost:3000/info` ga kirsangiz, o‘zingiz haqingizdagi ma’lumot JSON bo‘lib chiqadi.

---

### Yakuniy tushunchalar

* **Route (yo‘l)** — serverdagi har bir manzil (masalan `/about` yoki `/hello`).
* **`res.send()`** — oddiy matn yoki HTML yuboradi.
* **`res.json()`** — JSON formatida ma’lumot yuboradi.
* Har bir route foydalanuvchiga boshqa javob yuborishi mumkin.

---

</details>

<hr>


<details>
    <summary>Nodemon va Thunder Client bilan qulay ishlash</summary>
## 🗓️ 2-hafta — 3-dars

### 🏷️ Mavzu: **Nodemon va Thunder Client bilan qulay ishlash**

---

### Nodemon nima?

Biz hozircha server kodini o‘zgartirgandan so‘ng uni **CTRL + C** bilan to‘xtatib, yana `node server.js` deb ishga tushirishga majbur bo‘lyapmiz. Bu juda noqulay.

**Nodemon** — serverni avtomatik qayta ishga tushiradigan dastur. Kodni saqlash bilan birga server o‘zi yangilanadi. Juda tez ishlash imkonini beradi.

---

### Nodemon o‘rnatish

Terminalda yozing:

```bash
npm install --save-dev nodemon
```

> `--save-dev` — bu paketni faqat dastur yozish jarayonida kerak bo‘ladi, keyinchalik server ishlashi uchun majburiy emas.

`package.json` faylida endi “devDependencies” degan joyga nodemon qo‘shiladi.

---

### package.json dagi script sozlash

`package.json` faylini ochib, `"scripts"` bo‘limini toping va quyidagicha yozing:

```json
"scripts": {
  "start": "nodemon server.js"
}
```

Endi serverni ishga tushirish uchun terminalda faqat buni yozamiz:

```bash
npm start
```

✅ Endi kodni saqlash bilan birga server avtomatik qayta yuklanadi.

---

### Thunder Client nima?

Backend yozayotganda brauzer faqat **GET** so‘rovlarini yubora oladi. Ammo biz tez orada **POST, PUT, DELETE** kabi boshqa so‘rov turlarini ham ishlatamiz. Shuning uchun test qilish uchun maxsus vosita kerak.

**Thunder Client** — bu VS Code ichidagi qulay plagin. U orqali:

* GET, POST, PUT, DELETE so‘rovlari yuborish mumkin.
* JSON ma’lumot jo‘natish mumkin.
* Javobni chiroyli ko‘rish mumkin.

---

### Thunder Client o‘rnatish

1. VS Code’ni oching.
2. Chap tomondagi Extensions (kattalashtirilgan “pazl” belgisi) ga kiring.
3. Qidiruvdan **Thunder Client** yozing va o‘rnating.

VS Code’da endi chap tomonda chaqmoqcha belgili Thunder Client tugmasi paydo bo‘ladi.

---

### Thunder Client bilan sinash

1. Thunder Client oynasini oching (chap tomonda chaqmoq belgisi).
2. “New Request” tugmasini bosing.
3. Method: GET
4. URL: `http://localhost:3000`
5. Send tugmasini bosing → serverdan javob ko‘rasiz.

---

### Mashq: `/greet` route yaratish

`server.js` faylida yangi yo‘l qo‘shamiz:

```javascript
app.get('/greet', (req, res) => {
  const name = req.query.name;   // ?name=Ali orqali yuborilgan ismni olamiz
  res.send(`Salom, ${name || 'mehmon'}!`);
});
```

> Bu degani: agar foydalanuvchi manzilga `?name=Ali` qo‘shsa, server “Salom, Ali!” deb javob beradi. Agar hech narsa yubormasa — “Salom, mehmon!”.

---

### `/greet` ni Thunder Client’da tekshirish

1. Thunder Client’ni oching.
2. New Request → Method: GET
3. URL:

   * `http://localhost:3000/greet?name=Ali`
   * `http://localhost:3000/greet?name=Aziza`
   * `http://localhost:3000/greet`
4. Har birini yuboring va javobning qanday o‘zgarganini ko‘ring.

---

### Foydali tushunchalar

* **Nodemon** — kodni saqlaganda server avtomatik qayta ishga tushadi.
* **Thunder Client** — turli so‘rovlarni (GET, POST, DELETE va hokazo) qulay test qilishga yordam beradi.
* **Query** — URL’ning oxiridagi `?kalit=qiymat` ko‘rinishidagi qism.

---

</details>

<hr>


<details>
    <summary>Query va Params bilan ishlash (Requests & Data)</summary>
## 🗓️ 3-hafta — 1-dars

### 🏷️ Mavzu: **Query va Params bilan ishlash (Requests & Data)**

---

### So‘rov (Request) nima?

Server bilan ishlashni boshlaganimizda, foydalanuvchi (yoki brauzer) serverga **so‘rov** yuboradi. Bu xuddi biror odamga savol berishdek: “Menga ma’lumot yubor”.

So‘rovda ikki xil ma’lumot kelishi mumkin:

1. **Query (so‘rov parametrlari)** — URL oxirida `?` belgisidan keyin keladi.
2. **Params (yo‘l parametrlari)** — URL yo‘lining bir qismi sifatida yoziladi.

Bugun shu ikkisini farqlab, real misollarda ishlatib ko‘ramiz.

---

### Query nima?

**Query** — foydalanuvchi URL oxiriga qo‘shimcha ma’lumot yozib yuboradi.

Misol:
`http://localhost:3000/search?kitob=Alpomish`
Bu yerda:

* `?` — query qismi boshlanishi.
* `kitob` — kalit.
* `Alpomish` — qiymat.

Ko‘pincha query foydalanuvchi nimani izlayotgani, qaysi ma’lumotni olishni xohlayotganini bildiradi.

#### Express’da Query olish

```javascript
app.get('/search', (req, res) => {
  const kitob = req.query.kitob; // foydalanuvchi yuborgan 'kitob'
  res.send(`Siz izlayotgan kitob: ${kitob}`);
});
```

Endi brauzerda sinab ko‘ring:

* `http://localhost:3000/search?kitob=Alpomish`
  → “Siz izlayotgan kitob: Alpomish”
* `http://localhost:3000/search?kitob=Ufq`
  → “Siz izlayotgan kitob: Ufq”

Agar foydalanuvchi query yozmasa, qiymat `undefined` bo‘ladi. Uni oldini olish uchun zaxira qiymat berish mumkin:

```javascript
app.get('/search', (req, res) => {
  const kitob = req.query.kitob || 'hech narsa yuborilmadi';
  res.send(`Siz izlayotgan kitob: ${kitob}`);
});
```

---

### Params nima?

**Params** — bu URL yo‘lining bir qismi sifatida yoziladigan ma’lumot.
Ko‘pincha aniq bitta elementni chaqirish uchun ishlatiladi.

Misol:
`http://localhost:3000/books/10`
Bu yerda:

* `books` — yo‘l nomi.
* `10` — params (kitob ID’si).

#### Express’da Params olish

```javascript
app.get('/books/:id', (req, res) => {
  const id = req.params.id;  // foydalanuvchi yuborgan :id qiymati
  res.send(`Siz so‘ragan kitob ID: ${id}`);
});
```

Sinash:

* `http://localhost:3000/books/15`
  → “Siz so‘ragan kitob ID: 15”
* `http://localhost:3000/books/42`
  → “Siz so‘ragan kitob ID: 42”

Bir nechta params bo‘lishi ham mumkin:

```javascript
app.get('/users/:userId/books/:bookId', (req, res) => {
  const user = req.params.userId;
  const book = req.params.bookId;
  res.send(`Foydalanuvchi ID: ${user}, Kitob ID: ${book}`);
});
```

URL: `http://localhost:3000/users/7/books/99`
Natija: “Foydalanuvchi ID: 7, Kitob ID: 99”

---

### Query va Params farqi

| Taqqoslash        | Query (req.query)              | Params (req.params)                      |
| ----------------- | ------------------------------ | ---------------------------------------- |
| Qayerda yoziladi? | URL oxirida `?kalit=qiymat`    | URL yo‘lining bir qismi sifatida         |
| Odatda qachon?    | Filtrlash, qidirish, opsiyalar | Maxsus elementni chaqirish (ID yoki nom) |
| Misol             | `/search?kitob=Alpomish`       | `/books/10`                              |
| Ko‘rinishi        | `{ kitob: "Alpomish" }`        | `{ id: "10" }`                           |

✅ Oddiy qoida: **Query** — qo‘shimcha, ixtiyoriy ma’lumot. **Params** — majburiy va yo‘lning o‘zi.

---

### Mashq: `/hello/:name` route

Endi bolalar uchun sodda mashq qilamiz — foydalanuvchi URL’da o‘z ismini yozadi, server uni salomlaydi.

```javascript
app.get('/hello/:name', (req, res) => {
  const ism = req.params.name;
  res.send(`Hello, ${ism}!`);
});
```

Sinab ko‘ramiz:

* `http://localhost:3000/hello/Ali` → “Hello, Ali!”
* `http://localhost:3000/hello/Lola` → “Hello, Lola!”

---

### Mashq: `/hello` query bilan

Agar query ishlatmoqchi bo‘lsak:

```javascript
app.get('/hello', (req, res) => {
  const ism = req.query.name || 'mehmon';
  res.send(`Hello, ${ism}!`);
});
```

Sinash:

* `http://localhost:3000/hello?name=Ali` → “Hello, Ali!”
* `http://localhost:3000/hello` → “Hello, mehmon!”

---

### Qo‘shimcha misollar

**1. Foydalanuvchini params orqali tanlash**

```javascript
app.get('/user/:id', (req, res) => {
  const id = req.params.id;
  res.json({
    id: id,
    ism: 'Foydalanuvchi ' + id,
    status: 'active'
  });
});
```

`http://localhost:3000/user/25`
→ `{ "id": "25", "ism": "Foydalanuvchi 25", "status": "active" }`

**2. Qidiruv so‘zi bilan JSON qaytarish**

```javascript
app.get('/search', (req, res) => {
  const so‘z = req.query.q || 'hech narsa yozilmadi';
  res.json({
    qidiruv: so‘z,
    natija_soni: 0
  });
});
```

`http://localhost:3000/search?q=telefon` → `{ "qidiruv": "telefon", "natija_soni": 0 }`

---

### Xulosa

* `req.query` — URL’da `?kalit=qiymat` orqali kelgan ma’lumotni olish.
* `req.params` — URL’ning o‘zida yozilgan qiymatni olish (`/user/5`).
* Params aniq va majburiy, query qo‘shimcha va ixtiyoriy.
* Har ikkisini birgalikda ishlatish mumkin.

---

</details>

<hr>


<details>
    <summary>POST so‘rovi va Body ma’lumotlari bilan ishlash</summary>

## 🗓️ 3-hafta — 2-dars

### 🏷️ Mavzu: **POST so‘rovi va Body ma’lumotlari bilan ishlash**

---

### POST nima?

Oldingi darsda biz **GET** so‘rovlarini ko‘rib chiqdik — foydalanuvchi serverdan ma’lumot so‘raydi.
**POST** esa buning aksi: foydalanuvchi serverga yangi ma’lumot yuboradi.

* **GET** — ma’lumot olish uchun.
* **POST** — ma’lumot yuborish uchun.

Misollar:

* Telegramda xabar yuborish → POST
* Instagramda rasm yuklash → POST
* Onlayn do‘konda yangi buyurtma qilish → POST

---

### GET va POST farqi

|                    | GET                                     | POST                                             |
| ------------------ | --------------------------------------- | ------------------------------------------------ |
| Qayerda ko‘rinadi  | Ma’lumot URL’da ko‘rinadi (`?name=Ali`) | Ma’lumot yashirin (URL’da ko‘rinmaydi)           |
| Qachon ishlatiladi | O‘qish, qidirish, ko‘rish               | Yuborish, saqlash, ro‘yxatdan o‘tish             |
| Ma’lumot hajmi     | Kichik bo‘lishi kerak                   | Ko‘p va katta bo‘lishi mumkin (matn, rasm, fayl) |

---

### POST bilan JSON yuborish

Foydalanuvchi serverga ma’lumot yuborayotganida uni **body** ichiga joylaydi.
**Body** — bu so‘rovning ichidagi ma’lumotlar bo‘limi.

Bizning server POST ma’lumotni tushunishi uchun Express’da maxsus sozlash kerak:

```javascript
app.use(express.json());
```

Bu qator serverga kelayotgan JSON ma’lumotni o‘qib olish imkonini beradi.

---

### Amaliy misol: `/feedback` API

1. `server.js` faylida quyidagilarni yozamiz:

```javascript
import express from 'express';
const app = express();
const PORT = 3000;

// JSON body ma’lumotni o‘qish uchun sozlash
app.use(express.json());

app.post('/feedback', (req, res) => {
  const data = req.body; // foydalanuvchi yuborgan JSON ma’lumot
  console.log(data);     // Terminalga ko‘ramiz

  res.json({
    status: 'success',
    message: `Xabaringiz qabul qilindi: "${data.message}"`
  });
});

app.listen(PORT, () => {
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
app.post('/feedback', (req, res) => {
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

* **POST** — serverga yangi ma’lumot yuborish uchun ishlatiladi.
* **Body** — POST so‘rovida keladigan ma’lumotlar bo‘limi.
* **`express.json()`** — serverga JSON formatdagi ma’lumotni tushuntiradi.
* **`req.body`** — foydalanuvchi yuborgan JSON’ni olish uchun ishlatiladi.

---
</details>

<hr>


<details>
    <summary>Oddiy Todos API — xotirada ma’lumot saqlash (in-memory)</summary>
## 🗓️ 3-hafta — 3-dars

### 🏷️ Mavzu: **Oddiy Todos API — xotirada ma’lumot saqlash (in-memory)**

---

### Maqsad

Oldingi darsda biz foydalanuvchi yuborgan ma’lumotni POST orqali qabul qila oldik.
Bugun esa **haqiqiy kichkina API** yasaymiz. Bu API foydalanuvchi yuborgan vazifalarni (todo’larni) xotirada saqlaydi va GET orqali ularni ko‘rsatadi.

> ⚡️ Bu darsdan keyin siz shunday serverga ega bo‘lasiz:
>
> * `POST /todos` — yangi vazifa qo‘shish
> * `GET /todos` — barcha vazifalarni ko‘rish

---

### Xotira (Memory) nima?

Hozircha biz ma’lumotni fayl yoki bazaga yozmaymiz.
**In-memory** degani — ma’lumot server ishayotgan vaqtida kompyuter xotirasida saqlanadi.
Server o‘chsa yoki qayta ishga tushsa, ma’lumot yo‘qoladi.

Bu o‘quv bosqichida oddiy va tushunarli.

---

### Boshlang‘ich kod

`server.js` faylimizni yangilaymiz:

```javascript
import express from 'express';
const app = express();
const PORT = 3000;

// JSON body o‘qish
app.use(express.json());

// TODO larni saqlash uchun bo‘sh array
let todos = [];

// Barcha TODO larni ko‘rsatish
app.get('/todos', (req, res) => {
  res.json(todos);
});

// Yangi TODO qo‘shish
app.post('/todos', (req, res) => {
  const { title } = req.body;

  if (!title) {
    return res.status(400).json({
      status: 'error',
      message: 'Todo sarlavhasi kerak!'
    });
  }

  const newTodo = {
    id: todos.length + 1,
    title: title,
    completed: false
  };

  todos.push(newTodo);

  res.status(201).json({
    status: 'success',
    todo: newTodo
  });
});

app.listen(PORT, () => {
  console.log(`Server ishga tushdi: http://localhost:${PORT}`);
});
```

---

### Kodni tushuntirish

* `let todos = []` — vazifalar ro‘yxati saqlanadigan bo‘sh array.
* `app.get('/todos')` — barcha vazifalarni JSON qilib qaytaradi.
* `app.post('/todos')` — yangi vazifa qabul qiladi va ro‘yxatga qo‘shadi.
* `id` — har bir vazifaga tartib raqami beramiz (length + 1).
* `completed` — vazifa bajarilgan yoki yo‘qligini bilish uchun.

---

### Thunder Client bilan sinash

#### 1. Yangi vazifa qo‘shish

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

#### 2. Yana bir vazifa qo‘shamiz

```json
{
  "title": "Kitob o‘qish"
}
```

**Natija:**

```json
{
  "status": "success",
  "todo": {
    "id": 2,
    "title": "Kitob o‘qish",
    "completed": false
  }
}
```

#### 3. Barcha vazifalarni ko‘rish

* Method: GET
* URL: `http://localhost:3000/todos`

**Natija:**

```json
[
  { "id": 1, "title": "Uy vazifasini qilish", "completed": false },
  { "id": 2, "title": "Kitob o‘qish", "completed": false }
]
```

---

### Kengaytirish (qo‘shimcha)

Biz bajarilgan vazifalarni ko‘rsatish uchun `completed` qiymatini o‘zgartirish imkoniyatini qo‘shamiz:

```javascript
app.patch('/todos/:id', (req, res) => {
  const { id } = req.params;
  const todo = todos.find(t => t.id === parseInt(id));

  if (!todo) {
    return res.status(404).json({ message: 'Todo topilmadi' });
  }

  todo.completed = !todo.completed;
  res.json({ status: 'success', todo });
});
```

* URL: `http://localhost:3000/todos/1`
* Method: PATCH

Har safar chaqirsak `completed` qiymati o‘zgaradi.

---

### Qo‘shimcha mashqlar

1. `/clear` degan route yarating, u barcha vazifalarni o‘chirib yuborsin.
2. `/count` degan route yarating, u nechta vazifa borligini qaytarsin.

Misol:

```javascript
app.get('/count', (req, res) => {
  res.json({ total: todos.length });
});
```

---

### Asosiy tushunchalar

* **In-memory** — ma’lumot server xotirasida saqlanadi (o‘chsa yo‘qoladi).
* **GET** — saqlangan ma’lumotni olish.
* **POST** — yangi ma’lumot qo‘shish.
* **Array** — bir nechta obyektlarni tartibli saqlash uchun.
* **Status kodlar** — 200 (OK), 201 (yaratildi), 400 (xato), 404 (topilmadi).

---

</details>

<hr>

<details>
    <summary>Ma’lumotni xotirada emas, faylda saqlash (Database va Memory tushunchasi)</summary>
## 🗓️ 4-hafta — 1-dars

### 🏷️ Mavzu: **Ma’lumotni xotirada emas, faylda saqlash (Database va Memory tushunchasi)**

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

* **Memory** — vaqtinchalik xotira, server to‘xtasa ma’lumot yo‘qoladi.
* **Database** — ma’lumotni doimiy saqlash joyi.
* **JSON fayl** — oddiy ko‘rinishdagi kichik database.
* **lowdb** — JSON faylni database sifatida ishlatish uchun juda oddiy va qulay kutubxona.

---
</details>

<hr>

<details>
    <summary>lowdb bilan oddiy ma’lumotlar bazasini sozlash va Todos API’ni saqlash</summary>
## 🗓️ 4-hafta — 2-dars

### 🏷️ Mavzu: **lowdb bilan oddiy ma’lumotlar bazasini sozlash va Todos API’ni saqlash**

---

### lowdb bilan ishlashni boshlash

Oldingi darsda biz **memory** va **database** farqini o‘rgandik va lowdb kutubxonasini ko‘rdik. Bugun esa bizning **Todos API**’mizni to‘liq **db.json** fayliga ulaymiz. Endi ma’lumotlar server o‘chsa ham saqlanib qoladi.

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
app.get('/todos', (req, res) => {
  res.json(db.data.todos)
})
```

Bu orqali biz fayldagi barcha todos ro‘yxatini qaytarib beramiz.

---

### 5️⃣ POST /todos — yangi todo qo‘shish

```javascript
app.post('/todos', async (req, res) => {
  const { title } = req.body

  if (!title) {
    return res.status(400).json({ status: 'error', message: 'Todo nomi kerak!' })
  }

  const newTodo = {
    id: db.data.todos.length + 1,
    title,
    completed: false
  }

  db.data.todos.push(newTodo)  // ro‘yxatga qo‘shamiz
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
app.patch('/todos/:id', async (req, res) => {
  const { id } = req.params
  const todo = db.data.todos.find(t => t.id === parseInt(id))

  if (!todo) return res.status(404).json({ message: 'Todo topilmadi' })

  todo.completed = !todo.completed
  await db.write()

  res.json({ status: 'success', todo })
})
```

---

### Asosiy tushunchalar

* **lowdb** — JSON faylni oddiy database sifatida ishlatadi.
* **await db.read()** — fayldan ma’lumotni o‘qiydi.
* **await db.write()** — ma’lumotni faylga yozadi.
* **GET /todos** — ma’lumotlarni olish.
* **POST /todos** — yangi ma’lumot qo‘shish va saqlash.

---
</details>

<hr>


<details>
    <summary>CRUD to‘liq: DELETE va PUT/PATCH bilan yakunlash (lowdb)</summary>
## 🗓️ 4-hafta — 3-dars

### 🏷️ Mavzu: **CRUD to‘liq: DELETE va PUT/PATCH bilan yakunlash (lowdb)**

---

Bu darsda “Todos API”ni to‘liq **CRUD** (Create, Read, Update, Delete) holatiga keltiramiz:

* **DELETE `/todos/:id`** — todo’ni o‘chirish
* **PUT/PATCH `/todos/:id`** — todo’ni yangilash (masalan, `completed`ni belgilash)

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

// READ: Barcha todo’lar
app.get('/todos', (req, res) => {
  res.json(db.data.todos)
})

// CREATE: Yangi todo
app.post('/todos', async (req, res) => {
  const { title } = req.body
  if (!title) {
    return res.status(400).json({ status: 'error', message: 'Todo nomi kerak!' })
  }

  const newTodo = {
    id: db.data.todos.length ? Math.max(...db.data.todos.map(t => t.id)) + 1 : 1,
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
// DELETE: Todo o‘chirish
app.delete('/todos/:id', async (req, res) => {
  const id = Number(req.params.id)

  // noto‘g‘ri id yuborilsa
  if (Number.isNaN(id)) {
    return res.status(400).json({ status: 'error', message: 'Noto‘g‘ri ID' })
  }

  const index = db.data.todos.findIndex(t => t.id === id)

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
app.patch('/todos/:id', async (req, res) => {
  const id = Number(req.params.id)
  if (Number.isNaN(id)) {
    return res.status(400).json({ status: 'error', message: 'Noto‘g‘ri ID' })
  }

  const todo = db.data.todos.find(t => t.id === id)
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
// PATCH: completed ni aniq qiymatga o‘rnatish (body: { completed: true/false })
app.patch('/todos/:id/complete', async (req, res) => {
  const id = Number(req.params.id)
  const { completed } = req.body

  if (Number.isNaN(id)) {
    return res.status(400).json({ status: 'error', message: 'Noto‘g‘ri ID' })
  }
  if (typeof completed !== 'boolean') {
    return res.status(400).json({ status: 'error', message: 'completed true/false bo‘lishi kerak' })
  }

  const todo = db.data.todos.find(t => t.id === id)
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
// PUT: to‘liq yangilash (title va completed talab qilinadi)
app.put('/todos/:id', async (req, res) => {
  const id = Number(req.params.id)
  const { title, completed } = req.body

  if (Number.isNaN(id)) {
    return res.status(400).json({ status: 'error', message: 'Noto‘g‘ri ID' })
  }
  if (typeof title !== 'string' || !title.trim()) {
    return res.status(400).json({ status: 'error', message: 'title talab qilinadi' })
  }
  if (typeof completed !== 'boolean') {
    return res.status(400).json({ status: 'error', message: 'completed true/false bo‘lishi kerak' })
  }

  const index = db.data.todos.findIndex(t => t.id === id)
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
app.listen(PORT, () => {
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

Endi sizning “Todos API”ngiz to‘liq **CRUD** funksiyalariga ega:

* **POST** `/todos` — yaratish
* **GET** `/todos` — o‘qish
* **PATCH/PUT** `/todos/:id` — yangilash
* **DELETE** `/todos/:id` — o‘chirish

</details>

<hr>