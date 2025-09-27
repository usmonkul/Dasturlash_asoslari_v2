<details>
    <summary>Node.js o'rnatish</summary>

## 2.1 Node.js O'rnatish

### Node.js nima uchun kerak?

**Node.js** - backend dasturlar yozish uchun asosiy dastur. Bu JavaScript kodini serverda ishlatish imkonini beradi.

#### Node.js o'rnatishdan oldin:
- JavaScript faqat brauzerda ishlaydi
- Backend dasturlar yozish mumkin emas
- Server yaratish imkoni yo'q

#### Node.js o'rnatgandan keyin:
- JavaScript ni serverda ishlatish mumkin
- Backend dasturlar yozish mumkin
- Web serverlar yaratish mumkin

### Node.js versiyalari

#### LTS (Long Term Support):
- **Barqaror** - xatolar kam
- **Uzoq muddatli** - 3 yil qo'llab-quvvatlanadi
- **Ishlash uchun** - ishlab chiqish uchun yaxshi

#### Current (Hozirgi):
- **Yangi xususiyatlar** - eng so'nggi imkoniyatlar
- **Eksperimental** - ba'zi xatolar bo'lishi mumkin
- **Test uchun** - yangi narsalarni sinash uchun

### Node.js o'rnatish - Windows

#### 1-qadam: Node.js yuklab olish
1. **nodejs.org** saytiga kiring
2. **"Download for Windows"** tugmasini bosing
3. **LTS versiyasini** tanlang (masalan: 18.17.0)
4. **.msi faylini** yuklab oling

#### 2-qadam: O'rnatish
1. **Yuklab olingan faylni** oching
2. **"Next"** tugmalarini bosing
3. **"I accept the agreement"** belgilang
4. **"Install"** tugmasini bosing
5. **O'rnatish tugagunicha** kuting

#### 3-qadam: Tekshirish
```bash
# Command Prompt oching va yozing:
node --version
npm --version
```

**Natija:**
```
v18.17.0
9.6.7
```

### Node.js o'rnatish - Mac

#### 1-qadam: Homebrew o'rnatish (agar yo'q bo'lsa)
```bash
# Terminal oching va yozing:
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

#### 2-qadam: Node.js o'rnatish
```bash
# Homebrew orqali o'rnatish
brew install node
```

#### 3-qadam: Tekshirish
```bash
node --version
npm --version
```

### Node.js o'rnatish - Linux (Ubuntu)

#### 1-qadam: Paketlar ro'yxatini yangilash
```bash
sudo apt update
```

#### 2-qadam: Node.js o'rnatish
```bash
# Node.js o'rnatish
sudo apt install nodejs npm
```

#### 3-qadam: Tekshirish
```bash
node --version
npm --version
```

### Node.js o'rnatish xatolari

#### Xato: "node is not recognized"
```bash
# Windows da PATH muammosi
# Qayta o'rnatish yoki PATH ni sozlash kerak
```

**Yechim:**
1. Node.js ni qayta o'rnatish
2. Kompyuterni qayta ishga tushirish
3. Command Prompt ni qayta ochish

#### Xato: "Permission denied"
```bash
# Linux/Mac da ruxsat muammosi
sudo npm install -g package-name
```

#### Xato: "EACCES: permission denied"
```bash
# npm global paketlar uchun ruxsat
sudo chown -R $(whoami) ~/.npm
```

### Node.js sozlamalari

#### Global paketlar papkasi
```bash
# Global paketlar qayerda o'rnatiladi
npm config get prefix

# O'zgartirish (ixtiyoriy)
npm config set prefix ~/.npm-global
```

#### Registry o'zgartirish
```bash
# npm registry ko'rish
npm config get registry

# Boshqa registry (ixtiyoriy)
npm config set registry https://registry.npmjs.org/
```

### Node.js versiyasini o'zgartirish

#### nvm (Node Version Manager) o'rnatish

**Windows:**
```bash
# nvm-windows yuklab oling
# https://github.com/coreybutler/nvm-windows
nvm install 18.17.0
nvm use 18.17.0
```

**Mac/Linux:**
```bash
# nvm o'rnatish
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash

# Node.js versiyasini o'zgartirish
nvm install 18.17.0
nvm use 18.17.0
```

### Node.js o'rnatishni tekshirish

#### To'liq tekshirish
```bash
# Node.js versiyasi
node --version

# npm versiyasi
npm --version

# Node.js ma'lumotlari
node -p "process.versions"

# npm sozlamalari
npm config list
```

#### Test dastur
```javascript
// test.js fayl yarating
console.log('Node.js ishlayapti!');
console.log('Versiya:', process.version);
console.log('Platforma:', process.platform);

// Ishga tushirish
node test.js
```

**Natija:**
```
Node.js ishlayapti!
Versiya: v18.17.0
Platforma: win32
```

### Node.js o'rnatish maslahatlari

#### 1. LTS versiyasini tanlang
- Barqaror ishlaydi
- Xatolar kam
- Ko'p dasturchilar ishlatadi

#### 2. Administrator sifatida o'rnating
- Ruxsat muammolari yo'q
- Global paketlar o'rnatish mumkin

#### 3. Antivirus ni o'chiring
- O'rnatish jarayonida muammo bo'lmasin
- Keyin qayta yoqing

#### 4. Internet ulanishini tekshiring
- Node.js yuklab olish uchun kerak
- npm paketlar uchun kerak

### Xulosa

**Node.js o'rnatish** = Backend dasturlashni boshlash uchun birinchi qadam

#### Muvaffaqiyatli o'rnatish:
1. **nodejs.org** dan yuklab olish
2. **LTS versiyasini** tanlash
3. **O'rnatish** jarayonini tugatish
4. **node --version** bilan tekshirish

#### Keyingi qadam:
- npm haqida o'rganish
- VS Code sozlash
- Birinchi dastur yozish

Node.js o'rnatildi! Endi backend dasturlashni boshlash mumkin!

</details>

<details>
    <summary>npm (Node Package Manager) nima?</summary>

## 2.2 npm (Node Package Manager) Nima?

### npm nima?

**npm** - Node.js paketlarini boshqarish dasturi. Bu kutubxonalar, dasturlar va vositalarni o'rnatish va boshqarish uchun ishlatiladi.

#### npm vazifalari:
- **Paketlarni o'rnatish** - kutubxonalar
- **Paketlarni boshqarish** - versiyalar
- **Loyiha yaratish** - package.json
- **Skriptlar yozish** - avtomatlashtirish

### npm nima uchun kerak?

#### Paketlar kutubxonasi:
- **Millionlab paketlar** - Express, React, Vue
- **Tayyor yechimlar** - qayta yozmasdan ishlatish
- **Jamoa ishi** - boshqa dasturchilar kodi
- **Tez rivojlanish** - noldan yozmasdan

#### Misol:
```javascript
// npm siz (qiyin):
// HTTP server yozish - 100+ qator kod

// npm bilan (oson):
const express = require('express');
const app = express();
app.get('/', (req, res) => res.send('Salom!'));
app.listen(3000);
```

### npm paketlari

#### Mahalliy paketlar (Local):
```bash
# Loyiha papkasida o'rnatish
npm install express
```

**Natija:**
```
project/
├── node_modules/     # Paketlar papkasi
│   └── express/
├── package.json      # Loyiha ma'lumotlari
└── server.js
```

#### Global paketlar (Global):
```bash
# Butun kompyuterga o'rnatish
npm install -g nodemon
```

**Natija:**
- Har qayerda ishlatish mumkin
- Command line vositalar
- Masalan: `nodemon server.js`

### package.json fayli

#### package.json nima?
**package.json** - loyiha haqida ma'lumotlar fayli. Bu loyihangizning "passporti".

#### package.json yaratish:
```bash
# Yangi loyiha uchun
npm init

# Avtomatik yaratish
npm init -y
```

#### package.json misoli:
```json
{
  "name": "mening-loyiham",
  "version": "1.0.0",
  "description": "Mening birinchi Node.js loyiham",
  "main": "server.js",
  "scripts": {
    "start": "node server.js",
    "dev": "nodemon server.js"
  },
  "dependencies": {
    "express": "^4.18.2"
  },
  "author": "Ahmad",
  "license": "MIT"
}
```

#### package.json qismlari:
- **name** - loyiha nomi
- **version** - versiya
- **description** - tavsif
- **main** - asosiy fayl
- **scripts** - buyruqlar
- **dependencies** - kerakli paketlar

### npm buyruqlari

#### Paketlarni o'rnatish:
```bash
# Oddiy o'rnatish
npm install express

