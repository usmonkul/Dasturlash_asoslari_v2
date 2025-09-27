<details>
    <summary>JavaScript backend uchun qanday ishlaydi?</summary>

## 3.1 JavaScript Backend uchun Qanday Ishlaydi?

### JavaScript backend va frontend farqi

#### Frontend JavaScript:
- **Brauzerda ishlaydi** - Chrome, Firefox, Safari
- **DOM bilan ishlaydi** - HTML elementlari
- **Foydalanuvchi bilan** - tugmalar, formlar
- **Cheklangan imkoniyatlar** - xavfsizlik uchun

#### Backend JavaScript (Node.js):
- **Serverda ishlaydi** - kompyuter ichida
- **Fayllar bilan ishlaydi** - o'qish, yozish
- **Ma'lumotlar bazasi** - SQL, NoSQL
- **Keng imkoniyatlar** - server resurslari

### Node.js JavaScript engine

#### V8 Engine:
- **Google Chrome** ning JavaScript engine
- **JavaScript kodini** mashina kodiga aylantiradi
- **Tez ishlaydi** - C++ da yozilgan
- **Node.js** V8 ni serverda ishlatadi

#### Misol:
```javascript
// Bu kod brauzerda ham, Node.js da ham ishlaydi
console.log('Salom Dunyo!');

let name = 'Ahmad';
let age = 15;
console.log(`Salom, men ${name}, ${age} yoshdaman`);

// Ammo bu kod faqat Node.js da ishlaydi
const fs = require('fs');
fs.readFile('data.txt', 'utf8', function(err, data) {
    console.log(data);
});
```

### JavaScript backend xususiyatlari

#### 1. Event-driven (Hodisa asosli):
```javascript
// Server hodisasini kutish
const http = require('http');

const server = http.createServer(function(req, res) {
    // Har bir so'rov uchun bu funksiya ishlaydi
    console.log('Yangi so\'rov qabul qilindi');
    res.writeHead(200, {'Content-Type': 'text/html'});
    res.write('<h1>Salom Server!</h1>');
    res.end();
});

server.listen(3000, function() {
    // Server ishga tushganda bu funksiya ishlaydi
    console.log('Server 3000 portda ishlamoqda');
});
```

#### 2. Non-blocking (To'sqinlik qilmaydigan):
```javascript
// Blok qiluvchi kod (yomon)
console.log('1');
// Bu 3 soniya kutadi
setTimeout(function() {
    console.log('2');
}, 3000);
console.log('3');

// Natija: 1, 3, 2 (3 soniya keyin)
```

#### 3. Asynchronous (Asinxron):
```javascript
// Fayl o'qish - asinxron
const fs = require('fs');

console.log('Fayl o\'qish boshlandi');

fs.readFile('data.txt', 'utf8', function(err, data) {
    if (err) {
        console.log('Xato:', err);
    } else {
        console.log('Fayl mazmuni:', data);
    }
});

console.log('Fayl o\'qish tugagandan keyin');
// Bu avval chiqadi!
```

### JavaScript backend modullari

#### Built-in modullar:
```javascript
// HTTP moduli - web server yaratish
const http = require('http');

// File System moduli - fayllar bilan ishlash
const fs = require('fs');

// Path moduli - fayl yo'llari
const path = require('path');

// OS moduli - operatsion sistema
const os = require('os');

// URL moduli - URL parsing
const url = require('url');
```

#### Modul ishlatish misoli:
```javascript
// server.js
const http = require('http');
const fs = require('fs');
const path = require('path');

const server = http.createServer(function(req, res) {
    // URL ni parse qilish
    const parsedUrl = new URL(req.url, 'http://localhost:3000');
    const pathname = parsedUrl.pathname;
    
    console.log('So\'rov:', pathname);
    
    // Fayl yo'lini tuzish
    const filePath = path.join(__dirname, 'public', pathname);
    
    // Faylni o'qish
    fs.readFile(filePath, function(err, data) {
        if (err) {
            res.writeHead(404);
            res.write('Fayl topilmadi');
        } else {
            res.writeHead(200);
            res.write(data);
        }
        res.end();
    });
});

server.listen(3000);
```

### JavaScript backend vs boshqa tillar

#### JavaScript (Node.js):
```javascript
// Oddiy server
const http = require('http');
http.createServer((req, res) => {
    res.writeHead(200, {'Content-Type': 'text/html'});
    res.end('<h1>Salom!</h1>');
}).listen(3000);
```

