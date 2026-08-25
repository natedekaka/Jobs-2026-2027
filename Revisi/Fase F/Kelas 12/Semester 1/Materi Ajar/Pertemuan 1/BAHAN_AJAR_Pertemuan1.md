# BAHAN AJAR – PERTEMUAN 1 (S1)

## Review Excel (SUM, AVERAGE, IF, VLOOKUP)

*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XII |
| **Alokasi Waktu** | 5 JP × 45 menit/225 menit |
| **Elemen CP** | AD P1 |
| **Tujuan Pembelajaran** | Mahasiswa dapat menggunakan rumus dasar Excel: SUM, AVERAGE, IF, dan VLOOKUP untuk menganalisis data sederhana |
| **Materi Prasyarat** | Paham konsep spreadsheet dan sel dasar |

---

## A. Kisah Pemantik 🎬

> **"Bencana di Lab Komputer"**
>
> Selama praktikum, salah satu mahasiswa lupa menyimpan kerjaannya sebelum komputer mati mendadak. Semua data yang telah dibuat dalam waktu 3 jam hilang total. Kasus ini mengingatkan kita akan pentingnya rumus dan pengelolaan data di Excel.
>
> **Pertanyaan pemantik:** Jika Anda memiliki data pendapatan bulanan 12 bulan dan ingin menghitung total pendapatan, rata-rata pendapatan, serta mencari bulan dengan penjualan tertinggi menggunakan VLOOKUP, bagaimana caranya agar data tidak hilang dan dapat di-analisis kembali? Kaitkan dengan rumus yang akan kita pelajari!

---

## B. Konsep Inti + Tabel Istilah

**Excel** adalah spreadsheet yang memungkinkan pengolahan data terstruktur menggunakan rumus dan fungsi. Berikut konsep dasar:

| Istilah | Deskripsi |
|---|---|
| **Rumus** | Ekspresi yang menghitung nilai (dimulai dengan `=`) |
| **Fungsi** | Rumis bawaan Excel seperti SUM, AVERAGE, IF |
| **VLOOKUP** | Mencari nilai di kolom pertama tabel dan mengembalikan nilai dari kolom lain |
| **Range** | Rentang sel yang dilisi oleh rumus |

---

## C. Rumus Dasar Excel

### 1. Rumus SUM
**Fungsi:** Menjumlahkan nilai dalam rentang sel.
**Sintaks:** `=SUM(nilai1, [nilai2], ...)`

**Contoh data penjualan bulanan:**

| Bulan | Pendapatan (ribuan) |
|---|---|
| Januari | 50 |
| Februari | 75 |
| Maret | 60 |
| April | 80 |

**Contoh penggunaan:**
- `=SUM(B2:B5)` → hasil **265**
- `=SUM(B2,B4)` → hasil **130** ( hanya Januari dan April)

### 2. Rumus AVERAGE
**Fungsi:** Menghitung rata-rata nilai dari rentang sel.
**Sintaks:** `=AVERAGE(nilai1, [nilai2], ...)`

**Contoh:**
- `=AVERAGE(B2:B5)` → hasil **66.25** (total 265 ÷ 4 bulan)

### 3. Rumus IF (Logika)
**Fungsi:** Melakukan pengelompokan kondisional (jika-benar).
**Sintaks:** `=LOGIKAL(test, nilai_jika_benar, nilai_jika_salah)`

**Contoh kasus:** Menentukan lulus/tidak lulus berdasarkan nilai ujian:
- Jika nilai ≥ 60 → "LULUS"
- Jika nilai < 60 → "TIDAK LULUS"

**Contoh penggunaan:**
`=IF(B2>=60, "LULUS", "TIDAK LULUS")`

Jika nilai di cell B2 adalah 75, hasilnya "LULUS". Jika 50, hasilnya "TIDAK LULUS".

### 4. Rumus VLOOKUP
**Fungsi:** Mencari nilai di kolom pertama tabel dan mengembalikan nilai dari kolom yang ditentukan.
**Sintaks:** `=VLOOKUP(nilai_cari, range_tabel, kolom_index, FALSE)`

**Contoh tabel data mahasiswa:**

