<details>
    <summary>Ma’lumotlar bazasi tushunchasi va SQLite bilan tanishuv</summary>
## 🗓️ 5-hafta — 1-dars

### 🏷️ Mavzu: **Ma’lumotlar bazasi tushunchasi va SQLite bilan tanishuv**

---

### 1️⃣ Nega bizga “database” kerak?

Oldingi darslarda biz **lowdb** orqali ma’lumotni faylga yozib saqladik. Bu kichik loyihalar uchun yaxshi, ammo **real loyihalarda** kuchliroq yechim kerak bo‘ladi.

* Fayl ko‘paysa, tartibni saqlash qiyinlashadi.
* Katta ma’lumotlarda fayl bilan ishlash sekinlashadi.
* Bizga qidirish, filtrlash, tartiblash, statistikalar uchun qulay usullar kerak bo‘ladi.

Shuning uchun professional loyihalarda **database (ma’lumotlar bazasi)** ishlatiladi.

---

### 2️⃣ Table, Row, Column tushunchasi

**Database** ichidagi ma’lumotlar **jadval (table)** ko‘rinishida saqlanadi. Bu **Excel** yoki **Google Sheets** ga o‘xshaydi.

* **Table (jadval)** → Ma’lumotlar guruhi (masalan, `users`, `products`, `todos`).
* **Column (ustun)** → Har bir ma’lumot turi (masalan, `id`, `title`, `completed`).
* **Row (qator)** → Bitta yozuv (masalan, bitta todo).

**Misol jadval: `todos`**

| id | title                | completed |
| -- | -------------------- | --------- |
| 1  | Uy vazifasini qilish | false     |
| 2  | Kitob o‘qish         | true      |
| 3  | Sport zalga borish   | false     |

✅ Jadvalda har bir **row** — bitta vazifa, ustunlar — xususiyatlar.

---

### 3️⃣ SQL nima?

**SQL** (Structured Query Language) — ma’lumotlar bazasi bilan gaplashish tili.

SQL yordamida:

* **CREATE** — yangi jadval yaratamiz.
* **INSERT** — yangi ma’lumot qo‘shamiz.
* **SELECT** — ma’lumotni o‘qib olamiz.
* **UPDATE** — mavjud ma’lumotni yangilaymiz.
* **DELETE** — ma’lumotni o‘chirib tashlaymiz.

Misol:

```sql
SELECT * FROM todos;
```

→ barcha vazifalarni olib keladi.

```sql
INSERT INTO todos (title, completed) VALUES ('Kitob o‘qish', false);
```

→ yangi vazifa qo‘shadi.

---

### 4️⃣ SQLite nima?

**SQLite** — juda yengil va oddiy database tizimi.

* Faqat bitta fayl (`.db`) yaratadi — butun ma’lumot shu faylda.
* Server kerak emas, hamma narsa ichida.
* Juda tez va sodda, kichik va o‘rta loyihalar uchun juda qulay.

Shuning uchun biz SQLite’dan boshlaymiz.

---

### 5️⃣ VS Code uchun SQLite extension o‘rnatish

Ma’lumotlarni qulay ko‘rish uchun biz **SQLite extension** ishlatamiz.

1. VS Code’ni oching.
2. Chap tomondan Extensions (pazl belgisi) ni bosing.
3. Qidiruv maydoniga **SQLite** deb yozing.
4. “**SQLite Viewer**” yoki “**SQLite Explorer**” (ikkisidan biri bo‘lishi mumkin) ni o‘rnating.
5. O‘rnatilgach, VS Code’da yangi tugma chiqadi (odatda “database” belgisi bilan).
6. Shu orqali `.db` fayllarini ochib ichidagi jadvallarni ko‘ra olamiz.

---

### 6️⃣ SQLite bilan ishlashni boshlash

1. Terminalda SQLite o‘rnatilganligini tekshirish:

```bash
sqlite3 --version
```

Agar versiya chiqsa, SQLite ishlashga tayyor. (Agar topilmasa, [https://sqlite.org/download.html](https://sqlite.org/download.html) dan yuklab olish mumkin.)

2. Yangi database fayl yaratish:

```bash
sqlite3 todos.db
```

3. SQLite buyruqlarida:

```sql
CREATE TABLE todos (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  title TEXT,
  completed BOOLEAN
);
```

* `id` — unikal raqam (avtomatik qo‘shiladi)
* `title` — matn
* `completed` — boolean (true/false)

4. Dastlabki ma’lumot qo‘shamiz:

```sql
INSERT INTO todos (title, completed) VALUES ('Uy vazifasi qilish', false);
INSERT INTO todos (title, completed) VALUES ('Kitob o‘qish', true);
```

5. Barchasini ko‘rish:

```sql
SELECT * FROM todos;
```

---

### Amaliy mashq

1. VS Code’da yangi fayl `todos.db` yarating.
2. SQLite extension orqali oching.
3. “Run SQL query” orqali yuqoridagi `CREATE TABLE` va `INSERT` kodlarini yozing.
4. `SELECT * FROM todos;` bilan natijani ko‘ring.

---

### Asosiy tushunchalar

* **Database** — ma’lumotni doimiy saqlaydigan tizim.
* **Table, Row, Column** — jadval tuzilmasi.
* **SQL** — database bilan ishlash uchun til.
* **SQLite** — oddiy, yengil va fayl asosidagi database.
* VS Code uchun SQLite extension — ma’lumotni ko‘rish va test qilishni osonlashtiradi.

---

</details>

<hr>

<details>
    <summary>Node.js orqali SQLite bilan ishlash</summary>

## 🗓️ 5-hafta — 2-dars

### 🏷️ Mavzu: **Node.js orqali SQLite bilan ishlash**

---

### 1️⃣ Nega biz endi Node’dan SQLite bilan bog‘laymiz?

Oldingi darsda biz SQLite’ni bevosita terminal yoki VS Code extension orqali ishlatdik.
Ammo **backend server** yozayotganimizda, ma’lumotlarni **koddan turib** qo‘shish, o‘chirish, o‘qish kerak bo‘ladi.
Bugun Node.js’dan to‘g‘ridan-to‘g‘ri SQLite bilan ishlashni o‘rganamiz.

---

### 2️⃣ better-sqlite3 nima?

Node.js uchun SQLite bilan ishlashga yordam beradigan kutubxona.

* Tez va sodda.
* Promiseless (async/await kerak emas — lekin oddiy ishlash uchun juda yaxshi).
* Kichik loyihalar uchun juda qulay.

---

### 3️⃣ better-sqlite3 o‘rnatish

Terminalda:

```bash
npm install better-sqlite3
```

✅ Shu bilan loyihamizga kutubxona qo‘shildi.

---

### 4️⃣ Yangi fayl: `db.js`

Biz alohida `db.js` fayli yaratib, SQLite ulanishini shu yerga yozamiz.

```javascript
// db.js
import Database from 'better-sqlite3';

const db = new Database('todos.db'); // fayl nomi: todos.db (agar bo‘lmasa, avtomatik yaratiladi)

// 1. Agar jadval yo‘q bo‘lsa — yaratamiz
db.prepare(`
  CREATE TABLE IF NOT EXISTS todos (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    title TEXT NOT NULL,
    completed BOOLEAN DEFAULT 0
  )
`).run();

export default db;
```

✅ Bu kod shuni qiladi:

* `todos.db` faylini ochadi yoki yaratadi.
* Ichida `todos` jadvali bor-yo‘qligini tekshiradi, bo‘lmasa yaratadi.

---

### 5️⃣ Node.js orqali ma’lumot yozish (INSERT)

`server.js` faylida yoki sinov uchun alohida faylda yozamiz:

```javascript
import db from './db.js';

// Ma’lumot qo‘shish (INSERT)
const insert = db.prepare('INSERT INTO todos (title, completed) VALUES (?, ?)');
insert.run('Uy vazifasini qilish', false);
insert.run('Kitob o‘qish', true);

console.log('Ma’lumot qo‘shildi!');
```

✅ `?` belgisi o‘rniga keyinchalik qiymatlar qo‘yiladi (`title`, `completed`).

---

### 6️⃣ Ma’lumot o‘qish (SELECT)

```javascript
// SELECT — barchasini olish
const rows = db.prepare('SELECT * FROM todos').all();
console.log(rows);
```

Terminalda ishga tushiring:

```bash
node server.js
```

Natija:

```bash
[
  { id: 1, title: 'Uy vazifasini qilish', completed: 0 },
  { id: 2, title: 'Kitob o‘qish', completed: 1 }
]
```

> Eslatma: SQLite’da `BOOLEAN` asosan `0` yoki `1` ko‘rinishida saqlanadi.

---

### 7️⃣ Parametr bilan SELECT

Agar faqat bitta todo’ni olish kerak bo‘lsa:

```javascript
const getOne = db.prepare('SELECT * FROM todos WHERE id = ?');
const todo = getOne.get(1); // id = 1 bo‘lgan todo
console.log(todo);
```

Natija:

```bash
{ id: 1, title: 'Uy vazifasini qilish', completed: 0 }
```

---

### 8️⃣ Amaliy mashq

1. **Yangi todo qo‘shish:**
   Kodga `insert.run('Yangi dars qilish', false)` qo‘shing.

2. **Barcha todo’larni ko‘rish:**
   `db.prepare('SELECT * FROM todos').all()` orqali chiqarib ko‘ring.

3. **Bitta todo topish:**
   `db.prepare('SELECT * FROM todos WHERE id = ?').get(2)` bilan ikkinchi todo’ni ko‘ring.

---

### 9️⃣ Keyingi qadamlar

Endi biz Node orqali SQLite bilan ishlashni boshladik:

* Ma’lumotlar saqlanadi va qayta o‘qiladi.
* Jadval yaratish, yozish va o‘qish ishladi.

Keyingi darsda bu kodni **Express serveriga bog‘lab**, `GET /todos`, `POST /todos` ni SQLite’dan foydalanib ishlatamiz. Bu orqali API real database bilan ishlay boshlaydi.

---

### Asosiy tushunchalar

* **better-sqlite3** — Node.js uchun sodda va tez SQLite kutubxonasi.
* **CREATE TABLE IF NOT EXISTS** — jadval yo‘q bo‘lsa yaratadi.
* **INSERT** — ma’lumot qo‘shish.
* **SELECT** — ma’lumot o‘qish (`all()` barcha, `get()` bitta yozuv uchun).
* `?` — SQL so‘rovda parametr qo‘yish uchun xavfsiz usul.

---
</details>

<hr>

<details>
    <summary>Express API’ni lowdb’dan SQLite’ga o‘tkazish</summary>

## 🗓️ 5-hafta — 3-dars

### 🏷️ Mavzu: **Express API’ni lowdb’dan SQLite’ga o‘tkazish**

---

### 🎯 Maqsad

Oldingi darsda biz Node orqali **SQLite** bilan ishlashni o‘rgandik.
Bugun “Todos API”ni lowdb o‘rniga **SQLite** bilan ishlaydigan qilamiz.

✅ Natijada:

* API endi haqiqiy ma’lumotlar bazasi bilan ishlaydi.
* Ma’lumotlar server o‘chib qayta yoqilganda ham saqlanib qoladi.
* Bizning kod professionalroq bo‘lib qoladi.

---

### 1️⃣ Avvalgi lowdb kodimiz

Oldin shunday edi:

```javascript
import { Low } from 'lowdb'
import { JSONFile } from 'lowdb/node'
const adapter = new JSONFile('db.json')
const db = new Low(adapter, { todos: [] })
await db.read()
db.data ||= { todos: [] }
```

Endi lowdb kerak emas — o‘rniga **better-sqlite3** va `db.js` dan foydalanamiz.

---

### 2️⃣ `db.js` fayli

`db.js` faylingizni quyidagicha yarating yoki yangilang:

```javascript
// db.js
import Database from 'better-sqlite3';

const db = new Database('todos.db');

// Jadval mavjud bo‘lmasa, yaratamiz
db.prepare(`
  CREATE TABLE IF NOT EXISTS todos (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    title TEXT NOT NULL,
    completed BOOLEAN DEFAULT 0
  )
`).run();

export default db;
```

✅ Bu kod:

* `todos.db` faylini ochadi yoki yaratadi.
* `todos` jadvalini tayyorlab qo‘yadi.

---

### 3️⃣ `server.js` ni yangilash (Express + SQLite)

```javascript
import express from 'express'
import db from './db.js'

const app = express()
const PORT = 3000

app.use(express.json())

// GET /todos — barcha vazifalarni olish
app.get('/todos', (req, res) => {
  const todos = db.prepare('SELECT * FROM todos').all()
  res.json(todos)
})

// POST /todos — yangi vazifa qo‘shish
app.post('/todos', (req, res) => {
  const { title } = req.body
  if (!title || !title.trim()) {
    return res.status(400).json({ status: 'error', message: 'Todo nomi kerak!' })
  }

  const stmt = db.prepare('INSERT INTO todos (title, completed) VALUES (?, ?)')
  const info = stmt.run(title.trim(), false)

  const todo = db.prepare('SELECT * FROM todos WHERE id = ?').get(info.lastInsertRowid)
  res.status(201).json({ status: 'success', todo })
})

app.listen(PORT, () => {
  console.log(`✅ Server ishlayapti: http://localhost:${PORT}`)
})
```

**Asosiy o‘zgarishlar:**

* `lowdb` kodlari olib tashlandi.
* `db.prepare(...).all()` → barcha yozuvlarni olish.
* `db.prepare(...).run()` → yangi yozuv qo‘shish.
* `info.lastInsertRowid` → yangi qo‘shilgan yozuvning `id`si.

---

### 4️⃣ Serverni ishga tushirish

```bash
npm start
```

Brauzerda yoki Thunder Client’da sinab ko‘ring.

---

### 5️⃣ Thunder Client orqali sinov

#### A. Yangi todo qo‘shish

* Method: **POST**
* URL: `http://localhost:3000/todos`
* Body → JSON:

