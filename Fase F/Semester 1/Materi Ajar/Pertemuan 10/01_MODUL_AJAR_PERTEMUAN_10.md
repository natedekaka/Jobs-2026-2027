# MODUL AJAR INFORMATIKA – FASE F (KELAS XI)

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | F / XI |
| **Semester** | 1 (Ganjil) |
| **Pertemuan ke-** | 10 |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | SMA Negeri 6 Cimahi |
| **Materi Esensial** | Strategi Algoritmik |

---

## Tujuan Pembelajaran

| TP | IKTP |
|---|---|
| **BK, AP:** Memahami algoritma Backtracking | 10.1 Menjelaskan prinsip Backtracking (coba → gagal → mundur) |
| | 10.2 Menyelesaikan maze/labirin dengan Backtracking |
| | 10.3 Menyelesaikan permutasi angka dengan Backtracking |
| | 10.4 Menerapkan pruning untuk memotong cabang yang mustahil |
| | 10.5 Menyelesaikan puzzle N-Queens mini (4×4) dengan Backtracking |

---

## Langkah Pembelajaran

### Pembukaan (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 3 menit |
| 2. **Review**: "Pert 8: Greedy (ambil terbaik). Pert 9: D&C (pecah masalah). Hari ini: **Backtracking** — coba-coba, kalau salah mundur!" | 5 menit |
| 3. **Apersepsi**: "Main puzzle mencari jalan keluar labirin — kalau mentok, balik lagi ke persimpangan dan coba jalan lain. Itu Backtracking!" | 7 menit |

### Inti (175 menit)

#### Memahami (50 menit)

**1. Prinsip Backtracking — "Coba, Gagal, Mundur, Coba Lagi" (10 menit)**

| Langkah | Arti | Analogi Labirin |
|---|---|---|
| **Choose** | Pilih satu opsi yang tersedia | Ambil satu jalur di persimpangan |
| **Explore** | Lanjutkan dengan opsi tersebut | Jalan terus sampai ujung |
| **Check** | Apakah mencapai solusi? | Sampai keluar atau buntu? |
| **Backtrack** | Jika gagal → mundur, coba opsi lain | Balik ke persimpangan terakhir |
| **Prune** | Hentikan jalur yang pasti tidak mengarah ke solusi | "Jalur ini buntu, jangan coba" |

Karakteristik Backtracking:
- **Eksplorasi sistematis**: Coba semua kemungkinan dengan terstruktur
- **Recursive**: Biasanya diimplementasikan dengan rekursi
- **State space tree**: Pohon semua kemungkinan solusi
- **Pruning**: Potong cabang yang tidak mungkin sejak awal

**2. Contoh — Maze/Labirin (15 menit)**

Labirin 5×5 dari START (0,0) ke FINISH (4,4), hindari [X].

```
(0,0)──(0,1)──(0,2)──(0,3)──(0,4)
  │     [X]     │       │      │
(1,0)──(1,1)──(1,2)──(1,3)──(1,4)
  │      │      [X]     │      │
(2,0)──(2,1)──(2,2)──(2,3)──(2,4)
  │      │      │       │      │
(3,0)──(3,1)──(3,2)──(3,3)──(3,4)
  │      │      │       │      │
(4,0)──(4,1)──(4,2)──(4,3)──(4,4) → Finish
```

Demo: Tunjukkan pohon backtracking dan jalur yang dicoba hingga ditemukan solusi.

**3. Contoh — Permutasi {1, 2, 3} (15 menit)**

Pohon semua kemungkinan susunan:

```
                    []
        ┌───────────┼───────────┐
       [1]         [2]         [3]
    ┌───┼───┐   ┌───┼───┐   ┌───┼───┐
  [1,2] [1,3] [2,1] [2,3] [3,1] [3,2]
    │     │     │     │     │     │
  [1,2,3] [1,3,2] [2,1,3] [2,3,1] [3,1,2] [3,2,1]
```

Hasil: 6 permutasi = 3!
Tunjukkan pseudocode rekursif dan bagaimana backtrack bekerja.

