<details>
    <summary>Flexbox nima va nima uchun kerak?</summary>

## 7.1 Flexbox Nima va Nima Uchun Kerak?

### Flexbox nima?

**Flexbox** (Flexible Box Layout) - CSS ning zamonaviy layout usuli. Bu elementlarni qator yoki ustun ko'rinishida osongina joylashtirish imkonini beradi.

### Nima uchun Flexbox kerak?

#### 1. Oddiy joylashtirish
- Elementlarni bir qatorda joylashtirish
- Teng masofada tarqatish
- Markazga joylashtirish

#### 2. Responsive dizayn
- Turli ekran o'lchamlarida moslashish
- Elementlarning avtomatik o'lchamlanishi
- Qulay mobil dizayn

#### 3. Muammolarni hal qilish
- Vertikal markazlash
- Teng balandlik
- Elementlar orasidagi teng masofa

### Flexbox vs eski usullar

#### Eski usul (float):
```css
.eski-usul {
    float: left;
    width: 33.33%;
    margin: 0 1%;
}
```

#### Yangi usul (flexbox):
```css
.yangi-usul {
    display: flex;
    justify-content: space-between;
}
```

### Asosiy tushunchalar

#### 1. Flex Container
- `display: flex` xususiyatiga ega element
- Ichida flex itemlar joylashadi
- Boshqa elementlarning joylashuvini boshqaradi

#### 2. Flex Items
- Flex container ichidagi to'g'ridan-to'g'ri farzand elementlar
- Avtomatik ravishda flex qiladi
- O'lcham va joylashuvni o'zgartirish mumkin

### Amaliy misollar

#### 1. Oddiy flexbox
```html
<style>
.oddiy-flex {
    display: flex;
    background-color: #f0f0f0;
    padding: 20px;
    gap: 10px;
}

.flex-item {
    background-color: #4caf50;
    color: white;
    padding: 20px;
    text-align: center;
    flex: 1;
}
</style>

<div class="oddiy-flex">
    <div class="flex-item">Item 1</div>
    <div class="flex-item">Item 2</div>
    <div class="flex-item">Item 3</div>
</div>
```

#### 2. Float vs Flexbox taqqoslash
```html
<style>
.taqqoslash-konteyner {
    margin: 20px 0;
}

.float-usul {
    overflow: hidden;
    background-color: #e3f2fd;
    padding: 15px;
    margin-bottom: 20px;
}

.float-item {
    float: left;
    width: 30%;
    background-color: #2196f3;
    color: white;
    padding: 15px;
    margin: 1.5%;
    text-align: center;
}

.flex-usul {
    display: flex;
    background-color: #e8f5e8;
    padding: 15px;
    gap: 15px;
}

.flex-item {
    flex: 1;
    background-color: #4caf50;
    color: white;
    padding: 15px;
    text-align: center;
}
</style>

<div class="taqqoslash-konteyner">
    <h3>Float usuli (eski):</h3>
    <div class="float-usul">
        <div class="float-item">Float 1</div>
        <div class="float-item">Float 2</div>
        <div class="float-item">Float 3</div>
        <div style="clear: both;"></div>
    </div>
    
    <h3>Flexbox usuli (yangi):</h3>
    <div class="flex-usul">
        <div class="flex-item">Flex 1</div>
        <div class="flex-item">Flex 2</div>
        <div class="flex-item">Flex 3</div>
    </div>
</div>
```

#### 3. Vertikal markazlash
```html
<style>
.markazlash-demo {
    height: 200px;
    background-color: #f5f5f5;
    border: 2px solid #ddd;
    margin: 20px 0;
    display: flex;
    align-items: center;
    justify-content: center;
}

.markazlash-matn {
    background-color: #ff9800;
    color: white;
    padding: 20px;
    text-align: center;
    border-radius: 8px;
}
</style>

<div class="markazlash-demo">
    <div class="markazlash-matn">
        Bu matn gorizontal va vertikal markazda joylashgan!
    </div>
</div>
```

</details>

<details>
    <summary>Flex container va flex items</summary>