#### Python:
```python
# Flask server
from flask import Flask
app = Flask(__name__)

@app.route('/')
def hello():
    return '<h1>Salom!</h1>'

if __name__ == '__main__':
    app.run(port=3000)
```

#### PHP:
```php
<?php
// PHP server
echo '<h1>Salom!</h1>';
?>
```

### JavaScript backend afzalliklari

#### 1. Bir til:
- **Frontend** - JavaScript
- **Backend** - JavaScript
- **Qo'shimcha til** o'rganish shart emas

#### 2. Tez rivojlanish:
- **npm paketlar** - millionlab kutubxona
- **Ko'p misollar** - internetda
- **Katta jamoa** - yordam olish oson

#### 3. JSON tabiiy:
```javascript
// JavaScript da JSON tabiiy
let user = {
    name: 'Ahmad',
    age: 15,
    city: 'Toshkent'
};

// JSON ga aylantirish
let jsonString = JSON.stringify(user);
console.log(jsonString); // {"name":"Ahmad","age":15,"city":"Toshkent"}

// JSON dan obyektga
let userObj = JSON.parse(jsonString);
console.log(userObj.name); // Ahmad
```

### Xulosa

**JavaScript backend** = Bir til, keng imkoniyatlar, tez rivojlanish

#### Asosiy farqlar:
- **Frontend** - brauzerda, DOM bilan
- **Backend** - serverda, fayllar bilan
- **Bir xil til** - JavaScript
- **Keng imkoniyatlar** - server resurslari

JavaScript backend uchun ideal til!

</details>

<details>
    <summary>Console.log va debugging</summary>

## 3.2 Console.log va Debugging

### Console.log nima?

**Console.log** - JavaScript da ma'lumotlarni ko'rsatish uchun funksiya. Bu debugging va kod ishlashini kuzatish uchun ishlatiladi.

#### Console.log ishlatish:
```javascript
// Oddiy matn
console.log('Salom Dunyo!');

// O'zgaruvchi
let name = 'Ahmad';
console.log(name);

// Bir nechta ma'lumot
console.log('Ism:', name, 'Yosh:', 15);

// Template literal
console.log(`Salom, men ${name}man`);
```

### Console.log turlari

#### 1. Oddiy log:
```javascript
console.log('Oddiy xabar');
// Natija: Oddiy xabar
```

#### 2. Error log:
```javascript
console.error('Xato xabari');
// Natija: Xato xabari (qizil rangda)
```

#### 3. Warning log:
```javascript
console.warn('Ogohlantirish');
// Natija: Ogohlantirish (sariq rangda)
```

#### 4. Info log:
```javascript
console.info('Ma'lumot');
// Natija: Ma'lumot (ko'k rangda)
```

### Console.log misollari

#### O'zgaruvchilar bilan:
```javascript
let userName = 'Ahmad';
let userAge = 15;
let isStudent = true;

console.log('Foydalanuvchi ma\'lumotlari:');
console.log('Ism:', userName);
console.log('Yosh:', userAge);
console.log('Talaba:', isStudent);
```

#### Obyektlar bilan:
```javascript
let user = {
    name: 'Ahmad',
    age: 15,
    city: 'Toshkent',
    hobbies: ['dasturlash', 'futbol']
};

console.log('Foydalanuvchi:', user);
console.log('Ism:', user.name);
console.log('Sevimli mashg\'ulot:', user.hobbies[0]);
```

#### Massivlar bilan:
```javascript
let fruits = ['olma', 'banan', 'apelsin'];
console.log('Mevalar:', fruits);
console.log('Birinchi meva:', fruits[0]);
console.log('Mevalar soni:', fruits.length);
```

### Debugging nima?

**Debugging** - kodda xatolarni topish va tuzatish jarayoni. Bu dasturchining eng muhim ko'nikmalaridan biri.

#### Debugging bosqichlari:
1. **Xatoni topish** - qayerda xato?
2. **Xatoni tushunish** - nima xato?
3. **Xatoni tuzatish** - qanday tuzatish?
4. **Test qilish** - tuzatish ishlaydimi?

### Console.log bilan debugging

#### 1. Kod ishlashini kuzatish:
```javascript
function addNumbers(a, b) {
    console.log('addNumbers chaqirildi');
    console.log('a =', a);
    console.log('b =', b);
    
    let result = a + b;
    console.log('Natija =', result);
    
    return result;
}

let sum = addNumbers(5, 3);
console.log('Javob:', sum);
```

