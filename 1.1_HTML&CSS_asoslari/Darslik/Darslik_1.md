<details>
    <summary>Web-saytlar nima va qanday ishlaydi?</summary>
# MODUL 1: Web-saytlar Dunyosiga Kirish

## 1.1 Web-saytlar nima va qanday ishlaydi?

### Web-sayt nima?

Web-sayt (Website) - bu internetda joylashgan bir nechta bog'langan sahifalar to'plamidir. Masalan, Google, YouTube, Wikipedia - bularning barchasi web-saytlardir.

**Oddiy misol bilan tushuntiramiz:**
- Web-sayt xuddi kitobga o'xshaydi
- Har bir sahifa (webpage) - kitobning bir varaqiga o'xshaydi  
- Sahifalar orasida havolalar (links) bor - bu xuddi kitobdagi mundarijaga o'xshaydi

### Web-saytlar qanday ishlaydi?

Web-saytlar maxsus kompyuterlar - **server**larda saqlanadi. Biz o'z kompyuterimizdan internet orqali shu serverlarga murojaat qilamiz.

**Bu jarayon quyidagicha ishlaydi:**

1. **Siz manzil kiritasiz** - masalan: www.google.com
2. **Sizning kompyuteringiz so'rov yuboradi** - "Google sahifasini ko'rsating"
3. **Server javob beradi** - Google sahifasini yuboradi
4. **Brauzer sahifani ko'rsatadi** - siz sahifani ko'rasiz

```
Sizning kompyuter → Internet → Server → Web-sahifa → Brauzer → Siz ko'rasiz
```

### Web-saytlar nimalardan iborat?

Har bir web-sahifa asosan uchta qismdan iborat:

1. **Matn va rasm** - siz ko'radigan ma'lumotlar
2. **Dizayn va ranglar** - sahifaning chiroyli ko'rinishi  
3. **Interaktivlik** - tugmalar, formalar, animatsiyalar

---

## 1.2 Brauzer va Web-sahifalar

### Brauzer (Browser) nima?

**Brauzer** - bu web-sahifalarni ko'rish uchun maxsus dastur. Bu sizning internet oynangizdir.

**Mashhur brauzerlar:**
- **Google Chrome** 🌐
- **Safari** 🦁 (Apple kompyuterlarda)
- **Firefox** 🦊
- **Microsoft Edge** 🔷

### Brauzer qanday ishlaydi?

Brauzer - bu tarjimon kabi. U web-sahifaning kodini olib, uni siz tushuna oladigan ko'rinishga aylantiradi.

**Misol:**
```
Kod: <h1>Salom Dunyo!</h1>
Brauzer ko'rsatadi: SALOM DUNYO! (katta harflar bilan)
```

### Web-sahifa nima?

**Web-sahifa** - bu internet orqali ko'riladigan bitta hujjat. Har bir sahifada turli ma'lumotlar bo'lishi mumkin:

- **Matn** - maqolalar, yangiliklar
- **Rasmlar** - fotosuratlar, chizmalar  
- **Video** - filmlar, darsliklar
- **Havolalar** - boshqa sahifalarga o'tish
- **Formalar** - ma'lumot kiritish uchun

### Sahifa manzili (URL)

Har bir web-sahifaning o'z manzili bor - **URL** (Uniform Resource Locator).

**URL qismlari:**
```
https://www.google.com/search?q=dasturlash
│       │     │        │     │
│       │     │        │     └─ Qidiruv so'zi
│       │     │        └─ Sahifa nomi
│       │     └─ Sayt nomi
│       └─ Domen
└─ Protokol (xavfsizlik)
```

---

## 1.3 HTML va CSS nima?

### HTML - Sahifaning Asosi

**HTML** (HyperText Markup Language) - bu web-sahifaning asosiy tuzilishini yaratish tilidir.

**HTML nima qiladi:**
- Matnni tashkil etadi
- Sarlavhalar yaratadi
- Ro'yxatlar qo'shadi
- Rasmlar joylashtiradi
- Havolalar qo'yadi

**HTML - bu xuddi uy qurish kabi:**
- HTML = Uyning asosi, devorlari, eshik-derazalar
- CSS = Uyni bo'yash, bezatish, mebel qo'yish

### HTML Tag'lari

HTML **tag**'lar (belgilar) yordamida ishlaydi. Tag'lar `< >` ichida yoziladi.

**Asosiy tag'lar:**
```html
<h1>Katta sarlavha</h1>
<p>Oddiy matn paragraf</p>
<img>Rasm qo'yish uchun</img>
<a>Havola yaratish uchun</a>
```

### CSS - Chiroyli Dizayn

**CSS** (Cascading Style Sheets) - bu web-sahifani chiroyli qilish tilidir.

**CSS nima qiladi:**
- Ranglarni o'zgartiradi
- Shriftlarni tanlaydi  
- Elementlarni joylashtirishadi
- Animatsiya qo'shadi
- Responsive (moslashuvchan) qiladi

**CSS misoli:**
```css
h1 {
    color: blue;        /* Matn rangi ko'k */
    font-size: 24px;    /* Matn o'lchami */
    text-align: center; /* Markazga joylashtirish */
}
```

### HTML va CSS qanday birga ishlaydi?

1. **HTML** sahifaning skeletini yaratadi
2. **CSS** bu skeletni go'zal libos bilan bezatadi

**Misol:**
```html
<!-- HTML: Tuzilish -->
<h1>Mening Web-saytim</h1>
<p>Bu mening birinchi sahifam!</p>

<!-- CSS: Dizayn -->
<style>
h1 { color: red; }
p { color: green; }
</style>
```

**Natija:** "Mening Web-saytim" qizil rangda, "Bu mening birinchi sahifam!" yashil rangda ko'rinadi.

---

## 1.4 Birinchi Web-sahifani Yaratish

### Kerakli Asboblar

Birinchi web-sahifangizni yaratish uchun faqat ikki narsa kerak:
1. **Matn muharriri** (Text Editor) - Visual Studio Code tavsiya etiladi
2. **Brauzer** - Chrome, Safari, Firefox

### 1-qadam: Fayl yaratish

1. Kompyuteringizda yangi papka yarating: `Mening_Web_Saytim`
2. Bu papkada yangi fayl yarating: `index.html`
3. `.html` oxiri muhim - bu brauzerga bu web-sahifa ekanligini ko'rsatadi

### 2-qadam: Asosiy HTML yozish

`index.html` faylini oching va quyidagi kodni yozing:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Mening Birinchi Sahifam</title>
</head>
<body>
    <h1>Salom Dunyo!</h1>
    <p>Bu mening birinchi web-sahifam.</p>
</body>
</html>
```

### 3-qadam: Sahifani ochish

1. `index.html` faylni ikki marta bosing
2. U brauzerda ochiladi
3. Tabriklaymiz! Siz birinchi web-sahifangizni yaratdingiz! 🎉

### Kod tushuntirish

Keling, yozgan kodimizni qatorma-qator tushuntiramiz:

```html
<!DOCTYPE html>
```
- Bu brauzerga "Bu HTML5 sahifa" deydi

```html
<html>
</html>
```
- Butun sahifani o'rab oladi
- Barcha boshqa kodlar shu ichida yoziladi

```html
<head>
</head>
```
- Sahifa haqidagi ma'lumotlar
- Foydalanuvchi ko'rmaydi

```html
<title>Mening Birinchi Sahifam</title>
```
- Brauzer tab'ida ko'rinadigan nom

```html
<body>
</body>
```
- Sahifaning asosiy qismi
- Foydalanuvchi ko'radigan barcha narsalar shu yerda

```html
<h1>Salom Dunyo!</h1>
```
- Eng katta sarlavha
- Avtomatik qalin va katta harflar

```html
<p>Bu mening birinchi web-sahifam.</p>
```
- Oddiy paragraf
- Normal o'lchamdagi matn

---

## 1.5 Oddiy HTML Struktura

### To'liq HTML struktura

Har bir web-sahifa quyidagi asosiy strukturaga ega:

```html
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sahifa Nomi</title>
</head>
<body>
    <!-- Bu yerda sahifaning ko'rinadigan qismi -->
