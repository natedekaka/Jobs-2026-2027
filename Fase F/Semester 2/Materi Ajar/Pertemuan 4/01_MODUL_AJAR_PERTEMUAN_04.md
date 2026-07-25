# MODUL AJAR INFORMATIKA – FASE F (KELAS XI)

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | F / XI |
| **Semester** | 2 (Genap) |
| **Pertemuan ke-** | 4 |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | SMA Negeri 6 Cimahi |
| **Materi Esensial** | Pengolahan Data Bervolume Besar |

---

## Tujuan Pembelajaran

| TP | IKTP |
|---|---|
| **AD, AP:** Membaca dan menulis file CSV/JSON menggunakan Python | 4.1 Menjelaskan struktur file CSV dan JSON |
| | 4.2 Membaca file CSV dengan Python (csv module) |
| | 4.3 Membaca dan menulis file JSON dengan Python |
| | 4.4 Mengkonversi data antara CSV dan JSON |

---

## Langkah Pembelajaran

### Pembukaan (20 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 3 menit |
| 2. **Review**: "Pert 3: dashboard dari Google Sheets. Tapi kalau datanya besar — 1 juta baris — Sheets lemot. Kita butuh **Python!**" | 5 menit |
| 3. **Apersepsi**: "Buka file CSV di notepad — hanya teks dipisah koma. JSON — teks dengan kurung kurawal. Dua format data paling populer untuk programmer!" | 7 menit |
| 4. **Trigger**: "Tiktok, Instagram, Gojek — data mereka dalam format JSON. Kalian bisa baca dan olah data JSON dengan Python!" | 5 menit |

### Inti (170 menit)

#### Memahami (50 menit)

**1. Format Data — CSV (15 menit)**

> **CSV** = Comma-Separated Values — data tabel dipisah koma.

```
Nama,Kelas,Nilai
Budi Santoso,X-A,85
Citra Dewi,X-B,90
Adi Pratama,X-A,78
```

| Kelebihan | Kekurangan |
|---|---|
| Sederhana, bisa dibuka Excel | Tidak support nested data |
| Ringan (ukuran kecil) | Tidak ada tipe data (semua string) |
| Standar universal | Koma dalam data perlu di-quote |

**2. Format Data — JSON (15 menit)**

> **JSON** = JavaScript Object Notation — struktur key-value seperti dictionary Python.

```json
[
  {
    "nama": "Budi Santoso",
    "kelas": "X-A",
    "nilai": 85
  },
  {
    "nama": "Citra Dewi",
    "kelas": "X-B",
    "nilai": 90
  }
]
```

| Kelebihan | Kekurangan |
|---|---|
| Support nested (objek dalam objek) | Ukuran lebih besar dari CSV |
| Tipe data: string, number, boolean, null | Butuh parser |
| Standar API modern | Tidak bisa langsung dibuka Excel |

**3. Python untuk File I/O (20 menit)**

| Operasi | CSV | JSON |
|---|---|---|
| Import module | `import csv` | `import json` |
| Baca file | `csv.reader()` atau `csv.DictReader()` | `json.load()` |
| Tulis file | `csv.writer()` atau `csv.DictWriter()` | `json.dump()` |
| Baca string | `csv.reader(string.splitlines())` | `json.loads()` |
| Ubah ke string | — | `json.dumps()` |

#### Mengaplikasi — Praktik (90 menit)

**4. Demonstrasi Google Colab (10 menit)**
- Buka `colab.research.google.com`
- Buat notebook baru
- Upload file CSV/JSON sampel
- Demo: baca CSV → cetak isi

**5. Aktivitas 1 — Baca CSV (25 menit) — Individu**

```python
import csv

with open('nilai_siswa.csv', 'r') as file:
    reader = csv.reader(file)
    header = next(reader)  # baca header
    print('Header:', header)
    for row in reader:
        print(f'{row[0]} — {row[1]}: {row[2]}')
```

Tugas:
1. Buat file CSV manual (10 baris data nilai)
2. Baca dengan `csv.reader()` — cetak semua baris
3. Hitung rata-rata nilai dari data CSV
4. Cari siswa dengan nilai tertinggi

**6. Aktivitas 2 — Baca CSV dengan DictReader (20 menit) — Individu**

```python
import csv

with open('nilai_siswa.csv', 'r') as file:
    reader = csv.DictReader(file)
    for row in reader:
        print(f'{row["Nama"]} — {row["Kelas"]}: {row["Nilai"]}')
```

Tugas: Modifikasi kode untuk:
- Cari nilai rata-rata
- Filter siswa dengan nilai ≥ 80
- Simpan hasil filter ke file baru

**7. Aktivitas 3 — JSON (25 menit) — Berpasangan**

```python
import json

# Baca JSON
with open('data_siswa.json', 'r') as file:
    data = json.load(file)

print(json.dumps(data, indent=2))

# Hitung rata-rata
total = sum(siswa['nilai'] for siswa in data)
rata2 = total / len(data)
print(f'Rata-rata: {rata2}')
```

Tugas:
1. Buat data dictionary → konversi ke JSON
2. Simpan ke file JSON
3. Baca kembali dari file JSON
4. Tambah 1 siswa baru → simpan
5. Konversi CSV → JSON

**8. Aktivitas 4 — Konversi CSV ↔ JSON (10 menit) — Kelompok**

Buat fungsi Python untuk konversi:
- CSV → JSON: baca CSV, tulis JSON
- JSON → CSV: baca JSON, tulis CSV

#### Merefleksi (15 menit)

**9. Refleksi Jurnal (15 menit)**
- Perbedaan struktur CSV vs JSON
- Kapan pakai CSV? Kapan pakai JSON?
- Skala pemahaman 1–10

### Penutup (35 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman: CSV (tabel) → JSON (nested) → Python baca/tulis | 10 menit |
| 2. Kuis lisan: "Cara baca CSV dengan Python? Bedanya json.load vs json.loads?" | 10 menit |
| 3. Preview: "Pert 5: Studi Kasus Pengolahan Data — Gabung semua skill: Big Data → Cleaning → Dashboard → Python!" | 5 menit |
| 4. Tugas rumah: Ambil 1 dataset dari data.go.id (CSV), baca dengan Python, hitung statistik, simpan sebagai JSON | 10 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Baca CSV | Error | Berhasil baca | Baca + cetak rapi | Baca + olah (rata-rata, filter) |
| Baca JSON | Error | Berhasil baca | Baca + cetak rapi | Baca + olah + modifikasi |
| Konversi CSV↔JSON | Tidak | 1 arah | 2 arah | 2 arah + rapi + handle error |
| Kode Python | Tidak jalan | Jalan sebagian | Jalan benar | Jalan + efisien + komentar |

---

**MGMP Informatika SMAN 6 Cimahi**
