# BAHAN AJAR – PERTEMUAN 5 (S2)
## FOR & WHILE — Perulangan
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Analisis Data & Algoritma Pemrograman (AP) |
| **Tujuan Pembelajaran** | Menggunakan perulangan `for` dan `while`, menerapkan `break`/`continue`, serta membedakan kedua jenis perulangan |
| **Materi Prasyarat** | Variabel, Tipe Data, Operator, dan Percabangan (Pertemuan 2-4) |

---

## A. Kisah Pemantik 🎬

> **"Penjaga Taman Bermain"**
>
> Pak Rudi menghitung pengunjung taman bermain setiap akhir pekan. Menghitung satu per satu dari pengunjung pertama sampai terakhir melelahkan, padahal polanya sama setiap waktu: "hitung satu, lalu lanjut ke pengunjung berikutnya." Seandainya ada mesin yang mengulang pekerjaan itu secara otomatis — itulah **perulangan (loop)**.
>
> Dalam Python, `for` mengulang sejumlah tertentu (seperti menghitung 1 sampai 100), sedangkan `while` mengulang **selama kondisi masih benar** (seperti menjaga pintu tetap terbuka selagi pengunjung datang).
>
> **Pertanyaan pemantik:** Apa yang terjadi jika mesin penghitung Pak Rudi tidak pernah berhenti? Bagaimana kaitannya dengan "infinite loop" dalam pemrograman?

---

## B. Perulangan FOR dengan `range()` 🔁

`for` mengulang blok kode untuk setiap nilai dalam sebuah urutan.

```python
for i in range(5):         # 0, 1, 2, 3, 4
    print(i)
```

**Output:**
```
0
1
2
3
4
```

**Variasi `range()`:**

```python
for i in range(1, 6):          # mulai 1, berhenti sebelum 6
    print(i, end=" ")          # 1 2 3 4 5
print()
for i in range(0, 10, 2):      # start, stop, step (2)
    print(i, end=" ")          # 0 2 4 6 8
```

**Output:**
```
1 2 3 4 5
0 2 4 6 8
```

> 💡 **Ingat:** `range(stop)` berhenti **sebelum** nilai stop. `range(5)` menghasilkan `0..4`, bukan `1..5`.

---

## C. FOR dengan List & String 📋

`for` bisa mengulang elemen list atau setiap karakter string.

```python
buah = ["apel", "mangga", "jeruk"]
for b in buah:
    print("Saya suka", b)

for huruf in "Python":
    print(huruf)
```

**Output:**
```
Saya suka apel
Saya suka mangga
Saya suka jeruk
P
y
t
h
o
n
```

---

## D. Perulangan WHILE ♾️

`while` mengulang **selama kondisi bernilai `True`**. Pastikan ada pembaruan variabel agar tidak menjadi infinite loop.

```python
i = 1
while i <= 5:
    print(i)
    i += 1   # PENTING: update agar loop berhenti
```

**Output:**
```
1
2
3
4
5
```

**Hati-hati infinite loop!**

```python
i = 1
while i <= 5:
    print(i)
    # i tidak pernah bertambah -> loop berjalan selamanya!
```

> 💡 Jika programmu "macet" karena infinite loop di Colab, klik **Runtime → Interrupt execution** untuk menghentikannya.

---

## E. `break` dan `continue` 🛑

- **`break`** — menghentikan perulangan sepenuhnya.
- **`continue`** — melompati iterasi saat ini dan lanjut ke iterasi berikutnya.

```python
# break: berhenti saat i == 5
for i in range(10):
    if i == 5:
        break
    print(i)          # 0 1 2 3 4
```

**Output:**
```
0
1
2
3
4
```

```python
# continue: skip angka genap
for i in range(10):
    if i % 2 == 0:
        continue
    print(i)          # 1 3 5 7 9
```

**Output:**
```
1
3
5
7
9
```

---

## F. Loop Bersarang (Nested Loop) 🪆

Loop di dalam loop, misalnya untuk membuat tabel perkalian.

```python
for i in range(1, 4):
    for j in range(1, 4):
        print(f"{i}x{j}={i*j}", end="\t")
    print()
```

**Output:**
```
1x1=1	1x2=2	1x3=3
2x1=2	2x2=4	2x3=6
3x1=3	3x2=6	3x3=9
```

---

## G. Program Deret Bilangan 🔢

```python
# Bilangan genap 2-20
for i in range(2, 21, 2):
    print(i, end=" ")
print()

# Jumlah 1-100
total = 0
for i in range(1, 101):
    total += i
print("Jumlah 1-100:", total)
```

**Output:**
```
2 4 6 8 10 12 14 16 18 20
Jumlah 1-100: 5050
```

---

