# BAHAN AJAR – PERTEMUAN 3 (S2)
## Visualisasi Data & Dashboard

| TP | BK, AD — Pengolahan Data Bervolume Besar |
|---|---|

---

### A. KONSEP DASHBOARD

#### Definisi

> **Dashboard** adalah tampilan visual satu layar yang merangkum informasi penting, metrik, dan KPI untuk monitoring dan pengambilan keputusan.

#### Dashboard vs Grafik Biasa

| Grafik Biasa | Dashboard |
|---|---|
| 1 grafik saja | Banyak grafik + KPI + filter |
| Statis | Interaktif (filter, klik) |
| Tidak ada konteks | Judul, periode, sumber data |
| Untuk satu tujuan | Untuk monitoring menyeluruh |

#### Jenis Dashboard

| Jenis | Monitor | Analisis | Contoh Pengguna |
|---|---|---|---|
| **Operasional** | Harian/mingguan | Cepat | Guru lihat absensi hari ini |
| **Analitis** | Bulanan/semester | Mendalam | Wali kelas lihat tren nilai |
| **Strategis** | Tahunan | Keputusan besar | Kepsek lihat KPI sekolah |

---

### B. KOMPONEN DASHBOARD

#### 1. KPI (Key Performance Indicators)

Angka paling penting yang langsung menjawab "Bagaimana kondisi kita?"

| KPI | Rumus | Contoh |
|---|---|---|
| Rata-rata nilai | `=AVERAGE(range)` | 78.5 |
| Persentase lulus | `=COUNTIF(range,"≥75")/COUNT(range)*100` | 80% |
| Nilai tertinggi | `=MAX(range)` | 98 |
| Jumlah siswa | `=COUNT(range)` | 40 |
| Tren (naik/turun) | Bandingkan periode | Naik 5% dari PTS ke PAS |

#### 2. Grafik Utama

| Grafik | Letak | Ukuran |
|---|---|---|
| Column bar (perbandingan) | Tengah, kiri | Besar (lebar) |
| Line chart (tren) | Bawah | Sedang |
| Pie/Donut (proporsi) | Kanan atas | Sedang |
| Scatter (korelasi) | Kanan bawah | Sedang |
| Heatmap (kepadatan) | Alternatif | Bervariasi |

#### 3. Filter / Slicer

Filter interaktif memungkinkan pengguna memilih subset data.

| Filter | Contoh |
|---|---|
| Dropdown | Pilih kelas: X-A, X-B, X-C, X-D |
| Date range | Pilih rentang tanggal |
| Checkbox | Centang mata pelajaran |

#### 4. Judul & Metadata

```
Judul      : "Dashboard Nilai Semester 1 — Informatika Fase F"
Periode    : Juli – Desember 2026
Sumber     : Data Nilai SMAN 6 Cimahi
Update     : 25 Desember 2026
```

---

### C. PRINSIP TATA LETAK DASHBOARD

#### Layout F-Shape (paling umum)

```
╔══════════════════════════════════════════════╗
║  JUDUL DASHBOARD                     2026   ║
╠═══════╦═══════╦═══════╦══════════════════════╣
║ KPI 1 ║ KPI 2 ║ KPI 3 ║       GRAFIK 1      ║
║       ║       ║       ║   (Column chart)     ║
╠═══════╩═══════╩═══════╬══════════════════════╣
║      GRAFIK 2         ║     GRAFIK 3         ║
║   (Line chart)        ║    (Pie chart)       ║
╠═══════════════════════╩══════════════════════╣
║  FILTER | Sumber Data | Update Terakhir      ║
╚══════════════════════════════════════════════╝
```

#### Tips Tata Letak

| Tips | Jangan |
|---|---|
| KPI di baris paling atas | KPI di bawah / tengah |
| Grafik terpenting di kiri atas | Grafik penting di pojok |
| Konsisten warna & font | Warna pelangi |
| Gunakan whitespace | Penuh sesak |
| Maksimal 7 komponen | > 10 komponen |

---

### D. ALAT DASHBOARD

#### 1. Google Sheets Dashboard

**Langkah:**

| Langkah | Cara |
|---|---|
| 1. Siapkan data | Data bersih di sheet "Data" |
| 2. Buat sheet "Dashboard" | Sheet baru |
| 3. Layout | Merge cells untuk judul, KPI, grafik |
| 4. KPI | `=AVERAGE(Data!C2:C41)` |
| 5. Grafik | Insert → Chart → pilih jenis |
| 6. Filter | Data → Add a slicer → pilih kolom |
| 7. Selesai | Atur ukuran, warna, font |

#### 2. Google Looker Studio

> Alat dashboard interaktif gratis dari Google.

**Langkah:**

| Langkah | Cara |
|---|---|
| 1. Buka | `lookerstudio.google.com` |
| 2. Buat | Blank Report |
| 3. Konek data | Google Sheets → pilih spreadsheet |
| 4. Add chart | Chart → Scorecard (KPI), Bar, Pie, Line |
| 5. Atur dimensi & metrik | Drag & drop kolom |
| 6. Filter | Add a filter control → Dropdown |
| 7. Layout | Atur ukuran, posisi, warna tema |
| 8. Share | Share → view only / edit |

#### Perbandingan Alat

| Fitur | Google Sheets | Looker Studio | Tableau Public |
|---|---|---|---|
| Harga | Gratis | Gratis | Gratis (data publik) |
| Interaktif | Minimal | ✅ Ya | ✅ Sangat |
| Koneksi data | Sheets saja | Banyak | Banyak |
| Belajar | Mudah | Sedang | Sulit |
| Hasil | Sederhana | Profesional | Profesional |

---

### E. STUDI KASUS: DASHBOARD NILAI S1

Data: 40 siswa, 4 kelas (X-A s.d. X-D)

#### KPI

```
Jumlah Siswa   : 40
Rata-rata Nilai: 78.5
% Lulus (≥75)  : 80%
Nilai Tertinggi: 98
Nilai Terendah : 45
```

#### Grafik

| Grafik | Data | Insight |
|---|---|---|
| Column | Rata-rata per kelas | X-A = 85 (tertinggi), X-C = 72 (terendah) |
| Pie | % Remedial vs Lulus | 20% remedial |
| Scatter | UTS vs UAS | Korelasi positif: r = 0.78 |

#### Filter

| Filter | Fungsi |
|---|---|
| Kelas | Pilih 1 kelas → lihat detail per kelas |
| Status Lulus | Tampilkan hanya lulus / remedial |

---

### F. RANGKUMAN

| Konsep | Inti |
|---|---|
| **Dashboard** | Satu layar, visual, KPI, interaktif |
| **KPI** | Angka paling penting (rata-rata, %, max, min) |
| **Layout** | F-shape: KPI atas, grafik kiri–kanan |
| **Google Sheets** | Sederhana, cepat, gratis |
| **Looker Studio** | Profesional, interaktif, gratis |
| **Filter** | Interaktif — pilih kelas, tanggal, dll. |

---

**MGMP Informatika SMAN 6 Cimahi**