## 7.2 Flex Container va Flex Items

### Flex Container

Flex container - `display: flex` yoki `display: inline-flex` xususiyatiga ega element.

#### Flex container yaratish
```css
.flex-konteyner {
    display: flex;
}
```

#### Inline-flex container
```css
.inline-flex-konteyner {
    display: inline-flex;
}
```

### Flex Items

Flex items - flex container ichidagi to'g'ridan-to'g'ri farzand elementlar.

#### Flex item xususiyatlari
```css
.flex-item {
    flex: 1;                    /* Teng o'lcham */
    flex-grow: 1;               /* O'sish */
    flex-shrink: 1;             /* Qisqarish */
    flex-basis: auto;           /* Asosiy o'lcham */
}
```

### Flex Container xususiyatlari

#### 1. Flex-direction - yo'nalish
```css
.flex-direction-row {
    flex-direction: row;        /* Gorizontal (default) */
}

.flex-direction-column {
    flex-direction: column;     /* Vertikal */
}

.flex-direction-row-reverse {
    flex-direction: row-reverse; /* Gorizontal teskari */
}

.flex-direction-column-reverse {
    flex-direction: column-reverse; /* Vertikal teskari */
}
```

#### 2. Flex-wrap - o'rash
```css
.flex-wrap-nowrap {
    flex-wrap: nowrap;          /* O'rash yo'q (default) */
}

.flex-wrap-wrap {
    flex-wrap: wrap;            /* O'rash */
}

.flex-wrap-wrap-reverse {
    flex-wrap: wrap-reverse;    /* Teskari o'rash */
}
```

#### 3. Justify-content - asosiy o'q bo'yicha joylashuv
```css
.justify-start {
    justify-content: flex-start; /* Boshidan */
}

.justify-center {
    justify-content: center;    /* Markazda */
}

.justify-end {
    justify-content: flex-end;  /* Oxiridan */
}

.justify-between {
    justify-content: space-between; /* Oralarida */
}

.justify-around {
    justify-content: space-around;  /* Atrofida */
}

.justify-evenly {
    justify-content: space-evenly;  /* Teng masofada */
}
```

#### 4. Align-items - kross o'q bo'yicha joylashuv
```css
.align-stretch {
    align-items: stretch;       /* Cho'zish (default) */
}

.align-start {
    align-items: flex-start;    /* Yuqoridan */
}

.align-center {
    align-items: center;        /* Markazda */
}

.align-end {
    align-items: flex-end;      /* Pastdan */
}

.align-baseline {
    align-items: baseline;      /* Bazal chiziqda */
}
```

### Amaliy misollar

#### 1. Flex container va items
```html
<style>
.flex-konteyner-demo {
    display: flex;
    background-color: #e8f5e8;
    padding: 20px;
    gap: 15px;
    margin: 20px 0;
}

.flex-item-demo {
    background-color: #2e7d32;
    color: white;
    padding: 20px;
    text-align: center;
    border-radius: 5px;
    flex: 1;
}

.flex-item-katta {
    flex: 2;
    background-color: #4caf50;
}

.flex-item-kichik {
    flex: 0.5;
    background-color: #66bb6a;
}
</style>

<div class="flex-konteyner-demo">
    <div class="flex-item-demo">Oddiy item</div>
    <div class="flex-item-demo flex-item-katta">Katta item (flex: 2)</div>
    <div class="flex-item-demo flex-item-kichik">Kichik item (flex: 0.5)</div>
</div>
```

