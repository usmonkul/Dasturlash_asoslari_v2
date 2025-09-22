<details>
    <summary>HTML jadvallar (table, tr, td, th)</summary>

## 5.1 HTML Jadvallar (table, tr, td, th)

### Jadval nima?

**HTML jadval** - bu ma'lumotlarni qatorlar va ustunlar ko'rinishida tartibli tarzda ko'rsatish uchun ishlatiladi. Jadvallar turli xil ma'lumotlarni tashkil etish uchun juda qulay.

### Asosiy jadval teglari

#### 1. `<table>` - asosiy jadval konteyner
```html
<table>
    <!-- Jadval mazmuni bu yerda -->
</table>
```

#### 2. `<tr>` - jadval qatori (Table Row)
```html
<tr>
    <!-- Qator mazmuni -->
</tr>
```

#### 3. `<td>` - oddiy katakcha (Table Data)
```html
<td>Ma'lumot</td>
```

#### 4. `<th>` - sarlavha katakchasi (Table Header)
```html
<th>Sarlavha</th>
```

### Oddiy jadval yaratish

#### Asosiy jadval strukturasi
```html
<table>
    <tr>
        <th>Ism</th>
        <th>Yosh</th>
        <th>Shahar</th>
    </tr>
    <tr>
        <td>Ahmad</td>
        <td>25</td>
        <td>Toshkent</td>
    </tr>
    <tr>
        <td>Fatima</td>
        <td>22</td>
        <td>Samarqand</td>
    </tr>
</table>
```

### Qo'shimcha jadval teglari

#### 1. `<thead>` - jadval boshi
```html
<table>
    <thead>
        <tr>
            <th>Mahsulot</th>
            <th>Narx</th>
            <th>Soni</th>
        </tr>
    </thead>
</table>
```

#### 2. `<tbody>` - jadval tanasi
```html
<tbody>
    <tr>
        <td>Olma</td>
        <td>5000</td>
        <td>10</td>
    </tr>
    <tr>
        <td>Banan</td>
        <td>8000</td>
        <td>5</td>
    </tr>
</tbody>
```

#### 3. `<tfoot>` - jadval oyog'i
```html
<tfoot>
    <tr>
        <td>Jami</td>
        <td>13000</td>
        <td>15</td>
    </tr>
</tfoot>
```

### Katakchalarni birlashtirish

#### 1. Colspan - ustun bo'yicha birlashtirish
```html
<table>
    <tr>
        <th colspan="3">O'quvchilar ro'yxati</th>
    </tr>
    <tr>
        <th>Ism</th>
        <th>Sinf</th>
        <th>Baho</th>
    </tr>
    <tr>
        <td>Ali</td>
        <td>7-A</td>
        <td>5</td>
    </tr>
</table>
```

#### 2. Rowspan - qator bo'yicha birlashtirish
```html
<table>
    <tr>
        <th>Fan</th>
        <th>Dars vaqti</th>
        <th>O'qituvchi</th>
    </tr>
    <tr>
        <td rowspan="2">Matematika</td>
        <td>8:00-8:45</td>
        <td>Karimov A.</td>
    </tr>
    <tr>
        <td>9:00-9:45</td>
        <td>Karimov A.</td>
    </tr>
</table>
```

### Jadval atributlari

#### 1. Border atributi (eski usul)
```html
<table border="1">
    <tr>
        <td>Katakcha 1</td>
        <td>Katakcha 2</td>
    </tr>
</table>
```

#### 2. Cellpadding va Cellspacing (eski usul)
```html
<table border="1" cellpadding="10" cellspacing="5">
    <tr>
        <td>Matn</td>
        <td>Matn</td>
    </tr>
</table>
```

**Eslatma:** Zamonaviy web-dasturlashda CSS ishlatish yaxshiroq!

### Amaliy misollar

#### 1. O'quvchilar jadvali
```html
<table>
    <thead>
        <tr>
            <th>№</th>
            <th>Ism Familiya</th>
            <th>Sinf</th>
            <th>Matematika</th>
            <th>Fizika</th>
            <th>Kimyo</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>Ahmad Karimov</td>
            <td>9-A</td>
            <td>5</td>
            <td>4</td>
            <td>5</td>
        </tr>
        <tr>
            <td>2</td>
            <td>Fatima Yusupova</td>
            <td>9-A</td>
            <td>4</td>
            <td>5</td>
            <td>4</td>
        </tr>
        <tr>
            <td>3</td>
            <td>Bobur Rahmonov</td>
            <td>9-A</td>
            <td>5</td>
            <td>5</td>
            <td>5</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td colspan="3">O'rtacha ball</td>
            <td>4.7</td>
            <td>4.7</td>
            <td>4.7</td>
        </tr>
    </tfoot>
</table>
```

#### 2. Dars jadvali
```html
<table>
    <thead>
        <tr>
            <th>Vaqt</th>
            <th>Dushanba</th>
            <th>Seshanba</th>
            <th>Chorshanba</th>
            <th>Payshanba</th>
            <th>Juma</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>8:00-8:45</td>
            <td>Matematika</td>
            <td>Fizika</td>
            <td>Kimyo</td>
            <td>Biologiya</td>
            <td>Tarix</td>
        </tr>
        <tr>
            <td>9:00-9:45</td>
            <td>O'zbek tili</td>
            <td>Ingliz tili</td>
            <td>Matematika</td>
            <td>Fizika</td>
            <td>Geografiya</td>
        </tr>
        <tr>
            <td>10:00-10:45</td>
            <td>Jismoniy tarbiya</td>
            <td>Matematika</td>
            <td>Ingliz tili</td>
            <td>Adabiyot</td>
            <td>Informatika</td>
        </tr>
    </tbody>
</table>
```

