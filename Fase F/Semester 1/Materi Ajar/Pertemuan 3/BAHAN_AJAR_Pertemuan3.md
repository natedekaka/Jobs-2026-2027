# BAHAN AJAR – PERTEMUAN 3
## Perancangan (Design) & UI/UX

| TP | BK, LD — Proses Rekayasa |
|---|---|

---

### A. TAHAP DESIGN DALAM SDLC

Setelah analisis kebutuhan selesai (Pert 2), kita tahu **apa** yang harus dibuat. Tahap design menjawab **bagaimana** tampilan dan cara kerjanya.

#### Output Tahap Design

| Output | Deskripsi | Mirip |
|---|---|---|
| **Wireframe** | Sketsa kerangka hitam-putih, fokus pada tata letak | Denah rumah |
| **Mockup** | Desain visual dengan warna, font, gambar | Rumah 3D |
| **Prototype** | Mockup interaktif — bisa diklik/digunakan | Tur virtual rumah |
| **ERD** | Entity Relationship Diagram — struktur data | Diagram listrik |
| **User Flow** | Alur pengguna dari awal sampai tujuan | Peta jalan |

---

### B. UI vs UX

#### UI (User Interface)

**Tampilan** aplikasi — apa yang dilihat dan disentuh pengguna.

| Elemen UI | Contoh |
|---|---|
| Warna | Biru, putih, abu |
| Tipografi (font) | Arial, Roboto, ukuran 14pt |
| Tombol | Bentuk, ukuran, bayangan |
| Ikon | Icon menu, icon search |
| Tata letak | Posisi logo, menu, konten |

#### UX (User Experience)

**Pengalaman** pengguna saat menggunakan aplikasi — bagaimana perasaannya.

| Aspek UX | Pertanyaan | Contoh Baik |
|---|---|---|
| Mudah dipakai | "Berapa langkah untuk pesan?" | 3 langkah |
| Efisien | "Cepatkah aplikasi ini?" | Loading < 2 detik |
| Memuaskan | "Apakah nyaman?" | Warna enak dilihat |
| Aksesibel | "Bisa dipakai semua orang?" | Teks bisa diperbesar |

#### Analogi: Restoran

| UI | UX |
|---|---|
| Desain menu — font, gambar, warna | Kemudahan memilih menu |
| Dekorasi restoran | Kecepatan pelayanan |
| Seragam pelayan | Keramahan pelayan |

> **UI yang baik + UX yang baik = Produk yang sukses!**

---

### C. PRINSIP DESAIN UI/UX

#### 1. Konsisten

Elemen yang sama harus terlihat dan berfungsi sama di seluruh aplikasi.

| ❌ Tidak Konsisten | ✅ Konsisten |
|---|---|
| Tombol "Simpan" biru di halaman 1, merah di halaman 2 | Tombol "Simpan" selalu biru di kanan atas |
| Font judul Arial di halaman A, Times New Roman di halaman B | Font judul konsisten |

#### 2. Sederhana (Keep It Simple)

Jangan membebani pengguna dengan terlalu banyak pilihan.

| ❌ Terlalu Ramai | ✅ Sederhana |
|---|---|
| 15 menu di halaman utama | 3–5 menu utama |
| 10 warna berbeda | 2–3 warna utama |
| Paragraf panjang | Poin-poin singkat |

#### 3. Umpan Balik (Feedback)

Pengguna harus tahu bahwa aksinya diproses.

| Situasi | Umpan Balik |
|---|---|
| Klik tombol | Tombol berubah warna |
| Proses loading | Animasi loading / progress bar |
| Error | Pesan error yang jelas (bukan "Error 500") |
| Berhasil | Notifikasi hijau "Data tersimpan" |

#### 4. Toleransi Error

Pengguna boleh salah — dan harus bisa memperbaikinya dengan mudah.

| ❌ Tidak Toleran | ✅ Toleran |
|---|---|
| Hapus data langsung hilang | "Yakin hapus?" + tombol undo |
| Tidak bisa kembali | Tombol "Kembali" / "Back" |
| Form terisi hilang jika error | Data tetap terisi, tandai field merah |

#### 5. Visibilitas Status

Pengguna harus tahu **posisi mereka** dalam aplikasi.

- Breadcrumb: "Beranda > Produk > Detail"
- Judul halaman yang jelas
- Tab aktif ditandai

