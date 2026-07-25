---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 7 — SEMESTER 2
## PTS — Penilaian Tengah Semester
### Informatika – Fase E / Kelas X
#### SMA Negeri 6 Cimahi

---

## Aturan Ujian

| | |
|---|---|
| **Waktu** | 70 menit total |
| **PG** | 20 soal — 40 menit |
| **Esai** | 5 soal — 30 menit |
| **Nilai** | PG 60 + Esai 40 = **100** |

---

## Materi Ujian

| Pert | Materi | TP |
|---|---|---|
| 1 | **Array** | BK 1.1 |
| 2 | **Stack** | BK 1.1 |
| 3 | **Queue** | BK 1.1 |
| 4 | **Sequential Search** | BK 1.3 |
| 5 | **Binary Search** | BK 1.3 |
| 6 | **Bubble & Insertion Sort** | BK 1.3 |

---

## Ingat!

| Topik | Inti |
|---|---|
| Array | Indeks mulai **0**, akses acak |
| Stack | **LIFO** — push/pop |
| Queue | **FIFO** — enqueue/dequeue |
| Sequential | Cek satu per satu — **O(n)** |
| Binary | Data **terurut** — **O(log n)** |
| Bubble | Tukar pasangan — naik ke akhir |
| Insertion | Sisip ke posisi tepat |

---

## Review — Array

```python
A = [10, 20, 30, 40, 50]
```

- Indeks: `0, 1, 2, 3, 4`
- `A[2]` = **30**
- Array 2D: `B[2][3]`

---

## Review — Stack (LIFO)

```
push(5) → [5]
push(3) → [5, 3]
pop()   → [5]     (3 keluar)
push(7) → [5, 7]
```

> Seperti tumpukan piring!

---

## Review — Queue (FIFO)

```
enqueue(2) → [2]
enqueue(4) → [2, 4]
dequeue()  → [4]      (2 keluar)
enqueue(6) → [4, 6]
```

> Seperti antrean kasir!

---

## Review — Sequential Search

[15, 8, 23, 42, 10, 31, 5, 18]

Mencari **31**
> 15, 8, 23, 42, 10, **31** ✅ — 6 perbandingan

---

## Review — Binary Search

Untuk data **TERURUT**!

[3, 7, 10, 15, 20, 25, 30, 35, 42, 50]

Mencari **25**: `mid = 4` (20) → kanan → `mid = 7` (35) → kiri → `mid = 5` (**25** ✅)

Hanya **3 langkah**! (Sequential butuh 6)

---

## Review — Bubble Sort

[42, 15, 8, 23, 10]

```
Pas 1: [15, 8, 23, 10, 42]  → 42 mengapung
Pas 2: [8, 15, 10, 23, 42]  → 23 mengapung
Pas 3: [8, 10, 15, 23, 42]  → urut!
```
4 pas, 10 pertukaran

---

## Review — Insertion Sort

[42, 15, 8, 23, 10]

```
Ambil 42 → [42]
Ambil 15 → [15, 42]
Ambil 8  → [8, 15, 42]
Ambil 23 → [8, 15, 23, 42]
Ambil 10 → [8, 10, 15, 23, 42]
```
Lebih efisien untuk data hampir urut

---

## Kerjakan dengan Percaya Diri!

1. Baca soal dengan teliti
2. Dahulukan yang mudah
3. Untuk esai: tulis **langkah-langkahnya**
4. Cek kembali sebelum kumpul

> **Semoga Sukses! 🎯**

---

## Setelah PTS

| Pert | Materi |
|---|---|
| **8** | **Pseudocode & Flowchart** |
| 9 | Input/Output & Kondisi |
| 10 | Perulangan |
| 11 | Latihan Soal Algoritma |

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi
