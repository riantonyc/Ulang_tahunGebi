# 🎂 Halaman Web Ulang Tahun — Blandina Gebi

Membuat halaman web ulang tahun yang **interaktif, animatif, dan personal** untuk Blandina Gebi.
Terinspirasi dari [happy-birthday-card.vercel.app](https://happy-birthday-card.vercel.app/) yang menggunakan narasi storytelling bertahap, namun dengan desain yang lebih premium, penuh warna, dan lebih personal.

---

## Open Questions

> [!IMPORTANT]
> **Pertanyaan untuk kamu sebelum mulai implementasi:**
>
> 1. **Foto / Gambar**: Apakah ada foto Blandina Gebi yang ingin ditampilkan? Atau bisa pakai ilustrasi/avatar?
> 2. **Pesan khusus**: Apakah ada pesan ulang tahun spesifik yang ingin ditulis untuknya?
> 3. **Bahasa**: Pakai Bahasa Indonesia, Bahasa Inggris, atau campuran?
> 4. **Tema warna**: Ada preferensi warna tertentu? (Misal: pink girly, gold elegant, ungu misterius, dll)
> 5. **Musik**: Apakah ingin ada background music / lagu Happy Birthday?
> 6. **Deployment**: Apakah akan di-deploy ke Vercel atau cukup lokal saja?

---

## Konsep & Fitur

### 🎬 Alur Storytelling Interaktif (Scene-by-Scene)

Mirip dengan referensi, halaman ini akan memiliki **narasi bertahap** yang dijalankan user dengan klik/tap. Setiap scene memiliki animasi dan teks yang berbeda.

| Scene | Deskripsi |
|-------|-----------|
| **Scene 1** | Loading/Intro — layar gelap dengan nama "Blandina Gebi" muncul perlahan |
| **Scene 2** | Pintu tertutup dengan teks: *"Ada sesuatu untukmu hari ini..."* |
| **Scene 3** | Animasi berjalan di lorong gelap menuju cahaya |
| **Scene 4** | Hadiah/kado muncul — user diminta membukanya |
| **Scene 5** | Kado terbuka — balon-balon meledak, confetti jatuh |
| **Scene 6** | Kue ulang tahun muncul dengan lilin menyala |
| **Scene 7** | Teks pesan ulang tahun personal muncul satu per satu |
| **Scene 8** | Layar penuh bunga & balon, teks besar: "SELAMAT ULANG TAHUN BLANDINA GEBI 🎉" |
| **Scene 9** | Card penutup dengan tombol "Putar Lagi" |

---

## Proposed Changes

### 📁 Struktur File

```
d:/Project/HeFun/Birtday/
├── index.html          # Halaman utama
├── style.css           # Semua styling + animasi
├── script.js           # Logic scene & interaksi
├── assets/
│   ├── images/         # Gambar (cake, gift, balloon, dll)
│   ├── sounds/         # Opsional: musik background
│   └── fonts/          # Font lokal jika perlu
└── README.md
```

---

### [NEW] index.html

Halaman utama HTML dengan:
- Meta SEO (title: "Happy Birthday Blandina Gebi 🎂")
- Import Google Fonts (font: `Pacifico`, `Quicksand`, atau `Dancing Script` untuk nuansa birthday)
- Canvas element untuk animasi confetti
- Container scene-by-scene
- Tombol navigasi (klik/tap untuk lanjut)

---

### [NEW] style.css

Design system premium dengan:
- **Color palette**: Misalnya gradient pink-ungu (`#FF6B9D → #C44DFF → #FFD700`)
- **Glassmorphism cards** untuk narasi
- **Animasi CSS**:
  - `@keyframes fadeIn` — teks muncul perlahan
  - `@keyframes floatBalloon` — balon bergerak ke atas
  - `@keyframes candleFlicker` — lilin berkedip
  - `@keyframes confettiFall` — confetti jatuh
  - `@keyframes heartBeat` — elemen berdenyut
  - `@keyframes slideUp` — konten masuk dari bawah
- **Efek partikel** (bintang, hati, bunga)
- **Responsive** untuk mobile & desktop

---

### [NEW] script.js

Logic utama:
- **Scene Manager**: Array of scene configs yang ditampilkan satu per satu
- **Typewriter Effect**: Teks narasi muncul huruf per huruf
- **Konfeti Engine**: Partikel jatuh dari atas layar
- **Kado Interaksi**: Klik kado → open animasi
- **Lilin Interaksi**: Klik lilin → tiup animasi
- **Countdown/Timer**: Opsional — jam berputar sebelum hadiah muncul
- **Audio Manager**: Play/pause musik birthday (jika aset ada)

---

## Tech Stack

| Aspek | Pilihan |
|-------|---------|
| **Framework** | Vanilla HTML + CSS + JS (no framework) |
| **Animasi** | CSS Keyframes + JS Canvas |
| **Font** | Google Fonts (Dancing Script + Quicksand) |
| **Konfeti** | Custom JS particles (tidak perlu library) |
| **Ikon** | Emoji atau SVG inline |
| **Audio** | HTML5 `<audio>` tag (opsional) |

---

## Design Aesthetic

### 🎨 Color Palette Rekomendasi

```
Background:  #1a0a2e (deep purple night)
Primary:     #FF6B9D (hot pink)
Secondary:   #C44DFF (violet)
Accent:      #FFD700 (gold)
Text:        #FFFFFF / #FFE5F0
Glass:       rgba(255,255,255,0.1) + blur
```

### ✨ Visual Elements
- 🎈 Balon berwarna-warni melayang
- 🎂 Animasi kue dengan lilin berkedip
- 🎁 Kado yang bisa "dibuka"
- 🎊 Confetti jatuh dari langit
- ⭐ Bintang-bintang berkelip di latar
- 💖 Partikel hati berterbangan
- 🌸 Bunga-bunga animasi

---

## Verification Plan

### Manual Verification
- [ ] Buka `index.html` di browser
- [ ] Cek setiap scene berjalan mulus
- [ ] Cek animasi confetti tidak lag
- [ ] Cek tampilan di mobile (Chrome DevTools)
- [ ] Cek teks terbaca jelas di semua scene
- [ ] Cek tombol navigasi responsif
- [ ] Opsional: test di Vercel preview setelah deploy

---

> **Estimasi Waktu Build**: 1-2 jam implementasi penuh oleh AI
> **Target**: Halaman yang bikin Blandina Gebi terharu dan tersenyum! 🥹🎉
