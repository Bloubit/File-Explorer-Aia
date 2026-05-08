# 🎨 Dizayn va UI/UX

## 📱 Ekran Layouti

```
┌─────────────────────────────────┐
│  🔍 Qidirish        ⋮          │  <- Top Bar (Search + Menu)
├─────────────────────────────────┤
│                                 │
│  Turli Fayllar                  │
│  ┌──────┬──────┬──────┬──────┐  │
│  │ 📷   │ 🎬   │ 🎵   │ 📄   │  │ <- Categories Row 1
│  │Tasvi │Video │Audio │Hujja │  │
│  │rlar  │lar   │faylla│tlar  │  │
│  └──────┴──────┴──────┴──────┘  │
│  ┌──────┬──────┐                │
│  │ ⬇️   │ 📦   │                │ <- Categories Row 2
│  │Yukla │ APK  │                │
│  │b olli│ failya│               │
│  └──────┴──────┘                │
│                                 │
│  Oxirgi Fayllar                 │
│  ┌──────────────────────────┐   │
│  │  [Image] [Image] [Image] │   │ <- Recent Files Scroll
│  └──────────────────────────┘   │
│                                 │
│  Xotira                         │
│  ┌─────────────────────────┐    │
│  │ 📱 Ichki xotira         │    │
│  │ ▓▓▓▓▓▓░░░░░░           │ <- Storage Items
│  │ 73.0 GB / 256 GB       │    │
│  ├─────────────────────────┤    │
│  │ 💾 SD-karta             │    │
│  │ [Kiritilmagan]          │    │
│  ├─────────────────────────┤    │
│  │ ☁️  OneDrive             │    │
│  │ [Kiritilmagan]          │    │
│  ├─────────────────────────┤    │
│  │ 🔷 Google Drive         │    │
│  │ [Kiritilmagan]          │    │
│  ├─────────────────────────┤    │
│  │ 🌐 Tarmog qotirasi      │    │
│  │ [Ulanishi yoq]          │    │
│  └─────────────────────────┘    │
│                                 │
└─────────────────────────────────┘
```

---

## 🎨 Rang Sxemasi

| Komponenta | Rang | RGB | Izoh |
|-----------|------|-----|------|
| Background | Dark Grey | #000000 | Asosiy fon |
| Top Bar | Dark | #1a1a1a | Qidiruv paneli |
| Storage Bar | Darker | #2a2a2a | Xotira konteyner |
| Pictures | Red | #FF6B6B | Tasvirlar tugmasi |
| Videos | Teal | #4ECDC4 | Videolar tugmasi |
| Audio | Light Teal | #95E1D3 | Audio tugmasi |
| Documents | Yellow | #F7DC6F | Hujjatlar tugmasi |
| Downloads | Purple | #BB8FCE | Yuklab olinish tugmasi |
| APK | Light Blue | #85C1E2 | APK fayllar tugmasi |
| Text | White | #FFFFFF | Asosiy matn |
| Secondary Text | Light Grey | #AAAAAA | Ikkilamchi matn |

---

## 🎯 Kategoriya Icon'lari

- 📷 Tasvirlar (Pictures)
- 🎬 Videolar (Videos)
- 🎵 Audio fayllar (Audio)
- 📄 Hujjatlar (Documents)
- ⬇️ Yuklab olinganlar (Downloads)
- 📦 APK fayllar (APK)

---

## 💾 Xotira Storage Icon'lari

- 📱 Ichki xotira (Internal Storage)
- 💾 SD-karta (SD Card)
- ☁️ OneDrive
- 🔷 Google Drive
- 🌐 Tarmog qotirasi (Network Storage)

---

## 📐 Komponent O'lchamlari

### Top Bar
- Balandligi: 50px
- Searck Box: 250px x 50px
- Menu Button: 50px x 50px

### Kategoriya Tugmalari
- Har biri: 80px x 100px
- Spacing: 10px

### Recent Files Scroll
- Balandligi: 150px
- Card o'lchamlari: 120px x 150px

### Storage Items
- Balandligi: 80px
- Icon: 30px
- Margin: 10px

---

## 🎬 Animation va Transitions

| Hodisa | Animatsiya |
|--------|-----------|
| Tugma bosilganda | Rang o'zgaradi (fade) |
| Kategoriya ochilganda | List silliq ko'rinadi |
| Xotira loading | Progress bar animatsiyasi |
| Search natijasi | Listning yangilanishi |

---

## 👥 User Flow

```
1. App Ochiladi
   ↓
2. Xotira ma'lumotlari yuklanadi
   ↓
3. Kategoriyalar va recent fayllar ko'rinadi
   ↓
4. Foydalanuvchi kategoriya tanlaydi
   ↓
5. Kategoriya fayllar ochiladi
   ↓
6. Faylni bosib qo'y
   ↓
7. File manager'da ochiladi
```

---

## 📱 Responsive Design

- **Small (< 5")**: Kategoriyalar 2x3 grid
- **Medium (5-6")**: Kategoriyalar 3x2 grid (rasm 1'dagi kabi)
- **Large (> 6")**: Kategoriyalar 3x2 grid + sidebar

---

## 🌙 Dark Mode (Hozirgi)

- Qora fon (#000000)
- Och matnlar (#FFFFFF, #AAAAAA)
- Rangli tugmalar (category-specific)

---

## ⚙️ Font Settings

- **Asosiy font**: Roboto / sans-serif
- **Sarlavha**: 18px, Bold
- **Ordinary matn**: 14px, Normal
- **Kichik matn**: 12px, Normal

