<details>
    <summary>Backend va frontend farqi</summary>

## 1.1 Backend va Frontend Farqi

### Frontend nima?

**Frontend** - foydalanuvchi ko'radigan va bilan ishlaydigan qism. Bu veb-saytning ko'rinishi, dizayni va foydalanuvchi interfeysi.

#### Frontend qismlari:
- **HTML** - sahifa struktura va mazmun
- **CSS** - dizayn, ranglar, o'lchamlar
- **JavaScript** - interaktivlik, animatsiyalar
- **Rasmlar** - logotip, fotosuratlar
- **Tugmalar** - bosiladigan elementlar

#### Frontend misoli:
```html
<!-- Bu frontend kodi -->
<!DOCTYPE html>
<html>
<head>
    <title>Mening Saytim</title>
    <style>
        body { background-color: lightblue; }
        button { padding: 10px; }
    </style>
</head>
<body>
    <h1>Salom Dunyo!</h1>
    <button onclick="alert('Salom!')">Bosish</button>
</body>
</html>
```

### Backend nima?

**Backend** - foydalanuvchi ko'rmaydigan, lekin veb-saytning ishlashini ta'minlovchi qism. Bu server tomonida ishlaydigan kod.

#### Backend vazifalari:
- **Ma'lumotlarni saqlash** - foydalanuvchi ma'lumotlari
- **Hisoblashlar** - matematik amallar
- **Xavfsizlik** - parollar, shaxsiy ma'lumotlar
- **Ma'lumotlarni qaytarish** - frontend uchun javob
- **Fayllar bilan ishlash** - rasmlar, hujjatlar

#### Backend misoli:
```javascript
// Bu backend kodi (Node.js)
const express = require('express');
const app = express();

// Foydalanuvchi ma'lumotlarini qaytarish
app.get('/users', function(req, res) {
    let users = [
        { name: 'Ahmad', age: 15 },
        { name: 'Sara', age: 14 }
    ];
    res.json(users); // Frontend uchun javob
});

app.listen(3000, function() {
    console.log('Server ishlamoqda!');
});
```

### Frontend va Backend farqi

| Xususiyat | Frontend | Backend |
|-----------|----------|---------|
| **Ko'rinadi** | Ha, foydalanuvchi ko'radi | Yo'q, foydalanuvchi ko'rmaydi |
| **Ish joyi** | Brauzer (kompyuter) | Server (internet) |
| **Vazifasi** | Ko'rinish va interaktivlik | Ma'lumotlar va mantiq |
| **Tillar** | HTML, CSS, JavaScript | JavaScript, Python, Java |
| **Misollar** | Veb-sahifa, dizayn | Ma'lumotlar bazasi, API |

### Misol: Restoran veb-sayti

#### Frontend qismi:
- Restoran menyusi (HTML)
- Chiroyli dizayn (CSS)
- Buyurtma tugmasi (JavaScript)

#### Backend qismi:
- Buyurtmalarni saqlash
- Hisob-kitob qilish
- Restoran xodimlariga xabar berish
- Ma'lumotlarni bazaga yozish

### Nima uchun ikkalasiga ham kerak?

#### Frontend bo'lmagan backend:
- Hech kim ko'rolmaydi
- Ma'lumotlar bor, lekin ko'rinmaydi
- Foydalanuvchi bilan aloqa yo'q

#### Backend bo'lmagan frontend:
- Chiroyli ko'rinadi, lekin ishlamaydi
- Ma'lumotlarni saqlay olmaydi
- Dinamik mazmun bo'lmaydi

### Xulosa

**Frontend** = Ko'rinish + Interaktivlik  
**Backend** = Ma'lumotlar + Mantiq  

Ikkalasi ham birga ishlaydi va bir-biriga muhtoj!

</details>

<details>
    <summary>Server va client tushunchasi</summary>

## 1.2 Server va Client Tushunchasi

### Server nima?

**Server** - ma'lumotlarni saqlaydigan va boshqa kompyuterga yuboradigan kuchli kompyuter. Bu internetdagi katta kompyuter.

#### Server xususiyatlari:
- **24/7 ishlaydi** - doim yoqilgan
- **Internetda joylashgan** - butun dunyodan kirish mumkin
- **Kuchli** - ko'p ishlarni bir vaqtda qila oladi
- **Ma'lumotlarni saqlaydi** - foydalanuvchi ma'lumotlari

