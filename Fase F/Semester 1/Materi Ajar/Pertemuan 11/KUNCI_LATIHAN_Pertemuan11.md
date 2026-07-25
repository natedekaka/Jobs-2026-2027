# KUNCI JAWABAN – SOAL LATIHAN PERTEMUAN 11
## Greedy, D&C, Backtracking – Fase F

---

## A. GREEDY

### Soal 1 — Penukaran Koin Rp23.400

| Langkah | Sisa Uang | Ambil Pecahan | Sisa Baru |
|---|---|---|---|
| 1 | Rp23.400 | Rp10.000 (2×) | Rp3.400 |
| 2 | Rp3.400 | Rp2.000 | Rp1.400 |
| 3 | Rp1.400 | Rp1.000 | Rp400 |
| 4 | Rp400 | Rp200 (2×) | Rp0 |

**Jumlah minimal: 6 lembar/koin** (2×10.000 + 2.000 + 1.000 + 2×200)

### Soal 2 — Fractional Knapsack 40 kg

**Density:**
- A: 120jt/8 = **Rp15jt/kg**
- B: 150jt/15 = **Rp10jt/kg**
- C: 180jt/12 = **Rp15jt/kg**
- D: 80jt/10 = **Rp8jt/kg**
- E: 90jt/6 = **Rp15jt/kg**

**Urutan density:** C (15jt), A (15jt), E (15jt), B (10jt), D (8jt)

| Urutan | Barang | Density | Berat | Ambil? | Total Berat |
|---|---|---|---|---|---|
| 1 | C | 15jt | 12 | 12 kg (ambil semua) | 12 |
| 2 | A | 15jt | 8 | 8 kg (ambil semua) | 20 |
| 3 | E | 15jt | 6 | 6 kg (ambil semua) | 26 |
| 4 | B | 10jt | 15 | 14 kg (sisa kapasitas) | 40 |
| 5 | D | 8jt | 10 | 0 (penuh) | 40 |

**Total nilai:**
C: 12 × 15jt = Rp180jt
A: 8 × 15jt = Rp120jt
E: 6 × 15jt = Rp90jt
B: 14 × 10jt = Rp140jt
**Total = Rp530jt**

---

## B. DIVIDE & CONQUER

### Soal 3 — Binary Search

**Cari 35:**
| Langkah | Kiri | Kanan | Tengah | Nilai | Aksi |
|---|---|---|---|---|---|
| 1 | 0 | 9 | 4 | 24 | 35 > 24 → kiri = 5 |
| 2 | 5 | 9 | 7 | 42 | 35 < 42 → kanan = 6 |
| 3 | 5 | 6 | 5 | 29 | 35 > 29 → kiri = 6 |
| 4 | 6 | 6 | 6 | **35** | **Ditemukan!** |

Indeks: **6**

**Cari 9:**
| Langkah | Kiri | Kanan | Tengah | Nilai | Aksi |
|---|---|---|---|---|---|
| 1 | 0 | 9 | 4 | 24 | 9 < 24 → kanan = 3 |
| 2 | 0 | 3 | 1 | **9** | **Ditemukan!** |

Indeks: **1**

### Soal 4 — Merge Sort

**Divide:**
```
[54, 23, 11, 38, 47, 6, 29, 15]
[54, 23, 11, 38]    [47, 6, 29, 15]
[54, 23]  [11, 38]  [47, 6]  [29, 15]
[54] [23] [11] [38] [47] [6] [29] [15]
```

**Combine:**
```
[23, 54]  [11, 38]  [6, 47]  [15, 29]
[11, 23, 38, 54]    [6, 15, 29, 47]
[6, 11, 15, 23, 29, 38, 47, 54]
```

**Hasil akhir:** [6, 11, 15, 23, 29, 38, 47, 54]

---

## C. BACKTRACKING

### Soal 5 — Permutasi {A, B, C, D} — A tidak boleh sebelum B

Pohon Backtracking dengan pruning:

