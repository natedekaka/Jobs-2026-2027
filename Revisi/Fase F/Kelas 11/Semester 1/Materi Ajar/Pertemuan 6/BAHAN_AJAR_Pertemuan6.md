# BAHAN AJAR – PERTEMUAN 6 (S1)
## Flowchart - Urutan & I/O
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*



### 🧠 Memahami — Membangun Pemahaman Awal

## A. Tujuan Pembelajaran
Setelah mempelajari materi ini, siswa mampu:
1. Menjelaskan konsep flowchart dan fungsinya dalam algoritma
2. Mengidentifikasi simbol-simbol flowchart standar
3. Membuat flowchart untuk algoritma urutan (sequence) sederhana
4. Membuat flowchart dengan input, proses, dan output

## B. Pengertian Flowchart
Flowchart (diagram alir) adalah representasi grafis dari langkah-langkah suatu algoritma atau proses. Flowchart menggunakan simbol-simbol standar untuk menunjukkan urutan, input/output, dan keputusan.

**Mengapa Flowchart Penting?**
1. Memvisualisasikan algoritma sebelum coding
2. Memudahkan komunikasi antar programmer
3. Membantu menemukan error logika (debugging)
4. Dokumentasi program yang mudah dipahami

**Aturan Membuat Flowchart:**
1. Mulai dengan simbol START/END (terminal)
2. Tiap langkah ditulis dalam satu simbol
3. Gunakan panah untuk menunjukkan alur
4. Satu jalur masuk, satu jalur keluar (kecuali percabangan)
5. Sederhana dan jelas — hindari overlapping garis

## C. Simbol Flowchart Standar
| Simbol | Nama | Fungsi |
|--------|------|--------|
| Oval / Terminator | Mulai / Selesai program |
| Persegi Panjang | Proses | Operasi/perhitungan |
| Jajar Genjang | Input/Output | Baca data / Tampilkan hasil |
| Belah Ketupat | Keputusan | Percabangan (Ya/Tidak) |
| Lingkaran | Penghubung | Sambungan halaman |
| Panah | Alur | Menunjukkan urutan langkah |

## D. Flowchart Urutan (Sequence)
Urutan (sequence) adalah struktur algoritma paling sederhana — langkah dieksekusi berurutan dari atas ke bawah.

**Contoh 1: Flowchart "Sapa Pengguna"**
```
[Start] -> [Input nama] -> [Output "Halo, nama"] -> [End]
```

**Contoh 2: Flowchart Luas Persegi Panjang**
```
[Start] -> [Input panjang] -> [Input lebar] -> [luas = p * l] -> [Output luas] -> [End]
```

**Contoh 3: Flowchart Konversi Suhu**
```
[Start] -> [Input celcius] -> [fahren = celcius * 9/5 + 32] -> [Output fahren] -> [End]
```

## E. Flowchart dengan I/O (Input/Output)
Input/output adalah bagian penting dari program interaktif.

**Jenis I/O:**
| Jenis | Simbol | Contoh |
|-------|--------|--------|
| Input | Jajar Genjang | input(nama), input(usia) |
| Output | Jajar Genjang | print(nama), print("Halo") |

**Contoh 4: Flowchart Data Diri**
```
[Start] -> [Input nama] -> [Input usia] -> [Input kota]
-> [Tampilkan biodata] -> [End]
```

**Contoh 5: Flowchart Hitung Rata-rata**
```
[Start] -> [Input nilai1] -> [Input nilai2] -> [Input nilai3]
-> [rata = (nilai1 + nilai2 + nilai3) / 3]
-> [Output rata] -> [End]
```

## F. Flowchart Gabungan (Urutan + I/O)
**Contoh 6: Flowchart Kalkulator Sederhana**
```
[Start] -> [Input a] -> [Input b]
-> [jumlah = a + b] -> [selisih = a - b]
-> [kali = a * b] -> [Output jumlah, selisih, kali] -> [End]
```

**Contoh 7: Flowchart Luas Lingkaran**
```
[Start] -> [Input r] -> [luas = 3.14 * r * r] -> [Output luas] -> [End]
```


### 🔧 Mengaplikasi — Praktik & Penerapan

## G. Latihan
Buat flowchart untuk:
1. Program: input nama, cetak "Halo [nama]!"
2. Program: input 2 angka, cetak hasil penjumlahan dan perkalian
3. Program: input panjang & lebar, hitung & cetak luas persegi panjang
4. Program: input jam & menit, konversi ke total menit
5. Program: input nilai dalam rupiah, konversi ke dolar (kurs 1 USD = 15000 IDR)


### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagaimana konsep ini terkait dengan materi sebelumnya?
- Skala pemahaman diri: ___/10
- Apa yang ingin kamu pelajari lebih lanjut?

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) S1 Pert 6**