#### 3. Mahsulotlar katalogi
```html
<table>
    <caption>Elektronika mahsulotlari</caption>
    <thead>
        <tr>
            <th rowspan="2">Mahsulot</th>
            <th colspan="2">Narx (so'm)</th>
            <th rowspan="2">Mavjudligi</th>
        </tr>
        <tr>
            <th>Eski</th>
            <th>Yangi</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Telefon</td>
            <td>2,500,000</td>
            <td>2,200,000</td>
            <td>Bor</td>
        </tr>
        <tr>
            <td>Noutbuk</td>
            <td>8,000,000</td>
            <td>7,500,000</td>
            <td>Tugagan</td>
        </tr>
        <tr>
            <td>Planshet</td>
            <td>1,500,000</td>
            <td>1,300,000</td>
            <td>Bor</td>
        </tr>
    </tbody>
</table>
```

</details>

<details>
    <summary>Jadvallarni CSS bilan bezatish</summary>

## 5.2 Jadvallarni CSS bilan Bezatish

### Asosiy jadval stillar

#### 1. Jadval chegaralari
```css
table {
    border: 1px solid #333;          /* Jadval chegarasi */
    border-collapse: collapse;       /* Chegaralarni birlashtirish */
    width: 100%;                     /* To'liq kenglik */
}

th, td {
    border: 1px solid #ddd;          /* Katakcha chegaralari */
    padding: 8px;                    /* Ichki bo'shliq */
    text-align: left;                /* Matn joylashuvi */
}
```

#### 2. Sarlavha stillar
```css
th {
    background-color: #f2f2f2;       /* Fon rangi */
    font-weight: bold;               /* Qalin harflar */
    color: #333;                     /* Matn rangi */
    text-align: center;              /* Markazga joylashtirish */
}
```

#### 3. Qator stillari
```css
tr:nth-child(even) {
    background-color: #f9f9f9;       /* Juft qatorlar rangi */
}

tr:nth-child(odd) {
    background-color: white;         /* Toq qatorlar rangi */
}

tr:hover {
    background-color: #e6f3ff;       /* Hover rangi */
}
```

### Responsive jadvallar

#### 1. Kichik ekranlar uchun
```css
.responsive-table {
    overflow-x: auto;                /* Gorizontal scroll */
    width: 100%;
}

.responsive-table table {
    min-width: 600px;                /* Minimal kenglik */
}

@media (max-width: 768px) {
    .responsive-table table {
        font-size: 14px;              /* Kichik shrift */
    }
    
    .responsive-table th,
    .responsive-table td {
        padding: 5px;                 /* Kichik padding */
    }
}
```

#### 2. Mobil uchun kartochka ko'rinishi
```css
@media (max-width: 600px) {
    .mobile-table table,
    .mobile-table thead,
    .mobile-table tbody,
    .mobile-table th,
    .mobile-table td,
    .mobile-table tr {
        display: block;
    }
    
    .mobile-table thead tr {
        position: absolute;
        top: -9999px;
        left: -9999px;
    }
    
    .mobile-table tr {
        border: 1px solid #ccc;
        margin-bottom: 10px;
        padding: 10px;
        border-radius: 5px;
    }
    
    .mobile-table td {
        border: none;
        position: relative;
        padding-left: 50%;
    }
    
    .mobile-table td:before {
        content: attr(data-label) ": ";
        position: absolute;
        left: 6px;
        width: 45%;
        font-weight: bold;
    }
}
```

### Zamonaviy jadval dizayni

#### 1. Minimal dizayn
```css
.modern-table {
    border-collapse: collapse;
    width: 100%;
    background-color: white;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    border-radius: 8px;
    overflow: hidden;
}

.modern-table th {
    background-color: #4a90e2;
    color: white;
    font-weight: 600;
    padding: 15px;
    text-align: left;
    font-size: 14px;
    text-transform: uppercase;
    letter-spacing: 0.5px;
}

.modern-table td {
    padding: 15px;
    border-bottom: 1px solid #e0e0e0;
    font-size: 14px;
    color: #333;
}

.modern-table tr:last-child td {
    border-bottom: none;
}

.modern-table tr:hover {
    background-color: #f8f9fa;
}
```

#### 2. Rangli jadval
```css
.colorful-table {
    border-collapse: collapse;
    width: 100%;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
}

.colorful-table th {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 15px;
    text-align: center;
    font-weight: bold;
}

.colorful-table td {
    padding: 12px;
    text-align: center;
    border-bottom: 1px solid #e0e0e0;
}

.colorful-table tr:nth-child(odd) {
    background-color: #f8f9fa;
}

.colorful-table tr:nth-child(even) {
    background-color: white;
}

.colorful-table tr:hover {
    background: linear-gradient(135deg, #667eea15, #764ba215);
    transform: scale(1.02);
    transition: all 0.3s ease;
}
```

### Amaliy misollar

