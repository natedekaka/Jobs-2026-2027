# BAHAN AJAR – PERTEMUAN 10 (S1)
## Pseudocode - Percabangan
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*



### 🧠 Memahami — Membangun Pemahaman Awal

## A. Tujuan Pembelajaran
Setelah mempelajari materi ini, siswa mampu:
1. Menulis pseudocode dengan struktur percabangan IF-ELSE
2. Menulis pseudocode dengan IF bertingkat
3. Menulis pseudocode dengan logika AND/OR
4. Menerjemahkan pseudocode ke flowchart dan sebaliknya

## B. Review: Apa Itu Pseudocode?
Pseudocode adalah deskripsi algoritma menggunakan bahasa yang mirip dengan bahasa pemrograman, tapi tidak terikat pada sintaks bahasa tertentu. Pseudocode digunakan untuk merencanakan program sebelum coding.

**Aturan Pseudocode:**
1. Gunakan bahasa Indonesia atau Inggris yang jelas
2. Gunakan indentasi untuk blok kode
3. Tulis satu langkah per baris
4. Gunakan kata kunci: IF, ELSE, ENDIF, AND, OR, NOT

## C. Pseudocode IF Sederhana
```
INPUT usia
IF usia >= 17 THEN
    OUTPUT "Sudah cukup umur"
ENDIF
OUTPUT "Selesai"
```

**Contoh: Cek Genap**
```
INPUT angka
IF angka MOD 2 == 0 THEN
    OUTPUT "Genap"
ENDIF
```

## D. Pseudocode IF-ELSE
```
INPUT nilai
IF nilai >= 70 THEN
    OUTPUT "Lulus"
ELSE
    OUTPUT "Tidak Lulus"
ENDIF
```

**Contoh: Positif/Negatif**
```
INPUT angka
IF angka > 0 THEN
    OUTPUT "Positif"
ELSE
    IF angka < 0 THEN
        OUTPUT "Negatif"
    ELSE
        OUTPUT "Nol"
    ENDIF
ENDIF
```

## E. Pseudocode IF-ELIF-ELSE
```
INPUT nilai
IF nilai >= 85 THEN
    OUTPUT "A"
ELSE IF nilai >= 70 THEN
    OUTPUT "B"
ELSE IF nilai >= 55 THEN
    OUTPUT "C"
ELSE
    OUTPUT "D"
ENDIF
```

**Contoh: Kategori Usia**
```
INPUT usia
IF usia <= 5 THEN
    OUTPUT "Balita"
ELSE IF usia <= 12 THEN
    OUTPUT "Anak"
ELSE IF usia <= 17 THEN
    OUTPUT "Remaja"
ELSE
    OUTPUT "Dewasa"
ENDIF
```

## F. Pseudocode dengan AND/OR
```
INPUT nilai
INPUT absen

IF nilai >= 70 AND absen >= 80 THEN
    OUTPUT "Lulus"
ELSE
    OUTPUT "Tidak Lulus"
ENDIF
```

**Contoh: Diskon**
```
INPUT usia
INPUT hari

IF usia < 12 OR hari = "Selasa" THEN
    OUTPUT "Dapat diskon"
ELSE
    OUTPUT "Tidak dapat diskon"
ENDIF
```

## G. Pseudocode Nested IF
```
INPUT usia
INPUT nilai

IF usia >= 17 THEN
    IF nilai >= 70 THEN
        OUTPUT "Lulus dan cukup umur"
    ELSE
        OUTPUT "Cukup umur tapi tidak lulus"
    ENDIF
ELSE
    IF nilai >= 70 THEN
        OUTPUT "Lulus tapi belum cukup umur"
    ELSE
        OUTPUT "Tidak lulus dan belum cukup umur"
    ENDIF
ENDIF
```

## H. Translasi: Pseudocode ke Flowchart, Flowchart ke Pseudocode
Setiap pseudocode IF bisa digambar sebagai simbol belah ketupat di flowchart.

**Pseudocode -> Flowchart:**
1. IF menjadi simbol decision (belah ketupat)
2. THEN menjadi cabang Ya
3. ELSE menjadi cabang Tidak
4. ENDIF kembali ke alur utama


### 🔧 Mengaplikasi — Praktik & Penerapan

## I. Latihan
1. Buat pseudocode: input angka -> output "Genap" atau "Ganjil"
2. Buat pseudocode: input 3 angka -> output yang terbesar
3. Buat pseudocode: input tahun -> output "Kabisat" atau "Bukan"
4. Buat pseudocode: input suhu dan batuk -> output status kesehatan (AND)
5. Buat flowchart dari pseudocode "Cek Kelulusan"


### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagaimana konsep ini terkait dengan materi sebelumnya?
- Skala pemahaman diri: ___/10
- Apa yang ingin kamu pelajari lebih lanjut?

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) S1 Pert 10**
