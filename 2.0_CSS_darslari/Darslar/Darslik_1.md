<details>
    <summary>Display xususiyati</summary>

## 6.1 Display Xususiyati

### Display nima?

**Display xususiyati** - elementning qanday ko'rsatilishini belgilaydi. Har bir HTML elementi o'zining default display qiymatiga ega.

### Asosiy display qiymatlari

#### 1. Block - to'liq kenglik
```css
.block-element {
    display: block;
}
```

#### 2. Inline - matn kabi
```css
.inline-element {
    display: inline;
}
```

#### 3. Inline-block - aralash
```css
.inline-block-element {
    display: inline-block;
}
```

#### 4. None - yashirish
```css
.yashirilgan-element {
    display: none;
}
```

### Block elementlar

#### Xususiyatlari:
- To'liq kenglikni egallaydi
- Yangi qatordan boshlanadi
- Kenglik va balandlik o'rnatish mumkin
- Margin va padding ishlaydi

#### Misollar:
```html
<div style="display: block; background-color: lightblue; padding: 10px;">
    Bu block element
</div>

<p style="display: block; background-color: lightgreen; padding: 10px;">
    Bu ham block element
</p>
```

### Inline elementlar

#### Xususiyatlari:
- Faqat kerakli joyni egallaydi
- Boshqa elementlar bilan bir qatorda turadi
- Kenglik va balandlik o'rnatib bo'lmaydi
- Faqat gorizontal margin va padding ishlaydi

#### Misollar:
```html
<span style="display: inline; background-color: yellow; padding: 5px;">
    Bu inline element
</span>

<strong style="display: inline; background-color: orange; padding: 5px;">
    Bu ham inline element
</strong>
```

### Inline-block elementlar

#### Xususiyatlari:
- Inline kabi bir qatorda turadi
- Block kabi kenglik va balandlik o'rnatish mumkin
- Margin va padding to'liq ishlaydi

#### Misollar:
```html
<div style="display: inline-block; width: 100px; height: 50px; background-color: pink; margin: 5px;">
    Inline-block 1
</div>

<div style="display: inline-block; width: 100px; height: 50px; background-color: lightcoral; margin: 5px;">
    Inline-block 2
</div>
```

### Display qiymatlarini o'zgartirish

#### 1. Span ni block qilish
```css
span {
    display: block;
    background-color: lightblue;
    padding: 10px;
    margin: 5px;
}
```

#### 2. Div ni inline qilish
```css
div {
    display: inline;
    background-color: lightgreen;
    padding: 5px;
}
```

#### 3. Elementlarni yashirish
```css
.yashirish {
    display: none;
}
```

### Amaliy misollar

#### 1. Display qiymatlari taqqoslash
```html
<style>
.block-demo {
    display: block;
    background-color: #e3f2fd;
    padding: 15px;
    margin: 5px;
    border: 2px solid #2196f3;
}

.inline-demo {
    display: inline;
    background-color: #f3e5f5;
    padding: 10px;
    margin: 5px;
    border: 2px solid #9c27b0;
}

.inline-block-demo {
    display: inline-block;
    width: 120px;
    height: 60px;
    background-color: #e8f5e8;
    padding: 10px;
    margin: 5px;
    border: 2px solid #4caf50;
    text-align: center;
    line-height: 40px;
}
</style>

<h3>Display qiymatlari</h3>

<h4>Block elementlar:</h4>
<div class="block-demo">Block element 1</div>
<div class="block-demo">Block element 2</div>

<h4>Inline elementlar:</h4>
<span class="inline-demo">Inline 1</span>
<span class="inline-demo">Inline 2</span>
<span class="inline-demo">Inline 3</span>

<h4>Inline-block elementlar:</h4>
<div class="inline-block-demo">Inline-block 1</div>
<div class="inline-block-demo">Inline-block 2</div>
<div class="inline-block-demo">Inline-block 3</div>
```

