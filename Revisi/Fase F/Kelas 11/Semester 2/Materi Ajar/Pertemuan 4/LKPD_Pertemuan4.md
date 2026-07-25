# LKPD Pert 4 (S2) – IF Percabangan
*Mengacu pada Panduan Mapel 2025; INFORMATIKA Fase D-F — pendekatan Pembelajaran Mendalam (Memahami → Mengaplikasi → Merefleksi)*
| Nama | ____________________ |
|---|---|
| Kelas | ____________________ |





### 🧠 Memahami — Membangun Pemahaman Awal

### Aktivitas 1 — IF Sederhana (Individu, 20 menit)
Buat program: input nilai, jika >= 70 cetak "Lulus".
```python
nilai = int(input("Nilai: "))
if nilai >= 70:
    print("Lulus")
```

### Aktivitas 2 — IF-ELSE (Berpasangan, 20 menit)
Kembangkan program: jika >= 70 "Lulus", jika tidak "Tidak Lulus".

### Aktivitas 3 — IF-ELIF-ELSE (Individu, 25 menit)
Buat program predikat nilai:
>=85=A, >=70=B, >=55=C, <55=D.
Uji dengan nilai: 90, 75, 60, 40.





### 🔧 Mengaplikasi — Praktik & Penerapan

### Aktivitas 4 — IF dengan AND/OR (Kelompok, 20 menit)
Buat program cek kesehatan:
Input suhu dan batuk. Jika suhu>37.5 AND batuk=="ya": "Periksa Dokter". Jika hanya salah satu: "Istirahat". Jika tidak ada: "Sehat".


Uji: 10+5=___ 20/4=___ 7*3=___ 15-8=___
Gunakan IF/ELIF/ELSE untuk memproses, cetak hasil.
Buat program: input 2 angka dan operator (+, -, *, /).
Mengapa "MINGGU" tidak terdeteksi? _______________________________
Uji: hari=Sabtu -> _____ hari=Senin -> _____ hari=MINGGU -> _____
```
    print("Masuk sekolah")
else:
    print("Libur!")
if hari == "Sabtu" or hari == "Minggu":
hari = input("Hari: ")
```python
Uji: L,20 -> _____ P,15 -> _____ L,12 -> _____
Jika P: jika usia>=17 "Wanita Dewasa", jika tidak "Anak Perempuan"
Jika L: jika usia>=17 "Pria Dewasa", jika tidak "Anak Laki-laki"
Buat program: input jenis_kelamin (L/P) dan usia.
Uji: kata_sandi=admin123 -> _____ kata_sandi=halo -> _____
```
    print("Akses ditolak")
else:
    print("Akses diterima")
if kata_sandi == "admin123":
kata_sandi = input("Kata sandi: ")
```python
Skala: ___/10. IF bersarang: _________________
### Aktivitas 5 — Tantangan (Individu, 10 menit)
Buat program: input 3 angka, cetak yang terbesar.

Skala: ___/10. IF bersarang: _________________

### Aktivitas 6 — IF dengan String (Individu, 10 menit)
```python
kata_sandi = input("Kata sandi: ")
if kata_sandi == "admin123":
    print("Akses diterima")
else:
    print("Akses ditolak")
```
Uji: kata_sandi=admin123 -> _____ kata_sandi=halo -> _____

### Aktivitas 7 — Nested IF (Berpasangan, 10 menit)
Buat program: input jenis_kelamin (L/P) dan usia.
Jika L: jika usia>=17 "Pria Dewasa", jika tidak "Anak Laki-laki"
Jika P: jika usia>=17 "Wanita Dewasa", jika tidak "Anak Perempuan"
Uji: L,20 -> _____ P,15 -> _____ L,12 -> _____

### Aktivitas 8 — IF dengan OR (Individu, 10 menit)
```python
hari = input("Hari: ")
if hari == "Sabtu" or hari == "Minggu":
    print("Libur!")
else:
    print("Masuk sekolah")
```
Uji: hari=Sabtu -> _____ hari=Senin -> _____ hari=MINGGU -> _____
Mengapa "MINGGU" tidak terdeteksi? _______________________________

### Aktivitas 9 — Kalkulator IF (Berpasangan, 10 menit)
Buat program: input 2 angka dan operator (+, -, *, /).
Gunakan IF/ELIF/ELSE untuk memproses, cetak hasil.
Uji: 10+5=___ 20/4=___ 7*3=___ 15-8=___


- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagian mana yang masih sulit dipahami?
- Skala pemahaman diri: ___/10


### 🔍 Merefleksi — Refleksi & Evaluasi

- Apa konsep paling penting yang kamu pelajari hari ini?
- Bagian mana yang masih sulit dipahami?
- Skala pemahaman diri: ___/10

---
**MGMP Informatika SMAN 6 Cimahi — Fase F (Kelas XI) Semester 2**