#### Server misoli:
```
Google Server → Google.com saytini saqlaydi
Facebook Server → Facebook.com saytini saqlaydi
YouTube Server → Videolarni saqlaydi
```

### Client nima?

**Client** - foydalanuvchining kompyuteri, telefoni yoki plansheti. Bu serverdan ma'lumot oladigan qurilma.

#### Client qurilmalar:
- **Kompyuter** - Windows, Mac, Linux
- **Telefon** - iPhone, Android
- **Planshet** - iPad, Samsung Galaxy Tab
- **Smart TV** - Internetli televizor

### Server va Client aloqasi

#### Qanday ishlaydi:

1. **Client so'rov yuboradi** - "Google.com sahifasini ko'rsat"
2. **Server javob beradi** - HTML, CSS, JavaScript yuboradi
3. **Client ko'rsatadi** - Brauzerda sahifani ochadi

#### Misol:
```
Foydalanuvchi: "YouTube.com" yozadi
    ↓
Client: "Video ro'yxatini ber" so'rov yuboradi
    ↓
YouTube Server: Video ro'yxatini yuboradi
    ↓
Client: Videolarni ko'rsatadi
```

### Request va Response

#### Request (So'rov):
- Client serverga yuboradi
- "Men nima kerak" deb so'raydi
- Misol: "Barcha videolarni ber"

#### Response (Javob):
- Server clientga yuboradi
- "Mana senga kerakli narsa" deb beradi
- Misol: Video ro'yxati

### Misol: Veb-sayt ochish

#### 1-qadam: Client so'rov yuboradi
```
GET /index.html HTTP/1.1
Host: mysite.com
```

#### 2-qadam: Server javob beradi
```
HTTP/1.1 200 OK
Content-Type: text/html

<!DOCTYPE html>
<html>
<head>
    <title>Mening Saytim</title>
</head>
<body>
    <h1>Salom Dunyo!</h1>
</body>
</html>
```

#### 3-qadam: Client ko'rsatadi
- Brauzer HTML kodini o'qiydi
- Sahifani chizadi
- Foydalanuvchi ko'radi

### Turli xil serverlar

#### Web Server:
- Veb-saytlarni saqlaydi
- HTML, CSS, JavaScript yuboradi
- Misol: Apache, Nginx

#### Database Server:
- Ma'lumotlarni saqlaydi
- SQL so'rovlarni bajaradi
- Misol: MySQL, PostgreSQL

#### Application Server:
- Dasturlar ishlaydi
- Mantiqiy amallar bajaradi
- Misol: Node.js, PHP

### Localhost nima?

**Localhost** - o'z kompyuteringizdagi server. Bu rivojlantirish uchun ishlatiladi.

#### Localhost xususiyatlari:
- **Faqat sizga ko'rinadi** - boshqalar ko'rolmaydi
- **Tez ishlaydi** - internet kerak emas
- **Sinash uchun** - kodni test qilish
- **Port 3000** - http://localhost:3000

#### Misol:
```javascript
// Localhost server yaratish
const express = require('express');
const app = express();

app.get('/', function(req, res) {
    res.send('Salom Localhost!');
});

app.listen(3000, function() {
    console.log('Server localhost:3000 da ishlamoqda');
});
```

### Internet vs Localhost

| Xususiyat | Internet Server | Localhost |
|-----------|-----------------|-----------|
| **Kim ko'radi** | Butun dunyo | Faqat siz |
| **Tezlik** | Sekin (internet) | Tez (mahalliy) |
| **Xarajat** | Pul to'lash kerak | Bepul |
| **Maqsad** | Haqiqiy loyiha | Sinash va o'rganish |

### Xulosa

**Server** = Ma'lumotlar va dasturlar joylashgan joy  
**Client** = Foydalanuvchi qurilmasi  
**Request** = "Menga narsa ber"  
**Response** = "Mana senga narsa"  

Bu aloqa internetning asosidir!

</details>

<details>
    <summary>Backend dasturchi nima qiladi?</summary>

## 1.3 Backend Dasturchi Nima Qiladi?

### Backend dasturchi kim?

**Backend dasturchi** - veb-saytning "beyni"ni yaratadigan odam. Bu odam server tomonida ishlaydigan dasturlarni yozadi.

