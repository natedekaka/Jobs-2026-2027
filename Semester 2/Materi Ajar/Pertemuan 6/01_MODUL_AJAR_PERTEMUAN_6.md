# MODUL AJAR INFORMATIKA – FASE E (KELAS X)

## Informasi Umum

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | E / X |
| **Semester** | 2 (Genap) |
| **Pertemuan ke-** | 6 |
| **Alokasi Waktu** | 2 JP × 45 menit (90 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | **SMA Negeri 6 Cimahi** |

---

## Tujuan Pembelajaran

| TP | Indikator Ketercapaian Tujuan Pembelajaran (IKTP) |
|---|---|
| **BK 1.1, 1.3:** Memahami dan menerapkan algoritma pengurutan standar | 1.3.9 Menjelaskan konsep pengurutan (sorting)<br>1.3.10 Mendemonstrasikan cara kerja bubble sort<br>1.3.11 Mendemonstrasikan cara kerja insertion sort<br>1.3.12 Membandingkan efisiensi bubble sort dan insertion sort |

---

## Langkah Pembelajaran

### Pembukaan (10 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 2 menit |
| 2. **Review binary search**: "Syarat binary search?" (Data terurut). "Hari ini kita belajar **mengurutkan** data!" | 3 menit |
| 3. **Apersepsi**: 5 siswa maju dengan tinggi berbeda. "Urutkan dari terpendek ke tertinggi! — Itulah **sorting**! Sekarang kita akan belajar cara komputer melakukannya." | 5 menit |

### Inti (65 menit)

#### Memahami (20 menit)

1. **Apa itu Sorting? (5 menit)**
   - **Sorting** = mengurutkan data berdasarkan kriteria tertentu
   - **Mengapa penting?** Data terurut → binary search bisa bekerja
   - **Dua algoritma sorting sederhana**: Bubble Sort & Insertion Sort

2. **Bubble Sort — Gelembung yang Mengapung (8 menit)**
   - Prinsip: Bandingkan dua data berdekatan → tukar jika tidak urut → data terbesar "menggelembung" ke akhir
   - **Ilustrasi** [5, 3, 8, 1]:
     ```
     Pas 1: [5,3,8,1] → 5>3 → tukar → [3,5,8,1]
            [3,5,8,1] → 5<8 → tetap
            [3,5,8,1] → 8>1 → tukar → [3,5,1,8] (8 mengapung)
     Pas 2: [3,5,1,8] → 3<5 → tetap
            [3,5,1,8] → 5>1 → tukar → [3,1,5,8] (5 mengapung)
     Pas 3: [3,1,5,8] → 3>1 → tukar → [1,3,5,8] ✅
     ```

3. **Insertion Sort — Menyisipkan Kartu (7 menit)**
   - Prinsip: Ambil data → sisipkan ke posisi yang tepat di data yang sudah terurut
   - **Ilustrasi** [5, 3, 8, 1] — seperti menyusun kartu di tangan:
     ```
     Ambil 5 → [5] (sudah urut)
     Ambil 3 → [3,5] (3 < 5 → sisip di depan)
     Ambil 8 → [3,5,8] (8 > 5 → di belakang)
     Ambil 1 → [1,3,5,8] (1 < 3 → di depan)
     ```

#### Mengaplikasi (40 menit)

4. **Aktivitas 1: Simulasi Bubble Sort dengan Kartu (15 menit) — Berpasangan**
   - 5 kartu acak: [5, 3, 8, 1, 6]
   - Praktik bubble sort: bandingkan 2 kartu berdekatan → tukar jika tidak urut
   - Ulangi sampai semua urut
   - Catat jumlah pertukaran dan pas

5. **Aktivitas 2: Simulasi Insertion Sort dengan Kartu (15 menit) — Berpasangan**
   - 5 kartu acak: [5, 3, 8, 1, 6]
   - Praktik insertion sort: ambil kartu → sisipkan ke posisi tepat
   - Catat jumlah langkah

6. **Aktivitas 3: Perbandingan (10 menit)**
   - Diskusi: "Mana yang lebih mudah? Bubble atau Insertion?"
   - "Data [2,4,6,8,1] — mana yang lebih cepat?"
   - Tabel perbandingan di LKPD

#### Merefleksi (5 menit)

7. **Refleksi (5 menit)**

### Penutup (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman | 3 menit |
| 2. **Review PTS**: "Pertemuan depan PTS — materi Struktur Data (Array, Stack, Queue) + Algoritma (Sequential, Binary, Bubble, Insertion)" | 5 menit |
| 3. Tanya jawab persiapan PTS | 5 menit |
| 4. Doa & salam | 2 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Simulasi bubble | Tidak ikut | Ikut pasif | Ikut aktif | Aktif + catat pertukaran |
| Simulasi insertion | Tidak ikut | Ikut pasif | Ikut aktif | Aktif + catat langkah |
| Perbandingan | Tidak bisa | 1 perbedaan | 2 perbedaan | 3+ perbedaan + tepat |

---

**MGMP Informatika SMAN 6 Cimahi**
