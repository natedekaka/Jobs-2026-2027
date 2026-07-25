# BAHAN AJAR – PERTEMUAN 16
## Visualisasi Data

| TP | BK, AP — Pengolahan Data Bervolume Besar |
|---|---|

---

### A. MENGAPA VISUALISASI DATA?

```
Tabel:              vs      Grafik Batang:
┌──────┬───────┐            📊 Nilai Rata-rata per Kelas
│ Kelas│ Nilai │            ██
│ X-A  │ 85    │            ██  ██
│ X-B  │ 78    │            ██  ██  ██
│ X-C  │ 72    │            ██  ██  ██  ██
│ X-D  │ 80    │            ──────────────────
└──────┴───────┘             X-A X-B X-C X-D
```

**Fakta**: Otak manusia memproses gambar 60.000× lebih cepat dari teks.

---

### B. JENIS GRAFIK & KAPAN MENGGUNAKANNYA

#### 1. Column / Bar Chart

```
Kegunaan: Membandingkan antar kategori
Data: Kategorikal + Numerik
Variasi: Stacked bar (komposisi), Grouped bar (perbandingan ganda)
```

#### 2. Line Chart

```
Kegunaan: Menampilkan tren dari waktu ke waktu
Data: Time series + Numerik
Tips: Hati-hati dengan sumbu Y yang tidak dari 0
```

#### 3. Pie / Donut Chart

```
Kegunaan: Proporsi/bagian dari keseluruhan
Data: Kategorikal + Persentase
Tips: Maksimal 5 irisan — jangan gunakan 3D!
```

#### 4. Scatter Plot

```
Kegunaan: Menunjukkan korelasi antara 2 variabel numerik
Data: Numerik + Numerik
Tips: Tambahkan trendline untuk melihat arah korelasi
```

#### 5. Heatmap

```
Kegunaan: Matriks berwarna — cocok untuk data padat
Data: 2 kategori + Nilai
Contoh: Aktivitas per jam per hari, korelasi antar fitur
```

#### 6. Histogram

```
Kegunaan: Distribusi frekuensi (sebaran data)
Data: Numerik + Frekuensi
Tips: Pilih bin size yang tepat — terlalu besar = kehilangan detail
```

#### Panduan Cepat

| Data | Grafik |
|---|---|
| Kategori vs nilai | Bar / Column |
| Perubahan waktu | Line |
| Proporsi | Pie / Donut |
| Korelasi 2 variabel | Scatter |
| Distribusi | Histogram |
| Matriks padat | Heatmap |
| Komposisi + total | Stacked Bar |

---

### C. PRINSIP VISUALISASI YANG BAIK

#### 1. Data-Ink Ratio (Edward Tufte)

> Proporsi tinta yang digunakan untuk menampilkan data dibanding total tinta.

**Tingkatkan rasio dengan:**
- Hapus latar belakang gradien
- Hapus efek 3D
- Minimalisir grid lines
- Gunakan warna hanya untuk data penting

#### 2. Warna yang Efektif

| Lakukan | Jangan |
|---|---|
| Gunakan palet terbatas (2–5 warna) | Pelangi (rainbow) — membingungkan |
| Warna konsisten di seluruh grafik | Merah & hijau bersamaan (buta warna) |
| Warna kontras untuk data penting | Warna pudar tidak terbaca di proyektor |
| Biru/oren: ramah buta warna | Gradien tanpa arti |

#### 3. Label & Judul

| Elemen | Contoh |
|---|---|
| Judul grafik | "Rata-rata Nilai UAS per Kelas" |
| Label sumbu X | "Kelas" |
| Label sumbu Y | "Nilai (0–100)" |
| Legend | Jika perlu, letakkan di bawah/kanan |
| Sumber data | "Sumber: Data Nilai Siswa 2026" |

#### 4. Skala Jujur

| Aturan | Penjelasan |
|---|---|
| Sumbu Y dari 0 | Jangan dipotong — akan membesar-besarkan perbedaan |
| Skala proporsional | Luas/sebanding dengan nilai |
| Sumbu waktu konsisten | Interval waktu harus sama |

#### 5. Minimalis

**SETIAP elemen harus punya alasan.**
- Tidak ada efek 3D (kecuali dibutuhkan)
- Tidak ada gambar/clipart dekoratif
- Grid opsional, tipis
- Font simple, ukuran konsisten

---

### D. VISUALISASI MENYESATKAN

| Trik Kotor | Contoh | Cara Memperbaiki |
|---|---|---|
| **Truncated Y-axis** | Sumbu Y dari 50, bukan 0 | Mulai dari 0 |
| **3D Pie** | Irisan depan terlihat lebih besar | 2D donut chart |
| **Cherry-picking** | Grafik "kenaikan saham" dari titik terendah | Tampilkan seluruh rentang |
| **Skala ganda** | Dua sumbu Y berbeda di satu grafik | Pisahkan jadi 2 grafik |
| **Pemilihan chart salah** | Data waktu tapi pakai pie (tidak menunjukkan tren) | Ganti ke line chart |
| **Over-plotting** | 1000 titik di scatter tanpa transparansi | Gunakan alpha/hexbin |

**Latihan**: Cari 1 grafik menyesatkan di internet → analisis apa yang salah → tulis perbaikannya.

---

### E. ALAT VISUALISASI

| Alat | Kelebihan | Kekurangan |
|---|---|---|
| **Google Sheets** | Gratis, familiar | Terbatas templatenya |
| **Datawrapper** | Gratis, hasil jurnalistik, embed | Butuh koneksi internet |
| **Canva** | Template cantik, drag-drop | Versi gratis terbatas |
| **Python Matplotlib** | Bebas, kustom total | Butuh coding |
| **Tableau Public** | Interaktif, gratis | Data publik |

#### Quick Start — Datawrapper

1. Buka `datawrapper.de` → Klik "Create a Chart"
2. Upload dataset (CSV) atau paste data
3. Pilih jenis grafik
4. Atur warna, label, judul
5. Publish → Export sebagai PNG/PDF

#### Quick Start — Canva

1. Buka `canva.com` → Cari "Infographic"
2. Pilih template
3. Klik "Charts" → Pilih jenis
4. Edit data di spreadsheet Canva
5. Download sebagai PNG/PDF

---

### F. CONTOH KASUS

**Dataset**: Nilai siswa dari Pert 15

| Aktivitas | Grafik | Insight |
|---|---|---|
| Rata-rata per kelas | Column chart | X-A terbaik, X-C perlu perhatian |
| Remedial per kelas | Pie chart | 20% siswa remedial |
| Korelasi UTS vs UAS | Scatter + trendline | Semakin tinggi UTS, semakin tinggi UAS |
| Sebaran nilai UAS | Histogram | Mayoritas di 70–85 |
| Aktivitas per jam (data dummy) | Heatmap | Jam produktif: 8–10 |

---

**MGMP Informatika SMAN 6 Cimahi**
