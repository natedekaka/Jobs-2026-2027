# LEMBAR KERJA PESERTA DIDIK (LKPD)
## Pertemuan 13 – Algoritma Dijkstra

| TP | BK, AP — Strategi Algoritmik |
|---|---|
| Nama | ____________________ |
| Kelas | ____________________ |

---

### A. KONSEP DIJKSTRA

**Soal 1:** Isilah tabel berikut!

| Istilah | Arti |
|---|---|
| Jalur terpendek | |
| Bobot edge | |
| Relaxation | |
| Final (dalam Dijkstra) | |

**Soal 2:** Algoritma Dijkstra disebut Greedy karena...

---

### B. DIJKSTRA MANUAL — Graph 1

**Soal 3:** Cari jarak terpendek dari **A** ke semua verteks!

```
   A ──5── B ──3── C
   │               │
   2               1
   │               │
   D ──6── E ──2── F
```

| Langkah | Pilih | A(0) | B(∞) | C(∞) | D(∞) | E(∞) | F(∞) |
|---|---|---|---|---|---|---|---|
| 0 | — | **0** | ∞ | ∞ | ∞ | ∞ | ∞ |
| 1 | A | 0* | 5 | ∞ | 2 | ∞ | ∞ |
| 2 | | | | | | | |
| 3 | | | | | | | |
| 4 | | | | | | | |
| 5 | | | | | | | |
| 6 | | | | | | | |

**Hasil:**
- A → B: ___
- A → C: ___
- A → D: ___
- A → E: ___
- A → F: ___

**Jalur A → F:** _________________________________

---

### C. DIJKSTRA MANUAL — Graph 2 (Berpasangan)

**Soal 4:** Cari jarak terpendek dari **Sekolah** ke **Rumah**!

```
   Sekolah ──3── Toko ──5── Pasar
      │                  │
      4                  6
      │                  │
   Rumah ──2── Klinik ──1── Kantor
```

| Langkah | Pilih | S(0) | Toko | Pasar | Rumah | Klinik | Kantor |
|---|---|---|---|---|---|---|---|
| 0 | — | **0** | ∞ | ∞ | ∞ | ∞ | ∞ |
| 1 | | | | | | | |
| ... | | | | | | | |

**Jarak terpendek Sekolah → Rumah:** ________

**Jalur:** _________________________________

---

### D. STUDI KASUS — PETA SEKOLAH (Kelompok)

**Soal 5:** Gambar peta 4-5 tempat di sekitar sekolah!
Tentukan jarak antar tempat sebagai bobot.

| Tempat | Terhubung ke | Bobot (meter) |
|---|---|---|
| Gerbang Sekolah | | |
| | | |

Cari jalur terpendek dari Gerbang Sekolah ke:
1. ________________ → jarak: ____
2. ________________ → jarak: ____
3. ________________ → jarak: ____

---

### E. REFLEKSI

| Pertanyaan | Jawaban |
|---|---|
| Kenapa Dijkstra disebut Greedy? | |
| Beda Dijkstra dengan BFS? | |
| Selain Google Maps, aplikasi Dijkstra? | |
| Skala pemahaman (1–10) | / 10 |

---

### F. TUGAS RUMAH

Cari jalur terpendek dari rumah ke sekolah menggunakan Dijkstra!
- Gambar graph: tempat-tempat yang dilewati beserta jaraknya
- Tabel langkah Dijkstra
- Jalur terpendek

---

**MGMP Informatika SMAN 6 Cimahi**