#### 2. Flex-direction misollari
```html
<style>
.flex-direction-demo {
    display: flex;
    background-color: #f3e5f5;
    padding: 15px;
    gap: 10px;
    margin: 15px 0;
    min-height: 100px;
}

.flex-direction-item {
    background-color: #9c27b0;
    color: white;
    padding: 15px;
    text-align: center;
    flex: 1;
}

.row-demo {
    flex-direction: row;
}

.column-demo {
    flex-direction: column;
}

.row-reverse-demo {
    flex-direction: row-reverse;
}

.column-reverse-demo {
    flex-direction: column-reverse;
}
</style>

<h4>Row (gorizontal):</h4>
<div class="flex-direction-demo row-demo">
    <div class="flex-direction-item">1</div>
    <div class="flex-direction-item">2</div>
    <div class="flex-direction-item">3</div>
</div>

<h4>Column (vertikal):</h4>
<div class="flex-direction-demo column-demo">
    <div class="flex-direction-item">1</div>
    <div class="flex-direction-item">2</div>
    <div class="flex-direction-item">3</div>
</div>

<h4>Row-reverse (gorizontal teskari):</h4>
<div class="flex-direction-demo row-reverse-demo">
    <div class="flex-direction-item">1</div>
    <div class="flex-direction-item">2</div>
    <div class="flex-direction-item">3</div>
</div>

<h4>Column-reverse (vertikal teskari):</h4>
<div class="flex-direction-demo column-reverse-demo">
    <div class="flex-direction-item">1</div>
    <div class="flex-direction-item">2</div>
    <div class="flex-direction-item">3</div>
</div>
```

#### 3. Flex-wrap misollari
```html
<style>
.flex-wrap-demo {
    display: flex;
    background-color: #fff3e0;
    padding: 15px;
    gap: 10px;
    margin: 15px 0;
    max-width: 400px;
}

.flex-wrap-item {
    background-color: #ff9800;
    color: white;
    padding: 15px;
    text-align: center;
    min-width: 120px;
}

.nowrap-demo {
    flex-wrap: nowrap;
}

.wrap-demo {
    flex-wrap: wrap;
}

.wrap-reverse-demo {
    flex-wrap: wrap-reverse;
}
</style>

<h4>No-wrap (o'rash yo'q):</h4>
<div class="flex-wrap-demo nowrap-demo">
    <div class="flex-wrap-item">Item 1</div>
    <div class="flex-wrap-item">Item 2</div>
    <div class="flex-wrap-item">Item 3</div>
    <div class="flex-wrap-item">Item 4</div>
</div>

<h4>Wrap (o'rash):</h4>
<div class="flex-wrap-demo wrap-demo">
    <div class="flex-wrap-item">Item 1</div>
    <div class="flex-wrap-item">Item 2</div>
    <div class="flex-wrap-item">Item 3</div>
    <div class="flex-wrap-item">Item 4</div>
</div>

<h4>Wrap-reverse (teskari o'rash):</h4>
<div class="flex-wrap-demo wrap-reverse-demo">
    <div class="flex-wrap-item">Item 1</div>
    <div class="flex-wrap-item">Item 2</div>
    <div class="flex-wrap-item">Item 3</div>
    <div class="flex-wrap-item">Item 4</div>
</div>
```

</details>

<details>
    <summary>Justify-content va align-items</summary>

## 7.3 Justify-content va Align-items

### Justify-content - asosiy o'q bo'yicha joylashuv

Justify-content elementlarni **asosiy o'q** (main axis) bo'yicha joylashtiradi.

#### Justify-content qiymatlari
```css
.justify-flex-start {
    justify-content: flex-start;    /* Boshidan */
}

.justify-center {
    justify-content: center;        /* Markazda */
}

.justify-flex-end {
    justify-content: flex-end;      /* Oxiridan */
}

.justify-space-between {
    justify-content: space-between; /* Oralarida */
}

.justify-space-around {
    justify-content: space-around;  /* Atrofida */
}

.justify-space-evenly {
    justify-content: space-evenly;  /* Teng masofada */
}
```

### Align-items - kross o'q bo'yicha joylashuv

Align-items elementlarni **kross o'q** (cross axis) bo'yicha joylashtiradi.

#### Align-items qiymatlari
```css
.align-stretch {
    align-items: stretch;           /* Cho'zish (default) */
}

.align-flex-start {
    align-items: flex-start;        /* Yuqoridan */
}

.align-center {
    align-items: center;            /* Markazda */
}

.align-flex-end {
    align-items: flex-end;          /* Pastdan */
}

.align-baseline {
    align-items: baseline;          /* Bazal chiziqda */
}
```