</body>
</html>
```

### DOCTYPE nima?

```html
<!DOCTYPE html>
```
- Bu brauzerga qaysi HTML versiyasi ishlatilayotganini aytadi
- HTML5 uchun eng oddiy va zamonaviy usul
- Har doim HTML hujjatning eng boshida yoziladi

### HTML tegi

```html
<html lang="uz">
```
- Butun HTML hujjatni o'rab oladi
- `lang="uz"` - sahifa tilini ko'rsatadi (o'zbek tili)
- Bu qism brauzer va qidiruv tizimlari uchun muhim

### Head qismida nima bo'ladi?

```html
<head>
    <meta charset="UTF-8">
    <!-- O'zbek harflarini to'g'ri ko'rsatish uchun -->
    
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- Mobil telefonlarda to'g'ri ko'rinish uchun -->
    
    <title>Sahifa Nomi</title>
    <!-- Brauzer tepasida ko'rinadigan nom -->
</head>
```

**Head qismidagi asosiy elementlar:**

- **meta charset** - matn kodlashini belgilaydi
- **meta viewport** - mobil qurilmalarda to'g'ri ko'rinish uchun
- **title** - sahifa sarlavhasi (brauzer tab'ida ko'rinadi)

### Body qismida nima bo'ladi?

```html
<body>
    <h1>Asosiy Sarlavha</h1>        <!-- Eng muhim sarlavha -->
    <h2>Ikkinchi darajali sarlavha</h2>  <!-- Kichikroq sarlavha -->
    
    <p>Bu oddiy paragraf.</p>       <!-- Matn paragraf -->
    
    <p>Bu yana bir paragraf.</p>    <!-- Yana bir paragraf -->
</body>
```

**Body qismida:**
- Foydalanuvchi ko'radigan barcha ma'lumotlar
- Matn, rasmlar, havolalar, formalar
- Sahifaning asosiy mazmuni

### HTML Kommentariyalar

```html
<!-- Bu kommentariya - brauzer ko'rsatmaydi -->
<h1>Bu ko'rinadigan sarlavha</h1>
<!-- Kommentariyalar kodni tushuntirish uchun ishlatiladi -->
```

---

## 1.6 Matn va Sarlavhalar

### Sarlavha darajalari

HTML da 6 xil sarlavha darajasi bor:

```html
<h1>1-daraja sarlavha - eng katta</h1>
<h2>2-daraja sarlavha</h2>
<h3>3-daraja sarlavha</h3>
<h4>4-daraja sarlavha</h4>
<h5>5-daraja sarlavha</h5>
<h6>6-daraja sarlavha - eng kichik</h6>
```

### Sarlavhalar qanday ishlatiladi?

**Ierarxiya (tartib) muhim:**

```html
<h1>Kitob nomi</h1>
    <h2>1-bob</h2>
        <h3>1.1 qism</h3>
        <h3>1.2 qism</h3>
    <h2>2-bob</h2>
        <h3>2.1 qism</h3>
```

**Amaliy misol:**
```html
<h1>Futbol haqida</h1>
<h2>Futbol qoidalari</h2>
<h3>O'yinchilar soni</h3>
<h3>O'yin vaqti</h3>
<h2>Futbol tarixi</h2>
<h3>Futbolning paydo bo'lishi</h3>
<h3>Dunyodagi rivojlanishi</h3>
```

### Paragraflar

Matnni paragraflarga bo'lish uchun `<p>` tag'idan foydalanamiz:

```html
<p>Bu birinchi paragraf. Bu yerda biror mavzu haqida gapirish mumkin.</p>

<p>Bu ikkinchi paragraf. Paragraflar orasida avtomatik ravishda bo'sh joy qoladi.</p>

<p>Bu uchinchi paragraf.</p>
```

**Paragraf xususiyatlari:**
- Har bir paragraf yangi qatordan boshlanadi
- Paragraflar orasida avtomatik bo'shliq bor
- Uzun matnni o'qishni osonlashtiradi

### Matnni formatlash

HTML da matnni turlicha formatlash mumkin:

```html
<p>Bu <strong>muhim matn</strong> (qalin harflar)</p>
<p>Bu <em>ta'kidlangan matn</em> (qiyshiq harflar)</p>
<p>Bu <u>chizilgan matn</u> (chiziq bilan)</p>
<p>Bu <mark>belgilangan matn</mark> (sariq fon bilan)</p>
<p>Bu <small>kichik matn</small></p>
```

### Maxsus belgilar

```html
<p>Qator uzilishi uchun<br>br tag ishlatiladi</p>
<p>Gorizontal chiziq uchun:</p>
<hr>
<p>Yuqorida chiziq ko'rdingiz</p>
```

### Matn bloki

```html
<blockquote>
Bu uzun iqtibos yoki muhim matn bloki. 
Odatda chetdan surilgan ko'rinishda chiqadi.
</blockquote>
```

---

## 1.7 CSS bilan Ranglar Qo'shish

### CSS qanday ulanadi?

CSS ni HTML ga ulashning 3 yo'li bor:

#### 1-usul: Ichki CSS (Internal CSS)
```html
<head>
    <style>
        h1 { color: red; }
        p { color: blue; }
    </style>
</head>
```

#### 2-usul: Inline CSS
```html
<h1 style="color: red;">Qizil sarlavha</h1>
<p style="color: blue;">Ko'k matn</p>
```

#### 3-usul: Tashqi CSS (External CSS)
```html
<head>
    <link rel="stylesheet" href="style.css">