#### 1. O'quvchilar jadvali - zamonaviy dizayn
```html
<style>
.students-table {
    border-collapse: collapse;
    width: 100%;
    max-width: 800px;
    margin: 20px auto;
    background-color: white;
    box-shadow: 0 5px 15px rgba(0,0,0,0.08);
    border-radius: 10px;
    overflow: hidden;
}

.students-table th {
    background: linear-gradient(135deg, #2c3e50, #34495e);
    color: white;
    padding: 15px 10px;
    text-align: center;
    font-weight: 600;
    font-size: 13px;
    text-transform: uppercase;
    letter-spacing: 0.5px;
}

.students-table td {
    padding: 12px 10px;
    text-align: center;
    border-bottom: 1px solid #ecf0f1;
    font-size: 14px;
    color: #2c3e50;
}

.students-table tr:nth-child(even) {
    background-color: #f8f9fa;
}

.students-table tr:hover {
    background-color: #e3f2fd;
    transform: translateY(-1px);
    transition: all 0.3s ease;
}

.students-table .grade {
    font-weight: bold;
    padding: 5px 8px;
    border-radius: 15px;
    color: white;
}

.grade-5 { background-color: #4caf50; }
.grade-4 { background-color: #2196f3; }
.grade-3 { background-color: #ff9800; }
.grade-2 { background-color: #f44336; }

.total-row {
    background: linear-gradient(135deg, #e3f2fd, #bbdefb);
    font-weight: bold;
    color: #1976d2;
}
</style>

<table class="students-table">
    <thead>
        <tr>
            <th>№</th>
            <th>Ism Familiya</th>
            <th>Sinf</th>
            <th>Matematika</th>
            <th>Fizika</th>
            <th>Kimyo</th>
            <th>O'rtacha</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>Ahmad Karimov</td>
            <td>9-A</td>
            <td><span class="grade grade-5">5</span></td>
            <td><span class="grade grade-4">4</span></td>
            <td><span class="grade grade-5">5</span></td>
            <td>4.7</td>
        </tr>
        <tr>
            <td>2</td>
            <td>Fatima Yusupova</td>
            <td>9-A</td>
            <td><span class="grade grade-4">4</span></td>
            <td><span class="grade grade-5">5</span></td>
            <td><span class="grade grade-4">4</span></td>
            <td>4.3</td>
        </tr>
        <tr class="total-row">
            <td colspan="3">Sinf o'rtachasi</td>
            <td>4.5</td>
            <td>4.5</td>
            <td>4.5</td>
            <td>4.5</td>
        </tr>
    </tbody>
</table>
```

#### 2. Mahsulotlar katalogi - kartochka ko'rinishi
```html
<style>
.products-table {
    border-collapse: collapse;
    width: 100%;
    background-color: white;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 4px 20px rgba(0,0,0,0.08);
}

.products-table th {
    background: linear-gradient(135deg, #667eea, #764ba2);
    color: white;
    padding: 18px 15px;
    text-align: left;
    font-weight: 600;
    position: relative;
}

.products-table th:first-child {
    border-radius: 12px 0 0 0;
}

.products-table th:last-child {
    border-radius: 0 12px 0 0;
}

.products-table td {
    padding: 15px;
    border-bottom: 1px solid #f0f0f0;
    vertical-align: middle;
}

.products-table tr:hover {
    background: linear-gradient(135deg, #667eea08, #764ba208);
}

.price-old {
    text-decoration: line-through;
    color: #999;
    font-size: 12px;
}

.price-new {
    color: #e74c3c;
    font-weight: bold;
    font-size: 16px;
}

.status {
    padding: 5px 12px;
    border-radius: 20px;
    font-size: 12px;
    font-weight: 600;
    text-transform: uppercase;
}

.status-available {
    background-color: #d4edda;
    color: #155724;
}

.status-out {
    background-color: #f8d7da;
    color: #721c24;
}
</style>

<table class="products-table">
    <thead>
        <tr>
            <th>Mahsulot</th>
            <th>Eski narx</th>
            <th>Yangi narx</th>
            <th>Chegirma</th>
            <th>Holati</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>iPhone 14 Pro</td>
            <td><span class="price-old">15,000,000 so'm</span></td>
            <td><span class="price-new">13,500,000 so'm</span></td>
            <td>10%</td>
            <td><span class="status status-available">Mavjud</span></td>
        </tr>
        <tr>
            <td>Samsung Galaxy S23</td>
            <td><span class="price-old">12,000,000 so'm</span></td>
            <td><span class="price-new">10,800,000 so'm</span></td>
            <td>10%</td>
            <td><span class="status status-out">Tugagan</span></td>
        </tr>
        <tr>
            <td>MacBook Air M2</td>
            <td><span class="price-old">18,000,000 so'm</span></td>
            <td><span class="price-new">16,200,000 so'm</span></td>
            <td>10%</td>
            <td><span class="status status-available">Mavjud</span></td>
        </tr>
    </tbody>
</table>
```

</details>

<details>
    <summary>Box model tushunchasi (margin, padding, border)</summary>

## 5.3 Box Model Tushunchasi (margin, padding, border)

### Box Model nima?

**CSS Box Model** - bu har bir HTML elementning qanday joy egallashini tushuntiruvchi model. Har bir element to'rtburchaklar shaklida bo'lib, quyidagi qismlardan iborat:

1. **Content** - asosiy mazmun (matn, rasm)
2. **Padding** - mazmun va chegara orasidagi ichki bo'shliq
3. **Border** - element atrofidagi chegara
4. **Margin** - element va boshqa elementlar orasidagi tashqi bo'shliq

