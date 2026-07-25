# LEMBAR KERJA PESERTA DIDIK (LKPD)
## Pertemuan 12 – Graph, BFS & DFS

| TP | BK, AP — Strategi Algoritmik |
|---|---|
| Nama | ____________________ |
| Kelas | ____________________ |

---

### A. ISTILAH GRAPH

**Soal 1:** Isilah tabel berikut!

| Istilah | Arti | Contoh dalam Graph Media Sosial |
|---|---|---|
| Vertex | | |
| Edge | | |
| Derajat (degree) | | |
| Path | | |

**Soal 2:** Tentukan jenis graph berikut!

| Graph | Jenis |
|---|---|
| Twitter follow (@A → @B, @B → @C) | |
| Jalan tol (GT A — 5km — GT B) | |
| Group WhatsApp (semua anggota chat) | |
| Turnamen sepak bola (semua tim bermain) | |

---

### B. REPRESENTASI GRAPH

**Soal 3:** Diberikan graph pertemanan berikut:

```
Andi — Budi — Citra
  |             |
Dewi — Eka — Fani
```

Buat **Adjacency Matrix** dan **Adjacency List**!

**Adjacency Matrix:**

| | Andi | Budi | Citra | Dewi | Eka | Fani |
|---|---|---|---|---|---|---|
| Andi | 0 | 1 | 0 | 1 | 0 | 0 |
| Budi | | 0 | | | | |
| Citra | | | 0 | | | |
| Dewi | | | | 0 | | |
| Eka | | | | | 0 | |
| Fani | | | | | | 0 |

**Adjacency List:**

```
Andi: [_________, _________]
Budi: [_________, _________]
Citra: [_________, _________]
Dewi: [_________, _________, _________]
Eka: [_________, _________]
Fani: [_________]
```

**Derajat setiap verteks:**
- Andi: __
- Budi: __
- Citra: __
- Dewi: __
- Eka: __
- Fani: __

---

### C. BFS TRAVERSAL

**Soal 4:** Lakukan BFS dari verteks **Andi** pada graph di atas!

Isi tabel setiap langkah:

| Langkah | Queue (depan → belakang) | Vertex Dikunjungi | Kunjungan |
|---|---|---|---|
| 0 | [Andi] | — | |
| 1 | | Andi | Andi ✅ |
| 2 | | | |
| 3 | | | |
| 4 | | | |
| 5 | | | |
| 6 | | | |

**Urutan BFS dari Andi:** _________________________________

---

### D. DFS TRAVERSAL

**Soal 5:** Lakukan DFS dari verteks **Andi** pada graph yang sama!

Isi tabel setiap langkah:

| Langkah | Stack (bawah → atas) | Vertex Dikunjungi | Kunjungan |
|---|---|---|---|
| 0 | [Andi] | — | |
| 1 | | Andi | Andi ✅ |
| 2 | | | |
| 3 | | | |
| 4 | | | |
| 5 | | | |
| 6 | | | |

**Urutan DFS dari Andi:** _________________________________

---

### E. REFLEKSI

| Pertanyaan | Jawaban |
|---|---|
| Beda adjacency matrix dan adjacency list? | |
| Kapan BFS lebih baik dari DFS? | |
| Contoh graph di kehidupan sehari-hari? | |
| Skala pemahaman (1–10) | / 10 |

---

### F. TUGAS RUMAH

Cari 1 contoh graph di kehidupan nyata (selain media sosial)!
- Gambar graph-nya
- Jenis graph
- Bagaimana BFS/DFS bisa diterapkan?

---

**MGMP Informatika SMAN 6 Cimahi**
