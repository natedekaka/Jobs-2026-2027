# BAHAN AJAR – PERTEMUAN 4 (S1)
## Dashboard Excel
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*



### 🧠 Memahami — Membangun Pemahaman Awal

## A. Tujuan Pembelajaran
Setelah mempelajari materi ini, siswa mampu:
1. Menjelaskan komponen dashboard Excel (Pivot, Chart, Slicer, KPI, Timeline)
2. Membuat dashboard dari data penjualan/keuangan
3. Memilih jenis grafik yang tepat untuk setiap data
4. Menerapkan prinsip desain dashboard yang baik

## B. Apa Itu Dashboard?
Dashboard adalah tampilan visual yang merangkum data-data penting (Key Performance Indicators/KPI) dalam satu halaman/layar — sehingga pengguna bisa melihat kondisi bisnis atau proyek secara sekilas dan mengambil keputusan cepat.

**Analoginya:** Dashboard mobil — menunjukkan kecepatan, bensin, RPM, suhu — semua info penting dalam satu pandangan.

## C. 5 Komponen Utama Dashboard Excel
**1. Pivot Table — Ringkasan Data**
- Tempatkan Pivot Table sebagai sumber data utama
- Bisa beberapa Pivot Table untuk analisis berbeda
- Hubungan: Pivot Table → Chart

**2. Chart — Visualisasi Grafik**
- Bar/Column: perbandingan kategori (penjualan per produk)
- Line: tren waktu (penjualan per bulan)
- Pie: proporsi (market share)
- Combo: dua jenis data beda skala (bar + line)
- Stacked Bar: total + komposisi

**3. Slicer — Filter Interaktif**
- Tombol visual untuk menyaring data
- Bisa menghubungkan 1 slicer ke beberapa Pivot Table
- **Langkah:** PivotTable Analyze → Insert Slicer
- **Koneksi:** Klik kanan slicer → Report Connections → centang Pivot tujuan

**4. KPI Cards — Angka Penting**
Buat kotak dengan angka besar:
- Total Revenue: =SUM(penjualan[Total])
- Rata-rata Transaksi: =AVERAGE(penjualan[Total])
- Produk Terlaris: tampilkan via formula atau manual
- Persentase Target: =Total/Target

**5. Timeline — Filter Waktu**
- Filter tanggal dengan slider interaktif
- PivotTable Analyze → Insert Timeline

## D. Langkah Membuat Dashboard
1. **Persiapan Data:** Tabel rapi (30-100 baris) dengan header jelas
2. **Pivot Table 1:** Total per Produk (Baris: Produk, Nilai: Sum Total)
3. **Pivot Table 2:** Total per Bulan (Baris: Tanggal→Group Months, Nilai: Sum Total)
4. **Chart 1:** Column Chart dari Pivot 1
5. **Chart 2:** Line Chart dari Pivot 2
6. **Slicer:** Pilih field kategori, hubungkan ke kedua Pivot
7. **KPI Cards:** 3-4 angka penting di atas
8. **Layout & Format:**
   - Siapkan sheet baru bernama 'DASHBOARD'
   - Atur posisi: KPI di atas, chart di tengah, slicer di kanan
   - Warna konsisten (maks 3 warna)
   - Hide gridlines (View → Gridlines)
   - Hapus header baris/kolom

## E. Tips Desain Dashboard Profesional
1. **Hierarki:** Informasi paling penting di bagian atas (KPI cards)
2. **Konsistensi warna:** Pilih 2-3 warna, gunakan di seluruh dashboard
3. **White space:** Jangan penuh sesak — beri jarak antar komponen
4. **Ukuran font:** Judul 18pt, KPI 24pt, label chart 10pt
5. **Hapus elemen mengganggu:** Gridlines, row/column headers, scrollbars
6. **Tambahkan judul:** "Dashboard Penjualan Q1 2025"

## F. Contoh Layout Dashboard
```
+-----------------------------------------------------------+
|  [LOGO]      DASHBOARD PENJUALAN 2025          [Tanggal]   |
+-----------------------------------------------------------+
| [Total Rp 50jt] [Rata-rata 1.5jt] [Produk: Kopi] [Target] |
+----------------------------+-----------------------------+
| Penjualan per Produk (Bar) | Tren Bulanan (Line)         |
| [CHART]                    | [CHART]                     |
+----------------------------+-----------------------------+
| [Slicer: Kategori]         | [Timeline: 2024-2025]       |
+----------------------------+-----------------------------+
```

## G. Tantangan
1. Buat 30 data penjualan (Tanggal, Produk, Kategori, Qty, Harga, Total)
2. Buat dashboard dengan: 2 Pivot, 2 Chart, 1 Slicer, 3 KPI cards
3. Format rapi dengan tema warna pilihan
4. Siapkan dalam 1 sheet 'DASHBOARD' tanpa gridlines


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
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XII) S1 Pert 4**
