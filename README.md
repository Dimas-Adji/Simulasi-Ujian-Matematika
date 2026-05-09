# 📚 Aplikasi Kuis Interaktif - Simulasi Ujian

Aplikasi kuis berbasis HTML, CSS, dan JavaScript untuk simulasi ujian siswa. Dapat dijalankan langsung di browser tanpa server atau internet.

## 🆕 TRY OUT UAS MATEMATIKA KELAS 6 SD

Aplikasi ujian matematika dengan timer 45 menit, 20 soal pilihan ganda, dan 10 soal essay dengan pembahasan lengkap.

**File:** `soal_matematika.html`

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

---

## ✨ Fitur Aplikasi

### 🆕 TRY OUT MATEMATIKA KELAS 6 SD

#### 📝 Soal Pilihan Ganda (20 Soal)
- Materi: Desimal & Pecahan, Kubus & Balok, Peluang, Rasio
- Opsi A, B, C, D dengan desain modern
- Simpan jawaban untuk review akhir

#### ✏️ Soal Esai (10 Soal)
- Input jawaban dengan textarea
- Pembahasan lengkap dengan langkah penyelesaian
- Review setelah ujian selesai

#### ⏰ Timer 45 Menit
- Countdown timer otomatis
- Warning visual 5 menit (orange) dan 1 menit (red)
- Ujian otomatis berakhir saat waktu habis
- Auto-submit jawaban saat timer habis

#### 📊 Hasil & Review Lengkap
- Nilai akhir (skala 100)
- Statistik benar/salah
- **Review soal**: Lihat semua soal dan jawaban
- **Pembahasan esai**: Step-by-step penyelesaian matematika
- Pesan motivasi berdasarkan nilai

### 📱 Responsive Mobile
- Optimized untuk layar HP portrait
- Touch-friendly buttons
- Scrollable content

---

## 📝 Soal Pilihan Ganda (40 Soal) - Bahasa Indonesia
- Jawaban langsung diberi tahu benar/salah
- Pilihan opsi A, B, C, D dengan tampilan modern
- Penjelasan jawaban benar setelah memilih

### ✏️ Soal Esai (5 Soal)
- Input jawaban dengan textarea
- Pengecekan otomatis berdasarkan **keyword matching**
- Tidak case-sensitive, ignore spasi & tanda baca
- Feedback jumlah keyword terdeteksi

### 📊 Hasil & Review
- **Nilai akhir** (skala 100)
- Statistik: Jumlah benar, salah, total soal
- **Review lengkap**: Semua soal, jawaban murid, dan kunci jawaban
- Pesan motivasi berdasarkan nilai

### 🎨 Tampilan
- Desain modern dengan gradient
- Responsive (desktop & mobile)
- Progress bar pergerakan soal
- Animasi halus pada interaksi

---

## 🚀 Cara Menggunakan

### 1. Download File
Download file `Soal.html` dari repository ini.

### 2. Jalankan di Browser
Buka file `Soal.html` dengan browser modern (Chrome, Firefox, Edge, Safari):
```
Double-click Soal.html
atau
Drag file ke browser
```

### 3. Cara Mengerjakan (Bahasa Indonesia)
1. Masukkan nama murid
2. Klik **"Mulai Kuis"**
3. Kerjakan soal PG (pilih opsi → langsung tahu benar/salah)
4. Kerjakan soal esai (tulis jawaban → klik "Periksa Jawaban")
5. Klik **"Lanjut"** untuk soal berikutnya
6. Lihat hasil dan review setelah selesai

---

## 🧮 Cara Menggunakan TRY OUT MATEMATIKA

### 1. Buka File
```
soal_matematika.html
```

### 2. Mulai Ujian
1. Masukkan nama siswa
2. Klik **"Mulai Ujian"**
3. Timer 45 menit akan mulai berjalan

### 3. Mengerjakan Soal
- **Pilihan Ganda**: Klik opsi A/B/C/D untuk menjawab
- **Esai**: Tulis jawaban di kotak textarea
- Scroll ke bawah untuk melihat semua soal
- Klik **"Selesai & Kirim Jawaban"** jika sudah selesai sebelum waktu habis

### 4. Setelah Ujian
- Lihat nilai dan statistik
- Klik **"Review Soal"** untuk melihat:
  - Semua soal dan jawaban Anda
  - Jawaban yang benar untuk PG
  - Pembahasan lengkap dengan rumus untuk soal esai
- Klik **"Ulangi Ujian"** untuk mencoba lagi

### ⏰ Catatan Timer
- Ujian otomatis berakhir saat timer 45 menit habis
- Warning muncul saat tersisa 5 menit (orange) dan 1 menit (red)
- Jangan refresh halaman saat ujian berlangsung!

---

## 📁 Struktur File

```
📦 Simulasi-Ujian/
├── 📄 Soal.html              # Kuis Bahasa Indonesia (40 PG + 5 Esai)
├── 📄 soal_matematika.html   # TRY OUT Matematika Kelas 6 (20 PG + 10 Esai + Timer)
└── 📄 README.md              # Dokumentasi ini
```

**Catatan:** Semua kode ada dalam satu file untuk kemudahan distribusi dan penggunaan offline.

---

## ⚙️ Cara Menambah/Mengubah Soal

### Edit File HTML
Buka `Soal.html` di text editor (VS Code, Notepad++, dll).

### 1. Tambah Soal Pilihan Ganda
Cari bagian `const questions = [` dan tambahkan objek baru:

