<details>
    <summary>Loyiha rejalashtirish</summary>

## 15.1 Loyiha Rejalashtirish

### Portfolio veb-sayti nima?

**Portfolio veb-sayti** - o'zingiz haqingizda, qilgan ishlaringiz haqida ma'lumot beruvchi va ko'rsatuvchi veb-sayt. Bu sizning professional imijingizni shakllantirish va ishga olish imkonini beradi.

### Portfolio veb-sayti qismlari

#### 1. Asosiy sahifalar
- **Bosh sahifa** - umumiy ma'lumot
- **Men haqimda** - shaxsiy ma'lumotlar
- **Loyihalarim** - qilgan ishlar
- **Aloqa** - bog'lanish ma'lumotlari

#### 2. Kontent elementlari
- Shaxsiy ma'lumotlar
- Rasmlar va portret
- Loyiha tavsiflari
- Texnik ko'nikmalar
- Aloqa formasi

### Loyiha rejalashtirish bosqichlari

#### 1. Maqsadni belgilash
```javascript
// Loyiha maqsadi
let loyihaMaqsadi = {
    nom: "Shaxsiy Portfolio Veb-sayti",
    maqsad: "O'zim haqimda ma'lumot berish va loyihalarimni ko'rsatish",
    auditoriya: "Ish beruvchilar, mijozlar, hamkasblar",
    muddat: "2 hafta"
};
```

#### 2. Texnik talablar
```javascript
// Texnik talablar
let texnikTalablar = {
    til: ["HTML5", "CSS3", "JavaScript"],
    dizayn: "Responsive design",
    brauzerlar: ["Chrome", "Firefox", "Safari", "Edge"],
    qurilmalar: ["Desktop", "Tablet", "Mobile"]
};
```

#### 3. Kontent rejasi
```javascript
// Kontent rejasi
let kontentRejasi = {
    boshSahifa: {
        salomlashish: "Salom, men [Ism]",
        qisqaTavsif: "Web dasturchi",
        asosiyRasm: "portret.jpg"
    },
    menHaqimda: {
        toliqTavsif: "Batafsil ma'lumot",
        ko'nikmalar: ["HTML", "CSS", "JavaScript"],
        tajriba: "Loyihalar ro'yxati"
    },
    loyihalar: {
        loyiha1: {
            nom: "Loyiha nomi",
            tavsif: "Loyiha haqida",
            texnologiyalar: ["HTML", "CSS", "JS"],
            rasm: "loyiha1.jpg"
        }
    },
    aloqa: {
        email: "email@example.com",
        telefon: "+998 90 123 45 67",
        manzil: "Shahar, Tuman",
        ijtimoiyTarmoqlar: ["GitHub", "LinkedIn"]
    }
};
```

### Loyiha tuzilishi

#### 1. Papkalar tuzilishi
```
portfolio-website/
├── index.html
├── css/
│   ├── style.css
│   └── responsive.css
├── js/
│   └── script.js
├── images/
│   ├── profile.jpg
│   ├── project1.jpg
│   └── project2.jpg
└── README.md
```

#### 2. HTML sahifalar
- `index.html` - bosh sahifa
- `about.html` - men haqimda
- `projects.html` - loyihalar
- `contact.html` - aloqa

#### 3. CSS fayllar
- `style.css` - asosiy stillar
- `responsive.css` - responsive dizayn

#### 4. JavaScript fayllar
- `script.js` - interaktivlik

### Loyiha rejalashtirish misoli
```javascript
// Loyiha rejalashtirish
let portfolioRejasi = {
    hafta1: {
        kun1_2: "HTML struktura yaratish",
        kun3_4: "CSS dizayn qilish",
        kun5: "JavaScript qo'shish"
    },
    hafta2: {
        kun1_2: "Responsive dizayn",
        kun3_4: "Test qilish va tuzatish",
        kun5: "Internetga joylashtirish"
    }
};

console.log("Loyiha rejasi:");
console.log("1-hafta:", portfolioRejasi.hafta1);
console.log("2-hafta:", portfolioRejasi.hafta2);

// Vazifalar ro'yxati
let vazifalar = [
    "HTML struktura yaratish",
    "CSS dizayn qilish", 
    "JavaScript interaktivlik qo'shish",
    "Responsive dizayn qilish",
    "Rasmlar va kontent qo'shish",
    "Test qilish va tuzatish",
    "Internetga joylashtirish"
];

console.log("\nVazifalar ro'yxati:");
for (let i = 0; i < vazifalar.length; i++) {
    console.log((i + 1) + ". " + vazifalar[i]);
}

// Loyiha maqsadlari
let maqsadlar = {
    asosiy: "Professional portfolio veb-sayti yaratish",
    qoshimcha: [
        "Responsive dizayn qilish",
        "JavaScript interaktivlik qo'shish",
        "SEO optimizatsiya",
        "Tez yuklanish"
    ]
};

console.log("\nMaqsadlar:");
console.log("Asosiy maqsad:", maqsadlar.asosiy);
console.log("Qo'shimcha maqsadlar:");
for (let i = 0; i < maqsadlar.qoshimcha.length; i++) {
    console.log("- " + maqsadlar.qoshimcha[i]);
}
```

### Loyiha rejalashtirish maslahatlari

#### 1. Maqsadni aniq belgilang
- Portfolio veb-sayti nima uchun kerak?
- Kim uchun yaratilmoqda?
- Qanday natija kutilmoqda?

#### 2. Texnik talablarni aniqlang
- Qanday texnologiyalar ishlatiladi?
- Qanday qurilmalar qo'llab-quvvatlanadi?
- Qanday brauzerlar ishlaydi?

#### 3. Vaqt rejasini tuzing
- Har bir vazifa uchun vaqt belgilang
- Muhim vazifalarni birinchi o'ringa qo'ying
- Zaxira vaqt qoldiring

</details>

<details>
    <summary>Barcha o'rganilgan texnologiyalarni qo'llash</summary>

## 15.2 Barcha O'rganilgan Texnologiyalarni Qo'llash

### HTML texnologiyalari

#### 1. Asosiy HTML struktura
```html
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mening Portfolio</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <!-- Portfolio kontenti -->
</body>
</html>
```

#### 2. Semantic HTML teglar
```html
<header>
    <nav>
        <ul>
            <li><a href="#home">Bosh sahifa</a></li>
            <li><a href="#about">Men haqimda</a></li>
            <li><a href="#projects">Loyihalar</a></li>
            <li><a href="#contact">Aloqa</a></li>
        </ul>
    </nav>
</header>

<main>
    <section id="home">
        <h1>Salom, men Ahmad</h1>
        <p>Web dasturchi</p>
    </section>
    
    <section id="about">
        <h2>Men haqimda</h2>
        <p>Mening haqimda ma'lumot</p>
    </section>
    
    <section id="projects">
        <h2>Loyihalarim</h2>
        <article>
            <h3>Loyiha nomi</h3>
            <p>Loyiha tavsifi</p>
        </article>
    </section>
    
    <section id="contact">
        <h2>Aloqa</h2>
        <form>
            <input type="text" placeholder="Ism">
            <input type="email" placeholder="Email">
            <textarea placeholder="Xabar"></textarea>
            <button type="submit">Yuborish</button>
        </form>
    </section>
</main>

<footer>
    <p>&copy; 2024 Mening Portfolio</p>
</footer>
```

### CSS texnologiyalari

#### 1. Asosiy CSS stillar
```css
/* Global stillar */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    color: #333;
}

/* Header stillari */
header {
    background-color: #2c3e50;
    color: white;
    padding: 1rem 0;
    position: fixed;
    width: 100%;
    top: 0;
    z-index: 1000;
}

nav ul {
    list-style: none;
    display: flex;
    justify-content: center;
}

nav li {
    margin: 0 1rem;
}

nav a {
    color: white;
    text-decoration: none;
    padding: 0.5rem 1rem;
    border-radius: 5px;
    transition: background-color 0.3s;
}

nav a:hover {
    background-color: #34495e;
}

/* Main kontent */
main {
    margin-top: 80px;
}

section {
    padding: 2rem 0;
    min-height: 100vh;
}

#home {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    text-align: center;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

#home h1 {
    font-size: 3rem;
    margin-bottom: 1rem;
}

#home p {
    font-size: 1.5rem;
}
```

#### 2. Flexbox layout
```css
/* Flexbox layout */
.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 1rem;
}

.flex-container {
    display: flex;
    flex-wrap: wrap;
    gap: 2rem;
    justify-content: center;
    align-items: center;
}

.flex-item {
    flex: 1;
    min-width: 300px;
    text-align: center;
}

/* Projects grid */
.projects-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 2rem;
    justify-content: center;
}

.project-card {
    background: white;
    border-radius: 10px;
    box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    padding: 1.5rem;
    max-width: 300px;
    transition: transform 0.3s;
}

.project-card:hover {
    transform: translateY(-10px);
}
```

#### 3. Responsive design
```css
/* Media queries */
@media (max-width: 768px) {
    #home h1 {
        font-size: 2rem;
    }
    
    #home p {
        font-size: 1.2rem;
    }
    
    nav ul {
        flex-direction: column;
        text-align: center;
    }
    
    nav li {
        margin: 0.5rem 0;
    }
    
    .projects-grid {
        flex-direction: column;
        align-items: center;
    }
}

@media (max-width: 480px) {
    .container {
        padding: 0 0.5rem;
    }
    
    section {
        padding: 1rem 0;
    }
    
    #home h1 {
        font-size: 1.5rem;
    }
}
```

### JavaScript texnologiyalari

#### 1. DOM manipulation
```javascript
// DOM elementlarni topish
let navLinks = document.querySelectorAll('nav a');
let sections = document.querySelectorAll('section');
let contactForm = document.getElementById('contact-form');

// Smooth scrolling
navLinks.forEach(link => {
    link.addEventListener('click', function(e) {
        e.preventDefault();
        let targetId = this.getAttribute('href');
        let targetSection = document.querySelector(targetId);
        
        if (targetSection) {
            targetSection.scrollIntoView({
                behavior: 'smooth'
            });
        }
    });
});

// Active nav link
window.addEventListener('scroll', function() {
    let current = '';
    sections.forEach(section => {
        let sectionTop = section.offsetTop;
        let sectionHeight = section.clientHeight;
        
        if (window.pageYOffset >= (sectionTop - 200)) {
            current = section.getAttribute('id');
        }
    });
    
    navLinks.forEach(link => {
        link.classList.remove('active');
        if (link.getAttribute('href') === '#' + current) {
            link.classList.add('active');
        }
    });
});
```

#### 2. Form handling
```javascript
// Contact form handling
if (contactForm) {
    contactForm.addEventListener('submit', function(e) {
        e.preventDefault();
        
        let formData = new FormData(this);
        let name = formData.get('name');
        let email = formData.get('email');
        let message = formData.get('message');
        
        // Form validation
        if (!name || !email || !message) {
            alert('Barcha maydonlarni to\'ldiring!');
            return;
        }
        
        // Email validation
        let emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
        if (!emailRegex.test(email)) {
            alert('Noto\'g\'ri email manzil!');
            return;
        }
        
        // Success message
        alert('Xabaringiz yuborildi! Tez orada javob beramiz.');
        this.reset();
    });
}
```

#### 3. LocalStorage bilan ishlash
```javascript
// Portfolio preferences
let portfolioSettings = {
    theme: 'light',
    language: 'uz',
    showProjects: true
};

// Settings ni saqlash
function saveSettings() {
    localStorage.setItem('portfolioSettings', JSON.stringify(portfolioSettings));
}

// Settings ni olish
function loadSettings() {
    let saved = localStorage.getItem('portfolioSettings');
    if (saved) {
        portfolioSettings = JSON.parse(saved);
        applySettings();
    }
}

// Settings ni qo'llash
function applySettings() {
    // Theme qo'llash
    if (portfolioSettings.theme === 'dark') {
        document.body.classList.add('dark-theme');
    } else {
        document.body.classList.remove('dark-theme');
    }
    
    // Projects ko'rsatish
    let projectsSection = document.getElementById('projects');
    if (projectsSection) {
        projectsSection.style.display = portfolioSettings.showProjects ? 'block' : 'none';
    }
}

// Settings ni o'zgartirish
function toggleTheme() {
    portfolioSettings.theme = portfolioSettings.theme === 'light' ? 'dark' : 'light';
    saveSettings();
    applySettings();
}

// Sahifa yuklanganda settings ni yuklash
window.addEventListener('load', loadSettings);
```

#### 4. Animatsiyalar va effektlar
```javascript
// Scroll animations
function animateOnScroll() {
    let elements = document.querySelectorAll('.animate-on-scroll');
    
    elements.forEach(element => {
        let elementTop = element.offsetTop;
        let elementHeight = element.offsetHeight;
        let windowTop = window.pageYOffset;
        let windowHeight = window.innerHeight;
        
        if (windowTop > (elementTop - windowHeight + elementHeight)) {
            element.classList.add('animated');
        }
    });
}

// Intersection Observer
let observerOptions = {
    threshold: 0.1,
    rootMargin: '0px 0px -50px 0px'
};

let observer = new IntersectionObserver(function(entries) {
    entries.forEach(entry => {
        if (entry.isIntersecting) {
            entry.target.classList.add('animate-in');
        }
    });
}, observerOptions);

// Observe elements
document.querySelectorAll('.project-card').forEach(card => {
    observer.observe(card);
});

// Scroll event
window.addEventListener('scroll', animateOnScroll);
```

### Amaliy misol - Texnologiyalarni birlashtirish
```javascript
// Portfolio veb-sayti asosiy funksiyalari
let portfolioApp = {
    // Initialization
    init: function() {
        this.setupNavigation();
        this.setupForms();
        this.setupAnimations();
        this.loadSettings();
        console.log('Portfolio veb-sayti yuklandi!');
    },
    
    // Navigation setup
    setupNavigation: function() {
        let navLinks = document.querySelectorAll('nav a');
        navLinks.forEach(link => {
            link.addEventListener('click', this.handleNavClick);
        });
        
        window.addEventListener('scroll', this.handleScroll);
    },
    
    // Nav click handler
    handleNavClick: function(e) {
        e.preventDefault();
        let targetId = this.getAttribute('href');
        let targetSection = document.querySelector(targetId);
        
        if (targetSection) {
            targetSection.scrollIntoView({
                behavior: 'smooth'
            });
        }
    },
    
    // Scroll handler
    handleScroll: function() {
        let sections = document.querySelectorAll('section');
        let navLinks = document.querySelectorAll('nav a');
        let current = '';
        
        sections.forEach(section => {
            let sectionTop = section.offsetTop;
            if (window.pageYOffset >= (sectionTop - 200)) {
                current = section.getAttribute('id');
            }
        });
        
        navLinks.forEach(link => {
            link.classList.remove('active');
            if (link.getAttribute('href') === '#' + current) {
                link.classList.add('active');
            }
        });
    },
    
    // Forms setup
    setupForms: function() {
        let contactForm = document.getElementById('contact-form');
        if (contactForm) {
            contactForm.addEventListener('submit', this.handleFormSubmit);
        }
    },
    
    // Form submit handler
    handleFormSubmit: function(e) {
        e.preventDefault();
        let formData = new FormData(this);
        let data = Object.fromEntries(formData);
        
        // Validation
        if (!data.name || !data.email || !data.message) {
            alert('Barcha maydonlarni to\'ldiring!');
            return;
        }
        
        // Save to localStorage
        let messages = JSON.parse(localStorage.getItem('contactMessages') || '[]');
        messages.push({
            ...data,
            timestamp: new Date().toISOString()
        });
        localStorage.setItem('contactMessages', JSON.stringify(messages));
        
        alert('Xabaringiz saqlandi!');
        this.reset();
    },
    
    // Animations setup
    setupAnimations: function() {
        let observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };
        
        let observer = new IntersectionObserver(function(entries) {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('animate-in');
                }
            });
        }, observerOptions);
        
        document.querySelectorAll('.project-card').forEach(card => {
            observer.observe(card);
        });
    },
    
    // Load settings
    loadSettings: function() {
        let settings = JSON.parse(localStorage.getItem('portfolioSettings') || '{}');
        this.applySettings(settings);
    },
    
    // Apply settings
    applySettings: function(settings) {
        if (settings.theme === 'dark') {
            document.body.classList.add('dark-theme');
        }
        
        if (settings.language === 'en') {
            // Language switching logic
        }
    },
    
    // Utility functions
    utils: {
        // Debounce function
        debounce: function(func, wait) {
            let timeout;
            return function executedFunction(...args) {
                const later = () => {
                    clearTimeout(timeout);
                    func(...args);
                };
                clearTimeout(timeout);
                timeout = setTimeout(later, wait);
            };
        },
        
        // Throttle function
        throttle: function(func, limit) {
            let inThrottle;
            return function() {
                const args = arguments;
                const context = this;
                if (!inThrottle) {
                    func.apply(context, args);
                    inThrottle = true;
                    setTimeout(() => inThrottle = false, limit);
                }
            };
        }
    }
};

// Initialize portfolio app
document.addEventListener('DOMContentLoaded', function() {
    portfolioApp.init();
});
```

