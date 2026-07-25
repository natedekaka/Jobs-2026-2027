# BAHAN AJAR – PERTEMUAN 4 (S2)
## JSON/CSV & Python

| TP | AD, AP — Pengolahan Data Bervolume Besar |
|---|---|

---

### A. FORMAT DATA — CSV

#### Struktur CSV

> **CSV** = Comma-Separated Values. Data tabel di mana setiap baris adalah record dan kolom dipisahkan koma.

```
Nama,Kelas,Nilai,Status
Budi Santoso,X-A,85,Lulus
Citra Dewi,X-B,90,Lulus
Adi Pratama,X-A,78,Lulus
Dian Kurniawan,X-C,45,Remedial
```

| Baris | Nama | Kelas | Nilai | Status |
|---|---|---|---|---|
| 1 (header) | Nama | Kelas | Nilai | Status |
| 2 | Budi Santoso | X-A | 85 | Lulus |
| 3 | Citra Dewi | X-B | 90 | Lulus |
| 4 | Adi Pratama | X-A | 78 | Lulus |
| 5 | Dian Kurniawan | X-C | 45 | Remedial |

#### Aturan CSV

| Aturan | Contoh | Penjelasan |
|---|---|---|
| Delimiter koma | `Budi, X-A, 85` | Pemisah default |
| Quote jika ada koma | `"Budi, S. T.", X-A, 85` | Koma dalam data harus di-quote |
| Header opsional | Baris pertama | Jika ada, jadi nama kolom |
| Newline = baris baru | Enter | Setiap baris = 1 record |

#### Kelebihan & Kekurangan CSV

| ✅ Kelebihan | ❌ Kekurangan |
|---|---|
| Format paling sederhana | Tidak ada tipe data (semua string) |
| Bisa dibuka Excel / Google Sheets | Tidak support nested data |
| Ukuran file kecil | Tidak ada standar encoding |
| Standar universal — semua tool support | Koma dalam data butuh penanganan khusus |

---

### B. FORMAT DATA — JSON

#### Struktur JSON

> **JSON** = JavaScript Object Notation. Format berbasis teks untuk pertukaran data — mirip dictionary Python.

**Object (dict):**
```json
{
  "nama": "Budi Santoso",
  "kelas": "X-A",
  "nilai": 85,
  "lulus": true,
  "alamat": null
}
```

**Array (list) of objects:**
```json
[
  {"nama": "Budi", "kelas": "X-A", "nilai": 85},
  {"nama": "Citra", "kelas": "X-B", "nilai": 90}
]
```

**Nested (objek bersarang):**
```json
{
  "sekolah": "SMAN 6 Cimahi",
  "tahun": 2026,
  "siswa": [
    {"nama": "Budi", "nilai": {"uts": 85, "uas": 88}},
    {"nama": "Citra", "nilai": {"uts": 90, "uas": 92}}
  ]
}
```

#### Tipe Data JSON

| JSON | Python | Contoh |
|---|---|---|
| `string` | `str` | `"Budi"` |
| `number` | `int` / `float` | `85`, `3.14` |
| `boolean` | `bool` | `true` / `false` |
| `null` | `None` | `null` |
| `array` | `list` | `[1, 2, 3]` |
| `object` | `dict` | `{"key": "value"}` |

#### Kelebihan & Kekurangan JSON

| ✅ Kelebihan | ❌ Kekurangan |
|---|---|
| Support nested data | Ukuran lebih besar dari CSV |
| Tipe data eksplisit | Tidak bisa langsung dibuka Excel |
| Standar API web modern | Butuh parser untuk dibaca |
| Mudah dibaca manusia | Syntax lebih ketat dari CSV |

---

### C. PYTHON — MEMBACA & MENULIS FILE

#### Membuka File

```python
# Mode membuka file
'r'  # read (baca) — default
'w'  # write (tulis) — overwrite
'a'  # append (tambah)
'r+' # read + write

# Best practice: gunakan 'with' — auto close
with open('file.csv', 'r') as file:
    content = file.read()
```

