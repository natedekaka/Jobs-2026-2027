# MODUL AJAR INFORMATIKA – FASE F (KELAS XI)

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | F / XI |
| **Semester** | 1 (Ganjil) |
| **Pertemuan ke-** | 8 |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | SMA Negeri 6 Cimahi |
| **Materi Esensial** | Strategi Algoritmik |

---

## Tujuan Pembelajaran

| TP | IKTP |
|---|---|
| **BK, AP:** Memahami algoritma Greedy | 8.1 Menjelaskan prinsip Greedy (ambil yang terbaik saat ini) |
| | 8.2 Menyelesaikan masalah penukaran koin dengan Greedy |
| | 8.3 Menyelesaikan masalah knapsack pecahan dengan Greedy |
| | 8.4 Menganalisis kelebihan & kelemahan Greedy |

---

## Langkah Pembelajaran

### Pembukaan (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 3 menit |
| 2. **Review**: "Pert 1–7 kita belajar Proses Rekayasa. Mulai hari ini: **Strategi Algoritmik** — cara berpikir untuk menyelesaikan masalah!" | 5 menit |
| 3. **Apersepsi**: "Jika kalian punya uang Rp11.800 dan ingin ditukar ke pecahan minimal — apa yang kalian lakukan?" | 7 menit |

### Inti (175 menit)

#### Memahami (50 menit)

**1. Prinsip Greedy — "Rakus yang Cerdas" (10 menit)**
- **Greedy = rakus**: Ambil pilihan terbaik yang tersedia *saat ini* tanpa memikirkan masa depan
- **Tujuan**: Mendapatkan solusi optimal secara global dengan pilihan optimal lokal
- **Analogi**: "Kalau lapar, ambil makanan terbesar yang bisa dimakan sekarang — meskipun nanti kenyang dan tidak bisa makan hidangan penutup"
- **Kapan Greedy cocok?**: Masalah yang punya *optimal substructure* dan *greedy choice property*

**2. Karakteristik Greedy (10 menit)**

| Prinsip | Penjelasan | Contoh |
|---|---|---|
| **Greedy Choice** | Ambil pilihan terbaik saat ini | Ambil pecahan terbesar dulu |
| **Optimal Substructure** | Solusi optimal dari submasalah → solusi optimal global | Sisa uang setelah ambil pecahan besar |
| **Irrevocable** | Tidak bisa mundur — sekali pilih, tidak bisa dibatalkan | Tidak bisa "kembalikan" uang yang sudah diambil |
| **Local vs Global** | Optimal lokal belum tentu optimal global | Greedy gagal pada某些 kasus |

**3. Contoh Klasik — Penukaran Koin (15 menit)**

Masalah: Tukar Rp11.800 dengan jumlah koin/uang minimal.

Pecahan: Rp10.000, Rp5.000, Rp2.000, Rp1.000, Rp500, Rp200, Rp100

Langkah Greedy:
```
Sisa: 11.800
Ambil 10.000 (terbesar ≤ 11.800) → sisa 1.800
Ambil 1.000 (terbesar ≤ 1.800)  → sisa 800
Ambil 500  (terbesar ≤ 800)     → sisa 300
Ambil 200  (terbesar ≤ 300)     → sisa 100
Ambil 100  (terbesar ≤ 100)     → sisa 0
Hasil: 10.000 + 1.000 + 500 + 200 + 100 = 5 lembar
```

**4. Demo & Latihan Terbimbing (15 menit)**
- Guru demo 1 soal penukaran koin di papan tulis
- Siswa mengerjakan 1 soal bersama: Rp17.200
- Bahas langkah demi langkah: pilih pecahan terbesar, kurangi, ulangi
- Tunjukkan visualisasi dengan tabel/langkah bersusun

#### Mengaplikasi (110 menit)

**5. Aktivitas 1 — Penukaran Koin (15 menit) — Individu**
   - Pecahan: Rp20.000, Rp10.000, Rp5.000, Rp2.000, Rp1.000, Rp500, Rp200, Rp100
   - Tentukan koin minimal untuk: Rp27.500, Rp33.700, Rp45.900, Rp51.300
   - Gunakan langkah Greedy dan tulis setiap langkah

**6. Aktivitas 2 — Fractional Knapsack (25 menit) — Berpasangan**
   - Masalah: Tas kapasitas 50 kg. Tersedia barang:
     - Emas: 30 kg, Rp60.000.000/kg
     - Perak: 20 kg, Rp10.000.000/kg
     - Berlian: 5 kg, Rp100.000.000/kg
     - Mutiara: 10 kg, Rp25.000.000/kg
   - Hitung density (nilai/kg) setiap barang
   - Urutkan dari density tertinggi
   - Tentukan kombinasi maksimal! (Boleh pecahan)
   - Format jawaban: tabel density → urutan → perhitungan → total nilai

**7. Aktivitas 3 — Activity Selection (25 menit) — Berpasangan**
   - Masalah: Pilih aktivitas sebanyak mungkin dalam satu ruangan
   - Data aktivitas (start, finish):
     - A1: (1, 4), A2: (3, 5), A3: (0, 6), A4: (5, 7), A5: (3, 8), A6: (5, 9), A7: (6, 10), A8: (8, 11)
   - **Langkah Greedy**: Pilih aktivitas dengan finish time terkecil yang tidak bertabrakan
   - Urutkan berdasarkan waktu selesai
   - Pilih aktivitas yang start-nya >= finish aktivitas terakhir yang dipilih
   - Tulis aktivitas terpilih dan total durasi

**8. Aktivitas 4 — Presentasi & Diskusi (25 menit)**
   - 3 pasangan presentasi: 1 knapsack, 1 activity selection, 1 perbandingan
   - Diskusi: "Kapan Greedy gagal?" (contoh: penukaran koin dengan pecahan non-kanonik)
   - Kuis lisan interaktif: 3 soal cepat rebutan

**9. Soal Latihan Mandiri (20 menit)**
   - Soal 1: Penukaran Rp67.800 dengan pecahan yang sama
   - Soal 2: Knapsack dengan data berbeda (kapasitas 100 kg, 5 barang)
   - Soal 3: Activity Selection dengan 10 aktivitas
   - Kumpulkan hasilnya untuk dinilai

#### Merefleksi (15 menit)

**10. Refleksi (15 menit)**
   - Tulis 1 paragraf: "Apa yang saya pahami tentang Greedy?"
   - Sebutkan 1 kelebihan dan 1 kelemahan Greedy
   - Beri contoh masalah yang TIDAK cocok untuk Greedy

### Penutup (35 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman — poin kunci Greedy | 5 menit |
| 2. Kuis lisan: 3 soal (rebutan) | 10 menit |
| 3. Preview: "Pert 9: Divide and Conquer — pecah masalah besar jadi kecil" | 10 menit |
| 4. Tugas rumah: Cari 3 masalah sehari-hari yang bisa diselesaikan dengan Greedy + tulis langkahnya | 7 menit |
| 5. Doa & salam | 3 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Penukaran koin Greedy | Tidak bisa | 1 soal benar | 2 soal benar | 3 soal benar |
| Fractional Knapsack | Tidak bisa | Urutan density salah | Urutan benar, hitung salah | Benar semua |
| Refleksi Greedy | Tidak paham | Kelebihan saja | Kelebihan + kelemahan | Analisis kapan Greedy gagal |

---

**MGMP Informatika SMAN 6 Cimahi**
