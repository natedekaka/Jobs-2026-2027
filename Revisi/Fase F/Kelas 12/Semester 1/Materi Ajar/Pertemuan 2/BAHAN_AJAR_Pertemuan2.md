# BAHAN AJAR – PERTEMUAN 2 (S1)
## Pivot Table
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*



### 🧠 Memahami — Membangun Pemahaman Awal

## A. Tujuan Pembelajaran
Setelah mempelajari materi ini, siswa mampu:
1. Menjelaskan fungsi Pivot Table dalam analisis data
2. Membuat Pivot Table dari data mentah (30+ baris)
3. Menggunakan slicer dan timeline untuk filter interaktif
4. Menerapkan sort, filter, dan group dalam Pivot Table

## B. Apa Itu Pivot Table?
Pivot Table adalah fitur Excel yang digunakan untuk meringkas, mengelompokkan, menganalisis, dan menampilkan data dalam jumlah besar — tanpa mengubah data asli.

**Kapan menggunakan Pivot Table?**
- Data: 100+ baris, banyak kategori
- Tujuan: rekap per kategori, perbandingan, tren
- Contoh: penjualan per produk, nilai per kelas, pengunjung per bulan

## C. Syarat Data untuk Pivot Table
1. Data dalam bentuk tabel rapi (setiap kolom punya header unik)
2. Tidak ada merged cells di area data
3. Tidak ada baris/kolom kosong di tengah data
4. Tipe data konsisten (kolom angka semua angka, teks semua teks)

## D. Langkah Membuat Pivot Table
1. Blok seluruh data (termasuk header)
2. Insert → PivotTable → pilih New Worksheet → OK
3. Akan muncul PivotTable Fields panel di sebelah kanan
4. Drag and drop field ke salah satu 4 area:
   - Rows (Baris): kategori yang ingin dianalisis (contoh: Nama Produk)
   - Columns (Kolom): kategori kedua (opsional, contoh: Bulan)
   - Values (Nilai): data yang dihitung (contoh: Sum Total Penjualan)
   - Filters (Saring): filter global (contoh: Tahun)

## E. Contoh Praktik — Data Penjualan
Buat data 30 baris dengan kolom:
| Tanggal | Produk | Kategori | Qty | Harga | Total |
Kolom Total = Qty × Harga

**Analisis 1: Total per Produk**
- Rows: Produk
- Values: Sum of Total
- Hasil: lihat produk mana paling laris

**Analisis 2: Transaksi per Kategori**
- Rows: Kategori
- Values: Count of Qty
- Hasil: kategori mana paling sering dibeli

**Analisis 3: Matrix Produk × Kategori**
- Rows: Produk
- Columns: Kategori
- Values: Sum of Total
- Hasil: lihat perbandingan per produk dan kategori

**Analisis 4: Tren Bulanan**
1. Group by Bulan:
   - Klik kanan pada tanggal → Group → pilih Months → OK
   - Untuk grouping multiple: pilih Months, Quarters, Years
2. Rows: Bulan (hasil grouping)
3. Values: Sum of Total
4. Insert Line Chart → PivotChart

## F. Fitur Lanjutan Pivot Table

**Sort:** Klik dropdown di Row Labels → Sort A-Z atau Z-A
- Sort by Value: More Sort Options → sort berdasarkan nilai total

**Filter:** Klik dropdown → centang/centang kategori tertentu
- Berguna untuk: tampilkan hanya 1 kategori, sembunyikan 0

**Group:**
- Angka: group umur (0-10, 11-20, dst)
- Tanggal: group per bulan, kuartal, tahun
- Manual: select baris → kanan → Group

**Slicer (Filter Visual):**
1. Klik Pivot Table
2. PivotTable Analyze → Insert Slicer
3. Pilih field: Produk, Kategori, Bulan → OK
4. Klik tombol slicer untuk filter data Pivot
5. Kelebihan: bisa connect ke beberapa Pivot Table sekaligus

**Timeline (Filter Waktu):**
1. PivotTable Analyze → Insert Timeline
2. Pilih field tanggal → OK
3. Geser slider untuk filter rentang waktu

**Calculated Field (Kolom Kustom di Pivot):**
1. Klik Pivot → PivotTable Analyze → Fields → Calculated Field
2. Nama: "Profit", Formula: =Total - (Total*0.7)
3. Hasil: kolom baru muncul di Pivot Table

**Refresh Pivot Table:**
- Jika data sumber berubah: kanan → Refresh
- Atau: PivotTable Analyze → Refresh
- Saat buka file: Data → Refresh All

## G. Format Pivot Table
1. Design → Report Layout → Show in Tabular Form (tampilan baris rapi)
2. Design → Grand Totals → On for Rows and Columns
3. Right-click → Number Format → pilih format Rp atau angka desimal

## H. Tantangan
1. Buat Pivot Table dari 30 data: total penjualan per kategori + slicer
2. Group data per bulan, tampilkan dalam Line Chart
3. Tambahkan Calculated Field untuk profit (asumsi margin 30%)
4. Desain rapi dengan format Rp dan judul tabel


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
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XII) S1 Pert 2**