## H. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Cetak bilangan 10 sampai 1 (mundur).
**Jawaban:**
```python
for i in range(10, 0, -1):
    print(i, end=" ")
```
**Output:**
```
10 9 8 7 6 5 4 3 2 1
```

**Contoh 2:** Hitung jumlah bilangan genap dari 1 sampai 100.
**Jawaban:**
```python
total = 0
for i in range(2, 101, 2):
    total += i
print("Jumlah genap 1-100:", total)
```
**Output:**
```
Jumlah genap 1-100: 2550
```

**Contoh 3:** Buat tabel perkalian 5 (5×1 sampai 5×10).
**Jawaban:**
```python
for i in range(1, 11):
    print(f"5 x {i} = {5 * i}")
```
**Output (sebagian):**
```
5 x 1 = 5
5 x 2 = 10
...
5 x 10 = 50
```

**Contoh 4:** Cetak pola bintang menaik sebanyak 5 baris.
**Jawaban:**
```python
for i in range(1, 6):
    print("*" * i)
```
**Output:**
```
*
**
***
****
*****
```

**Contoh 5:** Tulis program tebak angka: komputer memilih 1-10, user menebak sampai benar.
**Jawaban:**
```python
import random
rahasia = random.randint(1, 10)
tebakan = 0
while tebakan != rahasia:
    tebakan = int(input("Tebak angka (1-10): "))
    if tebakan > rahasia:
        print("Terlalu besar!")
    elif tebakan < rahasia:
        print("Terlalu kecil!")
print("Benar! Angkanya", rahasia)
```

---

## I. Miskonsepsi & Kesalahan Umum 🚫

| Miskonsepsi / Kesalahan | Fakta yang Benar |
|---|---|
| "`range(5)` mencetak 1-5" | `range(5)` menghasilkan `0-4`; untuk `1-5` pakai `range(1,6)` |
| "Lupa menambahkan counter di `while`" | Tanpa update, terjadi infinite loop |
| "`break` dan `continue` sama" | `break` berhenti total; `continue` hanya melewati iterasi ini |
| "`while` bisa dipakai tanpa kondisi jelas" | `while` butuh kondisi yang akhirnya menjadi `False` |
| "Loop hanya untuk angka" | Loop juga bisa untuk list, string, dan elemen lainnya |
| "Urutan `range` harus naik" | Bisa mundur: `range(10, 0, -1)` |

---

## J. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Hitung Mundur (Mudah):** Cetak angka 10 sampai 1, lalu cetak "Go!" setelahnya.

**Tantangan 2 — Bilangan Ganjil (Sedang):** Cetak bilangan ganjil 1-20, lalu hitung jumlahnya.

**Tantangan 3 — Tabel Perkalian (Sedang):** Buat tabel perkalian 5, dari `5 x 1 = 5` sampai `5 x 10 = 50`.

**Tantangan 4 — Pola Bintang (Sulit):** Cetak pola bintang menaik 5 baris (`*` sampai `*****`), lalu pola menurun 4 baris.

**Tantangan 5 — Tebak Angka (Sulit):** Buat permainan tebak angka 1-10 dengan `while`; beri petunjuk "terlalu besar/kecil" dan berhenti saat benar.

---

## K. Rangkuman Kunci 🔑

- `for i in range(n)` mengulang `n` kali, mulai dari 0.
- `range(start, stop, step)` untuk rentang dan loncatan tertentu.
- `for` juga bisa mengulang elemen list dan string.
- `while` mengulang selama kondisi `True`; wajib memperbarui variabel kontrol.
- `break` menghentikan loop; `continue` melewati iterasi saat ini.
- Nested loop untuk pola/baris yang membutuhkan dua dimensi.
- Infinite loop dapat dihentikan lewat **Runtime → Interrupt** di Colab.

---

## L. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Loop / Perulangan** | Mengulang blok kode beberapa kali |
| **FOR** | Perulangan dengan jumlah yang diketahui |
| **WHILE** | Perulangan berdasarkan kondisi |
| **Range** | Fungsi menghasilkan urutan angka |
| **Break** | Menghentikan perulangan sepenuhnya |
| **Continue** | Melompati iterasi saat ini |
| **Infinite loop** | Perulangan yang tidak pernah berhenti |
| **Nested loop** | Perulangan di dalam perulangan |
| **Iterasi** | Satu kali putaran perulangan |

---

## M. Refleksi (Merefleksi) 🔍

- Kapan lebih tepat memakai `for` dan kapan memakai `while`?
- Mengapa pengaruh `break` dan `continue` sangat penting dalam perulangan?
- Pernahkah kamu terjebak infinite loop? Bagaimana perasaanmu saat menyadarinya?
- **Skala pemahaman diri:** ____/10
- Program perulangan apa yang ingin kamu bangun selanjutnya?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 2**