### Texnologiyalarni qo'llash maslahatlari

#### 1. HTML struktura
- Semantic teglardan foydalaning
- Accessibility qoidalarini qo'llang
- SEO optimizatsiya qiling

#### 2. CSS dizayn
- Mobile-first yondashuv
- Flexbox va Grid dan foydalaning
- CSS custom properties ishlating

#### 3. JavaScript funksionallik
- DOM manipulation
- Event handling
- LocalStorage
- Animatsiyalar

#### 4. Performance
- Optimizatsiya qiling
- Lazy loading qo'llang
- Minification qiling

</details>

<details>
    <summary>HTML struktura yaratish</summary>

## 15.3 HTML Struktura Yaratish

### Portfolio HTML struktura

#### 1. Asosiy HTML shablon
```html
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ahmad Karimov - Portfolio</title>
    <meta name="description" content="Web dasturchi Ahmad Karimovning shaxsiy portfolio veb-sayti">
    <meta name="keywords" content="web dasturchi, portfolio, HTML, CSS, JavaScript">
    <link rel="stylesheet" href="css/style.css">
    <link rel="stylesheet" href="css/responsive.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
</head>
<body>
    <!-- Navigation -->
    <header>
        <nav class="navbar">
            <div class="nav-container">
                <div class="nav-logo">
                    <a href="#home">Ahmad K.</a>
                </div>
                <ul class="nav-menu">
                    <li class="nav-item">
                        <a href="#home" class="nav-link">Bosh sahifa</a>
                    </li>
                    <li class="nav-item">
                        <a href="#about" class="nav-link">Men haqimda</a>
                    </li>
                    <li class="nav-item">
                        <a href="#skills" class="nav-link">Ko'nikmalar</a>
                    </li>
                    <li class="nav-item">
                        <a href="#projects" class="nav-link">Loyihalar</a>
                    </li>
                    <li class="nav-item">
                        <a href="#contact" class="nav-link">Aloqa</a>
                    </li>
                </ul>
                <div class="nav-toggle">
                    <span class="bar"></span>
                    <span class="bar"></span>
                    <span class="bar"></span>
                </div>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <main>
        <!-- Hero Section -->
        <section id="home" class="hero">
            <div class="container">
                <div class="hero-content">
                    <div class="hero-text">
                        <h1 class="hero-title">
                            Salom, men <span class="highlight">Ahmad Karimov</span>
                        </h1>
                        <p class="hero-subtitle">Web dasturchi va dizayner</p>
                        <p class="hero-description">
                            Men zamonaviy veb-saytlar yaratish va foydalanuvchi tajribasini 
                            yaxshilash bo'yicha ishlayman. HTML, CSS, JavaScript texnologiyalarida 
                            tajribam bor.
                        </p>
                        <div class="hero-buttons">
                            <a href="#projects" class="btn btn-primary">Loyihalarimni ko'ring</a>
                            <a href="#contact" class="btn btn-secondary">Aloqa</a>
                        </div>
                    </div>
                    <div class="hero-image">
                        <img src="images/profile.jpg" alt="Ahmad Karimov" class="profile-img">
                    </div>
                </div>
            </div>
        </section>

        <!-- About Section -->
        <section id="about" class="about">
            <div class="container">
                <h2 class="section-title">Men haqimda</h2>
                <div class="about-content">
                    <div class="about-text">
                        <p>
                            Men 15 yoshda bo'lib, web dasturlash sohasida ishlayman. 
                            Dasturlash asoslari kursini tamomlaganman va endi professional 
                            darajada loyihalar yaratishga harakat qilaman.
                        </p>
                        <p>
                            Mening asosiy qiziqishlarim: veb-dizayn, front-end dasturlash, 
                            foydalanuvchi tajribasi dizayni va yangi texnologiyalarni o'rganish.
                        </p>
                        <div class="about-stats">
                            <div class="stat">
                                <h3>2+</h3>
                                <p>Yil tajriba</p>
                            </div>
                            <div class="stat">
                                <h3>10+</h3>
                                <p>Loyiha</p>
                            </div>
                            <div class="stat">
                                <h3>5+</h3>
                                <p>Texnologiya</p>
                            </div>
                        </div>
                    </div>
                    <div class="about-image">
                        <img src="images/about.jpg" alt="Ahmad haqida" class="about-img">
                    </div>
                </div>
            </div>
        </section>

        <!-- Skills Section -->
        <section id="skills" class="skills">
            <div class="container">
                <h2 class="section-title">Ko'nikmalarim</h2>
                <div class="skills-grid">
                    <div class="skill-category">
                        <h3>Front-end</h3>
                        <div class="skill-items">
                            <div class="skill-item">
                                <span class="skill-name">HTML5</span>
                                <div class="skill-bar">
                                    <div class="skill-progress" data-width="90"></div>
                                </div>
                            </div>
                            <div class="skill-item">
                                <span class="skill-name">CSS3</span>
                                <div class="skill-bar">
                                    <div class="skill-progress" data-width="85"></div>
                                </div>
                            </div>
                            <div class="skill-item">
                                <span class="skill-name">JavaScript</span>
                                <div class="skill-bar">
                                    <div class="skill-progress" data-width="75"></div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="skill-category">
                        <h3>Dizayn</h3>
                        <div class="skill-items">
                            <div class="skill-item">
                                <span class="skill-name">Responsive Design</span>
                                <div class="skill-bar">
                                    <div class="skill-progress" data-width="80"></div>
                                </div>
                            </div>
                            <div class="skill-item">
                                <span class="skill-name">UI/UX</span>
                                <div class="skill-bar">
                                    <div class="skill-progress" data-width="70"></div>
                                </div>
                            </div>
                            <div class="skill-item">
                                <span class="skill-name">Figma</span>
                                <div class="skill-bar">
                                    <div class="skill-progress" data-width="65"></div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Projects Section -->
        <section id="projects" class="projects">
            <div class="container">
                <h2 class="section-title">Loyihalarim</h2>
                <div class="projects-filter">
                    <button class="filter-btn active" data-filter="all">Barchasi</button>
                    <button class="filter-btn" data-filter="web">Veb-saytlar</button>
                    <button class="filter-btn" data-filter="app">Ilovalar</button>
                    <button class="filter-btn" data-filter="design">Dizayn</button>
                </div>
                <div class="projects-grid">
                    <article class="project-card" data-category="web">
                        <div class="project-image">
                            <img src="images/project1.jpg" alt="Loyiha 1">
                            <div class="project-overlay">
                                <a href="#" class="project-link">Ko'rish</a>
                                <a href="#" class="project-github">GitHub</a>
                            </div>
                        </div>
                        <div class="project-content">
                            <h3 class="project-title">E-commerce Veb-sayt</h3>
                            <p class="project-description">
                                Zamonaviy onlayn do'kon veb-sayti. Responsive dizayn, 
                                foydalanuvchi do'st interfeys.
                            </p>
                            <div class="project-tech">
                                <span class="tech-tag">HTML</span>
                                <span class="tech-tag">CSS</span>
                                <span class="tech-tag">JavaScript</span>
                            </div>
                        </div>
                    </article>

                    <article class="project-card" data-category="web">
                        <div class="project-image">
                            <img src="images/project2.jpg" alt="Loyiha 2">
                            <div class="project-overlay">
                                <a href="#" class="project-link">Ko'rish</a>
                                <a href="#" class="project-github">GitHub</a>
                            </div>
                        </div>
                        <div class="project-content">
                            <h3 class="project-title">Blog Platformasi</h3>
                            <p class="project-description">
                                Blog yozish va o'qish uchun platforma. 
                                Admin paneli va foydalanuvchi interfeysi.
                            </p>
                            <div class="project-tech">
                                <span class="tech-tag">HTML</span>
                                <span class="tech-tag">CSS</span>
                                <span class="tech-tag">JavaScript</span>
                            </div>
                        </div>
                    </article>

                    <article class="project-card" data-category="app">
                        <div class="project-image">
                            <img src="images/project3.jpg" alt="Loyiha 3">
                            <div class="project-overlay">
                                <a href="#" class="project-link">Ko'rish</a>
                                <a href="#" class="project-github">GitHub</a>
                            </div>
                        </div>
                        <div class="project-content">
                            <h3 class="project-title">Vazifalar Menejeri</h3>
                            <p class="project-description">
                                Kundalik vazifalarni boshqarish uchun ilova. 
                                LocalStorage bilan ma'lumot saqlash.
                            </p>
                            <div class="project-tech">
                                <span class="tech-tag">HTML</span>
                                <span class="tech-tag">CSS</span>
                                <span class="tech-tag">JavaScript</span>
                            </div>
                        </div>
                    </article>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact" class="contact">
            <div class="container">
                <h2 class="section-title">Aloqa</h2>
                <div class="contact-content">
                    <div class="contact-info">
                        <h3>Keling, gaplashaylik!</h3>
                        <p>
                            Men yangi loyihalar va hamkorlik uchun har doim tayyor. 
                            Sizning loyihangiz haqida gaplashishni xohlayman.
                        </p>
                        <div class="contact-details">
                            <div class="contact-item">
                                <i class="icon">📧</i>
                                <div>
                                    <h4>Email</h4>
                                    <p>ahmad.karimov@example.com</p>
                                </div>
                            </div>
                            <div class="contact-item">
                                <i class="icon">📱</i>
                                <div>
                                    <h4>Telefon</h4>
                                    <p>+998 90 123 45 67</p>
                                </div>
                            </div>
                            <div class="contact-item">
                                <i class="icon">📍</i>
                                <div>
                                    <h4>Manzil</h4>
                                    <p>Toshkent, O'zbekiston</p>
                                </div>
                            </div>
                        </div>
                        <div class="social-links">
                            <a href="#" class="social-link">GitHub</a>
                            <a href="#" class="social-link">LinkedIn</a>
                            <a href="#" class="social-link">Twitter</a>
                        </div>
                    </div>
                    <div class="contact-form">
                        <form id="contact-form">
                            <div class="form-group">
                                <label for="name">Ism</label>
                                <input type="text" id="name" name="name" required>
                            </div>
                            <div class="form-group">
                                <label for="email">Email</label>
                                <input type="email" id="email" name="email" required>
                            </div>
                            <div class="form-group">
                                <label for="subject">Mavzu</label>
                                <input type="text" id="subject" name="subject" required>
                            </div>
                            <div class="form-group">
                                <label for="message">Xabar</label>
                                <textarea id="message" name="message" rows="5" required></textarea>
                            </div>
                            <button type="submit" class="btn btn-primary">Xabar yuborish</button>
                        </form>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <div class="footer-content">
                <div class="footer-text">
                    <p>&copy; 2024 Ahmad Karimov. Barcha huquqlar himoyalangan.</p>
                </div>
                <div class="footer-links">
                    <a href="#home">Bosh sahifa</a>
                    <a href="#about">Men haqimda</a>
                    <a href="#projects">Loyihalar</a>
                    <a href="#contact">Aloqa</a>
                </div>
            </div>
        </div>
    </footer>

    <!-- JavaScript -->
    <script src="js/script.js"></script>
</body>
</html>
```

