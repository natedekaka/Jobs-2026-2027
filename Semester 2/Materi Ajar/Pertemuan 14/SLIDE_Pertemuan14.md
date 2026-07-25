---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 14 — SEMESTER 2
## Python: List & Fungsi
### Informatika – Fase E / Kelas X
#### SMA Negeri 6 Cimahi

---

## Review — 13 Pertemuan

| Part | Materi |
|---|---|
| 1–6 | Array, Stack, Queue, Searching, Sorting |
| 7 | **PTS** |
| 8–11 | Pseudocode, Flowchart, IF, FOR, WHILE |
| 12–13 | **Python**: variabel, input/output, IF, FOR, WHILE |
| **14** | **Python: List & Fungsi** 🎯 |

---

## Apersepsi

Pert 1: **Array** — indeks 0, simpan banyak data

```
nilai1 = 85
nilai2 = 90
nilai3 = 78    → repot!
```

**List di Python:**
```python
nilai = [85, 90, 78]   → 1 variabel!
```

> Array (Pert 1) = List (Python)! Full circle! 🔄

---

# TUJUAN PEMBELAJARAN

1. ✅ List: buat, akses, method
2. ✅ Fungsi: def, parameter, return
3. ✅ Translasi array → list
4. ✅ Studi kasus: data nilai siswa

---

## Membuat List

```python
buah = ["apel", "mangga", "jeruk"]
angka = [5, 3, 8, 1, 6]
campur = ["Andi", 16, True, 85.5]
matriks = [[1, 2], [3, 4]]
```

> List bisa menyimpan **tipe data apa saja**!

---

## Akses Indeks

```python
buah = ["apel", "mangga", "jeruk", "duku"]

buah[0]        # "apel"     — indeks 0
buah[-1]       # "duku"     — dari belakang
buah[1:3]      # ["mangga", "jeruk"] — slicing
```

**Seperti Array di Pert 1!** 🎯

---

## Method List

```python
angka = [5, 3, 8, 1, 6]

angka.append(10)       # tambah di akhir
angka.insert(2, 99)    # sisip di indeks 2
angka.remove(3)        # hapus 3
angka.sort()           # urutkan ascending
angka.reverse()        # balik urutan
len(angka)             # panjang list
```

---

## Looping List

```python
buah = ["apel", "mangga", "jeruk"]

# FOR biasa
for b in buah:
    print(b)

# FOR dengan indeks
for i in range(len(buah)):
    print(f"{i}: {buah[i]}")
```

---

## Fungsi — def

Blok kode yang bisa **dipakai ulang**.

```python
def nama_fungsi(parameter):
    # kode
    return hasil
```

### Kenapa fungsi?
| Tanpa fungsi | Dengan fungsi |
|---|---|
| Kode berulang | Tulis sekali, pakai berkali-kali |
| Sulit dibaca | Modular & rapi |
| Sulit diperbaiki | Perbaiki di satu tempat |

---

## Contoh Fungsi

```python
# Tanpa parameter
def sapa():
    print("Halo!")

# Dengan parameter
def sapa_orang(nama):
    print(f"Halo, {nama}!")

# Dengan return
def luas_persegi(sisi):
    return sisi * sisi

# Default parameter
def sapa(nama="Teman"):
    print(f"Halo, {nama}!")
```

---

## Fungsi — Return

```python
def faktorial(n):
    hasil = 1
    for i in range(1, n + 1):
        hasil *= i
    return hasil

print(faktorial(5))   # 120
```

### Fungsi bisa dipanggil dari fungsi lain!

---

## Aktivitas 1: List

### Individu — 10 menit

1. Buat list nilai [85, 90, 78, 92, 88]
2. Akses indeks 2, -1, slicing 1:4
3. Append 95, sort, len
4. Rata-rata dengan loop FOR
5. List of lists 3 siswa

---

## Aktivitas 2: Fungsi

### Berpasangan — 10 menit

| Fungsi | Tugas |
|---|---|
| sapa(nama) | "Halo, {nama}!" |
| luas_segitiga(a, t) | a × t / 2 |
| faktorial(n) | n! |
| cek_prima(n) | True/False |

---

## Aktivitas 3: Data Nilai Siswa

### Kelompok — 15 menit

Program lengkap dengan list + fungsi:

1. ✅ Input jumlah & data siswa
2. ✅ Rata-rata kelas
3. ✅ Nilai tertinggi
4. ✅ Lulus (≥75) vs Remidi (<75)

---

## Studi Kasus — Output

### Input: Andi 85, Budi 72, Cici 90

```
Rata-rata kelas: 82.33
Nilai tertinggi: Cici (90)

Lulus (2 orang):
  - Andi: 85
  - Cici: 90

Remidi (1 orang):
  - Budi: 72
```

---

## Rangkuman

| Konsep | Python |
|---|---|
| List | `[a, b, c]` |
| Akses | `list[i]` |
| Tambah | `.append(x)` |
| Urut | `.sort()` |
| Panjang | `len(list)` |
| Fungsi | `def f(p):` |
| Return | `return x` |

---

## Tugas Rumah

Selesaikan program data nilai + **tambah fitur urutkan nilai descending**!

> 🌟 Bonus: bisa diurutkan dari tertinggi ke terendah

---

## Pertemuan Depan (Terakhir 🏁)

### Pert 15: Proyek Akhir & Review PAS
> Program Python lengkap sebagai portofolio

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Satu list menyimpan banyak data. Satu fungsi menyimpan banyak kode. Satu project menyimpan semua pembelajaran."
