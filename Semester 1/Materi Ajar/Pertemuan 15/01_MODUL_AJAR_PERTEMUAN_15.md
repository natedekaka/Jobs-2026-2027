# MODUL AJAR INFORMATIKA – FASE E (KELAS X)

## Informasi Umum

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | E / X |
| **Semester** | 1 (Ganjil) |
| **Pertemuan ke-** | 15 |
| **Alokasi Waktu** | 2 JP × 45 menit (90 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | **SMA Negeri 6 Cimahi** |

---

## Profil Pelajar Pancasila

| Dimensi | Indikator |
|---|---|
| Bernalar Kritis | Menerapkan teknik validasi dan verifikasi data secara sistematis |
| Mandiri | Membersihkan dataset secara cermat dan bertanggung jawab |
| Kreatif | Menemukan solusi untuk memperbaiki data bermasalah |

---

## Sarana & Prasarana

| Sarana | Keterangan |
|---|---|
| Lab komputer / laptop | 1 unit per 2 siswa |
| Aplikasi | Excel / Google Sheets |
| Dataset kotor | Dari Pertemuan 14 + dataset baru (lebih besar) |
| Proyektor / LCD | Untuk demo |

---

## Tujuan Pembelajaran (TP 1.2 — Sumatif)

| TP | Indikator Ketercapaian Tujuan Pembelajaran (IKTP) |
|---|---|
| **BK 1.2:** Mampu melakukan validasi, verifikasi, dan data cleansing pada dataset sederhana | 1.2.5 Melakukan validasi data (format, tipe, rentang)<br>1.2.6 Melakukan verifikasi data (kebenaran, konsistensi)<br>1.2.7 Membersihkan data menggunakan fitur spreadsheet (filter, sort, remove duplicates, find & replace)<br>1.2.8 Menghasilkan dataset bersih yang siap diolah |

---

## Peta Kompetensi

```
Pertemuan 15 — Validasi, Verifikasi & Data Cleansing (Sumatif)
│
├── Pendahuluan (10 menit)
│   ├── Review tugas GIGO: diskusi berita
│   └── Apersepsi: "Kita bersihkan dataset kotor kemarin!"
│
├── Inti (65 menit)
│   ├── Memahami (10 menit)
│   │   ├── Validasi vs Verifikasi
│   │   └── Demo teknik cleansing (filter, remove dupes, find&replace)
│   │
│   ├── Mengaplikasi (50 menit) — PROYEK SUMATIF
│   │   ├── [5'] Persiapan: buka dataset + analisis
│   │   ├── [15'] Validasi: format, tipe, rentang
│   │   ├── [15'] Verifikasi & cleansing
│   │   └── [15'] Final: dataset bersih + laporan
│   │
│   └── Merefleksi (5 menit)
│       └── Perbandingan before-after
│
└── Penutup (15 menit)
```

---

## Langkah Pembelajaran

### Pembukaan (10 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 2 menit |
| 2. **Review tugas**: 2–3 siswa ceritakan berita GIGO yang ditemukan | 5 menit |
| 3. **Apersepsi**: "Kemarin kita menemukan ~20 masalah dalam 15 baris data. Hari ini kita **bersihkan** dataset itu. Setelah bersih, data siap diolah!" | 3 menit |

### Inti (65 menit)

#### Memahami (berkesadaran, menggembirakan) — 10 menit

1. **Validasi vs Verifikasi (5 menit)**

   | Aspek | Validasi | Verifikasi |
   |---|---|---|
   | **Definisi** | Memeriksa apakah data **sesuai aturan/format** | Memeriksa apakah data **sesuai kenyataan** |
   | **Pertanyaan** | "Apakah formatnya benar?" | "Apakah isinya benar?" |
   | **Contoh** | Tanggal harus DD-MM-YYYY | Tanggal lahir benar-benar 15-03-2009 |
   | **Alat** | Data validation, conditional formatting | Cross-check sumber asli |
   | **Otomatis?** | Bisa otomatis (rules) | Butuh manual (sumber eksternal) |

   **Contoh:**
   - **Validasi**: Nilai harus 0–100. Jika ada nilai 200 → ❌
   - **Verifikasi**: Nama "Andi Pratama" — apakah benar nama itu? Cek dokumen asli.

2. **Teknik Data Cleansing (5 menit) — Demo Cepat**

   | Fitur Spreadsheet | Fungsi | Demo |
   |---|---|---|
   | **Filter** | Menyaring baris berdasarkan kondisi | Lihat semua missing value |
   | **Sort** | Mengurutkan data | Temukan outlier dengan mudah |
   | **Remove Duplicates** | Hapus baris duplikat | Hapus Andi & Budi yang dobel |
   | **Find & Replace** | Cari dan ganti nilai | "x-1" → "X-1" |
   | **Data Validation** | Batasi input (hanya angka, range) | Nilai hanya 0–100 |
   | **Conditional Formatting** | Tandai otomatis data bermasalah | Warna merah untuk invalid |
   | **TRIM()** | Hapus spasi berlebih | `"Cimahi "` → `"Cimahi"` |
   | **UPPER() / LOWER() / PROPER()** | Standarisasi huruf | `"x-1"` → `"X-1"` |

#### Mengaplikasi (bermakna, menggembirakan) — 50 menit (Proyek Sumatif)

3. **Proyek: Data Cleansing (50 menit) — Berpasangan**

   **Dataset:** Dataset Pertemuan 14 + Dataset baru (10 baris tambahan) — total 25 baris.

   **Tahapan Proyek:**

   | Tahap | Waktu | Aktivitas |
   |---|---|---|
   | **1. Persiapan** | 5 menit | Buka dataset, analisis masalah, siapkan tabel laporan |
   | **2. Validasi** | 15 menit | Terapkan aturan validasi: format tanggal standar (DD-MM-YYYY), nilai 0–100, No HP 10–13 digit, kelas format "X-1" |
   | **3. Verifikasi & Cleansing** | 15 menit | Hapus duplikat, isi missing value (jika bisa), koreksi inkonsistensi, tandai outlier, perbaiki format |
   | **4. Final** | 15 menit | Dataset bersih + laporan perubahan |

   **Detail Tahapan:**

   **Tahap 2 — Validasi:**
   | Aturan Validasi | Kolom | Pengecekan |
   |---|---|---|
   | Format tanggal | Tgl Lahir | DD-MM-YYYY (atau YYYY-MM-DD konsisten) |
   | Range nilai | Nilai | 0–100 (angka) |
   | Format No HP | No HP | 10–13 digit, hanya angka |
   | Format kelas | Kelas | "X-1", "X-2", "X-3" |
   | Kolom wajib | Nama, Kelas, Tgl Lahir | Tidak boleh kosong |

   **Tahap 3 — Verifikasi & Cleansing:**
   | Masalah | Teknik | Contoh |
   |---|---|---|
   | **Duplikat** | Data → Remove Duplicates | Andi (2×) → 1 baris |
   | **Format tanggal** | Find & Replace / Text to Columns | "2009-05-20" → "20-05-2009" |
   | **Kelas inkonsisten** | Find & Replace | "x-1" → "X-1" |
   | **Spasi berlebih** | TRIM() | |
   | **Missing value** | Isi jika tahu, hapus jika tidak | |
   | **Outlier / Invalid** | Koreksi / tandai | Nilai "-5" → hapus |
   | **Huruf besar/kecil** | PROPER() / UPPER() | "cimahi" → "Cimahi" |

   **Tahap 4 — Final:**
   Buat **sheet terpisah** bernama "CLEAN" yang berisi dataset yang sudah dibersihkan.
   
   **Laporan (di LKPD atau sheet "LOG"):**
   | No | Masalah | Teknik Cleansing | Baris Terdampak | Hasil |
   |---|---|---|---|---|

4. **Hasil Akhir yang Dikumpulkan:**
   - File spreadsheet dengan 2 sheet: **RAW** (asli) dan **CLEAN** (bersih)
   - Sheet **LOG** berisi laporan perubahan (minimal 10 baris log)
   - Dataset bersih harus: tidak ada duplikat, format konsisten, tidak ada invalid value

#### Merefleksi (berkesadaran, bermakna) — 5 menit

5. **Perbandingan Before-After (5 menit)**
   - Guru tunjukkan 2–3 hasil kerja siswa (RAW vs CLEAN)
   - "Apa yang paling banyak kalian perbaiki?"
   - "Bagaimana perasaan kalian setelah membersihkan data?"

### Penutup (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman: "Validasi cek aturan, verifikasi cek kebenaran, cleansing perbaiki data. 3 langkah menuju data berkualitas." | 3 menit |
| 2. **Kumpulkan hasil proyek** (file spreadsheet) | 5 menit |
| 3. Sampaikan pertemuan depan: HAKI, Profesi IT & Digitalisasi Budaya (bagian terakhir sebelum PAS) | 3 menit |
| 4. Doa & salam | 4 menit |

---

## Asesmen — Sumatif

### Rubrik Proyek Data Cleansing

| Kriteria | Bobot | 1 | 2 | 3 | 4 |
|---|---|---|---|---|---|
| **Validasi** (aturan diterapkan) | 20% | Tidak ada validasi | 1–2 aturan | 3–4 aturan | Semua aturan (5) |
| **Cleansing** (perbaikan) | 30% | < 5 perbaikan | 5–9 perbaikan | 10–14 perbaikan | ≥ 15 perbaikan |
| **Dataset bersih** | 25% | Masih banyak masalah | Beberapa masalah | Hampir bersih | Bersih total, format rapi |
| **Laporan (LOG)** | 15% | Tidak ada | Ada tapi tidak lengkap | Lengkap | Detail + analisis |
| **Ketepatan teknik** | 10% | Tidak tepat | Sebagian tepat | Tepat | Tepat + efisien |

**Nilai Akhir = (Validasi × 20%) + (Cleansing × 30%) + (Bersih × 25%) + (Laporan × 15%) + (Teknik × 10%)**

---

## Lampiran: Dataset Tambahan

(File terpisah untuk dataset 25 baris)

---

**MGMP Informatika SMAN 6 Cimahi**