# Qisqartma
npm i express

# Versiya bilan
npm install express@4.18.2

# Development uchun
npm install --save-dev nodemon

# Global o'rnatish
npm install -g nodemon
```

#### Paketlarni ko'rish:
```bash
# O'rnatilgan paketlar
npm list

# Global paketlar
npm list -g

# Faqat asosiy paketlar
npm list --depth=0
```

#### Paketlarni yangilash:
```bash
# Barcha paketlarni yangilash
npm update

# Biror paketni yangilash
npm update express

# Eng so'nggi versiyaga
npm install express@latest
```

#### Paketlarni o'chirish:
```bash
# Paketni o'chirish
npm uninstall express

# Global paketni o'chirish
npm uninstall -g nodemon
```

### npm skriptlar

#### package.json da skriptlar:
```json
{
  "scripts": {
    "start": "node server.js",
    "dev": "nodemon server.js",
    "test": "jest",
    "build": "webpack"
  }
}
```

#### Skriptlarni ishga tushirish:
```bash
# npm run bilan
npm run start
npm run dev
npm run test

# start va test uchun npm qisqartma
npm start
npm test
```

#### Skriptlar misoli:
```json
{
  "scripts": {
    "start": "node server.js",
    "dev": "nodemon server.js",
    "build": "mkdir build && cp *.js build/",
    "clean": "rm -rf build/"
  }
}
```

### npm xatolari va yechimlari

#### Xato: "npm ERR! EACCES: permission denied"
```bash
# Global paketlar uchun ruxsat
sudo chown -R $(whoami) ~/.npm
```

#### Xato: "npm ERR! network timeout"
```bash
# Registry o'zgartirish
npm config set registry https://registry.npmjs.org/

# Proxy sozlash (agar kerak bo'lsa)
npm config set proxy http://proxy.company.com:8080
```

#### Xato: "npm ERR! peer dep missing"
```bash
# Peer dependencies ni o'rnatish
npm install --save peer-package-name
```

### npm maslahatlari

#### 1. package-lock.json ni saqlang
- Versiyalarni qulflaydi
- Jamoa bilan bir xil versiyalar
- Git ga qo'shing

#### 2. node_modules ni ignore qiling
```gitignore
# .gitignore faylida
node_modules/
*.log
.env
```

#### 3. Semantic versioning
```json
{
  "dependencies": {
    "express": "^4.18.2",  // 4.x.x versiyalar
    "lodash": "~4.17.21",  // 4.17.x versiyalar
    "moment": "2.29.4"     // aniq versiya
  }
}
```

#### 4. npm audit
```bash
# Xavfsizlik tekshirish
npm audit