### HTML strukturaning muhim qismlari

#### 1. Meta teglar
```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Web dasturchi portfolio">
<meta name="keywords" content="web dasturchi, portfolio, HTML, CSS, JavaScript">
```

#### 2. Semantic HTML
```html
<header> <!-- Sahifa sarlavhasi -->
<nav>    <!-- Navigatsiya -->
<main>   <!-- Asosiy kontent -->
<section> <!-- Kontent bo'limlari -->
<article> <!-- Mustaqil maqolalar -->
<aside>   <!-- Qo'shimcha ma'lumot -->
<footer>  <!-- Sahifa pastki qismi -->
```

#### 3. Accessibility
```html
<!-- Alt atributlari -->
<img src="profile.jpg" alt="Ahmad Karimov portreti">

<!-- Label teglar -->
<label for="name">Ism</label>
<input type="text" id="name" name="name">

<!-- ARIA atributlari -->
<button aria-label="Menu ochish">
<nav role="navigation">
```

#### 4. SEO optimizatsiya
```html
<!-- Sarlavha ierarxiyasi -->
<h1>Asosiy sarlavha</h1>
<h2>Bo'lim sarlavhasi</h2>
<h3>Kichik sarlavha</h3>

<!-- Meta description -->
<meta name="description" content="Qisqa tavsif">

<!-- Open Graph -->
<meta property="og:title" content="Sahifa sarlavhasi">
<meta property="og:description" content="Sahifa tavsifi">
<meta property="og:image" content="rasm.jpg">
```

### HTML strukturaning afzalliklari

#### 1. Semantic HTML
- Brauzer va screen reader uchun tushunarli
- SEO uchun yaxshi
- Kod o'qilishi oson

#### 2. Accessibility
- Barcha foydalanuvchilar uchun kirish imkoniyati
- Screen reader qo'llab-quvvatlash
- Keyboard navigation

#### 3. SEO
- Qidiruv tizimlari uchun optimizatsiya
- Meta ma'lumotlar
- Semantic struktura

#### 4. Maintainability
- Kod tashkil etish
- Oson tahrirlash
- Kengaytirish imkoniyati

### HTML yaratish maslahatlari

#### 1. Struktura
- Semantic teglardan foydalaning
- Mantiqiy ierarxiya yarating
- ID va class nomlarini aniq yozing

#### 2. Accessibility
- Alt atributlarini qo'shing
- Label teglarini ishlating
- ARIA atributlarini qo'llang

#### 3. SEO
- Meta ma'lumotlarni to'ldiring
- Sarlavha ierarxiyasini to'g'ri qiling
- Open Graph teglarini qo'shing

#### 4. Performance
- Rasmlarni optimizatsiya qiling
- CSS va JS fayllarini minify qiling
- Lazy loading qo'llang

</details>

<details>
    <summary>CSS bilan chiroyli dizayn</summary>

## 15.4 CSS bilan Chiroyli Dizayn

### Portfolio CSS dizayn

#### 1. Asosiy CSS fayl (style.css)
```css
/* CSS Reset va Global Stillar */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

:root {
    /* CSS Custom Properties */
    --primary-color: #667eea;
    --secondary-color: #764ba2;
    --accent-color: #f093fb;
    --text-color: #333;
    --text-light: #666;
    --bg-color: #fff;
    --bg-light: #f8f9fa;
    --border-color: #e9ecef;
    --shadow: 0 5px 15px rgba(0,0,0,0.1);
    --shadow-hover: 0 10px 25px rgba(0,0,0,0.15);
    --border-radius: 8px;
    --transition: all 0.3s ease;
    --font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
}

/* Dark theme variables */
[data-theme="dark"] {
    --text-color: #fff;
    --text-light: #ccc;
    --bg-color: #1a1a1a;
    --bg-light: #2d2d2d;
    --border-color: #404040;
}

body {
    font-family: var(--font-family);
    line-height: 1.6;
    color: var(--text-color);
    background-color: var(--bg-color);
    overflow-x: hidden;
}

/* Smooth scrolling */
html {
    scroll-behavior: smooth;
}

/* Container */
.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 1rem;
}

/* Typography */
h1, h2, h3, h4, h5, h6 {
    font-weight: 600;
    line-height: 1.2;
    margin-bottom: 1rem;
}

h1 { font-size: 3rem; }
h2 { font-size: 2.5rem; }
h3 { font-size: 2rem; }
h4 { font-size: 1.5rem; }
h5 { font-size: 1.25rem; }
h6 { font-size: 1rem; }

p {
    margin-bottom: 1rem;
    color: var(--text-light);
}

/* Section styling */
section {
    padding: 5rem 0;
}

.section-title {
    text-align: center;
    margin-bottom: 3rem;
    position: relative;
}

.section-title::after {
    content: '';
    position: absolute;
    bottom: -10px;
    left: 50%;
    transform: translateX(-50%);
    width: 60px;
    height: 4px;
    background: linear-gradient(45deg, var(--primary-color), var(--secondary-color));
    border-radius: 2px;
}
```

#### 2. Navigation dizayn
```css
/* Header va Navigation */
header {
    position: fixed;
    top: 0;
    width: 100%;
    background: rgba(255, 255, 255, 0.95);
    backdrop-filter: blur(10px);
    border-bottom: 1px solid var(--border-color);
    z-index: 1000;
    transition: var(--transition);
}

.navbar {
    padding: 1rem 0;
}

.nav-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.nav-logo a {
    font-size: 1.5rem;
    font-weight: 700;
    color: var(--primary-color);
    text-decoration: none;
}

.nav-menu {
    display: flex;
    list-style: none;
    gap: 2rem;
}

.nav-link {
    color: var(--text-color);
    text-decoration: none;
    font-weight: 500;
    padding: 0.5rem 1rem;
    border-radius: var(--border-radius);
    transition: var(--transition);
    position: relative;
}

.nav-link:hover,
.nav-link.active {
    color: var(--primary-color);
    background-color: rgba(102, 126, 234, 0.1);
}

/* Mobile menu toggle */
.nav-toggle {
    display: none;
    flex-direction: column;
    cursor: pointer;
}

.bar {
    width: 25px;
    height: 3px;
    background-color: var(--text-color);
    margin: 3px 0;
    transition: var(--transition);
}
```

