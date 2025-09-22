<details>
    <summary>Rasmlarni qo'shish (img tegi)</summary>

## 4.1 Rasmlarni Qo'shish (img tegi)

### IMG tegi nima?

**`<img>` tegi** web-sahifaga rasmlarni qo'shish uchun ishlatiladi. Bu tag o'z-o'zidan yopiladigan tag hisoblanadi, ya'ni `</img>` yopish tegi yo'q.

### Asosiy sintaksis

```html
<img src="rasm_manzili" alt="rasm_tavsifi">
```

#### Majburiy atributlar

**1. src atributi** - rasm fayli manzili
```html
<img src="images/mening_rasmim.jpg" alt="Mening rasim">
```

**2. alt atributi** - rasm tavsifi (muhim!)
```html
<img src="logo.png" alt="Kompaniya logosi">
```

### Rasm manzillari turlari

#### 1. Nisbiy manzil (Relative Path)
```html
<!-- Bir xil papkada -->
<img src="rasm.jpg" alt="Rasm">

<!-- Images papkasida -->
<img src="images/rasm.jpg" alt="Rasm">

<!-- Yuqori papkada -->
<img src="../rasm.jpg" alt="Rasm">
```

#### 2. Mutlaq manzil (Absolute Path)
```html
<img src="/Users/foydalanuvchi/rasmlar/rasm.jpg" alt="Rasm">
```

#### 3. Internet manzili (URL)
```html
<img src="https://example.com/rasm.jpg" alt="Internet rasmi">
```

### Qo'shimcha atributlar

#### Width va Height - o'lchamlar
```html
<img src="rasm.jpg" alt="Rasm" width="300" height="200">
```

#### Title - tooltip matn
```html
<img src="rasm.jpg" alt="Rasm" title="Bu rasm haqida qo'shimcha ma'lumot">
```

### Rasm formatlari

**Eng keng tarqalgan formatlar:**
- **JPEG (.jpg, .jpeg)** - fotosuratlar uchun
- **PNG (.png)** - shaffoflik kerak bo'lganda  
- **GIF (.gif)** - animatsiyalar uchun
- **SVG (.svg)** - vector rasmlar uchun
- **WebP (.webp)** - zamonaviy format

### Amaliy misollar

#### Oddiy rasm qo'shish
```html
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <title>Rasmlar Sahifasi</title>
</head>
<body>
    <h1>Mening Rasmlarim</h1>
    
    <h2>Tabiat Rasmlari</h2>
    <img src="images/tabiat.jpg" alt="Go'zal tabiat manzarasi">
    
    <h2>Shahar Rasmlari</h2>
    <img src="images/shahar.jpg" alt="Zamonaviy shahar ko'rinishi">
</body>
</html>
```

#### Figure va Figcaption bilan
```html
<figure>
    <img src="sunset.jpg" alt="Quyosh botishi">
    <figcaption>Go'zal quyosh botishi ko'rinishi</figcaption>
</figure>
```

</details>

<details>
    <summary>Rasm o'lchamlari va joylashuvi</summary>

## 4.2 Rasm O'lchamlari va Joylashuvi

### HTML bilan o'lcham belgilash

#### Width va Height atributlari
```html
<!-- Piksellar bilan -->
<img src="rasm.jpg" alt="Rasm" width="400" height="300">

<!-- Nisbiy o'lcham (foiz) - CSS da yaxshiroq -->
<img src="rasm.jpg" alt="Rasm" style="width: 50%;">
```

### CSS bilan o'lcham boshqarish

#### Asosiy CSS xususiyatlari
```css
img {
    width: 300px;        /* Kenglik */
    height: 200px;       /* Balandlik */
    max-width: 100%;     /* Maksimal kenglik */
    max-height: 500px;   /* Maksimal balandlik */
}
```

#### Nisbat saqlash
```css
.responsive-img {
    width: 100%;         /* To'liq kenglik */
    height: auto;        /* Avtomatik balandlik */
    max-width: 600px;    /* Maksimal chegara */
}
```

### Rasmlarni joylash usullari

#### 1. Text-align bilan markazlashtirish
```css
.center-image {
    text-align: center;
}
```
```html
<div class="center-image">
    <img src="rasm.jpg" alt="Markazlashtirilgan rasm">
</div>
```

#### 2. Block element qilib markazlashtirish
```css
.center-block {
    display: block;
    margin: 0 auto;      /* Avtomatik chap-o'ng margin */
    max-width: 100%;
}
```