#### 2. Kartochkalar qatori
```html
<style>
.kartochka {
    display: inline-block;
    width: 150px;
    height: 100px;
    background-color: white;
    border: 2px solid #ddd;
    border-radius: 8px;
    padding: 15px;
    margin: 10px;
    text-align: center;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.kartochka h4 {
    margin: 0 0 10px 0;
    color: #333;
}

.kartochka p {
    margin: 0;
    color: #666;
    font-size: 14px;
}
</style>

<div class="kartochka">
    <h4>Kartochka 1</h4>
    <p>Birinchi kartochka</p>
</div>

<div class="kartochka">
    <h4>Kartochka 2</h4>
    <p>Ikkinchi kartochka</p>
</div>

<div class="kartochka">
    <h4>Kartochka 3</h4>
    <p>Uchinchi kartochka</p>
</div>
```

</details>

<details>
    <summary>Inline va block elementlar</summary>

## 6.2 Inline va Block Elementlar

### Block elementlar ro'yxati

#### HTML block elementlari:
- `<div>` - umumiy konteyner
- `<p>` - paragraf
- `<h1>`, `<h2>`, `<h3>` - sarlavhalar
- `<ul>`, `<ol>` - ro'yxatlar
- `<li>` - ro'yxat elementlari
- `<section>`, `<article>` - maqola bo'limlari
- `<header>`, `<footer>` - sahifa qismlari

#### Block element xususiyatlari:
```css
.block-element {
    display: block;              /* Default qiymat */
    width: 100%;                /* To'liq kenglik */
    margin: 10px 0;             /* Vertikal margin */
    padding: 15px;              /* Ichki bo'shliq */
    background-color: lightblue;
}
```

### Inline elementlar ro'yxati

#### HTML inline elementlari:
- `<span>` - matn qismi
- `<strong>`, `<em>` - matn formatlash
- `<a>` - havola
- `<img>` - rasm
- `<code>` - kod matni
- `<small>` - kichik matn

#### Inline element xususiyatlari:
```css
.inline-element {
    display: inline;             /* Default qiymat */
    padding: 5px;               /* Faqat gorizontal padding */
    margin: 0 5px;              /* Faqat gorizontal margin */
    background-color: lightgreen;
}
```

### Block va inline farqi

#### 1. Kenglik farqi
```html
<style>
.block-farq {
    display: block;
    background-color: #ffeb3b;
    padding: 10px;
    margin: 5px;
}

.inline-farq {
    display: inline;
    background-color: #4caf50;
    padding: 10px;
    margin: 5px;
}
</style>

<h4>Block elementlar (to'liq kenglik):</h4>
<div class="block-farq">Block 1</div>
<div class="block-farq">Block 2</div>

<h4>Inline elementlar (kerakli kenglik):</h4>
<span class="inline-farq">Inline 1</span>
<span class="inline-farq">Inline 2</span>
<span class="inline-farq">Inline 3</span>
```

#### 2. Margin va padding farqi
```html
<style>
.margin-demo {
    background-color: #e1f5fe;
    border: 2px solid #0277bd;
}

.block-margin {
    display: block;
    margin: 20px;
    padding: 15px;
}

.inline-margin {
    display: inline;
    margin: 20px;
    padding: 15px;
}
</style>

<h4>Block element margin:</h4>
<div class="margin-demo block-margin">Block element</div>
<div class="margin-demo block-margin">Block element</div>

<h4>Inline element margin:</h4>
<span class="margin-demo inline-margin">Inline element</span>
<span class="margin-demo inline-margin">Inline element</span>
```

### Display qiymatini o'zgartirish

#### 1. Inline ni block qilish
```css
span {
    display: block;
    width: 200px;
    height: 50px;
    background-color: lightcoral;
    margin: 10px 0;
    text-align: center;
    line-height: 50px;
}
```

#### 2. Block ni inline qilish
```css
div {
    display: inline;
    background-color: lightblue;
    padding: 5px;
    margin: 0 5px;
}
```

### Amaliy misollar

#### 1. Navigatsiya menyu
```html
<style>
.nav-menu {
    background-color: #2c3e50;
    padding: 15px;
}

.nav-menu a {
    display: inline-block;
    color: white;
    text-decoration: none;
    padding: 10px 20px;
    margin: 0 5px;
    background-color: #34495e;
    border-radius: 5px;
    transition: background-color 0.3s ease;
}

.nav-menu a:hover {
    background-color: #3498db;
}
</style>

<nav class="nav-menu">
    <a href="#">Bosh sahifa</a>
    <a href="#">Xizmatlar</a>
    <a href="#">Portfolio</a>
    <a href="#">Aloqa</a>
</nav>
```