#### 3. Hero section dizayn
```css
/* Hero Section */
.hero {
    min-height: 100vh;
    display: flex;
    align-items: center;
    background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
    color: white;
    position: relative;
    overflow: hidden;
}

.hero::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 1000"><polygon fill="rgba(255,255,255,0.1)" points="0,1000 1000,0 1000,1000"/></svg>');
    background-size: cover;
}

.hero-content {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    align-items: center;
    position: relative;
    z-index: 2;
}

.hero-title {
    font-size: 3.5rem;
    margin-bottom: 1rem;
    animation: fadeInUp 1s ease-out;
}

.highlight {
    background: linear-gradient(45deg, var(--accent-color), #ff6b6b);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
}

.hero-subtitle {
    font-size: 1.5rem;
    margin-bottom: 1rem;
    opacity: 0.9;
    animation: fadeInUp 1s ease-out 0.2s both;
}

.hero-description {
    font-size: 1.1rem;
    margin-bottom: 2rem;
    opacity: 0.8;
    animation: fadeInUp 1s ease-out 0.4s both;
}

.hero-buttons {
    display: flex;
    gap: 1rem;
    animation: fadeInUp 1s ease-out 0.6s both;
}

.hero-image {
    text-align: center;
    animation: fadeInRight 1s ease-out 0.8s both;
}

.profile-img {
    width: 300px;
    height: 300px;
    border-radius: 50%;
    object-fit: cover;
    border: 5px solid rgba(255, 255, 255, 0.2);
    box-shadow: var(--shadow-hover);
}

/* Animations */
@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(30px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

@keyframes fadeInRight {
    from {
        opacity: 0;
        transform: translateX(30px);
    }
    to {
        opacity: 1;
        transform: translateX(0);
    }
}
```

#### 4. Buttons dizayn
```css
/* Buttons */
.btn {
    display: inline-block;
    padding: 1rem 2rem;
    border-radius: var(--border-radius);
    text-decoration: none;
    font-weight: 500;
    transition: var(--transition);
    border: none;
    cursor: pointer;
    font-size: 1rem;
}

.btn-primary {
    background: linear-gradient(45deg, var(--primary-color), var(--secondary-color));
    color: white;
    box-shadow: var(--shadow);
}

.btn-primary:hover {
    transform: translateY(-2px);
    box-shadow: var(--shadow-hover);
}

.btn-secondary {
    background: transparent;
    color: white;
    border: 2px solid white;
}

.btn-secondary:hover {
    background: white;
    color: var(--primary-color);
}
```

#### 5. About section dizayn
```css
/* About Section */
.about {
    background-color: var(--bg-light);
}

.about-content {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    align-items: center;
}

.about-text {
    font-size: 1.1rem;
    line-height: 1.8;
}

.about-stats {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2rem;
    margin-top: 2rem;
}

.stat {
    text-align: center;
    padding: 1.5rem;
    background: white;
    border-radius: var(--border-radius);
    box-shadow: var(--shadow);
    transition: var(--transition);
}

.stat:hover {
    transform: translateY(-5px);
    box-shadow: var(--shadow-hover);
}

.stat h3 {
    font-size: 2.5rem;
    color: var(--primary-color);
    margin-bottom: 0.5rem;
}

.about-img {
    width: 100%;
    border-radius: var(--border-radius);
    box-shadow: var(--shadow);
}
```

#### 6. Skills section dizayn
```css
/* Skills Section */
.skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
    gap: 3rem;
}

.skill-category {
    background: white;
    padding: 2rem;
    border-radius: var(--border-radius);
    box-shadow: var(--shadow);
    transition: var(--transition);
}

.skill-category:hover {
    transform: translateY(-5px);
    box-shadow: var(--shadow-hover);
}

.skill-category h3 {
    color: var(--primary-color);
    margin-bottom: 1.5rem;
    text-align: center;
}

.skill-item {
    margin-bottom: 1.5rem;
}

.skill-name {
    display: block;
    margin-bottom: 0.5rem;
    font-weight: 500;
}

.skill-bar {
    width: 100%;
    height: 8px;
    background-color: var(--border-color);
    border-radius: 4px;
    overflow: hidden;
}

.skill-progress {
    height: 100%;
    background: linear-gradient(45deg, var(--primary-color), var(--secondary-color));
    border-radius: 4px;
    transition: width 1s ease-in-out;
    width: 0;
}

.skill-progress.animate {
    width: var(--width, 0%);
}
```

#### 7. Projects section dizayn
```css
/* Projects Section */
.projects {
    background-color: var(--bg-light);
}

.projects-filter {
    display: flex;
    justify-content: center;
    gap: 1rem;
    margin-bottom: 3rem;
    flex-wrap: wrap;
}

.filter-btn {
    padding: 0.75rem 1.5rem;
    border: 2px solid var(--primary-color);
    background: transparent;
    color: var(--primary-color);
    border-radius: var(--border-radius);
    cursor: pointer;
    transition: var(--transition);
    font-weight: 500;
}

.filter-btn:hover,
.filter-btn.active {
    background: var(--primary-color);
    color: white;
}

.projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
    gap: 2rem;
}

.project-card {
    background: white;
    border-radius: var(--border-radius);
    overflow: hidden;
    box-shadow: var(--shadow);
    transition: var(--transition);
    opacity: 1;
    transform: scale(1);
}

.project-card:hover {
    transform: translateY(-10px);
    box-shadow: var(--shadow-hover);
}

.project-card.hide {
    opacity: 0;
    transform: scale(0.8);
    pointer-events: none;
}

.project-image {
    position: relative;
    overflow: hidden;
    height: 250px;
}

.project-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: var(--transition);
}

.project-overlay {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgba(102, 126, 234, 0.9);
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 1rem;
    opacity: 0;
    transition: var(--transition);
}

.project-card:hover .project-overlay {
    opacity: 1;
}

.project-card:hover .project-image img {
    transform: scale(1.1);
}

.project-link,
.project-github {
    padding: 0.75rem 1.5rem;
    background: white;
    color: var(--primary-color);
    text-decoration: none;
    border-radius: var(--border-radius);
    font-weight: 500;
    transition: var(--transition);
}

.project-link:hover,
.project-github:hover {
    background: var(--primary-color);
    color: white;
}

.project-content {
    padding: 1.5rem;
}

.project-title {
    color: var(--text-color);
    margin-bottom: 1rem;
}

.project-description {
    color: var(--text-light);
    margin-bottom: 1.5rem;
    line-height: 1.6;
}

.project-tech {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
}

.tech-tag {
    padding: 0.25rem 0.75rem;
    background: var(--bg-light);
    color: var(--primary-color);
    border-radius: 20px;
    font-size: 0.875rem;
    font-weight: 500;
}
```

#### 8. Contact section dizayn
```css
/* Contact Section */
.contact-content {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
}

.contact-info h3 {
    color: var(--primary-color);
    margin-bottom: 1rem;
}

.contact-details {
    margin: 2rem 0;
}

.contact-item {
    display: flex;
    align-items: center;
    gap: 1rem;
    margin-bottom: 1.5rem;
}

.contact-item .icon {
    font-size: 1.5rem;
    width: 50px;
    height: 50px;
    background: var(--primary-color);
    color: white;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
}

.contact-item h4 {
    margin-bottom: 0.25rem;
    color: var(--text-color);
}

.contact-item p {
    color: var(--text-light);
    margin: 0;
}

.social-links {
    display: flex;
    gap: 1rem;
    margin-top: 2rem;
}

.social-link {
    padding: 0.75rem 1.5rem;
    background: var(--primary-color);
    color: white;
    text-decoration: none;
    border-radius: var(--border-radius);
    transition: var(--transition);
}

.social-link:hover {
    background: var(--secondary-color);
    transform: translateY(-2px);
}

/* Contact Form */
.contact-form {
    background: white;
    padding: 2rem;
    border-radius: var(--border-radius);
    box-shadow: var(--shadow);
}

.form-group {
    margin-bottom: 1.5rem;
}

.form-group label {
    display: block;
    margin-bottom: 0.5rem;
    font-weight: 500;
    color: var(--text-color);
}

.form-group input,
.form-group textarea {
    width: 100%;
    padding: 1rem;
    border: 2px solid var(--border-color);
    border-radius: var(--border-radius);
    font-size: 1rem;
    transition: var(--transition);
    font-family: inherit;
}

.form-group input:focus,
.form-group textarea:focus {
    outline: none;
    border-color: var(--primary-color);
    box-shadow: 0 0 0 3px rgba(102, 126, 234, 0.1);
}

.form-group textarea {
    resize: vertical;
    min-height: 120px;
}
```

