# SOAL LATIHAN — PERTEMUAN 11
## Review Algoritma (Struktur Data, Searching, Sorting, Pseudocode)

| Nama | ____________________ |
|---|---|
| Kelas | ____________________ |
| Kelompok | ____________________ |

---

### STASIUN A: STACK & QUEUE (2 soal — 8 menit)

**A1.** Stack mula-mula kosong. Lakukan operasi:
```
push(4), push(9), push(2), pop(), push(7), pop()
```

a. Gambarkan keadaan stack **setelah setiap operasi**!

| Operasi | Stack |
|---|---|
| push(4) | |
| push(9) | |
| push(2) | |
| pop() | |
| push(7) | |
| pop() | |

b. Data yang tersisa di akhir: _______________

**A2.** Queue mula-mula kosong. Lakukan operasi:
```
enqueue(8), enqueue(3), dequeue(), enqueue(5), enqueue(2), dequeue()
```

a. Gambarkan keadaan queue **setelah setiap operasi**!

| Operasi | Queue |
|---|---|
| enqueue(8) | |
| enqueue(3) | |
| dequeue() | |
| enqueue(5) | |
| enqueue(2) | |
| dequeue() | |

b. Data yang tersisa di akhir: _______________

---

### STASIUN B: SEARCHING (2 soal — 8 menit)

**B1. Sequential Search**

Array: [12, 7, 25, 9, 18, 3, 30, 14]. Cari angka **18**.

Tulis langkah-langkah pencarian (indeks, data, cocok?):

| Langkah | Indeks | Data | Cocok? |
|---|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |
| 4 | | | |
| 5 | | | |

Jumlah perbandingan: _______

**B2. Binary Search**

Array terurut: [3, 7, 12, 15, 20, 25, 30, 35, 42]. Cari angka **15**.

Tulis langkah-langkah (low, mid, high):

| Langkah | low | high | mid | Data[mid] | Arah |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |

Jumlah perbandingan: _______

---

### STASIUN C: SORTING (2 soal — 8 menit)

**C1. Bubble Sort**

Array: [35, 12, 8, 20, 5]. Urutkan ascending dengan bubble sort.

Tulis keadaan array **setiap akhir pas**:

| Pas | Array setelah pas |
|---|---|
| Awal | [35, 12, 8, 20, 5] |
| Pas 1 | |
| Pas 2 | |
| Pas 3 | |
| Pas 4 | |

Hasil akhir: ________________

**C2. Insertion Sort**

Array: [35, 12, 8, 20, 5]. Urutkan ascending dengan insertion sort.

Tulis keadaan array setiap langkah:

| Langkah | Ambil | Array |
|---|---|---|
| 1 | 35 | [35] |
| 2 | 12 | |
| 3 | 8 | |
| 4 | 20 | |
| 5 | 5 | |

Hasil akhir: ________________

---

### STASIUN D: PSEUDOCODE & FLOWCHART (2 soal — 8 menit)

**D1.** Baca pseudocode berikut. Apa output jika input = 75?

```
PROGRAM cek_nilai
    INPUT x
    IF x >= 92 THEN
        OUTPUT "A"
    ELSE
        IF x >= 83 THEN
            OUTPUT "B"
        ELSE
            IF x >= 75 THEN
                OUTPUT "C"
            ELSE
                OUTPUT "D"
            ENDIF
        ENDIF
    ENDIF
END
```

Jawab: _______________

**D2.** Gambar flowchart untuk algoritma berikut:

```
PROGRAM ganjil_genap
    INPUT x
    IF x MOD 2 = 0 THEN
        OUTPUT "Genap"
    ELSE
        OUTPUT "Ganjil"
    ENDIF
END
```

(Gambar di bawah ini)

---

### STASIUN E: PERULANGAN (2 soal — 8 menit)

**E1.** Baca pseudocode berikut. Apa outputnya?

```
PROGRAM deret
    total ← 0
    FOR i ← 1 TO 6
        IF i MOD 2 = 0 THEN
            total ← total + i
        ENDIF
    ENDFOR
    OUTPUT total
END
```

Jawab: _______________

**E2.** Tulis pseudocode WHILE untuk mencetak bilangan kelipatan 3 dari 3 sampai 30!

```
PROGRAM kelipatan_3

    _________________________________

    _________________________________

    _________________________________

    _________________________________

    _________________________________

    _________________________________

END
```

---

### BONUS (opsional)

Buat pseudocode untuk konversi suhu: input Celcius → output Fahrenheit (F = C × 9/5 + 32).

```
PROGRAM celcius_ke_fahrenheit

    _________________________________

    _________________________________

    _________________________________

    _________________________________

END
```

---

**MGMP Informatika SMAN 6 Cimahi**
