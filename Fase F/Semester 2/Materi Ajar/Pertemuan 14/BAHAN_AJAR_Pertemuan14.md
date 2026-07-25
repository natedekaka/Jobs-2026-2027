# BAHAN AJAR – PERTEMUAN 14 (S2)
## Proyek Akhir — Pipeline Pengolahan Data dengan Python

| TP | Pengolahan Data Bervolume Besar |
|---|---|

---

### A. PIPELINE PENGOLAHAN DATA

#### Diagram Alur

```
DATA KOTOR → LOAD → EXPLORE → CLEAN → TRANSFORM → ANALYZE → VISUALIZE → EXPORT
```

#### Library yang Digunakan

| Library | Fungsi | Install |
|---|---|---|
| **pandas** | Baca, manipulasi, analisis data | `pip install pandas` |
| **matplotlib** | Visualisasi grafik | `pip install matplotlib` |

---

### B. KODE REFERENSI LENGKAP

#### 1. Load & Explore

```python
import pandas as pd
import matplotlib.pyplot as plt

# Load CSV
df = pd.read_csv('nilai_siswa.csv')

# Lihat 5 baris pertama
print("=== 5 BARIS PERTAMA ===")
print(df.head())

# Informasi dataset
print("\n=== INFO DATASET ===")
print(df.info())

# Statistik deskriptif
print("\n=== DESKRIPSI STATISTIK ===")
print(df.describe())

# Cek missing value
print("\n=== MISSING VALUE ===")
print(df.isnull().sum())

# Cek duplikat
print(f"\nJUMLAH DUPLIKAT: {df.duplicated().sum()}")
```

#### 2. Clean

```python
# Hapus duplikat
df = df.drop_duplicates()

# Isi missing value dengan mean
df['Matematika'] = df['Matematika'].fillna(df['Matematika'].mean())

# Perbaiki outlier
df.loc[df['Informatika'] > 100, 'Informatika'] = 100

# Konversi ke integer
df['Matematika'] = df['Matematika'].astype(int)

# Verifikasi
print(df.isnull().sum())
print(df.describe())
```

#### 3. Transform

```python
# Daftar mapel
mapel = ['Matematika','B_Indonesia','B_Inggris','Informatika','IPA','IPS']

# Rata-rata
df['Rata_rata'] = df[mapel].mean(axis=1)

# Total
df['Total'] = df[mapel].sum(axis=1)

# Grade
def grade(rata):
    if rata >= 90: return 'A'
    elif rata >= 80: return 'B'
    elif rata >= 70: return 'C'
    elif rata >= 60: return 'D'
    else: return 'E'

df['Grade'] = df['Rata_rata'].apply(grade)

# Status
def status(rata):
    return 'LULUS' if rata >= 70 else 'REMIDI'

df['Status'] = df['Rata_rata'].apply(status)

print(df[['Nama','Rata_rata','Grade','Status']].head(10))
```

#### 4. Analyze

```python
# Rata-rata per kelas
print("=== RATA-RATA PER KELAS ===")
print(df.groupby('Kelas')[mapel + ['Rata_rata']].mean().round(1))

# Top 5
print("\n=== TOP 5 SISWA ===")
print(df.sort_values('Rata_rata', ascending=False)[['Nama','Kelas','Rata_rata','Grade']].head(5))

# Bottom 5
print("\n=== BOTTOM 5 ===")
print(df.sort_values('Rata_rata')[['Nama','Kelas','Rata_rata','Grade']].head(5))

# Distribusi grade
print(f"\n=== DISTRIBUSI GRADE ===")
print(df['Grade'].value_counts().sort_index())

# Jumlah remidi
print(f"\nJUMLAH REMIDI: {df[df['Status'] == 'REMIDI'].shape[0]}")
```

#### 5. Visualize

