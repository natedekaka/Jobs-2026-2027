# BAHAN AJAR – PERTEMUAN 3 (S2)
## Operator
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Informasi | Keterangan |
|---|---|
| **Fase / Kelas** | F / Kelas XI |
| **Alokasi Waktu** | 5 JP × 45 menit (225 menit) |
| **Elemen CP** | Analisis Data & Algoritma Pemrograman (AP) |
| **Tujuan Pembelajaran** | Menggunakan operator aritmatika, penugasan, perbandingan, dan logika; memahami prioritas operator |
| **Materi Prasyarat** | Variabel & Tipe Data (Pertemuan 2) |

---

## A. Kisah Pemantik 🎬

> **"Kalkulator Kasir Bu Sari"**
>
> Bu Sari ingin kasirnya menghitung total belanja otomatis: harga dikali jumlah, lalu dipotong diskon, kemudian dibagi rata ke beberapa pembeli. Ia menyadari bahwa urutan perhitungan sangat menentukan: *apakah diskon dihitung sebelum atau sesudah pajak?* Kalau salah urutan, hasilnya beda jauh!
>
> Di Python, operasi matematika dilakukan dengan **operator** (+, -, *, /, dsb.) dan mengikuti **urutan prioritas**. Memahami operator seperti memahami aturan main kalkulator: tahu kapan menambah, mengurang, atau membandingkan.
>
> **Pertanyaan pemantik:** Mengapa `5 + 3 * 2` menghasilkan 11, bukan 16? Apa yang terjadi jika kita memakai tanda kurung?

---

## B. Operator Aritmatika ➕➖✖️➗

| Operator | Nama | Contoh | Hasil |
|---|---|---|---|
| `+` | Penjumlahan | `10 + 3` | `13` |
| `-` | Pengurangan | `10 - 3` | `7` |
| `*` | Perkalian | `10 * 3` | `30` |
| `/` | Pembagian (float) | `10 / 3` | `3.333...` |
| `//` | Pembagian bulat | `10 // 3` | `3` |
| `%` | Modulus (sisa bagi) | `10 % 3` | `1` |
| `**` | Pangkat | `10 ** 3` | `1000` |

```python
a, b = 15, 4
print(a + b)    # 19
print(a - b)    # 11
print(a * b)    # 60
print(a / b)    # 3.75
print(a // b)   # 3
print(a % b)    # 3  -> karena 15 = 4 * 3 + 3
print(a ** b)   # 50625
```

**Output:**
```
19
11
60
3.75
3
3
50625
```

**Kegunaan praktis modulus (`%`):**
- Cek genap/ganjil: `n % 2 == 0` → genap.
- Cek kelipatan: `n % 5 == 0` → kelipatan 5.
- Mengambil sisa pembagian untuk masalah sehari-hari (misal membagi permen).

> 💡 **Perbedaan `/` dan `//`:** `/` selalu menghasilkan float (`7 / 2 = 3.5`), sedangkan `//` membulatkan ke bawah (`7 // 2 = 3`).

---

## C. Operator Penugasan 🎛️

Operator penugasan menggabungkan `=` dengan operasi lain untuk memperbarui nilai variabel.

```python
x = 10
x += 5    # x = 15   (x = x + 5)
x -= 3    # x = 12
x *= 2    # x = 24
x /= 4    # x = 6.0
print(x)  # 6.0
```

**Output:**
```
6.0
```

| Operator | Arti | Contoh | Hasil |
|---|---|---|---|
| `+=` | Tambah lalu simpan | `x += 1` | `x = x + 1` |
| `-=` | Kurang lalu simpan | `x -= 1` | `x = x - 1` |
| `*=` | Kali lalu simpan | `x *= 2` | `x = x * 2` |
| `/=` | Bagi lalu simpan | `x /= 2` | `x = x / 2` |

---

## D. Operator Perbandingan ⚖️

Operator perbandingan membandingkan dua nilai dan menghasilkan **`True` atau `False`**.