| NIM | Nama | Nilai Akhir |
|---|---|---|
| 2101 | Andi | 80 |
| 2102 | Budi | 65 |
| 2103 | Cahya | 90 |

**Contoh penggunaan:**
`=VLOOKUP(2102, A2:C4, 3, FALSE)` → hasil **65** (mencari NIM 2102 dan mengembalikan nilai dari kolom ketiga)

**Penting:** Parameter ke-4 `FALSE` menjamin pencarian nilai yang **sempurna** (bukan estimasi). Gunalkan `TRUE` hanya untuk data yang diurutkan dan pencarian estimasi.

---

## D. Latihan Terpadu: Menganalisis Data Penjualan

| Bulan | Produk A | Produk B | Produk C |
|---|---|---|---|
| Januari | 100 | 150 | 200 |
| Februari | 120 | 130 | 220 |
| Maret | 130 | 160 | 180 |
| April | 110 | 140 | 210 |

**Latihan:**
1. Hitung total penjualan Produk A menggunakan `=SUM(C4:C7)` → **460**
2. Hitung rata-rata Produk B menggunakan `=AVERAGE(D4:D7)` → **145**
3. Tentukan bulan dengan penjualan tertinggi Produk C menggunakan `=VLOOKUP(MAX(I4:I7),A4:I7,2,FALSE)` → **Februari** dengan 220

---

## E. Miskonsepsi/Kesalahan Umum

| Miskonsepsi | Fakta yang Benar |
|---|---|
| "Rumus VLOOKUP bisa cari ke kiri" | VLOOKUP hanya cari ke **kanan** dari kolom pertama range. Gunakan INDEX-MATCH untuk cari ke kiri. |
| "Rumus SUM bisa jumlah sel tidak berurutan" | `=SUM(5,10)` bisa, tetapi `=SUM(A1:A10)` hanya angka berturunannya. |
| "Rumus AVERAGE mencakup sel kosong" | AVERAGE mengabaikan sel kosong dan teks. Gunakan AVERAGEA jika butuh termasuk 0. |
| "Rumus IF hanya boleh satu kondisi" | bisa ganda: `=IF(condition1, result1, IF(condition2, result2, result3))` (nesting) |

---

## H. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Perhitungan Bersama:** Buat tabel data penjualan 10 baris dengan angka acak 100-500. Hitung total, rata-rata, dan gunakan IF untuk menandai nilai di atas 300 ("Tinggi") atau bawah 300 ("Rendah").

**Tantangan 2 — Pencarian Data:** Dapatkan NIM mahasiswa dari tabel 20 baris. Gunakan VLOOKUP untuk mencari nama dan nilai akhir berdasarkan NIM yang dicari.

**Tantangan 3 — Kassir Kritis:** Rumus `=IF(A1>300,"Lulus","Gagal")` digabung dengan `=AVERAGE(B1:B10)`. Jelaskan mengapa hasil rata-rata bisa berbeda jika data berisi teks atau kosong.

---

## I. Rangkuman Kunci 🔑

- **SUM** = menjumlahkan nilai dalam range sel
- **AVERAGE** = menghitung rata-rata nilai
- **IF** = fungsi logika untuk kondisi if-then-else
- **VLOOKUP** = mencari nilai dari kolom pertama ke kolom lain (parameter FALSE = exact match)
- Rumus dimulai dengan tanda `=`
- Parameter VLOOKUP: `lookup_value, table_array, col_index_num, range_lookup`

---

## J. Glosarium 📖

| Istilah | Arti |
|---|---|
| **SUM** | Rumus penjumlahan di Excel |
| **AVERAGE** | Rumus rata-rata di Excel |
| **IF** | Fungsi logika kondisional |
| **VLOOKUP** | Vertical Lookup — mencari nilai vertikal |
| **Range** | Kelompok sel yang dilisi |
| **Parameter** | Argumen yang dimasukkan dalam rumus |

---

## K. Refleksi (Merefleksi) 🔍

- Rumus Excel apa yang paling berguna untuk pekerjaan/future careermu?
- Kesulitan apa yang baru hadapi saat menggunakan VLOOKUP?
- **Skala pemahaman diri:** ____/10
- Rumus apa yang ingin kamu pelajari lebih dalam?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XII) Semester 1**