# Backend Asoslari - Testlar

> **Eslatma:** Har bir dars uchun 5-10 ta savol berilgan. O'zingizni sinab ko'ring!

---

## 1-hafta — 1-dars: Internet va Backend asoslari

### Savol 1
Internet nima?
- A) Faqat bir nechta kompyuterlarni bog'laydigan kichik tarmoq
- B) Butun dunyodagi kompyuterlar bir-biri bilan bog'langan ulkan tarmoq
- C) Faqat telefonlar uchun mo'ljallangan tarmoq
- D) Faqat serverlar uchun mo'ljallangan tarmoq

### Savol 2
Server nima qiladi?
- A) Faqat ma'lumot saqlaydi
- B) Faqat ma'lumot yuboradi
- C) Ma'lumot saqlaydi va uni boshqalarga jo'natadi
- D) Faqat internetni ta'minlaydi

### Savol 3
Frontend va Backend farqi nimada?
- A) Frontend ko'rinadigan qism, Backend ko'rinmaydigan qism
- B) Ikkalasi ham bir xil narsa
- C) Frontend faqat rasmlar, Backend faqat matnlar
- D) Frontend serverlarda, Backend brauzerda ishlaydi

### Savol 4
HTTP qaysi so'rov turi ma'lumot olish uchun ishlatiladi?
- A) POST
- B) GET
- C) DELETE
- D) UPDATE

### Savol 5
JSON formatida `{}` belgisi nimani bildiradi?
- A) Array (ro'yxat)
- B) String (matn)
- C) Obyekt
- D) Raqam

### Savol 6
Quyidagilardan qaysi biri JSON formatida to'g'ri yozilgan?
- A) {ism: "Ali", yosh: 14}
- B) {"ism": "Ali", "yosh": 14}
- C) (ism: "Ali", yosh: 14)
- D) [ism: "Ali", yosh: 14]

### Savol 7
Status kod 404 nimani anglatadi?
- A) Hammasi joyida
- B) Topilmadi
- C) Serverda xato
- D) Yaratildi

### Savol 8
Onlayn do'konda mahsulotlarni ko'rish qaysi qismga kiradi?
- A) Backend
- B) Frontend
- C) Database
- D) Server

---

## 1-hafta — 2-dars: Node.js o'rnatish va birinchi backend kodimiz

### Savol 1
Node.js nima?
- A) JavaScript'ni faqat brauzerda ishlatish uchun dastur
- B) JavaScript'ni brauzerdan tashqari ham ishlatish imkonini beruvchi platforma
- C) Faqat HTML uchun dastur
- D) CSS kutubxonasi

### Savol 2
Node.js o'rnatilganini qanday tekshirish mumkin?
- A) `node -v`
- B) `node start`
- C) `node check`
- D) `node install`

### Savol 3
npm nima uchun ishlatiladi?
- A) Faqat fayllarni o'chirish uchun
- B) Kutubxonalarni (paketlarni) o'rnatish uchun
- C) Faqat rasmlarni yuklash uchun
- D) HTML yaratish uchun

### Savol 4
`package.json` fayli nima uchun kerak?
- A) Rasmlarni saqlash uchun
- B) Loyiha haqida ma'lumot va sozlamalar saqlash uchun
- C) Faqat CSS yozish uchun
- D) Video saqlash uchun

### Savol 5
Node.js faylini ishga tushirish uchun qaysi buyruq ishlatiladi?
- A) `run fayl.js`
- B) `start fayl.js`
- C) `node fayl.js`
- D) `npm fayl.js`

### Savol 6
`"type": "module"` sozlamasi `package.json` da nima uchun kerak?
- A) Rasmlar bilan ishlash uchun
- B) ES Module (import/export) syntaxini ishlatish uchun
- C) CSS yozish uchun
- D) Database yaratish uchun

### Savol 7
`npm init -y` buyrug'i nima qiladi?
- A) Serverni ishga tushiradi
- B) package.json faylini yaratadi
- C) Node.js o'rnatadi
- D) Barcha fayllarni o'chiradi

---

## 1-hafta — 3-dars: Express bilan birinchi server

### Savol 1
Express nima?
- A) HTML kutubxonasi
- B) CSS framework
- C) Node.js uchun server yaratishni osonlashtiradigan kutubxona
- D) Ma'lumotlar bazasi

