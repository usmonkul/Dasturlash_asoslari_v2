# JavaScript Asoslari - Uy Ish va Chellenjlar
## Darslik 1 Davomi

---

## 📋 Umumiy Ko'rsatmalar

**MUHIM:** 
- Har doim `let` yoki `const` ishlating! ❌ `var` dan foydalanmang!
- Barcha kodni brauzerda console da test qiling!
- Har bir vazifa uchun HTML fayl yarating va JavaScript kodini `<script>` tag ichida yozing!

---

## 📚 Dars Bo'yicha Mashqlar

### 🎯 1-dars: JavaScript va Browser Console

**Mashqlar (Har birini HTML faylda kod qiling!):**

#### Mashq 1: Console bilan tanishing
1. Chrome brauzerini oching va **F12** yoki **Ctrl+Shift+I** bosing
2. Console tabga o'ting va quyidagi kodlarni yozing:
   - `console.log("Salom JavaScript!")`
   - `console.log(2024)`
   - `alert("Bu sizning birinchi JavaScript kodingiz!")`
   - `console.clear()` - kodini ham sinab ko'ring

**Natija:** Har xil turdagi xabarlar ekranda ko'rinishi kerak.

#### Mashq 2: Interaktivlik yaratish
1. `prompt()` funksiyasi yordamida foydalanuvchi ismini so'rang
2. Olingan ismni console ga chiqaring
3. "Salom, [Foydalanuvchi ismi]! JavaScript ga xush kelibsiz!" desplay qiling

**Qadamlar:**
- `let foydalanuvchiIsmi = prompt("Ismingizni kiriting:");`
- Natijani console ga chiqarish
- Alert bilan xabar ko'rsatish

#### Mashq 3: JavaScript ichida HTML
HTML fayl yarating va JavaScript kodini `<script>` tag ichida yozing:
```html
<!DOCTYPE html>
<html>
<head>
    <title>JavaScript Learning</title>
</head>
<body>
    <h1>JavaScript ko'rgan keling!</h1>
    <script>
        // JavaScript kodingizni bu yerga yozing
        console.log("HTML va JavaScript birgalikda ishlayapti!");
        alert("Sahifa ochildi!");
    </script>
</body>
</html>
```

---

### 🔢 2-dars: Variables (O'zgaruvchilar)

**Modern JavaScript Rules:**
- ✅ `let` - o'zgarmas qiymatlar uchun
- ✅ `const` - hech vaqt o'zgarmaydigan qiymatlar uchun  
- ❌ `var` - eski usul, ishlatmang!

#### Mashq 1: Shaxsiy ma'lumotlar
**Vazifa:** O'zingiz haqingizda 5 ta ma'lumotni variable sifatida saqlang va console ga chiqaring.

**Talablari:**
- `let` bilan `ism`, `familiya`, `yosh`, `maktab`, `sevimliFan` variables yarating
- Har biriga real qiymat bering
- `console.log()` yordamida barcha ma'lumotlarni ko'rsating
- `console.table()` ile tabular formatda ko'rsating

#### Mashq 2: Const va Let farqi
**Vazifa:** const va let ning farqini amaliy ko'rsatish.

**Yechim qadamları:**
1. `const maktabNomi = "15-maktab"` yarating
2. `let sinf = 9` yarating  
3. `sinf = 10` - qiymatni o'zgartiring
4. `maktabNomi = "10-maktab"` - sinab qarang (xato chiqishi kerak!)
5. Natijalarni console ga chiqaring

#### Mashq 3: Matematik calculator
**Vazifa:** Oddiy matematik calculator yasang.

**Steps:**
1. `let a = 15`, `let b = 5` yarating
2. Matematik operatsiyalar: qo'shish, ayirish, ko'paytish, bo'lish
3. Har bir natijani alohida variable ga saqlang
4. Console ga chiqaring: "15 + 5 = 20" formatda

---

### 📊 3-dars: Ma'lumot Turlari

#### Mashq 1: Type checking adventure
**Vazifa:** Har xil data types bilan experimentlar qiling.

**Test qilinadigan tiplar:**
```javascript
// Quyidagi variables larni yarating va har birining type ini tekshiring:
let userName = "Akmal";           // string
let userAge = 20;                 // number  
let isStudent = true;             // boolean
let userMoney = 99.99;            // number (decimal)
let userPhone = "995551234567";   // string (number ko'rinadigan, lekin string!)
```

**Vazifa:** Har bir variable uchun `typeof()` tekshiruvi va natijani console ga chiqarish.

#### Mashq 2: Real-life scenarios
**Scenario:** Talabalar uchun dastur yozish

