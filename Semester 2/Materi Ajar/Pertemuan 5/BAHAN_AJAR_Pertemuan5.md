# BAHAN AJAR – PERTEMUAN 5
## Binary Search (Pencarian Biner)

| TP | BK 1.1, 1.3 |
|---|---|

---

### A. KONSEP BINARY SEARCH

Binary search adalah algoritma pencarian yang bekerja dengan **membagi array terurut menjadi dua bagian** secara berulang hingga target ditemukan.

#### Syarat: Data Harus Terurut!

| Urut | Bisa Binary? |
|---|---|
| [10, 23, 45, 56, 78, 89, 92, 99] | ✅ Ya |
| [10, 45, 23, 89, 56, 78, 99, 92] | ❌ Tidak |

#### Cara Kerja

1. Tentukan **tengah** array: `mid = (kiri + kanan) / 2`
2. Bandingkan `arr[mid]` dengan `target`:
   - `arr[mid] == target` → ketemu, selesai
   - `arr[mid] > target` → cari di **kiri** (kanan = mid - 1)
   - `arr[mid] < target` → cari di **kanan** (kiri = mid + 1)
3. Ulangi sampai ketemu atau habis

#### Ilustrasi

**Cari 23 di [10, 23, 45, 56, 78, 89, 92, 99]:**

```
Langkah 1: kiri=0, kanan=7, mid=3 (nilai 56)
           23 < 56 → cari kiri (kanan = 2)
           [10, 23, 45, 56] ← sisa

Langkah 2: kiri=0, kanan=2, mid=1 (nilai 23)
           23 = 23 → KETEMU di indeks 1!
```

**Hanya 2 langkah!** Sequential butuh 2 langkah juga (kebetulan 23 di posisi 2).

#### Contoh Lain: Cari 99

```
Langkah 1: mid=3 (56), 99 > 56 → cari kanan (kiri=4)
           [78, 89, 92, 99]
Langkah 2: mid=5 (89), 99 > 89 → cari kanan (kiri=6)
           [92, 99]
Langkah 3: mid=6 (92), 99 > 92 → cari kanan (kiri=7)
           [99]
Langkah 4: mid=7 (99), 99 = 99 → KETEMU!
```

---

### B. PERBANDINGAN SEQUENTIAL VS BINARY

| Aspek | Sequential Search | Binary Search |
|---|---|---|
| **Syarat data** | Tidak perlu terurut | **Harus terurut** |
| **Cara kerja** | Cek satu per satu dari awal | Belah dua, buang setengah |
| **Kecepatan** | O(n) — linear | O(log n) — logaritmik |
| **Kompleksitas** | Sederhana | Sedang |
| **Cocok untuk** | Data kecil (<100) | Data besar |

#### Perbandingan Jumlah Langkah

| Jumlah Data (n) | Sequential (maks) | Binary (maks) |
|---|---|---|
| 10 | 10 | 4 |
| 100 | 100 | 7 |
| 1.000 | 1.000 | 10 |
| 10.000 | 10.000 | 14 |
| 100.000 | 100.000 | 17 |
| **1.000.000** | **1.000.000** | **20** |

**Rumus binary search:** maksimal langkah = ⌈log₂(n)⌉ + 1
- log₂(10) ≈ 3,3 → 4 langkah
- log₂(1.000.000) ≈ 19,9 → 20 langkah

---

### C. BINARY SEARCH DI PYTHON

```python
def binary_search(arr, target):
    kiri = 0
    kanan = len(arr) - 1
    
    while kiri <= kanan:
        mid = (kiri + kanan) // 2
        
        if arr[mid] == target:
            return mid          # Ditemukan
        elif arr[mid] < target:
            kiri = mid + 1      # Cari di kanan
        else:
            kanan = mid - 1     # Cari di kiri
    
    return -1                   # Tidak ditemukan

# Contoh
nilai = [10, 23, 45, 56, 78, 89, 92, 99]
print(binary_search(nilai, 23))  # Output: 1
print(binary_search(nilai, 50))  # Output: -1
```

---

### D. TEBAK ANGKA — BINARY SEARCH DI KEHIDUPAN

Permainan tebak angka 1–100 adalah contoh sempurna binary search:

| Tebakan | Respon | Rentang Tersisa |
|---|---|---|
| 50 | "Terlalu besar" | 1–49 |
| 25 | "Terlalu kecil" | 26–49 |
| 37 | "Terlalu besar" | 26–36 |
| 31 | "Terlalu kecil" | 32–36 |
| 34 | "Terlalu besar" | 32–33 |
| 33 | "Terlalu kecil" | 32 |
| **32** | **"BENAR!"** | ✅ |

**7 tebakan** untuk angka 1–100. Tidak akan pernah lebih dari 7!

#### Contoh Binary Search di Kehidupan

| Situasi | Cara Binary |
|---|---|
| Cari kata di kamus | Buka tengah → cek abjad → buang setengah |
| Cari nama di buku telepon | Buka tengah → cek huruf → buang setengah |
| Tebak harga barang | "Lebih mahal?" / "Lebih murah?" |
| Debug kode | Cari error dengan membelah kode jadi dua |

---

### E. RANGKUMAN

1. **Binary search**: belah data terurut jadi dua, buang setengah yang tidak mungkin
2. **Syarat**: data harus **terurut**
3. **O(log n)** — sangat cepat untuk data besar (1 juta → 20 langkah)
4. Sequential = O(n) — binary = O(log n) — binary **jauh lebih cepat**

---

**MGMP Informatika SMAN 6 Cimahi**
