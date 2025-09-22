<details>
    <summary>HTML formalar (form, input, textarea)</summary>

## 6.1 HTML Formalar (form, input, textarea)

### Form nima?

**HTML forma** - foydalanuvchilardan ma'lumot olish uchun ishlatiladi. Formalar orqali foydalanuvchilar matn kiritish, tanlov qilish va ma'lumotlarni yuborish mumkin.

### Asosiy form teglari

#### 1. `<form>` - forma konteyner
```html
<form>
    <!-- Form elementlari bu yerda -->
</form>
```

#### 2. `<input>` - ma'lumot kiritish maydoni
```html
<input type="text" name="username">
```

#### 3. `<textarea>` - uzun matn kiritish maydoni
```html
<textarea name="message"></textarea>
```

### Oddiy forma yaratish

#### Asosiy forma struktura
```html
<form>
    <input type="text" name="ism" placeholder="Ismingizni kiriting">
    <textarea name="xabar" placeholder="Xabaringizni yozing"></textarea>
</form>
```

### Form atributlari

#### 1. Action atributi
```html
<form action="/yuborish">
    <!-- Form ma'lumotlari qayerga yuborilishi -->
</form>
```

#### 2. Method atributi
```html
<form action="/yuborish" method="post">
    <!-- POST usuli bilan yuborish -->
</form>
```

#### 3. Name atributi
```html
<form>
    <input type="text" name="foydalanuvchi_ismi">
    <input type="email" name="elektron_pochta">
</form>
```

### Textarea xususiyatlari

#### 1. O'lchamlarni belgilash
```html
<textarea name="xabar" rows="4" cols="50"></textarea>
```

#### 2. Placeholder qo'shish
```html
<textarea name="xabar" placeholder="Xabaringizni bu yerda yozing"></textarea>
```

#### 3. Maksimal uzunlik
```html
<textarea name="xabar" maxlength="200"></textarea>
```

### Amaliy misollar

#### 1. Oddiy aloqa formasi
```html
<form>
    <h3>Biz bilan bog'laning</h3>
    
    <p>Ismingiz:</p>
    <input type="text" name="ism" placeholder="Ismingizni kiriting">
    
    <p>Xabaringiz:</p>
    <textarea name="xabar" rows="5" cols="40" placeholder="Xabaringizni yozing"></textarea>
    
    <br><br>
    <input type="submit" value="Yuborish">
</form>
```

#### 2. O'quvchi ro'yxatga olish formasi
```html
<form action="/ro_yxatga_olish" method="post">
    <h3>O'quvchi ro'yxatga olish</h3>
    
    <p>Ism Familiya:</p>
    <input type="text" name="toliq_ism" placeholder="Ism va familiyangiz">
    
    <p>Yoshingiz:</p>
    <input type="number" name="yosh" placeholder="Yoshingizni kiriting">
    
    <p>Haqida:</p>
    <textarea name="haqida" rows="3" cols="50" placeholder="O'zingiz haqingizda qisqacha yozing"></textarea>
    
    <br><br>
    <input type="submit" value="Ro'yxatdan o'tish">
</form>
```

#### 3. Shikoyat formasi
```html
<form>
    <h3>Shikoyat yuborish</h3>
    
    <p>Muammo haqida batafsil yozing:</p>
    <textarea name="shikoyat" rows="6" cols="60" placeholder="Muammoingizni batafsil tasvirlab bering"></textarea>
    
    <br><br>
    <input type="submit" value="Shikoyat yuborish">
</form>
```

</details>

<details>
    <summary>Turli xil input turlari (text, email, password)</summary>

## 6.2 Turli Xil Input Turlari (text, email, password)

### Input type xususiyati

Har bir `<input>` elementi `type` atributiga ega bo'lishi kerak. Bu atribut input qanday ishlashini belgilaydi.

### Matn input turlari