#### 2. Matn formatlash
```html
<style>
.matn-formatlash {
    font-size: 18px;
    line-height: 1.6;
}

.matn-formatlash strong {
    display: inline;
    background-color: #ffeb3b;
    padding: 2px 4px;
    font-weight: bold;
}

.matn-formatlash em {
    display: inline;
    background-color: #e8f5e8;
    padding: 2px 4px;
    font-style: italic;
}

.matn-formatlash code {
    display: inline;
    background-color: #f5f5f5;
    padding: 2px 6px;
    border: 1px solid #ddd;
    font-family: monospace;
}
</style>

<div class="matn-formatlash">
    <p>Bu yerda <strong>muhim matn</strong> va <em>qiyin matn</em> mavjud.</p>
    <p>Dasturlashda <code>display: block</code> va <code>display: inline</code> ishlatiladi.</p>
</div>
```

#### 3. Kartochkalar qatori
```html
<style>
.kartochkalar-qatori {
    text-align: center;
    padding: 20px;
}

.kartochka {
    display: inline-block;
    width: 180px;
    height: 120px;
    background-color: white;
    border: 2px solid #e0e0e0;
    border-radius: 10px;
    padding: 20px;
    margin: 10px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    text-align: center;
    vertical-align: top;
}

.kartochka h3 {
    margin: 0 0 10px 0;
    color: #333;
    font-size: 16px;
}

.kartochka p {
    margin: 0;
    color: #666;
    font-size: 14px;
}
</style>

<div class="kartochkalar-qatori">
    <div class="kartochka">
        <h3>HTML</h3>
        <p>Web-sahifa strukturasi</p>
    </div>
    
    <div class="kartochka">
        <h3>CSS</h3>
        <p>Web-sahifa dizayni</p>
    </div>
    
    <div class="kartochka">
        <h3>JavaScript</h3>
        <p>Web-sahifa interaktivligi</p>
    </div>
</div>
```

</details>

<details>
    <summary>Overflow</summary>

## 6.3 Overflow

### Overflow nima?

**Overflow** - element mazmuni uning o'lchamidan katta bo'lganda nima bo'lishini belgilaydi.

### Overflow qiymatlari

#### 1. Visible - ko'rinadi (default)
```css
.visible-overflow {
    overflow: visible;
}
```

#### 2. Hidden - yashiriladi
```css
.hidden-overflow {
    overflow: hidden;
}
```

#### 3. Scroll - scroll qo'shiladi
```css
.scroll-overflow {
    overflow: scroll;
}
```

#### 4. Auto - kerak bo'lsa scroll
```css
.auto-overflow {
    overflow: auto;
}
```

### Gorizontal va vertikal overflow

#### 1. Overflow-x - gorizontal
```css
.gorizontal-overflow {
    overflow-x: scroll;
}
```

#### 2. Overflow-y - vertikal
```css
.vertikal-overflow {
    overflow-y: hidden;
}
```

### Amaliy misollar

#### 1. Overflow qiymatlari taqqoslash
```html
<style>
.overflow-demo {
    width: 200px;
    height: 100px;
    border: 2px solid #333;
    margin: 10px;
    padding: 10px;
    background-color: #f0f0f0;
}

.visible-demo {
    overflow: visible;
}

.hidden-demo {
    overflow: hidden;
}

.scroll-demo {
    overflow: scroll;
}

.auto-demo {
    overflow: auto;
}

.overflow-matn {
    width: 300px;
    height: 80px;
    background-color: #e3f2fd;
    border: 1px solid #2196f3;
    padding: 10px;
    margin: 5px;
}
</style>

<h3>Overflow qiymatlari:</h3>

<div class="overflow-demo visible-demo">
    <h4>Visible (default)</h4>
    <div class="overflow-matn">Bu matn konteyner o'lchamidan katta. U to'liq ko'rinadi.</div>
</div>

<div class="overflow-demo hidden-demo">
    <h4>Hidden</h4>
    <div class="overflow-matn">Bu matn konteyner o'lchamidan katta. Ortiqcha qism yashiriladi.</div>
</div>

<div class="overflow-demo scroll-demo">
    <h4>Scroll</h4>
    <div class="overflow-matn">Bu matn konteyner o'lchamidan katta. Scroll bar ko'rinadi.</div>
</div>

<div class="overflow-demo auto-demo">
    <h4>Auto</h4>
    <div class="overflow-matn">Bu matn konteyner o'lchamidan katta. Kerak bo'lsa scroll ko'rinadi.</div>
</div>
```

