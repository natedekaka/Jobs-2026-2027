# BAHAN AJAR – PERTEMUAN 9
## Strategi Algoritmik — Divide and Conquer

| TP | BK, AP — Strategi Algoritmik |
|---|---|

---

### A. APA ITU DIVIDE AND CONQUER?

**Divide and Conquer** (Pecah dan Taklukkan) adalah strategi algoritmik di mana masalah besar dipecah menjadi submasalah yang lebih kecil, diselesaikan masing-masing, lalu digabungkan kembali.

#### 3 Langkah D&C

```
         ┌──────────────────────────┐
         │    MASALAH BESAR         │
         └──────────┬───────────────┘
                    │ DIVIDE
         ┌──────────┼──────────┐
         ▼          ▼          ▼
    ┌────────┐ ┌────────┐ ┌────────┐
    │ Sub-1  │ │ Sub-2  │ │ Sub-3  │ ← CONQUER (selesaikan)
    └────────┘ └────────┘ └────────┘
         │          │          │
         └──────────┼──────────┘
                    │ COMBINE
         ┌──────────┴───────────┐
         │      SOLUSI          │
         └──────────────────────┘
```

#### Analogi: Menelepon Teman

| Langkah | Analogi |
|---|---|
| **Divide** | Minta 3 teman cari di 3 toko berbeda |
| **Conquer** | Masing-masing cari di tokonya |
| **Combine** | Kumpulkan info: "Toko A ada, termurah!" |

---

### B. BINARY SEARCH — D&C PERTAMA

**Binary Search** mencari data dalam array **terurut** dengan cara membagi array menjadi dua bagian setiap langkah.

#### Syarat: Data harus sudah terurut!

#### Visualisasi: Cari 19

```
Langkah 1: [2, 5, 8, 12, 19, 24, 31, 37]
              ↑            ↑           ↑
              kiri        tengah     kanan
              (idx 0)     (idx 3)   (idx 7)
                        19 > 12 → cari kanan

Langkah 2: [19, 24, 31, 37]
            ↑     ↑        ↑
           kiri tengah    kanan
           (4)  (idx 5)   (7)
              19 < 31 → cari kiri

Langkah 3: [19, 24]
            ↑    ↑   ↑
          kiri tgh kanan
          (4)  (4)  (5)
            19 = 19 → Ditemukan! ✅
```

#### Pseudocode Binary Search

```
FUNCTION BinarySearch(arr[1..n], target)
    kiri ← 1
    kanan ← n
    
    WHILE kiri ≤ kanan DO
        tengah ← (kiri + kanan) / 2
        
        IF arr[tengah] = target THEN
            RETURN tengah  // ditemukan
        ELSE IF arr[tengah] < target THEN
            kiri ← tengah + 1  // cari kanan
        ELSE
            kanan ← tengah - 1  // cari kiri
        ENDIF
    ENDWHILE
    
    RETURN -1  // tidak ditemukan
END
```

#### Kompleksitas Waktu

| Ukuran Data (n) | Sequential Search O(n) | Binary Search O(log n) |
|---|---|---|
| 10 | 10 langkah | 4 langkah |
| 100 | 100 langkah | 7 langkah |
| 1.000 | 1.000 langkah | 10 langkah |
| 1.000.000 | 1.000.000 langkah | **20 langkah** |

> Binary Search 50.000× lebih cepat untuk 1 juta data!

---

### C. MERGE SORT — ANDALAN D&C

**Merge Sort** mengurutkan data dengan cara: bagi array sampai masing-masing tinggal 1 elemen, lalu gabungkan kembali secara terurut.

#### Visualisasi Lengkap

```
Data awal: [38, 27, 43, 3, 9, 82, 10]

                       DIVIDE
                       
        [38, 27, 43, 3]          [9, 82, 10]
           /        \               /     \
     [38, 27]     [43, 3]       [9, 82]   [10]
      /    \       /    \        /    \
   [38]   [27]  [43]   [3]    [9]   [82]

                     CONQUER & COMBINE
                     
   [27, 38]     [3, 43]       [9, 82]   [10]
        \         /              \       /
     [3, 27, 38, 43]          [9, 10, 82]
              \                  /
           [3, 9, 10, 27, 38, 43, 82]
```

#### Proses Merge (Gabung)

Menggabungkan [27, 38] dan [3, 43] menjadi [3, 27, 38, 43]:

```
[27, 38]   [3, 43]   → Bandingkan 27 vs 3 → ambil 3
[27, 38]   [43]      → Bandingkan 27 vs 43 → ambil 27
[38]       [43]      → Bandingkan 38 vs 43 → ambil 38
[]         [43]      → Sisa 43 → ambil 43
Hasil: [3, 27, 38, 43] ✅
```

#### Pseudocode Merge Sort

```
PROCEDURE MergeSort(arr[1..n])
    IF n ≤ 1 THEN
        RETURN arr  // base case
    ENDIF
    
    tengah ← n / 2
    kiri ← arr[1..tengah]     // DIVIDE
    kanan ← arr[tengah+1..n]  // DIVIDE
    
    kiriTerurut ← MergeSort(kiri)   // CONQUER
    kananTerurut ← MergeSort(kanan) // CONQUER
    
    RETURN Merge(kiriTerurut, kananTerurut)  // COMBINE
END

FUNCTION Merge(kiri[1..n1], kanan[1..n2])
    hasil ← []
    i ← 1
    j ← 1
    
    WHILE i ≤ n1 AND j ≤ n2 DO
        IF kiri[i] ≤ kanan[j] THEN
            hasil ← hasil + [kiri[i]]
            i ← i + 1
        ELSE
            hasil ← hasil + [kanan[j]]
            j ← j + 1
        ENDIF
    ENDWHILE
    
    // Sisa elemen
    hasil ← hasil + kiri[i..n1]
    hasil ← hasil + kanan[j..n2]
    
    RETURN hasil
END
```

---

### D. PERBANDINGAN ALGORITMA

#### Searching

| Algoritma | Strategi | Kompleksitas | Syarat |
|---|---|---|---|
| Sequential Search | Linear | O(n) | Tidak perlu urut |
| Binary Search | D&C | O(log n) | Data harus terurut |

#### Sorting

| Algoritma | Strategi | Kompleksitas | Stabil? |
|---|---|---|---|
| Bubble Sort | Iteratif | O(n²) | Ya |
| Insertion Sort | Iteratif | O(n²) | Ya |
| **Merge Sort** | **D&C** | **O(n log n)** | **Ya** |
| Quick Sort | D&C | O(n log n) rata-rata | Tidak |

#### Visual Grafik

```
Langkah
  ↑
  |                     Bubble Sort O(n²)
  |                  /
  |               /
  |            /  Merge Sort O(n log n)
  |         /   
  |      /    
  |   /  Binary Search O(log n)
  | /
  └──────────────────────────────→ n
```

---

### E. RANGKUMAN

| Konsep | Inti |
|---|---|
| **D&C** | Divide → Conquer → Combine |
| **Binary Search** | Cari di array terurut — O(log n) |
| **Merge Sort** | Urut dengan bagi-gabung — O(n log n) |
| **Divide** | Pecah hingga 1 elemen (base case) |
| **Combine** | Gabung kembali secara terurut |
| **Kompleksitas** | D&C biasanya O(n log n) atau O(log n) |

---

**MGMP Informatika SMAN 6 Cimahi**