#### 3. Float bilan joylash
```css
.float-left {
    float: left;         /* Chapga joylash */
    margin-right: 15px;  /* O'ng tomonda bo'shliq */
}

.float-right {
    float: right;        /* O'ngga joylash */
    margin-left: 15px;   /* Chap tomonda bo'shliq */
}
```

### Object-fit xususiyati

Rasm konteyner ichiga qanday joylashishini boshqaradi:

```css
.fit-cover {
    width: 300px;
    height: 200px;
    object-fit: cover;    /* Rasm to'liq qoplash */
}

.fit-contain {
    width: 300px;
    height: 200px;
    object-fit: contain;  /* Rasm to'liq ko'rinish */
}

.fit-fill {
    width: 300px;
    height: 200px;
    object-fit: fill;     /* Rasm cho'zilish */
}
```

### Responsive rasmlar

#### Moslashuvchan rasmlar
```css
.responsive {
    max-width: 100%;
    height: auto;
    display: block;
}
```

#### Turli ekranlar uchun
```css
/* Kichik ekranlar */
@media (max-width: 600px) {
    .mobile-img {
        width: 100%;
        height: auto;
    }
}

/* Katta ekranlar */
@media (min-width: 1200px) {
    .desktop-img {
        width: 800px;
        height: auto;
    }
}
```

### Amaliy misollar

#### To'liq responsive rasm
```html
<style>
.image-container {
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
}

.responsive-image {
    width: 100%;
    height: auto;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
}
</style>

<div class="image-container">
    <img src="landscape.jpg" alt="Tabiat manzarasi" class="responsive-image">
</div>
```

#### Rasm galereyasi
```html
<style>
.gallery {
    display: flex;
    flex-wrap: wrap;
    gap: 15px;
    justify-content: center;
}

.gallery-item {
    width: 200px;
    height: 150px;
    object-fit: cover;
    border-radius: 8px;
    transition: transform 0.3s ease;
}

.gallery-item:hover {
    transform: scale(1.05);
}
</style>

<div class="gallery">
    <img src="img1.jpg" alt="Rasm 1" class="gallery-item">
    <img src="img2.jpg" alt="Rasm 2" class="gallery-item">
    <img src="img3.jpg" alt="Rasm 3" class="gallery-item">
</div>
```

</details>

<details>
    <summary>Havolalar yaratish (a tegi)</summary>

## 4.3 Havolalar Yaratish (a tegi)

### A tegi nima?

**`<a>` tegi (Anchor)** boshqa sahifalarga, fayllar yoki sahifaning ma'lum qismlariga o'tish uchun havolalar yaratadi.

### Asosiy sintaksis

```html
<a href="manzil">Havola matni</a>
```

### Href atributi turlari

#### 1. Boshqa web-sahifaga havola
```html
<a href="about.html">Biz haqimizda</a>
<a href="contact.html">Aloqa</a>
```

#### 2. Boshqa veb-saytga havola
```html
<a href="https://www.google.com">Google</a>
<a href="https://www.youtube.com">YouTube</a>
```

#### 3. Email manzili
```html
<a href="mailto:info@example.com">Email yuborish</a>
<a href="mailto:admin@sayt.com?subject=Savol">Savolingiz bor?</a>
```

#### 4. Telefon raqami
```html
<a href="tel:+998901234567">Qo'ng'iroq qiling</a>
```

### Target atributi

Havola qayerda ochilishini belgilaydi:

```html
<!-- Yangi oynada ochish -->
<a href="https://google.com" target="_blank">Google (yangi oyna)</a>

<!-- Shu oynada ochish (standart) -->
<a href="page.html" target="_self">Sahifa</a>
```

### Qo'shimcha atributlar

#### Title atributi - tooltip
```html
<a href="about.html" title="Kompaniya haqida ma'lumot">Biz haqimizda</a>
```

#### Download atributi - fayl yuklab olish
```html
<a href="document.pdf" download="Hujjat.pdf">PDF yuklab olish</a>
<a href="image.jpg" download>Rasmni yuklab olish</a>
```

### Havolalarni CSS bilan bezatish

#### Asosiy stillar
```css
a {
    color: #007bff;           /* Rang */
    text-decoration: none;    /* Chiziqni olib tashlash */
    font-weight: bold;        /* Qalin qilish */
}

a:hover {
    color: #0056b3;           /* Hover ranggi */
    text-decoration: underline; /* Hover da chiziq */
}

a:visited {
    color: #6f42c1;           /* Tashrif buyurilgan rang */
}
```

