# LEMBAR KERJA PESERTA DIDIK (LKPD)
## Pertemuan 8 – Algoritma Greedy

| TP | BK, AP — Strategi Algoritmik |
|---|---|
| Nama | ____________________ |
| Kelas | ____________________ |

---

### A. PENUKARAN KOIN

**Soal 1:** Tentukan jumlah koin/lembar minimal menggunakan Greedy!

Pecahan: Rp20.000, Rp10.000, Rp5.000, Rp2.000, Rp1.000, Rp500, Rp200, Rp100

| Uang | Langkah Greedy | Jumlah |
|---|---|---|
| Rp27.500 | | |
| Rp33.700 | | |
| Rp45.900 | | |

**Soal 2:** Pecahan ganjil 1, 3, 4 — tukar uang 6.

| Langkah Greedy | Hasil Greedy |
|---|---|
| Ambil 4, sisa 2 → ambil 1, sisa 1 → ambil 1 | 4+1+1 = **3 koin** |

**Pertanyaan:** Apakah hasil Greedy optimal? Ada solusi lebih baik?

---

### B. FRACTIONAL KNAPSACK

**Soal 3:** Tas kapasitas 60 kg.

| Barang | Berat (kg) | Harga Total | Density (harga/kg) |
|---|---|---|---|
| A | 10 | Rp100.000.000 | |
| B | 20 | Rp140.000.000 | |
| C | 30 | Rp150.000.000 | |
| D | 15 | Rp225.000.000 | |

**Langkah:**
1. Hitung density (harga/kg) setiap barang!
2. Urutkan dari density tertinggi ke terendah!
3. Ambil sesuai kapasitas!

| Urutan | Barang | Density | Berat | Ambil | Total Berat |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |

**Total nilai optimal:** Rp _______________

---

### C. ACTIVITY SELECTION

**Soal 4:** Pilih kegiatan terbanyak tanpa tumpang tindih!

| Kegiatan | Mulai | Selesai |
|---|---|---|
| A | 07:00 | 08:30 |
| B | 08:00 | 09:00 |
| C | 09:00 | 10:00 |
| D | 09:30 | 11:00 |
| E | 10:30 | 12:00 |
| F | 11:00 | 12:30 |

**Langkah:**
1. Urutkan berdasarkan waktu selesai menaik:
2. Pilih kegiatan pertama → lalu cari yang mulai ≥ selesai sebelumnya

**Kegiatan terpilih:** ____, ____, ____ = **___ kegiatan**

---

### D. REFLEKSI

| Pertanyaan | Jawaban |
|---|---|
| Inti dari algoritma Greedy? | |
| Kapan Greedy bisa gagal? Beri contoh! | |
| Kesulitan saat mengerjakan knapsack? | |
| Skala pemahaman (1–10) | / 10 |

---

### E. TUGAS RUMAH

Cari 1 masalah sehari-hari yang bisa diselesaikan dengan Greedy!
- Deskripsikan masalah
- Langkah Greedy-nya
- Apakah hasilnya optimal?

---

**MGMP Informatika SMAN 6 Cimahi**
