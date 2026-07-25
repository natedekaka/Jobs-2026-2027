# ASESMEN – PERTEMUAN 3 (S2)
## Visualisasi Data & Dashboard

Informatika – Fase F / Kelas XI – SMA Negeri 6 Cimahi

---

## Rubrik Penilaian

### A. Konsep Dashboard (Bobot 10%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Perbedaan grafik vs dashboard | Tidak tepat | Kurang tepat | Tepat | Tepat + detail |
| Jenis dashboard | 1 jenis | 2 jenis | 3 jenis | 3 jenis + contoh |

### B. Rancangan Dashboard (Bobot 15%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Layout gambaran | Tidak ada | Ada, acak | Ada, rapi | Ada, rapi + KPI, grafik, filter |
| KPI yang dipilih | 0–1 | 2 | 3 | 4 relevan + formula |

### C. Praktik Google Sheets Dashboard (Bobot 35%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| 4 KPI | 0–1 | 2 | 3 | 4 + formula benar |
| 3 grafik | 0–1 | 2 | 3 | 3 + label + judul |
| Filter | Tidak ada | Ada | Ada berfungsi | Ada + rapi |
| Layout | Acak | Cukup rapi | Rapi | Rapi + konsisten |

### D. Praktik Looker Studio (Bobot 25%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Koneksi data | Tidak | Ada | Ada + benar | Ada + transformasi |
| Scorecard KPI | 0–1 | 2 | 3 | 4 |
| Chart | 0–1 | 2 | 3 | 3+ |
| Filter | Tidak | Ada | Ada berfungsi | Ada + multi-filter |
| Tema & layout | Acak | Cukup | Rapi | Profesional |

### E. Peer Review & Refleksi (Bobot 15%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Peer review | Tidak | Skor saja | Skor + saran | Skor + saran detail |
| Refleksi | Tidak diisi | 1 jawaban | 2 jawaban | 2 jawaban + mendalam |

---

## Kunci Jawaban

### Soal 1 — Grafik vs Dashboard

| Aspek | Grafik Biasa | Dashboard |
|---|---|---|
| Jumlah grafik | 1 grafik | Banyak grafik + KPI |
| Filter | Tidak interaktif | Ada filter/slicer |
| Tujuan | Satu analisis | Monitoring menyeluruh |

### Soal 2 — Jenis Dashboard

| Jenis | Contoh |
|---|---|
| Operasional | Absensi harian, penjualan hari ini |
| Analitis | Perbandingan nilai per semester, tren bulanan |
| Strategis | KPI sekolah, progress tahunan |

### Soal 4 — Contoh KPI

| KPI | Rumus | Contoh Nilai |
|---|---|---|
| Rata-rata nilai | `=AVERAGE(Data!E2:E41)` | 78.5 |
| % Lulus | `=COUNTIF(Data!E2:E41,"≥75")/COUNT(Data!E2:E41)*100` | 80% |
| Nilai tertinggi | `=MAX(Data!E2:E41)` | 98 |
| Nilai terendah | `=MIN(Data!E2:E41)` | 45 |
| Jumlah siswa | `=COUNTA(Data!A2:A41)` | 40 |

### Soal 5 — Dashboard Checklist (contoh penilaian)

| Komponen | Keterangan |
|---|---|
| Judul | "Dashboard Nilai Semester 1" |
| 4 KPI | Rata-rata, % remedial, max, min |
| Column chart | Rata-rata per kelas (label sumbu X = kelas) |
| Pie chart | Remedial 20%, Lulus 80% (label persen) |
| Scatter chart | UTS vs UAS (trendline positif) |
| Filter | Slicer kelas dropdown |

### Soal 7 — Peer Review (contoh)

| Aspek | Skor 5 | Alasan |
|---|---|---|
| Kelengkapan | 5 | Ada KPI + 3 grafik + filter |
| Tata letak | 4 | Rapi, KPI di atas, grafik di bawah |
| Visual | 4 | Warna konsisten, font terbaca |
| Interaktivitas | 3 | Filter kelas berfungsi, tapi belum multi-filter |

---

**MGMP Informatika SMAN 6 Cimahi**
