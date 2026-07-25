# MODUL AJAR INFORMATIKA – FASE F (KELAS XI)

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | F / XI |
| **Semester** | 2 (Genap) |
| **Pertemuan ke-** | 3 |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | SMA Negeri 6 Cimahi |
| **Materi Esensial** | Pengolahan Data Bervolume Besar |

---

## Tujuan Pembelajaran

| TP | IKTP |
|---|---|
| **BK, AD:** Membuat dashboard data yang informatif | 3.1 Menjelaskan konsep dashboard dan fungsinya |
| | 3.2 Merancang dashboard yang efektif (layout, KPI, grafik) |
| | 3.3 Membuat dashboard di Google Sheets |
| | 3.4 Membuat dashboard interaktif di Looker Studio |

---

## Langkah Pembelajaran

### Pembukaan (20 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 3 menit |
| 2. **Review**: "S1 kita belajar grafik. S2 Pert 2: data sudah bersih. Sekarang: kumpulkan semua grafik jadi satu — **Dashboard!**" | 5 menit |
| 3. **Apersepsi**: Tampilkan dashboard real (Google Analytics / Looker Studio). "Lihat — semua informasi penting dalam 1 layar. Tanpa dashboard, kita buka 10 file berbeda." | 7 menit |
| 4. **Trigger**: "Coba bayangkan kepala sekolah minta laporan kondisi sekolah — data absensi, nilai, keuangan, infrastruktur. Kamu kasih 4 file Excel atau 1 dashboard?" | 5 menit |

### Inti (170 menit)

#### Memahami (55 menit)

**1. Konsep Dashboard (15 menit)**

| Definisi | Dashboard = tampilan visual satu layar yang merangkum informasi penting, metrik, dan KPI (Key Performance Indicators) untuk monitoring dan pengambilan keputusan. |
|---|---|

**Karakteristik Dashboard yang Baik:**

| Karakteristik | Penjelasan |
|---|---|
| **Satu layar** | Semua informasi tanpa scroll (atau minimal scroll) |
| **Visual** | Grafik, bukan tabel angka |
| **Real-time / periodik** | Data selalu update |
| **Interaktif** | Filter, drill-down, klik |
| **Berfokus** | Hanya KPI penting, jangan overload |

**Jenis Dashboard:**

| Jenis | Tujuan | Contoh |
|---|---|---|
| **Operasional** | Monitoring harian | Absensi, penjualan harian |
| **Analitis** | Analisis tren | Perbandingan semester, prediksi |
| **Strategis** | Pengambilan keputusan | KPI sekolah, progress S1 |

**2. Komponen Dashboard (20 menit)**

| Komponen | Fungsi | Contoh |
|---|---|---|
| **KPI (Key Performance Indicators)** | Angka paling penting | Rata-rata nilai: 78.5 |
| **Grafik batang** | Perbandingan kategori | Rata-rata per kelas |
| **Grafik garis** | Tren waktu | Rata-rata nilai per bulan |
| **Grafik lingkaran** | Proporsi | % Lulus vs Remedial |
| **Tabel** | Data detail (opsional) | 10 siswa terbaik |
| **Filter** | Interaktif — pilih kelas, tanggal | Dropdown kelas |
| **Judul & Periode** | Konteks | "Laporan Nilai S1 2026/2027" |
| **Sumber data** | Kredibilitas | "Sumber: data.go.id" |

**Prinsip Tata Letak Dashboard:**

```
┌─────────────────────────────────────────────┐
│  JUDUL DASHBOARD                    Periode  │
├──────────┬──────────┬──────────┬────────────┤
│   KPI 1  │  KPI 2   │  KPI 3   │   KPI 4    │
│ Rata2 78 │ Remedial │ Tertinggi│ Terendah   │
│          │   20%    │    98    │    45      │
├──────────┴──────────┴──────────┴────────────┤
│      GRAFIK 1 (Column) — Perbandingan       │
├──────────┬──────────────────────────────────┤
│ GRAFIK 2 │     GRAFIK 3 (Pie / Scatter)     │
│ (Line)   │                                  │
├──────────┴──────────────────────────────────┤
│  FILTER: Kelas | Sumber: Data Nilai S1      │
└─────────────────────────────────────────────┘
```

