# LEMBAR KERJA PESERTA DIDIK (LKPD)
## Pertemuan 15 – Validasi, Verifikasi & Data Cleansing

| TP | BK 1.2 — Sumatif |
|---|---|
| Nama (1) | ____________________ |
| Nama (2) | ____________________ |
| Kelas | ____________________ |

---

### PROYEK DATA CLEANSING

**Dataset:** 25 baris data kotor (file: `DATASET_Proyek_15.csv`)

**Tujuan:** Hasilkan dataset BERSIH + laporan LOG.

---

### TAHAP 1: VALIDASI (cek aturan)

**Terapkan aturan validasi berikut. Catat pelanggaran yang ditemukan:**

| Aturan Validasi | Kolom | Jumlah Pelanggaran | Contoh Pelanggaran |
|---|---|---|---|
| Format tanggal konsisten | Tgl Lahir | | |
| Range nilai 0–100 (angka) | Nilai | | |
| No HP 10–13 digit (hanya angka) | No HP | | |
| Format kelas: X-1, X-2, X-3 | Kelas | | |
| Kolom wajib tidak boleh kosong | Semua | | |

---

### TAHAP 2: DATA CLEANSING

**Catat semua perubahan yang kamu lakukan di tabel LOG berikut.**

| No | Masalah | Teknik Cleansing | Baris | Sebelum | Sesudah |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |
| 6 | | | | | |
| 7 | | | | | |
| 8 | | | | | |
| 9 | | | | | |
| 10 | | | | | |
| 11 | | | | | |
| 12 | | | | | |
| 13 | | | | | |
| 14 | | | | | |

**Teknik yang bisa digunakan:**
- Remove Duplicates
- Find & Replace
- Filter → hapus/tandai
- Data Validation
- TRIM() / PROPER() / UPPER()
- Koreksi manual (jika tahu nilai sebenarnya)
- Hapus baris (jika data tidak bisa diperbaiki)

---

### TAHAP 3: HASIL AKHIR

**Statistik dataset:**

| Metrik | RAW | CLEAN |
|---|---|---|
| Jumlah baris | | |
| Jumlah duplikat | | |
| Jumlah missing value | | |
| Jumlah format error | | |
| Jumlah outlier | | |

**Skor kualitas data (1–10):** ___ / 10

---

### REFLEKSI

| Pertanyaan | Jawaban |
|---|---|
| Teknik cleansing paling berguna? | |
| Tantangan terbesar saat membersihkan data? | |
| Apa yang akan terjadi jika dataset ini tidak dibersihkan? | |
| Skala pemahaman data cleansing (1–10) | / 10 |

---

**MGMP Informatika SMAN 6 Cimahi**