#### Tugma ko'rinishidagi havolalar
```css
.btn-link {
    display: inline-block;
    padding: 10px 20px;
    background-color: #007bff;
    color: white;
    text-decoration: none;
    border-radius: 5px;
    transition: background-color 0.3s ease;
}

.btn-link:hover {
    background-color: #0056b3;
    color: white;
}
```

### Amaliy misollar

#### Navigatsiya menu
```html
<style>
.nav-menu {
    background-color: #f8f9fa;
    padding: 15px;
    text-align: center;
}

.nav-menu a {
    margin: 0 15px;
    color: #333;
    text-decoration: none;
    font-weight: bold;
    padding: 8px 15px;
    border-radius: 4px;
    transition: background-color 0.3s ease;
}

.nav-menu a:hover {
    background-color: #007bff;
    color: white;
}
</style>

<nav class="nav-menu">
    <a href="index.html">Bosh sahifa</a>
    <a href="about.html">Biz haqimizda</a>
    <a href="services.html">Xizmatlar</a>
    <a href="contact.html">Aloqa</a>
</nav>
```

</details>

<details>
    <summary>Ichki va tashqi havolalar</summary>

## 4.4 Ichki va Tashqi Havolalar

### Ichki havolalar (Internal Links)

Shu veb-sayt ichidagi boshqa sahifalarga o'tadigan havolalar.

#### 1. Boshqa sahifaga o'tish
```html
<!-- Nisbiy manzil -->
<a href="about.html">Biz haqimizda</a>
<a href="pages/contact.html">Aloqa sahifasi</a>
<a href="../index.html">Bosh sahifaga qaytish</a>
```

#### 2. Sahifa ichidagi qismga o'tish (Anchor Links)
```html
<!-- Sahifa yuqorisida -->
<a href="#section1">1-bo'lim</a>
<a href="#section2">2-bo'lim</a>
<a href="#footer">Pastki qism</a>

<!-- Sahifa mazmuni -->
<h2 id="section1">1-bo'lim</h2>
<p>Bu birinchi bo'lim mazmuni...</p>

<h2 id="section2">2-bo'lim</h2>
<p>Bu ikkinchi bo'lim mazmuni...</p>

<footer id="footer">
    <p>Pastki qism</p>
</footer>
```

#### 3. Yuqoriga qaytish havolasi
```html
<!-- Sahifa oxirida -->
<a href="#top">⬆ Yuqoriga</a>

<!-- Yoki body tegiga id qo'shish -->
<body id="top">
```

### Tashqi havolalar (External Links)

Boshqa veb-saytlarga o'tadigan havolalar.

#### 1. Boshqa veb-saytlarga
```html
<a href="https://www.google.com" target="_blank">Google</a>
<a href="https://www.youtube.com" target="_blank">YouTube</a>
<a href="https://www.wikipedia.org" target="_blank">Wikipedia</a>
```

#### 2. Xavfsizlik attributi
```html
<a href="https://example.com" target="_blank" rel="noopener noreferrer">
    Tashqi sayt
</a>
```

### Fayl havolalari

#### 1. Hujjatlarni yuklab olish
```html
<a href="files/catalog.pdf" download="Katalog.pdf">PDF yuklab olish</a>
<a href="files/price.xlsx" download>Narxlar jadvali</a>
<a href="images/photo.jpg" download="rasm.jpg">Rasmni saqlash</a>
```

#### 2. Turli fayl turlari
```html
<!-- Hujjatlar -->
<a href="document.pdf">PDF hujjat</a>
<a href="spreadsheet.xlsx">Excel jadval</a>
<a href="presentation.pptx">PowerPoint taqdimot</a>

<!-- Media fayllar -->
<a href="music.mp3">Musiqa fayli</a>
<a href="video.mp4">Video fayl</a>
```

### Email va telefon havolalari

#### Email havolalari
```html
<!-- Oddiy email -->
<a href="mailto:info@example.com">Email yuborish</a>

<!-- Mavzu bilan -->
<a href="mailto:support@example.com?subject=Yordam so'rovi">Yordam so'rash</a>

<!-- To'liq formatted email -->
<a href="mailto:contact@example.com?subject=Buyurtma&body=Assalomu alaykum,%0A%0AMen buyurtma bermoqchiman.">
    Buyurtma berish
</a>
```

