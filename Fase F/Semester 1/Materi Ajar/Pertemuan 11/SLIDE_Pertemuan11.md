---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 11 — FASE F
## Latihan Soal Strategi Algoritmik
### Informatika – Fase F / Kelas XI
#### SMA Negeri 6 Cimahi

---

## Review Singkat

| Pert | Strategi | Prinsip |
|---|---|---|
| 8 | **Greedy** | Ambil terbaik saat ini |
| 9 | **D&C** | Pecah → selesaikan → gabung |
| 10 | **Backtracking** | Coba → gagal → mundur |

> Hari ini: **Latihan Soal!**

---

## Apersepsi

"Manakah strategi yang tepat untuk masalah tertentu?"

> Mari uji dengan soal-soal!

---

## 1. Greedy — Review

**Prinsip:** Ambil pilihan terbaik lokal → harapan global optimal

**Contoh:** Penukaran koin, Fractional Knapsack

**⚠️ Gagal:** Pecahan 1,3,4 → tukar 6
- Greedy: 4+1+1 = 3 koin
- Optimal: 3+3 = 2 koin ✨

---

## 2. D&C — Review

**3 Langkah:**
```
Divide → Conquer → Combine
(Pecah)  (Selesaikan) (Gabung)
```

**Contoh:**
- Binary Search — O(log n)
- Merge Sort — O(n log n)

---

## 3. Backtracking — Review

**5 Langkah:**
```
Choose → Explore → Check
              ↓
       Backtrack ← ❌ Gagal
              ↓
         Prune ✂️
```

**Contoh:** Maze, Permutasi, Sudoku
**⚠️ Lambat:** O(n!) — hanya untuk n kecil

---

## Alokasi Waktu

| Bagian | Waktu |
|---|---|
| Review singkat | 50 menit |
| Soal Greedy (1-2) | 25 menit |
| Soal D&C (3-4) | 25 menit |
| Soal Backtracking (5-6) | 25 menit |
| Bahas bersama | 20 menit |
| Refleksi | 15 menit |

> Kerjakan mandiri dulu, baru diskusi!

---

## Soal 1 — Penukaran Koin

Pecahan: 10.000, 5.000, 2.000, 1.000, 500, 200, 100

**Tukar Rp23.400 dengan koin minimal!**

| Sisa | Ambil | Sisa Baru |
|---|---|---|
| 23.400 | ? | ... |

> Berapa lembar minimal?

---

## Soal 2 — Fractional Knapsack

Tas 40 kg. Cari nilai maksimal!

| Barang | Berat | Harga Total |
|---|---|---|
| A | 8 kg | Rp120jt |
| B | 15 kg | Rp150jt |
| C | 12 kg | Rp180jt |
| D | 10 kg | Rp80jt |
| E | 6 kg | Rp90jt |

> Hitung density, urutkan, ambil!

---

## Soal 3 — Binary Search

Data: [4, 9, 13, 18, 24, 29, 35, 42, 50, 57]

**Cari: 35 dan 9**

| Langkah | Kiri | Kanan | Tengah | arr[tengah] | Aksi |
|---|---|---|---|---|---|
| 1 | 0 | 9 | 4 | 24 | 35 > 24 → kiri=5 |
| ... | | | | | |

> Berapa langkah?

---

## Soal 4 — Merge Sort

**Urutkan:** [54, 23, 11, 38, 47, 6, 29, 15]

Gambar pohon divide & combine!

> Hasil akhir: [?, ?, ?, ?, ?, ?, ?, ?]

---

## Soal 5 — Permutasi Backtracking

**{A, B, C, D} — Syarat: A tidak boleh sebelum B**

Gunakan pruning!

> Berapa permutasi valid?

---

## Soal 6 — Labirin

```
     0   1   2   3
 0   S   .  [X]  .
 1  [X]  .   .  [X]
 2   .  [X]  .   .
 3   .   .  [X]  F
```

> Cari jalur S → F!

---

## Bahas Bersama

### 20 menit

Tulis jawaban di papan tulis!

> Soal mana yang paling sulit?
> Strategi mana yang paling mudah?

---

## Refleksi

| Pertanyaan | Jawaban |
|---|---|
| Strategi paling mudah? | |
| Strategi paling sulit? | |
| Kapan pakai Greedy? | |
| Kapan pakai Backtracking? | |

---

## Rangkuman

| Strategi | Kecepatan | Optimal? | Cocok untuk |
|---|---|---|---|
| **Greedy** | Cepat | ❌ Kadang | Koin, Knapsack pecahan |
| **D&C** | Sedang | ✅ Ya | Sorting, Searching |
| **Backtracking** | Lambat | ✅ Ya | Maze, Permutasi, n kecil |

---

## Pertemuan Depan

### Algoritma Dijkstra & Graph
> Mencari jalur terpendek!

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Latihan membuat sempurna — practice makes perfect!"
