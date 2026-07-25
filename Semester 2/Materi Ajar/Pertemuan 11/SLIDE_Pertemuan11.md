---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 11 — SEMESTER 2
## Latihan Soal Algoritma
### Informatika – Fase E / Kelas X
#### SMA Negeri 6 Cimahi

---

## Roadmap Sejauh Ini

| Pert | Materi |
|---|---|
| 1–3 | Array, Stack, Queue |
| 4–5 | Sequential & Binary Search |
| 6 | Bubble & Insertion Sort |
| 7 | **PTS** |
| 8–10 | Pseudocode, Flowchart, IF, FOR, WHILE |
| **11** | **Latihan Soal** |
| **12** | **Python!** 🚀 |

---

## Review Cepat

**Tanya jawab — angkat tangan!**

1. Beda Stack dan Queue?
2. Kapan pakai Binary Search?
3. Prinsip Bubble Sort?
4. Simbol decision di flowchart?
5. Kapan pakai FOR vs WHILE?
6. Output `FOR i←1 TO 3: OUTPUT i×i`?

---

## Jawaban Review

1. Stack **LIFO**, Queue **FIFO**
2. Data **terurut**
3. Bandingkan-tukar berpasangan → besar mengapung
4. **Belah ketupat (◇)**
5. FOR = **counter pasti**, WHILE = **kondisi**
6. **1, 4, 9**

---

# STASIUN BELAJAR

### Position Rotation — 5 Stasiun

| Stasiun | Materi |
|---|---|
| **A** | Stack & Queue |
| **B** | Searching |
| **C** | Sorting |
| **D** | Pseudocode & Flowchart |
| **E** | Perulangan |

> Setiap stasiun 8 menit, lalu rotasi!

---

## Stasiun A — Stack

`push(4), push(9), push(2), pop(), push(7), pop()`

| Operasi | Stack |
|---|---|
| push(4) | [4] |
| push(9) | [4, 9] |
| push(2) | [4, 9, 2] |
| pop() | [4, 9] |
| push(7) | [4, 9, 7] |
| pop() | [4, 9] |

> Sisa: **4, 9**

---

## Stasiun A — Queue

`enqueue(8), enqueue(3), dequeue(), enqueue(5), enqueue(2), dequeue()`

| Operasi | Queue |
|---|---|
| enqueue(8) | [8] |
| enqueue(3) | [8, 3] |
| dequeue() | [3] |
| enqueue(5) | [3, 5] |
| enqueue(2) | [3, 5, 2] |
| dequeue() | [5, 2] |

> Sisa: **5, 2**

---

## Stasiun B — Sequential Search

[12, 7, 25, 9, **18**, 3, 30, 14] — cari 18

| Langkah | Data | Cocok? |
|---|---|---|
| 1 | 12 | ❌ |
| 2 | 7 | ❌ |
| 3 | 25 | ❌ |
| 4 | 9 | ❌ |
| **5** | **18** | **✅** |

> **5 perbandingan**

---

## Stasiun B — Binary Search

[3, 7, 12, **15**, 20, 25, 30, 35, 42] — cari 15

| Langkah | low | mid | high | Data[mid] |
|---|---|---|---|---|
| 1 | 0 | 4 | 8 | 20 (terlalu besar) |
| 2 | 0 | 1 | 3 | 7 (terlalu kecil) |
| 3 | 2 | 2 | 3 | 12 (terlalu kecil) |
| 4 | 3 | 3 | 3 | **15 ✅** |

> **4 perbandingan** (Sequential butuh 4 juga karena 15 di posisi 3)

---

## Stasiun C — Bubble Sort

[35, 12, 8, 20, 5]

```
Pas 1: [12, 8, 20, 5, 35]
Pas 2: [8, 12, 5, 20, 35]
Pas 3: [8, 5, 12, 20, 35]
Pas 4: [5, 8, 12, 20, 35]
```

> **4 pas, 10 pertukaran**

---

## Stasiun C — Insertion Sort

[35, 12, 8, 20, 5]

```
Langkah 1: [35]
Langkah 2: [12, 35]
Langkah 3: [8, 12, 35]
Langkah 4: [8, 12, 20, 35]
Langkah 5: [5, 8, 12, 20, 35]
```

> Seperti **nyusun kartu**!

---

## Stasiun D — Pseudocode

Input 75:
```
≥ 92? ❌
≥ 83? ❌
≥ 75? ✅ → "C"
```

---

## Stasiun E — Perulangan

`FOR i←1 TO 6: IF i genap THEN total←total+i`

```
i=2 → total=2
i=4 → total=6
i=6 → total=12
```

> Output: **12**

---

## Koneksi ke Python 🐍

Pseudocode:
```
INPUT x
IF x > 0 THEN
    OUTPUT "Positif"
ENDIF
```

**Python:**
```python
x = int(input())
if x > 0:
    print("Positif")
```

> **Sangat mirip!** Pertemuan depan kita mulai Python!

---

## Preview Pertemuan 12

### Python — Variabel, Tipe Data, INPUT/OUTPUT, IF

> Semua yang sudah dipelajari di pseudocode → **tinggal translasi ke Python!**

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Latihan bukan membuatmu sempurna. Latihan membuatmu lebih baik."
