# BAHAN AJAR – PERTEMUAN 12
## Python: Variabel, Tipe Data, Input/Output, Percabangan

| TP | BK 1.4, BK 2.1 |
|---|---|

---

### A. APA ITU PYTHON?

**Python** adalah bahasa pemrograman tingkat tinggi yang:
- Mudah dibaca (mirip bahasa Inggris)
- Banyak digunakan di industri (data science, AI, web)
- **Interpreted** — langsung jalan tanpa kompilasi
- Sintaksisnya **sangat mirip pseudocode**!

---

### B. MENJALANKAN PYTHON

#### Opsi 1: Google Colab (Online — Gratis, Tanpa Instalasi)
1. Buka browser → `colab.research.google.com`
2. Login Google
3. Klik `+ New notebook`
4. Ketik kode di sel → tekan `Shift+Enter`

#### Opsi 2: Python IDLE (Offline)
1. Start Menu → Python → IDLE (Python 3.x)
2. Atau ketik `python` di terminal/CMD
3. Langsung bisa mengetik perintah Python

#### Opsi 3: VS Code + Extension Python
1. Buka VS Code
2. Install extension Python (Microsoft)
3. Buat file `.py` → klik run ▶

#### Program Pertama: Hello, World!
```python
print("Hello, World!")
```

> **Semua programmer dunia mulai dari sini!** 🎉

---

### C. VARIABEL DAN ASSIGNMENT

Di Python, variabel **tidak perlu dideklarasikan** — langsung assignment.

#### Aturan Penamaan Variabel
| ✅ Boleh | ❌ Tidak Boleh |
|---|---|
| Huruf, angka, underscore | Angka di awal |
| `nama`, `umur`, `nilai_uts` | `1data`, `nilai-uts` |
| Case-sensitive (`nama` ≠ `Nama`) | Spasi (`nilai uts`) |
| Pakai underscore untuk spasi | Kata kunci Python (`if`, `for`) |

#### Contoh Variabel
```python
nama = "Andi"          # string
umur = 16              # integer
tinggi = 165.5         # float
lulus = True           # boolean

print(nama)            # Andi
print(umur)            # 16
print(type(nama))      # <class 'str'>
print(type(umur))      # <class 'int'>
```

| Pseudocode | Python |
|---|---|
| `nama ← "Andi"` | `nama = "Andi"` |
| `x ← 5` | `x = 5` |
| `total ← a + b` | `total = a + b` |
| `usia ← usia + 1` | `usia = usia + 1` |

---

### D. TIPE DATA DASAR

| Tipe | Python | Contoh | Keterangan |
|---|---|---|---|
| Integer | `int` | `5`, `-10`, `1000` | Bilangan bulat |
| Float | `float` | `3.14`, `-0.5` | Bilangan pecahan |
| String | `str` | `"Halo"`, `'Python'` | Teks (petik satu/dua) |
| Boolean | `bool` | `True`, `False` | Logika (huruf besar) |

```python
x = 10
y = 3.14
z = "Informatika"
w = True

print(type(x))  # <class 'int'>
print(type(y))  # <class 'float'>
print(type(z))  # <class 'str'>
print(type(w))  # <class 'bool'>
```

#### Konversi Tipe Data
```python
angka_str = "50"
angka_int = int(angka_str)    # "50" → 50
angka_float = float(angka_str) # "50" → 50.0
nilai = 85.7
nilai_int = int(nilai)        # 85.7 → 85 (pembulatan ke bawah)
```

---

### E. INPUT DAN OUTPUT

#### print() — Output

```python
print("Halo Dunia")           # Halo Dunia
print(5)                      # 5
print("Nilai:", 85)           # Nilai: 85

# f-string (termudah & terpopuler)
nama = "Budi"
print(f"Halo, {nama}!")       # Halo, Budi!
print(f"Umur: {17}")          # Umur: 17
```

#### input() — Input

```python
nama = input()               # input → disimpan sebagai string
print(f"Halo, {nama}")

nama = input("Siapa namamu? ")  # dengan prompt
print(f"Halo, {nama}")
```

**⚠️ PENTING:** `input()` selalu mengembalikan **string**!
```python
x = input("Masukkan angka: ")  # user ketik 5
print(type(x))                  # <class 'str'>
print(x + 3)                    # ERROR! string + int

# Harus dikonversi:
x = int(input("Masukkan angka: "))  # langsung ke int
x = float(input("Masukkan angka: "))  # ke float
```

#### Contoh Program Input-Output

```python
# Menyapa pengguna
nama = input("Siapa namamu? ")
print(f"Selamat belajar, {nama}!")

# Menjumlahkan dua angka
a = int(input("Masukkan a: "))
b = int(input("Masukkan b: "))
hasil = a + b
print(f"{a} + {b} = {hasil}")
```

#### Translasi Pseudocode → Python (Input/Output)

| Pseudocode | Python |
|---|---|
| `INPUT nama` | `nama = input()` |
| `INPUT x` (angka) | `x = int(input())` |
| `OUTPUT "Halo"` | `print("Halo")` |
| `OUTPUT "Halo, ", nama` | `print(f"Halo, {nama}")` |
| `OUTPUT "Nilai: ", x` | `print(f"Nilai: {x}")` |

---

### F. PERCABANGAN IF-ELIF-ELSE

#### Sintaks

