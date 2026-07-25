# BAHAN AJAR – PERTEMUAN 2 (S2)
## Variabel & Tipe Data
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*



### 🧠 Memahami — Membangun Pemahaman Awal

## A. Tujuan Pembelajaran
Setelah mempelajari materi ini, siswa mampu:
1. Menjelaskan pengertian variabel dan aturan penamaan
2. Mengidentifikasi 5+ tipe data dasar Python
3. Menggunakan fungsi type() untuk cek tipe data
4. Melakukan konversi antar tipe data

## B. Apa Itu Variabel?
Variabel adalah wadah/container untuk menyimpan data di memori. Analogi: kotak dengan label — label adalah nama variabel, isinya adalah data.

```python
nama = "Andi"       # variabel nama berisi teks "Andi"
usia = 17           # variabel usia berisi angka 17
tinggi = 165.5      # variabel float
```
Cara baca: "nama diisi dengan Andi", bukan "nama sama dengan Andi".

## C. Aturan Penamaan Variabel
1. Huruf, angka, underscore — boleh: nama, usia_siswa, nilai1
2. Tidak boleh diawali angka — 1nilai (salah), nilai1 (benar)
3. Case-sensitive — Nama tidak sama dengan nama
4. Tidak boleh pakai spasi — usia_siswa, bukan usia siswa
5. Tidak boleh pakai keyword Python — if, for, while, True, False
6. Konvensi: snake_case — kata dipisah underscore

## D. Tipe Data Dasar
| Tipe | Contoh | Penjelasan |
|------|--------|------------|
| int | 17, 0, -5 | Bilangan bulat |
| float | 3.14, 2.0, -0.5 | Bilangan desimal |
| str | "Halo", 'Python' | Teks (string) |
| bool | True, False | Boolean |
| NoneType | None | Tidak ada nilai |

## E. Cek Tipe Data dengan type()
```python
nama = "Andi"
usia = 17
print(type(nama))    # <class 'str'>
print(type(usia))    # <class 'int'>
```

## F. Operasi String
```python
# Penggabungan
nama_d = "Andi"
nama_b = "Prasetyo"
nama_l = nama_d + " " + nama_b
print(nama_l)        # Andi Prasetyo

# Perkalian string
print("Ha" * 3)      # HaHaHa

# Panjang string
print(len("Python")) # 6

# Ubah case
print("python".upper())  # PYTHON
print("PYTHON".lower())  # python
```

## G. Konversi Tipe Data (Casting)
```python
# String ke Integer
umur_str = "17"
umur_int = int(umur_str)
print(umur_int + 3)      # 20

# Integer ke String
tahun = 2025
print("Tahun " + str(tahun))  # Tahun 2025

# Float ke Integer
pi = 3.14
print(int(pi))            # 3
```

## H. Input dari User
```python
nama = input("Siapa namamu? ")
print("Halo, " + nama + "!")
usia = input("Berapa usiamu? ")
print("Tahun depan kamu", int(usia) + 1, "tahun")
```


### 🔧 Mengaplikasi — Praktik & Penerapan

## I. Latihan
1. Buat variabel: nama, kelas, usia, hobi — lalu print semua
2. Cek tipe data dari 5 variabel berbeda
3. Minta user input nama dan usia → cetak "Halo [nama], usia [usia]"
4. Konversi suhu: input Celsius → output Fahrenheit (F = C * 9/5 + 32)
5. Buat program: input 2 angka → cetak hasil penjumlahan


### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagaimana konsep ini terkait dengan materi sebelumnya?
- Skala pemahaman diri: ___/10
- Apa yang ingin kamu pelajari lebih lanjut?

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) S2 Pert 2**