### Asosiy o'q va kross o'q

#### Row yo'nalishida (flex-direction: row):
- **Asosiy o'q**: gorizontal (chapdan o'ngga)
- **Kross o'q**: vertikal (yuqoridan pastga)

#### Column yo'nalishida (flex-direction: column):
- **Asosiy o'q**: vertikal (yuqoridan pastga)
- **Kross o'q**: gorizontal (chapdan o'ngga)

### Amaliy misollar

#### 1. Justify-content misollari
```html
<style>
.justify-demo {
    display: flex;
    background-color: #e3f2fd;
    padding: 15px;
    gap: 10px;
    margin: 15px 0;
    min-height: 80px;
}

.justify-item {
    background-color: #2196f3;
    color: white;
    padding: 15px;
    text-align: center;
    min-width: 80px;
}

.justify-start {
    justify-content: flex-start;
}

.justify-center {
    justify-content: center;
}

.justify-end {
    justify-content: flex-end;
}

.justify-between {
    justify-content: space-between;
}

.justify-around {
    justify-content: space-around;
}

.justify-evenly {
    justify-content: space-evenly;
}
</style>

<h4>Flex-start (boshidan):</h4>
<div class="justify-demo justify-start">
    <div class="justify-item">1</div>
    <div class="justify-item">2</div>
    <div class="justify-item">3</div>
</div>

<h4>Center (markazda):</h4>
<div class="justify-demo justify-center">
    <div class="justify-item">1</div>
    <div class="justify-item">2</div>
    <div class="justify-item">3</div>
</div>

<h4>Flex-end (oxiridan):</h4>
<div class="justify-demo justify-end">
    <div class="justify-item">1</div>
    <div class="justify-item">2</div>
    <div class="justify-item">3</div>
</div>

<h4>Space-between (oralarida):</h4>
<div class="justify-demo justify-between">
    <div class="justify-item">1</div>
    <div class="justify-item">2</div>
    <div class="justify-item">3</div>
</div>

<h4>Space-around (atrofida):</h4>
<div class="justify-demo justify-around">
    <div class="justify-item">1</div>
    <div class="justify-item">2</div>
    <div class="justify-item">3</div>
</div>

<h4>Space-evenly (teng masofada):</h4>
<div class="justify-demo justify-evenly">
    <div class="justify-item">1</div>
    <div class="justify-item">2</div>
    <div class="justify-item">3</div>
</div>
```

#### 2. Align-items misollari
```html
<style>
.align-demo {
    display: flex;
    background-color: #f3e5f5;
    padding: 15px;
    gap: 10px;
    margin: 15px 0;
    height: 120px;
}

.align-item {
    background-color: #9c27b0;
    color: white;
    padding: 10px;
    text-align: center;
    min-width: 60px;
}

.align-item-1 {
    height: 40px;
}

.align-item-2 {
    height: 60px;
}

.align-item-3 {
    height: 80px;
}

.align-stretch {
    align-items: stretch;
}

.align-start {
    align-items: flex-start;
}

.align-center {
    align-items: center;
}

.align-end {
    align-items: flex-end;
}

.align-baseline {
    align-items: baseline;
}
</style>

<h4>Stretch (cho'zish):</h4>
<div class="align-demo align-stretch">
    <div class="align-item align-item-1">1</div>
    <div class="align-item align-item-2">2</div>
    <div class="align-item align-item-3">3</div>
</div>

<h4>Flex-start (yuqoridan):</h4>
<div class="align-demo align-start">
    <div class="align-item align-item-1">1</div>
    <div class="align-item align-item-2">2</div>
    <div class="align-item align-item-3">3</div>
</div>

<h4>Center (markazda):</h4>
<div class="align-demo align-center">
    <div class="align-item align-item-1">1</div>
    <div class="align-item align-item-2">2</div>
    <div class="align-item align-item-3">3</div>
</div>

<h4>Flex-end (pastdan):</h4>
<div class="align-demo align-end">
    <div class="align-item align-item-1">1</div>
    <div class="align-item align-item-2">2</div>
    <div class="align-item align-item-3">3</div>
</div>

<h4>Baseline (bazal chiziqda):</h4>
<div class="align-demo align-baseline">
    <div class="align-item align-item-1">1</div>
    <div class="align-item align-item-2">2</div>
    <div class="align-item align-item-3">3</div>
</div>
```

