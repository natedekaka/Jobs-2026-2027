# BAHAN AJAR – PERTEMUAN 3 (S2)
## Referensi Sel & Fungsi (IF, VLOOKUP)
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | E / Kelas X |
| **Alokasi Waktu** | 2 JP × 45 menit (90 menit) |
| **Elemen CP** | Analisis Data (AD) / Teknik Informatika dan Komunikasi (TIK) |
| **Tujuan Pembelajaran** | Menerapkan fungsi logika IF dan IF bertingkat untuk pengambilan keputusan, serta menggunakan VLOOKUP untuk mencari data pada tabel referensi |
| **Materi Prasyarat** | Rumus dasar, operator aritmatika, dan referensi sel (relatif/absolut) (Pertemuan 2) |

---

## A. Kisah Pemantik 🎬

> **"Guru yang Menilai Ratusan Lembar dalam Sekejap"**
>
> Bu Rina harus mengubah nilai angka menjadi huruf (A, B, C, D) untuk 120 siswa setiap akhir semester. Dulu ia menilai satu per satu dengan tangan — 2 jam lebih. Kemudian ia menemukan fungsi **IF** di Excel: cukup satu rumus, ditarik ke bawah, dan semua nilai langsung menjadi huruf. Bahkan untuk menentukan "LULUS/TIDAK LULUS" dan mencari data siswa dengan **VLOOKUP**, semua selesai dalam hitungan menit. ⏱️
>
> **Pertanyaan pemantik:** Bagaimana caranya agar sebuah program "memutuskan" sesuatu berdasarkan kondisi? Pernahkah kamu melihat aplikasi yang otomatis memberi nilai, status, atau kategori tanpa campur tangan manusia?

---

## B. Fungsi IF — "Jika... maka..." 🤔

**IF** adalah fungsi logika untuk membuat keputusan: jika kondisi terpenuhi, lakukan satu hal; jika tidak, lakukan hal lain.

### Sintaks:
```
=IF(kondisi; nilai_jika_benar; nilai_jika_salah)
```
*(Catatan: di sebagian versi/regional Excel digunakan tanda koma `,` sebagai pemisah. Menyesuaikan pengaturan negara pada komputer.)*

### Contoh Sederhana
```
=IF(B2>=70; "LULUS"; "TIDAK LULUS")
```
Jika B2 berisi 85 → **LULUS**; jika B2 berisi 60 → **TIDAK LULUS**.

| Kondisi | Operator | Arti |
|---|---|---|
| `>=` | Lebih besar sama dengan | `B2>=70` |
| `>` | Lebih besar | `B2>70` |
| `<` | Lebih kecil | `B2<50` |
| `<=` | Lebih kecil sama dengan | `B2<=60` |
| `=` | Sama dengan | `B2=85` |
| `<>` | Tidak sama dengan | `B2<>70` |

---

## C. IF Bertingkat (Nested IF) 🪜

Jika kondisi lebih dari dua, IF dapat **disusun bertingkat**: nilai yang dihasilkan untuk kondisi salah adalah IF berikutnya.

### Contoh: Mengubah Nilai Menjadi Huruf
```
=IF(B2>=85; "A"; IF(B2>=70; "B"; IF(B2>=55; "C"; "D")))
```
- B2 = 90 → **A**
- B2 = 75 → **B**
- B2 = 60 → **C**
- B2 = 40 → **D**

### Studi Kasus Data Nilai
| A (Nama) | B (Nilai) | C (Huruf) | D (Status) |
|---|---|---|---|
| Andi | 85 | `=IF(B2>=85;"A";IF(B2>=70;"B";IF(B2>=55;"C";"D")))` | `=IF(B2>=70;"LULUS";"TIDAK LULUS")` |
| Budi | 62 | *(salin rumus ke bawah)* | `TIDAK LULUS` |
| Cici | 90 | `A` | `LULUS` |

> ⚠️ **Peringatan:** terlalu banyak IF bertingkat membuat rumus sulit dibaca. Jika kondisinya sangat banyak, pertimbangkan VLOOKUP dengan tabel nilai.

---

## D. Fungsi VLOOKUP — Mencari Data ke Tabel Referensi 🔍

**VLOOKUP** (Vertical Lookup) mencari nilai pada **kolom pertama** sebuah tabel, lalu mengambil data dari kolom lain di baris yang sama.

### Sintaks:
```
=VLOOKUP(nilai_yang_dicari; tabel_referensi; nomor_kolom; FALSE)
```

| Bagian | Contoh | Penjelasan |
|---|---|---|
| nilai yang dicari | `A2` | Kode/kunci yang ingin dicari |
| tabel referensi | `$E$1:$F$10` | Tabel tempat mencari (gunakan absolut `$`) |
| nomor kolom | `2` | Ambil data dari kolom ke-2 tabel tsb. |
| FALSE | `FALSE` | Cari **persis** (exact match); gunakan TRUE untuk rentang |

### Contoh: Mencari Nama Barang dari Kode
Tabel referensi di E1:F10:
| E (Kode) | F (Nama Barang) |
|---|---|
| BRG-01 | Buku Tulis |
| BRG-02 | Pulpen |
| BRG-03 | Penggaris |

Rumus di sel C2: `=VLOOKUP(A2;$E$1:$F$10;2;FALSE)`
- Jika A2 = `BRG-02` → hasil **"Pulpen"**.
- Jika A2 = `BRG-99` (tidak ada) → hasil **#N/A** (nilai tidak ditemukan).

