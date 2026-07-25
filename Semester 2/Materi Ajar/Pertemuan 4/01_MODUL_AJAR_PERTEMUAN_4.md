# MODUL AJAR INFORMATIKA – FASE E (KELAS X)

## Informasi Umum

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | E / X |
| **Semester** | 2 (Genap) |
| **Pertemuan ke-** | 4 |
| **Alokasi Waktu** | 2 JP × 45 menit (90 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | **SMA Negeri 6 Cimahi** |

---

## Tujuan Pembelajaran

| TP | Indikator Ketercapaian Tujuan Pembelajaran (IKTP) |
|---|---|
| **BK 1.1, 1.3:** Memahami dan menerapkan algoritma pencarian standar | 1.3.1 Menjelaskan konsep algoritma pencarian<br>1.3.2 Mendemonstrasikan cara kerja sequential search<br>1.3.3 Menganalisis kelebihan dan kekurangan sequential search<br>1.3.4 Menerapkan sequential search pada data array |

---

## Langkah Pembelajaran

### Pembukaan (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran — **Selamat datang kembali!** | 3 menit |
| 2. **Ice breaking**: "Apa kegiatan paling berkesan selama libur?" + **Review tugas Ramadan**: kumpulkan rangkuman & soal | 7 menit |
| 3. **Apersepsi**: "Bagaimana cara kamu mencari buku di rak perpustakaan? Lihat satu per satu dari awal sampai ketemu? Itu sequential search!" | 5 menit |

### Inti (60 menit)

#### Memahami (15 menit)

1. **Algoritma Pencarian (5 menit)**
   - **Pencarian = mencari data tertentu dalam kumpulan data**
   - Sequential search = cara paling sederhana: **cek satu per satu dari awal**
   - **Ibarat mencari buku**: mulai dari rak 1, lihat judul, lanjut, sampai ketemu

2. **Cara Kerja Sequential Search (5 menit)**
   ```
   Array: [10, 45, 78, 23, 56, 89, 12, 34]
   Cari: 56
   
   Langkah 1: 10 ≠ 56 → lanjut
   Langkah 2: 45 ≠ 56 → lanjut
   Langkah 3: 78 ≠ 56 → lanjut
   Langkah 4: 23 ≠ 56 → lanjut
   Langkah 5: 56 = 56 → KETEMU! (indeks 4)
   ```

3. **Kelebihan & Kekurangan (5 menit)**
   | Kelebihan | Kekurangan |
   |---|---|
   | Sederhana, mudah dipahami | Lambat untuk data besar (O(n)) |
   | Data tidak perlu terurut | Mencari semua elemen jika target di akhir |
   | Bisa untuk data tak terurut | Tidak efisien dibanding binary search |

#### Mengaplikasi (35 menit)

4. **Aktivitas 1: Simulasi Manual Sequential Search (15 menit)**
   - 8 siswa maju, masing-masing pegang kertas angka
   - Guru sebut angka target → siswa mencari dengan cara: satu per satu dari kiri ke kanan
   - Catat: berapa langkah sampai ketemu?
   - **Ulangi** dengan target di awal, tengah, akhir, dan tidak ada

5. **Aktivitas 2: Sequential Search LKPD (20 menit) — Berpasangan**

   **Tugas:** Diberikan array dan beberapa target, cari dengan sequential search.

   ```
   Array: [15, 82, 37, 91, 44, 53, 68, 29, 76, 10]
   ```

   | Target | Ada/Tidak? | Indeks | Langkah |
   |---|---|---|---|
   | 91 | | | |
   | 10 | | | |
   | 50 | | | |
   | 37 | | | |
   | 68 | | | |

   **Soal analisis:**
   - Berapa langkah maksimal untuk mencari dalam array 10 elemen?
   - Jika array 100 elemen, berapa langkah maksimal?
   - Kapan sequential search sangat lambat?

#### Merefleksi (10 menit)

6. **Diskusi (5 menit)**
   - "Kapan kalian menggunakan sequential search dalam kehidupan sehari-hari?"
   - "Apa yang terjadi jika data sangat besar (1 juta data)?"
   - "Bagaimana cara mempercepat pencarian?"

7. **Refleksi (5 menit)**

### Penutup (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman | 3 menit |
| 2. Tanya jawab | 5 menit |
| 3. **Tugas**: Cari 1 contoh sequential search di kehidupan + tulis langkah-langkahnya | 3 menit |
| 4. Sampaikan pertemuan depan: Binary Search — lebih cepat! | 2 menit |
| 5. Doa & salam | 2 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Simulasi | Tidak ikut | Ikut pasif | Ikut aktif | Aktif + catat langkah |
| LKPD | < 2 benar | 2–3 benar | 4 benar | 5 benar + analisis |
| Analisis | Tidak bisa | 1 analisis | 2 analisis | 3 analisis + tepat |

---

**MGMP Informatika SMAN 6 Cimahi**
