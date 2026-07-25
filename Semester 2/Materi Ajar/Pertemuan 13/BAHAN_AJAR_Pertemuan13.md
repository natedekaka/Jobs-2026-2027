# BAHAN AJAR – PERTEMUAN 13
## Python: Perulangan FOR, WHILE + Studi Kasus

| TP | BK 1.4, BK 2.1 |
|---|---|

---

### A. FOR DI PYTHON — range()

FOR di Python menggunakan `range()`.

#### range(stop) — dari 0 sampai stop-1
```python
for i in range(5):
    print(i)
# Output: 0 1 2 3 4
```

#### range(start, stop) — dari start sampai stop-1
```python
for i in range(1, 6):
    print(i)
# Output: 1 2 3 4 5
```

#### range(start, stop, step) — dengan langkah
```python
for i in range(2, 11, 2):
    print(i)
# Output: 2 4 6 8 10

for i in range(10, 0, -1):
    print(i)
# Output: 10 9 8 ... 1

for i in range(3, 31, 3):
    print(i)
# Output: 3 6 9 ... 30
```

#### Translasi Pseudocode → Python (FOR)

| Pseudocode | Python |
|---|---|
| `FOR i ← 1 TO 5` | `for i in range(1, 6):` |
| `FOR i ← 0 TO 4` | `for i in range(5):` |
| `FOR i ← 2 TO 10 STEP 2` | `for i in range(2, 11, 2):` |
| `FOR i ← 10 DOWNTO 1` | `for i in range(10, 0, -1):` |
| `ENDFOR` | *(indentasi)* |

#### Contoh Program FOR

**Cetak 1–10:**
```python
for i in range(1, 11):
    print(i)
```

**Tabel perkalian 7:**
```python
for i in range(1, 11):
    print(f"7 × {i} = {7 * i}")
```

**Jumlah 1+2+...+n:**
```python
n = int(input("Masukkan n: "))
total = 0
for i in range(1, n + 1):
    total += i
print(f"Total = {total}")
```

**Deret genap 2–20:**
```python
for i in range(2, 21, 2):
    print(i, end=" ")
# Output: 2 4 6 8 10 12 14 16 18 20
```

---

### B. WHILE DI PYTHON

WHILE mengulang **selama** kondisi TRUE.

#### Sintaks
```python
while kondisi:
    # kode diulang
```

#### Contoh 1: Cetak 1–5
```python
i = 1
while i <= 5:
    print(i)
    i += 1      # i = i + 1 — INGAT update!
```

#### Contoh 2: Input sampai 0
```python
total = 0
x = int(input("Angka (0=stop): "))
while x != 0:
    total += x
    x = int(input("Angka (0=stop): "))
print(f"Total = {total}")
```

#### Contoh 3: Tebak angka
```python
rahasia = 7
tebakan = int(input("Tebak angka: "))
while tebakan != rahasia:
    if tebakan < rahasia:
        print("Terlalu kecil!")
    else:
        print("Terlalu besar!")
    tebakan = int(input("Coba lagi: "))
print("Selamat! Benar!")
```

#### Contoh 4: Faktorial dengan WHILE
```python
n = int(input("n: "))
hasil = 1
i = 1
while i <= n:
    hasil *= i
    i += 1
print(f"{n}! = {hasil}")
```

#### Translasi Pseudocode → Python (WHILE)

| Pseudocode | Python |
|---|---|
| `WHILE x<10` | `while x < 10:` |
| `x ← x + 1` | `x += 1` |
| `ENDWHILE` | *(indentasi)* |

---

### C. BREAK & CONTINUE

#### break — Keluar dari perulangan
```python
# Berhenti saat pengguna mengetik 0
while True:
    x = int(input("Angka (0=stop): "))
    if x == 0:
        print("Bye!")
        break
    print(f"Kamu mengetik {x}")
```

#### continue — Loncat ke iterasi berikutnya
```python
# Cetak angka ganjil dari 1-10 (skip genap)
for i in range(1, 11):
    if i % 2 == 0:
        continue
    print(i, end=" ")
# Output: 1 3 5 7 9
```

#### Perbandingan break vs continue

| Perintah | Efek |
|---|---|
| `break` | **Keluar** dari perulangan (stop total) |
| `continue` | **Loncat** ke iterasi berikutnya (skip sisa kode) |

---

### D. STUDI KASUS

#### Kasus 1: Faktorial n!

Rumus: n! = n × (n-1) × (n-2) × ... × 1

**Dengan FOR:**
```python
n = int(input("Masukkan n: "))
hasil = 1
for i in range(1, n + 1):
    hasil *= i
print(f"{n}! = {hasil}")
```

**Dengan WHILE:**
```python
n = int(input("Masukkan n: "))
hasil = 1
i = 1
while i <= n:
    hasil *= i
    i += 1
print(f"{n}! = {hasil}")
```

| n | Proses | Hasil |
|---|---|---|
| 3 | 1×2×3 | 6 |
| 5 | 1×2×3×4×5 | 120 |
| 7 | 1×...×7 | 5040 |

---

#### Kasus 2: Deret Fibonacci

Rumus: F₀=0, F₁=1, Fₙ = Fₙ₋₁ + Fₙ₋₂
Deret: 0, 1, 1, 2, 3, 5, 8, 13, 21, ...

```python
n = int(input("Masukkan jumlah suku: "))
a, b = 0, 1
print(a, end=" ")
for i in range(2, n + 1):
    print(b, end=" ")
    a, b = b, a + b
```

**Simulasi n=7:**
| i | a | b | Output |
|---|---|---|---|
| — | 0 | 1 | 0 |
| 2 | 1 | 1 | 1 |
| 3 | 1 | 2 | 1 |
| 4 | 2 | 3 | 2 |
| 5 | 3 | 5 | 3 |
| 6 | 5 | 8 | 5 |
| 7 | 8 | 13 | 8 |

Output: `0 1 1 2 3 5 8`

---

#### Kasus 3: Cek Bilangan Prima

Bilangan prima hanya habis dibagi 1 dan dirinya sendiri.

```python
n = int(input("Masukkan angka: "))

if n < 2:
    print(f"{n} bukan prima")
else:
    prima = True
    for i in range(2, n):
        if n % i == 0:
            prima = False
            break
    
    if prima:
        print(f"{n} adalah prima")
    else:
        print(f"{n} bukan prima")
```

**Uji:**
| n | Prima? | Alasan |
|---|---|---|
| 1 | ❌ | < 2 |
| 2 | ✅ | Hanya habis dibagi 1 dan 2 |
| 7 | ✅ | 1×7 saja |
| 10 | ❌ | 2×5 = 10 |
| 17 | ✅ | 1×17 saja |

---

### E. RANGKUMAN

| Konsep | Python |
|---|---|
| FOR 0..n-1 | `for i in range(n):` |
| FOR 1..n | `for i in range(1, n+1):` |
| FOR step | `for i in range(awal, akhir, step):` |
| WHILE | `while kondisi:` |
| Update counter | `i += 1` |
| Break | `break` — keluar loop |
| Continue | `continue` — skip iterasi |
| Faktorial | `hasil *= i` |
| Fibonacci | `a, b = b, a+b` |
| Cek prima | FOR i=2..n-1, cek `n%i==0` |

---

**MGMP Informatika SMAN 6 Cimahi**
