<details>
    <summary>Bootstrap nima va nima uchun kerak?</summary>

## 9.1 Bootstrap Nima va Nima Uchun Kerak?

### Bootstrap nima?

**Bootstrap** - eng mashhur CSS framework bo'lib, tez va oson web-sayt yaratish uchun tayyor CSS va JavaScript komponentlari to'plami.

### Bootstrap nima uchun kerak?

#### 1. Tez rivojlantirish
- Tayyor komponentlar
- Kamroq kod yozish
- Tez prototip yaratish

#### 2. Responsive dizayn
- Avtomatik responsive
- Grid sistem
- Mobile-first yondashuv

#### 3. Konsistent dizayn
- Bir xil ko'rinish
- Professional dizayn
- Zamonaviy standartlar

#### 4. Brauzerlar mosligi
- Barcha brauzerlarda ishlaydi
- Cross-browser compatibility
- Muammosiz ishlash

### Bootstrap afzalliklari

#### 1. Oson foydalanish
```html
<!-- Oddiy tugma -->
<button class="btn btn-primary">Bosish</button>

<!-- Oddiy kartochka -->
<div class="card">
    <div class="card-body">
        <h5 class="card-title">Sarlavha</h5>
        <p class="card-text">Matn mazmuni</p>
    </div>
</div>
```

#### 2. Responsive grid
```html
<!-- 3 ustunli layout -->
<div class="row">
    <div class="col-md-4">Ustun 1</div>
    <div class="col-md-4">Ustun 2</div>
    <div class="col-md-4">Ustun 3</div>
</div>
```

#### 3. Tayyor stillar
```html
<!-- Ranglar -->
<button class="btn btn-primary">Primary</button>
<button class="btn btn-success">Success</button>
<button class="btn btn-danger">Danger</button>
```

### Bootstrap vs oddiy CSS

#### Oddiy CSS:
```css
/* Ko'p kod kerak */
.custom-button {
    background-color: #007bff;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 16px;
}

.custom-button:hover {
    background-color: #0056b3;
}
```

#### Bootstrap:
```html
<!-- Faqat class nomi -->
<button class="btn btn-primary">Tugma</button>
```

### Amaliy misollar

#### 1. Bootstrap taqqoslash
```html
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bootstrap Taqqoslash</title>
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
    <div class="container mt-5">
        <h1 class="text-center mb-4">Bootstrap vs Oddiy CSS</h1>
        
        <div class="row">
            <div class="col-md-6">
                <div class="card">
                    <div class="card-header bg-primary text-white">
                        <h5>Bootstrap Tugmalar</h5>
                    </div>
                    <div class="card-body">
                        <button class="btn btn-primary me-2">Primary</button>
                        <button class="btn btn-success me-2">Success</button>
                        <button class="btn btn-warning me-2">Warning</button>
                        <button class="btn btn-danger">Danger</button>
                    </div>
                </div>
            </div>
            
            <div class="col-md-6">
                <div class="card">
                    <div class="card-header bg-secondary text-white">
                        <h5>Oddiy CSS Tugmalar</h5>
                    </div>
                    <div class="card-body">
                        <button style="background-color: #007bff; color: white; padding: 8px 16px; border: none; border-radius: 4px; margin-right: 8px;">Primary</button>
                        <button style="background-color: #28a745; color: white; padding: 8px 16px; border: none; border-radius: 4px; margin-right: 8px;">Success</button>
                        <button style="background-color: #ffc107; color: black; padding: 8px 16px; border: none; border-radius: 4px; margin-right: 8px;">Warning</button>
                        <button style="background-color: #dc3545; color: white; padding: 8px 16px; border: none; border-radius: 4px;">Danger</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
```