#### 2. Loop larni kuzatish:
```javascript
let numbers = [1, 2, 3, 4, 5];

console.log('Loop boshlandi');
for (let i = 0; i < numbers.length; i++) {
    console.log(`i = ${i}, qiymat = ${numbers[i]}`);
}
console.log('Loop tugadi');
```

#### 3. Shartlarni tekshirish:
```javascript
let age = 15;

console.log('Yosh tekshirilmoqda:', age);

if (age >= 18) {
    console.log('Katta yosh');
} else {
    console.log('Kichik yosh');
}

console.log('Yosh tekshiruvi tugadi');
```

### Node.js da console.log

#### Server da console.log:
```javascript
const http = require('http');

const server = http.createServer(function(req, res) {
    // Har bir so'rov uchun log
    console.log('Yangi so\'rov:', req.url);
    console.log('So\'rov vaqti:', new Date());
    
    res.writeHead(200, {'Content-Type': 'text/html'});
    res.write('<h1>Salom!</h1>');
    res.end();
});

server.listen(3000, function() {
    console.log('Server ishga tushdi');
    console.log('Port: 3000');
    console.log('URL: http://localhost:3000');
});
```

#### Fayl bilan ishlashda console.log:
```javascript
const fs = require('fs');

console.log('Fayl o\'qish boshlandi');

fs.readFile('data.txt', 'utf8', function(err, data) {
    if (err) {
        console.error('Xato yuz berdi:', err.message);
    } else {
        console.log('Fayl muvaffaqiyatli o\'qildi');
        console.log('Fayl hajmi:', data.length, 'belgi');
        console.log('Fayl mazmuni:', data);
    }
});

console.log('Fayl o\'qish jarayoni tugadi');
```

### Console.log maslahatlari

#### 1. Ma'noli xabarlar yozing:
```javascript
// Yomon
console.log(data);

// Yaxshi
console.log('Foydalanuvchi ma\'lumotlari:', data);
console.log('Ma\'lumotlar soni:', data.length);
```

#### 2. Ranglar ishlating:
```javascript
console.log('\x1b[32m%s\x1b[0m', 'Muvaffaqiyat!'); // Yashil
console.log('\x1b[31m%s\x1b[0m', 'Xato!'); // Qizil
console.log('\x1b[33m%s\x1b[0m', 'Ogohlantirish!'); // Sariq
```

#### 3. Vaqt qo'shing:
```javascript
console.log(`[${new Date().toLocaleTimeString()}] Server ishga tushdi`);
```

### Xulosa

**Console.log** = Debugging va kod kuzatish uchun asosiy vosita

#### Foydalanish:
- **Ma'lumotlarni ko'rsatish** - o'zgaruvchilar, obyektlar
- **Kod ishlashini kuzatish** - qaysi qism ishlayapti
- **Xatolarni topish** - qayerda muammo
- **Server kuzatish** - so'rovlar, javoblar

Console.log - dasturchining eng yaxshi do'sti!

</details>

<details>
    <summary>Fayllar bilan ishlash (fs moduli)</summary>

## 3.3 Fayllar bilan Ishlash (fs moduli)

### fs moduli nima?

**fs (File System)** - Node.js ning fayllar bilan ishlash moduli. Bu fayllarni o'qish, yozish, o'chirish va boshqarish imkonini beradi.

#### fs modulini import qilish:
```javascript
// fs modulini import qilish
const fs = require('fs');

// Yoki ES6 sintaksis
import fs from 'fs';
```

### Fayl o'qish

#### 1. Synxron fayl o'qish:
```javascript
const fs = require('fs');

try {
    // Faylni o'qish
    const data = fs.readFileSync('data.txt', 'utf8');
    console.log('Fayl mazmuni:', data);
} catch (err) {
    console.error('Xato:', err.message);
}
```

#### 2. Asinxron fayl o'qish:
```javascript
const fs = require('fs');

// Callback funksiya bilan
fs.readFile('data.txt', 'utf8', function(err, data) {
    if (err) {
        console.error('Xato:', err);
    } else {
        console.log('Fayl mazmuni:', data);
    }
});

// Promise bilan (modern usul)
fs.promises.readFile('data.txt', 'utf8')
    .then(data => {
        console.log('Fayl mazmuni:', data);
    })
    .catch(err => {
        console.error('Xato:', err);
    });
```

