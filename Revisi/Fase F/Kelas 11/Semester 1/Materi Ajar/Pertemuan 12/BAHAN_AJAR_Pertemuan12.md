# BAHAN AJAR – PERTEMUAN 12 (S1)
## Fungsi Lanjut Excel
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Analisis Data (AD) |
| **Tujuan Pembelajaran** | Menggunakan fungsi teks (LEFT, RIGHT, MID, LEN, UPPER, LOWER, TRIM, FIND), fungsi tanggal (TODAY, DAY, MONTH, YEAR, DATEDIF), dan menggabungkannya dalam studi kasus data siswa |
| **Materi Prasyarat** | Pengenalan Excel (rumus dasar, SUM, AVERAGE, IF) |

---

## A. Kisah Pemantik 🎬

> **"Bendahara OSIS yang Kerepotan"**
>
> Bendahara OSIS harus membuat daftar 300 siswa: NIS, email sekolah, dan usia. Jika diketik satu per satu, ia butuh seminggu! Untungnya, ia menemukan bahwa Excel bisa **mengambil potongan nama, membuat email otomatis, dan menghitung usia** hanya dari tanggal lahir — semua selesai dalam hitungan menit.
>
> **Pertanyaan pemantik:** Data apa di sekolahmu yang dibuat manual tapi sebenarnya bisa otomatis? Fungsi Excel apa yang bisa membantu?

---

## B. Fungsi Teks (String Functions)

Fungsi teks digunakan untuk **memanipulasi data teks** di Excel.

**1. LEFT, RIGHT, MID — Mengambil Sebagian Teks**
| Fungsi | Sintaks | Contoh | Hasil |
|---|---|---|---|
| **LEFT** | `=LEFT(teks, n)` | `=LEFT("SMAN 6", 4)` | SMAN |
| **RIGHT** | `=RIGHT(teks, n)` | `=RIGHT("SMAN 6", 1)` | 6 |
| **MID** | `=MID(teks, mulai, n)` | `=MID("INFORMATIKA", 2, 5)` | NFORM |

**2. LEN — Panjang Teks**
`=LEN("Python")` → 6. Berguna untuk validasi: NIS harus 7 digit? `=IF(LEN(A2)=7, "Valid", "Cek")`.

**3. UPPER, LOWER, PROPER — Ubah Bentuk Huruf**
| Fungsi | Contoh | Hasil |
|---|---|---|
| UPPER | `=UPPER("andi")` | ANDI |
| LOWER | `=LOWER("ANDI")` | andi |
| PROPER | `=PROPER("andi prasetyo")` | Andi Prasetyo |

**4. TRIM — Hapus Spasi Berlebih**
`=TRIM("  Andi   Prasetyo  ")` → "Andi Prasetyo"

**5. FIND dan SEARCH — Cari Posisi Teks**
| Fungsi | Contoh | Hasil |
|---|---|---|
| FIND | `=FIND("@", "andi@gmail.com")` | 5 |
| SEARCH | `=SEARCH("s", "SMAN 6 Cimahi")` | 2 |

> 💡 **Perbedaan:** FIND **case-sensitive** (membedakan besar/kecil); SEARCH **tidak** case-sensitive dan mendukung wildcard.

---

## C. Fungsi Tanggal (Date Functions)

| Fungsi | Contoh | Keterangan |
|---|---|---|
| **TODAY** | `=TODAY()` | Tanggal hari ini (update otomatis) |
| **NOW** | `=NOW()` | Tanggal + waktu sekarang |
| **DAY** | `=DAY(TODAY())` | Nomor hari (1–31) |
| **MONTH** | `=MONTH(TODAY())` | Nomor bulan (1–12) |
| **YEAR** | `=YEAR(TODAY())` | Tahun |
| **DATEDIF** | `=DATEDIF(tgl_awal, tgl_akhir, "unit")` | Selisih dua tanggal |

**Unit DATEDIF:**
| Unit | Arti | Contoh |
|---|---|---|
| "Y" | Tahun | `=DATEDIF(A2, TODAY(), "Y")` |
| "M" | Bulan | `=DATEDIF(A2, TODAY(), "M")` |
| "D" | Hari | `=DATEDIF(A2, TODAY(), "D")` |

---

## D. Menggabungkan Teks — CONCATENATE / "&"

```
=C2 & " - " & D2
=CONCATENATE(C2, " - ", D2)
```

**Contoh — Buat NIS dari beberapa kolom:** Tahun Masuk, No Urut, Jurusan
`=A2 & "." & TEXT(B2, "000") & "." & C2` → **2025.001.A**

---

## E. Studi Kasus 1 — Data Siswa

Buat tabel: **NIS | Nama | Tanggal Lahir | Usia | Email**

| Kolom | Formula |
|---|---|---|
| Usia | `=DATEDIF(C2, TODAY(), "Y")` |
| Email | `=LOWER(B2) & "@sma6cimahi.sch.id"` |
| Inisial | `=LEFT(B2, 1) & "."` |

**Contoh data:** Nama = "Andi Prasetyo", Tgl Lahir = 15/03/2008 → Usia = `DATEDIF(C2,TODAY(),"Y")` (otomatis); Email = `andi prasetyo@sma6cimahi.sch.id` (lowercase).

