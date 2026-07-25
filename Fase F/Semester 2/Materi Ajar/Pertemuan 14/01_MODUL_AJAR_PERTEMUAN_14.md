# MODUL AJAR INFORMATIKA – FASE F (KELAS XI)

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | F / XI |
| **Semester** | 2 (Genap) |
| **Pertemuan ke-** | 14 |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | SMA Negeri 6 Cimahi |
| **Materi Esensial** | Pengolahan Data Bervolume Besar |

---

## Tujuan Pembelajaran

| TP | IKTP |
|---|---|
| **LD:** Menerapkan pipeline pengolahan data menggunakan Python | 14.1 Memuat & mengeksplorasi dataset CSV |
| | 14.2 Membersihkan data (missing value, duplikat) |
| | 14.3 Mentransformasi & menganalisis data |
| | 14.4 Memvisualisasikan hasil analisis |

---

## Persiapan

| Perlengkapan | Keterangan |
|---|---|
| Laptop/Chromebook | 1 per siswa (bawa sendiri) |
| Python + pandas + matplotlib | Install sebelum kelas — panduan dikirim H-1 |
| Dataset `nilai_siswa.csv` | Disiapkan guru — bagikan via Google Drive / flashdisk |
| Google Colab (alternatif) | Tidak perlu install — akses colab.research.google.com |
| Jaringan internet | Untuk Google Colab & dokumentasi |

**Panduan Install (kirim H-1 via grup):**

```
# Windows — Command Prompt (run as admin)
pip install pandas matplotlib

# Atau via Google Colab (tanpa install)
# Buka colab.research.google.com → New Notebook
```

---

## Langkah Pembelajaran

### Pembukaan (25 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran + pastikan semua bawa laptop | 5 menit |
| 2. **Review**: "Pert 1–5 S2 kita belajar teori pengolahan data. Pert 4 sudah coba Python dasar. Sekarang: pipeline lengkap — dari data kotor → laporan + grafik!" | 5 menit |
| 3. **Apersepsi**: "Kalian punya data nilai semester lalu — 100 siswa, 10 mapel. Ada nilai kosong, duplikat, outlier. Bagaimana cara membersihkan & menganalisisnya dengan Python?" | 10 menit |
| 4. **Trigger**: "Data science adalah profesi #1 di LinkedIn. Langkah pertama: pipeline pengolahan data. Kalian akan lakukan hari ini!" | 5 menit |

### Inti (160 menit)

#### Memahami (30 menit)

**1. Pipeline Pengolahan Data (10 menit)**

```
DATA KOTOR (CSV/JSON)
    ↓
1. LOAD — baca file (pandas.read_csv)
    ↓
2. EXPLORE — head(), info(), describe()
    ↓
3. CLEAN — dropna(), fillna(), drop_duplicates()
    ↓
4. TRANSFORM — kolom baru, groupby, mapping
    ↓
5. ANALYZE — mean, sum, sort_values
    ↓
6. VISUALIZE — matplotlib (bar, pie, scatter)
    ↓
7. EXPORT — to_csv(), to_excel()
    ↓
DATA BERSIH + LAPORAN + GRAFIK
```

**2. Dataset Hari Ini (10 menit)**

Dataset `nilai_siswa.csv` — nilai 50 siswa, 6 mapel:

| Kolom | Tipe | Contoh |
|---|---|---|
| Nama | string | "Andi Pratama" |
| Kelas | string | "XI-1" |
| Matematika | int/NaN | 85 |
| B_Indonesia | int/NaN | 78 |
| B_Inggris | int/NaN | 92 |
| Informatika | int/NaN | 88 |
| IPA | int/NaN | 75 |
| IPS | int/NaN | 80 |

**Masalah dalam dataset:**
- 3 siswa nilai Matematika kosong (NaN)
- 2 baris duplikat
- 1 siswa nilai Informatika 101 (outlier)
- Tipe data perlu dikonversi

**3. Tools (10 menit)**

Demonstrasi:
- Buka Google Colab / VS Code / terminal Python
- Import pandas & matplotlib
- Download dataset

#### Mengaplikasi (105 menit)

**Tahap 1 — Load & Explore (15 menit)**

```python
import pandas as pd
import matplotlib.pyplot as plt

# Load
df = pd.read_csv('nilai_siswa.csv')

# Explore
print(df.head(10))
print(df.info())
print(df.describe())
print(df.isnull().sum())
print(df.duplicated().sum())
```

**Tugas:** Cari jumlah baris, kolom, missing value, duplikat!

**Tahap 2 — Clean (20 menit)**

```python
# Hapus duplikat
df = df.drop_duplicates()
print(f"Setelah hapus duplikat: {len(df)} baris")

# Isi missing value dengan rata-rata kelas
df['Matematika'] = df['Matematika'].fillna(df['Matematika'].mean())

# Atau — hapus baris yang missing
# df = df.dropna()

# Perbaiki outlier (nilai > 100)
df.loc[df['Informatika'] > 100, 'Informatika'] = 100

# Konversi tipe
df['Matematika'] = df['Matematika'].astype(int)

print(df.isnull().sum())
print(df.describe())
```