**4. Visualisasi & Tanya Jawab (10 menit)**
- Demo labirin di papan tulis dengan kapur berwarna (tandai jalur sukses vs backtrack)
- Tanya: "Apa bedanya Backtracking dengan Brute Force?" (Backtracking bisa prune)
- Tanya: "Kapan kita tahu suatu jalur layak di-prune?"

#### Mengaplikasi (110 menit)

**5. Aktivitas 1 — Labirin 5×5 (15 menit) — Individu**

Labirin:
```
S . . X .
. X . . .
. . X . .
X . . . .
. . . . F
```
S = Start (0,0), F = Finish (4,4), X = tembok, . = jalan.
- Tentukan jalur dari S ke F
- Tandai setiap percobaan: (rute) dan (backtrack)
- Gambar pohon backtracking-nya

**6. Aktivitas 2 — Permutasi {A, B, C, D} (20 menit) — Berpasangan**
- Buat pohon permutasi lengkap (4! = 24)
- Tulis semua 24 permutasi
- Terapkan pruning: Buang cabang jika huruf vokal (A) bersebelahan dengan vokal lain
- Berapa solusi yang valid setelah pruning?

**7. Aktivitas 3 — N-Queens Mini (4×4) (30 menit) — Berpasangan**
- Masalah: Letakkan 4 ratu (Queen) di papan catur 4×4 sehingga tidak saling serang
- Aturan: Setiap baris, kolom, dan diagonal hanya boleh berisi 1 ratu
- Langkah Backtracking:
  1. Tempatkan ratu di baris 1, kolom 1
  2. Lanjut ke baris 2, cari kolom yang aman
  3. Jika tidak ada kolom aman → backtrack ke baris sebelumnya
  4. Ulangi sampai semua ratu terpasang
- Gambar papan 4×4 dan tulis langkah-langkahnya
- Berapa solusi yang ditemukan? (Ada 2 solusi untuk 4-Queens)

**8. Aktivitas 4 — Presentasi & Diskusi (25 menit)**
- 3 kelompok presentasi: 1 labirin, 1 permutasi, 1 N-Queens
- Diskusi: "Apa kelebihan dan kelemahan Backtracking?"
- Kuis interaktif: "Prune atau tidak?" — beri 3 situasi, siswa tebak apakah bisa diprune

**9. Soal Latihan Mandiri (20 menit)**
- Soal 1: Labirin 4×4 dengan rintangan, cari jalur
- Soal 2: Permutasi {1, 2, 3, 4} dengan pruning: angka genap (2,4) tidak boleh bersebelahan
- Soal 3: N-Queens 4×4 — gambar langkah backtracking hingga solusi ditemukan
- Kumpulkan untuk dinilai

#### Merefleksi (15 menit)

**10. Refleksi (15 menit)**
- Tulis perbandingan Greedy, D&C, dan Backtracking dalam 3 kalimat
- "Kapan waktu yang tepat menggunakan Backtracking?"
- "Apakah Backtracking selalu menjamin solusi optimal? Mengapa?"

### Penutup (35 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman — 5 langkah Backtracking + N-Queens | 5 menit |
| 2. Kuis lisan: 3 soal (tebak jalur backtracking) | 10 menit |
| 3. Preview: "Pert 11: Latihan Soal Strategi Algoritmik — Greedy, D&C, Backtracking" | 10 menit |
| 4. Tugas rumah: Implementasi pseudocode N-Queens 4×4 | 7 menit |
| 5. Doa & salam | 3 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Labirin | Tidak selesai | Jalur ditemukan | Jalur + tandai backtrack | Jalur + backtrack + pohon |
| Permutasi {A,B,C,D} | Tidak selesai | Sebagian | 24 permutasi | Pohon + pruning |
| N-Queens 4×4 | Tidak paham | 1 ratu benar | 2+ ratu benar | 4 ratu + backtrack |
| Refleksi | Tidak paham | 1 perbandingan | 2 perbandingan | 3 perbandingan + analisis |

---

**MGMP Informatika SMAN 6 Cimahi**
