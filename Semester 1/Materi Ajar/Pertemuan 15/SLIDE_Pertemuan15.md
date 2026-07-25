---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 15
## Validasi, Verifikasi & Data Cleansing
### Informatika – Fase E / Kelas X — SUMATIF
#### SMA Negeri 6 Cimahi

---

## Review — Tugas Berita GIGO

- Siapa yang berhasil menemukan berita dampak data jelek?
- 1–2 siswa cerita!

> Input jelek → output jelek.
> Tapi hari ini kita akan **membersihkan** inputnya!

---

## Apersepsi

**Kemarin:** Kita menemukan ~20 masalah dalam 15 baris data.

**Hari ini:** Kita akan **membersihkan** dataset 25 baris!

> "Data cleansing adalah merapikan kamar — setelahnya, semuanya jadi mudah."

---

# TUJUAN PEMBELAJARAN

1. ✅ Menerapkan validasi format, tipe, range
2. ✅ Menggunakan filter, sort, remove duplicates
3. ✅ Membersihkan dataset kotor jadi bersih
4. ✅ Membuat laporan log perubahan

---

## Validasi vs Verifikasi

| Validasi | Verifikasi |
|---|---|
| **"Formatnya benar?"** | **"Isinya benar?"** |
| Nilai 0–100? ✅ | Nilai 85, tapi aslinya 95? ❌ |
| Tanggal DD-MM-YYYY? ✅ | Tanggal 15-03-2009, asli 15-03-2009? ✅ |
| No HP angka semua? ✅ | No HP 08123456789 — punya Andi? ✅ |

> **Hari ini fokus di VALIDASI + CLEANSING.**

---

## Teknik Cleansing — Demo

| Teknik | Untuk Apa? |
|---|---|
| **Filter** | Lihat missing & outlier |
| **Remove Duplicates** | Hapus data dobel |
| **Find & Replace** | Standarisasi (x-1 → X-1) |
| **Data Validation** | Batasi input |
| **Conditional Format** | Tandai otomatis |
| **TRIM() / PROPER()** | Rapikan teks |

---

## Proyek Sumatif (50 menit)

### Dataset: 25 baris data kotor

| Tahap | Waktu |
|---|---|
| 1. **Persiapan** | 5' |
| 2. **Validasi** — cek aturan | 15' |
| 3. **Cleansing** — perbaiki | 15' |
| 4. **Final** — dataset bersih + log | 15' |

---

## Aturan Validasi

| Aturan | Kolom | Cek |
|---|---|---|
| Format tanggal konsisten | Tgl Lahir | DD-MM-YYYY |
| Range 0–100, angka | Nilai | ≥ 0 dan ≤ 100 |
| 10–13 digit, angka saja | No HP | Cari yang ada huruf |
| Format "X-1", "X-2", "X-3" | Kelas | Cari "x-1", "X-22" |
| Tidak boleh kosong | Semua | Minimal nama & kelas |

---

## Log Cleansing

| No | Masalah | Teknik | Baris | Sebelum | Sesudah |
|---|---|---|---|---|---|
| | | | | | |

> Target: **minimal 10 baris log!**

---

## Contoh Log

| No | Masalah | Teknik | Baris | Sebelum | Sesudah |
|---|---|---|---|---|---|
| 1 | Duplikat Andi | Remove Dupes | 4 | Andi 2× | 1 baris |
| 2 | Format tanggal | F&R | 2 | 2009-05-20 | 20-05-2009 |
| 3 | Kelas "x-1" | F&R | 8 | x-1 | X-1 |
| 4 | Nilai "AB" | Hapus | 14 | AB | (kosong) |
| 5 | No HP "08567ABCD" | Koreksi | 6 | 08567ABCD | 08567123456 |

---

## Hasil Akhir

### Kumpulkan file Excel/Sheets dengan 3 sheet:

| Sheet | Isi |
|---|---|
| **RAW** | Dataset asli (jangan diubah) |
| **CLEAN** | Dataset yang sudah dibersihkan |
| **LOG** | Laporan perubahan (min 10 baris) |

> Nama file: `Nama1_Nama2_Kelas_Cleansing.xlsx`

---

## Perbandingan Before-After

| Metrik | RAW | CLEAN |
|---|---|---|
| Jumlah baris | | |
| Duplikat | | |
| Missing value | | |
| Format error | | |

> Dataset bersih lebih sedikit, lebih rapi, lebih **berguna**!

---

## Rangkuman

| Tahap | Hasil |
|---|---|
| **Validasi** | Aturan ditegakkan |
| **Cleansing** | 15+ perbaikan |
| **Final** | Dataset bersih ✅ |

> "Data cleansing bukan sekali — tapi kebiasaan."

---

## Pertemuan Berikutnya

### HAKI, Profesi IT & Digitalisasi Budaya
> Bagian terakhir sebelum PAS!

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Data bersih = keputusan cerdas."
