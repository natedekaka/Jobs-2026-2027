# MODUL AJAR INFORMATIKA – FASE E (KELAS X)

## Informasi Umum

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | E / X |
| **Semester** | 2 (Genap) |
| **Pertemuan ke-** | 5 |
| **Alokasi Waktu** | 2 JP × 45 menit (90 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | **SMA Negeri 6 Cimahi** |

---

## Tujuan Pembelajaran

| TP | Indikator Ketercapaian Tujuan Pembelajaran (IKTP) |
|---|---|
| **BK 1.1, 1.3:** Memahami dan menerapkan algoritma pencarian standar | 1.3.5 Menjelaskan syarat binary search (data terurut)<br>1.3.6 Mendemonstrasikan cara kerja binary search (belah dua)<br>1.3.7 Membandingkan efisiensi sequential vs binary search<br>1.3.8 Menerapkan binary search pada data array terurut |

---

## Langkah Pembelajaran

### Pembukaan (10 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 2 menit |
| 2. **Review sequential search**: "Berapa langkah cari di 100 data?" (100 langkah). "Hari ini kita belajar cara yang lebih CEPAT!" | 3 menit |
| 3. **Apersepsi: Permainan Tebak Angka** — "Pikir angka 1–100. Saya akan tebak dalam ≤ 7 tebakan!" Guru demo tebak angka siswa. "Kok bisa? Itulah binary search!" | 5 menit |

### Inti (65 menit)

#### Memahami (20 menit)

1. **Konsep Binary Search (10 menit)**
   - **Syarat**: Data harus **terurut**
   - **Cara kerja**: Belah array jadi dua → bandingkan target dengan elemen tengah → cari di kiri atau kanan
   - **Setiap langkah**: buang setengah data yang tidak mungkin

   **Ilustrasi cari 23 di [10, 23, 45, 56, 78, 89, 92, 99]:**
   ```
   Langkah 1: [10, 23, 45, 56, 78, 89, 92, 99] → tengah = 56
              23 < 56 → cari di kiri
   Langkah 2: [10, 23, 45, 56] → tengah = 23
              23 = 23 → KETEMU! (indeks 1)
   ```
   Hanya **2 langkah**! Sequential butuh 2 langkah juga (kebetulan).

2. **Perbandingan Efisiensi (10 menit)**
   | Metode | 10 data | 100 data | 1.000 data | 1.000.000 data |
   |---|---|---|---|---|
   | **Sequential** | 10 | 100 | 1.000 | 1.000.000 |
   | **Binary** | 4 | 7 | 10 | 20 |

   **Demo:** Guru minta siswa buka kalkulator — log₂(1.000.000) ≈ 20.

#### Mengaplikasi (35 menit)

3. **Aktivitas 1: Tebak Angka Kelas (10 menit)**
   - Guru pilih angka rahasia 1–100
   - Siswa tebak → guru bilang "lebih besar" / "lebih kecil"
   - Hitung jumlah tebakan
   - **Ulangi** — buktikan selalu ≤ 7 tebakan

4. **Aktivitas 2: Binary Search dengan Kartu (15 menit) — Berpasangan**
   - 8 kartu terurut: [10, 23, 45, 56, 78, 89, 92, 99]
   - Cari target dengan metode binary search
   - **Percobaan**: cari 23, 99, 10, 45, 50 (tidak ada)
   - Catat jumlah langkah tiap target

5. **Aktivitas 3: Perbandingan Sequential vs Binary (10 menit)**
   - LKPD: tabel perbandingan sequential vs binary
   - Diskusi: "Kapan pakai sequential? Kapan binary?"

#### Merefleksi (10 menit)

6. **Kuis Cepat (5 menit)**
   - "Syarat binary search?" (Data terurut)
   - "Binary search 1.000 data → maks berapa langkah?" (10)
   - "Sequential 1.000 data → maks berapa langkah?" (1.000)

7. **Refleksi (5 menit)**

### Penutup (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman | 3 menit |
| 2. **Tugas**: Tebak angka 1–100 di rumah dengan binary search — buktikan ≤ 7 tebakan | 3 menit |
| 3. Sampaikan pertemuan depan: **Bubble Sort & Insertion Sort** | 2 menit |
| 4. Doa & salam | 2 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Tebak angka | Tidak ikut | Ikut pasif | Ikut aktif | Aktif + strategi |
| Binary search kartu | < 2 benar | 2–3 benar | 4 benar | 4 benar + hitung langkah |
| Perbandingan | Tidak bisa | 1 perbedaan | 2 perbedaan | ≥ 3 perbedaan + tepat |

---

**MGMP Informatika SMAN 6 Cimahi**