```python
# 1. Bar chart — rata-rata per mapel
plt.figure(figsize=(10, 5))
rata_mapel = df[mapel].mean()
warna = ['#FF6B6B','#4ECDC4','#45B7D1','#96CEB4','#FFEAA7','#DDA0DD']
plt.bar(mapel, rata_mapel, color=warna)
plt.title('Rata-rata Nilai per Mapel', fontsize=14, fontweight='bold')
plt.ylabel('Nilai', fontsize=11)
plt.ylim(0, 100)
for i, v in enumerate(round(rata_mapel, 1)):
    plt.text(i, v + 1, str(v), ha='center', fontsize=10)
plt.tight_layout()
plt.savefig('rata_mapel.png', dpi=150)
plt.show()

# 2. Pie — distribusi grade
plt.figure(figsize=(7, 7))
grade_counts = df['Grade'].value_counts()
warna_grade = {'A': '#FFD700', 'B': '#98FB98', 'C': '#87CEEB', 'D': '#FFA07A', 'E': '#FF6B6B'}
colors = [warna_grade[g] for g in grade_counts.index]
plt.pie(grade_counts, labels=[f"{g} ({c})" for g, c in zip(grade_counts.index, grade_counts.values)],
        colors=colors, autopct='%1.1f%%', startangle=90, textprops={'fontsize': 11})
plt.title('Distribusi Grade', fontsize=14, fontweight='bold')
plt.savefig('distribusi_grade.png', dpi=150)
plt.show()

# 3. Scatter — Matematika vs Informatika
plt.figure(figsize=(8, 6))
colors = ['green' if s == 'LULUS' else 'red' for s in df['Status']]
plt.scatter(df['Matematika'], df['Informatika'], c=colors, alpha=0.6, s=60)
plt.xlabel('Matematika', fontsize=11)
plt.ylabel('Informatika', fontsize=11)
plt.title('Korelasi Matematika vs Informatika', fontsize=14, fontweight='bold')
plt.grid(True, alpha=0.3)
plt.savefig('korelasi.png', dpi=150)
plt.show()

# 4. Boxplot — distribusi nilai per mapel
plt.figure(figsize=(10, 6))
df[mapel].boxplot()
plt.title('Distribusi Nilai per Mapel', fontsize=14, fontweight='bold')
plt.ylabel('Nilai', fontsize=11)
plt.grid(True, alpha=0.3)
plt.savefig('boxplot_nilai.png', dpi=150)
plt.show()
```

#### 6. Export

```python
# Data bersih
df.to_csv('nilai_siswa_bersih.csv', index=False)

# Statistik
df[mapel].describe().to_csv('statistik_nilai.csv')

# Rata-rata per kelas
df.groupby('Kelas')[mapel + ['Rata_rata']].mean().round(1).to_csv('rata_per_kelas.csv')

# 10 besar
df.sort_values('Rata_rata', ascending=False).head(10)[['Nama','Kelas','Rata_rata','Grade']].to_csv('top_10.csv', index=False)

print("Semua file berhasil diexport!")
```

---

### C. DATASET — nilai_siswa.csv

Download file ini, simpan di folder yang sama dengan script Python.

