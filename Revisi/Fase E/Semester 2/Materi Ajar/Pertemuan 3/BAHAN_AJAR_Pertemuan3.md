# BAHAN AJAR – PERTEMUAN 3 (S2)
## Referensi Sel & Fungsi
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*



### 🧠 Memahami — Membangun Pemahaman Awal

## A. Fungsi IF
IF digunakan untuk menentukan keputusan berdasarkan kondisi.

### Sintaks:
=IF(kondisi, nilai_jika_benar, nilai_jika_salah)

### Contoh:
=IF(B2>=70,"LULUS","TIDAK LULUS")
Jika nilai >= 70 → LULUS, jika tidak → TIDAK LULUS

### IF Bertingkat:
=IF(B2>=85,"A",IF(B2>=70,"B",IF(B2>=55,"C","D")))

## B. Fungsi VLOOKUP
VLOOKUP mencari nilai di kolom pertama tabel dan mengambil data dari kolom lain.

### Sintaks:
=VLOOKUP(nilai_cari, tabel_referensi, no_kolom, FALSE)

### Contoh:
=VLOOKUP(A2,$E$1:$F$10,2,FALSE)
- A2: nilai yang dicari (kode barang)
- $E$1:$F$10: tabel referensi
- 2: ambil data dari kolom ke-2
- FALSE: cari persis (exact match)

## C. Studi Kasus — Data Nilai
Buat tabel:
| Nama | Nilai | Huruf | Status |
|---|---|---|---|
| Andi | 85 | =IF(B2>=85,"A",...) | =IF(B2>=70,"L","TL") |
| Budi | 62 | ... | ... |


### 🔧 Mengaplikasi — Praktik & Penerapan

## D. Latihan
1. Tulis rumus IF: jika nilai > 75 maka "LULUS"!
2. Apa fungsi FALSE di VLOOKUP?
3. Buat IF bertingkat untuk nilai A≥85, B≥70, C<70

### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagaimana konsep ini terkait dengan materi sebelumnya?
- Skala pemahaman diri: ___/10
- Apa yang ingin kamu pelajari lebih lanjut?

---
**MGMP Informatika SMAN 6 Cimahi — Fase E (Kelas X) S2 Pert 3**