```json
{ "title": "Backend kursini yakunlash" }
```

✅ Javob:

```json
{
  "status": "success",
  "todo": {
    "id": 1,
    "title": "Backend kursini yakunlash",
    "completed": 0
  }
}
```

#### B. Barcha todo’larni olish

* Method: **GET**
* URL: `http://localhost:3000/todos`

✅ Javob:

```json
[
  { "id": 1, "title": "Backend kursini yakunlash", "completed": 0 }
]
```

---

### 6️⃣ Ma’lumot server o‘chganda ham qoladi

1. Serverni `CTRL + C` bilan to‘xtating.
2. Yana `npm start` bilan ishga tushiring.
3. `GET /todos` ga so‘rov yuboring — yozgan vazifalaringiz hamon bor!

✅ Chunki endi ma’lumotlar **todos.db** faylida saqlanadi.

---

### 7️⃣ Manual DB inspection (qo‘lda ko‘rish)

**VS Code SQLite extension** orqali:

* Chap tomonda “SQLite Explorer” yoki “Database” tugmasini bosing.
* `todos.db` faylini tanlang.
* “todos” jadvalini ko‘rib, yozuvlaringizni tekshiring.

**Terminal orqali:**

```bash
sqlite3 todos.db
sqlite> SELECT * FROM todos;
```

---

### Qo‘shimcha mashqlar

1. `completed` qiymatini teskari qilish uchun PATCH qo‘shing:

```javascript
app.patch('/todos/:id', (req, res) => {
  const id = Number(req.params.id)
  const todo = db.prepare('SELECT * FROM todos WHERE id = ?').get(id)
  if (!todo) return res.status(404).json({ message: 'Todo topilmadi' })

  const updated = db.prepare('UPDATE todos SET completed = ? WHERE id = ?')
  updated.run(!todo.completed, id)

  const refreshed = db.prepare('SELECT * FROM todos WHERE id = ?').get(id)
  res.json({ status: 'success', todo: refreshed })
})
```

2. `DELETE /todos/:id` ni yozib ko‘ring.

---

### Asosiy tushunchalar

* **lowdb** → JSON faylga yozardi, lekin endi biz haqiqiy **SQLite database** ishlatdik.
* **better-sqlite3** — SQL so‘rovlarni Node’dan to‘g‘ridan-to‘g‘ri bajaradi.
* **.all()** → bir nechta qator olish.
* **.get()** → bitta qator olish.
* **.run()** → INSERT/UPDATE/DELETE bajarish.

---

✅ Sizning Todos API’ingiz endi to‘liq SQLite bilan ishlayapti!
Ma’lumotlar server qayta ishga tushganda ham yo‘qolmaydi.
Keyingi qadam — bu API’ni yanada professional qilish (xatolarni yaxshi qaytarish, kodni modulga ajratish, autentifikatsiya asoslarini ko‘rsatish).

</details>

<hr>

<details>
    <summary>Status kodlari va xatolarni to‘g‘ri qaytarish</summary>

## 🗓️ 6-hafta — 1-dars

### 🏷️ Mavzu: **Status kodlari va xatolarni to‘g‘ri qaytarish**

---

### 1️⃣ HTTP status kodlari nima?

Bizning API foydalanuvchiga faqat JSON emas, balki **status kod** ham yuboradi.
Status kod — bu **raqamli signal**, serverdan keladigan javobning turini bildiradi.

Misol:

* ✅ 200 — hammasi yaxshi, javob tayyor.
* ✅ 201 — yangi resurs yaratildi.
* ⚠️ 400 — foydalanuvchi noto‘g‘ri so‘rov yubordi.
* ❌ 404 — topilmadi.

Status kodlarni to‘g‘ri ishlatish — yaxshi backendning asosiy belgilaridan biri.

---

### 2️⃣ Asosiy status kodlar

| Kod     | Nomi        | Qachon ishlatiladi                                                         |
| ------- | ----------- | -------------------------------------------------------------------------- |
| **200** | OK          | Har bir narsa muvaffaqiyatli o‘tgan bo‘lsa. (Masalan, `GET /todos`)        |
| **201** | Created     | Yangi obyekt yaratildi (masalan, `POST /todos` dan keyin).                 |
| **400** | Bad Request | Foydalanuvchi noto‘g‘ri ma’lumot yuborgan bo‘lsa (masalan, `title` bo‘sh). |
| **404** | Not Found   | So‘ralgan ma’lumot topilmasa (masalan, noto‘g‘ri `id` yuborilgan).         |

> Bundan tashqari ko‘plab status kodlar bor (500, 401, 403 va h.k.), lekin hozir eng kerakli 4 tasini o‘rganamiz.

---

### 3️⃣ Keling, mavjud API kodini yangilaymiz

**server.js** (SQLite bilan ishlayotgan):

```javascript
import express from 'express'
import db from './db.js'

const app = express()
const PORT = 3000

app.use(express.json())

// GET /todos — barcha vazifalar
app.get('/todos', (req, res) => {
  const todos = db.prepare('SELECT * FROM todos').all()
  res.status(200).json(todos) // 200 OK
})

// POST /todos — yangi vazifa qo‘shish
app.post('/todos', (req, res) => {
  const { title } = req.body
  if (!title || !title.trim()) {
    return res.status(400).json({
      status: 'error',
      message: 'Todo nomi kerak!'
    })
  }

  const info = db.prepare('INSERT INTO todos (title, completed) VALUES (?, ?)').run(title.trim(), false)
  const todo = db.prepare('SELECT * FROM todos WHERE id = ?').get(info.lastInsertRowid)

  res.status(201).json({ status: 'success', todo }) // 201 Created
})

// PATCH /todos/:id — completed ni o‘zgartirish
app.patch('/todos/:id', (req, res) => {
  const id = Number(req.params.id)
  if (Number.isNaN(id)) {
    return res.status(400).json({ status: 'error', message: 'ID noto‘g‘ri' })
  }

  const todo = db.prepare('SELECT * FROM todos WHERE id = ?').get(id)
  if (!todo) {
    return res.status(404).json({ status: 'error', message: 'Todo topilmadi' })
  }

  db.prepare('UPDATE todos SET completed = ? WHERE id = ?').run(!todo.completed, id)
  const updated = db.prepare('SELECT * FROM todos WHERE id = ?').get(id)

  res.status(200).json({ status: 'success', todo: updated })
})

// DELETE /todos/:id — o‘chirish
app.delete('/todos/:id', (req, res) => {
  const id = Number(req.params.id)
  if (Number.isNaN(id)) {
    return res.status(400).json({ status: 'error', message: 'ID noto‘g‘ri' })
  }

  const todo = db.prepare('SELECT * FROM todos WHERE id = ?').get(id)
  if (!todo) {
    return res.status(404).json({ status: 'error', message: 'Todo topilmadi' })
  }

  db.prepare('DELETE FROM todos WHERE id = ?').run(id)
  res.status(200).json({ status: 'success', message: 'Todo o‘chirildi' })
})

app.listen(PORT, () => {
  console.log(`✅ Server: http://localhost:${PORT}`)
})
```

---

### 4️⃣ Thunder Client orqali mashq

1. **GET /todos**

   * URL: `http://localhost:3000/todos`
   * Javobda yuqorida `200 OK` ko‘rinadi.

2. **POST /todos** (to‘g‘ri ma’lumot bilan)

   * Body:

     ```json
     { "title": "Matematika vazifasini bajarish" }
     ```
   * Javob: `201 Created`.

3. **POST /todos** (xato — bo‘sh body)

   * Body:

     ```json
     {}
     ```
   * Javob: `400 Bad Request`.

4. **PATCH /todos/:id** (mavjud bo‘lmagan id bilan)

   * URL: `http://localhost:3000/todos/999`
   * Javob: `404 Not Found`.

5. **DELETE /todos/:id** (mavjud id bilan)

   * Javob: `200 OK`.

---

### 5️⃣ Status kodlar qachon ishlatiladi — qisqacha

* **200 OK** → Odatdagi barcha muvaffaqiyatli javoblar.
* **201 Created** → Yangi resurs yaratilganda.
* **400 Bad Request** → So‘rovdagi ma’lumot noto‘g‘ri yoki yetarli emas.
* **404 Not Found** → Resurs topilmaganida.

---

### Mashq

* Sizning mavjud `GET/POST/PATCH/DELETE` kodlaringizni yuqoridagi kabi status kodlar bilan yangilang.
* Thunder Client orqali har bir so‘rovni test qiling va “Response” oynasida **status code** ni tekshiring.
* Xatoliklarda foydalanuvchiga tushunarli xabar yuboring.

---

### Asosiy tushunchalar