#### Backend dasturchi vazifalari:
- **Server dasturlari yozish** - ma'lumotlarni boshqarish
- **Ma'lumotlar bazasi yaratish** - ma'lumotlarni saqlash
- **API yaratish** - frontend va backend o'rtasida aloqa
- **Xavfsizlik ta'minlash** - ma'lumotlarni himoya qilish
- **Server sozlash** - dasturni internetga joylashtirish

### Backend dasturchi qanday ishlaydi?

#### 1. Loyiha talablarini o'rganadi
```
Mijoz: "Online do'kon yaratishim kerak"
Dasturchi: "Qanday mahsulotlar? Qanday to'lov?"
Mijoz: "Telefonlar, karta bilan to'lov"
Dasturchi: "Tushundim, loyihani boshlayman"
```

#### 2. Ma'lumotlar bazasi loyihasini yaratadi
```sql
-- Mahsulotlar jadvali
CREATE TABLE products (
    id INTEGER PRIMARY KEY,
    name TEXT,
    price DECIMAL,
    description TEXT
);

-- Buyurtmalar jadvali
CREATE TABLE orders (
    id INTEGER PRIMARY KEY,
    customer_name TEXT,
    total_price DECIMAL,
    order_date DATE
);
```

#### 3. API endpoints yaratadi
```javascript
// Mahsulotlarni ko'rsatish
app.get('/products', function(req, res) {
    // Ma'lumotlar bazasidan mahsulotlarni olish
    let products = database.getAllProducts();
    res.json(products);
});

// Yangi buyurtma yaratish
app.post('/orders', function(req, res) {
    // Buyurtma ma'lumotlarini saqlash
    let order = req.body;
    database.saveOrder(order);
    res.json({ message: 'Buyurtma qabul qilindi!' });
});
```

#### 4. Xavfsizlikni ta'minlaydi
```javascript
// Parolni shifrlash
const bcrypt = require('bcrypt');
let hashedPassword = bcrypt.hashSync(userPassword, 10);

// Foydalanuvchini tekshirish
app.post('/login', function(req, res) {
    let username = req.body.username;
    let password = req.body.password;
    
    // Parolni tekshirish
    if (bcrypt.compareSync(password, user.hashedPassword)) {
        res.json({ success: true });
    } else {
        res.json({ success: false });
    }
});
```

### Backend dasturchi kundalik ishlari

#### Dasturlash (70% vaqt):
- Kod yozish
- Xatolarni tuzatish
- Yangi funksiyalar qo'shish
- Kodni optimizatsiya qilish

#### Loyihalash (20% vaqt):
- Ma'lumotlar bazasi loyihasi
- API struktura
- Xavfsizlik rejasi
- Performance optimizatsiya

#### Hamkorlik (10% vaqt):
- Frontend dasturchi bilan ishlash
- Mijoz bilan suhbat
- Loyiha rahbari bilan maslahat
- Jamoa bilan kodni ko'rib chiqish

### Backend dasturchi qanday loyihalar yaratadi?

#### 1. E-commerce veb-saytlar
- **Mahsulotlar katalogi** - ma'lumotlar bazasida
- **Savatcha tizimi** - buyurtmalarni saqlash
- **To'lov tizimi** - xavfsiz to'lov
- **Buyurtma boshqaruvi** - admin panel

#### 2. Ijtimoiy tarmoqlar
- **Foydalanuvchi tizimi** - ro'yxatdan o'tish
- **Post yaratish** - ma'lumotlarni saqlash
- **Izohlar** - foydalanuvchilar o'rtasida aloqa
- **Dostlar tizimi** - munosabatlar

#### 3. Blog platformalar
- **Maqola yaratish** - ma'lumotlarni saqlash
- **Kategoriyalar** - tashkil etish
- **Izohlar** - foydalanuvchi fikrlari
- **Qidiruv** - ma'lumotlarni topish

#### 4. O'quv platformalar
- **Kurslar** - video va matn
- **Testlar** - savollar va javoblar
- **Baholash** - natijalarni hisoblash
- **Progress** - o'quvchi rivoji

### Backend dasturchi qanday ishlaydi?

#### Ish kuni misoli:

**9:00 - 10:00: Loyiha rejalashtirish**
- Bugungi vazifalarni ko'rib chiqish
- Frontend dasturchi bilan suhbat
- Yangi funksiyalar haqida o'ylash

**10:00 - 12:00: Dasturlash**
- Yangi API endpoint yaratish
- Ma'lumotlar bazasini o'zgartirish
- Kod yozish va test qilish

