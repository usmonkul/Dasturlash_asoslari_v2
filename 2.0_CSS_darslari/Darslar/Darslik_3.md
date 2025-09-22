<details>
    <summary>Media queries nima?</summary>

## 8.1 Media Queries Nima?

### Media queries nima?

**Media queries** - CSS ning xususiyati bo'lib, turli xil qurilmalar va ekran o'lchamlari uchun turli xil CSS qoidalarini qo'llash imkonini beradi.

### Nima uchun media queries kerak?

#### 1. Turli qurilmalar
- Kompyuter (katta ekran)
- Planshet (o'rta ekran)
- Telefon (kichik ekran)

#### 2. Moslashuvchan dizayn
- Har bir qurilma uchun mos dizayn
- Foydalanuvchi tajribasini yaxshilash
- Zamonaviy web-dizayn standarti

### Media queries sintaksisi

#### 1. Asosiy sintaksis
```css
@media (shart) {
    /* CSS qoidalar */
}
```

#### 2. Ekran o'lchami shartlari
```css
@media (max-width: 768px) {
    /* 768px dan kichik ekranlar uchun */
}

@media (min-width: 769px) {
    /* 769px dan katta ekranlar uchun */
}
```

#### 3. Range (oraliq) shartlar
```css
@media (min-width: 600px) and (max-width: 1024px) {
    /* 600px va 1024px orasidagi ekranlar uchun */
}
```

### Asosiy breakpoint'lar

#### 1. Standart breakpoint'lar
```css
/* Mobil (kichik telefon) */
@media (max-width: 480px) {
    /* CSS qoidalar */
}

/* Katta telefon va kichik planshet */
@media (min-width: 481px) and (max-width: 768px) {
    /* CSS qoidalar */
}

/* Planshet */
@media (min-width: 769px) and (max-width: 1024px) {
    /* CSS qoidalar */
}

/* Desktop */
@media (min-width: 1025px) {
    /* CSS qoidalar */
}
```

#### 2. Oddiy breakpoint'lar
```css
/* Mobil */
@media (max-width: 600px) {
    /* CSS qoidalar */
}

/* Planshet va katta */
@media (min-width: 601px) {
    /* CSS qoidalar */
}
```

### Amaliy misollar

#### 1. Oddiy media query
```html
<style>
.media-demo {
    background-color: #e3f2fd;
    padding: 20px;
    text-align: center;
    font-size: 18px;
}

/* Kichik ekranlar uchun */
@media (max-width: 600px) {
    .media-demo {
        background-color: #ffeb3b;
        font-size: 14px;
        padding: 10px;
    }
}

/* Katta ekranlar uchun */
@media (min-width: 1200px) {
    .media-demo {
        background-color: #4caf50;
        font-size: 24px;
        padding: 30px;
    }
}
</style>

<div class="media-demo">
    <h3>Media Query Demo</h3>
    <p>Ekran o'lchamini o'zgartiring va rang o'zgarishini kuzating!</p>
</div>
```

#### 2. Responsive matn o'lchamlari
```html
<style>
.responsive-matn {
    padding: 20px;
    background-color: #f8f9fa;
    border: 2px solid #dee2e6;
    border-radius: 8px;
    margin: 20px 0;
}

.responsive-matn h2 {
    color: #2c3e50;
    margin: 0 0 15px 0;
}

.responsive-matn p {
    color: #666;
    line-height: 1.6;
    margin: 0;
}

/* Kichik ekranlar (mobil) */
@media (max-width: 480px) {
    .responsive-matn {
        padding: 10px;
        font-size: 14px;
    }
    
    .responsive-matn h2 {
        font-size: 18px;
    }
    
    .responsive-matn p {
        font-size: 12px;
    }
}

/* O'rta ekranlar (planshet) */
@media (min-width: 481px) and (max-width: 768px) {
    .responsive-matn {
        padding: 15px;
        font-size: 16px;
    }
    
    .responsive-matn h2 {
        font-size: 22px;
    }
}

/* Katta ekranlar (desktop) */
@media (min-width: 769px) {
    .responsive-matn {
        padding: 25px;
        font-size: 18px;
        max-width: 800px;
        margin: 20px auto;
    }
    
    .responsive-matn h2 {
        font-size: 28px;
    }
    
    .responsive-matn p {
        font-size: 16px;
    }
}
</style>

<div class="responsive-matn">
    <h2>Responsive Matn</h2>
    <p>Bu matn turli ekran o'lchamlarida turli xil ko'rinadi. Ekran o'lchamini o'zgartiring va farqni kuzating!</p>
</div>
```

#### 3. Responsive kartochkalar
```html
<style>
.responsive-kartochkalar {
    display: flex;
    gap: 20px;
    padding: 20px;
    flex-wrap: wrap;
}

.kartochka {
    background-color: white;
    border: 2px solid #e0e0e0;
    border-radius: 10px;
    padding: 20px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    flex: 1;
    min-width: 200px;
}

.kartochka h3 {
    color: #2c3e50;
    margin: 0 0 15px 0;
}

.kartochka p {
    color: #666;
    line-height: 1.5;
    margin: 0;
}

/* Mobil uchun */
@media (max-width: 600px) {
    .responsive-kartochkalar {
        flex-direction: column;
        gap: 15px;
        padding: 15px;
    }
    
    .kartochka {
        min-width: auto;
        padding: 15px;
    }
}

/* Planshet uchun */
@media (min-width: 601px) and (max-width: 900px) {
    .kartochka {
        flex: 1 1 calc(50% - 10px);
        min-width: auto;
    }
}

/* Desktop uchun */
@media (min-width: 901px) {
    .kartochka {
        flex: 1;
        min-width: 200px;
    }
}
</style>

<div class="responsive-kartochkalar">
    <div class="kartochka">
        <h3>Kartochka 1</h3>
        <p>Bu birinchi kartochka. U turli ekran o'lchamlarida turli xil ko'rinadi.</p>
    </div>
    
    <div class="kartochka">
        <h3>Kartochka 2</h3>
        <p>Bu ikkinchi kartochka. Media queries yordamida responsive qilingan.</p>
    </div>
    
    <div class="kartochka">
        <h3>Kartochka 3</h3>
        <p>Bu uchinchi kartochka. Ekran o'lchamini o'zgartiring!</p>
    </div>
</div>
```

</details>

<details>
    <summary>Turli ekran o'lchamlari uchun dizayn</summary>

## 8.2 Turli Ekran O'lchamlari Uchun Dizayn

### Ekran o'lchamlari turlari

#### 1. Mobil qurilmalar
- **Kichik telefon**: 320px - 480px
- **Katta telefon**: 481px - 768px
- **Xususiyatlar**: Vertikal layout, katta tugmalar, kam mazmun

#### 2. Planshet qurilmalar
- **Kichik planshet**: 769px - 1024px
- **Katta planshet**: 1025px - 1440px
- **Xususiyatlar**: Aralash layout, o'rta mazmun

#### 3. Desktop qurilmalar
- **Kichik desktop**: 1441px - 1920px
- **Katta desktop**: 1921px va undan katta
- **Xususiyatlar**: Gorizontal layout, ko'p mazmun

### Responsive breakpoint strategiyasi

#### 1. Oddiy breakpoint'lar
```css
/* Mobil */
@media (max-width: 768px) {
    /* Mobil dizayn */
}

/* Planshet va katta */
@media (min-width: 769px) {
    /* Desktop dizayn */
}
```

#### 2. Detalli breakpoint'lar
```css
/* Kichik mobil */
@media (max-width: 480px) {
    /* Kichik telefon dizayni */
}

/* Katta mobil */
@media (min-width: 481px) and (max-width: 768px) {
    /* Katta telefon dizayni */
}

/* Planshet */
@media (min-width: 769px) and (max-width: 1024px) {
    /* Planshet dizayni */
}

/* Desktop */
@media (min-width: 1025px) {
    /* Desktop dizayni */
}
```

### Layout o'zgarishlari

#### 1. Mobil layout
- Vertikal joylashuv (flex-direction: column)
- Katta tugmalar va matn
- Kam mazmun sahifada
- Oddiy navigatsiya

#### 2. Planshet layout
- Aralash joylashuv
- O'rta o'lcham elementlar
- Qismli o'rash (flex-wrap: wrap)
- Yon panel ko'rsatish

#### 3. Desktop layout
- Gorizontal joylashuv
- Kichik o'lcham elementlar
- Ko'p mazmun sahifada
- To'liq navigatsiya

### Amaliy misollar

#### 1. Responsive navigatsiya
```html
<style>
.responsive-nav {
    background-color: #2c3e50;
    padding: 0;
}

.nav-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

.nav-logo {
    color: white;
    font-size: 1.5em;
    font-weight: bold;
    text-decoration: none;
    padding: 15px 0;
}

.nav-menu {
    display: flex;
    list-style: none;
    margin: 0;
    padding: 0;
    gap: 30px;
}

.nav-menu a {
    color: white;
    text-decoration: none;
    padding: 15px 0;
    transition: color 0.3s ease;
}

.nav-menu a:hover {
    color: #3498db;
}

/* Mobil uchun */
@media (max-width: 768px) {
    .nav-container {
        flex-direction: column;
        padding: 10px;
    }
    
    .nav-logo {
        font-size: 1.2em;
        padding: 10px 0;
    }
    
    .nav-menu {
        flex-direction: column;
        gap: 10px;
        width: 100%;
        text-align: center;
    }
    
    .nav-menu a {
        padding: 10px;
        border-bottom: 1px solid #34495e;
    }
}

/* Planshet uchun */
@media (min-width: 769px) and (max-width: 1024px) {
    .nav-container {
        padding: 0 15px;
    }
    
    .nav-menu {
        gap: 20px;
    }
    
    .nav-menu a {
        font-size: 14px;
    }
}

/* Desktop uchun */
@media (min-width: 1025px) {
    .nav-container {
        padding: 0 20px;
    }
    
    .nav-menu {
        gap: 40px;
    }
    
    .nav-menu a {
        font-size: 16px;
    }
}
</style>

<nav class="responsive-nav">
    <div class="nav-container">
        <a href="#" class="nav-logo">Mening Sahifam</a>
        <ul class="nav-menu">
            <li><a href="#">Bosh sahifa</a></li>
            <li><a href="#">Xizmatlar</a></li>
            <li><a href="#">Portfolio</a></li>
            <li><a href="#">Blog</a></li>
            <li><a href="#">Aloqa</a></li>
        </ul>
    </div>
</nav>
```

#### 2. Responsive layout (header, main, sidebar)
```html
<style>
.responsive-layout {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
}

.layout-header {
    background-color: #34495e;
    color: white;
    padding: 20px;
    text-align: center;
}

.layout-main {
    display: flex;
    flex: 1;
    gap: 20px;
    padding: 20px;
}

.layout-content {
    flex: 2;
    background-color: white;
    padding: 20px;
    border: 1px solid #e0e0e0;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.layout-sidebar {
    flex: 1;
    background-color: #f8f9fa;
    padding: 20px;
    border: 1px solid #e0e0e0;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.layout-footer {
    background-color: #2c3e50;
    color: white;
    padding: 15px;
    text-align: center;
}

.layout-content h2,
.layout-sidebar h3 {
    color: #2c3e50;
    margin-top: 0;
}

.layout-sidebar ul {
    list-style: none;
    padding: 0;
}

.layout-sidebar li {
    padding: 8px 0;
    border-bottom: 1px solid #e0e0e0;
}

.layout-sidebar a {
    color: #3498db;
    text-decoration: none;
}

.layout-sidebar a:hover {
    text-decoration: underline;
}

/* Mobil uchun */
@media (max-width: 768px) {
    .layout-header {
        padding: 15px;
    }
    
    .layout-header h1 {
        font-size: 1.5em;
        margin: 0;
    }
    
    .layout-main {
        flex-direction: column;
        gap: 15px;
        padding: 15px;
    }
    
    .layout-content,
    .layout-sidebar {
        flex: none;
    }
    
    .layout-sidebar {
        order: -1; /* Sidebar yuqoriga ko'tariladi */
    }
    
    .layout-content {
        padding: 15px;
    }
    
    .layout-sidebar {
        padding: 15px;
    }
}

/* Planshet uchun */
@media (min-width: 769px) and (max-width: 1024px) {
    .layout-header {
        padding: 18px;
    }
    
    .layout-main {
        flex-wrap: wrap;
        gap: 15px;
        padding: 18px;
    }
    
    .layout-content {
        flex: 1 1 100%;
        margin-bottom: 0;
    }
    
    .layout-sidebar {
        flex: 1 1 calc(50% - 8px);
    }
}

/* Desktop uchun */
@media (min-width: 1025px) {
    .layout-header {
        padding: 25px;
    }
    
    .layout-main {
        max-width: 1200px;
        margin: 0 auto;
        gap: 25px;
        padding: 25px;
    }
    
    .layout-content {
        flex: 2;
    }
    
    .layout-sidebar {
        flex: 1;
    }
}
</style>

<div class="responsive-layout">
    <header class="layout-header">
        <h1>Responsive Layout</h1>
        <p>Turli ekran o'lchamlari uchun moslashtirilgan dizayn</p>
    </header>
    
    <main class="layout-main">
        <div class="layout-content">
            <h2>Asosiy mazmun</h2>
            <p>Bu yerda sahifaning asosiy mazmuni joylashadi. Turli ekran o'lchamlarida turli xil ko'rinadi.</p>
            
            <h3>Responsive xususiyatlar:</h3>
            <ul>
                <li><strong>Mobil:</strong> Vertikal layout, katta matn, oddiy dizayn</li>
                <li><strong>Planshet:</strong> Aralash layout, o'rta o'lcham elementlar</li>
                <li><strong>Desktop:</strong> Gorizontal layout, kichik elementlar, ko'p mazmun</li>
            </ul>
        </div>
        
        <div class="layout-sidebar">
            <h3>Yon panel</h3>
            <ul>
                <li><a href="#">Link 1</a></li>
                <li><a href="#">Link 2</a></li>
                <li><a href="#">Link 3</a></li>
                <li><a href="#">Link 4</a></li>
                <li><a href="#">Link 5</a></li>
            </ul>
        </div>
    </main>
    
    <footer class="layout-footer">
        <p>&copy; 2024 Responsive Layout misoli</p>
    </footer>
</div>
```

#### 3. Responsive galereya
```html
<style>
.responsive-galereya {
    display: flex;
    flex-wrap: wrap;
    gap: 15px;
    padding: 20px;
    max-width: 1200px;
    margin: 0 auto;
}

.galereya-item {
    background-color: #e3f2fd;
    border: 2px solid #2196f3;
    border-radius: 8px;
    padding: 20px;
    text-align: center;
    flex: 1 1 200px;
    min-height: 150px;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: transform 0.3s ease;
}

.galereya-item:hover {
    transform: translateY(-5px);
    box-shadow: 0 4px 8px rgba(0,0,0,0.2);
}

.galereya-item h3 {
    color: #1976d2;
    margin: 0;
}

/* Kichik mobil (320px - 480px) */
@media (max-width: 480px) {
    .responsive-galereya {
        padding: 10px;
        gap: 10px;
    }
    
    .galereya-item {
        flex: 1 1 100%;
        min-height: 100px;
        padding: 15px;
    }
    
    .galereya-item h3 {
        font-size: 14px;
    }
}

/* Katta mobil (481px - 768px) */
@media (min-width: 481px) and (max-width: 768px) {
    .responsive-galereya {
        padding: 15px;
        gap: 12px;
    }
    
    .galereya-item {
        flex: 1 1 calc(50% - 6px);
        min-height: 120px;
        padding: 18px;
    }
    
    .galereya-item h3 {
        font-size: 16px;
    }
}

/* Planshet (769px - 1024px) */
@media (min-width: 769px) and (max-width: 1024px) {
    .responsive-galereya {
        padding: 18px;
        gap: 15px;
    }
    
    .galereya-item {
        flex: 1 1 calc(33.33% - 10px);
        min-height: 140px;
        padding: 20px;
    }
    
    .galereya-item h3 {
        font-size: 18px;
    }
}

/* Desktop (1025px+) */
@media (min-width: 1025px) {
    .responsive-galereya {
        padding: 25px;
        gap: 20px;
    }
    
    .galereya-item {
        flex: 1 1 calc(25% - 15px);
        min-height: 160px;
        padding: 25px;
    }
    
    .galereya-item h3 {
        font-size: 20px;
    }
}
</style>

<div class="responsive-galereya">
    <div class="galereya-item">
        <h3>Item 1</h3>
    </div>
    <div class="galereya-item">
        <h3>Item 2</h3>
    </div>
    <div class="galereya-item">
        <h3>Item 3</h3>
    </div>
    <div class="galereya-item">
        <h3>Item 4</h3>
    </div>
    <div class="galereya-item">
        <h3>Item 5</h3>
    </div>
    <div class="galereya-item">
        <h3>Item 6</h3>
    </div>
    <div class="galereya-item">
        <h3>Item 7</h3>
    </div>
    <div class="galereya-item">
        <h3>Item 8</h3>
    </div>
</div>
```

</details>

<details>
    <summary>Mobile-first yondashuv</summary>

## 8.3 Mobile-First Yondashuv

### Mobile-first nima?

**Mobile-first** - responsive dizayn yaratishda avval mobil qurilmalar uchun dizayn qilish, keyin katta ekranlar uchun kengaytirish.

### Mobile-first vs Desktop-first

#### Desktop-first (eski usul):
```css
/* Avval desktop dizayn */
.desktop-layout {
    display: flex;
    flex-direction: row;
}

/* Keyin mobil uchun kichraytirish */
@media (max-width: 768px) {
    .desktop-layout {
        flex-direction: column;
    }
}
```

#### Mobile-first (yangi usul):
```css
/* Avval mobil dizayn */
.mobile-layout {
    display: flex;
    flex-direction: column;
}

/* Keyin desktop uchun kengaytirish */
@media (min-width: 769px) {
    .mobile-layout {
        flex-direction: row;
    }
}
```

### Mobile-first afzalliklari

#### 1. Tezroq yuklash
- Kichik ekranlar uchun kamroq CSS
- Tezroq sahifa yuklash
- Yaxshi foydalanuvchi tajribasi

#### 2. Osonroq rivojlantirish
- Oddiy dizayndan murakkabgacha
- Kamroq muammo
- Qulay test qilish

#### 3. Zamonaviy yondashuv
- Ko'pchilik mobil foydalanadi
- Google mobile-first index
- Zamonaviy web standart

### Mobile-first breakpoint'lar

#### 1. Asosiy breakpoint'lar
```css
/* Mobil (default) */
.mobile-first {
    /* Mobil CSS qoidalar */
}

/* Katta telefon */
@media (min-width: 481px) {
    .mobile-first {
        /* Katta telefon CSS qoidalar */
    }
}

/* Planshet */
@media (min-width: 769px) {
    .mobile-first {
        /* Planshet CSS qoidalar */
    }
}

/* Desktop */
@media (min-width: 1025px) {
    .mobile-first {
        /* Desktop CSS qoidalar */
    }
}
```

#### 2. Oddiy breakpoint'lar
```css
/* Mobil (default) */
.simple-mobile-first {
    /* Mobil CSS qoidalar */
}

/* Planshet va katta */
@media (min-width: 768px) {
    .simple-mobile-first {
        /* Desktop CSS qoidalar */
    }
}
```

### Amaliy misollar

#### 1. Mobile-first navigatsiya
```html
<style>
.mobile-first-nav {
    background-color: #2c3e50;
    padding: 10px;
}

.nav-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 10px;
}

.nav-logo {
    color: white;
    font-size: 1.2em;
    font-weight: bold;
    text-decoration: none;
}

.nav-menu {
    display: flex;
    flex-direction: column;
    list-style: none;
    margin: 0;
    padding: 0;
    gap: 5px;
    width: 100%;
    text-align: center;
}

.nav-menu a {
    color: white;
    text-decoration: none;
    padding: 8px 12px;
    border-radius: 4px;
    transition: background-color 0.3s ease;
}

.nav-menu a:hover {
    background-color: #34495e;
}

/* Katta telefon */
@media (min-width: 481px) {
    .nav-container {
        flex-direction: row;
        justify-content: space-between;
        gap: 20px;
    }
    
    .nav-menu {
        flex-direction: row;
        gap: 15px;
        width: auto;
    }
    
    .nav-menu a {
        padding: 10px 15px;
    }
}

/* Planshet */
@media (min-width: 769px) {
    .mobile-first-nav {
        padding: 15px 20px;
    }
    
    .nav-logo {
        font-size: 1.4em;
    }
    
    .nav-menu {
        gap: 25px;
    }
    
    .nav-menu a {
        padding: 12px 18px;
        font-size: 16px;
    }
}

/* Desktop */
@media (min-width: 1025px) {
    .mobile-first-nav {
        padding: 20px;
    }
    
    .nav-container {
        max-width: 1200px;
        margin: 0 auto;
    }
    
    .nav-logo {
        font-size: 1.6em;
    }
    
    .nav-menu {
        gap: 35px;
    }
    
    .nav-menu a {
        padding: 15px 20px;
        font-size: 18px;
    }
}
</style>

<nav class="mobile-first-nav">
    <div class="nav-container">
        <a href="#" class="nav-logo">Mobile First</a>
        <ul class="nav-menu">
            <li><a href="#">Bosh sahifa</a></li>
            <li><a href="#">Xizmatlar</a></li>
            <li><a href="#">Portfolio</a></li>
            <li><a href="#">Aloqa</a></li>
        </ul>
    </div>
</nav>
```

#### 2. Mobile-first layout
```html
<style>
.mobile-first-layout {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
    padding: 10px;
}

.layout-header {
    background-color: #34495e;
    color: white;
    padding: 15px;
    text-align: center;
    border-radius: 8px;
    margin-bottom: 15px;
}

.layout-main {
    display: flex;
    flex-direction: column;
    gap: 15px;
    flex: 1;
}

.layout-content {
    background-color: white;
    padding: 15px;
    border: 1px solid #e0e0e0;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.layout-sidebar {
    background-color: #f8f9fa;
    padding: 15px;
    border: 1px solid #e0e0e0;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.layout-footer {
    background-color: #2c3e50;
    color: white;
    padding: 15px;
    text-align: center;
    border-radius: 8px;
    margin-top: 15px;
}

.layout-header h1 {
    margin: 0;
    font-size: 1.3em;
}

.layout-content h2,
.layout-sidebar h3 {
    color: #2c3e50;
    margin-top: 0;
    font-size: 1.1em;
}

.layout-sidebar ul {
    list-style: none;
    padding: 0;
}

.layout-sidebar li {
    padding: 6px 0;
    border-bottom: 1px solid #e0e0e0;
}

.layout-sidebar a {
    color: #3498db;
    text-decoration: none;
    font-size: 14px;
}

/* Katta telefon */
@media (min-width: 481px) {
    .mobile-first-layout {
        padding: 15px;
    }
    
    .layout-header,
    .layout-content,
    .layout-sidebar {
        padding: 18px;
    }
    
    .layout-header h1 {
        font-size: 1.5em;
    }
    
    .layout-content h2,
    .layout-sidebar h3 {
        font-size: 1.3em;
    }
}

/* Planshet */
@media (min-width: 769px) {
    .mobile-first-layout {
        padding: 20px;
    }
    
    .layout-main {
        flex-direction: row;
        gap: 20px;
    }
    
    .layout-content {
        flex: 2;
    }
    
    .layout-sidebar {
        flex: 1;
    }
    
    .layout-header,
    .layout-content,
    .layout-sidebar {
        padding: 20px;
    }
    
    .layout-header h1 {
        font-size: 1.8em;
    }
    
    .layout-content h2,
    .layout-sidebar h3 {
        font-size: 1.5em;
    }
    
    .layout-sidebar a {
        font-size: 16px;
    }
}

/* Desktop */
@media (min-width: 1025px) {
    .mobile-first-layout {
        max-width: 1200px;
        margin: 0 auto;
        padding: 25px;
    }
    
    .layout-main {
        gap: 25px;
    }
    
    .layout-header,
    .layout-content,
    .layout-sidebar {
        padding: 25px;
    }
    
    .layout-header h1 {
        font-size: 2.2em;
    }
    
    .layout-content h2,
    .layout-sidebar h3 {
        font-size: 1.8em;
    }
    
    .layout-content p,
    .layout-sidebar a {
        font-size: 16px;
        line-height: 1.6;
    }
}
</style>

<div class="mobile-first-layout">
    <header class="layout-header">
        <h1>Mobile-First Layout</h1>
        <p>Avval mobil, keyin desktop</p>
    </header>
    
    <main class="layout-main">
        <div class="layout-content">
            <h2>Asosiy mazmun</h2>
            <p>Bu layout mobile-first yondashuv bilan yaratilgan. Avval mobil dizayn, keyin katta ekranlar uchun kengaytirilgan.</p>
            
            <h3>Mobile-first afzalliklari:</h3>
            <ul>
                <li>Tezroq yuklash</li>
                <li>Osonroq rivojlantirish</li>
                <li>Zamonaviy yondashuv</li>
                <li>Yaxshi SEO</li>
            </ul>
        </div>
        
        <div class="layout-sidebar">
            <h3>Yon panel</h3>
            <ul>
                <li><a href="#">Mobile First</a></li>
                <li><a href="#">Responsive Design</a></li>
                <li><a href="#">Media Queries</a></li>
                <li><a href="#">Flexbox</a></li>
                <li><a href="#">CSS Grid</a></li>
            </ul>
        </div>
    </main>
    
    <footer class="layout-footer">
        <p>&copy; 2024 Mobile-First Layout</p>
    </footer>
</div>
```

#### 3. Mobile-first kartochkalar
```html
<style>
.mobile-first-cards {
    display: flex;
    flex-direction: column;
    gap: 15px;
    padding: 15px;
}

.card {
    background-color: white;
    border: 2px solid #e0e0e0;
    border-radius: 8px;
    padding: 15px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.card h3 {
    color: #2c3e50;
    margin: 0 0 10px 0;
    font-size: 1.1em;
}

.card p {
    color: #666;
    margin: 0;
    font-size: 14px;
    line-height: 1.4;
}

/* Katta telefon */
@media (min-width: 481px) {
    .mobile-first-cards {
        flex-direction: row;
        flex-wrap: wrap;
        gap: 12px;
        padding: 18px;
    }
    
    .card {
        flex: 1 1 calc(50% - 6px);
        padding: 18px;
    }
    
    .card h3 {
        font-size: 1.2em;
    }
    
    .card p {
        font-size: 15px;
        line-height: 1.5;
    }
}

/* Planshet */
@media (min-width: 769px) {
    .mobile-first-cards {
        gap: 15px;
        padding: 20px;
    }
    
    .card {
        flex: 1 1 calc(33.33% - 10px);
        padding: 20px;
    }
    
    .card h3 {
        font-size: 1.3em;
        margin-bottom: 12px;
    }
    
    .card p {
        font-size: 16px;
        line-height: 1.6;
    }
}

/* Desktop */
@media (min-width: 1025px) {
    .mobile-first-cards {
        max-width: 1200px;
        margin: 0 auto;
        gap: 20px;
        padding: 25px;
    }
    
    .card {
        flex: 1 1 calc(25% - 15px);
        padding: 25px;
    }
    
    .card h3 {
        font-size: 1.4em;
        margin-bottom: 15px;
    }
    
    .card p {
        font-size: 17px;
        line-height: 1.7;
    }
}
</style>

<div class="mobile-first-cards">
    <div class="card">
        <h3>Mobile First</h3>
        <p>Avval mobil dizayn qiling, keyin katta ekranlar uchun kengaytiring.</p>
    </div>
    
    <div class="card">
        <h3>Responsive</h3>
        <p>Turli ekran o'lchamlarida yaxshi ko'rinadigan dizayn yarating.</p>
    </div>
    
    <div class="card">
        <h3>Fast Loading</h3>
        <p>Kichik ekranlar uchun kamroq CSS, tezroq yuklash.</p>
    </div>
    
    <div class="card">
        <h3>Modern</h3>
        <p>Zamonaviy web-dizayn standartlari va yondashuvlari.</p>
    </div>
</div>
```

</details>

<details>
    <summary>Viewport meta tegi</summary>

## 8.4 Viewport Meta Tegi

### Viewport nima?

**Viewport** - foydalanuvchi brauzerida ko'rinadigan sahifa maydoni. Bu mobil qurilmalarda juda muhim.

### Viewport muammosi

#### Muammo:
- Mobil brauzerlar sahifani kichikroq ko'rsatadi
- Matn juda kichik bo'ladi
- Foydalanuvchi zoom qilishi kerak

#### Yechim:
- Viewport meta tegi qo'shish
- Brauzerga sahifa o'lchamini aytish
- Responsive dizayn uchun kerak

### Viewport meta tegi

#### 1. Asosiy viewport tegi
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

#### 2. Viewport parametrlari
```html
<!-- To'liq parametrlar -->
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
```

#### 3. Parametrlar tushuntirish
- **width=device-width**: Sahifa kengligi = qurilma kengligi
- **initial-scale=1.0**: Boshlang'ich zoom = 100%
- **maximum-scale=1.0**: Maksimal zoom = 100%
- **user-scalable=no**: Foydalanuvchi zoom qila olmaydi

### HTML head qismida joylash

#### To'g'ri joylashtirish:
```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Sahifa</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <!-- Sahifa mazmuni -->
</body>
</html>
```

### Amaliy misollar

#### 1. Viewport taqqoslash
```html
<style>
.viewport-demo {
    max-width: 800px;
    margin: 20px auto;
    padding: 20px;
    background-color: #f8f9fa;
    border: 2px solid #dee2e6;
    border-radius: 8px;
}

.viewport-demo h2 {
    color: #2c3e50;
    margin-top: 0;
}

.viewport-demo p {
    color: #666;
    line-height: 1.6;
    margin-bottom: 15px;
}

.viewport-demo .warning {
    background-color: #fff3cd;
    border: 1px solid #ffeaa7;
    padding: 15px;
    border-radius: 5px;
    color: #856404;
    margin: 15px 0;
}

.viewport-demo .success {
    background-color: #d4edda;
    border: 1px solid #c3e6cb;
    padding: 15px;
    border-radius: 5px;
    color: #155724;
    margin: 15px 0;
}

@media (max-width: 768px) {
    .viewport-demo {
        margin: 10px;
        padding: 15px;
    }
    
    .viewport-demo h2 {
        font-size: 1.3em;
    }
    
    .viewport-demo p {
        font-size: 16px;
    }
}
</style>

<div class="viewport-demo">
    <h2>Viewport Meta Tegi</h2>
    
    <p>Viewport meta tegi responsive dizayn uchun juda muhim. U brauzerga sahifa o'lchamini aytadi.</p>
    
    <div class="warning">
        <strong>Eslatma:</strong> Agar viewport meta tegi bo'lmasa, sahifa mobil qurilmalarda kichik ko'rinadi va foydalanuvchi zoom qilishi kerak bo'ladi.
    </div>
    
    <div class="success">
        <strong>To'g'ri:</strong> Viewport meta tegi bilan sahifa barcha qurilmalarda yaxshi ko'rinadi va responsive bo'ladi.
    </div>
    
    <h3>Viewport tegi qo'shish:</h3>
    <p>HTML head qismiga quyidagi tegni qo'shing:</p>
    <code>&lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;</code>
</div>
```

#### 2. Viewport test sahifasi
```html
<style>
.viewport-test {
    padding: 20px;
    background-color: #e8f5e8;
    border: 2px solid #4caf50;
    border-radius: 8px;
    margin: 20px 0;
}

.viewport-test h3 {
    color: #2e7d32;
    margin-top: 0;
}

.viewport-info {
    background-color: white;
    padding: 15px;
    border-radius: 5px;
    margin: 15px 0;
    font-family: monospace;
    font-size: 14px;
}

@media (max-width: 480px) {
    .viewport-test {
        padding: 15px;
        margin: 15px 10px;
    }
    
    .viewport-test h3 {
        font-size: 1.2em;
    }
    
    .viewport-info {
        font-size: 12px;
        padding: 12px;
    }
}

@media (min-width: 481px) and (max-width: 768px) {
    .viewport-test {
        padding: 18px;
    }
    
    .viewport-test h3 {
        font-size: 1.4em;
    }
}

@media (min-width: 769px) {
    .viewport-test {
        padding: 25px;
        max-width: 800px;
        margin: 20px auto;
    }
    
    .viewport-test h3 {
        font-size: 1.6em;
    }
    
    .viewport-info {
        font-size: 16px;
        padding: 20px;
    }
}
</style>

<div class="viewport-test">
    <h3>Viewport Test</h3>
    <p>Bu sahifa viewport meta tegi bilan yaratilgan. Ekran o'lchamini o'zgartiring va farqni kuzating.</p>
    
    <div class="viewport-info">
        <strong>Viewport meta tegi:</strong><br>
        &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    </div>
    
    <p>Bu tegi HTML head qismiga qo'shing va sahifa barcha qurilmalarda yaxshi ko'rinadi!</p>
</div>
```

</details>

<details>
    <summary>Responsive rasmlar</summary>

## 8.5 Responsive Rasmlar

### Responsive rasmlar nima?

**Responsive rasmlar** - turli ekran o'lchamlarida yaxshi ko'rinadigan va moslashuvchan rasm.

### Rasm muammolari

#### 1. Katta rasm muammosi
- Rasm konteyneridan katta
- Gorizontal scroll paydo bo'ladi
- Sahifa buziladi

#### 2. Kichik rasm muammosi
- Rasm juda kichik ko'rinadi
- Pixelated (pixelli) ko'rinish
- Yaxshi ko'rinmaydi

### Responsive rasm yechimlari

#### 1. CSS max-width
```css
.responsive-img {
    max-width: 100%;
    height: auto;
}
```

#### 2. CSS width va height
```css
.responsive-img {
    width: 100%;
    height: auto;
}
```

#### 3. CSS object-fit
```css
.responsive-img {
    width: 100%;
    height: 300px;
    object-fit: cover;
}
```

### Object-fit xususiyatlari

#### 1. Cover - qoplash
```css
.object-cover {
    object-fit: cover;
}
```

#### 2. Contain - o'z ichiga olish
```css
.object-contain {
    object-fit: contain;
}
```

#### 3. Fill - to'ldirish
```css
.object-fill {
    object-fit: fill;
}
```

### Amaliy misollar

#### 1. Oddiy responsive rasm
```html
<style>
.rasm-demo {
    max-width: 800px;
    margin: 20px auto;
    padding: 20px;
    background-color: #f8f9fa;
    border: 2px solid #dee2e6;
    border-radius: 8px;
}

.responsive-rasm {
    max-width: 100%;
    height: auto;
    border-radius: 8px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}

.rasm-demo h3 {
    color: #2c3e50;
    margin-top: 0;
}

.rasm-demo p {
    color: #666;
    line-height: 1.6;
}

@media (max-width: 768px) {
    .rasm-demo {
        margin: 10px;
        padding: 15px;
    }
    
    .rasm-demo h3 {
        font-size: 1.3em;
    }
    
    .rasm-demo p {
        font-size: 16px;
    }
}
</style>

<div class="rasm-demo">
    <h3>Responsive Rasm</h3>
    <p>Bu rasm barcha ekran o'lchamlarida yaxshi ko'rinadi.</p>
    
    <img src="https://via.placeholder.com/800x400/4CAF50/white?text=Responsive+Image" 
         alt="Responsive rasm" 
         class="responsive-rasm">
    
    <p>Rasm max-width: 100% va height: auto xususiyatlari bilan responsive qilingan.</p>
</div>
```

#### 2. Object-fit misollari
```html
<style>
.object-fit-demo {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    padding: 20px;
    max-width: 1200px;
    margin: 0 auto;
}

.object-fit-item {
    flex: 1 1 300px;
    background-color: white;
    border: 2px solid #e0e0e0;
    border-radius: 8px;
    padding: 15px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}

.object-fit-item h4 {
    color: #2c3e50;
    margin: 0 0 10px 0;
    text-align: center;
}

.object-fit-img {
    width: 100%;
    height: 200px;
    border-radius: 5px;
}

.cover-img {
    object-fit: cover;
}

.contain-img {
    object-fit: contain;
    background-color: #f0f0f0;
}

.fill-img {
    object-fit: fill;
}

@media (max-width: 768px) {
    .object-fit-demo {
        flex-direction: column;
        padding: 15px;
    }
    
    .object-fit-item {
        flex: none;
    }
    
    .object-fit-img {
        height: 150px;
    }
}

@media (min-width: 769px) and (max-width: 1024px) {
    .object-fit-item {
        flex: 1 1 calc(50% - 10px);
    }
}
</style>

<div class="object-fit-demo">
    <div class="object-fit-item">
        <h4>Cover</h4>
        <img src="https://via.placeholder.com/400x300/2196F3/white?text=Cover" 
             alt="Cover rasm" 
             class="object-fit-img cover-img">
        <p>Rasm konteynerni to'liq qoplaydi, qismlari kesilishi mumkin.</p>
    </div>
    
    <div class="object-fit-item">
        <h4>Contain</h4>
        <img src="https://via.placeholder.com/400x300/FF9800/white?text=Contain" 
             alt="Contain rasm" 
             class="object-fit-img contain-img">
        <p>Rasm to'liq ko'rinadi, bo'sh joy qolishi mumkin.</p>
    </div>
    
    <div class="object-fit-item">
        <h4>Fill</h4>
        <img src="https://via.placeholder.com/400x300/4CAF50/white?text=Fill" 
             alt="Fill rasm" 
             class="object-fit-img fill-img">
        <p>Rasm konteynerni to'ldiradi, buzilishi mumkin.</p>
    </div>
</div>
```

#### 3. Responsive rasm galereyasi
```html
<style>
.rasm-galereya {
    display: flex;
    flex-wrap: wrap;
    gap: 15px;
    padding: 20px;
    max-width: 1200px;
    margin: 0 auto;
}

.galereya-item {
    flex: 1 1 250px;
    background-color: white;
    border: 2px solid #e0e0e0;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    transition: transform 0.3s ease;
}

.galereya-item:hover {
    transform: translateY(-5px);
    box-shadow: 0 4px 15px rgba(0,0,0,0.2);
}

.galereya-rasm {
    width: 100%;
    height: 200px;
    object-fit: cover;
}

.galereya-content {
    padding: 15px;
}

.galereya-content h4 {
    color: #2c3e50;
    margin: 0 0 8px 0;
    font-size: 1.1em;
}

.galereya-content p {
    color: #666;
    margin: 0;
    font-size: 14px;
    line-height: 1.4;
}

/* Kichik mobil */
@media (max-width: 480px) {
    .rasm-galereya {
        padding: 10px;
        gap: 10px;
    }
    
    .galereya-item {
        flex: 1 1 100%;
    }
    
    .galereya-rasm {
        height: 150px;
    }
    
    .galereya-content {
        padding: 12px;
    }
    
    .galereya-content h4 {
        font-size: 1em;
    }
    
    .galereya-content p {
        font-size: 13px;
    }
}

/* Katta mobil */
@media (min-width: 481px) and (max-width: 768px) {
    .rasm-galereya {
        padding: 15px;
        gap: 12px;
    }
    
    .galereya-item {
        flex: 1 1 calc(50% - 6px);
    }
    
    .galereya-rasm {
        height: 180px;
    }
}

/* Planshet */
@media (min-width: 769px) and (max-width: 1024px) {
    .galereya-item {
        flex: 1 1 calc(33.33% - 10px);
    }
    
    .galereya-rasm {
        height: 200px;
    }
}

/* Desktop */
@media (min-width: 1025px) {
    .rasm-galereya {
        padding: 25px;
        gap: 20px;
    }
    
    .galereya-item {
        flex: 1 1 calc(25% - 15px);
    }
    
    .galereya-rasm {
        height: 220px;
    }
    
    .galereya-content {
        padding: 18px;
    }
    
    .galereya-content h4 {
        font-size: 1.2em;
    }
    
    .galereya-content p {
        font-size: 15px;
        line-height: 1.5;
    }
}
</style>

<div class="rasm-galereya">
    <div class="galereya-item">
        <img src="https://via.placeholder.com/400x300/E91E63/white?text=Nature+1" 
             alt="Tabiat 1" 
             class="galereya-rasm">
        <div class="galereya-content">
            <h4>Tabiat 1</h4>
            <p>Responsive rasm galereyasi misoli</p>
        </div>
    </div>
    
    <div class="galereya-item">
        <img src="https://via.placeholder.com/400x300/9C27B0/white?text=Nature+2" 
             alt="Tabiat 2" 
             class="galereya-rasm">
        <div class="galereya-content">
            <h4>Tabiat 2</h4>
            <p>Object-fit: cover bilan</p>
        </div>
    </div>
    
    <div class="galereya-item">
        <img src="https://via.placeholder.com/400x300/3F51B5/white?text=Nature+3" 
             alt="Tabiat 3" 
             class="galereya-rasm">
        <div class="galereya-content">
            <h4>Tabiat 3</h4>
            <p>Turli ekran o'lchamlari</p>
        </div>
    </div>
    
    <div class="galereya-item">
        <img src="https://via.placeholder.com/400x300/009688/white?text=Nature+4" 
             alt="Tabiat 4" 
             class="galereya-rasm">
        <div class="galereya-content">
            <h4>Tabiat 4</h4>
            <p>Responsive dizayn</p>
        </div>
    </div>
    
    <div class="galereya-item">
        <img src="https://via.placeholder.com/400x300/FF5722/white?text=Nature+5" 
             alt="Tabiat 5" 
             class="galereya-rasm">
        <div class="galereya-content">
            <h4>Tabiat 5</h4>
            <p>Flexbox layout</p>
        </div>
    </div>
    
    <div class="galereya-item">
        <img src="https://via.placeholder.com/400x300/795548/white?text=Nature+6" 
             alt="Tabiat 6" 
             class="galereya-rasm">
        <div class="galereya-content">
            <h4>Tabiat 6</h4>
            <p>Media queries</p>
        </div>
    </div>
</div>
```

</details>
