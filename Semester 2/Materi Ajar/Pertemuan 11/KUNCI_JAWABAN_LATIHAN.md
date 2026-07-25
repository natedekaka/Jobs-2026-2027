# KUNCI JAWABAN — SOAL LATIHAN PERTEMUAN 11

---

## STASIUN A: STACK & QUEUE

### A1. Stack
| Operasi | Stack |
|---|---|
| `push(4)` | [4] |
| `push(9)` | [4, 9] |
| `push(2)` | [4, 9, 2] |
| `pop()` | [4, 9] → 2 keluar |
| `push(7)` | [4, 9, 7] |
| `pop()` | [4, 9] → 7 keluar |

b. Data tersisa: **4 dan 9**

### A2. Queue
| Operasi | Queue |
|---|---|
| `enqueue(8)` | [8] |
| `enqueue(3)` | [8, 3] |
| `dequeue()` | [3] → 8 keluar |
| `enqueue(5)` | [3, 5] |
| `enqueue(2)` | [3, 5, 2] |
| `dequeue()` | [5, 2] → 3 keluar |

b. Data tersisa: **5 dan 2**

---

## STASIUN B: SEARCHING

### B1. Sequential Search — cari 18
Array: [12, 7, 25, 9, 18, 3, 30, 14]

| Langkah | Indeks | Data | Cocok? |
|---|---|---|---|
| 1 | 0 | 12 | ❌ |
| 2 | 1 | 7 | ❌ |
| 3 | 2 | 25 | ❌ |
| 4 | 3 | 9 | ❌ |
| 5 | 4 | 18 | ✅ |

**Jumlah perbandingan: 5**

### B2. Binary Search — cari 15
Array: [3, 7, 12, 15, 20, 25, 30, 35, 42] (indeks 0–8)

| Langkah | low | high | mid | Data[mid] | Arah |
|---|---|---|---|---|---|
| 1 | 0 | 8 | 4 | 20 | 15 < 20 → kiri (high=3) |
| 2 | 0 | 3 | 1 | 7 | 15 > 7 → kanan (low=2) |
| 3 | 2 | 3 | 2 | 12 | 15 > 12 → kanan (low=3) |
| 4 | 3 | 3 | 3 | 15 | ✅ Ditemukan! |

**Jumlah perbandingan: 4**

---

## STASIUN C: SORTING

### C1. Bubble Sort
Array: [35, 12, 8, 20, 5]

| Pas | Array setelah pas |
|---|---|
| Awal | [35, 12, 8, 20, 5] |
| Pas 1 | 35>12→T, 35>8→T, 35>20→T, 35>5→T → [12, 8, 20, 5, **35**] |
| Pas 2 | 12>8→T, 12>20→F, 20>5→T → [8, 12, 5, **20**, 35] |
| Pas 3 | 8>12→F, 12>5→T → [8, 5, **12**, 20, 35] |
| Pas 4 | 8>5→T → [**5**, 8, 12, 20, 35] |

**Hasil akhir:** [5, 8, 12, 20, 35]

### C2. Insertion Sort
Array: [35, 12, 8, 20, 5]

| Langkah | Ambil | Array |
|---|---|---|
| 1 | 35 | [35] |
| 2 | 12 | [12, 35] — 12 < 35, sisip di depan |
| 3 | 8 | [8, 12, 35] — 8 < 12, sisip di depan |
| 4 | 20 | [8, 12, 20, 35] — 20 < 35, sisip di depan 35 |
| 5 | 5 | [5, 8, 12, 20, 35] — 5 < 8, sisip di depan |

**Hasil akhir:** [5, 8, 12, 20, 35]

---

## STASIUN D: PSEUDOCODE & FLOWCHART

### D1. Input 75
75 >= 92? ❌ → 75 >= 83? ❌ → 75 >= 75? ✅ → OUTPUT "C"

**Jawab: C**

### D2. Flowchart Ganjil/Genap
```
   ┌─────────────┐
   │    Start    │
   └──────┬──────┘
          ▼
   ┌─────────────┐
   │  INPUT x    │
   └──────┬──────┘
          ▼
      ┌──────┐
      │x%2=0?│── Ya ──→ ┌──────────┐
      └──┬───┘          │ OUTPUT   │
         │ Tidak        │ "Genap"  │
         ▼              └────┬─────┘
   ┌──────────┐              │
   │ OUTPUT   │              │
   │ "Ganjil" │              │
   └────┬─────┘              │
        │◄───────────────────┘
        ▼
   ┌─────────────┐
   │    End      │
   └─────────────┘
```

---

## STASIUN E: PERULANGAN

### E1. Output deret genap 1..6
```
FOR i ← 1 TO 6
  IF i MOD 2 = 0 THEN total ← total + i
```
i=2 → +2, i=4 → +4, i=6 → +6
total = 2+4+6 = **12**

### E2. Kelipatan 3 dari 3 sampai 30
```
PROGRAM kelipatan_3
    i ← 3
    WHILE i <= 30
        OUTPUT i
        i ← i + 3
    ENDWHILE
END
```

Atau dengan FOR:
```
PROGRAM kelipatan_3
    FOR i ← 3 TO 30 STEP 3
        OUTPUT i
    ENDFOR
END
```

---

## BONUS: Celcius ke Fahrenheit

```
PROGRAM celcius_ke_fahrenheit
    INPUT celcius
    fahrenheit ← celcius × 9/5 + 32
    OUTPUT fahrenheit
END
```

Contoh: C=100 → F = 100×9/5+32 = 212

---

**MGMP Informatika SMAN 6 Cimahi**
