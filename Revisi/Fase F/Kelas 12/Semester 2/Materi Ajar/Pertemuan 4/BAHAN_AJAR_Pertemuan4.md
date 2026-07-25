# BAHAN AJAR – PERTEMUAN 4 (S2)
## Workshop — Analisis Data
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*



### 🧠 Memahami — Membangun Pemahaman Awal

## A. Tujuan Pembelajaran
Setelah mempelajari materi ini, siswa mampu:
1. Menggunakan Pivot Table untuk meringkas data survei
2. Membuat visualisasi data (bar chart, pie chart, line chart)
3. Menginterpretasikan hasil analisis
4. Menarik kesimpulan berdasarkan data

## B. Workshop 2: Analisis Data

**Review Pivot Table:**
Pivot Table = ringkas data mentah → tabel ringkasan

**Langkah Pivot:**
1. Blok data bersih → Insert → PivotTable → New Worksheet
2. Drag field ke area sesuai analisis

**Analisis Wajib untuk Proyek:**
| Analisis | Pivot Rows | Pivot Values | Grafik |
|----------|------------|--------------|--------|
| Perbandingan per kelas | Kelas | Count/Average | Bar/Column |
| Kategori favorit | Genre/Kategori | Count | Pie |
| Rata-rata numerik | Kelas | Average | Column |
| Tren/frekuensi | Kategori | Count | Bar |

**Contoh Analisis Survei Minat Baca:**
1. **Rata-rata buku/bulan per kelas**
   - Rows: Kelas, Values: Average of Buku/bulan
   - Interpretasi: "Kelas XI-A rata-rata 3.5 buku/bulan, tertinggi dari semua kelas"
2. **Genre favorit**
   - Rows: Genre, Values: Count
   - Pie chart: proporsi
   - Interpretasi: "Fiksi adalah genre paling populer (45%)"
3. **Hubungan kelas dan waktu baca**
   - Rows: Kelas, Columns: Waktu_baca, Values: Count
   - Interpretasi: "Kelas XII lebih banyak membaca >2 jam/hari"

## C. Membuat Grafik dari Pivot Table
1. Klik di dalam Pivot Table
2. PivotTable Analyze → PivotChart
3. Pilih jenis:
   - Column: perbandingan kategori
   - Pie: proporsi
   - Bar: perbandingan horizontal
   - Line: tren (jika data waktu)

## D. Interpretasi Data
Setelah grafik jadi, tulis interpretasi untuk setiap analisis:

**Template Interpretasi:**
"Berdasarkan grafik [judul grafik], dapat dilihat bahwa [temuan utama]. [Kategori A] memiliki [nilai] lebih [tinggi/rendah] dibanding [kategori B]. Hal ini menunjukkan bahwa [kesimpulan]. Kemungkinan penyebab: [alasan]. Rekomendasi: [saran]."

**Contoh:**
"Berdasarkan grafik Rata-rata Buku per Kelas, dapat dilihat bahwa kelas XI-A memiliki rata-rata 3.5 buku/bulan, lebih tinggi dari kelas XI-B (2.1 buku/bulan). Hal ini menunjukkan minat baca kelas XI-A lebih baik. Kemungkinan penyebab: kelas XI-A memiliki pojok baca yang aktif. Rekomendasi: kelas XI-B perlu program literasi tambahan."

## E. Output Pertemuan 4
1. Sheet "Analisis" di Excel berisi:
   - 3 Pivot Table
   - 3 Chart
   - Interpretasi di bawah tiap chart
2. Simpan sebagai "Analisis_Proyek_NamaKelompok.xlsx"


### 🔧 Mengaplikasi — Praktik & Penerapan

## F. Tugas
1. Buat 3 Pivot Table dan 3 Chart
2. Tulis interpretasi tiap analisis (3-4 kalimat)
3. Upload ke folder Google Drive kelompok


### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagaimana konsep ini terkait dengan materi sebelumnya?
- Skala pemahaman diri: ___/10
- Apa yang ingin kamu pelajari lebih lanjut?

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XII) S2 Pert 4**
