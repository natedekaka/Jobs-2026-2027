# BAHAN AJAR – PERTEMUAN 6 (S2)
## List & Tuple
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Analisis Data & Algoritma Pemrograman (AP) |
| **Tujuan Pembelajaran** | Membuat dan mengakses list, memakai method list, membedakan list dan tuple, serta mengolah tuple sebagai data tetap |
| **Materi Prasyarat** | Variabel, Operator, Percabangan, dan Perulangan (Pertemuan 2-5) |

---

## A. Kisah Pemantik 🎬

> **"Keranjang Belanja"**
>
> Saat berbelanja, Bu Dewi memasukkan banyak barang ke dalam satu keranjang. Keranjang itu bisa diisi barang baru, barang bisa dibuang, atau diambil untuk dibayar. Namun daftar **harga tetap** (seperti tarif pajak) tidak boleh berubah — ia hanya untuk dibaca.
>
> Dalam Python, **list** ibarat keranjang belanja: bisa diubah, ditambah, dan dikurangi. Sedangkan **tuple** ibarat daftar tetap: nilainya tidak bisa diubah setelah dibuat.
>
> **Pertanyaan pemantik:** Kapan kamu membutuhkan wadah data yang bisa diubah, dan kapan kamu membutuhkan data yang tidak boleh berubah? Berikan contoh keduanya dari kehidupan sehari-hari!

---

## B. List — Kumpulan Data 📋

**List** adalah tipe data yang menyimpan banyak nilai dalam satu variabel. List bersifat **mutable** (bisa diubah).

```python
buah = ["apel", "mangga", "jeruk"]     # list string
angka = [1, 2, 3, 4, 5]                # list integer
campur = ["Andi", 17, 165.5, True]     # list campuran
```

| Istilah | Arti |
|---|---|
| **List** | Kumpulan data yang bisa diubah (mutable) |
| **Tuple** | Kumpulan data yang tidak bisa diubah (immutable) |
| **Index** | Posisi elemen dalam list, dimulai dari 0 |
| **Slicing** | Memotong/mengambil bagian list |
| **Method** | Fungsi bawaan yang dimiliki list (misal `append`) |

---

## C. Indexing — Mengakses Elemen 🔢

Indeks list **dimulai dari 0**. Indeks negatif membaca dari belakang.

```python
buah = ["apel", "mangga", "jeruk", "anggur", "pisang"]
print(buah[0])     # apel
print(buah[-1])    # pisang (dari belakang)
print(buah[2])     # jeruk
```

**Output:**
```
apel
pisang
jeruk
```

| Index | 0 | 1 | 2 | 3 | 4 |
|---|---|---|---|---|---|
| Value | apel | mangga | jeruk | anggur | pisang |

> 💡 **Ingat:** elemen terakhir ada di indeks `len(buah) - 1`, bukan `len(buah)`.

---

## D. Slicing — Memotong List ✂️

```python
buah = ["apel", "mangga", "jeruk", "anggur", "pisang"]
print(buah[1:4])     # dari index 1 sampai sebelum 4
print(buah[:3])      # dari awal sampai sebelum 3
print(buah[2:])      # dari index 2 sampai akhir
print(buah[::2])     # ambil setiap 2 langkah
print(buah[::-1])    # dibalik
```

**Output:**
```
['mangga', 'jeruk', 'anggur']
['apel', 'mangga', 'jeruk']
['jeruk', 'anggur', 'pisang']
['apel', 'jeruk', 'pisang']
['pisang', 'anggur', 'jeruk', 'mangga', 'apel']
```

---

## E. Method List 🛠️

```python
buah = ["apel", "mangga", "jeruk"]
buah.append("durian")          # tambah di akhir
print(buah)                    # ['apel', 'mangga', 'jeruk', 'durian']

buah.insert(1, "semangka")     # tambah di index 1
print(buah)                    # ['apel', 'semangka', 'mangga', 'jeruk', 'durian']

buah.remove("jeruk")           # hapus berdasarkan nilai
buah.pop()                     # ambil & hapus elemen terakhir
print(buah)                    # ['apel', 'semangka', 'mangga']

buah.sort()                    # urutkan A-Z
print(buah)                    # ['apel', 'mangga', 'semangka']

print(len(buah))               # 3
print(buah.count("apel"))      # 1
```

**Output:**
```
['apel', 'mangga', 'jeruk', 'durian']
['apel', 'semangka', 'mangga', 'jeruk', 'durian']
['apel', 'semangka', 'mangga']
['apel', 'mangga', 'semangka']
3
1
```

---

## F. Loop dengan List 🔁

```python
buah = ["apel", "mangga", "jeruk"]

# Loop nilai
for b in buah:
    print(b)

# Loop indeks
for i in range(len(buah)):
    print(f"Index {i}: {buah[i]}")

# Enumerate (indeks + nilai sekaligus)
for i, b in enumerate(buah):
    print(f"{i}: {b}")
```

**Output:**
```
apel
mangga
jeruk
Index 0: apel
Index 1: mangga
Index 2: jeruk
0: apel
1: mangga
2: jeruk
```

---

## G. List Comprehension 🎯

Cara singkat membuat list berdasarkan aturan tertentu.

```python
kuadrat = [i**2 for i in range(1, 11)]
print(kuadrat)

genap = [i for i in range(1, 21) if i % 2 == 0]
print(genap)
```

**Output:**
```
[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
[2, 4, 6, 8, 10, 12, 14, 16, 18, 20]
```

---

## H. Tuple — Data Tetap 🔒

Tuple mirip list, tetapi **immutable** (tidak bisa diubah setelah dibuat).