#### 1. Text - oddiy matn
```html
<input type="text" name="ism" placeholder="Ismingizni kiriting">
```

#### 2. Email - elektron pochta
```html
<input type="email" name="email" placeholder="email@example.com">
```

#### 3. Password - parol
```html
<input type="password" name="parol" placeholder="Parolingizni kiriting">
```

#### 4. Number - raqam
```html
<input type="number" name="yosh" placeholder="Yoshingiz">
```

#### 5. Tel - telefon raqami
```html
<input type="tel" name="telefon" placeholder="+998 90 123 45 67">
```

#### 6. URL - veb-sayt manzili
```html
<input type="url" name="veb_sayt" placeholder="https://example.com">
```

### Tanlov input turlari

#### 1. Radio - bitta tanlov
```html
<input type="radio" name="jins" value="erkak"> Erkak
<input type="radio" name="jins" value="ayol"> Ayol
```

#### 2. Checkbox - ko'p tanlov
```html
<input type="checkbox" name="fanlar" value="matematika"> Matematika
<input type="checkbox" name="fanlar" value="fizika"> Fizika
<input type="checkbox" name="fanlar" value="kimyo"> Kimyo
```

### Boshqa input turlari

#### 1. Date - sana
```html
<input type="date" name="tugilgan_sana">
```

#### 2. Time - vaqt
```html
<input type="time" name="vaqt">
```

#### 3. File - fayl yuklash
```html
<input type="file" name="fayl">
```

#### 4. Submit - yuborish tugmasi
```html
<input type="submit" value="Yuborish">
```

#### 5. Reset - tozalash tugmasi
```html
<input type="reset" value="Tozalash">
```

### Input atributlari

#### 1. Required - majburiy
```html
<input type="text" name="ism" required>
```

#### 2. Maxlength - maksimal uzunlik
```html
<input type="text" name="ism" maxlength="50">
```

#### 3. Min va Max - minimum va maksimal qiymat
```html
<input type="number" name="yosh" min="10" max="100">
```

#### 4. Step - qadam
```html
<input type="number" name="ball" min="0" max="5" step="0.5">
```

### Amaliy misollar

#### 1. Foydalanuvchi ro'yxatga olish formasi
```html
<form>
    <h3>Yangi foydalanuvchi ro'yxatga olish</h3>
    
    <p>Ism Familiya:</p>
    <input type="text" name="toliq_ism" placeholder="Ism va familiyangiz" required>
    
    <p>Elektron pochta:</p>
    <input type="email" name="email" placeholder="email@example.com" required>
    
    <p>Parol:</p>
    <input type="password" name="parol" placeholder="Parol yarating" required>
    
    <p>Yoshingiz:</p>
    <input type="number" name="yosh" min="10" max="100" placeholder="Yoshingiz">
    
    <p>Telefon:</p>
    <input type="tel" name="telefon" placeholder="+998 90 123 45 67">
    
    <br><br>
    <input type="submit" value="Ro'yxatdan o'tish">
    <input type="reset" value="Tozalash">
</form>
```

#### 2. So'rovnoma formasi
```html
<form>
    <h3>So'rovnoma</h3>
    
    <p>Ismingiz:</p>
    <input type="text" name="ism" placeholder="Ismingizni kiriting" required>
    
    <p>Sevimli faningiz:</p>
    <input type="radio" name="sevimli_fan" value="matematika"> Matematika
    <input type="radio" name="sevimli_fan" value="fizika"> Fizika
    <input type="radio" name="sevimli_fan" value="kimyo"> Kimyo
    <input type="radio" name="sevimli_fan" value="biologiya"> Biologiya
    
    <p>Qaysi fanlarni o'rganmoqchisiz:</p>
    <input type="checkbox" name="fanlar" value="dasturlash"> Dasturlash
    <input type="checkbox" name="fanlar" value="dizayn"> Dizayn
    <input type="checkbox" name="fanlar" value="marketing"> Marketing
    
    <p>Tug'ilgan sanangiz:</p>
    <input type="date" name="tugilgan_sana">
    
    <br><br>
    <input type="submit" value="Javob yuborish">
</form>
```

