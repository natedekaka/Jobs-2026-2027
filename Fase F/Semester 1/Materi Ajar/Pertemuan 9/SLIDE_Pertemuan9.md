---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 9 — FASE F
## Divide and Conquer
### Informatika – Fase F / Kelas XI
#### SMA Negeri 6 Cimahi

---

## Review — Pert 8

**Greedy**: Ambil yang terbaik sekarang

> **D&C**: Pecah masalah besar → kecil → selesaikan → gabung!

---

## Apersepsi

"Cari buku di perpustakaan yang rapi berurutan — bagaimana cara cepat?"

> Jawaban: **Binary Search** — belah dua terus!

---

# TUJUAN PEMBELAJARAN

1. ✅ 3 langkah D&C
2. ✅ Binary Search
3. ✅ Merge Sort
4. ✅ Analisis kompleksitas

---

## 3 Langkah D&C

```
┌────────────────┐
│    MASALAH     │
└───────┬────────┘
        │ DIVIDE
   ┌────┼────┐
   ▼    ▼    ▼
 ┌──┐ ┌──┐ ┌──┐
 │S1│ │S2│ │S3│ ← CONQUER
 └──┘ └──┘ └──┘
   │    │    │
   └────┼────┘
        │ COMBINE
   ┌────┴────┐
   │ SOLUSI  │
   └─────────┘
```

---

## Analogi

| Langkah | Menelepon Teman |
|---|---|
| **Divide** | "Kamu cari toko A, kamu toko B, kamu toko C" |
| **Conquer** | "Toko A: ada, harga 50rb" |
| **Combine** | "Toko A termurah, beli di sana!" |

---

## Binary Search — Visual

Cari 19 di [2,5,8,12,19,24,31,37]

```
Langkah 1: [2, 5, 8, 12, 19, 24, 31, 37]
                    ↑ (tengah = 12)
             19 > 12 → cari kanan

Langkah 2: [19, 24, 31, 37]
                   ↑ (tengah = 31)
             19 < 31 → cari kiri

Langkah 3: [19, 24]
                ↑ (tengah = 19)
              19 = 19! ✅ Ditemukan!
```

---

## Pseudocode Binary Search

```
FUNCTION BinarySearch(arr, target)
    kiri ← 1
    kanan ← n
    
    WHILE kiri ≤ kanan DO
        tengah ← (kiri+kanan)/2
        IF arr[tengah] = target THEN
            RETURN tengah
        ELSE IF arr[tengah] < target THEN
            kiri ← tengah + 1
        ELSE
            kanan ← tengah - 1
        ENDIF
    ENDWHILE
    RETURN -1
END
```

---

## Kompleksitas Binary Search

| n | Sequential O(n) | Binary O(log n) |
|---|---|---|
| 10 | 10 | 4 |
| 100 | 100 | 7 |
| 1.000 | 1.000 | 10 |
| 1.000.000 | 1.000.000 | **20** |

> **50.000× lebih cepat!** 🚀

---

## Merge Sort — Divide

```
[38, 27, 43, 3, 9, 82, 10]

           DIVIDE
             ↓
 [38, 27, 43, 3]    [9, 82, 10]
   ↓        ↓          ↓     ↓
[38,27]  [43,3]    [9,82]   [10]
 ↓   ↓    ↓   ↓    ↓    ↓
[38][27] [43][3]  [9] [82]
```

---

## Merge Sort — Conquer & Combine

```
            COMBINE
              ↓
 [27,38]  [3,43]    [9,82]   [10]
     \      /          \      /
   [3,27,38,43]      [9,10,82]
          \              /
       [3,9,10,27,38,43,82]
```

> **Hasil: Terurut!** ✅

---

## Merge Sort — Kompleksitas

| n | Bubble O(n²) | Merge O(n log n) |
|---|---|---|
| 10 | 100 | 40 |
| 100 | 10.000 | 700 |
| 1.000 | 1.000.000 | 10.000 |

> Merge Sort **100× lebih cepat** untuk 1.000 data!

---

## Aktivitas 1: Binary Search

### Individu — 10 menit

Data: [3,7,11,15,22,28,34,41,50,56]

| Cari | Langkah | Indeks |
|---|---|---|
| 34 | ? | ? |
| 7 | ? | ? |
| 50 | ? | ? |

---

## Aktivitas 2: Merge Sort

### Berpasangan — 15 menit

Data: [42,16,7,23,31,5,19,8]

Gambar pohon divide → combine!

> Hasil akhir: [?, ?, ?, ?, ?, ?, ?, ?]

---

## Aktivitas 3: Perbandingan

### 10 menit

| n | Sequential | Binary | Bubble | Merge |
|---|---|---|---|---|
| 10 | | | | |
| 100 | | | | |
| 1.000 | | | | |

---

## Rangkuman

| Algoritma | Strategi | Kecepatan |
|---|---|---|
| **Binary Search** | D&C — bagi tengah | O(log n) |
| **Merge Sort** | D&C — bagi-urut-gabung | O(n log n) |
| Sequential | Linear | O(n) |
| Bubble Sort | Iteratif | O(n²) |

> D&C = cepat untuk data besar!

---

## Tugas Rumah

Tulis **pseudocode Binary Search** lengkap!

> Kirim ke guru!

---

## Pertemuan Depan

### Backtracking
> "Mundur jika salah langkah — seperti puzzle!"

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Pecahkan masalah besar dengan memotongnya menjadi bagian yang lebih kecil." — Charles E. Leiserson
