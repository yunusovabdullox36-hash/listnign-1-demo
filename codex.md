# IELTS Listening Practice loyiha hujjati

Ushbu loyiha bitta HTML faylda ishlaydigan IELTS Listening mashq sahifasi. Sayt lokal holatda ochiladi, audio bilan ishlaydi va foydalanuvchi javoblarini tekshirib, natijani modal oynada ko'rsatadi.

## Loyiha tarkibi

- `index.html` - butun interfeys, stillar va JavaScript logikasi shu fayl ichida
- `56658.mp3` - listening audio fayli
- `codex.md` - loyiha bo'yicha qisqa texnik va foydalanish hujjati

## Hozirgi funksiyalar

Sahifada quyidagi imkoniyatlar bor:

- yuqorida `sticky audio player`
- `play/pause` tugmasi
- `5 soniya oldinga` va `5 soniya orqaga` o'tish
- `progress bar` orqali audio ichida kerakli joyga sakrash
- `volume` boshqaruvi
- `speed` tanlash: `0.75x`, `1x`, `1.25x`, `1.5x`
- `4 ta part` bo'yicha savollarni alohida ko'rsatish
- `input`, `radio`, `select` turidagi savollar
- `Javoblarni tekshirish` tugmasi
- `band score` hisoblash
- `result modal` ichida umumiy natija, xatolar va part bo'yicha kesim
- mobil qurilmalar uchun responsive layout
- matnni belgilaganda ko'rinadigan `highlight/selection` rangi

## Highlight muammosi va tuzatish

Oldin matnni sichqoncha bilan belgilaganda aniq rangli highlight ko'rinmas edi. Bunga sabab sahifada global `::selection` stili yozilmagan edi.

Hozir `index.html` ichida quyidagilar qo'shildi:

- `--selection-bg`
- `--selection-text`
- global `::selection`
- global `::-moz-selection`

Natija:

- matn belgilaganda ko'k rangli fon chiqadi
- tanlangan matn kontrastli ko'rinadi
- Chrome, Edge va Firefox'da selection aniq ko'rinadi

## Saytni ishga tushirish

1. Papka ichida `index.html` va `56658.mp3` birga bo'lishi kerak.
2. `index.html` faylini brauzerda oching.
3. Audio panel tepada, savollar pastda chiqadi.

## Foydalanish tartibi

1. Audio'ni `Play` bilan ishga tushiring.
2. Kerakli `Part` ni tanlang.
3. Savollarga javob kiriting.
4. Kerak bo'lsa audio tezligini o'zgartiring yoki 5 soniya oldinga-orqaga o'ting.
5. Ish tugagach `Javoblarni tekshirish` tugmasini bosing.
6. Natijani modal oynada ko'ring.

## Natija qanday ko'rsatiladi

Tekshiruvdan keyin foydalanuvchi quyidagilarni ko'radi:

- nechta savol to'g'ri ishlangani
- nechta savol noto'g'ri bo'lgani
- nechta savol tashlab ketilgani
- `IELTS Band Score`
- har bir `Part` bo'yicha natija
- xato berilgan javoblar ro'yxati

## Ball hisoblash

Loyiha `Listening raw score -> band score` usulida ishlaydi. Har bir to'g'ri javob `1 point`.

Asosiy mapping:

- `39-40 = 9.0`
- `37-38 = 8.5`
- `35-36 = 8.0`
- `32-34 = 7.5`
- `30-31 = 7.0`
- `26-29 = 6.5`
- `23-25 = 6.0`
- `18-22 = 5.5`
- `16-17 = 5.0`
- `13-15 = 4.5`
- `11-12 = 4.0`

## Dizayn va texnik tuzilma

Loyiha alohida framework ishlatmaydi. Hammasi oddiy:

- `HTML`
- `CSS`
- `Vanilla JavaScript`

Asosiy interfeys qismlari:

- `#player-bar`
- `#progress-track`
- `.part-card`
- `#check-btn`
- `#result-modal-overlay`
- `#result-modal`

## Mobil moslashuv

Sahifa responsive holatda yozilgan. Kichik ekranlarda:

- audio panel ixcham ko'rinadi
- tugmalar ustma-ust tushadi
- input va select elementlar kengayadi
- part tugmalari qulay bosiladigan bo'ladi

## Agar muammo chiqsa

### Audio ishlamasa

- `56658.mp3` fayli joyida ekanini tekshiring
- fayl nomi o'zgarmagan bo'lsin
- sahifani qayta yuklang

### Highlight ko'rinmasa

- brauzerni yangilang
- keshlangan eski versiya ochilgan bo'lsa `Ctrl + F5` qiling
- `index.html` ichidagi `::selection` stillari o'chib ketmaganini tekshiring

### Natija chiqmasa

- barcha JavaScript kodlari to'liq yuklanganini tekshiring
- brauzer console ichida xato yo'qligini tekshiring

## Keyingi yangilashlar uchun tavsiya

Kelajakda quyidagilarni qo'shish mumkin:

- foydalanuvchi javoblarini `localStorage` ga saqlash
- timer
- testni qayta boshlash tugmasi
- audio bilan avtomatik part sync
- dark mode

## Qisqa xulosa

Bu loyiha IELTS Listening mashqi uchun qulay, lokal ishlaydigan, zamonaviy bitta sahifali test interfeysi. Hozirgi yangilanishdan keyin matnni belgilash highlight'i ham to'g'ri ishlaydi va hujjat loyiha holatiga moslab tozalandi.
