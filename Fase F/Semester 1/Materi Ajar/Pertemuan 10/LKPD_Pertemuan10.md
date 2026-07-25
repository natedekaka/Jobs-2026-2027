# LEMBAR KERJA PESERTA DIDIK (LKPD)
## Pertemuan 10 – Backtracking

| TP | BK, AP — Strategi Algoritmik |
|---|---|
| Nama | ____________________ |
| Kelas | ____________________ |

---

### A. KONSEP BACKTRACKING

**Soal 1:** Isi 5 langkah Backtracking!

| Langkah | Arti |
|---|---|
| 1. | |
| 2. | |
| 3. | |
| 4. | |
| 5. | |

**Soal 2:** Pasangkan!

| Konsep | Arti |
|---|---|
| 1. Pruning | A. Kembali ke state sebelumnya |
| 2. Backtrack | B. Memotong cabang yang pasti gagal |
| 3. Permutasi | C. Semua susunan yang mungkin |

Jawaban: 1=__, 2=__, 3=__

---

### B. LABIRIN

**Soal 3:** Cari jalur dari S ke F! [X] = rintangan.

```
        Kolom 0    1    2    3    4
Baris 0   S    [ ]  [ ]  [X]  [ ]
Baris 1  [X]   [ ]  [X]  [ ]  [ ]
Baris 2  [ ]   [ ]  [ ]  [ ]  [X]
Baris 3  [ ]   [X]  [X]  [ ]  [ ]
Baris 4  [ ]   [ ]  [ ]  [ ]  [F]
```

| Langkah | Posisi | Aksi | Keterangan |
|---|---|---|---|
| 1 | (0,0) S | Choose | Mulai |
| 2 | | | |
| ... | | | |
| Akhir | (4,4) F | Finish! | |

Tandai jalur di grid dengan panah!

---

### C. PERMUTASI {A, B, C, D}

**Soal 4:** Gambar pohon Backtracking permutasi {A, B, C, D} (kerjakan di kertas terpisah).

Jumlah permutasi: ___

---

### D. PERMUTASI DENGAN BATASAN

**Soal 5:** Permutasi {1, 2, 3} — syarat: **angka ganjil tidak boleh bersebelahan** (1 dan 3 ganjil).

| Langkah | Pilih | hasil sementara | Valid? | Aksi |
|---|---|---|---|---|
| 1 | 1 | [1] | ✅ | Lanjut |
| 2a | 1→2 | [1,2] | ✅ | Lanjut |
| 2b | 1→3 | [1,3] | ❌ 1&3 bersebelahan | **PRUNE** |
| ... | | | | |

**Solusi valid:** ________ dan ________

---

### E. REFLEKSI

| Pertanyaan | Jawaban |
|---|---|
| Beda Backtracking dengan Greedy? | |
| Kenapa Backtracking lambat? | |
| Apa gunanya pruning? | |
| Skala pemahaman (1–10) | / 10 |

---

### F. TUGAS RUMAH

Cari 1 contoh Backtracking dalam kehidupan sehari-hari!

Contoh: menyusun jadwal pelajaran, mengisi puzzle Sudoku, mencari rute perjalanan.

Tulis: masalah, solusi Backtracking-nya, apakah pakai pruning?

---

**MGMP Informatika SMAN 6 Cimahi**