```python
warna = ("merah", "kuning", "hijau")
print(warna[0])     # merah

# warna[0] = "biru"  # ERROR: TypeError (tuple tidak bisa diubah)
```

**Kapan memakai tuple?** Saat data bersifat konstan (tidak boleh berubah), misalnya hari dalam seminggu, nama bulan, atau koordinat tetap. Tuple juga lebih ringan dan lebih cepat daripada list.

```python
hari = ("Senin", "Selasa", "Rabu", "Kamis", "Jumat", "Sabtu", "Minggu")
print(len(hari))       # 7
print(hari[2])         # Rabu
```

**Output:**
```
7
Rabu
```

---

## I. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Buat list berisi 5 nama teman, lalu cetak satu per satu.
**Jawaban:**
```python
teman = ["Andi", "Budi", "Citra", "Dewi", "Eka"]
for nama in teman:
    print(nama)
```
**Output:**
```
Andi
Budi
Citra
Dewi
Eka
```

**Contoh 2:** Input 5 angka, simpan ke list, lalu cetak total dan rata-rata.
**Jawaban:**
```python
angka = []
for i in range(5):
    angka.append(int(input(f"Angka ke-{i+1}: ")))
total = sum(angka)
print("List:", angka)
print("Total:", total)
print("Rata-rata:", total / len(angka))
```
**Output (jika input 4, 6, 8, 10, 12):**
```
List: [4, 6, 8, 10, 12]
Total: 40
Rata-rata: 8.0
```

**Contoh 3:** Jelaskan perbedaan list dan tuple beserta contoh penggunaannya.
**Jawaban:** List bersifat mutable (bisa diubah dengan `append`, `remove`, dsb.), cocok untuk data dinamis seperti daftar tugas. Tuple bersifat immutable (tidak bisa diubah), cocok untuk data tetap seperti hari dalam seminggu atau nilai konstanta. Mengubah tuple akan memunculkan `TypeError`.

**Contoh 4:** Tulis list comprehension untuk mendapatkan bilangan genap dari 1 sampai 50.
**Jawaban:**
```python
genap = [i for i in range(1, 51) if i % 2 == 0]
print(genap)
```
**Output (sebagian):**
```
[2, 4, 6, 8, 10, ..., 50]
```

---

## J. Miskonsepsi & Kesalahan Umum 🚫

| Miskonsepsi / Kesalahan | Fakta yang Benar |
|---|---|
| "Indeks list dimulai dari 1" | Indeks dimulai dari **0** |
| "`buah[5]` mengambil elemen ke-5" | Untuk 5 elemen, indeks valid adalah `0-4`; `buah[5]` menghasilkan `IndexError` |
| "List dan tuple sama saja" | List mutable, tuple immutable |
| "Tuple tidak bisa diakses per elemen" | Tuple tetap bisa diakses dengan index, hanya tidak bisa diubah |
| "`sort()` mengubah sementara" | `sort()` mengubah list secara permanen |
| "List hanya bisa satu tipe data" | List bisa berisi campuran tipe (`int`, `str`, `bool`) |

---

## K. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Daftar Teman (Mudah):** Buat list 5 nama teman, cetak satu per satu, lalu tambahkan 2 nama dan urutkan A-Z.

**Tantangan 2 — Statistik Angka (Sedang):** Input 5 angka ke list, lalu cetak total, rata-rata, nilai terbesar (`max()`), dan terkecil (`min()`).

**Tantangan 3 — List Comprehension (Sedang):** Buat list kuadrat angka 1-10 dan list bilangan genap 1-50 memakai list comprehension.

**Tantangan 4 — Tuple Hari (Sulit):** Buat tuple 7 hari dalam seminggu. Cetak hari ke-3, hari terakhir, dan panjang tuple. Coba ubah salah satu elemen — catat pesan errornya.

**Tantangan 5 — Analisis Nilai (Sulit):** Input nilai 5 siswa ke list, tentukan yang lulus (≥70) dan tampilkan daftarnya.

---

## L. Rangkuman Kunci 🔑

- **List** = kumpulan data mutable, dibuat dengan `[ ]`.
- Indeks dimulai dari **0**; indeks negatif membaca dari belakang.
- Slicing `[start:stop:step]` untuk mengambil bagian list.
- Method list: `append`, `insert`, `remove`, `pop`, `sort`, `len`, `count`.
- **List comprehension**: `[ekspresi for item in iterable if kondisi]`.
- **Tuple** = kumpulan data immutable, dibuat dengan `( )`.
- Gunakan tuple untuk data tetap; gunakan list untuk data yang berubah.

---

## M. Glosarium 📖

| Istilah | Arti |
|---|---|
| **List** | Kumpulan data yang bisa diubah, ditulis dengan `[ ]` |
| **Tuple** | Kumpulan data tetap, ditulis dengan `( )` |
| **Mutable** | Bisa diubah setelah dibuat |
| **Immutable** | Tidak bisa diubah setelah dibuat |
| **Index** | Posisi elemen, dimulai dari 0 |
| **Slicing** | Mengambil bagian list berdasarkan rentang |
| **Method** | Fungsi bawaan yang dimiliki list/tuple |
| **List comprehension** | Cara ringkas membuat list |

---

## N. Refleksi (Merefleksi) 🔍

- Kapan kamu lebih memilih list dibanding tuple, dan sebaliknya?
- Apa manfaat memahami indexing dan slicing dalam mengelola data?
- Kesalahan apa yang sering muncul saat mengakses elemen list?
- **Skala pemahaman diri:** ____/10
- Apa yang ingin kamu olah lebih lanjut dengan list dan tuple?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 2**