**12:00 - 13:00: Tushlik**

**13:00 - 15:00: Dasturlash davomi**
- Xatolarni tuzatish
- Performance optimizatsiya
- Kodni tozalash

**15:00 - 16:00: Hamkorlik**
- Frontend dasturchi bilan maslahat
- Loyiha rahbari bilan hisobot
- Keyingi kun rejalari

**16:00 - 17:00: Hujjatlashtirish**
- Kod hujjatlarini yozish
- API hujjatlarini yangilash
- Loyiha hujjatlarini tayyorlash

### Backend dasturchi qanday kasb?

#### Ijobiy tomonlari:
- **Yuqori maosh** - yaxshi daromad
- **Talab yuqori** - ko'p ish o'rinlari
- **Masofaviy ish** - uydan ishlash mumkin
- **Ijodkorlik** - yangi yechimlar topish
- **O'sish imkoniyati** - doim yangi narsalar

#### Qiyinchiliklari:
- **Murakkablik** - ko'p narsalarni bilish kerak
- **Mas'uliyat** - xavfsizlik mas'uliyati
- **O'zgaruvchanlik** - texnologiyalar tez o'zgaradi
- **Xatolar** - kichik xato katta muammo

### Xulosa

**Backend dasturchi** = Veb-saytning "beyni"ni yaratadigan odam

#### Asosiy vazifalar:
- Ma'lumotlarni saqlash va boshqarish
- Frontend va backend o'rtasida aloqa
- Xavfsizlikni ta'minlash
- Server dasturlarini yozish

#### Qanday ishlaydi:
- Kod yozish (70%)
- Loyihalash (20%)
- Hamkorlik (10%)

Bu juda qiziqarli va talab qilinadigan kasb!

</details>

<details>
    <summary>Node.js nima va nima uchun tanlangan?</summary>

## 1.4 Node.js Nima va Nima Uchun Tanlangan?

### Node.js nima?

**Node.js** - JavaScript tilida server dasturlarini yozish uchun platforma. Bu JavaScript ni faqat brauzerda emas, serverda ham ishlatish imkonini beradi.

#### Node.js tushunchasi:
- **JavaScript** - bir xil til frontend va backend uchun
- **Server platforma** - backend dasturlar yozish
- **Event-driven** - hodisalar asosida ishlaydi
- **Non-blocking** - ko'p ishlarni bir vaqtda qila oladi

### JavaScript tarixi

#### Avvalgi holat:
```
Frontend: JavaScript (brauzerda)
Backend: PHP, Python, Java (serverda)
```

#### Node.js dan keyin:
```
Frontend: JavaScript (brauzerda)
Backend: JavaScript (serverda) ← Node.js
```

### Node.js qanday ishlaydi?

#### V8 Engine:
- **Google Chrome** ning JavaScript engine
- **JavaScript kodini** mashina kodiga aylantiradi
- **Tez ishlaydi** - C++ da yozilgan
- **Node.js** V8 ni serverda ishlatadi

#### Misol:
```javascript
// Bu kod brauzerda ishlaydi
console.log('Salom Brauzer!');

// Bu kod Node.js da ham ishlaydi
console.log('Salom Server!');
```

### Node.js afzalliklari

#### 1. Bir til - JavaScript
```javascript
// Frontend kodi
function getUserName() {
    return 'Ahmad';
}

// Backend kodi (Node.js)
function getUserName() {
    return 'Ahmad'; // Xuddi shunday!
}
```

#### 2. Tez ishlaydi
- **V8 Engine** - juda tez
- **Event-driven** - kutmaydi
- **Non-blocking** - ko'p ishlar bir vaqtda

#### 3. Katta jamoa
- **npm** - eng katta paketlar kutubxonasi
- **Ko'p dasturchilar** - yordam olish oson
- **Ko'p resurslar** - darsliklar, misollar

#### 4. Oddiy o'rganish
- **JavaScript** ni bilasizmi? Node.js ni ham bilasiz!
- **Bir xil sintaksis** - frontend va backend
- **Bir xil mantiq** - oson o'tish

### Node.js misollari

#### 1. Oddiy server
```javascript
// server.js
const http = require('http');

const server = http.createServer(function(req, res) {
    res.writeHead(200, {'Content-Type': 'text/html'});
    res.write('<h1>Salom Node.js!</h1>');
    res.end();
});

server.listen(3000, function() {
    console.log('Server 3000 portda ishlamoqda');
});
```

