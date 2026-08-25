# BAHAN AJAR – PERTEMUAN 1 (S2)
## Pengenalan Excel
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | E / Kelas X |
| **Alokasi Waktu** | 2 JP × 45 menit (90 menit) |
| **Elemen CP** | Analisis Data (AD) / Teknik Informatika dan Komunikasi (TIK) |
| **Tujuan Pembelajaran** | Mengenali antarmuka Microsoft Excel, memahami konsep sel dan range, serta menerapkan fungsi SUM, AVERAGE, dan COUNT untuk mengolah data sederhana |
| **Materi Prasyarat** | Mampu mengoperasikan komputer dan mengetik; mengenal tabel data dari materi pengolah kata (Semester 1) |

---

## A. Kisah Pemantik 🎬

> **"Buku Catatan Keuangan di Ponsel Ibu"**
>
> Ibu kamu punya usaha katering kecil. Setiap hari ia mencatat penjualan di buku tulis: nama menu, harga, dan jumlah porsi. Saat diminta menghitung **total pemasukan satu minggu**, Ibu harus menghitung ulang satu per satu dengan kalkulator — butuh waktu lama dan sering salah. Suatu malam, kakakmu memperlihatkan Microsoft Excel: cukup ketik data sekali, lalu biarkan Excel menghitung otomatis. Sejak itu, hitung-hitungan Ibu selesai dalam hitungan detik. 📊
>
> **Pertanyaan pemantik:** Pernahkah kamu harus menghitung banyak angka berulang-ulang dan malas melakukannya? Bayangkan kamu harus menjumlahkan nilai ulangan seluruh siswa di kelasmu (lebih dari 30 angka) tanpa kalkulator. Bagaimana Excel bisa membuat pekerjaan itu cepat dan bebas salah?

---

## B. Apa Itu Microsoft Excel? 🧮

**Microsoft Excel** adalah aplikasi *spreadsheet* (lembar kerja elektronik) untuk mengolah data dalam bentuk angka, membuat tabel, menghitung dengan rumus, dan menampilkan data dalam bentuk grafik. Berbeda dengan Word yang fokus pada dokumen teks, Excel "hidup" dari kotak-kotak kecil bernama **sel** yang berisi angka dan rumus.

| Istilah | Arti | Contoh |
|---|---|---|
| **Spreadsheet** | Lembar kerja berbentuk tabel untuk mengolah data | Excel, Google Sheets, LibreOffice Calc |
| **Workbook** | File Excel itu sendiri (ekstensi `.xlsx`) | `data_penjualan.xlsx` |
| **Worksheet / Sheet** | Lembar kerja di dalam workbook | Sheet1, Sheet2, Sheet3 |
| **Cell (sel)** | Pertemuan antara kolom dan baris | A1, B2, C5 |
| **Range** | Kumpulan beberapa sel yang dipilih | A1:A10, B2:D4 |
| **Active Cell** | Sel yang sedang aktif (ada kotak tebal) | Klik pada sel B3 |

> 💡 **Ingat:** 1 workbook bisa memuat banyak sheet. Biasanya data yang saling berhubungan diletakkan di sheet yang sama agar mudah dianalisis.

---

## C. Bagian-Bagian Jendela Excel 🪟

| Bagian | Fungsi |
|---|---|
| **Title Bar** | Menampilkan nama file dan aplikasi |
| **Ribbon** | Kumpulan menu (Home, Insert, Formulas, Data, dll.) |
| **Formula Bar** | Tempat menulis, melihat, dan mengedit rumus |
| **Name Box** | Menunjukkan alamat sel yang sedang aktif (mis. `A1`) |
| **Kolom** | Diidentifikasi huruf (A, B, C, …) |
| **Baris** | Diidentifikasi angka (1, 2, 3, …) |
| **Sheet Tab** | Tab untuk berpindah antar sheet |
| **Status Bar** | Menampilkan ringkasan cepat (SUM, AVERAGE, COUNT dari data yang diblok) |

**Alamat sel** ditulis dengan kombinasi **huruf kolom + angka baris**. Contoh: sel `D5` berarti berada di kolom D, baris 5.

---

## D. Sel, Range, dan Cara Memasukkan Data 📥

### D.1 Sel (Cell)
Sel adalah unit terkecil penyimpan data. Klik sebuah sel untuk menjadikannya *active cell*, lalu ketik isinya dan tekan **Enter** (berpindah ke bawah) atau **Tab** (berpindah ke kanan).