### Fayl yozish

#### 1. Synxron fayl yozish:
```javascript
const fs = require('fs');

try {
    // Faylga yozish
    fs.writeFileSync('output.txt', 'Salom Dunyo!');
    console.log('Fayl yozildi');
} catch (err) {
    console.error('Xato:', err.message);
}
```

#### 2. Asinxron fayl yozish:
```javascript
const fs = require('fs');

// Callback funksiya bilan
fs.writeFile('output.txt', 'Salom Dunyo!', function(err) {
    if (err) {
        console.error('Xato:', err);
    } else {
        console.log('Fayl yozildi');
    }
});

// Promise bilan
fs.promises.writeFile('output.txt', 'Salom Dunyo!')
    .then(() => {
        console.log('Fayl yozildi');
    })
    .catch(err => {
        console.error('Xato:', err);
    });
```

### Fayl qo'shish (append)

#### Fayl oxiriga qo'shish:
```javascript
const fs = require('fs');

// Fayl oxiriga qo'shish
fs.appendFile('log.txt', '\nYangi xabar: ' + new Date(), function(err) {
    if (err) {
        console.error('Xato:', err);
    } else {
        console.log('Xabar qo\'shildi');
    }
});
```

### Fayl va papka mavjudligini tekshirish

#### Fayl mavjudligini tekshirish:
```javascript
const fs = require('fs');

// Fayl mavjudligini tekshirish
fs.access('data.txt', fs.constants.F_OK, function(err) {
    if (err) {
        console.log('Fayl mavjud emas');
    } else {
        console.log('Fayl mavjud');
    }
});

// Yoki stat() funksiyasi
fs.stat('data.txt', function(err, stats) {
    if (err) {
        console.log('Fayl mavjud emas');
    } else {
        console.log('Fayl mavjud');
        console.log('Hajmi:', stats.size, 'bayt');
        console.log('Yaratilgan:', stats.birthtime);
    }
});
```

### Papkalar bilan ishlash

#### Papka yaratish:
```javascript
const fs = require('fs');

// Papka yaratish
fs.mkdir('yangi-papka', function(err) {
    if (err) {
        console.error('Xato:', err);
    } else {
        console.log('Papka yaratildi');
    }
});

// Ichki papkalar bilan
fs.mkdir('papka1/papka2/papka3', { recursive: true }, function(err) {
    if (err) {
        console.error('Xato:', err);
    } else {
        console.log('Papkalar yaratildi');
    }
});
```

#### Papka mazmunini ko'rish:
```javascript
const fs = require('fs');

// Papka mazmunini ko'rish
fs.readdir('.', function(err, files) {
    if (err) {
        console.error('Xato:', err);
    } else {
        console.log('Fayllar:', files);
    }
});

// Batafsil ma'lumot bilan
fs.readdir('.', function(err, files) {
    if (err) {
        console.error('Xato:', err);
        return;
    }
    
    files.forEach(function(file) {
        fs.stat(file, function(err, stats) {
            if (err) {
                console.error('Xato:', err);
                return;
            }
            
            if (stats.isDirectory()) {
                console.log('Papka:', file);
            } else {
                console.log('Fayl:', file, '(' + stats.size + ' bayt)');
            }
        });
    });
});
```

### Fayl va papka o'chirish

#### Fayl o'chirish:
```javascript
const fs = require('fs');

// Fayl o'chirish
fs.unlink('fayl.txt', function(err) {
    if (err) {
        console.error('Xato:', err);
    } else {
        console.log('Fayl o\'chirildi');
    }
});
```

#### Papka o'chirish:
```javascript
const fs = require('fs');

// Bo'sh papkani o'chirish
fs.rmdir('papka', function(err) {
    if (err) {
        console.error('Xato:', err);
    } else {
        console.log('Papka o\'chirildi');
    }
});

// Ichki papkalar bilan
fs.rmdir('papka', { recursive: true }, function(err) {
    if (err) {
        console.error('Xato:', err);
    } else {
        console.log('Papka va ichidagi hamma narsa o\'chirildi');
    }
});
```

### Fayl ko'chirish va qayta nomlash

#### Fayl ko'chirish:
```javascript
const fs = require('fs');

// Fayl ko'chirish
fs.copyFile('source.txt', 'destination.txt', function(err) {
    if (err) {
        console.error('Xato:', err);
    } else {
        console.log('Fayl ko\'chirildi');
    }
});
```

