# ASESMEN – PERTEMUAN 12
## Graph, BFS & DFS

Informatika – Fase F / Kelas XI – SMA Negeri 6 Cimahi

---

## Rubrik Penilaian

### A. Istilah & Jenis Graph (Bobot 15%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Soal 1 (istilah) | 0–1 benar | 2 benar | 3 benar | 4 benar |
| Soal 2 (jenis) | 0–1 benar | 2 benar | 3 benar | 4 benar |

### B. Representasi Graph (Bobot 30%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Adjacency Matrix | Tidak diisi | Sebagian | Hampir semua | Semua benar |
| Adjacency List | Tidak diisi | Sebagian | Hampir semua | Semua benar |
| Derajat | 0–2 benar | 3–4 benar | 5 benar | 6 benar |

### C. BFS Traversal (Bobot 25%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Urutan BFS | Tidak bisa | Urutan sebagian | Urutan benar | Urutan + queue benar |

### D. DFS Traversal (Bobot 20%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Urutan DFS | Tidak bisa | Urutan sebagian | Urutan benar | Urutan + stack benar |

### E. Refleksi & Tugas (Bobot 10%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Refleksi | Tidak diisi | 1 jawaban | 2 jawaban | 3+ jawaban |

---

## Kunci Jawaban

### Soal 1 — Istilah

| Istilah | Arti | Contoh Graph Media Sosial |
|---|---|---|
| Vertex | Simpul/node | Akun pengguna |
| Edge | Sisi/hubungan | Pertemanan |
| Derajat | Jumlah edge terhubung | Jumlah teman |
| Path | Jalur antar verteks | Teman dari teman |

### Soal 2 — Jenis Graph

| Graph | Jenis |
|---|---|
| Twitter follow | Berarah (Directed) |
| Jalan tol | Tak berarah, berbobot |
| Group WhatsApp | Tak berarah (lengkap) |
| Turnamen sepak bola | Tak berarah, lengkap |

### Soal 3 — Representasi Graph

**Adjacency Matrix:**

| | Andi | Budi | Citra | Dewi | Eka | Fani |
|---|---|---|---|---|---|---|
| Andi | 0 | 1 | 0 | 1 | 0 | 0 |
| Budi | 1 | 0 | 1 | 0 | 0 | 0 |
| Citra | 0 | 1 | 0 | 0 | 0 | 1 |
| Dewi | 1 | 0 | 0 | 0 | 1 | 0 |
| Eka | 0 | 0 | 0 | 1 | 0 | 1 |
| Fani | 0 | 0 | 1 | 0 | 1 | 0 |

**Adjacency List:**
```
Andi: [Budi, Dewi]
Budi: [Andi, Citra]
Citra: [Budi, Fani]
Dewi: [Andi, Eka]
Eka: [Dewi, Fani]
Fani: [Citra, Eka]
```

**Derajat:**
- Andi: 2 (Budi, Dewi)
- Budi: 2 (Andi, Citra)
- Citra: 2 (Budi, Fani)
- Dewi: 2 (Andi, Eka)
- Eka: 2 (Dewi, Fani)
- Fani: 2 (Citra, Eka)

### Soal 4 — BFS dari Andi

| Langkah | Queue | Kunjungan |
|---|---|---|
| 0 | [Andi] | — |
| 1 | [Budi, Dewi] | Andi ✅ |
| 2 | [Dewi, Citra] | Andi, Budi ✅ |
| 3 | [Citra, Eka] | Andi, Budi, Dewi ✅ |
| 4 | [Eka, Fani] | Andi, Budi, Dewi, Citra ✅ |
| 5 | [Fani] | Andi, Budi, Dewi, Citra, Eka ✅ |
| 6 | [] | Andi, Budi, Dewi, Citra, Eka, Fani ✅ |

**Urutan BFS:** Andi → Budi → Dewi → Citra → Eka → Fani

### Soal 5 — DFS dari Andi (tetangga urut abjad)

| Langkah | Stack | Kunjungan |
|---|---|---|
| 0 | [Andi] | — |
| 1 | [Budi, Dewi] | Andi ✅ |
| 2 | [Budi, Eka] | Andi, Dewi ✅ |
| 3 | [Budi, Fani] | Andi, Dewi, Eka ✅ |
| 4 | [Budi, Citra] | Andi, Dewi, Eka, Fani ✅ |
| 5 | [Budi] | Andi, Dewi, Eka, Fani, Citra ✅ |
| 6 | [] | Andi, Dewi, Eka, Fani, Citra, Budi ✅ |

**Urutan DFS:** Andi → Dewi → Eka → Fani → Citra → Budi

---

**MGMP Informatika SMAN 6 Cimahi**