### D.2 Range (Kumpulan Sel)
Range ditulis dengan tanda titik dua (`:`). Contoh:

| Notasi | Makna |
|---|---|
| `A1:A5` | Sel A1 sampai A5 (satu kolom, 5 baris) |
| `B2:D4` | Kotak persegi dari B2 sampai D4 (3 kolom × 3 baris) |
| `A1:C1` | Satu baris dari A1 sampai C1 |

Cara memilih range: klik sel pertama → tahan → seret ke sel terakhir, atau klik sel pertama → tekan **Shift** → klik sel terakhir.

### D.3 Tipe Data dalam Sel
| Tipe Data | Contoh | Catatan |
|---|---|---|
| **Teks** | `Nama`, `Kelas X-1` | Rata kiri secara default |
| **Angka** | `5000`, `3.14` | Rata kanan, bisa dihitung |
| **Tanggal** | `16/08/2026` | Dikenali sebagai tanggal |
| **Rumus** | `=A1+B1` | Diawali tanda `=` |

> ⚠️ **Penting:** Rumus WAJIB diawali tanda `=`. Jika kamu mengetik `A1+B1` tanpa `=`, Excel akan menganggapnya teks biasa dan tidak menghitung apa pun.

---

## E. Fungsi Dasar: SUM, AVERAGE, dan COUNT ➕

**Fungsi** adalah rumus siap pakai untuk mengolah data. Semua fungsi ditulis setelah tanda `=` dan memiliki tanda kurung `()`.

| Fungsi | Kegunaan | Contoh | Hasil (jika data 10, 20, 30) |
|---|---|---|---|
| `=SUM(range)` | Menjumlahkan semua angka | `=SUM(A1:A3)` | 60 |
| `=AVERAGE(range)` | Menghitung rata-rata | `=AVERAGE(A1:A3)` | 20 |
| `=COUNT(range)` | Menghitung banyaknya sel yang berisi **angka** | `=COUNT(A1:A5)` | 3 (mengabaikan teks) |
| `=MAX(range)` | Nilai tertinggi | `=MAX(A1:A3)` | 30 |
| `=MIN(range)` | Nilai terendah | `=MIN(A1:A3)` | 10 |

### Contoh Kasus Lengkap
Ketik data berikut di Excel, mulai dari sel A1:

| A (Nama) | B (Nilai) |
|---|---|
| Andi | 80 |
| Budi | 92 |
| Cici | 75 |
| Dewi | 88 |

Lalu ketik rumus berikut di kolom D:
- `D1` → `=SUM(B1:B4)` → **335** (jumlah nilai)
- `D2` → `=AVERAGE(B1:B4)` → **83,75** (rata-rata)
- `D3` → `=COUNT(B1:B4)` → **4** (banyak nilai)

> 💡 **Tips cepat:** Setelah mengetik `=SUM(`, cukup blok range `B1:B4` dengan mouse — Excel akan menuliskannya otomatis.

---

## F. Auto Fill dan Memformat Sel ✨

### F.1 Auto Fill (Isi Otomatis)
Ketik angka `1` di A1 dan `2` di A2 → blok keduanya → tarik **fill handle** (kotak kecil di pojok kanan bawah sel) ke bawah → Excel otomatis mengisi 3, 4, 5, …. Cara yang sama untuk deret tanggal, bulan, atau nomor urut.

### F.2 Format Sel (Tab Home → grup Number / Font / Alignment)
| Format | Menu | Kegunaan |
|---|---|---|
| Mata uang | Home → Number → `$` / "Accounting" | Menampilkan angka sebagai Rupiah/dollar |
| Persen | Home → Number → `%` | Nilai 0,25 tampil sebagai 25% |
| Rata teks | Home → Alignment | Kiri/kanan/tengah |
| Tebal & warna | Home → Font | Mempercantik judul tabel |
| Border | Home → Font → Border | Garis tepi tabel |
| Warna latar | Home → Font → Fill Color | Menyorot sel tertentu |

---

## F. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Tuliskan alamat sel di kolom B baris 7, lalu jelaskan arti notasi range `A1:C3`.
**Pembahasan:** Alamat sel tersebut adalah **B7**. Notasi `A1:C3` berarti kumpulan sel dari A1 sampai C3, yaitu 3 kolom (A, B, C) × 3 baris (1, 2, 3) = 9 sel.