#### 3. Kombinatsiya misoli
```html
<style>
.kombinatsiya-demo {
    display: flex;
    background-color: #e8f5e8;
    padding: 20px;
    gap: 15px;
    margin: 20px 0;
    height: 150px;
}

.kombinatsiya-item {
    background-color: #4caf50;
    color: white;
    padding: 20px;
    text-align: center;
    flex: 1;
}

.markazlash-demo {
    justify-content: center;
    align-items: center;
}

.ust-bosh-demo {
    justify-content: flex-start;
    align-items: flex-start;
}

.past-oxir-demo {
    justify-content: flex-end;
    align-items: flex-end;
}

.teng-tarqatish-demo {
    justify-content: space-between;
    align-items: center;
}
</style>

<h4>Markazda joylashuv:</h4>
<div class="kombinatsiya-demo markazlash-demo">
    <div class="kombinatsiya-item">Markazda</div>
    <div class="kombinatsiya-item">Markazda</div>
</div>

<h4>Yuqori chapda:</h4>
<div class="kombinatsiya-demo ust-bosh-demo">
    <div class="kombinatsiya-item">Yuqori</div>
    <div class="kombinatsiya-item">Chap</div>
</div>

<h4>Pastki o'ngda:</h4>
<div class="kombinatsiya-demo past-oxir-demo">
    <div class="kombinatsiya-item">Pastki</div>
    <div class="kombinatsiya-item">O'ng</div>
</div>

<h4>Teng tarqatish va markaz:</h4>
<div class="kombinatsiya-demo teng-tarqatish-demo">
    <div class="kombinatsiya-item">Teng</div>
    <div class="kombinatsiya-item">Tarqatish</div>
    <div class="kombinatsiya-item">Markaz</div>
</div>
```

</details>

<details>
    <summary>Flex-direction va flex-wrap</summary>

## 7.4 Flex-direction va Flex-wrap

### Flex-direction - yo'nalish

Flex-direction flex container ichidagi elementlarning yo'nalishini belgilaydi.

#### Flex-direction qiymatlari
```css
.flex-row {
    flex-direction: row;            /* Gorizontal (default) */
}

.flex-column {
    flex-direction: column;         /* Vertikal */
}

.flex-row-reverse {
    flex-direction: row-reverse;    /* Gorizontal teskari */
}

.flex-column-reverse {
    flex-direction: column-reverse; /* Vertikal teskari */
}
```

### Flex-wrap - o'rash

Flex-wrap elementlar konteyner o'lchamidan chiqib ketsa, qanday ishlashini belgilaydi.

#### Flex-wrap qiymatlari
```css
.flex-nowrap {
    flex-wrap: nowrap;              /* O'rash yo'q (default) */
}

.flex-wrap {
    flex-wrap: wrap;                /* O'rash */
}

.flex-wrap-reverse {
    flex-wrap: wrap-reverse;        /* Teskari o'rash */
}
```

### Flex-flow - qisqa yozish

Flex-flow flex-direction va flex-wrap ni bir vaqtda belgilash uchun qisqa yozish usuli.

```css
.flex-flow-short {
    flex-flow: row wrap;            /* flex-direction: row; flex-wrap: wrap; */
    flex-flow: column nowrap;       /* flex-direction: column; flex-wrap: nowrap; */
    flex-flow: row-reverse wrap;    /* flex-direction: row-reverse; flex-wrap: wrap; */
}
```

### Amaliy misollar