### Box Model diagrammasi

```
┌─────────────────────────────────────┐ ← Margin (tashqi)
│  ┌─────────────────────────────────┐ │ ← Border (chegara)
│  │  ┌─────────────────────────────┐ │ │ ← Padding (ichki)
│  │  │                             │ │ │
│  │  │          CONTENT            │ │ │ ← Content (mazmun)
│  │  │                             │ │ │
│  │  └─────────────────────────────┘ │ │
│  └─────────────────────────────────┘ │
└─────────────────────────────────────┘
```

### Padding - ichki bo'shliq

#### 1. Barcha tomonlar uchun bir xil
```css
.box {
    padding: 20px;                   /* Barcha tomonlarda 20px */
}
```

#### 2. Har bir tomon uchun alohida
```css
.box {
    padding-top: 10px;               /* Yuqori */
    padding-right: 15px;             /* O'ng */
    padding-bottom: 10px;            /* Pastki */
    padding-left: 15px;              /* Chap */
}
```

#### 3. Qisqa yozish usullari
```css
.box {
    padding: 10px 15px;              /* Yuqori-pastki: 10px, Chap-o'ng: 15px */
    padding: 10px 15px 20px;         /* Yuqori: 10px, Chap-o'ng: 15px, Pastki: 20px */
    padding: 10px 15px 20px 25px;    /* Yuqori, O'ng, Pastki, Chap (soat yo'nalishi) */
}
```

### Border - chegara

#### 1. Asosiy border xususiyatlari
```css
.box {
    border-width: 2px;               /* Qalinlik */
    border-style: solid;             /* Stil */
    border-color: #333;              /* Rang */
}

/* Yoki qisqa usul */
.box {
    border: 2px solid #333;
}
```

#### 2. Border stillari
```css
.solid-border { border: 2px solid #333; }        /* Uzluksiz */
.dashed-border { border: 2px dashed #333; }      /* Chiziqcha */
.dotted-border { border: 2px dotted #333; }      /* Nuqtacha */
.double-border { border: 4px double #333; }      /* Ikki qatorli */
.groove-border { border: 4px groove #333; }      /* Chuqur */
.ridge-border { border: 4px ridge #333; }        /* Baland */
```

#### 3. Har bir tomon uchun alohida
```css
.box {
    border-top: 2px solid red;       /* Yuqori */
    border-right: 3px dashed blue;   /* O'ng */
    border-bottom: 1px dotted green; /* Pastki */
    border-left: 4px double purple;  /* Chap */
}
```

#### 4. Border-radius - yumaloq burchaklar
```css
.rounded {
    border-radius: 10px;             /* Barcha burchaklar */
}

.custom-rounded {
    border-radius: 10px 5px 20px 15px; /* Har bir burchak alohida */
}

.circle {
    border-radius: 50%;              /* To'liq dumaloq */
}
```

### Margin - tashqi bo'shliq

#### 1. Asosiy margin foydalanish
```css
.box {
    margin: 20px;                    /* Barcha tomonlarda 20px */
}
```

#### 2. Har bir tomon uchun alohida
```css
.box {
    margin-top: 10px;
    margin-right: 15px;
    margin-bottom: 20px;
    margin-left: 25px;
}
```

#### 3. Markazga joylashtirish
```css
.center-box {
    width: 300px;
    margin: 0 auto;                  /* Gorizontal markazlash */
}
```

#### 4. Salbiy margin
```css
.overlap-box {
    margin-top: -10px;               /* Yuqoriga tortish */
    margin-left: -5px;               /* Chapga tortish */
}
```

### Box-sizing xususiyati

#### 1. Content-box (standart)
```css
.content-box {
    box-sizing: content-box;         /* Standart model */
    width: 300px;
    padding: 20px;
    border: 5px solid #333;
    /* Jami kenglik: 300 + 20×2 + 5×2 = 350px */
}
```

#### 2. Border-box (qulay)
```css
.border-box {
    box-sizing: border-box;          /* Qulay model */
    width: 300px;
    padding: 20px;
    border: 5px solid #333;
    /* Jami kenglik: 300px (padding va border ichida) */
}
```

#### 3. Barcha elementlar uchun border-box
```css
* {
    box-sizing: border-box;
}
```

### Amaliy misollar

#### 1. Kartochka dizayni
```html
<style>
.card {
    width: 300px;
    margin: 20px auto;
    padding: 20px;
    border: 1px solid #ddd;
    border-radius: 12px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    background-color: white;
    box-sizing: border-box;
}

.card-header {
    margin: -20px -20px 15px -20px;
    padding: 15px 20px;
    background-color: #f8f9fa;
    border-bottom: 1px solid #dee2e6;
    border-radius: 12px 12px 0 0;
}

.card-title {
    margin: 0;
    font-size: 18px;
    color: #333;
}

.card-content {
    margin-bottom: 15px;
    line-height: 1.6;
    color: #666;
}

.card-button {
    display: inline-block;
    padding: 10px 20px;
    background-color: #007bff;
    color: white;
    text-decoration: none;
    border-radius: 5px;
    border: none;
    cursor: pointer;
    transition: background-color 0.3s ease;
}

.card-button:hover {
    background-color: #0056b3;
}
</style>

<div class="card">
    <div class="card-header">
        <h3 class="card-title">Kartochka sarlavhasi</h3>
    </div>
    <div class="card-content">
        Bu kartochka Box Model xususiyatlarini ko'rsatish uchun yaratilgan. 
        Bu yerda margin, padding va border qanday ishlashini ko'rishingiz mumkin.
    </div>
    <button class="card-button">Tugma</button>
</div>
```