**3. Alat Dashboard (10 menit)**

| Alat | Kelebihan | Kekurangan |
|---|---|---|
| **Google Sheets** | Gratis, familiar | Terbatas interaktivitas |
| **Looker Studio** | Gratis, interaktif, konek banyak sumber | Butuh belajar |
| **Tableau Public** | Sangat interaktif | Data publik |
| **Power BI** | Profesional | Berbayar (gratis versi desktop) |

**4. Studi Kasus: Dashboard Sekolah (10 menit)**
- Data: Nilai siswa S1 (40 siswa, 4 kelas)
- KPI: Rata-rata, median, % remedial, % pujian
- Grafik: column per kelas, pie remedial, scatter UTS vs UAS

#### Mengaplikasi — Praktik (85 menit)

**5. Demonstrasi Google Sheets Dashboard (15 menit)**
- Buat sheet baru → layout dengan merged cells
- Tambahkan KPI dengan formula
- Insert chart → column, pie, scatter
- Tambahkan filter (slicer)

**6. Aktivitas 1 — Dashboard di Google Sheets (35 menit) — Berpasangan**

Buat dashboard dari dataset nilai S1 (Pert 15/16):

| Komponen | Spesifikasi |
|---|---|
| Judul | "Dashboard Nilai Semester 1" |
| 4 KPI | Rata-rata, % remedial, nilai tertinggi, nilai terendah |
| Column chart | Rata-rata per kelas |
| Pie chart | Remedial vs lulus |
| Scatter chart | Korelasi UTS vs UAS |
| Filter | Dropdown kelas (atau slicer) |
| Sumber data | "Data Nilai S1 SMAN 6 Cimahi" |

**7. Aktivitas 2 — Dashboard di Looker Studio (25 menit) — Individu**

Langkah:
1. Buka `lookerstudio.google.com`
2. Klik "Blank Report"
3. Add data → Google Sheets → pilih dataset cleaning Pert 2
4. Add chart: Scorecard (KPI), Time series, Bar, Pie
5. Add filter control
6. Atur layout, warna, judul

**8. Aktivitas 3 — Peer Review Dashboard (10 menit)**
- Tukar link dashboard dengan pasangan lain
- Nilai 1–5 untuk: (1) kelengkapan, (2) tata letak, (3) visual, (4) interaktivitas
- Beri 1 saran perbaikan

#### Merefleksi (15 menit)

**9. Refleksi Jurnal (15 menit)**
- Perbedaan grafik biasa dengan dashboard?
- Fitur Looker Studio paling berguna?
- Skala pemahaman 1–10

### Penutup (35 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman: Konsep dashboard → Layout → Google Sheets → Looker Studio | 10 menit |
| 2. Kuis lisan: "Apa itu KPI? Bedanya dashboard operasional vs strategis?" | 10 menit |
| 3. Preview: "Pert 4: JSON/CSV & Python — baca tulis file data dengan Python!" | 5 menit |
| 4. Tugas rumah: Sempurnakan dashboard Looker Studio + screenshot | 10 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| KPI (4 metrik) | 0–1 | 2 | 3 | 4 + formula benar |
| Grafik (3 jenis) | 0–1 | 2 | 3 rapi | 3 + label + judul |
| Tata letak | Acak | Cukup rapi | Rapi | Rapi + konsisten |
| Filter interaktif | Tidak ada | Ada | Ada + berfungsi | Ada + multi-filter |
| Looker Studio | Tidak buat | 1 grafik | Dashboard lengkap | Dashboard + interaktif |

---

**MGMP Informatika SMAN 6 Cimahi**
