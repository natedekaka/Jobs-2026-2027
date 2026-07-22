# Rancangan Pembelajaran Terdiferensiasi — Fase F Kelas 11
## Materi: Pengolahan Data Bervolume Besar dan Analisis Data

---

### 1. Tujuan Pembelajaran

1.1 Memahami konsep data bervolume besar dan karakteristiknya (volume, *variety*, *velocity*).  
1.2 Mengidentifikasi dan memanfaatkan sumber data terbuka, terpercaya, dan legal.  
1.3 Mengolah data bervolume besar menggunakan perangkat lunak pengolah data (Spreadsheet, Python, atau *tools* sederhana).  
1.4 Menyajikan data dalam bentuk visualisasi yang informatif.  
1.5 Membuat prediksi dan pengambilan keputusan berdasarkan data secara efektif, efisien, dan optimal.  
1.6 Mengevaluasi kebenaran konten menggunakan verifikasi teks, gambar, dan video.

---

### 2. Kompetensi Prasyarat

| No | Kompetensi Prasyarat | Keterkaitan |
|----|----------------------|-------------|
| 1 | Peserta didik mampu menggunakan *spreadsheet* dasar (Fase E) | Prasyarat pengolahan data |
| 2 | Peserta didik memahami konsep data, informasi, dan struktur data (Fase E) | Dasar analisis data |
| 3 | Peserta didik memiliki kemampuan literasi informasi dasar | Prasyarat verifikasi data dan sumber |

---

### 3. Asesmen Awal

#### 3.1 Instrumen Asesmen Awal

**Bentuk:** Tugas praktik *spreadsheet* + soal konsep data + studi kasus verifikasi.

**Tugas Praktik:**
> Berikan file *spreadsheet* berisi 50 baris data (misal: data nilai siswa). Minta peserta didik:
> 1. Menghitung rata-rata, nilai tertinggi, dan terendah
> 2. Membuat grafik sederhana dari data tersebut
> 3. Menuliskan 1 kesimpulan dari data

**Soal Konsep:**
1. "Apa yang dimaksud dengan data *volume besar*? Berikan contoh!"
2. "Bagaimana cara memastikan suatu sumber data dapat dipercaya?"
3. "Jika kamu memiliki data penjualan toko selama 1 tahun, informasi apa yang bisa kamu peroleh?"

**Studi Kasus Verifikasi:**
> Kamu menemukan *postingan* di media sosial yang menyatakan "90% siswa di Indonesia lebih suka belajar online". Postingan tersebut menyertakan grafik. Apa yang harus kamu lakukan untuk memverifikasi kebenaran klaim ini?

#### 3.2 Kriteria Kesiapan Belajar

| Kondisi | Kategori | Tindak Lanjut |
|---------|----------|---------------|
| Belum mahir *spreadsheet*, kesimpulan dangkal, verifikasi parsial | **Kurang Siap** | Tutorial *spreadsheet* dasar + latihan data sederhana |
| Mampu operasi dasar *spreadsheet*, kesimpulan cukup, verifikasi dengan 1 cara | **Cukup Siap** | Pengenalan fungsi lanjutan + visualisasi + verifikasi multi-sumber |
| Mahir *spreadsheet*, kesimpulan analitis, verifikasi sistematis | **Sudah Siap** | Eksplorasi data besar dengan Python/Google Colab + analisis prediktif |

---

### 4. Rancangan Diferensiasi

#### 4.1 Diferensiasi Konten

| Kelompok | Sumber Belajar | Kompleksitas |
|----------|---------------|--------------|
| **Kurang Siap** | Infografis "Data Besar di Sekitar Kita" + video tutorial *spreadsheet* + lembar kerja bertahap | Visual, praktis, bertahap |
| **Cukup Siap** | Modul fungsi *spreadsheet* lanjutan (*vlookup*, *pivot table*) + artikel sumber data terbuka + contoh visualisasi | Semi-abstrak, aplikatif |
| **Sudah Siap** | Dokumentasi Python *pandas*/*matplotlib* + dataset publik (Kaggle/data.go.id) + artikel prediksi berbasis data | Abstrak, teknis, eksploratif |

#### 4.2 Diferensiasi Proses

| Kelompok | Aktivitas Pembelajaran | Pendampingan |
|----------|------------------------|--------------|
| **Kurang Siap** | Mengolah data kelas (nilai, tinggi badan, hobi) dengan *spreadsheet*: input data → hitung rata-rata → buat grafik batang | Langkah demi langkah, contoh langsung, *template* disediakan |
| **Cukup Siap** | Mengunduh dataset publik (data cuaca/data.go.id) → membersihkan data → membuat *pivot table* → 3 visualisasi → menarik kesimpulan | *Scaffolding* berupa panduan fungsi *spreadsheet* |
| **Sudah Siap** | Mengolah dataset publik dengan Python (*pandas*): *cleaning*, *exploratory data analysis*, visualisasi, dan prediksi sederhana (*linear regression*) | Mandiri, pendidik sebagai *code reviewer* |

#### 4.3 Diferensiasi Produk

| Kelompok | Bentuk Produk | Kriteria |
|----------|--------------|----------|
| **Kurang Siap** | Laporan 1 halaman: data diolah dalam tabel + 1 grafik + 1 kesimpulan | Tabel benar, grafik sesuai, kesimpulan relevan |
| **Cukup Siap** | Dashboard/*infografis* digital: *pivot table* + 3 visualisasi + analisis + rekomendasi | Visualisasi variatif, analisis logis, rekomendasi berdasar data |
| **Sudah Siap** | Notebook Python (Google Colab): *data cleaning* → EDA → visualisasi → model prediksi → laporan eksekutif | Kode rapi + visualisasi + model + interpretasi |

---

### 5. Pengelompokan Fleksibel

- Praktik *spreadsheet* dilakukan berpasangan (saling memeriksa).
- Kelompok proyek data dibentuk heterogen: anggota yang sudah siap membantu yang kurang siap dalam teknis *spreadsheet*.
- Tantangan tambahan untuk kelompok sudah siap: menggunakan API publik untuk mengambil data *real-time*.

---

### 6. Asesmen Sumatif (Akhir Materi)

| Indikator | Perlu Perbaikan | Cukup | Baik | Sangat Baik |
|-----------|----------------|-------|------|-------------|
| Mengolah data | Input manual | Fungsi dasar | Fungsi lanjutan (*vlookup*, *pivot*) | Python *pandas* |
| Visualisasi data | 1 grafik | 2-3 grafik sesuai | 3+ grafik variatif + relevan | Visualisasi interaktif/dashboard |
| Analisis & prediksi | Kesimpulan dangkal | 1 kesimpulan berdasar data | 2-3 kesimpulan + rekomendasi | Analisis + prediksi + rekomendasi strategis |
| Verifikasi konten | Tidak bisa verifikasi | Verifikasi 1 sumber | Verifikasi multi-sumber | Verifikasi sistematis + *lateral reading* |