#### 1. Membaca CSV dengan `csv.reader`

```python
import csv

with open('nilai_siswa.csv', 'r') as file:
    reader = csv.reader(file)
    header = next(reader)  # ambil baris pertama (header)
    print('Header:', header)

    for row in reader:
        nama, kelas, nilai = row
        print(f'{nama} ({kelas}): {nilai}')
```

#### 2. Membaca CSV dengan `csv.DictReader`

```python
import csv

with open('nilai_siswa.csv', 'r') as file:
    reader = csv.DictReader(file)
    for row in reader:
        print(f"{row['Nama']} ({row['Kelas']}): {row['Nilai']}")
```

#### 3. Menulis CSV dengan `csv.writer`

```python
import csv

data = [
    ['Nama', 'Kelas', 'Nilai'],
    ['Budi', 'X-A', 85],
    ['Citra', 'X-B', 90],
]

with open('output.csv', 'w', newline='') as file:
    writer = csv.writer(file)
    writer.writerows(data)
```

#### 4. Menulis CSV dengan `csv.DictWriter`

```python
import csv

data = [
    {'Nama': 'Budi', 'Kelas': 'X-A', 'Nilai': 85},
    {'Nama': 'Citra', 'Kelas': 'X-B', 'Nilai': 90},
]

with open('output.csv', 'w', newline='') as file:
    fieldnames = ['Nama', 'Kelas', 'Nilai']
    writer = csv.DictWriter(file, fieldnames=fieldnames)
    writer.writeheader()
    writer.writerows(data)
```

#### 5. Membaca JSON

```python
import json

with open('data_siswa.json', 'r') as file:
    data = json.load(file)

print(type(data))  # list atau dict
print(json.dumps(data, indent=2))  # cetak rapi
```

#### 6. Menulis JSON

```python
import json

data = [
    {'nama': 'Budi', 'kelas': 'X-A', 'nilai': 85},
    {'nama': 'Citra', 'kelas': 'X-B', 'nilai': 90},
]

with open('output.json', 'w') as file:
    json.dump(data, file, indent=2)
```

---

### D. STUDI KASUS: KONVERSI CSV ↔ JSON

#### CSV → JSON

```python
import csv
import json

csv_file = 'nilai_siswa.csv'
json_file = 'nilai_siswa.json'

data = []
with open(csv_file, 'r') as f:
    reader = csv.DictReader(f)
    for row in reader:
        row['Nilai'] = int(row['Nilai'])  # konversi string ke int
        data.append(row)

with open(json_file, 'w') as f:
    json.dump(data, f, indent=2)

print(f'Konversi selesai: {csv_file} → {json_file}')
```

#### JSON → CSV

```python
import csv
import json

json_file = 'nilai_siswa.json'
csv_file = 'nilai_siswa_dari_json.csv'

with open(json_file, 'r') as f:
    data = json.load(f)

with open(csv_file, 'w', newline='') as f:
    fieldnames = data[0].keys()
    writer = csv.DictWriter(f, fieldnames=fieldnames)
    writer.writeheader()
    writer.writerows(data)

print(f'Konversi selesai: {json_file} → {csv_file}')
```

---

### E. RANGKUMAN

| Operasi | CSV | JSON |
|---|---|---|
| Struktur | Tabel (baris × kolom) | Key-value / nested |
| Module | `csv` | `json` |
| Baca file | `csv.reader()`, `csv.DictReader()` | `json.load()` |
| Tulis file | `csv.writer()`, `csv.DictWriter()` | `json.dump()` |
| Python → String | — | `json.dumps()` |
| String → Python | — | `json.loads()` |
| Kelebihan | Sederhana, ringan, Excel | Nested, tipe data, API |

---

**MGMP Informatika SMAN 6 Cimahi**