**Contoh 2:** Data nilai ulangan di sel B2 sampai B6 adalah 70, 85, 60, 95, 78. Tuliskan rumus untuk: (a) jumlah, (b) rata-rata, (c) banyaknya nilai.
**Pembahasan:**
1. `=SUM(B2:B6)` → 70+85+60+95+78 = **388**
2. `=AVERAGE(B2:B6)` → 388 ÷ 5 = **77,6**
3. `=COUNT(B2:B6)` → **5** (semua berisi angka)

**Contoh 3:** Mengapa `=count(A1:A5)` menghasilkan 3 padahal ada 5 data, dengan isi A1–A5 = 10, "Kucing", 20, "Anjing", 30?
**Pembahasan:** Fungsi `COUNT` **hanya menghitung sel berisi angka**. Sel A2 ("Kucing") dan A4 ("Anjing") berupa teks, sehingga diabaikan. Jadi yang dihitung hanya 10, 20, 30 → **3**.

---

## G. Miskonsepsi yang Sering Terjadi 🚫

| Miskonsepsi | Fakta yang Benar |
|---|---|
| "Rumus ditulis tanpa tanda `=`" | Rumus **selalu diawali `=`**; tanpa `=`, Excel menganggapnya teks |
| "Workbook dan worksheet itu sama" | Workbook = file (`.xlsx`); worksheet = lembar kerja di dalamnya |
| "COUNT menghitung semua sel yang terisi" | COUNT hanya menghitung sel **berisi angka**, teks diabaikan |
| "A1:D1 adalah range satu kolom" | `A1:D1` adalah range **satu baris** (4 kolom) |
| "Menekan Delete menghapus isi seluruh sheet" | Delete hanya menghapus isi sel yang dipilih |

---

## H. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Menjelajah Antarmuka:** Buka Excel, lalu tunjukkan dan sebutkan fungsi 5 bagian jendela Excel berikut: Name Box, Formula Bar, Ribbon, Sheet Tab, dan Status Bar.

**Tantangan 2 — Tabel Nilai Kelas:** Buat tabel 10 siswa dengan kolom Nama dan Nilai (bebas). Lalu gunakan rumus untuk menghitung jumlah, rata-rata, dan banyaknya data. Tulis hasilnya di bawah tabel.

**Tantangan 3 — Membuat Daftar Gaji Kecil:** Buat tabel 5 karyawan dengan kolom Nama, Gaji Pokok, dan Tunjangan. Tambahkan kolom **Total Gaji** berisi rumus `=C2+D2` (sesuaikan baris). Hitung total seluruh gaji dengan SUM. Gunakan Auto Fill untuk membuat nomor urut.

---

## I. Rangkuman Kunci 🔑

1. **Excel** adalah aplikasi *spreadsheet* untuk mengolah data angka.
2. **Workbook** adalah file; **worksheet** adalah lembar kerjanya.
3. **Sel** = pertemuan kolom & baris (A1); **range** = kumpulan sel (A1:A10).
4. Rumus **selalu diawali `=`**, contoh `=A1+B1`.
5. `=SUM` menjumlah, `=AVERAGE` merata-rata, `=COUNT` menghitung sel berisi angka.
6. **Auto Fill** membuat deret angka/tanggal otomatis.
7. Format sel (mata uang, persen, border, warna) memperindah dan memperjelas data.

---

## J. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Spreadsheet** | Lembar kerja elektronik untuk mengolah data |
| **Workbook** | File Excel (`.xlsx`) |
| **Worksheet** | Lembar kerja di dalam workbook |
| **Cell (sel)** | Pertemuan kolom dan baris; tempat menyimpan data |
| **Range** | Kumpulan sel, ditulis dengan titik dua (`A1:A5`) |
| **Formula Bar** | Tempat menulis dan melihat rumus |
| **Auto Fill** | Fitur isi otomatis deret angka/tanggal |

---

## K. Refleksi (Merefleksi) 🔍

- Konsep apa yang paling penting kamu pelajari hari ini?
- Bagaimana Excel bisa membantu pekerjaan mencatat dan menghitung di sekitarmu (kantin, toko, rapor)?
- Apa beda antara sel dan range? Tunjukkan dengan contohmu sendiri.
- Bagian mana yang masih sulit dipahami?
- **Skala pemahaman diri:** ____/10
- Apa yang ingin kamu pelajari lebih lanjut tentang Excel?

---

**MGMP Informatika SMAN 6 Cimahi — Fase E (Kelas X) Semester 2**