#### 6. Aksesibilitas

Aplikasi bisa dipakai oleh **semua orang**, termasuk penyandang disabilitas.

- Kontras warna cukup (mudah dibaca)
- Ukuran font bisa diperbesar
- Alternatif teks untuk gambar
- Navigasi dengan keyboard

---

### D. STUDI KASUS: REDESIGN APLIKASI SEKOLAH

#### Sebelum (Desain Buruk)

```
+--------------------------------------------------+
| [LOGO] [MENU 1] [MENU 2] [MENU 3] [MENU 4]      |
| [MENU 5] [MENU 6] [MENU 7] [MENU 8] [MENU 9]    |
+--------------------------------------------------+
|                                                   |
| SELAMAT DATANG DI APLIKASI SEKOLAH KITA YANG      |
| SANGAT LUAR BIASA DENGAN BERBAGAI FITUR           |
| YANG MUNGKIN ANDA BUTUHKAN UNTUK KEPERLUAN        |
| SEKOLAH HARI INI DAN SETERUSNYA                   |
|                                                   |
| [ TOMBOL 1 ] [ TOMBOL 2 ] [ TOMBOL 3 ]            |
| [ TOMBOL 4 ] [ TOMBOL 5 ] [ TOMBOL 6 ]            |
+--------------------------------------------------+
```

**Masalah:** Terlalu banyak menu, teks panjang, terlalu banyak tombol.

#### Sesudah (Desain Baik)

```
+--------------------------------------------------+
| [LOGO]         Beranda  Jadwal  Presensi  Profil  |
+--------------------------------------------------+
|                                                   |
|   Selamat datang, Andi!                          |
|   Hari ini: Senin, 15 Juli 2026                  |
|                                                   |
|   ┌─────────┐  ┌─────────┐  ┌─────────┐          |
|   │ 📅      │  │ 📋      │  │ 📊      │          |
|   │ Jadwal  │  │ Presensi│  │ Nilai   │          |
|   │ Hari Ini│  │ Hari Ini│  │ Terkini │          |
|   └─────────┘  └─────────┘  └─────────┘          |
|                                                   |
|   [+] Lihat Semua                                 |
+--------------------------------------------------+
```

**Perbaikan:** Menu utama 4, sambutan singkat, 3 fitur utama dengan ikon, tombol aksi jelas.

---

### E. CARA MEMBUAT WIREFRAME

#### Tools untuk Wireframe

| Tool | Platform | Tingkat |
|---|---|---|
| **Kertas & Pensil** | Manual | Konsep awal |
| **Google Draw / Canva** | Web | Sederhana |
| **Figma** | Web/Desktop | Profesional |
| **Balsamiq** | Desktop | Wireframe khusus |
| **Draw.io / diagrams.net** | Web | Gratis |

#### Langkah Membuat Wireframe

1. **Tentukan halaman** — apa yang mau dibuat? (login, dashboard, form, dll.)
2. **Buat kerangka** — kotak-kotak untuk setiap elemen
3. **Atur tata letak** — header di atas, konten di tengah, navigasi di samping/bawah
4. **Tambahkan label** — "Logo", "Menu", "Tombol Simpan"
5. **Review** — apakah alurnya jelas?

#### Contoh Wireframe — Halaman Login

```
┌────────────────────────────────┐
│ [LOGO APLIKASI]                │
│                                │
│   Masuk ke Akun Anda           │
│                                │
│   ┌──────────────────────┐     │
│   │  NISN                 │     │
│   └──────────────────────┘     │
│                                │
│   ┌──────────────────────┐     │
│   │  Password             │     │
│   └──────────────────────┘     │
│                                │
│   ┌──────────────────────┐     │
│   │      MASUK           │     │
│   └──────────────────────┘     │
│                                │
│   Lupa password?               │
│   Belum punya akun? Daftar     │
└────────────────────────────────┘
```

---

### F. RANGKUMAN

| Konsep | Inti |
|---|---|
| **Wireframe** | Sketsa kerangka hitam-putih |
| **Mockup** | Desain visual penuh warna |
| **Prototype** | Mockup interaktif |
| **UI** | Tampilan — warna, font, tata letak |
| **UX** | Pengalaman — mudah, cepat, nyaman |
| **Prinsip** | Konsisten, sederhana, feedback, toleransi error |

---

**MGMP Informatika SMAN 6 Cimahi**
