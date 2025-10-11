# Backend Asoslari - Uy Ishlari

> **Ko'rsatma:** Har bir dars uchun uy ishi berilgan. Topshiriqlarni tartib bilan bajaring va natijalarni saqlang.

---

## 1-hafta — 1-dars: Internet va Backend asoslari

### 📝 Uy ishi

**Topshiriq 1: JSON fayl yaratish**

1. Kompyuteringizda `mening_profilim.json` nomli fayl yarating
2. Quyidagi ma'lumotlarni JSON formatda yozing:
   - Ismingiz
   - Yoshingiz
   - Maktabingiz
   - 3 ta sevimli mashg'ulotingiz (array ko'rinishida)
   - Sevimli rangingiz

**Kutilgan natija misoli:**
```json
{
  "ism": "...",
  "yosh": 14,
  "maktab": "...",
  "qiziqishlar": ["...", "...", "..."],
  "sevimli_rang": "..."
}
```

**Topshiriq 2: API'larni o'rganish**

1. Brauzerda `https://jsonplaceholder.typicode.com/users` manzilini oching
2. Kelgan ma'lumotlarda nimalar borligini yozib oling (kamida 5 ta maydon)
3. Developer Tools (F12) ni ochib, Network bo'limida nima ko'rishingizni tekshiring

**Javob qog'ozga yozing:**
- JSON da qanday maydonlar bor?
- Nechta foydalanuvchi bor?
- Status kod nima?

**Topshiriq 3: HTTP metodlarini eslash**

Quyidagi real hayot harakatlarini to'g'ri HTTP metodi bilan moslashtiring va daftaringizga yozing:

- Instagram'ga yangi rasm yuklash: ___?___
- YouTube'da video qidirish: ___?___
- Telegram'da xabarni o'chirish: ___?___
- Profildagi telefon raqamini o'zgartirish: ___?___

---

## 1-hafta — 2-dars: Node.js o'rnatish

### 📝 Uy ishi

**Topshiriq 1: Node.js versiyasini tekshirish**

1. Terminalda `node -v` va `npm -v` buyruqlarini bajaring
2. Chiqgan versiyalarni daftaringizga yozing
3. Screenshot oling va saqlang

**Topshiriq 2: Oddiy Node.js dasturlari**

`uy-ishi` nomli yangi papka yarating va quyidagi fayllarni yarating:

**a) `salom.js` - Oddiy console.log**
```javascript
console.log("Salom, mening ismim [sizning ismingiz]");
console.log("Men backend dasturchi bo'laman!");
```

**b) `hisob.js` - Kalkulyator**

Quyidagi hisob-kitoblarni bajaring va natijalarini console.log qiling:
- 15 + 27
- 100 - 43
- 12 * 8
- 144 / 12
- 2025 yildan tug'ilgan yilingizni ayirib, yoshingizni hisoblang

**c) `mevalar.js` - Array bilan ishlash**

```javascript
const mevalar = ["Olma", "Banan", "Uzum", "Anor", "Shaftoli"];

console.log("Mevalar soni:", mevalar.length);
console.log("Birinchi meva:", mevalar[0]);
console.log("Oxirgi meva:", mevalar[mevalar.length - 1]);
console.log("Barcha mevalar:", mevalar.join(", "));
```

**Topshiriq 3: package.json yaratish**

1. Yangi `mening-loyiham` papkasi yarating
2. `npm init -y` buyrug'ini bajaring
3. package.json faylida quyidagilarni o'zgartiring:
   - `"name"` - o'zingizning loyiha nomingiz
   - `"description"` - qisqa tavsif
   - `"author"` - sizning ismingiz
   - `"type": "module"` qo'shing

**Topshiriq 4: chalk bilan rangli natijalar** (Bonus)

1. `npm install chalk` o'rnating
2. `rangli.js` fayli yarating:
```javascript
import chalk from 'chalk';

console.log(chalk.blue('Bu ko\'k rang'));
console.log(chalk.green('Bu yashil rang'));
console.log(chalk.red('Bu qizil rang'));
console.log(chalk.yellow('Bu sariq rang'));
```

