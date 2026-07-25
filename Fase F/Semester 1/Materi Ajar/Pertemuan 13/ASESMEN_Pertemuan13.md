# ASESMEN – PERTEMUAN 13
## Algoritma Dijkstra

Informatika – Fase F / Kelas XI – SMA Negeri 6 Cimahi

---

## Rubrik Penilaian

### A. Konsep Dijkstra (Bobot 15%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Soal 1 (istilah) | 0–1 benar | 2 benar | 3 benar | 4 benar |
| Soal 2 (Greedy) | Tidak tahu | Sebagian | Benar | Benar + penjelasan |

### B. Dijkstra Graph 1 (Bobot 35%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Tabel langkah | Tidak diisi | 2 langkah | 4–5 langkah | 6 langkah lengkap |
| Hasil jarak | 0–1 benar | 2–3 benar | 4–5 benar | 6 benar |
| Jalur A→F | Tidak ada | Sebagian | Benar | Benar + jarak |

### C. Dijkstra Graph 2 (Bobot 25%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Tabel | Tidak diisi | Sebagian | Lengkap | Lengkap + benar |
| Jarak & jalur | Salah | Jarak benar | Jarak + jalur benar | Lengkap |

### D. Studi Kasus (Bobot 15%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Graph peta | Tidak ada | 3 tempat | 4 tempat | 5 tempat + bobot |
| Dijkstra | Tidak | Sebagian | Selesai | Presentasi |

### E. Refleksi (Bobot 10%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Refleksi | Tidak diisi | 1 jawaban | 2 jawaban | 3 jawaban |

---

## Kunci Jawaban

### Soal 1 — Istilah

| Istilah | Arti |
|---|---|
| Jalur terpendek | Jalur dengan total bobot edge terkecil dari start ke target |
| Bobot edge | Nilai/biaya suatu edge (jarak, waktu, biaya) |
| Relaxation | Memperbarui jarak tetangga jika ditemukan jalur lebih pendek |
| Final | Verteks yang sudah diproses — jaraknya sudah pasti |

### Soal 2 — Dijkstra Greedy
Karena Dijkstra selalu memilih verteks dengan jarak terkecil saat ini (greedy choice) tanpa mempertimbangkan masa depan.

### Soal 3 — Graph 1 (A ke semua)

| Langkah | Pilih | A(0) | B(∞) | C(∞) | D(∞) | E(∞) | F(∞) |
|---|---|---|---|---|---|---|---|
| 0 | — | **0** | ∞ | ∞ | ∞ | ∞ | ∞ |
| 1 | A | 0* | 5 | ∞ | 2 | ∞ | ∞ |
| 2 | D | 0* | 5 | ∞ | 2* | 8 | ∞ |
| 3 | B | 0* | 5* | 8 | 2* | 8 | ∞ |
| 4 | C | 0* | 5* | 8* | 2* | 8 | 9 |
| | | | | | | | (8+1) |
| 5 | E | 0* | 5* | 8* | 2* | 8* | 9 |
| | | | | | | | (8+2=10 > 9) |
| 6 | F | 0* | 5* | 8* | 2* | 8* | 9* |

**Hasil:**
- A→B: 5
- A→C: 8
- A→D: 2
- A→E: 8
- A→F: 9

**Jalur A→F:** A → B → C → F (5+3+1=9)
Atau: A → D → E → F (2+6+2=10 — lebih jauh)

### Soal 4 — Graph 2 (Sekolah ke Rumah)

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
| 1 | S | 0* | 3 | ∞ | 4 | ∞ | ∞ |
| 2 | Toko | 0* | 3* | 8 | 4 | ∞ | ∞ |
| 3 | Rumah | 0* | 3* | 8 | 4* | 6 | ∞ |
| 4 | Klinik | 0* | 3* | 8 | 4* | 6* | 7 |
| 5 | Pasar | 0* | 3* | 8* | 4* | 6* | 7 |
| | | | | | | | (8+6=14 > 7) |
| 6 | Kantor | 0* | 3* | 8* | 4* | 6* | 7* |

**Jarak Sekolah → Rumah:** 4 (langsung S→Rumah dengan bobot 4)

**Jalur alternatif:** S → Toko → ... → Rumah = 3+?+? 

Dari tabel:
- S→Rumah: 4 (langsung)
- S→Toko→Pasar = 3+5=8
- S→Rumah→Klinik = 4+2=6
- S→Rumah→Klinik→Kantor = 6+1=7

---

**MGMP Informatika SMAN 6 Cimahi**
