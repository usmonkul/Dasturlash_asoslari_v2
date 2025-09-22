<details>
    <summary>Web-saytlar Dunyosiga Kirish</summary>
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
</details>