### Savol 2
Express'ni o'rnatish uchun qaysi buyruq ishlatiladi?
- A) `node install express`
- B) `npm install express`
- C) `npm get express`
- D) `node get express`

### Savol 3
`app.get()` funksiyasi nima uchun ishlatiladi?
- A) Ma'lumotni o'chirish uchun
- B) GET so'roviga javob berish uchun
- C) Fayllarni yuklash uchun
- D) Rasmlarni ko'rsatish uchun

### Savol 4
`res.send()` nima qiladi?
- A) Foydalanuvchiga matn yoki HTML yuboradi
- B) Fayllarni o'chiradi
- C) Serverni to'xtatadi
- D) Ma'lumotlar bazasini yaratadi

### Savol 5
PORT degani nima?
- A) Serverning nomi
- B) Server tinglaydigan "eshik" raqami
- C) Ma'lumotlar bazasi
- D) HTML fayli

### Savol 6
`http://localhost:3000/about` manzilida `/about` nima deyiladi?
- A) Query
- B) Body
- C) Route (yo'l)
- D) Port

### Savol 7
Quyidagi kodda nima xato?
```javascript
app.listen(3000);
app.get('/', function(req, res) {
  res.send('Salom');
});
```
- A) Hech narsa xato emas
- B) app.get() ni app.listen() dan oldin yozish kerak
- C) res.send() noto'g'ri
- D) Port raqami xato

### Savol 8
Serverni ishga tushirish uchun qaysi buyruq ishlatiladi?
- A) `npm server.js`
- B) `start server.js`
- C) `node server.js`
- D) `run server.js`

---

## 2-hafta — 1-dars: JSON ma'lumot va Thunder Client

### Savol 1
res.send() va res.json() o'rtasidagi asosiy farq nima?
- A) Farqi yo'q, bir xil
- B) res.send() matn yuboradi, res.json() JSON formatda yuboradi
- C) res.json() faqat raqamlar yuboradi
- D) res.send() faqat rasmlar yuboradi

### Savol 2
JSON array (ro'yxat) qaysi belgilar bilan yoziladi?
- A) {}
- B) []
- C) ()
- D) <>

### Savol 3
Thunder Client nima uchun kerak?
- A) Faqat HTML yozish uchun
- B) GET, POST, DELETE kabi turli so'rovlarni test qilish uchun
- C) Faqat rasmlarni ko'rish uchun
- D) CSS yozish uchun

### Savol 4
Quyidagi JSON kod to'g'ri yozilganmi?
```json
{
  "ism": "Ali",
  "yosh": 14
  "hobby": "futbol"
}
```
- A) Ha, to'g'ri
- B) Yo'q, vergul (,) yetishmayapti
- C) Yo'q, qavs xato
- D) Yo'q, ism xato

### Savol 5
Thunder Client qayerda joylashgan?
- A) Brauzerda
- B) Terminalda
- C) VS Code ichida
- D) Alohida dastur

### Savol 6
Quyidagi kodda nima qaytariladi?
```javascript
app.get('/son', function(req, res) {
  res.json({ raqam: 42 });
});
```
- A) "raqam: 42" matni
- B) {"raqam": 42} JSON obyekti
- C) 42 raqami
- D) Hech narsa

### Savol 7
Array ichida nechta obyekt bo'lishi mumkin?
- A) Faqat 1 ta
- B) Maksimum 10 ta
- C) Istalgancha
- D) Faqat 2 ta

---

## 2-hafta — 2-dars: Query parametrlari

### Savol 1
Query parametrlari qayerda yoziladi?
- A) URL boshida
- B) URL oxirida `?` belgisidan keyin
- C) Body ichida
- D) Header ichida

### Savol 2
`http://localhost:3000/salom?ism=Ali` manzilida query parametr qaysi?
- A) localhost
- B) salom
- C) ism=Ali
- D) 3000

### Savol 3
req.query nima uchun ishlatiladi?
- A) Serverni to'xtatish uchun
- B) URL'dan query parametrlarni olish uchun
- C) Fayllarni o'chirish uchun
- D) Rasmlarni yuklash uchun