#### 2. Box Model vizual ko'rsatkich
```html
<style>
.box-demo {
    width: 200px;
    height: 100px;
    margin: 30px auto;
    padding: 20px;
    border: 5px solid #e74c3c;
    background-color: #3498db;
    position: relative;
    text-align: center;
    color: white;
    font-weight: bold;
}

.box-demo::before {
    content: 'MARGIN';
    position: absolute;
    top: -25px;
    left: -25px;
    right: -25px;
    bottom: -25px;
    border: 2px dashed #95a5a6;
    background-color: rgba(149, 165, 166, 0.1);
    z-index: -1;
    display: flex;
    align-items: flex-start;
    justify-content: flex-start;
    padding: 5px;
    font-size: 12px;
    color: #95a5a6;
}

.box-demo::after {
    content: 'BORDER';
    position: absolute;
    top: -3px;
    left: -3px;
    right: -3px;
    bottom: -3px;
    border: 1px dashed #c0392b;
    z-index: -1;
}

.content-label {
    background-color: rgba(0,0,0,0.3);
    padding: 5px;
    border-radius: 3px;
    font-size: 12px;
}

.padding-label {
    position: absolute;
    top: 5px;
    right: 5px;
    font-size: 10px;
    background-color: rgba(255,255,255,0.2);
    padding: 2px 5px;
    border-radius: 2px;
}
</style>

<div class="box-demo">
    <div class="content-label">CONTENT</div>
    <div class="padding-label">PADDING</div>
</div>
```

#### 3. Turli xil bo'shliqlar namunasi
```html
<style>
.spacing-demo {
    max-width: 800px;
    margin: 20px auto;
    padding: 20px;
    background-color: #f8f9fa;
    border-radius: 10px;
}

.demo-box {
    background-color: #007bff;
    color: white;
    text-align: center;
    padding: 15px;
    margin-bottom: 20px;
    border-radius: 5px;
}

.no-spacing {
    margin: 0;
    padding: 5px;
}

.small-spacing {
    margin: 10px 0;
    padding: 10px;
}

.medium-spacing {
    margin: 20px 0;
    padding: 20px;
}

.large-spacing {
    margin: 40px 0;
    padding: 30px;
}

.custom-spacing {
    margin: 10px 30px 20px 10px;
    padding: 5px 15px 10px 20px;
    background-color: #28a745;
}
</style>

<div class="spacing-demo">
    <h3>Turli xil bo'shliqlar</h3>
    
    <div class="demo-box no-spacing">
        Minimal bo'shliq (margin: 0, padding: 5px)
    </div>
    
    <div class="demo-box small-spacing">
        Kichik bo'shliq (margin: 10px 0, padding: 10px)
    </div>
    
    <div class="demo-box medium-spacing">
        O'rta bo'shliq (margin: 20px 0, padding: 20px)
    </div>
    
    <div class="demo-box large-spacing">
        Katta bo'shliq (margin: 40px 0, padding: 30px)
    </div>
    
    <div class="demo-box custom-spacing">
        Maxsus bo'shliq (har xil margin va padding)
    </div>
</div>
```

</details>

<details>
    <summary>Elementlar orasidagi masofalar</summary>

## 5.4 Elementlar Orasidagi Masofalar

### Masofalarni boshqarish usullari

#### 1. Margin bilan masofa yaratish
```css
.spaced-elements p {
    margin-bottom: 20px;             /* Pastki masofa */
}

.spaced-elements h2 {
    margin-top: 30px;                /* Yuqori masofa */
    margin-bottom: 15px;             /* Pastki masofa */
}
```

#### 2. Gap xususiyati (Flexbox va Grid)
```css
.flex-container {
    display: flex;
    gap: 20px;                       /* Elementlar orasida 20px */
}

.grid-container {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 15px;                       /* Katakchalar orasida 15px */
}
```

#### 3. Space-between va Space-around (Flexbox)
```css
.space-between {
    display: flex;
    justify-content: space-between;  /* Elementlar orasida teng masofa */
}

.space-around {
    display: flex;
    justify-content: space-around;   /* Elementlar atrofida teng masofa */
}

.space-evenly {
    display: flex;
    justify-content: space-evenly;   /* Hammasi teng masofada */
}
```

### Vertikal masofalar

#### 1. Line-height bilan
```css
.text-spacing {
    line-height: 1.8;                /* Qatorlar orasidagi masofa */
}
```

#### 2. Margin collapse (birlashish)
```css
.first-element {
    margin-bottom: 20px;
}

.second-element {
    margin-top: 30px;
    /* Natija: elementlar orasida 30px (kattaroq qiymat) */
}
```

#### 3. Margin collapse oldini olish
```css
.no-collapse {
    padding-top: 1px;                /* Padding collapse qilmaydi */
}

.with-border {
    border-top: 1px solid transparent; /* Border ham collapse qilmaydi */
}
```

### Gorizontal masofalar

#### 1. Inline elementlar uchun
```css
.inline-spacing {
    word-spacing: 10px;              /* So'zlar orasidagi masofa */
    letter-spacing: 2px;             /* Harflar orasidagi masofa */
}
```