#### 1. Flex-direction to'liq misol
```html
<style>
.direction-demo {
    display: flex;
    background-color: #fff3e0;
    padding: 15px;
    gap: 10px;
    margin: 15px 0;
    min-height: 100px;
}

.direction-item {
    background-color: #ff9800;
    color: white;
    padding: 15px;
    text-align: center;
    flex: 1;
    min-width: 80px;
}

.row-demo {
    flex-direction: row;
}

.column-demo {
    flex-direction: column;
    height: 200px;
}

.row-reverse-demo {
    flex-direction: row-reverse;
}

.column-reverse-demo {
    flex-direction: column-reverse;
    height: 200px;
}
</style>

<h4>Row (gorizontal):</h4>
<div class="direction-demo row-demo">
    <div class="direction-item">1</div>
    <div class="direction-item">2</div>
    <div class="direction-item">3</div>
</div>

<h4>Column (vertikal):</h4>
<div class="direction-demo column-demo">
    <div class="direction-item">1</div>
    <div class="direction-item">2</div>
    <div class="direction-item">3</div>
</div>

<h4>Row-reverse (gorizontal teskari):</h4>
<div class="direction-demo row-reverse-demo">
    <div class="direction-item">1</div>
    <div class="direction-item">2</div>
    <div class="direction-item">3</div>
</div>

<h4>Column-reverse (vertikal teskari):</h4>
<div class="direction-demo column-reverse-demo">
    <div class="direction-item">1</div>
    <div class="direction-item">2</div>
    <div class="direction-item">3</div>
</div>
```

#### 2. Flex-wrap to'liq misol
```html
<style>
.wrap-demo {
    display: flex;
    background-color: #fce4ec;
    padding: 15px;
    gap: 10px;
    margin: 15px 0;
    max-width: 300px;
}

.wrap-item {
    background-color: #e91e63;
    color: white;
    padding: 15px;
    text-align: center;
    min-width: 80px;
    flex: 1;
}

.nowrap-demo {
    flex-wrap: nowrap;
}

.wrap-demo-wrap {
    flex-wrap: wrap;
}

.wrap-reverse-demo {
    flex-wrap: wrap-reverse;
}
</style>

<h4>Nowrap (o'rash yo'q):</h4>
<div class="wrap-demo nowrap-demo">
    <div class="wrap-item">Item 1</div>
    <div class="wrap-item">Item 2</div>
    <div class="wrap-item">Item 3</div>
    <div class="wrap-item">Item 4</div>
    <div class="wrap-item">Item 5</div>
</div>

<h4>Wrap (o'rash):</h4>
<div class="wrap-demo wrap-demo-wrap">
    <div class="wrap-item">Item 1</div>
    <div class="wrap-item">Item 2</div>
    <div class="wrap-item">Item 3</div>
    <div class="wrap-item">Item 4</div>
    <div class="wrap-item">Item 5</div>
</div>

<h4>Wrap-reverse (teskari o'rash):</h4>
<div class="wrap-demo wrap-reverse-demo">
    <div class="wrap-item">Item 1</div>
    <div class="wrap-item">Item 2</div>
    <div class="wrap-item">Item 3</div>
    <div class="wrap-item">Item 4</div>
    <div class="wrap-item">Item 5</div>
</div>
```

#### 3. Flex-flow kombinatsiya
```html
<style>
.flow-demo {
    display: flex;
    background-color: #e0f2f1;
    padding: 15px;
    gap: 10px;
    margin: 15px 0;
    max-width: 400px;
}

.flow-item {
    background-color: #00695c;
    color: white;
    padding: 15px;
    text-align: center;
    min-width: 80px;
    flex: 1;
}

.flow-row-wrap {
    flex-flow: row wrap;
}

.flow-column-wrap {
    flex-flow: column wrap;
    height: 200px;
}

.flow-row-reverse-wrap {
    flex-flow: row-reverse wrap;
}

.flow-column-reverse-wrap {
    flex-flow: column-reverse wrap;
    height: 200px;
}
</style>

<h4>Flex-flow: row wrap</h4>
<div class="flow-demo flow-row-wrap">
    <div class="flow-item">1</div>
    <div class="flow-item">2</div>
    <div class="flow-item">3</div>
    <div class="flow-item">4</div>
    <div class="flow-item">5</div>
    <div class="flow-item">6</div>
</div>

<h4>Flex-flow: column wrap</h4>
<div class="flow-demo flow-column-wrap">
    <div class="flow-item">1</div>
    <div class="flow-item">2</div>
    <div class="flow-item">3</div>
    <div class="flow-item">4</div>
    <div class="flow-item">5</div>
</div>

<h4>Flex-flow: row-reverse wrap</h4>
<div class="flow-demo flow-row-reverse-wrap">
    <div class="flow-item">1</div>
    <div class="flow-item">2</div>
    <div class="flow-item">3</div>
    <div class="flow-item">4</div>
    <div class="flow-item">5</div>
</div>

<h4>Flex-flow: column-reverse wrap</h4>
<div class="flow-demo flow-column-reverse-wrap">
    <div class="flow-item">1</div>
    <div class="flow-item">2</div>
    <div class="flow-item">3</div>
    <div class="flow-item">4</div>
    <div class="flow-item">5</div>
</div>
```