#### 3. Ma'lumotlar formasi
```html
<form>
    <h3>Shaxsiy ma'lumotlar</h3>
    
    <p>Ism:</p>
    <input type="text" name="ism" maxlength="30" required>
    
    <p>Email:</p>
    <input type="email" name="email" required>
    
    <p>Parol:</p>
    <input type="password" name="parol" required>
    
    <p>Telefon:</p>
    <input type="tel" name="telefon" placeholder="+998">
    
    <p>Veb-sayt (ixtiyoriy):</p>
    <input type="url" name="veb_sayt" placeholder="https://">
    
    <p>Yosh:</p>
    <input type="number" name="yosh" min="1" max="120">
    
    <br><br>
    <input type="submit" value="Saqlash">
    <input type="reset" value="Qayta boshlash">
</form>
```

</details>

<details>
    <summary>Tugmalar va bosish hodisalari</summary>

## 6.3 Tugmalar va Bosish Hodisalari

### Tugma turlari

#### 1. Submit tugmasi - forma yuborish
```html
<input type="submit" value="Yuborish">
```

#### 2. Reset tugmasi - forma tozalash
```html
<input type="reset" value="Tozalash">
```

#### 3. Button tugmasi - oddiy tugma
```html
<input type="button" value="Bosish" onclick="alert('Salom!')">
```

#### 4. Button tegi - zamonaviy tugma
```html
<button type="submit">Yuborish</button>
<button type="reset">Tozalash</button>
<button type="button">Oddiy tugma</button>
```

### Tugma atributlari

#### 1. Value - tugma matni
```html
<input type="submit" value="Ro'yxatdan o'tish">
```

#### 2. Disabled - tugmani o'chirish
```html
<input type="submit" value="Yuborish" disabled>
```

#### 3. Form - tugma qaysi formaga tegishli
```html
<form id="forma1">
    <input type="text" name="ism">
</form>
<button type="submit" form="forma1">Yuborish</button>
```

### Amaliy misollar

#### 1. Oddiy tugmalar
```html
<h3>Forma tugmalari</h3>

<form>
    <p>Ismingiz:</p>
    <input type="text" name="ism" placeholder="Ismingizni kiriting">
    
    <br><br>
    
    <button type="submit">Formani yuborish</button>
    <button type="reset">Formani tozalash</button>
</form>
```

#### 2. Turli tugma turlari
```html
<h3>Tugma turlari</h3>

<form>
    <input type="submit" value="Submit tugmasi">
    <input type="reset" value="Reset tugmasi">
    <input type="button" value="Oddiy tugma">
    
    <br><br>
    
    <button type="submit">Button tegi - Submit</button>
    <button type="reset">Button tegi - Reset</button>
    <button type="button">Button tegi - Oddiy</button>
</form>
```

#### 3. Disabled tugma
```html
<h3>Disabled tugma</h3>

<form>
    <input type="text" name="ism" placeholder="Ismingizni kiriting">
    
    <br><br>
    
    <button type="submit">Faol tugma</button>
    <button type="submit" disabled>O'chirilgan tugma</button>
</form>
```

</details>

<details>
    <summary>CSS bilan formalarni chiroyli qilish</summary>

## 6.4 CSS bilan Formalarni Chiroyli Qilish

### Asosiy form stillar

#### 1. Input maydonlari
```css
input[type="text"],
input[type="email"],
input[type="password"] {
    width: 300px;
    padding: 10px;
    border: 2px solid #ddd;
    border-radius: 5px;
    font-size: 16px;
}
```

#### 2. Textarea
```css
textarea {
    width: 300px;
    height: 100px;
    padding: 10px;
    border: 2px solid #ddd;
    border-radius: 5px;
    font-size: 16px;
    resize: vertical;
}
```

