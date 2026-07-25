# BAHAN AJAR – PERTEMUAN 7 (S1)
## Flowchart - Percabangan
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*



### 🧠 Memahami — Membangun Pemahaman Awal

## A. Tujuan Pembelajaran
Setelah mempelajari materi ini, siswa mampu:
1. Menjelaskan konsep percabangan dalam flowchart
2. Membuat flowchart dengan struktur IF-THEN-ELSE
3. Membuat flowchart dengan IF bertingkat dan AND/OR

## B. Konsep Percabangan (Branching)
Percabangan memungkinkan algoritma mengambil keputusan berdasarkan kondisi tertentu. Dalam flowchart, percabangan digambarkan dengan simbol belah ketupat (decision).

**Simbol Keputusan:**
- Masuk dari atas
- Pertanyaan/kondisi di dalam simbol (misal: usia >= 17?)
- Dua jalur keluar: Ya (True) dan Tidak (False)

## C. Flowchart IF Sederhana
**Contoh 1: Cek Usia**
```
[Start] -> [Input usia] -> <usia >= 17?> --Ya--> [Output "Cukup umur"]
                                                       |
                                                       +--> [End]
                              --Tidak--> [Output "Belum cukup"] -> [End]
```

**Flowchart dalam bentuk langkah:**
1. Start
2. Input usia
3. Jika usia >= 17, maka: Output "Cukup umur"
4. Jika tidak: Output "Belum cukup"
5. End

## D. Flowchart IF-ELSE
**Contoh 2: Cek Genap/Ganjil**
```
[Start] -> [Input angka] -> <angka % 2 == 0?>
        --Ya--> [Output "Genap"] -> [End]
        --Tidak--> [Output "Ganjil"] -> [End]
```

**Contoh 3: Cek Kelulusan**
```
[Start] -> [Input nilai] -> <nilai >= 70?>
        --Ya--> [Output "Lulus"] -> [End]
        --Tidak--> [Output "Tidak Lulus"] -> [End]
```

## E. Flowchart IF-ELIF-ELSE
**Contoh 4: Predikat Nilai**
```
[Start] -> [Input nilai] -> <nilai >= 85?>
   --Ya--> [Output "A"] -> [End]
   --Tidak--> <nilai >= 70?>
        --Ya--> [Output "B"] -> [End]
        --Tidak--> <nilai >= 55?>
             --Ya--> [Output "C"] -> [End]
             --Tidak--> [Output "D"] -> [End]
```

**Contoh 5: Kategori Usia**
```
[Start] -> [Input usia] -> <usia <= 5?>
   --Ya--> [Output "Balita"] -> [End]
   --Tidak--> <usia <= 12?>
        --Ya--> [Output "Anak"] -> [End]
        --Tidak--> <usia <= 17?>
             --Ya--> [Output "Remaja"] -> [End]
             --Tidak--> [Output "Dewasa"] -> [End]
```

## F. Flowchart dengan Logika AND/OR
**Contoh 6: Cek Kesehatan (AND)**
```
[Start] -> [Input suhu] -> [Input batuk]
-> <suhu > 37.5 AND batuk == "ya"?>
   --Ya--> [Output "Periksa dokter"] -> [End]
   --Tidak--> [Output "Sehat"] -> [End]
```

**Contoh 7: Cek Hari (OR)**
```
[Start] -> [Input hari]
-> <hari == "Sabtu" OR hari == "Minggu"?>
   --Ya--> [Output "Libur"] -> [End]
   --Tidak--> [Output "Masuk"] -> [End]
```


### 🔧 Mengaplikasi — Praktik & Penerapan

## G. Latihan
Buat flowchart untuk:
1. Input angka -> cetak "Positif", "Negatif", atau "Nol"
2. Input tahun -> cek kabisat (habis dibagi 4 DAN (tidak habis dibagi 100 ATAU habis dibagi 400))
3. Input 3 angka -> cari yang terbesar (nested if)
4. Input nilai dan absen -> jika nilai >= 70 DAN absen >= 80 maka "Lulus"
5. Input suhu -> jika > 37.5 demam, jika 36.5-37.5 normal, jika < 36.5 hipotermia


### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagaimana konsep ini terkait dengan materi sebelumnya?
- Skala pemahaman diri: ___/10
- Apa yang ingin kamu pelajari lebih lanjut?

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) S1 Pert 7**
