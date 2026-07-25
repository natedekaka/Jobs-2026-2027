# ASESMEN – PERTEMUAN 12
## Python: Variabel, Tipe Data, Input/Output, Percabangan

Informatika – Fase E / Kelas X – SMA Negeri 6 Cimahi

---

## Rubrik Penilaian

### A. Praktikum Hello World & Variabel (Bobot 20%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Menjalankan Python | Tidak bisa | Bantuan penuh | Bantuan minimal | Mandiri |
| Variabel & type() | Tidak diisi | Sebagian | Benar semua | Benar + eksplorasi |
| Variabel data diri | Tidak | Sebagian | Lengkap | Lengkap + kreatif |

### B. Input/Output (Bobot 25%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Program sapa | Tidak jalan | Jalan error | Jalan benar | Benar + rapi |
| Penjumlahan | Tidak jalan | Jalan error | Jalan benar | Benar + rapi |
| Celcius→Fahrenheit | Tidak jalan | Jalan error | Jalan benar | Benar + rapi |

### C. If-Elif-Else (Bobot 25%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Genap/ganjil | Tidak jalan | Struktur salah | Benar | Benar + test |
| Nilai→huruf mutu | Tidak jalan | Sebagian | Benar | Benar + test |

### D. Translasi Pseudocode→Python (Bobot 30%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Cek suhu | Tidak | Struktur salah | Hampir benar | Tepat |
| Diskon belanja | Tidak | Struktur salah | Hampir benar | Tepat |

---

## Kunci Jawaban LKPD

### Soal 3 (data diri)
```python
nama = "Andi"
kelas = "X-1"
hobi = "Membaca"
print(f"Nama: {nama}")
print(f"Kelas: {kelas}")
print(f"Hobi: {hobi}")
```

### Soal 4 (sapa)
Input: Budi → Output: `Halo, Budi! Selamat belajar Python!`

### Soal 5 (penjumlahan)
Input: a=12, b=7 → Output: `12 + 7 = 19`

### Soal 6 (Celcius→Fahrenheit)
C=100 → F=100×9/5+32 = **212.0**
C=0 → F=0×9/5+32 = **32.0**

### Soal 7 (Genap/ganjil)
| Input | Output |
|---|---|
| 7 | Ganjil |
| 10 | Genap |
| 0 | Genap |

### Soal 8 (Nilai→huruf)
| Input | Output |
|---|---|
| 95 | Nilai: 95.0 — Huruf: A |
| 88 | Nilai: 88.0 — Huruf: B |
| 70 | Nilai: 70.0 — Huruf: D |

### Soal 9 (Cek suhu)
```python
suhu = float(input("Masukkan suhu: "))
if suhu > 30:
    print("Panas")
elif suhu < 20:
    print("Dingin")
else:
    print("Sejuk")
```
Test: 35 → Panas, 15 → Dingin, 25 → Sejuk

### Soal 10 (Diskon belanja)
```python
total_belanja = float(input("Total belanja: "))
if total_belanja > 100000:
    diskon = total_belanja * 0.1
    total_bayar = total_belanja - diskon
else:
    total_bayar = total_belanja
print(f"Total bayar: {total_bayar}")
```

### Tugas Rumah

**1. Bilangan terbesar dari 3 angka**
```python
a = int(input("Masukkan a: "))
b = int(input("Masukkan b: "))
c = int(input("Masukkan c: "))

if a >= b and a >= c:
    maks = a
elif b >= a and b >= c:
    maks = b
else:
    maks = c

print(f"Terbesar: {maks}")
```

**2. Total 1+2+...+n dengan FOR**
```python
n = int(input("Masukkan n: "))
total = 0
for i in range(1, n + 1):
    total += i
print(f"Total 1+...+{n} = {total}")
```

**3. Faktorial n!**
```python
n = int(input("Masukkan n: "))
hasil = 1
for i in range(1, n + 1):
    hasil *= i
print(f"{n}! = {hasil}")
```

---

**MGMP Informatika SMAN 6 Cimahi**
