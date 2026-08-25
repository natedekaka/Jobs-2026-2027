# BAHAN AJAR – PERTEMUAN 17 (S1)
## PAS — Ujian Praktik Excel
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Praktik Lintas Bidang (PLB) |
| **Tujuan Pembelajaran** | Mengukur kemampuan praktik Excel: fungsi teks, fungsi tanggal, validasi data, dan laporan otomatis |
| **Materi Prasyarat** | Pertemuan 12–13 — Fungsi lanjut Excel, Conditional Formatting, Sort/Filter |

---

## A. Skenario Ujian 🎬

> **"Lomba Keterampilan Data"**
>
> Sekolah mengadakan lomba keterampilan pengolahan data. Setiap peserta diberi data mentah siswa dan harus menghasilkan laporan yang rapi dan otomatis: usia terhitung sendiri, email terbentuk sendiri, dan validasi langsung muncul. Kamu memakai kemampuan yang sudah kamu latih: LEFT, RIGHT, MID, LEN, DATEDIF, TODAY, IF, dan Conditional Formatting.
>
> **Pertanyaan pemantik:** Mengapa pemberi kerja sangat menghargai orang yang bisa mengolah data otomatis dengan Excel? Rumus apa yang paling penting untuk laporan data siswa?

---

## B. Format Ujian Praktik

| Sesi | Durasi | Soal | Bobot |
|---|---|---|---|
| **Praktik Excel** | 60 menit | 3 soal | 100% |

**Rubrik Penilaian:**
| Aspek | Bobot |
|---|---|
| Kebenaran formula | 40% |
| Kerapian format | 30% |
| Kelengkapan | 20% |
| Efisiensi (tidak manual) | 10% |

---

## C. Soal 1 — Data Siswa (40 poin)

Buat tabel **10 siswa** dengan struktur:

| NIS | Nama Lengkap | Kelas | Tgl Lahir | Usia | Email Sekolah |
|---|---|---|---|---|---|
| 2025001 | Andi Prasetyo | XI-A | 15/03/2008 | formula | formula |

**Kolom yang menggunakan formula:**
1. **Usia:** `=DATEDIF(D2, TODAY(), "Y") & " tahun"`
2. **Email:** `=LOWER(LEFT(B2,1)) & "." & LOWER(MID(B2, FIND(" ",B2)+1, 99)) & "@sma6.sch.id"` → contoh: `andi.prasetyo@sma6.sch.id`
3. **Kelas:** `=IF(MID(A2,8,1)="1","XI-A",IF(MID(A2,8,1)="2","XI-B","XI-C"))`

**Kriteria:** semua formula benar (20), format rapi + Freeze Panes (10), Table Style (10).

---

## D. Soal 2 — Validasi Data (30 poin)

Buat tabel validasi **10 baris** dengan 5 jenis validasi:

| Data | Jenis | Formula Validasi |
|---|---|---|
| 2025001 | NIS | `=IF(LEN(A2)=7,"Valid","Tidak Valid")` |
| andi@ | Email | `=IF(ISNUMBER(FIND("@",B2)),"Valid","Tidak Valid")` |
| ANDI PRASETYO | Nama | `=IF(EXACT(C2,UPPER(C2)),"Kapital","Cek")` |
| 2008 | Tahun | `=IF(AND(D2>=2008,D2<=2009),"Valid","Cek")` |
| 85 | Nilai | `=IF(AND(E2>=0,E2<=100),"Valid","Cek")` |

**5 jenis validasi yang harus dibuat:**
1. NIS: panjang 7 digit
2. Email: mengandung "@"
3. Nama: huruf kapital semua
4. Tanggal: tahun 2008–2009
5. Nilai: rentang 0–100

---

## E. Soal 3 — Laporan Otomatis (30 poin)

Buat laporan dengan fungsi tanggal:

| No | Keterangan | Formula |
|---|---|---|
| 1 | Tanggal hari ini | `=TODAY()` |
| 2 | Nama bulan | `=TEXT(TODAY(), "MMMM")` |
| 3 | Tahun ini | `=YEAR(TODAY())` |
| 4 | Hari (Senin–Minggu) | `=TEXT(TODAY(), "DDDD")` |
| 5 | Selisih dari 1 Januari tahun ini | `=DATEDIF(DATE(YEAR(TODAY()),1,1), TODAY(), "D")` |
| 6 | Akhir tahun | `=DATE(YEAR(TODAY()),12,31)` |
| 7 | Sisa hari menuju akhir tahun | `=A6 - TODAY()` |