#### 2. Rasm overflow
```html
<style>
.rasm-konteyner {
    width: 250px;
    height: 150px;
    border: 3px solid #333;
    margin: 10px;
    background-color: #f8f9fa;
}

.rasm-konteyner img {
    width: 400px;
    height: 300px;
}

.overflow-hidden {
    overflow: hidden;
}

.overflow-scroll {
    overflow: scroll;
}
</style>

<h3>Rasm overflow:</h3>

<div class="rasm-konteyner overflow-hidden">
    <img src="https://via.placeholder.com/400x300/4CAF50/white?text=Katta+Rasm" alt="Katta rasm">
</div>

<div class="rasm-konteyner overflow-scroll">
    <img src="https://via.placeholder.com/400x300/2196F3/white?text=Katta+Rasm" alt="Katta rasm">
</div>
```

#### 3. Matn qutisi
```html
<style>
.matn-qutisi {
    width: 300px;
    height: 200px;
    border: 2px solid #4caf50;
    border-radius: 8px;
    padding: 15px;
    margin: 20px;
    background-color: white;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
}

.matn-qutisi h3 {
    margin: 0 0 15px 0;
    color: #2e7d32;
}

.matn-qutisi .matn-mazmuni {
    overflow-y: auto;
    height: 120px;
    line-height: 1.5;
    color: #333;
}

.matn-qutisi .matn-mazmuni::-webkit-scrollbar {
    width: 8px;
}

.matn-qutisi .matn-mazmuni::-webkit-scrollbar-track {
    background: #f1f1f1;
    border-radius: 4px;
}

.matn-qutisi .matn-mazmuni::-webkit-scrollbar-thumb {
    background: #4caf50;
    border-radius: 4px;
}
</style>

<div class="matn-qutisi">
    <h3>Uzun matn</h3>
    <div class="matn-mazmuni">
        <p>Bu yerda juda uzun matn yozilgan. Bu matn konteyner balandligidan ko'proq joy egallaydi. Overflow: auto tufayli vertikal scroll ko'rinadi.</p>
        
        <p>CSS overflow xususiyati element mazmuni uning o'lchamidan katta bo'lganda qanday ishlashini belgilaydi. Bu juda foydali xususiyat.</p>
        
        <p>Overflow ning asosiy qiymatlari: visible, hidden, scroll va auto. Har biri o'zining vazifasiga ega.</p>
        
        <p>Visible - mazmun to'liq ko'rinadi, hatto konteyner o'lchamidan tashqariga chiqsa ham.</p>
        
        <p>Hidden - ortiqcha mazmun yashiriladi va ko'rinmaydi.</p>
        
        <p>Scroll - doimo scroll bar ko'rinadi.</p>
        
        <p>Auto - kerak bo'lganda scroll bar paydo bo'ladi.</p>
    </div>
</div>
```

</details>

<details>
    <summary>Oddiy layout yaratish</summary>

## 6.4 Oddiy Layout Yaratish

### Layout nima?

**Layout** - web-sahifadagi elementlarning joylashuvini va tartibini belgilaydi. Yaxshi layout foydalanuvchiga qulay bo'ladi.

### Asosiy layout elementlari

#### 1. Header - sahifa boshi
```html
<header>
    <h1>Sahifa sarlavhasi</h1>
    <nav>Navigatsiya menyu</nav>
</header>
```

#### 2. Main - asosiy mazmun
```html
<main>
    <article>Asosiy maqola</article>
    <aside>Yon panel</aside>
</main>
```

#### 3. Footer - sahifa oyog'i
```html
<footer>
    <p>Copyright ma'lumotlari</p>
</footer>
```

### Oddiy sahifa struktura

#### 1. Asosiy HTML struktura
```html
<!DOCTYPE html>
<html>
<head>
    <title>Oddiy Layout</title>
</head>
<body>
    <header>Bosh qism</header>
    <main>Asosiy mazmun</main>
    <footer>Pastki qism</footer>
</body>
</html>
```

#### 2. CSS stil
```css
header {
    background-color: #333;
    color: white;
    padding: 20px;
    text-align: center;
}

main {
    padding: 20px;
    min-height: 400px;
}

footer {
    background-color: #333;
    color: white;
    padding: 15px;
    text-align: center;
}
```