> 💡 **Tips:** Selalu gunakan `FALSE` agar pencarian tepat. Referensi tabel sebaiknya **absolut** (`$E$1:$F$10`) supaya saat disalin tidak bergeser.

---

## E. VLOOKUP dengan Tabel Nilai (Rentang) 📋

VLOOKUP juga bisa mengelompokkan nilai ke dalam kategori dengan `TRUE` (pencarian mendekati). Tabel referensi harus **diurutkan naik**.

| E (Nilai Terendah) | F (Predikat) |
|---|---|
| 0 | D |
| 55 | C |
| 70 | B |
| 85 | A |

Rumus: `=VLOOKUP(B2;$E$1:$F$4;2;TRUE)`
- B2 = 90 → **A**
- B2 = 72 → **B**
- B2 = 30 → **D**

---

## F. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Tuliskan rumus IF: jika nilai di B2 lebih dari 75 maka "LULUS", selain itu "REMEDIAL".
**Pembahasan:** `=IF(B2>75;"LULUS";"REMEDIAL")`.

**Contoh 2:** Buatlah IF bertingkat untuk kategori A (≥85), B (≥70), C (≥55), D (<55).
**Pembahasan:** `=IF(B2>=85;"A";IF(B2>=70;"B";IF(B2>=55;"C";"D")))`.

**Contoh 3:** Apa fungsi argumen FALSE pada VLOOKUP?
**Pembahasan:** FALSE memerintahkan pencarian **persis (exact match)** — nilainya harus sama persis dengan yang ada di kolom pertama tabel referensi. Tanpa FALSE (atau memakai TRUE), Excel mencari nilai terdekat, yang bisa menghasilkan data salah.

**Contoh 4:** Tabel referensi E1:F10 berisi kode (kolom E) dan nama (kolom F). Tuliskan VLOOKUP untuk menampilkan nama barang bila kodenya ada di A2.
**Pembahasan:** `=VLOOKUP(A2;$E$1:$F$10;2;FALSE)`.

---

## G. Miskonsepsi yang Sering Terjadi 🚫

| Miskonsepsi | Fakta yang Benar |
|---|---|
| "IF hanya bisa menangani satu kondisi" | IF bisa **bertingkat** untuk banyak kondisi |
| "`>=70` dan `>70` sama saja" | `>=70` menyertakan 70; `>70` tidak |
| "VLOOKUP mencari di kolom mana pun" | VLOOKUP hanya mencari di **kolom pertama** tabel referensi |
| "Lupa FALSE tidak masalah" | Tanpa FALSE hasil bisa salah untuk data tidak berurutan |
| "Tabel referensi boleh bergeser saat disalin" | Gunakan **absolut `$`** agar tabel tetap |

---

## H. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Status Kelulusan:** Buat tabel 8 siswa (Nama, Nilai) lalu tambahkan kolom Status dengan IF `>=75 → LULUS`.

**Tantangan 2 — Predikat Nilai:** Gunakan IF bertingkat untuk mengubah nilai menjadi huruf A/B/C/D pada data yang sama.

**Tantangan 3 — Daftar Barang:** Buat tabel referensi 8 kode barang (Kode → Nama → Harga). Gunakan VLOOKUP untuk mengisi otomatis Nama dan Harga dari kode yang diketik di kolom lain.

---

## I. Rangkuman Kunci 🔑

1. **IF** = pengambilan keputusan: `=IF(kondisi; benar; salah)`.
2. Operator perbandingan: `>`, `<`, `>=`, `<=`, `=`, `<>`.
3. **IF bertingkat** = IF di dalam IF untuk banyak kondisi.
4. **VLOOKUP** mencari di kolom pertama tabel referensi: `=VLOOKUP(kunci; tabel; kolom; FALSE)`.
5. Gunakan **FALSE** untuk pencarian persis; **TRUE** untuk rentang.
6. Kunci tabel referensi dengan **absolut `$`** agar tidak bergeser saat disalin.
7. Hasil `#N/A` berarti nilai kunci tidak ditemukan di tabel.

---

## J. Glosarium 📖

| Istilah | Arti |
|---|---|
| **IF** | Fungsi logika untuk kondisi "jika–maka" |
| **Nested IF** | IF bertingkat di dalam IF |
| **Operator perbandingan** | Simbol untuk membandingkan nilai (>=, <, dsb.) |
| **VLOOKUP** | Fungsi mencari data vertikal pada tabel referensi |
| **Exact match** | Pencarian persis (FALSE) |
| **#N/A** | Kode error saat nilai tidak ditemukan |

---

## K. Refleksi (Merefleksi) 🔍

- Kapan kamu lebih memilih IF bertingkat dibanding VLOOKUP?
- Bagaimana logika "jika–maka" muncul dalam kehidupan sehari-hari (keputusan, aturan, syarat)?
- Kesalahan apa yang paling sering kamu buat saat menulis IF atau VLOOKUP?
- Bagian mana yang masih perlu kamu pelajari lebih dalam?
- **Skala pemahaman diri:** ____/10
- Apa kasus nyata yang ingin kamu pecahkan dengan IF/VLOOKUP?

---

**MGMP Informatika SMAN 6 Cimahi — Fase E (Kelas X) Semester 2**