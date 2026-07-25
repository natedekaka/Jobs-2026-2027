# KUNCI JAWABAN — PTS SEMESTER 2

## A. Pilihan Ganda

| No | Jawaban | Pembahasan |
|---|---|---|
| 1 | **C** | Array = struktur data dengan indeks berurutan |
| 2 | **B** | Indeks array Python dimulai dari 0 |
| 3 | **D** | `A[1][2]` = baris indeks 1, kolom indeks 2 = elemen `6` |
| 4 | **B** | Stack = Last In First Out (LIFO) |
| 5 | **A** | Push = menambah data ke stack |
| 6 | **C** | `[5]` → `[5,3]` → pop(3) → `[5]` → `[5,7]` → sisa: 5 dan 7 |
| 7 | **A** | Queue = First In First Out (FIFO) |
| 8 | **C** | Enqueue = menambah data ke queue |
| 9 | **C** | `[2]` → `[2,4]` → dequeue(2) → `[4]` → `[4,6]` → sisa: 4 dan 6 |
| 10 | **B** | Stack LIFO, Queue FIFO |
| 11 | **C** | Sequential search = periksa data satu per satu dari awal |
| 12 | **C** | Worst case sequential = n perbandingan (data di akhir/tidak ada) |
| 13 | **B** | Binary search mensyaratkan data terurut |
| 14 | **D** | Binary search = O(log n) |
| 15 | **A** | `low=0, high=8, mid=4` (19), 12<19 → `high=3, mid=1` (5), 12>5 → `low=2, mid=2` (8), 12>8 → `low=3, mid=3` (12) ✅ → indeks: 4, 1, 2, 3 (yang ditanya indeks dibandingkan: 4, 2, 3) |
| 16 | **B** | Sorting = mengurutkan data |
| 17 | **B** | Bubble sort: data terbesar menggelembung ke akhir |
| 18 | **C** | Insertion sort: ambil 1 data → sisip ke posisi tepat |
| 19 | **C** | Data [2,4,6,8,1] hampir urut → insertion sort O(n), bubble tetap O(n²) |
| 20 | **A** | Stack LIFO cocok untuk undo/redo (membalikkan aksi) |

### Skoring PG
- Benar: 3 poin
- Salah: 0 poin
- Skor maks: 20 × 3 = 60

---

## B. Esai

### 21. Simulasi Stack (8 poin)

| No | Operasi | Keadaan Stack | Keterangan |
|---|---|---|---|
| 1 | `push(10)` | [10] | — |
| 2 | `push(20)` | [10, 20] | 20 di atas |
| 3 | `push(30)` | [10, 20, 30] | 30 di atas |
| 4 | `pop()` | [10, 20] | 30 dihapus |
| 5 | `push(40)` | [10, 20, 40] | 40 di atas |
| 6 | `pop()` | [10, 20] | 40 dihapus |

b. Data tersisa: **10 dan 20** (10 di bawah, 20 di atas)

**Rubrik:**
- Menggambar stack dengan benar setiap langkah: 5 poin (≈0,8 poin/langkah)
- Jawaban data tersisa benar: 3 poin

---

### 22. Simulasi Queue (8 poin)

| No | Operasi | Keadaan Queue | Keterangan |
|---|---|---|---|
| 1 | `enqueue(7)` | [7] | — |
| 2 | `enqueue(3)` | [7, 3] | 7 di depan |
| 3 | `enqueue(9)` | [7, 3, 9] | 7 di depan |
| 4 | `dequeue()` | [3, 9] | 7 dihapus |
| 5 | `enqueue(5)` | [3, 9, 5] | 3 di depan |

b. Data tersisa: **3, 9, dan 5** (3 di depan)

**Rubrik:**
- Menggambar queue dengan benar setiap langkah: 5 poin
- Jawaban data tersisa benar: 3 poin

---

### 23. Sequential Search (8 poin)

Array: [15, 8, 23, 42, 10, 31, 5, 18] — mencari 31

| Langkah | Indeks | Data | Sama dengan 31? |
|---|---|---|---|
| 1 | 0 | 15 | ❌ |
| 2 | 1 | 8 | ❌ |
| 3 | 2 | 23 | ❌ |
| 4 | 3 | 42 | ❌ |
| 5 | 4 | 10 | ❌ |
| 6 | 5 | 31 | ✅ Ditemukan! |

b. Jumlah perbandingan: **6 kali**

**Rubrik:**
- Menuliskan langkah-langkah dengan benar: 5 poin (≈0,8 poin/langkah)
- Jumlah perbandingan benar: 3 poin

---

### 24. Binary Search (8 poin)

Array: [3, 7, 10, 15, 20, 25, 30, 35, 42, 50] — mencari 25

| Langkah | low | high | mid | Data[mid] | Keterangan |
|---|---|---|---|---|---|
| 1 | 0 | 9 | 4 | 20 | 25 > 20 → cari kanan (low = mid+1 = 5) |
| 2 | 5 | 9 | 7 | 35 | 25 < 35 → cari kiri (high = mid-1 = 6) |
| 3 | 5 | 6 | 5 | 25 | ✅ Ditemukan! |

b. Jumlah perbandingan: **3 kali**

**Rubrik:**
- Menuliskan langkah (low, mid, high) dengan benar: 5 poin
- Jumlah perbandingan benar: 3 poin

---

### 25. Bubble Sort (8 poin)

Array: [42, 15, 8, 23, 10]

| Pas | Perbandingan & Pertukaran | Hasil Akhir Pas |
|---|---|---|
| 1 | 42>15 → T (15,42,8,23,10) → 42>8 → T (15,8,42,23,10) → 42>23 → T (15,8,23,42,10) → 42>10 → T (15,8,23,10,**42**) | [15, 8, 23, 10, **42**] |
| 2 | 15>8 → T (8,15,23,10,42) → 15>23 → F → 23>10 → T (8,15,10,**23**,42) | [8, 15, 10, **23**, 42] |
| 3 | 8>15 → F → 15>10 → T (8,10,**15**,23,42) | [8, **10**, **15**, 23, 42] |
| 4 | Semua terurut ✅ | **[8, 10, 15, 23, 42]** |

b. Jumlah pas: **4 pas**

**Rubrik:**
- Menuliskan keadaan array setiap pas dengan benar: 5 poin
- Jumlah pas benar: 3 poin

---

## Pedoman Penskoran

| Komponen | Skor Maks | Bobot |
|---|---|---|
| Pilihan Ganda (20 × 3) | 60 | 60% |
| Esai (5 × 8) | 40 | 40% |
| **Total** | **100** | **100%** |

**Rumus Nilai Akhir:**
```
Nilai = Skor PG + Skor Esai
```

**Konversi:**
| Nilai | Predikat |
|---|---|
| 92–100 | Sangat Baik (A) |
| 83–91 | Baik (B) |
| 75–82 | Cukup (C) |
| < 75 | Perlu Perbaikan (D) |

---

**MGMP Informatika SMAN 6 Cimahi**