#### 2. Bootstrap komponentlar namunasi
```html
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bootstrap Komponentlar</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
    <div class="container mt-4">
        <h1 class="text-center text-primary mb-4">Bootstrap Komponentlar</h1>
        
        <!-- Kartochkalar -->
        <div class="row mb-4">
            <div class="col-md-4">
                <div class="card">
                    <img src="https://via.placeholder.com/300x200/007bff/white?text=Kartochka+1" class="card-img-top" alt="Kartochka 1">
                    <div class="card-body">
                        <h5 class="card-title">Birinchi Kartochka</h5>
                        <p class="card-text">Bu Bootstrap kartochka komponenti misoli.</p>
                        <a href="#" class="btn btn-primary">Batafsil</a>
                    </div>
                </div>
            </div>
            
            <div class="col-md-4">
                <div class="card">
                    <img src="https://via.placeholder.com/300x200/28a745/white?text=Kartochka+2" class="card-img-top" alt="Kartochka 2">
                    <div class="card-body">
                        <h5 class="card-title">Ikkinchi Kartochka</h5>
                        <p class="card-text">Bootstrap yordamida tez va oson yaratilgan.</p>
                        <a href="#" class="btn btn-success">Batafsil</a>
                    </div>
                </div>
            </div>
            
            <div class="col-md-4">
                <div class="card">
                    <img src="https://via.placeholder.com/300x200/dc3545/white?text=Kartochka+3" class="card-img-top" alt="Kartochka 3">
                    <div class="card-body">
                        <h5 class="card-title">Uchinchi Kartochka</h5>
                        <p class="card-text">Professional ko'rinish va responsive dizayn.</p>
                        <a href="#" class="btn btn-danger">Batafsil</a>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Alert xabarlar -->
        <div class="row mb-4">
            <div class="col-12">
                <div class="alert alert-success" role="alert">
                    <strong>Muvaffaqiyat!</strong> Bootstrap muvaffaqiyatli o'rnatildi.
                </div>
                <div class="alert alert-warning" role="alert">
                    <strong>Ogohlantirish!</strong> Bootstrap versiyasini tekshiring.
                </div>
                <div class="alert alert-danger" role="alert">
                    <strong>Xato!</strong> CSS fayl topilmadi.
                </div>
            </div>
        </div>
        
        <!-- Tugmalar guruhi -->
        <div class="row">
            <div class="col-12">
                <h3 class="mb-3">Tugmalar Guruhi</h3>
                <div class="btn-group" role="group">
                    <button type="button" class="btn btn-outline-primary">Birinchi</button>
                    <button type="button" class="btn btn-outline-primary">Ikkinchi</button>
                    <button type="button" class="btn btn-outline-primary">Uchinchi</button>
                </div>
                
                <div class="btn-toolbar mt-3" role="toolbar">
                    <div class="btn-group me-2" role="group">
                        <button type="button" class="btn btn-secondary">1</button>
                        <button type="button" class="btn btn-secondary">2</button>
                        <button type="button" class="btn btn-secondary">3</button>
                    </div>
                    <div class="btn-group" role="group">
                        <button type="button" class="btn btn-secondary">4</button>
                        <button type="button" class="btn btn-secondary">5</button>
                        <button type="button" class="btn btn-secondary">6</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
```

</details>

<details>
    <summary>Bootstrap o'rnatish va ulash</summary>

## 9.2 Bootstrap O'rnatish va Ulash

### Bootstrap versiyalari

#### Hozirgi versiya: Bootstrap 5.3
- Eng yangi xususiyatlar
- Yaxshilangan performance
- Zamonaviy CSS Grid
- JavaScript ES6+

### Bootstrap o'rnatish usullari

#### 1. CDN orqali (Tavsiya etiladi)
```html
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bootstrap CDN</title>
    
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    
    <!-- Bootstrap JavaScript (ixtiyoriy) -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</head>
<body>
    <!-- Sahifa mazmuni -->
</body>
</html>
```

#### 2. Lokal fayl orqali
```html
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bootstrap Lokal</title>
    
    <!-- Lokal Bootstrap CSS -->
    <link href="css/bootstrap.min.css" rel="stylesheet">
    
    <!-- Lokal Bootstrap JavaScript -->
    <script src="js/bootstrap.bundle.min.js"></script>
</head>
<body>
    <!-- Sahifa mazmuni -->
</body>
</html>
```

### Bootstrap fayllarini yuklab olish