### Savol 4
Default qiymat nima uchun beriladi?
- A) Serverning tezligini oshirish uchun
- B) Foydalanuvchi parametr yubormasa xatolik bo'lmasligi uchun
- C) Kodni chiroyliroq qilish uchun
- D) Ma'lumotlar bazasini yaratish uchun

### Savol 5
`const ism = req.query.ism || 'mehmon'` kodida `mehmon` nima?
- A) O'zgaruvchi nomi
- B) Default (zaxira) qiymat
- C) Funksiya nomi
- D) Query parametr

### Savol 6
Bir nechta query parametrlarini qanday ajratamiz?
- A) Vergul (,) bilan
- B) Nuqta (.) bilan
- C) Ampersand (&) bilan
- D) Slash (/) bilan

### Savol 7
`http://localhost:3000/info?ism=Ali&yosh=14&shahar=Toshkent` manzilida nechta query parametr bor?
- A) 1 ta
- B) 2 ta
- C) 3 ta
- D) 4 ta

### Savol 8
Query parametrlar majburiymi?
- A) Ha, har doim majburiy
- B) Yo'q, ixtiyoriy (optional)
- C) Faqat GET'da majburiy
- D) Faqat POST'da majburiy

---

## 2-hafta — 3-dars: Route parametrlari va Nodemon

### Savol 1
Route parametrlari (params) qayerda joylashadi?
- A) URL oxirida `?` dan keyin
- B) URL yo'lining o'zi ichida
- C) Body ichida
- D) Header ichida

### Savol 2
`/user/:id` kodida `:id` nima?
- A) Oddiy matn
- B) Route parametri (o'zgaruvchi)
- C) Query parametr
- D) Port raqami

### Savol 3
`http://localhost:3000/kitob/5` manzilida `5` nimani bildiradi?
- A) Port raqami
- B) Route parametri (kitob ID'si)
- C) Query parametr
- D) Server raqami

### Savol 4
req.params nima uchun ishlatiladi?
- A) Query parametrlarni olish uchun
- B) Route parametrlarni olish uchun
- C) Serverni to'xtatish uchun
- D) Ma'lumotni o'chirish uchun

### Savol 5
Nodemon nima qiladi?
- A) Serverni faqat bir marta ishga tushiradi
- B) Kodni saqlashda serverni avtomatik qayta ishga tushiradi
- C) Fayllarni o'chiradi
- D) HTML yaratadi

### Savol 6
Nodemon'ni qanday o'rnatamiz?
- A) `npm install nodemon`
- B) `npm install --save-dev nodemon`
- C) `node install nodemon`
- D) `npm get nodemon`

### Savol 7
`npm start` buyrug'ini ishlashi uchun `package.json` da nima yozilgan bo'lishi kerak?
- A) `"main": "server.js"`
- B) `"scripts": { "start": "nodemon server.js" }`
- C) `"type": "module"`
- D) `"name": "backend"`

### Savol 8
Query va Params farqi nimada?
- A) Farqi yo'q, bir xil
- B) Query ixtiyoriy (?kalit=qiymat), Params yo'l tarkibi (/:id)
- C) Query faqat POST'da, Params faqat GET'da
- D) Query serverda, Params brauzerda

### Savol 9
`/sinf/:sinf/oquvchi/:id` da nechta params bor?
- A) 1 ta
- B) 2 ta
- C) 3 ta
- D) 0 ta

---

## 3-hafta — 1-dars: POST so'rovi va Body ma'lumotlari

### Savol 1
GET va POST farqi nimada?
- A) Farqi yo'q
- B) GET ma'lumot oladi, POST ma'lumot yuboradi
- C) GET tez, POST sekin
- D) GET frontend, POST backend

### Savol 2
POST so'rovida ma'lumot qayerda joylashadi?
- A) URL'da
- B) Body ichida
- C) Header ichida
- D) Port'da

### Savol 3
`app.use(express.json())` nima uchun yoziladi?
- A) Serverni ishga tushirish uchun
- B) JSON body ma'lumotlarini o'qish uchun
- C) HTML yaratish uchun
- D) Rasmlarni yuklash uchun

### Savol 4
req.body nima?
- A) Serverning tanasi
- B) Foydalanuvchi POST orqali yuborgan ma'lumot
- C) URL manzili
- D) Port raqami

