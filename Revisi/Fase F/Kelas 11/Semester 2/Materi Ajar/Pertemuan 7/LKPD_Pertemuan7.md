# LKPD Pert 7 (S2) – Fungsi
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*
| Nama | ____________________ |
|---|---|
| Kelas | ____________________ |





### 🧠 Memahami — Membangun Pemahaman Awal

### Aktivitas 1 — Fungsi Sederhana (Individu, 20 menit)
```python
def sapa():
    print("Halo! Selamat belajar!")
sapa()
```
Buat fungsi "ucapin(nama)" yang menerima parameter nama dan mencetak "Halo [nama]!".

### Aktivitas 2 — Fungsi dengan Return (Berpasangan, 20 menit)
```python
def luas_persegi(sisi):
    return sisi * sisi
print(luas_persegi(5))  # ?
```
Buat fungsi "luas_lingkaran(r)" return 3.14 * r * r. Uji dengan r=7.





### 🔧 Mengaplikasi — Praktik & Penerapan

### Aktivitas 3 — Fungsi Cek Genap (Individu, 20 menit)
Buat fungsi "cek_genap(angka)" return True jika genap, False jika ganjil.
Gunakan dalam IF: if cek_genap(10): print("Genap!")


```
mundur(5)  # ?
    print("Go!")
        print(i)
    for i in range(n, 0, -1):
def mundur(n):
```python
Buat fungsi "mundur(n)" yang mencetak n, n-1, ..., 1, "Go!" menggunakan FOR.
```
sapa()         # ?
sapa("Andi")   # ?
    print(f"Halo {nama}!")
def sapa(nama="Teman"):
```python
Skala: ___/10. Fungsi: _________________
### Aktivitas 4 — Program Kalkulator dalam Fungsi (Kelompok, 20 menit)
```python
def kalkulator(a, b, op):
    if op == "+": return a + b
    elif op == "-": return a - b
    elif op == "*": return a * b
    elif op == "/": return a / b if b != 0 else "Error"
print(kalkulator(10, 3, "+"))  # ?
print(kalkulator(10, 3, "*"))  # ?
```

### Aktivitas 5 — Tantangan (Individu, 10 menit)
Buat fungsi "faktorial(n)" return n! (n * n-1 * ... * 1). Uji: faktorial(5)=?

Skala: ___/10. Fungsi: _________________

### Aktivitas 6 — Fungsi dengan Default Parameter (Individu, 10 menit)
```python
def sapa(nama="Teman"):
    print(f"Halo {nama}!")
sapa("Andi")   # ?
sapa()         # ?
```

### Aktivitas 7 — Program Hitung Mundur (Berpasangan, 10 menit)
Buat fungsi "mundur(n)" yang mencetak n, n-1, ..., 1, "Go!" menggunakan FOR.
```python
def mundur(n):
    for i in range(n, 0, -1):
        print(i)
    print("Go!")
mundur(5)  # ?
```



- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagian mana yang masih sulit dipahami?
- Skala pemahaman diri: ___/10


### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagian mana yang masih sulit dipahami?
- Skala pemahaman diri: ___/10

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 2**