#### 3. Tugmalar
```css
input[type="submit"],
button {
    background-color: #007bff;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    font-size: 16px;
    cursor: pointer;
}

input[type="submit"]:hover,
button:hover {
    background-color: #0056b3;
}
```

### Form konteyner stillar

#### 1. Form dizayni
```css
.forma-konteyner {
    max-width: 400px;
    margin: 20px auto;
    padding: 20px;
    background-color: #f8f9fa;
    border-radius: 10px;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
}
```

#### 2. Form guruhi
```css
.form-guruh {
    margin-bottom: 15px;
}

.form-guruh label {
    display: block;
    margin-bottom: 5px;
    font-weight: bold;
    color: #333;
}
```

### Hover va focus effektlari

#### 1. Input hover va focus
```css
input:focus {
    border-color: #007bff;
    outline: none;
    box-shadow: 0 0 5px rgba(0,123,255,0.3);
}

input:hover {
    border-color: #0056b3;
}
```

#### 2. Tugma effektlari
```css
button {
    transition: all 0.3s ease;
}

button:hover {
    transform: translateY(-2px);
    box-shadow: 0 4px 8px rgba(0,0,0,0.2);
}

button:active {
    transform: translateY(0);
}
```

### Responsive form dizayni

#### 1. Mobil uchun
```css
@media (max-width: 600px) {
    .forma-konteyner {
        margin: 10px;
        padding: 15px;
    }
    
    input, textarea {
        width: 100%;
        box-sizing: border-box;
    }
}
```

### Amaliy misollar

#### 1. Oddiy chiroyli forma
```html
<style>
.chiroyli-forma {
    max-width: 400px;
    margin: 20px auto;
    padding: 30px;
    background-color: white;
    border-radius: 10px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
}

.chiroyli-forma h3 {
    text-align: center;
    color: #333;
    margin-bottom: 25px;
}

.form-guruh {
    margin-bottom: 20px;
}

.form-guruh label {
    display: block;
    margin-bottom: 5px;
    font-weight: bold;
    color: #555;
}

.form-guruh input,
.form-guruh textarea {
    width: 100%;
    padding: 12px;
    border: 2px solid #ddd;
    border-radius: 5px;
    font-size: 16px;
    box-sizing: border-box;
}

.form-guruh input:focus,
.form-guruh textarea:focus {
    border-color: #007bff;
    outline: none;
    box-shadow: 0 0 5px rgba(0,123,255,0.3);
}

.submit-tugma {
    width: 100%;
    background-color: #007bff;
    color: white;
    padding: 12px;
    border: none;
    border-radius: 5px;
    font-size: 16px;
    cursor: pointer;
    transition: background-color 0.3s ease;
}

.submit-tugma:hover {
    background-color: #0056b3;
}
</style>

<div class="chiroyli-forma">
    <h3>Biz bilan bog'laning</h3>
    
    <form>
        <div class="form-guruh">
            <label for="ism">Ismingiz:</label>
            <input type="text" id="ism" name="ism" placeholder="Ismingizni kiriting">
        </div>
        
        <div class="form-guruh">
            <label for="email">Email:</label>
            <input type="email" id="email" name="email" placeholder="email@example.com">
        </div>
        
        <div class="form-guruh">
            <label for="xabar">Xabar:</label>
            <textarea id="xabar" name="xabar" rows="4" placeholder="Xabaringizni yozing"></textarea>
        </div>
        
        <button type="submit" class="submit-tugma">Xabar yuborish</button>
    </form>
</div>
```

