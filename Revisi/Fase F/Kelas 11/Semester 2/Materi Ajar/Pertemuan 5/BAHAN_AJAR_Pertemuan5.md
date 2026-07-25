# BAHAN AJAR – PERTEMUAN 5 (S2)
## FOR & WHILE — Perulangan
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*



### 🧠 Memahami — Membangun Pemahaman Awal

## A. Tujuan Pembelajaran
Setelah mempelajari materi ini, siswa mampu:
1. Menggunakan FOR loop untuk perulangan dengan range
2. Menggunakan WHILE loop untuk perulangan dengan kondisi
3. Menggunakan break dan continue
4. Membedakan loop FOR dan WHILE

## B. FOR Loop dengan range()
```python
for i in range(5):       # 0, 1, 2, 3, 4
    print(i)
for i in range(1, 6):    # 1, 2, 3, 4, 5
    print(i)
for i in range(0, 10, 2): # 0, 2, 4, 6, 8
    print(i)
```

## C. FOR Loop dengan List/String
```python
buah = ["apel", "mangga", "jeruk"]
for b in buah:
    print("Saya suka", b)

for huruf in "Python":
    print(huruf)  # P, y, t, h, o, n
```

## D. WHILE Loop
```python
i = 1
while i <= 5:
    print(i)
    i += 1  # PENTING: update agar tidak infinite loop!
```

**Hati-hati Infinite Loop:**
```python
i = 1
while i <= 5:
    print(i)
    # i tidak bertambah → loop selamanya!
```

## E. break dan continue
**break — berhenti total:**
```python
for i in range(10):
    if i == 5:
        break
    print(i)   # 0, 1, 2, 3, 4
```

**continue — skip iterasi saat ini:**
```python
for i in range(10):
    if i % 2 == 0:
        continue  # skip genap
    print(i)      # 1, 3, 5, 7, 9
```

## F. Loop Bersarang (Nested Loop)
```python
for i in range(1, 4):
    for j in range(1, 4):
        print(f"{i}x{j}={i*j}", end="\t")
    print()
# 1x1=1  1x2=2  1x3=3
# 2x1=2  2x2=4  2x3=6
# 3x1=3  3x2=6  3x3=9
```

## G. Program — Deret Bilangan
```python
# Bilangan genap 2-20
for i in range(2, 21, 2):
    print(i, end=" ")

# Jumlah 1-100
total = 0
for i in range(1, 101):
    total += i
print("Jumlah 1-100:", total)  # 5050
```


### 🔧 Mengaplikasi — Praktik & Penerapan

## H. Latihan
1. Cetak angka 10 sampai 1 (mundur)
2. Cetak bilangan ganjil 1-20
3. Hitung jumlah bilangan genap 1-100
4. Tabel perkalian 5 (5x1=5 sampai 5x10=50)
5. Tebak angka: komputer pilih 1-10, user tebak sampai benar
6. Cetak pola bintang:
```
*
**
***
****
*****
```


### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagaimana konsep ini terkait dengan materi sebelumnya?
- Skala pemahaman diri: ___/10
- Apa yang ingin kamu pelajari lebih lanjut?

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) S2 Pert 5**
