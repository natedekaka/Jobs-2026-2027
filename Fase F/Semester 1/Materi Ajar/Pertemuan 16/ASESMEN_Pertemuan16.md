# ASESMEN – PERTEMUAN 16
## Visualisasi Data

Informatika – Fase F / Kelas XI – SMA Negeri 6 Cimahi

---

## Rubrik Penilaian

### A. Pemahaman Jenis Grafik (Bobot 15%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Mencocokkan chart type | 0–2 benar | 3–4 benar | 5–6 benar | 6 benar + penjelasan |
| Identifikasi kesalahan | 0–1 tepat | 2 tepat | 3–4 tepat | 5 tepat + perbaikan |

### B. Praktik Google Sheets (Bobot 30%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Column chart | Tidak sesuai | Sesuai tapi tanpa label | Sesuai + label | Sesuai + label + insight |
| Pie chart | Tidak sesuai | Sesuai tapi tanpa % | Sesuai + % | Sesuai + % + warna baik |
| Scatter chart | Tidak sesuai | Hanya titik | Titik + trendline | Trendline + insight |

### C. Infografis (Bobot 25%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Konten | < 2 grafik | 2 grafik | 2+ grafik | 3+ grafik + insight |
| Desain | Tidak rapi | Cukup rapi | Rapi, warna baik | Rapi + warna konsisten |
| Prinsip | Melanggar ≥ 3 | Melanggar 2 | Melanggar 1 | Semua prinsip dipatuhi |

### D. Kritik Visualisasi (Bobot 15%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Analisis grafik | 0 tepat | 1 tepat | 2 tepat | 3 tepat |
| Saran perbaikan | Tidak ada | 1 saran | 2 saran | 3 saran tepat |

### E. Tugas Rumah (Bobot 15%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Grafik ditemukan | Tidak | Ada, tanpa analisis | Ada + analisis | Ada + analisis + perbaikan |
| Refleksi | Tidak diisi | 1 jawaban | 2 jawaban | 3 jawaban |

---

## Kunci Jawaban

### Soal 1 — Jenis Grafik

| Grafik | Kegunaan |
|---|---|
| Column chart | 2 — Perbandingan antar kategori |
| Line chart | 3 — Tren dari waktu ke waktu |
| Pie chart | 1 — Proporsi/bagian dari total |
| Scatter plot | 4 — Korelasi dua variabel numerik |
| Histogram | 5 — Distribusi frekuensi |
| Heatmap | 6 — Kepadatan/matriks |

### Soal 2 — Identifikasi Masalah

| Masalah | Alasan | Perbaikan |
|---|---|---|
| Sumbu Y mulai 50 | Membesar-besarkan perbedaan | Mulai dari 0 |
| Pie 3D dengan 8 irisan | 3D distort persepsi, terlalu banyak irisan | 2D donut, maks 5 irisan |
| Scatter 500 titik tanpa transparansi | Over-plotting — tidak terlihat distribusi | Tambah alpha atau hexbin |
| Pelangi 6+ warna | Membingungkan, tidak konsisten | Palet 2–5 warna saja |
| Dua sumbu Y tanpa label | Tidak jelas data apa | Label sumbu atau pisahkan |

### Soal 3–5 — Praktik (contoh)

**Column Chart**
- Judul: "Rata-rata Nilai UAS per Kelas"
- Sumbu X: Kelas (X-A, X-B, X-C, X-D)
- Sumbu Y: Nilai (0–100)
- Insight: X-A tertinggi, X-C perlu perhatian

**Pie Chart**
- Remedial: 20%, Lulus: 80%
- Insight: 8 dari 40 siswa remedial

**Scatter Chart**
- Korelasi positif: semakin tinggi UTS, semakin tinggi UAS
- Trendline: menunjukkan arah positif

### Soal 7 — Kritik (contoh jawaban tergantung grafik guru)

Misal grafik A: batang dengan sumbu Y dipotong
- Masalah: truncated Y-axis — perbedaan terlihat 2× lebih besar
- Perbaikan: set sumbu Y dari 0

---

**MGMP Informatika SMAN 6 Cimahi**