#### 2. Rangli forma dizayni
```html
<style>
.rangli-forma {
    max-width: 350px;
    margin: 20px auto;
    padding: 25px;
    background: linear-gradient(135deg, #667eea, #764ba2);
    border-radius: 15px;
    color: white;
}

.rangli-forma h3 {
    text-align: center;
    margin-bottom: 25px;
    color: white;
}

.rangli-forma input,
.rangli-forma textarea {
    width: 100%;
    padding: 12px;
    border: none;
    border-radius: 8px;
    font-size: 16px;
    margin-bottom: 15px;
    box-sizing: border-box;
}

.rangli-forma input:focus,
.rangli-forma textarea:focus {
    outline: none;
    box-shadow: 0 0 10px rgba(255,255,255,0.3);
}

.rangli-tugma {
    width: 100%;
    background-color: white;
    color: #667eea;
    padding: 12px;
    border: none;
    border-radius: 8px;
    font-size: 16px;
    font-weight: bold;
    cursor: pointer;
    transition: transform 0.3s ease;
}

.rangli-tugma:hover {
    transform: translateY(-2px);
    box-shadow: 0 4px 8px rgba(0,0,0,0.2);
}
</style>

<div class="rangli-forma">
    <h3>Ro'yxatdan o'tish</h3>
    
    <form>
        <input type="text" name="ism" placeholder="Ismingizni kiriting">
        <input type="email" name="email" placeholder="Email manzilingiz">
        <input type="password" name="parol" placeholder="Parol yarating">
        <textarea name="haqida" rows="3" placeholder="O'zingiz haqingizda qisqacha"></textarea>
        
        <button type="submit" class="rangli-tugma">Ro'yxatdan o'tish</button>
    </form>
</div>
```

#### 3. Minimalist forma
```html
<style>
.minimal-forma {
    max-width: 300px;
    margin: 30px auto;
    padding: 40px 20px;
    background-color: #fafafa;
    border: 1px solid #e0e0e0;
}

.minimal-forma h3 {
    text-align: center;
    margin-bottom: 30px;
    color: #333;
    font-weight: 300;
}

.minimal-input {
    width: 100%;
    padding: 15px 0;
    border: none;
    border-bottom: 1px solid #ddd;
    background: transparent;
    font-size: 16px;
    margin-bottom: 20px;
    box-sizing: border-box;
}

.minimal-input:focus {
    outline: none;
    border-bottom-color: #333;
}

.minimal-tugma {
    width: 100%;
    background-color: #333;
    color: white;
    padding: 15px;
    border: none;
    font-size: 16px;
    cursor: pointer;
    margin-top: 20px;
}

.minimal-tugma:hover {
    background-color: #555;
}
</style>

<div class="minimal-forma">
    <h3>Kirish</h3>
    
    <form>
        <input type="email" class="minimal-input" placeholder="Email">
        <input type="password" class="minimal-input" placeholder="Parol">
        
        <button type="submit" class="minimal-tugma">Kirish</button>
    </form>
</div>
```

</details>

<details>
    <summary>Placeholder va label</summary>

## 6.5 Placeholder va Label

### Placeholder nima?

**Placeholder** - input maydonida ko'rsatiladigan qisqa yo'riqnoma matni. Foydalanuvchi matn kiritganda placeholder yo'qoladi.

### Label nima?

**Label** - input maydoniga bog'liq sarlavha. Label bosilganda input fokus oladi.

### Placeholder ishlatish

#### 1. Oddiy placeholder
```html
<input type="text" placeholder="Ismingizni kiriting">
<input type="email" placeholder="email@example.com">
<input type="password" placeholder="Parolingizni kiriting">
```

#### 2. Textarea uchun placeholder
```html
<textarea placeholder="Xabaringizni bu yerda yozing"></textarea>
```

#### 3. Turli input turlari uchun
```html
<input type="tel" placeholder="+998 90 123 45 67">
<input type="url" placeholder="https://example.com">
<input type="number" placeholder="Yoshingizni kiriting">
```

### Label ishlatish

#### 1. Oddiy label
```html
<label for="ism">Ismingiz:</label>
<input type="text" id="ism" name="ism">
```