#### 9. Footer dizayn
```css
/* Footer */
.footer {
    background: var(--text-color);
    color: white;
    padding: 2rem 0;
}

.footer-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 1rem;
}

.footer-links {
    display: flex;
    gap: 2rem;
}

.footer-links a {
    color: white;
    text-decoration: none;
    transition: var(--transition);
}

.footer-links a:hover {
    color: var(--primary-color);
}
```

### CSS dizayn afzalliklari

#### 1. Modern CSS
- CSS Custom Properties (variables)
- Flexbox va Grid layout
- CSS animations va transitions
- Modern selectors

#### 2. Responsive Design
- Mobile-first approach
- Flexible grid systems
- Media queries
- Fluid typography

#### 3. Performance
- Optimized selectors
- Efficient animations
- Minimal repaints
- Hardware acceleration

#### 4. Maintainability
- Organized code structure
- Reusable components
- Consistent naming
- Documentation

### CSS dizayn maslahatlari

#### 1. Planning
- Design system yarating
- Color palette tanlang
- Typography hierarchy
- Spacing system

#### 2. Organization
- Logical file structure
- Component-based CSS
- Consistent naming
- Comments qo'shing

#### 3. Performance
- Minimal CSS
- Efficient selectors
- Optimized animations
- Critical CSS

#### 4. Accessibility
- Color contrast
- Focus states
- Screen reader support
- Keyboard navigation

</details>

<details>
    <summary>JavaScript interaktivlik</summary>

## 15.5 JavaScript Interaktivlik

### Portfolio JavaScript funksionalligi

#### 1. Asosiy JavaScript fayl (script.js)
```javascript
// Portfolio JavaScript funksiyalari
let portfolioApp = {
    // App initialization
    init: function() {
        this.setupNavigation();
        this.setupMobileMenu();
        this.setupScrollEffects();
        this.setupProjectFilter();
        this.setupContactForm();
        this.setupSkillBars();
        this.setupThemeToggle();
        this.setupAnimations();
        console.log('Portfolio app initialized!');
    },

    // Navigation setup
    setupNavigation: function() {
        let navLinks = document.querySelectorAll('.nav-link');
        let sections = document.querySelectorAll('section');

        // Smooth scrolling
        navLinks.forEach(link => {
            link.addEventListener('click', function(e) {
                e.preventDefault();
                let targetId = this.getAttribute('href');
                let targetSection = document.querySelector(targetId);
                
                if (targetSection) {
                    targetSection.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Active link highlighting
        window.addEventListener('scroll', this.debounce(() => {
            let current = '';
            let scrollPos = window.pageYOffset + 100;

            sections.forEach(section => {
                let sectionTop = section.offsetTop;
                let sectionHeight = section.clientHeight;
                
                if (scrollPos >= sectionTop && scrollPos < sectionTop + sectionHeight) {
                    current = section.getAttribute('id');
                }
            });

            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href') === '#' + current) {
                    link.classList.add('active');
                }
            });
        }, 100));
    },

    // Mobile menu setup
    setupMobileMenu: function() {
        let navToggle = document.querySelector('.nav-toggle');
        let navMenu = document.querySelector('.nav-menu');

        if (navToggle && navMenu) {
            navToggle.addEventListener('click', function() {
                navMenu.classList.toggle('active');
                navToggle.classList.toggle('active');
            });

            // Close menu when clicking on links
            document.querySelectorAll('.nav-link').forEach(link => {
                link.addEventListener('click', () => {
                    navMenu.classList.remove('active');
                    navToggle.classList.remove('active');
                });
            });
        }
    },

    // Scroll effects
    setupScrollEffects: function() {
        // Header background on scroll
        window.addEventListener('scroll', () => {
            let header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });

        // Parallax effect for hero section
        window.addEventListener('scroll', () => {
            let scrolled = window.pageYOffset;
            let hero = document.querySelector('.hero');
            if (hero) {
                hero.style.transform = `translateY(${scrolled * 0.5}px)`;
            }
        });
    },

    // Project filtering
    setupProjectFilter: function() {
        let filterButtons = document.querySelectorAll('.filter-btn');
        let projectCards = document.querySelectorAll('.project-card');

        filterButtons.forEach(button => {
            button.addEventListener('click', function() {
                let filter = this.getAttribute('data-filter');

                // Update active button
                filterButtons.forEach(btn => btn.classList.remove('active'));
                this.classList.add('active');

                // Filter projects
                projectCards.forEach(card => {
                    let category = card.getAttribute('data-category');
                    
                    if (filter === 'all' || category === filter) {
                        card.classList.remove('hide');
                        setTimeout(() => {
                            card.style.display = 'block';
                        }, 100);
                    } else {
                        card.classList.add('hide');
                        setTimeout(() => {
                            card.style.display = 'none';
                        }, 300);
                    }
                });
            });
        });
    },

    // Contact form handling
    setupContactForm: function() {
        let contactForm = document.getElementById('contact-form');
        
        if (contactForm) {
            contactForm.addEventListener('submit', function(e) {
                e.preventDefault();
                
                let formData = new FormData(this);
                let data = Object.fromEntries(formData);
                
                // Form validation
                if (!data.name || !data.email || !data.subject || !data.message) {
                    portfolioApp.showNotification('Barcha maydonlarni to\'ldiring!', 'error');
                    return;
                }
                
                // Email validation
                let emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
                if (!emailRegex.test(data.email)) {
                    portfolioApp.showNotification('Noto\'g\'ri email manzil!', 'error');
                    return;
                }
                
                // Save message to localStorage
                let messages = JSON.parse(localStorage.getItem('contactMessages') || '[]');
                messages.push({
                    ...data,
                    timestamp: new Date().toISOString(),
                    read: false
                });
                localStorage.setItem('contactMessages', JSON.stringify(messages));
                
                // Show success message
                portfolioApp.showNotification('Xabaringiz yuborildi! Tez orada javob beramiz.', 'success');
                
                // Reset form
                this.reset();
            });
        }
    },

    // Skill bars animation
    setupSkillBars: function() {
        let skillBars = document.querySelectorAll('.skill-progress');
        
        let animateSkillBars = () => {
            skillBars.forEach(bar => {
                let rect = bar.getBoundingClientRect();
                let windowHeight = window.innerHeight;
                
                if (rect.top < windowHeight && rect.bottom > 0) {
                    let width = bar.getAttribute('data-width');
                    bar.style.setProperty('--width', width + '%');
                    bar.classList.add('animate');
                }
            });
        };

        // Initial check
        animateSkillBars();
        
        // Check on scroll
        window.addEventListener('scroll', this.throttle(animateSkillBars, 100));
    },

    // Theme toggle
    setupThemeToggle: function() {
        let themeToggle = document.querySelector('.theme-toggle');
        let currentTheme = localStorage.getItem('theme') || 'light';
        
        // Apply saved theme
        document.documentElement.setAttribute('data-theme', currentTheme);
        
        if (themeToggle) {
            themeToggle.addEventListener('click', function() {
                let newTheme = currentTheme === 'light' ? 'dark' : 'light';
                document.documentElement.setAttribute('data-theme', newTheme);
                localStorage.setItem('theme', newTheme);
                currentTheme = newTheme;
                
                // Update toggle button text/icon
                this.textContent = newTheme === 'light' ? '🌙' : '☀️';
            });
            
            // Set initial toggle state
            themeToggle.textContent = currentTheme === 'light' ? '🌙' : '☀️';
        }
    },

    // Animations setup
    setupAnimations: function() {
        // Intersection Observer for animations
        let observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        let observer = new IntersectionObserver(function(entries) {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('animate-in');
                    
                    // Stagger animation for multiple elements
                    if (entry.target.classList.contains('project-card')) {
                        let delay = Array.from(entry.target.parentNode.children).indexOf(entry.target) * 100;
                        entry.target.style.animationDelay = delay + 'ms';
                    }
                }
            });
        }, observerOptions);

        // Observe elements
        document.querySelectorAll('.project-card, .skill-category, .stat').forEach(el => {
            observer.observe(el);
        });

        // Typing effect for hero title
        this.setupTypingEffect();
    },

    // Typing effect
    setupTypingEffect: function() {
        let heroTitle = document.querySelector('.hero-title');
        if (!heroTitle) return;

        let text = heroTitle.textContent;
        let words = text.split(' ');
        let currentWordIndex = 0;
        let currentCharIndex = 0;
        let isDeleting = false;

        function typeWriter() {
            let currentWord = words[currentWordIndex];
            
            if (isDeleting) {
                heroTitle.textContent = words.slice(0, currentWordIndex).join(' ') + 
                    ' ' + currentWord.substring(0, currentCharIndex - 1);
                currentCharIndex--;
            } else {
                heroTitle.textContent = words.slice(0, currentWordIndex).join(' ') + 
                    ' ' + currentWord.substring(0, currentCharIndex + 1);
                currentCharIndex++;
            }

            let typeSpeed = isDeleting ? 50 : 100;

            if (!isDeleting && currentCharIndex === currentWord.length) {
                typeSpeed = 2000;
                isDeleting = true;
            } else if (isDeleting && currentCharIndex === 0) {
                isDeleting = false;
                currentWordIndex = (currentWordIndex + 1) % words.length;
                typeSpeed = 500;
            }

            setTimeout(typeWriter, typeSpeed);
        }

        // Start typing effect after page load
        setTimeout(typeWriter, 1000);
    },

    // Notification system
    showNotification: function(message, type = 'info') {
        let notification = document.createElement('div');
        notification.className = `notification notification-${type}`;
        notification.textContent = message;
        
        // Add styles
        notification.style.cssText = `
            position: fixed;
            top: 20px;
            right: 20px;
            padding: 1rem 2rem;
            border-radius: 8px;
            color: white;
            font-weight: 500;
            z-index: 10000;
            transform: translateX(100%);
            transition: transform 0.3s ease;
            max-width: 300px;
            word-wrap: break-word;
        `;
        
        // Set background color based on type
        let colors = {
            success: '#10b981',
            error: '#ef4444',
            warning: '#f59e0b',
            info: '#3b82f6'
        };
        notification.style.backgroundColor = colors[type] || colors.info;
        
        document.body.appendChild(notification);
        
        // Animate in
        setTimeout(() => {
            notification.style.transform = 'translateX(0)';
        }, 100);
        
        // Remove after 5 seconds
        setTimeout(() => {
            notification.style.transform = 'translateX(100%)';
            setTimeout(() => {
                document.body.removeChild(notification);
            }, 300);
        }, 5000);
    },

    // Utility functions
    debounce: function(func, wait) {
        let timeout;
        return function executedFunction(...args) {
            const later = () => {
                clearTimeout(timeout);
                func(...args);
            };
            clearTimeout(timeout);
            timeout = setTimeout(later, wait);
        };
    },

    throttle: function(func, limit) {
        let inThrottle;
        return function() {
            const args = arguments;
            const context = this;
            if (!inThrottle) {
                func.apply(context, args);
                inThrottle = true;
                setTimeout(() => inThrottle = false, limit);
            }
        };
    },

    // Portfolio statistics
    updateStats: function() {
        let stats = {
            projects: document.querySelectorAll('.project-card').length,
            skills: document.querySelectorAll('.skill-item').length,
            experience: 2, // years
            clients: 5
        };

        // Update stat elements if they exist
        document.querySelectorAll('.stat h3').forEach((stat, index) => {
            let values = [stats.experience + '+', stats.projects, stats.skills];
            if (values[index]) {
                stat.textContent = values[index];
            }
        });
    },

    // Load saved data
    loadSavedData: function() {
        // Load contact messages
        let messages = JSON.parse(localStorage.getItem('contactMessages') || '[]');
        console.log('Saved messages:', messages);

        // Load theme
        let theme = localStorage.getItem('theme') || 'light';
        document.documentElement.setAttribute('data-theme', theme);

        // Load portfolio settings
        let settings = JSON.parse(localStorage.getItem('portfolioSettings') || '{}');
        this.applySettings(settings);
    },

    // Apply portfolio settings
    applySettings: function(settings) {
        // Apply theme
        if (settings.theme) {
            document.documentElement.setAttribute('data-theme', settings.theme);
        }

        // Apply language
        if (settings.language) {
            document.documentElement.lang = settings.language;
        }

        // Apply other settings
        if (settings.showProjects !== undefined) {
            let projectsSection = document.getElementById('projects');
            if (projectsSection) {
                projectsSection.style.display = settings.showProjects ? 'block' : 'none';
            }
        }
    }
};

// Initialize app when DOM is loaded
document.addEventListener('DOMContentLoaded', function() {
    portfolioApp.init();
    portfolioApp.loadSavedData();
    portfolioApp.updateStats();
});

// Handle page visibility change
document.addEventListener('visibilitychange', function() {
    if (!document.hidden) {
        // Page became visible, refresh animations
        portfolioApp.setupSkillBars();
    }
});

// Handle window resize
window.addEventListener('resize', portfolioApp.debounce(function() {
    // Recalculate animations and layouts
    portfolioApp.setupSkillBars();
}, 250));
```