**Tugas:** Tentukan strategi pembersihan untuk tiap masalah!

**Tahap 3 — Transform (20 menit)**

```python
# Kolom rata-rata
df['Rata_rata'] = df[['Matematika','B_Indonesia','B_Inggris','Informatika','IPA','IPS']].mean(axis=1)

# Kolom total
df['Total'] = df[['Matematika','B_Indonesia','B_Inggris','Informatika','IPA','IPS']].sum(axis=1)

# Fungsi grade
def hitung_grade(rata):
    if rata >= 90: return 'A'
    elif rata >= 80: return 'B'
    elif rata >= 70: return 'C'
    elif rata >= 60: return 'D'
    else: return 'E'

df['Grade'] = df['Rata_rata'].apply(hitung_grade)

print(df[['Nama','Rata_rata','Grade']].head(10))
```

**Tugas:** Tambahkan kolom Grade!

**Tahap 4 — Analyze (20 menit)**

```python
# Statistik per kelas
print(df.groupby('Kelas')[['Matematika','B_Indonesia','B_Inggris','Informatika','IPA','IPS', 'Rata_rata']].mean())

# 5 siswa terbaik
print(df.sort_values('Rata_rata', ascending=False).head(5))

# Distribusi grade
print(df['Grade'].value_counts())

# Rata-rata per mapel
mapel = ['Matematika','B_Indonesia','B_Inggris','Informatika','IPA','IPS']
print(df[mapel].mean())
```

**Tugas:** Tentukan kelas dengan rata-rata tertinggi!

**Tahap 5 — Visualize (20 menit)**

```python
# 1. Bar chart — rata-rata per mapel
mapel = ['Matematika','B_Indonesia','B_Inggris','Informatika','IPA','IPS']
rata_mapel = df[mapel].mean()

plt.figure(figsize=(10, 5))
plt.bar(mapel, rata_mapel, color='skyblue')
plt.title('Rata-rata Nilai per Mapel')
plt.ylabel('Nilai')
plt.xticks(rotation=45)
plt.tight_layout()
plt.savefig('rata_mapel.png')
plt.show()

# 2. Pie chart — distribusi grade
grade_counts = df['Grade'].value_counts()
plt.figure(figsize=(6, 6))
plt.pie(grade_counts, labels=grade_counts.index, autopct='%1.1f%%', startangle=90)
plt.title('Distribusi Grade')
plt.savefig('distribusi_grade.png')
plt.show()

# 3. Scatter — Matematika vs Informatika
plt.figure(figsize=(8, 6))
plt.scatter(df['Matematika'], df['Informatika'], alpha=0.6)
plt.xlabel('Matematika')
plt.ylabel('Informatika')
plt.title('Korelasi Matematika vs Informatika')
plt.grid(True)
plt.savefig('korelasi.png')
plt.show()
```

**Tugas:** Screenshot grafik yang dihasilkan!

**Tahap 6 — Export (10 menit)**

```python
# Simpan data bersih
df.to_csv('nilai_siswa_bersih.csv', index=False)

# Simpan statistik
statistik = df[mapel].describe()
statistik.to_csv('statistik_nilai.csv')
```

**Tugas:** Pastikan file CSV tersimpan!

**10. Aktivitas Mandiri — Dataset Pilihan (opsional)**
Jika selesai lebih awal: download dataset dari data.go.id dan coba pipeline yang sama.

#### Merefleksi (10 menit)

**11. Refleksi (10 menit)**
- Langkah pipeline mana yang paling sulit?
- Insight apa yang didapat dari data nilai?
- Di luar sekolah, data apa yang ingin diolah?

### Penutup (40 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Review pipeline: Load → Explore → Clean → Transform → Analyze → Visualize → Export | 10 menit |
| 2. Kuis lisan: "Apa fungsi `drop_duplicates()`? `fillna()`? `groupby()`?" | 10 menit |
| 3. Tugas kumpul: File `.py` atau `.ipynb` + 3 screenshot grafik | 10 menit |
| 4. Preview: "Pert 15: Review PAS S2. Bawa semua catatan Semester 2 — kita review untuk PAS!" | 10 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Load & explore | Tidak bisa | Bisa load | Load + info | Load + analisis awal |
| Clean | Tidak | 1 masalah | 2 masalah | Semua + strategi |
| Transform & analyze | Tidak | 1 langkah | 2–3 langkah | 4+ langkah |
| Visualize | Tidak | 1 grafik | 2 grafik | 3 grafik + rapi |
| Export | Tidak | Ada file | File + rapi | File + dokumentasi |

---

**MGMP Informatika SMAN 6 Cimahi**
