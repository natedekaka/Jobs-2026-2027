# ASESMEN – PERTEMUAN 8
## Algoritma Greedy

Informatika – Fase F / Kelas XI – SMA Negeri 6 Cimahi

---

## Rubrik Penilaian

### A. Penukaran Koin (Bobot 30%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Soal 1 (3 soal penukaran) | 0–1 benar | 2 benar | 3 benar + langkah sebagian | 3 benar + langkah lengkap |
| Soal 2 (pecahan 1,3,4) | Tidak jawab | Greedy 3 koin | Tahu optimal 3+3=2 | Analisis kapan Greedy gagal |

### B. Fractional Knapsack (Bobot 35%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Menghitung density | Tidak | 2 benar | 3 benar | 4 benar |
| Urutan & pengambilan | Tidak urut | Urut benar, ambil salah | Urut + ambil benar | Urut + ambil + total nilai benar |

### C. Activity Selection (Bobot 20%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Urutan waktu selesai | Tidak urut | 3 tepat | 4–5 tepat | Semua tepat |
| Kegiatan terpilih | Salah | 2 kegiatan | 3 kegiatan | 3 + optimal |

### D. Refleksi & Tugas (Bobot 15%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Refleksi | Tidak diisi | 1 jawaban | 2 jawaban | 3 jawaban + mendalam |

---

## Kunci Jawaban

### Soal 1 — Penukaran Koin

| Uang | Langkah Greedy | Jumlah |
|---|---|---|
| Rp27.500 | 20.000 + 5.000 + 2.000 + 500 | 4 |
| Rp33.700 | 20.000 + 10.000 + 2.000 + 1.000 + 500 + 200 | 6 |
| Rp45.900 | 20.000 + 20.000 + 5.000 + 500 + 200 + 200 | 6 |

### Soal 2 — Pecahan 1, 3, 4

Greedy: 4 + 1 + 1 = 3 koin
**Optimal**: 3 + 3 = 2 koin
**Kesimpulan**: Greedy gagal — sistem pecahan tidak standar.

### Soal 3 — Fractional Knapsack

Density:
- A: 100jt/10 = Rp10jt/kg
- B: 140jt/20 = Rp7jt/kg
- C: 150jt/30 = Rp5jt/kg
- D: 225jt/15 = **Rp15jt/kg** ← tertinggi

Urutan: D (15jt), A (10jt), B (7jt), C (5jt)

| Urutan | Barang | Density | Berat | Ambil | Total Berat |
|---|---|---|---|---|---|
| 1 | D | 15jt | 15 | 15 (ambil semua) | 15 |
| 2 | A | 10jt | 10 | 10 (ambil semua) | 25 |
| 3 | B | 7jt | 20 | 20 (ambil semua) | 45 |
| 4 | C | 5jt | 30 | 15 (sisa kapasitas) | 60 |

Total: 15×15jt + 10×10jt + 20×7jt + 15×5jt
= 225jt + 100jt + 140jt + 75jt = **Rp540jt**

### Soal 4 — Activity Selection

Urutkan berdasarkan waktu selesai:
1. A (07:00–08:30) ✅ diambil
2. B (08:00–09:00) — mulai 08:00 < 08:30 ❌
3. C (09:00–10:00) — mulai 09:00 ≥ 08:30 ✅ diambil
4. D (09:30–11:00) — mulai 09:30 < 10:00 ❌
5. E (10:30–12:00) — mulai 10:30 ≥ 10:00 ✅ diambil
6. F (11:00–12:30) — mulai 11:00 < 12:00 ❌ (tapi mulai 11:00 ≥ 10:30 → sebenarnya 11:00 ≥ 10:30 ✅, tapi 11:00 < 12:00 ❌)

Wait, let me recalculate. After picking C (09:00-10:00), lastSelesai = 10:00.

D: 09:30-11:00 → 09:30 < 10:00 ❌
E: 10:30-12:00 → 10:30 ≥ 10:00 ✅ pick E, lastSelesai = 12:00
F: 11:00-12:30 → 11:00 < 12:00 ❌

Result: A, C, E = 3 activities.

After E (10:30-12:00):
F (11:00-12:30): 11:00 < 12:00 ❌. But wait, F starts at 11:00 which is < 12:00.

So yes: A, C, E = 3 kegiatan.

---

**MGMP Informatika SMAN 6 Cimahi**
