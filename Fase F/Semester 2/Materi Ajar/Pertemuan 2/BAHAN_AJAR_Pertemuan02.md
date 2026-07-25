# BAHAN AJAR – PERTEMUAN 2 (S2)
## Data Cleansing & Labeling

| TP | BK, AD — Pengolahan Data Bervolume Besar |
|---|---|

---

### A. MASALAH KUALITAS DATA

#### 1. Missing Values

Data kosong — tidak diisi saat pengumpulan.

| Penyebab | Contoh | Solusi |
|---|---|---|
| Responden tidak mau jawab | Survey: "Pendapatan?" | Isi dengan median |
| Error input | Sensor mati | Hapus baris tersebut |
| Tidak relevan | Pria → hamil? | Biarkan kosong (NA) |

**Dampak:**
- Rata-rata jadi bias
- Fungsi `AVERAGE` mengabaikan kosong (tapi jumlah sampel berkurang)
- Machine learning error

#### 2. Duplicates

Data yang sama muncul lebih dari sekali.

| Penyebab | Contoh |
|---|---|
| Error input ganda | "Budi" diinput 2× |
| Merge data dari sumber berbeda | Database A + Database B ada nama sama |
| Crawling/scraping ganda | Web scraping ambil halaman sama 2× |

#### 3. Outliers

Nilai yang sangat berbeda dari mayoritas data.

| Outlier | Contoh | Deteksi |
|---|---|---|
| Nilai 1000 (skala 0–100) | Kesalahan input | Filter + sort |
| Suhu 500°C di Indonesia | Sensor error | IQR: Q1 - 1.5*IQR s.d. Q3 + 1.5*IQR |
| Usia 200 tahun | Tidak wajar | Domain knowledge: usia max 120 |

#### 4. Inconsistent Data

Format yang tidak seragam.

| Kolom | Data Kotor | Standarisasi |
|---|---|---|
| Nama | "budi", "Budi", "BUDI", "budi santoso" | `=PROPER()` → "Budi Santoso" |
| Kelas | "X-A", " X-A", "XA", "10A", "X A" | Semua → "X-A" |
| Tanggal | "1/1/2026", "2026-01-01", "01-Jan-26" | Format ISO: 2026-01-01 |
| Alamat | "Jl.Merdeka", "Jalan Merdeka", "Jl. Merdeka" | Satu format: "Jl. Merdeka" |

---

### B. TEKNIK DATA CLEANING

#### Panduan Lengkap Google Sheets

| Tujuan | Langkah | Rumus / Menu |
|---|---|---|
| Cek missing | Filter kolom → cek (Blanks) | `=ISBLANK(A2)` |
| Isi missing (angka) | Cari rata-rata → isi | `=IF(ISBLANK(A2), AVERAGE(A:A), A2)` |
| Hapus baris kosong | Filter blok → Delete rows | Data → Create filter |
| Cek duplikat | Conditional formatting | Format → CF → `=COUNTIF(A:A,A1)>1` |
| Hapus duplikat | Data cleanup | Data → Data cleanup → Remove duplicates |
| Standarisasi teks | Ubah ke format seragam | `=UPPER()`, `=LOWER()`, `=PROPER()`, `=TRIM()` |
| Hapus spasi berlebih | Trim | `=TRIM(A2)` |
| Split kolom | Pisah data | Data → Split text to columns |
| Validasi data | Batasi input | Data → Data validation |

#### Mengukur "Kebersihan" Data

| Metrik | Arti | Target |
|---|---|---|
| Completeness | % data tidak kosong | > 95% |
| Uniqueness | % data unik | > 90% |
| Validity | % data valid (format benar) | > 98% |
| Consistency | % data konsisten format | 100% |

---

### C. DATA LABELING

#### Definisi

> **Labeling** = memberi label/kategori pada data mentah sehingga bisa digunakan untuk supervised machine learning.

#### Jenis Labeling

| Jenis | Deskripsi | Contoh |
|---|---|---|
| **Biner** | 2 kelas | Spam / Not Spam |
| **Multi-class** | > 2 kelas | Sentimen: Pos / Neu / Neg |
| **Multi-label** | 1 data → banyak label | Foto: [kucing, outdoor, siang] |
| **Regression** | Nilai kontinu | Harga rumah: Rp 500.000.000 |

#### Contoh Labeling — Sentimen

| Komentar | Label |
|---|---|
| "Produknya bagus sekali!" | Positif |
| "Pengiriman lambat" | Negatif |
| "Barang sesuai deskripsi" | Netral |
| "Mantap! rekomen!" | Positif |
| "Biasa aja sih" | Netral |

#### Inter-Annotator Agreement

> Dua orang labeler bisa berbeda pendapat. Semakin tinggi kesepakatan → semakin baik kualitas label.

| Agreement | Kualitas Label | Tindakan |
|---|---|---|
| > 90% | Sangat baik | Gunakan langsung |
| 70–90% | Baik | Diskusikan perbedaan |
| < 70% | Buruk | Perbaiki panduan labeling |

#### Tools Labeling

| Tool | Kelebihan |
|---|---|
| Google Sheets | Sederhana, manual |
| Label Studio | Open source, banyak format |
| Prodigy | Cepat, active learning |
| Roboflow | Labeling gambar |

---

### D. STUDI KASUS: CLEANING DATASET PENDUDUK

Dataset dari data.go.id "Jumlah Penduduk per Provinsi 2025"

| Masalah | Contoh Data Kotor | Tindakan Cleaning |
|---|---|---|
| Nama provinsi inkonsisten | "DKI JAKARTA", "Jakarta", "DKI Jakarta" | `=PROPER()` + standardisasi |
| Kode provinsi kosong | 1 baris kosong | Isi dengan kode yang sesuai |
| Jumlah penduduk -500 | Minus | Validasi sumber → isi ulang |
| Duplikat | "Jawa Barat" 2 baris | Hapus duplikat, jumlahkan |
| Format angka | "45.000.000" vs "45000000" | Hapus titik, format number |

---

### E. RANGKUMAN

| Langkah | Teknik |
|---|---|
| 1. Identifikasi masalah | Missing, duplikat, outlier, inkonsisten |
| 2. Cleaning | ISBLANK, COUNTIF, TRIM, PROPER, Remove duplicates |
| 3. Validasi | Cek completeness, uniqueness, validity |
| 4. Labeling | Beri label → siap untuk ML |
| 5. Dokumentasi | Catat setiap perubahan |

**Prinsip: Garbage In, Garbage Out!**

---

**MGMP Informatika SMAN 6 Cimahi**