```python
print(5 == 5)   # True   (sama dengan)
print(5 != 3)   # True   (tidak sama dengan)
print(5 > 3)    # True   (lebih besar)
print(5 < 3)    # False  (lebih kecil)
print(5 >= 5)   # True   (lebih besar atau sama)
print(5 <= 3)   # False  (lebih kecil atau sama)
```

**Output:**
```
True
True
True
False
True
False
```

> 💡 **Ingat:** `==` untuk membandingkan, `=` untuk menugaskan. Ini salah satu kesalahan paling umum bagi pemula!

---

## E. Operator Logika 🧠

Operator logika menggabungkan beberapa kondisi menjadi satu keputusan.

```python
print(True and True)    # True
print(True and False)   # False
print(True or False)    # True
print(not True)         # False

usia = 17
nilai = 80
print(usia >= 16 and nilai >= 70)   # True
print(usia >= 18 or nilai >= 85)    # False
```

**Output:**
```
True
False
True
False
True
False
```

| Operator | Fungsi | Aturan |
|---|---|---|
| `and` | Dan | Benar hanya jika kedua kondisi benar |
| `or` | Atau | Benar jika salah satu kondisi benar |
| `not` | Negasi | Membalik nilai (`True` → `False`) |

---

## F. Prioritas Operator 🥇

Urutan eksekusi operator (dari yang paling dahulu):

1. `()` — tanda kurung
2. `**` — pangkat
3. `*`, `/`, `//`, `%` — perkalian & pembagian
4. `+`, `-` — penjumlahan & pengurangan
5. `==`, `!=`, `>`, `<`, `>=`, `<=` — perbandingan
6. `not`, `and`, `or` — logika

```python
print(5 + 3 * 2)       # 11  (kali dulu)
print((5 + 3) * 2)     # 16  (kurung dulu)
print(10 - 2 ** 3)     # 2   (pangkat dulu: 8)
print(4 + 3 * 2 > 10 or 5 == 5)  # True
```

**Output:**
```
11
16
2
True
```

---

## G. Contoh Soal & Penyelesaian 📝

**Contoh 1:** Tentukan output dari `print(15 // 4)` dan `print(15 % 4)`.
**Jawaban:** `15 // 4 = 3` (hasil bagi bulat), `15 % 4 = 3` (sisa bagi, karena `15 = 4*3 + 3`).

**Contoh 2:** Tulis program yang menerima dua angka dan menampilkan semua operasi aritmatika dasar.
**Jawaban:**
```python
a = float(input("Angka pertama: "))
b = float(input("Angka kedua: "))
print(f"{a} + {b} = {a + b}")
print(f"{a} - {b} = {a - b}")
print(f"{a} * {b} = {a * b}")
print(f"{a} / {b} = {a / b}")
```
**Output (jika input 10 dan 4):**
```
10.0 + 4.0 = 14.0
10.0 - 4.0 = 6.0
10.0 * 4.0 = 40.0
10.0 / 4.0 = 2.5
```

**Contoh 3:** Buat program yang memeriksa apakah sebuah angka genap atau ganjil memakai operator modulus.
**Jawaban:**
```python
n = int(input("Masukkan angka: "))
if n % 2 == 0:
    print(n, "adalah bilangan genap")
else:
    print(n, "adalah bilangan ganjil")
```
**Output (jika input 7):**
```
7 adalah bilangan ganjil
```

**Contoh 4:** Evaluasi `(2 + 3) * 4 ** 2 // 5` dan jelaskan urutannya.
**Jawaban:** Kurung dulu: `(2+3)=5`. Pangkat: `4**2=16`. Lalu `5 * 16 = 80`. Terakhir `80 // 5 = 16`. Jadi hasilnya `16`.

**Contoh 5:** Buat ekspresi logika untuk mengecek kelulusan: lulus jika nilai ≥ 70 **dan** kehadiran ≥ 80%.
**Jawaban:**
```python
nilai = 75
hadir = 90
lulus = nilai >= 70 and hadir >= 80
print(lulus)   # True
```

