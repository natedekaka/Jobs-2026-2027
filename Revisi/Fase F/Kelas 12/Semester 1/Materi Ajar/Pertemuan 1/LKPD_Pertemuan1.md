# LKPD Pert 1 (S1) – Review Excel
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*
| Nama | ____________________ |
|---|---|
| Kelas | ____________________ |





### 🧠 Memahami — Membangun Pemahaman Awal

### Aktivitas 1 — Review Fungsi Dasar (Individu, 20 menit)
Buat data 15 siswa: No, Nama, Nilai.
Hitung: =AVERAGE(range), =MAX(range), =MIN(range), =COUNTIF(range,">=70")

### Aktivitas 2 — IF & VLOOKUP (Berpasangan, 25 menit)
Buat 2 tabel: Tabel1(ID,Nama,Kelas), Tabel2(ID,Nilai).
=VLOOKUP(A2,Table1!A:C,2,FALSE) untuk ambil nama.
=IF(nilai>=70,"Lulus","Tidak Lulus") untuk status.




### 🔧 Mengaplikasi — Praktik & Penerapan

### Aktivitas 3 — Format Tabel Profesional (Individu, 20 menit)
Buat tabel 20 baris data penjualan: Tanggal, Produk, Kategori, Qty, Harga, Total.
Terapkan: Ctrl+T (Table), Freeze Panes, Number Format Rp, Wrap Text.


### Aktivitas 4 — Studi Kasus (Kelompok, 20 menit)
Buat laporan: rata-rata nilai per kelas (AVERAGEIF), jumlah lulus per kelas (COUNTIFS).


e) Produk apa dengan total tertinggi? ___
d) Buat Pivot: Rows=Produk, Values=Sum Total
Dari data penjualan 20 baris:
c) Berapa rata-rata nilai XI-A? ___
b) Filter: tampilkan hanya kelas XI-A
a) Buat PivotTable: Rows=Kelas, Values=Average Nilai
Dari data 15 siswa:
b) Hitung jumlah siswa LULUS (>=70) dan TIDAK LULUS (<70)
a) Berapa siswa dapat A? ___ B? ___ C? ___ D? ___
=IF(E2>=85,"A",IF(E2>=70,"B",IF(E2>=55,"C","D")))
Buat kolom Grade dengan IF bertingkat:
e) Jumlah siswa tidak lulus: =COUNTIF(E2:E16,"<70") -> ___
d) Jumlah siswa lulus (>=70): =COUNTIF(E2:E16,">=70") -> ___
c) Nilai terendah: Manual: ___ =MIN(E2:E16) -> ___
b) Nilai tertinggi: Manual: ___ =MAX(E2:E16) -> ___
a) Rata-rata nilai kelas: Manual: ___ =AVERAGE(E2:E16) -> ___
Dari data 15 siswa, hitung manual lalu cek dengan rumus:
Skala: ___/10. Rumus yang masih lupa: _________________
Skala: ___/10. Rumus yang masih lupa: _________________

### Aktivitas 5 — Hitung Manual + Rumus (Individu, 15 menit)
Dari data 15 siswa, hitung manual lalu cek dengan rumus:
a) Rata-rata nilai kelas: Manual: ___ =AVERAGE(E2:E16) -> ___
b) Nilai tertinggi: Manual: ___ =MAX(E2:E16) -> ___
c) Nilai terendah: Manual: ___ =MIN(E2:E16) -> ___
d) Jumlah siswa lulus (>=70): =COUNTIF(E2:E16,">=70") -> ___
e) Jumlah siswa tidak lulus: =COUNTIF(E2:E16,"<70") -> ___

### Aktivitas 6 — IF Bertingkat (Berpasangan, 15 menit)
Buat kolom Grade dengan IF bertingkat:
=IF(E2>=85,"A",IF(E2>=70,"B",IF(E2>=55,"C","D")))
a) Berapa siswa dapat A? ___ B? ___ C? ___ D? ___
b) Hitung jumlah siswa LULUS (>=70) dan TIDAK LULUS (<70)

### Aktivitas 7 — PivotTable Review (Individu, 15 menit)
Dari data 15 siswa:
a) Buat PivotTable: Rows=Kelas, Values=Average Nilai
b) Filter: tampilkan hanya kelas XI-A
c) Berapa rata-rata nilai XI-A? ___
Dari data penjualan 20 baris:
d) Buat Pivot: Rows=Produk, Values=Sum Total
e) Produk apa dengan total tertinggi? ___



- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagian mana yang masih sulit dipahami?
- Skala pemahaman diri: ___/10


### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagian mana yang masih sulit dipahami?
- Skala pemahaman diri: ___/10

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XII) Semester 1**

### Aktivitas 8 — Format Angka & Tanggal (Individu, 10 menit)
a) Format kolom Total sebagai Rp: Right Click > Format Cells > Currency > Rp
b) Format kolom Tanggal sebagai Long Date: Format Cells > Date > 14 March 2025
c) Atur lebar kolom: AutoFit (double-click between column headers)
d) Wrap Text untuk header yang panjang
e) Freeze Panes: Select row 2 > View > Freeze Panes > Freeze Top Row