#### Fayl qayta nomlash:
```javascript
const fs = require('fs');

// Fayl qayta nomlash
fs.rename('eski-nom.txt', 'yangi-nom.txt', function(err) {
    if (err) {
        console.error('Xato:', err);
    } else {
        console.log('Fayl qayta nomlandi');
    }
});
```

### Amaliy misol: Log fayli

#### Server loglari uchun:
```javascript
const fs = require('fs');

function writeLog(message) {
    const timestamp = new Date().toISOString();
    const logMessage = `[${timestamp}] ${message}\n`;
    
    fs.appendFile('server.log', logMessage, function(err) {
        if (err) {
            console.error('Log yozishda xato:', err);
        }
    });
}

// Server da ishlatish
const http = require('http');

const server = http.createServer(function(req, res) {
    // Log yozish
    writeLog(`So'rov: ${req.url}`);
    
    res.writeHead(200, {'Content-Type': 'text/html'});
    res.write('<h1>Salom!</h1>');
    res.end();
});

server.listen(3000, function() {
    writeLog('Server 3000 portda ishga tushdi');
    console.log('Server ishlamoqda');
});
```

### Xulosa

**fs moduli** = Fayllar bilan ishlash uchun asosiy vosita

#### Asosiy funksiyalar:
- **readFile** - fayl o'qish
- **writeFile** - fayl yozish
- **appendFile** - fayl oxiriga qo'shish
- **mkdir** - papka yaratish
- **readdir** - papka mazmunini ko'rish
- **unlink** - fayl o'chirish
- **rmdir** - papka o'chirish

#### Xususiyatlar:
- **Synxron va asinxron** - ikki xil usul
- **Error handling** - xatolarni boshqarish
- **Callback va Promise** - ikki xil usul

fs moduli - fayllar bilan ishlash uchun kuchli vosita!

</details>

<details>
    <summary>Oddiy server yaratish</summary>

## 3.4 Oddiy Server Yaratish

### HTTP moduli

#### HTTP moduli nima?
**HTTP moduli** - Node.js ning web server yaratish moduli. Bu HTTP so'rov va javoblar bilan ishlash imkonini beradi.

#### HTTP modulini import qilish:
```javascript
const http = require('http');
```

### Oddiy HTTP server

#### 1. Asosiy server yaratish:
```javascript
const http = require('http');

// Server yaratish
const server = http.createServer(function(req, res) {
    // Har bir so'rov uchun bu funksiya ishlaydi
    console.log('Yangi so\'rov qabul qilindi');
    
    // Response header
    res.writeHead(200, {'Content-Type': 'text/html'});
    
    // HTML mazmun
    res.write('<h1>Salom Node.js!</h1>');
    res.write('<p>Mening birinchi serverim!</p>');
    
    // Response tugatish
    res.end();
});

// Server ishga tushirish
server.listen(3000, function() {
    console.log('Server http://localhost:3000 da ishlamoqda');
});
```

#### 2. Server ishga tushirish:
```bash
# Terminal da
node server.js

# Natija:
# Server http://localhost:3000 da ishlamoqda
```

#### 3. Brauzerda ko'rish:
1. **Brauzer oching**
2. **http://localhost:3000** yozing
3. **Enter** bosing
4. **"Salom Node.js!"** ko'rasiz

### Server so'rovlari

#### Request obyekti (req):
```javascript
const server = http.createServer(function(req, res) {
    // URL ma'lumotlari
    console.log('URL:', req.url);
    console.log('Method:', req.method);
    console.log('Headers:', req.headers);
    
    // Response
    res.writeHead(200, {'Content-Type': 'text/html'});
    res.write('<h1>So\'rov ma\'lumotlari</h1>');
    res.write(`<p>URL: ${req.url}</p>`);
    res.write(`<p>Method: ${req.method}</p>`);
    res.end();
});
```

#### URL parsing:
```javascript
const http = require('http');
const url = require('url');

const server = http.createServer(function(req, res) {
    // URL ni parse qilish
    const parsedUrl = url.parse(req.url, true);
    console.log('Pathname:', parsedUrl.pathname);
    console.log('Query:', parsedUrl.query);
    
    res.writeHead(200, {'Content-Type': 'text/html'});
    res.write('<h1>URL ma\'lumotlari</h1>');
    res.write(`<p>Pathname: ${parsedUrl.pathname}</p>`);
    res.write(`<p>Query: ${JSON.stringify(parsedUrl.query)}</p>`);
    res.end();
});

