---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 14
## Konsep Kualitas Data & GIGO
### Informatika – Fase E / Kelas X
#### SMA Negeri 6 Cimahi

---

## Review — Tugas Audit Privasi

- Siapa yang sudah audit Instagram / TikTok?
- Temuan paling menarik?

> Privasi terkunci = data pribadi aman!

---

## Apersepsi

**NASA Mars Climate Orbiter — $327 juta meledak**

Penyebabnya?
> Satu tim pakai **satuan imperial** (pound-force)
> Tim lain pakai **satuan metrik** (newton)

**Data tidak konsisten → roket meledak.**

Itulah **GIGO**.

---

# TUJUAN PEMBELAJARAN

1. ✅ Memahami ciri data berkualitas
2. ✅ Menjelaskan prinsip GIGO
3. ✅ Mengidentifikasi jenis data bermasalah
4. ✅ Menganalisis dampak data tidak berkualitas

---

## Data Berkualitas — 5 Dimensi

| Kriteria | Artinya |
|---|---|
| **Akurat** | Sesuai kenyataan |
| **Lengkap** | Semua terisi |
| **Konsisten** | Format seragam |
| **Tepat waktu** | Data terbaru |
| **Relevan** | Sesuai kebutuhan |

---

## Prinsip GIGO

```
Input (Garbage)  →  Proses  →  Output (Garbage)
```

> "Data sampah masuk = hasil sampah keluar"

### Contoh GIGO:
| Input | Proses | Output |
|---|---|---|
| Tanggal 30-02-2009 | Rumus apapun | ❌ |
| Nilai "Tujuhpuluh" | Rata-rata | ❌ |
| Duit "5000" vs "5.000" | Penjumlahan | ❌ |

---

## Jenis Data Bermasalah

| Jenis | Contoh |
|---|---|
| **Format** | Tanggal campur aduk |
| **Missing** | Kolom kosong |
| **Duplicate** | Data muncul 2× |
| **Outlier** | Usia 200 tahun |
| **Inkonsisten** | "L", "LK", "Laki" |
| **Invalid** | 30 Februari, nilai -5 |

---

## Praktik: Identifikasi Data!

### Dataset "Data Siswa" — 15 baris

**Tugas per pasangan (40 menit):**
1. Buka dataset (3')
2. Identifikasi semua masalah (15')
3. Klasifikasikan jenisnya (10')
4. Analisis dampak (7')
5. Tulis laporan (5')

> Berapa masalah yang bisa kamu temukan?

---

## Contoh Data

| Nama | Kelas | Tgl Lahir | Nilai |
|---|---|---|---|
| Andi Pratama | X-1 | 15-03-2009 | 85 ✅ |
| Budi Santoso | X-1 | 2009-05-20 | ❌ |
| Cici | X-2 | 20/05/2009 | 95 |
| Andi Pratama | X-1 | 15-03-2009 | 85 ⚠️ |
| Dedi | X-3 | 01-01-1900 | 200 🚩|

> **Ada berapa masalah di 5 baris ini?**

---

## Tabel Laporan

| Baris | Field | Masalah | Jenis | Dampak |
|---|---|---|---|---|
| | | | | |

---

## Diskusi

1. Masalah paling sering ditemukan?
2. Kenapa data bisa sekacau itu?
3. Dampak terburuk jika data ini diproses?

---

## Rangkuman

| Konsep | Inti |
|---|---|
| **Data berkualitas** | Akurat + lengkap + konsisten |
| **GIGO** | Input jelek = output jelek |
| **Masalah data** | Format, missing, duplikat, outlier |

> "Data yang baik bukan kebetulan — butuh ketelitian."

---

## Tugas Rumah

### Cari 1 berita tentang GIGO!
- Kasus nyata dampak data tidak berkualitas
- Tulis ringkasan 3–5 kalimat
- Siapkan untuk diskusi pertemuan depan

---

## Pertemuan Berikutnya

### Validasi, Verifikasi & Data Cleansing
> Kita **bersihkan** dataset yang tadi!

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Garbage In, Garbage Out — data jelek, keputusan jelek."