#### 2. Label va input bog'lash
```html
<label for="email">Email manzili:</label>
<input type="email" id="email" name="email">
```

#### 3. Label ichida input
```html
<label>
    Parol:
    <input type="password" name="parol">
</label>
```

### Label va placeholder birga

#### 1. Ikki usul birga
```html
<label for="username">Foydalanuvchi nomi:</label>
<input type="text" id="username" name="username" placeholder="Foydalanuvchi nomingizni kiriting">
```

#### 2. Ko'p maydonli forma
```html
<label for="ism">Ism Familiya:</label>
<input type="text" id="ism" name="ism" placeholder="Ism va familiyangiz">

<label for="yosh">Yosh:</label>
<input type="number" id="yosh" name="yosh" placeholder="Yoshingizni kiriting">

<label for="xabar">Xabar:</label>
<textarea id="xabar" name="xabar" placeholder="Xabaringizni bu yerda yozing"></textarea>
```

### CSS bilan placeholder bezatish

#### 1. Placeholder rangini o'zgartirish
```css
input::placeholder {
    color: #999;
    font-style: italic;
}

textarea::placeholder {
    color: #666;
}
```

#### 2. Placeholder matn o'lchami
```css
input::placeholder {
    font-size: 14px;
}
```

### Amaliy misollar

#### 1. To'liq forma - label va placeholder
```html
<style>
.toliq-forma {
    max-width: 400px;
    margin: 20px auto;
    padding: 25px;
    background-color: #f8f9fa;
    border-radius: 10px;
}

.form-qator {
    margin-bottom: 20px;
}

.form-qator label {
    display: block;
    margin-bottom: 5px;
    font-weight: bold;
    color: #333;
}

.form-qator input,
.form-qator textarea {
    width: 100%;
    padding: 10px;
    border: 2px solid #ddd;
    border-radius: 5px;
    font-size: 16px;
    box-sizing: border-box;
}

.form-qator input::placeholder,
.form-qator textarea::placeholder {
    color: #999;
    font-style: italic;
}

.submit-btn {
    background-color: #28a745;
    color: white;
    padding: 12px 25px;
    border: none;
    border-radius: 5px;
    font-size: 16px;
    cursor: pointer;
}
</style>

<div class="toliq-forma">
    <h3>Ma'lumotlar formasi</h3>
    
    <form>
        <div class="form-qator">
            <label for="toliq_ism">Ism Familiya:</label>
            <input type="text" id="toliq_ism" name="toliq_ism" placeholder="Ism va familiyangizni to'liq yozing">
        </div>
        
        <div class="form-qator">
            <label for="email">Elektron pochta:</label>
            <input type="email" id="email" name="email" placeholder="email@example.com">
        </div>
        
        <div class="form-qator">
            <label for="telefon">Telefon raqami:</label>
            <input type="tel" id="telefon" name="telefon" placeholder="+998 90 123 45 67">
        </div>
        
        <div class="form-qator">
            <label for="yosh">Yoshingiz:</label>
            <input type="number" id="yosh" name="yosh" placeholder="Yoshingizni raqam bilan kiriting">
        </div>
        
        <div class="form-qator">
            <label for="manzil">Manzil:</label>
            <input type="text" id="manzil" name="manzil" placeholder="Yashash joyingiz">
        </div>
        
        <div class="form-qator">
            <label for="haqida">O'zingiz haqingizda:</label>
            <textarea id="haqida" name="haqida" rows="4" placeholder="O'zingiz haqingizda qisqacha ma'lumot bering"></textarea>
        </div>
        
        <button type="submit" class="submit-btn">Ma'lumotlarni yuborish</button>
    </form>
</div>
```