# Xavfsizlik tuzatish
npm audit fix
```

### npm vs boshqa package managerlar

| Xususiyat | npm | yarn | pnpm |
|-----------|-----|------|------|
| **Tezlik** | O'rta | Tez | Juda tez |
| **Xotira** | Ko'p | O'rta | Kam |
| **Paketlar** | Ko'p | Ko'p | Ko'p |
| **O'rganish** | Oson | Oson | Oson |

### Xulosa

**npm** = Node.js paketlarini boshqarish dasturi

#### Asosiy buyruqlar:
- `npm install` - paket o'rnatish
- `npm init` - loyiha yaratish
- `npm run` - skript ishga tushirish
- `npm update` - yangilash

#### package.json:
- Loyiha ma'lumotlari
- Kerakli paketlar
- Skriptlar
- Versiya boshqaruvi

npm - backend dasturlash uchun eng muhim vosita!

</details>

<details>
    <summary>VS Code sozlash</summary>

## 2.3 VS Code Sozlash

### VS Code nima?

**VS Code (Visual Studio Code)** - Microsoft tomonidan yaratilgan bepul kod editori. Bu dasturlash uchun eng yaxshi vositalardan biri.

#### VS Code afzalliklari:
- **Bepul** - pul to'lash shart emas
- **Tez** - yengil va tez ishlaydi
- **Kengaytiriladi** - ko'p pluginlar
- **Ko'p tillar** - JavaScript, Python, Java
- **Git integratsiyasi** - versiya boshqaruvi

### VS Code o'rnatish

#### 1-qadam: Yuklab olish
1. **code.visualstudio.com** saytiga kiring
2. **"Download for Windows"** tugmasini bosing
3. **.exe faylini** yuklab oling

#### 2-qadam: O'rnatish
1. **Yuklab olingan faylni** oching
2. **"I accept the agreement"** belgilang
3. **"Next"** tugmalarini bosing
4. **"Install"** tugmasini bosing

#### 3-qadam: Ishga tushirish
- **Desktop** da VS Code ikonkasi paydo bo'ladi
- **Birinchi marta** ochishda sozlamalar so'raladi

### VS Code asosiy sozlamalari

#### 1. Til o'zgartirish
1. **Ctrl + Shift + P** (Windows) yoki **Cmd + Shift + P** (Mac)
2. **"Configure Display Language"** yozing
3. **"Install additional languages"** tanlang
4. **O'zbek tili** yoki **English** tanlang

#### 2. Tema o'zgartirish
1. **Ctrl + K, Ctrl + T** (Windows) yoki **Cmd + K, Cmd + T** (Mac)
2. **Tema tanlang:**
   - **Light** - oq fon
   - **Dark** - qora fon
   - **High Contrast** - yuqori kontrast

#### 3. Font o'lchami
1. **Ctrl + ,** (Windows) yoki **Cmd + ,** (Mac)
2. **"Font Size"** qidiring
3. **O'lchamni o'zgartiring** (masalan: 16)

### Node.js uchun kerakli pluginlar

#### 1. JavaScript (ES6) code snippets
```bash
# Plugin nomi: JavaScript (ES6) code snippets
# Muallif: charalampos karypidis
```

**Nima beradi:**
- JavaScript kodlarini tez yozish
- Snippetlar (qisqartmalar)
- Syntax highlighting

#### 2. Node.js Extension Pack
```bash
# Plugin nomi: Node.js Extension Pack
# Muallif: Microsoft
```

**Nima beradi:**
- Node.js debugging
- npm scripts
- IntelliSense
- Code snippets

#### 3. Prettier - Code formatter
```bash
# Plugin nomi: Prettier - Code formatter
# Muallif: Prettier
```

**Nima beradi:**
- Kodni chiroyli qilish
- Avtomatik formatlash
- Konsistent kod

#### Plugin o'rnatish:
1. **Extensions** panelini oching (Ctrl + Shift + X)
2. **Plugin nomini** qidiring
3. **"Install"** tugmasini bosing
4. **VS Code ni qayta ishga tushiring**

### VS Code foydali sozlamalari

#### settings.json fayli:
```json
{
  "editor.fontSize": 16,
  "editor.tabSize": 2,
  "editor.insertSpaces": true,
  "editor.wordWrap": "on",
  "editor.minimap.enabled": true,
  "editor.formatOnSave": true,
  "files.autoSave": "afterDelay",
  "terminal.integrated.fontSize": 14
}
```

#### Sozlamalarni o'zgartirish:
1. **Ctrl + ,** (Windows) yoki **Cmd + ,** (Mac)
2. **JSON faylni ochish** - o'ng burchakda
3. **settings.json** ni tahrirlash

### VS Code terminal

#### Terminal ochish:
- **Ctrl + `** (backtick)
- **View → Terminal**
- **Terminal → New Terminal**

#### Terminal sozlamalari:
```json
{
  "terminal.integrated.fontSize": 14,
  "terminal.integrated.fontFamily": "Consolas",
  "terminal.integrated.shell.windows": "cmd.exe"
}
```

#### Terminal buyruqlari:
```bash
# Fayl ro'yxati
dir          # Windows
ls           # Mac/Linux

# Papka o'zgartirish
cd folder-name

# Yangi papka
mkdir folder-name

# Fayl yaratish
echo. > filename.js    # Windows
touch filename.js      # Mac/Linux
```

### VS Code fayl boshqaruvi

