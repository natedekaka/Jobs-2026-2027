# MODUL AJAR INFORMATIKA – FASE F (KELAS XI)

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | F / XI |
| **Semester** | 1 (Ganjil) |
| **Pertemuan ke-** | 15 |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | SMA Negeri 6 Cimahi |
| **Materi Esensial** | Pengolahan Data Bervolume Besar |

---

## Tujuan Pembelajaran

| TP | IKTP |
|---|---|
| **BK, AP:** Mempraktikkan pengolahan data | 15.1 Melakukan pembersihan data (missing value, duplikat) |
| | 15.2 Menggunakan sorting dan filtering |
| | 15.3 Menghitung statistik dasar (mean, median, modus) |
| | 15.4 Membuat pivot table dan grafik sederhana |

---

## Langkah Pembelajaran

### Pembukaan (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 3 menit |
| 2. **Review**: "Pert 14: Big Data & Data Mining — teorinya. Hari ini: **Praktik!** Kita olah data sungguhan!" | 5 menit |
| 3. **Apersepsi**: "Kalian punya data nilai 500 siswa — bagaimana cara tahu rata-rata, nilai tertinggi, atau siapa yang remedial? Dengan alat pengolahan data!" | 7 menit |

### Inti (175 menit)

#### Memahami (50 menit)

**1. Alat Pengolahan Data (10 menit)**

| Alat | Kelebihan | Kekurangan |
|---|---|---|
| **Google Sheets** | Gratis, online, kolaborasi | Fitur terbatas untuk big data |
| **Excel** | Fitur lengkap | Berbayar |
| **Python Pandas** | Otomatis, bisa big data | Butuh coding |
| **Google Colab** | Gratis, Python online | Butuh koneksi internet |

**2. Teknik Dasar (15 menit)**

| Teknik | Cara | Fungsi/Kueri |
|---|---|---|
| **Sorting** | Urutkan data menaik/menurun | `=SORT()` atau Data→Sort |
| **Filtering** | Tampilkan data tertentu | Data→Create a filter |
| **Missing Values** | Cari data kosong | `=ISBLANK()` atau filter |
| **Duplicates** | Hapus duplikat | Data→Data cleanup |
| **Statistik** | Rata-rata, max, min | `=AVERAGE`, `=MAX`, `=MIN` |
| **Pivot Table** | Rangkum data | Data→Pivot table |
| **Chart** | Grafik | Insert→Chart |

**3. Studi Kasus — Data Nilai Siswa (25 menit)**
- Dataset: 40 siswa × 5 kolom (Nama, Kelas, Nilai UTS, Nilai UAS, Rata-rata)
- Demonstrasi langsung di Google Sheets:
  - Hitung rata-rata UTS dan UAS
  - Cari nilai tertinggi dan terendah
  - Filter siswa yang remedial (<75)
  - Buat pivot table rata-rata nilai per kelas
  - Buat grafik batang perbandingan per kelas

#### Mengaplikasi — Praktik (95 menit)

**4. Aktivitas 1 — Data Cleaning (20 menit) — Individu**
   - Buka Google Sheets / Excel
   - Import dataset (guru share link dataset nilai siswa)
   - Identifikasi: ada data kosong? ada duplikat? ada data anomali (nilai > 100)?
   - Bersihkan: isi data kosong dengan rata-rata, hapus duplikat

**5. Aktivitas 2 — Analisis Statistik (25 menit) — Individu**
   - Hitung: rata-rata, median, nilai tertinggi, nilai terendah
   - Filter: siswa dengan nilai ≥ 90 (layak pujian)
   - Filter: siswa dengan nilai < 75 (remedial)
   - Hitung berapa persen yang remedial

**6. Aktivitas 3 — Pivot Table & Grafik (30 menit) — Berpasangan**
   - Buat pivot table: rata-rata nilai per kelas
   - Buat pivot table: jumlah siswa remedial per kelas
   - Buat grafik batang: perbandingan rata-rata antar kelas
   - Buat grafik lingkaran: proporsi remedial vs lulus

**7. Aktivitas 4 — Interpretasi Data (20 menit) — Kelompok**
   - Diskusikan: "Kelas mana yang paling baik? Mana yang perlu perhatian?"
   - Tulis rekomendasi untuk guru: "Berdasarkan data, ..."
   - Presentasi (2 kelompok)

#### Merefleksi (15 menit)

**8. Refleksi Jurnal (15 menit)**
- 3 teknik pengolahan data yang dipelajari
- Fitur spreadsheet paling berguna?
- Apa tantangan saat mengolah data?

### Penutup (35 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman: Data cleaning → sorting → filtering → statistik → pivot → grafik | 10 menit |
| 2. Kuis lisan: fungsi spreadsheet untuk apa? (5 soal) | 10 menit |
| 3. Preview: "Pert 16: Visualisasi Data — grafik yang menarik & informatif" | 5 menit |
| 4. Tugas rumah: Selesaikan analisis data + screenshot hasil | 10 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Data cleaning | Tidak selesai | Sebagian | Semua benar | Semua + dokumentasi |
| Statistik | 0–2 benar | 3–4 benar | 5–6 benar | 6 benar + interpretasi |
| Pivot & grafik | Tidak buat | 1 pivot/grafik | 2 pivot/grafik | 3+ pivot/grafik + rapi |

---

**MGMP Informatika SMAN 6 Cimahi**