* **Status code** — serverdan javobning turini bildiruvchi raqam.
* To‘g‘ri status kod yozish API’ni professional va tushunarli qiladi.
* `res.status(kod).json(...)` orqali kodni qo‘yib javob yuboriladi.

---

✅ Endi sizning API’ingiz **status kodlarni professional darajada qaytaradi**.
Keyingi darsda biz **xatolarni yagona joyda boshqarish (Error Handling Middleware)** va API’ni yanada toza qilishni o‘rganamiz.

</details>

<hr>

<details>
    <summary>Kiritilgan ma’lumotni tekshirish (Input Validation)</summary>

## 🗓️ 6-hafta — 2-dars

### 🏷️ Mavzu: **Kiritilgan ma’lumotni tekshirish (Input Validation)**

---

### 1️⃣ Nega input validation kerak?

API yozayotganda foydalanuvchi (yoki dastur) noto‘g‘ri ma’lumot yuborishi mumkin.
Masalan:

* Bo‘sh `title` yuboradi.
* `title` matn emas, raqam yuboradi.
* Juda uzun yoki keraksiz qiymat yuboradi.

Agar biz tekshirmasak — ma’lumotlar buzilib ketadi yoki xato ishlaydi.

✅ **Validation** — foydalanuvchi yuborgan ma'lumotni tekshirish va noto'g'ri bo'lsa xatolik bilan javob berish.

### Validation Utility yaratamiz

Professional validation uchun utils faylini yaratamiz:

```javascript
// utils/validation.js
export const validateString = (value, fieldName = 'maydon') => {
  if (!value || typeof value !== 'string' || !value.trim()) {
    throw new Error(`${fieldName} matn bo'lishi kerak va bo'sh bo'lmasligini kerak`);
  }
  return value.trim();
};

export const validateNumber = (value, fieldName = 'maydon', min = 0) => {
  const num = Number(value);
  if (isNaN(num) || num < min) {
    throw new Error(`${fieldName} ${min} dan katta raqam bo'lishi kerak`);
  }
  return num;
};

export const validateBoolean = (value, fieldName = 'maydon') => {
  if (typeof value !== 'boolean') {
    throw new Error(`${fieldName} true/false qiymat bo'lishi kerak`);
  }
  return value;
};

export const validateOptionalString = (value, fieldName = 'maydon') => {
  if (value === undefined || value === null || value === '') {
    return null;
  }
  return validateString(value, fieldName);
};

export const validateOptionalNumber = (value, fieldName = 'maydon', min = 0) => {
  if (value === undefined || value === null || value === '') {
    return null;
  }
  return validateNumber(value, fieldName, min);
};
```

Bu utilitiesni server.js da import qilib ishlatamiz.

---

### 2️⃣ Avvalgi POST /todos (SQLite bilan)

Hozir bizning POST route shunday edi:

```javascript
app.post('/todos', (req, res) => {
  const { title } = req.body

  const info = db.prepare('INSERT INTO todos (title, completed) VALUES (?, ?)').run(title, false)
  const todo = db.prepare('SELECT * FROM todos WHERE id = ?').get(info.lastInsertRowid)

  res.status(201).json({ status: 'success', todo })
})
```

Bu yerda **title bo‘sh yoki noto‘g‘ri bo‘lsa ham** qo‘shib yuboradi.
Biz uni tekshirishimiz kerak.

---

### 3️⃣ Tekshirish (validation) qo‘shamiz

```javascript
app.post('/todos', (req, res) => {
  const { title } = req.body

  // ✅ Validation
  if (!title || typeof title !== 'string' || !title.trim()) {
    return res.status(400).json({
      status: 'error',
      message: 'Todo nomi kerak va bo‘sh bo‘lishi mumkin emas'
    })
  }

  const stmt = db.prepare('INSERT INTO todos (title, completed) VALUES (?, ?)')
  const info = stmt.run(title.trim(), false)
  const todo = db.prepare('SELECT * FROM todos WHERE id = ?').get(info.lastInsertRowid)

  res.status(201).json({ status: 'success', todo })
})
```

✅ Bu tekshiradi:

* `title` bor-yo‘qligini.
* `title` matn ekanligini.
* `title` bo‘sh bo‘lib qolmasligini (`title.trim()` bo‘sh bo‘lmasligi).

Agar xatolik bo‘lsa → `400 Bad Request` qaytaradi.

---

### 4️⃣ Thunder Client orqali sinov

#### A. To‘g‘ri ma’lumot yuborish

* Method: POST
* URL: `http://localhost:3000/todos`
* Body:

```json
{ "title": "Yangi vazifa" }
```

✅ Javob:

```json
{
  "status": "success",
  "todo": { "id": 1, "title": "Yangi vazifa", "completed": 0 }
}
```

#### B. Xato — bo‘sh body

* Body:

```json
{}
```

❌ Javob:

```json
{
  "status": "error",
  "message": "Todo nomi kerak va bo‘sh bo‘lishi mumkin emas"
}
```

Status code: **400 Bad Request**

#### C. Xato — bo‘sh string

```json
{ "title": "   " }
```

❌ Javob: xuddi yuqoridagi kabi 400 qaytaradi.

---

### 5️⃣ Yaxshi validation qilishning afzalligi

* API ni ishlatadigan har kim tushunarli xabar oladi.
* Ma’lumotlar bazasida keraksiz bo‘sh yozuvlar bo‘lmaydi.
* Ilova yanada mustahkam bo‘ladi.

---

### Mashq

1. `PATCH /todos/:id` route’da ham validation qo‘shing:

   * ID raqam bo‘lishi kerak.
   * Agar body bo‘sh yoki noto‘g‘ri bo‘lsa, `400` qaytarsin.

2. `DELETE /todos/:id` uchun ham noto‘g‘ri id yuborilganda `400` chiqsin.

---

### Asosiy tushunchalar

* **Validation** — foydalanuvchi yuborgan ma’lumotni tekshirish.
* **400 Bad Request** — noto‘g‘ri ma’lumot yuborilganda ishlatiladi.
* `!title || typeof title !== 'string' || !title.trim()` — `title` bo‘sh yoki matn emasligini tekshirish uchun yaxshi usul.

---
</details>

<hr>

<details>
    <summary>Global xatolarni ushlash — Error Handling Middleware (Express)</summary>
## 🗓️ 6-hafta — 3-dars

### 🏷️ Mavzu: **Global xatolarni ushlash — Error Handling Middleware (Express)**

---

### 1) Nima uchun “global error handler” kerak?

API’da xatolar bo‘lishi tabiiy: noto‘g‘ri `id`, bo‘sh `title`, DB ulanish xatosi va hokazo.
Har bir route ichida alohida `try/catch` yozib yurish o‘rniga **bitta global middleware** orqali hammasini markaziy tarzda boshqaramiz:

* Kod takrorlanmaydi.
* Bir xil formatda javob qaytaramiz (masalan: `{status, message}`).
* Loglash (konsolga yozish) va status kodlarini tartibga solish osonlashadi.

---

### 2) Express’da xatoni qanday “uzatamiz”?

* **Sync (oddiy) xatolar:** `throw new Error('xabar')` → Express avtomatik global handlerga uzatadi (agar mavjud bo‘lsa).
* **Async (Promise/await) xatolar:** `try { … } catch (err) { next(err) }`
* **Qo‘lda uzatish:** `next(err)` — ixtiyoriy xatoni keyingi “error middleware”ga yuboradi.

> **Esda tuting:** Error middleware signaturasi **4 ta argument** bilan bo‘ladi:
> `app.use((err, req, res, next) => { … })`

---

### 3) Boshlang‘ich loyiha (SQLite bilan) — qisqa tayyor holat

**server.js** (ESM: `package.json` ichida `"type":"module"` bor):

```javascript
import express from 'express'
import db from './db.js' // oldingi darslarda yozgan better-sqlite3 ulanishi

const app = express()
const PORT = 3000

app.use(express.json())

// --- ROUTES (namuna) --- //

// OK route (hammasi joyida)
app.get('/todos', (req, res, next) => {
  try {
    const todos = db.prepare('SELECT * FROM todos').all()
    return res.status(200).json(todos)
  } catch (err) {
    next(err) // DB xatosi bo‘lsa, global handlerga uzatamiz
  }
})

// Validation bilan POST
app.post('/todos', (req, res, next) => {
  try {
    const { title } = req.body
    if (!title || typeof title !== 'string' || !title.trim()) {
      const e = new Error('Todo nomi kerak va bo‘sh bo‘lishi mumkin emas')
      e.status = 400
      throw e
    }
    const info = db.prepare('INSERT INTO todos (title, completed) VALUES (?, ?)').run(title.trim(), 0)
    const todo = db.prepare('SELECT * FROM todos WHERE id = ?').get(info.lastInsertRowid)
    return res.status(201).json({ status: 'success', todo })
  } catch (err) {
    next(err)
  }
})

// Demonstratsiya uchun atayin xato
app.get('/boom', (req, res, next) => {
  const e = new Error('Atayin chiqarilgan xato')
  e.status = 500
  next(e)
})

// 404 — route topilmadi (har doim ROUTES dan keyin yoziladi)
app.use((req, res, next) => {
  return res.status(404).json({ status: 'error', message: 'Route topilmadi' })
})

// GLOBAL ERROR HANDLER — darsning markazi
app.use((err, req, res, next) => {
  // 1) Loglash (faqat dev/prodda boshqacha bo‘lishi mumkin)
  console.error('❌ ERROR:', err.message)
  if (err.stack) console.error(err.stack)

  // 2) Status kodni aniqlash
  const status = err.status && Number.isInteger(err.status) ? err.status : 500

  // 3) Yagona formatda javob
  return res.status(status).json({
    status: 'error',
    message: err.message || 'Ichki server xatosi'
  })
})

app.listen(PORT, () => {
  console.log(`✅ Server: http://localhost:${PORT}`)
})
```

**Nimalar bo‘ldi?**

* Har bir route ichida xato bo‘lsa `next(err)` orqali **global handler**ga yo‘naltiryapmiz.
* **404 middleware** — hech bir route mos kelmasa, shu yer ishlaydi.
* **Global error handler** — *oxirida* turadi va har qanday xatoni bir xilda javobga aylantiradi.

---

### 4) Async funksiyalar uchun qulay “wrapper”

Ko‘p `try/catch` yozmaslik uchun kichik “avtomatik tutuvchi” funksiya yozamiz:

```javascript
// utils/asyncWrap.js
export const asyncWrap = (fn) => {
  return (req, res, next) => {
    Promise.resolve(fn(req, res, next)).catch(next)
  }
}
```

Endi route’larni qisqartiramiz:

```javascript
import { asyncWrap } from './utils/asyncWrap.js'

// Misol: SELECT (agar kelajakda async bo‘lsa ham)
app.get('/todos', asyncWrap(async (req, res) => {
  const todos = db.prepare('SELECT * FROM todos').all()
  return res.status(200).json(todos)
}))

