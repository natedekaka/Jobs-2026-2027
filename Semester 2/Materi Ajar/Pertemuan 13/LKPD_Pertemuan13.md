# LEMBAR KERJA PESERTA DIDIK (LKPD)
## Pertemuan 13 – Python: Perulangan FOR, WHILE + Studi Kasus

| TP | BK 1.4, BK 2.1 |
|---|---|
| Nama | ____________________ |
| Kelas | ____________________ |

**Buka:** `colab.research.google.com` → `+ New notebook`

---

### A. FOR — range() (10 menit)

**Soal 1:** Ketik dan jalankan. Outputnya apa?

```python
for i in range(1, 6):
    print(i)
```

Output: _________

**Soal 2:** Modifikasi jadi cetak 1–10.

```python
for i in range(1, ____):
    print(i)
```

**Soal 3:** Cetak bilangan genap 2–20.

```python
for i in range(2, ____, ____):
    print(i, end=" ")
```

**Soal 4:** Tabel perkalian 7.

```python
for i in range(1, 11):
    print(f"7 × {i} = {____}")
```

**Soal 5:** Jumlah 1+2+...+n.

```python
n = int(input("Masukkan n: "))
total = 0
for i in range(1, n + 1):
    total ____ i
print(f"Total = {total}")
```
Test: n=10 → Output: _________

---

### B. WHILE (10 menit)

**Soal 6:** Cetak 1–10 dengan WHILE.

```python
i = 1
while i ____ 10:
    print(i, end=" ")
    i ____
```

**Soal 7:** Input angka sampai 0 → jumlah.

```python
total = 0
x = int(input("Angka (0=stop): "))
____ x != 0:
    total ____ x
    x = int(input("Angka (0=stop): "))
print(f"Total = {total}")
```
Test: 5, 3, 2, 0 → Output: _________

**Soal 8:** Cetak kelipatan 3 dari 3–30 dengan WHILE.

```python
i = 3
____ i <= 30:
    print(i, end=" ")
    i ____ ____
```

---

### C. BREAK & CONTINUE

**Soal 9:** Tebak angka dengan break.

```python
rahasia = 7
while True:
    tebakan = int(input("Tebak angka: "))
    if tebakan ____ rahasia:
        print("Selamat! Benar!")
        ____
    elif tebakan < rahasia:
        print("Terlalu kecil!")
    ____:
        print("Terlalu besar!")
```

**Soal 10:** Apa output program ini?

```python
for i in range(1, 11):
    if i % 3 == 0:
        continue
    print(i, end=" ")
```

Output: _________

---

### D. STUDI KASUS — KELOMPOK (15 menit)

**Soal 11: Faktorial n!**

```python
n = int(input("Masukkan n: "))
hasil = 1
for i in range(1, ____):
    hasil ____ i
print(f"{n}! = {hasil}")
```
| n | Hasil |
|---|---|
| 5 | |
| 8 | |

**Soal 12: Deret Fibonacci**

Lengkapi kode Fibonacci!

```python
n = int(input("Jumlah suku: "))
a, b = ____, ____
print(a, end=" ")
for i in range(____, n + 1):
    print(b, end=" ")
    a, b = ____, ____
```
Test: n=8 → Output: _________

**Soal 13: Cek Bilangan Prima**

```python
n = int(input("Masukkan angka: "))
if n < 2:
    print("Bukan prima")
else:
    prima = True
    for i in range(2, ____):
        if n ____ i == 0:
            prima = False
            ____
    if prima:
        print("Prima")
    else:
        print("Bukan prima")
```
Test: n=7 → ____, n=12 → ____

---

### E. REFLEKSI

| Pertanyaan | Jawaban |
|---|---|
| Beda range(5) dan range(1,6)? | |
| Kenapa WHILE perlu update counter? | |
| Bedanya break dan continue? | |
| Kesulitan di studi kasus? | |
| Skala pemahaman (1–10) | / 10 |

---

### F. TUGAS RUMAH

Buat program tebak angka lengkap:
- Angka rahasia acak (atau tetap 1–100)
- Loop sampai tebakan benar
- Hitung jumlah tebakan
- Output: "Selamat! Kamu menebak 5 kali."

```python
# Program tebak angka
import random
rahasia = random.randint(1, 100)
tebakan = 0
jumlah = 0

# Tulis kode di sini!
```

---

**MGMP Informatika SMAN 6 Cimahi**