### Ikki ustunli layout

#### 1. HTML struktura
```html
<div class="konteyner">
    <div class="chap-ustun">
        <h2>Chap ustun</h2>
        <p>Chap ustun mazmuni</p>
    </div>
    
    <div class="o_ng-ustun">
        <h2>O'ng ustun</h2>
        <p>O'ng ustun mazmuni</p>
    </div>
</div>
```

#### 2. CSS stillar
```css
.konteyner {
    display: flex;
    max-width: 1000px;
    margin: 0 auto;
}

.chap-ustun {
    flex: 1;
    background-color: #f8f9fa;
    padding: 20px;
    margin-right: 10px;
}

.o_ng-ustun {
    flex: 2;
    background-color: #e9ecef;
    padding: 20px;
    margin-left: 10px;
}
```

### Amaliy misollar

#### 1. Oddiy sahifa layout
```html
<style>
.oddiy-sahifa {
    max-width: 800px;
    margin: 0 auto;
    font-family: Arial, sans-serif;
}

.sahifa-header {
    background-color: #2c3e50;
    color: white;
    padding: 20px;
    text-align: center;
}

.sahifa-header h1 {
    margin: 0;
    font-size: 2em;
}

.sahifa-main {
    padding: 30px 20px;
    background-color: white;
    min-height: 400px;
}

.sahifa-main h2 {
    color: #2c3e50;
    border-bottom: 2px solid #3498db;
    padding-bottom: 10px;
}

.sahifa-footer {
    background-color: #34495e;
    color: white;
    padding: 15px;
    text-align: center;
}
</style>

<div class="oddiy-sahifa">
    <header class="sahifa-header">
        <h1>Mening Web-sahifam</h1>
        <p>CSS Layout asoslari</p>
    </header>
    
    <main class="sahifa-main">
        <h2>Asosiy mazmun</h2>
        <p>Bu yerda sahifaning asosiy mazmuni joylashadi. CSS layout yordamida elementlar chiroyli tartibda joylashtiriladi.</p>
        
        <h3>Layout elementlari:</h3>
        <ul>
            <li>Header - sahifa boshi</li>
            <li>Main - asosiy mazmun</li>
            <li>Footer - sahifa oyog'i</li>
        </ul>
    </main>
    
    <footer class="sahifa-footer">
        <p>&copy; 2024 Mening Web-sahifam</p>
    </footer>
</div>
```

#### 2. Kartochkalar layout
```html
<style>
.kartochkalar-layout {
    max-width: 900px;
    margin: 20px auto;
    padding: 20px;
}

.kartochka {
    display: inline-block;
    width: 250px;
    background-color: white;
    border: 2px solid #e0e0e0;
    border-radius: 10px;
    padding: 20px;
    margin: 15px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    vertical-align: top;
}

.kartochka h3 {
    color: #2c3e50;
    margin: 0 0 15px 0;
    font-size: 1.3em;
}

.kartochka p {
    color: #666;
    line-height: 1.5;
    margin: 0;
}

.kartochka .rang-1 {
    border-left: 4px solid #e74c3c;
}

.kartochka .rang-2 {
    border-left: 4px solid #3498db;
}

.kartochka .rang-3 {
    border-left: 4px solid #2ecc71;
}
</style>

<div class="kartochkalar-layout">
    <div class="kartochka rang-1">
        <h3>HTML</h3>
        <p>HTML web-sahifalarning asosini tashkil qiladi. U sahifa strukturasi va mazmunini belgilaydi.</p>
    </div>
    
    <div class="kartochka rang-2">
        <h3>CSS</h3>
        <p>CSS web-sahifalarni chiroyli qiladi. Ranglar, shriftlar va layout CSS orqali amalga oshiriladi.</p>
    </div>
    
    <div class="kartochka rang-3">
        <h3>JavaScript</h3>
        <p>JavaScript web-sahifalarni interaktiv qiladi. Foydalanuvchi harakatlariga javob beradi.</p>
    </div>
</div>
```

