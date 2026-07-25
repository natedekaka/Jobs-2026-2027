# MODUL AJAR INFORMATIKA – FASE F (KELAS XI)

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | F / XI |
| **Semester** | 1 (Ganjil) |
| **Pertemuan ke-** | 9 |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | SMA Negeri 6 Cimahi |
| **Materi Esensial** | Strategi Algoritmik |

---

## Tujuan Pembelajaran

| TP | IKTP |
|---|---|
| **BK, AP:** Memahami strategi Divide and Conquer | 9.1 Menjelaskan 3 langkah D&C (divide, conquer, combine) |
| | 9.2 Menerapkan D&C pada Binary Search |
| | 9.3 Menerapkan D&C pada Merge Sort |
| | 9.4 Menganalisis kompleksitas waktu D&C (log n, n log n) |

---

## Langkah Pembelajaran

### Pembukaan (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 3 menit |
| 2. **Review**: "Pert 8: Greedy — ambil yang terbaik sekarang. Hari ini: **Divide and Conquer** — pecah masalah besar jadi kecil-kecil!" | 5 menit |
| 3. **Apersepsi**: "Cari buku di perpustakaan yang rapi berurutan — bagaimana cara mencarinya dengan cepat? Tidak perlu lihat satu-satu!" | 7 menit |

### Inti (175 menit)

#### Memahami (50 menit)

**1. Konsep D&C — "Pecah, Selesaikan, Gabung" (10 menit)**

| Langkah | Arti | Analogi Gudang | Analogi Lain |
|---|---|---|---|
| **Divide** | Pecah masalah jadi submasalah lebih kecil | Bagi gudang jadi 2 bagian | Pecah tumpukan kartu jadi 2 |
| **Conquer** | Selesaikan setiap submasalah | Cari di masing-masing bagian | Urutkan setiap tumpukan |
| **Combine** | Gabungkan hasil | Satukan informasi | Gabung tumpukan terurut |

**2. Binary Search — Demo Interaktif (15 menit)**

Data terurut: [2, 5, 8, 12, 19, 24, 31, 37]
Cari 19:

| Langkah | Array | Tengah | Banding |
|---|---|---|---|
| 1 (Divide) | [2,5,8,12,19,24,31,37] | 12 (idx 3) | 19 > 12 → cari kanan |
| 2 (Divide) | [19,24,31,37] | 31 (idx 6) | 19 < 31 → cari kiri |
| 3 (Divide) | [19,24] | 19 (idx 4) | 19 = 19 ✅ Ditemukan! |

Hanya 3 langkah — vs 5 langkah sequential search.
- Demo 2: Cari 5 — hanya 2 langkah
- Demo 3: Cari 37 — hanya 3 langkah
- Tanya siswa: "Berapa maksimum langkah untuk n data?" (log₂ n)

**3. Merge Sort — Langkah Demi Langkah (15 menit)**

Data: [38, 27, 43, 3, 9, 82, 10]

```
Divide:
[38, 27, 43, 3]           [9, 82, 10]
[38, 27]   [43, 3]        [9, 82]   [10]
[38] [27]   [43] [3]      [9] [82]  [10]

Conquer & Combine:
[27, 38]   [3, 43]        [9, 82]   [10]
[3, 27, 38, 43]          [9, 10, 82]
[3, 9, 10, 27, 38, 43, 82] ✅
```

Visualisasi proses combine: tunjukkan cara membandingkan elemen pertama dua array dan mengambil yang lebih kecil.

**4. Visualisasi & Tanya Jawab (10 menit)**
- Demo visual Binary Search dengan kartu angka di papan tulis
- Tanya: "Mengapa data harus terurut untuk Binary Search?"
- Tanya: "Apa yang terjadi jika data tidak terurut?"
- Bahas kompleksitas: O(log n) vs O(n), O(n log n) vs O(n²)

#### Mengaplikasi (110 menit)