---

## 1-hafta — 3-dars: Express bilan birinchi server

### 📝 Uy ishi

**Topshiriq 1: Express o'rnatish va birinchi server**

1. Yangi `mening-serverim` papkasi yarating
2. `npm init -y` va `npm install express` bajaring
3. `server.js` yarating va quyidagi yo'llarni qo'shing:

**Minimal talablar:**
- `/` - "Salom! Mening serverim ishlayapti"
- `/ism` - O'zingizning ismingiz
- `/yil` - Hozirgi yil (new Date().getFullYear())
- `/kun` - Haftaning bugungi kuni

**Topshiriq 2: Mini Portfolio API**

`portfolio-server.js` yarating va quyidagi yo'llarni qo'shing:

```javascript
// Asosiy sahifa
app.get('/', function(req, res) {
  res.send('<h1>Mening Portfolio Serverim</h1>');
});

// Men haqimda
app.get('/about', function(req, res) {
  res.send('<h1>Men haqimda</h1><p>...</p>');
});

// Ko'nikmalarim
app.get('/skills', function(req, res) {
  res.send('<h1>Ko\'nikmalar</h1><ul><li>HTML</li><li>CSS</li><li>JavaScript</li></ul>');
});

// Bog'lanish
app.get('/contact', function(req, res) {
  res.send('<h1>Bog\'lanish</h1><p>Email: ...</p>');
});
```

O'zingizning ma'lumotlaringizni qo'shing!

**Topshiriq 3: Debugging mashq**

Quyidagi kodda 3 ta xato bor. Topib, to'g'rilab, ishlashiga ishonch hosil qiling:

```javascript
import express from 'express';
const app = express;
const PORT = 3000;

app.get('/', (req, res) => {
  res.send('Salom');
});

app.listen(PORT);
```

**Xatolarni toping va to'g'rilang!**

**Topshiriq 4: Qiziqarli yo'llar**

Kamida 5 ta qiziqarli yo'l yarating. Misol:
- `/random` - tasodifiy raqam (Math.random())
- `/date` - bugungi sana
- `/weather` - "Bugun quyosh chiqdi"
- `/joke` - kulgili hazil
- `/fact` - qiziqarli fakt

**Screenshot oling va saqlang!**

---

## 2-hafta — 1-dars: JSON ma'lumot va Thunder Client

### 📝 Uy ishi

**Topshiriq 1: JSON API'lar yaratish**

`json-api-server.js` yarating va quyidagilarni qo'shing:

**a) Sevimli kitoblar API** (`/books`)
- Kamida 3 ta sevimli kitobingiz
- Har birida: nomi, muallif, sahifalar soni
- JSON array formatida

**b) Sevimli filmlar API** (`/movies`)
- 5 ta sevimli film
- Har birida: nomi, yili, janr, reyting (1-10)

**c) Do'stlar API** (`/friends`)
- 3-4 ta do'stingiz
- Har birida: ism, yosh, sevimli_mashgulot

**Topshiriq 2: Thunder Client bilan test**

1. Thunder Client o'rnating (agar hali bo'lmasa)
2. Har bir endpoint'ni test qiling
3. Har bir natijadan screenshot oling
4. Bitta PDF yoki Word faylga birlashtiring

**Topshiriq 3: Murakkab obyektlar**

Quyidagi tuzilmada API yarating (`/profile`):

```json
{
  "ism": "...",
  "yosh": 14,
  "manzil": {
    "shahar": "...",
    "tuman": "...",
    "ko'cha": "..."
  },
  "maktab": {
    "nomi": "...",
    "sinf": "7A",
    "o'qituvchi": "..."
  },
  "qiziqishlar": ["...", "..."],
  "ballar": {
    "matematika": 5,
    "informatika": 5,
    "ingliz_tili": 4
  }
}
```

**Topshiriq 4: res.send() vs res.json()**

