# 🎮 Memory Card Game

# Naruto-Shippuden-Memory-Card-Game

## 📋 Deskripsi Project

Memory Card Game adalah permainan sederhana yang menguji kemampuan mengingat pemain. Pemain harus mencocokkan pasangan kartu yang memiliki gambar yang sama dalam waktu 60 detik.

### Gameplay
- **16 kartu** (8 pasang gambar yang sama)
- Semua kartu ditampilkan selama **2 detik** di awal permainan
- Pemain harus mengingat posisi kartu dan mencocokkan pasangannya
- Waktu permainan: **60 detik**
- Sistem scoring dengan bonus point

---

## ✨ Fitur

### 1. Main Menu
- Halaman awal dengan tombol **PLAY**
- Background menarik dengan karakter

### 2. Gameplay Utama
- **Preview Kartu**: Semua kartu ditampilkan selama 2 detik sebelum game dimulai
- **Timer Countdown**: 60 detik untuk menyelesaikan permainan
- **Sistem Scoring**:
  - ✅ Berhasil mencocokkan: **+200 poin**
  - ❌ Salah mencocokkan: **-20 poin**
- **Bonus Point**: Maksimal 600 poin, berkurang 10 poin/detik
- **Retry Feature**: Reset permainan dan mulai dari awal

### 3. End Game
- MessageBox menampilkan skor akhir
- Total score = Score + Bonus Point (jika menang)

---

## 🎯 Rule Permainan

1. **Timer**: Permainan berjalan selama 60 detik sejak dimulai
2. **Preview**: Di awal, semua kartu terbuka selama 2 detik
3. **Pinalti**: Salah mencocokkan = **-20 poin** (bisa minus)
4. **Reward**: Berhasil mencocokkan = **+200 poin**
5. **Bonus**: Maksimal 600 poin, berkurang 10 poin setiap detik
6. **Kondisi Menang**: 
   - Semua pasangan ditemukan sebelum waktu habis
   - Mendapat bonus point sesuai sisa waktu
7. **Kondisi Kalah**: Waktu habis sebelum semua pasangan ditemukan

---

## 🛠️ Teknologi yang Digunakan

- **Platform**: Windows Forms (.NET Framework)
- **Bahasa**: Visual Basic (VB.NET)
- **IDE**: Microsoft Visual Studio 2019/2022
- **Framework**: .NET Framework 4.7.2 atau lebih tinggi

---

## 📦 Cara Menjalankan Project

### Prerequisites
- Windows 10/11
- Visual Studio 2019 atau lebih baru
- .NET Framework 4.7.2+

### Langkah Instalasi

1. **Clone repository ini**
   ```bash
   git clone https://github.com/username/memory-card-game.git
   ```

2. **Buka project di Visual Studio**
   - Klik 2x file `MemoryCardGame.sln`
   - Atau: File → Open → Project/Solution → Pilih `.sln` file

3. **Restore NuGet Packages** (jika ada)
   - Tools → NuGet Package Manager → Manage NuGet Packages for Solution
   - Klik Restore

4. **Build Project**
   - Build → Build Solution (Ctrl+Shift+B)

5. **Run**
   - Debug → Start Debugging (F5)
   - Atau klik tombol ▶ Start

---

## 📁 Struktur Project

```
MemoryCardGame/
├── MemoryCardGame/
│   ├── Form1.vb                 # Main Menu Form
│   ├── FormMain.vb              # Game Form
│   ├── My Project/
│   │   └── Resources.resx       # Resource file untuk gambar
│   └── Resources/
│       ├── Images/
│       │   ├── Backgrounds/     # Background images
│       │   ├── Cards/           # Card images (8 jenis + backCard)
│       │   ├── Buttons/         # Play & Retry button
│       │   └── Characters/      # Karakter dekoratif
│       └── Sounds/              # SFX (opsional)
├── MemoryCardGame.sln           # Solution file
└── README.md                    # File ini
```

---

## 🎨 Assets yang Digunakan

### Gambar
- **Background**: Main Menu & Game Background
- **Kartu**: 8 jenis kartu + 1 backCard
- **Tombol**: Play button, Retry button
- **Karakter**: Retry character (maskot)

### Ukuran Komponen
- Form Size: **1500 x 900 px**
- Card Size: **155 x 155 px**
- Card Spacing: **160 px** (horizontal & vertical)

---

## 💻 Implementasi Teknis

### Komponen Utama

#### Form Main Menu (Form1.vb)
- PictureBox untuk background
- PictureBox tombol Play (dengan event click)

#### Form Main (FormMain.vb)
- **16 PictureBox** untuk kartu (pbCard1 - pbCard16)
- **6 Label** untuk Score, Time, Bonus Point
- **2 Timer**:
  - `TimerCloseCards` (2000ms) - Menutup kartu setelah preview
  - `Timer1` (1000ms) - Countdown & bonus point
- **1 PictureBox** untuk tombol Retry

### Algoritma Utama

1. **Random Kartu**: Fisher-Yates Shuffle Algorithm
2. **Matching Logic**: Membandingkan nilai Tag dari 2 kartu yang diklik
3. **Timer Management**: 
   - Countdown waktu
   - Pengurangan bonus point (10/detik)
4. **Score Calculation**: 
   - Correct match: +200
   - Wrong match: -20
   - Final: Score + Bonus (jika menang)

---

## 📸 Screenshots

### Main Menu
![Main Menu](screenshots/main-menu.png)

### Gameplay
![Gameplay](screenshots/gameplay.png)

*### Game Over*
*![Game Over](screenshots/game-over.png)*

*Note: Tambahkan folder `screenshots/` dan upload gambar di folder tersebut*

---


**Made with ❤️ by Yohanes Nevan/naomhán**
