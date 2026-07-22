# Rancangan Pembelajaran Terdiferensiasi — Fase F Kelas 12
## Materi: Analisis Data Lanjut untuk Prediksi dan Pengambilan Keputusan

---

### 1. Tujuan Pembelajaran

1.1 Memanfaatkan sumber data terbuka, terpercaya, dan legal dari berbagai sumber.  
1.2 Melakukan *data cleaning* dan *preprocessing* pada dataset bervolume besar.  
1.3 Menerapkan teknik analisis data lanjut (regresi, klasifikasi, klastering) menggunakan *tools*/*library* yang tersedia.  
1.4 Membuat visualisasi data interaktif dan *dashboard* informatif.  
1.5 Membuat prediksi berdasarkan data historis menggunakan model sederhana.  
1.6 Menyusun rekomendasi dan pengambilan keputusan berbasis data.

---

### 2. Kompetensi Prasyarat

| No | Kompetensi Prasyarat | Keterkaitan |
|----|----------------------|-------------|
| 1 | Peserta didik mampu mengolah data dengan *spreadsheet*/*tools* (Fase 11) | Dasar analisis lanjut |
| 2 | Peserta didik memahami konsep statistik deskriptif | Prasyarat interpretasi data |
| 3 | Peserta didik mampu membuat visualisasi data dasar | Prasyarat *dashboard* |
| 4 | Peserta didik mengenal AI/ML dasar (materi AI) | Prasyarat model prediktif |

---

### 3. Asesmen Awal

#### 3.1 Instrumen Asesmen Awal

**Bentuk:** Studi kasus prediksi + kuis *tools* analisis + praktik singkat.

**Studi Kasus Prediksi:**
> "Kamu memiliki data penjualan es krim selama 1 tahun (suhu harian vs jumlah penjualan). Bagaimana cara memprediksi berapa banyak es krim yang harus disiapkan besok jika suhu diperkirakan 35°C?"

**Kuis Tools Analisis:**
- [ ] Saya bisa menggunakan *vlookup*/*pivot table*
- [ ] Saya pernah menggunakan Python *pandas*
- [ ] Saya tahu cara menggabungkan dua tabel data
- [ ] Saya pernah membuat grafik dengan 2 sumbu Y
- [ ] Saya paham korelasi antara dua variabel

**Praktik Singkat:**
> Berikan dataset kecil (10 baris) berisi data nilai belajar dan nilai ujian. Minta peserta didik membuat grafik *scatter* dan menjelaskan hubungan kedua variabel.

#### 3.2 Kriteria Kesiapan Belajar

| Kondisi | Kategori | Tindak Lanjut |
|---------|----------|---------------|
| Studi kasus tidak bisa, *tools* ≤ 1, grafik tidak tepat | **Kurang Siap** | *Review* statistik deskriptif dan *spreadsheet*; fokus interpretasi visual |
| Studi kasus cukup, *tools* 2-3, grafik tepat interpretasi sederhana | **Cukup Siap** | Pengenalan analisis regresi/korelasi dengan *spreadsheet*; lanjut ke Python |
| Studi kasus tepat, *tools* ≥ 4, analisis mendalam | **Sudah Siap** | Analisis prediktif dengan Python, *dashboard* interaktif, presentasi eksekutif |

---

### 4. Rancangan Diferensiasi

#### 4.1 Diferensiasi Konten

| Kelompok | Sumber Belajar | Kompleksitas |
|----------|---------------|--------------|
| **Kurang Siap** | Infografis "Membaca Grafik" + video korelasi vs kausalitas + lembar kerja interpretasi data + contoh *dashboard* sederhana | Visual, interpretatif, bertahap |
| **Cukup Siap** | Modul analisis regresi dengan *spreadsheet* + tutorial Python *pandas* dasar + dataset publik + contoh *dashboard* | Semi-teknis, terstruktur |
| **Sudah Siap** | Dokumentasi *pandas*/*matplotlib*/*seaborn* + *scikit-learn* untuk regresi + dataset Kaggle + artikel *data storytelling* | Teknis, eksploratif, profesional |

#### 4.2 Diferensiasi Proses

| Kelompok | Aktivitas Pembelajaran | Pendampingan |
|----------|------------------------|--------------|
| **Kurang Siap** | Menginterpretasikan grafik yang sudah jadi → menarik kesimpulan → membuat 1 grafik dari data kelas dengan *spreadsheet* | Didampingi, pertanyaan pemantik, *template* |
| **Cukup Siap** | Mencari dataset publik → *cleaning* data → analisis korelasi/regresi dengan *spreadsheet* → 3 visualisasi → kesimpulan dan rekomendasi | *Scaffolding* berupa panduan fungsi dan interpretasi |
| **Sudah Siap** | *Data pipeline* lengkap dengan Python: *scraping*/import → *cleaning* → EDA → model regresi/klasifikasi → *dashboard* interaktif → presentasi eksekutif | Mandiri, pendidik sebagai *reviewer* |

#### 4.3 Diferensiasi Produk

| Kelompok | Bentuk Produk | Kriteria |
|----------|--------------|----------|
| **Kurang Siap** | Laporan 1 halaman: dataset → 2 grafik → 2 kesimpulan → 1 rekomendasi | Grafik sesuai data, kesimpulan logis, rekomendasi relevan |
| **Cukup Siap** | *Dashboard* (Spreadsheet/Canva/Google Data Studio): *pivot table* + 3-4 visualisasi + analisis + rekomendasi berbasis data | Visualisasi variatif, analisis mendalam, rekomendasi terukur |
| **Sudah Siap** | Notebook Python (Google Colab) lengkap + *dashboard* (Tableau Public/Streamlit) + laporan eksekutif (PDF) | *End-to-end*: data → analisis → model → visualisasi → rekomendasi |

---

### 5. Pengelompokan Fleksibel

- Kelompok proyek data berdasarkan minat topik (pendidikan, kesehatan, lingkungan, ekonomi).
- Setiap kelompok memiliki *data analyst*, *visualizer*, *interpreter*, dan *presenter*.
- Hasil analisis dipresentasikan dalam *data expo* kelas.

---

### 6. Asesmen Sumatif (Akhir Materi)

| Indikator | Perlu Perbaikan | Cukup | Baik | Sangat Baik |
|-----------|----------------|-------|------|-------------|
| Sumber data | Asal-asalan | 1 sumber terpercaya | 2-3 sumber terpercaya | Sumber terbuka + legal + relevan |
| *Data cleaning* | Tidak dilakukan | Parsial | Sistematis (missing value, outlier) | Otomatis dengan kode + dokumentasi |
| Analisis data | Deskriptif | 1 teknik analisis | 2-3 teknik (korelasi, regresi) | Teknik lanjut + model prediktif |
| Visualisasi | 1 grafik | 2-3 grafik sesuai | *Dashboard* multi-visualisasi | Interaktif/ *storytelling* |
| Prediksi & keputusan | Tidak ada | Prediksi intuitif | Prediksi berdasar data + rekomendasi | Model + validasi + rekomendasi strategis |