### Savol 5
Thunder Client'da POST so'rov yuborish uchun nimalar kerak?
- A) Faqat URL
- B) URL va Method (POST) va Body (JSON)
- C) Faqat Method
- D) Faqat Body

### Savol 6
Status kod 201 nimani anglatadi?
- A) Xato
- B) Topilmadi
- C) Yangi resurs yaratildi
- D) Serverda muammo

### Savol 7
Validation nima?
- A) Serverni ishga tushirish
- B) Foydalanuvchi yuborgan ma'lumotni tekshirish
- C) Ma'lumotni o'chirish
- D) JSON yaratish

### Savol 8
Status kod 400 qachon qaytariladi?
- A) Hammasi yaxshi bo'lganda
- B) Foydalanuvchi noto'g'ri ma'lumot yuborganda
- C) Yangi ma'lumot qo'shilganda
- D) Server ishga tushganda

---

## 3-hafta — 2-dars: Oddiy Todos API (in-memory)

### Savol 1
In-memory ma'lumot saqlash degani nima?
- A) Ma'lumot faylda saqlanadi
- B) Ma'lumot xotirada (RAM) saqlanadi
- C) Ma'lumot internetda saqlanadi
- D) Ma'lumot serverda doimiy saqlanadi

### Savol 2
In-memory ma'lumotning kamchiligi nima?
- A) Juda sekin ishlaydi
- B) Ko'p joy egallaydi
- C) Server o'chsa ma'lumot yo'qoladi
- D) Faqat raqamlar saqlanadi

### Savol 3
Quyidagi kodda `let todos = []` nima?
- A) Funksiya
- B) Bo'sh array (ro'yxat)
- C) Obyekt
- D) String

### Savol 4
ID avtomatik berish uchun qaysi usul ishlatiladi?
- A) `id: 1`
- B) `id: todos.length + 1`
- C) `id: 0`
- D) `id: random()`

### Savol 5
PATCH so'rovi odatda nima uchun ishlatiladi?
- A) Ma'lumotni to'liq o'chirish
- B) Ma'lumotni qisman yangilash
- C) Yangi ma'lumot qo'shish
- D) Ma'lumotni o'qish

### Savol 6
DELETE so'rovi nima qiladi?
- A) Ma'lumotni yangilaydi
- B) Ma'lumotni o'chiradi
- C) Ma'lumotni yaratadi
- D) Ma'lumotni o'qiydi

### Savol 7
`.find()` metodi nima qiladi?
- A) Barcha elementlarni qaytaradi
- B) Shart bo'yicha bitta elementni topadi
- C) Elementni o'chiradi
- D) Yangi element qo'shadi

### Savol 8
Status kod 404 qachon qaytariladi?
- A) Hammasi yaxshi bo'lganda
- B) Izlangan element topilmaganda
- C) Yangi element qo'shilganda
- D) Ma'lumot o'chirilganda

### Savol 9
CRUD nima?
- A) Ma'lumotlar bazasi nomi
- B) Create, Read, Update, Delete operatsiyalari
- C) Kutubxona nomi
- D) Server turi

---

## 4-hafta — 1-dars: Memory vs Database

### Savol 1
RAM (Memory) nima?
- A) Doimiy xotira
- B) Vaqtinchalik xotira
- C) Ma'lumotlar bazasi
- D) JSON fayl

### Savol 2
Database (Ma'lumotlar bazasi) nima?
- A) Vaqtinchalik xotira
- B) Ma'lumotni doimiy saqlaydigan joy
- C) Faqat raqamlar uchun
- D) Faqat matnlar uchun

### Savol 3
Nega ma'lumotni faylda saqlash yaxshiroq?
- A) Tezroq ishlaydi
- B) Server o'chganda ham ma'lumot saqlanadi
- C) Kodni osonlashtiradi
- D) Rang-baranglik uchun

### Savol 4
lowdb nima?
- A) Ma'lumotlar bazasi turi
- B) JSON faylni database sifatida ishlatish uchun kutubxona
- C) HTML framework
- D) CSS kutubxonasi

### Savol 5
lowdb'ni o'rnatish uchun qaysi buyruq ishlatiladi?
- A) `node install lowdb`
- B) `npm install lowdb`
- C) `npm get lowdb`
- D) `lowdb install`

