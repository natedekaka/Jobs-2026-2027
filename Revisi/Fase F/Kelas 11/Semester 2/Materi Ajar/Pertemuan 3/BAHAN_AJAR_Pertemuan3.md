# BAHAN AJAR – PERTEMUAN 3 (S2)
## Operator
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*



### 🧠 Memahami — Membangun Pemahaman Awal

## A. Tujuan Pembelajaran
Setelah mempelajari materi ini, siswa mampu:
1. Menggunakan operator aritmatika (+, -, *, /, //, %, **)
2. Menggunakan operator perbandingan (==, !=, >, <, >=, <=)
3. Menggunakan operator logika (and, or, not)
4. Memahami prioritas operator (urutan eksekusi)

## B. Operator Aritmatika
| Operator | Nama | Contoh | Hasil |
|----------|------|--------|-------|
| + | Penjumlahan | 10 + 3 | 13 |
| - | Pengurangan | 10 - 3 | 7 |
| * | Perkalian | 10 * 3 | 30 |
| / | Pembagian (float) | 10 / 3 | 3.33 |
| // | Pembagian bulat | 10 // 3 | 3 |
| % | Modulus (sisa bagi) | 10 % 3 | 1 |
| ** | Pangkat | 10 ** 3 | 1000 |

```python
a, b = 15, 4
print(a + b)   # 19
print(a - b)   # 11
print(a * b)   # 60
print(a / b)   # 3.75
print(a // b)  # 3
print(a % b)   # 3 (15 = 4*3 + 3)
print(a ** b)  # 50625
```

**Kegunaan Modulus:**
- Cek genap/ganjil: n % 2 == 0 → genap
- Cek kelipatan: n % 5 == 0 → kelipatan 5

## C. Operator Penugasan
```python
x = 10
x += 5    # x = 15
x -= 3    # x = 12
x *= 2    # x = 24
x /= 4    # x = 6.0
```

## D. Operator Perbandingan
| Operator | Arti | Contoh |
|----------|------|--------|
| == | Sama dengan | 5 == 5 True |
| != | Tidak sama | 5 != 3 True |
| > | Lebih besar | 5 > 3 True |
| < | Lebih kecil | 5 < 3 False |
| >= | Lebih besar/sama | 5 >= 5 True |
| <= | Lebih kecil/sama | 5 <= 3 False |

## E. Operator Logika
```python
print(True and True)    # True
print(True and False)   # False
print(True or False)    # True
print(not True)         # False

usia = 17
nilai = 80
print(usia >= 16 and nilai >= 70)  # True
```

## F. Prioritas Operator
1. () — kurung
2. ** — pangkat
3. *, /, //, % — perkalian, pembagian
4. +, - — penjumlahan, pengurangan
5. <, <=, >, >=, ==, != — perbandingan
6. not, and, or — logika

```python
print(5 + 3 * 2)         # 11
print((5 + 3) * 2)       # 16
print(10 - 2 ** 3)       # 2
```


### 🔧 Mengaplikasi — Praktik & Penerapan

## G. Latihan
1. Hitung: 10 + 5 * 2, (10 + 5) * 2, 2 ** 3 + 4, 15 // 4
2. Input 2 angka → tampilkan semua operasi aritmatika
3. Cek bilangan genap: input angka → print Genap/Ganjil
4. Cek kelulusan: input nilai → print True jika >= 70
5. Tebak hasil: 4 + 3 * 2 > 10 or 5 == 5


### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagaimana konsep ini terkait dengan materi sebelumnya?
- Skala pemahaman diri: ___/10
- Apa yang ingin kamu pelajari lebih lanjut?

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) S2 Pert 3**
