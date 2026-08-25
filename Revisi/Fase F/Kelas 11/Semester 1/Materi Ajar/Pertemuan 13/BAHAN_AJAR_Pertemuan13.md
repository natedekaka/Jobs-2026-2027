# BAHAN AJAR – PERTEMUAN 13 (S1)
## Conditional Formatting & Sort/Filter
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Analisis Data (AD) |
| **Tujuan Pembelajaran** | Menerapkan Conditional Formatting, mengurutkan data (sort) satu/beberapa level, menyaring data (filter) dengan kriteria, dan mengkombinasikan ketiganya untuk analisis data |
| **Materi Prasyarat** | Pertemuan 12 — Fungsi lanjut Excel (teks & tanggal) |

---

## A. Kisah Pemantik 🎬

> **"Mencari Jarum di Tumpukan Data"**
>
> OSIS punya daftar 400 siswa dan ingin tahu siapa yang nilainya di bawah KKM untuk remedial. Membaca 400 baris satu per satu sangat melelahkan. Dengan Excel: warna merah otomatis muncul pada nilai di bawah KKM (**Conditional Formatting**), data diurutkan dari terendah (**Sort**), lalu tinggal tampilkan yang merah saja (**Filter**). Masalah selesai dalam 3 klik!
>
> **Pertanyaan pemantik:** Pernahkah kamu kesulitan mencari satu data di tengah daftar panjang? Strategi apa yang bisa membuat pencarian itu lebih cepat?

---

## B. Conditional Formatting (CF)

**Conditional Formatting** adalah fitur Excel yang **otomatis mengubah format sel** (warna, font, border) berdasarkan nilai atau aturan tertentu. Tujuannya memudahkan identifikasi data penting secara **visual**.

**Aturan CF yang Sering Digunakan:**
| Jenis Aturan | Contoh | Efek |
|---|---|---|
| **Highlight Cell Rules** | Nilai > 75 | Sel berwarna |
| **Top/Bottom Rules** | 10 nilai tertinggi | Sel disorot |
| **Data Bars** | Semua sel | Batang warna di dalam sel |
| **Color Scales** | Semua sel | Gradien merah–putih–hijau |
| **Icon Sets** | Semua sel | Ikon panah/bulatan |
| **Custom Formula** | `=$A1="Lulus"` | Format berdasarkan rumus |

---

## C. Langkah Membuat Conditional Formatting

1. Blok range data yang ingin diformat
2. **Home → Conditional Formatting → New Rule**
3. Pilih jenis aturan (misal: "Format only cells that contain")
4. Tentukan kondisi: Cell Value → greater than → 75
5. Klik **Format** → pilih Fill (warna) → **OK**

**Contoh — Nilai siswa di kolom B2:B20:**
- Nilai ≥ 85 → **hijau** (A)
- Nilai 70–84 → **kuning** (B)
- Nilai < 70 → **merah** (perlu remedial)

---

## D. Sort (Mengurutkan Data)

| Jenis Sort | Langkah | Contoh |
|---|---|---|
| **Single Level** | Data → Sort → pilih kolom | Urutkan nilai terbesar ke terkecil |
| **Multi Level** | Data → Sort → Add Level | Urutkan kelas dulu, lalu nilai di dalam kelas |
| **Custom Sort** | Data → Sort → Options | Urutkan hari (Senin–Minggu) |

**Praktik:**
1. Sortir nilai dari tertinggi ke terendah
2. Sortir berdasarkan kelas (asc) lalu nilai (desc)
3. Sortir status kelulusan (Lulus di atas)

> 💡 **Ingat:** sebelum sort, pastikan seluruh tabel terseleksi agar baris data tidak terpisah.

---

## E. Filter (Menyaring Data)

**Filter** menampilkan **hanya baris yang memenuhi kriteria** tertentu.

**Langkah:**
1. Klik header tabel
2. **Data → Filter**
3. Klik dropdown di kolom → centang kriteria

**Contoh Filter:**
- Tampilkan hanya kelas XI-A
- Tampilkan siswa dengan nilai > 80
- Tampilkan produk dengan stok < 10
- Filter teks: "Contains" kata tertentu

---

## F. Studi Kasus Gabungan — Data Penjualan

**Data Penjualan Bulanan:**
| Tanggal | Produk | Qty | Harga | Total |
|---|---|---|---|---|
| 1/1 | Kopi | 50 | 5000 | 250000 |
| 2/1 | Teh | 30 | 3000 | 90000 |
| 3/1 | Susu | 120 | 8000 | 960000 |
| 4/1 | Kopi | 25 | 5000 | 125000 |