#### Telefon havolalari
```html
<a href="tel:+998901234567">+998 90 123 45 67</a>
<a href="tel:998712345678">Qo'ng'iroq qiling</a>
```

### Amaliy misollar

#### Sahifa ichidagi navigatsiya
```html
<style>
.page-nav {
    background-color: #f8f9fa;
    padding: 15px;
    border-radius: 5px;
    margin-bottom: 20px;
}

.page-nav h3 {
    margin-top: 0;
    color: #333;
}

.page-nav a {
    display: block;
    padding: 5px 0;
    color: #007bff;
    text-decoration: none;
}

.page-nav a:hover {
    color: #0056b3;
    text-decoration: underline;
}

.back-to-top {
    position: fixed;
    bottom: 20px;
    right: 20px;
    background-color: #007bff;
    color: white;
    padding: 10px 15px;
    text-decoration: none;
    border-radius: 50%;
    font-size: 18px;
}
</style>

<!-- Sahifa navigatsiyasi -->
<div class="page-nav">
    <h3>Bu sahifada:</h3>
    <a href="#intro">Kirish</a>
    <a href="#main-content">Asosiy mazmun</a>
    <a href="#examples">Misollar</a>
    <a href="#conclusion">Xulosa</a>
</div>

<!-- Sahifa mazmuni -->
<section id="intro">
    <h2>Kirish</h2>
    <p>Bu kirish bo'limi...</p>
</section>

<section id="main-content">
    <h2>Asosiy mazmun</h2>
    <p>Bu asosiy mazmun...</p>
</section>

<!-- Yuqoriga qaytish -->
<a href="#top" class="back-to-top">↑</a>
```

</details>

<details>
    <summary>CSS bilan rasmlarni bezatish</summary>

## 4.5 CSS bilan Rasmlarni Bezatish

### Asosiy bezatish xususiyatlari

#### 1. Chegara (Border)
```css
.border-img {
    border: 3px solid #007bff;        /* Oddiy chegara */
    border-radius: 10px;              /* Yumaloq burchaklar */
}

.double-border {
    border: 5px double #28a745;       /* Ikki qatorli chegara */
}

.dashed-border {
    border: 2px dashed #dc3545;       /* Chiziqcha chegara */
}
```

#### 2. Shadow (Soya)
```css
.shadow-img {
    box-shadow: 0 4px 8px rgba(0,0,0,0.2);  /* Oddiy soya */
}

.deep-shadow {
    box-shadow: 0 8px 16px rgba(0,0,0,0.3);  /* Chuqur soya */
}

.colored-shadow {
    box-shadow: 0 4px 15px rgba(0,123,255,0.3);  /* Rangli soya */
}
```

#### 3. Border-radius (Yumaloq qilish)
```css
.round-corners {
    border-radius: 15px;              /* Yumaloq burchaklar */
}

.circle-img {
    border-radius: 50%;               /* To'liq dumaloq */
    width: 200px;
    height: 200px;
    object-fit: cover;
}
```

### Filter effektlari

#### 1. Asosiy filterlar
```css
.blur-img {
    filter: blur(2px);                /* Loyqalik */
}

.brightness-img {
    filter: brightness(150%);         /* Yorqinlik */
}

.contrast-img {
    filter: contrast(120%);           /* Kontrast */
}

.grayscale-img {
    filter: grayscale(100%);          /* Oq-qora */
}

.sepia-img {
    filter: sepia(80%);               /* Eski rasm effekti */
}
```

#### 2. Transform effektlari
```css
.rotate-img {
    transform: rotate(5deg);          /* Aylantirish */
}

.scale-img {
    transform: scale(1.1);            /* Kattalashtirish */
}
```

### Amaliy misollar

#### 1. Profil rasmi
```html
<style>
.profile-img {
    width: 150px;
    height: 150px;
    border-radius: 50%;
    border: 4px solid #fff;
    box-shadow: 0 4px 12px rgba(0,0,0,0.15);
    object-fit: cover;
    transition: transform 0.3s ease;
}

.profile-img:hover {
    transform: scale(1.05);
}
</style>

<img src="profile.jpg" alt="Profil rasmi" class="profile-img">
```

#### 2. Rasm kartochkalari
```html
<style>
.card {
    width: 300px;
    background-color: white;
    border-radius: 12px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    overflow: hidden;
    transition: transform 0.3s ease;
}

.card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 25px rgba(0,0,0,0.15);
}

.card-img {
    width: 100%;
    height: 200px;
    object-fit: cover;
}

.card-content {
    padding: 20px;
}
</style>

<div class="card">
    <img src="nature.jpg" alt="Tabiat" class="card-img">
    <div class="card-content">
        <h3>Go'zal Tabiat</h3>
        <p>Bu go'zal tabiat manzarasi haqida qisqacha ma'lumot.</p>
    </div>
</div>
```

