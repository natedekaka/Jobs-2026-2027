---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 14 — FASE F (S2)
## Proyek Akhir 🐍
### Pipeline Pengolahan Data dengan Python
#### SMA Negeri 6 Cimahi

---

## Review — Pert 1–5 S2

```
Big Data → Cleaning → Dashboard → JSON/CSV → Studi Kasus

Hari ini:
PRAKTEK! Pipeline lengkap!
```

**Bawa laptop? 🖥️**

---

## Tujuan Pembelajaran

1. ✅ Load & explore dataset CSV
2. ✅ Clean data (missing, duplikat, outlier)
3. ✅ Transform & analyze
4. ✅ Visualize & export

---

## Pipeline Hari Ini

```
DATA KOTOR
    ↓
LOAD → EXPLORE → CLEAN → TRANSFORM
                              ↓
ANALYZE → VISUALIZE → EXPORT
                    ↓
          DATA BERSIH + GRAFIK
```

---

## Dataset: nilai_siswa.csv

| Kolom | Contoh |
|---|---|
| Nama | Andi Pratama |
| Kelas | XI-1 / XI-2 |
| Matematika | 85 |
| B_Indonesia | 78 |
| B_Inggris | 92 |
| Informatika | 88 |
| IPA | 75 |
| IPS | 80 |

**Masalah:** missing, duplikat, outlier!

---

## Tools

| Opsi | Cara |
|---|---|
| **Google Colab** | colab.research.google.com |
| **VS Code** | Buka folder → New File `.py` |
| **Terminal** | `python script.py` |

---

## Tahap 1 — Load & Explore

```python
import pandas as pd
df = pd.read_csv('nilai_siswa.csv')
print(df.head())
print(df.info())
print(df.describe())
print(df.isnull().sum())
```

---

## Tahap 2 — Clean

```python
df = df.drop_duplicates()
df['Matematika'] = df['Matematika'].fillna(
    df['Matematika'].mean()
)
df.loc[df['Informatika'] > 100, 'Informatika'] = 100
df['Matematika'] = df['Matematika'].astype(int)
```

---

## Tahap 3 — Transform

```python
mapel = ['Matematika','B_Indonesia','B_Inggris',
         'Informatika','IPA','IPS']

df['Rata_rata'] = df[mapel].mean(axis=1)
df['Grade'] = df['Rata_rata'].apply(hitung_grade)
df['Status'] = df['Rata_rata'].apply(
    lambda x: 'LULUS' if x >= 70 else 'REMIDI'
)
```

---

## Tahap 4 — Analyze

```python
print(df.groupby('Kelas').mean())
print(df.sort_values('Rata_rata', ascending=False).head(5))
print(df['Grade'].value_counts())
```

**Temukan:** Kelas terbaik? Top 5 siswa?

---

## Tahap 5 — Visualize

```python
# 1. Bar chart
plt.bar(mapel, df[mapel].mean())

# 2. Pie chart
plt.pie(grade_counts, labels=..., autopct='%1.1f%%')

# 3. Scatter plot
plt.scatter(df['Matematika'], df['Informatika'])
```

---

## Tahap 6 — Export

```python
df.to_csv('nilai_siswa_bersih.csv', index=False)
df[mapel].describe().to_csv('statistik.csv')
```

---

## Aktivitas Mandiri

Selesai lebih awal? Coba:

1. Download dataset dari **data.go.id**
2. Pipeline data penduduk / cuaca
3. Heatmap korelasi
4. Histogram distribusi nilai

---

## Tugas Kumpul

| File | Wajib? |
|---|---|
| `nilai_siswa.py` / `.ipynb` | ✅ |
| `rata_mapel.png` | ✅ |
| `distribusi_grade.png` | ✅ |
| `korelasi.png` | ✅ |
| `nilai_siswa_bersih.csv` | ✅ |

---

## Refleksi

- Langkah tersulit?
- Insight dari data nilai?
- Data apa yang ingin kalian olah?

---

## Preview — Pert 15 (Pertemuan Terakhir 🏁)

### Review PAS Semester 2

> Bawa semua catatan S2!
> Review semua materi: Big Data → Platform Digital

---

# Selamat Coding! 🚀

### MGMP Informatika SMAN 6 Cimahi

> "Data is the new oil — learn to refine it!"