#### 2. Fayl o'qish
```javascript
// file.js
const fs = require('fs');

fs.readFile('data.txt', 'utf8', function(err, data) {
    if (err) {
        console.log('Xato:', err);
    } else {
        console.log('Fayl mazmuni:', data);
    }
});
```

#### 3. Ma'lumotlar bazasi
```javascript
// database.js
const sqlite3 = require('sqlite3');

const db = new sqlite3.Database('mydatabase.db');

db.run("CREATE TABLE users (id INTEGER PRIMARY KEY, name TEXT)");
db.run("INSERT INTO users (name) VALUES ('Ahmad')");

db.all("SELECT * FROM users", function(err, rows) {
    console.log('Foydalanuvchilar:', rows);
});
```

### Node.js vs boshqa tillar

| Xususiyat | Node.js | PHP | Python | Java |
|-----------|---------|-----|--------|------|
| **Til** | JavaScript | PHP | Python | Java |
| **O'rganish** | Oson (JS bilasizmi?) | O'rganish kerak | O'rganish kerak | O'rganish kerak |
| **Tezlik** | Tez | O'rta | Sekin | Tez |
| **Paketlar** | Ko'p (npm) | Ko'p | Ko'p | Ko'p |
| **Ish o'rinlari** | Ko'p | Ko'p | Ko'p | Ko'p |

### Node.js nima uchun tanlangan?

#### 1. Oson o'rganish
- **JavaScript** ni bilasizmi? Node.js ni ham bilasiz!
- **Frontend** dan **backend** ga oson o'tish
- **Bir xil til** - qo'shimcha o'rganish yo'q

#### 2. Zamonaviy
- **Ko'p kompaniyalar** ishlatadi
- **Katta loyihalar** - Netflix, Uber, PayPal
- **Kelajakda** ham kerak bo'ladi

#### 3. Tez rivojlanish
- **Ko'p paketlar** - npm da millionlab
- **Express.js** - tez server yaratish
- **Ko'p misollar** - internetda

#### 4. Kichik loyihalar uchun ideal
- **Oddiy server** - bir necha qator kod
- **Ma'lumotlar bazasi** - SQLite bilan oson
- **API yaratish** - Express.js bilan tez

### Node.js bilan nima qilish mumkin?

#### 1. Veb-serverlar
```javascript
// Express.js bilan
const express = require('express');
const app = express();

app.get('/', function(req, res) {
    res.send('Salom Dunyo!');
});

app.listen(3000);
```

#### 2. API yaratish
```javascript
// REST API
app.get('/api/users', function(req, res) {
    res.json([{name: 'Ahmad'}, {name: 'Sara'}]);
});

app.post('/api/users', function(req, res) {
    // Yangi foydalanuvchi yaratish
    res.json({message: 'Foydalanuvchi yaratildi!'});
});
```

#### 3. Ma'lumotlar bazasi
```javascript
// SQLite bilan
const db = new sqlite3.Database('app.db');

app.get('/api/products', function(req, res) {
    db.all("SELECT * FROM products", function(err, rows) {
        res.json(rows);
    });
});
```

#### 4. Fayllar bilan ishlash
```javascript
// Fayl yuklash
app.post('/upload', function(req, res) {
    // Faylni saqlash
    res.json({message: 'Fayl yuklandi!'});
});
```

### Xulosa

**Node.js** = JavaScript ni serverda ishlatish imkonini beruvchi platforma

#### Afzalliklari:
- **Bir til** - JavaScript frontend va backend uchun
- **Oson o'rganish** - qo'shimcha til o'rganish yo'q
- **Tez ishlaydi** - V8 Engine
- **Ko'p paketlar** - npm kutubxonasi
- **Zamonaviy** - ko'p kompaniyalar ishlatadi

#### Nima uchun tanlangan:
- **Oson** - JavaScript ni bilasizmi, Node.js ni ham bilasiz!
- **Tez** - loyihalar tez yaratiladi
- **Kichik** - oddiy loyihalar uchun ideal
- **Kelajakda** - ish o'rinlari ko'p

Bu backend dasturlashni o'rganish uchun eng yaxshi tanlov!

</details>

<details>
    <summary>Backend qanday ishlaydi?</summary>

## 1.5 Backend Qanday Ishlaydi?