#### 2. Radio va checkbox bilan
```html
<style>
.tanlov-forma {
    max-width: 350px;
    margin: 20px auto;
    padding: 20px;
    background-color: white;
    border-radius: 8px;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
}

.tanlov-guruh {
    margin-bottom: 20px;
}

.tanlov-guruh label {
    display: block;
    margin-bottom: 10px;
    font-weight: bold;
    color: #333;
}

.radio-guruh,
.checkbox-guruh {
    margin-left: 20px;
}

.radio-guruh label,
.checkbox-guruh label {
    display: inline;
    margin-right: 15px;
    font-weight: normal;
    cursor: pointer;
}

.submit-btn {
    background-color: #007bff;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}
</style>

<div class="tanlov-forma">
    <h3>So'rovnoma</h3>
    
    <form>
        <div class="tanlov-guruh">
            <label for="ism">Ismingiz:</label>
            <input type="text" id="ism" name="ism" placeholder="Ismingizni kiriting">
        </div>
        
        <div class="tanlov-guruh">
            <label>Jinsingiz:</label>
            <div class="radio-guruh">
                <label><input type="radio" name="jins" value="erkak"> Erkak</label>
                <label><input type="radio" name="jins" value="ayol"> Ayol</label>
            </div>
        </div>
        
        <div class="tanlov-guruh">
            <label>Sevimli fanlaringiz:</label>
            <div class="checkbox-guruh">
                <label><input type="checkbox" name="fanlar" value="matematika"> Matematika</label><br>
                <label><input type="checkbox" name="fanlar" value="fizika"> Fizika</label><br>
                <label><input type="checkbox" name="fanlar" value="kimyo"> Kimyo</label><br>
                <label><input type="checkbox" name="fanlar" value="biologiya"> Biologiya</label>
            </div>
        </div>
        
        <div class="tanlov-guruh">
            <label for="izoh">Qo'shimcha izoh:</label>
            <textarea id="izoh" name="izoh" rows="3" placeholder="Qo'shimcha fikrlaringizni yozing"></textarea>
        </div>
        
        <button type="submit" class="submit-btn">Javob yuborish</button>
    </form>
</div>
```

#### 3. Sarlavha va placeholder kombinatsiyasi
```html
<style>
.kombinatsiya-forma {
    max-width: 300px;
    margin: 20px auto;
    padding: 20px;
    background: linear-gradient(135deg, #f093fb, #f5576c);
    border-radius: 10px;
    color: white;
}

.kombinatsiya-forma h3 {
    text-align: center;
    margin-bottom: 25px;
}

.form-element {
    margin-bottom: 15px;
}

.form-element label {
    display: block;
    margin-bottom: 5px;
    font-weight: bold;
}

.form-element input,
.form-element textarea {
    width: 100%;
    padding: 10px;
    border: none;
    border-radius: 5px;
    font-size: 16px;
    box-sizing: border-box;
}

.form-element input::placeholder,
.form-element textarea::placeholder {
    color: #ccc;
}

.submit-btn {
    width: 100%;
    background-color: white;
    color: #f5576c;
    padding: 12px;
    border: none;
    border-radius: 5px;
    font-size: 16px;
    font-weight: bold;
    cursor: pointer;
}
</style>

<div class="kombinatsiya-forma">
    <h3>Aloqa formasi</h3>
    
    <form>
        <div class="form-element">
            <label for="ism">Ismingiz:</label>
            <input type="text" id="ism" name="ism" placeholder="Ismingizni kiriting">
        </div>
        
        <div class="form-element">
            <label for="email">Email:</label>
            <input type="email" id="email" name="email" placeholder="email@example.com">
        </div>
        
        <div class="form-element">
            <label for="mavzu">Mavzu:</label>
            <input type="text" id="mavzu" name="mavzu" placeholder="Xabar mavzusi">
        </div>
        
        <div class="form-element">
            <label for="xabar">Xabar:</label>
            <textarea id="xabar" name="xabar" rows="4" placeholder="Xabaringizni bu yerda yozing"></textarea>
        </div>
        
        <button type="submit" class="submit-btn">Xabar yuborish</button>
    </form>
</div>
```

</details>
