# BAHAN AJAR – PERTEMUAN 10 (S1)
## Pseudocode — Percabangan
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Algoritma dan Pemrograman (AP) |
| **Tujuan Pembelajaran** | Menulis pseudocode IF-THEN-ELSE, IF bertingkat, dan logika AND/OR, serta menerjemahkan pseudocode ke flowchart dan sebaliknya |
| **Materi Prasyarat** | Pertemuan 9 — Struktur dasar pseudocode |

---

## A. Kisah Pemantik 🎬

> **"Diskon Rahasia Toko Buku"**
>
> Toko buku memberikan diskon dengan aturan: **anak di bawah 12 tahun** ATAU pembeli yang datang pada **hari Selasa** mendapat diskon 20%. Kasir tidak menanyai setiap pembeli, cukup memeriksa dua kondisi: umur dan hari. Begitu salah satu terpenuhi, diskon diberikan.
>
> **Pertanyaan pemantik:** Aturan "ATAU" dan "DAN" apa saja yang kamu temui dalam kehidupan sehari-hari? Apa bedanya saat salah satu syarat cukup vs semua syarat harus terpenuhi?

---

## B. Review: Aturan Menulis Pseudocode

1. Gunakan bahasa Indonesia atau Inggris yang jelas
2. Gunakan indentasi untuk menandai blok kode
3. Tulis satu langkah per baris
4. Gunakan kata kunci: **IF, THEN, ELSE, ENDIF, AND, OR, NOT**

---

## C. Pseudocode IF Sederhana & IF-THEN-ELSE

**IF sederhana** hanya menjalankan aksi bila kondisi benar — tanpa cabang ELSE, tidak ada aksi bila salah:

```
INPUT usia
IF usia >= 17 THEN
    OUTPUT "Sudah cukup umur"
ENDIF
```

**IF-THEN-ELSE** memberi dua kemungkinan aksi:

```
INPUT nilai
IF nilai >= 70 THEN
    OUTPUT "Lulus"
ELSE
    OUTPUT "Tidak Lulus"
ENDIF
```

---

## D. Pseudocode IF-ELIF-ELSE & Nested IF

**IF-ELIF-ELSE** untuk percabangan bertingkat — uji dari kondisi paling ketat ke paling longgar:

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

**Nested IF (IF bersarang)** untuk kondisi majemuk yang saling tergantung:

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

---

## E. Pseudocode dengan AND / OR

**AND** — semua kondisi harus benar:
```
INPUT nilai
INPUT absen
IF nilai >= 70 AND absen >= 80 THEN
    OUTPUT "Lulus"
ELSE
    OUTPUT "Tidak Lulus"
ENDIF
```

**OR** — salah satu kondisi benar saja sudah cukup:
```
INPUT usia
INPUT hari
IF usia < 12 OR hari == "Selasa" THEN
    OUTPUT "Dapat diskon"
ELSE
    OUTPUT "Tidak dapat diskon"
ENDIF
```

> 💡 **Ingat:** AND = dua-duanya benar; OR = salah satu cukup. Salah memakai operator akan mengubah hasil keputusan!

---

## F. Translasi: Pseudocode ↔ Flowchart

**Pseudocode → Flowchart:**
1. **IF** menjadi simbol **decision** (belah ketupat)
2. **THEN** menjadi cabang **Ya**
3. **ELSE** menjadi cabang **Tidak**
4. **ENDIF** kembali ke alur utama

**Flowchart → Pseudocode:**
1. Setiap belah ketupat menjadi **IF ... THEN**
2. Cabang Ya → blok THEN; cabang Tidak → blok ELSE
3. Kotak proses → assignment/perhitungan; jajar genjang → INPUT/OUTPUT

---

## G. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Tulis pseudocode: input angka → output "Genap" atau "Ganjil"!
**Jawaban:**
```
INPUT angka
IF angka MOD 2 == 0 THEN
    OUTPUT "Genap"
ELSE
    OUTPUT "Ganjil"
ENDIF
```