**Ma'lumotlar:**
- Talaba ismi (string)
- Talaba yoshi (number)  
- Talaba stipendiya oladimi (boolean)
- Talaba GPA (number)
- Talaba telefon raqami (string)

**Vazifa:** 
1. 3 ta talaba ma'lumotlarini yarating
2. Har birining data type ini tekshiring
3. Agar type noto'g'ri bo'lsa, tuzating
4. Console da hamma talaba ma'lumotlarini ko'rsating

#### Mashq 3: Type conversion challenge
**Challenge:** Strings va numbers o'rtasida conversion

**Steps:**
1. `let score = "85"` - string number yarating
2. O'qituvchi bonus berdi: +10 point
3. String ni number ga aylantiring
4. Bonus qo'shing
5. Natijani string ga qaytarib, "Sizning yangi balingiz: 95" formatda chiqaring

---

### ⚡ 4-dars: Matematik va Taqqoslash Amallari

#### Mashq 1: Grade Calculator  
**Vazifa:** Talaba baholarini hisoblash uchun system yasang.

**Requirements:**
- 5 ta fan uchun ball yozing (number variables)
- Umumiy score ni hisoblang (sum)
- O'rtacha balını hisoblang (average)
- Percentage ni hisoblang (out of 100)
- Qoldiq bilan bo'lish (%) ni ishlatib, kabisa yilini aniqlang

#### Mashq 2: Comparison operators playground
**Real Example:** Cinema ticket system yasang.

**Data:**
- `let userAge = 16`
- `let ticketPrice = 15000`
- `let userMoney = 20000`
- `let isStudent = true`

**Tekshiruvlar:**
1. User yoshi 18 dan katta/kichik (`>=`, `<`)
2. User da enough pul bormi (`>=`)
3. User studentmi (`===`)
4. Student discount (50%) uchun condition

#### Mashq 3: Logical Operators Master
**Challenge:** School admission system

**Conditions:**
- Talaba yoshi kamida 6 (`>=`)
- Talaba yoshi maksimum 18 dan kichik (`<`)
- Talaba tug'ilgan yili 2017 dan katta (`birthYear > 2017`)
- Talaba vaccination complete (`hasVaccines === true`)

**Vazifa:** 
- AND (`&&`) opertor bilan admission criteria yozing
- OR (`||`) operator bilan alternative admission yozing  
- NOT (`!`) operator bilan rejection criteria yozing

---

### 🎯 5-dars: Complex Operations

#### Mashq 1: Shopping Cart Calculator
**Real-life simulation:** Online shop

**Items va Prices:**
- `let bookPrice = 25000`
- `let penPrice = 5000` 
- `let notebookPrice = 15000`
- `let calculatorPrice = 75000`

**User ma'lumotlari:**
- `let userBudget = 100000`
- `let isStudent = true`

**Calculations:**
1. Total price hisoblash
2. Student discount (20%) hisoblash
3. Budget dan kam/ko'p ekanligini tekshirish
4. Qoldiq pulni hisoblash (budget - total)

#### Mashq 2: Weather App Logic
**Real-world scenario:** Simple weather conditions

**Weather data:**
- `let temperature = 25` (Celsius)
- `let isSunny = true`
- `let isWeekend = false`
- `let timeOfDay = "afternoon"`

**Logic qiling:**
1. Temperatura yukori (>20) va sunny → Beach weather
2. Temperatura past (<10) yoki rain → Indoor activity  
3. Weekend va good weather → Picnic suggestion
4. Afternoon va hot (>30) → Drink more water

---

## 🚀 Chellenj PROYEKTLAR

### 🎖️ Bronza Chellenji: Shaxsiy Ma'lumotlar Boshqaruvchisi

**Loyiha Maqsadi:** O'zingiz haqingizda ma'lumotlarni saqlash va hisoblash tizimi

**Kerakli Xususiyatlar:**

#### 1. Shaxsiy Ma'lumotlar
- Ism, familiya, yosh, maktab, sinf
- Telefon raqami, manzil
- Tug'ilgan yili va oyi

#### 2. Akademik Hisob-kitoblar
- 5 ta fan uchun baholar (Matematika, Fizika, Kimyo, Biologiya, Ingliz tili)
- O'rtacha baho hisoblash (GPA)
- Eng yuqori va eng past baholar
- Umumiy ball

#### 3. Yutuqlar Kiritish
- Sport yutuqlari (boolean: true/false)
- Olimpiada ishtiroki
- Jamiyat faoliyati
- Maxsus mukofotlar

#### 4. Oddiy Statistika
- Yoshlar guruhiga qarab tasniflash
- Fanlar bo'yicha o'rtacha baholar
- Yil davomida progress

