---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 10 — FASE F
## Strategi Algoritmik — Backtracking
### Informatika – Fase F / Kelas XI
#### SMA Negeri 6 Cimahi

---

## Review

| Pert | Strategi |
|---|---|
| 8 | **Greedy** — ambil terbaik sekarang |
| 9 | **D&C** — pecah → selesaikan → gabung |
| 10 | **Backtracking** — coba → gagal → mundur |

---

## Apersepsi

"Main labirin — mentok? Balik lagi ke persimpangan, coba jalan lain!"

> Itulah **Backtracking**!

---

# TUJUAN PEMBELAJARAN

1. ✅ Prinsip Backtracking
2. ✅ Maze / Labirin
3. ✅ Permutasi angka
4. ✅ Pruning

---

## 5 Langkah Backtracking

```
CHOOSE → EXPLORE → CHECK
                      │
              ┌───────┴───────┐
              ▼               ▼
           BERHASIL        GAGAL
              │               │
              ▼               ▼
           SOLUSI        BACKTRACK
                            │
                            ▼
                        CHOOSE LAGI
                 (dengan opsi berbeda)
```

---

## Analogi: Labirin

| Langkah | Labirin |
|---|---|
| **Choose** | Pilih jalur kiri di persimpangan |
| **Explore** | Jalan terus |
| **Check** | Sampai ujung? |
| **Backtrack** | Buntu → balik |
| **Prune** | "Jalur itu pasti buntu, skip!" |

---

## Labirin 5×5

```
     0   1   2   3   4
 0   S   .   .  [X]  .
 1  [X]  .  [X]  .   .
 2   .   .   .   .  [X]
 3   .  [X] [X]  .   .
 4   .   .   .   .   F
```

> S = Start, F = Finish, [X] = rintangan

---

## Pohon Labirin

```
S(0,0)
├── (0,1)
│   ├── (0,2) → buntu (0,3=[X], 1,2=[X])
│   │   ← BACKTRACK!
│   └── (1,1) ✅ → ...
└── (1,0) [X] → PRUNE!
```

---

## Aktivitas 1: Labirin

### Individu — 15 menit

Cari jalur S → F!

Tandai:
- ✅ Jalur yang dipilih
- 🔄 Backtrack
- ✂️ Pruning

---

## Permutasi {1, 2, 3}

```
                  []
        ┌─────────┼─────────┐
       [1]       [2]       [3]
    ┌───┼───┐ ┌───┼───┐ ┌───┼───┐
 [1,2] [1,3] [2,1] [2,3] [3,1] [3,2]
   │     │     │     │     │     │
[1,2,3] [1,3,2] [2,1,3] [2,3,1] [3,1,2] [3,2,1]
```

Jumlah: 3! = **6 permutasi**

---

## Pseudocode Permutasi

```
PROCEDURE Permutasi(elemen, terpakai, hasil)
    IF panjang(hasil) = n THEN
        simpan hasil // solusi!
        RETURN
    ENDIF
    
    FOR i ← 1 TO n DO
        IF NOT terpakai[i] THEN
            CHOOSE:   tandai terpakai
            EXPLORE:  panggil rekursif
            BACKTRACK: hapus tandai
        ENDIF
    ENDFOR
END
```

---

## Pruning

**Prune** = potong cabang yang pasti gagal

### Permutasi {1,2,3} — syarat: ganjil tidak bersebelahan

```
[1]
├── [1,2]
│   └── [1,2,3] ✅ (1 dan 3 dipisah 2)
└── [1,3] ❌ → PRUNE! (1&3 ganjil bersebelahan)
[2] ...
[3]
├── [3,2]
│   └── [3,2,1] ✅
└── [3,1] ❌ → PRUNE!
```

**Hanya 2 solusi:** [1,2,3] dan [3,2,1]

---

## Aktivitas 2: Permutasi {A,B,C,D}

### Berpasangan — 10 menit

Gambar pohon Backtracking!

> 4! = 24 permutasi

---

## Aktivitas 3: Permutasi dengan Pruning

### 10 menit

{1, 2, 3} — syarat: **ganjil tidak bersebelahan**

Gunakan pruning!

> Berapa solusi valid?

---

## Perbandingan 3 Strategi

| Aspek | Greedy | D&C | Backtracking |
|---|---|---|---|
| Cara | Ambil terbaik | Pecah-gabung | Coba-mundur |
| Optimal? | ❌ | ✅ | ✅ |
| Kecepatan | Cepat | Sedang | **Lambat** |
| Kompleksitas | O(n log n) | O(n log n) | **O(n!)** |

> Backtracking = pasti optimal, tapi lambat!

---

## Rangkuman

| Konsep | Inti |
|---|---|
| **Backtracking** | Coba sistematis, mundur jika gagal |
| **Choose → Explore → Backtrack** | 3 langkah utama |
| **Pruning** | Potong cabang mustahil |
| **Permutasi** | n! kemungkinan |
| **Kompleksitas** | O(n!) — untuk n kecil |

---

## Tugas Rumah

Cari 1 contoh Backtracking dalam kehidupan sehari-hari!

> Contoh: Sudoku, jadwal, rute perjalanan

---

## Pertemuan Depan

### Latihan Soal Strategi Algoritmik
> Greedy, D&C, Backtracking — review + soal!

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Backtracking: yang penting mau mundur dan coba lagi."