```javascript
{
    no: 46,                    // Nomor soal
    question: "Teks soal...",  // Bisa pakai <br> untuk baris baru
    options: ["A", "B", "C", "D"], // Pilihan jawaban
    answer: 1                  // Index jawaban benar (0=A, 1=B, 2=C, 3=D)
}
```

### 2. Tambah Soal Esai
Tambahkan dengan property `type: "esai"`:

```javascript
{
    no: 46,
    type: "esai",
    question: "Teks soal esai...",
    keywords: ["kata1", "kata2", "kata3"],  // Kata kunci yang dicari
    minMatch: 2,                            // Minimal cocok untuk benar
    hint: "Petunjuk menjawab...",
    correctAnswer: "Jawaban lengkap yang benar...",
    maxScore: 10
}
```

### Tips Keyword Matching
- Sistem otomatis **lowercase** dan hapus tanda baca
- Murid bisa jawab: "Lingkungan bersih", "LINGKUNGAN BERSIH", atau "lingkungan, bersih!"
- Semua dianggap sama oleh sistem

---

## 🎯 Logika Penilaian Esai

```javascript
// Normalisasi teks (auto oleh sistem)
function normalize(text) {
    return text
        .toLowerCase()                    // → lowercase
        .replace(/[.,!?;:'"]/g, '')       // → hapus tanda baca
        .trim();                          // → hapus spasi berlebih
}

// Contoh
Jawaban murid: "Lingkungan yang BERSIH sangat Sehat!"
→ normalisasi: "lingkungan yang bersih sangat sehat"

Keywords: ["lingkungan", "bersih", "sehat"]
→ Hasil: ✅ Benar (3/3 keyword cocok)
```

---

## 🖼️ Screenshot

| Halaman Mulai | Soal Pilihan Ganda | Soal Esai |
|:---:|:---:|:---:|
| Input nama | Opsi A-D | Textarea + hint |

| Feedback | Hasil | Review |
|:---:|:---:|:---:|
| ✅/❌ langsung | Score + stats | Semua jawaban |

---

## 🔧 Kustomisasi

### Ubah Warna Tema
Edit bagian CSS (variabel tidak ada, cari kode warna):

```css
/* Header gradient */
background: linear-gradient(135deg, #0d47a1 0%, #1976d2 50%, #2196f3 100%);

/* Benar */
border-color: #4CAF50;
background: #e8f5e9;

/* Salah */
border-color: #f44336;
background: #ffebee;
```

### Ubah Jumlah Soal
Tidak ada limit, tambah sebanyak mau di array `questions`.

### Ubah Bobot Nilai
Saat ini semua soal equal weight. Modifikasi function `showResult()` untuk bobot custom.

---

## 📱 Browser Support

| Browser | Versi Minimal |
|---------|---------------|
| Chrome | 60+ |
| Firefox | 60+ |
| Edge | 79+ (Chromium) |
| Safari | 12+ |
| Opera | 47+ |

---

## ⚠️ Batasan

1. **Tidak ada save progress** - Refresh halaman = mulai dari awal
2. **Tidak ada backend** - Data tidak tersimpan ke server/database
3. **Pengecekan esai sederhana** - Hanya keyword matching, tidak cek grammar/logika
4. **Offline only** - Tidak perlu internet tapi juga tidak bisa sync data

---

## 📝 Changelog

### v2.0 (2026-05-09)
- ✅ **NEW**: TRY OUT UAS Matematika Kelas 6 SD
- ✅ 20 soal pilihan ganda (Desimal, Pecahan, Kubus, Balok, Peluang, Rasio)
- ✅ 10 soal esai dengan pembahasan lengkap dan rumus
- ✅ Timer 45 menit dengan auto-submit
- ✅ Responsive design untuk mobile portrait
- ✅ Review soal dengan pembahasan matematika step-by-step

### v1.0 (2026-05-07)
- ✅ 40 soal pilihan ganda Bahasa Indonesia
- ✅ 5 soal esai dengan keyword matching
- ✅ Sistem review lengkap
- ✅ Tampilan responsive

---

## 🤝 Kontribusi

Silakan fork dan pull request untuk:
- Menambah soal baru
- Memperbaiki typo
- Meningkatkan UI/UX
- Menambah fitur baru

---

## 📄 Lisensi

**Free to use** untuk keperluan pendidikan. 
Dibuat untuk membantu guru dan siswa dalam proses belajar mengajar.

---

## 💡 Tips Penggunaan untuk Guru

### Untuk Kuis Bahasa Indonesia (`Soal.html`)
1. **Distribusi**: Copy file ke USB/drive murid
2. **Monitoring**: Berikan instruksi waktu pengerjaan
3. **Review**: Gunakan fitur "Review Soal" untuk diskusi di kelas
4. **Update**: Edit file langsung untuk perbarui soal tiap semester

### Untuk TRY OUT Matematika (`soal_matematika.html`)
1. **Persiapan**: Pastikan murid menggunakan HP dengan baterai cukup
2. **Timer**: Jelaskan bahwa ujian otomatis berakhir setelah 45 menit
3. **Pembahasan**: Gunakan fitur "Review Soal" untuk membahas jawaban bersama
4. **Latihan**: Murid bisa mengulang ujian berkali-kali untuk latihan
5. **Focus**: Tidak bisa kembali ke soal sebelumnya, kerjakan dengan teliti

---

**Dibuat dengan ❤️ untuk pendidikan Indonesia**

---

## 📞 Kontak

Jika ada pertanyaan atau saran, silakan buat issue di repository ini.
