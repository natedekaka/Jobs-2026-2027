# BAHAN AJAR – PERTEMUAN 6 (S2)
## List & Tuple
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*



### 🧠 Memahami — Membangun Pemahaman Awal

## A. Tujuan Pembelajaran
Setelah mempelajari materi ini, siswa mampu:
1. Membuat dan mengakses list (CRUD: Create, Read, Update, Delete)
2. Menggunakan method list (append, remove, sort, pop)
3. Membedakan list dan tuple
4. Mengoperasikan tuple sebagai data tetap

## B. List — Kumpulan Data
List adalah tipe data yang menyimpan banyak nilai dalam satu variabel. List bersifat mutable (bisa diubah).

```python
buah = ["apel", "mangga", "jeruk"]     # list string
angka = [1, 2, 3, 4, 5]                # list integer
campur = ["Andi", 17, 165.5, True]     # list campuran
```

## C. Indexing — Mengakses Elemen
Indeks dimulai dari 0:
```python
buah = ["apel", "mangga", "jeruk", "anggur", "pisang"]
print(buah[0])    # apel
print(buah[-1])   # pisang (indeks negatif = dari belakang)
```

| Index | 0 | 1 | 2 | 3 | 4 |
|-------|---|---|---|---|---|
| Value | apel | mangga | jeruk | anggur | pisang |

## D. Slicing — Memotong List
```python
print(buah[1:4])     # [mangga, jeruk, anggur]
print(buah[:3])      # [apel, mangga, jeruk]
print(buah[2:])      # [jeruk, anggur, pisang]
print(buah[::2])     # [apel, jeruk, pisang]
print(buah[::-1])    # dibalik
```

## E. Method List
```python
buah.append("durian")        # tambah di akhir
buah.insert(1, "semangka")   # tambah di indeks 1
buah.remove("jeruk")         # hapus berdasarkan nilai
buah.pop()                   # ambil & hapus terakhir
buah.sort()                  # urutkan A-Z
print(len(buah))             # panjang list
print(buah.count("apel"))    # hitung kemunculan
```

## F. Loop dengan List
```python
# Loop nilai
for b in buah:
    print(b)

# Loop indeks
for i in range(len(buah)):
    print(f"Index {i}: {buah[i]}")

# Enumerate
for i, b in enumerate(buah):
    print(f"{i}: {b}")
```

## G. List Comprehension
```python
kuadrat = [i**2 for i in range(1, 11)]
print(kuadrat)  # [1, 4, 9, ..., 100]

genap = [i for i in range(1, 21) if i % 2 == 0]
print(genap)    # [2, 4, 6, ..., 20]
```

## H. Tuple — Data Tetap
Tuple seperti list, tapi immutable (tidak bisa diubah).
```python
warna = ("merah", "kuning", "hijau")
warna[0] = "biru"  # ERROR: TypeError!
```

**Kapan pakai tuple?** Data konstanta, return function, faster than list.


### 🔧 Mengaplikasi — Praktik & Penerapan

## I. Latihan
1. Buat list 5 nama teman → cetak satu per satu
2. Tambah 2 nama, hapus 1, urutkan A-Z
3. Input 5 angka → simpan di list → cetak total dan rata-rata
4. List comprehension: bilangan genap 1-50
5. Buat tuple hari dalam seminggu


### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagaimana konsep ini terkait dengan materi sebelumnya?
- Skala pemahaman diri: ___/10
- Apa yang ingin kamu pelajari lebih lanjut?

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) S2 Pert 6**