```python
if kondisi:
    # kode jika TRUE
elif kondisi_lain:
    # kode jika kondisi pertama FALSE, ini TRUE
else:
    # kode jika semua FALSE
```

**⚠️ PENTING:**
- **Indentasi 4 spasi** — Python menggunakan indentasi, bukan `ENDIF`!
- **Titik dua `:`** setelah kondisi

#### Contoh 1: Positif/Negatif/Nol

```python
x = int(input("Masukkan angka: "))

if x > 0:
    print("Positif")
elif x < 0:
    print("Negatif")
else:
    print("Nol")
```

**Translasi dari pseudocode:**
```
PSEUDOCODE:                          PYTHON:
IF x > 0 THEN                        if x > 0:
    OUTPUT "Positif"                      print("Positif")
ELSE                                 else:
    IF x < 0 THEN                          if x < 0:
        OUTPUT "Negatif"                       print("Negatif")
    ELSE                                 else:
        OUTPUT "Nol"                          print("Nol")
    ENDIF
ENDIF
```

#### Contoh 2: Genap/Ganjil

```python
x = int(input("Masukkan angka: "))

if x % 2 == 0:
    print("Genap")
else:
    print("Ganjil")
```

#### Contoh 3: Nilai → Huruf Mutu

```python
nilai = float(input("Masukkan nilai akhir: "))

if nilai >= 92:
    huruf = "A"
elif nilai >= 83:
    huruf = "B"
elif nilai >= 75:
    huruf = "C"
else:
    huruf = "D"

print(f"Nilai: {nilai} — Huruf: {huruf}")
```

#### Operator Perbandingan & Logika

| Operator | Makna | Contoh |
|---|---|---|
| `==` | Sama dengan | `x == 5` |
| `!=` | Tidak sama | `x != 0` |
| `>` | Lebih besar | `x > 10` |
| `<` | Lebih kecil | `x < 10` |
| `>=` | ≥ | `x >= 75` |
| `<=` | ≤ | `x <= 100` |
| `and` | DAN | `x > 0 and x < 10` |
| `or` | ATAU | `x < 0 or x > 10` |
| `not` | BUKAN | `not(x > 0)` |

---

### G. TABEL TRANSLASI LENGKAP

| Konsep | Pseudocode | Python |
|---|---|---|
| Assignment | `x ← 5` | `x = 5` |
| Input string | `INPUT nama` | `nama = input()` |
| Input int | `INPUT x` | `x = int(input())` |
| Output | `OUTPUT x` | `print(x)` |
| Output teks | `OUTPUT "Halo"` | `print("Halo")` |
| Output + var | `OUTPUT "Nilai: ", x` | `print(f"Nilai: {x}")` |
| IF | `IF x>0 THEN` | `if x > 0:` |
| ELSE | `ELSE` | `else:` |
| ELSE IF | `ELSE IF` → nested | `elif:` |
| ENDIF | `ENDIF` | *(indentasi)* |
| AND | `AND` | `and` |
| OR | `OR` | `or` |
| MOD | `MOD` | `%` |
| Tidak sama | `≠` | `!=` |

---

### H. CONTOH PROGRAM LENGKAP

**Program: Diskon Belanja (Pseudocode → Python)**

| Pseudocode | Python |
|---|---|
| `PROGRAM diskon_belanja` | `# Program diskon belanja` |
| `INPUT total_belanja` | `total_belanja = float(input("Total belanja: "))` |
| `IF total_belanja > 100000 THEN` | `if total_belanja > 100000:` |
| `diskon ← total_belanja × 0.1` | `diskon = total_belanja * 0.1` |
| `total_bayar ← total_belanja - diskon` | `total_bayar = total_belanja - diskon` |
| `ELSE` | `else:` |
| `total_bayar ← total_belanja` | `total_bayar = total_belanja` |
| `ENDIF` | *(indentasi)* |
| `OUTPUT "Total bayar: ", total_bayar` | `print(f"Total bayar: {total_bayar}")` |
| `END` | *(selesai)* |

**Python lengkap:**
```python
# Program diskon belanja
total_belanja = float(input("Total belanja: "))

if total_belanja > 100000:
    diskon = total_belanja * 0.1
    total_bayar = total_belanja - diskon
else:
    total_bayar = total_belanja

print(f"Total bayar: {total_bayar}")
```

---

### I. KESALAHAN UMUM

| Kesalahan | Salah ❌ | Benar ✅ |
|---|---|---|
| Lupa indentasi | `if x>0:`<br>`print("Positif")` | `if x>0:`<br>`    print("Positif")` |
| Lupa titik dua | `if x>0` | `if x>0:` |
| `input()` tanpa konversi | `x = input()` lalu `x + 5` | `x = int(input())` |
| Assignment vs perbandingan | `if x = 5:` (assignment) | `if x == 5:` (perbandingan) |
| Case salah | `True` → `true` | `True`, `False` |
| Kurung print | `print "Halo"` | `print("Halo")` |

---

### J. RANGKUMAN

| Konsep | Python |
|---|---|
| Output | `print()` |
| Input (string) | `input()` |
| Input (angka) | `int(input())` / `float(input())` |
| IF | `if kondisi:` |
| IF-ELSE | `if ...: else:` |
| IF-ELIF-ELSE | `if ...: elif ...: else:` |
| Indentasi | **4 spasi** (wajib!) |
| f-string | `f"...{variabel}..."` |

---

**MGMP Informatika SMAN 6 Cimahi**
