# BAHAN AJAR – PERTEMUAN 12 (S1)
## Fungsi Lanjut Excel
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*



### 🧠 Memahami — Membangun Pemahaman Awal

## A. Tujuan Pembelajaran
Setelah mempelajari materi ini, siswa mampu:
1. Menggunakan fungsi lanjutan Excel (LEFT, RIGHT, MID, LEN, FIND)
2. Menggunakan fungsi teks (UPPER, LOWER, TRIM, CONCATENATE)
3. Menggunakan fungsi tanggal (TODAY, YEAR, MONTH, DATEDIF)
4. Menggabungkan fungsi teks dan logika dalam studi kasus

## B. Fungsi Teks (String Functions)
Fungsi teks digunakan untuk memanipulasi data teks di Excel.

### LEFT, RIGHT, MID — Mengambil Sebagian Teks
| Fungsi | Sintaks | Contoh | Hasil |
|--------|---------|--------|-------|
| LEFT | =LEFT(teks, n) | =LEFT("SMAN 6", 4) | SMAN |
| RIGHT | =RIGHT(teks, n) | =RIGHT("SMAN 6", 1) | 6 |
| MID | =MID(teks, start, n) | =MID("INFORMATIKA", 2, 5) | NFORM |

### LEN — Panjang Teks
=LEN("Python") -> 6
Berguna untuk validasi: NIS harus 10 digit? =IF(LEN(A2)=10, "Valid", "Cek")

### UPPER, LOWER, PROPER — Ubah Huruf
| Fungsi | Contoh | Hasil |
|--------|--------|-------|
| UPPER | =UPPER("andi") | ANDI |
| LOWER | =LOWER("ANDI") | andi |
| PROPER | =PROPER("andi prasetyo") | Andi Prasetyo |

### TRIM — Hapus Spasi Berlebih
=TRIM("  Andi   Prasetyo  ") -> "Andi Prasetyo"

### FIND dan SEARCH — Cari Posisi Teks
| Fungsi | Contoh | Hasil |
|--------|--------|-------|
| FIND | =FIND("@", "andi@gmail.com") | 5 |
| SEARCH | =SEARCH("s", "SMAN 6 Cimahi") | 2 |

FIND: case-sensitive (membedakan huruf besar/kecil)
SEARCH: case-insensitive, bisa wildcard

## C. Fungsi Tanggal (Date Functions)
### TODAY — Tanggal Hari Ini
=TODAY() -> 25/07/2026 (otomatis update setiap hari)

### NOW — Tanggal dan Waktu Sekarang
=NOW() -> 25/07/2026 14:30

### DAY, MONTH, YEAR — Ekstrak Tanggal
=DAY(TODAY()) -> 25
=MONTH(TODAY()) -> 7
=YEAR(TODAY()) -> 2026

### DATEDIF — Selisih Tanggal
=DATEDIF(tgl_awal, tgl_akhir, "unit")
| Unit | Arti | Contoh |
|------|------|--------|
| "Y" | Tahun | =DATEDIF(A2, TODAY(), "Y") |
| "M" | Bulan | =DATEDIF(A2, TODAY(), "M") |
| "D" | Hari | =DATEDIF(A2, TODAY(), "D") |

### CONCATENATE / "&" — Gabung Teks
=C2 & " - " & D2
=CONCATENATE(C2, " - ", D2)

**Contoh: Buat NIS dari beberapa kolom**
Kolom: Tahun Masuk, No Urut, Jurusan
Formula: =A2 & "." & TEXT(B2,"000") & "." & C2
Hasil: 2025.001.A

## D. Studi Kasus 1: Data Siswa
Buat tabel: NIS, Nama, Tanggal Lahir, Usia, Email
| Kolom | Formula |
|-------|---------|
| Usia | =DATEDIF(C2, TODAY(), "Y") |
| Email | =LOWER(B2) & "@sma6cimahi.sch.id" |
| Inisial | =LEFT(B2, 1) & ". | " |

## E. Studi Kasus 2: Validasi Data
| Data | Formula Validasi |
|------|-----------------|
| NIS (10 digit) | =IF(LEN(A2)=10, "Valid", "Error") |
| Email (ada @) | =IF(ISNUMBER(FIND("@", D2)), "Valid", "Error") |
| Nama Kapital | =IF(EXACT(B2, UPPER(B2)), "Benar", "Cek") |
| Umur > 15 | =IF(E2>=15, "SMA", "Belum SMA") |

## F. Fungsi IF dengan Teks
**Contoh: Ekstrak Jurusan dari NIS**
Asumsi NIS: 2025.001.A (A=IPA, B=IPS, C= Bahasa)
=IF(RIGHT(A2,1)="A","IPA",IF(RIGHT(A2,1)="B","IPS","Bahasa"))

**Contoh: Cek Domain Email**
=IF(RIGHT(D2, 9)="gmail.com", "Gmail", "Non-Gmail")


### 🔧 Mengaplikasi — Praktik & Penerapan

## G. Latihan
1. Buat: Ekstrak 3 digit pertama dari NIS "2025001" -> LEFT
2. Buat: Gabung Nama Depan dan Belakang dengan spasi
3. Buat: Hitung usia dari tanggal lahir (DATEDIF)
4. Buat: Validasi NIS panjang 10 digit
5. Studi Kasus: Buat tabel 10 siswa dengan NIS, Nama, Tgl Lahir, Usia, Email Otomatis


### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagaimana konsep ini terkait dengan materi sebelumnya?
- Skala pemahaman diri: ___/10
- Apa yang ingin kamu pelajari lebih lanjut?

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) S1 Pert 12**