</details>

<details>
    <summary>Responsive layout yaratish</summary>

## 7.5 Responsive Layout Yaratish

### Responsive layout nima?

**Responsive layout** - turli ekran o'lchamlarida (kompyuter, planshet, telefon) yaxshi ko'rinadigan layout.

### Media queries bilan responsive

#### 1. Asosiy media queries
```css
/* Kichik ekranlar (telefon) */
@media (max-width: 768px) {
    .responsive-container {
        flex-direction: column;
    }
}

/* O'rta ekranlar (planshet) */
@media (min-width: 769px) and (max-width: 1024px) {
    .responsive-container {
        flex-wrap: wrap;
    }
}

/* Katta ekranlar (kompyuter) */
@media (min-width: 1025px) {
    .responsive-container {
        flex-direction: row;
        flex-wrap: nowrap;
    }
}
```

#### 2. Oddiy responsive breakpoint
```css
/* Mobil */
@media (max-width: 600px) {
    .mobile-layout {
        flex-direction: column;
    }
}

/* Planshet va katta */
@media (min-width: 601px) {
    .desktop-layout {
        flex-direction: row;
    }
}
```

### Responsive flexbox xususiyatlari

#### 1. Flex-grow - o'sish
```css
.flex-grow-item {
    flex-grow: 1;               /* Teng o'sish */
}

.flex-grow-katta {
    flex-grow: 2;               /* Ikki marta tez o'sish */
}

.flex-grow-kichik {
    flex-grow: 0.5;             /* Yarim tez o'sish */
}
```

#### 2. Flex-shrink - qisqarish
```css
.flex-shrink-item {
    flex-shrink: 1;             /* Oddiy qisqarish */
}

.flex-shrink-yo'q {
    flex-shrink: 0;             /* Qisqarmaslik */
}

.flex-shrink-tez {
    flex-shrink: 2;             /* Ikki marta tez qisqarish */
}
```

#### 3. Flex-basis - asosiy o'lcham
```css
.flex-basis-item {
    flex-basis: 200px;          /* Asosiy kenglik */
}

.flex-basis-foiz {
    flex-basis: 33.33%;         /* Asosiy foiz */
}

.flex-basis-auto {
    flex-basis: auto;           /* Avtomatik (default) */
}
```

### Amaliy misollar

#### 1. Responsive kartochkalar
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
    min-width: 250px;
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
@media (max-width: 768px) {
    .responsive-kartochkalar {
        flex-direction: column;
        gap: 15px;
    }
    
    .kartochka {
        min-width: auto;
    }
}

/* Planshet uchun */
@media (min-width: 769px) and (max-width: 1024px) {
    .kartochka {
        flex: 1 1 calc(50% - 10px);
        max-width: calc(50% - 10px);
    }
}
</style>

