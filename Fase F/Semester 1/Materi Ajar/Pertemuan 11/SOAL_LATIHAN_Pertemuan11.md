# SOAL LATIHAN STRATEGI ALGORITMIK
## Pertemuan 11 – Greedy, D&C, Backtracking

| Nama | ____________________ |
|---|---|
| Kelas | ____________________ |
| Tanggal | ____________________ |

---

## A. GREEDY (Soal 1-2)

### Soal 1 — Penukaran Koin (15 menit)

Tentukan jumlah koin/lembar minimal untuk menukar **Rp23.400** menggunakan pecahan:
Rp10.000, Rp5.000, Rp2.000, Rp1.000, Rp500, Rp200, Rp100

| Langkah | Sisa Uang | Ambil Pecahan | Sisa Baru |
|---|---|---|---|
| 1 | Rp23.400 | | |
| 2 | | | |
| 3 | | | |
| 4 | | | |
| 5 | | | |
| ... | | | |

Jumlah minimal: ______ lembar/koin

### Soal 2 — Fractional Knapsack (15 menit)

Tas kapasitas **40 kg**. Tentukan nilai maksimal!

| Barang | Berat (kg) | Harga Total | Density (harga/kg) |
|---|---|---|---|
| A | 8 | Rp120.000.000 | |
| B | 15 | Rp150.000.000 | |
| C | 12 | Rp180.000.000 | |
| D | 10 | Rp80.000.000 | |
| E | 6 | Rp90.000.000 | |

**Langkah:**
1. Hitung density setiap barang
2. Urutkan density tertinggi → terendah
3. Ambil sesuai kapasitas

| Urutan | Barang | Density | Berat | Ambil? | Total Berat |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |

**Total nilai maksimal:** Rp _______________

---

## B. DIVIDE & CONQUER (Soal 3-4)

### Soal 3 — Binary Search (10 menit)

Data terurut: [4, 9, 13, 18, 24, 29, 35, 42, 50, 57]
Indeks:      0  1   2   3   4   5   6   7   8   9

**Cari angka 35:**

| Langkah | Kiri | Kanan | Tengah | arr[tengah] | Aksi |
|---|---|---|---|---|---|
| 1 | 0 | 9 | 4 (24) | 24 | 35 > 24 → kiri = 5 |
| 2 | | | | | |
| 3 | | | | | |

Ditemukan di indeks: ____

**Cari angka 9:**

| Langkah | Kiri | Kanan | Tengah | arr[tengah] | Aksi |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |

Ditemukan di indeks: ____

### Soal 4 — Merge Sort (15 menit)

Urutkan data berikut dengan Merge Sort:

[54, 23, 11, 38, 47, 6, 29, 15]

Gambar diagram pohon **Divide** dan **Combine** di bawah ini!

```
Divide:
[54, 23, 11, 38, 47, 6, 29, 15]

...

Combine:
...
```

**Hasil akhir:** [____, ____, ____, ____, ____, ____, ____, ____]

---

## C. BACKTRACKING (Soal 5-6)

### Soal 5 — Permutasi dengan Batasan (15 menit)

Buat semua permutasi {A, B, C, D} dengan syarat: **A tidak boleh sebelum B**.

Gunakan Backtracking dengan pruning!

Pohon:
```
                    []
       ┌───────┬───────┼───────┐
      [A]     [B]     [C]     [D]
       |       |       |       |
      ...     ...     ...     ...
```

| Langkah | Pilih | Hasil Sementara | Valid? | Aksi |
|---|---|---|---|---|
| 1 | A | [A] | ✅ | Lanjut |
| 2a | A→B | [A,B] | ❌ A sebelum B! | **PRUNE** |
| 2b | A→C | [A,C] | | |
| ... | | | | |

**Permutasi valid:** ______ (tulis semua yang lolos)

### Soal 6 — Labirin (10 menit)

Cari jalur dari **S (Start)** ke **F (Finish)**. [X] = rintangan.

```
        Kolom 0    1    2    3
Baris 0   S    [ ]  [X]  [ ]
Baris 1  [X]   [ ]  [ ]  [X]
Baris 2  [ ]   [X]  [ ]  [ ]
Baris 3  [ ]   [ ]  [X]  [F]
```

| Langkah | Posisi | Arah | Aksi |
|---|---|---|---|
| 1 | (0,0) S | — | Start |
| 2 | | | |
| ... | | | |
| Akhir | (3,3) F | — | Finish! |

**Jalur:** _________________________________

---

**MGMP Informatika SMAN 6 Cimahi**
