# BAHAN AJAR – PERTEMUAN 5 (S1)
## Studi Kasus Analisis Data
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*



### 🧠 Memahami — Membangun Pemahaman Awal

## A. Tujuan Pembelajaran
Setelah mempelajari materi ini, siswa mampu:
1. Menganalisis data penjualan UMKM menggunakan Excel
2. Membuat interpretasi dari hasil analisis data
3. Menyusun laporan analisis yang komunikatif
4. Memberikan rekomendasi berdasarkan data

## B. Studi Kasus — UMKM Kopi Nusantara
Sebuah UMKM menjual 3 kategori produk (Kopi, Minuman, Snack) selama 3 bulan (Jan-Mar 2025) dengan total 90 baris transaksi.

**Struktur Data:**
| Tanggal | Produk | Kategori | Qty | Harga Satuan | Total | Pelanggan | Wilayah |

**Data Sample:**
| 02/01/2025 | Kopi Arabika | Kopi | 5 | 25000 | 125000 | Andi | Bandung
| 02/01/2025 | Pisang Goreng | Snack | 3 | 15000 | 45000 | Budi | Jakarta
| ... (90 baris)

## C. Analisis yang Harus Dilakukan
**Analisis 1: Produk Terlaris (berdasarkan Qty)**
- Pivot: Rows=Produk, Values=Sum Qty
- Sort descending → produk mana paling laku?
- Interpretasi: "Kopi Arabika terjual 200 unit, tertinggi"

**Analisis 2: Kategori Paling Untung**
- Pivot: Rows=Kategori, Values=Sum Total
- Bar chart → kategori mana dominan?
- Interpretasi: "Kopi menyumbang 60% dari total revenue"

**Analisis 3: Tren Penjualan Bulanan**
- Pivot: Rows=Tanggal→Group Months, Values=Sum Total
- Line chart → tren naik/turun?
- Interpretasi: "Penjualan naik 15% dari Jan ke Feb"

**Analisis 4: Top 5 Pelanggan**
- Pivot: Rows=Pelanggan, Values=Sum Total
- Filter Top 10 → Sort descending
- Interpretasi: "5 pelanggan teratas menyumbang 40% revenue"

**Analisis 5: Wilayah Pemasaran**
- Pivot: Rows=Wilayah, Values=Sum Total, Count Transaksi
- Pie chart → proporsi per wilayah
- Interpretasi: "Bandung menyumbang 50% penjualan"

## D. Membuat Dashboard UMKM
1. Sheet "Data": 90 baris data mentah
2. Sheet "Analisis": Pivot Table + Chart untuk tiap poin di atas
3. Sheet "Dashboard": Satu tampilan dengan KPI + chart + slicer

**KPI Cards:**
- Total Revenue (3 bulan): Rp xxx
- Rata-rata Transaksi: Rp xxx
- Produk Terlaris: xxx
- Jumlah Pelanggan: xx
- Pertumbuhan Bulanan: xx%

**Slicer:** Kategori, Wilayah, Bulan

## E. Interpretasi Data
Tes Pemahaman — Jawab pertanyaan berikut setelah analisis:
1. Produk apa yang paling laris? Mengapa menurutmu?
2. Kategori apa yang paling menguntungkan?
3. Bulan apa penjualan tertinggi? Apa yang mungkin menyebabkannya?
4. Wilayah mana yang potensial dikembangkan?
5. Rekomendasi apa yang akan kamu berikan ke pemilik UMKM?

**Contoh Interpretasi yang Baik:**
"Penjualan tertinggi terjadi di bulan Maret (Rp 25jt), kemungkinan karena mendekati libur lebaran. Kopi Arabika menjadi produk paling laris karena kualitasnya. Disarankan menambah stok Kopi Arabika 30% menjelang bulan Ramadhan."

## F. Laporan Analisis (Output Akhir)
Buat sheet "Laporan" berisi:
1. **Ringkasan:** Total revenue, rata-rata transaksi, produk terlaris, kategori dominan
2. **Kesimpulan:** 3-5 kalimat — apa yang terjadi dengan bisnis ini?
3. **Saran:** 2-3 rekomendasi konkret untuk pemilik UMKM
4. **Data Pendukung:** Screenshot chart/Pivot Table

## G. Tantangan
1. Buat 90 baris data penjualan 3 bulan
2. Lakukan 5 analisis di atas dengan Pivot + Chart
3. Buat dashboard + laporan di sheet terpisah


### 🔧 Mengaplikasi — Praktik & Penerapan

### Latihan Pemahaman
1. Jelaskan konsep utama yang telah dipelajari dengan bahasamu sendiri!
2. Berikan 2 contoh penerapan dalam kehidupan sehari-hari!
3. Diskusikan dengan teman: bagaimana materi ini dapat membantu menyelesaikan masalah nyata?

### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagaimana konsep ini terkait dengan materi sebelumnya?
- Skala pemahaman diri: ___/10
- Apa yang ingin kamu pelajari lebih lanjut?

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XII) S1 Pert 5**