### Savol 6
`await db.read()` nima qiladi?
- A) Ma'lumotni o'chiradi
- B) Ma'lumotni fayldan o'qiydi
- C) Ma'lumotni faylga yozadi
- D) Serverni to'xtatadi

### Savol 7
`await db.write()` nima qiladi?
- A) Ma'lumotni fayldan o'qiydi
- B) Ma'lumotni faylga yozadi
- C) Ma'lumotni o'chiradi
- D) Serverni ishga tushiradi

### Savol 8
In-memory va Database taqqoslashda qaysi tezroq?
- A) Database
- B) In-memory
- C) Bir xil
- D) Ikkalasi ham sekin

---

## 4-hafta — 2-dars: lowdb bilan Todos API

### Savol 1
lowdb bilan ishlashda qaysi fayl yaratiladi?
- A) server.js
- B) db.json
- C) index.html
- D) style.css

### Savol 2
`db.data.todos` nima?
- A) Funksiya
- B) db.json faylidagi todos massivi
- C) Server nomi
- D) Port raqami

### Savol 3
lowdb bilan yangi todo qo'shganda nimani unutmaslik kerak?
- A) `await db.read()`
- B) `await db.write()`
- C) `res.send()`
- D) `console.log()`

### Savol 4
`db.data ||= { todos: [] }` kodi nima qiladi?
- A) Hech narsa
- B) Agar db.data bo'sh bo'lsa, default qiymat beradi
- C) Ma'lumotni o'chiradi
- D) Serverni ishga tushiradi

### Savol 5
lowdb bilan ishlaganda server qayta ishga tushsa ma'lumot qoladi?
- A) Yo'q, yo'qoladi
- B) Ha, db.json faylida saqlanadi
- C) Faqat birinchi 10 ta
- D) Faqat oxirgi 5 ta

### Savol 6
JSONFile adapter nima uchun kerak?
- A) HTML yaratish uchun
- B) lowdb ga qaysi fayldan foydalanishni ko'rsatadi
- C) CSS yozish uchun
- D) Rasmlarni saqlash uchun

### Savol 7
`await` kalit so'zi qachon ishlatiladi?
- A) Hamma joyda
- B) Async operatsiyalarda (masalan, fayl o'qish/yozish)
- C) Faqat GET so'rovlarda
- D) Faqat DELETE'da

---

## 4-hafta — 3-dars: To'liq CRUD (lowdb)

### Savol 1
CRUD nima?
- A) Ma'lumotlar bazasi nomi
- B) Create, Read, Update, Delete operatsiyalari
- C) Server turi
- D) Dasturlash tili

### Savol 2
CRUD'dagi "C" harfi nimani anglatadi?
- A) Connect
- B) Create (Yaratish)
- C) Check
- D) Close

### Savol 3
DELETE so'rovi qaysi HTTP metodidan foydalanadi?
- A) app.get()
- B) app.post()
- C) app.delete()
- D) app.remove()

### Savol 4
PATCH va PUT o'rtasidagi farq nima?
- A) Farqi yo'q
- B) PATCH qisman yangilaydi, PUT to'liq yangilaydi
- C) PATCH tez, PUT sekin
- D) PATCH yangi yaratadi, PUT o'chiradi

### Savol 5
`.findIndex()` metodi nima qaytaradi?
- A) Elementning o'zini
- B) Elementning indeksini (tartib raqamini)
- C) true/false
- D) Array

### Savol 6
`.splice(index, 1)` metodi nima qiladi?
- A) Element qo'shadi
- B) Berilgan indeksdagi elementni o'chiradi
- C) Barcha elementlarni o'chiradi
- D) Hech narsa qilmaydi

### Savol 7
lowdb bilan DELETE operatsiyasidan keyin nima qilish kerak?
- A) Hech narsa
- B) `await db.write()` - o'zgarishni saqlash
- C) Serverni qayta ishga tushirish
- D) Brauzerga xabar yuborish

### Savol 8
`Math.max(...db.data.todos.map(function(t) { return t.id })) + 1` kodi nima qiladi?
- A) Ma'lumotni o'chiradi
- B) Eng katta ID dan 1 katta qiymat qaytaradi (yangi unique ID)
- C) Ma'lumotni o'qiydi
- D) Serverni to'xtatadi

