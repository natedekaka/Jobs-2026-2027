# Rancangan Pembelajaran Terdiferensiasi — Fase F Kelas 12
## Materi: Kecerdasan Artifisial dan Machine Learning Dasar

---

### 1. Tujuan Pembelajaran

1.1 Memahami konsep dasar Kecerdasan Artifisial (AI) dan Machine Learning (ML).  
1.2 Membedakan jenis-jenis ML: *supervised learning*, *unsupervised learning*, *reinforcement learning*.  
1.3 Menggunakan *library*/*modul* AI/ML yang tersedia (misal: TensorFlow, scikit-learn, atau platform AI siap pakai).  
1.4 Menerapkan model ML sederhana untuk klasifikasi atau prediksi.  
1.5 Memahami implikasi etis penggunaan AI dalam kehidupan sehari-hari.  
1.6 Mengintegrasikan modul AI ke dalam program sederhana.

---

### 2. Kompetensi Prasyarat

| No | Kompetensi Prasyarat | Keterkaitan |
|----|----------------------|-------------|
| 1 | Peserta didik mampu membuat program dengan *library* eksternal | Prasyarat instalasi dan penggunaan modul AI |
| 2 | Peserta didik memahami analisis data dasar | Prasyarat *dataset* untuk ML |
| 3 | Peserta didik memahami konsep data dan statistik deskriptif | Prasyarat evaluasi model |
| 4 | Peserta didik mampu menggunakan Python atau bahasa pemrograman lain | Prasyarat implementasi |

---

### 3. Asesmen Awal

#### 3.1 Instrumen Asesmen Awal

**Bentuk:** Survei pengetahuan AI + studi kasus + *self-assessment* teknis.

**Survei Pengetahuan AI:**
- [ ] Saya tahu perbedaan AI, ML, dan *Deep Learning*
- [ ] Saya pernah menggunakan ChatGPT/Copilot/Gemini
- [ ] Saya tahu contoh AI dalam kehidupan sehari-hari
- [ ] Saya pernah melihat kode Python untuk ML
- [ ] Saya paham konsep "data latih" dan "data uji"

**Studi Kasus:**
> "Sebuah perusahaan ingin membuat sistem yang bisa membedakan gambar kucing dan anjing secara otomatis. Jelaskan langkah-langkah yang harus dilakukan!"

**Self-Assessment Teknis:**
1. "Sudah pernah install *library* Python? Sebutkan!"
2. "Apakah kamu paham konsep *array*/*list* dan *loop*?"
3. "Pernahkah kamu bekerja dengan file CSV atau *spreadsheet*?"

#### 3.2 Kriteria Kesiapan Belajar

| Kondisi | Kategori | Tindak Lanjut |
|---------|----------|---------------|
| Mencentang ≤ 1, studi kasus tidak tepat, belum pernah install *library* | **Kurang Siap** | Pengenalan AI konseptual dengan contoh nyata, *unplugged*, tanpa *coding* |
| Mencentang 2-3, studi kasus sebagian benar, pernah install *library* | **Cukup Siap** | Tutorial terbimbing menggunakan *platform* AI siap pakai (Teachable Machine, ML5.js) |
| Mencentang ≥ 4, studi kasus sistematis, bisa install *library* | **Sudah Siap** | Implementasi ML dengan Python (scikit-learn) pada dataset nyata |

---

### 4. Rancangan Diferensiasi

#### 4.1 Diferensiasi Konten

| Kelompok | Sumber Belajar | Kompleksitas |
|----------|---------------|--------------|
| **Kurang Siap** | Infografis "Apa itu AI?" + video contoh AI sehari-hari + kartu jenis-jenis AI + artikel etika AI | Visual, konseptual, tanpa kode |
| **Cukup Siap** | Tutorial Teachable Machine/ML5.js + *dataset* siap pakai + panduan *training* model visual | Semi-teknis, *drag-and-drop*, visual |
| **Sudah Siap** | Dokumentasi scikit-learn + *dataset* publik (Kaggle) + notebook Jupyter + artikel arsitektur ML | Teknis, kode, analitis |

#### 4.2 Diferensiasi Proses

| Kelompok | Aktivitas Pembelajaran | Pendampingan |
|----------|------------------------|--------------|
| **Kurang Siap** | Bermain "klasifikasi manusia": mengelompokkan gambar hewan/makanan secara manual → memahami konsep *labeling* dan *training* | Didampingi, analogi, *unplugged* |
| **Cukup Siap** | Menggunakan Teachable Machine: mengupload *dataset* gambar → *training* → *testing* → *export* model → integrasi ke halaman web sederhana | *Scaffolding* dengan panduan langkah |
| **Sudah Siap** | Membuat model klasifikasi dengan scikit-learn: *load dataset* → *preprocessing* → *train-test split* → *training* → evaluasi akurasi → prediksi | Mandiri, pendidik sebagai *reviewer* |

#### 4.3 Diferensiasi Produk

| Kelompok | Bentuk Produk | Kriteria |
|----------|--------------|----------|
| **Kurang Siap** | Poster "AI di Sekitarku" — menampilkan 5 contoh AI + cara kerjanya secara sederhana | 5 contoh nyata, penjelasan logis |
| **Cukup Siap** | Model klasifikasi gambar/suara menggunakan Teachable Machine yang bisa diakses via web | Model berjalan, akurasi ≥ 70%, bisa digunakan |
| **Sudah Siap** | Program Python dengan model ML (klasifikasi/regresi) + evaluasi akurasi + visualisasi hasil + laporan | Kode rapi, model terlatih, evaluasi, dokumentasi |

---

### 5. Pengelompokan Fleksibel

- Kelompok proyek AI berdasarkan minat (klasifikasi gambar, NLP sederhana, regresi data).
- Peserta didik yang sudah siap menjadi mentor bagi yang kurang siap saat praktik.
- Eksplorasi lanjutan: AI generatif, etika AI, bias dalam AI.

---

### 6. Asesmen Sumatif (Akhir Materi)

| Indikator | Perlu Perbaikan | Cukup | Baik | Sangat Baik |
|-----------|----------------|-------|------|-------------|
| Konsep AI/ML | Tidak paham perbedaan | Membedakan AI/ML/DL | Menjelaskan jenis ML + contoh | Menjelaskan + memilih tepat untuk kasus |
| Penggunaan modul AI | Tidak menggunakan | *Platform* visual | *Library* dengan panduan | *Library* mandiri + optimalisasi |
| Implementasi model | Tidak berhasil | Model berjalan, akurasi rendah | Model akurat + evaluasi | Model + *deployment* + dokumentasi |
| Etika AI | Tidak paham | Menyebut 1 isu etika | Menganalisis 2-3 isu etika | Analisis etika + rekomendasi |
