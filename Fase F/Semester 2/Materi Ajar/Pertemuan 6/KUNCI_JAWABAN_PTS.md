# KUNCI JAWABAN & RUBRIK PENILAIAN
## PENILAIAN TENGAH SEMESTER (PTS) GENAP — INFORMATIKA FASE F / KELAS XI
## SMA Negeri 6 Cimahi — TP 2026/2027

---

## BAGIAN A — PILIHAN GANDA (20 Soal × 2 Poin = 40 Poin)

| No | Jawaban | No | Jawaban | No | Jawaban |
|---|---|---|---|---|---|
| 1 | **B** Velocity | 8 | **B** | 15 | **B** |
| 2 | **D** | 9 | **B** | 16 | **B** |
| 3 | **C** | 10 | **C** | 17 | **B** |
| 4 | **B** | 11 | **C** | 18 | **B** |
| 5 | **C** | 12 | **B** | 19 | **B** |
| 6 | **C** | 13 | **B** | 20 | **B** |
| 7 | **B** | 14 | **D** | | |

---

## BAGIAN B — ESAI (4 Soal × 15 Poin = 60 Poin)

### Soal 21 — Data Cleaning (15 poin)

**a. 3 masalah kualitas data (3 poin):**
| No | Masalah | Contoh |
|---|---|---|
| 1 | **Duplikat** | "Budi Santoso" muncul 2× |
| 2 | **Missing Value** | Nilai Citra Dewi kosong |
| 3 | **Outlier** | Nilai -10 (minus) dan 120 (>100) |
| 4 | **Inkonsisten format** | "budi santoso" vs "Budi Santoso" (case) |

(3 masalah dari 4 di atas — @1 poin)

**b. Solusi cleaning (6 poin):**
| Masalah | Solusi | Skor |
|---|---|---|
| Duplikat | Hapus 1 baris duplikat → Data → Remove duplicates | 2 |
| Missing | Isi dengan rata-rata nilai yang ada (85+78+...)/n atau hapus baris | 2 |
| Outlier -10 | Validasi: tidak mungkin nilai negatif → koreksi atau hapus | 1 |
| Outlier 120 | Nilai max 100 → koreksi menjadi 100 atau hapus | 1 |
| Format nama | `=PROPER()` → "Budi Santoso", "Citra Dewi", dll. | (bonus) |

**c. Data setelah cleaning (contoh, 6 poin):**
```csv
Nama,Kelas,Nilai
Budi Santoso,X-A,85
Citra Dewi,X-B,80
Adi Pratama,X-C,78
Dian Kurniawan,X-A,85
Eka Putri,X-B,78
```
- Duplikat Budi dihapus (1 baris) ✅
- Missing Citra diisi rata-rata (misal 80) ✅
- Outlier -10 dihapus (Adi) atau dikoreksi ✅
- Outlier 120 dikoreksi jadi 100 atau 85 ✅
- Format nama konsisten PROPER ✅

### Soal 22 — Dashboard (15 poin)

**a. 4 KPI (4 poin):**
| KPI | Rumus |
|---|---|
| Total penjualan (hari) | `=COUNT(range)` |
| Total pendapatan | `=SUMPRODUCT(jumlah, harga)` |
| Rata-rata penjualan/hari | `=AVERAGE(jumlah)` |
| Menu terlaris | `=MODE(range_menu)` atau MAX(COUNTIF) |
| Rata-rata harga jual | `=AVERAGE(harga)` |
| Pendapatan tertinggi per hari | `=MAX(SUMPRODUCT)` |

(4 KPI relevan — @1 poin)

**b. 2 grafik + tujuan (6 poin):**

| Grafik | Tujuan | Skor |
|---|---|---|
| **Line chart** | Tren penjualan selama 30 hari — lihat hari ramai/sepi | 3 |
| **Pie chart** | Proporsi penjualan per menu — menu mana paling laris | 3 |
| Alternatif: Column chart (perbandingan per menu), Bar chart | | |