---

## F. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Tulis rumus usia (dalam tahun) dari tanggal lahir di D2!
**Jawaban:** `=DATEDIF(D2, TODAY(), "Y")` → menampilkan usia dalam tahun yang otomatis bertambah.

**Contoh 2:** Tulis rumus email dari nama "Andi Prasetyo" di B2!
**Jawaban:**
```
=LOWER(LEFT(B2,1)) & "." & LOWER(MID(B2, FIND(" ",B2)+1, 99)) & "@sma6.sch.id"
```
→ `andi.prasetyo@sma6.sch.id`.

**Contoh 3:** Tulis rumus validasi NIS harus 7 digit!
**Jawaban:** `=IF(LEN(A2)=7, "Valid", "Tidak Valid")`. NIS "2025001" (7 digit) → **Valid**.

**Contoh 4:** Tulis rumus mengecek nilai dalam rentang 0–100!
**Jawaban:** `=IF(AND(E2>=0, E2<=100), "Valid", "Cek")`.

**Contoh 5:** Bagaimana menampilkan sisa hari menuju akhir tahun?
**Jawaban:** Gunakan `=DATE(YEAR(TODAY()),12,31) - TODAY()` untuk menghitung selisih hari dari hari ini sampai 31 Desember.

---

## G. Miskonsepsi / Kesalahan Umum 🚫

| Miskonsepsi / Kesalahan | Fakta yang Benar |
|---|---|
| Mengetik data manual padahal bisa rumus | Ujian menilai **efisiensi** — gunakan rumus otomatis |
| Lupa tanda `=` di awal rumus | Semua rumus wajib diawali `=` |
| DATEDIF tanpa unit | DATEDIF harus menyertakan "Y"/"M"/"D" |
| Formula tanpa Freeze Panes saat data panjang | Freeze Panes memudahkan membaca header |
| Tidak menggunakan Table Style | Kerapian dinilai 30% dari total nilai |

---

## H. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Data Siswa (mudah):** Buat tabel 5 siswa dengan usia dan email otomatis.

**Tantangan 2 — Validasi (sedang):** Buat 5 validasi (NIS, email, nama, tahun, nilai) pada 10 baris data.

**Tantangan 3 — Laporan (sulit):** Buat laporan otomatis tanggal hari ini, bulan, tahun, dan sisa hari menuju akhir tahun.

**Tantangan 4 — Simulasi Penuh (paling sulit):** Kerjakan ketiga soal PAS (data siswa, validasi, laporan) dalam 60 menit, lalu periksa dengan rubrik.

---

## I. Rangkuman Kunci 🔑

- PAS praktik Excel: **3 soal, 60 menit**, berbobot 100%.
- Soal 1: data siswa — usia (DATEDIF), email (LOWER+MID+FIND), kelas (IF).
- Soal 2: validasi — LEN, FIND, EXACT, AND.
- Soal 3: laporan otomatis — TODAY, TEXT, YEAR, DATE, DATEDIF.
- Rubrik: kebenaran formula 40%, kerapian 30%, kelengkapan 20%, efisiensi 10%.

---

## J. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Validasi** | Pemeriksaan data memenuhi syarat tertentu |
| **Freeze Panes** | Mengunci baris/kolom agar tetap terlihat saat scroll |
| **Table Style** | Gaya tabel siap pakai di Excel |
| **Efisiensi** | Menggunakan rumus otomatis, tidak mengetik manual |
| **TEXT()** | Fungsi memformat tanggal/angka menjadi teks tertentu |

---

## K. Refleksi (Merefleksi) 🔍

- Rumus mana yang paling sering kamu gunakan hari ini?
- Bagian mana yang paling banyak memakan waktu?
- Apa yang akan kamu tingkatkan untuk ujian praktik berikutnya?
- **Skala pemahaman diri:** ____/10
- Target nilai praktikmu?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 1**