server.listen(3000);
```

### Turli route'lar

#### Oddiy routing:
```javascript
const http = require('http');
const url = require('url');

const server = http.createServer(function(req, res) {
    const parsedUrl = url.parse(req.url);
    const pathname = parsedUrl.pathname;
    
    res.writeHead(200, {'Content-Type': 'text/html'});
    
    // Turli yo'llar
    if (pathname === '/') {
        res.write('<h1>Bosh sahifa</h1>');
        res.write('<a href="/about">Biz haqimizda</a><br>');
        res.write('<a href="/contact">Aloqa</a>');
    } else if (pathname === '/about') {
        res.write('<h1>Biz haqimizda</h1>');
        res.write('<p>Bu mening birinchi Node.js serverim</p>');
        res.write('<a href="/">Bosh sahifa</a>');
    } else if (pathname === '/contact') {
        res.write('<h1>Aloqa</h1>');
        res.write('<p>Email: ahmad@example.com</p>');
        res.write('<a href="/">Bosh sahifa</a>');
    } else {
        res.write('<h1>404 - Sahifa topilmadi</h1>');
        res.write('<p>Siz qidirayotgan sahifa mavjud emas</p>');
        res.write('<a href="/">Bosh sahifa</a>');
    }
    
    res.end();
});

server.listen(3000);
```

### Static fayllar

#### HTML fayllarini serve qilish:
```javascript
const http = require('http');
const fs = require('fs');
const path = require('path');

const server = http.createServer(function(req, res) {
    const parsedUrl = url.parse(req.url);
    const pathname = parsedUrl.pathname;
    
    // Fayl yo'lini tuzish
    let filePath = path.join(__dirname, 'public', pathname);
    
    // Agar yo'l bo'sh bo'lsa, index.html ni ko'rsat
    if (pathname === '/') {
        filePath = path.join(__dirname, 'public', 'index.html');
    }
    
    // Faylni o'qish
    fs.readFile(filePath, function(err, data) {
        if (err) {
            // Fayl topilmadi
            res.writeHead(404);
            res.write('<h1>404 - Fayl topilmadi</h1>');
            res.end();
        } else {
            // MIME type aniqlash
            const ext = path.extname(filePath);
            let contentType = 'text/html';
            
            if (ext === '.css') contentType = 'text/css';
            if (ext === '.js') contentType = 'text/javascript';
            if (ext === '.png') contentType = 'image/png';
            
            res.writeHead(200, {'Content-Type': contentType});
            res.write(data);
            res.end();
        }
    });
});

server.listen(3000);
```

### Fayl struktura

#### To'g'ri fayl tuzilishi:
```
my-server/
├── server.js              # Asosiy server fayl
├── public/                # Static fayllar
│   ├── index.html         # Bosh sahifa
│   ├── about.html         # Biz haqimizda
│   ├── css/
│   │   └── style.css      # CSS fayllar
│   ├── js/
│   │   └── script.js      # JavaScript fayllar
│   └── images/            # Rasmlar
└── package.json           # Loyiha ma'lumotlari
```

#### index.html misoli:
```html
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mening Saytim</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <h1>Salom Dunyo!</h1>
    <p>Bu mening birinchi Node.js serverim</p>
    <nav>
        <a href="/">Bosh sahifa</a>
        <a href="/about">Biz haqimizda</a>
        <a href="/contact">Aloqa</a>
    </nav>
    <script src="js/script.js"></script>
</body>
</html>
```

### Server loglari

#### So'rovlarni kuzatish:
```javascript
const http = require('http');
const url = require('url');

const server = http.createServer(function(req, res) {
    const parsedUrl = url.parse(req.url);
    const timestamp = new Date().toISOString();
    
    // Log yozish
    console.log(`[${timestamp}] ${req.method} ${req.url} - ${req.headers['user-agent']}`);
    
    res.writeHead(200, {'Content-Type': 'text/html'});
    res.write('<h1>Salom!</h1>');
    res.end();
});

