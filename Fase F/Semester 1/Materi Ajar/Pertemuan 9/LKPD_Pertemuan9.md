# LEMBAR KERJA PESERTA DIDIK (LKPD)
## Pertemuan 9 – Divide and Conquer

| TP | BK, AP — Strategi Algoritmik |
|---|---|
| Nama | ____________________ |
| Kelas | ____________________ |

---

### A. 3 LANGKAH D&C

**Soal 1:** Isi 3 langkah Divide and Conquer!

| Langkah | Arti |
|---|---|
| 1. | |
| 2. | |
| 3. | |

**Soal 2:** Pasangkan algoritma dengan strateginya!

| Algoritma | Strategi |
|---|---|
| 1. Binary Search | A. Iteratif — tukar tetangga |
| 2. Merge Sort | B. Linear — cek satu-satu |
| 3. Bubble Sort | C. D&C — bagi, cari tengah |
| 4. Sequential Search | D. D&C — bagi, urut, gabung |

Jawaban: 1=__, 2=__, 3=__, 4=__

---

### B. BINARY SEARCH

**Soal 3:** Cari angka berikut dalam array dengan Binary Search!

Data: [3, 7, 11, 15, 22, 28, 34, 41, 50, 56]
Indeks:  0  1   2   3   4   5   6   7   8   9

| Target | Langkah (kiri, kanan, tengah) | Ditemukan di indeks? |
|---|---|---|
| 34 | | |
| 7 | | |
| 50 | | |

---

### C. MERGE SORT

**Soal 4:** Urutkan data berikut menggunakan Merge Sort!

Data: [42, 16, 7, 23, 31, 5, 19, 8]

Gambar diagram pohon divide → conquer → combine!

```
                        [42, 16, 7, 23, 31, 5, 19, 8]
                      
                       ... (gambar di sini)
                      
Hasil akhir: [____, ____, ____, ____, ____, ____, ____, ____]
```

---

### D. ANALISIS KOMPLEKSITAS

**Soal 5:** Hitung perkiraan jumlah langkah!

| n | Sequential O(n) | Binary O(log n) | Bubble O(n²) | Merge O(n log n) |
|---|---|---|---|---|
| 10 | | | | |
| 100 | | | | |
| 1.000 | | | | |

Rumus: log₂(n) — perkiraan:
- log₂(10) ≈ 4
- log₂(100) ≈ 7
- log₂(1.000) ≈ 10

**Soal 6:** Mana yang lebih cepat untuk 1.000 data?

- Sequential Search: ____ langkah
- Binary Search: ____ langkah
- Binary Search lebih cepat ____× lipat

---

### E. REFLEKSI

| Pertanyaan | Jawaban |
|---|---|
| Perbedaan Greedy dan D&C? | |
| Kenapa Binary Search butuh data terurut? | |
| Kesulitan saat Merge Sort manual? | |
| Skala pemahaman (1–10) | / 10 |

---

### F. TUGAS RUMAH

Tulis **pseudocode Binary Search** lengkap dengan parameter array, target, dan return indeks!

---

**MGMP Informatika SMAN 6 Cimahi**
