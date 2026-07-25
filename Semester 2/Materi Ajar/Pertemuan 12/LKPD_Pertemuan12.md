# LEMBAR KERJA PESERTA DIDIK (LKPD)
## Pertemuan 12 – Python: Variabel, Tipe Data, Input/Output, Percabangan

| TP | BK 1.4, BK 2.1 |
|---|---|
| Nama | ____________________ |
| Kelas | ____________________ |

**Cara menjalankan Python:**
- **Online**: Buka `colab.research.google.com` → Login → `+ New notebook` → ketik kode di sel → `Shift+Enter`
- **IDLE**: Start Menu → Python → IDLE

---

### A. HELLO, WORLD! & VARIABEL (10 menit)

**Soal 1:** Jalankan program pertama! Ketik di sel/IDLE:

```python
print("Hello, World!")
```

Ada output? _________

**Soal 2:** Buat variabel dan cek tipenya. Ketik dan jalankan:

```python
nama = "Namaku"
umur = 16
tinggi = 160.5
lulus = True

print(nama)
print(type(nama))
print(type(umur))
print(type(tinggi))
print(type(lulus))
```

Apa tipe data dari masing-masing?

| Variabel | Tipe |
|---|---|
| `nama` | |
| `umur` | |
| `tinggi` | |
| `lulus` | |

**Soal 3:** Buat variabel sesuai data dirimu, lalu print!

```python
nama = "______"
kelas = "______"
hobi = "______"
print(f"Nama: {nama}")
print(f"Kelas: {kelas}")
print(f"Hobi: {hobi}")
```

---

### B. INPUT & OUTPUT (10 menit)

**Soal 4:** Program menyapa. Jalankan dan catat output!

```python
nama = input("Siapa namamu? ")
print(f"Halo, {nama}! Selamat belajar Python!")
```

Input: _________
Output: _________

**Soal 5:** Program menjumlahkan dua angka.

```python
a = int(input("Masukkan a: "))
b = int(input("Masukkan b: "))
hasil = a + b
print(f"{a} + {b} = {hasil}")
```

Input: a=12, b=7
Output: _________

**Soal 6:** Celcius ke Fahrenheit. Translasi dari pseudocode!

| Pseudocode | Python |
|---|---|
| `INPUT celcius` | `celcius = float(input("Celcius: "))` |
| `fahrenheit ← celcius × 9/5 + 32` | `fahrenheit = celcius * 9/5 + 32` |
| `OUTPUT fahrenheit` | `print(f"Fahrenheit: {fahrenheit}")` |

Ketik dan jalankan!
```
Celcius: 100
```
Output: _________

```
Celcius: 0
```
Output: _________

---

### C. IF-ELIF-ELSE (10 menit)

**Soal 7:** Genap/ganjil. Translasi pseudocode → Python.

```python
x = int(input("Masukkan angka: "))

if x % 2 == 0:
    print("Genap")
else:
    print("Ganjil")
```

| Input | Output |
|---|---|
| 7 | |
| 10 | |
| 0 | |

**Soal 8:** Nilai → huruf mutu. Translasi dari Pertemuan 9!

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

| Input | Output |
|---|---|
| 95 | |
| 88 | |
| 70 | |

---

### D. TRANSLASI PSEUDOCODE → PYTHON

**Soal 9:** Translasi pseudocode berikut ke Python!

```
PROGRAM cek_suhu
    INPUT suhu
    IF suhu > 30 THEN
        OUTPUT "Panas"
    ELSE
        IF suhu < 20 THEN
            OUTPUT "Dingin"
        ELSE
            OUTPUT "Sejuk"
        ENDIF
    ENDIF
END
```

```python
# Program cek_suhu

suhu = float(input("Masukkan suhu: "))

if ________:
    print("Panas")
_____ suhu < 20:
    print("______")
else:
    print("______")
```

Test: suhu=35 → ______, suhu=15 → ______, suhu=25 → ______

**Soal 10:** Translasi pseudocode diskon belanja ke Python!

```
PROGRAM diskon_belanja
    INPUT total_belanja
    IF total_belanja > 100000 THEN
        diskon ← total_belanja × 0.1
        total_bayar ← total_belanja - diskon
    ELSE
        total_bayar ← total_belanja
    ENDIF
    OUTPUT "Total bayar: ", total_bayar
END
```

```python
# Program diskon_belanja

total_belanja = ________________

if ________________:
    diskon = ________________
    total_bayar = ________________
else:
    total_bayar = ________________

print(f"________________")
```

---

### E. REFLEKSI

| Pertanyaan | Jawaban |
|---|---|
| Apa perbedaan utama pseudocode dan Python? | |
| Apa arti indentasi di Python? | |
| Kenapa perlu `int(input())` bukan `input()` saja? | |
| Kesulitan yang dihadapi? | |
| Skala pemahaman (1–10) | / 10 |

---

### F. TUGAS RUMAH

Translasi 3 pseudocode berikut ke Python, jalankan, dan catat outputnya!

**1. Bilangan terbesar dari 3 angka (Pert 9)**
```python
# Tulis di buku tugas
```

**2. Total 1+2+...+n dengan FOR (Pert 10)**
```python
# Tulis di buku tugas
```

**3. Faktorial n! (Pert 10)**
```python
# Tulis di buku tugas
```

---

**MGMP Informatika SMAN 6 Cimahi**