</details>

<details>
    <summary>Hover effektlari</summary>

## 4.6 Hover Effektlari

### Hover nima?

**Hover** - foydalanuvchi sichqoncha ko'rsatkichini element ustiga olib kelganda sodir bo'ladigan hodisa. CSS da `:hover` pseudo-class yordamida boshqariladi.

### Asosiy hover effektlari

#### 1. Rangni o'zgartirish
```css
.color-change {
    background-color: #007bff;
    color: white;
    padding: 10px 20px;
    transition: background-color 0.3s ease;
}

.color-change:hover {
    background-color: #0056b3;
}
```

#### 2. O'lchamni o'zgartirish
```css
.scale-hover {
    transition: transform 0.3s ease;
}

.scale-hover:hover {
    transform: scale(1.1);            /* 10% kattalashtirish */
}
```

#### 3. Soya effektlari
```css
.shadow-hover {
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    transition: box-shadow 0.3s ease;
}

.shadow-hover:hover {
    box-shadow: 0 8px 25px rgba(0,0,0,0.2);
}
```

### Rasmlar uchun hover effektlari

#### 1. Filter effektlari
```css
.filter-hover {
    filter: grayscale(100%);          /* Boshlang'ich: oq-qora */
    transition: filter 0.3s ease;
}

.filter-hover:hover {
    filter: grayscale(0%);            /* Hover: rangli */
}
```

#### 2. Overlay effektlari
```html
<style>
.image-overlay {
    position: relative;
    display: inline-block;
    overflow: hidden;
}

.image-overlay img {
    width: 100%;
    transition: transform 0.3s ease;
}

.overlay-text {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-color: rgba(0,0,0,0.7);
    color: white;
    padding: 15px 25px;
    border-radius: 5px;
    opacity: 0;
    transition: opacity 0.3s ease;
}

.image-overlay:hover img {
    transform: scale(1.1);
}

.image-overlay:hover .overlay-text {
    opacity: 1;
}
</style>

<div class="image-overlay">
    <img src="nature.jpg" alt="Tabiat">
    <div class="overlay-text">Go'zal manzara</div>
</div>
```

#### 3. Zoom effektlari
```css
.zoom-container {
    width: 300px;
    height: 200px;
    overflow: hidden;
    border-radius: 10px;
}

.zoom-img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.5s ease;
}

.zoom-container:hover .zoom-img {
    transform: scale(1.2);            /* Zoom in */
}
```

### Animatsiya effektlari

#### 1. Aylanish
```css
.rotate-hover {
    transition: transform 0.3s ease;
}

.rotate-hover:hover {
    transform: rotate(360deg);
}
```

#### 2. Slide effektlari
```css
.slide-up {
    transition: transform 0.3s ease;
}

.slide-up:hover {
    transform: translateY(-10px);     /* Yuqoriga siljish */
}
```

### Amaliy misollar

#### Interaktiv galereya
```html
<style>
.interactive-gallery {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
    padding: 20px;
}

.gallery-item {
    position: relative;
    overflow: hidden;
    border-radius: 15px;
    box-shadow: 0 4px 15px rgba(0,0,0,0.1);
    transition: all 0.3s ease;
}

.gallery-item:hover {
    transform: translateY(-10px);
    box-shadow: 0 15px 35px rgba(0,0,0,0.2);
}

.gallery-item img {
    width: 100%;
    height: 200px;
    object-fit: cover;
    transition: transform 0.5s ease;
}

.gallery-item:hover img {
    transform: scale(1.1);
}

.gallery-info {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    background: linear-gradient(transparent, rgba(0,0,0,0.8));
    color: white;
    padding: 30px 20px 20px;
    transform: translateY(100%);
    transition: transform 0.3s ease;
}

.gallery-item:hover .gallery-info {
    transform: translateY(0);
}
</style>

<div class="interactive-gallery">
    <div class="gallery-item">
        <img src="img1.jpg" alt="Rasm 1">
        <div class="gallery-info">
            <h3>Go'zal Manzara</h3>
            <p>Tabiatning ajoyib ko'rinishi</p>
        </div>
    </div>
</div>
```

</details>