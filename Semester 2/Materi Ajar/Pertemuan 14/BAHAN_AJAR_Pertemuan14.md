# BAHAN AJAR – PERTEMUAN 14
## Python: List & Fungsi

| TP | BK 1.4, BK 2.1, BK 2.2 |
|---|---|

---

### A. LIST — ARRAY DI PYTHON

**List** adalah struktur data yang menyimpan **banyak nilai** dalam satu variabel. List adalah implementasi **Array** di Python.

#### Membuat List

```python
# List kosong
data = []

# List dengan isi
buah = ["apel", "mangga", "jeruk"]
angka = [5, 3, 8, 1, 6]
campur = ["Andi", 16, True, 85.5]
matriks = [[1, 2], [3, 4]]     # list of lists (array 2D)
```

#### Mengakses Elemen

```python
buah = ["apel", "mangga", "jeruk", "duku"]

print(buah[0])       # apel     — indeks positif dari 0
print(buah[-1])      # duku     — indeks negatif dari belakang
print(buah[1:3])     # ["mangga", "jeruk"] — slicing
print(buah[:2])      # ["apel", "mangga"]  — dari awal
print(buah[2:])      # ["jeruk", "duku"]   — sampai akhir

# Mengubah nilai
buah[1] = "rambutan"
print(buah)          # ["apel", "rambutan", "jeruk", "duku"]
```

| Konsep Array (Pert 1) | Python List |
|---|---|
| Indeks mulai 0 | ✅ Indeks mulai 0 |
| Akses acak | ✅ `list[indeks]` |
| Array 2D | ✅ `list_of_lists` |
| Slicing | ✅ `list[start:stop]` |

#### Method List

```python
angka = [5, 3, 8, 1, 6]

angka.append(10)       # tambah di akhir → [5,3,8,1,6,10]
angka.insert(2, 99)    # sisip di indeks 2 → [5,3,99,8,1,6,10]
angka.remove(3)        # hapus nilai 3 → [5,99,8,1,6,10]
angka.sort()           # urutkan ascending → [1,5,6,8,10,99]
angka.reverse()        # balik urutan → [99,10,8,6,5,1]
print(len(angka))      # panjang list → 6
print(angka.count(5))  # hitung jumlah 5 → 1
```

#### Looping List

```python
# FOR biasa
buah = ["apel", "mangga", "jeruk"]
for b in buah:
    print(b)

# FOR dengan indeks
for i in range(len(buah)):
    print(f"Indeks {i}: {buah[i]}")

# FOR dengan enumerate
for i, b in enumerate(buah):
    print(f"{i}: {b}")
```

#### List Komprehensif (opsional — efisien)

```python
# Buat list kuadrat 1-10
kuadrat = [i**2 for i in range(1, 11)]
print(kuadrat)  # [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]

# Filter genap
genap = [i for i in range(1, 21) if i % 2 == 0]
print(genap)    # [2, 4, 6, 8, 10, 12, 14, 16, 18, 20]
```

---

### B. FUNGSI (def)

**Fungsi** adalah blok kode yang bisa **dipakai ulang**. Fungsinya:
- Modular (program terpecah menjadi bagian-bagian kecil)
- Reusable (pakai berkali-kali)
- Readable (mudah dibaca)

#### Sintaks Fungsi

```python
def nama_fungsi(parameter1, parameter2):
    """Dokumentasi (opsional)"""
    # kode fungsi
    return hasil
```

#### Contoh Fungsi

**1. Fungsi Tanpa Parameter**
```python
def sapa():
    print("Halo! Selamat belajar Python!")

sapa()          # Halo! Selamat belajar Python!
sapa()          # bisa dipanggil berkali-kali
```

**2. Fungsi Dengan Parameter**
```python
def sapa_orang(nama):
    print(f"Halo, {nama}!")

sapa_orang("Andi")     # Halo, Andi!
sapa_orang("Budi")     # Halo, Budi!
```

