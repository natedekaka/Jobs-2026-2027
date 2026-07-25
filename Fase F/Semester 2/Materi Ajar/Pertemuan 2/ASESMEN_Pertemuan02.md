# ASESMEN – PERTEMUAN 2 (S2)
## Data Cleansing & Labeling

Informatika – Fase F / Kelas XI – SMA Negeri 6 Cimahi

---

## Rubrik Penilaian

### A. Identifikasi Masalah (Bobot 20%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Masalah ditemukan | 0–1 kolom | 2 kolom | 3–4 kolom | 5 kolom + analisis |
| Solusi | Tidak tepat | 1–2 tepat | 3–4 tepat | 5 tepat |

### B. Praktik Cleaning (Bobot 30%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Missing ditangani | Tidak | Sebagian | Semua | Semua + dokumentasi |
| Duplikat dihapus | Tidak | Sebagian | Semua | Semua + dicatat |
| Outlier dikoreksi | Tidak | Sebagian | Semua | Semua + alasan |
| Standarisasi | Tidak | 1–2 kolom | 3–4 kolom | 5 kolom + konsisten |

### C. Labeling Sentimen (Bobot 20%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Label benar | 0–3 | 4–6 | 7–9 | 10 + konsisten |
| Perbandingan kelompok | Tidak | Ada | Ada + diskusi | Ada + analisis perbedaan |

### D. Studi Kasus (Bobot 15%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Solusi | 0–1 tepat | 2 tepat | 3 tepat | 4 tepat + rinci |

### E. Refleksi & Tugas (Bobot 15%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Refleksi | Tidak diisi | 1 jawaban | 2 jawaban | 2 jawaban + mendalam |
| Tugas rumah | Tidak | Ada, minimal | Ada, lengkap | Ada, lengkap + screenshot |

---

## Kunci Jawaban

### Soal 1 — Identifikasi Masalah (contoh)

| Kolom | Masalah | Jumlah | Solusi |
|---|---|---|---|
| Nama | Typo, inconsistent case | 5 | `=PROPER()`, cek manual |
| Kelas | "X-A", " X-A", "XA", "10A" | 8 | Standarisasi → "X-A" |
| Nilai UTS | Kosong (3), >100 (1), -10 (1) | 5 | Isi rata-rata, koreksi/hapus |
| Nilai UAS | Kosong (2) | 2 | Isi rata-rata |
| Email | Format salah (2) | 2 | Koreksi/hapus |

### Soal 3 — Standarisasi

| Data Kotor | Hasil |
|---|---|
| "budi" | "Budi" |
| " X-A " | "X-A" |
| "BUDI SANTOSO" | "Budi Santoso" |
| "10A" | "X-A" |
| "siti.nurhaliza@" | "siti.nurhaliza@gmail.com" (atau hapus) |

### Soal 4 — Labeling Sentimen

| No | Komentar | Label |
|---|---|---|
| 1 | "Sekolahku keren banget!" | Positif |
| 2 | "Gurunya ramah dan sabar" | Positif |
| 3 | "Tugasnya banyak banget" | Negatif |
| 4 | "Kantinnya enak!" | Positif |
| 5 | "Belajar di sini biasa aja" | Netral |
| 6 | "Fasilitasnya lengkap" | Positif |
| 7 | "Ujiannya susah :(" | Negatif |
| 8 | "Teman-teman asyik" | Positif |
| 9 | "Parkirannya sempit" | Negatif |
| 10 | "Sekolahnya bersih dan nyaman" | Positif |

### Soal 6 — Studi Kasus Data Sekolah

| Masalah | Solusi |
|---|---|
| Alamat kosong (5%) | Isi dengan "Tidak Ada Data" atau cari dari sumber lain |
| Duplikat NPSN | Hapus duplikat, simpan 1 baris dengan data terlengkap |
| Format nama sekolah | Standarisasi: "SD Negeri 1" → "SDN 1 Cimahi" |
| Kode pos kosong | Cari referensi dari kecamatan/kelurahan |

---

**MGMP Informatika SMAN 6 Cimahi**
