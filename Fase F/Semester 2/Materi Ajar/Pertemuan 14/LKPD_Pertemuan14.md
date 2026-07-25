# LEMBAR KERJA PESERTA DIDIK (LKPD)
## Pertemuan 14 (S2) – Proyek Akhir Python Pipeline

| TP | Pengolahan Data Bervolume Besar |
|---|---|
| Nama | ____________________ |
| Kelas | ____________________ |

**Langkah Awal:**
1. Download `nilai_siswa.csv` dari guru
2. Buka Google Colab / VS Code / terminal Python
3. Simpan file CSV di folder kerja

---

### TAHAP 1 — LOAD & EXPLORE

```python
import pandas as pd
df = pd.read_csv('nilai_siswa.csv')
```

| Soal | Jawaban |
|---|---|
| Jumlah baris | |
| Jumlah kolom | |
| Nama kolom | |
| Jumlah missing value | |
| Jumlah duplikat | |
| Rata-rata Matematika | |

---

### TAHAP 2 — CLEAN

```python
df = df.drop_duplicates()
df['Matematika'] = df['Matematika'].fillna(df['Matematika'].mean())
df['Matematika'] = df['Matematika'].astype(int)
df.loc[df['Informatika'] > 100, 'Informatika'] = 100
```

| Masalah | Strategi |
|---|---|
| Duplikat | |
| Missing Matematika (3 siswa) | |
| Informatika = 101 | |

---

### TAHAP 3 — TRANSFORM

| Soal | Jawaban |
|---|---|
| Rata-rata kelas tertinggi (XI-1 / XI-2)? | |
| Siswa dengan rata-rata tertinggi? | |
| Siswa dengan rata-rata terendah? | |
| Jumlah remidi (< 70)? | |

Tambahkan script transform-mu di sini:

```python
# Tulis kode transform-mu

```

---

### TAHAP 4 — VISUALIZE

Tempel screenshot grafik:

| Grafik 1: Rata-rata per Mapel | Grafik 2: Distribusi Grade |
|---|---|
| (screenshot) | (screenshot) |

| Grafik 3: Korelasi | Grafik 4: Boxplot |
|---|---|
| (screenshot) | (screenshot) |

---

### TAHAP 5 — REFLEKSI

| Pertanyaan | Jawaban |
|---|---|
| Langkah tersulit? | |
| Insight dari data? | |
| Skala pemahaman (1–10) | / 10 |
| 1 hal baru yang dipelajari | |

---

### TUGAS KUMPUL

| File | ✅ |
|---|---|
| `nilai_siswa.py` (script Python) atau `.ipynb` (Colab) | |
| `rata_mapel.png` | |
| `distribusi_grade.png` | |
| `korelasi.png` (opsional) | |
| `nilai_siswa_bersih.csv` | |

**Kumpul via Google Drive / flashdisk ke guru!**

---

**MGMP Informatika SMAN 6 Cimahi**
