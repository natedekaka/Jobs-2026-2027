# BAHAN AJAR – PERTEMUAN 4
## Sequential Search (Pencarian Berurutan)

| TP | BK 1.1, 1.3 |
|---|---|

---

### A. APA ITU ALGORITMA PENCARIAN?

Algoritma pencarian adalah langkah-langkah sistematis untuk menemukan data tertentu dalam kumpulan data.

**Dua algoritma pencarian dasar:**
1. **Sequential Search (Linear Search)** — cek satu per satu dari awal (data tidak perlu terurut)
2. **Binary Search** — belah data jadi dua (data harus terurut) — pertemuan 5

---

### B. SEQUENTIAL SEARCH

#### Cara Kerja

Sequential search bekerja dengan **memeriksa setiap elemen satu per satu** dari awal array hingga:
- **Target ditemukan** → kembalikan indeks
- **Array habis** → target tidak ada

#### Ilustrasi

```
Array: [10, 45, 78, 23, 56, 89, 12, 34]
Cari: 56

Indeks 0: 10 ≠ 56 → lanjut
Indeks 1: 45 ≠ 56 → lanjut
Indeks 2: 78 ≠ 56 → lanjut
Indeks 3: 23 ≠ 56 → lanjut
Indeks 4: 56 = 56 → KETEMU! (indeks 4)
```

```
Cari: 99

Indeks 0: 10 ≠ 99 → lanjut
Indeks 1: 45 ≠ 99 → lanjut
...
Indeks 7: 34 ≠ 99 → lanjut
Selesai: 99 TIDAK DITEMUKAN
```

#### Pseudocode

```
PROCEDURE sequentialSearch(arr, target)
    FOR i FROM 0 TO length(arr) - 1
        IF arr[i] == target THEN
            RETURN i          // Ditemukan
        ENDIF
    ENDFOR
    RETURN -1                 // Tidak ditemukan
END PROCEDURE
```

---

### C. KASUS TERBAIK, TERBURUK, RATA-RATA

| Kasus | Terjadi Ketika | Langkah |
|---|---|---|
| **Terbaik** | Target di posisi pertama | 1 langkah |
| **Terburuk** | Target di posisi terakhir / tidak ada | n langkah |
| **Rata-rata** | Target di posisi tengah | n/2 langkah |

**Notasi Big O: O(n)** — waktu berbanding lurus dengan jumlah data.

| Jumlah Data (n) | Maks Langkah |
|---|---|
| 10 | 10 |
| 100 | 100 |
| 1.000 | 1.000 |
| 1.000.000 | 1.000.000 |

---

### D. KELEBIHAN & KEKURANGAN

| Kelebihan | Kekurangan |
|---|---|
| Sangat sederhana — mudah dipahami | Lambat untuk data besar (O(n)) |
| Data tidak perlu diurutkan | Tidak efisien — bisa cek semua data |
| Cocok untuk data kecil (< 100) | Binary search lebih cepat (O(log n)) |
| Bisa diterapkan di berbagai tipe data | Butuh banyak perbandingan |

#### Kapan Pakai Sequential Search?

| Situasi | Pakai Sequential? |
|---|---|
| Data hanya 10–20 elemen | ✅ Ya |
| Data tidak terurut | ✅ Ya |
| Data 1 juta elemen | ❌ Tidak — cari binary search |
| Pencarian dilakukan sekali | ✅ Ya |
| Pencarian dilakukan berulang | ❌ Tidak — urutkan dulu, pakai binary |

---

### E. SEQUENTIAL SEARCH DI PYTHON

```python
def sequential_search(arr, target):
    for i in range(len(arr)):
        if arr[i] == target:
            return i          # Ditemukan di indeks i
    return -1                 # Tidak ditemukan

# Contoh penggunaan
nilai = [15, 82, 37, 91, 44, 53, 68, 29, 76, 10]
cari = 91

hasil = sequential_search(nilai, cari)
if hasil != -1:
    print(f"{cari} ditemukan di indeks {hasil}")
else:
    print(f"{cari} tidak ditemukan")
```

**Output:**
```
91 ditemukan di indeks 3
```

---

### F. CONTOH SEQUENTIAL SEARCH DI KEHIDUPAN

| Situasi | Cara Kerja |
|---|---|
| Mencari buku di rak | Lihat satu per satu sampai ketemu |
| Mencari nomor kontak HP | Scroll daftar kontak dari atas |
| Mencari kunci di rumah | Cek satu per satu tempat |
| Mencari file di komputer | Buka folder satu per satu |
| Mencari kata di kamus cetak | Buka halaman satu per satu (kalau tidak pakai indeks) |

---

### G. RANGKUMAN

1. **Sequential search** = cari data dengan cek satu per satu dari awal
2. **O(n)** — waktu linear terhadap jumlah data
3. **Mudah**, data tidak perlu terurut, tapi **lambat** untuk data besar
4. Python: `sequential_search(arr, target)` — return indeks atau -1

---

**MGMP Informatika SMAN 6 Cimahi**