### Savol 9
To'liq CRUD API'da kamida qancha endpoint bo'lishi kerak?
- A) 2 ta (GET, POST)
- B) 3 ta (GET, POST, DELETE)
- C) 4 ta (GET, POST, PUT/PATCH, DELETE)
- D) 1 ta (GET)

### Savol 10
Quyidagi qaysi kod to'g'ri PATCH operatsiyasi?
- A) `app.get('/todos/:id', ...)`
- B) `app.patch('/todos/:id', ...)`
- C) `app.post('/todos/:id', ...)`
- D) `app.update('/todos/:id', ...)`

---

## Umumiy Savollar (Barcha Darslar)

### Savol 1
Backend dasturchi asosan nima bilan shug'ullanadi?
- A) Faqat dizayn
- B) Server, ma'lumotlar bazasi, API yaratish
- C) Faqat ranglar tanlash
- D) Faqat rasmlar bilan ishlash

### Savol 2
Express, Node.js bilan qanday bog'liq?
- A) Express - Node.js uchun framework
- B) Ular bir xil narsa
- C) Express - ma'lumotlar bazasi, Node.js - server
- D) Hech qanday aloqasi yo'q

### Savol 3
Qaysi biri to'g'ri API endpoint?
- A) `GET /users` - barcha foydalanuvchilar
- B) `DELETE /users/5` - 5-foydalanuvchini o'chirish
- C) `POST /users` - yangi foydalanuvchi qo'shish
- D) Barchasi to'g'ri

### Savol 4
Eng to'g'ri kod tartibini toping:
- A) app.listen() → app.use(express.json()) → app.get()
- B) app.get() → app.use(express.json()) → app.listen()
- C) app.use(express.json()) → app.get() → app.listen()
- D) Tartib muhim emas

### Savol 5
Quyidagi qaysi birida ma'lumot server o'chganda yo'qolmaydi?
- A) `let todos = []`
- B) `const todos = []`
- C) lowdb bilan db.json'ga saqlash
- D) Brauzer xotirasida saqlash

### Savol 6
Thunder Client'ning afzalligi nima?
- A) Faqat GET so'rov yuboradi
- B) Barcha HTTP metodlarini (GET, POST, PUT, DELETE) test qilish mumkin
- C) Faqat HTML yozadi
- D) Faqat CSS test qiladi

### Savol 7
Qaysi status kod muvaffaqiyatli operatsiyani bildiradi?
- A) 404
- B) 500
- C) 200
- D) 400

### Savol 8
`res.status(404).json({ xato: 'Topilmadi' })` nima qiladi?
- A) 404 status kod va JSON xabar yuboradi
- B) Faqat 404 yuboradi
- C) Faqat JSON yuboradi
- D) Hech narsa qilmaydi

### Savol 9
Quyidagilardan qaysi biri async operatsiya?
- A) `const x = 5`
- B) `await db.write()`
- C) `res.send('Salom')`
- D) `const app = express()`

### Savol 10
Haqiqiy backend dasturda qaysi qismlar bo'ladi?
- A) Faqat server
- B) Faqat ma'lumotlar bazasi
- C) Server, ma'lumotlar bazasi, API, validation
- D) Faqat HTML va CSS

---

## 🎯 Test Yakunlash Bo'yicha Ko'rsatma

Har bir dars uchun testlarni bajarib, quyidagicha baho bering:

**Baholash tizimi (har bir dars uchun):**
- 9-10 to'g'ri javob: ⭐⭐⭐⭐⭐ Ajoyib! Mavzuni a'lo darajada o'zlashtirdingiz
- 7-8 to'g'ri javob: ⭐⭐⭐⭐ Yaxshi! Asosiy tushunchalarni bildingiz
- 5-6 to'g'ri javob: ⭐⭐⭐ O'rtacha. Darsni qayta ko'rib chiqing
- 4 va undan kam: ⭐⭐ Darsni qaytadan o'rganish kerak

**Maslahat:**
- Agar test qiyin bo'lsa, darslikni qaytadan o'qing
- Amaliy mashqlarni kompyuterda bajaring
- Thunder Client'da o'zingiz sinab ko'ring
- Do'stlaringiz bilan birga muhokama qiling

**Omad tilaymiz!** 🚀