**Tugas Analisis:**
1. **CF:** Total > 500.000 → hijau; < 100.000 → merah
2. **Sort:** Total terbesar ke terkecil → Susu (960rb), Kopi (250rb), Kopi (125rb), Teh (90rb)
3. **Filter:** tampilkan hanya produk "Kopi" dengan Qty > 20 → Kopi Qty 50 dan 25

---

## G. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Bagaimana memberi warna merah otomatis pada sel bernilai < 70?
**Jawaban:** Blok range → Home → Conditional Formatting → New Rule → "Format only cells that contain" → Cell Value → less than → 70 → Format → Fill merah → OK. Semua sel < 70 otomatis merah.

**Contoh 2:** Urutkan data berikut berdasarkan Total (desc): A: 500rb, B: 200rb, C: 800rb!
**Jawaban:** Urutan dari terbesar: **C (800rb) → A (500rb) → B (200rb)**.

**Contoh 3:** Filter apa yang digunakan untuk menampilkan produk yang namanya mengandung kata "Susu"?
**Jawaban:** Data → Filter → klik dropdown kolom Produk → Text Filters → **Contains** → ketik "Susu" → OK. Hanya baris berisi "Susu" yang tampil.

**Contoh 4:** Buat CF dengan rumus menyorot seluruh baris jika kolom Status = "Tidak Lulus"!
**Jawaban:** Blok seluruh range data (A2:E20) → New Rule → "Use a formula" → `=$D2="Tidak Lulus"` (D = kolom Status) → Format → Fill merah → OK. Semua baris dengan Status "Tidak Lulus" ikut tersorot.

**Contoh 5:** Urutkan siswa berdasarkan kelas (ascending) lalu nilai (descending). Apa langkahnya?
**Jawaban:** Data → Sort → Add Level. Level 1: kolom Kelas, A–Z. Level 2: kolom Nilai, Z–A. Hasil: semua siswa kelas yang sama berkelompok, dan di dalam kelas diurutkan dari nilai tertinggi.

---

## H. Miskonsepsi / Kesalahan Umum 🚫

| Miskonsepsi / Kesalahan | Fakta yang Benar |
|---|---|
| Sort hanya memindahkan satu kolom | Seluruh baris ikut tersortir — seleksi tabel penuh |
| Filter menghapus data | Filter hanya **menyembunyikan** baris; data tetap ada |
| CF hanya warna | CF juga bisa font, border, icon, data bar |
| Mengira sort dan filter sama | Sort = mengurutkan; filter = menampilkan sebagian |
| Lupa tanda `=` pada formula CF | Formula CF harus diawali `=` dan pakai referensi baris |

---

## I. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — CF Dasar (mudah):** Buat 15 nilai acak, lalu beri warna: ≥85 hijau, 70–84 kuning, <70 merah.

**Tantangan 2 — Sort (sedang):** Sortir data 15 siswa: kelas ascending, lalu nilai descending.

**Tantangan 3 — Filter (sulit):** Filter data penjualan: tampilkan hanya "Kopi" dengan Qty > 20, lalu sort Total desc.

**Tantangan 4 — Analisis Gabungan (paling sulit):** Buat CF dengan formula untuk menyorot seluruh baris siswa yang "Tidak Lulus", filter hanya baris merah, lalu buat ringkasan jumlah siswa tidak lulus per kelas.

---

## J. Rangkuman Kunci 🔑

- **Conditional Formatting** memformat otomatis berdasarkan aturan.
- **Sort** mengurutkan data — bisa multi level (kelas → nilai).
- **Filter** menampilkan hanya baris yang memenuhi kriteria.
- CF + Sort + Filter = **alat analisis data cepat**.
- Sort jangan sampai memecah baris; filter tidak menghapus data.

---

## K. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Conditional Formatting** | Pemformatan otomatis berdasarkan aturan |
| **Sort** | Mengurutkan data (asc/desc, multi level) |
| **Filter** | Menyaring baris sesuai kriteria |
| **Ascending** | Urutan naik (A–Z, kecil–besar) |
| **Descending** | Urutan turun (Z–A, besar–kecil) |
| **Data Bars** | Batang warna di dalam sel sebagai visualisasi nilai |

---

## L. Refleksi (Merefleksi) 🔍

- Konsep apa yang paling penting kamu pelajari hari ini?
- Bagaimana CF + Sort + Filter membantu menganalisis data nyata?
- Bagian mana yang masih sulit dipahami?
- **Skala pemahaman diri:** ____/10
- Apa yang ingin kamu pelajari lebih lanjut?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 1**