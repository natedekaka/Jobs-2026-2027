# BAHAN AJAR – PERTEMUAN 14 (S1)
## PTS — Ujian Praktik
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Praktik Lintas Bidang (PLB) |
| **Tujuan Pembelajaran** | Mengukur penguasaan flowchart, pseudocode, dan fungsi lanjut Excel melalui ujian praktik sesuai kisi-kisi PTS |
| **Materi Prasyarat** | Pertemuan 1–13 — Algoritma, flowchart, pseudocode, dan Excel lanjutan |

---

## A. Skenario Ujian 🎬

> **"Ini Saatnya Membuktikan Kemampuanmu"**
>
> Selama 13 pertemuan, kamu sudah belajar algoritma, flowchart, pseudocode, dan Excel. Hari ini kamu membuktikannya dalam **PTS — Ujian Praktik**. Tidak ada kuis dadakan: semua soal diambil dari materi yang sudah kamu pelajari. Kerjakan dengan tenang, baca soal dengan teliti, dan gunakan waktu sebaik-baiknya.
>
> **Pertanyaan pemantik:** Materi mana yang kamu rasa paling kuat? Bagaimana strategi membagi waktu agar semua bagian ujian terselesaikan?

---

## B. Format & Rincian Ujian

| Sesi | Durasi | Jenis | Materi |
|---|---|---|---|
| **Sesi 1** | 60 menit | PG (10) + Praktik (3 flowchart + 2 pseudocode) | Flowchart & Pseudocode |
| **Sesi 2** | 30 menit | PG (5) + Praktik (2 soal Excel) | Excel Lanjutan |

**Rubrik Penilaian:**
| Aspek | Bobot | Detail |
|---|---|---|
| Teori Flowchart (PG) | 15% | 10 soal |
| Praktik Flowchart | 25% | 3 soal |
| Praktik Pseudocode | 25% | 2 soal |
| Teori Excel (PG) | 10% | 5 soal |
| Praktik Excel | 25% | 2 soal |

---

## C. Contoh Soal Teori (Pilihan Ganda)

1. Simbol flowchart untuk input/output adalah... **jajar genjang**
2. Simbol untuk percabangan adalah... **belah ketupat**
3. Simbol untuk proses adalah... **persegi panjang**
4. Struktur algoritma berurutan disebut... **sequence**
5. Simbol untuk mulai/selesai adalah... **oval/terminal**
6. Pseudocode menggunakan bahasa yang... **mirip bahasa manusia**
7. Kata kunci untuk percabangan: **IF-ELSE-ENDIF**
8. Kata kunci perulangan dengan jumlah pasti: **FOR**
9. Perulangan berdasarkan kondisi: **WHILE**
10. Menghubungkan simbol flowchart: **panah**

**Soal Teori Excel:**
1. Fungsi mengambil karakter kiri: **LEFT**
2. Fungsi panjang teks: **LEN**
3. Fungsi menghapus spasi berlebih: **TRIM**
4. Fungsi tanggal hari ini: **TODAY**
5. Fungsi selisih tanggal: **DATEDIF**

---

## D. Contoh Soal Praktik & Penyelesaian

**Soal 1 — Flowchart terbesar (30 poin):** Input 2 angka → cari yang terbesar.
**Penyelesaian:** Start → input a → input b → `a > b?` → Ya → output a; Tidak → output b → End.

**Soal 2 — Flowchart genap 1–20 (30 poin):** Cetak bilangan genap 1–20.
**Penyelesaian:** Start → i = 2 → `i <= 20?` → Ya → output i → i = i + 2 → kembali; Tidak → End.

**Soal 3 — Flowchart faktorial (40 poin):** Input n → hitung n!.
**Penyelesaian:** Start → input n → f = 1 → i = 1 → `i <= n?` → Ya → f = f × i → i = i + 1 → kembali; Tidak → output f → End.

**Soal 4 — Pseudocode predikat (30 poin):**
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

**Soal 5 — Pseudocode tebak angka (40 poin):**
```
rahasia = 7
INPUT tebakan
WHILE tebakan != rahasia
    OUTPUT "Salah, coba lagi"
    INPUT tebakan
ENDWHILE
OUTPUT "Benar!"
```

**Soal 6 — Excel data siswa (30 poin):** Tabel 5 siswa: NIS, Nama, Tgl Lahir, Usia (DATEDIF), Email (LOWER + CONCAT).
- Usia: `=DATEDIF(C2, TODAY(), "Y")`
- Email: `=LOWER(B2) & "@sma6.sch.id"`

