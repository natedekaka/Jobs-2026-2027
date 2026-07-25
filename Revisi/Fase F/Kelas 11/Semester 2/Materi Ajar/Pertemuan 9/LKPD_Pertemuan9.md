# LKPD Pert 9 (S2) – Program Sederhana 2
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*
| Nama | ____________________ |
|---|---|
| Kelas | ____________________ |





### 🧠 Memahami — Membangun Pemahaman Awal

### Aktivitas 1 — To-Do List (Individu, 25 menit)
Buat program: Menu 1.Lihat 2.Tambah 3.Hapus 4.Keluar. Gunakan list untuk menyimpan tugas.

### Aktivitas 2 — Pengelolaan Nilai (Berpasangan, 25 menit)
Input jumlah siswa, input nama+nilai tiap siswa. Output: total, rata-rata, max, min, jumlah lulus.

### Aktivitas 3 — Kuis Interaktif (Kelompok, 20 menit)
Buat kuis 3 soal: tanya jawab, beri skor di akhir.





### 🔧 Mengaplikasi — Praktik & Penerapan

### Aktivitas 4 — Refleksi Program (Individu, 15 menit)
Dari semua program yang dibuat (Kalkulator, BMI, To-Do List, Kuis), mana yang paling berguna? Mengapa?


Contoh: [1,3,2,3,1,3] -> "1 muncul 2 kali, 3 muncul 3 kali, 2 muncul 1 kali"
Output: "Angka X muncul Y kali".
Hitung berapa kali setiap angka muncul.
Buat program: input 10 angka ke list.
Gunakan manual search (loop), jangan pakai .index().
Cetak "Ditemukan di index ke-N" atau "Tidak ditemukan".
Buat program: input 10 angka ke list, lalu input angka yang dicari.
```
print(angka)
            angka[j], angka[j+1] = angka[j+1], angka[j]
        if angka[j] > angka[j+1]:
    for j in range(0, len(angka)-i-1):
for i in range(len(angka)):
angka = [5, 2, 8, 1, 9]
```python
Gunakan algoritma bubble sort sederhana.
Buat program: input 5 angka, urutkan dari terkecil ke terbesar.
JANGAN gunakan fungsi max(), min(), sum() bawaan Python. Gunakan loop manual!
Buat program: input 5 angka ke dalam list, lalu cetak nilai maksimum, minimum, dan rata-rata.
Skala: ___/10. Program favorit: _________________
Skala: ___/10. Program favorit: _________________

### Aktivitas 5 — Program Cari Nilai Max/Min (Individu, 20 menit)
Buat program: input 5 angka ke dalam list, lalu cetak nilai maksimum, minimum, dan rata-rata.
JANGAN gunakan fungsi max(), min(), sum() bawaan Python. Gunakan loop manual!

### Aktivitas 6 — Program Sorting Sederhana (Berpasangan, 20 menit)
Buat program: input 5 angka, urutkan dari terkecil ke terbesar.
Gunakan algoritma bubble sort sederhana.
```python
angka = [5, 2, 8, 1, 9]
for i in range(len(angka)):
    for j in range(0, len(angka)-i-1):
        if angka[j] > angka[j+1]:
            angka[j], angka[j+1] = angka[j+1], angka[j]
print(angka)
```

### Aktivitas 7 — Program Pencarian (Individu, 15 menit)
Buat program: input 10 angka ke list, lalu input angka yang dicari.
Cetak "Ditemukan di index ke-N" atau "Tidak ditemukan".
Gunakan manual search (loop), jangan pakai .index().

### Aktivitas 8 — Program Hitung Frekuensi (Berpasangan, 15 menit)
Buat program: input 10 angka ke list.
Hitung berapa kali setiap angka muncul.
Output: "Angka X muncul Y kali".
Contoh: [1,3,2,3,1,3] -> "1 muncul 2 kali, 3 muncul 3 kali, 2 muncul 1 kali"



- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagian mana yang masih sulit dipahami?
- Skala pemahaman diri: ___/10


### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagian mana yang masih sulit dipahami?
- Skala pemahaman diri: ___/10

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 2**

### Aktivitas 9 — Program Sorting (Individu, 10 menit)
Buat program: input 5 angka bebas, urutkan ascending (kecil ke besar) tanpa .sort().
Gunakan nested loop: for i in range(len(list)): for j in range(i+1, len(list)): if list[i] > list[j]: tukar.

### Bonus Challenge
Buat program: input 10 angka, hitung berapa bilangan positif, negatif, dan nol.
