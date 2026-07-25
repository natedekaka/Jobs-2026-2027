# LEMBAR KERJA PESERTA DIDIK (LKPD)
## Pertemuan 17 (S1) – PAS — Ujian Praktik Excel
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Nama | ____________________ |

|---|---|
| Kelas | ____________________ |

### Soal 1 — Format Data Siswa (25 menit)
Buat sheet "Data_Siswa" dengan kolom: No, NIS (text format, 7 digit), Nama, Tgl Lahir.
a) Format NIS: =LEFT(B2,4) & "-" & RIGHT(B2,3)
b) Usia: =DATEDIF(D2,TODAY(),"Y")
c) Email: =LOWER(LEFT(C2,1)) & "." & LOWER(MID(C2,FIND(" ",C2)+1,99)) & "@sma6.sch.id"
d) CF: usia >= 17 -> Green Fill, usia < 17 -> Yellow Fill

### Soal 2 — Validasi Data (20 menit)
a) NIS valid jika 7 digit: =IF(LEN(B2)=7,"Valid","Tidak Valid")
b) Email valid jika ada "@": =IF(ISNUMBER(FIND("@",E2)),"Valid","Tidak Valid")
c) Usia valid jika 0-100: =IF(AND(F2>=0,F2<=100),"Valid","Tidak Valid")
d) CF: "Tidak Valid" -> Red Fill

### Soal 3 — Statistik (15 menit)
Hitung:
a) Jumlah siswa: =COUNTA(range)
b) Rata-rata usia: =AVERAGE(range)
c) Usia tertinggi: =MAX(range)
d) Usia terendah: =MIN(range)
e) Jumlah siswa >= 17 tahun: =COUNTIF(range,">=17")

### Cek Jawaban (5 menit)
Periksa: format, rumus, CF. Pastikan tidak ada error #VALUE! atau #N/A.


Skala: ___/10. Soal tersulit: _____ Skor perkiraan: ___/100
### Soal 4 — CF & Format Tambahan (20 menit)
a) Tambahkan kolom "Status Usia": =IF(F2>=17,"Dewasa","Anak-anak")
b) CF: Status "Dewasa" -> Blue Fill, "Anak-anak" -> Orange Fill
c) Sort: Usia terbesar ke terkecil
d) Filter: tampilkan hanya siswa "Dewasa"
### Soal 5 — Print Setup (5 menit)
Atur: Page Layout > Orientation > Landscape
Margin: Narrow. Scaling: Fit to 1 page.
Print preview, pastikan semua kolom terlihat.
### Soal 6 — Conditional Formatting Lanjutan (15 menit)
a) CF Baris Bergantian: =MOD(ROW(),2)=0 -> Light Blue Fill (setiap baris genap)
b) CF untuk duplikat NIS: Home > CF > Highlight Cell Rules > Duplicate Values
c) Data Validation: NIS harus 7 digit angka. Data > Data Validation > Text Length = 7
d) Proteksi sheet: Review > Protect Sheet, beri password "pts2025"
### Soal 7 — Final Check (5 menit)
Ceklist sebelum kumpul:
[] Semua rumus benar [] CF teraplikasi [] Data tidak error [] Print preview rapi





---

### 🧠 Memahami — Petunjuk & Informasi





















- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagian mana yang masih sulit dipahami?

### 🔧 Mengaplikasi — Soal & Tugas


### 🔍 Merefleksi — Refleksi & Evaluasi

- Skala pemahaman diri: ___/10