2 ta endpoint yarating:
- `/html` - res.send() bilan HTML kod
- `/data` - res.json() bilan obyekt

Farqini tushuntiring (daftaringizga yozing)

---

## 2-hafta — 2-dars: Query parametrlari

### 📝 Uy ishi

**Topshiriq 1: Salomlashish API**

`/salom` endpoint yarating:
- Query: `ism` va `til` (uz, en, ru)
- Default: ism="Do'stim", til="uz"
- Turli tillarda salomlashsin

**Misol:**
- `/salom?ism=Ali&til=en` → "Hello, Ali!"
- `/salom?ism=Aziza&til=ru` → "Привет, Aziza!"
- `/salom` → "Salom, Do'stim!"

**Topshiriq 2: Matematik amallar API**

`/calc` endpoint:
- Query: `a`, `b`, `amal` (qoshish, ayirish, kopaytirish, bolish)
- Natijani JSON da qaytarish

**Misol:**
```
/calc?a=10&b=5&amal=qoshish
```

**Natija:**
```json
{
  "a": 10,
  "b": 5,
  "amal": "qoshish",
  "natija": 15
}
```

**Topshiriq 3: Mahsulotlar filtri**

Quyidagi mahsulotlar massivini yarating va `/mahsulotlar` endpoint qiling:

```javascript
const mahsulotlar = [
  { id: 1, nomi: "Telefon", narx: 2000000, kategoriya: "elektronika" },
  { id: 2, nomi: "Kitob", narx: 50000, kategoriya: "kitob" },
  { id: 3, nomi: "Sumka", narx: 150000, kategoriya: "aksessuar" },
  { id: 4, nomi: "Noutbuk", narx: 5000000, kategoriya: "elektronika" },
  { id: 5, nomi: "Qalam", narx: 5000, kategoriya: "maktab" }
];
```

Query parametrlar:
- `kategoriya` - kategoriya bo'yicha filtr
- `minNarx` - minimal narx
- `maxNarx` - maksimal narx

**Misol:** `/mahsulotlar?kategoriya=elektronika&minNarx=1000000`

**Topshiriq 4: Qidiruv API** (Bonus)

`/search` endpoint:
- `q` - qidiruv so'zi
- Mahsulotlar nomidan qidirsin (includes() ishlatib)
- Topilgan nechta mahsulot borligini ham ko'rsatsin

**Topshiriq 5: Thunder Client test**

Barcha yaratgan API'laringizni Thunder Client da test qiling va screenshotlar to'plang.

---

## 2-hafta — 3-dars: Route parametrlari va Nodemon

### 📝 Uy ishi

**Topshiriq 1: O'quvchilar API**

```javascript
const oquvchilar = [
  { id: 1, ism: "Ali", sinf: "7A", ball: 4.5 },
  { id: 2, ism: "Aziza", sinf: "7B", ball: 5.0 },
  { id: 3, ism: "Sardor", sinf: "7A", ball: 4.2 },
  { id: 4, ism: "Malika", sinf: "7C", ball: 4.8 }
];
```

**Endpoint'lar yarating:**
- `GET /oquvchilar` - barcha o'quvchilar
- `GET /oquvchilar/:id` - bitta o'quvchi (ID bo'yicha)
- `GET /sinf/:sinf` - sinf bo'yicha o'quvchilar (params + filter)

**Topshiriq 2: Matematika jadvallari**

`/jadval/:son/:limit` endpoint yarating:
- `:son` - qaysi sonning jadvali
- `:limit` - nechtagacha ko'rsatish (masalan, 10)

**Misol:**
```
GET /jadval/7/5
```

**Natija:**
```json
{
  "son": 7,
  "limit": 5,
  "jadval": [
    "7 x 1 = 7",
    "7 x 2 = 14",
    "7 x 3 = 21",
    "7 x 4 = 28",
    "7 x 5 = 35"
  ]
}
```

**Topshiriq 3: Nodemon sozlash**