```
                    Root []
       ┌──────────────┬──────────────┼──────────────┐
      [A]            [B]            [C]            [D]
       |              |              |              |
  A sebelum B?   B tanpa A    [B,C] [B,D]    [C,A] [C,B]
  Maka A hanya   belum aturan  |  |    |  |    |  |   |  |
  boleh muncul   → semua 6    [B,C,A]...[D,C,B]...
  setelah B!     permutasi    (cek A sebelum B?)
                 dari {B,C,D}
                 valid: 6
```

Semua permutasi dari {A,B,C,D} = 24. Syarat A tidak sebelum B.

Permutasi valid (A muncul setelah B):
- B harus sebelum A dalam urutan
- Dari 24 permutasi, setengahnya (12) memiliki A sebelum B, setengahnya (12) memiliki B sebelum A

**Permutasi valid (12):**
B, A, C, D — B, A, D, C — B, C, A, D — B, C, D, A — B, D, A, C — B, D, C, A
C, B, A, D — C, B, D, A — C, D, B, A — D, B, A, C — D, B, C, A — D, C, B, A

### Soal 6 — Labirin 4×4

```
        Kolom 0    1    2    3
Baris 0   S     .   [X]   .
Baris 1  [X]    .    .   [X]
Baris 2   .    [X]   .    .
Baris 3   .     .   [X]   F
```

**Jalur:** (0,0)→(0,1)→(1,1)→(2,1) → backtrack karena (2,1) punya (2,0) dan (1,1) sudah visited, (3,1) bisa tp coba dulu (2,2)...

Wait, let me trace:
(0,0) S
↓ (0,1) ✅
↓ (1,1) ✅
↓ (2,1) — [X] ❌ → backtrack to (1,1)
(1,1) → (1,2) ✅
↓ (2,2) ✅
↓ (3,2) — [X] ❌ → backtrack to (2,2)
(2,2) → (2,3) ✅
↓ (3,3) F ✅

**Jalur:** (0,0)→(0,1)→(1,1)→(1,2)→(2,2)→(2,3)→(3,3) F ✅

Atau alternatif: (0,0)→(0,1)→(1,1)→(1,2)→(2,2)→(2,3)→(3,3)

Let me also check (2,0):
(0,0)→(0,1)→(1,1)→(1,2)→... → what about going (0,0)→(0,1)→(1,1)→ no wait, (1,1) can't go to (2,1) since it's [X]. So from (1,1): (0,1) visited, (2,1)=[X] ❌, (1,2)✅ → that's the only option.

Actually let me re-check (2,1) — looking at the grid: Baris 2, Kolom 1 is [X].

From (0,0): right → (0,1), down → (1,0)=[X] ❌
From (0,1): right → (0,2)=[X] ❌, down → (1,1)✅
From (1,1): down → (2,1)=[X] ❌, right → (1,2)✅, left → (1,0)=[X] ❌, up → (0,1) visited
From (1,2): down → (2,2)✅, right → (1,3)=[X] ❌, left → (1,1) visited
From (2,2): down → (3,2)=[X] ❌, right → (2,3)✅, left → (2,1)=[X] ❌, up → (1,2) visited
From (2,3): down → (3,3)=F ✅

Jalur: (0,0)→(0,1)→(1,1)→(1,2)→(2,2)→(2,3)→(3,3)F

That's correct!

---

## Rubrik Penilaian

| Soal | 1 (25%) | 2 (50%) | 3 (75%) | 4 (100%) |
|---|---|---|---|---|
| 1 (koin) | Tidak diisi | Langkah sebagian | 6 lembar | 6 + langkah lengkap |
| 2 (knapsack) | Tidak diisi | Density benar | Urutan + ambil benar | Total Rp530jt |
| 3 (binary) | Tidak diisi | 1 angka benar | 2 angka benar | 2 + langkah |
| 4 (merge sort) | Tidak diisi | Divide saja | Sebagian combine | [6,11,15,23,29,38,47,54] |
| 5 (permutasi) | Tidak diisi | Pruning sebagian | 6 permutasi | 12 permutasi + pohon |
| 6 (labirin) | Tidak diisi | Jalur sebagian | Jalur benar | Jalur + backtrack |

---

**MGMP Informatika SMAN 6 Cimahi**
