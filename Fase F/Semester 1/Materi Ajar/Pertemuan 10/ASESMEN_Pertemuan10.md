# ASESMEN – PERTEMUAN 10
## Backtracking

Informatika – Fase F / Kelas XI – SMA Negeri 6 Cimahi

---

## Rubrik Penilaian

### A. Konsep Backtracking (Bobot 15%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Soal 1 (5 langkah) | 0–1 benar | 2–3 benar | 4 benar | 5 benar + penjelasan |
| Soal 2 (pasangan) | 0 benar | 1 benar | 2 benar | 3 benar |

### B. Labirin (Bobot 30%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Jalur ditemukan | Tidak | Sampai, tapi salah | Jalur benar | Jalur benar + tandai backtrack |
| Tabel langkah | Tidak ada | Sebagian | Lengkap | Lengkap + pruning |

### C. Permutasi {A,B,C,D} (Bobot 20%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Jumlah permutasi | Salah | — | — | 24 |
| Pohon | Tidak ada | Sebagian | Hampir lengkap | Lengkap semua cabang |

### D. Permutasi dengan Batasan (Bobot 20%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Pruning | Tidak ada pruning | 1 prune | Semua prune | Prune + 2 solusi valid |
| Solusi | 0 | 1 (hanya [1,2,3]) | 2 ([1,2,3] & [3,2,1]) | 2 + penjelasan |

### E. Refleksi & Tugas (Bobot 15%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Refleksi | Tidak diisi | 1–2 jawaban | 3 jawaban | 3 + mendalam |
| Tugas rumah | Tidak ada | Contoh ada, analisis kurang | Contoh + analisis | Contoh + analisis + pruning |

---

## Kunci Jawaban

### Soal 1 — 5 Langkah Backtracking
1. **Choose**: Pilih satu opsi
2. **Explore**: Coba opsi tersebut
3. **Check**: Apakah menuju solusi?
4. **Backtrack**: Mundur jika gagal
5. **Prune**: Potong cabang yang pasti gagal

### Soal 2 — Pasangan
1=B (Pruning = potong cabang)
2=A (Backtrack = mundur)
3=C (Permutasi = semua susunan)

### Soal 3 — Labirin

Jalur:
S(0,0)→(0,1)→(1,1)→(2,1)→(2,0)→(3,0)→(4,0)→(4,1)→(4,2)→(4,3)→(4,4)→F

**Backtrack terjadi di:**
- (0,2) → tidak bisa ke mana-mana (atas S sudah, kanan [X] di 0,3, bawah [X] di 1,2) → backtrack ke (0,1)
- (2,2) → bisa lanjut ke (2,3) → ...

Jalur final: (0,0)→(0,1)→(1,1)→(2,1)→(2,0)→(3,0)→(4,0)→(4,1)→(4,2)→(4,3)→(4,4)→(3,4)→F

### Soal 4 — Permutasi {A,B,C,D}
Jumlah: 4! = **24 permutasi**

### Soal 5 — Permutasi {1,2,3} — ganjil tidak bersebelahan

| Langkah | Pilih | Hasil | Valid? | Aksi |
|---|---|---|---|---|
| 1 | 1 | [1] | ✅ | Lanjut |
| 2a | 1→2 | [1,2] | ✅ | Lanjut |
| 3a | 1→2→3 | [1,2,3] | ✅ (1&3 dipisah 2) | Solusi |
| 2b | 1→3 | [1,3] | ❌ bersebelahan | PRUNE |
| 1c | 2 | [2] | ✅ | Lanjut |
| 2c | 2→1 | [2,1] | ✅ | Lanjut |
| 3c | 2→1→3 | [2,1,3] | ❌ 1&3 bersebelahan | PRUNE |
| 2d | 2→3 | [2,3] | ✅ | Lanjut |
| 3d | 2→3→1 | [2,3,1] | ❌ 3&1 bersebelahan | PRUNE |
| 1e | 3 | [3] | ✅ | Lanjut |
| 2e | 3→1 | [3,1] | ❌ bersebelahan | PRUNE |
| 2f | 3→2 | [3,2] | ✅ | Lanjut |
| 3f | 3→2→1 | [3,2,1] | ✅ (3&1 dipisah 2) | Solusi |

**Solusi valid:** [1, 2, 3] dan [3, 2, 1]

---

**MGMP Informatika SMAN 6 Cimahi**