1. Loyihangizda nodemon o'rnating
2. package.json da `"start"` scriptni sozlang
3. `npm start` bilan serverni ishga tushiring
4. Kodni o'zgartirib, avtomatik restart ishlashini tekshiring
5. Screenshot oling

**Topshiriq 4: Blog Post API**

```javascript
const postlar = [
  { id: 1, sarlavha: "Backend qiziq", muallif: "Ali", ko'rishlar: 100 },
  { id: 2, sarlavha: "Node.js o'rganish", muallif: "Aziza", ko'rishlar: 250 },
  { id: 3, sarlavha: "JavaScript asoslari", muallif: "Ali", ko'rishlar: 180 }
];
```

**Endpoint'lar:**
- `GET /postlar` - barchasi
- `GET /postlar/:id` - bitta post
- `GET /muallif/:ism/postlar` - muallif bo'yicha postlar
- `GET /postlar/:id/korishlar` - ko'rishlarni 1 ga oshirish

**Topshiriq 5: Query + Params kombinatsiya**

`/oquvchilar/:sinf/filter` yarating:
- Params: `:sinf`
- Query: `?minBall=4.5`
- Natijade: faqat shu sinf va shu balldan yuqori o'quvchilar

---

## 3-hafta — 1-dars: POST so'rovi

### 📝 Uy ishi

**Topshiriq 1: Fikr-mulohaza API**

```javascript
app.post('/fikr', function(req, res) {
  const { ism, fikr, reyting } = req.body;
  
  // Validation qo'shing!
  
  res.status(201).json({
    status: 'success',
    xabar: `Rahmat, ${ism}! Fikringiz qabul qilindi.`,
    reyting: reyting
  });
});
```

**Talab:**
- `ism` majburiy, bo'sh bo'lmasligi kerak
- `fikr` majburiy, kamida 10 ta belgi
- `reyting` 1 dan 5 gacha bo'lishi kerak
- Xato bo'lsa 400 status qaytarish

**Thunder Client'da test qiling:**
- To'g'ri ma'lumot
- Bo'sh ism
- Juda qisqa fikr
- Noto'g'ri reyting (masalan, 10)

**Topshiriq 2: Ro'yxatdan o'tish API**

`POST /register` yarating:

```json
{
  "ism": "Ali",
  "email": "ali@example.com",
  "yosh": 14,
  "parol": "12345"
}
```

**Validation qoidalari:**
- `ism` - bo'sh bo'lmasin
- `email` - @ belgisi bo'lishi kerak
- `yosh` - 10 dan 18 gacha
- `parol` - kamida 5 ta belgi

Har bir xato uchun alohida xabar qaytaring!

**Topshiriq 3: Izoh qoldirish API**

`POST /comment` yarating:
```json
{
  "username": "Ali",
  "post_id": 5,
  "comment": "Juda yaxshi post!",
  "vaqt": "2025-10-11T10:30:00"
}
```

Qabul qilingandan keyin quyidagi formatda javob bering:
```json
{
  "status": "success",
  "message": "Izohingiz qo'shildi",
  "izoh": {
    "username": "Ali",
    "post_id": 5,
    "comment": "Juda yaxshi post!",
    "vaqt": "2025-10-11T10:30:00"
  }
}
```

**Topshiriq 4: Matematik masala yuborish**

`POST /masala` - foydalanuvchi matematik masala yuboradi:

```json
{
  "savol": "5 + 3 = ?",
  "javob": 8,
  "qiyinlik": "oson"
}
```

Server tekshirib, qabul qilinganini bildirsin.

---

## 3-hafta — 2-dars: Todos API (in-memory)

### 📝 Uy ishi

**Topshiriq 1: To'liq Todos API**

Darslikdagi Todos API'ga quyidagi endpoint'larni qo'shing:

**Asosiy endpoint'lar:**
- `GET /todos` - barchasi
- `POST /todos` - yangi qo'shish
- `PATCH /todos/:id` - completed ni o'zgartirish
- `DELETE /todos/:id` - o'chirish