app.post('/todos', asyncWrap(async (req, res) => {
  const { title } = req.body
  if (!title || typeof title !== 'string' || !title.trim()) {
    const e = new Error('Todo nomi kerak va bo‘sh bo‘lishi mumkin emas')
    e.status = 400
    throw e
  }
  const info = db.prepare('INSERT INTO todos (title, completed) VALUES (?, ?)').run(title.trim(), 0)
  const todo = db.prepare('SELECT * FROM todos WHERE id = ?').get(info.lastInsertRowid)
  return res.status(201).json({ status: 'success', todo })
}))
```

**Foydasi:** route’lar ichida `try/catch` yozmaymiz; xato bo‘lsa avtomatik `next(err)` bo‘ladi.

---

### 5) “Operational” va “Programmer” xatolarini farqlash (qisqa)

* **Operational** (foydalanuvchi xatosi, DB ulanmadi, resurs topilmadi): kutiladigan va foydalanuvchiga **tushunarli** xabar bilan qaytariladigan xatolar. (Masalan, 400 / 404)
* **Programmer** (bug, undefined, noto‘g‘ri kod): dev/prodda loglab, foydalanuvchiga umumiy xabar beriladi (500).

Biz yuqorida `err.status` bo‘lsa shuni ishlatyapmiz (operational). Aks holda **500**.

---

### 6) Test ssenariylari (Thunder Client)

**A) 200 OK — hammasi yaxshi**

* Method: GET
* URL: `http://localhost:3000/todos`
* **Response:** `200 OK`, massiv qaytadi.

**B) 201 Created — to‘g‘ri POST**

* Method: POST
* URL: `http://localhost:3000/todos`
* Body (JSON):

  ```json
  { "title": "Dars tayyorlash" }
  ```
* **Response:** `201 Created`, `{ status: "success", todo: { ... } }`

**C) 400 Bad Request — validation xatosi**

* Method: POST
* URL: `http://localhost:3000/todos`
* Body:

  ```json
  { "title": "   " }
  ```
* **Response:** `400 Bad Request`, `{ status:"error", message:"Todo nomi kerak..." }`

**D) 404 Not Found — noto‘g‘ri route**

* Method: GET
* URL: `http://localhost:3000/no-such-path`
* **Response:** `404`, `{ status:"error", message:"Route topilmadi" }`

**E) 500 Internal Server Error — atayin xato**

* Method: GET
* URL: `http://localhost:3000/boom`
* **Response:** `500`, `{ status:"error", message:"Atayin chiqarilgan xato" }`
* Terminalda esa `❌ ERROR:` loglarini ko‘rasiz.

---

### 7) Javob formatini yagona qilish (ixtiyoriy, lekin foydali)

Yagona helper yozib, har doim bir xil strukturada javob qaytaramiz:

```javascript
// utils/send.js
export const ok = (res, data) => res.status(200).json({ status: 'success', data })
export const created = (res, data) => res.status(201).json({ status: 'success', data })
export const fail = (res, code, message) => res.status(code).json({ status: 'error', message })
```

Keyin route’larda:

```javascript
import { ok, created, fail } from './utils/send.js'

app.get('/todos', asyncWrap(async (req, res) => {
  const todos = db.prepare('SELECT * FROM todos').all()
  return ok(res, todos)
}))
```

---

### 8) Qisqa xulosa

* **Global error handler** (`app.use((err, req, res, next) => { … })`) — barcha xatolarni bitta joyda ushlab, bir xil ko‘rinishda qaytaradi.
* `next(err)` va/yoki `throw` → xatoni handlerga uzatadi.
* **404 middleware** — notog‘ri manzillarni aniq ushlab beradi.
* Thunder Client bilan 200/201/400/404/500 holatlarini alohida sinab chiqing.

---

### 🔧 Mini-faoliyat (Activity)

1. Kodingizga **global error handler** qo‘shing (yuqoridagi kabi).
2. `POST /todos` ga **validation xatosi** yuborib **400** qaytayotganini tekshiring.
3. `/boom` route bilan **500** xatoni ko‘ring.
4. Yaroqsiz manzilga kirib **404** xatoni ko‘ring.
5. Natijalarda status kodlar va JSON formatlari **bir xil** ekanini tasdiqlang.


</details>

<hr>

<details>
    <summary>Frontend bilan bog‘lanish — Fetch API asoslari</summary>
## 🗓️ 7-hafta — 1-dars

### 🏷️ Mavzu: **Frontend bilan bog‘lanish — Fetch API asoslari**

---

### 1️⃣ Fetch API nima?

Biz shu paytgacha API yaratdik, lekin uni foydalanuvchi (brauzer)dan qanday chaqiramiz?
Brauzerda **`fetch()`** degan funksiya bor. U serverga so‘rov yuborib, JSON yoki boshqa ma’lumotlarni olishga yordam beradi.

Oddiy tushuntirish:

* `fetch()` → brauzerning “hey server, menga shu ma’lumotni yubor” degan so‘rovi.
* Serverdan kelgan javobni `.json()` qilib o‘qib olamiz.
* So‘ng HTML sahifaga chiqaramiz.

---

### 2️⃣ Eng oddiy `fetch` misoli

```javascript
fetch('http://localhost:3000/todos')
  .then(response => response.json()) // serverdan JSON o‘qish
  .then(data => console.log(data))    // kelgan ma’lumotni ko‘rish
```

✅ Bu kod brauzer konsolida serverdan kelgan ma’lumotni chiqaradi.

---

### 3️⃣ Oddiy HTML sahifa yaratamiz

`index.html`:

```html
<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8" />
  <title>Todos Frontend</title>
  <style>
    body {
      font-family: sans-serif;
      background: #f7f7f7;
      padding: 20px;
    }
    h1 {
      color: #333;
    }
    ul {
      list-style: none;
      padding: 0;
    }
    li {
      background: white;
      margin: 5px 0;
      padding: 10px;
      border-radius: 6px;
    }
  </style>
</head>
<body>
  <h1>📋 Mening vazifalarim</h1>
  <ul id="todoList"></ul>

  <script>
    // Serverdan todos ma'lumotlarini olish
    fetch('http://localhost:3000/todos')
      .then(res => res.json())
      .then(todos => {
        const list = document.getElementById('todoList');
        todos.forEach(todo => {
          const li = document.createElement('li');
          li.textContent = `${todo.id}. ${todo.title} ${todo.completed ? '✅' : '❌'}`;
          list.appendChild(li);
        });
      })
      .catch(err => {
        console.error('Xatolik:', err);
      });
  </script>
</body>
</html>
```

✅ Qanday ishlaydi:

* Brauzer `http://localhost:3000/todos` ga GET so‘rov yuboradi.
* API JSON qaytaradi.
* JavaScript uni o‘qib, HTML sahifaga qo‘shadi.

---

### 4️⃣ Brauzer konsolini ko‘rib chiqish

1. Sahifani `Live Server` orqali oching.
2. `Ctrl+Shift+I` yoki `Cmd+Option+I` (Mac) → **Console** oynasiga kiring.
3. Serverdan kelgan ma’lumotlar `console.log(data)` orqali ko‘rinadi.
4. Sahifada esa vazifalar ro‘yxati chiqadi.

---

### 5️⃣ Mashq (Activity)

* **A)** API’da yangi todo qo‘shing (`POST /todos` bilan Thunder Client’dan yoki boshqa vositadan).
* **B)** Sahifani qayta yuklang — yangi qo‘shgan todo’lar ham ko‘rinsin.
* **C)** `fetch()` URL’ini xato yozib ko‘ring (`/todoss` bilan) — console’da xatolik chiqishini ko‘ring.

---

### 6️⃣ Qisqa tushunchalar

* `fetch(url)` → serverga so‘rov yuboradi.
* `.then(res => res.json())` → javobni JSON ga aylantiradi.
* DOM bilan ishlash orqali (JS yordamida `li`, `ul` yaratib) sahifaga ma’lumot chiqaramiz.
* Xatolik bo‘lsa `.catch()` orqali tutamiz.

---

✅ Endi siz **frontend va backendni bog‘ladingiz**: brauzer `fetch()` orqali Node.js API’dan ma’lumot olib sahifada ko‘rsatmoqda.
Keyingi darsda — **POST orqali yangi ma’lumot yuborish (yangi todo qo‘shish)**ni frontenddan o‘rganamiz.


</details>

<hr>

<details>
    <summary>Frontend’dan POST — Form orqali yangi Todo qo‘shish</summary>

## 🗓️ 7-hafta — 2-dars

### 🏷️ Mavzu: **Frontend’dan POST — Form orqali yangi Todo qo‘shish**

---

### 1️⃣ Brauzer orqali ma’lumot yuborish

Oldingi darsda biz faqat `GET` bilan ma’lumot olib kelgandik.
Endi foydalanuvchi **forma** orqali yangi vazifa kiritadi va biz uni **`fetch()` bilan POST** qilib serverga yuboramiz.

**Jarayon:**

1. HTML forma orqali foydalanuvchi vazifa nomini kiritadi.
2. JavaScript forma yuborilishini to‘xtatadi (page refresh bo‘lmasligi uchun).
3. `fetch()` yordamida `POST /todos` ga JSON yuboradi.
4. Server javob qaytaradi — biz yangi todo’ni ro‘yxatga qo‘shamiz.

---

### 2️⃣ HTML va JavaScript (to‘liq kod)

`index.html`:

```html
<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8" />
  <title>Todos Frontend</title>
  <style>
    body {
      font-family: sans-serif;
      background: #f7f7f7;
      padding: 20px;
    }
    h1 { color: #333; }
    ul {
      list-style: none;
      padding: 0;
    }
    li {
      background: white;
      margin: 5px 0;
      padding: 10px;
      border-radius: 6px;
    }
    form {
      display: flex;
      margin-bottom: 15px;
    }
    input {
      flex: 1;
      padding: 8px;
      font-size: 16px;
      border: 1px solid #ccc;
      border-radius: 6px 0 0 6px;
      outline: none;
    }
    button {
      padding: 8px 15px;
      font-size: 16px;
      border: none;
      background: #4caf50;
      color: white;
      border-radius: 0 6px 6px 0;
      cursor: pointer;
    }
    button:hover {
      background: #43a047;
    }
  </style>
</head>
<body>
  <h1>📋 Mening vazifalarim</h1>

  <!-- ✅ Yangi todo qo‘shish formasi -->
  <form id="todoForm">
    <input type="text" id="title" placeholder="Yangi vazifa yozing..." />
    <button type="submit">Qo‘shish</button>
  </form>

  <ul id="todoList"></ul>

  <script>
    const list = document.getElementById('todoList');
    const form = document.getElementById('todoForm');
    const input = document.getElementById('title');
    const API_URL = 'http://localhost:3000/todos';

    // Barcha todos’ni olish
    async function loadTodos() {
      list.innerHTML = ''; // eski ro‘yxatni tozalash
      const res = await fetch(API_URL);
      const todos = await res.json();
      todos.forEach(todo => {
        const li = document.createElement('li');
        li.textContent = `${todo.id}. ${todo.title} ${todo.completed ? '✅' : '❌'}`;
        list.appendChild(li);
      });
    }

    // Forma yuborilganda
    form.addEventListener('submit', async (e) => {
      e.preventDefault(); // sahifa qayta yuklanmasligi uchun
      const title = input.value.trim();

      if (!title) {
        alert('❗ Vazifa nomi bo‘sh bo‘lmasin');
        return;
      }

      // Serverga POST so‘rov yuborish
      const res = await fetch(API_URL, {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({ title })
      });

      if (!res.ok) {
        const err = await res.json();
        alert('Xato: ' + err.message);
        return;
      }

      const data = await res.json();
      console.log('Yangi todo:', data);

      input.value = ''; // inputni tozalash
      loadTodos();      // ro‘yxatni qayta yuklash
    });

    // Sahifa ochilganda todos’ni yuklash
    loadTodos();
  </script>
</body>
</html>
```

