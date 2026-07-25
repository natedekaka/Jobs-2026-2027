---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 4 — FASE F (S2)
## JSON/CSV & Python
### Informatika – Fase F / Kelas XI
#### SMA Negeri 6 Cimahi

---

## Review — Pert 3

```
Dashboard keren!
Tapi kalau data 1 juta baris → Sheets lemot
```

> Solusi: **Python!** 🐍

---

## Apersepsi

> File CSV dibuka di notepad = teks dipisah koma
> File JSON = teks dengan kurung kurawal

**Dua format data paling populer di dunia!**

---

## Tujuan Pembelajaran

1. ✅ Struktur CSV & JSON
2. ✅ Baca CSV dengan Python
3. ✅ Baca/tulis JSON
4. ✅ Konversi CSV ↔ JSON

---

## Format CSV

> Comma-Separated Values

```
Nama,Kelas,Nilai
Budi,X-A,85
Citra,X-B,90
```

| ✅ Sederhana | ❌ Tidak ada tipe data |
|---|---|
| ✅ Bisa Excel | ❌ Tidak support nested |

---

## Format JSON

> JavaScript Object Notation

```json
{
  "nama": "Budi",
  "kelas": "X-A",
  "nilai": 85,
  "lulus": true
}
```

| ✅ Nested | ❌ Lebih besar |
|---|---|
| ✅ Tipe data | ❌ Butuh parser |

---

## Perbandingan

```
CSV = TABEL sederhana
JSON = STRUKTUR (nested, tipe data)

CSV:  Data Analyst
JSON: Programmer / API
```

---

## Python Module

| Operasi | CSV | JSON |
|---|---|---|
| Import | `import csv` | `import json` |
| Baca file | `csv.reader()` | `json.load()` |
| Tulis file | `csv.writer()` | `json.dump()` |
| Ke string | — | `json.dumps()` |

---

## Baca CSV — reader

```python
import csv

with open('nilai.csv', 'r') as file:
    reader = csv.reader(file)
    next(reader)  # skip header
    for row in reader:
        print(row[0], row[2])
```

---

## Baca CSV — DictReader

```python
import csv

with open('nilai.csv', 'r') as file:
    reader = csv.DictReader(file)
    for row in reader:
        print(row['Nama'], row['Nilai'])
```

> ✅ Lebih rapi — panggil pakai nama kolom!

---

## Baca/Tulis JSON

```python
import json

# Tulis
with open('data.json', 'w') as f:
    json.dump(data, f, indent=2)

# Baca
with open('data.json', 'r') as f:
    data = json.load(f)
```

---

## Aktivitas 1 — Baca CSV

### 25 menit — Individu

```
1. Buat file CSV (10 baris)
2. Baca dengan csv.reader()
3. Hitung rata-rata
4. Cari nilai tertinggi
```

> Di Google Colab!

---

## Aktivitas 2 — DictReader Filter

### 20 menit — Individu

```
Filter:
✅ Nilai ≥ 80
✅ Nilai < 75
✅ Rata-rata ≥ 85

Simpan hasil ke file baru!
```

---

## Aktivitas 3 — JSON

### 25 menit — Berpasangan

```
1. Buat dict/list → simpan JSON
2. Baca JSON → cetak rapi
3. Tambah data → simpan lagi
4. Hitung rata-rata
```

---

## Aktivitas 4 — Konversi

### 10 menit — Kelompok

Buat fungsi:

```
csv_to_json('nilai.csv', 'nilai.json')
json_to_csv('nilai.json', 'nilai.csv')
```

---

## Refleksi

- Perbedaan CSV vs JSON?
- Kapan pakai CSV? Kapan JSON?
- Skala 1–10?

---

## Tugas Rumah

> Ambil dataset data.go.id (CSV) → baca Python
> Hitung statistik → simpan JSON
> Kumpulkan link Colab!

---

## Preview — Pert 5

### Studi Kasus Pengolahan Data

> Gabung semua skill: Big Data → Cleaning → Dashboard → Python!

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "CSV untuk tabel, JSON untuk struktur — Python untuk keduanya!"