#### Explorer paneli:
- **Ctrl + Shift + E** - Explorer ochish
- **Fayllar va papkalar** ko'rish
- **Yangi fayl/papka** yaratish

#### Fayl yaratish:
1. **Explorer** da o'ng tugma
2. **"New File"** yoki **"New Folder"**
3. **Nom berish**

#### Faylni ochish:
- **Ctrl + O** - fayl ochish
- **Ctrl + Shift + O** - tez ochish
- **Drag & Drop** - sudrab tashlash

### VS Code kod yozish yordamchilari

#### IntelliSense:
- **Avtomatik to'ldirish** - kod yozishda
- **Funktsiya ma'lumotlari** - parametrlar
- **Xatolarni ko'rsatish** - syntax xatolari

#### Snippetlar:
```javascript
// clg yozib Tab bosish
console.log();

// for yozib Tab bosish
for (let i = 0; i < array.length; i++) {
    const element = array[i];
}

// fn yozib Tab bosish
function name() {
    
}
```

#### Emmet (HTML/CSS):
```html
<!-- div yozib Tab bosish -->
<div></div>

<!-- .class yozib Tab bosish -->
<div class="class"></div>

<!-- #id yozib Tab bosish -->
<div id="id"></div>
```

### VS Code debugging

#### Node.js debugging:
1. **Fayl oching** (server.js)
2. **Breakpoint qo'ying** (qator yonida nuqta)
3. **F5** bosib debugging boshlang
4. **Variables** ni ko'rish

#### launch.json sozlamasi:
```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "type": "node",
      "request": "launch",
      "name": "Launch Program",
      "program": "${workspaceFolder}/server.js"
    }
  ]
}
```

### VS Code foydali kalitlar

#### Asosiy kalitlar:
- **Ctrl + S** - saqlash
- **Ctrl + Z** - qaytarish
- **Ctrl + Y** - qayta qilish
- **Ctrl + C** - nusxa olish
- **Ctrl + V** - qo'yish
- **Ctrl + X** - kesish

