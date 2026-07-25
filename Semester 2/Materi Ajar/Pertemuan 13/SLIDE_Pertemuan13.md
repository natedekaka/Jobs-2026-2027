---
marp: true
theme: uncover
class: invert
---

# PERTEMUAN 13 — SEMESTER 2
## Python: Perulangan FOR, WHILE + Studi Kasus
### Informatika – Fase E / Kelas X
#### SMA Negeri 6 Cimahi

---

## Review — Pert 12

| Konsep | Python |
|---|---|
| Output | `print()` |
| Input string | `input()` |
| Input angka | `int(input())` |
| IF | `if ...:` |
| IF-ELIF-ELSE | `if ...: elif ...: else:` |

> Hari ini: **Perulangan** — FOR & WHILE

---

## Apersepsi

Pert 10: FOR dan WHILE di **pseudocode**

| Pseudocode | Python |
|---|---|
| `FOR i ← 1 TO 5` | `for i in range(1,6):` |
| `WHILE x<10` | `while x < 10:` |

> **Sangat mirip!** Tinggal translasi!

---

# TUJUAN PEMBELAJARAN

1. ✅ FOR dengan range()
2. ✅ WHILE
3. ✅ break & continue
4. ✅ Studi kasus: faktorial, Fibonacci, prima

---

## FOR — range() di Python

```python
range(5)        # 0, 1, 2, 3, 4
range(1, 6)     # 1, 2, 3, 4, 5
range(2, 11, 2) # 2, 4, 6, 8, 10
range(10, 0, -1) # 10, 9, ..., 1
```

| Pseudocode | Python |
|---|---|
| `FOR i ← 1 TO 5` | `for i in range(1,6):` |
| `FOR i ← 2 TO 10 STEP 2` | `for i in range(2,11,2):` |

---

## FOR — Contoh

```python
# Cetak 1-10
for i in range(1, 11):
    print(i)

# Tabel perkalian 7
for i in range(1, 11):
    print(f"7 × {i} = {7*i}")

# Jumlah 1+...+n
total = 0
for i in range(1, n+1):
    total += i
```

---

## WHILE di Python

```
while kondisi:
    # kode
    # UPDATE counter!
```

```python
i = 1
while i <= 5:
    print(i)
    i += 1       # ← INGAT update!
```

> ⚠️ Lupa `i += 1` → **Infinite loop!**

---

## WHILE — Input Sampai 0

```python
total = 0
x = int(input("Angka (0=stop): "))
while x != 0:
    total += x
    x = int(input("Angka (0=stop): "))
print(f"Total = {total}")
```

### Test: 5, 3, 2, 0
> Total = **10**

---

## BREAK — Keluar dari Loop

```python
while True:
    x = int(input("Angka (0=stop): "))
    if x == 0:
        print("Bye!")
        break
    print(f"Kamu mengetik {x}")
```

> `break` menghentikan perulangan **total**

---

## CONTINUE — Skip Iterasi

```python
for i in range(1, 11):
    if i % 3 == 0:
        continue
    print(i, end=" ")
```

> Output: **1 2 4 5 7 8 10**
> (skip 3, 6, 9)

---

## BREAK vs CONTINUE

| Perintah | Efek |
|---|---|
| `break` | **Stop total** — keluar dari loop |
| `continue` | **Skip sisa kode** — lanjut iterasi berikut |

---

## Aktivitas 1: FOR

### Individu — 10 menit

1. Cetak 1–10
2. Genap 2–20
3. Tabel perkalian 7
4. Jumlah 1+2+...+n

---

## Aktivitas 2: WHILE

### Berpasangan — 10 menit

5. Cetak 1–10 dengan WHILE
6. Input sampai 0 → jumlah
7. Kelipatan 3 (3–30)

---

## Aktivitas 3: Studi Kasus

### Kelompok — 15 menit

| Soal | Tugas |
|---|---|
| **Faktorial** | n! = n × (n-1) × ... × 1 |
| **Fibonacci** | Cetak deret sampai suku ke-n |
| **Cek Prima** | Input n → prima / bukan |

---

## Faktorial — FOR

```python
n = int(input("n: "))
hasil = 1
for i in range(1, n + 1):
    hasil *= i
print(f"{n}! = {hasil}")
```

| n | Hasil |
|---|---|
| 5 | 120 |
| 8 | 40320 |

---

## Fibonacci

```python
n = int(input("Jumlah suku: "))
a, b = 0, 1
print(a, end=" ")
for i in range(2, n + 1):
    print(b, end=" ")
    a, b = b, a + b
```

### n=8: **0 1 1 2 3 5 8 13**

---

## Cek Prima

```python
n = int(input("Angka: "))
if n < 2:
    print("Bukan prima")
else:
    prima = True
    for i in range(2, n):
        if n % i == 0:
            prima = False
            break
    print("Prima" if prima else "Bukan prima")
```

| n | Hasil |
|---|---|
| 7 | ✅ Prima |
| 12 | ❌ Bukan prima |

---

## Rangkuman

| Konsep | Python |
|---|---|
| FOR 1..n | `for i in range(1, n+1):` |
| FOR step | `for i in range(a, b, step):` |
| WHILE | `while kondisi:` |
| update | `i += 1` |
| break | keluar loop |
| continue | skip iterasi |

---

## Tugas Rumah

### Tebak Angka (lengkap)

- Angka rahasia: `random.randint(1, 100)`
- Loop sampai benar
- Hitung jumlah tebakan
- Output: "Selamat! Kamu menebak X kali."

```python
import random
rahasia = random.randint(1, 100)
# ... lanjutkan!
```

---

## Pertemuan Depan

### Python — List & Fungsi
> List (array di Python) + fungsi (def)

---

# Terima Kasih

### MGMP Informatika SMAN 6 Cimahi

> "Perulangan: lakukan yang benar berulang kali, dan hasil besar akan datang."
