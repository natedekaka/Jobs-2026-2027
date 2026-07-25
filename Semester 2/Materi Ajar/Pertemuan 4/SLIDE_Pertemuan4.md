---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 4 — SEMESTER 2
## Sequential Search
### Informatika – Fase E / Kelas X
#### SMA Negeri 6 Cimahi

---

## Selamat Datang Kembali! 🎉

**Setelah libur Ramadan & Idul Fitri...**

- Kumpulkan **tugas Ramadan** (rangkuman + soal + visualgo)
- Siap belajar lagi!

> Hari ini kita mulai **algoritma**!

---

## Apersepsi

**Cari buku di rak perpustakaan:**

- Mulai dari ujung kiri
- Lihat judul satu per satu
- Sampai ketemu

> Itulah **Sequential Search**!

---

# TUJUAN PEMBELAJARAN

1. ✅ Algoritma pencarian
2. ✅ Cara kerja sequential search
3. ✅ Kelebihan & kekurangan
4. ✅ Menerapkan ke dalam array

---

## Algoritma Pencarian

**Tujuan:** Menemukan data tertentu dalam kumpulan data

| Algoritma | Data Terurut? | Kecepatan |
|---|---|---|
| **Sequential Search** | ❌ Tidak perlu | ⏳ O(n) |
| **Binary Search** | ✅ Harus terurut | ⚡ O(log n) |

> Hari ini: Sequential. Besok: Binary!

---

## Cara Kerja Sequential Search

```
Array: [10, 45, 78, 23, 56, 89, 12, 34]
Cari: 56

Langkah ke-1: 10 ≠ 56 → lanjut
Langkah ke-2: 45 ≠ 56 → lanjut
Langkah ke-3: 78 ≠ 56 → lanjut
Langkah ke-4: 23 ≠ 56 → lanjut
Langkah ke-5: 56 = 56 → ✅ KETEMU!

Indeks 4, butuh 5 langkah.
```

---

## Kelebihan & Kekurangan

| ✅ Kelebihan | ❌ Kekurangan |
|---|---|
| Sederhana | Lambat untuk data besar |
| Data tidak perlu terurut | Bisa cek semua elemen |
| Cocok data kecil (< 100) | O(n) — linear |

> Sequential search = sederhana tapi lambat.
> Seperti cari buku dengan lihat satu per satu.

---

## Kasus

| Kasus | Terjadi | Langkah |
|---|---|---|
| **Terbaik** | Target di awal | 1 |
| **Rata-rata** | Target di tengah | n/2 |
| **Terburuk** | Target di akhir/tidak ada | n |

**O(n):** 10 data → 10 langkah. 1 juta data → 1 juta langkah!

---

## Aktivitas 1: Simulasi Cari Angka

### Berpasangan — 15 menit

**Array:** [15, 82, 37, 91, 44, 53, 68, 29, 76, 10]

Cari target:
1. **91** — berapa langkah?
2. **10** — berapa langkah?
3. **50** — berapa langkah? (target tidak ada)

> Tulis di LKPD!

---

## Aktivitas 2: Soal Cerita

**Soal 1:** Daftar 30 siswa. Cari "Budi Santoso". Maks langkah?

**Soal 2:** Array [5,8,2,9,1,7,3,6,4]. Cari 3. Berapa langkah?

**Soal 3:** Array [10,20,30,40,50]. Cari 35. Berapa langkah?

---

## Python Code 🐍

```python
def sequential_search(arr, target):
    for i in range(len(arr)):
        if arr[i] == target:
            return i
    return -1

nilai = [15, 82, 37, 91, 44, 53, 68, 29, 76, 10]
print(sequential_search(nilai, 91))
# Output: 3
```

> Nanti kita coding ini di pertemuan Python!

---

## Refleksi

1. Contoh sequential search di kehidupan?
2. Kapan sequential search sangat lambat?
3. Skala pemahamanmu: ___ / 10

---

## Rangkuman

| Konsep | Inti |
|---|---|
| **Sequential Search** | Cek satu per satu dari awal |
| **O(n)** | Waktu = jumlah data |
| **Kelebihan** | Sederhana, data tidak perlu urut |
| **Kekurangan** | Lambat untuk data besar |

---

## Tugas Rumah

**Cari 1 contoh sequential search** di kehidupanmu!

Tulis langkah-langkahnya di buku.

Contoh: mencari kunci, mencari file, mencari kontak...

---

## Pertemuan Depan

### Binary Search 🎯
> Lebih cepat — tapi data harus terurut!

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Sequential search mengajarkan: kadang yang paling sederhana bukan yang paling cepat — tapi yang paling jujur."