---

### 3️⃣ Qanday ishlaydi

* **Forma yuborilganda** — `submit` hodisasi tutib olinadi.
* `e.preventDefault()` sahifaning default refresh’ini bloklaydi.
* `fetch()` bilan `method: 'POST'` va `headers: { 'Content-Type': 'application/json' }` yuboriladi.
* Serverga `body` ichida JSON ko‘rinishida `{title: "..."} ` boradi.
* Javob kelgach, yangi todo’ni ko‘rsatish uchun `loadTodos()` qayta chaqiriladi.

---

### 4️⃣ Thunder Client bilan tekshirish (ixtiyoriy)

Xohlasangiz, POST’ni hali ham Thunder Client’da ham test qilishingiz mumkin, lekin bu kod orqali brauzer ham xuddi shunday ish qiladi.

---

### 5️⃣ Faoliyat (Activity)

1. Formaga yangi vazifa kiriting va **Qo‘shish** tugmasini bosing.
   → Yangi todo ro‘yxatga qo‘shilganini ko‘ring.

2. Serverni qayta yoqib ko‘ring, sahifani yangilang — vazifalar **qolganini** ko‘ring (chunki biz SQLite ishlatyapmiz).

3. Xato holatni sinang: inputni bo‘sh qoldirib yuboring → alert chiqadi va serverga yuborilmaydi.

---

### 6️⃣ Asosiy tushunchalar

* **POST so‘rov** → serverga ma’lumot yuborish uchun ishlatiladi.
* **`fetch(url, { method, headers, body })`** → ma’lumot yuborish usuli.
* `Content-Type: application/json` — serverga JSON yuborayotganimizni bildiradi.
* `preventDefault()` — formaning default refresh xatti-harakatini to‘xtatadi.
* API bilan ishlashda xatoliklarni `res.ok` orqali tekshirish foydali.

---

✅ Endi siz **frontenddan real API’ga ma’lumot yuborishni (POST)** o‘rgandingiz.
Keyingi darsda biz **PATCH va DELETE** so‘rovlarini ham frontenddan bajarib, ro‘yxatni jonli tahrirlaymiz.

</details>

<hr>

<details>
    <summary>Styling & UX — ro‘yxatni chiroyli qilish va delete tugmasi qo‘shish</summary>
## 🗓️ 7-hafta — 3-dars

### 🏷️ Mavzu: **Styling & UX — ro‘yxatni chiroyli qilish va delete tugmasi qo‘shish**

---

### 1️⃣ Maqsad

Biz endi **frontenddagi UX (User Experience)** ni yaxshilaymiz:

* Todos ro‘yxatini chiroyli dizayn bilan ko‘rsatamiz.
* Har bir todo yoniga **O‘chirish (Delete)** tugmasi qo‘shamiz.
* Tugma bosilganda serverga **DELETE** so‘rov yuborib, todo’ni olib tashlaymiz.

---

### 2️⃣ Yakuniy HTML & CSS (yangilangan)

`index.html` faylini yangilaymiz:

```html
<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8" />
  <title>Todos App</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background: #f5f5f5;
      max-width: 500px;
      margin: auto;
      padding: 20px;
    }

    h1 {
      color: #333;
      text-align: center;
    }

    form {
      display: flex;
      margin-bottom: 15px;
    }

    input {
      flex: 1;
      padding: 10px;
      font-size: 16px;
      border: 1px solid #ddd;
      border-radius: 6px 0 0 6px;
      outline: none;
    }

    button {
      padding: 10px 15px;
      font-size: 16px;
      border: none;
      background: #4caf50;
      color: white;
      border-radius: 0 6px 6px 0;
      cursor: pointer;
      transition: background 0.3s;
    }

    button:hover {
      background: #43a047;
    }

    ul {
      list-style: none;
      padding: 0;
    }

    li {
      display: flex;
      justify-content: space-between;
      align-items: center;
      background: white;
      margin-bottom: 8px;
      padding: 10px 15px;
      border-radius: 6px;
      box-shadow: 0 1px 3px rgba(0,0,0,0.1);
      transition: transform 0.2s;
    }

    li:hover {
      transform: scale(1.02);
    }

    .delete-btn {
      background: #e53935;
      color: white;
      border: none;
      padding: 5px 10px;
      border-radius: 4px;
      cursor: pointer;
      transition: background 0.3s;
    }

    .delete-btn:hover {
      background: #c62828;
    }

    .completed {
      text-decoration: line-through;
      color: #777;
    }
  </style>
</head>
<body>
  <h1>📋 Mening vazifalarim</h1>

  <!-- Forma -->
  <form id="todoForm">
    <input type="text" id="title" placeholder="Yangi vazifa yozing..." />
    <button type="submit">Qo‘shish</button>
  </form>

  <!-- Ro‘yxat -->
  <ul id="todoList"></ul>

  <script>
    const list = document.getElementById('todoList');
    const form = document.getElementById('todoForm');
    const input = document.getElementById('title');
    const API_URL = 'http://localhost:3000/todos';

    // Barcha todos’ni yuklash
    async function loadTodos() {
      list.innerHTML = '';
      const res = await fetch(API_URL);
      const todos = await res.json();

      todos.forEach(todo => {
        const li = document.createElement('li');
        li.innerHTML = `
          <span class="${todo.completed ? 'completed' : ''}">
            ${todo.id}. ${todo.title}
          </span>
          <button class="delete-btn" data-id="${todo.id}">❌</button>
        `;
        list.appendChild(li);
      });

      // Har bir delete tugmasiga hodisa ulash
      document.querySelectorAll('.delete-btn').forEach(btn => {
        btn.addEventListener('click', async (e) => {
          const id = e.target.dataset.id;
          await deleteTodo(id);
        });
      });
    }

    // Yangi todo qo‘shish
    form.addEventListener('submit', async (e) => {
      e.preventDefault();
      const title = input.value.trim();
      if (!title) return alert('❗ Vazifa nomi bo‘sh bo‘lmasin');

      const res = await fetch(API_URL, {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({ title })
      });

      if (!res.ok) {
        const err = await res.json();
        alert('Xato: ' + err.message);
        return;
      }

      input.value = '';
      loadTodos();
    });

    // DELETE so‘rov yuborish
    async function deleteTodo(id) {
      const res = await fetch(`${API_URL}/${id}`, { method: 'DELETE' });
      if (!res.ok) {
        const err = await res.json();
        alert('Xato: ' + err.message);
        return;
      }
      loadTodos();
    }

    // Sahifa yuklanganda todo’larni ko‘rsatish
    loadTodos();
  </script>
</body>
</html>
```

---

### 3️⃣ Qanday ishlaydi

* **CSS bilan yaxshiroq UX**

  * Hover effekti (li elementiga yaqinlashganda biroz kattalashadi).
  * Todo o‘chirilganida ro‘yxat avtomatik yangilanadi.
  * `completed` klassi orqali bajarilgan topshiriqlar ustiga chizib qo‘yish mumkin (keyin o‘rganamiz).

* **Delete tugmasi**

  * Har bir todo yonida `data-id` atributi bo‘lgan ❌ tugma chiqadi.
  * Tugma bosilganda `deleteTodo(id)` funksiyasi chaqirilib, serverga DELETE so‘rov yuboradi.
  * Ma’lumot o‘chirilgach, ro‘yxat yangilanadi (`loadTodos()`).

---

### 4️⃣ Test

1. Brauzerni oching → eski todos ro‘yxati chiqadi.
2. Yangi vazifa qo‘shing → ro‘yxatga qo‘shiladi.
3. ❌ tugmasini bosing → todo o‘chadi va ro‘yxat yangilanadi.
4. Serverni qayta ishga tushiring va sahifani yangilang → hammasi SQLite’da saqlangan.

---

### 5️⃣ Faoliyat (Activity)

* Ro‘yxatdagi har bir element yonidagi ❌ tugmasini bosib **DELETE** so‘rovini tekshiring.
* UX ni yaxshilash uchun ranglar va animatsiyalar bilan o‘zingiz o‘zgartirib ko‘ring.
* Yangi qo‘shilgan vazifani darhol yuqoriga yoki pastga qo‘shish uchun kodni sozlab ko‘ring.

---

### Asosiy tushunchalar

* **UX (User Experience)** — foydalanuvchiga qulay ko‘rinish va ishlash tajribasini yaratish.
* **DELETE so‘rov** — ma’lumotni o‘chirish uchun ishlatiladi.
* DOM orqali tugmalarni dinamik yaratib, hodisa ulash mumkin (`data-id` orqali ID olish qulay).
* Frontend bilan API’ni integratsiya qilishni davom ettirdik: GET + POST + DELETE.

---

✅ Endi sizning Todos frontend ilovangiz **to‘liq ishlaydigan CRUD (GET, POST, DELETE)** funksiyalariga ega bo‘ldi va foydalanuvchi uchun qulay ko‘rinishga ega.
Keyingi bosqich — **PATCH orqali vazifalarni bajarilgan/bajarilmagan qilib belgilash va UX ni yanada yaxshilash** bo‘ladi.


</details>

<hr>

<details>
    <summary>Final loyiha rejalash — API tanlash, maydonlar va CRUD marshrutlar</summary>
## 🗓️ 8-hafta — 1-dars

### 🏷️ Mavzu: **Final loyiha rejalash — API tanlash, maydonlar va CRUD marshrutlar**

---

Quyida final loyiha uchun 3 variant beriladi. Ulardan bittasini tanlaysiz va aynan shu darsda **ma’lumotlar tuzilmasi (fields)**, **SQL jadval(lar)**, hamda **CRUD marshrutlar**ni (routes) aniq rejalashtirasiz. Keyingi darslarda aynan shu reja bo‘yicha kod yozasiz.

---

## 0) Rejalash bosqichlari (hamma loyihaga bir xil)

1. **Resursni tanlash** (masalan, “books”, “products”, “notes”).
2. **Maydonlarni aniqlash** (har bir ustun nomi va turi).
3. **SQLite jadval(lar) CREATE** so‘rovini yozish.
4. **CRUD routes** ro‘yxatini tuzish.
5. **Status kodlar** va **validatsiya** qoidalarini yozib qo‘yish.
6. **Namuna JSON** va test ssenariylari tayyorlash.

---

## Variant A — Book Library (Kitoblar kutubxonasi)

### 1) Maydonlar (fields)

| Ustun     | Turi    | Izoh                       |
| --------- | ------- | -------------------------- |
| id        | INTEGER | PRIMARY KEY AUTOINCREMENT  |
| title     | TEXT    | Majburiy                   |
| author    | TEXT    | Majburiy                   |
| year      | INTEGER | Ixtiyoriy (masalan 1998)   |
| pages     | INTEGER | Ixtiyoriy (sahifalar soni) |
| available | BOOLEAN | Majburiy (default: 1=true) |

### 2) SQLite jadvali

```sql
CREATE TABLE IF NOT EXISTS books (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  title TEXT NOT NULL,
  author TEXT NOT NULL,
  year INTEGER,
  pages INTEGER,
  available BOOLEAN DEFAULT 1
);
```

