---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 6 — SEMESTER 2
## Bubble Sort & Insertion Sort
### Informatika – Fase E / Kelas X
#### SMA Negeri 6 Cimahi

---

## Review — Binary Search

Syarat binary search?
> **Data harus terurut!**

Hari ini kita belajar **mengurutkan** data.

---

## Apersepsi

**5 siswa maju — tinggi badan berbeda.**

"Urutkan dari terpendek ke tertinggi!"

Prosesnya: bandingkan, tukar posisi, ulangi.

> Itulah **sorting**! Dan kita akan belajar dua caranya.

---

# TUJUAN PEMBELAJARAN

1. ✅ Konsep sorting
2. ✅ Bubble Sort — gelembung mengapung
3. ✅ Insertion Sort — menyusun kartu
4. ✅ Perbandingan keduanya

---

## Apa Itu Sorting?

**Sorting** = mengurutkan data

| Urutan | Contoh |
|---|---|
| **Ascending** (menaik) | 1, 2, 3, 4, 5 |
| **Descending** (menurun) | 5, 4, 3, 2, 1 |

**Kenapa penting?**
- Binary search butuh data terurut
- Data lebih mudah dianalisis

---

## Bubble Sort

**Prinsip:** Bandingkan dua data berdekatan → tukar jika tidak urut → data terbesar mengapung ke akhir

```
Pas 1: [5, 3, 8, 1]
 5>3 → TUKAR → [3, 5, 8, 1]
 5<8 → TETAP
 8>1 → TUKAR → [3, 5, 1, 8] ✅ 8 mengapung
```

---

## Bubble Sort — Animasi

```
[5, 3, 8, 1]

Pas 1: [3, 5, 1, 8] → 8 di akhir
Pas 2: [3, 1, 5, 8] → 5 di akhir
Pas 3: [1, 3, 5, 8] ✅ URUT!
```

Seperti **gelembung udara** yang naik ke permukaan!

---

## Insertion Sort

**Prinsip:** Ambil data → sisipkan ke posisi yang tepat

Seperti **menyusun kartu di tangan**:

```
[5, 3, 8, 1]

Ambil 5 → [5]
Ambil 3 → 3<5 → [3, 5]
Ambil 8 → 8>5 → [3, 5, 8]
Ambil 1 → 1<3 → [1, 3, 5, 8] ✅
```

---

## Insertion Sort — Visual

| Langkah | Kartu di Tangan | Aksi |
|---|---|---|
| 1 | [5] | Ambil 5 |
| 2 | [3, 5] | Ambil 3, sisip di depan 5 |
| 3 | [3, 5, 8] | Ambil 8, sisip di belakang |
| 4 | [1, 3, 5, 8] | Ambil 1, sisip di depan |

---

## Aktivitas 1: Bubble Sort

### Berpasangan — 15 menit

Kartu: [5, 3, 8, 1, 6]

Praktik bubble sort:
1. Bandingkan 2 kartu berdekatan
2. Tukar jika tidak urut
3. Ulangi sampai urut

> Catat jumlah pertukaran!

---

## Aktivitas 2: Insertion Sort

### Berpasangan — 15 menit

Kartu: [5, 3, 8, 1, 6]

Praktik insertion sort:
1. Ambil 1 kartu
2. Sisipkan ke posisi tepat
3. Ulangi sampai semua terambil

> Catat jumlah langkah!

---

## Bubble vs Insertion

| Aspek | Bubble | Insertion |
|---|---|---|
| Cara | Tukar pasangan | Sisip ke posisi |
| Data hampir urut | ❌ Tetap O(n²) | ✅ O(n) |
| Pertukaran | Banyak | Sedikit |

> **Kesimpulan:** Insertion sort > Bubble sort (untuk data nyata)

---

## Contoh: [2, 4, 6, 8, 1]

**Bubble:** 4 pas (banyak tukar)
**Insertion:** Ambil 1, geser 4x → selesai!

> Insertion jauh lebih cepat untuk data yang hampir urut!

---

## Rangkuman

| Algoritma | Prinsip | Kecepatan |
|---|---|---|
| **Bubble Sort** | Tukar berpasangan | O(n²) |
| **Insertion Sort** | Sisip ke posisi tepat | O(n²) / O(n) |

---

## Persiapan PTS! 📝

### Materi PTS (Pertemuan 7):

| Pert | Materi |
|---|---|
| 1 | Array |
| 2 | Stack |
| 3 | Queue |
| 4 | Sequential Search |
| 5 | Binary Search |
| 6 | Bubble & Insertion Sort |

> Mulai review dari sekarang!

---

## Pertemuan Depan

### 📝 PTS — Penilaian Tengah Semester
> Ujian tulis — struktur data & algoritma

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Sorting mengajarkan: kadang butuh beberapa kali pertukaran untuk mencapai urutan yang benar — seperti hidup."
