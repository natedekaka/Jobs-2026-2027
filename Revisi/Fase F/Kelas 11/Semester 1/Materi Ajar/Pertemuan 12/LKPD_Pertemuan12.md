# LEMBAR KERJA PESERTA DIDIK (LKPD)
## Pertemuan 12 (S1) – Fungsi Lanjut Excel
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*

| Nama | ____________________ |
|---|---|
| Kelas | ____________________ |





### 🧠 Memahami — Membangun Pemahaman Awal

### Aktivitas 1 — LEFT, RIGHT, MID (Individu, 20 menit)
Data NIS: "2025001" (4 digit tahun + 3 digit nomor urut)
a) =LEFT(A2,4) -> hasil: "_____"
b) =RIGHT(A2,3) -> hasil: "_____"
c) =MID(A2,5,1) -> hasil: "_____"
d) =MID(A2,5,3) -> hasil: "_____"
e) Gabungan: =LEFT(A2,4) & "-" & RIGHT(A2,3) -> hasil: "_____"

### Aktivitas 2 — LEN & FIND (Berpasangan, 20 menit)
Nama: "Andi Prasetyo"
a) =LEN("Andi Prasetyo") -> _____
b) =FIND(" ", "Andi Prasetyo") -> _____ (posisi spasi)
c) =LEFT("Andi Prasetyo", FIND(" ","Andi Prasetyo")-1) -> "_____"
d) =MID("Andi Prasetyo", FIND(" ","Andi Prasetyo")+1, 99) -> "_____"





### 🔧 Mengaplikasi — Praktik & Penerapan

### Aktivitas 3 — UPPER, LOWER, PROPER (Individu, 15 menit)
a) =UPPER("andi prasetyo") -> "_____"
b) =LOWER("ANDI PRASETYO") -> "_____"
c) =PROPER("andi prasetyo") -> "_____"
d) =LOWER(LEFT("Andi Prasetyo",1)) & "." & LOWER(MID("Andi Prasetyo",FIND(" ","Andi Prasetyo")+1,99)) & "@sma6.sch.id" -> "_____"


Gunakan TRANSPOSE untuk mengubah baris jadi kolom!
Hasil: kolom apa saja yang terbentuk? _____, _____, _____, _____
Gunakan Data > Text to Columns > Delimited > Pilih "-"
Data: "Andi-Prasetyo-2008-85" di sel A1.
d) CF: Email valid jika mengandung "@" (ISNUMBER+FIND)
c) Usia: DATEDIF + TODAY()
b) Email: lower(nama depan + "." + nama belakang + "@sma6.sch.id")
a) NIS: "2025001", "2025002", ... format: "2025-001"
Buat 5 data siswa: No | NIS | Nama | Tgl Lahir | Email | Usia
Skala: ___/10. Fungsi teks tersulit: _______________ Kegunaan DATEDIF: _______________
### Aktivitas 4 — DATEDIF (Kelompok, 20 menit)
Tgl Lahir: 17-Agustus-2008, Hari ini: 1-Januari-2026
a) =DATEDIF(C2, TODAY(), "Y") -> usia dalam tahun: _____
b) =DATEDIF(C2, TODAY(), "YM") -> sisa bulan setelah tahun: _____
c) =DATEDIF(C2, TODAY(), "MD") -> sisa hari setelah bulan: _____
d) =DATEDIF(C2, TODAY(), "Y") & " tahun " & DATEDIF(C2,TODAY(),"YM") & " bulan" -> "_____"

### Aktivitas 5 — Studi Kasus (Individu, 15 menit)
Buat email siswa: Nama="Andi Prasetyo", NIS="2025001".
Email: ___________________ @sma6.sch.id (gunakan LOWER, LEFT, MID/FIND)
NIS Format: "2025-001" (gunakan LEFT, RIGHT, &)

Skala: ___/10. Fungsi teks tersulit: _______________ Kegunaan DATEDIF: _______________

### Aktivitas 6 — Studi Kasus NIS & Email (Individu, 15 menit)
Buat 5 data siswa: No | NIS | Nama | Tgl Lahir | Email | Usia
a) NIS: "2025001", "2025002", ... format: "2025-001"
b) Email: lower(nama depan + "." + nama belakang + "@sma6.sch.id")
c) Usia: DATEDIF + TODAY()
d) CF: Email valid jika mengandung "@" (ISNUMBER+FIND)

### Aktivitas 7 — Text to Columns (Individu, 10 menit)
Data: "Andi-Prasetyo-2008-85" di sel A1.
Gunakan Data > Text to Columns > Delimited > Pilih "-"
Hasil: kolom apa saja yang terbentuk? _____, _____, _____, _____
Gunakan TRANSPOSE untuk mengubah baris jadi kolom!


- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagian mana yang masih sulit dipahami?
- Skala pemahaman diri: ___/10


### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagian mana yang masih sulit dipahami?
- Skala pemahaman diri: ___/10

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 1**
