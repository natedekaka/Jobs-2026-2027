# BAHAN AJAR – PERTEMUAN 8 (S1)
## Flowchart - Perulangan
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*



### 🧠 Memahami — Membangun Pemahaman Awal

## A. Tujuan Pembelajaran
Setelah mempelajari materi ini, siswa mampu:
1. Menjelaskan konsep perulangan (loop) dalam flowchart
2. Membuat flowchart dengan FOR loop
3. Membuat flowchart dengan WHILE loop
4. Membuat flowchart dengan loop bersarang

## B. Konsep Perulangan (Loop)
Perulangan memungkinkan algoritma menjalankan blok instruksi berulang kali. Dalam flowchart, perulangan digambarkan dengan panah kembali ke langkah sebelumnya (back loop).

**Jenis Perulangan:**
| Jenis | Ciri | Kapan Digunakan |
|-------|------|-----------------|
| FOR | Jumlah perulangan diketahui | range(1, 11) — 10 kali |
| WHILE | Berhenti berdasarkan kondisi | while tebakan != benar |
| Repeat-Until | Minimal sekali | do...while (jarang) |

## C. Flowchart FOR Loop
**Contoh 1: Cetak 1-5**
```
[Start] -> [i = 1] -> <i <= 5?> --Ya--> [Output i] -> [i = i + 1] --kembali ke kondisi-->
                       --Tidak--> [End]
```

**Contoh 2: Cetak Bilangan Genap 2-10**
```
[Start] -> [i = 2] -> <i <= 10?> --Ya--> [Output i] -> [i = i + 2] --kembali-->
                       --Tidak--> [End]
```

## D. Flowchart WHILE Loop
**Contoh 3: Tebak Angka**
```
[Start] -> [komputer = random 1-10] -> [Input tebakan]
-> <tebakan != komputer?> --Ya--> [Input ulang tebakan] --kembali-->
         --Tidak--> [Output "Benar!"] -> [End]
```

**Contoh 4: Hitung Mundur**
```
[Start] -> [Input n] -> <n > 0?> --Ya--> [Output n] -> [n = n - 1] --kembali-->
                       --Tidak--> [Output "Go!"] -> [End]
```

## E. Flowchart Akumulasi (Running Total)
**Contoh 5: Jumlah 1-100**
```
[Start] -> [total = 0] -> [i = 1] -> <i <= 100?>
   --Ya--> [total = total + i] -> [i = i + 1] --kembali-->
   --Tidak--> [Output total] -> [End]
```

**Contoh 6: Rata-rata N Nilai**
```
[Start] -> [Input n] -> [total = 0] -> [i = 1]
-> <i <= n?> --Ya--> [Input nilai] -> [total = total + nilai] -> [i = i + 1] --kembali-->
   --Tidak--> [rata = total / n] -> [Output rata] -> [End]
```

## F. Flowchart Break dalam Loop
**Contoh 7: Cari Angka dalam List**
```
[Start] -> [Input cari] -> [i = 0] -> <i < panjang_list?>
   --Ya--> <list[i] == cari?> --Ya--> [Output "Ditemukan"] -> [Break] -> [End]
         --Tidak--> [i = i + 1] --kembali-->
   --Tidak--> [Output "Tidak ditemukan"] -> [End]
```

## G. Flowchart Loop Bersarang (Nested Loop)
**Contoh 8: Tabel Perkalian 3x3**
```
[Start] -> [baris = 1] -> <baris <= 3?> --Ya--> [kolom = 1]
   -> <kolom <= 3?> --Ya--> [hitung = baris * kolom] -> [Output hitung]
   -> [kolom = kolom + 1] --kembali ke kondisi kolom-->
   --Tidak--> [baris = baris + 1] --kembali ke kondisi baris-->
   --Tidak--> [End]
```


### 🔧 Mengaplikasi — Praktik & Penerapan

## H. Latihan
Buat flowchart untuk:
1. Cetak bilangan ganjil 1-19
2. Hitung jumlah bilangan genap 1-50
3. Input n, cetak faktorial n! (n * n-1 * ... * 1)
4. Cetak pola bintang (segitiga siku)
5. Menu: pilih 1-4, loop sampai pilih 4 (keluar)


### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagaimana konsep ini terkait dengan materi sebelumnya?
- Skala pemahaman diri: ___/10
- Apa yang ingin kamu pelajari lebih lanjut?

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) S1 Pert 8**
