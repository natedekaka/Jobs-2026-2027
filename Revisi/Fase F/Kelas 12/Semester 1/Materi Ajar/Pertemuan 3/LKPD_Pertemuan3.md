# LKPD Pert 3 (S1) – Fungsi Statistik & Logika
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*
| Nama | ____________________ |
|---|---|
| Kelas | ____________________ |





### 🧠 Memahami — Membangun Pemahaman Awal

### Aktivitas 1 — COUNTIF, SUMIF, AVERAGEIF (Individu, 25 menit)
Data 30 siswa: Kelas, Gender, Nilai.
=COUNTIF(Kelas,"XI-A") -> jumlah siswa XI-A
=SUMIF(Kelas,"XI-A",Nilai) -> total nilai XI-A
=AVERAGEIF(Kelas,"XI-A",Nilai) -> rata nilai XI-A

### Aktivitas 2 — COUNTIFS, SUMIFS, AVERAGEIFS (Berpasangan, 25 menit)
=COUNTIFS(Kelas,"XI-A",Gender,"L") -> siswa XI-A laki-laki
=SUMIFS(Nilai,Kelas,"XI-A",Gender,"L") -> total nilai XI-A laki-laki
=AVERAGEIFS(Nilai,Kelas,"XI-A",Gender,"L") -> rata nilai XI-A laki-laki

### Aktivitas 3 — IF dengan AND/OR (Individu, 20 menit)
=IF(AND(nilai>=70,absen>=80),"Lulus","Tidak Lulus")
=IF(OR(hari="Sabtu",hari="Minggu"),"Libur","Masuk")





### 🔧 Mengaplikasi — Praktik & Penerapan

### Aktivitas 4 — IFERROR (Kelompok, 15 menit)
=IFERROR(VLOOKUP(A2,Table,2,FALSE),"Data tidak ada")
Uji: cari ID yang tidak ada di tabel, pastikan tidak error #N/A!


d) Bandingkan dengan SUBTOTAL — sama atau beda? ___
c) Pilih fungsi: Average, Count, Sum, Max, Min di setiap kolom
b) Design > Total Row
a) Ctrl+T untuk membuat Table
e) Buat baris SUBTOTAL di atas data, filter kelas, lihat perubahannya!
d) =SUBTOTAL(2, range) untuk COUNT yang terfilter
c) =SUBTOTAL(1, range) untuk AVERAGE yang terfilter
b) Filter data: centang hanya XI-A. SUBTOTAL berubah? ___ SUM berubah? ___
a) =SUBTOTAL(9, range) vs =SUM(range) — apa bedanya? ___
c) Buat rumus: IF usia >=17 AND sudah_voting="Ya" THEN "Pemilih" ELSE "Bukan Pemilih"
b) =IF(AND(gender="L",nilai>=70),"Lulus","Tidak Lulus") — untuk apa? ___
a) Apa bedanya dengan IF(nilai<70,"Remedial","Lulus")? ___
=IF(NOT(nilai>=70),"Remedial","Lulus")
d) Jumlah siswa XI-A lulus: =COUNTIFS(Kelas,"XI-A",Nilai,">=70") -> ___
c) Rata-rata nilai Laki-laki XI-A: =AVERAGEIFS(Nilai,Kelas,"XI-A",Gender,"L") -> ___
b) Jumlah siswa XI-A: =COUNTIF(Kelas,"XI-A") -> ___
a) Rata-rata nilai kelas XI-A: =AVERAGEIF(Kelas,"XI-A",Nilai) -> ___
Hitung manual, lalu cek rumus:
Data nilai ujian 30 siswa: Kelas (XI-A / XI-B / XI-C), Gender (L/P), Nilai (0-100).
Skala: ___/10. Rumus tersulit: _________________
Skala: ___/10. Rumus tersulit: _________________

### Aktivitas 5 — Studi Kasus Nilai Ujian (Individu, 15 menit)
Data nilai ujian 30 siswa: Kelas (XI-A / XI-B / XI-C), Gender (L/P), Nilai (0-100).
Hitung manual, lalu cek rumus:
a) Rata-rata nilai kelas XI-A: =AVERAGEIF(Kelas,"XI-A",Nilai) -> ___
b) Jumlah siswa XI-A: =COUNTIF(Kelas,"XI-A") -> ___
c) Rata-rata nilai Laki-laki XI-A: =AVERAGEIFS(Nilai,Kelas,"XI-A",Gender,"L") -> ___
d) Jumlah siswa XI-A lulus: =COUNTIFS(Kelas,"XI-A",Nilai,">=70") -> ___

### Aktivitas 6 — IF dengan NOT (Berpasangan, 15 menit)
=IF(NOT(nilai>=70),"Remedial","Lulus")
a) Apa bedanya dengan IF(nilai<70,"Remedial","Lulus")? ___
b) =IF(AND(gender="L",nilai>=70),"Lulus","Tidak Lulus") — untuk apa? ___
c) Buat rumus: IF usia >=17 AND sudah_voting="Ya" THEN "Pemilih" ELSE "Bukan Pemilih"

### Aktivitas 7 — SUBTOTAL vs SUM (Individu, 15 menit)
a) =SUBTOTAL(9, range) vs =SUM(range) — apa bedanya? ___
b) Filter data: centang hanya XI-A. SUBTOTAL berubah? ___ SUM berubah? ___
c) =SUBTOTAL(1, range) untuk AVERAGE yang terfilter
d) =SUBTOTAL(2, range) untuk COUNT yang terfilter
e) Buat baris SUBTOTAL di atas data, filter kelas, lihat perubahannya!

### Aktivitas 8 — Tabel dengan Total Row (Individu, 10 menit)
a) Ctrl+T untuk membuat Table
b) Design > Total Row
c) Pilih fungsi: Average, Count, Sum, Max, Min di setiap kolom
d) Bandingkan dengan SUBTOTAL — sama atau beda? ___



- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagian mana yang masih sulit dipahami?
- Skala pemahaman diri: ___/10


### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagian mana yang masih sulit dipahami?
- Skala pemahaman diri: ___/10

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XII) Semester 1**
