# LEMBAR KERJA PESERTA DIDIK (LKPD)
## Pertemuan 4 (S2) – JSON/CSV & Python

| TP | AD, AP — Pengolahan Data Bervolume Besar |
|---|---|
| Nama | ____________________ |
| Kelas | ____________________ |

---

### A. STRUKTUR CSV & JSON

**Soal 1:** Ubah data berikut ke format CSV dan JSON!

| Nama | Kelas | Nilai UTS | Nilai UAS |
|---|---|---|---|
| Adi | X-A | 82 | 88 |
| Budi | X-B | 75 | 70 |
| Citra | X-A | 90 | 92 |

**CSV:**
```
________________________________
________________________________
________________________________
________________________________
```

**JSON:**
```json

```

---

### B. BACA CSV DENGAN PYTHON

**Soal 2:** Buka Google Colab. Buat file `nilai.csv`. Tulis kode Python untuk membaca CSV dan jawab pertanyaan!

```python
import csv

# Tulis kode di sini
with open('nilai.csv', 'r') as file:
    # ...
```

| Pertanyaan | Kode | Hasil |
|---|---|---|
| Berapa jumlah siswa? | | |
| Rata-rata nilai UTS? | | |
| Rata-rata nilai UAS? | | |
| Nilai UTS tertinggi? | | |
| Siapa siswa dengan UAS terendah? | | |

---

### C. BACA CSV DENGAN DICTREADER

**Soal 3:** Gunakan DictReader untuk filter data!

```python
import csv

with open('nilai.csv', 'r') as file:
    reader = csv.DictReader(file)
    for row in reader:
        if int(row['Nilai UTS']) >= 85:
            print(f"{row['Nama']} — UTS: {row['Nilai UTS']}")
```

Tugas:
| Filter | Jumlah Siswa | Nama-nama |
|---|---|---|
| Nilai UTS ≥ 85 | | |
| Nilai UAS < 75 | | |
| Rata-rata ≥ 80 | | |

---

### D. JSON DENGAN PYTHON

**Soal 4:** Jalankan kode berikut di Colab!

```python
import json

data = [
    {"nama": "Adi", "kelas": "X-A", "uts": 82, "uas": 88},
    {"nama": "Budi", "kelas": "X-B", "uts": 75, "uas": 70},
    {"nama": "Citra", "kelas": "X-A", "uts": 90, "uas": 92}
]

# Simpan ke file JSON
with open('siswa.json', 'w') as f:
    json.dump(data, f, indent=2)

# Baca kembali
with open('siswa.json', 'r') as f:
    data_baca = json.load(f)
    print(json.dumps(data_baca, indent=2))
```

Tugas:
| Operasi | Kode | Hasil |
|---|---|---|
| Tambah 1 siswa baru ke list | | |
| Simpan lagi ke file | | |
| Hitung rata-rata UTS | | |
| Filter siswa dengan UAS > 80 | | |

---

### E. KONVERSI CSV ↔ JSON

**Soal 5:** Tulis fungsi konversi!

| Arah | Kode |
|---|---|
| CSV → JSON | ``` # tulis kode ``` |
| JSON → CSV | ``` # tulis kode ``` |

---

### F. TUGAS RUMAH

| Tugas | Status |
|---|---|
| Ambil 1 dataset CSV dari data.go.id | ✅ / ❌ |
| Baca dengan Python | ✅ / ❌ |
| Hitung statistik (rata-rata, max, min) | ✅ / ❌ |
| Simpan sebagai JSON | ✅ / ❌ |
| Kumpulkan link Colab | ✅ / ❌ |

**Link Google Colab:** ____________________

---

### G. REFLEKSI

| Pertanyaan | Jawaban |
|---|---|
| Perbedaan struktur CSV vs JSON? | |
| Kapan pakai CSV? Kapan JSON? | |
| Skala pemahaman (1–10) | / 10 |

---

**MGMP Informatika SMAN 6 Cimahi**
