# BAHAN AJAR – PERTEMUAN 4 (S2)
## IF — Percabangan
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*



### 🧠 Memahami — Membangun Pemahaman Awal

## A. Tujuan Pembelajaran
Setelah mempelajari materi ini, siswa mampu:
1. Menggunakan if, elif, else untuk percabangan
2. Membuat program dengan logika percabangan
3. Menggunakan operator logika dalam kondisi
4. Memahami perbedaan if dan elif

## B. IF Sederhana
```python
usia = 17
if usia >= 17:
    print("Kamu sudah cukup umur.")
```

## C. IF-ELSE
```python
if usia >= 17:
    print("Kamu sudah cukup umur.")
else:
    print("Kamu masih di bawah umur.")
```

**Contoh Genap/Ganjil:**
```python
angka = int(input("Masukkan angka: "))
if angka % 2 == 0:
    print(angka, "adalah bilangan genap")
else:
    print(angka, "adalah bilangan ganjil")
```

## D. IF-ELIF-ELSE
```python
nilai = int(input("Masukkan nilai: "))
if nilai >= 85:
    predikat = "A (Sangat Baik)"
elif nilai >= 70:
    predikat = "B (Baik)"
elif nilai >= 55:
    predikat = "C (Cukup)"
else:
    predikat = "D (Kurang)"
print("Predikat:", predikat)
```

## E. IF Bersarang (Nested IF)
```python
usia = int(input("Usia: "))
nilai = int(input("Nilai: "))

if usia >= 17:
    if nilai >= 70:
        print("Lulus dan cukup umur")
    else:
        print("Cukup umur tapi tidak lulus")
else:
    if nilai >= 70:
        print("Lulus tapi belum cukup umur")
    else:
        print("Tidak lulus dan belum cukup umur")
```

## F. IF dengan Logika AND/OR
```python
usia = int(input("Usia: "))
sehat = input("Sehat? (ya/tidak): ")
if usia >= 17 and sehat == "ya":
    print("Boleh ikut lomba")
else:
    print("Tidak boleh ikut lomba")
```

## G. Operator Ternary
```python
nilai = 75
status = "Lulus" if nilai >= 70 else "Tidak Lulus"
print(status)  # Lulus
```

## H. Program Lengkap — Cek Kesehatan
```python
print("=== CEK KESEHATAN ===")
suhu = float(input("Suhu tubuh: "))
batuk = input("Batuk? (ya/tidak): ")
if suhu > 37.5 and batuk == "ya":
    print("Periksa ke dokter!")
elif suhu > 37.5 or batuk == "ya":
    print("Istirahat di rumah")
else:
    print("Sehat walafiat")
```


### 🔧 Mengaplikasi — Praktik & Penerapan

## I. Latihan
1. Input nilai → cetak Lulus (>=70) atau Tidak Lulus
2. Input angka → cetak Positif, Negatif, atau Nol
3. Input tahun → cetak Kabisat atau Bukan Kabisat
4. Input usia → tentukan kategori: Balita 0-5, Anak 6-12, Remaja 13-17, Dewasa 18+
5. Gunakan ternary: input angka → cetak Genap/Ganjil


### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagaimana konsep ini terkait dengan materi sebelumnya?
- Skala pemahaman diri: ___/10
- Apa yang ingin kamu pelajari lebih lanjut?

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) S2 Pert 4**