**Qo'shimcha endpoint'lar:**
- `GET /todos/completed` - faqat bajarilganlar
- `GET /todos/pending` - faqat bajarilmaganlar
- `GET /todos/count` - statistika (jami, bajarilgan, bajarilmagan)
- `DELETE /todos/completed` - barcha bajarilganlarni o'chirish
- `GET /todos/:id` - bitta todo (ID bo'yicha)

**Topshiriq 2: Kitoblar kutubxonasi API**

```javascript
let kutubxona = [];
```

**Endpoint'lar:**
- `POST /books` - yangi kitob qo'shish
  ```json
  {
    "nomi": "Alpomish",
    "muallif": "Xalq og'zaki ijodi",
    "sahifalar": 120,
    "o'qilgan": false
  }
  ```
- `GET /books` - barcha kitoblar
- `GET /books/:id` - bitta kitob
- `PATCH /books/:id/read` - o'qilgan = true qilish
- `DELETE /books/:id` - kitobni o'chirish
- `GET /books/stats` - statistika

**Validation:**
- `nomi` va `muallif` majburiy
- `sahifalar` > 0
- 404 agar kitob topilmasa

**Topshiriq 3: Buyurtmalar API**

```javascript
let buyurtmalar = [];
```

**Tuzilma:**
```json
{
  "id": 1,
  "mahsulot": "Pizza",
  "miqdor": 2,
  "narx": 50000,
  "status": "kutilmoqda"
}
```

**Endpoint'lar:**
- `POST /buyurtmalar` - yangi buyurtma
- `GET /buyurtmalar` - barchasi
- `PATCH /buyurtmalar/:id/status` - statusni o'zgartirish
  - kutilmoqda → tayyorlanmoqda → tayyor → yetkazildi
- `DELETE /buyurtmalar/:id` - bekor qilish
- `GET /buyurtmalar/stats` - jami summa va buyurtmalar soni

**Topshiriq 4: Test ssenariyasi**

Thunder Client da quyidagilarni bajaring va natijalarini yozib boring:

1. 3 ta todo qo'shing (POST)
2. Barchasini ko'ring (GET)
3. Bitta todo'ni completed qiling (PATCH)
4. Statistikani tekshiring (GET /count)
5. 1 ta todo'ni o'chiring (DELETE)
6. Yana barchasini ko'ring

Har bir qadam uchun status kod va javobni yozib boring!

---

## 4-hafta — 1-dars: Memory vs Database

### 📝 Uy ishi

**Topshiriq 1: Taqqoslash jadvali**

Daftaringizga quyidagi jadvalni to'ldiring:

| Xususiyat | In-Memory | Database (lowdb) |
|-----------|-----------|------------------|
| Tezlik | ? | ? |
| Ma'lumot saqlanishimi? | ? | ? |
| Qiyin-osonligi | ? | ? |
| Qachon ishlatamiz? | ? | ? |

**Topshiriq 2: lowdb o'rnatish**

1. Yangi `database-test` papkasi yarating
2. npm init va lowdb o'rnating
3. `test-db.js` yarating:

```javascript
import { Low } from 'lowdb';
import { JSONFile } from 'lowdb/node';

const adapter = new JSONFile('test.json');
const db = new Low(adapter, { talabalar: [] });

await db.read();

// 3 ta talaba qo'shing
db.data.talabalar.push({ id: 1, ism: "Ali", ball: 5 });
db.data.talabalar.push({ id: 2, ism: "Aziza", ball: 4 });
db.data.talabalar.push({ id: 3, ism: "Sardor", ball: 5 });

await db.write();

console.log('Saqlandi:', db.data.talabalar);
```

4. Ishga tushiring va `test.json` faylini tekshiring

**Topshiriq 3: Eksperiment**

1. Yuqoridagi kodni ishga tushiring
2. `test.json` faylini oching va ichiga qarang
3. Kodni yana ishga tushiring (takroriy)
4. Nima bo'ladi? (Daftaringizga yozing)
5. Kodni o'zgartirib, 2 ta yana talaba qo'shing
6. Endi `test.json` da nima bor?

**Topshiriq 4: O'zingizning ma'lumotlaringiz**

`mening-db.js` yarating va quyidagilarni saqlang:
- Sevimli musiqalaringiz
- Sevimli taomlaringiz
- Sevimli joylaringiz

Har safar ishga tushirganda yangisini qo'shing va fayl o'sishini kuzating!

---

## 4-hafta — 2-dars: lowdb bilan Todos API

### 📝 Uy ishi

**Topshiriq 1: Todos API'ni lowdb ga o'tkazish**

Darslikdagi koddan foydalanib:
1. db.json faylini yarating
2. server.js da lowdb'ni sozlang
3. GET /todos va POST /todos ishlatishni ta'minlang
4. Test qiling va screenshotlar oling

**Topshiriq 2: Xarajatlar API** (Budget Tracker)

`budget-server.js` va `budget.json` yarating:

```javascript
// budget.json boshlang'ich holat
{
  "xarajatlar": []
}
```

**API tuzilmasi:**
```json
{
  "id": 1,
  "nom": "Tushlik",
  "summa": 15000,
  "kategoriya": "ovqat",
  "sana": "2025-10-11"
}
```

**Endpoint'lar:**
- `POST /xarajat` - yangi xarajat qo'shish
- `GET /xarajatlar` - barchasi
- `GET /xarajatlar/jami` - umumiy summa
- `GET /xarajatlar/kategoriya/:kat` - kategoriya bo'yicha
- `DELETE /xarajatlar/:id` - o'chirish

**Topshiriq 3: Darslar jadvali API**

```javascript
// jadval.json
{
  "darslar": []
}
```

**Har bir dars:**
```json
{
  "id": 1,
  "fan": "Matematika",
  "kun": "Dushanba",
  "soat": "8:00",
  "xona": "201",
  "o'qituvchi": "..."
}
```

**Endpoint'lar:**
- `POST /dars` - yangi dars qo'shish
- `GET /darslar` - barcha darslar
- `GET /darslar/kun/:kun` - kun bo'yicha darslar
- `PUT /darslar/:id` - darsni to'liq yangilash
- `DELETE /darslar/:id` - o'chirish

**Topshiriq 4: Server restart testi**

1. Todos API'ngizga 5 ta todo qo'shing
2. Serverni to'xtating (Ctrl+C)
3. Serverni qayta ishga tushiring
4. GET /todos qiling
5. Ma'lumotlar saqlangani uchun screenshotlar oling

**Bu isbotlaydi:** lowdb ma'lumotni faylda saqlaydi! ✅

---

## 4-hafta — 3-dars: To'liq CRUD (lowdb)

### 📝 Uy ishi

**Topshiriq 1: To'liq CRUD Todos**

Darslikdagi barcha endpoint'larni yozing va test qiling:

**Checklist:**
- [ ] GET /todos - barchasi
- [ ] POST /todos - yangi qo'shish
- [ ] GET /todos/:id - bitta todo
- [ ] PATCH /todos/:id - completed toggle
- [ ] PUT /todos/:id - to'liq yangilash
- [ ] DELETE /todos/:id - o'chirish

Har birini Thunder Client da test qilib, screenshot to'plang!

**Topshiriq 2: Kontaktlar API** (Full CRUD)

`contacts-server.js` va `contacts.json` yarating:

```json
{
  "id": 1,
  "ism": "Ali Valiyev",
  "telefon": "+998901234567",
  "email": "ali@example.com",
  "manzil": "Toshkent",
  "sevimli": false
}
```

**To'liq CRUD:**
- CREATE: `POST /contacts`
- READ: `GET /contacts`, `GET /contacts/:id`
- UPDATE: `PUT /contacts/:id`, `PATCH /contacts/:id/favorite`
- DELETE: `DELETE /contacts/:id`

**Qo'shimcha:**
- `GET /contacts/favorites` - faqat sevimlilar
- `GET /contacts/search?q=Ali` - qidiruv

**Topshiriq 3: Do'kon Mahsulotlari API**

```javascript
// products.json
{
  "mahsulotlar": []
}
```

**Mahsulot tuzilmasi:**
```json
{
  "id": 1,
  "nomi": "Telefon",
  "narx": 2000000,
  "soni": 10,
  "kategoriya": "elektronika",
  "sotuvda": true
}
```

**Full CRUD + Extra:**
- `POST /products` - qo'shish
- `GET /products` - barchasi
- `GET /products/:id` - bitta mahsulot
- `PATCH /products/:id/stock` - sonini o'zgartirish (body: {soni: 5})
- `PATCH /products/:id/sale` - sotuvda true/false
- `PUT /products/:id` - to'liq yangilash
- `DELETE /products/:id` - o'chirish
- `GET /products/search?q=telefon` - qidiruv
- `GET /products/category/:kat` - kategoriya bo'yicha

**Topshiriq 4: Musiqa Playlist API**

```javascript
// playlist.json
{
  "qoshiqlar": []
}
```

**Qo'shiq tuzilmasi:**
```json
{
  "id": 1,
  "nomi": "Yomg'ir",
  "ijrochi": "Shahzoda",
  "davomiyligi": "3:45",
  "yil": 2020,
  "sevimli": false
}
```

**Endpoint'lar o'ylab toping va yozing!** (CRUD asosida)

**Topshiriq 5: Test ssenariyasi (To'liq)**

Kontaktlar API uchun quyidagi test ssenariysini bajaring:

1. **CREATE** - 3 ta kontakt qo'shing
2. **READ ALL** - barchasini oling
3. **READ ONE** - bitta kontaktni ID bo'yicha oling
4. **UPDATE** - bitta kontaktni sevimli qiling
5. **UPDATE FULL** - bitta kontaktning barcha ma'lumotini o'zgartiring
6. **DELETE** - bitta kontaktni o'chiring
7. **VERIFY** - serverni restart qiling va ma'lumot saqlanganini tekshiring

Har bir qadam uchun:
- Thunder Client screenshot
- Status kod
- Javob JSON

**PDF shaklida topshiring!**

---

## 🎯 Yakuniy Katta Loyiha (Ixtiyoriy, Bonus)

Quyidagi loyihalardan **birini** tanlang va to'liq bajaring:

### **Variant A: Maktab Talabalar Boshqaruv Tizimi**

**Ma'lumotlar:**
```json
{
  "talabalar": [
    {
      "id": 1,
      "ism": "Ali Valiyev",
      "sinf": "7A",
      "ballari": {
        "matematika": 5,
        "fizika": 4,
        "kimyo": 5,
        "informatika": 5
      },
      "davomat": 95
    }
  ]
}
```

**Endpoint'lar:**
- CRUD: POST, GET, PUT, DELETE
- `GET /talabalar/sinf/:sinf` - sinf bo'yicha
- `GET /talabalar/:id/ortacha` - o'rtacha ball hisoblash
- `GET /talabalar/top` - eng yaxshi 5 ta talaba
- `PATCH /talabalar/:id/ball` - yangi ball qo'shish

### **Variant B: Mini Do'kon API**

**Ma'lumotlar:**
```json
{
  "mahsulotlar": [],
  "buyurtmalar": []
}
```

**Mahsulot:**
```json
{
  "id": 1,
  "nomi": "Telefon",
  "narx": 2000000,
  "soni": 10,
  "rasm": "phone.jpg"
}
```

**Buyurtma:**
```json
{
  "id": 1,
  "mahsulot_id": 1,
  "miqdor": 2,
  "jami": 4000000,
  "mijoz": "Ali",
  "status": "kutilmoqda"
}
```

**Endpoint'lar:**
- Mahsulotlar uchun to'liq CRUD
- Buyurtmalar uchun to'liq CRUD
- `POST /buyurtma` - buyurtma qilganda mahsulot sonini kamaytirish
- `GET /mahsulotlar/available` - faqat mavjud mahsulotlar (soni > 0)
- `GET /buyurtmalar/jami` - barcha buyurtmalar summasi

### **Variant C: Blog Post Tizimi**

**Ma'lumotlar:**
```json
{
  "postlar": [],
  "izohlar": []
}
```

**Post:**
```json
{
  "id": 1,
  "sarlavha": "Backend qiziq",
  "matn": "...",
  "muallif": "Ali",
  "vaqt": "2025-10-11T10:00:00",
  "ko'rishlar": 0,
  "likelar": 0
}
```

**Izoh:**
```json
{
  "id": 1,
  "post_id": 1,
  "username": "Aziza",
  "matn": "Juda yaxshi!",
  "vaqt": "2025-10-11T11:00:00"
}
```

**Endpoint'lar:**
- Postlar uchun CRUD
- Izohlar uchun CRUD
- `GET /postlar/:id/izohlar` - post uchun barcha izohlar
- `PATCH /postlar/:id/view` - ko'rishlarni 1 ga oshirish
- `PATCH /postlar/:id/like` - like qo'shish
- `GET /postlar/popular` - eng ko'p ko'rilgan 5 ta post

---

## 📤 Topshirish Ko'rsatmasi

### Nima topshirasiz?

**Har bir uy ishi uchun:**
1. ✅ Kod fayllari (server.js, db.json va boshqalar)
2. ✅ Thunder Client screenshot'lari
3. ✅ `README.md` fayli (qanday ishga tushirish haqida)
4. ✅ package.json fayli

### README.md shabloni:

```markdown
# Uy Ishi - [Dars nomi]

## Talabalar:
- Ismingiz
- Sana
- Dars: 1-hafta — 1-dars

## Loyihani ishga tushirish:

1. `npm install`
2. `npm start`
3. Brauzer: `http://localhost:3000`

## Endpoint'lar:

- GET /... - tavsif
- POST /... - tavsif
- ...

## Test natijalar:

(Screenshot'lar)

## Qiyinchiliklar:

(Qanday muammolar bo'ldi va qanday yechdingiz)
```

---

## ⭐ Bonus Topshiriqlar (Qo'shimcha ball)

### Bonus 1: Error Handling

Barcha API'laringizga try-catch va xatolarni to'g'ri qaytarish mexanizmini qo'shing.

### Bonus 2: Logging

Har bir so'rovni console.log qiling:
```javascript
app.use(function(req, res, next) {
  console.log(`${req.method} ${req.url} - ${new Date().toLocaleString()}`);
  next();
});
```

### Bonus 3: Data Validation

Har bir POST/PUT/PATCH da to'liq validation qo'shing va test qiling.

### Bonus 4: API Documentation

Barcha endpoint'laringiz uchun to'liq hujjat yozing:
- URL
- Method
- Body format
- Response format
- Xato holatlari

---

## 🏆 Baholash Mezonlari

| Mezon | Ball |
|-------|------|
| Kod to'g'ri ishlaydi | 40% |
| Validation qo'shilgan | 15% |
| Thunder Client test screenshot'lari | 20% |
| README.md to'liq | 10% |
| Kod tozaligi va izohlar | 10% |
| Kreativlik va qo'shimcha funksiyalar | 5% |

**Jami:** 100%

---

## 💡 Foydali Maslahatlar

1. **Kodni izohlab yozing** - keyinchalik tushunish oson bo'ladi
2. **Har bir endpoint'ni alohida test qiling** - hammasi birga ishlamasa, topish qiyin
3. **Default qiymatlarni unutmang** - xatolardan saqlanadi
4. **Git ishlatishni o'rganing** - kodingizni saqlash uchun
5. **Do'stlar bilan o'rtoqlashing** - birga o'rganish osonroq
6. **Xato chiqsa qo'rqmang** - bu normal, debugging o'rganing!

**Omad tilaymiz!** 🚀 Savollar bo'lsa o'qituvchiga murojaat qiling!

