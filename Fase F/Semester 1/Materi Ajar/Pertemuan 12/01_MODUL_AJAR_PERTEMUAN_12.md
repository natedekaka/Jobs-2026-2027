# MODUL AJAR INFORMATIKA – FASE F (KELAS XI)

| Komponen | Deskripsi |
|---|---|
| **Mata Pelajaran** | Informatika |
| **Fase / Kelas** | F / XI |
| **Semester** | 1 (Ganjil) |
| **Pertemuan ke-** | 12 |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Tahun Pelajaran** | 2026/2027 |
| **Satuan Pendidikan** | SMA Negeri 6 Cimahi |
| **Materi Esensial** | Strategi Algoritmik |

---

## Tujuan Pembelajaran

| TP | IKTP |
|---|---|
| **BK, AP:** Memahami graph dan algoritma traversal | 12.1 Menjelaskan struktur graph (verteks, edge, derajat) |
| | 12.2 Membedakan jenis graph (berarah, tak berarah, berbobot) |
| | 12.3 Menjelaskan BFS (Breadth-First Search) dengan queue |
| | 12.4 Menjelaskan DFS (Depth-First Search) dengan stack/rekursi |
| | 12.5 Melakukan BFS dan DFS pada graph sederhana |

---

## Langkah Pembelajaran

### Pembukaan (15 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Salam, doa, cek kehadiran | 3 menit |
| 2. **Review**: "Pert 8-11: Greedy, D&C, Backtracking. Hari ini: **Graph** — struktur data yang ada di mana-mana!" | 5 menit |
| 3. **Apersepsi**: "Facebook friends recommendation — bagaimana Facebook tahu kalian punya teman yang sama? Itu pakai **graph**! Atau Google Maps cari rute terpendek — graph juga!" | 7 menit |

### Inti (175 menit)

#### Memahami (50 menit)

**1. Apa itu Graph? (15 menit)**
- **Graph**: kumpulan **verteks** (simpul) dan **edge** (sisi) yang menghubungkannya
- **Vertex (V)**: simpul/node — misal: orang, kota, halaman web
- **Edge (E)**: hubungan antar simpul — misal: pertemanan, jalan, hyperlink
- Notasi: G = (V, E)

| Istilah | Arti | Analogi |
|---|---|---|
| Vertex / Node | Simpul | Anggota keluarga |
| Edge | Sisi/hubungan | Hubungan keluarga |
| Derajat (degree) | Jumlah edge yang terhubung ke verteks | Jumlah teman |
| Path | Jalur dari satu verteks ke verteks lain | Silsilah |

**2. Jenis-Jenis Graph (15 menit)**

| Jenis | Edge | Contoh |
|---|---|---|
| **Tak berarah** | Dua arah (A—B) | Facebook pertemanan |
| **Berarah** (Directed) | Satu arah (A→B) | Twitter follow |
| **Berbobot** (Weighted) | Punya nilai/bobot | Google Maps jarak |
| **Sederhana** | Tanpa edge ganda | Graph biasa |
| **Lengkap** | Semua verteks terhubung | Turnamen sepak bola |

**3. Representasi Graph (10 menit)**

| Cara | Struktur | Kelebihan | Kekurangan |
|---|---|---|---|
| **Adjacency Matrix** | Matriks V×V, 1=ada edge | Cek edge O(1) | Boros memori O(V²) |
| **Adjacency List** | Array daftar tetangga | Hemat memori | Cek edge O(V) |

**4. BFS & DFS — Pengantar (10 menit)**

| Algoritma | Struktur Data | Cara | Contoh |
|---|---|---|---|
| **BFS** | Queue (FIFO) | Level by level | Cari teman terdekat |
| **DFS** | Stack (LIFO) / Rekursi | Masuk terdalam dulu | Cari jalan buntu |

#### Mengaplikasi (95 menit)

**5. Aktivitas 1 — Representasi Graph (20 menit) — Individu**
   - Diberikan graph sosial media (5 orang dengan hubungan pertemanan)
   - Buat adjacency matrix dan adjacency list
   - Tentukan derajat setiap verteks

**6. Aktivitas 2 — BFS Manual (25 menit) — Berpasangan**
   - Graph: A—B—C—D, A—E—D (A terhubung ke B dan E)
   - Lakukan BFS dari A
   - Tulis urutan kunjungan dan isi queue di setiap langkah

**7. Aktivitas 3 — DFS Manual (25 menit) — Berpasangan**
   - Graph yang sama dengan Aktivitas 2
   - Lakukan DFS dari A (gunakan stack)
   - Tulis urutan kunjungan dan isi stack di setiap langkah
   - Bandingkan hasil BFS vs DFS

**8. Aktivitas 4 — Graph Nyata (25 menit) — Kelompok**
   - Cari contoh graph dalam kehidupan sehari-hari (selain media sosial)
   - Gambar graph-nya
   - Jelaskan: verteks, edge, jenis graph, dan bagaimana BFS/DFS bisa diterapkan
   - Presentasi singkat (2 kelompok)

#### Merefleksi (15 menit)

**9. Refleksi Jurnal (15 menit)**
- 3 hal dipelajari tentang graph
- Perbedaan BFS dan DFS
- Kapan sebaiknya pakai BFS? Kapan DFS?

### Penutup (35 menit)

| Kegiatan | Waktu |
|---|---|
| 1. Rangkuman: Graph = V + E. BFS = Queue (level). DFS = Stack (dalam). Representasi: Matriks vs List | 10 menit |
| 2. Kuis lisan: tebak jenis graph dari deskripsi (5 soal) | 10 menit |
| 3. Preview: "Pert 13: Algoritma Dijkstra — mencari jalur terpendek!" | 5 menit |
| 4. Tugas rumah: Cari 1 aplikasi graph di dunia nyata, gambar, dan jelaskan | 10 menit |

---

## Asesmen

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Representasi graph | Tidak bisa | Matriks / list saja | Keduanya | Keduanya + derajat |
| BFS traversal | Tidak bisa | Urutan salah | Urutan benar | Urutan benar + queue |
| DFS traversal | Tidak bisa | Urutan salah | Urutan benar | Urutan benar + stack |

---

**MGMP Informatika SMAN 6 Cimahi**