#### 3. Ikki ustunli layout
```html
<style>
.ikki-ustun-layout {
    max-width: 1000px;
    margin: 20px auto;
    display: flex;
    gap: 20px;
    padding: 0 20px;
}

.asosiy-ustun {
    flex: 2;
    background-color: white;
    padding: 25px;
    border: 1px solid #e0e0e0;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.yon-ustun {
    flex: 1;
    background-color: #f8f9fa;
    padding: 25px;
    border: 1px solid #e0e0e0;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.asosiy-ustun h2,
.yon-ustun h3 {
    color: #2c3e50;
    margin-top: 0;
}

.yon-ustun ul {
    list-style: none;
    padding: 0;
}

.yon-ustun li {
    padding: 8px 0;
    border-bottom: 1px solid #e0e0e0;
}

.yon-ustun a {
    color: #3498db;
    text-decoration: none;
}

.yon-ustun a:hover {
    text-decoration: underline;
}
</style>

<div class="ikki-ustun-layout">
    <div class="asosiy-ustun">
        <h2>Asosiy maqola</h2>
        <p>Bu yerda asosiy maqola mazmuni joylashadi. U keng joy egallaydi va foydalanuvchining diqqat markazida bo'ladi.</p>
        
        <h3>CSS Layout haqida</h3>
        <p>CSS layout web-sahifadagi elementlarning joylashuvini boshqarish uchun ishlatiladi. Display, overflow va boshqa xususiyatlar yordamida chiroyli sahifalar yaratish mumkin.</p>
        
        <p>Layout yaratishda quyidagi elementlar muhim:</p>
        <ul>
            <li>Header - sahifa boshi</li>
            <li>Navigation - navigatsiya menyu</li>
            <li>Main content - asosiy mazmun</li>
            <li>Sidebar - yon panel</li>
            <li>Footer - sahifa oyog'i</li>
        </ul>
    </div>
    
    <div class="yon-ustun">
        <h3>Menyu</h3>
        <ul>
            <li><a href="#">Bosh sahifa</a></li>
            <li><a href="#">CSS asoslari</a></li>
            <li><a href="#">Layout</a></li>
            <li><a href="#">Misol</a></li>
            <li><a href="#">Aloqa</a></li>
        </ul>
        
        <h3>Foydali havolalar</h3>
        <ul>
            <li><a href="#">CSS qo'llanma</a></li>
            <li><a href="#">HTML qo'llanma</a></li>
            <li><a href="#">Web-dizayn</a></li>
        </ul>
    </div>
</div>
```

</details>

<details>
    <summary>Elementlarni joylash</summary>

## 6.5 Elementlarni Joylash

### Position xususiyati

#### 1. Static - oddiy joylashuv (default)
```css
.static-element {
    position: static;
}
```

#### 2. Relative - nisbiy joylashuv
```css
.relative-element {
    position: relative;
    top: 10px;
    left: 20px;
}
```

#### 3. Absolute - mutlaq joylashuv
```css
.absolute-element {
    position: absolute;
    top: 50px;
    right: 30px;
}
```

#### 4. Fixed - qo'zg'aluvchan joylashuv
```css
.fixed-element {
    position: fixed;
    top: 20px;
    right: 20px;
}
```

### Float xususiyati

#### 1. Float left - chapga suzish
```css
.float-left {
    float: left;
    width: 200px;
}
```

#### 2. Float right - o'ngga suzish
```css
.float-right {
    float: right;
    width: 200px;
}
```

#### 3. Clear - float ni tozalash
```css
.clear-float {
    clear: both;
}
```

### Amaliy misollar

#### 1. Position qiymatlari
```html
<style>
.position-demo {
    position: relative;
    width: 400px;
    height: 300px;
    border: 2px solid #333;
    background-color: #f0f0f0;
    margin: 20px;
}

.static-box {
    position: static;
    background-color: #e3f2fd;
    padding: 10px;
    margin: 5px;
    border: 1px solid #2196f3;
}

.relative-box {
    position: relative;
    top: 20px;
    left: 30px;
    background-color: #f3e5f5;
    padding: 10px;
    border: 1px solid #9c27b0;
}

.absolute-box {
    position: absolute;
    top: 50px;
    right: 20px;
    background-color: #e8f5e8;
    padding: 10px;
    border: 1px solid #4caf50;
}

.fixed-box {
    position: fixed;
    top: 20px;
    right: 20px;
    background-color: #fff3e0;
    padding: 10px;
    border: 1px solid #ff9800;
    z-index: 1000;
}
</style>

<div class="position-demo">
    <div class="static-box">Static (oddiy)</div>
    <div class="relative-box">Relative (nisbiy)</div>
    <div class="absolute-box">Absolute (mutlaq)</div>
</div>

<div class="fixed-box">Fixed (qo'zg'aluvchan)</div>
```