### Backend ishlash jarayoni

Backend ishlashi juda oddiy tushuncha: **So'rov olish → Ishlash → Javob berish**

#### Asosiy jarayon:
```
1. Foydalanuvchi so'rov yuboradi
2. Backend so'rovni qabul qiladi
3. Backend ishlaydi (ma'lumotlar bilan)
4. Backend javob yuboradi
5. Foydalanuvchi javobni ko'radi
```

### Misol: Todo List veb-sayti

#### 1. Foydalanuvchi so'rov yuboradi
```
Foydalanuvchi: "Barcha vazifalarimni ko'rsat"
Brauzer: GET /todos so'rovini yuboradi
```

#### 2. Backend so'rovni qabul qiladi
```javascript
// Express.js server
app.get('/todos', function(req, res) {
    // So'rov qabul qilindi!
    console.log('Foydalanuvchi todos so'radi');
});
```

#### 3. Backend ishlaydi
```javascript
app.get('/todos', function(req, res) {
    // Ma'lumotlar bazasidan todos ni olish
    db.all("SELECT * FROM todos", function(err, todos) {
        if (err) {
            console.log('Xato:', err);
        } else {
            console.log('Todos topildi:', todos);
        }
    });
});
```

#### 4. Backend javob yuboradi
```javascript
app.get('/todos', function(req, res) {
    db.all("SELECT * FROM todos", function(err, todos) {
        if (err) {
            res.json({error: 'Xato yuz berdi'});
        } else {
            res.json(todos); // Foydalanuvchiga yuborish
        }
    });
});
```

#### 5. Foydalanuvchi javobni ko'radi
```
Backend: [{"id": 1, "text": "Dars o'qish"}, {"id": 2, "text": "Uy ishi"}]
Frontend: Todo listini ko'rsatadi
```

### Batafsil misol: Yangi todo qo'shish

#### 1. Foydalanuvchi formani to'ldiradi
```html
<!-- Frontend form -->
<form id="todoForm">
    <input type="text" id="todoText" placeholder="Yangi vazifa">
    <button type="submit">Qo'shish</button>
</form>
```

#### 2. JavaScript so'rov yuboradi
```javascript
// Frontend JavaScript
document.getElementById('todoForm').addEventListener('submit', function(e) {
    e.preventDefault();
    
    let todoText = document.getElementById('todoText').value;
    
    // Backend ga so'rov yuborish
    fetch('/todos', {
        method: 'POST',
        headers: {'Content-Type': 'application/json'},
        body: JSON.stringify({text: todoText})
    });
});
```

#### 3. Backend so'rovni qabul qiladi
```javascript
// Backend Express.js
app.post('/todos', function(req, res) {
    let todoText = req.body.text;
    console.log('Yangi todo:', todoText);
});
```

#### 4. Backend ma'lumotlar bazasiga yozadi
```javascript
app.post('/todos', function(req, res) {
    let todoText = req.body.text;
    
    // Ma'lumotlar bazasiga yozish
    db.run("INSERT INTO todos (text) VALUES (?)", [todoText], function(err) {
        if (err) {
            console.log('Xato:', err);
        } else {
            console.log('Todo saqlandi!');
        }
    });
});
```

#### 5. Backend javob yuboradi
```javascript
app.post('/todos', function(req, res) {
    let todoText = req.body.text;
    
    db.run("INSERT INTO todos (text) VALUES (?)", [todoText], function(err) {
        if (err) {
            res.json({success: false, error: err.message});
        } else {
            res.json({success: true, message: 'Todo qo\'shildi!'});
        }
    });
});
```

#### 6. Frontend javobni qabul qiladi
```javascript
// Frontend JavaScript
fetch('/todos', {
    method: 'POST',
    headers: {'Content-Type': 'application/json'},
    body: JSON.stringify({text: todoText})
})
.then(response => response.json())
.then(data => {
    if (data.success) {
        alert('Todo qo\'shildi!');
        // Todo listini yangilash
        loadTodos();
    } else {
        alert('Xato: ' + data.error);
    }
});
```

### Backend komponentlari

#### 1. Web Server
```javascript
// Server yaratish
const express = require('express');
const app = express();

// Server ishga tushirish
app.listen(3000, function() {
    console.log('Server ishlamoqda!');
});
```