---

## F. Studi Kasus 2 — Validasi Data

| Data | Formula Validasi |
|---|---|
| NIS (7 digit) | `=IF(LEN(A2)=7, "Valid", "Error")` |
| Email (mengandung @) | `=IF(ISNUMBER(FIND("@", D2)), "Valid", "Error")` |
| Nama huruf kapital | `=IF(EXACT(B2, UPPER(B2)), "Benar", "Cek")` |
| Umur ≥ 15 | `=IF(E2>=15, "SMA", "Belum SMA")` |

**Ekstrak Jurusan dari NIS** (asumsi: A=IPA, B=IPS, C=Bahasa):
`=IF(RIGHT(A2,1)="A", "IPA", IF(RIGHT(A2,1)="B", "IPS", "Bahasa"))`

**Cek Domain Email:**
`=IF(RIGHT(D2, 9)="gmail.com", "Gmail", "Non-Gmail")`

---

## G. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Ekstrak 3 digit pertama dari NIS "2025001"!
**Jawaban:** `=LEFT("2025001", 3)` → **202**.

**Contoh 2:** Gabungkan nama depan dan belakang dengan spasi (sel A2 = "Andi", B2 = "Prasetyo")!
**Jawaban:** `=A2 & " " & B2` → **Andi Prasetyo** (atau `=CONCATENATE(A2," ",B2)`).

**Contoh 3:** Hitung usia dari tanggal lahir 15/03/2008!
**Jawaban:** `=DATEDIF("15/03/2008", TODAY(), "Y")` → menghasilkan usia dalam tahun yang otomatis bertambah tiap ulang tahun.

**Contoh 4:** Validasi NIS yang harus 7 digit!
**Jawaban:** `=IF(LEN(A2)=7, "Valid", "Error")`. Jika NIS "2025001" (7 digit) → **Valid**.

**Contoh 5:** Buat formula email dari nama "Andi Prasetyo" dengan format `andi.prasetyo@sma6.sch.id`!
**Jawaban:**
```
=LOWER(LEFT(B2,1)) & "." & LOWER(MID(B2, FIND(" ",B2)+1, 99)) & "@sma6.sch.id"
```
→ **andi.prasetyo@sma6.sch.id**.

---

## H. Miskonsepsi / Kesalahan Umum 🚫

| Miskonsepsi / Kesalahan | Fakta yang Benar |
|---|---|
| Lupa tanda `=` di awal rumus | Semua rumus Excel harus diawali `=` |
| Mengira LEN menghitung kata | LEN menghitung **karakter** (termasuk spasi) |
| DATEDIF tanpa unit | DATEDIF wajib mencantumkan unit ("Y"/"M"/"D") |
| Mengira FIND dan SEARCH sama persis | FIND case-sensitive; SEARCH tidak |
| Mengetik email satu per satu | Gunakan rumus LOWER + "&" agar otomatis |

---

## I. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Fungsi Dasar (mudah):** Buat kolom dengan hasil `LEFT("INFORMATIKA",4)`, `RIGHT("SMAN 6",1)`, `LEN("Excel")`.

**Tantangan 2 — Email Otomatis (sedang):** Buat tabel 5 siswa: Nama → kolom Email `lowercase + @sma6cimahi.sch.id`.

**Tantangan 3 — Data Siswa Lengkap (sulit):** Buat tabel 10 siswa dengan NIS, Nama, Tgl Lahir, Usia (DATEDIF), Email, dan Jurusan (dari digit NIS).

**Tantangan 4 — Validasi (paling sulit):** Buat kolom validasi: NIS 7 digit, email mengandung "@", nama harus kapital semua, dan umur ≥ 15 tahun (SMA).

---

## J. Rangkuman Kunci 🔑

- Fungsi teks: **LEFT, RIGHT, MID, LEN, UPPER, LOWER, TRIM, FIND/SEARCH**.
- Fungsi tanggal: **TODAY, NOW, DAY, MONTH, YEAR, DATEDIF**.
- Gabungkan teks dengan **"&"** atau **CONCATENATE**.
- **DATEDIF** menghitung selisih tanggal dalam tahun/bulan/hari.
- Fungsi bisa **digabung** (misal LOWER + LEFT + FIND) untuk otomatisasi data.

---

## K. Glosarium 📖

| Istilah | Arti |
|---|---|
| **String** | Data berupa teks |
| **Case-sensitive** | Membedakan huruf besar/kecil |
| **Wildcard** | Karakter pengganti (*, ?) pada pencarian |
| **DATEDIF** | Fungsi selisih tanggal (Y/M/D) |
| **Validasi** | Pemeriksaan data memenuhi syarat |
| **CONCATENATE** | Fungsi penggabungan teks |

---

## L. Refleksi (Merefleksi) 🔍

- Konsep apa yang paling penting kamu pelajari hari ini?
- Bagaimana fungsi Excel bisa menghemat waktu mengelola data?
- Bagian mana yang masih sulit dipahami?
- **Skala pemahaman diri:** ____/10
- Apa yang ingin kamu pelajari lebih lanjut?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 1**