server.listen(3000, function() {
    console.log('Server ishga tushdi');
    console.log('URL: http://localhost:3000');
    console.log('Loglar ko\'rsatilmoqda...');
});
```

### Xulosa

**Oddiy server** = HTTP moduli bilan web server yaratish

#### Asosiy qismlar:
- **http.createServer()** - server yaratish
- **req** - so'rov ma'lumotlari
- **res** - javob yuborish
- **server.listen()** - portda ishga tushirish

#### Imkoniyatlar:
- **Route'lar** - turli yo'llar
- **Static fayllar** - HTML, CSS, JS
- **Logging** - so'rovlarni kuzatish
- **Error handling** - 404 sahifalar

Oddiy server - web dasturlashning asosidir!

</details>

<details>
    <summary>Error handling (xatoliklarni boshqarish)</summary>

## 3.5 Error Handling (Xatoliklarni Boshqarish)

### Error handling nima?

**Error handling** - dasturda yuzaga keladigan xatolarni boshqarish jarayoni. Bu dasturning barqaror ishlashi uchun juda muhim.

#### Nima uchun kerak?
- **Dastur ishlamay qolmasin** - xato yuz berganda
- **Foydalanuvchi xatoni ko'rsin** - nima bo'lganini bilsin
- **Xatolarni yozib qo'yish** - debug qilish uchun
- **Dasturni barqaror qilish** - ishonchli ishlashi uchun

### JavaScript xatolari

#### 1. Syntax Error (Sintaksis xatosi):
```javascript
// Xato: nuqta-virgul yo'q
let name = 'Ahmad'
console.log(name)

// To'g'ri:
let name = 'Ahmad';
console.log(name);
```

#### 2. Reference Error (Murojaat xatosi):
```javascript
// Xato: o'zgaruvchi aniqlanmagan
console.log(undefinedVariable);

// To'g'ri:
let definedVariable = 'Qiymat';
console.log(definedVariable);
```

#### 3. Type Error (Tur xatosi):
```javascript
// Xato: sonni string sifatida ishlatish
let number = 5;
console.log(number.toUpperCase());

// To'g'ri:
let text = 'Salom';
console.log(text.toUpperCase());
```

### try-catch bloki

#### Asosiy sintaksis:
```javascript
try {
    // Xato yuz berishi mumkin bo'lgan kod
    let result = riskyOperation();
    console.log('Natija:', result);
} catch (error) {
    // Xato yuz berganda ishlaydi
    console.error('Xato yuz berdi:', error.message);
} finally {
    // Har doim ishlaydi
    console.log('Try-catch bloki tugadi');
}
```

#### Amaliy misol:
```javascript
function divideNumbers(a, b) {
    try {
        if (b === 0) {
            throw new Error('Nolga bo\'lish mumkin emas!');
        }
        
        let result = a / b;
        console.log('Natija:', result);
        return result;
        
    } catch (error) {
        console.error('Xato:', error.message);
        return null;
    }
}

// Test qilish
divideNumbers(10, 2);  // 5
divideNumbers(10, 0);  // Xato: Nolga bo'lish mumkin emas!
```

### Node.js da error handling

#### 1. Fayl o'qishda xatolarni boshqarish:
```javascript
const fs = require('fs');

fs.readFile('mavjud-emas.txt', 'utf8', function(err, data) {
    if (err) {
        console.error('Fayl o\'qishda xato:', err.message);
        console.error('Xato kodi:', err.code);
        return;
    }
    
    console.log('Fayl mazmuni:', data);
});
```

#### 2. Server da xatolarni boshqarish:
```javascript
const http = require('http');
const fs = require('fs');

const server = http.createServer(function(req, res) {
    try {
        // Faylni o'qish
        const data = fs.readFileSync('public' + req.url, 'utf8');
        
        res.writeHead(200, {'Content-Type': 'text/html'});
        res.write(data);
        res.end();
        
    } catch (error) {
        // 404 sahifa
        res.writeHead(404, {'Content-Type': 'text/html'});
        res.write('<h1>404 - Sahifa topilmadi</h1>');
        res.write('<p>Qidirayotgan sahifa mavjud emas</p>');
        res.end();
        
        // Xatoni log qilish
        console.error('404 xato:', req.url, error.message);
    }
});

server.listen(3000);
```

### Process xatolari

#### Process xatolarini tutish:
```javascript
// Process xatolarini tutish
process.on('uncaughtException', function(error) {
    console.error('Tutilmagan xato:', error.message);
    console.error('Stack trace:', error.stack);
    
    // Dasturni xavfsiz yopish
    process.exit(1);
});

