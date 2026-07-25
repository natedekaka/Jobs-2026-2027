# MODUL AJAR INFORMATIKA – FASE F (KELAS XI)

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | F / XI |
| **Semester** | 1 (Ganjil) |
| **Pertemuan ke-** | 13 |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | SMA Negeri 6 Cimahi |
| **Materi Esensial** | Strategi Algoritmik |

---

## Tujuan Pembelajaran

| TP | IKTP |
|---|---|
| **BK, AP:** Memahami algoritma Dijkstra | 13.1 Menjelaskan masalah jalur terpendek (shortest path) |
| | 13.2 Menjelaskan langkah-langkah algoritma Dijkstra |
| | 13.3 Menjalankan Dijkstra pada graph berbobot sederhana |
| | 13.4 Menganalisis kompleksitas dan penerapan Dijkstra |

---

## Langkah Pembelajaran

### Pembukaan (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 3 menit |
| 2. **Review**: "Pert 12: Graph, BFS, DFS. Hari ini: **Dijkstra** — mencari jalur terpendek di graph berbobot!" | 5 menit |
| 3. **Apersepsi**: "Google Maps — kalian masukkan asal dan tujuan. Dalam hitungan detik, Maps tahu rute tercepat. **Algoritma Dijkstra** adalah salah satu jawabannya!" | 7 menit |

### Inti (175 menit)

#### Memahami (50 menit)

**1. Masalah Jalur Terpendek (10 menit)**
- Diberikan graph berbobot: setiap edge punya biaya/jarak
- Tujuan: cari jalur dengan total biaya terkecil dari start ke semua verteks
- Contoh: cari rute termurah dari rumah ke sekolah

**2. Algoritma Dijkstra — Langkah (25 menit)**

| Langkah | Aksi |
|---|---|
| 1 | Set jarak start = 0, semua verteks lain = ∞ |
| 2 | Pilih verteks dengan jarak terkecil yang belum diproses |
| 3 | Perbarui jarak tetangganya (relaxation) |
| 4 | Tandai verteks sebagai sudah diproses |
| 5 | Ulangi langkah 2-4 sampai semua verteks diproses |

**Relaxation:** `jarak_baru = jarak_verteks + bobot_edge`
Jika `jarak_baru < jarak_tetangga` → perbarui jarak tetangga.

**3. Contoh Lengkap (15 menit)**

```
   A ──4── B ──1── C
   │       │       │
   2       5       3
   │       │       │
   D ──8── E ──6── F
```

Cari jarak terpendek dari A ke semua verteks.

Tabel langkah:

| Langkah | Verteks | A(0) | B(∞) | C(∞) | D(∞) | E(∞) | F(∞) |
|---|---|---|---|---|---|---|---|
| 1 | Pilih A | 0* | 4 | ∞ | 2 | ∞ | ∞ |
| 2 | Pilih D | | 4 | ∞ | 2* | 10 | ∞ |
| 3 | Pilih B | | 4* | 5 | | 9 | ∞ |
| 4 | Pilih C | | | 5* | | 8 | 8 |
| 5 | Pilih E | | | | | 8* | 8 |
| 6 | Pilih F | | | | | | 8* |

#### Mengaplikasi (95 menit)

**4. Aktivitas 1 — Dijkstra Manual (30 menit) — Individu**
   - Graph: Rumah(0) → Toko(5) → Sekolah(3) → Rumah(0)→Pasar(2)→Sekolah(1)
   - Cari jalur terpendek dari Rumah ke Sekolah
   - Isi tabel jarak setiap langkah

**5. Aktivitas 2 — Dijkstra Graph Lebih Besar (30 menit) — Berpasangan**
   - Graph dengan 7 verteks (A-G) dengan bobot acak
   - Cari jarak terpendek dari A ke G
   - Tulis tabel dan jalur yang ditempuh

**6. Aktivitas 3 — Studi Kasus Google Maps (20 menit) — Kelompok**
   - Gambar peta sederhana (4-5 tempat di sekitar sekolah)
   - Tentukan bobot (jarak dalam meter)
   - Jalankan Dijkstra dari gerbang sekolah ke setiap tempat
   - Presentasikan rute terpendek

**7. Aktivitas 4 — Review Strategi Algoritmik (15 menit)**
   - Diskusi: dari 6 pertemuan strategi algoritmik (Greedy, D&C, Backtracking, Graph, Dijkstra) — mana favorit?
   - Hubungkan: Dijkstra adalah Greedy! (ambil verteks dengan jarak terkecil saat ini = local optimum)

#### Merefleksi (15 menit)

**8. Refleksi Jurnal (15 menit)**
- 3 hal dipelajari
- Kenapa Dijkstra disebut algoritma Greedy?
- Aplikasi Dijkstra di kehidupan nyata selain Google Maps?

### Penutup (35 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman: Dijkstra = Greedy + Graph. Cari jarak terpendek. Relaxation = perbarui jarak tetangga | 10 menit |
| 2. Kuis lisan: tebak langkah relaxation (5 soal) | 10 menit |
| 3. Preview bab baru: "Pert 14: Pengolahan Data Bervolume Besar — Big Data!" | 5 menit |
| 4. Tugas rumah: Cari jalur terpendek dari rumah ke sekolah menggunakan Dijkstra (gambar + tabel) | 10 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Dijkstra manual | Tidak bisa | Sebagian langkah | Tabel benar | Tabel + jalur |
| Dijkstra graph 7 verteks | Tidak bisa | Jarak awal | Jarak benar | Jarak + jalur |
| Studi kasus peta | Tidak ikut | Graph | Dijkstra | Presentasi |

---

**MGMP Informatika SMAN 6 Cimahi**