### JavaScript funksionallik turlari

#### 1. Navigation va Scroll
- Smooth scrolling
- Active link highlighting
- Mobile menu toggle
- Header background change

#### 2. Animatsiyalar
- Intersection Observer
- Skill bars animation
- Typing effect
- Staggered animations

#### 3. Interaktivlik
- Project filtering
- Contact form handling
- Theme toggle
- Notification system

#### 4. Ma'lumot saqlash
- LocalStorage integration
- Form data persistence
- Settings management
- Message history

### JavaScript afzalliklari

#### 1. Performance
- Debouncing va throttling
- Efficient event handling
- Optimized animations
- Lazy loading

#### 2. User Experience
- Smooth interactions
- Visual feedback
- Responsive design
- Accessibility support

#### 3. Code Organization
- Modular structure
- Reusable functions
- Event delegation
- Error handling

#### 4. Browser Compatibility
- Modern JavaScript features
- Fallback support
- Cross-browser testing
- Progressive enhancement

### JavaScript maslahatlari

#### 1. Code Structure
- Modular approach
- Clear naming
- Comment qo'shing
- Error handling

#### 2. Performance
- Debounce/throttle ishlating
- Efficient selectors
- Minimal DOM manipulation
- Event delegation

#### 3. User Experience
- Smooth animations
- Visual feedback
- Responsive interactions
- Accessibility

#### 4. Maintenance
- Clean code
- Documentation
- Testing
- Version control

</details>

<details>
    <summary>Responsive design</summary>

## 15.6 Responsive Design

### Responsive design nima?

**Responsive design** - veb-saytning turli qurilmalarda (kompyuter, planshet, telefon) bir xil yaxshi ko'rinishi va ishlashi uchun moslashuvchan dizayn. Bu foydalanuvchi tajribasini yaxshilaydi va SEO uchun muhim.

### Responsive design tamoyillari

#### 1. Mobile-first yondashuv
- Avval mobil qurilmalar uchun dizayn qilish
- Keyin katta ekranlar uchun kengaytirish
- Progressiv enhancement

#### 2. Flexible grid
- CSS Grid va Flexbox
- Relative units (%, em, rem, vw, vh)
- Flexible layouts

#### 3. Media queries
- Ekran o'lchamiga qarab stil o'zgartirish
- Breakpoint larni aniqlash
- Responsive typography