### 3) CRUD marshrutlar

* **GET `/books`** — barcha kitoblar (query bilan filtrlash ixtiyoriy: `?author=...`, `?q=...` qidiruv).
* **GET `/books/:id`** — bitta kitobni olish.
* **POST `/books`** — yangi kitob qo‘shish.
* **PUT `/books/:id`** — to‘liq yangilash (title, author, available… hammasi majburiy).
* **PATCH `/books/:id`** — qisman yangilash (faqat 1–2 maydon).
* **DELETE `/books/:id`** — o‘chirish.

### 4) Validatsiya

* `title` — **string & bo‘sh bo‘lmasin**.
* `author` — **string & bo‘sh bo‘lmasin**.
* `year` — agar kelsa, **raqam** bo‘lsin (masalan, 0 < year ≤ 2100).
* `pages` — agar kelsa, **raqam** bo‘lsin (0 < pages ≤ 10000).
* `available` — `true/false` (SQLite’da 1/0 sifatida saqlanadi).

### 5) Status kodlar

* `GET` muvaffaqiyat: **200**
* `POST` yaratildi: **201**
* Validatsiya xatosi: **400**
* Topilmadi: **404**

### 6) Namuna JSON

**POST `/books` (Body):**

```json
{
  "title": "Ufq",
  "author": "Odil Yoqubov",
  "year": 1974,
  "pages": 320,
  "available": true
}
```

**GET `/books` (Response):**

```json
[
  { "id": 1, "title": "Ufq", "author": "Odil Yoqubov", "year": 1974, "pages": 320, "available": 1 },
  { "id": 2, "title": "Alpomish", "author": "Xalq og'zaki ijodi", "year": null, "pages": null, "available": 1 }
]
```

**PATCH `/books/1` (Body — qisman):**

```json
{ "available": false }
```

---

## Variant B — Mini Shop (Mahsulotlar ro‘yxati)

### 1) Maydonlar

| Ustun    | Turi    | Izoh                               |
| -------- | ------- | ---------------------------------- |
| id       | INTEGER | PRIMARY KEY AUTOINCREMENT          |
| name     | TEXT    | Majburiy                           |
| price    | REAL    | Majburiy (≥ 0)                     |
| stock    | INTEGER | Majburiy (≥ 0)                     |
| category | TEXT    | Ixtiyoriy (masalan, “electronics”) |
| active   | BOOLEAN | Majburiy (default: 1=true)         |

### 2) SQLite jadvali

```sql
CREATE TABLE IF NOT EXISTS products (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  name TEXT NOT NULL,
  price REAL NOT NULL,
  stock INTEGER NOT NULL,
  category TEXT,
  active BOOLEAN DEFAULT 1
);
```

### 3) CRUD marshrutlar

* **GET `/products`** — barcha mahsulotlar (`?category=...`, `?q=...`, `?minPrice=...&maxPrice=...` ixtiyoriy).
* **GET `/products/:id`** — bitta mahsulot.
* **POST `/products`** — yangi mahsulot.
* **PUT `/products/:id`** — to‘liq yangilash.
* **PATCH `/products/:id`** — qisman yangilash (masalan, `stock`ni kamaytirish/oshirish).
* **DELETE `/products/:id`** — o‘chirish.

### 4) Validatsiya

* `name` — bo‘sh bo‘lmasin.
* `price` — **number**, `>= 0`.
* `stock` — **integer**, `>= 0`.
* `active` — `true/false`.

### 5) Namuna JSON

**POST `/products` (Body):**

```json
{
  "name": "Quloqchin",
  "price": 149000,
  "stock": 12,
  "category": "electronics",
  "active": true
}
```

**PATCH `/products/1` (Body — qisman):**

```json
{ "stock": 9 }
```

---

## Variant C — Notes (Qaydlar)

### 1) Maydonlar

| Ustun      | Turi    | Izoh                                         |
| ---------- | ------- | -------------------------------------------- |
| id         | INTEGER | PRIMARY KEY AUTOINCREMENT                    |
| title      | TEXT    | Majburiy                                     |
| content    | TEXT    | Majburiy                                     |
| created_at | TEXT    | ISO string (masalan, `2025-10-03T10:00:00Z`) |
| updated_at | TEXT    | Ixtiyoriy (yangilanganda yoziladi)           |

### 2) SQLite jadvali

```sql
CREATE TABLE IF NOT EXISTS notes (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  title TEXT NOT NULL,
  content TEXT NOT NULL,
  created_at TEXT NOT NULL,
  updated_at TEXT
);
```

> `created_at` va `updated_at` maydonlarini Node’dan `new Date().toISOString()` bilan to‘ldirasiz.

### 3) CRUD marshrutlar

* **GET `/notes`** — barcha qaydlar (`?q=` bilan sarlavha/mazmunga qidiruv ixtiyoriy).
* **GET `/notes/:id`** — bitta qayd.
* **POST `/notes`** — yangi qayd (title, content, created_at).
* **PUT `/notes/:id`** — to‘liq yangilash (title, content, updated_at).
* **PATCH `/notes/:id`** — qisman yangilash (masalan, faqat `content`).
* **DELETE `/notes/:id`** — o‘chirish.

### 4) Validatsiya

* `title` — matn, bo‘sh bo‘lmasin.
* `content` — matn, bo‘sh bo‘lmasin.
* `created_at` — ISO vaqt satri.
* `updated_at` — yangilanganda to‘ldiriladi.

### 5) Namuna JSON

**POST `/notes` (Body):**

```json
{
  "title": "Dars reja",
  "content": "Bugun fetch() va POST’ni ko‘rdik",
  "created_at": "2025-10-03T09:00:00.000Z"
}
```

**PATCH `/notes/1` (Body — qisman):**

```json
{ "content": "Fetch, POST va DELETE ham qo‘shildi", "updated_at": "2025-10-03T10:30:00.000Z" }
```

---

## Tanlangan loyiha uchun yozib qo‘yiladigan “API rejasi” shabloni

Quyidagi bo‘sh shablonni ko‘chirib, o‘zingiz tanlagan loyiha nomini qo‘yib to‘ldiring:

**Loyiha nomi:** (Book Library / Mini Shop / Notes / boshqasi)
**Asosiy jadval(lar):** (masalan, `books`)

**Fields (ustunlar):**

* `id` — INTEGER, PRIMARY KEY AUTOINCREMENT
* `...` — ...

**SQLite CREATE TABLE:**

```sql
CREATE TABLE IF NOT EXISTS ... (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  ...
);
```

**CRUD routes:**

* GET `/...` — (izoh)
* GET `/.../:id` — (izoh)
* POST `/...` — (izoh)
* PUT `/.../:id` — (izoh)
* PATCH `/.../:id` — (izoh)
* DELETE `/.../:id` — (izoh)

**Validatsiya:**

* (majburiy maydonlar, turlari, chegaralar)

**Status kodlar:**

* 200 OK, 201 Created, 400 Bad Request, 404 Not Found (zarur bo‘lsa 500)

**Namuna JSON (POST):**

```json
{ ... }
```

**Test ssenariylari (Thunder Client):**

1. POST → 201
2. GET → 200
3. GET /:id (topilgan) → 200
4. GET /:id (topilmagan) → 404
5. PUT/PATCH (to‘g‘ri) → 200
6. DELETE → 200

---

## Faoliyat (Activity)

1. **Variant tanlang** (Books / Products / Notes).
2. Jadval(lar) uchun **`CREATE TABLE`** SQL’ingizni yozing.
3. **CRUD marshrutlar** ro‘yxatini to‘liq yozing.
4. **Validatsiya** shartlaringizni ro‘yxat qilib qo‘ying.
5. **POST uchun namuna JSON** va **Thunder Client test ssenariylari**ni tayyorlang.
6. “`todos.db`” yoniga, tanlagan loyihangiz uchun masalan **`library.db`**, **`shop.db`**, yoki **`notes.db`** fayl nomini rejalashtiring (keyingi darsda ishlatamiz).

---

</details>

<hr>

<details>
    <summary>API qurish va Frontendga ulash (Book Library misolida)</summary>
## 🗓️ 8-hafta — 2-dars

### 🏷️ Mavzu: **API qurish va Frontendga ulash (Book Library misolida)**

---

Quyida bitta to‘liq kichik loyiha: **Book Library**.
Ma’lumotlar bazasi: **SQLite** (`better-sqlite3`), server: **Express**, frontend: oddiy **HTML + fetch()**.

---

## 1) Loyihani tayyorlash

```bash
mkdir book-library && cd book-library
npm init -y
npm install express better-sqlite3
```

`package.json` ichiga ESM uchun qo‘shing:

```json
{
  "name": "book-library",
  "version": "1.0.0",
  "type": "module",
  "description": "Book Library API with SQLite",
  "main": "server.js",
  "scripts": {
    "start": "node server.js",
    "dev": "nodemon server.js",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": ["backend", "api", "sqlite"],
  "author": "Sizning ismingiz",
  "license": "MIT",
  "dependencies": {
    "express": "^4.18.2",
    "better-sqlite3": "^8.7.0"
  },
  "devDependencies": {
    "nodemon": "^3.0.1"
  }
}
```

---

## Environment Configuration (.env fayli)

Professional loyihalar uchun environment variables ishlatamiz:

1. `.env` fayl yarating:
```bash
# Database
DB_FILE=library.db

# Server
PORT=3000
NODE_ENV=development

# API
API_VERSION=v1
```

2. `dotenv` paketini o'rnating:
```bash
npm install dotenv
```

3. `server.js` ning boshida yozamiz:
```javascript
import 'dotenv/config';

const config = {
  port: process.env.PORT || 3000,
  env: process.env.NODE_ENV || 'development',
  dbFile: process.env.DB_FILE || 'library.db',
  apiVersion: process.env.API_VERSION || 'v1'
};
```

4. `package.json` ga `.env` qo'shing:
```json
{
  "scripts": {
    "start": "node server.js",
    "dev": "nodemon server.js"
  }
}
```

---

## 2) Ma'lumotlar bazasi — `db.js`

```javascript
// db.js
import Database from 'better-sqlite3';

const db = new Database('library.db'); // fayl yaratiladi (bor bo'lmasa)

db.prepare(`
  CREATE TABLE IF NOT EXISTS books (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    title TEXT NOT NULL,
    author TEXT NOT NULL,
    year INTEGER,
    pages INTEGER,
    available BOOLEAN DEFAULT 1
  )
`).run();

export default db;
```

**Jadval maydonlari:**

* `id` — unikal (AUTOINCREMENT)
* `title`, `author` — majburiy
* `year`, `pages` — ixtiyoriy (raqam)
* `available` — `true/false` (SQLite ichida 1/0)

---

## 3) API — `server.js`

