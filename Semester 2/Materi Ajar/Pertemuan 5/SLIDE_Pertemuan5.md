---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 5 — SEMESTER 2
## Binary Search
### Informatika – Fase E / Kelas X
#### SMA Negeri 6 Cimahi

---

## Review

**Sequential Search:** 100 data → maks 100 langkah.

**Hari ini:** kita bisa cari di 1.000.000 data hanya dalam **20 langkah**!

> Kok bisa?

---

## Apersepsi: Tebak Angka! 🎯

**Pilih angka 1–100, saya tebak!**

- "50?" → "Terlalu besar" / "Terlalu kecil"
- "25?" → ...
- Saya pasti bisa dalam **≤ 7 tebakan**!

> Itulah **Binary Search**!

---

# TUJUAN PEMBELAJARAN

1. ✅ Syarat binary search
2. ✅ Cara kerja belah dua
3. ✅ Kecepatan O(log n)
4. ✅ Sequential vs Binary

---

## Syarat Binary Search

### Data Harus TERURUT! 📋

| Array | Bisa Binary? |
|---|---|
| [10, 23, 45, 56, 78, 89] | ✅ |
| [10, 45, 23, 89, 56, 78] | ❌ |

> Urut dulu, baru binary!

---

## Cara Kerja

**Cari 23 di [10, 23, 45, 56, 78, 89, 92, 99]**

```
Langkah 1: tengah = 56
           23 < 56 → cari KIRI
           
Langkah 2: tengah = 23
           23 = 23 → ✅ KETEMU! Indeks 1
```

Hanya **2 langkah**! 🚀

---

## Visualisasi

```
10  23  45  56  78  89  92  99
│              │              │
kiri         mid          kanan
              56

23 < 56 → buang kanan
┌─────────────────────┐
│ 10  23  45  56 │ 78  89  92  99 ✘
└─────────────────────┘

Langkah 2:
10  23  45  56
│   │       │
kiri mid   kanan
     23
23 = 23 → ✅ KETEMU!
```

---

## Sequential vs Binary

| Data | Sequential | Binary |
|---|---|---|
| 10 | 10 langkah | 4 langkah |
| 100 | 100 | 7 |
| 1.000 | 1.000 | 10 |
| 1.000.000 | 1.000.000 | **20** 🚀 |

> Binary 50.000× lebih cepat untuk 1 juta data!

---

## Aktivitas 1: Tebak Angka

### Klasikal — 10 menit

- Guru pilih angka rahasia 1–100
- Kalian tebak pakai binary search
- Guru: "Lebih besar!" / "Lebih kecil!"
- Hitung tebakan → selalu ≤ 7!

> Coba buktikan!

---

## Aktivitas 2: Binary dengan Kartu

### Berpasangan — 15 menit

**Array:** [10, 23, 45, 56, 78, 89, 92, 99]

Cari dengan binary search:
1. 23 → berapa langkah?
2. 99 → berapa langkah?
3. 50 → berapa langkah? (tidak ada)

---

## Aktivitas 3: Perbandingan

### Isi tabel:

| Data | Sequential | Binary |
|---|---|---|
| 8 | | |
| 100 | | |
| 1 juta | | |

> Mana yang lebih cepat?

---

## Python Code 🐍

```python
def binary_search(arr, target):
    kiri, kanan = 0, len(arr) - 1
    while kiri <= kanan:
        mid = (kiri + kanan) // 2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            kiri = mid + 1
        else:
            kanan = mid - 1
    return -1
```

---

## Rangkuman

| Konsep | Inti |
|---|---|
| **Binary Search** | Belah dua, buang setengah |
| **Syarat** | Data harus **terurut** |
| **Kecepatan** | O(log n) — super cepat |
| **Sequential** | O(n) — lambat untuk data besar |

---

## Tugas Rumah

**Tebak angka 1–100** di rumah:
1. Minta orang tua/teman pilih angka
2. Tebak pakai binary search
3. Catat jumlah tebakan (≤ 7!)

---

## Pertemuan Depan

### Bubble Sort & Insertion Sort
> Mengurutkan data — tapi cara mana yang paling efisien?

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Binary search mengajarkan: kadang cara tercepat bukan dengan melihat semua — tapi dengan tahu mana yang bisa dibuang."