#### 1. Rasmiy sayt orqali
- [getbootstrap.com](https://getbootstrap.com/)
- "Download" tugmasini bosish
- "Compiled CSS and JS" ni tanlash

#### 2. NPM orqali (developer uchun)
```bash
npm install bootstrap@5.3.0
```

### Bootstrap strukturasi

#### Fayl tuzilishi:
```
bootstrap/
├── css/
│   ├── bootstrap.min.css      # Minified CSS
│   └── bootstrap.css          # Development CSS
├── js/
│   ├── bootstrap.bundle.min.js # Minified JS (Popper bilan)
│   └── bootstrap.min.js       # Minified JS
└── scss/                      # Source files
```

### Bootstrap konteyner turlari

#### 1. Container
```html
<div class="container">
    <!-- Fixed width, responsive -->
</div>
```

#### 2. Container-fluid
```html
<div class="container-fluid">
    <!-- Full width -->
</div>
```

#### 3. Container-sm, md, lg, xl, xxl
```html
<div class="container-sm">   <!-- Small screens and up -->
<div class="container-md">   <!-- Medium screens and up -->
<div class="container-lg">   <!-- Large screens and up -->
<div class="container-xl">   <!-- Extra large screens and up -->
<div class="container-xxl">  <!-- Extra extra large screens and up -->
```

### Amaliy misollar

#### 1. Bootstrap asosiy sahifa
```html
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bootstrap Asosiy Sahifa</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</head>
<body>
    <!-- Header -->
    <header class="bg-primary text-white py-4">
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <h1 class="text-center mb-0">Bootstrap Sahifa</h1>
                    <p class="text-center mb-0">Bootstrap 5.3.0 bilan yaratilgan</p>
                </div>
            </div>
        </div>
    </header>
    
    <!-- Main Content -->
    <main class="py-5">
        <div class="container">
            <div class="row">
                <div class="col-lg-8">
                    <h2>Asosiy Mazmun</h2>
                    <p class="lead">Bu sahifa Bootstrap 5.3.0 versiyasi bilan yaratilgan.</p>
                    
                    <div class="card mb-4">
                        <div class="card-header">
                            <h5 class="card-title mb-0">Bootstrap Afzalliklari</h5>
                        </div>
                        <div class="card-body">
                            <ul class="list-group list-group-flush">
                                <li class="list-group-item">Tez rivojlantirish</li>
                                <li class="list-group-item">Responsive dizayn</li>
                                <li class="list-group-item">Tayyor komponentlar</li>
                                <li class="list-group-item">Professional ko'rinish</li>
                            </ul>
                        </div>
                    </div>
                </div>
                
                <div class="col-lg-4">
                    <div class="card">
                        <div class="card-header bg-secondary text-white">
                            <h5 class="card-title mb-0">Yon Panel</h5>
                        </div>
                        <div class="card-body">
                            <h6>Bootstrap Versiyalari:</h6>
                            <div class="list-group list-group-flush">
                                <a href="#" class="list-group-item list-group-item-action">
                                    Bootstrap 5.3.0 (Hozirgi)
                                </a>
                                <a href="#" class="list-group-item list-group-item-action">
                                    Bootstrap 5.2.3
                                </a>
                                <a href="#" class="list-group-item list-group-item-action">
                                    Bootstrap 4.6.2
                                </a>
                            </div>
                            
                            <div class="mt-3">
                                <button class="btn btn-primary w-100">Batafsil Ma'lumot</button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </main>
    
    <!-- Footer -->
    <footer class="bg-dark text-white py-4">
        <div class="container">
            <div class="row">
                <div class="col-12 text-center">
                    <p class="mb-0">&copy; 2024 Bootstrap Sahifa. Barcha huquqlar himoyalangan.</p>
                </div>
            </div>
        </div>
    </footer>
</body>
</html>
```

#### 2. Bootstrap konteyner taqqoslash
```html
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bootstrap Konteynerlar</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
    <div class="container-fluid py-4">
        <h1 class="text-center mb-4">Bootstrap Konteynerlar</h1>
        
        <div class="row">
            <div class="col-md-6 mb-4">
                <div class="card">
                    <div class="card-header bg-primary text-white">
                        <h5 class="card-title mb-0">Container</h5>
                    </div>
                    <div class="card-body">
                        <div class="container bg-light p-3">
                            <p class="mb-0">Bu container - fixed width, responsive</p>
                        </div>
                        <code class="mt-2 d-block">&lt;div class="container"&gt;</code>
                    </div>
                </div>
            </div>
            
            <div class="col-md-6 mb-4">
                <div class="card">
                    <div class="card-header bg-success text-white">
                        <h5 class="card-title mb-0">Container-fluid</h5>
                    </div>
                    <div class="card-body">
                        <div class="container-fluid bg-light p-3">
                            <p class="mb-0">Bu container-fluid - full width</p>
                        </div>
                        <code class="mt-2 d-block">&lt;div class="container-fluid"&gt;</code>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="row">
            <div class="col-12">
                <div class="card">
                    <div class="card-header bg-warning text-dark">
                        <h5 class="card-title mb-0">Responsive Konteynerlar</h5>
                    </div>
                    <div class="card-body">
                        <div class="row">
                            <div class="col-md-6 mb-3">
                                <div class="container-sm bg-info text-white p-2">
                                    <small>container-sm</small>
                                </div>
                            </div>
                            <div class="col-md-6 mb-3">
                                <div class="container-md bg-info text-white p-2">
                                    <small>container-md</small>
                                </div>
                            </div>
                            <div class="col-md-6 mb-3">
                                <div class="container-lg bg-info text-white p-2">
                                    <small>container-lg</small>
                                </div>
                            </div>
                            <div class="col-md-6 mb-3">
                                <div class="container-xl bg-info text-white p-2">
                                    <small>container-xl</small>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
```

#### 3. Bootstrap o'rnatish test
```html
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bootstrap Test</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
    <div class="container mt-5">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card">
                    <div class="card-header bg-success text-white text-center">
                        <h4 class="mb-0">✅ Bootstrap Muvaffaqiyatli O'rnatildi!</h4>
                    </div>
                    <div class="card-body text-center">
                        <div class="mb-4">
                            <i class="bi bi-check-circle-fill text-success" style="font-size: 4rem;"></i>
                        </div>
                        
                        <h5 class="card-title">Bootstrap 5.3.0</h5>
                        <p class="card-text">Bootstrap framework muvaffaqiyatli ulangan va ishlayapti.</p>
                        
                        <div class="row mt-4">
                            <div class="col-md-4">
                                <div class="p-3 bg-light rounded">
                                    <h6>CSS</h6>
                                    <span class="badge bg-success">✅ Ulangan</span>
                                </div>
                            </div>
                            <div class="col-md-4">
                                <div class="p-3 bg-light rounded">
                                    <h6>Grid</h6>
                                    <span class="badge bg-success">✅ Ishlaydi</span>
                                </div>
                            </div>
                            <div class="col-md-4">
                                <div class="p-3 bg-light rounded">
                                    <h6>Komponentlar</h6>
                                    <span class="badge bg-success">✅ Tayyor</span>
                                </div>
                            </div>
                        </div>
                        
                        <div class="mt-4">
                            <button class="btn btn-primary me-2">Bootstrap Docs</button>
                            <button class="btn btn-outline-secondary">Examples</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
```

</details>



<details>
    <summary>Grid sistem</summary>

## 9.3 Grid Sistem

### Bootstrap Grid nima?

**Bootstrap Grid** - 12 ustunli responsive grid sistem bo'lib, sahifa layout yaratish uchun ishlatiladi.

### Grid tushunchalari

#### 1. Container
- Grid sistem uchun wrapper
- Max-width va margin auto
- Responsive breakpoint'lar

#### 2. Row
- Ustunlar uchun konteyner
- Flexbox yordamida
- Negative margin bilan

#### 3. Column
- Asosiy grid elementlari
- 12 ustunli sistem
- Responsive breakpoint'lar

### Bootstrap breakpoint'lar

#### Breakpoint jadvali:
| Breakpoint | Class prefix | Width |
|------------|--------------|-------|
| X-Small    | (none)       | <576px |
| Small      | sm           | ≥576px |
| Medium     | md           | ≥768px |
| Large      | lg           | ≥992px |
| Extra Large| xl           | ≥1200px |
| XX Large   | xxl          | ≥1400px |

### Grid sintaksisi

#### 1. Asosiy sintaksis
```html
<div class="container">
    <div class="row">
        <div class="col">Ustun 1</div>
        <div class="col">Ustun 2</div>
        <div class="col">Ustun 3</div>
    </div>
</div>
```

#### 2. Ustun kengliklari
```html
<div class="container">
    <div class="row">
        <div class="col-4">4 ustun</div>
        <div class="col-8">8 ustun</div>
    </div>
</div>
```

#### 3. Responsive ustunlar
```html
<div class="container">
    <div class="row">
        <div class="col-md-6 col-lg-4">Responsive ustun</div>
        <div class="col-md-6 col-lg-8">Responsive ustun</div>
    </div>
</div>
```

### Amaliy misol - Grid demo
```html
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bootstrap Grid</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
    <div class="container mt-4">
        <h1 class="text-center mb-4">Bootstrap Grid Sistem</h1>
        
        <!-- 12 ustunli sistem -->
        <div class="row mb-3">
            <div class="col-1 bg-primary text-white text-center py-2">1</div>
            <div class="col-1 bg-primary text-white text-center py-2">2</div>
            <div class="col-1 bg-primary text-white text-center py-2">3</div>
            <div class="col-1 bg-primary text-white text-center py-2">4</div>
            <div class="col-1 bg-primary text-white text-center py-2">5</div>
            <div class="col-1 bg-primary text-white text-center py-2">6</div>
            <div class="col-1 bg-primary text-white text-center py-2">7</div>
            <div class="col-1 bg-primary text-white text-center py-2">8</div>
            <div class="col-1 bg-primary text-white text-center py-2">9</div>
            <div class="col-1 bg-primary text-white text-center py-2">10</div>
            <div class="col-1 bg-primary text-white text-center py-2">11</div>
            <div class="col-1 bg-primary text-white text-center py-2">12</div>
        </div>
        
        <!-- Teng ustunlar -->
        <div class="row mb-3">
            <div class="col-6 bg-success text-white text-center py-2">6 ustun</div>
            <div class="col-6 bg-success text-white text-center py-2">6 ustun</div>
        </div>
        
        <div class="row mb-3">
            <div class="col-4 bg-warning text-dark text-center py-2">4 ustun</div>
            <div class="col-4 bg-warning text-dark text-center py-2">4 ustun</div>
            <div class="col-4 bg-warning text-dark text-center py-2">4 ustun</div>
        </div>
        
        <!-- Responsive ustunlar -->
        <div class="row mb-3">
            <div class="col-12 col-md-6 col-lg-4 bg-info text-white text-center py-2">Responsive 1</div>
            <div class="col-12 col-md-6 col-lg-4 bg-info text-white text-center py-2">Responsive 2</div>
            <div class="col-12 col-md-12 col-lg-4 bg-info text-white text-center py-2">Responsive 3</div>
        </div>
    </div>
</body>
</html>
```

</details>

<details>
    <summary>Tayyor komponentlar (buttons, cards, navbar)</summary>

## 9.4 Tayyor Komponentlar

### Bootstrap komponentlari

Bootstrap juda ko'p tayyor komponentlar bilan keladi:

#### 1. Tugmalar (Buttons)
#### 2. Kartochkalar (Cards)
#### 3. Navigatsiya (Navbar)
#### 4. Alert xabarlar
#### 5. Form elementlari
#### 6. Modal oynalar
#### 7. Carousel
#### 8. Tab'lar

### Tugmalar (Buttons)

#### Asosiy tugmalar
```html
<!-- Asosiy tugmalar -->
<button class="btn btn-primary">Primary</button>
<button class="btn btn-secondary">Secondary</button>
<button class="btn btn-success">Success</button>
<button class="btn btn-danger">Danger</button>
<button class="btn btn-warning">Warning</button>
<button class="btn btn-info">Info</button>
<button class="btn btn-light">Light</button>
<button class="btn btn-dark">Dark</button>
```

#### Tugma o'lchamlari
```html
<!-- Tugma o'lchamlari -->
<button class="btn btn-primary btn-sm">Kichik tugma</button>
<button class="btn btn-primary">Oddiy tugma</button>
<button class="btn btn-primary btn-lg">Katta tugma</button>
```

#### Outline tugmalar
```html
<!-- Outline tugmalar -->
<button class="btn btn-outline-primary">Primary</button>
<button class="btn btn-outline-secondary">Secondary</button>
<button class="btn btn-outline-success">Success</button>
```

### Kartochkalar (Cards)

#### Oddiy kartochka
```html
<div class="card">
    <div class="card-body">
        <h5 class="card-title">Kartochka sarlavhasi</h5>
        <p class="card-text">Kartochka matni</p>
        <a href="#" class="btn btn-primary">Tugma</a>
    </div>
</div>
```

#### Rasm bilan kartochka
```html
<div class="card">
    <img src="rasm.jpg" class="card-img-top" alt="Rasm">
    <div class="card-body">
        <h5 class="card-title">Rasm bilan kartochka</h5>
        <p class="card-text">Rasm va matn bilan kartochka</p>
    </div>
</div>
```

### Navigatsiya (Navbar)

#### Asosiy navbar
```html
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container">
        <a class="navbar-brand" href="#">Mening Saytim</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav">
                <li class="nav-item">
                    <a class="nav-link" href="#">Bosh sahifa</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Xizmatlar</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Aloqa</a>
                </li>
            </ul>
        </div>
    </div>
</nav>
```

### Amaliy misol - Komponentlar demo
```html
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bootstrap Komponentlar</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</head>
<body>
    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
        <div class="container">
            <a class="navbar-brand" href="#">Bootstrap Demo</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav">
                    <li class="nav-item">
                        <a class="nav-link active" href="#">Bosh sahifa</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Komponentlar</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Grid</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <div class="container mt-4">
        <h1 class="text-center mb-4">Bootstrap Komponentlar</h1>
        
        <!-- Tugmalar -->
        <div class="row mb-4">
            <div class="col-12">
                <h3>Tugmalar</h3>
                <div class="mb-3">
                    <button class="btn btn-primary me-2">Primary</button>
                    <button class="btn btn-secondary me-2">Secondary</button>
                    <button class="btn btn-success me-2">Success</button>
                    <button class="btn btn-danger me-2">Danger</button>
                    <button class="btn btn-warning me-2">Warning</button>
                    <button class="btn btn-info me-2">Info</button>
                </div>
                
                <div class="mb-3">
                    <button class="btn btn-outline-primary me-2">Outline Primary</button>
                    <button class="btn btn-outline-secondary me-2">Outline Secondary</button>
                    <button class="btn btn-outline-success me-2">Outline Success</button>
                </div>
                
                <div class="mb-3">
                    <button class="btn btn-primary btn-sm me-2">Kichik</button>
                    <button class="btn btn-primary me-2">Oddiy</button>
                    <button class="btn btn-primary btn-lg">Katta</button>
                </div>
            </div>
        </div>
        
        <!-- Kartochkalar -->
        <div class="row mb-4">
            <div class="col-12">
                <h3>Kartochkalar</h3>
            </div>
        </div>
        
        <div class="row">
            <div class="col-md-4 mb-4">
                <div class="card">
                    <div class="card-body">
                        <h5 class="card-title">Oddiy Kartochka</h5>
                        <p class="card-text">Bu oddiy Bootstrap kartochka komponenti.</p>
                        <a href="#" class="btn btn-primary">Batafsil</a>
                    </div>
                </div>
            </div>
            
            <div class="col-md-4 mb-4">
                <div class="card">
                    <img src="https://via.placeholder.com/300x200/007bff/white?text=Kartochka+2" class="card-img-top" alt="Rasm">
                    <div class="card-body">
                        <h5 class="card-title">Rasm bilan Kartochka</h5>
                        <p class="card-text">Rasm va matn bilan kartochka.</p>
                        <a href="#" class="btn btn-success">Batafsil</a>
                    </div>
                </div>
            </div>
            
            <div class="col-md-4 mb-4">
                <div class="card">
                    <div class="card-header bg-warning text-dark">
                        <h5 class="card-title mb-0">Header bilan Kartochka</h5>
                    </div>
                    <div class="card-body">
                        <p class="card-text">Header va body bilan kartochka.</p>
                        <a href="#" class="btn btn-warning">Batafsil</a>
                    </div>
                    <div class="card-footer text-muted">
                        Footer matn
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Alert xabarlar -->
        <div class="row mb-4">
            <div class="col-12">
                <h3>Alert Xabarlar</h3>
                <div class="alert alert-success" role="alert">
                    <strong>Muvaffaqiyat!</strong> Bootstrap komponentlari muvaffaqiyatli yuklandi.
                </div>
                <div class="alert alert-warning" role="alert">
                    <strong>Ogohlantirish!</strong> Bu ogohlantirish xabari.
                </div>
                <div class="alert alert-danger" role="alert">
                    <strong>Xato!</strong> Bu xato xabari.
                </div>
            </div>
        </div>
        
        <!-- Badge'lar -->
        <div class="row">
            <div class="col-12">
                <h3>Badge'lar</h3>
                <div class="mb-3">
                    <span class="badge bg-primary">Primary</span>
                    <span class="badge bg-secondary">Secondary</span>
                    <span class="badge bg-success">Success</span>
                    <span class="badge bg-danger">Danger</span>
                    <span class="badge bg-warning text-dark">Warning</span>
                    <span class="badge bg-info">Info</span>
                </div>
                
                <div class="mb-3">
                    <h4>Kartochka sarlavhasi <span class="badge bg-secondary">Yangi</span></h4>
                    <p>Bu matn bilan badge ko'rsatiladi.</p>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
```

</details>

<details>
    <summary>Responsive utilities</summary>

## 9.5 Responsive Utilities

### Bootstrap Responsive Utilities

Bootstrap responsive utilities yordamida turli ekran o'lchamlarida turli xil ko'rinish yaratish mumkin.

### Display utilities

#### Display qiymatlari
```html
<!-- Display utilities -->
<div class="d-none">Hech qachon ko'rinmaydi</div>
<div class="d-block">Blok ko'rinishda</div>
<div class="d-inline">Inline ko'rinishda</div>
<div class="d-inline-block">Inline-block ko'rinishda</div>
<div class="d-flex">Flex ko'rinishda</div>
<div class="d-grid">Grid ko'rinishda</div>
```

#### Responsive display
```html
<!-- Responsive display -->
<div class="d-none d-md-block">Faqat md va undan katta ekranlarda ko'rinadi</div>
<div class="d-block d-md-none">Faqat md dan kichik ekranlarda ko'rinadi</div>
```

### Spacing utilities

#### Margin va padding
```html
<!-- Margin -->
<div class="m-0">Margin yo'q</div>
<div class="m-1">Kichik margin</div>
<div class="m-2">O'rta margin</div>
<div class="m-3">Katta margin</div>
<div class="m-4">Eng katta margin</div>
<div class="m-5">Juda katta margin</div>

<!-- Padding -->
<div class="p-0">Padding yo'q</div>
<div class="p-1">Kichik padding</div>
<div class="p-2">O'rta padding</div>
<div class="p-3">Katta padding</div>
<div class="p-4">Eng katta padding</div>
<div class="p-5">Juda katta padding</div>
```

#### Yo'nalish bo'yicha spacing
```html
<!-- Yo'nalish bo'yicha -->
<div class="mt-3">Top margin</div>
<div class="mb-3">Bottom margin</div>
<div class="ms-3">Start margin (chap)</div>
<div class="me-3">End margin (o'ng)</div>

<div class="pt-3">Top padding</div>
<div class="pb-3">Bottom padding</div>
<div class="ps-3">Start padding (chap)</div>
<div class="pe-3">End padding (o'ng)</div>
```

### Text utilities

#### Text alignment
```html
<!-- Text alignment -->
<p class="text-start">Chap tomondan tekislangan</p>
<p class="text-center">Markazda tekislangan</p>
<p class="text-end">O'ng tomondan tekislangan</p>

<!-- Responsive text alignment -->
<p class="text-center text-md-start">Markazda, md da chapda</p>
<p class="text-start text-lg-center">Chapda, lg da markazda</p>
```

#### Text o'lchamlari
```html
<!-- Text o'lchamlari -->
<p class="fs-1">Eng katta matn</p>
<p class="fs-2">Katta matn</p>
<p class="fs-3">O'rta matn</p>
<p class="fs-4">Kichik matn</p>
<p class="fs-5">Juda kichik matn</p>
<p class="fs-6">Eng kichik matn</p>
```

### Color utilities

#### Text ranglari
```html
<!-- Text ranglari -->
<p class="text-primary">Primary matn</p>
<p class="text-secondary">Secondary matn</p>
<p class="text-success">Success matn</p>
<p class="text-danger">Danger matn</p>
<p class="text-warning">Warning matn</p>
<p class="text-info">Info matn</p>
<p class="text-light bg-dark">Light matn</p>
<p class="text-dark">Dark matn</p>
<p class="text-muted">Muted matn</p>
```

#### Background ranglari
```html
<!-- Background ranglari -->
<div class="bg-primary text-white">Primary background</div>
<div class="bg-secondary text-white">Secondary background</div>
<div class="bg-success text-white">Success background</div>
<div class="bg-danger text-white">Danger background</div>
<div class="bg-warning text-dark">Warning background</div>
<div class="bg-info text-white">Info background</div>
<div class="bg-light text-dark">Light background</div>
<div class="bg-dark text-white">Dark background</div>
```

### Amaliy misol - Responsive utilities demo
```html
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bootstrap Responsive Utilities</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
    <div class="container mt-4">
        <h1 class="text-center mb-4">Bootstrap Responsive Utilities</h1>
        
        <!-- Display utilities -->
        <div class="row mb-4">
            <div class="col-12">
                <h3>Display Utilities</h3>
                <div class="row">
                    <div class="col-6 col-md-3 mb-2">
                        <div class="bg-primary text-white p-2 text-center">Ko'rinadi</div>
                    </div>
                    <div class="col-6 col-md-3 mb-2">
                        <div class="d-none d-md-block bg-success text-white p-2 text-center">Faqat MD+</div>
                    </div>
                    <div class="col-6 col-md-3 mb-2">
                        <div class="d-block d-md-none bg-warning text-dark p-2 text-center">Faqat MD-</div>
                    </div>
                    <div class="col-6 col-md-3 mb-2">
                        <div class="d-none d-lg-block bg-info text-white p-2 text-center">Faqat LG+</div>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Spacing utilities -->
        <div class="row mb-4">
            <div class="col-12">
                <h3>Spacing Utilities</h3>
                <div class="row">
                    <div class="col-md-6">
                        <h5>Margin</h5>
                        <div class="m-1 bg-light p-2">m-1 (kichik margin)</div>
                        <div class="m-2 bg-light p-2">m-2 (o'rta margin)</div>
                        <div class="m-3 bg-light p-2">m-3 (katta margin)</div>
                        <div class="m-4 bg-light p-2">m-4 (eng katta margin)</div>
                    </div>
                    <div class="col-md-6">
                        <h5>Padding</h5>
                        <div class="bg-primary text-white">
                            <div class="p-1">p-1 (kichik padding)</div>
                            <div class="p-2">p-2 (o'rta padding)</div>
                            <div class="p-3">p-3 (katta padding)</div>
                            <div class="p-4">p-4 (eng katta padding)</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Text utilities -->
        <div class="row mb-4">
            <div class="col-12">
                <h3>Text Utilities</h3>
                <div class="row">
                    <div class="col-md-6">
                        <h5>Text Alignment</h5>
                        <p class="text-start bg-light p-2">text-start (chapda)</p>
                        <p class="text-center bg-light p-2">text-center (markazda)</p>
                        <p class="text-end bg-light p-2">text-end (o'ngda)</p>
                        <p class="text-center text-md-start bg-light p-2">Responsive alignment</p>
                    </div>
                    <div class="col-md-6">
                        <h5>Text Sizes</h5>
                        <p class="fs-1">fs-1 (eng katta)</p>
                        <p class="fs-3">fs-3 (katta)</p>
                        <p class="fs-4">fs-4 (o'rta)</p>
                        <p class="fs-6">fs-6 (kichik)</p>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Color utilities -->
        <div class="row mb-4">
            <div class="col-12">
                <h3>Color Utilities</h3>
                <div class="row">
                    <div class="col-md-6">
                        <h5>Text Colors</h5>
                        <p class="text-primary">text-primary</p>
                        <p class="text-success">text-success</p>
                        <p class="text-warning">text-warning</p>
                        <p class="text-danger">text-danger</p>
                        <p class="text-info">text-info</p>
                        <p class="text-muted">text-muted</p>
                    </div>
                    <div class="col-md-6">
                        <h5>Background Colors</h5>
                        <div class="bg-primary text-white p-2 mb-1">bg-primary</div>
                        <div class="bg-success text-white p-2 mb-1">bg-success</div>
                        <div class="bg-warning text-dark p-2 mb-1">bg-warning</div>
                        <div class="bg-danger text-white p-2 mb-1">bg-danger</div>
                        <div class="bg-info text-white p-2 mb-1">bg-info</div>
                        <div class="bg-light text-dark p-2 mb-1">bg-light</div>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Responsive demo -->
        <div class="row">
            <div class="col-12">
                <h3>Responsive Demo</h3>
                <div class="alert alert-info">
                    <strong>Eslatma:</strong> Ekran o'lchamini o'zgartiring va elementlarning qanday o'zgarayotganini kuzating.
                </div>
                
                <div class="row">
                    <div class="col-12 col-md-6 col-lg-4 mb-3">
                        <div class="card">
                            <div class="card-body text-center">
                                <h5 class="card-title">Mobil: 12 ustun</h5>
                                <p class="card-text">Planshet: 6 ustun</p>
                                <p class="card-text">Desktop: 4 ustun</p>
                            </div>
                        </div>
                    </div>
                    <div class="col-12 col-md-6 col-lg-4 mb-3">
                        <div class="card">
                            <div class="card-body text-center">
                                <h5 class="card-title">Responsive</h5>
                                <p class="card-text">Bootstrap utilities</p>
                                <p class="card-text">Yordamida</p>
                            </div>
                        </div>
                    </div>
                    <div class="col-12 col-md-12 col-lg-4 mb-3">
                        <div class="card">
                            <div class="card-body text-center">
                                <h5 class="card-title">Professional</h5>
                                <p class="card-text">Responsive dizayn</p>
                                <p class="card-text">Yaratish</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
```

</details>
