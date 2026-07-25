---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 12 — SEMESTER 2
## Python: Variabel, Tipe Data, Input/Output, Percabangan
### Informatika – Fase E / Kelas X
#### SMA Negeri 6 Cimahi

---

## Roadmap

| Pert | Materi |
|---|---|
| 1–6 | Struktur Data, Searching, Sorting |
| 7 | **PTS** |
| 8–11 | Pseudocode, Flowchart, IF, FOR, WHILE |
| **12** | **🐍 Python!** |

> Semua yang dipelajari → **sekarang kita eksekusi!**

---

## Apersepsi

Pseudocode di papan tulis vs Python:

| Pseudocode | Python |
|---|---|
| `INPUT nama` | `nama = input()` |
| `OUTPUT "Halo"` | `print("Halo")` |
| `x ← 5` | `x = 5` |
| `IF x>0 THEN` | `if x > 0:` |
| `ENDIF` | *(indentasi)* |

> **Hanya beda sedikit!** Kalian sudah 80% bisa Python!

---

# TUJUAN PEMBELAJARAN

1. ✅ Menjalankan Python (Colab/IDLE)
2. ✅ Variabel & tipe data (int, float, str, bool)
3. ✅ input() & print()
4. ✅ if-elif-else
5. ✅ Translasi pseudocode → Python

---

## Cara Menjalankan Python

### 1. Google Colab (Online)
`colab.research.google.com` → + New → ketik → Shift+Enter

### 2. Python IDLE
Start Menu → Python → IDLE

### 3. VS Code + Python Extension

---

## Program Pertama

```python
print("Hello, World!")
```

> Semua programmer mulai dari sini!

### Jalankan sekarang! 🔥

---

## Variabel — Pseudocode vs Python

| Konsep | Pseudocode | Python |
|---|---|---|
| Assignment | `x ← 5` | `x = 5` |
| String | `"Andi"` | `"Andi"` |
| Cek tipe | — | `type(x)` |

```python
nama = "Andi"
umur = 16
print(nama)
print(type(umur))  # <class 'int'>
```

---

## Tipe Data

| Tipe | Python | Contoh |
|---|---|---|
| Integer | `int` | `5`, `-10` |
| Float | `float` | `3.14` |
| String | `str` | `"Halo"` |
| Boolean | `bool` | `True`, `False` |

> Python otomatis mendeteksi tipe data!

---

## Output — print()

```python
print("Halo Dunia")           # Halo Dunia
print(5)                      # 5
print("Nilai:", 85)           # Nilai: 85
```

### f-string (termudah!):
```python
nama = "Budi"
print(f"Halo, {nama}!")       # Halo, Budi!
```

---

## Input — input()

```python
nama = input("Siapa namamu? ")
print(f"Halo, {nama}!")
```

### ⚠️ input() selalu string!
```python
x = input("Angka: ")    # user ketik 5
print(x + 3)            # ERROR!

x = int(input("Angka: "))  # konversi ke int
print(x + 3)            # ✅ 8
```

---

## Translasi Input/Output

| Pseudocode | Python |
|---|---|
| `INPUT nama` | `nama = input()` |
| `INPUT x` (angka) | `x = int(input())` |
| `OUTPUT "Halo"` | `print("Halo")` |
| `OUTPUT "Halo, ", nama` | `print(f"Halo, {nama}")` |

---

## IF — Pseudocode vs Python

| Pseudocode | Python |
|---|---|
| `IF x>0 THEN` | `if x > 0:` |
| `ELSE` | `else:` |
| `ENDIF` | *(indentasi 4 spasi)* |

```python
x = int(input("Angka: "))
if x > 0:
    print("Positif")
elif x < 0:
    print("Negatif")
else:
    print("Nol")
```

---

## ⚠️ Indentasi adalah ENDIF!

Python tidak pakai `ENDIF` — pakai **indentasi**.

```
if x > 0:
    print("Positif")    ← 4 spasi
else:
    print("Lainnya")    ← 4 spasi
```

> Lupa indentasi = ERROR!

---

## Genap/Ganjil — Translasi

| Pseudocode | Python |
|---|---|
| `IF x MOD 2 = 0` | `if x % 2 == 0:` |
| `OUTPUT "Genap"` | `print("Genap")` |

```python
x = int(input("Masukkan angka: "))
if x % 2 == 0:
    print("Genap")
else:
    print("Ganjil")
```

---

## Nilai → Huruf Mutu

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

---

## Aktivitas 1: Hello World & Variabel

### Individu — 10 menit

1. `print("Hello, World!")`
2. Buat variabel nama, umur, kelas
3. Cek tipe dengan `type()`
4. Print data diri dengan f-string

---

## Aktivitas 2: Input & Output

### Berpasangan — 10 menit

1. Program sapa (input nama → sapa)
2. Jumlah dua angka
3. Celcius → Fahrenheit
4. Translasi pseudocode → Python

---

## Aktivitas 3: If-Elif-Else

### Berpasangan — 10 menit

1. Genap/ganjil
2. Nilai → huruf mutu
3. Translasi: cek suhu (Panas/Dingin/Sejuk)

---

## Kesalahan Umum ❌

| Salah | Benar |
|---|---|
| `if x = 5:` | `if x == 5:` |
| lupa `:` | `if x > 0:` |
| lupa indentasi | `    print(x)` |
| `x = input()` + `x+5` | `x = int(input())` |
| `print "Halo"` | `print("Halo")` |

---

## Rangkuman

| Konsep | Python |
|---|---|
| Output | `print()` |
| Input string | `input()` |
| Input angka | `int(input())` |
| IF | `if ...:` |
| IF-ELIF-ELSE | `if ...: elif ...: else:` |
| Indentasi | **wajib 4 spasi** |
| f-string | `f"...{var}..."` |

---

## Tugas Rumah

Translasi 3 pseudocode ke Python:

1. **Maks 3 angka** (Pert 9)
2. **Total 1..n dengan FOR** (Pert 10)
3. **Faktorial n!** (Pert 10)

> Jalankan dan catat output!

---

## Pertemuan Depan

### Python — Perulangan FOR & WHILE
> for, while, range(), study case

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Python adalah pseudocode yang menjadi nyata."