#### 2. Float bilan matn o'rash
```html
<style>
.float-demo {
    max-width: 600px;
    margin: 20px auto;
    padding: 20px;
    border: 1px solid #ddd;
    background-color: white;
}

.float-rasm {
    float: left;
    width: 150px;
    height: 100px;
    margin: 0 15px 10px 0;
    background-color: #e3f2fd;
    border: 2px solid #2196f3;
    border-radius: 5px;
}

.float-rasm-right {
    float: right;
    width: 150px;
    height: 100px;
    margin: 0 0 10px 15px;
    background-color: #f3e5f5;
    border: 2px solid #9c27b0;
    border-radius: 5px;
}

.clear-demo {
    clear: both;
    background-color: #e8f5e8;
    padding: 15px;
    margin-top: 20px;
    border: 2px solid #4caf50;
    border-radius: 5px;
}
</style>

<div class="float-demo">
    <div class="float-rasm"></div>
    
    <p>Bu matn float: left element atrofida o'raladi. Rasm chap tomonda joylashgan va matn uning o'ng tomonida davom etadi.</p>
    
    <p>Float xususiyati elementlarni matn ichida suzishga imkon beradi. Bu rasmlar va matn bilan ishlashda juda foydali.</p>
    
    <div class="float-rasm-right"></div>
    
    <p>Bu yerda rasm o'ng tomonda joylashgan. Matn uning chap tomonida o'raladi.</p>
    
    <div class="clear-demo">
        <strong>Clear demo:</strong> Bu quti clear: both xususiyatiga ega. U barcha float elementlardan keyin yangi qatordan boshlanadi.
    </div>
</div>
```

#### 3. Navigatsiya menyu
```html
<style>
.nav-container {
    background-color: #2c3e50;
    padding: 0;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 1000;
    box-shadow: 0 2px 5px rgba(0,0,0,0.2);
}

.nav-menu {
    max-width: 1000px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 20px;
}

.nav-logo {
    color: white;
    font-size: 1.5em;
    font-weight: bold;
    text-decoration: none;
}

.nav-links {
    display: flex;
    list-style: none;
    margin: 0;
    padding: 0;
}

.nav-links li {
    margin-left: 30px;
}

.nav-links a {
    color: white;
    text-decoration: none;
    padding: 15px 0;
    display: block;
    transition: color 0.3s ease;
}

.nav-links a:hover {
    color: #3498db;
}

.content {
    margin-top: 80px;
    padding: 20px;
    max-width: 1000px;
    margin-left: auto;
    margin-right: auto;
}
</style>

<nav class="nav-container">
    <div class="nav-menu">
        <a href="#" class="nav-logo">Mening Sahifam</a>
        <ul class="nav-links">
            <li><a href="#">Bosh sahifa</a></li>
            <li><a href="#">Xizmatlar</a></li>
            <li><a href="#">Portfolio</a></li>
            <li><a href="#">Aloqa</a></li>
        </ul>
    </div>
</nav>

<div class="content">
    <h1>Sahifa mazmuni</h1>
    <p>Bu yerda sahifaning asosiy mazmuni joylashadi. Fixed navigatsiya menyu sahifaning yuqori qismida doimo ko'rinadi.</p>
    
    <p>Position: fixed xususiyati elementni sahifaning muayyan joyida qo'zg'aluvchan qilib qo'yadi. Sahifa aylantirilganda ham element o'z joyida qoladi.</p>
    
    <h2>CSS Layout xususiyatlari</h2>
    <p>Elementlarni joylash uchun turli xil xususiyatlar ishlatiladi:</p>
    <ul>
        <li><strong>Position:</strong> static, relative, absolute, fixed</li>
        <li><strong>Float:</strong> left, right, none</li>
        <li><strong>Clear:</strong> left, right, both</li>
        <li><strong>Display:</strong> block, inline, inline-block</li>
    </ul>
    
    <p>Bu xususiyatlar yordamida chiroyli va funksional web-sahifalar yaratish mumkin.</p>
</div>
```

</details>