// Promise xatolarini tutish
process.on('unhandledRejection', function(reason, promise) {
    console.error('Tutilmagan Promise xatosi:', reason);
});

// Dastur yopilganda
process.on('SIGINT', function() {
    console.log('\nDastur yopilmoqda...');
    process.exit(0);
});
```

### Custom error yaratish

#### O'z xato turingizni yaratish:
```javascript
// Custom Error class
class ValidationError extends Error {
    constructor(message, field) {
        super(message);
        this.name = 'ValidationError';
        this.field = field;
    }
}

// Ishlatish
function validateUser(user) {
    if (!user.name) {
        throw new ValidationError('Ism kiritilmagan', 'name');
    }
    
    if (!user.email) {
        throw new ValidationError('Email kiritilmagan', 'email');
    }
    
    if (user.age < 0) {
        throw new ValidationError('Yosh noto\'g\'ri', 'age');
    }
    
    return true;
}

// Test qilish
try {
    validateUser({ name: '', email: 'test@example.com', age: -5 });
} catch (error) {
    if (error instanceof ValidationError) {
        console.error('Validation xatosi:', error.message);
        console.error('Maydon:', error.field);
    } else {
        console.error('Boshqa xato:', error.message);
    }
}
```

### Error logging

#### Xatolarni faylga yozish:
```javascript
const fs = require('fs');

function logError(error, context) {
    const timestamp = new Date().toISOString();
    const logMessage = `[${timestamp}] ${context}: ${error.message}\n${error.stack}\n\n`;
    
    fs.appendFile('error.log', logMessage, function(err) {
        if (err) {
            console.error('Log yozishda xato:', err);
        }
    });
}

// Ishlatish
try {
    // Xato yuz berishi mumkin bo'lgan kod
    riskyOperation();
} catch (error) {
    logError(error, 'riskyOperation');
    console.error('Xato yuz berdi va log ga yozildi');
}
```

### Server error handling

#### To'liq server misoli:
```javascript
const http = require('http');
const fs = require('fs');

const server = http.createServer(function(req, res) {
    try {
        const url = req.url;
        
        // Route handling
        if (url === '/') {
            res.writeHead(200, {'Content-Type': 'text/html'});
            res.write('<h1>Bosh sahifa</h1>');
            res.end();
            
        } else if (url === '/data') {
            // Fayl o'qish
            fs.readFile('data.json', 'utf8', function(err, data) {
                if (err) {
                    res.writeHead(500, {'Content-Type': 'text/html'});
                    res.write('<h1>500 - Server xatosi</h1>');
                    res.write('<p>Ma\'lumotlar fayli topilmadi</p>');
                    res.end();
                    
                    // Xatoni log qilish
                    console.error('Fayl o\'qish xatosi:', err.message);
                    return;
                }
                
                res.writeHead(200, {'Content-Type': 'application/json'});
                res.write(data);
                res.end();
            });
            
        } else {
            // 404 xato
            res.writeHead(404, {'Content-Type': 'text/html'});
            res.write('<h1>404 - Sahifa topilmadi</h1>');
            res.write('<p>Siz qidirayotgan sahifa mavjud emas</p>');
            res.end();
        }
        
    } catch (error) {
        // Umumiy xato
        res.writeHead(500, {'Content-Type': 'text/html'});
        res.write('<h1>500 - Server xatosi</h1>');
        res.write('<p>Kutilmagan xato yuz berdi</p>');
        res.end();
        
        // Xatoni log qilish
        console.error('Server xatosi:', error.message);
        console.error('Stack trace:', error.stack);
    }
});

// Server xatolarini tutish
server.on('error', function(error) {
    console.error('Server xatosi:', error.message);
});

server.listen(3000, function() {
    console.log('Server 3000 portda ishlamoqda');
});
```

### Xulosa

**Error handling** = Dasturda xatolarni boshqarish

#### Asosiy usullar:
- **try-catch** - xatolarni tutish
- **if-else** - shartli tekshirish
- **Process events** - tizim xatolari
- **Custom errors** - o'z xato turlari

#### Maqsadlar:
- **Dastur ishlamay qolmasin** - xato yuz berganda
- **Foydalanuvchi xatoni ko'rsin** - nima bo'lganini bilsin
- **Xatolarni log qilish** - debug qilish uchun
- **Dasturni barqaror qilish** - ishonchli ishlashi uchun

Error handling - professional dasturlashning asosidir!

</details>