**c. Layout dashboard (5 poin):**
```
┌──────────────────────────────────────────────────┐
│         DASHBOARD PENJUALAN KANTIN — Maret 2027    │
├──────────┬──────────┬──────────┬──────────────────┤
│ KPI 1    │ KPI 2    │ KPI 3    │   GRAFIK 1       │
│ Total    │ Pendapatan│ Rata-rata│   Line Chart     │
│ 30 hari  │ Rp 5 jt  │ 40 porsi │   (Tren harian)  │
├──────────┴──────────┴──────────┴──────────────────┤
│          GRAFIK 2 (Pie Chart — proporsi menu)      │
├──────────────────────────────────────────────────┤
│  FILTER: Tanggal | Menu | Sumber: Data Kantin     │
└──────────────────────────────────────────────────┘
```

### Soal 23 — Python CSV/JSON (15 poin)

```python
import csv
import json

# a. Baca CSV dan cetak (3 poin)
with open('data_siswa.csv', 'r') as f:
    reader = csv.DictReader(f)
    data = list(reader)
    for row in data:
        print(row)

# b. Rata-rata nilai (4 poin)
nilai_list = [int(row['Nilai']) for row in data]
rata2 = sum(nilai_list) / len(nilai_list)
print(f'Rata-rata: {rata2}')

# c. Simpan ke JSON (4 poin)
output = {
    'data': data,
    'rata_rata': rata2
}
with open('hasil.json', 'w') as f:
    json.dump(output, f, indent=2)

# d. Filter nilai ≥ 75 (4 poin)
lulus = [row for row in data if int(row['Nilai']) >= 75]
print('Siswa lulus:', [row['Nama'] for row in lulus])
```

### Soal 24 — Studi Kasus Pipeline (15 poin)

**a. 5 langkah pipeline (5 poin):**

| Langkah | Kegiatan | Skor |
|---|---|---|
| 1. **Cari** | Download data cuaca BMKG dari data.bmkg.go.id | 1 |
| 2. **Cuci** | Bersihkan missing values, outlier sensor, format tanggal | 1 |
| 3. **Olah** | Python: hitung rata-rata suhu per bulan, pola curah hujan | 1 |
| 4. **Visual** | Dashboard Looker Studio: grafik tren cuaca 10 tahun | 1 |
| 5. **Lapor** | Presentasi: musim tanam optimal berdasarkan data | 1 |

**b. 3 potensi masalah cuaca + solusi (6 poin):**

| Masalah | Contoh | Solusi | Skor |
|---|---|---|---|
| Missing values | Sensor hujan mati 3 hari | Isi dengan rata-rata 7 hari sebelumnya | 2 |
| Outlier sensor | Suhu 500°C | Hapus baris atau isi dengan data stasiun terdekat | 2 |
| Format tanggal | "1/1/2020", "2020-01-01", "01-Jan-20" | Standarisasi ke format ISO: 2020-01-01 | 2 |

**c. 2 grafik + insight (4 poin):**

| Grafik | Insight | Skor |
|---|---|---|
| **Line chart** — curah hujan per bulan (10 tahun) | Lihat pola musim hujan/kemarau → tentukan awal musim tanam | 2 |
| **Scatter plot** — suhu vs curah hujan | Korelasi: suhu tinggi + hujan rendah = kemarau → tidak cocok tanam padi | 2 |

---

## Rubrik Penilaian Esai

| Skor | Kriteria |
|---|---|
| 15 | Jawaban lengkap, tepat, detail, contoh konkret |
| 12–14 | Jawaban tepat, hampir lengkap, sedikit kurang detail |
| 9–11 | Jawaban benar, kurang detail |
| 6–8 | Jawaban setengah benar |
| 3–5 | Jawaban kurang tepat |
| 1–2 | Ada usaha |
| 0 | Tidak menjawab |

---

**MGMP Informatika SMAN 6 Cimahi**