**Soal 7 — Excel diskon (40 poin):** Tabel 10 barang: Kode, Nama, Qty, Harga, Diskon, Total.
- Diskon: `=IF(Qty >= 10, 10%, 0%)`
- Total: `=Qty * Harga * (1 - Diskon)`

---

## E. Panduan Strategi Ujian

1. **Flowchart:** gunakan simbol yang benar (oval start/end, jajar genjang I/O, persegi proses, belah ketupat keputusan) dan panah yang jelas.
2. **Pseudocode:** gunakan indentasi dan kata kunci IF/ELSE/FOR/WHILE/ENDIF/ENDFOR.
3. **Excel:** pastikan rumus benar (diawali `=`), format rapi.
4. **Prioritas:** kerjakan yang mudah dulu, sisakan 5 menit untuk review.

---

## F. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Jelaskan konsep utama yang telah kamu pelajari dengan bahasamu sendiri!
**Jawaban (contoh):** Algoritma adalah urutan langkah logis; direpresentasikan dengan flowchart (visual) dan pseudocode (mirip bahasa manusia). Excel membantu mengolah data dengan fungsi teks, tanggal, dan format kondisional.

**Contoh 2:** Berikan 2 contoh penerapan dalam kehidupan sehari-hari!
**Jawaban:** (1) Flowchart alur pelayanan di puskesmas (urutan + keputusan); (2) Excel untuk menghitung gaji/uang saku otomatis menggunakan DATEDIF dan IF.

**Contoh 3:** Diskusikan bagaimana materi ini membantu menyelesaikan masalah nyata!
**Jawaban:** Berpikir komputasional + flowchart memaksa kita memecah masalah dan melihat keputusan dengan jelas; Excel mempercepat pengolahan data sehingga keputusan berbasis data lebih cepat.

---

## G. Miskonsepsi / Kesalahan Umum 🚫

| Miskonsepsi / Kesalahan | Fakta yang Benar |
|---|---|
| "Soal ujian keluar dari materi" | Semua soal berasal dari kisi-kisi pertemuan 1–13 |
| "Menghafal jawaban tanpa paham" | Soal praktik menuntut menggambar/menulis algoritma sendiri |
| "Excel bisa dijawab tanpa mengetik rumus" | Rumus harus ditulis dengan benar agar diperiksa |
| "Menggambar flowchart asal-asalan" | Simbol dan panah harus sesuai standar agar dihargai |
| "Menghabiskan waktu di soal sulit" | Kerjakan mudah dulu, sisakan waktu review |

---

## H. Tantangan Persiapan (Mengaplikasi) 🎯

**Tantangan 1 — Latihan Simbol (mudah):** Gambar ulang 4 simbol dasar flowchart tanpa melihat catatan.

**Tantangan 2 — Latihan Pseudocode (sedang):** Tulis ulang dari ingatan: predikat nilai dan tebak angka.

**Tantangan 3 — Latihan Excel (sulit):** Buat tabel 10 barang dengan diskon IF dan total otomatis tanpa melihat rumus.

**Tantangan 4 — Simulasi (paling sulit):** Kerjakan seluruh soal praktik PTS dalam waktu 90 menit sebagai simulasi.

---

## I. Rangkuman Kunci 🔑

- PTS mengukur **flowchart, pseudocode, dan Excel lanjutan**.
- Rubrik: Teori flowchart 15%, Praktik flowchart 25%, Praktik pseudocode 25%, Teori Excel 10%, Praktik Excel 25%.
- Kunci flowchart: simbol benar + panah jelas.
- Kunci pseudocode: indentasi + kata kunci IF/ELSE/FOR/WHILE.
- Kunci Excel: rumus diawali `=` dan format rapi.

---

## J. Glosarium 📖

| Istilah | Arti |
|---|---|
| **PTS** | Penilaian Tengah Semester |
| **Kisi-kisi** | Rincian cakupan materi dan bobot ujian |
| **Rubrik** | Pedoman penilaian berdasarkan aspek |
| **Simulasi** | Latihan ujian menyerupai kondisi asli |
| **PLB** | Praktik Lintas Bidang |

---

## K. Refleksi (Merefleksi) 🔍

- Materi mana yang paling siap kamu hadapi?
- Bagian mana yang masih ragu dan perlu diperbaiki?
- Strategi waktu apa yang akan kamu gunakan?
- **Skala pemahaman diri:** ____/10
- Apa yang ingin kamu perbaiki untuk PAS nanti?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 1**