**3. Fungsi Dengan Return**
```python
def luas_persegi(sisi):
    return sisi * sisi

hasil = luas_persegi(5)
print(hasil)           # 25

print(luas_persegi(7)) # 49
```

**4. Fungsi Dengan Default Parameter**
```python
def sapa(nama="Teman"):
    print(f"Halo, {nama}!")

sapa("Andi")           # Halo, Andi!
sapa()                 # Halo, Teman! (pakai default)
```

**5. Fungsi Dengan Banyak Return**
```python
def operasi_dasar(a, b):
    jumlah = a + b
    kurang = a - b
    kali = a * b
    return jumlah, kurang, kali

j, k, kl = operasi_dasar(10, 3)
print(j)    # 13
print(k)    # 7
print(kl)   # 30
```

#### Contoh Fungsi — Translasi Algoritma

```python
# Sequential search dalam fungsi
def cari_angka(list_angka, target):
    for i in range(len(list_angka)):
        if list_angka[i] == target:
            return i
    return -1

data = [5, 3, 8, 1, 6]
print(cari_angka(data, 8))   # 2
print(cari_angka(data, 99))  # -1
```

```python
# Faktorial dalam fungsi
def faktorial(n):
    hasil = 1
    for i in range(1, n + 1):
        hasil *= i
    return hasil

print(faktorial(5))   # 120
print(faktorial(8))   # 40320
```

---

### C. STUDI KASUS: PROGRAM DATA NILAI SISWA

Program lengkap menggunakan list + fungsi.

```python
def input_data(jumlah):
    """Input data siswa: nama dan nilai"""
    data = []
    for i in range(jumlah):
        print(f"\nSiswa ke-{i+1}")
        nama = input("Nama: ")
        nilai = float(input("Nilai: "))
        data.append([nama, nilai])
    return data

def rata_rata(data):
    """Hitung rata-rata nilai kelas"""
    total = 0
    for siswa in data:
        total += siswa[1]
    return total / len(data)

def nilai_tertinggi(data):
    """Cari siswa dengan nilai tertinggi"""
    tertinggi = data[0]
    for siswa in data:
        if siswa[1] > tertinggi[1]:
            tertinggi = siswa
    return tertinggi

def tampilkan_kelulusan(data):
    """Tampilkan siswa lulus dan remidi"""
    lulus = []
    remidi = []
    for siswa in data:
        if siswa[1] >= 75:
            lulus.append(siswa)
        else:
            remidi.append(siswa)
    return lulus, remidi

# ===== PROGRAM UTAMA =====
print("=== PROGRAM DATA NILAI SISWA ===")
n = int(input("Jumlah siswa: "))
data_siswa = input_data(n)

print(f"\nRata-rata kelas: {rata_rata(data_siswa):.2f}")

terbaik = nilai_tertinggi(data_siswa)
print(f"Nilai tertinggi: {terbaik[0]} ({terbaik[1]})")

lulus, remidi = tampilkan_kelulusan(data_siswa)
print(f"\nLulus ({len(lulus)} orang):")
for s in lulus:
    print(f"  - {s[0]}: {s[1]}")

print(f"\nRemidi ({len(remidi)} orang):")
for s in remidi:
    print(f"  - {s[0]}: {s[1]}")
```

---

### D. RANGKUMAN

| Konsep | Python |
|---|---|
| Membuat list | `list = [1, 2, 3]` |
| Akses elemen | `list[i]` |
| Tambah elemen | `list.append(x)` |
| Sisip elemen | `list.insert(i, x)` |
| Hapus elemen | `list.remove(x)` |
| Urutkan | `list.sort()` |
| Panjang list | `len(list)` |
| Fungsi | `def nama(parameter):` |
| Return | `return nilai` |
| List of lists | `[[a,b], [c,d]]` |

---

**MGMP Informatika SMAN 6 Cimahi**