**Texnik Talablar:**
- Barcha o'zgaruvchilar `let`/`const` bilan yozilgan
- Barcha ma'lumot turlari ishlatilgan (string, number, boolean)
- Console da barcha ma'lumotlar ko'rsatilgan
- Oddiy hisob-kitoblar va taqqoslashlar

**Qadamlar:**
1. HTML fayl yarating va JavaScript kodini yozing
2. Shaxsiy ma'lumotlar uchun o'zgaruvchilar yarating
3. Baholar uchun o'zgaruvchilar yarating
4. O'rtacha baho hisoblash formulasini yozing
5. Yutuqlar uchun boolean o'zgaruvchilar yarating
6. Barcha ma'lumotlarni console ga chiqaring

### 🥈 Kumush Chellenji: Maktab Boshqaruv Tizimi

**Loyiha Maqsadi:** Kichik maktab boshqaruvi dasturi

**Asosiy Xususiyatlar:**

#### 1. Talaba Ro'yxatdan O'tkazish
**Ma'lumotlar:**
- Ism, familiya, yosh
- Sinf, talaba ID raqami
- Tug'ilgan yili
- Manzil

**Hisob-kitoblar:**
- Ro'yxatdan o'tkazish to'lovi (yoshga qarab)
- 6 yoshdan kichik - 50% chegirma
- 15 yoshdan katta - 25% qo'shimcha to'lov

**Tekshiruvlar:**
- Yoshi 6 dan katta va 18 dan kichik bo'lishi kerak
- Tug'ilgan yili 2017 dan katta bo'lishi kerak

#### 2. Akademik Kuzatish
**Baholar Tizimi:**
- 8 ta fan: Matematika, Fizika, Kimyo, Biologiya, Ingliz tili, O'zbek tili, Tarix, Geografiya
- Har bir fan uchun 1-5 baho
- O'rtacha baho hisoblash
- Baho tasnifi: 5=A, 4=B, 3=C, 2=D, 1=F

**Progress Kuzatish:**
- Sinfdan sinfga o'tish (yil oxirida)
- Keyingi yil sinfini aniqlash
- Akademik yutuqlar

#### 3. Biznes Mantiq
**Yosh Tekshiruvi:**
```javascript
let ageEligible = (age >= 6 && age <= 18);
```

**Sinf Progression:**
```javascript
let nextYearClass = currentClass + 1;
```

**To'lov Hisob-kitoblari:**
- Asosiy to'lov: 500,000 so'm
- Chegirmalar va qo'shimcha to'lovlar
- Oylik to'lovlar

**Qo'shimcha Xususiyatlar:**
- Talabalar o'rtasida taqqoslash (yosh, baholar, yutuqlar)
- Bir nechta talaba bilan ishlash
- Stipendiya uchun shartlar

**Qadamlar:**
1. Talaba ma'lumotlari uchun o'zgaruvchilar yarating
2. Yoshi tekshiruv logikasini yozing
3. Baholar tizimini yarating
4. To'lov hisob-kitoblarini yozing
5. Stipendiya shartlarini aniqlang
6. Console da barcha natijalarni ko'rsating

---

## 📝 Yakunlash Ro'yxati

**Har bir dars uchun:**
- [ ] Kod HTML faylda yozildi
- [ ] `let`/`const` ishlatildi (`var` ishlatilmadi!)
- [ ] Console da natijalar ko'rildi
- [ ] Haqiqiy ma'lumotlar bilan ishlagan
- [ ] Xatolarni boshqarish qo'shildi

**Final Loyiha uchun:**
- [ ] Zamonaviy JavaScript amaliyotlari ishlatildi
- [ ] Barcha ma'lumot turlari qamrab olindi
- [ ] Murakkab hisob-kitoblar amalga oshirildi
- [ ] Mantiqiy operatorlar to'g'ri ishlatildi
- [ ] Haqiqiy dunyo senariylari simulyatsiya qilindi

**Baholash Mezonlari:**
- ✅ **A'lo:** Oltin Chellenjsi bonus xususiyatlar bilan yakunlandi
- ✅ **Yaxshi:** Kumush Chellenjsi ko'pchilik xususiyatlar bilan ishlaydi
- ✅ **O'tdi:** Bronza Chellenjsi asosiy funksionallik bilan
- ❌ **O'tmadi:** To'liq bo'lmagan uy vazifasi yoki eskirgan amaliyotlar ishlatilgan

---

**🎯 Maqsad:** JavaScript da mustaqil ishlash va haqiqiy dunyo ilovalarini yaratish!

**⏰ Vaqt:** Bu vazifalar 1 hafta ichida yakunlanishi kerak!

**💡 Maslahat:** Chellenj proyektlarni bosqichma-bosqich bajaring. Avval bronza Chellenjsini to'liq tugatib, keyin keyingisiga o'ting!