**Contoh 2:** Tulis pseudocode: input 3 angka → output yang terbesar!
**Jawaban:**
```
INPUT a
INPUT b
INPUT c
IF a > b THEN
    IF a > c THEN
        OUTPUT a
    ELSE
        OUTPUT c
    ENDIF
ELSE
    IF b > c THEN
        OUTPUT b
    ELSE
        OUTPUT c
    ENDIF
ENDIF
```

**Contoh 3:** Tulis pseudocode: input tahun → output "Kabisat" atau "Bukan"!
**Jawaban:**
```
INPUT tahun
IF tahun MOD 4 == 0 THEN
    IF tahun MOD 100 != 0 OR tahun MOD 400 == 0 THEN
        OUTPUT "Kabisat"
    ELSE
        OUTPUT "Bukan"
    ENDIF
ELSE
    OUTPUT "Bukan"
ENDIF
```
Tracing: 2024 → kabisat; 1900 → bukan (habis dibagi 100 tapi tidak habis dibagi 400).

**Contoh 4:** Buat flowchart dari pseudocode "Cek Kelulusan"!
**Jawaban:** Start → input nilai → belah ketupat `nilai >= 70?` → cabang Ya → output "Lulus" → End; cabang Tidak → output "Tidak Lulus" → End.

**Contoh 5:** Tulis pseudocode predikat nilai, lalu tracing nilai 90, 72, 60, dan 40!
**Jawaban:** (gunakan struktur IF-ELIF di bagian D) → 90 = A; 72 = B; 60 = C; 40 = D.

---

## H. Miskonsepsi / Kesalahan Umum 🚫

| Miskonsepsi / Kesalahan | Fakta yang Benar |
|---|---|
| Lupa menulis ENDIF | ENDIF menutup blok IF — wajib untuk setiap IF |
| ELSE IF ditulis sebagai ELSE dan IF terpisah | Gunakan `ELSE IF` untuk percabangan bertingkat |
| Menggabungkan kondisi tanpa AND/OR | Tulis operator eksplisit, misal `A AND B` |
| Tidak mengindentasi blok | Indentasi menunjukkan struktur IF-ELSE |
| Kondisi IF bertingkat tidak berurutan | Uji dari kondisi paling ketat ke paling longgar |

---

## I. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Genap/Ganjil (mudah):** Tulis pseudocode input angka → output "Genap" atau "Ganjil".

**Tantangan 2 — Kelulusan Ganda (sedang):** Tulis pseudocode: input nilai dan absen → lulus bila nilai ≥ 70 **DAN** absen ≥ 80.

**Tantangan 3 — Terbesar 3 Angka (sulit):** Tulis pseudocode mencari terbesar dari 3 angka, lalu ubah menjadi flowchart.

**Tantangan 4 — Predikat (paling sulit):** Tulis pseudocode predikat A/B/C/D, lalu lakukan tracing dengan nilai 90, 72, 60, dan 40.

---

## J. Rangkuman Kunci 🔑

- **IF-THEN-ELSE** = cabang dua arah; **ENDIF** wajib menutup blok.
- **ELSE IF** digunakan untuk percabangan bertingkat (ELIF).
- **AND** = semua kondisi benar; **OR** = salah satu benar.
- **Nested IF** = IF di dalam IF untuk kondisi majemuk.
- Translasi: **IF ↔ belah ketupat**, THEN ↔ cabang Ya, ELSE ↔ cabang Tidak.

---

## K. Glosarium 📖

| Istilah | Arti |
|---|---|
| **IF-THEN-ELSE** | Struktur percabangan dua arah |
| **ELSE IF (ELIF)** | Percabangan bertingkat |
| **Nested IF** | IF di dalam IF |
| **Operator AND** | Semua kondisi harus benar |
| **Operator OR** | Salah satu kondisi benar saja |
| **ENDIF** | Penutup blok IF |

---

## L. Refleksi (Merefleksi) 🔍

- Konsep apa yang paling penting kamu pelajari hari ini?
- Bagaimana cara menerjemahkan IF ke simbol belah ketupat?
- Bagian mana yang masih sulit dipahami?
- **Skala pemahaman diri:** ____/10
- Apa yang ingin kamu pelajari lebih lanjut?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 1**