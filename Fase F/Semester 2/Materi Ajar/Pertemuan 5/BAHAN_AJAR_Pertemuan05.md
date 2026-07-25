# BAHAN AJAR – PERTEMUAN 5 (S2)
## Studi Kasus Pengolahan Data

| TP | BK, AD, AP — Pengolahan Data Bervolume Besar |
|---|---|

---

### A. PIPELINE PENGOLAHAN DATA

```
CARI → CUCI → OLAH → VISUAL → LAPOR
  │       │       │        │       │
  │       │       │        │       └── Presentasi insight
  │       │       │        └────────── Dashboard / Grafik
  │       │       └─────────────────── Python (statistik, filter)
  │       └─────────────────────────── Data cleaning
  └─────────────────────────────────── Sumber data legal
```

---

### B. LANGKAH 1: CARI DATASET

#### Sumber Dataset

| Sumber | URL | Tema |
|---|---|---|
| Satu Data Indonesia | `data.go.id` | Pendidikan, penduduk, ekonomi, kesehatan |
| BMKG | `data.bmkg.go.id` | Cuaca, gempa, iklim |
| BPS | `bps.go.id` | Statistik nasional |
| Data Jakarta | `data.jakarta.go.id` | Data provinsi DKI |
| Kaggle | `kaggle.com` | Semua tema (global) |

#### Kriteria Dataset yang Baik

| Kriteria | Penjelasan |
|---|---|
| **Legal** | Lisensi terbuka (Open Data / CC) |
| **Relevan** | Sesuai minat / topik |
| **Cukup besar** | ≥ 50 baris |
| **Cukup kolom** | ≥ 5 kolom (ada kategorikal + numerik) |
| **Machine-readable** | CSV atau JSON |

#### Contoh Dataset yang Direkomendasikan

| Dataset | Sumber | Baris | Kolom |
|---|---|---|---|
| Data Sekolah per Provinsi | data.go.id / Kemendikbud | 200.000+ | 15 |
| Jumlah Penduduk per Provinsi | data.go.id / BPS | 34+ | 10 |
| Realisasi APBN | data.go.id / Kemenkeu | 10.000+ | 20 |
| Data Iklim Kota | data.bmkg.go.id | 1.000+ | 10 |
| World Bank Education Data | data.worldbank.org | 5.000+ | 20 |

---

### C. LANGKAH 2: CUCI DATA

#### Checklist Cleaning

| Masalah | Tools | Tindakan |
|---|---|---|
| Missing values | Python / Sheets | Isi rata-rata / hapus baris |
| Duplikat | Python / Sheets | `drop_duplicates()` |
| Inkonsisten format | Python / Sheets | `str.lower()`, `str.strip()` |
| Outlier | Python | Filter `nilai > threshold` |
| Tipe data salah | Python | `int()`, `float()`, `datetime` |

#### Dokumentasi Cleaning

Buat tabel dokumentasi setiap perubahan:

| Kolom | Masalah | Jumlah | Tindakan |
|---|---|---|---|
| Nama Provinsi | "DKI JAKARTA", "Jakarta" | 5 | `str.title()` → "DKI Jakarta" |
| Jumlah Penduduk | -500 (minus) | 1 | Hapus baris |
| Kode Provinsi | Kosong | 3 | Isi manual |

---

### D. LANGKAH 3: OLAH DENGAN PYTHON

#### Template Analisis

```python
import csv
import json

# 1. Baca CSV
data = []
with open('dataset_bersih.csv', 'r') as f:
    reader = csv.DictReader(f)
    for row in reader:
        data.append(row)

print(f'Jumlah data: {len(data)}')

# 2. Statistik (asumsi kolom numerik)
nilai_list = [int(row['nilai']) for row in data]
print(f'Rata-rata: {sum(nilai_list) / len(nilai_list):.2f}')
print(f'Tertinggi: {max(nilai_list)}')
print(f'Terendah: {min(nilai_list)}')

# 3. Filter
lulus = [row for row in data if int(row['nilai']) >= 75]
print(f'Jumlah lulus: {len(lulus)} ({len(lulus)/len(data)*100:.1f}%)')

# 4. Group by (kategorikal)
from collections import Counter
kategori = Counter([row['kelas'] for row in data])
print('Per kategori:', dict(kategori))

# 5. Simpan JSON
with open('hasil_analisis.json', 'w') as f:
    json.dump({
        'total': len(data),
        'rata_rata': sum(nilai_list) / len(nilai_list),
        'tertinggi': max(nilai_list),
        'terendah': min(nilai_list),
        'per_kategori': dict(kategori)
    }, f, indent=2)
```

#### Insight Wajib

| Insight | Contoh |
|---|---|
| **Statistik deskriptif** | "Rata-rata nilai adalah 78.5 dengan rentang 45–98" |
| **Perbandingan kategori** | "Provinsi dengan sekolah terbanyak adalah Jawa Barat (45.000)" |
| **Nilai ekstrem** | "3 provinsi memiliki angka partisipasi sekolah di bawah 70%" |

---

### E. LANGKAH 4: VISUALISASI / DASHBOARD

#### Komponen Dashboard

```
┌──────────────────────────────────────────────┐
│  Judul: Analisis Dataset [nama]               │
├────────┬───────┬───────┬──────────────────────┤
│ KPI 1  │ KPI 2 │ KPI 3 │   GRAFIK 1           │
│ Total  │ Rata2 │ Max   │   Bar / Column       │
├────────┴───────┴───────┴──────────────────────┤
│  GRAFIK 2 (Line / Pie / Scatter)              │
├──────────────────────────────────────────────┤
│  Filter: [Dropdown] | Sumber: data.go.id       │
└──────────────────────────────────────────────┘
```

#### Pilihan Alat

| Alat | Kelebihan | Untuk |
|---|---|---|
| Google Sheets | Cepat, familiar | Dashboard sederhana |
| Looker Studio | Interaktif, gratis | Dashboard profesional |
| Python Matplotlib | Kustom penuh | Grafik di notebook |

---

### F. LANGKAH 5: LAPORAN & PRESENTASI

#### Struktur Laporan

| Bagian | Isi |
|---|---|
| **1. Pendahuluan** | Dataset apa? Dari mana? Mengapa dipilih? |
| **2. Metode** | Tools & langkah (clean → Python → dashboard) |
| **3. Hasil Cleaning** | Masalah ditemukan, solusi, tabel perbandingan |
| **4. Analisis** | Statistik, insight, grafik |
| **5. Dashboard** | Screenshot + link |
| **6. Kesimpulan** | Temuan utama, saran, keterbatasan |

#### Format Presentasi (3 menit)

| Waktu | Bagian |
|---|---|
| 30 detik | Dataset & sumber |
| 30 detik | Masalah cleaning & solusi |
| 60 detik | Insight dari Python |
| 30 detik | Demo dashboard |
| 30 detik | Kesimpulan |

---

### G. RANGKUMAN

| Langkah | Output | Tools |
|---|---|---|
| 1. Cari dataset | Dataset mentah (CSV/JSON) | data.go.id, Kaggle |
| 2. Cuci data | Data bersih | Python / Sheets |
| 3. Olah Python | Statistik + insight | Colab |
| 4. Visualisasi | Dashboard | Looker / Sheets |
| 5. Laporan | Presentasi | Slides / Canva |

---

**MGMP Informatika SMAN 6 Cimahi**
