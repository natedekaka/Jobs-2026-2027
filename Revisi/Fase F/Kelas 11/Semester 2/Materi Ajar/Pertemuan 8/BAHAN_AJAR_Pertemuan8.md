# BAHAN AJAR – PERTEMUAN 8 (S2)
## Program Sederhana 1
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*



### 🧠 Memahami — Membangun Pemahaman Awal

## A. Tujuan Pembelajaran
Setelah mempelajari materi ini, siswa mampu:
1. Membuat program Python utuh: input + proses + output
2. Membuat program kalkulator sederhana
3. Membuat program konversi suhu
4. Membuat program cek BMI

## B. Program 1: Kalkulator Sederhana
```python
def kalkulator():
    print("=" * 30)
    print("KALKULATOR SEDERHANA")
    print("=" * 30)
    print("1. Penjumlahan (+)")
    print("2. Pengurangan (-)")
    print("3. Perkalian (*)")
    print("4. Pembagian (/)")
    print("5. Pangkat (**)")

    pilihan = input("Pilih operasi (1-5): ")
    a = float(input("Angka pertama: "))
    b = float(input("Angka kedua: "))

    if pilihan == "1":
        print(f"{a} + {b} = {a + b}")
    elif pilihan == "2":
        print(f"{a} - {b} = {a - b}")
    elif pilihan == "3":
        print(f"{a} * {b} = {a * b}")
    elif pilihan == "4":
        if b != 0:
            print(f"{a} / {b} = {a / b:.2f}")
        else:
            print("ERROR: Tidak bisa dibagi nol!")
    elif pilihan == "5":
        print(f"{a} ** {b} = {a ** b}")

kalkulator()
```

## C. Program 2: Konversi Suhu
```python
def konversi_suhu():
    print("KONVERSI SUHU")
    print("1. C -> F")
    print("2. F -> C")
    print("3. C -> K")
    pilihan = input("Pilih (1-3): ")
    suhu = float(input("Suhu: "))
    if pilihan == "1":
        print(f"{suhu}C = {suhu*9/5+32:.1f}F")
    elif pilihan == "2":
        print(f"{suhu}F = {(suhu-32)*5/9:.1f}C")
    elif pilihan == "3":
        print(f"{suhu}C = {suhu+273.15:.1f}K")
konversi_suhu()
```

## D. Program 3: Cek BMI
```python
def hitung_bmi(berat, tinggi):
    return berat / (tinggi ** 2)

def kategori_bmi(bmi):
    if bmi < 18.5: return "Kurus"
    elif bmi < 25: return "Ideal"
    elif bmi < 30: return "Gemuk"
    else: return "Obesitas"

nama = input("Nama: ")
berat = float(input("Berat (kg): "))
tinggi = float(input("Tinggi (cm): ")) / 100
bmi = hitung_bmi(berat, tinggi)
print(f"BMI {nama}: {bmi:.1f} ({kategori_bmi(bmi)})")
```

## E. Program 4: Bilangan Prima
```python
def cek_prima(n):
    if n < 2: return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0: return False
    return True

for i in range(1, 51):
    if cek_prima(i):
        print(i, end=" ")
```

## F. Tantangan
1. Kalkulator + history perhitungan + loop
2. Konversi suhu lengkap (C, F, K, R)
3. BMI + kategori + saran kesehatan
4. Bilangan prima dalam range input user
5. Program nilai: total, rata-rata, max, min, predikat


### 🔧 Mengaplikasi — Praktik & Penerapan

### Latihan Pemahaman
1. Jelaskan konsep utama yang telah dipelajari dengan bahasamu sendiri!
2. Berikan 2 contoh penerapan dalam kehidupan sehari-hari!
3. Diskusikan dengan teman: bagaimana materi ini dapat membantu menyelesaikan masalah nyata?

### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagaimana konsep ini terkait dengan materi sebelumnya?
- Skala pemahaman diri: ___/10
- Apa yang ingin kamu pelajari lebih lanjut?

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) S2 Pert 8**
