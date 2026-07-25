---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 3 — FASE F (S2)
## Visualisasi Data & Dashboard
### Informatika – Fase F / Kelas XI
#### SMA Negeri 6 Cimahi

---

## Review — Pert 2

```
Data sudah BERSIH!
Sekarang: kumpulkan semua grafik
           jadi SATU LAYAR
               ⬇
           DASHBOARD! 📊
```

---

## Apersepsi

Kepala sekolah minta laporan kondisi sekolah:

> 4 file Excel vs 1 dashboard

**Mana yang lebih cepat dipahami?** 🤔

---

## Tujuan Pembelajaran

1. ✅ Konsep dashboard
2. ✅ Komponen dashboard
3. ✅ Dashboard di Google Sheets
4. ✅ Dashboard di Looker Studio

---

## Apa itu Dashboard?

> Tampilan **satu layar** yang merangkum informasi penting, metrik, dan KPI.

| Grafik Biasa | Dashboard |
|---|---|
| 1 grafik | Banyak grafik + KPI |
| Statis | Interaktif (filter) |
| Tanpa konteks | Judul, sumber, update |

---

## Jenis Dashboard

| Jenis | Monitoring | Contoh |
|---|---|---|
| **Operasional** | Harian | Absensi hari ini |
| **Analitis** | Bulanan | Tren nilai semester |
| **Strategis** | Tahunan | KPI sekolah |

---

## Komponen Dashboard

```
┌─────────┬─────────┬─────────┬─────────┐
│ KPI 1   │ KPI 2   │ KPI 3   │ KPI 4   │
│ Rata2   │ Remedial│ Tertingg│ Terendah│
├─────────┴─────────┴─────────┴─────────┤
│      GRAFIK 1 — Column (per kelas)    │
├─────────────────┬─────────────────────┤
│  GRAFIK 2       │   GRAFIK 3          │
│  Pie (proporsi) │   Scatter (korelasi)│
├─────────────────┴─────────────────────┤
│  FILTER: Kelas | Sumber Data          │
└───────────────────────────────────────┘
```

---

## KPI (Key Performance Indicators)

> Angka paling penting — langsung bisa dibaca

| KPI | Rumus Sheets |
|---|---|
| Rata-rata | `=AVERAGE(range)` |
| % Lulus | `=COUNTIF(range,"≥75")/COUNT(range)*100` |
| Tertinggi | `=MAX(range)` |
| Terendah | `=MIN(range)` |

---

## Alat Dashboard

| Alat | Harga | Interaktif |
|---|---|---|
| **Google Sheets** | Gratis | Minimal |
| **Looker Studio** | Gratis | ✅ Banget |
| **Tableau Public** | Gratis | ✅ Sangat |

---

## Google Sheets Dashboard

**Langkah:**
1. Sheet "Data" — data bersih
2. Sheet "Dashboard" — layout
3. Merge cells → judul, KPI
4. Formula untuk KPI
5. Insert → Chart
6. Data → Slicer (filter)

---

## Looker Studio Dashboard

**Langkah:**
1. Buka `lookerstudio.google.com`
2. Blank Report
3. Konek Google Sheets
4. Tambah Scorecard (KPI)
5. Tambah Bar, Pie, Line chart
6. Tambah Filter control
7. Atur tema & warna

---

## Aktivitas 1 — Sheets Dashboard

### 35 menit — Berpasangan

Buat dashboard nilai S1:

```
✅ Judul
✅ 4 KPI
✅ Column chart (per kelas)
✅ Pie chart (remedial)
✅ Scatter (UTS vs UAS)
✅ Filter kelas
```

---

## Aktivitas 2 — Looker Studio

### 25 menit — Individu

Buat dashboard di Looker Studio!

> Link dibagikan ke guru & teman

---

## Aktivitas 3 — Peer Review

### 10 menit

Tukar link → nilai dashboard teman!

```
1. Kelengkapan   : /5
2. Tata letak    : /5
3. Visual        : /5
4. Interaktif    : /5
```

---

## Refleksi

- Perbedaan grafik biasa vs dashboard?
- Fitur Looker Studio paling berguna?
- Skala 1–10?

---

## Preview — Pert 4

### JSON/CSV & Python

> Baca tulis file data dengan Python!

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Dashboard yang baik = data yang bersih + visual yang tepat + interaktif!"