```javascript
// server.js
import express from 'express';
import db from './db.js';

const app = express();
const PORT = 3000;

app.use(express.json({ limit: '10mb' })); // JSON body size limit
app.use(express.urlencoded({ extended: true, limit: '10mb' })); // Form data support

// Security headers
app.use((req, res, next) => {
  res.setHeader('X-Content-Type-Options', 'nosniff');
  res.setHeader('X-Frame-Options', 'DENY');
  res.setHeader('X-XSS-Protection', '1; mode=block');
  next();
});

// statik fayllar (index.html) uchun:
app.use(express.static('.')); // shu papkadan xizmat qiladi

// ----------- VALIDATION & SECURITY ----------- //
const sanitizeInput = (input) => {
  if (typeof input === 'string') {
    return input
      .trim()
      .replace(/[<>]/g, '') // Remove HTML tags
      .replace(/[\"']/g, '') // Remove quotes
      .substring(0, 1000); // Limit length
  }
  return input;
};

const isNonEmptyString = (v) => typeof v === 'string' && sanitizeInput(v).length > 0;
const isOptionalInt = (v) => v === undefined || v === null || Number.isInteger(Number(v));
const toBool = (v) => (v === true || v === 1 || v === '1');

// ----------- ENDPOINTS ----------- //

// GET /books — hammasi
app.get('/books', (req, res) => {
  const rows = db.prepare('SELECT * FROM books').all();
  res.status(200).json(rows);
});

// GET /books/:id — bitta
app.get('/books/:id', (req, res) => {
  const id = Number(req.params.id);
  if (Number.isNaN(id)) return res.status(400).json({ status: 'error', message: 'Noto‘g‘ri ID' });

  const row = db.prepare('SELECT * FROM books WHERE id = ?').get(id);
  if (!row) return res.status(404).json({ status: 'error', message: 'Kitob topilmadi' });

  res.status(200).json(row);
});

// POST /books — yaratish
app.post('/books', (req, res) => {
  const { title, author, year, pages, available } = req.body;

  // tekshiruv
  if (!isNonEmptyString(title) || !isNonEmptyString(author)) {
    return res.status(400).json({ status: 'error', message: 'title va author majburiy' });
  }
  if (!isOptionalInt(year) || !isOptionalInt(pages)) {
    return res.status(400).json({ status: 'error', message: 'year/pages raqam bo‘lishi kerak (yoki yubormang)' });
  }

  const stmt = db.prepare('INSERT INTO books (title, author, year, pages, available) VALUES (?, ?, ?, ?, ?)');
  const info = stmt.run(sanitizeInput(title), sanitizeInput(author),
    year !== undefined && year !== null && year !== '' ? Number(year) : null,
    pages !== undefined && pages !== null && pages !== '' ? Number(pages) : null,
    available !== undefined ? (toBool(available) ? 1 : 0) : 1
  );

  const created = db.prepare('SELECT * FROM books WHERE id = ?').get(info.lastInsertRowid);
  res.status(201).json({ status: 'success', book: created });
});

// PATCH /books/:id/available — mavjudligini almashtirish (toggle)
app.patch('/books/:id/available', (req, res) => {
  const id = Number(req.params.id);
  if (Number.isNaN(id)) return res.status(400).json({ status: 'error', message: 'Noto‘g‘ri ID' });

  const book = db.prepare('SELECT * FROM books WHERE id = ?').get(id);
  if (!book) return res.status(404).json({ status: 'error', message: 'Kitob topilmadi' });

  const newVal = book.available ? 0 : 1;
  db.prepare('UPDATE books SET available = ? WHERE id = ?').run(newVal, id);

  const refreshed = db.prepare('SELECT * FROM books WHERE id = ?').get(id);
  res.status(200).json({ status: 'success', book: refreshed });
});

// DELETE /books/:id — o‘chirish
app.delete('/books/:id', (req, res) => {
  const id = Number(req.params.id);
  if (Number.isNaN(id)) return res.status(400).json({ status: 'error', message: 'Noto‘g‘ri ID' });

  const exists = db.prepare('SELECT 1 FROM books WHERE id = ?').get(id);
  if (!exists) return res.status(404).json({ status: 'error', message: 'Kitob topilmadi' });

  db.prepare('DELETE FROM books WHERE id = ?').run(id);
  res.status(200).json({ status: 'success', message: 'O‘chirildi' });
});

app.listen(PORT, () => {
  console.log(`✅ Server: http://localhost:${PORT}`);
});
```

**Mazmuni:**

* **GET /books** — ro‘yxat
* **GET /books/:id** — bitta yozuv
* **POST /books** — qo‘shish (validation bilan)
* **PATCH /books/:id/available** — `available` ni teskari qilish
* **DELETE /books/:id** — o‘chirish
* `express.static('.')` — bir papkadagi `index.html` ning to‘g‘ridan-to‘g‘ri ochilishi

---

## 4) Oddiy Frontend — `index.html`

```html
<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8" />
  <title>Book Library</title>
  <style>
    body { font-family: system-ui, sans-serif; background:#f6f7fb; max-width: 720px; margin: 0 auto; padding: 24px; }
    h1 { text-align:center; color:#333; }
    form { display:grid; grid-template-columns: 1fr 1fr; gap:12px; background:#fff; padding:16px; border-radius:12px; box-shadow:0 2px 8px rgba(0,0,0,.06); margin-bottom:16px; }
    form input, form button, form select { padding:10px; font-size:16px; border:1px solid #ddd; border-radius:8px; }
    form button { background:#4caf50; color:#fff; border:none; cursor:pointer; }
    form button:hover { background:#43a047; }
    .full { grid-column: 1 / -1; }
    ul { list-style:none; padding:0; display:grid; gap:10px; }
    li { background:#fff; border-radius:10px; padding:12px 14px; display:flex; justify-content:space-between; align-items:center; box-shadow:0 1px 6px rgba(0,0,0,.05); }
    .meta { color:#666; font-size:14px; }
    .tag { font-size:12px; padding:3px 8px; border-radius:999px; background:#e8f5e9; color:#256029; margin-left:8px; }
    .tag.red { background:#ffebee; color:#b71c1c; }
    .row { display:flex; align-items:center; gap:8px; }
    .btn { border:none; padding:6px 10px; border-radius:8px; cursor:pointer; }
    .btn.toggle { background:#1976d2; color:#fff; }
    .btn.delete { background:#e53935; color:#fff; }
  </style>
</head>
<body>
  <h1>📚 Book Library</h1>

  <form id="bookForm">
    <input type="text" id="title" placeholder="Sarlavha (majburiy)" required />
    <input type="text" id="author" placeholder="Muallif (majburiy)" required />
    <input type="number" id="year" placeholder="Yil (ixtiyoriy)" />
    <input type="number" id="pages" placeholder="Sahifa (ixtiyoriy)" />
    <select id="available">
      <option value="1" selected>Mavjud</option>
      <option value="0">Mavjud emas</option>
    </select>
    <button type="submit">Qo‘shish</button>
  </form>

  <ul id="list"></ul>

  <script>
    const API = '/books';
    const form = document.getElementById('bookForm');
    const list = document.getElementById('list');

    async function loadBooks() {
      list.innerHTML = '';
      const res = await fetch(API);
      const books = await res.json();

      books.forEach(b => {
        const li = document.createElement('li');

        const left = document.createElement('div');
        const title = document.createElement('div');
        title.textContent = `${b.id}. ${b.title} — ${b.author}`;
        const meta = document.createElement('div');
        meta.className = 'meta';
        meta.textContent = `Yil: ${b.year ?? '—'} | Sahifa: ${b.pages ?? '—'}`;

        const tags = document.createElement('span');
        tags.className = 'tag ' + (b.available ? '' : 'red');
        tags.textContent = b.available ? 'Mavjud' : 'Mavjud emas';

        left.appendChild(title);
        const row = document.createElement('div');
        row.className = 'row';
        row.appendChild(meta);
        row.appendChild(tags);
        left.appendChild(row);

        const right = document.createElement('div');
        const toggleBtn = document.createElement('button');
        toggleBtn.className = 'btn toggle';
        toggleBtn.textContent = 'Available ↔';
        toggleBtn.onclick = async () => {
          await fetch(`${API}/${b.id}/available`, { method: 'PATCH' });
          await loadBooks();
        };

        const delBtn = document.createElement('button');
        delBtn.className = 'btn delete';
        delBtn.textContent = 'Delete';
        delBtn.onclick = async () => {
          const res = await fetch(`${API}/${b.id}`, { method: 'DELETE' });
          if (!res.ok) {
            const err = await res.json().catch(() => ({}));
            alert('Xato: ' + (err.message || res.statusText));
            return;
          }
          await loadBooks();
        };

        right.appendChild(toggleBtn);
        right.appendChild(delBtn);

        li.appendChild(left);
        li.appendChild(right);
        list.appendChild(li);
      });
    }

    form.addEventListener('submit', async (e) => {
      e.preventDefault();
      const payload = {
        title: document.getElementById('title').value.trim(),
        author: document.getElementById('author').value.trim(),
        year: document.getElementById('year').value ? Number(document.getElementById('year').value) : undefined,
        pages: document.getElementById('pages').value ? Number(document.getElementById('pages').value) : undefined,
        available: document.getElementById('available').value === '1'
      };

      if (!payload.title || !payload.author) {
        alert('title va author majburiy');
        return;
      }

      const res = await fetch(API, {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify(payload)
      });

      if (!res.ok) {
        const err = await res.json().catch(() => ({}));
        alert('Xato: ' + (err.message || res.statusText));
        return;
      }

      // formani tozalash
      e.target.reset();
      document.getElementById('available').value = '1';

      await loadBooks();
    });

    loadBooks();
  </script>
</body>
</html>
```

**Nimalar bor:**

* Forma: `title`, `author` (majburiy), `year`, `pages`, `available`.
* Ro‘yxat: barcha kitoblar, har birida **Available ↔** (PATCH) va **Delete** (DELETE) tugmalari.
* `express.static('.')` tufayli `index.html` ni bevosita `http://localhost:3000/index.html` dan ochasiz.

---

## 5) Ishga tushirish va tekshirish

```bash
npm start
```

Brauzerda:

* `http://localhost:3000/index.html` → ro‘yxat ko‘rinadi.
* Forma orqali kitob qo‘shing → ro‘yxatga darhol qo‘shiladi.
* Serverni to‘xtatib/yoqing → ma’lumot **library.db** ichida saqlanadi (yo‘qolmaydi).
* VS Code SQLite extension yoki `sqlite3 library.db` bilan jadvalni ko‘rib chiqing:

  ```sql
  SELECT * FROM books;
  ```

---

## Yakun

* **DB jadval** yaratildi (`db.js`).
* **Endpointlar** to‘liq ishlayapti (GET/GET:id/POST/PATCH available/DELETE).
* **Oddiy HTML sahifa** API bilan bog‘landi (fetch GET/POST/PATCH/DELETE).


</details>

<hr>

<details>
    <summary>Taqdimot va Demo (Presentation & Demo)</summary>
## 🗓️ 8-hafta — 3-dars

### 🏷️ Mavzu: **Taqdimot va Demo (Presentation & Demo)**

---

### 1) Taqdimotga tayyorgarlik (check-list)

**Kod**

* `server.js` ishlaydi (`npm start`).
* `db.js` (yoki `todos.db` / `library.db`) mavjud.
* Frontend fayl: `index.html` mavjud va `express.static('.')` orqali ochiladi.

**Test vositalari**

* Thunder Client (yoki Postman) ochiq.
* Brauzer oynasi ochiq (`http://localhost:3000/index.html`).

**Ma’lumotlar**

* Bazada kamida 2–3 ta yozuv bor (yo‘q bo‘lsa, darsdan oldin qo‘shib oling).
* Qancha endpoint borligi va ularning maqsadi yozib qo‘yilgan.

---

### 2) Taqdimot tarkibi (skript)

1. **Loyiha nomi va qisqa maqsadi**

   * “Loyihamiz — *Book Library* (yoki *Todos*, *Notes*). API qurildi, frontend `fetch()` bilan bog‘langan.”

2. **Arxitektura**

   * “Backend: Node.js + Express. Ma’lumotlar bazasi: SQLite (`better-sqlite3`). Frontend: HTML + JS (fetch).”

3. **Jadval maydonlari**

   * `books(id, title, author, year, pages, available)` — majburiy va ixtiyoriy maydonlar qisqacha.

4. **Endpointlar ro‘yxati (CRUD)**

   * GET `/books`, GET `/books/:id`, POST `/books`, PATCH `/books/:id/available`, DELETE `/books/:id`.

5. **Status kodlar va validatsiya**

   * `201 Created` — POST’da.
   * `400 Bad Request` — bo‘sh yoki noto‘g‘ri `title/author`.
   * `404 Not Found` — yo‘q `id`.
   * `200 OK` — muvaffaqiyatli o‘qish/yangilash/o‘chirish.

6. **Jonli demo**

   * Thunder Client’da API so‘rovlarini ko‘rsatish.
   * Brauzerda `index.html` orqali ro‘yxatni ko‘rsatish va forma bilan yozuv qo‘shish.
   * `available` ni almashtirish va o‘chirish tugmalarini ishga solish.

7. **DB isboti**

   * Serverni to‘xtatib/yoqib, ma’lumotlar saqlanib qolganini ko‘rsatish.
   * VS Code SQLite extension’da jadvalni ochib, `SELECT * FROM ...;` bilan tekshirish.

8. **Xulosa**

   * “Backend qanday ishlaydi, frontend qanday ulanish qiladi, status kodlar va validatsiyaning roli.”

---

### 3) Thunder Client ssenariylari (ko‘rsatma)

**A) GET — ro‘yxat**

* Method: GET, URL: `http://localhost:3000/books`
* Kutilgan: `200 OK`, array.

**B) POST — yangi yozuv**

* Method: POST, URL: `http://localhost:3000/books`
* Body (JSON):

```json
{
  "title": "Ufq",
  "author": "Odil Yoqubov",
  "year": 1974,
  "pages": 320,
  "available": true
}
```

* Kutilgan: `201 Created`, `book` obyekt.

**C) GET /:id — bitta yozuv**

* Method: GET, URL: `http://localhost:3000/books/1`
* Kutilgan: `200 OK`, bitta obyekt.

**D) PATCH — available ni almashtirish**

* Method: PATCH, URL: `http://localhost:3000/books/1/available`
* Kutilgan: `200 OK`, `available` teskari qiymatga o‘tadi (1↔0).

**E) DELETE — o‘chirish**

* Method: DELETE, URL: `http://localhost:3000/books/1`
* Kutilgan: `200 OK`, “O‘chirildi”.

**Xatolik namoyishi (ixtiyoriy):**

* POST’da bo‘sh `title` yuborish → `400 Bad Request`.
* GET `/books/9999` → `404 Not Found`.

---

### 4) Frontend demo (brauzer)

1. `http://localhost:3000/index.html` sahifasini oching.
2. Ro‘yxat avtomatik chiqadi (`loadBooks()` GET qiladi).
3. Formaga kitob qo‘shing → POST → ro‘yxat yangilanadi.
4. “Available ↔” tugmasini bosing → PATCH → badge rangi o‘zgaradi.
5. “Delete” tugmasini bosing → DELETE → ro‘yxatdan o‘chadi.
6. **Restart isboti:** `CTRL+C` bilan serverni to‘xtatib, `npm start` bilan yoqing, sahifani yangilang — ma’lumotlar saqlangan (SQLite faylda).

---

### 5) DB inspeksiyasi (qo‘lda tekshirish)

**VS Code extension**

* `library.db` faylini oching.
* `books` jadvalini tanlab, yozuvlarni ko‘ring.

**Terminal (ixtiyoriy):**

```bash
sqlite3 library.db
sqlite> SELECT * FROM books;
```

---

### 6) Namoyish matni (qisqa skript)

* “Hozir GET /books yuboraman — mana ro‘yxat.”
* “POST bilan yangi kitob qo‘shaman — 201 Created, qaytgan obyekt bu.”
* “Endi brauzerda ro‘yxatni ko‘rasiz — yangi kitob darhol paydo bo‘ldi.”
* “Available tugmasini bosaman — serverga PATCH ketdi, badge o‘zgardi.”
* “Delete bosaman — DELETE ketdi, ro‘yxatdan yo‘qoldi.”
* “Serverni to‘xtatib/yoqaman — ma’lumotlar saqlangan, chunki SQLite faylga yozildi.”
* “Oxirida DB faylini ochib, `SELECT *` bilan ko‘rsataman.”

---

### 7) Muammolarni tez yechish (troubleshooting)

* **CORS/xato fetch**: Frontendni ham shu portdan (`express.static('.')`) xizmat qildiring. URL'ni to'g'ri yozing (`/books`). 

**CORS qanday ishlaydi:**
Brauzerning xavfsizlik mexanizmi. Frontend boshqa portda ishlaganda CORS ko'rsatma kerak:

```javascript
// CORS middleware (server.js ning boshida qo'shing)
app.use((req, res, next) => {
  res.header('Access-Control-Allow-Origin', '*');
  res.header('Access-Control-Allow-Methods', 'GET, POST, PUT, DELETE, OPTIONS');
  res.header('Access-Control-Allow-Headers', 'Content-Type');
  
  if (req.method === 'OPTIONS') {
    res.sendStatus(200);
  } else {
    next();
  }
});
```
* **`Cannot GET /index.html`**: `app.use(express.static('.'))` yozilganini tekshiring.
* **DB bo‘sh**: POST yuborganmisiz? Yoki `library.db` boshqa papkadami?
* **`400 Bad Request`**: title/author bo‘sh — validatsiyaga rioya qiling.
* **`404 Not Found`**: noto‘g‘ri `id` — mavjud yozuvni tanlang.

---

### 8) Baholash mezonlari (o‘quvchilarga ko‘rinadigan)

* API ishlaydimi (GET/POST/PATCH/DELETE)?
* Validatsiya bormi (`400` holatlarda)?
* Frontend `fetch()` bilan to‘g‘ri ulanadimi?
* Restartdan keyin ma’lumot saqlanadimi (SQLite)?
* Taqdimotda tushunarli izoh va toza demo bormi?

---

### 9) Yakun va topshiriq

* Har bir guruh o‘z loyihasini 5–7 daqiqa ichida ko‘rsatadi (API so‘rovlar + sahifa).
* Kodni GitHub’ga joylab, `README.md` ga **Endpointlar, o‘rnatish bo‘yicha buyruqlar** va **screenshotlar** qo‘shing.

---

### 🎉 Natijalarni nishonlash

* Har bir loyiha nomi bilan qisqa “demo poster” yoki gif.
* “Eng yaxshi UX”, “Eng yaxshi validatsiya”, “Eng toza kod” kabi mini nominatsiyalar.
* Yakuniy ekran: “Backend + DB + Frontend = Ishlaydigan ilova!” 🙌

---

Shu bilan kurs loyihasi taqdimoti yakunlanadi: **server → database → frontend** zanjiri to‘liq namoyish etildi.


</details>

<hr>

<details>
    <summary>Authentication Essentials & Setup Instructions</summary>

## Authentication Essentials (Asosiy xavfsizlik)

Kelajakda professional API lar uchun authentication (kirish) kerak bo'ladi:

### Basic Authentication Misoli

```javascript
// middleware/auth.js
export const basicAuth = (req, res, next) => {
  const authHeader = req.headers.authorization;
  
  if (!authHeader || !authHeader.startsWith('Basic ')) {
    return res.status(401).json({ 
      status: 'error', 
      message: 'Authorization header required',
      hint: 'Send: Authorization: Basic ' + Buffer.from('username:password').toString('base64')
    });
  }
  
  const base64Credentials = authHeader.split(' ')[1];
  const credentials = Buffer.from(base64Credentials, 'base64').toString('utf8');
  const [username, password] = credentials.split(':');
  
  // Simple demo - production da DB dan tekshiriladi
  if (username === 'admin' && password === 'password123') {
    req.user = { username, role: 'admin' };
    next();
  } else {
    return res.status(401).json({ status: 'error', message: 'Invalid username or password' });
  }
};

// Usage in server.js
import { basicAuth } from './middleware/auth.js';

// Protect sensitive endpoints
app.get('/admin/stats', basicAuth, (req, res) => {
  res.json({ 
    message: `Welcome ${req.user.username}!`,
    secretData: 'This is protected data'
  });
});
```

### API Key Authentication

```javascript
// middleware/apiKey.js
export const apiKeyAuth = (req, res, next) => {
  const apiKey = req.headers['x-api-key'] || req.query.api_key;
  
  const validKeys = ['demo-key-123', 'test-key-456']; // DB dan keladi
  
  if (!apiKey) {
    return res.status(401).json({ status: 'error', message: 'API key required' });
  }
  
  if (!validKeys.includes(apiKey)) {
    return res.status(401).json({ status: 'error', message: 'Invalid API key' });
  }
  
  req.apiClient = { key: apiKey, tier: 'basic' };
  next();
};
```

**Xavfsizlik qoidalari:**
1. ✅ Hech qachon parolni plaintext da saqlamang
2. ✅ HTTPS bilan ishlang (production da)
3. ✅ Environment variables da secrets saqlang
4. ✅ Rate limiting qo'llang
5. ✅ Input validation va sanitization muhim

## Setup Instructions & Best Practices

### O'rnatish bo'yicha to'liq ko'rsatma

```bash
# 1. Loyiha papkasini yarating
mkdir my-backend-project
cd my-backend-project

# 2. Package.json yarating
npm init -y

# 3. Kerakli paketlarni o'rnating
npm install express better-sqlite3 dotenv
npm install --save-dev nodemon

# 4. Package.json ni sozlang
```

```json
{
  "type": "module",
  "scripts": {
    "start": "node server.js",
    "dev": "nodemon server.js"
  }
}
```

```bash
# 5. Environment faylini yarating
echo "PORT=3000
DB_FILE=database.db
NODE_ENV=development" > .env

# 6. Fayllarni yarating
touch server.js db.js index.html

# 7. Ishga tushiring
npm run dev
```

### Best Practices Checklist

#### Code Organization
- [ ] `server.js` - asosiy server fayli
- [ ] `db.js` - database configuration
- [ ] `utils/validation.js` - validation utilities  
- [ ] `middleware/auth.js` - authentication middleware
- [ ] `routes/api.js` - API endpoints
- [ ] `.env` - environment variables
- [ ] `.gitignore` - ignore node_modules, .env

#### Security Checklist
- [ ] Input validation barcha endpoints da
- [ ] Rate limiting qo'shilgan
- [ ] Security headers qo'shilgan
- [ ] Error handling middleware
- [ ] Environment variables ishlatilgan

#### Development Checklist
- [ ] ESLint/Pretwier sozlangan
- [ ] Package.json to'liq
- [ ] README.md yozilgan
- [ ] API endpoints documented
- [ ] Test examples mavjud

</details>

<hr>