### Responsive CSS (responsive.css)
```css
/* Responsive Design Styles */

/* Extra Large Devices (1400px and up) */
@media (min-width: 1400px) {
    .container {
        max-width: 1320px;
    }
    
    .hero-title {
        font-size: 4rem;
    }
    
    .hero-subtitle {
        font-size: 1.75rem;
    }
}

/* Large Devices (1200px and up) */
@media (min-width: 1200px) {
    .container {
        max-width: 1140px;
    }
    
    .hero-content {
        gap: 5rem;
    }
    
    .projects-grid {
        grid-template-columns: repeat(3, 1fr);
    }
}

/* Medium Devices (992px and up) */
@media (min-width: 992px) {
    .container {
        max-width: 960px;
    }
    
    .hero-title {
        font-size: 3.5rem;
    }
    
    .nav-menu {
        display: flex;
    }
    
    .nav-toggle {
        display: none;
    }
    
    .about-content {
        grid-template-columns: 1fr 1fr;
    }
    
    .contact-content {
        grid-template-columns: 1fr 1fr;
    }
}

/* Small Devices (768px and up) */
@media (min-width: 768px) {
    .container {
        max-width: 720px;
    }
    
    .hero-title {
        font-size: 3rem;
    }
    
    .hero-content {
        grid-template-columns: 1fr 1fr;
        gap: 3rem;
    }
    
    .skills-grid {
        grid-template-columns: repeat(2, 1fr);
    }
    
    .projects-grid {
        grid-template-columns: repeat(2, 1fr);
    }
    
    .about-stats {
        grid-template-columns: repeat(3, 1fr);
    }
}

/* Extra Small Devices (576px and up) */
@media (min-width: 576px) {
    .container {
        max-width: 540px;
    }
    
    .hero-title {
        font-size: 2.5rem;
    }
    
    .section-title {
        font-size: 2rem;
    }
    
    .project-card {
        max-width: 400px;
        margin: 0 auto;
    }
}

/* Mobile Devices (up to 575px) */
@media (max-width: 575px) {
    .container {
        padding: 0 0.75rem;
    }
    
    /* Typography */
    h1 { font-size: 2rem; }
    h2 { font-size: 1.75rem; }
    h3 { font-size: 1.5rem; }
    
    .hero-title {
        font-size: 2rem;
        line-height: 1.2;
    }
    
    .hero-subtitle {
        font-size: 1.2rem;
    }
    
    .hero-description {
        font-size: 1rem;
    }
    
    /* Navigation */
    .nav-menu {
        position: fixed;
        top: 70px;
        left: -100%;
        width: 100%;
        height: calc(100vh - 70px);
        background: rgba(255, 255, 255, 0.98);
        backdrop-filter: blur(10px);
        flex-direction: column;
        justify-content: flex-start;
        align-items: center;
        padding-top: 2rem;
        transition: left 0.3s ease;
        z-index: 999;
    }
    
    .nav-menu.active {
        left: 0;
    }
    
    .nav-item {
        margin: 1rem 0;
    }
    
    .nav-link {
        font-size: 1.2rem;
        padding: 1rem 2rem;
    }
    
    .nav-toggle {
        display: flex;
    }
    
    .nav-toggle.active .bar:nth-child(1) {
        transform: rotate(45deg) translate(5px, 5px);
    }
    
    .nav-toggle.active .bar:nth-child(2) {
        opacity: 0;
    }
    
    .nav-toggle.active .bar:nth-child(3) {
        transform: rotate(-45deg) translate(7px, -6px);
    }
    
    /* Hero Section */
    .hero {
        min-height: 100vh;
        padding: 2rem 0;
    }
    
    .hero-content {
        grid-template-columns: 1fr;
        gap: 2rem;
        text-align: center;
    }
    
    .hero-image {
        order: -1;
    }
    
    .profile-img {
        width: 200px;
        height: 200px;
    }
    
    .hero-buttons {
        flex-direction: column;
        gap: 1rem;
    }
    
    .btn {
        width: 100%;
        text-align: center;
    }
    
    /* Sections */
    section {
        padding: 3rem 0;
    }
    
    .section-title {
        font-size: 1.75rem;
        margin-bottom: 2rem;
    }
    
    /* About Section */
    .about-content {
        grid-template-columns: 1fr;
        gap: 2rem;
        text-align: center;
    }
    
    .about-stats {
        grid-template-columns: 1fr;
        gap: 1rem;
    }
    
    .stat {
        padding: 1rem;
    }
    
    .stat h3 {
        font-size: 2rem;
    }
    
    /* Skills Section */
    .skills-grid {
        grid-template-columns: 1fr;
        gap: 2rem;
    }
    
    .skill-category {
        padding: 1.5rem;
    }
    
    /* Projects Section */
    .projects-grid {
        grid-template-columns: 1fr;
        gap: 1.5rem;
    }
    
    .projects-filter {
        flex-direction: column;
        gap: 0.5rem;
    }
    
    .filter-btn {
        width: 100%;
        text-align: center;
    }
    
    .project-card {
        margin: 0;
    }
    
    .project-image {
        height: 200px;
    }
    
    .project-content {
        padding: 1rem;
    }
    
    .project-tech {
        justify-content: center;
    }
    
    /* Contact Section */
    .contact-content {
        grid-template-columns: 1fr;
        gap: 2rem;
    }
    
    .contact-form {
        padding: 1.5rem;
    }
    
    .contact-details {
        text-align: center;
    }
    
    .contact-item {
        justify-content: center;
        text-align: center;
    }
    
    .social-links {
        justify-content: center;
    }
    
    /* Footer */
    .footer-content {
        flex-direction: column;
        text-align: center;
        gap: 1rem;
    }
    
    .footer-links {
        flex-direction: column;
        gap: 1rem;
    }
    
    /* Utility Classes */
    .text-center {
        text-align: center;
    }
    
    .text-left {
        text-align: left;
    }
    
    .text-right {
        text-align: right;
    }
    
    .d-none {
        display: none;
    }
    
    .d-block {
        display: block;
    }
    
    .d-flex {
        display: flex;
    }
    
    .flex-column {
        flex-direction: column;
    }
    
    .flex-center {
        justify-content: center;
        align-items: center;
    }
    
    .w-100 {
        width: 100%;
    }
    
    .h-100 {
        height: 100%;
    }
}

/* Landscape Mobile Devices */
@media (max-width: 767px) and (orientation: landscape) {
    .hero {
        min-height: 100vh;
        padding: 1rem 0;
    }
    
    .hero-content {
        gap: 1rem;
    }
    
    .profile-img {
        width: 150px;
        height: 150px;
    }
    
    section {
        padding: 2rem 0;
    }
    
    .nav-menu {
        height: calc(100vh - 60px);
    }
}

/* Print Styles */
@media print {
    * {
        background: transparent !important;
        color: black !important;
        box-shadow: none !important;
        text-shadow: none !important;
    }
    
    body {
        font-size: 12pt;
        line-height: 1.4;
    }
    
    h1, h2, h3, h4, h5, h6 {
        page-break-after: avoid;
    }
    
    .nav-menu,
    .hero-buttons,
    .contact-form,
    .social-links {
        display: none;
    }
    
    .hero {
        min-height: auto;
        padding: 1rem 0;
    }
    
    section {
        padding: 1rem 0;
        page-break-inside: avoid;
    }
    
    .project-card {
        page-break-inside: avoid;
        margin-bottom: 1rem;
    }
}

/* High DPI Displays */
@media (-webkit-min-device-pixel-ratio: 2), (min-resolution: 192dpi) {
    .profile-img,
    .about-img,
    .project-image img {
        image-rendering: -webkit-optimize-contrast;
        image-rendering: crisp-edges;
    }
}

/* Reduced Motion */
@media (prefers-reduced-motion: reduce) {
    *,
    *::before,
    *::after {
        animation-duration: 0.01ms !important;
        animation-iteration-count: 1 !important;
        transition-duration: 0.01ms !important;
        scroll-behavior: auto !important;
    }
    
    .hero-title,
    .hero-subtitle,
    .hero-description,
    .hero-buttons,
    .hero-image {
        animation: none !important;
    }
    
    .skill-progress {
        transition: none !important;
    }
}

/* Dark Mode Support */
@media (prefers-color-scheme: dark) {
    :root {
        --text-color: #fff;
        --text-light: #ccc;
        --bg-color: #1a1a1a;
        --bg-light: #2d2d2d;
        --border-color: #404040;
    }
    
    header {
        background: rgba(26, 26, 26, 0.95);
        border-bottom-color: var(--border-color);
    }
    
    .nav-menu {
        background: rgba(26, 26, 26, 0.98);
    }
}

/* Focus Styles for Accessibility */
@media (prefers-reduced-motion: no-preference) {
    .nav-link:focus,
    .btn:focus,
    .filter-btn:focus,
    input:focus,
    textarea:focus {
        outline: 2px solid var(--primary-color);
        outline-offset: 2px;
    }
}

/* Hover Effects for Touch Devices */
@media (hover: none) {
    .project-card:hover,
    .stat:hover,
    .skill-category:hover,
    .btn:hover {
        transform: none;
        box-shadow: var(--shadow);
    }
    
    .nav-link:hover {
        background-color: transparent;
    }
    
    .filter-btn:hover {
        background: transparent;
        color: var(--primary-color);
    }
}
```

### Responsive design afzalliklari

#### 1. User Experience
- Barcha qurilmalarda yaxshi ko'rinish
- Tez yuklanish
- Oson navigatsiya
- Touch-friendly interfeys

#### 2. SEO Benefits
- Google mobile-first indexing
- Better search rankings
- Lower bounce rate
- Higher user engagement

#### 3. Maintenance
- Bitta kod bazasi
- Oson yangilash
- Kamroq hosting xarajatlari
- Unified analytics

#### 4. Performance
- Optimized images
- Efficient CSS
- Minimal JavaScript
- Fast loading

### Responsive design maslahatlari

#### 1. Planning
- Mobile-first approach
- Breakpoint strategiyasi
- Content prioritization
- Performance planning

#### 2. Implementation
- Flexible grid systems
- Responsive images
- Touch-friendly buttons
- Readable typography

#### 3. Testing
- Multiple devices
- Different browsers
- Network conditions
- User testing

#### 4. Optimization
- Image optimization
- CSS minification
- JavaScript optimization
- Performance monitoring

</details>