</head>
```

### Ranglar bilan ishlash

#### Rang nomlari (asosiy ranglar)
```css
h1 { color: red; }      /* qizil */
h2 { color: blue; }     /* ko'k */
h3 { color: green; }    /* yashil */
p { color: purple; }    /* binafsha */
```

**Boshqa rang nomlari:**
- `black` - qora
- `white` - oq  
- `gray` - kulrang
- `orange` - to'q sariq
- `pink` - pushti
- `brown` - jigarrang

#### Hex kodlar
```css
h1 { color: #FF0000; }  /* qizil */
h2 { color: #0000FF; }  /* ko'k */
h3 { color: #00FF00; }  /* yashil */
h4 { color: #FFFF00; }  /* sariq */
```

#### RGB ranglar
```css
h1 { color: rgb(255, 0, 0); }    /* qizil */
h2 { color: rgb(0, 0, 255); }    /* ko'k */
h3 { color: rgb(0, 255, 0); }    /* yashil */
h4 { color: rgb(255, 255, 0); }  /* sariq */
```

### Fon rangi (Background)

```css
body { 
    background-color: lightblue; 
}

h1 { 
    background-color: yellow; 
    color: black;
}

p {
    background-color: lightgray;
    color: darkblue;
}
```

### CSS Selektorlari

**Tag selektori:**
```css
h1 { color: red; }      /* Barcha h1 teglar */
p { color: blue; }      /* Barcha p teglar */
```

**Class selektori:**
```html
<p class="muhim">Bu muhim paragraf</p>
```
```css
.muhim { 
    color: red; 
    font-weight: bold;
}
```

**ID selektori:**
```html
<h1 id="sarlavha">Asosiy sarlavha</h1>
```
```css
#sarlavha { 
    color: green; 
    text-align: center;
}
```

### Matn xususiyatlari

```css
h1 {
    color: blue;              /* Matn rangi */
    font-size: 24px;          /* Matn o'lchami */
    text-align: center;       /* Markazga joylashtirish */
    font-weight: bold;        /* Qalin harflar */
    text-decoration: underline; /* Chiziq */
}

p {
    color: gray;
    font-size: 16px;
    text-align: left;         /* Chapga joylashtirish */
    line-height: 1.5;         /* Qatorlar orasidagi masofa */
}
```

### To'liq misol

```html
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <title>Rangli Sahifa</title>
    <style>
        body {
            background-color: lightcyan;
            font-family: Arial, sans-serif;
        }
        
        h1 {
            color: darkblue;
            text-align: center;
            background-color: lightyellow;
        }
        
        h2 {
            color: green;
            text-decoration: underline;
        }
        
        p {
            color: darkslategray;
            font-size: 16px;
            line-height: 1.6;
        }
        
        .muhim {
            color: red;
            font-weight: bold;
            background-color: yellow;
        }
    </style>
</head>
<body>
    <h1>Mening Rangli Sahifam</h1>
    
    <h2>Ranglar haqida</h2>
    <p>Bu sahifada turli ranglar ishlatilgan.</p>
    
    <p class="muhim">Bu juda muhim ma'lumot!</p>
    
    <h2>CSS haqida</h2>
    <p>CSS yordamida web-sahifalarni chiroyli qilish mumkin.</p>
</body>
</html>
```

</details>

<details>
    <summary>HTML teglari va ularning vazifasi</summary>

## 2.1 HTML Teglari va Ularning Vazifasi

### Tag nima?

**Tag** - bu HTML da elementlarni belgilash uchun ishlatiladigan maxsus belgilardir. Taglar `< >` qavslar ichida yoziladi.

**Tag tuzilishi:**
```html
<tag_nomi>Mazmun</tag_nomi>
```

### Asosiy HTML teglari

#### Matn teglari
```html
<h1>Eng katta sarlavha</h1>
<h2>Ikkinchi daraja sarlavha</h2>
<h3>Uchinchi daraja sarlavha</h3>
<h4>To'rtinchi daraja sarlavha</h4>
<h5>Beshinchi daraja sarlavha</h5>
<h6>Eng kichik sarlavha</h6>

<p>Paragraf matni</p>
```

#### Struktura teglari
```html
<!DOCTYPE html>    <!-- HTML5 hujjat turi -->
<html>             <!-- Asosiy konteyner -->
<head>             <!-- Sahifa haqida ma'lumot -->
<body>             <!-- Ko'rinadigan mazmun -->
<title>           <!-- Sahifa sarlavhasi -->
<meta>            <!-- Qo'shimcha ma'lumotlar -->
```

#### Matn formatlash teglari
```html
<strong>Qalin matn</strong>
<em>Qiyshiq matn</em>
<u>Chizilgan matn</u>
<mark>Belgilangan matn</mark>
<small>Kichik matn</small>
<big>Katta matn</big>
```

#### Maxsus tegler
```html
<br>              <!-- Qator uzilishi -->
<hr>              <!-- Gorizontal chiziq -->
<!-- komment -->  <!-- Kommentariya -->
```

### Teglarning turlari

#### 1. Konteyner teglar (ochiladi va yopiladi)
```html
<h1>Bu sarlavha</h1>
<p>Bu paragraf</p>
<strong>Bu qalin matn</strong>
```

#### 2. Bo'sh teglar (faqat ochiladi)
```html
<br>     <!-- Qator uzilishi -->
<hr>     <!-- Gorizontal chiziq -->
<img>    <!-- Rasm -->
<meta>   <!-- Meta ma'lumot -->
```

#### 3. Blok elementlar (yangi qatordan boshlanadi)
```html
<h1>Sarlavha</h1>
<p>Paragraf</p>
<div>Blok konteyner</div>
```

#### 4. Inline elementlar (bir qatorda davom etadi)
```html
Bu matnda <strong>qalin</strong> va <em>qiyshiq</em> so'zlar bor.
```

### Tag atributlari

Teglar qo'shimcha ma'lumotlar - **atributlar**ga ega bo'lishi mumkin:

```html
<p id="birinchi" class="muhim">Bu atributli paragraf</p>
<img src="rasm.jpg" alt="Rasm tavsifi">
<a href="https://google.com">Google havolasi</a>
```

**Asosiy atributlar:**
- `id` - yagona identifikator
- `class` - CSS uchun sinf
- `src` - rasm manbai
- `href` - havola manzili
- `alt` - muqobil matn

### Amaliy misol

```html
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <title>HTML Teglari Namunasi</title>
</head>
<body>
    <h1>Mening Sahifam</h1>
    <h2>HTML haqida</h2>
    
    <p>Bu oddiy paragraf. <strong>Bu qalin matn</strong> va 
    <em>bu qiyshiq matn</em>.</p>
    
    <hr>
    
    <p>Yangi paragraf<br>yangi qatordan davom etadi.</p>
    
    <!-- Bu kommentariya -->
    <p><mark>Belgilangan matn</mark> va <small>kichik matn</small>.</p>
</body>
</html>
```

</details>

<details>
    <summary>Matn formatlash (bold, italic, underline)</summary>

## 2.2 Matn Formatlash (Bold, Italic, Underline)

### Asosiy matn formatlash teglari

#### Qalin matn (Bold)

**1-usul: `<strong>` tegi (tavsiya etiladi)**
```html
<p>Bu <strong>juda muhim</strong> ma'lumot.</p>
```

**2-usul: `<b>` tegi**
```html
<p>Bu <b>qalin</b> matn.</p>
```

**Farqi:**
- `<strong>` - mazmuniy jihatdan muhim
- `<b>` - faqat vizual jihatdan qalin

#### Qiyshiq matn (Italic)

**1-usul: `<em>` tegi (tavsiya etiladi)**
```html
<p>Bu <em>ta'kidlangan</em> so'z.</p>
```

**2-usul: `<i>` tegi**
```html
<p>Bu <i>qiyshiq</i> matn.</p>
```

**Farqi:**
- `<em>` - ta'kidlash uchun
- `<i>` - faqat vizual jihatdan qiyshiq

#### Chizilgan matn (Underline)

```html
<p>Bu <u>chizilgan</u> matn.</p>
```

### Qo'shimcha formatlash teglari

#### Belgilangan matn
```html
<p>Bu <mark>sariq fon bilan belgilangan</mark> matn.</p>
```

#### Kichik va katta matn
```html
<p>Oddiy matn, <small>kichik matn</small> va <big>katta matn</big>.</p>
```

#### O'chirilgan matn
```html
<p>Bu <del>o'chirilgan</del> va bu <ins>qo'shilgan</ins> matn.</p>
```

#### Yuqori va pastki indeks
```html
<p>H<sub>2</sub>O - suv formulasi</p>
<p>E = mc<sup>2</sup> - Eynshteyn formulasi</p>
```

### Formatlash kombinatsiyasi

Bir nechta formatni birlashtirish mumkin:

```html
<p>Bu <strong><em>qalin va qiyshiq</em></strong> matn.</p>
<p>Bu <u><strong>chizilgan va qalin</strong></u> matn.</p>
<p>Bu <mark><em>belgilangan va qiyshiq</em></mark> matn.</p>
```

### CSS bilan formatlash

HTML teglardan tashqari, CSS bilan ham formatlash mumkin:

```html
<style>
.qalin { font-weight: bold; }
.qiyshiq { font-style: italic; }
.chizilgan { text-decoration: underline; }
</style>

<p class="qalin">CSS bilan qalin matn</p>
<p class="qiyshiq">CSS bilan qiyshiq matn</p>
<p class="chizilgan">CSS bilan chizilgan matn</p>
```

### To'liq misol

```html
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <title>Matn Formatlash</title>
</head>
<body>
    <h1>Matn Formatlash Misollar</h1>
    
    <h2>Asosiy formatlar</h2>
    <p>Bu oddiy matn. <strong>Bu muhim matn.</strong> 
    <em>Bu ta'kidlangan matn.</em> <u>Bu chizilgan matn.</u></p>
    
    <h2>Qo'shimcha formatlar</h2>
    <p>Bu <mark>belgilangan matn</mark>. Bu <small>kichik matn</small>.</p>
    
    <h2>Kombinatsiyalar</h2>
    <p><strong><em>Qalin va qiyshiq</em></strong> matn juda 
    <u><strong>ta'sirli</strong></u> ko'rinadi.</p>
    
    <h2>Ilmiy formulalar</h2>
    <p>Suv formulasi: H<sub>2</sub>O</p>
    <p>Eynshteyn formulasi: E = mc<sup>2</sup></p>
    
    <h2>Tahrirlash belgilari</h2>
    <p>Eski narx: <del>50,000 so'm</del></p>
    <p>Yangi narx: <ins>40,000 so'm</ins></p>
</body>
</html>
```

</details>

<details>
    <summary>Ro'yxatlar yaratish (ul, ol, li)</summary>

## 2.3 Ro'yxatlar Yaratish (ul, ol, li)

### Ro'yxat turlari

HTML da ikki asosiy ro'yxat turi bor:
1. **Tartibsiz ro'yxat** (Unordered List) - `<ul>`
2. **Tartiblangan ro'yxat** (Ordered List) - `<ol>`

### Tartibsiz ro'yxat (Unordered List)

Tartibsiz ro'yxatda elementlar nuqtalar bilan belgilanadi:

```html
<ul>
    <li>Birinchi element</li>
    <li>Ikkinchi element</li>
    <li>Uchinchi element</li>
</ul>
```

**Natija:**
- Birinchi element
- Ikkinchi element  
- Uchinchi element

#### Bullet turlari

```html
<ul style="list-style-type: disc;">
    <li>To'ldirilgan doira (disc)</li>
</ul>

<ul style="list-style-type: circle;">
    <li>Bo'sh doira (circle)</li>
</ul>

<ul style="list-style-type: square;">
    <li>Kvadrat (square)</li>
</ul>
```

### Tartiblangan ro'yxat (Ordered List)

Tartiblangan ro'yxatda elementlar raqamlar bilan belgilanadi:

```html
<ol>
    <li>Birinchi qadam</li>
    <li>Ikkinchi qadam</li>
    <li>Uchinchi qadam</li>
</ol>
```

**Natija:**
1. Birinchi qadam
2. Ikkinchi qadam
3. Uchinchi qadam

#### Raqamlash turlari

```html
<ol type="1">
    <li>Oddiy raqamlar (1, 2, 3)</li>
</ol>

<ol type="A">
    <li>Katta harflar (A, B, C)</li>
</ol>

<ol type="a">
    <li>Kichik harflar (a, b, c)</li>
</ol>

<ol type="I">
    <li>Katta rim raqamlari (I, II, III)</li>
</ol>

<ol type="i">
    <li>Kichik rim raqamlari (i, ii, iii)</li>
</ol>
```

#### Boshlanish raqamini o'zgartirish

```html
<ol start="5">
    <li>Beshinchi element</li>
    <li>Oltinchi element</li>
    <li>Yettinchi element</li>
</ol>
```

### Ichma-ich ro'yxatlar (Nested Lists)

Ro'yxatlar ichida boshqa ro'yxatlar yaratish mumkin:

```html
<ul>
    <li>Birinchi daraja
        <ul>
            <li>Ikkinchi daraja 1</li>
            <li>Ikkinchi daraja 2</li>
        </ul>
    </li>
    <li>Birinchi daraja davomi</li>
</ul>
```

#### Murakkab ichma-ich misol

```html
<ol>
    <li>Web dasturlash
        <ul>
            <li>Frontend
                <ol>
                    <li>HTML</li>
                    <li>CSS</li>
                    <li>JavaScript</li>
                </ol>
            </li>
            <li>Backend
                <ul>
                    <li>Python</li>
                    <li>Node.js</li>
                    <li>PHP</li>
                </ul>
            </li>
        </ul>
    </li>
    <li>Mobil dasturlash</li>
</ol>
```

### Tavsifli ro'yxat (Description List)

Atamalar va ularning tavsifini yozish uchun:

```html
<dl>
    <dt>HTML</dt>
    <dd>HyperText Markup Language - web-sahifalar yaratish tili</dd>
    
    <dt>CSS</dt>
    <dd>Cascading Style Sheets - sahifalarni bezatish tili</dd>
    
    <dt>JavaScript</dt>
    <dd>Interaktiv funksiyalar qo'shish tili</dd>
</dl>
```

### CSS bilan ro'yxatlarni bezatish

```html
<style>
.rangli-royxat {
    background-color: lightblue;
    padding: 10px;
}

.rangli-royxat li {
    color: darkblue;
    margin: 5px 0;
}

.maxsus-royxat {
    list-style-type: none; /* Bulletlarni olib tashlash */
}

.maxsus-royxat li::before {
    content: "✓ ";        /* Maxsus belgi qo'shish */
    color: green;
}
</style>

<ul class="rangli-royxat">
    <li>Rangli ro'yxat elementi</li>
    <li>Yana bir element</li>
</ul>

<ul class="maxsus-royxat">
    <li>Maxsus belgi bilan</li>
    <li>Yana bir element</li>
</ul>
```

### Amaliy misollar

#### Xarid ro'yxati
```html
<h2>Xarid ro'yxati</h2>
<ul>
    <li>Non</li>
    <li>Sut</li>
    <li>Tuxum</li>
    <li>Piyoz</li>
    <li>Kartoshka</li>
</ul>
```

#### Retsept qadamlari
```html
<h2>Osh tayyorlash</h2>
<ol>
    <li>Guruchni yuvish</li>
    <li>Go'shtni maydalash</li>
    <li>Sabzavotlarni qovurish</li>
    <li>Suv quyish</li>
    <li>45 daqiqa pishirish</li>
</ol>
```

#### O'quv dasturi
```html
<h2>Dasturlash kursi</h2>
<ol>
    <li>Asoslar
        <ul>
            <li>Kompyuter asoslari</li>
            <li>Internet haqida</li>
        </ul>
    </li>
    <li>Frontend
        <ol type="A">
            <li>HTML</li>
            <li>CSS</li>
            <li>JavaScript</li>
        </ol>
    </li>
    <li>Loyihalar
        <ul>
            <li>Portfolio sayt</li>
            <li>To-do list</li>
            <li>Kalkulyator</li>
        </ul>
    </li>
</ol>
```

### To'liq misol

```html
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <title>Ro'yxatlar Namunasi</title>
    <style>
        .highlighted { background-color: yellow; }
        .custom-list { list-style-type: none; }
        .custom-list li::before { content: "🎯 "; }
    </style>
</head>
<body>
    <h1>Turli Ro'yxat Turlari</h1>
    
    <h2>Tartibsiz ro'yxat</h2>
    <ul>
        <li>Apple</li>
        <li>Banan</li>
        <li>Apelsin</li>
    </ul>
    
    <h2>Tartiblangan ro'yxat</h2>
    <ol>
        <li>Uyg'onish</li>
        <li>Nonushta</li>
        <li>Maktabga borish</li>
    </ol>
    
    <h2>Ichma-ich ro'yxat</h2>
    <ul>
        <li>Dasturlash tillari
            <ol>
                <li>Python</li>
                <li>JavaScript</li>
                <li>HTML/CSS</li>
            </ol>
        </li>
        <li>Ma'lumotlar bazasi
            <ul>
                <li>MySQL</li>
                <li>MongoDB</li>
            </ul>
        </li>
    </ul>
    
    <h2>Maxsus bezatilgan ro'yxat</h2>
    <ul class="custom-list">
        <li>Birinchi maqsad</li>
        <li>Ikkinchi maqsad</li>
        <li>Uchinchi maqsad</li>
    </ul>
</body>
</html>
```

</details>

<details>
    <summary>CSS selektorlari</summary>

## 3.1 CSS Selektorlari

### Selektor nima?

**CSS selektor** - bu HTML elementlarini tanlash va ularga stil berish uchun ishlatiladigan qoidalardir. Selektorlar yordamida biz qaysi elementlarga qanday dizayn qo'llashni belgilaymiz.

### Asosiy selektor turlari

#### 1. Element selektori (Tag selektori)

HTML teglarini to'g'ridan-to'g'ri tanlaydi:

```css
h1 {
    color: blue;
}

p {
    font-size: 16px;
}

body {
    background-color: lightgray;
}
```

**Misol:**
```html
<style>
h1 { color: red; }
p { color: green; }
</style>

<h1>Bu qizil sarlavha</h1>
<p>Bu yashil paragraf</p>
<h1>Bu ham qizil sarlavha</h1>
```

#### 2. Class selektori

Class atributi orqali elementlarni tanlaydi. `.` (nuqta) bilan boshlanadi:

```css
.muhim {
    font-weight: bold;
    color: red;
}

.kichik {
    font-size: 12px;
}
```

**HTML da ishlatish:**
```html
<style>
.muhim { color: red; font-weight: bold; }
.yashil { color: green; }
</style>

<p class="muhim">Bu muhim paragraf</p>
<p class="yashil">Bu yashil paragraf</p>
<span class="muhim">Bu ham muhim matn</span>
```

#### 3. ID selektori

ID atributi orqali yagona elementni tanlaydi. `#` (panjara) bilan boshlanadi:

```css
#sarlavha {
    text-align: center;
    color: blue;
}

#footer {
    background-color: gray;
    padding: 20px;
}
```

**HTML da ishlatish:**
```html
<style>
#asosiy-sarlavha { 
    color: blue; 
    text-align: center; 
}
#maxsus-paragraf { 
    background-color: yellow; 
}
</style>

<h1 id="asosiy-sarlavha">Asosiy Sarlavha</h1>
<p id="maxsus-paragraf">Maxsus paragraf</p>
```

### Murakkab selektorlar

#### 4. Universal selektor

Barcha elementlarni tanlaydi:

```css
* {
    margin: 0;
    padding: 0;
}
```

#### 5. Guruhlash selektori

Bir nechta selektorni birgalikda ishlatish:

```css
h1, h2, h3 {
    color: blue;
    font-family: Arial;
}

.muhim, .diqqat, #maxsus {
    background-color: yellow;
}
```

#### 6. Descendant selektor (Avlod selektori)

Boshqa element ichidagi elementlarni tanlaydi:

```css
div p {
    color: red;
}

.konteyner h2 {
    text-align: center;
}
```

**Misol:**
```html
<style>
div p { color: red; }
</style>

<p>Bu qora rangda (div ichida emas)</p>
<div>
    <p>Bu qizil rangda (div ichida)</p>
    <span>
        <p>Bu ham qizil rangda (div ichidagi span ichida)</p>
    </span>
</div>
```

#### 7. Child selektor (Bola selektori)

To'g'ridan-to'g'ri bola elementlarni tanlaydi:

```css
div > p {
    font-weight: bold;
}
```

**Misol:**
```html
<style>
div > p { color: blue; }
</style>

<div>
    <p>Bu ko'k (to'g'ridan-to'g'ri bola)</p>
    <span>
        <p>Bu oddiy rang (nevara, bola emas)</p>
    </span>
</div>
```

#### 8. Adjacent sibling selektor

Keyingi qo'shni elementni tanlaydi:

```css
h1 + p {
    font-style: italic;
}
```

**Misol:**
```html
<style>
h1 + p { color: green; }
</style>

<h1>Sarlavha</h1>
<p>Bu yashil (h1 dan keyingi birinchi p)</p>
<p>Bu oddiy rang</p>
```

### Atribut selektorlari

#### 9. Atribut mavjudligi selektori

```css
[title] {
    border-bottom: 1px dotted;
}

input[required] {
    border: 2px solid red;
}
```

#### 10. Atribut qiymati selektori

```css
[class="muhim"] {
    color: red;
}

input[type="email"] {
    background-color: lightblue;
}
```

### Pseudo-class selektorlari

#### 11. Hover selektori

```css
a:hover {
    color: red;
    text-decoration: underline;
}

button:hover {
    background-color: blue;
}
```

#### 12. Boshqa pseudo-classlar

```css
a:visited { color: purple; }
input:focus { border: 2px solid blue; }
li:first-child { font-weight: bold; }
li:last-child { color: gray; }
p:nth-child(2) { background-color: yellow; }
```

### Selektorlar ustuvorligi

CSS da selektorlarning ahamiyati (specificity) bor:

1. **Inline CSS** (eng yuqori): `style="color: red"`
2. **ID selektori**: `#myId`
3. **Class selektori**: `.myClass`
4. **Element selektori**: `p`

```css
/* Eng past ustuvor */
p { color: black; }

/* O'rta ustuvor */
.muhim { color: blue; }

/* Yuqori ustuvor */
#maxsus { color: green; }

/* Eng yuqori ustuvor */
/* style="color: red" inline CSS */
```

### Amaliy misollar

#### Oddiy sayt strukturasi
```html
<style>
/* Asosiy elementlar */
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
}

/* Sarlavhalar */
h1, h2, h3 {
    color: #333;
}

/* Class selektorlari */
.header {
    background-color: #f4f4f4;
    padding: 20px;
    text-align: center;
}

.content {
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
}

.footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 10px;
}

/* Maxsus elementlar */
#logo {
    font-size: 24px;
    font-weight: bold;
}

/* Havolalar */
a {
    color: blue;
    text-decoration: none;
}

a:hover {
    color: red;
    text-decoration: underline;
}

/* Ro'yxatlar */
.menu li {
    display: inline;
    margin-right: 20px;
}
</style>

<div class="header">
    <h1 id="logo">Mening Saytim</h1>
    <ul class="menu">
        <li><a href="#home">Bosh sahifa</a></li>
        <li><a href="#about">Haqida</a></li>
        <li><a href="#contact">Aloqa</a></li>
    </ul>
</div>

<div class="content">
    <h2>Xush kelibsiz!</h2>
    <p>Bu mening birinchi web-saytim.</p>
</div>

<div class="footer">
    <p>© 2024 Mening Saytim</p>
</div>
```

### To'liq misol

```html
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <title>CSS Selektorlari</title>
    <style>
        /* Universal selektor */
        * { margin: 0; padding: 0; }
        
        /* Element selektorlari */
        body { 
            font-family: Arial, sans-serif; 
            background-color: #f9f9f9;
        }
        
        h1 { 
            color: #2c3e50; 
            text-align: center;
            margin: 20px 0;
        }
        
        /* Class selektorlari */
        .konteyner {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background-color: white;
        }
        
        .muhim {
            color: #e74c3c;
            font-weight: bold;
        }
        
        .belgilangan {
            background-color: #f1c40f;
            padding: 5px;
        }
        
        /* ID selektori */
        #maxsus-matn {
            font-size: 18px;
            color: #27ae60;
            border-left: 4px solid #27ae60;
            padding-left: 10px;
        }
        
        /* Descendant selektor */
        .konteyner p {
            line-height: 1.6;
            margin-bottom: 10px;
        }
        
        /* Pseudo-class */
        .tugma:hover {
            background-color: #3498db;
            color: white;
            cursor: pointer;
        }
        
        /* Atribut selektori */
        [title] {
            border-bottom: 1px dotted #333;
        }
    </style>
</head>
<body>
    <div class="konteyner">
        <h1>CSS Selektorlari Namunasi</h1>
        
        <p>Bu oddiy paragraf.</p>
        
        <p class="muhim">Bu muhim paragraf (class selektori).</p>
        
        <p id="maxsus-matn">Bu maxsus matn (ID selektori).</p>
        
        <p>Bu paragrafda <span class="belgilangan">belgilangan matn</span> bor.</p>
        
        <p title="Bu tooltip matn">Bu matnga hover qiling (atribut selektori).</p>
        
        <button class="tugma">Hover qiling</button>
    </div>
</body>
</html>
```

</details>

<details>
    <summary>Ranglar va shriftlar</summary>

## 3.2 Ranglar va Shriftlar

### CSS da ranglar

#### Rang belgilash usullari

**1. Rang nomlari**
```css
h1 { color: red; }
p { color: blue; }
div { background-color: green; }
```

**Asosiy rang nomlari:**
- `red` - qizil
- `blue` - ko'k  
- `green` - yashil
- `yellow` - sariq
- `purple` - binafsha
- `orange` - to'q sariq
- `pink` - pushti
- `brown` - jigarrang
- `black` - qora
- `white` - oq
- `gray` / `grey` - kulrang

**2. Hex kodlar**
```css
h1 { color: #FF0000; }    /* Qizil */
h2 { color: #00FF00; }    /* Yashil */
h3 { color: #0000FF; }    /* Ko'k */
p { color: #333333; }     /* To'q kulrang */
```

**Hex kod tushunchasi:**
- `#` bilan boshlanadi
- 6 ta raqam/harf (0-9, A-F)
- Birinchi 2 ta - qizil (Red)
- Keyingi 2 ta - yashil (Green)  
- Oxirgi 2 ta - ko'k (Blue)

**3. RGB ranglar**
```css
h1 { color: rgb(255, 0, 0); }     /* Qizil */
h2 { color: rgb(0, 255, 0); }     /* Yashil */
h3 { color: rgb(0, 0, 255); }     /* Ko'k */
p { color: rgb(100, 100, 100); }  /* Kulrang */
```

**4. RGBA ranglar (shaffoflik bilan)**
```css
div { 
    background-color: rgba(255, 0, 0, 0.5); /* Yarim shaffof qizil */
}
p {
    color: rgba(0, 0, 0, 0.8); /* Deyarli qora */
}
```

#### Rang xususiyatlari

**Matn rangi:**
```css
h1 { color: blue; }
p { color: #333; }
span { color: rgb(255, 0, 0); }
```

**Fon rangi:**
```css
body { background-color: #f9f9f9; }
div { background-color: lightblue; }
.container { background-color: rgba(0, 0, 0, 0.1); }
```

**Chegara rangi:**
```css
div {
    border: 2px solid red;
    border-color: blue; /* Chegara rangini alohida o'zgartirish */
}
```

### CSS da shriftlar

#### Font oilasi (Font Family)

```css
body {
    font-family: Arial, sans-serif;
}

h1 {
    font-family: "Times New Roman", serif;
}

.kod {
    font-family: "Courier New", monospace;
}
```

**Asosiy font turlari:**
- **Sans-serif:** Arial, Helvetica, Verdana
- **Serif:** Times New Roman, Georgia
- **Monospace:** Courier New, Monaco
- **Cursive:** Comic Sans MS
- **Fantasy:** Impact

#### Font o'lchami (Font Size)

```css
h1 { font-size: 32px; }
h2 { font-size: 24px; }
p { font-size: 16px; }
small { font-size: 12px; }

/* Nisbiy o'lchamlar */
h1 { font-size: 2em; }    /* Ota elementdan 2 baravar katta */
p { font-size: 1.2em; }   /* 20% katta */

/* Foiz o'lchamlar */
h2 { font-size: 150%; }   /* 1.5 baravar katta */
```

#### Font og'irligi (Font Weight)

```css
h1 { font-weight: bold; }      /* Qalin */
h2 { font-weight: normal; }    /* Oddiy */
p { font-weight: 300; }        /* Yengil */
strong { font-weight: 700; }   /* Qalin (raqam bilan) */

/* Raqamli qiymatlar: 100-900 */
```

#### Font uslubi (Font Style)

```css
em { font-style: italic; }     /* Qiyshiq */
p { font-style: normal; }      /* Oddiy */
.maxsus { font-style: oblique; } /* Og'ma */
```

#### Matn bezatish (Text Decoration)

```css
a { text-decoration: underline; }      /* Chiziq */
.orqali { text-decoration: line-through; } /* O'rtadan chiziq */
.ustida { text-decoration: overline; }     /* Ustidan chiziq */
.sof { text-decoration: none; }           /* Hech qanday bezak */
```

#### Matn joylashuvi (Text Align)

```css
h1 { text-align: center; }    /* Markazda */
p { text-align: left; }       /* Chapda */
.ong { text-align: right; }   /* O'ngda */
.tekis { text-align: justify; } /* Ikki tomonga tekislash */
```

#### Qator balandligi (Line Height)

```css
p {
    line-height: 1.5;     /* 1.5 baravar */
    line-height: 24px;    /* Aniq o'lcham */
    line-height: 150%;    /* Foiz */
}
```

### Google Fonts ishlatish

```html
<head>
    <!-- Google Fonts ulash -->
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap" rel="stylesheet">
    
    <style>
        body {
            font-family: 'Roboto', sans-serif;
        }
    </style>
</head>
```

### Amaliy misollar

#### Turli shrift va ranglar
```css
.sarlavha {
    font-family: 'Arial', sans-serif;
    font-size: 28px;
    font-weight: bold;
    color: #2c3e50;
    text-align: center;
}

.kichik-sarlavha {
    font-family: 'Georgia', serif;
    font-size: 20px;
    color: #34495e;
    border-bottom: 2px solid #3498db;
}

.asosiy-matn {
    font-family: 'Verdana', sans-serif;
    font-size: 16px;
    line-height: 1.6;
    color: #444;
    text-align: justify;
}

.muhim-matn {
    font-weight: bold;
    color: #e74c3c;
    background-color: rgba(231, 76, 60, 0.1);
    padding: 5px;
}

.kod-matn {
    font-family: 'Courier New', monospace;
    font-size: 14px;
    background-color: #f8f8f8;
    color: #333;
    border: 1px solid #ddd;
    padding: 10px;
}
```

### To'liq misol

```html
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <title>Ranglar va Shriftlar</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f5f5f5;
            margin: 0;
            padding: 20px;
        }
        
        .container {
            max-width: 800px;
            margin: 0 auto;
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        h1 {
            font-family: 'Georgia', serif;
            font-size: 32px;
            font-weight: bold;
            color: #2c3e50;
            text-align: center;
            margin-bottom: 30px;
            border-bottom: 3px solid #3498db;
            padding-bottom: 10px;
        }
        
        h2 {
            font-size: 24px;
            color: #34495e;
            margin-top: 25px;
            margin-bottom: 15px;
        }
        
        p {
            font-size: 16px;
            line-height: 1.6;
            color: #555;
            margin-bottom: 15px;
            text-align: justify;
        }
        
        .muhim {
            color: #e74c3c;
            font-weight: bold;
            background-color: rgba(231, 76, 60, 0.1);
            padding: 3px 6px;
            border-radius: 3px;
        }
        
        .belgilangan {
            background-color: #f1c40f;
            padding: 2px 4px;
            border-radius: 2px;
        }
        
        .kod {
            font-family: 'Courier New', monospace;
            background-color: #ecf0f1;
            border: 1px solid #bdc3c7;
            padding: 15px;
            border-radius: 5px;
            font-size: 14px;
            color: #2c3e50;
        }
        
        .rang-namuna {
            display: inline-block;
            width: 20px;
            height: 20px;
            margin-right: 10px;
            border: 1px solid #ccc;
            vertical-align: middle;
        }
        
        .qizil { background-color: #e74c3c; }
        .yashil { background-color: #27ae60; }
        .kok { background-color: #3498db; }
        .sariq { background-color: #f1c40f; }
    </style>
</head>
<body>
    <div class="container">
        <h1>Ranglar va Shriftlar</h1>
        
        <h2>Turli Ranglar</h2>
        <p>
            <span class="rang-namuna qizil"></span>Qizil rang - 
            <span class="muhim">muhim ma'lumotlar</span> uchun
        </p>
        <p>
            <span class="rang-namuna yashil"></span>Yashil rang - 
            muvaffaqiyat belgilari uchun
        </p>
        <p>
            <span class="rang-namuna kok"></span>Ko'k rang - 
            havolalar va tugmalar uchun
        </p>
        <p>
            <span class="rang-namuna sariq"></span>Sariq rang - 
            <span class="belgilangan">belgilangan matn</span> uchun
        </p>
        
        <h2>Shrift Misollar</h2>
        <p>Bu oddiy Arial shriftidagi matn.</p>
        
        <div class="kod">
            Bu Courier New shriftidagi kod matni.
            Monospace shriftlar kod uchun juda mos keladi.
        </div>
        
        <h2>Matn Formatlash</h2>
        <p style="text-align: center; font-style: italic;">
            Bu markazga joylashtirilgan va qiyshiq matn.
        </p>
        
        <p style="text-decoration: underline; font-weight: bold;">
            Bu chizilgan va qalin matn.
        </p>
    </div>
</body>
</html>
```

</details>

<details>
    <summary>Matn o'lchamlari</summary>

## 3.3 Matn O'lchamlari

### Font o'lchami (Font Size)

#### Mutlaq o'lchamlar

**Piksellar (px) - eng aniq**
```css
h1 { font-size: 32px; }
h2 { font-size: 24px; }
p { font-size: 16px; }
small { font-size: 12px; }
```

**Nuqtalar (pt) - bosma uchun**
```css
h1 { font-size: 24pt; }
p { font-size: 12pt; }
```

#### Nisbiy o'lchamlar

**Em - ota elementga nisbatan**
```css
body { font-size: 16px; }
h1 { font-size: 2em; }    /* 32px (16 × 2) */
h2 { font-size: 1.5em; }  /* 24px (16 × 1.5) */
p { font-size: 1em; }     /* 16px (16 × 1) */
small { font-size: 0.8em; } /* 12.8px (16 × 0.8) */
```

**Rem - root elementga nisbatan**
```css
html { font-size: 16px; }
h1 { font-size: 2rem; }   /* 32px */
h2 { font-size: 1.5rem; } /* 24px */
p { font-size: 1rem; }    /* 16px */
```

**Foizlar (%)**
```css
h1 { font-size: 200%; }   /* Ota elementdan 2 baravar katta */
h2 { font-size: 150%; }   /* 1.5 baravar katta */
p { font-size: 100%; }    /* Ota element bilan bir xil */
```

#### Maxsus kalit so'zlar

```css
h1 { font-size: xx-large; }
h2 { font-size: x-large; }
h3 { font-size: large; }
p { font-size: medium; }
small { font-size: small; }
```

**O'lcham ierarxiyasi:**
- `xx-small` - juda kichik
- `x-small` - kichik
- `small` - kichikroq
- `medium` - o'rta (standart)
- `large` - kattaroq
- `x-large` - katta
- `xx-large` - juda katta

### Qator balandligi (Line Height)

#### Turli usullar

```css
p {
    line-height: 1.5;      /* Raqamli qiymat (tavsiya) */
    line-height: 24px;     /* Piksellar */
    line-height: 1.5em;    /* Em */
    line-height: 150%;     /* Foiz */
}
```

#### Qator balandligi ta'siri

```css
.siqiq {
    line-height: 1.2;   /* Siqiq qatorlar */
}

.oddiy {
    line-height: 1.5;   /* Oddiy oraliq */
}

.keng {
    line-height: 2.0;   /* Keng oraliq */
}
```

### Harf oralig'i (Letter Spacing)

```css
h1 {
    letter-spacing: 2px;    /* Harflar orasida 2px */
}

.keng-harflar {
    letter-spacing: 0.1em;  /* Keng harflar */
}

.siqiq-harflar {
    letter-spacing: -1px;   /* Siqiq harflar */
}

.oddiy {
    letter-spacing: normal; /* Standart */
}
```

### So'z oralig'i (Word Spacing)

```css
p {
    word-spacing: 5px;      /* So'zlar orasida 5px */
}

.keng-sozlar {
    word-spacing: 0.3em;    /* Keng so'z oralig'i */
}

.oddiy {
    word-spacing: normal;   /* Standart */
}
```

### Matn chuqurlik (Text Indent)

```css
p {
    text-indent: 20px;      /* Birinchi qator chuqurligi */
}

.paragraf {
    text-indent: 2em;       /* 2em chuqurlik */
}
```

### Matn transformatsiyasi (Text Transform)

```css
.katta-harflar {
    text-transform: uppercase;   /* KATTA HARFLAR */
}

.kichik-harflar {
    text-transform: lowercase;   /* kichik harflar */
}

.bosh-harflar {
    text-transform: capitalize;  /* Har So'z Bosh Harfi */
}

.oddiy {
    text-transform: none;        /* O'zgartirmaslik */
}
```

### Responsive matn o'lchamlari

#### Media queries bilan

```css
/* Mobil (kichik ekranlar) */
@media (max-width: 600px) {
    h1 { font-size: 24px; }
    p { font-size: 14px; }
}

/* Planshet */
@media (min-width: 601px) and (max-width: 900px) {
    h1 { font-size: 28px; }
    p { font-size: 15px; }
}

/* Desktop */
@media (min-width: 901px) {
    h1 { font-size: 32px; }
    p { font-size: 16px; }
}
```

#### Viewport birliklaridan foydalanish

```css
h1 {
    font-size: 4vw;  /* Viewport kengligining 4% */
}

h2 {
    font-size: 3vh;  /* Viewport balandligining 3% */
}

p {
    font-size: 2vmin; /* Viewport minimal o'lchamining 2% */
}
```

### Font Weight (Og'irlik) raqamlari

```css
.juda-yengil { font-weight: 100; }
.yengil { font-weight: 300; }
.oddiy { font-weight: 400; }    /* normal */
.o'rta { font-weight: 500; }
.yarim-qalin { font-weight: 600; }
.qalin { font-weight: 700; }    /* bold */
.juda-qalin { font-weight: 900; }
```

### Amaliy misollar

#### Maqola dizayni
```css
.maqola {
    max-width: 700px;
    margin: 0 auto;
    padding: 20px;
}

.maqola h1 {
    font-size: 2.5rem;
    line-height: 1.2;
    margin-bottom: 0.5em;
    text-align: center;
}

.maqola h2 {
    font-size: 1.8rem;
    line-height: 1.3;
    margin-top: 1.5em;
    margin-bottom: 0.5em;
}

.maqola p {
    font-size: 1.1rem;
    line-height: 1.6;
    text-indent: 1.5em;
    margin-bottom: 1em;
    text-align: justify;
}

.maqola .birinchi-paragraf {
    text-indent: 0;     /* Birinchi paragraf chuqursiz */
    font-size: 1.2rem;
}
```

#### Turli o'lchamdagi kontentlar
```css
.kichik-matn {
    font-size: 0.8rem;
    line-height: 1.4;
    color: #666;
}

.oddiy-matn {
    font-size: 1rem;
    line-height: 1.5;
}

.katta-matn {
    font-size: 1.2rem;
    line-height: 1.6;
    font-weight: 300;
}

.juda-katta {
    font-size: 2rem;
    line-height: 1.2;
    font-weight: bold;
    letter-spacing: 1px;
}
```

### To'liq misol

```html
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <title>Matn O'lchamlari</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 20px;
            background-color: #f9f9f9;
        }
        
        .container {
            max-width: 800px;
            margin: 0 auto;
            background-color: white;
            padding: 30px;
            border-radius: 10px;
        }
        
        /* Turli o'lchamli sarlavhalar */
        .sarlavha-1 {
            font-size: 3rem;
            line-height: 1.1;
            text-align: center;
            margin-bottom: 0.5em;
            color: #2c3e50;
        }
        
        .sarlavha-2 {
            font-size: 2rem;
            line-height: 1.3;
            margin: 1.5em 0 0.5em 0;
            color: #34495e;
        }
        
        .sarlavha-3 {
            font-size: 1.5rem;
            line-height: 1.4;
            margin: 1em 0 0.5em 0;
            color: #7f8c8d;
        }
        
        /* Turli paragraf uslublari */
        .birinchi-paragraf {
            font-size: 1.2rem;
            line-height: 1.6;
            font-weight: 300;
            color: #2c3e50;
            text-indent: 0;
        }
        
        .oddiy-paragraf {
            font-size: 1rem;
            line-height: 1.6;
            text-indent: 2em;
            margin-bottom: 1em;
            text-align: justify;
        }
        
        .kichik-matn {
            font-size: 0.9rem;
            line-height: 1.4;
            color: #7f8c8d;
            font-style: italic;
        }
        
        /* Maxsus formatlar */
        .keng-harflar {
            letter-spacing: 3px;
            text-transform: uppercase;
            font-weight: bold;
        }
        
        .siqiq-qatorlar {
            line-height: 1.2;
            background-color: #ecf0f1;
            padding: 10px;
            border-left: 4px solid #3498db;
        }
        
        .keng-qatorlar {
            line-height: 2.5;
            background-color: #fdf2e9;
            padding: 15px;
        }
        
        /* Responsive font */
        .responsive-sarlavha {
            font-size: 4vw;
            text-align: center;
            color: #e74c3c;
            margin: 20px 0;
        }
        
        /* Font weight misollar */
        .yengil { font-weight: 300; }
        .oddiy { font-weight: 400; }
        .yarim-qalin { font-weight: 600; }
        .qalin { font-weight: 700; }
        .juda-qalin { font-weight: 900; }
        
        @media (max-width: 600px) {
            .sarlavha-1 { font-size: 2rem; }
            .sarlavha-2 { font-size: 1.5rem; }
            .responsive-sarlavha { font-size: 6vw; }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1 class="sarlavha-1">Matn O'lchamlari</h1>
        
        <p class="birinchi-paragraf">
            Bu birinchi paragraf bo'lib, boshqa paragraflardan biroz kattaroq 
            va yengilroq ko'rinishda.
        </p>
        
        <h2 class="sarlavha-2">Font Size Misollar</h2>
        
        <p class="oddiy-paragraf">
            Bu oddiy paragraf bo'lib, standart o'lchamda va qator balandligida. 
            Matn justify qilingan va birinchi qatorida chuqurlik mavjud.
        </p>
        
        <p class="oddiy-paragraf">
            Ikkinchi paragraf ham xuddi birinchisi kabi formatlanган, 
            lekin boshqa mazmun bilan.
        </p>
        
        <h3 class="sarlavha-3">Line Height Misollar</h3>
        
        <div class="siqiq-qatorlar">
            <strong>Siqiq qatorlar:</strong> Bu matn siqiq qator balandligi bilan yozilgan. 
            Qatorlar bir-biriga yaqin joylashgan va matn zichroq ko'rinadi.
        </div>
        
        <div class="keng-qatorlar">
            <strong>Keng qatorlar:</strong> Bu matn keng qator balandligi bilan yozilgan. 
            Qatorlar orasida ko'proq joy bor va o'qish osonroq.
        </div>
        
        <h3 class="sarlavha-3">Letter Spacing</h3>
        
        <p class="keng-harflar">Keng harflar bilan yozilgan matn</p>
        
        <h3 class="sarlavha-3">Font Weight Misollar</h3>
        
        <p><span class="yengil">Yengil matn (300)</span></p>
        <p><span class="oddiy">Oddiy matn (400)</span></p>
        <p><span class="yarim-qalin">Yarim qalin matn (600)</span></p>
        <p><span class="qalin">Qalin matn (700)</span></p>
        <p><span class="juda-qalin">Juda qalin matn (900)</span></p>
        
        <h2 class="responsive-sarlavha">Responsive Sarlavha</h2>
        
        <p class="kichik-matn">
            Bu kichik matn - odatda izohlar, sanalar yoki qo'shimcha 
            ma'lumotlar uchun ishlatiladi.
        </p>
    </div>
</body>
</html>
```

</details>