#### 2. Inline-block elementlar
```css
.inline-block-spacing {
    display: inline-block;
    margin-right: 15px;              /* O'ng tomonda masofa */
}

.inline-block-spacing:last-child {
    margin-right: 0;                 /* Oxirgi elementda margin yo'q */
}
```

### Amaliy misollar

#### 1. Maqola matn bo'shliqlari
```html
<style>
.article-spacing {
    max-width: 700px;
    margin: 0 auto;
    padding: 30px;
    line-height: 1.6;
}

.article-spacing h1 {
    margin: 0 0 25px 0;
    font-size: 2.5em;
    color: #2c3e50;
}

.article-spacing h2 {
    margin: 35px 0 20px 0;
    font-size: 1.8em;
    color: #34495e;
    border-bottom: 2px solid #3498db;
    padding-bottom: 10px;
}

.article-spacing h3 {
    margin: 25px 0 15px 0;
    font-size: 1.3em;
    color: #2c3e50;
}

.article-spacing p {
    margin-bottom: 20px;
    text-align: justify;
    color: #444;
}

.article-spacing ul, 
.article-spacing ol {
    margin: 20px 0 20px 30px;
}

.article-spacing li {
    margin-bottom: 8px;
}

.article-spacing blockquote {
    margin: 30px 0;
    padding: 20px 30px;
    background-color: #f8f9fa;
    border-left: 4px solid #3498db;
    font-style: italic;
}

.article-spacing .highlight {
    margin: 25px 0;
    padding: 20px;
    background-color: #fff3cd;
    border: 1px solid #ffeaa7;
    border-radius: 5px;
}
</style>

<article class="article-spacing">
    <h1>Maqola Sarlavhasi</h1>
    
    <p>Bu maqolaning kirish qismi. Bu yerda asosiy mavzu haqida qisqacha ma'lumot beriladi.</p>
    
    <h2>Birinchi Bo'lim</h2>
    
    <p>Bu birinchi bo'limning mazmuni. Bu yerda mavzu batafsil yoritiladi.</p>
    
    <h3>Kichik sarlavha</h3>
    
    <p>Kichik bo'lim mazmuni bu yerda yoziladi.</p>
    
    <ul>
        <li>Birinchi nuqta</li>
        <li>Ikkinchi nuqta</li>
        <li>Uchinchi nuqta</li>
    </ul>
    
    <blockquote>
        Bu muhim iqtibos yoki ta'kidlanishi kerak bo'lgan matn.
    </blockquote>
    
    <div class="highlight">
        Bu muhim ma'lumot yoki ogohlantirish matni.
    </div>
    
    <h2>Ikkinchi Bo'lim</h2>
    
    <p>Ikkinchi bo'lim mazmuni bu yerda davom etadi.</p>
</article>
```

#### 2. Kartochkalar gallereyasi
```html
<style>
.cards-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 25px;
    padding: 30px;
    max-width: 1200px;
    margin: 0 auto;
}

.spacing-card {
    background-color: white;
    border-radius: 12px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    padding: 0;
    overflow: hidden;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.spacing-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 25px rgba(0,0,0,0.15);
}

.card-image {
    width: 100%;
    height: 180px;
    background: linear-gradient(135deg, #667eea, #764ba2);
    margin-bottom: 0;
}

.card-content {
    padding: 20px;
}

.card-title {
    margin: 0 0 12px 0;
    font-size: 1.4em;
    color: #2c3e50;
}

.card-text {
    margin: 0 0 20px 0;
    color: #666;
    line-height: 1.5;
}

.card-meta {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 15px;
    padding-top: 15px;
    border-top: 1px solid #eee;
}

.card-date {
    font-size: 0.9em;
    color: #999;
}

.card-button {
    padding: 8px 16px;
    background-color: #3498db;
    color: white;
    text-decoration: none;
    border-radius: 20px;
    font-size: 0.9em;
    transition: background-color 0.3s ease;
}

.card-button:hover {
    background-color: #2980b9;
}
</style>

<div class="cards-grid">
    <div class="spacing-card">
        <div class="card-image"></div>
        <div class="card-content">
            <h3 class="card-title">Birinchi Kartochka</h3>
            <p class="card-text">Bu kartochka mazmuni. Bu yerda qisqacha ma'lumot beriladi.</p>
            <div class="card-meta">
                <span class="card-date">2024-01-15</span>
                <a href="#" class="card-button">Batafsil</a>
            </div>
        </div>
    </div>
    
    <div class="spacing-card">
        <div class="card-image"></div>
        <div class="card-content">
            <h3 class="card-title">Ikkinchi Kartochka</h3>
            <p class="card-text">Ikkinchi kartochka mazmuni va qo'shimcha ma'lumotlar.</p>
            <div class="card-meta">
                <span class="card-date">2024-01-16</span>
                <a href="#" class="card-button">Batafsil</a>
            </div>
        </div>
    </div>
    
    <div class="spacing-card">
        <div class="card-image"></div>
        <div class="card-content">
            <h3 class="card-title">Uchinchi Kartochka</h3>
            <p class="card-text">Uchinchi kartochka uchun mazmun va tavsiflar.</p>
            <div class="card-meta">
                <span class="card-date">2024-01-17</span>
                <a href="#" class="card-button">Batafsil</a>
            </div>
        </div>
    </div>
</div>
```