#### Kod bilan ishlash:
- **Ctrl + /** - izoh qo'shish
- **Ctrl + Shift + /** - blok izoh
- **Ctrl + D** - so'zni tanlash
- **Ctrl + Shift + K** - qatorni o'chirish
- **Alt + Up/Down** - qatorni ko'tarish/tushirish

#### Fayl bilan ishlash:
- **Ctrl + N** - yangi fayl
- **Ctrl + W** - faylni yopish
- **Ctrl + Tab** - fayllar o'rtasida o'tish
- **Ctrl + P** - tez fayl ochish

### VS Code workspace

#### Workspace nima?
**Workspace** - loyiha papkasi. Bu barcha fayllaringiz bir joyda.

#### Workspace yaratish:
1. **File → Open Folder**
2. **Loyiha papkasini** tanlang
3. **VS Code** papkani ochadi

#### Workspace saqlash:
1. **File → Save Workspace As**
2. **.code-workspace** fayl yaratadi
3. **Keyingi safar** ochish uchun

### Xulosa

**VS Code** = Dasturlash uchun eng yaxshi editor

#### Asosiy sozlamalar:
- **Pluginlar o'rnatish** - JavaScript, Node.js
- **Terminal sozlash** - buyruqlar uchun
- **Tema va font** - ko'rish uchun
- **Debugging** - xatolarni topish uchun

#### Foydali xususiyatlar:
- **IntelliSense** - avtomatik to'ldirish
- **Snippetlar** - tez kod yozish
- **Git integratsiyasi** - versiya boshqaruvi
- **Terminal** - buyruqlar uchun

VS Code tayyor! Endi dasturlashni boshlash mumkin!

</details>

<details>
    <summary>Terminal/Command Prompt bilan ishlash</summary>

## 2.4 Terminal/Command Prompt bilan Ishlash

### Terminal nima?

**Terminal** (yoki **Command Prompt** Windows da) - kompyuterga matn orqali buyruq berish dasturi. Bu grafik interfeys bo'lmagan, faqat matn.

#### Terminal nima uchun kerak?
- **Fayllar bilan ishlash** - yaratish, o'chirish, ko'chirish
- **Dasturlarni ishga tushirish** - Node.js, npm
- **Papkalar bilan ishlash** - o'tish, yaratish
- **Git buyruqlari** - versiya boshqaruvi

### Windows Command Prompt

#### Command Prompt ochish:
1. **Windows + R** bosib
2. **"cmd"** yozib **Enter**
3. Yoki **Start** da **"cmd"** qidirish

#### Asosiy buyruqlar:
```cmd
# Hozirgi papkani ko'rish
dir

# Papka o'zgartirish
cd folder-name

# Yuqori papkaga chiqish
cd ..

# Yangi papka yaratish
mkdir folder-name

# Fayl yaratish
echo. > filename.txt

# Fayl mazmunini ko'rish
type filename.txt

# Faylni o'chirish
del filename.txt

# Papkani o'chirish
rmdir folder-name
```

#### Command Prompt misollari:
```cmd
# Hozirgi joy
C:\Users\Ahmad>

# Papka ichiga kirish
C:\Users\Ahmad> cd Documents
C:\Users\Ahmad\Documents>

# Yangi papka yaratish
C:\Users\Ahmad\Documents> mkdir my-project
C:\Users\Ahmad\Documents> cd my-project
C:\Users\Ahmad\Documents\my-project>

# Fayl yaratish
C:\Users\Ahmad\Documents\my-project> echo. > server.js
```

### Mac/Linux Terminal

#### Terminal ochish:
- **Mac:** **Cmd + Space**, **"Terminal"** yozish
- **Linux:** **Ctrl + Alt + T**

#### Asosiy buyruqlar:
```bash
# Hozirgi papkani ko'rish
ls

# Batafsil ko'rish
ls -l

# Yashirin fayllar bilan
ls -la

# Papka o'zgartirish
cd folder-name

# Yuqori papkaga chiqish
cd ..

# Uy papkasiga o'tish
cd ~

# Yangi papka yaratish
mkdir folder-name

# Fayl yaratish
touch filename.txt

# Fayl mazmunini ko'rish
cat filename.txt

# Faylni o'chirish
rm filename.txt

# Papkani o'chirish
rmdir folder-name

# Papka va ichidagi hamma narsani o'chirish
rm -rf folder-name
```

### Node.js bilan ishlash

#### Node.js dasturini ishga tushirish:
```bash
# JavaScript faylini ishga tushirish
node server.js

# Fayl mazmunini ko'rsatish
node -e "console.log('Salom Node.js!')"

# Node.js versiyasini ko'rish
node --version
```

#### npm buyruqlari:
```bash
# Paket o'rnatish
npm install express

# Global paket o'rnatish
npm install -g nodemon

# Skript ishga tushirish
npm run start
npm start

# O'rnatilgan paketlarni ko'rish
npm list

# Paket o'chirish
npm uninstall express
```

### Fayl va papka boshqaruvi

#### Fayl yaratish:
```bash
# Windows
echo. > server.js
echo console.log('Salom!'); > server.js

# Mac/Linux
touch server.js
echo "console.log('Salom!');" > server.js
```

#### Fayl mazmunini ko'rish:
```bash
# Windows
type server.js

# Mac/Linux
cat server.js
```

#### Faylni tahrirlash:
```bash
# VS Code da ochish
code server.js

# Nano editor (Linux/Mac)
nano server.js

# Vim editor (Linux/Mac)
vi server.js
```

#### Fayllarni ko'chirish:
```bash
# Windows
copy file1.js file2.js
move file1.js folder/

# Mac/Linux
cp file1.js file2.js
mv file1.js folder/
```

### Terminal sozlamalari

#### Ranglar va ko'rinish:
```bash
# Windows (PowerShell)
# Ranglar avtomatik

# Mac/Linux
# .bashrc yoki .zshrc faylida
export PS1="\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]\$ "
```

#### Aliaslar (qisqartmalar):
```bash
# .bashrc yoki .zshrc faylida
alias ll='ls -la'
alias la='ls -A'
alias l='ls -CF'
alias ..='cd ..'
alias ...='cd ../..'

# Node.js uchun
alias ni='npm install'
alias ns='npm start'
alias nt='npm test'
```

### Terminal maslahatlari

#### 1. Tab completion
- **Tab** tugmasini bosib buyruqlarni to'ldirish
- Fayl va papka nomlarini avtomatik yozish

#### 2. Buyruq tarixi
- **↑/↓** tugmalari bilan oldingi buyruqlarni ko'rish
- **history** buyruqi bilan barcha buyruqlarni ko'rish

#### 3. Fayl yo'llari
```bash
# Mutlaq yo'l
C:\Users\Ahmad\Documents\project\server.js    # Windows
/home/ahmad/documents/project/server.js       # Linux
/Users/ahmad/documents/project/server.js      # Mac

# Nisbiy yo'l
./server.js          # Hozirgi papkada
../config/db.js      # Yuqori papkada
```

#### 4. Wildcards
```bash
# Barcha .js fayllar
*.js

# server bilan boshlanuvchi fayllar
server*

# .txt bilan tugaydigan fayllar
*.txt
```

### Xulosa

**Terminal** = Kompyuterga matn orqali buyruq berish

#### Asosiy buyruqlar:
- **dir/ls** - fayllarni ko'rish
- **cd** - papka o'zgartirish
- **mkdir** - papka yaratish
- **echo/touch** - fayl yaratish

#### Node.js uchun:
- **node** - JavaScript ishga tushirish
- **npm** - paketlar boshqaruvi
- **code** - VS Code da ochish

Terminal - dasturchining eng muhim vositasidir!

</details>

<details>
    <summary>Birinchi Node.js dasturini ishga tushirish</summary>

## 2.5 Birinchi Node.js Dasturini Ishga Tushirish

### Birinchi dastur yaratish

#### 1-qadam: Papka yaratish
```bash
# Terminal oching
mkdir my-first-node-app
cd my-first-node-app
```

#### 2-qadam: package.json yaratish
```bash
# package.json yaratish
npm init -y
```

**Natija:**
```json
{
  "name": "my-first-node-app",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC"
}
```

#### 3-qadam: Birinchi JavaScript fayl
```javascript
// server.js fayl yarating
console.log('Salom Node.js!');
console.log('Mening birinchi dasturim!');
```

#### 4-qadam: Dasturni ishga tushirish
```bash
# Dasturni ishga tushirish
node server.js
```

**Natija:**
```
Salom Node.js!
Mening birinchi dasturim!
```

### Oddiy web server yaratish

#### server.js fayli:
```javascript
// HTTP modulini import qilish
const http = require('http');

// Server yaratish
const server = http.createServer(function(req, res) {
    // Response header
    res.writeHead(200, {'Content-Type': 'text/html; charset=utf-8'});
    
    // HTML mazmun
    res.write('<h1>Salom Node.js!</h1>');
    res.write('<p>Mening birinchi web serverim!</p>');
    res.write('<p>Port: 3000</p>');
    
    // Response tugatish
    res.end();
});

// Server ishga tushirish
server.listen(3000, function() {
    console.log('Server http://localhost:3000 da ishlamoqda');
    console.log('Brauzerda oching: http://localhost:3000');
});
```

#### Dasturni ishga tushirish:
```bash
# Server ishga tushirish
node server.js
```

#### Brauzerda ko'rish:
1. **Brauzer oching**
2. **http://localhost:3000** yozing
3. **Enter** bosing
4. **"Salom Node.js!"** ko'rasiz

### Express.js bilan server

#### 1-qadam: Express o'rnatish
```bash
# Express paketini o'rnatish
npm install express
```

#### 2-qadam: Express server yaratish
```javascript
// server.js
const express = require('express');
const app = express();

// Route yaratish
app.get('/', function(req, res) {
    res.send('<h1>Salom Express.js!</h1>');
});

app.get('/about', function(req, res) {
    res.send('<h1>Biz haqimizda</h1><p>Bu mening birinchi Express serverim</p>');
});

// Server ishga tushirish
app.listen(3000, function() {
    console.log('Express server http://localhost:3000 da ishlamoqda');
});
```

#### 3-qadam: package.json ni yangilash
```json
{
  "name": "my-first-node-app",
  "version": "1.0.0",
  "description": "Mening birinchi Node.js loyiham",
  "main": "server.js",
  "scripts": {
    "start": "node server.js",
    "dev": "nodemon server.js"
  },
  "dependencies": {
    "express": "^4.18.2"
  }
}
```

#### 4-qadam: Skriptlar bilan ishga tushirish
```bash
# npm start bilan
npm start

# yoki to'g'ridan-to'g'ri
node server.js
```

### Fayl struktura

#### To'g'ri fayl tuzilishi:
```
my-first-node-app/
├── node_modules/          # npm paketlar
├── package.json          # Loyiha ma'lumotlari
├── package-lock.json     # Versiya qulfi
├── server.js             # Asosiy server fayl
├── public/               # Static fayllar
│   ├── css/
│   ├── js/
│   └── images/
└── README.md             # Loyiha hujjati
```

#### Static fayllar bilan:
```javascript
// server.js
const express = require('express');
const path = require('path');
const app = express();

// Static fayllarni serve qilish
app.use(express.static('public'));

// Route lar
app.get('/', function(req, res) {
    res.sendFile(path.join(__dirname, 'public', 'index.html'));
});

app.listen(3000, function() {
    console.log('Server ishlamoqda!');
});
```

### Xatolarni tuzatish

#### Umumiy xatolar:

#### 1. "Cannot find module 'express'"
```bash
# Express o'rnatilmagan
npm install express
```

#### 2. "Port 3000 is already in use"
```javascript
// Boshqa port ishlatish
app.listen(3001, function() {
    console.log('Server 3001 portda ishlamoqda');
});
```

#### 3. "EADDRINUSE: address already in use"
```bash
# Windows da portni to'xtatish
netstat -ano | findstr :3000
taskkill /PID <PID> /F

# Mac/Linux da
lsof -ti:3000 | xargs kill -9
```

### Development server (nodemon)

#### 1-qadam: nodemon o'rnatish
```bash
# Global o'rnatish
npm install -g nodemon

# yoki development dependency
npm install --save-dev nodemon
```

#### 2-qadam: nodemon bilan ishga tushirish
```bash
# nodemon bilan
nodemon server.js

# yoki npm script
npm run dev
```

#### 3-qadam: Avtomatik qayta ishga tushish
- **Faylni saqlash** - nodemon avtomatik qayta ishga tushiradi
- **Xatolarni ko'rish** - darhol natija
- **Tez rivojlanish** - qayta-qayta ishga tushirish shart emas

### Loyihani test qilish

#### 1. Server ishlamoqdamimi?
```bash
# Terminal da
node server.js
# "Server ishlamoqda" xabari ko'rinishi kerak
```

#### 2. Brauzerda ochilaydimi?
```
http://localhost:3000
# "Salom Express.js!" ko'rinishi kerak
```

#### 3. Route lar ishlaydimi?
```
http://localhost:3000/about
# "Biz haqimizda" sahifasi ko'rinishi kerak
```

### Keyingi qadamlar

#### 1. HTML sahifa yaratish:
```html
<!-- public/index.html -->
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mening Saytim</title>
</head>
<body>
    <h1>Salom Dunyo!</h1>
    <p>Bu mening birinchi Node.js loyiham</p>
</body>
</html>
```

#### 2. CSS qo'shish:
```css
/* public/css/style.css */
body {
    font-family: Arial, sans-serif;
    margin: 40px;
    background-color: #f0f0f0;
}

h1 {
    color: #333;
}
```

#### 3. JavaScript qo'shish:
```javascript
// public/js/script.js
console.log('Frontend JavaScript ishlayapti!');

document.addEventListener('DOMContentLoaded', function() {
    console.log('Sahifa yuklandi!');
});
```

### Xulosa

**Birinchi Node.js dasturi** = Backend dasturlashni boshlash

#### Muvaffaqiyatli ishga tushirish:
1. **Papka yaratish** - loyiha uchun
2. **package.json** - loyiha ma'lumotlari
3. **server.js** - asosiy dastur
4. **node server.js** - ishga tushirish
5. **localhost:3000** - brauzerda ko'rish

#### Keyingi qadamlar:
- **Express.js** - framework o'rganish
- **Routes** - yo'llar yaratish
- **Static fayllar** - HTML, CSS, JS
- **Ma'lumotlar bazasi** - ma'lumotlarni saqlash

Muvaffaqiyat! Sizning birinchi Node.js dasturingiz ishlamoqda!

</details>
