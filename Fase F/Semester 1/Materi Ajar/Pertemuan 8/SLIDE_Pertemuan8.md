---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 8 — FASE F
## Strategi Algoritmik — Greedy
### Informatika – Fase F / Kelas XI
#### SMA Negeri 6 Cimahi

---

## Materi Esensial Baru!

| Pert 1-7 | Pert 8-13 |
|---|---|
| ✅ Proses Rekayasa | 🔄 **Strategi Algoritmik** |

> Hari ini: **Algoritma Greedy** — rakus yang cerdas!

---

## Apersepsi

"Kamu punya Rp11.800. Ingin ditukar ke pecahan minimal. Pecahan: 10.000, 5.000, 2.000, 1.000, 500, 200, 100."

> Apa yang kamu lakukan?

---

# TUJUAN PEMBELAJARAN

1. ✅ Prinsip Greedy
2. ✅ Penukaran Koin
3. ✅ Fractional Knapsack
4. ✅ Kelebihan & kelemahan

---

## Greedy = Rakus!

**Prinsip**: Ambil pilihan terbaik **saat ini juga** (local optimum)
**Harapan**: Menghasilkan solusi terbaik global

| Strategi | Cara |
|---|---|
| **Greedy** | Ambil yang terbaik sekarang, teruskan |
| **Non-Greedy** | Hitung semua kemungkinan dulu |

---

## Karakteristik Greedy

| Karakteristik | Arti |
|---|---|
| **Greedy Choice** | Pilih yang terbaik saat ini |
| **Optimal Substructure** | Submasalah → solusi global |
| **Irrevocable** | Tidak bisa mundur |

---

## Penukaran Koin — Rp11.800

| Sisa | Ambil | Sisa Baru |
|---|---|---|
| 11.800 | 10.000 ✅ | 1.800 |
| 1.800 | 1.000 ✅ | 800 |
| 800 | 500 ✅ | 300 |
| 300 | 200 ✅ | 100 |
| 100 | 100 ✅ | 0 |

**Hasil: 5 lembar!** 🎉

---

## Algoritma Penukaran Koin

```
PROCEDURE TukarKoin(M, koin[1..n])
    sisa ← M
    FOR i ← 1 TO n DO
        WHILE sisa ≥ koin[i] DO
            ambil koin[i]
            sisa ← sisa - koin[i]
        ENDWHILE
    ENDFOR
END
```

---

## Aktivitas 1: Penukaran Koin

### Individu — 10 menit

Pecahan: 20k, 10k, 5k, 2k, 1k, 500, 200, 100

| Uang | Jumlah Minimal |
|---|---|
| Rp27.500 | ? |
| Rp33.700 | ? |
| Rp45.900 | ? |

---

## Fractional Knapsack

**Masalah**: Tas 50 kg, barang boleh pecahan.

| Barang | Berat | Harga/kg |
|---|---|---|
| Berlian | 5 kg | Rp100jt |
| Emas | 30 kg | Rp60jt |
| Mutiara | 10 kg | Rp25jt |
| Perak | 20 kg | Rp10jt |

**Strategi Greedy: Ambil density tertinggi dulu!**

---

## Langkah Knapsack

| Urutan | Barang | Density | Ambil | Total |
|---|---|---|---|---|
| 1 | Berlian | 100jt | 5 kg | 5 kg |
| 2 | Emas | 60jt | 30 kg | 35 kg |
| 3 | Mutiara | 25jt | 10 kg | 45 kg |
| 4 | Perak | 10jt | 5 kg | **50 kg** |

Total: **Rp2.600.000.000!** 💰

---

## Activity Selection

Pilih kegiatan terbanyak tanpa tumpang tindih!

| Keg | Mulai | Selesai |
|---|---|---|
| A | 08:00 | 10:00 |
| B | 09:00 | 11:00 |
| C | 10:30 | 12:00 |
| D | 11:30 | 13:00 |
| E | 13:00 | 14:00 |

**Strategi: Pilih yang selesai paling awal!**

A (08-10) + C (10:30-12) + E (13-14) = **3 kegiatan** ✅

---

## Kapan Greedy GAGAL?

**Pecahan 1, 3, 4 — tukar uang 6**

| Greedy | Optimal |
|---|---|
| 4 + 1 + 1 = **3 koin** | 3 + 3 = **2 koin** |

❌ Greedy tidak selalu optimal!

---

## Kelebihan vs Kelemahan

| ✅ Kelebihan | ❌ Kelemahan |
|---|---|
| Sederhana | Tidak selalu optimal |
| Cepat O(n log n) | Hanya masalah tertentu |
| Cocok masalah besar | Sukar dibuktikan |

---

## Aktivitas 2: Knapsack

### Berpasangan — 15 menit

Tas 60 kg:
- A: 10 kg, Rp100jt
- B: 20 kg, Rp140jt
- C: 30 kg, Rp150jt
- D: 15 kg, Rp225jt

> Hitung density, urutkan, ambil!

---

## Rangkuman

| Masalah | Strategi Greedy |
|---|---|
| Penukaran Koin | Ambil pecahan terbesar |
| Knapsack | Ambil density tertinggi |
| Jadwal | Pilih selesai paling awal |

> Greedy = cepat & sederhana — tapi tidak selalu optimal!

---

## Tugas Rumah

Cari 1 masalah sehari-hari yang bisa pakai Greedy!

> Contoh: milih antrian kasir terpendek, isi bensin di pom terdekat

---

## Pertemuan Depan

### Divide and Conquer
> Pecah masalah besar jadi masalah kecil!

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Greedy: ambil yang terbaik sekarang, urusan nanti — nanti!"