#### 3. Navigatsiya menu masofalar
```html
<style>
.spacing-nav {
    background-color: #2c3e50;
    padding: 15px 0;
}

.nav-container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

.nav-list {
    display: flex;
    list-style: none;
    margin: 0;
    padding: 0;
    gap: 0;
}

.nav-item {
    margin-right: 40px;              /* Elementlar orasidagi masofa */
}

.nav-item:last-child {
    margin-right: 0;                 /* Oxirgi elementda margin yo'q */
}

.nav-link {
    color: white;
    text-decoration: none;
    padding: 10px 15px;              /* Ichki bo'shliq */
    border-radius: 5px;
    transition: background-color 0.3s ease;
    display: block;
}

.nav-link:hover {
    background-color: #34495e;
}

.nav-link.active {
    background-color: #3498db;
}

/* Mobil uchun */
@media (max-width: 768px) {
    .nav-list {
        flex-direction: column;
        gap: 10px;
    }
    
    .nav-item {
        margin-right: 0;
        margin-bottom: 0;
    }
    
    .nav-link {
        padding: 15px;
        text-align: center;
    }
}
</style>

<nav class="spacing-nav">
    <div class="nav-container">
        <ul class="nav-list">
            <li class="nav-item">
                <a href="#" class="nav-link active">Bosh sahifa</a>
            </li>
            <li class="nav-item">
                <a href="#" class="nav-link">Xizmatlar</a>
            </li>
            <li class="nav-item">
                <a href="#" class="nav-link">Portfolio</a>
            </li>
            <li class="nav-item">
                <a href="#" class="nav-link">Blog</a>
            </li>
            <li class="nav-item">
                <a href="#" class="nav-link">Aloqa</a>
            </li>
        </ul>
    </div>
</nav>
```

</details>

<details>
    <summary>Chegaralar va fon ranglari</summary>

## 5.5 Chegaralar va Fon Ranglari

### Border xususiyatlari

#### 1. Asosiy border stillari
```css
.solid-border { border: 2px solid #333; }        /* Uzluksiz */
.dashed-border { border: 2px dashed #007bff; }   /* Chiziqcha */
.dotted-border { border: 2px dotted #28a745; }   /* Nuqtacha */
.double-border { border: 4px double #dc3545; }   /* Ikki qatorli */
.groove-border { border: 5px groove #6c757d; }   /* Chuqur */
.ridge-border { border: 5px ridge #fd7e14; }     /* Baland */
.inset-border { border: 4px inset #20c997; }     /* Ichkariga */
.outset-border { border: 4px outset #e83e8c; }   /* Tashqariga */
```

#### 2. Har xil tomon chegaralari
```css
.custom-borders {
    border-top: 3px solid #e74c3c;       /* Yuqori: qizil uzluksiz */
    border-right: 2px dashed #f39c12;    /* O'ng: sariq chiziqcha */
    border-bottom: 4px double #2ecc71;   /* Pastki: yashil ikki qatorli */
    border-left: 5px dotted #9b59b6;     /* Chap: binafsha nuqtacha */
}
```

#### 3. Border-radius bilan yumaloq qilish
```css
.rounded-borders {
    border: 2px solid #3498db;
    border-radius: 10px;                  /* Barcha burchaklar */
}

.custom-radius {
    border: 2px solid #e74c3c;
    border-radius: 20px 5px 15px 10px;   /* Har bir burchak alohida */
}

.circle {
    width: 100px;
    height: 100px;
    border: 3px solid #f39c12;
    border-radius: 50%;                   /* To'liq dumaloq */
}

.pill {
    border: 2px solid #2ecc71;
    border-radius: 25px;                  /* Tabletka shakli */
}
```

### Background (fon) xususiyatlari

#### 1. Fon ranglari
```css
.bg-colors {
    background-color: #3498db;            /* Oddiy rang */
    background-color: rgba(52, 152, 219, 0.5); /* Shaffof rang */
    background-color: transparent;        /* Shaffof */
}
```

#### 2. Gradient fon ranglari
```css
.linear-gradient {
    background: linear-gradient(to right, #3498db, #2ecc71);
}

.diagonal-gradient {
    background: linear-gradient(45deg, #e74c3c, #f39c12);
}

.multi-gradient {
    background: linear-gradient(135deg, 
        #667eea 0%, 
        #764ba2 50%, 
        #667eea 100%);
}

.radial-gradient {
    background: radial-gradient(circle, #3498db, #2c3e50);
}
```

#### 3. Fon rasmlari
```css
.bg-image {
    background-image: url('image.jpg');
    background-size: cover;               /* To'liq qoplash */
    background-position: center;          /* Markazga joylashtirish */
    background-repeat: no-repeat;         /* Takrorlamaslik */
}

.bg-pattern {
    background-image: url('pattern.png');
    background-repeat: repeat;            /* Takrorlash */
    background-size: 50px 50px;          /* O'lcham */
}
```

### Box-shadow - soya effektlari

#### 1. Asosiy soya
```css
.simple-shadow {
    box-shadow: 5px 5px 10px rgba(0,0,0,0.3);
    /* x-offset y-offset blur-radius color */
}

.soft-shadow {
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
}

.deep-shadow {
    box-shadow: 0 10px 30px rgba(0,0,0,0.3);
}
```

#### 2. Ko'p qatorli soya
```css
.multiple-shadows {
    box-shadow: 
        0 1px 3px rgba(0,0,0,0.12),
        0 1px 2px rgba(0,0,0,0.24),
        inset 0 1px 0 rgba(255,255,255,0.1);
}
```