```csv
Nama,Kelas,Matematika,B_Indonesia,B_Inggris,Informatika,IPA,IPS
Andi Pratama,XI-1,85,78,92,88,75,80
Budi Santoso,XI-1,72,85,80,90,78,82
Citra Dewi,XI-2,90,88,95,92,85,88
Dedi Kusuma,XI-1,,80,75,85,70,72
Eka Fitriani,XI-2,78,92,88,95,80,90
Fajar Hermawan,XI-1,88,75,82,90,78,76
Gita Permata,XI-2,92,85,90,96,88,92
Hadi Nugroho,XI-1,65,70,72,68,60,65
Indah Lestari,XI-2,95,90,96,98,92,94
Joko Susilo,XI-1,70,65,68,72,62,70
Kartika Sari,XI-1,82,88,75,90,80,78
Lina Marlina,XI-2,88,85,90,92,86,84
Mega Putri,XI-1,,78,70,80,72,75
Nanda Pratama,XI-2,80,82,88,85,78,82
Oscar Wijaya,XI-1,75,72,80,78,70,74
Putri Ayu,XI-2,90,92,94,96,88,90
Qori Aini,XI-1,68,72,65,70,62,68
Rizky Ramadhan,XI-2,95,88,92,98,90,88
Sari Dewanti,XI-1,78,85,82,80,75,78
Teguh Prasetyo,XI-2,72,70,68,75,65,70
Umi Kalsum,XI-1,85,80,88,90,82,80
Vino Bastian,XI-2,60,65,62,58,55,60
Wulan Sari,XI-1,92,90,88,94,86,90
Xavier Putra,XI-2,88,82,90,85,80,85
Yuni Rahma,XI-1,76,80,78,82,74,76
Zaidan Malik,XI-2,84,86,85,88,80,82
Ahmad Fauzi,XI-1,70,75,72,68,65,70
Bunga Citra,XI-2,94,90,92,96,88,92
Cahyo Nugroho,XI-1,68,72,70,75,65,68
Dian Sastro,XI-2,86,88,90,92,84,86
Eko Prasetyo,XI-1,82,78,80,85,76,80
Fitriani Dewi,XI-2,90,92,88,94,86,90
Gilang Putra,XI-1,72,68,70,75,65,70
Hana Safira,XI-2,96,92,94,98,90,94
Indra Lesmana,XI-1,78,82,80,85,72,78
Jasmine Azahra,XI-2,88,90,92,95,86,88
Kevin Sanjaya,XI-1,65,70,68,72,60,65
Larasati Putri,XI-2,92,88,90,94,86,90
Maulana Hasan,XI-1,80,75,78,82,72,76
Nabila Putri,XI-2,94,96,92,98,90,92
Oki Setiawan,XI-1,72,68,70,65,62,68
Puspa Indah,XI-2,86,90,88,92,82,86
Qomarul Huda,XI-1,78,82,80,85,76,78
Ratna Kusuma,XI-2,90,88,92,95,86,90
Sandy Pratama,XI-1,68,72,65,70,62,68
Tania Putri,XI-2,92,90,94,96,88,92
Ujang Komarudin,XI-1,82,78,80,85,78,76
Vera Anggraini,XI-2,88,92,90,94,84,88
Wahyu Hidayat,XI-1,70,72,68,75,65,68
Xena Olivia,XI-2,95,90,92,98,88,92
Yoga Pratama,XI-1,75,80,78,82,72,74
Zahra Aulia,XI-2,90,88,92,94,86,90
```

> **Catatan:** Dataset ini sengaja mengandung missing value, duplikat (Andi Pratama & Citra Dewi muncul 2×), dan outlier (Informatika 101).

---

### D. TANTANGAN LANJUTAN (Jika Selesai Lebih Awal)

| Tantangan | Deskripsi |
|---|---|
| 1 | Download dataset dari data.go.id (misal: "Data Penduduk") — coba pipeline yang sama |
| 2 | Tambahkan histogram untuk distribusi nilai per mapel |
| 3 | Analisis korelasi antara 2 mapel dengan `df.corr()` |
| 4 | Ekspor data per kelas ke file terpisah: `nilai_XI-1.csv`, `nilai_XI-2.csv` |
| 5 | Tambahkan visualisasi heatmap korelasi |

```python
# Contoh heatmap
import seaborn as sns  # pip install seaborn
plt.figure(figsize=(8, 6))
sns.heatmap(df[mapel].corr(), annot=True, cmap='coolwarm')
plt.title('Heatmap Korelasi Antar Mapel')
plt.savefig('heatmap_korelasi.png', dpi=150)
plt.show()
```

---

### E. CHEAT SHEET

| Fungsi | Kegunaan |
|---|---|
| `pd.read_csv(file)` | Baca CSV |
| `df.head(n)` | Lihat n baris pertama |
| `df.info()` | Info kolom & tipe data |
| `df.describe()` | Statistik deskriptif |
| `df.isnull().sum()` | Jumlah missing per kolom |
| `df.duplicated().sum()` | Jumlah duplikat |
| `df.drop_duplicates()` | Hapus duplikat |
| `df.fillna(x)` | Isi missing dengan x |
| `df['kolom'].mean()` | Rata-rata kolom |
| `df.groupby('kolom').mean()` | Rata-rata per grup |
| `df.sort_values('kolom')` | Urutkan |
| `plt.bar()`, `plt.pie()`, `plt.scatter()` | Grafik |
| `df.to_csv('file.csv')` | Ekspor CSV |

---

**MGMP Informatika SMAN 6 Cimahi**