---

## H. Miskonsepsi & Kesalahan Umum 🚫

| Miskonsepsi / Kesalahan | Fakta yang Benar |
|---|---|
| "`/` selalu menghasilkan bilangan bulat" | `/` menghasilkan float; pakai `//` untuk pembagian bulat |
| "`=` dan `==` sama" | `=` menugaskan, `==` membandingkan |
| "Perkalian dihitung setelah penjumlahan" | `*`, `/`, `//`, `%` dihitung sebelum `+`, `-` |
| "`or` berarti satu saja boleh salah" | `or` benar jika salah satu benar; `and` harus keduanya benar |
| "Modulus itu sisa koma" | `%` adalah sisa **pembagian bulat**, bukan nilai desimal |
| "`x += 1` dan `x = x + 1` berbeda" | Keduanya identik |

---

## I. Tantangan Praktik (Mengaplikasi) 🎯

**Tantangan 1 — Hitung Cepat (Mudah):** Prediksi hasil, lalu verifikasi dengan Python: `10 + 5 * 2`, `(10 + 5) * 2`, `2 ** 3 + 4`, `15 // 4`, `15 % 4`.

**Tantangan 2 — Kalkulator Dua Angka (Sedang):** Input dua angka, tampilkan hasil `+`, `-`, `*`, `/`, `//`, `%`, dan `**`.

**Tantangan 3 — Cek Genap/Ganjil (Sedang):** Input sebuah angka dan cetak "Genap" atau "Ganjil" memakai `%`.

**Tantangan 4 — Cek Kelulusan (Sulit):** Input nilai dan kehadiran, lalu cetak `True`/`False` untuk kelulusan (`nilai ≥ 70 and hadir ≥ 80`). Tambahkan pesan yang menjelaskan alasannya.

**Tantangan 5 — Ekspresi Majemuk (Sulit):** Tebak output `4 + 3 * 2 > 10 or 5 == 5`, lalu buktikan dengan Python dan jelaskan langkah prioritasnya.

---

## J. Rangkuman Kunci 🔑

- Operator aritmatika: `+`, `-`, `*`, `/`, `//`, `%`, `**`.
- `/` menghasilkan float, `//` pembulatan ke bawah, `%` sisa bagi.
- Operator penugasan: `+=`, `-=`, `*=`, `/=` untuk memperbarui nilai variabel.
- Operator perbandingan menghasilkan `True`/`False`.
- Operator logika: `and` (keduanya), `or` (salah satu), `not` (negasi).
- Prioritas: kurung → pangkat → kali/bagi → tambah/kurang → perbandingan → logika.

---

## K. Glosarium 📖

| Istilah | Arti |
|---|---|
| **Operator** | Simbol yang melakukan operasi pada nilai |
| **Aritmatika** | Operasi matematika dasar (+, -, *, /) |
| **Modulus** | Sisa pembagian bulat (`%`) |
| **Floor division** | Pembagian yang dibulatkan ke bawah (`//`) |
| **Pangkat** | Operasi eksponen (`**`) |
| **Penugasan** | Memberi/memperbarui nilai variabel |
| **Perbandingan** | Membandingkan dua nilai menjadi `True`/`False` |
| **Logika** | `and`, `or`, `not` untuk menggabungkan kondisi |
| **Prioritas** | Urutan eksekusi operator dalam sebuah ekspresi |

---

## L. Refleksi (Merefleksi) 🔍

- Mengapa urutan prioritas operator penting untuk menghasilkan perhitungan yang benar?
- Di kehidupan sehari-hari, kapan kamu perlu memutuskan dengan dua syarat sekaligus (analog `and`/`or`)?
- Kesalahan apa yang paling sering kamu lakukan saat menulis operator, dan bagaimana mengatasinya?
- **Skala pemahaman diri:** ____/10
- Apa yang ingin kamu eksplorasi lebih lanjut tentang operator?

---

**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 2**