<div class="responsive-kartochkalar">
    <div class="kartochka">
        <h3>HTML</h3>
        <p>HTML web-sahifalarning asosini tashkil qiladi. U sahifa strukturasi va mazmunini belgilaydi.</p>
    </div>
    
    <div class="kartochka">
        <h3>CSS</h3>
        <p>CSS web-sahifalarni chiroyli qiladi. Ranglar, shriftlar va layout CSS orqali amalga oshiriladi.</p>
    </div>
    
    <div class="kartochka">
        <h3>JavaScript</h3>
        <p>JavaScript web-sahifalarni interaktiv qiladi. Foydalanuvchi harakatlariga javob beradi.</p>
    </div>
</div>
```

#### 2. Responsive navigatsiya
```html
<style>
.responsive-nav {
    background-color: #2c3e50;
    padding: 15px 0;
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
    padding: 10px 0;
    transition: color 0.3s ease;
}

.nav-menu a:hover {
    color: #3498db;
}

/* Mobil uchun */
@media (max-width: 768px) {
    .nav-container {
        flex-direction: column;
        gap: 15px;
    }
    
    .nav-menu {
        flex-direction: column;
        gap: 15px;
        text-align: center;
    }
    
    .nav-menu li {
        margin: 0;
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
            <li><a href="#">Aloqa</a></li>
        </ul>
    </div>
</nav>
```

#### 3. Responsive layout (header, main, sidebar)
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
}

.layout-sidebar {
    flex: 1;
    background-color: #f8f9fa;
    padding: 20px;
    border: 1px solid #e0e0e0;
    border-radius: 8px;
}

.layout-footer {
    background-color: #2c3e50;
    color: white;
    padding: 15px;
    text-align: center;
}

/* Mobil uchun */
@media (max-width: 768px) {
    .layout-main {
        flex-direction: column;
    }
    
    .layout-content,
    .layout-sidebar {
        flex: none;
    }
    
    .layout-sidebar {
        order: -1; /* Sidebar yuqoriga ko'tariladi */
    }
}

/* Planshet uchun */
@media (min-width: 769px) and (max-width: 1024px) {
    .layout-main {
        flex-wrap: wrap;
    }
    
    .layout-content {
        flex: 1 1 100%;
        margin-bottom: 20px;
    }
    
    .layout-sidebar {
        flex: 1 1 calc(50% - 10px);
    }
}
</style>

<div class="responsive-layout">
    <header class="layout-header">
        <h1>Responsive Layout</h1>
        <p>Flexbox bilan responsive dizayn</p>
    </header>
    
    <main class="layout-main">
        <div class="layout-content">
            <h2>Asosiy mazmun</h2>
            <p>Bu yerda sahifaning asosiy mazmuni joylashadi. Flexbox yordamida responsive layout yaratilgan.</p>
            
            <h3>Responsive xususiyatlar:</h3>
            <ul>
                <li>Mobil: Vertikal layout</li>
                <li>Planshet: Qismli o'rash</li>
                <li>Desktop: To'liq gorizontal layout</li>
            </ul>
        </div>
        
        <div class="layout-sidebar">
            <h3>Yon panel</h3>
            <ul>
                <li><a href="#">Link 1</a></li>
                <li><a href="#">Link 2</a></li>
                <li><a href="#">Link 3</a></li>
                <li><a href="#">Link 4</a></li>
            </ul>
        </div>
    </main>
    
    <footer class="layout-footer">
        <p>&copy; 2024 Responsive Layout misoli</p>
    </footer>
</div>
```

#### 4. Responsive galereya
```html
<style>
.responsive-galereya {
    display: flex;
    flex-wrap: wrap;
    gap: 15px;
    padding: 20px;
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
}

.galereya-item h3 {
    color: #1976d2;
    margin: 0;
}

/* Mobil uchun */
@media (max-width: 600px) {
    .galereya-item {
        flex: 1 1 100%;
        min-width: auto;
    }
}

/* Kichik planshet uchun */
@media (min-width: 601px) and (max-width: 900px) {
    .galereya-item {
        flex: 1 1 calc(50% - 8px);
    }
}

/* Katta planshet va desktop uchun */
@media (min-width: 901px) {
    .galereya-item {
        flex: 1 1 calc(33.33% - 10px);
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
</div>
```

</details>
