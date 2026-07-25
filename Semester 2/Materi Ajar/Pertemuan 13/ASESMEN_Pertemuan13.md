# ASESMEN – PERTEMUAN 13
## Python: Perulangan FOR, WHILE + Studi Kasus

Informatika – Fase E / Kelas X – SMA Negeri 6 Cimahi

---

## Rubrik Penilaian

### A. FOR + range() (Bobot 25%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Soal 1 (1..5) | Tidak jalan | — | — | Benar |
| Soal 3 (genap 2–20) | Tidak jalan | Range salah | Step 2 benar | Benar |
| Soal 4 (tabel 7) | Tidak jalan | Sebagian | Hampir benar | Tepat |
| Soal 5 (total 1..n) | Tidak jalan | Logika salah | Benar | Benar + test |

### B. WHILE (Bobot 25%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Soal 6 (cetak 1–10) | Tidak jalan | — | — | Benar |
| Soal 7 (input 0) | Tidak jalan | Logika salah | Benar | Benar + test |
| Soal 8 (kelipatan 3) | Tidak jalan | Logika salah | Benar | Benar |

### C. Break/Continue (Bobot 15%)

| No | Jawaban | Skor |
|---|---|---|
| 9 | Tebak angka dengan break = selesai | 2 |
| 10 | Output: 1 2 4 5 7 8 10 (skip kelipatan 3) | 2 |

### D. Studi Kasus (Bobot 35%)

| Kriteria | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| Faktorial (5) | Tidak selesai | Logika salah | Benar (120) | Benar + test 8 |
| Fibonacci (8 suku) | Tidak selesai | Logika salah | Benar | Benar (0 1 1 2 3 5 8 13) |
| Cek prima (7, 12) | Tidak selesai | 1/2 benar | 2/2 benar | Benar + alasan |

---

## Kunci Jawaban LKPD

### A. FOR

**Soal 1:** 1 2 3 4 5

**Soal 2:** `for i in range(1, 11):`

**Soal 3:** `for i in range(2, 21, 2):`
Output: 2 4 6 8 10 12 14 16 18 20

**Soal 4:** `print(f"7 × {i} = {7 * i}")`

**Soal 5:** `total += i` → n=10 → Total = 55

### B. WHILE

**Soal 6:**
```python
i = 1
while i <= 10:
    print(i, end=" ")
    i += 1
```

**Soal 7:**
```python
while x != 0:
    total += x
```
Test: 5+3+2 = 10 → Output: `Total = 10`

**Soal 8:**
```python
i = 3
while i <= 30:
    print(i, end=" ")
    i += 3
```
Output: 3 6 9 12 15 18 21 24 27 30

### C. Break/Continue

**Soal 9:**
```python
if tebakan == rahasia:
    print("Selamat! Benar!")
    break
elif tebakan < rahasia:
    print("Terlalu kecil!")
else:
    print("Terlalu besar!")
```

**Soal 10:** Output: `1 2 4 5 7 8 10` (skip 3, 6, 9)

### D. Studi Kasus

**Soal 11: Faktorial**
```python
for i in range(1, n + 1):
    hasil *= i
```
| n | Hasil |
|---|---|
| 5 | 120 |
| 8 | 40320 |

**Soal 12: Fibonacci**
```python
a, b = 0, 1
print(a, end=" ")
for i in range(2, n + 1):
    print(b, end=" ")
    a, b = b, a + b
```
n=8 → Output: `0 1 1 2 3 5 8 13`

**Soal 13: Cek Prima**
```python
for i in range(2, n):
    if n % i == 0:
        prima = False
        break
```
Test: n=7 → Prima, n=12 → Bukan prima

### Tugas Rumah — Tebak Angka
```python
import random
rahasia = random.randint(1, 100)
tebakan = 0
jumlah = 0

while tebakan != rahasia:
    tebakan = int(input("Tebak (1-100): "))
    jumlah += 1
    if tebakan < rahasia:
        print("Terlalu kecil!")
    elif tebakan > rahasia:
        print("Terlalu besar!")

print(f"Selamat! Kamu menebak {jumlah} kali.")
```

---

**MGMP Informatika SMAN 6 Cimahi**
