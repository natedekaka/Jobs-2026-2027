# Rancangan Pembelajaran Terdiferensiasi — Fase F Kelas 11
## Materi: Strategi Algoritmik Dasar

---

### 1. Tujuan Pembelajaran

1.1 Memahami konsep strategi algoritmik (*divide and conquer*, *greedy*, *brute force*, dll).  
1.2 Menganalisis suatu persoalan untuk menghasilkan beberapa alternatif solusi dengan strategi algoritmik yang berbeda.  
1.3 Memberikan justifikasi efisiensi, kelebihan, dan keterbatasan dari setiap alternatif solusi.  
1.4 Memilih dan menerapkan solusi terbaik, paling efisien, dan optimal.  
1.5 Menuliskan algoritma yang efisien, efektif, dan optimal.

---

### 2. Kompetensi Prasyarat

| No | Kompetensi Prasyarat | Keterkaitan |
|----|----------------------|-------------|
| 1 | Peserta didik menguasai algoritma pencarian dan pengurutan dasar (Fase E) | Prasyarat untuk membandingkan efisiensi algoritma |
| 2 | Peserta didik memahami konsep pseudocode dan logika pemrograman | Dasar penulisan solusi algoritmik |
| 3 | Peserta didik mampu mengenali pola dan dekomposisi masalah | Prasyarat strategi *divide and conquer* |

---

### 3. Asesmen Awal

#### 3.1 Instrumen Asesmen Awal

**Bentuk:** Tes diagnostik (2 soal pemecahan masalah) + wawancara singkat.

**Soal 1 — Brute Force:**
> "Temukan angka 75 dalam daftar berikut: [12, 45, 67, 75, 89, 90, 23, 34, 56, 78]. Jelaskan caramu! Bisakah kamu menemukan cara yang lebih cepat?"

**Soal 2 — Strategi:**
> "Kamu memiliki 8 koin yang tampak sama, tetapi salah satunya lebih ringan. Kamu memiliki timbangan dua lengan. Berapa kali minimal kamu perlu menimbang untuk menemukan koin palsu? Jelaskan strategimu!"

**Wawancara Singkat:**
> "Apa yang kamu ketahui tentang algoritma yang efisien? Bagaimana cara mengukur apakah suatu algoritma lebih baik dari yang lain?"

#### 3.2 Kriteria Kesiapan Belajar

| Kondisi | Kategori | Tindak Lanjut |
|---------|----------|---------------|
| Hanya menggunakan pendekatan coba-coba, belum bisa membandingkan strategi, tidak memahami efisiensi | **Kurang Siap** | *Games* dan teka-teki berbasis strategi (koin palsu, menara Hanoi) secara *unplugged* |
| Mampu menemukan solusi tetapi hanya 1 strategi, pemahaman efisiensi masih intuitif | **Cukup Siap** | Pengenalan 2-3 strategi algoritmik dengan contoh nyata dan perbandingan sederhana |
| Mampu menemukan >1 strategi dan memilih yang terbaik, memahami konsep efisiensi | **Sudah Siap** | Analisis Big-O, perbandingan formal, dan implementasi strategi dalam kode |

---

### 4. Rancangan Diferensiasi

#### 4.1 Diferensiasi Konten

| Kelompok | Sumber Belajar | Kompleksitas |
|----------|---------------|--------------|
| **Kurang Siap** | Kartu teka-teki strategi + video animasi *divide and conquer* dengan analogi cokelat pecah + poster perbandingan strategi | Konkret, bergambar, analogi sehari-hari |
| **Cukup Siap** | Modul strategi algoritmik dengan contoh + tabel perbandingan kompleksitas + LKPD studi kasus | Terstruktur, contoh nyata |
| **Sudah Siap** | Buku teks algoritma + jurnal/artikel tentang kompleksitas + soal tantangan dari Bebras/OSN | Abstrak, menantang |

#### 4.2 Diferensiasi Proses

| Kelompok | Aktivitas Pembelajaran | Pendampingan |
|----------|------------------------|--------------|
| **Kurang Siap** | Bermain "menara Hanoi" dengan piring/kardus — menemukan pola langkah minimal; teka-teki koin palsu dengan timbangan sungguhan | Didampingi, eksplorasi terpandu |
| **Cukup Siap** | Studi kasus berkelompok: menyelesaikan 1 persoalan dengan 2-3 strategi berbeda; mendokumentasikan perbedaan jumlah langkah | *Scaffolding* berupa tabel perbandingan |
| **Sudah Siap** | Analisis Big-O dari algoritma *sorting*/*searching* yang sudah dikenal; implementasi strategi *divide and conquer* dalam kode Python | Mandiri, pendidik sebagai *reviewer* |

#### 4.3 Diferensiasi Produk

| Kelompok | Bentuk Produk | Kriteria |
|----------|--------------|----------|
| **Kurang Siap** | Poster analogi strategi algoritmik (misal: *greedy* = ambil permen sebanyak-banyaknya sekarang) | Menjelaskan 1 strategi dengan analogi benar |
| **Cukup Siap** | Laporan perbandingan 2-3 strategi untuk 1 persoalan (disertai tabel langkah dan kesimpulan) | Membandingkan minimal 2 strategi dengan data |
| **Sudah Siap** | Program Python yang menerapkan 2 strategi berbeda untuk masalah yang sama + analisis Big-O + rekomendasi | Kode berjalan + analisis kompleksitas + justifikasi |

---

### 5. Pengelompokan Fleksibel

- Kelompok teka-teki bersifat homogen untuk memberikan tantangan sesuai level.
- Kelompok analisis bersifat heterogen agar terjadi transfer pengetahuan.
- Peserta didik yang sudah siap dapat merancang soal tantangan untuk kelompok lain.

---

### 6. Asesmen Sumatif (Akhir Materi)

| Indikator | Perlu Perbaikan | Cukup | Baik | Sangat Baik |
|-----------|----------------|-------|------|-------------|
| Memahami strategi algoritmik | Menyebut 1 strategi | Menyebut 2 strategi | Menyebut 3 strategi + contoh | Menyebut >3 strategi + kapan digunakan |
| Menganalisis persoalan | Solusi tunggal | >1 solusi tanpa justifikasi | >1 solusi + justifikasi | >1 solusi + justifikasi + analisis Big-O |
| Efisiensi algoritma | Tidak memahami | Intuitif benar | Menghitung langkah | Analisis Big-O formal |
| Implementasi | Tidak bisa | Dengan panduan | Mandiri | Mandiri + optimal |
