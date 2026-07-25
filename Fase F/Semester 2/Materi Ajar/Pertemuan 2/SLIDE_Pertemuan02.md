---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 2 — FASE F (S2)
## Data Cleansing & Labeling
### Informatika – Fase F / Kelas XI
#### SMA Negeri 6 Cimahi

---

## Review — Pert 1

```
Sumber data legal → data.go.id

Tapi data masih KOTOR!
```

> **Garbage In, Garbage Out!** 🗑️

---

## Tujuan Pembelajaran

1. ✅ Identifikasi masalah data
2. ✅ Data cleaning (Sheets)
3. ✅ Konsep labeling
4. ✅ Praktik labeling sentimen

---

# Masalah Kualitas Data

---

## 1. Missing Values

> Data kosong / tidak diisi

```
Nilai: 80, 75, _, 90, 85
           ↑ kosong!
```

**Solusi**: Isi rata-rata / hapus baris

---

## 2. Duplicates

> Data sama muncul 2× atau lebih

```
"Budi Santoso" — baris 5
"Budi Santoso" — baris 23  → HAPUS!
```

**Solusi**: Data → Remove duplicates

---

## 3. Outliers

> Nilai yang tidak wajar

```
Nilai UTS: 80, 75, 90, 85, 1000, 70
                                   ↑ OUTLIER!
```

**Solusi**: Filter → sort → cek nilai ekstrem

---

## 4. Inconsistent Data

> Format tidak seragam

```
Nama: "budi", "Budi", "BUDI"
Kelas: "X-A", " X-A", "XA", "10A"
```

**Solusi**: `=PROPER()`, `=TRIM()`, standarisasi

---

# TEKNIK CLEANING

---

## Google Sheets Cleaning

| Masalah | Cara |
|---|---|
| Cek missing | `=ISBLANK(A2)` |
| Hapus duplikat | Data → Remove duplicates |
| Standarisasi | `=PROPER()`, `=UPPER()`, `=LOWER()` |
| Bersihkan spasi | `=TRIM()` |
| Deteksi outlier | Filter → sort |

---

## Sebelum vs Sesudah

```
SEBELUM:    SESUDAH:
100 baris   95 baris (-5 duplikat)
5 kosong    0 kosong (isi rata-rata)
3 outlier   0 outlier (koreksi)
Campur aduk Seragam
```

> Data bersih = analisis akurat!

---

# DATA LABELING

---

## Apa itu Labeling?

> Memberi label/kategori pada data mentah untuk ML

```
"Produk bagus!"   → Positif
"Pengiriman lama" → Negatif
"Barang sesuai"   → Netral
```

---

## Jenis Labeling

```
Biner        : Spam / Bukan
Multi-class  : Pos / Neu / Neg
Multi-label  : [kucing, outdoor]
Regression   : Harga Rp 500jt
```

---

## Aktivitas 1 — Cleaning

### 35 menit — Individu

Dataset kotor → bersihkan!

```
Missing → Duplikat → Outlier → Standarisasi
```

Buat sheet "Hasil Cleaning"

---

## Aktivitas 2 — Labeling

### 25 menit — Berpasangan

Label 10 komentar sekolah:

| Komentar | Label? |
|---|---|
| "Sekolahku keren!" | ? |
| "Tugasnya banyak" | ? |
| "Biasa aja" | ? |

---

## Bandingkan!

Cocokkan label dengan kelompok lain!

> Kalau beda → diskusi, kenapa?

---

## Refleksi

- Masalah data paling sering ditemui?
- Teknik cleaning favorit?
- Skala 1–10?

---

## Preview — Pert 3

### Visualisasi Data & Dashboard

> Dashboard keren dari data bersih!

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Data bersih = analisis akurat = keputusan tepat!"