**5. Aktivitas 1 — Binary Search Manual (15 menit) — Individu**
   - Data: [3, 7, 11, 15, 22, 28, 34, 41, 50, 56]
   - Cari: 34, 7, 50, 15
   - Catat langkah divide setiap pencarian dalam format tabel!
   - Hitung jumlah langkah vs sequential search

**6. Aktivitas 2 — Merge Sort Manual (25 menit) — Berpasangan**
   - Data: [42, 16, 7, 23, 31, 5, 19, 8, 51, 12]
   - Gambar diagram pohon divide → conquer → combine
   - Tulis hasil akhir terurut
   - Hitung jumlah perbandingan yang dilakukan

**7. Aktivitas 3 — Quick Sort dengan D&C (25 menit) — Berpasangan**
   - Konsep Quick Sort: pilih pivot, partisi kiri (< pivot) dan kanan (> pivot), rekursif
   - Data: [33, 10, 55, 22, 18, 47, 5, 39]
   - Langkah:
     1. Pilih pivot (ambil elemen terakhir: 39)
     2. Partisi: kiri = [33,10,22,18,5], kanan = [55,47], pivot = [39]
     3. Rekursif pada kiri dan kanan (pilih pivot lagi)
     4. Gabungkan semua: kiri terurut + pivot + kanan terurut
   - Gambar pohon rekursi Quick Sort
   - Bandingkan dengan Merge Sort: Quick Sort tidak perlu combine (in-place)

**8. Aktivitas 4 — Perbandingan Algoritma & Analisis (25 menit)**
   - Sequential Search O(n) vs Binary Search O(log n)
   - Bubble Sort O(n²) vs Merge Sort O(n log n) vs Quick Sort O(n log n)
   - Hitung untuk n=100, n=1000, n=1.000.000
   - Diskusi: "Kapan pakai Merge Sort? Kapan pakai Quick Sort?"

| Algoritma | Best Case | Average Case | Worst Case |
|---|---|---|---|
| Sequential Search | O(1) | O(n) | O(n) |
| Binary Search | O(1) | O(log n) | O(log n) |
| Bubble Sort | O(n) | O(n²) | O(n²) |
| Merge Sort | O(n log n) | O(n log n) | O(n log n) |
| Quick Sort | O(n log n) | O(n log n) | O(n²) |

**9. Soal Latihan Mandiri (20 menit)**
   - Soal 1: Binary Search pada data [4, 9, 13, 18, 25, 30, 37, 42, 56, 63] — cari 42 dan 13
   - Soal 2: Merge Sort pada data [55, 22, 18, 47, 5, 39, 61, 28] — gambar pohon lengkap
   - Soal 3: Quick Sort pada data [29, 14, 37, 8, 51, 3, 42] — tulis langkah partisi
   - Kumpulkan untuk dinilai

#### Merefleksi (15 menit)

**10. Refleksi (15 menit)**
   - Tulis perbedaan antara Greedy dan D&C dalam 2-3 kalimat
   - Sebutkan 1 algoritma D&C selain Binary Search, Merge Sort, Quick Sort
   - "Menurutmu, apakah D&C selalu lebih baik dari pendekatan biasa? Mengapa?"

### Penutup (35 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman — 3 langkah D&C + kompleksitas | 5 menit |
| 2. Kuis lisan: tebak kompleksitas 3 algoritma | 10 menit |
| 3. Preview: "Pert 10: Backtracking — coba-coba, kalau salah mundur" | 10 menit |
| 4. Tugas rumah: Implementasi Binary Search dalam pseudocode + hitung langkah untuk n=1000 | 7 menit |
| 5. Doa & salam | 3 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Binary Search manual | Tidak bisa | 1 benar | 2 benar | 3 benar + langkah |
| Merge Sort manual | Tidak selesai | Divide saja | Divide + conquer | Divide + conquer + combine benar |
| Analisis kompleksitas | Tidak paham | 1 benar | 2 benar | 2 benar + hitungan n |

---

**MGMP Informatika SMAN 6 Cimahi**
