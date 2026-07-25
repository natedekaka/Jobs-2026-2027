# ASESMEN – PERTEMUAN 14 (S2)
## Proyek Akhir — Python Pipeline

Informatika – Fase F / Kelas XI – SMA Negeri 6 Cimahi

---

## Rubrik Penilaian

### A. Load & Explore (Bobot 15%)

| Kriteria | 0 | 1 | 2 | 3 |
|---|---|---|---|---|
| Load CSV | Tidak | Error — tapi diperbaiki | Berhasil | Berhasil + cek path |
| Explore data | Tidak | head() saja | info() + describe() | info, describe, isnull, duplicated |

### B. Clean (Bobot 20%)

| Kriteria | 0 | 1 | 2 | 3 |
|---|---|---|---|---|
| Duplikat | Tidak | Ada kode | Berhasil hapus | Berhasil + verifikasi |
| Missing value | Tidak | Ada kode | Berhasil isi | Strategi tepat + alasan |
| Outlier | Tidak | Deteksi | Perbaiki | Perbaiki + verifikasi |

### C. Transform & Analyze (Bobot 25%)

| Kriteria | 0 | 1 | 2 | 3 |
|---|---|---|---|---|
| Kolom baru | Tidak | 1 kolom | 2 kolom | 3+ kolom (rata, grade, status) |
| Groupby | Tidak | Ada kode | Berhasil | Berhasil + interpretasi |
| Sorting | Tidak | Ada kode | Berhasil | Top + bottom + insight |

### D. Visualize (Bobot 25%)

| Kriteria | 0 | 1 | 2 | 3 |
|---|---|---|---|---|
| Bar chart | Tidak | Ada — error | Ada — rapi | Ada — rapi + label + warna |
| Pie chart | Tidak | Ada — error | Ada — rapi | Ada — label + persen |
| Grafik tambahan | Tidak | 1 | 2 | 3+ (scatter, boxplot, heatmap) |

### E. Export & Dokumentasi (Bobot 15%)

| Kriteria | 0 | 1 | 2 | 3 |
|---|---|---|---|---|
| Export CSV | Tidak | Ada kode | Berhasil | Berhasil + rapi |
| Dokumentasi | Tidak | File saja | File + screenshot | File + screenshot + refleksi |

---

## Kunci Jawaban (Verifikasi)

### Explore

| Item | Hasil (dataset awal) |
|---|---|
| Jumlah baris | 52 (termasuk 2 duplikat) |
| Jumlah kolom | 8 |
| Missing value | Matematika: 3 |
| Duplikat | 2 (Andi Pratama, Citra Dewi) |
| Outlier | Informatika: 101 |

### Setelah Clean

| Item | Hasil |
|---|---|
| Baris | 50 (setelah hapus 2 duplikat) |
| Missing | 0 |
| Rata-rata Matematika | ~79.8 |

### Analyze

| Item | Hasil |
|---|---|
| Rata-rata XI-1 | ~75.8 |
| Rata-rata XI-2 | ~87.6 |
| Siswa terbaik | Indah Lestari / Xena Olivia / Nabila Putri / Zaidan Malik (~93–94) |
| Jumlah remidi (<70) | ~5 siswa |
| Grade A (90+) | ~10 siswa |
| Grade E (<60) | ~1 siswa |

---

**MGMP Informatika SMAN 6 Cimahi**
