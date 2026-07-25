# ASESMEN – PERTEMUAN 4 (S2)
## JSON/CSV & Python

Informatika – Fase F / Kelas XI – SMA Negeri 6 Cimahi

---

## Rubrik Penilaian

### A. Struktur CSV & JSON (Bobot 15%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| CSV | Tidak benar | Format salah | Format benar | Benar + header |
| JSON | Tidak benar | Syntax error | Syntax benar | Benar + tipe data tepat |

### B. Baca CSV (Bobot 25%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Kode berjalan | Error | Berhasil 1 fungsi | 2–3 fungsi | 4–5 fungsi |
| Hasil benar | 0–1 | 2 | 3–4 | 5 |

### C. DictReader & Filter (Bobot 20%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Filter | Tidak jalan | 1 filter | 2 filter | 3 filter + benar |
| Output | Error | Ada output | Output benar | Output + rapi |

### D. JSON (Bobot 20%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Baca/tulis JSON | Tidak | Baca saja | Baca + tulis | Baca + tulis + modifikasi |
| Operasi data | Tidak | 1 operasi | 2 operasi | 3+ operasi benar |

### E. Konversi CSV↔JSON (Bobot 10%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Konversi | Tidak | 1 arah error | 1 arah benar | 2 arah benar |

### F. Refleksi & Tugas (Bobot 10%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Refleksi | Tidak diisi | 1 jawaban | 2 jawaban | 2 jawaban + mendalam |
| Tugas rumah | Tidak | Sebagian | Lengkap | Lengkap + Colab link |

---

## Kunci Jawaban

### Soal 1 — CSV & JSON

**CSV:**
```csv
Nama,Kelas,Nilai UTS,Nilai UAS
Adi,X-A,82,88
Budi,X-B,75,70
Citra,X-A,90,92
```

**JSON:**
```json
[
  {"nama": "Adi", "kelas": "X-A", "uts": 82, "uas": 88},
  {"nama": "Budi", "kelas": "X-B", "uts": 75, "uas": 70},
  {"nama": "Citra", "kelas": "X-A", "uts": 90, "uas": 92}
]
```

### Soal 2 — Baca CSV (contoh)

```python
import csv

with open('nilai.csv', 'r') as file:
    reader = csv.reader(file)
    next(reader)  # skip header
    total_uts = 0
    total_uas = 0
    count = 0
    max_uts = 0
    min_uas = 100
    siswa_min_uas = ''

    for row in reader:
        nama, kelas, uts, uas = row
        uts = int(uts)
        uas = int(uas)
        total_uts += uts
        total_uas += uas
        count += 1
        if uts > max_uts:
            max_uts = uts
        if uas < min_uas:
            min_uas = uas
            siswa_min_uas = nama

    print('Jumlah siswa:', count)
    print('Rata-rata UTS:', total_uts / count)
    print('Rata-rata UAS:', total_uas / count)
    print('UTS tertinggi:', max_uts)
    print('UAS terendah:', min_uas, '—', siswa_min_uas)
```

### Soal 3 — Filter DictReader

| Filter | Jumlah | Nama |
|---|---|---|
| UTS ≥ 85 | 1 | Citra |
| UAS < 75 | 1 | Budi |
| Rata-rata ≥ 80 | 2 | Adi, Citra |

### Soal 4 — JSON

```python
# Tambah siswa
data.append({"nama": "Dian", "kelas": "X-C", "uts": 65, "uas": 70})

# Simpan lagi
with open('siswa.json', 'w') as f:
    json.dump(data, f, indent=2)

# Rata-rata UTS
total = sum(s['uts'] for s in data)
print('Rata-rata UTS:', total / len(data))

# Filter UAS > 80
lulus = [s for s in data if s['uas'] > 80]
print('Siswa UAS > 80:', [s['nama'] for s in lulus])
```

### Soal 5 — Konversi (contoh)

```python
# CSV → JSON
def csv_to_json(csv_file, json_file):
    import csv, json
    data = []
    with open(csv_file, 'r') as f:
        reader = csv.DictReader(f)
        for row in reader:
            data.append(row)
    with open(json_file, 'w') as f:
        json.dump(data, f, indent=2)

# JSON → CSV
def json_to_csv(json_file, csv_file):
    import csv, json
    with open(json_file, 'r') as f:
        data = json.load(f)
    with open(csv_file, 'w', newline='') as f:
        fieldnames = data[0].keys()
        writer = csv.DictWriter(f, fieldnames=fieldnames)
        writer.writeheader()
        writer.writerows(data)
```

---

**MGMP Informatika SMAN 6 Cimahi**
