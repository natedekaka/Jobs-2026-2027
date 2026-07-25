# BAHAN AJAR – PERTEMUAN 7 (S2)
## Fungsi
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*



### 🧠 Memahami — Membangun Pemahaman Awal

## A. Tujuan Pembelajaran
Setelah mempelajari materi ini, siswa mampu:
1. Mendefinisikan dan memanggil fungsi dengan def
2. Menggunakan parameter dan return value
3. Menerapkan konsep scope (lokal vs global)
4. Membuat fungsi dengan parameter default

## B. Apa Itu Fungsi?
Fungsi adalah blok kode yang bisa dipanggil berkali-kali. Tujuannya: DRY (Don't Repeat Yourself).

## C. Fungsi Tanpa Parameter
```python
def sapa():
    print("Halo! Selamat datang!")
sapa()
sapa()  # bisa dipanggil berkali-kali
```

## D. Fungsi dengan Parameter
```python
def sapa_user(nama):
    print(f"Halo, {nama}!")

sapa_user("Andi")   # Halo, Andi!
sapa_user("Budi")   # Halo, Budi!
```

## E. Fungsi dengan Return
```python
def luas_persegi(sisi):
    return sisi * sisi

hasil = luas_persegi(5)
print(hasil)  # 25
```

**Contoh Cek Genap:**
```python
def cek_genap(angka):
    return angka % 2 == 0

print(cek_genap(4))  # True
if cek_genap(10):
    print("Genap!")
```

## F. Banyak Return
```python
def hitung(a, b):
    return a+b, a-b, a*b, a/b

j, s, k, bg = hitung(10, 3)
print(j, s, k, round(bg, 2))  # 13 7 30 3.33
```

## G. Parameter Default
```python
def sapa(nama="Teman"):
    print(f"Halo, {nama}!")
sapa("Andi")    # Halo, Andi!
sapa()          # Halo, Teman!
```

## H. Scope (Lokal vs Global)
```python
nama = "Andi"  # global
def sapa():
    nama = "Budi"  # lokal
    print("Halo", nama)
sapa()           # Halo Budi
print(nama)      # Andi
```

## I. Program Kalkulator dalam Fungsi
```python
def kalkulator():
    a = float(input("Angka pertama: "))
    b = float(input("Angka kedua: "))
    op = input("Operator (+, -, *, /): ")
    if op == "+": print(f"Hasil: {a + b}")
    elif op == "-": print(f"Hasil: {a - b}")
    elif op == "*": print(f"Hasil: {a * b}")
    elif op == "/":
        print("Error: bagi 0!" if b == 0 else f"Hasil: {a / b}")
kalkulator()
```


### 🔧 Mengaplikasi — Praktik & Penerapan

## J. Latihan
1. Fungsi sapa(nama) — cetak "Halo [nama]!"
2. Fungsi luas_lingkaran(r) — return phi * r**2
3. Fungsi cek_kabisat(tahun) — return True/False
4. Fungsi faktorial(n) — return n!
5. Program: fungsi BMI + kategori


### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagaimana konsep ini terkait dengan materi sebelumnya?
- Skala pemahaman diri: ___/10
- Apa yang ingin kamu pelajari lebih lanjut?

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) S2 Pert 7**
