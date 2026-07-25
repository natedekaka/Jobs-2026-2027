# ASESMEN – PERTEMUAN 9
## Divide and Conquer

Informatika – Fase F / Kelas XI – SMA Negeri 6 Cimahi

---

## Rubrik Penilaian

### A. Konsep D&C (Bobot 15%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Soal 1 (3 langkah) | Tidak diisi | 1 langkah | 2 langkah | 3 langkah + penjelasan |
| Soal 2 (pasangan) | 0–1 benar | 2 benar | 3 benar | 4 benar |

### B. Binary Search (Bobot 30%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| 34 | Tidak ditemukan | Langkah salah | Langkah benar, salah indeks | Ditemukan idx 6 |
| 7 | Tidak ditemukan | Langkah salah | Langkah benar, salah indeks | Ditemukan idx 1 |
| 50 | Tidak ditemukan | Langkah salah | Langkah benar, salah indeks | Ditemukan idx 8 |

### C. Merge Sort (Bobot 30%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Diagram divide | Tidak ada | Sebagian | Lengkap | Lengkap + rapi |
| Hasil akhir | Tidak urut | 2–4 benar | 6–7 benar | Semua benar [5,7,8,16,19,23,31,42] |

### D. Analisis Kompleksitas (Bobot 15%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Soal 5 (tabel) | Tidak diisi | 4 benar | 8 benar | 12+ benar |
| Soal 6 | Tidak diisi | 1 benar | 2 benar | 3 benar + faktor lipat |

### E. Tugas Rumah (Bobot 10%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Pseudocode Binary Search | Tidak ada | Struktur salah | Logika benar | Lengkap + komentar |

---

## Kunci Jawaban

### Soal 1 — 3 Langkah D&C
1. **Divide**: Pecah masalah jadi submasalah lebih kecil
2. **Conquer**: Selesaikan setiap submasalah (rekursif)
3. **Combine**: Gabungkan hasil submasalah

### Soal 2 — Pasangan
1=C (Binary Search = D&C cari tengah)
2=D (Merge Sort = D&C bagi-urut-gabung)
3=A (Bubble Sort = tukar tetangga)
4=B (Sequential Search = cek satu-satu)

### Soal 3 — Binary Search (n=10)

| Target | Langkah | Ditemukan |
|---|---|---|
| 34 | kiri=0, kanan=9, tgh=4(22) → 34>22 → kiri=5; tgh=7(41) → 34<41 → kanan=6; tgh=6(34) ✅ | idx 6 |
| 7 | kiri=0, kanan=9, tgh=4(22) → 7<22 → kanan=3; tgh=1(7) ✅ | idx 1 |
| 50 | kiri=0, kanan=9, tgh=4(22) → 50>22 → kiri=5; tgh=7(41) → 50>41 → kiri=8; tgh=8(50) ✅ | idx 8 |

### Soal 4 — Merge Sort

Hasil akhir: [5, 7, 8, 16, 19, 23, 31, 42]

Urutan merge:
1. [42] [16] → [16, 42]
2. [7] [23] → [7, 23]
3. [31] [5] → [5, 31]
4. [19] [8] → [8, 19]
5. [16, 42] [7, 23] → [7, 16, 23, 42]
6. [5, 31] [8, 19] → [5, 8, 19, 31]
7. [7, 16, 23, 42] [5, 8, 19, 31] → [5, 7, 8, 16, 19, 23, 31, 42]

### Soal 5 — Kompleksitas

| n | Sequential O(n) | Binary O(log n) | Bubble O(n²) | Merge O(n log n) |
|---|---|---|---|---|
| 10 | 10 | 4 | 100 | 40 |
| 100 | 100 | 7 | 10.000 | 700 |
| 1.000 | 1.000 | 10 | 1.000.000 | 10.000 |

### Soal 6 — Perbandingan
- Sequential Search: 1.000 langkah
- Binary Search: 10 langkah
- Binary Search 100× lebih cepat

---

**MGMP Informatika SMAN 6 Cimahi**