#### 2. Routes (Yo'llar)
```javascript
// Turli yo'llar
app.get('/todos', function(req, res) {
    // Barcha todos ni olish
});

app.post('/todos', function(req, res) {
    // Yangi todo qo'shish
});

app.put('/todos/:id', function(req, res) {
    // Todo ni o'zgartirish
});

app.delete('/todos/:id', function(req, res) {
    // Todo ni o'chirish
});
```

#### 3. Database (Ma'lumotlar bazasi)
```javascript
// SQLite ma'lumotlar bazasi
const sqlite3 = require('sqlite3');
const db = new sqlite3.Database('todos.db');

// Jadval yaratish
db.run("CREATE TABLE IF NOT EXISTS todos (id INTEGER PRIMARY KEY, text TEXT)");
```

#### 4. Middleware (Orta dastur)
```javascript
// JSON ma'lumotlarni o'qish
app.use(express.json());

// Static fayllarni serve qilish
app.use(express.static('public'));

// CORS sozlamalari
app.use(function(req, res, next) {
    res.header('Access-Control-Allow-Origin', '*');
    next();
});
```

### Backend ishlash bosqichlari

#### 1. Dastur boshlanishi
```javascript
// server.js
const express = require('express');
const app = express();

// Middleware sozlash
app.use(express.json());
app.use(express.static('public'));

// Routes sozlash
app.get('/', function(req, res) {
    res.sendFile(__dirname + '/public/index.html');
});

// Server ishga tushirish
app.listen(3000, function() {
    console.log('Server http://localhost:3000 da ishlamoqda');
});
```

#### 2. So'rov qabul qilish
```javascript
// Foydalanuvchi so'rov yuboradi
// GET /todos

app.get('/todos', function(req, res) {
    console.log('GET /todos so\'rovi qabul qilindi');
    // Ma'lumotlar bazasidan olish
});
```

#### 3. Ma'lumotlar bilan ishlash
```javascript
app.get('/todos', function(req, res) {
    // Ma'lumotlar bazasidan olish
    db.all("SELECT * FROM todos", function(err, todos) {
        if (err) {
            console.log('Database xatosi:', err);
            res.status(500).json({error: 'Server xatosi'});
        } else {
            console.log('Todos topildi:', todos.length, 'ta');
            res.json(todos);
        }
    });
});
```

#### 4. Javob yuborish
```javascript
// Javob tayyor
let response = {
    success: true,
    data: todos,
    count: todos.length
};

res.json(response);
```

### Backend xatolari

#### 1. Ma'lumotlar bazasi xatosi
```javascript
db.all("SELECT * FROM todos", function(err, todos) {
    if (err) {
        console.log('Database xatosi:', err);
        res.status(500).json({
            success: false,
            error: 'Ma\'lumotlar bazasi xatosi'
        });
    } else {
        res.json(todos);
    }
});
```

#### 2. Noto'g'ri so'rov
```javascript
app.get('/todos/:id', function(req, res) {
    let id = req.params.id;
    
    if (isNaN(id)) {
        res.status(400).json({
            success: false,
            error: 'Noto\'g\'ri ID'
        });
        return;
    }
    
    // Davom etish...
});
```

#### 3. Ma'lumot topilmadi
```javascript
app.get('/todos/:id', function(req, res) {
    let id = req.params.id;
    
    db.get("SELECT * FROM todos WHERE id = ?", [id], function(err, todo) {
        if (err) {
            res.status(500).json({error: 'Server xatosi'});
        } else if (!todo) {
            res.status(404).json({error: 'Todo topilmadi'});
        } else {
            res.json(todo);
        }
    });
});
```

### Xulosa

**Backend ishlashi** = So'rov → Ishlash → Javob

#### Asosiy jarayon:
1. **So'rov qabul qilish** - foydalanuvchi nima xohlaydi?
2. **Ishlash** - ma'lumotlar bilan amallar
3. **Javob berish** - natijani yuborish

#### Backend komponentlari:
- **Web Server** - so'rovlarni qabul qiladi
- **Routes** - turli yo'llar
- **Database** - ma'lumotlarni saqlaydi
- **Middleware** - orta dastur

#### Misol:
- Foydalanuvchi: "Todos ni ko'rsat"
- Backend: Ma'lumotlar bazasidan olish
- Backend: JSON formatida yuborish
- Foydalanuvchi: Todo listini ko'rish

Bu juda oddiy va mantiqiy jarayon!

</details>