#### 3. Rangli soyalar
```css
.colored-shadows {
    box-shadow: 0 5px 15px rgba(52, 152, 219, 0.4);
}

.neon-effect {
    box-shadow: 
        0 0 5px #00ff00,
        0 0 10px #00ff00,
        0 0 15px #00ff00;
}
```

### Amaliy misollar

#### 1. Kartochka dizayni - turli chegaralar
```html
<style>
.border-showcase {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
    padding: 30px;
    background-color: #f8f9fa;
}

.border-card {
    padding: 20px;
    background-color: white;
    text-align: center;
    min-height: 120px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: bold;
    color: #2c3e50;
}

.card-1 {
    border: 3px solid #e74c3c;
    border-radius: 0;
}

.card-2 {
    border: 3px dashed #f39c12;
    border-radius: 10px;
}

.card-3 {
    border: 3px dotted #2ecc71;
    border-radius: 50%;
}

.card-4 {
    border: 4px double #9b59b6;
    border-radius: 15px;
}

.card-5 {
    border-top: 4px solid #e74c3c;
    border-radius: 5px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
}

.card-6 {
    border: none;
    border-left: 5px solid #3498db;
    background: linear-gradient(135deg, #667eea, #764ba2);
    color: white;
}
</style>

<div class="border-showcase">
    <div class="border-card card-1">Solid Border</div>
    <div class="border-card card-2">Dashed Border</div>
    <div class="border-card card-3">Dotted Circle</div>
    <div class="border-card card-4">Double Border</div>
    <div class="border-card card-5">Top Border + Shadow</div>
    <div class="border-card card-6">Left Border + Gradient</div>
</div>
```

#### 2. Fon ranglari namunasi
```html
<style>
.background-demo {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
    padding: 30px;
}

.bg-sample {
    height: 150px;
    padding: 20px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: bold;
    color: white;
    text-align: center;
    border-radius: 10px;
    text-shadow: 1px 1px 2px rgba(0,0,0,0.5);
}

.bg-solid {
    background-color: #3498db;
}

.bg-linear {
    background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
}

.bg-radial {
    background: radial-gradient(circle, #ffecd2, #fcb69f);
    color: #333;
    text-shadow: none;
}

.bg-multiple {
    background: 
        linear-gradient(135deg, rgba(255,255,255,0.1) 0%, transparent 50%),
        linear-gradient(45deg, #667eea, #764ba2);
}

.bg-transparent {
    background-color: rgba(52, 152, 219, 0.7);
    border: 2px solid #3498db;
}

.bg-pattern {
    background: 
        radial-gradient(circle at 20% 80%, rgba(120,119,198,0.3) 0%, transparent 50%),
        radial-gradient(circle at 80% 20%, rgba(255,119,198,0.3) 0%, transparent 50%),
        radial-gradient(circle at 40% 40%, rgba(120,200,255,0.3) 0%, transparent 50%),
        linear-gradient(135deg, #667eea, #764ba2);
}
</style>

<div class="background-demo">
    <div class="bg-sample bg-solid">Oddiy Fon Rangi</div>
    <div class="bg-sample bg-linear">Linear Gradient</div>
    <div class="bg-sample bg-radial">Radial Gradient</div>
    <div class="bg-sample bg-multiple">Ko'p Qatorli Fon</div>
    <div class="bg-sample bg-transparent">Shaffof Fon</div>
    <div class="bg-sample bg-pattern">Murakkab Pattern</div>
</div>
```

#### 3. Soya effektlari namunasi
```html
<style>
.shadow-demo {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 30px;
    padding: 50px 30px;
    background: linear-gradient(135deg, #f5f7fa, #c3cfe2);
}

.shadow-card {
    height: 120px;
    background-color: white;
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: bold;
    color: #2c3e50;
    text-align: center;
}

.shadow-1 {
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.shadow-2 {
    box-shadow: 0 4px 8px rgba(0,0,0,0.15);
}

.shadow-3 {
    box-shadow: 0 8px 16px rgba(0,0,0,0.2);
}

.shadow-4 {
    box-shadow: 0 12px 24px rgba(0,0,0,0.25);
}

.shadow-colored {
    box-shadow: 0 8px 16px rgba(52, 152, 219, 0.3);
}

.shadow-multiple {
    box-shadow: 
        0 1px 3px rgba(0,0,0,0.12),
        0 1px 2px rgba(0,0,0,0.24);
}

.shadow-inset {
    box-shadow: inset 0 2px 4px rgba(0,0,0,0.1);
}

.shadow-neon {
    background-color: #2c3e50;
    color: #00ff00;
    box-shadow: 
        0 0 5px #00ff00,
        0 0 10px #00ff00,
        0 0 15px #00ff00;
}
</style>

<div class="shadow-demo">
    <div class="shadow-card shadow-1">Engil Soya</div>
    <div class="shadow-card shadow-2">O'rta Soya</div>
    <div class="shadow-card shadow-3">Chuqur Soya</div>
    <div class="shadow-card shadow-4">Juda Chuqur</div>
    <div class="shadow-card shadow-colored">Rangli Soya</div>
    <div class="shadow-card shadow-multiple">Ko'p Qatorli</div>
    <div class="shadow-card shadow-inset">Ichki Soya</div>
    <div class="shadow-card shadow-neon">Neon Effekt</div>
</div>
```

</details>
