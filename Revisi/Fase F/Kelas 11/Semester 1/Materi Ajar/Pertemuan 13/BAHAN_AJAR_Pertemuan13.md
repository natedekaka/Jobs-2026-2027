# BAHAN AJAR – PERTEMUAN 13 (S1)
## Conditional Formatting & Sort/Filter
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*


### A. Conditional Formatting (CF)
Conditional Formatting adalah fitur Excel yang otomatis mengubah format sel (warna, font, border) berdasarkan nilai atau aturan tertentu. Tujuannya memudahkan identifikasi data penting secara visual.

### B. Aturan CF yang Sering Digunakan

| Jenis Aturan | Contoh | Efek |
|---|---|---|
| Highlight Cell Rules | Nilai > 75 | Sel hijau |
| Top/Bottom Rules | 10 nilai tertinggi | Sel kuning |
| Data Bars | Semua sel | Batang warna di dalam sel |
| Color Scales | Semua sel | Gradien merah-putih-hijau |
| Icon Sets | Semua sel | Ikon panah/bulatan |
| Custom Formula | =$A1="Lulus" | Format berdasarkan rumus |

### C. Langkah Membuat CF

1. Blok range data yang ingin diformat
2. Home → Conditional Formatting → New Rule
3. Pilih jenis aturan (contoh: "Format only cells that contain")
4. Tentukan kondisi: Cell Value → greater than → 75
5. Klik Format → pilih Fill (warna hijau) → OK

**Contoh:** Nilai siswa di kolom B2:B20
- Nilai ≥ 85 → hijau (A)
- Nilai 70-84 → kuning (B)
- Nilai < 70 → merah (perlu remedial)

### D. Sort (Mengurutkan Data)

| Jenis Sort | Langkah | Contoh |
|---|---|---|
| Single Level | Data → Sort → pilih kolom | Urutkan nilai terbesar ke terkecil |
| Multi Level | Data → Sort → Add Level | Urutkan kelas, lalu nilai dalam kelas |
| Custom Sort | Data → Sort → Options | Urutkan berdasarkan hari (Senin-Minggu) |

**Praktik:**
1. Sortir nilai dari tertinggi ke terendah
2. Sortir berdasarkan kelas (asc) lalu nilai (desc)
3. Sortir berdasarkan status kelulusan (Lulus di atas)

### E. Filter (Menyaring Data)

Filter menampilkan hanya baris yang memenuhi kriteria tertentu.

**Langkah:**
1. Click header tabel
2. Data → Filter
3. Klik dropdown di kolom → centang kriteria

**Contoh Filter:**
- Tampilkan hanya kelas XI-A
- Tampilkan siswa dengan nilai > 80
- Tampilkan produk dengan stok < 10
- Filter teks: "Contains" kata tertentu

### F. Studi Kasus Gabungan

**Data Penjualan Bulanan:**
| Tanggal | Produk | Qty | Harga | Total |
|---|---|---|---|---|
| 1/1 | Kopi | 50 | 5000 | 250000 |
| 2/1 | Teh | 30 | 3000 | 90000 |
| ... | ... | ... | ... | ... |

**Tugas:**
1. CF: Total > 500rb → hijau, < 100rb → merah
2. Sort: Total terbesar ke terkecil
3. Filter: tampilkan hanya produk "Kopi" dengan Qty > 20


### 🧠 Memahami — Membangun Pemahaman Awal


### 🔧 Mengaplikasi — Praktik & Penerapan

### G. Latihan Soal
1. Bagaimana cara memberi warna merah otomatis pada sel yang bernilai < 70?
2. Urutkan data berikut berdasarkan Total (desc): (A: 500rb, B: 200rb, C: 800rb)
3. Filter apa yang digunakan untuk menampilkan data produk yang namanya mengandung kata "Susu"?
4. Buat CF dengan rumus: sorot seluruh baris jika kolom Status = "Tidak Lulus"

- CF memformat otomatis berdasarkan aturan
- Sort mengurutkan data (1 atau banyak level)
- Filter menyaring data berdasarkan kriteria
- CF + Sort + Filter = alat analisis data cepat


### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagaimana konsep ini terkait dengan materi sebelumnya?
- Skala pemahaman diri: ___/10
- Apa yang ingin kamu pelajari lebih lanjut?

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 1**
